# Comparing `tmp/mlfast-0.0.8.tar.gz` & `tmp/mlfast-0.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "mlfast-0.0.8.tar", last modified: Sat Jun  3 22:16:07 2023, max compression
+gzip compressed data, was "mlfast-0.0.9.tar", last modified: Sun Jun  4 12:57:43 2023, max compression
```

## Comparing `mlfast-0.0.8.tar` & `mlfast-0.0.9.tar`

### file list

```diff
@@ -1,22 +1,22 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-03 22:16:07.818027 mlfast-0.0.8/
--rw-r--r--   0 runner    (1001) docker     (123)     1069 2023-06-03 22:14:29.000000 mlfast-0.0.8/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     1422 2023-06-03 22:16:07.818027 mlfast-0.0.8/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      865 2023-06-03 22:14:29.000000 mlfast-0.0.8/README.md
--rw-r--r--   0 runner    (1001) docker     (123)      218 2023-06-03 22:14:29.000000 mlfast-0.0.8/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)      552 2023-06-03 22:16:07.818027 mlfast-0.0.8/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      762 2023-06-03 22:14:29.000000 mlfast-0.0.8/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-03 22:16:07.814027 mlfast-0.0.8/src/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-03 22:16:07.814027 mlfast-0.0.8/src/mlfast/
--rw-r--r--   0 runner    (1001) docker     (123)     1572 2023-06-03 22:14:29.000000 mlfast-0.0.8/src/mlfast/Chatbot.py
--rw-r--r--   0 runner    (1001) docker     (123)     3058 2023-06-03 22:14:29.000000 mlfast-0.0.8/src/mlfast/Classification.py
--rw-r--r--   0 runner    (1001) docker     (123)     3162 2023-06-03 22:14:29.000000 mlfast-0.0.8/src/mlfast/Regression.py
--rw-r--r--   0 runner    (1001) docker     (123)     2537 2023-06-03 22:14:29.000000 mlfast-0.0.8/src/mlfast/Text_preprocessing.py
--rw-r--r--   0 runner    (1001) docker     (123)      181 2023-06-03 22:14:29.000000 mlfast-0.0.8/src/mlfast/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      169 2023-06-03 22:14:29.000000 mlfast-0.0.8/src/mlfast/custom_exception.py
--rw-r--r--   0 runner    (1001) docker     (123)      437 2023-06-03 22:14:29.000000 mlfast-0.0.8/src/mlfast/logger.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-03 22:16:07.818027 mlfast-0.0.8/src/mlfast.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1422 2023-06-03 22:16:07.000000 mlfast-0.0.8/src/mlfast.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      404 2023-06-03 22:16:07.000000 mlfast-0.0.8/src/mlfast.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-06-03 22:16:07.000000 mlfast-0.0.8/src/mlfast.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      109 2023-06-03 22:16:07.000000 mlfast-0.0.8/src/mlfast.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        7 2023-06-03 22:16:07.000000 mlfast-0.0.8/src/mlfast.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-04 12:57:43.986586 mlfast-0.0.9/
+-rw-r--r--   0 runner    (1001) docker     (123)     1069 2023-06-04 12:56:26.000000 mlfast-0.0.9/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     1422 2023-06-04 12:57:43.986586 mlfast-0.0.9/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      865 2023-06-04 12:56:26.000000 mlfast-0.0.9/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      218 2023-06-04 12:56:26.000000 mlfast-0.0.9/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)      552 2023-06-04 12:57:43.986586 mlfast-0.0.9/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      762 2023-06-04 12:56:26.000000 mlfast-0.0.9/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-04 12:57:43.982586 mlfast-0.0.9/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-04 12:57:43.986586 mlfast-0.0.9/src/mlfast/
+-rw-r--r--   0 runner    (1001) docker     (123)     1572 2023-06-04 12:56:26.000000 mlfast-0.0.9/src/mlfast/Chatbot.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3058 2023-06-04 12:56:26.000000 mlfast-0.0.9/src/mlfast/Classification.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3162 2023-06-04 12:56:26.000000 mlfast-0.0.9/src/mlfast/Regression.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2537 2023-06-04 12:56:26.000000 mlfast-0.0.9/src/mlfast/Text_preprocessing.py
+-rw-r--r--   0 runner    (1001) docker     (123)      181 2023-06-04 12:56:26.000000 mlfast-0.0.9/src/mlfast/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      169 2023-06-04 12:56:26.000000 mlfast-0.0.9/src/mlfast/custom_exception.py
+-rw-r--r--   0 runner    (1001) docker     (123)      437 2023-06-04 12:56:26.000000 mlfast-0.0.9/src/mlfast/logger.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-04 12:57:43.986586 mlfast-0.0.9/src/mlfast.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1422 2023-06-04 12:57:43.000000 mlfast-0.0.9/src/mlfast.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      404 2023-06-04 12:57:43.000000 mlfast-0.0.9/src/mlfast.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-06-04 12:57:43.000000 mlfast-0.0.9/src/mlfast.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      109 2023-06-04 12:57:43.000000 mlfast-0.0.9/src/mlfast.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        7 2023-06-04 12:57:43.000000 mlfast-0.0.9/src/mlfast.egg-info/top_level.txt
```

### Comparing `mlfast-0.0.8/LICENSE` & `mlfast-0.0.9/LICENSE`

 * *Files identical despite different names*

### Comparing `mlfast-0.0.8/PKG-INFO` & `mlfast-0.0.9/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: mlfast
-Version: 0.0.8
+Version: 0.0.9
 Summary: its a python machine learning package
 Home-page: https://github.com/Abdul-Jaweed/mlfast
 Author: Abdul-Jaweed
 Author-email: jdgaming7320@gmail.com
 License: MIT
 Project-URL: Bug Tracker, https://github.com/Abdul-Jaweed/mlfast/issues
 Classifier: Programming Language :: Python :: 3.7
