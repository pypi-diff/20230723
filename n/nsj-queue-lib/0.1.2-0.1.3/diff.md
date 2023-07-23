# Comparing `tmp/nsj_queue_lib-0.1.2.tar.gz` & `tmp/nsj_queue_lib-0.1.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nsj_queue_lib-0.1.2.tar", last modified: Sat Jul 22 23:50:08 2023, max compression
+gzip compressed data, was "nsj_queue_lib-0.1.3.tar", last modified: Sun Jul 23 00:04:36 2023, max compression
```

## Comparing `nsj_queue_lib-0.1.2.tar` & `nsj_queue_lib-0.1.3.tar`

### file list

```diff
@@ -1,27 +1,27 @@
-drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-22 23:50:08.726892 nsj_queue_lib-0.1.2/
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     2542 2023-07-22 23:50:08.726892 nsj_queue_lib-0.1.2/PKG-INFO
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     1976 2023-07-21 22:40:47.000000 nsj_queue_lib-0.1.2/README.md
-drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-22 23:50:08.726892 nsj_queue_lib-0.1.2/nsj_queue_lib/
--rw-rw-r--   0 sergio    (1000) sergio    (1000)        0 2023-07-19 18:24:10.000000 nsj_queue_lib-0.1.2/nsj_queue_lib/__init__.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)       45 2023-07-19 18:24:10.000000 nsj_queue_lib-0.1.2/nsj_queue_lib/exception.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     1090 2023-07-22 22:37:18.000000 nsj_queue_lib-0.1.2/nsj_queue_lib/lock_dao.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     7294 2023-07-22 22:39:51.000000 nsj_queue_lib-0.1.2/nsj_queue_lib/main_thread.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     3908 2023-07-22 22:40:09.000000 nsj_queue_lib-0.1.2/nsj_queue_lib/notify_thread.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     3213 2023-07-22 22:40:19.000000 nsj_queue_lib-0.1.2/nsj_queue_lib/purge_thread.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     2848 2023-07-22 23:49:16.000000 nsj_queue_lib-0.1.2/nsj_queue_lib/queue_client.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     4883 2023-07-22 22:40:29.000000 nsj_queue_lib-0.1.2/nsj_queue_lib/retry_thread.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     3827 2023-07-22 20:27:57.000000 nsj_queue_lib-0.1.2/nsj_queue_lib/retry_util.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     1824 2023-07-19 18:24:10.000000 nsj_queue_lib-0.1.2/nsj_queue_lib/settings.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     7177 2023-07-22 23:48:23.000000 nsj_queue_lib-0.1.2/nsj_queue_lib/tarefa_dao.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)      860 2023-07-19 18:24:10.000000 nsj_queue_lib-0.1.2/nsj_queue_lib/worker_base.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)      252 2023-07-22 18:37:53.000000 nsj_queue_lib-0.1.2/nsj_queue_lib/worker_fila_teste.py
-drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-22 23:50:08.726892 nsj_queue_lib-0.1.2/nsj_queue_lib.egg-info/
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     2542 2023-07-22 23:50:08.000000 nsj_queue_lib-0.1.2/nsj_queue_lib.egg-info/PKG-INFO
--rw-rw-r--   0 sergio    (1000) sergio    (1000)      661 2023-07-22 23:50:08.000000 nsj_queue_lib-0.1.2/nsj_queue_lib.egg-info/SOURCES.txt
--rw-rw-r--   0 sergio    (1000) sergio    (1000)        1 2023-07-22 23:50:08.000000 nsj_queue_lib-0.1.2/nsj_queue_lib.egg-info/dependency_links.txt
--rw-rw-r--   0 sergio    (1000) sergio    (1000)       64 2023-07-22 23:50:08.000000 nsj_queue_lib-0.1.2/nsj_queue_lib.egg-info/requires.txt
--rw-rw-r--   0 sergio    (1000) sergio    (1000)       14 2023-07-22 23:50:08.000000 nsj_queue_lib-0.1.2/nsj_queue_lib.egg-info/top_level.txt
--rw-rw-r--   0 sergio    (1000) sergio    (1000)      103 2023-07-21 22:32:09.000000 nsj_queue_lib-0.1.2/pyproject.toml
--rw-rw-r--   0 sergio    (1000) sergio    (1000)      786 2023-07-22 23:50:08.726892 nsj_queue_lib-0.1.2/setup.cfg
-drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-22 23:50:08.726892 nsj_queue_lib-0.1.2/tests/
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     1324 2023-07-22 22:40:40.000000 nsj_queue_lib-0.1.2/tests/test_push_notification.py
+drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-23 00:04:36.986728 nsj_queue_lib-0.1.3/
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     2542 2023-07-23 00:04:36.986728 nsj_queue_lib-0.1.3/PKG-INFO
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     1976 2023-07-21 22:40:47.000000 nsj_queue_lib-0.1.3/README.md
+drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-23 00:04:36.986728 nsj_queue_lib-0.1.3/nsj_queue_lib/
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)        0 2023-07-19 18:24:10.000000 nsj_queue_lib-0.1.3/nsj_queue_lib/__init__.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)       45 2023-07-19 18:24:10.000000 nsj_queue_lib-0.1.3/nsj_queue_lib/exception.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     1090 2023-07-22 22:37:18.000000 nsj_queue_lib-0.1.3/nsj_queue_lib/lock_dao.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     7337 2023-07-22 23:56:41.000000 nsj_queue_lib-0.1.3/nsj_queue_lib/main_thread.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     3938 2023-07-22 23:56:52.000000 nsj_queue_lib-0.1.3/nsj_queue_lib/notify_thread.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     3243 2023-07-22 23:57:02.000000 nsj_queue_lib-0.1.3/nsj_queue_lib/purge_thread.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     2879 2023-07-22 23:57:12.000000 nsj_queue_lib-0.1.3/nsj_queue_lib/queue_client.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     4913 2023-07-22 23:57:41.000000 nsj_queue_lib-0.1.3/nsj_queue_lib/retry_thread.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     3827 2023-07-22 20:27:57.000000 nsj_queue_lib-0.1.3/nsj_queue_lib/retry_util.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     1824 2023-07-19 18:24:10.000000 nsj_queue_lib-0.1.3/nsj_queue_lib/settings.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     7252 2023-07-22 23:56:10.000000 nsj_queue_lib-0.1.3/nsj_queue_lib/tarefa_dao.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)      860 2023-07-19 18:24:10.000000 nsj_queue_lib-0.1.3/nsj_queue_lib/worker_base.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)      252 2023-07-22 18:37:53.000000 nsj_queue_lib-0.1.3/nsj_queue_lib/worker_fila_teste.py
+drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-23 00:04:36.986728 nsj_queue_lib-0.1.3/nsj_queue_lib.egg-info/
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     2542 2023-07-23 00:04:36.000000 nsj_queue_lib-0.1.3/nsj_queue_lib.egg-info/PKG-INFO
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)      661 2023-07-23 00:04:36.000000 nsj_queue_lib-0.1.3/nsj_queue_lib.egg-info/SOURCES.txt
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)        1 2023-07-23 00:04:36.000000 nsj_queue_lib-0.1.3/nsj_queue_lib.egg-info/dependency_links.txt
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)       64 2023-07-23 00:04:36.000000 nsj_queue_lib-0.1.3/nsj_queue_lib.egg-info/requires.txt
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)       14 2023-07-23 00:04:36.000000 nsj_queue_lib-0.1.3/nsj_queue_lib.egg-info/top_level.txt
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)      103 2023-07-21 22:32:09.000000 nsj_queue_lib-0.1.3/pyproject.toml
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)      786 2023-07-23 00:04:36.986728 nsj_queue_lib-0.1.3/setup.cfg
+drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-23 00:04:36.986728 nsj_queue_lib-0.1.3/tests/
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     1324 2023-07-22 22:40:40.000000 nsj_queue_lib-0.1.3/tests/test_push_notification.py
```

### Comparing `nsj_queue_lib-0.1.2/PKG-INFO` & `nsj_queue_lib-0.1.3/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nsj_queue_lib
-Version: 0.1.2
+Version: 0.1.3
 Summary: Biblioteca para facilitar a implementação de filas e workers.
 Home-page: https://github.com/Nasajon/nsj-queue-lib
 Author: Nasajon Sistemas
 Author-email: contact.dev@nasajon.com.br
 Project-URL: Source, https://github.com/Nasajon/nsj-queue-lib
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
```

### Comparing `nsj_queue_lib-0.1.2/README.md` & `nsj_queue_lib-0.1.3/README.md`

 * *Files identical despite different names*

### Comparing `nsj_queue_lib-0.1.2/nsj_queue_lib/lock_dao.py` & `nsj_queue_lib-0.1.3/nsj_queue_lib/lock_dao.py`

 * *Files identical despite different names*

### Comparing `nsj_queue_lib-0.1.2/nsj_queue_lib/main_thread.py` & `nsj_queue_lib-0.1.3/nsj_queue_lib/main_thread.py`

 * *Files 4% similar despite different names*

```diff
@@ -14,14 +14,15 @@
     DB_PORT,
     DB_BASE,
     DB_USER,
     DB_PASS,
     QUEUE_NAME,
     GLOBAL_RUN,
     QUEUE_MAX_RETRY,
