# Comparing `tmp/pytheus_backend_rs-0.0.7.tar.gz` & `tmp/pytheus_backend_rs-0.0.8.tar.gz`

## Comparing `pytheus_backend_rs-0.0.7.tar` & `pytheus_backend_rs-0.0.8.tar`

### file list

```diff
@@ -1,10 +1,12 @@
--rw-r--r--   0        0        0      404 1970-01-01 00:00:00.000000 pytheus_backend_rs-0.0.7/Cargo.toml
--rw-r--r--   0     1001      123     2792 2023-06-30 23:27:45.000000 pytheus_backend_rs-0.0.7/.github/workflows/CI.yml
--rw-r--r--   0     1001      123      685 2023-06-30 23:27:45.000000 pytheus_backend_rs-0.0.7/.gitignore
--rw-r--r--   0     1001      123    11357 2023-06-30 23:27:45.000000 pytheus_backend_rs-0.0.7/LICENSE
--rw-r--r--   0     1001      123      620 2023-06-30 23:27:45.000000 pytheus_backend_rs-0.0.7/pyproject.toml
--rw-r--r--   0     1001      123    14381 2023-06-30 23:27:45.000000 pytheus_backend_rs-0.0.7/src/lib.rs
--rw-r--r--   0     1001      123        0 2023-06-30 23:27:45.000000 pytheus_backend_rs-0.0.7/tests/__init__.py
--rw-r--r--   0     1001      123     5615 2023-06-30 23:27:45.000000 pytheus_backend_rs-0.0.7/tests/test_redis.py
--rw-r--r--   0     1001      123    13922 2023-06-30 23:27:45.000000 pytheus_backend_rs-0.0.7/Cargo.lock
--rw-r--r--   0        0        0      530 1970-01-01 00:00:00.000000 pytheus_backend_rs-0.0.7/PKG-INFO
+-rw-r--r--   0        0        0      404 1970-01-01 00:00:00.000000 pytheus_backend_rs-0.0.8/Cargo.toml
+-rw-r--r--   0     1001      123     2792 2023-07-23 14:32:20.000000 pytheus_backend_rs-0.0.8/.github/workflows/CI.yml
+-rw-r--r--   0     1001      123      685 2023-07-23 14:32:20.000000 pytheus_backend_rs-0.0.8/.gitignore
+-rw-r--r--   0     1001      123    11357 2023-07-23 14:32:20.000000 pytheus_backend_rs-0.0.8/LICENSE
+-rw-r--r--   0     1001      123       53 2023-07-23 14:32:20.000000 pytheus_backend_rs-0.0.8/README.md
+-rw-r--r--   0     1001      123      620 2023-07-23 14:32:20.000000 pytheus_backend_rs-0.0.8/pyproject.toml
+-rw-r--r--   0     1001      123     2754 2023-07-23 14:32:20.000000 pytheus_backend_rs-0.0.8/src/atomic.rs
+-rw-r--r--   0     1001      123    15391 2023-07-23 14:32:20.000000 pytheus_backend_rs-0.0.8/src/lib.rs
+-rw-r--r--   0     1001      123        0 2023-07-23 14:32:20.000000 pytheus_backend_rs-0.0.8/tests/__init__.py
+-rw-r--r--   0     1001      123     5615 2023-07-23 14:32:20.000000 pytheus_backend_rs-0.0.8/tests/test_redis.py
+-rw-r--r--   0     1001      123    13922 2023-07-23 14:32:26.000000 pytheus_backend_rs-0.0.8/Cargo.lock
+-rw-r--r--   0        0        0      653 1970-01-01 00:00:00.000000 pytheus_backend_rs-0.0.8/PKG-INFO
```

### Comparing `pytheus_backend_rs-0.0.7/.github/workflows/CI.yml` & `pytheus_backend_rs-0.0.8/.github/workflows/CI.yml`

 * *Files identical despite different names*

### Comparing `pytheus_backend_rs-0.0.7/.gitignore` & `pytheus_backend_rs-0.0.8/.gitignore`

 * *Files identical despite different names*

### Comparing `pytheus_backend_rs-0.0.7/LICENSE` & `pytheus_backend_rs-0.0.8/LICENSE`

 * *Files identical despite different names*

### Comparing `pytheus_backend_rs-0.0.7/pyproject.toml` & `pytheus_backend_rs-0.0.8/pyproject.toml`

 * *Files identical despite different names*

