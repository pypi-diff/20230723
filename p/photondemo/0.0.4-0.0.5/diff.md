# Comparing `tmp/photondemo-0.0.4.tar.gz` & `tmp/photondemo-0.0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "photondemo-0.0.4.tar", last modified: Sat Jul 22 18:23:46 2023, max compression
+gzip compressed data, was "photondemo-0.0.5.tar", last modified: Sun Jul 23 19:16:29 2023, max compression
```

## Comparing `photondemo-0.0.4.tar` & `photondemo-0.0.5.tar`

### file list

```diff
@@ -1,16 +1,19 @@
-drwxr-xr-x   0 charlie    (501) staff       (20)        0 2023-07-22 18:23:46.210535 photondemo-0.0.4/
--rw-r--r--   0 charlie    (501) staff       (20)      239 2023-07-22 18:23:46.210211 photondemo-0.0.4/PKG-INFO
-drwxr-xr-x   0 charlie    (501) staff       (20)        0 2023-07-22 18:23:46.204676 photondemo-0.0.4/logger/
--rw-r--r--   0 charlie    (501) staff       (20)        0 2023-07-22 16:45:12.000000 photondemo-0.0.4/logger/__init__.py
--rw-r--r--   0 charlie    (501) staff       (20)      360 2023-07-22 18:23:19.000000 photondemo-0.0.4/logger/logger.py
-drwxr-xr-x   0 charlie    (501) staff       (20)        0 2023-07-22 18:23:46.208766 photondemo-0.0.4/photondemo.egg-info/
--rw-r--r--   0 charlie    (501) staff       (20)      239 2023-07-22 18:23:46.000000 photondemo-0.0.4/photondemo.egg-info/PKG-INFO
--rw-r--r--   0 charlie    (501) staff       (20)      260 2023-07-22 18:23:46.000000 photondemo-0.0.4/photondemo.egg-info/SOURCES.txt
--rw-r--r--   0 charlie    (501) staff       (20)        1 2023-07-22 18:23:46.000000 photondemo-0.0.4/photondemo.egg-info/dependency_links.txt
--rw-r--r--   0 charlie    (501) staff       (20)        9 2023-07-22 18:23:46.000000 photondemo-0.0.4/photondemo.egg-info/requires.txt
--rw-r--r--   0 charlie    (501) staff       (20)       18 2023-07-22 18:23:46.000000 photondemo-0.0.4/photondemo.egg-info/top_level.txt
-drwxr-xr-x   0 charlie    (501) staff       (20)        0 2023-07-22 18:23:46.209663 photondemo-0.0.4/processors/
--rw-r--r--   0 charlie    (501) staff       (20)        0 2023-07-22 15:10:25.000000 photondemo-0.0.4/processors/__init__.py
--rw-r--r--   0 charlie    (501) staff       (20)     1085 2023-07-22 18:22:36.000000 photondemo-0.0.4/processors/processor.py
--rw-r--r--   0 charlie    (501) staff       (20)       38 2023-07-22 18:23:46.210655 photondemo-0.0.4/setup.cfg
--rw-r--r--   0 charlie    (501) staff       (20)      537 2023-07-22 18:23:30.000000 photondemo-0.0.4/setup.py
+drwxr-xr-x   0 charlie    (501) staff       (20)        0 2023-07-23 19:16:29.588650 photondemo-0.0.5/
+-rw-r--r--   0 charlie    (501) staff       (20)      239 2023-07-23 19:16:29.588348 photondemo-0.0.5/PKG-INFO
+drwxr-xr-x   0 charlie    (501) staff       (20)        0 2023-07-23 19:16:29.567655 photondemo-0.0.5/logger/
+-rw-r--r--   0 charlie    (501) staff       (20)        0 2023-07-22 16:45:12.000000 photondemo-0.0.5/logger/__init__.py
+-rw-r--r--   0 charlie    (501) staff       (20)      360 2023-07-22 18:23:19.000000 photondemo-0.0.5/logger/logger.py
+drwxr-xr-x   0 charlie    (501) staff       (20)        0 2023-07-23 19:16:29.585232 photondemo-0.0.5/photondemo.egg-info/
+-rw-r--r--   0 charlie    (501) staff       (20)      239 2023-07-23 19:16:29.000000 photondemo-0.0.5/photondemo.egg-info/PKG-INFO
+-rw-r--r--   0 charlie    (501) staff       (20)      302 2023-07-23 19:16:29.000000 photondemo-0.0.5/photondemo.egg-info/SOURCES.txt
+-rw-r--r--   0 charlie    (501) staff       (20)        1 2023-07-23 19:16:29.000000 photondemo-0.0.5/photondemo.egg-info/dependency_links.txt
+-rw-r--r--   0 charlie    (501) staff       (20)        9 2023-07-23 19:16:29.000000 photondemo-0.0.5/photondemo.egg-info/requires.txt
+-rw-r--r--   0 charlie    (501) staff       (20)       28 2023-07-23 19:16:29.000000 photondemo-0.0.5/photondemo.egg-info/top_level.txt
+drwxr-xr-x   0 charlie    (501) staff       (20)        0 2023-07-23 19:16:29.586204 photondemo-0.0.5/processors/
+-rw-r--r--   0 charlie    (501) staff       (20)        0 2023-07-22 15:10:25.000000 photondemo-0.0.5/processors/__init__.py
+-rw-r--r--   0 charlie    (501) staff       (20)      806 2023-07-23 19:12:29.000000 photondemo-0.0.5/processors/processor.py
+drwxr-xr-x   0 charlie    (501) staff       (20)        0 2023-07-23 19:16:29.587520 photondemo-0.0.5/providers/
+-rw-r--r--   0 charlie    (501) staff       (20)        0 2023-07-23 10:09:19.000000 photondemo-0.0.5/providers/__init__.py
+-rw-r--r--   0 charlie    (501) staff       (20)     1448 2023-07-23 10:14:15.000000 photondemo-0.0.5/providers/openai.py
+-rw-r--r--   0 charlie    (501) staff       (20)       38 2023-07-23 19:16:29.588891 photondemo-0.0.5/setup.cfg
+-rw-r--r--   0 charlie    (501) staff       (20)      537 2023-07-23 19:16:20.000000 photondemo-0.0.5/setup.py
```

### Comparing `photondemo-0.0.4/setup.py` & `photondemo-0.0.5/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from setuptools import find_packages, setup
 
-VERSION = "0.0.4"
+VERSION = "0.0.5"
 DESCRIPTION = ""
 LONG_DESCRIPTION = ""
 
 setup(
     name="photondemo",
     version=VERSION,
     author="Charlie Day",
```

