# Comparing `tmp/HPO-0.2.tar.gz` & `tmp/HPO-0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "HPO-0.2.tar", last modified: Sun Jul 23 17:11:53 2023, max compression
+gzip compressed data, was "HPO-0.3.tar", last modified: Sun Jul 23 17:24:48 2023, max compression
```

## Comparing `HPO-0.2.tar` & `HPO-0.3.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxrwxr-x   0 cmackinnon  (1000) cmackinnon  (1000)        0 2023-07-23 17:11:53.061519 HPO-0.2/
--rw-rw-r--   0 cmackinnon  (1000) cmackinnon  (1000)      596 2023-07-23 17:11:53.061519 HPO-0.2/PKG-INFO
--rw-rw-r--   0 cmackinnon  (1000) cmackinnon  (1000)      496 2023-04-04 13:53:10.000000 HPO-0.2/pyproject.toml
--rw-rw-r--   0 cmackinnon  (1000) cmackinnon  (1000)      789 2023-07-23 17:11:53.061519 HPO-0.2/setup.cfg
--rw-rw-r--   0 cmackinnon  (1000) cmackinnon  (1000)       89 2023-07-23 16:54:44.000000 HPO-0.2/setup.py
-drwxrwxr-x   0 cmackinnon  (1000) cmackinnon  (1000)        0 2023-07-23 17:11:53.057519 HPO-0.2/src/
-drwxrwxr-x   0 cmackinnon  (1000) cmackinnon  (1000)        0 2023-07-23 17:11:53.057519 HPO-0.2/src/HPO/
--rw-rw-r--   0 cmackinnon  (1000) cmackinnon  (1000)        0 2023-04-04 13:53:10.000000 HPO-0.2/src/HPO/__init__.py
--rw-rw-r--   0 cmackinnon  (1000) cmackinnon  (1000)     1716 2023-04-04 13:53:10.000000 HPO-0.2/src/HPO/general_utils.py
-drwxrwxr-x   0 cmackinnon  (1000) cmackinnon  (1000)        0 2023-07-23 17:11:53.061519 HPO-0.2/src/HPO.egg-info/
--rw-rw-r--   0 cmackinnon  (1000) cmackinnon  (1000)      596 2023-07-23 17:11:53.000000 HPO-0.2/src/HPO.egg-info/PKG-INFO
--rw-rw-r--   0 cmackinnon  (1000) cmackinnon  (1000)      262 2023-07-23 17:11:53.000000 HPO-0.2/src/HPO.egg-info/SOURCES.txt
--rw-rw-r--   0 cmackinnon  (1000) cmackinnon  (1000)        1 2023-07-23 17:11:53.000000 HPO-0.2/src/HPO.egg-info/dependency_links.txt
--rw-rw-r--   0 cmackinnon  (1000) cmackinnon  (1000)        1 2023-04-04 13:53:10.000000 HPO-0.2/src/HPO.egg-info/not-zip-safe
--rw-rw-r--   0 cmackinnon  (1000) cmackinnon  (1000)       73 2023-07-23 17:11:53.000000 HPO-0.2/src/HPO.egg-info/requires.txt
--rw-rw-r--   0 cmackinnon  (1000) cmackinnon  (1000)        4 2023-07-23 17:11:53.000000 HPO-0.2/src/HPO.egg-info/top_level.txt
+drwxrwxr-x   0 cmackinnon  (1000) cmackinnon  (1000)        0 2023-07-23 17:24:48.873289 HPO-0.3/
+-rw-rw-r--   0 cmackinnon  (1000) cmackinnon  (1000)      596 2023-07-23 17:24:48.873289 HPO-0.3/PKG-INFO
+-rw-rw-r--   0 cmackinnon  (1000) cmackinnon  (1000)      496 2023-04-04 13:53:10.000000 HPO-0.3/pyproject.toml
+-rw-rw-r--   0 cmackinnon  (1000) cmackinnon  (1000)      789 2023-07-23 17:24:48.873289 HPO-0.3/setup.cfg
+-rw-rw-r--   0 cmackinnon  (1000) cmackinnon  (1000)       89 2023-07-23 16:54:44.000000 HPO-0.3/setup.py
+drwxrwxr-x   0 cmackinnon  (1000) cmackinnon  (1000)        0 2023-07-23 17:24:48.873289 HPO-0.3/src/
+drwxrwxr-x   0 cmackinnon  (1000) cmackinnon  (1000)        0 2023-07-23 17:24:48.873289 HPO-0.3/src/HPO/
+-rw-rw-r--   0 cmackinnon  (1000) cmackinnon  (1000)        0 2023-04-04 13:53:10.000000 HPO-0.3/src/HPO/__init__.py
+-rw-rw-r--   0 cmackinnon  (1000) cmackinnon  (1000)     1716 2023-04-04 13:53:10.000000 HPO-0.3/src/HPO/general_utils.py
+drwxrwxr-x   0 cmackinnon  (1000) cmackinnon  (1000)        0 2023-07-23 17:24:48.873289 HPO-0.3/src/HPO.egg-info/
+-rw-rw-r--   0 cmackinnon  (1000) cmackinnon  (1000)      596 2023-07-23 17:24:48.000000 HPO-0.3/src/HPO.egg-info/PKG-INFO
+-rw-rw-r--   0 cmackinnon  (1000) cmackinnon  (1000)      262 2023-07-23 17:24:48.000000 HPO-0.3/src/HPO.egg-info/SOURCES.txt
+-rw-rw-r--   0 cmackinnon  (1000) cmackinnon  (1000)        1 2023-07-23 17:24:48.000000 HPO-0.3/src/HPO.egg-info/dependency_links.txt
+-rw-rw-r--   0 cmackinnon  (1000) cmackinnon  (1000)        1 2023-04-04 13:53:10.000000 HPO-0.3/src/HPO.egg-info/not-zip-safe
+-rw-rw-r--   0 cmackinnon  (1000) cmackinnon  (1000)       73 2023-07-23 17:24:48.000000 HPO-0.3/src/HPO.egg-info/requires.txt
+-rw-rw-r--   0 cmackinnon  (1000) cmackinnon  (1000)        1 2023-07-23 17:24:48.000000 HPO-0.3/src/HPO.egg-info/top_level.txt
```

### Comparing `HPO-0.2/PKG-INFO` & `HPO-0.3/PKG-INFO`

 * *Files 17% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: HPO
-Version: 0.2
+Version: 0.3
 Summary: Package for testing NAS and HPO workers, search spaces and algorithms together.
 Author: Christopher MacKinnon
 License: GPL3
 Platform: linux
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3 :: Only
 Classifier: Programming Language :: Python :: 3.6
```

