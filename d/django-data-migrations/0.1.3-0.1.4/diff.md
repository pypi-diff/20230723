# Comparing `tmp/django-data-migrations-0.1.3.tar.gz` & `tmp/django-data-migrations-0.1.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "django-data-migrations-0.1.3.tar", last modified: Mon Oct 24 13:12:27 2022, max compression
+gzip compressed data, was "django-data-migrations-0.1.4.tar", last modified: Wed Feb 22 07:47:38 2023, max compression
```

## Comparing `django-data-migrations-0.1.3.tar` & `django-data-migrations-0.1.4.tar`

### file list

```diff
@@ -1,37 +1,37 @@
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-24 13:12:27.578101 django-data-migrations-0.1.3/
--rw-r--r--   0 runner    (1001) docker     (121)     1069 2022-10-24 13:12:10.000000 django-data-migrations-0.1.3/LICENSE
--rw-r--r--   0 runner    (1001) docker     (121)       94 2022-10-24 13:12:10.000000 django-data-migrations-0.1.3/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (121)     5437 2022-10-24 13:12:27.578101 django-data-migrations-0.1.3/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     4258 2022-10-24 13:12:10.000000 django-data-migrations-0.1.3/README.rst
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-24 13:12:27.574101 django-data-migrations-0.1.3/data_migration/
--rw-r--r--   0 runner    (1001) docker     (121)      112 2022-10-24 13:12:10.000000 django-data-migrations-0.1.3/data_migration/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)      300 2022-10-24 13:12:10.000000 django-data-migrations-0.1.3/data_migration/apps.py
--rw-r--r--   0 runner    (1001) docker     (121)      229 2022-10-24 13:12:10.000000 django-data-migrations-0.1.3/data_migration/helper.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-24 13:12:27.574101 django-data-migrations-0.1.3/data_migration/management/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2022-10-24 13:12:10.000000 django-data-migrations-0.1.3/data_migration/management/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-24 13:12:27.574101 django-data-migrations-0.1.3/data_migration/management/commands/
--rw-r--r--   0 runner    (1001) docker     (121)       36 2022-10-24 13:12:10.000000 django-data-migrations-0.1.3/data_migration/management/commands/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     1053 2022-10-24 13:12:10.000000 django-data-migrations-0.1.3/data_migration/management/commands/data_migrate.py
--rw-r--r--   0 runner    (1001) docker     (121)      279 2022-10-24 13:12:10.000000 django-data-migrations-0.1.3/data_migration/management/commands/django_makemigrations.py
--rw-r--r--   0 runner    (1001) docker     (121)      265 2022-10-24 13:12:10.000000 django-data-migrations-0.1.3/data_migration/management/commands/django_migrate.py
--rw-r--r--   0 runner    (1001) docker     (121)      269 2022-10-24 13:12:10.000000 django-data-migrations-0.1.3/data_migration/management/commands/django_squashmigrations.py
--rw-r--r--   0 runner    (1001) docker     (121)     1148 2022-10-24 13:12:10.000000 django-data-migrations-0.1.3/data_migration/management/commands/makemigrations.py
--rw-r--r--   0 runner    (1001) docker     (121)     1143 2022-10-24 13:12:10.000000 django-data-migrations-0.1.3/data_migration/management/commands/migrate.py
--rw-r--r--   0 runner    (1001) docker     (121)     1386 2022-10-24 13:12:10.000000 django-data-migrations-0.1.3/data_migration/management/commands/squashmigrations.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-24 13:12:27.574101 django-data-migrations-0.1.3/data_migration/services/
--rw-r--r--   0 runner    (1001) docker     (121)        0 2022-10-24 13:12:10.000000 django-data-migrations-0.1.3/data_migration/services/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     5167 2022-10-24 13:12:10.000000 django-data-migrations-0.1.3/data_migration/services/file_generator.py
--rw-r--r--   0 runner    (1001) docker     (121)    11491 2022-10-24 13:12:10.000000 django-data-migrations-0.1.3/data_migration/services/graph.py
--rw-r--r--   0 runner    (1001) docker     (121)     3504 2022-10-24 13:12:10.000000 django-data-migrations-0.1.3/data_migration/services/node.py
--rw-r--r--   0 runner    (1001) docker     (121)     8725 2022-10-24 13:12:10.000000 django-data-migrations-0.1.3/data_migration/services/squasher.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-24 13:12:27.574101 django-data-migrations-0.1.3/data_migration/services/templates/
--rw-r--r--   0 runner    (1001) docker     (121)      889 2022-10-24 13:12:10.000000 django-data-migrations-0.1.3/data_migration/services/templates/migration.py.txt
--rw-r--r--   0 runner    (1001) docker     (121)     1140 2022-10-24 13:12:10.000000 django-data-migrations-0.1.3/data_migration/settings.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-10-24 13:12:27.578101 django-data-migrations-0.1.3/django_data_migrations.egg-info/
--rw-r--r--   0 runner    (1001) docker     (121)     5437 2022-10-24 13:12:27.000000 django-data-migrations-0.1.3/django_data_migrations.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     1065 2022-10-24 13:12:27.000000 django-data-migrations-0.1.3/django_data_migrations.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2022-10-24 13:12:27.000000 django-data-migrations-0.1.3/django_data_migrations.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (121)       12 2022-10-24 13:12:27.000000 django-data-migrations-0.1.3/django_data_migrations.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (121)       15 2022-10-24 13:12:27.000000 django-data-migrations-0.1.3/django_data_migrations.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (121)       38 2022-10-24 13:12:27.578101 django-data-migrations-0.1.3/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (121)     1580 2022-10-24 13:12:10.000000 django-data-migrations-0.1.3/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-22 07:47:38.573958 django-data-migrations-0.1.4/
+-rw-r--r--   0 runner    (1001) docker     (123)     1069 2023-02-22 07:47:25.000000 django-data-migrations-0.1.4/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       94 2023-02-22 07:47:25.000000 django-data-migrations-0.1.4/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     5698 2023-02-22 07:47:38.573958 django-data-migrations-0.1.4/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     4519 2023-02-22 07:47:25.000000 django-data-migrations-0.1.4/README.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-22 07:47:38.569957 django-data-migrations-0.1.4/data_migration/
+-rw-r--r--   0 runner    (1001) docker     (123)      112 2023-02-22 07:47:25.000000 django-data-migrations-0.1.4/data_migration/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      300 2023-02-22 07:47:25.000000 django-data-migrations-0.1.4/data_migration/apps.py
+-rw-r--r--   0 runner    (1001) docker     (123)      229 2023-02-22 07:47:25.000000 django-data-migrations-0.1.4/data_migration/helper.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-22 07:47:38.573958 django-data-migrations-0.1.4/data_migration/management/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-22 07:47:25.000000 django-data-migrations-0.1.4/data_migration/management/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-22 07:47:38.573958 django-data-migrations-0.1.4/data_migration/management/commands/
+-rw-r--r--   0 runner    (1001) docker     (123)       36 2023-02-22 07:47:25.000000 django-data-migrations-0.1.4/data_migration/management/commands/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1053 2023-02-22 07:47:25.000000 django-data-migrations-0.1.4/data_migration/management/commands/data_migrate.py
+-rw-r--r--   0 runner    (1001) docker     (123)      279 2023-02-22 07:47:25.000000 django-data-migrations-0.1.4/data_migration/management/commands/django_makemigrations.py
+-rw-r--r--   0 runner    (1001) docker     (123)      265 2023-02-22 07:47:25.000000 django-data-migrations-0.1.4/data_migration/management/commands/django_migrate.py
+-rw-r--r--   0 runner    (1001) docker     (123)      269 2023-02-22 07:47:25.000000 django-data-migrations-0.1.4/data_migration/management/commands/django_squashmigrations.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1148 2023-02-22 07:47:25.000000 django-data-migrations-0.1.4/data_migration/management/commands/makemigrations.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1143 2023-02-22 07:47:25.000000 django-data-migrations-0.1.4/data_migration/management/commands/migrate.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1386 2023-02-22 07:47:25.000000 django-data-migrations-0.1.4/data_migration/management/commands/squashmigrations.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-22 07:47:38.573958 django-data-migrations-0.1.4/data_migration/services/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-02-22 07:47:25.000000 django-data-migrations-0.1.4/data_migration/services/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5167 2023-02-22 07:47:25.000000 django-data-migrations-0.1.4/data_migration/services/file_generator.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11491 2023-02-22 07:47:25.000000 django-data-migrations-0.1.4/data_migration/services/graph.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3504 2023-02-22 07:47:25.000000 django-data-migrations-0.1.4/data_migration/services/node.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8725 2023-02-22 07:47:25.000000 django-data-migrations-0.1.4/data_migration/services/squasher.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-22 07:47:38.573958 django-data-migrations-0.1.4/data_migration/services/templates/
+-rw-r--r--   0 runner    (1001) docker     (123)      889 2023-02-22 07:47:25.000000 django-data-migrations-0.1.4/data_migration/services/templates/migration.py.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1140 2023-02-22 07:47:25.000000 django-data-migrations-0.1.4/data_migration/settings.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-02-22 07:47:38.573958 django-data-migrations-0.1.4/django_data_migrations.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     5698 2023-02-22 07:47:38.000000 django-data-migrations-0.1.4/django_data_migrations.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1065 2023-02-22 07:47:38.000000 django-data-migrations-0.1.4/django_data_migrations.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-02-22 07:47:38.000000 django-data-migrations-0.1.4/django_data_migrations.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       12 2023-02-22 07:47:38.000000 django-data-migrations-0.1.4/django_data_migrations.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       15 2023-02-22 07:47:38.000000 django-data-migrations-0.1.4/django_data_migrations.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-02-22 07:47:38.573958 django-data-migrations-0.1.4/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1580 2023-02-22 07:47:25.000000 django-data-migrations-0.1.4/setup.py
```

### Comparing `django-data-migrations-0.1.3/LICENSE` & `django-data-migrations-0.1.4/LICENSE`

 * *Files identical despite different names*

### Comparing `django-data-migrations-0.1.3/PKG-INFO` & `django-data-migrations-0.1.4/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: django-data-migrations
-Version: 0.1.3
+Version: 0.1.4
 Summary: Extraction tool for data only django migrations
 Home-page: https://github.com/philsupertramp/django-data-migration/
 Author: Philipp Zettl
 Author-email: philipp.zett@godesteem.de
 License: MIT
 Keywords: django,database migrations
 Classifier: Development Status :: 4 - Beta
