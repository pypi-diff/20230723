# Comparing `tmp/rpy2-arrow-0.0.7.tar.gz` & `tmp/rpy2-arrow-0.0.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "rpy2-arrow-0.0.7.tar", last modified: Tue Nov  8 03:33:43 2022, max compression
+gzip compressed data, was "rpy2-arrow-0.0.8.tar", last modified: Sun Jul 23 15:10:40 2023, max compression
```

## Comparing `rpy2-arrow-0.0.7.tar` & `rpy2-arrow-0.0.8.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxrwxr-x   0 laurent   (1000) laurent   (1000)        0 2022-11-08 03:33:43.152357 rpy2-arrow-0.0.7/
--rw-rw-r--   0 laurent   (1000) laurent   (1000)     1061 2021-07-05 22:24:45.000000 rpy2-arrow-0.0.7/LICENSE
--rw-rw-r--   0 laurent   (1000) laurent   (1000)     1496 2022-11-08 03:33:43.152357 rpy2-arrow-0.0.7/PKG-INFO
--rw-rw-r--   0 laurent   (1000) laurent   (1000)      467 2021-07-05 22:28:26.000000 rpy2-arrow-0.0.7/README.md
--rw-rw-r--   0 laurent   (1000) laurent   (1000)     1397 2022-11-08 03:29:58.000000 rpy2-arrow-0.0.7/pyproject.toml
-drwxrwxr-x   0 laurent   (1000) laurent   (1000)        0 2022-11-08 03:33:43.152357 rpy2-arrow-0.0.7/rpy2_arrow/
--rw-rw-r--   0 laurent   (1000) laurent   (1000)       22 2022-11-08 03:29:58.000000 rpy2-arrow-0.0.7/rpy2_arrow/__init__.py
--rw-rw-r--   0 laurent   (1000) laurent   (1000)    11232 2022-11-08 03:29:58.000000 rpy2-arrow-0.0.7/rpy2_arrow/arrow.py
--rw-rw-r--   0 laurent   (1000) laurent   (1000)      175 2022-11-08 03:29:58.000000 rpy2-arrow-0.0.7/rpy2_arrow/pyarrow_rarrow.py
--rw-rw-r--   0 laurent   (1000) laurent   (1000)     1373 2022-11-08 03:29:58.000000 rpy2-arrow-0.0.7/rpy2_arrow/r6b.py
--rw-rw-r--   0 laurent   (1000) laurent   (1000)     4065 2022-11-08 03:29:58.000000 rpy2-arrow-0.0.7/rpy2_arrow/tests.py
--rw-rw-r--   0 laurent   (1000) laurent   (1000)     1115 2022-11-08 03:29:58.000000 rpy2-arrow-0.0.7/rpy2_arrow/tests_r6b.py
-drwxrwxr-x   0 laurent   (1000) laurent   (1000)        0 2022-11-08 03:33:43.152357 rpy2-arrow-0.0.7/rpy2_arrow.egg-info/
--rw-rw-r--   0 laurent   (1000) laurent   (1000)     1496 2022-11-08 03:33:43.000000 rpy2-arrow-0.0.7/rpy2_arrow.egg-info/PKG-INFO
--rw-rw-r--   0 laurent   (1000) laurent   (1000)      344 2022-11-08 03:33:43.000000 rpy2-arrow-0.0.7/rpy2_arrow.egg-info/SOURCES.txt
--rw-rw-r--   0 laurent   (1000) laurent   (1000)        1 2022-11-08 03:33:43.000000 rpy2-arrow-0.0.7/rpy2_arrow.egg-info/dependency_links.txt
--rw-rw-r--   0 laurent   (1000) laurent   (1000)       83 2022-11-08 03:33:43.000000 rpy2-arrow-0.0.7/rpy2_arrow.egg-info/requires.txt
--rw-rw-r--   0 laurent   (1000) laurent   (1000)       11 2022-11-08 03:33:43.000000 rpy2-arrow-0.0.7/rpy2_arrow.egg-info/top_level.txt
--rw-rw-r--   0 laurent   (1000) laurent   (1000)       38 2022-11-08 03:33:43.152357 rpy2-arrow-0.0.7/setup.cfg
--rw-rw-r--   0 laurent   (1000) laurent   (1000)       69 2022-11-08 03:29:58.000000 rpy2-arrow-0.0.7/setup.py
+drwxrwxr-x   0 laurent   (1000) laurent   (1000)        0 2023-07-23 15:10:40.429495 rpy2-arrow-0.0.8/
+-rw-rw-r--   0 laurent   (1000) laurent   (1000)     1061 2021-07-05 22:24:45.000000 rpy2-arrow-0.0.8/LICENSE
+-rw-rw-r--   0 laurent   (1000) laurent   (1000)     1747 2023-07-23 15:10:40.429495 rpy2-arrow-0.0.8/PKG-INFO
+-rw-rw-r--   0 laurent   (1000) laurent   (1000)      718 2023-07-23 15:08:40.000000 rpy2-arrow-0.0.8/README.md
+-rw-rw-r--   0 laurent   (1000) laurent   (1000)     1397 2022-11-08 03:29:58.000000 rpy2-arrow-0.0.8/pyproject.toml
+drwxrwxr-x   0 laurent   (1000) laurent   (1000)        0 2023-07-23 15:10:40.429495 rpy2-arrow-0.0.8/rpy2_arrow/
+-rw-rw-r--   0 laurent   (1000) laurent   (1000)       22 2022-11-08 03:48:34.000000 rpy2-arrow-0.0.8/rpy2_arrow/__init__.py
+-rw-rw-r--   0 laurent   (1000) laurent   (1000)    11469 2023-07-23 15:08:40.000000 rpy2-arrow-0.0.8/rpy2_arrow/arrow.py
+-rw-rw-r--   0 laurent   (1000) laurent   (1000)      175 2022-11-08 03:29:58.000000 rpy2-arrow-0.0.8/rpy2_arrow/pyarrow_rarrow.py
+-rw-rw-r--   0 laurent   (1000) laurent   (1000)     1373 2023-07-23 15:08:40.000000 rpy2-arrow-0.0.8/rpy2_arrow/r6b.py
+-rw-rw-r--   0 laurent   (1000) laurent   (1000)     4065 2022-11-08 03:29:58.000000 rpy2-arrow-0.0.8/rpy2_arrow/tests.py
+-rw-rw-r--   0 laurent   (1000) laurent   (1000)     1135 2023-07-23 15:08:40.000000 rpy2-arrow-0.0.8/rpy2_arrow/tests_r6b.py
+drwxrwxr-x   0 laurent   (1000) laurent   (1000)        0 2023-07-23 15:10:40.429495 rpy2-arrow-0.0.8/rpy2_arrow.egg-info/
+-rw-rw-r--   0 laurent   (1000) laurent   (1000)     1747 2023-07-23 15:10:40.000000 rpy2-arrow-0.0.8/rpy2_arrow.egg-info/PKG-INFO
+-rw-rw-r--   0 laurent   (1000) laurent   (1000)      344 2023-07-23 15:10:40.000000 rpy2-arrow-0.0.8/rpy2_arrow.egg-info/SOURCES.txt
+-rw-rw-r--   0 laurent   (1000) laurent   (1000)        1 2023-07-23 15:10:40.000000 rpy2-arrow-0.0.8/rpy2_arrow.egg-info/dependency_links.txt
+-rw-rw-r--   0 laurent   (1000) laurent   (1000)       83 2023-07-23 15:10:40.000000 rpy2-arrow-0.0.8/rpy2_arrow.egg-info/requires.txt
+-rw-rw-r--   0 laurent   (1000) laurent   (1000)       11 2023-07-23 15:10:40.000000 rpy2-arrow-0.0.8/rpy2_arrow.egg-info/top_level.txt
+-rw-rw-r--   0 laurent   (1000) laurent   (1000)       38 2023-07-23 15:10:40.429495 rpy2-arrow-0.0.8/setup.cfg
+-rw-rw-r--   0 laurent   (1000) laurent   (1000)       69 2022-11-08 03:29:58.000000 rpy2-arrow-0.0.8/setup.py
```

### Comparing `rpy2-arrow-0.0.7/LICENSE` & `rpy2-arrow-0.0.8/LICENSE`

 * *Files identical despite different names*

### Comparing `rpy2-arrow-0.0.7/PKG-INFO` & `rpy2-arrow-0.0.8/PKG-INFO`

 * *Files 9% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: rpy2-arrow
-Version: 0.0.7
+Version: 0.0.8
 Summary: Bridge Arrow between Python and R when using rpy2
 Author-email: Laurent Gautier <lgautier@gmail.com>
 License: MIT
 Project-URL: Homepage, https://rpy2.github.io/rpy2-arrow/
 Project-URL: Documentation, https://rpy2.github.io/rpy2-arrow/version/main/html/index.html
 Project-URL: Source, https://github.com/rpy2/rpy2-arrow/
 Project-URL: Tracker, https://github.com/rpy2/rpy2-arrow/issue
@@ -25,14 +25,19 @@
 License-File: LICENSE
 
 Share Apache Arrow objects between Python and R using rpy2.
 
 [![pypi](https://img.shields.io/pypi/v/rpy2-arrow.svg?style=flat-square)](https://pypi.python.org/pypi/rpy2-arrow)
 ![Python package](https://github.com/rpy2/rpy2-arrow/workflows/Python%20package/badge.svg)
 
+This package supports sharing Apache Arrow data structures across Python and R by using
+[rpy2](https://rpy2.github.io),
+R's [arrow](https://arrow.apache.org/docs/r/index.html),
+and Python's [pyarrow](https://arrow.apache.org/docs/python/index.html).
+
 This is still work in progress, but there is:
 
 - [HTML doc](https://rpy2.github.io/rpy2-arrow/version/main/html/)
 - [demo notebooks](doc/notebooks/).
 
 To install:
```

