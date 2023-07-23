# Comparing `tmp/BlitzChain-0.7.0.tar.gz` & `tmp/BlitzChain-0.7.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "BlitzChain-0.7.0.tar", last modified: Thu Jul 20 07:26:57 2023, max compression
+gzip compressed data, was "BlitzChain-0.7.1.tar", last modified: Sun Jul 23 12:57:01 2023, max compression
```

## Comparing `BlitzChain-0.7.0.tar` & `BlitzChain-0.7.1.tar`

### file list

```diff
@@ -1,24 +1,24 @@
-drwxr-xr-x   0 jackywong   (501) staff       (20)        0 2023-07-20 07:26:57.746065 BlitzChain-0.7.0/
-drwxr-xr-x   0 jackywong   (501) staff       (20)        0 2023-07-20 07:26:57.740579 BlitzChain-0.7.0/BlitzChain.egg-info/
--rw-r--r--   0 jackywong   (501) staff       (20)      189 2023-07-20 07:26:57.000000 BlitzChain-0.7.0/BlitzChain.egg-info/PKG-INFO
--rw-r--r--   0 jackywong   (501) staff       (20)      361 2023-07-20 07:26:57.000000 BlitzChain-0.7.0/BlitzChain.egg-info/SOURCES.txt
--rw-r--r--   0 jackywong   (501) staff       (20)        1 2023-07-20 07:26:57.000000 BlitzChain-0.7.0/BlitzChain.egg-info/dependency_links.txt
--rw-r--r--   0 jackywong   (501) staff       (20)        9 2023-07-20 07:26:57.000000 BlitzChain-0.7.0/BlitzChain.egg-info/requires.txt
--rw-r--r--   0 jackywong   (501) staff       (20)       15 2023-07-20 07:26:57.000000 BlitzChain-0.7.0/BlitzChain.egg-info/top_level.txt
--rw-r--r--   0 jackywong   (501) staff       (20)    11357 2023-06-25 04:01:50.000000 BlitzChain-0.7.0/LICENSE
--rw-r--r--   0 jackywong   (501) staff       (20)      189 2023-07-20 07:26:57.745762 BlitzChain-0.7.0/PKG-INFO
--rw-r--r--   0 jackywong   (501) staff       (20)     3436 2023-07-09 13:29:34.000000 BlitzChain-0.7.0/README.md
-drwxr-xr-x   0 jackywong   (501) staff       (20)        0 2023-07-20 07:26:57.742445 BlitzChain-0.7.0/blitzchain/
--rw-r--r--   0 jackywong   (501) staff       (20)       42 2023-07-20 07:05:27.000000 BlitzChain-0.7.0/blitzchain/__init__.py
--rw-r--r--   0 jackywong   (501) staff       (20)     8357 2023-07-20 07:06:24.000000 BlitzChain-0.7.0/blitzchain/api.py
--rw-r--r--   0 jackywong   (501) staff       (20)     2079 2023-07-20 07:06:24.000000 BlitzChain-0.7.0/blitzchain/splitter.py
--rw-r--r--   0 jackywong   (501) staff       (20)      794 2023-07-20 07:06:24.000000 BlitzChain-0.7.0/blitzchain/utils.py
-drwxr-xr-x   0 jackywong   (501) staff       (20)        0 2023-07-20 07:26:57.743422 BlitzChain-0.7.0/cli/
--rw-r--r--   0 jackywong   (501) staff       (20)        0 2023-07-09 14:53:24.000000 BlitzChain-0.7.0/cli/__init__.py
--rw-r--r--   0 jackywong   (501) staff       (20)      435 2023-07-20 07:06:24.000000 BlitzChain-0.7.0/cli/main.py
--rw-r--r--   0 jackywong   (501) staff       (20)       38 2023-07-20 07:26:57.746173 BlitzChain-0.7.0/setup.cfg
--rw-r--r--   0 jackywong   (501) staff       (20)      481 2023-07-20 07:06:24.000000 BlitzChain-0.7.0/setup.py
-drwxr-xr-x   0 jackywong   (501) staff       (20)        0 2023-07-20 07:26:57.745152 BlitzChain-0.7.0/tests/
--rw-r--r--   0 jackywong   (501) staff       (20)      216 2023-07-20 07:06:24.000000 BlitzChain-0.7.0/tests/test_crud.py
--rw-r--r--   0 jackywong   (501) staff       (20)      722 2023-07-20 07:06:24.000000 BlitzChain-0.7.0/tests/test_pdf.py
--rw-r--r--   0 jackywong   (501) staff       (20)      615 2023-07-20 07:06:24.000000 BlitzChain-0.7.0/tests/test_qa.py
+drwxr-xr-x   0 jackywong   (501) staff       (20)        0 2023-07-23 12:57:01.229037 BlitzChain-0.7.1/
+drwxr-xr-x   0 jackywong   (501) staff       (20)        0 2023-07-23 12:57:01.224424 BlitzChain-0.7.1/BlitzChain.egg-info/
+-rw-r--r--   0 jackywong   (501) staff       (20)      189 2023-07-23 12:57:01.000000 BlitzChain-0.7.1/BlitzChain.egg-info/PKG-INFO
+-rw-r--r--   0 jackywong   (501) staff       (20)      361 2023-07-23 12:57:01.000000 BlitzChain-0.7.1/BlitzChain.egg-info/SOURCES.txt
+-rw-r--r--   0 jackywong   (501) staff       (20)        1 2023-07-23 12:57:01.000000 BlitzChain-0.7.1/BlitzChain.egg-info/dependency_links.txt
+-rw-r--r--   0 jackywong   (501) staff       (20)        9 2023-07-23 12:57:01.000000 BlitzChain-0.7.1/BlitzChain.egg-info/requires.txt
+-rw-r--r--   0 jackywong   (501) staff       (20)       15 2023-07-23 12:57:01.000000 BlitzChain-0.7.1/BlitzChain.egg-info/top_level.txt
+-rw-r--r--   0 jackywong   (501) staff       (20)    11357 2023-06-25 04:01:50.000000 BlitzChain-0.7.1/LICENSE
+-rw-r--r--   0 jackywong   (501) staff       (20)      189 2023-07-23 12:57:01.228698 BlitzChain-0.7.1/PKG-INFO
+-rw-r--r--   0 jackywong   (501) staff       (20)     3436 2023-07-09 13:29:34.000000 BlitzChain-0.7.1/README.md
+drwxr-xr-x   0 jackywong   (501) staff       (20)        0 2023-07-23 12:57:01.225994 BlitzChain-0.7.1/blitzchain/
+-rw-r--r--   0 jackywong   (501) staff       (20)       42 2023-07-23 12:55:22.000000 BlitzChain-0.7.1/blitzchain/__init__.py
+-rw-r--r--   0 jackywong   (501) staff       (20)     9261 2023-07-23 12:56:43.000000 BlitzChain-0.7.1/blitzchain/api.py
+-rw-r--r--   0 jackywong   (501) staff       (20)     2079 2023-07-20 07:06:24.000000 BlitzChain-0.7.1/blitzchain/splitter.py
+-rw-r--r--   0 jackywong   (501) staff       (20)      794 2023-07-23 12:53:33.000000 BlitzChain-0.7.1/blitzchain/utils.py
+drwxr-xr-x   0 jackywong   (501) staff       (20)        0 2023-07-23 12:57:01.226654 BlitzChain-0.7.1/cli/
+-rw-r--r--   0 jackywong   (501) staff       (20)        0 2023-07-09 14:53:24.000000 BlitzChain-0.7.1/cli/__init__.py
+-rw-r--r--   0 jackywong   (501) staff       (20)      435 2023-07-20 07:06:24.000000 BlitzChain-0.7.1/cli/main.py
+-rw-r--r--   0 jackywong   (501) staff       (20)       38 2023-07-23 12:57:01.229128 BlitzChain-0.7.1/setup.cfg
+-rw-r--r--   0 jackywong   (501) staff       (20)      481 2023-07-20 07:06:24.000000 BlitzChain-0.7.1/setup.py
+drwxr-xr-x   0 jackywong   (501) staff       (20)        0 2023-07-23 12:57:01.228083 BlitzChain-0.7.1/tests/
+-rw-r--r--   0 jackywong   (501) staff       (20)      216 2023-07-20 07:06:24.000000 BlitzChain-0.7.1/tests/test_crud.py
+-rw-r--r--   0 jackywong   (501) staff       (20)      722 2023-07-20 07:06:24.000000 BlitzChain-0.7.1/tests/test_pdf.py
+-rw-r--r--   0 jackywong   (501) staff       (20)      615 2023-07-20 07:06:24.000000 BlitzChain-0.7.1/tests/test_qa.py
```

### Comparing `BlitzChain-0.7.0/LICENSE` & `BlitzChain-0.7.1/LICENSE`

 * *Files identical despite different names*

### Comparing `BlitzChain-0.7.0/README.md` & `BlitzChain-0.7.1/README.md`

 * *Files identical despite different names*

### Comparing `BlitzChain-0.7.0/blitzchain/api.py` & `BlitzChain-0.7.1/blitzchain/api.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,14 +1,16 @@
 """The API behind BlitzChain
 """
 import json
 import base64
 import requests