@@ -32,28 +32,31 @@
 =====================
 
 |Test dev branch|
 |Pypi|
 
 | Developing and maintaining a django project over many years can start to become a constant fight against time consuming tasks including execution of a test suite, recreation of a local environment or setting up a project in a new environment.
 
-| Due to different flavors of deployment and/or different approaches within the same working environment migration files of long running django applications tent to be bloated and contain unnecessary code. Which was at that time implemented to move, edit, duplicate or basically modify data. And the idea behind it is also clever.
+| Due to different flavors of deployment and/or different approaches within the same working environment migration files of long running django applications tent to be bloated and contain unnecessary code. Sometimes we even create migrations in the purpose of single-time usage to move, edit, duplicate or basically modify data.
 
-| With this approach you gained the option to trigger migration of leaf migrations prior to starting your updated application code.
+| Generally speaking, the idea behind it is clever.
+
+| With this approach you gained the option to trigger the execution of leaf migrations prior to starting your updated application code.
 
 .. code:: text
 
            Missing migration?
            /                \
      yes, migrate        no, continue
            \                /
         restart app with new code
 
 | But on the other hand you create a new node within a already giant migration graph.
-| This is where ``django-data-migration`` comes in place. It is a drop-in replacement for regular migrations, without the need of an dedicated node in the migration tree.
+| This is where ``django-data-migration`` comes in place. It is a drop-in replacement for regular migrations, without the need of a dedicated node in the migration tree.
+| It does that, by providing a "data-only" migration graph, that can optionally be maintained automatically in parallel with the existing migration graph, or executed independently, depending on your needs.
 
 Installation
 ============
 
 Install package:
 
 | ``pip install django-data-migrations``
