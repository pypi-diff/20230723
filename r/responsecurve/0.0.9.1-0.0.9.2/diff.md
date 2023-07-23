# Comparing `tmp/responsecurve-0.0.9.1.tar.gz` & `tmp/responsecurve-0.0.9.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "responsecurve-0.0.9.1.tar", last modified: Sat Jul 22 23:59:10 2023, max compression
+gzip compressed data, was "responsecurve-0.0.9.2.tar", last modified: Sun Jul 23 00:06:50 2023, max compression
```

## Comparing `responsecurve-0.0.9.1.tar` & `responsecurve-0.0.9.2.tar`

### file list

```diff
@@ -1,12 +1,12 @@
-drwxr-xr-x   0 ishanramrakhiani   (501) staff       (20)        0 2023-07-22 23:59:10.096241 responsecurve-0.0.9.1/
--rw-r--r--   0 ishanramrakhiani   (501) staff       (20)     1163 2023-07-20 18:34:56.000000 responsecurve-0.0.9.1/LICENSE
--rw-r--r--   0 ishanramrakhiani   (501) staff       (20)    13789 2023-07-22 23:59:10.095635 responsecurve-0.0.9.1/PKG-INFO
--rw-r--r--   0 ishanramrakhiani   (501) staff       (20)    13475 2023-07-20 22:49:19.000000 responsecurve-0.0.9.1/README.md
-drwxr-xr-x   0 ishanramrakhiani   (501) staff       (20)        0 2023-07-22 23:59:10.094392 responsecurve-0.0.9.1/responsecurve.egg-info/
--rw-r--r--   0 ishanramrakhiani   (501) staff       (20)    13789 2023-07-22 23:59:09.000000 responsecurve-0.0.9.1/responsecurve.egg-info/PKG-INFO
--rw-r--r--   0 ishanramrakhiani   (501) staff       (20)      210 2023-07-22 23:59:09.000000 responsecurve-0.0.9.1/responsecurve.egg-info/SOURCES.txt
--rw-r--r--   0 ishanramrakhiani   (501) staff       (20)        1 2023-07-22 23:59:09.000000 responsecurve-0.0.9.1/responsecurve.egg-info/dependency_links.txt
--rw-r--r--   0 ishanramrakhiani   (501) staff       (20)       43 2023-07-22 23:59:09.000000 responsecurve-0.0.9.1/responsecurve.egg-info/requires.txt
--rw-r--r--   0 ishanramrakhiani   (501) staff       (20)        1 2023-07-22 23:59:09.000000 responsecurve-0.0.9.1/responsecurve.egg-info/top_level.txt
--rw-r--r--   0 ishanramrakhiani   (501) staff       (20)       38 2023-07-22 23:59:10.096440 responsecurve-0.0.9.1/setup.cfg
--rw-r--r--   0 ishanramrakhiani   (501) staff       (20)      628 2023-07-22 23:59:06.000000 responsecurve-0.0.9.1/setup.py
+drwxr-xr-x   0 ishanramrakhiani   (501) staff       (20)        0 2023-07-23 00:06:50.111591 responsecurve-0.0.9.2/
+-rw-r--r--   0 ishanramrakhiani   (501) staff       (20)     1163 2023-07-20 18:34:56.000000 responsecurve-0.0.9.2/LICENSE
+-rw-r--r--   0 ishanramrakhiani   (501) staff       (20)    13862 2023-07-23 00:06:50.110714 responsecurve-0.0.9.2/PKG-INFO
+-rw-r--r--   0 ishanramrakhiani   (501) staff       (20)    13548 2023-07-23 00:06:35.000000 responsecurve-0.0.9.2/README.md
+drwxr-xr-x   0 ishanramrakhiani   (501) staff       (20)        0 2023-07-23 00:06:50.108619 responsecurve-0.0.9.2/responsecurve.egg-info/
+-rw-r--r--   0 ishanramrakhiani   (501) staff       (20)    13862 2023-07-23 00:06:49.000000 responsecurve-0.0.9.2/responsecurve.egg-info/PKG-INFO
+-rw-r--r--   0 ishanramrakhiani   (501) staff       (20)      210 2023-07-23 00:06:49.000000 responsecurve-0.0.9.2/responsecurve.egg-info/SOURCES.txt
+-rw-r--r--   0 ishanramrakhiani   (501) staff       (20)        1 2023-07-23 00:06:49.000000 responsecurve-0.0.9.2/responsecurve.egg-info/dependency_links.txt
+-rw-r--r--   0 ishanramrakhiani   (501) staff       (20)       43 2023-07-23 00:06:49.000000 responsecurve-0.0.9.2/responsecurve.egg-info/requires.txt
+-rw-r--r--   0 ishanramrakhiani   (501) staff       (20)        1 2023-07-23 00:06:49.000000 responsecurve-0.0.9.2/responsecurve.egg-info/top_level.txt
+-rw-r--r--   0 ishanramrakhiani   (501) staff       (20)       38 2023-07-23 00:06:50.112111 responsecurve-0.0.9.2/setup.cfg
+-rw-r--r--   0 ishanramrakhiani   (501) staff       (20)      628 2023-07-23 00:06:43.000000 responsecurve-0.0.9.2/setup.py
```

### Comparing `responsecurve-0.0.9.1/LICENSE` & `responsecurve-0.0.9.2/LICENSE`

 * *Files identical despite different names*

### Comparing `responsecurve-0.0.9.1/PKG-INFO` & `responsecurve-0.0.9.2/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: responsecurve
-Version: 0.0.9.1
+Version: 0.0.9.2
 Summary: A library for detecting response curves in time series data.
 Home-page: https://github.com/himanalot/ResponseCurve
 Author: Ishan Ramrakhiani
 Author-email: ishanramrakhiani@gmail.com
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
@@ -57,15 +57,15 @@
 **Inputs:**
 
 - `window_size`: An integer indicating the size of the window to use for local analysis around the detected start point. Default is 5.
 - `plot`: A boolean indicating whether to plot the response with the start and end points. Default is False.
 
 **Output:** A tuple with the start and end points as pandas DataFrame rows.
 
