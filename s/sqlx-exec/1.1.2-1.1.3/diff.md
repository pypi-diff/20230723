# Comparing `tmp/sqlx-exec-1.1.2.tar.gz` & `tmp/sqlx-exec-1.1.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist\sqlx-exec-1.1.2.tar", last modified: Sat Jul 22 02:28:53 2023, max compression
+gzip compressed data, was "dist\sqlx-exec-1.1.3.tar", last modified: Sat Jul 22 18:33:54 2023, max compression
```

## Comparing `sqlx-exec-1.1.2.tar` & `sqlx-exec-1.1.3.tar`

### file list

```diff
@@ -1,20 +1,21 @@
-drwxrwxrwx   0        0        0        0 2023-07-22 02:28:53.000000 sqlx-exec-1.1.2/
--rw-rw-rw-   0        0        0    11558 2023-07-21 06:24:32.000000 sqlx-exec-1.1.2/LICENSE
--rw-rw-rw-   0        0        0     2667 2023-07-22 02:28:53.000000 sqlx-exec-1.1.2/PKG-INFO
--rw-rw-rw-   0        0        0     2159 2023-07-22 02:28:05.000000 sqlx-exec-1.1.2/README.rst
--rw-rw-rw-   0        0        0       42 2023-07-22 02:28:53.000000 sqlx-exec-1.1.2/setup.cfg
--rw-rw-rw-   0        0        0     1161 2023-07-22 02:28:48.000000 sqlx-exec-1.1.2/setup.py
-drwxrwxrwx   0        0        0        0 2023-07-22 02:28:53.000000 sqlx-exec-1.1.2/sqlexec/
--rw-rw-rw-   0        0        0     2457 2023-07-21 22:49:57.000000 sqlx-exec-1.1.2/sqlexec/engin.py
--rw-rw-rw-   0        0        0    10884 2023-07-21 23:56:22.000000 sqlx-exec-1.1.2/sqlexec/exec.py
--rw-rw-rw-   0        0        0     1030 2023-07-21 22:35:47.000000 sqlx-exec-1.1.2/sqlexec/log_support.py
--rw-rw-rw-   0        0        0     2786 2023-07-21 16:37:12.000000 sqlx-exec-1.1.2/sqlexec/pooling.py
--rw-rw-rw-   0        0        0     2419 2023-07-22 02:04:44.000000 sqlx-exec-1.1.2/sqlexec/sql_support.py
--rw-rw-rw-   0        0        0     4275 2023-07-21 16:54:46.000000 sqlx-exec-1.1.2/sqlexec/support.py
--rw-rw-rw-   0        0        0      364 2023-07-22 02:04:16.000000 sqlx-exec-1.1.2/sqlexec/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-22 02:28:53.000000 sqlx-exec-1.1.2/sqlx_exec.egg-info/
--rw-rw-rw-   0        0        0        1 2023-07-22 02:28:53.000000 sqlx-exec-1.1.2/sqlx_exec.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        2 2023-07-21 08:56:11.000000 sqlx-exec-1.1.2/sqlx_exec.egg-info/not-zip-safe
--rw-rw-rw-   0        0        0     2667 2023-07-22 02:28:53.000000 sqlx-exec-1.1.2/sqlx_exec.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      328 2023-07-22 02:28:53.000000 sqlx-exec-1.1.2/sqlx_exec.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        8 2023-07-22 02:28:53.000000 sqlx-exec-1.1.2/sqlx_exec.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-22 18:33:54.000000 sqlx-exec-1.1.3/
+-rw-rw-rw-   0        0        0    11558 2023-07-21 06:24:32.000000 sqlx-exec-1.1.3/LICENSE
+-rw-rw-rw-   0        0        0     2667 2023-07-22 18:33:54.000000 sqlx-exec-1.1.3/PKG-INFO
+-rw-rw-rw-   0        0        0     2159 2023-07-22 02:28:05.000000 sqlx-exec-1.1.3/README.rst
+-rw-rw-rw-   0        0        0       42 2023-07-22 18:33:54.000000 sqlx-exec-1.1.3/setup.cfg
+-rw-rw-rw-   0        0        0     1161 2023-07-22 18:33:22.000000 sqlx-exec-1.1.3/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-22 18:33:54.000000 sqlx-exec-1.1.3/sqlexec/
+-rw-rw-rw-   0        0        0       79 2023-07-22 18:18:06.000000 sqlx-exec-1.1.3/sqlexec/constant.py
+-rw-rw-rw-   0        0        0     3011 2023-07-22 18:22:09.000000 sqlx-exec-1.1.3/sqlexec/engin.py
+-rw-rw-rw-   0        0        0    10960 2023-07-22 18:15:37.000000 sqlx-exec-1.1.3/sqlexec/exec.py
+-rw-rw-rw-   0        0        0     1030 2023-07-21 22:35:47.000000 sqlx-exec-1.1.3/sqlexec/log_support.py
+-rw-rw-rw-   0        0        0     2761 2023-07-22 17:16:08.000000 sqlx-exec-1.1.3/sqlexec/pooling.py
+-rw-rw-rw-   0        0        0     2133 2023-07-22 18:28:23.000000 sqlx-exec-1.1.3/sqlexec/sql_support.py
+-rw-rw-rw-   0        0        0     4275 2023-07-21 16:54:46.000000 sqlx-exec-1.1.3/sqlexec/support.py
+-rw-rw-rw-   0        0        0      361 2023-07-22 17:31:16.000000 sqlx-exec-1.1.3/sqlexec/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-22 18:33:54.000000 sqlx-exec-1.1.3/sqlx_exec.egg-info/
+-rw-rw-rw-   0        0        0        1 2023-07-22 18:33:54.000000 sqlx-exec-1.1.3/sqlx_exec.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        2 2023-07-21 08:56:11.000000 sqlx-exec-1.1.3/sqlx_exec.egg-info/not-zip-safe
+-rw-rw-rw-   0        0        0     2667 2023-07-22 18:33:54.000000 sqlx-exec-1.1.3/sqlx_exec.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      348 2023-07-22 18:33:54.000000 sqlx-exec-1.1.3/sqlx_exec.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        8 2023-07-22 18:33:54.000000 sqlx-exec-1.1.3/sqlx_exec.egg-info/top_level.txt
```

### Comparing `sqlx-exec-1.1.2/LICENSE` & `sqlx-exec-1.1.3/LICENSE`

 * *Files identical despite different names*

### Comparing `sqlx-exec-1.1.2/PKG-INFO` & `sqlx-exec-1.1.3/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: sqlx-exec
-Version: 1.1.2
+Version: 1.1.3
 Summary: sqlx-exec is a simple sql executor for Python, it help you auto manage database connection and transaction.
 Home-page: https://gitee.com/summry/sql-exec
 Author: summy
 Author-email: xiazhongbiao@126.com
 License: UNKNOWN
 Keywords: sql,MySQL,PostgreSQL,python
 Platform: UNKNOWN
