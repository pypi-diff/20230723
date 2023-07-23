# Comparing `tmp/suanpan-sprt-0.6.6.tar.gz` & `tmp/suanpan-sprt-0.6.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/suanpan-sprt-0.6.6.tar", last modified: Sat Jul 22 10:21:55 2023, max compression
+gzip compressed data, was "dist/suanpan-sprt-0.6.7.tar", last modified: Sun Jul 23 08:10:41 2023, max compression
```

## Comparing `suanpan-sprt-0.6.6.tar` & `suanpan-sprt-0.6.7.tar`

### file list

```diff
@@ -1,26 +1,26 @@
-drwxrwxr-x   0 gitlab-runner  (1003) gitlab-runner  (1003)        0 2023-07-22 10:21:55.000000 suanpan-sprt-0.6.6/
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      482 2023-07-22 10:21:55.000000 suanpan-sprt-0.6.6/PKG-INFO
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      129 2023-07-12 09:08:26.000000 suanpan-sprt-0.6.6/README.md
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)       38 2023-07-22 10:21:55.000000 suanpan-sprt-0.6.6/setup.cfg
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     1073 2023-07-12 09:08:26.000000 suanpan-sprt-0.6.6/setup.py
-drwxrwxr-x   0 gitlab-runner  (1003) gitlab-runner  (1003)        0 2023-07-22 10:21:55.000000 suanpan-sprt-0.6.6/sprt/
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      100 2023-07-12 09:08:26.000000 suanpan-sprt-0.6.6/sprt/__init__.py
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     4337 2023-07-18 09:03:49.000000 suanpan-sprt-0.6.6/sprt/__main__.py
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     8168 2023-07-12 09:08:26.000000 suanpan-sprt-0.6.6/sprt/arguments.py
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     1251 2023-07-12 09:08:26.000000 suanpan-sprt-0.6.6/sprt/envs.py
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      242 2023-07-12 09:08:26.000000 suanpan-sprt-0.6.6/sprt/exceptions.py
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     6021 2023-07-22 10:21:55.000000 suanpan-sprt-0.6.6/sprt/loader.py
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     2087 2023-07-17 07:00:31.000000 suanpan-sprt-0.6.6/sprt/log.py
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      903 2023-07-22 10:21:55.000000 suanpan-sprt-0.6.6/sprt/master.py
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     6917 2023-07-22 10:21:55.000000 suanpan-sprt-0.6.6/sprt/server.py
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     6419 2023-07-12 09:08:26.000000 suanpan-sprt-0.6.6/sprt/storage.py
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     3261 2023-07-12 09:08:26.000000 suanpan-sprt-0.6.6/sprt/testing.py
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     1290 2023-07-12 09:08:26.000000 suanpan-sprt-0.6.6/sprt/utils.py
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)       22 2023-07-22 10:21:55.000000 suanpan-sprt-0.6.6/sprt/version.py
-drwxrwxr-x   0 gitlab-runner  (1003) gitlab-runner  (1003)        0 2023-07-22 10:21:55.000000 suanpan-sprt-0.6.6/suanpan_sprt.egg-info/
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      482 2023-07-22 10:21:55.000000 suanpan-sprt-0.6.6/suanpan_sprt.egg-info/PKG-INFO
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      439 2023-07-22 10:21:55.000000 suanpan-sprt-0.6.6/suanpan_sprt.egg-info/SOURCES.txt
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)        1 2023-07-22 10:21:55.000000 suanpan-sprt-0.6.6/suanpan_sprt.egg-info/dependency_links.txt
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)       70 2023-07-22 10:21:55.000000 suanpan-sprt-0.6.6/suanpan_sprt.egg-info/entry_points.txt
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      158 2023-07-22 10:21:55.000000 suanpan-sprt-0.6.6/suanpan_sprt.egg-info/requires.txt
--rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)        5 2023-07-22 10:21:55.000000 suanpan-sprt-0.6.6/suanpan_sprt.egg-info/top_level.txt
+drwxrwxr-x   0 gitlab-runner  (1003) gitlab-runner  (1003)        0 2023-07-23 08:10:41.000000 suanpan-sprt-0.6.7/
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      482 2023-07-23 08:10:41.000000 suanpan-sprt-0.6.7/PKG-INFO
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      129 2023-07-12 09:08:26.000000 suanpan-sprt-0.6.7/README.md
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)       38 2023-07-23 08:10:41.000000 suanpan-sprt-0.6.7/setup.cfg
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     1073 2023-07-12 09:08:26.000000 suanpan-sprt-0.6.7/setup.py
+drwxrwxr-x   0 gitlab-runner  (1003) gitlab-runner  (1003)        0 2023-07-23 08:10:41.000000 suanpan-sprt-0.6.7/sprt/
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      100 2023-07-12 09:08:26.000000 suanpan-sprt-0.6.7/sprt/__init__.py
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     4337 2023-07-18 09:03:49.000000 suanpan-sprt-0.6.7/sprt/__main__.py
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     8168 2023-07-12 09:08:26.000000 suanpan-sprt-0.6.7/sprt/arguments.py
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     1251 2023-07-12 09:08:26.000000 suanpan-sprt-0.6.7/sprt/envs.py
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      242 2023-07-12 09:08:26.000000 suanpan-sprt-0.6.7/sprt/exceptions.py
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     6021 2023-07-22 10:21:55.000000 suanpan-sprt-0.6.7/sprt/loader.py
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     2136 2023-07-23 08:10:40.000000 suanpan-sprt-0.6.7/sprt/log.py
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      880 2023-07-23 08:10:40.000000 suanpan-sprt-0.6.7/sprt/master.py
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     6917 2023-07-22 10:21:55.000000 suanpan-sprt-0.6.7/sprt/server.py
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     6419 2023-07-12 09:08:26.000000 suanpan-sprt-0.6.7/sprt/storage.py
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     3261 2023-07-12 09:08:26.000000 suanpan-sprt-0.6.7/sprt/testing.py
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)     1290 2023-07-12 09:08:26.000000 suanpan-sprt-0.6.7/sprt/utils.py
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)       22 2023-07-23 08:10:40.000000 suanpan-sprt-0.6.7/sprt/version.py
+drwxrwxr-x   0 gitlab-runner  (1003) gitlab-runner  (1003)        0 2023-07-23 08:10:41.000000 suanpan-sprt-0.6.7/suanpan_sprt.egg-info/
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      482 2023-07-23 08:10:41.000000 suanpan-sprt-0.6.7/suanpan_sprt.egg-info/PKG-INFO
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      439 2023-07-23 08:10:41.000000 suanpan-sprt-0.6.7/suanpan_sprt.egg-info/SOURCES.txt
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)        1 2023-07-23 08:10:41.000000 suanpan-sprt-0.6.7/suanpan_sprt.egg-info/dependency_links.txt
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)       70 2023-07-23 08:10:41.000000 suanpan-sprt-0.6.7/suanpan_sprt.egg-info/entry_points.txt
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)      158 2023-07-23 08:10:41.000000 suanpan-sprt-0.6.7/suanpan_sprt.egg-info/requires.txt
+-rw-rw-r--   0 gitlab-runner  (1003) gitlab-runner  (1003)        5 2023-07-23 08:10:41.000000 suanpan-sprt-0.6.7/suanpan_sprt.egg-info/top_level.txt
```

### Comparing `suanpan-sprt-0.6.6/setup.py` & `suanpan-sprt-0.6.7/setup.py`

 * *Files identical despite different names*

### Comparing `suanpan-sprt-0.6.6/sprt/__main__.py` & `suanpan-sprt-0.6.7/sprt/__main__.py`

 * *Files identical despite different names*

### Comparing `suanpan-sprt-0.6.6/sprt/arguments.py` & `suanpan-sprt-0.6.7/sprt/arguments.py`

 * *Files identical despite different names*

### Comparing `suanpan-sprt-0.6.6/sprt/envs.py` & `suanpan-sprt-0.6.7/sprt/envs.py`

 * *Files identical despite different names*

### Comparing `suanpan-sprt-0.6.6/sprt/loader.py` & `suanpan-sprt-0.6.7/sprt/loader.py`

 * *Files identical despite different names*

### Comparing `suanpan-sprt-0.6.6/sprt/log.py` & `suanpan-sprt-0.6.7/sprt/log.py`

 * *Files 2% similar despite different names*

```diff
@@ -67,11 +67,12 @@
         Closes the socket.
         """
         self.acquire()
         try:
             client = self.client
             if client:
                 self.client = None
+                client.reconnection_attempts = 1
                 client.disconnect()
             super().close()
         finally:
             self.release()
```

### Comparing `suanpan-sprt-0.6.6/sprt/master.py` & `suanpan-sprt-0.6.7/sprt/master.py`

 * *Files 13% similar despite different names*

```diff
@@ -28,15 +28,15 @@
         envs.userSignatureHeaderField: signature_v1(envs.accessSecret, envs.userId),
         envs.userSignVersionHeaderField: "v1",
     }
 
 
 def sio(*args, **kwargs):
     kwargs["headers"] = {**default_headers(), **kwargs.pop("headers", {})}
-    client = socketio.Client(reconnection_attempts=3)
+    client = socketio.Client()
     client.connect(*args, **kwargs)
 
     return client
 
 
 def get_token():
     # TODO: add for oss
```

### Comparing `suanpan-sprt-0.6.6/sprt/server.py` & `suanpan-sprt-0.6.7/sprt/server.py`

 * *Files identical despite different names*

### Comparing `suanpan-sprt-0.6.6/sprt/storage.py` & `suanpan-sprt-0.6.7/sprt/storage.py`

 * *Files identical despite different names*

### Comparing `suanpan-sprt-0.6.6/sprt/testing.py` & `suanpan-sprt-0.6.7/sprt/testing.py`

 * *Files identical despite different names*

### Comparing `suanpan-sprt-0.6.6/sprt/utils.py` & `suanpan-sprt-0.6.7/sprt/utils.py`

 * *Files identical despite different names*

