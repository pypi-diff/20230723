# Comparing `tmp/unitauto-1.0.2.tar.gz` & `tmp/unitauto-1.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "/home/runner/work/unitauto-py/unitauto-py/dist/.tmp-sf2gyurg/unitauto-1.0.2.tar", last modified: Mon Jul 17 16:30:30 2023, max compression
+gzip compressed data, was "/home/runner/work/unitauto-py/unitauto-py/dist/.tmp-mpwep_3f/unitauto-1.0.3.tar", last modified: Sun Jul 23 16:38:12 2023, max compression
```

## Comparing `unitauto-1.0.2.tar` & `unitauto-1.0.3.tar`

### file list

```diff
@@ -1,18 +1,18 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-17 16:30:30.000000 unitauto-1.0.2/
--rw-r--r--   0 runner    (1001) docker     (123)     1066 2023-07-17 16:30:13.000000 unitauto-1.0.2/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     2470 2023-07-17 16:30:30.000000 unitauto-1.0.2/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1948 2023-07-17 16:30:13.000000 unitauto-1.0.2/README.md
--rw-r--r--   0 runner    (1001) docker     (123)      103 2023-07-17 16:30:13.000000 unitauto-1.0.2/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)      583 2023-07-17 16:30:30.000000 unitauto-1.0.2/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-17 16:30:30.000000 unitauto-1.0.2/unitauto/
--rw-r--r--   0 runner    (1001) docker     (123)       18 2023-07-17 16:30:13.000000 unitauto-1.0.2/unitauto/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    30829 2023-07-17 16:30:13.000000 unitauto-1.0.2/unitauto/methodutil.py
--rw-r--r--   0 runner    (1001) docker     (123)     7071 2023-07-17 16:30:13.000000 unitauto-1.0.2/unitauto/server.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-17 16:30:30.000000 unitauto-1.0.2/unitauto/test/
--rw-r--r--   0 runner    (1001) docker     (123)     2233 2023-07-17 16:30:13.000000 unitauto-1.0.2/unitauto/test/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3273 2023-07-17 16:30:13.000000 unitauto-1.0.2/unitauto/test/testutil.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-17 16:30:30.000000 unitauto-1.0.2/unitauto.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2470 2023-07-17 16:30:30.000000 unitauto-1.0.2/unitauto.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      285 2023-07-17 16:30:30.000000 unitauto-1.0.2/unitauto.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-17 16:30:30.000000 unitauto-1.0.2/unitauto.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-17 16:30:30.000000 unitauto-1.0.2/unitauto.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:38:12.000000 unitauto-1.0.3/
+-rw-r--r--   0 runner    (1001) docker     (123)     1066 2023-07-23 16:37:56.000000 unitauto-1.0.3/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     2470 2023-07-23 16:38:12.000000 unitauto-1.0.3/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1948 2023-07-23 16:37:56.000000 unitauto-1.0.3/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      103 2023-07-23 16:37:56.000000 unitauto-1.0.3/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)      583 2023-07-23 16:38:12.000000 unitauto-1.0.3/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:38:12.000000 unitauto-1.0.3/unitauto/
+-rw-r--r--   0 runner    (1001) docker     (123)       18 2023-07-23 16:37:56.000000 unitauto-1.0.3/unitauto/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    33695 2023-07-23 16:37:56.000000 unitauto-1.0.3/unitauto/methodutil.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7273 2023-07-23 16:37:56.000000 unitauto-1.0.3/unitauto/server.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:38:12.000000 unitauto-1.0.3/unitauto/test/
+-rw-r--r--   0 runner    (1001) docker     (123)     2233 2023-07-23 16:37:56.000000 unitauto-1.0.3/unitauto/test/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3414 2023-07-23 16:37:56.000000 unitauto-1.0.3/unitauto/test/testutil.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:38:12.000000 unitauto-1.0.3/unitauto.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2470 2023-07-23 16:38:12.000000 unitauto-1.0.3/unitauto.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      285 2023-07-23 16:38:12.000000 unitauto-1.0.3/unitauto.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 16:38:12.000000 unitauto-1.0.3/unitauto.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-23 16:38:12.000000 unitauto-1.0.3/unitauto.egg-info/top_level.txt
```

### Comparing `unitauto-1.0.2/LICENSE` & `unitauto-1.0.3/LICENSE`

 * *Files identical despite different names*

### Comparing `unitauto-1.0.2/PKG-INFO` & `unitauto-1.0.3/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: unitauto
-Version: 1.0.2
+Version: 1.0.3
 Summary: An unit testing platform powered by machine learning. Coding-free, comprehensive and automatic testing for methods/functions
 Home-page: https://github.com/TommyLemon/unitauto-py
 Author: TommyLemon
 Author-email: tommylemon@qq.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `unitauto-1.0.2/README.md` & `unitauto-1.0.3/README.md`

 * *Files identical despite different names*

