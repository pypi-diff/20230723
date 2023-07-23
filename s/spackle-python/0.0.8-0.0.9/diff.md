# Comparing `tmp/spackle-python-0.0.8.tar.gz` & `tmp/spackle-python-0.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "spackle-python-0.0.8.tar", max compression
+gzip compressed data, was "spackle-python-0.0.9.tar", max compression
```

## Comparing `spackle-python-0.0.8.tar` & `spackle-python-0.0.9.tar`

### file list

```diff
@@ -1,8 +1,9 @@
--rw-r--r--   0        0        0        0 2022-11-11 18:03:10.050786 spackle-python-0.0.8/README.md
--rw-r--r--   0        0        0      447 2022-12-19 16:30:23.373336 spackle-python-0.0.8/pyproject.toml
--rw-r--r--   0        0        0      138 2022-12-18 04:40:35.462897 spackle-python-0.0.8/spackle/__init__.py
--rw-r--r--   0        0        0      956 2022-12-19 03:43:52.624106 spackle-python-0.0.8/spackle/customer.py
--rw-r--r--   0        0        0     1902 2022-12-19 16:27:21.252413 spackle-python-0.0.8/spackle/dynamodb.py
--rw-r--r--   0        0        0       44 2022-11-13 19:32:18.598568 spackle-python-0.0.8/spackle/exceptions.py
--rw-r--r--   0        0        0      621 1970-01-01 00:00:00.000000 spackle-python-0.0.8/setup.py
--rw-r--r--   0        0        0      423 1970-01-01 00:00:00.000000 spackle-python-0.0.8/PKG-INFO
+-rw-r--r--   0        0        0        0 2022-11-11 18:03:10.050786 spackle-python-0.0.9/README.md
+-rw-r--r--   0        0        0      447 2022-12-19 19:03:35.278533 spackle-python-0.0.9/pyproject.toml
+-rw-r--r--   0        0        0      138 2022-12-18 04:40:35.462897 spackle-python-0.0.9/spackle/__init__.py
+-rw-r--r--   0        0        0     1202 2022-12-19 19:01:55.408359 spackle-python-0.0.9/spackle/customer.py
+-rw-r--r--   0        0        0     2031 2022-12-19 19:01:14.840795 spackle-python-0.0.9/spackle/dynamodb.py
+-rw-r--r--   0        0        0       44 2022-11-13 19:32:18.598568 spackle-python-0.0.9/spackle/exceptions.py
+-rw-r--r--   0        0        0     1652 2022-12-19 18:51:36.726000 spackle-python-0.0.9/spackle/log.py
+-rw-r--r--   0        0        0      621 1970-01-01 00:00:00.000000 spackle-python-0.0.9/setup.py
+-rw-r--r--   0        0        0      423 1970-01-01 00:00:00.000000 spackle-python-0.0.9/PKG-INFO
```

### Comparing `spackle-python-0.0.8/spackle/customer.py` & `spackle-python-0.0.9/spackle/customer.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,38 +1,43 @@
 import json
-import time
+import pprint
 
-from spackle import dynamodb
-from spackle.exceptions import SpackleException
+from spackle import dynamodb, log
 
 
 class Customer:
-    def __init__(self, data):
+    def __init__(self, id, data):
+        self.id = id
         self.data = data
 
     @staticmethod
     def retrieve(customer_id):
+        log.log_debug("Retrieving customer data for %s" % customer_id)
         dynamodb_client = dynamodb.get_client()
         response = dynamodb_client.get_item(
             TableName=dynamodb.table_name,
             Key={
                 "AccountId": {"S": dynamodb.identity_id},
                 "CustomerId": {"S": customer_id},
             },
         )
 
         data = json.loads(response["Item"]["State"]["S"])
-        return Customer(data)
+        log.log_debug("Retrieved customer data for %s: %s" % (customer_id, data))
+        return Customer(customer_id, data)
 
     def enabled(self, key):
         for feature in self.data["features"]:
             if feature["key"] == key:
                 return feature["value_flag"]
 
         return False
 
     def limit(self, key):
         for feature in self.data["features"]:
             if feature["key"] == key:
                 return feature["value_limit"]
 
         return 0
+
+    def __repr__(self):
+        return f"<Customer ({self.id}):\n{pprint.pformat(self.data)}>"
```

### Comparing `spackle-python-0.0.8/spackle/dynamodb.py` & `spackle-python-0.0.9/spackle/dynamodb.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,10 +1,11 @@
 import boto3
 import requests
 from datetime import datetime, timezone
+from spackle import log
 
 _aws_access_key_id = None
 _aws_region = None
 _aws_secret_access_key = None
 _aws_session_expiration = None
 _aws_session_token = None
 
@@ -25,14 +26,15 @@
     ):
         _bootstrap_client()
 
     return client
 
 
 def _bootstrap_client():
+    log.log_debug("Bootstrapping DynamoDB client...")
     from spackle import api_key, api_base
 
     global client
     global table_name
     global identity_id
     global _aws_access_key_id
     global _aws_region
@@ -40,14 +42,15 @@
     global _aws_session_token
     global _aws_session_expiration
 
     session = requests.post(
         f"{api_base}/auth/session",
         headers={"Authorization": f"Bearer {api_key}"},
     ).json()
+    log.log_debug("Created session: %s" % session)
 
     sts_client = boto3.client("sts")
     credentials = sts_client.assume_role_with_web_identity(
         RoleArn=session["role_arn"],
         RoleSessionName=session["account_id"],
         WebIdentityToken=session["token"],
     )
```

### Comparing `spackle-python-0.0.8/setup.py` & `spackle-python-0.0.9/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -8,15 +8,15 @@
 {'': ['*']}
 
 install_requires = \
 ['boto3>=1.26.32,<2.0.0', 'requests>=2.28.1,<3.0.0']
 
 setup_kwargs = {
     'name': 'spackle-python',
-    'version': '0.0.8',
+    'version': '0.0.9',
     'description': '',
     'long_description': '',
     'author': 'Hunter Clarke',
     'author_email': 'hunter@spackle.so',
     'maintainer': 'None',
     'maintainer_email': 'None',
     'url': 'None',
```

