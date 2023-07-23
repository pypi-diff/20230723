# Comparing `tmp/CloudEdgeAssetsOptimizer-0.1.1.tar.gz` & `tmp/CloudEdgeAssetsOptimizer-0.1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "CloudEdgeAssetsOptimizer-0.1.1.tar", last modified: Sun Jul 23 12:25:03 2023, max compression
+gzip compressed data, was "CloudEdgeAssetsOptimizer-0.1.2.tar", last modified: Sun Jul 23 12:40:48 2023, max compression
```

## Comparing `CloudEdgeAssetsOptimizer-0.1.1.tar` & `CloudEdgeAssetsOptimizer-0.1.2.tar`

### file list

```diff
@@ -1,12 +1,20 @@
-drwxr-xr-x   0 paulius    (501) staff       (20)        0 2023-07-23 12:25:03.000000 CloudEdgeAssetsOptimizer-0.1.1/
-drwxr-xr-x   0 paulius    (501) staff       (20)        0 2023-07-23 12:25:03.000000 CloudEdgeAssetsOptimizer-0.1.1/CloudEdgeAssetsOptimizer.egg-info/
--rw-r--r--   0 paulius    (501) staff       (20)     1691 2023-07-23 12:25:03.000000 CloudEdgeAssetsOptimizer-0.1.1/CloudEdgeAssetsOptimizer.egg-info/PKG-INFO
--rw-r--r--   0 paulius    (501) staff       (20)      265 2023-07-23 12:25:03.000000 CloudEdgeAssetsOptimizer-0.1.1/CloudEdgeAssetsOptimizer.egg-info/SOURCES.txt
--rw-r--r--   0 paulius    (501) staff       (20)        1 2023-07-23 12:25:03.000000 CloudEdgeAssetsOptimizer-0.1.1/CloudEdgeAssetsOptimizer.egg-info/dependency_links.txt
--rw-r--r--   0 paulius    (501) staff       (20)       31 2023-07-23 12:25:03.000000 CloudEdgeAssetsOptimizer-0.1.1/CloudEdgeAssetsOptimizer.egg-info/requires.txt
--rw-r--r--   0 paulius    (501) staff       (20)       25 2023-07-23 12:25:03.000000 CloudEdgeAssetsOptimizer-0.1.1/CloudEdgeAssetsOptimizer.egg-info/top_level.txt
--rw-r--r--   0 paulius    (501) staff       (20)     1067 2023-07-23 11:50:18.000000 CloudEdgeAssetsOptimizer-0.1.1/LICENSE
--rw-r--r--   0 paulius    (501) staff       (20)     1691 2023-07-23 12:25:03.000000 CloudEdgeAssetsOptimizer-0.1.1/PKG-INFO
--rw-r--r--   0 paulius    (501) staff       (20)     1101 2023-07-23 12:24:27.000000 CloudEdgeAssetsOptimizer-0.1.1/README.md
--rw-r--r--   0 paulius    (501) staff       (20)       38 2023-07-23 12:25:03.000000 CloudEdgeAssetsOptimizer-0.1.1/setup.cfg
--rw-r--r--   0 paulius    (501) staff       (20)     1975 2023-07-23 12:24:53.000000 CloudEdgeAssetsOptimizer-0.1.1/setup.py
+drwxr-xr-x   0 paulius    (501) staff       (20)        0 2023-07-23 12:40:47.000000 CloudEdgeAssetsOptimizer-0.1.2/
+drwxr-xr-x   0 paulius    (501) staff       (20)        0 2023-07-23 12:40:47.000000 CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer/
+-rw-r--r--   0 paulius    (501) staff       (20)     1435 2023-07-23 12:05:19.000000 CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer/CloudEdgeAssetOptimizer.py
+-rw-r--r--   0 paulius    (501) staff       (20)       38 2023-07-23 12:34:07.000000 CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer/__init__.py
+-rw-r--r--   0 paulius    (501) staff       (20)     7147 2023-07-23 12:05:19.000000 CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer/calculation.py
+-rw-r--r--   0 paulius    (501) staff       (20)     3153 2023-07-23 12:05:19.000000 CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer/graph.py
+-rw-r--r--   0 paulius    (501) staff       (20)    15033 2023-07-23 12:05:19.000000 CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer/gui_frontend.py
+-rw-r--r--   0 paulius    (501) staff       (20)     3375 2023-07-23 12:05:19.000000 CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer/optimizer.py
+-rw-r--r--   0 paulius    (501) staff       (20)    13264 2023-07-23 12:05:19.000000 CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer/qsystems.py
+drwxr-xr-x   0 paulius    (501) staff       (20)        0 2023-07-23 12:40:47.000000 CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer.egg-info/
+-rw-r--r--   0 paulius    (501) staff       (20)     1691 2023-07-23 12:40:48.000000 CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer.egg-info/PKG-INFO
+-rw-r--r--   0 paulius    (501) staff       (20)      544 2023-07-23 12:40:48.000000 CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer.egg-info/SOURCES.txt
+-rw-r--r--   0 paulius    (501) staff       (20)        1 2023-07-23 12:40:48.000000 CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer.egg-info/dependency_links.txt
+-rw-r--r--   0 paulius    (501) staff       (20)       31 2023-07-23 12:40:48.000000 CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer.egg-info/requires.txt
+-rw-r--r--   0 paulius    (501) staff       (20)       25 2023-07-23 12:40:48.000000 CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer.egg-info/top_level.txt
+-rw-r--r--   0 paulius    (501) staff       (20)     1067 2023-07-23 11:50:18.000000 CloudEdgeAssetsOptimizer-0.1.2/LICENSE
+-rw-r--r--   0 paulius    (501) staff       (20)     1691 2023-07-23 12:40:48.000000 CloudEdgeAssetsOptimizer-0.1.2/PKG-INFO
+-rw-r--r--   0 paulius    (501) staff       (20)     1101 2023-07-23 12:24:27.000000 CloudEdgeAssetsOptimizer-0.1.2/README.md
+-rw-r--r--   0 paulius    (501) staff       (20)       38 2023-07-23 12:40:48.000000 CloudEdgeAssetsOptimizer-0.1.2/setup.cfg
+-rw-r--r--   0 paulius    (501) staff       (20)     1975 2023-07-23 12:34:37.000000 CloudEdgeAssetsOptimizer-0.1.2/setup.py
```

### Comparing `CloudEdgeAssetsOptimizer-0.1.1/CloudEdgeAssetsOptimizer.egg-info/PKG-INFO` & `CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer.egg-info/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: CloudEdgeAssetsOptimizer
-Version: 0.1.1
+Version: 0.1.2
 Summary: # CloudEdgeAssetsOptimizer   
 Home-page: https://github.com/pauterv/CloudEdgeAssetsOptimizer
 Author: Paulius Tervydis
 Author-email: Paulius.Tervydis@ktu.lt
 Classifier: Development Status :: 3 - Alpha
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
```

### Comparing `CloudEdgeAssetsOptimizer-0.1.1/LICENSE` & `CloudEdgeAssetsOptimizer-0.1.2/LICENSE`

 * *Files identical despite different names*

### Comparing `CloudEdgeAssetsOptimizer-0.1.1/PKG-INFO` & `CloudEdgeAssetsOptimizer-0.1.2/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: CloudEdgeAssetsOptimizer
-Version: 0.1.1
+Version: 0.1.2
 Summary: # CloudEdgeAssetsOptimizer   
 Home-page: https://github.com/pauterv/CloudEdgeAssetsOptimizer
 Author: Paulius Tervydis
 Author-email: Paulius.Tervydis@ktu.lt
 Classifier: Development Status :: 3 - Alpha
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
```

### Comparing `CloudEdgeAssetsOptimizer-0.1.1/README.md` & `CloudEdgeAssetsOptimizer-0.1.2/README.md`

 * *Files identical despite different names*

### Comparing `CloudEdgeAssetsOptimizer-0.1.1/setup.py` & `CloudEdgeAssetsOptimizer-0.1.2/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup
 
 setup(
     name='CloudEdgeAssetsOptimizer',
-    version='0.1.1',
+    version='0.1.2',
     author='Paulius Tervydis',
     author_email='Paulius.Tervydis@ktu.lt',
     description="""
 
 # CloudEdgeAssetsOptimizer   
     
 CloudEdgeAssetsOptimizer is a software tool designed to evaluate and
```

