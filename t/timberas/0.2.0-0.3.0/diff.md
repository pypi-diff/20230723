# Comparing `tmp/timberas-0.2.0.tar.gz` & `tmp/timberas-0.3.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "timberas-0.2.0.tar", last modified: Tue Jul 18 11:25:49 2023, max compression
+gzip compressed data, was "timberas-0.3.0.tar", last modified: Sun Jul 23 12:49:21 2023, max compression
```

## Comparing `timberas-0.2.0.tar` & `timberas-0.3.0.tar`

### file list

```diff
@@ -1,44 +1,50 @@
-drwxrwxrwx   0        0        0        0 2023-07-18 11:25:49.850557 timberas-0.2.0/
--rw-rw-rw-   0        0        0     1089 2023-07-18 03:18:28.000000 timberas-0.2.0/LICENSE.md
--rw-rw-rw-   0        0        0      157 2023-06-25 23:26:46.000000 timberas-0.2.0/MANIFEST.in
--rw-rw-rw-   0        0        0     3186 2023-07-18 11:25:49.848556 timberas-0.2.0/PKG-INFO
--rw-rw-rw-   0        0        0     2592 2023-07-18 03:18:28.000000 timberas-0.2.0/README.md
-drwxrwxrwx   0        0        0        0 2023-07-18 11:25:49.726568 timberas-0.2.0/docs/
--rw-rw-rw-   0        0        0        0 2023-06-25 23:26:46.000000 timberas-0.2.0/docs/how-to-guides.md
--rw-rw-rw-   0        0        0     1838 2023-07-18 03:18:28.000000 timberas-0.2.0/docs/index.md
--rw-rw-rw-   0        0        0      868 2023-07-18 03:18:28.000000 timberas-0.2.0/docs/install.md
--rw-rw-rw-   0        0        0      153 2023-06-29 00:29:21.000000 timberas-0.2.0/docs/reference.md
--rw-rw-rw-   0        0        0     4094 2023-07-18 03:18:28.000000 timberas-0.2.0/docs/tutorial-1.md
--rw-rw-rw-   0        0        0       61 2023-07-18 03:18:28.000000 timberas-0.2.0/docs/tutorial-2.md
-drwxrwxrwx   0        0        0        0 2023-07-18 11:25:49.736557 timberas-0.2.0/examples/
--rw-rw-rw-   0        0        0     2541 2023-07-18 03:18:28.000000 timberas-0.2.0/examples/getting_started_1.py
--rw-rw-rw-   0        0        0     7516 2023-07-18 03:18:28.000000 timberas-0.2.0/examples/getting_started_2.py
--rw-rw-rw-   0        0        0      761 2023-07-18 11:25:20.000000 timberas-0.2.0/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-07-18 11:25:49.851557 timberas-0.2.0/setup.cfg
-drwxrwxrwx   0        0        0        0 2023-07-18 11:25:49.681556 timberas-0.2.0/src/
-drwxrwxrwx   0        0        0        0 2023-07-18 11:25:49.762556 timberas-0.2.0/src/timberas/
--rw-rw-rw-   0        0        0     7193 2023-07-18 03:18:28.000000 timberas-0.2.0/src/timberas/AS1684_dicts.py
--rw-rw-rw-   0        0        0       35 2023-06-25 23:26:46.000000 timberas-0.2.0/src/timberas/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-18 11:25:49.816556 timberas-0.2.0/src/timberas/__pycache__/
--rw-rw-rw-   0        0        0     5639 2023-06-26 00:58:42.000000 timberas-0.2.0/src/timberas/__pycache__/AS1684_dicts.cpython-310.pyc
--rw-rw-rw-   0        0        0      201 2023-06-26 00:56:57.000000 timberas-0.2.0/src/timberas/__pycache__/__init__.cpython-310.pyc
--rw-rw-rw-   0        0        0     8771 2023-07-18 01:01:57.000000 timberas-0.2.0/src/timberas/__pycache__/geometry.cpython-310.pyc
--rw-rw-rw-   0        0        0     7827 2023-07-18 00:52:28.000000 timberas-0.2.0/src/timberas/__pycache__/material.cpython-310.pyc
--rw-rw-rw-   0        0        0    13992 2023-06-29 04:32:12.000000 timberas-0.2.0/src/timberas/__pycache__/member.cpython-310.pyc
-drwxrwxrwx   0        0        0        0 2023-07-18 11:25:49.831555 timberas-0.2.0/src/timberas/data/
--rw-rw-rw-   0        0        0        0 2023-06-25 23:26:46.000000 timberas-0.2.0/src/timberas/data/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-18 11:25:49.836555 timberas-0.2.0/src/timberas/data/__pycache__/
--rw-rw-rw-   0        0        0      167 2023-06-26 00:56:57.000000 timberas-0.2.0/src/timberas/data/__pycache__/__init__.cpython-310.pyc
--rw-rw-rw-   0        0        0     5292 2023-07-18 00:52:03.000000 timberas-0.2.0/src/timberas/data/material_library.csv
--rw-rw-rw-   0        0        0     3150 2023-07-18 03:18:28.000000 timberas-0.2.0/src/timberas/data/section_library.csv
--rw-rw-rw-   0        0        0     8729 2023-07-18 11:02:27.000000 timberas-0.2.0/src/timberas/geometry.py
--rw-rw-rw-   0        0        0     8289 2023-07-18 11:01:35.000000 timberas-0.2.0/src/timberas/material.py
--rw-rw-rw-   0        0        0    15502 2023-07-18 00:52:03.000000 timberas-0.2.0/src/timberas/member.py
-drwxrwxrwx   0        0        0        0 2023-07-18 11:25:49.789555 timberas-0.2.0/src/timberas.egg-info/
--rw-rw-rw-   0        0        0     3186 2023-07-18 11:25:49.000000 timberas-0.2.0/src/timberas.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      959 2023-07-18 11:25:49.000000 timberas-0.2.0/src/timberas.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-18 11:25:49.000000 timberas-0.2.0/src/timberas.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       28 2023-07-18 11:25:49.000000 timberas-0.2.0/src/timberas.egg-info/requires.txt
--rw-rw-rw-   0        0        0        9 2023-07-18 11:25:49.000000 timberas-0.2.0/src/timberas.egg-info/top_level.txt
-drwxrwxrwx   0        0        0        0 2023-07-18 11:25:49.842556 timberas-0.2.0/tests/
--rw-rw-rw-   0        0        0     4357 2023-07-18 03:18:28.000000 timberas-0.2.0/tests/test_materials.py
+drwxrwxrwx   0        0        0        0 2023-07-23 12:49:21.789828 timberas-0.3.0/
+-rw-rw-rw-   0        0        0     1089 2023-07-23 12:48:14.000000 timberas-0.3.0/LICENSE.md
+-rw-rw-rw-   0        0        0      157 2023-06-25 23:26:46.000000 timberas-0.3.0/MANIFEST.in
+-rw-rw-rw-   0        0        0     3187 2023-07-23 12:49:21.787827 timberas-0.3.0/PKG-INFO
+-rw-rw-rw-   0        0        0     2593 2023-07-19 00:20:55.000000 timberas-0.3.0/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 12:49:21.603819 timberas-0.3.0/docs/
+-rw-rw-rw-   0        0        0        0 2023-06-25 23:26:46.000000 timberas-0.3.0/docs/how-to-guides.md
+-rw-rw-rw-   0        0        0     1902 2023-07-23 12:48:14.000000 timberas-0.3.0/docs/index.md
+-rw-rw-rw-   0        0        0      868 2023-07-18 03:18:28.000000 timberas-0.3.0/docs/install.md
+-rw-rw-rw-   0        0        0      153 2023-06-29 00:29:21.000000 timberas-0.3.0/docs/reference.md
+-rw-rw-rw-   0        0        0     1100 2023-07-23 12:48:14.000000 timberas-0.3.0/docs/tutorial-1.md
+-rw-rw-rw-   0        0        0     6236 2023-07-23 12:48:14.000000 timberas-0.3.0/docs/tutorial-2.md
+-rw-rw-rw-   0        0        0    11430 2023-07-23 12:48:14.000000 timberas-0.3.0/docs/tutorial-3.md
+-rw-rw-rw-   0        0        0     6534 2023-07-23 12:48:14.000000 timberas-0.3.0/docs/tutorial-4.md
+drwxrwxrwx   0        0        0        0 2023-07-23 12:49:21.622825 timberas-0.3.0/examples/
+-rw-rw-rw-   0        0        0      452 2023-07-23 12:48:14.000000 timberas-0.3.0/examples/tutorial_1.py
+-rw-rw-rw-   0        0        0     3430 2023-07-23 12:48:14.000000 timberas-0.3.0/examples/tutorial_2.py
+-rw-rw-rw-   0        0        0     3696 2023-07-23 12:48:14.000000 timberas-0.3.0/examples/tutorial_3.py
+-rw-rw-rw-   0        0        0     2200 2023-07-23 12:48:14.000000 timberas-0.3.0/examples/tutorial_4.py
+-rw-rw-rw-   0        0        0      761 2023-07-23 12:48:14.000000 timberas-0.3.0/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-07-23 12:49:21.790827 timberas-0.3.0/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-07-23 12:49:21.545820 timberas-0.3.0/src/
+drwxrwxrwx   0        0        0        0 2023-07-23 12:49:21.654821 timberas-0.3.0/src/timberas/
+-rw-rw-rw-   0        0        0     7193 2023-07-18 03:18:28.000000 timberas-0.3.0/src/timberas/AS1684_dicts.py
+-rw-rw-rw-   0        0        0       35 2023-06-25 23:26:46.000000 timberas-0.3.0/src/timberas/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 12:49:21.754826 timberas-0.3.0/src/timberas/__pycache__/
+-rw-rw-rw-   0        0        0     5639 2023-06-26 00:58:42.000000 timberas-0.3.0/src/timberas/__pycache__/AS1684_dicts.cpython-310.pyc
+-rw-rw-rw-   0        0        0      201 2023-06-26 00:56:57.000000 timberas-0.3.0/src/timberas/__pycache__/__init__.cpython-310.pyc
+-rw-rw-rw-   0        0        0     8756 2023-07-23 12:48:30.000000 timberas-0.3.0/src/timberas/__pycache__/geometry.cpython-310.pyc
+-rw-rw-rw-   0        0        0     7838 2023-07-23 12:48:32.000000 timberas-0.3.0/src/timberas/__pycache__/material.cpython-310.pyc
+-rw-rw-rw-   0        0        0    17641 2023-07-23 12:48:32.000000 timberas-0.3.0/src/timberas/__pycache__/member.cpython-310.pyc
+-rw-rw-rw-   0        0        0      689 2023-07-23 12:48:32.000000 timberas-0.3.0/src/timberas/__pycache__/utils.cpython-310.pyc
+drwxrwxrwx   0        0        0        0 2023-07-23 12:49:21.770829 timberas-0.3.0/src/timberas/data/
+-rw-rw-rw-   0        0        0        0 2023-06-25 23:26:46.000000 timberas-0.3.0/src/timberas/data/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 12:49:21.776828 timberas-0.3.0/src/timberas/data/__pycache__/
+-rw-rw-rw-   0        0        0      167 2023-06-26 00:56:57.000000 timberas-0.3.0/src/timberas/data/__pycache__/__init__.cpython-310.pyc
+-rw-rw-rw-   0        0        0     5292 2023-07-18 00:52:03.000000 timberas-0.3.0/src/timberas/data/material_library.csv
+-rw-rw-rw-   0        0        0     3150 2023-07-18 03:18:28.000000 timberas-0.3.0/src/timberas/data/section_library.csv
+-rw-rw-rw-   0        0        0     8735 2023-07-23 12:48:14.000000 timberas-0.3.0/src/timberas/geometry.py
+-rw-rw-rw-   0        0        0     8282 2023-07-23 12:48:14.000000 timberas-0.3.0/src/timberas/material.py
+-rw-rw-rw-   0        0        0    21231 2023-07-23 12:48:14.000000 timberas-0.3.0/src/timberas/member.py
+-rw-rw-rw-   0        0        0      730 2023-07-23 12:48:14.000000 timberas-0.3.0/src/timberas/utils.py
+drwxrwxrwx   0        0        0        0 2023-07-23 12:49:21.708824 timberas-0.3.0/src/timberas.egg-info/
+-rw-rw-rw-   0        0        0     3187 2023-07-23 12:49:21.000000 timberas-0.3.0/src/timberas.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0     1098 2023-07-23 12:49:21.000000 timberas-0.3.0/src/timberas.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 12:49:21.000000 timberas-0.3.0/src/timberas.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       28 2023-07-23 12:49:21.000000 timberas-0.3.0/src/timberas.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        9 2023-07-23 12:49:21.000000 timberas-0.3.0/src/timberas.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 12:49:21.781825 timberas-0.3.0/tests/
+-rw-rw-rw-   0        0        0     4357 2023-07-18 03:18:28.000000 timberas-0.3.0/tests/test_materials.py
```

### Comparing `timberas-0.2.0/LICENSE.md` & `timberas-0.3.0/LICENSE.md`

 * *Files 9% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 MIT License
 
-Copyright (c) 2023 Joseph Gatras
+Copyright (c) 2023 Joseph Gattas
 
 Permission is hereby granted, free of charge, to any person obtaining a copy
 of this software and associated documentation files (the "Software"), to deal
 in the Software without restriction, including without limitation the rights
 to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
 copies of the Software, and to permit persons to whom the Software is
 furnished to do so, subject to the following conditions:
```

### Comparing `timberas-0.2.0/PKG-INFO` & `timberas-0.3.0/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: timberas
-Version: 0.2.0
+Version: 0.3.0
 Summary: timberas is a Python package for the design of timber structures to relevant Australian Standards
 Author-email: Joe Gattas <j.gattas@uq.edu.au>
 Project-URL: Homepage, https://github.com/Folded-Structures-Lab/timber-as
 Keywords: AS1170,AS1684,timber structures,structural engineering
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
@@ -12,15 +12,15 @@
 Description-Content-Type: text/markdown
 License-File: LICENSE.md
 
 # About
 *timberas* is a Python package with tools to support research and design of Australian timber structures. It can be used to determine the material properties, section properties, and design capacities for structural members as per Australian Standard AS1720.1:2020 (Timber Structures Part 1: Design Methods). 
 
 # Documentation
