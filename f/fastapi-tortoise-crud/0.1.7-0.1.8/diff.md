# Comparing `tmp/fastapi-tortoise-crud-0.1.7.tar.gz` & `tmp/fastapi-tortoise-crud-0.1.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "fastapi-tortoise-crud-0.1.7.tar", last modified: Thu Oct 20 12:58:56 2022, max compression
+gzip compressed data, was "fastapi-tortoise-crud-0.1.8.tar", last modified: Sun Jul 23 07:57:51 2023, max compression
```

## Comparing `fastapi-tortoise-crud-0.1.7.tar` & `fastapi-tortoise-crud-0.1.8.tar`

### file list

```diff
@@ -1,7 +1,11 @@
--rw-rw-rw-   0        0        0      151 2022-10-16 07:09:46.193960 fastapi-tortoise-crud-0.1.7/fastapi_tortoise_crud/__init__.py
--rw-rw-rw-   0        0        0     4979 2022-10-20 12:58:10.871076 fastapi-tortoise-crud-0.1.7/fastapi_tortoise_crud/crud.py
--rw-rw-rw-   0        0        0     3373 2022-10-18 14:21:04.357427 fastapi-tortoise-crud-0.1.7/fastapi_tortoise_crud/model.py
--rw-rw-rw-   0        0        0     1646 2022-10-18 15:42:10.438561 fastapi-tortoise-crud-0.1.7/fastapi_tortoise_crud/response_code.py
--rw-rw-rw-   0        0        0      649 2022-10-20 12:58:22.726026 fastapi-tortoise-crud-0.1.7/pyproject.toml
--rw-rw-rw-   0        0        0       21 2022-10-16 05:38:09.414000 fastapi-tortoise-crud-0.1.7/README.md
--rw-rw-rw-   0        0        0      273 2022-10-20 12:58:56.434125 fastapi-tortoise-crud-0.1.7/PKG-INFO
+-rw-r--r--   0        0        0       93 2023-07-23 07:54:17.352545 fastapi-tortoise-crud-0.1.8/fastapi_tortoise_crud/__init__.py
+-rw-r--r--   0        0        0      278 2023-07-23 07:54:31.685696 fastapi-tortoise-crud-0.1.8/fastapi_tortoise_crud/__pycache__/__init__.cpython-310.pyc
+-rw-r--r--   0        0        0     5696 2023-07-23 07:53:59.970551 fastapi-tortoise-crud-0.1.8/fastapi_tortoise_crud/__pycache__/crud.cpython-310.pyc
+-rw-r--r--   0        0        0     5000 2023-07-23 07:54:00.046552 fastapi-tortoise-crud-0.1.8/fastapi_tortoise_crud/__pycache__/model.cpython-310.pyc
+-rw-r--r--   0        0        0      655 2023-07-23 07:54:00.090527 fastapi-tortoise-crud-0.1.8/fastapi_tortoise_crud/__pycache__/response.cpython-310.pyc
+-rw-r--r--   0        0        0     5800 2023-07-23 07:52:48.111105 fastapi-tortoise-crud-0.1.8/fastapi_tortoise_crud/crud.py
+-rw-r--r--   0        0        0     3772 2023-07-23 07:48:02.667719 fastapi-tortoise-crud-0.1.8/fastapi_tortoise_crud/model.py
+-rw-r--r--   0        0        0      311 2023-07-23 07:50:11.624463 fastapi-tortoise-crud-0.1.8/fastapi_tortoise_crud/response.py
+-rw-r--r--   0        0        0      683 2023-07-23 07:56:44.753118 fastapi-tortoise-crud-0.1.8/pyproject.toml
+-rw-r--r--   0        0        0       21 2022-10-16 05:38:09.414000 fastapi-tortoise-crud-0.1.8/README.md
+-rw-r--r--   0        0        0      273 1970-01-01 00:00:00.000000 fastapi-tortoise-crud-0.1.8/PKG-INFO
```

### Comparing `fastapi-tortoise-crud-0.1.7/fastapi_tortoise_crud/model.py` & `fastapi-tortoise-crud-0.1.8/fastapi_tortoise_crud/model.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,18 +1,19 @@
 # -*- coding: utf-8 -*-
