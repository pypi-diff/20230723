# Comparing `tmp/codeless-django-0.0.14.tar.gz` & `tmp/codeless-django-0.0.15.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "codeless-django-0.0.14.tar", last modified: Sun Jul 23 06:50:11 2023, max compression
+gzip compressed data, was "codeless-django-0.0.15.tar", last modified: Sun Jul 23 15:06:11 2023, max compression
```

## Comparing `codeless-django-0.0.14.tar` & `codeless-django-0.0.15.tar`

### file list

```diff
@@ -1,77 +1,78 @@
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 06:50:11.444571 codeless-django-0.0.14/
--rw-rw-r--   0 omar      (1000) omar      (1000)     1450 2023-04-11 02:03:29.000000 codeless-django-0.0.14/LICENSE
--rw-rw-r--   0 omar      (1000) omar      (1000)      277 2023-07-23 06:49:00.000000 codeless-django-0.0.14/MANIFEST.in
--rw-rw-r--   0 omar      (1000) omar      (1000)     1375 2023-07-23 06:50:11.444571 codeless-django-0.0.14/PKG-INFO
--rw-rw-r--   0 omar      (1000) omar      (1000)      828 2023-04-11 03:07:49.000000 codeless-django-0.0.14/README.md
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 06:50:11.436571 codeless-django-0.0.14/codeless_django/
--rw-rw-r--   0 omar      (1000) omar      (1000)        0 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/__init__.py
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 06:50:11.436571 codeless-django-0.0.14/codeless_django/additional_files/
--rw-rw-r--   0 omar      (1000) omar      (1000)     1823 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/additional_files/.gitignore
--rw-rw-r--   0 omar      (1000) omar      (1000)     1623 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/additional_files/root_urls.py
--rw-rw-r--   0 omar      (1000) omar      (1000)      154 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/apps.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     3218 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/data_manager.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     4461 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/fields.json
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 06:50:11.432571 codeless-django-0.0.14/codeless_django/management/
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 06:50:11.436571 codeless-django-0.0.14/codeless_django/management/commands/
--rw-rw-r--   0 omar      (1000) omar      (1000)        0 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/management/commands/__init__.py
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 06:50:11.436571 codeless-django-0.0.14/codeless_django/management/commands/__pycache__/
--rw-rw-r--   0 omar      (1000) omar      (1000)      164 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/management/commands/__pycache__/__init__.cpython-310.pyc
--rw-rw-r--   0 omar      (1000) omar      (1000)     1428 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/management/commands/__pycache__/writeapps.cpython-310.pyc
--rw-rw-r--   0 omar      (1000) omar      (1000)     1144 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/management/commands/writeapps.py
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 06:50:11.432571 codeless-django-0.0.14/codeless_django/templates/
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 06:50:11.440571 codeless-django-0.0.14/codeless_django/templates/codeless_django/
--rw-rw-r--   0 omar      (1000) omar      (1000)     2183 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templates/codeless_django/base.html
--rw-rw-r--   0 omar      (1000) omar      (1000)     2922 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templates/codeless_django/demo.html
--rw-rw-r--   0 omar      (1000) omar      (1000)      369 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templates/codeless_django/fields.html
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 06:50:11.440571 codeless-django-0.0.14/codeless_django/templates/codeless_django/forms/
--rw-rw-r--   0 omar      (1000) omar      (1000)      121 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templates/codeless_django/forms/all_field_types.html
--rw-rw-r--   0 omar      (1000) omar      (1000)      480 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templates/codeless_django/forms/app_form.html
--rw-rw-r--   0 omar      (1000) omar      (1000)      198 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templates/codeless_django/forms/choice_option.html
--rw-rw-r--   0 omar      (1000) omar      (1000)      257 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templates/codeless_django/forms/common_option_form.html
--rw-rw-r--   0 omar      (1000) omar      (1000)      288 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templates/codeless_django/forms/dropdown_option.html
--rw-rw-r--   0 omar      (1000) omar      (1000)      986 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templates/codeless_django/forms/field_form.html
--rw-rw-r--   0 omar      (1000) omar      (1000)      761 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templates/codeless_django/forms/field_option.html
--rw-rw-r--   0 omar      (1000) omar      (1000)      159 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templates/codeless_django/forms/model_form.html
--rw-rw-r--   0 omar      (1000) omar      (1000)     1122 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templates/codeless_django/forms/model_meta_form.html
--rw-rw-r--   0 omar      (1000) omar      (1000)        0 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templates/codeless_django/forms/option_form.html
--rw-rw-r--   0 omar      (1000) omar      (1000)     3437 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templates/codeless_django/home.html
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 06:50:11.440571 codeless-django-0.0.14/codeless_django/templatetags/
--rw-rw-r--   0 omar      (1000) omar      (1000)        0 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templatetags/__init__.py
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 06:50:11.440571 codeless-django-0.0.14/codeless_django/templatetags/__pycache__/
--rw-rw-r--   0 omar      (1000) omar      (1000)      157 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templatetags/__pycache__/__init__.cpython-310.pyc
--rw-rw-r--   0 omar      (1000) omar      (1000)      820 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templatetags/__pycache__/codeless_django_tags.cpython-310.pyc
--rw-rw-r--   0 omar      (1000) omar      (1000)      575 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/templatetags/codeless_django_tags.py
--rw-rw-r--   0 omar      (1000) omar      (1000)       60 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/tests.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     1065 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/urls.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     3750 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/views.py
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 06:50:11.444571 codeless-django-0.0.14/codeless_django/writers/
--rw-rw-r--   0 omar      (1000) omar      (1000)        0 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/__init__.py
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 06:50:11.444571 codeless-django-0.0.14/codeless_django/writers/__pycache__/
--rw-rw-r--   0 omar      (1000) omar      (1000)      152 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/__pycache__/__init__.cpython-310.pyc
--rw-rw-r--   0 omar      (1000) omar      (1000)     2838 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/__pycache__/apis.cpython-310.pyc
--rw-rw-r--   0 omar      (1000) omar      (1000)     6218 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/__pycache__/apps.cpython-310.pyc
--rw-rw-r--   0 omar      (1000) omar      (1000)     2648 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/__pycache__/base.cpython-310.pyc
--rw-rw-r--   0 omar      (1000) omar      (1000)      849 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/__pycache__/documentation.cpython-310.pyc
--rw-rw-r--   0 omar      (1000) omar      (1000)     3889 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/__pycache__/files.cpython-310.pyc
--rw-rw-r--   0 omar      (1000) omar      (1000)     2603 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/__pycache__/models.cpython-310.pyc
--rw-rw-r--   0 omar      (1000) omar      (1000)     1865 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/__pycache__/serializers.cpython-310.pyc
--rw-rw-r--   0 omar      (1000) omar      (1000)     1877 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/__pycache__/urls.cpython-310.pyc
--rw-rw-r--   0 omar      (1000) omar      (1000)     3060 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/__pycache__/views.cpython-310.pyc
--rw-rw-r--   0 omar      (1000) omar      (1000)     1937 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/apis.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     5343 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/apps.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     1248 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/base.py
--rw-rw-r--   0 omar      (1000) omar      (1000)      308 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/documentation.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     2580 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/files.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     1907 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/models.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     1150 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/serializers.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     1933 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/urls.py
--rw-rw-r--   0 omar      (1000) omar      (1000)     2055 2023-07-23 06:47:40.000000 codeless-django-0.0.14/codeless_django/writers/views.py
-drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 06:50:11.436571 codeless-django-0.0.14/codeless_django.egg-info/
--rw-rw-r--   0 omar      (1000) omar      (1000)     1375 2023-07-23 06:50:11.000000 codeless-django-0.0.14/codeless_django.egg-info/PKG-INFO
--rw-rw-r--   0 omar      (1000) omar      (1000)     2830 2023-07-23 06:50:11.000000 codeless-django-0.0.14/codeless_django.egg-info/SOURCES.txt
--rw-rw-r--   0 omar      (1000) omar      (1000)        1 2023-07-23 06:50:11.000000 codeless-django-0.0.14/codeless_django.egg-info/dependency_links.txt
--rw-rw-r--   0 omar      (1000) omar      (1000)       12 2023-07-23 06:50:11.000000 codeless-django-0.0.14/codeless_django.egg-info/requires.txt
--rw-rw-r--   0 omar      (1000) omar      (1000)       16 2023-07-23 06:50:11.000000 codeless-django-0.0.14/codeless_django.egg-info/top_level.txt
--rw-rw-r--   0 omar      (1000) omar      (1000)      528 2023-07-23 06:49:31.000000 codeless-django-0.0.14/pyproject.toml
--rw-rw-r--   0 omar      (1000) omar      (1000)      938 2023-07-23 06:50:11.444571 codeless-django-0.0.14/setup.cfg
--rw-rw-r--   0 omar      (1000) omar      (1000)      139 2023-07-21 14:12:57.000000 codeless-django-0.0.14/setup.py
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:06:11.883810 codeless-django-0.0.15/
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1450 2023-04-11 02:03:29.000000 codeless-django-0.0.15/LICENSE
+-rw-rw-r--   0 omar      (1000) omar      (1000)      277 2023-07-23 06:49:00.000000 codeless-django-0.0.15/MANIFEST.in
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1375 2023-07-23 15:06:11.883810 codeless-django-0.0.15/PKG-INFO
+-rw-rw-r--   0 omar      (1000) omar      (1000)      828 2023-04-11 03:07:49.000000 codeless-django-0.0.15/README.md
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:06:11.871810 codeless-django-0.0.15/codeless_django/
+-rw-rw-r--   0 omar      (1000) omar      (1000)        0 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/__init__.py
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:06:11.875810 codeless-django-0.0.15/codeless_django/additional_files/
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1823 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/additional_files/.gitignore
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1623 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/additional_files/root_urls.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)      154 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/apps.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     3218 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/data_manager.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     4461 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/fields.json
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:06:11.871810 codeless-django-0.0.15/codeless_django/management/
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:06:11.875810 codeless-django-0.0.15/codeless_django/management/commands/
+-rw-rw-r--   0 omar      (1000) omar      (1000)        0 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/management/commands/__init__.py
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:06:11.875810 codeless-django-0.0.15/codeless_django/management/commands/__pycache__/
+-rw-rw-r--   0 omar      (1000) omar      (1000)      199 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/management/commands/__pycache__/__init__.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1463 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/management/commands/__pycache__/writeapps.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1144 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/management/commands/writeapps.py
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:06:11.871810 codeless-django-0.0.15/codeless_django/templates/
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:06:11.875810 codeless-django-0.0.15/codeless_django/templates/codeless_django/
+-rw-rw-r--   0 omar      (1000) omar      (1000)     2183 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templates/codeless_django/base.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)     2922 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templates/codeless_django/demo.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)      369 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templates/codeless_django/fields.html
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:06:11.879810 codeless-django-0.0.15/codeless_django/templates/codeless_django/forms/
+-rw-rw-r--   0 omar      (1000) omar      (1000)      121 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templates/codeless_django/forms/all_field_types.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)      480 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templates/codeless_django/forms/app_form.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)      198 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templates/codeless_django/forms/choice_option.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)      257 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templates/codeless_django/forms/common_option_form.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)      288 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templates/codeless_django/forms/dropdown_option.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)      986 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templates/codeless_django/forms/field_form.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)      761 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templates/codeless_django/forms/field_option.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)      159 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templates/codeless_django/forms/model_form.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1122 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templates/codeless_django/forms/model_meta_form.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)        0 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templates/codeless_django/forms/option_form.html
+-rw-rw-r--   0 omar      (1000) omar      (1000)     3437 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templates/codeless_django/home.html
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:06:11.879810 codeless-django-0.0.15/codeless_django/templatetags/
+-rw-rw-r--   0 omar      (1000) omar      (1000)        0 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templatetags/__init__.py
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:06:11.879810 codeless-django-0.0.15/codeless_django/templatetags/__pycache__/
+-rw-rw-r--   0 omar      (1000) omar      (1000)      192 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templatetags/__pycache__/__init__.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)      905 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templatetags/__pycache__/codeless_django_tags.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)      629 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/templatetags/codeless_django_tags.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)       60 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/tests.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1065 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/urls.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)      227 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/utils.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     3750 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/views.py
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:06:11.879810 codeless-django-0.0.15/codeless_django/writers/
+-rw-rw-r--   0 omar      (1000) omar      (1000)        0 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/__init__.py
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:06:11.883810 codeless-django-0.0.15/codeless_django/writers/__pycache__/
+-rw-rw-r--   0 omar      (1000) omar      (1000)      187 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/__pycache__/__init__.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     2873 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/__pycache__/apis.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     6253 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/__pycache__/apps.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     2683 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/__pycache__/base.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)      969 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/__pycache__/documentation.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     4013 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/__pycache__/files.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     2638 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/__pycache__/models.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1900 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/__pycache__/serializers.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1912 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/__pycache__/urls.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     3095 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/__pycache__/views.cpython-310.pyc
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1937 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/apis.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     5343 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/apps.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1248 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/base.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)      401 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/documentation.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     2674 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/files.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1907 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/models.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1150 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/serializers.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1933 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/urls.py
+-rw-rw-r--   0 omar      (1000) omar      (1000)     2055 2023-07-23 15:03:28.000000 codeless-django-0.0.15/codeless_django/writers/views.py
+drwxrwxr-x   0 omar      (1000) omar      (1000)        0 2023-07-23 15:06:11.875810 codeless-django-0.0.15/codeless_django.egg-info/
+-rw-rw-r--   0 omar      (1000) omar      (1000)     1375 2023-07-23 15:06:11.000000 codeless-django-0.0.15/codeless_django.egg-info/PKG-INFO
+-rw-rw-r--   0 omar      (1000) omar      (1000)     2855 2023-07-23 15:06:11.000000 codeless-django-0.0.15/codeless_django.egg-info/SOURCES.txt
+-rw-rw-r--   0 omar      (1000) omar      (1000)        1 2023-07-23 15:06:11.000000 codeless-django-0.0.15/codeless_django.egg-info/dependency_links.txt
+-rw-rw-r--   0 omar      (1000) omar      (1000)       12 2023-07-23 15:06:11.000000 codeless-django-0.0.15/codeless_django.egg-info/requires.txt
+-rw-rw-r--   0 omar      (1000) omar      (1000)       16 2023-07-23 15:06:11.000000 codeless-django-0.0.15/codeless_django.egg-info/top_level.txt
+-rw-rw-r--   0 omar      (1000) omar      (1000)      528 2023-07-23 15:05:45.000000 codeless-django-0.0.15/pyproject.toml
+-rw-rw-r--   0 omar      (1000) omar      (1000)      938 2023-07-23 15:06:11.883810 codeless-django-0.0.15/setup.cfg
+-rw-rw-r--   0 omar      (1000) omar      (1000)      139 2023-07-21 14:12:57.000000 codeless-django-0.0.15/setup.py
```

### Comparing `codeless-django-0.0.14/LICENSE` & `codeless-django-0.0.15/LICENSE`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.14/PKG-INFO` & `codeless-django-0.0.15/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: codeless-django
-Version: 0.0.14
+Version: 0.0.15
 Summary: A Django app to create django apps, models, urls, views , api-views, documentation in a single click
 Home-page: https://www.example.com/
 Author: Omar Faruk
 Author-email: Omar Faruk <omar.iut.09@gmail.com>
 License: BSD-3-Clause  # Example license
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: BSD License
```

### Comparing `codeless-django-0.0.14/README.md` & `codeless-django-0.0.15/README.md`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.14/codeless_django/additional_files/.gitignore` & `codeless-django-0.0.15/codeless_django/additional_files/.gitignore`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.14/codeless_django/additional_files/root_urls.py` & `codeless-django-0.0.15/codeless_django/additional_files/root_urls.py`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.14/codeless_django/data_manager.py` & `codeless-django-0.0.15/codeless_django/data_manager.py`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.14/codeless_django/fields.json` & `codeless-django-0.0.15/codeless_django/fields.json`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.14/codeless_django/management/commands/__pycache__/writeapps.cpython-310.pyc` & `codeless-django-0.0.15/codeless_django/management/commands/__pycache__/writeapps.cpython-310.pyc`

 * *Format-specific differences are supported for Python .pyc files but no file-specific differences were detected; falling back to a binary diff. file(1) reports: Byte-compiled Python module for CPython 3.10, timestamp-based, .py timestamp: Fri Jun  9 00:15:04 2023 UTC, .py size: 1144 bytes*

 * *Could not decompile bytecode: bad marshal data (unknown type code)*

 * *Files 4% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-00000000: 6f0d 0d0a 0000 0000 086f 8264 7804 0000  o........o.dx...
+00000000: 6f0d 0d0a 0000 0000 6f28 bd64 7804 0000  o.......o(.dx...
 00000010: e300 0000 0000 0000 0000 0000 0000 0000  ................
 00000020: 0004 0000 0040 0000 0073 5200 0000 6400  .....@...sR...d.
 00000030: 6401 6c00 6d01 5a01 0100 6400 6402 6c02  d.l.m.Z...d.d.l.
 00000040: 6d03 5a03 0100 6400 6403 6c04 6d05 5a05  m.Z...d.d.l.m.Z.
 00000050: 0100 6400 6404 6c06 6d07 5a07 0100 6505  ..d.d.l.m.Z...e.
 00000060: 8300 5a08 6400 6405 6c09 5a09 4700 6406  ..Z.d.d.l.Z.G.d.
 00000070: 6407 8400 6407 6501 8303 5a0a 6405 5300  d...d.e...Z.d.S.
@@ -25,66 +25,68 @@
 00000180: 5f74 7275 657a 1457 7269 7465 2074 656d  _truez.Write tem
 00000190: 706c 6174 6520 7669 6577 7329 02da 0661  plate views)...a
 000001a0: 6374 696f 6eda 0468 656c 707a 0b2d 2d61  ction..helpz.--a
 000001b0: 7069 2d76 6965 7773 7a0f 5772 6974 6520  pi-viewsz.Write 
 000001c0: 4150 4920 7669 6577 7329 01da 0c61 6464  API views)...add
 000001d0: 5f61 7267 756d 656e 7429 02da 0473 656c  _argument)...sel
 000001e0: 66da 0670 6172 7365 72a9 0072 0d00 0000  f..parser..r....
-000001f0: fa48 2f68 6f6d 652f 6f6d 6172 2f63 6f64  .H/home/omar/cod
-00000200: 652f 5175 6963 6b44 6a2f 636f 6465 6c65  e/QuickDj/codele
-00000210: 7373 5f64 6a61 6e67 6f2f 6d61 6e61 6765  ss_django/manage
-00000220: 6d65 6e74 2f63 6f6d 6d61 6e64 732f 7772  ment/commands/wr
-00000230: 6974 6561 7070 732e 7079 da0d 6164 645f  iteapps.py..add_
-00000240: 6172 6775 6d65 6e74 730c 0000 0073 1400  arguments....s..
-00000250: 0000 0401 0201 0201 0201 06fd 0405 0201  ................
-00000260: 0201 0201 0afd 7a15 436f 6d6d 616e 642e  ......z.Command.
-00000270: 6164 645f 6172 6775 6d65 6e74 7363 0100  add_argumentsc..
-00000280: 0000 0000 0000 0000 0000 0800 0000 0400  ................
-00000290: 0000 4f00 0000 7360 0000 007c 0264 0119  ..O...s`...|.d..
-000002a0: 007d 037c 0264 0219 007d 0474 00a0 01a1  .}.|.d...}.t....
-000002b0: 007d 0574 027c 0564 0319 007c 037c 0483  .}.t.|.d...|.|..
-000002c0: 037d 067c 06a0 03a1 0001 007c 006a 04a0  .}.|.......|.j..
-000002d0: 0364 04a1 0101 0064 057d 077c 006a 04a0  .d.....d.}.|.j..
-000002e0: 0364 067c 079b 009d 02a1 0101 0074 05a0  .d.|.........t..
-000002f0: 0664 07a1 0101 0064 0053 0029 084e da0e  .d.....d.S.).N..
-00000300: 7465 6d70 6c61 7465 5f76 6965 7773 da09  template_views..
-00000310: 6170 695f 7669 6577 73da 0461 7070 737a  api_views..appsz
-00000320: 1157 7269 7469 6e67 206d 6f64 656c 732e  .Writing models.
-00000330: 2e2e 7a1e 2068 7474 703a 2f2f 3132 372e  ..z. http://127.
-00000340: 302e 302e 313a 3830 3030 2f73 7761 6767  0.0.1:8000/swagg
-00000350: 6572 7a14 446f 6375 6d65 6e74 6174 696f  erz.Documentatio
-00000360: 6e20 6c69 6e6b 3a20 7a1f 7079 7468 6f6e  n link: z.python
-00000370: 206d 616e 6167 652e 7079 2072 756e 7365   manage.py runse
-00000380: 7276 6572 2038 3030 3029 07da 0c64 6174  rver 8000)...dat
-00000390: 615f 6d61 6e61 6765 72da 0a5f 6c6f 6164  a_manager.._load
-000003a0: 5f64 6174 6172 0300 0000 da05 7772 6974  _datar......writ
-000003b0: 65da 0673 7464 6f75 74da 026f 73da 0673  e..stdout..os..s
-000003c0: 7973 7465 6d29 0872 0b00 0000 da04 6172  ystem).r......ar
-000003d0: 6773 da07 6f70 7469 6f6e 73da 1477 7269  gs..options..wri
-000003e0: 7465 5f74 656d 706c 6174 655f 7669 6577  te_template_view
-000003f0: 73da 0f77 7269 7465 5f61 7069 5f76 6965  s..write_api_vie
-00000400: 7773 da04 6461 7461 da0a 6170 705f 7772  ws..data..app_wr
-00000410: 6974 6572 da12 646f 6375 6d65 6e74 6174  iter..documentat
-00000420: 696f 6e5f 6c69 6e6b 720d 0000 0072 0d00  ion_linkr....r..
-00000430: 0000 720e 0000 00da 0668 616e 646c 6518  ..r......handle.
-00000440: 0000 0073 1200 0000 0801 0801 0801 1001  ...s............
-00000450: 0801 0c01 0402 1201 0e01 7a0e 436f 6d6d  ..........z.Comm
-00000460: 616e 642e 6861 6e64 6c65 4e29 06da 085f  and.handleN)..._
-00000470: 5f6e 616d 655f 5fda 0a5f 5f6d 6f64 756c  _name__..__modul
-00000480: 655f 5fda 0c5f 5f71 7561 6c6e 616d 655f  e__..__qualname_
-00000490: 5f72 0900 0000 720f 0000 0072 2000 0000  _r....r....r ...
-000004a0: 720d 0000 0072 0d00 0000 720d 0000 0072  r....r....r....r
-000004b0: 0e00 0000 7206 0000 0009 0000 0073 0800  ....r........s..
-000004c0: 0000 0800 0401 0802 0c0c 7206 0000 0029  ..........r....)
-000004d0: 0bda 1b64 6a61 6e67 6f2e 636f 7265 2e6d  ...django.core.m
-000004e0: 616e 6167 656d 656e 742e 6261 7365 7202  anagement.baser.
-000004f0: 0000 00da 1c63 6f64 656c 6573 735f 646a  .....codeless_dj
-00000500: 616e 676f 2e77 7269 7465 7273 2e61 7070  ango.writers.app
-00000510: 7372 0300 0000 da1c 636f 6465 6c65 7373  sr......codeless
-00000520: 5f64 6a61 6e67 6f2e 6461 7461 5f6d 616e  _django.data_man
-00000530: 6167 6572 7204 0000 00da 1064 6a61 6e67  agerr......djang
-00000540: 6f2e 7368 6f72 7463 7574 7372 0500 0000  o.shortcutsr....
-00000550: 7213 0000 0072 1700 0000 7206 0000 0072  r....r....r....r
-00000560: 0d00 0000 720d 0000 0072 0d00 0000 720e  ....r....r....r.
-00000570: 0000 00da 083c 6d6f 6475 6c65 3e01 0000  .....<module>...
-00000580: 0073 0e00 0000 0c00 0c01 0c01 0c01 0601  .s..............
-00000590: 0801 1403                                ....
+000001f0: fa6b 2f68 6f6d 652f 6f6d 6172 2f63 6f64  .k/home/omar/cod
+00000200: 652f 7465 7374 2d63 6c64 2f76 656e 762f  e/test-cld/venv/
+00000210: 6c69 622f 7079 7468 6f6e 332e 3130 2f73  lib/python3.10/s
+00000220: 6974 652d 7061 636b 6167 6573 2f63 6f64  ite-packages/cod
+00000230: 656c 6573 735f 646a 616e 676f 2f6d 616e  eless_django/man
+00000240: 6167 656d 656e 742f 636f 6d6d 616e 6473  agement/commands
+00000250: 2f77 7269 7465 6170 7073 2e70 79da 0d61  /writeapps.py..a
+00000260: 6464 5f61 7267 756d 656e 7473 0c00 0000  dd_arguments....
+00000270: 7314 0000 0004 0102 0102 0102 0106 fd04  s...............
+00000280: 0502 0102 0102 010a fd7a 1543 6f6d 6d61  .........z.Comma
+00000290: 6e64 2e61 6464 5f61 7267 756d 656e 7473  nd.add_arguments
+000002a0: 6301 0000 0000 0000 0000 0000 0008 0000  c...............
+000002b0: 0004 0000 004f 0000 0073 6000 0000 7c02  .....O...s`...|.
+000002c0: 6401 1900 7d03 7c02 6402 1900 7d04 7400  d...}.|.d...}.t.
+000002d0: a001 a100 7d05 7402 7c05 6403 1900 7c03  ....}.t.|.d...|.
+000002e0: 7c04 8303 7d06 7c06 a003 a100 0100 7c00  |...}.|.......|.
+000002f0: 6a04 a003 6404 a101 0100 6405 7d07 7c00  j...d.....d.}.|.
+00000300: 6a04 a003 6406 7c07 9b00 9d02 a101 0100  j...d.|.........
+00000310: 7405 a006 6407 a101 0100 6400 5300 2908  t...d.....d.S.).
+00000320: 4eda 0e74 656d 706c 6174 655f 7669 6577  N..template_view
+00000330: 73da 0961 7069 5f76 6965 7773 da04 6170  s..api_views..ap
+00000340: 7073 7a11 5772 6974 696e 6720 6d6f 6465  psz.Writing mode
+00000350: 6c73 2e2e 2e7a 1e20 6874 7470 3a2f 2f31  ls...z. http://1
+00000360: 3237 2e30 2e30 2e31 3a38 3030 302f 7377  27.0.0.1:8000/sw
+00000370: 6167 6765 727a 1444 6f63 756d 656e 7461  aggerz.Documenta
+00000380: 7469 6f6e 206c 696e 6b3a 207a 1f70 7974  tion link: z.pyt
+00000390: 686f 6e20 6d61 6e61 6765 2e70 7920 7275  hon manage.py ru
+000003a0: 6e73 6572 7665 7220 3830 3030 2907 da0c  nserver 8000)...
+000003b0: 6461 7461 5f6d 616e 6167 6572 da0a 5f6c  data_manager.._l
+000003c0: 6f61 645f 6461 7461 7203 0000 00da 0577  oad_datar......w
+000003d0: 7269 7465 da06 7374 646f 7574 da02 6f73  rite..stdout..os
+000003e0: da06 7379 7374 656d 2908 720b 0000 00da  ..system).r.....
+000003f0: 0461 7267 73da 076f 7074 696f 6e73 da14  .args..options..
+00000400: 7772 6974 655f 7465 6d70 6c61 7465 5f76  write_template_v
+00000410: 6965 7773 da0f 7772 6974 655f 6170 695f  iews..write_api_
+00000420: 7669 6577 73da 0464 6174 61da 0a61 7070  views..data..app
+00000430: 5f77 7269 7465 72da 1264 6f63 756d 656e  _writer..documen
+00000440: 7461 7469 6f6e 5f6c 696e 6b72 0d00 0000  tation_linkr....
+00000450: 720d 0000 0072 0e00 0000 da06 6861 6e64  r....r......hand
+00000460: 6c65 1800 0000 7312 0000 0008 0108 0108  le....s.........
+00000470: 0110 0108 010c 0104 0212 010e 017a 0e43  .............z.C
+00000480: 6f6d 6d61 6e64 2e68 616e 646c 654e 2906  ommand.handleN).
+00000490: da08 5f5f 6e61 6d65 5f5f da0a 5f5f 6d6f  ..__name__..__mo
+000004a0: 6475 6c65 5f5f da0c 5f5f 7175 616c 6e61  dule__..__qualna
+000004b0: 6d65 5f5f 7209 0000 0072 0f00 0000 7220  me__r....r....r 
+000004c0: 0000 0072 0d00 0000 720d 0000 0072 0d00  ...r....r....r..
+000004d0: 0000 720e 0000 0072 0600 0000 0900 0000  ..r....r........
+000004e0: 7308 0000 0008 0004 0108 020c 0c72 0600  s............r..
+000004f0: 0000 290b da1b 646a 616e 676f 2e63 6f72  ..)...django.cor
+00000500: 652e 6d61 6e61 6765 6d65 6e74 2e62 6173  e.management.bas
+00000510: 6572 0200 0000 da1c 636f 6465 6c65 7373  er......codeless
+00000520: 5f64 6a61 6e67 6f2e 7772 6974 6572 732e  _django.writers.
+00000530: 6170 7073 7203 0000 00da 1c63 6f64 656c  appsr......codel
+00000540: 6573 735f 646a 616e 676f 2e64 6174 615f  ess_django.data_
+00000550: 6d61 6e61 6765 7272 0400 0000 da10 646a  managerr......dj
+00000560: 616e 676f 2e73 686f 7274 6375 7473 7205  ango.shortcutsr.
+00000570: 0000 0072 1300 0000 7217 0000 0072 0600  ...r....r....r..
+00000580: 0000 720d 0000 0072 0d00 0000 720d 0000  ..r....r....r...
+00000590: 0072 0e00 0000 da08 3c6d 6f64 756c 653e  .r......<module>
+000005a0: 0100 0000 730e 0000 000c 000c 010c 010c  ....s...........
+000005b0: 0106 0108 0114 03                        .......
```

### Comparing `codeless-django-0.0.14/codeless_django/management/commands/writeapps.py` & `codeless-django-0.0.15/codeless_django/management/commands/writeapps.py`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.14/codeless_django/templates/codeless_django/base.html` & `codeless-django-0.0.15/codeless_django/templates/codeless_django/base.html`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.14/codeless_django/templates/codeless_django/demo.html` & `codeless-django-0.0.15/codeless_django/templates/codeless_django/demo.html`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.14/codeless_django/templates/codeless_django/forms/field_form.html` & `codeless-django-0.0.15/codeless_django/templates/codeless_django/forms/field_form.html`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.14/codeless_django/templates/codeless_django/forms/field_option.html` & `codeless-django-0.0.15/codeless_django/templates/codeless_django/forms/field_option.html`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.14/codeless_django/templates/codeless_django/forms/model_meta_form.html` & `codeless-django-0.0.15/codeless_django/templates/codeless_django/forms/model_meta_form.html`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.14/codeless_django/templates/codeless_django/home.html` & `codeless-django-0.0.15/codeless_django/templates/codeless_django/home.html`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.14/codeless_django/templatetags/__pycache__/codeless_django_tags.cpython-310.pyc` & `codeless-django-0.0.15/codeless_django/templatetags/__pycache__/codeless_django_tags.cpython-310.pyc`

 * *Format-specific differences are supported for Python .pyc files but no file-specific differences were detected; falling back to a binary diff. file(1) reports: Byte-compiled Python module for CPython 3.10, timestamp-based, .py timestamp: Mon Apr 10 18:34:30 2023 UTC, .py size: 575 bytes*

 * *Could not decompile bytecode: bad marshal data (unknown type code)*

 * *Files 16% similar despite different names*

```diff
@@ -1,52 +1,57 @@
-00000000: 6f0d 0d0a 0000 0000 b656 3464 3f02 0000  o........V4d?...
+00000000: 6f0d 0d0a 0000 0000 6f28 bd64 7502 0000  o.......o(.du...
 00000010: e300 0000 0000 0000 0000 0000 0000 0000  ................
-00000020: 0003 0000 0040 0000 0073 4a00 0000 6400  .....@...sJ...d.
+00000020: 0003 0000 0040 0000 0073 5a00 0000 6400  .....@...sZ...d.
 00000030: 6401 6c00 6d01 5a01 0100 6400 6402 6c02  d.l.m.Z...d.d.l.
-00000040: 6d03 5a03 0100 6501 a004 a100 5a05 6503  m.Z...e.....Z.e.
-00000050: 6403 6404 8d01 5a06 6505 6a07 6405 6406  d.d...Z.e.j.d.d.
-00000060: 8400 8301 5a08 6505 6a07 6407 6408 8400  ....Z.e.j.d.d...
-00000070: 8301 5a09 6409 5300 290a e900 0000 0029  ..Z.d.S.)......)
-00000080: 01da 0874 656d 706c 6174 6529 01da 0b44  ...template)...D
-00000090: 6174 614d 616e 6167 6572 7a1b 636f 6465  ataManagerz.code
-000000a0: 6c65 7373 5f64 6a61 6e67 6f2f 6669 656c  less_django/fiel
-000000b0: 6473 2e6a 736f 6e29 01da 0466 696c 6563  ds.json)...filec
-000000c0: 0100 0000 0000 0000 0000 0000 0400 0000  ................
-000000d0: 0400 0000 4300 0000 7328 0000 0074 00a0  ....C...s(...t..
-000000e0: 01a1 007d 017c 01a0 027c 0067 00a1 027d  ...}.|...|.g...}
-000000f0: 027c 01a0 0264 0167 00a1 027d 037c 027c  .|...d.g...}.|.|
-00000100: 0317 0053 00a9 024e da06 436f 6d6d 6f6e  ...S...N..Common
-00000110: 2903 da0c 6461 7461 5f6d 616e 6167 6572  )...data_manager
-00000120: da0a 5f6c 6f61 645f 6461 7461 da03 6765  .._load_data..ge
-00000130: 7429 04da 0576 616c 7565 da06 6669 656c  t)...value..fiel
-00000140: 6473 da0d 6669 656c 645f 6f70 7469 6f6e  ds..field_option
-00000150: 73da 0e63 6f6d 6d6f 6e5f 6f70 7469 6f6e  s..common_option
-00000160: 73a9 0072 0e00 0000 fa4c 2f68 6f6d 652f  s..r.....L/home/
-00000170: 6f6d 6172 2f63 6f64 652f 5175 6963 6b44  omar/code/QuickD
-00000180: 6a2f 636f 6465 6c65 7373 5f64 6a61 6e67  j/codeless_djang
-00000190: 6f2f 7465 6d70 6c61 7465 7461 6773 2f63  o/templatetags/c
-000001a0: 6f64 656c 6573 735f 646a 616e 676f 5f74  odeless_django_t
-000001b0: 6167 732e 7079 da1f 6765 745f 6f70 7469  ags.py..get_opti
-000001c0: 6f6e 735f 7769 7468 5f64 6566 6175 6c74  ons_with_default
-000001d0: 5f76 616c 7565 7307 0000 0073 0800 0000  _values....s....
-000001e0: 0802 0c01 0c01 0801 7210 0000 0063 0100  ........r....c..
-000001f0: 0000 0000 0000 0000 0000 0300 0000 0300  ................
-00000200: 0000 4300 0000 7322 0000 0074 00a0 01a1  ..C...s"...t....
-00000210: 007d 0174 027c 01a0 03a1 0083 017d 027c  .}.t.|.......}.|
-00000220: 02a0 0464 01a1 0101 007c 0253 0072 0500  ...d.....|.S.r..
-00000230: 0000 2905 7207 0000 0072 0800 0000 da04  ..).r....r......
-00000240: 6c69 7374 da04 6b65 7973 da06 7265 6d6f  list..keys..remo
-00000250: 7665 2903 720a 0000 0072 0b00 0000 da0b  ve).r....r......
-00000260: 6669 656c 645f 7479 7065 7372 0e00 0000  field_typesr....
-00000270: 720e 0000 0072 0f00 0000 da0e 6765 745f  r....r......get_
-00000280: 616c 6c5f 6669 656c 6473 0e00 0000 7308  all_fields....s.
-00000290: 0000 0008 020c 010a 0104 0172 1500 0000  ...........r....
-000002a0: 4e29 0ada 0664 6a61 6e67 6f72 0200 0000  N)...djangor....
-000002b0: da1c 636f 6465 6c65 7373 5f64 6a61 6e67  ..codeless_djang
-000002c0: 6f2e 6461 7461 5f6d 616e 6167 6572 7203  o.data_managerr.
-000002d0: 0000 00da 074c 6962 7261 7279 da08 7265  .....Library..re
-000002e0: 6769 7374 6572 7207 0000 00da 0666 696c  gisterr......fil
-000002f0: 7465 7272 1000 0000 7215 0000 0072 0e00  terr....r....r..
-00000300: 0000 720e 0000 0072 0e00 0000 720f 0000  ..r....r....r...
-00000310: 00da 083c 6d6f 6475 6c65 3e01 0000 0073  ...<module>....s
-00000320: 1000 0000 0c00 0c01 0802 0a01 0402 0a01  ................
-00000330: 0406 0e01                                ....
+00000040: 6d03 5a03 0100 6400 6403 6c04 6d05 5a05  m.Z...d.d.l.m.Z.
+00000050: 0100 6501 a006 a100 5a07 6505 6503 6404  ..e.....Z.e.e.d.
+00000060: 8301 6405 8d01 5a08 6507 6a09 6406 6407  ..d...Z.e.j.d.d.
+00000070: 8400 8301 5a0a 6507 6a09 6408 6409 8400  ....Z.e.j.d.d...
+00000080: 8301 5a0b 640a 5300 290b e900 0000 0029  ..Z.d.S.)......)
+00000090: 01da 0874 656d 706c 6174 6529 01da 1067  ...template)...g
+000000a0: 6574 5f6f 735f 6669 6c65 5f70 6174 6829  et_os_file_path)
+000000b0: 01da 0b44 6174 614d 616e 6167 6572 7a0b  ...DataManagerz.
+000000c0: 6669 656c 6473 2e6a 736f 6e29 01da 0466  fields.json)...f
+000000d0: 696c 6563 0100 0000 0000 0000 0000 0000  ilec............
+000000e0: 0400 0000 0400 0000 4300 0000 7328 0000  ........C...s(..
+000000f0: 0074 00a0 01a1 007d 017c 01a0 027c 0067  .t.....}.|...|.g
+00000100: 00a1 027d 027c 01a0 0264 0167 00a1 027d  ...}.|...d.g...}
+00000110: 037c 027c 0317 0053 00a9 024e da06 436f  .|.|...S...N..Co
+00000120: 6d6d 6f6e 2903 da0c 6461 7461 5f6d 616e  mmon)...data_man
+00000130: 6167 6572 da0a 5f6c 6f61 645f 6461 7461  ager.._load_data
+00000140: da03 6765 7429 04da 0576 616c 7565 da06  ..get)...value..
+00000150: 6669 656c 6473 da0d 6669 656c 645f 6f70  fields..field_op
+00000160: 7469 6f6e 73da 0e63 6f6d 6d6f 6e5f 6f70  tions..common_op
+00000170: 7469 6f6e 73a9 0072 0f00 0000 fa6f 2f68  tions..r.....o/h
+00000180: 6f6d 652f 6f6d 6172 2f63 6f64 652f 7465  ome/omar/code/te
+00000190: 7374 2d63 6c64 2f76 656e 762f 6c69 622f  st-cld/venv/lib/
+000001a0: 7079 7468 6f6e 332e 3130 2f73 6974 652d  python3.10/site-
+000001b0: 7061 636b 6167 6573 2f63 6f64 656c 6573  packages/codeles
+000001c0: 735f 646a 616e 676f 2f74 656d 706c 6174  s_django/templat
+000001d0: 6574 6167 732f 636f 6465 6c65 7373 5f64  etags/codeless_d
+000001e0: 6a61 6e67 6f5f 7461 6773 2e70 79da 1f67  jango_tags.py..g
+000001f0: 6574 5f6f 7074 696f 6e73 5f77 6974 685f  et_options_with_
+00000200: 6465 6661 756c 745f 7661 6c75 6573 0900  default_values..
+00000210: 0000 7308 0000 0008 020c 010c 0108 0172  ..s............r
+00000220: 1100 0000 6301 0000 0000 0000 0000 0000  ....c...........
+00000230: 0003 0000 0003 0000 0043 0000 0073 2200  .........C...s".
+00000240: 0000 7400 a001 a100 7d01 7402 7c01 a003  ..t.....}.t.|...
+00000250: a100 8301 7d02 7c02 a004 6401 a101 0100  ....}.|...d.....
+00000260: 7c02 5300 7206 0000 0029 0572 0800 0000  |.S.r....).r....
+00000270: 7209 0000 00da 046c 6973 74da 046b 6579  r......list..key
+00000280: 73da 0672 656d 6f76 6529 0372 0b00 0000  s..remove).r....
+00000290: 720c 0000 00da 0b66 6965 6c64 5f74 7970  r......field_typ
+000002a0: 6573 720f 0000 0072 0f00 0000 7210 0000  esr....r....r...
+000002b0: 00da 0e67 6574 5f61 6c6c 5f66 6965 6c64  ...get_all_field
+000002c0: 7310 0000 0073 0800 0000 0802 0c01 0a01  s....s..........
+000002d0: 0401 7216 0000 004e 290c da06 646a 616e  ..r....N)...djan
+000002e0: 676f 7202 0000 00da 1563 6f64 656c 6573  gor......codeles
+000002f0: 735f 646a 616e 676f 2e75 7469 6c73 7203  s_django.utilsr.
+00000300: 0000 00da 1c63 6f64 656c 6573 735f 646a  .....codeless_dj
+00000310: 616e 676f 2e64 6174 615f 6d61 6e61 6765  ango.data_manage
+00000320: 7272 0400 0000 da07 4c69 6272 6172 79da  rr......Library.
+00000330: 0872 6567 6973 7465 7272 0800 0000 da06  .registerr......
+00000340: 6669 6c74 6572 7211 0000 0072 1600 0000  filterr....r....
+00000350: 720f 0000 0072 0f00 0000 720f 0000 0072  r....r....r....r
+00000360: 1000 0000 da08 3c6d 6f64 756c 653e 0100  ......<module>..
+00000370: 0000 7312 0000 000c 000c 010c 0108 020e  ..s.............
+00000380: 0204 020a 0104 060e 01                   .........
```

### Comparing `codeless-django-0.0.14/codeless_django/templatetags/codeless_django_tags.py` & `codeless-django-0.0.15/codeless_django/templatetags/codeless_django_tags.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,12 +1,14 @@
 from django import template
+from codeless_django.utils import get_os_file_path
 from codeless_django.data_manager import DataManager
 
 register = template.Library()
-data_manager=DataManager(file='codeless_django/fields.json')
+
+data_manager=DataManager(file=get_os_file_path('fields.json'))
 
 @register.filter
 def get_options_with_default_values(value):
     fields = data_manager._load_data()
     field_options= fields.get(value,[])
     common_options=fields.get("Common",[])
     return field_options + common_options
```

### Comparing `codeless-django-0.0.14/codeless_django/urls.py` & `codeless-django-0.0.15/codeless_django/urls.py`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.14/codeless_django/views.py` & `codeless-django-0.0.15/codeless_django/views.py`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.14/codeless_django/writers/__pycache__/apis.cpython-310.pyc` & `codeless-django-0.0.15/codeless_django/writers/__pycache__/apis.cpython-310.pyc`

 * *Format-specific differences are supported for Python .pyc files but no file-specific differences were detected; falling back to a binary diff. file(1) reports: Byte-compiled Python module for CPython 3.10, timestamp-based, .py timestamp: Thu Jun  1 00:43:57 2023 UTC, .py size: 1937 bytes*

 * *Could not decompile bytecode: bad marshal data (unknown type code)*

 * *Files 4% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-00000000: 6f0d 0d0a 0000 0000 cde9 7764 9107 0000  o.........wd....
+00000000: 6f0d 0d0a 0000 0000 6f28 bd64 9107 0000  o.......o(.d....
 00000010: e300 0000 0000 0000 0000 0000 0000 0000  ................
 00000020: 0004 0000 0040 0000 0073 6600 0000 6400  .....@...sf...d.
 00000030: 6401 6c00 6d01 5a01 6d02 5a02 6d03 5a03  d.l.m.Z.m.Z.m.Z.
 00000040: 0100 4700 6402 6403 8400 6403 6501 8303  ..G.d.d...d.e...
 00000050: 5a04 4700 6404 6405 8400 6405 6504 8303  Z.G.d.d...d.e...
 00000060: 5a05 4700 6406 6407 8400 6407 6504 8303  Z.G.d.d...d.e...
 00000070: 5a06 4700 6408 6409 8400 6409 6502 8303  Z.G.d.d...d.e...
@@ -17,162 +17,164 @@
 00000100: 06da 1242 6173 6541 5049 5669 6577 4275  ...BaseAPIViewBu
 00000110: 696c 6465 7263 0300 0000 0000 0000 0000  ilderc..........
 00000120: 0000 0300 0000 0200 0000 4300 0000 f310  ..........C.....
 00000130: 0000 007c 027c 005f 007c 017c 005f 0164  ...|.|._.|.|._.d
 00000140: 0053 00a9 014e a902 da0a 6d6f 6465 6c5f  .S...N....model_
 00000150: 6e61 6d65 da08 6170 705f 6e61 6d65 a903  name..app_name..
 00000160: da04 7365 6c66 720b 0000 0072 0a00 0000  ..selfr....r....
-00000170: a900 720e 0000 00fa 372f 686f 6d65 2f6f  ..r.....7/home/o
-00000180: 6d61 722f 636f 6465 2f51 7569 636b 446a  mar/code/QuickDj
-00000190: 2f63 6f64 656c 6573 735f 646a 616e 676f  /codeless_django
-000001a0: 2f77 7269 7465 7273 2f61 7069 732e 7079  /writers/apis.py
-000001b0: da08 5f5f 696e 6974 5f5f 0500 0000 f304  ..__init__......
-000001c0: 0000 0006 010a 017a 1b42 6173 6541 5049  .......z.BaseAPI
-000001d0: 5669 6577 4275 696c 6465 722e 5f5f 696e  ViewBuilder.__in
-000001e0: 6974 5f5f 6301 0000 0000 0000 0000 0000  it__c...........
-000001f0: 0001 0000 0007 0000 0043 0000 0073 1e00  .........C...s..
-00000200: 0000 6401 7c00 6a00 9b00 6402 7c00 6a01  ..d.|.j...d.|.j.
-00000210: 9b00 6403 7c00 6a00 9b00 6404 9d07 5300  ..d.|.j...d...S.
-00000220: 2905 4e7a 2009 7365 7269 616c 697a 6572  ).Nz .serializer
-00000230: 5f63 6c61 7373 203d 2073 6572 6961 6c69  _class = seriali
-00000240: 7a65 7273 2e7a 1753 6572 6961 6c69 7a65  zers.z.Serialize
-00000250: 720a 0971 7565 7279 7365 7420 3d20 7a08  r..queryset = z.
-00000260: 5f6d 6f64 656c 732e 7a51 2e6f 626a 6563  _models.zQ.objec
-00000270: 7473 2e66 696c 7465 7228 292e 7365 6c65  ts.filter().sele
-00000280: 6374 5f72 656c 6174 6564 2829 2e70 7265  ct_related().pre
-00000290: 6665 7463 685f 7265 6c61 7465 6428 290a  fetch_related().
-000002a0: 0923 6175 7468 656e 7469 6361 7469 6f6e  .#authentication
-000002b0: 5f63 6c61 7373 6573 3d28 2972 0900 0000  _classes=()r....
-000002c0: a901 720d 0000 0072 0e00 0000 720e 0000  ..r....r....r...
-000002d0: 0072 0f00 0000 da0f 6765 745f 6f62 6a65  .r......get_obje
-000002e0: 6374 5f62 6f64 7909 0000 0073 0200 0000  ct_body....s....
-000002f0: 1e01 7a22 4261 7365 4150 4956 6965 7742  ..z"BaseAPIViewB
-00000300: 7569 6c64 6572 2e67 6574 5f6f 626a 6563  uilder.get_objec
-00000310: 745f 626f 6479 4e29 05da 085f 5f6e 616d  t_bodyN)...__nam
-00000320: 655f 5fda 0a5f 5f6d 6f64 756c 655f 5fda  e__..__module__.
-00000330: 0c5f 5f71 7561 6c6e 616d 655f 5f72 1000  .__qualname__r..
-00000340: 0000 7213 0000 0072 0e00 0000 720e 0000  ..r....r....r...
-00000350: 0072 0e00 0000 720f 0000 0072 0600 0000  .r....r....r....
-00000360: 0400 0000 7306 0000 0008 0008 010c 0472  ....s..........r
-00000370: 0600 0000 6300 0000 0000 0000 0000 0000  ....c...........
-00000380: 0000 0000 0002 0000 0040 0000 00f3 1400  .........@......
-00000390: 0000 6500 5a01 6400 5a02 6401 6402 8400  ..e.Z.d.Z.d.d...
-000003a0: 5a03 6403 5300 2904 da18 4c69 7374 4372  Z.d.S.)...ListCr
-000003b0: 6561 7465 4150 4956 6965 7742 7569 6c64  eateAPIViewBuild
-000003c0: 6572 6301 0000 0000 0000 0000 0000 0001  erc.............
-000003d0: 0000 0003 0000 0043 0000 00f3 0e00 0000  .......C........
-000003e0: 6401 7c00 6a00 9b00 6402 9d03 5300 2903  d.|.j...d...S.).
-000003f0: 4efa 0663 6c61 7373 207a 2f4c 6973 7443  N..class z/ListC
-00000400: 7265 6174 6541 5049 5669 6577 2867 656e  reateAPIView(gen
-00000410: 6572 6963 732e 4c69 7374 4372 6561 7465  erics.ListCreate
-00000420: 4150 4956 6965 7729 3a0a a901 720a 0000  APIView):...r...
-00000430: 0072 1200 0000 720e 0000 0072 0e00 0000  .r....r....r....
-00000440: 720f 0000 00da 1167 6574 5f6f 626a 6563  r......get_objec
-00000450: 745f 6865 6164 6572 0f00 0000 f302 0000  t_header........
-00000460: 000e 017a 2a4c 6973 7443 7265 6174 6541  ...z*ListCreateA
-00000470: 5049 5669 6577 4275 696c 6465 722e 6765  PIViewBuilder.ge
-00000480: 745f 6f62 6a65 6374 5f68 6561 6465 724e  t_object_headerN
-00000490: a904 7214 0000 0072 1500 0000 7216 0000  ..r....r....r...
-000004a0: 0072 1c00 0000 720e 0000 0072 0e00 0000  .r....r....r....
-000004b0: 720e 0000 0072 0f00 0000 7218 0000 000d  r....r....r.....
-000004c0: 0000 00f3 0400 0000 0800 0c02 7218 0000  ............r...
-000004d0: 0063 0000 0000 0000 0000 0000 0000 0000  .c..............
-000004e0: 0000 0200 0000 4000 0000 7217 0000 0029  ......@...r....)
-000004f0: 04da 2352 6574 7269 6576 6555 7064 6174  ..#RetrieveUpdat
-00000500: 6544 6573 7472 6f79 4150 4956 6965 7742  eDestroyAPIViewB
-00000510: 7569 6c64 6572 6301 0000 0000 0000 0000  uilderc.........
-00000520: 0000 0001 0000 0003 0000 0043 0000 0072  ...........C...r
-00000530: 1900 0000 2903 4e72 1a00 0000 7a45 5265  ....).Nr....zERe
-00000540: 7472 6965 7665 5570 6461 7465 4465 7374  trieveUpdateDest
-00000550: 726f 7941 5049 5669 6577 2867 656e 6572  royAPIView(gener
-00000560: 6963 732e 5265 7472 6965 7665 5570 6461  ics.RetrieveUpda
-00000570: 7465 4465 7374 726f 7941 5049 5669 6577  teDestroyAPIView
-00000580: 293a 0a72 1b00 0000 7212 0000 0072 0e00  ):.r....r....r..
-00000590: 0000 720e 0000 0072 0f00 0000 721c 0000  ..r....r....r...
-000005a0: 0014 0000 0072 1d00 0000 7a35 5265 7472  .....r....z5Retr
-000005b0: 6965 7665 5570 6461 7465 4465 7374 726f  ieveUpdateDestro
-000005c0: 7941 5049 5669 6577 4275 696c 6465 722e  yAPIViewBuilder.
-000005d0: 6765 745f 6f62 6a65 6374 5f68 6561 6465  get_object_heade
-000005e0: 724e 721e 0000 0072 0e00 0000 720e 0000  rNr....r....r...
-000005f0: 0072 0e00 0000 720f 0000 0072 2000 0000  .r....r....r ...
-00000600: 1200 0000 721f 0000 0072 2000 0000 6300  ....r....r ...c.
-00000610: 0000 0000 0000 0000 0000 0000 0000 0003  ................
-00000620: 0000 0000 0000 0073 2400 0000 6500 5a01  .......s$...e.Z.
-00000630: 6400 5a02 8700 6601 6401 6402 8408 5a03  d.Z...f.d.d...Z.
-00000640: 6403 6404 8400 5a04 8700 0400 5a05 5300  d.d...Z.....Z.S.
-00000650: 2905 da0d 4150 4956 6965 7757 7269 7465  )...APIViewWrite
-00000660: 7263 0300 0000 0000 0000 0000 0000 0400  rc..............
-00000670: 0000 0300 0000 0300 0000 7326 0000 007c  ..........s&...|
-00000680: 027c 005f 007c 017c 005f 017c 019b 0064  .|._.|.|._.|...d
-00000690: 019d 027d 0374 0283 00a0 037c 03a1 0101  ...}.t.....|....
-000006a0: 0064 0053 0029 024e 7a09 2f76 6965 7773  .d.S.).Nz./views
-000006b0: 2e70 7929 04da 066d 6f64 656c 7372 0b00  .py)...modelsr..
-000006c0: 0000 da05 7375 7065 7272 1000 0000 2904  ....superr....).
-000006d0: 720d 0000 0072 0b00 0000 7222 0000 00da  r....r....r"....
-000006e0: 0966 696c 655f 6e61 6d65 a901 da09 5f5f  .file_name....__
-000006f0: 636c 6173 735f 5f72 0e00 0000 720f 0000  class__r....r...
-00000700: 0072 1000 0000 1800 0000 7308 0000 0006  .r........s.....
-00000710: 0106 010a 0110 017a 1641 5049 5669 6577  .......z.APIView
-00000720: 5772 6974 6572 2e5f 5f69 6e69 745f 5f63  Writer.__init__c
-00000730: 0100 0000 0000 0000 0000 0000 0400 0000  ................
-00000740: 0500 0000 4300 0000 7342 0000 007c 006a  ....C...sB...|.j
-00000750: 007d 0164 017d 027c 006a 01a0 02a1 0044  .}.d.}.|.j.....D
-00000760: 005d 147d 037c 0274 037c 017c 0383 02a0  .].}.|.t.|.|....
-00000770: 04a1 0037 007d 027c 0274 057c 017c 0383  ...7.}.|.t.|.|..
-00000780: 02a0 04a1 0037 007d 0271 0a7c 0253 0029  .....7.}.q.|.S.)
-00000790: 024e da00 2906 720b 0000 0072 2200 0000  .N..).r....r"...
-000007a0: da04 6b65 7973 7218 0000 00da 1167 6574  ..keysr......get
-000007b0: 5f6f 626a 6563 745f 7374 7269 6e67 7220  _object_stringr 
-000007c0: 0000 0029 0472 0d00 0000 720b 0000 00da  ...).r....r.....
-000007d0: 0b66 756c 6c5f 7374 7269 6e67 720a 0000  .full_stringr...
-000007e0: 0072 0e00 0000 720e 0000 0072 0f00 0000  .r....r....r....
-000007f0: da0f 6765 745f 6675 6c6c 5f73 7472 696e  ..get_full_strin
-00000800: 671e 0000 0073 0c00 0000 0601 0401 0e01  g....s..........
-00000810: 1201 1401 0401 7a1d 4150 4956 6965 7757  ......z.APIViewW
-00000820: 7269 7465 722e 6765 745f 6675 6c6c 5f73  riter.get_full_s
-00000830: 7472 696e 6729 0672 1400 0000 7215 0000  tring).r....r...
-00000840: 0072 1600 0000 7210 0000 0072 2b00 0000  .r....r....r+...
-00000850: da0d 5f5f 636c 6173 7363 656c 6c5f 5f72  ..__classcell__r
-00000860: 0e00 0000 720e 0000 0072 2500 0000 720f  ....r....r%...r.
-00000870: 0000 0072 2100 0000 1700 0000 7306 0000  ...r!.......s...
-00000880: 0008 000c 0110 0672 2100 0000 6300 0000  .......r!...c...
-00000890: 0000 0000 0000 0000 0000 0000 0002 0000  ................
-000008a0: 0040 0000 0072 0500 0000 2906 da10 4150  .@...r....)...AP
-000008b0: 4956 6965 7755 524c 5772 6974 6572 6303  IViewURLWriterc.
-000008c0: 0000 0000 0000 0000 0000 0003 0000 0002  ................
-000008d0: 0000 0043 0000 0072 0700 0000 7208 0000  ...C...r....r...
-000008e0: 0072 0900 0000 720c 0000 0072 0e00 0000  .r....r....r....
-000008f0: 720e 0000 0072 0f00 0000 7210 0000 002b  r....r....r....+
-00000900: 0000 0072 1100 0000 7a19 4150 4956 6965  ...r....z.APIVie
-00000910: 7755 524c 5772 6974 6572 2e5f 5f69 6e69  wURLWriter.__ini
-00000920: 745f 5f63 0100 0000 0000 0000 0000 0000  t__c............
-00000930: 0300 0000 0300 0000 4300 0000 733a 0000  ........C...s:..
-00000940: 007c 006a 007d 017c 006a 017d 0274 027c  .|.j.}.|.j.}.t.|
-00000950: 017c 0283 02a0 03a1 0001 0074 047c 017c  .|.........t.|.|
-00000960: 0283 02a0 03a1 0001 0074 057c 017c 0283  .........t.|.|..
-00000970: 02a0 03a1 0001 0064 0053 0072 0800 0000  .......d.S.r....
-00000980: 2906 720b 0000 0072 0a00 0000 da17 4c69  ).r....r......Li
-00000990: 7374 4372 6561 7465 4150 4956 6965 7757  stCreateAPIViewW
-000009a0: 7269 7465 72da 0c77 7269 7465 5f6f 626a  riter..write_obj
-000009b0: 6563 74da 2252 6574 7269 6576 6555 7064  ect."RetrieveUpd
-000009c0: 6174 6544 6573 7472 6f79 4150 4956 6965  ateDestroyAPIVie
-000009d0: 7757 7269 7465 72da 0c41 5049 5572 6c57  wWriter..APIUrlW
-000009e0: 7269 7465 7272 0c00 0000 720e 0000 0072  riterr....r....r
-000009f0: 0e00 0000 720f 0000 00da 1877 7269 7465  ....r......write
-00000a00: 5f61 7069 5f76 6965 7773 5f61 6e64 5f75  _api_views_and_u
-00000a10: 726c 732f 0000 0073 0a00 0000 0601 0601  rls/...s........
-00000a20: 0e01 0e01 1201 7a29 4150 4956 6965 7755  ......z)APIViewU
-00000a30: 524c 5772 6974 6572 2e77 7269 7465 5f61  RLWriter.write_a
-00000a40: 7069 5f76 6965 7773 5f61 6e64 5f75 726c  pi_views_and_url
-00000a50: 734e 2905 7214 0000 0072 1500 0000 7216  sN).r....r....r.
-00000a60: 0000 0072 1000 0000 7232 0000 0072 0e00  ...r....r2...r..
-00000a70: 0000 720e 0000 0072 0e00 0000 720f 0000  ..r....r....r...
-00000a80: 0072 2d00 0000 2900 0000 7306 0000 0008  .r-...)...s.....
-00000a90: 0008 020c 0472 2d00 0000 4e29 09da 1c63  .....r-...N)...c
-00000aa0: 6f64 656c 6573 735f 646a 616e 676f 2e77  odeless_django.w
-00000ab0: 7269 7465 7273 2e62 6173 6572 0200 0000  riters.baser....
-00000ac0: 7203 0000 0072 0400 0000 7206 0000 0072  r....r....r....r
-00000ad0: 1800 0000 7220 0000 0072 2100 0000 722d  ....r ...r!...r-
-00000ae0: 0000 0072 0e00 0000 720e 0000 0072 0e00  ...r....r....r..
-00000af0: 0000 720f 0000 00da 083c 6d6f 6475 6c65  ..r......<module
-00000b00: 3e01 0000 0073 0c00 0000 1400 1003 1009  >....s..........
-00000b10: 1005 1005 1212                           ......
+00000170: a900 720e 0000 00fa 5a2f 686f 6d65 2f6f  ..r.....Z/home/o
+00000180: 6d61 722f 636f 6465 2f74 6573 742d 636c  mar/code/test-cl
+00000190: 642f 7665 6e76 2f6c 6962 2f70 7974 686f  d/venv/lib/pytho
+000001a0: 6e33 2e31 302f 7369 7465 2d70 6163 6b61  n3.10/site-packa
+000001b0: 6765 732f 636f 6465 6c65 7373 5f64 6a61  ges/codeless_dja
+000001c0: 6e67 6f2f 7772 6974 6572 732f 6170 6973  ngo/writers/apis
+000001d0: 2e70 79da 085f 5f69 6e69 745f 5f05 0000  .py..__init__...
+000001e0: 00f3 0400 0000 0601 0a01 7a1b 4261 7365  ..........z.Base
+000001f0: 4150 4956 6965 7742 7569 6c64 6572 2e5f  APIViewBuilder._
+00000200: 5f69 6e69 745f 5f63 0100 0000 0000 0000  _init__c........
+00000210: 0000 0000 0100 0000 0700 0000 4300 0000  ............C...
+00000220: 731e 0000 0064 017c 006a 009b 0064 027c  s....d.|.j...d.|
+00000230: 006a 019b 0064 037c 006a 009b 0064 049d  .j...d.|.j...d..
+00000240: 0753 0029 054e 7a20 0973 6572 6961 6c69  .S.).Nz .seriali
+00000250: 7a65 725f 636c 6173 7320 3d20 7365 7269  zer_class = seri
+00000260: 616c 697a 6572 732e 7a17 5365 7269 616c  alizers.z.Serial
+00000270: 697a 6572 0a09 7175 6572 7973 6574 203d  izer..queryset =
+00000280: 207a 085f 6d6f 6465 6c73 2e7a 512e 6f62   z._models.zQ.ob
+00000290: 6a65 6374 732e 6669 6c74 6572 2829 2e73  jects.filter().s
+000002a0: 656c 6563 745f 7265 6c61 7465 6428 292e  elect_related().
+000002b0: 7072 6566 6574 6368 5f72 656c 6174 6564  prefetch_related
+000002c0: 2829 0a09 2361 7574 6865 6e74 6963 6174  ()..#authenticat
+000002d0: 696f 6e5f 636c 6173 7365 733d 2829 7209  ion_classes=()r.
+000002e0: 0000 00a9 0172 0d00 0000 720e 0000 0072  .....r....r....r
+000002f0: 0e00 0000 720f 0000 00da 0f67 6574 5f6f  ....r......get_o
+00000300: 626a 6563 745f 626f 6479 0900 0000 7302  bject_body....s.
+00000310: 0000 001e 017a 2242 6173 6541 5049 5669  .....z"BaseAPIVi
+00000320: 6577 4275 696c 6465 722e 6765 745f 6f62  ewBuilder.get_ob
+00000330: 6a65 6374 5f62 6f64 794e 2905 da08 5f5f  ject_bodyN)...__
+00000340: 6e61 6d65 5f5f da0a 5f5f 6d6f 6475 6c65  name__..__module
+00000350: 5f5f da0c 5f5f 7175 616c 6e61 6d65 5f5f  __..__qualname__
+00000360: 7210 0000 0072 1300 0000 720e 0000 0072  r....r....r....r
+00000370: 0e00 0000 720e 0000 0072 0f00 0000 7206  ....r....r....r.
+00000380: 0000 0004 0000 0073 0600 0000 0800 0801  .......s........
+00000390: 0c04 7206 0000 0063 0000 0000 0000 0000  ..r....c........
+000003a0: 0000 0000 0000 0000 0200 0000 4000 0000  ............@...
+000003b0: f314 0000 0065 005a 0164 005a 0264 0164  .....e.Z.d.Z.d.d
+000003c0: 0284 005a 0364 0353 0029 04da 184c 6973  ...Z.d.S.)...Lis
+000003d0: 7443 7265 6174 6541 5049 5669 6577 4275  tCreateAPIViewBu
+000003e0: 696c 6465 7263 0100 0000 0000 0000 0000  ilderc..........
+000003f0: 0000 0100 0000 0300 0000 4300 0000 f30e  ..........C.....
+00000400: 0000 0064 017c 006a 009b 0064 029d 0353  ...d.|.j...d...S
+00000410: 0029 034e fa06 636c 6173 7320 7a2f 4c69  .).N..class z/Li
+00000420: 7374 4372 6561 7465 4150 4956 6965 7728  stCreateAPIView(
+00000430: 6765 6e65 7269 6373 2e4c 6973 7443 7265  generics.ListCre
+00000440: 6174 6541 5049 5669 6577 293a 0aa9 0172  ateAPIView):...r
+00000450: 0a00 0000 7212 0000 0072 0e00 0000 720e  ....r....r....r.
+00000460: 0000 0072 0f00 0000 da11 6765 745f 6f62  ...r......get_ob
+00000470: 6a65 6374 5f68 6561 6465 720f 0000 00f3  ject_header.....
+00000480: 0200 0000 0e01 7a2a 4c69 7374 4372 6561  ......z*ListCrea
+00000490: 7465 4150 4956 6965 7742 7569 6c64 6572  teAPIViewBuilder
+000004a0: 2e67 6574 5f6f 626a 6563 745f 6865 6164  .get_object_head
+000004b0: 6572 4ea9 0472 1400 0000 7215 0000 0072  erN..r....r....r
+000004c0: 1600 0000 721c 0000 0072 0e00 0000 720e  ....r....r....r.
+000004d0: 0000 0072 0e00 0000 720f 0000 0072 1800  ...r....r....r..
+000004e0: 0000 0d00 0000 f304 0000 0008 000c 0272  ...............r
+000004f0: 1800 0000 6300 0000 0000 0000 0000 0000  ....c...........
+00000500: 0000 0000 0002 0000 0040 0000 0072 1700  .........@...r..
+00000510: 0000 2904 da23 5265 7472 6965 7665 5570  ..)..#RetrieveUp
+00000520: 6461 7465 4465 7374 726f 7941 5049 5669  dateDestroyAPIVi
+00000530: 6577 4275 696c 6465 7263 0100 0000 0000  ewBuilderc......
+00000540: 0000 0000 0000 0100 0000 0300 0000 4300  ..............C.
+00000550: 0000 7219 0000 0029 034e 721a 0000 007a  ..r....).Nr....z
+00000560: 4552 6574 7269 6576 6555 7064 6174 6544  ERetrieveUpdateD
+00000570: 6573 7472 6f79 4150 4956 6965 7728 6765  estroyAPIView(ge
+00000580: 6e65 7269 6373 2e52 6574 7269 6576 6555  nerics.RetrieveU
+00000590: 7064 6174 6544 6573 7472 6f79 4150 4956  pdateDestroyAPIV
+000005a0: 6965 7729 3a0a 721b 0000 0072 1200 0000  iew):.r....r....
+000005b0: 720e 0000 0072 0e00 0000 720f 0000 0072  r....r....r....r
+000005c0: 1c00 0000 1400 0000 721d 0000 007a 3552  ........r....z5R
+000005d0: 6574 7269 6576 6555 7064 6174 6544 6573  etrieveUpdateDes
+000005e0: 7472 6f79 4150 4956 6965 7742 7569 6c64  troyAPIViewBuild
+000005f0: 6572 2e67 6574 5f6f 626a 6563 745f 6865  er.get_object_he
+00000600: 6164 6572 4e72 1e00 0000 720e 0000 0072  aderNr....r....r
+00000610: 0e00 0000 720e 0000 0072 0f00 0000 7220  ....r....r....r 
+00000620: 0000 0012 0000 0072 1f00 0000 7220 0000  .......r....r ..
+00000630: 0063 0000 0000 0000 0000 0000 0000 0000  .c..............
+00000640: 0000 0300 0000 0000 0000 7324 0000 0065  ..........s$...e
+00000650: 005a 0164 005a 0287 0066 0164 0164 0284  .Z.d.Z...f.d.d..
+00000660: 085a 0364 0364 0484 005a 0487 0004 005a  .Z.d.d...Z.....Z
+00000670: 0553 0029 05da 0d41 5049 5669 6577 5772  .S.)...APIViewWr
+00000680: 6974 6572 6303 0000 0000 0000 0000 0000  iterc...........
+00000690: 0004 0000 0003 0000 0003 0000 0073 2600  .............s&.
+000006a0: 0000 7c02 7c00 5f00 7c01 7c00 5f01 7c01  ..|.|._.|.|._.|.
+000006b0: 9b00 6401 9d02 7d03 7402 8300 a003 7c03  ..d...}.t.....|.
+000006c0: a101 0100 6400 5300 2902 4e7a 092f 7669  ....d.S.).Nz./vi
+000006d0: 6577 732e 7079 2904 da06 6d6f 6465 6c73  ews.py)...models
+000006e0: 720b 0000 00da 0573 7570 6572 7210 0000  r......superr...
+000006f0: 0029 0472 0d00 0000 720b 0000 0072 2200  .).r....r....r".
+00000700: 0000 da09 6669 6c65 5f6e 616d 65a9 01da  ....file_name...
+00000710: 095f 5f63 6c61 7373 5f5f 720e 0000 0072  .__class__r....r
+00000720: 0f00 0000 7210 0000 0018 0000 0073 0800  ....r........s..
+00000730: 0000 0601 0601 0a01 1001 7a16 4150 4956  ..........z.APIV
+00000740: 6965 7757 7269 7465 722e 5f5f 696e 6974  iewWriter.__init
+00000750: 5f5f 6301 0000 0000 0000 0000 0000 0004  __c.............
+00000760: 0000 0005 0000 0043 0000 0073 4200 0000  .......C...sB...
+00000770: 7c00 6a00 7d01 6401 7d02 7c00 6a01 a002  |.j.}.d.}.|.j...
+00000780: a100 4400 5d14 7d03 7c02 7403 7c01 7c03  ..D.].}.|.t.|.|.
+00000790: 8302 a004 a100 3700 7d02 7c02 7405 7c01  ......7.}.|.t.|.
+000007a0: 7c03 8302 a004 a100 3700 7d02 710a 7c02  |.......7.}.q.|.
+000007b0: 5300 2902 4eda 0029 0672 0b00 0000 7222  S.).N..).r....r"
+000007c0: 0000 00da 046b 6579 7372 1800 0000 da11  .....keysr......
+000007d0: 6765 745f 6f62 6a65 6374 5f73 7472 696e  get_object_strin
+000007e0: 6772 2000 0000 2904 720d 0000 0072 0b00  gr ...).r....r..
+000007f0: 0000 da0b 6675 6c6c 5f73 7472 696e 6772  ....full_stringr
+00000800: 0a00 0000 720e 0000 0072 0e00 0000 720f  ....r....r....r.
+00000810: 0000 00da 0f67 6574 5f66 756c 6c5f 7374  .....get_full_st
+00000820: 7269 6e67 1e00 0000 730c 0000 0006 0104  ring....s.......
+00000830: 010e 0112 0114 0104 017a 1d41 5049 5669  .........z.APIVi
+00000840: 6577 5772 6974 6572 2e67 6574 5f66 756c  ewWriter.get_ful
+00000850: 6c5f 7374 7269 6e67 2906 7214 0000 0072  l_string).r....r
+00000860: 1500 0000 7216 0000 0072 1000 0000 722b  ....r....r....r+
+00000870: 0000 00da 0d5f 5f63 6c61 7373 6365 6c6c  .....__classcell
+00000880: 5f5f 720e 0000 0072 0e00 0000 7225 0000  __r....r....r%..
+00000890: 0072 0f00 0000 7221 0000 0017 0000 0073  .r....r!.......s
+000008a0: 0600 0000 0800 0c01 1006 7221 0000 0063  ..........r!...c
+000008b0: 0000 0000 0000 0000 0000 0000 0000 0000  ................
+000008c0: 0200 0000 4000 0000 7205 0000 0029 06da  ....@...r....)..
+000008d0: 1041 5049 5669 6577 5552 4c57 7269 7465  .APIViewURLWrite
+000008e0: 7263 0300 0000 0000 0000 0000 0000 0300  rc..............
+000008f0: 0000 0200 0000 4300 0000 7207 0000 0072  ......C...r....r
+00000900: 0800 0000 7209 0000 0072 0c00 0000 720e  ....r....r....r.
+00000910: 0000 0072 0e00 0000 720f 0000 0072 1000  ...r....r....r..
+00000920: 0000 2b00 0000 7211 0000 007a 1941 5049  ..+...r....z.API
+00000930: 5669 6577 5552 4c57 7269 7465 722e 5f5f  ViewURLWriter.__
+00000940: 696e 6974 5f5f 6301 0000 0000 0000 0000  init__c.........
+00000950: 0000 0003 0000 0003 0000 0043 0000 0073  ...........C...s
+00000960: 3a00 0000 7c00 6a00 7d01 7c00 6a01 7d02  :...|.j.}.|.j.}.
+00000970: 7402 7c01 7c02 8302 a003 a100 0100 7404  t.|.|.........t.
+00000980: 7c01 7c02 8302 a003 a100 0100 7405 7c01  |.|.........t.|.
+00000990: 7c02 8302 a003 a100 0100 6400 5300 7208  |.........d.S.r.
+000009a0: 0000 0029 0672 0b00 0000 720a 0000 00da  ...).r....r.....
+000009b0: 174c 6973 7443 7265 6174 6541 5049 5669  .ListCreateAPIVi
+000009c0: 6577 5772 6974 6572 da0c 7772 6974 655f  ewWriter..write_
+000009d0: 6f62 6a65 6374 da22 5265 7472 6965 7665  object."Retrieve
+000009e0: 5570 6461 7465 4465 7374 726f 7941 5049  UpdateDestroyAPI
+000009f0: 5669 6577 5772 6974 6572 da0c 4150 4955  ViewWriter..APIU
+00000a00: 726c 5772 6974 6572 720c 0000 0072 0e00  rlWriterr....r..
+00000a10: 0000 720e 0000 0072 0f00 0000 da18 7772  ..r....r......wr
+00000a20: 6974 655f 6170 695f 7669 6577 735f 616e  ite_api_views_an
+00000a30: 645f 7572 6c73 2f00 0000 730a 0000 0006  d_urls/...s.....
+00000a40: 0106 010e 010e 0112 017a 2941 5049 5669  .........z)APIVi
+00000a50: 6577 5552 4c57 7269 7465 722e 7772 6974  ewURLWriter.writ
+00000a60: 655f 6170 695f 7669 6577 735f 616e 645f  e_api_views_and_
+00000a70: 7572 6c73 4e29 0572 1400 0000 7215 0000  urlsN).r....r...
+00000a80: 0072 1600 0000 7210 0000 0072 3200 0000  .r....r....r2...
+00000a90: 720e 0000 0072 0e00 0000 720e 0000 0072  r....r....r....r
+00000aa0: 0f00 0000 722d 0000 0029 0000 0073 0600  ....r-...)...s..
+00000ab0: 0000 0800 0802 0c04 722d 0000 004e 2909  ........r-...N).
+00000ac0: da1c 636f 6465 6c65 7373 5f64 6a61 6e67  ..codeless_djang
+00000ad0: 6f2e 7772 6974 6572 732e 6261 7365 7202  o.writers.baser.
+00000ae0: 0000 0072 0300 0000 7204 0000 0072 0600  ...r....r....r..
+00000af0: 0000 7218 0000 0072 2000 0000 7221 0000  ..r....r ...r!..
+00000b00: 0072 2d00 0000 720e 0000 0072 0e00 0000  .r-...r....r....
+00000b10: 720e 0000 0072 0f00 0000 da08 3c6d 6f64  r....r......<mod
+00000b20: 756c 653e 0100 0000 730c 0000 0014 0010  ule>....s.......
+00000b30: 0310 0910 0510 0512 12                   .........
```

### Comparing `codeless-django-0.0.14/codeless_django/writers/__pycache__/apps.cpython-310.pyc` & `codeless-django-0.0.15/codeless_django/writers/__pycache__/apps.cpython-310.pyc`

 * *Format-specific differences are supported for Python .pyc files but no file-specific differences were detected; falling back to a binary diff. file(1) reports: Byte-compiled Python module for CPython 3.10, timestamp-based, .py timestamp: Thu Jun  8 23:43:49 2023 UTC, .py size: 5343 bytes*

 * *Could not decompile bytecode: bad marshal data (unknown type code)*

 * *Files 2% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-00000000: 6f0d 0d0a 0000 0000 b567 8264 df14 0000  o........g.d....
+00000000: 6f0d 0d0a 0000 0000 6f28 bd64 df14 0000  o.......o(.d....
 00000010: e300 0000 0000 0000 0000 0000 0000 0000  ................
 00000020: 0004 0000 0040 0000 0073 ba00 0000 6400  .....@...s....d.
 00000030: 6401 6c00 5a00 6400 6402 6c01 6d02 5a02  d.l.Z.d.d.l.m.Z.
 00000040: 0100 6400 6403 6c03 6d04 5a04 6d05 5a05  ..d.d.l.m.Z.m.Z.
 00000050: 0100 6400 6404 6c06 6d07 5a07 0100 6400  ..d.d.l.m.Z...d.
 00000060: 6405 6c08 6d09 5a09 0100 6400 6406 6c0a  d.l.m.Z...d.d.l.
 00000070: 6d0b 5a0b 0100 6400 6407 6c0c 6d0d 5a0d  m.Z...d.d.l.m.Z.
@@ -37,353 +37,355 @@
 00000240: 5f04 6400 5300 2904 4eda 012e 7201 0000  _.d.S.).N...r...
 00000250: 007a 0c2f 7365 7474 696e 6773 2e70 79a9  .z./settings.py.
 00000260: 05da 0961 7070 5f6e 616d 6573 7202 0000  ...app_namesr...
 00000270: 00da 0c52 4f4f 545f 5552 4c43 4f4e 46da  ...ROOT_URLCONF.
 00000280: 0573 706c 6974 da09 6669 6c65 5f6e 616d  .split..file_nam
 00000290: 6529 03da 0473 656c 6672 1000 0000 da0d  e)...selfr......
 000002a0: 7365 7474 696e 6773 5f66 696c 65a9 0072  settings_file..r
-000002b0: 1600 0000 fa37 2f68 6f6d 652f 6f6d 6172  .....7/home/omar
-000002c0: 2f63 6f64 652f 5175 6963 6b44 6a2f 636f  /code/QuickDj/co
-000002d0: 6465 6c65 7373 5f64 6a61 6e67 6f2f 7772  deless_django/wr
-000002e0: 6974 6572 732f 6170 7073 2e70 79da 085f  iters/apps.py.._
-000002f0: 5f69 6e69 745f 5f0e 0000 0073 0600 0000  _init__....s....
-00000300: 0601 1401 0a01 7a16 4e65 7741 7070 7357  ......z.NewAppsW
-00000310: 7269 7465 722e 5f5f 696e 6974 5f5f 6301  riter.__init__c.
-00000320: 0000 0000 0000 0000 0000 0001 0000 0001  ................
-00000330: 0000 0043 0000 00f3 0400 0000 6401 5300  ...C........d.S.
-00000340: 2902 4e7a 1149 4e53 5441 4c4c 4544 5f41  ).Nz.INSTALLED_A
-00000350: 5050 532b 3d5b 7216 0000 00a9 0172 1400  PPS+=[r......r..
-00000360: 0000 7216 0000 0072 1600 0000 7217 0000  ..r....r....r...
-00000370: 00da 1167 6574 5f6f 626a 6563 745f 6865  ...get_object_he
-00000380: 6164 6572 1300 0000 f302 0000 0004 017a  ader...........z
-00000390: 1f4e 6577 4170 7073 5772 6974 6572 2e67  .NewAppsWriter.g
-000003a0: 6574 5f6f 626a 6563 745f 6865 6164 6572  et_object_header
-000003b0: 6301 0000 0000 0000 0000 0000 0003 0000  c...............
-000003c0: 0005 0000 0043 0000 0073 2800 0000 6401  .....C...s(...d.
-000003d0: 7d01 7c00 6a00 4400 5d0a 7d02 7c01 6402  }.|.j.D.].}.|.d.
-000003e0: 7c02 9b00 6403 9d03 3700 7d01 7105 7c01  |...d...7.}.q.|.
-000003f0: 6404 1700 5300 2905 4eda 010a 7a03 0920  d...S.).N...z.. 
-00000400: 227a 0422 2c20 0a7a 030a 5d0a 2901 7210  "z.", .z..].).r.
-00000410: 0000 0029 0372 1400 0000 da08 6e65 775f  ...).r......new_
-00000420: 6170 7073 da04 6e61 6d65 7216 0000 0072  apps..namer....r
-00000430: 1600 0000 7217 0000 00da 0f67 6574 5f6f  ....r......get_o
-00000440: 626a 6563 745f 626f 6479 1600 0000 7308  bject_body....s.
-00000450: 0000 0004 010a 0112 0108 017a 1d4e 6577  ...........z.New
-00000460: 4170 7073 5772 6974 6572 2e67 6574 5f6f  AppsWriter.get_o
-00000470: 626a 6563 745f 626f 6479 6301 0000 0000  bject_bodyc.....
-00000480: 0000 0000 0000 0001 0000 0003 0000 0043  ...............C
-00000490: 0000 00f3 1000 0000 7c00 a000 a100 7c00  ........|.....|.
-000004a0: a001 a100 1700 5300 a901 4ea9 0272 1b00  ......S...N..r..
-000004b0: 0000 7220 0000 0072 1a00 0000 7216 0000  ..r ...r....r...
-000004c0: 0072 1600 0000 7217 0000 00da 0f67 6574  .r....r......get
-000004d0: 5f66 756c 6c5f 7374 7269 6e67 1c00 0000  _full_string....
-000004e0: f302 0000 0010 017a 1d4e 6577 4170 7073  .......z.NewApps
-000004f0: 5772 6974 6572 2e67 6574 5f66 756c 6c5f  Writer.get_full_
-00000500: 7374 7269 6e67 4e29 07da 085f 5f6e 616d  stringN)...__nam
-00000510: 655f 5fda 0a5f 5f6d 6f64 756c 655f 5fda  e__..__module__.
-00000520: 0c5f 5f71 7561 6c6e 616d 655f 5f72 1800  .__qualname__r..
-00000530: 0000 721b 0000 0072 2000 0000 7224 0000  ..r....r ...r$..
-00000540: 0072 1600 0000 7216 0000 0072 1600 0000  .r....r....r....
-00000550: 7217 0000 0072 0d00 0000 0d00 0000 730a  r....r........s.
-00000560: 0000 0008 0008 0108 0508 030c 0672 0d00  .............r..
-00000570: 0000 6300 0000 0000 0000 0000 0000 0000  ..c.............
-00000580: 0000 0002 0000 0040 0000 0073 3400 0000  .......@...s4...
-00000590: 6500 5a01 6400 5a02 6401 6402 8400 5a03  e.Z.d.Z.d.d...Z.
-000005a0: 6403 6404 8400 5a04 6405 6406 8400 5a05  d.d...Z.d.d...Z.
-000005b0: 6407 6408 8400 5a06 6409 640a 8400 5a07  d.d...Z.d.d...Z.
-000005c0: 640b 5300 290c da1c 496e 636c 7564 6541  d.S.)...IncludeA
-000005d0: 7070 5572 6c54 6f52 6f6f 7455 726c 5772  ppUrlToRootUrlWr
-000005e0: 6974 6572 6302 0000 0000 0000 0000 0000  iterc...........
-000005f0: 0002 0000 0003 0000 0043 0000 0073 2000  .........C...s .
-00000600: 0000 7c01 7c00 5f00 7401 6a02 a003 6401  ..|.|._.t.j...d.
-00000610: a101 6402 1900 6403 1700 7c00 5f04 6400  ..d...d...|._.d.
-00000620: 5300 2904 4e72 0e00 0000 7201 0000 007a  S.).Nr....r....z
-00000630: 082f 7572 6c73 2e70 7972 0f00 0000 a902  ./urls.pyr......
-00000640: 7214 0000 0072 1000 0000 7216 0000 0072  r....r....r....r
-00000650: 1600 0000 7217 0000 0072 1800 0000 2100  ....r....r....!.
-00000660: 0000 7304 0000 0006 011a 017a 2549 6e63  ..s........z%Inc
-00000670: 6c75 6465 4170 7055 726c 546f 526f 6f74  ludeAppUrlToRoot
-00000680: 5572 6c57 7269 7465 722e 5f5f 696e 6974  UrlWriter.__init
-00000690: 5f5f 6301 0000 0000 0000 0000 0000 0001  __c.............
-000006a0: 0000 0001 0000 0043 0000 0072 1900 0000  .......C...r....
-000006b0: 2902 4e7a 1075 726c 7061 7474 6572 6e73  ).Nz.urlpatterns
-000006c0: 2b3d 5b0a 0972 1600 0000 721a 0000 0072  +=[..r....r....r
-000006d0: 1600 0000 7216 0000 0072 1700 0000 721b  ....r....r....r.
-000006e0: 0000 0025 0000 0072 1c00 0000 7a2e 496e  ...%...r....z.In
-000006f0: 636c 7564 6541 7070 5572 6c54 6f52 6f6f  cludeAppUrlToRoo
-00000700: 7455 726c 5772 6974 6572 2e67 6574 5f6f  tUrlWriter.get_o
-00000710: 626a 6563 745f 6865 6164 6572 6302 0000  bject_headerc...
-00000720: 0000 0000 0000 0000 0002 0000 0005 0000  ................
-00000730: 0043 0000 0073 1200 0000 6401 7c01 9b00  .C...s....d.|...
-00000740: 6402 7c01 9b00 6403 9d05 5300 2904 4e7a  d.|...d...S.).Nz
-00000750: 0670 6174 6828 277a 0d2f 272c 2069 6e63  .path('z./', inc
-00000760: 6c75 6465 2827 7a0c 2e75 726c 7327 2929  lude('z..urls'))
-00000770: 2c20 0a09 7216 0000 00a9 0272 1400 0000  , ..r......r....
-00000780: da08 6170 705f 6e61 6d65 7216 0000 0072  ..app_namer....r
-00000790: 1600 0000 7217 0000 00da 1367 6574 5f69  ....r......get_i
-000007a0: 6e63 6c75 6465 5f61 7070 5f75 726c 2800  nclude_app_url(.
-000007b0: 0000 7302 0000 0012 017a 3049 6e63 6c75  ..s......z0Inclu
-000007c0: 6465 4170 7055 726c 546f 526f 6f74 5572  deAppUrlToRootUr
-000007d0: 6c57 7269 7465 722e 6765 745f 696e 636c  lWriter.get_incl
-000007e0: 7564 655f 6170 705f 7572 6c63 0100 0000  ude_app_urlc....
-000007f0: 0000 0000 0000 0000 0300 0000 0500 0000  ................
-00000800: 4300 0000 7326 0000 0064 017d 017c 006a  C...s&...d.}.|.j
-00000810: 0044 005d 097d 027c 017c 00a0 017c 02a1  .D.].}.|.|...|..
-00000820: 0137 007d 0171 057c 0164 0217 0053 0029  .7.}.q.|.d...S.)
-00000830: 034e da00 7a04 0a20 5d0a 2902 7210 0000  .N..z.. ].).r...
-00000840: 0072 2d00 0000 2903 7214 0000 00da 0861  .r-...).r......a
-00000850: 7070 5f75 726c 7372 1f00 0000 7216 0000  pp_urlsr....r...
-00000860: 0072 1600 0000 7217 0000 0072 2000 0000  .r....r....r ...
-00000870: 2c00 0000 7308 0000 0004 010a 0110 0108  ,...s...........
-00000880: 027a 2c49 6e63 6c75 6465 4170 7055 726c  .z,IncludeAppUrl
-00000890: 546f 526f 6f74 5572 6c57 7269 7465 722e  ToRootUrlWriter.
-000008a0: 6765 745f 6f62 6a65 6374 5f62 6f64 7963  get_object_bodyc
-000008b0: 0100 0000 0000 0000 0000 0000 0100 0000  ................
-000008c0: 0300 0000 4300 0000 7221 0000 0072 2200  ....C...r!...r".
-000008d0: 0000 7223 0000 0072 1a00 0000 7216 0000  ..r#...r....r...
-000008e0: 0072 1600 0000 7217 0000 0072 2400 0000  .r....r....r$...
-000008f0: 3300 0000 7225 0000 007a 2c49 6e63 6c75  3...r%...z,Inclu
-00000900: 6465 4170 7055 726c 546f 526f 6f74 5572  deAppUrlToRootUr
-00000910: 6c57 7269 7465 722e 6765 745f 6675 6c6c  lWriter.get_full
-00000920: 5f73 7472 696e 674e 2908 7226 0000 0072  _stringN).r&...r
-00000930: 2700 0000 7228 0000 0072 1800 0000 721b  '...r(...r....r.
-00000940: 0000 0072 2d00 0000 7220 0000 0072 2400  ...r-...r ...r$.
-00000950: 0000 7216 0000 0072 1600 0000 7216 0000  ..r....r....r...
-00000960: 0072 1700 0000 7229 0000 001f 0000 0073  .r....r).......s
-00000970: 0c00 0000 0800 0802 0804 0803 0804 0c07  ................
-00000980: 7229 0000 0063 0000 0000 0000 0000 0000  r)...c..........
-00000990: 0000 0000 0000 0400 0000 4000 0000 7382  ..........@...s.
-000009a0: 0000 0065 005a 0164 005a 0264 1f64 2064  ...e.Z.d.Z.d.d d
-000009b0: 0464 0584 055a 0364 0665 0464 0264 0366  .d...Z.d.e.d.d.f
-000009c0: 0464 0764 0884 045a 0564 0964 0a84 005a  .d.d...Z.d.d...Z
-000009d0: 0664 0b64 0c84 005a 0764 0d64 0e84 005a  .d.d...Z.d.d...Z
-000009e0: 0864 0f64 1084 005a 0964 1164 1284 005a  .d.d...Z.d.d...Z
-000009f0: 0a64 1364 1484 005a 0b64 1564 1684 005a  .d.d...Z.d.d...Z
-00000a00: 0c64 1764 1884 005a 0d64 1964 1a84 005a  .d.d...Z.d.d...Z
-00000a10: 0e64 1b64 1c84 005a 0f64 1d64 1e84 005a  .d.d...Z.d.d...Z
-00000a20: 1064 0353 0029 21da 0957 7269 7465 4170  .d.S.)!..WriteAp
-00000a30: 7073 46da 0672 6574 7572 6e4e 6304 0000  psF..returnNc...
-00000a40: 0000 0000 0000 0000 0004 0000 0003 0000  ................
-00000a50: 0043 0000 0073 2a00 0000 7c01 7c00 5f00  .C...s*...|.|._.
-00000a60: 7c02 7c00 5f01 7c03 7c00 5f02 6401 6402  |.|._.|.|._.d.d.
-00000a70: 8400 7c01 a003 a100 4400 8301 7c00 5f04  ..|.....D...|._.
-00000a80: 6400 5300 2903 4e63 0100 0000 0000 0000  d.S.).Nc........
-00000a90: 0000 0000 0300 0000 0400 0000 5300 0000  ............S...
-00000aa0: 7314 0000 0067 007c 005d 065c 027d 017d  s....g.|.].\.}.}
-00000ab0: 027c 0191 0271 0253 0072 1600 0000 7216  .|...q.S.r....r.
-00000ac0: 0000 0029 03da 022e 3072 2c00 0000 da05  ...)....0r,.....
-00000ad0: 7661 6c75 6572 1600 0000 7216 0000 0072  valuer....r....r
-00000ae0: 1700 0000 da0a 3c6c 6973 7463 6f6d 703e  ......<listcomp>
-00000af0: 3e00 0000 7302 0000 0014 007a 2657 7269  >...s......z&Wri
-00000b00: 7465 4170 7073 2e5f 5f69 6e69 745f 5f2e  teApps.__init__.
-00000b10: 3c6c 6f63 616c 733e 2e3c 6c69 7374 636f  <locals>.<listco
-00000b20: 6d70 3e29 05da 0461 7070 73da 1477 7269  mp>)...apps..wri
-00000b30: 7465 5f74 656d 706c 6174 655f 7669 6577  te_template_view
-00000b40: 73da 0f77 7269 7465 5f61 7069 5f76 6965  s..write_api_vie
-00000b50: 7773 da05 6974 656d 73da 0f6c 6f63 616c  ws..items..local
-00000b60: 5f61 7070 5f6e 616d 6573 2904 7214 0000  _app_names).r...
-00000b70: 0072 3500 0000 7236 0000 0072 3700 0000  .r5...r6...r7...
-00000b80: 7216 0000 0072 1600 0000 7217 0000 0072  r....r....r....r
-00000b90: 1800 0000 3a00 0000 7308 0000 0006 0106  ....:...s.......
-00000ba0: 0106 0118 017a 1257 7269 7465 4170 7073  .....z.WriteApps
-00000bb0: 2e5f 5f69 6e69 745f 5f72 2c00 0000 6302  .__init__r,...c.
-00000bc0: 0000 0000 0000 0000 0000 0002 0000 0006  ................
-00000bd0: 0000 0043 0000 0073 1a00 0000 7400 a001  ...C...s....t...
-00000be0: 6401 7c01 9b00 6402 7c01 9b00 9d04 a101  d.|...d.|.......
-00000bf0: 0100 6400 5300 2903 4e7a 0772 6d20 2d72  ..d.S.).Nz.rm -r
-00000c00: 6620 7a1e 2026 2620 7079 7468 6f6e 206d  f z. && python m
-00000c10: 616e 6167 652e 7079 2073 7461 7274 6170  anage.py startap
-00000c20: 7020 2902 da02 6f73 da06 7379 7374 656d  p )...os..system
-00000c30: 722b 0000 0072 1600 0000 7216 0000 0072  r+...r....r....r
-00000c40: 1700 0000 da09 7374 6172 745f 6170 7040  ......start_app@
-00000c50: 0000 0073 0200 0000 1a01 7a13 5772 6974  ...s......z.Writ
-00000c60: 6541 7070 732e 7374 6172 745f 6170 7063  eApps.start_appc
-00000c70: 0100 0000 0000 0000 0000 0000 0300 0000  ................
-00000c80: 0400 0000 4300 0000 7322 0000 007c 006a  ....C...s"...|.j
-00000c90: 00a0 01a1 0044 005d 095c 027d 017d 027c  .....D.].\.}.}.|
-00000ca0: 00a0 027c 01a1 0101 0071 0564 0053 0072  ...|.....q.d.S.r
-00000cb0: 2200 0000 2903 7235 0000 0072 3800 0000  "...).r5...r8...
-00000cc0: 723c 0000 00a9 0372 1400 0000 722c 0000  r<.....r....r,..
-00000cd0: 0072 3300 0000 7216 0000 0072 1600 0000  .r3...r....r....
-00000ce0: 7217 0000 00da 1263 7265 6174 655f 6170  r......create_ap
-00000cf0: 705f 666f 6c64 6572 7343 0000 0073 0600  p_foldersC...s..
-00000d00: 0000 1201 0c01 04ff 7a1c 5772 6974 6541  ........z.WriteA
-00000d10: 7070 732e 6372 6561 7465 5f61 7070 5f66  pps.create_app_f
-00000d20: 6f6c 6465 7273 6301 0000 0000 0000 0000  oldersc.........
-00000d30: 0000 0003 0000 0004 0000 0043 0000 0073  ...........C...s
-00000d40: 2400 0000 7c00 6a00 a001 a100 4400 5d0a  $...|.j.....D.].
-00000d50: 5c02 7d01 7d02 7402 7c01 7c00 6a03 8302  \.}.}.t.|.|.j...
-00000d60: 0100 7105 6400 5300 7222 0000 0029 0472  ..q.d.S.r"...).r
-00000d70: 3500 0000 7238 0000 0072 0800 0000 7237  5...r8...r....r7
-00000d80: 0000 0072 3d00 0000 7216 0000 0072 1600  ...r=...r....r..
-00000d90: 0000 7217 0000 00da 2169 6e69 7469 6174  ..r.....!initiat
-00000da0: 655f 6170 705f 7572 6c73 5f61 6e64 5f76  e_app_urls_and_v
-00000db0: 6965 7773 5f66 696c 6573 4700 0000 7306  iews_filesG...s.
-00000dc0: 0000 0012 010e 0104 ff7a 2b57 7269 7465  .........z+Write
-00000dd0: 4170 7073 2e69 6e69 7469 6174 655f 6170  Apps.initiate_ap
-00000de0: 705f 7572 6c73 5f61 6e64 5f76 6965 7773  p_urls_and_views
-00000df0: 5f66 696c 6573 6301 0000 0000 0000 0000  _filesc.........
-00000e00: 0000 0004 0000 0004 0000 0043 0000 0073  ...........C...s
-00000e10: 2e00 0000 7c00 6a00 a001 a100 4400 5d0f  ....|.j.....D.].
-00000e20: 5c02 7d01 7d02 7c02 6401 1900 7d03 7402  \.}.}.|.d...}.t.
-00000e30: 7c01 7c03 8302 a003 a100 0100 7105 6400  |.|.........q.d.
-00000e40: 5300 a902 4eda 066d 6f64 656c 7329 0472  S...N..models).r
-00000e50: 3500 0000 7238 0000 0072 0700 0000 da0c  5...r8...r......
-00000e60: 7772 6974 655f 6f62 6a65 6374 a904 7214  write_object..r.
-00000e70: 0000 0072 2c00 0000 7233 0000 0072 4100  ...r,...r3...rA.
-00000e80: 0000 7216 0000 0072 1600 0000 7217 0000  ..r....r....r...
-00000e90: 00da 0c77 7269 7465 5f6d 6f64 656c 734b  ...write_modelsK
-00000ea0: 0000 0073 0800 0000 1201 0801 1001 04fe  ...s............
-00000eb0: 7a16 5772 6974 6541 7070 732e 7772 6974  z.WriteApps.writ
-00000ec0: 655f 6d6f 6465 6c73 6301 0000 0000 0000  e_modelsc.......
-00000ed0: 0000 0000 0002 0000 0002 0000 0043 0000  .............C..
-00000ee0: 0073 2600 0000 7c00 6a00 7d01 7c00 6a01  .s&...|.j.}.|.j.
-00000ef0: 7309 7c00 6a02 7211 7403 7c01 8301 a004  s.|.j.r.t.|.....
-00000f00: a100 0100 6400 5300 6400 5300 7222 0000  ....d.S.d.S.r"..
-00000f10: 0029 0572 3900 0000 7237 0000 0072 3600  .).r9...r7...r6.
-00000f20: 0000 7229 0000 0072 4200 0000 722a 0000  ..r)...rB...r*..
-00000f30: 0072 1600 0000 7216 0000 0072 1700 0000  .r....r....r....
-00000f40: da10 696e 636c 7564 655f 6170 705f 7572  ..include_app_ur
-00000f50: 6c73 5000 0000 7308 0000 0006 010c 0110  lsP...s.........
-00000f60: 0104 ff7a 1a57 7269 7465 4170 7073 2e69  ...z.WriteApps.i
-00000f70: 6e63 6c75 6465 5f61 7070 5f75 726c 7363  nclude_app_urlsc
-00000f80: 0100 0000 0000 0000 0000 0000 0200 0000  ................
-00000f90: 0300 0000 4300 0000 7334 0000 007c 006a  ....C...s4...|.j
-00000fa0: 00a0 01a1 007d 017c 006a 0272 0d7c 01a0  .....}.|.j.r.|..
-00000fb0: 0364 01a1 0101 007c 01a0 0364 02a1 0101  .d.....|...d....
-00000fc0: 0074 047c 0183 01a0 05a1 0001 0064 0053  .t.|.........d.S
-00000fd0: 0029 034e da0e 7265 7374 5f66 7261 6d65  .).N..rest_frame
-00000fe0: 776f 726b da08 6472 665f 7961 7367 2906  work..drf_yasg).
-00000ff0: 7239 0000 00da 0463 6f70 7972 3700 0000  r9.....copyr7...
-00001000: da06 6170 7065 6e64 720d 0000 0072 4200  ..appendr....rB.
-00001010: 0000 722a 0000 0072 1600 0000 7216 0000  ..r*...r....r...
-00001020: 0072 1700 0000 da17 696e 636c 7564 655f  .r......include_
-00001030: 6170 705f 746f 5f73 6574 7469 6e67 7355  app_to_settingsU
-00001040: 0000 0073 0a00 0000 0a01 0601 0a01 0a01  ...s............
-00001050: 1002 7a21 5772 6974 6541 7070 732e 696e  ..z!WriteApps.in
-00001060: 636c 7564 655f 6170 705f 746f 5f73 6574  clude_app_to_set
-00001070: 7469 6e67 7363 0100 0000 0000 0000 0000  tingsc..........
-00001080: 0000 0400 0000 0400 0000 4300 0000 f338  ..........C....8
-00001090: 0000 007c 006a 0072 187c 006a 01a0 02a1  ...|.j.r.|.j....
-000010a0: 0044 005d 115c 027d 017d 027c 0264 0119  .D.].\.}.}.|.d..
-000010b0: 007d 0374 037c 017c 0383 02a0 04a1 0001  .}.t.|.|........
-000010c0: 0071 0864 0053 0064 0053 0072 4000 0000  .q.d.S.d.S.r@...
-000010d0: 2905 7236 0000 0072 3500 0000 7238 0000  ).r6...r5...r8..
-000010e0: 0072 0500 0000 7242 0000 0072 4300 0000  .r....rB...rC...
-000010f0: 7216 0000 0072 1600 0000 7217 0000 00da  r....r....r.....
-00001100: 0f77 7269 7465 5f61 7070 5f76 6965 7773  .write_app_views
-00001110: 5d00 0000 f30c 0000 0006 0112 0108 0110  ]...............
-00001120: 0104 fd04 017a 1957 7269 7465 4170 7073  .....z.WriteApps
-00001130: 2e77 7269 7465 5f61 7070 5f76 6965 7773  .write_app_views
-00001140: 6301 0000 0000 0000 0000 0000 0004 0000  c...............
-00001150: 0004 0000 0043 0000 0072 4b00 0000 7240  .....C...rK...r@
-00001160: 0000 0029 0572 3600 0000 7235 0000 0072  ...).r6...r5...r
-00001170: 3800 0000 7203 0000 0072 4200 0000 7243  8...r....rB...rC
-00001180: 0000 0072 1600 0000 7216 0000 0072 1700  ...r....r....r..
-00001190: 0000 da0a 7772 6974 655f 7572 6c73 6300  ....write_urlsc.
-000011a0: 0000 724d 0000 007a 1457 7269 7465 4170  ..rM...z.WriteAp
-000011b0: 7073 2e77 7269 7465 5f75 726c 7363 0100  ps.write_urlsc..
-000011c0: 0000 0000 0000 0000 0000 0400 0000 0400  ................
-000011d0: 0000 4300 0000 724b 0000 0072 4000 0000  ..C...rK...r@...
-000011e0: 2905 7237 0000 0072 3500 0000 7238 0000  ).r7...r5...r8..
-000011f0: 0072 0400 0000 7242 0000 0072 4300 0000  .r....rB...rC...
-00001200: 7216 0000 0072 1600 0000 7217 0000 00da  r....r....r.....
-00001210: 0e77 7269 7465 5f61 7069 5f75 726c 7369  .write_api_urlsi
-00001220: 0000 0073 0c00 0000 0601 1202 0801 1001  ...s............
-00001230: 04fc 0402 7a18 5772 6974 6541 7070 732e  ....z.WriteApps.
-00001240: 7772 6974 655f 6170 695f 7572 6c73 6301  write_api_urlsc.
-00001250: 0000 0000 0000 0000 0000 0004 0000 0004  ................
-00001260: 0000 0043 0000 0072 4b00 0000 7240 0000  ...C...rK...r@..
-00001270: 0029 0572 3700 0000 7235 0000 0072 3800  .).r7...r5...r8.
-00001280: 0000 720b 0000 0072 4200 0000 7243 0000  ..r....rB...rC..
-00001290: 0072 1600 0000 7216 0000 0072 1700 0000  .r....r....r....
-000012a0: da11 7772 6974 655f 7365 7269 616c 697a  ..write_serializ
-000012b0: 6572 7372 0000 0072 4d00 0000 7a1b 5772  ersr...rM...z.Wr
-000012c0: 6974 6541 7070 732e 7772 6974 655f 7365  iteApps.write_se
-000012d0: 7269 616c 697a 6572 7363 0100 0000 0000  rializersc......
-000012e0: 0000 0000 0000 0400 0000 0400 0000 4300  ..............C.
-000012f0: 0000 724b 0000 0072 4000 0000 2905 7237  ..rK...r@...).r7
-00001300: 0000 0072 3500 0000 7238 0000 0072 0600  ...r5...r8...r..
-00001310: 0000 7242 0000 0072 4300 0000 7216 0000  ..rB...rC...r...
-00001320: 0072 1600 0000 7217 0000 00da 1377 7269  .r....r......wri
-00001330: 7465 5f61 7070 5f61 7069 5f76 6965 7773  te_app_api_views
-00001340: 7800 0000 724d 0000 007a 1d57 7269 7465  x...rM...z.Write
-00001350: 4170 7073 2e77 7269 7465 5f61 7070 5f61  Apps.write_app_a
-00001360: 7069 5f76 6965 7773 6301 0000 0000 0000  pi_viewsc.......
-00001370: 0000 0000 0005 0000 0004 0000 0043 0000  .............C..
-00001380: 0073 c000 0000 7400 8300 7d01 7c01 a001  .s....t...}.|...
-00001390: a100 0100 7c00 a002 a100 0100 7c01 a003  ....|.......|...
-000013a0: 6401 6402 a102 0100 7c00 6a04 721a 7c01  d.d.....|.j.r.|.
-000013b0: a003 6403 6404 a102 0100 7405 a006 6405  ..d.d.....t...d.
-000013c0: a101 0100 7407 8300 7d02 7c02 a008 a100  ....t...}.|.....
-000013d0: 0100 7c00 a009 a100 0100 7c00 a00a a100  ..|.......|.....
-000013e0: 0100 7c00 a00b a100 0100 7c00 6a0c a00d  ..|.......|.j...
-000013f0: a100 4400 5d1c 5c02 7d03 7d04 7c00 a00e  ..D.].\.}.}.|...
-00001400: a100 0100 7c00 a00f a100 0100 7c00 a010  ....|.......|...
-00001410: a100 0100 7c00 a011 a100 0100 7c00 a012  ....|.......|...
-00001420: a100 0100 7c00 a013 a100 0100 7137 7405  ....|.......q7t.
-00001430: a006 6406 a101 0100 7405 a006 6407 a101  ..d.....t...d...
-00001440: 0100 6400 5300 2908 4e72 4700 0000 7a06  ..d.S.).NrG...z.
-00001450: 312e 3231 2e35 da13 646a 616e 676f 7265  1.21.5..djangore
-00001460: 7374 6672 616d 6577 6f72 6b7a 0633 2e31  stframeworkz.3.1
-00001470: 342e 307a 1f70 6970 2069 6e73 7461 6c6c  4.0z.pip install
-00001480: 202d 7220 7265 7175 6972 656d 656e 7473   -r requirements
-00001490: 2e74 7874 7a20 7079 7468 6f6e 3320 6d61  .txtz python3 ma
-000014a0: 6e61 6765 2e70 7920 6d61 6b65 6d69 6772  nage.py makemigr
-000014b0: 6174 696f 6e73 7a19 7079 7468 6f6e 3320  ationsz.python3 
-000014c0: 6d61 6e61 6765 2e70 7920 6d69 6772 6174  manage.py migrat
-000014d0: 6529 1472 0900 0000 da14 7772 6974 655f  e).r......write_
-000014e0: 6769 7469 676e 6f72 655f 6669 6c65 723e  gitignore_filer>
-000014f0: 0000 00da 2677 7269 7465 5f6e 6577 5f70  ....&write_new_p
-00001500: 6163 6b61 6765 5f69 6e5f 7265 7175 6972  ackage_in_requir
-00001510: 656d 656e 7473 5f74 6578 7472 3700 0000  ements_textr7...
-00001520: 723a 0000 0072 3b00 0000 720c 0000 00da  r:...r;...r.....
-00001530: 1777 7269 7465 5f64 6f63 756d 656e 7461  .write_documenta
-00001540: 7469 6f6e 5f75 726c 723f 0000 0072 4a00  tion_urlr?...rJ.
-00001550: 0000 7245 0000 0072 3500 0000 7238 0000  ..rE...r5...r8..
-00001560: 0072 4400 0000 724c 0000 0072 4e00 0000  .rD...rL...rN...
-00001570: 7250 0000 0072 5100 0000 724f 0000 0029  rP...rQ...rO...)
-00001580: 0572 1400 0000 da0b 6669 6c65 5f77 7269  .r......file_wri
-00001590: 7465 72da 0a64 6f63 5f77 7269 7465 7272  ter..doc_writerr
-000015a0: 2c00 0000 7233 0000 0072 1600 0000 7216  ,...r3...r....r.
-000015b0: 0000 0072 1700 0000 da05 7772 6974 657f  ...r......write.
-000015c0: 0000 0073 2a00 0000 0601 0801 0801 0c01  ...s*...........
-000015d0: 0601 0c01 0a01 0603 0801 0801 0801 0801  ................
-000015e0: 1202 0801 0801 0801 0801 0801 0a01 0a02  ................
-000015f0: 0e01 7a0f 5772 6974 6541 7070 732e 7772  ..z.WriteApps.wr
-00001600: 6974 6529 0246 4629 0272 3100 0000 4e29  ite).FF).r1...N)
-00001610: 1172 2600 0000 7227 0000 0072 2800 0000  .r&...r'...r(...
-00001620: 7218 0000 00da 0373 7472 723c 0000 0072  r......strr<...r
-00001630: 3e00 0000 723f 0000 0072 4400 0000 7245  >...r?...rD...rE
-00001640: 0000 0072 4a00 0000 724c 0000 0072 4e00  ...rJ...rL...rN.
-00001650: 0000 724f 0000 0072 5000 0000 7251 0000  ..rO...rP...rQ..
-00001660: 0072 5800 0000 7216 0000 0072 1600 0000  .rX...r....r....
-00001670: 7216 0000 0072 1700 0000 7230 0000 0039  r....r....r0...9
-00001680: 0000 0073 1c00 0000 0800 0c01 1206 0803  ...s............
-00001690: 0804 0804 0805 0805 0808 0806 0806 0809  ................
-000016a0: 0806 0c07 7230 0000 0029 1872 3a00 0000  ....r0...).r:...
-000016b0: da0b 646a 616e 676f 2e63 6f6e 6672 0200  ..django.confr..
-000016c0: 0000 da1c 636f 6465 6c65 7373 5f64 6a61  ....codeless_dja
-000016d0: 6e67 6f2e 7772 6974 6572 732e 7572 6c73  ngo.writers.urls
-000016e0: 7203 0000 0072 0400 0000 da1d 636f 6465  r....r......code
-000016f0: 6c65 7373 5f64 6a61 6e67 6f2e 7772 6974  less_django.writ
-00001700: 6572 732e 7669 6577 7372 0500 0000 da1c  ers.viewsr......
-00001710: 636f 6465 6c65 7373 5f64 6a61 6e67 6f2e  codeless_django.
-00001720: 7772 6974 6572 732e 6170 6973 7206 0000  writers.apisr...
-00001730: 00da 1e63 6f64 656c 6573 735f 646a 616e  ...codeless_djan
-00001740: 676f 2e77 7269 7465 7273 2e6d 6f64 656c  go.writers.model
-00001750: 7372 0700 0000 da1d 636f 6465 6c65 7373  sr......codeless
-00001760: 5f64 6a61 6e67 6f2e 7772 6974 6572 732e  _django.writers.
-00001770: 6669 6c65 7372 0800 0000 7209 0000 00da  filesr....r.....
-00001780: 1c63 6f64 656c 6573 735f 646a 616e 676f  .codeless_django
-00001790: 2e77 7269 7465 7273 2e62 6173 6572 0a00  .writers.baser..
-000017a0: 0000 da23 636f 6465 6c65 7373 5f64 6a61  ...#codeless_dja
-000017b0: 6e67 6f2e 7772 6974 6572 732e 7365 7269  ngo.writers.seri
-000017c0: 616c 697a 6572 7372 0b00 0000 da25 636f  alizersr.....%co
-000017d0: 6465 6c65 7373 5f64 6a61 6e67 6f2e 7772  deless_django.wr
-000017e0: 6974 6572 732e 646f 6375 6d65 6e74 6174  iters.documentat
-000017f0: 696f 6e72 0c00 0000 720d 0000 0072 2900  ionr....r....r).
-00001800: 0000 7230 0000 0072 1600 0000 7216 0000  ..r0...r....r...
-00001810: 0072 1600 0000 7217 0000 00da 083c 6d6f  .r....r......<mo
-00001820: 6475 6c65 3e01 0000 0073 1c00 0000 0800  dule>....s......
-00001830: 0c01 1001 0c01 0c01 0c01 1001 0c01 0c01  ................
-00001840: 0c01 0c01 1002 1012 121a                 ..........
+000002b0: 1600 0000 fa5a 2f68 6f6d 652f 6f6d 6172  .....Z/home/omar
+000002c0: 2f63 6f64 652f 7465 7374 2d63 6c64 2f76  /code/test-cld/v
+000002d0: 656e 762f 6c69 622f 7079 7468 6f6e 332e  env/lib/python3.
+000002e0: 3130 2f73 6974 652d 7061 636b 6167 6573  10/site-packages
+000002f0: 2f63 6f64 656c 6573 735f 646a 616e 676f  /codeless_django
+00000300: 2f77 7269 7465 7273 2f61 7070 732e 7079  /writers/apps.py
+00000310: da08 5f5f 696e 6974 5f5f 0e00 0000 7306  ..__init__....s.
+00000320: 0000 0006 0114 010a 017a 164e 6577 4170  .........z.NewAp
+00000330: 7073 5772 6974 6572 2e5f 5f69 6e69 745f  psWriter.__init_
+00000340: 5f63 0100 0000 0000 0000 0000 0000 0100  _c..............
+00000350: 0000 0100 0000 4300 0000 f304 0000 0064  ......C........d
+00000360: 0153 0029 024e 7a11 494e 5354 414c 4c45  .S.).Nz.INSTALLE
+00000370: 445f 4150 5053 2b3d 5b72 1600 0000 a901  D_APPS+=[r......
+00000380: 7214 0000 0072 1600 0000 7216 0000 0072  r....r....r....r
+00000390: 1700 0000 da11 6765 745f 6f62 6a65 6374  ......get_object
+000003a0: 5f68 6561 6465 7213 0000 00f3 0200 0000  _header.........
+000003b0: 0401 7a1f 4e65 7741 7070 7357 7269 7465  ..z.NewAppsWrite
+000003c0: 722e 6765 745f 6f62 6a65 6374 5f68 6561  r.get_object_hea
+000003d0: 6465 7263 0100 0000 0000 0000 0000 0000  derc............
+000003e0: 0300 0000 0500 0000 4300 0000 7328 0000  ........C...s(..
+000003f0: 0064 017d 017c 006a 0044 005d 0a7d 027c  .d.}.|.j.D.].}.|
+00000400: 0164 027c 029b 0064 039d 0337 007d 0171  .d.|...d...7.}.q
+00000410: 057c 0164 0417 0053 0029 054e da01 0a7a  .|.d...S.).N...z
+00000420: 0309 2022 7a04 222c 200a 7a03 0a5d 0a29  .. "z.", .z..].)
+00000430: 0172 1000 0000 2903 7214 0000 00da 086e  .r....).r......n
+00000440: 6577 5f61 7070 73da 046e 616d 6572 1600  ew_apps..namer..
+00000450: 0000 7216 0000 0072 1700 0000 da0f 6765  ..r....r......ge
+00000460: 745f 6f62 6a65 6374 5f62 6f64 7916 0000  t_object_body...
+00000470: 0073 0800 0000 0401 0a01 1201 0801 7a1d  .s............z.
+00000480: 4e65 7741 7070 7357 7269 7465 722e 6765  NewAppsWriter.ge
+00000490: 745f 6f62 6a65 6374 5f62 6f64 7963 0100  t_object_bodyc..
+000004a0: 0000 0000 0000 0000 0000 0100 0000 0300  ................
+000004b0: 0000 4300 0000 f310 0000 007c 00a0 00a1  ..C........|....
+000004c0: 007c 00a0 01a1 0017 0053 00a9 014e a902  .|.......S...N..
+000004d0: 721b 0000 0072 2000 0000 721a 0000 0072  r....r ...r....r
+000004e0: 1600 0000 7216 0000 0072 1700 0000 da0f  ....r....r......
+000004f0: 6765 745f 6675 6c6c 5f73 7472 696e 671c  get_full_string.
+00000500: 0000 00f3 0200 0000 1001 7a1d 4e65 7741  ..........z.NewA
+00000510: 7070 7357 7269 7465 722e 6765 745f 6675  ppsWriter.get_fu
+00000520: 6c6c 5f73 7472 696e 674e 2907 da08 5f5f  ll_stringN)...__
+00000530: 6e61 6d65 5f5f da0a 5f5f 6d6f 6475 6c65  name__..__module
+00000540: 5f5f da0c 5f5f 7175 616c 6e61 6d65 5f5f  __..__qualname__
+00000550: 7218 0000 0072 1b00 0000 7220 0000 0072  r....r....r ...r
+00000560: 2400 0000 7216 0000 0072 1600 0000 7216  $...r....r....r.
+00000570: 0000 0072 1700 0000 720d 0000 000d 0000  ...r....r.......
+00000580: 0073 0a00 0000 0800 0801 0805 0803 0c06  .s..............
+00000590: 720d 0000 0063 0000 0000 0000 0000 0000  r....c..........
+000005a0: 0000 0000 0000 0200 0000 4000 0000 7334  ..........@...s4
+000005b0: 0000 0065 005a 0164 005a 0264 0164 0284  ...e.Z.d.Z.d.d..
+000005c0: 005a 0364 0364 0484 005a 0464 0564 0684  .Z.d.d...Z.d.d..
+000005d0: 005a 0564 0764 0884 005a 0664 0964 0a84  .Z.d.d...Z.d.d..
+000005e0: 005a 0764 0b53 0029 0cda 1c49 6e63 6c75  .Z.d.S.)...Inclu
+000005f0: 6465 4170 7055 726c 546f 526f 6f74 5572  deAppUrlToRootUr
+00000600: 6c57 7269 7465 7263 0200 0000 0000 0000  lWriterc........
+00000610: 0000 0000 0200 0000 0300 0000 4300 0000  ............C...
+00000620: 7320 0000 007c 017c 005f 0074 016a 02a0  s ...|.|._.t.j..
+00000630: 0364 01a1 0164 0219 0064 0317 007c 005f  .d...d...d...|._
+00000640: 0464 0053 0029 044e 720e 0000 0072 0100  .d.S.).Nr....r..
+00000650: 0000 7a08 2f75 726c 732e 7079 720f 0000  ..z./urls.pyr...
+00000660: 00a9 0272 1400 0000 7210 0000 0072 1600  ...r....r....r..
+00000670: 0000 7216 0000 0072 1700 0000 7218 0000  ..r....r....r...
+00000680: 0021 0000 0073 0400 0000 0601 1a01 7a25  .!...s........z%
+00000690: 496e 636c 7564 6541 7070 5572 6c54 6f52  IncludeAppUrlToR
+000006a0: 6f6f 7455 726c 5772 6974 6572 2e5f 5f69  ootUrlWriter.__i
+000006b0: 6e69 745f 5f63 0100 0000 0000 0000 0000  nit__c..........
+000006c0: 0000 0100 0000 0100 0000 4300 0000 7219  ..........C...r.
+000006d0: 0000 0029 024e 7a10 7572 6c70 6174 7465  ...).Nz.urlpatte
+000006e0: 726e 732b 3d5b 0a09 7216 0000 0072 1a00  rns+=[..r....r..
+000006f0: 0000 7216 0000 0072 1600 0000 7217 0000  ..r....r....r...
+00000700: 0072 1b00 0000 2500 0000 721c 0000 007a  .r....%...r....z
+00000710: 2e49 6e63 6c75 6465 4170 7055 726c 546f  .IncludeAppUrlTo
+00000720: 526f 6f74 5572 6c57 7269 7465 722e 6765  RootUrlWriter.ge
+00000730: 745f 6f62 6a65 6374 5f68 6561 6465 7263  t_object_headerc
+00000740: 0200 0000 0000 0000 0000 0000 0200 0000  ................
+00000750: 0500 0000 4300 0000 7312 0000 0064 017c  ....C...s....d.|
+00000760: 019b 0064 027c 019b 0064 039d 0553 0029  ...d.|...d...S.)
+00000770: 044e 7a06 7061 7468 2827 7a0d 2f27 2c20  .Nz.path('z./', 
+00000780: 696e 636c 7564 6528 277a 0c2e 7572 6c73  include('z..urls
+00000790: 2729 292c 200a 0972 1600 0000 a902 7214  ')), ..r......r.
+000007a0: 0000 00da 0861 7070 5f6e 616d 6572 1600  .....app_namer..
+000007b0: 0000 7216 0000 0072 1700 0000 da13 6765  ..r....r......ge
+000007c0: 745f 696e 636c 7564 655f 6170 705f 7572  t_include_app_ur
+000007d0: 6c28 0000 0073 0200 0000 1201 7a30 496e  l(...s......z0In
+000007e0: 636c 7564 6541 7070 5572 6c54 6f52 6f6f  cludeAppUrlToRoo
+000007f0: 7455 726c 5772 6974 6572 2e67 6574 5f69  tUrlWriter.get_i
+00000800: 6e63 6c75 6465 5f61 7070 5f75 726c 6301  nclude_app_urlc.
+00000810: 0000 0000 0000 0000 0000 0003 0000 0005  ................
+00000820: 0000 0043 0000 0073 2600 0000 6401 7d01  ...C...s&...d.}.
+00000830: 7c00 6a00 4400 5d09 7d02 7c01 7c00 a001  |.j.D.].}.|.|...
+00000840: 7c02 a101 3700 7d01 7105 7c01 6402 1700  |...7.}.q.|.d...
+00000850: 5300 2903 4eda 007a 040a 205d 0a29 0272  S.).N..z.. ].).r
+00000860: 1000 0000 722d 0000 0029 0372 1400 0000  ....r-...).r....
+00000870: da08 6170 705f 7572 6c73 721f 0000 0072  ..app_urlsr....r
+00000880: 1600 0000 7216 0000 0072 1700 0000 7220  ....r....r....r 
+00000890: 0000 002c 0000 0073 0800 0000 0401 0a01  ...,...s........
+000008a0: 1001 0802 7a2c 496e 636c 7564 6541 7070  ....z,IncludeApp
+000008b0: 5572 6c54 6f52 6f6f 7455 726c 5772 6974  UrlToRootUrlWrit
+000008c0: 6572 2e67 6574 5f6f 626a 6563 745f 626f  er.get_object_bo
+000008d0: 6479 6301 0000 0000 0000 0000 0000 0001  dyc.............
+000008e0: 0000 0003 0000 0043 0000 0072 2100 0000  .......C...r!...
+000008f0: 7222 0000 0072 2300 0000 721a 0000 0072  r"...r#...r....r
+00000900: 1600 0000 7216 0000 0072 1700 0000 7224  ....r....r....r$
+00000910: 0000 0033 0000 0072 2500 0000 7a2c 496e  ...3...r%...z,In
+00000920: 636c 7564 6541 7070 5572 6c54 6f52 6f6f  cludeAppUrlToRoo
+00000930: 7455 726c 5772 6974 6572 2e67 6574 5f66  tUrlWriter.get_f
+00000940: 756c 6c5f 7374 7269 6e67 4e29 0872 2600  ull_stringN).r&.
+00000950: 0000 7227 0000 0072 2800 0000 7218 0000  ..r'...r(...r...
+00000960: 0072 1b00 0000 722d 0000 0072 2000 0000  .r....r-...r ...
+00000970: 7224 0000 0072 1600 0000 7216 0000 0072  r$...r....r....r
+00000980: 1600 0000 7217 0000 0072 2900 0000 1f00  ....r....r).....
+00000990: 0000 730c 0000 0008 0008 0208 0408 0308  ..s.............
+000009a0: 040c 0772 2900 0000 6300 0000 0000 0000  ...r)...c.......
+000009b0: 0000 0000 0000 0000 0004 0000 0040 0000  .............@..
+000009c0: 0073 8200 0000 6500 5a01 6400 5a02 641f  .s....e.Z.d.Z.d.
+000009d0: 6420 6404 6405 8405 5a03 6406 6504 6402  d d.d...Z.d.e.d.
+000009e0: 6403 6604 6407 6408 8404 5a05 6409 640a  d.f.d.d...Z.d.d.
+000009f0: 8400 5a06 640b 640c 8400 5a07 640d 640e  ..Z.d.d...Z.d.d.
+00000a00: 8400 5a08 640f 6410 8400 5a09 6411 6412  ..Z.d.d...Z.d.d.
+00000a10: 8400 5a0a 6413 6414 8400 5a0b 6415 6416  ..Z.d.d...Z.d.d.
+00000a20: 8400 5a0c 6417 6418 8400 5a0d 6419 641a  ..Z.d.d...Z.d.d.
+00000a30: 8400 5a0e 641b 641c 8400 5a0f 641d 641e  ..Z.d.d...Z.d.d.
+00000a40: 8400 5a10 6403 5300 2921 da09 5772 6974  ..Z.d.S.)!..Writ
+00000a50: 6541 7070 7346 da06 7265 7475 726e 4e63  eAppsF..returnNc
+00000a60: 0400 0000 0000 0000 0000 0000 0400 0000  ................
+00000a70: 0300 0000 4300 0000 732a 0000 007c 017c  ....C...s*...|.|
+00000a80: 005f 007c 027c 005f 017c 037c 005f 0264  ._.|.|._.|.|._.d
+00000a90: 0164 0284 007c 01a0 03a1 0044 0083 017c  .d...|.....D...|
+00000aa0: 005f 0464 0053 0029 034e 6301 0000 0000  ._.d.S.).Nc.....
+00000ab0: 0000 0000 0000 0003 0000 0004 0000 0053  ...............S
+00000ac0: 0000 0073 1400 0000 6700 7c00 5d06 5c02  ...s....g.|.].\.
+00000ad0: 7d01 7d02 7c01 9102 7102 5300 7216 0000  }.}.|...q.S.r...
+00000ae0: 0072 1600 0000 2903 da02 2e30 722c 0000  .r....)....0r,..
+00000af0: 00da 0576 616c 7565 7216 0000 0072 1600  ...valuer....r..
+00000b00: 0000 7217 0000 00da 0a3c 6c69 7374 636f  ..r......<listco
+00000b10: 6d70 3e3e 0000 0073 0200 0000 1400 7a26  mp>>...s......z&
+00000b20: 5772 6974 6541 7070 732e 5f5f 696e 6974  WriteApps.__init
+00000b30: 5f5f 2e3c 6c6f 6361 6c73 3e2e 3c6c 6973  __.<locals>.<lis
+00000b40: 7463 6f6d 703e 2905 da04 6170 7073 da14  tcomp>)...apps..
+00000b50: 7772 6974 655f 7465 6d70 6c61 7465 5f76  write_template_v
+00000b60: 6965 7773 da0f 7772 6974 655f 6170 695f  iews..write_api_
+00000b70: 7669 6577 73da 0569 7465 6d73 da0f 6c6f  views..items..lo
+00000b80: 6361 6c5f 6170 705f 6e61 6d65 7329 0472  cal_app_names).r
+00000b90: 1400 0000 7235 0000 0072 3600 0000 7237  ....r5...r6...r7
+00000ba0: 0000 0072 1600 0000 7216 0000 0072 1700  ...r....r....r..
+00000bb0: 0000 7218 0000 003a 0000 0073 0800 0000  ..r....:...s....
+00000bc0: 0601 0601 0601 1801 7a12 5772 6974 6541  ........z.WriteA
+00000bd0: 7070 732e 5f5f 696e 6974 5f5f 722c 0000  pps.__init__r,..
+00000be0: 0063 0200 0000 0000 0000 0000 0000 0200  .c..............
+00000bf0: 0000 0600 0000 4300 0000 731a 0000 0074  ......C...s....t
+00000c00: 00a0 0164 017c 019b 0064 027c 019b 009d  ...d.|...d.|....
+00000c10: 04a1 0101 0064 0053 0029 034e 7a07 726d  .....d.S.).Nz.rm
+00000c20: 202d 7266 207a 1e20 2626 2070 7974 686f   -rf z. && pytho
+00000c30: 6e20 6d61 6e61 6765 2e70 7920 7374 6172  n manage.py star
+00000c40: 7461 7070 2029 02da 026f 73da 0673 7973  tapp )...os..sys
+00000c50: 7465 6d72 2b00 0000 7216 0000 0072 1600  temr+...r....r..
+00000c60: 0000 7217 0000 00da 0973 7461 7274 5f61  ..r......start_a
+00000c70: 7070 4000 0000 7302 0000 001a 017a 1357  pp@...s......z.W
+00000c80: 7269 7465 4170 7073 2e73 7461 7274 5f61  riteApps.start_a
+00000c90: 7070 6301 0000 0000 0000 0000 0000 0003  ppc.............
+00000ca0: 0000 0004 0000 0043 0000 0073 2200 0000  .......C...s"...
+00000cb0: 7c00 6a00 a001 a100 4400 5d09 5c02 7d01  |.j.....D.].\.}.
+00000cc0: 7d02 7c00 a002 7c01 a101 0100 7105 6400  }.|...|.....q.d.
+00000cd0: 5300 7222 0000 0029 0372 3500 0000 7238  S.r"...).r5...r8
+00000ce0: 0000 0072 3c00 0000 a903 7214 0000 0072  ...r<.....r....r
+00000cf0: 2c00 0000 7233 0000 0072 1600 0000 7216  ,...r3...r....r.
+00000d00: 0000 0072 1700 0000 da12 6372 6561 7465  ...r......create
+00000d10: 5f61 7070 5f66 6f6c 6465 7273 4300 0000  _app_foldersC...
+00000d20: 7306 0000 0012 010c 0104 ff7a 1c57 7269  s..........z.Wri
+00000d30: 7465 4170 7073 2e63 7265 6174 655f 6170  teApps.create_ap
+00000d40: 705f 666f 6c64 6572 7363 0100 0000 0000  p_foldersc......
+00000d50: 0000 0000 0000 0300 0000 0400 0000 4300  ..............C.
+00000d60: 0000 7324 0000 007c 006a 00a0 01a1 0044  ..s$...|.j.....D
+00000d70: 005d 0a5c 027d 017d 0274 027c 017c 006a  .].\.}.}.t.|.|.j
+00000d80: 0383 0201 0071 0564 0053 0072 2200 0000  .....q.d.S.r"...
+00000d90: 2904 7235 0000 0072 3800 0000 7208 0000  ).r5...r8...r...
+00000da0: 0072 3700 0000 723d 0000 0072 1600 0000  .r7...r=...r....
+00000db0: 7216 0000 0072 1700 0000 da21 696e 6974  r....r.....!init
+00000dc0: 6961 7465 5f61 7070 5f75 726c 735f 616e  iate_app_urls_an
+00000dd0: 645f 7669 6577 735f 6669 6c65 7347 0000  d_views_filesG..
+00000de0: 0073 0600 0000 1201 0e01 04ff 7a2b 5772  .s..........z+Wr
+00000df0: 6974 6541 7070 732e 696e 6974 6961 7465  iteApps.initiate
+00000e00: 5f61 7070 5f75 726c 735f 616e 645f 7669  _app_urls_and_vi
+00000e10: 6577 735f 6669 6c65 7363 0100 0000 0000  ews_filesc......
+00000e20: 0000 0000 0000 0400 0000 0400 0000 4300  ..............C.
+00000e30: 0000 732e 0000 007c 006a 00a0 01a1 0044  ..s....|.j.....D
+00000e40: 005d 0f5c 027d 017d 027c 0264 0119 007d  .].\.}.}.|.d...}
+00000e50: 0374 027c 017c 0383 02a0 03a1 0001 0071  .t.|.|.........q
+00000e60: 0564 0053 00a9 024e da06 6d6f 6465 6c73  .d.S...N..models
+00000e70: 2904 7235 0000 0072 3800 0000 7207 0000  ).r5...r8...r...
+00000e80: 00da 0c77 7269 7465 5f6f 626a 6563 74a9  ...write_object.
+00000e90: 0472 1400 0000 722c 0000 0072 3300 0000  .r....r,...r3...
+00000ea0: 7241 0000 0072 1600 0000 7216 0000 0072  rA...r....r....r
+00000eb0: 1700 0000 da0c 7772 6974 655f 6d6f 6465  ......write_mode
+00000ec0: 6c73 4b00 0000 7308 0000 0012 0108 0110  lsK...s.........
+00000ed0: 0104 fe7a 1657 7269 7465 4170 7073 2e77  ...z.WriteApps.w
+00000ee0: 7269 7465 5f6d 6f64 656c 7363 0100 0000  rite_modelsc....
+00000ef0: 0000 0000 0000 0000 0200 0000 0200 0000  ................
+00000f00: 4300 0000 7326 0000 007c 006a 007d 017c  C...s&...|.j.}.|
+00000f10: 006a 0173 097c 006a 0272 1174 037c 0183  .j.s.|.j.r.t.|..
+00000f20: 01a0 04a1 0001 0064 0053 0064 0053 0072  .......d.S.d.S.r
+00000f30: 2200 0000 2905 7239 0000 0072 3700 0000  "...).r9...r7...
+00000f40: 7236 0000 0072 2900 0000 7242 0000 0072  r6...r)...rB...r
+00000f50: 2a00 0000 7216 0000 0072 1600 0000 7217  *...r....r....r.
+00000f60: 0000 00da 1069 6e63 6c75 6465 5f61 7070  .....include_app
+00000f70: 5f75 726c 7350 0000 0073 0800 0000 0601  _urlsP...s......
+00000f80: 0c01 1001 04ff 7a1a 5772 6974 6541 7070  ......z.WriteApp
+00000f90: 732e 696e 636c 7564 655f 6170 705f 7572  s.include_app_ur
+00000fa0: 6c73 6301 0000 0000 0000 0000 0000 0002  lsc.............
+00000fb0: 0000 0003 0000 0043 0000 0073 3400 0000  .......C...s4...
+00000fc0: 7c00 6a00 a001 a100 7d01 7c00 6a02 720d  |.j.....}.|.j.r.
+00000fd0: 7c01 a003 6401 a101 0100 7c01 a003 6402  |...d.....|...d.
+00000fe0: a101 0100 7404 7c01 8301 a005 a100 0100  ....t.|.........
+00000ff0: 6400 5300 2903 4eda 0e72 6573 745f 6672  d.S.).N..rest_fr
+00001000: 616d 6577 6f72 6bda 0864 7266 5f79 6173  amework..drf_yas
+00001010: 6729 0672 3900 0000 da04 636f 7079 7237  g).r9.....copyr7
+00001020: 0000 00da 0661 7070 656e 6472 0d00 0000  .....appendr....
+00001030: 7242 0000 0072 2a00 0000 7216 0000 0072  rB...r*...r....r
+00001040: 1600 0000 7217 0000 00da 1769 6e63 6c75  ....r......inclu
+00001050: 6465 5f61 7070 5f74 6f5f 7365 7474 696e  de_app_to_settin
+00001060: 6773 5500 0000 730a 0000 000a 0106 010a  gsU...s.........
+00001070: 010a 0110 027a 2157 7269 7465 4170 7073  .....z!WriteApps
+00001080: 2e69 6e63 6c75 6465 5f61 7070 5f74 6f5f  .include_app_to_
+00001090: 7365 7474 696e 6773 6301 0000 0000 0000  settingsc.......
+000010a0: 0000 0000 0004 0000 0004 0000 0043 0000  .............C..
+000010b0: 00f3 3800 0000 7c00 6a00 7218 7c00 6a01  ..8...|.j.r.|.j.
+000010c0: a002 a100 4400 5d11 5c02 7d01 7d02 7c02  ....D.].\.}.}.|.
+000010d0: 6401 1900 7d03 7403 7c01 7c03 8302 a004  d...}.t.|.|.....
+000010e0: a100 0100 7108 6400 5300 6400 5300 7240  ....q.d.S.d.S.r@
+000010f0: 0000 0029 0572 3600 0000 7235 0000 0072  ...).r6...r5...r
+00001100: 3800 0000 7205 0000 0072 4200 0000 7243  8...r....rB...rC
+00001110: 0000 0072 1600 0000 7216 0000 0072 1700  ...r....r....r..
+00001120: 0000 da0f 7772 6974 655f 6170 705f 7669  ....write_app_vi
+00001130: 6577 735d 0000 00f3 0c00 0000 0601 1201  ews]............
+00001140: 0801 1001 04fd 0401 7a19 5772 6974 6541  ........z.WriteA
+00001150: 7070 732e 7772 6974 655f 6170 705f 7669  pps.write_app_vi
+00001160: 6577 7363 0100 0000 0000 0000 0000 0000  ewsc............
+00001170: 0400 0000 0400 0000 4300 0000 724b 0000  ........C...rK..
+00001180: 0072 4000 0000 2905 7236 0000 0072 3500  .r@...).r6...r5.
+00001190: 0000 7238 0000 0072 0300 0000 7242 0000  ..r8...r....rB..
+000011a0: 0072 4300 0000 7216 0000 0072 1600 0000  .rC...r....r....
+000011b0: 7217 0000 00da 0a77 7269 7465 5f75 726c  r......write_url
+000011c0: 7363 0000 0072 4d00 0000 7a14 5772 6974  sc...rM...z.Writ
+000011d0: 6541 7070 732e 7772 6974 655f 7572 6c73  eApps.write_urls
+000011e0: 6301 0000 0000 0000 0000 0000 0004 0000  c...............
+000011f0: 0004 0000 0043 0000 0072 4b00 0000 7240  .....C...rK...r@
+00001200: 0000 0029 0572 3700 0000 7235 0000 0072  ...).r7...r5...r
+00001210: 3800 0000 7204 0000 0072 4200 0000 7243  8...r....rB...rC
+00001220: 0000 0072 1600 0000 7216 0000 0072 1700  ...r....r....r..
+00001230: 0000 da0e 7772 6974 655f 6170 695f 7572  ....write_api_ur
+00001240: 6c73 6900 0000 730c 0000 0006 0112 0208  lsi...s.........
+00001250: 0110 0104 fc04 027a 1857 7269 7465 4170  .......z.WriteAp
+00001260: 7073 2e77 7269 7465 5f61 7069 5f75 726c  ps.write_api_url
+00001270: 7363 0100 0000 0000 0000 0000 0000 0400  sc..............
+00001280: 0000 0400 0000 4300 0000 724b 0000 0072  ......C...rK...r
+00001290: 4000 0000 2905 7237 0000 0072 3500 0000  @...).r7...r5...
+000012a0: 7238 0000 0072 0b00 0000 7242 0000 0072  r8...r....rB...r
+000012b0: 4300 0000 7216 0000 0072 1600 0000 7217  C...r....r....r.
+000012c0: 0000 00da 1177 7269 7465 5f73 6572 6961  .....write_seria
+000012d0: 6c69 7a65 7273 7200 0000 724d 0000 007a  lizersr...rM...z
+000012e0: 1b57 7269 7465 4170 7073 2e77 7269 7465  .WriteApps.write
+000012f0: 5f73 6572 6961 6c69 7a65 7273 6301 0000  _serializersc...
+00001300: 0000 0000 0000 0000 0004 0000 0004 0000  ................
+00001310: 0043 0000 0072 4b00 0000 7240 0000 0029  .C...rK...r@...)
+00001320: 0572 3700 0000 7235 0000 0072 3800 0000  .r7...r5...r8...
+00001330: 7206 0000 0072 4200 0000 7243 0000 0072  r....rB...rC...r
+00001340: 1600 0000 7216 0000 0072 1700 0000 da13  ....r....r......
+00001350: 7772 6974 655f 6170 705f 6170 695f 7669  write_app_api_vi
+00001360: 6577 7378 0000 0072 4d00 0000 7a1d 5772  ewsx...rM...z.Wr
+00001370: 6974 6541 7070 732e 7772 6974 655f 6170  iteApps.write_ap
+00001380: 705f 6170 695f 7669 6577 7363 0100 0000  p_api_viewsc....
+00001390: 0000 0000 0000 0000 0500 0000 0400 0000  ................
+000013a0: 4300 0000 73c0 0000 0074 0083 007d 017c  C...s....t...}.|
+000013b0: 01a0 01a1 0001 007c 00a0 02a1 0001 007c  .......|.......|
+000013c0: 01a0 0364 0164 02a1 0201 007c 006a 0472  ...d.d.....|.j.r
+000013d0: 1a7c 01a0 0364 0364 04a1 0201 0074 05a0  .|...d.d.....t..
+000013e0: 0664 05a1 0101 0074 0783 007d 027c 02a0  .d.....t...}.|..
+000013f0: 08a1 0001 007c 00a0 09a1 0001 007c 00a0  .....|.......|..
+00001400: 0aa1 0001 007c 00a0 0ba1 0001 007c 006a  .....|.......|.j
+00001410: 0ca0 0da1 0044 005d 1c5c 027d 037d 047c  .....D.].\.}.}.|
+00001420: 00a0 0ea1 0001 007c 00a0 0fa1 0001 007c  .......|.......|
+00001430: 00a0 10a1 0001 007c 00a0 11a1 0001 007c  .......|.......|
+00001440: 00a0 12a1 0001 007c 00a0 13a1 0001 0071  .......|.......q
+00001450: 3774 05a0 0664 06a1 0101 0074 05a0 0664  7t...d.....t...d
+00001460: 07a1 0101 0064 0053 0029 084e 7247 0000  .....d.S.).NrG..
+00001470: 007a 0631 2e32 312e 35da 1364 6a61 6e67  .z.1.21.5..djang
+00001480: 6f72 6573 7466 7261 6d65 776f 726b 7a06  orestframeworkz.
+00001490: 332e 3134 2e30 7a1f 7069 7020 696e 7374  3.14.0z.pip inst
+000014a0: 616c 6c20 2d72 2072 6571 7569 7265 6d65  all -r requireme
+000014b0: 6e74 732e 7478 747a 2070 7974 686f 6e33  nts.txtz python3
+000014c0: 206d 616e 6167 652e 7079 206d 616b 656d   manage.py makem
+000014d0: 6967 7261 7469 6f6e 737a 1970 7974 686f  igrationsz.pytho
+000014e0: 6e33 206d 616e 6167 652e 7079 206d 6967  n3 manage.py mig
+000014f0: 7261 7465 2914 7209 0000 00da 1477 7269  rate).r......wri
+00001500: 7465 5f67 6974 6967 6e6f 7265 5f66 696c  te_gitignore_fil
+00001510: 6572 3e00 0000 da26 7772 6974 655f 6e65  er>....&write_ne
+00001520: 775f 7061 636b 6167 655f 696e 5f72 6571  w_package_in_req
+00001530: 7569 7265 6d65 6e74 735f 7465 7874 7237  uirements_textr7
+00001540: 0000 0072 3a00 0000 723b 0000 0072 0c00  ...r:...r;...r..
+00001550: 0000 da17 7772 6974 655f 646f 6375 6d65  ....write_docume
+00001560: 6e74 6174 696f 6e5f 7572 6c72 3f00 0000  ntation_urlr?...
+00001570: 724a 0000 0072 4500 0000 7235 0000 0072  rJ...rE...r5...r
+00001580: 3800 0000 7244 0000 0072 4c00 0000 724e  8...rD...rL...rN
+00001590: 0000 0072 5000 0000 7251 0000 0072 4f00  ...rP...rQ...rO.
+000015a0: 0000 2905 7214 0000 00da 0b66 696c 655f  ..).r......file_
+000015b0: 7772 6974 6572 da0a 646f 635f 7772 6974  writer..doc_writ
+000015c0: 6572 722c 0000 0072 3300 0000 7216 0000  err,...r3...r...
+000015d0: 0072 1600 0000 7217 0000 00da 0577 7269  .r....r......wri
+000015e0: 7465 7f00 0000 732a 0000 0006 0108 0108  te....s*........
+000015f0: 010c 0106 010c 010a 0106 0308 0108 0108  ................
+00001600: 0108 0112 0208 0108 0108 0108 0108 010a  ................
+00001610: 010a 020e 017a 0f57 7269 7465 4170 7073  .....z.WriteApps
+00001620: 2e77 7269 7465 2902 4646 2902 7231 0000  .write).FF).r1..
+00001630: 004e 2911 7226 0000 0072 2700 0000 7228  .N).r&...r'...r(
+00001640: 0000 0072 1800 0000 da03 7374 7272 3c00  ...r......strr<.
+00001650: 0000 723e 0000 0072 3f00 0000 7244 0000  ..r>...r?...rD..
+00001660: 0072 4500 0000 724a 0000 0072 4c00 0000  .rE...rJ...rL...
+00001670: 724e 0000 0072 4f00 0000 7250 0000 0072  rN...rO...rP...r
+00001680: 5100 0000 7258 0000 0072 1600 0000 7216  Q...rX...r....r.
+00001690: 0000 0072 1600 0000 7217 0000 0072 3000  ...r....r....r0.
+000016a0: 0000 3900 0000 731c 0000 0008 000c 0112  ..9...s.........
+000016b0: 0608 0308 0408 0408 0508 0508 0808 0608  ................
+000016c0: 0608 0908 060c 0772 3000 0000 2918 723a  .......r0...).r:
+000016d0: 0000 00da 0b64 6a61 6e67 6f2e 636f 6e66  .....django.conf
+000016e0: 7202 0000 00da 1c63 6f64 656c 6573 735f  r......codeless_
+000016f0: 646a 616e 676f 2e77 7269 7465 7273 2e75  django.writers.u
+00001700: 726c 7372 0300 0000 7204 0000 00da 1d63  rlsr....r......c
+00001710: 6f64 656c 6573 735f 646a 616e 676f 2e77  odeless_django.w
+00001720: 7269 7465 7273 2e76 6965 7773 7205 0000  riters.viewsr...
+00001730: 00da 1c63 6f64 656c 6573 735f 646a 616e  ...codeless_djan
+00001740: 676f 2e77 7269 7465 7273 2e61 7069 7372  go.writers.apisr
+00001750: 0600 0000 da1e 636f 6465 6c65 7373 5f64  ......codeless_d
+00001760: 6a61 6e67 6f2e 7772 6974 6572 732e 6d6f  jango.writers.mo
+00001770: 6465 6c73 7207 0000 00da 1d63 6f64 656c  delsr......codel
+00001780: 6573 735f 646a 616e 676f 2e77 7269 7465  ess_django.write
+00001790: 7273 2e66 696c 6573 7208 0000 0072 0900  rs.filesr....r..
+000017a0: 0000 da1c 636f 6465 6c65 7373 5f64 6a61  ....codeless_dja
+000017b0: 6e67 6f2e 7772 6974 6572 732e 6261 7365  ngo.writers.base
+000017c0: 720a 0000 00da 2363 6f64 656c 6573 735f  r.....#codeless_
+000017d0: 646a 616e 676f 2e77 7269 7465 7273 2e73  django.writers.s
+000017e0: 6572 6961 6c69 7a65 7273 720b 0000 00da  erializersr.....
+000017f0: 2563 6f64 656c 6573 735f 646a 616e 676f  %codeless_django
+00001800: 2e77 7269 7465 7273 2e64 6f63 756d 656e  .writers.documen
+00001810: 7461 7469 6f6e 720c 0000 0072 0d00 0000  tationr....r....
+00001820: 7229 0000 0072 3000 0000 7216 0000 0072  r)...r0...r....r
+00001830: 1600 0000 7216 0000 0072 1700 0000 da08  ....r....r......
+00001840: 3c6d 6f64 756c 653e 0100 0000 731c 0000  <module>....s...
+00001850: 0008 000c 0110 010c 010c 010c 0110 010c  ................
+00001860: 010c 010c 010c 0110 0210 1212 1a         .............
```

### Comparing `codeless-django-0.0.14/codeless_django/writers/__pycache__/base.cpython-310.pyc` & `codeless-django-0.0.15/codeless_django/writers/__pycache__/base.cpython-310.pyc`

 * *Format-specific differences are supported for Python .pyc files but no file-specific differences were detected; falling back to a binary diff. file(1) reports: Byte-compiled Python module for CPython 3.10, timestamp-based, .py timestamp: Sun May 21 00:58:02 2023 UTC, .py size: 1248 bytes*

 * *Could not decompile bytecode: bad marshal data (unknown type code)*

 * *Files 3% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-00000000: 6f0d 0d0a 0000 0000 9a6c 6964 e004 0000  o........lid....
+00000000: 6f0d 0d0a 0000 0000 6f28 bd64 e004 0000  o.......o(.d....
 00000010: e300 0000 0000 0000 0000 0000 0000 0000  ................
 00000020: 0004 0000 0040 0000 0073 5400 0000 6400  .....@...sT...d.
 00000030: 6401 6c00 6d01 5a01 6d02 5a02 0100 4700  d.l.m.Z.m.Z...G.
 00000040: 6402 6403 8400 6403 6501 8303 5a03 4700  d.d...d.e...Z.G.
 00000050: 6404 6405 8400 6405 6501 8303 5a04 4700  d.d...d.e...Z.G.
 00000060: 6406 6407 8400 6407 6504 8303 5a05 4700  d.d...d.e...Z.G.
 00000070: 6408 6409 8400 6409 6504 8303 5a06 640a  d.d...d.e...Z.d.
@@ -13,154 +13,156 @@
 000000c0: 5a01 6400 5a02 6503 6401 6402 8400 8301  Z.d.Z.e.d.d.....
 000000d0: 5a04 6503 6403 6404 8400 8301 5a05 6405  Z.e.d.d.....Z.d.
 000000e0: 6406 8400 5a06 6407 5300 2908 da0b 4261  d...Z.d.S.)...Ba
 000000f0: 7365 4275 696c 6465 7263 0100 0000 0000  seBuilderc......
 00000100: 0000 0000 0000 0100 0000 0100 0000 4300  ..............C.
 00000110: 0000 f304 0000 0064 0053 00a9 014e a900  .......d.S...N..
 00000120: a901 da04 7365 6c66 7207 0000 0072 0700  ....selfr....r..
-00000130: 0000 fa37 2f68 6f6d 652f 6f6d 6172 2f63  ...7/home/omar/c
-00000140: 6f64 652f 5175 6963 6b44 6a2f 636f 6465  ode/QuickDj/code
-00000150: 6c65 7373 5f64 6a61 6e67 6f2f 7772 6974  less_django/writ
-00000160: 6572 732f 6261 7365 2e70 79da 1167 6574  ers/base.py..get
-00000170: 5f6f 626a 6563 745f 6865 6164 6572 0500  _object_header..
-00000180: 0000 f302 0000 0004 027a 1d42 6173 6542  .........z.BaseB
-00000190: 7569 6c64 6572 2e67 6574 5f6f 626a 6563  uilder.get_objec
-000001a0: 745f 6865 6164 6572 6301 0000 0000 0000  t_headerc.......
-000001b0: 0000 0000 0001 0000 0001 0000 0043 0000  .............C..
-000001c0: 0072 0500 0000 7206 0000 0072 0700 0000  .r....r....r....
-000001d0: 7208 0000 0072 0700 0000 7207 0000 0072  r....r....r....r
-000001e0: 0a00 0000 da0f 6765 745f 6f62 6a65 6374  ......get_object
-000001f0: 5f62 6f64 7909 0000 0072 0c00 0000 7a1b  _body....r....z.
-00000200: 4261 7365 4275 696c 6465 722e 6765 745f  BaseBuilder.get_
-00000210: 6f62 6a65 6374 5f62 6f64 7963 0100 0000  object_bodyc....
-00000220: 0000 0000 0000 0000 0100 0000 0300 0000  ................
-00000230: 4300 0000 7314 0000 007c 00a0 00a1 007c  C...s....|.....|
-00000240: 00a0 01a1 0017 0064 0117 0053 0029 024e  .......d...S.).N
-00000250: da01 0a29 0272 0b00 0000 720d 0000 0072  ...).r....r....r
-00000260: 0800 0000 7207 0000 0072 0700 0000 720a  ....r....r....r.
-00000270: 0000 00da 1167 6574 5f6f 626a 6563 745f  .....get_object_
-00000280: 7374 7269 6e67 0d00 0000 7302 0000 0014  string....s.....
-00000290: 017a 1d42 6173 6542 7569 6c64 6572 2e67  .z.BaseBuilder.g
-000002a0: 6574 5f6f 626a 6563 745f 7374 7269 6e67  et_object_string
-000002b0: 4e29 07da 085f 5f6e 616d 655f 5fda 0a5f  N)...__name__.._
-000002c0: 5f6d 6f64 756c 655f 5fda 0c5f 5f71 7561  _module__..__qua
-000002d0: 6c6e 616d 655f 5f72 0300 0000 720b 0000  lname__r....r...
-000002e0: 0072 0d00 0000 720f 0000 0072 0700 0000  .r....r....r....
-000002f0: 7207 0000 0072 0700 0000 720a 0000 0072  r....r....r....r
-00000300: 0400 0000 0300 0000 730c 0000 0008 0002  ........s.......
-00000310: 020a 0102 030a 010c 0372 0400 0000 6300  .........r....c.
-00000320: 0000 0000 0000 0000 0000 0000 0000 0002  ................
-00000330: 0000 0040 0000 0073 2400 0000 6500 5a01  ...@...s$...e.Z.
-00000340: 6400 5a02 6401 6402 8400 5a03 6403 6404  d.Z.d.d...Z.d.d.
-00000350: 8400 5a04 6405 6406 8400 5a05 6407 5300  ..Z.d.d...Z.d.S.
-00000360: 2908 da0a 4261 7365 5772 6974 6572 6302  )...BaseWriterc.
-00000370: 0000 0000 0000 0000 0000 0002 0000 0002  ................
-00000380: 0000 0043 0000 0073 0a00 0000 7c01 7c00  ...C...s....|.|.
-00000390: 5f00 6400 5300 7206 0000 0029 01da 0966  _.d.S.r....)...f
-000003a0: 696c 655f 6e61 6d65 2902 7209 0000 0072  ile_name).r....r
-000003b0: 1400 0000 7207 0000 0072 0700 0000 720a  ....r....r....r.
-000003c0: 0000 00da 085f 5f69 6e69 745f 5f14 0000  .....__init__...
-000003d0: 0073 0200 0000 0a01 7a13 4261 7365 5772  .s......z.BaseWr
-000003e0: 6974 6572 2e5f 5f69 6e69 745f 5f63 0100  iter.__init__c..
-000003f0: 0000 0000 0000 0000 0000 0100 0000 0100  ................
-00000400: 0000 4300 0000 7205 0000 0072 0600 0000  ..C...r....r....
-00000410: 7207 0000 0072 0800 0000 7207 0000 0072  r....r....r....r
-00000420: 0700 0000 720a 0000 00da 0f67 6574 5f66  ....r......get_f
-00000430: 756c 6c5f 7374 7269 6e67 1a00 0000 f302  ull_string......
-00000440: 0000 0004 017a 1a42 6173 6557 7269 7465  .....z.BaseWrite
-00000450: 722e 6765 745f 6675 6c6c 5f73 7472 696e  r.get_full_strin
-00000460: 6763 0100 0000 0000 0000 0000 0000 0200  gc..............
-00000470: 0000 0800 0000 4300 0000 7340 0000 0074  ......C...s@...t
-00000480: 007c 006a 0164 0183 028f 107d 017c 01a0  .|.j.d.....}.|..
-00000490: 027c 00a0 03a1 00a1 0101 0057 0064 0004  .|.........W.d..
-000004a0: 0004 0083 0301 0064 0053 0031 0073 1977  .......d.S.1.s.w
-000004b0: 0101 0001 0001 0059 0001 0064 0053 0029  .......Y...d.S.)
-000004c0: 024e da01 6129 04da 046f 7065 6e72 1400  .N..a)...openr..
-000004d0: 0000 da05 7772 6974 6572 1600 0000 2902  ....writer....).
-000004e0: 7209 0000 00da 0166 7207 0000 0072 0700  r......fr....r..
-000004f0: 0000 720a 0000 00da 0c77 7269 7465 5f6f  ..r......write_o
-00000500: 626a 6563 741d 0000 0073 0600 0000 0e01  bject....s......
-00000510: 1001 22ff 7a17 4261 7365 5772 6974 6572  ..".z.BaseWriter
-00000520: 2e77 7269 7465 5f6f 626a 6563 744e 2906  .write_objectN).
-00000530: 7210 0000 0072 1100 0000 7212 0000 0072  r....r....r....r
-00000540: 1500 0000 7216 0000 0072 1c00 0000 7207  ....r....r....r.
-00000550: 0000 0072 0700 0000 7207 0000 0072 0a00  ...r....r....r..
-00000560: 0000 7213 0000 0012 0000 0073 0800 0000  ..r........s....
-00000570: 0800 0802 0806 0c03 7213 0000 0063 0000  ........r....c..
-00000580: 0000 0000 0000 0000 0000 0000 0000 0300  ................
-00000590: 0000 0000 0000 731c 0000 0065 005a 0164  ......s....e.Z.d
-000005a0: 005a 0287 0066 0164 0164 0284 085a 0387  .Z...f.d.d...Z..
-000005b0: 0004 005a 0453 0029 03da 0e42 6173 6556  ...Z.S.)...BaseV
-000005c0: 6965 7757 7269 7465 7263 0300 0000 0000  iewWriterc......
-000005d0: 0000 0000 0000 0400 0000 0500 0000 0300  ................
-000005e0: 0000 f31a 0000 007c 019b 0064 019d 027d  .......|...d...}
-000005f0: 0374 0083 00a0 017c 017c 027c 03a1 0353  .t.....|.|.|...S
-00000600: 0029 024e 7a09 2f76 6965 7773 2e70 79a9  .).Nz./views.py.
-00000610: 02da 0573 7570 6572 7215 0000 00a9 0472  ...superr......r
-00000620: 0900 0000 da08 6170 705f 6e61 6d65 da0a  ......app_name..
-00000630: 6d6f 6465 6c5f 6e61 6d65 7214 0000 00a9  model_namer.....
-00000640: 01da 095f 5f63 6c61 7373 5f5f 7207 0000  ...__class__r...
-00000650: 0072 0a00 0000 7215 0000 0024 0000 00f3  .r....r....$....
-00000660: 0400 0000 0a01 1001 7a17 4261 7365 5669  ........z.BaseVi
-00000670: 6577 5772 6974 6572 2e5f 5f69 6e69 745f  ewWriter.__init_
-00000680: 5f29 0572 1000 0000 7211 0000 0072 1200  _).r....r....r..
-00000690: 0000 7215 0000 00da 0d5f 5f63 6c61 7373  ..r......__class
-000006a0: 6365 6c6c 5f5f 7207 0000 0072 0700 0000  cell__r....r....
-000006b0: 7224 0000 0072 0a00 0000 721d 0000 0022  r$...r....r...."
-000006c0: 0000 0073 0400 0000 0800 1402 721d 0000  ...s........r...
-000006d0: 0063 0000 0000 0000 0000 0000 0000 0000  .c..............
-000006e0: 0000 0300 0000 0000 0000 7340 0000 0065  ..........s@...e
-000006f0: 005a 0164 005a 0287 0066 0164 0164 0284  .Z.d.Z...f.d.d..
-00000700: 085a 0364 0364 0484 005a 0464 0564 0684  .Z.d.d...Z.d.d..
-00000710: 005a 0565 0664 0764 0884 0083 015a 0764  .Z.e.d.d.....Z.d
-00000720: 0964 0a84 005a 0887 0004 005a 0953 0029  .d...Z.....Z.S.)
-00000730: 0bda 0d42 6173 6555 524c 5772 6974 6572  ...BaseURLWriter
-00000740: 6303 0000 0000 0000 0000 0000 0004 0000  c...............
-00000750: 0005 0000 0003 0000 0072 1e00 0000 2902  .........r....).
-00000760: 4e7a 082f 7572 6c73 2e70 7972 1f00 0000  Nz./urls.pyr....
-00000770: 7221 0000 0072 2400 0000 7207 0000 0072  r!...r$...r....r
-00000780: 0a00 0000 7215 0000 002c 0000 0072 2600  ....r....,...r&.
-00000790: 0000 7a16 4261 7365 5552 4c57 7269 7465  ..z.BaseURLWrite
-000007a0: 722e 5f5f 696e 6974 5f5f 6301 0000 0000  r.__init__c.....
-000007b0: 0000 0000 0000 0001 0000 0001 0000 0043  ...............C
-000007c0: 0000 0072 0500 0000 7206 0000 0072 0700  ...r....r....r..
-000007d0: 0000 7208 0000 0072 0700 0000 7207 0000  ..r....r....r...
-000007e0: 0072 0a00 0000 720b 0000 0031 0000 0072  .r....r....1...r
-000007f0: 1700 0000 7a1f 4261 7365 5552 4c57 7269  ....z.BaseURLWri
-00000800: 7465 722e 6765 745f 6f62 6a65 6374 5f68  ter.get_object_h
-00000810: 6561 6465 7263 0100 0000 0000 0000 0000  eaderc..........
-00000820: 0000 0100 0000 0100 0000 4300 0000 7205  ..........C...r.
-00000830: 0000 0072 0600 0000 7207 0000 0072 0800  ...r....r....r..
-00000840: 0000 7207 0000 0072 0700 0000 720a 0000  ..r....r....r...
-00000850: 0072 0d00 0000 3500 0000 7217 0000 007a  .r....5...r....z
-00000860: 1d42 6173 6555 524c 5772 6974 6572 2e67  .BaseURLWriter.g
-00000870: 6574 5f6f 626a 6563 745f 626f 6479 6301  et_object_bodyc.
-00000880: 0000 0000 0000 0000 0000 0001 0000 0001  ................
-00000890: 0000 0043 0000 0072 0500 0000 7206 0000  ...C...r....r...
-000008a0: 0072 0700 0000 7208 0000 0072 0700 0000  .r....r....r....
-000008b0: 7207 0000 0072 0a00 0000 da0e 6765 745f  r....r......get_
-000008c0: 7572 6c5f 7374 7269 6e67 3800 0000 720c  url_string8...r.
-000008d0: 0000 007a 1c42 6173 6555 524c 5772 6974  ...z.BaseURLWrit
-000008e0: 6572 2e67 6574 5f75 726c 5f73 7472 696e  er.get_url_strin
-000008f0: 6763 0100 0000 0000 0000 0000 0000 0200  gc..............
-00000900: 0000 0200 0000 4300 0000 7314 0000 007c  ......C...s....|
-00000910: 00a0 00a1 007d 0164 017c 0117 0064 0217  .....}.d.|...d..
-00000920: 0053 0029 034e 7a10 7572 6c70 6174 7465  .S.).Nz.urlpatte
-00000930: 726e 7320 3d20 5b0a 7a02 5d0a 2901 7229  rns = [.z.].).r)
-00000940: 0000 0029 0272 0900 0000 da0a 7572 6c5f  ...).r......url_
-00000950: 7374 7269 6e67 7207 0000 0072 0700 0000  stringr....r....
-00000960: 720a 0000 0072 0f00 0000 3c00 0000 7304  r....r....<...s.
-00000970: 0000 0008 010c 017a 1f42 6173 6555 524c  .......z.BaseURL
-00000980: 5772 6974 6572 2e67 6574 5f6f 626a 6563  Writer.get_objec
-00000990: 745f 7374 7269 6e67 290a 7210 0000 0072  t_string).r....r
-000009a0: 1100 0000 7212 0000 0072 1500 0000 720b  ....r....r....r.
-000009b0: 0000 0072 0d00 0000 7203 0000 0072 2900  ...r....r....r).
-000009c0: 0000 720f 0000 0072 2700 0000 7207 0000  ..r....r'...r...
-000009d0: 0072 0700 0000 7224 0000 0072 0a00 0000  .r....r$...r....
-000009e0: 7228 0000 002b 0000 0073 0e00 0000 0800  r(...+...s......
-000009f0: 0c01 0805 0804 0203 0a01 1003 7228 0000  ............r(..
-00000a00: 004e 2907 da03 6162 6372 0200 0000 7203  .N)...abcr....r.
-00000a10: 0000 0072 0400 0000 7213 0000 0072 1d00  ...r....r....r..
-00000a20: 0000 7228 0000 0072 0700 0000 7207 0000  ..r(...r....r...
-00000a30: 0072 0700 0000 720a 0000 00da 083c 6d6f  .r....r......<mo
-00000a40: 6475 6c65 3e01 0000 0073 0a00 0000 1000  dule>....s......
-00000a50: 1002 100f 1010 1409                      ........
+00000130: 0000 fa5a 2f68 6f6d 652f 6f6d 6172 2f63  ...Z/home/omar/c
+00000140: 6f64 652f 7465 7374 2d63 6c64 2f76 656e  ode/test-cld/ven
+00000150: 762f 6c69 622f 7079 7468 6f6e 332e 3130  v/lib/python3.10
+00000160: 2f73 6974 652d 7061 636b 6167 6573 2f63  /site-packages/c
+00000170: 6f64 656c 6573 735f 646a 616e 676f 2f77  odeless_django/w
+00000180: 7269 7465 7273 2f62 6173 652e 7079 da11  riters/base.py..
+00000190: 6765 745f 6f62 6a65 6374 5f68 6561 6465  get_object_heade
+000001a0: 7205 0000 00f3 0200 0000 0402 7a1d 4261  r...........z.Ba
+000001b0: 7365 4275 696c 6465 722e 6765 745f 6f62  seBuilder.get_ob
+000001c0: 6a65 6374 5f68 6561 6465 7263 0100 0000  ject_headerc....
+000001d0: 0000 0000 0000 0000 0100 0000 0100 0000  ................
+000001e0: 4300 0000 7205 0000 0072 0600 0000 7207  C...r....r....r.
+000001f0: 0000 0072 0800 0000 7207 0000 0072 0700  ...r....r....r..
+00000200: 0000 720a 0000 00da 0f67 6574 5f6f 626a  ..r......get_obj
+00000210: 6563 745f 626f 6479 0900 0000 720c 0000  ect_body....r...
+00000220: 007a 1b42 6173 6542 7569 6c64 6572 2e67  .z.BaseBuilder.g
+00000230: 6574 5f6f 626a 6563 745f 626f 6479 6301  et_object_bodyc.
+00000240: 0000 0000 0000 0000 0000 0001 0000 0003  ................
+00000250: 0000 0043 0000 0073 1400 0000 7c00 a000  ...C...s....|...
+00000260: a100 7c00 a001 a100 1700 6401 1700 5300  ..|.......d...S.
+00000270: 2902 4eda 010a 2902 720b 0000 0072 0d00  ).N...).r....r..
+00000280: 0000 7208 0000 0072 0700 0000 7207 0000  ..r....r....r...
+00000290: 0072 0a00 0000 da11 6765 745f 6f62 6a65  .r......get_obje
+000002a0: 6374 5f73 7472 696e 670d 0000 0073 0200  ct_string....s..
+000002b0: 0000 1401 7a1d 4261 7365 4275 696c 6465  ....z.BaseBuilde
+000002c0: 722e 6765 745f 6f62 6a65 6374 5f73 7472  r.get_object_str
+000002d0: 696e 674e 2907 da08 5f5f 6e61 6d65 5f5f  ingN)...__name__
+000002e0: da0a 5f5f 6d6f 6475 6c65 5f5f da0c 5f5f  ..__module__..__
+000002f0: 7175 616c 6e61 6d65 5f5f 7203 0000 0072  qualname__r....r
+00000300: 0b00 0000 720d 0000 0072 0f00 0000 7207  ....r....r....r.
+00000310: 0000 0072 0700 0000 7207 0000 0072 0a00  ...r....r....r..
+00000320: 0000 7204 0000 0003 0000 0073 0c00 0000  ..r........s....
+00000330: 0800 0202 0a01 0203 0a01 0c03 7204 0000  ............r...
+00000340: 0063 0000 0000 0000 0000 0000 0000 0000  .c..............
+00000350: 0000 0200 0000 4000 0000 7324 0000 0065  ......@...s$...e
+00000360: 005a 0164 005a 0264 0164 0284 005a 0364  .Z.d.Z.d.d...Z.d
+00000370: 0364 0484 005a 0464 0564 0684 005a 0564  .d...Z.d.d...Z.d
+00000380: 0753 0029 08da 0a42 6173 6557 7269 7465  .S.)...BaseWrite
+00000390: 7263 0200 0000 0000 0000 0000 0000 0200  rc..............
+000003a0: 0000 0200 0000 4300 0000 730a 0000 007c  ......C...s....|
+000003b0: 017c 005f 0064 0053 0072 0600 0000 2901  .|._.d.S.r....).
+000003c0: da09 6669 6c65 5f6e 616d 6529 0272 0900  ..file_name).r..
+000003d0: 0000 7214 0000 0072 0700 0000 7207 0000  ..r....r....r...
+000003e0: 0072 0a00 0000 da08 5f5f 696e 6974 5f5f  .r......__init__
+000003f0: 1400 0000 7302 0000 000a 017a 1342 6173  ....s......z.Bas
+00000400: 6557 7269 7465 722e 5f5f 696e 6974 5f5f  eWriter.__init__
+00000410: 6301 0000 0000 0000 0000 0000 0001 0000  c...............
+00000420: 0001 0000 0043 0000 0072 0500 0000 7206  .....C...r....r.
+00000430: 0000 0072 0700 0000 7208 0000 0072 0700  ...r....r....r..
+00000440: 0000 7207 0000 0072 0a00 0000 da0f 6765  ..r....r......ge
+00000450: 745f 6675 6c6c 5f73 7472 696e 671a 0000  t_full_string...
+00000460: 00f3 0200 0000 0401 7a1a 4261 7365 5772  ........z.BaseWr
+00000470: 6974 6572 2e67 6574 5f66 756c 6c5f 7374  iter.get_full_st
+00000480: 7269 6e67 6301 0000 0000 0000 0000 0000  ringc...........
+00000490: 0002 0000 0008 0000 0043 0000 0073 4000  .........C...s@.
+000004a0: 0000 7400 7c00 6a01 6401 8302 8f10 7d01  ..t.|.j.d.....}.
+000004b0: 7c01 a002 7c00 a003 a100 a101 0100 5700  |...|.........W.
+000004c0: 6400 0400 0400 8303 0100 6400 5300 3100  d.........d.S.1.
+000004d0: 7319 7701 0100 0100 0100 5900 0100 6400  s.w.......Y...d.
+000004e0: 5300 2902 4eda 0161 2904 da04 6f70 656e  S.).N..a)...open
+000004f0: 7214 0000 00da 0577 7269 7465 7216 0000  r......writer...
+00000500: 0029 0272 0900 0000 da01 6672 0700 0000  .).r......fr....
+00000510: 7207 0000 0072 0a00 0000 da0c 7772 6974  r....r......writ
+00000520: 655f 6f62 6a65 6374 1d00 0000 7306 0000  e_object....s...
+00000530: 000e 0110 0122 ff7a 1742 6173 6557 7269  .....".z.BaseWri
+00000540: 7465 722e 7772 6974 655f 6f62 6a65 6374  ter.write_object
+00000550: 4e29 0672 1000 0000 7211 0000 0072 1200  N).r....r....r..
+00000560: 0000 7215 0000 0072 1600 0000 721c 0000  ..r....r....r...
+00000570: 0072 0700 0000 7207 0000 0072 0700 0000  .r....r....r....
+00000580: 720a 0000 0072 1300 0000 1200 0000 7308  r....r........s.
+00000590: 0000 0008 0008 0208 060c 0372 1300 0000  ...........r....
+000005a0: 6300 0000 0000 0000 0000 0000 0000 0000  c...............
+000005b0: 0003 0000 0000 0000 0073 1c00 0000 6500  .........s....e.
+000005c0: 5a01 6400 5a02 8700 6601 6401 6402 8408  Z.d.Z...f.d.d...
+000005d0: 5a03 8700 0400 5a04 5300 2903 da0e 4261  Z.....Z.S.)...Ba
+000005e0: 7365 5669 6577 5772 6974 6572 6303 0000  seViewWriterc...
+000005f0: 0000 0000 0000 0000 0004 0000 0005 0000  ................
+00000600: 0003 0000 00f3 1a00 0000 7c01 9b00 6401  ..........|...d.
+00000610: 9d02 7d03 7400 8300 a001 7c01 7c02 7c03  ..}.t.....|.|.|.
+00000620: a103 5300 2902 4e7a 092f 7669 6577 732e  ..S.).Nz./views.
+00000630: 7079 a902 da05 7375 7065 7272 1500 0000  py....superr....
+00000640: a904 7209 0000 00da 0861 7070 5f6e 616d  ..r......app_nam
+00000650: 65da 0a6d 6f64 656c 5f6e 616d 6572 1400  e..model_namer..
+00000660: 0000 a901 da09 5f5f 636c 6173 735f 5f72  ......__class__r
+00000670: 0700 0000 720a 0000 0072 1500 0000 2400  ....r....r....$.
+00000680: 0000 f304 0000 000a 0110 017a 1742 6173  ...........z.Bas
+00000690: 6556 6965 7757 7269 7465 722e 5f5f 696e  eViewWriter.__in
+000006a0: 6974 5f5f 2905 7210 0000 0072 1100 0000  it__).r....r....
+000006b0: 7212 0000 0072 1500 0000 da0d 5f5f 636c  r....r......__cl
+000006c0: 6173 7363 656c 6c5f 5f72 0700 0000 7207  asscell__r....r.
+000006d0: 0000 0072 2400 0000 720a 0000 0072 1d00  ...r$...r....r..
+000006e0: 0000 2200 0000 7304 0000 0008 0014 0272  .."...s........r
+000006f0: 1d00 0000 6300 0000 0000 0000 0000 0000  ....c...........
+00000700: 0000 0000 0003 0000 0000 0000 0073 4000  .............s@.
+00000710: 0000 6500 5a01 6400 5a02 8700 6601 6401  ..e.Z.d.Z...f.d.
+00000720: 6402 8408 5a03 6403 6404 8400 5a04 6405  d...Z.d.d...Z.d.
+00000730: 6406 8400 5a05 6506 6407 6408 8400 8301  d...Z.e.d.d.....
+00000740: 5a07 6409 640a 8400 5a08 8700 0400 5a09  Z.d.d...Z.....Z.
+00000750: 5300 290b da0d 4261 7365 5552 4c57 7269  S.)...BaseURLWri
+00000760: 7465 7263 0300 0000 0000 0000 0000 0000  terc............
+00000770: 0400 0000 0500 0000 0300 0000 721e 0000  ............r...
+00000780: 0029 024e 7a08 2f75 726c 732e 7079 721f  .).Nz./urls.pyr.
+00000790: 0000 0072 2100 0000 7224 0000 0072 0700  ...r!...r$...r..
+000007a0: 0000 720a 0000 0072 1500 0000 2c00 0000  ..r....r....,...
+000007b0: 7226 0000 007a 1642 6173 6555 524c 5772  r&...z.BaseURLWr
+000007c0: 6974 6572 2e5f 5f69 6e69 745f 5f63 0100  iter.__init__c..
+000007d0: 0000 0000 0000 0000 0000 0100 0000 0100  ................
+000007e0: 0000 4300 0000 7205 0000 0072 0600 0000  ..C...r....r....
+000007f0: 7207 0000 0072 0800 0000 7207 0000 0072  r....r....r....r
+00000800: 0700 0000 720a 0000 0072 0b00 0000 3100  ....r....r....1.
+00000810: 0000 7217 0000 007a 1f42 6173 6555 524c  ..r....z.BaseURL
+00000820: 5772 6974 6572 2e67 6574 5f6f 626a 6563  Writer.get_objec
+00000830: 745f 6865 6164 6572 6301 0000 0000 0000  t_headerc.......
+00000840: 0000 0000 0001 0000 0001 0000 0043 0000  .............C..
+00000850: 0072 0500 0000 7206 0000 0072 0700 0000  .r....r....r....
+00000860: 7208 0000 0072 0700 0000 7207 0000 0072  r....r....r....r
+00000870: 0a00 0000 720d 0000 0035 0000 0072 1700  ....r....5...r..
+00000880: 0000 7a1d 4261 7365 5552 4c57 7269 7465  ..z.BaseURLWrite
+00000890: 722e 6765 745f 6f62 6a65 6374 5f62 6f64  r.get_object_bod
+000008a0: 7963 0100 0000 0000 0000 0000 0000 0100  yc..............
+000008b0: 0000 0100 0000 4300 0000 7205 0000 0072  ......C...r....r
+000008c0: 0600 0000 7207 0000 0072 0800 0000 7207  ....r....r....r.
+000008d0: 0000 0072 0700 0000 720a 0000 00da 0e67  ...r....r......g
+000008e0: 6574 5f75 726c 5f73 7472 696e 6738 0000  et_url_string8..
+000008f0: 0072 0c00 0000 7a1c 4261 7365 5552 4c57  .r....z.BaseURLW
+00000900: 7269 7465 722e 6765 745f 7572 6c5f 7374  riter.get_url_st
+00000910: 7269 6e67 6301 0000 0000 0000 0000 0000  ringc...........
+00000920: 0002 0000 0002 0000 0043 0000 0073 1400  .........C...s..
+00000930: 0000 7c00 a000 a100 7d01 6401 7c01 1700  ..|.....}.d.|...
+00000940: 6402 1700 5300 2903 4e7a 1075 726c 7061  d...S.).Nz.urlpa
+00000950: 7474 6572 6e73 203d 205b 0a7a 025d 0a29  tterns = [.z.].)
+00000960: 0172 2900 0000 2902 7209 0000 00da 0a75  .r)...).r......u
+00000970: 726c 5f73 7472 696e 6772 0700 0000 7207  rl_stringr....r.
+00000980: 0000 0072 0a00 0000 720f 0000 003c 0000  ...r....r....<..
+00000990: 0073 0400 0000 0801 0c01 7a1f 4261 7365  .s........z.Base
+000009a0: 5552 4c57 7269 7465 722e 6765 745f 6f62  URLWriter.get_ob
+000009b0: 6a65 6374 5f73 7472 696e 6729 0a72 1000  ject_string).r..
+000009c0: 0000 7211 0000 0072 1200 0000 7215 0000  ..r....r....r...
+000009d0: 0072 0b00 0000 720d 0000 0072 0300 0000  .r....r....r....
+000009e0: 7229 0000 0072 0f00 0000 7227 0000 0072  r)...r....r'...r
+000009f0: 0700 0000 7207 0000 0072 2400 0000 720a  ....r....r$...r.
+00000a00: 0000 0072 2800 0000 2b00 0000 730e 0000  ...r(...+...s...
+00000a10: 0008 000c 0108 0508 0402 030a 0110 0372  ...............r
+00000a20: 2800 0000 4e29 07da 0361 6263 7202 0000  (...N)...abcr...
+00000a30: 0072 0300 0000 7204 0000 0072 1300 0000  .r....r....r....
+00000a40: 721d 0000 0072 2800 0000 7207 0000 0072  r....r(...r....r
+00000a50: 0700 0000 7207 0000 0072 0a00 0000 da08  ....r....r......
+00000a60: 3c6d 6f64 756c 653e 0100 0000 730a 0000  <module>....s...
+00000a70: 0010 0010 0210 0f10 1014 09              ...........
```

### Comparing `codeless-django-0.0.14/codeless_django/writers/__pycache__/files.cpython-310.pyc` & `codeless-django-0.0.15/codeless_django/writers/__pycache__/files.cpython-310.pyc`

 * *Format-specific differences are supported for Python .pyc files but no file-specific differences were detected; falling back to a binary diff. file(1) reports: Byte-compiled Python module for CPython 3.10, timestamp-based, .py timestamp: Fri Jun  9 00:42:56 2023 UTC, .py size: 2580 bytes*

 * *Could not decompile bytecode: bad marshal data (unknown type code)*

 * *Files 19% similar despite different names*

```diff
@@ -1,244 +1,251 @@
-00000000: 6f0d 0d0a 0000 0000 9075 8264 140a 0000  o........u.d....
+00000000: 6f0d 0d0a 0000 0000 242b bd64 720a 0000  o.......$+.dr...
 00000010: e300 0000 0000 0000 0000 0000 0000 0000  ................
-00000020: 0003 0000 0040 0000 0073 5000 0000 6400  .....@...sP...d.
+00000020: 0003 0000 0040 0000 0073 5c00 0000 6400  .....@...s\...d.
 00000030: 6401 6c00 6d01 5a01 0100 6400 6402 6c02  d.l.m.Z...d.d.l.
-00000040: 5a02 4700 6403 6404 8400 6404 8302 5a03  Z.G.d.d...d...Z.
-00000050: 4700 6405 6406 8400 6406 8302 5a04 4700  G.d.d...d...Z.G.
-00000060: 6407 6408 8400 6408 8302 5a05 4700 6409  d.d...d...Z.G.d.
-00000070: 640a 8400 640a 8302 5a06 6402 5300 290b  d...d...Z.d.S.).
-00000080: e900 0000 0029 01da 0a42 6173 6557 7269  .....)...BaseWri
-00000090: 7465 724e 6300 0000 0000 0000 0000 0000  terNc...........
-000000a0: 0000 0000 0003 0000 0040 0000 0073 3600  .........@...s6.
-000000b0: 0000 6500 5a01 6400 5a02 640d 6402 6403  ..e.Z.d.Z.d.d.d.
-000000c0: 8401 5a03 6404 6405 8400 5a04 6406 6407  ..Z.d.d...Z.d.d.
-000000d0: 8400 5a05 6408 6409 8400 5a06 640a 640b  ..Z.d.d...Z.d.d.
-000000e0: 8400 5a07 640c 5300 290e da0c 5072 6570  ..Z.d.S.)...Prep
-000000f0: 6172 6546 696c 6573 4663 0300 0000 0000  areFilesFc......
-00000100: 0000 0000 0000 0300 0000 0200 0000 4300  ..............C.
-00000110: 0000 7328 0000 007c 017c 005f 007c 027c  ..s(...|.|._.|.|
-00000120: 005f 017c 00a0 02a1 0001 007c 00a0 03a1  ._.|.......|....
-00000130: 0001 007c 00a0 04a1 0001 0064 0053 00a9  ...|.......d.S..
-00000140: 014e 2905 da08 6170 705f 6e61 6d65 da0f  .N)...app_name..
-00000150: 7772 6974 655f 6170 695f 7669 6577 73da  write_api_views.
-00000160: 1e77 7269 7465 5f69 6d70 6f72 745f 6c69  .write_import_li
-00000170: 6e65 5f74 6f5f 7669 6577 5f66 696c 65da  ne_to_view_file.
-00000180: 1d77 7269 7465 5f69 6d70 6f72 745f 6c69  .write_import_li
-00000190: 6e65 5f74 6f5f 7572 6c5f 6669 6c65 da25  ne_to_url_file.%
-000001a0: 7772 6974 655f 696d 706f 7274 5f6c 696e  write_import_lin
-000001b0: 655f 746f 5f73 6572 6961 6c69 7a65 7273  e_to_serializers
-000001c0: 5f66 696c 6529 03da 0473 656c 6672 0500  _file)...selfr..
-000001d0: 0000 7206 0000 00a9 0072 0b00 0000 fa38  ..r......r.....8
-000001e0: 2f68 6f6d 652f 6f6d 6172 2f63 6f64 652f  /home/omar/code/
-000001f0: 5175 6963 6b44 6a2f 636f 6465 6c65 7373  QuickDj/codeless
-00000200: 5f64 6a61 6e67 6f2f 7772 6974 6572 732f  _django/writers/
-00000210: 6669 6c65 732e 7079 da08 5f5f 696e 6974  files.py..__init
-00000220: 5f5f 0600 0000 730a 0000 0006 0106 0108  __....s.........
-00000230: 0108 010c 017a 1550 7265 7061 7265 4669  .....z.PrepareFi
-00000240: 6c65 732e 5f5f 696e 6974 5f5f 6303 0000  les.__init__c...
-00000250: 0000 0000 0000 0000 0004 0000 0008 0000  ................
-00000260: 0043 0000 0073 3e00 0000 7400 7c01 6401  .C...s>...t.|.d.
-00000270: 8302 8f10 7d03 7c03 a001 7c02 6402 1700  ....}.|...|.d...
-00000280: a101 0100 5700 6400 0400 0400 8303 0100  ....W.d.........
-00000290: 6400 5300 3100 7318 7701 0100 0100 0100  d.S.1.s.w.......
-000002a0: 5900 0100 6400 5300 2903 4eda 0177 7a03  Y...d.S.).N..wz.
-000002b0: 0a20 0a29 02da 046f 7065 6eda 0577 7269  . .)...open..wri
-000002c0: 7465 2904 720a 0000 00da 0966 696c 655f  te).r......file_
-000002d0: 6e61 6d65 da0b 696d 706f 7274 5f6c 696e  name..import_lin
-000002e0: 65da 0166 720b 0000 0072 0b00 0000 720c  e..fr....r....r.
-000002f0: 0000 00da 1177 7269 7465 5f69 6d70 6f72  .....write_impor
-00000300: 745f 6c69 6e65 0d00 0000 7306 0000 000c  t_line....s.....
-00000310: 0210 0122 ff7a 1e50 7265 7061 7265 4669  ...".z.PrepareFi
-00000320: 6c65 732e 7772 6974 655f 696d 706f 7274  les.write_import
-00000330: 5f6c 696e 6563 0100 0000 0000 0000 0000  _linec..........
-00000340: 0000 0300 0000 0600 0000 4300 0000 7356  ..........C...sV
-00000350: 0000 007c 006a 009b 0064 019d 027d 0164  ...|.j...d...}.d
-00000360: 027d 027c 0264 037c 006a 009b 0064 047c  .}.|.d.|.j...d.|
-00000370: 006a 009b 0064 059d 0537 007d 027c 006a  .j...d...7.}.|.j
-00000380: 0172 237c 0264 0664 037c 006a 009b 0064  .r#|.d.d.|.j...d
-00000390: 079d 0317 0037 007d 027c 00a0 027c 017c  .....7.}.|...|.|
-000003a0: 02a1 0201 0064 0053 0029 084e 7a09 2f76  .....d.S.).Nz./v
-000003b0: 6965 7773 2e70 797a 2266 726f 6d20 646a  iews.pyz"from dj
-000003c0: 616e 676f 2e76 6965 7773 2069 6d70 6f72  ango.views impor
-000003d0: 7420 6765 6e65 7269 6320 0afa 0566 726f  t generic ...fro
-000003e0: 6d20 fa12 2069 6d70 6f72 7420 6d6f 6465  m .. import mode
-000003f0: 6c73 2061 7320 fa09 5f6d 6f64 656c 7320  ls as .._models 
-00000400: 0a7a 2566 726f 6d20 7265 7374 5f66 7261  .z%from rest_fra
-00000410: 6d65 776f 726b 2069 6d70 6f72 7420 6765  mework import ge
-00000420: 6e65 7269 6373 200a 7a14 2069 6d70 6f72  nerics .z. impor
-00000430: 7420 7365 7269 616c 697a 6572 730a a903  t serializers...
-00000440: 7205 0000 0072 0600 0000 7214 0000 00a9  r....r....r.....
-00000450: 0372 0a00 0000 7211 0000 0072 1200 0000  .r....r....r....
-00000460: 720b 0000 0072 0b00 0000 720c 0000 0072  r....r....r....r
-00000470: 0700 0000 1200 0000 730c 0000 000c 0104  ........s.......
-00000480: 011a 0106 0116 0110 017a 2b50 7265 7061  .........z+Prepa
-00000490: 7265 4669 6c65 732e 7772 6974 655f 696d  reFiles.write_im
-000004a0: 706f 7274 5f6c 696e 655f 746f 5f76 6965  port_line_to_vie
-000004b0: 775f 6669 6c65 6301 0000 0000 0000 0000  w_filec.........
-000004c0: 0000 0003 0000 0006 0000 0043 0000 0073  ...........C...s
-000004d0: 4400 0000 7c00 6a00 9b00 6401 9d02 7d01  D...|.j...d...}.
-000004e0: 7c00 6a01 7220 6402 7d02 7c02 6403 7c00  |.j.r d.}.|.d.|.
-000004f0: 6a00 9b00 6404 7c00 6a00 9b00 6405 9d05  j...d.|.j...d...
-00000500: 3700 7d02 7c00 a002 7c01 7c02 a102 0100  7.}.|...|.|.....
-00000510: 6400 5300 6400 5300 2906 4e7a 0f2f 7365  d.S.d.S.).Nz./se
-00000520: 7269 616c 697a 6572 732e 7079 7a29 6672  rializers.pyz)fr
-00000530: 6f6d 2072 6573 745f 6672 616d 6577 6f72  om rest_framewor
-00000540: 6b20 696d 706f 7274 2073 6572 6961 6c69  k import seriali
-00000550: 7a65 7273 2020 0a72 1500 0000 7216 0000  zers  .r....r...
-00000560: 0072 1700 0000 7218 0000 0072 1900 0000  .r....r....r....
-00000570: 720b 0000 0072 0b00 0000 720c 0000 0072  r....r....r....r
-00000580: 0900 0000 1a00 0000 730c 0000 000c 0106  ........s.......
-00000590: 0104 011a 0110 0104 fd7a 3250 7265 7061  .........z2Prepa
-000005a0: 7265 4669 6c65 732e 7772 6974 655f 696d  reFiles.write_im
-000005b0: 706f 7274 5f6c 696e 655f 746f 5f73 6572  port_line_to_ser
-000005c0: 6961 6c69 7a65 7273 5f66 696c 6563 0100  ializers_filec..
-000005d0: 0000 0000 0000 0000 0000 0500 0000 0400  ................
-000005e0: 0000 4300 0000 733a 0000 007c 006a 009b  ..C...s:...|.j..
-000005f0: 0064 019d 027d 0164 0264 037c 006a 009b  .d...}.d.d.|.j..
-00000600: 0064 049d 0317 007d 0264 057d 037c 027c  .d.....}.d.}.|.|
-00000610: 0317 007d 047c 00a0 017c 017c 04a1 0201  ...}.|...|.|....
-00000620: 0064 0053 0029 064e 7a08 2f75 726c 732e  .d.S.).Nz./urls.
-00000630: 7079 7a1d 6672 6f6d 2064 6a61 6e67 6f2e  pyz.from django.
-00000640: 7572 6c73 2069 6d70 6f72 7420 7061 7468  urls import path
-00000650: 0a72 1500 0000 7a0f 2069 6d70 6f72 7420  .r....z. import 
-00000660: 7669 6577 7320 0a7a 1275 726c 7061 7474  views .z.urlpatt
-00000670: 6572 6e73 203d 205b 5d20 0a29 0272 0500  erns = [] .).r..
-00000680: 0000 7214 0000 0029 0572 0a00 0000 7211  ..r....).r....r.
-00000690: 0000 0072 1200 0000 da13 696e 6974 6961  ...r......initia
-000006a0: 6c5f 7572 6c5f 7061 7474 6572 6eda 0474  l_url_pattern..t
-000006b0: 6578 7472 0b00 0000 720b 0000 0072 0c00  extr....r....r..
-000006c0: 0000 7208 0000 0021 0000 0073 0a00 0000  ..r....!...s....
-000006d0: 0c01 1201 0401 0801 1001 7a2a 5072 6570  ..........z*Prep
-000006e0: 6172 6546 696c 6573 2e77 7269 7465 5f69  areFiles.write_i
-000006f0: 6d70 6f72 745f 6c69 6e65 5f74 6f5f 7572  mport_line_to_ur
-00000700: 6c5f 6669 6c65 4e29 0146 2908 da08 5f5f  l_fileN).F)...__
-00000710: 6e61 6d65 5f5f da0a 5f5f 6d6f 6475 6c65  name__..__module
-00000720: 5f5f da0c 5f5f 7175 616c 6e61 6d65 5f5f  __..__qualname__
-00000730: 720d 0000 0072 1400 0000 7207 0000 0072  r....r....r....r
-00000740: 0900 0000 7208 0000 0072 0b00 0000 720b  ....r....r....r.
-00000750: 0000 0072 0b00 0000 720c 0000 0072 0300  ...r....r....r..
-00000760: 0000 0400 0000 730c 0000 0008 000a 0208  ......s.........
-00000770: 0708 0508 080c 0772 0300 0000 6300 0000  .......r....c...
-00000780: 0000 0000 0000 0000 0000 0000 0002 0000  ................
-00000790: 0040 0000 00f3 1c00 0000 6500 5a01 6400  .@........e.Z.d.
-000007a0: 5a02 6401 6402 8400 5a03 6403 6404 8400  Z.d.d...Z.d.d...
-000007b0: 5a04 6405 5300 2906 da15 5265 7175 6972  Z.d.S.)...Requir
-000007c0: 656d 656e 7454 6578 7457 7269 7465 7263  ementTextWriterc
-000007d0: 0100 0000 0000 0000 0000 0000 0200 0000  ................
-000007e0: 0800 0000 4300 0000 7342 0000 0064 017c  ....C...sB...d.|
-000007f0: 005f 0074 017c 006a 0064 0283 028f 0e7d  ._.t.|.j.d.....}
-00000800: 017c 01a0 0264 03a1 0101 0057 0064 0004  .|...d.....W.d..
-00000810: 0004 0083 0301 0064 0053 0031 0073 1a77  .......d.S.1.s.w
-00000820: 0101 0001 0001 0059 0001 0064 0053 0029  .......Y...d.S.)
-00000830: 044e 7a10 7265 7175 6972 656d 656e 7473  .Nz.requirements
-00000840: 2e74 7874 da01 617a 1f64 6a61 6e67 6f3e  .txt..az.django>
-00000850: 3d32 2e32 2e31 3620 0a50 696c 6c6f 773d  =2.2.16 .Pillow=
-00000860: 3d39 2e35 2e30 200a 2903 7211 0000 0072  =9.5.0 .).r....r
-00000870: 0f00 0000 7210 0000 0029 0272 0a00 0000  ....r....).r....
-00000880: 7213 0000 0072 0b00 0000 720b 0000 0072  r....r....r....r
-00000890: 0c00 0000 720d 0000 0029 0000 0073 0800  ....r....)...s..
-000008a0: 0000 0601 0e01 0c01 22ff 7a1e 5265 7175  ........".z.Requ
-000008b0: 6972 656d 656e 7454 6578 7457 7269 7465  irementTextWrite
-000008c0: 722e 5f5f 696e 6974 5f5f 6303 0000 0000  r.__init__c.....
-000008d0: 0000 0000 0000 0004 0000 0008 0000 0043  ...............C
-000008e0: 0000 0073 4800 0000 7400 7c00 6a01 6401  ...sH...t.|.j.d.
-000008f0: 8302 8f14 7d03 7c03 a002 7c01 9b00 6402  ....}.|...|...d.
-00000900: 7c02 9b00 6403 9d04 a101 0100 5700 6400  |...d.......W.d.
-00000910: 0400 0400 8303 0100 6400 5300 3100 731d  ........d.S.1.s.
-00000920: 7701 0100 0100 0100 5900 0100 6400 5300  w.......Y...d.S.
-00000930: 2904 4e72 2100 0000 7a02 3d3d da01 0aa9  ).Nr!...z.==....
-00000940: 0372 0f00 0000 7211 0000 0072 1000 0000  .r....r....r....
-00000950: 2904 720a 0000 00da 0c70 6163 6b61 6765  ).r......package
-00000960: 5f6e 616d 65da 0776 6572 7369 6f6e 7213  _name..versionr.
-00000970: 0000 0072 0b00 0000 720b 0000 0072 0c00  ...r....r....r..
-00000980: 0000 da0f 6164 645f 6e65 775f 7061 636b  ....add_new_pack
-00000990: 6167 652f 0000 0073 0600 0000 0e01 1801  age/...s........
-000009a0: 22ff 7a25 5265 7175 6972 656d 656e 7454  ".z%RequirementT
-000009b0: 6578 7457 7269 7465 722e 6164 645f 6e65  extWriter.add_ne
-000009c0: 775f 7061 636b 6167 654e 2905 721c 0000  w_packageN).r...
-000009d0: 0072 1d00 0000 721e 0000 0072 0d00 0000  .r....r....r....
-000009e0: 7226 0000 0072 0b00 0000 720b 0000 0072  r&...r....r....r
-000009f0: 0b00 0000 720c 0000 0072 2000 0000 2800  ....r....r ...(.
-00000a00: 0000 7306 0000 0008 0008 010c 0672 2000  ..s..........r .
-00000a10: 0000 6300 0000 0000 0000 0000 0000 0000  ..c.............
-00000a20: 0000 0002 0000 0040 0000 0072 1f00 0000  .......@...r....
-00000a30: 2906 da10 446f 7445 6e76 4669 6c65 5772  )...DotEnvFileWr
-00000a40: 6974 6572 6301 0000 0000 0000 0000 0000  iterc...........
-00000a50: 0001 0000 0002 0000 0043 0000 0073 0a00  .........C...s..
-00000a60: 0000 6401 7c00 5f00 6400 5300 2902 4e7a  ..d.|._.d.S.).Nz
-00000a70: 042e 656e 7629 0172 1100 0000 a901 720a  ..env).r......r.
-00000a80: 0000 0072 0b00 0000 720b 0000 0072 0c00  ...r....r....r..
-00000a90: 0000 720d 0000 0035 0000 0073 0200 0000  ..r....5...s....
-00000aa0: 0a01 7a19 446f 7445 6e76 4669 6c65 5772  ..z.DotEnvFileWr
-00000ab0: 6974 6572 2e5f 5f69 6e69 745f 5f63 0300  iter.__init__c..
-00000ac0: 0000 0000 0000 0000 0000 0400 0000 0800  ................
-00000ad0: 0000 4300 0000 7346 0000 0074 007c 006a  ..C...sF...t.|.j
-00000ae0: 0164 0183 028f 137d 037c 03a0 027c 019b  .d.....}.|...|..
-00000af0: 0064 027c 029b 009d 03a1 0101 0057 0064  .d.|.........W.d
-00000b00: 0004 0004 0083 0301 0064 0053 0031 0073  .........d.S.1.s
-00000b10: 1c77 0101 0001 0001 0059 0001 0064 0053  .w.......Y...d.S
-00000b20: 0029 034e 7221 0000 00da 013d 7223 0000  .).Nr!.....=r#..
-00000b30: 0029 0472 0a00 0000 da03 6b65 79da 0576  .).r......key..v
-00000b40: 616c 7565 7213 0000 0072 0b00 0000 720b  aluer....r....r.
-00000b50: 0000 0072 0c00 0000 da0b 6164 645f 6e65  ...r......add_ne
-00000b60: 775f 6b65 7938 0000 0073 0600 0000 0e01  w_key8...s......
-00000b70: 1601 22ff 7a1c 446f 7445 6e76 4669 6c65  ..".z.DotEnvFile
-00000b80: 5772 6974 6572 2e61 6464 5f6e 6577 5f6b  Writer.add_new_k
-00000b90: 6579 4e29 0572 1c00 0000 721d 0000 0072  eyN).r....r....r
-00000ba0: 1e00 0000 720d 0000 0072 2c00 0000 720b  ....r....r,...r.
-00000bb0: 0000 0072 0b00 0000 720b 0000 0072 0c00  ...r....r....r..
-00000bc0: 0000 7227 0000 0034 0000 0073 0600 0000  ..r'...4...s....
-00000bd0: 0800 0801 0c03 7227 0000 0063 0000 0000  ......r'...c....
-00000be0: 0000 0000 0000 0000 0000 0000 0200 0000  ................
-00000bf0: 4000 0000 7324 0000 0065 005a 0164 005a  @...s$...e.Z.d.Z
-00000c00: 0264 0164 0284 005a 0364 0364 0484 005a  .d.d...Z.d.d...Z
-00000c10: 0464 0564 0684 005a 0564 0753 0029 08da  .d.d...Z.d.S.)..
-00000c20: 1441 6464 6974 696f 6e61 6c46 696c 6557  .AdditionalFileW
-00000c30: 7269 7465 7263 0100 0000 0000 0000 0000  riterc..........
-00000c40: 0000 0100 0000 0200 0000 4300 0000 730c  ..........C...s.
-00000c50: 0000 0074 0083 007c 005f 0164 0053 0072  ...t...|._.d.S.r
-00000c60: 0400 0000 2902 7220 0000 00da 1772 6571  ....).r .....req
-00000c70: 7569 7265 6d65 6e74 5f74 6578 745f 7772  uirement_text_wr
-00000c80: 6974 6572 7228 0000 0072 0b00 0000 720b  iterr(...r....r.
-00000c90: 0000 0072 0c00 0000 720d 0000 003e 0000  ...r....r....>..
-00000ca0: 0073 0200 0000 0c01 7a1d 4164 6469 7469  .s......z.Additi
-00000cb0: 6f6e 616c 4669 6c65 5772 6974 6572 2e5f  onalFileWriter._
-00000cc0: 5f69 6e69 745f 5f63 0100 0000 0000 0000  _init__c........
-00000cd0: 0000 0000 0100 0000 0300 0000 4300 0000  ............C...
-00000ce0: 730e 0000 0074 00a0 0164 01a1 0101 0064  s....t...d.....d
-00000cf0: 0053 0029 024e 7a39 6370 2063 6f64 656c  .S.).Nz9cp codel
-00000d00: 6573 735f 646a 616e 676f 2f61 6464 6974  ess_django/addit
-00000d10: 696f 6e61 6c5f 6669 6c65 732f 2e67 6974  ional_files/.git
-00000d20: 6967 6e6f 7265 202e 6769 7469 676e 6f72  ignore .gitignor
-00000d30: 6529 02da 026f 73da 0673 7973 7465 6d72  e)...os..systemr
-00000d40: 2800 0000 720b 0000 0072 0b00 0000 720c  (...r....r....r.
-00000d50: 0000 00da 1477 7269 7465 5f67 6974 6967  .....write_gitig
-00000d60: 6e6f 7265 5f66 696c 6542 0000 0073 0200  nore_fileB...s..
-00000d70: 0000 0e01 7a29 4164 6469 7469 6f6e 616c  ....z)Additional
-00000d80: 4669 6c65 5772 6974 6572 2e77 7269 7465  FileWriter.write
-00000d90: 5f67 6974 6967 6e6f 7265 5f66 696c 6563  _gitignore_filec
-00000da0: 0300 0000 0000 0000 0000 0000 0300 0000  ................
-00000db0: 0400 0000 4300 0000 7312 0000 007c 006a  ....C...s....|.j
-00000dc0: 00a0 017c 017c 02a1 0201 0064 0053 0072  ...|.|.....d.S.r
-00000dd0: 0400 0000 2902 722e 0000 0072 2600 0000  ....).r....r&...
-00000de0: 2903 720a 0000 0072 2400 0000 7225 0000  ).r....r$...r%..
-00000df0: 0072 0b00 0000 720b 0000 0072 0c00 0000  .r....r....r....
-00000e00: da26 7772 6974 655f 6e65 775f 7061 636b  .&write_new_pack
-00000e10: 6167 655f 696e 5f72 6571 7569 7265 6d65  age_in_requireme
-00000e20: 6e74 735f 7465 7874 4500 0000 7302 0000  nts_textE...s...
-00000e30: 0012 017a 3b41 6464 6974 696f 6e61 6c46  ...z;AdditionalF
-00000e40: 696c 6557 7269 7465 722e 7772 6974 655f  ileWriter.write_
-00000e50: 6e65 775f 7061 636b 6167 655f 696e 5f72  new_package_in_r
-00000e60: 6571 7569 7265 6d65 6e74 735f 7465 7874  equirements_text
-00000e70: 4e29 0672 1c00 0000 721d 0000 0072 1e00  N).r....r....r..
-00000e80: 0000 720d 0000 0072 3100 0000 7232 0000  ..r....r1...r2..
-00000e90: 0072 0b00 0000 720b 0000 0072 0b00 0000  .r....r....r....
-00000ea0: 720c 0000 0072 2d00 0000 3d00 0000 7308  r....r-...=...s.
-00000eb0: 0000 0008 0008 0108 040c 0372 2d00 0000  ...........r-...
-00000ec0: 2907 da1c 636f 6465 6c65 7373 5f64 6a61  )...codeless_dja
-00000ed0: 6e67 6f2e 7772 6974 6572 732e 6261 7365  ngo.writers.base
-00000ee0: 7202 0000 0072 2f00 0000 7203 0000 0072  r....r/...r....r
-00000ef0: 2000 0000 7227 0000 0072 2d00 0000 720b   ...r'...r-...r.
-00000f00: 0000 0072 0b00 0000 720b 0000 0072 0c00  ...r....r....r..
-00000f10: 0000 da08 3c6d 6f64 756c 653e 0100 0000  ....<module>....
-00000f20: 730c 0000 000c 0008 010e 020e 240e 0c12  s...........$...
-00000f30: 09                                       .
+00000040: 5a02 6400 6403 6c03 6d04 5a04 0100 4700  Z.d.d.l.m.Z...G.
+00000050: 6404 6405 8400 6405 8302 5a05 4700 6406  d.d...d...Z.G.d.
+00000060: 6407 8400 6407 8302 5a06 4700 6408 6409  d...d...Z.G.d.d.
+00000070: 8400 6409 8302 5a07 4700 640a 640b 8400  ..d...Z.G.d.d...
+00000080: 640b 8302 5a08 6402 5300 290c e900 0000  d...Z.d.S.).....
+00000090: 0029 01da 0a42 6173 6557 7269 7465 724e  .)...BaseWriterN
+000000a0: 2901 da10 6765 745f 6f73 5f66 696c 655f  )...get_os_file_
+000000b0: 7061 7468 6300 0000 0000 0000 0000 0000  pathc...........
+000000c0: 0000 0000 0003 0000 0040 0000 0073 3600  .........@...s6.
+000000d0: 0000 6500 5a01 6400 5a02 640d 6402 6403  ..e.Z.d.Z.d.d.d.
+000000e0: 8401 5a03 6404 6405 8400 5a04 6406 6407  ..Z.d.d...Z.d.d.
+000000f0: 8400 5a05 6408 6409 8400 5a06 640a 640b  ..Z.d.d...Z.d.d.
+00000100: 8400 5a07 640c 5300 290e da0c 5072 6570  ..Z.d.S.)...Prep
+00000110: 6172 6546 696c 6573 4663 0300 0000 0000  areFilesFc......
+00000120: 0000 0000 0000 0300 0000 0200 0000 4300  ..............C.
+00000130: 0000 7328 0000 007c 017c 005f 007c 027c  ..s(...|.|._.|.|
+00000140: 005f 017c 00a0 02a1 0001 007c 00a0 03a1  ._.|.......|....
+00000150: 0001 007c 00a0 04a1 0001 0064 0053 00a9  ...|.......d.S..
+00000160: 014e 2905 da08 6170 705f 6e61 6d65 da0f  .N)...app_name..
+00000170: 7772 6974 655f 6170 695f 7669 6577 73da  write_api_views.
+00000180: 1e77 7269 7465 5f69 6d70 6f72 745f 6c69  .write_import_li
+00000190: 6e65 5f74 6f5f 7669 6577 5f66 696c 65da  ne_to_view_file.
+000001a0: 1d77 7269 7465 5f69 6d70 6f72 745f 6c69  .write_import_li
+000001b0: 6e65 5f74 6f5f 7572 6c5f 6669 6c65 da25  ne_to_url_file.%
+000001c0: 7772 6974 655f 696d 706f 7274 5f6c 696e  write_import_lin
+000001d0: 655f 746f 5f73 6572 6961 6c69 7a65 7273  e_to_serializers
+000001e0: 5f66 696c 6529 03da 0473 656c 6672 0600  _file)...selfr..
+000001f0: 0000 7207 0000 00a9 0072 0c00 0000 fa5b  ..r......r.....[
+00000200: 2f68 6f6d 652f 6f6d 6172 2f63 6f64 652f  /home/omar/code/
+00000210: 7465 7374 2d63 6c64 2f76 656e 762f 6c69  test-cld/venv/li
+00000220: 622f 7079 7468 6f6e 332e 3130 2f73 6974  b/python3.10/sit
+00000230: 652d 7061 636b 6167 6573 2f63 6f64 656c  e-packages/codel
+00000240: 6573 735f 646a 616e 676f 2f77 7269 7465  ess_django/write
+00000250: 7273 2f66 696c 6573 2e70 79da 085f 5f69  rs/files.py..__i
+00000260: 6e69 745f 5f07 0000 0073 0a00 0000 0601  nit__....s......
+00000270: 0601 0801 0801 0c01 7a15 5072 6570 6172  ........z.Prepar
+00000280: 6546 696c 6573 2e5f 5f69 6e69 745f 5f63  eFiles.__init__c
+00000290: 0300 0000 0000 0000 0000 0000 0400 0000  ................
+000002a0: 0800 0000 4300 0000 733e 0000 0074 007c  ....C...s>...t.|
+000002b0: 0164 0183 028f 107d 037c 03a0 017c 0264  .d.....}.|...|.d
+000002c0: 0217 00a1 0101 0057 0064 0004 0004 0083  .......W.d......
+000002d0: 0301 0064 0053 0031 0073 1877 0101 0001  ...d.S.1.s.w....
+000002e0: 0001 0059 0001 0064 0053 0029 034e da01  ...Y...d.S.).N..
+000002f0: 777a 030a 200a 2902 da04 6f70 656e da05  wz.. .)...open..
+00000300: 7772 6974 6529 0472 0b00 0000 da09 6669  write).r......fi
+00000310: 6c65 5f6e 616d 65da 0b69 6d70 6f72 745f  le_name..import_
+00000320: 6c69 6e65 da01 6672 0c00 0000 720c 0000  line..fr....r...
+00000330: 0072 0d00 0000 da11 7772 6974 655f 696d  .r......write_im
+00000340: 706f 7274 5f6c 696e 650e 0000 0073 0600  port_line....s..
+00000350: 0000 0c02 1001 22ff 7a1e 5072 6570 6172  ......".z.Prepar
+00000360: 6546 696c 6573 2e77 7269 7465 5f69 6d70  eFiles.write_imp
+00000370: 6f72 745f 6c69 6e65 6301 0000 0000 0000  ort_linec.......
+00000380: 0000 0000 0003 0000 0006 0000 0043 0000  .............C..
+00000390: 0073 5600 0000 7c00 6a00 9b00 6401 9d02  .sV...|.j...d...
+000003a0: 7d01 6402 7d02 7c02 6403 7c00 6a00 9b00  }.d.}.|.d.|.j...
+000003b0: 6404 7c00 6a00 9b00 6405 9d05 3700 7d02  d.|.j...d...7.}.
+000003c0: 7c00 6a01 7223 7c02 6406 6403 7c00 6a00  |.j.r#|.d.d.|.j.
+000003d0: 9b00 6407 9d03 1700 3700 7d02 7c00 a002  ..d.....7.}.|...
+000003e0: 7c01 7c02 a102 0100 6400 5300 2908 4e7a  |.|.....d.S.).Nz
+000003f0: 092f 7669 6577 732e 7079 7a22 6672 6f6d  ./views.pyz"from
+00000400: 2064 6a61 6e67 6f2e 7669 6577 7320 696d   django.views im
+00000410: 706f 7274 2067 656e 6572 6963 200a fa05  port generic ...
+00000420: 6672 6f6d 20fa 1220 696d 706f 7274 206d  from .. import m
+00000430: 6f64 656c 7320 6173 20fa 095f 6d6f 6465  odels as .._mode
+00000440: 6c73 200a 7a25 6672 6f6d 2072 6573 745f  ls .z%from rest_
+00000450: 6672 616d 6577 6f72 6b20 696d 706f 7274  framework import
+00000460: 2067 656e 6572 6963 7320 0a7a 1420 696d   generics .z. im
+00000470: 706f 7274 2073 6572 6961 6c69 7a65 7273  port serializers
+00000480: 0aa9 0372 0600 0000 7207 0000 0072 1500  ...r....r....r..
+00000490: 0000 a903 720b 0000 0072 1200 0000 7213  ....r....r....r.
+000004a0: 0000 0072 0c00 0000 720c 0000 0072 0d00  ...r....r....r..
+000004b0: 0000 7208 0000 0013 0000 0073 0c00 0000  ..r........s....
+000004c0: 0c01 0401 1a01 0601 1601 1001 7a2b 5072  ............z+Pr
+000004d0: 6570 6172 6546 696c 6573 2e77 7269 7465  epareFiles.write
+000004e0: 5f69 6d70 6f72 745f 6c69 6e65 5f74 6f5f  _import_line_to_
+000004f0: 7669 6577 5f66 696c 6563 0100 0000 0000  view_filec......
+00000500: 0000 0000 0000 0300 0000 0600 0000 4300  ..............C.
+00000510: 0000 7344 0000 007c 006a 009b 0064 019d  ..sD...|.j...d..
+00000520: 027d 017c 006a 0172 2064 027d 027c 0264  .}.|.j.r d.}.|.d
+00000530: 037c 006a 009b 0064 047c 006a 009b 0064  .|.j...d.|.j...d
+00000540: 059d 0537 007d 027c 00a0 027c 017c 02a1  ...7.}.|...|.|..
+00000550: 0201 0064 0053 0064 0053 0029 064e 7a0f  ...d.S.d.S.).Nz.
+00000560: 2f73 6572 6961 6c69 7a65 7273 2e70 797a  /serializers.pyz
+00000570: 2966 726f 6d20 7265 7374 5f66 7261 6d65  )from rest_frame
+00000580: 776f 726b 2069 6d70 6f72 7420 7365 7269  work import seri
+00000590: 616c 697a 6572 7320 200a 7216 0000 0072  alizers  .r....r
+000005a0: 1700 0000 7218 0000 0072 1900 0000 721a  ....r....r....r.
+000005b0: 0000 0072 0c00 0000 720c 0000 0072 0d00  ...r....r....r..
+000005c0: 0000 720a 0000 001b 0000 0073 0c00 0000  ..r........s....
+000005d0: 0c01 0601 0401 1a01 1001 04fd 7a32 5072  ............z2Pr
+000005e0: 6570 6172 6546 696c 6573 2e77 7269 7465  epareFiles.write
+000005f0: 5f69 6d70 6f72 745f 6c69 6e65 5f74 6f5f  _import_line_to_
+00000600: 7365 7269 616c 697a 6572 735f 6669 6c65  serializers_file
+00000610: 6301 0000 0000 0000 0000 0000 0005 0000  c...............
+00000620: 0004 0000 0043 0000 0073 3a00 0000 7c00  .....C...s:...|.
+00000630: 6a00 9b00 6401 9d02 7d01 6402 6403 7c00  j...d...}.d.d.|.
+00000640: 6a00 9b00 6404 9d03 1700 7d02 6405 7d03  j...d.....}.d.}.
+00000650: 7c02 7c03 1700 7d04 7c00 a001 7c01 7c04  |.|...}.|...|.|.
+00000660: a102 0100 6400 5300 2906 4e7a 082f 7572  ....d.S.).Nz./ur
+00000670: 6c73 2e70 797a 1d66 726f 6d20 646a 616e  ls.pyz.from djan
+00000680: 676f 2e75 726c 7320 696d 706f 7274 2070  go.urls import p
+00000690: 6174 680a 7216 0000 007a 0f20 696d 706f  ath.r....z. impo
+000006a0: 7274 2076 6965 7773 200a 7a12 7572 6c70  rt views .z.urlp
+000006b0: 6174 7465 726e 7320 3d20 5b5d 200a 2902  atterns = [] .).
+000006c0: 7206 0000 0072 1500 0000 2905 720b 0000  r....r....).r...
+000006d0: 0072 1200 0000 7213 0000 00da 1369 6e69  .r....r......ini
+000006e0: 7469 616c 5f75 726c 5f70 6174 7465 726e  tial_url_pattern
+000006f0: da04 7465 7874 720c 0000 0072 0c00 0000  ..textr....r....
+00000700: 720d 0000 0072 0900 0000 2200 0000 730a  r....r...."...s.
+00000710: 0000 000c 0112 0104 0108 0110 017a 2a50  .............z*P
+00000720: 7265 7061 7265 4669 6c65 732e 7772 6974  repareFiles.writ
+00000730: 655f 696d 706f 7274 5f6c 696e 655f 746f  e_import_line_to
+00000740: 5f75 726c 5f66 696c 654e 2901 4629 08da  _url_fileN).F)..
+00000750: 085f 5f6e 616d 655f 5fda 0a5f 5f6d 6f64  .__name__..__mod
+00000760: 756c 655f 5fda 0c5f 5f71 7561 6c6e 616d  ule__..__qualnam
+00000770: 655f 5f72 0e00 0000 7215 0000 0072 0800  e__r....r....r..
+00000780: 0000 720a 0000 0072 0900 0000 720c 0000  ..r....r....r...
+00000790: 0072 0c00 0000 720c 0000 0072 0d00 0000  .r....r....r....
+000007a0: 7204 0000 0005 0000 0073 0c00 0000 0800  r........s......
+000007b0: 0a02 0807 0805 0808 0c07 7204 0000 0063  ..........r....c
+000007c0: 0000 0000 0000 0000 0000 0000 0000 0000  ................
+000007d0: 0200 0000 4000 0000 f31c 0000 0065 005a  ....@........e.Z
+000007e0: 0164 005a 0264 0164 0284 005a 0364 0364  .d.Z.d.d...Z.d.d
+000007f0: 0484 005a 0464 0553 0029 06da 1552 6571  ...Z.d.S.)...Req
+00000800: 7569 7265 6d65 6e74 5465 7874 5772 6974  uirementTextWrit
+00000810: 6572 6301 0000 0000 0000 0000 0000 0002  erc.............
+00000820: 0000 0008 0000 0043 0000 0073 4200 0000  .......C...sB...
+00000830: 6401 7c00 5f00 7401 7c00 6a00 6402 8302  d.|._.t.|.j.d...
+00000840: 8f0e 7d01 7c01 a002 6403 a101 0100 5700  ..}.|...d.....W.
+00000850: 6400 0400 0400 8303 0100 6400 5300 3100  d.........d.S.1.
+00000860: 731a 7701 0100 0100 0100 5900 0100 6400  s.w.......Y...d.
+00000870: 5300 2904 4e7a 1072 6571 7569 7265 6d65  S.).Nz.requireme
+00000880: 6e74 732e 7478 74da 0161 7a1f 646a 616e  nts.txt..az.djan
+00000890: 676f 3e3d 322e 322e 3136 200a 5069 6c6c  go>=2.2.16 .Pill
+000008a0: 6f77 3d3d 392e 352e 3020 0a29 0372 1200  ow==9.5.0 .).r..
+000008b0: 0000 7210 0000 0072 1100 0000 2902 720b  ..r....r....).r.
+000008c0: 0000 0072 1400 0000 720c 0000 0072 0c00  ...r....r....r..
+000008d0: 0000 720d 0000 0072 0e00 0000 2a00 0000  ..r....r....*...
+000008e0: 7308 0000 0006 010e 010c 0122 ff7a 1e52  s..........".z.R
+000008f0: 6571 7569 7265 6d65 6e74 5465 7874 5772  equirementTextWr
+00000900: 6974 6572 2e5f 5f69 6e69 745f 5f63 0300  iter.__init__c..
+00000910: 0000 0000 0000 0000 0000 0400 0000 0800  ................
+00000920: 0000 4300 0000 7348 0000 0074 007c 006a  ..C...sH...t.|.j
+00000930: 0164 0183 028f 147d 037c 03a0 027c 019b  .d.....}.|...|..
+00000940: 0064 027c 029b 0064 039d 04a1 0101 0057  .d.|...d.......W
+00000950: 0064 0004 0004 0083 0301 0064 0053 0031  .d.........d.S.1
+00000960: 0073 1d77 0101 0001 0001 0059 0001 0064  .s.w.......Y...d
+00000970: 0053 0029 044e 7222 0000 007a 023d 3dda  .S.).Nr"...z.==.
+00000980: 010a a903 7210 0000 0072 1200 0000 7211  ....r....r....r.
+00000990: 0000 0029 0472 0b00 0000 da0c 7061 636b  ...).r......pack
+000009a0: 6167 655f 6e61 6d65 da07 7665 7273 696f  age_name..versio
+000009b0: 6e72 1400 0000 720c 0000 0072 0c00 0000  nr....r....r....
+000009c0: 720d 0000 00da 0f61 6464 5f6e 6577 5f70  r......add_new_p
+000009d0: 6163 6b61 6765 3000 0000 7306 0000 000e  ackage0...s.....
+000009e0: 0118 0122 ff7a 2552 6571 7569 7265 6d65  ...".z%Requireme
+000009f0: 6e74 5465 7874 5772 6974 6572 2e61 6464  ntTextWriter.add
+00000a00: 5f6e 6577 5f70 6163 6b61 6765 4e29 0572  _new_packageN).r
+00000a10: 1d00 0000 721e 0000 0072 1f00 0000 720e  ....r....r....r.
+00000a20: 0000 0072 2700 0000 720c 0000 0072 0c00  ...r'...r....r..
+00000a30: 0000 720c 0000 0072 0d00 0000 7221 0000  ..r....r....r!..
+00000a40: 0029 0000 0073 0600 0000 0800 0801 0c06  .)...s..........
+00000a50: 7221 0000 0063 0000 0000 0000 0000 0000  r!...c..........
+00000a60: 0000 0000 0000 0200 0000 4000 0000 7220  ..........@...r 
+00000a70: 0000 0029 06da 1044 6f74 456e 7646 696c  ...)...DotEnvFil
+00000a80: 6557 7269 7465 7263 0100 0000 0000 0000  eWriterc........
+00000a90: 0000 0000 0100 0000 0200 0000 4300 0000  ............C...
+00000aa0: 730a 0000 0064 017c 005f 0064 0053 0029  s....d.|._.d.S.)
+00000ab0: 024e 7a04 2e65 6e76 2901 7212 0000 00a9  .Nz..env).r.....
+00000ac0: 0172 0b00 0000 720c 0000 0072 0c00 0000  .r....r....r....
+00000ad0: 720d 0000 0072 0e00 0000 3600 0000 7302  r....r....6...s.
+00000ae0: 0000 000a 017a 1944 6f74 456e 7646 696c  .....z.DotEnvFil
+00000af0: 6557 7269 7465 722e 5f5f 696e 6974 5f5f  eWriter.__init__
+00000b00: 6303 0000 0000 0000 0000 0000 0004 0000  c...............
+00000b10: 0008 0000 0043 0000 0073 4600 0000 7400  .....C...sF...t.
+00000b20: 7c00 6a01 6401 8302 8f13 7d03 7c03 a002  |.j.d.....}.|...
+00000b30: 7c01 9b00 6402 7c02 9b00 9d03 a101 0100  |...d.|.........
+00000b40: 5700 6400 0400 0400 8303 0100 6400 5300  W.d.........d.S.
+00000b50: 3100 731c 7701 0100 0100 0100 5900 0100  1.s.w.......Y...
+00000b60: 6400 5300 2903 4e72 2200 0000 fa01 3d72  d.S.).Nr".....=r
+00000b70: 2400 0000 2904 720b 0000 00da 036b 6579  $...).r......key
+00000b80: da05 7661 6c75 6572 1400 0000 720c 0000  ..valuer....r...
+00000b90: 0072 0c00 0000 720d 0000 00da 0b61 6464  .r....r......add
+00000ba0: 5f6e 6577 5f6b 6579 3900 0000 7306 0000  _new_key9...s...
+00000bb0: 000e 0116 0122 ff7a 1c44 6f74 456e 7646  .....".z.DotEnvF
+00000bc0: 696c 6557 7269 7465 722e 6164 645f 6e65  ileWriter.add_ne
+00000bd0: 775f 6b65 794e 2905 721d 0000 0072 1e00  w_keyN).r....r..
+00000be0: 0000 721f 0000 0072 0e00 0000 722d 0000  ..r....r....r-..
+00000bf0: 0072 0c00 0000 720c 0000 0072 0c00 0000  .r....r....r....
+00000c00: 720d 0000 0072 2800 0000 3500 0000 7306  r....r(...5...s.
+00000c10: 0000 0008 0008 010c 0372 2800 0000 6300  .........r(...c.
+00000c20: 0000 0000 0000 0000 0000 0000 0000 0002  ................
+00000c30: 0000 0040 0000 0073 2400 0000 6500 5a01  ...@...s$...e.Z.
+00000c40: 6400 5a02 6401 6402 8400 5a03 6403 6404  d.Z.d.d...Z.d.d.
+00000c50: 8400 5a04 6405 6406 8400 5a05 6407 5300  ..Z.d.d...Z.d.S.
+00000c60: 2908 da14 4164 6469 7469 6f6e 616c 4669  )...AdditionalFi
+00000c70: 6c65 5772 6974 6572 6301 0000 0000 0000  leWriterc.......
+00000c80: 0000 0000 0001 0000 0002 0000 0043 0000  .............C..
+00000c90: 0073 0c00 0000 7400 8300 7c00 5f01 6400  .s....t...|._.d.
+00000ca0: 5300 7205 0000 0029 0272 2100 0000 da17  S.r....).r!.....
+00000cb0: 7265 7175 6972 656d 656e 745f 7465 7874  requirement_text
+00000cc0: 5f77 7269 7465 7272 2900 0000 720c 0000  _writerr)...r...
+00000cd0: 0072 0c00 0000 720d 0000 0072 0e00 0000  .r....r....r....
+00000ce0: 3f00 0000 7302 0000 000c 017a 1d41 6464  ?...s......z.Add
+00000cf0: 6974 696f 6e61 6c46 696c 6557 7269 7465  itionalFileWrite
+00000d00: 722e 5f5f 696e 6974 5f5f 6301 0000 0000  r.__init__c.....
+00000d10: 0000 0000 0000 0002 0000 0005 0000 0043  ...............C
+00000d20: 0000 0073 1e00 0000 7400 6401 8301 7d01  ...s....t.d...}.
+00000d30: 7401 a002 6402 7c01 9b00 6403 9d03 a101  t...d.|...d.....
+00000d40: 0100 6400 5300 2904 4e7a 1b61 6464 6974  ..d.S.).Nz.addit
+00000d50: 696f 6e61 6c5f 6669 6c65 732f 2e67 6974  ional_files/.git
+00000d60: 6967 6e6f 7265 7a03 6370 207a 0b20 2e67  ignorez.cp z. .g
+00000d70: 6974 6967 6e6f 7265 2903 7203 0000 00da  itignore).r.....
+00000d80: 026f 73da 0673 7973 7465 6d29 0272 0b00  .os..system).r..
+00000d90: 0000 da0c 6f73 5f66 696c 655f 7061 7468  ....os_file_path
+00000da0: 720c 0000 0072 0c00 0000 720d 0000 00da  r....r....r.....
+00000db0: 1477 7269 7465 5f67 6974 6967 6e6f 7265  .write_gitignore
+00000dc0: 5f66 696c 6543 0000 0073 0400 0000 0801  _fileC...s......
+00000dd0: 1601 7a29 4164 6469 7469 6f6e 616c 4669  ..z)AdditionalFi
+00000de0: 6c65 5772 6974 6572 2e77 7269 7465 5f67  leWriter.write_g
+00000df0: 6974 6967 6e6f 7265 5f66 696c 6563 0300  itignore_filec..
+00000e00: 0000 0000 0000 0000 0000 0300 0000 0400  ................
+00000e10: 0000 4300 0000 7312 0000 007c 006a 00a0  ..C...s....|.j..
+00000e20: 017c 017c 02a1 0201 0064 0053 0072 0500  .|.|.....d.S.r..
+00000e30: 0000 2902 722f 0000 0072 2700 0000 2903  ..).r/...r'...).
+00000e40: 720b 0000 0072 2500 0000 7226 0000 0072  r....r%...r&...r
+00000e50: 0c00 0000 720c 0000 0072 0d00 0000 da26  ....r....r.....&
+00000e60: 7772 6974 655f 6e65 775f 7061 636b 6167  write_new_packag
+00000e70: 655f 696e 5f72 6571 7569 7265 6d65 6e74  e_in_requirement
+00000e80: 735f 7465 7874 4700 0000 7302 0000 0012  s_textG...s.....
+00000e90: 017a 3b41 6464 6974 696f 6e61 6c46 696c  .z;AdditionalFil
+00000ea0: 6557 7269 7465 722e 7772 6974 655f 6e65  eWriter.write_ne
+00000eb0: 775f 7061 636b 6167 655f 696e 5f72 6571  w_package_in_req
+00000ec0: 7569 7265 6d65 6e74 735f 7465 7874 4e29  uirements_textN)
+00000ed0: 0672 1d00 0000 721e 0000 0072 1f00 0000  .r....r....r....
+00000ee0: 720e 0000 0072 3300 0000 7234 0000 0072  r....r3...r4...r
+00000ef0: 0c00 0000 720c 0000 0072 0c00 0000 720d  ....r....r....r.
+00000f00: 0000 0072 2e00 0000 3e00 0000 7308 0000  ...r....>...s...
+00000f10: 0008 0008 0108 040c 0472 2e00 0000 2909  .........r....).
+00000f20: da1c 636f 6465 6c65 7373 5f64 6a61 6e67  ..codeless_djang
+00000f30: 6f2e 7772 6974 6572 732e 6261 7365 7202  o.writers.baser.
+00000f40: 0000 0072 3000 0000 da15 636f 6465 6c65  ...r0.....codele
+00000f50: 7373 5f64 6a61 6e67 6f2e 7574 696c 7372  ss_django.utilsr
+00000f60: 0300 0000 7204 0000 0072 2100 0000 7228  ....r....r!...r(
+00000f70: 0000 0072 2e00 0000 720c 0000 0072 0c00  ...r....r....r..
+00000f80: 0000 720c 0000 0072 0d00 0000 da08 3c6d  ..r....r......<m
+00000f90: 6f64 756c 653e 0100 0000 730e 0000 000c  odule>....s.....
+00000fa0: 0008 010c 010e 020e 240e 0c12 09         ........$....
```

### Comparing `codeless-django-0.0.14/codeless_django/writers/__pycache__/models.cpython-310.pyc` & `codeless-django-0.0.15/codeless_django/writers/__pycache__/models.cpython-310.pyc`

 * *Format-specific differences are supported for Python .pyc files but no file-specific differences were detected; falling back to a binary diff. file(1) reports: Byte-compiled Python module for CPython 3.10, timestamp-based, .py timestamp: Sat May 20 16:06:48 2023 UTC, .py size: 1907 bytes*

 * *Could not decompile bytecode: bad marshal data (unknown type code)*

 * *Files 1% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-00000000: 6f0d 0d0a 0000 0000 18f0 6864 7307 0000  o.........hds...
+00000000: 6f0d 0d0a 0000 0000 6f28 bd64 7307 0000  o.......o(.ds...
 00000010: e300 0000 0000 0000 0000 0000 0000 0000  ................
 00000020: 0004 0000 0040 0000 0073 3400 0000 6400  .....@...s4...d.
 00000030: 6401 6c00 6d01 5a01 6d02 5a02 0100 4700  d.l.m.Z.m.Z...G.
 00000040: 6402 6403 8400 6403 6502 8303 5a03 4700  d.d...d.e...Z.G.
 00000050: 6404 6405 8400 6405 6501 8303 5a04 6406  d.d...d.e...Z.d.
 00000060: 5300 2907 e900 0000 0029 02da 0a42 6173  S.)......)...Bas
 00000070: 6557 7269 7465 72da 0b42 6173 6542 7569  eWriter..BaseBui
@@ -16,148 +16,150 @@
 000000f0: 0000 0000 0000 0000 0000 0004 0000 0002  ................
 00000100: 0000 0043 0000 0073 1600 0000 7c01 7c00  ...C...s....|.|.
 00000110: 5f00 7c02 7c00 5f01 7c03 7c00 5f02 6400  _.|.|._.|.|._.d.
 00000120: 5300 2901 4e29 03da 0a6d 6f64 656c 5f6e  S.).N)...model_n
 00000130: 616d 65da 0666 6965 6c64 73da 0c6d 6574  ame..fields..met
 00000140: 615f 6f70 7469 6f6e 7329 04da 0473 656c  a_options)...sel
 00000150: 6672 0500 0000 7206 0000 0072 0700 0000  fr....r....r....
-00000160: a900 7209 0000 00fa 392f 686f 6d65 2f6f  ..r.....9/home/o
-00000170: 6d61 722f 636f 6465 2f51 7569 636b 446a  mar/code/QuickDj
-00000180: 2f63 6f64 656c 6573 735f 646a 616e 676f  /codeless_django
-00000190: 2f77 7269 7465 7273 2f6d 6f64 656c 732e  /writers/models.
-000001a0: 7079 da08 5f5f 696e 6974 5f5f 0500 0000  py..__init__....
-000001b0: 7306 0000 0006 0106 010a 017a 154d 6f64  s..........z.Mod
-000001c0: 656c 4275 696c 6465 722e 5f5f 696e 6974  elBuilder.__init
-000001d0: 5f5f 6302 0000 0000 0000 0000 0000 0002  __c.............
-000001e0: 0000 0004 0000 0043 0000 0073 1400 0000  .......C...s....
-000001f0: 6401 a000 6402 6403 8400 7c01 4400 8301  d...d.d...|.D...
-00000200: a101 5300 2904 4e7a 022c 2063 0100 0000  ..S.).Nz., c....
-00000210: 0000 0000 0000 0000 0200 0000 0600 0000  ................
-00000220: 5300 0000 7322 0000 0067 007c 005d 0d7d  S...s"...g.|.].}
-00000230: 017c 0164 0019 009b 0064 017c 0164 0219  .|.d.....d.|.d..
-00000240: 009b 009d 0391 0271 0253 0029 03da 046e  .......q.S.)...n
-00000250: 616d 65da 013d da05 7661 6c75 6572 0900  ame..=..valuer..
-00000260: 0000 2902 da02 2e30 da03 6f70 7472 0900  ..)....0..optr..
-00000270: 0000 7209 0000 0072 0a00 0000 da0a 3c6c  ..r....r......<l
-00000280: 6973 7463 6f6d 703e 0b00 0000 7302 0000  istcomp>....s...
-00000290: 0022 007a 324d 6f64 656c 4275 696c 6465  .".z2ModelBuilde
-000002a0: 722e 6765 745f 6669 656c 645f 6f70 7469  r.get_field_opti
-000002b0: 6f6e 732e 3c6c 6f63 616c 733e 2e3c 6c69  ons.<locals>.<li
-000002c0: 7374 636f 6d70 3e29 01da 046a 6f69 6e29  stcomp>)...join)
-000002d0: 0272 0800 0000 da07 6f70 7469 6f6e 7372  .r......optionsr
-000002e0: 0900 0000 7209 0000 0072 0a00 0000 da11  ....r....r......
-000002f0: 6765 745f 6669 656c 645f 6f70 7469 6f6e  get_field_option
-00000300: 730a 0000 00f3 0200 0000 1401 7a1e 4d6f  s...........z.Mo
-00000310: 6465 6c42 7569 6c64 6572 2e67 6574 5f66  delBuilder.get_f
-00000320: 6965 6c64 5f6f 7074 696f 6e73 6304 0000  ield_optionsc...
-00000330: 0000 0000 0000 0000 0005 0000 0006 0000  ................
-00000340: 0043 0000 0073 2000 0000 7c00 a000 7c03  .C...s ...|...|.
-00000350: a101 7d04 7c01 9b00 6401 7c02 9b00 6402  ..}.|...d.|...d.
-00000360: 7c04 9b00 6403 9d06 5300 2904 4e7a 0a20  |...d...S.).Nz. 
-00000370: 3d20 6d6f 6465 6c73 2efa 0128 fa01 2929  = models...(..))
-00000380: 0172 1400 0000 2905 7208 0000 00da 0a66  .r....).r......f
-00000390: 6965 6c64 5f6e 616d 65da 0a66 6965 6c64  ield_name..field
-000003a0: 5f74 7970 6572 1300 0000 da0d 6669 656c  _typer......fiel
-000003b0: 645f 6f70 7469 6f6e 7372 0900 0000 7209  d_optionsr....r.
-000003c0: 0000 0072 0a00 0000 da10 6765 745f 6669  ...r......get_fi
-000003d0: 656c 645f 7374 7269 6e67 0d00 0000 7304  eld_string....s.
-000003e0: 0000 000a 0116 017a 1d4d 6f64 656c 4275  .......z.ModelBu
-000003f0: 696c 6465 722e 6765 745f 6669 656c 645f  ilder.get_field_
-00000400: 7374 7269 6e67 6301 0000 0000 0000 0000  stringc.........
-00000410: 0000 0001 0000 0003 0000 0043 0000 0073  ...........C...s
-00000420: 0e00 0000 6401 7c00 6a00 9b00 6402 9d03  ....d.|.j...d...
-00000430: 5300 2903 4e7a 0663 6c61 7373 207a 1028  S.).Nz.class z.(
-00000440: 6d6f 6465 6c73 2e4d 6f64 656c 293a 0a29  models.Model):.)
-00000450: 0172 0500 0000 a901 7208 0000 0072 0900  .r......r....r..
-00000460: 0000 7209 0000 0072 0a00 0000 da11 6765  ..r....r......ge
-00000470: 745f 6f62 6a65 6374 5f68 6561 6465 7212  t_object_header.
-00000480: 0000 0073 0200 0000 0e01 7a1e 4d6f 6465  ...s......z.Mode
-00000490: 6c42 7569 6c64 6572 2e67 6574 5f6f 626a  lBuilder.get_obj
-000004a0: 6563 745f 6865 6164 6572 6301 0000 0000  ect_headerc.....
-000004b0: 0000 0000 0000 000a 0000 0007 0000 0043  ...............C
-000004c0: 0000 0073 8600 0000 6401 7d01 7c00 6a00  ...s....d.}.|.j.
-000004d0: a001 a100 4400 5d1b 5c02 7d02 7d03 7c03  ....D.].\.}.}.|.
-000004e0: 6402 1900 7d04 7c03 6403 1900 7d05 7c00  d...}.|.d...}.|.
-000004f0: a002 7c02 7c04 7c05 a103 7d06 7c01 6404  ..|.|.|...}.|.d.
-00000500: 7c06 1700 6401 1700 3700 7d01 7107 7c00  |...d...7.}.q.|.
-00000510: 6a03 7241 6405 7d07 7c00 6a03 a001 a100  j.rAd.}.|.j.....
-00000520: 4400 5d0f 5c02 7d08 7d09 7c07 6406 7c08  D.].\.}.}.|.d.|.
-00000530: 9b00 6407 7c09 9b00 6401 9d05 3700 7d07  ..d.|...d...7.}.
-00000540: 712d 7c01 7c07 1700 5300 7c01 5300 2908  q-|.|...S.|.S.).
-00000550: 4eda 010a da04 7479 7065 7213 0000 00fa  N.....typer.....
-00000560: 0109 7a0f 0a09 636c 6173 7320 4d65 7461  ..z...class Meta
-00000570: 3a20 0a7a 0209 0972 0d00 0000 2904 7206  : .z...r....).r.
-00000580: 0000 00da 0569 7465 6d73 721b 0000 0072  .....itemsr....r
-00000590: 0700 0000 290a 7208 0000 00da 0a6d 6f64  ....).r......mod
-000005a0: 656c 5f62 6f64 7972 1800 0000 da06 7661  el_bodyr......va
-000005b0: 6c75 6573 7219 0000 0072 1300 0000 da0c  luesr....r......
-000005c0: 6669 656c 645f 7374 7269 6e67 da09 6d65  field_string..me
-000005d0: 7461 5f62 6f64 79da 036b 6579 720e 0000  ta_body..keyr...
-000005e0: 0072 0900 0000 7209 0000 0072 0a00 0000  .r....r....r....
-000005f0: da0f 6765 745f 6f62 6a65 6374 5f62 6f64  ..get_object_bod
-00000600: 7915 0000 0073 1800 0000 0401 1201 0802  y....s..........
-00000610: 0801 0e01 1201 0602 0401 1201 1801 0802  ................
-00000620: 0402 7a1c 4d6f 6465 6c42 7569 6c64 6572  ..z.ModelBuilder
-00000630: 2e67 6574 5f6f 626a 6563 745f 626f 6479  .get_object_body
-00000640: 6301 0000 0000 0000 0000 0000 0001 0000  c...............
-00000650: 0003 0000 0043 0000 0073 1400 0000 7c00  .....C...s....|.
-00000660: a000 a100 7c00 a001 a100 1700 6401 1700  ....|.......d...
-00000670: 5300 2902 4e72 1e00 0000 2902 721d 0000  S.).Nr....).r...
-00000680: 0072 2700 0000 721c 0000 0072 0900 0000  .r'...r....r....
-00000690: 7209 0000 0072 0a00 0000 da11 6765 745f  r....r......get_
-000006a0: 6f62 6a65 6374 5f73 7472 696e 6727 0000  object_string'..
-000006b0: 0072 1500 0000 7a1e 4d6f 6465 6c42 7569  .r....z.ModelBui
-000006c0: 6c64 6572 2e67 6574 5f6f 626a 6563 745f  lder.get_object_
-000006d0: 7374 7269 6e67 4e29 09da 085f 5f6e 616d  stringN)...__nam
-000006e0: 655f 5fda 0a5f 5f6d 6f64 756c 655f 5fda  e__..__module__.
-000006f0: 0c5f 5f71 7561 6c6e 616d 655f 5f72 0b00  .__qualname__r..
-00000700: 0000 7214 0000 0072 1b00 0000 721d 0000  ..r....r....r...
-00000710: 0072 2700 0000 7228 0000 0072 0900 0000  .r'...r(...r....
-00000720: 7209 0000 0072 0900 0000 720a 0000 0072  r....r....r....r
-00000730: 0400 0000 0300 0000 730e 0000 0008 0008  ........s.......
-00000740: 0208 0508 0308 0508 030c 1272 0400 0000  ...........r....
-00000750: 6300 0000 0000 0000 0000 0000 0000 0000  c...............
-00000760: 0003 0000 0000 0000 0073 2400 0000 6500  .........s$...e.
-00000770: 5a01 6400 5a02 8700 6601 6401 6402 8408  Z.d.Z...f.d.d...
-00000780: 5a03 6403 6404 8400 5a04 8700 0400 5a05  Z.d.d...Z.....Z.
-00000790: 5300 2905 da0b 4d6f 6465 6c57 7269 7465  S.)...ModelWrite
-000007a0: 7263 0300 0000 0000 0000 0000 0000 0400  rc..............
-000007b0: 0000 0300 0000 0300 0000 7320 0000 007c  ..........s ...|
-000007c0: 027c 005f 007c 019b 0064 019d 027d 0374  .|._.|...d...}.t
-000007d0: 0183 00a0 027c 03a1 0101 0064 0053 0029  .....|.....d.S.)
-000007e0: 024e 7a0a 2f6d 6f64 656c 732e 7079 2903  .Nz./models.py).
-000007f0: da06 6d6f 6465 6c73 da05 7375 7065 7272  ..models..superr
-00000800: 0b00 0000 2904 7208 0000 00da 0861 7070  ....).r......app
-00000810: 5f6e 616d 6572 2d00 0000 da09 6669 6c65  _namer-.....file
-00000820: 5f6e 616d 65a9 01da 095f 5f63 6c61 7373  _name....__class
-00000830: 5f5f 7209 0000 0072 0a00 0000 720b 0000  __r....r....r...
-00000840: 002b 0000 0073 0600 0000 0601 0a01 1001  .+...s..........
-00000850: 7a14 4d6f 6465 6c57 7269 7465 722e 5f5f  z.ModelWriter.__
-00000860: 696e 6974 5f5f 6301 0000 0000 0000 0000  init__c.........
-00000870: 0000 0007 0000 0005 0000 0043 0000 0073  ...........C...s
-00000880: 4400 0000 6401 7d01 7c00 6a00 a001 a100  D...d.}.|.j.....
-00000890: 4400 5d18 5c02 7d02 7d03 7c03 6402 1900  D.].\.}.}.|.d...
-000008a0: 7d04 7c03 6403 1900 7d05 7402 7c02 7c04  }.|.d...}.t.|.|.
-000008b0: 7c05 8303 7d06 7c01 7c06 a003 a100 3700  |...}.|.|.....7.
-000008c0: 7d01 7107 7c01 5300 2904 4eda 0072 0600  }.q.|.S.).N..r..
-000008d0: 0000 7207 0000 0029 0472 2d00 0000 7221  ..r....).r-...r!
-000008e0: 0000 0072 0400 0000 7228 0000 0029 0772  ...r....r(...).r
-000008f0: 0800 0000 da0b 6675 6c6c 5f73 7472 696e  ......full_strin
-00000900: 6772 0500 0000 720e 0000 0072 0600 0000  gr....r....r....
-00000910: 7207 0000 00da 0762 7569 6c64 6572 7209  r......builderr.
-00000920: 0000 0072 0900 0000 720a 0000 00da 0f67  ...r....r......g
-00000930: 6574 5f66 756c 6c5f 7374 7269 6e67 3000  et_full_string0.
-00000940: 0000 730e 0000 0004 0112 0108 0108 010c  ..s.............
-00000950: 010e 0104 017a 1b4d 6f64 656c 5772 6974  .....z.ModelWrit
-00000960: 6572 2e67 6574 5f66 756c 6c5f 7374 7269  er.get_full_stri
-00000970: 6e67 2906 7229 0000 0072 2a00 0000 722b  ng).r)...r*...r+
-00000980: 0000 0072 0b00 0000 7236 0000 00da 0d5f  ...r....r6....._
-00000990: 5f63 6c61 7373 6365 6c6c 5f5f 7209 0000  _classcell__r...
-000009a0: 0072 0900 0000 7231 0000 0072 0a00 0000  .r....r1...r....
-000009b0: 722c 0000 0029 0000 0073 0600 0000 0800  r,...)...s......
-000009c0: 0c02 1005 722c 0000 004e 2905 da1c 636f  ....r,...N)...co
-000009d0: 6465 6c65 7373 5f64 6a61 6e67 6f2e 7772  deless_django.wr
-000009e0: 6974 6572 732e 6261 7365 7202 0000 0072  iters.baser....r
-000009f0: 0300 0000 7204 0000 0072 2c00 0000 7209  ....r....r,...r.
-00000a00: 0000 0072 0900 0000 7209 0000 0072 0a00  ...r....r....r..
-00000a10: 0000 da08 3c6d 6f64 756c 653e 0100 0000  ....<module>....
-00000a20: 7306 0000 0010 0010 0214 26              s.........&
+00000160: a900 7209 0000 00fa 5c2f 686f 6d65 2f6f  ..r.....\/home/o
+00000170: 6d61 722f 636f 6465 2f74 6573 742d 636c  mar/code/test-cl
+00000180: 642f 7665 6e76 2f6c 6962 2f70 7974 686f  d/venv/lib/pytho
+00000190: 6e33 2e31 302f 7369 7465 2d70 6163 6b61  n3.10/site-packa
+000001a0: 6765 732f 636f 6465 6c65 7373 5f64 6a61  ges/codeless_dja
+000001b0: 6e67 6f2f 7772 6974 6572 732f 6d6f 6465  ngo/writers/mode
+000001c0: 6c73 2e70 79da 085f 5f69 6e69 745f 5f05  ls.py..__init__.
+000001d0: 0000 0073 0600 0000 0601 0601 0a01 7a15  ...s..........z.
+000001e0: 4d6f 6465 6c42 7569 6c64 6572 2e5f 5f69  ModelBuilder.__i
+000001f0: 6e69 745f 5f63 0200 0000 0000 0000 0000  nit__c..........
+00000200: 0000 0200 0000 0400 0000 4300 0000 7314  ..........C...s.
+00000210: 0000 0064 01a0 0064 0264 0384 007c 0144  ...d...d.d...|.D
+00000220: 0083 01a1 0153 0029 044e 7a02 2c20 6301  .....S.).Nz., c.
+00000230: 0000 0000 0000 0000 0000 0002 0000 0006  ................
+00000240: 0000 0053 0000 0073 2200 0000 6700 7c00  ...S...s"...g.|.
+00000250: 5d0d 7d01 7c01 6400 1900 9b00 6401 7c01  ].}.|.d.....d.|.
+00000260: 6402 1900 9b00 9d03 9102 7102 5300 2903  d.........q.S.).
+00000270: da04 6e61 6d65 fa01 3dda 0576 616c 7565  ..name..=..value
+00000280: 7209 0000 0029 02da 022e 30da 036f 7074  r....)....0..opt
+00000290: 7209 0000 0072 0900 0000 720a 0000 00da  r....r....r.....
+000002a0: 0a3c 6c69 7374 636f 6d70 3e0b 0000 0073  .<listcomp>....s
+000002b0: 0200 0000 2200 7a32 4d6f 6465 6c42 7569  ....".z2ModelBui
+000002c0: 6c64 6572 2e67 6574 5f66 6965 6c64 5f6f  lder.get_field_o
+000002d0: 7074 696f 6e73 2e3c 6c6f 6361 6c73 3e2e  ptions.<locals>.
+000002e0: 3c6c 6973 7463 6f6d 703e 2901 da04 6a6f  <listcomp>)...jo
+000002f0: 696e 2902 7208 0000 00da 076f 7074 696f  in).r......optio
+00000300: 6e73 7209 0000 0072 0900 0000 720a 0000  nsr....r....r...
+00000310: 00da 1167 6574 5f66 6965 6c64 5f6f 7074  ...get_field_opt
+00000320: 696f 6e73 0a00 0000 f302 0000 0014 017a  ions...........z
+00000330: 1e4d 6f64 656c 4275 696c 6465 722e 6765  .ModelBuilder.ge
+00000340: 745f 6669 656c 645f 6f70 7469 6f6e 7363  t_field_optionsc
+00000350: 0400 0000 0000 0000 0000 0000 0500 0000  ................
+00000360: 0600 0000 4300 0000 7320 0000 007c 00a0  ....C...s ...|..
+00000370: 007c 03a1 017d 047c 019b 0064 017c 029b  .|...}.|...d.|..
+00000380: 0064 027c 049b 0064 039d 0653 0029 044e  .d.|...d...S.).N
+00000390: 7a0a 203d 206d 6f64 656c 732e fa01 28fa  z. = models...(.
+000003a0: 0129 2901 7214 0000 0029 0572 0800 0000  .)).r....).r....
+000003b0: da0a 6669 656c 645f 6e61 6d65 da0a 6669  ..field_name..fi
+000003c0: 656c 645f 7479 7065 7213 0000 00da 0d66  eld_typer......f
+000003d0: 6965 6c64 5f6f 7074 696f 6e73 7209 0000  ield_optionsr...
+000003e0: 0072 0900 0000 720a 0000 00da 1067 6574  .r....r......get
+000003f0: 5f66 6965 6c64 5f73 7472 696e 670d 0000  _field_string...
+00000400: 0073 0400 0000 0a01 1601 7a1d 4d6f 6465  .s........z.Mode
+00000410: 6c42 7569 6c64 6572 2e67 6574 5f66 6965  lBuilder.get_fie
+00000420: 6c64 5f73 7472 696e 6763 0100 0000 0000  ld_stringc......
+00000430: 0000 0000 0000 0100 0000 0300 0000 4300  ..............C.
+00000440: 0000 730e 0000 0064 017c 006a 009b 0064  ..s....d.|.j...d
+00000450: 029d 0353 0029 034e 7a06 636c 6173 7320  ...S.).Nz.class 
+00000460: 7a10 286d 6f64 656c 732e 4d6f 6465 6c29  z.(models.Model)
+00000470: 3a0a 2901 7205 0000 00a9 0172 0800 0000  :.).r......r....
+00000480: 7209 0000 0072 0900 0000 720a 0000 00da  r....r....r.....
+00000490: 1167 6574 5f6f 626a 6563 745f 6865 6164  .get_object_head
+000004a0: 6572 1200 0000 7302 0000 000e 017a 1e4d  er....s......z.M
+000004b0: 6f64 656c 4275 696c 6465 722e 6765 745f  odelBuilder.get_
+000004c0: 6f62 6a65 6374 5f68 6561 6465 7263 0100  object_headerc..
+000004d0: 0000 0000 0000 0000 0000 0a00 0000 0700  ................
+000004e0: 0000 4300 0000 7386 0000 0064 017d 017c  ..C...s....d.}.|
+000004f0: 006a 00a0 01a1 0044 005d 1b5c 027d 027d  .j.....D.].\.}.}
+00000500: 037c 0364 0219 007d 047c 0364 0319 007d  .|.d...}.|.d...}
+00000510: 057c 00a0 027c 027c 047c 05a1 037d 067c  .|...|.|.|...}.|
+00000520: 0164 047c 0617 0064 0117 0037 007d 0171  .d.|...d...7.}.q
+00000530: 077c 006a 0372 4164 057d 077c 006a 03a0  .|.j.rAd.}.|.j..
+00000540: 01a1 0044 005d 0f5c 027d 087d 097c 0764  ...D.].\.}.}.|.d
+00000550: 067c 089b 0064 077c 099b 0064 019d 0537  .|...d.|...d...7
+00000560: 007d 0771 2d7c 017c 0717 0053 007c 0153  .}.q-|.|...S.|.S
+00000570: 0029 084e da01 0ada 0474 7970 6572 1300  .).N.....typer..
+00000580: 0000 fa01 097a 0f0a 0963 6c61 7373 204d  .....z...class M
+00000590: 6574 613a 200a 7a02 0909 720d 0000 0029  eta: .z...r....)
+000005a0: 0472 0600 0000 da05 6974 656d 7372 1b00  .r......itemsr..
+000005b0: 0000 7207 0000 0029 0a72 0800 0000 da0a  ..r....).r......
+000005c0: 6d6f 6465 6c5f 626f 6479 7218 0000 00da  model_bodyr.....
+000005d0: 0676 616c 7565 7372 1900 0000 7213 0000  .valuesr....r...
+000005e0: 00da 0c66 6965 6c64 5f73 7472 696e 67da  ...field_string.
+000005f0: 096d 6574 615f 626f 6479 da03 6b65 7972  .meta_body..keyr
+00000600: 0e00 0000 7209 0000 0072 0900 0000 720a  ....r....r....r.
+00000610: 0000 00da 0f67 6574 5f6f 626a 6563 745f  .....get_object_
+00000620: 626f 6479 1500 0000 7318 0000 0004 0112  body....s.......
+00000630: 0108 0208 010e 0112 0106 0204 0112 0118  ................
+00000640: 0108 0204 027a 1c4d 6f64 656c 4275 696c  .....z.ModelBuil
+00000650: 6465 722e 6765 745f 6f62 6a65 6374 5f62  der.get_object_b
+00000660: 6f64 7963 0100 0000 0000 0000 0000 0000  odyc............
+00000670: 0100 0000 0300 0000 4300 0000 7314 0000  ........C...s...
+00000680: 007c 00a0 00a1 007c 00a0 01a1 0017 0064  .|.....|.......d
+00000690: 0117 0053 0029 024e 721e 0000 0029 0272  ...S.).Nr....).r
+000006a0: 1d00 0000 7227 0000 0072 1c00 0000 7209  ....r'...r....r.
+000006b0: 0000 0072 0900 0000 720a 0000 00da 1167  ...r....r......g
+000006c0: 6574 5f6f 626a 6563 745f 7374 7269 6e67  et_object_string
+000006d0: 2700 0000 7215 0000 007a 1e4d 6f64 656c  '...r....z.Model
+000006e0: 4275 696c 6465 722e 6765 745f 6f62 6a65  Builder.get_obje
+000006f0: 6374 5f73 7472 696e 674e 2909 da08 5f5f  ct_stringN)...__
+00000700: 6e61 6d65 5f5f da0a 5f5f 6d6f 6475 6c65  name__..__module
+00000710: 5f5f da0c 5f5f 7175 616c 6e61 6d65 5f5f  __..__qualname__
+00000720: 720b 0000 0072 1400 0000 721b 0000 0072  r....r....r....r
+00000730: 1d00 0000 7227 0000 0072 2800 0000 7209  ....r'...r(...r.
+00000740: 0000 0072 0900 0000 7209 0000 0072 0a00  ...r....r....r..
+00000750: 0000 7204 0000 0003 0000 0073 0e00 0000  ..r........s....
+00000760: 0800 0802 0805 0803 0805 0803 0c12 7204  ..............r.
+00000770: 0000 0063 0000 0000 0000 0000 0000 0000  ...c............
+00000780: 0000 0000 0300 0000 0000 0000 7324 0000  ............s$..
+00000790: 0065 005a 0164 005a 0287 0066 0164 0164  .e.Z.d.Z...f.d.d
+000007a0: 0284 085a 0364 0364 0484 005a 0487 0004  ...Z.d.d...Z....
+000007b0: 005a 0553 0029 05da 0b4d 6f64 656c 5772  .Z.S.)...ModelWr
+000007c0: 6974 6572 6303 0000 0000 0000 0000 0000  iterc...........
+000007d0: 0004 0000 0003 0000 0003 0000 0073 2000  .............s .
+000007e0: 0000 7c02 7c00 5f00 7c01 9b00 6401 9d02  ..|.|._.|...d...
+000007f0: 7d03 7401 8300 a002 7c03 a101 0100 6400  }.t.....|.....d.
+00000800: 5300 2902 4e7a 0a2f 6d6f 6465 6c73 2e70  S.).Nz./models.p
+00000810: 7929 03da 066d 6f64 656c 73da 0573 7570  y)...models..sup
+00000820: 6572 720b 0000 0029 0472 0800 0000 da08  err....).r......
+00000830: 6170 705f 6e61 6d65 722d 0000 00da 0966  app_namer-.....f
+00000840: 696c 655f 6e61 6d65 a901 da09 5f5f 636c  ile_name....__cl
+00000850: 6173 735f 5f72 0900 0000 720a 0000 0072  ass__r....r....r
+00000860: 0b00 0000 2b00 0000 7306 0000 0006 010a  ....+...s.......
+00000870: 0110 017a 144d 6f64 656c 5772 6974 6572  ...z.ModelWriter
+00000880: 2e5f 5f69 6e69 745f 5f63 0100 0000 0000  .__init__c......
+00000890: 0000 0000 0000 0700 0000 0500 0000 4300  ..............C.
+000008a0: 0000 7344 0000 0064 017d 017c 006a 00a0  ..sD...d.}.|.j..
+000008b0: 01a1 0044 005d 185c 027d 027d 037c 0364  ...D.].\.}.}.|.d
+000008c0: 0219 007d 047c 0364 0319 007d 0574 027c  ...}.|.d...}.t.|
+000008d0: 027c 047c 0583 037d 067c 017c 06a0 03a1  .|.|...}.|.|....
+000008e0: 0037 007d 0171 077c 0153 0029 044e da00  .7.}.q.|.S.).N..
+000008f0: 7206 0000 0072 0700 0000 2904 722d 0000  r....r....).r-..
+00000900: 0072 2100 0000 7204 0000 0072 2800 0000  .r!...r....r(...
+00000910: 2907 7208 0000 00da 0b66 756c 6c5f 7374  ).r......full_st
+00000920: 7269 6e67 7205 0000 0072 0e00 0000 7206  ringr....r....r.
+00000930: 0000 0072 0700 0000 da07 6275 696c 6465  ...r......builde
+00000940: 7272 0900 0000 7209 0000 0072 0a00 0000  rr....r....r....
+00000950: da0f 6765 745f 6675 6c6c 5f73 7472 696e  ..get_full_strin
+00000960: 6730 0000 0073 0e00 0000 0401 1201 0801  g0...s..........
+00000970: 0801 0c01 0e01 0401 7a1b 4d6f 6465 6c57  ........z.ModelW
+00000980: 7269 7465 722e 6765 745f 6675 6c6c 5f73  riter.get_full_s
+00000990: 7472 696e 6729 0672 2900 0000 722a 0000  tring).r)...r*..
+000009a0: 0072 2b00 0000 720b 0000 0072 3600 0000  .r+...r....r6...
+000009b0: da0d 5f5f 636c 6173 7363 656c 6c5f 5f72  ..__classcell__r
+000009c0: 0900 0000 7209 0000 0072 3100 0000 720a  ....r....r1...r.
+000009d0: 0000 0072 2c00 0000 2900 0000 7306 0000  ...r,...)...s...
+000009e0: 0008 000c 0210 0572 2c00 0000 4e29 05da  .......r,...N)..
+000009f0: 1c63 6f64 656c 6573 735f 646a 616e 676f  .codeless_django
+00000a00: 2e77 7269 7465 7273 2e62 6173 6572 0200  .writers.baser..
+00000a10: 0000 7203 0000 0072 0400 0000 722c 0000  ..r....r....r,..
+00000a20: 0072 0900 0000 7209 0000 0072 0900 0000  .r....r....r....
+00000a30: 720a 0000 00da 083c 6d6f 6475 6c65 3e01  r......<module>.
+00000a40: 0000 0073 0600 0000 1000 1002 1426       ...s.........&
```

### Comparing `codeless-django-0.0.14/codeless_django/writers/__pycache__/serializers.cpython-310.pyc` & `codeless-django-0.0.15/codeless_django/writers/__pycache__/serializers.cpython-310.pyc`

 * *Format-specific differences are supported for Python .pyc files but no file-specific differences were detected; falling back to a binary diff. file(1) reports: Byte-compiled Python module for CPython 3.10, timestamp-based, .py timestamp: Wed May 31 02:46:22 2023 UTC, .py size: 1150 bytes*

 * *Could not decompile bytecode: bad marshal data (unknown type code)*

 * *Files 3% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-00000000: 6f0d 0d0a 0000 0000 feb4 7664 7e04 0000  o.........vd~...
+00000000: 6f0d 0d0a 0000 0000 6f28 bd64 7e04 0000  o.......o(.d~...
 00000010: e300 0000 0000 0000 0000 0000 0000 0000  ................
 00000020: 0004 0000 0040 0000 0073 3c00 0000 6400  .....@...s<...d.
 00000030: 6401 6c00 5a00 6400 6402 6c01 6d02 5a02  d.l.Z.d.d.l.m.Z.
 00000040: 6d03 5a03 0100 4700 6403 6404 8400 6404  m.Z...G.d.d...d.
 00000050: 6503 8303 5a04 4700 6405 6406 8400 6406  e...Z.G.d.d...d.
 00000060: 6502 8303 5a05 6401 5300 2907 e900 0000  e...Z.d.S.).....
 00000070: 004e 2902 da0a 4261 7365 5772 6974 6572  .N)...BaseWriter
@@ -14,104 +14,106 @@
 000000d0: 08da 164d 6f64 656c 5365 7269 616c 697a  ...ModelSerializ
 000000e0: 6572 4275 696c 6465 7263 0300 0000 0000  erBuilderc......
 000000f0: 0000 0000 0000 0300 0000 0200 0000 4300  ..............C.
 00000100: 0000 7310 0000 007c 027c 005f 007c 017c  ..s....|.|._.|.|
 00000110: 005f 0164 0053 0029 014e 2902 da0a 6d6f  ._.d.S.).N)...mo
 00000120: 6465 6c5f 6e61 6d65 da08 6170 705f 6e61  del_name..app_na
 00000130: 6d65 2903 da04 7365 6c66 7206 0000 0072  me)...selfr....r
-00000140: 0500 0000 a900 7208 0000 00fa 3e2f 686f  ......r.....>/ho
-00000150: 6d65 2f6f 6d61 722f 636f 6465 2f51 7569  me/omar/code/Qui
-00000160: 636b 446a 2f63 6f64 656c 6573 735f 646a  ckDj/codeless_dj
-00000170: 616e 676f 2f77 7269 7465 7273 2f73 6572  ango/writers/ser
-00000180: 6961 6c69 7a65 7273 2e70 79da 085f 5f69  ializers.py..__i
-00000190: 6e69 745f 5f07 0000 0073 0400 0000 0601  nit__....s......
-000001a0: 0a01 7a1f 4d6f 6465 6c53 6572 6961 6c69  ..z.ModelSeriali
-000001b0: 7a65 7242 7569 6c64 6572 2e5f 5f69 6e69  zerBuilder.__ini
-000001c0: 745f 5f63 0100 0000 0000 0000 0000 0000  t__c............
-000001d0: 0100 0000 0300 0000 4300 0000 730e 0000  ........C...s...
-000001e0: 0064 017c 006a 009b 0064 029d 0353 0029  .d.|.j...d...S.)
-000001f0: 034e 7a06 636c 6173 7320 7a37 5365 7269  .Nz.class z7Seri
-00000200: 616c 697a 6572 2873 6572 6961 6c69 7a65  alizer(serialize
-00000210: 7273 2e4d 6f64 656c 5365 7269 616c 697a  rs.ModelSerializ
-00000220: 6572 293a 0a0a 0963 6c61 7373 204d 6574  er):...class Met
-00000230: 613a 0a29 0172 0500 0000 a901 7207 0000  a:.).r......r...
-00000240: 0072 0800 0000 7208 0000 0072 0900 0000  .r....r....r....
-00000250: da11 6765 745f 6f62 6a65 6374 5f68 6561  ..get_object_hea
-00000260: 6465 720b 0000 0073 0200 0000 0e01 7a28  der....s......z(
-00000270: 4d6f 6465 6c53 6572 6961 6c69 7a65 7242  ModelSerializerB
-00000280: 7569 6c64 6572 2e67 6574 5f6f 626a 6563  uilder.get_objec
-00000290: 745f 6865 6164 6572 6301 0000 0000 0000  t_headerc.......
-000002a0: 0000 0000 0001 0000 0005 0000 0043 0000  .............C..
-000002b0: 0073 1600 0000 6401 7c00 6a00 9b00 6402  .s....d.|.j...d.
-000002c0: 7c00 6a01 9b00 6403 9d05 5300 2904 4e7a  |.j...d...S.).Nz
-000002d0: 0a09 096d 6f64 656c 203d 207a 085f 6d6f  ...model = z._mo
-000002e0: 6465 6c73 2e7a 150a 0909 6669 656c 6473  dels.z....fields
-000002f0: 203d 2027 5f5f 616c 6c5f 5f27 2902 7206   = '__all__').r.
-00000300: 0000 0072 0500 0000 720b 0000 0072 0800  ...r....r....r..
-00000310: 0000 7208 0000 0072 0900 0000 da0f 6765  ..r....r......ge
-00000320: 745f 6f62 6a65 6374 5f62 6f64 790e 0000  t_object_body...
-00000330: 0073 0200 0000 1601 7a26 4d6f 6465 6c53  .s......z&ModelS
-00000340: 6572 6961 6c69 7a65 7242 7569 6c64 6572  erializerBuilder
-00000350: 2e67 6574 5f6f 626a 6563 745f 626f 6479  .get_object_body
-00000360: 4e29 06da 085f 5f6e 616d 655f 5fda 0a5f  N)...__name__.._
-00000370: 5f6d 6f64 756c 655f 5fda 0c5f 5f71 7561  _module__..__qua
-00000380: 6c6e 616d 655f 5f72 0a00 0000 720c 0000  lname__r....r...
-00000390: 0072 0d00 0000 7208 0000 0072 0800 0000  .r....r....r....
-000003a0: 7208 0000 0072 0900 0000 7204 0000 0005  r....r....r.....
-000003b0: 0000 0073 0800 0000 0800 0802 0804 0c03  ...s............
-000003c0: 7204 0000 0063 0000 0000 0000 0000 0000  r....c..........
-000003d0: 0000 0000 0000 0300 0000 0000 0000 7324  ..............s$
-000003e0: 0000 0065 005a 0164 005a 0287 0066 0164  ...e.Z.d.Z...f.d
-000003f0: 0164 0284 085a 0364 0364 0484 005a 0487  .d...Z.d.d...Z..
-00000400: 0004 005a 0553 0029 05da 154d 6f64 656c  ...Z.S.)...Model
-00000410: 5365 7269 616c 697a 6572 5772 6974 6572  SerializerWriter
-00000420: 6303 0000 0000 0000 0000 0000 0005 0000  c...............
-00000430: 0008 0000 0003 0000 0073 6600 0000 7c01  .........sf...|.
-00000440: 7c00 5f00 7c02 7c00 5f01 7c01 9b00 6401  |._.|.|._.|...d.
-00000450: 9d02 7d03 7402 6a03 a004 7c03 a101 732b  ..}.t.j...|...s+
-00000460: 7405 7c03 6402 8302 8f0d 7d04 7c04 a006  t.|.d.....}.|...
-00000470: 6403 a101 0100 5700 6400 0400 0400 8303  d.....W.d.......
-00000480: 0100 6e08 3100 7326 7701 0100 0100 0100  ..n.1.s&w.......
-00000490: 5900 0100 7407 8300 a008 7c03 a101 0100  Y...t.....|.....
-000004a0: 6400 5300 2904 4e7a 0f2f 7365 7269 616c  d.S.).Nz./serial
-000004b0: 697a 6572 732e 7079 da01 617a 2a66 726f  izers.py..az*fro
-000004c0: 6d20 7265 7374 5f66 7261 6d65 776f 726b  m rest_framework
-000004d0: 2069 6d70 6f72 7420 7365 7269 616c 697a   import serializ
-000004e0: 6572 7320 0a20 0a29 0972 0600 0000 da06  ers . .).r......
-000004f0: 6d6f 6465 6c73 da02 6f73 da04 7061 7468  models..os..path
-00000500: da06 6578 6973 7473 da04 6f70 656e da05  ..exists..open..
-00000510: 7772 6974 65da 0573 7570 6572 720a 0000  write..superr...
-00000520: 0029 0572 0700 0000 7206 0000 0072 1300  .).r....r....r..
-00000530: 0000 da09 6669 6c65 5f6e 616d 65da 0166  ....file_name..f
-00000540: a901 da09 5f5f 636c 6173 735f 5f72 0800  ....__class__r..
-00000550: 0000 7209 0000 0072 0a00 0000 1300 0000  ..r....r........
-00000560: 7310 0000 0006 0106 010a 010c 020c 010c  s...............
-00000570: 011c ff10 027a 1e4d 6f64 656c 5365 7269  .....z.ModelSeri
-00000580: 616c 697a 6572 5772 6974 6572 2e5f 5f69  alizerWriter.__i
-00000590: 6e69 745f 5f63 0100 0000 0000 0000 0000  nit__c..........
-000005a0: 0000 0400 0000 0500 0000 4300 0000 7330  ..........C...s0
-000005b0: 0000 007c 006a 007d 0164 017d 027c 006a  ...|.j.}.d.}.|.j
-000005c0: 01a0 02a1 0044 005d 0b7d 037c 0274 037c  .....D.].}.|.t.|
-000005d0: 017c 0383 02a0 04a1 0037 007d 0271 0a7c  .|.......7.}.q.|
-000005e0: 0253 0029 024e da00 2905 7206 0000 0072  .S.).N..).r....r
-000005f0: 1300 0000 da04 6b65 7973 7204 0000 00da  ......keysr.....
-00000600: 1167 6574 5f6f 626a 6563 745f 7374 7269  .get_object_stri
-00000610: 6e67 2904 7207 0000 0072 0600 0000 da0b  ng).r....r......
-00000620: 6675 6c6c 5f73 7472 696e 6772 0500 0000  full_stringr....
-00000630: 7208 0000 0072 0800 0000 7209 0000 00da  r....r....r.....
-00000640: 0f67 6574 5f66 756c 6c5f 7374 7269 6e67  .get_full_string
-00000650: 1d00 0000 730a 0000 0006 0104 010e 0114  ....s...........
-00000660: 0104 027a 254d 6f64 656c 5365 7269 616c  ...z%ModelSerial
-00000670: 697a 6572 5772 6974 6572 2e67 6574 5f66  izerWriter.get_f
-00000680: 756c 6c5f 7374 7269 6e67 2906 720e 0000  ull_string).r...
-00000690: 0072 0f00 0000 7210 0000 0072 0a00 0000  .r....r....r....
-000006a0: 7222 0000 00da 0d5f 5f63 6c61 7373 6365  r".....__classce
-000006b0: 6c6c 5f5f 7208 0000 0072 0800 0000 721c  ll__r....r....r.
-000006c0: 0000 0072 0900 0000 7211 0000 0012 0000  ...r....r.......
-000006d0: 0073 0600 0000 0800 0c01 100a 7211 0000  .s..........r...
-000006e0: 0029 0672 1400 0000 da1c 636f 6465 6c65  .).r......codele
-000006f0: 7373 5f64 6a61 6e67 6f2e 7772 6974 6572  ss_django.writer
-00000700: 732e 6261 7365 7202 0000 0072 0300 0000  s.baser....r....
-00000710: 7204 0000 0072 1100 0000 7208 0000 0072  r....r....r....r
-00000720: 0800 0000 7208 0000 0072 0900 0000 da08  ....r....r......
-00000730: 3c6d 6f64 756c 653e 0100 0000 7308 0000  <module>....s...
-00000740: 0008 0110 0110 0214 0d                   .........
+00000140: 0500 0000 a900 7208 0000 00fa 612f 686f  ......r.....a/ho
+00000150: 6d65 2f6f 6d61 722f 636f 6465 2f74 6573  me/omar/code/tes
+00000160: 742d 636c 642f 7665 6e76 2f6c 6962 2f70  t-cld/venv/lib/p
+00000170: 7974 686f 6e33 2e31 302f 7369 7465 2d70  ython3.10/site-p
+00000180: 6163 6b61 6765 732f 636f 6465 6c65 7373  ackages/codeless
+00000190: 5f64 6a61 6e67 6f2f 7772 6974 6572 732f  _django/writers/
+000001a0: 7365 7269 616c 697a 6572 732e 7079 da08  serializers.py..
+000001b0: 5f5f 696e 6974 5f5f 0700 0000 7304 0000  __init__....s...
+000001c0: 0006 010a 017a 1f4d 6f64 656c 5365 7269  .....z.ModelSeri
+000001d0: 616c 697a 6572 4275 696c 6465 722e 5f5f  alizerBuilder.__
+000001e0: 696e 6974 5f5f 6301 0000 0000 0000 0000  init__c.........
+000001f0: 0000 0001 0000 0003 0000 0043 0000 0073  ...........C...s
+00000200: 0e00 0000 6401 7c00 6a00 9b00 6402 9d03  ....d.|.j...d...
+00000210: 5300 2903 4e7a 0663 6c61 7373 207a 3753  S.).Nz.class z7S
+00000220: 6572 6961 6c69 7a65 7228 7365 7269 616c  erializer(serial
+00000230: 697a 6572 732e 4d6f 6465 6c53 6572 6961  izers.ModelSeria
+00000240: 6c69 7a65 7229 3a0a 0a09 636c 6173 7320  lizer):...class 
+00000250: 4d65 7461 3a0a 2901 7205 0000 00a9 0172  Meta:.).r......r
+00000260: 0700 0000 7208 0000 0072 0800 0000 7209  ....r....r....r.
+00000270: 0000 00da 1167 6574 5f6f 626a 6563 745f  .....get_object_
+00000280: 6865 6164 6572 0b00 0000 7302 0000 000e  header....s.....
+00000290: 017a 284d 6f64 656c 5365 7269 616c 697a  .z(ModelSerializ
+000002a0: 6572 4275 696c 6465 722e 6765 745f 6f62  erBuilder.get_ob
+000002b0: 6a65 6374 5f68 6561 6465 7263 0100 0000  ject_headerc....
+000002c0: 0000 0000 0000 0000 0100 0000 0500 0000  ................
+000002d0: 4300 0000 7316 0000 0064 017c 006a 009b  C...s....d.|.j..
+000002e0: 0064 027c 006a 019b 0064 039d 0553 0029  .d.|.j...d...S.)
+000002f0: 044e 7a0a 0909 6d6f 6465 6c20 3d20 7a08  .Nz...model = z.
+00000300: 5f6d 6f64 656c 732e 7a15 0a09 0966 6965  _models.z....fie
+00000310: 6c64 7320 3d20 275f 5f61 6c6c 5f5f 2729  lds = '__all__')
+00000320: 0272 0600 0000 7205 0000 0072 0b00 0000  .r....r....r....
+00000330: 7208 0000 0072 0800 0000 7209 0000 00da  r....r....r.....
+00000340: 0f67 6574 5f6f 626a 6563 745f 626f 6479  .get_object_body
+00000350: 0e00 0000 7302 0000 0016 017a 264d 6f64  ....s......z&Mod
+00000360: 656c 5365 7269 616c 697a 6572 4275 696c  elSerializerBuil
+00000370: 6465 722e 6765 745f 6f62 6a65 6374 5f62  der.get_object_b
+00000380: 6f64 794e 2906 da08 5f5f 6e61 6d65 5f5f  odyN)...__name__
+00000390: da0a 5f5f 6d6f 6475 6c65 5f5f da0c 5f5f  ..__module__..__
+000003a0: 7175 616c 6e61 6d65 5f5f 720a 0000 0072  qualname__r....r
+000003b0: 0c00 0000 720d 0000 0072 0800 0000 7208  ....r....r....r.
+000003c0: 0000 0072 0800 0000 7209 0000 0072 0400  ...r....r....r..
+000003d0: 0000 0500 0000 7308 0000 0008 0008 0208  ......s.........
+000003e0: 040c 0372 0400 0000 6300 0000 0000 0000  ...r....c.......
+000003f0: 0000 0000 0000 0000 0003 0000 0000 0000  ................
+00000400: 0073 2400 0000 6500 5a01 6400 5a02 8700  .s$...e.Z.d.Z...
+00000410: 6601 6401 6402 8408 5a03 6403 6404 8400  f.d.d...Z.d.d...
+00000420: 5a04 8700 0400 5a05 5300 2905 da15 4d6f  Z.....Z.S.)...Mo
+00000430: 6465 6c53 6572 6961 6c69 7a65 7257 7269  delSerializerWri
+00000440: 7465 7263 0300 0000 0000 0000 0000 0000  terc............
+00000450: 0500 0000 0800 0000 0300 0000 7366 0000  ............sf..
+00000460: 007c 017c 005f 007c 027c 005f 017c 019b  .|.|._.|.|._.|..
+00000470: 0064 019d 027d 0374 026a 03a0 047c 03a1  .d...}.t.j...|..
+00000480: 0173 2b74 057c 0364 0283 028f 0d7d 047c  .s+t.|.d.....}.|
+00000490: 04a0 0664 03a1 0101 0057 0064 0004 0004  ...d.....W.d....
+000004a0: 0083 0301 006e 0831 0073 2677 0101 0001  .....n.1.s&w....
+000004b0: 0001 0059 0001 0074 0783 00a0 087c 03a1  ...Y...t.....|..
+000004c0: 0101 0064 0053 0029 044e 7a0f 2f73 6572  ...d.S.).Nz./ser
+000004d0: 6961 6c69 7a65 7273 2e70 79da 0161 7a2a  ializers.py..az*
+000004e0: 6672 6f6d 2072 6573 745f 6672 616d 6577  from rest_framew
+000004f0: 6f72 6b20 696d 706f 7274 2073 6572 6961  ork import seria
+00000500: 6c69 7a65 7273 200a 200a 2909 7206 0000  lizers . .).r...
+00000510: 00da 066d 6f64 656c 73da 026f 73da 0470  ...models..os..p
+00000520: 6174 68da 0665 7869 7374 73da 046f 7065  ath..exists..ope
+00000530: 6eda 0577 7269 7465 da05 7375 7065 7272  n..write..superr
+00000540: 0a00 0000 2905 7207 0000 0072 0600 0000  ....).r....r....
+00000550: 7213 0000 00da 0966 696c 655f 6e61 6d65  r......file_name
+00000560: da01 66a9 01da 095f 5f63 6c61 7373 5f5f  ..f....__class__
+00000570: 7208 0000 0072 0900 0000 720a 0000 0013  r....r....r.....
+00000580: 0000 0073 1000 0000 0601 0601 0a01 0c02  ...s............
+00000590: 0c01 0c01 1cff 1002 7a1e 4d6f 6465 6c53  ........z.ModelS
+000005a0: 6572 6961 6c69 7a65 7257 7269 7465 722e  erializerWriter.
+000005b0: 5f5f 696e 6974 5f5f 6301 0000 0000 0000  __init__c.......
+000005c0: 0000 0000 0004 0000 0005 0000 0043 0000  .............C..
+000005d0: 0073 3000 0000 7c00 6a00 7d01 6401 7d02  .s0...|.j.}.d.}.
+000005e0: 7c00 6a01 a002 a100 4400 5d0b 7d03 7c02  |.j.....D.].}.|.
+000005f0: 7403 7c01 7c03 8302 a004 a100 3700 7d02  t.|.|.......7.}.
+00000600: 710a 7c02 5300 2902 4eda 0029 0572 0600  q.|.S.).N..).r..
+00000610: 0000 7213 0000 00da 046b 6579 7372 0400  ..r......keysr..
+00000620: 0000 da11 6765 745f 6f62 6a65 6374 5f73  ....get_object_s
+00000630: 7472 696e 6729 0472 0700 0000 7206 0000  tring).r....r...
+00000640: 00da 0b66 756c 6c5f 7374 7269 6e67 7205  ...full_stringr.
+00000650: 0000 0072 0800 0000 7208 0000 0072 0900  ...r....r....r..
+00000660: 0000 da0f 6765 745f 6675 6c6c 5f73 7472  ....get_full_str
+00000670: 696e 671d 0000 0073 0a00 0000 0601 0401  ing....s........
+00000680: 0e01 1401 0402 7a25 4d6f 6465 6c53 6572  ......z%ModelSer
+00000690: 6961 6c69 7a65 7257 7269 7465 722e 6765  ializerWriter.ge
+000006a0: 745f 6675 6c6c 5f73 7472 696e 6729 0672  t_full_string).r
+000006b0: 0e00 0000 720f 0000 0072 1000 0000 720a  ....r....r....r.
+000006c0: 0000 0072 2200 0000 da0d 5f5f 636c 6173  ...r".....__clas
+000006d0: 7363 656c 6c5f 5f72 0800 0000 7208 0000  scell__r....r...
+000006e0: 0072 1c00 0000 7209 0000 0072 1100 0000  .r....r....r....
+000006f0: 1200 0000 7306 0000 0008 000c 0110 0a72  ....s..........r
+00000700: 1100 0000 2906 7214 0000 00da 1c63 6f64  ....).r......cod
+00000710: 656c 6573 735f 646a 616e 676f 2e77 7269  eless_django.wri
+00000720: 7465 7273 2e62 6173 6572 0200 0000 7203  ters.baser....r.
+00000730: 0000 0072 0400 0000 7211 0000 0072 0800  ...r....r....r..
+00000740: 0000 7208 0000 0072 0800 0000 7209 0000  ..r....r....r...
+00000750: 00da 083c 6d6f 6475 6c65 3e01 0000 0073  ...<module>....s
+00000760: 0800 0000 0801 1001 1002 140d            ............
```

### Comparing `codeless-django-0.0.14/codeless_django/writers/__pycache__/urls.cpython-310.pyc` & `codeless-django-0.0.15/codeless_django/writers/__pycache__/urls.cpython-310.pyc`

 * *Format-specific differences are supported for Python .pyc files but no file-specific differences were detected; falling back to a binary diff. file(1) reports: Byte-compiled Python module for CPython 3.10, timestamp-based, .py timestamp: Thu Jun  1 02:10:37 2023 UTC, .py size: 1933 bytes*

 * *Could not decompile bytecode: bad marshal data (unknown type code)*

 * *Files 7% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-00000000: 6f0d 0d0a 0000 0000 1dfe 7764 8d07 0000  o.........wd....
+00000000: 6f0d 0d0a 0000 0000 6f28 bd64 8d07 0000  o.......o(.d....
 00000010: e300 0000 0000 0000 0000 0000 0000 0000  ................
 00000020: 0004 0000 0040 0000 0073 3000 0000 6400  .....@...s0...d.
 00000030: 6401 6c00 6d01 5a01 0100 4700 6402 6403  d.l.m.Z...G.d.d.
 00000040: 8400 6403 6501 8303 5a02 4700 6404 6405  ..d.e...Z.G.d.d.
 00000050: 8400 6405 6501 8303 5a03 6406 5300 2907  ..d.e...Z.d.S.).
 00000060: e900 0000 0029 01da 0a42 6173 6557 7269  .....)...BaseWri
 00000070: 7465 7263 0000 0000 0000 0000 0000 0000  terc............
@@ -16,103 +16,105 @@
 000000f0: 6401 9d02 7d03 7402 8300 a003 7c03 a101  d...}.t.....|...
 00000100: 0100 6400 5300 a902 4e7a 082f 7572 6c73  ..d.S...Nz./urls
 00000110: 2e70 79a9 04da 066d 6f64 656c 73da 0861  .py....models..a
 00000120: 7070 5f6e 616d 65da 0573 7570 6572 da08  pp_name..super..
 00000130: 5f5f 696e 6974 5f5f a904 da04 7365 6c66  __init__....self
 00000140: 7209 0000 0072 0800 0000 da09 6669 6c65  r....r......file
 00000150: 5f6e 616d 65a9 01da 095f 5f63 6c61 7373  _name....__class
-00000160: 5f5f a900 fa37 2f68 6f6d 652f 6f6d 6172  __...7/home/omar
-00000170: 2f63 6f64 652f 5175 6963 6b44 6a2f 636f  /code/QuickDj/co
-00000180: 6465 6c65 7373 5f64 6a61 6e67 6f2f 7772  deless_django/wr
-00000190: 6974 6572 732f 7572 6c73 2e70 7972 0b00  iters/urls.pyr..
-000001a0: 0000 0600 0000 f308 0000 0006 0106 010a  ................
-000001b0: 0110 017a 1255 524c 5772 6974 6572 2e5f  ...z.URLWriter._
-000001c0: 5f69 6e69 745f 5f63 0100 0000 0000 0000  _init__c........
-000001d0: 0000 0000 0600 0000 0900 0000 4300 0000  ............C...
-000001e0: 73a0 0000 0064 017d 0164 027d 027c 006a  s....d.}.d.}.|.j
-000001f0: 00a0 01a1 0044 005d 3e7d 0364 027d 047c  .....D.]>}.d.}.|
-00000200: 0464 037c 03a0 02a1 009b 0064 047c 039b  .d.|.......d.|..
-00000210: 0064 057c 03a0 02a1 009b 0064 069d 0737  .d.|.......d...7
-00000220: 007d 047c 0464 037c 03a0 02a1 009b 0064  .}.|.d.|.......d
-00000230: 077c 039b 0064 087c 03a0 02a1 009b 0064  .|...d.|.......d
-00000240: 099d 0737 007d 047c 0464 037c 03a0 02a1  ...7.}.|.d.|....
-00000250: 009b 0064 0a7c 039b 0064 0b7c 03a0 02a1  ...d.|...d.|....
-00000260: 009b 0064 0c9d 0737 007d 047c 027c 0437  ...d...7.}.|.|.7
-00000270: 007d 0271 097c 017c 0217 0064 0d17 007d  .}.q.|.|...d...}
-00000280: 057c 0553 0029 0e4e fa12 7572 6c70 6174  .|.S.).N..urlpat
-00000290: 7465 726e 7320 2b3d 205b 200a da00 fa0a  terns += [ .....
-000002a0: 2020 2020 7061 7468 2827 7a0f 2f6c 6973      path('z./lis
-000002b0: 742f 272c 2076 6965 7773 2e7a 1a4c 6973  t/', views.z.Lis
-000002c0: 7456 6965 772e 6173 5f76 6965 7728 292c  tView.as_view(),
-000002d0: 206e 616d 653d 277a 095f 6c69 7374 2729   name='z._list')
-000002e0: 2c0a 7a11 2f63 7265 6174 652f 272c 2076  ,.z./create/', v
-000002f0: 6965 7773 2e7a 1c43 7265 6174 6556 6965  iews.z.CreateVie
-00000300: 772e 6173 5f76 6965 7728 292c 206e 616d  w.as_view(), nam
-00000310: 653d 277a 0b5f 6372 6561 7465 2729 2c0a  e='z._create'),.
-00000320: 7a13 2f3c 696e 743a 706b 3e2f 272c 2076  z./<int:pk>/', v
-00000330: 6965 7773 2e7a 1c44 6574 6169 6c56 6965  iews.z.DetailVie
-00000340: 772e 6173 5f76 6965 7728 292c 206e 616d  w.as_view(), nam
-00000350: 653d 277a 0b5f 6465 7461 696c 2729 2c0a  e='z._detail'),.
-00000360: fa06 0a20 5d20 0a0a a903 7208 0000 00da  ... ] ....r.....
-00000370: 046b 6579 73da 056c 6f77 6572 a906 720d  .keys..lower..r.
-00000380: 0000 00da 0e69 6e69 7469 616c 5f73 7472  .....initial_str
-00000390: 696e 67da 1075 726c 5f70 6174 685f 7374  ing..url_path_st
-000003a0: 7269 6e67 73da 0a6d 6f64 656c 5f6e 616d  rings..model_nam
-000003b0: 65da 0a75 726c 5f73 7472 696e 67da 0b66  e..url_string..f
-000003c0: 756c 6c5f 7374 7269 6e67 7211 0000 0072  ull_stringr....r
-000003d0: 1100 0000 7212 0000 00da 0f67 6574 5f66  ....r......get_f
-000003e0: 756c 6c5f 7374 7269 6e67 0c00 0000 7314  ull_string....s.
-000003f0: 0000 0004 0104 010e 0204 0124 0124 0124  ...........$.$.$
-00000400: 010a 010c 0204 017a 1955 524c 5772 6974  .......z.URLWrit
-00000410: 6572 2e67 6574 5f66 756c 6c5f 7374 7269  er.get_full_stri
-00000420: 6e67 a906 da08 5f5f 6e61 6d65 5f5f da0a  ng....__name__..
-00000430: 5f5f 6d6f 6475 6c65 5f5f da0c 5f5f 7175  __module__..__qu
-00000440: 616c 6e61 6d65 5f5f 720b 0000 0072 2100  alname__r....r!.
-00000450: 0000 da0d 5f5f 636c 6173 7363 656c 6c5f  ....__classcell_
-00000460: 5f72 1100 0000 7211 0000 0072 0f00 0000  _r....r....r....
-00000470: 7212 0000 0072 0400 0000 0500 0000 f306  r....r..........
-00000480: 0000 0008 000c 0110 0672 0400 0000 6300  .........r....c.
-00000490: 0000 0000 0000 0000 0000 0000 0000 0003  ................
-000004a0: 0000 0000 0000 0072 0300 0000 2905 da0c  .......r....)...
-000004b0: 4150 4955 726c 5772 6974 6572 6303 0000  APIUrlWriterc...
-000004c0: 0000 0000 0000 0000 0004 0000 0003 0000  ................
-000004d0: 0003 0000 0072 0500 0000 7206 0000 0072  .....r....r....r
-000004e0: 0700 0000 720c 0000 0072 0f00 0000 7211  ....r....r....r.
-000004f0: 0000 0072 1200 0000 720b 0000 001c 0000  ...r....r.......
-00000500: 0072 1300 0000 7a15 4150 4955 726c 5772  .r....z.APIUrlWr
-00000510: 6974 6572 2e5f 5f69 6e69 745f 5f63 0100  iter.__init__c..
-00000520: 0000 0000 0000 0000 0000 0600 0000 0900  ................
-00000530: 0000 4300 0000 737c 0000 0064 017d 0164  ..C...s|...d.}.d
-00000540: 027d 027c 006a 00a0 01a1 0044 005d 2c7d  .}.|.j.....D.],}
-00000550: 0364 027d 047c 0464 037c 03a0 02a1 009b  .d.}.|.d.|......
-00000560: 0064 047c 039b 0064 057c 03a0 02a1 009b  .d.|...d.|......
-00000570: 0064 069d 0737 007d 047c 0464 037c 03a0  .d...7.}.|.d.|..
-00000580: 02a1 009b 0064 077c 039b 0064 087c 03a0  .....d.|...d.|..
-00000590: 02a1 009b 0064 099d 0737 007d 047c 027c  .....d...7.}.|.|
-000005a0: 0437 007d 0271 097c 017c 0217 0064 0a17  .7.}.q.|.|...d..
-000005b0: 007d 057c 0553 0029 0b4e 7214 0000 0072  .}.|.S.).Nr....r
-000005c0: 1500 0000 7216 0000 007a 0b73 2f27 2c20  ....r....z.s/', 
-000005d0: 7669 6577 732e 7a23 4c69 7374 4372 6561  views.z#ListCrea
-000005e0: 7465 4150 4956 6965 772e 6173 5f76 6965  teAPIView.as_vie
-000005f0: 7728 292c 206e 616d 653d 277a 105f 6c69  w(), name='z._li
-00000600: 7374 5f63 7265 6174 6527 292c 0a7a 1373  st_create'),.z.s
-00000610: 2f3c 696e 743a 706b 3e27 2c20 7669 6577  /<int:pk>', view
-00000620: 732e 7a2e 5265 7472 6965 7665 5570 6461  s.z.RetrieveUpda
-00000630: 7465 4465 7374 726f 7941 5049 5669 6577  teDestroyAPIView
-00000640: 2e61 735f 7669 6577 2829 2c20 6e61 6d65  .as_view(), name
-00000650: 3d27 7a1c 5f72 6574 7269 6576 655f 7570  ='z._retrieve_up
-00000660: 6461 7465 5f64 6573 7472 6f79 2729 2c0a  date_destroy'),.
-00000670: 7217 0000 0072 1800 0000 721b 0000 0072  r....r....r....r
-00000680: 1100 0000 7211 0000 0072 1200 0000 7221  ....r....r....r!
-00000690: 0000 0022 0000 0073 1200 0000 0401 0401  ..."...s........
-000006a0: 0e02 0401 2401 2401 0a01 0c02 0401 7a1c  ....$.$.......z.
-000006b0: 4150 4955 726c 5772 6974 6572 2e67 6574  APIUrlWriter.get
-000006c0: 5f66 756c 6c5f 7374 7269 6e67 7222 0000  _full_stringr"..
-000006d0: 0072 1100 0000 7211 0000 0072 0f00 0000  .r....r....r....
-000006e0: 7212 0000 0072 2800 0000 1b00 0000 7227  r....r(.......r'
-000006f0: 0000 0072 2800 0000 4e29 04da 1c63 6f64  ...r(...N)...cod
-00000700: 656c 6573 735f 646a 616e 676f 2e77 7269  eless_django.wri
-00000710: 7465 7273 2e62 6173 6572 0200 0000 7204  ters.baser....r.
-00000720: 0000 0072 2800 0000 7211 0000 0072 1100  ...r(...r....r..
-00000730: 0000 7211 0000 0072 1200 0000 da08 3c6d  ..r....r......<m
-00000740: 6f64 756c 653e 0100 0000 7306 0000 000c  odule>....s.....
-00000750: 0010 0414 16                             .....
+00000160: 5f5f a900 fa5a 2f68 6f6d 652f 6f6d 6172  __...Z/home/omar
+00000170: 2f63 6f64 652f 7465 7374 2d63 6c64 2f76  /code/test-cld/v
+00000180: 656e 762f 6c69 622f 7079 7468 6f6e 332e  env/lib/python3.
+00000190: 3130 2f73 6974 652d 7061 636b 6167 6573  10/site-packages
+000001a0: 2f63 6f64 656c 6573 735f 646a 616e 676f  /codeless_django
+000001b0: 2f77 7269 7465 7273 2f75 726c 732e 7079  /writers/urls.py
+000001c0: 720b 0000 0006 0000 00f3 0800 0000 0601  r...............
+000001d0: 0601 0a01 1001 7a12 5552 4c57 7269 7465  ......z.URLWrite
+000001e0: 722e 5f5f 696e 6974 5f5f 6301 0000 0000  r.__init__c.....
+000001f0: 0000 0000 0000 0006 0000 0009 0000 0043  ...............C
+00000200: 0000 0073 a000 0000 6401 7d01 6402 7d02  ...s....d.}.d.}.
+00000210: 7c00 6a00 a001 a100 4400 5d3e 7d03 6402  |.j.....D.]>}.d.
+00000220: 7d04 7c04 6403 7c03 a002 a100 9b00 6404  }.|.d.|.......d.
+00000230: 7c03 9b00 6405 7c03 a002 a100 9b00 6406  |...d.|.......d.
+00000240: 9d07 3700 7d04 7c04 6403 7c03 a002 a100  ..7.}.|.d.|.....
+00000250: 9b00 6407 7c03 9b00 6408 7c03 a002 a100  ..d.|...d.|.....
+00000260: 9b00 6409 9d07 3700 7d04 7c04 6403 7c03  ..d...7.}.|.d.|.
+00000270: a002 a100 9b00 640a 7c03 9b00 640b 7c03  ......d.|...d.|.
+00000280: a002 a100 9b00 640c 9d07 3700 7d04 7c02  ......d...7.}.|.
+00000290: 7c04 3700 7d02 7109 7c01 7c02 1700 640d  |.7.}.q.|.|...d.
+000002a0: 1700 7d05 7c05 5300 290e 4efa 1275 726c  ..}.|.S.).N..url
+000002b0: 7061 7474 6572 6e73 202b 3d20 5b20 0ada  patterns += [ ..
+000002c0: 00fa 0a20 2020 2070 6174 6828 277a 0f2f  ...    path('z./
+000002d0: 6c69 7374 2f27 2c20 7669 6577 732e 7a1a  list/', views.z.
+000002e0: 4c69 7374 5669 6577 2e61 735f 7669 6577  ListView.as_view
+000002f0: 2829 2c20 6e61 6d65 3d27 7a09 5f6c 6973  (), name='z._lis
+00000300: 7427 292c 0a7a 112f 6372 6561 7465 2f27  t'),.z./create/'
+00000310: 2c20 7669 6577 732e 7a1c 4372 6561 7465  , views.z.Create
+00000320: 5669 6577 2e61 735f 7669 6577 2829 2c20  View.as_view(), 
+00000330: 6e61 6d65 3d27 7a0b 5f63 7265 6174 6527  name='z._create'
+00000340: 292c 0a7a 132f 3c69 6e74 3a70 6b3e 2f27  ),.z./<int:pk>/'
+00000350: 2c20 7669 6577 732e 7a1c 4465 7461 696c  , views.z.Detail
+00000360: 5669 6577 2e61 735f 7669 6577 2829 2c20  View.as_view(), 
+00000370: 6e61 6d65 3d27 7a0b 5f64 6574 6169 6c27  name='z._detail'
+00000380: 292c 0afa 060a 205d 200a 0aa9 0372 0800  ),.... ] ....r..
+00000390: 0000 da04 6b65 7973 da05 6c6f 7765 72a9  ....keys..lower.
+000003a0: 0672 0d00 0000 da0e 696e 6974 6961 6c5f  .r......initial_
+000003b0: 7374 7269 6e67 da10 7572 6c5f 7061 7468  string..url_path
+000003c0: 5f73 7472 696e 6773 da0a 6d6f 6465 6c5f  _strings..model_
+000003d0: 6e61 6d65 da0a 7572 6c5f 7374 7269 6e67  name..url_string
+000003e0: da0b 6675 6c6c 5f73 7472 696e 6772 1100  ..full_stringr..
+000003f0: 0000 7211 0000 0072 1200 0000 da0f 6765  ..r....r......ge
+00000400: 745f 6675 6c6c 5f73 7472 696e 670c 0000  t_full_string...
+00000410: 0073 1400 0000 0401 0401 0e02 0401 2401  .s............$.
+00000420: 2401 2401 0a01 0c02 0401 7a19 5552 4c57  $.$.......z.URLW
+00000430: 7269 7465 722e 6765 745f 6675 6c6c 5f73  riter.get_full_s
+00000440: 7472 696e 67a9 06da 085f 5f6e 616d 655f  tring....__name_
+00000450: 5fda 0a5f 5f6d 6f64 756c 655f 5fda 0c5f  _..__module__.._
+00000460: 5f71 7561 6c6e 616d 655f 5f72 0b00 0000  _qualname__r....
+00000470: 7221 0000 00da 0d5f 5f63 6c61 7373 6365  r!.....__classce
+00000480: 6c6c 5f5f 7211 0000 0072 1100 0000 720f  ll__r....r....r.
+00000490: 0000 0072 1200 0000 7204 0000 0005 0000  ...r....r.......
+000004a0: 00f3 0600 0000 0800 0c01 1006 7204 0000  ............r...
+000004b0: 0063 0000 0000 0000 0000 0000 0000 0000  .c..............
+000004c0: 0000 0300 0000 0000 0000 7203 0000 0029  ..........r....)
+000004d0: 05da 0c41 5049 5572 6c57 7269 7465 7263  ...APIUrlWriterc
+000004e0: 0300 0000 0000 0000 0000 0000 0400 0000  ................
+000004f0: 0300 0000 0300 0000 7205 0000 0072 0600  ........r....r..
+00000500: 0000 7207 0000 0072 0c00 0000 720f 0000  ..r....r....r...
+00000510: 0072 1100 0000 7212 0000 0072 0b00 0000  .r....r....r....
+00000520: 1c00 0000 7213 0000 007a 1541 5049 5572  ....r....z.APIUr
+00000530: 6c57 7269 7465 722e 5f5f 696e 6974 5f5f  lWriter.__init__
+00000540: 6301 0000 0000 0000 0000 0000 0006 0000  c...............
+00000550: 0009 0000 0043 0000 0073 7c00 0000 6401  .....C...s|...d.
+00000560: 7d01 6402 7d02 7c00 6a00 a001 a100 4400  }.d.}.|.j.....D.
+00000570: 5d2c 7d03 6402 7d04 7c04 6403 7c03 a002  ],}.d.}.|.d.|...
+00000580: a100 9b00 6404 7c03 9b00 6405 7c03 a002  ....d.|...d.|...
+00000590: a100 9b00 6406 9d07 3700 7d04 7c04 6403  ....d...7.}.|.d.
+000005a0: 7c03 a002 a100 9b00 6407 7c03 9b00 6408  |.......d.|...d.
+000005b0: 7c03 a002 a100 9b00 6409 9d07 3700 7d04  |.......d...7.}.
+000005c0: 7c02 7c04 3700 7d02 7109 7c01 7c02 1700  |.|.7.}.q.|.|...
+000005d0: 640a 1700 7d05 7c05 5300 290b 4e72 1400  d...}.|.S.).Nr..
+000005e0: 0000 7215 0000 0072 1600 0000 7a0b 732f  ..r....r....z.s/
+000005f0: 272c 2076 6965 7773 2e7a 234c 6973 7443  ', views.z#ListC
+00000600: 7265 6174 6541 5049 5669 6577 2e61 735f  reateAPIView.as_
+00000610: 7669 6577 2829 2c20 6e61 6d65 3d27 7a10  view(), name='z.
+00000620: 5f6c 6973 745f 6372 6561 7465 2729 2c0a  _list_create'),.
+00000630: 7a13 732f 3c69 6e74 3a70 6b3e 272c 2076  z.s/<int:pk>', v
+00000640: 6965 7773 2e7a 2e52 6574 7269 6576 6555  iews.z.RetrieveU
+00000650: 7064 6174 6544 6573 7472 6f79 4150 4956  pdateDestroyAPIV
+00000660: 6965 772e 6173 5f76 6965 7728 292c 206e  iew.as_view(), n
+00000670: 616d 653d 277a 1c5f 7265 7472 6965 7665  ame='z._retrieve
+00000680: 5f75 7064 6174 655f 6465 7374 726f 7927  _update_destroy'
+00000690: 292c 0a72 1700 0000 7218 0000 0072 1b00  ),.r....r....r..
+000006a0: 0000 7211 0000 0072 1100 0000 7212 0000  ..r....r....r...
+000006b0: 0072 2100 0000 2200 0000 7312 0000 0004  .r!..."...s.....
+000006c0: 0104 010e 0204 0124 0124 010a 010c 0204  .......$.$......
+000006d0: 017a 1c41 5049 5572 6c57 7269 7465 722e  .z.APIUrlWriter.
+000006e0: 6765 745f 6675 6c6c 5f73 7472 696e 6772  get_full_stringr
+000006f0: 2200 0000 7211 0000 0072 1100 0000 720f  "...r....r....r.
+00000700: 0000 0072 1200 0000 7228 0000 001b 0000  ...r....r(......
+00000710: 0072 2700 0000 7228 0000 004e 2904 da1c  .r'...r(...N)...
+00000720: 636f 6465 6c65 7373 5f64 6a61 6e67 6f2e  codeless_django.
+00000730: 7772 6974 6572 732e 6261 7365 7202 0000  writers.baser...
+00000740: 0072 0400 0000 7228 0000 0072 1100 0000  .r....r(...r....
+00000750: 7211 0000 0072 1100 0000 7212 0000 00da  r....r....r.....
+00000760: 083c 6d6f 6475 6c65 3e01 0000 0073 0600  .<module>....s..
+00000770: 0000 0c00 1004 1416                      ........
```

### Comparing `codeless-django-0.0.14/codeless_django/writers/__pycache__/views.cpython-310.pyc` & `codeless-django-0.0.15/codeless_django/writers/__pycache__/views.cpython-310.pyc`

 * *Format-specific differences are supported for Python .pyc files but no file-specific differences were detected; falling back to a binary diff. file(1) reports: Byte-compiled Python module for CPython 3.10, timestamp-based, .py timestamp: Thu Jun  1 00:43:12 2023 UTC, .py size: 2055 bytes*

 * *Could not decompile bytecode: bad marshal data (unknown type code)*

 * *Files 13% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-00000000: 6f0d 0d0a 0000 0000 a0e9 7764 0708 0000  o.........wd....
+00000000: 6f0d 0d0a 0000 0000 6f28 bd64 0708 0000  o.......o(.d....
 00000010: e300 0000 0000 0000 0000 0000 0000 0000  ................
 00000020: 0004 0000 0040 0000 0073 7c00 0000 6400  .....@...s|...d.
 00000030: 6401 6c00 6d01 5a01 6d02 5a02 6d03 5a03  d.l.m.Z.m.Z.m.Z.
 00000040: 6d04 5a04 0100 4700 6402 6403 8400 6403  m.Z...G.d.d...d.
 00000050: 6504 8303 5a05 4700 6404 6405 8400 6405  e...Z.G.d.d...d.
 00000060: 6505 8303 5a06 4700 6406 6407 8400 6407  e...Z.G.d.d...d.
 00000070: 6505 8303 5a07 4700 6408 6409 8400 6409  e...Z.G.d.d...d.
@@ -19,174 +19,176 @@
 00000120: 0f42 6173 6556 6965 7742 7569 6c64 6572  .BaseViewBuilder
 00000130: 6303 0000 0000 0000 0000 0000 0003 0000  c...............
 00000140: 0002 0000 0043 0000 0073 1000 0000 7c02  .....C...s....|.
 00000150: 7c00 5f00 7c01 7c00 5f01 6400 5300 2901  |._.|.|._.d.S.).
 00000160: 4e29 02da 0a6d 6f64 656c 5f6e 616d 65da  N)...model_name.
 00000170: 0861 7070 5f6e 616d 6529 03da 0473 656c  .app_name)...sel
 00000180: 6672 0800 0000 7207 0000 00a9 0072 0a00  fr....r......r..
-00000190: 0000 fa38 2f68 6f6d 652f 6f6d 6172 2f63  ...8/home/omar/c
-000001a0: 6f64 652f 5175 6963 6b44 6a2f 636f 6465  ode/QuickDj/code
-000001b0: 6c65 7373 5f64 6a61 6e67 6f2f 7772 6974  less_django/writ
-000001c0: 6572 732f 7669 6577 732e 7079 da08 5f5f  ers/views.py..__
-000001d0: 696e 6974 5f5f 0500 0000 7304 0000 0006  init__....s.....
-000001e0: 010a 017a 1842 6173 6556 6965 7742 7569  ...z.BaseViewBui
-000001f0: 6c64 6572 2e5f 5f69 6e69 745f 5f4e 2904  lder.__init__N).
-00000200: da08 5f5f 6e61 6d65 5f5f da0a 5f5f 6d6f  ..__name__..__mo
-00000210: 6475 6c65 5f5f da0c 5f5f 7175 616c 6e61  dule__..__qualna
-00000220: 6d65 5f5f 720c 0000 0072 0a00 0000 720a  me__r....r....r.
-00000230: 0000 0072 0a00 0000 720b 0000 0072 0600  ...r....r....r..
-00000240: 0000 0400 0000 7304 0000 0008 000c 0172  ......s........r
-00000250: 0600 0000 6300 0000 0000 0000 0000 0000  ....c...........
-00000260: 0000 0000 0002 0000 0040 0000 00f3 1c00  .........@......
-00000270: 0000 6500 5a01 6400 5a02 6401 6402 8400  ..e.Z.d.Z.d.d...
-00000280: 5a03 6403 6404 8400 5a04 6405 5300 2906  Z.d.d...Z.d.S.).
-00000290: da11 4372 6561 7465 5669 6577 4275 696c  ..CreateViewBuil
-000002a0: 6465 7263 0100 0000 0000 0000 0000 0000  derc............
-000002b0: 0100 0000 0300 0000 4300 0000 f30e 0000  ........C.......
-000002c0: 0064 017c 006a 009b 0064 029d 0353 0029  .d.|.j...d...S.)
-000002d0: 034e fa06 636c 6173 7320 7a20 4372 6561  .N..class z Crea
-000002e0: 7465 5669 6577 2867 656e 6572 6963 2e43  teView(generic.C
-000002f0: 7265 6174 6556 6965 7729 3a0a a901 7207  reateView):...r.
-00000300: 0000 00a9 0172 0900 0000 720a 0000 0072  .....r....r....r
-00000310: 0a00 0000 720b 0000 00da 1167 6574 5f6f  ....r......get_o
-00000320: 626a 6563 745f 6865 6164 6572 0c00 0000  bject_header....
-00000330: f302 0000 000e 017a 2343 7265 6174 6556  .......z#CreateV
-00000340: 6965 7742 7569 6c64 6572 2e67 6574 5f6f  iewBuilder.get_o
-00000350: 626a 6563 745f 6865 6164 6572 6301 0000  bject_headerc...
-00000360: 0000 0000 0000 0000 0001 0000 0005 0000  ................
-00000370: 0043 0000 00f3 1600 0000 6401 7c00 6a00  .C........d.|.j.
-00000380: 9b00 6402 7c00 6a01 9b00 6403 9d05 5300  ..d.|.j...d...S.
-00000390: 2904 4e7a 0909 6d6f 6465 6c20 3d20 fa08  ).Nz..model = ..
-000003a0: 5f6d 6f64 656c 732e 7a29 0a09 6669 656c  _models.z)..fiel
-000003b0: 6473 203d 2027 5f5f 616c 6c5f 5f27 0a09  ds = '__all__'..
-000003c0: 7375 6363 6573 735f 7572 6c3d 2027 205c  success_url= ' \
-000003d0: 2027 20a9 0272 0800 0000 7207 0000 0072   ' ..r....r....r
-000003e0: 1500 0000 720a 0000 0072 0a00 0000 720b  ....r....r....r.
-000003f0: 0000 00da 0f67 6574 5f6f 626a 6563 745f  .....get_object_
-00000400: 626f 6479 0f00 0000 f302 0000 0016 017a  body...........z
-00000410: 2143 7265 6174 6556 6965 7742 7569 6c64  !CreateViewBuild
-00000420: 6572 2e67 6574 5f6f 626a 6563 745f 626f  er.get_object_bo
-00000430: 6479 4ea9 0572 0d00 0000 720e 0000 0072  dyN..r....r....r
-00000440: 0f00 0000 7216 0000 0072 1b00 0000 720a  ....r....r....r.
-00000450: 0000 0072 0a00 0000 720a 0000 0072 0b00  ...r....r....r..
-00000460: 0000 7211 0000 000a 0000 00f3 0600 0000  ..r.............
-00000470: 0800 0802 0c03 7211 0000 0063 0000 0000  ......r....c....
-00000480: 0000 0000 0000 0000 0000 0000 0200 0000  ................
-00000490: 4000 0000 7210 0000 0029 06da 0f4c 6973  @...r....)...Lis
-000004a0: 7456 6965 7742 7569 6c64 6572 6301 0000  tViewBuilderc...
-000004b0: 0000 0000 0000 0000 0001 0000 0003 0000  ................
-000004c0: 0043 0000 0072 1200 0000 2903 4e72 1300  .C...r....).Nr..
-000004d0: 0000 7a1c 4c69 7374 5669 6577 2867 656e  ..z.ListView(gen
-000004e0: 6572 6963 2e4c 6973 7456 6965 7729 3a0a  eric.ListView):.
-000004f0: 7214 0000 0072 1500 0000 720a 0000 0072  r....r....r....r
-00000500: 0a00 0000 720b 0000 0072 1600 0000 1500  ....r....r......
-00000510: 0000 7217 0000 007a 214c 6973 7456 6965  ..r....z!ListVie
-00000520: 7742 7569 6c64 6572 2e67 6574 5f6f 626a  wBuilder.get_obj
-00000530: 6563 745f 6865 6164 6572 6301 0000 0000  ect_headerc.....
-00000540: 0000 0000 0000 0001 0000 0005 0000 0043  ...............C
-00000550: 0000 0072 1800 0000 2904 4efa 0a09 6d6f  ...r....).N...mo
-00000560: 6465 6c20 3d20 2072 1900 0000 7a14 0a09  del =  r....z...
-00000570: 7061 6769 6e61 7465 5f62 7920 3d20 3130  paginate_by = 10
-00000580: 200a 721a 0000 0072 1500 0000 720a 0000   .r....r....r...
-00000590: 0072 0a00 0000 720b 0000 0072 1b00 0000  .r....r....r....
-000005a0: 1800 0000 721c 0000 007a 1f4c 6973 7456  ....r....z.ListV
-000005b0: 6965 7742 7569 6c64 6572 2e67 6574 5f6f  iewBuilder.get_o
-000005c0: 626a 6563 745f 626f 6479 4e72 1d00 0000  bject_bodyNr....
-000005d0: 720a 0000 0072 0a00 0000 720a 0000 0072  r....r....r....r
-000005e0: 0b00 0000 721f 0000 0013 0000 0072 1e00  ....r........r..
-000005f0: 0000 721f 0000 0063 0000 0000 0000 0000  ..r....c........
-00000600: 0000 0000 0000 0000 0200 0000 4000 0000  ............@...
-00000610: 7210 0000 0029 06da 1144 6574 6169 6c56  r....)...DetailV
-00000620: 6965 7742 7569 6c64 6572 6301 0000 0000  iewBuilderc.....
-00000630: 0000 0000 0000 0001 0000 0003 0000 0043  ...............C
-00000640: 0000 0072 1200 0000 2903 4e72 1300 0000  ...r....).Nr....
-00000650: 7a20 4465 7461 696c 5669 6577 2867 656e  z DetailView(gen
-00000660: 6572 6963 2e44 6574 6169 6c56 6965 7729  eric.DetailView)
-00000670: 3a0a 7214 0000 0072 1500 0000 720a 0000  :.r....r....r...
-00000680: 0072 0a00 0000 720b 0000 0072 1600 0000  .r....r....r....
-00000690: 1e00 0000 7217 0000 007a 2344 6574 6169  ....r....z#Detai
-000006a0: 6c56 6965 7742 7569 6c64 6572 2e67 6574  lViewBuilder.get
-000006b0: 5f6f 626a 6563 745f 6865 6164 6572 6301  _object_headerc.
-000006c0: 0000 0000 0000 0000 0000 0001 0000 0005  ................
-000006d0: 0000 0043 0000 0072 1800 0000 a904 4e72  ...C...r......Nr
-000006e0: 2000 0000 7219 0000 007a 0220 0a72 1a00   ...r....z. .r..
-000006f0: 0000 7215 0000 0072 0a00 0000 720a 0000  ..r....r....r...
-00000700: 0072 0b00 0000 721b 0000 0021 0000 0072  .r....r....!...r
-00000710: 1c00 0000 7a21 4465 7461 696c 5669 6577  ....z!DetailView
-00000720: 4275 696c 6465 722e 6765 745f 6f62 6a65  Builder.get_obje
-00000730: 6374 5f62 6f64 794e 721d 0000 0072 0a00  ct_bodyNr....r..
-00000740: 0000 720a 0000 0072 0a00 0000 720b 0000  ..r....r....r...
-00000750: 0072 2100 0000 1c00 0000 721e 0000 0072  .r!.......r....r
-00000760: 2100 0000 6300 0000 0000 0000 0000 0000  !...c...........
-00000770: 0000 0000 0002 0000 0040 0000 0072 1000  .........@...r..
-00000780: 0000 2906 da11 5570 6461 7465 5669 6577  ..)...UpdateView
-00000790: 4275 696c 6465 7263 0100 0000 0000 0000  Builderc........
-000007a0: 0000 0000 0100 0000 0300 0000 4300 0000  ............C...
-000007b0: 7212 0000 0029 034e 7213 0000 007a 2055  r....).Nr....z U
-000007c0: 7064 6174 6556 6965 7728 6765 6e65 7269  pdateView(generi
-000007d0: 632e 5570 6461 7465 5669 6577 293a 0a72  c.UpdateView):.r
-000007e0: 1400 0000 7215 0000 0072 0a00 0000 720a  ....r....r....r.
-000007f0: 0000 0072 0b00 0000 7216 0000 0027 0000  ...r....r....'..
-00000800: 0072 1700 0000 7a23 5570 6461 7465 5669  .r....z#UpdateVi
-00000810: 6577 4275 696c 6465 722e 6765 745f 6f62  ewBuilder.get_ob
-00000820: 6a65 6374 5f68 6561 6465 7263 0100 0000  ject_headerc....
-00000830: 0000 0000 0000 0000 0100 0000 0500 0000  ................
-00000840: 4300 0000 7218 0000 0072 2200 0000 721a  C...r....r"...r.
-00000850: 0000 0072 1500 0000 720a 0000 0072 0a00  ...r....r....r..
-00000860: 0000 720b 0000 0072 1b00 0000 2a00 0000  ..r....r....*...
-00000870: 721c 0000 007a 2155 7064 6174 6556 6965  r....z!UpdateVie
-00000880: 7742 7569 6c64 6572 2e67 6574 5f6f 626a  wBuilder.get_obj
-00000890: 6563 745f 626f 6479 4e72 1d00 0000 720a  ect_bodyNr....r.
-000008a0: 0000 0072 0a00 0000 720a 0000 0072 0b00  ...r....r....r..
-000008b0: 0000 7223 0000 0025 0000 0072 1e00 0000  ..r#...%...r....
-000008c0: 7223 0000 0063 0000 0000 0000 0000 0000  r#...c..........
-000008d0: 0000 0000 0000 0300 0000 0000 0000 7324  ..............s$
-000008e0: 0000 0065 005a 0164 005a 0287 0066 0164  ...e.Z.d.Z...f.d
-000008f0: 0164 0284 085a 0364 0364 0484 005a 0487  .d...Z.d.d...Z..
-00000900: 0004 005a 0553 0029 05da 0a56 6965 7757  ...Z.S.)...ViewW
-00000910: 7269 7465 7263 0300 0000 0000 0000 0000  riterc..........
-00000920: 0000 0400 0000 0300 0000 0300 0000 7326  ..............s&
-00000930: 0000 007c 027c 005f 007c 017c 005f 017c  ...|.|._.|.|._.|
-00000940: 019b 0064 019d 027d 0374 0283 00a0 037c  ...d...}.t.....|
-00000950: 03a1 0101 0064 0053 0029 024e 7a09 2f76  .....d.S.).Nz./v
-00000960: 6965 7773 2e70 7929 04da 066d 6f64 656c  iews.py)...model
-00000970: 7372 0800 0000 da05 7375 7065 7272 0c00  sr......superr..
-00000980: 0000 2904 7209 0000 0072 0800 0000 7225  ..).r....r....r%
-00000990: 0000 00da 0966 696c 655f 6e61 6d65 a901  .....file_name..
-000009a0: da09 5f5f 636c 6173 735f 5f72 0a00 0000  ..__class__r....
-000009b0: 720b 0000 0072 0c00 0000 2f00 0000 7308  r....r..../...s.
-000009c0: 0000 0006 0106 010a 0110 017a 1356 6965  ...........z.Vie
-000009d0: 7757 7269 7465 722e 5f5f 696e 6974 5f5f  wWriter.__init__
-000009e0: 6301 0000 0000 0000 0000 0000 0004 0000  c...............
-000009f0: 0005 0000 0043 0000 0073 6600 0000 7c00  .....C...sf...|.
-00000a00: 6a00 7d01 6401 7d02 7c00 6a01 a002 a100  j.}.d.}.|.j.....
-00000a10: 4400 5d26 7d03 7c02 7403 7c01 7c03 8302  D.]&}.|.t.|.|...
-00000a20: a004 a100 3700 7d02 7c02 7405 7c01 7c03  ....7.}.|.t.|.|.
-00000a30: 8302 a004 a100 3700 7d02 7c02 7406 7c01  ......7.}.|.t.|.
-00000a40: 7c03 8302 a004 a100 3700 7d02 7c02 7407  |.......7.}.|.t.
-00000a50: 7c01 7c03 8302 a004 a100 3700 7d02 710a  |.|.......7.}.q.
-00000a60: 7c02 5300 2902 4eda 0029 0872 0800 0000  |.S.).N..).r....
-00000a70: 7225 0000 00da 046b 6579 7372 1f00 0000  r%.....keysr....
-00000a80: da11 6765 745f 6f62 6a65 6374 5f73 7472  ..get_object_str
-00000a90: 696e 6772 2100 0000 7223 0000 0072 1100  ingr!...r#...r..
-00000aa0: 0000 2904 7209 0000 0072 0800 0000 da0b  ..).r....r......
-00000ab0: 6675 6c6c 5f73 7472 696e 6772 0700 0000  full_stringr....
-00000ac0: 720a 0000 0072 0a00 0000 720b 0000 00da  r....r....r.....
-00000ad0: 0f67 6574 5f66 756c 6c5f 7374 7269 6e67  .get_full_string
-00000ae0: 3500 0000 7310 0000 0006 0104 010e 0112  5...s...........
-00000af0: 0112 0112 0114 0104 027a 1a56 6965 7757  .........z.ViewW
-00000b00: 7269 7465 722e 6765 745f 6675 6c6c 5f73  riter.get_full_s
-00000b10: 7472 696e 6729 0672 0d00 0000 720e 0000  tring).r....r...
-00000b20: 0072 0f00 0000 720c 0000 0072 2e00 0000  .r....r....r....
-00000b30: da0d 5f5f 636c 6173 7363 656c 6c5f 5f72  ..__classcell__r
-00000b40: 0a00 0000 720a 0000 0072 2800 0000 720b  ....r....r(...r.
-00000b50: 0000 0072 2400 0000 2e00 0000 7306 0000  ...r$.......s...
-00000b60: 0008 000c 0110 0672 2400 0000 4e29 0bda  .......r$...N)..
-00000b70: 1c63 6f64 656c 6573 735f 646a 616e 676f  .codeless_django
-00000b80: 2e77 7269 7465 7273 2e62 6173 6572 0200  .writers.baser..
-00000b90: 0000 7203 0000 0072 0400 0000 7205 0000  ..r....r....r...
-00000ba0: 0072 0600 0000 7211 0000 0072 1f00 0000  .r....r....r....
-00000bb0: 7221 0000 0072 2300 0000 7224 0000 0072  r!...r#...r$...r
-00000bc0: 0a00 0000 720a 0000 0072 0a00 0000 720b  ....r....r....r.
-00000bd0: 0000 00da 083c 6d6f 6475 6c65 3e01 0000  .....<module>...
-00000be0: 0073 0e00 0000 1800 1003 1006 1009 1009  .s..............
-00000bf0: 1009 1409                                ....
+00000190: 0000 fa5b 2f68 6f6d 652f 6f6d 6172 2f63  ...[/home/omar/c
+000001a0: 6f64 652f 7465 7374 2d63 6c64 2f76 656e  ode/test-cld/ven
+000001b0: 762f 6c69 622f 7079 7468 6f6e 332e 3130  v/lib/python3.10
+000001c0: 2f73 6974 652d 7061 636b 6167 6573 2f63  /site-packages/c
+000001d0: 6f64 656c 6573 735f 646a 616e 676f 2f77  odeless_django/w
+000001e0: 7269 7465 7273 2f76 6965 7773 2e70 79da  riters/views.py.
+000001f0: 085f 5f69 6e69 745f 5f05 0000 0073 0400  .__init__....s..
+00000200: 0000 0601 0a01 7a18 4261 7365 5669 6577  ......z.BaseView
+00000210: 4275 696c 6465 722e 5f5f 696e 6974 5f5f  Builder.__init__
+00000220: 4e29 04da 085f 5f6e 616d 655f 5fda 0a5f  N)...__name__.._
+00000230: 5f6d 6f64 756c 655f 5fda 0c5f 5f71 7561  _module__..__qua
+00000240: 6c6e 616d 655f 5f72 0c00 0000 720a 0000  lname__r....r...
+00000250: 0072 0a00 0000 720a 0000 0072 0b00 0000  .r....r....r....
+00000260: 7206 0000 0004 0000 0073 0400 0000 0800  r........s......
+00000270: 0c01 7206 0000 0063 0000 0000 0000 0000  ..r....c........
+00000280: 0000 0000 0000 0000 0200 0000 4000 0000  ............@...
+00000290: f31c 0000 0065 005a 0164 005a 0264 0164  .....e.Z.d.Z.d.d
+000002a0: 0284 005a 0364 0364 0484 005a 0464 0553  ...Z.d.d...Z.d.S
+000002b0: 0029 06da 1143 7265 6174 6556 6965 7742  .)...CreateViewB
+000002c0: 7569 6c64 6572 6301 0000 0000 0000 0000  uilderc.........
+000002d0: 0000 0001 0000 0003 0000 0043 0000 00f3  ...........C....
+000002e0: 0e00 0000 6401 7c00 6a00 9b00 6402 9d03  ....d.|.j...d...
+000002f0: 5300 2903 4efa 0663 6c61 7373 207a 2043  S.).N..class z C
+00000300: 7265 6174 6556 6965 7728 6765 6e65 7269  reateView(generi
+00000310: 632e 4372 6561 7465 5669 6577 293a 0aa9  c.CreateView):..
+00000320: 0172 0700 0000 a901 7209 0000 0072 0a00  .r......r....r..
+00000330: 0000 720a 0000 0072 0b00 0000 da11 6765  ..r....r......ge
+00000340: 745f 6f62 6a65 6374 5f68 6561 6465 720c  t_object_header.
+00000350: 0000 00f3 0200 0000 0e01 7a23 4372 6561  ..........z#Crea
+00000360: 7465 5669 6577 4275 696c 6465 722e 6765  teViewBuilder.ge
+00000370: 745f 6f62 6a65 6374 5f68 6561 6465 7263  t_object_headerc
+00000380: 0100 0000 0000 0000 0000 0000 0100 0000  ................
+00000390: 0500 0000 4300 0000 f316 0000 0064 017c  ....C........d.|
+000003a0: 006a 009b 0064 027c 006a 019b 0064 039d  .j...d.|.j...d..
+000003b0: 0553 0029 044e 7a09 096d 6f64 656c 203d  .S.).Nz..model =
+000003c0: 20fa 085f 6d6f 6465 6c73 2e7a 290a 0966   .._models.z)..f
+000003d0: 6965 6c64 7320 3d20 275f 5f61 6c6c 5f5f  ields = '__all__
+000003e0: 270a 0973 7563 6365 7373 5f75 726c 3d20  '..success_url= 
+000003f0: 2720 5c20 2720 a902 7208 0000 0072 0700  ' \ ' ..r....r..
+00000400: 0000 7215 0000 0072 0a00 0000 720a 0000  ..r....r....r...
+00000410: 0072 0b00 0000 da0f 6765 745f 6f62 6a65  .r......get_obje
+00000420: 6374 5f62 6f64 790f 0000 00f3 0200 0000  ct_body.........
+00000430: 1601 7a21 4372 6561 7465 5669 6577 4275  ..z!CreateViewBu
+00000440: 696c 6465 722e 6765 745f 6f62 6a65 6374  ilder.get_object
+00000450: 5f62 6f64 794e a905 720d 0000 0072 0e00  _bodyN..r....r..
+00000460: 0000 720f 0000 0072 1600 0000 721b 0000  ..r....r....r...
+00000470: 0072 0a00 0000 720a 0000 0072 0a00 0000  .r....r....r....
+00000480: 720b 0000 0072 1100 0000 0a00 0000 f306  r....r..........
+00000490: 0000 0008 0008 020c 0372 1100 0000 6300  .........r....c.
+000004a0: 0000 0000 0000 0000 0000 0000 0000 0002  ................
+000004b0: 0000 0040 0000 0072 1000 0000 2906 da0f  ...@...r....)...
+000004c0: 4c69 7374 5669 6577 4275 696c 6465 7263  ListViewBuilderc
+000004d0: 0100 0000 0000 0000 0000 0000 0100 0000  ................
+000004e0: 0300 0000 4300 0000 7212 0000 0029 034e  ....C...r....).N
+000004f0: 7213 0000 007a 1c4c 6973 7456 6965 7728  r....z.ListView(
+00000500: 6765 6e65 7269 632e 4c69 7374 5669 6577  generic.ListView
+00000510: 293a 0a72 1400 0000 7215 0000 0072 0a00  ):.r....r....r..
+00000520: 0000 720a 0000 0072 0b00 0000 7216 0000  ..r....r....r...
+00000530: 0015 0000 0072 1700 0000 7a21 4c69 7374  .....r....z!List
+00000540: 5669 6577 4275 696c 6465 722e 6765 745f  ViewBuilder.get_
+00000550: 6f62 6a65 6374 5f68 6561 6465 7263 0100  object_headerc..
+00000560: 0000 0000 0000 0000 0000 0100 0000 0500  ................
+00000570: 0000 4300 0000 7218 0000 0029 044e fa0a  ..C...r....).N..
+00000580: 096d 6f64 656c 203d 2020 7219 0000 007a  .model =  r....z
+00000590: 140a 0970 6167 696e 6174 655f 6279 203d  ...paginate_by =
+000005a0: 2031 3020 0a72 1a00 0000 7215 0000 0072   10 .r....r....r
+000005b0: 0a00 0000 720a 0000 0072 0b00 0000 721b  ....r....r....r.
+000005c0: 0000 0018 0000 0072 1c00 0000 7a1f 4c69  .......r....z.Li
+000005d0: 7374 5669 6577 4275 696c 6465 722e 6765  stViewBuilder.ge
+000005e0: 745f 6f62 6a65 6374 5f62 6f64 794e 721d  t_object_bodyNr.
+000005f0: 0000 0072 0a00 0000 720a 0000 0072 0a00  ...r....r....r..
+00000600: 0000 720b 0000 0072 1f00 0000 1300 0000  ..r....r........
+00000610: 721e 0000 0072 1f00 0000 6300 0000 0000  r....r....c.....
+00000620: 0000 0000 0000 0000 0000 0002 0000 0040  ...............@
+00000630: 0000 0072 1000 0000 2906 da11 4465 7461  ...r....)...Deta
+00000640: 696c 5669 6577 4275 696c 6465 7263 0100  ilViewBuilderc..
+00000650: 0000 0000 0000 0000 0000 0100 0000 0300  ................
+00000660: 0000 4300 0000 7212 0000 0029 034e 7213  ..C...r....).Nr.
+00000670: 0000 007a 2044 6574 6169 6c56 6965 7728  ...z DetailView(
+00000680: 6765 6e65 7269 632e 4465 7461 696c 5669  generic.DetailVi
+00000690: 6577 293a 0a72 1400 0000 7215 0000 0072  ew):.r....r....r
+000006a0: 0a00 0000 720a 0000 0072 0b00 0000 7216  ....r....r....r.
+000006b0: 0000 001e 0000 0072 1700 0000 7a23 4465  .......r....z#De
+000006c0: 7461 696c 5669 6577 4275 696c 6465 722e  tailViewBuilder.
+000006d0: 6765 745f 6f62 6a65 6374 5f68 6561 6465  get_object_heade
+000006e0: 7263 0100 0000 0000 0000 0000 0000 0100  rc..............
+000006f0: 0000 0500 0000 4300 0000 7218 0000 00a9  ......C...r.....
+00000700: 044e 7220 0000 0072 1900 0000 7a02 200a  .Nr ...r....z. .
+00000710: 721a 0000 0072 1500 0000 720a 0000 0072  r....r....r....r
+00000720: 0a00 0000 720b 0000 0072 1b00 0000 2100  ....r....r....!.
+00000730: 0000 721c 0000 007a 2144 6574 6169 6c56  ..r....z!DetailV
+00000740: 6965 7742 7569 6c64 6572 2e67 6574 5f6f  iewBuilder.get_o
+00000750: 626a 6563 745f 626f 6479 4e72 1d00 0000  bject_bodyNr....
+00000760: 720a 0000 0072 0a00 0000 720a 0000 0072  r....r....r....r
+00000770: 0b00 0000 7221 0000 001c 0000 0072 1e00  ....r!.......r..
+00000780: 0000 7221 0000 0063 0000 0000 0000 0000  ..r!...c........
+00000790: 0000 0000 0000 0000 0200 0000 4000 0000  ............@...
+000007a0: 7210 0000 0029 06da 1155 7064 6174 6556  r....)...UpdateV
+000007b0: 6965 7742 7569 6c64 6572 6301 0000 0000  iewBuilderc.....
+000007c0: 0000 0000 0000 0001 0000 0003 0000 0043  ...............C
+000007d0: 0000 0072 1200 0000 2903 4e72 1300 0000  ...r....).Nr....
+000007e0: 7a20 5570 6461 7465 5669 6577 2867 656e  z UpdateView(gen
+000007f0: 6572 6963 2e55 7064 6174 6556 6965 7729  eric.UpdateView)
+00000800: 3a0a 7214 0000 0072 1500 0000 720a 0000  :.r....r....r...
+00000810: 0072 0a00 0000 720b 0000 0072 1600 0000  .r....r....r....
+00000820: 2700 0000 7217 0000 007a 2355 7064 6174  '...r....z#Updat
+00000830: 6556 6965 7742 7569 6c64 6572 2e67 6574  eViewBuilder.get
+00000840: 5f6f 626a 6563 745f 6865 6164 6572 6301  _object_headerc.
+00000850: 0000 0000 0000 0000 0000 0001 0000 0005  ................
+00000860: 0000 0043 0000 0072 1800 0000 7222 0000  ...C...r....r"..
+00000870: 0072 1a00 0000 7215 0000 0072 0a00 0000  .r....r....r....
+00000880: 720a 0000 0072 0b00 0000 721b 0000 002a  r....r....r....*
+00000890: 0000 0072 1c00 0000 7a21 5570 6461 7465  ...r....z!Update
+000008a0: 5669 6577 4275 696c 6465 722e 6765 745f  ViewBuilder.get_
+000008b0: 6f62 6a65 6374 5f62 6f64 794e 721d 0000  object_bodyNr...
+000008c0: 0072 0a00 0000 720a 0000 0072 0a00 0000  .r....r....r....
+000008d0: 720b 0000 0072 2300 0000 2500 0000 721e  r....r#...%...r.
+000008e0: 0000 0072 2300 0000 6300 0000 0000 0000  ...r#...c.......
+000008f0: 0000 0000 0000 0000 0003 0000 0000 0000  ................
+00000900: 0073 2400 0000 6500 5a01 6400 5a02 8700  .s$...e.Z.d.Z...
+00000910: 6601 6401 6402 8408 5a03 6403 6404 8400  f.d.d...Z.d.d...
+00000920: 5a04 8700 0400 5a05 5300 2905 da0a 5669  Z.....Z.S.)...Vi
+00000930: 6577 5772 6974 6572 6303 0000 0000 0000  ewWriterc.......
+00000940: 0000 0000 0004 0000 0003 0000 0003 0000  ................
+00000950: 0073 2600 0000 7c02 7c00 5f00 7c01 7c00  .s&...|.|._.|.|.
+00000960: 5f01 7c01 9b00 6401 9d02 7d03 7402 8300  _.|...d...}.t...
+00000970: a003 7c03 a101 0100 6400 5300 2902 4e7a  ..|.....d.S.).Nz
+00000980: 092f 7669 6577 732e 7079 2904 da06 6d6f  ./views.py)...mo
+00000990: 6465 6c73 7208 0000 00da 0573 7570 6572  delsr......super
+000009a0: 720c 0000 0029 0472 0900 0000 7208 0000  r....).r....r...
+000009b0: 0072 2500 0000 da09 6669 6c65 5f6e 616d  .r%.....file_nam
+000009c0: 65a9 01da 095f 5f63 6c61 7373 5f5f 720a  e....__class__r.
+000009d0: 0000 0072 0b00 0000 720c 0000 002f 0000  ...r....r..../..
+000009e0: 0073 0800 0000 0601 0601 0a01 1001 7a13  .s............z.
+000009f0: 5669 6577 5772 6974 6572 2e5f 5f69 6e69  ViewWriter.__ini
+00000a00: 745f 5f63 0100 0000 0000 0000 0000 0000  t__c............
+00000a10: 0400 0000 0500 0000 4300 0000 7366 0000  ........C...sf..
+00000a20: 007c 006a 007d 0164 017d 027c 006a 01a0  .|.j.}.d.}.|.j..
+00000a30: 02a1 0044 005d 267d 037c 0274 037c 017c  ...D.]&}.|.t.|.|
+00000a40: 0383 02a0 04a1 0037 007d 027c 0274 057c  .......7.}.|.t.|
+00000a50: 017c 0383 02a0 04a1 0037 007d 027c 0274  .|.......7.}.|.t
+00000a60: 067c 017c 0383 02a0 04a1 0037 007d 027c  .|.|.......7.}.|
+00000a70: 0274 077c 017c 0383 02a0 04a1 0037 007d  .t.|.|.......7.}
+00000a80: 0271 0a7c 0253 0029 024e da00 2908 7208  .q.|.S.).N..).r.
+00000a90: 0000 0072 2500 0000 da04 6b65 7973 721f  ...r%.....keysr.
+00000aa0: 0000 00da 1167 6574 5f6f 626a 6563 745f  .....get_object_
+00000ab0: 7374 7269 6e67 7221 0000 0072 2300 0000  stringr!...r#...
+00000ac0: 7211 0000 0029 0472 0900 0000 7208 0000  r....).r....r...
+00000ad0: 00da 0b66 756c 6c5f 7374 7269 6e67 7207  ...full_stringr.
+00000ae0: 0000 0072 0a00 0000 720a 0000 0072 0b00  ...r....r....r..
+00000af0: 0000 da0f 6765 745f 6675 6c6c 5f73 7472  ....get_full_str
+00000b00: 696e 6735 0000 0073 1000 0000 0601 0401  ing5...s........
+00000b10: 0e01 1201 1201 1201 1401 0402 7a1a 5669  ............z.Vi
+00000b20: 6577 5772 6974 6572 2e67 6574 5f66 756c  ewWriter.get_ful
+00000b30: 6c5f 7374 7269 6e67 2906 720d 0000 0072  l_string).r....r
+00000b40: 0e00 0000 720f 0000 0072 0c00 0000 722e  ....r....r....r.
+00000b50: 0000 00da 0d5f 5f63 6c61 7373 6365 6c6c  .....__classcell
+00000b60: 5f5f 720a 0000 0072 0a00 0000 7228 0000  __r....r....r(..
+00000b70: 0072 0b00 0000 7224 0000 002e 0000 0073  .r....r$.......s
+00000b80: 0600 0000 0800 0c01 1006 7224 0000 004e  ..........r$...N
+00000b90: 290b da1c 636f 6465 6c65 7373 5f64 6a61  )...codeless_dja
+00000ba0: 6e67 6f2e 7772 6974 6572 732e 6261 7365  ngo.writers.base
+00000bb0: 7202 0000 0072 0300 0000 7204 0000 0072  r....r....r....r
+00000bc0: 0500 0000 7206 0000 0072 1100 0000 721f  ....r....r....r.
+00000bd0: 0000 0072 2100 0000 7223 0000 0072 2400  ...r!...r#...r$.
+00000be0: 0000 720a 0000 0072 0a00 0000 720a 0000  ..r....r....r...
+00000bf0: 0072 0b00 0000 da08 3c6d 6f64 756c 653e  .r......<module>
+00000c00: 0100 0000 730e 0000 0018 0010 0310 0610  ....s...........
+00000c10: 0910 0910 0914 09                        .......
```

### Comparing `codeless-django-0.0.14/codeless_django/writers/apis.py` & `codeless-django-0.0.15/codeless_django/writers/apis.py`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.14/codeless_django/writers/apps.py` & `codeless-django-0.0.15/codeless_django/writers/apps.py`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.14/codeless_django/writers/base.py` & `codeless-django-0.0.15/codeless_django/writers/base.py`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.14/codeless_django/writers/files.py` & `codeless-django-0.0.15/codeless_django/writers/files.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,9 +1,10 @@
 from codeless_django.writers.base import BaseWriter
 import os
+from codeless_django.utils import get_os_file_path
 
 class PrepareFiles:
 
     def __init__(self,app_name,write_api_views=False):
         self.app_name=app_name
         self.write_api_views=write_api_views
         self.write_import_line_to_view_file()
@@ -60,11 +61,12 @@
 
 class AdditionalFileWriter:
     def __init__(self):
         self.requirement_text_writer = RequirementTextWriter()
 
 
     def write_gitignore_file(self):
-        os.system("cp codeless_django/additional_files/.gitignore .gitignore")
+        os_file_path = get_os_file_path('additional_files/.gitignore')
+        os.system(f"cp {os_file_path} .gitignore")
     
     def write_new_package_in_requirements_text(self,package_name,version):
         self.requirement_text_writer.add_new_package(package_name, version)
```

### Comparing `codeless-django-0.0.14/codeless_django/writers/models.py` & `codeless-django-0.0.15/codeless_django/writers/models.py`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.14/codeless_django/writers/serializers.py` & `codeless-django-0.0.15/codeless_django/writers/serializers.py`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.14/codeless_django/writers/urls.py` & `codeless-django-0.0.15/codeless_django/writers/urls.py`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.14/codeless_django/writers/views.py` & `codeless-django-0.0.15/codeless_django/writers/views.py`

 * *Files identical despite different names*

### Comparing `codeless-django-0.0.14/codeless_django.egg-info/PKG-INFO` & `codeless-django-0.0.15/codeless_django.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: codeless-django
-Version: 0.0.14
+Version: 0.0.15
 Summary: A Django app to create django apps, models, urls, views , api-views, documentation in a single click
 Home-page: https://www.example.com/
 Author: Omar Faruk
 Author-email: Omar Faruk <omar.iut.09@gmail.com>
 License: BSD-3-Clause  # Example license
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: BSD License
```

### Comparing `codeless-django-0.0.14/codeless_django.egg-info/SOURCES.txt` & `codeless-django-0.0.15/codeless_django.egg-info/SOURCES.txt`

 * *Files 0% similar despite different names*

```diff
@@ -6,14 +6,15 @@
 setup.py
 codeless_django/__init__.py
 codeless_django/apps.py
 codeless_django/data_manager.py
 codeless_django/fields.json
 codeless_django/tests.py
 codeless_django/urls.py
+codeless_django/utils.py
 codeless_django/views.py
 codeless_django.egg-info/PKG-INFO
 codeless_django.egg-info/SOURCES.txt
 codeless_django.egg-info/dependency_links.txt
 codeless_django.egg-info/requires.txt
 codeless_django.egg-info/top_level.txt
 codeless_django/additional_files/.gitignore
```

### Comparing `codeless-django-0.0.14/pyproject.toml` & `codeless-django-0.0.15/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["hatchling"]
 build-backend = "hatchling.build"
 
 [project]
 name = "codeless-django"
-version = "0.0.14"
+version = "0.0.15"
 authors = [
   { name="Omar Faruk", email="omar.iut.09@gmail.com" },
 ]
 description = "A Django app to create django apps, models, urls, views , api-views, documentation in a single click"
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = [
```

### Comparing `codeless-django-0.0.14/setup.cfg` & `codeless-django-0.0.15/setup.cfg`

 * *Files identical despite different names*

