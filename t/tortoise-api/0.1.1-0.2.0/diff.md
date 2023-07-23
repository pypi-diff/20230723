# Comparing `tmp/tortoise-api-0.1.1.tar.gz` & `tmp/tortoise-api-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "tortoise-api-0.1.1.tar", last modified: Thu Jul 20 23:27:06 2023, max compression
+gzip compressed data, was "tortoise-api-0.2.0.tar", last modified: Sun Jul 23 16:25:20 2023, max compression
```

## Comparing `tortoise-api-0.1.1.tar` & `tortoise-api-0.2.0.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxr-xr-x   0 sol        (501) staff       (20)        0 2023-07-20 23:27:06.082958 tortoise-api-0.1.1/
--rw-r--r--   0 sol        (501) staff       (20)     1069 2023-07-20 16:06:42.000000 tortoise-api-0.1.1/LICENSE
--rw-r--r--   0 sol        (501) staff       (20)     2412 2023-07-20 23:27:06.082716 tortoise-api-0.1.1/PKG-INFO
--rw-r--r--   0 sol        (501) staff       (20)     1911 2023-07-20 16:15:02.000000 tortoise-api-0.1.1/README.md
--rw-r--r--   0 sol        (501) staff       (20)      681 2023-07-20 23:25:59.000000 tortoise-api-0.1.1/pyproject.toml
--rw-r--r--   0 sol        (501) staff       (20)       38 2023-07-20 23:27:06.083019 tortoise-api-0.1.1/setup.cfg
-drwxr-xr-x   0 sol        (501) staff       (20)        0 2023-07-20 23:27:06.081183 tortoise-api-0.1.1/tortoise_api/
--rw-r--r--   0 sol        (501) staff       (20)       21 2023-07-20 18:33:16.000000 tortoise-api-0.1.1/tortoise_api/__init__.py
--rw-r--r--   0 sol        (501) staff       (20)     2521 2023-07-20 18:22:34.000000 tortoise-api-0.1.1/tortoise_api/api.py
--rw-r--r--   0 sol        (501) staff       (20)     1018 2023-07-20 23:25:38.000000 tortoise-api-0.1.1/tortoise_api/util.py
-drwxr-xr-x   0 sol        (501) staff       (20)        0 2023-07-20 23:27:06.082433 tortoise-api-0.1.1/tortoise_api.egg-info/
--rw-r--r--   0 sol        (501) staff       (20)     2412 2023-07-20 23:27:06.000000 tortoise-api-0.1.1/tortoise_api.egg-info/PKG-INFO
--rw-r--r--   0 sol        (501) staff       (20)      277 2023-07-20 23:27:06.000000 tortoise-api-0.1.1/tortoise_api.egg-info/SOURCES.txt
--rw-r--r--   0 sol        (501) staff       (20)        1 2023-07-20 23:27:06.000000 tortoise-api-0.1.1/tortoise_api.egg-info/dependency_links.txt
--rw-r--r--   0 sol        (501) staff       (20)       59 2023-07-20 23:27:06.000000 tortoise-api-0.1.1/tortoise_api.egg-info/requires.txt
--rw-r--r--   0 sol        (501) staff       (20)       13 2023-07-20 23:27:06.000000 tortoise-api-0.1.1/tortoise_api.egg-info/top_level.txt
+drwxr-xr-x   0 sol        (501) staff       (20)        0 2023-07-23 16:25:20.259421 tortoise-api-0.2.0/
+-rw-r--r--   0 sol        (501) staff       (20)     1069 2023-07-20 16:06:42.000000 tortoise-api-0.2.0/LICENSE
+-rw-r--r--   0 sol        (501) staff       (20)     2410 2023-07-23 16:25:20.259193 tortoise-api-0.2.0/PKG-INFO
+-rw-r--r--   0 sol        (501) staff       (20)     1911 2023-07-20 16:15:02.000000 tortoise-api-0.2.0/README.md
+-rw-r--r--   0 sol        (501) staff       (20)      679 2023-07-23 11:38:30.000000 tortoise-api-0.2.0/pyproject.toml
+-rw-r--r--   0 sol        (501) staff       (20)       38 2023-07-23 16:25:20.259477 tortoise-api-0.2.0/setup.cfg
+drwxr-xr-x   0 sol        (501) staff       (20)        0 2023-07-23 16:25:20.257853 tortoise-api-0.2.0/tortoise_api/
+-rw-r--r--   0 sol        (501) staff       (20)       21 2023-07-20 18:33:16.000000 tortoise-api-0.2.0/tortoise_api/__init__.py
+-rw-r--r--   0 sol        (501) staff       (20)     3136 2023-07-23 11:37:57.000000 tortoise-api-0.2.0/tortoise_api/api.py
+-rw-r--r--   0 sol        (501) staff       (20)     1663 2023-07-23 11:35:37.000000 tortoise-api-0.2.0/tortoise_api/util.py
+drwxr-xr-x   0 sol        (501) staff       (20)        0 2023-07-23 16:25:20.258933 tortoise-api-0.2.0/tortoise_api.egg-info/
+-rw-r--r--   0 sol        (501) staff       (20)     2410 2023-07-23 16:25:20.000000 tortoise-api-0.2.0/tortoise_api.egg-info/PKG-INFO
+-rw-r--r--   0 sol        (501) staff       (20)      277 2023-07-23 16:25:20.000000 tortoise-api-0.2.0/tortoise_api.egg-info/SOURCES.txt
+-rw-r--r--   0 sol        (501) staff       (20)        1 2023-07-23 16:25:20.000000 tortoise-api-0.2.0/tortoise_api.egg-info/dependency_links.txt
+-rw-r--r--   0 sol        (501) staff       (20)       59 2023-07-23 16:25:20.000000 tortoise-api-0.2.0/tortoise_api.egg-info/requires.txt
+-rw-r--r--   0 sol        (501) staff       (20)       13 2023-07-23 16:25:20.000000 tortoise-api-0.2.0/tortoise_api.egg-info/top_level.txt
```

### Comparing `tortoise-api-0.1.1/LICENSE` & `tortoise-api-0.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `tortoise-api-0.1.1/PKG-INFO` & `tortoise-api-0.2.0/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 Metadata-Version: 2.1
 Name: tortoise-api
-Version: 0.1.1
+Version: 0.2.0
 Summary: Simplest fastest minimal REST API CRUD generator for Tortoise ORM models
 Author-email: Artemiev <mixartemev@gmail.com>
 License: MIT
 Project-URL: Homepage, https://github.com/mixartemev/tortoise-api
 Project-URL: Repository, https://github.com/mixartemev/tortoise-api
-Keywords: starlette,fastapi,admin,dashboard,datatables,crud,tortoise-orm,ASGI-admin
+Keywords: starlette,fastapi,admin,generator,db-model,crud,tortoise-orm,ASGI-admin
 Requires-Python: >=3.9
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # Tortoise-API
 ###### Simplest fastest minimal REST API CRUD generator for Tortoise ORM models.
 Fully async Zero config One line ASGI app
```

