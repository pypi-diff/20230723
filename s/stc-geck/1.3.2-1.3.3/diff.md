# Comparing `tmp/stc-geck-1.3.2.tar.gz` & `tmp/stc-geck-1.3.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "stc-geck-1.3.2.tar", last modified: Sun Jul 23 16:40:12 2023, max compression
+gzip compressed data, was "stc-geck-1.3.3.tar", last modified: Sun Jul 23 16:44:26 2023, max compression
```

## Comparing `stc-geck-1.3.2.tar` & `stc-geck-1.3.3.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxr-xr-x   0 pasha      (501) staff       (20)        0 2023-07-23 16:40:12.474511 stc-geck-1.3.2/
--rw-r--r--   0 pasha      (501) staff       (20)       24 2022-12-01 11:19:40.000000 stc-geck-1.3.2/MANIFEST.in
--rw-r--r--   0 pasha      (501) staff       (20)     1033 2023-07-23 16:40:12.473872 stc-geck-1.3.2/PKG-INFO
--rw-r--r--   0 pasha      (501) staff       (20)      688 2023-07-22 19:34:42.000000 stc-geck-1.3.2/README.md
--rw-r--r--   0 pasha      (501) staff       (20)      600 2023-07-22 19:20:49.000000 stc-geck-1.3.2/pyproject.toml
--rw-r--r--   0 pasha      (501) staff       (20)      161 2023-07-20 13:58:38.000000 stc-geck-1.3.2/requirements.txt
--rw-r--r--   0 pasha      (501) staff       (20)       38 2023-07-23 16:40:12.474828 stc-geck-1.3.2/setup.cfg
-drwxr-xr-x   0 pasha      (501) staff       (20)        0 2023-07-23 16:40:12.467378 stc-geck-1.3.2/stc_geck/
--rw-r--r--   0 pasha      (501) staff       (20)        0 2023-07-19 19:56:31.000000 stc-geck-1.3.2/stc_geck/__init__.py
--rw-r--r--   0 pasha      (501) staff       (20)      923 2023-07-06 11:45:56.000000 stc-geck-1.3.2/stc_geck/advices.py
--rw-r--r--   0 pasha      (501) staff       (20)     7344 2023-07-22 18:20:45.000000 stc-geck-1.3.2/stc_geck/cli.py
--rw-r--r--   0 pasha      (501) staff       (20)     7229 2023-07-22 08:15:51.000000 stc-geck-1.3.2/stc_geck/client.py
--rw-r--r--   0 pasha      (501) staff       (20)     1877 2023-07-22 08:16:03.000000 stc-geck-1.3.2/stc_geck/utils.py
-drwxr-xr-x   0 pasha      (501) staff       (20)        0 2023-07-23 16:40:12.472698 stc-geck-1.3.2/stc_geck.egg-info/
--rw-r--r--   0 pasha      (501) staff       (20)     1033 2023-07-23 16:40:12.000000 stc-geck-1.3.2/stc_geck.egg-info/PKG-INFO
--rw-r--r--   0 pasha      (501) staff       (20)      341 2023-07-23 16:40:12.000000 stc-geck-1.3.2/stc_geck.egg-info/SOURCES.txt
--rw-r--r--   0 pasha      (501) staff       (20)        1 2023-07-23 16:40:12.000000 stc-geck-1.3.2/stc_geck.egg-info/dependency_links.txt
--rw-r--r--   0 pasha      (501) staff       (20)       43 2023-07-23 16:40:12.000000 stc-geck-1.3.2/stc_geck.egg-info/entry_points.txt
--rw-r--r--   0 pasha      (501) staff       (20)      162 2023-07-23 16:40:12.000000 stc-geck-1.3.2/stc_geck.egg-info/requires.txt
--rw-r--r--   0 pasha      (501) staff       (20)        9 2023-07-23 16:40:12.000000 stc-geck-1.3.2/stc_geck.egg-info/top_level.txt
+drwxr-xr-x   0 pasha      (501) staff       (20)        0 2023-07-23 16:44:26.322884 stc-geck-1.3.3/
+-rw-r--r--   0 pasha      (501) staff       (20)       24 2022-12-01 11:19:40.000000 stc-geck-1.3.3/MANIFEST.in
+-rw-r--r--   0 pasha      (501) staff       (20)     1033 2023-07-23 16:44:26.321935 stc-geck-1.3.3/PKG-INFO
+-rw-r--r--   0 pasha      (501) staff       (20)      688 2023-07-22 19:34:42.000000 stc-geck-1.3.3/README.md
+-rw-r--r--   0 pasha      (501) staff       (20)      600 2023-07-23 16:43:55.000000 stc-geck-1.3.3/pyproject.toml
+-rw-r--r--   0 pasha      (501) staff       (20)      161 2023-07-20 13:58:38.000000 stc-geck-1.3.3/requirements.txt
+-rw-r--r--   0 pasha      (501) staff       (20)       38 2023-07-23 16:44:26.323155 stc-geck-1.3.3/setup.cfg
+drwxr-xr-x   0 pasha      (501) staff       (20)        0 2023-07-23 16:44:26.315554 stc-geck-1.3.3/stc_geck/
+-rw-r--r--   0 pasha      (501) staff       (20)        0 2023-07-19 19:56:31.000000 stc-geck-1.3.3/stc_geck/__init__.py
+-rw-r--r--   0 pasha      (501) staff       (20)      923 2023-07-06 11:45:56.000000 stc-geck-1.3.3/stc_geck/advices.py
+-rw-r--r--   0 pasha      (501) staff       (20)     7346 2023-07-23 16:43:55.000000 stc-geck-1.3.3/stc_geck/cli.py
+-rw-r--r--   0 pasha      (501) staff       (20)     7231 2023-07-23 16:43:55.000000 stc-geck-1.3.3/stc_geck/client.py
+-rw-r--r--   0 pasha      (501) staff       (20)     1877 2023-07-22 08:16:03.000000 stc-geck-1.3.3/stc_geck/utils.py
+drwxr-xr-x   0 pasha      (501) staff       (20)        0 2023-07-23 16:44:26.320711 stc-geck-1.3.3/stc_geck.egg-info/
+-rw-r--r--   0 pasha      (501) staff       (20)     1033 2023-07-23 16:44:26.000000 stc-geck-1.3.3/stc_geck.egg-info/PKG-INFO
+-rw-r--r--   0 pasha      (501) staff       (20)      341 2023-07-23 16:44:26.000000 stc-geck-1.3.3/stc_geck.egg-info/SOURCES.txt
+-rw-r--r--   0 pasha      (501) staff       (20)        1 2023-07-23 16:44:26.000000 stc-geck-1.3.3/stc_geck.egg-info/dependency_links.txt
+-rw-r--r--   0 pasha      (501) staff       (20)       43 2023-07-23 16:44:26.000000 stc-geck-1.3.3/stc_geck.egg-info/entry_points.txt
+-rw-r--r--   0 pasha      (501) staff       (20)      162 2023-07-23 16:44:26.000000 stc-geck-1.3.3/stc_geck.egg-info/requires.txt
+-rw-r--r--   0 pasha      (501) staff       (20)        9 2023-07-23 16:44:26.000000 stc-geck-1.3.3/stc_geck.egg-info/top_level.txt
```

### Comparing `stc-geck-1.3.2/PKG-INFO` & `stc-geck-1.3.3/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: stc-geck
-Version: 1.3.2
+Version: 1.3.3
 Summary: GECK (Garden Of Eden Creation Kit) is a toolkit for setting up and maintaning STC
 Author: Interdimensional Walker
 Project-URL: Homepage, https://github.com/nexus-stc/stc
 Classifier: Programming Language :: Python :: 3.8
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
```

### Comparing `stc-geck-1.3.2/README.md` & `stc-geck-1.3.3/README.md`

 * *Files identical despite different names*

### Comparing `stc-geck-1.3.2/pyproject.toml` & `stc-geck-1.3.3/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools<65.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "stc-geck"
-version = "1.3.2"
+version = "1.3.3"
 authors = [{ name = "Interdimensional Walker" }]
 description = "GECK (Garden Of Eden Creation Kit) is a toolkit for setting up and maintaning STC"
 readme = "README.md"
 requires-python = ">=3.8"
 classifiers = [
     "Programming Language :: Python :: 3.8",
 ]
