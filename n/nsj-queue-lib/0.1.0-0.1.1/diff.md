# Comparing `tmp/nsj_queue_lib-0.1.0.tar.gz` & `tmp/nsj_queue_lib-0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nsj_queue_lib-0.1.0.tar", last modified: Sat Jul 22 20:31:06 2023, max compression
+gzip compressed data, was "nsj_queue_lib-0.1.1.tar", last modified: Sat Jul 22 22:50:29 2023, max compression
```

## Comparing `nsj_queue_lib-0.1.0.tar` & `nsj_queue_lib-0.1.1.tar`

### file list

```diff
@@ -1,14 +1,27 @@
-drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-22 20:31:06.088917 nsj_queue_lib-0.1.0/
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     2542 2023-07-22 20:31:06.088917 nsj_queue_lib-0.1.0/PKG-INFO
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     1976 2023-07-21 22:40:47.000000 nsj_queue_lib-0.1.0/README.md
-drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-22 20:31:06.084917 nsj_queue_lib-0.1.0/nsj_queue_lib/
-drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-22 20:31:06.088917 nsj_queue_lib-0.1.0/nsj_queue_lib/nsj_queue_lib.egg-info/
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     2542 2023-07-22 20:31:06.000000 nsj_queue_lib-0.1.0/nsj_queue_lib/nsj_queue_lib.egg-info/PKG-INFO
--rw-rw-r--   0 sergio    (1000) sergio    (1000)      320 2023-07-22 20:31:06.000000 nsj_queue_lib-0.1.0/nsj_queue_lib/nsj_queue_lib.egg-info/SOURCES.txt
--rw-rw-r--   0 sergio    (1000) sergio    (1000)        1 2023-07-22 20:31:06.000000 nsj_queue_lib-0.1.0/nsj_queue_lib/nsj_queue_lib.egg-info/dependency_links.txt
--rw-rw-r--   0 sergio    (1000) sergio    (1000)       64 2023-07-22 20:31:06.000000 nsj_queue_lib-0.1.0/nsj_queue_lib/nsj_queue_lib.egg-info/requires.txt
--rw-rw-r--   0 sergio    (1000) sergio    (1000)        1 2023-07-22 20:31:06.000000 nsj_queue_lib-0.1.0/nsj_queue_lib/nsj_queue_lib.egg-info/top_level.txt
--rw-rw-r--   0 sergio    (1000) sergio    (1000)      103 2023-07-21 22:32:09.000000 nsj_queue_lib-0.1.0/pyproject.toml
--rw-rw-r--   0 sergio    (1000) sergio    (1000)      808 2023-07-22 20:31:06.088917 nsj_queue_lib-0.1.0/setup.cfg
-drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-22 20:31:06.088917 nsj_queue_lib-0.1.0/tests/
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     1284 2023-07-19 18:24:10.000000 nsj_queue_lib-0.1.0/tests/test_push_notification.py
+drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-22 22:50:29.163897 nsj_queue_lib-0.1.1/
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     2542 2023-07-22 22:50:29.163897 nsj_queue_lib-0.1.1/PKG-INFO
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     1976 2023-07-21 22:40:47.000000 nsj_queue_lib-0.1.1/README.md
+drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-22 22:50:29.163897 nsj_queue_lib-0.1.1/nsj_queue_lib/
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)        0 2023-07-19 18:24:10.000000 nsj_queue_lib-0.1.1/nsj_queue_lib/__init__.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)       45 2023-07-19 18:24:10.000000 nsj_queue_lib-0.1.1/nsj_queue_lib/exception.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     1090 2023-07-22 22:37:18.000000 nsj_queue_lib-0.1.1/nsj_queue_lib/lock_dao.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     7294 2023-07-22 22:39:51.000000 nsj_queue_lib-0.1.1/nsj_queue_lib/main_thread.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     3908 2023-07-22 22:40:09.000000 nsj_queue_lib-0.1.1/nsj_queue_lib/notify_thread.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     3213 2023-07-22 22:40:19.000000 nsj_queue_lib-0.1.1/nsj_queue_lib/purge_thread.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     1667 2023-07-22 22:49:32.000000 nsj_queue_lib-0.1.1/nsj_queue_lib/queue_client.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     4883 2023-07-22 22:40:29.000000 nsj_queue_lib-0.1.1/nsj_queue_lib/retry_thread.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     3827 2023-07-22 20:27:57.000000 nsj_queue_lib-0.1.1/nsj_queue_lib/retry_util.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     1824 2023-07-19 18:24:10.000000 nsj_queue_lib-0.1.1/nsj_queue_lib/settings.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     5910 2023-07-22 22:48:30.000000 nsj_queue_lib-0.1.1/nsj_queue_lib/tarefa_dao.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)      860 2023-07-19 18:24:10.000000 nsj_queue_lib-0.1.1/nsj_queue_lib/worker_base.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)      252 2023-07-22 18:37:53.000000 nsj_queue_lib-0.1.1/nsj_queue_lib/worker_fila_teste.py
+drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-22 22:50:29.163897 nsj_queue_lib-0.1.1/nsj_queue_lib.egg-info/
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     2542 2023-07-22 22:50:29.000000 nsj_queue_lib-0.1.1/nsj_queue_lib.egg-info/PKG-INFO
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)      661 2023-07-22 22:50:29.000000 nsj_queue_lib-0.1.1/nsj_queue_lib.egg-info/SOURCES.txt
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)        1 2023-07-22 22:50:29.000000 nsj_queue_lib-0.1.1/nsj_queue_lib.egg-info/dependency_links.txt
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)       64 2023-07-22 22:50:29.000000 nsj_queue_lib-0.1.1/nsj_queue_lib.egg-info/requires.txt
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)       14 2023-07-22 22:50:29.000000 nsj_queue_lib-0.1.1/nsj_queue_lib.egg-info/top_level.txt
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)      103 2023-07-21 22:32:09.000000 nsj_queue_lib-0.1.1/pyproject.toml
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)      786 2023-07-22 22:50:29.163897 nsj_queue_lib-0.1.1/setup.cfg
+drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-22 22:50:29.163897 nsj_queue_lib-0.1.1/tests/
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     1324 2023-07-22 22:40:40.000000 nsj_queue_lib-0.1.1/tests/test_push_notification.py
```

### Comparing `nsj_queue_lib-0.1.0/PKG-INFO` & `nsj_queue_lib-0.1.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nsj_queue_lib
-Version: 0.1.0
+Version: 0.1.1
 Summary: Biblioteca para facilitar a implementação de filas e workers.
 Home-page: https://github.com/Nasajon/nsj-queue-lib
 Author: Nasajon Sistemas
 Author-email: contact.dev@nasajon.com.br
 Project-URL: Source, https://github.com/Nasajon/nsj-queue-lib
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
```

### Comparing `nsj_queue_lib-0.1.0/README.md` & `nsj_queue_lib-0.1.1/README.md`

 * *Files identical despite different names*

### Comparing `nsj_queue_lib-0.1.0/nsj_queue_lib/nsj_queue_lib.egg-info/PKG-INFO` & `nsj_queue_lib-0.1.1/nsj_queue_lib.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nsj-queue-lib
-Version: 0.1.0
+Version: 0.1.1
 Summary: Biblioteca para facilitar a implementação de filas e workers.
 Home-page: https://github.com/Nasajon/nsj-queue-lib
 Author: Nasajon Sistemas
 Author-email: contact.dev@nasajon.com.br
 Project-URL: Source, https://github.com/Nasajon/nsj-queue-lib
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
```

### Comparing `nsj_queue_lib-0.1.0/setup.cfg` & `nsj_queue_lib-0.1.1/setup.cfg`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = nsj_queue_lib
-version = 0.1.0
+version = 0.1.1
 author = Nasajon Sistemas
 author_email = contact.dev@nasajon.com.br
 description = Biblioteca para facilitar a implementação de filas e workers.
 long_description = file: README.md
 long_description_content_type = text/markdown
 url = https://github.com/Nasajon/nsj-queue-lib
 project_urls = 
@@ -13,22 +13,22 @@
 	Development Status :: 3 - Alpha
 	Intended Audience :: Developers
 	Topic :: Software Development :: Libraries
 	Programming Language :: Python :: 3
 
 [options]
 package_dir = 
-	= nsj_queue_lib
+	= ./
 packages = find:
 python_requires = >=3.4
 install_requires = 
 	psycopg2_binary>=2.9.6
 	python-logging-loki>=0.3.1
 	pytest>=7.1.3
 
 [options.packages.find]
-where = nsj_queue_lib
+where = ./
 
 [egg_info]
 tag_build = 
 tag_date = 0
```

