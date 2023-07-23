# Comparing `tmp/dup_hawk-0.0.6.tar.gz` & `tmp/dup_hawk-0.0.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dup_hawk-0.0.6.tar", max compression
+gzip compressed data, was "dup_hawk-0.0.7.tar", max compression
```

## Comparing `dup_hawk-0.0.6.tar` & `dup_hawk-0.0.7.tar`

### file list

```diff
@@ -1,7 +1,7 @@
--rw-r--r--   0        0        0     1059 2023-07-23 18:19:25.010552 dup_hawk-0.0.6/LICENSE
--rw-r--r--   0        0        0     1208 2023-07-23 18:19:25.010552 dup_hawk-0.0.6/README.md
--rw-r--r--   0        0        0      126 2023-07-23 18:19:25.010552 dup_hawk-0.0.6/dup_hawk/__init__.py
--rw-r--r--   0        0        0     4370 2023-07-23 18:19:25.010552 dup_hawk-0.0.6/dup_hawk/dup_hawk.py
--rw-r--r--   0        0        0     2475 2023-07-23 18:19:25.010552 dup_hawk-0.0.6/dup_hawk/github.py
--rw-r--r--   0        0        0      667 2023-07-23 18:19:25.010552 dup_hawk-0.0.6/pyproject.toml
--rw-r--r--   0        0        0     2044 1970-01-01 00:00:00.000000 dup_hawk-0.0.6/PKG-INFO
+-rw-r--r--   0        0        0     1059 2023-07-23 18:21:31.109104 dup_hawk-0.0.7/LICENSE
+-rw-r--r--   0        0        0     1246 2023-07-23 18:21:31.109104 dup_hawk-0.0.7/README.md
+-rw-r--r--   0        0        0      126 2023-07-23 18:21:31.109104 dup_hawk-0.0.7/dup_hawk/__init__.py
+-rw-r--r--   0        0        0     4405 2023-07-23 18:21:31.109104 dup_hawk-0.0.7/dup_hawk/dup_hawk.py
+-rw-r--r--   0        0        0     2475 2023-07-23 18:21:31.109104 dup_hawk-0.0.7/dup_hawk/github.py
+-rw-r--r--   0        0        0      667 2023-07-23 18:21:31.109104 dup_hawk-0.0.7/pyproject.toml
+-rw-r--r--   0        0        0     2082 1970-01-01 00:00:00.000000 dup_hawk-0.0.7/PKG-INFO
```

### Comparing `dup_hawk-0.0.6/LICENSE` & `dup_hawk-0.0.7/LICENSE`

 * *Files identical despite different names*

### Comparing `dup_hawk-0.0.6/README.md` & `dup_hawk-0.0.7/README.md`

 * *Files 4% similar despite different names*

```diff
@@ -31,14 +31,19 @@
 cd dup-hawk
 pip install . -e
 ```
 
 ## Quickstart 
 
 ```
+dup-hawk --help
+```
+will output:
+
+```
 
 ```
 
 # Tests
 
 ```
 poetry run pytest
```

### Comparing `dup_hawk-0.0.6/dup_hawk/dup_hawk.py` & `dup_hawk-0.0.7/dup_hawk/dup_hawk.py`

 * *Files 8% similar despite different names*

```diff
@@ -37,20 +37,20 @@
     default=None,
     required=True,
     help="GitHub repo URL that you want to mark duplicate issues for.",
 )
 @click.option(
     "--git-pat-token",
     default=os.getenv("GITHUB_PAT_TOKEN"),
-    help="GitHub repo URL that you want to mark duplicate issues for.",
+    help="GitHub PAT token of the github user that will be marking the issues.",
 )
 @click.option(
     "--openai-api-key",
     default=os.getenv("OPENAI_API_KEY"),
-    help="OpenAI API key.",
+    help="OpenAI API key for generating embeddings.",
 )
 def dup_hawk_click(git_repo_url: str, git_pat_token: str, openai_api_key: str):
     dup_hawk(git_repo_url, git_pat_token, openai_api_key)
 
 
 def dup_hawk(git_repo_url: str, git_pat_token: str, openai_api_key: str):
     openai.key = openai_api_key
```

### Comparing `dup_hawk-0.0.6/dup_hawk/github.py` & `dup_hawk-0.0.7/dup_hawk/github.py`

 * *Files identical despite different names*

### Comparing `dup_hawk-0.0.6/pyproject.toml` & `dup_hawk-0.0.7/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "dup-hawk"
-version = "0.0.6"
+version = "0.0.7"
 description = "Python CLI for marking duplicates submissions on GitHub."
 authors = ["PatrickAlphac <54278053+PatrickAlphaC@users.noreply.github.com>"]
 readme = "README.md"
 packages = [{include = "dup_hawk"}]
 
 [tool.poetry.dependencies]
 python = ">=3.10,<3.13"
```

### Comparing `dup_hawk-0.0.6/PKG-INFO` & `dup_hawk-0.0.7/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dup-hawk
-Version: 0.0.6
+Version: 0.0.7
 Summary: Python CLI for marking duplicates submissions on GitHub.
 Author: PatrickAlphac
 Author-email: 54278053+PatrickAlphaC@users.noreply.github.com
 Requires-Python: >=3.10,<3.13
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
@@ -53,14 +53,19 @@
 cd dup-hawk
 pip install . -e
 ```
 
 ## Quickstart 
 
 ```
+dup-hawk --help
+```
+will output:
+
+```
 
 ```
 
 # Tests
 
 ```
 poetry run pytest
```