```

### Comparing `django-data-migrations-0.1.3/README.rst` & `django-data-migrations-0.1.4/README.rst`

 * *Files 6% similar despite different names*

```diff
@@ -2,28 +2,31 @@
 =====================
 
 |Test dev branch|
 |Pypi|
 
 | Developing and maintaining a django project over many years can start to become a constant fight against time consuming tasks including execution of a test suite, recreation of a local environment or setting up a project in a new environment.
 
-| Due to different flavors of deployment and/or different approaches within the same working environment migration files of long running django applications tent to be bloated and contain unnecessary code. Which was at that time implemented to move, edit, duplicate or basically modify data. And the idea behind it is also clever.
+| Due to different flavors of deployment and/or different approaches within the same working environment migration files of long running django applications tent to be bloated and contain unnecessary code. Sometimes we even create migrations in the purpose of single-time usage to move, edit, duplicate or basically modify data.
 
-| With this approach you gained the option to trigger migration of leaf migrations prior to starting your updated application code.
+| Generally speaking, the idea behind it is clever.
+
+| With this approach you gained the option to trigger the execution of leaf migrations prior to starting your updated application code.
 
 .. code:: text
 
            Missing migration?
            /                \
      yes, migrate        no, continue
            \                /
         restart app with new code
 
 | But on the other hand you create a new node within a already giant migration graph.
-| This is where ``django-data-migration`` comes in place. It is a drop-in replacement for regular migrations, without the need of an dedicated node in the migration tree.
+| This is where ``django-data-migration`` comes in place. It is a drop-in replacement for regular migrations, without the need of a dedicated node in the migration tree.
+| It does that, by providing a "data-only" migration graph, that can optionally be maintained automatically in parallel with the existing migration graph, or executed independently, depending on your needs.
 
 Installation
 ============
 
 Install package:
 
 | ``pip install django-data-migrations``
