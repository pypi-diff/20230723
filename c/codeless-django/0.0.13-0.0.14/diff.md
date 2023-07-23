# Comparing `tmp/codeless-django-0.0.13.tar.gz` & `tmp/codeless-django-0.0.14.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "codeless-django-0.0.13.tar", last modified: Fri Jul 21 14:18:27 2023, max compression
+gzip compressed data, was "codeless-django-0.0.14.tar", last modified: Sun Jul 23 06:50:11 2023, max compression
```

## Comparing `codeless-django-0.0.13.tar` & `codeless-django-0.0.14.tar`

### file list

```diff
@@ -1,55 +1,77 @@
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-21 14:18:27.242252 codeless-django-0.0.13/
--rw-rw-r--   0 omar      (1000) omar      (1000)     1450 2023-04-11 02:03:29.000000 codeless-django-0.0.13/LICENSE
--rw-rw-r--   0 omar      (1000) omar      (1000)      228 2023-07-21 14:01:55.000000 codeless-django-0.0.13/MANIFEST.in
--rw-rw-r--   0 omar      (1000) omar      (1000)     1375 2023-07-21 14:18:27.242252 codeless-django-0.0.13/PKG-INFO
--rw-rw-r--   0 omar      (1000) omar      (1000)      828 2023-04-11 03:07:49.000000 codeless-django-0.0.13/README.md
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-21 14:18:27.234252 codeless-django-0.0.13/codeless_django/
--rw-rw-r--   0 omar      (1000) omar      (1000)        0 2023-04-11 01:56:03.000000 codeless-django-0.0.13/codeless_django/__init__.py
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-21 14:18:27.238252 codeless-django-0.0.13/codeless_django/additional_files/
--rw-rw-r--   0 omar      (1000) omar      (1000)     1823 2023-04-11 01:56:03.000000 codeless-django-0.0.13/codeless_django/additional_files/.gitignore
--rw-rw-r--   0 omar      (1000) omar      (1000)     1623 2023-04-11 01:56:03.000000 codeless-django-0.0.13/codeless_django/additional_files/root_urls.py
--rw-rw-r--   0 omar      (1000) omar      (1000)      154 2023-04-11 01:56:03.000000 codeless-django-0.0.13/codeless_django/apps.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     3218 2023-04-11 01:56:03.000000 codeless-django-0.0.13/codeless_django/data_manager.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     4463 2023-04-11 14:55:10.000000 codeless-django-0.0.13/codeless_django/fields.json
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-21 14:18:27.234252 codeless-django-0.0.13/codeless_django/templates/
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-21 14:18:27.238252 codeless-django-0.0.13/codeless_django/templates/codeless_django/
--rw-rw-r--   0 omar      (1000) omar      (1000)     2183 2023-04-11 01:56:03.000000 codeless-django-0.0.13/codeless_django/templates/codeless_django/base.html
--rw-rw-r--   0 omar      (1000) omar      (1000)     2925 2023-04-11 14:28:30.000000 codeless-django-0.0.13/codeless_django/templates/codeless_django/demo.html
--rw-rw-r--   0 omar      (1000) omar      (1000)      369 2023-04-11 01:56:03.000000 codeless-django-0.0.13/codeless_django/templates/codeless_django/fields.html
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-21 14:18:27.238252 codeless-django-0.0.13/codeless_django/templates/codeless_django/forms/
--rw-rw-r--   0 omar      (1000) omar      (1000)      121 2023-04-11 01:56:03.000000 codeless-django-0.0.13/codeless_django/templates/codeless_django/forms/all_field_types.html
--rw-rw-r--   0 omar      (1000) omar      (1000)      480 2023-04-11 01:56:03.000000 codeless-django-0.0.13/codeless_django/templates/codeless_django/forms/app_form.html
--rw-rw-r--   0 omar      (1000) omar      (1000)      198 2023-04-11 01:56:03.000000 codeless-django-0.0.13/codeless_django/templates/codeless_django/forms/choice_option.html
--rw-rw-r--   0 omar      (1000) omar      (1000)      257 2023-04-11 01:56:03.000000 codeless-django-0.0.13/codeless_django/templates/codeless_django/forms/common_option_form.html
--rw-rw-r--   0 omar      (1000) omar      (1000)      288 2023-04-11 01:56:03.000000 codeless-django-0.0.13/codeless_django/templates/codeless_django/forms/dropdown_option.html
--rw-rw-r--   0 omar      (1000) omar      (1000)      986 2023-04-11 01:56:03.000000 codeless-django-0.0.13/codeless_django/templates/codeless_django/forms/field_form.html
--rw-rw-r--   0 omar      (1000) omar      (1000)      761 2023-04-11 01:56:03.000000 codeless-django-0.0.13/codeless_django/templates/codeless_django/forms/field_option.html
--rw-rw-r--   0 omar      (1000) omar      (1000)      159 2023-04-11 01:56:03.000000 codeless-django-0.0.13/codeless_django/templates/codeless_django/forms/model_form.html
--rw-rw-r--   0 omar      (1000) omar      (1000)     1122 2023-04-11 01:56:03.000000 codeless-django-0.0.13/codeless_django/templates/codeless_django/forms/model_meta_form.html
--rw-rw-r--   0 omar      (1000) omar      (1000)        0 2023-04-11 01:56:03.000000 codeless-django-0.0.13/codeless_django/templates/codeless_django/forms/option_form.html
--rw-rw-r--   0 omar      (1000) omar      (1000)     3437 2023-04-11 01:56:03.000000 codeless-django-0.0.13/codeless_django/templates/codeless_django/home.html
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-21 14:18:27.238252 codeless-django-0.0.13/codeless_django/templatetags/
--rw-rw-r--   0 omar      (1000) omar      (1000)        0 2023-04-11 01:56:03.000000 codeless-django-0.0.13/codeless_django/templatetags/__init__.py
--rw-rw-r--   0 omar      (1000) omar      (1000)      716 2023-04-11 15:32:15.000000 codeless-django-0.0.13/codeless_django/templatetags/codeless_django_tags.py
--rw-rw-r--   0 omar      (1000) omar      (1000)       60 2023-04-11 01:56:03.000000 codeless-django-0.0.13/codeless_django/tests.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     1065 2023-04-11 01:56:03.000000 codeless-django-0.0.13/codeless_django/urls.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     3719 2023-04-23 15:48:20.000000 codeless-django-0.0.13/codeless_django/views.py
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-21 14:18:27.242252 codeless-django-0.0.13/codeless_django/writers/
--rw-rw-r--   0 omar      (1000) omar      (1000)        0 2023-04-11 01:56:03.000000 codeless-django-0.0.13/codeless_django/writers/__init__.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     1871 2023-04-11 01:56:03.000000 codeless-django-0.0.13/codeless_django/writers/apis.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     4645 2023-04-11 01:56:03.000000 codeless-django-0.0.13/codeless_django/writers/apps.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     1389 2023-04-11 01:56:03.000000 codeless-django-0.0.13/codeless_django/writers/base.py
--rw-rw-r--   0 omar      (1000) omar      (1000)      447 2023-04-11 15:15:42.000000 codeless-django-0.0.13/codeless_django/writers/documentation.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     2590 2023-04-11 15:25:44.000000 codeless-django-0.0.13/codeless_django/writers/files.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     1342 2023-04-11 01:56:03.000000 codeless-django-0.0.13/codeless_django/writers/models.py
--rw-rw-r--   0 omar      (1000) omar      (1000)      689 2023-04-11 15:17:07.000000 codeless-django-0.0.13/codeless_django/writers/serializers.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     1965 2023-04-11 01:56:03.000000 codeless-django-0.0.13/codeless_django/writers/views.py
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-21 14:18:27.234252 codeless-django-0.0.13/codeless_django.egg-info/
--rw-rw-r--   0 omar      (1000) omar      (1000)     1375 2023-07-21 14:18:27.000000 codeless-django-0.0.13/codeless_django.egg-info/PKG-INFO
--rw-rw-r--   0 omar      (1000) omar      (1000)     1816 2023-07-21 14:18:27.000000 codeless-django-0.0.13/codeless_django.egg-info/SOURCES.txt
--rw-rw-r--   0 omar      (1000) omar      (1000)        1 2023-07-21 14:18:27.000000 codeless-django-0.0.13/codeless_django.egg-info/dependency_links.txt
--rw-rw-r--   0 omar      (1000) omar      (1000)       12 2023-07-21 14:18:27.000000 codeless-django-0.0.13/codeless_django.egg-info/requires.txt
--rw-rw-r--   0 omar      (1000) omar      (1000)       16 2023-07-21 14:18:27.000000 codeless-django-0.0.13/codeless_django.egg-info/top_level.txt
--rw-rw-r--   0 omar      (1000) omar      (1000)      528 2023-07-21 14:18:12.000000 codeless-django-0.0.13/pyproject.toml
--rw-rw-r--   0 omar      (1000) omar      (1000)      938 2023-07-21 14:18:27.242252 codeless-django-0.0.13/setup.cfg
--rw-rw-r--   0 omar      (1000) omar      (1000)      139 2023-07-21 14:12:57.000000 codeless-django-0.0.13/setup.py
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 06:50:11.444571 codeless-django-0.0.14/
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1450 2023-04-11 02:03:29.000000 codeless-django-0.0.14/LICENSE
+-rw-rw-r--   0 omar      (1000) omar      (1000)      277 2023-07-23 06:49:00.000000 codeless-django-0.0.14/MANIFEST.in
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1375 2023-07-23 06:50:11.444571 codeless-django-0.0.14/PKG-INFO
+-rw-rw-r--   0 omar      (1000) omar      (1000)      828 2023-04-11 03:07:49.000000 codeless-django-0.0.14/README.md
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 06:50:11.436571 codeless-django-0.0.14/codeless_django/
+-rw-rw-r--   0 omar      (1000) omar      (1000)        0 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/__init__.py
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 06:50:11.436571 codeless-django-0.0.14/codeless_django/additional_files/
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1823 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/additional_files/.gitignore
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1623 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/additional_files/root_urls.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)      154 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/apps.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     3218 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/data_manager.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     4461 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/fields.json
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 06:50:11.432571 codeless-django-0.0.14/codeless_django/management/
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 06:50:11.436571 codeless-django-0.0.14/codeless_django/management/commands/
+-rw-rw-r--   0 omar      (1000) omar      (1000)        0 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/management/commands/__init__.py
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 06:50:11.436571 codeless-django-0.0.14/codeless_django/management/commands/__pycache__/
+-rw-rw-r--   0 omar      (1000) omar      (1000)      164 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/management/commands/__pycache__/__init__.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1428 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/management/commands/__pycache__/writeapps.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1144 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/management/commands/writeapps.py
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 06:50:11.432571 codeless-django-0.0.14/codeless_django/templates/
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 06:50:11.440571 codeless-django-0.0.14/codeless_django/templates/codeless_django/
+-rw-rw-r--   0 omar      (1000) omar      (1000)     2183 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templates/codeless_django/base.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)     2922 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templates/codeless_django/demo.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)      369 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templates/codeless_django/fields.html
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 06:50:11.440571 codeless-django-0.0.14/codeless_django/templates/codeless_django/forms/
+-rw-rw-r--   0 omar      (1000) omar      (1000)      121 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templates/codeless_django/forms/all_field_types.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)      480 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templates/codeless_django/forms/app_form.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)      198 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templates/codeless_django/forms/choice_option.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)      257 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templates/codeless_django/forms/common_option_form.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)      288 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templates/codeless_django/forms/dropdown_option.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)      986 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templates/codeless_django/forms/field_form.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)      761 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templates/codeless_django/forms/field_option.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)      159 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templates/codeless_django/forms/model_form.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1122 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templates/codeless_django/forms/model_meta_form.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)        0 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templates/codeless_django/forms/option_form.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)     3437 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templates/codeless_django/home.html
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 06:50:11.440571 codeless-django-0.0.14/codeless_django/templatetags/
+-rw-rw-r--   0 omar      (1000) omar      (1000)        0 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templatetags/__init__.py
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 06:50:11.440571 codeless-django-0.0.14/codeless_django/templatetags/__pycache__/
+-rw-rw-r--   0 omar      (1000) omar      (1000)      157 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templatetags/__pycache__/__init__.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)      820 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templatetags/__pycache__/codeless_django_tags.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)      575 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templatetags/codeless_django_tags.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)       60 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/tests.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1065 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/urls.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     3750 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/views.py
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 06:50:11.444571 codeless-django-0.0.14/codeless_django/writers/
+-rw-rw-r--   0 omar      (1000) omar      (1000)        0 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/__init__.py
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 06:50:11.444571 codeless-django-0.0.14/codeless_django/writers/__pycache__/
+-rw-rw-r--   0 omar      (1000) omar      (1000)      152 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/__pycache__/__init__.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     2838 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/__pycache__/apis.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     6218 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/__pycache__/apps.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     2648 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/__pycache__/base.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)      849 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/__pycache__/documentation.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     3889 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/__pycache__/files.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     2603 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/__pycache__/models.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1865 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/__pycache__/serializers.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1877 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/__pycache__/urls.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     3060 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/__pycache__/views.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1937 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/apis.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     5343 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/apps.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1248 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/base.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)      308 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/documentation.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     2580 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/files.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1907 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/models.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1150 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/serializers.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1933 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/urls.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     2055 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/views.py
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 06:50:11.436571 codeless-django-0.0.14/codeless_django.egg-info/
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1375 2023-07-23 06:50:11.000000 codeless-django-0.0.14/codeless_django.egg-info/PKG-INFO
+-rw-rw-r--   0 omar      (1000) omar      (1000)     2830 2023-07-23 06:50:11.000000 codeless-django-0.0.14/codeless_django.egg-info/SOURCES.txt
+-rw-rw-r--   0 omar      (1000) omar      (1000)        1 2023-07-23 06:50:11.000000 codeless-django-0.0.14/codeless_django.egg-info/dependency_links.txt
+-rw-rw-r--   0 omar      (1000) omar      (1000)       12 2023-07-23 06:50:11.000000 codeless-django-0.0.14/codeless_django.egg-info/requires.txt
+-rw-rw-r--   0 omar      (1000) omar      (1000)       16 2023-07-23 06:50:11.000000 codeless-django-0.0.14/codeless_django.egg-info/top_level.txt
+-rw-rw-r--   0 omar      (1000) omar      (1000)      528 2023-07-23 06:49:31.000000 codeless-django-0.0.14/pyproject.toml
+-rw-rw-r--   0 omar      (1000) omar      (1000)      938 2023-07-23 06:50:11.444571 codeless-django-0.0.14/setup.cfg
+-rw-rw-r--   0 omar      (1000) omar      (1000)      139 2023-07-21 14:12:57.000000 codeless-django-0.0.14/setup.py
```

### Comparing `codeless-django-0.0.13/LICENSE` & `codeless-django-0.0.14/LICENSE`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.13/PKG-INFO` & `codeless-django-0.0.14/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: codeless-django
-Version: 0.0.13
+Version: 0.0.14
 Summary: A Django app to create django apps, models, urls, views , api-views, documentation in a single click
 Home-page: https://www.example.com/
 Author: Omar Faruk
 Author-email: Omar Faruk <omar.iut.09@gmail.com>
 License: BSD-3-Clause  # Example license
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: BSD License
```

