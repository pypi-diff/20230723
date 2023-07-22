# Comparing `tmp/chalk-harness-1.0.4.tar.gz` & `tmp/chalk-harness-1.0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "chalk-harness-1.0.4.tar", last modified: Tue Jul 18 20:04:43 2023, max compression
+gzip compressed data, was "chalk-harness-1.0.5.tar", last modified: Sat Jul 22 23:12:39 2023, max compression
```

## Comparing `chalk-harness-1.0.4.tar` & `chalk-harness-1.0.5.tar`

### file list

```diff
@@ -1,21 +1,21 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 20:04:43.040292 chalk-harness-1.0.4/
--rw-r--r--   0 runner    (1001) docker     (123)       35 2023-07-18 20:04:25.000000 chalk-harness-1.0.4/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)      967 2023-07-18 20:04:43.040292 chalk-harness-1.0.4/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      612 2023-07-18 20:04:25.000000 chalk-harness-1.0.4/README.md
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-18 20:04:25.000000 chalk-harness-1.0.4/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       22 2023-07-18 20:04:25.000000 chalk-harness-1.0.4/_version.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 20:04:43.040292 chalk-harness-1.0.4/chalk_harness.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)      967 2023-07-18 20:04:42.000000 chalk-harness-1.0.4/chalk_harness.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      343 2023-07-18 20:04:42.000000 chalk-harness-1.0.4/chalk_harness.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-18 20:04:42.000000 chalk-harness-1.0.4/chalk_harness.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       16 2023-07-18 20:04:42.000000 chalk-harness-1.0.4/chalk_harness.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       13 2023-07-18 20:04:42.000000 chalk-harness-1.0.4/chalk_harness.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 20:04:43.040292 chalk-harness-1.0.4/chalkharness/
--rw-r--r--   0 runner    (1001) docker     (123)     6548 2023-07-18 20:04:25.000000 chalk-harness-1.0.4/chalkharness/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-18 20:04:25.000000 chalk-harness-1.0.4/chalkharness/py.typed
--rw-r--r--   0 runner    (1001) docker     (123)       16 2023-07-18 20:04:25.000000 chalk-harness-1.0.4/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-18 20:04:43.040292 chalk-harness-1.0.4/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1479 2023-07-18 20:04:25.000000 chalk-harness-1.0.4/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 20:04:43.040292 chalk-harness-1.0.4/tests/
--rw-r--r--   0 runner    (1001) docker     (123)     1019 2023-07-18 20:04:25.000000 chalk-harness-1.0.4/tests/SanityTestCase.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-18 20:04:25.000000 chalk-harness-1.0.4/tests/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 23:12:39.060551 chalk-harness-1.0.5/
+-rw-r--r--   0 runner    (1001) docker     (123)       35 2023-07-22 23:12:18.000000 chalk-harness-1.0.5/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)      967 2023-07-22 23:12:39.056551 chalk-harness-1.0.5/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      612 2023-07-22 23:12:18.000000 chalk-harness-1.0.5/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-22 23:12:18.000000 chalk-harness-1.0.5/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       22 2023-07-22 23:12:19.000000 chalk-harness-1.0.5/_version.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 23:12:39.056551 chalk-harness-1.0.5/chalk_harness.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)      967 2023-07-22 23:12:38.000000 chalk-harness-1.0.5/chalk_harness.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      343 2023-07-22 23:12:39.000000 chalk-harness-1.0.5/chalk_harness.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-22 23:12:38.000000 chalk-harness-1.0.5/chalk_harness.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       16 2023-07-22 23:12:38.000000 chalk-harness-1.0.5/chalk_harness.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       13 2023-07-22 23:12:38.000000 chalk-harness-1.0.5/chalk_harness.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 23:12:39.056551 chalk-harness-1.0.5/chalkharness/
+-rw-r--r--   0 runner    (1001) docker     (123)     6548 2023-07-22 23:12:18.000000 chalk-harness-1.0.5/chalkharness/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-22 23:12:18.000000 chalk-harness-1.0.5/chalkharness/py.typed
+-rw-r--r--   0 runner    (1001) docker     (123)       16 2023-07-22 23:12:18.000000 chalk-harness-1.0.5/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-22 23:12:39.060551 chalk-harness-1.0.5/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1479 2023-07-22 23:12:18.000000 chalk-harness-1.0.5/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 23:12:39.056551 chalk-harness-1.0.5/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     1019 2023-07-22 23:12:18.000000 chalk-harness-1.0.5/tests/SanityTestCase.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-22 23:12:18.000000 chalk-harness-1.0.5/tests/__init__.py
```

### Comparing `chalk-harness-1.0.4/PKG-INFO` & `chalk-harness-1.0.5/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: chalk-harness
-Version: 1.0.4
+Version: 1.0.5
 Summary: Python wrapper for Chalk's CLI
 Home-page: https://chalk.ai
 Author: Chalk AI, Inc.
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Requires-Python: >=3.8.0
```

### Comparing `chalk-harness-1.0.4/README.md` & `chalk-harness-1.0.5/README.md`

 * *Files identical despite different names*

### Comparing `chalk-harness-1.0.4/chalk_harness.egg-info/PKG-INFO` & `chalk-harness-1.0.5/chalk_harness.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: chalk-harness
-Version: 1.0.4
+Version: 1.0.5
 Summary: Python wrapper for Chalk's CLI
 Home-page: https://chalk.ai
 Author: Chalk AI, Inc.
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Requires-Python: >=3.8.0
```

### Comparing `chalk-harness-1.0.4/chalkharness/__init__.py` & `chalk-harness-1.0.5/chalkharness/__init__.py`

 * *Files identical despite different names*

### Comparing `chalk-harness-1.0.4/setup.py` & `chalk-harness-1.0.5/setup.py`

 * *Files identical despite different names*

### Comparing `chalk-harness-1.0.4/tests/SanityTestCase.py` & `chalk-harness-1.0.5/tests/SanityTestCase.py`

 * *Files identical despite different names*

