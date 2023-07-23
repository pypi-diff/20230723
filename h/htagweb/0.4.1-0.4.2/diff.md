# Comparing `tmp/htagweb-0.4.1.tar.gz` & `tmp/htagweb-0.4.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "htagweb-0.4.1.tar", max compression
+gzip compressed data, was "htagweb-0.4.2.tar", max compression
```

## Comparing `htagweb-0.4.1.tar` & `htagweb-0.4.2.tar`

### file list

```diff
@@ -1,11 +1,11 @@
--rw-r--r--   0        0        0     1065 2023-07-22 12:55:44.754644 htagweb-0.4.1/LICENSE
--rw-r--r--   0        0        0     3148 2023-07-22 12:55:44.754644 htagweb-0.4.1/README.md
--rw-r--r--   0        0        0      518 2023-07-22 12:55:45.050646 htagweb-0.4.1/htagweb/__init__.py
--rw-r--r--   0        0        0      421 2023-07-22 12:55:44.758643 htagweb-0.4.1/htagweb/__main__.py
--rw-r--r--   0        0        0     2521 2023-07-22 12:55:44.758643 htagweb-0.4.1/htagweb/crypto.py
--rw-r--r--   0        0        0    10493 2023-07-22 12:55:44.758643 htagweb-0.4.1/htagweb/htagserver.py
--rw-r--r--   0        0        0     3797 2023-07-22 12:55:44.758643 htagweb-0.4.1/htagweb/manager.py
--rw-r--r--   0        0        0     5543 2023-07-22 12:55:44.758643 htagweb-0.4.1/htagweb/uidprocess.py
--rw-r--r--   0        0        0     9904 2023-07-22 12:55:44.758643 htagweb-0.4.1/htagweb/webbase.py
--rw-r--r--   0        0        0     1124 2023-07-22 12:55:45.050646 htagweb-0.4.1/pyproject.toml
--rw-r--r--   0        0        0     4350 1970-01-01 00:00:00.000000 htagweb-0.4.1/PKG-INFO
+-rw-r--r--   0        0        0     1065 2023-07-23 08:37:12.344180 htagweb-0.4.2/LICENSE
+-rw-r--r--   0        0        0     3148 2023-07-23 08:37:12.344180 htagweb-0.4.2/README.md
+-rw-r--r--   0        0        0      518 2023-07-23 08:37:12.920194 htagweb-0.4.2/htagweb/__init__.py
+-rw-r--r--   0        0        0      421 2023-07-23 08:37:12.344180 htagweb-0.4.2/htagweb/__main__.py
+-rw-r--r--   0        0        0     2521 2023-07-23 08:37:12.344180 htagweb-0.4.2/htagweb/crypto.py
+-rw-r--r--   0        0        0    10670 2023-07-23 08:37:12.344180 htagweb-0.4.2/htagweb/htagserver.py
+-rw-r--r--   0        0        0     3797 2023-07-23 08:37:12.344180 htagweb-0.4.2/htagweb/manager.py
+-rw-r--r--   0        0        0     5659 2023-07-23 08:37:12.344180 htagweb-0.4.2/htagweb/uidprocess.py
+-rw-r--r--   0        0        0     9925 2023-07-23 08:37:12.344180 htagweb-0.4.2/htagweb/webbase.py
+-rw-r--r--   0        0        0     1124 2023-07-23 08:37:12.920194 htagweb-0.4.2/pyproject.toml
+-rw-r--r--   0        0        0     4350 1970-01-01 00:00:00.000000 htagweb-0.4.2/PKG-INFO
```

### Comparing `htagweb-0.4.1/LICENSE` & `htagweb-0.4.2/LICENSE`

 * *Files identical despite different names*

### Comparing `htagweb-0.4.1/README.md` & `htagweb-0.4.2/README.md`

 * *Files identical despite different names*

### Comparing `htagweb-0.4.1/htagweb/__init__.py` & `htagweb-0.4.2/htagweb/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -10,8 +10,8 @@
 from .webbase import WebServer
 from .webbase import WebServerWS
 
 from .htagserver import HtagServer  # a completly different beast.
 
 __all__= ["WebServer","WebServerWS","HtagServer"]
 
