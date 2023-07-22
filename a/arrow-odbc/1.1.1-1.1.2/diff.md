# Comparing `tmp/arrow_odbc-1.1.1.tar.gz` & `tmp/arrow_odbc-1.1.2.tar.gz`

## Comparing `arrow_odbc-1.1.1.tar` & `arrow_odbc-1.1.2.tar`

### file list

```diff
@@ -1,45 +1,45 @@
--rw-r--r--   0        0        0      788 1970-01-01 00:00:00.000000 arrow_odbc-1.1.1/Cargo.toml
--rw-r--r--   0        0        0      136 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/.gitattributes
--rw-r--r--   0        0        0      131 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/.github/dependabot.yml
--rw-r--r--   0        0        0     1522 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/.github/workflows/test.yml
--rw-r--r--   0        0        0     1807 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/.github/workflows/wheel.yml
--rw-r--r--   0        0        0      286 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/.gitignore
--rw-r--r--   0        0        0      841 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/.readthedocs.yaml
--rw-r--r--   0        0        0     5026 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/Changelog.md
--rw-r--r--   0        0        0     1954 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/Contributing.md
--rw-r--r--   0        0        0     1069 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/LICENSE
--rw-r--r--   0        0        0     7727 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/README.md
--rw-r--r--   0        0        0       14 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/cbindgen.toml
--rw-r--r--   0        0        0      639 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/conftest.py
--rw-r--r--   0        0        0      638 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/doc/Makefile
--rw-r--r--   0        0        0      804 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/doc/make.bat
--rw-r--r--   0        0        0       16 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/doc/requirements.txt
--rw-r--r--   0        0        0      155 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/doc/source/arrow_odbc.rst
--rw-r--r--   0        0        0     1965 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/doc/source/conf.py
--rw-r--r--   0        0        0      458 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/doc/source/index.rst
--rw-r--r--   0        0        0       67 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/doc/source/modules.rst
--rw-r--r--   0        0        0      348 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/docker-compose.yml
--rw-r--r--   0        0        0      564 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/manylinux/Dockerfile
--rw-r--r--   0        0        0      121 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/manylinux/Readme.md
--rw-r--r--   0        0        0      148 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/manylinux/WHEEL
--rw-r--r--   0        0        0     1256 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/manylinux/build_wheel.sh
--rw-r--r--   0        0        0      640 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/pyproject.toml
--rw-r--r--   0        0        0      358 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/python/arrow_odbc/__init__.py
--rw-r--r--   0        0        0     1645 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/python/arrow_odbc/connect.py
--rw-r--r--   0        0        0      672 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/python/arrow_odbc/error.py
--rw-r--r--   0        0        0      791 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/python/arrow_odbc/log.py
--rw-r--r--   0        0        0    15067 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/python/arrow_odbc/reader.py
--rw-r--r--   0        0        0     9164 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/python/arrow_odbc/writer.py
--rw-r--r--   0        0        0     2322 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/src/error.rs
--rw-r--r--   0        0        0     2897 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/src/lib.rs
--rw-r--r--   0        0        0      685 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/src/logging.rs
--rw-r--r--   0        0        0     1239 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/src/parameter.rs
--rw-r--r--   0        0        0     3030 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/src/reader/arrow_odbc_reader.rs
--rw-r--r--   0        0        0     6484 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/src/reader.rs
--rw-r--r--   0        0        0     3613 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/src/writer.rs
--rw-r--r--   0        0        0        0 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/tests/__init__.py
--rw-r--r--   0        0        0     4115 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/tests/iris.csv
--rw-r--r--   0        0        0     2413 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/tests/iris.parquet
--rw-r--r--   0        0        0    19491 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/tests/test_arrow_odbc.py
--rw-r--r--   0        0        0    34251 2023-06-08 18:27:26.000000 arrow_odbc-1.1.1/Cargo.lock
--rw-r--r--   0        0        0     8251 1970-01-01 00:00:00.000000 arrow_odbc-1.1.1/PKG-INFO
+-rw-r--r--   0        0        0      788 1970-01-01 00:00:00.000000 arrow_odbc-1.1.2/Cargo.toml
+-rw-r--r--   0        0        0      136 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/.gitattributes
+-rw-r--r--   0        0        0      131 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/.github/dependabot.yml
+-rw-r--r--   0        0        0     1522 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/.github/workflows/test.yml
+-rw-r--r--   0        0        0     1807 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/.github/workflows/wheel.yml
+-rw-r--r--   0        0        0      286 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/.gitignore
+-rw-r--r--   0        0        0      841 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/.readthedocs.yaml
+-rw-r--r--   0        0        0     5081 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/Changelog.md
+-rw-r--r--   0        0        0     1954 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/Contributing.md
+-rw-r--r--   0        0        0     1069 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/LICENSE
+-rw-r--r--   0        0        0     7729 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/README.md
+-rw-r--r--   0        0        0       14 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/cbindgen.toml
+-rw-r--r--   0        0        0      639 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/conftest.py
+-rw-r--r--   0        0        0      638 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/doc/Makefile
+-rw-r--r--   0        0        0      804 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/doc/make.bat
+-rw-r--r--   0        0        0       16 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/doc/requirements.txt
+-rw-r--r--   0        0        0      155 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/doc/source/arrow_odbc.rst
+-rw-r--r--   0        0        0     1965 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/doc/source/conf.py
+-rw-r--r--   0        0        0      458 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/doc/source/index.rst
+-rw-r--r--   0        0        0       67 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/doc/source/modules.rst
+-rw-r--r--   0        0        0      348 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/docker-compose.yml
+-rw-r--r--   0        0        0      564 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/manylinux/Dockerfile
+-rw-r--r--   0        0        0      121 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/manylinux/Readme.md
+-rw-r--r--   0        0        0      148 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/manylinux/WHEEL
+-rw-r--r--   0        0        0     1256 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/manylinux/build_wheel.sh
+-rw-r--r--   0        0        0      649 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/pyproject.toml
+-rw-r--r--   0        0        0      358 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/python/arrow_odbc/__init__.py
+-rw-r--r--   0        0        0     1645 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/python/arrow_odbc/connect.py
+-rw-r--r--   0        0        0      672 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/python/arrow_odbc/error.py
+-rw-r--r--   0        0        0      791 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/python/arrow_odbc/log.py
+-rw-r--r--   0        0        0    15067 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/python/arrow_odbc/reader.py
+-rw-r--r--   0        0        0     9164 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/python/arrow_odbc/writer.py
+-rw-r--r--   0        0        0     2322 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/src/error.rs
+-rw-r--r--   0        0        0     2897 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/src/lib.rs
+-rw-r--r--   0        0        0      685 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/src/logging.rs
+-rw-r--r--   0        0        0     1239 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/src/parameter.rs
+-rw-r--r--   0        0        0     3030 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/src/reader/arrow_odbc_reader.rs
+-rw-r--r--   0        0        0     6484 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/src/reader.rs
+-rw-r--r--   0        0        0     3613 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/src/writer.rs
+-rw-r--r--   0        0        0        0 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/tests/__init__.py
+-rw-r--r--   0        0        0     4115 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/tests/iris.csv
+-rw-r--r--   0        0        0     2413 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/tests/iris.parquet
+-rw-r--r--   0        0        0    19491 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/tests/test_arrow_odbc.py
+-rw-r--r--   0        0        0    34251 2023-07-22 23:13:55.000000 arrow_odbc-1.1.2/Cargo.lock
+-rw-r--r--   0        0        0     8261 1970-01-01 00:00:00.000000 arrow_odbc-1.1.2/PKG-INFO
```