+    QUEUE_TABLE,
     logger,
 )
 
 
 class MainThread:
     def __init__(self, worker):
         self.worker = worker
@@ -83,15 +84,15 @@
     def _run_tarefas(self, conn):
         """
         Recupera a lista de tarefas pendentes, e tenta executar uma de cada vez.
         """
 
         db = DBAdapter3(conn)
         lock_dao = LockDAO(db)
-        tarefa_dao = TarefaDAO(db)
+        tarefa_dao = TarefaDAO(db, QUEUE_TABLE)
 
         # Recuperando todas as tarefas pendentes
         logger.info("Recuperando tarefas pendentes.")
         pendentes, count = tarefa_dao.list_pendentes(QUEUE_MAX_RETRY)
         logger.info(f"Quantidade recuperada {count}.")
 
         for tarefa in pendentes:
@@ -171,15 +172,15 @@
         """
 
         # Iniciando nova conexão com o BD, para a tarefa
         with DBConnectionPsycopg2(
             DB_HOST, DB_PORT, DB_BASE, DB_USER, DB_PASS
         ) as new_dbconn:
             new_db = DBAdapter3(new_dbconn.conn)
-            new_dao = TarefaDAO(new_db)
+            new_dao = TarefaDAO(new_db, QUEUE_TABLE)
 
             # Iniciando transação
             new_dao.db.begin()
             try:
                 # Invocando o código customizado para execução da tarefa.
                 self.worker.execute(tarefa, new_dbconn)
```

### Comparing `nsj_queue_lib-0.1.2/nsj_queue_lib/notify_thread.py` & `nsj_queue_lib-0.1.3/nsj_queue_lib/notify_thread.py`

 * *Files 2% similar despite different names*

```diff
@@ -12,14 +12,15 @@
     DB_HOST,
     DB_PORT,
     DB_BASE,
     DB_USER,
     DB_PASS,
     QUEUE_NAME,
     QUEUE_MINUTE_NOTIFY_THREAD,
+    QUEUE_TABLE,
     GLOBAL_RUN,
     logger,
 )
 
 
 class NotifyThread(threading.Thread):
     def __init__(self):
@@ -67,15 +68,15 @@
                             logger.debug(
                                 "Desistindo do notify, porque já há outro worker operando o mesmo."
                             )
                             continue
 
                         logger.info("Iniciando tratamento de notify...")
 
-                        dao = TarefaDAO(db)
+                        dao = TarefaDAO(db, QUEUE_TABLE)
                         self._notify(dao)
 
                     finally:
                         if lock:
                             lock_dao.unlock_notify()
 
             except Exception as e:
```

### Comparing `nsj_queue_lib-0.1.2/nsj_queue_lib/purge_thread.py` & `nsj_queue_lib-0.1.3/nsj_queue_lib/purge_thread.py`

 * *Files 2% similar despite different names*

```diff
@@ -13,14 +13,15 @@
     DB_PORT,
     DB_BASE,
     DB_USER,
     DB_PASS,
     QUEUE_MINUTE_PURGE_THREAD,
     QUEUE_PURGE_MAX_AGE,
     QUEUE_PURGE_LIMIT,
+    QUEUE_TABLE,
     GLOBAL_RUN,
     logger,
 )
 
 
 class PurgeThread(threading.Thread):
     def __init__(self):
@@ -67,15 +68,15 @@
                             logger.debug(
                                 "Desistindo do purge, porque já há outro worker operando o mesmo."
                             )
                             continue
 
                         logger.info("Iniciando tratamento de purge...")
 
-                        dao = TarefaDAO(db)
+                        dao = TarefaDAO(db, QUEUE_TABLE)
                         self._purge(dao)
 
                     finally:
                         if lock:
                             lock_dao.unlock_purge()
 
             except Exception as e:
```

### Comparing `nsj_queue_lib-0.1.2/nsj_queue_lib/queue_client.py` & `nsj_queue_lib-0.1.3/nsj_queue_lib/queue_client.py`

 * *Files 5% similar despite different names*

```diff
@@ -2,16 +2,16 @@
 
 from nsj_sql_utils_lib.dbadapter3 import DBAdapter3
 
 from tarefa_dao import TarefaDAO
 
 
 class QueueClient:
-    def __init__(self, bd_conn) -> None:
-        self._tarefa_dao = TarefaDAO(DBAdapter3(bd_conn))
+    def __init__(self, bd_conn, queue_table: str) -> None:
+        self._tarefa_dao = TarefaDAO(DBAdapter3(bd_conn), queue_table)
 
     def insert_task(
         self,
         origem: str,
         destino: str,
         processo: str,
         chave_externa: str,
```

### Comparing `nsj_queue_lib-0.1.2/nsj_queue_lib/retry_thread.py` & `nsj_queue_lib-0.1.3/nsj_queue_lib/retry_thread.py`

 * *Files 3% similar despite different names*

```diff
@@ -13,14 +13,15 @@
 from nsj_queue_lib.settings import (
     DB_HOST,
     DB_PORT,
     DB_BASE,
     DB_USER,
     DB_PASS,
     QUEUE_MINUTE_RETRY_THREAD,
+    QUEUE_TABLE,
     GLOBAL_RUN,
     logger,
 )
 
 
 class RetryThread(threading.Thread):
     def __init__(self):
@@ -68,15 +69,15 @@
                             logger.debug(
                                 "Desistindo da thread de retentativas, porque já há outro worker operando o mesmo."
                             )
                             continue
 
                         logger.info("Iniciando tratamento de retentativas...")
 
-                        tarefa_dao = TarefaDAO(db)
+                        tarefa_dao = TarefaDAO(db, QUEUE_TABLE)
                         # self._retry_falhas(tarefa_dao)
                         self._retry_perdidas(tarefa_dao, lock_dao)
 
                     finally:
                         if lock:
                             lock_dao.unlock_retry()
             except Exception as e:
```

### Comparing `nsj_queue_lib-0.1.2/nsj_queue_lib/retry_util.py` & `nsj_queue_lib-0.1.3/nsj_queue_lib/retry_util.py`

 * *Files identical despite different names*

### Comparing `nsj_queue_lib-0.1.2/nsj_queue_lib/settings.py` & `nsj_queue_lib-0.1.3/nsj_queue_lib/settings.py`

 * *Files identical despite different names*

### Comparing `nsj_queue_lib-0.1.2/nsj_queue_lib/tarefa_dao.py` & `nsj_queue_lib-0.1.3/nsj_queue_lib/tarefa_dao.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,15 +1,14 @@
 import datetime
 import hashlib
 
 from nsj_sql_utils_lib import dao_util
 
 from nsj_sql_utils_lib.dbadapter3 import DBAdapter3
 from nsj_queue_lib.exception import NotFoundException
-from nsj_queue_lib.settings import QUEUE_TABLE
 
 
 class TarefaDAO:
     COLUNAS = [
         "id",
         "id_inicial",
         "data_hora_inicial",
@@ -28,28 +27,29 @@
         "mensagem_anterior",
         "tenant",
         "grupo_empresarial",
         "payload_hash",
     ]
     COLUNAS_STR = "tarefa." + ", tarefa.".join(COLUNAS)
 
-    def __init__(self, db: DBAdapter3):
+    def __init__(self, db: DBAdapter3, queue_table: str):
         self.db = db
+        self.queue_table = queue_table
 
     def get(self, id: int):
         """
         Recupera uma tarefa, por meio de seu ID
         """
         sql = f"""
             select
                 {TarefaDAO.COLUNAS_STR},
                 coalesce(tarefa.payload, inicial.payload) as payload
             from
