# Comparing `tmp/Flask-SQL-Pro-3.3.tar.gz` & `tmp/Flask-SQL-Pro-3.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "Flask-SQL-Pro-3.3.tar", last modified: Sun Jul 23 16:51:01 2023, max compression
+gzip compressed data, was "Flask-SQL-Pro-3.4.tar", last modified: Sun Jul 23 16:58:51 2023, max compression
```

## Comparing `Flask-SQL-Pro-3.3.tar` & `Flask-SQL-Pro-3.4.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxr-xr-x   0 kela       (501) staff       (20)        0 2023-07-23 16:51:01.002243 Flask-SQL-Pro-3.3/
-drwxr-xr-x   0 kela       (501) staff       (20)        0 2023-07-23 16:51:01.001192 Flask-SQL-Pro-3.3/Flask_SQL_Pro.egg-info/
--rw-r--r--   0 kela       (501) staff       (20)     8833 2023-07-23 16:51:00.000000 Flask-SQL-Pro-3.3/Flask_SQL_Pro.egg-info/PKG-INFO
--rw-r--r--   0 kela       (501) staff       (20)      277 2023-07-23 16:51:00.000000 Flask-SQL-Pro-3.3/Flask_SQL_Pro.egg-info/SOURCES.txt
--rw-r--r--   0 kela       (501) staff       (20)        1 2023-07-23 16:51:00.000000 Flask-SQL-Pro-3.3/Flask_SQL_Pro.egg-info/dependency_links.txt
--rw-r--r--   0 kela       (501) staff       (20)       30 2023-07-23 16:51:00.000000 Flask-SQL-Pro-3.3/Flask_SQL_Pro.egg-info/requires.txt
--rw-r--r--   0 kela       (501) staff       (20)       14 2023-07-23 16:51:00.000000 Flask-SQL-Pro-3.3/Flask_SQL_Pro.egg-info/top_level.txt
--rw-r--r--   0 kela       (501) staff       (20)     8833 2023-07-23 16:51:01.002059 Flask-SQL-Pro-3.3/PKG-INFO
--rw-r--r--   0 kela       (501) staff       (20)     8316 2023-07-23 16:37:58.000000 Flask-SQL-Pro-3.3/README.rst
-drwxr-xr-x   0 kela       (501) staff       (20)        0 2023-07-23 16:51:01.001744 Flask-SQL-Pro-3.3/flask_sql_pro/
--rw-r--r--   0 kela       (501) staff       (20)     1843 2023-07-23 16:05:44.000000 Flask-SQL-Pro-3.3/flask_sql_pro/__init__.py
--rw-r--r--   0 kela       (501) staff       (20)     8872 2023-07-23 16:50:42.000000 Flask-SQL-Pro-3.3/flask_sql_pro/db.py
--rw-r--r--   0 kela       (501) staff       (20)     6020 2023-07-23 16:21:52.000000 Flask-SQL-Pro-3.3/flask_sql_pro/sql_loader.py
--rw-r--r--   0 kela       (501) staff       (20)       38 2023-07-23 16:51:01.002296 Flask-SQL-Pro-3.3/setup.cfg
--rw-r--r--   0 kela       (501) staff       (20)      816 2023-07-23 16:50:47.000000 Flask-SQL-Pro-3.3/setup.py
+drwxr-xr-x   0 kela       (501) staff       (20)        0 2023-07-23 16:58:51.966322 Flask-SQL-Pro-3.4/
+drwxr-xr-x   0 kela       (501) staff       (20)        0 2023-07-23 16:58:51.965383 Flask-SQL-Pro-3.4/Flask_SQL_Pro.egg-info/
+-rw-r--r--   0 kela       (501) staff       (20)     8833 2023-07-23 16:58:51.000000 Flask-SQL-Pro-3.4/Flask_SQL_Pro.egg-info/PKG-INFO
+-rw-r--r--   0 kela       (501) staff       (20)      277 2023-07-23 16:58:51.000000 Flask-SQL-Pro-3.4/Flask_SQL_Pro.egg-info/SOURCES.txt
+-rw-r--r--   0 kela       (501) staff       (20)        1 2023-07-23 16:58:51.000000 Flask-SQL-Pro-3.4/Flask_SQL_Pro.egg-info/dependency_links.txt
+-rw-r--r--   0 kela       (501) staff       (20)       30 2023-07-23 16:58:51.000000 Flask-SQL-Pro-3.4/Flask_SQL_Pro.egg-info/requires.txt
+-rw-r--r--   0 kela       (501) staff       (20)       14 2023-07-23 16:58:51.000000 Flask-SQL-Pro-3.4/Flask_SQL_Pro.egg-info/top_level.txt
+-rw-r--r--   0 kela       (501) staff       (20)     8833 2023-07-23 16:58:51.966073 Flask-SQL-Pro-3.4/PKG-INFO
+-rw-r--r--   0 kela       (501) staff       (20)     8316 2023-07-23 16:37:58.000000 Flask-SQL-Pro-3.4/README.rst
+drwxr-xr-x   0 kela       (501) staff       (20)        0 2023-07-23 16:58:51.965773 Flask-SQL-Pro-3.4/flask_sql_pro/
+-rw-r--r--   0 kela       (501) staff       (20)     1843 2023-07-23 16:05:44.000000 Flask-SQL-Pro-3.4/flask_sql_pro/__init__.py
+-rw-r--r--   0 kela       (501) staff       (20)     8729 2023-07-23 16:58:25.000000 Flask-SQL-Pro-3.4/flask_sql_pro/db.py
+-rw-r--r--   0 kela       (501) staff       (20)     6020 2023-07-23 16:21:52.000000 Flask-SQL-Pro-3.4/flask_sql_pro/sql_loader.py
+-rw-r--r--   0 kela       (501) staff       (20)       38 2023-07-23 16:58:51.966378 Flask-SQL-Pro-3.4/setup.cfg
+-rw-r--r--   0 kela       (501) staff       (20)      816 2023-07-23 16:58:49.000000 Flask-SQL-Pro-3.4/setup.py
```

### Comparing `Flask-SQL-Pro-3.3/Flask_SQL_Pro.egg-info/PKG-INFO` & `Flask-SQL-Pro-3.4/Flask_SQL_Pro.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: Flask-SQL-Pro
-Version: 3.3
+Version: 3.4
 Summary: 基于Flask-SQLAlchemy, 抽离SQL语句, 使用Jinja2语法实现动态SQL, 支持上下文事务, 支持分页
 Author: miaokela
 Author-email: 2972799448@qq.com
 Maintainer: miaokela
 Maintainer-email: 2972799448@qq.com
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3.7
```

### Comparing `Flask-SQL-Pro-3.3/PKG-INFO` & `Flask-SQL-Pro-3.4/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: Flask-SQL-Pro
-Version: 3.3
+Version: 3.4
 Summary: 基于Flask-SQLAlchemy, 抽离SQL语句, 使用Jinja2语法实现动态SQL, 支持上下文事务, 支持分页
 Author: miaokela
 Author-email: 2972799448@qq.com
 Maintainer: miaokela
 Maintainer-email: 2972799448@qq.com
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3.7
```

### Comparing `Flask-SQL-Pro-3.3/README.rst` & `Flask-SQL-Pro-3.4/README.rst`

 * *Files identical despite different names*

### Comparing `Flask-SQL-Pro-3.3/flask_sql_pro/__init__.py` & `Flask-SQL-Pro-3.4/flask_sql_pro/__init__.py`

 * *Files identical despite different names*

### Comparing `Flask-SQL-Pro-3.3/flask_sql_pro/db.py` & `Flask-SQL-Pro-3.4/flask_sql_pro/db.py`

 * *Files 2% similar despite different names*

```diff
@@ -167,35 +167,29 @@
         :param bind:
         :param app:
         :param logic:
         :param tb_name: indicates the table name
         :param where: indicates the filter condition
         :return: indicates the number of deleted items
         """
+        sql = "DELETE FROM " + tb_name
         if logic:
-            sql = "UPDATE :table SET :flag=1"
-            params = {"table": tb_name, "flag": cls.logic_delete_flag}
-        else:
-            sql = "DELETE FROM :table"
-            params = {"table": tb_name}
-            
+            sql = "UPDATE %s SET %s=1" % (tb_name, cls.logic_delete_flag)
         sql = cls.set_where_phrase(sql, where)
         where = cls.fullfilled_data({}, where)
 
-        params.update(where)
-
         try:
             if app and bind:
                 bind = cls.db.get_engine(app, bind=bind)
-                result = cls.db.session.execute(sql, params, bind=bind)
+                result = cls.db.session.execute(sql, where, bind=bind)
             else:
-                result = cls.db.session.execute(sql, params)
+                result = cls.db.session.execute(sql, where)
             return result.rowcount
         except Exception as e:
-            cls.print("Failed to execute sql: < %s %s >! Cause: %s" % (sql, str(params), str(e)))
+            cls.print("Failed to execute sql: < %s %s >! Cause: %s" % (sql, str(where), str(e)))
             return None
 
     @classmethod
     def execute_sql(cls, sql_id, params=None, options: typing.Dict[str, str] = None, app=None, bind=None, return_obj=True):
         """
         General methods of dynamic sql
         :param return_obj: Returns Dict or DBData
```

### Comparing `Flask-SQL-Pro-3.3/flask_sql_pro/sql_loader.py` & `Flask-SQL-Pro-3.4/flask_sql_pro/sql_loader.py`

 * *Files identical despite different names*

### Comparing `Flask-SQL-Pro-3.3/setup.py` & `Flask-SQL-Pro-3.4/setup.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name='Flask-SQL-Pro',
-    version='3.3',
+    version='3.4',
     description='基于Flask-SQLAlchemy, 抽离SQL语句, 使用Jinja2语法实现动态SQL, 支持上下文事务, 支持分页',
     long_description=open('README.rst').read(),
     author='miaokela',
     author_email='2972799448@qq.com',
     maintainer='miaokela',
     maintainer_email='2972799448@qq.com',
     packages=find_packages(),
```

