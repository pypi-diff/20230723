# Comparing `tmp/rubpy-6.3.2.tar.gz` & `tmp/rubpy-6.3.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "rubpy-6.3.2.tar", last modified: Sun Jul 23 18:20:35 2023, max compression
+gzip compressed data, was "rubpy-6.3.3.tar", last modified: Sun Jul 23 18:24:39 2023, max compression
```

## Comparing `rubpy-6.3.2.tar` & `rubpy-6.3.3.tar`

### file list

```diff
@@ -1,38 +1,38 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 18:20:35.926236 rubpy-6.3.2/
--rw-rw-rw-   0        0        0     3378 2023-07-23 18:20:35.926236 rubpy-6.3.2/PKG-INFO
--rw-rw-rw-   0        0        0     2238 2023-04-26 17:35:11.000000 rubpy-6.3.2/README.md
-drwxrwxrwx   0        0        0        0 2023-07-23 18:20:35.875981 rubpy-6.3.2/rubpy/
--rw-rw-rw-   0        0        0      240 2023-07-23 18:19:36.000000 rubpy-6.3.2/rubpy/__init__.py
--rw-rw-rw-   0        0        0    43761 2023-07-23 18:19:04.000000 rubpy-6.3.2/rubpy/client.py
-drwxrwxrwx   0        0        0        0 2023-07-23 18:20:35.905907 rubpy-6.3.2/rubpy/crypto/
--rw-rw-rw-   0        0        0       26 2022-09-12 11:03:20.000000 rubpy-6.3.2/rubpy/crypto/__init__.py
--rw-rw-rw-   0        0        0     3288 2023-07-19 15:43:06.000000 rubpy-6.3.2/rubpy/crypto/crypto.py
-drwxrwxrwx   0        0        0        0 2023-07-23 18:20:35.919729 rubpy-6.3.2/rubpy/gadgets/
--rw-rw-rw-   0        0        0      106 2022-09-12 11:03:20.000000 rubpy-6.3.2/rubpy/gadgets/__init__.py
--rw-rw-rw-   0        0        0      892 2023-06-14 19:16:37.000000 rubpy-6.3.2/rubpy/gadgets/classino.py
--rw-rw-rw-   0        0        0     2118 2023-04-26 18:12:01.000000 rubpy-6.3.2/rubpy/gadgets/exceptions.py
--rw-rw-rw-   0        0        0    27137 2023-06-15 19:36:00.000000 rubpy-6.3.2/rubpy/gadgets/grouping.py
--rw-rw-rw-   0        0        0    14188 2023-04-26 17:30:17.000000 rubpy-6.3.2/rubpy/gadgets/methods.py
--rw-rw-rw-   0        0        0     6772 2023-06-29 12:36:38.000000 rubpy-6.3.2/rubpy/gadgets/thumbnail.py
-drwxrwxrwx   0        0        0        0 2023-07-23 18:20:35.926236 rubpy-6.3.2/rubpy/network/
--rw-rw-rw-   0        0        0       64 2022-09-12 11:03:20.000000 rubpy-6.3.2/rubpy/network/__init__.py
--rw-rw-rw-   0        0        0    12184 2023-07-20 09:50:47.000000 rubpy-6.3.2/rubpy/network/connection.py
--rw-rw-rw-   0        0        0    14807 2022-09-12 11:03:20.000000 rubpy-6.3.2/rubpy/network/proxies.py
-drwxrwxrwx   0        0        0        0 2023-07-23 18:20:35.926236 rubpy-6.3.2/rubpy/sessions/
--rw-rw-rw-   0        0        0       82 2022-09-12 11:03:20.000000 rubpy-6.3.2/rubpy/sessions/__init__.py
--rw-rw-rw-   0        0        0     2295 2023-06-14 11:13:33.000000 rubpy-6.3.2/rubpy/sessions/sqliteSession.py
--rw-rw-rw-   0        0        0     1223 2022-09-12 11:03:20.000000 rubpy-6.3.2/rubpy/sessions/stringSession.py
-drwxrwxrwx   0        0        0        0 2023-07-23 18:20:35.926236 rubpy-6.3.2/rubpy/structs/
--rw-rw-rw-   0        0        0       99 2022-09-12 11:03:20.000000 rubpy-6.3.2/rubpy/structs/__init__.py
--rw-rw-rw-   0        0        0     1985 2022-09-12 11:03:20.000000 rubpy-6.3.2/rubpy/structs/handlers.py
--rw-rw-rw-   0        0        0     4585 2022-09-12 11:03:20.000000 rubpy-6.3.2/rubpy/structs/models.py
--rw-rw-rw-   0        0        0      702 2022-09-12 11:03:20.000000 rubpy-6.3.2/rubpy/structs/results.py
--rw-rw-rw-   0        0        0    15140 2023-04-23 17:55:22.000000 rubpy-6.3.2/rubpy/structs/struct.py
-drwxrwxrwx   0        0        0        0 2023-07-23 18:20:35.905907 rubpy-6.3.2/rubpy.egg-info/
--rw-rw-rw-   0        0        0     3378 2023-07-23 18:20:35.000000 rubpy-6.3.2/rubpy.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      697 2023-07-23 18:20:35.000000 rubpy-6.3.2/rubpy.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 18:20:35.000000 rubpy-6.3.2/rubpy.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       69 2023-07-23 18:20:35.000000 rubpy-6.3.2/rubpy.egg-info/requires.txt
--rw-rw-rw-   0        0        0        6 2023-07-23 18:20:35.000000 rubpy-6.3.2/rubpy.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-23 18:20:35.926236 rubpy-6.3.2/setup.cfg
--rw-rw-rw-   0        0        0     1558 2023-07-23 18:20:09.000000 rubpy-6.3.2/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 18:24:39.513049 rubpy-6.3.3/
+-rw-rw-rw-   0        0        0     3378 2023-07-23 18:24:39.513049 rubpy-6.3.3/PKG-INFO
+-rw-rw-rw-   0        0        0     2238 2023-04-26 17:35:11.000000 rubpy-6.3.3/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 18:24:39.482566 rubpy-6.3.3/rubpy/
+-rw-rw-rw-   0        0        0      240 2023-07-23 18:24:12.000000 rubpy-6.3.3/rubpy/__init__.py
+-rw-rw-rw-   0        0        0    43769 2023-07-23 18:24:23.000000 rubpy-6.3.3/rubpy/client.py
+drwxrwxrwx   0        0        0        0 2023-07-23 18:24:39.503022 rubpy-6.3.3/rubpy/crypto/
+-rw-rw-rw-   0        0        0       26 2022-09-12 11:03:20.000000 rubpy-6.3.3/rubpy/crypto/__init__.py
+-rw-rw-rw-   0        0        0     3288 2023-07-19 15:43:06.000000 rubpy-6.3.3/rubpy/crypto/crypto.py
+drwxrwxrwx   0        0        0        0 2023-07-23 18:24:39.510040 rubpy-6.3.3/rubpy/gadgets/
+-rw-rw-rw-   0        0        0      106 2022-09-12 11:03:20.000000 rubpy-6.3.3/rubpy/gadgets/__init__.py
+-rw-rw-rw-   0        0        0      892 2023-06-14 19:16:37.000000 rubpy-6.3.3/rubpy/gadgets/classino.py
+-rw-rw-rw-   0        0        0     2118 2023-04-26 18:12:01.000000 rubpy-6.3.3/rubpy/gadgets/exceptions.py
+-rw-rw-rw-   0        0        0    27137 2023-06-15 19:36:00.000000 rubpy-6.3.3/rubpy/gadgets/grouping.py
+-rw-rw-rw-   0        0        0    14188 2023-04-26 17:30:17.000000 rubpy-6.3.3/rubpy/gadgets/methods.py
+-rw-rw-rw-   0        0        0     6772 2023-06-29 12:36:38.000000 rubpy-6.3.3/rubpy/gadgets/thumbnail.py
+drwxrwxrwx   0        0        0        0 2023-07-23 18:24:39.513049 rubpy-6.3.3/rubpy/network/
+-rw-rw-rw-   0        0        0       64 2022-09-12 11:03:20.000000 rubpy-6.3.3/rubpy/network/__init__.py
+-rw-rw-rw-   0        0        0    12184 2023-07-20 09:50:47.000000 rubpy-6.3.3/rubpy/network/connection.py
+-rw-rw-rw-   0        0        0    14807 2022-09-12 11:03:20.000000 rubpy-6.3.3/rubpy/network/proxies.py
+drwxrwxrwx   0        0        0        0 2023-07-23 18:24:39.513049 rubpy-6.3.3/rubpy/sessions/
+-rw-rw-rw-   0        0        0       82 2022-09-12 11:03:20.000000 rubpy-6.3.3/rubpy/sessions/__init__.py
+-rw-rw-rw-   0        0        0     2295 2023-06-14 11:13:33.000000 rubpy-6.3.3/rubpy/sessions/sqliteSession.py
+-rw-rw-rw-   0        0        0     1223 2022-09-12 11:03:20.000000 rubpy-6.3.3/rubpy/sessions/stringSession.py
+drwxrwxrwx   0        0        0        0 2023-07-23 18:24:39.513049 rubpy-6.3.3/rubpy/structs/
+-rw-rw-rw-   0        0        0       99 2022-09-12 11:03:20.000000 rubpy-6.3.3/rubpy/structs/__init__.py
+-rw-rw-rw-   0        0        0     1985 2022-09-12 11:03:20.000000 rubpy-6.3.3/rubpy/structs/handlers.py
+-rw-rw-rw-   0        0        0     4585 2022-09-12 11:03:20.000000 rubpy-6.3.3/rubpy/structs/models.py
+-rw-rw-rw-   0        0        0      702 2022-09-12 11:03:20.000000 rubpy-6.3.3/rubpy/structs/results.py
+-rw-rw-rw-   0        0        0    15140 2023-04-23 17:55:22.000000 rubpy-6.3.3/rubpy/structs/struct.py
+drwxrwxrwx   0        0        0        0 2023-07-23 18:24:39.503022 rubpy-6.3.3/rubpy.egg-info/
+-rw-rw-rw-   0        0        0     3378 2023-07-23 18:24:39.000000 rubpy-6.3.3/rubpy.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      697 2023-07-23 18:24:39.000000 rubpy-6.3.3/rubpy.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 18:24:39.000000 rubpy-6.3.3/rubpy.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       69 2023-07-23 18:24:39.000000 rubpy-6.3.3/rubpy.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        6 2023-07-23 18:24:39.000000 rubpy-6.3.3/rubpy.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 18:24:39.522970 rubpy-6.3.3/setup.cfg
+-rw-rw-rw-   0        0        0     1558 2023-07-23 18:24:00.000000 rubpy-6.3.3/setup.py
```

### Comparing `rubpy-6.3.2/PKG-INFO` & `rubpy-6.3.3/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: rubpy
-Version: 6.3.2
+Version: 6.3.3
 Summary: This is an unofficial library and fastest library for deploying robots on Rubika accounts.
 Home-page: https://github.com/shayanheidari01/rubika
 Author: Shayan Heidari
 Author-email: contact@shayanheidari.info
 Keywords: rubika,rubpy,chat,bot,robot,asyncio
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: rubpy Version: 6.3.2 Summary: This is an unofficial
+Metadata-Version: 2.1 Name: rubpy Version: 6.3.3 Summary: This is an unofficial
 library and fastest library for deploying robots on Rubika accounts. Home-page:
 https://github.com/shayanheidari01/rubika Author: Shayan Heidari Author-email:
 contact@shayanheidari.info Keywords: rubika,rubpy,chat,bot,robot,asyncio
 Classifier: Programming Language :: Python :: 3.7 Classifier: Programming
 Language :: Python :: 3.8 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10 Classifier: Programming
 Language :: Python :: 3.11 Classifier: Programming Language :: Python :: 3.12