-Detailed information on *timberas* is available in package documentation at [timberas.readthedocs.io](https://timberas.readthedocs.io/). This includes project background, examples, and an API reference guide.
+Detailed information on *timberas* is available in package documentation at [timberas.readthedocs.io](https://timber-as.readthedocs.io/). This includes project background, examples, and an API reference guide.
 
 # Installation
 *timberas* can be installed from the Python Package index:
 ```
 pip install timberas
 ```
 For more detailed instructions, please refer to the [documentation]([https://timberas.readthedocs.io]).
```

### Comparing `timberas-0.2.0/README.md` & `timberas-0.3.0/README.md`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 # About
 *timberas* is a Python package with tools to support research and design of Australian timber structures. It can be used to determine the material properties, section properties, and design capacities for structural members as per Australian Standard AS1720.1:2020 (Timber Structures Part 1: Design Methods). 
 
 # Documentation
-Detailed information on *timberas* is available in package documentation at [timberas.readthedocs.io](https://timberas.readthedocs.io/). This includes project background, examples, and an API reference guide.
+Detailed information on *timberas* is available in package documentation at [timberas.readthedocs.io](https://timber-as.readthedocs.io/). This includes project background, examples, and an API reference guide.
 
 # Installation
 *timberas* can be installed from the Python Package index:
 ```
 pip install timberas
 ```
 For more detailed instructions, please refer to the [documentation]([https://timberas.readthedocs.io]).
```

### Comparing `timberas-0.2.0/docs/index.md` & `timberas-0.3.0/docs/index.md`

 * *Files 22% similar despite different names*

```diff
@@ -3,21 +3,23 @@
 *timberas* is a Python package developed to support research and design of Australian timber structures. It can be used to determine the section properties, materials properties, and design capacities for structural members as per Australian Standard AS1720.1:2020 (Timber Structures Part 1: Design Methods). 
 
 *timberas* is developed by [Dr Joe Gattas](https://researchers.uq.edu.au/researcher/9443)  and research collaborators at the [University of Queensland](https://civil.uq.edu.au/) and [ARC Advance Timber Hub](https://www.advance-timber-hub.org/). 
 
 # Contents
 - [Installation](install.md)
 - Tutorials
-    - [Getting Started I](tutorial-1.md): Create timber sections and materials
-    - [Getting Started II](tutorial-2.md) Create a timber member and solve member design capacities. 
+    - [Quick Start](tutorial-1.md)
+    - [Sections and Materials](tutorial-2.md)
+    - [Tension and Compression Capacity](tutorial-3.md) 
+    - [Bending and Shear Capacity](tutorial-4.md) 
 - [API Reference](reference.md)
 
 
 # Support
-Please see the project Github repository and README file for the latest updates and issues. 
+Please see the project [Github repository](https://github.com/Folded-Structures-Lab/timber-as) and README file for the latest updates and issues. 
 
 # License
 *timberas* is provided under an MIT License. Please refer to the project Github repository and LICENSE file for more information. 
 
 
 # Acknowledgements
 This package has been developed from research projects supported by the [University of Queensland](https://civil.uq.edu.au/) and [ARC Future Timber Hub](https://futuretimberhub.org/).
```

### Comparing `timberas-0.2.0/docs/install.md` & `timberas-0.3.0/docs/install.md`

 * *Files identical despite different names*

### Comparing `timberas-0.2.0/pyproject.toml` & `timberas-0.3.0/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "timberas"
-version = "0.2.0"
+version = "0.3.0"
 authors = [
   { name="Joe Gattas", email="j.gattas@uq.edu.au" },
 ]
 description = "timberas is a Python package for the design of timber structures to relevant Australian Standards"
 readme = "README.md"
 requires-python = ">=3.10"
 classifiers = [
```

### Comparing `timberas-0.2.0/src/timberas/AS1684_dicts.py` & `timberas-0.3.0/src/timberas/AS1684_dicts.py`

 * *Files identical despite different names*

### Comparing `timberas-0.2.0/src/timberas/__pycache__/AS1684_dicts.cpython-310.pyc` & `timberas-0.3.0/src/timberas/__pycache__/AS1684_dicts.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `timberas-0.2.0/src/timberas/__pycache__/geometry.cpython-310.pyc` & `timberas-0.3.0/src/timberas/__pycache__/geometry.cpython-310.pyc`

 * *Format-specific differences are supported for Python .pyc files but no file-specific differences were detected; falling back to a binary diff. file(1) reports: Byte-compiled Python module for CPython 3.10, timestamp-based, .py timestamp: Tue Jul 18 01:01:54 2023 UTC, .py size: 8746 bytes*

 * *Could not decompile bytecode: bad marshal data (unknown type code)*

 * *Files 14% similar despite different names*

```diff
@@ -1,549 +1,548 @@
-00000000: 6f0d 0d0a 0000 0000 82e4 b564 2a22 0000  o..........d*"..
+00000000: 6f0d 0d0a 0000 0000 8e21 bd64 1f22 0000  o........!.d."..
 00000010: e300 0000 0000 0000 0000 0000 0000 0000  ................
-00000020: 0005 0000 0040 0000 0173 aa00 0000 6400  .....@...s....d.
+00000020: 0005 0000 0040 0000 0173 a600 0000 6400  .....@...s....d.
 00000030: 5a00 6401 6402 6c01 6d02 5a02 0100 6401  Z.d.d.l.m.Z...d.
-00000040: 6403 6c03 6d04 5a04 0100 6401 6404 6c05  d.l.m.Z...d.d.l.
-00000050: 6d06 5a06 6d07 5a07 0100 6401 6405 6c08  m.Z.m.Z...d.d.l.
-00000060: 6d09 5a09 6d0a 5a0a 6d0b 5a0b 6d0c 5a0c  m.Z.m.Z.m.Z.m.Z.
-00000070: 0100 6401 6406 6c0d 6d0e 5a0e 6d0f 5a0f  ..d.d.l.m.Z.m.Z.
-00000080: 0100 6401 6407 6c10 5a11 4700 6408 6409  ..d.d.l.Z.G.d.d.
-00000090: 8400 6409 6512 650e 8304 5a13 6506 640a  ..d.e.e...Z.e.d.
-000000a0: 640b 8d01 4700 640c 640d 8400 640d 8302  d...G.d.d...d...
-000000b0: 8301 5a14 6414 6410 6411 8404 5a15 6506  ..Z.d.d.d...Z.e.
-000000c0: 4700 6412 6413 8400 6413 8302 8301 5a16  G.d.d...d.....Z.
-000000d0: 6516 5a17 6407 5300 2915 612d 0200 000a  e.Z.d.S.).a-....
-000000e0: 5468 6973 206d 6f64 756c 6520 7072 6f76  This module prov
-000000f0: 6964 6573 2063 6c61 7373 6573 2061 6e64  ides classes and
-00000100: 2066 756e 6374 696f 6e73 2074 6f20 6d61   functions to ma
-00000110: 6e61 6765 2074 696d 6265 7220 7365 6374  nage timber sect
-00000120: 696f 6e73 2061 6e64 2074 6865 6972 2067  ions and their g
-00000130: 656f 6d65 7472 6963 2070 726f 7065 7274  eometric propert
-00000140: 6965 732e 0a0a 436c 6173 7365 733a 2020  ies...Classes:  
-00000150: 2020 0a20 2020 2053 6861 7065 5479 7065    .    ShapeType
-00000160: 3a20 456e 756d 2063 6c61 7373 2064 6566  : Enum class def
-00000170: 696e 696e 6720 7365 6374 696f 6e20 7479  ining section ty
-00000180: 7065 2073 7472 696e 6720 636f 6e73 7461  pe string consta
-00000190: 6e74 732e 200a 0a20 2020 2054 696d 6265  nts. ..    Timbe
-000001a0: 7253 6563 7469 6f6e 3a20 4120 636c 6173  rSection: A clas
-000001b0: 7320 6973 2075 7365 6420 746f 206d 616e  s is used to man
-000001c0: 6167 6520 7469 6d62 6572 2073 6563 7469  age timber secti
-000001d0: 6f6e 2061 7474 7269 6275 7465 732e 200a  on attributes. .
-000001e0: 0a20 2020 2052 6563 7461 6e67 6c65 5368  .    RectangleSh
-000001f0: 6170 653a 2052 6570 7265 7365 6e74 7320  ape: Represents 
-00000200: 7374 7275 6374 7572 616c 2073 6563 7469  structural secti
-00000210: 6f6e 2070 726f 7065 7274 6965 7320 666f  on properties fo
-00000220: 7220 6120 7265 6374 616e 6775 6c61 7220  r a rectangular 
-00000230: 6372 6f73 732d 7365 6374 696f 6e2e 200a  cross-section. .
-00000240: 0a20 2020 2054 696d 6265 7253 6861 7065  .    TimberShape
-00000250: 3a20 416e 2061 6c69 6173 2066 6f72 2074  : An alias for t
-00000260: 6865 2052 6563 7461 6e67 6c65 5368 6170  he RectangleShap
-00000270: 6520 636c 6173 732e 0a20 2020 200a 4675  e class..    .Fu
-00000280: 6e63 7469 6f6e 733a 0a20 2020 2069 6d70  nctions:.    imp
-00000290: 6f72 745f 7365 6374 696f 6e5f 6c69 6272  ort_section_libr
-000002a0: 6172 7928 293a 2052 6574 7572 6e73 2061  ary(): Returns a
-000002b0: 2044 6174 6146 7261 6d65 2063 6f6e 7461   DataFrame conta
-000002c0: 696e 696e 6720 7468 6520 7365 6374 696f  ining the sectio
-000002d0: 6e20 6c69 6272 6172 7920 6465 6669 6e65  n library define
-000002e0: 640a 2020 2020 696e 2074 696d 6265 7261  d.    in timbera
-000002f0: 732f 6461 7461 2f73 6563 7469 6f6e 5f6c  s/data/section_l
-00000300: 6962 7261 7279 2e63 7376 0a0a e900 0000  ibrary.csv......
-00000310: 0029 01da 0b61 6e6e 6f74 6174 696f 6e73  .)...annotations
-00000320: 2901 da05 6669 6c65 7329 02da 0964 6174  )...files)...dat
-00000330: 6163 6c61 7373 da05 6669 656c 6429 04da  aclass..field)..
-00000340: 036e 616e da05 6973 6e61 6eda 0566 6c6f  .nan..isnan..flo
-00000350: 6f72 da05 6c6f 6731 3029 02da 0445 6e75  or..log10)...Enu
-00000360: 6dda 0461 7574 6f4e 6300 0000 0000 0000  m..autoNc.......
-00000370: 0000 0000 0000 0000 0001 0000 0040 0000  .............@..
-00000380: 0173 1c00 0000 6500 5a01 6400 5a02 6401  .s....e.Z.d.Z.d.
-00000390: 5a03 6402 5a04 6403 5a05 6404 5a06 6405  Z.d.Z.d.Z.d.Z.d.
-000003a0: 5300 2906 da09 5368 6170 6554 7970 6561  S.)...ShapeTypea
-000003b0: 7c01 0000 0a20 2020 2041 6e20 656e 756d  |....    An enum
-000003c0: 6572 6174 696f 6e20 6f66 2073 6563 7469  eration of secti
-000003d0: 6f6e 2074 7970 6520 7374 7269 6e67 2063  on type string c
-000003e0: 6f6e 7374 616e 7473 2e20 5072 6f76 6964  onstants. Provid
-000003f0: 6573 2061 2074 7970 652d 7361 6665 2077  es a type-safe w
-00000400: 6179 206f 6620 7265 7072 6573 656e 7469  ay of representi
-00000410: 6e67 0a20 2020 2064 6966 6665 7265 6e74  ng.    different
-00000420: 2073 6563 7469 6f6e 2074 7970 6573 2e0a   section types..
-00000430: 0a20 2020 2041 7474 7269 6275 7465 733a  .    Attributes:
-00000440: 0a20 2020 2020 2020 2053 494e 474c 455f  .        SINGLE_
-00000450: 424f 4152 4420 2873 7472 293a 2052 6570  BOARD (str): Rep
-00000460: 7265 7365 6e74 7320 6120 7365 6374 696f  resents a sectio
-00000470: 6e20 636f 6d70 6f73 6564 206f 6620 6120  n composed of a 
-00000480: 7369 6e67 6c65 2062 6f61 7264 2c20 652e  single board, e.
-00000490: 672e 2039 3078 3335 0a20 2020 2020 2020  g. 90x35.       
-000004a0: 204d 554c 5449 5f42 4f41 5244 2028 7374   MULTI_BOARD (st
-000004b0: 7229 3a20 5265 7072 6573 656e 7473 2061  r): Represents a
-000004c0: 2073 6563 7469 6f6e 2063 6f6d 706f 7365   section compose
-000004d0: 6420 6f66 206d 756c 7469 706c 6520 626f  d of multiple bo
-000004e0: 6172 6473 2c20 652e 672e 2032 2f39 3078  ards, e.g. 2/90x
-000004f0: 3335 0a20 2020 2020 2020 2052 4f55 4e44  35.        ROUND
-00000500: 2028 7374 7229 3a20 5265 7072 6573 656e   (str): Represen
-00000510: 7473 2061 2072 6f75 6e64 2073 6563 7469  ts a round secti
-00000520: 6f6e 2028 756e 7573 6564 290a 2020 2020  on (unused).    
-00000530: 5a0c 7369 6e67 6c65 5f62 6f61 7264 5a0b  Z.single_boardZ.
-00000540: 6d75 6c74 695f 626f 6172 64da 0572 6f75  multi_board..rou
-00000550: 6e64 4e29 07da 085f 5f6e 616d 655f 5fda  ndN)...__name__.
-00000560: 0a5f 5f6d 6f64 756c 655f 5fda 0c5f 5f71  .__module__..__q
-00000570: 7561 6c6e 616d 655f 5fda 075f 5f64 6f63  ualname__..__doc
-00000580: 5f5f da0c 5349 4e47 4c45 5f42 4f41 5244  __..SINGLE_BOARD
-00000590: da0b 4d55 4c54 495f 424f 4152 445a 0552  ..MULTI_BOARDZ.R
-000005a0: 4f55 4e44 a900 7214 0000 0072 1400 0000  OUND..r....r....
-000005b0: fa45 633a 5c75 7365 7273 5c75 716a 6761  .Ec:\users\uqjga
-000005c0: 7474 615c 646f 6375 6d65 6e74 735c 6769  tta\documents\gi
-000005d0: 7468 7562 5c74 696d 6265 722d 6173 5c73  thub\timber-as\s
-000005e0: 7263 5c74 696d 6265 7261 735c 6765 6f6d  rc\timberas\geom
-000005f0: 6574 7279 2e70 7972 0c00 0000 1c00 0000  etry.pyr........
-00000600: 730a 0000 0008 0004 0104 0b04 0108 0172  s..............r
-00000610: 0c00 0000 5429 015a 076b 775f 6f6e 6c79  ....T).Z.kw_only
-00000620: 6300 0000 0000 0000 0000 0000 0000 0000  c...............
-00000630: 0005 0000 0040 0000 0173 0c01 0000 6500  .....@...s....e.
-00000640: 5a01 6400 5a02 5500 6401 5a03 6402 6504  Z.d.Z.U.d.Z.d.e.
-00000650: 6403 3c00 6404 6504 6405 3c00 6404 6504  d.<.d.e.d.<.d.e.
-00000660: 6406 3c00 6407 5a05 6408 6504 6409 3c00  d.<.d.Z.d.e.d.<.
-00000670: 640a 5a06 640b 6504 640c 3c00 6507 5a08  d.Z.d.e.d.<.e.Z.
-00000680: 6404 6504 640d 3c00 6507 5a09 6404 6504  d.e.d.<.e.Z.d.e.
-00000690: 640e 3c00 6507 5a0a 6404 6504 640f 3c00  d.<.e.Z.d.e.d.<.
-000006a0: 6507 5a0b 6404 6504 6410 3c00 6507 5a0c  e.Z.d.e.d.<.e.Z.
-000006b0: 6404 6504 6411 3c00 650d 6412 6413 8d01  d.e.d.<.e.d.d...
-000006c0: 5a0e 6414 6504 6415 3c00 650d 6412 6416  Z.d.e.d.<.e.d.d.
-000006d0: 6417 8d02 5a0f 6408 6504 6418 3c00 6419  d...Z.d.e.d.<.d.
-000006e0: 641a 8400 5a10 641b 641c 8400 5a11 6512  d...Z.d.d...Z.e.
-000006f0: 6432 6433 6423 6424 8405 8301 5a13 6512  d2d3d#d$....Z.e.
-00000700: 6434 6435 6428 6429 8405 8301 5a14 6515  d4d5d(d)....Z.e.
-00000710: 6436 642a 642b 8404 8301 5a16 6515 6436  d6d*d+....Z.e.d6
-00000720: 642c 642d 8404 8301 5a17 6515 6436 642e  d,d-....Z.e.d6d.
-00000730: 642f 8404 8301 5a18 6515 6436 6430 6431  d/....Z.e.d6d0d1
-00000740: 8404 8301 5a19 6425 5300 2937 da0d 5469  ....Z.d%S.)7..Ti
-00000750: 6d62 6572 5365 6374 696f 6e61 ed04 0000  mberSectiona....
-00000760: 0a20 2020 2043 616c 6375 6c61 7465 7320  .    Calculates 
-00000770: 6765 6f6d 6574 7269 6320 616e 6420 7374  geometric and st
-00000780: 7275 6374 7572 616c 2073 6563 7469 6f6e  ructural section
-00000790: 2070 726f 7065 7274 6965 7320 6672 6f6d   properties from
-000007a0: 2063 726f 7373 2d73 6563 7469 6f6e 2070   cross-section p
-000007b0: 6172 616d 6574 6572 732e 2053 656c 6563  arameters. Selec
-000007c0: 7473 0a20 2020 2073 6861 7065 2063 6c61  ts.    shape cla
-000007d0: 7373 2066 726f 6d20 7368 6170 655f 7479  ss from shape_ty
-000007e0: 7065 2074 6f20 6361 6c63 756c 6174 653a  pe to calculate:
-000007f0: 2041 5f67 2c20 415f 742c 2041 5f63 2c20   A_g, A_t, A_c, 
-00000800: 495f 782c 2049 5f79 2e20 436c 6173 7320  I_x, I_y. Class 
-00000810: 7072 6f70 6572 7469 6573 205a 5f78 2c20  properties Z_x, 
-00000820: 5a5f 792c 0a20 2020 2062 5f74 6f74 2c20  Z_y,.    b_tot, 
-00000830: 616e 6420 415f 7320 6361 6c63 756c 6174  and A_s calculat
-00000840: 6564 2061 7320 6465 7269 7665 6420 6174  ed as derived at
-00000850: 7472 6962 7574 6573 2e0a 0a20 2020 2041  tributes...    A
-00000860: 7474 7269 6275 7465 733a 0a20 2020 2020  ttributes:.     
-00000870: 2020 2073 6861 7065 5f74 7970 6520 2853     shape_type (S
-00000880: 6861 7065 5479 7065 207c 2073 7472 293a  hapeType | str):
-00000890: 2054 6865 2074 7970 6520 6f66 2074 6865   The type of the
-000008a0: 2073 6563 7469 6f6e 2073 6861 7065 2e0a   section shape..
-000008b0: 0a20 2020 2020 2020 2062 2028 666c 6f61  .        b (floa
-000008c0: 7429 3a20 5468 6520 6272 6561 6474 6820  t): The breadth 
-000008d0: 6f66 2074 6865 2073 6563 7469 6f6e 2e0a  of the section..
-000008e0: 2020 2020 2020 2020 6420 2866 6c6f 6174          d (float
-000008f0: 293a 2054 6865 2064 6570 7468 206f 6620  ): The depth of 
-00000900: 7468 6520 7365 6374 696f 6e2e 0a20 2020  the section..   
-00000910: 2020 2020 206e 2028 696e 742c 206f 7074       n (int, opt
-00000920: 696f 6e61 6c29 3a20 5468 6520 6e75 6d62  ional): The numb
-00000930: 6572 206f 6620 6d65 6d62 6572 7320 696e  er of members in
-00000940: 2074 6865 2073 6563 7469 6f6e 2e20 4465   the section. De
-00000950: 6661 756c 7420 3d20 312e 0a20 2020 2020  fault = 1..     
-00000960: 2020 206e 616d 6520 2873 7472 2c20 6f70     name (str, op
-00000970: 7469 6f6e 616c 293a 2054 6865 206e 616d  tional): The nam
-00000980: 6520 6f66 2074 6865 2073 6563 7469 6f6e  e of the section
-00000990: 2e20 4465 6661 756c 7473 2074 6f20 616e  . Defaults to an
-000009a0: 2065 6d70 7479 2073 7472 696e 672e 0a20   empty string.. 
-000009b0: 2020 2020 2020 2073 6861 7065 2028 5469         shape (Ti
-000009c0: 6d62 6572 5368 6170 6529 3a20 5468 6520  mberShape): The 
-000009d0: 7368 6170 6520 6f66 2074 6865 2073 6563  shape of the sec
-000009e0: 7469 6f6e 2c20 6361 6c63 756c 6174 6564  tion, calculated
-000009f0: 2061 6674 6572 2069 6e69 7469 616c 697a   after initializ
-00000a00: 6174 696f 6e2e 0a20 2020 2020 2020 2041  ation..        A
-00000a10: 5f67 2028 666c 6f61 7429 3a20 5468 6520  _g (float): The 
-00000a20: 6772 6f73 7320 6172 6561 206f 6620 7468  gross area of th
-00000a30: 6520 7365 6374 696f 6e2c 2063 616c 6375  e section, calcu
-00000a40: 6c61 7465 6420 6166 7465 7220 7368 6170  lated after shap
-00000a50: 6520 6973 2073 6f6c 7665 642e 0a20 2020  e is solved..   
-00000a60: 2020 2020 2041 5f74 2028 666c 6f61 7429       A_t (float)
-00000a70: 3a20 5468 6520 7465 6e73 696c 6520 6172  : The tensile ar
-00000a80: 6561 206f 6620 7468 6520 7365 6374 696f  ea of the sectio
-00000a90: 6e2c 2063 616c 6375 6c61 7465 6420 6166  n, calculated af
-00000aa0: 7465 7220 7368 6170 6520 6973 2073 6f6c  ter shape is sol
-00000ab0: 7665 642e 0a20 2020 2020 2020 2041 5f63  ved..        A_c
-00000ac0: 2028 666c 6f61 7429 3a20 5468 6520 636f   (float): The co
-00000ad0: 6d70 7265 7373 6976 6520 6172 6561 206f  mpressive area o
-00000ae0: 6620 7468 6520 7365 6374 696f 6e2c 2063  f the section, c
-00000af0: 616c 6375 6c61 7465 6420 6166 7465 7220  alculated after 
-00000b00: 7368 6170 6520 6973 2073 6f6c 7665 642e  shape is solved.
-00000b10: 0a20 2020 2020 2020 2049 5f78 2028 666c  .        I_x (fl
-00000b20: 6f61 7429 3a20 5468 6520 6d6f 6d65 6e74  oat): The moment
-00000b30: 206f 6620 696e 6572 7469 6120 6162 6f75   of inertia abou
-00000b40: 7420 7468 6520 782d 6178 6973 2c20 6361  t the x-axis, ca
-00000b50: 6c63 756c 6174 6564 2061 6674 6572 2073  lculated after s
-00000b60: 6861 7065 2069 7320 736f 6c76 6564 2e0a  hape is solved..
-00000b70: 2020 2020 2020 2020 495f 7920 2866 6c6f          I_y (flo
-00000b80: 6174 293a 2054 6865 206d 6f6d 656e 7420  at): The moment 
-00000b90: 6f66 2069 6e65 7274 6961 2061 626f 7574  of inertia about
-00000ba0: 2074 6865 2079 2d61 7869 732c 2063 616c   the y-axis, cal
-00000bb0: 6375 6c61 7465 6420 6279 2073 6861 7065  culated by shape
-00000bc0: 2069 6620 6e6f 7420 7072 6f76 6964 6564   if not provided
-00000bd0: 2e0a 2020 2020 2020 2020 7369 675f 6669  ..        sig_fi
-00000be0: 6773 2028 696e 742c 206f 7074 696f 6e61  gs (int, optiona
-00000bf0: 6c29 3a20 4e75 6d62 6572 206f 6620 7369  l): Number of si
-00000c00: 676e 6966 6963 616e 7420 6669 6775 7265  gnificant figure
-00000c10: 7320 746f 2072 6f75 6e64 2063 616c 6163  s to round calac
-00000c20: 756c 6174 6564 2076 616c 7565 7320 746f  ulated values to
-00000c30: 2e0a 2020 2020 2020 2020 4465 6661 756c  ..        Defaul
-00000c40: 7473 2074 6f20 342e 0a20 2020 207a 0f53  ts to 4..    z.S
-00000c50: 6861 7065 5479 7065 207c 2073 7472 da0a  hapeType | str..
-00000c60: 7368 6170 655f 7479 7065 da05 666c 6f61  shape_type..floa
-00000c70: 74da 0162 da01 64e9 0100 0000 da03 696e  t..b..d.......in
-00000c80: 74da 016e da00 da03 7374 72da 046e 616d  t..n....str..nam
-00000c90: 65da 0341 5f67 da03 415f 74da 0341 5f63  e..A_g..A_t..A_c
-00000ca0: da03 495f 78da 0349 5f79 4629 015a 0469  ..I_x..I_yF).Z.i
-00000cb0: 6e69 74da 0b54 696d 6265 7253 6861 7065  nit..TimberShape
-00000cc0: da05 7368 6170 65e9 0400 0000 2902 da04  ..shape.....)...
-00000cd0: 7265 7072 da07 6465 6661 756c 74da 0873  repr..default..s
-00000ce0: 6967 5f66 6967 7363 0100 0000 0000 0000  ig_figsc........
-00000cf0: 0000 0000 0100 0000 0200 0000 4300 0001  ............C...
-00000d00: 730c 0000 007c 00a0 00a1 0001 0064 0053  s....|.......d.S
-00000d10: 00a9 014e 2901 da0b 736f 6c76 655f 7368  ...N)...solve_sh
-00000d20: 6170 65a9 01da 0473 656c 6672 1400 0000  ape....selfr....
-00000d30: 7214 0000 0072 1500 0000 da0d 5f5f 706f  r....r......__po
-00000d40: 7374 5f69 6e69 745f 5f57 0000 0073 0200  st_init__W...s..
-00000d50: 0000 0c01 7a1b 5469 6d62 6572 5365 6374  ....z.TimberSect
-00000d60: 696f 6e2e 5f5f 706f 7374 5f69 6e69 745f  ion.__post_init_
-00000d70: 5f63 0100 0000 0000 0000 0000 0000 0300  _c..............
-00000d80: 0000 0c00 0000 4300 0001 730c 0100 007c  ......C...s....|
-00000d90: 006a 0074 016a 0274 016a 0366 0276 0072  .j.t.j.t.j.f.v.r
-00000da0: 1374 047c 006a 057c 006a 0664 018d 027c  .t.|.j.|.j.d...|
-00000db0: 005f 076e 0974 0864 027c 006a 009b 0064  ._.n.t.d.|.j...d
-00000dc0: 039d 0383 0182 017c 006a 0974 0a75 0072  .......|.j.t.u.r
-00000dd0: 267c 006a 076a 097c 005f 097c 006a 0b74  &|.j.j.|._.|.j.t
-00000de0: 0a75 0072 307c 006a 076a 097c 005f 0b7c  .u.r0|.j.j.|._.|
-00000df0: 006a 0c74 0a75 0072 3a7c 006a 076a 097c  .j.t.u.r:|.j.j.|
-00000e00: 005f 0c7c 006a 0d74 0a75 0072 447c 006a  ._.|.j.t.u.rD|.j
-00000e10: 076a 0d7c 005f 0d7c 006a 0e74 0a75 0072  .j.|._.|.j.t.u.r
-00000e20: 4e7c 006a 076a 0e7c 005f 0e7c 006a 0f72  N|.j.j.|._.|.j.r
-00000e30: 8274 107c 006a 11a0 12a1 0083 0144 005d  .t.|.j.......D.]
-00000e40: 2b5c 027d 017d 0274 137c 0274 1474 1566  +\.}.}.t.|.t.t.f
-00000e50: 0283 0272 8174 167c 0283 0173 817c 0264  ...r.t.|...s.|.d
-00000e60: 046b 0372 8174 177c 007c 0174 187c 027c  .k.r.t.|.|.t.|.|
-00000e70: 006a 0f74 1574 1974 1a74 1b7c 0283 0183  .j.t.t.t.t.|....
-00000e80: 0183 0183 0118 0064 0518 0083 0283 0301  .......d........
-00000e90: 0071 5864 0653 0064 0653 0029 077a 5253  .qXd.S.d.S.).zRS
-00000ea0: 6574 7320 7368 6170 6520 636c 6173 7320  ets shape class 
-00000eb0: 6261 7365 6420 6f6e 2073 6861 7065 5f74  based on shape_t
-00000ec0: 7970 6520 616e 6420 7265 6361 6c63 756c  ype and recalcul
-00000ed0: 6174 6573 2072 656c 6576 616e 7420 7365  ates relevant se
-00000ee0: 6374 696f 6e20 7072 6f70 6572 7469 6573  ction properties
-00000ef0: 2ea9 0272 1a00 0000 7219 0000 007a 0e73  ...r....r....z.s
-00000f00: 6563 7469 6f6e 2074 7970 653a 207a 1620  ection type: z. 
-00000f10: 6861 7320 6e6f 2073 6861 7065 2066 756e  has no shape fun
-00000f20: 6374 696f 6e72 0100 0000 721b 0000 004e  ctionr....r....N
-00000f30: 291c 7217 0000 0072 0c00 0000 7212 0000  ).r....r....r...
-00000f40: 0072 1300 0000 da0e 5265 6374 616e 676c  .r......Rectangl
-00000f50: 6553 6861 7065 721a 0000 00da 0562 5f74  eShaper......b_t
-00000f60: 6f74 7227 0000 00da 134e 6f74 496d 706c  otr'.....NotImpl
-00000f70: 656d 656e 7465 6445 7272 6f72 7221 0000  ementedErrorr!..
-00000f80: 0072 0600 0000 7222 0000 0072 2300 0000  .r....r"...r#...
-00000f90: 7224 0000 0072 2500 0000 722b 0000 00da  r$...r%...r+....
-00000fa0: 046c 6973 74da 085f 5f64 6963 745f 5fda  .list..__dict__.
-00000fb0: 0569 7465 6d73 da0a 6973 696e 7374 616e  .items..isinstan
-00000fc0: 6365 7218 0000 0072 1c00 0000 7207 0000  cer....r....r...
-00000fd0: 00da 0773 6574 6174 7472 720d 0000 0072  ...setattrr....r
-00000fe0: 0800 0000 7209 0000 00da 0361 6273 2903  ....r......abs).
-00000ff0: 722f 0000 00da 036b 6579 da03 7661 6c72  r/.....key..valr
-00001000: 1400 0000 7214 0000 0072 1500 0000 722d  ....r....r....r-
-00001010: 0000 005a 0000 0073 3400 0000 1202 1401  ...Z...s4.......
-00001020: 0202 0c01 04ff 0a04 0a01 0a01 0a01 0a01  ................
-00001030: 0a01 0a01 0a01 0a01 0a01 0603 1601 1e01  ................
-00001040: 0201 0201 0201 2201 04fd 0280 04fd 0401  ......".........
-00001050: 7a19 5469 6d62 6572 5365 6374 696f 6e2e  z.TimberSection.
-00001060: 736f 6c76 655f 7368 6170 6554 da0a 696e  solve_shapeT..in
-00001070: 7075 745f 6469 6374 da04 6469 6374 da08  put_dict..dict..
-00001080: 736f 6c76 655f 6d65 da04 626f 6f6c da06  solve_me..bool..
-00001090: 7265 7475 726e 6303 0000 0000 0000 0000  returnc.........
-000010a0: 0000 0005 0000 0004 0000 0003 0000 0173  ...............s
-000010b0: 3e00 0000 7c00 6a00 a001 a100 8900 8700  >...|.j.........
-000010c0: 6601 6401 6402 8408 7c01 a002 a100 4400  f.d.d...|.....D.
-000010d0: 8301 7d03 7c00 6404 6900 7c03 a401 8e01  ..}.|.d.i.|.....
-000010e0: 7d04 7c02 721d 7c04 a003 a100 0100 7c04  }.|.r.|.......|.
-000010f0: 5300 2905 61ed 0100 000a 2020 2020 2020  S.).a.....      
-00001100: 2020 4372 6561 7465 2061 2054 696d 6265    Create a Timbe
-00001110: 7253 6563 7469 6f6e 2062 7920 6469 7265  rSection by dire
-00001120: 6374 6c79 2070 6f70 756c 6174 696e 6720  ctly populating 
-00001130: 6174 7472 6962 7574 6573 2066 726f 6d20  attributes from 
-00001140: 696e 7075 7420 6469 6374 696f 6e61 7279  input dictionary
-00001150: 2c0a 2020 2020 2020 2020 6967 6e6f 7269  ,.        ignori
-00001160: 6e67 2064 6963 7469 6f6e 6172 7920 6b65  ng dictionary ke
-00001170: 7973 2077 6869 6368 2061 7265 6e27 7420  ys which aren't 
-00001180: 636c 6173 7320 6174 7472 6962 7574 6573  class attributes
-00001190: 2e0a 0a20 2020 2020 2020 2041 7267 733a  ...        Args:
-000011a0: 0a20 2020 2020 2020 2020 2020 2069 6e70  .            inp
-000011b0: 7574 5f64 6963 743a 2044 6566 696e 6573  ut_dict: Defines
-000011c0: 2074 696d 6265 7220 6d61 7465 7269 616c   timber material
-000011d0: 2064 6174 6120 746f 2062 6520 6164 6465   data to be adde
-000011e0: 642c 206b 6579 7320 636f 7272 6573 706f  d, keys correspo
-000011f0: 6e64 696e 6720 746f 2063 6c61 7373 0a20  nding to class. 
-00001200: 2020 2020 2020 2020 2020 2061 7474 7269             attri
-00001210: 6275 7465 206e 616d 6573 2077 696c 6c20  bute names will 
-00001220: 6265 2075 7064 6174 6564 2061 6e64 206f  be updated and o
-00001230: 7468 6572 7320 7769 6c6c 2062 6520 6967  thers will be ig
-00001240: 6e6f 7265 640a 2020 2020 2020 2020 2020  nored.          
-00001250: 2020 736f 6c76 655f 6d65 3a20 4966 2054    solve_me: If T
-00001260: 7275 6520 7769 6c6c 2072 756e 2073 6f6c  rue will run sol
-00001270: 7665 5f73 6861 7065 2829 2061 6674 6572  ve_shape() after
-00001280: 2061 7474 7269 6275 7465 7320 6172 6520   attributes are 
-00001290: 6164 6465 640a 0a20 2020 2020 2020 2052  added..        R
-000012a0: 6574 7572 6e73 3a0a 2020 2020 2020 2020  eturns:.        
-000012b0: 2020 2020 5469 6d62 6572 5365 6374 696f      TimberSectio
-000012c0: 6e3a 2054 6865 2074 696d 6265 7220 7365  n: The timber se
-000012d0: 6374 696f 6e20 6f62 6a65 6374 2e0a 2020  ction object..  
-000012e0: 2020 2020 2020 6301 0000 0000 0000 0000        c.........
-000012f0: 0000 0003 0000 0004 0000 0013 0000 0173  ...............s
-00001300: 1e00 0000 6900 7c00 5d0b 5c02 7d01 7d02  ....i.|.].\.}.}.
-00001310: 7c01 8800 7600 7202 7c01 7c02 9302 7102  |...v.r.|.|...q.
-00001320: 5300 7214 0000 0072 1400 0000 2903 da02  S.r....r....)...
-00001330: 2e30 da01 6bda 0176 a901 5a0a 7661 6c69  .0..k..v..Z.vali
-00001340: 645f 6b65 7973 7214 0000 0072 1500 0000  d_keysr....r....
-00001350: da0a 3c64 6963 7463 6f6d 703e 8a00 0000  ..<dictcomp>....
-00001360: 7302 0000 001e 007a 2b54 696d 6265 7253  s......z+TimberS
-00001370: 6563 7469 6f6e 2e66 726f 6d5f 6469 6374  ection.from_dict
-00001380: 2e3c 6c6f 6361 6c73 3e2e 3c64 6963 7463  .<locals>.<dictc
-00001390: 6f6d 703e 4e72 1400 0000 2904 da0f 5f5f  omp>Nr....)...__
-000013a0: 616e 6e6f 7461 7469 6f6e 735f 5fda 046b  annotations__..k
-000013b0: 6579 7372 3700 0000 722d 0000 0029 05da  eysr7...r-...)..
-000013c0: 0363 6c73 723d 0000 0072 3f00 0000 5a0a  .clsr=...r?...Z.
-000013d0: 7661 6c69 645f 6469 6374 5a07 6e65 775f  valid_dictZ.new_
-000013e0: 6f62 6a72 1400 0000 7245 0000 0072 1500  objr....rE...r..
-000013f0: 0000 da09 6672 6f6d 5f64 6963 7478 0000  ....from_dictx..
-00001400: 0073 0c00 0000 0a10 1602 0e02 0401 0801  .s..............
-00001410: 0401 7a17 5469 6d62 6572 5365 6374 696f  ..z.TimberSectio
-00001420: 6e2e 6672 6f6d 5f64 6963 744e da07 6c69  n.from_dictN..li
-00001430: 6272 6172 79fa 1370 642e 4461 7461 4672  brary..pd.DataFr
-00001440: 616d 6520 7c20 4e6f 6e65 6303 0000 0000  ame | Nonec.....
-00001450: 0000 0000 0000 0005 0000 0003 0000 0043  ...............C
-00001460: 0000 0173 3a00 0000 7c02 6401 7500 7207  ...s:...|.d.u.r.
-00001470: 7400 8300 7d02 7c02 6a01 7c02 6402 1900  t...}.|.j.|.d...
-00001480: 7c01 6b02 1900 7d03 7c03 6a02 6403 6404  |.k...}.|.j.d.d.
-00001490: 8d01 6405 1900 7d04 7c00 a003 7c04 a101  ..d...}.|...|...
-000014a0: 5300 2906 61c7 0100 0043 7265 6174 6573  S.).a....Creates
-000014b0: 2061 2054 696d 6265 7253 6563 7469 6f6e   a TimberSection
-000014c0: 206f 626a 6563 7420 6672 6f6d 2061 206d   object from a m
-000014d0: 6174 6572 6961 6c20 6c69 6272 6172 7920  aterial library 
-000014e0: 2844 6174 6146 7261 6d65 292e 0a0a 2020  (DataFrame)...  
-000014f0: 2020 2020 2020 4172 6773 3a0a 2020 2020        Args:.    
-00001500: 2020 2020 2020 2020 6e61 6d65 3a20 5468          name: Th
-00001510: 6520 6e61 6d65 206f 6620 7468 6520 7469  e name of the ti
-00001520: 6d62 6572 206d 6174 6572 6961 6c20 746f  mber material to
-00001530: 206c 6f6f 6b75 7020 696e 2074 6865 206c   lookup in the l
-00001540: 6962 7261 7279 2028 696e 2027 6e61 6d65  ibrary (in 'name
-00001550: 2720 636f 6c75 6d6e 290a 2020 2020 2020  ' column).      
-00001560: 2020 2020 2020 6c69 6272 6172 7920 2870        library (p
-00001570: 642e 4461 7461 4672 616d 652c 206f 7074  d.DataFrame, opt
-00001580: 696f 6e61 6c29 3a20 4461 7461 4672 616d  ional): DataFram
-00001590: 6520 636f 6e74 6169 6e69 6e67 2061 206c  e containing a l
-000015a0: 6962 7261 7279 206f 6620 7469 6d62 6572  ibrary of timber
-000015b0: 206d 6174 6572 6961 6c73 2e0a 2020 2020   materials..    
-000015c0: 2020 2020 2020 2020 2020 2020 4966 206e              If n
-000015d0: 6f74 2070 726f 7669 6465 642c 2074 6865  ot provided, the
-000015e0: 2064 6566 6175 6c74 2073 6563 7469 6f6e   default section
-000015f0: 206c 6962 7261 7279 2069 7320 7573 6564   library is used
-00001600: 2066 726f 6d20 696d 706f 7274 5f73 6563   from import_sec
-00001610: 7469 6f6e 5f6c 6962 7261 7279 2e0a 0a20  tion_library... 
-00001620: 2020 2020 2020 2052 6574 7572 6e73 3a0a         Returns:.
-00001630: 2020 2020 2020 2020 2020 2020 5469 6d62              Timb
-00001640: 6572 4d61 7465 7269 616c 3a20 5468 6520  erMaterial: The 
-00001650: 7469 6d62 6572 206d 6174 6572 6961 6c20  timber material 
-00001660: 6f62 6a65 6374 2e0a 2020 2020 2020 2020  object..        
-00001670: 4e72 2000 0000 5a07 7265 636f 7264 7329  Nr ...Z.records)
-00001680: 015a 066f 7269 656e 7472 0100 0000 2904  .Z.orientr....).
-00001690: da16 696d 706f 7274 5f73 6563 7469 6f6e  ..import_section
-000016a0: 5f6c 6962 7261 7279 5a03 6c6f 635a 0774  _libraryZ.locZ.t
-000016b0: 6f5f 6469 6374 724a 0000 0029 0572 4900  o_dictrJ...).rI.
-000016c0: 0000 7220 0000 0072 4b00 0000 da07 7365  ..r ...rK.....se
-000016d0: 6374 696f 6e5a 0873 6563 5f64 6963 7472  ctionZ.sec_dictr
-000016e0: 1400 0000 7214 0000 0072 1500 0000 da0c  ....r....r......
-000016f0: 6672 6f6d 5f6c 6962 7261 7279 9100 0000  from_library....
-00001700: 730a 0000 0008 0c06 0112 0110 010a 017a  s..............z
-00001710: 1a54 696d 6265 7253 6563 7469 6f6e 2e66  .TimberSection.f
-00001720: 726f 6d5f 6c69 6272 6172 7963 0100 0000  rom_libraryc....
-00001730: 0000 0000 0000 0000 0100 0000 0200 0000  ................
-00001740: 4300 0001 f30c 0000 007c 006a 007c 006a  C........|.j.|.j
-00001750: 0114 0053 0029 017a 4774 6f74 616c 2077  ...S.).zGtotal w
-00001760: 6964 7468 206f 6620 7365 6374 696f 6e20  idth of section 
-00001770: 636f 6e74 6169 6e69 6e67 206f 6e65 206f  containing one o
-00001780: 7220 6d75 6c74 6970 6c65 2062 6f61 7264  r multiple board
-00001790: 732c 2062 5f74 6f74 203d 206e 2078 2062  s, b_tot = n x b
-000017a0: 2902 721d 0000 0072 1900 0000 722e 0000  ).r....r....r...
-000017b0: 0072 1400 0000 7214 0000 0072 1500 0000  .r....r....r....
-000017c0: 7233 0000 00a3 0000 00f3 0200 0000 0c03  r3..............
-000017d0: 7a13 5469 6d62 6572 5365 6374 696f 6e2e  z.TimberSection.
-000017e0: 625f 746f 7463 0100 0000 0000 0000 0000  b_totc..........
-000017f0: 0000 0200 0000 0400 0000 4300 0001 733c  ..........C...s<
-00001800: 0000 007c 006a 0074 016a 0274 016a 0366  ...|.j.t.j.t.j.f
-00001810: 0276 0072 157c 006a 047c 006a 0564 0113  .v.r.|.j.|.j.d..
-00001820: 0014 0064 021b 007d 017c 0153 0074 0664  ...d...}.|.S.t.d
-00001830: 037c 006a 009b 0064 049d 0383 0182 0129  .|.j...d.......)
-00001840: 057a 1d53 6563 7469 6f6e 206d 6f64 756c  .z.Section modul
-00001850: 7573 2061 626f 7574 2078 2d61 7869 732e  us about x-axis.
-00001860: e902 0000 00e9 0600 0000 7a20 5365 6374  ..........z Sect
-00001870: 696f 6e20 4d6f 6475 6c75 7320 6e6f 7420  ion Modulus not 
-00001880: 6465 6669 6e65 6420 666f 7220 da01 2e29  defined for ...)
-00001890: 0772 1700 0000 720c 0000 0072 1200 0000  .r....r....r....
-000018a0: 7213 0000 0072 3300 0000 721a 0000 0072  r....r3...r....r
-000018b0: 3400 0000 2902 722f 0000 005a 057a 5f6d  4...).r/...Z.z_m
-000018c0: 6f64 7214 0000 0072 1400 0000 7215 0000  odr....r....r...
-000018d0: 00da 035a 5f78 a800 0000 730c 0000 0012  ...Z_x....s.....
-000018e0: 0314 0104 0502 fd0c 0104 ff7a 1154 696d  ...........z.Tim
-000018f0: 6265 7253 6563 7469 6f6e 2e5a 5f78 6301  berSection.Z_xc.
-00001900: 0000 0000 0000 0000 0000 0001 0000 0001  ................
-00001910: 0000 0043 0000 0173 0400 0000 7400 8201  ...C...s....t...
-00001920: 2901 7a7d 5365 6374 696f 6e20 6d6f 6475  ).z}Section modu
-00001930: 6c75 7320 6162 6f75 7420 792d 6178 6973  lus about y-axis
-00001940: 2e0a 2020 2020 2020 2020 4e4f 5445 3a20  ..        NOTE: 
-00001950: 5a20 666f 7220 626c 6f63 6b20 7365 6374  Z for block sect
-00001960: 696f 6e20 7573 6573 2062 5f74 6f74 2028  ion uses b_tot (
-00001970: 6e20 7820 6229 2c20 6275 7420 6b31 3220  n x b), but k12 
-00001980: 7374 6162 696c 6974 7920 6661 6374 6f72  stability factor
-00001990: 2075 7365 7320 622e 0a20 2020 2020 2020   uses b..       
-000019a0: 2029 0172 3400 0000 722e 0000 0072 1400   ).r4...r....r..
-000019b0: 0000 7214 0000 0072 1500 0000 da03 5a5f  ..r....r......Z_
-000019c0: 79b3 0000 0073 0200 0000 0405 7a11 5469  y....s......z.Ti
-000019d0: 6d62 6572 5365 6374 696f 6e2e 5a5f 7963  mberSection.Z_yc
-000019e0: 0100 0000 0000 0000 0000 0000 0100 0000  ................
-000019f0: 0200 0000 4300 0001 7310 0000 0064 017c  ....C...s....d.|
-00001a00: 006a 0014 007c 006a 0114 0053 0029 027a  .j...|.j...S.).z
-00001a10: 1673 6865 6172 2070 6c61 6e65 2061 7265  .shear plane are
-00001a20: 6120 332e 322e 3567 5555 5555 5555 e53f  a 3.2.5gUUUUUU.?
-00001a30: 2902 721a 0000 0072 3300 0000 722e 0000  ).r....r3...r...
-00001a40: 0072 1400 0000 7214 0000 0072 1500 0000  .r....r....r....
-00001a50: da03 415f 73c3 0000 0073 0200 0000 1003  ..A_s....s......
-00001a60: 7a11 5469 6d62 6572 5365 6374 696f 6e2e  z.TimberSection.
-00001a70: 415f 7329 0154 2906 723d 0000 0072 3e00  A_s).T).r=...r>.
-00001a80: 0000 723f 0000 0072 4000 0000 7241 0000  ..r?...r@...rA..
-00001a90: 0072 1600 0000 722c 0000 0029 0472 2000  .r....r,...).r .
-00001aa0: 0000 721f 0000 0072 4b00 0000 724c 0000  ..r....rK...rL..
-00001ab0: 00a9 0272 4100 0000 7218 0000 0029 1a72  ...rA...r....).r
-00001ac0: 0e00 0000 720f 0000 0072 1000 0000 7211  ....r....r....r.
-00001ad0: 0000 0072 4700 0000 721d 0000 0072 2000  ...rG...r....r .
-00001ae0: 0000 7206 0000 0072 2100 0000 7222 0000  ..r....r!...r"..
-00001af0: 0072 2300 0000 7224 0000 0072 2500 0000  .r#...r$...r%...
-00001b00: 7205 0000 0072 2700 0000 722b 0000 0072  r....r'...r+...r
-00001b10: 3000 0000 722d 0000 00da 0b63 6c61 7373  0...r-.....class
-00001b20: 6d65 7468 6f64 724a 0000 0072 4f00 0000  methodrJ...rO...
-00001b30: da08 7072 6f70 6572 7479 7233 0000 0072  ..propertyr3...r
-00001b40: 5500 0000 7256 0000 0072 5700 0000 7214  U...rV...rW...r.
-00001b50: 0000 0072 1400 0000 7214 0000 0072 1500  ...r....r....r..
-00001b60: 0000 7216 0000 002d 0000 0073 3800 0000  ..r....-...s8...
-00001b70: 0a00 0402 0816 0802 0801 0c01 0c01 0c03  ................
-00001b80: 0c01 0c01 0c01 0c01 1202 1402 0802 0803  ................
-00001b90: 021e 0e01 0218 0e01 0211 0c01 0204 0c01  ................
-00001ba0: 020a 0c01 020f 1001 7216 0000 0072 4100  ........r....rA.
-00001bb0: 0000 fa0c 7064 2e44 6174 6146 7261 6d65  ....pd.DataFrame
-00001bc0: 6300 0000 0000 0000 0000 0000 0001 0000  c...............
-00001bd0: 0004 0000 0043 0000 0173 1c00 0000 7400  .....C...s....t.
-00001be0: 7401 6401 8301 a002 6402 a101 8301 7d00  t.d.....d.....}.
-00001bf0: 7403 a004 7c00 a101 5300 2903 612a 0100  t...|...S.).a*..
-00001c00: 000a 2020 2020 496d 706f 7274 7320 6120  ..    Imports a 
-00001c10: 7365 6374 696f 6e20 6c69 6272 6172 7920  section library 
-00001c20: 6672 6f6d 2061 2043 5356 2066 696c 652e  from a CSV file.
-00001c30: 0a0a 2020 2020 5468 6520 4353 5620 6669  ..    The CSV fi
-00001c40: 6c65 2069 7320 6c6f 6361 7465 6420 6174  le is located at
-00001c50: 2027 7469 6d62 6572 6173 2e64 6174 612f   'timberas.data/
-00001c60: 7365 6374 696f 6e5f 6c69 6272 6172 792e  section_library.
-00001c70: 6373 7627 2e0a 0a20 2020 2052 6574 7572  csv'...    Retur
-00001c80: 6e73 3a0a 2020 2020 2020 2020 7064 2e44  ns:.        pd.D
-00001c90: 6174 6146 7261 6d65 3a20 4120 4461 7461  ataFrame: A Data
-00001ca0: 4672 616d 6520 636f 6e74 6169 6e69 6e67  Frame containing
-00001cb0: 2074 6865 2063 6f6e 7465 6e74 7320 6f66   the contents of
-00001cc0: 2074 6865 2073 6563 7469 6f6e 206c 6962   the section lib
-00001cd0: 7261 7279 2043 5356 2066 696c 652e 0a0a  rary CSV file...
-00001ce0: 2020 2020 5261 6973 6573 3a0a 2020 2020      Raises:.    
-00001cf0: 2020 2020 4669 6c65 4e6f 7446 6f75 6e64      FileNotFound
-00001d00: 4572 726f 723a 2049 6620 7468 6520 4353  Error: If the CS
-00001d10: 5620 6669 6c65 2064 6f65 7320 6e6f 7420  V file does not 
-00001d20: 6578 6973 742e 0a20 2020 207a 0d74 696d  exist..    z.tim
-00001d30: 6265 7261 732e 6461 7461 7a13 7365 6374  beras.dataz.sect
-00001d40: 696f 6e5f 6c69 6272 6172 792e 6373 7629  ion_library.csv)
-00001d50: 0572 1f00 0000 7203 0000 005a 086a 6f69  .r....r....Z.joi
-00001d60: 6e70 6174 68da 0270 645a 0872 6561 645f  npath..pdZ.read_
-00001d70: 6373 7629 01da 0966 696c 655f 6e61 6d65  csv)...file_name
-00001d80: 7214 0000 0072 1400 0000 7215 0000 0072  r....r....r....r
-00001d90: 4d00 0000 c900 0000 7304 0000 0012 0c0a  M.......s.......
-00001da0: 0172 4d00 0000 6300 0000 0000 0000 0000  .rM...c.........
-00001db0: 0000 0000 0000 0004 0000 0040 0000 0173  ...........@...s
-00001dc0: 4c00 0000 6500 5a01 6400 5a02 5500 6401  L...e.Z.d.Z.U.d.
-00001dd0: 5a03 6402 6504 6403 3c00 6402 6504 6404  Z.d.e.d.<.d.e.d.
-00001de0: 3c00 6505 640d 6406 6407 8404 8301 5a06  <.e.d.d.d.....Z.
-00001df0: 6505 640d 6408 6409 8404 8301 5a07 6505  e.d.d.d.....Z.e.
-00001e00: 640d 640a 640b 8404 8301 5a08 640c 5300  d.d.d.....Z.d.S.
-00001e10: 290e 7232 0000 0061 2601 0000 0a20 2020  ).r2...a&....   
-00001e20: 2044 6174 6163 6c61 7373 2072 6570 7265   Dataclass repre
-00001e30: 7365 6e74 696e 6720 7374 7275 6374 7572  senting structur
-00001e40: 616c 2073 6563 7469 6f6e 2070 726f 7065  al section prope
-00001e50: 7274 6965 7320 666f 7220 6120 7265 6374  rties for a rect
-00001e60: 616e 6775 6c61 7220 6372 6f73 732d 7365  angular cross-se
-00001e70: 6374 696f 6e2e 0a20 2020 2043 6c61 7373  ction..    Class
-00001e80: 2070 726f 7065 7274 6965 7320 415f 672c   properties A_g,
-00001e90: 2049 5f78 2c20 616e 6420 495f 7920 6361   I_x, and I_y ca
-00001ea0: 6c63 756c 6174 6564 2061 7320 6465 7269  lculated as deri
-00001eb0: 7665 6420 6174 7472 6962 7574 6573 2e0a  ved attributes..
-00001ec0: 0a20 2020 2041 7474 7269 6275 7465 733a  .    Attributes:
-00001ed0: 0a20 2020 2020 2020 2064 2028 666c 6f61  .        d (floa
-00001ee0: 7429 3a20 5468 6520 6865 6967 6874 206f  t): The height o
-00001ef0: 6620 7468 6520 7265 6374 616e 676c 652e  f the rectangle.
-00001f00: 0a20 2020 2020 2020 2062 2028 666c 6f61  .        b (floa
-00001f10: 7429 3a20 5468 6520 6272 6561 6474 6820  t): The breadth 
-00001f20: 286f 7220 7769 6474 6829 206f 6620 7468  (or width) of th
-00001f30: 6520 7265 6374 616e 676c 652e 0a0a 2020  e rectangle...  
-00001f40: 2020 7218 0000 0072 1a00 0000 7219 0000    r....r....r...
-00001f50: 0072 4100 0000 6301 0000 0000 0000 0000  .rA...c.........
-00001f60: 0000 0001 0000 0002 0000 0043 0000 0172  ...........C...r
-00001f70: 5000 0000 2901 7a0a 4772 6f73 7320 6172  P...).z.Gross ar
-00001f80: 6561 7231 0000 0072 2e00 0000 7214 0000  ear1...r....r...
-00001f90: 0072 1400 0000 7215 0000 0072 2100 0000  .r....r....r!...
-00001fa0: e800 0000 7251 0000 007a 1252 6563 7461  ....rQ...z.Recta
-00001fb0: 6e67 6c65 5368 6170 652e 415f 6763 0100  ngleShape.A_gc..
-00001fc0: 0000 0000 0000 0000 0000 0100 0000 0300  ................
-00001fd0: 0000 4300 0001 f314 0000 007c 006a 007c  ..C........|.j.|
-00001fe0: 006a 0164 0113 0014 0064 021b 0053 0029  .j.d.....d...S.)
-00001ff0: 037a 1e4d 6f6d 656e 7420 6f66 2069 6e65  .z.Moment of ine
-00002000: 7274 6961 202d 206d 616a 6f72 2061 7869  rtia - major axi
-00002010: 73e9 0300 0000 e90c 0000 0029 0272 1900  s..........).r..
-00002020: 0000 721a 0000 0072 2e00 0000 7214 0000  ..r....r....r...
-00002030: 0072 1400 0000 7215 0000 0072 2400 0000  .r....r....r$...
-00002040: ed00 0000 f302 0000 0014 037a 1252 6563  ...........z.Rec
-00002050: 7461 6e67 6c65 5368 6170 652e 495f 7863  tangleShape.I_xc
-00002060: 0100 0000 0000 0000 0000 0000 0100 0000  ................
-00002070: 0300 0000 4300 0001 725e 0000 0029 037a  ....C...r^...).z
-00002080: 1e4d 6f6d 656e 7420 6f66 2069 6e65 7274  .Moment of inert
-00002090: 6961 202d 206d 696e 6f72 2061 7869 7372  ia - minor axisr
-000020a0: 5f00 0000 7260 0000 0072 3100 0000 722e  _...r`...r1...r.
-000020b0: 0000 0072 1400 0000 7214 0000 0072 1500  ...r....r....r..
-000020c0: 0000 7225 0000 00f2 0000 0072 6100 0000  ..r%.......ra...
-000020d0: 7a12 5265 6374 616e 676c 6553 6861 7065  z.RectangleShape
-000020e0: 2e49 5f79 4e72 5800 0000 2909 720e 0000  .I_yNrX...).r...
-000020f0: 0072 0f00 0000 7210 0000 0072 1100 0000  .r....r....r....
-00002100: 7247 0000 0072 5a00 0000 7221 0000 0072  rG...rZ...r!...r
-00002110: 2400 0000 7225 0000 0072 1400 0000 7214  $...r%...r....r.
-00002120: 0000 0072 1400 0000 7215 0000 0072 3200  ...r....r....r2.
-00002130: 0000 d900 0000 7314 0000 000a 0004 0208  ......s.........
-00002140: 0a08 0102 020c 0102 040c 0102 0410 0172  ...............r
-00002150: 3200 0000 2902 7241 0000 0072 5b00 0000  2...).rA...r[...
-00002160: 2918 7211 0000 005a 0a5f 5f66 7574 7572  ).r....Z.__futur
-00002170: 655f 5f72 0200 0000 5a13 696d 706f 7274  e__r....Z.import
-00002180: 6c69 622e 7265 736f 7572 6365 7372 0300  lib.resourcesr..
-00002190: 0000 5a0b 6461 7461 636c 6173 7365 7372  ..Z.dataclassesr
-000021a0: 0400 0000 7205 0000 005a 046d 6174 6872  ....r....Z.mathr
-000021b0: 0600 0000 7207 0000 0072 0800 0000 7209  ....r....r....r.
-000021c0: 0000 005a 0465 6e75 6d72 0a00 0000 720b  ...Z.enumr....r.
-000021d0: 0000 005a 0670 616e 6461 7372 5c00 0000  ...Z.pandasr\...
-000021e0: 721f 0000 0072 0c00 0000 7216 0000 0072  r....r....r....r
-000021f0: 4d00 0000 7232 0000 0072 2600 0000 7214  M...r2...r&...r.
-00002200: 0000 0072 1400 0000 7214 0000 0072 1500  ...r....r....r..
-00002210: 0000 da08 3c6d 6f64 756c 653e 0100 0000  ....<module>....
-00002220: 731e 0000 0004 000c 120c 0210 0118 0110  s...............
-00002230: 0108 0112 0308 1110 0100 7f0a 1c02 1010  ................
-00002240: 0108 1e                                  ...
+00000040: 6403 6c03 5a03 6401 6404 6c04 6d05 5a05  d.l.Z.d.d.l.m.Z.
+00000050: 6d06 5a06 0100 6401 6405 6c07 6d08 5a08  m.Z...d.d.l.m.Z.
+00000060: 6d09 5a09 6d0a 5a0a 6d0b 5a0b 0100 6401  m.Z.m.Z.m.Z...d.
+00000070: 6406 6c0c 6d0d 5a0d 6d0e 5a0e 0100 6401  d.l.m.Z.m.Z...d.
+00000080: 6403 6c0f 5a10 4700 6407 6408 8400 6408  d.l.Z.G.d.d...d.
+00000090: 6511 650d 8304 5a12 6505 6409 640a 8d01  e.e...Z.e.d.d...
+000000a0: 4700 640b 640c 8400 640c 8302 8301 5a13  G.d.d...d.....Z.
+000000b0: 6413 640f 6410 8404 5a14 6505 4700 6411  d.d.d...Z.e.G.d.
+000000c0: 6412 8400 6412 8302 8301 5a15 6515 5a16  d...d.....Z.e.Z.
+000000d0: 6403 5300 2914 612d 0200 000a 5468 6973  d.S.).a-....This
+000000e0: 206d 6f64 756c 6520 7072 6f76 6964 6573   module provides
+000000f0: 2063 6c61 7373 6573 2061 6e64 2066 756e   classes and fun
+00000100: 6374 696f 6e73 2074 6f20 6d61 6e61 6765  ctions to manage
+00000110: 2074 696d 6265 7220 7365 6374 696f 6e73   timber sections
+00000120: 2061 6e64 2074 6865 6972 2067 656f 6d65   and their geome
+00000130: 7472 6963 2070 726f 7065 7274 6965 732e  tric properties.
+00000140: 0a0a 436c 6173 7365 733a 2020 2020 0a20  ..Classes:    . 
+00000150: 2020 2053 6861 7065 5479 7065 3a20 456e     ShapeType: En
+00000160: 756d 2063 6c61 7373 2064 6566 696e 696e  um class definin
+00000170: 6720 7365 6374 696f 6e20 7479 7065 2073  g section type s
+00000180: 7472 696e 6720 636f 6e73 7461 6e74 732e  tring constants.
+00000190: 200a 0a20 2020 2054 696d 6265 7253 6563   ..    TimberSec
+000001a0: 7469 6f6e 3a20 4120 636c 6173 7320 6973  tion: A class is
+000001b0: 2075 7365 6420 746f 206d 616e 6167 6520   used to manage 
+000001c0: 7469 6d62 6572 2073 6563 7469 6f6e 2061  timber section a
+000001d0: 7474 7269 6275 7465 732e 200a 0a20 2020  ttributes. ..   
+000001e0: 2052 6563 7461 6e67 6c65 5368 6170 653a   RectangleShape:
+000001f0: 2052 6570 7265 7365 6e74 7320 7374 7275   Represents stru
+00000200: 6374 7572 616c 2073 6563 7469 6f6e 2070  ctural section p
+00000210: 726f 7065 7274 6965 7320 666f 7220 6120  roperties for a 
+00000220: 7265 6374 616e 6775 6c61 7220 6372 6f73  rectangular cros
+00000230: 732d 7365 6374 696f 6e2e 200a 0a20 2020  s-section. ..   
+00000240: 2054 696d 6265 7253 6861 7065 3a20 416e   TimberShape: An
+00000250: 2061 6c69 6173 2066 6f72 2074 6865 2052   alias for the R
+00000260: 6563 7461 6e67 6c65 5368 6170 6520 636c  ectangleShape cl
+00000270: 6173 732e 0a20 2020 200a 4675 6e63 7469  ass..    .Functi
+00000280: 6f6e 733a 0a20 2020 2069 6d70 6f72 745f  ons:.    import_
+00000290: 7365 6374 696f 6e5f 6c69 6272 6172 7928  section_library(
+000002a0: 293a 2052 6574 7572 6e73 2061 2044 6174  ): Returns a Dat
+000002b0: 6146 7261 6d65 2063 6f6e 7461 696e 696e  aFrame containin
+000002c0: 6720 7468 6520 7365 6374 696f 6e20 6c69  g the section li
+000002d0: 6272 6172 7920 6465 6669 6e65 640a 2020  brary defined.  
+000002e0: 2020 696e 2074 696d 6265 7261 732f 6461    in timberas/da
+000002f0: 7461 2f73 6563 7469 6f6e 5f6c 6962 7261  ta/section_libra
+00000300: 7279 2e63 7376 0a0a e900 0000 0029 01da  ry.csv.......)..
+00000310: 0b61 6e6e 6f74 6174 696f 6e73 4e29 02da  .annotationsN)..
+00000320: 0964 6174 6163 6c61 7373 da05 6669 656c  .dataclass..fiel
+00000330: 6429 04da 036e 616e da05 6973 6e61 6eda  d)...nan..isnan.
+00000340: 0566 6c6f 6f72 da05 6c6f 6731 3029 02da  .floor..log10)..
+00000350: 0445 6e75 6dda 0461 7574 6f63 0000 0000  .Enum..autoc....
+00000360: 0000 0000 0000 0000 0000 0000 0100 0000  ................
+00000370: 4000 0001 731c 0000 0065 005a 0164 005a  @...s....e.Z.d.Z
+00000380: 0264 015a 0364 025a 0464 035a 0564 045a  .d.Z.d.Z.d.Z.d.Z
+00000390: 0664 0553 0029 06da 0953 6861 7065 5479  .d.S.)...ShapeTy
+000003a0: 7065 617c 0100 000a 2020 2020 416e 2065  pea|....    An e
+000003b0: 6e75 6d65 7261 7469 6f6e 206f 6620 7365  numeration of se
+000003c0: 6374 696f 6e20 7479 7065 2073 7472 696e  ction type strin
+000003d0: 6720 636f 6e73 7461 6e74 732e 2050 726f  g constants. Pro
+000003e0: 7669 6465 7320 6120 7479 7065 2d73 6166  vides a type-saf
+000003f0: 6520 7761 7920 6f66 2072 6570 7265 7365  e way of represe
+00000400: 6e74 696e 670a 2020 2020 6469 6666 6572  nting.    differ
+00000410: 656e 7420 7365 6374 696f 6e20 7479 7065  ent section type
+00000420: 732e 0a0a 2020 2020 4174 7472 6962 7574  s...    Attribut
+00000430: 6573 3a0a 2020 2020 2020 2020 5349 4e47  es:.        SING
+00000440: 4c45 5f42 4f41 5244 2028 7374 7229 3a20  LE_BOARD (str): 
+00000450: 5265 7072 6573 656e 7473 2061 2073 6563  Represents a sec
+00000460: 7469 6f6e 2063 6f6d 706f 7365 6420 6f66  tion composed of
+00000470: 2061 2073 696e 676c 6520 626f 6172 642c   a single board,
+00000480: 2065 2e67 2e20 3930 7833 350a 2020 2020   e.g. 90x35.    
+00000490: 2020 2020 4d55 4c54 495f 424f 4152 4420      MULTI_BOARD 
+000004a0: 2873 7472 293a 2052 6570 7265 7365 6e74  (str): Represent
+000004b0: 7320 6120 7365 6374 696f 6e20 636f 6d70  s a section comp
+000004c0: 6f73 6564 206f 6620 6d75 6c74 6970 6c65  osed of multiple
+000004d0: 2062 6f61 7264 732c 2065 2e67 2e20 322f   boards, e.g. 2/
+000004e0: 3930 7833 350a 2020 2020 2020 2020 524f  90x35.        RO
+000004f0: 554e 4420 2873 7472 293a 2052 6570 7265  UND (str): Repre
+00000500: 7365 6e74 7320 6120 726f 756e 6420 7365  sents a round se
+00000510: 6374 696f 6e20 2875 6e75 7365 6429 0a20  ction (unused). 
+00000520: 2020 205a 0c73 696e 676c 655f 626f 6172     Z.single_boar
+00000530: 645a 0b6d 756c 7469 5f62 6f61 7264 da05  dZ.multi_board..
+00000540: 726f 756e 644e 2907 da08 5f5f 6e61 6d65  roundN)...__name
+00000550: 5f5f da0a 5f5f 6d6f 6475 6c65 5f5f da0c  __..__module__..
+00000560: 5f5f 7175 616c 6e61 6d65 5f5f da07 5f5f  __qualname__..__
+00000570: 646f 635f 5fda 0c53 494e 474c 455f 424f  doc__..SINGLE_BO
+00000580: 4152 44da 0b4d 554c 5449 5f42 4f41 5244  ARD..MULTI_BOARD
+00000590: 5a05 524f 554e 44a9 0072 1300 0000 7213  Z.ROUND..r....r.
+000005a0: 0000 00fa 4563 3a5c 7573 6572 735c 7571  ....Ec:\users\uq
+000005b0: 6a67 6174 7461 5c64 6f63 756d 656e 7473  jgatta\documents
+000005c0: 5c67 6974 6875 625c 7469 6d62 6572 2d61  \github\timber-a
+000005d0: 735c 7372 635c 7469 6d62 6572 6173 5c67  s\src\timberas\g
+000005e0: 656f 6d65 7472 792e 7079 720b 0000 001c  eometry.pyr.....
+000005f0: 0000 0073 0a00 0000 0800 0401 040b 0401  ...s............
+00000600: 0801 720b 0000 0054 2901 5a07 6b77 5f6f  ..r....T).Z.kw_o
+00000610: 6e6c 7963 0000 0000 0000 0000 0000 0000  nlyc............
+00000620: 0000 0000 0500 0000 4000 0001 730c 0100  ........@...s...
+00000630: 0065 005a 0164 005a 0255 0064 015a 0364  .e.Z.d.Z.U.d.Z.d
+00000640: 0265 0464 033c 0064 0465 0464 053c 0064  .e.d.<.d.e.d.<.d
+00000650: 0465 0464 063c 0064 075a 0564 0865 0464  .e.d.<.d.Z.d.e.d
+00000660: 093c 0064 0a5a 0664 0b65 0464 0c3c 0065  .<.d.Z.d.e.d.<.e
+00000670: 075a 0864 0465 0464 0d3c 0065 075a 0964  .Z.d.e.d.<.e.Z.d
+00000680: 0465 0464 0e3c 0065 075a 0a64 0465 0464  .e.d.<.e.Z.d.e.d
+00000690: 0f3c 0065 075a 0b64 0465 0464 103c 0065  .<.e.Z.d.e.d.<.e
+000006a0: 075a 0c64 0465 0464 113c 0065 0d64 1264  .Z.d.e.d.<.e.d.d
+000006b0: 138d 015a 0e64 1465 0464 153c 0065 0d64  ...Z.d.e.d.<.e.d
+000006c0: 1264 1664 178d 025a 0f64 0865 0464 183c  .d.d...Z.d.e.d.<
+000006d0: 0064 1964 1a84 005a 1064 1b64 1c84 005a  .d.d...Z.d.d...Z
+000006e0: 1165 1264 3264 3364 2364 2484 0583 015a  .e.d2d3d#d$....Z
+000006f0: 1365 1264 3464 3564 2864 2984 0583 015a  .e.d4d5d(d)....Z
+00000700: 1465 1564 3664 2a64 2b84 0483 015a 1665  .e.d6d*d+....Z.e
+00000710: 1564 3664 2c64 2d84 0483 015a 1765 1564  .d6d,d-....Z.e.d
+00000720: 3664 2e64 2f84 0483 015a 1865 1564 3664  6d.d/....Z.e.d6d
+00000730: 3064 3184 0483 015a 1964 2553 0029 37da  0d1....Z.d%S.)7.
+00000740: 0d54 696d 6265 7253 6563 7469 6f6e 61ed  .TimberSectiona.
+00000750: 0400 000a 2020 2020 4361 6c63 756c 6174  ....    Calculat
+00000760: 6573 2067 656f 6d65 7472 6963 2061 6e64  es geometric and
+00000770: 2073 7472 7563 7475 7261 6c20 7365 6374   structural sect
+00000780: 696f 6e20 7072 6f70 6572 7469 6573 2066  ion properties f
+00000790: 726f 6d20 6372 6f73 732d 7365 6374 696f  rom cross-sectio
+000007a0: 6e20 7061 7261 6d65 7465 7273 2e20 5365  n parameters. Se
+000007b0: 6c65 6374 730a 2020 2020 7368 6170 6520  lects.    shape 
+000007c0: 636c 6173 7320 6672 6f6d 2073 6861 7065  class from shape
+000007d0: 5f74 7970 6520 746f 2063 616c 6375 6c61  _type to calcula
+000007e0: 7465 3a20 415f 672c 2041 5f74 2c20 415f  te: A_g, A_t, A_
+000007f0: 632c 2049 5f78 2c20 495f 792e 2043 6c61  c, I_x, I_y. Cla
+00000800: 7373 2070 726f 7065 7274 6965 7320 5a5f  ss properties Z_
+00000810: 782c 205a 5f79 2c0a 2020 2020 625f 746f  x, Z_y,.    b_to
+00000820: 742c 2061 6e64 2041 5f73 2063 616c 6375  t, and A_s calcu
+00000830: 6c61 7465 6420 6173 2064 6572 6976 6564  lated as derived
+00000840: 2061 7474 7269 6275 7465 732e 0a0a 2020   attributes...  
+00000850: 2020 4174 7472 6962 7574 6573 3a0a 2020    Attributes:.  
+00000860: 2020 2020 2020 7368 6170 655f 7479 7065        shape_type
+00000870: 2028 5368 6170 6554 7970 6520 7c20 7374   (ShapeType | st
+00000880: 7229 3a20 5468 6520 7479 7065 206f 6620  r): The type of 
+00000890: 7468 6520 7365 6374 696f 6e20 7368 6170  the section shap
+000008a0: 652e 0a0a 2020 2020 2020 2020 6220 2866  e...        b (f
+000008b0: 6c6f 6174 293a 2054 6865 2062 7265 6164  loat): The bread
+000008c0: 7468 206f 6620 7468 6520 7365 6374 696f  th of the sectio
+000008d0: 6e2e 0a20 2020 2020 2020 2064 2028 666c  n..        d (fl
+000008e0: 6f61 7429 3a20 5468 6520 6465 7074 6820  oat): The depth 
+000008f0: 6f66 2074 6865 2073 6563 7469 6f6e 2e0a  of the section..
+00000900: 2020 2020 2020 2020 6e20 2869 6e74 2c20          n (int, 
+00000910: 6f70 7469 6f6e 616c 293a 2054 6865 206e  optional): The n
+00000920: 756d 6265 7220 6f66 206d 656d 6265 7273  umber of members
+00000930: 2069 6e20 7468 6520 7365 6374 696f 6e2e   in the section.
+00000940: 2044 6566 6175 6c74 203d 2031 2e0a 2020   Default = 1..  
+00000950: 2020 2020 2020 6e61 6d65 2028 7374 722c        name (str,
+00000960: 206f 7074 696f 6e61 6c29 3a20 5468 6520   optional): The 
+00000970: 6e61 6d65 206f 6620 7468 6520 7365 6374  name of the sect
+00000980: 696f 6e2e 2044 6566 6175 6c74 7320 746f  ion. Defaults to
+00000990: 2061 6e20 656d 7074 7920 7374 7269 6e67   an empty string
+000009a0: 2e0a 2020 2020 2020 2020 7368 6170 6520  ..        shape 
+000009b0: 2854 696d 6265 7253 6861 7065 293a 2054  (TimberShape): T
+000009c0: 6865 2073 6861 7065 206f 6620 7468 6520  he shape of the 
+000009d0: 7365 6374 696f 6e2c 2063 616c 6375 6c61  section, calcula
+000009e0: 7465 6420 6166 7465 7220 696e 6974 6961  ted after initia
+000009f0: 6c69 7a61 7469 6f6e 2e0a 2020 2020 2020  lization..      
+00000a00: 2020 415f 6720 2866 6c6f 6174 293a 2054    A_g (float): T
+00000a10: 6865 2067 726f 7373 2061 7265 6120 6f66  he gross area of
+00000a20: 2074 6865 2073 6563 7469 6f6e 2c20 6361   the section, ca
+00000a30: 6c63 756c 6174 6564 2061 6674 6572 2073  lculated after s
+00000a40: 6861 7065 2069 7320 736f 6c76 6564 2e0a  hape is solved..
+00000a50: 2020 2020 2020 2020 415f 7420 2866 6c6f          A_t (flo
+00000a60: 6174 293a 2054 6865 2074 656e 7369 6c65  at): The tensile
+00000a70: 2061 7265 6120 6f66 2074 6865 2073 6563   area of the sec
+00000a80: 7469 6f6e 2c20 6361 6c63 756c 6174 6564  tion, calculated
+00000a90: 2061 6674 6572 2073 6861 7065 2069 7320   after shape is 
+00000aa0: 736f 6c76 6564 2e0a 2020 2020 2020 2020  solved..        
+00000ab0: 415f 6320 2866 6c6f 6174 293a 2054 6865  A_c (float): The
+00000ac0: 2063 6f6d 7072 6573 7369 7665 2061 7265   compressive are
+00000ad0: 6120 6f66 2074 6865 2073 6563 7469 6f6e  a of the section
+00000ae0: 2c20 6361 6c63 756c 6174 6564 2061 6674  , calculated aft
+00000af0: 6572 2073 6861 7065 2069 7320 736f 6c76  er shape is solv
+00000b00: 6564 2e0a 2020 2020 2020 2020 495f 7820  ed..        I_x 
+00000b10: 2866 6c6f 6174 293a 2054 6865 206d 6f6d  (float): The mom
+00000b20: 656e 7420 6f66 2069 6e65 7274 6961 2061  ent of inertia a
+00000b30: 626f 7574 2074 6865 2078 2d61 7869 732c  bout the x-axis,
+00000b40: 2063 616c 6375 6c61 7465 6420 6166 7465   calculated afte
+00000b50: 7220 7368 6170 6520 6973 2073 6f6c 7665  r shape is solve
+00000b60: 642e 0a20 2020 2020 2020 2049 5f79 2028  d..        I_y (
+00000b70: 666c 6f61 7429 3a20 5468 6520 6d6f 6d65  float): The mome
+00000b80: 6e74 206f 6620 696e 6572 7469 6120 6162  nt of inertia ab
+00000b90: 6f75 7420 7468 6520 792d 6178 6973 2c20  out the y-axis, 
+00000ba0: 6361 6c63 756c 6174 6564 2062 7920 7368  calculated by sh
+00000bb0: 6170 6520 6966 206e 6f74 2070 726f 7669  ape if not provi
+00000bc0: 6465 642e 0a20 2020 2020 2020 2073 6967  ded..        sig
+00000bd0: 5f66 6967 7320 2869 6e74 2c20 6f70 7469  _figs (int, opti
+00000be0: 6f6e 616c 293a 204e 756d 6265 7220 6f66  onal): Number of
+00000bf0: 2073 6967 6e69 6669 6361 6e74 2066 6967   significant fig
+00000c00: 7572 6573 2074 6f20 726f 756e 6420 6361  ures to round ca
+00000c10: 6c61 6375 6c61 7465 6420 7661 6c75 6573  laculated values
+00000c20: 2074 6f2e 0a20 2020 2020 2020 2044 6566   to..        Def
+00000c30: 6175 6c74 7320 746f 2034 2e0a 2020 2020  aults to 4..    
+00000c40: 7a0f 5368 6170 6554 7970 6520 7c20 7374  z.ShapeType | st
+00000c50: 72da 0a73 6861 7065 5f74 7970 65da 0566  r..shape_type..f
+00000c60: 6c6f 6174 da01 62da 0164 e901 0000 00da  loat..b..d......
+00000c70: 0369 6e74 da01 6eda 00da 0373 7472 da04  .int..n....str..
+00000c80: 6e61 6d65 da03 415f 67da 0341 5f74 da03  name..A_g..A_t..
+00000c90: 415f 63da 0349 5f78 da03 495f 7946 2901  A_c..I_x..I_yF).
+00000ca0: 5a04 696e 6974 da0b 5469 6d62 6572 5368  Z.init..TimberSh
+00000cb0: 6170 65da 0573 6861 7065 e904 0000 0029  ape..shape.....)
+00000cc0: 02da 0472 6570 72da 0764 6566 6175 6c74  ...repr..default
+00000cd0: da08 7369 675f 6669 6773 6301 0000 0000  ..sig_figsc.....
+00000ce0: 0000 0000 0000 0001 0000 0002 0000 0043  ...............C
+00000cf0: 0000 0173 0c00 0000 7c00 a000 a100 0100  ...s....|.......
+00000d00: 6400 5300 a901 4e29 01da 0b73 6f6c 7665  d.S...N)...solve
+00000d10: 5f73 6861 7065 a901 da04 7365 6c66 7213  _shape....selfr.
+00000d20: 0000 0072 1300 0000 7214 0000 00da 0d5f  ...r....r......_
+00000d30: 5f70 6f73 745f 696e 6974 5f5f 5700 0000  _post_init__W...
+00000d40: 7302 0000 000c 017a 1b54 696d 6265 7253  s......z.TimberS
+00000d50: 6563 7469 6f6e 2e5f 5f70 6f73 745f 696e  ection.__post_in
+00000d60: 6974 5f5f 6301 0000 0000 0000 0000 0000  it__c...........
+00000d70: 0003 0000 000c 0000 0043 0000 0173 0c01  .........C...s..
+00000d80: 0000 7c00 6a00 7401 6a02 7401 6a03 6602  ..|.j.t.j.t.j.f.
+00000d90: 7600 7213 7404 7c00 6a05 7c00 6a06 6401  v.r.t.|.j.|.j.d.
+00000da0: 8d02 7c00 5f07 6e09 7408 6402 7c00 6a00  ..|._.n.t.d.|.j.
+00000db0: 9b00 6403 9d03 8301 8201 7c00 6a09 740a  ..d.......|.j.t.
+00000dc0: 7500 7226 7c00 6a07 6a09 7c00 5f09 7c00  u.r&|.j.j.|._.|.
+00000dd0: 6a0b 740a 7500 7230 7c00 6a07 6a09 7c00  j.t.u.r0|.j.j.|.
+00000de0: 5f0b 7c00 6a0c 740a 7500 723a 7c00 6a07  _.|.j.t.u.r:|.j.
+00000df0: 6a09 7c00 5f0c 7c00 6a0d 740a 7500 7244  j.|._.|.j.t.u.rD
+00000e00: 7c00 6a07 6a0d 7c00 5f0d 7c00 6a0e 740a  |.j.j.|._.|.j.t.
+00000e10: 7500 724e 7c00 6a07 6a0e 7c00 5f0e 7c00  u.rN|.j.j.|._.|.
+00000e20: 6a0f 7282 7410 7c00 6a11 a012 a100 8301  j.r.t.|.j.......
+00000e30: 4400 5d2b 5c02 7d01 7d02 7413 7c02 7414  D.]+\.}.}.t.|.t.
+00000e40: 7415 6602 8302 7281 7416 7c02 8301 7381  t.f...r.t.|...s.
+00000e50: 7c02 6404 6b03 7281 7417 7c00 7c01 7418  |.d.k.r.t.|.|.t.
+00000e60: 7c02 7c00 6a0f 7415 7419 741a 741b 7c02  |.|.j.t.t.t.t.|.
+00000e70: 8301 8301 8301 8301 1800 6405 1800 8302  ..........d.....
+00000e80: 8303 0100 7158 6406 5300 6406 5300 2907  ....qXd.S.d.S.).
+00000e90: 7a52 5365 7473 2073 6861 7065 2063 6c61  zRSets shape cla
+00000ea0: 7373 2062 6173 6564 206f 6e20 7368 6170  ss based on shap
+00000eb0: 655f 7479 7065 2061 6e64 2072 6563 616c  e_type and recal
+00000ec0: 6375 6c61 7465 7320 7265 6c65 7661 6e74  culates relevant
+00000ed0: 2073 6563 7469 6f6e 2070 726f 7065 7274   section propert
+00000ee0: 6965 732e a902 7219 0000 0072 1800 0000  ies...r....r....
+00000ef0: 7a0e 7365 6374 696f 6e20 7479 7065 3a20  z.section type: 
+00000f00: 7a16 2068 6173 206e 6f20 7368 6170 6520  z. has no shape 
+00000f10: 6675 6e63 7469 6f6e 7201 0000 0072 1a00  functionr....r..
+00000f20: 0000 4e29 1c72 1600 0000 720b 0000 0072  ..N).r....r....r
+00000f30: 1100 0000 7212 0000 00da 0e52 6563 7461  ....r......Recta
+00000f40: 6e67 6c65 5368 6170 6572 1900 0000 da05  ngleShaper......
+00000f50: 625f 746f 7472 2600 0000 da13 4e6f 7449  b_totr&.....NotI
+00000f60: 6d70 6c65 6d65 6e74 6564 4572 726f 7272  mplementedErrorr
+00000f70: 2000 0000 7205 0000 0072 2100 0000 7222   ...r....r!...r"
+00000f80: 0000 0072 2300 0000 7224 0000 0072 2a00  ...r#...r$...r*.
+00000f90: 0000 da04 6c69 7374 da08 5f5f 6469 6374  ....list..__dict
+00000fa0: 5f5f da05 6974 656d 73da 0a69 7369 6e73  __..items..isins
+00000fb0: 7461 6e63 6572 1700 0000 721b 0000 0072  tancer....r....r
+00000fc0: 0600 0000 da07 7365 7461 7474 7272 0c00  ......setattrr..
+00000fd0: 0000 7207 0000 0072 0800 0000 da03 6162  ..r....r......ab
+00000fe0: 7329 0372 2e00 0000 da03 6b65 79da 0376  s).r......key..v
+00000ff0: 616c 7213 0000 0072 1300 0000 7214 0000  alr....r....r...
+00001000: 0072 2c00 0000 5a00 0000 7334 0000 0012  .r,...Z...s4....
+00001010: 0214 0102 020c 0104 ff0a 040a 010a 010a  ................
+00001020: 010a 010a 010a 010a 010a 010a 0106 0316  ................
+00001030: 011e 0102 0102 0102 0122 0104 fd02 8004  ........."......
+00001040: fd04 017a 1954 696d 6265 7253 6563 7469  ...z.TimberSecti
+00001050: 6f6e 2e73 6f6c 7665 5f73 6861 7065 54da  on.solve_shapeT.
+00001060: 0a69 6e70 7574 5f64 6963 74da 0464 6963  .input_dict..dic
+00001070: 74da 0873 6f6c 7665 5f6d 65da 0462 6f6f  t..solve_me..boo
+00001080: 6cda 0672 6574 7572 6e63 0300 0000 0000  l..returnc......
+00001090: 0000 0000 0000 0500 0000 0400 0000 0300  ................
+000010a0: 0001 733e 0000 007c 006a 00a0 01a1 0089  ..s>...|.j......
+000010b0: 0087 0066 0164 0164 0284 087c 01a0 02a1  ...f.d.d...|....
+000010c0: 0044 0083 017d 037c 0064 0469 007c 03a4  .D...}.|.d.i.|..
+000010d0: 018e 017d 047c 0272 1d7c 04a0 03a1 0001  ...}.|.r.|......
+000010e0: 007c 0453 0029 0561 ed01 0000 0a20 2020  .|.S.).a.....   
+000010f0: 2020 2020 2043 7265 6174 6520 6120 5469       Create a Ti
+00001100: 6d62 6572 5365 6374 696f 6e20 6279 2064  mberSection by d
+00001110: 6972 6563 746c 7920 706f 7075 6c61 7469  irectly populati
+00001120: 6e67 2061 7474 7269 6275 7465 7320 6672  ng attributes fr
+00001130: 6f6d 2069 6e70 7574 2064 6963 7469 6f6e  om input diction
+00001140: 6172 792c 0a20 2020 2020 2020 2069 676e  ary,.        ign
+00001150: 6f72 696e 6720 6469 6374 696f 6e61 7279  oring dictionary
+00001160: 206b 6579 7320 7768 6963 6820 6172 656e   keys which aren
+00001170: 2774 2063 6c61 7373 2061 7474 7269 6275  't class attribu
+00001180: 7465 732e 0a0a 2020 2020 2020 2020 4172  tes...        Ar
+00001190: 6773 3a0a 2020 2020 2020 2020 2020 2020  gs:.            
+000011a0: 696e 7075 745f 6469 6374 3a20 4465 6669  input_dict: Defi
+000011b0: 6e65 7320 7469 6d62 6572 206d 6174 6572  nes timber mater
+000011c0: 6961 6c20 6461 7461 2074 6f20 6265 2061  ial data to be a
+000011d0: 6464 6564 2c20 6b65 7973 2063 6f72 7265  dded, keys corre
+000011e0: 7370 6f6e 6469 6e67 2074 6f20 636c 6173  sponding to clas
+000011f0: 730a 2020 2020 2020 2020 2020 2020 6174  s.            at
+00001200: 7472 6962 7574 6520 6e61 6d65 7320 7769  tribute names wi
+00001210: 6c6c 2062 6520 7570 6461 7465 6420 616e  ll be updated an
+00001220: 6420 6f74 6865 7273 2077 696c 6c20 6265  d others will be
+00001230: 2069 676e 6f72 6564 0a20 2020 2020 2020   ignored.       
+00001240: 2020 2020 2073 6f6c 7665 5f6d 653a 2049       solve_me: I
+00001250: 6620 5472 7565 2077 696c 6c20 7275 6e20  f True will run 
+00001260: 736f 6c76 655f 7368 6170 6528 2920 6166  solve_shape() af
+00001270: 7465 7220 6174 7472 6962 7574 6573 2061  ter attributes a
+00001280: 7265 2061 6464 6564 0a0a 2020 2020 2020  re added..      
+00001290: 2020 5265 7475 726e 733a 0a20 2020 2020    Returns:.     
+000012a0: 2020 2020 2020 2054 696d 6265 7253 6563         TimberSec
+000012b0: 7469 6f6e 3a20 5468 6520 7469 6d62 6572  tion: The timber
+000012c0: 2073 6563 7469 6f6e 206f 626a 6563 742e   section object.
+000012d0: 0a20 2020 2020 2020 2063 0100 0000 0000  .        c......
+000012e0: 0000 0000 0000 0300 0000 0400 0000 1300  ................
+000012f0: 0001 731e 0000 0069 007c 005d 0b5c 027d  ..s....i.|.].\.}
+00001300: 017d 027c 0188 0076 0072 027c 017c 0293  .}.|...v.r.|.|..
+00001310: 0271 0253 0072 1300 0000 7213 0000 0029  .q.S.r....r....)
+00001320: 03da 022e 30da 016b da01 76a9 015a 0a76  ....0..k..v..Z.v
+00001330: 616c 6964 5f6b 6579 7372 1300 0000 7214  alid_keysr....r.
+00001340: 0000 00da 0a3c 6469 6374 636f 6d70 3e8a  .....<dictcomp>.
+00001350: 0000 0073 0200 0000 1e00 7a2b 5469 6d62  ...s......z+Timb
+00001360: 6572 5365 6374 696f 6e2e 6672 6f6d 5f64  erSection.from_d
+00001370: 6963 742e 3c6c 6f63 616c 733e 2e3c 6469  ict.<locals>.<di
+00001380: 6374 636f 6d70 3e4e 7213 0000 0029 04da  ctcomp>Nr....)..
+00001390: 0f5f 5f61 6e6e 6f74 6174 696f 6e73 5f5f  .__annotations__
+000013a0: da04 6b65 7973 7236 0000 0072 2c00 0000  ..keysr6...r,...
+000013b0: 2905 da03 636c 7372 3c00 0000 723e 0000  )...clsr<...r>..
+000013c0: 005a 0a76 616c 6964 5f64 6963 745a 076e  .Z.valid_dictZ.n
+000013d0: 6577 5f6f 626a 7213 0000 0072 4400 0000  ew_objr....rD...
+000013e0: 7214 0000 00da 0966 726f 6d5f 6469 6374  r......from_dict
+000013f0: 7800 0000 730c 0000 000a 1016 020e 0204  x...s...........
+00001400: 0108 0104 017a 1754 696d 6265 7253 6563  .....z.TimberSec
+00001410: 7469 6f6e 2e66 726f 6d5f 6469 6374 4eda  tion.from_dictN.
+00001420: 076c 6962 7261 7279 fa13 7064 2e44 6174  .library..pd.Dat
+00001430: 6146 7261 6d65 207c 204e 6f6e 6563 0300  aFrame | Nonec..
+00001440: 0000 0000 0000 0000 0000 0500 0000 0300  ................
+00001450: 0000 4300 0001 733a 0000 007c 0264 0175  ..C...s:...|.d.u
+00001460: 0072 0774 0083 007d 027c 026a 017c 0264  .r.t...}.|.j.|.d
+00001470: 0219 007c 016b 0219 007d 037c 036a 0264  ...|.k...}.|.j.d
+00001480: 0364 048d 0164 0519 007d 047c 00a0 037c  .d...d...}.|...|
+00001490: 04a1 0153 0029 0661 c701 0000 4372 6561  ...S.).a....Crea
+000014a0: 7465 7320 6120 5469 6d62 6572 5365 6374  tes a TimberSect
+000014b0: 696f 6e20 6f62 6a65 6374 2066 726f 6d20  ion object from 
+000014c0: 6120 6d61 7465 7269 616c 206c 6962 7261  a material libra
+000014d0: 7279 2028 4461 7461 4672 616d 6529 2e0a  ry (DataFrame)..
+000014e0: 0a20 2020 2020 2020 2041 7267 733a 0a20  .        Args:. 
+000014f0: 2020 2020 2020 2020 2020 206e 616d 653a             name:
+00001500: 2054 6865 206e 616d 6520 6f66 2074 6865   The name of the
+00001510: 2074 696d 6265 7220 6d61 7465 7269 616c   timber material
+00001520: 2074 6f20 6c6f 6f6b 7570 2069 6e20 7468   to lookup in th
+00001530: 6520 6c69 6272 6172 7920 2869 6e20 276e  e library (in 'n
+00001540: 616d 6527 2063 6f6c 756d 6e29 0a20 2020  ame' column).   
+00001550: 2020 2020 2020 2020 206c 6962 7261 7279           library
+00001560: 2028 7064 2e44 6174 6146 7261 6d65 2c20   (pd.DataFrame, 
+00001570: 6f70 7469 6f6e 616c 293a 2044 6174 6146  optional): DataF
+00001580: 7261 6d65 2063 6f6e 7461 696e 696e 6720  rame containing 
+00001590: 6120 6c69 6272 6172 7920 6f66 2074 696d  a library of tim
+000015a0: 6265 7220 6d61 7465 7269 616c 732e 0a20  ber materials.. 
+000015b0: 2020 2020 2020 2020 2020 2020 2020 2049                 I
+000015c0: 6620 6e6f 7420 7072 6f76 6964 6564 2c20  f not provided, 
+000015d0: 7468 6520 6465 6661 756c 7420 7365 6374  the default sect
+000015e0: 696f 6e20 6c69 6272 6172 7920 6973 2075  ion library is u
+000015f0: 7365 6420 6672 6f6d 2069 6d70 6f72 745f  sed from import_
+00001600: 7365 6374 696f 6e5f 6c69 6272 6172 792e  section_library.
+00001610: 0a0a 2020 2020 2020 2020 5265 7475 726e  ..        Return
+00001620: 733a 0a20 2020 2020 2020 2020 2020 2054  s:.            T
+00001630: 696d 6265 724d 6174 6572 6961 6c3a 2054  imberMaterial: T
+00001640: 6865 2074 696d 6265 7220 6d61 7465 7269  he timber materi
+00001650: 616c 206f 626a 6563 742e 0a20 2020 2020  al object..     
+00001660: 2020 204e 721f 0000 005a 0772 6563 6f72     Nr....Z.recor
+00001670: 6473 2901 5a06 6f72 6965 6e74 7201 0000  ds).Z.orientr...
+00001680: 0029 04da 1669 6d70 6f72 745f 7365 6374  .)...import_sect
+00001690: 696f 6e5f 6c69 6272 6172 795a 036c 6f63  ion_libraryZ.loc
+000016a0: 5a07 746f 5f64 6963 7472 4900 0000 2905  Z.to_dictrI...).
+000016b0: 7248 0000 0072 1f00 0000 724a 0000 005a  rH...r....rJ...Z
+000016c0: 0773 6563 7469 6f6e 5a08 7365 635f 6469  .sectionZ.sec_di
+000016d0: 6374 7213 0000 0072 1300 0000 7214 0000  ctr....r....r...
+000016e0: 00da 0c66 726f 6d5f 6c69 6272 6172 7991  ...from_library.
+000016f0: 0000 0073 0a00 0000 080c 0601 1201 1001  ...s............
+00001700: 0a01 7a1a 5469 6d62 6572 5365 6374 696f  ..z.TimberSectio
+00001710: 6e2e 6672 6f6d 5f6c 6962 7261 7279 6301  n.from_libraryc.
+00001720: 0000 0000 0000 0000 0000 0001 0000 0002  ................
+00001730: 0000 0043 0000 01f3 0c00 0000 7c00 6a00  ...C........|.j.
+00001740: 7c00 6a01 1400 5300 2901 7a47 746f 7461  |.j...S.).zGtota
+00001750: 6c20 7769 6474 6820 6f66 2073 6563 7469  l width of secti
+00001760: 6f6e 2063 6f6e 7461 696e 696e 6720 6f6e  on containing on
+00001770: 6520 6f72 206d 756c 7469 706c 6520 626f  e or multiple bo
+00001780: 6172 6473 2c20 625f 746f 7420 3d20 6e20  ards, b_tot = n 
+00001790: 7820 6229 0272 1c00 0000 7218 0000 0072  x b).r....r....r
+000017a0: 2d00 0000 7213 0000 0072 1300 0000 7214  -...r....r....r.
+000017b0: 0000 0072 3200 0000 a300 0000 f302 0000  ...r2...........
+000017c0: 000c 037a 1354 696d 6265 7253 6563 7469  ...z.TimberSecti
+000017d0: 6f6e 2e62 5f74 6f74 6301 0000 0000 0000  on.b_totc.......
+000017e0: 0000 0000 0002 0000 0004 0000 0043 0000  .............C..
+000017f0: 0173 3c00 0000 7c00 6a00 7401 6a02 7401  .s<...|.j.t.j.t.
+00001800: 6a03 6602 7600 7215 7c00 6a04 7c00 6a05  j.f.v.r.|.j.|.j.
+00001810: 6401 1300 1400 6402 1b00 7d01 7c01 5300  d.....d...}.|.S.
+00001820: 7406 6403 7c00 6a00 9b00 6404 9d03 8301  t.d.|.j...d.....
+00001830: 8201 2905 7a1d 5365 6374 696f 6e20 6d6f  ..).z.Section mo
+00001840: 6475 6c75 7320 6162 6f75 7420 782d 6178  dulus about x-ax
+00001850: 6973 2ee9 0200 0000 e906 0000 007a 2053  is...........z S
+00001860: 6563 7469 6f6e 204d 6f64 756c 7573 206e  ection Modulus n
+00001870: 6f74 2064 6566 696e 6564 2066 6f72 20da  ot defined for .
+00001880: 012e 2907 7216 0000 0072 0b00 0000 7211  ..).r....r....r.
+00001890: 0000 0072 1200 0000 7232 0000 0072 1900  ...r....r2...r..
+000018a0: 0000 7233 0000 0029 0272 2e00 0000 5a05  ..r3...).r....Z.
+000018b0: 7a5f 6d6f 6472 1300 0000 7213 0000 0072  z_modr....r....r
+000018c0: 1400 0000 da03 5a5f 78a8 0000 0073 0c00  ......Z_x....s..
+000018d0: 0000 1203 1401 0405 02fd 0c01 04ff 7a11  ..............z.
+000018e0: 5469 6d62 6572 5365 6374 696f 6e2e 5a5f  TimberSection.Z_
+000018f0: 7863 0100 0000 0000 0000 0000 0000 0100  xc..............
+00001900: 0000 0100 0000 4300 0001 7304 0000 0074  ......C...s....t
+00001910: 0082 0129 017a 7d53 6563 7469 6f6e 206d  ...).z}Section m
+00001920: 6f64 756c 7573 2061 626f 7574 2079 2d61  odulus about y-a
+00001930: 7869 732e 0a20 2020 2020 2020 204e 4f54  xis..        NOT
+00001940: 453a 205a 2066 6f72 2062 6c6f 636b 2073  E: Z for block s
+00001950: 6563 7469 6f6e 2075 7365 7320 625f 746f  ection uses b_to
+00001960: 7420 286e 2078 2062 292c 2062 7574 206b  t (n x b), but k
+00001970: 3132 2073 7461 6269 6c69 7479 2066 6163  12 stability fac
+00001980: 746f 7220 7573 6573 2062 2e0a 2020 2020  tor uses b..    
+00001990: 2020 2020 2901 7233 0000 0072 2d00 0000      ).r3...r-...
+000019a0: 7213 0000 0072 1300 0000 7214 0000 00da  r....r....r.....
+000019b0: 035a 5f79 b300 0000 7302 0000 0004 057a  .Z_y....s......z
+000019c0: 1154 696d 6265 7253 6563 7469 6f6e 2e5a  .TimberSection.Z
+000019d0: 5f79 6301 0000 0000 0000 0000 0000 0001  _yc.............
+000019e0: 0000 0002 0000 0043 0000 0173 1000 0000  .......C...s....
+000019f0: 6401 7c00 6a00 1400 7c00 6a01 1400 5300  d.|.j...|.j...S.
+00001a00: 2902 7a16 7368 6561 7220 706c 616e 6520  ).z.shear plane 
+00001a10: 6172 6561 2033 2e32 2e35 6755 5555 5555  area 3.2.5gUUUUU
+00001a20: 55e5 3f29 0272 1900 0000 7232 0000 0072  U.?).r....r2...r
+00001a30: 2d00 0000 7213 0000 0072 1300 0000 7214  -...r....r....r.
+00001a40: 0000 00da 0341 5f73 c300 0000 7302 0000  .....A_s....s...
+00001a50: 0010 037a 1154 696d 6265 7253 6563 7469  ...z.TimberSecti
+00001a60: 6f6e 2e41 5f73 2901 5429 0672 3c00 0000  on.A_s).T).r<...
+00001a70: 723d 0000 0072 3e00 0000 723f 0000 0072  r=...r>...r?...r
+00001a80: 4000 0000 7215 0000 0072 2b00 0000 2904  @...r....r+...).
+00001a90: 721f 0000 0072 1e00 0000 724a 0000 0072  r....r....rJ...r
+00001aa0: 4b00 0000 a902 7240 0000 0072 1700 0000  K.....r@...r....
+00001ab0: 291a 720d 0000 0072 0e00 0000 720f 0000  ).r....r....r...
+00001ac0: 0072 1000 0000 7246 0000 0072 1c00 0000  .r....rF...r....
+00001ad0: 721f 0000 0072 0500 0000 7220 0000 0072  r....r....r ...r
+00001ae0: 2100 0000 7222 0000 0072 2300 0000 7224  !...r"...r#...r$
+00001af0: 0000 0072 0400 0000 7226 0000 0072 2a00  ...r....r&...r*.
+00001b00: 0000 722f 0000 0072 2c00 0000 da0b 636c  ..r/...r,.....cl
+00001b10: 6173 736d 6574 686f 6472 4900 0000 724d  assmethodrI...rM
+00001b20: 0000 00da 0870 726f 7065 7274 7972 3200  .....propertyr2.
+00001b30: 0000 7253 0000 0072 5400 0000 7255 0000  ..rS...rT...rU..
+00001b40: 0072 1300 0000 7213 0000 0072 1300 0000  .r....r....r....
+00001b50: 7214 0000 0072 1500 0000 2d00 0000 7338  r....r....-...s8
+00001b60: 0000 000a 0004 0208 1608 0208 010c 010c  ................
+00001b70: 010c 030c 010c 010c 010c 0112 0214 0208  ................
+00001b80: 0208 0302 1e0e 0102 180e 0102 110c 0102  ................
+00001b90: 040c 0102 0a0c 0102 0f10 0172 1500 0000  ...........r....
+00001ba0: 7240 0000 00fa 0c70 642e 4461 7461 4672  r@.....pd.DataFr
+00001bb0: 616d 6563 0000 0000 0000 0000 0000 0000  amec............
+00001bc0: 0200 0000 0400 0000 4300 0001 7324 0000  ........C...s$..
+00001bd0: 0074 006a 01a0 0274 03a1 017d 0074 006a  .t.j...t...}.t.j
+00001be0: 01a0 047c 0064 01a1 027d 0174 05a0 067c  ...|.d...}.t...|
+00001bf0: 01a1 0153 0029 0261 2a01 0000 0a20 2020  ...S.).a*....   
+00001c00: 2049 6d70 6f72 7473 2061 2073 6563 7469   Imports a secti
+00001c10: 6f6e 206c 6962 7261 7279 2066 726f 6d20  on library from 
+00001c20: 6120 4353 5620 6669 6c65 2e0a 0a20 2020  a CSV file...   
+00001c30: 2054 6865 2043 5356 2066 696c 6520 6973   The CSV file is
+00001c40: 206c 6f63 6174 6564 2061 7420 2774 696d   located at 'tim
+00001c50: 6265 7261 732f 6461 7461 2f73 6563 7469  beras/data/secti
+00001c60: 6f6e 5f6c 6962 7261 7279 2e63 7376 272e  on_library.csv'.
+00001c70: 0a0a 2020 2020 5265 7475 726e 733a 0a20  ..    Returns:. 
+00001c80: 2020 2020 2020 2070 642e 4461 7461 4672         pd.DataFr
+00001c90: 616d 653a 2041 2044 6174 6146 7261 6d65  ame: A DataFrame
+00001ca0: 2063 6f6e 7461 696e 696e 6720 7468 6520   containing the 
+00001cb0: 636f 6e74 656e 7473 206f 6620 7468 6520  contents of the 
+00001cc0: 7365 6374 696f 6e20 6c69 6272 6172 7920  section library 
+00001cd0: 4353 5620 6669 6c65 2e0a 0a20 2020 2052  CSV file...    R
+00001ce0: 6169 7365 733a 0a20 2020 2020 2020 2046  aises:.        F
+00001cf0: 696c 654e 6f74 466f 756e 6445 7272 6f72  ileNotFoundError
+00001d00: 3a20 4966 2074 6865 2043 5356 2066 696c  : If the CSV fil
+00001d10: 6520 646f 6573 206e 6f74 2065 7869 7374  e does not exist
+00001d20: 2e0a 2020 2020 7a18 6461 7461 2f73 6563  ..    z.data/sec
+00001d30: 7469 6f6e 5f6c 6962 7261 7279 2e63 7376  tion_library.csv
+00001d40: 2907 da02 6f73 da04 7061 7468 da07 6469  )...os..path..di
+00001d50: 726e 616d 65da 085f 5f66 696c 655f 5fda  rname..__file__.
+00001d60: 046a 6f69 6eda 0270 645a 0872 6561 645f  .join..pdZ.read_
+00001d70: 6373 7629 02da 0363 7764 5a08 6c69 625f  csv)...cwdZ.lib_
+00001d80: 7061 7468 7213 0000 0072 1300 0000 7214  pathr....r....r.
+00001d90: 0000 0072 4c00 0000 c900 0000 7306 0000  ...rL.......s...
+00001da0: 000c 0c0e 010a 0172 4c00 0000 6300 0000  .......rL...c...
+00001db0: 0000 0000 0000 0000 0000 0000 0004 0000  ................
+00001dc0: 0040 0000 0173 4c00 0000 6500 5a01 6400  .@...sL...e.Z.d.
+00001dd0: 5a02 5500 6401 5a03 6402 6504 6403 3c00  Z.U.d.Z.d.e.d.<.
+00001de0: 6402 6504 6404 3c00 6505 640d 6406 6407  d.e.d.<.e.d.d.d.
+00001df0: 8404 8301 5a06 6505 640d 6408 6409 8404  ....Z.e.d.d.d...
+00001e00: 8301 5a07 6505 640d 640a 640b 8404 8301  ..Z.e.d.d.d.....
+00001e10: 5a08 640c 5300 290e 7231 0000 0061 2601  Z.d.S.).r1...a&.
+00001e20: 0000 0a20 2020 2044 6174 6163 6c61 7373  ...    Dataclass
+00001e30: 2072 6570 7265 7365 6e74 696e 6720 7374   representing st
+00001e40: 7275 6374 7572 616c 2073 6563 7469 6f6e  ructural section
+00001e50: 2070 726f 7065 7274 6965 7320 666f 7220   properties for 
+00001e60: 6120 7265 6374 616e 6775 6c61 7220 6372  a rectangular cr
+00001e70: 6f73 732d 7365 6374 696f 6e2e 0a20 2020  oss-section..   
+00001e80: 2043 6c61 7373 2070 726f 7065 7274 6965   Class propertie
+00001e90: 7320 415f 672c 2049 5f78 2c20 616e 6420  s A_g, I_x, and 
+00001ea0: 495f 7920 6361 6c63 756c 6174 6564 2061  I_y calculated a
+00001eb0: 7320 6465 7269 7665 6420 6174 7472 6962  s derived attrib
+00001ec0: 7574 6573 2e0a 0a20 2020 2041 7474 7269  utes...    Attri
+00001ed0: 6275 7465 733a 0a20 2020 2020 2020 2064  butes:.        d
+00001ee0: 2028 666c 6f61 7429 3a20 5468 6520 6865   (float): The he
+00001ef0: 6967 6874 206f 6620 7468 6520 7265 6374  ight of the rect
+00001f00: 616e 676c 652e 0a20 2020 2020 2020 2062  angle..        b
+00001f10: 2028 666c 6f61 7429 3a20 5468 6520 6272   (float): The br
+00001f20: 6561 6474 6820 286f 7220 7769 6474 6829  eadth (or width)
+00001f30: 206f 6620 7468 6520 7265 6374 616e 676c   of the rectangl
+00001f40: 652e 0a0a 2020 2020 7217 0000 0072 1900  e...    r....r..
+00001f50: 0000 7218 0000 0072 4000 0000 6301 0000  ..r....r@...c...
+00001f60: 0000 0000 0000 0000 0001 0000 0002 0000  ................
+00001f70: 0043 0000 0172 4e00 0000 2901 7a0a 4772  .C...rN...).z.Gr
+00001f80: 6f73 7320 6172 6561 7230 0000 0072 2d00  oss arear0...r-.
+00001f90: 0000 7213 0000 0072 1300 0000 7214 0000  ..r....r....r...
+00001fa0: 0072 2000 0000 e900 0000 724f 0000 007a  .r .......rO...z
+00001fb0: 1252 6563 7461 6e67 6c65 5368 6170 652e  .RectangleShape.
+00001fc0: 415f 6763 0100 0000 0000 0000 0000 0000  A_gc............
+00001fd0: 0100 0000 0300 0000 4300 0001 f314 0000  ........C.......
+00001fe0: 007c 006a 007c 006a 0164 0113 0014 0064  .|.j.|.j.d.....d
+00001ff0: 021b 0053 0029 037a 1e4d 6f6d 656e 7420  ...S.).z.Moment 
+00002000: 6f66 2069 6e65 7274 6961 202d 206d 616a  of inertia - maj
+00002010: 6f72 2061 7869 73e9 0300 0000 e90c 0000  or axis.........
+00002020: 0029 0272 1800 0000 7219 0000 0072 2d00  .).r....r....r-.
+00002030: 0000 7213 0000 0072 1300 0000 7214 0000  ..r....r....r...
+00002040: 0072 2300 0000 ee00 0000 f302 0000 0014  .r#.............
+00002050: 037a 1252 6563 7461 6e67 6c65 5368 6170  .z.RectangleShap
+00002060: 652e 495f 7863 0100 0000 0000 0000 0000  e.I_xc..........
+00002070: 0000 0100 0000 0300 0000 4300 0001 7261  ..........C...ra
+00002080: 0000 0029 037a 1e4d 6f6d 656e 7420 6f66  ...).z.Moment of
+00002090: 2069 6e65 7274 6961 202d 206d 696e 6f72   inertia - minor
+000020a0: 2061 7869 7372 6200 0000 7263 0000 0072   axisrb...rc...r
+000020b0: 3000 0000 722d 0000 0072 1300 0000 7213  0...r-...r....r.
+000020c0: 0000 0072 1400 0000 7224 0000 00f3 0000  ...r....r$......
+000020d0: 0072 6400 0000 7a12 5265 6374 616e 676c  .rd...z.Rectangl
+000020e0: 6553 6861 7065 2e49 5f79 4e72 5600 0000  eShape.I_yNrV...
+000020f0: 2909 720d 0000 0072 0e00 0000 720f 0000  ).r....r....r...
+00002100: 0072 1000 0000 7246 0000 0072 5800 0000  .r....rF...rX...
+00002110: 7220 0000 0072 2300 0000 7224 0000 0072  r ...r#...r$...r
+00002120: 1300 0000 7213 0000 0072 1300 0000 7214  ....r....r....r.
+00002130: 0000 0072 3100 0000 da00 0000 7314 0000  ...r1.......s...
+00002140: 000a 0004 0208 0a08 0102 020c 0102 040c  ................
+00002150: 0102 0410 0172 3100 0000 2902 7240 0000  .....r1...).r@..
+00002160: 0072 5900 0000 2917 7210 0000 005a 0a5f  .rY...).r....Z._
+00002170: 5f66 7574 7572 655f 5f72 0200 0000 725a  _future__r....rZ
+00002180: 0000 005a 0b64 6174 6163 6c61 7373 6573  ...Z.dataclasses
+00002190: 7203 0000 0072 0400 0000 5a04 6d61 7468  r....r....Z.math
+000021a0: 7205 0000 0072 0600 0000 7207 0000 0072  r....r....r....r
+000021b0: 0800 0000 5a04 656e 756d 7209 0000 0072  ....Z.enumr....r
+000021c0: 0a00 0000 5a06 7061 6e64 6173 725f 0000  ....Z.pandasr_..
+000021d0: 0072 1e00 0000 720b 0000 0072 1500 0000  .r....r....r....
+000021e0: 724c 0000 0072 3100 0000 7225 0000 0072  rL...r1...r%...r
+000021f0: 1300 0000 7213 0000 0072 1300 0000 7214  ....r....r....r.
+00002200: 0000 00da 083c 6d6f 6475 6c65 3e01 0000  .....<module>...
+00002210: 0073 1e00 0000 0400 0c12 0802 1001 1801  .s..............
+00002220: 1001 0801 1203 0811 1001 007f 0a1c 0211  ................
+00002230: 1001 081e                                ....
```

### Comparing `timberas-0.2.0/src/timberas/__pycache__/material.cpython-310.pyc` & `timberas-0.3.0/src/timberas/__pycache__/material.cpython-310.pyc`

 * *Format-specific differences are supported for Python .pyc files but no file-specific differences were detected; falling back to a binary diff. file(1) reports: Byte-compiled Python module for CPython 3.10, timestamp-based, .py timestamp: Tue Jul 18 00:52:03 2023 UTC, .py size: 8228 bytes*

 * *Could not decompile bytecode: bad marshal data (unknown type code)*

 * *Files 8% similar despite different names*

```diff
@@ -1,490 +1,490 @@
-00000000: 6f0d 0d0a 0000 0000 33e2 b564 2420 0000  o.......3..d$ ..
+00000000: 6f0d 0d0a 0000 0000 8e21 bd64 5a20 0000  o........!.dZ ..
 00000010: e300 0000 0000 0000 0000 0000 0000 0000  ................
