# Comparing `tmp/nsj_queue_lib-0.1.1.tar.gz` & `tmp/nsj_queue_lib-0.1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nsj_queue_lib-0.1.1.tar", last modified: Sat Jul 22 22:50:29 2023, max compression
+gzip compressed data, was "nsj_queue_lib-0.1.2.tar", last modified: Sat Jul 22 23:50:08 2023, max compression
```

## Comparing `nsj_queue_lib-0.1.1.tar` & `nsj_queue_lib-0.1.2.tar`

### file list

```diff
@@ -1,27 +1,27 @@
-drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-22 22:50:29.163897 nsj_queue_lib-0.1.1/
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     2542 2023-07-22 22:50:29.163897 nsj_queue_lib-0.1.1/PKG-INFO
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     1976 2023-07-21 22:40:47.000000 nsj_queue_lib-0.1.1/README.md
-drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-22 22:50:29.163897 nsj_queue_lib-0.1.1/nsj_queue_lib/
--rw-rw-r--   0 sergio    (1000) sergio    (1000)        0 2023-07-19 18:24:10.000000 nsj_queue_lib-0.1.1/nsj_queue_lib/__init__.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)       45 2023-07-19 18:24:10.000000 nsj_queue_lib-0.1.1/nsj_queue_lib/exception.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     1090 2023-07-22 22:37:18.000000 nsj_queue_lib-0.1.1/nsj_queue_lib/lock_dao.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     7294 2023-07-22 22:39:51.000000 nsj_queue_lib-0.1.1/nsj_queue_lib/main_thread.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     3908 2023-07-22 22:40:09.000000 nsj_queue_lib-0.1.1/nsj_queue_lib/notify_thread.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     3213 2023-07-22 22:40:19.000000 nsj_queue_lib-0.1.1/nsj_queue_lib/purge_thread.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     1667 2023-07-22 22:49:32.000000 nsj_queue_lib-0.1.1/nsj_queue_lib/queue_client.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     4883 2023-07-22 22:40:29.000000 nsj_queue_lib-0.1.1/nsj_queue_lib/retry_thread.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     3827 2023-07-22 20:27:57.000000 nsj_queue_lib-0.1.1/nsj_queue_lib/retry_util.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     1824 2023-07-19 18:24:10.000000 nsj_queue_lib-0.1.1/nsj_queue_lib/settings.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     5910 2023-07-22 22:48:30.000000 nsj_queue_lib-0.1.1/nsj_queue_lib/tarefa_dao.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)      860 2023-07-19 18:24:10.000000 nsj_queue_lib-0.1.1/nsj_queue_lib/worker_base.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)      252 2023-07-22 18:37:53.000000 nsj_queue_lib-0.1.1/nsj_queue_lib/worker_fila_teste.py
-drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-22 22:50:29.163897 nsj_queue_lib-0.1.1/nsj_queue_lib.egg-info/
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     2542 2023-07-22 22:50:29.000000 nsj_queue_lib-0.1.1/nsj_queue_lib.egg-info/PKG-INFO
--rw-rw-r--   0 sergio    (1000) sergio    (1000)      661 2023-07-22 22:50:29.000000 nsj_queue_lib-0.1.1/nsj_queue_lib.egg-info/SOURCES.txt
--rw-rw-r--   0 sergio    (1000) sergio    (1000)        1 2023-07-22 22:50:29.000000 nsj_queue_lib-0.1.1/nsj_queue_lib.egg-info/dependency_links.txt
--rw-rw-r--   0 sergio    (1000) sergio    (1000)       64 2023-07-22 22:50:29.000000 nsj_queue_lib-0.1.1/nsj_queue_lib.egg-info/requires.txt
--rw-rw-r--   0 sergio    (1000) sergio    (1000)       14 2023-07-22 22:50:29.000000 nsj_queue_lib-0.1.1/nsj_queue_lib.egg-info/top_level.txt
--rw-rw-r--   0 sergio    (1000) sergio    (1000)      103 2023-07-21 22:32:09.000000 nsj_queue_lib-0.1.1/pyproject.toml
--rw-rw-r--   0 sergio    (1000) sergio    (1000)      786 2023-07-22 22:50:29.163897 nsj_queue_lib-0.1.1/setup.cfg
-drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-22 22:50:29.163897 nsj_queue_lib-0.1.1/tests/
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     1324 2023-07-22 22:40:40.000000 nsj_queue_lib-0.1.1/tests/test_push_notification.py
+drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-22 23:50:08.726892 nsj_queue_lib-0.1.2/
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     2542 2023-07-22 23:50:08.726892 nsj_queue_lib-0.1.2/PKG-INFO
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     1976 2023-07-21 22:40:47.000000 nsj_queue_lib-0.1.2/README.md
+drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-22 23:50:08.726892 nsj_queue_lib-0.1.2/nsj_queue_lib/
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)        0 2023-07-19 18:24:10.000000 nsj_queue_lib-0.1.2/nsj_queue_lib/__init__.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)       45 2023-07-19 18:24:10.000000 nsj_queue_lib-0.1.2/nsj_queue_lib/exception.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     1090 2023-07-22 22:37:18.000000 nsj_queue_lib-0.1.2/nsj_queue_lib/lock_dao.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     7294 2023-07-22 22:39:51.000000 nsj_queue_lib-0.1.2/nsj_queue_lib/main_thread.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     3908 2023-07-22 22:40:09.000000 nsj_queue_lib-0.1.2/nsj_queue_lib/notify_thread.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     3213 2023-07-22 22:40:19.000000 nsj_queue_lib-0.1.2/nsj_queue_lib/purge_thread.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     2848 2023-07-22 23:49:16.000000 nsj_queue_lib-0.1.2/nsj_queue_lib/queue_client.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     4883 2023-07-22 22:40:29.000000 nsj_queue_lib-0.1.2/nsj_queue_lib/retry_thread.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     3827 2023-07-22 20:27:57.000000 nsj_queue_lib-0.1.2/nsj_queue_lib/retry_util.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     1824 2023-07-19 18:24:10.000000 nsj_queue_lib-0.1.2/nsj_queue_lib/settings.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     7177 2023-07-22 23:48:23.000000 nsj_queue_lib-0.1.2/nsj_queue_lib/tarefa_dao.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)      860 2023-07-19 18:24:10.000000 nsj_queue_lib-0.1.2/nsj_queue_lib/worker_base.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)      252 2023-07-22 18:37:53.000000 nsj_queue_lib-0.1.2/nsj_queue_lib/worker_fila_teste.py
+drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-22 23:50:08.726892 nsj_queue_lib-0.1.2/nsj_queue_lib.egg-info/
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     2542 2023-07-22 23:50:08.000000 nsj_queue_lib-0.1.2/nsj_queue_lib.egg-info/PKG-INFO
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)      661 2023-07-22 23:50:08.000000 nsj_queue_lib-0.1.2/nsj_queue_lib.egg-info/SOURCES.txt
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)        1 2023-07-22 23:50:08.000000 nsj_queue_lib-0.1.2/nsj_queue_lib.egg-info/dependency_links.txt
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)       64 2023-07-22 23:50:08.000000 nsj_queue_lib-0.1.2/nsj_queue_lib.egg-info/requires.txt
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)       14 2023-07-22 23:50:08.000000 nsj_queue_lib-0.1.2/nsj_queue_lib.egg-info/top_level.txt
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)      103 2023-07-21 22:32:09.000000 nsj_queue_lib-0.1.2/pyproject.toml
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)      786 2023-07-22 23:50:08.726892 nsj_queue_lib-0.1.2/setup.cfg
+drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-22 23:50:08.726892 nsj_queue_lib-0.1.2/tests/
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     1324 2023-07-22 22:40:40.000000 nsj_queue_lib-0.1.2/tests/test_push_notification.py
```

### Comparing `nsj_queue_lib-0.1.1/PKG-INFO` & `nsj_queue_lib-0.1.2/nsj_queue_lib.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
-Name: nsj_queue_lib
-Version: 0.1.1
+Name: nsj-queue-lib
+Version: 0.1.2
 Summary: Biblioteca para facilitar a implementação de filas e workers.
 Home-page: https://github.com/Nasajon/nsj-queue-lib
 Author: Nasajon Sistemas
 Author-email: contact.dev@nasajon.com.br
 Project-URL: Source, https://github.com/Nasajon/nsj-queue-lib
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
```

### Comparing `nsj_queue_lib-0.1.1/README.md` & `nsj_queue_lib-0.1.2/README.md`

 * *Files identical despite different names*

### Comparing `nsj_queue_lib-0.1.1/nsj_queue_lib/lock_dao.py` & `nsj_queue_lib-0.1.2/nsj_queue_lib/lock_dao.py`

 * *Files identical despite different names*

### Comparing `nsj_queue_lib-0.1.1/nsj_queue_lib/main_thread.py` & `nsj_queue_lib-0.1.2/nsj_queue_lib/main_thread.py`

 * *Files identical despite different names*

### Comparing `nsj_queue_lib-0.1.1/nsj_queue_lib/notify_thread.py` & `nsj_queue_lib-0.1.2/nsj_queue_lib/notify_thread.py`

 * *Files identical despite different names*

### Comparing `nsj_queue_lib-0.1.1/nsj_queue_lib/purge_thread.py` & `nsj_queue_lib-0.1.2/nsj_queue_lib/purge_thread.py`

 * *Files identical despite different names*

### Comparing `nsj_queue_lib-0.1.1/nsj_queue_lib/retry_thread.py` & `nsj_queue_lib-0.1.2/nsj_queue_lib/retry_thread.py`

 * *Files identical despite different names*

### Comparing `nsj_queue_lib-0.1.1/nsj_queue_lib/retry_util.py` & `nsj_queue_lib-0.1.2/nsj_queue_lib/retry_util.py`

 * *Files identical despite different names*

### Comparing `nsj_queue_lib-0.1.1/nsj_queue_lib/settings.py` & `nsj_queue_lib-0.1.2/nsj_queue_lib/settings.py`

 * *Files identical despite different names*

### Comparing `nsj_queue_lib-0.1.1/nsj_queue_lib/tarefa_dao.py` & `nsj_queue_lib-0.1.2/nsj_queue_lib/tarefa_dao.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,8 +1,9 @@
 import datetime
