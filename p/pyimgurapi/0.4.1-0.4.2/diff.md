# Comparing `tmp/pyimgurapi-0.4.1.tar.gz` & `tmp/pyimgurapi-0.4.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyimgurapi-0.4.1.tar", max compression
+gzip compressed data, was "pyimgurapi-0.4.2.tar", max compression
```

## Comparing `pyimgurapi-0.4.1.tar` & `pyimgurapi-0.4.2.tar`

### file list

```diff
@@ -1,17 +1,17 @@
--rw-r--r--   0        0        0     1080 2023-05-05 16:45:13.078314 pyimgurapi-0.4.1/LICENSE
--rw-r--r--   0        0        0       54 2023-05-08 15:51:05.855700 pyimgurapi-0.4.1/pyimgurapi/__init__.py
--rw-r--r--   0        0        0     2771 2023-07-23 11:47:22.776243 pyimgurapi-0.4.1/pyimgurapi/api.py
--rw-r--r--   0        0        0      241 2023-05-08 18:48:16.094298 pyimgurapi-0.4.1/pyimgurapi/endpoints/__init__.py
--rw-r--r--   0        0        0     6338 2023-07-23 01:11:40.129544 pyimgurapi-0.4.1/pyimgurapi/endpoints/account.py
--rw-r--r--   0        0        0     3993 2023-06-11 20:39:27.669271 pyimgurapi-0.4.1/pyimgurapi/endpoints/album.py
--rw-r--r--   0        0        0     2601 2023-07-19 21:36:40.810670 pyimgurapi-0.4.1/pyimgurapi/endpoints/base_endpoint.py
--rw-r--r--   0        0        0     2409 2023-06-25 12:25:21.696989 pyimgurapi-0.4.1/pyimgurapi/endpoints/comment.py
--rw-r--r--   0        0        0       82 2023-05-08 18:11:01.478181 pyimgurapi-0.4.1/pyimgurapi/endpoints/feed.py
--rw-r--r--   0        0        0       85 2023-05-08 18:11:01.512250 pyimgurapi-0.4.1/pyimgurapi/endpoints/gallery.py
--rw-r--r--   0        0        0     9856 2023-07-23 01:12:22.523470 pyimgurapi-0.4.1/pyimgurapi/endpoints/image.py
--rw-r--r--   0        0        0      502 2023-05-11 18:42:58.380280 pyimgurapi-0.4.1/pyimgurapi/exceptions.py
--rw-r--r--   0        0        0     2951 2023-07-12 18:16:54.887240 pyimgurapi-0.4.1/pyimgurapi/form_factories.py
--rw-r--r--   0        0        0     3846 2023-07-23 11:43:47.712185 pyimgurapi-0.4.1/pyimgurapi/utils.py
--rw-r--r--   0        0        0      388 2023-07-23 16:04:29.658980 pyimgurapi-0.4.1/pyproject.toml
--rw-r--r--   0        0        0     4891 2023-07-23 16:03:33.122969 pyimgurapi-0.4.1/README.md
--rw-r--r--   0        0        0     5234 1970-01-01 00:00:00.000000 pyimgurapi-0.4.1/PKG-INFO
+-rw-r--r--   0        0        0     1080 2023-05-05 16:45:13.078314 pyimgurapi-0.4.2/LICENSE
+-rw-r--r--   0        0        0       54 2023-05-08 15:51:05.855700 pyimgurapi-0.4.2/pyimgurapi/__init__.py
+-rw-r--r--   0        0        0     2771 2023-07-23 11:47:22.776243 pyimgurapi-0.4.2/pyimgurapi/api.py
+-rw-r--r--   0        0        0      241 2023-05-08 18:48:16.094298 pyimgurapi-0.4.2/pyimgurapi/endpoints/__init__.py
+-rw-r--r--   0        0        0     6338 2023-07-23 01:11:40.129544 pyimgurapi-0.4.2/pyimgurapi/endpoints/account.py
+-rw-r--r--   0        0        0     3993 2023-06-11 20:39:27.669271 pyimgurapi-0.4.2/pyimgurapi/endpoints/album.py
+-rw-r--r--   0        0        0     2601 2023-07-19 21:36:40.810670 pyimgurapi-0.4.2/pyimgurapi/endpoints/base_endpoint.py
+-rw-r--r--   0        0        0     2409 2023-06-25 12:25:21.696989 pyimgurapi-0.4.2/pyimgurapi/endpoints/comment.py
+-rw-r--r--   0        0        0       82 2023-05-08 18:11:01.478181 pyimgurapi-0.4.2/pyimgurapi/endpoints/feed.py
+-rw-r--r--   0        0        0       85 2023-05-08 18:11:01.512250 pyimgurapi-0.4.2/pyimgurapi/endpoints/gallery.py
+-rw-r--r--   0        0        0     9856 2023-07-23 01:12:22.523470 pyimgurapi-0.4.2/pyimgurapi/endpoints/image.py
+-rw-r--r--   0        0        0      502 2023-05-11 18:42:58.380280 pyimgurapi-0.4.2/pyimgurapi/exceptions.py
+-rw-r--r--   0        0        0     2951 2023-07-12 18:16:54.887240 pyimgurapi-0.4.2/pyimgurapi/form_factories.py
+-rw-r--r--   0        0        0     3846 2023-07-23 11:43:47.712185 pyimgurapi-0.4.2/pyimgurapi/utils.py
+-rw-r--r--   0        0        0      388 2023-07-23 16:36:07.344205 pyimgurapi-0.4.2/pyproject.toml
+-rw-r--r--   0        0        0     5094 2023-07-23 16:33:31.233528 pyimgurapi-0.4.2/README.md
+-rw-r--r--   0        0        0     5436 1970-01-01 00:00:00.000000 pyimgurapi-0.4.2/PKG-INFO
```

### Comparing `pyimgurapi-0.4.1/LICENSE` & `pyimgurapi-0.4.2/LICENSE`

 * *Files identical despite different names*

### Comparing `pyimgurapi-0.4.1/pyimgurapi/api.py` & `pyimgurapi-0.4.2/pyimgurapi/api.py`

 * *Files identical despite different names*

### Comparing `pyimgurapi-0.4.1/pyimgurapi/endpoints/account.py` & `pyimgurapi-0.4.2/pyimgurapi/endpoints/account.py`

 * *Files identical despite different names*

### Comparing `pyimgurapi-0.4.1/pyimgurapi/endpoints/album.py` & `pyimgurapi-0.4.2/pyimgurapi/endpoints/album.py`

 * *Files identical despite different names*

### Comparing `pyimgurapi-0.4.1/pyimgurapi/endpoints/base_endpoint.py` & `pyimgurapi-0.4.2/pyimgurapi/endpoints/base_endpoint.py`

 * *Files identical despite different names*

### Comparing `pyimgurapi-0.4.1/pyimgurapi/endpoints/comment.py` & `pyimgurapi-0.4.2/pyimgurapi/endpoints/comment.py`

 * *Files identical despite different names*

### Comparing `pyimgurapi-0.4.1/pyimgurapi/endpoints/image.py` & `pyimgurapi-0.4.2/pyimgurapi/endpoints/image.py`

 * *Files identical despite different names*

### Comparing `pyimgurapi-0.4.1/pyimgurapi/form_factories.py` & `pyimgurapi-0.4.2/pyimgurapi/form_factories.py`

 * *Files identical despite different names*

### Comparing `pyimgurapi-0.4.1/pyimgurapi/utils.py` & `pyimgurapi-0.4.2/pyimgurapi/utils.py`

 * *Files identical despite different names*

### Comparing `pyimgurapi-0.4.1/README.md` & `pyimgurapi-0.4.2/README.md`

 * *Files 4% similar despite different names*

```diff
@@ -1,9 +1,12 @@
 # PyImgurAPI
 
