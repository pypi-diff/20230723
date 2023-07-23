# Comparing `tmp/cybrex-1.0.8.tar.gz` & `tmp/cybrex-1.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "cybrex-1.0.8.tar", last modified: Sun Jul 23 17:53:43 2023, max compression
+gzip compressed data, was "cybrex-1.0.9.tar", last modified: Sun Jul 23 17:55:39 2023, max compression
```

## Comparing `cybrex-1.0.8.tar` & `cybrex-1.0.9.tar`

### file list

```diff
@@ -1,19 +1,19 @@
-drwxr-xr-x   0 pasha      (501) staff       (20)        0 2023-07-23 17:53:43.687547 cybrex-1.0.8/
--rw-r--r--   0 pasha      (501) staff       (20)       24 2022-12-01 11:19:40.000000 cybrex-1.0.8/MANIFEST.in
--rw-r--r--   0 pasha      (501) staff       (20)     1479 2023-07-23 17:53:43.687350 cybrex-1.0.8/PKG-INFO
--rw-r--r--   0 pasha      (501) staff       (20)     1203 2023-07-23 17:52:09.000000 cybrex-1.0.8/README.md
-drwxr-xr-x   0 pasha      (501) staff       (20)        0 2023-07-23 17:53:43.685376 cybrex-1.0.8/cybrex/
--rw-r--r--   0 pasha      (501) staff       (20)        0 2023-07-12 12:59:05.000000 cybrex-1.0.8/cybrex/__init__.py
--rw-r--r--   0 pasha      (501) staff       (20)     4683 2023-07-20 13:00:27.000000 cybrex-1.0.8/cybrex/cli.py
--rw-r--r--   0 pasha      (501) staff       (20)     8204 2023-07-23 16:52:45.000000 cybrex-1.0.8/cybrex/cybrex_ai.py
--rw-r--r--   0 pasha      (501) staff       (20)     3187 2023-07-23 16:54:13.000000 cybrex-1.0.8/cybrex/models.py
-drwxr-xr-x   0 pasha      (501) staff       (20)        0 2023-07-23 17:53:43.687059 cybrex-1.0.8/cybrex.egg-info/
--rw-r--r--   0 pasha      (501) staff       (20)     1479 2023-07-23 17:53:43.000000 cybrex-1.0.8/cybrex.egg-info/PKG-INFO
--rw-r--r--   0 pasha      (501) staff       (20)      305 2023-07-23 17:53:43.000000 cybrex-1.0.8/cybrex.egg-info/SOURCES.txt
--rw-r--r--   0 pasha      (501) staff       (20)        1 2023-07-23 17:53:43.000000 cybrex-1.0.8/cybrex.egg-info/dependency_links.txt
--rw-r--r--   0 pasha      (501) staff       (20)       43 2023-07-23 17:53:43.000000 cybrex-1.0.8/cybrex.egg-info/entry_points.txt
--rw-r--r--   0 pasha      (501) staff       (20)      182 2023-07-23 17:53:43.000000 cybrex-1.0.8/cybrex.egg-info/requires.txt
--rw-r--r--   0 pasha      (501) staff       (20)        7 2023-07-23 17:53:43.000000 cybrex-1.0.8/cybrex.egg-info/top_level.txt
--rw-r--r--   0 pasha      (501) staff       (20)      531 2023-07-23 17:50:41.000000 cybrex-1.0.8/pyproject.toml
--rw-r--r--   0 pasha      (501) staff       (20)      182 2023-07-19 20:14:47.000000 cybrex-1.0.8/requirements.txt
--rw-r--r--   0 pasha      (501) staff       (20)       38 2023-07-23 17:53:43.687667 cybrex-1.0.8/setup.cfg
+drwxr-xr-x   0 pasha      (501) staff       (20)        0 2023-07-23 17:55:39.759788 cybrex-1.0.9/
+-rw-r--r--   0 pasha      (501) staff       (20)       24 2022-12-01 11:19:40.000000 cybrex-1.0.9/MANIFEST.in
+-rw-r--r--   0 pasha      (501) staff       (20)     1479 2023-07-23 17:55:39.759548 cybrex-1.0.9/PKG-INFO
+-rw-r--r--   0 pasha      (501) staff       (20)     1203 2023-07-23 17:52:09.000000 cybrex-1.0.9/README.md
+drwxr-xr-x   0 pasha      (501) staff       (20)        0 2023-07-23 17:55:39.757233 cybrex-1.0.9/cybrex/
+-rw-r--r--   0 pasha      (501) staff       (20)        0 2023-07-12 12:59:05.000000 cybrex-1.0.9/cybrex/__init__.py
+-rw-r--r--   0 pasha      (501) staff       (20)     4685 2023-07-23 17:55:11.000000 cybrex-1.0.9/cybrex/cli.py
+-rw-r--r--   0 pasha      (501) staff       (20)     8231 2023-07-23 17:55:13.000000 cybrex-1.0.9/cybrex/cybrex_ai.py
+-rw-r--r--   0 pasha      (501) staff       (20)     3213 2023-07-23 17:55:13.000000 cybrex-1.0.9/cybrex/models.py
+drwxr-xr-x   0 pasha      (501) staff       (20)        0 2023-07-23 17:55:39.759129 cybrex-1.0.9/cybrex.egg-info/
+-rw-r--r--   0 pasha      (501) staff       (20)     1479 2023-07-23 17:55:39.000000 cybrex-1.0.9/cybrex.egg-info/PKG-INFO
+-rw-r--r--   0 pasha      (501) staff       (20)      305 2023-07-23 17:55:39.000000 cybrex-1.0.9/cybrex.egg-info/SOURCES.txt
+-rw-r--r--   0 pasha      (501) staff       (20)        1 2023-07-23 17:55:39.000000 cybrex-1.0.9/cybrex.egg-info/dependency_links.txt
+-rw-r--r--   0 pasha      (501) staff       (20)       43 2023-07-23 17:55:39.000000 cybrex-1.0.9/cybrex.egg-info/entry_points.txt
+-rw-r--r--   0 pasha      (501) staff       (20)      182 2023-07-23 17:55:39.000000 cybrex-1.0.9/cybrex.egg-info/requires.txt
+-rw-r--r--   0 pasha      (501) staff       (20)        7 2023-07-23 17:55:39.000000 cybrex-1.0.9/cybrex.egg-info/top_level.txt
+-rw-r--r--   0 pasha      (501) staff       (20)      531 2023-07-23 17:55:23.000000 cybrex-1.0.9/pyproject.toml
+-rw-r--r--   0 pasha      (501) staff       (20)      182 2023-07-19 20:14:47.000000 cybrex-1.0.9/requirements.txt
+-rw-r--r--   0 pasha      (501) staff       (20)       38 2023-07-23 17:55:39.759935 cybrex-1.0.9/setup.cfg
```

### Comparing `cybrex-1.0.8/PKG-INFO` & `cybrex-1.0.9/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cybrex
-Version: 1.0.8
+Version: 1.0.9
 Summary: Researching AI
 Author: Interdimensional Walker
 Project-URL: Homepage, https://github.com/nexus-stc/stc
 Classifier: Programming Language :: Python :: 3.8
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
```

### Comparing `cybrex-1.0.8/README.md` & `cybrex-1.0.9/README.md`

 * *Files identical despite different names*

### Comparing `cybrex-1.0.8/cybrex/cli.py` & `cybrex-1.0.9/cybrex/cli.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,16 +1,17 @@
 import json
 import logging
 import sys
 import textwrap
 
 import fire
