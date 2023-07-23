# Comparing `tmp/pymolviz-1.0.1.tar.gz` & `tmp/pymolviz-1.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pymolviz-1.0.1.tar", last modified: Fri Jul 21 08:14:15 2023, max compression
+gzip compressed data, was "pymolviz-1.0.2.tar", last modified: Sun Jul 23 16:12:23 2023, max compression
```

## Comparing `pymolviz-1.0.1.tar` & `pymolviz-1.0.2.tar`

### file list

```diff
@@ -1,17 +1,17 @@
-drwxr-xr-x   0 highgarden  (1000) highgarden  (1000)        0 2023-07-21 08:14:15.250288 pymolviz-1.0.1/
--rw-r--r--   0 highgarden  (1000) highgarden  (1000)      230 2023-07-21 08:14:15.250288 pymolviz-1.0.1/PKG-INFO
-drwxr-xr-x   0 highgarden  (1000) highgarden  (1000)        0 2023-07-21 08:14:15.250288 pymolviz-1.0.1/pymolviz/
--rw-r--r--   0 highgarden  (1000) highgarden  (1000)     7883 2023-07-20 14:22:32.000000 pymolviz-1.0.1/pymolviz/ColorMap.py
--rw-r--r--   0 highgarden  (1000) highgarden  (1000)     1597 2023-07-20 14:22:32.000000 pymolviz-1.0.1/pymolviz/Displayable.py
--rw-r--r--   0 highgarden  (1000) highgarden  (1000)     1865 2023-07-20 14:22:32.000000 pymolviz-1.0.1/pymolviz/Group.py
--rw-r--r--   0 highgarden  (1000) highgarden  (1000)     2014 2023-07-20 14:22:32.000000 pymolviz-1.0.1/pymolviz/Script.py
--rw-r--r--   0 highgarden  (1000) highgarden  (1000)      301 2023-07-20 14:22:32.000000 pymolviz-1.0.1/pymolviz/__init__.py
-drwxr-xr-x   0 highgarden  (1000) highgarden  (1000)        0 2023-07-21 08:14:15.250288 pymolviz-1.0.1/pymolviz.egg-info/
--rw-r--r--   0 highgarden  (1000) highgarden  (1000)      230 2023-07-21 08:14:15.000000 pymolviz-1.0.1/pymolviz.egg-info/PKG-INFO
--rw-r--r--   0 highgarden  (1000) highgarden  (1000)      301 2023-07-21 08:14:15.000000 pymolviz-1.0.1/pymolviz.egg-info/SOURCES.txt
--rw-r--r--   0 highgarden  (1000) highgarden  (1000)        1 2023-07-21 08:14:15.000000 pymolviz-1.0.1/pymolviz.egg-info/dependency_links.txt
--rw-r--r--   0 highgarden  (1000) highgarden  (1000)        1 2023-07-20 14:30:13.000000 pymolviz-1.0.1/pymolviz.egg-info/not-zip-safe
--rw-r--r--   0 highgarden  (1000) highgarden  (1000)       23 2023-07-21 08:14:15.000000 pymolviz-1.0.1/pymolviz.egg-info/requires.txt
--rw-r--r--   0 highgarden  (1000) highgarden  (1000)        9 2023-07-21 08:14:15.000000 pymolviz-1.0.1/pymolviz.egg-info/top_level.txt
--rw-r--r--   0 highgarden  (1000) highgarden  (1000)       38 2023-07-21 08:14:15.250288 pymolviz-1.0.1/setup.cfg
--rw-r--r--   0 highgarden  (1000) highgarden  (1000)      493 2023-07-21 08:14:06.000000 pymolviz-1.0.1/setup.py
+drwxrwxr-x   0 finn      (1000) finn      (1000)        0 2023-07-23 16:12:23.837429 pymolviz-1.0.2/
+-rw-rw-r--   0 finn      (1000) finn      (1000)      230 2023-07-23 16:12:23.837429 pymolviz-1.0.2/PKG-INFO
+drwxrwxr-x   0 finn      (1000) finn      (1000)        0 2023-07-23 16:12:23.833429 pymolviz-1.0.2/pymolviz/
+-rw-rw-r--   0 finn      (1000) finn      (1000)     7883 2023-07-23 16:06:34.000000 pymolviz-1.0.2/pymolviz/ColorMap.py
+-rw-rw-r--   0 finn      (1000) finn      (1000)     1597 2023-07-23 16:06:34.000000 pymolviz-1.0.2/pymolviz/Displayable.py
+-rw-rw-r--   0 finn      (1000) finn      (1000)     1865 2023-07-23 16:06:34.000000 pymolviz-1.0.2/pymolviz/Group.py
+-rw-rw-r--   0 finn      (1000) finn      (1000)     2014 2023-07-23 16:06:34.000000 pymolviz-1.0.2/pymolviz/Script.py
+-rw-rw-r--   0 finn      (1000) finn      (1000)      238 2023-07-23 16:08:18.000000 pymolviz-1.0.2/pymolviz/__init__.py
+drwxrwxr-x   0 finn      (1000) finn      (1000)        0 2023-07-23 16:12:23.837429 pymolviz-1.0.2/pymolviz.egg-info/
+-rw-rw-r--   0 finn      (1000) finn      (1000)      230 2023-07-23 16:12:23.000000 pymolviz-1.0.2/pymolviz.egg-info/PKG-INFO
+-rw-rw-r--   0 finn      (1000) finn      (1000)      301 2023-07-23 16:12:23.000000 pymolviz-1.0.2/pymolviz.egg-info/SOURCES.txt
+-rw-rw-r--   0 finn      (1000) finn      (1000)        1 2023-07-23 16:12:23.000000 pymolviz-1.0.2/pymolviz.egg-info/dependency_links.txt
+-rw-rw-r--   0 finn      (1000) finn      (1000)        1 2023-07-23 16:08:50.000000 pymolviz-1.0.2/pymolviz.egg-info/not-zip-safe
+-rw-rw-r--   0 finn      (1000) finn      (1000)       30 2023-07-23 16:12:23.000000 pymolviz-1.0.2/pymolviz.egg-info/requires.txt
+-rw-rw-r--   0 finn      (1000) finn      (1000)        9 2023-07-23 16:12:23.000000 pymolviz-1.0.2/pymolviz.egg-info/top_level.txt
+-rw-rw-r--   0 finn      (1000) finn      (1000)       38 2023-07-23 16:12:23.837429 pymolviz-1.0.2/setup.cfg
+-rw-rw-r--   0 finn      (1000) finn      (1000)      518 2023-07-23 16:09:52.000000 pymolviz-1.0.2/setup.py
```

### Comparing `pymolviz-1.0.1/pymolviz/ColorMap.py` & `pymolviz-1.0.2/pymolviz/ColorMap.py`

 * *Files identical despite different names*

### Comparing `pymolviz-1.0.1/pymolviz/Displayable.py` & `pymolviz-1.0.2/pymolviz/Displayable.py`

 * *Files identical despite different names*

### Comparing `pymolviz-1.0.1/pymolviz/Group.py` & `pymolviz-1.0.2/pymolviz/Group.py`

 * *Files identical despite different names*

### Comparing `pymolviz-1.0.1/pymolviz/Script.py` & `pymolviz-1.0.2/pymolviz/Script.py`

 * *Files identical despite different names*

