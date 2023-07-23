# Comparing `tmp/steroid-0.6b0.tar.gz` & `tmp/steroid-0.7b0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "steroid-0.6b0.tar", max compression
+gzip compressed data, was "steroid-0.7b0.tar", max compression
```

## Comparing `steroid-0.6b0.tar` & `steroid-0.7b0.tar`

### file list

```diff
@@ -1,11 +1,12 @@
--rw-r--r--   0        0        0     1078 2023-07-20 15:00:50.985429 steroid-0.6b0/LICENSE
--rw-r--r--   0        0        0      199 2023-07-20 15:00:50.985429 steroid-0.6b0/README.md
--rw-r--r--   0        0        0      803 2023-07-20 15:01:21.993691 steroid-0.6b0/pyproject.toml
--rw-r--r--   0        0        0      164 2023-07-20 15:00:50.985429 steroid-0.6b0/steroid/__init__.py
--rw-r--r--   0        0        0     1689 2023-07-20 15:00:50.985429 steroid-0.6b0/steroid/app.py
--rw-r--r--   0        0        0     1112 2023-07-20 15:00:50.985429 steroid-0.6b0/steroid/controller.py
--rw-r--r--   0        0        0      971 2023-07-20 15:00:50.985429 steroid-0.6b0/steroid/logging.py
--rw-r--r--   0        0        0     1706 2023-07-20 15:00:50.985429 steroid-0.6b0/steroid/methods.py
--rw-r--r--   0        0        0     1808 2023-07-20 15:00:50.985429 steroid-0.6b0/steroid/middleware.py
--rw-r--r--   0        0        0      485 2023-07-20 15:00:50.985429 steroid-0.6b0/steroid/utils.py
--rw-r--r--   0        0        0     1322 1970-01-01 00:00:00.000000 steroid-0.6b0/PKG-INFO
+-rw-r--r--   0        0        0     1078 2023-07-23 18:15:42.378866 steroid-0.7b0/LICENSE
+-rw-r--r--   0        0        0     1886 2023-07-23 18:15:42.378866 steroid-0.7b0/README.md
+-rw-r--r--   0        0        0      924 2023-07-23 18:16:02.347378 steroid-0.7b0/pyproject.toml
+-rw-r--r--   0        0        0      164 2023-07-23 18:15:42.378866 steroid-0.7b0/steroid/__init__.py
+-rw-r--r--   0        0        0     1272 2023-07-23 18:15:42.378866 steroid-0.7b0/steroid/app.py
+-rw-r--r--   0        0        0      253 2023-07-23 18:15:42.378866 steroid-0.7b0/steroid/constants.py
+-rw-r--r--   0        0        0     2309 2023-07-23 18:15:42.378866 steroid-0.7b0/steroid/controller.py
+-rw-r--r--   0        0        0     2430 2023-07-23 18:15:42.378866 steroid-0.7b0/steroid/logging.py
+-rw-r--r--   0        0        0     1828 2023-07-23 18:15:42.378866 steroid-0.7b0/steroid/methods.py
+-rw-r--r--   0        0        0     2695 2023-07-23 18:15:42.378866 steroid-0.7b0/steroid/middleware.py
+-rw-r--r--   0        0        0      485 2023-07-23 18:15:42.378866 steroid-0.7b0/steroid/utils.py
+-rw-r--r--   0        0        0     3220 1970-01-01 00:00:00.000000 steroid-0.7b0/PKG-INFO
```

### Comparing `steroid-0.6b0/LICENSE` & `steroid-0.7b0/LICENSE`

 * *Files identical despite different names*

### Comparing `steroid-0.6b0/pyproject.toml` & `steroid-0.7b0/pyproject.toml`

 * *Files 14% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [tool.poetry]
 name = "steroid"
-version = "v0.6b"
+version = "v0.7b"
 authors = [
   "Mohammed Al Ameen <ameenmohammed2311@gmail.com>"
 ]
 description = "Steroid"
 readme = "README.md"
 
 repository = "https://github.com/struckchure/steroid"
@@ -20,18 +20,24 @@
   "Operating System :: OS Independent",
 ]
 
 [tool.poetry.dependencies]
 python = "^3.8"
 annotated-types = "0.5.0"
 anyio = "3.7.1"
+black = "23.7.0"
 click = "8.1.5"
 exceptiongroup = "1.1.2"
 fastapi = "0.100.0"
 h11 = "0.14.0"
 idna = "3.4"
+mypy-extensions = "1.0.0"
+packaging = "23.1"
+pathspec = "0.11.1"
+platformdirs = "3.9.1"
 pydantic = "2.0.3"
 pydantic-core = "2.3.0"
 sniffio = "1.3.0"
 starlette = "0.27.0"
+tomli = "2.0.1"
 typing-extensions = "4.7.1"
 uvicorn = "0.23.0"
```

### Comparing `steroid-0.6b0/steroid/app.py` & `steroid-0.7b0/steroid/app.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,68 +1,46 @@
 import os
