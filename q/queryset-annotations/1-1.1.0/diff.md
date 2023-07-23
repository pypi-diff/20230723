# Comparing `tmp/queryset_annotations-1.tar.gz` & `tmp/queryset_annotations-1.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "queryset_annotations-1.tar", last modified: Fri Jul 14 21:44:29 2023, max compression
+gzip compressed data, was "queryset_annotations-1.1.0.tar", last modified: Sun Jul 23 18:52:37 2023, max compression
```

## Comparing `queryset_annotations-1.tar` & `queryset_annotations-1.1.0.tar`

### file list

```diff
@@ -1,43 +1,51 @@
-drwxr-xr-x   0 gefest     (501) staff       (20)        0 2023-07-14 21:44:29.616780 queryset_annotations-1/
--rw-r--r--   0 gefest     (501) staff       (20)     1073 2023-07-07 16:13:35.000000 queryset_annotations-1/LICENSE
--rw-r--r--   0 gefest     (501) staff       (20)      260 2023-07-14 21:44:29.616372 queryset_annotations-1/PKG-INFO
--rw-r--r--   0 gefest     (501) staff       (20)     2066 2023-07-14 13:03:51.000000 queryset_annotations-1/README.md
-drwxr-xr-x   0 gefest     (501) staff       (20)        0 2023-07-14 21:44:29.601250 queryset_annotations-1/annotation/
--rw-r--r--   0 gefest     (501) staff       (20)        0 2023-07-07 19:16:10.000000 queryset_annotations-1/annotation/__init__.py
--rw-r--r--   0 gefest     (501) staff       (20)       63 2023-07-07 19:16:10.000000 queryset_annotations-1/annotation/admin.py
--rw-r--r--   0 gefest     (501) staff       (20)      152 2023-07-07 19:16:10.000000 queryset_annotations-1/annotation/apps.py
-drwxr-xr-x   0 gefest     (501) staff       (20)        0 2023-07-14 21:44:29.603825 queryset_annotations-1/annotation/migrations/
--rw-r--r--   0 gefest     (501) staff       (20)     1051 2023-07-14 11:29:08.000000 queryset_annotations-1/annotation/migrations/0001_initial.py
--rw-r--r--   0 gefest     (501) staff       (20)      587 2023-07-14 12:29:30.000000 queryset_annotations-1/annotation/migrations/0002_remove_author_book_alter_book_author.py
--rw-r--r--   0 gefest     (501) staff       (20)        0 2023-07-07 19:16:10.000000 queryset_annotations-1/annotation/migrations/__init__.py
--rw-r--r--   0 gefest     (501) staff       (20)      324 2023-07-14 12:29:21.000000 queryset_annotations-1/annotation/models.py
--rw-r--r--   0 gefest     (501) staff       (20)       60 2023-07-07 19:16:10.000000 queryset_annotations-1/annotation/tests.py
--rw-r--r--   0 gefest     (501) staff       (20)     1103 2023-07-14 12:29:21.000000 queryset_annotations-1/annotation/views.py
-drwxr-xr-x   0 gefest     (501) staff       (20)        0 2023-07-14 21:44:29.606880 queryset_annotations-1/example/
--rw-r--r--   0 gefest     (501) staff       (20)        0 2023-07-07 19:14:24.000000 queryset_annotations-1/example/__init__.py
--rw-r--r--   0 gefest     (501) staff       (20)      391 2023-07-07 19:14:24.000000 queryset_annotations-1/example/asgi.py
--rw-r--r--   0 gefest     (501) staff       (20)     3575 2023-07-14 11:31:34.000000 queryset_annotations-1/example/settings.py
--rw-r--r--   0 gefest     (501) staff       (20)     1306 2023-07-14 12:29:21.000000 queryset_annotations-1/example/urls.py
--rw-r--r--   0 gefest     (501) staff       (20)      391 2023-07-07 19:14:24.000000 queryset_annotations-1/example/wsgi.py
--rw-r--r--   0 gefest     (501) staff       (20)     2924 2023-07-07 23:17:25.000000 queryset_annotations-1/pyproject.toml
-drwxr-xr-x   0 gefest     (501) staff       (20)        0 2023-07-14 21:44:29.607539 queryset_annotations-1/queryset_annotations/
--rw-r--r--   0 gefest     (501) staff       (20)       75 2023-07-07 23:21:27.000000 queryset_annotations-1/queryset_annotations/__init__.py
-drwxr-xr-x   0 gefest     (501) staff       (20)        0 2023-07-14 21:44:29.611645 queryset_annotations-1/queryset_annotations/base/
--rw-r--r--   0 gefest     (501) staff       (20)       35 2023-07-07 17:10:49.000000 queryset_annotations-1/queryset_annotations/base/__init__.py
--rw-r--r--   0 gefest     (501) staff       (20)      807 2023-07-07 17:24:08.000000 queryset_annotations-1/queryset_annotations/base/abstract_annotation.py
--rw-r--r--   0 gefest     (501) staff       (20)      762 2023-07-07 22:05:47.000000 queryset_annotations-1/queryset_annotations/base/subquery_annotation.py
-drwxr-xr-x   0 gefest     (501) staff       (20)        0 2023-07-14 21:44:29.613225 queryset_annotations-1/queryset_annotations/mixins/
--rw-r--r--   0 gefest     (501) staff       (20)       37 2023-07-07 17:20:12.000000 queryset_annotations-1/queryset_annotations/mixins/__init__.py
--rw-r--r--   0 gefest     (501) staff       (20)      449 2023-07-07 17:36:26.000000 queryset_annotations-1/queryset_annotations/mixins/dependency_annotation.py
-drwxr-xr-x   0 gefest     (501) staff       (20)        0 2023-07-14 21:44:29.615475 queryset_annotations-1/queryset_annotations/proxy/
--rw-r--r--   0 gefest     (501) staff       (20)       41 2023-07-07 23:02:02.000000 queryset_annotations-1/queryset_annotations/proxy/__init__.py
--rw-r--r--   0 gefest     (501) staff       (20)     1844 2023-07-14 12:45:20.000000 queryset_annotations-1/queryset_annotations/proxy/meta.py
--rw-r--r--   0 gefest     (501) staff       (20)      213 2023-07-07 23:02:02.000000 queryset_annotations-1/queryset_annotations/proxy/model.py
-drwxr-xr-x   0 gefest     (501) staff       (20)        0 2023-07-14 21:44:29.609857 queryset_annotations-1/queryset_annotations.egg-info/
--rw-r--r--   0 gefest     (501) staff       (20)      260 2023-07-14 21:44:29.000000 queryset_annotations-1/queryset_annotations.egg-info/PKG-INFO
--rw-r--r--   0 gefest     (501) staff       (20)      982 2023-07-14 21:44:29.000000 queryset_annotations-1/queryset_annotations.egg-info/SOURCES.txt
--rw-r--r--   0 gefest     (501) staff       (20)        1 2023-07-14 21:44:29.000000 queryset_annotations-1/queryset_annotations.egg-info/dependency_links.txt
--rw-r--r--   0 gefest     (501) staff       (20)       12 2023-07-14 21:44:29.000000 queryset_annotations-1/queryset_annotations.egg-info/requires.txt
--rw-r--r--   0 gefest     (501) staff       (20)       40 2023-07-14 21:44:29.000000 queryset_annotations-1/queryset_annotations.egg-info/top_level.txt
--rw-r--r--   0 gefest     (501) staff       (20)       38 2023-07-14 21:44:29.616891 queryset_annotations-1/setup.cfg
--rw-r--r--   0 gefest     (501) staff       (20)      415 2023-07-07 17:20:12.000000 queryset_annotations-1/setup.py
+drwxr-xr-x   0 gefest     (501) staff       (20)        0 2023-07-23 18:52:37.847720 queryset_annotations-1.1.0/
+-rw-r--r--   0 gefest     (501) staff       (20)     1073 2023-07-07 16:13:35.000000 queryset_annotations-1.1.0/LICENSE
+-rw-r--r--   0 gefest     (501) staff       (20)     6614 2023-07-23 18:52:37.847462 queryset_annotations-1.1.0/PKG-INFO
+-rw-r--r--   0 gefest     (501) staff       (20)     4943 2023-07-23 18:51:44.000000 queryset_annotations-1.1.0/README.md
+drwxr-xr-x   0 gefest     (501) staff       (20)        0 2023-07-23 18:52:37.832852 queryset_annotations-1.1.0/annotation/
+-rw-r--r--   0 gefest     (501) staff       (20)        0 2023-07-07 19:16:10.000000 queryset_annotations-1.1.0/annotation/__init__.py
+-rw-r--r--   0 gefest     (501) staff       (20)       63 2023-07-07 19:16:10.000000 queryset_annotations-1.1.0/annotation/admin.py
+-rw-r--r--   0 gefest     (501) staff       (20)      152 2023-07-07 19:16:10.000000 queryset_annotations-1.1.0/annotation/apps.py
+drwxr-xr-x   0 gefest     (501) staff       (20)        0 2023-07-23 18:52:37.835313 queryset_annotations-1.1.0/annotation/migrations/
+-rw-r--r--   0 gefest     (501) staff       (20)     1051 2023-07-14 11:29:08.000000 queryset_annotations-1.1.0/annotation/migrations/0001_initial.py
+-rw-r--r--   0 gefest     (501) staff       (20)      587 2023-07-14 12:29:30.000000 queryset_annotations-1.1.0/annotation/migrations/0002_remove_author_book_alter_book_author.py
+-rw-r--r--   0 gefest     (501) staff       (20)        0 2023-07-07 19:16:10.000000 queryset_annotations-1.1.0/annotation/migrations/__init__.py
+-rw-r--r--   0 gefest     (501) staff       (20)      324 2023-07-14 12:29:21.000000 queryset_annotations-1.1.0/annotation/models.py
+-rw-r--r--   0 gefest     (501) staff       (20)       60 2023-07-07 19:16:10.000000 queryset_annotations-1.1.0/annotation/tests.py
+-rw-r--r--   0 gefest     (501) staff       (20)     1545 2023-07-23 18:40:25.000000 queryset_annotations-1.1.0/annotation/views.py
+drwxr-xr-x   0 gefest     (501) staff       (20)        0 2023-07-23 18:52:37.837687 queryset_annotations-1.1.0/example/
+-rw-r--r--   0 gefest     (501) staff       (20)        0 2023-07-07 19:14:24.000000 queryset_annotations-1.1.0/example/__init__.py
+-rw-r--r--   0 gefest     (501) staff       (20)      391 2023-07-07 19:14:24.000000 queryset_annotations-1.1.0/example/asgi.py
+-rw-r--r--   0 gefest     (501) staff       (20)     3575 2023-07-14 11:31:34.000000 queryset_annotations-1.1.0/example/settings.py
+-rw-r--r--   0 gefest     (501) staff       (20)     1306 2023-07-14 12:29:21.000000 queryset_annotations-1.1.0/example/urls.py
+-rw-r--r--   0 gefest     (501) staff       (20)      391 2023-07-07 19:14:24.000000 queryset_annotations-1.1.0/example/wsgi.py
+-rw-r--r--   0 gefest     (501) staff       (20)     3321 2023-07-23 18:48:18.000000 queryset_annotations-1.1.0/pyproject.toml
+drwxr-xr-x   0 gefest     (501) staff       (20)        0 2023-07-23 18:52:37.838878 queryset_annotations-1.1.0/queryset_annotations/
+-rw-r--r--   0 gefest     (501) staff       (20)       75 2023-07-07 23:21:27.000000 queryset_annotations-1.1.0/queryset_annotations/__init__.py
+drwxr-xr-x   0 gefest     (501) staff       (20)        0 2023-07-23 18:52:37.842464 queryset_annotations-1.1.0/queryset_annotations/base/
+-rw-r--r--   0 gefest     (501) staff       (20)       58 2023-07-23 18:48:17.000000 queryset_annotations-1.1.0/queryset_annotations/base/__init__.py
+-rw-r--r--   0 gefest     (501) staff       (20)     1083 2023-07-23 18:48:17.000000 queryset_annotations-1.1.0/queryset_annotations/base/abstract_annotation.py
+-rw-r--r--   0 gefest     (501) staff       (20)      243 2023-07-23 18:48:17.000000 queryset_annotations-1.1.0/queryset_annotations/base/context.py
+-rw-r--r--   0 gefest     (501) staff       (20)      762 2023-07-07 22:05:47.000000 queryset_annotations-1.1.0/queryset_annotations/base/subquery_annotation.py
+drwxr-xr-x   0 gefest     (501) staff       (20)        0 2023-07-23 18:52:37.843270 queryset_annotations-1.1.0/queryset_annotations/drf/
+-rw-r--r--   0 gefest     (501) staff       (20)        0 2023-07-23 18:48:17.000000 queryset_annotations-1.1.0/queryset_annotations/drf/__init__.py
+drwxr-xr-x   0 gefest     (501) staff       (20)        0 2023-07-23 18:52:37.843886 queryset_annotations-1.1.0/queryset_annotations/drf/views/
+-rw-r--r--   0 gefest     (501) staff       (20)       22 2023-07-23 18:48:17.000000 queryset_annotations-1.1.0/queryset_annotations/drf/views/__init__.py
+-rw-r--r--   0 gefest     (501) staff       (20)      512 2023-07-23 18:48:17.000000 queryset_annotations-1.1.0/queryset_annotations/drf/views/mixins.py
+drwxr-xr-x   0 gefest     (501) staff       (20)        0 2023-07-23 18:52:37.844938 queryset_annotations-1.1.0/queryset_annotations/mixins/
+-rw-r--r--   0 gefest     (501) staff       (20)       37 2023-07-07 17:20:12.000000 queryset_annotations-1.1.0/queryset_annotations/mixins/__init__.py
+-rw-r--r--   0 gefest     (501) staff       (20)      449 2023-07-07 17:36:26.000000 queryset_annotations-1.1.0/queryset_annotations/mixins/dependency_annotation.py
+drwxr-xr-x   0 gefest     (501) staff       (20)        0 2023-07-23 18:52:37.847003 queryset_annotations-1.1.0/queryset_annotations/proxy/
+-rw-r--r--   0 gefest     (501) staff       (20)       41 2023-07-07 23:02:02.000000 queryset_annotations-1.1.0/queryset_annotations/proxy/__init__.py
+-rw-r--r--   0 gefest     (501) staff       (20)      874 2023-07-23 18:48:17.000000 queryset_annotations-1.1.0/queryset_annotations/proxy/manager.py
+-rw-r--r--   0 gefest     (501) staff       (20)     2071 2023-07-23 18:48:17.000000 queryset_annotations-1.1.0/queryset_annotations/proxy/meta.py
+-rw-r--r--   0 gefest     (501) staff       (20)      295 2023-07-23 18:48:17.000000 queryset_annotations-1.1.0/queryset_annotations/proxy/model.py
+-rw-r--r--   0 gefest     (501) staff       (20)      345 2023-07-23 18:48:17.000000 queryset_annotations-1.1.0/queryset_annotations/tools.py
+drwxr-xr-x   0 gefest     (501) staff       (20)        0 2023-07-23 18:52:37.840706 queryset_annotations-1.1.0/queryset_annotations.egg-info/
+-rw-r--r--   0 gefest     (501) staff       (20)     6614 2023-07-23 18:52:37.000000 queryset_annotations-1.1.0/queryset_annotations.egg-info/PKG-INFO
+-rw-r--r--   0 gefest     (501) staff       (20)     1208 2023-07-23 18:52:37.000000 queryset_annotations-1.1.0/queryset_annotations.egg-info/SOURCES.txt
+-rw-r--r--   0 gefest     (501) staff       (20)        1 2023-07-23 18:52:37.000000 queryset_annotations-1.1.0/queryset_annotations.egg-info/dependency_links.txt
+-rw-r--r--   0 gefest     (501) staff       (20)       12 2023-07-23 18:52:37.000000 queryset_annotations-1.1.0/queryset_annotations.egg-info/requires.txt
+-rw-r--r--   0 gefest     (501) staff       (20)       40 2023-07-23 18:52:37.000000 queryset_annotations-1.1.0/queryset_annotations.egg-info/top_level.txt
+-rw-r--r--   0 gefest     (501) staff       (20)       38 2023-07-23 18:52:37.847792 queryset_annotations-1.1.0/setup.cfg
+-rw-r--r--   0 gefest     (501) staff       (20)      419 2023-07-23 18:48:18.000000 queryset_annotations-1.1.0/setup.py
```

### Comparing `queryset_annotations-1/LICENSE` & `queryset_annotations-1.1.0/LICENSE`

 * *Files identical despite different names*

### Comparing `queryset_annotations-1/README.md` & `queryset_annotations-1.1.0/annotation/views.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,79 +1,52 @@
-# django_queryset_annotations
-The queryset_annotations library provides a way to add annotations to Django querysets.
-Annotations are additional fields that are calculated on the fly and added to the queryset results.
-
-To use the queryset_annotations library, you first need to create an annotation class.
-An annotation class is a subclass of the BaseAnnotation class.
-The BaseAnnotation class provides a number of methods that you can use to define the annotation,
-such as the name, output_field, and get_expression() methods.
-
-## how to use django queryset annotations
-
-example models.py
-```python
 from django.db import models
+from rest_framework import serializers
+from rest_framework.viewsets import ModelViewSet
 
-class Book(models.Model):
-    title = models.CharField(max_length=100)
-    author = models.ForeignKey("Author", on_delete=models.CASCADE, related_name="books")
-
-
-class Author(models.Model):
-    name = models.CharField(max_length=100)
-    age = models.IntegerField()
-
-```
+from annotation.models import Author, Book
+from queryset_annotations.base import BaseAnnotation, BaseContextManager
+from queryset_annotations.drf.views import AnnotatedQuerysetMixin
+from queryset_annotations.proxy.model import BaseProxyModel
 