+[![PyPI](https://img.shields.io/pypi/v/pyimgurapi.svg)](https://pypi.org/project/pyimgurapi/)
+[![Python Version](https://img.shields.io/pypi/pyversions/pyimgurapi.svg)](https://pypi.org/project/pyimgurapi/)
+
 A Python SDK for the Imgur API.
 
 ## Overview
 The package is supposed to be in strict accordance with the [Imgur's documentation](https://apidocs.imgur.com/), i.e. description for any endpoint implemented in the SDK can also be found there.
 
 The package does not have any third-party dependencies; it requires only Python 3.7+.
 
@@ -19,17 +22,15 @@
 $ pip install pyimgurapi
 ```
 
 ## First authentication
 
 1. [Register your application](https://api.imgur.com/oauth2/addclient) to get `client_id` and `client_secret`.
 2. Open the next URL in a browser:
-```
-https://api.imgur.com/oauth2/authorize?client_id=<your_client_id>&response_type=token
-```
+`https://api.imgur.com/oauth2/authorize?client_id=<your_client_id>&response_type=token`
 _(replace `<your_client_id>` with the actual ID)_
 3. Allow authentication for a client.
 4. Copy the `refresh_token` value from the URL field.
 5. Then you can authenticate your client:
 ```python
 from pyimgurapi import ImgurAPI
```

### Comparing `pyimgurapi-0.4.1/PKG-INFO` & `pyimgurapi-0.4.2/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,24 +1,27 @@
 Metadata-Version: 2.1
 Name: pyimgurapi
-Version: 0.4.1
+Version: 0.4.2
 Summary: 
 Author: nautics889
 Author-email: cyberukr@gmail.com
 Requires-Python: >=3.7,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Description-Content-Type: text/markdown
 
 # PyImgurAPI
 
+[![PyPI](https://img.shields.io/pypi/v/pyimgurapi.svg)](https://pypi.org/project/pyimgurapi/)
+[![Python Version](https://img.shields.io/pypi/pyversions/pyimgurapi.svg)](https://pypi.org/project/pyimgurapi/)
+
 A Python SDK for the Imgur API.
 
 ## Overview
 The package is supposed to be in strict accordance with the [Imgur's documentation](https://apidocs.imgur.com/), i.e. description for any endpoint implemented in the SDK can also be found there.
 
 The package does not have any third-party dependencies; it requires only Python 3.7+.
 
@@ -34,17 +37,15 @@
 $ pip install pyimgurapi
 ```
 
 ## First authentication
 
 1. [Register your application](https://api.imgur.com/oauth2/addclient) to get `client_id` and `client_secret`.
 2. Open the next URL in a browser:
-```
-https://api.imgur.com/oauth2/authorize?client_id=<your_client_id>&response_type=token
-```
+`https://api.imgur.com/oauth2/authorize?client_id=<your_client_id>&response_type=token`
 _(replace `<your_client_id>` with the actual ID)_
 3. Allow authentication for a client.
 4. Copy the `refresh_token` value from the URL field.
 5. Then you can authenticate your client:
 ```python
 from pyimgurapi import ImgurAPI
```