-__version__ = "0.4.1" # auto updated
+__version__ = "0.4.2" # auto updated
```

### Comparing `htagweb-0.4.1/htagweb/crypto.py` & `htagweb-0.4.2/htagweb/crypto.py`

 * *Files identical despite different names*

### Comparing `htagweb-0.4.1/htagweb/htagserver.py` & `htagweb-0.4.2/htagweb/htagserver.py`

 * *Files 3% similar despite different names*

```diff
@@ -163,14 +163,20 @@
             pass
     else:
         module=importlib.import_module(modulename)
     #---------------------------
     klass= getattr(module,name)
     if not ( inspect.isclass(klass) and issubclass(klass,Tag) ):
         raise Exception(f"'{fqn}' is not a htag.Tag subclass")
+
+    if not hasattr(klass,"imports"):
+        # if klass doesn't declare its imports
+        # we prefer to set them empty
+        # to avoid clutering
+        klass.imports=[]
     return klass
 
 class HRSocket(WebSocketEndpoint):
     encoding = "text"
 
     async def _sendback(self,ws, txt:str) -> bool:
         try:
```

### Comparing `htagweb-0.4.1/htagweb/manager.py` & `htagweb-0.4.2/htagweb/manager.py`

 * *Files identical despite different names*

### Comparing `htagweb-0.4.1/htagweb/uidprocess.py` & `htagweb-0.4.2/htagweb/uidprocess.py`

 * *Files 5% similar despite different names*

```diff
@@ -32,16 +32,19 @@
             if init_params is None : init_params=((),{})
 
             hr=HTS.get(fqn)
             if renew or (hr is None) or str(init_params)!=str(hr.init):
                 ##HRenderer(tagClass: type, js:str, exit_callback:Optional[Callable]=None, init= ((),{}), fullerror=False, statics=[], session=None ):
 
                 #--------------------------- fqn -> module, name
-                names = fqn.split(".")
-                modulename,name=".".join(names[:-1]), names[-1]
+                if ":" in fqn:
+                    modulename,name = fqn.split(":",1)
+                else:
+                    names = fqn.split(".")
+                    modulename,name=".".join(names[:-1]), names[-1]
                 if modulename in sys.modules:
                     module=sys.modules[modulename]
                     try:
                         module=importlib.reload( module )
                     except ModuleNotFoundError:
                         """ can't be (really) reloaded if the component is in the
                         same module as the instance htag server"""
```

### Comparing `htagweb-0.4.1/htagweb/webbase.py` & `htagweb-0.4.2/htagweb/webbase.py`

 * *Files 1% similar despite different names*

```diff
@@ -111,15 +111,15 @@
         await self.app(scope, receive, send_wrapper)
 
 
 
 
 def findfqn(x) -> str:
     if isinstance(x,str):
-        if "." not in x:
+        if ("." not in x) and (":" not in x):
             raise Exception(f"'{x}' is not a 'full qualified name' (expected 'module.name') of an App (htag.Tag class)")
         return x    # /!\ x is a fqn /!\ DANGEROUS /!\
     elif isinstance(x, ModuleType):
         if hasattr(x,"App"):
             tagClass=getattr(x,"App")
             if not issubclass(tagClass,Tag):
                 raise Exception("The 'App' of the module is not inherited from 'htag.Tag class'")
```

### Comparing `htagweb-0.4.1/pyproject.toml` & `htagweb-0.4.2/pyproject.toml`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "htagweb"
-version = "0.4.1" # auto-updated
+version = "0.4.2" # auto-updated
 description = "It's a robust webserver (http/ws) for hosting htag apps on the web (a process by user)"
 authors = ["manatlan <manatlan@gmail.com>"]
 readme = 'README.md'
 license="MIT"
 keywords=['htag','webserver']
 homepage = "https://github.com/manatlan/htagweb"
 repository = "https://github.com/manatlan/htagweb"
```

### Comparing `htagweb-0.4.1/PKG-INFO` & `htagweb-0.4.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: htagweb
-Version: 0.4.1
+Version: 0.4.2
 Summary: It's a robust webserver (http/ws) for hosting htag apps on the web (a process by user)
 Home-page: https://github.com/manatlan/htagweb
 License: MIT
 Keywords: htag,webserver
 Author: manatlan
 Author-email: manatlan@gmail.com
 Requires-Python: >=3.8,<4.0
```

