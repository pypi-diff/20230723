# Comparing `tmp/Signal8-5.0.1.tar.gz` & `tmp/Signal8-5.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "Signal8-5.0.1.tar", last modified: Sun Jul 23 00:45:18 2023, max compression
+gzip compressed data, was "Signal8-5.0.2.tar", last modified: Sun Jul 23 21:41:40 2023, max compression
```

## Comparing `Signal8-5.0.1.tar` & `Signal8-5.0.2.tar`

### file list

```diff
@@ -1,22 +1,22 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 00:45:18.358195 Signal8-5.0.1/
--rw-rw-rw-   0        0        0     1089 2023-04-10 03:39:38.000000 Signal8-5.0.1/LICENSE
--rw-rw-rw-   0        0        0     5300 2023-07-23 00:45:18.342193 Signal8-5.0.1/PKG-INFO
--rw-rw-rw-   0        0        0     4800 2023-07-22 22:09:51.000000 Signal8-5.0.1/README.md
-drwxrwxrwx   0        0        0        0 2023-07-23 00:45:18.238193 Signal8-5.0.1/Signal8/
--rw-rw-rw-   0        0        0    11418 2023-07-23 00:42:01.000000 Signal8-5.0.1/Signal8/Signal8.py
--rw-rw-rw-   0        0        0       24 2023-06-19 21:16:46.000000 Signal8-5.0.1/Signal8/__init__.py
--rw-rw-rw-   0        0        0     3252 2023-07-23 00:27:57.000000 Signal8-5.0.1/Signal8/main.py
-drwxrwxrwx   0        0        0        0 2023-07-23 00:45:18.337193 Signal8-5.0.1/Signal8/utils/
--rw-rw-rw-   0        0        0        0 2023-05-19 05:01:34.000000 Signal8-5.0.1/Signal8/utils/__init__.py
--rw-rw-rw-   0        0        0     5299 2023-07-22 23:36:30.000000 Signal8-5.0.1/Signal8/utils/core.py
--rw-rw-rw-   0        0        0     2326 2023-07-23 00:27:30.000000 Signal8-5.0.1/Signal8/utils/problems.py
--rw-rw-rw-   0        0        0      292 2023-02-28 21:08:59.000000 Signal8-5.0.1/Signal8/utils/scenario.py
--rw-rw-rw-   0        0        0    11976 2023-07-22 23:36:18.000000 Signal8-5.0.1/Signal8/utils/simple_env.py
--rw-rw-rw-   0        0        0     1659 2023-06-08 18:48:20.000000 Signal8-5.0.1/Signal8/utils/test_dynamic_obs.py
-drwxrwxrwx   0        0        0        0 2023-07-23 00:45:18.297193 Signal8-5.0.1/Signal8.egg-info/
--rw-rw-rw-   0        0        0     5300 2023-07-23 00:45:17.000000 Signal8-5.0.1/Signal8.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      510 2023-07-23 00:45:18.000000 Signal8-5.0.1/Signal8.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 00:45:17.000000 Signal8-5.0.1/Signal8.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        8 2023-07-23 00:45:17.000000 Signal8-5.0.1/Signal8.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-23 00:45:18.359193 Signal8-5.0.1/setup.cfg
--rw-rw-rw-   0        0        0      647 2023-07-23 00:44:56.000000 Signal8-5.0.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 21:41:40.097639 Signal8-5.0.2/
+-rw-rw-rw-   0        0        0     1089 2023-04-10 03:39:38.000000 Signal8-5.0.2/LICENSE
+-rw-rw-rw-   0        0        0     5300 2023-07-23 21:41:40.094642 Signal8-5.0.2/PKG-INFO
+-rw-rw-rw-   0        0        0     4800 2023-07-22 22:09:51.000000 Signal8-5.0.2/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 21:41:40.035640 Signal8-5.0.2/Signal8/
+-rw-rw-rw-   0        0        0    11576 2023-07-23 21:39:18.000000 Signal8-5.0.2/Signal8/Signal8.py
+-rw-rw-rw-   0        0        0       24 2023-06-19 21:16:46.000000 Signal8-5.0.2/Signal8/__init__.py
+-rw-rw-rw-   0        0        0     3301 2023-07-23 21:38:25.000000 Signal8-5.0.2/Signal8/main.py
+drwxrwxrwx   0        0        0        0 2023-07-23 21:41:40.090639 Signal8-5.0.2/Signal8/utils/
+-rw-rw-rw-   0        0        0        0 2023-05-19 05:01:34.000000 Signal8-5.0.2/Signal8/utils/__init__.py
+-rw-rw-rw-   0        0        0     5299 2023-07-22 23:36:30.000000 Signal8-5.0.2/Signal8/utils/core.py
+-rw-rw-rw-   0        0        0     2326 2023-07-23 00:27:30.000000 Signal8-5.0.2/Signal8/utils/problems.py
+-rw-rw-rw-   0        0        0      292 2023-02-28 21:08:59.000000 Signal8-5.0.2/Signal8/utils/scenario.py
+-rw-rw-rw-   0        0        0    11976 2023-07-22 23:36:18.000000 Signal8-5.0.2/Signal8/utils/simple_env.py
+-rw-rw-rw-   0        0        0     1659 2023-06-08 18:48:20.000000 Signal8-5.0.2/Signal8/utils/test_dynamic_obs.py
+drwxrwxrwx   0        0        0        0 2023-07-23 21:41:40.073638 Signal8-5.0.2/Signal8.egg-info/
+-rw-rw-rw-   0        0        0     5300 2023-07-23 21:41:39.000000 Signal8-5.0.2/Signal8.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      510 2023-07-23 21:41:39.000000 Signal8-5.0.2/Signal8.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 21:41:39.000000 Signal8-5.0.2/Signal8.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        8 2023-07-23 21:41:39.000000 Signal8-5.0.2/Signal8.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 21:41:40.097639 Signal8-5.0.2/setup.cfg
+-rw-rw-rw-   0        0        0      647 2023-07-23 21:40:56.000000 Signal8-5.0.2/setup.py
```

### Comparing `Signal8-5.0.1/LICENSE` & `Signal8-5.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `Signal8-5.0.1/PKG-INFO` & `Signal8-5.0.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: Signal8
-Version: 5.0.1
+Version: 5.0.2
 Summary: A multi-agent environment inspired by the Lewis Signaling Game, featuring eight unique problem configurations with both static and dynamic obstacles.
 Home-page: https://github.com/ethanmclark1/signal8
 Author: Ethan Clark
 Author-email: eclark715@gmail.com.com
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python
 Description-Content-Type: text/markdown
```

