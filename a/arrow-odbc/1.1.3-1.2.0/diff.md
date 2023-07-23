# Comparing `tmp/arrow_odbc-1.1.3.tar.gz` & `tmp/arrow_odbc-1.2.0.tar.gz`

## Comparing `arrow_odbc-1.1.3.tar` & `arrow_odbc-1.2.0.tar`

### file list

```diff
@@ -1,45 +1,47 @@
--rw-r--r--   0        0        0      788 1970-01-01 00:00:00.000000 arrow_odbc-1.1.3/Cargo.toml
--rw-r--r--   0      501       20      136 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/.gitattributes
--rw-r--r--   0      501       20      131 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/.github/dependabot.yml
--rw-r--r--   0      501       20     1522 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/.github/workflows/test.yml
--rw-r--r--   0      501       20     1807 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/.github/workflows/wheel.yml
--rw-r--r--   0      501       20      286 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/.gitignore
--rw-r--r--   0      501       20      841 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/.readthedocs.yaml
--rw-r--r--   0      501       20     5119 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/Changelog.md
--rw-r--r--   0      501       20     1954 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/Contributing.md
--rw-r--r--   0      501       20     1069 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/LICENSE
--rw-r--r--   0      501       20     7729 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/README.md
--rw-r--r--   0      501       20       14 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/cbindgen.toml
--rw-r--r--   0      501       20      639 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/conftest.py
--rw-r--r--   0      501       20      638 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/doc/Makefile
--rw-r--r--   0      501       20      804 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/doc/make.bat
--rw-r--r--   0      501       20       16 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/doc/requirements.txt
--rw-r--r--   0      501       20      155 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/doc/source/arrow_odbc.rst
--rw-r--r--   0      501       20     1965 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/doc/source/conf.py
--rw-r--r--   0      501       20      458 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/doc/source/index.rst
--rw-r--r--   0      501       20       67 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/doc/source/modules.rst
--rw-r--r--   0      501       20      348 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/docker-compose.yml
--rw-r--r--   0      501       20      564 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/manylinux/Dockerfile
--rw-r--r--   0      501       20      121 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/manylinux/Readme.md
--rw-r--r--   0      501       20      148 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/manylinux/WHEEL
--rw-r--r--   0      501       20     1256 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/manylinux/build_wheel.sh
--rw-r--r--   0      501       20      649 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/pyproject.toml
--rw-r--r--   0      501       20      358 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/python/arrow_odbc/__init__.py
--rw-r--r--   0      501       20     1645 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/python/arrow_odbc/connect.py
--rw-r--r--   0      501       20      672 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/python/arrow_odbc/error.py
--rw-r--r--   0      501       20      791 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/python/arrow_odbc/log.py
--rw-r--r--   0      501       20    15067 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/python/arrow_odbc/reader.py
--rw-r--r--   0      501       20     9164 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/python/arrow_odbc/writer.py
--rw-r--r--   0      501       20     2322 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/src/error.rs
--rw-r--r--   0      501       20     2897 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/src/lib.rs
--rw-r--r--   0      501       20      655 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/src/logging.rs
--rw-r--r--   0      501       20     1239 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/src/parameter.rs
--rw-r--r--   0      501       20     2921 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/src/reader/arrow_odbc_reader.rs
--rw-r--r--   0      501       20     6502 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/src/reader.rs
--rw-r--r--   0      501       20     3545 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/src/writer.rs
--rw-r--r--   0      501       20        0 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/tests/__init__.py
--rw-r--r--   0      501       20     4115 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/tests/iris.csv
--rw-r--r--   0      501       20     2413 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/tests/iris.parquet
--rw-r--r--   0      501       20    19491 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/tests/test_arrow_odbc.py
--rw-r--r--   0      501       20    35078 2023-07-22 23:59:17.000000 arrow_odbc-1.1.3/Cargo.lock
--rw-r--r--   0        0        0     8261 1970-01-01 00:00:00.000000 arrow_odbc-1.1.3/PKG-INFO
+-rw-r--r--   0        0        0      788 1970-01-01 00:00:00.000000 arrow_odbc-1.2.0/Cargo.toml
+-rw-r--r--   0      501       20      136 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/.gitattributes
+-rw-r--r--   0      501       20      131 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/.github/dependabot.yml
+-rw-r--r--   0      501       20     1522 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/.github/workflows/test.yml
+-rw-r--r--   0      501       20     1807 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/.github/workflows/wheel.yml
+-rw-r--r--   0      501       20      286 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/.gitignore
+-rw-r--r--   0      501       20      841 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/.readthedocs.yaml
+-rw-r--r--   0      501       20     5239 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/Changelog.md
+-rw-r--r--   0      501       20     1954 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/Contributing.md
+-rw-r--r--   0      501       20     1069 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/LICENSE
+-rw-r--r--   0      501       20     7729 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/README.md
+-rw-r--r--   0      501       20       14 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/cbindgen.toml
+-rw-r--r--   0      501       20      639 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/conftest.py
+-rw-r--r--   0      501       20      638 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/doc/Makefile
+-rw-r--r--   0      501       20      804 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/doc/make.bat
+-rw-r--r--   0      501       20       16 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/doc/requirements.txt
+-rw-r--r--   0      501       20      155 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/doc/source/arrow_odbc.rst
+-rw-r--r--   0      501       20     1965 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/doc/source/conf.py
+-rw-r--r--   0      501       20      458 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/doc/source/index.rst
+-rw-r--r--   0      501       20       67 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/doc/source/modules.rst
+-rw-r--r--   0      501       20      348 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/docker-compose.yml
+-rw-r--r--   0      501       20      564 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/manylinux/Dockerfile
+-rw-r--r--   0      501       20      121 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/manylinux/Readme.md
+-rw-r--r--   0      501       20      148 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/manylinux/WHEEL
+-rw-r--r--   0      501       20     1256 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/manylinux/build_wheel.sh
+-rw-r--r--   0      501       20      649 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/pyproject.toml
+-rw-r--r--   0      501       20      445 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/python/arrow_odbc/__init__.py
+-rw-r--r--   0      501       20     1645 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/python/arrow_odbc/connect.py
+-rw-r--r--   0      501       20      672 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/python/arrow_odbc/error.py
+-rw-r--r--   0      501       20      801 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/python/arrow_odbc/log.py
+-rw-r--r--   0      501       20      579 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/python/arrow_odbc/pool.py
+-rw-r--r--   0      501       20    15067 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/python/arrow_odbc/reader.py
+-rw-r--r--   0      501       20     9164 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/python/arrow_odbc/writer.py
+-rw-r--r--   0      501       20     2322 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/src/error.rs
+-rw-r--r--   0      501       20     2907 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/src/lib.rs
+-rw-r--r--   0      501       20      655 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/src/logging.rs
+-rw-r--r--   0      501       20     1239 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/src/parameter.rs
+-rw-r--r--   0      501       20      421 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/src/pool.rs
+-rw-r--r--   0      501       20     2921 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/src/reader/arrow_odbc_reader.rs
+-rw-r--r--   0      501       20     6502 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/src/reader.rs
+-rw-r--r--   0      501       20     3545 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/src/writer.rs
+-rw-r--r--   0      501       20        0 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/tests/__init__.py
+-rw-r--r--   0      501       20     4115 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/tests/iris.csv
+-rw-r--r--   0      501       20     2413 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/tests/iris.parquet
+-rw-r--r--   0      501       20    19559 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/tests/test_arrow_odbc.py
+-rw-r--r--   0      501       20    35078 2023-07-23 15:13:10.000000 arrow_odbc-1.2.0/Cargo.lock
+-rw-r--r--   0        0        0     8261 1970-01-01 00:00:00.000000 arrow_odbc-1.2.0/PKG-INFO
```

