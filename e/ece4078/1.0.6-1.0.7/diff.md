# Comparing `tmp/ece4078-1.0.6.tar.gz` & `tmp/ece4078-1.0.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ece4078-1.0.6.tar", last modified: Tue Aug  2 03:05:16 2022, max compression
+gzip compressed data, was "ece4078-1.0.7.tar", last modified: Sun Jul 23 04:01:22 2023, max compression
```

## Comparing `ece4078-1.0.6.tar` & `ece4078-1.0.7.tar`

### file list

```diff
@@ -1,23 +1,27 @@
-drwxrwxr-x   0 ttra0024  (1001) ttra0024  (1001)        0 2022-08-02 03:05:16.747373 ece4078-1.0.6/
--rw-rw-r--   0 ttra0024  (1001) ttra0024  (1001)      231 2022-08-02 03:05:16.747373 ece4078-1.0.6/PKG-INFO
--rw-rw-r--   0 ttra0024  (1001) ttra0024  (1001)      431 2022-07-26 04:01:13.000000 ece4078-1.0.6/README.md
--rw-rw-r--   0 ttra0024  (1001) ttra0024  (1001)       38 2022-08-02 03:05:16.747373 ece4078-1.0.6/setup.cfg
--rw-rw-r--   0 ttra0024  (1001) ttra0024  (1001)      457 2022-08-02 03:04:33.000000 ece4078-1.0.6/setup.py
-drwxrwxr-x   0 ttra0024  (1001) ttra0024  (1001)        0 2022-08-02 03:05:16.747373 ece4078-1.0.6/src/
-drwxrwxr-x   0 ttra0024  (1001) ttra0024  (1001)        0 2022-08-02 03:05:16.747373 ece4078-1.0.6/src/ece4078/
--rw-rw-r--   0 ttra0024  (1001) ttra0024  (1001)    10007 2022-08-02 03:04:27.000000 ece4078-1.0.6/src/ece4078/Utility.py
-drwxrwxr-x   0 ttra0024  (1001) ttra0024  (1001)        0 2022-08-02 03:05:16.747373 ece4078-1.0.6/src/ece4078/Week02/
--rw-rw-r--   0 ttra0024  (1001) ttra0024  (1001)     8158 2022-07-26 04:01:13.000000 ece4078-1.0.6/src/ece4078/Week02/Renderer.py
--rw-rw-r--   0 ttra0024  (1001) ttra0024  (1001)       23 2022-07-26 04:01:13.000000 ece4078-1.0.6/src/ece4078/Week02/__init__.py
-drwxrwxr-x   0 ttra0024  (1001) ttra0024  (1001)        0 2022-08-02 03:05:16.747373 ece4078-1.0.6/src/ece4078/Week03/
--rw-rw-r--   0 ttra0024  (1001) ttra0024  (1001)     6082 2022-07-26 04:01:13.000000 ece4078-1.0.6/src/ece4078/Week03/Obstacle.py
--rw-rw-r--   0 ttra0024  (1001) ttra0024  (1001)      107 2022-07-26 04:01:13.000000 ece4078-1.0.6/src/ece4078/Week03/__init__.py
--rw-rw-r--   0 ttra0024  (1001) ttra0024  (1001)     6153 2022-07-26 04:01:13.000000 ece4078-1.0.6/src/ece4078/Week03/math_functions.py
--rw-rw-r--   0 ttra0024  (1001) ttra0024  (1001)     7553 2022-07-26 04:01:13.000000 ece4078-1.0.6/src/ece4078/Week03/path_animation.py
--rw-rw-r--   0 ttra0024  (1001) ttra0024  (1001)     2478 2022-07-26 04:01:13.000000 ece4078-1.0.6/src/ece4078/Week03/path_search.py
--rw-rw-r--   0 ttra0024  (1001) ttra0024  (1001)       22 2022-07-26 04:01:13.000000 ece4078-1.0.6/src/ece4078/__init__.py
-drwxrwxr-x   0 ttra0024  (1001) ttra0024  (1001)        0 2022-08-02 03:05:16.747373 ece4078-1.0.6/src/ece4078.egg-info/
--rw-rw-r--   0 ttra0024  (1001) ttra0024  (1001)      231 2022-08-02 03:05:16.000000 ece4078-1.0.6/src/ece4078.egg-info/PKG-INFO
--rw-rw-r--   0 ttra0024  (1001) ttra0024  (1001)      437 2022-08-02 03:05:16.000000 ece4078-1.0.6/src/ece4078.egg-info/SOURCES.txt
--rw-rw-r--   0 ttra0024  (1001) ttra0024  (1001)        1 2022-08-02 03:05:16.000000 ece4078-1.0.6/src/ece4078.egg-info/dependency_links.txt
--rw-rw-r--   0 ttra0024  (1001) ttra0024  (1001)        8 2022-08-02 03:05:16.000000 ece4078-1.0.6/src/ece4078.egg-info/top_level.txt
+drwxr-xr-x   0 tinsirius  (1000) tinsirius  (1000)        0 2023-07-23 04:01:22.133200 ece4078-1.0.7/
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)     1066 2023-07-23 03:51:35.000000 ece4078-1.0.7/LICENSE
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)      178 2023-07-23 04:01:22.133200 ece4078-1.0.7/PKG-INFO
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)      431 2023-07-23 03:51:35.000000 ece4078-1.0.7/README.md
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)       38 2023-07-23 04:01:22.133200 ece4078-1.0.7/setup.cfg
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)      457 2023-07-23 04:00:42.000000 ece4078-1.0.7/setup.py
+drwxr-xr-x   0 tinsirius  (1000) tinsirius  (1000)        0 2023-07-23 04:01:22.133200 ece4078-1.0.7/src/
+drwxr-xr-x   0 tinsirius  (1000) tinsirius  (1000)        0 2023-07-23 04:01:22.133200 ece4078-1.0.7/src/ece4078/
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)     1751 2023-07-23 04:00:32.000000 ece4078-1.0.7/src/ece4078/NotebookChecker.py
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)    10007 2023-07-23 03:51:35.000000 ece4078-1.0.7/src/ece4078/Utility.py
+drwxr-xr-x   0 tinsirius  (1000) tinsirius  (1000)        0 2023-07-23 04:01:22.133200 ece4078-1.0.7/src/ece4078/Week02/
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)     8158 2023-07-23 03:51:35.000000 ece4078-1.0.7/src/ece4078/Week02/Renderer.py
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)       23 2023-07-23 03:51:35.000000 ece4078-1.0.7/src/ece4078/Week02/__init__.py
+drwxr-xr-x   0 tinsirius  (1000) tinsirius  (1000)        0 2023-07-23 04:01:22.133200 ece4078-1.0.7/src/ece4078/Week03/
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)     6082 2023-07-23 03:51:35.000000 ece4078-1.0.7/src/ece4078/Week03/Obstacle.py
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)      107 2023-07-23 03:51:35.000000 ece4078-1.0.7/src/ece4078/Week03/__init__.py
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)     6153 2023-07-23 03:51:35.000000 ece4078-1.0.7/src/ece4078/Week03/math_functions.py
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)     7553 2023-07-23 03:51:35.000000 ece4078-1.0.7/src/ece4078/Week03/path_animation.py
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)     2478 2023-07-23 03:51:35.000000 ece4078-1.0.7/src/ece4078/Week03/path_search.py
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)       22 2023-07-23 03:51:35.000000 ece4078-1.0.7/src/ece4078/__init__.py
+-rwxr-xr-x   0 tinsirius  (1000) tinsirius  (1000)      869 2023-07-23 03:51:35.000000 ece4078-1.0.7/src/ece4078/install_nginx
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)      597 2023-07-23 03:51:35.000000 ece4078-1.0.7/src/ece4078/nginx-meshcat-proxy.conf
+drwxr-xr-x   0 tinsirius  (1000) tinsirius  (1000)        0 2023-07-23 04:01:22.133200 ece4078-1.0.7/src/ece4078.egg-info/
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)      178 2023-07-23 04:01:22.000000 ece4078-1.0.7/src/ece4078.egg-info/PKG-INFO
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)      539 2023-07-23 04:01:22.000000 ece4078-1.0.7/src/ece4078.egg-info/SOURCES.txt
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)        1 2023-07-23 04:01:22.000000 ece4078-1.0.7/src/ece4078.egg-info/dependency_links.txt
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)        8 2023-07-23 04:01:22.000000 ece4078-1.0.7/src/ece4078.egg-info/top_level.txt
```

### Comparing `ece4078-1.0.6/src/ece4078/Utility.py` & `ece4078-1.0.7/src/ece4078/Utility.py`

 * *Files identical despite different names*

### Comparing `ece4078-1.0.6/src/ece4078/Week02/Renderer.py` & `ece4078-1.0.7/src/ece4078/Week02/Renderer.py`

 * *Files identical despite different names*

### Comparing `ece4078-1.0.6/src/ece4078/Week03/Obstacle.py` & `ece4078-1.0.7/src/ece4078/Week03/Obstacle.py`

 * *Files identical despite different names*

### Comparing `ece4078-1.0.6/src/ece4078/Week03/math_functions.py` & `ece4078-1.0.7/src/ece4078/Week03/math_functions.py`

 * *Files identical despite different names*

### Comparing `ece4078-1.0.6/src/ece4078/Week03/path_animation.py` & `ece4078-1.0.7/src/ece4078/Week03/path_animation.py`

 * *Files identical despite different names*

### Comparing `ece4078-1.0.6/src/ece4078/Week03/path_search.py` & `ece4078-1.0.7/src/ece4078/Week03/path_search.py`

 * *Files identical despite different names*

