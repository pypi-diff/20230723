# Comparing `tmp/pyquizrd-0.1.3.tar.gz` & `tmp/pyquizrd-0.1.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyquizrd-0.1.3.tar", max compression
+gzip compressed data, was "pyquizrd-0.1.4.tar", max compression
```

## Comparing `pyquizrd-0.1.3.tar` & `pyquizrd-0.1.4.tar`

### file list

```diff
@@ -1,20 +1,20 @@
--rw-r--r--   0        0        0       98 2023-07-23 10:34:43.549162 pyquizrd-0.1.3/README.md
--rw-r--r--   0        0        0      425 2023-07-23 11:31:21.973996 pyquizrd-0.1.3/pyproject.toml
--rw-r--r--   0        0        0        0 2023-07-22 17:17:17.006420 pyquizrd-0.1.3/pyquizrd/__init__.py
--rw-r--r--   0        0        0        0 2023-07-22 18:11:49.069651 pyquizrd-0.1.3/pyquizrd/gpt/__init__.py
--rw-r--r--   0        0        0     2241 2023-07-23 10:33:53.547156 pyquizrd-0.1.3/pyquizrd/gpt/gpt.py
--rw-r--r--   0        0        0     1651 2023-07-23 09:59:48.550229 pyquizrd-0.1.3/pyquizrd/gpt/prompt.txt
--rw-r--r--   0        0        0      155 2023-07-23 10:00:37.082356 pyquizrd-0.1.3/pyquizrd/gpt/x.py
--rw-r--r--   0        0        0        0 2023-07-22 18:26:18.049474 pyquizrd-0.1.3/pyquizrd/jeopardy/__init__.py
--rw-r--r--   0        0        0     1551 2023-07-23 10:34:17.787420 pyquizrd-0.1.3/pyquizrd/jeopardy/jeopardy.py
--rw-r--r--   0        0        0  5256096 2023-07-22 18:26:18.051795 pyquizrd-0.1.3/pyquizrd/jeopardy/pruned_jeopardy.json
--rw-r--r--   0        0        0  1922867 2023-07-22 18:27:06.494033 pyquizrd-0.1.3/pyquizrd/jeopardy/pruned_jeopardy.json.Z
--rw-r--r--   0        0        0        0 2023-07-22 18:11:51.787936 pyquizrd-0.1.3/pyquizrd/manual/__init__.py
--rw-r--r--   0        0        0      480 2023-07-22 19:34:54.128923 pyquizrd-0.1.3/pyquizrd/manual/manual.py
--rw-r--r--   0        0        0        0 2023-07-22 18:11:54.929318 pyquizrd-0.1.3/pyquizrd/opentrivia/__init__.py
--rw-r--r--   0        0        0     1919 2023-07-22 19:26:29.744147 pyquizrd-0.1.3/pyquizrd/opentrivia/opentrivia.py
--rw-r--r--   0        0        0        0 2023-07-22 18:11:58.225280 pyquizrd-0.1.3/pyquizrd/palm/__init__.py
--rw-r--r--   0        0        0     1810 2023-07-23 11:30:40.102376 pyquizrd-0.1.3/pyquizrd/palm/palm.py
--rw-r--r--   0        0        0     1651 2023-07-22 17:28:49.452163 pyquizrd-0.1.3/pyquizrd/palm/prompt.txt
--rw-r--r--   0        0        0     1429 2023-07-23 10:33:33.092773 pyquizrd-0.1.3/pyquizrd/pyquizrd.py
--rw-r--r--   0        0        0      430 1970-01-01 00:00:00.000000 pyquizrd-0.1.3/PKG-INFO
+-rw-r--r--   0        0        0       98 2023-07-23 10:34:43.549162 pyquizrd-0.1.4/README.md
+-rw-r--r--   0        0        0      425 2023-07-23 11:42:18.689285 pyquizrd-0.1.4/pyproject.toml
+-rw-r--r--   0        0        0        0 2023-07-22 17:17:17.006420 pyquizrd-0.1.4/pyquizrd/__init__.py
+-rw-r--r--   0        0        0        0 2023-07-22 18:11:49.069651 pyquizrd-0.1.4/pyquizrd/gpt/__init__.py
+-rw-r--r--   0        0        0     2241 2023-07-23 10:33:53.547156 pyquizrd-0.1.4/pyquizrd/gpt/gpt.py
+-rw-r--r--   0        0        0     1651 2023-07-23 09:59:48.550229 pyquizrd-0.1.4/pyquizrd/gpt/prompt.txt
+-rw-r--r--   0        0        0      155 2023-07-23 10:00:37.082356 pyquizrd-0.1.4/pyquizrd/gpt/x.py
+-rw-r--r--   0        0        0        0 2023-07-22 18:26:18.049474 pyquizrd-0.1.4/pyquizrd/jeopardy/__init__.py
+-rw-r--r--   0        0        0     1551 2023-07-23 10:34:17.787420 pyquizrd-0.1.4/pyquizrd/jeopardy/jeopardy.py
+-rw-r--r--   0        0        0  5256096 2023-07-22 18:26:18.051795 pyquizrd-0.1.4/pyquizrd/jeopardy/pruned_jeopardy.json
+-rw-r--r--   0        0        0  1922867 2023-07-22 18:27:06.494033 pyquizrd-0.1.4/pyquizrd/jeopardy/pruned_jeopardy.json.Z
+-rw-r--r--   0        0        0        0 2023-07-22 18:11:51.787936 pyquizrd-0.1.4/pyquizrd/manual/__init__.py
+-rw-r--r--   0        0        0      480 2023-07-22 19:34:54.128923 pyquizrd-0.1.4/pyquizrd/manual/manual.py
+-rw-r--r--   0        0        0        0 2023-07-22 18:11:54.929318 pyquizrd-0.1.4/pyquizrd/opentrivia/__init__.py
+-rw-r--r--   0        0        0     1919 2023-07-22 19:26:29.744147 pyquizrd-0.1.4/pyquizrd/opentrivia/opentrivia.py
+-rw-r--r--   0        0        0        0 2023-07-22 18:11:58.225280 pyquizrd-0.1.4/pyquizrd/palm/__init__.py
+-rw-r--r--   0        0        0     1903 2023-07-23 11:41:55.637430 pyquizrd-0.1.4/pyquizrd/palm/palm.py
+-rw-r--r--   0        0        0     1651 2023-07-22 17:28:49.452163 pyquizrd-0.1.4/pyquizrd/palm/prompt.txt
+-rw-r--r--   0        0        0     1429 2023-07-23 10:33:33.092773 pyquizrd-0.1.4/pyquizrd/pyquizrd.py
+-rw-r--r--   0        0        0      430 1970-01-01 00:00:00.000000 pyquizrd-0.1.4/PKG-INFO
```

### Comparing `pyquizrd-0.1.3/pyquizrd/gpt/gpt.py` & `pyquizrd-0.1.4/pyquizrd/gpt/gpt.py`

 * *Files identical despite different names*

### Comparing `pyquizrd-0.1.3/pyquizrd/gpt/prompt.txt` & `pyquizrd-0.1.4/pyquizrd/gpt/prompt.txt`

 * *Files identical despite different names*

### Comparing `pyquizrd-0.1.3/pyquizrd/jeopardy/jeopardy.py` & `pyquizrd-0.1.4/pyquizrd/jeopardy/jeopardy.py`

 * *Files identical despite different names*

### Comparing `pyquizrd-0.1.3/pyquizrd/jeopardy/pruned_jeopardy.json` & `pyquizrd-0.1.4/pyquizrd/jeopardy/pruned_jeopardy.json`

 * *Files identical despite different names*

### Comparing `pyquizrd-0.1.3/pyquizrd/jeopardy/pruned_jeopardy.json.Z` & `pyquizrd-0.1.4/pyquizrd/jeopardy/pruned_jeopardy.json.Z`

 * *Files identical despite different names*

### Comparing `pyquizrd-0.1.3/pyquizrd/opentrivia/opentrivia.py` & `pyquizrd-0.1.4/pyquizrd/opentrivia/opentrivia.py`

 * *Files identical despite different names*

### Comparing `pyquizrd-0.1.3/pyquizrd/palm/palm.py` & `pyquizrd-0.1.4/pyquizrd/palm/palm.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,21 +1,23 @@
 import json
 import pprint
 import google.generativeai as palm
+import importlib
 import os
 import random
 import vertexai
 from vertexai.preview.language_models import TextGenerationModel
 
 class Quizgen:
     def __init__(self, project="quizrd-prod-382117", location="us-central1"):
         self.topics = set()
         vertexai.init(project=project, location=location)
-        print("cwd:", os.getcwd())
-        self.prompt = open("palm/prompt.txt").read()
+        data_path = os.path.join(os.path.dirname(__file__), "prompt.txt")
+        with open(data_path, encoding='utf-8') as fp:
+            self.prompt = fp.read()
 
     def __str__(self):
         return "palm quiz generator"
 
     def get_topics(self, num=None):
         return self.topics
```

### Comparing `pyquizrd-0.1.3/pyquizrd/palm/prompt.txt` & `pyquizrd-0.1.4/pyquizrd/palm/prompt.txt`

 * *Files identical despite different names*

### Comparing `pyquizrd-0.1.3/pyquizrd/pyquizrd.py` & `pyquizrd-0.1.4/pyquizrd/pyquizrd.py`

 * *Files identical despite different names*

