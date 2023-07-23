# Comparing `tmp/transformers_js_py-0.1.3.tar.gz` & `tmp/transformers_js_py-0.1.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "transformers_js_py-0.1.3.tar", max compression
+gzip compressed data, was "transformers_js_py-0.1.4.tar", max compression
```

## Comparing `transformers_js_py-0.1.3.tar` & `transformers_js_py-0.1.4.tar`

### file list

```diff
@@ -1,5 +1,5 @@
--rw-r--r--   0        0        0    11357 2023-07-22 07:03:28.528284 transformers_js_py-0.1.3/LICENSE
--rw-r--r--   0        0        0       21 2023-07-22 07:03:28.528284 transformers_js_py-0.1.3/README.md
--rw-r--r--   0        0        0      579 2023-07-22 07:03:28.528284 transformers_js_py-0.1.3/pyproject.toml
--rw-r--r--   0        0        0     2442 2023-07-22 07:03:28.528284 transformers_js_py-0.1.3/transformers_js/__init__.py
--rw-r--r--   0        0        0      468 1970-01-01 00:00:00.000000 transformers_js_py-0.1.3/PKG-INFO
+-rw-r--r--   0        0        0    11357 2023-07-23 00:11:09.181570 transformers_js_py-0.1.4/LICENSE
+-rw-r--r--   0        0        0       21 2023-07-23 00:11:09.181570 transformers_js_py-0.1.4/README.md
+-rw-r--r--   0        0        0      579 2023-07-23 00:11:09.181570 transformers_js_py-0.1.4/pyproject.toml
+-rw-r--r--   0        0        0     2536 2023-07-23 00:11:09.181570 transformers_js_py-0.1.4/transformers_js/__init__.py
+-rw-r--r--   0        0        0      468 1970-01-01 00:00:00.000000 transformers_js_py-0.1.4/PKG-INFO
```

### Comparing `transformers_js_py-0.1.3/LICENSE` & `transformers_js_py-0.1.4/LICENSE`

 * *Files identical despite different names*

### Comparing `transformers_js_py-0.1.3/pyproject.toml` & `transformers_js_py-0.1.4/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "transformers-js-py"
-version = "0.1.3"
+version = "0.1.4"
 description = ""
 authors = ["Yuichiro Tachibana (Tsuchiya) <t.yic.yt@gmail.com>"]
 license = "Apache-2.0"
 readme = "README.md"
 packages = [{include = "transformers_js"}]
 
 [tool.poetry.dependencies]
```

### Comparing `transformers_js_py-0.1.3/transformers_js/__init__.py` & `transformers_js_py-0.1.4/transformers_js/__init__.py`

 * *Files 7% similar despite different names*

```diff
@@ -59,15 +59,16 @@
     return obj
 
 
 async def import_transformers_js():
     pyodide.code.run_js(
         """
     async function loadTransformersJs() {
-        const transformers = await import('https://cdn.jsdelivr.net/npm/@xenova/transformers@2.4.1');
+        const isBrowser = typeof window !== 'undefined';
+        const transformers = await import(isBrowser ? 'https://cdn.jsdelivr.net/npm/@xenova/transformers@2.4.2' : '@xenova/transformers');
 
         transformers.env.allowLocalModels = false;
 
         globalThis._transformers = {  // Convert a module to an object.
             ...transformers,
         };
     }
```

