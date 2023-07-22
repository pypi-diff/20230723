# Comparing `tmp/Signal8-4.94.tar.gz` & `tmp/Signal8-4.95.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "Signal8-4.94.tar", last modified: Fri Jul 21 00:30:32 2023, max compression
+gzip compressed data, was "Signal8-4.95.tar", last modified: Sat Jul 22 22:10:25 2023, max compression
```

## Comparing `Signal8-4.94.tar` & `Signal8-4.95.tar`

### file list

```diff
@@ -1,22 +1,22 @@
-drwxrwxrwx   0        0        0        0 2023-07-21 00:30:32.738595 Signal8-4.94/
--rw-rw-rw-   0        0        0     1089 2023-04-10 03:39:38.000000 Signal8-4.94/LICENSE
--rw-rw-rw-   0        0        0     6075 2023-07-21 00:30:32.737595 Signal8-4.94/PKG-INFO
--rw-rw-rw-   0        0        0     5576 2023-07-21 00:28:58.000000 Signal8-4.94/README.md
-drwxrwxrwx   0        0        0        0 2023-07-21 00:30:32.626595 Signal8-4.94/Signal8/
--rw-rw-rw-   0        0        0    11167 2023-07-20 21:05:39.000000 Signal8-4.94/Signal8/Signal8.py
--rw-rw-rw-   0        0        0       24 2023-06-19 21:16:46.000000 Signal8-4.94/Signal8/__init__.py
--rw-rw-rw-   0        0        0      240 2023-07-17 21:38:01.000000 Signal8-4.94/Signal8/main.py
-drwxrwxrwx   0        0        0        0 2023-07-21 00:30:32.731596 Signal8-4.94/Signal8/utils/
--rw-rw-rw-   0        0        0        0 2023-05-19 05:01:34.000000 Signal8-4.94/Signal8/utils/__init__.py
--rw-rw-rw-   0        0        0     5285 2023-07-14 01:01:24.000000 Signal8-4.94/Signal8/utils/core.py
--rw-rw-rw-   0        0        0     2328 2023-07-20 21:04:43.000000 Signal8-4.94/Signal8/utils/problems.py
--rw-rw-rw-   0        0        0      292 2023-02-28 21:08:59.000000 Signal8-4.94/Signal8/utils/scenario.py
--rw-rw-rw-   0        0        0    11960 2023-07-13 18:01:37.000000 Signal8-4.94/Signal8/utils/simple_env.py
--rw-rw-rw-   0        0        0     1659 2023-06-08 18:48:20.000000 Signal8-4.94/Signal8/utils/test_dynamic_obs.py
-drwxrwxrwx   0        0        0        0 2023-07-21 00:30:32.717594 Signal8-4.94/Signal8.egg-info/
--rw-rw-rw-   0        0        0     6075 2023-07-21 00:30:32.000000 Signal8-4.94/Signal8.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      510 2023-07-21 00:30:32.000000 Signal8-4.94/Signal8.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-21 00:30:32.000000 Signal8-4.94/Signal8.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        8 2023-07-21 00:30:32.000000 Signal8-4.94/Signal8.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-21 00:30:32.739596 Signal8-4.94/setup.cfg
--rw-rw-rw-   0        0        0      646 2023-07-20 21:05:58.000000 Signal8-4.94/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-22 22:10:25.838349 Signal8-4.95/
+-rw-rw-rw-   0        0        0     1089 2023-04-10 03:39:38.000000 Signal8-4.95/LICENSE
+-rw-rw-rw-   0        0        0     5299 2023-07-22 22:10:25.837349 Signal8-4.95/PKG-INFO
+-rw-rw-rw-   0        0        0     4800 2023-07-22 22:09:51.000000 Signal8-4.95/README.md
+drwxrwxrwx   0        0        0        0 2023-07-22 22:10:25.726347 Signal8-4.95/Signal8/
+-rw-rw-rw-   0        0        0    11149 2023-07-22 22:05:52.000000 Signal8-4.95/Signal8/Signal8.py
+-rw-rw-rw-   0        0        0       24 2023-06-19 21:16:46.000000 Signal8-4.95/Signal8/__init__.py
+-rw-rw-rw-   0        0        0      241 2023-07-22 21:54:42.000000 Signal8-4.95/Signal8/main.py
+drwxrwxrwx   0        0        0        0 2023-07-22 22:10:25.831347 Signal8-4.95/Signal8/utils/
+-rw-rw-rw-   0        0        0        0 2023-05-19 05:01:34.000000 Signal8-4.95/Signal8/utils/__init__.py
+-rw-rw-rw-   0        0        0     5285 2023-07-14 01:01:24.000000 Signal8-4.95/Signal8/utils/core.py
+-rw-rw-rw-   0        0        0     2328 2023-07-20 21:04:43.000000 Signal8-4.95/Signal8/utils/problems.py
+-rw-rw-rw-   0        0        0      292 2023-02-28 21:08:59.000000 Signal8-4.95/Signal8/utils/scenario.py
+-rw-rw-rw-   0        0        0    11960 2023-07-13 18:01:37.000000 Signal8-4.95/Signal8/utils/simple_env.py
+-rw-rw-rw-   0        0        0     1659 2023-06-08 18:48:20.000000 Signal8-4.95/Signal8/utils/test_dynamic_obs.py
+drwxrwxrwx   0        0        0        0 2023-07-22 22:10:25.774347 Signal8-4.95/Signal8.egg-info/
+-rw-rw-rw-   0        0        0     5299 2023-07-22 22:10:25.000000 Signal8-4.95/Signal8.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      510 2023-07-22 22:10:25.000000 Signal8-4.95/Signal8.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-22 22:10:25.000000 Signal8-4.95/Signal8.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        8 2023-07-22 22:10:25.000000 Signal8-4.95/Signal8.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-22 22:10:25.841351 Signal8-4.95/setup.cfg
+-rw-rw-rw-   0        0        0      646 2023-07-22 22:09:16.000000 Signal8-4.95/setup.py
```

### Comparing `Signal8-4.94/LICENSE` & `Signal8-4.95/LICENSE`

 * *Files identical despite different names*

### Comparing `Signal8-4.94/PKG-INFO` & `Signal8-4.95/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: Signal8
-Version: 4.94
+Version: 4.95
 Summary: A multi-agent environment inspired by the Lewis Signaling Game, featuring eight unique problem configurations with both static and dynamic obstacles.
 Home-page: https://github.com/ethanmclark1/signal8
 Author: Ethan Clark
 Author-email: eclark715@gmail.com.com
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python
 Description-Content-Type: text/markdown