### Comparing `HPO-0.2/setup.cfg` & `HPO-0.3/setup.cfg`

 * *Files 1% similar despite different names*

```diff
@@ -1,26 +1,25 @@
 [metadata]
 name = HPO
-version = 0.2
+version = 0.3
 description = Package for testing NAS and HPO workers, search spaces and algorithms together.
 author = Christopher MacKinnon
 license = GPL3
 platforms = linux
 classifiers = 
 	Programming Language :: Python :: 3
 	Programming Language :: Python :: 3 :: Only
 	Programming Language :: Python :: 3.6
 	Programming Language :: Python :: 3.7
 	Programming Language :: Python :: 3.8
 	Programming Language :: Python :: 3.9
 	Programming Language :: Python :: 3.10
 
 [options]
-packages = 
-	HPO
+packages = find:
 python_requires = >=3.6
 package_dir = 
 	= src
 zip_safe = no
 
 [options.extras_require]
 testing =
```

### Comparing `HPO-0.2/src/HPO/general_utils.py` & `HPO-0.3/src/HPO/general_utils.py`

 * *Files identical despite different names*

### Comparing `HPO-0.2/src/HPO.egg-info/PKG-INFO` & `HPO-0.3/src/HPO.egg-info/PKG-INFO`

 * *Files 17% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: HPO
-Version: 0.2
+Version: 0.3
 Summary: Package for testing NAS and HPO workers, search spaces and algorithms together.
 Author: Christopher MacKinnon
 License: GPL3
 Platform: linux
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3 :: Only
 Classifier: Programming Language :: Python :: 3.6
```

