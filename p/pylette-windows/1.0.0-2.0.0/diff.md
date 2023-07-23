# Comparing `tmp/pylette-windows-1.0.0.tar.gz` & `tmp/pylette-windows-2.0.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pylette-windows-1.0.0.tar", last modified: Tue Jul 18 19:31:10 2023, max compression
+gzip compressed data, was "pylette-windows-2.0.0.tar", last modified: Sun Jul 23 15:30:41 2023, max compression
```

## Comparing `pylette-windows-1.0.0.tar` & `pylette-windows-2.0.0.tar`

### file list

```diff
@@ -1,22 +1,22 @@
-drwxrwxrwx   0        0        0        0 2023-07-18 19:31:10.111300 pylette-windows-1.0.0/
--rw-rw-rw-   0        0        0     1095 2023-07-18 18:36:23.000000 pylette-windows-1.0.0/LICENSE.md
--rw-rw-rw-   0        0        0     9240 2023-07-18 19:31:10.112304 pylette-windows-1.0.0/PKG-INFO
--rw-rw-rw-   0        0        0     7465 2023-07-18 18:36:23.000000 pylette-windows-1.0.0/README.md
--rw-rw-rw-   0        0        0      784 2023-07-18 19:29:49.000000 pylette-windows-1.0.0/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-07-18 19:31:10.112304 pylette-windows-1.0.0/setup.cfg
-drwxrwxrwx   0        0        0        0 2023-07-18 19:31:10.081302 pylette-windows-1.0.0/src/
-drwxrwxrwx   0        0        0        0 2023-07-18 19:31:10.094302 pylette-windows-1.0.0/src/Pylette/
--rw-rw-rw-   0        0        0      102 2023-07-18 18:36:23.000000 pylette-windows-1.0.0/src/Pylette/__init__.py
--rw-rw-rw-   0        0        0     1921 2023-07-18 18:36:17.000000 pylette-windows-1.0.0/src/Pylette/auxiliary.py
--rw-rw-rw-   0        0        0     1703 2023-07-18 18:36:23.000000 pylette-windows-1.0.0/src/Pylette/cmd.py
--rw-rw-rw-   0        0        0     1196 2023-07-18 18:36:23.000000 pylette-windows-1.0.0/src/Pylette/color.py
--rw-rw-rw-   0        0        0     2976 2023-07-18 18:48:04.000000 pylette-windows-1.0.0/src/Pylette/color_extraction.py
--rw-rw-rw-   0        0        0     3869 2023-07-18 18:36:23.000000 pylette-windows-1.0.0/src/Pylette/gui.py
--rw-rw-rw-   0        0        0     2963 2023-07-18 18:36:23.000000 pylette-windows-1.0.0/src/Pylette/palette.py
-drwxrwxrwx   0        0        0        0 2023-07-18 19:31:10.110300 pylette-windows-1.0.0/src/pylette_windows.egg-info/
--rw-rw-rw-   0        0        0     9240 2023-07-18 19:31:10.000000 pylette-windows-1.0.0/src/pylette_windows.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      468 2023-07-18 19:31:10.000000 pylette-windows-1.0.0/src/pylette_windows.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-18 19:31:10.000000 pylette-windows-1.0.0/src/pylette_windows.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       49 2023-07-18 19:31:10.000000 pylette-windows-1.0.0/src/pylette_windows.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0       63 2023-07-18 19:31:10.000000 pylette-windows-1.0.0/src/pylette_windows.egg-info/requires.txt
--rw-rw-rw-   0        0        0        8 2023-07-18 19:31:10.000000 pylette-windows-1.0.0/src/pylette_windows.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 15:30:41.632555 pylette-windows-2.0.0/
+-rw-rw-rw-   0        0        0     1095 2023-07-18 18:36:23.000000 pylette-windows-2.0.0/LICENSE.md
+-rw-rw-rw-   0        0        0     9240 2023-07-23 15:30:41.632555 pylette-windows-2.0.0/PKG-INFO
+-rw-rw-rw-   0        0        0     7465 2023-07-18 18:36:23.000000 pylette-windows-2.0.0/README.md
+-rw-rw-rw-   0        0        0      784 2023-07-23 15:28:21.000000 pylette-windows-2.0.0/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-07-23 15:30:41.633546 pylette-windows-2.0.0/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-07-23 15:30:41.573546 pylette-windows-2.0.0/src/
+drwxrwxrwx   0        0        0        0 2023-07-23 15:30:41.588545 pylette-windows-2.0.0/src/Pylette/
+-rw-rw-rw-   0        0        0      102 2023-07-18 18:36:23.000000 pylette-windows-2.0.0/src/Pylette/__init__.py
+-rw-rw-rw-   0        0        0     1921 2023-07-18 18:36:17.000000 pylette-windows-2.0.0/src/Pylette/auxiliary.py
+-rw-rw-rw-   0        0        0     1703 2023-07-18 18:36:23.000000 pylette-windows-2.0.0/src/Pylette/cmd.py
+-rw-rw-rw-   0        0        0     1196 2023-07-18 18:36:23.000000 pylette-windows-2.0.0/src/Pylette/color.py
+-rw-rw-rw-   0        0        0     2976 2023-07-18 18:48:04.000000 pylette-windows-2.0.0/src/Pylette/color_extraction.py
+-rw-rw-rw-   0        0        0     3869 2023-07-18 18:36:23.000000 pylette-windows-2.0.0/src/Pylette/gui.py
+-rw-rw-rw-   0        0        0     2963 2023-07-18 18:36:23.000000 pylette-windows-2.0.0/src/Pylette/palette.py
+drwxrwxrwx   0        0        0        0 2023-07-23 15:30:41.631547 pylette-windows-2.0.0/src/pylette_windows.egg-info/
+-rw-rw-rw-   0        0        0     9240 2023-07-23 15:30:41.000000 pylette-windows-2.0.0/src/pylette_windows.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      468 2023-07-23 15:30:41.000000 pylette-windows-2.0.0/src/pylette_windows.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 15:30:41.000000 pylette-windows-2.0.0/src/pylette_windows.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       49 2023-07-23 15:30:41.000000 pylette-windows-2.0.0/src/pylette_windows.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0       63 2023-07-23 15:30:41.000000 pylette-windows-2.0.0/src/pylette_windows.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       21 2023-07-23 15:30:41.000000 pylette-windows-2.0.0/src/pylette_windows.egg-info/top_level.txt
```

### Comparing `pylette-windows-1.0.0/LICENSE.md` & `pylette-windows-2.0.0/LICENSE.md`

 * *Files identical despite different names*

### Comparing `pylette-windows-1.0.0/PKG-INFO` & `pylette-windows-2.0.0/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pylette-windows
-Version: 1.0.0
+Version: 2.0.0
 Summary: Pylette for Windows
 Author-email: Austin Bryant <c00481025@louisiana.edu>
 License: MIT License
         
         Copyright (c) [2018] [Ivar Stangeby]
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
```

### Comparing `pylette-windows-1.0.0/README.md` & `pylette-windows-2.0.0/README.md`

 * *Files identical despite different names*

### Comparing `pylette-windows-1.0.0/pyproject.toml` & `pylette-windows-2.0.0/pyproject.toml`

 * *Files 14% similar despite different names*

```diff
@@ -1,26 +1,26 @@
 [build-system]
 requires = ["setuptools>=61.0.0", "wheel"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name="pylette-windows"
-version="1.0.0"
+version="2.0.0"
 description="Pylette for Windows"
 readme="README.md"
 authors=[{ name = "Austin Bryant", email = "c00481025@louisiana.edu" }]
 license={ file = "LICENSE.md" }
 classifiers=[
     "License :: OSI Approved :: MIT License",
     "Programming Language :: Python",
     "Programming Language :: Python :: 3",
 ]
 keywords=["palette", "color", "image"]
 dependencies=[
-    "numpy>=1.25.1",
+    "numpy==1.24.3",
     "Pillow>=10.0.0",
     "PyQt5>=5.15.9",
     "scikit-learn>=1.3.0"
 ]
 requires-python=">=3.11.4"
 
 [project.urls]
```

### Comparing `pylette-windows-1.0.0/src/Pylette/auxiliary.py` & `pylette-windows-2.0.0/src/Pylette/auxiliary.py`

 * *Files identical despite different names*

### Comparing `pylette-windows-1.0.0/src/Pylette/cmd.py` & `pylette-windows-2.0.0/src/Pylette/cmd.py`

 * *Files identical despite different names*

### Comparing `pylette-windows-1.0.0/src/Pylette/color.py` & `pylette-windows-2.0.0/src/Pylette/color.py`

 * *Files identical despite different names*

### Comparing `pylette-windows-1.0.0/src/Pylette/color_extraction.py` & `pylette-windows-2.0.0/src/Pylette/color_extraction.py`

 * *Files identical despite different names*

### Comparing `pylette-windows-1.0.0/src/Pylette/gui.py` & `pylette-windows-2.0.0/src/Pylette/gui.py`

 * *Files identical despite different names*

### Comparing `pylette-windows-1.0.0/src/Pylette/palette.py` & `pylette-windows-2.0.0/src/Pylette/palette.py`

 * *Files identical despite different names*

### Comparing `pylette-windows-1.0.0/src/pylette_windows.egg-info/PKG-INFO` & `pylette-windows-2.0.0/src/pylette_windows.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pylette-windows
-Version: 1.0.0
+Version: 2.0.0
 Summary: Pylette for Windows
 Author-email: Austin Bryant <c00481025@louisiana.edu>
 License: MIT License
         
         Copyright (c) [2018] [Ivar Stangeby]
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
```

