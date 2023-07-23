# Comparing `tmp/aa_example_plugin-0.0.5.tar.gz` & `tmp/aa_example_plugin-0.0.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "aa_example_plugin-0.0.5.tar", last modified: Tue Apr 18 16:04:49 2023, max compression
+gzip compressed data, was "aa_example_plugin-0.0.6.tar", last modified: Sun Jul 23 19:50:58 2023, max compression
```

## Comparing `aa_example_plugin-0.0.5.tar` & `aa_example_plugin-0.0.6.tar`

### file list

```diff
@@ -1,39 +1,39 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-18 16:04:49.773968 aa_example_plugin-0.0.5/
--rw-r--r--   0 runner    (1001) docker     (123)    35149 2023-04-18 16:04:29.000000 aa_example_plugin-0.0.5/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      120 2023-04-18 16:04:29.000000 aa_example_plugin-0.0.5/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     9715 2023-04-18 16:04:49.773968 aa_example_plugin-0.0.5/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     8467 2023-04-18 16:04:29.000000 aa_example_plugin-0.0.5/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-18 16:04:49.769967 aa_example_plugin-0.0.5/aa_example_plugin.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     9715 2023-04-18 16:04:49.000000 aa_example_plugin-0.0.5/aa_example_plugin.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      716 2023-04-18 16:04:49.000000 aa_example_plugin-0.0.5/aa_example_plugin.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-04-18 16:04:49.000000 aa_example_plugin-0.0.5/aa_example_plugin.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-04-18 16:04:49.000000 aa_example_plugin-0.0.5/aa_example_plugin.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)       20 2023-04-18 16:04:49.000000 aa_example_plugin-0.0.5/aa_example_plugin.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        8 2023-04-18 16:04:49.000000 aa_example_plugin-0.0.5/aa_example_plugin.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-18 16:04:49.773968 aa_example_plugin-0.0.5/example/
--rw-r--r--   0 runner    (1001) docker     (123)       70 2023-04-18 16:04:29.000000 aa_example_plugin-0.0.5/example/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      106 2023-04-18 16:04:29.000000 aa_example_plugin-0.0.5/example/admin.py
--rw-r--r--   0 runner    (1001) docker     (123)      163 2023-04-18 16:04:29.000000 aa_example_plugin-0.0.5/example/app_settings.py
--rw-r--r--   0 runner    (1001) docker     (123)      266 2023-04-18 16:04:29.000000 aa_example_plugin-0.0.5/example/apps.py
--rw-r--r--   0 runner    (1001) docker     (123)     1062 2023-04-18 16:04:29.000000 aa_example_plugin-0.0.5/example/auth_hooks.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-18 16:04:49.773968 aa_example_plugin-0.0.5/example/locale/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-18 16:04:29.000000 aa_example_plugin-0.0.5/example/locale/.gitkeep
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-18 16:04:49.773968 aa_example_plugin-0.0.5/example/migrations/
--rw-r--r--   0 runner    (1001) docker     (123)      798 2023-04-18 16:04:29.000000 aa_example_plugin-0.0.5/example/migrations/0001_initial.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-18 16:04:29.000000 aa_example_plugin-0.0.5/example/migrations/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      328 2023-04-18 16:04:29.000000 aa_example_plugin-0.0.5/example/models.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-18 16:04:49.765967 aa_example_plugin-0.0.5/example/static/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-18 16:04:49.773968 aa_example_plugin-0.0.5/example/static/example/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-18 16:04:29.000000 aa_example_plugin-0.0.5/example/static/example/.gitkeep
--rw-r--r--   0 runner    (1001) docker     (123)      244 2023-04-18 16:04:29.000000 aa_example_plugin-0.0.5/example/tasks.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-18 16:04:49.765967 aa_example_plugin-0.0.5/example/templates/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-18 16:04:49.773968 aa_example_plugin-0.0.5/example/templates/example/
--rw-r--r--   0 runner    (1001) docker     (123)      343 2023-04-18 16:04:29.000000 aa_example_plugin-0.0.5/example/templates/example/base.html
--rw-r--r--   0 runner    (1001) docker     (123)      478 2023-04-18 16:04:29.000000 aa_example_plugin-0.0.5/example/templates/example/index.html
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-18 16:04:49.773968 aa_example_plugin-0.0.5/example/tests/
--rw-r--r--   0 runner    (1001) docker     (123)       27 2023-04-18 16:04:29.000000 aa_example_plugin-0.0.5/example/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      436 2023-04-18 16:04:29.000000 aa_example_plugin-0.0.5/example/tests/test_example.py
--rw-r--r--   0 runner    (1001) docker     (123)      185 2023-04-18 16:04:29.000000 aa_example_plugin-0.0.5/example/urls.py
--rw-r--r--   0 runner    (1001) docker     (123)      504 2023-04-18 16:04:29.000000 aa_example_plugin-0.0.5/example/views.py
--rw-r--r--   0 runner    (1001) docker     (123)      104 2023-04-18 16:04:29.000000 aa_example_plugin-0.0.5/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)     1419 2023-04-18 16:04:49.777968 aa_example_plugin-0.0.5/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:50:58.402521 aa_example_plugin-0.0.6/
+-rw-r--r--   0 runner    (1001) docker     (123)    35149 2023-07-23 19:50:37.000000 aa_example_plugin-0.0.6/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      120 2023-07-23 19:50:37.000000 aa_example_plugin-0.0.6/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     9715 2023-07-23 19:50:58.402521 aa_example_plugin-0.0.6/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     8467 2023-07-23 19:50:37.000000 aa_example_plugin-0.0.6/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:50:58.398521 aa_example_plugin-0.0.6/aa_example_plugin.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     9715 2023-07-23 19:50:58.000000 aa_example_plugin-0.0.6/aa_example_plugin.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      716 2023-07-23 19:50:58.000000 aa_example_plugin-0.0.6/aa_example_plugin.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 19:50:58.000000 aa_example_plugin-0.0.6/aa_example_plugin.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 19:50:58.000000 aa_example_plugin-0.0.6/aa_example_plugin.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)       20 2023-07-23 19:50:58.000000 aa_example_plugin-0.0.6/aa_example_plugin.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        8 2023-07-23 19:50:58.000000 aa_example_plugin-0.0.6/aa_example_plugin.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:50:58.398521 aa_example_plugin-0.0.6/example/
+-rw-r--r--   0 runner    (1001) docker     (123)       70 2023-07-23 19:50:37.000000 aa_example_plugin-0.0.6/example/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      106 2023-07-23 19:50:37.000000 aa_example_plugin-0.0.6/example/admin.py
+-rw-r--r--   0 runner    (1001) docker     (123)      163 2023-07-23 19:50:37.000000 aa_example_plugin-0.0.6/example/app_settings.py
+-rw-r--r--   0 runner    (1001) docker     (123)      266 2023-07-23 19:50:37.000000 aa_example_plugin-0.0.6/example/apps.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1062 2023-07-23 19:50:37.000000 aa_example_plugin-0.0.6/example/auth_hooks.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:50:58.398521 aa_example_plugin-0.0.6/example/locale/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:50:37.000000 aa_example_plugin-0.0.6/example/locale/.gitkeep
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:50:58.398521 aa_example_plugin-0.0.6/example/migrations/
+-rw-r--r--   0 runner    (1001) docker     (123)      797 2023-07-23 19:50:37.000000 aa_example_plugin-0.0.6/example/migrations/0001_initial.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:50:37.000000 aa_example_plugin-0.0.6/example/migrations/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      328 2023-07-23 19:50:37.000000 aa_example_plugin-0.0.6/example/models.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:50:58.394521 aa_example_plugin-0.0.6/example/static/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:50:58.398521 aa_example_plugin-0.0.6/example/static/example/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 19:50:37.000000 aa_example_plugin-0.0.6/example/static/example/.gitkeep
+-rw-r--r--   0 runner    (1001) docker     (123)      244 2023-07-23 19:50:37.000000 aa_example_plugin-0.0.6/example/tasks.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:50:58.394521 aa_example_plugin-0.0.6/example/templates/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:50:58.402521 aa_example_plugin-0.0.6/example/templates/example/
+-rw-r--r--   0 runner    (1001) docker     (123)      343 2023-07-23 19:50:37.000000 aa_example_plugin-0.0.6/example/templates/example/base.html
+-rw-r--r--   0 runner    (1001) docker     (123)      478 2023-07-23 19:50:37.000000 aa_example_plugin-0.0.6/example/templates/example/index.html
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:50:58.402521 aa_example_plugin-0.0.6/example/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)       27 2023-07-23 19:50:37.000000 aa_example_plugin-0.0.6/example/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      436 2023-07-23 19:50:37.000000 aa_example_plugin-0.0.6/example/tests/test_example.py
+-rw-r--r--   0 runner    (1001) docker     (123)      185 2023-07-23 19:50:37.000000 aa_example_plugin-0.0.6/example/urls.py
+-rw-r--r--   0 runner    (1001) docker     (123)      504 2023-07-23 19:50:37.000000 aa_example_plugin-0.0.6/example/views.py
+-rw-r--r--   0 runner    (1001) docker     (123)      104 2023-07-23 19:50:37.000000 aa_example_plugin-0.0.6/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)     1420 2023-07-23 19:50:58.402521 aa_example_plugin-0.0.6/setup.cfg
```

### Comparing `aa_example_plugin-0.0.5/LICENSE` & `aa_example_plugin-0.0.6/LICENSE`

 * *Files identical despite different names*

### Comparing `aa_example_plugin-0.0.5/PKG-INFO` & `aa_example_plugin-0.0.6/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: aa_example_plugin
-Version: 0.0.5
+Version: 0.0.6
 Summary: Example Plugin for Alliance Auth (GitHub Version)
 Home-page: https://github.com/ppfeufer/aa-example-plugin
 Author: Peter Pfeufer
 Author-email: development@ppfeufer.de
 Maintainer: Peter Pfeufer
 Maintainer-email: development@ppfeufer.de
 License: GPL-3.0
