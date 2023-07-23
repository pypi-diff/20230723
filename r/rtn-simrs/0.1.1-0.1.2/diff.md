# Comparing `tmp/rtn_simrs-0.1.1.tar.gz` & `tmp/rtn_simrs-0.1.2.tar.gz`

## Comparing `rtn_simrs-0.1.1.tar` & `rtn_simrs-0.1.2.tar`

### file list

```diff
@@ -1,5 +1,5 @@
--rw-r--r--   0        0        0      279 1970-01-01 00:00:00.000000 rtn_simrs-0.1.1/Cargo.toml
--rw-r--r--   0     1000     1000      369 2023-07-23 10:53:22.000000 rtn_simrs-0.1.1/pyproject.toml
--rw-r--r--   0     1000     1000     2914 2023-07-23 17:07:49.000000 rtn_simrs-0.1.1/src/lib.rs
--rw-r--r--   0     1000     1000     9472 2023-07-23 17:11:53.000000 rtn_simrs-0.1.1/Cargo.lock
--rw-r--r--   0        0        0      258 1970-01-01 00:00:00.000000 rtn_simrs-0.1.1/PKG-INFO
+-rw-r--r--   0        0        0      279 1970-01-01 00:00:00.000000 rtn_simrs-0.1.2/Cargo.toml
+-rw-r--r--   0     1000     1000      369 2023-07-23 10:53:22.000000 rtn_simrs-0.1.2/pyproject.toml
+-rw-r--r--   0     1000     1000     2927 2023-07-23 17:25:11.000000 rtn_simrs-0.1.2/src/lib.rs
+-rw-r--r--   0     1000     1000     9472 2023-07-23 17:25:33.000000 rtn_simrs-0.1.2/Cargo.lock
+-rw-r--r--   0        0        0      258 1970-01-01 00:00:00.000000 rtn_simrs-0.1.2/PKG-INFO
```

### Comparing `rtn_simrs-0.1.1/src/lib.rs` & `rtn_simrs-0.1.2/src/lib.rs`

 * *Files 2% similar despite different names*

```diff
@@ -39,19 +39,19 @@
         scales[i] = between.sample(rng).exp().round() as usize;
     }
 }
 
 /// Formats the sum of two numbers as string.
 #[pyfunction]
 fn gen_n_rtn(n: usize, fs: f64, a: f64, b: f64, rtn_len: usize) -> PyResult<Vec<f64>> {
-    let available_threads = std::thread::available_parallelism().unwrap();
+    let available_threads = usize::from(std::thread::available_parallelism().unwrap());
     let total_n = n;
     let mut join_handles = vec![];
 
-    for _i in 0..available_threads.into() {
+    for _i in 0..available_threads.min(n) {
         join_handles.push(std::thread::spawn({
             let n;
             if _i == 0 {
                 n = total_n / available_threads + total_n % available_threads;
             } else {
                 n = total_n / available_threads;
             }
```

### Comparing `rtn_simrs-0.1.1/Cargo.lock` & `rtn_simrs-0.1.2/Cargo.lock`

 * *Files 0% similar despite different names*

```diff
@@ -238,15 +238,15 @@
 checksum = "567664f262709473930a4bf9e51bf2ebf3348f2e748ccc50dea20646858f8f29"
 dependencies = [
  "bitflags",
 ]
 
 [[package]]
 name = "rtn_simrs"
-version = "0.1.1"
+version = "0.1.2"
 dependencies = [
  "pyo3",
  "rand",
  "rand_distr",
 ]
 
 [[package]]
```

