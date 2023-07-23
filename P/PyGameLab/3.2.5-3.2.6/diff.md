# Comparing `tmp/PyGameLab-3.2.5.tar.gz` & `tmp/PyGameLab-3.2.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "PyGameLab-3.2.5.tar", last modified: Sun Jul 23 19:21:31 2023, max compression
+gzip compressed data, was "PyGameLab-3.2.6.tar", last modified: Sun Jul 23 19:29:23 2023, max compression
```

## Comparing `PyGameLab-3.2.5.tar` & `PyGameLab-3.2.6.tar`

### file list

```diff
@@ -1,21 +1,21 @@
-drwxr-xr-x   0 leandrofeippe     (0) staff       (20)        0 2023-07-23 19:21:31.000000 PyGameLab-3.2.5/
--rw-r--r--   0 leandrofeippe     (0) staff       (20)     1072 2023-07-16 20:03:01.000000 PyGameLab-3.2.5/LICENCE
--rw-r--r--   0 leandrofeippe     (0) staff       (20)     1796 2023-07-23 19:21:31.000000 PyGameLab-3.2.5/PKG-INFO
--rw-r--r--   0 leandrofeippe     (0) staff       (20)     1235 2023-07-23 00:04:45.000000 PyGameLab-3.2.5/README.md
--rw-r--r--   0 leandrofeippe     (0) staff       (20)      646 2023-07-23 19:20:43.000000 PyGameLab-3.2.5/pyproject.toml
--rw-r--r--   0 leandrofeippe     (0) staff       (20)       38 2023-07-23 19:21:31.000000 PyGameLab-3.2.5/setup.cfg
-drwxr-xr-x   0 leandrofeippe     (0) staff       (20)        0 2023-07-23 19:21:31.000000 PyGameLab-3.2.5/src/
-drwxr-xr-x   0 leandrofeippe     (0) staff       (20)        0 2023-07-23 19:21:31.000000 PyGameLab-3.2.5/src/PyGameLab.egg-info/
--rw-r--r--   0 leandrofeippe     (0) staff       (20)     1796 2023-07-23 19:21:31.000000 PyGameLab-3.2.5/src/PyGameLab.egg-info/PKG-INFO
--rw-r--r--   0 leandrofeippe     (0) staff       (20)      375 2023-07-23 19:21:31.000000 PyGameLab-3.2.5/src/PyGameLab.egg-info/SOURCES.txt
--rw-r--r--   0 leandrofeippe     (0) staff       (20)        1 2023-07-23 19:21:31.000000 PyGameLab-3.2.5/src/PyGameLab.egg-info/dependency_links.txt
--rw-r--r--   0 leandrofeippe     (0) staff       (20)       10 2023-07-23 19:21:31.000000 PyGameLab-3.2.5/src/PyGameLab.egg-info/top_level.txt
-drwxr-xr-x   0 leandrofeippe     (0) staff       (20)        0 2023-07-23 19:21:31.000000 PyGameLab-3.2.5/src/pygamelab/
--rw-r--r--   0 leandrofeippe     (0) staff       (20)      959 2023-07-23 19:16:05.000000 PyGameLab-3.2.5/src/pygamelab/__init__.py
--rw-r--r--   0 leandrofeippe     (0) staff       (20)     1945 2023-07-23 18:39:26.000000 PyGameLab-3.2.5/src/pygamelab/canvas.py
--rw-r--r--   0 leandrofeippe     (0) staff       (20)     8669 2023-07-23 18:39:11.000000 PyGameLab-3.2.5/src/pygamelab/common.py
--rw-r--r--   0 leandrofeippe     (0) staff       (20)      813 2023-07-23 19:20:59.000000 PyGameLab-3.2.5/src/pygamelab/data.py
--rw-r--r--   0 leandrofeippe     (0) staff       (20)     1298 2023-07-23 18:27:02.000000 PyGameLab-3.2.5/src/pygamelab/document.py
--rw-r--r--   0 leandrofeippe     (0) staff       (20)      343 2023-07-23 18:39:52.000000 PyGameLab-3.2.5/src/pygamelab/locals.py
--rw-r--r--   0 leandrofeippe     (0) staff       (20)     1623 2023-07-23 18:30:07.000000 PyGameLab-3.2.5/src/pygamelab/random.py
--rw-r--r--   0 leandrofeippe     (0) staff       (20)      929 2023-07-23 18:40:13.000000 PyGameLab-3.2.5/src/pygamelab/storage.py
+drwxr-xr-x   0 leandrofeippe     (0) staff       (20)        0 2023-07-23 19:29:23.000000 PyGameLab-3.2.6/
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)     1072 2023-07-16 20:03:01.000000 PyGameLab-3.2.6/LICENCE
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)     1789 2023-07-23 19:29:23.000000 PyGameLab-3.2.6/PKG-INFO
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)     1228 2023-07-23 19:21:52.000000 PyGameLab-3.2.6/README.md
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)      646 2023-07-23 19:28:47.000000 PyGameLab-3.2.6/pyproject.toml
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)       38 2023-07-23 19:29:23.000000 PyGameLab-3.2.6/setup.cfg
+drwxr-xr-x   0 leandrofeippe     (0) staff       (20)        0 2023-07-23 19:29:23.000000 PyGameLab-3.2.6/src/
+drwxr-xr-x   0 leandrofeippe     (0) staff       (20)        0 2023-07-23 19:29:23.000000 PyGameLab-3.2.6/src/PyGameLab.egg-info/
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)     1789 2023-07-23 19:29:23.000000 PyGameLab-3.2.6/src/PyGameLab.egg-info/PKG-INFO
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)      375 2023-07-23 19:29:23.000000 PyGameLab-3.2.6/src/PyGameLab.egg-info/SOURCES.txt
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)        1 2023-07-23 19:29:23.000000 PyGameLab-3.2.6/src/PyGameLab.egg-info/dependency_links.txt
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)       10 2023-07-23 19:29:23.000000 PyGameLab-3.2.6/src/PyGameLab.egg-info/top_level.txt
+drwxr-xr-x   0 leandrofeippe     (0) staff       (20)        0 2023-07-23 19:29:23.000000 PyGameLab-3.2.6/src/pygamelab/
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)      959 2023-07-23 19:16:05.000000 PyGameLab-3.2.6/src/pygamelab/__init__.py
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)     1945 2023-07-23 18:39:26.000000 PyGameLab-3.2.6/src/pygamelab/canvas.py
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)     8669 2023-07-23 18:39:11.000000 PyGameLab-3.2.6/src/pygamelab/common.py
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)      813 2023-07-23 19:28:24.000000 PyGameLab-3.2.6/src/pygamelab/data.py
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)     1298 2023-07-23 18:27:02.000000 PyGameLab-3.2.6/src/pygamelab/document.py
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)      343 2023-07-23 18:39:52.000000 PyGameLab-3.2.6/src/pygamelab/locals.py
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)     1623 2023-07-23 18:30:07.000000 PyGameLab-3.2.6/src/pygamelab/random.py
+-rw-r--r--   0 leandrofeippe     (0) staff       (20)      929 2023-07-23 18:40:13.000000 PyGameLab-3.2.6/src/pygamelab/storage.py
```

### Comparing `PyGameLab-3.2.5/LICENCE` & `PyGameLab-3.2.6/LICENCE`

 * *Files identical despite different names*

### Comparing `PyGameLab-3.2.5/PKG-INFO` & `PyGameLab-3.2.6/PKG-INFO`

 * *Files 13% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: PyGameLab
-Version: 3.2.5
+Version: 3.2.6
 Summary: PyGameLab: A versatile Python library for game development using Pygame.
 Author-email: Leandro Feippe <feippe5454@gmail.com>
 Project-URL: Homepage, https://github.com/leandrofeippe/pygamelab
 Project-URL: Bug Tracker, https://github.com/leandrofeippe/pygamelab/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
@@ -32,24 +32,23 @@
 - Console logging and debugging utilities
 
 
 ## Installation
 
 You can install PygameLab using pip:
 
-`pip install pygamelab`
+`pip install PyGameLab`
 
 
 ## Usage
 
 Here's a simple example of how to use PygameLab to create a game window:
 
 ```python