### Comparing `tortoise-api-0.1.1/README.md` & `tortoise-api-0.2.0/README.md`

 * *Files identical despite different names*

### Comparing `tortoise-api-0.1.1/pyproject.toml` & `tortoise-api-0.2.0/pyproject.toml`

 * *Files 6% similar despite different names*

```diff
@@ -1,25 +1,25 @@
 [project]
 name = "tortoise-api"
 requires-python = ">=3.9"
 authors = [
     {name = "Artemiev", email = "mixartemev@gmail.com"},
 ]
-keywords = ["starlette", "fastapi", "admin", "dashboard", "datatables", "crud", "tortoise-orm", "ASGI-admin"]
+keywords = ["starlette", "fastapi", "admin", "generator", "db-model", "crud", "tortoise-orm", "ASGI-admin"]
 description = "Simplest fastest minimal REST API CRUD generator for Tortoise ORM models"
 readme = "README.md"
 license = {text = "MIT"}
 dependencies = [
     "asyncpg",
     "python-dotenv",
     "starlette",
     "tortoise-api-model",
     "uvicorn"
 ]
-version = "0.1.1"
+version = "0.2.0"
 
 [project.urls]
 Homepage = "https://github.com/mixartemev/tortoise-api"
 Repository = "https://github.com/mixartemev/tortoise-api"
 
 [tool.setuptools]
 packages = ["tortoise_api"]
```

