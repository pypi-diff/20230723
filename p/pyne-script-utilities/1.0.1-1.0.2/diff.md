# Comparing `tmp/pyne_script_utilities-1.0.1.tar.gz` & `tmp/pyne_script_utilities-1.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, last modified: Sun Feb  2 00:00:00 2020, max compression
+gzip compressed data, was "pyne_script_utilities-1.0.2.tar", last modified: Sun Jul 23 09:30:38 2023, max compression
```

## Comparing `pyne_script_utilities-1.0.1.tar` & `pyne_script_utilities-1.0.2.tar`

### file list

```diff
@@ -1,10 +1,16 @@
--rw-r--r--   0        0        0     1593 2020-02-02 00:00:00.000000 pyne_script_utilities-1.0.1/docs/README_series.md
--rw-r--r--   0        0        0      623 2020-02-02 00:00:00.000000 pyne_script_utilities-1.0.1/examples/basics.py
--rw-r--r--   0        0        0     3037 2020-02-02 00:00:00.000000 pyne_script_utilities-1.0.1/examples/random_graph.py
--rw-r--r--   0        0        0       38 2020-02-02 00:00:00.000000 pyne_script_utilities-1.0.1/src/pyne_script/__init__.py
--rw-r--r--   0        0        0    20704 2020-02-02 00:00:00.000000 pyne_script_utilities-1.0.1/src/pyne_script/series.py
--rw-r--r--   0        0        0     3126 2020-02-02 00:00:00.000000 pyne_script_utilities-1.0.1/.gitignore
--rw-r--r--   0        0        0    35148 2020-02-02 00:00:00.000000 pyne_script_utilities-1.0.1/LICENSE
--rw-r--r--   0        0        0      613 2020-02-02 00:00:00.000000 pyne_script_utilities-1.0.1/README.md
--rw-r--r--   0        0        0      600 2020-02-02 00:00:00.000000 pyne_script_utilities-1.0.1/pyproject.toml
--rw-r--r--   0        0        0     1149 2020-02-02 00:00:00.000000 pyne_script_utilities-1.0.1/PKG-INFO
+drwxr-xr-x   0 krijn     (1000) krijn     (1000)        0 2023-07-23 09:30:38.159611 pyne_script_utilities-1.0.2/
+-rw-r--r--   0 krijn     (1000) krijn     (1000)    35148 2023-07-06 09:11:48.000000 pyne_script_utilities-1.0.2/LICENSE
+-rw-r--r--   0 krijn     (1000) krijn     (1000)     1149 2023-07-23 09:30:38.159611 pyne_script_utilities-1.0.2/PKG-INFO
+-rw-r--r--   0 krijn     (1000) krijn     (1000)      613 2023-07-19 19:47:36.000000 pyne_script_utilities-1.0.2/README.md
+-rw-r--r--   0 krijn     (1000) krijn     (1000)      727 2023-07-23 09:27:44.000000 pyne_script_utilities-1.0.2/pyproject.toml
+-rw-r--r--   0 krijn     (1000) krijn     (1000)       38 2023-07-23 09:30:38.159611 pyne_script_utilities-1.0.2/setup.cfg
+drwxr-xr-x   0 krijn     (1000) krijn     (1000)        0 2023-07-23 09:30:38.159611 pyne_script_utilities-1.0.2/src/
+drwxr-xr-x   0 krijn     (1000) krijn     (1000)        0 2023-07-23 09:30:38.159611 pyne_script_utilities-1.0.2/src/pyne_script/
+-rw-r--r--   0 krijn     (1000) krijn     (1000)       38 2023-07-22 13:56:07.000000 pyne_script_utilities-1.0.2/src/pyne_script/__init__.py
+-rw-r--r--   0 krijn     (1000) krijn     (1000)    20703 2023-07-23 09:27:11.000000 pyne_script_utilities-1.0.2/src/pyne_script/series.py
+drwxr-xr-x   0 krijn     (1000) krijn     (1000)        0 2023-07-23 09:30:38.159611 pyne_script_utilities-1.0.2/src/pyne_script_utilities.egg-info/
+-rw-r--r--   0 krijn     (1000) krijn     (1000)     1149 2023-07-23 09:30:38.000000 pyne_script_utilities-1.0.2/src/pyne_script_utilities.egg-info/PKG-INFO
+-rw-r--r--   0 krijn     (1000) krijn     (1000)      330 2023-07-23 09:30:38.000000 pyne_script_utilities-1.0.2/src/pyne_script_utilities.egg-info/SOURCES.txt
+-rw-r--r--   0 krijn     (1000) krijn     (1000)        1 2023-07-23 09:30:38.000000 pyne_script_utilities-1.0.2/src/pyne_script_utilities.egg-info/dependency_links.txt
+-rw-r--r--   0 krijn     (1000) krijn     (1000)        6 2023-07-23 09:30:38.000000 pyne_script_utilities-1.0.2/src/pyne_script_utilities.egg-info/requires.txt
+-rw-r--r--   0 krijn     (1000) krijn     (1000)       12 2023-07-23 09:30:38.000000 pyne_script_utilities-1.0.2/src/pyne_script_utilities.egg-info/top_level.txt
```

### Comparing `pyne_script_utilities-1.0.1/src/pyne_script/series.py` & `pyne_script_utilities-1.0.2/src/pyne_script/series.py`

 * *Files 0% similar despite different names*

```diff
@@ -213,15 +213,15 @@
     def __init__(
         self,
         key_value_pairs_int: dict[str | int, list[int]] = {},
         key_value_pairs_float: dict[str | int, list[float]] = {},
         track_history_mode: int = 0,
         window_size: int = 200,
         initial_update: bool = False,
-        dtypes: dict[type, type] = {int: np.int64, float: np.float128},
+        dtypes: dict[type, type] = {int: np.int64, float: np.float32},
     ) -> None:
         """
         Args:
         - key_value_pairs_[type]: Initial values for each series.
           Formated as a dict[string or int, numeric list of corrosponding type]
           with each list having equal length with at least length 1.
           Last value in each list is used as current head value.
```

### Comparing `pyne_script_utilities-1.0.1/LICENSE` & `pyne_script_utilities-1.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `pyne_script_utilities-1.0.1/README.md` & `pyne_script_utilities-1.0.2/README.md`

 * *Files identical despite different names*

### Comparing `pyne_script_utilities-1.0.1/PKG-INFO` & `pyne_script_utilities-1.0.2/PKG-INFO`

 * *Files 10% similar despite different names*

```diff
@@ -1,19 +1,19 @@
 Metadata-Version: 2.1
 Name: pyne_script_utilities
-Version: 1.0.1
+Version: 1.0.2
 Summary: A set of utility sub-modules that allow for code structure similar to pinescript in python
+Author: 80sVectorz
 Project-URL: Homepage, https://github.com/80sVectorz/pyne_script
 Project-URL: Bug Tracker, https://github.com/80sVectorz/pyne_script/issues
-Author: 80sVectorz
-License-File: LICENSE
-Classifier: License :: OSI Approved :: GNU General Public License v3 (GPLv3)
 Classifier: Programming Language :: Python :: 3
+Classifier: License :: OSI Approved :: GNU General Public License v3 (GPLv3)
 Requires-Python: >=3.10
 Description-Content-Type: text/markdown
+License-File: LICENSE
 
 # Pyne Script
 
 Pyne Script aims to offer a set of utility sub-modules that allow for code structure similar to Trading View Pine Script in Python.
 
 ## Installation
```

