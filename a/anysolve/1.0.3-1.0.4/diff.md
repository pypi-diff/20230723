# Comparing `tmp/anysolve-1.0.3.tar.gz` & `tmp/anysolve-1.0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "anysolve-1.0.3.tar", last modified: Sat Jul 22 11:30:12 2023, max compression
+gzip compressed data, was "anysolve-1.0.4.tar", last modified: Sun Jul 23 19:28:15 2023, max compression
```

## Comparing `anysolve-1.0.3.tar` & `anysolve-1.0.4.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 11:30:12.639943 anysolve-1.0.3/
--rw-r--r--   0 runner    (1001) docker     (123)     1211 2023-07-22 11:30:11.000000 anysolve-1.0.3/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)    11770 2023-07-22 11:30:12.639943 anysolve-1.0.3/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     8397 2023-07-22 11:30:11.000000 anysolve-1.0.3/README.rst
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 11:30:12.639943 anysolve-1.0.3/anysolve/
--rw-r--r--   0 runner    (1001) docker     (123)      851 2023-07-22 11:30:11.000000 anysolve-1.0.3/anysolve/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 11:30:12.639943 anysolve-1.0.3/anysolve.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)    11770 2023-07-22 11:30:12.000000 anysolve-1.0.3/anysolve.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      248 2023-07-22 11:30:12.000000 anysolve-1.0.3/anysolve.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-22 11:30:12.000000 anysolve-1.0.3/anysolve.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-22 11:30:12.000000 anysolve-1.0.3/anysolve.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-22 11:30:12.000000 anysolve-1.0.3/anysolve.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-22 11:30:12.000000 anysolve-1.0.3/anysolve.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)      203 2023-07-22 11:30:12.643943 anysolve-1.0.3/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1754 2023-07-22 11:30:11.000000 anysolve-1.0.3/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:28:15.762932 anysolve-1.0.4/
+-rw-r--r--   0 runner    (1001) docker     (123)     1211 2023-07-23 19:28:14.000000 anysolve-1.0.4/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)    11765 2023-07-23 19:28:15.766932 anysolve-1.0.4/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     8397 2023-07-23 19:28:14.000000 anysolve-1.0.4/README.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:28:15.762932 anysolve-1.0.4/anysolve/
+-rw-r--r--   0 runner    (1001) docker     (123)      851 2023-07-23 19:28:14.000000 anysolve-1.0.4/anysolve/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:28:15.762932 anysolve-1.0.4/anysolve.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)    11765 2023-07-23 19:28:15.000000 anysolve-1.0.4/anysolve.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      248 2023-07-23 19:28:15.000000 anysolve-1.0.4/anysolve.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 19:28:15.000000 anysolve-1.0.4/anysolve.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 19:28:15.000000 anysolve-1.0.4/anysolve.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-23 19:28:15.000000 anysolve-1.0.4/anysolve.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-23 19:28:15.000000 anysolve-1.0.4/anysolve.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      203 2023-07-23 19:28:15.766932 anysolve-1.0.4/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1749 2023-07-23 19:28:14.000000 anysolve-1.0.4/setup.py
```

### Comparing `anysolve-1.0.3/LICENSE` & `anysolve-1.0.4/LICENSE`

 * *Files identical despite different names*

### Comparing `anysolve-1.0.3/PKG-INFO` & `anysolve-1.0.4/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 Metadata-Version: 1.2
 Name: anysolve
-Version: 1.0.3
+Version: 1.0.4
 Summary: AnySolve.ai Client library
 Home-page: https://github.com/BlackriverOrg/anysolve
-Author: Simon Hecht
-Author-email: simon_hecht@hotmail.com
+Author: AnySolve.ai
+Author-email: office@anysolve.ai
 License: License :: OSI Approved :: The Unlicense (Unlicense)
 Description: #########################
          Python Library anysolve
         #########################
         
         `anysolve` is a library for executing `AnySolve.ai <https://www.anysolve.ai>`_ tasks. It needs an `API-Key` that can be
         created in the settings of an anysolve.ai account. The settings can be
```

### Comparing `anysolve-1.0.3/README.rst` & `anysolve-1.0.4/README.rst`

 * *Files identical despite different names*

### Comparing `anysolve-1.0.3/anysolve/__init__.py` & `anysolve-1.0.4/anysolve/__init__.py`

 * *Files identical despite different names*

### Comparing `anysolve-1.0.3/anysolve.egg-info/PKG-INFO` & `anysolve-1.0.4/anysolve.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 Metadata-Version: 1.2
 Name: anysolve
-Version: 1.0.3
+Version: 1.0.4
 Summary: AnySolve.ai Client library
 Home-page: https://github.com/BlackriverOrg/anysolve
-Author: Simon Hecht
-Author-email: simon_hecht@hotmail.com
+Author: AnySolve.ai
+Author-email: office@anysolve.ai
 License: License :: OSI Approved :: The Unlicense (Unlicense)
 Description: #########################
          Python Library anysolve
         #########################
         
         `anysolve` is a library for executing `AnySolve.ai <https://www.anysolve.ai>`_ tasks. It needs an `API-Key` that can be
         created in the settings of an anysolve.ai account. The settings can be
```

### Comparing `anysolve-1.0.3/setup.py` & `anysolve-1.0.4/setup.py`

 * *Files 4% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 import setuptools
 
 
 # Package metadata.
 
 name = "anysolve"
 description = "AnySolve.ai Client library"
-version = "1.0.3"
+version = "1.0.4"
 release_status = "Development Status :: 5 - Production/Stable"
 dependencies = [
     "requests",
 ]
 extras = {}
 
 
@@ -27,16 +27,16 @@
 packages = [package for package in setuptools.find_packages()]
 
 setuptools.setup(
     name=name,
     version=version,
     description=description,
     long_description=readme,
-    author="Simon Hecht",
-    author_email="simon_hecht@hotmail.com",
+    author="AnySolve.ai",
+    author_email="office@anysolve.ai",
     license="License :: OSI Approved :: The Unlicense (Unlicense)",
     url="https://github.com/BlackriverOrg/anysolve",
     classifiers=[
         release_status,
         "Intended Audience :: Developers",
         "License :: OSI Approved :: The Unlicense (Unlicense)",
         "Programming Language :: Python",
```

