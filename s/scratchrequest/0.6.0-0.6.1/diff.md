# Comparing `tmp/scratchrequest-0.6.0.tar.gz` & `tmp/scratchrequest-0.6.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "scratchrequest-0.6.0.tar", last modified: Mon Jul 17 19:01:43 2023, max compression
+gzip compressed data, was "scratchrequest-0.6.1.tar", last modified: Sun Jul 23 19:19:59 2023, max compression
```

## Comparing `scratchrequest-0.6.0.tar` & `scratchrequest-0.6.1.tar`

### file list

```diff
@@ -1,19 +1,20 @@
-drwxrwxrwx   0        0        0        0 2023-07-17 19:01:43.185363 scratchrequest-0.6.0/
--rw-rw-rw-   0        0        0     1091 2023-07-06 16:37:14.000000 scratchrequest-0.6.0/LICENSE
--rw-rw-rw-   0        0        0      724 2023-07-17 19:01:43.180362 scratchrequest-0.6.0/PKG-INFO
--rw-rw-rw-   0        0        0        2 2023-07-06 16:23:32.000000 scratchrequest-0.6.0/README.md
-drwxrwxrwx   0        0        0        0 2023-07-17 19:01:43.099361 scratchrequest-0.6.0/scratchrequest/
--rw-rw-rw-   0        0        0      158 2023-07-03 18:02:47.000000 scratchrequest-0.6.0/scratchrequest/__init__.py
--rw-rw-rw-   0        0        0     9912 2023-07-03 16:44:51.000000 scratchrequest-0.6.0/scratchrequest/_cloud.py
--rw-rw-rw-   0        0        0      322 2023-07-17 09:03:00.000000 scratchrequest-0.6.0/scratchrequest/_exceptions.py
--rw-rw-rw-   0        0        0     1946 2023-07-17 10:39:16.000000 scratchrequest-0.6.0/scratchrequest/_project.py
--rw-rw-rw-   0        0        0     3798 2023-07-17 10:39:49.000000 scratchrequest-0.6.0/scratchrequest/_session.py
--rw-rw-rw-   0        0        0     2974 2023-07-03 18:36:49.000000 scratchrequest-0.6.0/scratchrequest/_twcloud.py
-drwxrwxrwx   0        0        0        0 2023-07-17 19:01:43.170366 scratchrequest-0.6.0/scratchrequest.egg-info/
--rw-rw-rw-   0        0        0      724 2023-07-17 19:01:42.000000 scratchrequest-0.6.0/scratchrequest.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      378 2023-07-17 19:01:42.000000 scratchrequest-0.6.0/scratchrequest.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-17 19:01:42.000000 scratchrequest-0.6.0/scratchrequest.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       26 2023-07-17 19:01:42.000000 scratchrequest-0.6.0/scratchrequest.egg-info/requires.txt
--rw-rw-rw-   0        0        0       15 2023-07-17 19:01:42.000000 scratchrequest-0.6.0/scratchrequest.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-17 19:01:43.187365 scratchrequest-0.6.0/setup.cfg
--rw-rw-rw-   0        0        0     1081 2023-07-17 19:00:12.000000 scratchrequest-0.6.0/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 19:19:59.438681 scratchrequest-0.6.1/
+-rw-rw-rw-   0        0        0     1091 2023-07-06 16:37:14.000000 scratchrequest-0.6.1/LICENSE
+-rw-rw-rw-   0        0        0      724 2023-07-23 19:19:59.393684 scratchrequest-0.6.1/PKG-INFO
+-rw-rw-rw-   0        0        0        2 2023-07-06 16:23:32.000000 scratchrequest-0.6.1/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 19:19:59.199682 scratchrequest-0.6.1/scratchrequest/
+-rw-rw-rw-   0        0        0      250 2023-07-17 18:12:20.000000 scratchrequest-0.6.1/scratchrequest/__init__.py
+-rw-rw-rw-   0        0        0     9912 2023-07-03 16:44:51.000000 scratchrequest-0.6.1/scratchrequest/_cloud.py
+-rw-rw-rw-   0        0        0      366 2023-07-23 15:23:53.000000 scratchrequest-0.6.1/scratchrequest/_exceptions.py
+-rw-rw-rw-   0        0        0     4544 2023-07-23 19:04:50.000000 scratchrequest-0.6.1/scratchrequest/_project.py
+-rw-rw-rw-   0        0        0     4015 2023-07-17 18:39:59.000000 scratchrequest-0.6.1/scratchrequest/_session.py
+-rw-rw-rw-   0        0        0     2012 2023-07-17 18:47:13.000000 scratchrequest-0.6.1/scratchrequest/_settings.py
+-rw-rw-rw-   0        0        0     2974 2023-07-03 18:36:49.000000 scratchrequest-0.6.1/scratchrequest/_twcloud.py
+drwxrwxrwx   0        0        0        0 2023-07-23 19:19:59.386685 scratchrequest-0.6.1/scratchrequest.egg-info/
+-rw-rw-rw-   0        0        0      724 2023-07-23 19:19:58.000000 scratchrequest-0.6.1/scratchrequest.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      406 2023-07-23 19:19:58.000000 scratchrequest-0.6.1/scratchrequest.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 19:19:58.000000 scratchrequest-0.6.1/scratchrequest.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       26 2023-07-23 19:19:58.000000 scratchrequest-0.6.1/scratchrequest.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       15 2023-07-23 19:19:58.000000 scratchrequest-0.6.1/scratchrequest.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 19:19:59.439687 scratchrequest-0.6.1/setup.cfg
+-rw-rw-rw-   0        0        0     1081 2023-07-23 19:14:35.000000 scratchrequest-0.6.1/setup.py
```

### Comparing `scratchrequest-0.6.0/LICENSE` & `scratchrequest-0.6.1/LICENSE`

 * *Files identical despite different names*

### Comparing `scratchrequest-0.6.0/PKG-INFO` & `scratchrequest-0.6.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: scratchrequest
-Version: 0.6.0
+Version: 0.6.1
 Summary: An Scratch API Wrapper for scratch.mit.edu
 Home-page: https://github.com/programordie2/scratchrequest
 Author: programORdie
 Author-email: 
 Keywords: scratch api,scratchrequest,scratch api python,scratch python,scratch for python,scratch,scratch cloud,scratch cloud variables,scratch bot
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Developers
```

### Comparing `scratchrequest-0.6.0/scratchrequest/_cloud.py` & `scratchrequest-0.6.1/scratchrequest/_cloud.py`

 * *Files identical despite different names*

### Comparing `scratchrequest-0.6.0/scratchrequest/_session.py` & `scratchrequest-0.6.1/scratchrequest/_session.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 import warnings
 from ._exceptions import LoginError
 from . import _cloud
 from . import _project