+import time
 from typing import List, Dict, Any
 from .splitter import WordSplitter
+from .utils import chunk_documents
 
 
 def get_json_response(response):
     try:
         return response.json()
     except Exception as e:
         return response.content
@@ -95,26 +97,43 @@
                 "Content-Type": "application/json",
                 "Authorization": "Bearer " + self.api_key,
             },
             json={"collection": self.collection_name, "object": object},
         )
         return get_json_response(response)
 
-    def update_objects(self, objects: List[Dict]):
+    def update_objects(self, objects: List[Dict], autochunk: bool=True, chunksize: int=20):
         """Update objects"""
-        api_url = self.base_url + "collection/bulk-update"
-        response = requests.post(
-            api_url,
-            headers={
-                "Content-Type": "application/json",
-                "Authorization": "Bearer " + self.api_key,
-            },
-            json={"collection": self.collection_name, "objects": objects},
-        )
-        return get_json_response(response)
+        if autochunk:
+            print("Automatically chunking updating to avoid overloading the server.")
+            for chunk in chunk_documents(objects=objects, chunksize=chunksize):
+                api_url = self.base_url + "collection/bulk-update"
+                response = requests.post(
+                    api_url,
+                    headers={
+                        "Content-Type": "application/json",
+                        "Authorization": "Bearer " + self.api_key,
+                    },
+                    json={"collection": self.collection_name, "objects": chunk},
+                )
+                print(get_json_response(response))
+                time.sleep(3)
+            return
+        else:
+            raise ValueError("Autochunk needs to be set to `true` for now.")
+        # api_url = self.base_url + "collection/bulk-update"
+        # response = requests.post(
+        #     api_url,
+        #     headers={
+        #         "Content-Type": "application/json",
+        #         "Authorization": "Bearer " + self.api_key,
+        #     },
+        #     json={"collection": self.collection_name, "objects": objects},
+        # )
+        # return get_json_response(response)
 
     def insert_html(self, html: str, metadata: dict = None):
         api_url = self.base_url + "collection/insert-html"
         response = requests.post(
             api_url,
             headers={
                 "Content-Type": "application/json",
```

### Comparing `BlitzChain-0.7.0/blitzchain/splitter.py` & `BlitzChain-0.7.1/blitzchain/splitter.py`

 * *Files identical despite different names*

### Comparing `BlitzChain-0.7.0/blitzchain/utils.py` & `BlitzChain-0.7.1/blitzchain/utils.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 """Utility functions for BlitzChain.
 """
 import sys
 
 
-def split_documents(documents, chunksize=20):
+def chunk_documents(documents, chunksize=20):
     for i in range(0, len(documents), chunksize):
         yield documents[i : i + chunksize]
 
 
 def get_size(obj):
     """Recursively finds size of objects"""
     size = sys.getsizeof(obj)
```

### Comparing `BlitzChain-0.7.0/tests/test_pdf.py` & `BlitzChain-0.7.1/tests/test_pdf.py`

 * *Files identical despite different names*

### Comparing `BlitzChain-0.7.0/tests/test_qa.py` & `BlitzChain-0.7.1/tests/test_qa.py`

 * *Files identical despite different names*