-Create annotation class
-```python
-from django.db import models
-from queryset_annotations.base import BaseAnnotation
 
 class BookCountAnnotation(BaseAnnotation):
     name = "book_count"
     output_field = models.IntegerField()
 
-    def get_expression(self):
+    def get_expression(self, *, context_manager: BaseContextManager = None):
         return models.Count("books", distinct=True)
 
 
-```
-
-create proxy model for Author
-```python
-from queryset_annotations.proxy.model import BaseProxyModel
-
 class AuthorProxyModel(BaseProxyModel):
     book_count = BookCountAnnotation()
 
     class Meta:
         model = Author
 
-```
-use proxy model in serializers and viewsets
-```python
-from rest_framework import serializers
-from rest_framework.viewsets import ModelViewSet
 
 class AuthorSerializer(serializers.ModelSerializer):
+    user = serializers.HiddenField(default=serializers.CurrentUserDefault())
+
     class Meta:
         model = AuthorProxyModel
         fields = "__all__"
 
 
 class BookSerializer(serializers.ModelSerializer):
     class Meta:
         model = Book
         fields = "__all__"
 
 
-class AuthorViewSet(ModelViewSet):
-    queryset = AuthorProxyModel.objects.all()
+class AuthorViewSet(AnnotatedQuerysetMixin, ModelViewSet):
+    annotation_context_class = BaseContextManager
+    annotated_model = AuthorProxyModel
     serializer_class = AuthorSerializer
 
+    def get_queryset(self):
+        context_manager = self.annotation_context_class(self.get_serializer_context())
+        return self.queryset.get_annotated_queryset(context_manager=context_manager)
+
 
 class BookViewSet(ModelViewSet):
     queryset = Book.objects.all()
     serializer_class = BookSerializer
-
-```
```

### Comparing `queryset_annotations-1/annotation/migrations/0001_initial.py` & `queryset_annotations-1.1.0/annotation/migrations/0001_initial.py`

 * *Files identical despite different names*

### Comparing `queryset_annotations-1/annotation/migrations/0002_remove_author_book_alter_book_author.py` & `queryset_annotations-1.1.0/annotation/migrations/0002_remove_author_book_alter_book_author.py`

 * *Files identical despite different names*

### Comparing `queryset_annotations-1/example/settings.py` & `queryset_annotations-1.1.0/example/settings.py`

 * *Files identical despite different names*

### Comparing `queryset_annotations-1/example/urls.py` & `queryset_annotations-1.1.0/example/urls.py`

 * *Files identical despite different names*

### Comparing `queryset_annotations-1/pyproject.toml` & `queryset_annotations-1.1.0/pyproject.toml`

 * *Files 20% similar despite different names*

```diff
@@ -1,12 +1,28 @@
+[build-system]
+requires = ["setuptools", "wheel"]
+
+[project]
+name = "queryset_annotations"
+version = "1.1.0"
+description = "Django Smart Queryset Annotations"
+readme = "README.md"
+authors = [
+    { name = "Sergei (Gefest) Romanchuk" }
+]
+license = { file = "LICENSE" }
+urls = { homepage = "https://github.com/GefMar/django_queryset_annotations" }
+classifiers = [
+    "License :: OSI Approved :: MIT License"
+]
+
 [tool.isort]
