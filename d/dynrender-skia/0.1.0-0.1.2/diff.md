# Comparing `tmp/dynrender_skia-0.1.0.tar.gz` & `tmp/dynrender_skia-0.1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dynrender_skia-0.1.0.tar", max compression
+gzip compressed data, was "dynrender_skia-0.1.2.tar", max compression
```

## Comparing `dynrender_skia-0.1.0.tar` & `dynrender_skia-0.1.2.tar`

### file list

```diff
@@ -1,15 +1,15 @@
--rw-r--r--   0        0        0    35149 2023-07-18 04:51:58.303257 dynrender_skia-0.1.0/LICENSE
--rw-r--r--   0        0        0     1501 2023-07-23 04:08:01.780776 dynrender_skia-0.1.0/README.md
--rw-r--r--   0        0        0     2225 2023-07-23 03:58:50.724582 dynrender_skia-0.1.0/dynrender_skia/Core.py
--rw-r--r--   0        0        0    18382 2023-07-23 03:58:50.724582 dynrender_skia-0.1.0/dynrender_skia/DynAdditional.py
--rw-r--r--   0        0        0     5499 2023-07-23 03:58:50.724582 dynrender_skia-0.1.0/dynrender_skia/DynConfig.py
--rw-r--r--   0        0        0    11153 2023-07-23 03:58:50.724582 dynrender_skia-0.1.0/dynrender_skia/DynHeader.py
--rw-r--r--   0        0        0    28444 2023-07-23 03:58:50.724582 dynrender_skia-0.1.0/dynrender_skia/DynMajor.py
--rw-r--r--   0        0        0     1204 2023-07-23 03:58:50.724582 dynrender_skia-0.1.0/dynrender_skia/DynRepost.py
--rw-r--r--   0        0        0      849 2023-07-23 03:58:50.728582 dynrender_skia-0.1.0/dynrender_skia/DynStyle.py
--rw-r--r--   0        0        0    12798 2023-07-23 03:58:50.728582 dynrender_skia-0.1.0/dynrender_skia/DynText.py
--rw-r--r--   0        0        0     4084 2023-07-23 03:58:50.728582 dynrender_skia-0.1.0/dynrender_skia/DynTools.py
--rw-r--r--   0        0        0   334112 2023-07-18 04:51:58.303257 dynrender_skia-0.1.0/dynrender_skia/Static.zip
--rw-r--r--   0        0        0        0 2023-07-18 04:51:58.303257 dynrender_skia-0.1.0/dynrender_skia/__init__.py
--rw-r--r--   0        0        0      519 2023-07-23 03:58:50.732582 dynrender_skia-0.1.0/pyproject.toml
--rw-r--r--   0        0        0     2218 1970-01-01 00:00:00.000000 dynrender_skia-0.1.0/PKG-INFO
+-rw-r--r--   0        0        0    35149 2023-07-23 04:40:30.049036 dynrender_skia-0.1.2/LICENSE
+-rw-r--r--   0        0        0     1501 2023-07-23 04:40:30.049036 dynrender_skia-0.1.2/README.md
+-rw-r--r--   0        0        0     2225 2023-07-23 04:40:30.049036 dynrender_skia-0.1.2/dynrender_skia/Core.py
+-rw-r--r--   0        0        0    18382 2023-07-23 04:40:30.049036 dynrender_skia-0.1.2/dynrender_skia/DynAdditional.py
+-rw-r--r--   0        0        0     5499 2023-07-23 04:40:30.049036 dynrender_skia-0.1.2/dynrender_skia/DynConfig.py
+-rw-r--r--   0        0        0    11153 2023-07-23 04:40:30.049036 dynrender_skia-0.1.2/dynrender_skia/DynHeader.py
+-rw-r--r--   0        0        0    28444 2023-07-23 04:40:30.049036 dynrender_skia-0.1.2/dynrender_skia/DynMajor.py
+-rw-r--r--   0        0        0     1204 2023-07-23 04:40:30.049036 dynrender_skia-0.1.2/dynrender_skia/DynRepost.py
+-rw-r--r--   0        0        0      849 2023-07-23 04:40:30.049036 dynrender_skia-0.1.2/dynrender_skia/DynStyle.py
+-rw-r--r--   0        0        0    12798 2023-07-23 04:40:30.049036 dynrender_skia-0.1.2/dynrender_skia/DynText.py
+-rw-r--r--   0        0        0     4084 2023-07-23 04:40:30.049036 dynrender_skia-0.1.2/dynrender_skia/DynTools.py
+-rw-r--r--   0        0        0   334112 2023-07-23 04:40:30.049036 dynrender_skia-0.1.2/dynrender_skia/Static.zip
+-rw-r--r--   0        0        0        0 2023-07-23 04:40:30.049036 dynrender_skia-0.1.2/dynrender_skia/__init__.py
+-rw-r--r--   0        0        0      519 2023-07-23 04:40:30.053036 dynrender_skia-0.1.2/pyproject.toml
+-rw-r--r--   0        0        0     2218 1970-01-01 00:00:00.000000 dynrender_skia-0.1.2/PKG-INFO
```

### Comparing `dynrender_skia-0.1.0/LICENSE` & `dynrender_skia-0.1.2/LICENSE`

 * *Files identical despite different names*

### Comparing `dynrender_skia-0.1.0/README.md` & `dynrender_skia-0.1.2/README.md`

 * *Files identical despite different names*

### Comparing `dynrender_skia-0.1.0/dynrender_skia/Core.py` & `dynrender_skia-0.1.2/dynrender_skia/Core.py`

 * *Files identical despite different names*

### Comparing `dynrender_skia-0.1.0/dynrender_skia/DynAdditional.py` & `dynrender_skia-0.1.2/dynrender_skia/DynAdditional.py`

 * *Files identical despite different names*

### Comparing `dynrender_skia-0.1.0/dynrender_skia/DynConfig.py` & `dynrender_skia-0.1.2/dynrender_skia/DynConfig.py`

 * *Files identical despite different names*

### Comparing `dynrender_skia-0.1.0/dynrender_skia/DynHeader.py` & `dynrender_skia-0.1.2/dynrender_skia/DynHeader.py`

 * *Files identical despite different names*

### Comparing `dynrender_skia-0.1.0/dynrender_skia/DynMajor.py` & `dynrender_skia-0.1.2/dynrender_skia/DynMajor.py`

 * *Files identical despite different names*

### Comparing `dynrender_skia-0.1.0/dynrender_skia/DynRepost.py` & `dynrender_skia-0.1.2/dynrender_skia/DynRepost.py`

 * *Files identical despite different names*

### Comparing `dynrender_skia-0.1.0/dynrender_skia/DynStyle.py` & `dynrender_skia-0.1.2/dynrender_skia/DynStyle.py`

 * *Files identical despite different names*

### Comparing `dynrender_skia-0.1.0/dynrender_skia/DynText.py` & `dynrender_skia-0.1.2/dynrender_skia/DynText.py`

 * *Files identical despite different names*

### Comparing `dynrender_skia-0.1.0/dynrender_skia/DynTools.py` & `dynrender_skia-0.1.2/dynrender_skia/DynTools.py`

 * *Files identical despite different names*

### Comparing `dynrender_skia-0.1.0/dynrender_skia/Static.zip` & `dynrender_skia-0.1.2/dynrender_skia/Static.zip`

 * *Files identical despite different names*

### Comparing `dynrender_skia-0.1.0/pyproject.toml` & `dynrender_skia-0.1.2/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "dynrender-skia"
-version = "0.1.0"
+version = "0.1.2"
 description = "使用skia-python将BiliBili动态渲染为图片"
 authors = ["DMC <lzxder@outlook.com>"]
 license = "GNU GPLv3"
 readme = "README.md"
 packages = [{include = "dynrender_skia"}]
 
 [tool.poetry.dependencies]
```

### Comparing `dynrender_skia-0.1.0/PKG-INFO` & `dynrender_skia-0.1.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dynrender-skia
-Version: 0.1.0
+Version: 0.1.2
 Summary: 使用skia-python将BiliBili动态渲染为图片
 License: GNU GPLv3
 Author: DMC
 Author-email: lzxder@outlook.com
 Requires-Python: >=3.8,<4.0
 Classifier: License :: Other/Proprietary License
 Classifier: Programming Language :: Python :: 3
```

