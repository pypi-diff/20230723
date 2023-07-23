# Comparing `tmp/fastapi-tortoise-crud-0.1.8.tar.gz` & `tmp/fastapi-tortoise-crud-0.1.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "fastapi-tortoise-crud-0.1.8.tar", last modified: Sun Jul 23 07:57:51 2023, max compression
+gzip compressed data, was "fastapi-tortoise-crud-0.1.9.tar", last modified: Sun Jul 23 08:21:08 2023, max compression
```

## Comparing `fastapi-tortoise-crud-0.1.8.tar` & `fastapi-tortoise-crud-0.1.9.tar`

### file list

```diff
@@ -1,11 +1,11 @@
--rw-r--r--   0        0        0       93 2023-07-23 07:54:17.352545 fastapi-tortoise-crud-0.1.8/fastapi_tortoise_crud/__init__.py
--rw-r--r--   0        0        0      278 2023-07-23 07:54:31.685696 fastapi-tortoise-crud-0.1.8/fastapi_tortoise_crud/__pycache__/__init__.cpython-310.pyc
--rw-r--r--   0        0        0     5696 2023-07-23 07:53:59.970551 fastapi-tortoise-crud-0.1.8/fastapi_tortoise_crud/__pycache__/crud.cpython-310.pyc
--rw-r--r--   0        0        0     5000 2023-07-23 07:54:00.046552 fastapi-tortoise-crud-0.1.8/fastapi_tortoise_crud/__pycache__/model.cpython-310.pyc
--rw-r--r--   0        0        0      655 2023-07-23 07:54:00.090527 fastapi-tortoise-crud-0.1.8/fastapi_tortoise_crud/__pycache__/response.cpython-310.pyc
--rw-r--r--   0        0        0     5800 2023-07-23 07:52:48.111105 fastapi-tortoise-crud-0.1.8/fastapi_tortoise_crud/crud.py
--rw-r--r--   0        0        0     3772 2023-07-23 07:48:02.667719 fastapi-tortoise-crud-0.1.8/fastapi_tortoise_crud/model.py
--rw-r--r--   0        0        0      311 2023-07-23 07:50:11.624463 fastapi-tortoise-crud-0.1.8/fastapi_tortoise_crud/response.py
--rw-r--r--   0        0        0      683 2023-07-23 07:56:44.753118 fastapi-tortoise-crud-0.1.8/pyproject.toml
--rw-r--r--   0        0        0       21 2022-10-16 05:38:09.414000 fastapi-tortoise-crud-0.1.8/README.md
--rw-r--r--   0        0        0      273 1970-01-01 00:00:00.000000 fastapi-tortoise-crud-0.1.8/PKG-INFO
+-rw-r--r--   0        0        0       93 2023-07-23 07:54:17.352545 fastapi-tortoise-crud-0.1.9/fastapi_tortoise_crud/__init__.py
+-rw-r--r--   0        0        0      278 2023-07-23 07:54:31.685696 fastapi-tortoise-crud-0.1.9/fastapi_tortoise_crud/__pycache__/__init__.cpython-310.pyc
+-rw-r--r--   0        0        0     5696 2023-07-23 07:53:59.970551 fastapi-tortoise-crud-0.1.9/fastapi_tortoise_crud/__pycache__/crud.cpython-310.pyc
+-rw-r--r--   0        0        0     5000 2023-07-23 07:54:00.046552 fastapi-tortoise-crud-0.1.9/fastapi_tortoise_crud/__pycache__/model.cpython-310.pyc
+-rw-r--r--   0        0        0      621 2023-07-23 08:11:33.832764 fastapi-tortoise-crud-0.1.9/fastapi_tortoise_crud/__pycache__/response.cpython-310.pyc
+-rw-r--r--   0        0        0     5800 2023-07-23 07:52:48.111105 fastapi-tortoise-crud-0.1.9/fastapi_tortoise_crud/crud.py
+-rw-r--r--   0        0        0     3772 2023-07-23 07:48:02.667719 fastapi-tortoise-crud-0.1.9/fastapi_tortoise_crud/model.py
+-rw-r--r--   0        0        0      274 2023-07-23 08:11:24.522429 fastapi-tortoise-crud-0.1.9/fastapi_tortoise_crud/response.py
+-rw-r--r--   0        0        0      686 2023-07-23 08:17:41.441611 fastapi-tortoise-crud-0.1.9/pyproject.toml
+-rw-r--r--   0        0        0       98 2023-07-23 08:15:41.291166 fastapi-tortoise-crud-0.1.9/README.md
+-rw-r--r--   0        0        0      347 1970-01-01 00:00:00.000000 fastapi-tortoise-crud-0.1.9/PKG-INFO
```

### Comparing `fastapi-tortoise-crud-0.1.8/fastapi_tortoise_crud/__pycache__/crud.cpython-310.pyc` & `fastapi-tortoise-crud-0.1.9/fastapi_tortoise_crud/__pycache__/crud.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `fastapi-tortoise-crud-0.1.8/fastapi_tortoise_crud/__pycache__/model.cpython-310.pyc` & `fastapi-tortoise-crud-0.1.9/fastapi_tortoise_crud/__pycache__/model.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `fastapi-tortoise-crud-0.1.8/fastapi_tortoise_crud/crud.py` & `fastapi-tortoise-crud-0.1.9/fastapi_tortoise_crud/crud.py`

 * *Files identical despite different names*

### Comparing `fastapi-tortoise-crud-0.1.8/fastapi_tortoise_crud/model.py` & `fastapi-tortoise-crud-0.1.9/fastapi_tortoise_crud/model.py`

 * *Files identical despite different names*

### Comparing `fastapi-tortoise-crud-0.1.8/pyproject.toml` & `fastapi-tortoise-crud-0.1.9/pyproject.toml`

 * *Files 18% similar despite different names*

```diff
@@ -1,22 +1,22 @@
 [project]
 name = "fastapi-tortoise-crud"
-version = "0.1.8"
+version = "0.1.9"
 description = "fastpi简单crud"
 keywords = [
     "Fastapi-admin",
     "Tortoise-orm",
     "Crud",
 ]
 authors = [
     { name = "moxiaoying", email = "768091671@qq.com" },
 ]
 dependencies = [
     "tortoise-orm>=0.19.3",
-    "fastapi>=0.85",
+    "fastapi>=0.100.0",
     "fastapi-pagination>=0.12.6",
 ]
 requires-python = ">=3.9"
 readme = "README.md"
 
 [project.license]
 text = "MIT"
```

