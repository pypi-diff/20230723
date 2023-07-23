# Comparing `tmp/photondemo-0.0.5.tar.gz` & `tmp/photondemo-0.0.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "photondemo-0.0.5.tar", last modified: Sun Jul 23 19:16:29 2023, max compression
+gzip compressed data, was "photondemo-0.0.6.tar", last modified: Sun Jul 23 19:47:51 2023, max compression
```

## Comparing `photondemo-0.0.5.tar` & `photondemo-0.0.6.tar`

### file list

```diff
@@ -1,19 +1,19 @@
-drwxr-xr-x   0 charlie    (501) staff       (20)        0 2023-07-23 19:16:29.588650 photondemo-0.0.5/
--rw-r--r--   0 charlie    (501) staff       (20)      239 2023-07-23 19:16:29.588348 photondemo-0.0.5/PKG-INFO
-drwxr-xr-x   0 charlie    (501) staff       (20)        0 2023-07-23 19:16:29.567655 photondemo-0.0.5/logger/
--rw-r--r--   0 charlie    (501) staff       (20)        0 2023-07-22 16:45:12.000000 photondemo-0.0.5/logger/__init__.py
--rw-r--r--   0 charlie    (501) staff       (20)      360 2023-07-22 18:23:19.000000 photondemo-0.0.5/logger/logger.py
-drwxr-xr-x   0 charlie    (501) staff       (20)        0 2023-07-23 19:16:29.585232 photondemo-0.0.5/photondemo.egg-info/
--rw-r--r--   0 charlie    (501) staff       (20)      239 2023-07-23 19:16:29.000000 photondemo-0.0.5/photondemo.egg-info/PKG-INFO
--rw-r--r--   0 charlie    (501) staff       (20)      302 2023-07-23 19:16:29.000000 photondemo-0.0.5/photondemo.egg-info/SOURCES.txt
--rw-r--r--   0 charlie    (501) staff       (20)        1 2023-07-23 19:16:29.000000 photondemo-0.0.5/photondemo.egg-info/dependency_links.txt
--rw-r--r--   0 charlie    (501) staff       (20)        9 2023-07-23 19:16:29.000000 photondemo-0.0.5/photondemo.egg-info/requires.txt
--rw-r--r--   0 charlie    (501) staff       (20)       28 2023-07-23 19:16:29.000000 photondemo-0.0.5/photondemo.egg-info/top_level.txt
-drwxr-xr-x   0 charlie    (501) staff       (20)        0 2023-07-23 19:16:29.586204 photondemo-0.0.5/processors/
--rw-r--r--   0 charlie    (501) staff       (20)        0 2023-07-22 15:10:25.000000 photondemo-0.0.5/processors/__init__.py
--rw-r--r--   0 charlie    (501) staff       (20)      806 2023-07-23 19:12:29.000000 photondemo-0.0.5/processors/processor.py
-drwxr-xr-x   0 charlie    (501) staff       (20)        0 2023-07-23 19:16:29.587520 photondemo-0.0.5/providers/
--rw-r--r--   0 charlie    (501) staff       (20)        0 2023-07-23 10:09:19.000000 photondemo-0.0.5/providers/__init__.py
--rw-r--r--   0 charlie    (501) staff       (20)     1448 2023-07-23 10:14:15.000000 photondemo-0.0.5/providers/openai.py
--rw-r--r--   0 charlie    (501) staff       (20)       38 2023-07-23 19:16:29.588891 photondemo-0.0.5/setup.cfg
--rw-r--r--   0 charlie    (501) staff       (20)      537 2023-07-23 19:16:20.000000 photondemo-0.0.5/setup.py
+drwxr-xr-x   0 charlie    (501) staff       (20)        0 2023-07-23 19:47:51.595909 photondemo-0.0.6/
+-rw-r--r--   0 charlie    (501) staff       (20)      239 2023-07-23 19:47:51.595589 photondemo-0.0.6/PKG-INFO
+drwxr-xr-x   0 charlie    (501) staff       (20)        0 2023-07-23 19:47:51.588409 photondemo-0.0.6/logger/
+-rw-r--r--   0 charlie    (501) staff       (20)        0 2023-07-22 16:45:12.000000 photondemo-0.0.6/logger/__init__.py
+-rw-r--r--   0 charlie    (501) staff       (20)      360 2023-07-22 18:23:19.000000 photondemo-0.0.6/logger/logger.py
+drwxr-xr-x   0 charlie    (501) staff       (20)        0 2023-07-23 19:47:51.593089 photondemo-0.0.6/photondemo.egg-info/
+-rw-r--r--   0 charlie    (501) staff       (20)      239 2023-07-23 19:47:51.000000 photondemo-0.0.6/photondemo.egg-info/PKG-INFO
+-rw-r--r--   0 charlie    (501) staff       (20)      302 2023-07-23 19:47:51.000000 photondemo-0.0.6/photondemo.egg-info/SOURCES.txt
+-rw-r--r--   0 charlie    (501) staff       (20)        1 2023-07-23 19:47:51.000000 photondemo-0.0.6/photondemo.egg-info/dependency_links.txt
+-rw-r--r--   0 charlie    (501) staff       (20)        9 2023-07-23 19:47:51.000000 photondemo-0.0.6/photondemo.egg-info/requires.txt
+-rw-r--r--   0 charlie    (501) staff       (20)       28 2023-07-23 19:47:51.000000 photondemo-0.0.6/photondemo.egg-info/top_level.txt
+drwxr-xr-x   0 charlie    (501) staff       (20)        0 2023-07-23 19:47:51.594106 photondemo-0.0.6/processors/
+-rw-r--r--   0 charlie    (501) staff       (20)        0 2023-07-22 15:10:25.000000 photondemo-0.0.6/processors/__init__.py
+-rw-r--r--   0 charlie    (501) staff       (20)      806 2023-07-23 19:12:29.000000 photondemo-0.0.6/processors/processor.py
+drwxr-xr-x   0 charlie    (501) staff       (20)        0 2023-07-23 19:47:51.595005 photondemo-0.0.6/providers/
+-rw-r--r--   0 charlie    (501) staff       (20)        0 2023-07-23 10:09:19.000000 photondemo-0.0.6/providers/__init__.py
+-rw-r--r--   0 charlie    (501) staff       (20)     1448 2023-07-23 10:14:15.000000 photondemo-0.0.6/providers/openai.py
+-rw-r--r--   0 charlie    (501) staff       (20)       38 2023-07-23 19:47:51.596027 photondemo-0.0.6/setup.cfg
+-rw-r--r--   0 charlie    (501) staff       (20)      539 2023-07-23 19:47:31.000000 photondemo-0.0.6/setup.py
```

### Comparing `photondemo-0.0.5/processors/processor.py` & `photondemo-0.0.6/processors/processor.py`

 * *Files identical despite different names*

### Comparing `photondemo-0.0.5/providers/openai.py` & `photondemo-0.0.6/providers/openai.py`

 * *Files identical despite different names*

### Comparing `photondemo-0.0.5/setup.py` & `photondemo-0.0.6/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from setuptools import find_packages, setup
 
-VERSION = "0.0.5"
+VERSION = "0.0.6"
 DESCRIPTION = ""
 LONG_DESCRIPTION = ""
 
 setup(
     name="photondemo",
     version=VERSION,
     author="Charlie Day",
@@ -16,7 +16,9 @@
     install_requires=[
         'requests',
     ],  # add any additional packages that
     # needs to be installed along with your package
     keywords=["python"],
     classifiers=[],
 )
+
+
```

