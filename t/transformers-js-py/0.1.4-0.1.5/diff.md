# Comparing `tmp/transformers_js_py-0.1.4.tar.gz` & `tmp/transformers_js_py-0.1.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "transformers_js_py-0.1.4.tar", max compression
+gzip compressed data, was "transformers_js_py-0.1.5.tar", max compression
```

## Comparing `transformers_js_py-0.1.4.tar` & `transformers_js_py-0.1.5.tar`

### file list

```diff
@@ -1,5 +1,5 @@
--rw-r--r--   0        0        0    11357 2023-07-23 00:11:09.181570 transformers_js_py-0.1.4/LICENSE
--rw-r--r--   0        0        0       21 2023-07-23 00:11:09.181570 transformers_js_py-0.1.4/README.md
--rw-r--r--   0        0        0      579 2023-07-23 00:11:09.181570 transformers_js_py-0.1.4/pyproject.toml
--rw-r--r--   0        0        0     2536 2023-07-23 00:11:09.181570 transformers_js_py-0.1.4/transformers_js/__init__.py
--rw-r--r--   0        0        0      468 1970-01-01 00:00:00.000000 transformers_js_py-0.1.4/PKG-INFO
+-rw-r--r--   0        0        0    11357 2023-07-23 00:23:23.289673 transformers_js_py-0.1.5/LICENSE
+-rw-r--r--   0        0        0       21 2023-07-23 00:23:23.289673 transformers_js_py-0.1.5/README.md
+-rw-r--r--   0        0        0      579 2023-07-23 00:23:23.289673 transformers_js_py-0.1.5/pyproject.toml
+-rw-r--r--   0        0        0     2755 2023-07-23 00:23:23.289673 transformers_js_py-0.1.5/transformers_js/__init__.py
+-rw-r--r--   0        0        0      468 1970-01-01 00:00:00.000000 transformers_js_py-0.1.5/PKG-INFO
```

### Comparing `transformers_js_py-0.1.4/LICENSE` & `transformers_js_py-0.1.5/LICENSE`

 * *Files identical despite different names*

### Comparing `transformers_js_py-0.1.4/pyproject.toml` & `transformers_js_py-0.1.5/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "transformers-js-py"
-version = "0.1.4"
+version = "0.1.5"
 description = ""
 authors = ["Yuichiro Tachibana (Tsuchiya) <t.yic.yt@gmail.com>"]
 license = "Apache-2.0"
 readme = "README.md"
 packages = [{include = "transformers_js"}]
 
 [tool.poetry.dependencies]
```

### Comparing `transformers_js_py-0.1.4/transformers_js/__init__.py` & `transformers_js_py-0.1.5/transformers_js/__init__.py`

 * *Files 18% similar despite different names*

```diff
@@ -20,37 +20,43 @@
 
     def __repr__(self) -> str:
         return "TjsModuleProxy({})".format(", ".join(self.js_obj.object_keys()))
 
 
 class TjsProxy:
     def __init__(self, js_obj: pyodide.ffi.JsProxy):
-        self.js_obj = js_obj
+        self._js_obj = js_obj
 
     def __call__(self, *args: Any, **kwds: Any) -> Any:
-        if hasattr(self.js_obj, "_call"):
+        if hasattr(self._js_obj, "_call"):
             # Transformers.js uses a custom _call() method
             # to make the JS classes callable.
             # https://github.com/xenova/transformers.js/blob/2.4.1/src/utils/core.js#L45-L77
-            res = self.js_obj._call(*args, **kwds)
+            res = self._js_obj._call(*args, **kwds)
         else:
-            res = self.js_obj(*args, **kwds)
+            res = self._js_obj(*args, **kwds)
 
         return wrap_or_unwrap_proxy_object(res)
 
     def __getattr__(self, name: str) -> Any:
-        res = getattr(self.js_obj, name)
+        res = getattr(self._js_obj, name)
         return wrap_or_unwrap_proxy_object(res)
 
     def __getitem__(self, key: Any) -> Any:
-        res = self.js_obj[key]
+        res = self._js_obj[key]
         return wrap_or_unwrap_proxy_object(res)
 
     def __setitem__(self, key: Any, value: Any) -> None:
-        self.js_obj[key] = value
+        self._js_obj[key] = value
+
+    def __setattr__(self, __name: str, __value: Any) -> None:
+        if __name == "_js_obj":
+            super().__setattr__("_js_obj", __value)
+        else:
+            setattr(self._js_obj, __name, __value)
 
 
 def wrap_or_unwrap_proxy_object(obj):
     if isinstance(obj, pyodide.ffi.JsProxy):
         if obj.typeof == "object":
             return obj.to_py()
         return TjsProxy(obj)
```