### Comparing `unitauto-1.0.2/setup.cfg` & `unitauto-1.0.3/setup.cfg`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = unitauto
-version = 1.0.2
+version = 1.0.3
 author = TommyLemon
 author_email = tommylemon@qq.com
 description = An unit testing platform powered by machine learning. Coding-free, comprehensive and automatic testing for methods/functions
 long_description = file: README.md
 long_description_content_type = text/markdown
 url = https://github.com/TommyLemon/unitauto-py
 classifiers =
```

### Comparing `unitauto-1.0.2/unitauto/methodutil.py` & `unitauto-1.0.3/unitauto/methodutil.py`

 * *Files 5% similar despite different names*

```diff
@@ -19,14 +19,15 @@
 # AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
 # LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
 # OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
 # SOFTWARE.
 import asyncio
 import builtins
 import json
+import os
 import re
 import time
 import inspect
 from typing import Type
 
 null = None
 false = False
@@ -48,25 +49,26 @@
 KEY_UI = "ui"
 KEY_TIME = "time"
 KEY_TIMEOUT = "timeout"
 KEY_PACKAGE = "package"
 KEY_THIS = "this"
 KEY_CLASS = "class"
 KEY_CONSTRUCTOR = "constructor"
-KEY_KEY = 'key'
+KEY_KEY = "key"
 KEY_TYPE = "type"
 KEY_AT_TYPE = "@type"
 KEY_VALUE = "value"
 KEY_WARN = "warn"
 KEY_STATIC = "static"
 KEY_ASYNC = "async"
 KEY_NAME = "name"
 KEY_METHOD = "method"
 KEY_MOCK = "mock"
 KEY_QUERY = "query"
+KEY_DEPTH = "depth"
 KEY_RETURN = "return"
 KEY_TIME_DETAIL = "time:start|duration|end"
 KEY_CLASS_ARGS = "classArgs"
 KEY_METHOD_ARGS = "methodArgs"
 KEY_CALLBACK = "callback"
 KEY_GLOBAL = "global"
 
@@ -138,16 +140,54 @@
 })
 
 
 class InterfaceProxy:
     pass
 
 
