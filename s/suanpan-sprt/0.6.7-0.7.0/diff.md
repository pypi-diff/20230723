# Comparing `tmp/suanpan-sprt-0.6.7.tar.gz` & `tmp/suanpan-sprt-0.7.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/suanpan-sprt-0.6.7.tar", last modified: Sun Jul 23 08:10:41 2023, max compression
+gzip compressed data, was "dist/suanpan-sprt-0.7.0.tar", last modified: Sun Jul 23 09:30:28 2023, max compression
```

## Comparing `suanpan-sprt-0.6.7.tar` & `suanpan-sprt-0.7.0.tar`

### file list

```diff
@@ -1,26 +1,26 @@
-drwxrwxr-x   0 gitlab-runner  (1003) gitlab-runner  (1003)        0 2023-07-23 08:10:41.000000 suanpan-sprt-0.6.7/
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      482 2023-07-23 08:10:41.000000 suanpan-sprt-0.6.7/PKG-INFO
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      129 2023-07-12 09:08:26.000000 suanpan-sprt-0.6.7/README.md
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)       38 2023-07-23 08:10:41.000000 suanpan-sprt-0.6.7/setup.cfg
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     1073 2023-07-12 09:08:26.000000 suanpan-sprt-0.6.7/setup.py
-drwxrwxr-x   0 gitlab-runner  (1003) gitlab-runner  (1003)        0 2023-07-23 08:10:41.000000 suanpan-sprt-0.6.7/sprt/
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      100 2023-07-12 09:08:26.000000 suanpan-sprt-0.6.7/sprt/__init__.py
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     4337 2023-07-18 09:03:49.000000 suanpan-sprt-0.6.7/sprt/__main__.py
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     8168 2023-07-12 09:08:26.000000 suanpan-sprt-0.6.7/sprt/arguments.py
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     1251 2023-07-12 09:08:26.000000 suanpan-sprt-0.6.7/sprt/envs.py
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      242 2023-07-12 09:08:26.000000 suanpan-sprt-0.6.7/sprt/exceptions.py
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     6021 2023-07-22 10:21:55.000000 suanpan-sprt-0.6.7/sprt/loader.py
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     2136 2023-07-23 08:10:40.000000 suanpan-sprt-0.6.7/sprt/log.py
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      880 2023-07-23 08:10:40.000000 suanpan-sprt-0.6.7/sprt/master.py
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     6917 2023-07-22 10:21:55.000000 suanpan-sprt-0.6.7/sprt/server.py
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     6419 2023-07-12 09:08:26.000000 suanpan-sprt-0.6.7/sprt/storage.py
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     3261 2023-07-12 09:08:26.000000 suanpan-sprt-0.6.7/sprt/testing.py
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     1290 2023-07-12 09:08:26.000000 suanpan-sprt-0.6.7/sprt/utils.py
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)       22 2023-07-23 08:10:40.000000 suanpan-sprt-0.6.7/sprt/version.py
-drwxrwxr-x   0 gitlab-runner  (1003) gitlab-runner  (1003)        0 2023-07-23 08:10:41.000000 suanpan-sprt-0.6.7/suanpan_sprt.egg-info/
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      482 2023-07-23 08:10:41.000000 suanpan-sprt-0.6.7/suanpan_sprt.egg-info/PKG-INFO
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      439 2023-07-23 08:10:41.000000 suanpan-sprt-0.6.7/suanpan_sprt.egg-info/SOURCES.txt
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)        1 2023-07-23 08:10:41.000000 suanpan-sprt-0.6.7/suanpan_sprt.egg-info/dependency_links.txt
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)       70 2023-07-23 08:10:41.000000 suanpan-sprt-0.6.7/suanpan_sprt.egg-info/entry_points.txt
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      158 2023-07-23 08:10:41.000000 suanpan-sprt-0.6.7/suanpan_sprt.egg-info/requires.txt
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)        5 2023-07-23 08:10:41.000000 suanpan-sprt-0.6.7/suanpan_sprt.egg-info/top_level.txt
+drwxrwxr-x   0 gitlab-runner  (1003) gitlab-runner  (1003)        0 2023-07-23 09:30:28.000000 suanpan-sprt-0.7.0/
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      482 2023-07-23 09:30:28.000000 suanpan-sprt-0.7.0/PKG-INFO
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      129 2023-07-12 09:08:26.000000 suanpan-sprt-0.7.0/README.md
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)       38 2023-07-23 09:30:28.000000 suanpan-sprt-0.7.0/setup.cfg
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     1073 2023-07-12 09:08:26.000000 suanpan-sprt-0.7.0/setup.py
+drwxrwxr-x   0 gitlab-runner  (1003) gitlab-runner  (1003)        0 2023-07-23 09:30:28.000000 suanpan-sprt-0.7.0/sprt/
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      100 2023-07-12 09:08:26.000000 suanpan-sprt-0.7.0/sprt/__init__.py
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     4337 2023-07-18 09:03:49.000000 suanpan-sprt-0.7.0/sprt/__main__.py
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     8168 2023-07-12 09:08:26.000000 suanpan-sprt-0.7.0/sprt/arguments.py
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     1251 2023-07-12 09:08:26.000000 suanpan-sprt-0.7.0/sprt/envs.py
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      242 2023-07-12 09:08:26.000000 suanpan-sprt-0.7.0/sprt/exceptions.py
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     4546 2023-07-23 09:30:27.000000 suanpan-sprt-0.7.0/sprt/loader.py
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     4375 2023-07-23 09:30:27.000000 suanpan-sprt-0.7.0/sprt/log.py
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      880 2023-07-23 08:10:40.000000 suanpan-sprt-0.7.0/sprt/master.py
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     6982 2023-07-23 09:30:27.000000 suanpan-sprt-0.7.0/sprt/server.py
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     6419 2023-07-12 09:08:26.000000 suanpan-sprt-0.7.0/sprt/storage.py
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     3261 2023-07-12 09:08:26.000000 suanpan-sprt-0.7.0/sprt/testing.py
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     1290 2023-07-12 09:08:26.000000 suanpan-sprt-0.7.0/sprt/utils.py
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)       22 2023-07-23 09:30:27.000000 suanpan-sprt-0.7.0/sprt/version.py
+drwxrwxr-x   0 gitlab-runner  (1003) gitlab-runner  (1003)        0 2023-07-23 09:30:28.000000 suanpan-sprt-0.7.0/suanpan_sprt.egg-info/
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      482 2023-07-23 09:30:28.000000 suanpan-sprt-0.7.0/suanpan_sprt.egg-info/PKG-INFO
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      439 2023-07-23 09:30:28.000000 suanpan-sprt-0.7.0/suanpan_sprt.egg-info/SOURCES.txt
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)        1 2023-07-23 09:30:28.000000 suanpan-sprt-0.7.0/suanpan_sprt.egg-info/dependency_links.txt
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)       70 2023-07-23 09:30:28.000000 suanpan-sprt-0.7.0/suanpan_sprt.egg-info/entry_points.txt
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      158 2023-07-23 09:30:28.000000 suanpan-sprt-0.7.0/suanpan_sprt.egg-info/requires.txt
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)        5 2023-07-23 09:30:28.000000 suanpan-sprt-0.7.0/suanpan_sprt.egg-info/top_level.txt
```

### Comparing `suanpan-sprt-0.6.7/setup.py` & `suanpan-sprt-0.7.0/setup.py`

 * *Files identical despite different names*

### Comparing `suanpan-sprt-0.6.7/sprt/__main__.py` & `suanpan-sprt-0.7.0/sprt/__main__.py`

 * *Files identical despite different names*

### Comparing `suanpan-sprt-0.6.7/sprt/arguments.py` & `suanpan-sprt-0.7.0/sprt/arguments.py`

 * *Files identical despite different names*

### Comparing `suanpan-sprt-0.6.7/sprt/envs.py` & `suanpan-sprt-0.7.0/sprt/envs.py`

 * *Files identical despite different names*

### Comparing `suanpan-sprt-0.6.7/sprt/loader.py` & `suanpan-sprt-0.7.0/sprt/loader.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,34 +1,30 @@
 import json