```

### Comparing `django-data-migrations-0.1.3/data_migration/management/commands/data_migrate.py` & `django-data-migrations-0.1.4/data_migration/management/commands/data_migrate.py`

 * *Files identical despite different names*

### Comparing `django-data-migrations-0.1.3/data_migration/management/commands/makemigrations.py` & `django-data-migrations-0.1.4/data_migration/management/commands/makemigrations.py`

 * *Files identical despite different names*

### Comparing `django-data-migrations-0.1.3/data_migration/management/commands/migrate.py` & `django-data-migrations-0.1.4/data_migration/management/commands/migrate.py`

 * *Files identical despite different names*

### Comparing `django-data-migrations-0.1.3/data_migration/management/commands/squashmigrations.py` & `django-data-migrations-0.1.4/data_migration/management/commands/squashmigrations.py`

 * *Files identical despite different names*

### Comparing `django-data-migrations-0.1.3/data_migration/services/file_generator.py` & `django-data-migrations-0.1.4/data_migration/services/file_generator.py`

 * *Files identical despite different names*

### Comparing `django-data-migrations-0.1.3/data_migration/services/graph.py` & `django-data-migrations-0.1.4/data_migration/services/graph.py`

 * *Files identical despite different names*

### Comparing `django-data-migrations-0.1.3/data_migration/services/node.py` & `django-data-migrations-0.1.4/data_migration/services/node.py`

 * *Files identical despite different names*

### Comparing `django-data-migrations-0.1.3/data_migration/services/squasher.py` & `django-data-migrations-0.1.4/data_migration/services/squasher.py`

 * *Files identical despite different names*

### Comparing `django-data-migrations-0.1.3/data_migration/services/templates/migration.py.txt` & `django-data-migrations-0.1.4/data_migration/services/templates/migration.py.txt`

 * *Files identical despite different names*

### Comparing `django-data-migrations-0.1.3/data_migration/settings.py` & `django-data-migrations-0.1.4/data_migration/settings.py`

 * *Files identical despite different names*

### Comparing `django-data-migrations-0.1.3/django_data_migrations.egg-info/PKG-INFO` & `django-data-migrations-0.1.4/django_data_migrations.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: django-data-migrations
-Version: 0.1.3
+Version: 0.1.4
 Summary: Extraction tool for data only django migrations
 Home-page: https://github.com/philsupertramp/django-data-migration/
 Author: Philipp Zettl
 Author-email: philipp.zett@godesteem.de
 License: MIT
 Keywords: django,database migrations
 Classifier: Development Status :: 4 - Beta
@@ -32,28 +32,31 @@
 =====================
 
 |Test dev branch|
 |Pypi|
 
 | Developing and maintaining a django project over many years can start to become a constant fight against time consuming tasks including execution of a test suite, recreation of a local environment or setting up a project in a new environment.
 
-| Due to different flavors of deployment and/or different approaches within the same working environment migration files of long running django applications tent to be bloated and contain unnecessary code. Which was at that time implemented to move, edit, duplicate or basically modify data. And the idea behind it is also clever.
+| Due to different flavors of deployment and/or different approaches within the same working environment migration files of long running django applications tent to be bloated and contain unnecessary code. Sometimes we even create migrations in the purpose of single-time usage to move, edit, duplicate or basically modify data.
 
-| With this approach you gained the option to trigger migration of leaf migrations prior to starting your updated application code.
+| Generally speaking, the idea behind it is clever.
+
+| With this approach you gained the option to trigger the execution of leaf migrations prior to starting your updated application code.
 
 .. code:: text
 
            Missing migration?
            /                \
      yes, migrate        no, continue
            \                /
         restart app with new code
 
 | But on the other hand you create a new node within a already giant migration graph.
-| This is where ``django-data-migration`` comes in place. It is a drop-in replacement for regular migrations, without the need of an dedicated node in the migration tree.
+| This is where ``django-data-migration`` comes in place. It is a drop-in replacement for regular migrations, without the need of a dedicated node in the migration tree.
+| It does that, by providing a "data-only" migration graph, that can optionally be maintained automatically in parallel with the existing migration graph, or executed independently, depending on your needs.
 
 Installation
 ============
 
 Install package:
 
 | ``pip install django-data-migrations``
```

### Comparing `django-data-migrations-0.1.3/django_data_migrations.egg-info/SOURCES.txt` & `django-data-migrations-0.1.4/django_data_migrations.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `django-data-migrations-0.1.3/setup.py` & `django-data-migrations-0.1.4/setup.py`

 * *Files identical despite different names*