### Comparing `codeless-django-0.0.13/README.md` & `codeless-django-0.0.14/README.md`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.13/codeless_django/additional_files/.gitignore` & `codeless-django-0.0.14/codeless_django/additional_files/.gitignore`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.13/codeless_django/additional_files/root_urls.py` & `codeless-django-0.0.14/codeless_django/additional_files/root_urls.py`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.13/codeless_django/data_manager.py` & `codeless-django-0.0.14/codeless_django/data_manager.py`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.13/codeless_django/fields.json` & `codeless-django-0.0.14/codeless_django/fields.json`

 * *Format-specific differences are supported for JSON files but no file-specific differences were detected; falling back to a binary diff. file(1) reports: JSON text data*

 * *Files 0% similar despite different names*

```diff
@@ -1,279 +1,279 @@
-00000000: 0a0a 7b0a 2020 2020 2243 6f6d 6d6f 6e22  ..{.    "Common"
-00000010: 3a20 0a20 2020 205b 0a20 2020 2020 2020  : .    [.       
-00000020: 207b 226e 616d 6522 3a22 6e75 6c6c 222c   {"name":"null",
-00000030: 2274 7970 6522 3a22 6472 6f70 646f 776e  "type":"dropdown
-00000040: 222c 2022 6465 6661 756c 7422 3a66 616c  ", "default":fal
-00000050: 7365 7d2c 0a20 2020 2020 2020 207b 226e  se},.        {"n
-00000060: 616d 6522 3a22 626c 616e 6b22 2c22 7479  ame":"blank","ty
-00000070: 7065 223a 2264 726f 7064 6f77 6e22 2c20  pe":"dropdown", 
-00000080: 2264 6566 6175 6c74 223a 6661 6c73 657d  "default":false}
-00000090: 2c0a 2020 2020 2020 2020 7b22 6e61 6d65  ,.        {"name
-000000a0: 223a 2265 6469 7461 626c 6522 2c20 2274  ":"editable", "t
-000000b0: 7970 6522 3a22 6472 6f70 646f 776e 222c  ype":"dropdown",
-000000c0: 2264 6566 6175 6c74 223a 7472 7565 7d2c  "default":true},
-000000d0: 0a20 2020 2020 2020 207b 226e 616d 6522  .        {"name"
-000000e0: 3a22 6368 6f69 6365 7322 2c20 2274 7970  :"choices", "typ
-000000f0: 6522 3a22 7465 7874 222c 2264 6566 6175  e":"text","defau
-00000100: 6c74 223a 2222 7d2c 0a20 2020 2020 2020  lt":""},.       
-00000110: 207b 226e 616d 6522 3a22 6462 5f63 6f6c   {"name":"db_col
-00000120: 756d 6e22 2c20 2274 7970 6522 3a22 7465  umn", "type":"te
-00000130: 7874 222c 2022 6465 6661 756c 7422 3a22  xt", "default":"
-00000140: 227d 2c0a 2020 2020 2020 2020 7b22 6e61  "},.        {"na
-00000150: 6d65 223a 2264 625f 696e 6465 7822 2c20  me":"db_index", 
-00000160: 2274 7970 6522 3a22 6472 6f70 646f 776e  "type":"dropdown
-00000170: 222c 2022 6465 6661 756c 7422 3a66 616c  ", "default":fal
-00000180: 7365 7d2c 0a20 2020 2020 2020 207b 226e  se},.        {"n
-00000190: 616d 6522 3a22 6465 6661 756c 7422 2c20  ame":"default", 
-000001a0: 2274 7970 6522 3a22 7465 7874 222c 2022  "type":"text", "
-000001b0: 6465 6661 756c 7422 3a22 227d 2c0a 2020  default":""},.  
-000001c0: 2020 2020 2020 7b22 6e61 6d65 223a 2268        {"name":"h
-000001d0: 656c 705f 7465 7874 222c 2022 7479 7065  elp_text", "type
-000001e0: 223a 2274 6578 7422 2c20 2264 6566 6175  ":"text", "defau
-000001f0: 6c74 223a 2222 7d2c 0a20 2020 2020 2020  lt":""},.       
-00000200: 207b 226e 616d 6522 3a22 7072 696d 6172   {"name":"primar
-00000210: 795f 6b65 7922 2c20 2274 7970 6522 3a22  y_key", "type":"
-00000220: 6472 6f70 646f 776e 222c 2022 6465 6661  dropdown", "defa
-00000230: 756c 7422 3a66 616c 7365 7d2c 0a20 2020  ult":false},.   
-00000240: 2020 2020 207b 226e 616d 6522 3a22 756e       {"name":"un
-00000250: 6971 7565 222c 2022 7479 7065 223a 2264  ique", "type":"d
-00000260: 726f 7064 6f77 6e22 2c20 2264 6566 6175  ropdown", "defau
-00000270: 6c74 223a 6661 6c73 657d 2c0a 2020 2020  lt":false},.    
-00000280: 2020 2020 7b22 6e61 6d65 223a 2276 6572      {"name":"ver
-00000290: 626f 7365 5f6e 616d 6522 2c20 2274 7970  bose_name", "typ
-000002a0: 6522 3a22 7465 7874 222c 2022 6465 6661  e":"text", "defa
-000002b0: 756c 7422 3a22 227d 0a20 2020 2020 2020  ult":""}.       
-000002c0: 200a 2020 2020 5d2c 0a0a 2020 2020 2242   .    ],..    "B
-000002d0: 696e 6172 7946 6965 6c64 223a 5b0a 2020  inaryField":[.  
-000002e0: 2020 2020 2020 7b22 6e61 6d65 223a 226d        {"name":"m
-000002f0: 6178 5f6c 656e 6774 6822 2c20 2274 7970  ax_length", "typ
-00000300: 6522 3a22 7465 7874 222c 2022 6465 6661  e":"text", "defa
-00000310: 756c 7422 3a22 227d 0a0a 2020 2020 5d2c  ult":""}..    ],
-00000320: 0a20 2020 2022 426f 6f6c 6561 6e46 6965  .    "BooleanFie
-00000330: 6c64 223a 5b0a 0a20 2020 205d 2c0a 2020  ld":[..    ],.  
-00000340: 2020 2243 6861 7246 6965 6c64 223a 5b0a    "CharField":[.
-00000350: 2020 2020 2020 2020 7b22 6e61 6d65 223a          {"name":
-00000360: 226d 6178 5f6c 656e 6774 6822 2c20 2274  "max_length", "t
-00000370: 7970 6522 3a22 6e75 6d62 6572 222c 2022  ype":"number", "
-00000380: 6465 6661 756c 7422 3a31 3030 7d0a 2020  default":100}.  
-00000390: 2020 5d2c 0a20 2020 2022 4461 7465 4669    ],.    "DateFi
-000003a0: 656c 6422 3a5b 0a20 2020 2020 2020 207b  eld":[.        {
-000003b0: 226e 616d 6522 3a22 6175 746f 5f6e 6f77  "name":"auto_now
-000003c0: 222c 2022 7479 7065 223a 2264 726f 7064  ", "type":"dropd
-000003d0: 6f77 6e22 2c20 2264 6566 6175 6c74 223a  own", "default":
-000003e0: 6661 6c73 657d 2c0a 2020 2020 2020 2020  false},.        
-000003f0: 7b22 6e61 6d65 223a 2261 7574 6f5f 6e6f  {"name":"auto_no
-00000400: 775f 6164 6422 2c20 2274 7970 6522 3a22  w_add", "type":"
-00000410: 6472 6f70 646f 776e 222c 2022 6465 6661  dropdown", "defa
-00000420: 756c 7422 3a66 616c 7365 7d0a 2020 2020  ult":false}.    
-00000430: 2020 200a 2020 2020 5d2c 0a20 2020 2022     .    ],.    "
-00000440: 4461 7465 5469 6d65 4669 656c 6422 3a5b  DateTimeField":[
-00000450: 0a20 2020 2020 2020 207b 226e 616d 6522  .        {"name"
-00000460: 3a22 6175 746f 5f6e 6f77 222c 2022 7479  :"auto_now", "ty
-00000470: 7065 223a 2264 726f 7064 6f77 6e22 2c20  pe":"dropdown", 
-00000480: 2264 6566 6175 6c74 223a 6661 6c73 657d  "default":false}
-00000490: 2c0a 2020 2020 2020 2020 7b22 6e61 6d65  ,.        {"name
-000004a0: 223a 2261 7574 6f5f 6e6f 775f 6164 6422  ":"auto_now_add"
-000004b0: 2c20 2274 7970 6522 3a22 6472 6f70 646f  , "type":"dropdo
-000004c0: 776e 222c 2022 6465 6661 756c 7422 3a66  wn", "default":f
-000004d0: 616c 7365 7d0a 2020 2020 2020 200a 2020  alse}.       .  
-000004e0: 2020 5d2c 0a20 2020 2022 4465 6369 6d61    ],.    "Decima
-000004f0: 6c46 6965 6c64 223a 5b0a 2020 2020 2020  lField":[.      
-00000500: 2020 7b22 6e61 6d65 223a 226d 6178 5f64    {"name":"max_d
-00000510: 6967 6974 7322 2c20 2274 7970 6522 3a22  igits", "type":"
-00000520: 6e75 6d62 6572 222c 2022 6465 6661 756c  number", "defaul
-00000530: 7422 3a35 7d2c 0a20 2020 2020 2020 207b  t":5},.        {
-00000540: 226e 616d 6522 3a22 6465 6369 6d61 6c5f  "name":"decimal_
-00000550: 706c 6163 6573 222c 2022 7479 7065 223a  places", "type":
-00000560: 226e 756d 6265 7222 2c20 2264 6566 6175  "number", "defau
-00000570: 6c74 223a 327d 0a20 2020 205d 2c0a 2020  lt":2}.    ],.  
-00000580: 2020 2244 7572 6174 696f 6e46 6965 6c64    "DurationField
-00000590: 223a 5b0a 0a20 2020 205d 2c0a 2020 2020  ":[..    ],.    
-000005a0: 2245 6d61 696c 4669 656c 6422 3a5b 0a20  "EmailField":[. 
-000005b0: 2020 2020 2020 207b 226e 616d 6522 3a22         {"name":"
-000005c0: 6d61 785f 6c65 6e67 7468 222c 2022 7479  max_length", "ty
-000005d0: 7065 223a 226e 756d 6265 7222 2c20 2264  pe":"number", "d
-000005e0: 6566 6175 6c74 223a 3235 347d 0a20 2020  efault":254}.   
-000005f0: 205d 2c0a 2020 2020 2246 696c 6546 6965   ],.    "FileFie
-00000600: 6c64 223a 5b0a 2020 2020 2020 2020 7b22  ld":[.        {"
-00000610: 6e61 6d65 223a 2275 706c 6f61 645f 746f  name":"upload_to
-00000620: 222c 2022 7479 7065 223a 2274 6578 7422  ", "type":"text"
-00000630: 2c20 2264 6566 6175 6c74 223a 2222 7d2c  , "default":""},
-00000640: 0a20 2020 2020 2020 207b 226e 616d 6522  .        {"name"
-00000650: 3a22 7374 6f72 6167 6522 2c20 2274 7970  :"storage", "typ
-00000660: 6522 3a22 7465 7874 222c 2022 6465 6661  e":"text", "defa
-00000670: 756c 7422 3a22 227d 2c0a 2020 2020 2020  ult":""},.      
-00000680: 2020 7b22 6e61 6d65 223a 226d 6178 5f6c    {"name":"max_l
-00000690: 656e 6774 6822 2c20 2274 7970 6522 3a22  ength", "type":"
-000006a0: 6e75 6d62 6572 222c 2022 6465 6661 756c  number", "defaul
-000006b0: 7422 3a31 3030 7d0a 0a20 2020 205d 2c0a  t":100}..    ],.
-000006c0: 2020 0a20 2020 2022 466c 6f61 7446 6965    .    "FloatFie
-000006d0: 6c64 223a 0a20 2020 205b 5d2c 0a20 2020  ld":.    [],.   
-000006e0: 2022 4765 6e65 7269 6349 5041 6464 7265   "GenericIPAddre
-000006f0: 7373 4669 656c 6422 3a5b 0a20 2020 2020  ssField":[.     
-00000700: 2020 207b 226e 616d 6522 3a22 7072 6f74     {"name":"prot
-00000710: 6f63 6f6c 222c 2022 7479 7065 223a 2274  ocol", "type":"t
-00000720: 6578 7422 2c20 2264 6566 6175 6c74 223a  ext", "default":
-00000730: 2262 6f74 6822 7d2c 0a20 2020 2020 2020  "both"},.       
-00000740: 207b 226e 616d 6522 3a22 756e 7061 636b   {"name":"unpack
-00000750: 5f69 7076 3422 2c20 2274 7970 6522 3a22  _ipv4", "type":"
-00000760: 6472 6f70 646f 776e 222c 2022 6465 6661  dropdown", "defa
-00000770: 756c 7422 3a66 616c 7365 7d0a 0a20 2020  ult":false}..   
-00000780: 205d 2c0a 2020 2020 2249 6d61 6765 4669   ],.    "ImageFi
-00000790: 656c 6422 3a5b 0a20 2020 2020 2020 207b  eld":[.        {
-000007a0: 226e 616d 6522 3a22 7570 6c6f 6164 5f74  "name":"upload_t
-000007b0: 6f22 2c20 2274 7970 6522 3a22 7465 7874  o", "type":"text
-000007c0: 222c 2022 6465 6661 756c 7422 3a22 227d  ", "default":""}
-000007d0: 2c0a 2020 2020 2020 2020 7b22 6e61 6d65  ,.        {"name
-000007e0: 223a 2268 6569 6768 745f 6669 656c 6422  ":"height_field"
-000007f0: 2c20 2274 7970 6522 3a22 7465 7874 222c  , "type":"text",
-00000800: 2022 6465 6661 756c 7422 3a22 227d 2c0a   "default":""},.
-00000810: 2020 2020 2020 2020 7b22 6e61 6d65 223a          {"name":
-00000820: 2277 6964 7468 5f66 6965 6c64 222c 2022  "width_field", "
-00000830: 7479 7065 223a 2274 6578 7422 2c20 2264  type":"text", "d
-00000840: 6566 6175 6c74 223a 2222 7d2c 0a20 2020  efault":""},.   
-00000850: 2020 2020 207b 226e 616d 6522 3a22 6d61       {"name":"ma
-00000860: 785f 6c65 6e67 7468 222c 2022 7479 7065  x_length", "type
-00000870: 223a 226e 756d 6265 7222 2c20 2264 6566  ":"number", "def
-00000880: 6175 6c74 223a 3130 307d 0a0a 0a20 2020  ault":100}...   
-00000890: 205d 2c0a 2020 2020 2249 6e74 6567 6572   ],.    "Integer
-000008a0: 4669 656c 6422 3a5b 0a0a 2020 2020 5d2c  Field":[..    ],
-000008b0: 0a20 2020 2022 4a53 4f4e 4669 656c 6422  .    "JSONField"
-000008c0: 3a5b 0a20 2020 2020 2020 207b 226e 616d  :[.        {"nam
-000008d0: 6522 3a22 656e 636f 6465 7222 2c20 2274  e":"encoder", "t
-000008e0: 7970 6522 3a22 7465 7874 222c 2022 6465  ype":"text", "de
-000008f0: 6661 756c 7422 3a22 227d 2c0a 2020 2020  fault":""},.    
-00000900: 2020 2020 7b22 6e61 6d65 223a 2264 6563      {"name":"dec
-00000910: 6f64 6572 222c 2022 7479 7065 223a 2274  oder", "type":"t
-00000920: 6578 7422 2c20 2264 6566 6175 6c74 223a  ext", "default":
-00000930: 2222 7d0a 2020 2020 5d2c 0a20 2020 2022  ""}.    ],.    "
-00000940: 506f 7369 7469 7665 4269 6749 6e74 6567  PositiveBigInteg
-00000950: 6572 4669 656c 6422 3a5b 5d2c 0a20 2020  erField":[],.   
-00000960: 2022 506f 7369 7469 7665 496e 7465 6765   "PositiveIntege
-00000970: 7246 6965 6c64 223a 5b5d 2c0a 2020 2020  rField":[],.    
-00000980: 2250 6f73 6974 6976 6553 6d61 6c6c 496e  "PositiveSmallIn
-00000990: 7465 6765 7246 6965 6c64 223a 5b5d 2c0a  tegerField":[],.
-000009a0: 2020 2020 2253 6c75 6746 6965 6c64 223a      "SlugField":
-000009b0: 5b0a 2020 2020 2020 2020 7b22 6e61 6d65  [.        {"name
-000009c0: 223a 226d 6178 5f6c 656e 6774 6822 2c20  ":"max_length", 
-000009d0: 2274 7970 6522 3a22 6e75 6d62 6572 222c  "type":"number",
-000009e0: 2022 6465 6661 756c 7422 3a35 307d 0a20   "default":50}. 
-000009f0: 2020 205d 2c0a 2020 2020 2253 6d61 6c6c     ],.    "Small
-00000a00: 4175 746f 4669 656c 6422 3a5b 5d2c 0a20  AutoField":[],. 
-00000a10: 2020 2022 536d 616c 6c49 6e74 6567 6572     "SmallInteger
-00000a20: 4669 656c 6422 3a5b 5d2c 0a20 2020 2022  Field":[],.    "
-00000a30: 5465 7874 4669 656c 6422 3a5b 5d2c 0a20  TextField":[],. 
-00000a40: 2020 2022 5469 6d65 4669 656c 6422 3a5b     "TimeField":[
-00000a50: 0a20 2020 2020 2020 207b 226e 616d 6522  .        {"name"
-00000a60: 3a22 6175 746f 5f6e 6f77 222c 2022 7479  :"auto_now", "ty
-00000a70: 7065 223a 2264 726f 7064 6f77 6e22 2c20  pe":"dropdown", 
-00000a80: 2264 6566 6175 6c74 223a 6661 6c73 657d  "default":false}
-00000a90: 2c0a 2020 2020 2020 2020 7b22 6e61 6d65  ,.        {"name
-00000aa0: 223a 2261 7574 6f5f 6e6f 775f 6164 6422  ":"auto_now_add"
-00000ab0: 2c20 2274 7970 6522 3a22 6472 6f70 646f  , "type":"dropdo
-00000ac0: 776e 222c 2022 6465 6661 756c 7422 3a66  wn", "default":f
-00000ad0: 616c 7365 7d0a 200a 2020 2020 5d2c 0a20  alse}. .    ],. 
-00000ae0: 2020 2022 5552 4c46 6965 6c64 223a 5b0a     "URLField":[.
-00000af0: 2020 2020 2020 2020 7b22 6e61 6d65 223a          {"name":
-00000b00: 226d 6178 5f6c 656e 6774 6822 2c20 2274  "max_length", "t
-00000b10: 7970 6522 3a22 6e75 6d62 6572 222c 2022  ype":"number", "
-00000b20: 6465 6661 756c 7422 3a32 3030 7d0a 2020  default":200}.  
-00000b30: 2020 5d2c 0a20 2020 2022 5555 4944 4669    ],.    "UUIDFi
-00000b40: 656c 6422 3a5b 5d2c 0a20 2020 2022 466f  eld":[],.    "Fo
-00000b50: 7265 6967 6e4b 6579 223a 5b0a 2020 2020  reignKey":[.    
-00000b60: 2020 2020 7b22 6e61 6d65 223a 2274 6f22      {"name":"to"
-00000b70: 2c20 2274 7970 6522 3a22 7465 7874 222c  , "type":"text",
-00000b80: 2022 6465 6661 756c 7422 3a22 4d6f 6465   "default":"Mode
-00000b90: 6c2d 4e61 6d65 227d 2c0a 2020 2020 2020  l-Name"},.      
-00000ba0: 2020 7b22 6e61 6d65 223a 226f 6e5f 6465    {"name":"on_de
-00000bb0: 6c65 7465 222c 2022 7479 7065 223a 2263  lete", "type":"c
-00000bc0: 686f 6963 6522 2c20 2263 686f 6963 6573  hoice", "choices
-00000bd0: 223a 5b0a 2020 2020 2020 2020 2020 2020  ":[.            
-00000be0: 226d 6f64 656c 732e 4341 5343 4144 4522  "models.CASCADE"
-00000bf0: 2c0a 2020 2020 2020 2020 2020 2020 226d  ,.            "m
-00000c00: 6f64 656c 732e 5052 4f54 4543 5422 2c0a  odels.PROTECT",.
-00000c10: 2020 2020 2020 2020 2020 2020 226d 6f64              "mod
-00000c20: 656c 732e 5245 5354 5249 4354 222c 0a20  els.RESTRICT",. 
-00000c30: 2020 2020 2020 2020 2020 2022 6d6f 6465             "mode
-00000c40: 6c73 2e53 4554 5f4e 554c 4c22 2c0a 2020  ls.SET_NULL",.  
-00000c50: 2020 2020 2020 2020 2020 226d 6f64 656c            "model
-00000c60: 732e 5345 545f 4445 4641 554c 5422 0a0a  s.SET_DEFAULT"..
-00000c70: 2020 2020 2020 2020 5d20 2c22 6465 6661          ] ,"defa
-00000c80: 756c 7422 3a22 227d 2c0a 2020 2020 2020  ult":""},.      
-00000c90: 2020 7b22 6e61 6d65 223a 226c 696d 6974    {"name":"limit
-00000ca0: 5f63 686f 6963 6573 5f74 6f22 2c20 2274  _choices_to", "t
-00000cb0: 7970 6522 3a22 7465 7874 222c 2022 6465  ype":"text", "de
-00000cc0: 6661 756c 7422 3a22 227d 2c0a 2020 2020  fault":""},.    
-00000cd0: 2020 2020 7b22 6e61 6d65 223a 2272 656c      {"name":"rel
-00000ce0: 6174 6564 5f6e 616d 6522 2c20 2274 7970  ated_name", "typ
-00000cf0: 6522 3a22 7465 7874 222c 2022 6465 6661  e":"text", "defa
-00000d00: 756c 7422 3a22 227d 2c0a 2020 2020 2020  ult":""},.      
-00000d10: 2020 7b22 6e61 6d65 223a 2272 656c 6174    {"name":"relat
-00000d20: 6564 5f71 7565 7279 5f6e 616d 6522 2c20  ed_query_name", 
-00000d30: 2274 7970 6522 3a22 7465 7874 222c 2022  "type":"text", "
-00000d40: 6465 6661 756c 7422 3a22 227d 2c0a 2020  default":""},.  
-00000d50: 2020 2020 2020 7b22 6e61 6d65 223a 2274        {"name":"t
-00000d60: 6f5f 6669 656c 6422 2c20 2274 7970 6522  o_field", "type"
-00000d70: 3a22 7465 7874 222c 2022 6465 6661 756c  :"text", "defaul
-00000d80: 7422 3a22 227d 0a0a 0a20 2020 205d 2c0a  t":""}...    ],.
-00000d90: 2020 2020 224d 616e 7954 6f4d 616e 7946      "ManyToManyF
-00000da0: 6965 6c64 223a 5b0a 2020 2020 2020 2020  ield":[.        
-00000db0: 7b22 6e61 6d65 223a 2274 6f22 2c20 2274  {"name":"to", "t
-00000dc0: 7970 6522 3a22 7465 7874 222c 2022 6465  ype":"text", "de
-00000dd0: 6661 756c 7422 3a22 4d4f 6465 6c20 4e61  fault":"MOdel Na
-00000de0: 6d65 227d 2c0a 2020 2020 2020 2020 7b22  me"},.        {"
-00000df0: 6e61 6d65 223a 226c 696d 6974 5f63 686f  name":"limit_cho
-00000e00: 6963 6573 5f74 6f22 2c20 2274 7970 6522  ices_to", "type"
-00000e10: 3a22 7465 7874 222c 2022 6465 6661 756c  :"text", "defaul
-00000e20: 7422 3a22 227d 2c0a 2020 2020 2020 2020  t":""},.        
-00000e30: 7b22 6e61 6d65 223a 2272 656c 6174 6564  {"name":"related
-00000e40: 5f6e 616d 6522 2c20 2274 7970 6522 3a22  _name", "type":"
-00000e50: 7465 7874 222c 2022 6465 6661 756c 7422  text", "default"
-00000e60: 3a22 227d 2c0a 2020 2020 2020 2020 7b22  :""},.        {"
-00000e70: 6e61 6d65 223a 2272 656c 6174 6564 5f71  name":"related_q
-00000e80: 7565 7279 5f6e 616d 6522 2c20 2274 7970  uery_name", "typ
-00000e90: 6522 3a22 7465 7874 222c 2022 6465 6661  e":"text", "defa
-00000ea0: 756c 7422 3a22 227d 2c0a 2020 2020 2020  ult":""},.      
-00000eb0: 2020 7b22 6e61 6d65 223a 2274 6872 6f75    {"name":"throu
-00000ec0: 6768 222c 2022 7479 7065 223a 2274 6578  gh", "type":"tex
-00000ed0: 7422 2c20 2264 6566 6175 6c74 223a 2222  t", "default":""
-00000ee0: 7d2c 0a20 2020 2020 2020 207b 226e 616d  },.        {"nam
-00000ef0: 6522 3a22 7468 726f 7567 685f 6669 656c  e":"through_fiel
-00000f00: 6473 222c 2022 7479 7065 223a 2274 6578  ds", "type":"tex
-00000f10: 7422 2c20 2264 6566 6175 6c74 223a 2222  t", "default":""
-00000f20: 7d2c 0a20 2020 2020 2020 207b 226e 616d  },.        {"nam
-00000f30: 6522 3a22 6462 5f74 6162 6c65 222c 2022  e":"db_table", "
-00000f40: 7479 7065 223a 2274 6578 7422 2c20 2264  type":"text", "d
-00000f50: 6566 6175 6c74 223a 2222 7d0a 0a0a 2020  efault":""}...  
-00000f60: 2020 5d2c 0a20 2020 2022 4f6e 6554 6f4f    ],.    "OneToO
-00000f70: 6e65 4669 656c 6422 3a5b 0a20 2020 2020  neField":[.     
-00000f80: 2020 207b 226e 616d 6522 3a22 746f 222c     {"name":"to",
-00000f90: 2022 7479 7065 223a 2274 6578 7422 2c20   "type":"text", 
-00000fa0: 2264 6566 6175 6c74 223a 2222 7d2c 0a20  "default":""},. 
-00000fb0: 2020 2020 2020 207b 226e 616d 6522 3a22         {"name":"
-00000fc0: 6f6e 5f64 656c 6574 6522 2c20 2274 7970  on_delete", "typ
-00000fd0: 6522 3a22 6368 6f69 6365 222c 2022 6368  e":"choice", "ch
-00000fe0: 6f69 6365 7322 3a5b 0a20 2020 2020 2020  oices":[.       
-00000ff0: 2020 2020 2022 6d6f 6465 6c73 2e43 4153       "models.CAS
-00001000: 4341 4445 222c 0a20 2020 2020 2020 2020  CADE",.         
-00001010: 2020 2022 6d6f 6465 6c73 2e50 524f 5445     "models.PROTE
-00001020: 4354 222c 0a20 2020 2020 2020 2020 2020  CT",.           
-00001030: 2022 6d6f 6465 6c73 2e52 4553 5452 4943   "models.RESTRIC
-00001040: 5422 2c0a 2020 2020 2020 2020 2020 2020  T",.            
-00001050: 226d 6f64 656c 732e 5345 545f 4e55 4c4c  "models.SET_NULL
-00001060: 222c 0a20 2020 2020 2020 2020 2020 2022  ",.            "
-00001070: 6d6f 6465 6c73 2e53 4554 5f44 4546 4155  models.SET_DEFAU
-00001080: 4c54 220a 0a20 2020 2020 2020 205d 202c  LT"..        ] ,
-00001090: 2264 6566 6175 6c74 223a 2222 7d2c 0a0a  "default":""},..
-000010a0: 0a0a 2020 2020 2020 2020 7b22 6e61 6d65  ..        {"name
-000010b0: 223a 226c 696d 6974 5f63 686f 6963 6573  ":"limit_choices
-000010c0: 5f74 6f22 2c20 2274 7970 6522 3a22 7465  _to", "type":"te
-000010d0: 7874 222c 2022 6465 6661 756c 7422 3a22  xt", "default":"
-000010e0: 227d 2c0a 2020 2020 2020 2020 7b22 6e61  "},.        {"na
-000010f0: 6d65 223a 2272 656c 6174 6564 5f6e 616d  me":"related_nam
-00001100: 6522 2c20 2274 7970 6522 3a22 7465 7874  e", "type":"text
-00001110: 222c 2022 6465 6661 756c 7422 3a22 227d  ", "default":""}
-00001120: 2c0a 2020 2020 2020 2020 7b22 6e61 6d65  ,.        {"name
-00001130: 223a 2270 6172 656e 745f 6c69 6e6b 222c  ":"parent_link",
-00001140: 2022 7479 7065 223a 2264 726f 7064 6f77   "type":"dropdow
-00001150: 6e22 2c20 2264 6566 6175 6c74 223a 6661  n", "default":fa
-00001160: 6c73 657d 0a0a 0a20 2020 205d 0a7d 0a    lse}...    ].}.
+00000000: 7b0a 2020 2020 2243 6f6d 6d6f 6e22 3a20  {.    "Common": 
+00000010: 0a20 2020 205b 0a20 2020 2020 2020 207b  .    [.        {
+00000020: 226e 616d 6522 3a22 6e75 6c6c 222c 2274  "name":"null","t
+00000030: 7970 6522 3a22 6472 6f70 646f 776e 222c  ype":"dropdown",
+00000040: 2022 6465 6661 756c 7422 3a66 616c 7365   "default":false
+00000050: 7d2c 0a20 2020 2020 2020 207b 226e 616d  },.        {"nam
+00000060: 6522 3a22 626c 616e 6b22 2c22 7479 7065  e":"blank","type
+00000070: 223a 2264 726f 7064 6f77 6e22 2c20 2264  ":"dropdown", "d
+00000080: 6566 6175 6c74 223a 6661 6c73 657d 2c0a  efault":false},.
+00000090: 2020 2020 2020 2020 7b22 6e61 6d65 223a          {"name":
+000000a0: 2265 6469 7461 626c 6522 2c20 2274 7970  "editable", "typ
+000000b0: 6522 3a22 6472 6f70 646f 776e 222c 2264  e":"dropdown","d
+000000c0: 6566 6175 6c74 223a 7472 7565 7d2c 0a20  efault":true},. 
+000000d0: 2020 2020 2020 207b 226e 616d 6522 3a22         {"name":"
+000000e0: 6368 6f69 6365 7322 2c20 2274 7970 6522  choices", "type"
+000000f0: 3a22 7465 7874 222c 2264 6566 6175 6c74  :"text","default
+00000100: 223a 2222 7d2c 0a20 2020 2020 2020 207b  ":""},.        {
+00000110: 226e 616d 6522 3a22 6462 5f63 6f6c 756d  "name":"db_colum
+00000120: 6e22 2c20 2274 7970 6522 3a22 7465 7874  n", "type":"text
+00000130: 222c 2022 6465 6661 756c 7422 3a22 227d  ", "default":""}
+00000140: 2c0a 2020 2020 2020 2020 7b22 6e61 6d65  ,.        {"name
+00000150: 223a 2264 625f 696e 6465 7822 2c20 2274  ":"db_index", "t
+00000160: 7970 6522 3a22 6472 6f70 646f 776e 222c  ype":"dropdown",
+00000170: 2022 6465 6661 756c 7422 3a66 616c 7365   "default":false
+00000180: 7d2c 0a20 2020 2020 2020 207b 226e 616d  },.        {"nam
+00000190: 6522 3a22 6465 6661 756c 7422 2c20 2274  e":"default", "t
+000001a0: 7970 6522 3a22 7465 7874 222c 2022 6465  ype":"text", "de
+000001b0: 6661 756c 7422 3a22 227d 2c0a 2020 2020  fault":""},.    
+000001c0: 2020 2020 7b22 6e61 6d65 223a 2268 656c      {"name":"hel
+000001d0: 705f 7465 7874 222c 2022 7479 7065 223a  p_text", "type":
+000001e0: 2274 6578 7422 2c20 2264 6566 6175 6c74  "text", "default
+000001f0: 223a 2222 7d2c 0a20 2020 2020 2020 207b  ":""},.        {
+00000200: 226e 616d 6522 3a22 7072 696d 6172 795f  "name":"primary_
+00000210: 6b65 7922 2c20 2274 7970 6522 3a22 6472  key", "type":"dr
+00000220: 6f70 646f 776e 222c 2022 6465 6661 756c  opdown", "defaul
+00000230: 7422 3a66 616c 7365 7d2c 0a20 2020 2020  t":false},.     
+00000240: 2020 207b 226e 616d 6522 3a22 756e 6971     {"name":"uniq
+00000250: 7565 222c 2022 7479 7065 223a 2264 726f  ue", "type":"dro
+00000260: 7064 6f77 6e22 2c20 2264 6566 6175 6c74  pdown", "default
+00000270: 223a 6661 6c73 657d 2c0a 2020 2020 2020  ":false},.      
+00000280: 2020 7b22 6e61 6d65 223a 2276 6572 626f    {"name":"verbo
+00000290: 7365 5f6e 616d 6522 2c20 2274 7970 6522  se_name", "type"
+000002a0: 3a22 7465 7874 222c 2022 6465 6661 756c  :"text", "defaul
+000002b0: 7422 3a22 227d 0a20 2020 2020 2020 200a  t":""}.        .
+000002c0: 2020 2020 5d2c 0a0a 2020 2020 2242 696e      ],..    "Bin
+000002d0: 6172 7946 6965 6c64 223a 5b0a 2020 2020  aryField":[.    
+000002e0: 2020 2020 7b22 6e61 6d65 223a 226d 6178      {"name":"max
+000002f0: 5f6c 656e 6774 6822 2c20 2274 7970 6522  _length", "type"
+00000300: 3a22 7465 7874 222c 2022 6465 6661 756c  :"text", "defaul
+00000310: 7422 3a22 227d 0a0a 2020 2020 5d2c 0a20  t":""}..    ],. 
+00000320: 2020 2022 426f 6f6c 6561 6e46 6965 6c64     "BooleanField
+00000330: 223a 5b0a 0a20 2020 205d 2c0a 2020 2020  ":[..    ],.    
+00000340: 2243 6861 7246 6965 6c64 223a 5b0a 2020  "CharField":[.  
+00000350: 2020 2020 2020 7b22 6e61 6d65 223a 226d        {"name":"m
+00000360: 6178 5f6c 656e 6774 6822 2c20 2274 7970  ax_length", "typ
+00000370: 6522 3a22 6e75 6d62 6572 222c 2022 6465  e":"number", "de
+00000380: 6661 756c 7422 3a31 3030 7d0a 2020 2020  fault":100}.    
+00000390: 5d2c 0a20 2020 2022 4461 7465 4669 656c  ],.    "DateFiel
+000003a0: 6422 3a5b 0a20 2020 2020 2020 207b 226e  d":[.        {"n
+000003b0: 616d 6522 3a22 6175 746f 5f6e 6f77 222c  ame":"auto_now",
+000003c0: 2022 7479 7065 223a 2264 726f 7064 6f77   "type":"dropdow
+000003d0: 6e22 2c20 2264 6566 6175 6c74 223a 6661  n", "default":fa
+000003e0: 6c73 657d 2c0a 2020 2020 2020 2020 7b22  lse},.        {"
+000003f0: 6e61 6d65 223a 2261 7574 6f5f 6e6f 775f  name":"auto_now_
+00000400: 6164 6422 2c20 2274 7970 6522 3a22 6472  add", "type":"dr
+00000410: 6f70 646f 776e 222c 2022 6465 6661 756c  opdown", "defaul
+00000420: 7422 3a66 616c 7365 7d0a 2020 2020 2020  t":false}.      
+00000430: 200a 2020 2020 5d2c 0a20 2020 2022 4461   .    ],.    "Da
+00000440: 7465 5469 6d65 4669 656c 6422 3a5b 0a20  teTimeField":[. 
+00000450: 2020 2020 2020 207b 226e 616d 6522 3a22         {"name":"
+00000460: 6175 746f 5f6e 6f77 222c 2022 7479 7065  auto_now", "type
+00000470: 223a 2264 726f 7064 6f77 6e22 2c20 2264  ":"dropdown", "d
+00000480: 6566 6175 6c74 223a 6661 6c73 657d 2c0a  efault":false},.
+00000490: 2020 2020 2020 2020 7b22 6e61 6d65 223a          {"name":
+000004a0: 2261 7574 6f5f 6e6f 775f 6164 6422 2c20  "auto_now_add", 
+000004b0: 2274 7970 6522 3a22 6472 6f70 646f 776e  "type":"dropdown
+000004c0: 222c 2022 6465 6661 756c 7422 3a66 616c  ", "default":fal
+000004d0: 7365 7d0a 2020 2020 2020 200a 2020 2020  se}.       .    
+000004e0: 5d2c 0a20 2020 2022 4465 6369 6d61 6c46  ],.    "DecimalF
+000004f0: 6965 6c64 223a 5b0a 2020 2020 2020 2020  ield":[.        
+00000500: 7b22 6e61 6d65 223a 226d 6178 5f64 6967  {"name":"max_dig
+00000510: 6974 7322 2c20 2274 7970 6522 3a22 6e75  its", "type":"nu
+00000520: 6d62 6572 222c 2022 6465 6661 756c 7422  mber", "default"
+00000530: 3a35 7d2c 0a20 2020 2020 2020 207b 226e  :5},.        {"n
+00000540: 616d 6522 3a22 6465 6369 6d61 6c5f 706c  ame":"decimal_pl
+00000550: 6163 6573 222c 2022 7479 7065 223a 226e  aces", "type":"n
+00000560: 756d 6265 7222 2c20 2264 6566 6175 6c74  umber", "default
+00000570: 223a 327d 0a20 2020 205d 2c0a 2020 2020  ":2}.    ],.    
+00000580: 2244 7572 6174 696f 6e46 6965 6c64 223a  "DurationField":
+00000590: 5b0a 0a20 2020 205d 2c0a 2020 2020 2245  [..    ],.    "E
+000005a0: 6d61 696c 4669 656c 6422 3a5b 0a20 2020  mailField":[.   
+000005b0: 2020 2020 207b 226e 616d 6522 3a22 6d61       {"name":"ma
+000005c0: 785f 6c65 6e67 7468 222c 2022 7479 7065  x_length", "type
+000005d0: 223a 226e 756d 6265 7222 2c20 2264 6566  ":"number", "def
+000005e0: 6175 6c74 223a 3235 347d 0a20 2020 205d  ault":254}.    ]
+000005f0: 2c0a 2020 2020 2246 696c 6546 6965 6c64  ,.    "FileField
+00000600: 223a 5b0a 2020 2020 2020 2020 7b22 6e61  ":[.        {"na
+00000610: 6d65 223a 2275 706c 6f61 645f 746f 222c  me":"upload_to",
+00000620: 2022 7479 7065 223a 2274 6578 7422 2c20   "type":"text", 
+00000630: 2264 6566 6175 6c74 223a 2222 7d2c 0a20  "default":""},. 
+00000640: 2020 2020 2020 207b 226e 616d 6522 3a22         {"name":"
+00000650: 7374 6f72 6167 6522 2c20 2274 7970 6522  storage", "type"
+00000660: 3a22 7465 7874 222c 2022 6465 6661 756c  :"text", "defaul
+00000670: 7422 3a22 227d 2c0a 2020 2020 2020 2020  t":""},.        
+00000680: 7b22 6e61 6d65 223a 226d 6178 5f6c 656e  {"name":"max_len
+00000690: 6774 6822 2c20 2274 7970 6522 3a22 6e75  gth", "type":"nu
+000006a0: 6d62 6572 222c 2022 6465 6661 756c 7422  mber", "default"
+000006b0: 3a31 3030 7d0a 0a20 2020 205d 2c0a 2020  :100}..    ],.  
+000006c0: 0a20 2020 2022 466c 6f61 7446 6965 6c64  .    "FloatField
+000006d0: 223a 0a20 2020 205b 5d2c 0a20 2020 2022  ":.    [],.    "
+000006e0: 4765 6e65 7269 6349 5041 6464 7265 7373  GenericIPAddress
+000006f0: 4669 656c 6422 3a5b 0a20 2020 2020 2020  Field":[.       
+00000700: 207b 226e 616d 6522 3a22 7072 6f74 6f63   {"name":"protoc
+00000710: 6f6c 222c 2022 7479 7065 223a 2274 6578  ol", "type":"tex
+00000720: 7422 2c20 2264 6566 6175 6c74 223a 2262  t", "default":"b
+00000730: 6f74 6822 7d2c 0a20 2020 2020 2020 207b  oth"},.        {
+00000740: 226e 616d 6522 3a22 756e 7061 636b 5f69  "name":"unpack_i
+00000750: 7076 3422 2c20 2274 7970 6522 3a22 6472  pv4", "type":"dr
+00000760: 6f70 646f 776e 222c 2022 6465 6661 756c  opdown", "defaul
+00000770: 7422 3a66 616c 7365 7d0a 0a20 2020 205d  t":false}..    ]
+00000780: 2c0a 2020 2020 2249 6d61 6765 4669 656c  ,.    "ImageFiel
+00000790: 6422 3a5b 0a20 2020 2020 2020 207b 226e  d":[.        {"n
+000007a0: 616d 6522 3a22 7570 6c6f 6164 5f74 6f22  ame":"upload_to"
+000007b0: 2c20 2274 7970 6522 3a22 7465 7874 222c  , "type":"text",
+000007c0: 2022 6465 6661 756c 7422 3a22 227d 2c0a   "default":""},.
+000007d0: 2020 2020 2020 2020 7b22 6e61 6d65 223a          {"name":
+000007e0: 2268 6569 6768 745f 6669 656c 6422 2c20  "height_field", 
+000007f0: 2274 7970 6522 3a22 7465 7874 222c 2022  "type":"text", "
+00000800: 6465 6661 756c 7422 3a22 227d 2c0a 2020  default":""},.  
+00000810: 2020 2020 2020 7b22 6e61 6d65 223a 2277        {"name":"w
+00000820: 6964 7468 5f66 6965 6c64 222c 2022 7479  idth_field", "ty
+00000830: 7065 223a 2274 6578 7422 2c20 2264 6566  pe":"text", "def
+00000840: 6175 6c74 223a 2222 7d2c 0a20 2020 2020  ault":""},.     
+00000850: 2020 207b 226e 616d 6522 3a22 6d61 785f     {"name":"max_
+00000860: 6c65 6e67 7468 222c 2022 7479 7065 223a  length", "type":
+00000870: 226e 756d 6265 7222 2c20 2264 6566 6175  "number", "defau
+00000880: 6c74 223a 3130 307d 0a0a 0a20 2020 205d  lt":100}...    ]
+00000890: 2c0a 2020 2020 2249 6e74 6567 6572 4669  ,.    "IntegerFi
+000008a0: 656c 6422 3a5b 0a0a 2020 2020 5d2c 0a20  eld":[..    ],. 
+000008b0: 2020 2022 4a53 4f4e 4669 656c 6422 3a5b     "JSONField":[
+000008c0: 0a20 2020 2020 2020 207b 226e 616d 6522  .        {"name"
+000008d0: 3a22 656e 636f 6465 7222 2c20 2274 7970  :"encoder", "typ
+000008e0: 6522 3a22 7465 7874 222c 2022 6465 6661  e":"text", "defa
+000008f0: 756c 7422 3a22 227d 2c0a 2020 2020 2020  ult":""},.      
+00000900: 2020 7b22 6e61 6d65 223a 2264 6563 6f64    {"name":"decod
+00000910: 6572 222c 2022 7479 7065 223a 2274 6578  er", "type":"tex
+00000920: 7422 2c20 2264 6566 6175 6c74 223a 2222  t", "default":""
+00000930: 7d0a 2020 2020 5d2c 0a20 2020 2022 506f  }.    ],.    "Po
+00000940: 7369 7469 7665 4269 6749 6e74 6567 6572  sitiveBigInteger
+00000950: 4669 656c 6422 3a5b 5d2c 0a20 2020 2022  Field":[],.    "
+00000960: 506f 7369 7469 7665 496e 7465 6765 7246  PositiveIntegerF
+00000970: 6965 6c64 223a 5b5d 2c0a 2020 2020 2250  ield":[],.    "P
+00000980: 6f73 6974 6976 6553 6d61 6c6c 496e 7465  ositiveSmallInte
+00000990: 6765 7246 6965 6c64 223a 5b5d 2c0a 2020  gerField":[],.  
+000009a0: 2020 2253 6c75 6746 6965 6c64 223a 5b0a    "SlugField":[.
+000009b0: 2020 2020 2020 2020 7b22 6e61 6d65 223a          {"name":
+000009c0: 226d 6178 5f6c 656e 6774 6822 2c20 2274  "max_length", "t
+000009d0: 7970 6522 3a22 6e75 6d62 6572 222c 2022  ype":"number", "
+000009e0: 6465 6661 756c 7422 3a35 307d 0a20 2020  default":50}.   
+000009f0: 205d 2c0a 2020 2020 2253 6d61 6c6c 4175   ],.    "SmallAu
+00000a00: 746f 4669 656c 6422 3a5b 5d2c 0a20 2020  toField":[],.   
+00000a10: 2022 536d 616c 6c49 6e74 6567 6572 4669   "SmallIntegerFi
+00000a20: 656c 6422 3a5b 5d2c 0a20 2020 2022 5465  eld":[],.    "Te
+00000a30: 7874 4669 656c 6422 3a5b 5d2c 0a20 2020  xtField":[],.   
+00000a40: 2022 5469 6d65 4669 656c 6422 3a5b 0a20   "TimeField":[. 
+00000a50: 2020 2020 2020 207b 226e 616d 6522 3a22         {"name":"
+00000a60: 6175 746f 5f6e 6f77 222c 2022 7479 7065  auto_now", "type
+00000a70: 223a 2264 726f 7064 6f77 6e22 2c20 2264  ":"dropdown", "d
+00000a80: 6566 6175 6c74 223a 6661 6c73 657d 2c0a  efault":false},.
+00000a90: 2020 2020 2020 2020 7b22 6e61 6d65 223a          {"name":
+00000aa0: 2261 7574 6f5f 6e6f 775f 6164 6422 2c20  "auto_now_add", 
+00000ab0: 2274 7970 6522 3a22 6472 6f70 646f 776e  "type":"dropdown
+00000ac0: 222c 2022 6465 6661 756c 7422 3a66 616c  ", "default":fal
+00000ad0: 7365 7d0a 200a 2020 2020 5d2c 0a20 2020  se}. .    ],.   
+00000ae0: 2022 5552 4c46 6965 6c64 223a 5b0a 2020   "URLField":[.  
+00000af0: 2020 2020 2020 7b22 6e61 6d65 223a 226d        {"name":"m
+00000b00: 6178 5f6c 656e 6774 6822 2c20 2274 7970  ax_length", "typ
+00000b10: 6522 3a22 6e75 6d62 6572 222c 2022 6465  e":"number", "de
+00000b20: 6661 756c 7422 3a32 3030 7d0a 2020 2020  fault":200}.    
+00000b30: 5d2c 0a20 2020 2022 5555 4944 4669 656c  ],.    "UUIDFiel
+00000b40: 6422 3a5b 5d2c 0a20 2020 2022 466f 7265  d":[],.    "Fore
+00000b50: 6967 6e4b 6579 223a 5b0a 2020 2020 2020  ignKey":[.      
+00000b60: 2020 7b22 6e61 6d65 223a 2274 6f22 2c20    {"name":"to", 
+00000b70: 2274 7970 6522 3a22 7465 7874 222c 2022  "type":"text", "
+00000b80: 6465 6661 756c 7422 3a22 4d6f 6465 6c2d  default":"Model-
+00000b90: 4e61 6d65 227d 2c0a 2020 2020 2020 2020  Name"},.        
+00000ba0: 7b22 6e61 6d65 223a 226f 6e5f 6465 6c65  {"name":"on_dele
+00000bb0: 7465 222c 2022 7479 7065 223a 2263 686f  te", "type":"cho
+00000bc0: 6963 6522 2c20 2263 686f 6963 6573 223a  ice", "choices":
+00000bd0: 5b0a 2020 2020 2020 2020 2020 2020 226d  [.            "m
+00000be0: 6f64 656c 732e 4341 5343 4144 4522 2c0a  odels.CASCADE",.
+00000bf0: 2020 2020 2020 2020 2020 2020 226d 6f64              "mod
+00000c00: 656c 732e 5052 4f54 4543 5422 2c0a 2020  els.PROTECT",.  
+00000c10: 2020 2020 2020 2020 2020 226d 6f64 656c            "model
+00000c20: 732e 5245 5354 5249 4354 222c 0a20 2020  s.RESTRICT",.   
+00000c30: 2020 2020 2020 2020 2022 6d6f 6465 6c73           "models
+00000c40: 2e53 4554 5f4e 554c 4c22 2c0a 2020 2020  .SET_NULL",.    
+00000c50: 2020 2020 2020 2020 226d 6f64 656c 732e          "models.
+00000c60: 5345 545f 4445 4641 554c 5422 0a0a 2020  SET_DEFAULT"..  
+00000c70: 2020 2020 2020 5d20 2c22 6465 6661 756c        ] ,"defaul
+00000c80: 7422 3a22 227d 2c0a 2020 2020 2020 2020  t":""},.        
+00000c90: 7b22 6e61 6d65 223a 226c 696d 6974 5f63  {"name":"limit_c
+00000ca0: 686f 6963 6573 5f74 6f22 2c20 2274 7970  hoices_to", "typ
+00000cb0: 6522 3a22 7465 7874 222c 2022 6465 6661  e":"text", "defa
+00000cc0: 756c 7422 3a22 227d 2c0a 2020 2020 2020  ult":""},.      
+00000cd0: 2020 7b22 6e61 6d65 223a 2272 656c 6174    {"name":"relat
+00000ce0: 6564 5f6e 616d 6522 2c20 2274 7970 6522  ed_name", "type"
+00000cf0: 3a22 7465 7874 222c 2022 6465 6661 756c  :"text", "defaul
+00000d00: 7422 3a22 227d 2c0a 2020 2020 2020 2020  t":""},.        
+00000d10: 7b22 6e61 6d65 223a 2272 656c 6174 6564  {"name":"related
+00000d20: 5f71 7565 7279 5f6e 616d 6522 2c20 2274  _query_name", "t
+00000d30: 7970 6522 3a22 7465 7874 222c 2022 6465  ype":"text", "de
+00000d40: 6661 756c 7422 3a22 227d 2c0a 2020 2020  fault":""},.    
+00000d50: 2020 2020 7b22 6e61 6d65 223a 2274 6f5f      {"name":"to_
+00000d60: 6669 656c 6422 2c20 2274 7970 6522 3a22  field", "type":"
+00000d70: 7465 7874 222c 2022 6465 6661 756c 7422  text", "default"
+00000d80: 3a22 227d 0a0a 0a20 2020 205d 2c0a 2020  :""}...    ],.  
+00000d90: 2020 224d 616e 7954 6f4d 616e 7946 6965    "ManyToManyFie
+00000da0: 6c64 223a 5b0a 2020 2020 2020 2020 7b22  ld":[.        {"
+00000db0: 6e61 6d65 223a 2274 6f22 2c20 2274 7970  name":"to", "typ
+00000dc0: 6522 3a22 7465 7874 222c 2022 6465 6661  e":"text", "defa
+00000dd0: 756c 7422 3a22 4d4f 6465 6c20 4e61 6d65  ult":"MOdel Name
+00000de0: 227d 2c0a 2020 2020 2020 2020 7b22 6e61  "},.        {"na
+00000df0: 6d65 223a 226c 696d 6974 5f63 686f 6963  me":"limit_choic
+00000e00: 6573 5f74 6f22 2c20 2274 7970 6522 3a22  es_to", "type":"
+00000e10: 7465 7874 222c 2022 6465 6661 756c 7422  text", "default"
+00000e20: 3a22 227d 2c0a 2020 2020 2020 2020 7b22  :""},.        {"
+00000e30: 6e61 6d65 223a 2272 656c 6174 6564 5f6e  name":"related_n
+00000e40: 616d 6522 2c20 2274 7970 6522 3a22 7465  ame", "type":"te
+00000e50: 7874 222c 2022 6465 6661 756c 7422 3a22  xt", "default":"
+00000e60: 227d 2c0a 2020 2020 2020 2020 7b22 6e61  "},.        {"na
+00000e70: 6d65 223a 2272 656c 6174 6564 5f71 7565  me":"related_que
+00000e80: 7279 5f6e 616d 6522 2c20 2274 7970 6522  ry_name", "type"
+00000e90: 3a22 7465 7874 222c 2022 6465 6661 756c  :"text", "defaul
+00000ea0: 7422 3a22 227d 2c0a 2020 2020 2020 2020  t":""},.        
+00000eb0: 7b22 6e61 6d65 223a 2274 6872 6f75 6768  {"name":"through
+00000ec0: 222c 2022 7479 7065 223a 2274 6578 7422  ", "type":"text"
+00000ed0: 2c20 2264 6566 6175 6c74 223a 2222 7d2c  , "default":""},
+00000ee0: 0a20 2020 2020 2020 207b 226e 616d 6522  .        {"name"
+00000ef0: 3a22 7468 726f 7567 685f 6669 656c 6473  :"through_fields
+00000f00: 222c 2022 7479 7065 223a 2274 6578 7422  ", "type":"text"
+00000f10: 2c20 2264 6566 6175 6c74 223a 2222 7d2c  , "default":""},
+00000f20: 0a20 2020 2020 2020 207b 226e 616d 6522  .        {"name"
+00000f30: 3a22 6462 5f74 6162 6c65 222c 2022 7479  :"db_table", "ty
+00000f40: 7065 223a 2274 6578 7422 2c20 2264 6566  pe":"text", "def
+00000f50: 6175 6c74 223a 2222 7d0a 0a0a 2020 2020  ault":""}...    
+00000f60: 5d2c 0a20 2020 2022 4f6e 6554 6f4f 6e65  ],.    "OneToOne
+00000f70: 4669 656c 6422 3a5b 0a20 2020 2020 2020  Field":[.       
+00000f80: 207b 226e 616d 6522 3a22 746f 222c 2022   {"name":"to", "
+00000f90: 7479 7065 223a 2274 6578 7422 2c20 2264  type":"text", "d
+00000fa0: 6566 6175 6c74 223a 2222 7d2c 0a20 2020  efault":""},.   
+00000fb0: 2020 2020 207b 226e 616d 6522 3a22 6f6e       {"name":"on
+00000fc0: 5f64 656c 6574 6522 2c20 2274 7970 6522  _delete", "type"
+00000fd0: 3a22 6368 6f69 6365 222c 2022 6368 6f69  :"choice", "choi
+00000fe0: 6365 7322 3a5b 0a20 2020 2020 2020 2020  ces":[.         
+00000ff0: 2020 2022 6d6f 6465 6c73 2e43 4153 4341     "models.CASCA
+00001000: 4445 222c 0a20 2020 2020 2020 2020 2020  DE",.           
+00001010: 2022 6d6f 6465 6c73 2e50 524f 5445 4354   "models.PROTECT
+00001020: 222c 0a20 2020 2020 2020 2020 2020 2022  ",.            "
+00001030: 6d6f 6465 6c73 2e52 4553 5452 4943 5422  models.RESTRICT"
+00001040: 2c0a 2020 2020 2020 2020 2020 2020 226d  ,.            "m
+00001050: 6f64 656c 732e 5345 545f 4e55 4c4c 222c  odels.SET_NULL",
+00001060: 0a20 2020 2020 2020 2020 2020 2022 6d6f  .            "mo
+00001070: 6465 6c73 2e53 4554 5f44 4546 4155 4c54  dels.SET_DEFAULT
+00001080: 220a 0a20 2020 2020 2020 205d 202c 2264  "..        ] ,"d
+00001090: 6566 6175 6c74 223a 2222 7d2c 0a0a 0a0a  efault":""},....
+000010a0: 2020 2020 2020 2020 7b22 6e61 6d65 223a          {"name":
+000010b0: 226c 696d 6974 5f63 686f 6963 6573 5f74  "limit_choices_t
+000010c0: 6f22 2c20 2274 7970 6522 3a22 7465 7874  o", "type":"text
+000010d0: 222c 2022 6465 6661 756c 7422 3a22 227d  ", "default":""}
+000010e0: 2c0a 2020 2020 2020 2020 7b22 6e61 6d65  ,.        {"name
+000010f0: 223a 2272 656c 6174 6564 5f6e 616d 6522  ":"related_name"
+00001100: 2c20 2274 7970 6522 3a22 7465 7874 222c  , "type":"text",
+00001110: 2022 6465 6661 756c 7422 3a22 227d 2c0a   "default":""},.
+00001120: 2020 2020 2020 2020 7b22 6e61 6d65 223a          {"name":
+00001130: 2270 6172 656e 745f 6c69 6e6b 222c 2022  "parent_link", "
+00001140: 7479 7065 223a 2264 726f 7064 6f77 6e22  type":"dropdown"
+00001150: 2c20 2264 6566 6175 6c74 223a 6661 6c73  , "default":fals
+00001160: 657d 0a0a 0a20 2020 205d 0a7d 0a         e}...    ].}.
```