-import logging
 import inspect
 import pathlib
 import importlib
 import importlib.util
-from quart import current_app
 from .arguments import init_arg_from_arg_spec, init_return_from_value, DEFAULT_DATA_SUBTYPE_ARGS_MAP
 from .storage import Storage
 from .exceptions import ParamsArgError, InvocationFunctionError
-from .log import NodeStreamHandler, LogkitHandler
+from .log import LogManager
 
 
 class NodeFunction(object):
     def __init__(self, user_id, app_id, node_id, working_dir, filename, function='main'):
         file = pathlib.Path(filename)
         self.name = file.stem
         self.location = pathlib.Path(working_dir) / filename
         self.function = function
         self.module = self.load_module()
         self.context = RuntimeContext(user_id, app_id, node_id)
         self.input_arguments = []
         self.has_context = False
         self.load_validator()
-        self._logkit = self._init_logkit(app_id, node_id)
-        self.context.log = self._logkit
-        self._logkit_handler = None
+        self.context.log = LogManager.get_logger(app_id)
 
     def load_module(self):
         if not self.location.is_file():
             raise Exception(f'invalid component file: {self.location}')
 
         spec = importlib.util.spec_from_file_location(self.name, self.location)
         if spec is None:
@@ -89,52 +85,18 @@
                         for index, r in enumerate(ret)}
             else:
                 return {'out1': init_return_from_value(ret, arg_spec, 0)(f'out{1}', request_id=request_id).save(ret)}
         except Exception as e:
             raise InvocationFunctionError(f'call function: {e}')
 
     def update_logkit(self, logkit=None):
