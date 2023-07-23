# Comparing `tmp/multion-0.1.8.tar.gz` & `tmp/multion-0.1.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "multion-0.1.8.tar", max compression
+gzip compressed data, was "multion-0.1.9.tar", max compression
```

## Comparing `multion-0.1.8.tar` & `multion-0.1.9.tar`

### file list

```diff
@@ -1,6 +1,6 @@
--rw-r--r--   0        0        0      188 2023-06-24 00:14:48.342052 multion-0.1.8/README.md
--rw-r--r--   0        0        0      387 2023-06-24 04:13:21.479092 multion-0.1.8/multion/__init__.py
--rw-r--r--   0        0        0     5556 2023-06-24 04:05:13.399193 multion-0.1.8/multion/multion.py
--rw-r--r--   0        0        0      325 2023-06-24 00:14:48.352052 multion-0.1.8/multion/setup.py
--rw-r--r--   0        0        0      360 2023-06-24 04:13:26.849091 multion-0.1.8/pyproject.toml
--rw-r--r--   0        0        0      764 1970-01-01 00:00:00.000000 multion-0.1.8/PKG-INFO
+-rw-r--r--   0        0        0      188 2023-06-24 00:14:48.342052 multion-0.1.9/README.md
+-rw-r--r--   0        0        0      387 2023-06-24 04:13:21.479092 multion-0.1.9/multion/__init__.py
+-rw-r--r--   0        0        0     5783 2023-06-24 04:42:39.588728 multion-0.1.9/multion/multion.py
+-rw-r--r--   0        0        0      325 2023-06-24 00:14:48.352052 multion-0.1.9/multion/setup.py
+-rw-r--r--   0        0        0      360 2023-06-24 04:42:44.538727 multion-0.1.9/pyproject.toml
+-rw-r--r--   0        0        0      764 1970-01-01 00:00:00.000000 multion-0.1.9/PKG-INFO
```

### Comparing `multion-0.1.8/multion/multion.py` & `multion-0.1.9/multion/multion.py`

 * *Files 4% similar despite different names*

```diff
@@ -5,26 +5,28 @@
 from flask import Flask, request
 from requests_oauthlib import OAuth2Session
 from threading import Thread
 import json
 import time
 
 class _Multion:
-    def __init__(self, token_file='multion_token.txt'):
-        self.client_id = os.environ['MULTION_CLIENT_ID']
-        self.client_secret = os.environ['MULTION_CLIENT_SECRET']
+    def __init__(self, client_id=None, client_secret=None, token_file='multion_token.txt'):
+        self.client_id = client_id if client_id else os.environ['MULTION_CLIENT_ID']
+        self.client_secret = client_secret if client_secret else os.environ['MULTION_CLIENT_SECRET']
         self.token_file = token_file
         self.token = None
 
         # Try to load the token from the token file
         if os.path.exists(self.token_file):
             with open(self.token_file, 'r') as f:
                 self.token = f.read().strip()
 
-    def login(self):
+    def login(client_id=None, client_secret=None):
+        _multion_instance = _Multion(client_id, client_secret)
+        _multion_instance.login()
         # If the token is already loaded, no need to log in again
         if self.token is not None:
             return
 
         # OAuth endpoints
         authorization_base_url = 'https://auth.multion.ai/oauth2/authorize'
         token_url = 'https://auth.multion.ai/oauth2/token'
```

### Comparing `multion-0.1.8/PKG-INFO` & `multion-0.1.9/PKG-INFO`

 * *Files 14% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: multion
-Version: 0.1.8
+Version: 0.1.9
 Summary: MULTION API
 Author: Div Garg
 Requires-Python: >=3.9,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
```