### Comparing `codeless-django-0.0.13/codeless_django/templates/codeless_django/base.html` & `codeless-django-0.0.14/codeless_django/templates/codeless_django/base.html`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.13/codeless_django/templates/codeless_django/demo.html` & `codeless-django-0.0.14/codeless_django/templates/codeless_django/demo.html`

 * *Files 1% similar despite different names*

```diff
@@ -81,19 +81,16 @@
     </ul>
 
   </li>
   {%endwith%}
   {%endfor%}
 </ul>
 
-
 <form action="{%url 'create-app' %}" method="post">
   <label for="api_views">api_view</label>
 <input type="checkbox" name="api_views" id="api_views" >
 <label for="template_views">template_views</label>
 <input type="checkbox" name="template_views" id="template_views">
 
   <button type="submit">Create Apps</button>
 </form>
-
-
 {% endblock content %}
```

### Comparing `codeless-django-0.0.13/codeless_django/templates/codeless_django/forms/field_form.html` & `codeless-django-0.0.14/codeless_django/templates/codeless_django/forms/field_form.html`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.13/codeless_django/templates/codeless_django/forms/field_option.html` & `codeless-django-0.0.14/codeless_django/templates/codeless_django/forms/field_option.html`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.13/codeless_django/templates/codeless_django/forms/model_meta_form.html` & `codeless-django-0.0.14/codeless_django/templates/codeless_django/forms/model_meta_form.html`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.13/codeless_django/templates/codeless_django/home.html` & `codeless-django-0.0.14/codeless_django/templates/codeless_django/home.html`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.13/codeless_django/urls.py` & `codeless-django-0.0.14/codeless_django/urls.py`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.13/codeless_django/views.py` & `codeless-django-0.0.14/codeless_django/views.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-from django.shortcuts import render,redirect
+from django.shortcuts import render,redirect,reverse
 from django.views.decorators.csrf import csrf_exempt
 import json
 from django.core.exceptions import BadRequest
 from django.http import HttpResponse
 from codeless_django.data_manager import DataManager
 from codeless_django.writers.apps import WriteApps
 from codeless_django.writers.files import AdditionalFileWriter