-line_length = "119"
-multi_line_output = "3"
-include_trailing_comma = "true"
-skip = "migrations"
+line_length = 119
+multi_line_output = 3
+include_trailing_comma = true
 
 [tool.black]
 line-length = 120
 target-version = ['py38']
 include = '\.pyi?$'
 
 [tool.flakeheaven]
@@ -85,13 +101,14 @@
     "-WPS347",
     "-WPS412",
 ]
 [tool.flakeheaven.exceptions."*/meta.py"]
 "*" = [
     "-WPS608",
     "-WPS613",
+    "-N804",
 ]
 
 [tool.flakeheaven.exceptions."*.md"]
 "*" = [
     "-*",
 ]
```

### Comparing `queryset_annotations-1/queryset_annotations/base/subquery_annotation.py` & `queryset_annotations-1.1.0/queryset_annotations/base/subquery_annotation.py`

 * *Files identical despite different names*

### Comparing `queryset_annotations-1/queryset_annotations/proxy/meta.py` & `queryset_annotations-1.1.0/queryset_annotations/proxy/meta.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,45 +1,64 @@
 __all__ = ("MetaProxyModel",)
 
 from copy import copy
 
 from ..base.abstract_annotation import BaseAnnotation
+from .manager import get_proxy_manager
 
 
 class MetaProxyModel(type):
