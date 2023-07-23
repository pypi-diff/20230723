# Comparing `tmp/sqlx-batis-0.0.5.tar.gz` & `tmp/sqlx-batis-0.0.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist\sqlx-batis-0.0.5.tar", last modified: Sun Jul 23 10:23:54 2023, max compression
+gzip compressed data, was "dist\sqlx-batis-0.0.6.tar", last modified: Sun Jul 23 14:10:43 2023, max compression
```

## Comparing `sqlx-batis-0.0.5.tar` & `sqlx-batis-0.0.6.tar`

### file list

```diff
@@ -1,25 +1,25 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 10:23:54.000000 sqlx-batis-0.0.5/
--rw-rw-rw-   0        0        0     3430 2023-07-23 10:23:54.000000 sqlx-batis-0.0.5/PKG-INFO
--rw-rw-rw-   0        0        0     2948 2023-07-22 02:28:27.000000 sqlx-batis-0.0.5/README.rst
--rw-rw-rw-   0        0        0       42 2023-07-23 10:23:54.000000 sqlx-batis-0.0.5/setup.cfg
--rw-rw-rw-   0        0        0     1210 2023-07-23 10:23:51.000000 sqlx-batis-0.0.5/setup.py
-drwxrwxrwx   0        0        0        0 2023-07-23 10:23:54.000000 sqlx-batis-0.0.5/sqlxbatis/
--rw-rw-rw-   0        0        0      295 2023-07-22 19:43:35.000000 sqlx-batis-0.0.5/sqlxbatis/constant.py
--rw-rw-rw-   0        0        0     8225 2023-07-23 10:19:45.000000 sqlx-batis-0.0.5/sqlxbatis/db.py
--rw-rw-rw-   0        0        0     6418 2023-07-23 10:21:10.000000 sqlx-batis-0.0.5/sqlxbatis/dbx.py
--rw-rw-rw-   0        0        0      824 2023-07-22 19:35:47.000000 sqlx-batis-0.0.5/sqlxbatis/exec_support.py
--rw-rw-rw-   0        0        0     3875 2023-07-22 21:17:32.000000 sqlx-batis-0.0.5/sqlxbatis/log_support.py
--rw-rw-rw-   0        0        0    38575 2023-07-22 21:17:32.000000 sqlx-batis-0.0.5/sqlxbatis/orm.py
--rw-rw-rw-   0        0        0     2399 2023-07-22 21:14:39.000000 sqlx-batis-0.0.5/sqlxbatis/snowflake.py
--rw-rw-rw-   0        0        0     7056 2023-07-22 18:30:15.000000 sqlx-batis-0.0.5/sqlxbatis/sql_holder.py
--rw-rw-rw-   0        0        0     4120 2023-07-22 18:31:21.000000 sqlx-batis-0.0.5/sqlxbatis/sql_mapper.py
--rw-rw-rw-   0        0        0     1345 2023-07-22 20:40:59.000000 sqlx-batis-0.0.5/sqlxbatis/sql_support.py
--rw-rw-rw-   0        0        0      272 2023-07-22 19:39:25.000000 sqlx-batis-0.0.5/sqlxbatis/support.py
--rw-rw-rw-   0        0        0      177 2023-07-22 03:49:33.000000 sqlx-batis-0.0.5/sqlxbatis/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 10:23:54.000000 sqlx-batis-0.0.5/sqlx_batis.egg-info/
--rw-rw-rw-   0        0        0        1 2023-07-23 10:23:54.000000 sqlx-batis-0.0.5/sqlx_batis.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        2 2023-07-22 02:18:23.000000 sqlx-batis-0.0.5/sqlx_batis.egg-info/not-zip-safe
--rw-rw-rw-   0        0        0     3430 2023-07-23 10:23:54.000000 sqlx-batis-0.0.5/sqlx_batis.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0       31 2023-07-23 10:23:54.000000 sqlx-batis-0.0.5/sqlx_batis.egg-info/requires.txt
--rw-rw-rw-   0        0        0      483 2023-07-23 10:23:54.000000 sqlx-batis-0.0.5/sqlx_batis.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0       10 2023-07-23 10:23:54.000000 sqlx-batis-0.0.5/sqlx_batis.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 14:10:43.000000 sqlx-batis-0.0.6/
+-rw-rw-rw-   0        0        0     3427 2023-07-23 14:10:43.000000 sqlx-batis-0.0.6/PKG-INFO
+-rw-rw-rw-   0        0        0     2945 2023-07-23 14:10:39.000000 sqlx-batis-0.0.6/README.rst
+-rw-rw-rw-   0        0        0       42 2023-07-23 14:10:43.000000 sqlx-batis-0.0.6/setup.cfg
+-rw-rw-rw-   0        0        0     1209 2023-07-23 14:10:39.000000 sqlx-batis-0.0.6/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 14:10:43.000000 sqlx-batis-0.0.6/sqlbatis/
+-rw-rw-rw-   0        0        0      387 2023-07-23 13:58:19.000000 sqlx-batis-0.0.6/sqlbatis/constant.py
+-rw-rw-rw-   0        0        0     8258 2023-07-23 13:56:11.000000 sqlx-batis-0.0.6/sqlbatis/db.py
+-rw-rw-rw-   0        0        0     6472 2023-07-23 13:59:13.000000 sqlx-batis-0.0.6/sqlbatis/dbx.py
+-rw-rw-rw-   0        0        0      800 2023-07-23 14:05:59.000000 sqlx-batis-0.0.6/sqlbatis/exec_support.py
+-rw-rw-rw-   0        0        0     3875 2023-07-22 21:17:32.000000 sqlx-batis-0.0.6/sqlbatis/log_support.py
+-rw-rw-rw-   0        0        0    38549 2023-07-23 14:00:47.000000 sqlx-batis-0.0.6/sqlbatis/orm.py
+-rw-rw-rw-   0        0        0     2399 2023-07-22 21:14:39.000000 sqlx-batis-0.0.6/sqlbatis/snowflake.py
+-rw-rw-rw-   0        0        0     7056 2023-07-22 18:30:15.000000 sqlx-batis-0.0.6/sqlbatis/sql_holder.py
+-rw-rw-rw-   0        0        0     4120 2023-07-22 18:31:21.000000 sqlx-batis-0.0.6/sqlbatis/sql_mapper.py
+-rw-rw-rw-   0        0        0     1421 2023-07-23 14:00:47.000000 sqlx-batis-0.0.6/sqlbatis/sql_support.py
+-rw-rw-rw-   0        0        0      287 2023-07-23 13:34:34.000000 sqlx-batis-0.0.6/sqlbatis/support.py
+-rw-rw-rw-   0        0        0      154 2023-07-23 13:54:14.000000 sqlx-batis-0.0.6/sqlbatis/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 14:10:43.000000 sqlx-batis-0.0.6/sqlx_batis.egg-info/
+-rw-rw-rw-   0        0        0        1 2023-07-23 14:10:43.000000 sqlx-batis-0.0.6/sqlx_batis.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        2 2023-07-22 02:18:23.000000 sqlx-batis-0.0.6/sqlx_batis.egg-info/not-zip-safe
+-rw-rw-rw-   0        0        0     3427 2023-07-23 14:10:43.000000 sqlx-batis-0.0.6/sqlx_batis.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0       31 2023-07-23 14:10:43.000000 sqlx-batis-0.0.6/sqlx_batis.egg-info/requires.txt
+-rw-rw-rw-   0        0        0      471 2023-07-23 14:10:43.000000 sqlx-batis-0.0.6/sqlx_batis.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        9 2023-07-23 14:10:43.000000 sqlx-batis-0.0.6/sqlx_batis.egg-info/top_level.txt
```

### Comparing `sqlx-batis-0.0.5/PKG-INFO` & `sqlx-batis-0.0.6/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: sqlx-batis
-Version: 0.0.5
+Version: 0.0.6
 Summary: sqlx-batis is a sql executor for Python like MyBatis.
 Home-page: https://gitee.com/summry/sqlx-batis
 Author: summy
 Author-email: xiazhongbiao@126.com
 License: UNKNOWN
 Keywords: sql,MySQL,PostgreSQL,MyBatis,python
 Platform: UNKNOWN