@@ -97,10 +97,9 @@
 @csrf_exempt
 def create_apps(request):
     write_template_views=bool(request.POST.get("template_views"))
     write_api_views=bool(request.POST.get("api_views"))
     data=data_manager._load_data()
     app_writer = WriteApps(data["apps"],write_template_views,write_api_views)
     app_writer.write()
-    os.system("rm data.json")
+    documentation_link = reverse('schema-swagger-ui')
     return redirect('/swagger/')
-
```

### Comparing `codeless-django-0.0.13/codeless_django/writers/apis.py` & `codeless-django-0.0.14/codeless_django/writers/views.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,50 +1,66 @@
-from codeless_django.writers.base import BaseViewWriter,BaseURLWriter
+from  codeless_django.writers.base import BaseWriter, BaseViewWriter,BaseURLWriter,BaseBuilder
 
 
-class BaseAPIViewWriter(BaseViewWriter):
+class BaseViewBuilder(BaseBuilder):
+    def __init__(self,app_name,model_name):
+        self.model_name=model_name
+        self.app_name=app_name
 
 
-    def get_object_body(self):
-        return f"\tserializer_class = serializers.{self.model_name}Serializer\n\tqueryset = {self.app_name}_models.{self.model_name}.objects.filter().select_related().prefetch_related()\n\t#authentication_classes=()"
+class CreateViewBuilder(BaseViewBuilder):
 
