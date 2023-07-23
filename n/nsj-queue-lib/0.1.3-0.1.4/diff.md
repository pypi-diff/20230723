# Comparing `tmp/nsj_queue_lib-0.1.3.tar.gz` & `tmp/nsj_queue_lib-0.1.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nsj_queue_lib-0.1.3.tar", last modified: Sun Jul 23 00:04:36 2023, max compression
+gzip compressed data, was "nsj_queue_lib-0.1.4.tar", last modified: Sun Jul 23 00:11:20 2023, max compression
```

## Comparing `nsj_queue_lib-0.1.3.tar` & `nsj_queue_lib-0.1.4.tar`

### file list

```diff
@@ -1,27 +1,27 @@
-drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-23 00:04:36.986728 nsj_queue_lib-0.1.3/
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     2542 2023-07-23 00:04:36.986728 nsj_queue_lib-0.1.3/PKG-INFO
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     1976 2023-07-21 22:40:47.000000 nsj_queue_lib-0.1.3/README.md
-drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-23 00:04:36.986728 nsj_queue_lib-0.1.3/nsj_queue_lib/
--rw-rw-r--   0 sergio    (1000) sergio    (1000)        0 2023-07-19 18:24:10.000000 nsj_queue_lib-0.1.3/nsj_queue_lib/__init__.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)       45 2023-07-19 18:24:10.000000 nsj_queue_lib-0.1.3/nsj_queue_lib/exception.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     1090 2023-07-22 22:37:18.000000 nsj_queue_lib-0.1.3/nsj_queue_lib/lock_dao.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     7337 2023-07-22 23:56:41.000000 nsj_queue_lib-0.1.3/nsj_queue_lib/main_thread.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     3938 2023-07-22 23:56:52.000000 nsj_queue_lib-0.1.3/nsj_queue_lib/notify_thread.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     3243 2023-07-22 23:57:02.000000 nsj_queue_lib-0.1.3/nsj_queue_lib/purge_thread.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     2879 2023-07-22 23:57:12.000000 nsj_queue_lib-0.1.3/nsj_queue_lib/queue_client.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     4913 2023-07-22 23:57:41.000000 nsj_queue_lib-0.1.3/nsj_queue_lib/retry_thread.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     3827 2023-07-22 20:27:57.000000 nsj_queue_lib-0.1.3/nsj_queue_lib/retry_util.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     1824 2023-07-19 18:24:10.000000 nsj_queue_lib-0.1.3/nsj_queue_lib/settings.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     7252 2023-07-22 23:56:10.000000 nsj_queue_lib-0.1.3/nsj_queue_lib/tarefa_dao.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)      860 2023-07-19 18:24:10.000000 nsj_queue_lib-0.1.3/nsj_queue_lib/worker_base.py
--rw-rw-r--   0 sergio    (1000) sergio    (1000)      252 2023-07-22 18:37:53.000000 nsj_queue_lib-0.1.3/nsj_queue_lib/worker_fila_teste.py
-drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-23 00:04:36.986728 nsj_queue_lib-0.1.3/nsj_queue_lib.egg-info/
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     2542 2023-07-23 00:04:36.000000 nsj_queue_lib-0.1.3/nsj_queue_lib.egg-info/PKG-INFO
--rw-rw-r--   0 sergio    (1000) sergio    (1000)      661 2023-07-23 00:04:36.000000 nsj_queue_lib-0.1.3/nsj_queue_lib.egg-info/SOURCES.txt
--rw-rw-r--   0 sergio    (1000) sergio    (1000)        1 2023-07-23 00:04:36.000000 nsj_queue_lib-0.1.3/nsj_queue_lib.egg-info/dependency_links.txt
--rw-rw-r--   0 sergio    (1000) sergio    (1000)       64 2023-07-23 00:04:36.000000 nsj_queue_lib-0.1.3/nsj_queue_lib.egg-info/requires.txt
--rw-rw-r--   0 sergio    (1000) sergio    (1000)       14 2023-07-23 00:04:36.000000 nsj_queue_lib-0.1.3/nsj_queue_lib.egg-info/top_level.txt
--rw-rw-r--   0 sergio    (1000) sergio    (1000)      103 2023-07-21 22:32:09.000000 nsj_queue_lib-0.1.3/pyproject.toml
--rw-rw-r--   0 sergio    (1000) sergio    (1000)      786 2023-07-23 00:04:36.986728 nsj_queue_lib-0.1.3/setup.cfg
-drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-23 00:04:36.986728 nsj_queue_lib-0.1.3/tests/
--rw-rw-r--   0 sergio    (1000) sergio    (1000)     1324 2023-07-22 22:40:40.000000 nsj_queue_lib-0.1.3/tests/test_push_notification.py
+drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-23 00:11:20.698797 nsj_queue_lib-0.1.4/
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     2542 2023-07-23 00:11:20.698797 nsj_queue_lib-0.1.4/PKG-INFO
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     1976 2023-07-21 22:40:47.000000 nsj_queue_lib-0.1.4/README.md
+drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-23 00:11:20.698797 nsj_queue_lib-0.1.4/nsj_queue_lib/
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)        0 2023-07-19 18:24:10.000000 nsj_queue_lib-0.1.4/nsj_queue_lib/__init__.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)       45 2023-07-19 18:24:10.000000 nsj_queue_lib-0.1.4/nsj_queue_lib/exception.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     1090 2023-07-22 22:37:18.000000 nsj_queue_lib-0.1.4/nsj_queue_lib/lock_dao.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     7337 2023-07-22 23:56:41.000000 nsj_queue_lib-0.1.4/nsj_queue_lib/main_thread.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     3938 2023-07-22 23:56:52.000000 nsj_queue_lib-0.1.4/nsj_queue_lib/notify_thread.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     3243 2023-07-22 23:57:02.000000 nsj_queue_lib-0.1.4/nsj_queue_lib/purge_thread.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     2914 2023-07-23 00:11:01.000000 nsj_queue_lib-0.1.4/nsj_queue_lib/queue_client.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     4913 2023-07-22 23:57:41.000000 nsj_queue_lib-0.1.4/nsj_queue_lib/retry_thread.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     3827 2023-07-22 20:27:57.000000 nsj_queue_lib-0.1.4/nsj_queue_lib/retry_util.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     1824 2023-07-19 18:24:10.000000 nsj_queue_lib-0.1.4/nsj_queue_lib/settings.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     7252 2023-07-22 23:56:10.000000 nsj_queue_lib-0.1.4/nsj_queue_lib/tarefa_dao.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)      860 2023-07-19 18:24:10.000000 nsj_queue_lib-0.1.4/nsj_queue_lib/worker_base.py
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)      252 2023-07-22 18:37:53.000000 nsj_queue_lib-0.1.4/nsj_queue_lib/worker_fila_teste.py
+drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-23 00:11:20.698797 nsj_queue_lib-0.1.4/nsj_queue_lib.egg-info/
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     2542 2023-07-23 00:11:20.000000 nsj_queue_lib-0.1.4/nsj_queue_lib.egg-info/PKG-INFO
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)      661 2023-07-23 00:11:20.000000 nsj_queue_lib-0.1.4/nsj_queue_lib.egg-info/SOURCES.txt
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)        1 2023-07-23 00:11:20.000000 nsj_queue_lib-0.1.4/nsj_queue_lib.egg-info/dependency_links.txt
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)       64 2023-07-23 00:11:20.000000 nsj_queue_lib-0.1.4/nsj_queue_lib.egg-info/requires.txt
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)       14 2023-07-23 00:11:20.000000 nsj_queue_lib-0.1.4/nsj_queue_lib.egg-info/top_level.txt
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)      103 2023-07-21 22:32:09.000000 nsj_queue_lib-0.1.4/pyproject.toml
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)      786 2023-07-23 00:11:20.698797 nsj_queue_lib-0.1.4/setup.cfg
+drwxrwxr-x   0 sergio    (1000) sergio    (1000)        0 2023-07-23 00:11:20.698797 nsj_queue_lib-0.1.4/tests/
+-rw-rw-r--   0 sergio    (1000) sergio    (1000)     1324 2023-07-22 22:40:40.000000 nsj_queue_lib-0.1.4/tests/test_push_notification.py
```

### Comparing `nsj_queue_lib-0.1.3/PKG-INFO` & `nsj_queue_lib-0.1.4/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nsj_queue_lib
-Version: 0.1.3
+Version: 0.1.4
 Summary: Biblioteca para facilitar a implementação de filas e workers.
 Home-page: https://github.com/Nasajon/nsj-queue-lib
 Author: Nasajon Sistemas
 Author-email: contact.dev@nasajon.com.br
 Project-URL: Source, https://github.com/Nasajon/nsj-queue-lib
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
```

### Comparing `nsj_queue_lib-0.1.3/README.md` & `nsj_queue_lib-0.1.4/README.md`

 * *Files identical despite different names*

### Comparing `nsj_queue_lib-0.1.3/nsj_queue_lib/lock_dao.py` & `nsj_queue_lib-0.1.4/nsj_queue_lib/lock_dao.py`

 * *Files identical despite different names*

### Comparing `nsj_queue_lib-0.1.3/nsj_queue_lib/main_thread.py` & `nsj_queue_lib-0.1.4/nsj_queue_lib/main_thread.py`

 * *Files identical despite different names*

### Comparing `nsj_queue_lib-0.1.3/nsj_queue_lib/notify_thread.py` & `nsj_queue_lib-0.1.4/nsj_queue_lib/notify_thread.py`

 * *Files identical despite different names*

### Comparing `nsj_queue_lib-0.1.3/nsj_queue_lib/purge_thread.py` & `nsj_queue_lib-0.1.4/nsj_queue_lib/purge_thread.py`

 * *Files identical despite different names*

### Comparing `nsj_queue_lib-0.1.3/nsj_queue_lib/queue_client.py` & `nsj_queue_lib-0.1.4/nsj_queue_lib/queue_client.py`

 * *Files 5% similar despite different names*

```diff
@@ -47,24 +47,23 @@
         origem: str,
         destino: str,
         processo: str,
         chave_externa: str,
         payload: str,
         tenant: int = None,
         grupo_empresarial: str = None,
