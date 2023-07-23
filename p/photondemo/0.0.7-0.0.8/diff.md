# Comparing `tmp/photondemo-0.0.7.tar.gz` & `tmp/photondemo-0.0.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "photondemo-0.0.7.tar", last modified: Sun Jul 23 19:55:22 2023, max compression
+gzip compressed data, was "photondemo-0.0.8.tar", last modified: Sun Jul 23 20:01:47 2023, max compression
```

## Comparing `photondemo-0.0.7.tar` & `photondemo-0.0.8.tar`

### file list

```diff
@@ -1,19 +1,19 @@
-drwxr-xr-x   0 charlie    (501) staff       (20)        0 2023-07-23 19:55:22.331260 photondemo-0.0.7/
--rw-r--r--   0 charlie    (501) staff       (20)      239 2023-07-23 19:55:22.330918 photondemo-0.0.7/PKG-INFO
-drwxr-xr-x   0 charlie    (501) staff       (20)        0 2023-07-23 19:55:22.308332 photondemo-0.0.7/logger/
--rw-r--r--   0 charlie    (501) staff       (20)        0 2023-07-22 16:45:12.000000 photondemo-0.0.7/logger/__init__.py
--rw-r--r--   0 charlie    (501) staff       (20)      360 2023-07-22 18:23:19.000000 photondemo-0.0.7/logger/logger.py
-drwxr-xr-x   0 charlie    (501) staff       (20)        0 2023-07-23 19:55:22.327473 photondemo-0.0.7/photondemo.egg-info/
--rw-r--r--   0 charlie    (501) staff       (20)      239 2023-07-23 19:55:22.000000 photondemo-0.0.7/photondemo.egg-info/PKG-INFO
--rw-r--r--   0 charlie    (501) staff       (20)      302 2023-07-23 19:55:22.000000 photondemo-0.0.7/photondemo.egg-info/SOURCES.txt
--rw-r--r--   0 charlie    (501) staff       (20)        1 2023-07-23 19:55:22.000000 photondemo-0.0.7/photondemo.egg-info/dependency_links.txt
--rw-r--r--   0 charlie    (501) staff       (20)        9 2023-07-23 19:55:22.000000 photondemo-0.0.7/photondemo.egg-info/requires.txt
--rw-r--r--   0 charlie    (501) staff       (20)       28 2023-07-23 19:55:22.000000 photondemo-0.0.7/photondemo.egg-info/top_level.txt
-drwxr-xr-x   0 charlie    (501) staff       (20)        0 2023-07-23 19:55:22.328554 photondemo-0.0.7/processors/
--rw-r--r--   0 charlie    (501) staff       (20)        0 2023-07-22 15:10:25.000000 photondemo-0.0.7/processors/__init__.py
--rw-r--r--   0 charlie    (501) staff       (20)      806 2023-07-23 19:12:29.000000 photondemo-0.0.7/processors/processor.py
-drwxr-xr-x   0 charlie    (501) staff       (20)        0 2023-07-23 19:55:22.330034 photondemo-0.0.7/providers/
--rw-r--r--   0 charlie    (501) staff       (20)        0 2023-07-23 10:09:19.000000 photondemo-0.0.7/providers/__init__.py
--rw-r--r--   0 charlie    (501) staff       (20)     1448 2023-07-23 10:14:15.000000 photondemo-0.0.7/providers/openai.py
--rw-r--r--   0 charlie    (501) staff       (20)       38 2023-07-23 19:55:22.331383 photondemo-0.0.7/setup.cfg
--rw-r--r--   0 charlie    (501) staff       (20)      539 2023-07-23 19:55:16.000000 photondemo-0.0.7/setup.py
+drwxr-xr-x   0 charlie    (501) staff       (20)        0 2023-07-23 20:01:47.177159 photondemo-0.0.8/
+-rw-r--r--   0 charlie    (501) staff       (20)      239 2023-07-23 20:01:47.176884 photondemo-0.0.8/PKG-INFO
+drwxr-xr-x   0 charlie    (501) staff       (20)        0 2023-07-23 20:01:47.170383 photondemo-0.0.8/logger/
+-rw-r--r--   0 charlie    (501) staff       (20)        0 2023-07-22 16:45:12.000000 photondemo-0.0.8/logger/__init__.py
+-rw-r--r--   0 charlie    (501) staff       (20)      360 2023-07-22 18:23:19.000000 photondemo-0.0.8/logger/logger.py
+drwxr-xr-x   0 charlie    (501) staff       (20)        0 2023-07-23 20:01:47.174250 photondemo-0.0.8/photondemo.egg-info/
+-rw-r--r--   0 charlie    (501) staff       (20)      239 2023-07-23 20:01:47.000000 photondemo-0.0.8/photondemo.egg-info/PKG-INFO
+-rw-r--r--   0 charlie    (501) staff       (20)      302 2023-07-23 20:01:47.000000 photondemo-0.0.8/photondemo.egg-info/SOURCES.txt
+-rw-r--r--   0 charlie    (501) staff       (20)        1 2023-07-23 20:01:47.000000 photondemo-0.0.8/photondemo.egg-info/dependency_links.txt
+-rw-r--r--   0 charlie    (501) staff       (20)        9 2023-07-23 20:01:47.000000 photondemo-0.0.8/photondemo.egg-info/requires.txt
+-rw-r--r--   0 charlie    (501) staff       (20)       28 2023-07-23 20:01:47.000000 photondemo-0.0.8/photondemo.egg-info/top_level.txt
+drwxr-xr-x   0 charlie    (501) staff       (20)        0 2023-07-23 20:01:47.175067 photondemo-0.0.8/processors/
+-rw-r--r--   0 charlie    (501) staff       (20)        0 2023-07-22 15:10:25.000000 photondemo-0.0.8/processors/__init__.py
+-rw-r--r--   0 charlie    (501) staff       (20)      806 2023-07-23 19:12:29.000000 photondemo-0.0.8/processors/processor.py
+drwxr-xr-x   0 charlie    (501) staff       (20)        0 2023-07-23 20:01:47.176152 photondemo-0.0.8/providers/
+-rw-r--r--   0 charlie    (501) staff       (20)        0 2023-07-23 10:09:19.000000 photondemo-0.0.8/providers/__init__.py
+-rw-r--r--   0 charlie    (501) staff       (20)     1448 2023-07-23 10:14:15.000000 photondemo-0.0.8/providers/openai.py
+-rw-r--r--   0 charlie    (501) staff       (20)       38 2023-07-23 20:01:47.177266 photondemo-0.0.8/setup.cfg
+-rw-r--r--   0 charlie    (501) staff       (20)      539 2023-07-23 20:00:17.000000 photondemo-0.0.8/setup.py
```

### Comparing `photondemo-0.0.7/processors/processor.py` & `photondemo-0.0.8/processors/processor.py`

 * *Files identical despite different names*

### Comparing `photondemo-0.0.7/providers/openai.py` & `photondemo-0.0.8/providers/openai.py`

 * *Files identical despite different names*

### Comparing `photondemo-0.0.7/setup.py` & `photondemo-0.0.8/setup.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from setuptools import find_packages, setup
 
-VERSION = "0.0.7"
+VERSION = "0.0.8"
 DESCRIPTION = ""
 LONG_DESCRIPTION = ""
 
 setup(
     name="photondemo",
     version=VERSION,
     author="Charlie Day",
```