+    def get_object_header(self):
+        return f"class {self.model_name}CreateView(generic.CreateView):\n"
 
-class ListCreateAPIViewWriter(BaseAPIViewWriter):
+    def get_object_body(self):
+        return f"\tmodel = {self.app_name}_models.{self.model_name}\n\tfields = '__all__'\n\tsuccess_url= ' \ \' "
 
-    def __init__(self,app_name, model_name):
-        super().__init__(app_name,model_name)
 
-    def get_object_header(self):
-        return f"class {self.model_name}ListCreateAPIView(generics.ListCreateAPIView):\n"
+class ListViewBuilder(BaseViewBuilder):
 
-class RetrieveUpdateDestroyAPIViewWriter(BaseAPIViewWriter):
+    def get_object_header(self):
+        return f"class {self.model_name}ListView(generic.ListView):\n"
 
-    def __init__(self,app_name, model_name):
-        super().__init__(app_name,model_name)
+    def get_object_body(self):
+        return f"\tmodel =  {self.app_name}_models.{self.model_name}\n\tpaginate_by = 10 \n"
 
-    def get_object_header(self):
-        return f"class {self.model_name}RetrieveUpdateDestroyAPIView(generics.RetrieveUpdateDestroyAPIView):\n"
 
-class APIUrlWriter(BaseURLWriter):
+class DetailViewBuilder(BaseViewBuilder):
 
