# Comparing `tmp/neuralpit-2.0.8.tar.gz` & `tmp/neuralpit-2.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "neuralpit-2.0.8.tar", last modified: Wed Jul 19 01:17:12 2023, max compression
+gzip compressed data, was "neuralpit-2.0.9.tar", last modified: Thu Jul 20 06:03:37 2023, max compression
```

## Comparing `neuralpit-2.0.8.tar` & `neuralpit-2.0.9.tar`

### file list

```diff
@@ -1,21 +1,21 @@
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-19 01:17:12.989636 neuralpit-2.0.8/
--rw-r--r--   0 root         (0) root         (0)       38 2023-07-19 01:16:43.000000 neuralpit-2.0.8/MANIFEST.in
--rw-r--r--   0 root         (0) root         (0)      632 2023-07-19 01:17:12.989636 neuralpit-2.0.8/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)      242 2023-07-19 01:16:43.000000 neuralpit-2.0.8/README.md
--rw-r--r--   0 root         (0) root         (0)      963 2023-07-19 01:16:43.000000 neuralpit-2.0.8/pyproject.toml
--rw-r--r--   0 root         (0) root         (0)       38 2023-07-19 01:17:12.989636 neuralpit-2.0.8/setup.cfg
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-19 01:17:12.985636 neuralpit-2.0.8/src/
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-19 01:17:12.989636 neuralpit-2.0.8/src/neuralpit/
--rw-r--r--   0 root         (0) root         (0)      586 2023-07-19 01:16:43.000000 neuralpit-2.0.8/src/neuralpit/__init__.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-19 01:17:12.989636 neuralpit-2.0.8/src/neuralpit/services/
--rw-r--r--   0 root         (0) root         (0)        0 2023-07-19 01:16:43.000000 neuralpit-2.0.8/src/neuralpit/services/__init__.py
--rw-r--r--   0 root         (0) root         (0)     3777 2023-07-19 01:16:43.000000 neuralpit-2.0.8/src/neuralpit/services/conversation.py
--rw-r--r--   0 root         (0) root         (0)      571 2023-07-19 01:16:43.000000 neuralpit-2.0.8/src/neuralpit/services/conversion.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-19 01:17:12.989636 neuralpit-2.0.8/src/neuralpit.egg-info/
--rw-r--r--   0 root         (0) root         (0)      632 2023-07-19 01:17:12.000000 neuralpit-2.0.8/src/neuralpit.egg-info/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)      388 2023-07-19 01:17:12.000000 neuralpit-2.0.8/src/neuralpit.egg-info/SOURCES.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-07-19 01:17:12.000000 neuralpit-2.0.8/src/neuralpit.egg-info/dependency_links.txt
--rw-r--r--   0 root         (0) root         (0)       53 2023-07-19 01:17:12.000000 neuralpit-2.0.8/src/neuralpit.egg-info/requires.txt
--rw-r--r--   0 root         (0) root         (0)       10 2023-07-19 01:17:12.000000 neuralpit-2.0.8/src/neuralpit.egg-info/top_level.txt
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-19 01:17:12.989636 neuralpit-2.0.8/test/
--rw-r--r--   0 root         (0) root         (0)      411 2023-07-19 01:16:43.000000 neuralpit-2.0.8/test/testCreateConversation.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-20 06:03:37.973272 neuralpit-2.0.9/
+-rw-r--r--   0 root         (0) root         (0)       38 2023-07-20 06:03:05.000000 neuralpit-2.0.9/MANIFEST.in
+-rw-r--r--   0 root         (0) root         (0)      632 2023-07-20 06:03:37.973272 neuralpit-2.0.9/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)      242 2023-07-20 06:03:05.000000 neuralpit-2.0.9/README.md
+-rw-r--r--   0 root         (0) root         (0)      963 2023-07-20 06:03:05.000000 neuralpit-2.0.9/pyproject.toml
+-rw-r--r--   0 root         (0) root         (0)       38 2023-07-20 06:03:37.973272 neuralpit-2.0.9/setup.cfg
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-20 06:03:37.969272 neuralpit-2.0.9/src/
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-20 06:03:37.969272 neuralpit-2.0.9/src/neuralpit/
+-rw-r--r--   0 root         (0) root         (0)      586 2023-07-20 06:03:05.000000 neuralpit-2.0.9/src/neuralpit/__init__.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-20 06:03:37.973272 neuralpit-2.0.9/src/neuralpit/services/
+-rw-r--r--   0 root         (0) root         (0)        0 2023-07-20 06:03:05.000000 neuralpit-2.0.9/src/neuralpit/services/__init__.py
+-rw-r--r--   0 root         (0) root         (0)     3353 2023-07-20 06:03:05.000000 neuralpit-2.0.9/src/neuralpit/services/conversation.py
+-rw-r--r--   0 root         (0) root         (0)      571 2023-07-20 06:03:05.000000 neuralpit-2.0.9/src/neuralpit/services/conversion.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-20 06:03:37.973272 neuralpit-2.0.9/src/neuralpit.egg-info/
+-rw-r--r--   0 root         (0) root         (0)      632 2023-07-20 06:03:37.000000 neuralpit-2.0.9/src/neuralpit.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)      388 2023-07-20 06:03:37.000000 neuralpit-2.0.9/src/neuralpit.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-07-20 06:03:37.000000 neuralpit-2.0.9/src/neuralpit.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)       53 2023-07-20 06:03:37.000000 neuralpit-2.0.9/src/neuralpit.egg-info/requires.txt
+-rw-r--r--   0 root         (0) root         (0)       10 2023-07-20 06:03:37.000000 neuralpit-2.0.9/src/neuralpit.egg-info/top_level.txt
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-20 06:03:37.973272 neuralpit-2.0.9/test/
+-rw-r--r--   0 root         (0) root         (0)      411 2023-07-20 06:03:05.000000 neuralpit-2.0.9/test/testCreateConversation.py
```

### Comparing `neuralpit-2.0.8/pyproject.toml` & `neuralpit-2.0.9/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 
 [build-system]
 requires      = ["setuptools>=61.0.0", "wheel"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "neuralpit"
-version = "2.0.8"
+version = "2.0.9"
 description = "NeuralPit SDK"
 readme = "README.md"
 authors = [{ name = "Quang Nguyen", email = "quang.nguyen@neuralpit.com" }]
 license = { file = "LICENSE" }
 classifiers = [
     "License :: OSI Approved :: MIT License",
     "Programming Language :: Python",
```

### Comparing `neuralpit-2.0.8/src/neuralpit/__init__.py` & `neuralpit-2.0.9/src/neuralpit/__init__.py`

 * *Files identical despite different names*

### Comparing `neuralpit-2.0.8/src/neuralpit/services/conversation.py` & `neuralpit-2.0.9/src/neuralpit/services/conversation.py`

 * *Files 5% similar despite different names*

```diff
@@ -23,29 +23,21 @@
     
     def deleteConversation(self, conversation_id):
         delete_url = urljoin(self.api_endpoint,f'/conversation/{conversation_id}')
         headers = {'x-api-key':self.api_key, 'Content-Type':'application/json'}
         delete_call = requests.delete(delete_url, headers = headers)
         return True
     
-    def addConversationDocumentFromNeuralPitStorage(self, conversation_id, bucket, keys:List[str]):
-        post_url = urljoin(self.api_endpoint,f'/conversation/{conversation_id}/neuralpit_platform_file')
+    def addConversationDocumentFromS3(self, conversation_id, bucket, keys:List[str]):
+        post_url = urljoin(self.api_endpoint,f'/conversation/{conversation_id}/s3_document')
         headers = {'x-api-key':self.api_key, 'Content-Type':'application/json'}
         post_call = requests.post(post_url, headers = headers, json = [{'bucket': bucket, 'key': key} for key in keys])
         resp =  json.loads(post_call.content)
         return resp
     
-    def addConversationDocumentFromLocalFile(self, conversation_id, file):
-        post_url = urljoin(self.api_endpoint,f'/conversation/{conversation_id}/local_file')
-        headers = {'x-api-key':self.api_key}
-        upload_files = {'file':(file.name,file)}
-        post_call = requests.post(post_url, files = upload_files)
-        resp =  json.loads(post_call.content)
-        return resp
-    
     def deleteConversationDocument(self, conversation_id, document_id):
         delete_url = urljoin(self.api_endpoint,f'/conversation/{conversation_id}/document/{document_id}')
         headers = {'x-api-key':self.api_key, 'Content-Type':'application/json'}
         delete_call = requests.delete(delete_url, headers = headers)
         return True
     
     def listConversationDocument(self, conversation_id):
```

### Comparing `neuralpit-2.0.8/src/neuralpit/services/conversion.py` & `neuralpit-2.0.9/src/neuralpit/services/conversion.py`

 * *Files identical despite different names*