-                {QUEUE_TABLE} as tarefa
-                left join {QUEUE_TABLE} as inicial
+                {self.queue_table} as tarefa
+                left join {self.queue_table} as inicial
                 on (tarefa.id_inicial = inicial.id)
             where
                 tarefa.id = %(id)s
         """
         result, count = self.db.execute(sql, id=id)
 
         if count != 1:
@@ -61,15 +61,15 @@
     #     """
     #     Lista as tarefas que tiveram falha, mas ainda passíveis de novo tratamento.
     #     """
     #     sql = f"""
     #         select
     #             {TarefaDAO.COLUNAS}
     #         from
-    #             {QUEUE_TABLE}
+    #             {self.queue_table}
     #         where
     #             status = 'falha'
     #             and tentativa <= %(max_tentativas)s
     #             and not reenfileirado
     #     """
     #     return self.db.execute(sql, max_tentativas=max_retries)
 
@@ -77,30 +77,30 @@
         """
         Lista as tarefas que estão em processando.
         """
         sql = f"""
             select
                 {TarefaDAO.COLUNAS_STR}
             from
-                {QUEUE_TABLE} as tarefa
+                {self.queue_table} as tarefa
             where
                 status = 'processando'
         """
         return self.db.execute(sql)
 
     def list_pendentes(self, max_tentativas: int):
         """
         Lista as tarefas que estiverem disponíveis para execução.
         """
         # TODO Adicionar join para ordenação com prioridades (tabela de configuração das prioridades)
         sql = f"""
             select
                 {TarefaDAO.COLUNAS_STR}
             from
-                {QUEUE_TABLE} as tarefa
+                {self.queue_table} as tarefa
             where
                 status = 'pendente'
                 and tentativa <= %(max_tentativas)s
                 and data_hora <= clock_timestamp()
             order by data_hora
         """
         return self.db.execute(sql, max_tentativas=max_tentativas)