```

### Comparing `mlfast-0.0.8/README.md` & `mlfast-0.0.9/README.md`

 * *Files identical despite different names*

### Comparing `mlfast-0.0.8/setup.cfg` & `mlfast-0.0.9/setup.cfg`

 * *Files identical despite different names*

### Comparing `mlfast-0.0.8/setup.py` & `mlfast-0.0.9/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 import setuptools
 
 with open("README.md", "r", encoding="utf-8") as f:
     long_description = f.read()
 
-__version__ = "0.0.8"
+__version__ = "0.0.9"
 
 REPO_NAME = "mlfast"
 AUTHOR_USER_NAME = "Abdul-Jaweed"
 SRC_REPO = "mlfast"
 AUTHOR_EMAIL = "jdgaming7320@gmail.com"
 
 setuptools.setup(
```

### Comparing `mlfast-0.0.8/src/mlfast/Chatbot.py` & `mlfast-0.0.9/src/mlfast/Chatbot.py`

 * *Files identical despite different names*

### Comparing `mlfast-0.0.8/src/mlfast/Classification.py` & `mlfast-0.0.9/src/mlfast/Classification.py`

 * *Files identical despite different names*

### Comparing `mlfast-0.0.8/src/mlfast/Regression.py` & `mlfast-0.0.9/src/mlfast/Regression.py`

 * *Files identical despite different names*

### Comparing `mlfast-0.0.8/src/mlfast/Text_preprocessing.py` & `mlfast-0.0.9/src/mlfast/Text_preprocessing.py`

 * *Files identical despite different names*

### Comparing `mlfast-0.0.8/src/mlfast.egg-info/PKG-INFO` & `mlfast-0.0.9/src/mlfast.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: mlfast
-Version: 0.0.8
+Version: 0.0.9
 Summary: its a python machine learning package
 Home-page: https://github.com/Abdul-Jaweed/mlfast
 Author: Abdul-Jaweed
 Author-email: jdgaming7320@gmail.com
 License: MIT
 Project-URL: Bug Tracker, https://github.com/Abdul-Jaweed/mlfast/issues
 Classifier: Programming Language :: Python :: 3.7
```

