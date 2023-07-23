# Comparing `tmp/factool-0.0.8.tar.gz` & `tmp/factool-0.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "factool-0.0.8.tar", last modified: Sat Jul 15 08:05:51 2023, max compression
+gzip compressed data, was "factool-0.1.0.tar", last modified: Sun Jul 23 04:42:24 2023, max compression
```

## Comparing `factool-0.0.8.tar` & `factool-0.1.0.tar`

### file list

```diff
@@ -1,52 +1,53 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-15 08:05:51.091860 factool-0.0.8/
--rw-r--r--   0 runner    (1001) docker     (123)      141 2023-07-15 08:05:10.000000 factool-0.0.8/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)    18079 2023-07-15 08:05:51.091860 factool-0.0.8/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)    17448 2023-07-15 08:05:10.000000 factool-0.0.8/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-15 08:05:51.091860 factool-0.0.8/factool/
--rw-r--r--   0 runner    (1001) docker     (123)       35 2023-07-15 08:05:10.000000 factool-0.0.8/factool/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-15 08:05:51.091860 factool-0.0.8/factool/code/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-15 08:05:10.000000 factool-0.0.8/factool/code/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-15 08:05:51.091860 factool-0.0.8/factool/code/helper/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-15 08:05:10.000000 factool-0.0.8/factool/code/helper/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     8271 2023-07-15 08:05:10.000000 factool-0.0.8/factool/code/helper/_execution.py
--rw-r--r--   0 runner    (1001) docker     (123)     1696 2023-07-15 08:05:10.000000 factool-0.0.8/factool/code/helper/execution.py
--rw-r--r--   0 runner    (1001) docker     (123)      705 2023-07-15 08:05:10.000000 factool-0.0.8/factool/code/helper/io_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     1345 2023-07-15 08:05:10.000000 factool-0.0.8/factool/code/helper/postprocess.py
--rw-r--r--   0 runner    (1001) docker     (123)    12954 2023-07-15 08:05:10.000000 factool-0.0.8/factool/code/pipeline.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-15 08:05:10.000000 factool-0.0.8/factool/code/tool.py
--rw-r--r--   0 runner    (1001) docker     (123)      638 2023-07-15 08:05:10.000000 factool-0.0.8/factool/env_config.py
--rw-r--r--   0 runner    (1001) docker     (123)     3739 2023-07-15 08:05:10.000000 factool-0.0.8/factool/factool.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-15 08:05:51.091860 factool-0.0.8/factool/knowledge_qa/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-15 08:05:10.000000 factool-0.0.8/factool/knowledge_qa/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4132 2023-07-15 08:05:10.000000 factool-0.0.8/factool/knowledge_qa/google_serper.py
--rw-r--r--   0 runner    (1001) docker     (123)     9940 2023-07-15 08:05:10.000000 factool-0.0.8/factool/knowledge_qa/pipeline.py
--rw-r--r--   0 runner    (1001) docker     (123)      283 2023-07-15 08:05:10.000000 factool-0.0.8/factool/knowledge_qa/tool.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-15 08:05:51.091860 factool-0.0.8/factool/math/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-15 08:05:10.000000 factool-0.0.8/factool/math/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     9075 2023-07-15 08:05:10.000000 factool-0.0.8/factool/math/pipeline.py
--rw-r--r--   0 runner    (1001) docker     (123)     1065 2023-07-15 08:05:10.000000 factool-0.0.8/factool/math/tool.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-15 08:05:51.091860 factool-0.0.8/factool/scientific/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-15 08:05:10.000000 factool-0.0.8/factool/scientific/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    10730 2023-07-15 08:05:10.000000 factool-0.0.8/factool/scientific/pipeline.py
--rw-r--r--   0 runner    (1001) docker     (123)      644 2023-07-15 08:05:10.000000 factool-0.0.8/factool/scientific/tool.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-15 08:05:51.091860 factool-0.0.8/factool/utils/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-15 08:05:10.000000 factool-0.0.8/factool/utils/__init_.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-15 08:05:51.091860 factool-0.0.8/factool/utils/base/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-15 08:05:10.000000 factool-0.0.8/factool/utils/base/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      632 2023-07-15 08:05:10.000000 factool-0.0.8/factool/utils/base/pipeline.py
--rw-r--r--   0 runner    (1001) docker     (123)     2742 2023-07-15 08:05:10.000000 factool-0.0.8/factool/utils/claim_extractor.py
--rw-r--r--   0 runner    (1001) docker     (123)     4277 2023-07-15 08:05:10.000000 factool-0.0.8/factool/utils/openai_wrapper.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-15 08:05:51.091860 factool-0.0.8/factool/utils/prompts/
--rw-r--r--   0 runner    (1001) docker     (123)     2716 2023-07-15 08:05:10.000000 factool-0.0.8/factool/utils/prompts/agreement_verification.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     5656 2023-07-15 08:05:10.000000 factool-0.0.8/factool/utils/prompts/claim_extraction.yaml
--rw-r--r--   0 runner    (1001) docker     (123)     5543 2023-07-15 08:05:10.000000 factool-0.0.8/factool/utils/prompts/query_generation.yaml
--rw-r--r--   0 runner    (1001) docker     (123)    19200 2023-07-15 08:05:10.000000 factool-0.0.8/factool/utils/prompts/self_check.yaml
--rw-r--r--   0 runner    (1001) docker     (123)      367 2023-07-15 08:05:10.000000 factool-0.0.8/factool/utils/utils_json.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-15 08:05:51.091860 factool-0.0.8/factool.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)    18079 2023-07-15 08:05:51.000000 factool-0.0.8/factool.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1141 2023-07-15 08:05:51.000000 factool-0.0.8/factool.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-15 08:05:51.000000 factool-0.0.8/factool.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      143 2023-07-15 08:05:51.000000 factool-0.0.8/factool.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        8 2023-07-15 08:05:51.000000 factool-0.0.8/factool.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)     1293 2023-07-15 08:05:51.095860 factool-0.0.8/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)       73 2023-07-15 08:05:10.000000 factool-0.0.8/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:42:24.141682 factool-0.1.0/
+-rw-r--r--   0 runner    (1001) docker     (123)      141 2023-07-23 04:41:39.000000 factool-0.1.0/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)    31412 2023-07-23 04:42:24.141682 factool-0.1.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    30781 2023-07-23 04:41:39.000000 factool-0.1.0/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:42:24.137682 factool-0.1.0/factool/
+-rw-r--r--   0 runner    (1001) docker     (123)       70 2023-07-23 04:41:39.000000 factool-0.1.0/factool/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:42:24.137682 factool-0.1.0/factool/code/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 04:41:39.000000 factool-0.1.0/factool/code/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:42:24.137682 factool-0.1.0/factool/code/helper/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 04:41:39.000000 factool-0.1.0/factool/code/helper/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8300 2023-07-23 04:41:39.000000 factool-0.1.0/factool/code/helper/_execution.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1696 2023-07-23 04:41:39.000000 factool-0.1.0/factool/code/helper/execution.py
+-rw-r--r--   0 runner    (1001) docker     (123)      705 2023-07-23 04:41:39.000000 factool-0.1.0/factool/code/helper/io_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1345 2023-07-23 04:41:39.000000 factool-0.1.0/factool/code/helper/postprocess.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12954 2023-07-23 04:41:39.000000 factool-0.1.0/factool/code/pipeline.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 04:41:39.000000 factool-0.1.0/factool/code/tool.py
+-rw-r--r--   0 runner    (1001) docker     (123)      638 2023-07-23 04:41:39.000000 factool-0.1.0/factool/env_config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5154 2023-07-23 04:41:39.000000 factool-0.1.0/factool/factool.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:42:24.137682 factool-0.1.0/factool/knowledge_qa/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 04:41:39.000000 factool-0.1.0/factool/knowledge_qa/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4132 2023-07-23 04:41:39.000000 factool-0.1.0/factool/knowledge_qa/google_serper.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9940 2023-07-23 04:41:39.000000 factool-0.1.0/factool/knowledge_qa/pipeline.py
+-rw-r--r--   0 runner    (1001) docker     (123)      283 2023-07-23 04:41:39.000000 factool-0.1.0/factool/knowledge_qa/tool.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:42:24.137682 factool-0.1.0/factool/math/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 04:41:39.000000 factool-0.1.0/factool/math/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9075 2023-07-23 04:41:39.000000 factool-0.1.0/factool/math/pipeline.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1065 2023-07-23 04:41:39.000000 factool-0.1.0/factool/math/tool.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:42:24.141682 factool-0.1.0/factool/scientific/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 04:41:39.000000 factool-0.1.0/factool/scientific/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10730 2023-07-23 04:41:39.000000 factool-0.1.0/factool/scientific/pipeline.py
+-rw-r--r--   0 runner    (1001) docker     (123)      793 2023-07-23 04:41:39.000000 factool-0.1.0/factool/scientific/tool.py
+-rw-r--r--   0 runner    (1001) docker     (123)      475 2023-07-23 04:41:39.000000 factool-0.1.0/factool/tasks.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:42:24.141682 factool-0.1.0/factool/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 04:41:39.000000 factool-0.1.0/factool/utils/__init_.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:42:24.141682 factool-0.1.0/factool/utils/base/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 04:41:39.000000 factool-0.1.0/factool/utils/base/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      632 2023-07-23 04:41:39.000000 factool-0.1.0/factool/utils/base/pipeline.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2742 2023-07-23 04:41:39.000000 factool-0.1.0/factool/utils/claim_extractor.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4425 2023-07-23 04:41:39.000000 factool-0.1.0/factool/utils/openai_wrapper.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:42:24.141682 factool-0.1.0/factool/utils/prompts/
+-rw-r--r--   0 runner    (1001) docker     (123)     2716 2023-07-23 04:41:39.000000 factool-0.1.0/factool/utils/prompts/agreement_verification.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     5656 2023-07-23 04:41:39.000000 factool-0.1.0/factool/utils/prompts/claim_extraction.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)     5543 2023-07-23 04:41:39.000000 factool-0.1.0/factool/utils/prompts/query_generation.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)    19200 2023-07-23 04:41:39.000000 factool-0.1.0/factool/utils/prompts/self_check.yaml
+-rw-r--r--   0 runner    (1001) docker     (123)      367 2023-07-23 04:41:39.000000 factool-0.1.0/factool/utils/utils_json.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:42:24.137682 factool-0.1.0/factool.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)    31412 2023-07-23 04:42:24.000000 factool-0.1.0/factool.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1158 2023-07-23 04:42:24.000000 factool-0.1.0/factool.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 04:42:24.000000 factool-0.1.0/factool.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      143 2023-07-23 04:42:24.000000 factool-0.1.0/factool.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        8 2023-07-23 04:42:24.000000 factool-0.1.0/factool.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1293 2023-07-23 04:42:24.141682 factool-0.1.0/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)       73 2023-07-23 04:41:39.000000 factool-0.1.0/setup.py
```

### Comparing `factool-0.0.8/factool/code/helper/_execution.py` & `factool-0.1.0/factool/code/helper/_execution.py`

 * *Files 2% similar despite different names*

```diff
@@ -69,16 +69,15 @@
                  "    return \"\".join([chr(((ord(ch)"
                  " + 5 - ord(\"a\")) % 26) + ord(\"a\")) for ch in s])\n\n\n"]
             for helper in helper_funcs_to_be_included:
                 if helper in prompt:
                     helper_func = helper
 
             check_program = (
-                prompt[:import_packages_end_index]
-                + helper_func + completion + "\n" + f'result = {test}'
+                (prompt[:import_packages_end_index] if import_packages_end_index != -1 else "") + helper_func + completion + "\n" + f'result = {test}'
             )
 
             try:
                 exec_globals = {}
                 with swallow_io():
                     with time_limit(timeout):
                         exec(check_program, exec_globals)
