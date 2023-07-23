# Comparing `tmp/posaydones-material-theming-1.0.4.tar.gz` & `tmp/posaydones-material-theming-1.0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "posaydones-material-theming-1.0.4.tar", last modified: Sun Jul 23 16:00:13 2023, max compression
+gzip compressed data, was "posaydones-material-theming-1.0.5.tar", last modified: Sun Jul 23 16:03:31 2023, max compression
```

## Comparing `posaydones-material-theming-1.0.4.tar` & `posaydones-material-theming-1.0.5.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxr-xr-x   0 posaydone  (1000) posaydone  (1000)        0 2023-07-23 16:00:13.889960 posaydones-material-theming-1.0.4/
--rwxr-xr-x   0 posaydone  (1000) posaydone  (1000)        0 2023-07-18 10:58:03.000000 posaydones-material-theming-1.0.4/MANIFEST.in
--rw-r--r--   0 posaydone  (1000) posaydone  (1000)      704 2023-07-23 16:00:13.889960 posaydones-material-theming-1.0.4/PKG-INFO
--rw-r--r--   0 posaydone  (1000) posaydone  (1000)      112 2023-07-22 15:56:50.000000 posaydones-material-theming-1.0.4/README.rst
-drwxr-xr-x   0 posaydone  (1000) posaydone  (1000)        0 2023-07-23 16:00:13.888960 posaydones-material-theming-1.0.4/data/
--rw-r--r--   0 posaydone  (1000) posaydone  (1000)     3634 2023-07-21 12:49:21.000000 posaydones-material-theming-1.0.4/data/pmt.cmb
--rw-r--r--   0 posaydone  (1000) posaydone  (1000)     2920 2023-07-21 12:46:33.000000 posaydones-material-theming-1.0.4/data/pmt.ui
-drwxr-xr-x   0 posaydone  (1000) posaydone  (1000)        0 2023-07-23 16:00:13.889960 posaydones-material-theming-1.0.4/posaydones_material_theming.egg-info/
--rw-r--r--   0 posaydone  (1000) posaydone  (1000)      704 2023-07-23 16:00:13.000000 posaydones-material-theming-1.0.4/posaydones_material_theming.egg-info/PKG-INFO
--rw-r--r--   0 posaydone  (1000) posaydone  (1000)      406 2023-07-23 16:00:13.000000 posaydones-material-theming-1.0.4/posaydones_material_theming.egg-info/SOURCES.txt
--rw-r--r--   0 posaydone  (1000) posaydone  (1000)        1 2023-07-23 16:00:13.000000 posaydones-material-theming-1.0.4/posaydones_material_theming.egg-info/dependency_links.txt
--rw-r--r--   0 posaydone  (1000) posaydone  (1000)       33 2023-07-23 16:00:13.000000 posaydones-material-theming-1.0.4/posaydones_material_theming.egg-info/entry_points.txt
--rw-r--r--   0 posaydone  (1000) posaydone  (1000)       45 2023-07-23 16:00:13.000000 posaydones-material-theming-1.0.4/posaydones_material_theming.egg-info/requires.txt
--rw-r--r--   0 posaydone  (1000) posaydone  (1000)       10 2023-07-23 16:00:13.000000 posaydones-material-theming-1.0.4/posaydones_material_theming.egg-info/top_level.txt
--rw-r--r--   0 posaydone  (1000) posaydone  (1000)      144 2023-07-18 10:58:03.000000 posaydones-material-theming-1.0.4/requirements.txt
--rwxr-xr-x   0 posaydone  (1000) posaydone  (1000)       65 2023-07-23 10:22:34.000000 posaydones-material-theming-1.0.4/runner.py
--rw-r--r--   0 posaydone  (1000) posaydone  (1000)       38 2023-07-23 16:00:13.889960 posaydones-material-theming-1.0.4/setup.cfg
--rwxr-xr-x   0 posaydone  (1000) posaydone  (1000)     2870 2023-07-23 15:47:23.000000 posaydones-material-theming-1.0.4/setup.py
-drwxr-xr-x   0 posaydone  (1000) posaydone  (1000)        0 2023-07-23 16:00:13.889960 posaydones-material-theming-1.0.4/tests/
--rw-r--r--   0 posaydone  (1000) posaydone  (1000)      118 2023-07-18 13:59:26.000000 posaydones-material-theming-1.0.4/tests/tests.py
+drwxr-xr-x   0 posaydone  (1000) posaydone  (1000)        0 2023-07-23 16:03:31.101183 posaydones-material-theming-1.0.5/
+-rwxr-xr-x   0 posaydone  (1000) posaydone  (1000)        0 2023-07-18 10:58:03.000000 posaydones-material-theming-1.0.5/MANIFEST.in
+-rw-r--r--   0 posaydone  (1000) posaydone  (1000)      704 2023-07-23 16:03:31.101183 posaydones-material-theming-1.0.5/PKG-INFO
+-rw-r--r--   0 posaydone  (1000) posaydone  (1000)      112 2023-07-22 15:56:50.000000 posaydones-material-theming-1.0.5/README.rst
+drwxr-xr-x   0 posaydone  (1000) posaydone  (1000)        0 2023-07-23 16:03:31.101183 posaydones-material-theming-1.0.5/data/
+-rw-r--r--   0 posaydone  (1000) posaydone  (1000)     3634 2023-07-21 12:49:21.000000 posaydones-material-theming-1.0.5/data/pmt.cmb
+-rw-r--r--   0 posaydone  (1000) posaydone  (1000)     2920 2023-07-21 12:46:33.000000 posaydones-material-theming-1.0.5/data/pmt.ui
+drwxr-xr-x   0 posaydone  (1000) posaydone  (1000)        0 2023-07-23 16:03:31.101183 posaydones-material-theming-1.0.5/posaydones_material_theming.egg-info/
+-rw-r--r--   0 posaydone  (1000) posaydone  (1000)      704 2023-07-23 16:03:31.000000 posaydones-material-theming-1.0.5/posaydones_material_theming.egg-info/PKG-INFO
+-rw-r--r--   0 posaydone  (1000) posaydone  (1000)      406 2023-07-23 16:03:31.000000 posaydones-material-theming-1.0.5/posaydones_material_theming.egg-info/SOURCES.txt
+-rw-r--r--   0 posaydone  (1000) posaydone  (1000)        1 2023-07-23 16:03:31.000000 posaydones-material-theming-1.0.5/posaydones_material_theming.egg-info/dependency_links.txt
+-rw-r--r--   0 posaydone  (1000) posaydone  (1000)       33 2023-07-23 16:03:31.000000 posaydones-material-theming-1.0.5/posaydones_material_theming.egg-info/entry_points.txt
+-rw-r--r--   0 posaydone  (1000) posaydone  (1000)       45 2023-07-23 16:03:31.000000 posaydones-material-theming-1.0.5/posaydones_material_theming.egg-info/requires.txt
+-rw-r--r--   0 posaydone  (1000) posaydone  (1000)       10 2023-07-23 16:03:31.000000 posaydones-material-theming-1.0.5/posaydones_material_theming.egg-info/top_level.txt
+-rw-r--r--   0 posaydone  (1000) posaydone  (1000)      144 2023-07-18 10:58:03.000000 posaydones-material-theming-1.0.5/requirements.txt
+-rwxr-xr-x   0 posaydone  (1000) posaydone  (1000)       65 2023-07-23 10:22:34.000000 posaydones-material-theming-1.0.5/runner.py
+-rw-r--r--   0 posaydone  (1000) posaydone  (1000)       38 2023-07-23 16:03:31.102183 posaydones-material-theming-1.0.5/setup.cfg
+-rwxr-xr-x   0 posaydone  (1000) posaydone  (1000)     2870 2023-07-23 15:47:23.000000 posaydones-material-theming-1.0.5/setup.py
+drwxr-xr-x   0 posaydone  (1000) posaydone  (1000)        0 2023-07-23 16:03:31.101183 posaydones-material-theming-1.0.5/tests/
+-rw-r--r--   0 posaydone  (1000) posaydone  (1000)      118 2023-07-18 13:59:26.000000 posaydones-material-theming-1.0.5/tests/tests.py
```

### Comparing `posaydones-material-theming-1.0.4/PKG-INFO` & `posaydones-material-theming-1.0.5/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: posaydones-material-theming
-Version: 1.0.4
+Version: 1.0.5
 Summary: Small cli+gui app to manage material theming.
 Home-page: https://github.com/posaydone/pmt
 Author: PoSayDone
 Author-email: poseaydone@ya.ru
 License: MIT
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python
```

### Comparing `posaydones-material-theming-1.0.4/data/pmt.cmb` & `posaydones-material-theming-1.0.5/data/pmt.cmb`

 * *Files identical despite different names*

### Comparing `posaydones-material-theming-1.0.4/data/pmt.ui` & `posaydones-material-theming-1.0.5/data/pmt.ui`

 * *Files identical despite different names*

### Comparing `posaydones-material-theming-1.0.4/posaydones_material_theming.egg-info/PKG-INFO` & `posaydones-material-theming-1.0.5/posaydones_material_theming.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: posaydones-material-theming
-Version: 1.0.4
+Version: 1.0.5
 Summary: Small cli+gui app to manage material theming.
 Home-page: https://github.com/posaydone/pmt
 Author: PoSayDone
 Author-email: poseaydone@ya.ru
 License: MIT
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python
```

### Comparing `posaydones-material-theming-1.0.4/setup.py` & `posaydones-material-theming-1.0.5/setup.py`

 * *Files identical despite different names*

