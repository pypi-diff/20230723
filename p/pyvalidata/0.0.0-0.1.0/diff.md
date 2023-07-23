# Comparing `tmp/pyvalidata-0.0.0.tar.gz` & `tmp/pyvalidata-0.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyvalidata-0.0.0.tar", last modified: Sun Jul 23 07:17:10 2023, max compression
+gzip compressed data, was "pyvalidata-0.1.0.tar", last modified: Sun Jul 23 07:11:21 2023, max compression
```

## Comparing `pyvalidata-0.0.0.tar` & `pyvalidata-0.1.0.tar`

### file list

```diff
@@ -1,13 +1,13 @@
-drwxr-xr-x   0 eklavyatomar   (502) staff       (20)        0 2023-07-23 07:17:10.112529 pyvalidata-0.0.0/
--rw-r--r--   0 eklavyatomar   (502) staff       (20)     1074 2023-07-21 12:41:43.000000 pyvalidata-0.0.0/LICENSE
--rw-r--r--   0 eklavyatomar   (502) staff       (20)      724 2023-07-23 07:17:10.112363 pyvalidata-0.0.0/PKG-INFO
-drwxr-xr-x   0 eklavyatomar   (502) staff       (20)        0 2023-07-23 07:17:10.111219 pyvalidata-0.0.0/pyvalidata/
--rw-r--r--   0 eklavyatomar   (502) staff       (20)     8514 2023-07-22 08:57:48.000000 pyvalidata-0.0.0/pyvalidata/__init__.py
--rw-r--r--   0 eklavyatomar   (502) staff       (20)     4048 2023-07-23 07:05:18.000000 pyvalidata-0.0.0/pyvalidata/validators.py
-drwxr-xr-x   0 eklavyatomar   (502) staff       (20)        0 2023-07-23 07:17:10.112098 pyvalidata-0.0.0/pyvalidata.egg-info/
--rw-r--r--   0 eklavyatomar   (502) staff       (20)      724 2023-07-23 07:17:10.000000 pyvalidata-0.0.0/pyvalidata.egg-info/PKG-INFO
--rw-r--r--   0 eklavyatomar   (502) staff       (20)      200 2023-07-23 07:17:10.000000 pyvalidata-0.0.0/pyvalidata.egg-info/SOURCES.txt
--rw-r--r--   0 eklavyatomar   (502) staff       (20)        1 2023-07-23 07:17:10.000000 pyvalidata-0.0.0/pyvalidata.egg-info/dependency_links.txt
--rw-r--r--   0 eklavyatomar   (502) staff       (20)       11 2023-07-23 07:17:10.000000 pyvalidata-0.0.0/pyvalidata.egg-info/top_level.txt
--rw-r--r--   0 eklavyatomar   (502) staff       (20)       38 2023-07-23 07:17:10.112590 pyvalidata-0.0.0/setup.cfg
--rw-r--r--   0 eklavyatomar   (502) staff       (20)      762 2023-07-23 07:16:30.000000 pyvalidata-0.0.0/setup.py
+drwxr-xr-x   0 eklavyatomar   (502) staff       (20)        0 2023-07-23 07:11:21.233834 pyvalidata-0.1.0/
+-rw-r--r--   0 eklavyatomar   (502) staff       (20)     1074 2023-07-21 12:41:43.000000 pyvalidata-0.1.0/LICENSE
+-rw-r--r--   0 eklavyatomar   (502) staff       (20)      724 2023-07-23 07:11:21.233636 pyvalidata-0.1.0/PKG-INFO
+drwxr-xr-x   0 eklavyatomar   (502) staff       (20)        0 2023-07-23 07:11:21.232440 pyvalidata-0.1.0/pyvalidata/
+-rw-r--r--   0 eklavyatomar   (502) staff       (20)     8514 2023-07-22 08:57:48.000000 pyvalidata-0.1.0/pyvalidata/__init__.py
+-rw-r--r--   0 eklavyatomar   (502) staff       (20)     4048 2023-07-23 07:05:18.000000 pyvalidata-0.1.0/pyvalidata/validators.py
+drwxr-xr-x   0 eklavyatomar   (502) staff       (20)        0 2023-07-23 07:11:21.233350 pyvalidata-0.1.0/pyvalidata.egg-info/
+-rw-r--r--   0 eklavyatomar   (502) staff       (20)      724 2023-07-23 07:11:21.000000 pyvalidata-0.1.0/pyvalidata.egg-info/PKG-INFO
+-rw-r--r--   0 eklavyatomar   (502) staff       (20)      200 2023-07-23 07:11:21.000000 pyvalidata-0.1.0/pyvalidata.egg-info/SOURCES.txt
+-rw-r--r--   0 eklavyatomar   (502) staff       (20)        1 2023-07-23 07:11:21.000000 pyvalidata-0.1.0/pyvalidata.egg-info/dependency_links.txt
+-rw-r--r--   0 eklavyatomar   (502) staff       (20)       11 2023-07-23 07:11:21.000000 pyvalidata-0.1.0/pyvalidata.egg-info/top_level.txt
+-rw-r--r--   0 eklavyatomar   (502) staff       (20)       38 2023-07-23 07:11:21.233925 pyvalidata-0.1.0/setup.cfg
+-rw-r--r--   0 eklavyatomar   (502) staff       (20)      778 2023-07-21 12:41:28.000000 pyvalidata-0.1.0/setup.py
```

### Comparing `pyvalidata-0.0.0/LICENSE` & `pyvalidata-0.1.0/LICENSE`

 * *Files identical despite different names*

### Comparing `pyvalidata-0.0.0/PKG-INFO` & `pyvalidata-0.1.0/PKG-INFO`

 * *Files 14% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyvalidata
-Version: 0.0.0
+Version: 0.1.0
 Summary: A Python package for data validation
 Home-page: https://github.com/EklavyaT/pyvalidata
 Author: Eklavya Tomar
 Author-email: eklavyaprogramming@gmail.com
 License: UNKNOWN
 Platform: UNKNOWN
 Classifier: Development Status :: 3 - Alpha
```

### Comparing `pyvalidata-0.0.0/pyvalidata/__init__.py` & `pyvalidata-0.1.0/pyvalidata/__init__.py`

 * *Files identical despite different names*

### Comparing `pyvalidata-0.0.0/pyvalidata/validators.py` & `pyvalidata-0.1.0/pyvalidata/validators.py`

 * *Files identical despite different names*

### Comparing `pyvalidata-0.0.0/pyvalidata.egg-info/PKG-INFO` & `pyvalidata-0.1.0/pyvalidata.egg-info/PKG-INFO`

 * *Files 14% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyvalidata
-Version: 0.0.0
+Version: 0.1.0
 Summary: A Python package for data validation
 Home-page: https://github.com/EklavyaT/pyvalidata
 Author: Eklavya Tomar
 Author-email: eklavyaprogramming@gmail.com
 License: UNKNOWN
 Platform: UNKNOWN
 Classifier: Development Status :: 3 - Alpha
```

### Comparing `pyvalidata-0.0.0/setup.py` & `pyvalidata-0.1.0/setup.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup
 
 setup(
     name='pyvalidata',
-    
+    version='0.1.0',
     description='A Python package for data validation',
     author='Eklavya Tomar',
     author_email='eklavyaprogramming@gmail.com',
     url='https://github.com/EklavyaT/pyvalidata',
     packages=['pyvalidata'],
     install_requires=[],
     classifiers=[
```

