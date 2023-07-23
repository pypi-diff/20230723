# Comparing `tmp/autoapi-django-0.9.1.tar.gz` & `tmp/autoapi-django-0.9.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "autoapi-django-0.9.1.tar", last modified: Sat Apr 29 10:09:01 2023, max compression
+gzip compressed data, was "autoapi-django-0.9.2.tar", last modified: Sat Apr 29 12:54:43 2023, max compression
```

## Comparing `autoapi-django-0.9.1.tar` & `autoapi-django-0.9.2.tar`

### file list

```diff
@@ -1,87 +1,104 @@
-drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 10:09:01.496361 autoapi-django-0.9.1/
--rw-r--r--   0 th        (1000) th        (1000)     1107 2023-04-07 21:50:01.000000 autoapi-django-0.9.1/LICENSE.txt
--rw-r--r--   0 th        (1000) th        (1000)       34 2023-04-07 21:50:01.000000 autoapi-django-0.9.1/MANIFEST.in
--rw-r--r--   0 th        (1000) th        (1000)     3043 2023-04-29 10:09:01.496361 autoapi-django-0.9.1/PKG-INFO
--rw-r--r--   0 th        (1000) th        (1000)     1280 2023-04-08 23:10:32.000000 autoapi-django-0.9.1/README.md
-drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 10:09:01.456361 autoapi-django-0.9.1/autoapi/
--rw-r--r--   0 th        (1000) th        (1000)        0 2023-04-07 21:50:01.000000 autoapi-django-0.9.1/autoapi/__init__.py
-drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 10:09:01.456361 autoapi-django-0.9.1/autoapi/api/
--rw-r--r--   0 th        (1000) th        (1000)        0 2023-04-07 21:50:01.000000 autoapi-django-0.9.1/autoapi/api/__init__.py
--rw-r--r--   0 th        (1000) th        (1000)      726 2023-04-08 23:19:52.000000 autoapi-django-0.9.1/autoapi/api/encoders.py
-drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 10:09:01.456361 autoapi-django-0.9.1/autoapi/api/http_explorer/
--rw-r--r--   0 th        (1000) th        (1000)        0 2023-04-07 21:50:01.000000 autoapi-django-0.9.1/autoapi/api/http_explorer/__init__.py
--rw-r--r--   0 th        (1000) th        (1000)      789 2023-04-08 23:34:33.000000 autoapi-django-0.9.1/autoapi/api/http_explorer/interface.py
--rw-r--r--   0 th        (1000) th        (1000)      573 2023-04-07 21:50:01.000000 autoapi-django-0.9.1/autoapi/api/http_explorer/openapi_views.py
--rw-r--r--   0 th        (1000) th        (1000)     1017 2023-04-08 23:34:32.000000 autoapi-django-0.9.1/autoapi/api/http_explorer/swagger.py
--rw-r--r--   0 th        (1000) th        (1000)      288 2023-04-07 21:50:01.000000 autoapi-django-0.9.1/autoapi/api/response.py
-drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 10:09:01.466361 autoapi-django-0.9.1/autoapi/api/routes/
--rw-r--r--   0 th        (1000) th        (1000)        0 2023-04-07 21:50:01.000000 autoapi-django-0.9.1/autoapi/api/routes/__init__.py
-drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 10:09:01.466361 autoapi-django-0.9.1/autoapi/api/routes/django/
--rw-r--r--   0 th        (1000) th        (1000)        0 2023-04-07 21:50:01.000000 autoapi-django-0.9.1/autoapi/api/routes/django/__init__.py
--rw-r--r--   0 th        (1000) th        (1000)     5354 2023-04-29 10:07:20.000000 autoapi-django-0.9.1/autoapi/api/routes/django/base.py
--rw-r--r--   0 th        (1000) th        (1000)     1541 2023-04-08 22:16:13.000000 autoapi-django-0.9.1/autoapi/api/routes/django/http.py
--rw-r--r--   0 th        (1000) th        (1000)      745 2023-04-08 22:16:13.000000 autoapi-django-0.9.1/autoapi/api/routes/interface.py
--rw-r--r--   0 th        (1000) th        (1000)      466 2023-04-08 22:16:13.000000 autoapi-django-0.9.1/autoapi/api/routes/urls.py
-drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 10:09:01.466361 autoapi-django-0.9.1/autoapi/api/schema_serializers/
--rw-r--r--   0 th        (1000) th        (1000)        0 2023-04-07 21:50:01.000000 autoapi-django-0.9.1/autoapi/api/schema_serializers/__init__.py
--rw-r--r--   0 th        (1000) th        (1000)      459 2023-04-08 22:16:13.000000 autoapi-django-0.9.1/autoapi/api/schema_serializers/interface.py
--rw-r--r--   0 th        (1000) th        (1000)     7090 2023-04-23 19:30:33.000000 autoapi-django-0.9.1/autoapi/api/schema_serializers/openapi.py
--rw-r--r--   0 th        (1000) th        (1000)     2250 2023-04-23 19:30:33.000000 autoapi-django-0.9.1/autoapi/app.py
-drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 10:09:01.466361 autoapi-django-0.9.1/autoapi/auth/
--rw-r--r--   0 th        (1000) th        (1000)        0 2023-04-07 21:50:01.000000 autoapi-django-0.9.1/autoapi/auth/__init__.py
--rw-r--r--   0 th        (1000) th        (1000)      428 2023-04-09 16:42:28.000000 autoapi-django-0.9.1/autoapi/auth/interface.py
--rw-r--r--   0 th        (1000) th        (1000)      400 2023-04-07 21:50:01.000000 autoapi-django-0.9.1/autoapi/auth/provider.py
--rw-r--r--   0 th        (1000) th        (1000)      101 2023-04-07 21:50:01.000000 autoapi-django-0.9.1/autoapi/auth/vars.py
--rw-r--r--   0 th        (1000) th        (1000)     6821 2023-04-23 19:30:33.000000 autoapi-django-0.9.1/autoapi/dependencies.py
-drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 10:09:01.466361 autoapi-django-0.9.1/autoapi/deserializers/
--rw-r--r--   0 th        (1000) th        (1000)        0 2023-04-07 21:50:01.000000 autoapi-django-0.9.1/autoapi/deserializers/__init__.py
--rw-r--r--   0 th        (1000) th        (1000)      476 2023-04-23 19:39:05.000000 autoapi-django-0.9.1/autoapi/deserializers/content_deserializer.py
--rw-r--r--   0 th        (1000) th        (1000)      956 2023-04-08 22:16:13.000000 autoapi-django-0.9.1/autoapi/deserializers/interface.py
-drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 10:09:01.476361 autoapi-django-0.9.1/autoapi/deserializers/parsers/
--rw-r--r--   0 th        (1000) th        (1000)        0 2023-04-08 22:16:13.000000 autoapi-django-0.9.1/autoapi/deserializers/parsers/__init__.py
--rw-r--r--   0 th        (1000) th        (1000)      333 2023-04-08 22:16:13.000000 autoapi-django-0.9.1/autoapi/deserializers/parsers/bool.py
--rw-r--r--   0 th        (1000) th        (1000)      372 2023-04-23 19:30:33.000000 autoapi-django-0.9.1/autoapi/deserializers/parsers/date.py
--rw-r--r--   0 th        (1000) th        (1000)      392 2023-04-23 19:30:33.000000 autoapi-django-0.9.1/autoapi/deserializers/parsers/datetime.py
--rw-r--r--   0 th        (1000) th        (1000)      660 2023-04-08 22:16:13.000000 autoapi-django-0.9.1/autoapi/deserializers/parsers/exception.py
--rw-r--r--   0 th        (1000) th        (1000)      336 2023-04-08 22:16:13.000000 autoapi-django-0.9.1/autoapi/deserializers/parsers/float.py
--rw-r--r--   0 th        (1000) th        (1000)      330 2023-04-23 19:36:47.000000 autoapi-django-0.9.1/autoapi/deserializers/parsers/int.py
--rw-r--r--   0 th        (1000) th        (1000)      706 2023-04-08 22:16:13.000000 autoapi-django-0.9.1/autoapi/deserializers/parsers/list.py
--rw-r--r--   0 th        (1000) th        (1000)      929 2023-04-23 19:40:49.000000 autoapi-django-0.9.1/autoapi/deserializers/parsers/model.py
--rw-r--r--   0 th        (1000) th        (1000)      330 2023-04-08 22:16:13.000000 autoapi-django-0.9.1/autoapi/deserializers/parsers/str.py
--rw-r--r--   0 th        (1000) th        (1000)      372 2023-04-23 19:30:33.000000 autoapi-django-0.9.1/autoapi/deserializers/parsers/time.py
-drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 10:09:01.486361 autoapi-django-0.9.1/autoapi/schema/
--rw-r--r--   0 th        (1000) th        (1000)        0 2023-04-07 21:50:01.000000 autoapi-django-0.9.1/autoapi/schema/__init__.py
--rw-r--r--   0 th        (1000) th        (1000)     1305 2023-04-08 22:16:13.000000 autoapi-django-0.9.1/autoapi/schema/annotation.py
--rw-r--r--   0 th        (1000) th        (1000)     1932 2023-04-08 22:16:13.000000 autoapi-django-0.9.1/autoapi/schema/data.py
--rw-r--r--   0 th        (1000) th        (1000)      124 2023-04-07 21:50:01.000000 autoapi-django-0.9.1/autoapi/schema/empty.py
--rw-r--r--   0 th        (1000) th        (1000)      216 2023-04-08 22:16:13.000000 autoapi-django-0.9.1/autoapi/schema/enums.py
--rw-r--r--   0 th        (1000) th        (1000)     2211 2023-04-23 19:30:33.000000 autoapi-django-0.9.1/autoapi/schema/interfaces.py
--rw-r--r--   0 th        (1000) th        (1000)     2840 2023-04-08 22:16:13.000000 autoapi-django-0.9.1/autoapi/schema/method.py
-drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 10:09:01.496361 autoapi-django-0.9.1/autoapi/schema/parsers/
--rw-r--r--   0 th        (1000) th        (1000)        0 2023-04-08 22:16:13.000000 autoapi-django-0.9.1/autoapi/schema/parsers/__init__.py
--rw-r--r--   0 th        (1000) th        (1000)     1063 2023-04-08 22:16:13.000000 autoapi-django-0.9.1/autoapi/schema/parsers/dataclass.py
--rw-r--r--   0 th        (1000) th        (1000)      483 2023-04-23 19:30:33.000000 autoapi-django-0.9.1/autoapi/schema/parsers/date.py
--rw-r--r--   0 th        (1000) th        (1000)      491 2023-04-23 19:30:33.000000 autoapi-django-0.9.1/autoapi/schema/parsers/datetime.py
--rw-r--r--   0 th        (1000) th        (1000)     1416 2023-04-23 19:30:38.000000 autoapi-django-0.9.1/autoapi/schema/parsers/django.py
--rw-r--r--   0 th        (1000) th        (1000)     1008 2023-04-22 11:43:50.000000 autoapi-django-0.9.1/autoapi/schema/parsers/exception.py
--rw-r--r--   0 th        (1000) th        (1000)      456 2023-04-08 22:16:13.000000 autoapi-django-0.9.1/autoapi/schema/parsers/file.py
--rw-r--r--   0 th        (1000) th        (1000)      486 2023-04-08 22:16:13.000000 autoapi-django-0.9.1/autoapi/schema/parsers/primitive.py
--rw-r--r--   0 th        (1000) th        (1000)      483 2023-04-23 19:30:33.000000 autoapi-django-0.9.1/autoapi/schema/parsers/time.py
--rw-r--r--   0 th        (1000) th        (1000)     1153 2023-04-08 22:16:13.000000 autoapi-django-0.9.1/autoapi/schema/service.py
--rw-r--r--   0 th        (1000) th        (1000)      375 2023-04-08 23:06:09.000000 autoapi-django-0.9.1/autoapi/schema/types.py
--rw-r--r--   0 th        (1000) th        (1000)     3867 2023-04-08 22:16:13.000000 autoapi-django-0.9.1/autoapi/schema/utils.py
--rw-r--r--   0 th        (1000) th        (1000)      327 2023-04-08 22:23:53.000000 autoapi-django-0.9.1/autoapi/settings.py
-drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 10:09:01.446361 autoapi-django-0.9.1/autoapi/templates/
-drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 10:09:01.496361 autoapi-django-0.9.1/autoapi/templates/autoapi/
--rw-r--r--   0 th        (1000) th        (1000)      666 2023-04-07 21:50:01.000000 autoapi-django-0.9.1/autoapi/templates/autoapi/swagger.html
-drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 10:09:01.496361 autoapi-django-0.9.1/autoapi_django.egg-info/
--rw-r--r--   0 th        (1000) th        (1000)     3043 2023-04-29 10:09:01.000000 autoapi-django-0.9.1/autoapi_django.egg-info/PKG-INFO
--rw-r--r--   0 th        (1000) th        (1000)     2155 2023-04-29 10:09:01.000000 autoapi-django-0.9.1/autoapi_django.egg-info/SOURCES.txt
--rw-r--r--   0 th        (1000) th        (1000)        1 2023-04-29 10:09:01.000000 autoapi-django-0.9.1/autoapi_django.egg-info/dependency_links.txt
--rw-r--r--   0 th        (1000) th        (1000)       87 2023-04-29 10:09:01.000000 autoapi-django-0.9.1/autoapi_django.egg-info/requires.txt
--rw-r--r--   0 th        (1000) th        (1000)        8 2023-04-29 10:09:01.000000 autoapi-django-0.9.1/autoapi_django.egg-info/top_level.txt
--rw-r--r--   0 th        (1000) th        (1000)      983 2023-04-29 10:08:35.000000 autoapi-django-0.9.1/pyproject.toml
--rw-r--r--   0 th        (1000) th        (1000)       38 2023-04-29 10:09:01.496361 autoapi-django-0.9.1/setup.cfg
-drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 10:09:01.496361 autoapi-django-0.9.1/tests/
--rw-r--r--   0 th        (1000) th        (1000)     2475 2023-04-22 11:43:50.000000 autoapi-django-0.9.1/tests/test_auth.py
--rw-r--r--   0 th        (1000) th        (1000)     1140 2023-04-22 11:43:50.000000 autoapi-django-0.9.1/tests/test_quickstart.py
+drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 12:54:43.596357 autoapi-django-0.9.2/
+-rw-r--r--   0 th        (1000) th        (1000)     1107 2023-04-07 21:50:01.000000 autoapi-django-0.9.2/LICENSE.txt
+-rw-r--r--   0 th        (1000) th        (1000)       34 2023-04-07 21:50:01.000000 autoapi-django-0.9.2/MANIFEST.in
+-rw-r--r--   0 th        (1000) th        (1000)     3043 2023-04-29 12:54:43.596357 autoapi-django-0.9.2/PKG-INFO
+-rw-r--r--   0 th        (1000) th        (1000)     1280 2023-04-08 23:10:32.000000 autoapi-django-0.9.2/README.md
+drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 12:54:43.546357 autoapi-django-0.9.2/autoapi/
+-rw-r--r--   0 th        (1000) th        (1000)        0 2023-04-07 21:50:01.000000 autoapi-django-0.9.2/autoapi/__init__.py
+drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 12:54:43.546357 autoapi-django-0.9.2/autoapi/api/
+-rw-r--r--   0 th        (1000) th        (1000)        0 2023-04-07 21:50:01.000000 autoapi-django-0.9.2/autoapi/api/__init__.py
+-rw-r--r--   0 th        (1000) th        (1000)      726 2023-04-08 23:19:52.000000 autoapi-django-0.9.2/autoapi/api/encoders.py
+drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 12:54:43.556357 autoapi-django-0.9.2/autoapi/api/http_explorer/
+-rw-r--r--   0 th        (1000) th        (1000)        0 2023-04-07 21:50:01.000000 autoapi-django-0.9.2/autoapi/api/http_explorer/__init__.py
+-rw-r--r--   0 th        (1000) th        (1000)      773 2023-04-29 10:35:31.000000 autoapi-django-0.9.2/autoapi/api/http_explorer/interface.py
+-rw-r--r--   0 th        (1000) th        (1000)      573 2023-04-07 21:50:01.000000 autoapi-django-0.9.2/autoapi/api/http_explorer/openapi_views.py
+-rw-r--r--   0 th        (1000) th        (1000)     1017 2023-04-08 23:34:32.000000 autoapi-django-0.9.2/autoapi/api/http_explorer/swagger.py
+-rw-r--r--   0 th        (1000) th        (1000)      288 2023-04-07 21:50:01.000000 autoapi-django-0.9.2/autoapi/api/response.py
+drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 12:54:43.556357 autoapi-django-0.9.2/autoapi/api/routes/
+-rw-r--r--   0 th        (1000) th        (1000)        0 2023-04-07 21:50:01.000000 autoapi-django-0.9.2/autoapi/api/routes/__init__.py
+drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 12:54:43.556357 autoapi-django-0.9.2/autoapi/api/routes/django/
+-rw-r--r--   0 th        (1000) th        (1000)        0 2023-04-07 21:50:01.000000 autoapi-django-0.9.2/autoapi/api/routes/django/__init__.py
+-rw-r--r--   0 th        (1000) th        (1000)     5425 2023-04-29 10:35:31.000000 autoapi-django-0.9.2/autoapi/api/routes/django/base.py
+-rw-r--r--   0 th        (1000) th        (1000)     1541 2023-04-08 22:16:13.000000 autoapi-django-0.9.2/autoapi/api/routes/django/http.py
+-rw-r--r--   0 th        (1000) th        (1000)      725 2023-04-29 10:35:31.000000 autoapi-django-0.9.2/autoapi/api/routes/interface.py
+-rw-r--r--   0 th        (1000) th        (1000)      466 2023-04-08 22:16:13.000000 autoapi-django-0.9.2/autoapi/api/routes/urls.py
+drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 12:54:43.556357 autoapi-django-0.9.2/autoapi/api/schema_presenter/
+-rw-r--r--   0 th        (1000) th        (1000)        0 2023-04-29 10:35:31.000000 autoapi-django-0.9.2/autoapi/api/schema_presenter/__init__.py
+-rw-r--r--   0 th        (1000) th        (1000)      586 2023-04-29 10:35:31.000000 autoapi-django-0.9.2/autoapi/api/schema_presenter/interface.py
+drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 12:54:43.556357 autoapi-django-0.9.2/autoapi/api/schema_presenter/openapi/
+-rw-r--r--   0 th        (1000) th        (1000)        0 2023-04-29 10:35:31.000000 autoapi-django-0.9.2/autoapi/api/schema_presenter/openapi/__init__.py
+-rw-r--r--   0 th        (1000) th        (1000)     6506 2023-04-29 10:35:31.000000 autoapi-django-0.9.2/autoapi/api/schema_presenter/openapi/presenter.py
+drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 12:54:43.566357 autoapi-django-0.9.2/autoapi/api/schema_presenter/openapi/properties/
+-rw-r--r--   0 th        (1000) th        (1000)        0 2023-04-29 10:35:31.000000 autoapi-django-0.9.2/autoapi/api/schema_presenter/openapi/properties/__init__.py
+-rw-r--r--   0 th        (1000) th        (1000)      292 2023-04-29 10:35:31.000000 autoapi-django-0.9.2/autoapi/api/schema_presenter/openapi/properties/any.py
+-rw-r--r--   0 th        (1000) th        (1000)      337 2023-04-29 10:35:31.000000 autoapi-django-0.9.2/autoapi/api/schema_presenter/openapi/properties/boolean.py
+-rw-r--r--   0 th        (1000) th        (1000)      389 2023-04-29 10:35:31.000000 autoapi-django-0.9.2/autoapi/api/schema_presenter/openapi/properties/date.py
+-rw-r--r--   0 th        (1000) th        (1000)      401 2023-04-29 10:35:31.000000 autoapi-django-0.9.2/autoapi/api/schema_presenter/openapi/properties/datetime.py
+-rw-r--r--   0 th        (1000) th        (1000)      362 2023-04-29 12:41:55.000000 autoapi-django-0.9.2/autoapi/api/schema_presenter/openapi/properties/empty.py
+-rw-r--r--   0 th        (1000) th        (1000)      330 2023-04-29 10:35:31.000000 autoapi-django-0.9.2/autoapi/api/schema_presenter/openapi/properties/file_.py
+-rw-r--r--   0 th        (1000) th        (1000)      334 2023-04-29 10:35:31.000000 autoapi-django-0.9.2/autoapi/api/schema_presenter/openapi/properties/float.py
+-rw-r--r--   0 th        (1000) th        (1000)      330 2023-04-29 10:35:31.000000 autoapi-django-0.9.2/autoapi/api/schema_presenter/openapi/properties/integer.py
+-rw-r--r--   0 th        (1000) th        (1000)      249 2023-04-29 10:35:31.000000 autoapi-django-0.9.2/autoapi/api/schema_presenter/openapi/properties/interface.py
+-rw-r--r--   0 th        (1000) th        (1000)      360 2023-04-29 10:35:31.000000 autoapi-django-0.9.2/autoapi/api/schema_presenter/openapi/properties/model.py
+-rw-r--r--   0 th        (1000) th        (1000)      330 2023-04-29 10:35:31.000000 autoapi-django-0.9.2/autoapi/api/schema_presenter/openapi/properties/string.py
+-rw-r--r--   0 th        (1000) th        (1000)      388 2023-04-29 10:35:32.000000 autoapi-django-0.9.2/autoapi/api/schema_presenter/openapi/properties/time.py
+-rw-r--r--   0 th        (1000) th        (1000)     2250 2023-04-23 19:30:33.000000 autoapi-django-0.9.2/autoapi/app.py
+drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 12:54:43.566357 autoapi-django-0.9.2/autoapi/auth/
+-rw-r--r--   0 th        (1000) th        (1000)        0 2023-04-07 21:50:01.000000 autoapi-django-0.9.2/autoapi/auth/__init__.py
+-rw-r--r--   0 th        (1000) th        (1000)      428 2023-04-09 16:42:28.000000 autoapi-django-0.9.2/autoapi/auth/interface.py
+-rw-r--r--   0 th        (1000) th        (1000)      400 2023-04-07 21:50:01.000000 autoapi-django-0.9.2/autoapi/auth/provider.py
+-rw-r--r--   0 th        (1000) th        (1000)      101 2023-04-07 21:50:01.000000 autoapi-django-0.9.2/autoapi/auth/vars.py
+-rw-r--r--   0 th        (1000) th        (1000)     8253 2023-04-29 12:41:55.000000 autoapi-django-0.9.2/autoapi/dependencies.py
+drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 12:54:43.576357 autoapi-django-0.9.2/autoapi/schema/
+-rw-r--r--   0 th        (1000) th        (1000)        0 2023-04-07 21:50:01.000000 autoapi-django-0.9.2/autoapi/schema/__init__.py
+-rw-r--r--   0 th        (1000) th        (1000)     1305 2023-04-29 12:40:13.000000 autoapi-django-0.9.2/autoapi/schema/annotation.py
+-rw-r--r--   0 th        (1000) th        (1000)     1932 2023-04-08 22:16:13.000000 autoapi-django-0.9.2/autoapi/schema/data.py
+-rw-r--r--   0 th        (1000) th        (1000)      124 2023-04-07 21:50:01.000000 autoapi-django-0.9.2/autoapi/schema/empty.py
+-rw-r--r--   0 th        (1000) th        (1000)      216 2023-04-08 22:16:13.000000 autoapi-django-0.9.2/autoapi/schema/enums.py
+-rw-r--r--   0 th        (1000) th        (1000)     2211 2023-04-29 12:40:13.000000 autoapi-django-0.9.2/autoapi/schema/interfaces.py
+-rw-r--r--   0 th        (1000) th        (1000)     2840 2023-04-29 12:40:13.000000 autoapi-django-0.9.2/autoapi/schema/method.py
+drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 12:54:43.586357 autoapi-django-0.9.2/autoapi/schema/parsers/
+-rw-r--r--   0 th        (1000) th        (1000)        0 2023-04-08 22:16:13.000000 autoapi-django-0.9.2/autoapi/schema/parsers/__init__.py
+-rw-r--r--   0 th        (1000) th        (1000)     1063 2023-04-29 12:40:13.000000 autoapi-django-0.9.2/autoapi/schema/parsers/dataclass.py
+-rw-r--r--   0 th        (1000) th        (1000)      483 2023-04-29 12:40:13.000000 autoapi-django-0.9.2/autoapi/schema/parsers/date.py
+-rw-r--r--   0 th        (1000) th        (1000)      491 2023-04-29 12:40:13.000000 autoapi-django-0.9.2/autoapi/schema/parsers/datetime.py
+-rw-r--r--   0 th        (1000) th        (1000)     1620 2023-04-29 12:40:13.000000 autoapi-django-0.9.2/autoapi/schema/parsers/django.py
+-rw-r--r--   0 th        (1000) th        (1000)     1008 2023-04-29 12:40:13.000000 autoapi-django-0.9.2/autoapi/schema/parsers/exception.py
+-rw-r--r--   0 th        (1000) th        (1000)      456 2023-04-29 12:40:13.000000 autoapi-django-0.9.2/autoapi/schema/parsers/file.py
+-rw-r--r--   0 th        (1000) th        (1000)      486 2023-04-29 12:40:13.000000 autoapi-django-0.9.2/autoapi/schema/parsers/primitive.py
+-rw-r--r--   0 th        (1000) th        (1000)      483 2023-04-29 12:40:13.000000 autoapi-django-0.9.2/autoapi/schema/parsers/time.py
+-rw-r--r--   0 th        (1000) th        (1000)     1153 2023-04-08 22:16:13.000000 autoapi-django-0.9.2/autoapi/schema/service.py
+-rw-r--r--   0 th        (1000) th        (1000)      375 2023-04-29 12:40:13.000000 autoapi-django-0.9.2/autoapi/schema/types.py
+-rw-r--r--   0 th        (1000) th        (1000)     3867 2023-04-08 22:16:13.000000 autoapi-django-0.9.2/autoapi/schema/utils.py
+drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 12:54:43.586357 autoapi-django-0.9.2/autoapi/serializers/
+-rw-r--r--   0 th        (1000) th        (1000)        0 2023-04-29 10:35:32.000000 autoapi-django-0.9.2/autoapi/serializers/__init__.py
+-rw-r--r--   0 th        (1000) th        (1000)     1257 2023-04-29 10:35:32.000000 autoapi-django-0.9.2/autoapi/serializers/interface.py
+-rw-r--r--   0 th        (1000) th        (1000)      746 2023-04-29 10:35:32.000000 autoapi-django-0.9.2/autoapi/serializers/serializer.py
+drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 12:54:43.586357 autoapi-django-0.9.2/autoapi/serializers/types/
+-rw-r--r--   0 th        (1000) th        (1000)        0 2023-04-29 10:35:32.000000 autoapi-django-0.9.2/autoapi/serializers/types/__init__.py
+-rw-r--r--   0 th        (1000) th        (1000)      681 2023-04-29 10:35:32.000000 autoapi-django-0.9.2/autoapi/serializers/types/bool.py
+-rw-r--r--   0 th        (1000) th        (1000)      621 2023-04-29 10:35:32.000000 autoapi-django-0.9.2/autoapi/serializers/types/date.py
+-rw-r--r--   0 th        (1000) th        (1000)      653 2023-04-29 10:35:32.000000 autoapi-django-0.9.2/autoapi/serializers/types/datetime.py
+-rw-r--r--   0 th        (1000) th        (1000)      772 2023-04-29 10:35:32.000000 autoapi-django-0.9.2/autoapi/serializers/types/exception.py
+-rw-r--r--   0 th        (1000) th        (1000)      456 2023-04-29 10:35:32.000000 autoapi-django-0.9.2/autoapi/serializers/types/file.py
+-rw-r--r--   0 th        (1000) th        (1000)      567 2023-04-29 12:52:09.000000 autoapi-django-0.9.2/autoapi/serializers/types/float.py
+-rw-r--r--   0 th        (1000) th        (1000)      547 2023-04-29 10:35:32.000000 autoapi-django-0.9.2/autoapi/serializers/types/int.py
+-rw-r--r--   0 th        (1000) th        (1000)      912 2023-04-29 10:35:32.000000 autoapi-django-0.9.2/autoapi/serializers/types/list.py
+-rw-r--r--   0 th        (1000) th        (1000)     1620 2023-04-29 12:53:03.000000 autoapi-django-0.9.2/autoapi/serializers/types/model.py
+-rw-r--r--   0 th        (1000) th        (1000)      546 2023-04-29 10:35:32.000000 autoapi-django-0.9.2/autoapi/serializers/types/str.py
+-rw-r--r--   0 th        (1000) th        (1000)      625 2023-04-29 10:35:32.000000 autoapi-django-0.9.2/autoapi/serializers/types/time.py
+-rw-r--r--   0 th        (1000) th        (1000)      327 2023-04-08 22:23:53.000000 autoapi-django-0.9.2/autoapi/settings.py
+drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 12:54:43.546357 autoapi-django-0.9.2/autoapi/templates/
+drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 12:54:43.586357 autoapi-django-0.9.2/autoapi/templates/autoapi/
+-rw-r--r--   0 th        (1000) th        (1000)      666 2023-04-07 21:50:01.000000 autoapi-django-0.9.2/autoapi/templates/autoapi/swagger.html
+drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 12:54:43.596357 autoapi-django-0.9.2/autoapi_django.egg-info/
+-rw-r--r--   0 th        (1000) th        (1000)     3043 2023-04-29 12:54:43.000000 autoapi-django-0.9.2/autoapi_django.egg-info/PKG-INFO
+-rw-r--r--   0 th        (1000) th        (1000)     2934 2023-04-29 12:54:43.000000 autoapi-django-0.9.2/autoapi_django.egg-info/SOURCES.txt
+-rw-r--r--   0 th        (1000) th        (1000)        1 2023-04-29 12:54:43.000000 autoapi-django-0.9.2/autoapi_django.egg-info/dependency_links.txt
+-rw-r--r--   0 th        (1000) th        (1000)       87 2023-04-29 12:54:43.000000 autoapi-django-0.9.2/autoapi_django.egg-info/requires.txt
+-rw-r--r--   0 th        (1000) th        (1000)        8 2023-04-29 12:54:43.000000 autoapi-django-0.9.2/autoapi_django.egg-info/top_level.txt
+-rw-r--r--   0 th        (1000) th        (1000)     1101 2023-04-29 12:54:19.000000 autoapi-django-0.9.2/pyproject.toml
+-rw-r--r--   0 th        (1000) th        (1000)       38 2023-04-29 12:54:43.596357 autoapi-django-0.9.2/setup.cfg
+drwxr-xr-x   0 th        (1000) th        (1000)        0 2023-04-29 12:54:43.596357 autoapi-django-0.9.2/tests/
+-rw-r--r--   0 th        (1000) th        (1000)     2475 2023-04-22 11:43:50.000000 autoapi-django-0.9.2/tests/test_auth.py
+-rw-r--r--   0 th        (1000) th        (1000)     1140 2023-04-22 11:43:50.000000 autoapi-django-0.9.2/tests/test_quickstart.py
```

### Comparing `autoapi-django-0.9.1/LICENSE.txt` & `autoapi-django-0.9.2/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `autoapi-django-0.9.1/PKG-INFO` & `autoapi-django-0.9.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: autoapi-django
-Version: 0.9.1
+Version: 0.9.2
 Summary: Library for generating transport logic for web application
 Author-email: Artem Romanukov <vens148@gmail.com>
 License: The MIT License (MIT)
         
         Copyright (c) 2018 Sebastián Ramírez
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
```

