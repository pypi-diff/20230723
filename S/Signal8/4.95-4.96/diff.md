# Comparing `tmp/Signal8-4.95.tar.gz` & `tmp/Signal8-4.96.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "Signal8-4.95.tar", last modified: Sat Jul 22 22:10:25 2023, max compression
+gzip compressed data, was "Signal8-4.96.tar", last modified: Sat Jul 22 22:13:31 2023, max compression
```

## Comparing `Signal8-4.95.tar` & `Signal8-4.96.tar`

### file list

```diff
@@ -1,22 +1,22 @@
-drwxrwxrwx   0        0        0        0 2023-07-22 22:10:25.838349 Signal8-4.95/
--rw-rw-rw-   0        0        0     1089 2023-04-10 03:39:38.000000 Signal8-4.95/LICENSE
--rw-rw-rw-   0        0        0     5299 2023-07-22 22:10:25.837349 Signal8-4.95/PKG-INFO
--rw-rw-rw-   0        0        0     4800 2023-07-22 22:09:51.000000 Signal8-4.95/README.md
-drwxrwxrwx   0        0        0        0 2023-07-22 22:10:25.726347 Signal8-4.95/Signal8/
--rw-rw-rw-   0        0        0    11149 2023-07-22 22:05:52.000000 Signal8-4.95/Signal8/Signal8.py
--rw-rw-rw-   0        0        0       24 2023-06-19 21:16:46.000000 Signal8-4.95/Signal8/__init__.py
--rw-rw-rw-   0        0        0      241 2023-07-22 21:54:42.000000 Signal8-4.95/Signal8/main.py
-drwxrwxrwx   0        0        0        0 2023-07-22 22:10:25.831347 Signal8-4.95/Signal8/utils/
--rw-rw-rw-   0        0        0        0 2023-05-19 05:01:34.000000 Signal8-4.95/Signal8/utils/__init__.py
--rw-rw-rw-   0        0        0     5285 2023-07-14 01:01:24.000000 Signal8-4.95/Signal8/utils/core.py
--rw-rw-rw-   0        0        0     2328 2023-07-20 21:04:43.000000 Signal8-4.95/Signal8/utils/problems.py
--rw-rw-rw-   0        0        0      292 2023-02-28 21:08:59.000000 Signal8-4.95/Signal8/utils/scenario.py
--rw-rw-rw-   0        0        0    11960 2023-07-13 18:01:37.000000 Signal8-4.95/Signal8/utils/simple_env.py
--rw-rw-rw-   0        0        0     1659 2023-06-08 18:48:20.000000 Signal8-4.95/Signal8/utils/test_dynamic_obs.py
-drwxrwxrwx   0        0        0        0 2023-07-22 22:10:25.774347 Signal8-4.95/Signal8.egg-info/
--rw-rw-rw-   0        0        0     5299 2023-07-22 22:10:25.000000 Signal8-4.95/Signal8.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      510 2023-07-22 22:10:25.000000 Signal8-4.95/Signal8.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-22 22:10:25.000000 Signal8-4.95/Signal8.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        8 2023-07-22 22:10:25.000000 Signal8-4.95/Signal8.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-22 22:10:25.841351 Signal8-4.95/setup.cfg
--rw-rw-rw-   0        0        0      646 2023-07-22 22:09:16.000000 Signal8-4.95/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-22 22:13:31.845919 Signal8-4.96/
+-rw-rw-rw-   0        0        0     1089 2023-04-10 03:39:38.000000 Signal8-4.96/LICENSE
+-rw-rw-rw-   0        0        0     5299 2023-07-22 22:13:31.842916 Signal8-4.96/PKG-INFO
+-rw-rw-rw-   0        0        0     4800 2023-07-22 22:09:51.000000 Signal8-4.96/README.md
+drwxrwxrwx   0        0        0        0 2023-07-22 22:13:31.761916 Signal8-4.96/Signal8/
+-rw-rw-rw-   0        0        0    11153 2023-07-22 22:12:44.000000 Signal8-4.96/Signal8/Signal8.py
+-rw-rw-rw-   0        0        0       24 2023-06-19 21:16:46.000000 Signal8-4.96/Signal8/__init__.py
+-rw-rw-rw-   0        0        0      241 2023-07-22 22:12:52.000000 Signal8-4.96/Signal8/main.py
+drwxrwxrwx   0        0        0        0 2023-07-22 22:13:31.834920 Signal8-4.96/Signal8/utils/
+-rw-rw-rw-   0        0        0        0 2023-05-19 05:01:34.000000 Signal8-4.96/Signal8/utils/__init__.py
+-rw-rw-rw-   0        0        0     5285 2023-07-14 01:01:24.000000 Signal8-4.96/Signal8/utils/core.py
+-rw-rw-rw-   0        0        0     2328 2023-07-20 21:04:43.000000 Signal8-4.96/Signal8/utils/problems.py
+-rw-rw-rw-   0        0        0      292 2023-02-28 21:08:59.000000 Signal8-4.96/Signal8/utils/scenario.py
+-rw-rw-rw-   0        0        0    11960 2023-07-13 18:01:37.000000 Signal8-4.96/Signal8/utils/simple_env.py
+-rw-rw-rw-   0        0        0     1659 2023-06-08 18:48:20.000000 Signal8-4.96/Signal8/utils/test_dynamic_obs.py
+drwxrwxrwx   0        0        0        0 2023-07-22 22:13:31.798916 Signal8-4.96/Signal8.egg-info/
+-rw-rw-rw-   0        0        0     5299 2023-07-22 22:13:31.000000 Signal8-4.96/Signal8.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      510 2023-07-22 22:13:31.000000 Signal8-4.96/Signal8.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-22 22:13:31.000000 Signal8-4.96/Signal8.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        8 2023-07-22 22:13:31.000000 Signal8-4.96/Signal8.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-22 22:13:31.846918 Signal8-4.96/setup.cfg
+-rw-rw-rw-   0        0        0      646 2023-07-22 22:13:07.000000 Signal8-4.96/setup.py
```

### Comparing `Signal8-4.95/LICENSE` & `Signal8-4.96/LICENSE`

 * *Files identical despite different names*

### Comparing `Signal8-4.95/PKG-INFO` & `Signal8-4.96/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: Signal8
-Version: 4.95
+Version: 4.96
 Summary: A multi-agent environment inspired by the Lewis Signaling Game, featuring eight unique problem configurations with both static and dynamic obstacles.
 Home-page: https://github.com/ethanmclark1/signal8
 Author: Ethan Clark
 Author-email: eclark715@gmail.com.com
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python
 Description-Content-Type: text/markdown