### Comparing `arrow_odbc-1.1.1/Cargo.toml` & `arrow_odbc-1.1.2/Cargo.toml`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.1/.github/workflows/test.yml` & `arrow_odbc-1.1.2/.github/workflows/test.yml`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.1/.github/workflows/wheel.yml` & `arrow_odbc-1.1.2/.github/workflows/wheel.yml`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.1/.readthedocs.yaml` & `arrow_odbc-1.1.2/.readthedocs.yaml`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.1/Changelog.md` & `arrow_odbc-1.1.2/Changelog.md`

 * *Files 1% similar despite different names*

```diff
@@ -1,9 +1,13 @@
 # Changelog
 
+## 1.1.2
+
+- Declare minimal version in pyproject.toml
+
 ## 1.1.1
 
 - Fix version number in documentation.
 
 ## 1.1.0
 
 - Update Rust dependencies
```

### Comparing `arrow_odbc-1.1.1/Contributing.md` & `arrow_odbc-1.1.2/Contributing.md`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.1/LICENSE` & `arrow_odbc-1.1.2/LICENSE`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.1/README.md` & `arrow_odbc-1.1.2/README.md`

 * *Files 1% similar despite different names*

```diff
@@ -98,15 +98,15 @@
 ```
 
 `arrow-odbc` utilizes `cffi` and the Arrow C-Interface to glue Rust and Python code together. Therefore the wheel does not need to be build against the precise version either of Python or Arrow.
 
 ### Installing with conda
 
 ```shell
-conda install -c conda-forge turbodbc
+conda install -c conda-forge arrow-odbc
 ```
 
 Thanks to @timkpaine for maintaining the recipie!
 
 ### Building wheel from source
 
 There is no ready made wheel for the platform you want to target? Do not worry, you can probably build it from source.
```

### Comparing `arrow_odbc-1.1.1/conftest.py` & `arrow_odbc-1.1.2/conftest.py`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.1/doc/Makefile` & `arrow_odbc-1.1.2/doc/Makefile`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.1/doc/make.bat` & `arrow_odbc-1.1.2/doc/make.bat`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.1/doc/source/conf.py` & `arrow_odbc-1.1.2/doc/source/conf.py`

 * *Files 1% similar despite different names*

