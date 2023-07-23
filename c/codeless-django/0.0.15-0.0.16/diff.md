# Comparing `tmp/codeless-django-0.0.15.tar.gz` & `tmp/codeless-django-0.0.16.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "codeless-django-0.0.15.tar", last modified: Sun Jul 23 15:06:11 2023, max compression
+gzip compressed data, was "codeless-django-0.0.16.tar", last modified: Sun Jul 23 15:12:03 2023, max compression
```

## Comparing `codeless-django-0.0.15.tar` & `codeless-django-0.0.16.tar`

### file list

```diff
@@ -1,78 +1,78 @@
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:06:11.883810 codeless-django-0.0.15/
--rw-rw-r--   0 omar      (1000) omar      (1000)     1450 2023-04-11 02:03:29.000000 codeless-django-0.0.15/LICENSE
--rw-rw-r--   0 omar      (1000) omar      (1000)      277 2023-07-23 06:49:00.000000 codeless-django-0.0.15/MANIFEST.in
--rw-rw-r--   0 omar      (1000) omar      (1000)     1375 2023-07-23 15:06:11.883810 codeless-django-0.0.15/PKG-INFO
--rw-rw-r--   0 omar      (1000) omar      (1000)      828 2023-04-11 03:07:49.000000 codeless-django-0.0.15/README.md
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:06:11.871810 codeless-django-0.0.15/codeless_django/
--rw-rw-r--   0 omar      (1000) omar      (1000)        0 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/__init__.py
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:06:11.875810 codeless-django-0.0.15/codeless_django/additional_files/
--rw-rw-r--   0 omar      (1000) omar      (1000)     1823 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/additional_files/.gitignore
--rw-rw-r--   0 omar      (1000) omar      (1000)     1623 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/additional_files/root_urls.py
--rw-rw-r--   0 omar      (1000) omar      (1000)      154 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/apps.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     3218 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/data_manager.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     4461 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/fields.json
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:06:11.871810 codeless-django-0.0.15/codeless_django/management/
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:06:11.875810 codeless-django-0.0.15/codeless_django/management/commands/
--rw-rw-r--   0 omar      (1000) omar      (1000)        0 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/management/commands/__init__.py
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:06:11.875810 codeless-django-0.0.15/codeless_django/management/commands/__pycache__/
--rw-rw-r--   0 omar      (1000) omar      (1000)      199 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/management/commands/__pycache__/__init__.cpython-310.pyc
--rw-rw-r--   0 omar      (1000) omar      (1000)     1463 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/management/commands/__pycache__/writeapps.cpython-310.pyc
--rw-rw-r--   0 omar      (1000) omar      (1000)     1144 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/management/commands/writeapps.py
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:06:11.871810 codeless-django-0.0.15/codeless_django/templates/
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:06:11.875810 codeless-django-0.0.15/codeless_django/templates/codeless_django/
--rw-rw-r--   0 omar      (1000) omar      (1000)     2183 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templates/codeless_django/base.html
--rw-rw-r--   0 omar      (1000) omar      (1000)     2922 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templates/codeless_django/demo.html
--rw-rw-r--   0 omar      (1000) omar      (1000)      369 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templates/codeless_django/fields.html
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:06:11.879810 codeless-django-0.0.15/codeless_django/templates/codeless_django/forms/
--rw-rw-r--   0 omar      (1000) omar      (1000)      121 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templates/codeless_django/forms/all_field_types.html
--rw-rw-r--   0 omar      (1000) omar      (1000)      480 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templates/codeless_django/forms/app_form.html
--rw-rw-r--   0 omar      (1000) omar      (1000)      198 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templates/codeless_django/forms/choice_option.html
--rw-rw-r--   0 omar      (1000) omar      (1000)      257 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templates/codeless_django/forms/common_option_form.html
--rw-rw-r--   0 omar      (1000) omar      (1000)      288 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templates/codeless_django/forms/dropdown_option.html
--rw-rw-r--   0 omar      (1000) omar      (1000)      986 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templates/codeless_django/forms/field_form.html
--rw-rw-r--   0 omar      (1000) omar      (1000)      761 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templates/codeless_django/forms/field_option.html
--rw-rw-r--   0 omar      (1000) omar      (1000)      159 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templates/codeless_django/forms/model_form.html
--rw-rw-r--   0 omar      (1000) omar      (1000)     1122 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templates/codeless_django/forms/model_meta_form.html
--rw-rw-r--   0 omar      (1000) omar      (1000)        0 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templates/codeless_django/forms/option_form.html
--rw-rw-r--   0 omar      (1000) omar      (1000)     3437 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templates/codeless_django/home.html
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:06:11.879810 codeless-django-0.0.15/codeless_django/templatetags/
--rw-rw-r--   0 omar      (1000) omar      (1000)        0 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templatetags/__init__.py
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:06:11.879810 codeless-django-0.0.15/codeless_django/templatetags/__pycache__/
--rw-rw-r--   0 omar      (1000) omar      (1000)      192 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templatetags/__pycache__/__init__.cpython-310.pyc
--rw-rw-r--   0 omar      (1000) omar      (1000)      905 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templatetags/__pycache__/codeless_django_tags.cpython-310.pyc
--rw-rw-r--   0 omar      (1000) omar      (1000)      629 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templatetags/codeless_django_tags.py
--rw-rw-r--   0 omar      (1000) omar      (1000)       60 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/tests.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     1065 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/urls.py
--rw-rw-r--   0 omar      (1000) omar      (1000)      227 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/utils.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     3750 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/views.py
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:06:11.879810 codeless-django-0.0.15/codeless_django/writers/
--rw-rw-r--   0 omar      (1000) omar      (1000)        0 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/__init__.py
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:06:11.883810 codeless-django-0.0.15/codeless_django/writers/__pycache__/
--rw-rw-r--   0 omar      (1000) omar      (1000)      187 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/__pycache__/__init__.cpython-310.pyc
--rw-rw-r--   0 omar      (1000) omar      (1000)     2873 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/__pycache__/apis.cpython-310.pyc
--rw-rw-r--   0 omar      (1000) omar      (1000)     6253 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/__pycache__/apps.cpython-310.pyc
--rw-rw-r--   0 omar      (1000) omar      (1000)     2683 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/__pycache__/base.cpython-310.pyc
--rw-rw-r--   0 omar      (1000) omar      (1000)      969 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/__pycache__/documentation.cpython-310.pyc
--rw-rw-r--   0 omar      (1000) omar      (1000)     4013 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/__pycache__/files.cpython-310.pyc
--rw-rw-r--   0 omar      (1000) omar      (1000)     2638 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/__pycache__/models.cpython-310.pyc
--rw-rw-r--   0 omar      (1000) omar      (1000)     1900 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/__pycache__/serializers.cpython-310.pyc
--rw-rw-r--   0 omar      (1000) omar      (1000)     1912 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/__pycache__/urls.cpython-310.pyc
--rw-rw-r--   0 omar      (1000) omar      (1000)     3095 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/__pycache__/views.cpython-310.pyc
--rw-rw-r--   0 omar      (1000) omar      (1000)     1937 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/apis.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     5343 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/apps.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     1248 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/base.py
--rw-rw-r--   0 omar      (1000) omar      (1000)      401 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/documentation.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     2674 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/files.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     1907 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/models.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     1150 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/serializers.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     1933 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/urls.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     2055 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/views.py
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:06:11.875810 codeless-django-0.0.15/codeless_django.egg-info/
--rw-rw-r--   0 omar      (1000) omar      (1000)     1375 2023-07-23 15:06:11.000000 codeless-django-0.0.15/codeless_django.egg-info/PKG-INFO
--rw-rw-r--   0 omar      (1000) omar      (1000)     2855 2023-07-23 15:06:11.000000 codeless-django-0.0.15/codeless_django.egg-info/SOURCES.txt
--rw-rw-r--   0 omar      (1000) omar      (1000)        1 2023-07-23 15:06:11.000000 codeless-django-0.0.15/codeless_django.egg-info/dependency_links.txt
--rw-rw-r--   0 omar      (1000) omar      (1000)       12 2023-07-23 15:06:11.000000 codeless-django-0.0.15/codeless_django.egg-info/requires.txt
--rw-rw-r--   0 omar      (1000) omar      (1000)       16 2023-07-23 15:06:11.000000 codeless-django-0.0.15/codeless_django.egg-info/top_level.txt
--rw-rw-r--   0 omar      (1000) omar      (1000)      528 2023-07-23 15:05:45.000000 codeless-django-0.0.15/pyproject.toml
--rw-rw-r--   0 omar      (1000) omar      (1000)      938 2023-07-23 15:06:11.883810 codeless-django-0.0.15/setup.cfg
--rw-rw-r--   0 omar      (1000) omar      (1000)      139 2023-07-21 14:12:57.000000 codeless-django-0.0.15/setup.py
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:12:03.938649 codeless-django-0.0.16/
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1450 2023-04-11 02:03:29.000000 codeless-django-0.0.16/LICENSE
+-rw-rw-r--   0 omar      (1000) omar      (1000)      277 2023-07-23 06:49:00.000000 codeless-django-0.0.16/MANIFEST.in
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1375 2023-07-23 15:12:03.938649 codeless-django-0.0.16/PKG-INFO
+-rw-rw-r--   0 omar      (1000) omar      (1000)      828 2023-04-11 03:07:49.000000 codeless-django-0.0.16/README.md
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:12:03.926649 codeless-django-0.0.16/codeless_django/
+-rw-rw-r--   0 omar      (1000) omar      (1000)        0 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/__init__.py
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:12:03.930649 codeless-django-0.0.16/codeless_django/additional_files/
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1823 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/additional_files/.gitignore
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1623 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/additional_files/root_urls.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)      154 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/apps.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     3218 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/data_manager.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     4461 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/fields.json
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:12:03.922649 codeless-django-0.0.16/codeless_django/management/
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:12:03.930649 codeless-django-0.0.16/codeless_django/management/commands/
+-rw-rw-r--   0 omar      (1000) omar      (1000)        0 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/management/commands/__init__.py
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:12:03.930649 codeless-django-0.0.16/codeless_django/management/commands/__pycache__/
+-rw-rw-r--   0 omar      (1000) omar      (1000)      199 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/management/commands/__pycache__/__init__.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1463 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/management/commands/__pycache__/writeapps.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1144 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/management/commands/writeapps.py
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:12:03.922649 codeless-django-0.0.16/codeless_django/templates/
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:12:03.930649 codeless-django-0.0.16/codeless_django/templates/codeless_django/
+-rw-rw-r--   0 omar      (1000) omar      (1000)     2183 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/templates/codeless_django/base.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)     2922 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/templates/codeless_django/demo.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)      369 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/templates/codeless_django/fields.html
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:12:03.934649 codeless-django-0.0.16/codeless_django/templates/codeless_django/forms/
+-rw-rw-r--   0 omar      (1000) omar      (1000)      121 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/templates/codeless_django/forms/all_field_types.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)      480 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/templates/codeless_django/forms/app_form.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)      198 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/templates/codeless_django/forms/choice_option.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)      257 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/templates/codeless_django/forms/common_option_form.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)      288 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/templates/codeless_django/forms/dropdown_option.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)      986 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/templates/codeless_django/forms/field_form.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)      761 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/templates/codeless_django/forms/field_option.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)      159 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/templates/codeless_django/forms/model_form.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1122 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/templates/codeless_django/forms/model_meta_form.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)        0 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/templates/codeless_django/forms/option_form.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)     3437 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/templates/codeless_django/home.html
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:12:03.934649 codeless-django-0.0.16/codeless_django/templatetags/
+-rw-rw-r--   0 omar      (1000) omar      (1000)        0 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/templatetags/__init__.py
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:12:03.934649 codeless-django-0.0.16/codeless_django/templatetags/__pycache__/
+-rw-rw-r--   0 omar      (1000) omar      (1000)      192 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/templatetags/__pycache__/__init__.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)      905 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/templatetags/__pycache__/codeless_django_tags.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)      629 2023-07-23 15:10:35.000000 codeless-django-0.0.16/codeless_django/templatetags/codeless_django_tags.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)       60 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/tests.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1065 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/urls.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)      227 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/utils.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     3750 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/views.py
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:12:03.934649 codeless-django-0.0.16/codeless_django/writers/
+-rw-rw-r--   0 omar      (1000) omar      (1000)        0 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/writers/__init__.py
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:12:03.938649 codeless-django-0.0.16/codeless_django/writers/__pycache__/
+-rw-rw-r--   0 omar      (1000) omar      (1000)      187 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/writers/__pycache__/__init__.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     2873 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/writers/__pycache__/apis.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     6253 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/writers/__pycache__/apps.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     2683 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/writers/__pycache__/base.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)      969 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/writers/__pycache__/documentation.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     4013 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/writers/__pycache__/files.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     2638 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/writers/__pycache__/models.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1900 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/writers/__pycache__/serializers.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1912 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/writers/__pycache__/urls.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     3095 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/writers/__pycache__/views.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1937 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/writers/apis.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     5343 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/writers/apps.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1248 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/writers/base.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)      401 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/writers/documentation.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     2674 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/writers/files.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1907 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/writers/models.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1150 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/writers/serializers.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1933 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/writers/urls.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     2055 2023-07-23 15:03:28.000000 codeless-django-0.0.16/codeless_django/writers/views.py
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:12:03.930649 codeless-django-0.0.16/codeless_django.egg-info/
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1375 2023-07-23 15:12:03.000000 codeless-django-0.0.16/codeless_django.egg-info/PKG-INFO
+-rw-rw-r--   0 omar      (1000) omar      (1000)     2855 2023-07-23 15:12:03.000000 codeless-django-0.0.16/codeless_django.egg-info/SOURCES.txt
+-rw-rw-r--   0 omar      (1000) omar      (1000)        1 2023-07-23 15:12:03.000000 codeless-django-0.0.16/codeless_django.egg-info/dependency_links.txt
+-rw-rw-r--   0 omar      (1000) omar      (1000)       12 2023-07-23 15:12:03.000000 codeless-django-0.0.16/codeless_django.egg-info/requires.txt
+-rw-rw-r--   0 omar      (1000) omar      (1000)       16 2023-07-23 15:12:03.000000 codeless-django-0.0.16/codeless_django.egg-info/top_level.txt
+-rw-rw-r--   0 omar      (1000) omar      (1000)      528 2023-07-23 15:11:59.000000 codeless-django-0.0.16/pyproject.toml
+-rw-rw-r--   0 omar      (1000) omar      (1000)      938 2023-07-23 15:12:03.938649 codeless-django-0.0.16/setup.cfg
+-rw-rw-r--   0 omar      (1000) omar      (1000)      139 2023-07-21 14:12:57.000000 codeless-django-0.0.16/setup.py
```

### Comparing `codeless-django-0.0.15/LICENSE` & `codeless-django-0.0.16/LICENSE`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/PKG-INFO` & `codeless-django-0.0.16/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: codeless-django
-Version: 0.0.15
+Version: 0.0.16
 Summary: A Django app to create django apps, models, urls, views , api-views, documentation in a single click
 Home-page: https://www.example.com/
 Author: Omar Faruk
 Author-email: Omar Faruk <omar.iut.09@gmail.com>
 License: BSD-3-Clause  # Example license
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: BSD License
```