-from cybrex_ai import CybrexAI
 from termcolor import colored
 
+from .cybrex_ai import CybrexAI
+
 
 def create_snippet(document, metadata):
     return metadata['doi'] + ': ' + document
 
 
 class CybrexCli:
     def __init__(self):
```

### Comparing `cybrex-1.0.8/cybrex/cybrex_ai.py` & `cybrex-1.0.9/cybrex/cybrex_ai.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,15 @@
 import io
 import logging
 import os.path
 import uuid
-from typing import List, Optional
+from typing import (
+    List,
+    Optional,
+)
 
 import chromadb
 import pypdf
 import yaml
 from aiokit import AioThing
 from izihawa_configurator import Configurator
 from izihawa_utils.exceptions import BaseError
@@ -14,15 +17,18 @@
 from langchain.chains import RetrievalQA
 from langchain.chains.summarize import load_summarize_chain
 from langchain.schema import Document
 from langchain.vectorstores import Chroma
 from stc_geck.advices import get_documents_on_topic
 from stc_geck.client import StcGeck
 
-from models import OpenAIModel, models_dict
+from .models import (
+    OpenAIModel,
+    models_dict,
+)
 
 
 class DocumentNotFoundError(BaseError):
     pass
 
 
 def print_color(text, color):
```

### Comparing `cybrex-1.0.8/cybrex/models.py` & `cybrex-1.0.9/cybrex/models.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,12 +1,18 @@
 from ctransformers.langchain import CTransformers
 from keybert import KeyBERT
-from langchain import OpenAI, PromptTemplate
+from langchain import (
+    OpenAI,
+    PromptTemplate,
+)
 from langchain.chains import RetrievalQA
-from langchain.embeddings import HuggingFaceInstructEmbeddings, OpenAIEmbeddings
+from langchain.embeddings import (
+    HuggingFaceInstructEmbeddings,
+    OpenAIEmbeddings,
+)
 from langchain.text_splitter import RecursiveCharacterTextSplitter
 from lazy import lazy
 
 wizardlm_question_prompt = """
 A chat between a curious user and an artificial intelligence assistant.
 If assistant doesn't know the answer, it says that he doesn't know and doesn't try to make up an answer.
 Assistant can use the following pieces of context to answer the question.
```

### Comparing `cybrex-1.0.8/cybrex.egg-info/PKG-INFO` & `cybrex-1.0.9/cybrex.egg-info/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cybrex
-Version: 1.0.8
+Version: 1.0.9
 Summary: Researching AI
 Author: Interdimensional Walker
 Project-URL: Homepage, https://github.com/nexus-stc/stc
 Classifier: Programming Language :: Python :: 3.8
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
```

### Comparing `cybrex-1.0.8/pyproject.toml` & `cybrex-1.0.9/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools<65.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "cybrex"
-version = "1.0.8"
+version = "1.0.9"
 authors = [{ name = "Interdimensional Walker" }]
 description = "Researching AI"
 readme = "README.md"
 requires-python = ">=3.8"
 classifiers = [
     "Programming Language :: Python :: 3.8",
 ]
```

