# Comparing `tmp/CloudEdgeAssetsOptimizer-0.1.2.tar.gz` & `tmp/CloudEdgeAssetsOptimizer-0.1.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "CloudEdgeAssetsOptimizer-0.1.2.tar", last modified: Sun Jul 23 12:40:48 2023, max compression
+gzip compressed data, was "CloudEdgeAssetsOptimizer-0.1.3.tar", last modified: Sun Jul 23 13:00:23 2023, max compression
```

## Comparing `CloudEdgeAssetsOptimizer-0.1.2.tar` & `CloudEdgeAssetsOptimizer-0.1.3.tar`

### file list

```diff
@@ -1,20 +1,21 @@
-drwxr-xr-x   0 paulius    (501) staff       (20)        0 2023-07-23 12:40:47.000000 CloudEdgeAssetsOptimizer-0.1.2/
-drwxr-xr-x   0 paulius    (501) staff       (20)        0 2023-07-23 12:40:47.000000 CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer/
--rw-r--r--   0 paulius    (501) staff       (20)     1435 2023-07-23 12:05:19.000000 CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer/CloudEdgeAssetOptimizer.py
--rw-r--r--   0 paulius    (501) staff       (20)       38 2023-07-23 12:34:07.000000 CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer/__init__.py
--rw-r--r--   0 paulius    (501) staff       (20)     7147 2023-07-23 12:05:19.000000 CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer/calculation.py
--rw-r--r--   0 paulius    (501) staff       (20)     3153 2023-07-23 12:05:19.000000 CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer/graph.py
--rw-r--r--   0 paulius    (501) staff       (20)    15033 2023-07-23 12:05:19.000000 CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer/gui_frontend.py
--rw-r--r--   0 paulius    (501) staff       (20)     3375 2023-07-23 12:05:19.000000 CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer/optimizer.py
--rw-r--r--   0 paulius    (501) staff       (20)    13264 2023-07-23 12:05:19.000000 CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer/qsystems.py
-drwxr-xr-x   0 paulius    (501) staff       (20)        0 2023-07-23 12:40:47.000000 CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer.egg-info/
--rw-r--r--   0 paulius    (501) staff       (20)     1691 2023-07-23 12:40:48.000000 CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer.egg-info/PKG-INFO
--rw-r--r--   0 paulius    (501) staff       (20)      544 2023-07-23 12:40:48.000000 CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer.egg-info/SOURCES.txt
--rw-r--r--   0 paulius    (501) staff       (20)        1 2023-07-23 12:40:48.000000 CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer.egg-info/dependency_links.txt
--rw-r--r--   0 paulius    (501) staff       (20)       31 2023-07-23 12:40:48.000000 CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer.egg-info/requires.txt
--rw-r--r--   0 paulius    (501) staff       (20)       25 2023-07-23 12:40:48.000000 CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer.egg-info/top_level.txt
--rw-r--r--   0 paulius    (501) staff       (20)     1067 2023-07-23 11:50:18.000000 CloudEdgeAssetsOptimizer-0.1.2/LICENSE
--rw-r--r--   0 paulius    (501) staff       (20)     1691 2023-07-23 12:40:48.000000 CloudEdgeAssetsOptimizer-0.1.2/PKG-INFO
--rw-r--r--   0 paulius    (501) staff       (20)     1101 2023-07-23 12:24:27.000000 CloudEdgeAssetsOptimizer-0.1.2/README.md
--rw-r--r--   0 paulius    (501) staff       (20)       38 2023-07-23 12:40:48.000000 CloudEdgeAssetsOptimizer-0.1.2/setup.cfg
--rw-r--r--   0 paulius    (501) staff       (20)     1975 2023-07-23 12:34:37.000000 CloudEdgeAssetsOptimizer-0.1.2/setup.py
+drwxr-xr-x   0 paulius    (501) staff       (20)        0 2023-07-23 13:00:23.000000 CloudEdgeAssetsOptimizer-0.1.3/
+drwxr-xr-x   0 paulius    (501) staff       (20)        0 2023-07-23 13:00:23.000000 CloudEdgeAssetsOptimizer-0.1.3/CloudEdgeAssetsOptimizer/
+-rw-r--r--   0 paulius    (501) staff       (20)     1435 2023-07-23 12:05:19.000000 CloudEdgeAssetsOptimizer-0.1.3/CloudEdgeAssetsOptimizer/CloudEdgeAssetOptimizer.py
+-rw-r--r--   0 paulius    (501) staff       (20)       38 2023-07-23 12:59:33.000000 CloudEdgeAssetsOptimizer-0.1.3/CloudEdgeAssetsOptimizer/__init__.py
+-rw-r--r--   0 paulius    (501) staff       (20)     7147 2023-07-23 12:05:19.000000 CloudEdgeAssetsOptimizer-0.1.3/CloudEdgeAssetsOptimizer/calculation.py
+-rw-r--r--   0 paulius    (501) staff       (20)     3153 2023-07-23 12:05:19.000000 CloudEdgeAssetsOptimizer-0.1.3/CloudEdgeAssetsOptimizer/graph.py
+-rw-r--r--   0 paulius    (501) staff       (20)    15033 2023-07-23 12:05:19.000000 CloudEdgeAssetsOptimizer-0.1.3/CloudEdgeAssetsOptimizer/gui_frontend.py
+-rw-r--r--   0 paulius    (501) staff       (20)     3375 2023-07-23 12:05:19.000000 CloudEdgeAssetsOptimizer-0.1.3/CloudEdgeAssetsOptimizer/optimizer.py
+-rw-r--r--   0 paulius    (501) staff       (20)    13264 2023-07-23 12:05:19.000000 CloudEdgeAssetsOptimizer-0.1.3/CloudEdgeAssetsOptimizer/qsystems.py
+drwxr-xr-x   0 paulius    (501) staff       (20)        0 2023-07-23 13:00:23.000000 CloudEdgeAssetsOptimizer-0.1.3/CloudEdgeAssetsOptimizer.egg-info/
+-rw-r--r--   0 paulius    (501) staff       (20)     1691 2023-07-23 13:00:23.000000 CloudEdgeAssetsOptimizer-0.1.3/CloudEdgeAssetsOptimizer.egg-info/PKG-INFO
+-rw-r--r--   0 paulius    (501) staff       (20)      595 2023-07-23 13:00:23.000000 CloudEdgeAssetsOptimizer-0.1.3/CloudEdgeAssetsOptimizer.egg-info/SOURCES.txt
+-rw-r--r--   0 paulius    (501) staff       (20)        1 2023-07-23 13:00:23.000000 CloudEdgeAssetsOptimizer-0.1.3/CloudEdgeAssetsOptimizer.egg-info/dependency_links.txt
+-rw-r--r--   0 paulius    (501) staff       (20)      100 2023-07-23 13:00:23.000000 CloudEdgeAssetsOptimizer-0.1.3/CloudEdgeAssetsOptimizer.egg-info/entry_points.txt
+-rw-r--r--   0 paulius    (501) staff       (20)       31 2023-07-23 13:00:23.000000 CloudEdgeAssetsOptimizer-0.1.3/CloudEdgeAssetsOptimizer.egg-info/requires.txt
+-rw-r--r--   0 paulius    (501) staff       (20)       25 2023-07-23 13:00:23.000000 CloudEdgeAssetsOptimizer-0.1.3/CloudEdgeAssetsOptimizer.egg-info/top_level.txt
+-rw-r--r--   0 paulius    (501) staff       (20)     1067 2023-07-23 11:50:18.000000 CloudEdgeAssetsOptimizer-0.1.3/LICENSE
+-rw-r--r--   0 paulius    (501) staff       (20)     1691 2023-07-23 13:00:23.000000 CloudEdgeAssetsOptimizer-0.1.3/PKG-INFO
+-rw-r--r--   0 paulius    (501) staff       (20)     1101 2023-07-23 12:24:27.000000 CloudEdgeAssetsOptimizer-0.1.3/README.md
+-rw-r--r--   0 paulius    (501) staff       (20)       38 2023-07-23 13:00:23.000000 CloudEdgeAssetsOptimizer-0.1.3/setup.cfg
+-rw-r--r--   0 paulius    (501) staff       (20)     2136 2023-07-23 12:59:10.000000 CloudEdgeAssetsOptimizer-0.1.3/setup.py
```

### Comparing `CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer/CloudEdgeAssetOptimizer.py` & `CloudEdgeAssetsOptimizer-0.1.3/CloudEdgeAssetsOptimizer/CloudEdgeAssetOptimizer.py`

 * *Files identical despite different names*

### Comparing `CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer/calculation.py` & `CloudEdgeAssetsOptimizer-0.1.3/CloudEdgeAssetsOptimizer/calculation.py`

 * *Files identical despite different names*

### Comparing `CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer/graph.py` & `CloudEdgeAssetsOptimizer-0.1.3/CloudEdgeAssetsOptimizer/graph.py`

 * *Files identical despite different names*

### Comparing `CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer/gui_frontend.py` & `CloudEdgeAssetsOptimizer-0.1.3/CloudEdgeAssetsOptimizer/gui_frontend.py`

 * *Files identical despite different names*

### Comparing `CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer/optimizer.py` & `CloudEdgeAssetsOptimizer-0.1.3/CloudEdgeAssetsOptimizer/optimizer.py`

 * *Files identical despite different names*

### Comparing `CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer/qsystems.py` & `CloudEdgeAssetsOptimizer-0.1.3/CloudEdgeAssetsOptimizer/qsystems.py`

 * *Files identical despite different names*

### Comparing `CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer.egg-info/PKG-INFO` & `CloudEdgeAssetsOptimizer-0.1.3/CloudEdgeAssetsOptimizer.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: CloudEdgeAssetsOptimizer
-Version: 0.1.2
+Version: 0.1.3
 Summary: # CloudEdgeAssetsOptimizer   
 Home-page: https://github.com/pauterv/CloudEdgeAssetsOptimizer
 Author: Paulius Tervydis
 Author-email: Paulius.Tervydis@ktu.lt
 Classifier: Development Status :: 3 - Alpha
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
```

### Comparing `CloudEdgeAssetsOptimizer-0.1.2/CloudEdgeAssetsOptimizer.egg-info/SOURCES.txt` & `CloudEdgeAssetsOptimizer-0.1.3/CloudEdgeAssetsOptimizer.egg-info/SOURCES.txt`

 * *Files 5% similar despite different names*

```diff
@@ -7,9 +7,10 @@
 CloudEdgeAssetsOptimizer/graph.py
 CloudEdgeAssetsOptimizer/gui_frontend.py
 CloudEdgeAssetsOptimizer/optimizer.py
 CloudEdgeAssetsOptimizer/qsystems.py
 CloudEdgeAssetsOptimizer.egg-info/PKG-INFO
 CloudEdgeAssetsOptimizer.egg-info/SOURCES.txt
 CloudEdgeAssetsOptimizer.egg-info/dependency_links.txt