-def get_instance(self, typ: Type, value: any, class_args: list = null, reuse: bool = false):
-    return
+INSTANCE_MAP = {}
+
+
+def get_instance(
+    clazz, value: any = null, constructor: callable = null, class_args: list = null,
+    reuse: bool = false, module=null, import_fun: callable = null
+):
+    reuse = reuse or false
+    key = str(clazz) + ('' if is_none(constructor) else '.' + str(constructor))\
+        + '(' + str(class_args) + ')' if reuse else null
+
+    instance = INSTANCE_MAP[key] if reuse else null
+
+    if is_none(instance):
+        cal = size(class_args)
+        ca_keys = [null] * cal
+        ca_types = [null] * cal
+        ca_values = [null] * cal
+        c_kwargs = {}
+        init_args(class_args, ca_keys, ca_types, ca_values, c_kwargs, import_fun=import_fun)
+        if constructor is None:
+            instance = clazz(*ca_values, **c_kwargs)
+        else:
+            try:
+                instance = constructor(*ca_values, **c_kwargs)
+            except Exception as e:
+                print(e)
+                try:
+                    instance = clazz.constructor(*ca_values, **c_kwargs)  # @staticmethod in class
+                except Exception as e2:
+                    raise Exception(
+                        str(module) + ' does not have such a function, and ' + str(clazz)
+                        + ' does not have a @staticmethod called ' + str(constructor)
+                        + '! ' + str(e) + '; ' + str(e2)
+                    )
+
+        if reuse and not_none(instance):
+            INSTANCE_MAP[key] = instance
+
+    return instance
 
 
 def on_complete(data: any, method: callable, proxy: InterfaceProxy, *extras: any):
     pass
 
 
 def on_callback(data: any, method: callable, proxy: InterfaceProxy, *extras: any):
@@ -159,26 +199,29 @@
     callback: callable = on_callback
     getinstance: callable = get_instance
 
 
 listener = Listener()
 
 
-def list_method(req) -> dict:
+def list_method(req, import_fun: callable = null) -> dict:
     start_time = cur_time_in_millis()
     try:
         if is_str(req):
             req = parse_json(req)
 
         mock = req.get(KEY_MOCK)
         assert mock in [null, true, false], KEY_MOCK + ' must be in [true, false]!'
 
         query = req.get(KEY_QUERY)
         assert query in [null, 0, 1, 2], KEY_QUERY + ' must be in [0, 1, 2]! 0-Data, 1-Total count, 2-Both above'
 
+        depth = req.get(KEY_DEPTH)
+        assert is_int(depth, false), KEY_DEPTH + ' must be int!'
+
         package = req.get(KEY_PACKAGE)
         assert is_str(package), KEY_PACKAGE + ' must be str!'
 
         clazz = req.get(KEY_CLASS)
         assert is_str(clazz), KEY_CLASS + ' must be str!'
 
         method = req.get(KEY_METHOD)
@@ -190,40 +233,60 @@
         is_all_pkg = is_empty(package)
         is_all_cls = is_empty(clazz)
         is_all_mtd = is_empty(method)
 
         fl = split(clazz, '$')
 
         module_list = []
-        if is_all_pkg:
-            root_module = __import__('')
-        else:
-            mn = package if is_empty(fl) else package + '.' + fl[0]
-            root_module = __import__(mn, fromlist=['__init__'] if is_empty(fl) else fl[0])
+        import_fun = import_fun or __import__
 
-            module_list.append(root_module)
+        depth = depth or 0
+        d = 0
+        for root, dirs, files in os.walk(package):
+            d += 1
+            if depth > 0 and d > depth:
+                break
+
+            for name in files:
+                if size(name) <= 3 or not name.endswith('.py'):
+                    continue
+
+                name = name[:-3]
+                p = os.path.join(root, name).replace('/', '.')
+                m = import_fun(p, fromlist=name)
+                if is_none(m) or module_list.__contains__(m):
+                    continue
+
+                module_list.append(m)
+
+        if is_empty(module_list):
             try:
+                mn = package if is_empty(fl) else package + '.' + fl[0]
+                root_module = import_fun(mn, fromlist=['__init__'] if is_empty(fl) else fl[0])
+
+                module_list.append(root_module)
                 mdl_dict = root_module.__dict__
                 vs = mdl_dict.values()
                 for v in vs:
                     if type(v).__name__ == 'module' and str(v).endswith("/__init__.py'>"):  # if isinstance(v, module):
                         module_list.append(v)
                         pass
+
             except Exception as e:
                 print(e)
 
         pkg_list = []
 
         for module_item in module_list:
             cl = []
             pkg = module_item.__name__
             pkg_str = str(module_item)
             is_file = pkg_str.endswith(".py'>") and not pkg_str.endswith("/__init__.py'>")
             if is_file:
-                ns = split(pkg, '.')  # 不存在这个函数 ind = pkg.lastindex('.')
+                ns = split(pkg, '.')  # 不存在这个函数 ind = lastindex(pkg, '.')
                 pkg = pkg[:-1-len(ns[-1])]
 
             if is_empty(pkg):
                 continue
 
             mdl_list = dir(module_item)
             l = size(mdl_list)
@@ -253,15 +316,15 @@
                         s = str(cls)
                         if ct == 'function':
                             mtd = parse_method(cls) if is_all_mtd or cls.__name__ == method else null
                             if is_empty(mtd):
                                 continue
 
                             cls_list.append({
-                                KEY_CLASS: cls.__name__,
+                                # KEY_CLASS: cls.__name__,
                                 KEY_METHOD_LIST: [mtd]
                             })
                         if ct == 'class' or ct == 'type':
                             cl.append(cls)
                         elif ct == 'module':
                             if is_file or (s.endswith(".py'>") and not s.endswith("/__init__.py'>")):
                                 cl.append(cls)
@@ -413,15 +476,18 @@
         'parameterTypeList': types if static else types[1:],
         'genericParameterTypeList': types if static else types[1:],
         'parameterNameList': names if static else names[1:],
         'parameterDefaultValueList': null
     }
 
 
-def wrap_result(instance, func, method_args, ma_types, ma_values, result, start_time):
+def wrap_result(
+    instance, func, method_args, ma_types, ma_values, result, start_time,
+    json_dumps: callable = null, json_loads: callable = null
+):
     time_detail = get_time_detail(start_time)
 
     signature = inspect.signature(func)
     return_annotation = null if signature is None else signature.return_annotation
     rt = null
     if return_annotation is not None:
         try:
@@ -430,27 +496,29 @@
                 rt = type(result).__name__
         except Exception as e:
             print(e)
             rt = type(result).__name__  # str(return_annotation)
 
     mal = size(method_args)
     mas = [null] * mal
+
+    json_dumps = json_dumps or json.dumps
     if mal > 0:  # bug 要及时发现 and size(ma_values) == mal:
         i = -1
         for v in ma_values:
             i += 1
 
             if callable(v):
                 mas[i] = method_args[i]
                 continue
 
             t = ma_types[i]
 
             try:
-                json.dumps(v)
+                json_dumps(v)
             except Exception as e:
                 print(e)
                 v = str(v)
 
             mas[i] = {
                 KEY_TYPE: t.__name__ if t is not None else type(v),
                 KEY_VALUE: v
@@ -469,25 +537,26 @@
         }
 
     cls = type(instance)
     this = {
         KEY_TYPE: cls.__name__,
     }
 
+    json_loads = json_loads or json.loads
     try:
-        json.dumps(instance)
+        json_dumps(instance)
         this[KEY_VALUE] = instance
     except Exception as e:
         print(e)
         try:
-            this[KEY_VALUE] = json.loads(json.dumps(instance, cls=cls))
+            this[KEY_VALUE] = json_loads(json_dumps(instance, cls=cls))
         except Exception as e2:
             print(e2)
             try:
-                this[KEY_VALUE] = json.loads(instance.encode(null))
+                this[KEY_VALUE] = json_loads(instance.encode(null))
             except Exception as e3:
                 print(e3)  # FIXME instance.__dict__ , dir(instance)
                 this[KEY_VALUE] = str(instance)
                 this[KEY_WARN] = str(e)
 
     return {
         KEY_LANGUAGE: LANGUAGE,
@@ -498,22 +567,33 @@
         KEY_RETURN: result,
         KEY_METHOD_ARGS: mas,
         KEY_THIS: this,
         KEY_TIME_DETAIL: time_detail
     }
 
 