```

### Comparing `Signal8-4.95/README.md` & `Signal8-4.96/README.md`

 * *Files identical despite different names*

### Comparing `Signal8-4.95/Signal8/Signal8.py` & `Signal8-4.96/Signal8/Signal8.py`

 * *Files 0% similar despite different names*

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
```

### Comparing `Signal8-4.95/Signal8/utils/core.py` & `Signal8-4.96/Signal8/utils/core.py`

 * *Files identical despite different names*

### Comparing `Signal8-4.95/Signal8/utils/problems.py` & `Signal8-4.96/Signal8/utils/problems.py`

 * *Files identical despite different names*

### Comparing `Signal8-4.95/Signal8/utils/simple_env.py` & `Signal8-4.96/Signal8/utils/simple_env.py`

 * *Files identical despite different names*

### Comparing `Signal8-4.95/Signal8/utils/test_dynamic_obs.py` & `Signal8-4.96/Signal8/utils/test_dynamic_obs.py`

 * *Files identical despite different names*

### Comparing `Signal8-4.95/Signal8.egg-info/PKG-INFO` & `Signal8-4.96/Signal8.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: Signal8
-Version: 4.95
+Version: 4.96
 Summary: A multi-agent environment inspired by the Lewis Signaling Game, featuring eight unique problem configurations with both static and dynamic obstacles.
 Home-page: https://github.com/ethanmclark1/signal8
 Author: Ethan Clark
 Author-email: eclark715@gmail.com.com
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python
 Description-Content-Type: text/markdown
```

### Comparing `Signal8-4.95/setup.py` & `Signal8-4.96/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name="Signal8",
-    version="4.95",
+    version="4.96",
     packages=find_packages(),
     author="Ethan Clark",
     author_email="eclark715@gmail.com.com",
     description="A multi-agent environment inspired by the Lewis Signaling Game, featuring eight unique problem configurations with both static and dynamic obstacles.",
     long_description=open('README.md').read(),
     long_description_content_type='text/markdown',
     url="https://github.com/ethanmclark1/signal8",
```