-00000020: 0005 0000 0040 0000 0173 9200 0000 6400  .....@...s....d.
+00000020: 0005 0000 0040 0000 0173 8e00 0000 6400  .....@...s....d.
 00000030: 5a00 6401 6402 6c01 6d02 5a02 0100 6401  Z.d.d.l.m.Z...d.
-00000040: 6403 6c03 6d04 5a04 0100 6401 6404 6c05  d.l.m.Z...d.d.l.
-00000050: 6d06 5a06 6d07 5a07 0100 6401 6405 6c08  m.Z.m.Z...d.d.l.
-00000060: 6d09 5a09 0100 6401 6406 6c0a 5a0b 4700  m.Z...d.d.l.Z.G.
-00000070: 6407 6408 8400 6408 650c 6509 8304 5a0d  d.d...d.e.e...Z.
-00000080: 6414 640b 640c 8404 5a0e 6506 640d 640e  d.d.d...Z.e.d.d.
-00000090: 8d01 4700 640f 6410 8400 6410 8302 8301  ..G.d.d...d.....
-000000a0: 5a0f 6411 6412 8400 5a10 6511 6413 6b02  Z.d.d...Z.e.d.k.
-000000b0: 7247 6510 8300 0100 6406 5300 6406 5300  rGe.....d.S.d.S.
-000000c0: 2915 618e 0100 000a 5468 6973 206d 6f64  ).a.....This mod
-000000d0: 756c 6520 7072 6f76 6964 6573 2063 6c61  ule provides cla
-000000e0: 7373 6573 2061 6e64 2066 756e 6374 696f  sses and functio
-000000f0: 6e73 2066 6f72 2063 7265 6174 696e 6720  ns for creating 
-00000100: 7265 7072 6573 656e 7469 6e67 2074 696d  representing tim
-00000110: 6265 7220 6d61 7465 7269 616c 7320 0a62  ber materials .b
-00000120: 6173 6564 206f 6e20 4153 3137 3230 2e20  ased on AS1720. 
-00000130: 0a0a 436c 6173 7365 733a 0a20 2020 2047  ..Classes:.    G
-00000140: 7261 6465 5479 7065 3a20 456e 756d 2063  radeType: Enum c
-00000150: 6c61 7373 2064 6566 696e 696e 6720 6d61  lass defining ma
-00000160: 7465 7269 616c 2067 7261 6465 2073 7472  terial grade str
-00000170: 696e 6720 636f 6e73 7461 6e74 732e 200a  ing constants. .
-00000180: 0a20 2020 2054 696d 6265 724d 6174 6572  .    TimberMater
-00000190: 6961 6c3a 2052 6570 7265 7365 6e74 7320  ial: Represents 
-000001a0: 6120 7469 6d62 6572 206d 6174 6572 6961  a timber materia
-000001b0: 6c20 6261 7365 6420 6f6e 2041 5331 3732  l based on AS172
-000001c0: 302e 200a 0a46 756e 6374 696f 6e73 3a0a  0. ..Functions:.
-000001d0: 2020 2020 696d 706f 7274 5f6d 6174 6572      import_mater
-000001e0: 6961 6c5f 6c69 6272 6172 7928 293a 2052  ial_library(): R
-000001f0: 6574 7572 6e73 2061 2044 6174 6146 7261  eturns a DataFra
-00000200: 6d65 2063 6f6e 7461 696e 696e 6720 7468  me containing th
-00000210: 6520 6d61 7465 7269 616c 206c 6962 7261  e material libra
-00000220: 7279 2064 6566 696e 6564 0a20 2020 2069  ry defined.    i
-00000230: 6e20 7469 6d62 6572 6173 2f64 6174 612f  n timberas/data/
-00000240: 6d61 7465 7269 616c 5f6c 6962 7261 7279  material_library
-00000250: 2e63 7376 0ae9 0000 0000 2901 da0b 616e  .csv......)...an
-00000260: 6e6f 7461 7469 6f6e 7329 01da 0566 696c  notations)...fil
-00000270: 6573 2902 da09 6461 7461 636c 6173 73da  es)...dataclass.
-00000280: 0566 6965 6c64 2901 da04 456e 756d 4e63  .field)...EnumNc
-00000290: 0000 0000 0000 0000 0000 0000 0000 0000  ................
-000002a0: 0100 0000 4000 0001 7320 0000 0065 005a  ....@...s ...e.Z
-000002b0: 0164 005a 0264 015a 0364 025a 0464 035a  .d.Z.d.Z.d.Z.d.Z
-000002c0: 0564 045a 0664 055a 0764 0653 0029 07da  .d.Z.d.Z.d.S.)..
-000002d0: 0947 7261 6465 5479 7065 615e 0100 000a  .GradeTypea^....
-000002e0: 2020 2020 416e 2065 6e75 6d65 7261 7469      An enumerati
-000002f0: 6f6e 206f 6620 6772 6164 6520 7479 7065  on of grade type
-00000300: 2073 7472 696e 6720 636f 6e73 7461 6e74   string constant
-00000310: 732e 2050 726f 7669 6465 2061 2074 7970  s. Provide a typ
-00000320: 652d 7361 6665 2077 6179 206f 6620 7265  e-safe way of re
-00000330: 7072 6573 656e 7469 6e67 0a20 2020 2064  presenting.    d
-00000340: 6966 6665 7265 6e74 2067 7261 6465 2074  ifferent grade t
-00000350: 7970 6573 2e0a 0a20 2020 2041 7474 7269  ypes...    Attri
-00000360: 6275 7465 733a 0a20 2020 2020 2020 2046  butes:.        F
-00000370: 5f47 5241 4445 2028 7374 7229 3a20 5265  _GRADE (str): Re
-00000380: 7072 6573 656e 7473 2074 6865 2022 4622  presents the "F"
-00000390: 2067 7261 6465 2074 7970 650a 2020 2020   grade type.    
-000003a0: 2020 2020 4d47 5020 2873 7472 293a 2052      MGP (str): R
-000003b0: 6570 7265 7365 6e74 7320 7468 6520 224d  epresents the "M
-000003c0: 4750 2220 6772 6164 6520 7479 7065 0a20  GP" grade type. 
-000003d0: 2020 2020 2020 2047 4c55 4c41 4d20 2873         GLULAM (s
-000003e0: 7472 293a 2052 6570 7265 7365 6e74 7320  tr): Represents 
-000003f0: 7468 6520 2247 4c22 2067 7261 6465 2074  the "GL" grade t
-00000400: 7970 650a 2020 2020 2020 2020 415f 4752  ype.        A_GR
-00000410: 4144 4520 2873 7472 293a 2052 6570 7265  ADE (str): Repre
-00000420: 7365 6e74 7320 7468 6520 2241 2220 6772  sents the "A" gr
-00000430: 6164 6520 7479 7065 0a20 2020 20da 0146  ade type.    ..F
-00000440: da03 4d47 505a 0247 4cda 0141 4e29 08da  ..MGPZ.GL..AN)..
-00000450: 085f 5f6e 616d 655f 5fda 0a5f 5f6d 6f64  .__name__..__mod
-00000460: 756c 655f 5fda 0c5f 5f71 7561 6c6e 616d  ule__..__qualnam
-00000470: 655f 5fda 075f 5f64 6f63 5f5f da07 465f  e__..__doc__..F_
-00000480: 4752 4144 4572 0900 0000 da06 474c 554c  GRADEr......GLUL
-00000490: 414d da07 415f 4752 4144 45a9 0072 1200  AM..A_GRADE..r..
-000004a0: 0000 7212 0000 00fa 4563 3a5c 7573 6572  ..r.....Ec:\user
-000004b0: 735c 7571 6a67 6174 7461 5c64 6f63 756d  s\uqjgatta\docum
-000004c0: 656e 7473 5c67 6974 6875 625c 7469 6d62  ents\github\timb
-000004d0: 6572 2d61 735c 7372 635c 7469 6d62 6572  er-as\src\timber
-000004e0: 6173 5c6d 6174 6572 6961 6c2e 7079 7207  as\material.pyr.
-000004f0: 0000 0015 0000 0073 0c00 0000 0800 0401  .......s........
-00000500: 040b 0401 0401 0801 7207 0000 00da 0672  ........r......r
-00000510: 6574 7572 6efa 0c70 642e 4461 7461 4672  eturn..pd.DataFr
-00000520: 616d 6563 0000 0000 0000 0000 0000 0000  amec............
-00000530: 0000 0000 0500 0000 4300 0001 7314 0000  ........C...s...
-00000540: 0074 00a0 0174 0264 0183 01a0 0364 02a1  .t...t.d.....d..
-00000550: 01a1 0153 0029 0361 2801 0000 496d 706f  ...S.).a(...Impo
-00000560: 7274 7320 6120 6d61 7465 7269 616c 206c  rts a material l
-00000570: 6962 7261 7279 2066 726f 6d20 6120 4353  ibrary from a CS
-00000580: 5620 6669 6c65 2e0a 0a20 2020 2054 6865  V file...    The
-00000590: 2043 5356 2066 696c 6520 6973 206c 6f63   CSV file is loc
-000005a0: 6174 6564 2061 7420 2774 696d 6265 7261  ated at 'timbera
-000005b0: 732f 6461 7461 2f6d 6174 6572 6961 6c5f  s/data/material_
-000005c0: 6c69 6272 6172 792e 6373 7627 2e0a 0a20  library.csv'... 
-000005d0: 2020 2052 6574 7572 6e73 3a0a 2020 2020     Returns:.    
-000005e0: 2020 2020 7064 2e44 6174 6146 7261 6d65      pd.DataFrame
-000005f0: 3a20 4120 4461 7461 4672 616d 6520 636f  : A DataFrame co
-00000600: 6e74 6169 6e69 6e67 2074 6865 2063 6f6e  ntaining the con
-00000610: 7465 6e74 7320 6f66 2074 6865 206d 6174  tents of the mat
-00000620: 6572 6961 6c20 6c69 6272 6172 7920 4353  erial library CS
-00000630: 5620 6669 6c65 2e0a 0a20 2020 2052 6169  V file...    Rai
-00000640: 7365 733a 0a20 2020 2020 2020 2046 696c  ses:.        Fil
-00000650: 654e 6f74 466f 756e 6445 7272 6f72 3a20  eNotFoundError: 
-00000660: 4966 2074 6865 2043 5356 2066 696c 6520  If the CSV file 
-00000670: 646f 6573 206e 6f74 2065 7869 7374 2e0a  does not exist..
-00000680: 2020 2020 7a0d 7469 6d62 6572 6173 2e64      z.timberas.d
-00000690: 6174 617a 146d 6174 6572 6961 6c5f 6c69  ataz.material_li
-000006a0: 6272 6172 792e 6373 7629 04da 0270 64da  brary.csv)...pd.
-000006b0: 0872 6561 645f 6373 7672 0300 0000 da08  .read_csvr......
-000006c0: 6a6f 696e 7061 7468 7212 0000 0072 1200  joinpathr....r..
-000006d0: 0000 7212 0000 0072 1300 0000 da17 696d  ..r....r......im
-000006e0: 706f 7274 5f6d 6174 6572 6961 6c5f 6c69  port_material_li
-000006f0: 6272 6172 7927 0000 0073 0200 0000 140b  brary'...s......
-00000700: 7219 0000 0054 2901 da07 6b77 5f6f 6e6c  r....T)...kw_onl
-00000710: 7963 0000 0000 0000 0000 0000 0000 0000  yc..............
-00000720: 0000 0500 0000 4000 0001 7306 0100 0065  ......@...s....e
-00000730: 005a 0164 005a 0255 0064 015a 0364 025a  .Z.d.Z.U.d.Z.d.Z
-00000740: 0464 0365 0564 043c 0064 025a 0664 0365  .d.e.d.<.d.Z.d.e
-00000750: 0564 053c 0064 065a 0764 0765 0564 083c  .d.<.d.Z.d.e.d.<
-00000760: 0064 025a 0864 0365 0564 093c 0064 0a5a  .d.Z.d.e.d.<.d.Z
-00000770: 0964 0b65 0564 0c3c 0064 0a5a 0a64 0b65  .d.e.d.<.d.Z.d.e
-00000780: 0564 0d3c 0064 0a5a 0b64 0b65 0564 0e3c  .d.<.d.Z.d.e.d.<
-00000790: 0064 0a5a 0c64 0b65 0564 0f3c 0064 0a5a  .d.Z.d.e.d.<.d.Z
-000007a0: 0d64 0b65 0564 103c 0064 0a5a 0e64 0b65  .d.e.d.<.d.Z.d.e
-000007b0: 0564 113c 0064 0a5a 0f64 0b65 0564 123c  .d.<.d.Z.d.e.d.<
-000007c0: 0065 1064 0a64 1364 148d 025a 1164 0b65  .e.d.d.d...Z.d.e
-000007d0: 0564 153c 0065 1064 0a64 1364 148d 025a  .d.<.e.d.d.d...Z
-000007e0: 1264 0b65 0564 163c 0065 1064 0a64 1364  .d.e.d.<.e.d.d.d
-000007f0: 148d 025a 1364 0b65 0564 173c 0064 2c64  ...Z.d.e.d.<.d,d
-00000800: 1b64 1c84 045a 1464 2d64 2e64 2264 2384  .d...Z.d-d.d"d#.
-00000810: 055a 1565 1664 2f64 2664 2784 0483 015a  .Z.e.d/d&d'....Z
-00000820: 1765 1664 2d64 3064 2a64 2b84 0583 015a  .e.d-d0d*d+....Z
-00000830: 1864 1d53 0029 31da 0e54 696d 6265 724d  .d.S.)1..TimberM
-00000840: 6174 6572 6961 6c61 9603 0000 5265 7072  ateriala....Repr
-00000850: 6573 656e 7473 2074 696d 6265 7220 6d61  esents timber ma
-00000860: 7465 7269 616c 2070 726f 7065 7274 6965  terial propertie
-00000870: 7320 6173 2064 6566 696e 6564 2069 6e20  s as defined in 
-00000880: 4153 3137 3230 2e0a 0a20 2020 2041 7474  AS1720...    Att
-00000890: 7269 6275 7465 733a 0a20 2020 2020 2020  ributes:.       
-000008a0: 206e 616d 653a 2054 6865 206e 616d 6520   name: The name 
-000008b0: 6f66 2074 6865 2074 696d 6265 7220 6d61  of the timber ma
-000008c0: 7465 7269 616c 2e0a 2020 2020 2020 2020  terial..        
-000008d0: 6772 6164 653a 2054 6865 2067 7261 6465  grade: The grade
-000008e0: 206f 6620 7468 6520 7469 6d62 6572 206d   of the timber m
-000008f0: 6174 6572 6961 6c0a 2020 2020 2020 2020  aterial.        
-00000900: 7365 6173 6f6e 6564 2028 626f 6f6c 293a  seasoned (bool):
-00000910: 2041 2062 6f6f 6c65 616e 2069 6e64 6963   A boolean indic
-00000920: 6174 696e 6720 7768 6574 6865 7220 7468  ating whether th
-00000930: 6520 7469 6d62 6572 206d 6174 6572 6961  e timber materia
-00000940: 6c20 6973 2073 6561 736f 6e65 642e 0a20  l is seasoned.. 
-00000950: 2020 2020 2020 2067 7261 6465 5f74 7970         grade_typ
-00000960: 653a 2054 6865 2074 7970 6520 6f66 2074  e: The type of t
-00000970: 6865 2074 696d 6265 7220 6772 6164 652c  he timber grade,
-00000980: 2065 2e67 2046 2c20 4d47 502c 2047 4c2e   e.g F, MGP, GL.
-00000990: 0a20 2020 2020 2020 2066 5f62 3a20 4d61  .        f_b: Ma
-000009a0: 7465 7269 616c 2063 6861 7261 6374 6572  terial character
-000009b0: 6973 7469 6320 7374 7265 6e67 7468 2069  istic strength i
-000009c0: 6e20 6265 6e64 696e 672e 0a20 2020 2020  n bending..     
-000009d0: 2020 2066 5f74 3a20 4d61 7465 7269 616c     f_t: Material
-000009e0: 2063 6861 7261 6374 6572 6973 7469 6320   characteristic 
-000009f0: 7374 7265 6e67 7468 2069 6e20 7465 6e73  strength in tens
-00000a00: 696f 6e2e 0a20 2020 2020 2020 2066 5f73  ion..        f_s
-00000a10: 3a20 4d61 7465 7269 616c 2063 6861 7261  : Material chara
-00000a20: 6374 6572 6973 7469 6320 7374 7265 6e67  cteristic streng
-00000a30: 7468 2069 6e20 7368 6561 722e 0a20 2020  th in shear..   
-00000a40: 2020 2020 2066 5f63 3a20 4d61 7465 7269       f_c: Materi
-00000a50: 616c 2063 6861 7261 6374 6572 6973 7469  al characteristi
-00000a60: 6320 7374 7265 6e67 7468 2069 6e20 636f  c strength in co
-00000a70: 6d70 7265 7373 696f 6e2e 0a20 2020 2020  mpression..     
-00000a80: 2020 2045 3a20 4d61 7465 7269 616c 204d     E: Material M
-00000a90: 6f64 756c 7573 206f 6620 456c 6173 7469  odulus of Elasti
-00000aa0: 6369 7479 2e0a 2020 2020 2020 2020 473a  city..        G:
-00000ab0: 204d 6174 6572 6961 6c20 4d6f 6475 6c75   Material Modulu
-00000ac0: 7320 6f66 2052 6967 6964 6974 792e 0a20  s of Rigidity.. 
-00000ad0: 2020 2020 2020 2064 656e 7369 7479 3a20         density: 
-00000ae0: 4d61 7465 7269 616c 2064 656e 7369 7479  Material density
-00000af0: 2e0a 2020 2020 2020 2020 7068 695f 313a  ..        phi_1:
-00000b00: 2043 6170 6163 6974 7920 6661 6374 6f72   Capacity factor
-00000b10: 2066 6f72 2074 6865 206d 6174 6572 6961   for the materia
-00000b20: 6c20 666f 7220 6170 706c 6963 6174 696f  l for applicatio
-00000b30: 6e20 6361 7465 676f 7279 206f 6e65 2e0a  n category one..
-00000b40: 2020 2020 2020 2020 7068 695f 323a 2043          phi_2: C
-00000b50: 6170 6163 6974 7920 6661 6374 6f72 2066  apacity factor f
-00000b60: 6f72 2074 6865 206d 6174 6572 6961 6c20  or the material 
-00000b70: 666f 7220 6170 706c 6963 6174 696f 6e20  for application 
-00000b80: 6361 7465 676f 7279 2074 776f 2e0a 2020  category two..  
-00000b90: 2020 2020 2020 7068 695f 333a 2043 6170        phi_3: Cap
-00000ba0: 6163 6974 7920 6661 6374 6f72 2066 6f72  acity factor for
-00000bb0: 2074 6865 206d 6174 6572 6961 6c20 666f   the material fo
-00000bc0: 7220 6170 706c 6963 6174 696f 6e20 6361  r application ca
-00000bd0: 7465 676f 7279 2074 6872 6565 2e0a 2020  tegory three..  
-00000be0: 2020 da00 da03 7374 72da 046e 616d 65da    ....str..name.
-00000bf0: 0567 7261 6465 54da 0462 6f6f 6cda 0873  .gradeT..bool..s
-00000c00: 6561 736f 6e65 64da 0a67 7261 6465 5f74  easoned..grade_t
-00000c10: 7970 6572 0100 0000 da05 666c 6f61 74da  yper......float.
-00000c20: 0366 5f62 da03 665f 74da 0366 5f73 da03  .f_b..f_t..f_s..
-00000c30: 665f 63da 0145 da01 47da 0764 656e 7369  f_c..E..G..densi
-00000c40: 7479 4629 02da 0764 6566 6175 6c74 da04  tyF)...default..
-00000c50: 7265 7072 da05 7068 695f 31da 0570 6869  repr..phi_1..phi
-00000c60: 5f32 da05 7068 695f 33da 0f61 7070 6c69  _2..phi_3..appli
-00000c70: 6361 7469 6f6e 5f63 6174 da03 696e 7472  cation_cat..intr
-00000c80: 1400 0000 6302 0000 0000 0000 0000 0000  ....c...........
-00000c90: 0002 0000 0004 0000 0043 0000 0173 4000  .........C...s@.
-00000ca0: 0000 7c01 0400 6401 6b02 7209 0100 7c00  ..|...d.k.r...|.
-00000cb0: 6a00 5300 0400 6402 6b02 7211 0100 7c00  j.S...d.k.r...|.
-00000cc0: 6a01 5300 6403 6b02 7217 7c00 6a02 5300  j.S.d.k.r.|.j.S.
-00000cd0: 0900 7403 6404 7c01 9b00 6405 9d03 8301  ..t.d.|...d.....
-00000ce0: 8201 2906 6157 0100 0052 6574 7572 6e73  ..).aW...Returns
-00000cf0: 2074 6865 2061 7070 726f 7072 6961 7465   the appropriate
-00000d00: 2063 6170 6163 6974 7920 6661 6374 6f72   capacity factor
-00000d10: 2066 6f72 2074 6865 2067 6976 656e 2061   for the given a
-00000d20: 7070 6c69 6361 7469 6f6e 0a20 2020 2020  pplication.     
-00000d30: 2020 2063 6174 6567 6f72 792e 0a0a 2020     category...  
-00000d40: 2020 2020 2020 4172 6773 3a0a 2020 2020        Args:.    
-00000d50: 2020 2020 2020 2020 6170 706c 6963 6174          applicat
-00000d60: 696f 6e5f 6361 743a 2054 6865 2061 7070  ion_cat: The app
-00000d70: 6c69 6361 7469 6f6e 2063 6174 6567 6f72  lication categor
-00000d80: 792e 0a0a 2020 2020 2020 2020 5265 7475  y...        Retu
-00000d90: 726e 733a 0a20 2020 2020 2020 2020 2020  rns:.           
-00000da0: 2066 6c6f 6174 3a20 5468 6520 6361 7061   float: The capa
-00000db0: 6369 7479 2066 6163 746f 7220 666f 7220  city factor for 
-00000dc0: 7468 6520 6769 7665 6e20 6170 706c 6963  the given applic
-00000dd0: 6174 696f 6e20 6361 7465 676f 7279 2e0a  ation category..
-00000de0: 0a20 2020 2020 2020 2052 6169 7365 733a  .        Raises:
-00000df0: 0a20 2020 2020 2020 2020 2020 2056 616c  .            Val
-00000e00: 7565 4572 726f 723a 2049 6620 7468 6520  ueError: If the 
-00000e10: 6170 706c 6963 6174 696f 6e20 6361 7465  application cate
-00000e20: 676f 7279 2069 7320 6e6f 7420 7265 636f  gory is not reco
-00000e30: 676e 697a 6564 2e0a 2020 2020 2020 2020  gnized..        
-00000e40: e901 0000 00e9 0200 0000 e903 0000 007a  ...............z
-00000e50: 1541 7070 6c69 6361 7469 6f6e 2043 6174  .Application Cat
-00000e60: 6567 6f72 7920 7a10 206e 6f74 2072 6563  egory z. not rec
-00000e70: 6f67 6e69 7365 642e 2904 722d 0000 0072  ognised.).r-...r
-00000e80: 2e00 0000 722f 0000 00da 0a56 616c 7565  ....r/.....Value
-00000e90: 4572 726f 7229 02da 0473 656c 6672 3000  Error)...selfr0.
-00000ea0: 0000 7212 0000 0072 1200 0000 7213 0000  ..r....r....r...
-00000eb0: 00da 0370 6869 5900 0000 7316 0000 0002  ...phiY...s.....
-00000ec0: 0e0a 0106 010a 0106 0106 0106 0102 0102  ................
-00000ed0: 010a 0104 ff7a 1254 696d 6265 724d 6174  .....z.TimberMat
-00000ee0: 6572 6961 6c2e 7068 694e da01 64da 0162  erial.phiN..d..b
-00000ef0: fa0c 666c 6f61 7420 7c20 4e6f 6e65 da04  ..float | None..
-00000f00: 4e6f 6e65 6303 0000 0000 0000 0000 0000  Nonec...........
-00000f10: 0006 0000 0006 0000 0043 0000 0173 bc01  .........C...s..
-00000f20: 0000 7c00 6a00 7401 6a02 6b02 7256 7c01  ..|.j.t.j.k.rV|.
-00000f30: 6401 6b04 7256 7c01 0400 6402 6b02 7210  d.k.rV|...d.k.r.
-00000f40: 6e0c 0400 6403 6b02 7215 6e07 0400 6404  n...d.k.r.n...d.
-00000f50: 6b02 721a 6e02 0100 6e0b 0100 7c00 6a03  k.r.n...n...|.j.
-00000f60: 9b00 6405 7c01 9b00 6406 9d04 7d03 6e09  ..d.|...d...}.n.
-00000f70: 0900 7404 6407 7c01 9b00 6408 9d03 8301  ..t.d.|...d.....
-00000f80: 8201 7405 6409 7c00 6a03 9b00 640a 7c03  ..t.d.|.j...d.|.
-00000f90: 9b00 9d04 8301 0100 7c00 a006 7c03 a101  ........|...|...
-00000fa0: 7d03 7c03 6a03 7c00 5f03 7c03 6a07 7c00  }.|.j.|._.|.j.|.
-00000fb0: 5f07 7c03 6a08 7c00 5f08 7c03 6a09 7c00  _.|.j.|._.|.j.|.
-00000fc0: 5f09 7c03 6a0a 7c00 5f0a 6416 5300 7c00  _.|.j.|._.d.S.|.
-00000fd0: 6a00 7401 6a0b 6b02 72a0 7c01 640b 6b04  j.t.j.k.r.|.d.k.
-00000fe0: 727c 7c00 6a08 7d04 740c 7c00 6a08 640b  r||.j.}.t.|.j.d.
-00000ff0: 7c01 1b00 640c 1300 1400 640d 8302 7c00  |...d.....d...|.
-00001000: 5f08 7405 640e 7c04 9b00 640a 7c00 6a08  _.t.d.|...d.|.j.
-00001010: 9b00 640f 9d05 8301 0100 7c01 6410 6b04  ..d.......|.d.k.
-00001020: 729e 7c00 6a07 7d05 740c 7c00 6a07 6410  r.|.j.}.t.|.j.d.
-00001030: 7c01 1b00 640c 1300 1400 640d 8302 7c00  |...d.....d...|.
-00001040: 5f07 7405 6411 7c05 9b00 640a 7c00 6a07  _.t.d.|...d.|.j.
-00001050: 9b00 6412 9d05 8301 0100 6416 5300 6416  ..d.......d.S.d.
-00001060: 5300 7c00 6a00 7401 6a0d 6b02 72b2 7405  S.|.j.t.j.k.r.t.
-00001070: 6413 7c01 9b00 6414 7c02 9b00 9d04 8301  d.|...d.|.......
-00001080: 0100 740e 8201 7c00 6a00 7401 6a0f 6b02  ..t...|.j.t.j.k.
-00001090: 72da 7c01 640b 6b04 72dc 7c00 6a08 7d04  r.|.d.k.r.|.j.}.
-000010a0: 740c 7c00 6a08 640b 7c01 1b00 640c 1300  t.|.j.d.|...d...
-000010b0: 1400 640d 8302 7c00 5f08 7405 640e 7c04  ..d...|._.t.d.|.
-000010c0: 9b00 640a 7c00 6a08 9b00 6415 9d05 8301  ..d.|.j...d.....
-000010d0: 0100 6416 5300 6416 5300 6416 5300 2917  ..d.S.d.S.d.S.).
-000010e0: 6115 0200 0055 7064 6174 6573 2074 6865  a....Updates the
-000010f0: 2066 5f74 2070 726f 7065 7274 7920 666f   f_t property fo
-00001100: 7220 6c61 7267 6520 7365 6374 696f 6e73  r large sections
-00001110: 2c20 696e 636c 7564 696e 673a 0a20 2020  , including:.   
-00001120: 2020 2020 2020 2066 5f74 2c20 665f 622c         f_t, f_b,
-00001130: 2066 5f63 2c20 665f 7320 666f 7220 4d47   f_c, f_s for MG
-00001140: 5020 7365 6374 696f 6e73 2077 6974 6820  P sections with 
-00001150: 643e 3134 306d 6d20 2841 5331 3732 302e  d>140mm (AS1720.
-00001160: 3120 5461 626c 6520 4833 2e31 2c20 4e6f  1 Table H3.1, No
-00001170: 7465 2034 293b 0a20 2020 2020 2020 2020  te 4);.         
-00001180: 2066 5f62 2066 6f72 2046 2d67 7261 6465   f_b for F-grade
-00001190: 2073 6563 7469 6f6e 7320 7769 7468 2064   sections with d
-000011a0: 203e 2033 3030 6d6d 2028 4153 3137 3230   > 300mm (AS1720
-000011b0: 2e31 2054 6162 6c65 2048 322e 3120 4e6f  .1 Table H2.1 No
-000011c0: 7465 2031 293b 0a20 2020 2020 2020 2020  te 1);.         
-000011d0: 2066 5f74 2066 6f72 2046 2d67 7261 6465   f_t for F-grade
-000011e0: 2073 6563 7469 6f6e 7320 7769 7468 2064   sections with d
-000011f0: 203e 2031 3530 6d6d 2028 4153 3137 3230   > 150mm (AS1720
-00001200: 2e31 2054 6162 6c65 2048 2e32 204e 6f74  .1 Table H.2 Not
-00001210: 6520 3229 3b0a 2020 2020 2020 2020 2020  e 2);.          
-00001220: 665f 7420 666f 7220 476c 756c 616d 2073  f_t for Glulam s
-00001230: 6563 7469 6f6e 7320 7769 7468 2064 203e  ections with d >
-00001240: 2031 3530 6d6d 2020 2841 5331 3732 302e   150mm  (AS1720.
-00001250: 3120 5461 626c 6520 372e 3120 4e6f 7465  1 Table 7.1 Note
-00001260: 2031 292e 0a0a 2020 2020 2020 2020 4172   1)...        Ar
-00001270: 6773 3a0a 2020 2020 2020 2020 2020 2020  gs:.            
-00001280: 643a 2054 6865 2064 6570 7468 206f 6620  d: The depth of 
-00001290: 7468 6520 7469 6d62 6572 2073 6563 7469  the timber secti
-000012a0: 6f6e 2e0a 2020 2020 2020 2020 2020 2020  on..            
-000012b0: 623a 2054 6865 2062 7265 6164 7468 206f  b: The breadth o
-000012c0: 6620 7468 6520 7469 6d62 6572 2073 6563  f the timber sec
-000012d0: 7469 6f6e 2028 7265 7175 6972 6564 2066  tion (required f
-000012e0: 6f72 2041 3137 206d 6174 6572 6961 6c29  or A17 material)
-000012f0: 2e0a 2020 2020 2020 2020 e98c 0000 00e9  ..        ......
-00001300: be00 0000 e9f0 0000 0069 2201 0000 fa01  .........i".....
-00001310: 207a 086d 6d20 6465 7074 687a 0e53 6563   z.mm depthz.Sec
-00001320: 7469 6f6e 2064 6570 7468 207a 5620 3e20  tion depth zV > 
-00001330: 3134 306d 6d2c 2070 6c65 6173 6520 696e  140mm, please in
-00001340: 7465 7270 6f6c 6174 6520 6d61 7465 7269  terpolate materi
-00001350: 616c 2070 726f 7065 7274 6965 7320 666f  al properties fo
-00001360: 7220 4d47 5020 7365 6374 696f 6e20 2874  r MGP section (t
-00001370: 6162 6c65 2048 332e 312c 204e 6f74 6520  able H3.1, Note 
-00001380: 3429 2e7a 164d 6174 6572 6961 6c20 6368  4).z.Material ch
-00001390: 616e 6765 6420 6672 6f6d 207a 0420 746f  anged from z. to
-000013a0: 20e9 9600 0000 67c7 4b37 8941 60c5 3f72   .....g.K7.A`.?r
-000013b0: 3400 0000 7a22 5465 6e73 696c 6520 7374  4...z"Tensile st
-000013c0: 7265 6e67 7468 2066 5f74 2063 6861 6e67  rength f_t chang
-000013d0: 6564 2066 726f 6d20 7a26 2064 7565 2074  ed from z& due t
-000013e0: 6f20 7365 6374 696f 6e20 7369 7a65 2c20  o section size, 
-000013f0: 5461 626c 6520 482e 3220 4e6f 7465 2032  Table H.2 Note 2
-00001400: 692c 0100 007a 2242 656e 6469 6e67 2073  i,...z"Bending s
-00001410: 7472 656e 6774 6820 665f 6220 6368 616e  trength f_b chan
-00001420: 6765 6420 6672 6f6d 207a 2620 6475 6520  ged from z& due 
-00001430: 746f 2073 6563 7469 6f6e 2073 697a 652c  to section size,
-00001440: 2054 6162 6c65 2048 2e32 204e 6f74 6520   Table H.2 Note 
-00001450: 317a 0972 6571 7569 7265 7320 7a05 2061  1z.requires z. a
-00001460: 6e64 207a 2420 6475 6520 746f 2073 6563  nd z$ due to sec
-00001470: 7469 6f6e 2073 697a 652c 2054 6162 6c65  tion size, Table
-00001480: 2037 2e31 204e 6f74 654e 2910 7222 0000   7.1 NoteN).r"..
-00001490: 0072 0700 0000 7209 0000 0072 1e00 0000  .r....r....r....
-000014a0: 7235 0000 00da 0570 7269 6e74 da0c 6672  r5.....print..fr
-000014b0: 6f6d 5f6c 6962 7261 7279 7224 0000 0072  om_libraryr$...r
-000014c0: 2500 0000 7227 0000 0072 2600 0000 720f  %...r'...r&...r.
-000014d0: 0000 00da 0572 6f75 6e64 7211 0000 00da  .....roundr.....
-000014e0: 134e 6f74 496d 706c 656d 656e 7465 6445  .NotImplementedE
-000014f0: 7272 6f72 7210 0000 0029 0672 3600 0000  rrorr....).r6...
-00001500: 7238 0000 0072 3900 0000 5a07 6e65 775f  r8...r9...Z.new_
-00001510: 6d61 745a 0c6f 7269 6769 6e61 6c5f 665f  matZ.original_f_
-00001520: 745a 0c6f 7269 6769 6e61 6c5f 665f 6272  tZ.original_f_br
-00001530: 1200 0000 7212 0000 0072 1300 0000 da18  ....r....r......
-00001540: 7570 6461 7465 5f66 726f 6d5f 7365 6374  update_from_sect
-00001550: 696f 6e5f 7369 7a65 7300 0000 734e 0000  ion_sizes...sN..
-00001560: 0014 0b02 0124 0114 0102 0102 010a 0104  .....$..........
-00001570: ff16 040a 0108 0108 0108 0108 010c 010c  ................
-00001580: 0208 0106 021a 0102 0112 0104 ff08 0406  ................
-00001590: 021a 0102 0112 0108 ff04 fc0c 0814 0104  ................
-000015a0: 0114 0206 021a 0102 0112 0108 ff08 fc7a  ...............z
-000015b0: 2754 696d 6265 724d 6174 6572 6961 6c2e  'TimberMaterial.
-000015c0: 7570 6461 7465 5f66 726f 6d5f 7365 6374  update_from_sect
-000015d0: 696f 6e5f 7369 7a65 da0a 696e 7075 745f  ion_size..input_
-000015e0: 6469 6374 da04 6469 6374 6302 0000 0000  dict..dictc.....
-000015f0: 0000 0000 0000 0003 0000 0004 0000 0003  ................
-00001600: 0000 0173 2e00 0000 7c00 6a00 a001 a100  ...s....|.j.....
-00001610: 8900 8700 6601 6401 6402 8408 7c01 a002  ....f.d.d...|...
-00001620: a100 4400 8301 7d02 7c00 6404 6900 7c02  ..D...}.|.d.i.|.
-00001630: a401 8e01 5300 2905 6181 0100 0043 7265  ....S.).a....Cre
-00001640: 6174 6520 6120 5469 6d62 6572 4d61 7465  ate a TimberMate
-00001650: 7269 616c 2062 7920 6469 7265 6374 6c79  rial by directly
-00001660: 2070 6f70 756c 6174 696e 6720 6174 7472   populating attr
-00001670: 6962 7574 6573 2066 726f 6d20 696e 7075  ibutes from inpu
-00001680: 7420 6469 6374 696f 6e61 7279 2c0a 2020  t dictionary,.  
-00001690: 2020 2020 2020 6967 6e6f 7269 6e67 2064        ignoring d
-000016a0: 6963 7469 6f6e 6172 7920 6b65 7973 2077  ictionary keys w
-000016b0: 6869 6368 2061 7265 6e27 7420 636c 6173  hich aren't clas
-000016c0: 7320 6174 7472 6962 7574 6573 2e0a 0a20  s attributes... 
-000016d0: 2020 2020 2020 2041 7267 733a 0a20 2020         Args:.   
-000016e0: 2020 2020 2020 2020 2069 6e70 7574 5f64           input_d
-000016f0: 6963 743a 204b 6579 2d76 616c 7565 2070  ict: Key-value p
-00001700: 6169 7273 2074 6f20 6465 6669 6e65 2074  airs to define t
-00001710: 6865 2074 696d 6265 7220 6d61 7465 7269  he timber materi
-00001720: 616c 2c20 6b65 7973 2063 6f72 7265 7370  al, keys corresp
-00001730: 6f6e 6469 6e67 2074 6f20 636c 6173 730a  onding to class.
-00001740: 2020 2020 2020 2020 2020 2020 6174 7472              attr
-00001750: 6962 7574 6520 6e61 6d65 7320 7769 6c6c  ibute names will
-00001760: 2062 6520 7570 6461 7465 640a 0a20 2020   be updated..   
-00001770: 2020 2020 2052 6574 7572 6e73 3a0a 2020       Returns:.  
-00001780: 2020 2020 2020 2020 2020 5469 6d62 6572            Timber
-00001790: 4d61 7465 7269 616c 3a20 5468 6520 7469  Material: The ti
-000017a0: 6d62 6572 206d 6174 6572 6961 6c20 6f62  mber material ob
-000017b0: 6a65 6374 2e0a 2020 2020 2020 2020 6301  ject..        c.
-000017c0: 0000 0000 0000 0000 0000 0003 0000 0004  ................
-000017d0: 0000 0013 0000 0173 1e00 0000 6900 7c00  .......s....i.|.
-000017e0: 5d0b 5c02 7d01 7d02 7c01 8800 7600 7202  ].\.}.}.|...v.r.
-000017f0: 7c01 7c02 9302 7102 5300 7212 0000 0072  |.|...q.S.r....r
-00001800: 1200 0000 2903 da02 2e30 da01 6bda 0176  ....)....0..k..v
-00001810: a901 da0a 7661 6c69 645f 6b65 7973 7212  ....valid_keysr.
-00001820: 0000 0072 1300 0000 da0a 3c64 6963 7463  ...r......<dictc
-00001830: 6f6d 703e bd00 0000 7302 0000 001e 007a  omp>....s......z
-00001840: 2c54 696d 6265 724d 6174 6572 6961 6c2e  ,TimberMaterial.
-00001850: 6672 6f6d 5f64 6963 742e 3c6c 6f63 616c  from_dict.<local
-00001860: 733e 2e3c 6469 6374 636f 6d70 3e4e 7212  s>.<dictcomp>Nr.
-00001870: 0000 0029 03da 0f5f 5f61 6e6e 6f74 6174  ...)...__annotat
-00001880: 696f 6e73 5f5f da04 6b65 7973 da05 6974  ions__..keys..it
-00001890: 656d 7329 03da 0363 6c73 7246 0000 00da  ems)...clsrF....
-000018a0: 0a76 616c 6964 5f64 6963 7472 1200 0000  .valid_dictr....
-000018b0: 724b 0000 0072 1300 0000 da09 6672 6f6d  rK...r......from
-000018c0: 5f64 6963 74ad 0000 0073 0600 0000 0a0e  _dict....s......
-000018d0: 1602 0e02 7a18 5469 6d62 6572 4d61 7465  ....z.TimberMate
-000018e0: 7269 616c 2e66 726f 6d5f 6469 6374 da07  rial.from_dict..
-000018f0: 6c69 6272 6172 79fa 1370 642e 4461 7461  library..pd.Data
-00001900: 4672 616d 6520 7c20 4e6f 6e65 6303 0000  Frame | Nonec...
-00001910: 0000 0000 0000 0000 0005 0000 0003 0000  ................
-00001920: 0043 0000 0173 3a00 0000 7c02 6401 7500  .C...s:...|.d.u.
-00001930: 7207 7400 8300 7d02 7c02 6a01 7c02 6402  r.t...}.|.j.|.d.
-00001940: 1900 7c01 6b02 1900 7d03 7c03 6a02 6403  ..|.k...}.|.j.d.
-00001950: 6404 8d01 6405 1900 7d04 7c00 a003 7c04  d...d...}.|...|.
-00001960: a101 5300 2906 61b5 0100 0043 7265 6174  ..S.).a....Creat
-00001970: 6573 2061 2054 696d 6265 724d 6174 6572  es a TimberMater
-00001980: 6961 6c20 6f62 6a65 6374 2066 726f 6d20  ial object from 
-00001990: 6120 6d61 7465 7269 616c 206c 6962 7261  a material libra
-000019a0: 7279 2028 4461 7461 4672 616d 6529 2e0a  ry (DataFrame)..
-000019b0: 0a20 2020 2020 2020 2041 7267 733a 0a20  .        Args:. 
-000019c0: 2020 2020 2020 2020 2020 206e 616d 653a             name:
-000019d0: 2054 6865 206e 616d 6520 6f66 2074 6865   The name of the
-000019e0: 2074 696d 6265 7220 6d61 7465 7269 616c   timber material
-000019f0: 2074 6f20 6c6f 6f6b 7570 2069 6e20 7468   to lookup in th
-00001a00: 6520 6c69 6272 6172 7920 2869 6e20 276e  e library (in 'n
-00001a10: 616d 6527 2063 6f6c 756d 6e29 0a20 2020  ame' column).   
-00001a20: 2020 2020 2020 2020 206c 6962 7261 7279           library
-00001a30: 2028 7064 2e44 6174 6146 7261 6d65 2c20   (pd.DataFrame, 
-00001a40: 6f70 7469 6f6e 616c 293a 2054 6865 2044  optional): The D
-00001a50: 6174 6146 7261 6d65 206f 6620 7468 6520  ataFrame of the 
-00001a60: 6c69 6272 6172 7920 6f66 2074 696d 6265  library of timbe
-00001a70: 7220 6d61 7465 7269 616c 732e 0a20 2020  r materials..   
-00001a80: 2020 2020 2020 2020 2020 2020 2049 6620               If 
-00001a90: 6e6f 7420 7072 6f76 6964 6564 2c20 7468  not provided, th
-00001aa0: 6520 6465 6661 756c 7420 6c69 6272 6172  e default librar
-00001ab0: 7920 604d 4154 4552 4941 4c5f 4c49 4252  y `MATERIAL_LIBR
-00001ac0: 4152 5960 2069 7320 7573 6564 2e0a 0a20  ARY` is used... 
-00001ad0: 2020 2020 2020 2052 6574 7572 6e73 3a0a         Returns:.
-00001ae0: 2020 2020 2020 2020 2020 2020 5469 6d62              Timb
-00001af0: 6572 4d61 7465 7269 616c 3a20 5468 6520  erMaterial: The 
-00001b00: 7469 6d62 6572 206d 6174 6572 6961 6c20  timber material 
-00001b10: 6f62 6a65 6374 2e0a 2020 2020 2020 2020  object..        
-00001b20: 4e72 1e00 0000 da07 7265 636f 7264 7329  Nr......records)
-00001b30: 01da 066f 7269 656e 7472 0100 0000 2904  ...orientr....).
-00001b40: 7219 0000 00da 036c 6f63 da07 746f 5f64  r......loc..to_d
-00001b50: 6963 7472 5300 0000 2905 7251 0000 0072  ictrS...).rQ...r
-00001b60: 1e00 0000 7254 0000 00da 086d 6174 6572  ....rT.....mater
-00001b70: 6961 6c5a 086d 6174 5f64 6963 7472 1200  ialZ.mat_dictr..
-00001b80: 0000 7212 0000 0072 1300 0000 7242 0000  ..r....r....rB..
-00001b90: 00c1 0000 0073 0a00 0000 080c 0601 1201  .....s..........
-00001ba0: 1001 0a01 7a1b 5469 6d62 6572 4d61 7465  ....z.TimberMate
-00001bb0: 7269 616c 2e66 726f 6d5f 6c69 6272 6172  rial.from_librar
-00001bc0: 7929 0472 3000 0000 7231 0000 0072 1400  y).r0...r1...r..
-00001bd0: 0000 7223 0000 0029 014e 2906 7238 0000  ..r#...).N).r8..
-00001be0: 0072 2300 0000 7239 0000 0072 3a00 0000  .r#...r9...r:...
-00001bf0: 7214 0000 0072 3b00 0000 2904 7246 0000  r....r;...).rF..
-00001c00: 0072 4700 0000 7214 0000 0072 1b00 0000  .rG...r....r....
-00001c10: 2904 721e 0000 0072 1d00 0000 7254 0000  ).r....r....rT..
-00001c20: 0072 5500 0000 2919 720b 0000 0072 0c00  .rU...).r....r..
-00001c30: 0000 720d 0000 0072 0e00 0000 721e 0000  ..r....r....r...
-00001c40: 0072 4e00 0000 721f 0000 0072 2100 0000  .rN...r....r!...
-00001c50: 7222 0000 0072 2400 0000 7225 0000 0072  r"...r$...r%...r
-00001c60: 2600 0000 7227 0000 0072 2800 0000 7229  &...r'...r(...r)
-00001c70: 0000 0072 2a00 0000 7205 0000 0072 2d00  ...r*...r....r-.
-00001c80: 0000 722e 0000 0072 2f00 0000 7237 0000  ..r....r/...r7..
-00001c90: 0072 4500 0000 da0b 636c 6173 736d 6574  .rE.....classmet
-00001ca0: 686f 6472 5300 0000 7242 0000 0072 1200  hodrS...rB...r..
-00001cb0: 0000 7212 0000 0072 1200 0000 7213 0000  ..r....r....r...
-00001cc0: 0072 1b00 0000 3500 0000 732c 0000 000a  .r....5...s,....
-00001cd0: 0004 020c 130c 010c 010c 010c 010c 010c  ................
-00001ce0: 010c 010c 010c 010c 0114 0114 0114 010a  ................
-00001cf0: 020c 1a02 3a0c 0102 1312 0172 1b00 0000  ....:......r....
-00001d00: 6300 0000 0000 0000 0000 0000 0002 0000  c...............
-00001d10: 0004 0000 0043 0000 0173 2800 0000 7400  .....C...s(...t.
-00001d20: 8300 7d00 7401 a002 6401 a101 7d01 7401  ..}.t...d...}.t.
-00001d30: a002 6401 7c00 a102 7d01 7403 7c01 8301  ..d.|...}.t.|...
-00001d40: 0100 6402 5300 2903 7a0b 4d61 696e 2053  ..d.S.).z.Main S
-00001d50: 6372 6970 745a 054d 4750 3130 4e29 0472  criptZ.MGP10N).r
-00001d60: 1900 0000 721b 0000 0072 4200 0000 7241  ....r....rB...rA
-00001d70: 0000 0029 025a 106d 6174 6572 6961 6c5f  ...).Z.material_
-00001d80: 6c69 6272 6172 795a 056d 6770 3130 7212  libraryZ.mgp10r.
-00001d90: 0000 0072 1200 0000 7213 0000 00da 046d  ...r....r......m
-00001da0: 6169 6ed4 0000 0073 0800 0000 0602 0a01  ain....s........
-00001db0: 0c01 0c01 725c 0000 00da 085f 5f6d 6169  ....r\.....__mai
-00001dc0: 6e5f 5f29 0272 1400 0000 7215 0000 0029  n__).r....r....)
-00001dd0: 1272 0e00 0000 da0a 5f5f 6675 7475 7265  .r......__future
-00001de0: 5f5f 7202 0000 00da 1369 6d70 6f72 746c  __r......importl
-00001df0: 6962 2e72 6573 6f75 7263 6573 7203 0000  ib.resourcesr...
-00001e00: 00da 0b64 6174 6163 6c61 7373 6573 7204  ...dataclassesr.
-00001e10: 0000 0072 0500 0000 da04 656e 756d 7206  ...r......enumr.
-00001e20: 0000 00da 0670 616e 6461 7372 1600 0000  .....pandasr....
-00001e30: 721d 0000 0072 0700 0000 7219 0000 0072  r....r....r....r
-00001e40: 1b00 0000 725c 0000 0072 0b00 0000 7212  ....r\...r....r.
-00001e50: 0000 0072 1200 0000 7212 0000 0072 1300  ...r....r....r..
-00001e60: 0000 da08 3c6d 6f64 756c 653e 0100 0000  ....<module>....
-00001e70: 731e 0000 0004 000c 0d0c 0110 010c 0108  s...............
-00001e80: 0112 030a 1208 0e10 0100 7f08 1f08 080a  ................
-00001e90: 0104 ff                                  ...
+00000040: 6403 6c03 5a03 6401 6404 6c04 6d05 5a05  d.l.Z.d.d.l.m.Z.
+00000050: 6d06 5a06 0100 6401 6405 6c07 6d08 5a08  m.Z...d.d.l.m.Z.
+00000060: 0100 6401 6403 6c09 5a0a 4700 6406 6407  ..d.d.l.Z.G.d.d.
+00000070: 8400 6407 650b 6508 8304 5a0c 6413 640a  ..d.e.e...Z.d.d.
+00000080: 640b 8404 5a0d 6505 640c 640d 8d01 4700  d...Z.e.d.d...G.
+00000090: 640e 640f 8400 640f 8302 8301 5a0e 6410  d.d...d.....Z.d.
+000000a0: 6411 8400 5a0f 6510 6412 6b02 7245 650f  d...Z.e.d.k.rEe.
+000000b0: 8300 0100 6403 5300 6403 5300 2914 6187  ....d.S.d.S.).a.
+000000c0: 0100 000a 5468 6973 206d 6f64 756c 6520  ....This module 
+000000d0: 7072 6f76 6964 6573 2063 6c61 7373 6573  provides classes
+000000e0: 2061 6e64 2066 756e 6374 696f 6e73 2066   and functions f
+000000f0: 6f72 2063 7265 6174 696e 6720 7469 6d62  or creating timb
+00000100: 6572 206d 6174 6572 6961 6c73 200a 6465  er materials .de
+00000110: 7363 7269 6265 6420 696e 2041 5331 3732  scribed in AS172
+00000120: 302e 312e 200a 0a43 6c61 7373 6573 3a0a  0.1. ..Classes:.
+00000130: 2020 2020 4772 6164 6554 7970 653a 2045      GradeType: E
+00000140: 6e75 6d20 636c 6173 7320 6465 6669 6e69  num class defini
+00000150: 6e67 206d 6174 6572 6961 6c20 6772 6164  ng material grad
+00000160: 6520 7374 7269 6e67 2063 6f6e 7374 616e  e string constan
+00000170: 7473 2e20 0a0a 2020 2020 5469 6d62 6572  ts. ..    Timber
+00000180: 4d61 7465 7269 616c 3a20 5265 7072 6573  Material: Repres
+00000190: 656e 7473 2061 2074 696d 6265 7220 6d61  ents a timber ma
+000001a0: 7465 7269 616c 2062 6173 6564 206f 6e20  terial based on 
+000001b0: 4153 3137 3230 2e20 0a0a 4675 6e63 7469  AS1720. ..Functi
+000001c0: 6f6e 733a 0a20 2020 2069 6d70 6f72 745f  ons:.    import_
+000001d0: 6d61 7465 7269 616c 5f6c 6962 7261 7279  material_library
+000001e0: 2829 3a20 5265 7475 726e 7320 6120 4461  (): Returns a Da
+000001f0: 7461 4672 616d 6520 636f 6e74 6169 6e69  taFrame containi
+00000200: 6e67 2074 6865 206d 6174 6572 6961 6c20  ng the material 
+00000210: 6c69 6272 6172 7920 6465 6669 6e65 640a  library defined.
+00000220: 2020 2020 696e 2074 696d 6265 7261 732f      in timberas/
+00000230: 6461 7461 2f6d 6174 6572 6961 6c5f 6c69  data/material_li
+00000240: 6272 6172 792e 6373 760a e900 0000 0029  brary.csv......)
+00000250: 01da 0b61 6e6e 6f74 6174 696f 6e73 4e29  ...annotationsN)
+00000260: 02da 0964 6174 6163 6c61 7373 da05 6669  ...dataclass..fi
+00000270: 656c 6429 01da 0445 6e75 6d63 0000 0000  eld)...Enumc....
+00000280: 0000 0000 0000 0000 0000 0000 0100 0000  ................
+00000290: 4000 0001 7320 0000 0065 005a 0164 005a  @...s ...e.Z.d.Z
+000002a0: 0264 015a 0364 025a 0464 035a 0564 045a  .d.Z.d.Z.d.Z.d.Z
+000002b0: 0664 055a 0764 0653 0029 07da 0947 7261  .d.Z.d.S.)...Gra
+000002c0: 6465 5479 7065 615e 0100 000a 2020 2020  deTypea^....    
+000002d0: 416e 2065 6e75 6d65 7261 7469 6f6e 206f  An enumeration o
+000002e0: 6620 6772 6164 6520 7479 7065 2073 7472  f grade type str
+000002f0: 696e 6720 636f 6e73 7461 6e74 732e 2050  ing constants. P
+00000300: 726f 7669 6465 2061 2074 7970 652d 7361  rovide a type-sa
+00000310: 6665 2077 6179 206f 6620 7265 7072 6573  fe way of repres
+00000320: 656e 7469 6e67 0a20 2020 2064 6966 6665  enting.    diffe
+00000330: 7265 6e74 2067 7261 6465 2074 7970 6573  rent grade types
+00000340: 2e0a 0a20 2020 2041 7474 7269 6275 7465  ...    Attribute
+00000350: 733a 0a20 2020 2020 2020 2046 5f47 5241  s:.        F_GRA
+00000360: 4445 2028 7374 7229 3a20 5265 7072 6573  DE (str): Repres
+00000370: 656e 7473 2074 6865 2022 4622 2067 7261  ents the "F" gra
+00000380: 6465 2074 7970 650a 2020 2020 2020 2020  de type.        
+00000390: 4d47 5020 2873 7472 293a 2052 6570 7265  MGP (str): Repre
+000003a0: 7365 6e74 7320 7468 6520 224d 4750 2220  sents the "MGP" 
+000003b0: 6772 6164 6520 7479 7065 0a20 2020 2020  grade type.     
+000003c0: 2020 2047 4c55 4c41 4d20 2873 7472 293a     GLULAM (str):
+000003d0: 2052 6570 7265 7365 6e74 7320 7468 6520   Represents the 
+000003e0: 2247 4c22 2067 7261 6465 2074 7970 650a  "GL" grade type.
+000003f0: 2020 2020 2020 2020 415f 4752 4144 4520          A_GRADE 
+00000400: 2873 7472 293a 2052 6570 7265 7365 6e74  (str): Represent
+00000410: 7320 7468 6520 2241 2220 6772 6164 6520  s the "A" grade 
+00000420: 7479 7065 0a20 2020 20da 0146 da03 4d47  type.    ..F..MG
+00000430: 505a 0247 4cda 0141 4e29 08da 085f 5f6e  PZ.GL..AN)...__n
+00000440: 616d 655f 5fda 0a5f 5f6d 6f64 756c 655f  ame__..__module_
+00000450: 5fda 0c5f 5f71 7561 6c6e 616d 655f 5fda  _..__qualname__.
+00000460: 075f 5f64 6f63 5f5f da07 465f 4752 4144  .__doc__..F_GRAD
+00000470: 4572 0800 0000 da06 474c 554c 414d da07  Er......GLULAM..
+00000480: 415f 4752 4144 45a9 0072 1100 0000 7211  A_GRADE..r....r.
+00000490: 0000 00fa 4563 3a5c 7573 6572 735c 7571  ....Ec:\users\uq
+000004a0: 6a67 6174 7461 5c64 6f63 756d 656e 7473  jgatta\documents
+000004b0: 5c67 6974 6875 625c 7469 6d62 6572 2d61  \github\timber-a
+000004c0: 735c 7372 635c 7469 6d62 6572 6173 5c6d  s\src\timberas\m
+000004d0: 6174 6572 6961 6c2e 7079 7206 0000 0015  aterial.pyr.....
+000004e0: 0000 0073 0c00 0000 0800 0401 040b 0401  ...s............
+000004f0: 0401 0801 7206 0000 00da 0672 6574 7572  ....r......retur
+00000500: 6efa 0c70 642e 4461 7461 4672 616d 6563  n..pd.DataFramec
+00000510: 0000 0000 0000 0000 0000 0000 0200 0000  ................
+00000520: 0400 0000 4300 0001 7324 0000 0074 006a  ....C...s$...t.j
+00000530: 01a0 0274 03a1 017d 0074 006a 01a0 047c  ...t...}.t.j...|
+00000540: 0064 01a1 027d 0174 05a0 067c 01a1 0153  .d...}.t...|...S
+00000550: 0029 0261 2801 0000 496d 706f 7274 7320  .).a(...Imports 
+00000560: 6120 6d61 7465 7269 616c 206c 6962 7261  a material libra
+00000570: 7279 2066 726f 6d20 6120 4353 5620 6669  ry from a CSV fi
+00000580: 6c65 2e0a 0a20 2020 2054 6865 2043 5356  le...    The CSV
+00000590: 2066 696c 6520 6973 206c 6f63 6174 6564   file is located
+000005a0: 2061 7420 2774 696d 6265 7261 732f 6461   at 'timberas/da
+000005b0: 7461 2f6d 6174 6572 6961 6c5f 6c69 6272  ta/material_libr
+000005c0: 6172 792e 6373 7627 2e0a 0a20 2020 2052  ary.csv'...    R
+000005d0: 6574 7572 6e73 3a0a 2020 2020 2020 2020  eturns:.        
+000005e0: 7064 2e44 6174 6146 7261 6d65 3a20 4120  pd.DataFrame: A 
+000005f0: 4461 7461 4672 616d 6520 636f 6e74 6169  DataFrame contai
+00000600: 6e69 6e67 2074 6865 2063 6f6e 7465 6e74  ning the content
+00000610: 7320 6f66 2074 6865 206d 6174 6572 6961  s of the materia
+00000620: 6c20 6c69 6272 6172 7920 4353 5620 6669  l library CSV fi
+00000630: 6c65 2e0a 0a20 2020 2052 6169 7365 733a  le...    Raises:
+00000640: 0a20 2020 2020 2020 2046 696c 654e 6f74  .        FileNot
+00000650: 466f 756e 6445 7272 6f72 3a20 4966 2074  FoundError: If t
+00000660: 6865 2043 5356 2066 696c 6520 646f 6573  he CSV file does
+00000670: 206e 6f74 2065 7869 7374 2e0a 2020 2020   not exist..    
+00000680: 7a19 6461 7461 2f6d 6174 6572 6961 6c5f  z.data/material_
+00000690: 6c69 6272 6172 792e 6373 7629 07da 026f  library.csv)...o
+000006a0: 73da 0470 6174 68da 0764 6972 6e61 6d65  s..path..dirname
+000006b0: da08 5f5f 6669 6c65 5f5f da04 6a6f 696e  ..__file__..join
+000006c0: da02 7064 da08 7265 6164 5f63 7376 2902  ..pd..read_csv).
+000006d0: da03 6377 64da 086c 6962 5f70 6174 6872  ..cwd..lib_pathr
+000006e0: 1100 0000 7211 0000 0072 1200 0000 da17  ....r....r......
+000006f0: 696d 706f 7274 5f6d 6174 6572 6961 6c5f  import_material_
+00000700: 6c69 6272 6172 7927 0000 0073 0600 0000  library'...s....
+00000710: 0c0c 0e01 0a01 721e 0000 0054 2901 da07  ......r....T)...
+00000720: 6b77 5f6f 6e6c 7963 0000 0000 0000 0000  kw_onlyc........
+00000730: 0000 0000 0000 0000 0500 0000 4000 0001  ............@...
+00000740: 7306 0100 0065 005a 0164 005a 0255 0064  s....e.Z.d.Z.U.d
+00000750: 015a 0364 025a 0464 0365 0564 043c 0064  .Z.d.Z.d.e.d.<.d
+00000760: 025a 0664 0365 0564 053c 0064 065a 0764  .Z.d.e.d.<.d.Z.d
+00000770: 0765 0564 083c 0064 025a 0864 0365 0564  .e.d.<.d.Z.d.e.d
+00000780: 093c 0064 0a5a 0964 0b65 0564 0c3c 0064  .<.d.Z.d.e.d.<.d
+00000790: 0a5a 0a64 0b65 0564 0d3c 0064 0a5a 0b64  .Z.d.e.d.<.d.Z.d
+000007a0: 0b65 0564 0e3c 0064 0a5a 0c64 0b65 0564  .e.d.<.d.Z.d.e.d
+000007b0: 0f3c 0064 0a5a 0d64 0b65 0564 103c 0064  .<.d.Z.d.e.d.<.d
+000007c0: 0a5a 0e64 0b65 0564 113c 0064 0a5a 0f64  .Z.d.e.d.<.d.Z.d
+000007d0: 0b65 0564 123c 0065 1064 0a64 1364 148d  .e.d.<.e.d.d.d..
+000007e0: 025a 1164 0b65 0564 153c 0065 1064 0a64  .Z.d.e.d.<.e.d.d
+000007f0: 1364 148d 025a 1264 0b65 0564 163c 0065  .d...Z.d.e.d.<.e
+00000800: 1064 0a64 1364 148d 025a 1364 0b65 0564  .d.d.d...Z.d.e.d
+00000810: 173c 0064 2c64 1b64 1c84 045a 1464 2d64  .<.d,d.d...Z.d-d
+00000820: 2e64 2264 2384 055a 1565 1664 2f64 2664  .d"d#..Z.e.d/d&d
+00000830: 2784 0483 015a 1765 1664 2d64 3064 2a64  '....Z.e.d-d0d*d
+00000840: 2b84 0583 015a 1864 1d53 0029 31da 0e54  +....Z.d.S.)1..T
+00000850: 696d 6265 724d 6174 6572 6961 6c61 9603  imberMateriala..
+00000860: 0000 5265 7072 6573 656e 7473 2074 696d  ..Represents tim
+00000870: 6265 7220 6d61 7465 7269 616c 2070 726f  ber material pro
+00000880: 7065 7274 6965 7320 6173 2064 6566 696e  perties as defin
+00000890: 6564 2069 6e20 4153 3137 3230 2e0a 0a20  ed in AS1720... 
+000008a0: 2020 2041 7474 7269 6275 7465 733a 0a20     Attributes:. 
+000008b0: 2020 2020 2020 206e 616d 653a 2054 6865         name: The
+000008c0: 206e 616d 6520 6f66 2074 6865 2074 696d   name of the tim
+000008d0: 6265 7220 6d61 7465 7269 616c 2e0a 2020  ber material..  
+000008e0: 2020 2020 2020 6772 6164 653a 2054 6865        grade: The
+000008f0: 2067 7261 6465 206f 6620 7468 6520 7469   grade of the ti
+00000900: 6d62 6572 206d 6174 6572 6961 6c0a 2020  mber material.  
+00000910: 2020 2020 2020 7365 6173 6f6e 6564 2028        seasoned (
+00000920: 626f 6f6c 293a 2041 2062 6f6f 6c65 616e  bool): A boolean
+00000930: 2069 6e64 6963 6174 696e 6720 7768 6574   indicating whet
+00000940: 6865 7220 7468 6520 7469 6d62 6572 206d  her the timber m
+00000950: 6174 6572 6961 6c20 6973 2073 6561 736f  aterial is seaso
+00000960: 6e65 642e 0a20 2020 2020 2020 2067 7261  ned..        gra
+00000970: 6465 5f74 7970 653a 2054 6865 2074 7970  de_type: The typ
+00000980: 6520 6f66 2074 6865 2074 696d 6265 7220  e of the timber 
+00000990: 6772 6164 652c 2065 2e67 2046 2c20 4d47  grade, e.g F, MG
+000009a0: 502c 2047 4c2e 0a20 2020 2020 2020 2066  P, GL..        f
+000009b0: 5f62 3a20 4d61 7465 7269 616c 2063 6861  _b: Material cha
+000009c0: 7261 6374 6572 6973 7469 6320 7374 7265  racteristic stre
+000009d0: 6e67 7468 2069 6e20 6265 6e64 696e 672e  ngth in bending.
+000009e0: 0a20 2020 2020 2020 2066 5f74 3a20 4d61  .        f_t: Ma
+000009f0: 7465 7269 616c 2063 6861 7261 6374 6572  terial character
+00000a00: 6973 7469 6320 7374 7265 6e67 7468 2069  istic strength i
+00000a10: 6e20 7465 6e73 696f 6e2e 0a20 2020 2020  n tension..     
+00000a20: 2020 2066 5f73 3a20 4d61 7465 7269 616c     f_s: Material
+00000a30: 2063 6861 7261 6374 6572 6973 7469 6320   characteristic 
+00000a40: 7374 7265 6e67 7468 2069 6e20 7368 6561  strength in shea
+00000a50: 722e 0a20 2020 2020 2020 2066 5f63 3a20  r..        f_c: 
+00000a60: 4d61 7465 7269 616c 2063 6861 7261 6374  Material charact
+00000a70: 6572 6973 7469 6320 7374 7265 6e67 7468  eristic strength
+00000a80: 2069 6e20 636f 6d70 7265 7373 696f 6e2e   in compression.
+00000a90: 0a20 2020 2020 2020 2045 3a20 4d61 7465  .        E: Mate
+00000aa0: 7269 616c 204d 6f64 756c 7573 206f 6620  rial Modulus of 
+00000ab0: 456c 6173 7469 6369 7479 2e0a 2020 2020  Elasticity..    
+00000ac0: 2020 2020 473a 204d 6174 6572 6961 6c20      G: Material 
+00000ad0: 4d6f 6475 6c75 7320 6f66 2052 6967 6964  Modulus of Rigid
+00000ae0: 6974 792e 0a20 2020 2020 2020 2064 656e  ity..        den
+00000af0: 7369 7479 3a20 4d61 7465 7269 616c 2064  sity: Material d
+00000b00: 656e 7369 7479 2e0a 2020 2020 2020 2020  ensity..        
+00000b10: 7068 695f 313a 2043 6170 6163 6974 7920  phi_1: Capacity 
+00000b20: 6661 6374 6f72 2066 6f72 2074 6865 206d  factor for the m
+00000b30: 6174 6572 6961 6c20 666f 7220 6170 706c  aterial for appl
+00000b40: 6963 6174 696f 6e20 6361 7465 676f 7279  ication category
+00000b50: 206f 6e65 2e0a 2020 2020 2020 2020 7068   one..        ph
+00000b60: 695f 323a 2043 6170 6163 6974 7920 6661  i_2: Capacity fa
+00000b70: 6374 6f72 2066 6f72 2074 6865 206d 6174  ctor for the mat
+00000b80: 6572 6961 6c20 666f 7220 6170 706c 6963  erial for applic
+00000b90: 6174 696f 6e20 6361 7465 676f 7279 2074  ation category t
+00000ba0: 776f 2e0a 2020 2020 2020 2020 7068 695f  wo..        phi_
+00000bb0: 333a 2043 6170 6163 6974 7920 6661 6374  3: Capacity fact
+00000bc0: 6f72 2066 6f72 2074 6865 206d 6174 6572  or for the mater
+00000bd0: 6961 6c20 666f 7220 6170 706c 6963 6174  ial for applicat
+00000be0: 696f 6e20 6361 7465 676f 7279 2074 6872  ion category thr
+00000bf0: 6565 2e0a 2020 2020 da00 da03 7374 72da  ee..    ....str.
+00000c00: 046e 616d 65da 0567 7261 6465 54da 0462  .name..gradeT..b
+00000c10: 6f6f 6cda 0873 6561 736f 6e65 64da 0a67  ool..seasoned..g
+00000c20: 7261 6465 5f74 7970 6572 0100 0000 da05  rade_typer......
+00000c30: 666c 6f61 74da 0366 5f62 da03 665f 74da  float..f_b..f_t.
+00000c40: 0366 5f73 da03 665f 63da 0145 da01 47da  .f_s..f_c..E..G.
+00000c50: 0764 656e 7369 7479 4629 02da 0764 6566  .densityF)...def
+00000c60: 6175 6c74 da04 7265 7072 da05 7068 695f  ault..repr..phi_
+00000c70: 31da 0570 6869 5f32 da05 7068 695f 33da  1..phi_2..phi_3.
+00000c80: 0f61 7070 6c69 6361 7469 6f6e 5f63 6174  .application_cat
+00000c90: da03 696e 7472 1300 0000 6302 0000 0000  ..intr....c.....
+00000ca0: 0000 0000 0000 0002 0000 0004 0000 0043  ...............C
+00000cb0: 0000 0173 4000 0000 7c01 0400 6401 6b02  ...s@...|...d.k.
+00000cc0: 7209 0100 7c00 6a00 5300 0400 6402 6b02  r...|.j.S...d.k.
+00000cd0: 7211 0100 7c00 6a01 5300 6403 6b02 7217  r...|.j.S.d.k.r.
+00000ce0: 7c00 6a02 5300 0900 7403 6404 7c01 9b00  |.j.S...t.d.|...
+00000cf0: 6405 9d03 8301 8201 2906 6157 0100 0052  d.......).aW...R
+00000d00: 6574 7572 6e73 2074 6865 2061 7070 726f  eturns the appro
+00000d10: 7072 6961 7465 2063 6170 6163 6974 7920  priate capacity 
+00000d20: 6661 6374 6f72 2066 6f72 2074 6865 2067  factor for the g
+00000d30: 6976 656e 2061 7070 6c69 6361 7469 6f6e  iven application
+00000d40: 0a20 2020 2020 2020 2063 6174 6567 6f72  .        categor
+00000d50: 792e 0a0a 2020 2020 2020 2020 4172 6773  y...        Args
+00000d60: 3a0a 2020 2020 2020 2020 2020 2020 6170  :.            ap
+00000d70: 706c 6963 6174 696f 6e5f 6361 743a 2054  plication_cat: T
+00000d80: 6865 2061 7070 6c69 6361 7469 6f6e 2063  he application c
+00000d90: 6174 6567 6f72 792e 0a0a 2020 2020 2020  ategory...      
+00000da0: 2020 5265 7475 726e 733a 0a20 2020 2020    Returns:.     
+00000db0: 2020 2020 2020 2066 6c6f 6174 3a20 5468         float: Th
+00000dc0: 6520 6361 7061 6369 7479 2066 6163 746f  e capacity facto
+00000dd0: 7220 666f 7220 7468 6520 6769 7665 6e20  r for the given 
+00000de0: 6170 706c 6963 6174 696f 6e20 6361 7465  application cate
+00000df0: 676f 7279 2e0a 0a20 2020 2020 2020 2052  gory...        R
+00000e00: 6169 7365 733a 0a20 2020 2020 2020 2020  aises:.         
+00000e10: 2020 2056 616c 7565 4572 726f 723a 2049     ValueError: I
+00000e20: 6620 7468 6520 6170 706c 6963 6174 696f  f the applicatio
+00000e30: 6e20 6361 7465 676f 7279 2069 7320 6e6f  n category is no
+00000e40: 7420 7265 636f 676e 697a 6564 2e0a 2020  t recognized..  
+00000e50: 2020 2020 2020 e901 0000 00e9 0200 0000        ..........
+00000e60: e903 0000 007a 1541 7070 6c69 6361 7469  .....z.Applicati
+00000e70: 6f6e 2043 6174 6567 6f72 7920 7a10 206e  on Category z. n
+00000e80: 6f74 2072 6563 6f67 6e69 7365 642e 2904  ot recognised.).
+00000e90: 7232 0000 0072 3300 0000 7234 0000 00da  r2...r3...r4....
+00000ea0: 0a56 616c 7565 4572 726f 7229 02da 0473  .ValueError)...s
+00000eb0: 656c 6672 3500 0000 7211 0000 0072 1100  elfr5...r....r..
+00000ec0: 0000 7212 0000 00da 0370 6869 5c00 0000  ..r......phi\...
+00000ed0: 7316 0000 0002 0e0a 0106 010a 0106 0106  s...............
+00000ee0: 0106 0102 0102 010a 0104 ff7a 1254 696d  ...........z.Tim
+00000ef0: 6265 724d 6174 6572 6961 6c2e 7068 694e  berMaterial.phiN
+00000f00: da01 64da 0162 fa0c 666c 6f61 7420 7c20  ..d..b..float | 
+00000f10: 4e6f 6e65 da04 4e6f 6e65 6303 0000 0000  None..Nonec.....
+00000f20: 0000 0000 0000 0006 0000 0006 0000 0043  ...............C
+00000f30: 0000 0173 bc01 0000 7c00 6a00 7401 6a02  ...s....|.j.t.j.
+00000f40: 6b02 7256 7c01 6401 6b04 7256 7c01 0400  k.rV|.d.k.rV|...
+00000f50: 6402 6b02 7210 6e0c 0400 6403 6b02 7215  d.k.r.n...d.k.r.
+00000f60: 6e07 0400 6404 6b02 721a 6e02 0100 6e0b  n...d.k.r.n...n.
+00000f70: 0100 7c00 6a03 9b00 6405 7c01 9b00 6406  ..|.j...d.|...d.
+00000f80: 9d04 7d03 6e09 0900 7404 6407 7c01 9b00  ..}.n...t.d.|...
+00000f90: 6408 9d03 8301 8201 7405 6409 7c00 6a03  d.......t.d.|.j.
+00000fa0: 9b00 640a 7c03 9b00 9d04 8301 0100 7c00  ..d.|.........|.
+00000fb0: a006 7c03 a101 7d03 7c03 6a03 7c00 5f03  ..|...}.|.j.|._.
+00000fc0: 7c03 6a07 7c00 5f07 7c03 6a08 7c00 5f08  |.j.|._.|.j.|._.
+00000fd0: 7c03 6a09 7c00 5f09 7c03 6a0a 7c00 5f0a  |.j.|._.|.j.|._.
+00000fe0: 6416 5300 7c00 6a00 7401 6a0b 6b02 72a0  d.S.|.j.t.j.k.r.
+00000ff0: 7c01 640b 6b04 727c 7c00 6a08 7d04 740c  |.d.k.r||.j.}.t.
+00001000: 7c00 6a08 640b 7c01 1b00 640c 1300 1400  |.j.d.|...d.....
+00001010: 640d 8302 7c00 5f08 7405 640e 7c04 9b00  d...|._.t.d.|...
+00001020: 640a 7c00 6a08 9b00 640f 9d05 8301 0100  d.|.j...d.......
+00001030: 7c01 6410 6b04 729e 7c00 6a07 7d05 740c  |.d.k.r.|.j.}.t.
+00001040: 7c00 6a07 6410 7c01 1b00 640c 1300 1400  |.j.d.|...d.....
+00001050: 640d 8302 7c00 5f07 7405 6411 7c05 9b00  d...|._.t.d.|...
+00001060: 640a 7c00 6a07 9b00 6412 9d05 8301 0100  d.|.j...d.......
+00001070: 6416 5300 6416 5300 7c00 6a00 7401 6a0d  d.S.d.S.|.j.t.j.
+00001080: 6b02 72b2 7405 6413 7c01 9b00 6414 7c02  k.r.t.d.|...d.|.
+00001090: 9b00 9d04 8301 0100 740e 8201 7c00 6a00  ........t...|.j.
+000010a0: 7401 6a0f 6b02 72da 7c01 640b 6b04 72dc  t.j.k.r.|.d.k.r.
+000010b0: 7c00 6a08 7d04 740c 7c00 6a08 640b 7c01  |.j.}.t.|.j.d.|.
+000010c0: 1b00 640c 1300 1400 640d 8302 7c00 5f08  ..d.....d...|._.
+000010d0: 7405 640e 7c04 9b00 640a 7c00 6a08 9b00  t.d.|...d.|.j...
+000010e0: 6415 9d05 8301 0100 6416 5300 6416 5300  d.......d.S.d.S.
+000010f0: 6416 5300 2917 6115 0200 0055 7064 6174  d.S.).a....Updat
+00001100: 6573 2074 6865 2066 5f74 2070 726f 7065  es the f_t prope
+00001110: 7274 7920 666f 7220 6c61 7267 6520 7365  rty for large se
+00001120: 6374 696f 6e73 2c20 696e 636c 7564 696e  ctions, includin
+00001130: 673a 0a20 2020 2020 2020 2020 2066 5f74  g:.          f_t
+00001140: 2c20 665f 622c 2066 5f63 2c20 665f 7320  , f_b, f_c, f_s 
+00001150: 666f 7220 4d47 5020 7365 6374 696f 6e73  for MGP sections
+00001160: 2077 6974 6820 643e 3134 306d 6d20 2841   with d>140mm (A
+00001170: 5331 3732 302e 3120 5461 626c 6520 4833  S1720.1 Table H3
+00001180: 2e31 2c20 4e6f 7465 2034 293b 0a20 2020  .1, Note 4);.   
+00001190: 2020 2020 2020 2066 5f62 2066 6f72 2046         f_b for F
+000011a0: 2d67 7261 6465 2073 6563 7469 6f6e 7320  -grade sections 
+000011b0: 7769 7468 2064 203e 2033 3030 6d6d 2028  with d > 300mm (
+000011c0: 4153 3137 3230 2e31 2054 6162 6c65 2048  AS1720.1 Table H
+000011d0: 322e 3120 4e6f 7465 2031 293b 0a20 2020  2.1 Note 1);.   
+000011e0: 2020 2020 2020 2066 5f74 2066 6f72 2046         f_t for F
+000011f0: 2d67 7261 6465 2073 6563 7469 6f6e 7320  -grade sections 
+00001200: 7769 7468 2064 203e 2031 3530 6d6d 2028  with d > 150mm (
+00001210: 4153 3137 3230 2e31 2054 6162 6c65 2048  AS1720.1 Table H
+00001220: 2e32 204e 6f74 6520 3229 3b0a 2020 2020  .2 Note 2);.    
+00001230: 2020 2020 2020 665f 7420 666f 7220 476c        f_t for Gl
+00001240: 756c 616d 2073 6563 7469 6f6e 7320 7769  ulam sections wi
+00001250: 7468 2064 203e 2031 3530 6d6d 2020 2841  th d > 150mm  (A
+00001260: 5331 3732 302e 3120 5461 626c 6520 372e  S1720.1 Table 7.
+00001270: 3120 4e6f 7465 2031 292e 0a0a 2020 2020  1 Note 1)...    
+00001280: 2020 2020 4172 6773 3a0a 2020 2020 2020      Args:.      
+00001290: 2020 2020 2020 643a 2054 6865 2064 6570        d: The dep
+000012a0: 7468 206f 6620 7468 6520 7469 6d62 6572  th of the timber
+000012b0: 2073 6563 7469 6f6e 2e0a 2020 2020 2020   section..      
+000012c0: 2020 2020 2020 623a 2054 6865 2062 7265        b: The bre
+000012d0: 6164 7468 206f 6620 7468 6520 7469 6d62  adth of the timb
+000012e0: 6572 2073 6563 7469 6f6e 2028 7265 7175  er section (requ
+000012f0: 6972 6564 2066 6f72 2041 3137 206d 6174  ired for A17 mat
+00001300: 6572 6961 6c29 2e0a 2020 2020 2020 2020  erial)..        
+00001310: e98c 0000 00e9 be00 0000 e9f0 0000 0069  ...............i
+00001320: 2201 0000 fa01 207a 086d 6d20 6465 7074  "..... z.mm dept
+00001330: 687a 0e53 6563 7469 6f6e 2064 6570 7468  hz.Section depth
+00001340: 207a 5620 3e20 3134 306d 6d2c 2070 6c65   zV > 140mm, ple
+00001350: 6173 6520 696e 7465 7270 6f6c 6174 6520  ase interpolate 
+00001360: 6d61 7465 7269 616c 2070 726f 7065 7274  material propert
+00001370: 6965 7320 666f 7220 4d47 5020 7365 6374  ies for MGP sect
+00001380: 696f 6e20 2874 6162 6c65 2048 332e 312c  ion (table H3.1,
+00001390: 204e 6f74 6520 3429 2e7a 164d 6174 6572   Note 4).z.Mater
+000013a0: 6961 6c20 6368 616e 6765 6420 6672 6f6d  ial changed from
+000013b0: 207a 0420 746f 20e9 9600 0000 67c7 4b37   z. to .....g.K7
+000013c0: 8941 60c5 3f72 3900 0000 7a22 5465 6e73  .A`.?r9...z"Tens
+000013d0: 696c 6520 7374 7265 6e67 7468 2066 5f74  ile strength f_t
+000013e0: 2063 6861 6e67 6564 2066 726f 6d20 7a26   changed from z&
+000013f0: 2064 7565 2074 6f20 7365 6374 696f 6e20   due to section 
+00001400: 7369 7a65 2c20 5461 626c 6520 482e 3220  size, Table H.2 
+00001410: 4e6f 7465 2032 692c 0100 007a 2242 656e  Note 2i,...z"Ben
+00001420: 6469 6e67 2073 7472 656e 6774 6820 665f  ding strength f_
+00001430: 6220 6368 616e 6765 6420 6672 6f6d 207a  b changed from z
+00001440: 2620 6475 6520 746f 2073 6563 7469 6f6e  & due to section
+00001450: 2073 697a 652c 2054 6162 6c65 2048 2e32   size, Table H.2
+00001460: 204e 6f74 6520 317a 0972 6571 7569 7265   Note 1z.require
+00001470: 7320 7a05 2061 6e64 207a 2420 6475 6520  s z. and z$ due 
+00001480: 746f 2073 6563 7469 6f6e 2073 697a 652c  to section size,
+00001490: 2054 6162 6c65 2037 2e31 204e 6f74 654e   Table 7.1 NoteN
+000014a0: 2910 7227 0000 0072 0600 0000 7208 0000  ).r'...r....r...
+000014b0: 0072 2300 0000 723a 0000 00da 0570 7269  .r#...r:.....pri
+000014c0: 6e74 da0c 6672 6f6d 5f6c 6962 7261 7279  nt..from_library
+000014d0: 7229 0000 0072 2a00 0000 722c 0000 0072  r)...r*...r,...r
+000014e0: 2b00 0000 720e 0000 00da 0572 6f75 6e64  +...r......round
+000014f0: 7210 0000 00da 134e 6f74 496d 706c 656d  r......NotImplem
+00001500: 656e 7465 6445 7272 6f72 720f 0000 0029  entedErrorr....)
+00001510: 0672 3b00 0000 723d 0000 0072 3e00 0000  .r;...r=...r>...
+00001520: 5a07 6e65 775f 6d61 745a 0c6f 7269 6769  Z.new_matZ.origi
+00001530: 6e61 6c5f 665f 745a 0c6f 7269 6769 6e61  nal_f_tZ.origina
+00001540: 6c5f 665f 6272 1100 0000 7211 0000 0072  l_f_br....r....r
+00001550: 1200 0000 da18 7570 6461 7465 5f66 726f  ......update_fro
+00001560: 6d5f 7365 6374 696f 6e5f 7369 7a65 7600  m_section_sizev.
+00001570: 0000 734e 0000 0014 0b02 0124 0114 0102  ..sN.......$....
+00001580: 0102 010a 0104 ff16 040a 0108 0108 0108  ................
+00001590: 0108 010c 010c 0208 0106 021a 0102 0112  ................
+000015a0: 0104 ff08 0406 021a 0102 0112 0108 ff04  ................
+000015b0: fc0c 0814 0104 0114 0206 021a 0102 0112  ................
+000015c0: 0108 ff08 fc7a 2754 696d 6265 724d 6174  .....z'TimberMat
+000015d0: 6572 6961 6c2e 7570 6461 7465 5f66 726f  erial.update_fro
+000015e0: 6d5f 7365 6374 696f 6e5f 7369 7a65 da0a  m_section_size..
+000015f0: 696e 7075 745f 6469 6374 da04 6469 6374  input_dict..dict
+00001600: 6302 0000 0000 0000 0000 0000 0003 0000  c...............
+00001610: 0004 0000 0003 0000 0173 2e00 0000 7c00  .........s....|.
+00001620: 6a00 a001 a100 8900 8700 6601 6401 6402  j.........f.d.d.
+00001630: 8408 7c01 a002 a100 4400 8301 7d02 7c00  ..|.....D...}.|.
+00001640: 6404 6900 7c02 a401 8e01 5300 2905 6181  d.i.|.....S.).a.
+00001650: 0100 0043 7265 6174 6520 6120 5469 6d62  ...Create a Timb
+00001660: 6572 4d61 7465 7269 616c 2062 7920 6469  erMaterial by di
+00001670: 7265 6374 6c79 2070 6f70 756c 6174 696e  rectly populatin
+00001680: 6720 6174 7472 6962 7574 6573 2066 726f  g attributes fro
+00001690: 6d20 696e 7075 7420 6469 6374 696f 6e61  m input dictiona
+000016a0: 7279 2c0a 2020 2020 2020 2020 6967 6e6f  ry,.        igno
+000016b0: 7269 6e67 2064 6963 7469 6f6e 6172 7920  ring dictionary 
+000016c0: 6b65 7973 2077 6869 6368 2061 7265 6e27  keys which aren'
+000016d0: 7420 636c 6173 7320 6174 7472 6962 7574  t class attribut
+000016e0: 6573 2e0a 0a20 2020 2020 2020 2041 7267  es...        Arg
+000016f0: 733a 0a20 2020 2020 2020 2020 2020 2069  s:.            i
+00001700: 6e70 7574 5f64 6963 743a 204b 6579 2d76  nput_dict: Key-v
+00001710: 616c 7565 2070 6169 7273 2074 6f20 6465  alue pairs to de
+00001720: 6669 6e65 2074 6865 2074 696d 6265 7220  fine the timber 
+00001730: 6d61 7465 7269 616c 2c20 6b65 7973 2063  material, keys c
+00001740: 6f72 7265 7370 6f6e 6469 6e67 2074 6f20  orresponding to 
+00001750: 636c 6173 730a 2020 2020 2020 2020 2020  class.          
+00001760: 2020 6174 7472 6962 7574 6520 6e61 6d65    attribute name
+00001770: 7320 7769 6c6c 2062 6520 7570 6461 7465  s will be update
+00001780: 640a 0a20 2020 2020 2020 2052 6574 7572  d..        Retur
+00001790: 6e73 3a0a 2020 2020 2020 2020 2020 2020  ns:.            
+000017a0: 5469 6d62 6572 4d61 7465 7269 616c 3a20  TimberMaterial: 
+000017b0: 5468 6520 7469 6d62 6572 206d 6174 6572  The timber mater
+000017c0: 6961 6c20 6f62 6a65 6374 2e0a 2020 2020  ial object..    
+000017d0: 2020 2020 6301 0000 0000 0000 0000 0000      c...........
+000017e0: 0003 0000 0004 0000 0013 0000 0173 1e00  .............s..
+000017f0: 0000 6900 7c00 5d0b 5c02 7d01 7d02 7c01  ..i.|.].\.}.}.|.
+00001800: 8800 7600 7202 7c01 7c02 9302 7102 5300  ..v.r.|.|...q.S.
+00001810: 7211 0000 0072 1100 0000 2903 da02 2e30  r....r....)....0
+00001820: da01 6bda 0176 a901 da0a 7661 6c69 645f  ..k..v....valid_
+00001830: 6b65 7973 7211 0000 0072 1200 0000 da0a  keysr....r......
+00001840: 3c64 6963 7463 6f6d 703e c000 0000 7302  <dictcomp>....s.
+00001850: 0000 001e 007a 2c54 696d 6265 724d 6174  .....z,TimberMat
+00001860: 6572 6961 6c2e 6672 6f6d 5f64 6963 742e  erial.from_dict.
+00001870: 3c6c 6f63 616c 733e 2e3c 6469 6374 636f  <locals>.<dictco
+00001880: 6d70 3e4e 7211 0000 0029 03da 0f5f 5f61  mp>Nr....)...__a
+00001890: 6e6e 6f74 6174 696f 6e73 5f5f da04 6b65  nnotations__..ke
+000018a0: 7973 da05 6974 656d 7329 03da 0363 6c73  ys..items)...cls
+000018b0: 724b 0000 00da 0a76 616c 6964 5f64 6963  rK.....valid_dic
+000018c0: 7472 1100 0000 7250 0000 0072 1200 0000  tr....rP...r....
+000018d0: da09 6672 6f6d 5f64 6963 74b0 0000 0073  ..from_dict....s
+000018e0: 0600 0000 0a0e 1602 0e02 7a18 5469 6d62  ..........z.Timb
+000018f0: 6572 4d61 7465 7269 616c 2e66 726f 6d5f  erMaterial.from_
+00001900: 6469 6374 da07 6c69 6272 6172 79fa 1370  dict..library..p
+00001910: 642e 4461 7461 4672 616d 6520 7c20 4e6f  d.DataFrame | No
+00001920: 6e65 6303 0000 0000 0000 0000 0000 0005  nec.............
+00001930: 0000 0003 0000 0043 0000 0173 3a00 0000  .......C...s:...
+00001940: 7c02 6401 7500 7207 7400 8300 7d02 7c02  |.d.u.r.t...}.|.
+00001950: 6a01 7c02 6402 1900 7c01 6b02 1900 7d03  j.|.d...|.k...}.
+00001960: 7c03 6a02 6403 6404 8d01 6405 1900 7d04  |.j.d.d...d...}.
+00001970: 7c00 a003 7c04 a101 5300 2906 61b5 0100  |...|...S.).a...
+00001980: 0043 7265 6174 6573 2061 2054 696d 6265  .Creates a Timbe
+00001990: 724d 6174 6572 6961 6c20 6f62 6a65 6374  rMaterial object
+000019a0: 2066 726f 6d20 6120 6d61 7465 7269 616c   from a material
+000019b0: 206c 6962 7261 7279 2028 4461 7461 4672   library (DataFr
+000019c0: 616d 6529 2e0a 0a20 2020 2020 2020 2041  ame)...        A
+000019d0: 7267 733a 0a20 2020 2020 2020 2020 2020  rgs:.           
+000019e0: 206e 616d 653a 2054 6865 206e 616d 6520   name: The name 
+000019f0: 6f66 2074 6865 2074 696d 6265 7220 6d61  of the timber ma
+00001a00: 7465 7269 616c 2074 6f20 6c6f 6f6b 7570  terial to lookup
+00001a10: 2069 6e20 7468 6520 6c69 6272 6172 7920   in the library 
+00001a20: 2869 6e20 276e 616d 6527 2063 6f6c 756d  (in 'name' colum
+00001a30: 6e29 0a20 2020 2020 2020 2020 2020 206c  n).            l
+00001a40: 6962 7261 7279 2028 7064 2e44 6174 6146  ibrary (pd.DataF
+00001a50: 7261 6d65 2c20 6f70 7469 6f6e 616c 293a  rame, optional):
+00001a60: 2054 6865 2044 6174 6146 7261 6d65 206f   The DataFrame o
+00001a70: 6620 7468 6520 6c69 6272 6172 7920 6f66  f the library of
+00001a80: 2074 696d 6265 7220 6d61 7465 7269 616c   timber material
+00001a90: 732e 0a20 2020 2020 2020 2020 2020 2020  s..             
+00001aa0: 2020 2049 6620 6e6f 7420 7072 6f76 6964     If not provid
+00001ab0: 6564 2c20 7468 6520 6465 6661 756c 7420  ed, the default 
+00001ac0: 6c69 6272 6172 7920 604d 4154 4552 4941  library `MATERIA
+00001ad0: 4c5f 4c49 4252 4152 5960 2069 7320 7573  L_LIBRARY` is us
+00001ae0: 6564 2e0a 0a20 2020 2020 2020 2052 6574  ed...        Ret
+00001af0: 7572 6e73 3a0a 2020 2020 2020 2020 2020  urns:.          
+00001b00: 2020 5469 6d62 6572 4d61 7465 7269 616c    TimberMaterial
+00001b10: 3a20 5468 6520 7469 6d62 6572 206d 6174  : The timber mat
+00001b20: 6572 6961 6c20 6f62 6a65 6374 2e0a 2020  erial object..  
+00001b30: 2020 2020 2020 4e72 2300 0000 da07 7265        Nr#.....re
+00001b40: 636f 7264 7329 01da 066f 7269 656e 7472  cords)...orientr
+00001b50: 0100 0000 2904 721e 0000 00da 036c 6f63  ....).r......loc
+00001b60: da07 746f 5f64 6963 7472 5800 0000 2905  ..to_dictrX...).
+00001b70: 7256 0000 0072 2300 0000 7259 0000 00da  rV...r#...rY....
+00001b80: 086d 6174 6572 6961 6c5a 086d 6174 5f64  .materialZ.mat_d
+00001b90: 6963 7472 1100 0000 7211 0000 0072 1200  ictr....r....r..
+00001ba0: 0000 7247 0000 00c4 0000 0073 0a00 0000  ..rG.......s....
+00001bb0: 080c 0601 1201 1001 0a01 7a1b 5469 6d62  ..........z.Timb
+00001bc0: 6572 4d61 7465 7269 616c 2e66 726f 6d5f  erMaterial.from_
+00001bd0: 6c69 6272 6172 7929 0472 3500 0000 7236  library).r5...r6
+00001be0: 0000 0072 1300 0000 7228 0000 0029 014e  ...r....r(...).N
+00001bf0: 2906 723d 0000 0072 2800 0000 723e 0000  ).r=...r(...r>..
+00001c00: 0072 3f00 0000 7213 0000 0072 4000 0000  .r?...r....r@...
+00001c10: 2904 724b 0000 0072 4c00 0000 7213 0000  ).rK...rL...r...
+00001c20: 0072 2000 0000 2904 7223 0000 0072 2200  .r ...).r#...r".
+00001c30: 0000 7259 0000 0072 5a00 0000 2919 720a  ..rY...rZ...).r.
+00001c40: 0000 0072 0b00 0000 720c 0000 0072 0d00  ...r....r....r..
+00001c50: 0000 7223 0000 0072 5300 0000 7224 0000  ..r#...rS...r$..
+00001c60: 0072 2600 0000 7227 0000 0072 2900 0000  .r&...r'...r)...
+00001c70: 722a 0000 0072 2b00 0000 722c 0000 0072  r*...r+...r,...r
+00001c80: 2d00 0000 722e 0000 0072 2f00 0000 7204  -...r....r/...r.
+00001c90: 0000 0072 3200 0000 7233 0000 0072 3400  ...r2...r3...r4.
+00001ca0: 0000 723c 0000 0072 4a00 0000 da0b 636c  ..r<...rJ.....cl
+00001cb0: 6173 736d 6574 686f 6472 5800 0000 7247  assmethodrX...rG
+00001cc0: 0000 0072 1100 0000 7211 0000 0072 1100  ...r....r....r..
+00001cd0: 0000 7212 0000 0072 2000 0000 3800 0000  ..r....r ...8...
+00001ce0: 732c 0000 000a 0004 020c 130c 010c 010c  s,..............
+00001cf0: 010c 010c 010c 010c 010c 010c 010c 0114  ................
+00001d00: 0114 0114 010a 020c 1a02 3a0c 0102 1312  ..........:.....
+00001d10: 0172 2000 0000 6300 0000 0000 0000 0000  .r ...c.........
+00001d20: 0000 0002 0000 0004 0000 0043 0000 0173  ...........C...s
+00001d30: 3000 0000 7400 8300 7d00 7401 7c00 8301  0...t...}.t.|...
+00001d40: 0100 7402 a003 6401 a101 7d01 7402 a003  ..t...d...}.t...
+00001d50: 6401 7c00 a102 7d01 7401 7c01 8301 0100  d.|...}.t.|.....
+00001d60: 6402 5300 2903 7a0b 4d61 696e 2053 6372  d.S.).z.Main Scr
+00001d70: 6970 74da 054d 4750 3130 4e29 0472 1e00  ipt..MGP10N).r..
+00001d80: 0000 7246 0000 0072 2000 0000 7247 0000  ..rF...r ...rG..
+00001d90: 0029 025a 106d 6174 6572 6961 6c5f 6c69  .).Z.material_li
+00001da0: 6272 6172 795a 056d 6770 3130 7211 0000  braryZ.mgp10r...
+00001db0: 0072 1100 0000 7212 0000 00da 046d 6169  .r....r......mai
+00001dc0: 6ed7 0000 0073 0a00 0000 0602 0801 0a01  n....s..........
+00001dd0: 0c01 0c01 7262 0000 00da 085f 5f6d 6169  ....rb.....__mai
+00001de0: 6e5f 5f29 0272 1300 0000 7214 0000 0029  n__).r....r....)
+00001df0: 1172 0d00 0000 da0a 5f5f 6675 7475 7265  .r......__future
+00001e00: 5f5f 7202 0000 0072 1500 0000 da0b 6461  __r....r......da
+00001e10: 7461 636c 6173 7365 7372 0300 0000 7204  taclassesr....r.
+00001e20: 0000 00da 0465 6e75 6d72 0500 0000 da06  .....enumr......
+00001e30: 7061 6e64 6173 721a 0000 0072 2200 0000  pandasr....r"...
+00001e40: 7206 0000 0072 1e00 0000 7220 0000 0072  r....r....r ...r
+00001e50: 6200 0000 720a 0000 0072 1100 0000 7211  b...r....r....r.
+00001e60: 0000 0072 1100 0000 7212 0000 00da 083c  ...r....r......<
+00001e70: 6d6f 6475 6c65 3e01 0000 0073 1e00 0000  module>....s....
+00001e80: 0400 0c0d 0801 1001 0c01 0801 1203 0a12  ................
+00001e90: 0811 1001 007f 081f 0809 0a01 04ff       ..............
```

### Comparing `timberas-0.2.0/src/timberas/data/material_library.csv` & `timberas-0.3.0/src/timberas/data/material_library.csv`

 * *Files identical despite different names*

### Comparing `timberas-0.2.0/src/timberas/data/section_library.csv` & `timberas-0.3.0/src/timberas/data/section_library.csv`

 * *Files identical despite different names*

### Comparing `timberas-0.2.0/src/timberas/geometry.py` & `timberas-0.3.0/src/timberas/geometry.py`

 * *Files 1% similar despite different names*

```diff
@@ -17,15 +17,15 @@
 """
 
 from __future__ import annotations
 
 import os
 from dataclasses import dataclass, field
 from math import nan, isnan, floor, log10
-from enum import Enum
+from enum import Enum, auto
 import pandas as pd
 
 
 class ShapeType(str, Enum):
     """
     An enumeration of section type string constants. Provides a type-safe way of representing
     different section types.
