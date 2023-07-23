# Comparing `tmp/adafri-0.0.50.tar.gz` & `tmp/adafri-0.0.51.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "adafri-0.0.50.tar", last modified: Sun Jul 23 09:51:36 2023, max compression
+gzip compressed data, was "adafri-0.0.51.tar", last modified: Sun Jul 23 10:10:38 2023, max compression
```

## Comparing `adafri-0.0.50.tar` & `adafri-0.0.51.tar`

### file list

```diff
@@ -1,55 +1,55 @@
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.780714 adafri-0.0.50/
--rw-r--r--   0 ibrahima   (502) staff       (20)      177 2023-07-23 09:51:36.780137 adafri-0.0.50/PKG-INFO
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.737339 adafri-0.0.50/adafri/
--rw-r--r--   0 ibrahima   (502) staff       (20)       80 2023-07-23 09:51:27.000000 adafri-0.0.50/adafri/__init__.py
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.745957 adafri-0.0.50/adafri/utils/
--rw-r--r--   0 ibrahima   (502) staff       (20)      101 2023-07-21 05:44:28.000000 adafri-0.0.50/adafri/utils/__init__.py
--rw-r--r--   0 ibrahima   (502) staff       (20)     1252 2023-07-21 06:19:41.000000 adafri-0.0.50/adafri/utils/country.py
--rw-r--r--   0 ibrahima   (502) staff       (20)     2519 2023-07-22 08:32:21.000000 adafri-0.0.50/adafri/utils/phone_number.py
--rw-r--r--   0 ibrahima   (502) staff       (20)     1268 2023-07-11 19:28:16.000000 adafri-0.0.50/adafri/utils/response.py
--rw-r--r--   0 ibrahima   (502) staff       (20)    16874 2023-07-21 02:54:06.000000 adafri-0.0.50/adafri/utils/utils.py
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.752313 adafri-0.0.50/adafri/v1/
--rw-r--r--   0 ibrahima   (502) staff       (20)       93 2023-07-16 06:12:23.000000 adafri-0.0.50/adafri/v1/__init__.py
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.753216 adafri-0.0.50/adafri/v1/account/
--rw-r--r--   0 ibrahima   (502) staff       (20)      151 2023-07-12 07:06:08.000000 adafri-0.0.50/adafri/v1/account/__init__.py
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.756425 adafri-0.0.50/adafri/v1/account/models/
--rw-r--r--   0 ibrahima   (502) staff       (20)       91 2023-07-12 06:20:02.000000 adafri-0.0.50/adafri/v1/account/models/__init__.py
--rw-r--r--   0 ibrahima   (502) staff       (20)     4514 2023-07-20 05:14:32.000000 adafri-0.0.50/adafri/v1/account/models/account.py
--rw-r--r--   0 ibrahima   (502) staff       (20)     3816 2023-07-12 22:09:50.000000 adafri-0.0.50/adafri/v1/account/models/account_fields.py
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.757471 adafri-0.0.50/adafri/v1/auth/
--rw-r--r--   0 ibrahima   (502) staff       (20)      249 2023-07-16 05:40:34.000000 adafri-0.0.50/adafri/v1/auth/__init__.py
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.758757 adafri-0.0.50/adafri/v1/auth/firebase_auth/
--rw-r--r--   0 ibrahima   (502) staff       (20)       63 2023-07-23 09:42:02.000000 adafri-0.0.50/adafri/v1/auth/firebase_auth/__init__.py
--rw-r--r--   0 ibrahima   (502) staff       (20)     1556 2023-07-23 09:40:51.000000 adafri-0.0.50/adafri/v1/auth/firebase_auth/firebase_auth.py
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.759408 adafri-0.0.50/adafri/v1/auth/models/
--rw-r--r--   0 ibrahima   (502) staff       (20)        0 2023-07-12 11:05:39.000000 adafri-0.0.50/adafri/v1/auth/models/__init__.py
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.759905 adafri-0.0.50/adafri/v1/auth/oauth/
--rw-r--r--   0 ibrahima   (502) staff       (20)      814 2023-07-18 00:36:46.000000 adafri-0.0.50/adafri/v1/auth/oauth/__init__.py
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.768591 adafri-0.0.50/adafri/v1/auth/oauth/models/
--rw-r--r--   0 ibrahima   (502) staff       (20)       93 2023-07-12 11:08:07.000000 adafri-0.0.50/adafri/v1/auth/oauth/models/__init__.py
--rw-r--r--   0 ibrahima   (502) staff       (20)     6761 2023-07-21 06:23:32.000000 adafri-0.0.50/adafri/v1/auth/oauth/models/client.py
--rw-r--r--   0 ibrahima   (502) staff       (20)     4857 2023-07-13 16:12:18.000000 adafri-0.0.50/adafri/v1/auth/oauth/models/client_fields.py
--rw-r--r--   0 ibrahima   (502) staff       (20)    16078 2023-07-21 03:05:48.000000 adafri-0.0.50/adafri/v1/auth/oauth/models/grant.py
--rw-r--r--   0 ibrahima   (502) staff       (20)     3635 2023-07-19 20:20:48.000000 adafri-0.0.50/adafri/v1/auth/oauth/models/grant_fields.py
--rw-r--r--   0 ibrahima   (502) staff       (20)     9363 2023-07-21 03:03:35.000000 adafri-0.0.50/adafri/v1/auth/oauth/models/token.py
--rw-r--r--   0 ibrahima   (502) staff       (20)     3710 2023-07-21 03:04:50.000000 adafri-0.0.50/adafri/v1/auth/oauth/models/token_fields.py
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.772423 adafri-0.0.50/adafri/v1/auth/oauth/server/
--rw-r--r--   0 ibrahima   (502) staff       (20)      163 2023-07-16 05:39:01.000000 adafri-0.0.50/adafri/v1/auth/oauth/server/__init__.py
--rw-r--r--   0 ibrahima   (502) staff       (20)     1574 2023-07-20 05:43:11.000000 adafri-0.0.50/adafri/v1/auth/oauth/server/oidc_server.py
--rw-r--r--   0 ibrahima   (502) staff       (20)     2685 2023-07-19 19:45:35.000000 adafri-0.0.50/adafri/v1/auth/oauth/server/server.py
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.774828 adafri-0.0.50/adafri/v1/base/
--rw-r--r--   0 ibrahima   (502) staff       (20)       71 2023-07-12 22:38:38.000000 adafri-0.0.50/adafri/v1/base/__init__.py
--rw-r--r--   0 ibrahima   (502) staff       (20)     4240 2023-07-13 16:13:01.000000 adafri-0.0.50/adafri/v1/base/firebase_collection.py
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.775706 adafri-0.0.50/adafri/v1/user/
--rw-r--r--   0 ibrahima   (502) staff       (20)      129 2023-07-12 01:27:49.000000 adafri-0.0.50/adafri/v1/user/__init__.py
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.778804 adafri-0.0.50/adafri/v1/user/models/
--rw-r--r--   0 ibrahima   (502) staff       (20)       78 2023-07-12 00:55:42.000000 adafri-0.0.50/adafri/v1/user/models/__init__.py
--rw-r--r--   0 ibrahima   (502) staff       (20)    11424 2023-07-23 09:51:16.000000 adafri-0.0.50/adafri/v1/user/models/user.py
--rw-r--r--   0 ibrahima   (502) staff       (20)     5205 2023-07-12 04:59:49.000000 adafri-0.0.50/adafri/v1/user/models/user_fields.py
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.739762 adafri-0.0.50/adafri.egg-info/
--rw-r--r--   0 ibrahima   (502) staff       (20)      177 2023-07-23 09:51:36.000000 adafri-0.0.50/adafri.egg-info/PKG-INFO
--rw-r--r--   0 ibrahima   (502) staff       (20)     1220 2023-07-23 09:51:36.000000 adafri-0.0.50/adafri.egg-info/SOURCES.txt
--rw-r--r--   0 ibrahima   (502) staff       (20)        1 2023-07-23 09:51:36.000000 adafri-0.0.50/adafri.egg-info/dependency_links.txt
--rw-r--r--   0 ibrahima   (502) staff       (20)        7 2023-07-23 09:51:36.000000 adafri-0.0.50/adafri.egg-info/top_level.txt
--rw-r--r--   0 ibrahima   (502) staff       (20)       38 2023-07-23 09:51:36.781077 adafri-0.0.50/setup.cfg
--rw-r--r--   0 ibrahima   (502) staff       (20)      684 2023-07-16 01:48:05.000000 adafri-0.0.50/setup.py
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 10:10:38.261275 adafri-0.0.51/
+-rw-r--r--   0 ibrahima   (502) staff       (20)      177 2023-07-23 10:10:38.260807 adafri-0.0.51/PKG-INFO
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 10:10:38.217252 adafri-0.0.51/adafri/
+-rw-r--r--   0 ibrahima   (502) staff       (20)       80 2023-07-23 10:10:34.000000 adafri-0.0.51/adafri/__init__.py
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 10:10:38.225273 adafri-0.0.51/adafri/utils/
+-rw-r--r--   0 ibrahima   (502) staff       (20)      101 2023-07-21 05:44:28.000000 adafri-0.0.51/adafri/utils/__init__.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)     1252 2023-07-21 06:19:41.000000 adafri-0.0.51/adafri/utils/country.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)     2519 2023-07-22 08:32:21.000000 adafri-0.0.51/adafri/utils/phone_number.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)     1268 2023-07-11 19:28:16.000000 adafri-0.0.51/adafri/utils/response.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)    17295 2023-07-23 10:10:20.000000 adafri-0.0.51/adafri/utils/utils.py
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 10:10:38.226836 adafri-0.0.51/adafri/v1/
+-rw-r--r--   0 ibrahima   (502) staff       (20)       93 2023-07-16 06:12:23.000000 adafri-0.0.51/adafri/v1/__init__.py
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 10:10:38.227877 adafri-0.0.51/adafri/v1/account/
+-rw-r--r--   0 ibrahima   (502) staff       (20)      151 2023-07-12 07:06:08.000000 adafri-0.0.51/adafri/v1/account/__init__.py
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 10:10:38.230841 adafri-0.0.51/adafri/v1/account/models/
+-rw-r--r--   0 ibrahima   (502) staff       (20)       91 2023-07-12 06:20:02.000000 adafri-0.0.51/adafri/v1/account/models/__init__.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)     4514 2023-07-20 05:14:32.000000 adafri-0.0.51/adafri/v1/account/models/account.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)     3816 2023-07-12 22:09:50.000000 adafri-0.0.51/adafri/v1/account/models/account_fields.py
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 10:10:38.231778 adafri-0.0.51/adafri/v1/auth/
+-rw-r--r--   0 ibrahima   (502) staff       (20)      249 2023-07-16 05:40:34.000000 adafri-0.0.51/adafri/v1/auth/__init__.py
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 10:10:38.233601 adafri-0.0.51/adafri/v1/auth/firebase_auth/
+-rw-r--r--   0 ibrahima   (502) staff       (20)       63 2023-07-23 09:42:02.000000 adafri-0.0.51/adafri/v1/auth/firebase_auth/__init__.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)     1556 2023-07-23 09:40:51.000000 adafri-0.0.51/adafri/v1/auth/firebase_auth/firebase_auth.py
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 10:10:38.234726 adafri-0.0.51/adafri/v1/auth/models/
+-rw-r--r--   0 ibrahima   (502) staff       (20)        0 2023-07-12 11:05:39.000000 adafri-0.0.51/adafri/v1/auth/models/__init__.py
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 10:10:38.235470 adafri-0.0.51/adafri/v1/auth/oauth/
+-rw-r--r--   0 ibrahima   (502) staff       (20)      814 2023-07-18 00:36:46.000000 adafri-0.0.51/adafri/v1/auth/oauth/__init__.py
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 10:10:38.249903 adafri-0.0.51/adafri/v1/auth/oauth/models/
+-rw-r--r--   0 ibrahima   (502) staff       (20)       93 2023-07-12 11:08:07.000000 adafri-0.0.51/adafri/v1/auth/oauth/models/__init__.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)     6761 2023-07-21 06:23:32.000000 adafri-0.0.51/adafri/v1/auth/oauth/models/client.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)     4857 2023-07-13 16:12:18.000000 adafri-0.0.51/adafri/v1/auth/oauth/models/client_fields.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)    16078 2023-07-21 03:05:48.000000 adafri-0.0.51/adafri/v1/auth/oauth/models/grant.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)     3635 2023-07-19 20:20:48.000000 adafri-0.0.51/adafri/v1/auth/oauth/models/grant_fields.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)     9363 2023-07-21 03:03:35.000000 adafri-0.0.51/adafri/v1/auth/oauth/models/token.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)     3710 2023-07-21 03:04:50.000000 adafri-0.0.51/adafri/v1/auth/oauth/models/token_fields.py
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 10:10:38.253688 adafri-0.0.51/adafri/v1/auth/oauth/server/
+-rw-r--r--   0 ibrahima   (502) staff       (20)      163 2023-07-16 05:39:01.000000 adafri-0.0.51/adafri/v1/auth/oauth/server/__init__.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)     1574 2023-07-20 05:43:11.000000 adafri-0.0.51/adafri/v1/auth/oauth/server/oidc_server.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)     2685 2023-07-19 19:45:35.000000 adafri-0.0.51/adafri/v1/auth/oauth/server/server.py
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 10:10:38.256065 adafri-0.0.51/adafri/v1/base/
+-rw-r--r--   0 ibrahima   (502) staff       (20)       71 2023-07-12 22:38:38.000000 adafri-0.0.51/adafri/v1/base/__init__.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)     4240 2023-07-13 16:13:01.000000 adafri-0.0.51/adafri/v1/base/firebase_collection.py
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 10:10:38.256588 adafri-0.0.51/adafri/v1/user/
+-rw-r--r--   0 ibrahima   (502) staff       (20)      129 2023-07-12 01:27:49.000000 adafri-0.0.51/adafri/v1/user/__init__.py
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 10:10:38.259533 adafri-0.0.51/adafri/v1/user/models/
+-rw-r--r--   0 ibrahima   (502) staff       (20)       78 2023-07-12 00:55:42.000000 adafri-0.0.51/adafri/v1/user/models/__init__.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)    11424 2023-07-23 09:51:16.000000 adafri-0.0.51/adafri/v1/user/models/user.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)     5205 2023-07-12 04:59:49.000000 adafri-0.0.51/adafri/v1/user/models/user_fields.py
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 10:10:38.220281 adafri-0.0.51/adafri.egg-info/
+-rw-r--r--   0 ibrahima   (502) staff       (20)      177 2023-07-23 10:10:38.000000 adafri-0.0.51/adafri.egg-info/PKG-INFO
+-rw-r--r--   0 ibrahima   (502) staff       (20)     1220 2023-07-23 10:10:38.000000 adafri-0.0.51/adafri.egg-info/SOURCES.txt
+-rw-r--r--   0 ibrahima   (502) staff       (20)        1 2023-07-23 10:10:38.000000 adafri-0.0.51/adafri.egg-info/dependency_links.txt
+-rw-r--r--   0 ibrahima   (502) staff       (20)        7 2023-07-23 10:10:38.000000 adafri-0.0.51/adafri.egg-info/top_level.txt
+-rw-r--r--   0 ibrahima   (502) staff       (20)       38 2023-07-23 10:10:38.261479 adafri-0.0.51/setup.cfg
+-rw-r--r--   0 ibrahima   (502) staff       (20)      684 2023-07-16 01:48:05.000000 adafri-0.0.51/setup.py
```

### Comparing `adafri-0.0.50/adafri/utils/country.py` & `adafri-0.0.51/adafri/utils/country.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.50/adafri/utils/phone_number.py` & `adafri-0.0.51/adafri/utils/phone_number.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.50/adafri/utils/response.py` & `adafri-0.0.51/adafri/utils/response.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.50/adafri/utils/utils.py` & `adafri-0.0.51/adafri/utils/utils.py`

 * *Files 1% similar despite different names*

```diff
@@ -3,19 +3,35 @@
 from typing import Iterable
 import hashlib
 from cryptography.fernet import Fernet
 import os
 import base64
 from datetime import (date, datetime)
 from urllib.parse import urlparse, parse_qs
