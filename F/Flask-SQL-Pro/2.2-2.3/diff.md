# Comparing `tmp/Flask-SQL-Pro-2.2.tar.gz` & `tmp/Flask-SQL-Pro-2.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "Flask-SQL-Pro-2.2.tar", last modified: Fri Jul 21 07:13:00 2023, max compression
+gzip compressed data, was "Flask-SQL-Pro-2.3.tar", last modified: Sun Jul 23 05:14:37 2023, max compression
```

## Comparing `Flask-SQL-Pro-2.2.tar` & `Flask-SQL-Pro-2.3.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxr-xr-x   0 kela       (501) staff       (20)        0 2023-07-21 07:13:00.364610 Flask-SQL-Pro-2.2/
-drwxr-xr-x   0 kela       (501) staff       (20)        0 2023-07-21 07:13:00.363452 Flask-SQL-Pro-2.2/Flask_SQL_Pro.egg-info/
--rw-r--r--   0 kela       (501) staff       (20)      621 2023-07-21 07:13:00.000000 Flask-SQL-Pro-2.2/Flask_SQL_Pro.egg-info/PKG-INFO
--rw-r--r--   0 kela       (501) staff       (20)      277 2023-07-21 07:13:00.000000 Flask-SQL-Pro-2.2/Flask_SQL_Pro.egg-info/SOURCES.txt
--rw-r--r--   0 kela       (501) staff       (20)        1 2023-07-21 07:13:00.000000 Flask-SQL-Pro-2.2/Flask_SQL_Pro.egg-info/dependency_links.txt
--rw-r--r--   0 kela       (501) staff       (20)       30 2023-07-21 07:13:00.000000 Flask-SQL-Pro-2.2/Flask_SQL_Pro.egg-info/requires.txt
--rw-r--r--   0 kela       (501) staff       (20)       14 2023-07-21 07:13:00.000000 Flask-SQL-Pro-2.2/Flask_SQL_Pro.egg-info/top_level.txt
--rw-r--r--   0 kela       (501) staff       (20)      621 2023-07-21 07:13:00.364483 Flask-SQL-Pro-2.2/PKG-INFO
--rw-r--r--   0 kela       (501) staff       (20)       63 2023-07-21 07:09:30.000000 Flask-SQL-Pro-2.2/README.rst
-drwxr-xr-x   0 kela       (501) staff       (20)        0 2023-07-21 07:13:00.364185 Flask-SQL-Pro-2.2/flask_sql_pro/
--rw-r--r--   0 kela       (501) staff       (20)     1739 2023-07-21 05:57:01.000000 Flask-SQL-Pro-2.2/flask_sql_pro/__init__.py
--rw-r--r--   0 kela       (501) staff       (20)     8149 2023-07-21 05:07:24.000000 Flask-SQL-Pro-2.2/flask_sql_pro/db.py
--rw-r--r--   0 kela       (501) staff       (20)     6025 2023-07-21 05:10:52.000000 Flask-SQL-Pro-2.2/flask_sql_pro/sql_loader.py
--rw-r--r--   0 kela       (501) staff       (20)       38 2023-07-21 07:13:00.364658 Flask-SQL-Pro-2.2/setup.cfg
--rw-r--r--   0 kela       (501) staff       (20)      856 2023-07-21 07:12:53.000000 Flask-SQL-Pro-2.2/setup.py
+drwxr-xr-x   0 kela       (501) staff       (20)        0 2023-07-23 05:14:37.957772 Flask-SQL-Pro-2.3/
+drwxr-xr-x   0 kela       (501) staff       (20)        0 2023-07-23 05:14:37.956273 Flask-SQL-Pro-2.3/Flask_SQL_Pro.egg-info/
+-rw-r--r--   0 kela       (501) staff       (20)     8512 2023-07-23 05:14:37.000000 Flask-SQL-Pro-2.3/Flask_SQL_Pro.egg-info/PKG-INFO
+-rw-r--r--   0 kela       (501) staff       (20)      277 2023-07-23 05:14:37.000000 Flask-SQL-Pro-2.3/Flask_SQL_Pro.egg-info/SOURCES.txt
+-rw-r--r--   0 kela       (501) staff       (20)        1 2023-07-23 05:14:37.000000 Flask-SQL-Pro-2.3/Flask_SQL_Pro.egg-info/dependency_links.txt
+-rw-r--r--   0 kela       (501) staff       (20)       30 2023-07-23 05:14:37.000000 Flask-SQL-Pro-2.3/Flask_SQL_Pro.egg-info/requires.txt
+-rw-r--r--   0 kela       (501) staff       (20)       14 2023-07-23 05:14:37.000000 Flask-SQL-Pro-2.3/Flask_SQL_Pro.egg-info/top_level.txt
+-rw-r--r--   0 kela       (501) staff       (20)     8512 2023-07-23 05:14:37.957611 Flask-SQL-Pro-2.3/PKG-INFO
+-rw-r--r--   0 kela       (501) staff       (20)     7955 2023-07-23 05:13:56.000000 Flask-SQL-Pro-2.3/README.rst
+drwxr-xr-x   0 kela       (501) staff       (20)        0 2023-07-23 05:14:37.957275 Flask-SQL-Pro-2.3/flask_sql_pro/
+-rw-r--r--   0 kela       (501) staff       (20)     1739 2023-07-21 05:57:01.000000 Flask-SQL-Pro-2.3/flask_sql_pro/__init__.py
+-rw-r--r--   0 kela       (501) staff       (20)     8149 2023-07-21 05:07:24.000000 Flask-SQL-Pro-2.3/flask_sql_pro/db.py
+-rw-r--r--   0 kela       (501) staff       (20)     6025 2023-07-21 05:10:52.000000 Flask-SQL-Pro-2.3/flask_sql_pro/sql_loader.py
+-rw-r--r--   0 kela       (501) staff       (20)       38 2023-07-23 05:14:37.957816 Flask-SQL-Pro-2.3/setup.cfg
+-rw-r--r--   0 kela       (501) staff       (20)      856 2023-07-23 05:06:34.000000 Flask-SQL-Pro-2.3/setup.py
```

### Comparing `Flask-SQL-Pro-2.2/flask_sql_pro/__init__.py` & `Flask-SQL-Pro-2.3/flask_sql_pro/__init__.py`

 * *Files identical despite different names*

### Comparing `Flask-SQL-Pro-2.2/flask_sql_pro/db.py` & `Flask-SQL-Pro-2.3/flask_sql_pro/db.py`

 * *Files identical despite different names*

### Comparing `Flask-SQL-Pro-2.2/flask_sql_pro/sql_loader.py` & `Flask-SQL-Pro-2.3/flask_sql_pro/sql_loader.py`

 * *Files identical despite different names*

### Comparing `Flask-SQL-Pro-2.2/setup.py` & `Flask-SQL-Pro-2.3/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name='Flask-SQL-Pro',
-    version='2.2',
+    version='2.3',
     description='旨在为写sql的程序拆分sql语句出程序中,分类管理。目前支持增删改查、分页、事务,以及flask项目中多数据库连接。',
     long_description=open('README.rst').read(),
     author='miaokela',
     author_email='2972799448@qq.com',
     maintainer='miaokela',
     maintainer_email='2972799448@qq.com',
     packages=find_packages(),
```