@@ -198,15 +198,15 @@
         return 2 / 3 * self.d * self.b_tot
 
 
 def import_section_library() -> pd.DataFrame:
     """
     Imports a section library from a CSV file.
 
-    The CSV file is located at 'timberas.data/section_library.csv'.
+    The CSV file is located at 'timberas/data/section_library.csv'.
 
     Returns:
         pd.DataFrame: A DataFrame containing the contents of the section library CSV file.
 
     Raises:
         FileNotFoundError: If the CSV file does not exist.
     """
```

### Comparing `timberas-0.2.0/src/timberas/material.py` & `timberas-0.3.0/src/timberas/material.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 """
-This module provides classes and functions for creating representing timber materials 
-based on AS1720. 
+This module provides classes and functions for creating timber materials 
+described in AS1720.1. 
 
 Classes:
     GradeType: Enum class defining material grade string constants. 
 
     TimberMaterial: Represents a timber material based on AS1720. 
 
 Functions:
```

### Comparing `timberas-0.2.0/src/timberas/member.py` & `timberas-0.3.0/src/timberas/member.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,17 +1,18 @@
 """
 TODO
 """
 from __future__ import annotations
 import math
-from math import nan, isnan, floor, log10
-from enum import auto, IntEnum, Enum
+from math import isnan, floor, log10
+from enum import IntEnum, Enum
 from dataclasses import dataclass, field
 from timberas.material import TimberMaterial
 from timberas.geometry import TimberSection
+from timberas.utils import nomenclature_AS1720 as NOMEN
 
 
 class EffectiveLengthFactor(float, Enum):
     """Dataclass containing values for effective length factor g_13 for columns with intermediate
     lateral restraint. End restraint conditions as listed in Table 3.2, AS1720.1:2010.
 
     Attributes:
@@ -58,22 +59,21 @@
     FIVE_DAYS = 0.94
     FIVE_MONTHS = 0.8
     FIFTY_YEARS = 0.57
     # DL_ONLY = 0.57
     # DL_AND_LONG_TERM_LL = 0.57
 
 
-class BendingRestraint(str, Enum):
-    """compresssion edge is critical edge"""
+class RestraintEdge(str, Enum):
+    """compression edge is critical edge"""
 
-    DISCRETE_LATERAL_RESTRAINT_COMPRESSION_EDGE = auto()
-    DISCRETE_LATERAL_RESTRAINT_TENSION_EDGE = auto()
-    CONTINUOUS_LATERAL_RESTRAINT_COMPRESSION_EDGE = auto()
-    CONTINUOUS_LATERAL_RESTRAINT_TENSION_EDGE = auto()
-    CONTINUOUS_LATERAL_RESTRAINT_TENSION_AND_DISCRETE_TORSIONAL_COMPRESSION = auto()
+    TENSION = "tension"
+    COMPRESSION = "compression"
+    BOTH = "both"  # uses compression edge formulas
+    TENSION_AND_TORSIONAL = "tension_and_torsional"
 
 
 # def locations_latitudes():
 #     """Clause 2.4.3, AS1720.1:2010"""
 #     l = [
 #         "Queensland_&_North_of_25˚S",
 #         "Queensland_&_South_of_25˚S",