```

### Comparing `factool-0.0.8/factool/code/helper/execution.py` & `factool-0.1.0/factool/code/helper/execution.py`

 * *Files identical despite different names*

### Comparing `factool-0.0.8/factool/code/helper/io_utils.py` & `factool-0.1.0/factool/code/helper/io_utils.py`

 * *Files identical despite different names*

### Comparing `factool-0.0.8/factool/code/helper/postprocess.py` & `factool-0.1.0/factool/code/helper/postprocess.py`

 * *Files identical despite different names*

### Comparing `factool-0.0.8/factool/code/pipeline.py` & `factool-0.1.0/factool/code/pipeline.py`

 * *Files identical despite different names*

### Comparing `factool-0.0.8/factool/env_config.py` & `factool-0.1.0/factool/env_config.py`

 * *Files identical despite different names*

### Comparing `factool-0.0.8/factool/knowledge_qa/google_serper.py` & `factool-0.1.0/factool/knowledge_qa/google_serper.py`

 * *Files identical despite different names*

### Comparing `factool-0.0.8/factool/knowledge_qa/pipeline.py` & `factool-0.1.0/factool/knowledge_qa/pipeline.py`

 * *Files identical despite different names*

### Comparing `factool-0.0.8/factool/math/pipeline.py` & `factool-0.1.0/factool/math/pipeline.py`

 * *Files identical despite different names*

### Comparing `factool-0.0.8/factool/math/tool.py` & `factool-0.1.0/factool/math/tool.py`

 * *Files identical despite different names*

### Comparing `factool-0.0.8/factool/scientific/pipeline.py` & `factool-0.1.0/factool/scientific/pipeline.py`

 * *Files identical despite different names*

### Comparing `factool-0.0.8/factool/scientific/tool.py` & `factool-0.1.0/factool/scientific/tool.py`

 * *Files 21% similar despite different names*

```diff
@@ -12,11 +12,14 @@
     def __init__(self):
         pg = ProxyGenerator()
         if scraper_api_key is not None:
             success = pg.ScraperAPI(scraper_api_key)
             scholarly.use_proxy(pg)
 
     def run(self, query):
