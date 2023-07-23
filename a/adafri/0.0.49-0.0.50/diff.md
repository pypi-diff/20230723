# Comparing `tmp/adafri-0.0.49.tar.gz` & `tmp/adafri-0.0.50.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "adafri-0.0.49.tar", last modified: Sat Jul 22 08:32:35 2023, max compression
+gzip compressed data, was "adafri-0.0.50.tar", last modified: Sun Jul 23 09:51:36 2023, max compression
```

## Comparing `adafri-0.0.49.tar` & `adafri-0.0.50.tar`

### file list

```diff
@@ -1,55 +1,55 @@
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-22 08:32:35.722051 adafri-0.0.49/
--rw-r--r--   0 ibrahima   (502) staff       (20)      177 2023-07-22 08:32:35.721496 adafri-0.0.49/PKG-INFO
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-22 08:32:35.677786 adafri-0.0.49/adafri/
--rw-r--r--   0 ibrahima   (502) staff       (20)       80 2023-07-22 08:32:28.000000 adafri-0.0.49/adafri/__init__.py
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-22 08:32:35.685865 adafri-0.0.49/adafri/utils/
--rw-r--r--   0 ibrahima   (502) staff       (20)      101 2023-07-21 05:44:28.000000 adafri-0.0.49/adafri/utils/__init__.py
--rw-r--r--   0 ibrahima   (502) staff       (20)     1252 2023-07-21 06:19:41.000000 adafri-0.0.49/adafri/utils/country.py
--rw-r--r--   0 ibrahima   (502) staff       (20)     2519 2023-07-22 08:32:21.000000 adafri-0.0.49/adafri/utils/phone_number.py
--rw-r--r--   0 ibrahima   (502) staff       (20)     1268 2023-07-11 19:28:16.000000 adafri-0.0.49/adafri/utils/response.py
--rw-r--r--   0 ibrahima   (502) staff       (20)    16874 2023-07-21 02:54:06.000000 adafri-0.0.49/adafri/utils/utils.py
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-22 08:32:35.688212 adafri-0.0.49/adafri/v1/
--rw-r--r--   0 ibrahima   (502) staff       (20)       93 2023-07-16 06:12:23.000000 adafri-0.0.49/adafri/v1/__init__.py
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-22 08:32:35.689496 adafri-0.0.49/adafri/v1/account/
--rw-r--r--   0 ibrahima   (502) staff       (20)      151 2023-07-12 07:06:08.000000 adafri-0.0.49/adafri/v1/account/__init__.py
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-22 08:32:35.692648 adafri-0.0.49/adafri/v1/account/models/
--rw-r--r--   0 ibrahima   (502) staff       (20)       91 2023-07-12 06:20:02.000000 adafri-0.0.49/adafri/v1/account/models/__init__.py
--rw-r--r--   0 ibrahima   (502) staff       (20)     4514 2023-07-20 05:14:32.000000 adafri-0.0.49/adafri/v1/account/models/account.py
--rw-r--r--   0 ibrahima   (502) staff       (20)     3816 2023-07-12 22:09:50.000000 adafri-0.0.49/adafri/v1/account/models/account_fields.py
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-22 08:32:35.693860 adafri-0.0.49/adafri/v1/auth/
--rw-r--r--   0 ibrahima   (502) staff       (20)      249 2023-07-16 05:40:34.000000 adafri-0.0.49/adafri/v1/auth/__init__.py
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-22 08:32:35.696237 adafri-0.0.49/adafri/v1/auth/firebase_auth/
--rw-r--r--   0 ibrahima   (502) staff       (20)       39 2023-07-12 12:02:09.000000 adafri-0.0.49/adafri/v1/auth/firebase_auth/__init__.py
--rw-r--r--   0 ibrahima   (502) staff       (20)     1226 2023-07-13 01:57:34.000000 adafri-0.0.49/adafri/v1/auth/firebase_auth/firebase_auth.py
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-22 08:32:35.697675 adafri-0.0.49/adafri/v1/auth/models/
--rw-r--r--   0 ibrahima   (502) staff       (20)        0 2023-07-12 11:05:39.000000 adafri-0.0.49/adafri/v1/auth/models/__init__.py
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-22 08:32:35.698300 adafri-0.0.49/adafri/v1/auth/oauth/
--rw-r--r--   0 ibrahima   (502) staff       (20)      814 2023-07-18 00:36:46.000000 adafri-0.0.49/adafri/v1/auth/oauth/__init__.py
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-22 08:32:35.710273 adafri-0.0.49/adafri/v1/auth/oauth/models/
--rw-r--r--   0 ibrahima   (502) staff       (20)       93 2023-07-12 11:08:07.000000 adafri-0.0.49/adafri/v1/auth/oauth/models/__init__.py
--rw-r--r--   0 ibrahima   (502) staff       (20)     6761 2023-07-21 06:23:32.000000 adafri-0.0.49/adafri/v1/auth/oauth/models/client.py
--rw-r--r--   0 ibrahima   (502) staff       (20)     4857 2023-07-13 16:12:18.000000 adafri-0.0.49/adafri/v1/auth/oauth/models/client_fields.py
--rw-r--r--   0 ibrahima   (502) staff       (20)    16078 2023-07-21 03:05:48.000000 adafri-0.0.49/adafri/v1/auth/oauth/models/grant.py
--rw-r--r--   0 ibrahima   (502) staff       (20)     3635 2023-07-19 20:20:48.000000 adafri-0.0.49/adafri/v1/auth/oauth/models/grant_fields.py
--rw-r--r--   0 ibrahima   (502) staff       (20)     9363 2023-07-21 03:03:35.000000 adafri-0.0.49/adafri/v1/auth/oauth/models/token.py
--rw-r--r--   0 ibrahima   (502) staff       (20)     3710 2023-07-21 03:04:50.000000 adafri-0.0.49/adafri/v1/auth/oauth/models/token_fields.py
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-22 08:32:35.713550 adafri-0.0.49/adafri/v1/auth/oauth/server/
--rw-r--r--   0 ibrahima   (502) staff       (20)      163 2023-07-16 05:39:01.000000 adafri-0.0.49/adafri/v1/auth/oauth/server/__init__.py
--rw-r--r--   0 ibrahima   (502) staff       (20)     1574 2023-07-20 05:43:11.000000 adafri-0.0.49/adafri/v1/auth/oauth/server/oidc_server.py
--rw-r--r--   0 ibrahima   (502) staff       (20)     2685 2023-07-19 19:45:35.000000 adafri-0.0.49/adafri/v1/auth/oauth/server/server.py
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-22 08:32:35.715763 adafri-0.0.49/adafri/v1/base/
--rw-r--r--   0 ibrahima   (502) staff       (20)       71 2023-07-12 22:38:38.000000 adafri-0.0.49/adafri/v1/base/__init__.py
--rw-r--r--   0 ibrahima   (502) staff       (20)     4240 2023-07-13 16:13:01.000000 adafri-0.0.49/adafri/v1/base/firebase_collection.py
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-22 08:32:35.716564 adafri-0.0.49/adafri/v1/user/
--rw-r--r--   0 ibrahima   (502) staff       (20)      129 2023-07-12 01:27:49.000000 adafri-0.0.49/adafri/v1/user/__init__.py
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-22 08:32:35.720125 adafri-0.0.49/adafri/v1/user/models/
--rw-r--r--   0 ibrahima   (502) staff       (20)       78 2023-07-12 00:55:42.000000 adafri-0.0.49/adafri/v1/user/models/__init__.py
--rw-r--r--   0 ibrahima   (502) staff       (20)     9309 2023-07-20 05:13:59.000000 adafri-0.0.49/adafri/v1/user/models/user.py
--rw-r--r--   0 ibrahima   (502) staff       (20)     5205 2023-07-12 04:59:49.000000 adafri-0.0.49/adafri/v1/user/models/user_fields.py
-drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-22 08:32:35.680311 adafri-0.0.49/adafri.egg-info/
--rw-r--r--   0 ibrahima   (502) staff       (20)      177 2023-07-22 08:32:35.000000 adafri-0.0.49/adafri.egg-info/PKG-INFO
--rw-r--r--   0 ibrahima   (502) staff       (20)     1220 2023-07-22 08:32:35.000000 adafri-0.0.49/adafri.egg-info/SOURCES.txt
--rw-r--r--   0 ibrahima   (502) staff       (20)        1 2023-07-22 08:32:35.000000 adafri-0.0.49/adafri.egg-info/dependency_links.txt
--rw-r--r--   0 ibrahima   (502) staff       (20)        7 2023-07-22 08:32:35.000000 adafri-0.0.49/adafri.egg-info/top_level.txt
--rw-r--r--   0 ibrahima   (502) staff       (20)       38 2023-07-22 08:32:35.722298 adafri-0.0.49/setup.cfg
--rw-r--r--   0 ibrahima   (502) staff       (20)      684 2023-07-16 01:48:05.000000 adafri-0.0.49/setup.py
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.780714 adafri-0.0.50/
+-rw-r--r--   0 ibrahima   (502) staff       (20)      177 2023-07-23 09:51:36.780137 adafri-0.0.50/PKG-INFO
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.737339 adafri-0.0.50/adafri/
+-rw-r--r--   0 ibrahima   (502) staff       (20)       80 2023-07-23 09:51:27.000000 adafri-0.0.50/adafri/__init__.py
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.745957 adafri-0.0.50/adafri/utils/
+-rw-r--r--   0 ibrahima   (502) staff       (20)      101 2023-07-21 05:44:28.000000 adafri-0.0.50/adafri/utils/__init__.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)     1252 2023-07-21 06:19:41.000000 adafri-0.0.50/adafri/utils/country.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)     2519 2023-07-22 08:32:21.000000 adafri-0.0.50/adafri/utils/phone_number.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)     1268 2023-07-11 19:28:16.000000 adafri-0.0.50/adafri/utils/response.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)    16874 2023-07-21 02:54:06.000000 adafri-0.0.50/adafri/utils/utils.py
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.752313 adafri-0.0.50/adafri/v1/
+-rw-r--r--   0 ibrahima   (502) staff       (20)       93 2023-07-16 06:12:23.000000 adafri-0.0.50/adafri/v1/__init__.py
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.753216 adafri-0.0.50/adafri/v1/account/
+-rw-r--r--   0 ibrahima   (502) staff       (20)      151 2023-07-12 07:06:08.000000 adafri-0.0.50/adafri/v1/account/__init__.py
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.756425 adafri-0.0.50/adafri/v1/account/models/
+-rw-r--r--   0 ibrahima   (502) staff       (20)       91 2023-07-12 06:20:02.000000 adafri-0.0.50/adafri/v1/account/models/__init__.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)     4514 2023-07-20 05:14:32.000000 adafri-0.0.50/adafri/v1/account/models/account.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)     3816 2023-07-12 22:09:50.000000 adafri-0.0.50/adafri/v1/account/models/account_fields.py
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.757471 adafri-0.0.50/adafri/v1/auth/
+-rw-r--r--   0 ibrahima   (502) staff       (20)      249 2023-07-16 05:40:34.000000 adafri-0.0.50/adafri/v1/auth/__init__.py
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.758757 adafri-0.0.50/adafri/v1/auth/firebase_auth/
+-rw-r--r--   0 ibrahima   (502) staff       (20)       63 2023-07-23 09:42:02.000000 adafri-0.0.50/adafri/v1/auth/firebase_auth/__init__.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)     1556 2023-07-23 09:40:51.000000 adafri-0.0.50/adafri/v1/auth/firebase_auth/firebase_auth.py
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.759408 adafri-0.0.50/adafri/v1/auth/models/
+-rw-r--r--   0 ibrahima   (502) staff       (20)        0 2023-07-12 11:05:39.000000 adafri-0.0.50/adafri/v1/auth/models/__init__.py
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.759905 adafri-0.0.50/adafri/v1/auth/oauth/
+-rw-r--r--   0 ibrahima   (502) staff       (20)      814 2023-07-18 00:36:46.000000 adafri-0.0.50/adafri/v1/auth/oauth/__init__.py
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.768591 adafri-0.0.50/adafri/v1/auth/oauth/models/
+-rw-r--r--   0 ibrahima   (502) staff       (20)       93 2023-07-12 11:08:07.000000 adafri-0.0.50/adafri/v1/auth/oauth/models/__init__.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)     6761 2023-07-21 06:23:32.000000 adafri-0.0.50/adafri/v1/auth/oauth/models/client.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)     4857 2023-07-13 16:12:18.000000 adafri-0.0.50/adafri/v1/auth/oauth/models/client_fields.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)    16078 2023-07-21 03:05:48.000000 adafri-0.0.50/adafri/v1/auth/oauth/models/grant.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)     3635 2023-07-19 20:20:48.000000 adafri-0.0.50/adafri/v1/auth/oauth/models/grant_fields.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)     9363 2023-07-21 03:03:35.000000 adafri-0.0.50/adafri/v1/auth/oauth/models/token.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)     3710 2023-07-21 03:04:50.000000 adafri-0.0.50/adafri/v1/auth/oauth/models/token_fields.py
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.772423 adafri-0.0.50/adafri/v1/auth/oauth/server/
+-rw-r--r--   0 ibrahima   (502) staff       (20)      163 2023-07-16 05:39:01.000000 adafri-0.0.50/adafri/v1/auth/oauth/server/__init__.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)     1574 2023-07-20 05:43:11.000000 adafri-0.0.50/adafri/v1/auth/oauth/server/oidc_server.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)     2685 2023-07-19 19:45:35.000000 adafri-0.0.50/adafri/v1/auth/oauth/server/server.py
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.774828 adafri-0.0.50/adafri/v1/base/
+-rw-r--r--   0 ibrahima   (502) staff       (20)       71 2023-07-12 22:38:38.000000 adafri-0.0.50/adafri/v1/base/__init__.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)     4240 2023-07-13 16:13:01.000000 adafri-0.0.50/adafri/v1/base/firebase_collection.py
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.775706 adafri-0.0.50/adafri/v1/user/
+-rw-r--r--   0 ibrahima   (502) staff       (20)      129 2023-07-12 01:27:49.000000 adafri-0.0.50/adafri/v1/user/__init__.py
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.778804 adafri-0.0.50/adafri/v1/user/models/
+-rw-r--r--   0 ibrahima   (502) staff       (20)       78 2023-07-12 00:55:42.000000 adafri-0.0.50/adafri/v1/user/models/__init__.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)    11424 2023-07-23 09:51:16.000000 adafri-0.0.50/adafri/v1/user/models/user.py
+-rw-r--r--   0 ibrahima   (502) staff       (20)     5205 2023-07-12 04:59:49.000000 adafri-0.0.50/adafri/v1/user/models/user_fields.py
+drwxr-xr-x   0 ibrahima   (502) staff       (20)        0 2023-07-23 09:51:36.739762 adafri-0.0.50/adafri.egg-info/
+-rw-r--r--   0 ibrahima   (502) staff       (20)      177 2023-07-23 09:51:36.000000 adafri-0.0.50/adafri.egg-info/PKG-INFO
+-rw-r--r--   0 ibrahima   (502) staff       (20)     1220 2023-07-23 09:51:36.000000 adafri-0.0.50/adafri.egg-info/SOURCES.txt
+-rw-r--r--   0 ibrahima   (502) staff       (20)        1 2023-07-23 09:51:36.000000 adafri-0.0.50/adafri.egg-info/dependency_links.txt
+-rw-r--r--   0 ibrahima   (502) staff       (20)        7 2023-07-23 09:51:36.000000 adafri-0.0.50/adafri.egg-info/top_level.txt
+-rw-r--r--   0 ibrahima   (502) staff       (20)       38 2023-07-23 09:51:36.781077 adafri-0.0.50/setup.cfg
+-rw-r--r--   0 ibrahima   (502) staff       (20)      684 2023-07-16 01:48:05.000000 adafri-0.0.50/setup.py
```

### Comparing `adafri-0.0.49/adafri/utils/country.py` & `adafri-0.0.50/adafri/utils/country.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.49/adafri/utils/phone_number.py` & `adafri-0.0.50/adafri/utils/phone_number.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.49/adafri/utils/response.py` & `adafri-0.0.50/adafri/utils/response.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.49/adafri/utils/utils.py` & `adafri-0.0.50/adafri/utils/utils.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.49/adafri/v1/account/models/account.py` & `adafri-0.0.50/adafri/v1/account/models/account.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.49/adafri/v1/account/models/account_fields.py` & `adafri-0.0.50/adafri/v1/account/models/account_fields.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.49/adafri/v1/auth/firebase_auth/firebase_auth.py` & `adafri-0.0.50/adafri/v1/auth/firebase_auth/firebase_auth.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,13 +1,24 @@
 import firebase_admin
 from firebase_admin import credentials
 from firebase_admin import firestore as f
 from firebase_admin.firestore import firestore
