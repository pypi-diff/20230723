# Comparing `tmp/finanalysis-0.1.0.tar.gz` & `tmp/finanalysis-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "finanalysis-0.1.0.tar", last modified: Sun Jul 23 15:34:26 2023, max compression
+gzip compressed data, was "finanalysis-0.2.0.tar", last modified: Sun Jul 23 15:39:12 2023, max compression
```

## Comparing `finanalysis-0.1.0.tar` & `finanalysis-0.2.0.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 15:34:26.108869 finanalysis-0.1.0/
--rw-rw-rw-   0        0        0      714 2023-07-23 15:34:26.107896 finanalysis-0.1.0/PKG-INFO
--rw-rw-rw-   0        0        0        0 2023-07-23 07:45:30.000000 finanalysis-0.1.0/README.md
-drwxrwxrwx   0        0        0        0 2023-07-23 15:34:26.094754 finanalysis-0.1.0/finanalysis.egg-info/
-drwxrwxrwx   0        0        0        0 2023-07-23 15:34:26.105817 finanalysis-0.1.0/finanalysis.egg-info/.ipynb_checkpoints/
--rw-rw-rw-   0        0        0      721 2023-07-23 07:52:19.000000 finanalysis-0.1.0/finanalysis.egg-info/.ipynb_checkpoints/PKG-INFO-checkpoint
--rw-rw-rw-   0        0        0      227 2023-07-23 07:52:19.000000 finanalysis-0.1.0/finanalysis.egg-info/.ipynb_checkpoints/SOURCES-checkpoint.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 07:52:19.000000 finanalysis-0.1.0/finanalysis.egg-info/.ipynb_checkpoints/dependency_links-checkpoint.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 07:52:19.000000 finanalysis-0.1.0/finanalysis.egg-info/.ipynb_checkpoints/top_level-checkpoint.txt
--rw-rw-rw-   0        0        0      714 2023-07-23 15:34:25.000000 finanalysis-0.1.0/finanalysis.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      452 2023-07-23 15:34:25.000000 finanalysis-0.1.0/finanalysis.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 15:34:25.000000 finanalysis-0.1.0/finanalysis.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       32 2023-07-23 15:34:25.000000 finanalysis-0.1.0/finanalysis.egg-info/requires.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 15:34:25.000000 finanalysis-0.1.0/finanalysis.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-23 15:34:26.109809 finanalysis-0.1.0/setup.cfg
--rw-rw-rw-   0        0        0      938 2023-07-23 15:34:18.000000 finanalysis-0.1.0/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 15:39:12.085517 finanalysis-0.2.0/
+-rw-rw-rw-   0        0        0      714 2023-07-23 15:39:12.085073 finanalysis-0.2.0/PKG-INFO
+-rw-rw-rw-   0        0        0        0 2023-07-23 07:45:30.000000 finanalysis-0.2.0/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 15:39:12.069950 finanalysis-0.2.0/finanalysis.egg-info/
+drwxrwxrwx   0        0        0        0 2023-07-23 15:39:12.082080 finanalysis-0.2.0/finanalysis.egg-info/.ipynb_checkpoints/
+-rw-rw-rw-   0        0        0      721 2023-07-23 07:52:19.000000 finanalysis-0.2.0/finanalysis.egg-info/.ipynb_checkpoints/PKG-INFO-checkpoint
+-rw-rw-rw-   0        0        0      227 2023-07-23 07:52:19.000000 finanalysis-0.2.0/finanalysis.egg-info/.ipynb_checkpoints/SOURCES-checkpoint.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 07:52:19.000000 finanalysis-0.2.0/finanalysis.egg-info/.ipynb_checkpoints/dependency_links-checkpoint.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 07:52:19.000000 finanalysis-0.2.0/finanalysis.egg-info/.ipynb_checkpoints/top_level-checkpoint.txt
+-rw-rw-rw-   0        0        0      714 2023-07-23 15:39:11.000000 finanalysis-0.2.0/finanalysis.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      452 2023-07-23 15:39:11.000000 finanalysis-0.2.0/finanalysis.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 15:39:11.000000 finanalysis-0.2.0/finanalysis.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       32 2023-07-23 15:39:11.000000 finanalysis-0.2.0/finanalysis.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 15:39:11.000000 finanalysis-0.2.0/finanalysis.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 15:39:12.086560 finanalysis-0.2.0/setup.cfg
+-rw-rw-rw-   0        0        0      938 2023-07-23 15:39:08.000000 finanalysis-0.2.0/setup.py
```

### Comparing `finanalysis-0.1.0/PKG-INFO` & `finanalysis-0.2.0/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: finanalysis
-Version: 0.1.0
+Version: 0.2.0
 Summary: A package for analyzing Financial Instruments like stocks.
 Home-page: https://github.com/MANOJ21K/FinOps/blob/main/custom_package
 Author: Manoj Kumar
 Author-email: manojkotary@gmail.com
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `finanalysis-0.1.0/finanalysis.egg-info/.ipynb_checkpoints/PKG-INFO-checkpoint` & `finanalysis-0.2.0/finanalysis.egg-info/.ipynb_checkpoints/PKG-INFO-checkpoint`

 * *Files identical despite different names*

### Comparing `finanalysis-0.1.0/finanalysis.egg-info/PKG-INFO` & `finanalysis-0.2.0/finanalysis.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: finanalysis
-Version: 0.1.0
+Version: 0.2.0
 Summary: A package for analyzing Financial Instruments like stocks.
 Home-page: https://github.com/MANOJ21K/FinOps/blob/main/custom_package
 Author: Manoj Kumar
 Author-email: manojkotary@gmail.com
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `finanalysis-0.1.0/setup.py` & `finanalysis-0.2.0/setup.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name='finanalysis',
-    version='0.1.0',
+    version='0.2.0',
     packages=find_packages(),
     install_requires=[
         'finnhub',
         'pandas',
         'numpy',
         'matplotlib'
     ],
```