@@ -110,15 +110,15 @@
         Lista as tarefas que estiverem agendadas e já passíveis de execução.
         """
         # TODO Adicionar join para ordenação com prioridades (tabela de configuração das prioridades)
         sql = f"""
             select
                 {TarefaDAO.COLUNAS_STR}
             from
-                {QUEUE_TABLE} as tarefa
+                {self.queue_table} as tarefa
             where
                 status = 'agendada'
                 and data_hora <= clock_timestamp()
             order by data_hora
         """
         return self.db.execute(sql)
 
@@ -141,15 +141,15 @@
         # Criando a partes de fields e values do insert
         sql_fields, sql_values = dao_util.make_sql_insert_fields_values(
             fields, psycopg2=True
         )
 
         # Criando a query em si
         sql = f"""
-            insert into {QUEUE_TABLE} (
+            insert into {self.queue_table} (
                 {sql_fields}
             ) values (
                 {sql_values}
             )
         """
 
         # Executando o insert
@@ -159,15 +159,15 @@
         self,
         tarefa_id: int,
         status: str,
         msg: str,
         proxima_tentativa: datetime.datetime,
     ):
         sql = f"""
-            update {QUEUE_TABLE} set
+            update {self.queue_table} set
                 reenfileirado = True,
                 status = %(status)s,
                 mensagem=%(msg)s,
                 proxima_tentativa=%(proxima_tentativa)s
             where id=%(id)s
         """
         self.db.execute(
@@ -176,35 +176,35 @@
             status=status,
             msg=msg,
             proxima_tentativa=proxima_tentativa,
         )
 
     def update_falha_max_retries(self, tarefa_id: int, status: str, msg: str):
         sql = f"""
-            update {QUEUE_TABLE} set estouro_tentativas = True, status = %(status)s, mensagem=%(msg)s where id=%(id)s
+            update {self.queue_table} set estouro_tentativas = True, status = %(status)s, mensagem=%(msg)s where id=%(id)s
         """
         self.db.execute(sql, id=tarefa_id, status=status, msg=msg)
 
     def purge(self, max_age: int, purge_limit: int):
         sql = f"""
-            DELETE FROM {QUEUE_TABLE}
+            DELETE FROM {self.queue_table}
             WHERE ctid IN (
                 SELECT ctid
-                FROM {QUEUE_TABLE}
+                FROM {self.queue_table}
                 WHERE
                     data_hora > clock_timestamp() - interval '{max_age} days'
                 ORDER BY data_hora
                 LIMIT {purge_limit}
             )        
         """
         self.db.execute(sql)
 
     def update_status(self, tarefa_id: int, status: str):
         sql = f"""
-            update {QUEUE_TABLE} set status = %(status)s where id=%(id)s
+            update {self.queue_table} set status = %(status)s where id=%(id)s
         """
         self.db.execute(sql, id=tarefa_id, status=status)
 
     def notify(self, nome_fila: str):
         sql = f"""
             notify {nome_fila}, ''
         """
@@ -220,15 +220,15 @@
         if payload is not None and payload != "":
             payload_hash = hashlib.sha256(payload.encode()).hexdigest()
 
         sql = f"""
             select
                 {TarefaDAO.COLUNAS_STR}
             from
-                {QUEUE_TABLE} as tarefa
+                {self.queue_table} as tarefa
             where
                 tarefa.payload_hash = %(payload_hash)s
                 and chave_externa = %(chave_externa)s
                 and tarefa.status in %(status)s
         """
 
         result, _ = self.db.execute(
```

### Comparing `nsj_queue_lib-0.1.2/nsj_queue_lib/worker_base.py` & `nsj_queue_lib-0.1.3/nsj_queue_lib/worker_base.py`

 * *Files identical despite different names*

### Comparing `nsj_queue_lib-0.1.2/nsj_queue_lib.egg-info/PKG-INFO` & `nsj_queue_lib-0.1.3/nsj_queue_lib.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nsj-queue-lib
-Version: 0.1.2
+Version: 0.1.3
 Summary: Biblioteca para facilitar a implementação de filas e workers.
 Home-page: https://github.com/Nasajon/nsj-queue-lib
 Author: Nasajon Sistemas
 Author-email: contact.dev@nasajon.com.br
 Project-URL: Source, https://github.com/Nasajon/nsj-queue-lib
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
```

### Comparing `nsj_queue_lib-0.1.2/nsj_queue_lib.egg-info/SOURCES.txt` & `nsj_queue_lib-0.1.3/nsj_queue_lib.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `nsj_queue_lib-0.1.2/setup.cfg` & `nsj_queue_lib-0.1.3/setup.cfg`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = nsj_queue_lib
-version = 0.1.2
+version = 0.1.3
 author = Nasajon Sistemas
 author_email = contact.dev@nasajon.com.br
 description = Biblioteca para facilitar a implementação de filas e workers.
 long_description = file: README.md
 long_description_content_type = text/markdown
 url = https://github.com/Nasajon/nsj-queue-lib
 project_urls =
```

### Comparing `nsj_queue_lib-0.1.2/tests/test_push_notification.py` & `nsj_queue_lib-0.1.3/tests/test_push_notification.py`

 * *Files identical despite different names*