### Comparing `pytheus_backend_rs-0.0.7/src/lib.rs` & `pytheus_backend_rs-0.0.8/src/lib.rs`

 * *Files 3% similar despite different names*

```diff
@@ -1,16 +1,19 @@
+mod atomic;
+
 use crossbeam::channel;
 use itertools::Itertools;
 use log::{error, info};
 use pyo3::exceptions::PyException;
 use pyo3::intern;
 use pyo3::prelude::*;
 use pyo3::types::{PyDict, PyType};
 use redis::ConnectionLike;
 use std::collections::HashMap;
+use std::sync::atomic::Ordering;
 use std::sync::{mpsc, Mutex, OnceLock};
 use std::thread;
 
 // This could be completely wrong, not sure if it would break the channel, let's try 🤞
 static REDIS_JOB_TX: OnceLock<Mutex<mpsc::Sender<RedisJob>>> = OnceLock::new();
 static REDIS_PIPELINE_JOB_TX: OnceLock<Mutex<channel::Sender<RedisPipelineJob>>> = OnceLock::new();
 const EXPIRE_KEY_SECONDS: usize = 3600;
@@ -454,17 +457,58 @@
 
     fn get(&self) -> f64 {
         let data = self.value.lock().unwrap();
         *data
     }
 }
 
+#[pyclass]
+struct SingleProcessAtomicBackend {
+    #[pyo3(get)]
+    config: Py<PyDict>,
+    #[pyo3(get)]
+    metric: Py<PyAny>,
+    #[pyo3(get)]
+    histogram_bucket: Option<String>,
+    value: atomic::AtomicF64,
+}
+
+#[pymethods]
+impl SingleProcessAtomicBackend {
+    #[new]
+    fn new(config: &PyDict, metric: &PyAny, histogram_bucket: Option<String>) -> Self {
+        Self {
+            config: config.into(),
+            metric: metric.into(),
+            histogram_bucket,
+            value: atomic::AtomicF64::new(0.0),
+        }
+    }
+
+    fn inc(&mut self, value: f64) {
+        self.value.fetch_add(value, Ordering::Relaxed);
+    }
+
+    fn dec(&mut self, value: f64) {
+        self.value.fetch_sub(value, Ordering::Relaxed);
+    }
+
+    fn set(&mut self, value: f64) {
+        self.value.store(value, Ordering::Relaxed);
+    }
+
+    fn get(&self) -> f64 {
+        self.value.load(Ordering::Relaxed)
+    }
+}
+
 /// A Python module implemented in Rust.
 #[pymodule]
 fn pytheus_backend_rs(_py: Python, m: &PyModule) -> PyResult<()> {
     pyo3_log::init();
 
     m.add_class::<RedisBackend>()?;
     m.add_class::<SingleProcessBackend>()?;
+    m.add_class::<SingleProcessAtomicBackend>()?;
     m.add_class::<OutSample>()?;
     Ok(())
 }
```

### Comparing `pytheus_backend_rs-0.0.7/tests/test_redis.py` & `pytheus_backend_rs-0.0.8/tests/test_redis.py`

 * *Files identical despite different names*

### Comparing `pytheus_backend_rs-0.0.7/Cargo.lock` & `pytheus_backend_rs-0.0.8/Cargo.lock`

 * *Files 0% similar despite different names*

```diff
@@ -305,15 +305,15 @@
  "proc-macro2",
  "quote",
  "syn",
 ]
 
 [[package]]
 name = "pytheus-backend-rs"
-version = "0.0.7"
+version = "0.0.8"
 dependencies = [
  "crossbeam",
  "itertools",
  "log",
  "pyo3",
  "pyo3-log",
  "r2d2",
```

### Comparing `pytheus_backend_rs-0.0.7/PKG-INFO` & `pytheus_backend_rs-0.0.8/PKG-INFO`

 * *Files 15% similar despite different names*

```diff
@@ -1,13 +1,19 @@
 Metadata-Version: 2.1
 Name: pytheus-backend-rs
-Version: 0.0.7
+Version: 0.0.8
 Classifier: Programming Language :: Rust
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 License-File: LICENSE
 Author-email: Llandy Riveron Del Risco <llandy3d@gmail.com>
 Requires-Python: >=3.8
+Description-Content-Type: text/markdown; charset=UTF-8; variant=GFM
+
+# pytheus-backend-rs
+
+https://pythe.us/rust_backend/
+
```

