# Comparing `tmp/fastllm-0.1.0.tar.gz` & `tmp/fastllm-0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "fastllm-0.1.0.tar", max compression
+gzip compressed data, was "fastllm-0.1.1.tar", max compression
```

## Comparing `fastllm-0.1.0.tar` & `fastllm-0.1.1.tar`

### file list

```diff
@@ -1,8 +1,7 @@
--rw-r--r--   0        0        0    11357 2023-07-16 18:54:36.878631 fastllm-0.1.0/LICENSE
--rw-r--r--   0        0        0     1217 2023-07-17 15:28:18.737939 fastllm-0.1.0/README.md
--rw-r--r--   0        0        0      137 2023-07-16 19:41:58.634805 fastllm-0.1.0/fastllm/__init__.py
--rw-r--r--   0        0        0    13832 2023-07-17 15:26:32.541329 fastllm-0.1.0/fastllm/base.py
--rw-r--r--   0        0        0     1768 2023-07-16 19:48:56.141261 fastllm-0.1.0/fastllm/utils.py
--rw-r--r--   0        0        0      996 2023-07-17 15:26:54.065445 fastllm-0.1.0/pyproject.toml
--rw-r--r--   0        0        0     2013 1970-01-01 00:00:00.000000 fastllm-0.1.0/setup.py
--rw-r--r--   0        0        0     1807 1970-01-01 00:00:00.000000 fastllm-0.1.0/PKG-INFO
+-rw-r--r--   0        0        0    11357 2023-07-16 18:54:36.878631 fastllm-0.1.1/LICENSE
+-rw-r--r--   0        0        0     4120 2023-07-23 15:50:40.782536 fastllm-0.1.1/README.md
+-rw-r--r--   0        0        0      137 2023-07-23 15:51:19.906944 fastllm-0.1.1/fastllm/__init__.py
+-rw-r--r--   0        0        0    20280 2023-07-23 15:51:15.498897 fastllm-0.1.1/fastllm/base.py
+-rw-r--r--   0        0        0     1443 2023-07-23 15:50:48.598612 fastllm-0.1.1/pyproject.toml
+-rw-r--r--   0        0        0     5028 1970-01-01 00:00:00.000000 fastllm-0.1.1/setup.py
+-rw-r--r--   0        0        0     5153 1970-01-01 00:00:00.000000 fastllm-0.1.1/PKG-INFO
```

### Comparing `fastllm-0.1.0/LICENSE` & `fastllm-0.1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `fastllm-0.1.0/pyproject.toml` & `fastllm-0.1.1/pyproject.toml`

 * *Files 22% similar despite different names*

```diff
@@ -1,49 +1,61 @@
 [tool.poetry]
 name = "fastllm"
-version = "0.1.0"
+version = "0.1.1"
 description = "Fast and easy wrapper around LLMs."
 authors = ["Clemens Kriechbaumer <clemens.kriechbaumer@gmail.com>"]
 readme = "README.md"
 license = "Apache-2.0"
 homepage = "https://github.com/clemens33/fastllm"
+repository = "https://github.com/clemens33/fastllm"
+keywords = ["agents", "chatbots", "openai", "llm"]
+classifiers = [
+    "Development Status :: 2 - Pre-Alpha",
+
+    'Programming Language :: Python :: 3',
+    'Programming Language :: Python :: 3.10',
+    'Programming Language :: Python :: 3.11',
+    'Programming Language :: Python :: 3.12',
+]
 packages = [{ include = "fastllm" }]
 
 [tool.poetry.dependencies]
-python = "^3.11"
-openai = "^0.27.8"
+python = "^3.10"
 jinja2 = "^3.1.2"
 backoff = "^2.2.1"
+openai = "^0.27.8"
+jsonschema = "^4.18.4"
 
 [tool.poetry.group.dev.dependencies]
 ruff = "^0.0.278"
 black = "^23.7.0"
 pyright = "^1.1.317"
 pytest = "^7.4.0"
+pytest-cov = "^4.1.0"
+python-dotenv = "^1.0.0"
 
 [build-system]
 requires = ["poetry-core"]
 build-backend = "poetry.core.masonry.api"
 
 [tool.ruff]
-line-length = 88
-select = ["D", "F"]
+select = ["E", "W", "F", "D", "N"]
 ignore = ["D202"]
-target-version = "py311"
+target-version = "py310"
 
 [tool.ruff.pydocstyle]
 convention = "google"
-ignore-decorators = ["D202"]
 
 [tool.black]
-line-length = 88
+target-version = ["py310", "py311", "py312"]
 
 [tool.pyright]
-pythonVersion = "3.11"
+pythonVersion = "3.10"
 typeCheckingMode = "basic"
 
 [tool.pytest.ini_options]
 log_cli = true
 log_cli_level = "INFO"
-markers = [    
-    "openai: mark tests requiring openai api key",
-]
+markers = ["openai: mark tests requiring openai api key"]
+
+[tool.coverage.report]
+show_missing = true
```