@@ -39,17 +39,17 @@
    </mapper>
 
 Usage Sample
 ''''''''''''
 
 .. code:: python
 
-   from sqlxbatis import dbx, Engin
+   from sqlbatis import dbx, Engin
    from typing import List, Tuple, Mapping
-   from sqlxbatis.sql_mapper import mapper, sql
+   from sqlbatis.sql_mapper import mapper, sql
 
    @mapper(namespace='person')
    def select_all(): List
 
    @mapper(namespace='person')
    def select_by_name(name: str): List
 
@@ -95,15 +95,15 @@
        # (3, 'zhangsan', 15)
 
 Transaction
 '''''''''''
 
 .. code:: python
 
-   from sqlxbatis import with_transaction, transaction
+   from sqlbatis import with_transaction, transaction
 
    @with_transaction
    def test_transaction():
        insert_func(....)
        update_func(....)
```

### Comparing `sqlx-batis-0.0.5/README.rst` & `sqlx-batis-0.0.6/README.rst`

 * *Files 1% similar despite different names*

```diff
@@ -26,17 +26,17 @@
    </mapper>
 
 Usage Sample
 ''''''''''''
 
 .. code:: python
 
-   from sqlxbatis import dbx, Engin
+   from sqlbatis import dbx, Engin
    from typing import List, Tuple, Mapping
-   from sqlxbatis.sql_mapper import mapper, sql
+   from sqlbatis.sql_mapper import mapper, sql
 
    @mapper(namespace='person')
    def select_all(): List
 
    @mapper(namespace='person')
    def select_by_name(name: str): List
 
@@ -82,15 +82,15 @@
        # (3, 'zhangsan', 15)
 
 Transaction
 '''''''''''
 
 .. code:: python
 