+        status: list[str] = ["sucesso", "pendente", "agendada"],
     ):
         """
         Lista as tarefas equivalentes, encontradas na fila, contemplando
-        os status sucesso, pendente e agendada.
+        os status recebidos (padrão: sucesso, pendente e agendada).
         """
 
         # Listando as tarefas pela chave externa, pelo payload e pelo status
-        tarefas = self._tarefa_dao.list_equivalent(
-            chave_externa, payload, ["sucesso", "pendente", "agendada"]
-        )
+        tarefas = self._tarefa_dao.list_equivalent(chave_externa, payload, status)
 
         # Inserinfo a tarefa
         return [
             t
             for t in tarefas
             if origem == t["origem"]
             and destino == t["destino"]
```

### Comparing `nsj_queue_lib-0.1.3/nsj_queue_lib/retry_thread.py` & `nsj_queue_lib-0.1.4/nsj_queue_lib/retry_thread.py`

 * *Files identical despite different names*

### Comparing `nsj_queue_lib-0.1.3/nsj_queue_lib/retry_util.py` & `nsj_queue_lib-0.1.4/nsj_queue_lib/retry_util.py`

 * *Files identical despite different names*

### Comparing `nsj_queue_lib-0.1.3/nsj_queue_lib/settings.py` & `nsj_queue_lib-0.1.4/nsj_queue_lib/settings.py`

 * *Files identical despite different names*

### Comparing `nsj_queue_lib-0.1.3/nsj_queue_lib/tarefa_dao.py` & `nsj_queue_lib-0.1.4/nsj_queue_lib/tarefa_dao.py`

 * *Files identical despite different names*

### Comparing `nsj_queue_lib-0.1.3/nsj_queue_lib/worker_base.py` & `nsj_queue_lib-0.1.4/nsj_queue_lib/worker_base.py`

 * *Files identical despite different names*

### Comparing `nsj_queue_lib-0.1.3/nsj_queue_lib.egg-info/PKG-INFO` & `nsj_queue_lib-0.1.4/nsj_queue_lib.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nsj-queue-lib
-Version: 0.1.3
+Version: 0.1.4
 Summary: Biblioteca para facilitar a implementação de filas e workers.
 Home-page: https://github.com/Nasajon/nsj-queue-lib
 Author: Nasajon Sistemas
 Author-email: contact.dev@nasajon.com.br
 Project-URL: Source, https://github.com/Nasajon/nsj-queue-lib
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
```

### Comparing `nsj_queue_lib-0.1.3/nsj_queue_lib.egg-info/SOURCES.txt` & `nsj_queue_lib-0.1.4/nsj_queue_lib.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `nsj_queue_lib-0.1.3/setup.cfg` & `nsj_queue_lib-0.1.4/setup.cfg`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = nsj_queue_lib
-version = 0.1.3
+version = 0.1.4
 author = Nasajon Sistemas
 author_email = contact.dev@nasajon.com.br
 description = Biblioteca para facilitar a implementação de filas e workers.
 long_description = file: README.md
 long_description_content_type = text/markdown
 url = https://github.com/Nasajon/nsj-queue-lib
 project_urls =
```

### Comparing `nsj_queue_lib-0.1.3/tests/test_push_notification.py` & `nsj_queue_lib-0.1.4/tests/test_push_notification.py`

 * *Files identical despite different names*