```diff
@@ -18,15 +18,15 @@
 # -- Project information -----------------------------------------------------
 
 project = "arrow-odbc"
 copyright = "2021, Markus Klein"
 author = "Markus Klein"
 
 # The full version, including alpha/beta/rc tags
-release = "1.1.1"
+release = "1.1.2"
 
 
 # -- General configuration ---------------------------------------------------
 
 # Add any Sphinx extension module names here, as strings. They can be
 # extensions coming with Sphinx (named 'sphinx.ext.*') or your custom
 # ones.
```

### Comparing `arrow_odbc-1.1.1/manylinux/Dockerfile` & `arrow_odbc-1.1.2/manylinux/Dockerfile`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.1/manylinux/build_wheel.sh` & `arrow_odbc-1.1.2/manylinux/build_wheel.sh`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.1/pyproject.toml` & `arrow_odbc-1.1.2/pyproject.toml`

 * *Files 19% similar despite different names*

```diff
@@ -3,16 +3,16 @@
 build-backend = "maturin"
 
 [project]
 name = "arrow-odbc"
 authors = [{name = "Markus Klein"}]
 description="Read the data of an ODBC data source as sequence of Apache Arrow record batches."
 readme = "README.md"
-version = "1.1.1"
-dependencies = ["cffi", "pyarrow"]
+version = "1.1.2"
+dependencies = ["cffi", "pyarrow >= 8.0.0"]
 
 [project.license]
 file = "LICENSE"
 
 [project.optional-dependencies]
 test = ["pytest < 8.0.0"]
```

### Comparing `arrow_odbc-1.1.1/python/arrow_odbc/connect.py` & `arrow_odbc-1.1.2/python/arrow_odbc/connect.py`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.1/python/arrow_odbc/error.py` & `arrow_odbc-1.1.2/python/arrow_odbc/error.py`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.1/python/arrow_odbc/log.py` & `arrow_odbc-1.1.2/python/arrow_odbc/log.py`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.1/python/arrow_odbc/reader.py` & `arrow_odbc-1.1.2/python/arrow_odbc/reader.py`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.1/python/arrow_odbc/writer.py` & `arrow_odbc-1.1.2/python/arrow_odbc/writer.py`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.1/src/error.rs` & `arrow_odbc-1.1.2/src/error.rs`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.1/src/lib.rs` & `arrow_odbc-1.1.2/src/lib.rs`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.1/src/logging.rs` & `arrow_odbc-1.1.2/src/logging.rs`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.1/src/parameter.rs` & `arrow_odbc-1.1.2/src/parameter.rs`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.1/src/reader/arrow_odbc_reader.rs` & `arrow_odbc-1.1.2/src/reader/arrow_odbc_reader.rs`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.1/src/reader.rs` & `arrow_odbc-1.1.2/src/reader.rs`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.1/src/writer.rs` & `arrow_odbc-1.1.2/src/writer.rs`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.1/tests/iris.csv` & `arrow_odbc-1.1.2/tests/iris.csv`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.1/tests/iris.parquet` & `arrow_odbc-1.1.2/tests/iris.parquet`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.1/tests/test_arrow_odbc.py` & `arrow_odbc-1.1.2/tests/test_arrow_odbc.py`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.1/Cargo.lock` & `arrow_odbc-1.1.2/Cargo.lock`

 * *Files identical despite different names*

### Comparing `arrow_odbc-1.1.1/PKG-INFO` & `arrow_odbc-1.1.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 Metadata-Version: 2.1
 Name: arrow-odbc
-Version: 1.1.1
+Version: 1.1.2
 Requires-Dist: cffi
-Requires-Dist: pyarrow
+Requires-Dist: pyarrow >=8.0.0
 Requires-Dist: pytest <8.0.0 ; extra == 'test'
 Provides-Extra: test
 License-File: LICENSE
 Summary: Read the data of an ODBC data source as sequence of Apache Arrow record batches.
 Author: Markus Klein
 Description-Content-Type: text/markdown; charset=UTF-8; variant=GFM
 Project-URL: repository, https://github.com/pacman82/arrow-odbc-py
@@ -112,15 +112,15 @@
 ```
 
 `arrow-odbc` utilizes `cffi` and the Arrow C-Interface to glue Rust and Python code together. Therefore the wheel does not need to be build against the precise version either of Python or Arrow.
 
 ### Installing with conda
 
 ```shell
-conda install -c conda-forge turbodbc
+conda install -c conda-forge arrow-odbc
 ```
 
 Thanks to @timkpaine for maintaining the recipie!
 
 ### Building wheel from source
 
 There is no ready made wheel for the platform you want to target? Do not worry, you can probably build it from source.
```

