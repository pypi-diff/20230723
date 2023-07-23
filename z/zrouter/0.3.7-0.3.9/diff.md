# Comparing `tmp/zrouter-0.3.7.tar.gz` & `tmp/zrouter-0.3.9.tar.gz`

## Comparing `zrouter-0.3.7.tar` & `zrouter-0.3.9.tar`

### file list

```diff
@@ -1,7 +1,7 @@
--rw-r--r--   0        0        0     2539 2020-02-02 00:00:00.000000 zrouter-0.3.7/src/zrouter/__init__.py
--rw-r--r--   0        0        0     2407 2020-02-02 00:00:00.000000 zrouter-0.3.7/src/zrouter/decorator.py
--rw-r--r--   0        0        0       43 2020-02-02 00:00:00.000000 zrouter-0.3.7/src/zrouter/exception.py
--rw-r--r--   0        0        0     1091 2020-02-02 00:00:00.000000 zrouter-0.3.7/LICENSE
--rw-r--r--   0        0        0       29 2020-02-02 00:00:00.000000 zrouter-0.3.7/README.md
--rw-r--r--   0        0        0      642 2020-02-02 00:00:00.000000 zrouter-0.3.7/pyproject.toml
--rw-r--r--   0        0        0      595 2020-02-02 00:00:00.000000 zrouter-0.3.7/PKG-INFO
+-rw-r--r--   0        0        0     2547 2020-02-02 00:00:00.000000 zrouter-0.3.9/src/zrouter/__init__.py
+-rw-r--r--   0        0        0     2407 2020-02-02 00:00:00.000000 zrouter-0.3.9/src/zrouter/decorator.py
+-rw-r--r--   0        0        0       43 2020-02-02 00:00:00.000000 zrouter-0.3.9/src/zrouter/exception.py
+-rw-r--r--   0        0        0     1091 2020-02-02 00:00:00.000000 zrouter-0.3.9/LICENSE
+-rw-r--r--   0        0        0       29 2020-02-02 00:00:00.000000 zrouter-0.3.9/README.md
+-rw-r--r--   0        0        0      642 2020-02-02 00:00:00.000000 zrouter-0.3.9/pyproject.toml
+-rw-r--r--   0        0        0      595 2020-02-02 00:00:00.000000 zrouter-0.3.9/PKG-INFO
```

### Comparing `zrouter-0.3.7/src/zrouter/__init__.py` & `zrouter-0.3.9/src/zrouter/__init__.py`

 * *Files 4% similar despite different names*

```diff
@@ -8,36 +8,37 @@
 
 class RouterUtility:
     @staticmethod
     def get_params():
         """ 获取路由参数"""
         if request.method in ['GET', 'DELETE']:
             return json_.to_lowcase(request.args)
-        elif request.content_type == 'application/x-www-form-urlencoded':
+        elif 'multipart/form-data' in request.content_type:
             return {
                 'files': request.files,
-                'params': request.form.to_dict()
+                'params': json_.to_lowcase(request.form.to_dict())
             }
         else:
             try:
                 params = request.get_json()
-                return json_.to_lowcase(params)
+                return json_.iter_lowcase(params)
             except:
                 return {
                     'data': request.get_data()
                 }
 
     @staticmethod
     def clean_params(params):
         """空值参数清理"""
         return {k: v for k, v in params.items() if v not in ('', 'null') and v is not None}
 
 
 class Router(Blueprint, RouterUtility):
     """路由"""
+
     def __init__(self, *args, **kwargs):
         Blueprint.__init__(self, *args, **kwargs)
 
     @property
     def authorized(self):
         return True
```

### Comparing `zrouter-0.3.7/src/zrouter/decorator.py` & `zrouter-0.3.9/src/zrouter/decorator.py`

 * *Files identical despite different names*

### Comparing `zrouter-0.3.7/LICENSE` & `zrouter-0.3.9/LICENSE`

 * *Files identical despite different names*

### Comparing `zrouter-0.3.7/pyproject.toml` & `zrouter-0.3.9/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["hatchling"]
 build-backend = "hatchling.build"
 
 [project]
 name = "zrouter"
-version = "0.3.7"
+version = "0.3.9"
 authors = [
   { name="inspirare6", email="inspirare6@163.com" },
 ]
 description = "zen router library"
 readme = "README.md"
 requires-python = ">=3.7"
 dependencies = [
```

### Comparing `zrouter-0.3.7/PKG-INFO` & `zrouter-0.3.9/PKG-INFO`

 * *Files 16% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: zrouter
-Version: 0.3.7
+Version: 0.3.9
 Summary: zen router library
 Project-URL: Homepage, https://github.com/inspirare6/zrouter
 Project-URL: Bug Tracker, https://github.com/inspirare6/zrouter/issues
 Author-email: inspirare6 <inspirare6@163.com>
 License-File: LICENSE
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