+import re
 
 hash = hashlib.sha1(str(os.getenv('CRYPTO_KEY')).encode())
 ENCRYPTION_KEY = base64.b64encode(hash.hexdigest()[:32].encode()).decode();
 
 
+camel_pat = re.compile(r'([A-Z])')
+under_pat = re.compile(r'_([a-z])')
+
+def camel_to_underscore(name):
+    return camel_pat.sub(lambda x: '_' + x.group(1).lower(), name)
+
+def underscore_to_camel(name):
+    return under_pat.sub(lambda x: x.group(1).upper(), name)
+
+def convert_to_camelcase(obj):
+    data = {}
+    for key in pydash.keys(obj):
+        data[underscore_to_camel(key)] = obj[key];
+    return data;
+
 def add_param_to_url(input_url,  params):
     import urllib.parse as urlparse
     from urllib.parse import urlencode
     url_parts = list(urlparse.urlparse(input_url))
     query = dict(urlparse.parse_qsl(url_parts[4]))
     query.update(params)
     url_parts[4] = urlencode(query)
```

### Comparing `adafri-0.0.50/adafri/v1/account/models/account.py` & `adafri-0.0.51/adafri/v1/account/models/account.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.50/adafri/v1/account/models/account_fields.py` & `adafri-0.0.51/adafri/v1/account/models/account_fields.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.50/adafri/v1/auth/firebase_auth/firebase_auth.py` & `adafri-0.0.51/adafri/v1/auth/firebase_auth/firebase_auth.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.50/adafri/v1/auth/oauth/__init__.py` & `adafri-0.0.51/adafri/v1/auth/oauth/__init__.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.50/adafri/v1/auth/oauth/models/client.py` & `adafri-0.0.51/adafri/v1/auth/oauth/models/client.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.50/adafri/v1/auth/oauth/models/client_fields.py` & `adafri-0.0.51/adafri/v1/auth/oauth/models/client_fields.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.50/adafri/v1/auth/oauth/models/grant.py` & `adafri-0.0.51/adafri/v1/auth/oauth/models/grant.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.50/adafri/v1/auth/oauth/models/grant_fields.py` & `adafri-0.0.51/adafri/v1/auth/oauth/models/grant_fields.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.50/adafri/v1/auth/oauth/models/token.py` & `adafri-0.0.51/adafri/v1/auth/oauth/models/token.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.50/adafri/v1/auth/oauth/models/token_fields.py` & `adafri-0.0.51/adafri/v1/auth/oauth/models/token_fields.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.50/adafri/v1/auth/oauth/server/oidc_server.py` & `adafri-0.0.51/adafri/v1/auth/oauth/server/oidc_server.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.50/adafri/v1/auth/oauth/server/server.py` & `adafri-0.0.51/adafri/v1/auth/oauth/server/server.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.50/adafri/v1/base/firebase_collection.py` & `adafri-0.0.51/adafri/v1/base/firebase_collection.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.50/adafri/v1/user/models/user.py` & `adafri-0.0.51/adafri/v1/user/models/user.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.50/adafri/v1/user/models/user_fields.py` & `adafri-0.0.51/adafri/v1/user/models/user_fields.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.50/adafri.egg-info/SOURCES.txt` & `adafri-0.0.51/adafri.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `adafri-0.0.50/setup.py` & `adafri-0.0.51/setup.py`

 * *Files identical despite different names*