-def invoke_method(req: any, callback: callable = null) -> dict:
+def invoke_method(
+    req: any, callback: callable = null, getinstance: callable = null,
+    json_dumps: callable = null, json_loads: callable = null, import_fun: callable = null
+) -> dict:
     start_time = time.time_ns()
     is_wait = false
     try:
+        getinstance = getinstance or get_instance
+        json_dumps = json_dumps or to_json_str
+        json_loads = json_loads or parse_json
+        import_fun = import_fun or __import__
+
         assert is_none(callback) or callable(callback)
 
         if is_str(req):
-            req = parse_json(req)
+            req = json_loads(req)
+
+        reuse = req.get(KEY_REUSE)
+        assert is_bool(reuse), (KEY_REUSE + ' must be bool!')
 
         static = req.get(KEY_STATIC)
         assert is_bool(static), (KEY_STATIC + ' must be bool!')
 
         is_async = req.get(KEY_ASYNC)
         assert is_bool(is_async), (KEY_ASYNC + ' must be bool!')
 
@@ -545,39 +625,40 @@
             assert class_args is None, KEY_THIS + ' cannot appear together with ' + KEY_CLASS_ARGS + '!'
             assert constructor is None, KEY_THIS + ' cannot appear together with ' + KEY_CONSTRUCTOR + '!'
 
             this_keys = [null]
             this_types = [null]
             this_values = [null]
             this_kwargs = {}
-            init_args([this], this_keys, this_types, this_values, this_kwargs)
+            init_args([this], this_keys, this_types, this_values, this_kwargs, import_fun=import_fun)
             instance = this_values[0]
 
         if class_args is not None:
             assert not static, KEY_CLASS_ARGS + ' cannot appear together with ' + KEY_STATIC + '!'
             assert this is None, KEY_CLASS_ARGS + ' cannot appear together with ' + KEY_THIS + '!'
 
         mal = size(method_args)
         ma_keys = [null] * mal
         ma_types = [null] * mal
         ma_values = [null] * mal
         m_kwargs = {}
 
         final_result = {}
+
         def final_callback(*args, **kwargs):
             if not_none(callback):  # callable(callback):
                 callback(wrap_result(final_result.get(KEY_THIS), func, method_args, ma_types, ma_values, final_result.get(KEY_VALUE), start_time))
 
-        is_wait = init_args(method_args, ma_keys, ma_types, ma_values, m_kwargs, true, final_callback)
+        is_wait = init_args(method_args, ma_keys, ma_types, ma_values, m_kwargs, true, final_callback, import_fun=import_fun)
 
         fl = split(clazz, '$')
         l = size(fl)
 
         mn = package if l <= 0 else package + '.' + fl[0]
-        module = __import__(mn, fromlist=['__init__'] if l <= 0 else fl[0])
+        module = import_fun(mn, fromlist=['__init__'] if l <= 0 else fl[0])
 
         cls: any = null
         if l > 1:
             i = -1
             for n in fl:
                 i += 1
                 if i <= 0:
@@ -585,37 +666,35 @@
                 cls = getattr(module, n)
 
         if cls is None:
             func = getattr(module, method)
         elif static:
             func = getattr(cls, method)
         else:
-            constructor_func = None if constructor is None else getattr(module, constructor)
-
             if instance is None:
-                cal = size(class_args)
-                ca_keys = [null] * cal
-                ca_types = [null] * cal
-                ca_values = [null] * cal
-                c_kwargs = {}
-                init_args(class_args, ca_keys, ca_types, ca_values, c_kwargs)
-                instance = cls(*ca_values, **c_kwargs) if constructor_func is None else constructor_func(*ca_values, **c_kwargs)
+                constructor_func = None if is_empty(constructor) else getattr(module, constructor)
+                instance = getinstance(
+                    cls, null, constructor_func, class_args, reuse=reuse, module=module, import_fun=import_fun
+                )
 
             func = getattr(instance, method)
 
         final_result[KEY_THIS] = instance
         ksl = size(m_kwargs)
         start_time = cur_time_in_millis()
 
         # TODO 自动识别 async 关键词
         result = asyncio.run(func(*ma_values[:mal-ksl], **m_kwargs)) if is_async \
             else func(*ma_values[:mal-ksl], **m_kwargs)  # asyncio.run 只允许调 async 函数 is_async != false
 
         final_result[KEY_VALUE] = result