-        results = scholarly.search_pubs(query)
-        paper_info = next(results)
-        paper_info_subset = {key: paper_info['bib'][key] for key in ['title', 'author', 'pub_year']}
-        return paper_info_subset
+        try:
+            results = scholarly.search_pubs(query)
+            paper_info = next(results)
+            paper_info_subset = {key: paper_info['bib'][key] for key in ['title', 'author', 'pub_year']}
+            return paper_info_subset
+        except StopIteration:
+            return {'title': "no match!", "author": "no match!", "pub_year": "no match!"}
```

### Comparing `factool-0.0.8/factool/utils/base/pipeline.py` & `factool-0.1.0/factool/utils/base/pipeline.py`

 * *Files identical despite different names*

### Comparing `factool-0.0.8/factool/utils/claim_extractor.py` & `factool-0.1.0/factool/utils/claim_extractor.py`

 * *Files identical despite different names*

### Comparing `factool-0.0.8/factool/utils/openai_wrapper.py` & `factool-0.1.0/factool/utils/openai_wrapper.py`

 * *Files 4% similar despite different names*

```diff
@@ -15,16 +15,29 @@
 
 from factool.env_config import factool_env_config
 
 # env
 openai.api_key = factool_env_config.openai_api_key
 
 class OpenAIChat():
