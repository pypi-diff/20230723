# Comparing `tmp/punwrap-0.2.1.tar.gz` & `tmp/punwrap-0.2.2.tar.gz`

## Comparing `punwrap-0.2.1.tar` & `punwrap-0.2.2.tar`

### file list

```diff
@@ -1,7 +1,7 @@
--rw-r--r--   0        0        0      801 1970-01-01 00:00:00.000000 punwrap-0.2.1/Cargo.toml
--rw-rw-r--   0     1000     1000      850 2022-03-17 06:56:51.000000 punwrap-0.2.1/CHANGELOG.md
--rw-rw-r--   0     1000     1000    35149 2021-06-06 14:12:24.000000 punwrap-0.2.1/LICENSE
--rw-rw-r--   0     1000     1000      395 2022-03-17 06:43:29.000000 punwrap-0.2.1/README.md
--rw-rw-r--   0     1000     1000      252 2021-07-10 17:57:06.000000 punwrap-0.2.1/pyproject.toml
--rw-rw-r--   0     1000     1000      699 2021-06-06 15:30:12.000000 punwrap-0.2.1/src/lib.rs
--rw-r--r--   0        0        0      709 1970-01-01 00:00:00.000000 punwrap-0.2.1/PKG-INFO
+-rw-r--r--   0        0        0      801 1970-01-01 00:00:00.000000 punwrap-0.2.2/Cargo.toml
+-rw-rw-r--   0     1000     1000     1063 2023-07-23 07:13:00.000000 punwrap-0.2.2/CHANGELOG.md
+-rw-rw-r--   0     1000     1000    35149 2021-06-06 14:12:24.000000 punwrap-0.2.2/LICENSE
+-rw-rw-r--   0     1000     1000      395 2022-03-17 06:43:29.000000 punwrap-0.2.2/README.md
+-rw-rw-r--   0     1000     1000      252 2021-07-10 17:57:06.000000 punwrap-0.2.2/pyproject.toml
+-rw-rw-r--   0     1000     1000      698 2023-07-22 20:38:41.000000 punwrap-0.2.2/src/lib.rs
+-rw-r--r--   0        0        0      709 1970-01-01 00:00:00.000000 punwrap-0.2.2/PKG-INFO
```

### Comparing `punwrap-0.2.1/Cargo.toml` & `punwrap-0.2.2/Cargo.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [package]
 name = "punwrap"
-version = "0.2.1"
+version = "0.2.2"
 authors = ["Viktor Eikman <viktor.eikman@gmail.com>"]
 edition = "2018"
 description = "Python bindings for runwrap"
 readme = "README.md"
 repository = "https://github.com/veikman/punwrap"
 license = "GPL-3.0-or-later"
 keywords = ["text", "markdown", "vcs"]
```

### Comparing `punwrap-0.2.1/LICENSE` & `punwrap-0.2.2/LICENSE`

 * *Files identical despite different names*

### Comparing `punwrap-0.2.1/src/lib.rs` & `punwrap-0.2.2/src/lib.rs`

 * *Files 27% similar despite different names*

```diff
@@ -1,9 +1,8 @@
 /// Wrap each of the interface functions of runwrap.
-
 use pyo3::prelude::*;
 use pyo3::wrap_pyfunction;
 use runwrap;
 
 #[pyfunction]
 fn wrap(raw: &str, width: usize) -> PyResult<String> {
     Ok(runwrap::wrap(raw, width))
```

### Comparing `punwrap-0.2.1/PKG-INFO` & `punwrap-0.2.2/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: punwrap
-Version: 0.2.1
+Version: 0.2.2
 Summary: Python bindings for runwrap
 Keywords: text,markdown,vcs
 Author: Viktor Eikman <viktor.eikman@gmail.com>
 Author-email: Viktor Eikman <viktor.eikman@gmail.com>
 License: GPL-3.0-or-later
 Description-Content-Type: text/markdown; charset=UTF-8; variant=GFM
```