```

### Comparing `stc-geck-1.3.2/stc_geck/advices.py` & `stc-geck-1.3.3/stc_geck/advices.py`

 * *Files identical despite different names*

### Comparing `stc-geck-1.3.2/stc_geck/cli.py` & `stc-geck-1.3.3/stc_geck/cli.py`

 * *Files 0% similar despite different names*

```diff
@@ -4,17 +4,18 @@
 import logging
 import os.path
 import sys
 from typing import Optional
 
 import fire
 import humanfriendly
-from client import StcGeck
 from termcolor import colored
 
+from .client import StcGeck
+
 
 class ItemNotFound(Exception):
     def __init__(self, query):
         self.query = query
 
     def __str__(self):
         return f'ItemNotFound(query="{self.query}")'
```

### Comparing `stc-geck-1.3.2/stc_geck/client.py` & `stc-geck-1.3.3/stc_geck/client.py`

 * *Files 1% similar despite different names*

```diff
@@ -8,15 +8,16 @@
 import aiohttp
 import orjson
 import summa_embed
 from aiokit import AioThing
 from aiosumma import SummaClient
 from izihawa_ipfs_api import IpfsApiClient, IpfsHttpClient
 from izihawa_utils.random import reservoir_sampling_async
-from utils import create_car, is_endpoint_listening
+
+from .utils import create_car, is_endpoint_listening
 
 
 def get_config():
     return {
         'debug': True,
         'api': {
             'http_endpoint': None,
```

### Comparing `stc-geck-1.3.2/stc_geck/utils.py` & `stc-geck-1.3.3/stc_geck/utils.py`

 * *Files identical despite different names*

### Comparing `stc-geck-1.3.2/stc_geck.egg-info/PKG-INFO` & `stc-geck-1.3.3/stc_geck.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: stc-geck
-Version: 1.3.2
+Version: 1.3.3
 Summary: GECK (Garden Of Eden Creation Kit) is a toolkit for setting up and maintaning STC
 Author: Interdimensional Walker
 Project-URL: Homepage, https://github.com/nexus-stc/stc
 Classifier: Programming Language :: Python :: 3.8
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
```