@@ -93,31 +93,25 @@
     sec_name: str = field(init=False)
     mat_name: str = field(init=False)
 
     application_cat: int = 1  # application category for structural member
     high_temp_latitude: bool = False
     consider_partial_seasoning: bool = False
 
-    n_com: int = 1
-    n_mem: int = 1
-    member_spacing: float = 0  # member spacing
-
     L: float = 1  # length
-    L_ay: float = 0
-    L_ar: float = nan  # torsional constraint, compression edge
-    g_13: float = 1
+    L_a: float | dict | None = None
+    # L_ar: float = nan  # torsional constraint, compression edge
+    g_13: float | dict = 1
     k_1: float = 1.0
     r: float = 0.25  # ratio of temporary to total design action effect
-    restraint: str | BendingRestraint = (
-        BendingRestraint.DISCRETE_LATERAL_RESTRAINT_TENSION_EDGE
-    )
+    restraint_edge: str | RestraintEdge = RestraintEdge.TENSION
 
     N_dt: float = field(init=False)  # kN
-    N_cx: float = field(init=False)  # kN
-    N_cy: float = field(init=False)  # kN
+    N_dcx: float = field(init=False)  # kN
+    N_dcy: float = field(init=False)  # kN
     N_dc: float = field(init=False)  # kN
     M_d: float = field(init=False)  # kNm
     V_d: float = field(init=False)  # kNm
 
     sig_figs: int = field(repr=False, default=4)
 
     def __post_init__(self):