+import hashlib
 
 from nsj_sql_utils_lib import dao_util
 
 from nsj_sql_utils_lib.dbadapter3 import DBAdapter3
 from nsj_queue_lib.exception import NotFoundException
 from nsj_queue_lib.settings import QUEUE_TABLE
 
@@ -23,14 +24,15 @@
         "mensagem",
         "id_anterior",
         "data_hora_anterior",
         "status_anterior",
         "mensagem_anterior",
         "tenant",
         "grupo_empresarial",
+        "payload_hash",
     ]
     COLUNAS_STR = "tarefa." + ", tarefa.".join(COLUNAS)
 
     def __init__(self, db: DBAdapter3):
         self.db = db
 
     def get(self, id: int):
@@ -117,14 +119,23 @@
                 status = 'agendada'
                 and data_hora <= clock_timestamp()
             order by data_hora
         """
         return self.db.execute(sql)
 
     def insert(self, tarefa: dict[str, any]):
+        # Calculando o hash do payload
+        if (
+            "payload" in tarefa
+            and tarefa["payload"] is not None
+            and tarefa["payload"] != ""
+        ):
+            payload_hash = hashlib.sha256(tarefa["payload"].encode()).hexdigest()
+            tarefa["payload_hash"] = payload_hash
+
         # Verificando os fields recebidos
         fields = []
         for col in TarefaDAO.COLUNAS:
             if col in tarefa:
                 fields.append(col)
 
         # Criando a partes de fields e values do insert
@@ -194,7 +205,37 @@
         self.db.execute(sql, id=tarefa_id, status=status)
 
     def notify(self, nome_fila: str):
         sql = f"""
             notify {nome_fila}, ''
         """
         self.db.execute(sql)
+
+    def list_equivalent(self, chave_externa: str, payload: str, status: list[str]):
+        """
+        Lista as tarefas com mesma chave externa, payload e em algum dos status passados.
+        """
+
+        # Calculando o hash do payload
+        payload_hash = None
+        if payload is not None and payload != "":
+            payload_hash = hashlib.sha256(payload.encode()).hexdigest()
+
+        sql = f"""
+            select
+                {TarefaDAO.COLUNAS_STR}
+            from
+                {QUEUE_TABLE} as tarefa
+            where
+                tarefa.payload_hash = %(payload_hash)s
+                and chave_externa = %(chave_externa)s
+                and tarefa.status in %(status)s
+        """
+
+        result, _ = self.db.execute(
+            sql,
+            payload_hash=payload_hash,
+            chave_externa=chave_externa,
+            status=tuple(status),
+        )
+
+        return result
```

### Comparing `nsj_queue_lib-0.1.1/nsj_queue_lib/worker_base.py` & `nsj_queue_lib-0.1.2/nsj_queue_lib/worker_base.py`

 * *Files identical despite different names*

### Comparing `nsj_queue_lib-0.1.1/nsj_queue_lib.egg-info/PKG-INFO` & `nsj_queue_lib-0.1.2/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
-Name: nsj-queue-lib
-Version: 0.1.1
+Name: nsj_queue_lib
+Version: 0.1.2
 Summary: Biblioteca para facilitar a implementação de filas e workers.
 Home-page: https://github.com/Nasajon/nsj-queue-lib
 Author: Nasajon Sistemas
 Author-email: contact.dev@nasajon.com.br
 Project-URL: Source, https://github.com/Nasajon/nsj-queue-lib
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
```

### Comparing `nsj_queue_lib-0.1.1/nsj_queue_lib.egg-info/SOURCES.txt` & `nsj_queue_lib-0.1.2/nsj_queue_lib.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `nsj_queue_lib-0.1.1/setup.cfg` & `nsj_queue_lib-0.1.2/setup.cfg`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = nsj_queue_lib
-version = 0.1.1
+version = 0.1.2
 author = Nasajon Sistemas
 author_email = contact.dev@nasajon.com.br
 description = Biblioteca para facilitar a implementação de filas e workers.
 long_description = file: README.md
 long_description_content_type = text/markdown
 url = https://github.com/Nasajon/nsj-queue-lib
 project_urls =
```

### Comparing `nsj_queue_lib-0.1.1/tests/test_push_notification.py` & `nsj_queue_lib-0.1.2/tests/test_push_notification.py`

 * *Files identical despite different names*