### Comparing `arrow_odbc-1.1.3/Cargo.toml` & `arrow_odbc-1.2.0/Cargo.toml`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.3/.github/workflows/test.yml` & `arrow_odbc-1.2.0/.github/workflows/test.yml`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.3/.github/workflows/wheel.yml` & `arrow_odbc-1.2.0/.github/workflows/wheel.yml`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.3/.readthedocs.yaml` & `arrow_odbc-1.2.0/.readthedocs.yaml`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.3/Changelog.md` & `arrow_odbc-1.2.0/Changelog.md`

 * *Files 2% similar despite different names*

```diff
@@ -1,9 +1,13 @@
 # Changelog
 
+## 1.2.0
+
+- Introduce `enable_odbc_connection_pooling` to allow for reducing overhead then creating "new" connections.
+
 ## 1.1.3
 
 - Update Rust dependencies
 
 ## 1.1.2
 
 - Declare minimal version in pyproject.toml
```

### Comparing `arrow_odbc-1.1.3/Contributing.md` & `arrow_odbc-1.2.0/Contributing.md`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.3/LICENSE` & `arrow_odbc-1.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.3/README.md` & `arrow_odbc-1.2.0/README.md`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.3/conftest.py` & `arrow_odbc-1.2.0/conftest.py`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.3/doc/Makefile` & `arrow_odbc-1.2.0/doc/Makefile`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.3/doc/make.bat` & `arrow_odbc-1.2.0/doc/make.bat`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.3/doc/source/conf.py` & `arrow_odbc-1.2.0/doc/source/conf.py`

 * *Files 0% similar despite different names*

```diff
@@ -18,15 +18,15 @@
 # -- Project information -----------------------------------------------------
 
 project = "arrow-odbc"
 copyright = "2021, Markus Klein"
 author = "Markus Klein"
 
 # The full version, including alpha/beta/rc tags
-release = "1.1.3"
+release = "1.2.0"
 
 
 # -- General configuration ---------------------------------------------------
 
 # Add any Sphinx extension module names here, as strings. They can be
 # extensions coming with Sphinx (named 'sphinx.ext.*') or your custom
 # ones.
```

