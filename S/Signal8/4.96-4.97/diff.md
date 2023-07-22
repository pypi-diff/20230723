# Comparing `tmp/Signal8-4.96.tar.gz` & `tmp/Signal8-4.97.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "Signal8-4.96.tar", last modified: Sat Jul 22 22:13:31 2023, max compression
+gzip compressed data, was "Signal8-4.97.tar", last modified: Sat Jul 22 22:19:24 2023, max compression
```

## Comparing `Signal8-4.96.tar` & `Signal8-4.97.tar`

### file list

```diff
@@ -1,22 +1,22 @@
-drwxrwxrwx   0        0        0        0 2023-07-22 22:13:31.845919 Signal8-4.96/
--rw-rw-rw-   0        0        0     1089 2023-04-10 03:39:38.000000 Signal8-4.96/LICENSE
--rw-rw-rw-   0        0        0     5299 2023-07-22 22:13:31.842916 Signal8-4.96/PKG-INFO
--rw-rw-rw-   0        0        0     4800 2023-07-22 22:09:51.000000 Signal8-4.96/README.md
-drwxrwxrwx   0        0        0        0 2023-07-22 22:13:31.761916 Signal8-4.96/Signal8/
--rw-rw-rw-   0        0        0    11153 2023-07-22 22:12:44.000000 Signal8-4.96/Signal8/Signal8.py
--rw-rw-rw-   0        0        0       24 2023-06-19 21:16:46.000000 Signal8-4.96/Signal8/__init__.py
--rw-rw-rw-   0        0        0      241 2023-07-22 22:12:52.000000 Signal8-4.96/Signal8/main.py
-drwxrwxrwx   0        0        0        0 2023-07-22 22:13:31.834920 Signal8-4.96/Signal8/utils/
--rw-rw-rw-   0        0        0        0 2023-05-19 05:01:34.000000 Signal8-4.96/Signal8/utils/__init__.py
--rw-rw-rw-   0        0        0     5285 2023-07-14 01:01:24.000000 Signal8-4.96/Signal8/utils/core.py
--rw-rw-rw-   0        0        0     2328 2023-07-20 21:04:43.000000 Signal8-4.96/Signal8/utils/problems.py
--rw-rw-rw-   0        0        0      292 2023-02-28 21:08:59.000000 Signal8-4.96/Signal8/utils/scenario.py
--rw-rw-rw-   0        0        0    11960 2023-07-13 18:01:37.000000 Signal8-4.96/Signal8/utils/simple_env.py
--rw-rw-rw-   0        0        0     1659 2023-06-08 18:48:20.000000 Signal8-4.96/Signal8/utils/test_dynamic_obs.py
-drwxrwxrwx   0        0        0        0 2023-07-22 22:13:31.798916 Signal8-4.96/Signal8.egg-info/
--rw-rw-rw-   0        0        0     5299 2023-07-22 22:13:31.000000 Signal8-4.96/Signal8.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      510 2023-07-22 22:13:31.000000 Signal8-4.96/Signal8.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-22 22:13:31.000000 Signal8-4.96/Signal8.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        8 2023-07-22 22:13:31.000000 Signal8-4.96/Signal8.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-22 22:13:31.846918 Signal8-4.96/setup.cfg
--rw-rw-rw-   0        0        0      646 2023-07-22 22:13:07.000000 Signal8-4.96/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-22 22:19:24.557052 Signal8-4.97/
+-rw-rw-rw-   0        0        0     1089 2023-04-10 03:39:38.000000 Signal8-4.97/LICENSE
+-rw-rw-rw-   0        0        0     5299 2023-07-22 22:19:24.545050 Signal8-4.97/PKG-INFO
+-rw-rw-rw-   0        0        0     4800 2023-07-22 22:09:51.000000 Signal8-4.97/README.md
+drwxrwxrwx   0        0        0        0 2023-07-22 22:19:24.440051 Signal8-4.97/Signal8/
+-rw-rw-rw-   0        0        0    11162 2023-07-22 22:18:44.000000 Signal8-4.97/Signal8/Signal8.py
+-rw-rw-rw-   0        0        0       24 2023-06-19 21:16:46.000000 Signal8-4.97/Signal8/__init__.py
+-rw-rw-rw-   0        0        0      241 2023-07-22 22:16:47.000000 Signal8-4.97/Signal8/main.py
+drwxrwxrwx   0        0        0        0 2023-07-22 22:19:24.540049 Signal8-4.97/Signal8/utils/
+-rw-rw-rw-   0        0        0        0 2023-05-19 05:01:34.000000 Signal8-4.97/Signal8/utils/__init__.py
+-rw-rw-rw-   0        0        0     5285 2023-07-14 01:01:24.000000 Signal8-4.97/Signal8/utils/core.py
+-rw-rw-rw-   0        0        0     2328 2023-07-20 21:04:43.000000 Signal8-4.97/Signal8/utils/problems.py
+-rw-rw-rw-   0        0        0      292 2023-02-28 21:08:59.000000 Signal8-4.97/Signal8/utils/scenario.py
+-rw-rw-rw-   0        0        0    11960 2023-07-13 18:01:37.000000 Signal8-4.97/Signal8/utils/simple_env.py
+-rw-rw-rw-   0        0        0     1659 2023-06-08 18:48:20.000000 Signal8-4.97/Signal8/utils/test_dynamic_obs.py
+drwxrwxrwx   0        0        0        0 2023-07-22 22:19:24.510050 Signal8-4.97/Signal8.egg-info/
+-rw-rw-rw-   0        0        0     5299 2023-07-22 22:19:24.000000 Signal8-4.97/Signal8.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      510 2023-07-22 22:19:24.000000 Signal8-4.97/Signal8.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-22 22:19:24.000000 Signal8-4.97/Signal8.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        8 2023-07-22 22:19:24.000000 Signal8-4.97/Signal8.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-22 22:19:24.557052 Signal8-4.97/setup.cfg
+-rw-rw-rw-   0        0        0      646 2023-07-22 22:18:50.000000 Signal8-4.97/setup.py
```

### Comparing `Signal8-4.96/LICENSE` & `Signal8-4.97/LICENSE`

 * *Files identical despite different names*

### Comparing `Signal8-4.96/PKG-INFO` & `Signal8-4.97/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: Signal8
-Version: 4.96
+Version: 4.97
 Summary: A multi-agent environment inspired by the Lewis Signaling Game, featuring eight unique problem configurations with both static and dynamic obstacles.
 Home-page: https://github.com/ethanmclark1/signal8
 Author: Ethan Clark
 Author-email: eclark715@gmail.com.com
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python
 Description-Content-Type: text/markdown