### Comparing `autoapi-django-0.9.1/README.md` & `autoapi-django-0.9.2/README.md`

 * *Files identical despite different names*

### Comparing `autoapi-django-0.9.1/autoapi/api/encoders.py` & `autoapi-django-0.9.2/autoapi/api/encoders.py`

 * *Files identical despite different names*

### Comparing `autoapi-django-0.9.1/autoapi/api/http_explorer/interface.py` & `autoapi-django-0.9.2/autoapi/api/http_explorer/interface.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,18 +1,18 @@
 from abc import ABC, abstractmethod
 
 from django.urls.resolvers import RoutePattern
 
-from autoapi.api.schema_serializers.interface import IAppStructureSerializer
+from autoapi.api.schema_presenter.interface import ISchemaPresenter
 from autoapi.schema.data import Type, ServiceSchema
 from autoapi.settings import AutoAPISettings
 
 
 class IExplorerGenerator(ABC):
-    app_structure_serializer: IAppStructureSerializer
+    app_structure_serializer: ISchemaPresenter
     settings: AutoAPISettings
 
     @abstractmethod
     def endpoints(self, schemas: list[ServiceSchema], models: dict[str, Type]) -> list[RoutePattern]:
         """
         Генерирует массив RoutePattern'ов для HTTP API explorer'a
         Обычно там 2 ендпоинта: под схему (e.g. openapi.json)
```

### Comparing `autoapi-django-0.9.1/autoapi/api/http_explorer/openapi_views.py` & `autoapi-django-0.9.2/autoapi/api/http_explorer/openapi_views.py`

 * *Files identical despite different names*

### Comparing `autoapi-django-0.9.1/autoapi/api/http_explorer/swagger.py` & `autoapi-django-0.9.2/autoapi/api/http_explorer/swagger.py`

 * *Files identical despite different names*

### Comparing `autoapi-django-0.9.1/autoapi/api/routes/django/base.py` & `autoapi-django-0.9.2/autoapi/api/routes/django/base.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 import asyncio
 import json
 import logging
 import traceback
+from dataclasses import asdict
 
 from typing import Any
 from uuid import uuid4
 from pathlib import Path
 
 import magic
 from django.contrib.auth import login, logout
@@ -14,25 +15,25 @@
 from django.http import HttpRequest, HttpResponse, StreamingHttpResponse, FileResponse, JsonResponse
 from django.utils.decorators import method_decorator
 from django.views import View
 from django.views.decorators.csrf import csrf_exempt
 
 from autoapi.api.response import Response
 from autoapi.auth.provider import IAuthProvider
-from autoapi.deserializers.interface import IContentDeserializer
+from autoapi.serializers.interface import ISerializer
 from autoapi.api.encoders import JsonEncoder
 from autoapi.schema.data import MethodSchema
 
 
 @method_decorator(csrf_exempt, name='dispatch')
 class BaseExecuteMethodDjangoView(View):
     service: type
     schema: MethodSchema
     auth: IAuthProvider
-    deserializer: IContentDeserializer
+    deserializer: ISerializer
     use_aio: bool
 
     def dispatch(self, request: HttpRequest, *args, **kwargs):
         try:
             self.auth.authorize(request)
             if request.method == 'GET':
                 kwargs = self._GET(request)
@@ -50,18 +51,20 @@
                     logout(request)
             return self._make_http_response(result)
         except BaseException as exc:
             result = self._wrap_panic(exc)
             logging.warning(traceback.format_exc(), f'Exception ID: {result.panic["id"]}')
             return self._make_http_response(result)
 
-    def execute_method(self, **kwargs) -> Response:
+    def execute_method(self, **kwargs) -> Response | File:
         try:
             result = self.schema.func(self.service, **kwargs)
             result = self._handle_async(result)
+            if isinstance(result, File):
+                return result
             return self._wrap_result(result)
         except BaseException as exc:
             result = self._wrap_error(exc)
             logging.error(traceback.format_exc() + f'Exception ID: {result.error["id"]}')
             return result
 
     def _handle_async(self, result: any) -> any:
@@ -126,16 +129,16 @@
             fields[attr] = getattr(exc, attr)
         if not hasattr(exc, 'traceback'):
             fields['traceback'] = traceback.format_exc().split('\n')
         if not hasattr(exc, 'id'):
             fields['id'] = str(uuid4())
         return fields
 
-    def _make_http_response(self, result: Response) -> HttpResponse | StreamingHttpResponse:
-        if self.schema.returns.type.name == 'File' and result.ok:
-            if not isinstance(result.result, File):
-                raise ValueError(f'Result {result} is not a file')
-            filename = Path(result.result.name).name
+    def _make_http_response(self, response: Response | File) -> HttpResponse | StreamingHttpResponse:
+        if isinstance(response, File):
+            filename = Path(response.name).name
             _magic = magic.Magic(mime=True)
-            content_type = _magic.from_file(result.result.name)
-            return FileResponse(result.result, filename=filename, content_type=content_type)
-        return JsonResponse(result, encoder=JsonEncoder, safe=False)
+            content_type = _magic.from_file(response.name)
+            return FileResponse(response, filename=filename, content_type=content_type)
+        response.result = self.deserializer.serialize(response.result, self.schema.returns)
+        serialized_response = asdict(response)
+        return JsonResponse(serialized_response, safe=False)
```

### Comparing `autoapi-django-0.9.1/autoapi/api/routes/django/http.py` & `autoapi-django-0.9.2/autoapi/api/routes/django/http.py`

 * *Files identical despite different names*

### Comparing `autoapi-django-0.9.1/autoapi/api/routes/interface.py` & `autoapi-django-0.9.2/autoapi/api/routes/interface.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,21 +1,21 @@
 from abc import ABC, abstractmethod
 
 from django.urls.resolvers import RoutePattern
 
 from autoapi.api.routes.urls import IURLBuilder
 from autoapi.auth.provider import IAuthProvider
-from autoapi.deserializers.interface import IContentDeserializer
+from autoapi.serializers.interface import ISerializer
 from autoapi.schema.data import ServiceSchema
 from autoapi.settings import AutoAPISettings
 
 
 class IEndpointsGenerator(ABC):
     auth_provider: IAuthProvider
-    content_deserializer: IContentDeserializer
+    content_deserializer: ISerializer
     url_builder: IURLBuilder
     settings: AutoAPISettings
 
     @abstractmethod
     def generate_api(self, services: list[ServiceSchema]) -> list[RoutePattern]:
         """
         Генерирует эндпоинды для методов сервисов