+from firebase_admin.exceptions import FirebaseError
 import os
 
+from firebase_admin import auth
+
+def create_firebase_user(email, password) -> 'auth.UserRecord':
+    try:
+        return auth.create_user(email=email, password=password)
+    except ValueError as e:
+        raise e
+    except FirebaseError as e:
+        raise e;  
+
 DEFAULT_PATH = os.environ.get('FIREBASE_CREDENTIALS_PATH');
 
 def initializeApp(path: str):
     if path is None:
         return None;
     try:
         absolute_path = os.path.dirname(__file__)
@@ -24,14 +35,15 @@
     
 class FirestoreApp:
     def __init__(self, credentials_path: str=DEFAULT_PATH) -> None:
         # print("Initializing Firestore from", credentials_path)
         app = initializeApp(credentials_path);
         if app is not None:
             self.app = app;
+            
     
     def firestore_client(self) -> firestore.Client:
         app = getattr(self, 'app', None)
         if app is None:
             return None;
         firestore_database = f.client(self.app);
         return firestore_database;
```

### Comparing `adafri-0.0.49/adafri/v1/auth/oauth/__init__.py` & `adafri-0.0.50/adafri/v1/auth/oauth/__init__.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.49/adafri/v1/auth/oauth/models/client.py` & `adafri-0.0.50/adafri/v1/auth/oauth/models/client.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.49/adafri/v1/auth/oauth/models/client_fields.py` & `adafri-0.0.50/adafri/v1/auth/oauth/models/client_fields.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.49/adafri/v1/auth/oauth/models/grant.py` & `adafri-0.0.50/adafri/v1/auth/oauth/models/grant.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.49/adafri/v1/auth/oauth/models/grant_fields.py` & `adafri-0.0.50/adafri/v1/auth/oauth/models/grant_fields.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.49/adafri/v1/auth/oauth/models/token.py` & `adafri-0.0.50/adafri/v1/auth/oauth/models/token.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.49/adafri/v1/auth/oauth/models/token_fields.py` & `adafri-0.0.50/adafri/v1/auth/oauth/models/token_fields.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.49/adafri/v1/auth/oauth/server/oidc_server.py` & `adafri-0.0.50/adafri/v1/auth/oauth/server/oidc_server.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.49/adafri/v1/auth/oauth/server/server.py` & `adafri-0.0.50/adafri/v1/auth/oauth/server/server.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.49/adafri/v1/base/firebase_collection.py` & `adafri-0.0.50/adafri/v1/base/firebase_collection.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.49/adafri/v1/user/models/user.py` & `adafri-0.0.50/adafri/v1/user/models/user.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,15 +1,16 @@
-from ...base.firebase_collection import FirebaseCollectionBase
-from ....utils import (DictUtils, get_object_model_class, init_class_kwargs)
+from ...base.firebase_collection import FirebaseCollectionBase, getTimestamp
+from ....utils import (DictUtils, get_object_model_class, init_class_kwargs, Crypto)
 from ....utils.response import ApiResponse, Error, ResponseStatus, StatusCode
 from .user_fields import UserFields, UserFieldProps, STANDARD_FIELDS, USERS_COLLECTION
 from typing import List
 from typing import Any
 from dataclasses import dataclass
 from firebase_admin import auth as admin_auth
