# Comparing `tmp/steroid-0.8b0.tar.gz` & `tmp/steroid-0.9b0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "steroid-0.8b0.tar", max compression
+gzip compressed data, was "steroid-0.9b0.tar", max compression
```

## Comparing `steroid-0.8b0.tar` & `steroid-0.9b0.tar`

### file list

```diff
@@ -1,12 +1,12 @@
--rw-r--r--   0        0        0     1078 2023-07-23 18:26:09.045723 steroid-0.8b0/LICENSE
--rw-r--r--   0        0        0     2359 2023-07-23 18:26:09.045723 steroid-0.8b0/README.md
--rw-r--r--   0        0        0      924 2023-07-23 18:26:32.425865 steroid-0.8b0/pyproject.toml
--rw-r--r--   0        0        0      164 2023-07-23 18:26:09.045723 steroid-0.8b0/steroid/__init__.py
--rw-r--r--   0        0        0     1272 2023-07-23 18:26:09.045723 steroid-0.8b0/steroid/app.py
--rw-r--r--   0        0        0      253 2023-07-23 18:26:09.045723 steroid-0.8b0/steroid/constants.py
--rw-r--r--   0        0        0     2309 2023-07-23 18:26:09.045723 steroid-0.8b0/steroid/controller.py
--rw-r--r--   0        0        0     2430 2023-07-23 18:26:09.045723 steroid-0.8b0/steroid/logging.py
--rw-r--r--   0        0        0     1828 2023-07-23 18:26:09.045723 steroid-0.8b0/steroid/methods.py
--rw-r--r--   0        0        0     2695 2023-07-23 18:26:09.045723 steroid-0.8b0/steroid/middleware.py
--rw-r--r--   0        0        0      485 2023-07-23 18:26:09.045723 steroid-0.8b0/steroid/utils.py
--rw-r--r--   0        0        0     3693 1970-01-01 00:00:00.000000 steroid-0.8b0/PKG-INFO
+-rw-r--r--   0        0        0     1078 2023-07-23 18:29:38.149778 steroid-0.9b0/LICENSE
+-rw-r--r--   0        0        0     2359 2023-07-23 18:29:38.149778 steroid-0.9b0/README.md
+-rw-r--r--   0        0        0      924 2023-07-23 18:30:00.018410 steroid-0.9b0/pyproject.toml
+-rw-r--r--   0        0        0      164 2023-07-23 18:29:38.149778 steroid-0.9b0/steroid/__init__.py
+-rw-r--r--   0        0        0     1272 2023-07-23 18:29:38.149778 steroid-0.9b0/steroid/app.py
+-rw-r--r--   0        0        0      253 2023-07-23 18:29:38.149778 steroid-0.9b0/steroid/constants.py
+-rw-r--r--   0        0        0     2309 2023-07-23 18:29:38.149778 steroid-0.9b0/steroid/controller.py
+-rw-r--r--   0        0        0     2430 2023-07-23 18:29:38.149778 steroid-0.9b0/steroid/logging.py
+-rw-r--r--   0        0        0     1828 2023-07-23 18:29:38.149778 steroid-0.9b0/steroid/methods.py
+-rw-r--r--   0        0        0     2695 2023-07-23 18:29:38.149778 steroid-0.9b0/steroid/middleware.py
+-rw-r--r--   0        0        0      485 2023-07-23 18:29:38.149778 steroid-0.9b0/steroid/utils.py
+-rw-r--r--   0        0        0     3693 1970-01-01 00:00:00.000000 steroid-0.9b0/PKG-INFO
```

### Comparing `steroid-0.8b0/LICENSE` & `steroid-0.9b0/LICENSE`

 * *Files identical despite different names*

### Comparing `steroid-0.8b0/README.md` & `steroid-0.9b0/README.md`

 * *Files identical despite different names*

### Comparing `steroid-0.8b0/pyproject.toml` & `steroid-0.9b0/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [tool.poetry]
 name = "steroid"
-version = "v0.8b"
+version = "v0.9b"
 authors = [
   "Mohammed Al Ameen <ameenmohammed2311@gmail.com>"
 ]
 description = "Steroid"
 readme = "README.md"
 
 repository = "https://github.com/struckchure/steroid"
```

### Comparing `steroid-0.8b0/steroid/app.py` & `steroid-0.9b0/steroid/app.py`

 * *Files identical despite different names*

### Comparing `steroid-0.8b0/steroid/controller.py` & `steroid-0.9b0/steroid/controller.py`

 * *Files identical despite different names*

### Comparing `steroid-0.8b0/steroid/logging.py` & `steroid-0.9b0/steroid/logging.py`

 * *Files identical despite different names*

### Comparing `steroid-0.8b0/steroid/methods.py` & `steroid-0.9b0/steroid/methods.py`

 * *Files identical despite different names*

### Comparing `steroid-0.8b0/steroid/middleware.py` & `steroid-0.9b0/steroid/middleware.py`

 * *Files identical despite different names*

### Comparing `steroid-0.8b0/PKG-INFO` & `steroid-0.9b0/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: steroid
-Version: 0.8b0
+Version: 0.9b0
 Summary: Steroid
 Home-page: https://github.com/struckchure/steroid
 Author: Mohammed Al Ameen
 Author-email: ameenmohammed2311@gmail.com
 Requires-Python: >=3.8,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

