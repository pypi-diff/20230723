# Comparing `tmp/kidash-0.5.9.tar.gz` & `tmp/kidash-0.5.9rc1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "kidash-0.5.9.tar", max compression
+gzip compressed data, was "kidash-0.5.9rc1.tar", max compression
```

## Comparing `kidash-0.5.9.tar` & `kidash-0.5.9rc1.tar`

### file list

```diff
@@ -1,13 +1,13 @@
--rw-r--r--   0        0        0      300 2023-07-23 19:47:15.342414 kidash-0.5.9/AUTHORS
--rw-r--r--   0        0        0    35147 2023-07-23 19:47:15.342414 kidash-0.5.9/LICENSE
--rw-r--r--   0        0        0     1600 2023-07-23 19:47:15.342414 kidash-0.5.9/NEWS
--rw-r--r--   0        0        0     2525 2023-07-23 19:47:15.342414 kidash-0.5.9/README.md
--rw-r--r--   0        0        0      894 2023-07-23 19:47:15.342414 kidash-0.5.9/kidash/__init__.py
--rw-r--r--   0        0        0       86 2023-07-23 19:47:15.342414 kidash-0.5.9/kidash/_version.py
--rwxr-xr-x   0        0        0     4355 2023-07-23 19:47:15.342414 kidash-0.5.9/kidash/bin/kidash.py
--rwxr-xr-x   0        0        0    59367 2023-07-23 19:47:15.342414 kidash-0.5.9/kidash/kidash.py
--rw-r--r--   0        0        0     1302 2023-07-23 19:47:15.342414 kidash-0.5.9/pyproject.toml
--rw-r--r--   0        0        0    54328 2023-07-23 19:47:15.342414 kidash-0.5.9/tests/data/overview-with-index-patterns.json
--rwxr-xr-x   0        0        0     1166 2023-07-23 19:47:15.342414 kidash-0.5.9/tests/run_tests.py
--rw-r--r--   0        0        0     2131 2023-07-23 19:47:15.342414 kidash-0.5.9/tests/test_export.py
--rw-r--r--   0        0        0     3658 1970-01-01 00:00:00.000000 kidash-0.5.9/PKG-INFO
+-rw-r--r--   0        0        0      300 2023-07-23 16:22:39.694513 kidash-0.5.9rc1/AUTHORS
+-rw-r--r--   0        0        0    35147 2023-07-23 16:22:39.694513 kidash-0.5.9rc1/LICENSE
+-rw-r--r--   0        0        0     1522 2023-07-23 16:22:39.694513 kidash-0.5.9rc1/NEWS
+-rw-r--r--   0        0        0     2525 2023-07-23 16:22:39.694513 kidash-0.5.9rc1/README.md
+-rw-r--r--   0        0        0      894 2023-07-23 16:22:39.694513 kidash-0.5.9rc1/kidash/__init__.py
+-rw-r--r--   0        0        0       91 2023-07-23 16:22:39.694513 kidash-0.5.9rc1/kidash/_version.py
+-rwxr-xr-x   0        0        0     4355 2023-07-23 16:22:39.694513 kidash-0.5.9rc1/kidash/bin/kidash.py
+-rwxr-xr-x   0        0        0    59367 2023-07-23 16:22:39.694513 kidash-0.5.9rc1/kidash/kidash.py
+-rw-r--r--   0        0        0     1307 2023-07-23 16:22:39.694513 kidash-0.5.9rc1/pyproject.toml
+-rw-r--r--   0        0        0    54328 2023-07-23 16:22:39.698513 kidash-0.5.9rc1/tests/data/overview-with-index-patterns.json
+-rwxr-xr-x   0        0        0     1166 2023-07-23 16:22:39.698513 kidash-0.5.9rc1/tests/run_tests.py
+-rw-r--r--   0        0        0     2131 2023-07-23 16:22:39.698513 kidash-0.5.9rc1/tests/test_export.py
+-rw-r--r--   0        0        0     3661 1970-01-01 00:00:00.000000 kidash-0.5.9rc1/PKG-INFO
```

### Comparing `kidash-0.5.9/LICENSE` & `kidash-0.5.9rc1/LICENSE`

 * *Files identical despite different names*

### Comparing `kidash-0.5.9/NEWS` & `kidash-0.5.9rc1/NEWS`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,9 @@
 # Releases
 
-  ## kidash 0.5.9 - (2023-07-23)
-  
-  * Update Poetry's package dependencies
-
   ## kidash 0.5.8 - (2023-07-11)
   
   * Update Poetry's package dependencies
 
   ## kidash 0.5.7 - (2023-06-28)
   
   * Update Poetry's package dependencies
```

### Comparing `kidash-0.5.9/README.md` & `kidash-0.5.9rc1/README.md`

 * *Files identical despite different names*

### Comparing `kidash-0.5.9/kidash/__init__.py` & `kidash-0.5.9rc1/kidash/__init__.py`

 * *Files identical despite different names*

### Comparing `kidash-0.5.9/kidash/bin/kidash.py` & `kidash-0.5.9rc1/kidash/bin/kidash.py`

 * *Files identical despite different names*

### Comparing `kidash-0.5.9/kidash/kidash.py` & `kidash-0.5.9rc1/kidash/kidash.py`

 * *Files identical despite different names*

### Comparing `kidash-0.5.9/pyproject.toml` & `kidash-0.5.9rc1/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "kidash"
-version = "0.5.9"
+version = "0.5.9-rc.1"
 description = "GrimoireLab script to manage Kibana dashboards from the command line"
 authors = [
     "GrimoireLab Developers"
 ]
 license = "GPL-3.0+"
 
 readme = "README.md"
```

### Comparing `kidash-0.5.9/tests/data/overview-with-index-patterns.json` & `kidash-0.5.9rc1/tests/data/overview-with-index-patterns.json`

 * *Files identical despite different names*

### Comparing `kidash-0.5.9/tests/run_tests.py` & `kidash-0.5.9rc1/tests/run_tests.py`

 * *Files identical despite different names*

### Comparing `kidash-0.5.9/tests/test_export.py` & `kidash-0.5.9rc1/tests/test_export.py`

 * *Files identical despite different names*

### Comparing `kidash-0.5.9/PKG-INFO` & `kidash-0.5.9rc1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: kidash
-Version: 0.5.9
+Version: 0.5.9rc1
 Summary: GrimoireLab script to manage Kibana dashboards from the command line
 Home-page: https://chaoss.github.io/grimoirelab/
 License: GPL-3.0+
 Keywords: development,grimoirelab
 Author: GrimoireLab Developers
 Requires-Python: >=3.7,<4.0
 Classifier: Development Status :: 5 - Production/Stable
```

