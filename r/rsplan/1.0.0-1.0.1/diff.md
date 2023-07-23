# Comparing `tmp/rsplan-1.0.0.tar.gz` & `tmp/rsplan-1.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "rsplan-1.0.0.tar", last modified: Fri Jul 21 23:24:56 2023, max compression
+gzip compressed data, was "rsplan-1.0.1.tar", last modified: Sun Jul 23 20:14:42 2023, max compression
```

## Comparing `rsplan-1.0.0.tar` & `rsplan-1.0.1.tar`

### file list

```diff
@@ -1,21 +1,21 @@
-drwxrwxr-x   0 built     (1000) built     (1000)        0 2023-07-21 23:24:56.500264 rsplan-1.0.0/
--rw-rw-r--   0 built     (1000) built     (1000)     1070 2023-07-21 19:25:35.000000 rsplan-1.0.0/LICENSE
--rw-rw-r--   0 built     (1000) built     (1000)     5412 2023-07-21 23:24:56.500264 rsplan-1.0.0/PKG-INFO
--rw-rw-r--   0 built     (1000) built     (1000)     3755 2023-07-21 21:43:28.000000 rsplan-1.0.0/README.md
--rw-rw-r--   0 built     (1000) built     (1000)     1072 2023-07-21 23:24:37.000000 rsplan-1.0.0/pyproject.toml
-drwxrwxr-x   0 built     (1000) built     (1000)        0 2023-07-21 23:24:56.496264 rsplan-1.0.0/rsplan/
--rw-rw-r--   0 built     (1000) built     (1000)        0 2023-07-19 03:21:47.000000 rsplan-1.0.0/rsplan/__init__.py
--rw-rw-r--   0 built     (1000) built     (1000)    28371 2023-07-21 17:30:46.000000 rsplan-1.0.0/rsplan/curves.py
--rw-rw-r--   0 built     (1000) built     (1000)     2602 2023-07-21 17:30:46.000000 rsplan-1.0.0/rsplan/demo.py
--rw-rw-r--   0 built     (1000) built     (1000)     3082 2023-07-19 19:07:31.000000 rsplan-1.0.0/rsplan/helpers.py
--rw-rw-r--   0 built     (1000) built     (1000)     6515 2023-07-21 20:54:22.000000 rsplan-1.0.0/rsplan/planner.py
--rw-rw-r--   0 built     (1000) built     (1000)    11977 2023-07-21 17:30:35.000000 rsplan-1.0.0/rsplan/primitives.py
--rw-rw-r--   0 built     (1000) built     (1000)     5097 2023-07-21 17:29:59.000000 rsplan-1.0.0/rsplan/unit_tests.py
-drwxrwxr-x   0 built     (1000) built     (1000)        0 2023-07-21 23:24:56.496264 rsplan-1.0.0/rsplan.egg-info/
--rw-rw-r--   0 built     (1000) built     (1000)     5412 2023-07-21 23:24:56.000000 rsplan-1.0.0/rsplan.egg-info/PKG-INFO
--rw-rw-r--   0 built     (1000) built     (1000)      319 2023-07-21 23:24:56.000000 rsplan-1.0.0/rsplan.egg-info/SOURCES.txt
--rw-rw-r--   0 built     (1000) built     (1000)        1 2023-07-21 23:24:56.000000 rsplan-1.0.0/rsplan.egg-info/dependency_links.txt
--rw-rw-r--   0 built     (1000) built     (1000)       39 2023-07-21 23:24:56.000000 rsplan-1.0.0/rsplan.egg-info/requires.txt
--rw-rw-r--   0 built     (1000) built     (1000)        7 2023-07-21 23:24:56.000000 rsplan-1.0.0/rsplan.egg-info/top_level.txt
--rw-rw-r--   0 built     (1000) built     (1000)       38 2023-07-21 23:24:56.500264 rsplan-1.0.0/setup.cfg
--rw-rw-r--   0 built     (1000) built     (1000)      643 2023-07-21 23:24:26.000000 rsplan-1.0.0/setup.py
+drwxrwxr-x   0 built     (1000) built     (1000)        0 2023-07-23 20:14:42.366807 rsplan-1.0.1/
+-rw-rw-r--   0 built     (1000) built     (1000)     1070 2023-07-21 19:25:35.000000 rsplan-1.0.1/LICENSE
+-rw-rw-r--   0 built     (1000) built     (1000)     5412 2023-07-23 20:14:42.366807 rsplan-1.0.1/PKG-INFO
+-rw-rw-r--   0 built     (1000) built     (1000)     3755 2023-07-21 21:43:28.000000 rsplan-1.0.1/README.md
+-rw-rw-r--   0 built     (1000) built     (1000)     1072 2023-07-23 20:14:12.000000 rsplan-1.0.1/pyproject.toml
+drwxrwxr-x   0 built     (1000) built     (1000)        0 2023-07-23 20:14:42.366807 rsplan-1.0.1/rsplan/
+-rw-rw-r--   0 built     (1000) built     (1000)        0 2023-07-19 03:21:47.000000 rsplan-1.0.1/rsplan/__init__.py
+-rw-rw-r--   0 built     (1000) built     (1000)    28383 2023-07-23 20:09:00.000000 rsplan-1.0.1/rsplan/curves.py
+-rw-rw-r--   0 built     (1000) built     (1000)     2614 2023-07-23 20:09:06.000000 rsplan-1.0.1/rsplan/demo.py
+-rw-rw-r--   0 built     (1000) built     (1000)     3082 2023-07-19 19:07:31.000000 rsplan-1.0.1/rsplan/helpers.py
+-rw-rw-r--   0 built     (1000) built     (1000)     6527 2023-07-23 20:08:41.000000 rsplan-1.0.1/rsplan/planner.py
+-rw-rw-r--   0 built     (1000) built     (1000)    11977 2023-07-21 17:30:35.000000 rsplan-1.0.1/rsplan/primitives.py
+-rw-rw-r--   0 built     (1000) built     (1000)     5109 2023-07-23 20:08:55.000000 rsplan-1.0.1/rsplan/unit_tests.py
+drwxrwxr-x   0 built     (1000) built     (1000)        0 2023-07-23 20:14:42.366807 rsplan-1.0.1/rsplan.egg-info/
+-rw-rw-r--   0 built     (1000) built     (1000)     5412 2023-07-23 20:14:42.000000 rsplan-1.0.1/rsplan.egg-info/PKG-INFO
+-rw-rw-r--   0 built     (1000) built     (1000)      319 2023-07-23 20:14:42.000000 rsplan-1.0.1/rsplan.egg-info/SOURCES.txt
+-rw-rw-r--   0 built     (1000) built     (1000)        1 2023-07-23 20:14:42.000000 rsplan-1.0.1/rsplan.egg-info/dependency_links.txt
+-rw-rw-r--   0 built     (1000) built     (1000)       39 2023-07-23 20:14:42.000000 rsplan-1.0.1/rsplan.egg-info/requires.txt
+-rw-rw-r--   0 built     (1000) built     (1000)        7 2023-07-23 20:14:42.000000 rsplan-1.0.1/rsplan.egg-info/top_level.txt
+-rw-rw-r--   0 built     (1000) built     (1000)       38 2023-07-23 20:14:42.366807 rsplan-1.0.1/setup.cfg
+-rw-rw-r--   0 built     (1000) built     (1000)      643 2023-07-23 20:14:21.000000 rsplan-1.0.1/setup.py
```

### Comparing `rsplan-1.0.0/LICENSE` & `rsplan-1.0.1/LICENSE`

 * *Files identical despite different names*

### Comparing `rsplan-1.0.0/PKG-INFO` & `rsplan-1.0.1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: rsplan
-Version: 1.0.0
+Version: 1.0.1
 Summary: Reeds-Shepp algorithm implementation in Python
 Home-page: https://github.com/builtrobotics/rs
 Author: Built Robotics
 Author-email: Built Robotics <tarakapoor9@gmail.com>
 License: MIT License
         
         Copyright (c) 2023 Built Robotics
