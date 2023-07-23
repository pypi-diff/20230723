# Comparing `tmp/autopack_tools-0.3.1.tar.gz` & `tmp/autopack_tools-0.3.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "autopack_tools-0.3.1.tar", max compression
+gzip compressed data, was "autopack_tools-0.3.2.tar", max compression
```

## Comparing `autopack_tools-0.3.1.tar` & `autopack_tools-0.3.2.tar`

### file list

```diff
@@ -1,19 +1,19 @@
--rw-r--r--   0        0        0     1069 2023-06-25 23:21:07.938011 autopack_tools-0.3.1/LICENSE
--rw-r--r--   0        0        0     2862 2023-07-02 21:31:24.435654 autopack_tools-0.3.1/README.md
--rw-r--r--   0        0        0        6 2023-06-25 23:21:01.956323 autopack_tools-0.3.1/autopack/VERSION
--rw-r--r--   0        0        0       51 2023-07-22 21:10:26.696185 autopack_tools-0.3.1/autopack/__init__.py
--rw-r--r--   0        0        0      134 2023-06-25 23:21:01.956609 autopack_tools-0.3.1/autopack/__main__.py
--rw-r--r--   0        0        0     2869 2023-07-23 21:13:30.082198 autopack_tools-0.3.1/autopack/api.py
--rw-r--r--   0        0        0     1091 2023-07-22 21:45:58.090041 autopack_tools-0.3.1/autopack/cli.py
--rw-r--r--   0        0        0      317 2023-07-22 20:36:24.222128 autopack_tools-0.3.1/autopack/errors.py
--rw-r--r--   0        0        0     2568 2023-07-23 01:25:16.569309 autopack_tools-0.3.1/autopack/get_pack.py
--rw-r--r--   0        0        0     3935 2023-07-23 04:34:40.466812 autopack_tools-0.3.1/autopack/installation.py
--rw-r--r--   0        0        0     5029 2023-07-23 20:21:14.829622 autopack_tools-0.3.1/autopack/pack.py
--rw-r--r--   0        0        0      252 2023-07-22 21:40:46.525129 autopack_tools-0.3.1/autopack/pack_response.py
--rw-r--r--   0        0        0      393 2023-07-22 23:02:14.133585 autopack_tools-0.3.1/autopack/pack_search_response.py
--rw-r--r--   0        0        0     2217 2023-07-22 21:58:39.610211 autopack_tools-0.3.1/autopack/prompts.py
--rw-r--r--   0        0        0      394 2023-07-22 23:03:16.870292 autopack_tools-0.3.1/autopack/search.py
--rw-r--r--   0        0        0     3604 2023-07-23 21:07:17.383625 autopack_tools-0.3.1/autopack/selection.py
--rw-r--r--   0        0        0     7904 2023-07-23 05:25:55.315020 autopack_tools-0.3.1/autopack/utils.py
--rw-r--r--   0        0        0     1080 2023-07-23 21:13:44.586806 autopack_tools-0.3.1/pyproject.toml
--rw-r--r--   0        0        0     3709 1970-01-01 00:00:00.000000 autopack_tools-0.3.1/PKG-INFO
+-rw-r--r--   0        0        0     1069 2023-06-25 23:21:07.938011 autopack_tools-0.3.2/LICENSE
+-rw-r--r--   0        0        0     2862 2023-07-02 21:31:24.435654 autopack_tools-0.3.2/README.md
+-rw-r--r--   0        0        0        6 2023-06-25 23:21:01.956323 autopack_tools-0.3.2/autopack/VERSION
+-rw-r--r--   0        0        0       51 2023-07-22 21:10:26.696185 autopack_tools-0.3.2/autopack/__init__.py
+-rw-r--r--   0        0        0      134 2023-06-25 23:21:01.956609 autopack_tools-0.3.2/autopack/__main__.py
+-rw-r--r--   0        0        0     2869 2023-07-23 21:13:30.082198 autopack_tools-0.3.2/autopack/api.py
+-rw-r--r--   0        0        0     1091 2023-07-22 21:45:58.090041 autopack_tools-0.3.2/autopack/cli.py
+-rw-r--r--   0        0        0      317 2023-07-22 20:36:24.222128 autopack_tools-0.3.2/autopack/errors.py
+-rw-r--r--   0        0        0     2568 2023-07-23 01:25:16.569309 autopack_tools-0.3.2/autopack/get_pack.py
+-rw-r--r--   0        0        0     3935 2023-07-23 04:34:40.466812 autopack_tools-0.3.2/autopack/installation.py
+-rw-r--r--   0        0        0     5029 2023-07-23 20:21:14.829622 autopack_tools-0.3.2/autopack/pack.py
+-rw-r--r--   0        0        0      276 2023-07-23 21:19:00.939247 autopack_tools-0.3.2/autopack/pack_response.py
+-rw-r--r--   0        0        0      393 2023-07-22 23:02:14.133585 autopack_tools-0.3.2/autopack/pack_search_response.py
+-rw-r--r--   0        0        0     2217 2023-07-22 21:58:39.610211 autopack_tools-0.3.2/autopack/prompts.py
+-rw-r--r--   0        0        0      394 2023-07-22 23:03:16.870292 autopack_tools-0.3.2/autopack/search.py
+-rw-r--r--   0        0        0     3604 2023-07-23 21:07:17.383625 autopack_tools-0.3.2/autopack/selection.py
+-rw-r--r--   0        0        0     7904 2023-07-23 05:25:55.315020 autopack_tools-0.3.2/autopack/utils.py
+-rw-r--r--   0        0        0     1080 2023-07-23 21:21:04.533722 autopack_tools-0.3.2/pyproject.toml
+-rw-r--r--   0        0        0     3709 1970-01-01 00:00:00.000000 autopack_tools-0.3.2/PKG-INFO
```

### Comparing `autopack_tools-0.3.1/LICENSE` & `autopack_tools-0.3.2/LICENSE`

 * *Files identical despite different names*

### Comparing `autopack_tools-0.3.1/README.md` & `autopack_tools-0.3.2/README.md`

 * *Files identical despite different names*

### Comparing `autopack_tools-0.3.1/autopack/api.py` & `autopack_tools-0.3.2/autopack/api.py`

 * *Files identical despite different names*

### Comparing `autopack_tools-0.3.1/autopack/cli.py` & `autopack_tools-0.3.2/autopack/cli.py`

 * *Files identical despite different names*

### Comparing `autopack_tools-0.3.1/autopack/get_pack.py` & `autopack_tools-0.3.2/autopack/get_pack.py`

 * *Files identical despite different names*

### Comparing `autopack_tools-0.3.1/autopack/installation.py` & `autopack_tools-0.3.2/autopack/installation.py`

 * *Files identical despite different names*

### Comparing `autopack_tools-0.3.1/autopack/pack.py` & `autopack_tools-0.3.2/autopack/pack.py`

 * *Files identical despite different names*

### Comparing `autopack_tools-0.3.1/autopack/prompts.py` & `autopack_tools-0.3.2/autopack/prompts.py`

 * *Files identical despite different names*

### Comparing `autopack_tools-0.3.1/autopack/selection.py` & `autopack_tools-0.3.2/autopack/selection.py`

 * *Files identical despite different names*

### Comparing `autopack_tools-0.3.1/autopack/utils.py` & `autopack_tools-0.3.2/autopack/utils.py`

 * *Files identical despite different names*

### Comparing `autopack_tools-0.3.1/pyproject.toml` & `autopack_tools-0.3.2/pyproject.toml`

 * *Files 11% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "autopack-tools"
-version = "0.3.1"
+version = "0.3.2"
 repository = "https://github.com/AutoPackAI/autopack"
 homepage = "https://autopack.ai"
 description = "Package Manager for AI Agent tools"
 authors = ["Erik Peterson <e@eriklp.com>"]
 license = "MIT"
 readme = "README.md"
 packages = [{ include = "autopack" }]
```

### Comparing `autopack_tools-0.3.1/PKG-INFO` & `autopack_tools-0.3.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: autopack-tools
-Version: 0.3.1
+Version: 0.3.2
 Summary: Package Manager for AI Agent tools
 Home-page: https://autopack.ai
 License: MIT
 Author: Erik Peterson
 Author-email: e@eriklp.com
 Requires-Python: >=3.8.1,<4.0
 Classifier: License :: OSI Approved :: MIT License
```