-    def __new__(cls, name, bases, attrs):
+    __manager_cls = None
+    __objects = None
+    _annotations: dict[str, BaseAnnotation] = {}
+
+    def __new__(mcls, name, bases, attrs):
         if getattr(attrs["Meta"], "abstract", False):
-            return super().__new__(cls, name, bases, attrs)
-        return cls.make_proxy_model(name, bases, attrs)
+            return super().__new__(mcls, name, bases, attrs)
+        return mcls.make_proxy_model(name, bases, attrs)
 
     @classmethod
-    def make_proxy_model(cls, name, bases, attrs):
-        expressions = {}
+    def make_proxy_model(mcls, name, bases, attrs):
         annotations = {}
         meta = copy(attrs["Meta"].model._meta)  # noqa: WPS437
         meta_fields = list(meta.fields)
-        for field_name, attr in attrs.items():
-            if isinstance(attr, BaseAnnotation):
-                attr.output_field.attname = field_name
-                attr.output_field.name = field_name
-                attr.output_field.editable = False
-                attr.output_field.concrete = False
-                attr.output_field.column = None
-                meta_fields.append(attr.output_field)
-                expressions[field_name] = attr.get_expression()
-                annotations[field_name] = attr
+        filtered_attrs = filter(lambda obj: isinstance(obj[1], BaseAnnotation), attrs.items())
+        for field_name, attr in filtered_attrs:
+            output_field = mcls.__make_output_field(attr.output_field, field_name)
+            meta_fields.append(output_field)
+            annotations[field_name] = attr
         meta.fields = type(meta.fields)(meta_fields)
         meta.concrete_model._meta = meta  # noqa: WPS437
         attrs["_meta"] = meta
         attrs["_annotations"] = annotations