@@ -125,16 +119,16 @@
         self.mat_name = self.mat.name
         # self.mat.update_f_t(self.sec_type, self.d)
         self.solve_capacities()
 
     def solve_capacities(self):
         """Calculate tension, compression, and bending design capacities."""
         self.N_dt = self._N_dt()
-        self.N_cx = self._N_cx()
-        self.N_cy = self._N_cy()
+        self.N_dcx = self._N_dcx()
+        self.N_dcy = self._N_dcy()
         self.N_dc = self._N_dc()
         self.M_d = self._M_d()
         self.V_d = self._V_d()
 
         # round to sig figs
         if self.sig_figs:
             for key, val in list(self.__dict__.items()):
@@ -147,49 +141,88 @@
 
     def update_k_1(self, k_1: float) -> TimberSection:
         """Change k_1 factor and recalculate section capacities."""
         self.k_1 = k_1
         self.solve_capacities()
         return self
 
+    def report(
+        self,
+        attribute_names: str | list[str] | None = None,
+        report_type: str = "print",
+        with_nomenclature: bool = False,
+        with_clause: bool = False,
+    ) -> None:
+        # convert single-value attribute to list
+        if attribute_names is None:
+            attribute_names = list(self.__annotations__.keys())
+        if not isinstance(attribute_names, list):
+            attribute_names = [attribute_names]
+
+        if report_type == "print":
+            # print out attributes
+            for att in attribute_names:
+                # get attribute val from self, self.sec, or self.mat
+                att_val = None
+                if hasattr(self, att):
+                    att_val = getattr(self, att)
+                elif hasattr(self.mat, att):
+                    att_val = getattr(self.mat, att)
+                elif hasattr(self.sec, att):
+                    att_val = getattr(self.sec, att)
+                if att_val is not None:
+                    prefix = ""
+                    if att in NOMEN:
+                        # check it attribute defined in nomenclature dictionary
+                        nom, clause = NOMEN[att]
+                        if with_nomenclature:
+                            # add nomenclature
+                            prefix = prefix + " " + nom
+                        if with_clause:
+                            # add clause
+                            prefix = prefix + " " + clause
+                    print(f"    {att}{prefix} = {att_val}")
+                else:
+                    print(f"Unknown attribute {att}")
+
     @property
     def phi(self) -> float:
         """Table 2.1, AS1720.1:2010"""
         phi: float = self.mat.phi(self.application_cat)
         return phi
 
