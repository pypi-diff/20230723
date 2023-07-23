# Comparing `tmp/PyGameLab-3.2.6.tar.gz` & `tmp/PyGameLab-3.2.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "PyGameLab-3.2.6.tar", last modified: Sun Jul 23 19:29:23 2023, max compression
+gzip compressed data, was "PyGameLab-3.2.7.tar", last modified: Sun Jul 23 19:49:10 2023, max compression
```

## Comparing `PyGameLab-3.2.6.tar` & `PyGameLab-3.2.7.tar`

### file list

```diff
@@ -1,21 +1,21 @@
-drwxr-xr-x   0 leandrofeippe     (0) staff       (20)        0 2023-07-23 19:29:23.000000 PyGameLab-3.2.6/
--rw-r--r--   0 leandrofeippe     (0) staff       (20)     1072 2023-07-16 20:03:01.000000 PyGameLab-3.2.6/LICENCE
--rw-r--r--   0 leandrofeippe     (0) staff       (20)     1789 2023-07-23 19:29:23.000000 PyGameLab-3.2.6/PKG-INFO
--rw-r--r--   0 leandrofeippe     (0) staff       (20)     1228 2023-07-23 19:21:52.000000 PyGameLab-3.2.6/README.md
--rw-r--r--   0 leandrofeippe     (0) staff       (20)      646 2023-07-23 19:28:47.000000 PyGameLab-3.2.6/pyproject.toml
--rw-r--r--   0 leandrofeippe     (0) staff       (20)       38 2023-07-23 19:29:23.000000 PyGameLab-3.2.6/setup.cfg
-drwxr-xr-x   0 leandrofeippe     (0) staff       (20)        0 2023-07-23 19:29:23.000000 PyGameLab-3.2.6/src/
-drwxr-xr-x   0 leandrofeippe     (0) staff       (20)        0 2023-07-23 19:29:23.000000 PyGameLab-3.2.6/src/PyGameLab.egg-info/
--rw-r--r--   0 leandrofeippe     (0) staff       (20)     1789 2023-07-23 19:29:23.000000 PyGameLab-3.2.6/src/PyGameLab.egg-info/PKG-INFO
--rw-r--r--   0 leandrofeippe     (0) staff       (20)      375 2023-07-23 19:29:23.000000 PyGameLab-3.2.6/src/PyGameLab.egg-info/SOURCES.txt
--rw-r--r--   0 leandrofeippe     (0) staff       (20)        1 2023-07-23 19:29:23.000000 PyGameLab-3.2.6/src/PyGameLab.egg-info/dependency_links.txt
--rw-r--r--   0 leandrofeippe     (0) staff       (20)       10 2023-07-23 19:29:23.000000 PyGameLab-3.2.6/src/PyGameLab.egg-info/top_level.txt
-drwxr-xr-x   0 leandrofeippe     (0) staff       (20)        0 2023-07-23 19:29:23.000000 PyGameLab-3.2.6/src/pygamelab/
--rw-r--r--   0 leandrofeippe     (0) staff       (20)      959 2023-07-23 19:16:05.000000 PyGameLab-3.2.6/src/pygamelab/__init__.py
--rw-r--r--   0 leandrofeippe     (0) staff       (20)     1945 2023-07-23 18:39:26.000000 PyGameLab-3.2.6/src/pygamelab/canvas.py
--rw-r--r--   0 leandrofeippe     (0) staff       (20)     8669 2023-07-23 18:39:11.000000 PyGameLab-3.2.6/src/pygamelab/common.py
--rw-r--r--   0 leandrofeippe     (0) staff       (20)      813 2023-07-23 19:28:24.000000 PyGameLab-3.2.6/src/pygamelab/data.py
--rw-r--r--   0 leandrofeippe     (0) staff       (20)     1298 2023-07-23 18:27:02.000000 PyGameLab-3.2.6/src/pygamelab/document.py
--rw-r--r--   0 leandrofeippe     (0) staff       (20)      343 2023-07-23 18:39:52.000000 PyGameLab-3.2.6/src/pygamelab/locals.py
--rw-r--r--   0 leandrofeippe     (0) staff       (20)     1623 2023-07-23 18:30:07.000000 PyGameLab-3.2.6/src/pygamelab/random.py
--rw-r--r--   0 leandrofeippe     (0) staff       (20)      929 2023-07-23 18:40:13.000000 PyGameLab-3.2.6/src/pygamelab/storage.py
+drwxr-xr-x   0 leandrofeippe     (0) staff       (20)        0 2023-07-23 19:49:10.000000 PyGameLab-3.2.7/
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)     1072 2023-07-16 20:03:01.000000 PyGameLab-3.2.7/LICENCE
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)     1789 2023-07-23 19:49:10.000000 PyGameLab-3.2.7/PKG-INFO
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)     1228 2023-07-23 19:21:52.000000 PyGameLab-3.2.7/README.md
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)      646 2023-07-23 19:48:30.000000 PyGameLab-3.2.7/pyproject.toml
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)       38 2023-07-23 19:49:10.000000 PyGameLab-3.2.7/setup.cfg
+drwxr-xr-x   0 leandrofeippe     (0) staff       (20)        0 2023-07-23 19:49:10.000000 PyGameLab-3.2.7/src/
+drwxr-xr-x   0 leandrofeippe     (0) staff       (20)        0 2023-07-23 19:49:10.000000 PyGameLab-3.2.7/src/PyGameLab.egg-info/
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)     1789 2023-07-23 19:49:10.000000 PyGameLab-3.2.7/src/PyGameLab.egg-info/PKG-INFO
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)      375 2023-07-23 19:49:10.000000 PyGameLab-3.2.7/src/PyGameLab.egg-info/SOURCES.txt
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)        1 2023-07-23 19:49:10.000000 PyGameLab-3.2.7/src/PyGameLab.egg-info/dependency_links.txt
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)       10 2023-07-23 19:49:10.000000 PyGameLab-3.2.7/src/PyGameLab.egg-info/top_level.txt
+drwxr-xr-x   0 leandrofeippe     (0) staff       (20)        0 2023-07-23 19:49:10.000000 PyGameLab-3.2.7/src/pygamelab/
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)      964 2023-07-23 19:44:55.000000 PyGameLab-3.2.7/src/pygamelab/__init__.py
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)     1945 2023-07-23 18:39:26.000000 PyGameLab-3.2.7/src/pygamelab/canvas.py
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)     8669 2023-07-23 18:39:11.000000 PyGameLab-3.2.7/src/pygamelab/common.py
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)      813 2023-07-23 19:28:24.000000 PyGameLab-3.2.7/src/pygamelab/data.py
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)     1160 2023-07-23 19:47:34.000000 PyGameLab-3.2.7/src/pygamelab/document.py
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)      343 2023-07-23 18:39:52.000000 PyGameLab-3.2.7/src/pygamelab/locals.py
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)     1623 2023-07-23 18:30:07.000000 PyGameLab-3.2.7/src/pygamelab/random.py
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)      929 2023-07-23 18:40:13.000000 PyGameLab-3.2.7/src/pygamelab/storage.py
```

### Comparing `PyGameLab-3.2.6/LICENCE` & `PyGameLab-3.2.7/LICENCE`

 * *Files identical despite different names*

### Comparing `PyGameLab-3.2.6/PKG-INFO` & `PyGameLab-3.2.7/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: PyGameLab
-Version: 3.2.6
+Version: 3.2.7
 Summary: PyGameLab: A versatile Python library for game development using Pygame.
 Author-email: Leandro Feippe <feippe5454@gmail.com>
 Project-URL: Homepage, https://github.com/leandrofeippe/pygamelab
 Project-URL: Bug Tracker, https://github.com/leandrofeippe/pygamelab/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `PyGameLab-3.2.6/README.md` & `PyGameLab-3.2.7/README.md`

 * *Files identical despite different names*

