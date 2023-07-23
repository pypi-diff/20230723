# Comparing `tmp/openai_functools-0.2.30.tar.gz` & `tmp/openai_functools-0.2.33.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "openai_functools-0.2.30.tar", max compression
+gzip compressed data, was "openai_functools-0.2.33.tar", max compression
```

## Comparing `openai_functools-0.2.30.tar` & `openai_functools-0.2.33.tar`

### file list

```diff
@@ -1,8 +1,8 @@
--rw-r--r--   0        0        0     1070 2023-07-21 14:54:30.947704 openai_functools-0.2.30/LICENSE
--rw-r--r--   0        0        0     3868 2023-07-21 14:54:30.947704 openai_functools-0.2.30/README.md
--rw-r--r--   0        0        0      195 2023-07-21 14:54:30.947704 openai_functools-0.2.30/openai_functools/__init__.py
--rw-r--r--   0        0        0     1755 2023-07-21 14:54:30.947704 openai_functools-0.2.30/openai_functools/metadata_generator.py
--rw-r--r--   0        0        0      470 2023-07-21 14:54:30.947704 openai_functools-0.2.30/openai_functools/types.py
--rw-r--r--   0        0        0     2318 2023-07-21 14:54:30.947704 openai_functools-0.2.30/openai_functools/utils/openai_service.py
--rw-r--r--   0        0        0      537 2023-07-21 14:54:51.739959 openai_functools-0.2.30/pyproject.toml
--rw-r--r--   0        0        0     4515 1970-01-01 00:00:00.000000 openai_functools-0.2.30/PKG-INFO
+-rw-r--r--   0        0        0     1070 2023-07-23 08:39:00.924455 openai_functools-0.2.33/LICENSE
+-rw-r--r--   0        0        0     3916 2023-07-23 08:39:00.924455 openai_functools-0.2.33/README.md
+-rw-r--r--   0        0        0      195 2023-07-23 08:39:00.928455 openai_functools-0.2.33/openai_functools/__init__.py
+-rw-r--r--   0        0        0     1755 2023-07-23 08:39:00.928455 openai_functools-0.2.33/openai_functools/metadata_generator.py
+-rw-r--r--   0        0        0      470 2023-07-23 08:39:00.928455 openai_functools-0.2.33/openai_functools/types.py
+-rw-r--r--   0        0        0     2318 2023-07-23 08:39:00.928455 openai_functools-0.2.33/openai_functools/utils/openai_service.py
+-rw-r--r--   0        0        0      537 2023-07-23 08:39:30.412744 openai_functools-0.2.33/pyproject.toml
+-rw-r--r--   0        0        0     4563 1970-01-01 00:00:00.000000 openai_functools-0.2.33/PKG-INFO
```

### Comparing `openai_functools-0.2.30/LICENSE` & `openai_functools-0.2.33/LICENSE`

 * *Files identical despite different names*

### Comparing `openai_functools-0.2.30/README.md` & `openai_functools-0.2.33/README.md`

 * *Files 1% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# openai-functools
+# [openai-functools](https://github.com/Jakob-98/openai-functools)
 
 `openai-functools` is a Python library designed to enhance the functionality of OpenAI's 1 `gpt-3.5-turbo-0613` and `gpt-4-0613` models for function calling. This library focuses on generating the required JSON automatically by wrapping existing Python functions in our decorator. This removes the need for you to manually create and manage the JSON structures required for function calling in these models.
 
 ## Installation
 
 This package is hosted on PyPI and can be installed with pip:
```

### Comparing `openai_functools-0.2.30/openai_functools/metadata_generator.py` & `openai_functools-0.2.33/openai_functools/metadata_generator.py`

 * *Files identical despite different names*

### Comparing `openai_functools-0.2.30/openai_functools/utils/openai_service.py` & `openai_functools-0.2.33/openai_functools/utils/openai_service.py`

 * *Files identical despite different names*

### Comparing `openai_functools-0.2.30/pyproject.toml` & `openai_functools-0.2.33/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "openai_functools"
-version = "0.2.30"
+version = "0.2.33"
 description = "python openai functions tooling"
 authors = ["Jakob Serlier <37184788+Jakob-98@users.noreply.github.com>", "Marc van Duyn <codingkitties@gmail.com>"]
 readme = "README.md"
 packages = [{include = "openai_functools"}]
 
 [tool.poetry.dependencies]
 python = "^3.10"
```

### Comparing `openai_functools-0.2.30/PKG-INFO` & `openai_functools-0.2.33/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: openai-functools
-Version: 0.2.30
+Version: 0.2.33
 Summary: python openai functions tooling
 Author: Jakob Serlier
 Author-email: 37184788+Jakob-98@users.noreply.github.com
 Requires-Python: >=3.10,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
@@ -12,15 +12,15 @@
 Requires-Dist: docstring-parser (>=0.15,<0.16)
 Requires-Dist: flake8 (>=6.0.0,<7.0.0)
 Requires-Dist: isort (>=5.12.0,<6.0.0)
 Requires-Dist: openai (>=0.27.8,<0.28.0)
 Requires-Dist: pytest (>=7.4.0,<8.0.0)
 Description-Content-Type: text/markdown
 
-# openai-functools
+# [openai-functools](https://github.com/Jakob-98/openai-functools)
 
 `openai-functools` is a Python library designed to enhance the functionality of OpenAI's 1 `gpt-3.5-turbo-0613` and `gpt-4-0613` models for function calling. This library focuses on generating the required JSON automatically by wrapping existing Python functions in our decorator. This removes the need for you to manually create and manage the JSON structures required for function calling in these models.
 
 ## Installation
 
 This package is hosted on PyPI and can be installed with pip:
```