```

### Comparing `aa_example_plugin-0.0.5/README.md` & `aa_example_plugin-0.0.6/README.md`

 * *Files identical despite different names*

### Comparing `aa_example_plugin-0.0.5/aa_example_plugin.egg-info/PKG-INFO` & `aa_example_plugin-0.0.6/aa_example_plugin.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: aa-example-plugin
-Version: 0.0.5
+Version: 0.0.6
 Summary: Example Plugin for Alliance Auth (GitHub Version)
 Home-page: https://github.com/ppfeufer/aa-example-plugin
 Author: Peter Pfeufer
 Author-email: development@ppfeufer.de
 Maintainer: Peter Pfeufer
 Maintainer-email: development@ppfeufer.de
 License: GPL-3.0
```

### Comparing `aa_example_plugin-0.0.5/aa_example_plugin.egg-info/SOURCES.txt` & `aa_example_plugin-0.0.6/aa_example_plugin.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `aa_example_plugin-0.0.5/example/auth_hooks.py` & `aa_example_plugin-0.0.6/example/auth_hooks.py`

 * *Files identical despite different names*

### Comparing `aa_example_plugin-0.0.5/example/migrations/0001_initial.py` & `aa_example_plugin-0.0.6/example/migrations/0001_initial.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,14 @@
 # Generated by Django 4.0.3 on 2022-03-12 20:03
 
 # Django
 from django.db import migrations, models
 
 
 class Migration(migrations.Migration):
-
     initial = True
 
     dependencies = []
 
     operations = [
         migrations.CreateModel(
             name="General",
```

### Comparing `aa_example_plugin-0.0.5/setup.cfg` & `aa_example_plugin-0.0.6/setup.cfg`

 * *Files 0% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 long_description = file: README.md
 long_description_content_type = text/markdown
 author = Peter Pfeufer
 author_email = development@ppfeufer.de
 maintainer = Peter Pfeufer
 maintainer_email = development@ppfeufer.de
 license = GPL-3.0
-license_file = LICENSE
+license_files = LICENSE
 classifiers = 
 	Environment :: Web Environment
 	Framework :: Django
 	Framework :: Django :: 4.0
 	Intended Audience :: Developers
 	License :: OSI Approved :: GNU General Public License v3 (GPLv3)
 	Operating System :: OS Independent
```