### Comparing `rpy2-arrow-0.0.7/pyproject.toml` & `rpy2-arrow-0.0.8/pyproject.toml`

 * *Files identical despite different names*

### Comparing `rpy2-arrow-0.0.7/rpy2_arrow/arrow.py` & `rpy2-arrow-0.0.8/rpy2_arrow/arrow.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,30 +1,36 @@
 import pyarrow  # type: ignore
 from pyarrow.cffi import ffi
 import rpy2.rinterface as rinterface
 import rpy2.robjects as robjects
 import rpy2.robjects.conversion as conversion
 import rpy2.robjects.packages as packages
 import typing
+import warnings
 
 
 rarrow = packages.importr('arrow')
 
+if rinterface.BoolSexpVector(
+        rinterface.evalr("""
+        utils::packageVersion("arrow") < base::package_version("12.0")
+        """)
+)[0]:
+    warnings.warn('Segfaults may occur with the R package arrow < 12.0')
 
 # make sure a version is installed with the C API
 _rarrow_has_c_api = rinterface.BoolSexpVector(
     rinterface.evalr("""
     utils::packageVersion("arrow") >= base::package_version("5.0.0")
     """)
 )[0]
 
 if not _rarrow_has_c_api:
     raise ValueError("rpy2_arrow requires R 'arrow' package version >= 5.0.0")
 
