# Comparing `tmp/LordXen-0.0.0.2.tar.gz` & `tmp/LordXen-2023.7.23.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "LordXen-0.0.0.2.tar", last modified: Sun Oct 23 20:17:52 2022, max compression
+gzip compressed data, was "LordXen-2023.7.23.tar", last modified: Sun Jul 23 15:03:54 2023, max compression
```

## Comparing `LordXen-0.0.0.2.tar` & `LordXen-2023.7.23.tar`

### file list

```diff
@@ -1,15 +1,13 @@
-drwxr-xr-x   0 philippkitzmuller   (501) staff       (20)        0 2022-10-23 20:17:52.178824 LordXen-0.0.0.2/
-drwxr-xr-x   0 philippkitzmuller   (501) staff       (20)        0 2022-10-23 20:17:52.177701 LordXen-0.0.0.2/LordXen/
--rw-r--r--   0 philippkitzmuller   (501) staff       (20)     5631 2022-10-23 20:06:12.000000 LordXen-0.0.0.2/LordXen/__init__.py
--rw-r--r--   0 philippkitzmuller   (501) staff       (20)     1048 2022-10-23 20:06:12.000000 LordXen-0.0.0.2/LordXen/exceptions.py
-drwxr-xr-x   0 philippkitzmuller   (501) staff       (20)        0 2022-10-23 20:17:52.178549 LordXen-0.0.0.2/LordXen.egg-info/
--rw-r--r--   0 philippkitzmuller   (501) staff       (20)     1610 2022-10-23 20:17:52.000000 LordXen-0.0.0.2/LordXen.egg-info/PKG-INFO
--rw-r--r--   0 philippkitzmuller   (501) staff       (20)      245 2022-10-23 20:17:52.000000 LordXen-0.0.0.2/LordXen.egg-info/SOURCES.txt
--rw-r--r--   0 philippkitzmuller   (501) staff       (20)        1 2022-10-23 20:17:52.000000 LordXen-0.0.0.2/LordXen.egg-info/dependency_links.txt
--rw-r--r--   0 philippkitzmuller   (501) staff       (20)        1 2022-10-23 20:10:36.000000 LordXen-0.0.0.2/LordXen.egg-info/not-zip-safe
--rw-r--r--   0 philippkitzmuller   (501) staff       (20)        9 2022-10-23 20:17:52.000000 LordXen-0.0.0.2/LordXen.egg-info/requires.txt
--rw-r--r--   0 philippkitzmuller   (501) staff       (20)        8 2022-10-23 20:17:52.000000 LordXen-0.0.0.2/LordXen.egg-info/top_level.txt
--rw-r--r--   0 philippkitzmuller   (501) staff       (20)     1610 2022-10-23 20:17:52.178702 LordXen-0.0.0.2/PKG-INFO
--rw-r--r--   0 philippkitzmuller   (501) staff       (20)     1029 2022-10-23 20:14:16.000000 LordXen-0.0.0.2/README.rst
--rw-r--r--   0 philippkitzmuller   (501) staff       (20)       38 2022-10-23 20:17:52.178854 LordXen-0.0.0.2/setup.cfg
--rw-r--r--   0 philippkitzmuller   (501) staff       (20)      922 2022-10-23 20:17:34.000000 LordXen-0.0.0.2/setup.py
+drwxr-xr-x   0 philippkitzmuller   (501) staff       (20)        0 2023-07-23 15:03:54.811984 LordXen-2023.7.23/
+drwxr-xr-x   0 philippkitzmuller   (501) staff       (20)        0 2023-07-23 15:03:54.810569 LordXen-2023.7.23/LordXen/
+-rw-r--r--   0 philippkitzmuller   (501) staff       (20)     5677 2023-07-23 15:00:57.000000 LordXen-2023.7.23/LordXen/__init__.py
+-rw-r--r--   0 philippkitzmuller   (501) staff       (20)     1048 2023-07-14 17:51:34.000000 LordXen-2023.7.23/LordXen/exceptions.py
+drwxr-xr-x   0 philippkitzmuller   (501) staff       (20)        0 2023-07-23 15:03:54.811601 LordXen-2023.7.23/LordXen.egg-info/
+-rw-r--r--   0 philippkitzmuller   (501) staff       (20)     1409 2023-07-23 15:03:54.000000 LordXen-2023.7.23/LordXen.egg-info/PKG-INFO
+-rw-r--r--   0 philippkitzmuller   (501) staff       (20)      191 2023-07-23 15:03:54.000000 LordXen-2023.7.23/LordXen.egg-info/SOURCES.txt
+-rw-r--r--   0 philippkitzmuller   (501) staff       (20)        1 2023-07-23 15:03:54.000000 LordXen-2023.7.23/LordXen.egg-info/dependency_links.txt
+-rw-r--r--   0 philippkitzmuller   (501) staff       (20)        8 2023-07-23 15:03:54.000000 LordXen-2023.7.23/LordXen.egg-info/top_level.txt
+-rw-r--r--   0 philippkitzmuller   (501) staff       (20)     1409 2023-07-23 15:03:54.811825 LordXen-2023.7.23/PKG-INFO
+-rw-r--r--   0 philippkitzmuller   (501) staff       (20)     1029 2023-07-14 17:51:34.000000 LordXen-2023.7.23/README.rst
+-rw-r--r--   0 philippkitzmuller   (501) staff       (20)      460 2023-07-23 15:03:50.000000 LordXen-2023.7.23/pyproject.toml
+-rw-r--r--   0 philippkitzmuller   (501) staff       (20)       38 2023-07-23 15:03:54.812029 LordXen-2023.7.23/setup.cfg
```

### Comparing `LordXen-0.0.0.2/LordXen/__init__.py` & `LordXen-2023.7.23/LordXen/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,16 @@
 