### Comparing `codeless-django-0.0.15/README.md` & `codeless-django-0.0.16/README.md`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/additional_files/.gitignore` & `codeless-django-0.0.16/codeless_django/additional_files/.gitignore`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/additional_files/root_urls.py` & `codeless-django-0.0.16/codeless_django/additional_files/root_urls.py`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/data_manager.py` & `codeless-django-0.0.16/codeless_django/data_manager.py`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/fields.json` & `codeless-django-0.0.16/codeless_django/fields.json`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/management/commands/__pycache__/writeapps.cpython-310.pyc` & `codeless-django-0.0.16/codeless_django/management/commands/__pycache__/writeapps.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/management/commands/writeapps.py` & `codeless-django-0.0.16/codeless_django/management/commands/writeapps.py`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/templates/codeless_django/base.html` & `codeless-django-0.0.16/codeless_django/templates/codeless_django/base.html`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/templates/codeless_django/demo.html` & `codeless-django-0.0.16/codeless_django/templates/codeless_django/demo.html`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/templates/codeless_django/forms/field_form.html` & `codeless-django-0.0.16/codeless_django/templates/codeless_django/forms/field_form.html`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/templates/codeless_django/forms/field_option.html` & `codeless-django-0.0.16/codeless_django/templates/codeless_django/forms/field_option.html`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/templates/codeless_django/forms/model_meta_form.html` & `codeless-django-0.0.16/codeless_django/templates/codeless_django/forms/model_meta_form.html`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/templates/codeless_django/home.html` & `codeless-django-0.0.16/codeless_django/templates/codeless_django/home.html`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/templatetags/__pycache__/codeless_django_tags.cpython-310.pyc` & `codeless-django-0.0.16/codeless_django/templatetags/__pycache__/codeless_django_tags.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/templatetags/codeless_django_tags.py` & `codeless-django-0.0.16/codeless_django/templatetags/codeless_django_tags.py`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/urls.py` & `codeless-django-0.0.16/codeless_django/urls.py`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/views.py` & `codeless-django-0.0.16/codeless_django/views.py`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/writers/__pycache__/apis.cpython-310.pyc` & `codeless-django-0.0.16/codeless_django/writers/__pycache__/apis.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/writers/__pycache__/apps.cpython-310.pyc` & `codeless-django-0.0.16/codeless_django/writers/__pycache__/apps.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/writers/__pycache__/base.cpython-310.pyc` & `codeless-django-0.0.16/codeless_django/writers/__pycache__/base.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/writers/__pycache__/documentation.cpython-310.pyc` & `codeless-django-0.0.16/codeless_django/writers/__pycache__/documentation.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/writers/__pycache__/files.cpython-310.pyc` & `codeless-django-0.0.16/codeless_django/writers/__pycache__/files.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/writers/__pycache__/models.cpython-310.pyc` & `codeless-django-0.0.16/codeless_django/writers/__pycache__/models.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/writers/__pycache__/serializers.cpython-310.pyc` & `codeless-django-0.0.16/codeless_django/writers/__pycache__/serializers.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/writers/__pycache__/urls.cpython-310.pyc` & `codeless-django-0.0.16/codeless_django/writers/__pycache__/urls.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/writers/__pycache__/views.cpython-310.pyc` & `codeless-django-0.0.16/codeless_django/writers/__pycache__/views.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/writers/apis.py` & `codeless-django-0.0.16/codeless_django/writers/apis.py`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/writers/apps.py` & `codeless-django-0.0.16/codeless_django/writers/apps.py`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/writers/base.py` & `codeless-django-0.0.16/codeless_django/writers/base.py`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/writers/files.py` & `codeless-django-0.0.16/codeless_django/writers/files.py`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/writers/models.py` & `codeless-django-0.0.16/codeless_django/writers/models.py`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/writers/serializers.py` & `codeless-django-0.0.16/codeless_django/writers/serializers.py`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/writers/urls.py` & `codeless-django-0.0.16/codeless_django/writers/urls.py`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django/writers/views.py` & `codeless-django-0.0.16/codeless_django/writers/views.py`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/codeless_django.egg-info/PKG-INFO` & `codeless-django-0.0.16/codeless_django.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: codeless-django
-Version: 0.0.15
+Version: 0.0.16
 Summary: A Django app to create django apps, models, urls, views , api-views, documentation in a single click
 Home-page: https://www.example.com/
 Author: Omar Faruk
 Author-email: Omar Faruk <omar.iut.09@gmail.com>
 License: BSD-3-Clause  # Example license
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: BSD License
```

### Comparing `codeless-django-0.0.15/codeless_django.egg-info/SOURCES.txt` & `codeless-django-0.0.16/codeless_django.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.15/setup.cfg` & `codeless-django-0.0.16/setup.cfg`

 * *Files identical despite different names*