### Comparing `arrow_odbc-1.1.3/manylinux/Dockerfile` & `arrow_odbc-1.2.0/manylinux/Dockerfile`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.3/manylinux/build_wheel.sh` & `arrow_odbc-1.2.0/manylinux/build_wheel.sh`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.3/pyproject.toml` & `arrow_odbc-1.2.0/pyproject.toml`

 * *Files 22% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 build-backend = "maturin"
 
 [project]
 name = "arrow-odbc"
 authors = [{name = "Markus Klein"}]
 description="Read the data of an ODBC data source as sequence of Apache Arrow record batches."
 readme = "README.md"
-version = "1.1.3"
+version = "1.2.0"
 dependencies = ["cffi", "pyarrow >= 8.0.0"]
 
 [project.license]
 file = "LICENSE"
 
 [project.optional-dependencies]
 test = ["pytest < 8.0.0"]
```

### Comparing `arrow_odbc-1.1.3/python/arrow_odbc/connect.py` & `arrow_odbc-1.2.0/python/arrow_odbc/connect.py`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.3/python/arrow_odbc/error.py` & `arrow_odbc-1.2.0/python/arrow_odbc/error.py`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.3/python/arrow_odbc/log.py` & `arrow_odbc-1.2.0/python/arrow_odbc/log.py`

 * *Files 0% similar despite different names*

```diff
@@ -5,14 +5,15 @@
 def log_to_stderr(level: int = 1):
     """
     Activate logging from native code directly to standard error. In particular these logs contain
     diagnostic information emitted by ODBC. Call this method only once in your application
 
     :param level: Specifies the log level with which the standard error logger in rust is
         initialized.
+        
         * 0 - Error
         * 1 - Warning,
         * 2 - Info
         * 3 - Debug
         * 4 - Trace
 
         All diagnostics emitted by ODBC are usually warning. In case of an exeception multiple
```

### Comparing `arrow_odbc-1.1.3/python/arrow_odbc/reader.py` & `arrow_odbc-1.2.0/python/arrow_odbc/reader.py`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.3/python/arrow_odbc/writer.py` & `arrow_odbc-1.2.0/python/arrow_odbc/writer.py`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.3/src/error.rs` & `arrow_odbc-1.2.0/src/error.rs`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.3/src/lib.rs` & `arrow_odbc-1.2.0/src/lib.rs`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 //! Defines C bindings for `arrow-odbc` to enable using it from Python.
 mod error;
 mod logging;
 mod parameter;
+mod pool;
 mod reader;
 mod writer;
 
 use std::{borrow::Cow, ptr::null_mut, slice, str};
 
 use arrow_odbc::odbc_api::{escape_attribute_value, Connection, ConnectionOptions, Environment};
 use lazy_static::lazy_static;
```

### Comparing `arrow_odbc-1.1.3/src/logging.rs` & `arrow_odbc-1.2.0/src/logging.rs`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.3/src/parameter.rs` & `arrow_odbc-1.2.0/src/parameter.rs`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.3/src/reader/arrow_odbc_reader.rs` & `arrow_odbc-1.2.0/src/reader/arrow_odbc_reader.rs`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.3/src/reader.rs` & `arrow_odbc-1.2.0/src/reader.rs`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.3/src/writer.rs` & `arrow_odbc-1.2.0/src/writer.rs`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.3/tests/iris.csv` & `arrow_odbc-1.2.0/tests/iris.csv`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.3/tests/iris.parquet` & `arrow_odbc-1.2.0/tests/iris.parquet`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.3/tests/test_arrow_odbc.py` & `arrow_odbc-1.2.0/tests/test_arrow_odbc.py`

 * *Files 0% similar despite different names*

```diff
@@ -12,21 +12,22 @@
 from pytest import raises
 
 from arrow_odbc import (
     insert_into_table,
     from_table_to_db,
     read_arrow_batches_from_odbc,
     log_to_stderr,
+    enable_odbc_connection_pooling,
     Error,
 )
 
 MSSQL = "Driver={ODBC Driver 17 for SQL Server};Server=localhost;UID=SA;PWD=My@Test@Password1;"
 
 log_to_stderr()
-
+enable_odbc_connection_pooling()
 
 def test_should_report_error_on_invalid_connection_string_reading():
     """
     We want to forward the original ODBC errors to the end user. Of course foo
     is not a valid connection string. Therefore we want to see the creation of
     this connection fail, but with a nice error.
     """
```

### Comparing `arrow_odbc-1.1.3/Cargo.lock` & `arrow_odbc-1.2.0/Cargo.lock`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.3/PKG-INFO` & `arrow_odbc-1.2.0/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: arrow-odbc
-Version: 1.1.3
+Version: 1.2.0
 Requires-Dist: cffi
 Requires-Dist: pyarrow >=8.0.0
 Requires-Dist: pytest <8.0.0 ; extra == 'test'
 Provides-Extra: test
 License-File: LICENSE
 Summary: Read the data of an ODBC data source as sequence of Apache Arrow record batches.
 Author: Markus Klein
```