+from typing import Union
 
 import uvicorn
 from fastapi import FastAPI
-from watchfiles import Change, DefaultFilter, run_process
 
+from steroid.constants import APP_COMPONENT, APP_COMPONENT_TYPE, APP_CONTROLLER
 from steroid.controller import Controller
-from steroid.logging import getLogger
-from steroid.utils import clearTerminal, removeLeadingOrTrailingSlash
-
-
-class OnlyPythonFilesFilter(DefaultFilter):
-    allowed_extensions = ".py"
-
-    def __call__(self, change: Change, path: str) -> bool:
-        return super().__call__(change, path) and path.endswith(self.allowed_extensions)
+from steroid.logging import getLogConfig, getLogger
+from steroid.utils import clearTerminal
 
 
 class CreateApp:
     _APP: FastAPI = None
-    logger = getLogger()
+    logger = None
 
     def __new__(cls, *args, **kwargs):
         if cls._APP is None:
+            cls.logger = getLogger()
             cls._APP = FastAPI(*args, **kwargs)
 
         return cls
 
     @classmethod
     @property
     def app(cls):
         return cls._APP
 
     @classmethod
-    def _start(cls):
+    def start(cls, host: str = "0.0.0.0", port: int = 8000):
         clearTerminal()
 
-        uvicorn.run(cls.app)
+        uvicorn.run(cls.app, host=host, port=port, log_config=getLogConfig())
 
     @classmethod
-    def onFileChange(cls, change: Change):
-        getLogger().info(f"reloading ... file changes in {change}")
+    def addController(cls, controller):
+        componentType = getattr(controller, APP_COMPONENT_TYPE, None)
+        component: Union[Controller, None] = getattr(controller, APP_COMPONENT, None)
 
-    @classmethod
-    def start(cls, reload=True):
-        if reload == False:
-            cls._start()
-            return
-
-        watchFilePath = os.getcwd()
-
-        run_process(
-            watchFilePath,
-            target=cls._start,
-            callback=cls.onFileChange,
-            watch_filter=OnlyPythonFilesFilter(),
-        )
+        if not componentType == APP_CONTROLLER:
+            raise Exception(f"Controller component must be of type {APP_CONTROLLER}")
 
-    @classmethod
-    def addController(cls, controller: Controller):
-        cls.app.include_router(
-            controller.router,
-            prefix=controller.path,
-            tags=[removeLeadingOrTrailingSlash(controller.path)]
-            if controller.path
-            else [],
-        )
-        cls.logger.info(f"Mapped {controller.path} to router")
+        if not component:
+            raise Exception(f"Controller component not detected")
+
+        component.setupController(cls.app)
```

### Comparing `steroid-0.6b0/steroid/methods.py` & `steroid-0.7b0/steroid/methods.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,52 +1,50 @@
 import inspect
 
-from steroid.utils import formatPath
+from steroid.constants import APP_COMPONENT, APP_COMPONENT_TYPE, APP_CONTROLLER_METHOD
+from steroid.utils import formatPath, removeLeadingOrTrailingSlash
 
 
 class BaseMethod:
-    _METHOD: str
+    _METHOD: str = None
+    _PATH: str = None
+    _FULL_PATH: str = None
+
+    _CONTROLLER = None
 
     def __init__(self, path: str = "", *args, **kwargs):
-        self.path = formatPath(path)
+        self._PATH = formatPath(path)
 
         self.args = args
         self.kwargs = kwargs
 
-        self.route = None
-
-    def __call__(self, func, router=None):
-        # TODO: alot feels very wrong in this method, help me!
-
+    def __call__(self, func):
         self.func = func
 
-        if router:
-            httpMethodDecorator = getattr(router, self._METHOD.lower())
-
-            def wrapper(*args, **kwargs):
-                return func(*args, **kwargs)
-
-            parameters = [
-                parameter
-                for parameter in dict(inspect.signature(func).parameters).values()
-            ]
-
-            httpMethodDecorator(self.path)(func)(*parameters)
-
-            return wrapper
-
         def wrapper(*args, **kwargs):
             return func(*args, **kwargs)
 
-        setattr(wrapper, "object", self)
+        setattr(wrapper, APP_COMPONENT_TYPE, APP_CONTROLLER_METHOD)
+        setattr(wrapper, APP_COMPONENT, self)
 
         return wrapper
 
-    def mapSelfToRouter(self, router):
-        self.__call__(self.func, router)
+    def setupMethod(self, controller):
+        self._CONTROLLER = controller
+
+        httpMethodDecorator = getattr(controller.router, self._METHOD.lower())
+        parameters = [
+            parameter
+            for parameter in dict(inspect.signature(self.func).parameters).values()
+        ]
+        httpMethodDecorator(self.path)(self.func)(*parameters)
+
+    @property
+    def path(self):
+        return f"/{removeLeadingOrTrailingSlash(self._PATH)}/"
 
 
 class Get(BaseMethod):
     _METHOD = "GET"
 
     def __init__(self, *args, **kwargs):
         super().__init__(*args, **kwargs)
```

