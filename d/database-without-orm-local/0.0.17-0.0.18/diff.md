# Comparing `tmp/database-without-orm-local-0.0.17.tar.gz` & `tmp/database-without-orm-local-0.0.18.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "database-without-orm-local-0.0.17.tar", last modified: Sat Jul 22 10:44:48 2023, max compression
+gzip compressed data, was "database-without-orm-local-0.0.18.tar", last modified: Sun Jul 23 16:46:23 2023, max compression
```

## Comparing `database-without-orm-local-0.0.17.tar` & `database-without-orm-local-0.0.18.tar`

### file list

```diff
@@ -1,14 +1,14 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 10:44:48.020954 database-without-orm-local-0.0.17/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-22 10:44:19.000000 database-without-orm-local-0.0.17/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      489 2023-07-22 10:44:48.016954 database-without-orm-local-0.0.17/PKG-INFO
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 10:44:48.016954 database-without-orm-local-0.0.17/circles_local_database_python/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-22 10:44:19.000000 database-without-orm-local-0.0.17/circles_local_database_python/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1275 2023-07-22 10:44:19.000000 database-without-orm-local-0.0.17/circles_local_database_python/database.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 10:44:48.016954 database-without-orm-local-0.0.17/database_without_orm_local.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)      489 2023-07-22 10:44:48.000000 database-without-orm-local-0.0.17/database_without_orm_local.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      315 2023-07-22 10:44:48.000000 database-without-orm-local-0.0.17/database_without_orm_local.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-22 10:44:48.000000 database-without-orm-local-0.0.17/database_without_orm_local.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       30 2023-07-22 10:44:48.000000 database-without-orm-local-0.0.17/database_without_orm_local.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       86 2023-07-22 10:44:19.000000 database-without-orm-local-0.0.17/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-22 10:44:48.020954 database-without-orm-local-0.0.17/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      698 2023-07-22 10:44:19.000000 database-without-orm-local-0.0.17/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:46:23.390596 database-without-orm-local-0.0.18/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 16:46:01.000000 database-without-orm-local-0.0.18/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      489 2023-07-23 16:46:23.390596 database-without-orm-local-0.0.18/PKG-INFO
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:46:23.390596 database-without-orm-local-0.0.18/circles_local_database_python/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 16:46:01.000000 database-without-orm-local-0.0.18/circles_local_database_python/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1260 2023-07-23 16:46:01.000000 database-without-orm-local-0.0.18/circles_local_database_python/database.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:46:23.390596 database-without-orm-local-0.0.18/database_without_orm_local.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)      489 2023-07-23 16:46:23.000000 database-without-orm-local-0.0.18/database_without_orm_local.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      315 2023-07-23 16:46:23.000000 database-without-orm-local-0.0.18/database_without_orm_local.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 16:46:23.000000 database-without-orm-local-0.0.18/database_without_orm_local.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       30 2023-07-23 16:46:23.000000 database-without-orm-local-0.0.18/database_without_orm_local.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       86 2023-07-23 16:46:01.000000 database-without-orm-local-0.0.18/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 16:46:23.390596 database-without-orm-local-0.0.18/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      698 2023-07-23 16:46:01.000000 database-without-orm-local-0.0.18/setup.py
```

### Comparing `database-without-orm-local-0.0.17/circles_local_database_python/database.py` & `database-without-orm-local-0.0.18/circles_local_database_python/database.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import mysql.connector
 import os
 from dotenv import load_dotenv
-from logger_local_python_package.LoggerLocal import logger_local
+from logger_local.LoggerLocal import logger_local
 load_dotenv()
 
 DATABASE_WITHOUT_ORM_COMPONENT_ID = 112
 
 
 class database():
     def connect_to_database(self):
```

### Comparing `database-without-orm-local-0.0.17/setup.py` & `database-without-orm-local-0.0.18/setup.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 import setuptools
 # used by python -m build
 setuptools.setup(
     name='database-without-orm-local',
-    version='0.0.17',  # https://pypi.org/project/database-without-orm-local/
+    version='0.0.18',  # https://pypi.org/project/database-without-orm-local/
     author="Circles",
     author_email="info@circles.life",
     description="Circles Local Database without ORM Python PyPI Package",
     long_description="This is a package for sharing common Database methods",
     long_description_content_type="text/markdown",
     url="https://github.com/javatechy/dokr",
     packages=setuptools.find_packages(),
```