-    def __init__(self, model_name='gpt-3.5-turbo', max_tokens=2500, temperature=0.5, top_p=1, request_timeout=60):
-        self.config = {'model_name': model_name, 'max_tokens': max_tokens, 'temperature': temperature, 'top_p': top_p, 'request_timeout': request_timeout}
+    def __init__(
+            self,
+            model_name='gpt-3.5-turbo',
+            max_tokens=2500,
+            temperature=0,
+            top_p=1,
+            request_timeout=60,
+    ):
+        self.config = {
+            'model_name': model_name,
+            'max_tokens': max_tokens,
+            'temperature': temperature,
+            'top_p': top_p,
+            'request_timeout': request_timeout,
+        }
 
     
     def _boolean_fix(self, output):
         return output.replace("true", "True").replace("false", "False")
 
     def _type_check(self, output, expected_type):
         try:
```

### Comparing `factool-0.0.8/factool/utils/prompts/agreement_verification.yaml` & `factool-0.1.0/factool/utils/prompts/agreement_verification.yaml`

 * *Files identical despite different names*

### Comparing `factool-0.0.8/factool/utils/prompts/claim_extraction.yaml` & `factool-0.1.0/factool/utils/prompts/claim_extraction.yaml`

 * *Files identical despite different names*

### Comparing `factool-0.0.8/factool/utils/prompts/query_generation.yaml` & `factool-0.1.0/factool/utils/prompts/query_generation.yaml`

 * *Files identical despite different names*

### Comparing `factool-0.0.8/factool/utils/prompts/self_check.yaml` & `factool-0.1.0/factool/utils/prompts/self_check.yaml`

 * *Files identical despite different names*

### Comparing `factool-0.0.8/factool.egg-info/SOURCES.txt` & `factool-0.1.0/factool.egg-info/SOURCES.txt`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,15 @@
 MANIFEST.in
 README.md
 setup.cfg
 setup.py
 factool/__init__.py
 factool/env_config.py
 factool/factool.py
+factool/tasks.py
 factool.egg-info/PKG-INFO
 factool.egg-info/SOURCES.txt
 factool.egg-info/dependency_links.txt
 factool.egg-info/requires.txt
 factool.egg-info/top_level.txt
 factool/code/__init__.py
 factool/code/pipeline.py
```

### Comparing `factool-0.0.8/setup.cfg` & `factool-0.1.0/setup.cfg`

 * *Files identical despite different names*