-This function detects the start and end points of the response in the data using the second derivative and differences. It optionally plots the response with the start and end points.
+This function detects the start and end points of the response in the data using the second derivative and differences. It optionally plots the response with the start and end points. **It is meant to be used on a dataset which contains 1 response curve.**
 
 ### response_duration(start=None, end=None)
 **Function:** `response_duration(start=None, end=None)`
 
 **Inputs:**
 
 - `start`: A pandas DataFrame row representing the start point of the response. If None, a ValueError is raised.
```

### Comparing `responsecurve-0.0.9.1/README.md` & `responsecurve-0.0.9.2/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -47,15 +47,15 @@
 **Inputs:**
 
 - `window_size`: An integer indicating the size of the window to use for local analysis around the detected start point. Default is 5.
 - `plot`: A boolean indicating whether to plot the response with the start and end points. Default is False.
 
 **Output:** A tuple with the start and end points as pandas DataFrame rows.
 
-This function detects the start and end points of the response in the data using the second derivative and differences. It optionally plots the response with the start and end points.
+This function detects the start and end points of the response in the data using the second derivative and differences. It optionally plots the response with the start and end points. **It is meant to be used on a dataset which contains 1 response curve.**
 
 ### response_duration(start=None, end=None)
 **Function:** `response_duration(start=None, end=None)`
 
 **Inputs:**
 
 - `start`: A pandas DataFrame row representing the start point of the response. If None, a ValueError is raised.
```

### Comparing `responsecurve-0.0.9.1/responsecurve.egg-info/PKG-INFO` & `responsecurve-0.0.9.2/responsecurve.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: responsecurve
-Version: 0.0.9.1
+Version: 0.0.9.2
 Summary: A library for detecting response curves in time series data.
 Home-page: https://github.com/himanalot/ResponseCurve
 Author: Ishan Ramrakhiani
 Author-email: ishanramrakhiani@gmail.com
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
@@ -57,15 +57,15 @@
 **Inputs:**
 
 - `window_size`: An integer indicating the size of the window to use for local analysis around the detected start point. Default is 5.
 - `plot`: A boolean indicating whether to plot the response with the start and end points. Default is False.
 
 **Output:** A tuple with the start and end points as pandas DataFrame rows.
 
-This function detects the start and end points of the response in the data using the second derivative and differences. It optionally plots the response with the start and end points.
+This function detects the start and end points of the response in the data using the second derivative and differences. It optionally plots the response with the start and end points. **It is meant to be used on a dataset which contains 1 response curve.**
 
 ### response_duration(start=None, end=None)
 **Function:** `response_duration(start=None, end=None)`
 
 **Inputs:**
 
 - `start`: A pandas DataFrame row representing the start point of the response. If None, a ValueError is raised.
```

### Comparing `responsecurve-0.0.9.1/setup.py` & `responsecurve-0.0.9.2/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from setuptools import setup, find_packages
 
 with open('README.md', 'r') as f:
     long_description = f.read()
 
 setup(
     name='responsecurve',
-    version='0.0.9.1',
+    version='0.0.9.2',
     packages=find_packages(),
     install_requires=[
         'pandas',
         'numpy',
         'scipy',
         'matplotlib',
         'scikit-learn'
```