```

### Comparing `Signal8-4.96/README.md` & `Signal8-4.97/README.md`

 * *Files identical despite different names*

### Comparing `Signal8-4.96/Signal8/Signal8.py` & `Signal8-4.97/Signal8/Signal8.py`

 * *Files 1% similar despite different names*

```diff
@@ -87,15 +87,15 @@
     # Check if point is outside of triangular obstacle regions
     def _outside_triangle(self, point, paths, epsilon):
         enlarged_paths = []
         for path in paths:
             centroid = np.mean(path.vertices, axis=0)
             enlarged_vertices = path.vertices + epsilon * (path.vertices - centroid)
             enlarged_paths.append(mpath.Path(enlarged_vertices))
-        return not any(path.contains_points(point) for path in enlarged_paths)
+        return not any(path.contains_points(point[None, :]) for path in enlarged_paths)
     
     # Check if point is outside of circular obstacle regions
     def _outside_circles(self, point, centers_radii, epsilon):
         return not any(np.linalg.norm(point - center) <= radius + epsilon for center, radius in centers_radii)
     
     # Check if point is outside of rectangular obstacle regions
     def _outside_rectangle(self, point, x_constraints, y_constraints, epsilon):
```

### Comparing `Signal8-4.96/Signal8/utils/core.py` & `Signal8-4.97/Signal8/utils/core.py`

 * *Files identical despite different names*

### Comparing `Signal8-4.96/Signal8/utils/problems.py` & `Signal8-4.97/Signal8/utils/problems.py`

 * *Files identical despite different names*

### Comparing `Signal8-4.96/Signal8/utils/simple_env.py` & `Signal8-4.97/Signal8/utils/simple_env.py`

 * *Files identical despite different names*

### Comparing `Signal8-4.96/Signal8/utils/test_dynamic_obs.py` & `Signal8-4.97/Signal8/utils/test_dynamic_obs.py`

 * *Files identical despite different names*

### Comparing `Signal8-4.96/Signal8.egg-info/PKG-INFO` & `Signal8-4.97/Signal8.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: Signal8
-Version: 4.96
+Version: 4.97
 Summary: A multi-agent environment inspired by the Lewis Signaling Game, featuring eight unique problem configurations with both static and dynamic obstacles.
 Home-page: https://github.com/ethanmclark1/signal8
 Author: Ethan Clark
 Author-email: eclark715@gmail.com.com
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python
 Description-Content-Type: text/markdown
```

### Comparing `Signal8-4.96/setup.py` & `Signal8-4.97/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name="Signal8",
-    version="4.96",
+    version="4.97",
     packages=find_packages(),
     author="Ethan Clark",
     author_email="eclark715@gmail.com.com",
     description="A multi-agent environment inspired by the Lewis Signaling Game, featuring eight unique problem configurations with both static and dynamic obstacles.",
     long_description=open('README.md').read(),
     long_description_content_type='text/markdown',
     url="https://github.com/ethanmclark1/signal8",
```