+CloudEdgeAssetsOptimizer.egg-info/entry_points.txt
 CloudEdgeAssetsOptimizer.egg-info/requires.txt
 CloudEdgeAssetsOptimizer.egg-info/top_level.txt
```

### Comparing `CloudEdgeAssetsOptimizer-0.1.2/LICENSE` & `CloudEdgeAssetsOptimizer-0.1.3/LICENSE`

 * *Files identical despite different names*

### Comparing `CloudEdgeAssetsOptimizer-0.1.2/PKG-INFO` & `CloudEdgeAssetsOptimizer-0.1.3/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: CloudEdgeAssetsOptimizer
-Version: 0.1.2
+Version: 0.1.3
 Summary: # CloudEdgeAssetsOptimizer   
 Home-page: https://github.com/pauterv/CloudEdgeAssetsOptimizer
 Author: Paulius Tervydis
 Author-email: Paulius.Tervydis@ktu.lt
 Classifier: Development Status :: 3 - Alpha
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
```

### Comparing `CloudEdgeAssetsOptimizer-0.1.2/README.md` & `CloudEdgeAssetsOptimizer-0.1.3/README.md`

 * *Files identical despite different names*

### Comparing `CloudEdgeAssetsOptimizer-0.1.2/setup.py` & `CloudEdgeAssetsOptimizer-0.1.3/setup.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup
 
 setup(
     name='CloudEdgeAssetsOptimizer',
-    version='0.1.2',
+    version='0.1.3',
     author='Paulius Tervydis',
     author_email='Paulius.Tervydis@ktu.lt',
     description="""
 
 # CloudEdgeAssetsOptimizer   
     
 CloudEdgeAssetsOptimizer is a software tool designed to evaluate and 
@@ -39,14 +39,19 @@
     install_requires=[
         # List any dependencies your package requires
         'numpy',
         'pandas',
         'matplotlib',
         'Pillow',
     ],
+    entry_points={
+        'console_scripts': [
+            'CloudEdgeAssetsOptimizer=CloudEdgeAssetsOptimizer.CloudEdgeAssetsOptimizer:main',
+        ],
+    },
     classifiers=[
         'Development Status :: 3 - Alpha',
         'License :: OSI Approved :: MIT License',
         'Programming Language :: Python :: 3',
         'Programming Language :: Python :: 3.6',
         'Programming Language :: Python :: 3.7',
         'Programming Language :: Python :: 3.8',
```