```

### Comparing `sqlx-exec-1.1.2/README.rst` & `sqlx-exec-1.1.3/README.rst`

 * *Files identical despite different names*

### Comparing `sqlx-exec-1.1.2/setup.py` & `sqlx-exec-1.1.3/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -13,15 +13,15 @@
 
 setup(
     name='sqlx-exec',
     packages=['sqlexec'],
     description="sqlx-exec is a simple sql executor for Python, it help you auto manage database connection and transaction.",
     long_description=long_description,
     long_description_content_type='text/markdown',
-    version='1.1.2',
+    version='1.1.3',
     url='https://gitee.com/summry/sql-exec',
     author='summy',
     author_email='xiazhongbiao@126.com',
     keywords=['sql', 'MySQL', 'PostgreSQL', 'python'],
     package_data={
         # include json and txt files
         '': ['*.rst', '*.dtd', '*.tpl'],
```

### Comparing `sqlx-exec-1.1.2/sqlexec/engin.py` & `sqlx-exec-1.1.3/sqlexec/engin.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,40 +1,48 @@
+import re
 from enum import Enum
 from typing import Sequence
 from functools import lru_cache
+from .log_support import logger
+from .constant import CACHE_SIZE
 
-CACHE_SIZE = 256
+
+def create_sql_engin(engin, show_sql):
+    if engin == Engin.MySQL:
+        return MySqlEngin(show_sql)
+    elif engin == Engin.PostgreSQL:
+        return PostgresEngin(show_sql)
+    raise
 
 
 class Engin(Enum):
     MySQL = 'MySQL'
     PostgreSQL = 'PostgreSQL'
 
 
 class SqlEngin:
-    def __init__(self, logger, show_sql):
-        self.logger = logger
+    def __init__(self, show_sql):
         self.show_sql = show_sql
 
     def before_execute(self, function: str, sql: str, *args):
         if self.show_sql:
-            self.logger.info("Exec func 'sqlexec.%s' \n\tSQL: %s \n\tARGS: %s" % (function, sql, args))
+            logger.info("Exec func 'sqlexec.%s' \n\tSQL: %s \n\tARGS: %s" % (function, sql, args))
         return sql.replace('?', '%s')
 
     @staticmethod
     @lru_cache(maxsize=CACHE_SIZE)
     def create_insert_sql(table: str, cols: Sequence[str]):
         columns, placeholders = zip(*[('{}'.format(col), '?') for col in cols])
         return 'INSERT INTO {}({}) VALUES({})'.format(table, ', '.join(columns), ','.join(placeholders))
 
 
 class MySqlEngin(SqlEngin):
 
-    def __init__(self, logger, show_sql):
-        super().__init__(logger, show_sql)
+    def __init__(self, show_sql):
+        super().__init__(show_sql)
 
     @staticmethod
     @lru_cache(maxsize=CACHE_SIZE)
     def create_insert_sql(table: str, cols: Sequence[str]):
         columns, placeholders = zip(*[('`{}`'.format(col), '?') for col in cols])
         return 'INSERT INTO `{}`({}) VALUES({})'.format(table, ', '.join(columns), ','.join(placeholders))
 
@@ -42,33 +50,43 @@
     def page_sql_args(require_limit, sql: str, start, page_size, *args):
         if require_limit(sql):
             sql = '{} limit ?, ?'.format(sql)
         args = [*args, start, page_size]
         return sql, args
 
     @staticmethod
-    def get_select_key(*args):
+    def get_select_key(*args, **kwargs):
         return "SELECT LAST_INSERT_ID()"
 
 
 class PostgresEngin(SqlEngin):
 
-    def __init__(self, logger, show_sql):
-        super().__init__(logger, show_sql)
+    def __init__(self, show_sql):
+        super().__init__(show_sql)
 
     def before_execute(self, function: str, sql: str, *args):
         if self.show_sql:
-            self.logger.info("Exec func 'sqlexec.%s' \n\tSQL: %s \n\tARGS: %s" % (function, sql, args))
+            logger.info("Exec func 'sqlexec.%s' \n\tSQL: %s \n\tARGS: %s" % (function, sql, args))
         if '%' in sql and 'like' in sql.lower():
             sql = sql.replace('%', '%%').replace('%%%%', '%%')
         return sql.replace('?', '%s')
 
     @staticmethod
     def page_sql_args(require_limit, sql: str, start, page_size, *args):
         if require_limit(sql):
             sql = '{} LIMIT ? OFFSET ?'.format(sql)
         args = [*args, page_size, start]
         return sql, args
 
     @staticmethod
-    def get_select_key(pk_seq, *args):
-        return  "SELECT currval('{}')".format(pk_seq)
+    def get_select_key(pk_seq: str, sql: str, *args, **kwargs):
+        if not pk_seq:
+            pk_seq = _get_pk_seq_from_sql(sql)
+        return f"SELECT currval('{pk_seq}')"
+
+
+@lru_cache(maxsize=CACHE_SIZE)
+def _get_pk_seq_from_sql(sql: str):
+    table = re.search('(?<=into )\w+', sql, re.I)
+    pk_seq = "{}_id_seq".format(table.group())
+    logger.warning("'pk_seq' is None, will use default '{}' from sql.".format(pk_seq))
+    return pk_seq
```

### Comparing `sqlx-exec-1.1.2/sqlexec/exec.py` & `sqlx-exec-1.1.3/sqlexec/exec.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,66 +1,73 @@
 import functools
-from . import sql_support
 from .engin import Engin
+from . import sql_support
+from .constant import MAPPER_PATH
 from .log_support import logger, insert_log, save_log, get_log, page_log
 from .support import DBCtx, ConnectionCtx, Dict, MultiColumnsError, TransactionCtx, try_commit, DBError, DB_LOCK
 
 _DB_CTX = None
 
 
-def init_engin(connect=None, user='root', password='', database='test', host='127.0.0.1', port=3306, engin=Engin.MySQL, pool_size=1, show_sql=False, **kwargs):
+def init_db(connect=None, user='root', password='', database='test', host='127.0.0.1', port=3306, engin=Engin.MySQL, pool_size=1, show_sql=False, **kwargs):
     sql_support.set_config(engin, show_sql)
+    if MAPPER_PATH in kwargs:
+        del kwargs[MAPPER_PATH]
+
     if 'debug' in kwargs:
         if kwargs.pop('debug'):
             from logging import DEBUG
             logger.setLevel(DEBUG)
 
     if connect:
         import types
         assert isinstance(connect, types.FunctionType), '`connect` must be a function, you can use like `connect=lambda: connect(**kwargs)`.'
-        _init_engin(connect, engin, pool_size, pool_size)
+        _init_db(connect, engin, pool_size, pool_size)
     else:
-        _import_init_engin(user, password, database, host, port, engin, pool_size, **kwargs)
+        kwargs['user'] = user
+        kwargs['password'] = password
+        kwargs['database'] = database
+        kwargs['host'] = host
+        kwargs['port'] = port
+        _import_init(engin, pool_size, **kwargs)
 
 
-def _import_init_engin(user, password, database, host, port, engin, pool_size, **kwargs):
+def _import_init(engin, pool_size, **kwargs):
     prepared = False
-    kwargs['user'] = user
-    kwargs['password'] = password
-    kwargs['database'] = database
-    kwargs['host'] = host
-    kwargs['port'] = port
     real_size = pool_size
+
     if engin == Engin.MySQL:
         try:
             from mysql.connector import connect
             prepared = True
             if pool_size > 0:
                 kwargs['pool_size'] = pool_size
                 if 'pool_name' not in kwargs:
-                    kwargs['pool_name'] = "{}_pool".format(database)
+                    kwargs['pool_name'] = "{}_pool".format(kwargs.get('database'))
                 pool_size = 0
         except ImportError:
             from pymysql import connect
     elif engin == Engin.PostgreSQL:
         from psycopg2 import connect
     else:
         raise DBError('Engin is invalid: %s', engin)
-    _init_engin(lambda: connect(**kwargs), engin, pool_size, real_size, prepared)
+
+    _init_db(lambda: connect(**kwargs), engin, pool_size, real_size, prepared)
 
 
-def _init_engin(connect, engin, pool_size, real_size, prepared=False):
+def _init_db(connect, engin, pool_size, real_size, prepared=False):
     global _DB_CTX
     with DB_LOCK:
         if _DB_CTX is not None:
             raise DBError('DB is already initialized.')
-
-        from . import pooling
-        _DB_CTX = DBCtx(connect=pooling.get_connect(connect, pool_size) if pool_size>=1 else connect, pool_size=real_size, prepared=prepared)
-        logger.info('Init db engine <%s> of %s with pool size: %d.' % (hex(id(_DB_CTX)), engin.value, real_size))
+        if pool_size >= 1:
+            from .pooling import pooled_connect
+            connect = pooled_connect(connect, pool_size)
+        _DB_CTX = DBCtx(connect=connect, pool_size=real_size, prepared=prepared)
+    logger.info('Init db engine <%s> of %s with pool size: %d.' % (hex(id(_DB_CTX)), engin.value, real_size))
 
 
 def connection():
     """
     Return _ConnectionCtx object that can be used by 'with' statement:
     with connection():
         pass
```

### Comparing `sqlx-exec-1.1.2/sqlexec/log_support.py` & `sqlx-exec-1.1.3/sqlexec/log_support.py`

 * *Files identical despite different names*

### Comparing `sqlx-exec-1.1.2/sqlexec/pooling.py` & `sqlx-exec-1.1.3/sqlexec/pooling.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 from queue import Queue
 from .support import DB_LOCK
 
 MAX_POOL_SIZE = 32
 _CONNECTION_POOL = None
 
-def get_connect(conn_func, pool_size):
+def pooled_connect(conn_func, pool_size):
     global _CONNECTION_POOL
     assert 1 <= pool_size <= MAX_POOL_SIZE, 'pool_size should be higher or equal to 1 and lower or equal to {}'.format(MAX_POOL_SIZE)
 
     if _CONNECTION_POOL is None:
         with DB_LOCK:
             if _CONNECTION_POOL is None:
                 _CONNECTION_POOL = ConnectionPool(conn_func, pool_size)
@@ -17,33 +17,33 @@
 
 
 class ConnectionPool:
 
     def __init__(self, conn_func, pool_size):
         self.connect = conn_func
         self.pool_size = pool_size
-        self.pool_queue = Queue(pool_size)
+        self._pool_queue = Queue(pool_size)
 
         for _ in range(pool_size):
-            self.add_connection()
+            self._add_connection()
 
-    def add_connection(self, conn=None):
-        if conn:
-            self.pool_queue.put(conn, block=False)
-        else:
-            self.pool_queue.put(self.connect(), block=False)
+    def add_connection(self, conn):
+        self._pool_queue.put(conn, block=False)
+
+    def _add_connection(self):
+        self.add_connection(self.connect())
 
     def get_connection(self):
-        conn = self.pool_queue.get(timeout=1)
+        conn = self._pool_queue.get(timeout=1)
         return PooledConnection(self, conn)
 
     def close_all(self):
         for _ in  range(self.pool_size):
             try:
-                self.pool_queue.get().close()
+                self._pool_queue.get().close()
             except:
                 pass
 
 
 class PooledConnection(object):
     """Class holding a Connection in a pool
 
@@ -59,15 +59,15 @@
 
         The pool argument must be an instance of ConnectionPoll. conn
         if an instance of Connection.
         """
         if not isinstance(pool, ConnectionPool):
             raise AttributeError(
                 "pool should be a ConnectionPool")
-        self._cnx_pool = pool
+        self._pool = pool
         self.conn = conn
 
     def __enter__(self):
         return self
 
     def __exit__(self, exc_type, exc_value, traceback):
         self.close()
@@ -82,9 +82,9 @@
         The close() method does not close the connection with the
         MySQL server. The connection is added back to the pool so it
         can be reused.
 
         When the pool is configured to reset the session, the session
         state will be cleared by re-authenticating the user.
         """
-        self._cnx_pool.add_connection(self.conn)
+        self._pool.add_connection(self.conn)
         self.conn = None
```

### Comparing `sqlx-exec-1.1.2/sqlexec/sql_support.py` & `sqlx-exec-1.1.3/sqlexec/sql_support.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,16 +1,14 @@
 import re
 from typing import Sequence
-from .log_support import logger
 from functools import lru_cache
-from .engin import Engin, MySqlEngin, PostgresEngin
+from .engin import create_sql_engin
+from .constant import CACHE_SIZE, NAMED_REGEX
 
-CACHE_SIZE = 256
-NAMED_REGEX = r':[\w|\d]*'
-_ENGIN = None
+# _ENGIN = None
 _SQL_ENGIN = None
 before_execute = None
 
 
 def insert_sql_args(table: str, **kwargs):
     cols, args = zip(*kwargs.items())
     sql = _SQL_ENGIN.create_insert_sql(table, cols)
@@ -32,19 +30,14 @@
 def batch_named_sql_args(sql: str, *args):
     args = get_batch_args(*args)
     args = [get_named_args(sql, **arg) for arg in args]
     sql = get_named_sql(sql)
     return sql, args
 
 
-def get_named_sql_args(sql: str, **kwargs):
-    args = get_named_args(sql, **kwargs)
-    return get_named_sql(sql), args
-
-
 @lru_cache(maxsize=CACHE_SIZE)
 def get_named_sql(sql: str):
     return re.sub(NAMED_REGEX, '?', sql)
 
 
 def get_named_args(sql: str, **kwargs):
     return [kwargs[r[1:]] for r in re.findall(NAMED_REGEX, sql)]
@@ -68,30 +61,23 @@
     idx = lower_sql.rindex('limit')
     if idx > 0 and ')' in lower_sql[idx:]:
         return True
     return False
 
 
 def set_config(engin, show_sql):
-    global _ENGIN
+    # global _ENGIN
     global _SQL_ENGIN
     global before_execute
-    _ENGIN = engin
-    if engin == Engin.MySQL:
-        _SQL_ENGIN = MySqlEngin(logger, show_sql)
-    elif engin == Engin.PostgreSQL:
-        _SQL_ENGIN = PostgresEngin(logger, show_sql)
+    # _ENGIN = engin
+    _SQL_ENGIN = create_sql_engin(engin, show_sql)
     before_execute = _SQL_ENGIN.before_execute
 
 
-def get_engin():
-    global _ENGIN
-    return _ENGIN
-
-
-def get_sql_engin():
-    global _SQL_ENGIN
-    return _SQL_ENGIN
-
-
-
-
+# def get_engin():
+#     global _ENGIN
+#     return _ENGIN
+#
+#
+# def get_sql_engin():
+#     global _SQL_ENGIN
+#     return _SQL_ENGIN
```

### Comparing `sqlx-exec-1.1.2/sqlexec/support.py` & `sqlx-exec-1.1.3/sqlexec/support.py`

 * *Files identical despite different names*

### Comparing `sqlx-exec-1.1.2/sqlx_exec.egg-info/PKG-INFO` & `sqlx-exec-1.1.3/sqlx_exec.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: sqlx-exec
-Version: 1.1.2
+Version: 1.1.3
 Summary: sqlx-exec is a simple sql executor for Python, it help you auto manage database connection and transaction.
 Home-page: https://gitee.com/summry/sql-exec
 Author: summy
 Author-email: xiazhongbiao@126.com
 License: UNKNOWN
 Keywords: sql,MySQL,PostgreSQL,python
 Platform: UNKNOWN
```