-        if logkit is None:
-            self._logkit.removeHandler(self._logkit_handler)
-        else:
-            if self._logkit_handler and logkit.uri != self._logkit_handler.uri:
-                self._logkit.removeHandler(self._logkit_handler)
-                self._logkit_handler = None
-
-            if self._logkit_handler is None:
-                logging.info('setup logkit handler: %s', logkit.uri)
-                lh = LogkitHandler(logkit.uri, logkit.namespace, logkit.path, logkit.events_append)
-                lh.setLevel(logkit.logs_level.upper())
-                self._logkit.addHandler(lh)
-                self._logkit_handler = lh
-                # self._logkit.setLevel(logkit.logs_level.upper())
-
-    @staticmethod
-    def _init_logkit(app_id, node_id):
-        name = f'logkit_{app_id}_{node_id}'
-        logger = logging.getLogger(name)
-        logger.propagate = False
-
-        if len(logger.handlers) > 0:
-            return logger
-
-        formatter = logging.Formatter('%(asctime)s :: [%(levelname)-8s] %(message)s')
-        sh = NodeStreamHandler()
-        sh.setLevel('DEBUG')
-        sh.setFormatter(formatter)
-        logger.addHandler(sh)
-
-        return logger
+        LogManager.update_logger(self.context.app_id, logkit)
 
     def __del__(self):
         # os.remove(self.location)
-        if self._logkit_handler:
-            current_app.logger.info('close logkit handler: %s', self._logkit_handler.uri)
-            self._logkit_handler.close()
-        self._logkit.handlers.clear()
         del self.module
 
 
 class RuntimeContext(object):
     def __init__(self, user_id, app_id, node_id):
         self.request_id = None
         self.user_id = user_id
```

### Comparing `suanpan-sprt-0.6.7/sprt/master.py` & `suanpan-sprt-0.7.0/sprt/master.py`

 * *Files identical despite different names*

### Comparing `suanpan-sprt-0.6.7/sprt/server.py` & `suanpan-sprt-0.7.0/sprt/server.py`

 * *Files 2% similar despite different names*

```diff
@@ -8,14 +8,15 @@
 import pydantic
 from quart import current_app
 from contextlib import redirect_stdout, redirect_stderr, contextmanager
 from quart import Quart
 from quart_schema import QuartSchema, validate_request, validate_response, RequestSchemaValidationError
 from quart_schema import validation
 from . import loader, envs, exceptions, utils
+from .log import LogManager
 
 
 @dataclasses.dataclass
 class LogkitInfo:
     uri: str
     path: str
     namespace: typing.Optional[str] = "/logkit"
@@ -162,14 +163,16 @@
         if node_function.context.app_id == app_id:
             del_nodes.append(node_id)
 
     for node_id in del_nodes:
         current_app.logger.info(f'node {node_id} release')
         del module_imported[node_id]
 
+    LogManager.clear_logger(app_id)
+
     gc.collect()
 
 module_imported = {}
 
 
 def load(data: FunctionParams, default_dir):
     user_id = data.context.user_id
```

### Comparing `suanpan-sprt-0.6.7/sprt/storage.py` & `suanpan-sprt-0.7.0/sprt/storage.py`

 * *Files identical despite different names*

### Comparing `suanpan-sprt-0.6.7/sprt/testing.py` & `suanpan-sprt-0.7.0/sprt/testing.py`

 * *Files identical despite different names*

### Comparing `suanpan-sprt-0.6.7/sprt/utils.py` & `suanpan-sprt-0.7.0/sprt/utils.py`

 * *Files identical despite different names*

