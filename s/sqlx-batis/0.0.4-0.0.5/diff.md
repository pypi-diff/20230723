# Comparing `tmp/sqlx-batis-0.0.4.tar.gz` & `tmp/sqlx-batis-0.0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist\sqlx-batis-0.0.4.tar", last modified: Sat Jul 22 18:34:09 2023, max compression
+gzip compressed data, was "dist\sqlx-batis-0.0.5.tar", last modified: Sun Jul 23 10:23:54 2023, max compression
```

## Comparing `sqlx-batis-0.0.4.tar` & `sqlx-batis-0.0.5.tar`

### file list

```diff
@@ -1,22 +1,25 @@
-drwxrwxrwx   0        0        0        0 2023-07-22 18:34:09.000000 sqlx-batis-0.0.4/
--rw-rw-rw-   0        0        0     3430 2023-07-22 18:34:09.000000 sqlx-batis-0.0.4/PKG-INFO
--rw-rw-rw-   0        0        0     2948 2023-07-22 02:28:27.000000 sqlx-batis-0.0.4/README.rst
--rw-rw-rw-   0        0        0       42 2023-07-22 18:34:09.000000 sqlx-batis-0.0.4/setup.cfg
--rw-rw-rw-   0        0        0     1210 2023-07-22 18:33:47.000000 sqlx-batis-0.0.4/setup.py
-drwxrwxrwx   0        0        0        0 2023-07-22 18:34:09.000000 sqlx-batis-0.0.4/sqlxbatis/
--rw-rw-rw-   0        0        0       64 2023-07-22 18:25:44.000000 sqlx-batis-0.0.4/sqlxbatis/constant.py
--rw-rw-rw-   0        0        0     7033 2023-07-22 18:13:12.000000 sqlx-batis-0.0.4/sqlxbatis/dbx.py
--rw-rw-rw-   0        0        0      818 2023-07-22 18:13:12.000000 sqlx-batis-0.0.4/sqlxbatis/exec_support.py
--rw-rw-rw-   0        0        0      488 2023-07-22 18:24:31.000000 sqlx-batis-0.0.4/sqlxbatis/log_support.py
--rw-rw-rw-   0        0        0     7056 2023-07-22 18:30:15.000000 sqlx-batis-0.0.4/sqlxbatis/sql_holder.py
--rw-rw-rw-   0        0        0     4120 2023-07-22 18:31:21.000000 sqlx-batis-0.0.4/sqlxbatis/sql_mapper.py
--rw-rw-rw-   0        0        0      616 2023-07-22 18:29:54.000000 sqlx-batis-0.0.4/sqlxbatis/sql_support.py
--rw-rw-rw-   0        0        0      227 2023-07-22 03:49:33.000000 sqlx-batis-0.0.4/sqlxbatis/support.py
--rw-rw-rw-   0        0        0      177 2023-07-22 03:49:33.000000 sqlx-batis-0.0.4/sqlxbatis/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-22 18:34:09.000000 sqlx-batis-0.0.4/sqlx_batis.egg-info/
--rw-rw-rw-   0        0        0        1 2023-07-22 18:34:09.000000 sqlx-batis-0.0.4/sqlx_batis.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        2 2023-07-22 02:18:23.000000 sqlx-batis-0.0.4/sqlx_batis.egg-info/not-zip-safe
--rw-rw-rw-   0        0        0     3430 2023-07-22 18:34:09.000000 sqlx-batis-0.0.4/sqlx_batis.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0       31 2023-07-22 18:34:09.000000 sqlx-batis-0.0.4/sqlx_batis.egg-info/requires.txt
--rw-rw-rw-   0        0        0      427 2023-07-22 18:34:09.000000 sqlx-batis-0.0.4/sqlx_batis.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0       10 2023-07-22 18:34:09.000000 sqlx-batis-0.0.4/sqlx_batis.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 10:23:54.000000 sqlx-batis-0.0.5/
+-rw-rw-rw-   0        0        0     3430 2023-07-23 10:23:54.000000 sqlx-batis-0.0.5/PKG-INFO
+-rw-rw-rw-   0        0        0     2948 2023-07-22 02:28:27.000000 sqlx-batis-0.0.5/README.rst
+-rw-rw-rw-   0        0        0       42 2023-07-23 10:23:54.000000 sqlx-batis-0.0.5/setup.cfg
+-rw-rw-rw-   0        0        0     1210 2023-07-23 10:23:51.000000 sqlx-batis-0.0.5/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 10:23:54.000000 sqlx-batis-0.0.5/sqlxbatis/
+-rw-rw-rw-   0        0        0      295 2023-07-22 19:43:35.000000 sqlx-batis-0.0.5/sqlxbatis/constant.py
+-rw-rw-rw-   0        0        0     8225 2023-07-23 10:19:45.000000 sqlx-batis-0.0.5/sqlxbatis/db.py
+-rw-rw-rw-   0        0        0     6418 2023-07-23 10:21:10.000000 sqlx-batis-0.0.5/sqlxbatis/dbx.py
+-rw-rw-rw-   0        0        0      824 2023-07-22 19:35:47.000000 sqlx-batis-0.0.5/sqlxbatis/exec_support.py
+-rw-rw-rw-   0        0        0     3875 2023-07-22 21:17:32.000000 sqlx-batis-0.0.5/sqlxbatis/log_support.py
+-rw-rw-rw-   0        0        0    38575 2023-07-22 21:17:32.000000 sqlx-batis-0.0.5/sqlxbatis/orm.py
+-rw-rw-rw-   0        0        0     2399 2023-07-22 21:14:39.000000 sqlx-batis-0.0.5/sqlxbatis/snowflake.py
+-rw-rw-rw-   0        0        0     7056 2023-07-22 18:30:15.000000 sqlx-batis-0.0.5/sqlxbatis/sql_holder.py
+-rw-rw-rw-   0        0        0     4120 2023-07-22 18:31:21.000000 sqlx-batis-0.0.5/sqlxbatis/sql_mapper.py
+-rw-rw-rw-   0        0        0     1345 2023-07-22 20:40:59.000000 sqlx-batis-0.0.5/sqlxbatis/sql_support.py
+-rw-rw-rw-   0        0        0      272 2023-07-22 19:39:25.000000 sqlx-batis-0.0.5/sqlxbatis/support.py
+-rw-rw-rw-   0        0        0      177 2023-07-22 03:49:33.000000 sqlx-batis-0.0.5/sqlxbatis/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 10:23:54.000000 sqlx-batis-0.0.5/sqlx_batis.egg-info/
+-rw-rw-rw-   0        0        0        1 2023-07-23 10:23:54.000000 sqlx-batis-0.0.5/sqlx_batis.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        2 2023-07-22 02:18:23.000000 sqlx-batis-0.0.5/sqlx_batis.egg-info/not-zip-safe
+-rw-rw-rw-   0        0        0     3430 2023-07-23 10:23:54.000000 sqlx-batis-0.0.5/sqlx_batis.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0       31 2023-07-23 10:23:54.000000 sqlx-batis-0.0.5/sqlx_batis.egg-info/requires.txt
+-rw-rw-rw-   0        0        0      483 2023-07-23 10:23:54.000000 sqlx-batis-0.0.5/sqlx_batis.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0       10 2023-07-23 10:23:54.000000 sqlx-batis-0.0.5/sqlx_batis.egg-info/top_level.txt
```

### Comparing `sqlx-batis-0.0.4/PKG-INFO` & `sqlx-batis-0.0.5/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: sqlx-batis
-Version: 0.0.4
+Version: 0.0.5
 Summary: sqlx-batis is a sql executor for Python like MyBatis.
 Home-page: https://gitee.com/summry/sqlx-batis
 Author: summy
 Author-email: xiazhongbiao@126.com
 License: UNKNOWN
 Keywords: sql,MySQL,PostgreSQL,MyBatis,python
 Platform: UNKNOWN