```

### Comparing `rsplan-1.0.0/README.md` & `rsplan-1.0.1/README.md`

 * *Files identical despite different names*

### Comparing `rsplan-1.0.0/pyproject.toml` & `rsplan-1.0.1/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 
 [build-system]
 requires      = ["setuptools>=61.0.0", "wheel"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "rsplan"
-version = "1.0.0"
+version = "1.0.1"
 description = "Reeds-Shepp algorithm implementation in Python"
 readme = "README.md"
 authors = [{ name = "Built Robotics", email = "tarakapoor9@gmail.com" }]
 license = { file = "LICENSE" }
 classifiers = [
     "License :: OSI Approved :: MIT License",
     "Programming Language :: Python",
```

### Comparing `rsplan-1.0.0/rsplan/curves.py` & `rsplan-1.0.1/rsplan/curves.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 from itertools import chain
 from typing import Callable, List, Literal, Optional, Tuple
 
 import numpy as np
 
-import helpers, primitives
+from rsplan import helpers, primitives
 
 """This file outlines curve calculations for the 48 different Reeds-Shepp path types.
 A "|" cusp means direction change between the curves (+ to -, - to +).
 
 As a whole, t, u, v are segment parameters generated in each of the curve helper
 functions that represent the distance (angular distance for curved segments, linear
 distance for straight segments) of their respective segments.
```

### Comparing `rsplan-1.0.0/rsplan/demo.py` & `rsplan-1.0.1/rsplan/demo.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from __future__ import annotations
 
 from typing import List, Tuple
 
 import matplotlib.pyplot as plt  # type: ignore[import]
 import numpy as np
 
-import planner, primitives
+from rsplan import planner, primitives
 
 # List of path endpoints to visualize Reeds-Shepp paths for with matplotlib.
 # Format: (end x, end y, end yaw, turn radius, runway length)
 _END_POSES: List[Tuple[float, float, float, int, float]] = [
     (5, 6, np.pi, 1, 0),
     (15, 3, np.pi / 2.0, 2, 6),
     (-2, -4, np.pi, 4, 3),
```

### Comparing `rsplan-1.0.0/rsplan/helpers.py` & `rsplan-1.0.1/rsplan/helpers.py`

 * *Files identical despite different names*

### Comparing `rsplan-1.0.0/rsplan/planner.py` & `rsplan-1.0.1/rsplan/planner.py`

 * *Files 1% similar despite different names*

```diff
@@ -20,15 +20,15 @@
 have a total length within 2 meters of each others.
 """
 
 from typing import List, Literal, Tuple
 
 import numpy as np
 
-import curves, helpers, primitives
+from rsplan import curves, helpers, primitives
 
 
 def path(
     start_pt: Tuple[float, float, float],
     end_pt: Tuple[float, float, float],
     turn_radius: float,
     runway_length: float,
```

### Comparing `rsplan-1.0.0/rsplan/primitives.py` & `rsplan-1.0.1/rsplan/primitives.py`

 * *Files identical despite different names*

### Comparing `rsplan-1.0.0/rsplan/unit_tests.py` & `rsplan-1.0.1/rsplan/unit_tests.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 from typing import List, Tuple
 
 import numpy as np
 import pytest
 
-import helpers, planner, primitives
+from rsplan import helpers, planner, primitives
 
 _STEP_SIZE = 0.05  # in meters
 _RANDOM_PATH_DISTANCE_RANGE = 10  # in meters
 _RANDOM_PATH_ANGLE_RANGE = 2 * np.pi  # radians
 
 _ORIGIN = (0.0, 0.0, 0.0)
 _TRANSLATED = (4, 7, 0)
```

### Comparing `rsplan-1.0.0/rsplan.egg-info/PKG-INFO` & `rsplan-1.0.1/rsplan.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: rsplan
-Version: 1.0.0
+Version: 1.0.1
 Summary: Reeds-Shepp algorithm implementation in Python
 Home-page: https://github.com/builtrobotics/rs
 Author: Built Robotics
 Author-email: Built Robotics <tarakapoor9@gmail.com>
 License: MIT License
         
         Copyright (c) 2023 Built Robotics
```

### Comparing `rsplan-1.0.0/setup.py` & `rsplan-1.0.1/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 from setuptools import setup
 
 def read(fname):
     return open(os.path.join(os.path.dirname(__file__), fname)).read()
 
 setup(
     name = "rsplan",
-    version = "1.0.0",
+    version = "1.0.1",
     author = "Built Robotics",
     author_email = "tarakapoor9@gmail.com",
     description = ("Reeds-Shepp algorithm implementation in Python."),
     license = "MIT",
     keywords = "reeds-shepp path planning",
     url = "https://github.com/builtrobotics/rs",
     packages=['rsplan'],
```