@@ -12,22 +12,20 @@
 
 # An Extension of Multi-Agent Particle Environment
 
 Signal8 is an enhancement on top of the Simple environment, originally developed by the [Farama Foundation](https://farama.org/) as part of their [Multi-Agent Particle Environment (MPE)](https://pettingzoo.farama.org/environments/mpe/).
 
 # Signal8
 
-Signal8 is an open-source research project aimed advancing the development of communication strategies in multi-agent systems. The project proposes a unique environment that emphasizes the principles of the Lewis signaling game. This distinct setting serves as a testing ground for advancing robot-to-robot communication protocols.
+Signal8 is an open-source research project aimed at advancing the development of communication strategies in multi-agent systems. The project proposes a unique environment that emphasizes the principles of the Lewis signaling game. This distinct setting serves as a testing ground for advancing robot-to-robot communication protocols.
 
 Each problem set within Signal8 introduces different constraints on entity positioning such as start points, goals, and obstacles. This dynamic aspect encourages the investigation of communication strategies in diverse settings, enhancing the environment's adaptability and realism.
 
 A notable characteristic of Signal8 is its incorporation of asymmetric information, whereby two types of agents â€“ an 'eye in the sky' agent with global information and ground agents with only local information â€“ operate simultaneously. This asymmetry replicates real-world situations, presenting challenges for the development of efficient communication strategies. It also provides intriguing prospects for the generation of context-dependent language and high-level directives.
 
-In Signal8, obstacles are split into two categories: large obstacles that are observable exclusively by the aerial agents, and small obstacles which are observable to ground agents only. This distinct division introduces further complexity for agents navigating the environment. Large obstacles serve as barriers that define the structure of the environment, while small obstacles, appearing unpredictably within the vicinity of the ground agents. Both large and small obstacles remain stationary throughout the instance, adding an element of constant challenge to the environment. This multi-layered design richly expands the realism and complexity of the environment, making Signal8 a more demanding and intriguing platform for testing multi-agent communication strategies.
-
 For additional information on utilizing the environment API, please refer to the [PettingZoo API documentation](https://pettingzoo.farama.org/content/basic_usage/).
 
 ## Installation
 
 ```
 git clone https://github.com/ethanmclark1/signal8.git
 cd signal8
```

### Comparing `Signal8-4.94/README.md` & `Signal8-4.95/README.md`

 * *Files 8% similar despite different names*

```diff
@@ -1,21 +1,19 @@
 # An Extension of Multi-Agent Particle Environment
 
 Signal8 is an enhancement on top of the Simple environment, originally developed by the [Farama Foundation](https://farama.org/) as part of their [Multi-Agent Particle Environment (MPE)](https://pettingzoo.farama.org/environments/mpe/).
 
 # Signal8
 
-Signal8 is an open-source research project aimed advancing the development of communication strategies in multi-agent systems. The project proposes a unique environment that emphasizes the principles of the Lewis signaling game. This distinct setting serves as a testing ground for advancing robot-to-robot communication protocols.
+Signal8 is an open-source research project aimed at advancing the development of communication strategies in multi-agent systems. The project proposes a unique environment that emphasizes the principles of the Lewis signaling game. This distinct setting serves as a testing ground for advancing robot-to-robot communication protocols.
 
 Each problem set within Signal8 introduces different constraints on entity positioning such as start points, goals, and obstacles. This dynamic aspect encourages the investigation of communication strategies in diverse settings, enhancing the environment's adaptability and realism.
 
 A notable characteristic of Signal8 is its incorporation of asymmetric information, whereby two types of agents – an 'eye in the sky' agent with global information and ground agents with only local information – operate simultaneously. This asymmetry replicates real-world situations, presenting challenges for the development of efficient communication strategies. It also provides intriguing prospects for the generation of context-dependent language and high-level directives.
 
-In Signal8, obstacles are split into two categories: large obstacles that are observable exclusively by the aerial agents, and small obstacles which are observable to ground agents only. This distinct division introduces further complexity for agents navigating the environment. Large obstacles serve as barriers that define the structure of the environment, while small obstacles, appearing unpredictably within the vicinity of the ground agents. Both large and small obstacles remain stationary throughout the instance, adding an element of constant challenge to the environment. This multi-layered design richly expands the realism and complexity of the environment, making Signal8 a more demanding and intriguing platform for testing multi-agent communication strategies.
-
 For additional information on utilizing the environment API, please refer to the [PettingZoo API documentation](https://pettingzoo.farama.org/content/basic_usage/).
 
 ## Installation
 
 ```
 git clone https://github.com/ethanmclark1/signal8.git
 cd signal8
```

### Comparing `Signal8-4.94/Signal8/Signal8.py` & `Signal8-4.95/Signal8/Signal8.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import numpy as np
 import matplotlib.path as mpath
 
 from functools import partial
-from .utils.scenario import BaseScenario
-from .utils.simple_env import SimpleEnv, make_env
-from .utils.core import Agent, Goal, Obstacle, World
-from .utils.problems import get_problem_list, get_problem_instance
+from utils.scenario import BaseScenario
+from utils.simple_env import SimpleEnv, make_env
+from utils.core import Agent, Goal, Obstacle, World
+from utils.problems import get_problem_list, get_problem_instance
 
 from gymnasium.utils import EzPickle
 
 
 class raw_env(SimpleEnv, EzPickle):
     def __init__(
         self, 
@@ -84,18 +84,18 @@
                 break
         return point
 
     # Check if point is outside of triangular obstacle regions
     def _outside_triangle(self, point, paths, epsilon):
         enlarged_paths = []
         for path in paths:
-            centroid = np.mean(path.vertices[:-1], axis=0)
+            centroid = np.mean(path.vertices, axis=0)
             enlarged_vertices = path.vertices + epsilon * (path.vertices - centroid)
             enlarged_paths.append(mpath.Path(enlarged_vertices))
-        return not any(path.contains_points(point[None, :]) for path in enlarged_paths)
+        return not any(path.contains_points(point) for path in enlarged_paths)
     
     # Check if point is outside of circular obstacle regions
     def _outside_circles(self, point, centers_radii, epsilon):
         return not any(np.linalg.norm(point - center) <= radius + epsilon for center, radius in centers_radii)
     
     # Check if point is outside of rectangular obstacle regions
     def _outside_rectangle(self, point, x_constraints, y_constraints, epsilon):
```

### Comparing `Signal8-4.94/Signal8/utils/core.py` & `Signal8-4.95/Signal8/utils/core.py`

 * *Files identical despite different names*

### Comparing `Signal8-4.94/Signal8/utils/problems.py` & `Signal8-4.95/Signal8/utils/problems.py`

 * *Files identical despite different names*

### Comparing `Signal8-4.94/Signal8/utils/simple_env.py` & `Signal8-4.95/Signal8/utils/simple_env.py`

 * *Files identical despite different names*

### Comparing `Signal8-4.94/Signal8/utils/test_dynamic_obs.py` & `Signal8-4.95/Signal8/utils/test_dynamic_obs.py`

 * *Files identical despite different names*

### Comparing `Signal8-4.94/Signal8.egg-info/PKG-INFO` & `Signal8-4.95/Signal8.egg-info/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: Signal8
-Version: 4.94
+Version: 4.95
 Summary: A multi-agent environment inspired by the Lewis Signaling Game, featuring eight unique problem configurations with both static and dynamic obstacles.
 Home-page: https://github.com/ethanmclark1/signal8
 Author: Ethan Clark
 Author-email: eclark715@gmail.com.com
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python
 Description-Content-Type: text/markdown
@@ -12,22 +12,20 @@
 
 # An Extension of Multi-Agent Particle Environment
 
 Signal8 is an enhancement on top of the Simple environment, originally developed by the [Farama Foundation](https://farama.org/) as part of their [Multi-Agent Particle Environment (MPE)](https://pettingzoo.farama.org/environments/mpe/).
 
 # Signal8
 
-Signal8 is an open-source research project aimed advancing the development of communication strategies in multi-agent systems. The project proposes a unique environment that emphasizes the principles of the Lewis signaling game. This distinct setting serves as a testing ground for advancing robot-to-robot communication protocols.
+Signal8 is an open-source research project aimed at advancing the development of communication strategies in multi-agent systems. The project proposes a unique environment that emphasizes the principles of the Lewis signaling game. This distinct setting serves as a testing ground for advancing robot-to-robot communication protocols.
 
 Each problem set within Signal8 introduces different constraints on entity positioning such as start points, goals, and obstacles. This dynamic aspect encourages the investigation of communication strategies in diverse settings, enhancing the environment's adaptability and realism.
 
 A notable characteristic of Signal8 is its incorporation of asymmetric information, whereby two types of agents â€“ an 'eye in the sky' agent with global information and ground agents with only local information â€“ operate simultaneously. This asymmetry replicates real-world situations, presenting challenges for the development of efficient communication strategies. It also provides intriguing prospects for the generation of context-dependent language and high-level directives.
 
-In Signal8, obstacles are split into two categories: large obstacles that are observable exclusively by the aerial agents, and small obstacles which are observable to ground agents only. This distinct division introduces further complexity for agents navigating the environment. Large obstacles serve as barriers that define the structure of the environment, while small obstacles, appearing unpredictably within the vicinity of the ground agents. Both large and small obstacles remain stationary throughout the instance, adding an element of constant challenge to the environment. This multi-layered design richly expands the realism and complexity of the environment, making Signal8 a more demanding and intriguing platform for testing multi-agent communication strategies.
-
 For additional information on utilizing the environment API, please refer to the [PettingZoo API documentation](https://pettingzoo.farama.org/content/basic_usage/).
 
 ## Installation
 
 ```
 git clone https://github.com/ethanmclark1/signal8.git
 cd signal8
```

### Comparing `Signal8-4.94/setup.py` & `Signal8-4.95/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name="Signal8",
-    version="4.94",
+    version="4.95",
     packages=find_packages(),
     author="Ethan Clark",
     author_email="eclark715@gmail.com.com",
     description="A multi-agent environment inspired by the Lewis Signaling Game, featuring eight unique problem configurations with both static and dynamic obstacles.",
     long_description=open('README.md').read(),
     long_description_content_type='text/markdown',
     url="https://github.com/ethanmclark1/signal8",
```

