# Comparing `tmp/Flask-SQL-Pro-3.2.tar.gz` & `tmp/Flask-SQL-Pro-3.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "Flask-SQL-Pro-3.2.tar", last modified: Sun Jul 23 16:48:43 2023, max compression
+gzip compressed data, was "Flask-SQL-Pro-3.3.tar", last modified: Sun Jul 23 16:51:01 2023, max compression
```

## Comparing `Flask-SQL-Pro-3.2.tar` & `Flask-SQL-Pro-3.3.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxr-xr-x   0 kela       (501) staff       (20)        0 2023-07-23 16:48:43.207086 Flask-SQL-Pro-3.2/
-drwxr-xr-x   0 kela       (501) staff       (20)        0 2023-07-23 16:48:43.206200 Flask-SQL-Pro-3.2/Flask_SQL_Pro.egg-info/
--rw-r--r--   0 kela       (501) staff       (20)     8833 2023-07-23 16:48:43.000000 Flask-SQL-Pro-3.2/Flask_SQL_Pro.egg-info/PKG-INFO
--rw-r--r--   0 kela       (501) staff       (20)      277 2023-07-23 16:48:43.000000 Flask-SQL-Pro-3.2/Flask_SQL_Pro.egg-info/SOURCES.txt
--rw-r--r--   0 kela       (501) staff       (20)        1 2023-07-23 16:48:43.000000 Flask-SQL-Pro-3.2/Flask_SQL_Pro.egg-info/dependency_links.txt
--rw-r--r--   0 kela       (501) staff       (20)       30 2023-07-23 16:48:43.000000 Flask-SQL-Pro-3.2/Flask_SQL_Pro.egg-info/requires.txt
--rw-r--r--   0 kela       (501) staff       (20)       14 2023-07-23 16:48:43.000000 Flask-SQL-Pro-3.2/Flask_SQL_Pro.egg-info/top_level.txt
--rw-r--r--   0 kela       (501) staff       (20)     8833 2023-07-23 16:48:43.206895 Flask-SQL-Pro-3.2/PKG-INFO
--rw-r--r--   0 kela       (501) staff       (20)     8316 2023-07-23 16:37:58.000000 Flask-SQL-Pro-3.2/README.rst
-drwxr-xr-x   0 kela       (501) staff       (20)        0 2023-07-23 16:48:43.206637 Flask-SQL-Pro-3.2/flask_sql_pro/
--rw-r--r--   0 kela       (501) staff       (20)     1843 2023-07-23 16:05:44.000000 Flask-SQL-Pro-3.2/flask_sql_pro/__init__.py
--rw-r--r--   0 kela       (501) staff       (20)     8878 2023-07-23 16:48:22.000000 Flask-SQL-Pro-3.2/flask_sql_pro/db.py
--rw-r--r--   0 kela       (501) staff       (20)     6020 2023-07-23 16:21:52.000000 Flask-SQL-Pro-3.2/flask_sql_pro/sql_loader.py
--rw-r--r--   0 kela       (501) staff       (20)       38 2023-07-23 16:48:43.207136 Flask-SQL-Pro-3.2/setup.cfg
--rw-r--r--   0 kela       (501) staff       (20)      816 2023-07-23 16:48:31.000000 Flask-SQL-Pro-3.2/setup.py
+drwxr-xr-x   0 kela       (501) staff       (20)        0 2023-07-23 16:51:01.002243 Flask-SQL-Pro-3.3/
+drwxr-xr-x   0 kela       (501) staff       (20)        0 2023-07-23 16:51:01.001192 Flask-SQL-Pro-3.3/Flask_SQL_Pro.egg-info/
+-rw-r--r--   0 kela       (501) staff       (20)     8833 2023-07-23 16:51:00.000000 Flask-SQL-Pro-3.3/Flask_SQL_Pro.egg-info/PKG-INFO
+-rw-r--r--   0 kela       (501) staff       (20)      277 2023-07-23 16:51:00.000000 Flask-SQL-Pro-3.3/Flask_SQL_Pro.egg-info/SOURCES.txt
+-rw-r--r--   0 kela       (501) staff       (20)        1 2023-07-23 16:51:00.000000 Flask-SQL-Pro-3.3/Flask_SQL_Pro.egg-info/dependency_links.txt
+-rw-r--r--   0 kela       (501) staff       (20)       30 2023-07-23 16:51:00.000000 Flask-SQL-Pro-3.3/Flask_SQL_Pro.egg-info/requires.txt
+-rw-r--r--   0 kela       (501) staff       (20)       14 2023-07-23 16:51:00.000000 Flask-SQL-Pro-3.3/Flask_SQL_Pro.egg-info/top_level.txt
+-rw-r--r--   0 kela       (501) staff       (20)     8833 2023-07-23 16:51:01.002059 Flask-SQL-Pro-3.3/PKG-INFO
+-rw-r--r--   0 kela       (501) staff       (20)     8316 2023-07-23 16:37:58.000000 Flask-SQL-Pro-3.3/README.rst
+drwxr-xr-x   0 kela       (501) staff       (20)        0 2023-07-23 16:51:01.001744 Flask-SQL-Pro-3.3/flask_sql_pro/
+-rw-r--r--   0 kela       (501) staff       (20)     1843 2023-07-23 16:05:44.000000 Flask-SQL-Pro-3.3/flask_sql_pro/__init__.py
+-rw-r--r--   0 kela       (501) staff       (20)     8872 2023-07-23 16:50:42.000000 Flask-SQL-Pro-3.3/flask_sql_pro/db.py
+-rw-r--r--   0 kela       (501) staff       (20)     6020 2023-07-23 16:21:52.000000 Flask-SQL-Pro-3.3/flask_sql_pro/sql_loader.py
+-rw-r--r--   0 kela       (501) staff       (20)       38 2023-07-23 16:51:01.002296 Flask-SQL-Pro-3.3/setup.cfg
+-rw-r--r--   0 kela       (501) staff       (20)      816 2023-07-23 16:50:47.000000 Flask-SQL-Pro-3.3/setup.py
```

### Comparing `Flask-SQL-Pro-3.2/Flask_SQL_Pro.egg-info/PKG-INFO` & `Flask-SQL-Pro-3.3/Flask_SQL_Pro.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: Flask-SQL-Pro
-Version: 3.2
+Version: 3.3
 Summary: 基于Flask-SQLAlchemy, 抽离SQL语句, 使用Jinja2语法实现动态SQL, 支持上下文事务, 支持分页
 Author: miaokela
 Author-email: 2972799448@qq.com
 Maintainer: miaokela
 Maintainer-email: 2972799448@qq.com
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3.7
```

### Comparing `Flask-SQL-Pro-3.2/PKG-INFO` & `Flask-SQL-Pro-3.3/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: Flask-SQL-Pro
-Version: 3.2
+Version: 3.3
 Summary: 基于Flask-SQLAlchemy, 抽离SQL语句, 使用Jinja2语法实现动态SQL, 支持上下文事务, 支持分页
 Author: miaokela
 Author-email: 2972799448@qq.com
 Maintainer: miaokela
 Maintainer-email: 2972799448@qq.com
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3.7
```

### Comparing `Flask-SQL-Pro-3.2/README.rst` & `Flask-SQL-Pro-3.3/README.rst`

 * *Files identical despite different names*

### Comparing `Flask-SQL-Pro-3.2/flask_sql_pro/__init__.py` & `Flask-SQL-Pro-3.3/flask_sql_pro/__init__.py`

 * *Files identical despite different names*

### Comparing `Flask-SQL-Pro-3.2/flask_sql_pro/db.py` & `Flask-SQL-Pro-3.3/flask_sql_pro/db.py`

 * *Files 1% similar despite different names*

```diff
@@ -168,18 +168,18 @@
         :param app:
         :param logic:
         :param tb_name: indicates the table name
         :param where: indicates the filter condition
         :return: indicates the number of deleted items
         """
         if logic:
-            sql = "UPDATE `:table` SET `:flag`=1"
+            sql = "UPDATE :table SET :flag=1"
             params = {"table": tb_name, "flag": cls.logic_delete_flag}
         else:
-            sql = "DELETE FROM `:table`"
+            sql = "DELETE FROM :table"
             params = {"table": tb_name}
             
         sql = cls.set_where_phrase(sql, where)
         where = cls.fullfilled_data({}, where)
 
         params.update(where)
```

### Comparing `Flask-SQL-Pro-3.2/flask_sql_pro/sql_loader.py` & `Flask-SQL-Pro-3.3/flask_sql_pro/sql_loader.py`

 * *Files identical despite different names*

### Comparing `Flask-SQL-Pro-3.2/setup.py` & `Flask-SQL-Pro-3.3/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name='Flask-SQL-Pro',
-    version='3.2',
+    version='3.3',
     description='基于Flask-SQLAlchemy, 抽离SQL语句, 使用Jinja2语法实现动态SQL, 支持上下文事务, 支持分页',
     long_description=open('README.rst').read(),
     author='miaokela',
     author_email='2972799448@qq.com',
     maintainer='miaokela',
     maintainer_email='2972799448@qq.com',
     packages=find_packages(),
```