### Comparing `nsj_queue_lib-0.1.0/tests/test_push_notification.py` & `nsj_queue_lib-0.1.1/tests/test_push_notification.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,52 +1,53 @@
 import time
 
-from nsj_queue_lib.dbadapter import DBAdapter
-from nsj_queue_lib.dbconection import DBConnection
+from nsj_sql_utils_lib.dbadapter3 import DBAdapter3
+from nsj_sql_utils_lib.dbconection_psycopg2 import DBConnectionPsycopg2
+
 from nsj_queue_lib.settings import (
     DB_HOST,
     DB_PORT,
     DB_BASE,
     DB_USER,
     DB_PASS,
 )
 
 
-def _load_scene(db: DBAdapter):
+def _load_scene(db: DBAdapter3):
     sql = """
         insert into fila_teste (origem, destino, processo, chave_externa, payload) values
         ('dbeaver', 'codigo', 'teste_da_fila', '123456', 'conteudo da mensagem, pode ser muito complexo')
         returning id
     """
     resp, _ = db.execute(sql)
 
     return resp[0]["id"]
 
 
-def _get_tarefa(db: DBAdapter, tarefa_id: int):
+def _get_tarefa(db: DBAdapter3, tarefa_id: int):
     sql = """
         select * from fila_teste where id=%(id)s
     """
     resp, _ = db.execute(sql, id=tarefa_id)
 
     return resp[0]
 
 
-def _delete_tarefa(db: DBAdapter, tarefa_id: int):
+def _delete_tarefa(db: DBAdapter3, tarefa_id: int):
     sql = """
         delete from fila_teste where id=%(id)s
     """
     _, count = db.execute(sql, id=tarefa_id)
 
     return count
 
 
 def test_push_notification():
-    with DBConnection(DB_HOST, DB_PORT, DB_BASE, DB_USER, DB_PASS) as dbconn:
-        db = DBAdapter(dbconn.conn)
+    with DBConnectionPsycopg2(DB_HOST, DB_PORT, DB_BASE, DB_USER, DB_PASS) as dbconn:
+        db = DBAdapter3(dbconn.conn)
 
         tarefa_id = _load_scene(db)
 
         time.sleep(5)
 
         tarefa = _get_tarefa(db, tarefa_id)
```