+from adafri.v1.auth.firebase_auth import create_firebase_user
 from firebase_admin.exceptions import FirebaseError
 import pydash
 
 @dataclass
 class Account:
     canManageClients: bool
     childs: List[object]
@@ -166,15 +167,15 @@
     telephone: str
     token: List[str]
     uid: str
     user_type: str
     password: str
     provider: str
     
-    def __init__(self, user, **kwargs):
+    def __init__(self, user=None, **kwargs):
         (cls_object, keys, data_args) = init_class_kwargs(self, user, STANDARD_FIELDS, UserFieldProps, USERS_COLLECTION, ['id','uid'], **kwargs)
         super().__init__(**data_args);
         for key in keys:
             setattr(self, key, cls_object[key]);
     
 
 
@@ -207,14 +208,50 @@
             else:
                 for doc in query_result:
                     result.append(User.from_dict(user=doc, db=self.db, collection_name=self.collection_name))
                 return result
         if first:
                 return None
         return [];
+
+    def create(self, **kwargs):
+        data_dict = DictUtils.pick_fields(kwargs, UserFields.filtered_keys('mutable', True));
+        user_model = User().from_dict(DictUtils.merge_dict(data_dict, User.generate_model()));
+        if bool(user_model.to_json()) is False:
+            return ApiResponse(ResponseStatus.ERROR, StatusCode.status_400, None, Error("Empty request","INVALID_REQUEST", 1)).to_json(), 200
+        
+        email = user_model.email
+        password = user_model.password
+        
+        if bool(email) is False:
+            return ApiResponse(ResponseStatus.ERROR, StatusCode.status_400, None, Error("Email required","INVALID_REQUEST", 1));
+    
+        if bool(password) is False:
+            return ApiResponse(ResponseStatus.ERROR, StatusCode.status_400, None, Error("Password required","INVALID_REQUEST", 1));
+    
+        docs = User().collection().where('email', '==', email).get();
+        found_users = [];
+        if len(docs) > 0:
+            for doc in docs:
+                found_users.append(User.from_dict(doc.to_dict()).to_json());
+            return ApiResponse(ResponseStatus.ERROR, StatusCode.status_400, None, Error(f"User wiith emaill {user_model.email} already exist","INVALID_REQUEST", 1));
+    
+    
+        try:
+            user_model.isConnectWithMailAndPassword = bool(user_model.uid) is False
+            if bool(user_model.uid) is False:
+                user_record = create_firebase_user(email, password);
+                user_model.uid = user_record.uid;
+                hashed_password = Crypto().encrypt(password);
+                user_model.password = hashed_password;
+            User().collection().document(user_model.uid).set({**user_model.to_json(), "createdAt": getTimestamp()}, merge=True)
+            return ApiResponse(ResponseStatus.OK, StatusCode.status_200, user_model.to_json(), None);
+        except Exception as e:
+            print(e)
+            return ApiResponse(ResponseStatus.ERROR, StatusCode.status_400, None, Error(str(e),"INVALID_REQUEST", 1));
     
     def update(self, data):
         try:
             last_value = self.to_json();
             filtered_value = pydash.pick(data, UserFields.filtered_keys('editable', True));
             new_value = DictUtils.merge_dict(filtered_value, self.to_json());
             changed_fields = DictUtils.get_changed_field(last_value, new_value);
```

### Comparing `adafri-0.0.49/adafri/v1/user/models/user_fields.py` & `adafri-0.0.50/adafri/v1/user/models/user_fields.py`

 * *Files identical despite different names*

### Comparing `adafri-0.0.49/adafri.egg-info/SOURCES.txt` & `adafri-0.0.50/adafri.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `adafri-0.0.49/setup.py` & `adafri-0.0.50/setup.py`

 * *Files identical despite different names*