### Comparing `Signal8-5.0.1/README.md` & `Signal8-5.0.2/README.md`

 * *Files identical despite different names*

### Comparing `Signal8-5.0.1/Signal8/Signal8.py` & `Signal8-5.0.2/Signal8/Signal8.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import numpy as np
 import matplotlib.path as mpath
 
 from functools import partial
-from utils.scenario import BaseScenario
-from utils.simple_env import SimpleEnv, make_env
-from utils.core import Agent, Goal, Obstacle, World
-from utils.problems import get_problem_list, get_problem_instance
+from .utils.scenario import BaseScenario
+from .utils.simple_env import SimpleEnv, make_env
+from .utils.core import Agent, Goal, Obstacle, World
+from .utils.problems import get_problem_list, get_problem_instance
 
 from gymnasium.utils import EzPickle
 
 
 class raw_env(SimpleEnv, EzPickle):
     def __init__(
         self, 
@@ -85,15 +85,16 @@
         return point
 
     # Check if point is outside of triangular obstacle regions
     def _outside_triangle(self, point, paths, epsilon):
         enlarged_paths = []
         for path in paths:
             centroid = np.mean(path.vertices, axis=0)
-            enlarged_vertices = centroid + (1 + epsilon) * (path.vertices - centroid)
+            # Make the triangle larger by moving each vertex away from the centroid by the `epsilon` distance
+            enlarged_vertices = centroid + (1 + epsilon) * (path.vertices - centroid) / np.linalg.norm(centroid - path.vertices)
             enlarged_paths.append(mpath.Path(enlarged_vertices))
         return not any(path.contains_points(point[None, :]) for path in enlarged_paths)
     
     # Check if point is outside of circular obstacle regions
     def _outside_circles(self, point, centers_radii, epsilon):
         return not any(np.linalg.norm(point - center) <= radius + epsilon for center, radius in centers_radii)
```

### Comparing `Signal8-5.0.1/Signal8/main.py` & `Signal8-5.0.2/Signal8/main.py`

 * *Files 3% similar despite different names*

```diff
@@ -63,20 +63,18 @@
     lines = MultiLineString(valid_lines).buffer(distance=distance)
     boundary = lines.convex_hull
     polygons = boundary.difference(lines)
     regions = [polygons] if polygons.geom_type == 'Polygon' else list(polygons.geoms)
     return regions
 
 
-
-
 env = signal8.env()
-given_list = [1, 1, 0.95, 1, -1, 0.95, -1, 1, 0.95, -1, -1, 0.95]
-problem_instance = 'corners'
-# test_coeffs(given_list)
+given_list =  [0.38, -1, 0.9, 0.38, -1, 0.275, 0.93, -1, -0.05, 0.93, -1, -0.8, -1, -0.474, -0.15, -1, -0.143, 0.8]
+problem_instance = 'right_arrows'
+test_coeffs(given_list)
 
 agent_radius = env.unwrapped.world.agents[0].radius
 obstacle_radius = env.unwrapped.world.large_obstacles[0].radius
 
 for i in range(100):
     env.reset(options={'problem_instance': problem_instance})
     start_state = env.state()
```

### Comparing `Signal8-5.0.1/Signal8/utils/core.py` & `Signal8-5.0.2/Signal8/utils/core.py`

 * *Files identical despite different names*

### Comparing `Signal8-5.0.1/Signal8/utils/problems.py` & `Signal8-5.0.2/Signal8/utils/problems.py`

 * *Files identical despite different names*

### Comparing `Signal8-5.0.1/Signal8/utils/simple_env.py` & `Signal8-5.0.2/Signal8/utils/simple_env.py`

 * *Files identical despite different names*

### Comparing `Signal8-5.0.1/Signal8/utils/test_dynamic_obs.py` & `Signal8-5.0.2/Signal8/utils/test_dynamic_obs.py`

 * *Files identical despite different names*

### Comparing `Signal8-5.0.1/Signal8.egg-info/PKG-INFO` & `Signal8-5.0.2/Signal8.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: Signal8
-Version: 5.0.1
+Version: 5.0.2
 Summary: A multi-agent environment inspired by the Lewis Signaling Game, featuring eight unique problem configurations with both static and dynamic obstacles.
 Home-page: https://github.com/ethanmclark1/signal8
 Author: Ethan Clark
 Author-email: eclark715@gmail.com.com
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python
 Description-Content-Type: text/markdown
```

### Comparing `Signal8-5.0.1/setup.py` & `Signal8-5.0.2/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name="Signal8",
-    version="5.0.1",
+    version="5.0.2",
     packages=find_packages(),
     author="Ethan Clark",
     author_email="eclark715@gmail.com.com",
     description="A multi-agent environment inspired by the Lewis Signaling Game, featuring eight unique problem configurations with both static and dynamic obstacles.",
     long_description=open('README.md').read(),
     long_description_content_type='text/markdown',
     url="https://github.com/ethanmclark1/signal8",
```