+    def get_object_header(self):
+        return f"class {self.model_name}DetailView(generic.DetailView):\n"
 
-    def get_url_string(self):
-        url_string = ''
-        url_string += f"    path('{self.model_name.lower()}s/', views.{self.model_name}ListCreateAPIView.as_view(), name='{self.model_name.lower()}_list_create'),\n"
-        url_string += f"    path('{self.model_name.lower()}s/<int:pk>', views.{self.model_name}RetrieveUpdateDestroyAPIView.as_view(), name='{self.model_name.lower()}_retrieve_update_destroy'),\n"
-        return url_string
+    def get_object_body(self):
+        return f"\tmodel =  {self.app_name}_models.{self.model_name} \n"
 
 
+class UpdateViewBuilder(BaseViewBuilder):
 
+    def get_object_header(self):
+        return f"class {self.model_name}UpdateView(generic.UpdateView):\n"
 
-class APIViewURLWriter:
+    def get_object_body(self):
+        return f"\tmodel =  {self.app_name}_models.{self.model_name} \n"
+    
 
-    def __init__(self,app_name, model_name):
-        self.model_name = model_name
+class ViewWriter(BaseWriter):
+    def __init__(self, app_name,models):
+        self.models = models
         self.app_name=app_name
+        file_name = f"{app_name}/views.py"
+        super().__init__(file_name)
     