-import pygame
-from pygamelab import Window
+from PyGameLab.common import Window
 
 # Create a game window
 window = Window((800, 600), "My Game")
 
 # Main game loop
 while window.running:
     for event in pygame.event.get():
```

### Comparing `PyGameLab-3.2.5/README.md` & `PyGameLab-3.2.6/README.md`

 * *Files 12% similar despite different names*

```diff
@@ -18,24 +18,23 @@
 - Console logging and debugging utilities
 
 
 ## Installation
 
 You can install PygameLab using pip:
 
-`pip install pygamelab`
+`pip install PyGameLab`
 
 
 ## Usage
 
 Here's a simple example of how to use PygameLab to create a game window:
 
 ```python
-import pygame
-from pygamelab import Window
+from PyGameLab.common import Window
 
 # Create a game window
 window = Window((800, 600), "My Game")
 
 # Main game loop
 while window.running:
     for event in pygame.event.get():
```

### Comparing `PyGameLab-3.2.5/pyproject.toml` & `PyGameLab-3.2.6/pyproject.toml`

 * *Files 18% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 [build-system]
 requires = ["setuptools>=61.0", "pygame"]
 build-backend = "setuptools.build_meta"
 
 
 [project]
 name = "PyGameLab"
-version = "3.2.5"
+version = "3.2.6"
 authors = [
   { name="Leandro Feippe", email="feippe5454@gmail.com" },
 ]
 description = "PyGameLab: A versatile Python library for game development using Pygame."
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = [
```

### Comparing `PyGameLab-3.2.5/src/PyGameLab.egg-info/PKG-INFO` & `PyGameLab-3.2.6/src/PyGameLab.egg-info/PKG-INFO`

 * *Files 13% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: PyGameLab
-Version: 3.2.5
+Version: 3.2.6
 Summary: PyGameLab: A versatile Python library for game development using Pygame.
 Author-email: Leandro Feippe <feippe5454@gmail.com>
 Project-URL: Homepage, https://github.com/leandrofeippe/pygamelab
 Project-URL: Bug Tracker, https://github.com/leandrofeippe/pygamelab/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
@@ -32,24 +32,23 @@
 - Console logging and debugging utilities
 
 
 ## Installation
 
 You can install PygameLab using pip:
 
-`pip install pygamelab`
+`pip install PyGameLab`
 
 
 ## Usage
 
 Here's a simple example of how to use PygameLab to create a game window:
 
 ```python
-import pygame
-from pygamelab import Window
+from PyGameLab.common import Window
 
 # Create a game window
 window = Window((800, 600), "My Game")
 
 # Main game loop
 while window.running:
     for event in pygame.event.get():
```

### Comparing `PyGameLab-3.2.5/src/pygamelab/__init__.py` & `PyGameLab-3.2.6/src/pygamelab/__init__.py`

 * *Files identical despite different names*

### Comparing `PyGameLab-3.2.5/src/pygamelab/canvas.py` & `PyGameLab-3.2.6/src/pygamelab/canvas.py`

 * *Files identical despite different names*

### Comparing `PyGameLab-3.2.5/src/pygamelab/common.py` & `PyGameLab-3.2.6/src/pygamelab/common.py`

 * *Files identical despite different names*

### Comparing `PyGameLab-3.2.5/src/pygamelab/data.py` & `PyGameLab-3.2.6/src/pygamelab/data.py`

 * *Files 12% similar despite different names*

```diff
@@ -9,15 +9,15 @@
 dependences.append("string")
 dependences.append("sys")
 dependences.append("unicodedata")
 
 dependences.append("pygame")
 
 initialized = False
-version = "3.2.5"
+version = "3.2.6"
 interpreter = "Python 3.10.11"
 dependences_printable = "\n  - ".join(dependences)
 
 
 class Date:
     today = datetime.date.today()
     now = datetime.datetime.now()
```

### Comparing `PyGameLab-3.2.5/src/pygamelab/document.py` & `PyGameLab-3.2.6/src/pygamelab/document.py`

 * *Files identical despite different names*

### Comparing `PyGameLab-3.2.5/src/pygamelab/random.py` & `PyGameLab-3.2.6/src/pygamelab/random.py`

 * *Files identical despite different names*

### Comparing `PyGameLab-3.2.5/src/pygamelab/storage.py` & `PyGameLab-3.2.6/src/pygamelab/storage.py`

 * *Files identical despite different names*