-    def _N_cx(self) -> float:
+    def _N_dcx(self) -> float:
         """Clause 3.3.1.1, AS1720.1:2010"""
         return (
             self.phi
             * self.k_1
             * self.k_4
             * self.k_6
             * self.k_12_x
             * self.mat.f_c
             * self.sec.A_c
             / 1000
         )
 
-    def _N_cy(self) -> float:
+    def _N_dcy(self) -> float:
         """Clause 3.3.1.1, AS1720.1:2010"""
         return (
             self.phi
             * self.k_1
             * self.k_4
             * self.k_6
             * self.k_12_y
             * self.mat.f_c
             * self.sec.A_c
             / 1000
         )
 
     def _N_dc(self) -> float:
         """Clause 3.3.1.1, AS1720.1:2010"""
-        return min(self._N_cx(), self._N_cy())
+        return min(self._N_dcx(), self._N_dcy())
 
     def _N_dt(self) -> float:
         """Clause 3.4.1, AS1720.1:2010"""
         return (
             self.phi
             * self.k_1
             * self.k_4
@@ -237,39 +270,106 @@
     def S2(self) -> float:
         """Slenderness coefficient for lateral buckling under bending, minor axis.
         Clause 3.2.3(c), AS1720.1:2010."""
         return 0
 
     @property
     def S3(self) -> float:
-        """Slenderness coefficient for lateral buckling under compression, major axis.
+        """Slenderness coefficient for lateral buckling under compression, x axis.
         Clause 3.3.2, AS1720.1:2010. Not implemented in TimberMember parent class, added in
         child classes."""
         raise NotImplementedError
 
     @property
     def S4(self) -> float:
         """Clause 3.3.2.2(b), AS1720.1:2010"""
         # NOTE: b_i or b? valid for other cases?
         calc_1 = self.L_ay / self.sec.b
-        calc_2 = self.g_13 * self.L / (self.sec.b)
+        calc_2 = self.g_13_y * self.L / (self.sec.b)
         return round(min(calc_1, calc_2), 2)
 
     @property
     def rho_c(self) -> float:
         """Section E2, AS1720.1:2010"""
         # NOTE -> move to child class when other materials (LVL) added
         r = self.r if self.r > 0 else 0.25
         if self.mat.seasoned:
             rho = 11.39 * (self.mat.E / self.mat.f_c) ** (-0.408) * r ** (-0.074)
         else:
             rho = 9.29 * (self.mat.E / self.mat.f_c) ** (-0.367) * r ** (-0.146)
         return rho
 
     @property
+    def g_13_x(self) -> float:
+        """Effective length factor for compressive buckling, x-axis"""
+        # g_13 is float - use in x and y axes
+        if isinstance(self.g_13, float | int):
+            return self.g_13
+        # else g_13 is dictionary - use x axis key value only
+        if "x" in self.g_13:
+            return self.g_13["x"]
+        # raise error if not yet returned
+        raise KeyError(
+            "effective length factor g_13 not defined for x-axis compressive buckling"
+        )
+
+    @property
+    def g_13_y(self) -> float:
+        """Effective length factor for compressive buckling, y-axis"""
+        # g_13 is float - use in x and y axes
+        if isinstance(self.g_13, float | int):
+            return self.g_13
+        # else g_13 is dictionary - use y axis key value only
+        if "y" in self.g_13:
+            return self.g_13["y"]
+        # raise error if not yet returned
+        raise KeyError(
+            "effective length factor g_13 not defined for y-axis compressive buckling"
+        )
+
+    @property
+    def L_ax(self) -> float:
+        """distance between effective lateral restraint against buckling about x-axis."""
+        if isinstance(self.L_a, float | int) or (self.L_a is None):
+            l_ax = self.L_a
+        elif isinstance(self.L_a, dict) and "x" in self.L_a:
+            l_ax = self.L_a["x"]
+        else:  # raise error if not yet returned
+            raise KeyError(
+                "lateral restraint for x-axis compressive buckling L_ax not defined"
+            )
+        if l_ax is None:
+            l_ax = self.L
+        return l_ax
+
+    @property
+    def L_ay(self) -> float:
+        """distance between effective lateral restraint against buckling about y-axis."""
+        if isinstance(self.L_a, float | int) or (self.L_a is None):
+            l_ay = self.L_a
+        elif isinstance(self.L_a, dict) and "y" in self.L_a:
+            l_ay = self.L_a["y"]
+        else:  # raise error if not yet returned
+            raise KeyError(
+                "lateral restraint for y-axis compressive buckling L_ay not defined"
+            )
+        if l_ay is None:
+            l_ay = self.L
+        return l_ay
+
+    @property
+    def L_a_phi(self) -> float:
+        """distance between effective torsional restraint against buckling, Cl 3.2.3.2(b)."""
+        if isinstance(self.L_a, dict) and "phi" in self.L_a:
+            return self.L_a["phi"]
+        raise KeyError(
+            "no torsional restraint distance L_a_phi provided, i.e. not 'phi' key in L_a input"
+        )
+
+    @property
     def rho_b(self) -> float:
         """Section E2, AS1720.1:2010"""
         r = self.r if self.r > 0 else 0.25
         # NOTE - some of this term is a material attribute only
         if self.mat.seasoned:
             rho = 14.71 * (self.mat.E / self.mat.f_b) ** (-0.480) * r ** (-0.061)
         else:
@@ -278,14 +378,18 @@
 
     @property
     def L_CLR(self) -> float:
         """Clause"""
         raise NotImplementedError
 
     @property
+    def CLR(self) -> bool:
+        raise NotImplementedError
+
+    @property
     def k_4(self) -> float:
         """Table 2.5, AS1720.1:2010"""
         if self.mat.seasoned:
             return 1.0
         elif not self.consider_partial_seasoning:
             return 1.0
         else:  # material is unseasoned and consider_partial_seasoning
@@ -302,15 +406,15 @@
             else:
                 raise NotImplementedError(
                     f"{self.sec.d} not defined for k_4 partial seasoning factor"
                 )
 
     @property
     def k_6(self) -> float:
-        """Çlause 2.4.3, AS1720.1:2010"""
+        """Clause 2.4.3, AS1720.1:2010"""
         return self.k_6_lookup(self.mat.seasoned, self.high_temp_latitude)
 
     @property
     def k_9(self) -> float:
         """Modification factor for strength sharing. Clause 2.4.5.3, AS1720.1:2010.
         Not Implemented in TimberMember parent class, added in child classes."""
         raise NotImplementedError
@@ -333,14 +437,18 @@
         strength (y-axis). Clause 3.3.3, AS1720.1:2010."""
         return self.calc_k12_compression(self.rho_c, self.S4)
 
     @property
     def k_12_bend(self) -> float:
         """Modification factor for stability, to allow for slenderness effects on bending
         strength. Clause 3.2.4, AS1720.1:2010."""
+        if self.sec.I_x < self.sec.I_y:
+            # x axis is minor axis
+            print("note - x-axis is minor axis, k_12_bend = 1.0")
+            return 1.0
         return self.calc_k12_bending(self.rho_b, self.S1)
 
     def k_6_lookup(self, seasoned: bool, high_temp_latitude: float) -> float:
         """Modification factor for strength for the effect of temperature.
         Clause 2.4.3, AS1720.1:2010."""
         if seasoned and high_temp_latitude:
             k_6 = 0.9
@@ -365,59 +473,100 @@
             return 1.0
         if rho_times_s >= 10 and rho_times_s <= 20:
             return 1.5 - (0.05 * rho_times_s)
         if rho_times_s >= 20:
             return 200 / ((rho_times_s) ** 2)
 
 
-class BoardMember(TimberMember):
+class RectangleMemberStabilityMixin:
     """TODO"""
 
     @property
     def S1(self) -> float:
-        """Clause 3.2.3.2(b), AS1720.1:2010"""
+        """Clause   (b), AS1720.1:2010"""
         # Continuous restraint, tension edge
         # NOTE -> self.b for single and multiboard?
-        match self.restraint:
-            case BendingRestraint.DISCRETE_LATERAL_RESTRAINT_COMPRESSION_EDGE:
-                val = 1.25 * self.sec.d / self.sec.b * (self.L_ay / self.sec.d) ** 0.5
-            case BendingRestraint.DISCRETE_LATERAL_RESTRAINT_TENSION_EDGE:
-                val = (self.sec.d / self.sec.b) ** 1.35 * (
-                    self.L_ay / self.sec.d
-                ) ** 0.25
-            case BendingRestraint.CONTINUOUS_LATERAL_RESTRAINT_COMPRESSION_EDGE:
-                val = 2.25 * self.sec.d / self.sec.b
-            case BendingRestraint.CONTINUOUS_LATERAL_RESTRAINT_TENSION_EDGE:
-                bot = (((math.pi * self.sec.d) / self.L_ar) ** 2 + 0.4) ** 0.5
-                val = 1.5 * (self.sec.d / self.sec.b) / bot
+
+        if self.CLR:
+            # continuous restraint
+            match self.restraint_edge:
+                case RestraintEdge.COMPRESSION | RestraintEdge.BOTH:
+                    # continuous compression - Cl 3.2.3.2(b)
+                    val = 0
+                case RestraintEdge.TENSION:
+                    # continuous tension - Eq 3.2(7)
+                    val = 2.25 * self.sec.d / self.sec.b
+                case RestraintEdge.TENSION_AND_TORSIONAL:
+                    # continuous tension - Eq 3.2(8)
+                    bot = (((math.pi * self.sec.d) / self.L_a_phi) ** 2 + 0.4) ** 0.5
+                    val = 1.5 * (self.sec.d / self.sec.b) / bot
+        else:
+            # discrete restraint
+            match self.restraint_edge:
+                case RestraintEdge.COMPRESSION | RestraintEdge.BOTH:
+                    # discrete compression - Cl 3.2.3.2(a), Eq 3.2(4)
+                    val = (
+                        1.25 * self.sec.d / self.sec.b * (self.L_ay / self.sec.d) ** 0.5
+                    )
+                case RestraintEdge.TENSION:
+                    # discrete tension edge Cl 3.2.3.2(a), Eq 3.2(5)
+                    val = (self.sec.d / self.sec.b) ** 1.35 * (
+                        self.L_ay / self.sec.d
+                    ) ** 0.25
+                case RestraintEdge.TENSION_AND_TORSIONAL:
+                    raise ValueError(
+                        "restraint_edge error - discrete (non-continuous) tension edge"
+                        "restraint defined with torsional restraint - no formula for S1"
+                    )
 
         return round(val, 2)
 
     @property
     def S3(self) -> float:
-        """Slenderness coefficient for buckling about major axis in rectangular sections.
+        """Slenderness coefficient for buckling about x axis in rectangular sections.
         Clause 3.3.2.2(a), AS1720.1:2010."""
-        return round(self.g_13 * self.L / self.sec.d, 2)
+        return round(self.g_13_x * self.L / self.sec.d, 2)
+
+    @property
+    def L_CLR(self) -> float:
+        """3.2.3.2"""
+        # Eq 3.2(6)
+        val = 64 / self.sec.d * (self.sec.b / self.rho_b) ** 2
+        return val
+
+    @property
+    def CLR(self) -> bool:
+        # evaluate if lateral restraint is continuous
+        if self.L_ay <= self.L_CLR:
+            # continuous restraint
+            return True
+        return False
+
+
+class BoardMember(RectangleMemberStabilityMixin, TimberMember):
+    """TODO"""
+
+    # member spacing parameters for k_9 evaluation
+    # n_com: int = 1
+    n_mem: int = 1
+    s: float = 0  # member spacing
 
     @property
     def k_9(self) -> float:
         """Clause 2.4.5.3, AS1720.1:2010"""
         return max(
-            self.g_31
-            + (self.g_32 - self.g_31) * (1 - (2 * self.member_spacing / self.L)),
+            self.g_31 + (self.g_32 - self.g_31) * (1 - (2 * self.s / self.L)),
             1,
         )
 
-    # for n in n_all:
-
     @property
-    def L_CLR(self) -> float:
-        """3.2.3.2"""
-        val = 64 / self.sec.d * (self.sec.b / self.rho_b) ** 2
-        return val
+    def n_com(self) -> int:
+        if self.sec.n > 1:
+            return self.sec.n
+        return 1
 
     @property
     def g_31(self) -> float:
         """Table 2.7, AS1720.1:2010"""
         return self.g3_lookup(self.n_com)
 
     @property
@@ -456,14 +605,14 @@
     # def g32_lookup(self, n_cm: int) -> float:
     #     """Table 2.7, AS1720.1:2010"""
     #     # g31 = geometric factor for combined members in discrete parallel system
     #     g32 = self.g31_lookup(n_cm)
     #     return g32
 
 
-class GlulamMember(BoardMember):
+class GlulamMember(RectangleMemberStabilityMixin, TimberMember):
     """TODO"""
 
     @property
     def k_9(self) -> float:
         """TODO"""
         return 1.0
```

### Comparing `timberas-0.2.0/src/timberas.egg-info/PKG-INFO` & `timberas-0.3.0/src/timberas.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: timberas
-Version: 0.2.0
+Version: 0.3.0
 Summary: timberas is a Python package for the design of timber structures to relevant Australian Standards
 Author-email: Joe Gattas <j.gattas@uq.edu.au>
 Project-URL: Homepage, https://github.com/Folded-Structures-Lab/timber-as
 Keywords: AS1170,AS1684,timber structures,structural engineering
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
@@ -12,15 +12,15 @@
 Description-Content-Type: text/markdown
 License-File: LICENSE.md
 
 # About
 *timberas* is a Python package with tools to support research and design of Australian timber structures. It can be used to determine the material properties, section properties, and design capacities for structural members as per Australian Standard AS1720.1:2020 (Timber Structures Part 1: Design Methods). 
 
 # Documentation
-Detailed information on *timberas* is available in package documentation at [timberas.readthedocs.io](https://timberas.readthedocs.io/). This includes project background, examples, and an API reference guide.
+Detailed information on *timberas* is available in package documentation at [timberas.readthedocs.io](https://timber-as.readthedocs.io/). This includes project background, examples, and an API reference guide.
 
 # Installation
 *timberas* can be installed from the Python Package index:
 ```
 pip install timberas
 ```
 For more detailed instructions, please refer to the [documentation]([https://timberas.readthedocs.io]).
```

### Comparing `timberas-0.2.0/src/timberas.egg-info/SOURCES.txt` & `timberas-0.3.0/src/timberas.egg-info/SOURCES.txt`

 * *Files 15% similar despite different names*

```diff
@@ -4,29 +4,35 @@
 pyproject.toml
 docs/how-to-guides.md
 docs/index.md
 docs/install.md
 docs/reference.md
 docs/tutorial-1.md
 docs/tutorial-2.md
-examples/getting_started_1.py
-examples/getting_started_2.py
+docs/tutorial-3.md
+docs/tutorial-4.md
+examples/tutorial_1.py
+examples/tutorial_2.py
+examples/tutorial_3.py
+examples/tutorial_4.py
 src/timberas/AS1684_dicts.py
 src/timberas/__init__.py
 src/timberas/geometry.py
 src/timberas/material.py
 src/timberas/member.py
+src/timberas/utils.py
 src/timberas.egg-info/PKG-INFO
 src/timberas.egg-info/SOURCES.txt
 src/timberas.egg-info/dependency_links.txt
 src/timberas.egg-info/requires.txt
 src/timberas.egg-info/top_level.txt
 src/timberas/__pycache__/AS1684_dicts.cpython-310.pyc
 src/timberas/__pycache__/__init__.cpython-310.pyc
 src/timberas/__pycache__/geometry.cpython-310.pyc
 src/timberas/__pycache__/material.cpython-310.pyc
 src/timberas/__pycache__/member.cpython-310.pyc
+src/timberas/__pycache__/utils.cpython-310.pyc
 src/timberas/data/__init__.py
 src/timberas/data/material_library.csv
 src/timberas/data/section_library.csv
 src/timberas/data/__pycache__/__init__.cpython-310.pyc
 tests/test_materials.py
```

### Comparing `timberas-0.2.0/tests/test_materials.py` & `timberas-0.3.0/tests/test_materials.py`

 * *Files identical despite different names*