-        res = wrap_result(instance, func, method_args, ma_types, ma_values, result, start_time)
+        res = wrap_result(
+            instance, func, method_args, ma_types, ma_values, result, start_time,
+            json_dumps=json_dumps, json_loads=json_loads
+        )
     except Exception as e:
         res = {
             KEY_LANGUAGE: LANGUAGE,
             KEY_OK: false,
             KEY_CODE: CODE_SERVER_ERROR,
             KEY_MSG: str(e),
             KEY_TIME_DETAIL: get_time_detail(start_time),
@@ -626,15 +705,16 @@
     if (not is_wait) and callable(callback):
         callback(res)
     return res
 
 
 def init_args(
     method_args: list, ma_keys: list, ma_types: list, ma_values: list,
-    ma_kwargs: dict, keep_kwargs_in_types_and_values: bool = false, callback: callable = null
+    ma_kwargs: dict, keep_kwargs_in_types_and_values: bool = false,
+    callback: callable = null, import_fun: callable = null
 ):
     is_wait = false
     mal = size(method_args)
     if mal > 0:
         i = -1
         for arg in method_args:
             i += 1
@@ -683,14 +763,15 @@
                         fa_types[j] = null if ak_ind < 0 else ak[:ak_ind]
                         fa_keys[j] = ak if ak_ind < 0 else ak[ak_ind+1:]
 
                     rtn_type = value.get(KEY_TYPE)
                     rtn_val = value.get(KEY_RETURN)
 
                     raw_val: dict = value
+
                     def cb_fun(*args, **kwargs):
                         mas: list = []
                         if not_empty(args):
                             for arg in args:
                                 mas.append({
                                     KEY_TYPE: type(arg).__name__,
                                     KEY_VALUE: arg
@@ -740,15 +821,15 @@
                             except Exception as e:
                                 print(e)
 
                         return cast(rv, get_class(rtn_type, rv))
 
                     value = cb_fun  # eval('lambda ' + ', '.join(fa_keys) + ': ' + str(rtn_val))
 
-            clazz = type(value) if is_fun else get_class(typ, value)
+            clazz = type(value) if is_fun else get_class(typ, value, import_fun)
             value = cast(value, clazz) if not is_fun else value
 
             ma_keys[i] = key
             if is_none(key):
                 if is_empty(ma_kwargs):
                     ma_types[i] = clazz
                     ma_values[i] = value
@@ -764,58 +845,63 @@
             else:
                 del ma_types[-1]
                 del ma_values[-1]
 
     return is_wait
 
 
-def cast(value, clazz):
+def cast(value, clazz, json_dumps: callable = null, json_loads: callable = null):
     if value is not None and not isinstance(value, clazz):
+        json_dumps = json_dumps or json.dumps
+        json_loads = json_loads or json.loads
+
         s = ''
         try:
-            s = value if is_str(value) else json.dumps(value)
+            s = value if is_str(value) else json_dumps(value)
             if PRIMITIVE_CLASS_MAP.__contains__(clazz.__name__):
                 value = eval(clazz.__name__ + '(' + s + ')')
             else:
-                value = json.loads(s, cls=clazz)  # FIXME 目前仅支持继承 JSONDecoder 且重写了 decode 方法的类
+                value = json_loads(s, cls=clazz)  # FIXME 目前仅支持继承 JSONDecoder 且重写了 decode 方法的类
         except Exception as e:
             print(e)
             if is_str(value):
-                value = json.loads(value)
+                value = json_loads(value)
 
             if not isinstance(value, clazz):
                 if is_list(value):
                     value = clazz(*value)
                 elif is_dict(value):
                     value = clazz(**value)  # FIXME 目前仅支持继承 __init__ 传完整参数且顺序一致的类
                 else:
                     pass
 
     return value
 
 
-def get_class(typ: str, value: any = None) -> Type:
+def get_class(typ: str, value: any = None, import_fun: callable = null) -> Type:
     fl = split(typ, '$')
     if is_empty(fl):
         return type(value)
 
+    import_fun = import_fun or __import__
+
     path = typ
     clazz = CLASS_MAP.get(path)
     if clazz is None:
         fl = split(path, '$')
         pkg = fl[0]
 
         pl = split(pkg, '.')
         end = size(pl) - 1
         cn = null if end < 0 else pl[end]
         # pkg = pkg[:-len(cn)]
 
         l = size(fl)
         mn = fl[0]  # pkg if is_empty(fl) else pkg + '.' + cn
-        module = __import__(mn, fromlist=cn)
+        module = import_fun(mn, fromlist=cn)
         if l <= 1:
             clazz = getattr(module, cn)
         else:
             j = -1
             for n in fl:
                 j += 1
                 if j <= 0:
```

### Comparing `unitauto-1.0.2/unitauto/server.py` & `unitauto-1.0.3/unitauto/server.py`

 * *Files 2% similar despite different names*

```diff
@@ -75,24 +75,32 @@
 
         bs = self.rfile.read(int(self.headers[KEY_CONTENT_LENGTH]))
         req = bs.decode()  # bs.decode(CHARSET)
         # req = urllib.unquote(bs).decode(CHARSET, 'ignore')
 
         done = [false]
 
+        wfile = self.wfile
+
         def callback(res):
             res_str = to_json_str(res)
             res_byte = res_str.encode()
             self.send_response(RESPONSE_CODE_SUCCESS)
             self.send_headers(origin, method)
-            if done[0] or self.wfile.closed:
+            if done[0] or wfile is None or wfile.closed:
                 return
-            self.wfile.write(res_byte)
-            self.wfile.close()
+
+            wfile.write(res_byte)
             done[0] = true
+            try:
+                wfile.close()
+            except BaseException as e:
+                # print(e)
+                pass
+            # cause error 'unresolved reference'  wfile = null
 
         if path == '/method/list':
             rsp = list_method(req)
             callback(rsp)
         else:
             invoke_method(req, callback)
             while true:
```

### Comparing `unitauto-1.0.2/unitauto/test/__init__.py` & `unitauto-1.0.3/unitauto/test/__init__.py`

 * *Files identical despite different names*

### Comparing `unitauto-1.0.2/unitauto/test/testutil.py` & `unitauto-1.0.3/unitauto/test/testutil.py`

 * *Files 8% similar despite different names*

```diff
@@ -90,14 +90,18 @@
 
     def __init__(self, id: int = 0, sex: int = 0, name: str = ''):
         super().__init__()
         self.id = id
         self.sex = sex
         self.name = name
 
+    @staticmethod
+    def get_instance(id: int = 0, sex: int = 0, name: str = '') -> 'Test':
+        return Test(id=id, sex=sex, name=name)
+
     def decode(self, s: str, _w: Callable[..., Any] = ...) -> Any:
         args = json.loads(s)
         return Test(**args)
 
     def encode(self, o: Any) -> str:
         return json.dumps({
             'id': self.id,
```

### Comparing `unitauto-1.0.2/unitauto.egg-info/PKG-INFO` & `unitauto-1.0.3/unitauto.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: unitauto
-Version: 1.0.2
+Version: 1.0.3
 Summary: An unit testing platform powered by machine learning. Coding-free, comprehensive and automatic testing for methods/functions
 Home-page: https://github.com/TommyLemon/unitauto-py
 Author: TommyLemon
 Author-email: tommylemon@qq.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