-    def write_api_views_and_urls(self):
+    def get_full_string(self):
         app_name=self.app_name
-        model_name=self.model_name
-        ListCreateAPIViewWriter(app_name, model_name).write_object()
-        RetrieveUpdateDestroyAPIViewWriter(app_name, model_name).write_object()
-        APIUrlWriter(app_name, model_name).write_object()
+        full_string = ""
+        for model_name in self.models.keys():
+            full_string+=ListViewBuilder(app_name, model_name).get_object_string()
+            full_string+=DetailViewBuilder(app_name, model_name).get_object_string()
+            full_string+=UpdateViewBuilder(app_name, model_name).get_object_string()
+            full_string+=CreateViewBuilder(app_name, model_name).get_object_string()
+
+        return full_string
+
+
+
+
```

### Comparing `codeless-django-0.0.13/codeless_django/writers/apps.py` & `codeless-django-0.0.14/codeless_django/writers/apps.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 import os
 from django.conf import settings
-from codeless_django.writers.views import ViewURLWriter
-from codeless_django.writers.apis import APIViewURLWriter
+from codeless_django.writers.urls import URLWriter,APIUrlWriter
+from codeless_django.writers.views import ViewWriter
+from codeless_django.writers.apis import APIViewWriter
 from codeless_django.writers.models import ModelWriter
 from codeless_django.writers.files import PrepareFiles,AdditionalFileWriter
 from codeless_django.writers.base import BaseWriter
 from codeless_django.writers.serializers import ModelSerializerWriter
 from codeless_django.writers.documentation import DocumentationWriter
 from django.conf import settings
 
@@ -19,14 +20,17 @@
         return "INSTALLED_APPS+=["
 
     def get_object_body(self):
         new_apps = "\n"
         for name in self.app_names:
             new_apps+=f"\t \"{name}\", \n"
         return new_apps + "\n]\n"
+    
+    def get_full_string(self):
+        return self.get_object_header()+self.get_object_body()
 
 class IncludeAppUrlToRootUrlWriter(BaseWriter):
 
     def __init__(self,app_names):
         self.app_names=app_names
         self.file_name=settings.ROOT_URLCONF.split(".")[0] + "/urls.py"
     
@@ -40,14 +44,16 @@
     def get_object_body(self):
         app_urls=""
         for name in self.app_names:
             app_urls+=self.get_include_app_url(name)
         
         return app_urls + "\n ]\n"
 
+    def get_full_string(self):
+        return self.get_object_header()+self.get_object_body()
 
 
 
 
 class WriteApps:
     def __init__(self,apps,write_template_views=False,write_api_views=False)-> None:
         self.apps=apps
@@ -65,65 +71,92 @@
     def initiate_app_urls_and_views_files(self):
         for app_name, value in self.apps.items():
             PrepareFiles(app_name,self.write_api_views)
     
     def write_models(self):
         for app_name, value in self.apps.items():
             models = value["models"]
-            for model_name,value in models.items():
-                fields=value["fields"]
-                meta_options=value["meta_options"]
-                ModelWriter(app_name, model_name, fields,meta_options).write_object()
+            ModelWriter(app_name, models).write_object()
     
     def include_app_urls(self):
         app_names=self.local_app_names
         if self.write_api_views or self.write_template_views:
                 IncludeAppUrlToRootUrlWriter(app_names).write_object()
 
     def include_app_to_settings(self):
         app_names=self.local_app_names.copy()    
         if self.write_api_views:
             app_names.append('rest_framework')
         app_names.append('drf_yasg')
 
         NewAppsWriter(app_names).write_object()
     
-    def write_app_views(self,app_name,model_name):
+    def write_app_views(self):
+        if self.write_template_views:
+            for app_name, value in self.apps.items():
+                models = value["models"]
+                ViewWriter(app_name, models).write_object()
+    
+    def write_urls(self):
         if self.write_template_views:
-            ViewURLWriter(app_name, model_name).write_views_and_urls()
+            for app_name, value in self.apps.items():
+                models = value["models"]
+                URLWriter(app_name, models).write_object()
+
+    def write_api_urls(self):
+        if self.write_api_views:
+            
+            for app_name, value in self.apps.items():
+                models = value["models"]
+                APIUrlWriter(app_name, models).write_object()
+            
+    
     
-    def write_serializers(self,app_name,model_name):
+    def write_serializers(self):
         if self.write_api_views:
-            ModelSerializerWriter(app_name, model_name).write_object()
+            for app_name, value in self.apps.items():
+                models = value["models"]
+                ModelSerializerWriter(app_name, models).write_object()
 
-    def write_app_api_views(self,app_name,model_name):
+    def write_app_api_views(self):
         if self.write_api_views:
-            APIViewURLWriter(app_name, model_name).write_api_views_and_urls()
+            for app_name, value in self.apps.items():
+                models = value["models"]
+                APIViewWriter(app_name, models).write_object()
+            
     
     def write(self):
         file_writer = AdditionalFileWriter()
         file_writer.write_gitignore_file()
         self.create_app_folders()