```

### Comparing `sqlx-batis-0.0.4/README.rst` & `sqlx-batis-0.0.5/README.rst`

 * *Files identical despite different names*

### Comparing `sqlx-batis-0.0.4/setup.py` & `sqlx-batis-0.0.5/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -15,17 +15,17 @@
     name='sqlx-batis',
     packages=['sqlxbatis'],
     description="sqlx-batis is a sql executor for Python like MyBatis.",
     long_description=long_description,
     long_description_content_type='text/markdown',
     install_requires=[
         'Jinja2>=2.7.0',
-        'sqlx-exec>=1.1.3',
+        'sqlx-exec>=1.1.4',
     ],
-    version='0.0.4',
+    version='0.0.5',
     url='https://gitee.com/summry/sqlx-batis',
     author='summy',
     author_email='xiazhongbiao@126.com',
     keywords=['sql', 'MySQL', 'PostgreSQL', 'MyBatis', 'python'],
     package_data={
         # include json and txt files
         '': ['*.rst', '*.dtd', '*.tpl'],
```

### Comparing `sqlx-batis-0.0.4/sqlxbatis/dbx.py` & `sqlx-batis-0.0.5/sqlxbatis/dbx.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,28 +1,20 @@
 import sqlexec
 from .exec_support import do_save
-from . import Engin, sql_holder as holder
-from .sql_support import limit_one_sql_args
+from . import db, Engin, sql_holder as holder
 from sqlexec.sql_support import get_batch_args
 from .log_support import logger, sql_id_log, page_sql_id_log
 
-
-def init_db(user='root', password='', database='test', host='127.0.0.1', port=3306, show_sql=False, mapper_path='mapper', engin=Engin.MySQL, **kwargs):
-    holder.load_mapper(mapper_path)
-    sqlexec.init_db(user=user, password=password, database=database, host=host, port=port, show_sql=show_sql, engin=engin, **kwargs)
+# Don't remove. Import for not repetitive implementation
+from sqlexec import(insert, batch_insert)
 
 
-def insert(table: str, **kwargs):
-    """
-    Insert data into table, return effect rowcount.
-    :param table: table name
-    :param kwargs: {'name': '张三', 'age': 20}
-    return: Effect rowcount
-    """
-    return sqlexec.insert(table, **kwargs)
+def init_db(user='root', password='', database='test', host='127.0.0.1', port=3306, mapper_path='mapper', engin=Engin.MySQL, pool_size=2, show_sql=False, **kwargs):
+    holder.load_mapper(mapper_path)
+    sqlexec.init_db(user=user, password=password, database=database, host=host, port=port, engin=engin, pool_size=pool_size, show_sql=show_sql, **kwargs)
 
 
 def save(sql_id: str, *args, **kwargs):
     """
     Execute insert SQL, return primary key.
     :return: Primary key
     """
@@ -38,24 +30,14 @@
          INSERT INTO person(name, age) VALUES(:name,:age)  -->  kwargs: {'name': '张三', 'age': 20}
     """
     sql_id_log('dbx.execute', sql_id, *args, **kwargs)
     sql, args = holder.get_sql(sql_id, *args, **kwargs)
     return sqlexec.execute(sql, *args)
 
 
-def batch_insert(table: str, *args):
-    """
-    Batch insert
-    :param table: table name
-    :param args: All number must have same key. [{'name': '张三', 'age': 20}, {'name': '李四', 'age': 28}]
-    :return: Effect row count
-    """
-    return sqlexec.batch_insert(table, *args)
-
-
 def batch_execute(sql_id: str, *args):
     """
     Batch execute
     sql: INSERT INTO person(name, age) VALUES(?, ?)  -->  args: [('张三', 20), ('李四', 28)]
          INSERT INTO person(name, age) VALUES(:name,:age)  -->  args: [{'name': '张三', 'age': 20}, {'name': '李四', 'age': 28}]
     :return: Effect row count
     """
@@ -72,16 +54,15 @@
     Execute select SQL and expected one int and only one int result. Automatically add 'limit ?' behind the sql statement if not.
     MultiColumnsError: Expect only one column.
     sql: SELECT count(1) FROM person WHERE name=? and age=? limit 1  -->  args: ('张三', 20)
          SELECT count(1) FROM person WHERE name=:name and age=:age limit 1  -->  kwargs: ('张三', 20) --> kwargs: {'name': '张三', 'age': 20}
     """
     sql_id_log('get', sql_id, *args, **kwargs)
     sql, args = holder.get_sql(sql_id, *args, **kwargs)
-    sql, args = limit_one_sql_args(sql, *args)
-    return sqlexec.get(sql, *args)
+    return db.do_get(sql, *args)
 
 
 def query(sql_id: str, *args, **kwargs):
     """
     Execute select SQL and return list or empty list if no result.
     sql: SELECT * FROM person WHERE name=? and age=?  -->  args: ('张三', 20)
          SELECT * FROM person WHERE name=:name and age=:age  -->  kwargs: ('张三', 20) --> kwargs: {'name': '张三', 'age': 20}
@@ -97,16 +78,15 @@
     If no result found, return None.
     If multiple results found, the first one returned.
     sql: SELECT * FROM person WHERE name=? and age=? limit 1 -->  args: ('张三', 20)
          SELECT * FROM person WHERE name=:name and age=:age limit 1  -->  kwargs: ('张三', 20) --> kwargs: {'name': '张三', 'age': 20}
     """
     sql_id_log('query_one', sql_id, *args, **kwargs)
     sql, args = holder.get_sql(sql_id, *args, **kwargs)
-    sql, args = limit_one_sql_args(sql, *args)
-    return sqlexec.query_one(sql, *args)
+    return db.do_query_one(sql, *args)
 
 
 def select(sql_id: str, *args, **kwargs):
     """
     Execute select SQL and return list(tuple) or empty list if no result.
     sql: SELECT * FROM person WHERE name=? and age=?  -->  args: ('张三', 20)
          SELECT * FROM person WHERE name=:name and age=:age   -->  kwargs: ('张三', 20) --> kwargs: {'name': '张三', 'age': 20}
@@ -122,16 +102,15 @@
     If no result found, return None.
     If multiple results found, the first one returned.
     sql: SELECT * FROM person WHERE name=? and age=? limit 1  -->  args: ('张三', 20)
          SELECT * FROM person WHERE name=:name and age=:age limit 1  -->  kwargs: ('张三', 20) --> kwargs: {'name': '张三', 'age': 20}
     """
     sql_id_log('select_one', sql_id, *args, **kwargs)
     sql, args = holder.get_sql(sql_id, *args, **kwargs)
-    sql, args = limit_one_sql_args(sql, *args)
-    return sqlexec.select_one(sql, *args)
+    return db.do_select_one(sql, *args)
 
 
 def query_page(sql_id: str, page_num=1, page_size=10, *args, **kwargs):
     """
     Execute select SQL and return list or empty list if no result. Automatically add 'limit ?,?' after sql statement if not.
     sql: SELECT * FROM person WHERE name=? and age=?  -->  args: ('张三', 20)
          SELECT * FROM person WHERE name=:name and age=:age  -->  kwargs: ('张三', 20) --> kwargs: {'name': '张三', 'age': 20}
```

### Comparing `sqlx-batis-0.0.4/sqlxbatis/exec_support.py` & `sqlx-batis-0.0.5/sqlxbatis/exec_support.py`

 * *Files 1% similar despite different names*

```diff
@@ -13,12 +13,12 @@
     return  do_save0(select_key, pk_seq, sql, *args)
 
 
 def do_save0(select_key, pk_seq, sql, *args):
     if select_key:
         return sqlexec.save_sql(select_key, sql, *args)
 
-    select_key = get_select_key(pk_seq, sql)
+    select_key = get_select_key(pk_seq, None, sql)
     if select_key:
         return sqlexec.save_sql(select_key, sql, *args)
 
     raise DBError("Can not get select key.")
```

### Comparing `sqlx-batis-0.0.4/sqlxbatis/sql_holder.py` & `sqlx-batis-0.0.5/sqlxbatis/sql_holder.py`

 * *Files identical despite different names*

### Comparing `sqlx-batis-0.0.4/sqlxbatis/sql_mapper.py` & `sqlx-batis-0.0.5/sqlxbatis/sql_mapper.py`

 * *Files identical despite different names*

### Comparing `sqlx-batis-0.0.4/sqlx_batis.egg-info/PKG-INFO` & `sqlx-batis-0.0.5/sqlx_batis.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: sqlx-batis
-Version: 0.0.4
+Version: 0.0.5
 Summary: sqlx-batis is a sql executor for Python like MyBatis.
 Home-page: https://gitee.com/summry/sqlx-batis
 Author: summy
 Author-email: xiazhongbiao@126.com
 License: UNKNOWN
 Keywords: sql,MySQL,PostgreSQL,MyBatis,python
 Platform: UNKNOWN
```

