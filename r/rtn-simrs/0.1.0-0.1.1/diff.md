# Comparing `tmp/rtn_simrs-0.1.0.tar.gz` & `tmp/rtn_simrs-0.1.1.tar.gz`

## Comparing `rtn_simrs-0.1.0.tar` & `rtn_simrs-0.1.1.tar`

### file list

```diff
@@ -1,5 +1,5 @@
--rw-r--r--   0        0        0      279 1970-01-01 00:00:00.000000 rtn_simrs-0.1.0/Cargo.toml
--rw-r--r--   0     1000     1000      369 2023-07-23 10:53:22.000000 rtn_simrs-0.1.0/pyproject.toml
--rw-r--r--   0     1000     1000     2059 2023-07-23 11:36:11.000000 rtn_simrs-0.1.0/src/lib.rs
--rw-r--r--   0     1000     1000     9472 2023-07-23 11:19:37.000000 rtn_simrs-0.1.0/Cargo.lock
--rw-r--r--   0        0        0      258 1970-01-01 00:00:00.000000 rtn_simrs-0.1.0/PKG-INFO
+-rw-r--r--   0        0        0      279 1970-01-01 00:00:00.000000 rtn_simrs-0.1.1/Cargo.toml
+-rw-r--r--   0     1000     1000      369 2023-07-23 10:53:22.000000 rtn_simrs-0.1.1/pyproject.toml
+-rw-r--r--   0     1000     1000     2914 2023-07-23 17:07:49.000000 rtn_simrs-0.1.1/src/lib.rs
+-rw-r--r--   0     1000     1000     9472 2023-07-23 17:11:53.000000 rtn_simrs-0.1.1/Cargo.lock
+-rw-r--r--   0        0        0      258 1970-01-01 00:00:00.000000 rtn_simrs-0.1.1/PKG-INFO
```

### Comparing `rtn_simrs-0.1.0/src/lib.rs` & `rtn_simrs-0.1.1/src/lib.rs`

 * *Files 12% similar despite different names*

```diff
@@ -1,70 +1,95 @@
 use pyo3::prelude::*;
-use rand::{distributions::{Uniform}, rngs::ThreadRng};
 use rand::seq::SliceRandom;
-use rand_distr::{Poisson, Distribution};
+use rand::{distributions::Uniform, rngs::ThreadRng};
+use rand_distr::{Distribution, Poisson};
 
 pub const STATES: [f64; 2] = [-1., 1.];
 
 fn gen_rtn(fs: f64, scale: usize, a: f64, b: f64, rtn_len: usize, rng: &mut ThreadRng) -> Vec<f64> {
     let mut rtn = vec![0.0; rtn_len as usize];
-    
+
+    // println!("scale: {}", scale);
     let poi = Poisson::new(scale as f64).unwrap();
     let mut state = *STATES.choose(rng).unwrap();
     let mut poi_iter = poi.sample_iter(rng);
 
-
     let mut actual_len: usize = 0;
     let mut n: usize = 0;
-    
+
     while actual_len < rtn_len && n < rtn_len {
-    let time = poi_iter.next().unwrap().round() as usize;
-      if state < 0. {
-        rtn[actual_len..rtn_len.min(actual_len + time)].fill(STATES[0]);
-        actual_len = actual_len + time;
-        state = STATES[1];
-      } else {
-        rtn[actual_len..rtn_len.min(actual_len + time)].fill(STATES[1]);
-        actual_len = actual_len + time;
-        state = STATES[0];
-      }
-      n += 1
+        let time = poi_iter.next().unwrap().round() as usize;
+        if state < 0. {
+            rtn[actual_len..rtn_len.min(actual_len + time)].fill(STATES[0]);
+            actual_len = actual_len + time;
+            state = STATES[1];
+        } else {
+            rtn[actual_len..rtn_len.min(actual_len + time)].fill(STATES[1]);
+            actual_len = actual_len + time;
+            state = STATES[0];
+        }
+        n += 1
     }
+
     rtn
 }
 
 fn gen_scales(scales: &mut Vec<usize>, a: f64, b: f64, rng: &mut ThreadRng) {
     let between = Uniform::try_from(a.ln()..b.ln()).unwrap();
     for i in 0..scales.len() {
         scales[i] = between.sample(rng).exp().round() as usize;
     }
 }
 
 /// Formats the sum of two numbers as string.
 #[pyfunction]
 fn gen_n_rtn(n: usize, fs: f64, a: f64, b: f64, rtn_len: usize) -> PyResult<Vec<f64>> {
-    let mut rng = rand::thread_rng();
-    let mut scales: Vec<usize> = vec![0; n as usize];
-    gen_scales(&mut scales, a, b, &mut rng);
-    let mut res = gen_rtn(fs, scales[0], a, b, rtn_len, &mut rng);
-
-    if n-1 > 0 {
-        for _i in 1..n-1 {
-            add(&mut res, gen_rtn(fs, scales[_i], a, b, rtn_len, &mut rng));
-        }
+    let available_threads = std::thread::available_parallelism().unwrap();
+    let total_n = n;
+    let mut join_handles = vec![];
+
+    for _i in 0..available_threads.into() {
+        join_handles.push(std::thread::spawn({
+            let n;
+            if _i == 0 {
+                n = total_n / available_threads + total_n % available_threads;
+            } else {
+                n = total_n / available_threads;
+            }
+            move || {
+                let mut rng = rand::thread_rng();
+                let mut scales: Vec<usize> = vec![0; n as usize];
+                gen_scales(&mut scales, a, b, &mut rng);
+                let mut res = gen_rtn(fs, scales[0], a, b, rtn_len, &mut rng);
+
+                if n - 1 > 0 {
+                    for _i in 1..n - 1 {
+                        add(&mut res, gen_rtn(fs, scales[_i], a, b, rtn_len, &mut rng));
+                    }
+                }
+                res
+            }
+        }));
+    }
+
+    let mut res = vec![0.0; rtn_len];
+
+    for handle in join_handles.into_iter() {
+        let handle_res = handle.join().unwrap();
+        add(&mut res, handle_res);
     }
 
     Ok(res)
 }
 
 fn add(a: &mut Vec<f64>, b: Vec<f64>) {
-    for (i,  bval) in b.iter().enumerate() {
+    for (i, bval) in b.iter().enumerate() {
         a[i] += bval;
     }
 }
 
 /// A Python module implemented in Rust.
 #[pymodule]
 fn rtn_simrs(_py: Python, m: &PyModule) -> PyResult<()> {
     m.add_function(wrap_pyfunction!(gen_n_rtn, m)?)?;
     Ok(())
-}
+}
```

### Comparing `rtn_simrs-0.1.0/Cargo.lock` & `rtn_simrs-0.1.1/Cargo.lock`

 * *Files 0% similar despite different names*

```diff
@@ -238,15 +238,15 @@
 checksum = "567664f262709473930a4bf9e51bf2ebf3348f2e748ccc50dea20646858f8f29"
 dependencies = [
  "bitflags",
 ]
 
 [[package]]
 name = "rtn_simrs"
-version = "0.1.0"
+version = "0.1.1"
 dependencies = [
  "pyo3",
  "rand",
  "rand_distr",
 ]
 
 [[package]]
```

