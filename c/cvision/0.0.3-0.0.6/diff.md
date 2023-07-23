# Comparing `tmp/cvision-0.0.3.tar.gz` & `tmp/cvision-0.0.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "cvision-0.0.3.tar", last modified: Sat Jul 22 17:21:10 2023, max compression
+gzip compressed data, was "cvision-0.0.6.tar", last modified: Sun Jul 23 12:58:49 2023, max compression
```

## Comparing `cvision-0.0.3.tar` & `cvision-0.0.6.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxrwxrwx   0        0        0        0 2023-07-22 17:21:10.439247 cvision-0.0.3/
--rw-rw-rw-   0        0        0     1091 2023-07-20 20:17:27.000000 cvision-0.0.3/LICENSE.txt
--rw-rw-rw-   0        0        0      648 2023-07-22 17:21:10.423625 cvision-0.0.3/PKG-INFO
--rw-rw-rw-   0        0        0      174 2023-07-20 20:16:36.000000 cvision-0.0.3/README.md
-drwxrwxrwx   0        0        0        0 2023-07-22 17:21:10.408004 cvision-0.0.3/cvision/
--rw-rw-rw-   0        0        0       43 2023-07-22 17:20:28.000000 cvision-0.0.3/cvision/__init__.py
--rw-rw-rw-   0        0        0     5320 2023-07-22 17:20:02.000000 cvision-0.0.3/cvision/cvision.py
-drwxrwxrwx   0        0        0        0 2023-07-22 17:21:10.423625 cvision-0.0.3/cvision.egg-info/
--rw-rw-rw-   0        0        0      648 2023-07-22 17:21:10.000000 cvision-0.0.3/cvision.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      193 2023-07-22 17:21:10.000000 cvision-0.0.3/cvision.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-22 17:21:10.000000 cvision-0.0.3/cvision.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        8 2023-07-22 17:21:10.000000 cvision-0.0.3/cvision.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-22 17:21:10.439247 cvision-0.0.3/setup.cfg
--rw-rw-rw-   0        0        0      953 2023-07-22 17:21:00.000000 cvision-0.0.3/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 12:58:49.164506 cvision-0.0.6/
+-rw-rw-rw-   0        0        0     1091 2023-07-20 20:17:27.000000 cvision-0.0.6/LICENSE.txt
+-rw-rw-rw-   0        0        0      732 2023-07-23 12:58:49.164506 cvision-0.0.6/PKG-INFO
+-rw-rw-rw-   0        0        0      174 2023-07-20 20:16:36.000000 cvision-0.0.6/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 12:58:49.142367 cvision-0.0.6/cvision/
+-rw-rw-rw-   0        0        0       86 2023-07-23 12:47:36.000000 cvision-0.0.6/cvision/__init__.py
+-rw-rw-rw-   0        0        0    21294 2023-07-23 12:55:51.000000 cvision-0.0.6/cvision/cvision.py
+drwxrwxrwx   0        0        0        0 2023-07-23 12:58:49.164506 cvision-0.0.6/cvision.egg-info/
+-rw-rw-rw-   0        0        0      732 2023-07-23 12:58:49.000000 cvision-0.0.6/cvision.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      193 2023-07-23 12:58:49.000000 cvision-0.0.6/cvision.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 12:58:49.000000 cvision-0.0.6/cvision.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        8 2023-07-23 12:58:49.000000 cvision-0.0.6/cvision.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 12:58:49.164506 cvision-0.0.6/setup.cfg
+-rw-rw-rw-   0        0        0     1037 2023-07-23 12:57:28.000000 cvision-0.0.6/setup.py
```

### Comparing `cvision-0.0.3/LICENSE.txt` & `cvision-0.0.6/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `cvision-0.0.3/PKG-INFO` & `cvision-0.0.6/PKG-INFO`

 * *Files 20% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cvision
-Version: 0.0.3
+Version: 0.0.6
 Summary: Computer vision package
 Home-page: UNKNOWN
 Author: Dr Anna Sung and Prof Kelvin Leong
 Author-email: <k.leong@chester.ac.uk>
 License: UNKNOWN
 Keywords: python,first package
 Platform: UNKNOWN
@@ -12,9 +12,9 @@
 Classifier: Intended Audience :: Education
 Classifier: Programming Language :: Python :: 2
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: MacOS :: MacOS X
 Classifier: Operating System :: Microsoft :: Windows
 License-File: LICENSE.txt
 
-This Python package aims to evaluate image with computer vision.
+This Python package aims to evaluate image in different ways, including emotion (love, joy, surprise, anger, sadness and fear) with computer vision.
```

### Comparing `cvision-0.0.3/cvision.egg-info/PKG-INFO` & `cvision-0.0.6/cvision.egg-info/PKG-INFO`

 * *Files 20% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cvision
-Version: 0.0.3
+Version: 0.0.6
 Summary: Computer vision package
 Home-page: UNKNOWN
 Author: Dr Anna Sung and Prof Kelvin Leong
 Author-email: <k.leong@chester.ac.uk>
 License: UNKNOWN
 Keywords: python,first package
 Platform: UNKNOWN
@@ -12,9 +12,9 @@
 Classifier: Intended Audience :: Education
 Classifier: Programming Language :: Python :: 2
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: MacOS :: MacOS X
 Classifier: Operating System :: Microsoft :: Windows
 License-File: LICENSE.txt
 
-This Python package aims to evaluate image with computer vision.
+This Python package aims to evaluate image in different ways, including emotion (love, joy, surprise, anger, sadness and fear) with computer vision.
```

### Comparing `cvision-0.0.3/setup.py` & `cvision-0.0.6/setup.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
-VERSION = '0.0.03' 
+VERSION = '0.0.06' 
 DESCRIPTION = 'Computer vision package'
-LONG_DESCRIPTION = 'This Python package aims to evaluate image with computer vision.'
+LONG_DESCRIPTION = 'This Python package aims to evaluate image in different ways, including emotion (love, joy, surprise, anger, sadness and fear) with computer vision.'
 
 
 setup(
         name="cvision", 
         version=VERSION,
         author="Dr Anna Sung and Prof Kelvin Leong",
         author_email="<k.leong@chester.ac.uk>",
```