```

### Comparing `autoapi-django-0.9.1/autoapi/app.py` & `autoapi-django-0.9.2/autoapi/app.py`

 * *Files identical despite different names*

### Comparing `autoapi-django-0.9.1/autoapi/dependencies.py` & `autoapi-django-0.9.2/autoapi/dependencies.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,34 +1,47 @@
 import inspect
 from contextvars import ContextVar
 from dataclasses import dataclass, field
 
 from django.utils.module_loading import import_string
 
 from autoapi.api.http_explorer.interface import IExplorerGenerator
+from autoapi.api.schema_presenter.openapi.properties.any import AnyProperty
+from autoapi.api.schema_presenter.openapi.properties.boolean import BoolTimeProperty
+from autoapi.api.schema_presenter.openapi.properties.datetime import DateTimeProperty
+from autoapi.api.schema_presenter.openapi.properties.empty import EmptyProperty
+from autoapi.api.schema_presenter.openapi.properties.file_ import FileProperty
+from autoapi.api.schema_presenter.openapi.properties.float import FloatProperty
+from autoapi.api.schema_presenter.openapi.properties.integer import IntProperty
+from autoapi.api.schema_presenter.openapi.properties.interface import IComponentProperty
+from autoapi.api.schema_presenter.openapi.properties.date import DateProperty
+from autoapi.api.schema_presenter.openapi.properties.model import DjangoModelProperty
+from autoapi.api.schema_presenter.openapi.properties.string import StrProperty
+from autoapi.api.schema_presenter.openapi.properties.time import TimeProperty
 from autoapi.api.http_explorer.swagger import Swagger
 from autoapi.api.routes.django.http import HTTPEndpointsGenerator
 from autoapi.api.routes.interface import IEndpointsGenerator
 from autoapi.api.routes.urls import IURLBuilder, DefaultURLBuilder