```

### Comparing `rubpy-6.3.2/README.md` & `rubpy-6.3.3/README.md`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.2/rubpy/client.py` & `rubpy-6.3.3/rubpy/client.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 from .gadgets import exceptions, methods, thumbnail
 from .sessions import StringSession, SQLiteSession
 from .network import Connection, Proxies
 from . import __name__ as logger_name
 from mutagen.mp3 import MP3
 from .structs import Struct
-from aiofiles import aiopen
+from aiofiles import open as aiopen
 from .crypto import Crypto
 from io import BytesIO
 from re import compile
 import logging
 import os
```

### Comparing `rubpy-6.3.2/rubpy/crypto/crypto.py` & `rubpy-6.3.3/rubpy/crypto/crypto.py`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.2/rubpy/gadgets/classino.py` & `rubpy-6.3.3/rubpy/gadgets/classino.py`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.2/rubpy/gadgets/exceptions.py` & `rubpy-6.3.3/rubpy/gadgets/exceptions.py`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.2/rubpy/gadgets/grouping.py` & `rubpy-6.3.3/rubpy/gadgets/grouping.py`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.2/rubpy/gadgets/methods.py` & `rubpy-6.3.3/rubpy/gadgets/methods.py`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.2/rubpy/gadgets/thumbnail.py` & `rubpy-6.3.3/rubpy/gadgets/thumbnail.py`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.2/rubpy/network/connection.py` & `rubpy-6.3.3/rubpy/network/connection.py`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.2/rubpy/network/proxies.py` & `rubpy-6.3.3/rubpy/network/proxies.py`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.2/rubpy/sessions/sqliteSession.py` & `rubpy-6.3.3/rubpy/sessions/sqliteSession.py`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.2/rubpy/sessions/stringSession.py` & `rubpy-6.3.3/rubpy/sessions/stringSession.py`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.2/rubpy/structs/handlers.py` & `rubpy-6.3.3/rubpy/structs/handlers.py`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.2/rubpy/structs/models.py` & `rubpy-6.3.3/rubpy/structs/models.py`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.2/rubpy/structs/results.py` & `rubpy-6.3.3/rubpy/structs/results.py`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.2/rubpy/structs/struct.py` & `rubpy-6.3.3/rubpy/structs/struct.py`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.2/rubpy.egg-info/PKG-INFO` & `rubpy-6.3.3/rubpy.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: rubpy
-Version: 6.3.2
+Version: 6.3.3
 Summary: This is an unofficial library and fastest library for deploying robots on Rubika accounts.
 Home-page: https://github.com/shayanheidari01/rubika
 Author: Shayan Heidari
 Author-email: contact@shayanheidari.info
 Keywords: rubika,rubpy,chat,bot,robot,asyncio
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: rubpy Version: 6.3.2 Summary: This is an unofficial
+Metadata-Version: 2.1 Name: rubpy Version: 6.3.3 Summary: This is an unofficial
 library and fastest library for deploying robots on Rubika accounts. Home-page:
 https://github.com/shayanheidari01/rubika Author: Shayan Heidari Author-email:
 contact@shayanheidari.info Keywords: rubika,rubpy,chat,bot,robot,asyncio
 Classifier: Programming Language :: Python :: 3.7 Classifier: Programming
 Language :: Python :: 3.8 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10 Classifier: Programming
 Language :: Python :: 3.11 Classifier: Programming Language :: Python :: 3.12
```

### Comparing `rubpy-6.3.2/rubpy.egg-info/SOURCES.txt` & `rubpy-6.3.3/rubpy.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.2/setup.py` & `rubpy-6.3.3/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 requirements = ['aiohttp', 'pycryptodome', 'aiofiles', 'mutagen']
 
 with open("README.md", encoding="UTF-8") as f:
     readme = f.read()
 
 setup(
     name = 'rubpy',
-    version = '6.3.2',
+    version = '6.3.3',
     author='Shayan Heidari',
     author_email = 'contact@shayanheidari.info',
     description = 'This is an unofficial library and fastest library for deploying robots on Rubika accounts.',
     keywords = ['rubika', 'rubpy', 'chat', 'bot', 'robot', 'asyncio'],
     long_description = readme,
     python_requires="~=3.7",
     long_description_content_type = 'text/markdown',
```

