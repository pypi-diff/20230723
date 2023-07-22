# Comparing `tmp/sita_package_ml-0.1.1.tar.gz` & `tmp/sita_package_ml-0.1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "sita_package_ml-0.1.1.tar", last modified: Sat Jul 22 21:29:37 2023, max compression
+gzip compressed data, was "sita_package_ml-0.1.2.tar", last modified: Sat Jul 22 22:04:50 2023, max compression
```

## Comparing `sita_package_ml-0.1.1.tar` & `sita_package_ml-0.1.2.tar`

### file list

```diff
@@ -1,17 +1,17 @@
-drwxrwxr-x   0 djeinaba  (1000) djeinaba  (1000)        0 2023-07-22 21:29:37.106692 sita_package_ml-0.1.1/
--rw-rw-r--   0 djeinaba  (1000) djeinaba  (1000)     1073 2023-07-22 19:46:38.000000 sita_package_ml-0.1.1/LICENSE
--rw-rw-r--   0 djeinaba  (1000) djeinaba  (1000)      491 2023-07-22 21:29:37.106692 sita_package_ml-0.1.1/PKG-INFO
--rw-rw-r--   0 djeinaba  (1000) djeinaba  (1000)        0 2023-07-22 19:29:26.000000 sita_package_ml-0.1.1/README.md
--rw-rw-r--   0 djeinaba  (1000) djeinaba  (1000)       38 2023-07-22 21:29:37.106692 sita_package_ml-0.1.1/setup.cfg
--rwxr-xr-x   0 djeinaba  (1000) djeinaba  (1000)      855 2023-07-22 21:27:19.000000 sita_package_ml-0.1.1/setup.py
-drwxrwxr-x   0 djeinaba  (1000) djeinaba  (1000)        0 2023-07-22 21:29:37.102692 sita_package_ml-0.1.1/sita_package_ml/
--rwxr-xr-x   0 djeinaba  (1000) djeinaba  (1000)      104 2023-07-22 21:27:59.000000 sita_package_ml-0.1.1/sita_package_ml/__init__.py
--rw-rw-rw-   0 djeinaba  (1000) djeinaba  (1000)     4695 2023-07-22 21:08:28.000000 sita_package_ml-0.1.1/sita_package_ml/code_src.py
-drwxrwxr-x   0 djeinaba  (1000) djeinaba  (1000)        0 2023-07-22 21:29:37.106692 sita_package_ml-0.1.1/sita_package_ml.egg-info/
--rw-rw-r--   0 djeinaba  (1000) djeinaba  (1000)      491 2023-07-22 21:29:37.000000 sita_package_ml-0.1.1/sita_package_ml.egg-info/PKG-INFO
--rw-rw-r--   0 djeinaba  (1000) djeinaba  (1000)      289 2023-07-22 21:29:37.000000 sita_package_ml-0.1.1/sita_package_ml.egg-info/SOURCES.txt
--rw-rw-r--   0 djeinaba  (1000) djeinaba  (1000)        1 2023-07-22 21:29:37.000000 sita_package_ml-0.1.1/sita_package_ml.egg-info/dependency_links.txt
--rw-rw-r--   0 djeinaba  (1000) djeinaba  (1000)       22 2023-07-22 21:29:37.000000 sita_package_ml-0.1.1/sita_package_ml.egg-info/requires.txt
--rw-rw-r--   0 djeinaba  (1000) djeinaba  (1000)       16 2023-07-22 21:29:37.000000 sita_package_ml-0.1.1/sita_package_ml.egg-info/top_level.txt
-drwxrwxr-x   0 djeinaba  (1000) djeinaba  (1000)        0 2023-07-22 21:29:37.106692 sita_package_ml-0.1.1/test/
--rw-rw-r--   0 djeinaba  (1000) djeinaba  (1000)      900 2023-07-22 21:23:30.000000 sita_package_ml-0.1.1/test/test.py
+drwxrwxr-x   0 djeinaba  (1000) djeinaba  (1000)        0 2023-07-22 22:04:50.562959 sita_package_ml-0.1.2/
+-rw-rw-r--   0 djeinaba  (1000) djeinaba  (1000)     1073 2023-07-22 19:46:38.000000 sita_package_ml-0.1.2/LICENSE
+-rw-rw-r--   0 djeinaba  (1000) djeinaba  (1000)      491 2023-07-22 22:04:50.558959 sita_package_ml-0.1.2/PKG-INFO
+-rw-rw-r--   0 djeinaba  (1000) djeinaba  (1000)        0 2023-07-22 19:29:26.000000 sita_package_ml-0.1.2/README.md
+-rw-rw-r--   0 djeinaba  (1000) djeinaba  (1000)       38 2023-07-22 22:04:50.562959 sita_package_ml-0.1.2/setup.cfg
+-rwxr-xr-x   0 djeinaba  (1000) djeinaba  (1000)      896 2023-07-22 21:59:19.000000 sita_package_ml-0.1.2/setup.py
+drwxrwxr-x   0 djeinaba  (1000) djeinaba  (1000)        0 2023-07-22 22:04:50.558959 sita_package_ml-0.1.2/sita_package_ml/
+-rwxr-xr-x   0 djeinaba  (1000) djeinaba  (1000)      104 2023-07-22 22:00:23.000000 sita_package_ml-0.1.2/sita_package_ml/__init__.py
+-rw-rw-rw-   0 djeinaba  (1000) djeinaba  (1000)     4695 2023-07-22 21:08:28.000000 sita_package_ml-0.1.2/sita_package_ml/code_src.py
+drwxrwxr-x   0 djeinaba  (1000) djeinaba  (1000)        0 2023-07-22 22:04:50.558959 sita_package_ml-0.1.2/sita_package_ml.egg-info/
+-rw-rw-r--   0 djeinaba  (1000) djeinaba  (1000)      491 2023-07-22 22:04:50.000000 sita_package_ml-0.1.2/sita_package_ml.egg-info/PKG-INFO
+-rw-rw-r--   0 djeinaba  (1000) djeinaba  (1000)      289 2023-07-22 22:04:50.000000 sita_package_ml-0.1.2/sita_package_ml.egg-info/SOURCES.txt
+-rw-rw-r--   0 djeinaba  (1000) djeinaba  (1000)        1 2023-07-22 22:04:50.000000 sita_package_ml-0.1.2/sita_package_ml.egg-info/dependency_links.txt
+-rw-rw-r--   0 djeinaba  (1000) djeinaba  (1000)       52 2023-07-22 22:04:50.000000 sita_package_ml-0.1.2/sita_package_ml.egg-info/requires.txt
+-rw-rw-r--   0 djeinaba  (1000) djeinaba  (1000)       16 2023-07-22 22:04:50.000000 sita_package_ml-0.1.2/sita_package_ml.egg-info/top_level.txt
+drwxrwxr-x   0 djeinaba  (1000) djeinaba  (1000)        0 2023-07-22 22:04:50.558959 sita_package_ml-0.1.2/test/
+-rw-rw-r--   0 djeinaba  (1000) djeinaba  (1000)      900 2023-07-22 21:23:30.000000 sita_package_ml-0.1.2/test/test.py
```

### Comparing `sita_package_ml-0.1.1/LICENSE` & `sita_package_ml-0.1.2/LICENSE`

 * *Files identical despite different names*

### Comparing `sita_package_ml-0.1.1/setup.py` & `sita_package_ml-0.1.2/setup.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,20 +1,21 @@
 import setuptools
 setuptools.setup(
     name="sita_package_ml",
-    version="0.1.1",                        
+    version="0.1.2",                        
     author="Djeinaba",
     author_email="djeinaba147@gmail.com",
     description="buiding a python package",
     long_description="python package for ML models",
     long_description_content_type="hello this is just a test",
     install_requires=[                     
         "numpy",
-        "sklearn>",
+        "scikit-learn>=0.24.2",
         "plotly",
+        "matplotlib>=3.3.0",
         
                                                   
     ],                                             
     url="https://gitlab.com/Djeinaba_Doro/test_project",  
     packages=setuptools.find_packages(),
     classifiers=[                               
         "Programming Language :: Python :: 3.7",
```

### Comparing `sita_package_ml-0.1.1/sita_package_ml/code_src.py` & `sita_package_ml-0.1.2/sita_package_ml/code_src.py`

 * *Files identical despite different names*

### Comparing `sita_package_ml-0.1.1/test/test.py` & `sita_package_ml-0.1.2/test/test.py`

 * *Files identical despite different names*