-   from sqlxbatis import with_transaction, transaction
+   from sqlbatis import with_transaction, transaction
 
    @with_transaction
    def test_transaction():
        insert_func(....)
        update_func(....)
```

### Comparing `sqlx-batis-0.0.5/setup.py` & `sqlx-batis-0.0.6/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -9,23 +9,23 @@
     with open(os.path.join(here, rel_path), 'r', encoding='UTF-8') as fp:
         return fp.read()
 
 long_description = read("README.rst")
 
 setup(
     name='sqlx-batis',
-    packages=['sqlxbatis'],
+    packages=['sqlbatis'],
     description="sqlx-batis is a sql executor for Python like MyBatis.",
     long_description=long_description,
     long_description_content_type='text/markdown',
     install_requires=[
         'Jinja2>=2.7.0',
-        'sqlx-exec>=1.1.4',
+        'sqlx-exec>=1.1.5',
     ],
-    version='0.0.5',
+    version='0.0.6',
     url='https://gitee.com/summry/sqlx-batis',
     author='summy',
     author_email='xiazhongbiao@126.com',
     keywords=['sql', 'MySQL', 'PostgreSQL', 'MyBatis', 'python'],
     package_data={
         # include json and txt files
         '': ['*.rst', '*.dtd', '*.tpl'],
```

### Comparing `sqlx-batis-0.0.5/sqlxbatis/db.py` & `sqlx-batis-0.0.6/sqlbatis/db.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,21 +1,22 @@
 import sqlexec
 from . import sql_support, Engin
-from sqlexec.constant import MAPPER_PATH
-from .log_support import sql_log, page_log, insert_log, do_sql_log
+from .constant import MAPPER_PATH
+from .log_support import sql_log, page_log, do_sql_log
 
 # Don't remove. Import for not repetitive implementation
 from sqlexec import(insert, save, save_sql, batch_insert, batch_execute)
 
 
-def init_db(user='root', password='', database='test', host='127.0.0.1', port=3306, engin=Engin.MySQL, pool_size=2, show_sql=False, **kwargs):
+def init_db(connect=None, user='root', password='', database='test', host='127.0.0.1', port=3306, engin=Engin.MySQL, pool_size=0, show_sql=False, **kwargs):
     if MAPPER_PATH in kwargs:
         from .sql_holder import load_mapper
         load_mapper(kwargs.pop(MAPPER_PATH))
-    sqlexec.init_db(user=user, password=password, database=database, host=host, port=port, engin=engin, pool_size=pool_size, show_sql=show_sql, **kwargs)
+    sqlexec.init_db(connect=connect, user=user, password=password, database=database, host=host, port=port, engin=engin, pool_size=pool_size,
+                    show_sql=show_sql, **kwargs)
 
 
 # ----------------------------------------------------------Update function------------------------------------------------------------------
 def execute(sql: str, *args, **kwargs):
     """
     Execute SQL.
     sql: INSERT INTO user(name, age) VALUES(?, ?)  -->  args: ('张三', 20)
```

### Comparing `sqlx-batis-0.0.5/sqlxbatis/dbx.py` & `sqlx-batis-0.0.6/sqlbatis/dbx.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,20 +1,22 @@
 import sqlexec
 from .exec_support import do_save
 from . import db, Engin, sql_holder as holder
-from sqlexec.sql_support import get_batch_args
+from .sql_support import get_batch_args
 from .log_support import logger, sql_id_log, page_sql_id_log
 
 # Don't remove. Import for not repetitive implementation
 from sqlexec import(insert, batch_insert)
 
 
-def init_db(user='root', password='', database='test', host='127.0.0.1', port=3306, mapper_path='mapper', engin=Engin.MySQL, pool_size=2, show_sql=False, **kwargs):
+def init_db(connect=None, user='root', password='', database='test', host='127.0.0.1', port=3306, mapper_path='mapper', engin=Engin.MySQL,
+        pool_size=0, show_sql=False, **kwargs):
     holder.load_mapper(mapper_path)
-    sqlexec.init_db(user=user, password=password, database=database, host=host, port=port, engin=engin, pool_size=pool_size, show_sql=show_sql, **kwargs)
+    sqlexec.init_db(connect=connect, user=user, password=password, database=database, host=host, port=port, engin=engin, pool_size=pool_size,
+                    show_sql=show_sql, **kwargs)
 
 
 def save(sql_id: str, *args, **kwargs):
     """
     Execute insert SQL, return primary key.
     :return: Primary key
     """
```

### Comparing `sqlx-batis-0.0.5/sqlxbatis/exec_support.py` & `sqlx-batis-0.0.6/sqlbatis/exec_support.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,24 +1,23 @@
 import sqlexec
-from . import DBError
-from .support import SqlAction
+from . import DBEngin
 from .sql_holder import do_get_sql
-from sqlexec.sql_support import get_select_key
+from .support import SqlAction, DBError
 
 
 def do_save(sql_model, batch, param_names, *args, **kwargs):
     assert SqlAction.INSERT.value == sql_model.action, 'Only insert sql can return primary key.'
     sql, args = do_get_sql(sql_model, batch, param_names, *args, **kwargs)
     select_key = sql_model.select_key
     pk_seq = sql_model.pk_seq
     return  do_save0(select_key, pk_seq, sql, *args)
 
 
 def do_save0(select_key, pk_seq, sql, *args):
     if select_key:
         return sqlexec.save_sql(select_key, sql, *args)
 
-    select_key = get_select_key(pk_seq, None, sql)
+    select_key = DBEngin.get_select_key(pk_seq=pk_seq, sql=sql)
     if select_key:
         return sqlexec.save_sql(select_key, sql, *args)
 
-    raise DBError("Can not get select key.")
+    raise DBError("Can not get select key.")
```

### Comparing `sqlx-batis-0.0.5/sqlxbatis/log_support.py` & `sqlx-batis-0.0.6/sqlbatis/log_support.py`

 * *Files identical despite different names*

### Comparing `sqlx-batis-0.0.5/sqlxbatis/orm.py` & `sqlx-batis-0.0.6/sqlbatis/orm.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,18 +1,17 @@
 import sys
 import sqlexec
-from . import db, log_support, transaction
 from datetime import datetime
 from .snowflake import get_id
 from enum import Enum, IntEnum
 from functools import lru_cache
 from .sql_support import simple_sql
 from .support import DBError, NotFoundError
 from typing import Sequence, Union, List, Tuple
-from sqlexec.sql_support import get_column_sql, get_select_key
+from . import db, log_support, transaction, DBEngin
 from .constant import LIMIT_1, NO_LIMIT, DEFAULT_PK_FIELD, PK, PK_SEQ, TABLE, UPDATE_BY, UPDATE_TIME, DEL_FLAG, PK_STRATEGY, CACHE_SIZE
 
 
 class DelFlag(IntEnum):
     UN_DELETE = 0
     DELETED = 1
 
@@ -209,15 +208,15 @@
                 _id = kwargs[pk]
             else:
                 _id = get_id()
                 kwargs[pk] = _id
             sqlexec.insert(table, **kwargs)
         else:
             pk_seq = cls._get_pk_seq()
-            _id = sqlexec.save(get_select_key(pk_seq, table), table, **kwargs)
+            _id = sqlexec.save(DBEngin.get_select_key(pk_seq=pk_seq, table=table), table, **kwargs)
         return _id
 
     @classmethod
     def create(cls, **kwargs):
         """
         person = Person.create(name='张三', age=20)
         :return: Instance object
@@ -825,15 +824,15 @@
             raise ValueError("The type of the parameter 'limit' must be 'int' or tuple, list, and it length is 2.")
     else:
         return 'SELECT {} FROM {} {}'.format(fields, table, where)
 
 
 @lru_cache(maxsize=CACHE_SIZE)
 def _get_table_columns(table: str):
-    return sqlexec.get(get_column_sql(), table, LIMIT_1)
+    return sqlexec.get(DBEngin.get_column_sql(), table, LIMIT_1)
 
 
 def _get_condition_arg(k: str, v: object):
     if k.endswith("__eq"):
         return "{}=?".format(k[:-4]), v
     if k.endswith("__ne"):
         return "{}!=?".format(k[:-4]), v
```

### Comparing `sqlx-batis-0.0.5/sqlxbatis/snowflake.py` & `sqlx-batis-0.0.6/sqlbatis/snowflake.py`

 * *Files identical despite different names*

### Comparing `sqlx-batis-0.0.5/sqlxbatis/sql_holder.py` & `sqlx-batis-0.0.6/sqlbatis/sql_holder.py`

 * *Files identical despite different names*

### Comparing `sqlx-batis-0.0.5/sqlxbatis/sql_mapper.py` & `sqlx-batis-0.0.6/sqlbatis/sql_mapper.py`

 * *Files identical despite different names*

### Comparing `sqlx-batis-0.0.5/sqlxbatis/sql_support.py` & `sqlx-batis-0.0.6/sqlbatis/sql_support.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,13 +1,15 @@
 import re
 from jinja2 import Template
 from functools import lru_cache
 from .support import MapperError
 from .constant import LIMIT_1, DYNAMIC_REGEX, CACHE_SIZE
-from sqlexec.sql_support import require_limit, get_named_args, get_named_sql
+# Don't remove. Import for not repetitive implementation
+from sqlexec.sql_support import require_limit, get_named_args, get_named_sql, get_batch_args
+
 
 def simple_sql(sql: str, *args, **kwargs):
     return get_named_sql_args(sql, **kwargs) if kwargs else (sql, args)
 
 
 def dynamic_sql(sql: str, *args, **kwargs):
     sql_type = _get_sql_type(sql)
```

### Comparing `sqlx-batis-0.0.5/sqlx_batis.egg-info/PKG-INFO` & `sqlx-batis-0.0.6/sqlx_batis.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: sqlx-batis
-Version: 0.0.5
+Version: 0.0.6
 Summary: sqlx-batis is a sql executor for Python like MyBatis.
 Home-page: https://gitee.com/summry/sqlx-batis
 Author: summy
 Author-email: xiazhongbiao@126.com
 License: UNKNOWN
 Keywords: sql,MySQL,PostgreSQL,MyBatis,python
 Platform: UNKNOWN
@@ -39,17 +39,17 @@
    </mapper>
 
 Usage Sample
 ''''''''''''
 
 .. code:: python
 
-   from sqlxbatis import dbx, Engin
+   from sqlbatis import dbx, Engin
    from typing import List, Tuple, Mapping
-   from sqlxbatis.sql_mapper import mapper, sql
+   from sqlbatis.sql_mapper import mapper, sql
 
    @mapper(namespace='person')
    def select_all(): List
 
    @mapper(namespace='person')
    def select_by_name(name: str): List
 
@@ -95,15 +95,15 @@
        # (3, 'zhangsan', 15)
 
 Transaction
 '''''''''''
 
 .. code:: python
 
-   from sqlxbatis import with_transaction, transaction
+   from sqlbatis import with_transaction, transaction
 
    @with_transaction
    def test_transaction():
        insert_func(....)
        update_func(....)
```