-import requests
+import cloudscraper
 from requests.auth import HTTPBasicAuth
-
 from LordXen.exceptions import *
 
 
+requests = cloudscraper.create_scraper()
+
+
 class XenThread:
     def __init__(self, xforo, thread_id, title=None, tags=None, prefix_id=None, prefix=None):
         xforo: XenForo
         self.xforo = xforo
         self.thread_id = thread_id
         self.title = title
         self.tags = tags
```

### Comparing `LordXen-0.0.0.2/LordXen/exceptions.py` & `LordXen-2023.7.23/LordXen/exceptions.py`

 * *Files identical despite different names*

### Comparing `LordXen-0.0.0.2/LordXen.egg-info/PKG-INFO` & `LordXen-2023.7.23/LordXen.egg-info/PKG-INFO`

 * *Files 23% similar despite different names*

```diff
@@ -1,23 +1,17 @@
 Metadata-Version: 2.1
 Name: LordXen
-Version: 0.0.0.2
-Summary: Python XenForo Api lib
-Home-page: https://github.com/LordBex/LordXen
-Author: lordbex
-Author-email: lordibex@protonmail.com
-License: UNKNOWN
-Platform: any
-Classifier: Environment :: Web Environment
-Classifier: Intended Audience :: Developers
-Classifier: Operating System :: OS Independent
-Classifier: Programming Language :: Python
-Classifier: Programming Language :: Python :: 3.10
-Classifier: Topic :: Internet :: WWW/HTTP :: Dynamic Content
-Classifier: Topic :: Software Development :: Libraries :: Python Modules
+Version: 2023.7.23
+Summary: Python XenForo Api Lib für Posten 
+Author-email: lordbex <lordibex@protonmail.com>
+Maintainer-email: lordbex <lordibex@protonmail.com>
+Project-URL: homepage, https://github.com/LordBex/LordXen
+Project-URL: repository, https://github.com/LordBex/LordXen
+Requires-Python: >=3.10
+Description-Content-Type: text/x-rst
 
 Python XenForo Api
 ==================
 
 ! PRE-VERSION !
 
 Python Lib für die XenForo api
@@ -68,9 +62,7 @@
   Thread with id 800 exist
   Thread with id 17291 edited!
   Created post for 17291
 
 
 *by LordBex*
 
-
-
```

### Comparing `LordXen-0.0.0.2/PKG-INFO` & `LordXen-2023.7.23/PKG-INFO`

 * *Files 23% similar despite different names*

```diff
@@ -1,23 +1,17 @@
 Metadata-Version: 2.1
 Name: LordXen
-Version: 0.0.0.2
-Summary: Python XenForo Api lib
-Home-page: https://github.com/LordBex/LordXen
-Author: lordbex
-Author-email: lordibex@protonmail.com
-License: UNKNOWN
-Platform: any
-Classifier: Environment :: Web Environment
-Classifier: Intended Audience :: Developers
-Classifier: Operating System :: OS Independent
-Classifier: Programming Language :: Python
-Classifier: Programming Language :: Python :: 3.10
-Classifier: Topic :: Internet :: WWW/HTTP :: Dynamic Content
-Classifier: Topic :: Software Development :: Libraries :: Python Modules
+Version: 2023.7.23
+Summary: Python XenForo Api Lib für Posten 
+Author-email: lordbex <lordibex@protonmail.com>
+Maintainer-email: lordbex <lordibex@protonmail.com>
+Project-URL: homepage, https://github.com/LordBex/LordXen
+Project-URL: repository, https://github.com/LordBex/LordXen
+Requires-Python: >=3.10
+Description-Content-Type: text/x-rst
 
 Python XenForo Api
 ==================
 
 ! PRE-VERSION !
 
 Python Lib für die XenForo api
@@ -68,9 +62,7 @@
   Thread with id 800 exist
   Thread with id 17291 edited!
   Created post for 17291
 
 
 *by LordBex*
 
-
-
```

### Comparing `LordXen-0.0.0.2/README.rst` & `LordXen-2023.7.23/README.rst`

 * *Files identical despite different names*