### Comparing `PyGameLab-3.2.6/pyproject.toml` & `PyGameLab-3.2.7/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 [build-system]
 requires = ["setuptools>=61.0", "pygame"]
 build-backend = "setuptools.build_meta"
 
 
 [project]
 name = "PyGameLab"
-version = "3.2.6"
+version = "3.2.7"
 authors = [
   { name="Leandro Feippe", email="feippe5454@gmail.com" },
 ]
 description = "PyGameLab: A versatile Python library for game development using Pygame."
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = [
```

### Comparing `PyGameLab-3.2.6/src/PyGameLab.egg-info/PKG-INFO` & `PyGameLab-3.2.7/src/PyGameLab.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: PyGameLab
-Version: 3.2.6
+Version: 3.2.7
 Summary: PyGameLab: A versatile Python library for game development using Pygame.
 Author-email: Leandro Feippe <feippe5454@gmail.com>
 Project-URL: Homepage, https://github.com/leandrofeippe/pygamelab
 Project-URL: Bug Tracker, https://github.com/leandrofeippe/pygamelab/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `PyGameLab-3.2.6/src/pygamelab/__init__.py` & `PyGameLab-3.2.7/src/pygamelab/__init__.py`

 * *Files 16% similar despite different names*

```diff
@@ -9,15 +9,15 @@
     if not data.initialized:
         pygame.init()
         document.Unicode.key = {}
         for codepoint in range(0x10000):
             char = chr(codepoint)
             name = unicodedata.name(char, "")
             document.Unicode.key[name] = char
-        initialized = True
+        data.initialized = True
         pivot_point = (0, 0)
         print(
             f"\npygamelab {data.version} ({data.interpreter})", file=sys.stdout)
         print("Hello from PyGameLab Services.", file=sys.stdout)
         print(
             f"You are currently using {len(data.dependences)} dependences:", file=sys.stdout)
         print(f"  - {data.dependences_printable}.", file=sys.stdout)
```

### Comparing `PyGameLab-3.2.6/src/pygamelab/canvas.py` & `PyGameLab-3.2.7/src/pygamelab/canvas.py`

 * *Files identical despite different names*

### Comparing `PyGameLab-3.2.6/src/pygamelab/common.py` & `PyGameLab-3.2.7/src/pygamelab/common.py`

 * *Files identical despite different names*

### Comparing `PyGameLab-3.2.6/src/pygamelab/data.py` & `PyGameLab-3.2.7/src/pygamelab/data.py`

 * *Files identical despite different names*

### Comparing `PyGameLab-3.2.6/src/pygamelab/document.py` & `PyGameLab-3.2.7/src/pygamelab/document.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,35 +1,26 @@
-import pygame
-import unicodedata
-import sys
-import string
-import random
-import json
 import difflib
-import datetime
-import pygame.locals
-import os
-from PyGameLab.common import Data
+from PyGameLab import data
 
 class Unicode:
     @staticmethod
     def char(char_name):
-        if Data.initialized:
+        if data.initialized:
             if char_name in Unicode.key:
                 return Unicode.key[char_name]
             else:
                 matches = difflib.get_close_matches(
                     char_name, Unicode.key.keys(), n=1)
                 if matches:
                     return Unicode.key[matches[0]]
                 else:
                     raise ValueError(
                         "No se encontró el carácter Unicode correspondiente.")
         else:
-            raise TypeError("PyGameLab no se ha inicializado correctamente.")
+            raise NameError("PyGameLab no se ha inicializado correctamente.")
 
 
 
 
 class Colors:
     class text:
         RESET = "\033[0m"
```

### Comparing `PyGameLab-3.2.6/src/pygamelab/random.py` & `PyGameLab-3.2.7/src/pygamelab/random.py`

 * *Files identical despite different names*

### Comparing `PyGameLab-3.2.6/src/pygamelab/storage.py` & `PyGameLab-3.2.7/src/pygamelab/storage.py`

 * *Files identical despite different names*