+from . import _settings
 import requests, json, re
 
 headers = {
     "user-agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/75.0.3770.142 Safari/537.36",
     "x-csrftoken": "a",
     "x-requested-with": "XMLHttpRequest",
     "referer": "https://scratch.mit.edu",
@@ -85,7 +86,13 @@
         return _cloud.CreateCloudConnection(project_id=project_id, session=self, **kwargs)
 
     def ConnectProject(self, id : int) -> _project.CreateConnectProject:
         '''
         Create a connection to a project.
         '''
         return _project.CreateConnectProject(id=id, session=self)
+
+    def ManageSettings(self) -> _settings.ManageSettings:
+        '''
+        Makes it possible to edit your settings.
+        '''
+        return _settings.ManageSettings(session=self)
```

### Comparing `scratchrequest-0.6.0/scratchrequest/_twcloud.py` & `scratchrequest-0.6.1/scratchrequest/_twcloud.py`

 * *Files identical despite different names*

### Comparing `scratchrequest-0.6.0/scratchrequest.egg-info/PKG-INFO` & `scratchrequest-0.6.1/scratchrequest.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: scratchrequest
-Version: 0.6.0
+Version: 0.6.1
 Summary: An Scratch API Wrapper for scratch.mit.edu
 Home-page: https://github.com/programordie2/scratchrequest
 Author: programORdie
 Author-email: 
 Keywords: scratch api,scratchrequest,scratch api python,scratch python,scratch for python,scratch,scratch cloud,scratch cloud variables,scratch bot
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Developers
```

### Comparing `scratchrequest-0.6.0/setup.py` & `scratchrequest-0.6.1/setup.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 import codecs
 import os
 
-VERSION = '0.6.0'
+VERSION = '0.6.1'
 DESCRIPTION = 'An Scratch API Wrapper for scratch.mit.edu'
 LONG_DESCRIPTION = DESCRIPTION
 
 # Setting up
 setup(
     name="scratchrequest",
     version=VERSION,
```