-from autoapi.api.schema_serializers.interface import IAppStructureSerializer
-from autoapi.api.schema_serializers.openapi import OpenAPISerializer
+from autoapi.api.schema_presenter.interface import ISchemaPresenter
+from autoapi.api.schema_presenter.openapi.presenter import OpenAPIPresenter
 from autoapi.auth.interface import IAuthProvider
 from autoapi.auth.provider import DjangoRequestAuthProvider
 from autoapi.auth.vars import authorized_user
-from autoapi.deserializers.content_deserializer import ContentDeserializer
-from autoapi.deserializers.interface import IContentDeserializer, IContentParser
-from autoapi.deserializers.parsers.bool import BoolParser
-from autoapi.deserializers.parsers.float import FloatParser
-from autoapi.deserializers.parsers.int import IntParser
-from autoapi.deserializers.parsers.list import ListParser
-from autoapi.deserializers.parsers.model import ModelParser
-from autoapi.deserializers.parsers.str import StrParser
-from autoapi.deserializers.parsers.datetime import DateTimeParser as DDateTimeParser
-from autoapi.deserializers.parsers.date import DateParser as DDateParser
-from autoapi.deserializers.parsers.time import TimeParser as DTimeParser
+from autoapi.serializers.serializer import Serializer
+from autoapi.serializers.interface import ISerializer, ITypeSerializer
+from autoapi.serializers.types.bool import BoolSerializer
+from autoapi.serializers.types.file import FileSerializer
+from autoapi.serializers.types.float import FloatSerializer
+from autoapi.serializers.types.int import IntSerializer
+from autoapi.serializers.types.list import ListSerializer
+from autoapi.serializers.types.model import ModelSerializer
+from autoapi.serializers.types.str import StrSerializer
+from autoapi.serializers.types.datetime import DateTimeSerializer as DDateTimeParser
+from autoapi.serializers.types.date import DateSerializer as DDateParser
+from autoapi.serializers.types.time import TimeSerializer as DTimeParser
 from autoapi.schema.annotation import AnnotationBuilder
 from autoapi.schema.interfaces import ITypeBuilder, IServiceBuilder, IMethodBuilder, ITypeParser, IAnnotationBuilder
 from autoapi.schema.method import MethodBuilder
 from autoapi.schema.parsers.dataclass import DataclassParser
 from autoapi.schema.parsers.django import DjangoModelParser
 from autoapi.schema.parsers.date import DateParser
 from autoapi.schema.parsers.time import TimeParser
