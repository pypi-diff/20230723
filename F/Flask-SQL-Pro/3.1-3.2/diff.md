# Comparing `tmp/Flask-SQL-Pro-3.1.tar.gz` & `tmp/Flask-SQL-Pro-3.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "Flask-SQL-Pro-3.1.tar", last modified: Sun Jul 23 16:38:08 2023, max compression
+gzip compressed data, was "Flask-SQL-Pro-3.2.tar", last modified: Sun Jul 23 16:48:43 2023, max compression
```

## Comparing `Flask-SQL-Pro-3.1.tar` & `Flask-SQL-Pro-3.2.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxr-xr-x   0 kela       (501) staff       (20)        0 2023-07-23 16:38:08.301905 Flask-SQL-Pro-3.1/
-drwxr-xr-x   0 kela       (501) staff       (20)        0 2023-07-23 16:38:08.294306 Flask-SQL-Pro-3.1/Flask_SQL_Pro.egg-info/
--rw-r--r--   0 kela       (501) staff       (20)     8833 2023-07-23 16:38:08.000000 Flask-SQL-Pro-3.1/Flask_SQL_Pro.egg-info/PKG-INFO
--rw-r--r--   0 kela       (501) staff       (20)      277 2023-07-23 16:38:08.000000 Flask-SQL-Pro-3.1/Flask_SQL_Pro.egg-info/SOURCES.txt
--rw-r--r--   0 kela       (501) staff       (20)        1 2023-07-23 16:38:08.000000 Flask-SQL-Pro-3.1/Flask_SQL_Pro.egg-info/dependency_links.txt
--rw-r--r--   0 kela       (501) staff       (20)       30 2023-07-23 16:38:08.000000 Flask-SQL-Pro-3.1/Flask_SQL_Pro.egg-info/requires.txt
--rw-r--r--   0 kela       (501) staff       (20)       14 2023-07-23 16:38:08.000000 Flask-SQL-Pro-3.1/Flask_SQL_Pro.egg-info/top_level.txt
--rw-r--r--   0 kela       (501) staff       (20)     8833 2023-07-23 16:38:08.296663 Flask-SQL-Pro-3.1/PKG-INFO
--rw-r--r--   0 kela       (501) staff       (20)     8316 2023-07-23 16:37:58.000000 Flask-SQL-Pro-3.1/README.rst
-drwxr-xr-x   0 kela       (501) staff       (20)        0 2023-07-23 16:38:08.296307 Flask-SQL-Pro-3.1/flask_sql_pro/
--rw-r--r--   0 kela       (501) staff       (20)     1843 2023-07-23 16:05:44.000000 Flask-SQL-Pro-3.1/flask_sql_pro/__init__.py
--rw-r--r--   0 kela       (501) staff       (20)     8871 2023-07-23 16:34:23.000000 Flask-SQL-Pro-3.1/flask_sql_pro/db.py
--rw-r--r--   0 kela       (501) staff       (20)     6020 2023-07-23 16:21:52.000000 Flask-SQL-Pro-3.1/flask_sql_pro/sql_loader.py
--rw-r--r--   0 kela       (501) staff       (20)       38 2023-07-23 16:38:08.301973 Flask-SQL-Pro-3.1/setup.cfg
--rw-r--r--   0 kela       (501) staff       (20)      816 2023-07-23 16:35:18.000000 Flask-SQL-Pro-3.1/setup.py
+drwxr-xr-x   0 kela       (501) staff       (20)        0 2023-07-23 16:48:43.207086 Flask-SQL-Pro-3.2/
+drwxr-xr-x   0 kela       (501) staff       (20)        0 2023-07-23 16:48:43.206200 Flask-SQL-Pro-3.2/Flask_SQL_Pro.egg-info/
+-rw-r--r--   0 kela       (501) staff       (20)     8833 2023-07-23 16:48:43.000000 Flask-SQL-Pro-3.2/Flask_SQL_Pro.egg-info/PKG-INFO
+-rw-r--r--   0 kela       (501) staff       (20)      277 2023-07-23 16:48:43.000000 Flask-SQL-Pro-3.2/Flask_SQL_Pro.egg-info/SOURCES.txt
+-rw-r--r--   0 kela       (501) staff       (20)        1 2023-07-23 16:48:43.000000 Flask-SQL-Pro-3.2/Flask_SQL_Pro.egg-info/dependency_links.txt
+-rw-r--r--   0 kela       (501) staff       (20)       30 2023-07-23 16:48:43.000000 Flask-SQL-Pro-3.2/Flask_SQL_Pro.egg-info/requires.txt
+-rw-r--r--   0 kela       (501) staff       (20)       14 2023-07-23 16:48:43.000000 Flask-SQL-Pro-3.2/Flask_SQL_Pro.egg-info/top_level.txt
+-rw-r--r--   0 kela       (501) staff       (20)     8833 2023-07-23 16:48:43.206895 Flask-SQL-Pro-3.2/PKG-INFO
+-rw-r--r--   0 kela       (501) staff       (20)     8316 2023-07-23 16:37:58.000000 Flask-SQL-Pro-3.2/README.rst
+drwxr-xr-x   0 kela       (501) staff       (20)        0 2023-07-23 16:48:43.206637 Flask-SQL-Pro-3.2/flask_sql_pro/
+-rw-r--r--   0 kela       (501) staff       (20)     1843 2023-07-23 16:05:44.000000 Flask-SQL-Pro-3.2/flask_sql_pro/__init__.py
+-rw-r--r--   0 kela       (501) staff       (20)     8878 2023-07-23 16:48:22.000000 Flask-SQL-Pro-3.2/flask_sql_pro/db.py
+-rw-r--r--   0 kela       (501) staff       (20)     6020 2023-07-23 16:21:52.000000 Flask-SQL-Pro-3.2/flask_sql_pro/sql_loader.py
+-rw-r--r--   0 kela       (501) staff       (20)       38 2023-07-23 16:48:43.207136 Flask-SQL-Pro-3.2/setup.cfg
+-rw-r--r--   0 kela       (501) staff       (20)      816 2023-07-23 16:48:31.000000 Flask-SQL-Pro-3.2/setup.py
```

### Comparing `Flask-SQL-Pro-3.1/Flask_SQL_Pro.egg-info/PKG-INFO` & `Flask-SQL-Pro-3.2/Flask_SQL_Pro.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: Flask-SQL-Pro
-Version: 3.1
+Version: 3.2
 Summary: 基于Flask-SQLAlchemy, 抽离SQL语句, 使用Jinja2语法实现动态SQL, 支持上下文事务, 支持分页
 Author: miaokela
 Author-email: 2972799448@qq.com
 Maintainer: miaokela
 Maintainer-email: 2972799448@qq.com
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3.7
```

### Comparing `Flask-SQL-Pro-3.1/PKG-INFO` & `Flask-SQL-Pro-3.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: Flask-SQL-Pro
-Version: 3.1
+Version: 3.2
 Summary: 基于Flask-SQLAlchemy, 抽离SQL语句, 使用Jinja2语法实现动态SQL, 支持上下文事务, 支持分页
 Author: miaokela
 Author-email: 2972799448@qq.com
 Maintainer: miaokela
 Maintainer-email: 2972799448@qq.com
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3.7
```

### Comparing `Flask-SQL-Pro-3.1/README.rst` & `Flask-SQL-Pro-3.2/README.rst`

 * *Files identical despite different names*

### Comparing `Flask-SQL-Pro-3.1/flask_sql_pro/__init__.py` & `Flask-SQL-Pro-3.2/flask_sql_pro/__init__.py`

 * *Files identical despite different names*

### Comparing `Flask-SQL-Pro-3.1/flask_sql_pro/db.py` & `Flask-SQL-Pro-3.2/flask_sql_pro/db.py`

 * *Files 0% similar despite different names*

```diff
@@ -168,18 +168,18 @@
         :param app:
         :param logic:
         :param tb_name: indicates the table name
         :param where: indicates the filter condition
         :return: indicates the number of deleted items
         """
         if logic:
-            sql = "UPDATE :table SET :flag=1"
+            sql = "UPDATE `:table` SET `:flag`=1"
             params = {"table": tb_name, "flag": cls.logic_delete_flag}
         else:
-            sql = "DELETE FROM :table"
+            sql = "DELETE FROM `:table`"
             params = {"table": tb_name}
             
         sql = cls.set_where_phrase(sql, where)
         where = cls.fullfilled_data({}, where)
 
         params.update(where)
 
@@ -187,15 +187,15 @@
             if app and bind:
                 bind = cls.db.get_engine(app, bind=bind)
                 result = cls.db.session.execute(sql, params, bind=bind)
             else:
                 result = cls.db.session.execute(sql, params)
             return result.rowcount
         except Exception as e:
-            cls.print("Failed to execute sql: < %s %s >! Cause: %s" % (sql, str(where), str(e)))
+            cls.print("Failed to execute sql: < %s %s >! Cause: %s" % (sql, str(params), str(e)))
             return None
 
     @classmethod
     def execute_sql(cls, sql_id, params=None, options: typing.Dict[str, str] = None, app=None, bind=None, return_obj=True):
         """
         General methods of dynamic sql
         :param return_obj: Returns Dict or DBData
```

### Comparing `Flask-SQL-Pro-3.1/flask_sql_pro/sql_loader.py` & `Flask-SQL-Pro-3.2/flask_sql_pro/sql_loader.py`

 * *Files identical despite different names*