-""" 
+"""
 @author: moxiaoying
 @create: 2022/10/16
 @description: 基础模型
 """
 from tortoise import fields
 
 from typing import Type
 from tortoise.models import Model
 from tortoise.contrib.pydantic import pydantic_model_creator
+from pydantic import BaseConfig, Extra
 
 
 class BaseCrudMixin(Model):
     @classmethod
     async def create_one(cls, item: dict):
         return await cls.create(**item)
 
@@ -36,42 +37,51 @@
 
     @classmethod
     async def delete_many(cls, ids: list) -> int:
         deleted_count = await cls.filter(id__in=ids).delete()
         return deleted_count
 
 
+class ModelConfig(BaseConfig):
+    extra: Extra = Extra.ignore
+
+
 class BaseSchemaMixin:
     @classmethod
     def base_schema(cls: Type[Model], name, include=(), exclude=(), **kwargs):
         name = f'{cls.__name__}Schema{name}'
+        optional = kwargs.pop('optional', ()) or cls._meta.fields
+        # print(f'{name}\t{optional}')
         # include = kwargs.get('include', ())
         if include:
-            return pydantic_model_creator(cls, name=name, include=include, **kwargs)
-        return pydantic_model_creator(cls, name=name, exclude=exclude, **kwargs)
+            return pydantic_model_creator(cls, name=name, include=include, optional=optional, config_class=ModelConfig,
+                                          **kwargs)
+        return pydantic_model_creator(cls, name=name, config_class=ModelConfig, optional=optional, exclude=exclude,
+                                      **kwargs)
 
     @classmethod
     def schema_list(cls, name='List', include=(), exclude=(), **kwargs):
-        return cls.base_schema(name=name, include=include, exclude=exclude, **kwargs)
+        return cls.base_schema(name=name, include=include, exclude=exclude,  **kwargs)
 
     @classmethod
     def schema_create(cls, name='Create', include=(), exclude=(), **kwargs):
         return cls.base_schema(name, include=include, exclude=exclude, exclude_readonly=True, **kwargs)
 
     @classmethod
     def schema_read(cls, name='Read', include=(), exclude=(), **kwargs):
         return cls.base_schema(name, include=include, exclude=exclude, **kwargs)
 
     @classmethod
     def schema_update(cls, name='Update', include=(), exclude=(), **kwargs):
-        return cls.base_schema(name, include=include, exclude=exclude, exclude_readonly=True, **kwargs)
+        return cls.base_schema(name, include=include, exclude=exclude, exclude_readonly=True,
+                               **kwargs)
 
     @classmethod
-    def schema_filters(cls, name='Filters', include=('',), exclude=(), **kwargs):
-        return cls.base_schema(name, include=include, exclude=exclude, optional=include, exclude_readonly=True,
+    def schema_filters(cls, name='Filters', include=(), exclude=(), **kwargs):
+        return cls.base_schema(name, include=include, exclude=exclude, exclude_readonly=True,
                                **kwargs)
 
     @classmethod
     def schema_delete(cls):
         return int
```

### Comparing `fastapi-tortoise-crud-0.1.7/pyproject.toml` & `fastapi-tortoise-crud-0.1.8/pyproject.toml`

 * *Files 12% similar despite different names*

```diff
@@ -1,22 +1,23 @@
 [project]
 name = "fastapi-tortoise-crud"
-version = "0.1.7"
+version = "0.1.8"
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
-    "tortoise-orm>=0.19.2",
+    "tortoise-orm>=0.19.3",
     "fastapi>=0.85",
+    "fastapi-pagination>=0.12.6",
 ]
 requires-python = ">=3.9"
 readme = "README.md"
 
 [project.license]
 text = "MIT"
```