-        self.write_models()
         file_writer.write_new_package_in_requirements_text('drf_yasg', "1.21.5")
         if self.write_api_views:
             file_writer.write_new_package_in_requirements_text('djangorestframework', "3.14.0")
         os.system('pip install -r requirements.txt')
-        os.system("python3 manage.py makemigrations")
-        os.system("python3 manage.py migrate")
+        
+        
         doc_writer=DocumentationWriter()
         doc_writer.write_documentation_url()
         self.initiate_app_urls_and_views_files()
         self.include_app_to_settings()
         self.include_app_urls()
-
         
         for app_name, value in self.apps.items():
-            models = value["models"]
-            for model_name,value in models.items():
-                self.write_app_views(app_name, model_name)
-                self.write_serializers(app_name, model_name)
-                self.write_app_api_views(app_name, model_name)
+            self.write_models()
+            self.write_app_views()
+            self.write_urls()
+            self.write_serializers()
+            self.write_app_api_views()
+            self.write_api_urls()
+
+        os.system("python3 manage.py makemigrations")
+        os.system("python3 manage.py migrate")
+
+
+
+
+
+
```

### Comparing `codeless-django-0.0.13/codeless_django/writers/base.py` & `codeless-django-0.0.14/codeless_django/writers/base.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,44 +1,47 @@
 from abc import ABC, abstractmethod
-class BaseWriter(ABC):
-    
-    def __init__(self,app_name, model_name,file_name):
-        self.model_name = model_name
-        self.app_name=app_name
-        self.file_name=file_name
-    
+
+class BaseBuilder(ABC):
+
     @abstractmethod
     def get_object_header(self):
         pass
 
     @abstractmethod
     def get_object_body(self):
         pass
 
     def get_object_string(self):
         return self.get_object_header() + self.get_object_body() + '\n'
     
+
+
+class BaseWriter(ABC):
+    
+    def __init__(self,file_name):
+        self.file_name=file_name
+    
+
+    
+    
+    def get_full_string(self):
+        pass
+    
     def write_object(self):
         with open(self.file_name,'a') as f:
-            f.write(self.get_object_string()+ "\n\n")
+            f.write(self.get_full_string())
 
 
 class BaseViewWriter(BaseWriter):
 
     def __init__(self,app_name, model_name):
         file_name=f"{app_name}/views.py"
         return super().__init__(app_name, model_name,file_name)
 
-    @abstractmethod
-    def get_object_header(self):
-        pass
 
-    @abstractmethod
-    def get_object_body(self):
-        pass
 
 
 class BaseURLWriter(BaseWriter):
     def __init__(self,app_name, model_name,):
         file_name=f"{app_name}/urls.py"
         return super().__init__(app_name, model_name,file_name)
```

### Comparing `codeless-django-0.0.13/codeless_django/writers/files.py` & `codeless-django-0.0.14/codeless_django/writers/files.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,16 +1,10 @@
 from codeless_django.writers.base import BaseWriter
 import os
 
-import codeless_django
-root_path =  os.path.abspath(codeless_django.__file__).strip('__init__.py')
-gitignore_file_path=os.path.join(root_path, 'additional_files','.gitignore')
-
-
-
 class PrepareFiles:
 
     def __init__(self,app_name,write_api_views=False):
         self.app_name=app_name
         self.write_api_views=write_api_views
         self.write_import_line_to_view_file()
         self.write_import_line_to_url_file()
@@ -34,21 +28,25 @@
         if self.write_api_views:
             import_line="from rest_framework import serializers  \n"
             import_line+=f"from {self.app_name} import models as {self.app_name}_models \n"
             self.write_import_line(file_name,import_line)
 
     def write_import_line_to_url_file(self):
         file_name=f"{self.app_name}/urls.py"
-        import_line="from django.urls import path" + "\n" + f"from {self.app_name} import views"
-        self.write_import_line(file_name,import_line)
+        import_line="from django.urls import path" + "\n" + f"from {self.app_name} import views \n"
+        initial_url_pattern = "urlpatterns = [] \n"
+        text = import_line + initial_url_pattern
+        self.write_import_line(file_name,text)
 
 class RequirementTextWriter:
     def __init__(self):
         self.file_name="requirements.txt"
-        os.system("pip freeze > requirements.txt")
+        with open(self.file_name,'a') as f:
+            f.write(f"django>=2.2.16 \nPillow==9.5.0 \n")
+
     
     def add_new_package(self,package_name,version):
         with open(self.file_name,'a') as f:
             f.write(f"{package_name}=={version}\n")
 
 
 class DotEnvFileWriter:
@@ -62,11 +60,11 @@
 
 class AdditionalFileWriter:
     def __init__(self):
         self.requirement_text_writer = RequirementTextWriter()
 
 
     def write_gitignore_file(self):
-        os.system(f"cp  {gitignore_file_path} .gitignore")
+        os.system("cp codeless_django/additional_files/.gitignore .gitignore")
     
     def write_new_package_in_requirements_text(self,package_name,version):
         self.requirement_text_writer.add_new_package(package_name, version)
```

### Comparing `codeless-django-0.0.13/codeless_django/writers/models.py` & `codeless-django-0.0.14/codeless_django/writers/models.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,17 +1,16 @@
-from codeless_django.writers.base import BaseWriter
+from codeless_django.writers.base import BaseWriter,BaseBuilder
 
-class ModelWriter(BaseWriter):
+class ModelBuilder(BaseBuilder):
 
-    def __init__(self, app_name, model_name, fields,meta_options):
+    def __init__(self,model_name, fields,meta_options):
+        self.model_name=model_name
         self.fields=fields
         self.meta_options=meta_options
-        file_name = f"{app_name}/models.py"
-        super().__init__(app_name, model_name, file_name)
-    
+
     def get_field_options(self,options):
         return ", ".join([f"{opt['name']}={opt['value']}" for opt in options])
     
     def get_field_string(self,field_name,field_type,options):
         field_options=self.get_field_options(options)
         return f"{field_name} = models.{field_type}({field_options})"
 
@@ -31,8 +30,26 @@
         if self.meta_options:
             meta_body="\n\tclass Meta: \n"
             for key,value in self.meta_options.items():
                 meta_body+=f"\t\t{key}={value}\n"
 
             return model_body + meta_body
         else:
-            return model_body
+            return model_body
+
+    def get_object_string(self):
+        return self.get_object_header() + self.get_object_body() + '\n'
+class ModelWriter(BaseWriter):
+
+    def __init__(self, app_name,models):
+        self.models = models
+        file_name = f"{app_name}/models.py"
+        super().__init__(file_name)
+    
+    def get_full_string(self):
+        full_string = ""
+        for model_name,value in self.models.items():
+            fields=value["fields"]
+            meta_options=value["meta_options"]
+            builder = ModelBuilder(model_name,fields, meta_options)
+            full_string+= builder.get_object_string()
+        return full_string
```

### Comparing `codeless-django-0.0.13/codeless_django/writers/views.py` & `codeless-django-0.0.14/codeless_django/writers/apis.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,50 +1,52 @@
-from  codeless_django.writers.base import BaseViewWriter,BaseURLWriter
+from codeless_django.writers.base import BaseBuilder,BaseWriter,BaseURLWriter #BaseViewWriter,BaseURLWriter
 
-class CreateViewWriter(BaseViewWriter):
 
-    def get_object_header(self):
-        return f"class {self.model_name}CreateView(generic.CreateView):\n"
+class BaseAPIViewBuilder(BaseBuilder):
+    def __init__(self,app_name,model_name):
+            self.model_name=model_name
+            self.app_name=app_name
 
     def get_object_body(self):
-        return f"\tmodel = {self.app_name}_models.{self.model_name}\n\tfields = '__all__'\n\tsuccess_url= ' \ \' "
+        return f"\tserializer_class = serializers.{self.model_name}Serializer\n\tqueryset = {self.app_name}_models.{self.model_name}.objects.filter().select_related().prefetch_related()\n\t#authentication_classes=()"
 
 
-class ListViewWriter(BaseViewWriter):
+class ListCreateAPIViewBuilder(BaseAPIViewBuilder):
 
     def get_object_header(self):
-        return f"class {self.model_name}ListView(generic.ListView):\n"
-
-    def get_object_body(self):
-        return f"\tmodel =  {self.app_name}_models.{self.model_name}\n\tpaginate_by = 10 \n"
+        return f"class {self.model_name}ListCreateAPIView(generics.ListCreateAPIView):\n"
 
-
-class DetailViewWriter(BaseViewWriter):
+class RetrieveUpdateDestroyAPIViewBuilder(BaseAPIViewBuilder):
 
     def get_object_header(self):
-        return f"class {self.model_name}DetailView(generic.DetailView):\n"
+        return f"class {self.model_name}RetrieveUpdateDestroyAPIView(generics.RetrieveUpdateDestroyAPIView):\n"
+
+class APIViewWriter(BaseWriter):
+    def __init__(self, app_name,models):
+        self.models = models
+        self.app_name=app_name
+        file_name = f"{app_name}/views.py"
+        super().__init__(file_name)
+    
+    def get_full_string(self):
+        app_name=self.app_name
+        full_string = ""
+        for model_name in self.models.keys():
+            full_string+=ListCreateAPIViewBuilder(app_name, model_name).get_object_string()
+            full_string+=RetrieveUpdateDestroyAPIViewBuilder(app_name, model_name).get_object_string()
+        return full_string
 
-    def get_object_body(self):
-        return f"\tmodel =  {self.app_name}_models.{self.model_name} \n"
 
-class URLWriter(BaseURLWriter):
 
-    def get_url_string(self):
-        url_string = ''
-        url_string += f"    path('{self.model_name.lower()}/list/', views.{self.model_name}ListView.as_view(), name='{self.model_name.lower()}_list'),\n"
-        url_string += f"    path('{self.model_name.lower()}/create/', views.{self.model_name}CreateView.as_view(), name='{self.model_name.lower()}_create'),\n"
-        url_string += f"    path('{self.model_name.lower()}/<int:pk>/', views.{self.model_name}DetailView.as_view(), name='{self.model_name.lower()}_detail'),\n"
-        return url_string
 
-class ViewURLWriter:
+class APIViewURLWriter:
 
     def __init__(self,app_name, model_name):
         self.model_name = model_name
         self.app_name=app_name
     
-    def write_views_and_urls(self):
+    def write_api_views_and_urls(self):
         app_name=self.app_name
         model_name=self.model_name
-        ListViewWriter(app_name, model_name).write_object()
-        CreateViewWriter(app_name, model_name).write_object()
-        DetailViewWriter(app_name, model_name).write_object()
-        URLWriter(app_name, model_name).write_object()
+        ListCreateAPIViewWriter(app_name, model_name).write_object()
+        RetrieveUpdateDestroyAPIViewWriter(app_name, model_name).write_object()
+        APIUrlWriter(app_name, model_name).write_object()
```

### Comparing `codeless-django-0.0.13/codeless_django.egg-info/PKG-INFO` & `codeless-django-0.0.14/codeless_django.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: codeless-django
-Version: 0.0.13
+Version: 0.0.14
 Summary: A Django app to create django apps, models, urls, views , api-views, documentation in a single click
 Home-page: https://www.example.com/
 Author: Omar Faruk
 Author-email: Omar Faruk <omar.iut.09@gmail.com>
 License: BSD-3-Clause  # Example license
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: BSD License
```

### Comparing `codeless-django-0.0.13/pyproject.toml` & `codeless-django-0.0.14/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["hatchling"]
 build-backend = "hatchling.build"
 
 [project]
 name = "codeless-django"
-version = "0.0.13"
+version = "0.0.14"
 authors = [
   { name="Omar Faruk", email="omar.iut.09@gmail.com" },
 ]
 description = "A Django app to create django apps, models, urls, views , api-views, documentation in a single click"
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = [
```

### Comparing `codeless-django-0.0.13/setup.cfg` & `codeless-django-0.0.14/setup.cfg`

 * *Files identical despite different names*