-
 # In arrow >= 7.0.0, pointers can be passed as externalptr,
 # bit64::integer64(), or string, all of which prevent possible
 # problems with the previous versions which required a double().
 _use_r_ptr_string = rinterface.BoolSexpVector(
     rinterface.evalr("""
     utils::packageVersion("arrow") >= base::package_version("6.0.1.9000")
     """)
```

### Comparing `rpy2-arrow-0.0.7/rpy2_arrow/r6b.py` & `rpy2-arrow-0.0.8/rpy2_arrow/r6b.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-import rpy2_R6.r6b as r6b
+import rpy2_r6.r6b as r6b
 import rpy2_arrow.arrow as pyra
 import rpy2.rinterface as rinterface
 import rpy2.robjects
 import rpy2.robjects.conversion
 
 # Python proxies for the R6 class factories
 array_factory = r6b.R6DynamicClassGenerator(pyra.rarrow.Array)
```

### Comparing `rpy2-arrow-0.0.7/rpy2_arrow/tests.py` & `rpy2-arrow-0.0.8/rpy2_arrow/tests.py`

 * *Files identical despite different names*

### Comparing `rpy2-arrow-0.0.7/rpy2_arrow/tests_r6b.py` & `rpy2-arrow-0.0.8/rpy2_arrow/tests_r6b.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 import rpy2.rinterface as rinterface
 import rpy2.robjects.conversion as conversion
 import rpy2.robjects as ro
 import rpy2_arrow.arrow as pyra
 import rpy2_arrow.r6b as r6b_ar
-import rpy2_R6.r6b as r6b
+import rpy2_r6.r6b as r6b
 import pyarrow
 import pytest
 
 
 @pytest.mark.xfail
 @pytest.mark.parametrize(
     'pyarrow_constructor,pyr_py2r',
@@ -20,16 +20,16 @@
     a = [1, 2, 3]
     py_ar = pyarrow_constructor(a)
     r6_ar = pyr_py2r(py_ar)
     assert isinstance(r6_ar, rinterface.SexpEnvironment)
     # TODO: bug in rpy2's layering of conversion rules?
     # with conversion.local_converter(
     #         ro.default_converter + r6b_ar.converter
-    # ) as cv:
+    # ).context() as cv:
     env_map = (ro.conversion
                .converter.rpy2py_nc_name[rinterface.SexpEnvironment])
     with conversion.NameClassMapContext(
             env_map,
             r6b_ar.converter.rpy2py_nc_name[rinterface.SexpEnvironment]._map
-    ):
+    ).context():
         r6_ar = pyr_py2r(py_ar)
         assert isinstance(r6_ar, r6b.R6)
```

### Comparing `rpy2-arrow-0.0.7/rpy2_arrow.egg-info/PKG-INFO` & `rpy2-arrow-0.0.8/rpy2_arrow.egg-info/PKG-INFO`

 * *Files 9% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: rpy2-arrow
-Version: 0.0.7
+Version: 0.0.8
 Summary: Bridge Arrow between Python and R when using rpy2
 Author-email: Laurent Gautier <lgautier@gmail.com>
 License: MIT
 Project-URL: Homepage, https://rpy2.github.io/rpy2-arrow/
 Project-URL: Documentation, https://rpy2.github.io/rpy2-arrow/version/main/html/index.html
 Project-URL: Source, https://github.com/rpy2/rpy2-arrow/
 Project-URL: Tracker, https://github.com/rpy2/rpy2-arrow/issue
@@ -25,14 +25,19 @@
 License-File: LICENSE
 
 Share Apache Arrow objects between Python and R using rpy2.
 
 [![pypi](https://img.shields.io/pypi/v/rpy2-arrow.svg?style=flat-square)](https://pypi.python.org/pypi/rpy2-arrow)
 ![Python package](https://github.com/rpy2/rpy2-arrow/workflows/Python%20package/badge.svg)
 
+This package supports sharing Apache Arrow data structures across Python and R by using
+[rpy2](https://rpy2.github.io),
+R's [arrow](https://arrow.apache.org/docs/r/index.html),
+and Python's [pyarrow](https://arrow.apache.org/docs/python/index.html).
+
 This is still work in progress, but there is:
 
 - [HTML doc](https://rpy2.github.io/rpy2-arrow/version/main/html/)
 - [demo notebooks](doc/notebooks/).
 
 To install:
```