@@ -56,31 +69,45 @@
         TimeParser(),
     ])
     type_parsers_extra: list[ITypeParser] = field(default_factory=list)
     type_builder: ITypeBuilder = TypeBuilder()
     annotation_builder: IAnnotationBuilder = AnnotationBuilder()
     endpoints_generator: str | IEndpointsGenerator = HTTPEndpointsGenerator()
     explorer_views_generator: str | IExplorerGenerator = Swagger()
-    app_structure_serializer: str | IAppStructureSerializer = OpenAPISerializer()
+    app_structure_serializer: str | ISchemaPresenter = OpenAPIPresenter()
     url_builder: str | IURLBuilder = DefaultURLBuilder()
     auth_provider: str | IAuthProvider = DjangoRequestAuthProvider()
     user_context_var: str | ContextVar = authorized_user
-    content_deserializer: str | IContentDeserializer = ContentDeserializer()
-    content_parsers: list[str | IContentParser] = field(default_factory=lambda: [
-        BoolParser(),
+    content_deserializer: str | ISerializer = Serializer()
+    content_parsers: list[str | ITypeSerializer] = field(default_factory=lambda: [
+        BoolSerializer(),
         ExceptionParser(),
-        FloatParser(),
-        IntParser(),
-        ListParser(),
-        ModelParser(),
-        StrParser(),
+        FloatSerializer(),
+        FileSerializer(),
+        IntSerializer(),
+        ListSerializer(),
+        ModelSerializer(),
+        StrSerializer(),
         DDateTimeParser(),
         DDateParser(),
         DTimeParser(),
     ])
+    components_properties_parsers: list[IComponentProperty] = field(default_factory=lambda: {
+        DateProperty(),
+        IntProperty(),
+        StrProperty(),
+        DateTimeProperty(),
+        BoolTimeProperty(),
+        FloatProperty(),
+        FileProperty(),
+        TimeProperty(),
+        AnyProperty(),
+        DjangoModelProperty(),
+        EmptyProperty(),
+    })
 
     _settings: AutoAPISettings = None
 
 
     def resolve(self, settings: AutoAPISettings):
         self._settings = settings
```

### Comparing `autoapi-django-0.9.1/autoapi/deserializers/parsers/exception.py` & `autoapi-django-0.9.2/autoapi/serializers/types/exception.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,19 +1,22 @@
-import json
-
-from autoapi.deserializers.interface import IContentParser
-from autoapi.schema.data import Annotation
-
-
-class ExceptionParser(IContentParser):
-    def check(self, annotation: Annotation):
-        t = annotation.type.type
-        return isinstance(t, type) and issubclass(t, BaseException)
-
-    def parse(self, content: any, annotation: Annotation) -> any:
-        if type(content) is str:
-            content = json.loads(content)
-        instance = annotation.type.type()
-        if isinstance(content, dict):
-            for key, value in content.items():
-                setattr(instance, key, value)
-        return instance
+import json
+
+from autoapi.serializers.interface import ITypeSerializer
+from autoapi.schema.data import Annotation
+
+
+class ExceptionSerializer(ITypeSerializer):
+    def check(self, annotation: Annotation):
+        t = annotation.type.type
+        return isinstance(t, type) and issubclass(t, BaseException)
+
+    # def serialize(self, content: any, annotation: Annotation) -> any:
+    #     if not isinstance(content, Exception)
+
+    def deserialize(self, content: any, annotation: Annotation) -> any:
+        if type(content) is str:
+            content = json.loads(content)
+        instance = annotation.type.type()
+        if isinstance(content, dict):
+            for key, value in content.items():
+                setattr(instance, key, value)
+        return instance
```

### Comparing `autoapi-django-0.9.1/autoapi/deserializers/parsers/list.py` & `autoapi-django-0.9.2/autoapi/serializers/types/list.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,20 +1,25 @@
-import json
-from typing import List
-
-from autoapi.deserializers.interface import IContentParser
-from autoapi.schema.data import Annotation
-
-
-class ListParser(IContentParser):
-    def check(self, annotation: Annotation):
-        return annotation.type.type in (list, List)
-
-    def parse(self, content: any, annotation: Annotation) -> any:
-        if isinstance(content, str):
-            content: list[any] = json.loads(content)
-        if not isinstance(content, list):
-            raise ValueError(f'Content {content} is not a list')
-        return [
-            self.content_deserializer.deserialize(data, annotation.generic_annotations[0])
-            for data in content
-        ]
+import json
+from typing import List
+
+from autoapi.serializers.interface import ITypeSerializer
+from autoapi.schema.data import Annotation
+
+
+class ListSerializer(ITypeSerializer):
+    def check(self, annotation: Annotation):
+        return annotation.type.type in (list, List)
+
+    def serialize(self, content: any, annotation: Annotation) -> list:
+        if not isinstance(content, list):
+            raise ValueError(f'Cannot serialize content = {content} as list!')
+        return content
+
+    def deserialize(self, content: any, annotation: Annotation) -> any:
+        if isinstance(content, str):
+            content: list[any] = json.loads(content)
+        if not isinstance(content, list):
+            raise ValueError(f'Content {content} is not a list')
+        return [
+            self.content_deserializer.deserialize(data, annotation.generic_annotations[0])
+            for data in content
+        ]
```

### Comparing `autoapi-django-0.9.1/autoapi/schema/annotation.py` & `autoapi-django-0.9.2/autoapi/schema/annotation.py`

 * *Files identical despite different names*

### Comparing `autoapi-django-0.9.1/autoapi/schema/data.py` & `autoapi-django-0.9.2/autoapi/schema/data.py`

 * *Files identical despite different names*

### Comparing `autoapi-django-0.9.1/autoapi/schema/interfaces.py` & `autoapi-django-0.9.2/autoapi/schema/interfaces.py`

 * *Files identical despite different names*

### Comparing `autoapi-django-0.9.1/autoapi/schema/method.py` & `autoapi-django-0.9.2/autoapi/schema/method.py`

 * *Files identical despite different names*

### Comparing `autoapi-django-0.9.1/autoapi/schema/parsers/dataclass.py` & `autoapi-django-0.9.2/autoapi/schema/parsers/dataclass.py`

 * *Files identical despite different names*

### Comparing `autoapi-django-0.9.1/autoapi/schema/parsers/django.py` & `autoapi-django-0.9.2/autoapi/schema/parsers/django.py`

 * *Files 18% similar despite different names*

```diff
@@ -29,16 +29,20 @@
         return isinstance(t, type) and issubclass(t, Model)
 
     def parse(self, t: typing.Type[Model]) -> tuple[Type, dict[str, Type]]:
         props = {}
         models = {}
         for field in t._meta.fields:
             field: Field
-            field_type = self.FIELDS_TYPES_MAPPING[type(field).__name__]
-            field_annotation, models_ = self.annotation_builder.build(field_type)
+            field_name = type(field).__name__
+            if field_name == 'ForeignKey':
+                field_annotation, models_ = self.annotation_builder.build(field.related_model)
+            else:
+                field_type = self.FIELDS_TYPES_MAPPING[field_name]
+                field_annotation, models_ = self.annotation_builder.build(field_type)
             props[field.name] = field_annotation
             models.update(models_)
         return Type(
             name=t.__name__,
             type=t,
             is_model=True,
             model_fields=props,
```

### Comparing `autoapi-django-0.9.1/autoapi/schema/parsers/exception.py` & `autoapi-django-0.9.2/autoapi/schema/parsers/exception.py`

 * *Files identical despite different names*

### Comparing `autoapi-django-0.9.1/autoapi/schema/service.py` & `autoapi-django-0.9.2/autoapi/schema/service.py`

 * *Files identical despite different names*

### Comparing `autoapi-django-0.9.1/autoapi/schema/utils.py` & `autoapi-django-0.9.2/autoapi/schema/utils.py`

 * *Files identical despite different names*

### Comparing `autoapi-django-0.9.1/autoapi/templates/autoapi/swagger.html` & `autoapi-django-0.9.2/autoapi/templates/autoapi/swagger.html`

 * *Files identical despite different names*

### Comparing `autoapi-django-0.9.1/autoapi_django.egg-info/PKG-INFO` & `autoapi-django-0.9.2/autoapi_django.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: autoapi-django
-Version: 0.9.1
+Version: 0.9.2
 Summary: Library for generating transport logic for web application
 Author-email: Artem Romanukov <vens148@gmail.com>
 License: The MIT License (MIT)
         
         Copyright (c) 2018 Sebastián Ramírez
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
```

### Comparing `autoapi-django-0.9.1/pyproject.toml` & `autoapi-django-0.9.2/pyproject.toml`

 * *Files 19% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [project]
 name = "autoapi-django"
-version = "0.9.1"
+version = "0.9.2"
 description = "Library for generating transport logic for web application"
 authors = [
     {name = "Artem Romanukov", email="vens148@gmail.com"},
 ]
 license = {file = "LICENSE.txt"}
 readme = "README.md"
 requires-python = ">=3.9"
@@ -26,14 +26,18 @@
 homepage = "https://github.com/romanukov/autoapi/"
 documentation = "https://github.com/romanukov/autoapi/"
 repository = "https://github.com/romanukov/autoapi/"
 
 [build-system]
 requires = [
     "setuptools >= 35.0.2",
+    "Django>=4.1,<5",
+    "django-cors-headers>=3.14,<3.15",
+    "requests>=2.28,<2.29",
+    "Pillow>=9.5.0,<9.6"
 ]
 
 [tool.setuptools]
 include-package-data = true
 
 [tool.setuptools.package-data]
 autoapi = ["*.html"]
```

### Comparing `autoapi-django-0.9.1/tests/test_auth.py` & `autoapi-django-0.9.2/tests/test_auth.py`

 * *Files identical despite different names*

### Comparing `autoapi-django-0.9.1/tests/test_quickstart.py` & `autoapi-django-0.9.2/tests/test_quickstart.py`

 * *Files identical despite different names*