### Comparing `tortoise-api-0.1.1/tortoise_api/api.py` & `tortoise-api-0.2.0/tortoise_api/api.py`

 * *Files 25% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 from starlette.requests import Request
 from starlette.responses import JSONResponse, Response
 from starlette.routing import Route
 from starlette.templating import Jinja2Templates
 from tortoise.contrib.starlette import register_tortoise
 from tortoise_api_model import Model
 
-from tortoise_api.util import jsonify
+from tortoise_api.util import jsonify, upsert, update, delete
 
 
 class Api:
     app: Starlette
     models: {str: Model}
 
     def __init__(
@@ -24,17 +24,17 @@
         """
         Parameters:
             debug: Debug SQL queries, api requests
             # auth_provider: Authentication Provider
         """
         self.templates = Jinja2Templates("templates")
         self.routes: [Route] = [
-            Route('/{model}/{oid}', self.api_one, methods=['GET', 'POST']),
+            Route('/{model}/{oid}', self.one_update, methods=['GET', 'POST', 'DELETE']),
             Route('/favicon.ico', lambda req: Response(), methods=['GET']),  # avoid chrome auto favicon load
-            Route('/{model}', self.api_all, methods=['GET', 'POST']),
+            Route('/{model}', self.all_create, methods=['GET', 'POST']),
             Route('/', self.api_menu, methods=['GET']),
         ]
         self.debug = debug
 
     def start(self, models_module):
         self.models = {key: model for key in dir(models_module) if isinstance(model := getattr(models_module, key), type(Model)) and model.mro()[1]==Model}
         if self.debug:
@@ -44,23 +44,33 @@
         register_tortoise(self.app, db_url=env("DB_URL"), modules={"models": [models_module]}, generate_schemas=self.debug)
         return self.app
 
     # ROUTES
     async def api_menu(self, _: Request):
         return JSONResponse(list(self.models))
 
-    async def api_all(self, request: Request):
-        model: Model = self._get_model(request)
+    async def all_create(self, request: Request):
+        model: type[Model] = self._get_model(request)
+        if request.method == 'POST':
+            res = await upsert(model, await request.json())
+            return JSONResponse(jsonify(res[0]), status_code={True: 201, False: 202}[res[1]]) # create
         objects: [Model] = await model.all().prefetch_related(*model._meta.fetch_fields)
         data = [jsonify(obj) for obj in objects]
-        return JSONResponse({'data': data})
+        return JSONResponse({'data': data}) # show all
 
-    async def api_one(self, request: Request):
-        model: Model = self._get_model(request)
-        obj = await self._get_model(request).get(id=request.path_params['oid']).prefetch_related(*model._meta.fetch_fields)
-        return JSONResponse(jsonify(obj))
+    async def one_update(self, request: Request):
+        model: type[Model] = self._get_model(request)
+        oid = request.path_params['oid']
+        if request.method == 'POST':
+            res = await update(model, await request.json(), oid)
+            return JSONResponse(jsonify(res[0]), status_code=202) # update
+        elif request.method == 'DELETE':
+            res = await delete(model, oid)
+            return JSONResponse(jsonify(res[0]), status_code=202) # update
+        obj = await model.get(id=oid).prefetch_related(*model._meta.fetch_fields)
+        return JSONResponse(jsonify(obj)) # show one
 
 
     # UTILS
-    def _get_model(self, request: Request) -> type(Model):
+    def _get_model(self, request: Request) -> type[Model]:
         model_id: str = request.path_params['model']
         return self.models.get(model_id)
```

### Comparing `tortoise-api-0.1.1/tortoise_api.egg-info/PKG-INFO` & `tortoise-api-0.2.0/tortoise_api.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 Metadata-Version: 2.1
 Name: tortoise-api
-Version: 0.1.1
+Version: 0.2.0
 Summary: Simplest fastest minimal REST API CRUD generator for Tortoise ORM models
 Author-email: Artemiev <mixartemev@gmail.com>
 License: MIT
 Project-URL: Homepage, https://github.com/mixartemev/tortoise-api
 Project-URL: Repository, https://github.com/mixartemev/tortoise-api
-Keywords: starlette,fastapi,admin,dashboard,datatables,crud,tortoise-orm,ASGI-admin
+Keywords: starlette,fastapi,admin,generator,db-model,crud,tortoise-orm,ASGI-admin
 Requires-Python: >=3.9
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # Tortoise-API
 ###### Simplest fastest minimal REST API CRUD generator for Tortoise ORM models.
 Fully async Zero config One line ASGI app
```