-        attrs["objects"] = cls.make_manager(attrs["Meta"].model.objects.__class__, expressions)()
-        attrs["_default_manager"] = attrs["objects"]
-        attrs["objects"].model = attrs["Meta"].model
 
-        return super().__new__(cls, name, bases, attrs)
+        return super().__new__(mcls, name, bases, attrs)
 
-    @classmethod
-    def make_manager(cls, original_manager, expressions):
-        def get_queryset(self):
-            return super(self.__class__, self).get_queryset().annotate(**expressions)
+    @property
+    def manager_cls(cls):
+        if cls.__manager_cls is None:
+            cls.__manager_cls = get_proxy_manager(
+                cls.Meta.model.objects.__class__,
+                cls._annotations,
+            )
+        return cls.__manager_cls
+
+    @property
+    def objects(cls):
+        if cls.__objects is None:
+            cls.__objects = cls.manager_cls()
+            cls.__objects.model = cls.Meta.model
+
+        return cls.__objects
+
+    @property
+    def _default_manager(cls):
+        return cls.objects
 
-        return type(f"Annotated{original_manager.__name__}", (original_manager,), {"get_queryset": get_queryset})
+    @classmethod
+    def __make_output_field(mcls, output_field, field_name):
+        output_field.attname = field_name
+        output_field.name = field_name
+        output_field.editable = False
+        output_field.concrete = False
+        output_field.column = None
+        return output_field
```

### Comparing `queryset_annotations-1/queryset_annotations.egg-info/SOURCES.txt` & `queryset_annotations-1.1.0/queryset_annotations.egg-info/SOURCES.txt`

 * *Files 7% similar despite different names*

```diff
@@ -13,20 +13,26 @@
 annotation/migrations/__init__.py
 example/__init__.py
 example/asgi.py
 example/settings.py
 example/urls.py
 example/wsgi.py
 queryset_annotations/__init__.py
+queryset_annotations/tools.py
 queryset_annotations.egg-info/PKG-INFO
 queryset_annotations.egg-info/SOURCES.txt
 queryset_annotations.egg-info/dependency_links.txt
 queryset_annotations.egg-info/requires.txt
 queryset_annotations.egg-info/top_level.txt
 queryset_annotations/base/__init__.py
 queryset_annotations/base/abstract_annotation.py
+queryset_annotations/base/context.py
 queryset_annotations/base/subquery_annotation.py
+queryset_annotations/drf/__init__.py
+queryset_annotations/drf/views/__init__.py
+queryset_annotations/drf/views/mixins.py
 queryset_annotations/mixins/__init__.py
 queryset_annotations/mixins/dependency_annotation.py
 queryset_annotations/proxy/__init__.py
+queryset_annotations/proxy/manager.py
 queryset_annotations/proxy/meta.py
 queryset_annotations/proxy/model.py
```

