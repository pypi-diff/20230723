# Comparing `tmp/gandai-1.2.0.tar.gz` & `tmp/gandai-1.3.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "gandai-1.2.0.tar", last modified: Tue Jun  6 18:45:50 2023, max compression
+gzip compressed data, was "gandai-1.3.0.tar", last modified: Sat Jul 22 20:39:46 2023, max compression
```

## Comparing `gandai-1.2.0.tar` & `gandai-1.3.0.tar`

### file list

```diff
@@ -1,45 +1,51 @@
-drwxr-xr-x   0 parker     (501) staff       (20)        0 2023-06-06 18:45:50.071389 gandai-1.2.0/
--rw-r--r--   0 parker     (501) staff       (20)       26 2023-05-23 11:45:31.000000 gandai-1.2.0/MANIFEST.in
--rw-r--r--   0 parker     (501) staff       (20)      215 2023-06-06 18:45:50.071264 gandai-1.2.0/PKG-INFO
-drwxr-xr-x   0 parker     (501) staff       (20)        0 2023-06-06 18:45:50.065190 gandai-1.2.0/gandai/
--rw-r--r--   0 parker     (501) staff       (20)       45 2023-05-23 11:45:31.000000 gandai-1.2.0/gandai/__init__.py
-drwxr-xr-x   0 parker     (501) staff       (20)        0 2023-06-06 18:45:50.069198 gandai-1.2.0/gandai/__pycache__/
--rw-r--r--   0 parker     (501) staff       (20)      264 2023-05-23 11:53:24.000000 gandai-1.2.0/gandai/__pycache__/__init__.cpython-311.pyc
--rw-r--r--   0 parker     (501) staff       (20)     7464 2023-05-09 01:55:35.000000 gandai-1.2.0/gandai/__pycache__/adapters.cpython-311.pyc
--rw-r--r--   0 parker     (501) staff       (20)     4157 2023-06-06 18:31:07.000000 gandai-1.2.0/gandai/__pycache__/auth.cpython-311.pyc
--rw-r--r--   0 parker     (501) staff       (20)     4039 2023-06-06 18:24:16.000000 gandai-1.2.0/gandai/__pycache__/datastore.cpython-311.pyc
--rw-r--r--   0 parker     (501) staff       (20)     2016 2023-06-06 18:08:14.000000 gandai-1.2.0/gandai/__pycache__/db.cpython-311.pyc
--rw-r--r--   0 parker     (501) staff       (20)     5979 2023-05-05 21:52:33.000000 gandai-1.2.0/gandai/__pycache__/grata.cpython-311.pyc
--rw-r--r--   0 parker     (501) staff       (20)     4131 2023-05-23 12:17:36.000000 gandai-1.2.0/gandai/__pycache__/main.cpython-311.pyc
--rw-r--r--   0 parker     (501) staff       (20)     6153 2023-05-23 11:53:24.000000 gandai-1.2.0/gandai/__pycache__/models.cpython-311.pyc
--rw-r--r--   0 parker     (501) staff       (20)    22092 2023-05-23 12:27:15.000000 gandai-1.2.0/gandai/__pycache__/query.cpython-311.pyc
--rw-r--r--   0 parker     (501) staff       (20)     1997 2023-06-06 18:17:51.000000 gandai-1.2.0/gandai/__pycache__/secrets.cpython-311.pyc
--rw-r--r--   0 parker     (501) staff       (20)     3403 2023-05-01 00:06:24.000000 gandai-1.2.0/gandai/__pycache__/services.cpython-311.pyc
--rw-r--r--   0 parker     (501) staff       (20)     8063 2023-06-06 18:28:45.000000 gandai-1.2.0/gandai/__pycache__/sources.cpython-311.pyc
--rw-r--r--   0 parker     (501) staff       (20)     1794 2023-06-06 18:31:06.000000 gandai-1.2.0/gandai/auth.py
--rw-r--r--   0 parker     (501) staff       (20)     1500 2023-06-06 18:24:12.000000 gandai-1.2.0/gandai/datastore.py
--rw-r--r--   0 parker     (501) staff       (20)     1205 2023-06-06 18:08:11.000000 gandai-1.2.0/gandai/db.py
--rw-r--r--   0 parker     (501) staff       (20)     2860 2023-05-23 12:17:34.000000 gandai-1.2.0/gandai/main.py
-drwxr-xr-x   0 parker     (501) staff       (20)        0 2023-06-06 18:45:50.069899 gandai-1.2.0/gandai/migrations/
--rw-r--r--   0 parker     (501) staff       (20)        0 2023-04-10 12:18:33.000000 gandai-1.2.0/gandai/migrations/__init__.py
-drwxr-xr-x   0 parker     (501) staff       (20)        0 2023-06-06 18:45:50.070315 gandai-1.2.0/gandai/migrations/__pycache__/
--rw-r--r--   0 parker     (501) staff       (20)      190 2023-05-13 21:27:35.000000 gandai-1.2.0/gandai/migrations/__pycache__/__init__.cpython-311.pyc
--rw-r--r--   0 parker     (501) staff       (20)     6432 2023-05-23 12:06:36.000000 gandai-1.2.0/gandai/migrations/__pycache__/dealcloud.cpython-311.pyc
--rw-r--r--   0 parker     (501) staff       (20)      409 2023-05-23 11:45:31.000000 gandai-1.2.0/gandai/migrations/db_create.py
--rw-r--r--   0 parker     (501) staff       (20)     1655 2023-06-06 18:34:56.000000 gandai-1.2.0/gandai/migrations/db_seed.py
--rw-r--r--   0 parker     (501) staff       (20)     3257 2023-05-23 11:45:31.000000 gandai-1.2.0/gandai/migrations/dealcloud.py
-drwxr-xr-x   0 parker     (501) staff       (20)        0 2023-06-06 18:45:50.070991 gandai-1.2.0/gandai/migrations/sql/
--rw-r--r--   0 parker     (501) staff       (20)      168 2023-05-23 16:11:22.000000 gandai-1.2.0/gandai/migrations/sql/2305023-alter.sql
--rw-r--r--   0 parker     (501) staff       (20)     2924 2023-05-23 15:19:19.000000 gandai-1.2.0/gandai/migrations/sql/schema.sql
--rw-r--r--   0 parker     (501) staff       (20)     2652 2023-05-23 11:45:31.000000 gandai-1.2.0/gandai/models.py
--rw-r--r--   0 parker     (501) staff       (20)    12867 2023-05-23 12:27:14.000000 gandai-1.2.0/gandai/query.py
--rw-r--r--   0 parker     (501) staff       (20)      965 2023-06-06 18:14:26.000000 gandai-1.2.0/gandai/secrets.py
--rw-r--r--   0 parker     (501) staff       (20)     5534 2023-06-06 18:13:42.000000 gandai-1.2.0/gandai/sources.py
-drwxr-xr-x   0 parker     (501) staff       (20)        0 2023-06-06 18:45:50.065780 gandai-1.2.0/gandai.egg-info/
--rw-r--r--   0 parker     (501) staff       (20)      215 2023-06-06 18:45:50.000000 gandai-1.2.0/gandai.egg-info/PKG-INFO
--rw-r--r--   0 parker     (501) staff       (20)     1116 2023-06-06 18:45:50.000000 gandai-1.2.0/gandai.egg-info/SOURCES.txt
--rw-r--r--   0 parker     (501) staff       (20)        1 2023-06-06 18:45:50.000000 gandai-1.2.0/gandai.egg-info/dependency_links.txt
--rw-r--r--   0 parker     (501) staff       (20)        7 2023-06-06 18:45:50.000000 gandai-1.2.0/gandai.egg-info/top_level.txt
--rw-r--r--   0 parker     (501) staff       (20)      384 2023-06-06 18:43:29.000000 gandai-1.2.0/pyproject.toml
--rw-r--r--   0 parker     (501) staff       (20)       38 2023-06-06 18:45:50.071420 gandai-1.2.0/setup.cfg
--rw-r--r--   0 parker     (501) staff       (20)      159 2023-03-06 14:38:11.000000 gandai-1.2.0/setup.py
+drwxr-xr-x   0 parker     (501) staff       (20)        0 2023-07-22 20:39:46.316356 gandai-1.3.0/
+-rw-r--r--   0 parker     (501) staff       (20)       26 2023-05-23 11:45:31.000000 gandai-1.3.0/MANIFEST.in
+-rw-r--r--   0 parker     (501) staff       (20)      214 2023-07-22 20:39:46.316223 gandai-1.3.0/PKG-INFO
+drwxr-xr-x   0 parker     (501) staff       (20)        0 2023-07-22 20:39:46.309959 gandai-1.3.0/gandai/
+-rw-r--r--   0 parker     (501) staff       (20)       46 2023-07-17 18:25:43.000000 gandai-1.3.0/gandai/__init__.py
+drwxr-xr-x   0 parker     (501) staff       (20)        0 2023-07-22 20:39:46.314229 gandai-1.3.0/gandai/__pycache__/
+-rw-r--r--   0 parker     (501) staff       (20)      264 2023-07-17 18:43:09.000000 gandai-1.3.0/gandai/__pycache__/__init__.cpython-311.pyc
+-rw-r--r--   0 parker     (501) staff       (20)     7464 2023-05-09 01:55:35.000000 gandai-1.3.0/gandai/__pycache__/adapters.cpython-311.pyc
+-rw-r--r--   0 parker     (501) staff       (20)     2295 2023-07-19 22:26:33.000000 gandai-1.3.0/gandai/__pycache__/analytics.cpython-311.pyc
+-rw-r--r--   0 parker     (501) staff       (20)     4305 2023-07-19 22:26:35.000000 gandai-1.3.0/gandai/__pycache__/auth.cpython-311.pyc
+-rw-r--r--   0 parker     (501) staff       (20)     4039 2023-06-06 18:24:16.000000 gandai-1.3.0/gandai/__pycache__/datastore.cpython-311.pyc
+-rw-r--r--   0 parker     (501) staff       (20)     2014 2023-07-17 18:43:09.000000 gandai-1.3.0/gandai/__pycache__/db.cpython-311.pyc
+-rw-r--r--   0 parker     (501) staff       (20)     2095 2023-07-18 21:07:13.000000 gandai-1.3.0/gandai/__pycache__/gpt.cpython-311.pyc
+-rw-r--r--   0 parker     (501) staff       (20)     5979 2023-05-05 21:52:33.000000 gandai-1.3.0/gandai/__pycache__/grata.cpython-311.pyc
+-rw-r--r--   0 parker     (501) staff       (20)      734 2023-07-17 18:43:09.000000 gandai-1.3.0/gandai/__pycache__/helpers.cpython-311.pyc
+-rw-r--r--   0 parker     (501) staff       (20)     4283 2023-07-19 22:26:35.000000 gandai-1.3.0/gandai/__pycache__/main.cpython-311.pyc
+-rw-r--r--   0 parker     (501) staff       (20)     6151 2023-07-17 18:43:10.000000 gandai-1.3.0/gandai/__pycache__/models.cpython-311.pyc
+-rw-r--r--   0 parker     (501) staff       (20)    29814 2023-07-22 19:52:02.000000 gandai-1.3.0/gandai/__pycache__/query.cpython-311.pyc
+-rw-r--r--   0 parker     (501) staff       (20)     2221 2023-07-17 18:43:09.000000 gandai-1.3.0/gandai/__pycache__/secrets.cpython-311.pyc
+-rw-r--r--   0 parker     (501) staff       (20)     3403 2023-05-01 00:06:24.000000 gandai-1.3.0/gandai/__pycache__/services.cpython-311.pyc
+-rw-r--r--   0 parker     (501) staff       (20)    16053 2023-07-19 18:02:31.000000 gandai-1.3.0/gandai/__pycache__/sources.cpython-311.pyc
+-rw-r--r--   0 parker     (501) staff       (20)     1190 2023-07-17 18:25:43.000000 gandai-1.3.0/gandai/analytics.py
+-rw-r--r--   0 parker     (501) staff       (20)     1822 2023-07-17 18:25:43.000000 gandai-1.3.0/gandai/auth.py
+-rw-r--r--   0 parker     (501) staff       (20)     1492 2023-07-17 18:25:43.000000 gandai-1.3.0/gandai/datastore.py
+-rw-r--r--   0 parker     (501) staff       (20)     1200 2023-07-17 18:25:43.000000 gandai-1.3.0/gandai/db.py
+-rw-r--r--   0 parker     (501) staff       (20)     1025 2023-07-18 20:42:40.000000 gandai-1.3.0/gandai/gpt.py
+-rw-r--r--   0 parker     (501) staff       (20)      220 2023-07-17 18:25:43.000000 gandai-1.3.0/gandai/helpers.py
+-rw-r--r--   0 parker     (501) staff       (20)     2900 2023-07-17 18:25:43.000000 gandai-1.3.0/gandai/main.py
+drwxr-xr-x   0 parker     (501) staff       (20)        0 2023-07-22 20:39:46.315053 gandai-1.3.0/gandai/migrations/
+-rw-r--r--   0 parker     (501) staff       (20)        0 2023-04-10 12:18:33.000000 gandai-1.3.0/gandai/migrations/__init__.py
+drwxr-xr-x   0 parker     (501) staff       (20)        0 2023-07-22 20:39:46.315497 gandai-1.3.0/gandai/migrations/__pycache__/
+-rw-r--r--   0 parker     (501) staff       (20)      190 2023-05-13 21:27:35.000000 gandai-1.3.0/gandai/migrations/__pycache__/__init__.cpython-311.pyc
+-rw-r--r--   0 parker     (501) staff       (20)     6432 2023-05-23 12:06:36.000000 gandai-1.3.0/gandai/migrations/__pycache__/dealcloud.cpython-311.pyc
+-rw-r--r--   0 parker     (501) staff       (20)      412 2023-07-17 18:25:43.000000 gandai-1.3.0/gandai/migrations/db_create.py
+-rw-r--r--   0 parker     (501) staff       (20)     1653 2023-07-17 18:25:43.000000 gandai-1.3.0/gandai/migrations/db_seed.py
+-rw-r--r--   0 parker     (501) staff       (20)     3258 2023-07-17 18:25:43.000000 gandai-1.3.0/gandai/migrations/dealcloud.py
+drwxr-xr-x   0 parker     (501) staff       (20)        0 2023-07-22 20:39:46.316007 gandai-1.3.0/gandai/migrations/sql/
+-rw-r--r--   0 parker     (501) staff       (20)      168 2023-06-07 16:12:27.000000 gandai-1.3.0/gandai/migrations/sql/2305023-alter.sql
+-rw-r--r--   0 parker     (501) staff       (20)     3061 2023-07-17 18:25:43.000000 gandai-1.3.0/gandai/migrations/sql/schema.sql
+-rw-r--r--   0 parker     (501) staff       (20)     2683 2023-07-17 18:25:43.000000 gandai-1.3.0/gandai/models.py
+-rw-r--r--   0 parker     (501) staff       (20)    21175 2023-07-22 19:51:55.000000 gandai-1.3.0/gandai/query.py
+-rw-r--r--   0 parker     (501) staff       (20)     1069 2023-07-17 18:25:43.000000 gandai-1.3.0/gandai/secrets.py
+-rw-r--r--   0 parker     (501) staff       (20)    10781 2023-07-18 21:32:33.000000 gandai-1.3.0/gandai/sources.py
+drwxr-xr-x   0 parker     (501) staff       (20)        0 2023-07-22 20:39:46.310617 gandai-1.3.0/gandai.egg-info/
+-rw-r--r--   0 parker     (501) staff       (20)      214 2023-07-22 20:39:46.000000 gandai-1.3.0/gandai.egg-info/PKG-INFO
+-rw-r--r--   0 parker     (501) staff       (20)     1295 2023-07-22 20:39:46.000000 gandai-1.3.0/gandai.egg-info/SOURCES.txt
+-rw-r--r--   0 parker     (501) staff       (20)        1 2023-07-22 20:39:46.000000 gandai-1.3.0/gandai.egg-info/dependency_links.txt
+-rw-r--r--   0 parker     (501) staff       (20)        7 2023-07-22 20:39:46.000000 gandai-1.3.0/gandai.egg-info/top_level.txt
+-rw-r--r--   0 parker     (501) staff       (20)      383 2023-07-22 20:39:39.000000 gandai-1.3.0/pyproject.toml
+-rw-r--r--   0 parker     (501) staff       (20)       38 2023-07-22 20:39:46.316389 gandai-1.3.0/setup.cfg
+-rw-r--r--   0 parker     (501) staff       (20)      157 2023-07-17 18:25:43.000000 gandai-1.3.0/setup.py
```

### Comparing `gandai-1.2.0/gandai/__pycache__/adapters.cpython-311.pyc` & `gandai-1.3.0/gandai/__pycache__/adapters.cpython-311.pyc`

 * *Files identical despite different names*

### Comparing `gandai-1.2.0/gandai/__pycache__/auth.cpython-311.pyc` & `gandai-1.3.0/gandai/__pycache__/auth.cpython-311.pyc`

 * *Files 10% similar despite different names*

#### Python bytecode

```diff
@@ -1,150 +1,150 @@
 magic:    0xa70d0d0a
-moddate:  0x6a7b7f64 (Tue Jun  6 18:31:06 2023 UTC)
-files sz: 1794
+moddate:  0xa787b564 (Mon Jul 17 18:25:43 2023 UTC)
+files sz: 1822
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 6
    flags     : 0
    code
-      0x9700640064016c005a01640064016c025a02640064026c036d045a046d
-      055a056d065a060100640064036c076d085a080100640064046c096d095a
-      090100640064016c0a5a0a640064056c0b6d0c5a0c0100640064066c0d6d
+      0x9700640064016c005a00640064016c015a01640064026c026d035a036d
+      045a046d055a050100640064036c066d075a070100640064046c086d085a
+      080100640064016c095a0a640064056c0b6d0c5a0c0100640064066c0d6d
       0e5a0e010069005a0f0200650c0200650e6407a6010000ab010000000000
       0000000200650e6408a6010000ab010000000000000000a6020000ab0200
-      000000000000005a1065050200470064098400640aa6020000ab02000000
+      000000000000005a1065040200470064098400640aa6020000ab02000000
       0000000000a6000000ab0000000000000000005a11640b6511640c640166
       04640d84045a12640e6513640c64016604640f84045a1464106513640c65
       116604641184045a1564126513640c65166604641384045a1764015300
      0           0 RESUME                   0
    
      1           2 LOAD_CONST               0 (0)
                  4 LOAD_CONST               1 (None)
-                 6 IMPORT_NAME              0 (pandas)
-                 8 STORE_NAME               1 (pd)
+                 6 IMPORT_NAME              0 (os)
+                 8 STORE_NAME               0 (os)
    
      2          10 LOAD_CONST               0 (0)
                 12 LOAD_CONST               1 (None)
-                14 IMPORT_NAME              2 (random)
-                16 STORE_NAME               2 (random)
+                14 IMPORT_NAME              1 (random)
+                16 STORE_NAME               1 (random)
    
      3          18 LOAD_CONST               0 (0)
                 20 LOAD_CONST               2 (('asdict', 'dataclass', 'field'))
-                22 IMPORT_NAME              3 (dataclasses)
-                24 IMPORT_FROM              4 (asdict)
-                26 STORE_NAME               4 (asdict)
-                28 IMPORT_FROM              5 (dataclass)
-                30 STORE_NAME               5 (dataclass)
-                32 IMPORT_FROM              6 (field)
-                34 STORE_NAME               6 (field)
+                22 IMPORT_NAME              2 (dataclasses)
+                24 IMPORT_FROM              3 (asdict)
+                26 STORE_NAME               3 (asdict)
+                28 IMPORT_FROM              4 (dataclass)
+                30 STORE_NAME               4 (dataclass)
+                32 IMPORT_FROM              5 (field)
+                34 STORE_NAME               5 (field)
                 36 POP_TOP
    
      4          38 LOAD_CONST               0 (0)
                 40 LOAD_CONST               3 (('md5',))
-                42 IMPORT_NAME              7 (hashlib)
-                44 IMPORT_FROM              8 (md5)
-                46 STORE_NAME               8 (md5)
+                42 IMPORT_NAME              6 (hashlib)
+                44 IMPORT_FROM              7 (md5)
+                46 STORE_NAME               7 (md5)
                 48 POP_TOP
    
      5          50 LOAD_CONST               0 (0)
                 52 LOAD_CONST               4 (('time',))
-                54 IMPORT_NAME              9 (time)
-                56 IMPORT_FROM              9 (time)
-                58 STORE_NAME               9 (time)
+                54 IMPORT_NAME              8 (time)
+                56 IMPORT_FROM              8 (time)
+                58 STORE_NAME               8 (time)
                 60 POP_TOP
    
-     6          62 LOAD_CONST               0 (0)
+     7          62 LOAD_CONST               0 (0)
                 64 LOAD_CONST               1 (None)
-                66 IMPORT_NAME             10 (os)
-                68 STORE_NAME              10 (os)
+                66 IMPORT_NAME              9 (pandas)
+                68 STORE_NAME              10 (pd)
    
-     7          70 LOAD_CONST               0 (0)
+     8          70 LOAD_CONST               0 (0)
                 72 LOAD_CONST               5 (('Client',))
                 74 IMPORT_NAME             11 (twilio.rest)
                 76 IMPORT_FROM             12 (Client)
                 78 STORE_NAME              12 (Client)
                 80 POP_TOP
    
-    12          82 LOAD_CONST               0 (0)
+    10          82 LOAD_CONST               0 (0)
                 84 LOAD_CONST               6 (('access_secret_version',))
                 86 IMPORT_NAME             13 (gandai.secrets)
                 88 IMPORT_FROM             14 (access_secret_version)
                 90 STORE_NAME              14 (access_secret_version)
                 92 POP_TOP
    
-    16          94 BUILD_MAP                0
+    17          94 BUILD_MAP                0
                 96 STORE_NAME              15 (ds)
    
-    17          98 PUSH_NULL
+    18          98 PUSH_NULL
                100 LOAD_NAME               12 (Client)
    
-    18         102 PUSH_NULL
+    19         102 PUSH_NULL
                104 LOAD_NAME               14 (access_secret_version)
                106 LOAD_CONST               7 ('TWILIO_APP')
                108 PRECALL                  1
                112 CALL                     1
                122 PUSH_NULL
                124 LOAD_NAME               14 (access_secret_version)
                126 LOAD_CONST               8 ('TWILIO_TOKEN')
                128 PRECALL                  1
                132 CALL                     1
    
-    17         142 PRECALL                  2
+    18         142 PRECALL                  2
                146 CALL                     2
                156 STORE_NAME              16 (twilio_client)
    
-    22         158 LOAD_NAME                5 (dataclass)
+    23         158 LOAD_NAME                4 (dataclass)
    
-    23         160 PUSH_NULL
+    24         160 PUSH_NULL
                162 LOAD_BUILD_CLASS
-               164 LOAD_CONST               9 (<code object Auth, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/auth.py", line 22>)
+               164 LOAD_CONST               9 (<code object Auth, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/auth.py", line 23>)
                166 MAKE_FUNCTION            0
                168 LOAD_CONST              10 ('Auth')
                170 PRECALL                  2
                174 CALL                     2
    
-    22         184 PRECALL                  0
+    23         184 PRECALL                  0
                188 CALL                     0
    
-    23         198 STORE_NAME              17 (Auth)
+    24         198 STORE_NAME              17 (Auth)
    
-    39         200 LOAD_CONST              11 ('auth')
+    40         200 LOAD_CONST              11 ('auth')
                202 LOAD_NAME               17 (Auth)
                204 LOAD_CONST              12 ('return')
                206 LOAD_CONST               1 (None)
                208 BUILD_TUPLE              4
-               210 LOAD_CONST              13 (<code object _send_code, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/auth.py", line 39>)
+               210 LOAD_CONST              13 (<code object _send_code, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/auth.py", line 40>)
                212 MAKE_FUNCTION            4 (annotations)
                214 STORE_NAME              18 (_send_code)
    
-    48         216 LOAD_CONST              14 ('phone')
+    49         216 LOAD_CONST              14 ('phone')
                218 LOAD_NAME               19 (str)
                220 LOAD_CONST              12 ('return')
                222 LOAD_CONST               1 (None)
                224 BUILD_TUPLE              4
-               226 LOAD_CONST              15 (<code object send_code, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/auth.py", line 48>)
+               226 LOAD_CONST              15 (<code object send_code, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/auth.py", line 49>)
                228 MAKE_FUNCTION            4 (annotations)
                230 STORE_NAME              20 (send_code)
    
-    56         232 LOAD_CONST              16 ('code')
+    57         232 LOAD_CONST              16 ('code')
                234 LOAD_NAME               19 (str)
                236 LOAD_CONST              12 ('return')
                238 LOAD_NAME               17 (Auth)
                240 BUILD_TUPLE              4
-               242 LOAD_CONST              17 (<code object authenticate, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/auth.py", line 56>)
+               242 LOAD_CONST              17 (<code object authenticate, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/auth.py", line 57>)
                244 MAKE_FUNCTION            4 (annotations)
                246 STORE_NAME              21 (authenticate)
    
-    68         248 LOAD_CONST              18 ('token')
+    70         248 LOAD_CONST              18 ('token')
                250 LOAD_NAME               19 (str)
                252 LOAD_CONST              12 ('return')
                254 LOAD_NAME               22 (bool)
                256 BUILD_TUPLE              4
-               258 LOAD_CONST              19 (<code object validate, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/auth.py", line 68>)
+               258 LOAD_CONST              19 (<code object validate, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/auth.py", line 70>)
                260 MAKE_FUNCTION            4 (annotations)
                262 STORE_NAME              23 (validate)
                264 LOAD_CONST               1 (None)
                266 RETURN_VALUE
    consts
       0
       None
@@ -162,68 +162,68 @@
          flags     : 0
          code
             0x970065005a0164005a025500020065036401ac02a6010000ab01000000
             00000000005a046505650664033c0000006505650664043c000000650565
             0664053c000000020065036401ac02a6010000ab0100000000000000005a
             076508650664063c000000020065036401ac02a6010000ab010000000000
             0000005a096505650664073c000000640884005a0a64095300
-          22           0 RESUME                   0
+          23           0 RESUME                   0
                        2 LOAD_NAME                0 (__name__)
                        4 STORE_NAME               1 (__module__)
                        6 LOAD_CONST               0 ('Auth')
                        8 STORE_NAME               2 (__qualname__)
                       10 SETUP_ANNOTATIONS
          
-          24          12 PUSH_NULL
+          25          12 PUSH_NULL
                       14 LOAD_NAME                3 (field)
                       16 LOAD_CONST               1 (False)
                       18 KW_NAMES                 2
                       20 PRECALL                  1
                       24 CALL                     1
                       34 STORE_NAME               4 (key)
                       36 LOAD_NAME                5 (str)
                       38 LOAD_NAME                6 (__annotations__)
                       40 LOAD_CONST               3 ('key')
                       42 STORE_SUBSCR
          
-          25          46 LOAD_NAME                5 (str)
+          26          46 LOAD_NAME                5 (str)
                       48 LOAD_NAME                6 (__annotations__)
                       50 LOAD_CONST               4 ('phone')
                       52 STORE_SUBSCR
          
-          26          56 LOAD_NAME                5 (str)
+          27          56 LOAD_NAME                5 (str)
                       58 LOAD_NAME                6 (__annotations__)
                       60 LOAD_CONST               5 ('code')
                       62 STORE_SUBSCR
          
-          27          66 PUSH_NULL
+          28          66 PUSH_NULL
                       68 LOAD_NAME                3 (field)
                       70 LOAD_CONST               1 (False)
                       72 KW_NAMES                 2
                       74 PRECALL                  1
                       78 CALL                     1
                       88 STORE_NAME               7 (expires)
                       90 LOAD_NAME                8 (int)
                       92 LOAD_NAME                6 (__annotations__)
                       94 LOAD_CONST               6 ('expires')
                       96 STORE_SUBSCR
          
-          28         100 PUSH_NULL
+          29         100 PUSH_NULL
                      102 LOAD_NAME                3 (field)
                      104 LOAD_CONST               1 (False)
                      106 KW_NAMES                 2
                      108 PRECALL                  1
                      112 CALL                     1
                      122 STORE_NAME               9 (token)
                      124 LOAD_NAME                5 (str)
                      126 LOAD_NAME                6 (__annotations__)
                      128 LOAD_CONST               7 ('token')
                      130 STORE_SUBSCR
          
-          30         134 LOAD_CONST               8 (<code object __post_init__, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/auth.py", line 30>)
+          31         134 LOAD_CONST               8 (<code object __post_init__, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/auth.py", line 31>)
                      136 MAKE_FUNCTION            0
                      138 STORE_NAME              10 (__post_init__)
                      140 LOAD_CONST               9 (None)
                      142 RETURN_VALUE
          consts
             'Auth'
             False
@@ -249,71 +249,71 @@
                   00000000007c017a0000007c005f06000000000000000064047c006a0300
                   000000000000009b0064057c006a0600000000000000009b009d047c005f
                   0700000000000000007411000000000000000000007c006a070000000000
                   000000a0090000000000000000000000000000000000000000a6000000ab
                   000000000000000000a6010000ab010000000000000000a00a0000000000
                   000000000000000000000000000000a6000000ab0000000000000000007c
                   005f0b000000000000000064005300
-                30           0 RESUME                   0
+                31           0 RESUME                   0
                
-                31           2 LOAD_GLOBAL              1 (NULL + len)
+                32           2 LOAD_GLOBAL              1 (NULL + len)
                             14 LOAD_GLOBAL              3 (NULL + str)
                             26 LOAD_FAST                0 (self)
                             28 LOAD_ATTR                2 (code)
                             38 PRECALL                  1
                             42 CALL                     1
                             52 PRECALL                  1
                             56 CALL                     1
                             66 LOAD_CONST               1 (6)
                             68 COMPARE_OP               2 (==)
                             74 POP_JUMP_FORWARD_IF_TRUE     2 (to 80)
                             76 LOAD_ASSERTION_ERROR
                             78 RAISE_VARARGS            1
                
-                32     >>   80 LOAD_GLOBAL              1 (NULL + len)
+                33     >>   80 LOAD_GLOBAL              1 (NULL + len)
                             92 LOAD_GLOBAL              3 (NULL + str)
                            104 LOAD_FAST                0 (self)
                            106 LOAD_ATTR                3 (phone)
                            116 PRECALL                  1
                            120 CALL                     1
                            130 PRECALL                  1
                            134 CALL                     1
                            144 LOAD_CONST               2 (10)
                            146 COMPARE_OP               2 (==)
                            152 POP_JUMP_FORWARD_IF_TRUE     2 (to 158)
                            154 LOAD_ASSERTION_ERROR
                            156 RAISE_VARARGS            1
                
-                33     >>  158 LOAD_CONST               3 (604800)
+                34     >>  158 LOAD_CONST               3 (604800)
                            160 STORE_FAST               1 (SEVEN_DAYS)
                
-                34         162 LOAD_GLOBAL              9 (NULL + int)
+                35         162 LOAD_GLOBAL              9 (NULL + int)
                            174 LOAD_GLOBAL             11 (NULL + time)
                            186 PRECALL                  0
                            190 CALL                     0
                            200 PRECALL                  1
                            204 CALL                     1
                            214 LOAD_FAST                1 (SEVEN_DAYS)
                            216 BINARY_OP                0 (+)
                            220 LOAD_FAST                0 (self)
                            222 STORE_ATTR               6 (expires)
                
-                35         232 LOAD_CONST               4 ('auth/')
+                36         232 LOAD_CONST               4 ('auth/')
                            234 LOAD_FAST                0 (self)
                            236 LOAD_ATTR                3 (phone)
                            246 FORMAT_VALUE             0
                            248 LOAD_CONST               5 ('/')
                            250 LOAD_FAST                0 (self)
                            252 LOAD_ATTR                6 (expires)
                            262 FORMAT_VALUE             0
                            264 BUILD_STRING             4
                            266 LOAD_FAST                0 (self)
                            268 STORE_ATTR               7 (key)
                
-                36         278 LOAD_GLOBAL             17 (NULL + md5)
+                37         278 LOAD_GLOBAL             17 (NULL + md5)
                            290 LOAD_FAST                0 (self)
                            292 LOAD_ATTR                7 (key)
                            302 LOAD_METHOD              9 (encode)
                            324 PRECALL                  0
                            328 CALL                     0
                            338 PRECALL                  1
                            342 CALL                     1
@@ -333,137 +333,135 @@
                   '/'
                names      ('len', 'str', 'code', 'phone', 'int', 'time', 'expires', 'key', 'md5', 'encode', 'hexdigest', 'token')
                varnames   ('self', 'SEVEN_DAYS')
                freevars   ()
                cellvars   ()
                filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/auth.py'
                name       '__post_init__'
-               firstlineno 30
+               firstlineno 31
                lnotab 0x02014e014e01040146012e01
             None
          names      ('__name__', '__module__', '__qualname__', 'field', 'key', 'str', '__annotations__', 'expires', 'int', 'token', '__post_init__')
          varnames   ()
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/auth.py'
          name       'Auth'
-         firstlineno 22
+         firstlineno 23
          lnotab 0x0c0222010a010a0122012202
       'Auth'
       'auth'
       'return'
       code
          argcount  : 1
          nlocals   : 2
          stacksize : 6
          flags     : 3
          code
             0x97007400000000000000000000006a010000000000000000a002000000
             00000000000000000000000000000000007c006a03000000000000000074
-            09000000000000000000006a0500000000000000006401a6010000ab0100
-            000000000000007c006a0600000000000000009b0064029d02ac03a60300
-            00ab0300000000000000007d01740f0000000000000000000064047c006a
-            0300000000000000009b009d02a6010000ab010000000000000000010064
-            005300
-          39           0 RESUME                   0
+            09000000000000000000006401a6010000ab0100000000000000007c006a
+            0500000000000000009b0064029d02ac03a6030000ab0300000000000000
+            007d01740d0000000000000000000064047c006a0300000000000000009b
+            009d02a6010000ab010000000000000000010064005300
+          40           0 RESUME                   0
          
-          40           2 LOAD_GLOBAL              0 (twilio_client)
+          41           2 LOAD_GLOBAL              0 (twilio_client)
                       14 LOAD_ATTR                1 (messages)
                       24 LOAD_METHOD              2 (create)
          
-          41          46 LOAD_FAST                0 (auth)
+          42          46 LOAD_FAST                0 (auth)
                       48 LOAD_ATTR                3 (phone)
          
-          42          58 LOAD_GLOBAL              9 (NULL + os)
-                      70 LOAD_ATTR                5 (getenv)
-                      80 LOAD_CONST               1 ('TWILIO_NUMBER')
-                      82 PRECALL                  1
-                      86 CALL                     1
-         
-          43          96 LOAD_FAST                0 (auth)
-                      98 LOAD_ATTR                6 (code)
-                     108 FORMAT_VALUE             0
-                     110 LOAD_CONST               2 (' is your GA Research authentication code.')
-                     112 BUILD_STRING             2
-         
-          40         114 KW_NAMES                 3
-                     116 PRECALL                  3
-                     120 CALL                     3
-                     130 STORE_FAST               1 (message)
-         
-          45         132 LOAD_GLOBAL             15 (NULL + print)
-                     144 LOAD_CONST               4 ('Login Sent to ')
-                     146 LOAD_FAST                0 (auth)
-                     148 LOAD_ATTR                3 (phone)
-                     158 FORMAT_VALUE             0
-                     160 BUILD_STRING             2
-                     162 PRECALL                  1
-                     166 CALL                     1
-                     176 POP_TOP
-                     178 LOAD_CONST               0 (None)
-                     180 RETURN_VALUE
+          43          58 LOAD_GLOBAL              9 (NULL + access_secret_version)
+                      70 LOAD_CONST               1 ('TWILIO_NUMBER')
+                      72 PRECALL                  1
+                      76 CALL                     1
+         
+          44          86 LOAD_FAST                0 (auth)
+                      88 LOAD_ATTR                5 (code)
+                      98 FORMAT_VALUE             0
+                     100 LOAD_CONST               2 (' is your TargetSelect authentication code.')
+                     102 BUILD_STRING             2
+         
+          41         104 KW_NAMES                 3
+                     106 PRECALL                  3
+                     110 CALL                     3
+                     120 STORE_FAST               1 (message)
+         
+          46         122 LOAD_GLOBAL             13 (NULL + print)
+                     134 LOAD_CONST               4 ('Login Sent to ')
+                     136 LOAD_FAST                0 (auth)
+                     138 LOAD_ATTR                3 (phone)
+                     148 FORMAT_VALUE             0
+                     150 BUILD_STRING             2
+                     152 PRECALL                  1
+                     156 CALL                     1
+                     166 POP_TOP
+                     168 LOAD_CONST               0 (None)
+                     170 RETURN_VALUE
          consts
             None
             'TWILIO_NUMBER'
-            ' is your GA Research authentication code.'
+            ' is your TargetSelect authentication code.'
             ('to', 'from_', 'body')
             'Login Sent to '
-         names      ('twilio_client', 'messages', 'create', 'phone', 'os', 'getenv', 'code', 'print')
+         names      ('twilio_client', 'messages', 'create', 'phone', 'access_secret_version', 'code', 'print')
          varnames   ('auth', 'message')
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/auth.py'
          name       '_send_code'
-         firstlineno 39
-         lnotab 0x02012c010c01260112fd1205
+         firstlineno 40
+         lnotab 0x02012c010c011c0112fd1205
       'phone'
       code
          argcount  : 1
          nlocals   : 3
          stacksize : 6
          flags     : 3
          code
             0x97007401000000000000000000007403000000000000000000006a0200
             0000000000000064016402a6020000ab020000000000000000a6010000ab
             0100000000000000007d017407000000000000000000007c007c01ac03a6
             020000ab0200000000000000007d027409000000000000000000007c02a6
             010000ab010000000000000000740a000000000000000000007c026a0600
             000000000000003c000000740f000000000000000000007c02a6010000ab
             010000000000000000010064005300
-          48           0 RESUME                   0
+          49           0 RESUME                   0
          
-          50           2 LOAD_GLOBAL              1 (NULL + str)
+          51           2 LOAD_GLOBAL              1 (NULL + str)
                       14 LOAD_GLOBAL              3 (NULL + random)
                       26 LOAD_ATTR                2 (randint)
                       36 LOAD_CONST               1 (100000)
                       38 LOAD_CONST               2 (999999)
                       40 PRECALL                  2
                       44 CALL                     2
                       54 PRECALL                  1
                       58 CALL                     1
                       68 STORE_FAST               1 (auth_code)
          
-          51          70 LOAD_GLOBAL              7 (NULL + Auth)
+          52          70 LOAD_GLOBAL              7 (NULL + Auth)
                       82 LOAD_FAST                0 (phone)
                       84 LOAD_FAST                1 (auth_code)
                       86 KW_NAMES                 3
                       88 PRECALL                  2
                       92 CALL                     2
                      102 STORE_FAST               2 (auth)
          
-          52         104 LOAD_GLOBAL              9 (NULL + asdict)
+          53         104 LOAD_GLOBAL              9 (NULL + asdict)
                      116 LOAD_FAST                2 (auth)
                      118 PRECALL                  1
                      122 CALL                     1
                      132 LOAD_GLOBAL             10 (ds)
                      144 LOAD_FAST                2 (auth)
                      146 LOAD_ATTR                6 (key)
                      156 STORE_SUBSCR
          
-          53         160 LOAD_GLOBAL             15 (NULL + _send_code)
+          54         160 LOAD_GLOBAL             15 (NULL + _send_code)
                      172 LOAD_FAST                2 (auth)
                      174 PRECALL                  1
                      178 CALL                     1
                      188 POP_TOP
                      190 LOAD_CONST               0 (None)
                      192 RETURN_VALUE
          consts
@@ -473,144 +471,172 @@
             ('phone', 'code')
          names      ('str', 'random', 'randint', 'Auth', 'asdict', 'ds', 'key', '_send_code')
          varnames   ('phone', 'auth_code', 'auth')
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/auth.py'
          name       'send_code'
-         firstlineno 48
+         firstlineno 49
          lnotab 0x0202440122013801
       'code'
       code
          argcount  : 1
          nlocals   : 3
          stacksize : 6
          flags     : 3
          code
-            0x9700740000000000000000000000a00100000000000000000000000000
-            000000000000006401a6010000ab01000000000000000064026400850219
-            0000000000000000007d017405000000000000000000006a030000000000
-            000000740000000000000000000000a00400000000000000000000000000
-            000000000000007c01a6010000ab010000000000000000a6010000ab0100
-            000000000000007d027c027c02640319000000000000000000740b000000
-            00000000000000740d00000000000000000000a6000000ab000000000000
-            000000a6010000ab0100000000000000006b040000000019000000000000
-            0000007d027c027c026404190000000000000000007c006b020000000019
-            0000000000000000007d02740f000000000000000000007c02a6010000ab
-            01000000000000000064056b0400000000721c7c02a00800000000000000
-            000000000000000000000000006406ac07a6010000ab0100000000000000
-            00640519000000000000000000530064005300
-          56           0 RESUME                   0
-         
-          57           2 LOAD_GLOBAL              0 (ds)
-                      14 LOAD_METHOD              1 (keys)
-                      36 LOAD_CONST               1 ('auth/')
-                      38 PRECALL                  1
-                      42 CALL                     1
-                      52 LOAD_CONST               2 (1)
-                      54 LOAD_CONST               0 (None)
-                      56 BUILD_SLICE              2
-                      58 BINARY_SUBSCR
-                      68 STORE_FAST               1 (keys)
-         
-          58          70 LOAD_GLOBAL              5 (NULL + pd)
-                      82 LOAD_ATTR                3 (DataFrame)
-                      92 LOAD_GLOBAL              0 (ds)
-                     104 LOAD_METHOD              4 (load_async)
-                     126 LOAD_FAST                1 (keys)
-                     128 PRECALL                  1
-                     132 CALL                     1
-                     142 PRECALL                  1
-                     146 CALL                     1
-                     156 STORE_FAST               2 (df)
-         
-          59         158 LOAD_FAST                2 (df)
-                     160 LOAD_FAST                2 (df)
-                     162 LOAD_CONST               3 ('expires')
-                     164 BINARY_SUBSCR
-                     174 LOAD_GLOBAL             11 (NULL + int)
-                     186 LOAD_GLOBAL             13 (NULL + time)
-                     198 PRECALL                  0
-                     202 CALL                     0
-                     212 PRECALL                  1
-                     216 CALL                     1
-                     226 COMPARE_OP               4 (>)
-                     232 BINARY_SUBSCR
-                     242 STORE_FAST               2 (df)
-         
-          60         244 LOAD_FAST                2 (df)
-                     246 LOAD_FAST                2 (df)
-                     248 LOAD_CONST               4 ('code')
-                     250 BINARY_SUBSCR
-                     260 LOAD_FAST                0 (code)
-                     262 COMPARE_OP               2 (==)
-                     268 BINARY_SUBSCR
-                     278 STORE_FAST               2 (df)
-         
-          61         280 LOAD_GLOBAL             15 (NULL + len)
-                     292 LOAD_FAST                2 (df)
-                     294 PRECALL                  1
-                     298 CALL                     1
-                     308 LOAD_CONST               5 (0)
-                     310 COMPARE_OP               4 (>)
-                     316 POP_JUMP_FORWARD_IF_FALSE    28 (to 374)
-         
-          63         318 LOAD_FAST                2 (df)
-                     320 LOAD_METHOD              8 (to_dict)
-                     342 LOAD_CONST               6 ('records')
-                     344 KW_NAMES                 7
-                     346 PRECALL                  1
-                     350 CALL                     1
-                     360 LOAD_CONST               5 (0)
-                     362 BINARY_SUBSCR
-                     372 RETURN_VALUE
+            0x97007c00a0000000000000000000000000000000000000000000a60000
+            00ab0000000000000000007d00740200000000000000000000a002000000
+            0000000000000000000000000000000000a6000000ab0000000000000000
+            007d017407000000000000000000006a040000000000000000640184007c
+            014400a6000000ab000000000000000000a6010000ab0100000000000000
+            007d027c027c02640219000000000000000000740b000000000000000000
+            00740d00000000000000000000a6000000ab000000000000000000a60100
+            00ab0100000000000000006b0400000000190000000000000000007d027c
+            027c026403190000000000000000007c006b020000000019000000000000
+            0000007d02740f000000000000000000007c02a6010000ab010000000000
+            00000064046b0400000000721c7c02a00800000000000000000000000000
+            000000000000006405ac06a6010000ab0100000000000000006404190000
+            00000000000000530064005300
+          57           0 RESUME                   0
+         
+          58           2 LOAD_FAST                0 (code)
+                       4 LOAD_METHOD              0 (strip)
+                      26 PRECALL                  0
+                      30 CALL                     0
+                      40 STORE_FAST               0 (code)
+         
+          59          42 LOAD_GLOBAL              2 (ds)
+                      54 LOAD_METHOD              2 (keys)
+                      76 PRECALL                  0
+                      80 CALL                     0
+                      90 STORE_FAST               1 (keys)
+         
+          60          92 LOAD_GLOBAL              7 (NULL + pd)
+                     104 LOAD_ATTR                4 (DataFrame)
+                     114 LOAD_CONST               1 (<code object <listcomp>, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/auth.py", line 60>)
+                     116 MAKE_FUNCTION            0
+                     118 LOAD_FAST                1 (keys)
+                     120 GET_ITER
+                     122 PRECALL                  0
+                     126 CALL                     0
+                     136 PRECALL                  1
+                     140 CALL                     1
+                     150 STORE_FAST               2 (df)
+         
+          61         152 LOAD_FAST                2 (df)
+                     154 LOAD_FAST                2 (df)
+                     156 LOAD_CONST               2 ('expires')
+                     158 BINARY_SUBSCR
+                     168 LOAD_GLOBAL             11 (NULL + int)
+                     180 LOAD_GLOBAL             13 (NULL + time)
+                     192 PRECALL                  0
+                     196 CALL                     0
+                     206 PRECALL                  1
+                     210 CALL                     1
+                     220 COMPARE_OP               4 (>)
+                     226 BINARY_SUBSCR
+                     236 STORE_FAST               2 (df)
+         
+          62         238 LOAD_FAST                2 (df)
+                     240 LOAD_FAST                2 (df)
+                     242 LOAD_CONST               3 ('code')
+                     244 BINARY_SUBSCR
+                     254 LOAD_FAST                0 (code)
+                     256 COMPARE_OP               2 (==)
+                     262 BINARY_SUBSCR
+                     272 STORE_FAST               2 (df)
+         
+          63         274 LOAD_GLOBAL             15 (NULL + len)
+                     286 LOAD_FAST                2 (df)
+                     288 PRECALL                  1
+                     292 CALL                     1
+                     302 LOAD_CONST               4 (0)
+                     304 COMPARE_OP               4 (>)
+                     310 POP_JUMP_FORWARD_IF_FALSE    28 (to 368)
+         
+          65         312 LOAD_FAST                2 (df)
+                     314 LOAD_METHOD              8 (to_dict)
+                     336 LOAD_CONST               5 ('records')
+                     338 KW_NAMES                 6
+                     340 PRECALL                  1
+                     344 CALL                     1
+                     354 LOAD_CONST               4 (0)
+                     356 BINARY_SUBSCR
+                     366 RETURN_VALUE
          
-          65     >>  374 LOAD_CONST               0 (None)
-                     376 RETURN_VALUE
+          67     >>  368 LOAD_CONST               0 (None)
+                     370 RETURN_VALUE
          consts
             None
-            'auth/'
-            1
+            code
+               argcount  : 1
+               nlocals   : 2
+               stacksize : 4
+               flags     : 19
+               code
+                  0x970067007c005d0f7d017400000000000000000000007c011900000000
+                  000000000091028c105300
+                60           0 RESUME                   0
+                             2 BUILD_LIST               0
+                             4 LOAD_FAST                0 (.0)
+                       >>    6 FOR_ITER                15 (to 38)
+                             8 STORE_FAST               1 (k)
+                            10 LOAD_GLOBAL              0 (ds)
+                            22 LOAD_FAST                1 (k)
+                            24 BINARY_SUBSCR
+                            34 LIST_APPEND              2
+                            36 JUMP_BACKWARD           16 (to 6)
+                       >>   38 RETURN_VALUE
+               consts
+               names      ('ds',)
+               varnames   ('.0', 'k')
+               freevars   ()
+               cellvars   ()
+               filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/auth.py'
+               name       '<listcomp>'
+               firstlineno 60
+               lnotab 0x
             'expires'
             'code'
             0
             'records'
             ('orient',)
-         names      ('ds', 'keys', 'pd', 'DataFrame', 'load_async', 'int', 'time', 'len', 'to_dict')
+         names      ('strip', 'ds', 'keys', 'pd', 'DataFrame', 'int', 'time', 'len', 'to_dict')
          varnames   ('code', 'keys', 'df')
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/auth.py'
          name       'authenticate'
-         firstlineno 56
-         lnotab 0x0201440158015601240126023802
+         firstlineno 57
+         lnotab 0x0201280132013c015601240126023802
       'token'
       code
          argcount  : 1
          nlocals   : 1
          stacksize : 1
          flags     : 3
          code 0x970064005300
-          68           0 RESUME                   0
+          70           0 RESUME                   0
          
-          69           2 LOAD_CONST               0 (None)
+          71           2 LOAD_CONST               0 (None)
                        4 RETURN_VALUE
          consts
             None
          names      ()
          varnames   ('token',)
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/auth.py'
          name       'validate'
-         firstlineno 68
+         firstlineno 70
          lnotab 0x0201
-   names      ('pandas', 'pd', 'random', 'dataclasses', 'asdict', 'dataclass', 'field', 'hashlib', 'md5', 'time', 'os', 'twilio.rest', 'Client', 'gandai.secrets', 'access_secret_version', 'ds', 'twilio_client', 'Auth', '_send_code', 'str', 'send_code', 'authenticate', 'bool', 'validate')
+   names      ('os', 'random', 'dataclasses', 'asdict', 'dataclass', 'field', 'hashlib', 'md5', 'time', 'pandas', 'pd', 'twilio.rest', 'Client', 'gandai.secrets', 'access_secret_version', 'ds', 'twilio_client', 'Auth', '_send_code', 'str', 'send_code', 'authenticate', 'bool', 'validate')
    varnames   ()
    freevars   ()
    cellvars   ()
    filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/auth.py'
    name       '<module>'
    firstlineno 1
    lnotab
-      0x00ff02010801080114010c010c0108010c050c040401040128ff100502
-      0118ff0e01021010091008100c
+      0x00ff02010801080114010c010c0208010c020c070401040128ff100502
+      0118ff0e01021010091008100d
```

### Comparing `gandai-1.2.0/gandai/__pycache__/datastore.cpython-311.pyc` & `gandai-1.3.0/gandai/__pycache__/datastore.cpython-311.pyc`

 * *Files identical despite different names*

### Comparing `gandai-1.2.0/gandai/__pycache__/db.cpython-311.pyc` & `gandai-1.3.0/gandai/__pycache__/db.cpython-311.pyc`

 * *Files 15% similar despite different names*

#### Python bytecode

```diff
@@ -1,60 +1,60 @@
 magic:    0xa70d0d0a
-moddate:  0x0b767f64 (Tue Jun  6 18:08:11 2023 UTC)
-files sz: 1205
+moddate:  0xa787b564 (Mon Jul 17 18:25:43 2023 UTC)
+files sz: 1200
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 2
    flags     : 0
    code
-      0x9700640064016c005a00640064026c016d025a026d035a030100640064
-      016c045a04640064016c055a05640064036c066d075a070100640465056a
+      0x9700640064016c005a00640064016c015a01640064016c025a02640064
+      026c036d045a046d055a050100640064036c066d075a070100640465026a
       0800000000000000006a0900000000000000006a0a000000000000000066
       02640584045a0b64015300
      0           0 RESUME                   0
    
      1           2 LOAD_CONST               0 (0)
                  4 LOAD_CONST               1 (None)
                  6 IMPORT_NAME              0 (os)
                  8 STORE_NAME               0 (os)
    
      3          10 LOAD_CONST               0 (0)
-                12 LOAD_CONST               2 (('Connector', 'IPTypes'))
-                14 IMPORT_NAME              1 (google.cloud.sql.connector)
-                16 IMPORT_FROM              2 (Connector)
-                18 STORE_NAME               2 (Connector)
-                20 IMPORT_FROM              3 (IPTypes)
-                22 STORE_NAME               3 (IPTypes)
-                24 POP_TOP
+                12 LOAD_CONST               1 (None)
+                14 IMPORT_NAME              1 (pg8000)
+                16 STORE_NAME               1 (pg8000)
    
-     4          26 LOAD_CONST               0 (0)
-                28 LOAD_CONST               1 (None)
-                30 IMPORT_NAME              4 (pg8000)
-                32 STORE_NAME               4 (pg8000)
+     4          18 LOAD_CONST               0 (0)
+                20 LOAD_CONST               1 (None)
+                22 IMPORT_NAME              2 (sqlalchemy)
+                24 STORE_NAME               2 (sqlalchemy)
    
-     6          34 LOAD_CONST               0 (0)
-                36 LOAD_CONST               1 (None)
-                38 IMPORT_NAME              5 (sqlalchemy)
-                40 STORE_NAME               5 (sqlalchemy)
+     5          26 LOAD_CONST               0 (0)
+                28 LOAD_CONST               2 (('Connector', 'IPTypes'))
+                30 IMPORT_NAME              3 (google.cloud.sql.connector)
+                32 IMPORT_FROM              4 (Connector)
+                34 STORE_NAME               4 (Connector)
+                36 IMPORT_FROM              5 (IPTypes)
+                38 STORE_NAME               5 (IPTypes)
+                40 POP_TOP
    
      7          42 LOAD_CONST               0 (0)
                 44 LOAD_CONST               3 (('access_secret_version',))
                 46 IMPORT_NAME              6 (gandai.secrets)
                 48 IMPORT_FROM              7 (access_secret_version)
                 50 STORE_NAME               7 (access_secret_version)
                 52 POP_TOP
    
-     9          54 LOAD_CONST               4 ('return')
-                56 LOAD_NAME                5 (sqlalchemy)
+    10          54 LOAD_CONST               4 ('return')
+                56 LOAD_NAME                2 (sqlalchemy)
                 58 LOAD_ATTR                8 (engine)
                 68 LOAD_ATTR                9 (base)
                 78 LOAD_ATTR               10 (Engine)
                 88 BUILD_TUPLE              2
-                90 LOAD_CONST               5 (<code object connect_with_connector, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/db.py", line 9>)
+                90 LOAD_CONST               5 (<code object connect_with_connector, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/db.py", line 10>)
                 92 MAKE_FUNCTION            4 (annotations)
                 94 STORE_NAME              11 (connect_with_connector)
                 96 LOAD_CONST               1 (None)
                 98 RETURN_VALUE
    consts
       0
       None
@@ -79,15 +79,15 @@
             000000660288028803880466036408840c7d007407000000000000000000
             006a04000000000000000064097c00640a640b640c640dac0ea6060000ab
             0600000000000000007d017c015300
                        0 MAKE_CELL                2 (connector)
                        2 MAKE_CELL                3 (db_pass)
                        4 MAKE_CELL                4 (instance_connection_name)
          
-           9           6 RESUME                   0
+          10           6 RESUME                   0
          
           12           8 LOAD_GLOBAL              1 (NULL + os)
                       20 LOAD_ATTR                1 (getenv)
                       30 LOAD_CONST               1 ('LOCAL_DB')
                       32 LOAD_CONST               2 (False)
                       34 PRECALL                  2
                       38 CALL                     2
@@ -245,19 +245,19 @@
             ('creator', 'pool_size', 'max_overflow', 'pool_timeout', 'pool_recycle')
          names      ('os', 'getenv', 'print', 'sqlalchemy', 'create_engine', 'Connector', 'access_secret_version', 'pg8000', 'dbapi', 'Connection')
          varnames   ('getconn', 'pool')
          freevars   ()
          cellvars   ('connector', 'db_pass', 'instance_connection_name')
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/db.py'
          name       'connect_with_connector'
-         firstlineno 9
+         firstlineno 10
          lnotab
-            0x08032a011e0128021c011e011e011e02320b1601020102010201020102
+            0x08022a011e0128021c011e011e011e02320b1601020102010201020102
             0102fa1208
-   names      ('os', 'google.cloud.sql.connector', 'Connector', 'IPTypes', 'pg8000', 'sqlalchemy', 'gandai.secrets', 'access_secret_version', 'engine', 'base', 'Engine', 'connect_with_connector')
+   names      ('os', 'pg8000', 'sqlalchemy', 'google.cloud.sql.connector', 'Connector', 'IPTypes', 'gandai.secrets', 'access_secret_version', 'engine', 'base', 'Engine', 'connect_with_connector')
    varnames   ()
    freevars   ()
    cellvars   ()
    filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/db.py'
    name       '<module>'
    firstlineno 1
-   lnotab 0x00ff020108021001080208010c02
+   lnotab 0x00ff020108020801080110020c03
```

### Comparing `gandai-1.2.0/gandai/__pycache__/grata.cpython-311.pyc` & `gandai-1.3.0/gandai/__pycache__/grata.cpython-311.pyc`

 * *Files identical despite different names*

### Comparing `gandai-1.2.0/gandai/__pycache__/main.cpython-311.pyc` & `gandai-1.3.0/gandai/__pycache__/main.cpython-311.pyc`

 * *Files 14% similar despite different names*

#### Python bytecode

```diff
@@ -1,160 +1,159 @@
 magic:    0xa70d0d0a
-moddate:  0xdeae6c64 (Tue May 23 12:17:34 2023 UTC)
-files sz: 2860
+moddate:  0xa787b564 (Mon Jul 17 18:25:43 2023 UTC)
+files sz: 2900
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 4
    flags     : 0
    code
-      0x9700640064016c005a01640064026c026d035a030100640064036c046d
-      055a056d065a060100640064046c076d085a080100640064056c096d095a
-      090100640064066c0a6d0b5a0b6d0c5a0c6d0d5a0d0100640064076c0e6d
-      0f5a0f0100640064086c106d115a12010064096513640a64016604640b84
-      045a14640c6513640a65136604640d84045a1564015300
+      0x9700640064016c006d015a010100640064026c026d035a036d045a0401
+      00640064036c056d055a050100640064046c065a07640064056c086d095a
+      090100640064066c0a6d0b5a0b0100640064076c0c6d0d5a0d6d0e5a0e6d
+      0f5a0f0100640064086c106d115a12010064096513640a64046604640b84
+      045a14640c6513640a65136604640d84045a1564045300
      0           0 RESUME                   0
    
      1           2 LOAD_CONST               0 (0)
-                 4 LOAD_CONST               1 (None)
-                 6 IMPORT_NAME              0 (pandas)
-                 8 STORE_NAME               1 (pd)
+                 4 LOAD_CONST               1 (('ThreadPoolExecutor',))
+                 6 IMPORT_NAME              0 (concurrent.futures)
+                 8 IMPORT_FROM              1 (ThreadPoolExecutor)
+                10 STORE_NAME               1 (ThreadPoolExecutor)
+                12 POP_TOP
    
-     2          10 LOAD_CONST               0 (0)
-                12 LOAD_CONST               2 (('from_dict',))
-                14 IMPORT_NAME              2 (dacite)
-                16 IMPORT_FROM              3 (from_dict)
-                18 STORE_NAME               3 (from_dict)
-                20 POP_TOP
+     2          14 LOAD_CONST               0 (0)
+                16 LOAD_CONST               2 (('dataclass', 'field'))
+                18 IMPORT_NAME              2 (dataclasses)
+                20 IMPORT_FROM              3 (dataclass)
+                22 STORE_NAME               3 (dataclass)
+                24 IMPORT_FROM              4 (field)
+                26 STORE_NAME               4 (field)
+                28 POP_TOP
    
-     3          22 LOAD_CONST               0 (0)
-                24 LOAD_CONST               3 (('dataclass', 'field'))
-                26 IMPORT_NAME              4 (dataclasses)
-                28 IMPORT_FROM              5 (dataclass)
-                30 STORE_NAME               5 (dataclass)
-                32 IMPORT_FROM              6 (field)
-                34 STORE_NAME               6 (field)
-                36 POP_TOP
+     3          30 LOAD_CONST               0 (0)
+                32 LOAD_CONST               3 (('time',))
+                34 IMPORT_NAME              5 (time)
+                36 IMPORT_FROM              5 (time)
+                38 STORE_NAME               5 (time)
+                40 POP_TOP
    
-     4          38 LOAD_CONST               0 (0)
-                40 LOAD_CONST               4 (('ThreadPoolExecutor',))
-                42 IMPORT_NAME              7 (concurrent.futures)
-                44 IMPORT_FROM              8 (ThreadPoolExecutor)
-                46 STORE_NAME               8 (ThreadPoolExecutor)
-                48 POP_TOP
+     5          42 LOAD_CONST               0 (0)
+                44 LOAD_CONST               4 (None)
+                46 IMPORT_NAME              6 (pandas)
+                48 STORE_NAME               7 (pd)
    
-     5          50 LOAD_CONST               0 (0)
-                52 LOAD_CONST               5 (('time',))
-                54 IMPORT_NAME              9 (time)
-                56 IMPORT_FROM              9 (time)
-                58 STORE_NAME               9 (time)
+     6          50 LOAD_CONST               0 (0)
+                52 LOAD_CONST               5 (('from_dict',))
+                54 IMPORT_NAME              8 (dacite)
+                56 IMPORT_FROM              9 (from_dict)
+                58 STORE_NAME               9 (from_dict)
                 60 POP_TOP
    
      8          62 LOAD_CONST               0 (0)
-                64 LOAD_CONST               6 (('Event', 'Company', 'Checkpoint'))
-                66 IMPORT_NAME             10 (gandai.models)
-                68 IMPORT_FROM             11 (Event)
-                70 STORE_NAME              11 (Event)
-                72 IMPORT_FROM             12 (Company)
-                74 STORE_NAME              12 (Company)
-                76 IMPORT_FROM             13 (Checkpoint)
-                78 STORE_NAME              13 (Checkpoint)
-                80 POP_TOP
+                64 LOAD_CONST               6 (('query',))
+                66 IMPORT_NAME             10 (gandai)
+                68 IMPORT_FROM             11 (query)
+                70 STORE_NAME              11 (query)
+                72 POP_TOP
    
-     9          82 LOAD_CONST               0 (0)
-                84 LOAD_CONST               7 (('query',))
-                86 IMPORT_NAME             14 (gandai)
-                88 IMPORT_FROM             15 (query)
-                90 STORE_NAME              15 (query)
+     9          74 LOAD_CONST               0 (0)
+                76 LOAD_CONST               7 (('Checkpoint', 'Company', 'Event'))
+                78 IMPORT_NAME             12 (gandai.models)
+                80 IMPORT_FROM             13 (Checkpoint)
+                82 STORE_NAME              13 (Checkpoint)
+                84 IMPORT_FROM             14 (Company)
+                86 STORE_NAME              14 (Company)
+                88 IMPORT_FROM             15 (Event)
+                90 STORE_NAME              15 (Event)
                 92 POP_TOP
    
     10          94 LOAD_CONST               0 (0)
                 96 LOAD_CONST               8 (('GrataWrapper',))
                 98 IMPORT_NAME             16 (gandai.sources)
                100 IMPORT_FROM             17 (GrataWrapper)
                102 STORE_NAME              18 (grata)
                104 POP_TOP
    
     13         106 LOAD_CONST               9 ('event_id')
                108 LOAD_NAME               19 (int)
                110 LOAD_CONST              10 ('return')
-               112 LOAD_CONST               1 (None)
+               112 LOAD_CONST               4 (None)
                114 BUILD_TUPLE              4
                116 LOAD_CONST              11 (<code object process_event, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/main.py", line 13>)
                118 MAKE_FUNCTION            4 (annotations)
                120 STORE_NAME              20 (process_event)
    
     72         122 LOAD_CONST              12 ('search_uid')
                124 LOAD_NAME               19 (int)
                126 LOAD_CONST              10 ('return')
                128 LOAD_NAME               19 (int)
                130 BUILD_TUPLE              4
                132 LOAD_CONST              13 (<code object process_events, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/main.py", line 72>)
                134 MAKE_FUNCTION            4 (annotations)
                136 STORE_NAME              21 (process_events)
-               138 LOAD_CONST               1 (None)
+               138 LOAD_CONST               4 (None)
                140 RETURN_VALUE
    consts
       0
-      None
-      ('from_dict',)
-      ('dataclass', 'field')
       ('ThreadPoolExecutor',)
+      ('dataclass', 'field')
       ('time',)
-      ('Event', 'Company', 'Checkpoint')
+      None
+      ('from_dict',)
       ('query',)
+      ('Checkpoint', 'Company', 'Event')
       ('GrataWrapper',)
       'event_id'
       'return'
       code
          argcount  : 1
          nlocals   : 7
          stacksize : 5
          flags     : 3
          code
             0x97007401000000000000000000006a0100000000000000007c00a60100
             00ab0100000000000000007d017c016a0200000000000000007d027c016a
-            03000000000000000064016b0200000000720290016eee7c016a03000000
-            000000000064026b0200000000900172047401000000000000000000006a
-            0400000000000000007c016a050000000000000000a6010000ab01000000
-            00000000007d03740d000000000000000000007c036a0700000000000000
-            00a0080000000000000000000000000000000000000000a6000000ab0000
-            00000000000000a6010000ab01000000000000000064036b000000000072
-            ae7413000000000000000000006a0a00000000000000007c036a05000000
-            0000000000a6010000ab0100000000000000007d047c04a00b0000000000
-            0000000000000000000000000000006404a6010000ab0100000000000000
-            0064056b020000000072147419000000000000000000007c039b0064069d
-            02a6010000ab010000000000000000010090016e59741900000000000000
-            0000007c04a6010000ab01000000000000000001007c04a00b0000000000
-            0000000000000000000000000000006407a6010000ab0100000000000000
-            007c035f0d00000000000000007c04a00b00000000000000000000000000
-            000000000000006408a6010000ab0100000000000000007c035f0e000000
-            000000000069007c036a070000000000000000a5017c04a5017c035f0700
-            000000000000007401000000000000000000006a0f00000000000000007c
-            03a6010000ab01000000000000000001006ef17419000000000000000000
-            007c039b0064099d02a6010000ab01000000000000000001006ede7c016a
-            030000000000000000640a6b020000000072477401000000000000000000
-            006a1000000000000000007c02a6010000ab0100000000000000007d0574
-            13000000000000000000006a1100000000000000007c016a050000000000
-            0000007c05ac0ba6020000ab0200000000000000007d0674010000000000
-            00000000006a1200000000000000007c067c02640cac0da6030000ab0300
-            0000000000000001006e8c7c016a030000000000000000640e6b02000000
-            0072016e807c016a030000000000000000640f6b020000000072016e747c
-            016a03000000000000000064106b020000000072016e687c016a03000000
-            000000000064116b020000000072016e5c7c016a03000000000000000064
-            126b0200000000725174190000000000000000000064137c029b009d02a6
-            010000ab01000000000000000001007401000000000000000000006a1000
-            000000000000007c02a6010000ab0100000000000000007d057413000000
-            000000000000006a1300000000000000007c05a6010000ab010000000000
-            0000007d067401000000000000000000006a1200000000000000007c067c
-            02640cac0da6030000ab0300000000000000000100740100000000000000
-            0000006a140000000000000000742b000000000000000000007c016a1600
-            00000000000000ac14a6010000ab010000000000000000a6010000ab0100
-            00000000000000010074190000000000000000000064157c019b009d02a6
-            010000ab010000000000000000010064165300
+            03000000000000000064016b0200000000720290016ede7c016a03000000
+            000000000064026b020000000072f57401000000000000000000006a0400
+            000000000000007c016a050000000000000000a6010000ab010000000000
+            0000007d0364037c036a060000000000000000a007000000000000000000
+            0000000000000000000000a6000000ab000000000000000000760172ae74
+            11000000000000000000006a0900000000000000007c036a050000000000
+            000000a6010000ab0100000000000000007d047c04a00a00000000000000
+            000000000000000000000000006404a6010000ab01000000000000000064
+            056b020000000072147417000000000000000000007c039b0064069d02a6
+            010000ab010000000000000000010090016e597417000000000000000000
+            007c04a6010000ab01000000000000000001007c04a00a00000000000000
+            000000000000000000000000006407a6010000ab0100000000000000007c
+            035f0c00000000000000007c04a00a000000000000000000000000000000
+            00000000006408a6010000ab0100000000000000007c035f0d0000000000
+            00000069007c036a060000000000000000a5017c04a5017c035f06000000
+            00000000007401000000000000000000006a0e00000000000000007c03a6
+            010000ab01000000000000000001006ef17417000000000000000000007c
+            039b0064099d02a6010000ab01000000000000000001006ede7c016a0300
+            00000000000000640a6b020000000072477401000000000000000000006a
+            0f00000000000000007c02a6010000ab0100000000000000007d05741100
+            0000000000000000006a1000000000000000007c016a0500000000000000
+            007c05ac0ba6020000ab0200000000000000007d06740100000000000000
+            0000006a1100000000000000007c067c02640cac0da6030000ab03000000
+            000000000001006e8c7c016a030000000000000000640e6b020000000072
+            016e807c016a030000000000000000640f6b020000000072016e747c016a
+            03000000000000000064106b020000000072016e687c016a030000000000
+            00000064116b020000000072016e5c7c016a03000000000000000064126b
+            0200000000725174170000000000000000000064137c029b009d02a60100
+            00ab01000000000000000001007401000000000000000000006a0f000000
+            00000000007c02a6010000ab0100000000000000007d0574110000000000
+            00000000006a1200000000000000007c05a6010000ab0100000000000000
+            007d067401000000000000000000006a1100000000000000007c067c0264
+            0cac0da6030000ab03000000000000000001007401000000000000000000
+            006a1300000000000000007429000000000000000000007c016a15000000
+            0000000000ac14a6010000ab010000000000000000a6010000ab01000000
+            0000000000010074170000000000000000000064157c019b009d02a60100
+            00ab010000000000000000010064165300
           13           0 RESUME                   0
          
           19           2 LOAD_GLOBAL              1 (NULL + query)
                       14 LOAD_ATTR                1 (find_event_by_id)
                       24 LOAD_FAST                0 (event_id)
                       26 PRECALL                  1
                       30 CALL                     1
@@ -167,256 +166,252 @@
           22          56 LOAD_FAST                1 (e)
                       58 LOAD_ATTR                3 (type)
                       68 LOAD_CONST               1 ('create')
                       70 COMPARE_OP               2 (==)
                       76 POP_JUMP_FORWARD_IF_FALSE     2 (to 82)
          
           23          78 EXTENDED_ARG             1
-                      80 JUMP_FORWARD           494 (to 1070)
+                      80 JUMP_FORWARD           478 (to 1038)
          
           24     >>   82 LOAD_FAST                1 (e)
                       84 LOAD_ATTR                3 (type)
                       94 LOAD_CONST               2 ('advance')
                       96 COMPARE_OP               2 (==)
-                     102 EXTENDED_ARG             1
-                     104 POP_JUMP_FORWARD_IF_FALSE   260 (to 626)
+                     102 POP_JUMP_FORWARD_IF_FALSE   245 (to 594)
          
-          26         106 LOAD_GLOBAL              1 (NULL + query)
-                     118 LOAD_ATTR                4 (find_company_by_domain)
-                     128 LOAD_FAST                1 (e)
-                     130 LOAD_ATTR                5 (domain)
-                     140 PRECALL                  1
-                     144 CALL                     1
-                     154 STORE_FAST               3 (company)
-         
-          28         156 LOAD_GLOBAL             13 (NULL + len)
-                     168 LOAD_FAST                3 (company)
-                     170 LOAD_ATTR                7 (meta)
-                     180 LOAD_METHOD              8 (keys)
-                     202 PRECALL                  0
-                     206 CALL                     0
-                     216 PRECALL                  1
-                     220 CALL                     1
-                     230 LOAD_CONST               3 (10)
-                     232 COMPARE_OP               0 (<)
-                     238 POP_JUMP_FORWARD_IF_FALSE   174 (to 588)
-         
-          31         240 LOAD_GLOBAL             19 (NULL + grata)
-                     252 LOAD_ATTR               10 (enrich)
-                     262 LOAD_FAST                3 (company)
-                     264 LOAD_ATTR                5 (domain)
-                     274 PRECALL                  1
-                     278 CALL                     1
-                     288 STORE_FAST               4 (resp)
-         
-          32         290 LOAD_FAST                4 (resp)
-                     292 LOAD_METHOD             11 (get)
-                     314 LOAD_CONST               4 ('status')
-                     316 PRECALL                  1
-                     320 CALL                     1
-                     330 LOAD_CONST               5 (404)
-                     332 COMPARE_OP               2 (==)
-                     338 POP_JUMP_FORWARD_IF_FALSE    20 (to 380)
-         
-          33         340 LOAD_GLOBAL             25 (NULL + print)
-                     352 LOAD_FAST                3 (company)
-                     354 FORMAT_VALUE             0
-                     356 LOAD_CONST               6 (' not found')
-                     358 BUILD_STRING             2
-                     360 PRECALL                  1
-                     364 CALL                     1
-                     374 POP_TOP
-                     376 EXTENDED_ARG             1
-                     378 JUMP_FORWARD           345 (to 1070)
-         
-          35     >>  380 LOAD_GLOBAL             25 (NULL + print)
-                     392 LOAD_FAST                4 (resp)
-                     394 PRECALL                  1
-                     398 CALL                     1
-                     408 POP_TOP
-         
-          36         410 LOAD_FAST                4 (resp)
-                     412 LOAD_METHOD             11 (get)
-                     434 LOAD_CONST               7 ('name')
-                     436 PRECALL                  1
-                     440 CALL                     1
-                     450 LOAD_FAST                3 (company)
-                     452 STORE_ATTR              13 (name)
-         
-          37         462 LOAD_FAST                4 (resp)
-                     464 LOAD_METHOD             11 (get)
-                     486 LOAD_CONST               8 ('description')
-                     488 PRECALL                  1
-                     492 CALL                     1
+          26         104 LOAD_GLOBAL              1 (NULL + query)
+                     116 LOAD_ATTR                4 (find_company_by_domain)
+                     126 LOAD_FAST                1 (e)
+                     128 LOAD_ATTR                5 (domain)
+                     138 PRECALL                  1
+                     142 CALL                     1
+                     152 STORE_FAST               3 (company)
+         
+          28         154 LOAD_CONST               3 ('company_uid')
+                     156 LOAD_FAST                3 (company)
+                     158 LOAD_ATTR                6 (meta)
+                     168 LOAD_METHOD              7 (keys)
+                     190 PRECALL                  0
+                     194 CALL                     0
+                     204 CONTAINS_OP              1
+                     206 POP_JUMP_FORWARD_IF_FALSE   174 (to 556)
+         
+          31         208 LOAD_GLOBAL             17 (NULL + grata)
+                     220 LOAD_ATTR                9 (enrich)
+                     230 LOAD_FAST                3 (company)
+                     232 LOAD_ATTR                5 (domain)
+                     242 PRECALL                  1
+                     246 CALL                     1
+                     256 STORE_FAST               4 (resp)
+         
+          32         258 LOAD_FAST                4 (resp)
+                     260 LOAD_METHOD             10 (get)
+                     282 LOAD_CONST               4 ('status')
+                     284 PRECALL                  1
+                     288 CALL                     1
+                     298 LOAD_CONST               5 (404)
+                     300 COMPARE_OP               2 (==)
+                     306 POP_JUMP_FORWARD_IF_FALSE    20 (to 348)
+         
+          33         308 LOAD_GLOBAL             23 (NULL + print)
+                     320 LOAD_FAST                3 (company)
+                     322 FORMAT_VALUE             0
+                     324 LOAD_CONST               6 (' not found')
+                     326 BUILD_STRING             2
+                     328 PRECALL                  1
+                     332 CALL                     1
+                     342 POP_TOP
+                     344 EXTENDED_ARG             1
+                     346 JUMP_FORWARD           345 (to 1038)
+         
+          35     >>  348 LOAD_GLOBAL             23 (NULL + print)
+                     360 LOAD_FAST                4 (resp)
+                     362 PRECALL                  1
+                     366 CALL                     1
+                     376 POP_TOP
+         
+          36         378 LOAD_FAST                4 (resp)
+                     380 LOAD_METHOD             10 (get)
+                     402 LOAD_CONST               7 ('name')
+                     404 PRECALL                  1
+                     408 CALL                     1
+                     418 LOAD_FAST                3 (company)
+                     420 STORE_ATTR              12 (name)
+         
+          37         430 LOAD_FAST                4 (resp)
+                     432 LOAD_METHOD             10 (get)
+                     454 LOAD_CONST               8 ('description')
+                     456 PRECALL                  1
+                     460 CALL                     1
+                     470 LOAD_FAST                3 (company)
+                     472 STORE_ATTR              13 (description)
+         
+          38         482 BUILD_MAP                0
+                     484 LOAD_FAST                3 (company)
+                     486 LOAD_ATTR                6 (meta)
+                     496 DICT_UPDATE              1
+                     498 LOAD_FAST                4 (resp)
+                     500 DICT_UPDATE              1
                      502 LOAD_FAST                3 (company)
-                     504 STORE_ATTR              14 (description)
+                     504 STORE_ATTR               6 (meta)
          
-          38         514 BUILD_MAP                0
-                     516 LOAD_FAST                3 (company)
-                     518 LOAD_ATTR                7 (meta)
-                     528 DICT_UPDATE              1
-                     530 LOAD_FAST                4 (resp)
-                     532 DICT_UPDATE              1
-                     534 LOAD_FAST                3 (company)
-                     536 STORE_ATTR               7 (meta)
+          39         514 LOAD_GLOBAL              1 (NULL + query)
+                     526 LOAD_ATTR               14 (update_company)
+                     536 LOAD_FAST                3 (company)
+                     538 PRECALL                  1
+                     542 CALL                     1
+                     552 POP_TOP
+                     554 JUMP_FORWARD           241 (to 1038)
          
-          39         546 LOAD_GLOBAL              1 (NULL + query)
-                     558 LOAD_ATTR               15 (update_company)
+          41     >>  556 LOAD_GLOBAL             23 (NULL + print)
                      568 LOAD_FAST                3 (company)
-                     570 PRECALL                  1
-                     574 CALL                     1
-                     584 POP_TOP
-                     586 JUMP_FORWARD           241 (to 1070)
-         
-          41     >>  588 LOAD_GLOBAL             25 (NULL + print)
-                     600 LOAD_FAST                3 (company)
-                     602 FORMAT_VALUE             0
-                     604 LOAD_CONST               9 (' already enriched.')
-                     606 BUILD_STRING             2
-                     608 PRECALL                  1
-                     612 CALL                     1
-                     622 POP_TOP
-                     624 JUMP_FORWARD           222 (to 1070)
-         
-          43     >>  626 LOAD_FAST                1 (e)
-                     628 LOAD_ATTR                3 (type)
-                     638 LOAD_CONST              10 ('validate')
-                     640 COMPARE_OP               2 (==)
-                     646 POP_JUMP_FORWARD_IF_FALSE    71 (to 790)
-         
-          44         648 LOAD_GLOBAL              1 (NULL + query)
-                     660 LOAD_ATTR               16 (find_search_by_uid)
-                     670 LOAD_FAST                2 (search_uid)
-                     672 PRECALL                  1
-                     676 CALL                     1
-                     686 STORE_FAST               5 (search)
-         
-          45         688 LOAD_GLOBAL             19 (NULL + grata)
-                     700 LOAD_ATTR               17 (find_similar)
-                     710 LOAD_FAST                1 (e)
-                     712 LOAD_ATTR                5 (domain)
-                     722 LOAD_FAST                5 (search)
-                     724 KW_NAMES                11
-                     726 PRECALL                  2
-                     730 CALL                     2
-                     740 STORE_FAST               6 (grata_companies)
-         
-          46         742 LOAD_GLOBAL              1 (NULL + query)
-                     754 LOAD_ATTR               18 (insert_companies_as_targets)
-         
-          47         764 LOAD_FAST                6 (grata_companies)
-                     766 LOAD_FAST                2 (search_uid)
-                     768 LOAD_CONST              12 ('grata')
-         
-          46         770 KW_NAMES                13
-                     772 PRECALL                  3
-                     776 CALL                     3
-                     786 POP_TOP
-                     788 JUMP_FORWARD           140 (to 1070)
-         
-          50     >>  790 LOAD_FAST                1 (e)
-                     792 LOAD_ATTR                3 (type)
-                     802 LOAD_CONST              14 ('send')
-                     804 COMPARE_OP               2 (==)
-                     810 POP_JUMP_FORWARD_IF_FALSE     1 (to 814)
-         
-          51         812 JUMP_FORWARD           128 (to 1070)
-         
-          52     >>  814 LOAD_FAST                1 (e)
-                     816 LOAD_ATTR                3 (type)
-                     826 LOAD_CONST              15 ('accept')
-                     828 COMPARE_OP               2 (==)
-                     834 POP_JUMP_FORWARD_IF_FALSE     1 (to 838)
-         
-          53         836 JUMP_FORWARD           116 (to 1070)
-         
-          54     >>  838 LOAD_FAST                1 (e)
-                     840 LOAD_ATTR                3 (type)
-                     850 LOAD_CONST              16 ('reject')
-                     852 COMPARE_OP               2 (==)
-                     858 POP_JUMP_FORWARD_IF_FALSE     1 (to 862)
-         
-          55         860 JUMP_FORWARD           104 (to 1070)
-         
-          56     >>  862 LOAD_FAST                1 (e)
-                     864 LOAD_ATTR                3 (type)
-                     874 LOAD_CONST              17 ('conflict')
-                     876 COMPARE_OP               2 (==)
-                     882 POP_JUMP_FORWARD_IF_FALSE     1 (to 886)
-         
-          57         884 JUMP_FORWARD            92 (to 1070)
-         
-          58     >>  886 LOAD_FAST                1 (e)
-                     888 LOAD_ATTR                3 (type)
-                     898 LOAD_CONST              18 ('criteria')
-                     900 COMPARE_OP               2 (==)
-                     906 POP_JUMP_FORWARD_IF_FALSE    81 (to 1070)
-         
-          59         908 LOAD_GLOBAL             25 (NULL + print)
-                     920 LOAD_CONST              19 ('criteria search for ')
-                     922 LOAD_FAST                2 (search_uid)
-                     924 FORMAT_VALUE             0
-                     926 BUILD_STRING             2
-                     928 PRECALL                  1
-                     932 CALL                     1
-                     942 POP_TOP
-         
-          60         944 LOAD_GLOBAL              1 (NULL + query)
-                     956 LOAD_ATTR               16 (find_search_by_uid)
-                     966 LOAD_FAST                2 (search_uid)
-                     968 PRECALL                  1
-                     972 CALL                     1
-                     982 STORE_FAST               5 (search)
-         
-          61         984 LOAD_GLOBAL             19 (NULL + grata)
-                     996 LOAD_ATTR               19 (find_by_criteria)
-                    1006 LOAD_FAST                5 (search)
-                    1008 PRECALL                  1
-                    1012 CALL                     1
-                    1022 STORE_FAST               6 (grata_companies)
-         
-          62        1024 LOAD_GLOBAL              1 (NULL + query)
-                    1036 LOAD_ATTR               18 (insert_companies_as_targets)
-         
-          63        1046 LOAD_FAST                6 (grata_companies)
-                    1048 LOAD_FAST                2 (search_uid)
-                    1050 LOAD_CONST              12 ('grata')
-         
-          62        1052 KW_NAMES                13
-                    1054 PRECALL                  3
-                    1058 CALL                     3
-                    1068 POP_TOP
-         
-          68     >> 1070 LOAD_GLOBAL              1 (NULL + query)
-                    1082 LOAD_ATTR               20 (insert_checkpoint)
-                    1092 LOAD_GLOBAL             43 (NULL + Checkpoint)
-                    1104 LOAD_FAST                1 (e)
-                    1106 LOAD_ATTR               22 (id)
-                    1116 KW_NAMES                20
-                    1118 PRECALL                  1
-                    1122 CALL                     1
-                    1132 PRECALL                  1
-                    1136 CALL                     1
-                    1146 POP_TOP
-         
-          69        1148 LOAD_GLOBAL             25 (NULL + print)
-                    1160 LOAD_CONST              21 ('processed: ')
-                    1162 LOAD_FAST                1 (e)
-                    1164 FORMAT_VALUE             0
-                    1166 BUILD_STRING             2
-                    1168 PRECALL                  1
-                    1172 CALL                     1
-                    1182 POP_TOP
-                    1184 LOAD_CONST              22 (None)
-                    1186 RETURN_VALUE
+                     570 FORMAT_VALUE             0
+                     572 LOAD_CONST               9 (' already enriched.')
+                     574 BUILD_STRING             2
+                     576 PRECALL                  1
+                     580 CALL                     1
+                     590 POP_TOP
+                     592 JUMP_FORWARD           222 (to 1038)
+         
+          43     >>  594 LOAD_FAST                1 (e)
+                     596 LOAD_ATTR                3 (type)
+                     606 LOAD_CONST              10 ('validate')
+                     608 COMPARE_OP               2 (==)
+                     614 POP_JUMP_FORWARD_IF_FALSE    71 (to 758)
+         
+          44         616 LOAD_GLOBAL              1 (NULL + query)
+                     628 LOAD_ATTR               15 (find_search_by_uid)
+                     638 LOAD_FAST                2 (search_uid)
+                     640 PRECALL                  1
+                     644 CALL                     1
+                     654 STORE_FAST               5 (search)
+         
+          45         656 LOAD_GLOBAL             17 (NULL + grata)
+                     668 LOAD_ATTR               16 (find_similar)
+                     678 LOAD_FAST                1 (e)
+                     680 LOAD_ATTR                5 (domain)
+                     690 LOAD_FAST                5 (search)
+                     692 KW_NAMES                11
+                     694 PRECALL                  2
+                     698 CALL                     2
+                     708 STORE_FAST               6 (grata_companies)
+         
+          46         710 LOAD_GLOBAL              1 (NULL + query)
+                     722 LOAD_ATTR               17 (insert_companies_as_targets)
+         
+          47         732 LOAD_FAST                6 (grata_companies)
+                     734 LOAD_FAST                2 (search_uid)
+                     736 LOAD_CONST              12 ('grata')
+         
+          46         738 KW_NAMES                13
+                     740 PRECALL                  3
+                     744 CALL                     3
+                     754 POP_TOP
+                     756 JUMP_FORWARD           140 (to 1038)
+         
+          50     >>  758 LOAD_FAST                1 (e)
+                     760 LOAD_ATTR                3 (type)
+                     770 LOAD_CONST              14 ('send')
+                     772 COMPARE_OP               2 (==)
+                     778 POP_JUMP_FORWARD_IF_FALSE     1 (to 782)
+         
+          51         780 JUMP_FORWARD           128 (to 1038)
+         
+          52     >>  782 LOAD_FAST                1 (e)
+                     784 LOAD_ATTR                3 (type)
+                     794 LOAD_CONST              15 ('accept')
+                     796 COMPARE_OP               2 (==)
+                     802 POP_JUMP_FORWARD_IF_FALSE     1 (to 806)
+         
+          53         804 JUMP_FORWARD           116 (to 1038)
+         
+          54     >>  806 LOAD_FAST                1 (e)
+                     808 LOAD_ATTR                3 (type)
+                     818 LOAD_CONST              16 ('reject')
+                     820 COMPARE_OP               2 (==)
+                     826 POP_JUMP_FORWARD_IF_FALSE     1 (to 830)
+         
+          55         828 JUMP_FORWARD           104 (to 1038)
+         
+          56     >>  830 LOAD_FAST                1 (e)
+                     832 LOAD_ATTR                3 (type)
+                     842 LOAD_CONST              17 ('conflict')
+                     844 COMPARE_OP               2 (==)
+                     850 POP_JUMP_FORWARD_IF_FALSE     1 (to 854)
+         
+          57         852 JUMP_FORWARD            92 (to 1038)
+         
+          58     >>  854 LOAD_FAST                1 (e)
+                     856 LOAD_ATTR                3 (type)
+                     866 LOAD_CONST              18 ('criteria')
+                     868 COMPARE_OP               2 (==)
+                     874 POP_JUMP_FORWARD_IF_FALSE    81 (to 1038)
+         
+          59         876 LOAD_GLOBAL             23 (NULL + print)
+                     888 LOAD_CONST              19 ('criteria search for ')
+                     890 LOAD_FAST                2 (search_uid)
+                     892 FORMAT_VALUE             0
+                     894 BUILD_STRING             2
+                     896 PRECALL                  1
+                     900 CALL                     1
+                     910 POP_TOP
+         
+          60         912 LOAD_GLOBAL              1 (NULL + query)
+                     924 LOAD_ATTR               15 (find_search_by_uid)
+                     934 LOAD_FAST                2 (search_uid)
+                     936 PRECALL                  1
+                     940 CALL                     1
+                     950 STORE_FAST               5 (search)
+         
+          61         952 LOAD_GLOBAL             17 (NULL + grata)
+                     964 LOAD_ATTR               18 (find_by_criteria)
+                     974 LOAD_FAST                5 (search)
+                     976 PRECALL                  1
+                     980 CALL                     1
+                     990 STORE_FAST               6 (grata_companies)
+         
+          62         992 LOAD_GLOBAL              1 (NULL + query)
+                    1004 LOAD_ATTR               17 (insert_companies_as_targets)
+         
+          63        1014 LOAD_FAST                6 (grata_companies)
+                    1016 LOAD_FAST                2 (search_uid)
+                    1018 LOAD_CONST              12 ('grata')
+         
+          62        1020 KW_NAMES                13
+                    1022 PRECALL                  3
+                    1026 CALL                     3
+                    1036 POP_TOP
+         
+          68     >> 1038 LOAD_GLOBAL              1 (NULL + query)
+                    1050 LOAD_ATTR               19 (insert_checkpoint)
+                    1060 LOAD_GLOBAL             41 (NULL + Checkpoint)
+                    1072 LOAD_FAST                1 (e)
+                    1074 LOAD_ATTR               21 (id)
+                    1084 KW_NAMES                20
+                    1086 PRECALL                  1
+                    1090 CALL                     1
+                    1100 PRECALL                  1
+                    1104 CALL                     1
+                    1114 POP_TOP
+         
+          69        1116 LOAD_GLOBAL             23 (NULL + print)
+                    1128 LOAD_CONST              21 ('processed: ')
+                    1130 LOAD_FAST                1 (e)
+                    1132 FORMAT_VALUE             0
+                    1134 BUILD_STRING             2
+                    1136 PRECALL                  1
+                    1140 CALL                     1
+                    1150 POP_TOP
+                    1152 LOAD_CONST              22 (None)
+                    1154 RETURN_VALUE
          consts
             '\n    May trigger additional targets adding to inbox, or something else\n    (e.g. a notification)\n    '
             'create'
             'advance'
-            10
+            'company_uid'
             'status'
             404
             ' not found'
             'name'
             'description'
             ' already enriched.'
             'validate'
@@ -428,23 +423,23 @@
             'reject'
             'conflict'
             'criteria'
             'criteria search for '
             ('event_id',)
             'processed: '
             None
-         names      ('query', 'find_event_by_id', 'search_uid', 'type', 'find_company_by_domain', 'domain', 'len', 'meta', 'keys', 'grata', 'enrich', 'get', 'print', 'name', 'description', 'update_company', 'find_search_by_uid', 'find_similar', 'insert_companies_as_targets', 'find_by_criteria', 'insert_checkpoint', 'Checkpoint', 'id')
+         names      ('query', 'find_event_by_id', 'search_uid', 'type', 'find_company_by_domain', 'domain', 'meta', 'keys', 'grata', 'enrich', 'get', 'print', 'name', 'description', 'update_company', 'find_search_by_uid', 'find_similar', 'insert_companies_as_targets', 'find_by_criteria', 'insert_checkpoint', 'Checkpoint', 'id')
          varnames   ('event_id', 'e', 'search_uid', 'company', 'resp', 'search', 'grata_companies')
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/main.py'
          name       'process_event'
          firstlineno 13
          lnotab
-            0x020628010e02160104011802320254033201320128021e013401340120
+            0x020628010e02160104011602320236033201320128021e013401340120
             012a022602160128013601160106ff140416010201160102011601020116
             0102011601240128012801160106ff12064e01
       'search_uid'
       code
          argcount  : 1
          nlocals   : 5
          stacksize : 7
@@ -455,18 +450,20 @@
             000000000000007c00ac01a6010000ab0100000000000000007d02740700
             0000000000000000007409000000000000000000007c0164021900000000
             0000000000a0050000000000000000000000000000000000000000a60000
             00ab000000000000000000a6010000ab0100000000000000007409000000
             000000000000007c02640319000000000000000000a00500000000000000
             00000000000000000000000000a6000000ab000000000000000000a60100
             00ab0100000000000000007a0a0000a6010000ab0100000000000000007d
-            037c0344005d207d04740d000000000000000000007c04a6010000ab0100
-            000000000000000100740f000000000000000000007c04a6010000ab0100
-            0000000000000001008c217411000000000000000000007c03a6010000ab
-            0100000000000000005300
+            03740d000000000000000000006404ac05a6010000ab0100000000000000
+            0035007d047c04a007000000000000000000000000000000000000000074
+            10000000000000000000007c03a6020000ab020000000000000000010064
+            0664066406a6020000ab02000000000000000001006e0b23003100730477
+            0278035900770101005900010001007413000000000000000000007c03a6
+            010000ab0100000000000000005300
           72           0 RESUME                   0
          
           77           2 LOAD_GLOBAL              1 (NULL + query)
                       14 LOAD_ATTR                1 (event)
                       24 LOAD_FAST                0 (search_uid)
                       26 KW_NAMES                 1
                       28 PRECALL                  1
@@ -501,51 +498,75 @@
                      236 PRECALL                  1
                      240 CALL                     1
                      250 BINARY_OP               10 (-)
                      254 PRECALL                  1
                      258 CALL                     1
                      268 STORE_FAST               3 (q)
          
-          82         270 LOAD_FAST                3 (q)
-                     272 GET_ITER
-                 >>  274 FOR_ITER                32 (to 340)
-                     276 STORE_FAST               4 (event_id)
-         
-          83         278 LOAD_GLOBAL             13 (NULL + print)
-                     290 LOAD_FAST                4 (event_id)
-                     292 PRECALL                  1
-                     296 CALL                     1
-                     306 POP_TOP
-         
-          84         308 LOAD_GLOBAL             15 (NULL + process_event)
-                     320 LOAD_FAST                4 (event_id)
-                     322 PRECALL                  1
-                     326 CALL                     1
-                     336 POP_TOP
-                     338 JUMP_BACKWARD           33 (to 274)
-         
-          90     >>  340 LOAD_GLOBAL             17 (NULL + len)
-                     352 LOAD_FAST                3 (q)
-                     354 PRECALL                  1
-                     358 CALL                     1
-                     368 RETURN_VALUE
+          87         270 LOAD_GLOBAL             13 (NULL + ThreadPoolExecutor)
+                     282 LOAD_CONST               4 (4)
+                     284 KW_NAMES                 5
+                     286 PRECALL                  1
+                     290 CALL                     1
+                     300 BEFORE_WITH
+                     302 STORE_FAST               4 (executor)
+         
+          88         304 LOAD_FAST                4 (executor)
+                     306 LOAD_METHOD              7 (map)
+                     328 LOAD_GLOBAL             16 (process_event)
+                     340 LOAD_FAST                3 (q)
+                     342 PRECALL                  2
+                     346 CALL                     2
+                     356 POP_TOP
+         
+          87         358 LOAD_CONST               6 (None)
+                     360 LOAD_CONST               6 (None)
+                     362 LOAD_CONST               6 (None)
+                     364 PRECALL                  2
+                     368 CALL                     2
+                     378 POP_TOP
+                     380 JUMP_FORWARD            11 (to 404)
+                 >>  382 PUSH_EXC_INFO
+                     384 WITH_EXCEPT_START
+                     386 POP_JUMP_FORWARD_IF_TRUE     4 (to 396)
+                     388 RERAISE                  2
+                 >>  390 COPY                     3
+                     392 POP_EXCEPT
+                     394 RERAISE                  1
+                 >>  396 POP_TOP
+                     398 POP_EXCEPT
+                     400 POP_TOP
+                     402 POP_TOP
+         
+          90     >>  404 LOAD_GLOBAL             19 (NULL + len)
+                     416 LOAD_FAST                3 (q)
+                     418 PRECALL                  1
+                     422 CALL                     1
+                     432 RETURN_VALUE
+         ExceptionTable:
+           302 to 356 -> 382 [1] lasti
+           382 to 388 -> 390 [3] lasti
+           396 to 396 -> 390 [3] lasti
          consts
             '\n    Process all events for a given search\n    '
             ('search_uid',)
             'id'
             'event_id'
-         names      ('query', 'event', 'checkpoint', 'list', 'set', 'tolist', 'print', 'process_event', 'len')
-         varnames   ('search_uid', 'events', 'checkpoints', 'q', 'event_id')
+            4
+            ('max_workers',)
+            None
+         names      ('query', 'event', 'checkpoint', 'list', 'set', 'tolist', 'ThreadPoolExecutor', 'map', 'process_event', 'len')
+         varnames   ('search_uid', 'events', 'checkpoints', 'q', 'executor')
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/main.py'
          name       'process_events'
          firstlineno 72
-         lnotab 0x02052a012a02b80208011e012006
-   names      ('pandas', 'pd', 'dacite', 'from_dict', 'dataclasses', 'dataclass', 'field', 'concurrent.futures', 'ThreadPoolExecutor', 'time', 'gandai.models', 'Event', 'Company', 'Checkpoint', 'gandai', 'query', 'gandai.sources', 'GrataWrapper', 'grata', 'int', 'process_event', 'process_events')
+         lnotab 0x02052a012a02b807220136ff2e03
+   names      ('concurrent.futures', 'ThreadPoolExecutor', 'dataclasses', 'dataclass', 'field', 'time', 'pandas', 'pd', 'dacite', 'from_dict', 'gandai', 'query', 'gandai.models', 'Checkpoint', 'Company', 'Event', 'gandai.sources', 'GrataWrapper', 'grata', 'int', 'process_event', 'process_events')
    varnames   ()
    freevars   ()
    cellvars   ()
    filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/main.py'
    name       '<module>'
    firstlineno 1
-   lnotab 0x00ff020108010c0110010c010c0314010c010c03103b
+   lnotab 0x00ff02010c0110010c0208010c020c0114010c03103b
```

### Comparing `gandai-1.2.0/gandai/__pycache__/models.cpython-311.pyc` & `gandai-1.3.0/gandai/__pycache__/models.cpython-311.pyc`

 * *Files 13% similar despite different names*

#### Python bytecode

```diff
@@ -1,128 +1,128 @@
 magic:    0xa70d0d0a
-moddate:  0x5ba76c64 (Tue May 23 11:45:31 2023 UTC)
-files sz: 2652
+moddate:  0xa787b564 (Mon Jul 17 18:25:43 2023 UTC)
+files sz: 2683
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 6
    flags     : 0
    code
-      0x9700640064016c006d015a016d025a020100640064026c036d045a046d
-      055a050100640064036c066d075a076d085a086d095a0901006508020047
+      0x9700640064016c006d015a016d025a026d035a030100640064026c046d
+      055a056d065a060100640064036c076d085a086d095a0901006502020047
       00640484006405a6020000ab020000000000000000a6000000ab00000000
-      00000000005a0a020065086406ac07a6010000ab01000000000000000002
+      00000000005a0a020065026406ac07a6010000ab01000000000000000002
       004700640884006409a6020000ab020000000000000000a6000000ab0000
-      000000000000005a0b02004700640a8400640b650c6504a6040000ab0400
-      000000000000005a0d650802004700640c8400640da6020000ab02000000
-      0000000000a6000000ab0000000000000000005a0e650802004700640e84
+      000000000000005a0b02004700640a8400640b650c6505a6040000ab0400
+      000000000000005a0d650202004700640c8400640da6020000ab02000000
+      0000000000a6000000ab0000000000000000005a0e650202004700640e84
       00640f650ea6030000ab030000000000000000a6000000ab000000000000
-      0000005a0f650802004700641084006411650ea6030000ab030000000000
-      000000a6000000ab0000000000000000005a106508020047006412840064
+      0000005a0f650202004700641084006411650ea6030000ab030000000000
+      000000a6000000ab0000000000000000005a106502020047006412840064
       13a6020000ab020000000000000000a6000000ab0000000000000000005a
-      11020065086406ac07a6010000ab01000000000000000002004700641484
+      11020065026406ac07a6010000ab01000000000000000002004700641484
       006415a6020000ab020000000000000000a6000000ab0000000000000000
-      005a12650802004700641684006417a6020000ab020000000000000000a6
-      000000ab0000000000000000005a13650802004700641884006419a60200
-      00ab020000000000000000a6000000ab0000000000000000005a14650802
+      005a12650202004700641684006417a6020000ab020000000000000000a6
+      000000ab0000000000000000005a13650202004700641884006419a60200
+      00ab020000000000000000a6000000ab0000000000000000005a14650202
       004700641a8400641ba6020000ab020000000000000000a6000000ab0000
       000000000000005a15641c5300
      0           0 RESUME                   0
    
      1           2 LOAD_CONST               0 (0)
-                 4 LOAD_CONST               1 (('List', 'Optional'))
-                 6 IMPORT_NAME              0 (typing)
-                 8 IMPORT_FROM              1 (List)
-                10 STORE_NAME               1 (List)
-                12 IMPORT_FROM              2 (Optional)
-                14 STORE_NAME               2 (Optional)
-                16 POP_TOP
-   
-     2          18 LOAD_CONST               0 (0)
-                20 LOAD_CONST               2 (('Enum', 'auto'))
-                22 IMPORT_NAME              3 (enum)
-                24 IMPORT_FROM              4 (Enum)
-                26 STORE_NAME               4 (Enum)
-                28 IMPORT_FROM              5 (auto)
-                30 STORE_NAME               5 (auto)
-                32 POP_TOP
-   
-     3          34 LOAD_CONST               0 (0)
-                36 LOAD_CONST               3 (('asdict', 'dataclass', 'field'))
-                38 IMPORT_NAME              6 (dataclasses)
-                40 IMPORT_FROM              7 (asdict)
-                42 STORE_NAME               7 (asdict)
-                44 IMPORT_FROM              8 (dataclass)
-                46 STORE_NAME               8 (dataclass)
-                48 IMPORT_FROM              9 (field)
-                50 STORE_NAME               9 (field)
+                 4 LOAD_CONST               1 (('asdict', 'dataclass', 'field'))
+                 6 IMPORT_NAME              0 (dataclasses)
+                 8 IMPORT_FROM              1 (asdict)
+                10 STORE_NAME               1 (asdict)
+                12 IMPORT_FROM              2 (dataclass)
+                14 STORE_NAME               2 (dataclass)
+                16 IMPORT_FROM              3 (field)
+                18 STORE_NAME               3 (field)
+                20 POP_TOP
+   
+     2          22 LOAD_CONST               0 (0)
+                24 LOAD_CONST               2 (('Enum', 'auto'))
+                26 IMPORT_NAME              4 (enum)
+                28 IMPORT_FROM              5 (Enum)
+                30 STORE_NAME               5 (Enum)
+                32 IMPORT_FROM              6 (auto)
+                34 STORE_NAME               6 (auto)
+                36 POP_TOP
+   
+     3          38 LOAD_CONST               0 (0)
+                40 LOAD_CONST               3 (('List', 'Optional'))
+                42 IMPORT_NAME              7 (typing)
+                44 IMPORT_FROM              8 (List)
+                46 STORE_NAME               8 (List)
+                48 IMPORT_FROM              9 (Optional)
+                50 STORE_NAME               9 (Optional)
                 52 POP_TOP
    
-     5          54 LOAD_NAME                8 (dataclass)
+     6          54 LOAD_NAME                2 (dataclass)
    
-     6          56 PUSH_NULL
+     7          56 PUSH_NULL
                 58 LOAD_BUILD_CLASS
-                60 LOAD_CONST               4 (<code object Actor, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py", line 5>)
+                60 LOAD_CONST               4 (<code object Actor, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py", line 6>)
                 62 MAKE_FUNCTION            0
                 64 LOAD_CONST               5 ('Actor')
                 66 PRECALL                  2
                 70 CALL                     2
    
-     5          80 PRECALL                  0
+     6          80 PRECALL                  0
                 84 CALL                     0
    
-     6          94 STORE_NAME              10 (Actor)
+     7          94 STORE_NAME              10 (Actor)
    
-    15          96 PUSH_NULL
-                98 LOAD_NAME                8 (dataclass)
+    16          96 PUSH_NULL
+                98 LOAD_NAME                2 (dataclass)
                100 LOAD_CONST               6 (True)
                102 KW_NAMES                 7
                104 PRECALL                  1
                108 CALL                     1
    
-    16         118 PUSH_NULL
+    17         118 PUSH_NULL
                120 LOAD_BUILD_CLASS
-               122 LOAD_CONST               8 (<code object Company, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py", line 15>)
+               122 LOAD_CONST               8 (<code object Company, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py", line 16>)
                124 MAKE_FUNCTION            0
                126 LOAD_CONST               9 ('Company')
                128 PRECALL                  2
                132 CALL                     2
    
-    15         142 PRECALL                  0
+    16         142 PRECALL                  0
                146 CALL                     0
    
-    16         156 STORE_NAME              11 (Company)
+    17         156 STORE_NAME              11 (Company)
    
-    25         158 PUSH_NULL
+    26         158 PUSH_NULL
                160 LOAD_BUILD_CLASS
-               162 LOAD_CONST              10 (<code object EventType, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py", line 25>)
+               162 LOAD_CONST              10 (<code object EventType, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py", line 26>)
                164 MAKE_FUNCTION            0
                166 LOAD_CONST              11 ('EventType')
                168 LOAD_NAME               12 (str)
-               170 LOAD_NAME                4 (Enum)
+               170 LOAD_NAME                5 (Enum)
                172 PRECALL                  4
                176 CALL                     4
                186 STORE_NAME              13 (EventType)
    
-    36         188 LOAD_NAME                8 (dataclass)
+    37         188 LOAD_NAME                2 (dataclass)
    
-    37         190 PUSH_NULL
+    38         190 PUSH_NULL
                192 LOAD_BUILD_CLASS
-               194 LOAD_CONST              12 (<code object Event, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py", line 36>)
+               194 LOAD_CONST              12 (<code object Event, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py", line 37>)
                196 MAKE_FUNCTION            0
                198 LOAD_CONST              13 ('Event')
                200 PRECALL                  2
                204 CALL                     2
    
-    36         214 PRECALL                  0
+    37         214 PRECALL                  0
                218 CALL                     0
    
-    37         228 STORE_NAME              14 (Event)
+    38         228 STORE_NAME              14 (Event)
    
-    48         230 LOAD_NAME                8 (dataclass)
+    48         230 LOAD_NAME                2 (dataclass)
    
     49         232 PUSH_NULL
                234 LOAD_BUILD_CLASS
                236 LOAD_CONST              14 (<code object Comment, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py", line 48>)
                238 MAKE_FUNCTION            0
                240 LOAD_CONST              15 ('Comment')
                242 LOAD_NAME               14 (Event)
@@ -130,142 +130,142 @@
                248 CALL                     3
    
     48         258 PRECALL                  0
                262 CALL                     0
    
     49         272 STORE_NAME              15 (Comment)
    
-    54         274 LOAD_NAME                8 (dataclass)
+    55         274 LOAD_NAME                2 (dataclass)
    
-    55         276 PUSH_NULL
+    56         276 PUSH_NULL
                278 LOAD_BUILD_CLASS
-               280 LOAD_CONST              16 (<code object Rating, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py", line 54>)
+               280 LOAD_CONST              16 (<code object Rating, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py", line 55>)
                282 MAKE_FUNCTION            0
                284 LOAD_CONST              17 ('Rating')
                286 LOAD_NAME               14 (Event)
                288 PRECALL                  3
                292 CALL                     3
    
-    54         302 PRECALL                  0
+    55         302 PRECALL                  0
                306 CALL                     0
    
-    55         316 STORE_NAME              16 (Rating)
+    56         316 STORE_NAME              16 (Rating)
    
-    59         318 LOAD_NAME                8 (dataclass)
+    61         318 LOAD_NAME                2 (dataclass)
    
-    60         320 PUSH_NULL
+    62         320 PUSH_NULL
                322 LOAD_BUILD_CLASS
-               324 LOAD_CONST              18 (<code object Checkpoint, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py", line 59>)
+               324 LOAD_CONST              18 (<code object Checkpoint, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py", line 61>)
                326 MAKE_FUNCTION            0
                328 LOAD_CONST              19 ('Checkpoint')
                330 PRECALL                  2
                334 CALL                     2
    
-    59         344 PRECALL                  0
+    61         344 PRECALL                  0
                348 CALL                     0
    
-    60         358 STORE_NAME              17 (Checkpoint)
+    62         358 STORE_NAME              17 (Checkpoint)
    
-    66         360 PUSH_NULL
-               362 LOAD_NAME                8 (dataclass)
+    69         360 PUSH_NULL
+               362 LOAD_NAME                2 (dataclass)
                364 LOAD_CONST               6 (True)
                366 KW_NAMES                 7
                368 PRECALL                  1
                372 CALL                     1
    
-    67         382 PUSH_NULL
+    70         382 PUSH_NULL
                384 LOAD_BUILD_CLASS
-               386 LOAD_CONST              20 (<code object Target, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py", line 66>)
+               386 LOAD_CONST              20 (<code object Target, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py", line 69>)
                388 MAKE_FUNCTION            0
                390 LOAD_CONST              21 ('Target')
                392 PRECALL                  2
                396 CALL                     2
    
-    66         406 PRECALL                  0
+    69         406 PRECALL                  0
                410 CALL                     0
    
-    67         420 STORE_NAME              18 (Target)
+    70         420 STORE_NAME              18 (Target)
    
-    78         422 LOAD_NAME                8 (dataclass)
+    81         422 LOAD_NAME                2 (dataclass)
    
-    79         424 PUSH_NULL
+    82         424 PUSH_NULL
                426 LOAD_BUILD_CLASS
-               428 LOAD_CONST              22 (<code object Criteria, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py", line 78>)
+               428 LOAD_CONST              22 (<code object Criteria, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py", line 81>)
                430 MAKE_FUNCTION            0
                432 LOAD_CONST              23 ('Criteria')
                434 PRECALL                  2
                438 CALL                     2
    
-    78         448 PRECALL                  0
+    81         448 PRECALL                  0
                452 CALL                     0
    
-    79         462 STORE_NAME              19 (Criteria)
+    82         462 STORE_NAME              19 (Criteria)
    
-    94         464 LOAD_NAME                8 (dataclass)
+    97         464 LOAD_NAME                2 (dataclass)
    
-    95         466 PUSH_NULL
+    98         466 PUSH_NULL
                468 LOAD_BUILD_CLASS
-               470 LOAD_CONST              24 (<code object Search, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py", line 94>)
+               470 LOAD_CONST              24 (<code object Search, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py", line 97>)
                472 MAKE_FUNCTION            0
                474 LOAD_CONST              25 ('Search')
                476 PRECALL                  2
                480 CALL                     2
    
-    94         490 PRECALL                  0
+    97         490 PRECALL                  0
                494 CALL                     0
    
-    95         504 STORE_NAME              20 (Search)
+    98         504 STORE_NAME              20 (Search)
    
-   109         506 LOAD_NAME                8 (dataclass)
+   111         506 LOAD_NAME                2 (dataclass)
    
-   110         508 PUSH_NULL
+   112         508 PUSH_NULL
                510 LOAD_BUILD_CLASS
-               512 LOAD_CONST              26 (<code object Sort, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py", line 109>)
+               512 LOAD_CONST              26 (<code object Sort, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py", line 111>)
                514 MAKE_FUNCTION            0
                516 LOAD_CONST              27 ('Sort')
                518 PRECALL                  2
                522 CALL                     2
    
-   109         532 PRECALL                  0
+   111         532 PRECALL                  0
                536 CALL                     0
    
-   110         546 STORE_NAME              21 (Sort)
+   112         546 STORE_NAME              21 (Sort)
                548 LOAD_CONST              28 (None)
                550 RETURN_VALUE
    consts
       0
-      ('List', 'Optional')
-      ('Enum', 'auto')
       ('asdict', 'dataclass', 'field')
+      ('Enum', 'auto')
+      ('List', 'Optional')
       code
          argcount  : 0
          nlocals   : 0
          stacksize : 3
          flags     : 0
          code
             0x970065005a0164005a0255006503650464013c0000006503650464023c
             0000006503650464033c00000064045300
-           5           0 RESUME                   0
+           6           0 RESUME                   0
                        2 LOAD_NAME                0 (__name__)
                        4 STORE_NAME               1 (__module__)
                        6 LOAD_CONST               0 ('Actor')
                        8 STORE_NAME               2 (__qualname__)
                       10 SETUP_ANNOTATIONS
          
-           8          12 LOAD_NAME                3 (str)
+           9          12 LOAD_NAME                3 (str)
                       14 LOAD_NAME                4 (__annotations__)
                       16 LOAD_CONST               1 ('key')
                       18 STORE_SUBSCR
          
-           9          22 LOAD_NAME                3 (str)
+          10          22 LOAD_NAME                3 (str)
                       24 LOAD_NAME                4 (__annotations__)
                       26 LOAD_CONST               2 ('type')
                       28 STORE_SUBSCR
          
-          10          32 LOAD_NAME                3 (str)
+          11          32 LOAD_NAME                3 (str)
                       34 LOAD_NAME                4 (__annotations__)
                       36 LOAD_CONST               3 ('name')
                       38 STORE_SUBSCR
                       42 LOAD_CONST               4 (None)
                       44 RETURN_VALUE
          consts
             'Actor'
@@ -275,15 +275,15 @@
             None
          names      ('__name__', '__module__', '__qualname__', 'str', '__annotations__')
          varnames   ()
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py'
          name       'Actor'
-         firstlineno 5
+         firstlineno 6
          lnotab 0x0c030a010a01
       'Actor'
       True
       ('order',)
       code
          argcount  : 0
          nlocals   : 0
@@ -293,69 +293,69 @@
             0x970065005a0164005a0255006503650464013c00000064025a05650665
             0319000000000000000000650464033c00000064025a0765066503190000
             00000000000000650464043c000000020065086509ac05a6010000ab0100
             000000000000005a0a6509650464063c000000020065086402ac07a60100
             00ab0100000000000000005a0b650c650464083c000000020065086402ac
             07a6010000ab0100000000000000005a0d6506650c190000000000000000
             00650464093c00000064025300
-          15           0 RESUME                   0
+          16           0 RESUME                   0
                        2 LOAD_NAME                0 (__name__)
                        4 STORE_NAME               1 (__module__)
                        6 LOAD_CONST               0 ('Company')
                        8 STORE_NAME               2 (__qualname__)
                       10 SETUP_ANNOTATIONS
          
-          17          12 LOAD_NAME                3 (str)
+          18          12 LOAD_NAME                3 (str)
                       14 LOAD_NAME                4 (__annotations__)
                       16 LOAD_CONST               1 ('domain')
                       18 STORE_SUBSCR
          
-          18          22 LOAD_CONST               2 (None)
+          19          22 LOAD_CONST               2 (None)
                       24 STORE_NAME               5 (name)
                       26 LOAD_NAME                6 (Optional)
                       28 LOAD_NAME                3 (str)
                       30 BINARY_SUBSCR
                       40 LOAD_NAME                4 (__annotations__)
                       42 LOAD_CONST               3 ('name')
                       44 STORE_SUBSCR
          
-          19          48 LOAD_CONST               2 (None)
+          20          48 LOAD_CONST               2 (None)
                       50 STORE_NAME               7 (description)
                       52 LOAD_NAME                6 (Optional)
                       54 LOAD_NAME                3 (str)
                       56 BINARY_SUBSCR
                       66 LOAD_NAME                4 (__annotations__)
                       68 LOAD_CONST               4 ('description')
                       70 STORE_SUBSCR
          
-          20          74 PUSH_NULL
+          21          74 PUSH_NULL
                       76 LOAD_NAME                8 (field)
                       78 LOAD_NAME                9 (dict)
                       80 KW_NAMES                 5
                       82 PRECALL                  1
                       86 CALL                     1
                       96 STORE_NAME              10 (meta)
                       98 LOAD_NAME                9 (dict)
                      100 LOAD_NAME                4 (__annotations__)
                      102 LOAD_CONST               6 ('meta')
                      104 STORE_SUBSCR
          
-          21         108 PUSH_NULL
+          22         108 PUSH_NULL
                      110 LOAD_NAME                8 (field)
                      112 LOAD_CONST               2 (None)
                      114 KW_NAMES                 7
                      116 PRECALL                  1
                      120 CALL                     1
                      130 STORE_NAME              11 (id)
                      132 LOAD_NAME               12 (int)
                      134 LOAD_NAME                4 (__annotations__)
                      136 LOAD_CONST               8 ('id')
                      138 STORE_SUBSCR
          
-          22         142 PUSH_NULL
+          23         142 PUSH_NULL
                      144 LOAD_NAME                8 (field)
                      146 LOAD_CONST               2 (None)
                      148 KW_NAMES                 7
                      150 PRECALL                  1
                      154 CALL                     1
                      164 STORE_NAME              13 (uid)
                      166 LOAD_NAME                6 (Optional)
@@ -379,78 +379,78 @@
             'uid'
          names      ('__name__', '__module__', '__qualname__', 'str', '__annotations__', 'name', 'Optional', 'description', 'field', 'dict', 'meta', 'id', 'int', 'uid')
          varnames   ()
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py'
          name       'Company'
-         firstlineno 15
+         firstlineno 16
          lnotab 0x0c020a011a011a0122012201
       'Company'
       code
          argcount  : 0
          nlocals   : 0
          stacksize : 2
          flags     : 0
          code
             0x970065005a0164005a0202006503a6000000ab0000000000000000005a
             0402006503a6000000ab0000000000000000005a0502006503a6000000ab
             0000000000000000005a0602006503a6000000ab0000000000000000005a
             0702006503a6000000ab0000000000000000005a0802006503a6000000ab
             0000000000000000005a0902006503a6000000ab0000000000000000005a
             0a02006503a6000000ab0000000000000000005a0b64015300
-          25           0 RESUME                   0
+          26           0 RESUME                   0
                        2 LOAD_NAME                0 (__name__)
                        4 STORE_NAME               1 (__module__)
                        6 LOAD_CONST               0 ('EventType')
                        8 STORE_NAME               2 (__qualname__)
          
-          26          10 PUSH_NULL
+          27          10 PUSH_NULL
                       12 LOAD_NAME                3 (auto)
                       14 PRECALL                  0
                       18 CALL                     0
                       28 STORE_NAME               4 (CREATE)
          
-          27          30 PUSH_NULL
+          28          30 PUSH_NULL
                       32 LOAD_NAME                3 (auto)
                       34 PRECALL                  0
                       38 CALL                     0
                       48 STORE_NAME               5 (ADVANCE)
          
-          28          50 PUSH_NULL
+          29          50 PUSH_NULL
                       52 LOAD_NAME                3 (auto)
                       54 PRECALL                  0
                       58 CALL                     0
                       68 STORE_NAME               6 (VALIDATE)
          
-          29          70 PUSH_NULL
+          30          70 PUSH_NULL
                       72 LOAD_NAME                3 (auto)
                       74 PRECALL                  0
                       78 CALL                     0
                       88 STORE_NAME               7 (SEND)
          
-          30          90 PUSH_NULL
+          31          90 PUSH_NULL
                       92 LOAD_NAME                3 (auto)
                       94 PRECALL                  0
                       98 CALL                     0
                      108 STORE_NAME               8 (CLIENT_ACCEPT)
          
-          31         110 PUSH_NULL
+          32         110 PUSH_NULL
                      112 LOAD_NAME                3 (auto)
                      114 PRECALL                  0
                      118 CALL                     0
                      128 STORE_NAME               9 (CONFLICT)
          
-          32         130 PUSH_NULL
+          33         130 PUSH_NULL
                      132 LOAD_NAME                3 (auto)
                      134 PRECALL                  0
                      138 CALL                     0
                      148 STORE_NAME              10 (REJECT)
          
-          33         150 PUSH_NULL
+          34         150 PUSH_NULL
                      152 LOAD_NAME                3 (auto)
                      154 PRECALL                  0
                      158 CALL                     0
                      168 STORE_NAME              11 (CRITERIA)
                      170 LOAD_CONST               1 (None)
                      172 RETURN_VALUE
          consts
@@ -458,29 +458,29 @@
             None
          names      ('__name__', '__module__', '__qualname__', 'auto', 'CREATE', 'ADVANCE', 'VALIDATE', 'SEND', 'CLIENT_ACCEPT', 'CONFLICT', 'REJECT', 'CRITERIA')
          varnames   ()
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py'
          name       'EventType'
-         firstlineno 25
+         firstlineno 26
          lnotab 0x0a011401140114011401140114011401
       'EventType'
       code
          argcount  : 0
          nlocals   : 0
          stacksize : 3
          flags     : 0
          code
             0x970065005a0164005a0255006503650464013c00000065056506190000
             00000000000000650464023c0000006506650464033c0000006506650464
             043c000000020065076508ac05a6010000ab0100000000000000005a0965
             08650464063c000000020065076407ac08a6010000ab0100000000000000
             005a0a6503650464093c00000064075300
-          36           0 RESUME                   0
+          37           0 RESUME                   0
                        2 LOAD_NAME                0 (__name__)
                        4 STORE_NAME               1 (__module__)
                        6 LOAD_CONST               0 ('Event')
                        8 STORE_NAME               2 (__qualname__)
                       10 SETUP_ANNOTATIONS
          
           39          12 LOAD_NAME                3 (int)
@@ -543,16 +543,16 @@
             'id'
          names      ('__name__', '__module__', '__qualname__', 'int', '__annotations__', 'Optional', 'str', 'field', 'dict', 'data', 'id')
          varnames   ()
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py'
          name       'Event'
-         firstlineno 36
-         lnotab 0x0c030a0116010a010a012201
+         firstlineno 37
+         lnotab 0x0c020a0116010a010a012201
       'Event'
       code
          argcount  : 0
          nlocals   : 0
          stacksize : 1
          flags     : 0
          code 0x970065005a0164005a02640184005a0364025300
@@ -576,15 +576,15 @@
                flags     : 3
                code
                   0x97007401000000000000000000007c006a010000000000000000640119
                   000000000000000000740400000000000000000000a6020000ab02000000
                   000000000073024a00820164005300
                 50           0 RESUME                   0
                
-                51           2 LOAD_GLOBAL              1 (NULL + isinstance)
+                52           2 LOAD_GLOBAL              1 (NULL + isinstance)
                             14 LOAD_FAST                0 (self)
                             16 LOAD_ATTR                1 (data)
                             26 LOAD_CONST               1 ('comment')
                             28 BINARY_SUBSCR
                             38 LOAD_GLOBAL              4 (str)
                             50 PRECALL                  2
                             54 CALL                     2
@@ -599,15 +599,15 @@
                names      ('isinstance', 'data', 'str')
                varnames   ('self',)
                freevars   ()
                cellvars   ()
                filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py'
                name       '__post_init__'
                firstlineno 50
-               lnotab 0x0201
+               lnotab 0x0202
             None
          names      ('__name__', '__module__', '__qualname__', '__post_init__')
          varnames   ()
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py'
          name       'Comment'
@@ -616,21 +616,21 @@
       'Comment'
       code
          argcount  : 0
          nlocals   : 0
          stacksize : 1
          flags     : 0
          code 0x970065005a0164005a02640184005a0364025300
-          54           0 RESUME                   0
+          55           0 RESUME                   0
                        2 LOAD_NAME                0 (__name__)
                        4 STORE_NAME               1 (__module__)
                        6 LOAD_CONST               0 ('Rating')
                        8 STORE_NAME               2 (__qualname__)
          
-          56          10 LOAD_CONST               1 (<code object __post_init__, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py", line 56>)
+          57          10 LOAD_CONST               1 (<code object __post_init__, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py", line 57>)
                       12 MAKE_FUNCTION            0
                       14 STORE_NAME               3 (__post_init__)
                       16 LOAD_CONST               2 (None)
                       18 RETURN_VALUE
          consts
             'Rating'
             code
@@ -638,17 +638,17 @@
                nlocals   : 1
                stacksize : 4
                flags     : 3
                code
                   0x97007401000000000000000000007c006a010000000000000000640119
                   000000000000000000740400000000000000000000a6020000ab02000000
                   000000000073024a00820164005300
-                56           0 RESUME                   0
+                57           0 RESUME                   0
                
-                57           2 LOAD_GLOBAL              1 (NULL + isinstance)
+                58           2 LOAD_GLOBAL              1 (NULL + isinstance)
                             14 LOAD_FAST                0 (self)
                             16 LOAD_ATTR                1 (data)
                             26 LOAD_CONST               1 ('rating')
                             28 BINARY_SUBSCR
                             38 LOAD_GLOBAL              4 (int)
                             50 PRECALL                  2
                             54 CALL                     2
@@ -662,48 +662,48 @@
                   'rating'
                names      ('isinstance', 'data', 'int')
                varnames   ('self',)
                freevars   ()
                cellvars   ()
                filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py'
                name       '__post_init__'
-               firstlineno 56
+               firstlineno 57
                lnotab 0x0201
             None
          names      ('__name__', '__module__', '__qualname__', '__post_init__')
          varnames   ()
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py'
          name       'Rating'
-         firstlineno 54
+         firstlineno 55
          lnotab 0x0a02
       'Rating'
       code
          argcount  : 0
          nlocals   : 0
          stacksize : 3
          flags     : 0
          code
             0x970065005a0164005a0255006503650464013c000000020065056402ac
             03a6010000ab0100000000000000005a066503650464043c000000640253
             00
-          59           0 RESUME                   0
+          61           0 RESUME                   0
                        2 LOAD_NAME                0 (__name__)
                        4 STORE_NAME               1 (__module__)
                        6 LOAD_CONST               0 ('Checkpoint')
                        8 STORE_NAME               2 (__qualname__)
                       10 SETUP_ANNOTATIONS
          
-          62          12 LOAD_NAME                3 (int)
+          64          12 LOAD_NAME                3 (int)
                       14 LOAD_NAME                4 (__annotations__)
                       16 LOAD_CONST               1 ('event_id')
                       18 STORE_SUBSCR
          
-          63          22 PUSH_NULL
+          65          22 PUSH_NULL
                       24 LOAD_NAME                5 (field)
                       26 LOAD_CONST               2 (None)
                       28 KW_NAMES                 3
                       30 PRECALL                  1
                       34 CALL                     1
                       44 STORE_NAME               6 (id)
                       46 LOAD_NAME                3 (int)
@@ -720,70 +720,70 @@
             'id'
          names      ('__name__', '__module__', '__qualname__', 'int', '__annotations__', 'field', 'id')
          varnames   ()
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py'
          name       'Checkpoint'
-         firstlineno 59
+         firstlineno 61
          lnotab 0x0c030a01
       'Checkpoint'
       code
          argcount  : 0
          nlocals   : 0
          stacksize : 3
          flags     : 0
          code
             0x970065005a0164005a0255006503650464013c0000006503650464023c
             0000006505650464033c0000006503650464043c0000006506650464053c
             0000006503650464063c0000006505650464073c0000006507650464083c
             00000064095300
-          66           0 RESUME                   0
+          69           0 RESUME                   0
                        2 LOAD_NAME                0 (__name__)
                        4 STORE_NAME               1 (__module__)
                        6 LOAD_CONST               0 ('Target')
                        8 STORE_NAME               2 (__qualname__)
                       10 SETUP_ANNOTATIONS
          
-          68          12 LOAD_NAME                3 (str)
+          71          12 LOAD_NAME                3 (str)
                       14 LOAD_NAME                4 (__annotations__)
                       16 LOAD_CONST               1 ('domain')
                       18 STORE_SUBSCR
          
-          69          22 LOAD_NAME                3 (str)
+          72          22 LOAD_NAME                3 (str)
                       24 LOAD_NAME                4 (__annotations__)
                       26 LOAD_CONST               2 ('name')
                       28 STORE_SUBSCR
          
-          70          32 LOAD_NAME                5 (int)
+          73          32 LOAD_NAME                5 (int)
                       34 LOAD_NAME                4 (__annotations__)
                       36 LOAD_CONST               3 ('search_id')
                       38 STORE_SUBSCR
          
-          71          42 LOAD_NAME                3 (str)
+          74          42 LOAD_NAME                3 (str)
                       44 LOAD_NAME                4 (__annotations__)
                       46 LOAD_CONST               4 ('description')
                       48 STORE_SUBSCR
          
-          72          52 LOAD_NAME                6 (List)
+          75          52 LOAD_NAME                6 (List)
                       54 LOAD_NAME                4 (__annotations__)
                       56 LOAD_CONST               5 ('event')
                       58 STORE_SUBSCR
          
-          73          62 LOAD_NAME                3 (str)
+          76          62 LOAD_NAME                3 (str)
                       64 LOAD_NAME                4 (__annotations__)
                       66 LOAD_CONST               6 ('last_event_type')
                       68 STORE_SUBSCR
          
-          74          72 LOAD_NAME                5 (int)
+          77          72 LOAD_NAME                5 (int)
                       74 LOAD_NAME                4 (__annotations__)
                       76 LOAD_CONST               7 ('last_rating')
                       78 STORE_SUBSCR
          
-          75          82 LOAD_NAME                7 (dict)
+          78          82 LOAD_NAME                7 (dict)
                       84 LOAD_NAME                4 (__annotations__)
                       86 LOAD_CONST               8 ('meta')
                       88 STORE_SUBSCR
                       92 LOAD_CONST               9 (None)
                       94 RETURN_VALUE
          consts
             'Target'
@@ -798,91 +798,91 @@
             None
          names      ('__name__', '__module__', '__qualname__', 'str', '__annotations__', 'int', 'List', 'dict')
          varnames   ()
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py'
          name       'Target'
-         firstlineno 66
+         firstlineno 69
          lnotab 0x0c020a010a010a010a010a010a010a01
       'Target'
       code
          argcount  : 0
          nlocals   : 0
          stacksize : 3
          flags     : 0
          code
             0x970065005a0164005a0255006503650464013c0000006505650464023c
             0000006505650464033c0000006506650464043c0000006506650464053c
             0000006506650464063c0000006506650464073c0000006506650464083c
             0000006506650464093c00000065066504640a3c00000065036504640b3c
             00000065036504640c3c000000640d5300
-          78           0 RESUME                   0
+          81           0 RESUME                   0
                        2 LOAD_NAME                0 (__name__)
                        4 STORE_NAME               1 (__module__)
                        6 LOAD_CONST               0 ('Criteria')
                        8 STORE_NAME               2 (__qualname__)
                       10 SETUP_ANNOTATIONS
          
-          80          12 LOAD_NAME                3 (int)
+          83          12 LOAD_NAME                3 (int)
                       14 LOAD_NAME                4 (__annotations__)
                       16 LOAD_CONST               1 ('search_id')
                       18 STORE_SUBSCR
          
-          81          22 LOAD_NAME                5 (str)
+          84          22 LOAD_NAME                5 (str)
                       24 LOAD_NAME                4 (__annotations__)
                       26 LOAD_CONST               2 ('type')
                       28 STORE_SUBSCR
          
-          82          32 LOAD_NAME                5 (str)
+          85          32 LOAD_NAME                5 (str)
                       34 LOAD_NAME                4 (__annotations__)
                       36 LOAD_CONST               3 ('prompt')
                       38 STORE_SUBSCR
          
-          83          42 LOAD_NAME                6 (list)
+          86          42 LOAD_NAME                6 (list)
                       44 LOAD_NAME                4 (__annotations__)
                       46 LOAD_CONST               4 ('rating')
                       48 STORE_SUBSCR
          
-          84          52 LOAD_NAME                6 (list)
+          87          52 LOAD_NAME                6 (list)
                       54 LOAD_NAME                4 (__annotations__)
                       56 LOAD_CONST               5 ('employees_range')
                       58 STORE_SUBSCR
          
-          85          62 LOAD_NAME                6 (list)
+          88          62 LOAD_NAME                6 (list)
                       64 LOAD_NAME                4 (__annotations__)
                       66 LOAD_CONST               6 ('country')
                       68 STORE_SUBSCR
          
-          86          72 LOAD_NAME                6 (list)
+          89          72 LOAD_NAME                6 (list)
                       74 LOAD_NAME                4 (__annotations__)
                       76 LOAD_CONST               7 ('state')
                       78 STORE_SUBSCR
          
-          87          82 LOAD_NAME                6 (list)
+          90          82 LOAD_NAME                6 (list)
                       84 LOAD_NAME                4 (__annotations__)
                       86 LOAD_CONST               8 ('ownership')
                       88 STORE_SUBSCR
          
-          88          92 LOAD_NAME                6 (list)
+          91          92 LOAD_NAME                6 (list)
                       94 LOAD_NAME                4 (__annotations__)
                       96 LOAD_CONST               9 ('product')
                       98 STORE_SUBSCR
          
-          89         102 LOAD_NAME                6 (list)
+          92         102 LOAD_NAME                6 (list)
                      104 LOAD_NAME                4 (__annotations__)
                      106 LOAD_CONST              10 ('services')
                      108 STORE_SUBSCR
          
-          90         112 LOAD_NAME                3 (int)
+          93         112 LOAD_NAME                3 (int)
                      114 LOAD_NAME                4 (__annotations__)
                      116 LOAD_CONST              11 ('updated')
                      118 STORE_SUBSCR
          
-          91         122 LOAD_NAME                3 (int)
+          94         122 LOAD_NAME                3 (int)
                      124 LOAD_NAME                4 (__annotations__)
                      126 LOAD_CONST              12 ('actor_id')
                      128 STORE_SUBSCR
                      132 LOAD_CONST              13 (None)
                      134 RETURN_VALUE
          consts
             'Criteria'
@@ -901,15 +901,15 @@
             None
          names      ('__name__', '__module__', '__qualname__', 'int', '__annotations__', 'str', 'list')
          varnames   ()
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py'
          name       'Criteria'
-         firstlineno 78
+         firstlineno 81
          lnotab 0x0c020a010a010a010a010a010a010a010a010a010a010a01
       'Criteria'
       code
          argcount  : 0
          nlocals   : 0
          stacksize : 3
          flags     : 0
@@ -918,85 +918,85 @@
             0000006505650464033c000000020065066507ac04a6010000ab01000000
             00000000005a086507650464053c000000020065066507ac04a6010000ab
             0100000000000000005a096507650464063c000000020065066507ac04a6
             010000ab0100000000000000005a0a6507650464073c0000000200650665
             07ac04a6010000ab0100000000000000005a0b6507650464083c00000002
             0065066409ac0aa6010000ab0100000000000000005a0c65036504640b3c
             00000064095300
-          94           0 RESUME                   0
+          97           0 RESUME                   0
                        2 LOAD_NAME                0 (__name__)
                        4 STORE_NAME               1 (__module__)
                        6 LOAD_CONST               0 ('Search')
                        8 STORE_NAME               2 (__qualname__)
                       10 SETUP_ANNOTATIONS
          
-          97          12 LOAD_NAME                3 (int)
+          99          12 LOAD_NAME                3 (int)
                       14 LOAD_NAME                4 (__annotations__)
                       16 LOAD_CONST               1 ('uid')
                       18 STORE_SUBSCR
          
-          98          22 LOAD_NAME                5 (str)
+         100          22 LOAD_NAME                5 (str)
                       24 LOAD_NAME                4 (__annotations__)
                       26 LOAD_CONST               2 ('client_domain')
                       28 STORE_SUBSCR
          
-          99          32 LOAD_NAME                5 (str)
+         101          32 LOAD_NAME                5 (str)
                       34 LOAD_NAME                4 (__annotations__)
                       36 LOAD_CONST               3 ('label')
                       38 STORE_SUBSCR
          
-         100          42 PUSH_NULL
+         102          42 PUSH_NULL
                       44 LOAD_NAME                6 (field)
                       46 LOAD_NAME                7 (dict)
                       48 KW_NAMES                 4
                       50 PRECALL                  1
                       54 CALL                     1
                       64 STORE_NAME               8 (meta)
                       66 LOAD_NAME                7 (dict)
                       68 LOAD_NAME                4 (__annotations__)
                       70 LOAD_CONST               5 ('meta')
                       72 STORE_SUBSCR
          
-         101          76 PUSH_NULL
+         103          76 PUSH_NULL
                       78 LOAD_NAME                6 (field)
                       80 LOAD_NAME                7 (dict)
                       82 KW_NAMES                 4
                       84 PRECALL                  1
                       88 CALL                     1
                       98 STORE_NAME               9 (inclusion)
                      100 LOAD_NAME                7 (dict)
                      102 LOAD_NAME                4 (__annotations__)
                      104 LOAD_CONST               6 ('inclusion')
                      106 STORE_SUBSCR
          
-         102         110 PUSH_NULL
+         104         110 PUSH_NULL
                      112 LOAD_NAME                6 (field)
                      114 LOAD_NAME                7 (dict)
                      116 KW_NAMES                 4
                      118 PRECALL                  1
                      122 CALL                     1
                      132 STORE_NAME              10 (exclusion)
                      134 LOAD_NAME                7 (dict)
                      136 LOAD_NAME                4 (__annotations__)
                      138 LOAD_CONST               7 ('exclusion')
                      140 STORE_SUBSCR
          
-         103         144 PUSH_NULL
+         105         144 PUSH_NULL
                      146 LOAD_NAME                6 (field)
                      148 LOAD_NAME                7 (dict)
                      150 KW_NAMES                 4
                      152 PRECALL                  1
                      156 CALL                     1
                      166 STORE_NAME              11 (sort)
                      168 LOAD_NAME                7 (dict)
                      170 LOAD_NAME                4 (__annotations__)
                      172 LOAD_CONST               8 ('sort')
                      174 STORE_SUBSCR
          
-         104         178 PUSH_NULL
+         106         178 PUSH_NULL
                      180 LOAD_NAME                6 (field)
                      182 LOAD_CONST               9 (None)
                      184 KW_NAMES                10
                      186 PRECALL                  1
                      190 CALL                     1
                      200 STORE_NAME              12 (id)
                      202 LOAD_NAME                3 (int)
@@ -1020,48 +1020,48 @@
             'id'
          names      ('__name__', '__module__', '__qualname__', 'int', '__annotations__', 'str', 'field', 'dict', 'meta', 'inclusion', 'exclusion', 'sort', 'id')
          varnames   ()
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py'
          name       'Search'
-         firstlineno 94
-         lnotab 0x0c030a010a010a012201220122012201
+         firstlineno 97
+         lnotab 0x0c020a010a010a012201220122012201
       'Search'
       code
          argcount  : 0
          nlocals   : 0
          stacksize : 3
          flags     : 0
          code
             0x970065005a0164005a02550067006401a2015a036402640367025a0465
             05650664043c0000006505650664053c00000064065300
-         109           0 RESUME                   0
+         111           0 RESUME                   0
                        2 LOAD_NAME                0 (__name__)
                        4 STORE_NAME               1 (__module__)
                        6 LOAD_CONST               0 ('Sort')
                        8 STORE_NAME               2 (__qualname__)
                       10 SETUP_ANNOTATIONS
          
-         111          12 BUILD_LIST               0
+         113          12 BUILD_LIST               0
                       14 LOAD_CONST               1 (('employee_count', 'rating', 'state', 'country', 'year_founded', 'name'))
                       16 LIST_EXTEND              1
                       18 STORE_NAME               3 (FIELDS)
          
-         112          20 LOAD_CONST               2 ('asc')
+         114          20 LOAD_CONST               2 ('asc')
                       22 LOAD_CONST               3 ('desc')
                       24 BUILD_LIST               2
                       26 STORE_NAME               4 (ORDERS)
          
-         114          28 LOAD_NAME                5 (str)
+         116          28 LOAD_NAME                5 (str)
                       30 LOAD_NAME                6 (__annotations__)
                       32 LOAD_CONST               4 ('field')
                       34 STORE_SUBSCR
          
-         115          38 LOAD_NAME                5 (str)
+         117          38 LOAD_NAME                5 (str)
                       40 LOAD_NAME                6 (__annotations__)
                       42 LOAD_CONST               5 ('order')
                       44 STORE_SUBSCR
                       48 LOAD_CONST               6 (None)
                       50 RETURN_VALUE
          consts
             'Sort'
@@ -1073,23 +1073,23 @@
             None
          names      ('__name__', '__module__', '__qualname__', 'FIELDS', 'ORDERS', 'str', '__annotations__')
          varnames   ()
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py'
          name       'Sort'
-         firstlineno 109
+         firstlineno 111
          lnotab 0x0c02080108020a01
       'Sort'
       None
-   names      ('typing', 'List', 'Optional', 'enum', 'Enum', 'auto', 'dataclasses', 'asdict', 'dataclass', 'field', 'Actor', 'Company', 'str', 'EventType', 'Event', 'Comment', 'Rating', 'Checkpoint', 'Target', 'Criteria', 'Search', 'Sort')
+   names      ('dataclasses', 'asdict', 'dataclass', 'field', 'enum', 'Enum', 'auto', 'typing', 'List', 'Optional', 'Actor', 'Company', 'str', 'EventType', 'Event', 'Comment', 'Rating', 'Checkpoint', 'Target', 'Criteria', 'Search', 'Sort')
    varnames   ()
    freevars   ()
    cellvars   ()
    filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/models.py'
    name       '<module>'
    firstlineno 1
    lnotab
-      0x00ff0201100110011402020118ff0e010209160118ff0e0102091e0b02
-      0118ff0e01020b02011aff0e01020502011aff0e010204020118ff0e0102
-      06160118ff0e01020b020118ff0e01020f020118ff0e01020e020118ff0e
+      0x00ff0201140110011003020118ff0e010209160118ff0e0102091e0b02
+      0118ff0e01020a02011aff0e01020602011aff0e010205020118ff0e0102
+      07160118ff0e01020b020118ff0e01020f020118ff0e01020d020118ff0e
       01
```

### Comparing `gandai-1.2.0/gandai/__pycache__/query.cpython-311.pyc` & `gandai-1.3.0/gandai/__pycache__/query.cpython-311.pyc`

 * *Files 26% similar despite different names*

#### Python bytecode

```diff
@@ -1,332 +1,384 @@
 magic:    0xa70d0d0a
-moddate:  0x22b16c64 (Tue May 23 12:27:14 2023 UTC)
-files sz: 12867
+moddate:  0x5b33bc64 (Sat Jul 22 19:51:55 2023 UTC)
+files sz: 21175
 code
    argcount  : 0
    nlocals   : 0
-   stacksize : 8
+   stacksize : 10
    flags     : 0
    code
-      0x9700640064016c005a00640064016c015a02640064026c036d045a046d
-      055a050100640064036c066d075a070100640064046c086d095a09010064
-      0064056c0a6d0b5a0b6d0c5a0c6d0d5a0d6d0e5a0e6d0f5a0f6d105a1001
-      00640064016c115a11640064066c126d135a130100640064076c146d155a
-      15010002006515a6000000ab0000000000000000000100640064086c166d
-      175a17010002006517a6000000ab0000000000000000005a186409650c66
-      02640a84045a19640b650b640c650b6604640d84045a1a640e650e640c65
-      0e6604640f84045a1b6410650f640c650f6604641184045a1c6412651064
-      0c65106604641384045a1d64146504651e19000000000000000000641565
-      1f6416651e640c64016608641784045a2064186504650519000000000000
-      0000006415651f6416651e640c64016608641984045a21641a84005a2264
-      296415651f641b651e6604641c84055a236415651f640c65026a24000000
-      00000000006604641d84045a256415651f640c65026a2400000000000000
-      006604641e84045a26640c65026a2400000000000000006602641f84045a
-      276415651f640c65026a2400000000000000006604642084045a28641565
-      1f640c65026a2400000000000000006604642184045a296415651f640c65
-      0f6604642284045a2a6423651e640c650c6604642484045a2b6425651f64
-      0c650b6604642684045a2c6409650c640c64016604642784045a2d641065
-      0f640c64016604642884045a2e64015300
+      0x9700640064016c005a00640064026c016d025a020100640064036c036d
+      045a046d055a050100640064016c065a07640064016c085a08640064046c
+      096d0a5a0a0100640064056c0b6d0c5a0c0100640064066c0d6d0e5a0e01
+      000200650ca6000000ab0000000000000000000100640064076c0f6d105a
+      100100640064086c116d125a120100640064096c136d145a146d155a156d
+      165a166d175a176d185a186d195a19010002006512a6000000ab00000000
+      00000000005a1a640a65166602640b84045a1b640c6517640d6517660464
+      0e84045a1c640f6514640d65146604641084045a1d64116519640d651966
+      04641284045a1e64136515640d65156604641484045a1f64156505652019
+      000000000000000000641665216417652064186520640d6401660a641984
+      045a22641a65056504190000000000000000006416652164176520640d64
+      016608641b84045a23640d65076a2400000000000000006602641c84045a
+      25641d84005a26640d65076a2400000000000000006602641e84045a2764
+      2e64166521641865206604641f84055a2864166521640d65076a24000000
+      00000000006604642084045a2964166521640d65076a2400000000000000
+      006604642184045a2a64166521640d65076a240000000000000000660464
+      2284045a2b64166521640d65076a2400000000000000006604642384045a
+      2c640d65076a2400000000000000006602642484045a2d64166521640d65
+      076a2400000000000000006604642584045a2e64166521640d65076a2400
+      000000000000006604642684045a2f64166521640d65196604642784045a
+      3064286520640d65166604642984045a31642a6521640d65176604642b84
+      045a32640a6516640d64016604642c84045a3364116519640d6401660464
+      2d84045a3464015300
      0           0 RESUME                   0
    
      1           2 LOAD_CONST               0 (0)
                  4 LOAD_CONST               1 (None)
                  6 IMPORT_NAME              0 (json)
                  8 STORE_NAME               0 (json)
    
      2          10 LOAD_CONST               0 (0)
-                12 LOAD_CONST               1 (None)
-                14 IMPORT_NAME              1 (pandas)
-                16 STORE_NAME               2 (pd)
-   
-     3          18 LOAD_CONST               0 (0)
-                20 LOAD_CONST               2 (('List', 'Any'))
-                22 IMPORT_NAME              3 (typing)
-                24 IMPORT_FROM              4 (List)
-                26 STORE_NAME               4 (List)
-                28 IMPORT_FROM              5 (Any)
-                30 STORE_NAME               5 (Any)
-                32 POP_TOP
-   
-     4          34 LOAD_CONST               0 (0)
-                36 LOAD_CONST               3 (('asdict',))
-                38 IMPORT_NAME              6 (dataclasses)
-                40 IMPORT_FROM              7 (asdict)
-                42 STORE_NAME               7 (asdict)
-                44 POP_TOP
-   
-     5          46 LOAD_CONST               0 (0)
-                48 LOAD_CONST               4 (('from_dict',))
-                50 IMPORT_NAME              8 (dacite)
-                52 IMPORT_FROM              9 (from_dict)
-                54 STORE_NAME               9 (from_dict)
-                56 POP_TOP
-   
-     6          58 LOAD_CONST               0 (0)
-                60 LOAD_CONST               5 (('Event', 'Company', 'EventType', 'Actor', 'Search', 'Checkpoint'))
-                62 IMPORT_NAME             10 (gandai.models)
-                64 IMPORT_FROM             11 (Event)
-                66 STORE_NAME              11 (Event)
-                68 IMPORT_FROM             12 (Company)
-                70 STORE_NAME              12 (Company)
-                72 IMPORT_FROM             13 (EventType)
-                74 STORE_NAME              13 (EventType)
-                76 IMPORT_FROM             14 (Actor)
-                78 STORE_NAME              14 (Actor)
-                80 IMPORT_FROM             15 (Search)
-                82 STORE_NAME              15 (Search)
-                84 IMPORT_FROM             16 (Checkpoint)
-                86 STORE_NAME              16 (Checkpoint)
+                12 LOAD_CONST               2 (('asdict',))
+                14 IMPORT_NAME              1 (dataclasses)
+                16 IMPORT_FROM              2 (asdict)
+                18 STORE_NAME               2 (asdict)
+                20 POP_TOP
+   
+     3          22 LOAD_CONST               0 (0)
+                24 LOAD_CONST               3 (('Any', 'List'))
+                26 IMPORT_NAME              3 (typing)
+                28 IMPORT_FROM              4 (Any)
+                30 STORE_NAME               4 (Any)
+                32 IMPORT_FROM              5 (List)
+                34 STORE_NAME               5 (List)
+                36 POP_TOP
+   
+     5          38 LOAD_CONST               0 (0)
+                40 LOAD_CONST               1 (None)
+                42 IMPORT_NAME              6 (pandas)
+                44 STORE_NAME               7 (pd)
+   
+     6          46 LOAD_CONST               0 (0)
+                48 LOAD_CONST               1 (None)
+                50 IMPORT_NAME              8 (sqlalchemy)
+                52 STORE_NAME               8 (sqlalchemy)
+   
+     7          54 LOAD_CONST               0 (0)
+                56 LOAD_CONST               4 (('from_dict',))
+                58 IMPORT_NAME              9 (dacite)
+                60 IMPORT_FROM             10 (from_dict)
+                62 STORE_NAME              10 (from_dict)
+                64 POP_TOP
+   
+     8          66 LOAD_CONST               0 (0)
+                68 LOAD_CONST               5 (('load_dotenv',))
+                70 IMPORT_NAME             11 (dotenv)
+                72 IMPORT_FROM             12 (load_dotenv)
+                74 STORE_NAME              12 (load_dotenv)
+                76 POP_TOP
+   
+     9          78 LOAD_CONST               0 (0)
+                80 LOAD_CONST               6 (('Connector',))
+                82 IMPORT_NAME             13 (google.cloud.sql.connector)
+                84 IMPORT_FROM             14 (Connector)
+                86 STORE_NAME              14 (Connector)
                 88 POP_TOP
    
-    16          90 LOAD_CONST               0 (0)
-                92 LOAD_CONST               1 (None)
-                94 IMPORT_NAME             17 (sqlalchemy)
-                96 STORE_NAME              17 (sqlalchemy)
-   
-    18          98 LOAD_CONST               0 (0)
-               100 LOAD_CONST               6 (('Connector',))
-               102 IMPORT_NAME             18 (google.cloud.sql.connector)
-               104 IMPORT_FROM             19 (Connector)
-               106 STORE_NAME              19 (Connector)
+    11          90 PUSH_NULL
+                92 LOAD_NAME               12 (load_dotenv)
+                94 PRECALL                  0
+                98 CALL                     0
                108 POP_TOP
    
-    19         110 LOAD_CONST               0 (0)
-               112 LOAD_CONST               7 (('load_dotenv',))
-               114 IMPORT_NAME             20 (dotenv)
-               116 IMPORT_FROM             21 (load_dotenv)
-               118 STORE_NAME              21 (load_dotenv)
+    13         110 LOAD_CONST               0 (0)
+               112 LOAD_CONST               7 (('helpers',))
+               114 IMPORT_NAME             15 (gandai)
+               116 IMPORT_FROM             16 (helpers)
+               118 STORE_NAME              16 (helpers)
                120 POP_TOP
    
-    21         122 PUSH_NULL
-               124 LOAD_NAME               21 (load_dotenv)
-               126 PRECALL                  0
-               130 CALL                     0
-               140 POP_TOP
-   
-    23         142 LOAD_CONST               0 (0)
-               144 LOAD_CONST               8 (('connect_with_connector',))
-               146 IMPORT_NAME             22 (gandai.db)
-               148 IMPORT_FROM             23 (connect_with_connector)
-               150 STORE_NAME              23 (connect_with_connector)
-               152 POP_TOP
-   
-    25         154 PUSH_NULL
-               156 LOAD_NAME               23 (connect_with_connector)
-               158 PRECALL                  0
-               162 CALL                     0
-               172 STORE_NAME              24 (db)
-   
-    31         174 LOAD_CONST               9 ('company')
-               176 LOAD_NAME               12 (Company)
-               178 BUILD_TUPLE              2
-               180 LOAD_CONST              10 (<code object insert_company, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 31>)
-               182 MAKE_FUNCTION            4 (annotations)
-               184 STORE_NAME              25 (insert_company)
-   
-    45         186 LOAD_CONST              11 ('event')
-               188 LOAD_NAME               11 (Event)
-               190 LOAD_CONST              12 ('return')
-               192 LOAD_NAME               11 (Event)
-               194 BUILD_TUPLE              4
-               196 LOAD_CONST              13 (<code object insert_event, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 45>)
-               198 MAKE_FUNCTION            4 (annotations)
-               200 STORE_NAME              26 (insert_event)
-   
-    66         202 LOAD_CONST              14 ('actor')
-               204 LOAD_NAME               14 (Actor)
-               206 LOAD_CONST              12 ('return')
-               208 LOAD_NAME               14 (Actor)
-               210 BUILD_TUPLE              4
-               212 LOAD_CONST              15 (<code object insert_actor, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 66>)
-               214 MAKE_FUNCTION            4 (annotations)
-               216 STORE_NAME              27 (insert_actor)
-   
-    81         218 LOAD_CONST              16 ('search')
-               220 LOAD_NAME               15 (Search)
-               222 LOAD_CONST              12 ('return')
-               224 LOAD_NAME               15 (Search)
-               226 BUILD_TUPLE              4
-               228 LOAD_CONST              17 (<code object insert_search, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 81>)
-               230 MAKE_FUNCTION            4 (annotations)
-               232 STORE_NAME              28 (insert_search)
-   
-   100         234 LOAD_CONST              18 ('checkpoint')
-               236 LOAD_NAME               16 (Checkpoint)
-               238 LOAD_CONST              12 ('return')
-               240 LOAD_NAME               16 (Checkpoint)
-               242 BUILD_TUPLE              4
-               244 LOAD_CONST              19 (<code object insert_checkpoint, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 100>)
-               246 MAKE_FUNCTION            4 (annotations)
-               248 STORE_NAME              29 (insert_checkpoint)
-   
-   113         250 LOAD_CONST              20 ('domains')
-   
-   114         252 LOAD_NAME                4 (List)
-               254 LOAD_NAME               30 (str)
-               256 BINARY_SUBSCR
-   
-   113         266 LOAD_CONST              21 ('search_uid')
-   
-   114         268 LOAD_NAME               31 (int)
-   
-   113         270 LOAD_CONST              22 ('actor_key')
-   
-   114         272 LOAD_NAME               30 (str)
-   
-   113         274 LOAD_CONST              12 ('return')
-   
-   115         276 LOAD_CONST               1 (None)
-   
-   113         278 BUILD_TUPLE              8
-               280 LOAD_CONST              23 (<code object insert_and_advance_targets_from_domains, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 113>)
-               282 MAKE_FUNCTION            4 (annotations)
-               284 STORE_NAME              32 (insert_and_advance_targets_from_domains)
-   
-   167         286 LOAD_CONST              24 ('companies')
-   
-   168         288 LOAD_NAME                4 (List)
-               290 LOAD_NAME                5 (Any)
-               292 BINARY_SUBSCR
-   
-   167         302 LOAD_CONST              21 ('search_uid')
-   
-   168         304 LOAD_NAME               31 (int)
-   
-   167         306 LOAD_CONST              22 ('actor_key')
-   
-   168         308 LOAD_NAME               30 (str)
-   
-   167         310 LOAD_CONST              12 ('return')
-   
-   169         312 LOAD_CONST               1 (None)
-   
-   167         314 BUILD_TUPLE              8
-               316 LOAD_CONST              25 (<code object insert_companies_as_targets, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 167>)
-               318 MAKE_FUNCTION            4 (annotations)
-               320 STORE_NAME              33 (insert_companies_as_targets)
-   
-   221         322 LOAD_CONST              26 (<code object search, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 221>)
-               324 MAKE_FUNCTION            0
-               326 STORE_NAME              34 (search)
-   
-   230         328 LOAD_CONST              41 ((None,))
-               330 LOAD_CONST              21 ('search_uid')
-               332 LOAD_NAME               31 (int)
-               334 LOAD_CONST              27 ('last_event_type')
-               336 LOAD_NAME               30 (str)
-               338 BUILD_TUPLE              4
-               340 LOAD_CONST              28 (<code object target, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 230>)
-               342 MAKE_FUNCTION            5 (defaults, annotations)
-               344 STORE_NAME              35 (target)
-   
-   261         346 LOAD_CONST              21 ('search_uid')
-               348 LOAD_NAME               31 (int)
-               350 LOAD_CONST              12 ('return')
-               352 LOAD_NAME                2 (pd)
-               354 LOAD_ATTR               36 (DataFrame)
-               364 BUILD_TUPLE              4
-               366 LOAD_CONST              29 (<code object target_count, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 261>)
-               368 MAKE_FUNCTION            4 (annotations)
-               370 STORE_NAME              37 (target_count)
-   
-   277         372 LOAD_CONST              21 ('search_uid')
-               374 LOAD_NAME               31 (int)
-               376 LOAD_CONST              12 ('return')
-               378 LOAD_NAME                2 (pd)
-               380 LOAD_ATTR               36 (DataFrame)
-               390 BUILD_TUPLE              4
-               392 LOAD_CONST              30 (<code object event, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 277>)
-               394 MAKE_FUNCTION            4 (annotations)
-               396 STORE_NAME              38 (event)
-   
-   289         398 LOAD_CONST              12 ('return')
-               400 LOAD_NAME                2 (pd)
-               402 LOAD_ATTR               36 (DataFrame)
-               412 BUILD_TUPLE              2
-               414 LOAD_CONST              31 (<code object company, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 289>)
-               416 MAKE_FUNCTION            4 (annotations)
-               418 STORE_NAME              39 (company)
-   
-   300         420 LOAD_CONST              21 ('search_uid')
-               422 LOAD_NAME               31 (int)
-               424 LOAD_CONST              12 ('return')
-               426 LOAD_NAME                2 (pd)
-               428 LOAD_ATTR               36 (DataFrame)
-               438 BUILD_TUPLE              4
-               440 LOAD_CONST              32 (<code object checkpoint, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 300>)
-               442 MAKE_FUNCTION            4 (annotations)
-               444 STORE_NAME              40 (checkpoint)
-   
-   313         446 LOAD_CONST              21 ('search_uid')
-               448 LOAD_NAME               31 (int)
-               450 LOAD_CONST              12 ('return')
-               452 LOAD_NAME                2 (pd)
-               454 LOAD_ATTR               36 (DataFrame)
-               464 BUILD_TUPLE              4
-               466 LOAD_CONST              33 (<code object comment_by_domain, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 313>)
-               468 MAKE_FUNCTION            4 (annotations)
-               470 STORE_NAME              41 (comment_by_domain)
-   
-   334         472 LOAD_CONST              21 ('search_uid')
-               474 LOAD_NAME               31 (int)
-               476 LOAD_CONST              12 ('return')
-               478 LOAD_NAME               15 (Search)
-               480 BUILD_TUPLE              4
-               482 LOAD_CONST              34 (<code object find_search_by_uid, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 334>)
-               484 MAKE_FUNCTION            4 (annotations)
-               486 STORE_NAME              42 (find_search_by_uid)
-   
-   350         488 LOAD_CONST              35 ('domain')
-               490 LOAD_NAME               30 (str)
-               492 LOAD_CONST              12 ('return')
-               494 LOAD_NAME               12 (Company)
-               496 BUILD_TUPLE              4
-               498 LOAD_CONST              36 (<code object find_company_by_domain, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 350>)
-               500 MAKE_FUNCTION            4 (annotations)
-               502 STORE_NAME              43 (find_company_by_domain)
-   
-   366         504 LOAD_CONST              37 ('event_id')
-               506 LOAD_NAME               31 (int)
-               508 LOAD_CONST              12 ('return')
-               510 LOAD_NAME               11 (Event)
-               512 BUILD_TUPLE              4
-               514 LOAD_CONST              38 (<code object find_event_by_id, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 366>)
-               516 MAKE_FUNCTION            4 (annotations)
-               518 STORE_NAME              44 (find_event_by_id)
-   
-   385         520 LOAD_CONST               9 ('company')
-               522 LOAD_NAME               12 (Company)
-               524 LOAD_CONST              12 ('return')
-               526 LOAD_CONST               1 (None)
-               528 BUILD_TUPLE              4
-               530 LOAD_CONST              39 (<code object update_company, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 385>)
-               532 MAKE_FUNCTION            4 (annotations)
-               534 STORE_NAME              45 (update_company)
-   
-   409         536 LOAD_CONST              16 ('search')
-               538 LOAD_NAME               15 (Search)
-               540 LOAD_CONST              12 ('return')
-               542 LOAD_CONST               1 (None)
-               544 BUILD_TUPLE              4
-               546 LOAD_CONST              40 (<code object update_search, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 409>)
-               548 MAKE_FUNCTION            4 (annotations)
-               550 STORE_NAME              46 (update_search)
-               552 LOAD_CONST               1 (None)
-               554 RETURN_VALUE
+    14         122 LOAD_CONST               0 (0)
+               124 LOAD_CONST               8 (('connect_with_connector',))
+               126 IMPORT_NAME             17 (gandai.db)
+               128 IMPORT_FROM             18 (connect_with_connector)
+               130 STORE_NAME              18 (connect_with_connector)
+               132 POP_TOP
+   
+    15         134 LOAD_CONST               0 (0)
+               136 LOAD_CONST               9 (('Actor', 'Checkpoint', 'Company', 'Event', 'EventType', 'Search'))
+               138 IMPORT_NAME             19 (gandai.models)
+               140 IMPORT_FROM             20 (Actor)
+               142 STORE_NAME              20 (Actor)
+               144 IMPORT_FROM             21 (Checkpoint)
+               146 STORE_NAME              21 (Checkpoint)
+               148 IMPORT_FROM             22 (Company)
+               150 STORE_NAME              22 (Company)
+               152 IMPORT_FROM             23 (Event)
+               154 STORE_NAME              23 (Event)
+               156 IMPORT_FROM             24 (EventType)
+               158 STORE_NAME              24 (EventType)
+               160 IMPORT_FROM             25 (Search)
+               162 STORE_NAME              25 (Search)
+               164 POP_TOP
+   
+    17         166 PUSH_NULL
+               168 LOAD_NAME               18 (connect_with_connector)
+               170 PRECALL                  0
+               174 CALL                     0
+               184 STORE_NAME              26 (db)
+   
+    23         186 LOAD_CONST              10 ('company')
+               188 LOAD_NAME               22 (Company)
+               190 BUILD_TUPLE              2
+               192 LOAD_CONST              11 (<code object insert_company, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 23>)
+               194 MAKE_FUNCTION            4 (annotations)
+               196 STORE_NAME              27 (insert_company)
+   
+    37         198 LOAD_CONST              12 ('event')
+               200 LOAD_NAME               23 (Event)
+               202 LOAD_CONST              13 ('return')
+               204 LOAD_NAME               23 (Event)
+               206 BUILD_TUPLE              4
+               208 LOAD_CONST              14 (<code object insert_event, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 37>)
+               210 MAKE_FUNCTION            4 (annotations)
+               212 STORE_NAME              28 (insert_event)
+   
+    58         214 LOAD_CONST              15 ('actor')
+               216 LOAD_NAME               20 (Actor)
+               218 LOAD_CONST              13 ('return')
+               220 LOAD_NAME               20 (Actor)
+               222 BUILD_TUPLE              4
+               224 LOAD_CONST              16 (<code object insert_actor, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 58>)
+               226 MAKE_FUNCTION            4 (annotations)
+               228 STORE_NAME              29 (insert_actor)
+   
+    73         230 LOAD_CONST              17 ('search')
+               232 LOAD_NAME               25 (Search)
+               234 LOAD_CONST              13 ('return')
+               236 LOAD_NAME               25 (Search)
+               238 BUILD_TUPLE              4
+               240 LOAD_CONST              18 (<code object insert_search, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 73>)
+               242 MAKE_FUNCTION            4 (annotations)
+               244 STORE_NAME              30 (insert_search)
+   
+    92         246 LOAD_CONST              19 ('checkpoint')
+               248 LOAD_NAME               21 (Checkpoint)
+               250 LOAD_CONST              13 ('return')
+               252 LOAD_NAME               21 (Checkpoint)
+               254 BUILD_TUPLE              4
+               256 LOAD_CONST              20 (<code object insert_checkpoint, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 92>)
+               258 MAKE_FUNCTION            4 (annotations)
+               260 STORE_NAME              31 (insert_checkpoint)
+   
+   105         262 LOAD_CONST              21 ('domains')
+   
+   106         264 LOAD_NAME                5 (List)
+               266 LOAD_NAME               32 (str)
+               268 BINARY_SUBSCR
+   
+   105         278 LOAD_CONST              22 ('search_uid')
+   
+   106         280 LOAD_NAME               33 (int)
+   
+   105         282 LOAD_CONST              23 ('actor_key')
+   
+   106         284 LOAD_NAME               32 (str)
+   
+   105         286 LOAD_CONST              24 ('last_event_type')
+   
+   106         288 LOAD_NAME               32 (str)
+   
+   105         290 LOAD_CONST              13 ('return')
+   
+   107         292 LOAD_CONST               1 (None)
+   
+   105         294 BUILD_TUPLE             10
+               296 LOAD_CONST              25 (<code object insert_targets_from_domains, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 105>)
+               298 MAKE_FUNCTION            4 (annotations)
+               300 STORE_NAME              34 (insert_targets_from_domains)
+   
+   160         302 LOAD_CONST              26 ('companies')
+   
+   161         304 LOAD_NAME                5 (List)
+               306 LOAD_NAME                4 (Any)
+               308 BINARY_SUBSCR
+   
+   160         318 LOAD_CONST              22 ('search_uid')
+   
+   161         320 LOAD_NAME               33 (int)
+   
+   160         322 LOAD_CONST              23 ('actor_key')
+   
+   161         324 LOAD_NAME               32 (str)
+   
+   160         326 LOAD_CONST              13 ('return')
+   
+   162         328 LOAD_CONST               1 (None)
+   
+   160         330 BUILD_TUPLE              8
+               332 LOAD_CONST              27 (<code object insert_companies_as_targets, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 160>)
+               334 MAKE_FUNCTION            4 (annotations)
+               336 STORE_NAME              35 (insert_companies_as_targets)
+   
+   215         338 LOAD_CONST              13 ('return')
+               340 LOAD_NAME                7 (pd)
+               342 LOAD_ATTR               36 (DataFrame)
+               352 BUILD_TUPLE              2
+               354 LOAD_CONST              28 (<code object top_actor_per_search, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 215>)
+               356 MAKE_FUNCTION            4 (annotations)
+               358 STORE_NAME              37 (top_actor_per_search)
+   
+   254         360 LOAD_CONST              29 (<code object search, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 254>)
+               362 MAKE_FUNCTION            0
+               364 STORE_NAME              38 (search)
+   
+   293         366 LOAD_CONST              13 ('return')
+               368 LOAD_NAME                7 (pd)
+               370 LOAD_ATTR               36 (DataFrame)
+               380 BUILD_TUPLE              2
+               382 LOAD_CONST              30 (<code object actor, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 293>)
+               384 MAKE_FUNCTION            4 (annotations)
+               386 STORE_NAME              39 (actor)
+   
+   307         388 LOAD_CONST              46 ((None,))
+               390 LOAD_CONST              22 ('search_uid')
+               392 LOAD_NAME               33 (int)
+               394 LOAD_CONST              24 ('last_event_type')
+               396 LOAD_NAME               32 (str)
+               398 BUILD_TUPLE              4
+               400 LOAD_CONST              31 (<code object search_target_by_last_event_type, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 307>)
+               402 MAKE_FUNCTION            5 (defaults, annotations)
+               404 STORE_NAME              40 (search_target_by_last_event_type)
+   
+   376         406 LOAD_CONST              22 ('search_uid')
+               408 LOAD_NAME               33 (int)
+               410 LOAD_CONST              13 ('return')
+               412 LOAD_NAME                7 (pd)
+               414 LOAD_ATTR               36 (DataFrame)
+               424 BUILD_TUPLE              4
+               426 LOAD_CONST              32 (<code object search_target_export, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 376>)
+               428 MAKE_FUNCTION            4 (annotations)
+               430 STORE_NAME              41 (search_target_export)
+   
+   465         432 LOAD_CONST              22 ('search_uid')
+               434 LOAD_NAME               33 (int)
+               436 LOAD_CONST              13 ('return')
+               438 LOAD_NAME                7 (pd)
+               440 LOAD_ATTR               36 (DataFrame)
+               450 BUILD_TUPLE              4
+               452 LOAD_CONST              33 (<code object target_count, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 465>)
+               454 MAKE_FUNCTION            4 (annotations)
+               456 STORE_NAME              42 (target_count)
+   
+   495         458 LOAD_CONST              22 ('search_uid')
+               460 LOAD_NAME               33 (int)
+               462 LOAD_CONST              13 ('return')
+               464 LOAD_NAME                7 (pd)
+               466 LOAD_ATTR               36 (DataFrame)
+               476 BUILD_TUPLE              4
+               478 LOAD_CONST              34 (<code object event, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 495>)
+               480 MAKE_FUNCTION            4 (annotations)
+               482 STORE_NAME              43 (event)
+   
+   507         484 LOAD_CONST              22 ('search_uid')
+               486 LOAD_NAME               33 (int)
+               488 LOAD_CONST              13 ('return')
+               490 LOAD_NAME                7 (pd)
+               492 LOAD_ATTR               36 (DataFrame)
+               502 BUILD_TUPLE              4
+               504 LOAD_CONST              35 (<code object unique_domains, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 507>)
+               506 MAKE_FUNCTION            4 (annotations)
+               508 STORE_NAME              44 (unique_domains)
+   
+   519         510 LOAD_CONST              13 ('return')
+               512 LOAD_NAME                7 (pd)
+               514 LOAD_ATTR               36 (DataFrame)
+               524 BUILD_TUPLE              2
+               526 LOAD_CONST              36 (<code object company, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 519>)
+               528 MAKE_FUNCTION            4 (annotations)
+               530 STORE_NAME              45 (company)
+   
+   530         532 LOAD_CONST              22 ('search_uid')
+               534 LOAD_NAME               33 (int)
+               536 LOAD_CONST              13 ('return')
+               538 LOAD_NAME                7 (pd)
+               540 LOAD_ATTR               36 (DataFrame)
+               550 BUILD_TUPLE              4
+               552 LOAD_CONST              37 (<code object checkpoint, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 530>)
+               554 MAKE_FUNCTION            4 (annotations)
+               556 STORE_NAME              46 (checkpoint)
+   
+   543         558 LOAD_CONST              22 ('search_uid')
+               560 LOAD_NAME               33 (int)
+               562 LOAD_CONST              13 ('return')
+               564 LOAD_NAME                7 (pd)
+               566 LOAD_ATTR               36 (DataFrame)
+               576 BUILD_TUPLE              4
+               578 LOAD_CONST              38 (<code object comment_by_domain, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 543>)
+               580 MAKE_FUNCTION            4 (annotations)
+               582 STORE_NAME              47 (comment_by_domain)
+   
+   564         584 LOAD_CONST              22 ('search_uid')
+               586 LOAD_NAME               33 (int)
+               588 LOAD_CONST              13 ('return')
+               590 LOAD_NAME               25 (Search)
+               592 BUILD_TUPLE              4
+               594 LOAD_CONST              39 (<code object find_search_by_uid, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 564>)
+               596 MAKE_FUNCTION            4 (annotations)
+               598 STORE_NAME              48 (find_search_by_uid)
+   
+   582         600 LOAD_CONST              40 ('domain')
+               602 LOAD_NAME               32 (str)
+               604 LOAD_CONST              13 ('return')
+               606 LOAD_NAME               22 (Company)
+               608 BUILD_TUPLE              4
+               610 LOAD_CONST              41 (<code object find_company_by_domain, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 582>)
+               612 MAKE_FUNCTION            4 (annotations)
+               614 STORE_NAME              49 (find_company_by_domain)
+   
+   598         616 LOAD_CONST              42 ('event_id')
+               618 LOAD_NAME               33 (int)
+               620 LOAD_CONST              13 ('return')
+               622 LOAD_NAME               23 (Event)
+               624 BUILD_TUPLE              4
+               626 LOAD_CONST              43 (<code object find_event_by_id, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 598>)
+               628 MAKE_FUNCTION            4 (annotations)
+               630 STORE_NAME              50 (find_event_by_id)
+   
+   617         632 LOAD_CONST              10 ('company')
+               634 LOAD_NAME               22 (Company)
+               636 LOAD_CONST              13 ('return')
+               638 LOAD_CONST               1 (None)
+               640 BUILD_TUPLE              4
+               642 LOAD_CONST              44 (<code object update_company, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 617>)
+               644 MAKE_FUNCTION            4 (annotations)
+               646 STORE_NAME              51 (update_company)
+   
+   642         648 LOAD_CONST              17 ('search')
+               650 LOAD_NAME               25 (Search)
+               652 LOAD_CONST              13 ('return')
+               654 LOAD_CONST               1 (None)
+               656 BUILD_TUPLE              4
+               658 LOAD_CONST              45 (<code object update_search, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 642>)
+               660 MAKE_FUNCTION            4 (annotations)
+               662 STORE_NAME              52 (update_search)
+               664 LOAD_CONST               1 (None)
+               666 RETURN_VALUE
    consts
       0
       None
-      ('List', 'Any')
       ('asdict',)
+      ('Any', 'List')
       ('from_dict',)
-      ('Event', 'Company', 'EventType', 'Actor', 'Search', 'Checkpoint')
-      ('Connector',)
       ('load_dotenv',)
+      ('Connector',)
+      ('helpers',)
       ('connect_with_connector',)
+      ('Actor', 'Checkpoint', 'Company', 'Event', 'EventType', 'Search')
       'company'
       code
          argcount  : 1
          nlocals   : 3
          stacksize : 7
          flags     : 3
          code
@@ -335,50 +387,50 @@
             000000000000006a0300000000000000006401a6010000ab010000000000
             0000007d027c01a00400000000000000000000000000000000000000007c
             02740b000000000000000000007c00a6010000ab010000000000000000a6
             020000ab02000000000000000001007c01a0060000000000000000000000
             000000000000000000a6000000ab00000000000000000001006400640064
             00a6020000ab02000000000000000001006e0b2300310073047702780359
             00770101005900010001007c005300
-          31           0 RESUME                   0
+          23           0 RESUME                   0
          
-          32           2 LOAD_GLOBAL              0 (db)
+          24           2 LOAD_GLOBAL              0 (db)
                       14 LOAD_METHOD              1 (connect)
                       36 PRECALL                  0
                       40 CALL                     0
                       50 BEFORE_WITH
                       52 STORE_FAST               1 (con)
          
-          33          54 LOAD_GLOBAL              5 (NULL + sqlalchemy)
+          25          54 LOAD_GLOBAL              5 (NULL + sqlalchemy)
                       66 LOAD_ATTR                3 (text)
          
-          34          76 LOAD_CONST               1 ('\n                INSERT INTO company (domain, name, description) \n                VALUES(:domain, :name, :description)\n                ON CONFLICT DO NOTHING\n            ')
+          26          76 LOAD_CONST               1 ('\n                INSERT INTO company (domain, name, description) \n                VALUES(:domain, :name, :description)\n                ON CONFLICT DO NOTHING\n            ')
          
-          33          78 PRECALL                  1
+          25          78 PRECALL                  1
                       82 CALL                     1
                       92 STORE_FAST               2 (statement)
          
-          40          94 LOAD_FAST                1 (con)
+          32          94 LOAD_FAST                1 (con)
                       96 LOAD_METHOD              4 (execute)
                      118 LOAD_FAST                2 (statement)
                      120 LOAD_GLOBAL             11 (NULL + asdict)
                      132 LOAD_FAST                0 (company)
                      134 PRECALL                  1
                      138 CALL                     1
                      148 PRECALL                  2
                      152 CALL                     2
                      162 POP_TOP
          
-          41         164 LOAD_FAST                1 (con)
+          33         164 LOAD_FAST                1 (con)
                      166 LOAD_METHOD              6 (commit)
                      188 PRECALL                  0
                      192 CALL                     0
                      202 POP_TOP
          
-          32         204 LOAD_CONST               0 (None)
+          24         204 LOAD_CONST               0 (None)
                      206 LOAD_CONST               0 (None)
                      208 LOAD_CONST               0 (None)
                      210 PRECALL                  2
                      214 CALL                     2
                      224 POP_TOP
                      226 JUMP_FORWARD            11 (to 250)
                  >>  228 PUSH_EXC_INFO
@@ -389,30 +441,30 @@
                      238 POP_EXCEPT
                      240 RERAISE                  1
                  >>  242 POP_TOP
                      244 POP_EXCEPT
                      246 POP_TOP
                      248 POP_TOP
          
-          42     >>  250 LOAD_FAST                0 (company)
+          34     >>  250 LOAD_FAST                0 (company)
                      252 RETURN_VALUE
          ExceptionTable:
            52 to 202 -> 228 [1] lasti
            228 to 234 -> 236 [3] lasti
            242 to 242 -> 236 [3] lasti
          consts
             None
             '\n                INSERT INTO company (domain, name, description) \n                VALUES(:domain, :name, :description)\n                ON CONFLICT DO NOTHING\n            '
          names      ('db', 'connect', 'sqlalchemy', 'text', 'execute', 'asdict', 'commit')
          varnames   ('company', 'con', 'statement')
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py'
          name       'insert_company'
-         firstlineno 31
+         firstlineno 23
          lnotab 0x02013401160102ff1007460128f72e0a
       'event'
       'return'
       code
          argcount  : 1
          nlocals   : 6
          stacksize : 6
@@ -424,135 +476,121 @@
             0000007d027409000000000000000000007c00a6010000ab010000000000
             0000007d03740b000000000000000000006a0600000000000000007c0364
             0219000000000000000000a6010000ab0100000000000000007c0364023c
             0000007c01a00700000000000000000000000000000000000000007c027c
             03a6020000ab0200000000000000007d047c04a008000000000000000000
             0000000000000000000000a6000000ab0000000000000000007d057c0572
             087c056403190000000000000000006e0164007c005f0900000000000000
-            007c01a00700000000000000000000000000000000000000007405000000
-            000000000000006a0300000000000000006404a6010000ab010000000000
-            000000a6010000ab01000000000000000001007c01a00a00000000000000
-            00000000000000000000000000a6000000ab000000000000000000010064
-            0064006400a6020000ab02000000000000000001006e0b23003100730477
-            0278035900770101005900010001007c005300
-          45           0 RESUME                   0
+            007c01a00a0000000000000000000000000000000000000000a6000000ab
+            0000000000000000000100640064006400a6020000ab0200000000000000
+            0001006e0b230031007304770278035900770101005900010001007c0053
+            00
+          37           0 RESUME                   0
          
-          46           2 LOAD_GLOBAL              0 (db)
+          38           2 LOAD_GLOBAL              0 (db)
                       14 LOAD_METHOD              1 (connect)
                       36 PRECALL                  0
                       40 CALL                     0
                       50 BEFORE_WITH
                       52 STORE_FAST               1 (con)
          
-          47          54 LOAD_GLOBAL              5 (NULL + sqlalchemy)
+          39          54 LOAD_GLOBAL              5 (NULL + sqlalchemy)
                       66 LOAD_ATTR                3 (text)
          
-          48          76 LOAD_CONST               1 ('\n                INSERT INTO event (search_uid, domain, actor_key, type, data) \n                VALUES(:search_uid, :domain, :actor_key, :type, :data)\n                ON CONFLICT DO NOTHING\n                RETURNING id\n            ')
+          40          76 LOAD_CONST               1 ('\n                INSERT INTO event (search_uid, domain, actor_key, type, data) \n                VALUES(:search_uid, :domain, :actor_key, :type, :data)\n                ON CONFLICT DO NOTHING\n                RETURNING id\n            ')
          
-          47          78 PRECALL                  1
+          39          78 PRECALL                  1
                       82 CALL                     1
                       92 STORE_FAST               2 (statement)
          
-          55          94 LOAD_GLOBAL              9 (NULL + asdict)
+          47          94 LOAD_GLOBAL              9 (NULL + asdict)
                      106 LOAD_FAST                0 (event)
                      108 PRECALL                  1
                      112 CALL                     1
                      122 STORE_FAST               3 (obj)
          
-          56         124 LOAD_GLOBAL             11 (NULL + json)
+          48         124 LOAD_GLOBAL             11 (NULL + json)
                      136 LOAD_ATTR                6 (dumps)
                      146 LOAD_FAST                3 (obj)
                      148 LOAD_CONST               2 ('data')
                      150 BINARY_SUBSCR
                      160 PRECALL                  1
                      164 CALL                     1
                      174 LOAD_FAST                3 (obj)
                      176 LOAD_CONST               2 ('data')
                      178 STORE_SUBSCR
          
-          57         182 LOAD_FAST                1 (con)
+          49         182 LOAD_FAST                1 (con)
                      184 LOAD_METHOD              7 (execute)
                      206 LOAD_FAST                2 (statement)
                      208 LOAD_FAST                3 (obj)
                      210 PRECALL                  2
                      214 CALL                     2
                      224 STORE_FAST               4 (result)
          
-          59         226 LOAD_FAST                4 (result)
+          51         226 LOAD_FAST                4 (result)
                      228 LOAD_METHOD              8 (first)
                      250 PRECALL                  0
                      254 CALL                     0
                      264 STORE_FAST               5 (_id)
          
-          60         266 LOAD_FAST                5 (_id)
+          52         266 LOAD_FAST                5 (_id)
                      268 POP_JUMP_FORWARD_IF_FALSE     8 (to 286)
                      270 LOAD_FAST                5 (_id)
                      272 LOAD_CONST               3 (0)
                      274 BINARY_SUBSCR
                      284 JUMP_FORWARD             1 (to 288)
                  >>  286 LOAD_CONST               0 (None)
                  >>  288 LOAD_FAST                0 (event)
                      290 STORE_ATTR               9 (id)
          
-          61         300 LOAD_FAST                1 (con)
-                     302 LOAD_METHOD              7 (execute)
-                     324 LOAD_GLOBAL              5 (NULL + sqlalchemy)
-                     336 LOAD_ATTR                3 (text)
-                     346 LOAD_CONST               4 ('REFRESH MATERIALIZED VIEW target')
-                     348 PRECALL                  1
-                     352 CALL                     1
-                     362 PRECALL                  1
-                     366 CALL                     1
-                     376 POP_TOP
+          54         300 LOAD_FAST                1 (con)
+                     302 LOAD_METHOD             10 (commit)
+                     324 PRECALL                  0
+                     328 CALL                     0
+                     338 POP_TOP
          
-          62         378 LOAD_FAST                1 (con)
-                     380 LOAD_METHOD             10 (commit)
-                     402 PRECALL                  0
-                     406 CALL                     0
-                     416 POP_TOP
-         
-          46         418 LOAD_CONST               0 (None)
-                     420 LOAD_CONST               0 (None)
-                     422 LOAD_CONST               0 (None)
-                     424 PRECALL                  2
-                     428 CALL                     2
-                     438 POP_TOP
-                     440 JUMP_FORWARD            11 (to 464)
-                 >>  442 PUSH_EXC_INFO
-                     444 WITH_EXCEPT_START
-                     446 POP_JUMP_FORWARD_IF_TRUE     4 (to 456)
-                     448 RERAISE                  2
-                 >>  450 COPY                     3
-                     452 POP_EXCEPT
-                     454 RERAISE                  1
-                 >>  456 POP_TOP
-                     458 POP_EXCEPT
-                     460 POP_TOP
-                     462 POP_TOP
+          38         340 LOAD_CONST               0 (None)
+                     342 LOAD_CONST               0 (None)
+                     344 LOAD_CONST               0 (None)
+                     346 PRECALL                  2
+                     350 CALL                     2
+                     360 POP_TOP
+                     362 JUMP_FORWARD            11 (to 386)
+                 >>  364 PUSH_EXC_INFO
+                     366 WITH_EXCEPT_START
+                     368 POP_JUMP_FORWARD_IF_TRUE     4 (to 378)
+                     370 RERAISE                  2
+                 >>  372 COPY                     3
+                     374 POP_EXCEPT
+                     376 RERAISE                  1
+                 >>  378 POP_TOP
+                     380 POP_EXCEPT
+                     382 POP_TOP
+                     384 POP_TOP
          
-          63     >>  464 LOAD_FAST                0 (event)
-                     466 RETURN_VALUE
+          55     >>  386 LOAD_FAST                0 (event)
+                     388 RETURN_VALUE
          ExceptionTable:
-           52 to 416 -> 442 [1] lasti
-           442 to 448 -> 450 [3] lasti
-           456 to 456 -> 450 [3] lasti
+           52 to 338 -> 364 [1] lasti
+           364 to 370 -> 372 [3] lasti
+           378 to 378 -> 372 [3] lasti
          consts
             None
             '\n                INSERT INTO event (search_uid, domain, actor_key, type, data) \n                VALUES(:search_uid, :domain, :actor_key, :type, :data)\n                ON CONFLICT DO NOTHING\n                RETURNING id\n            '
             'data'
             0
-            'REFRESH MATERIALIZED VIEW target'
          names      ('db', 'connect', 'sqlalchemy', 'text', 'asdict', 'json', 'dumps', 'execute', 'first', 'id', 'commit')
          varnames   ('event', 'con', 'statement', 'obj', 'result', '_id')
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py'
          name       'insert_event'
-         firstlineno 45
-         lnotab 0x02013401160102ff10081e013a012c02280122014e0128f02e11
+         firstlineno 37
+         lnotab 0x02013401160102ff10081e013a012c022801220228f02e11
       'actor'
       code
          argcount  : 1
          nlocals   : 4
          stacksize : 6
          flags     : 3
          code
@@ -561,53 +599,53 @@
             000000000000006a0300000000000000006401a6010000ab010000000000
             0000007d027409000000000000000000007c00a6010000ab010000000000
             0000007d037c01a00500000000000000000000000000000000000000007c
             027c03a6020000ab02000000000000000001007c01a00600000000000000
             00000000000000000000000000a6000000ab000000000000000000010064
             0064006400a6020000ab02000000000000000001006e0b23003100730477
             0278035900770101005900010001007c005300
-          66           0 RESUME                   0
+          58           0 RESUME                   0
          
-          67           2 LOAD_GLOBAL              0 (db)
+          59           2 LOAD_GLOBAL              0 (db)
                       14 LOAD_METHOD              1 (connect)
                       36 PRECALL                  0
                       40 CALL                     0
                       50 BEFORE_WITH
                       52 STORE_FAST               1 (con)
          
-          68          54 LOAD_GLOBAL              5 (NULL + sqlalchemy)
+          60          54 LOAD_GLOBAL              5 (NULL + sqlalchemy)
                       66 LOAD_ATTR                3 (text)
          
-          69          76 LOAD_CONST               1 ('\n                INSERT INTO actor (key, type, name) \n                VALUES(:key, :type, :name)\n                ON CONFLICT DO NOTHING\n            ')
+          61          76 LOAD_CONST               1 ('\n                INSERT INTO actor (key, type, name) \n                VALUES(:key, :type, :name)\n                ON CONFLICT DO NOTHING\n            ')
          
-          68          78 PRECALL                  1
+          60          78 PRECALL                  1
                       82 CALL                     1
                       92 STORE_FAST               2 (statement)
          
-          75          94 LOAD_GLOBAL              9 (NULL + asdict)
+          67          94 LOAD_GLOBAL              9 (NULL + asdict)
                      106 LOAD_FAST                0 (actor)
                      108 PRECALL                  1
                      112 CALL                     1
                      122 STORE_FAST               3 (obj)
          
-          76         124 LOAD_FAST                1 (con)
+          68         124 LOAD_FAST                1 (con)
                      126 LOAD_METHOD              5 (execute)
                      148 LOAD_FAST                2 (statement)
                      150 LOAD_FAST                3 (obj)
                      152 PRECALL                  2
                      156 CALL                     2
                      166 POP_TOP
          
-          77         168 LOAD_FAST                1 (con)
+          69         168 LOAD_FAST                1 (con)
                      170 LOAD_METHOD              6 (commit)
                      192 PRECALL                  0
                      196 CALL                     0
                      206 POP_TOP
          
-          67         208 LOAD_CONST               0 (None)
+          59         208 LOAD_CONST               0 (None)
                      210 LOAD_CONST               0 (None)
                      212 LOAD_CONST               0 (None)
                      214 PRECALL                  2
                      218 CALL                     2
                      228 POP_TOP
                      230 JUMP_FORWARD            11 (to 254)
                  >>  232 PUSH_EXC_INFO
@@ -618,30 +656,30 @@
                      242 POP_EXCEPT
                      244 RERAISE                  1
                  >>  246 POP_TOP
                      248 POP_EXCEPT
                      250 POP_TOP
                      252 POP_TOP
          
-          78     >>  254 LOAD_FAST                0 (actor)
+          70     >>  254 LOAD_FAST                0 (actor)
                      256 RETURN_VALUE
          ExceptionTable:
            52 to 206 -> 232 [1] lasti
            232 to 238 -> 240 [3] lasti
            246 to 246 -> 240 [3] lasti
          consts
             None
             '\n                INSERT INTO actor (key, type, name) \n                VALUES(:key, :type, :name)\n                ON CONFLICT DO NOTHING\n            '
          names      ('db', 'connect', 'sqlalchemy', 'text', 'asdict', 'execute', 'commit')
          varnames   ('actor', 'con', 'statement', 'obj')
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py'
          name       'insert_actor'
-         firstlineno 66
+         firstlineno 58
          lnotab 0x02013401160102ff10071e012c0128f62e0b
       'search'
       code
          argcount  : 1
          nlocals   : 4
          stacksize : 6
          flags     : 3
@@ -659,97 +697,97 @@
             0b000000000000000000006a0600000000000000007c0364051900000000
             0000000000a6010000ab0100000000000000007c0364053c0000007c01a0
             0700000000000000000000000000000000000000007c027c03a6020000ab
             02000000000000000001007c01a008000000000000000000000000000000
             0000000000a6000000ab0000000000000000000100640064006400a60200
             00ab02000000000000000001006e0b230031007304770278035900770101
             005900010001007c005300
-          81           0 RESUME                   0
+          73           0 RESUME                   0
          
-          82           2 LOAD_GLOBAL              0 (db)
+          74           2 LOAD_GLOBAL              0 (db)
                       14 LOAD_METHOD              1 (connect)
                       36 PRECALL                  0
                       40 CALL                     0
                       50 BEFORE_WITH
                       52 STORE_FAST               1 (con)
          
-          83          54 LOAD_GLOBAL              5 (NULL + sqlalchemy)
+          75          54 LOAD_GLOBAL              5 (NULL + sqlalchemy)
                       66 LOAD_ATTR                3 (text)
          
-          84          76 LOAD_CONST               1 ('\n                INSERT INTO search (uid, client_domain, label, meta, inclusion, exclusion, sort) \n                VALUES(:uid, :client_domain, :label, :meta, :inclusion, :exclusion, :sort)\n                ON CONFLICT DO NOTHING\n            ')
+          76          76 LOAD_CONST               1 ('\n                INSERT INTO search (uid, client_domain, label, meta, inclusion, exclusion, sort) \n                VALUES(:uid, :client_domain, :label, :meta, :inclusion, :exclusion, :sort)\n                ON CONFLICT DO NOTHING\n            ')
          
-          83          78 PRECALL                  1
+          75          78 PRECALL                  1
                       82 CALL                     1
                       92 STORE_FAST               2 (statement)
          
-          90          94 LOAD_GLOBAL              9 (NULL + asdict)
+          82          94 LOAD_GLOBAL              9 (NULL + asdict)
                      106 LOAD_FAST                0 (search)
                      108 PRECALL                  1
                      112 CALL                     1
                      122 STORE_FAST               3 (obj)
          
-          91         124 LOAD_GLOBAL             11 (NULL + json)
+          83         124 LOAD_GLOBAL             11 (NULL + json)
                      136 LOAD_ATTR                6 (dumps)
                      146 LOAD_FAST                3 (obj)
                      148 LOAD_CONST               2 ('meta')
                      150 BINARY_SUBSCR
                      160 PRECALL                  1
                      164 CALL                     1
                      174 LOAD_FAST                3 (obj)
                      176 LOAD_CONST               2 ('meta')
                      178 STORE_SUBSCR
          
-          92         182 LOAD_GLOBAL             11 (NULL + json)
+          84         182 LOAD_GLOBAL             11 (NULL + json)
                      194 LOAD_ATTR                6 (dumps)
                      204 LOAD_FAST                3 (obj)
                      206 LOAD_CONST               3 ('inclusion')
                      208 BINARY_SUBSCR
                      218 PRECALL                  1
                      222 CALL                     1
                      232 LOAD_FAST                3 (obj)
                      234 LOAD_CONST               3 ('inclusion')
                      236 STORE_SUBSCR
          
-          93         240 LOAD_GLOBAL             11 (NULL + json)
+          85         240 LOAD_GLOBAL             11 (NULL + json)
                      252 LOAD_ATTR                6 (dumps)
                      262 LOAD_FAST                3 (obj)
                      264 LOAD_CONST               4 ('exclusion')
                      266 BINARY_SUBSCR
                      276 PRECALL                  1
                      280 CALL                     1
                      290 LOAD_FAST                3 (obj)
                      292 LOAD_CONST               4 ('exclusion')
                      294 STORE_SUBSCR
          
-          94         298 LOAD_GLOBAL             11 (NULL + json)
+          86         298 LOAD_GLOBAL             11 (NULL + json)
                      310 LOAD_ATTR                6 (dumps)
                      320 LOAD_FAST                3 (obj)
                      322 LOAD_CONST               5 ('sort')
                      324 BINARY_SUBSCR
                      334 PRECALL                  1
                      338 CALL                     1
                      348 LOAD_FAST                3 (obj)
                      350 LOAD_CONST               5 ('sort')
                      352 STORE_SUBSCR
          
-          95         356 LOAD_FAST                1 (con)
+          87         356 LOAD_FAST                1 (con)
                      358 LOAD_METHOD              7 (execute)
                      380 LOAD_FAST                2 (statement)
                      382 LOAD_FAST                3 (obj)
                      384 PRECALL                  2
                      388 CALL                     2
                      398 POP_TOP
          
-          96         400 LOAD_FAST                1 (con)
+          88         400 LOAD_FAST                1 (con)
                      402 LOAD_METHOD              8 (commit)
                      424 PRECALL                  0
                      428 CALL                     0
                      438 POP_TOP
          
-          82         440 LOAD_CONST               0 (None)
+          74         440 LOAD_CONST               0 (None)
                      442 LOAD_CONST               0 (None)
                      444 LOAD_CONST               0 (None)
                      446 PRECALL                  2
                      450 CALL                     2
                      460 POP_TOP
                      462 JUMP_FORWARD            11 (to 486)
                  >>  464 PUSH_EXC_INFO
@@ -760,15 +798,15 @@
                      474 POP_EXCEPT
                      476 RERAISE                  1
                  >>  478 POP_TOP
                      480 POP_EXCEPT
                      482 POP_TOP
                      484 POP_TOP
          
-          97     >>  486 LOAD_FAST                0 (search)
+          89     >>  486 LOAD_FAST                0 (search)
                      488 RETURN_VALUE
          ExceptionTable:
            52 to 438 -> 464 [1] lasti
            464 to 470 -> 472 [3] lasti
            478 to 478 -> 472 [3] lasti
          consts
             None
@@ -779,15 +817,15 @@
             'sort'
          names      ('db', 'connect', 'sqlalchemy', 'text', 'asdict', 'json', 'dumps', 'execute', 'commit')
          varnames   ('search', 'con', 'statement', 'obj')
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py'
          name       'insert_search'
-         firstlineno 81
+         firstlineno 73
          lnotab 0x02013401160102ff10071e013a013a013a013a012c0128f22e0f
       'checkpoint'
       code
          argcount  : 1
          nlocals   : 3
          stacksize : 7
          flags     : 3
@@ -797,50 +835,50 @@
             000000000000006a0300000000000000006401a6010000ab010000000000
             0000007d027c01a00400000000000000000000000000000000000000007c
             02740b000000000000000000007c00a6010000ab010000000000000000a6
             020000ab02000000000000000001007c01a0060000000000000000000000
             000000000000000000a6000000ab00000000000000000001006400640064
             00a6020000ab02000000000000000001006e0b2300310073047702780359
             00770101005900010001007c005300
-         100           0 RESUME                   0
+          92           0 RESUME                   0
          
-         101           2 LOAD_GLOBAL              0 (db)
+          93           2 LOAD_GLOBAL              0 (db)
                       14 LOAD_METHOD              1 (connect)
                       36 PRECALL                  0
                       40 CALL                     0
                       50 BEFORE_WITH
                       52 STORE_FAST               1 (con)
          
-         102          54 LOAD_GLOBAL              5 (NULL + sqlalchemy)
+          94          54 LOAD_GLOBAL              5 (NULL + sqlalchemy)
                       66 LOAD_ATTR                3 (text)
          
-         103          76 LOAD_CONST               1 ('\n                INSERT INTO checkpoint (event_id) \n                VALUES(:event_id)\n            ')
+          95          76 LOAD_CONST               1 ('\n                INSERT INTO checkpoint (event_id) \n                VALUES(:event_id)\n            ')
          
-         102          78 PRECALL                  1
+          94          78 PRECALL                  1
                       82 CALL                     1
                       92 STORE_FAST               2 (statement)
          
-         108          94 LOAD_FAST                1 (con)
+         100          94 LOAD_FAST                1 (con)
                       96 LOAD_METHOD              4 (execute)
                      118 LOAD_FAST                2 (statement)
                      120 LOAD_GLOBAL             11 (NULL + asdict)
                      132 LOAD_FAST                0 (checkpoint)
                      134 PRECALL                  1
                      138 CALL                     1
                      148 PRECALL                  2
                      152 CALL                     2
                      162 POP_TOP
          
-         109         164 LOAD_FAST                1 (con)
+         101         164 LOAD_FAST                1 (con)
                      166 LOAD_METHOD              6 (commit)
                      188 PRECALL                  0
                      192 CALL                     0
                      202 POP_TOP
          
-         101         204 LOAD_CONST               0 (None)
+          93         204 LOAD_CONST               0 (None)
                      206 LOAD_CONST               0 (None)
                      208 LOAD_CONST               0 (None)
                      210 PRECALL                  2
                      214 CALL                     2
                      224 POP_TOP
                      226 JUMP_FORWARD            11 (to 250)
                  >>  228 PUSH_EXC_INFO
@@ -851,814 +889,1176 @@
                      238 POP_EXCEPT
                      240 RERAISE                  1
                  >>  242 POP_TOP
                      244 POP_EXCEPT
                      246 POP_TOP
                      248 POP_TOP
          
-         110     >>  250 LOAD_FAST                0 (checkpoint)
+         102     >>  250 LOAD_FAST                0 (checkpoint)
                      252 RETURN_VALUE
          ExceptionTable:
            52 to 202 -> 228 [1] lasti
            228 to 234 -> 236 [3] lasti
            242 to 242 -> 236 [3] lasti
          consts
             None
             '\n                INSERT INTO checkpoint (event_id) \n                VALUES(:event_id)\n            '
          names      ('db', 'connect', 'sqlalchemy', 'text', 'execute', 'asdict', 'commit')
          varnames   ('checkpoint', 'con', 'statement')
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py'
          name       'insert_checkpoint'
-         firstlineno 100
+         firstlineno 92
          lnotab 0x02013401160102ff1006460128f82e09
       'domains'
       'search_uid'
       'actor_key'
+      'last_event_type'
       code
-         argcount  : 3
-         nlocals   : 6
+         argcount  : 4
+         nlocals   : 7
          stacksize : 10
          flags     : 3
          code
             0x97007401000000000000000000007c01ac01a6010000ab010000000000
-            0000007d03740200000000000000000000a0020000000000000000000000
-            000000000000000000a6000000ab00000000000000000035007d047c0044
-            0090015d157d057c05a00300000000000000000000000000000000000000
-            00a6000000ab000000000000000000a00400000000000000000000000000
-            00000000000000a6000000ab000000000000000000a00500000000000000
-            0000000000000000000000000064026403a6020000ab0200000000000000
-            00a005000000000000000000000000000000000000000064046403a60200
-            00ab020000000000000000a0050000000000000000000000000000000000
-            00000064046403a6020000ab0200000000000000007d057c036405190000
-            000000000000006a060000000000000000a0070000000000000000000000
-            0000000000000000007c05a6010000ab010000000000000000a008000000
-            0000000000000000000000000000000000a6000000ab0000000000000000
-            00721474130000000000000000000064067c059b0064079d03a6010000ab
-            01000000000000000001008cab74130000000000000000000064087c059b
-            0064099d03a6010000ab01000000000000000001007c04a00a0000000000
-            0000000000000000000000000000007417000000000000000000006a0c00
-            00000000000000640aa6010000ab01000000000000000064057c056901a6
-            020000ab02000000000000000001007c04a00a0000000000000000000000
-            0000000000000000007417000000000000000000006a0c00000000000000
-            00640ba6010000ab0100000000000000007c017c027c05640c640d9c04a6
-            020000ab020000000000000000010090018c177c04a00a00000000000000
-            000000000000000000000000007417000000000000000000006a0c000000
-            0000000000640ea6010000ab010000000000000000a6010000ab01000000
-            000000000001007c04a00d00000000000000000000000000000000000000
-            00a6000000ab0000000000000000000100640f640f640fa6020000ab0200
-            000000000000000100640f53002300310073047702780359007701010059
-            0001000100640f5300
-         113           0 RESUME                   0
+            000000640219000000000000000000a00100000000000000000000000000
+            00000000000000a6000000ab0000000000000000007d0474040000000000
+            0000000000a0030000000000000000000000000000000000000000a60000
+            00ab00000000000000000035007d057c0044005db07d0664037c06760172
+            1474090000000000000000000064047c069b0064059d03a6010000ab0100
+            0000000000000001008c1a740b000000000000000000006a060000000000
+            0000007c06a6010000ab0100000000000000007d067c067c047600721474
+            090000000000000000000064047c069b0064069d03a6010000ab01000000
+            000000000001008c4674090000000000000000000064077c069b0064089d
+            03a6010000ab01000000000000000001007c05a007000000000000000000
+            00000000000000000000007411000000000000000000006a090000000000
+            0000006409a6010000ab01000000000000000064027c066901a6020000ab
+            02000000000000000001007c05a007000000000000000000000000000000
+            00000000007411000000000000000000006a090000000000000000640aa6
+            010000ab0100000000000000007c017c027c067c03640b9c04a6020000ab
+            02000000000000000001008cb17c05a00a00000000000000000000000000
+            00000000000000a6000000ab0000000000000000000100640c640c640ca6
+            020000ab0200000000000000000100640c53002300310073047702780359
+            0077010100590001000100640c5300
+         105           0 RESUME                   0
          
-         121           2 LOAD_GLOBAL              1 (NULL + target)
+         113           2 LOAD_GLOBAL              1 (NULL + unique_domains)
                       14 LOAD_FAST                1 (search_uid)
                       16 KW_NAMES                 1
                       18 PRECALL                  1
                       22 CALL                     1
-                      32 STORE_FAST               3 (targets)
          
-         122          34 LOAD_GLOBAL              2 (db)
-                      46 LOAD_METHOD              2 (connect)
-                      68 PRECALL                  0
-                      72 CALL                     0
-                      82 BEFORE_WITH
-                      84 STORE_FAST               4 (con)
-         
-         123          86 LOAD_FAST                0 (domains)
-                      88 GET_ITER
-                 >>   90 EXTENDED_ARG             1
-                      92 FOR_ITER               277 (to 648)
-                      94 STORE_FAST               5 (domain)
-         
-         126          96 LOAD_FAST                5 (domain)
-                      98 LOAD_METHOD              3 (lower)
-                     120 PRECALL                  0
-                     124 CALL                     0
-         
-         127         134 LOAD_METHOD              4 (strip)
-                     156 PRECALL                  0
-                     160 CALL                     0
-         
-         128         170 LOAD_METHOD              5 (replace)
-                     192 LOAD_CONST               2 ('www.')
-                     194 LOAD_CONST               3 ('')
-                     196 PRECALL                  2
-                     200 CALL                     2
-         
-         129         210 LOAD_METHOD              5 (replace)
-                     232 LOAD_CONST               4 ('https://')
-                     234 LOAD_CONST               3 ('')
-                     236 PRECALL                  2
-                     240 CALL                     2
+         114          32 LOAD_CONST               2 ('domain')
          
-         130         250 LOAD_METHOD              5 (replace)
-                     272 LOAD_CONST               4 ('https://')
-                     274 LOAD_CONST               3 ('')
-                     276 PRECALL                  2
-                     280 CALL                     2
+         113          34 BINARY_SUBSCR
+         
+         115          44 LOAD_METHOD              1 (to_list)
+                      66 PRECALL                  0
+                      70 CALL                     0
+         
+         113          80 STORE_FAST               4 (existing_search_domains)
+         
+         116          82 LOAD_GLOBAL              4 (db)
+                      94 LOAD_METHOD              3 (connect)
+                     116 PRECALL                  0
+                     120 CALL                     0
+                     130 BEFORE_WITH
+                     132 STORE_FAST               5 (con)
+         
+         117         134 LOAD_FAST                0 (domains)
+                     136 GET_ITER
+                 >>  138 FOR_ITER               176 (to 492)
+                     140 STORE_FAST               6 (domain)
+         
+         118         142 LOAD_CONST               3 ('.')
+                     144 LOAD_FAST                6 (domain)
+                     146 CONTAINS_OP              1
+                     148 POP_JUMP_FORWARD_IF_FALSE    20 (to 190)
+         
+         119         150 LOAD_GLOBAL              9 (NULL + print)
+                     162 LOAD_CONST               4 ('Skipping ')
+                     164 LOAD_FAST                6 (domain)
+                     166 FORMAT_VALUE             0
+                     168 LOAD_CONST               5 (' as not a valid domain')
+                     170 BUILD_STRING             3
+                     172 PRECALL                  1
+                     176 CALL                     1
+                     186 POP_TOP
          
-         125         290 STORE_FAST               5 (domain)
+         120         188 JUMP_BACKWARD           26 (to 138)
          
-         132         292 LOAD_FAST                3 (targets)
-                     294 LOAD_CONST               5 ('domain')
-                     296 BINARY_SUBSCR
-                     306 LOAD_ATTR                6 (str)
-                     316 LOAD_METHOD              7 (contains)
-                     338 LOAD_FAST                5 (domain)
-                     340 PRECALL                  1
-                     344 CALL                     1
-                     354 LOAD_METHOD              8 (any)
-                     376 PRECALL                  0
-                     380 CALL                     0
-                     390 POP_JUMP_FORWARD_IF_FALSE    20 (to 432)
-         
-         133         392 LOAD_GLOBAL             19 (NULL + print)
-                     404 LOAD_CONST               6 ('Skipping ')
-                     406 LOAD_FAST                5 (domain)
-                     408 FORMAT_VALUE             0
-                     410 LOAD_CONST               7 (' as already a target')
-                     412 BUILD_STRING             3
-                     414 PRECALL                  1
-                     418 CALL                     1
-                     428 POP_TOP
-         
-         134         430 JUMP_BACKWARD          171 (to 90)
-         
-         136     >>  432 LOAD_GLOBAL             19 (NULL + print)
-                     444 LOAD_CONST               8 ('Adding ')
-                     446 LOAD_FAST                5 (domain)
-                     448 FORMAT_VALUE             0
-                     450 LOAD_CONST               9 (' as target')
-                     452 BUILD_STRING             3
-                     454 PRECALL                  1
-                     458 CALL                     1
-                     468 POP_TOP
-         
-         138         470 LOAD_FAST                4 (con)
-                     472 LOAD_METHOD             10 (execute)
-         
-         139         494 LOAD_GLOBAL             23 (NULL + sqlalchemy)
-                     506 LOAD_ATTR               12 (text)
-         
-         140         516 LOAD_CONST              10 ('\n                    INSERT INTO company (domain) \n                    VALUES(:domain)\n                    ON CONFLICT DO NOTHING\n                    ')
-         
-         139         518 PRECALL                  1
-                     522 CALL                     1
-         
-         146         532 LOAD_CONST               5 ('domain')
-                     534 LOAD_FAST                5 (domain)
-                     536 BUILD_MAP                1
+         122     >>  190 LOAD_GLOBAL             11 (NULL + helpers)
+                     202 LOAD_ATTR                6 (clean_domain)
+                     212 LOAD_FAST                6 (domain)
+                     214 PRECALL                  1
+                     218 CALL                     1
+                     228 STORE_FAST               6 (domain)
+         
+         124         230 LOAD_FAST                6 (domain)
+                     232 LOAD_FAST                4 (existing_search_domains)
+                     234 CONTAINS_OP              0
+                     236 POP_JUMP_FORWARD_IF_FALSE    20 (to 278)
+         
+         125         238 LOAD_GLOBAL              9 (NULL + print)
+                     250 LOAD_CONST               4 ('Skipping ')
+                     252 LOAD_FAST                6 (domain)
+                     254 FORMAT_VALUE             0
+                     256 LOAD_CONST               6 (' as already a target')
+                     258 BUILD_STRING             3
+                     260 PRECALL                  1
+                     264 CALL                     1
+                     274 POP_TOP
+         
+         126         276 JUMP_BACKWARD           70 (to 138)
+         
+         128     >>  278 LOAD_GLOBAL              9 (NULL + print)
+                     290 LOAD_CONST               7 ('Adding ')
+                     292 LOAD_FAST                6 (domain)
+                     294 FORMAT_VALUE             0
+                     296 LOAD_CONST               8 (' as target')
+                     298 BUILD_STRING             3
+                     300 PRECALL                  1
+                     304 CALL                     1
+                     314 POP_TOP
+         
+         131         316 LOAD_FAST                5 (con)
+                     318 LOAD_METHOD              7 (execute)
+         
+         132         340 LOAD_GLOBAL             17 (NULL + sqlalchemy)
+                     352 LOAD_ATTR                9 (text)
+         
+         133         362 LOAD_CONST               9 ('\n                    INSERT INTO company (domain) \n                    VALUES(:domain)\n                    ON CONFLICT DO NOTHING\n                    ')
+         
+         132         364 PRECALL                  1
+                     368 CALL                     1
+         
+         139         378 LOAD_CONST               2 ('domain')
+                     380 LOAD_FAST                6 (domain)
+                     382 BUILD_MAP                1
          
-         138         538 PRECALL                  2
-                     542 CALL                     2
-                     552 POP_TOP
+         131         384 PRECALL                  2
+                     388 CALL                     2
+                     398 POP_TOP
+         
+         142         400 LOAD_FAST                5 (con)
+                     402 LOAD_METHOD              7 (execute)
          
-         149         554 LOAD_FAST                4 (con)
-                     556 LOAD_METHOD             10 (execute)
+         143         424 LOAD_GLOBAL             17 (NULL + sqlalchemy)
+                     436 LOAD_ATTR                9 (text)
          
-         150         578 LOAD_GLOBAL             23 (NULL + sqlalchemy)
-                     590 LOAD_ATTR               12 (text)
+         144         446 LOAD_CONST              10 ('\n                    INSERT INTO event (search_uid, domain, actor_key, type) \n                    VALUES(:search_uid, :domain, :actor_key, :type)\n                    ')
          
-         151         600 LOAD_CONST              11 ('\n                    INSERT INTO event (search_uid, domain, actor_key, type) \n                    VALUES(:search_uid, :domain, :actor_key, :type)\n                    ')
+         143         448 PRECALL                  1
+                     452 CALL                     1
          
-         150         602 PRECALL                  1
-                     606 CALL                     1
-         
-         157         616 LOAD_FAST                1 (search_uid)
-         
-         158         618 LOAD_FAST                2 (actor_key)
-         
-         159         620 LOAD_FAST                5 (domain)
-         
-         160         622 LOAD_CONST              12 ('advance')
-         
-         156         624 LOAD_CONST              13 (('search_uid', 'actor_key', 'domain', 'type'))
-                     626 BUILD_CONST_KEY_MAP      4
-         
-         149         628 PRECALL                  2
-                     632 CALL                     2
-                     642 POP_TOP
-                     644 EXTENDED_ARG             1
-                     646 JUMP_BACKWARD          279 (to 90)
-         
-         163     >>  648 LOAD_FAST                4 (con)
-                     650 LOAD_METHOD             10 (execute)
-                     672 LOAD_GLOBAL             23 (NULL + sqlalchemy)
-                     684 LOAD_ATTR               12 (text)
-                     694 LOAD_CONST              14 ('REFRESH MATERIALIZED VIEW target')
-                     696 PRECALL                  1
-                     700 CALL                     1
-                     710 PRECALL                  1
-                     714 CALL                     1
-                     724 POP_TOP
-         
-         164         726 LOAD_FAST                4 (con)
-                     728 LOAD_METHOD             13 (commit)
-                     750 PRECALL                  0
-                     754 CALL                     0
-                     764 POP_TOP
-         
-         122         766 LOAD_CONST              15 (None)
-                     768 LOAD_CONST              15 (None)
-                     770 LOAD_CONST              15 (None)
-                     772 PRECALL                  2
-                     776 CALL                     2
-                     786 POP_TOP
-                     788 LOAD_CONST              15 (None)
-                     790 RETURN_VALUE
-                 >>  792 PUSH_EXC_INFO
-                     794 WITH_EXCEPT_START
-                     796 POP_JUMP_FORWARD_IF_TRUE     4 (to 806)
-                     798 RERAISE                  2
-                 >>  800 COPY                     3
-                     802 POP_EXCEPT
-                     804 RERAISE                  1
-                 >>  806 POP_TOP
-                     808 POP_EXCEPT
-                     810 POP_TOP
-                     812 POP_TOP
-                     814 LOAD_CONST              15 (None)
-                     816 RETURN_VALUE
-         ExceptionTable:
-           84 to 764 -> 792 [1] lasti
-           792 to 798 -> 800 [3] lasti
-           806 to 806 -> 800 [3] lasti
+         150         462 LOAD_FAST                1 (search_uid)
+         
+         151         464 LOAD_FAST                2 (actor_key)
+         
+         152         466 LOAD_FAST                6 (domain)
+         
+         153         468 LOAD_FAST                3 (last_event_type)
+         
+         149         470 LOAD_CONST              11 (('search_uid', 'actor_key', 'domain', 'type'))
+                     472 BUILD_CONST_KEY_MAP      4
+         
+         142         474 PRECALL                  2
+                     478 CALL                     2
+                     488 POP_TOP
+                     490 JUMP_BACKWARD          177 (to 138)
+         
+         157     >>  492 LOAD_FAST                5 (con)
+                     494 LOAD_METHOD             10 (commit)
+                     516 PRECALL                  0
+                     520 CALL                     0
+                     530 POP_TOP
+         
+         116         532 LOAD_CONST              12 (None)
+                     534 LOAD_CONST              12 (None)
+                     536 LOAD_CONST              12 (None)
+                     538 PRECALL                  2
+                     542 CALL                     2
+                     552 POP_TOP
+                     554 LOAD_CONST              12 (None)
+                     556 RETURN_VALUE
+                 >>  558 PUSH_EXC_INFO
+                     560 WITH_EXCEPT_START
+                     562 POP_JUMP_FORWARD_IF_TRUE     4 (to 572)
+                     564 RERAISE                  2
+                 >>  566 COPY                     3
+                     568 POP_EXCEPT
+                     570 RERAISE                  1
+                 >>  572 POP_TOP
+                     574 POP_EXCEPT
+                     576 POP_TOP
+                     578 POP_TOP
+                     580 LOAD_CONST              12 (None)
+                     582 RETURN_VALUE
+         ExceptionTable:
+           132 to 530 -> 558 [1] lasti
+           558 to 564 -> 566 [3] lasti
+           572 to 572 -> 566 [3] lasti
          consts
             '\n    Takes in domains, inserts targets into a review stage, where they will\n    try to be enriched on process event\n\n    '
             ('search_uid',)
-            'www.'
-            ''
-            'https://'
             'domain'
+            '.'
             'Skipping '
+            ' as not a valid domain'
             ' as already a target'
             'Adding '
             ' as target'
             '\n                    INSERT INTO company (domain) \n                    VALUES(:domain)\n                    ON CONFLICT DO NOTHING\n                    '
             '\n                    INSERT INTO event (search_uid, domain, actor_key, type) \n                    VALUES(:search_uid, :domain, :actor_key, :type)\n                    '
-            'advance'
             ('search_uid', 'actor_key', 'domain', 'type')
-            'REFRESH MATERIALIZED VIEW target'
             None
-         names      ('target', 'db', 'connect', 'lower', 'strip', 'replace', 'str', 'contains', 'any', 'print', 'execute', 'sqlalchemy', 'text', 'commit')
-         varnames   ('domains', 'search_uid', 'actor_key', 'targets', 'con', 'domain')
+         names      ('unique_domains', 'to_list', 'db', 'connect', 'print', 'helpers', 'clean_domain', 'execute', 'sqlalchemy', 'text', 'commit')
+         varnames   ('domains', 'search_uid', 'actor_key', 'last_event_type', 'existing_search_domains', 'con', 'domain')
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py'
-         name       'insert_and_advance_targets_from_domains'
-         firstlineno 113
+         name       'insert_targets_from_domains'
+         firstlineno 105
          lnotab
-            0x0208200134010a03260124012801280128fb0207640126010202260218
-            01160102ff0e0706f8100b1801160102ff0e0702010201020102fc04f914
-            0e4e0128d6
+            0x02081e0102ff0a0224fe02033401080108012601020228020801260102
+            0226031801160102ff0e0706f8100b1801160102ff0e0702010201020102
+            fc04f9120f28d7
       'companies'
       code
          argcount  : 3
          nlocals   : 6
          stacksize : 10
          flags     : 3
          code
             0x97007401000000000000000000007c01ac01a6010000ab010000000000
-            0000007d03740200000000000000000000a0020000000000000000000000
-            000000000000000000a6000000ab00000000000000000035007d047c0044
-            0090015d3c7d057c05a00300000000000000000000000000000000000000
-            006402a6010000ab01000000000000000080147409000000000000000000
-            0064037c059b0064049d03a6010000ab01000000000000000001008c2c7c
-            036402190000000000000000006a050000000000000000a0060000000000
-            0000000000000000000000000000007c05640219000000000000000000a6
-            010000ab010000000000000000a007000000000000000000000000000000
-            0000000000a6000000ab000000000000000000721a740900000000000000
-            00000064057c056402190000000000000000009b0064069d03a6010000ab
-            01000000000000000001008c7e74090000000000000000000064077c0564
-            02190000000000000000009b0064089d03a6010000ab0100000000000000
-            0001007c04a0080000000000000000000000000000000000000000741300
-            0000000000000000006a0a00000000000000006409a6010000ab01000000
-            00000000007c05a003000000000000000000000000000000000000000064
-            02a6010000ab0100000000000000007c05a0030000000000000000000000
-            000000000000000000640aa6010000ab0100000000000000007c05a00300
-            00000000000000000000000000000000000000640ba6010000ab01000000
-            0000000000640c9c03a6020000ab02000000000000000001007c04a00800
-            000000000000000000000000000000000000007413000000000000000000
-            006a0a0000000000000000640da6010000ab0100000000000000007c017c
-            027c05a00300000000000000000000000000000000000000006402a60100
-            00ab010000000000000000640e640f9c04a6020000ab0200000000000000
-            00010090018c3e7c04a00800000000000000000000000000000000000000
-            007413000000000000000000006a0a00000000000000006410a6010000ab
-            010000000000000000a6010000ab01000000000000000001007c04a00b00
-            00000000000000000000000000000000000000a6000000ab000000000000
-            0000000100640064006400a6020000ab0200000000000000000100640053
-            002300310073047702780359007701010059000100010064005300
-         167           0 RESUME                   0
+            000000640219000000000000000000a00100000000000000000000000000
+            00000000000000a6000000ab0000000000000000007d0374040000000000
+            0000000000a0030000000000000000000000000000000000000000a60000
+            00ab00000000000000000035007d047c00440090015d0e7d057c05a00400
+            000000000000000000000000000000000000006402a6010000ab01000000
+            00000000008014740b0000000000000000000064047c059b0064059d03a6
+            010000ab01000000000000000001008c2c7c056402190000000000000000
+            007c037600721a740b0000000000000000000064067c0564021900000000
+            00000000009b0064079d03a6010000ab01000000000000000001008c5074
+            0b0000000000000000000064087c056402190000000000000000009b0064
+            099d03a6010000ab01000000000000000001007c04a00600000000000000
+            00000000000000000000000000740f000000000000000000006a08000000
+            0000000000640aa6010000ab0100000000000000007c05a0040000000000
+            0000000000000000000000000000006402a6010000ab0100000000000000
+            007c05a0040000000000000000000000000000000000000000640ba60100
+            00ab0100000000000000007c05a004000000000000000000000000000000
+            0000000000640ca6010000ab010000000000000000640d9c03a6020000ab
+            02000000000000000001007c04a006000000000000000000000000000000
+            0000000000740f000000000000000000006a080000000000000000640ea6
+            010000ab0100000000000000007c017c027c05a004000000000000000000
+            00000000000000000000006402a6010000ab010000000000000000640f64
+            109c04a6020000ab020000000000000000010090018c107c04a009000000
+            0000000000000000000000000000000000a6000000ab0000000000000000
+            000100640364036403a6020000ab02000000000000000001006403530023
+            00310073047702780359007701010059000100010064035300
+         160           0 RESUME                   0
          
-         170           2 LOAD_GLOBAL              1 (NULL + target)
+         164           2 LOAD_GLOBAL              1 (NULL + unique_domains)
                       14 LOAD_FAST                1 (search_uid)
                       16 KW_NAMES                 1
                       18 PRECALL                  1
                       22 CALL                     1
-                      32 STORE_FAST               3 (targets)
-         
-         171          34 LOAD_GLOBAL              2 (db)
-                      46 LOAD_METHOD              2 (connect)
-                      68 PRECALL                  0
-                      72 CALL                     0
-                      82 BEFORE_WITH
-                      84 STORE_FAST               4 (con)
-         
-         172          86 LOAD_FAST                0 (companies)
-                      88 GET_ITER
-                 >>   90 EXTENDED_ARG             1
-                      92 FOR_ITER               316 (to 726)
-                      94 STORE_FAST               5 (company)
-         
-         173          96 LOAD_FAST                5 (company)
-                      98 LOAD_METHOD              3 (get)
-                     120 LOAD_CONST               2 ('domain')
-                     122 PRECALL                  1
-                     126 CALL                     1
-                     136 POP_JUMP_FORWARD_IF_NOT_NONE    20 (to 178)
-         
-         174         138 LOAD_GLOBAL              9 (NULL + print)
-                     150 LOAD_CONST               3 ('Missing domain: ')
-                     152 LOAD_FAST                5 (company)
-                     154 FORMAT_VALUE             0
-                     156 LOAD_CONST               4 ('. Skipping')
-                     158 BUILD_STRING             3
-                     160 PRECALL                  1
-                     164 CALL                     1
-                     174 POP_TOP
-         
-         175         176 JUMP_BACKWARD           44 (to 90)
-         
-         178     >>  178 LOAD_FAST                3 (targets)
-                     180 LOAD_CONST               2 ('domain')
-                     182 BINARY_SUBSCR
-                     192 LOAD_ATTR                5 (str)
-                     202 LOAD_METHOD              6 (contains)
-                     224 LOAD_FAST                5 (company)
-                     226 LOAD_CONST               2 ('domain')
-                     228 BINARY_SUBSCR
-                     238 PRECALL                  1
-                     242 CALL                     1
-                     252 LOAD_METHOD              7 (any)
-                     274 PRECALL                  0
-                     278 CALL                     0
-                     288 POP_JUMP_FORWARD_IF_FALSE    26 (to 342)
-         
-         179         290 LOAD_GLOBAL              9 (NULL + print)
-                     302 LOAD_CONST               5 ('Skipping ')
-                     304 LOAD_FAST                5 (company)
-                     306 LOAD_CONST               2 ('domain')
-                     308 BINARY_SUBSCR
-                     318 FORMAT_VALUE             0
-                     320 LOAD_CONST               6 (' as already a target')
-                     322 BUILD_STRING             3
-                     324 PRECALL                  1
-                     328 CALL                     1
-                     338 POP_TOP
-         
-         180         340 JUMP_BACKWARD          126 (to 90)
+                      32 LOAD_CONST               2 ('domain')
+                      34 BINARY_SUBSCR
+                      44 LOAD_METHOD              1 (to_list)
+                      66 PRECALL                  0
+                      70 CALL                     0
+                      80 STORE_FAST               3 (existing_search_domains)
+         
+         165          82 LOAD_GLOBAL              4 (db)
+                      94 LOAD_METHOD              3 (connect)
+                     116 PRECALL                  0
+                     120 CALL                     0
+                     130 BEFORE_WITH
+                     132 STORE_FAST               4 (con)
+         
+         166         134 LOAD_FAST                0 (companies)
+                     136 GET_ITER
+                 >>  138 EXTENDED_ARG             1
+                     140 FOR_ITER               270 (to 682)
+                     142 STORE_FAST               5 (company)
+         
+         167         144 LOAD_FAST                5 (company)
+                     146 LOAD_METHOD              4 (get)
+                     168 LOAD_CONST               2 ('domain')
+                     170 PRECALL                  1
+                     174 CALL                     1
+                     184 POP_JUMP_FORWARD_IF_NOT_NONE    20 (to 226)
+         
+         168         186 LOAD_GLOBAL             11 (NULL + print)
+                     198 LOAD_CONST               4 ('Missing domain: ')
+                     200 LOAD_FAST                5 (company)
+                     202 FORMAT_VALUE             0
+                     204 LOAD_CONST               5 ('. Skipping')
+                     206 BUILD_STRING             3
+                     208 PRECALL                  1
+                     212 CALL                     1
+                     222 POP_TOP
          
-         182     >>  342 LOAD_GLOBAL              9 (NULL + print)
-                     354 LOAD_CONST               7 ('Adding ')
-                     356 LOAD_FAST                5 (company)
-                     358 LOAD_CONST               2 ('domain')
-                     360 BINARY_SUBSCR
-                     370 FORMAT_VALUE             0
-                     372 LOAD_CONST               8 (' as target')
-                     374 BUILD_STRING             3
-                     376 PRECALL                  1
-                     380 CALL                     1
-                     390 POP_TOP
-         
-         184         392 LOAD_FAST                4 (con)
-                     394 LOAD_METHOD              8 (execute)
-         
-         185         416 LOAD_GLOBAL             19 (NULL + sqlalchemy)
-                     428 LOAD_ATTR               10 (text)
-         
-         186         438 LOAD_CONST               9 ('\n                    INSERT INTO company (domain, name, description) \n                    VALUES(:domain, :name, :description)\n                    ON CONFLICT DO NOTHING\n                    ')
-         
-         185         440 PRECALL                  1
-                     444 CALL                     1
-         
-         193         454 LOAD_FAST                5 (company)
-                     456 LOAD_METHOD              3 (get)
-                     478 LOAD_CONST               2 ('domain')
-                     480 PRECALL                  1
-                     484 CALL                     1
-         
-         194         494 LOAD_FAST                5 (company)
-                     496 LOAD_METHOD              3 (get)
-                     518 LOAD_CONST              10 ('name')
-                     520 PRECALL                  1
-                     524 CALL                     1
-         
-         195         534 LOAD_FAST                5 (company)
-                     536 LOAD_METHOD              3 (get)
-                     558 LOAD_CONST              11 ('description')
-                     560 PRECALL                  1
-                     564 CALL                     1
-         
-         192         574 LOAD_CONST              12 (('domain', 'name', 'description'))
-                     576 BUILD_CONST_KEY_MAP      3
-         
-         184         578 PRECALL                  2
-                     582 CALL                     2
-                     592 POP_TOP
-         
-         199         594 LOAD_FAST                4 (con)
-                     596 LOAD_METHOD              8 (execute)
+         169         224 JUMP_BACKWARD           44 (to 138)
          
-         200         618 LOAD_GLOBAL             19 (NULL + sqlalchemy)
-                     630 LOAD_ATTR               10 (text)
+         172     >>  226 LOAD_FAST                5 (company)
+                     228 LOAD_CONST               2 ('domain')
+                     230 BINARY_SUBSCR
+                     240 LOAD_FAST                3 (existing_search_domains)
+                     242 CONTAINS_OP              0
+                     244 POP_JUMP_FORWARD_IF_FALSE    26 (to 298)
+         
+         173         246 LOAD_GLOBAL             11 (NULL + print)
+                     258 LOAD_CONST               6 ('Skipping ')
+                     260 LOAD_FAST                5 (company)
+                     262 LOAD_CONST               2 ('domain')
+                     264 BINARY_SUBSCR
+                     274 FORMAT_VALUE             0
+                     276 LOAD_CONST               7 (' as already a target')
+                     278 BUILD_STRING             3
+                     280 PRECALL                  1
+                     284 CALL                     1
+                     294 POP_TOP
          
-         201         640 LOAD_CONST              13 ('\n                    INSERT INTO event (search_uid, domain, actor_key, type) \n                    VALUES(:search_uid, :domain, :actor_key, :type)\n                    ')
+         174         296 JUMP_BACKWARD           80 (to 138)
          
-         200         642 PRECALL                  1
+         176     >>  298 LOAD_GLOBAL             11 (NULL + print)
+                     310 LOAD_CONST               8 ('Adding ')
+                     312 LOAD_FAST                5 (company)
+                     314 LOAD_CONST               2 ('domain')
+                     316 BINARY_SUBSCR
+                     326 FORMAT_VALUE             0
+                     328 LOAD_CONST               9 (' as target')
+                     330 BUILD_STRING             3
+                     332 PRECALL                  1
+                     336 CALL                     1
+                     346 POP_TOP
+         
+         178         348 LOAD_FAST                4 (con)
+                     350 LOAD_METHOD              6 (execute)
+         
+         179         372 LOAD_GLOBAL             15 (NULL + sqlalchemy)
+                     384 LOAD_ATTR                8 (text)
+         
+         180         394 LOAD_CONST              10 ('\n                    INSERT INTO company (domain, name, description) \n                    VALUES(:domain, :name, :description)\n                    ON CONFLICT DO NOTHING\n                    ')
+         
+         179         396 PRECALL                  1
+                     400 CALL                     1
+         
+         187         410 LOAD_FAST                5 (company)
+                     412 LOAD_METHOD              4 (get)
+                     434 LOAD_CONST               2 ('domain')
+                     436 PRECALL                  1
+                     440 CALL                     1
+         
+         188         450 LOAD_FAST                5 (company)
+                     452 LOAD_METHOD              4 (get)
+                     474 LOAD_CONST              11 ('name')
+                     476 PRECALL                  1
+                     480 CALL                     1
+         
+         189         490 LOAD_FAST                5 (company)
+                     492 LOAD_METHOD              4 (get)
+                     514 LOAD_CONST              12 ('description')
+                     516 PRECALL                  1
+                     520 CALL                     1
+         
+         186         530 LOAD_CONST              13 (('domain', 'name', 'description'))
+                     532 BUILD_CONST_KEY_MAP      3
+         
+         178         534 PRECALL                  2
+                     538 CALL                     2
+                     548 POP_TOP
+         
+         193         550 LOAD_FAST                4 (con)
+                     552 LOAD_METHOD              6 (execute)
+         
+         194         574 LOAD_GLOBAL             15 (NULL + sqlalchemy)
+                     586 LOAD_ATTR                8 (text)
+         
+         195         596 LOAD_CONST              14 ('\n                    INSERT INTO event (search_uid, domain, actor_key, type) \n                    VALUES(:search_uid, :domain, :actor_key, :type)\n                    ')
+         
+         194         598 PRECALL                  1
+                     602 CALL                     1
+         
+         201         612 LOAD_FAST                1 (search_uid)
+         
+         202         614 LOAD_FAST                2 (actor_key)
+         
+         203         616 LOAD_FAST                5 (company)
+                     618 LOAD_METHOD              4 (get)
+                     640 LOAD_CONST               2 ('domain')
+                     642 PRECALL                  1
                      646 CALL                     1
          
-         207         656 LOAD_FAST                1 (search_uid)
+         204         656 LOAD_CONST              15 ('create')
          
-         208         658 LOAD_FAST                2 (actor_key)
+         200         658 LOAD_CONST              16 (('search_uid', 'actor_key', 'domain', 'type'))
+                     660 BUILD_CONST_KEY_MAP      4
          
-         209         660 LOAD_FAST                5 (company)
-                     662 LOAD_METHOD              3 (get)
-                     684 LOAD_CONST               2 ('domain')
-                     686 PRECALL                  1
-                     690 CALL                     1
-         
-         210         700 LOAD_CONST              14 ('create')
-         
-         206         702 LOAD_CONST              15 (('search_uid', 'actor_key', 'domain', 'type'))
-                     704 BUILD_CONST_KEY_MAP      4
-         
-         199         706 PRECALL                  2
-                     710 CALL                     2
+         193         662 PRECALL                  2
+                     666 CALL                     2
+                     676 POP_TOP
+                     678 EXTENDED_ARG             1
+                     680 JUMP_BACKWARD          272 (to 138)
+         
+         209     >>  682 LOAD_FAST                4 (con)
+                     684 LOAD_METHOD              9 (commit)
+                     706 PRECALL                  0
+                     710 CALL                     0
                      720 POP_TOP
-                     722 EXTENDED_ARG             1
-                     724 JUMP_BACKWARD          318 (to 90)
          
-         214     >>  726 LOAD_FAST                4 (con)
-                     728 LOAD_METHOD              8 (execute)
-                     750 LOAD_GLOBAL             19 (NULL + sqlalchemy)
-                     762 LOAD_ATTR               10 (text)
-                     772 LOAD_CONST              16 ('REFRESH MATERIALIZED VIEW target')
-                     774 PRECALL                  1
-                     778 CALL                     1
-                     788 PRECALL                  1
-                     792 CALL                     1
-                     802 POP_TOP
-         
-         215         804 LOAD_FAST                4 (con)
-                     806 LOAD_METHOD             11 (commit)
-                     828 PRECALL                  0
-                     832 CALL                     0
-                     842 POP_TOP
-         
-         171         844 LOAD_CONST               0 (None)
-                     846 LOAD_CONST               0 (None)
-                     848 LOAD_CONST               0 (None)
-                     850 PRECALL                  2
-                     854 CALL                     2
-                     864 POP_TOP
-                     866 LOAD_CONST               0 (None)
-                     868 RETURN_VALUE
-                 >>  870 PUSH_EXC_INFO
-                     872 WITH_EXCEPT_START
-                     874 POP_JUMP_FORWARD_IF_TRUE     4 (to 884)
-                     876 RERAISE                  2
-                 >>  878 COPY                     3
-                     880 POP_EXCEPT
-                     882 RERAISE                  1
-                 >>  884 POP_TOP
-                     886 POP_EXCEPT
-                     888 POP_TOP
-                     890 POP_TOP
-                     892 LOAD_CONST               0 (None)
-                     894 RETURN_VALUE
-         ExceptionTable:
-           84 to 842 -> 870 [1] lasti
-           870 to 876 -> 878 [3] lasti
-           884 to 884 -> 878 [3] lasti
+         165         722 LOAD_CONST               3 (None)
+                     724 LOAD_CONST               3 (None)
+                     726 LOAD_CONST               3 (None)
+                     728 PRECALL                  2
+                     732 CALL                     2
+                     742 POP_TOP
+                     744 LOAD_CONST               3 (None)
+                     746 RETURN_VALUE
+                 >>  748 PUSH_EXC_INFO
+                     750 WITH_EXCEPT_START
+                     752 POP_JUMP_FORWARD_IF_TRUE     4 (to 762)
+                     754 RERAISE                  2
+                 >>  756 COPY                     3
+                     758 POP_EXCEPT
+                     760 RERAISE                  1
+                 >>  762 POP_TOP
+                     764 POP_EXCEPT
+                     766 POP_TOP
+                     768 POP_TOP
+                     770 LOAD_CONST               3 (None)
+                     772 RETURN_VALUE
+         ExceptionTable:
+           132 to 720 -> 748 [1] lasti
+           748 to 754 -> 756 [3] lasti
+           762 to 762 -> 756 [3] lasti
          consts
-            None
+            'Takes Structured Companies (e.g. from source.find_similiar()) and inserts to Review phase'
             ('search_uid',)
             'domain'
+            None
             'Missing domain: '
             '. Skipping'
             'Skipping '
             ' as already a target'
             'Adding '
             ' as target'
             '\n                    INSERT INTO company (domain, name, description) \n                    VALUES(:domain, :name, :description)\n                    ON CONFLICT DO NOTHING\n                    '
             'name'
             'description'
             ('domain', 'name', 'description')
             '\n                    INSERT INTO event (search_uid, domain, actor_key, type) \n                    VALUES(:search_uid, :domain, :actor_key, :type)\n                    '
             'create'
             ('search_uid', 'actor_key', 'domain', 'type')
-            'REFRESH MATERIALIZED VIEW target'
-         names      ('target', 'db', 'connect', 'get', 'print', 'str', 'contains', 'any', 'execute', 'sqlalchemy', 'text', 'commit')
-         varnames   ('companies', 'search_uid', 'actor_key', 'targets', 'con', 'company')
+         names      ('unique_domains', 'to_list', 'db', 'connect', 'get', 'print', 'execute', 'sqlalchemy', 'text', 'commit')
+         varnames   ('companies', 'search_uid', 'actor_key', 'existing_search_domains', 'con', 'company')
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py'
          name       'insert_companies_as_targets'
-         firstlineno 167
+         firstlineno 160
          lnotab
-            0x0203200134010a012a012601020370013201020232021801160102ff0e
+            0x0204500134010a012a012601020314013201020232021801160102ff0e
             082801280128fd04f8100f1801160102ff0e0702010201280102fc04f914
-            0f4e0128d4
+            1028d4
+      code
+         argcount  : 0
+         nlocals   : 4
+         stacksize : 6
+         flags     : 3
+         code
+            0x9700740000000000000000000000a00100000000000000000000000000
+            00000000000000a6000000ab00000000000000000035007d0064017d017c
+            00a002000000000000000000000000000000000000000074070000000000
+            00000000006a0400000000000000007c01a6010000ab0100000000000000
+            00a6010000ab0100000000000000007d02740b000000000000000000006a
+            0600000000000000007c02a0070000000000000000000000000000000000
+            000000a6000000ab0000000000000000007c02a008000000000000000000
+            0000000000000000000000a6000000ab000000000000000000ac02a60200
+            00ab0200000000000000007d037c036302640064006400a6020000ab0200
+            000000000000000100530023003100730477027803590077010100590001
+            00010064005300
+         215           0 RESUME                   0
+         
+         216           2 LOAD_GLOBAL              0 (db)
+                      14 LOAD_METHOD              1 (connect)
+                      36 PRECALL                  0
+                      40 CALL                     0
+                      50 BEFORE_WITH
+                      52 STORE_FAST               0 (conn)
+         
+         217          54 LOAD_CONST               1 ("\n        WITH ranked_actors AS (\n            SELECT \n                a.name,\n                s.uid AS search_uid,\n                COUNT(e.id) AS total_validate_count,\n                ROW_NUMBER() OVER (\n                    PARTITION BY s.uid\n                    ORDER BY COUNT(e.id) DESC\n                ) as rn\n            FROM \n                event e\n            INNER JOIN \n                actor a ON a.key = e.actor_key\n            INNER JOIN \n                search s ON s.uid = e.search_uid\n            WHERE\n                a.type = 'research' AND \n                e.type = 'validate' \n            GROUP BY \n                a.name, s.uid\n        )\n        SELECT \n            name, \n            search_uid, \n            total_validate_count\n        FROM \n            ranked_actors\n        WHERE \n            rn = 1;\n        ")
+                      56 STORE_FAST               1 (statement)
+         
+         249          58 LOAD_FAST                0 (conn)
+                      60 LOAD_METHOD              2 (execute)
+                      82 LOAD_GLOBAL              7 (NULL + sqlalchemy)
+                      94 LOAD_ATTR                4 (text)
+                     104 LOAD_FAST                1 (statement)
+                     106 PRECALL                  1
+                     110 CALL                     1
+                     120 PRECALL                  1
+                     124 CALL                     1
+                     134 STORE_FAST               2 (result)
+         
+         250         136 LOAD_GLOBAL             11 (NULL + pd)
+                     148 LOAD_ATTR                6 (DataFrame)
+                     158 LOAD_FAST                2 (result)
+                     160 LOAD_METHOD              7 (fetchall)
+                     182 PRECALL                  0
+                     186 CALL                     0
+                     196 LOAD_FAST                2 (result)
+                     198 LOAD_METHOD              8 (keys)
+                     220 PRECALL                  0
+                     224 CALL                     0
+                     234 KW_NAMES                 2
+                     236 PRECALL                  2
+                     240 CALL                     2
+                     250 STORE_FAST               3 (df)
+         
+         251         252 LOAD_FAST                3 (df)
+         
+         216         254 SWAP                     2
+                     256 LOAD_CONST               0 (None)
+                     258 LOAD_CONST               0 (None)
+                     260 LOAD_CONST               0 (None)
+                     262 PRECALL                  2
+                     266 CALL                     2
+                     276 POP_TOP
+                     278 RETURN_VALUE
+                 >>  280 PUSH_EXC_INFO
+                     282 WITH_EXCEPT_START
+                     284 POP_JUMP_FORWARD_IF_TRUE     4 (to 294)
+                     286 RERAISE                  2
+                 >>  288 COPY                     3
+                     290 POP_EXCEPT
+                     292 RERAISE                  1
+                 >>  294 POP_TOP
+                     296 POP_EXCEPT
+                     298 POP_TOP
+                     300 POP_TOP
+                     302 LOAD_CONST               0 (None)
+                     304 RETURN_VALUE
+         ExceptionTable:
+           52 to 252 -> 280 [1] lasti
+           280 to 286 -> 288 [3] lasti
+           294 to 294 -> 288 [3] lasti
+         consts
+            None
+            "\n        WITH ranked_actors AS (\n            SELECT \n                a.name,\n                s.uid AS search_uid,\n                COUNT(e.id) AS total_validate_count,\n                ROW_NUMBER() OVER (\n                    PARTITION BY s.uid\n                    ORDER BY COUNT(e.id) DESC\n                ) as rn\n            FROM \n                event e\n            INNER JOIN \n                actor a ON a.key = e.actor_key\n            INNER JOIN \n                search s ON s.uid = e.search_uid\n            WHERE\n                a.type = 'research' AND \n                e.type = 'validate' \n            GROUP BY \n                a.name, s.uid\n        )\n        SELECT \n            name, \n            search_uid, \n            total_validate_count\n        FROM \n            ranked_actors\n        WHERE \n            rn = 1;\n        "
+            ('columns',)
+         names      ('db', 'connect', 'execute', 'sqlalchemy', 'text', 'pd', 'DataFrame', 'fetchall', 'keys')
+         varnames   ('conn', 'statement', 'result', 'df')
+         freevars   ()
+         cellvars   ()
+         filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py'
+         name       'top_actor_per_search'
+         firstlineno 215
+         lnotab 0x0201340104204e01740102dd
+      code
+         argcount  : 0
+         nlocals   : 5
+         stacksize : 7
+         flags     : 3
+         code
+            0x9700740000000000000000000000a00100000000000000000000000000
+            00000000000000a6000000ab00000000000000000035007d0064017d017c
+            00a002000000000000000000000000000000000000000074070000000000
+            00000000006a0400000000000000007c01a6010000ab0100000000000000
+            00a6010000ab0100000000000000007d02740b000000000000000000006a
+            0600000000000000007c02a0070000000000000000000000000000000000
+            000000a6000000ab0000000000000000007c02a008000000000000000000
+            0000000000000000000000a6000000ab000000000000000000ac02a60200
+            00ab0200000000000000007d037c03a00900000000000000000000000000
+            00000000000000741500000000000000000000a6000000ab000000000000
+            000000640364046405ac06a6040000ab0400000000000000007d03640784
+            007d047c03a00b00000000000000000000000000000000000000007c0464
+            08ac09a6020000ab0200000000000000007c03640a3c0000007c03a00c00
+            000000000000000000000000000000000000006700640ba2016700640ca2
+            01ac0da6020000ab0200000000000000007d037c03a00d00000000000000
+            00000000000000000000000000640ea6010000ab0100000000000000007d
+            03640064006400a6020000ab02000000000000000001006e0b2300310073
+            04770278035900770101005900010001007c035300
+         254           0 RESUME                   0
+         
+         255           2 LOAD_GLOBAL              0 (db)
+                      14 LOAD_METHOD              1 (connect)
+                      36 PRECALL                  0
+                      40 CALL                     0
+                      50 BEFORE_WITH
+                      52 STORE_FAST               0 (conn)
+         
+         256          54 LOAD_CONST               1 ("\n        SELECT \n            s.uid,\n            s.label,\n            (SELECT COUNT(*) \n            FROM event e\n            WHERE \n            e.search_uid = s.uid AND e.created >= EXTRACT(EPOCH FROM (NOW() - INTERVAL '7 days')) and type = 'validate'\n            ) AS recent_validate_count\n        FROM \n            search s;\n        ")
+                      56 STORE_FAST               1 (statement)
+         
+         268          58 LOAD_FAST                0 (conn)
+                      60 LOAD_METHOD              2 (execute)
+                      82 LOAD_GLOBAL              7 (NULL + sqlalchemy)
+                      94 LOAD_ATTR                4 (text)
+                     104 LOAD_FAST                1 (statement)
+                     106 PRECALL                  1
+                     110 CALL                     1
+                     120 PRECALL                  1
+                     124 CALL                     1
+                     134 STORE_FAST               2 (result)
+         
+         269         136 LOAD_GLOBAL             11 (NULL + pd)
+                     148 LOAD_ATTR                6 (DataFrame)
+                     158 LOAD_FAST                2 (result)
+                     160 LOAD_METHOD              7 (fetchall)
+                     182 PRECALL                  0
+                     186 CALL                     0
+                     196 LOAD_FAST                2 (result)
+                     198 LOAD_METHOD              8 (keys)
+                     220 PRECALL                  0
+                     224 CALL                     0
+                     234 KW_NAMES                 2
+                     236 PRECALL                  2
+                     240 CALL                     2
+                     250 STORE_FAST               3 (df)
+         
+         271         252 LOAD_FAST                3 (df)
+                     254 LOAD_METHOD              9 (merge)
+         
+         272         276 LOAD_GLOBAL             21 (NULL + top_actor_per_search)
+                     288 PRECALL                  0
+                     292 CALL                     0
+                     302 LOAD_CONST               3 ('uid')
+                     304 LOAD_CONST               4 ('search_uid')
+                     306 LOAD_CONST               5 ('left')
+         
+         271         308 KW_NAMES                 6
+                     310 PRECALL                  4
+                     314 CALL                     4
+                     324 STORE_FAST               3 (df)
+         
+         275         326 LOAD_CONST               7 (<code object _set_group, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 275>)
+                     328 MAKE_FUNCTION            0
+                     330 STORE_FAST               4 (_set_group)
+         
+         283         332 LOAD_FAST                3 (df)
+                     334 LOAD_METHOD             11 (apply)
+                     356 LOAD_FAST                4 (_set_group)
+                     358 LOAD_CONST               8 (1)
+                     360 KW_NAMES                 9
+                     362 PRECALL                  2
+                     366 CALL                     2
+                     376 LOAD_FAST                3 (df)
+                     378 LOAD_CONST              10 ('group')
+                     380 STORE_SUBSCR
+         
+         284         384 LOAD_FAST                3 (df)
+                     386 LOAD_METHOD             12 (sort_values)
+         
+         285         408 BUILD_LIST               0
+                     410 LOAD_CONST              11 (('group', 'recent_validate_count', 'total_validate_count', 'label'))
+                     412 LIST_EXTEND              1
+         
+         286         414 BUILD_LIST               0
+                     416 LOAD_CONST              12 ((False, False, False, True))
+                     418 LIST_EXTEND              1
+         
+         284         420 KW_NAMES                13
+                     422 PRECALL                  2
+                     426 CALL                     2
+                     436 STORE_FAST               3 (df)
+         
+         289         438 LOAD_FAST                3 (df)
+                     440 LOAD_METHOD             13 (fillna)
+                     462 LOAD_CONST              14 ('')
+                     464 PRECALL                  1
+                     468 CALL                     1
+                     478 STORE_FAST               3 (df)
+         
+         255         480 LOAD_CONST               0 (None)
+                     482 LOAD_CONST               0 (None)
+                     484 LOAD_CONST               0 (None)
+                     486 PRECALL                  2
+                     490 CALL                     2
+                     500 POP_TOP
+                     502 JUMP_FORWARD            11 (to 526)
+                 >>  504 PUSH_EXC_INFO
+                     506 WITH_EXCEPT_START
+                     508 POP_JUMP_FORWARD_IF_TRUE     4 (to 518)
+                     510 RERAISE                  2
+                 >>  512 COPY                     3
+                     514 POP_EXCEPT
+                     516 RERAISE                  1
+                 >>  518 POP_TOP
+                     520 POP_EXCEPT
+                     522 POP_TOP
+                     524 POP_TOP
+         
+         291     >>  526 LOAD_FAST                3 (df)
+                     528 RETURN_VALUE
+         ExceptionTable:
+           52 to 478 -> 504 [1] lasti
+           504 to 510 -> 512 [3] lasti
+           518 to 518 -> 512 [3] lasti
+         consts
+            None
+            "\n        SELECT \n            s.uid,\n            s.label,\n            (SELECT COUNT(*) \n            FROM event e\n            WHERE \n            e.search_uid = s.uid AND e.created >= EXTRACT(EPOCH FROM (NOW() - INTERVAL '7 days')) and type = 'validate'\n            ) AS recent_validate_count\n        FROM \n            search s;\n        "
+            ('columns',)
+            'uid'
+            'search_uid'
+            'left'
+            ('left_on', 'right_on', 'how')
+            code
+               argcount  : 1
+               nlocals   : 1
+               stacksize : 2
+               flags     : 19
+               code
+                  0x97007c0064011900000000000000000064026b04000000007202640353
+                  007c0064041900000000000000000064056b040000000072026406530064
+                  075300
+               275           0 RESUME                   0
+               
+               276           2 LOAD_FAST                0 (row)
+                             4 LOAD_CONST               1 ('recent_validate_count')
+                             6 BINARY_SUBSCR
+                            16 LOAD_CONST               2 (0)
+                            18 COMPARE_OP               4 (>)
+                            24 POP_JUMP_FORWARD_IF_FALSE     2 (to 30)
+               
+               277          26 LOAD_CONST               3 ('Trending Searches')
+                            28 RETURN_VALUE
+               
+               278     >>   30 LOAD_FAST                0 (row)
+                            32 LOAD_CONST               4 ('total_validate_count')
+                            34 BINARY_SUBSCR
+                            44 LOAD_CONST               5 (25)
+                            46 COMPARE_OP               4 (>)
+                            52 POP_JUMP_FORWARD_IF_FALSE     2 (to 58)
+               
+               279          54 LOAD_CONST               6 ('Top Searches')
+                            56 RETURN_VALUE
+               
+               281     >>   58 LOAD_CONST               7 ('All Searches')
+                            60 RETURN_VALUE
+               consts
+                  None
+                  'recent_validate_count'
+                  0
+                  'Trending Searches'
+                  'total_validate_count'
+                  25
+                  'Top Searches'
+                  'All Searches'
+               names      ()
+               varnames   ('row',)
+               freevars   ()
+               cellvars   ()
+               filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py'
+               name       '_set_group'
+               firstlineno 275
+               lnotab 0x02011801040118010402
+            1
+            ('axis',)
+            'group'
+            ('group', 'recent_validate_count', 'total_validate_count', 'label')
+            (False, False, False, True)
+            ('by', 'ascending')
+            ''
+         names      ('db', 'connect', 'execute', 'sqlalchemy', 'text', 'pd', 'DataFrame', 'fetchall', 'keys', 'merge', 'top_actor_per_search', 'apply', 'sort_values', 'fillna')
+         varnames   ('conn', 'statement', 'result', 'df', '_set_group')
+         freevars   ()
+         cellvars   ()
+         filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py'
+         name       'search'
+         firstlineno 254
+         lnotab
+            0x02013401040c4e017402180120ff1204060834011801060106fe12052a
+            de2e24
       code
          argcount  : 0
          nlocals   : 3
          stacksize : 6
          flags     : 3
          code
             0x9700740000000000000000000000a00100000000000000000000000000
             00000000000000a6000000ab00000000000000000035007d007c00a00200
             000000000000000000000000000000000000007407000000000000000000
             006a0400000000000000006401a6010000ab010000000000000000a60100
             00ab0100000000000000007d01740b000000000000000000006a06000000
             00000000007c01a0070000000000000000000000000000000000000000a6
             000000ab0000000000000000007c01a00800000000000000000000000000
             00000000000000a6000000ab000000000000000000ac02a6020000ab0200
-            000000000000007d02640064006400a6020000ab02000000000000000001
-            006e0b230031007304770278035900770101005900010001007c025300
-         221           0 RESUME                   0
+            000000000000007d027c02a0090000000000000000000000000000000000
+            00000067006403a201ac02a6010000ab0100000000000000007d027c0263
+            02640064006400a6020000ab020000000000000000010053002300310073
+            047702780359007701010059000100010064005300
+         293           0 RESUME                   0
          
-         222           2 LOAD_GLOBAL              0 (db)
+         294           2 LOAD_GLOBAL              0 (db)
                       14 LOAD_METHOD              1 (connect)
                       36 PRECALL                  0
                       40 CALL                     0
                       50 BEFORE_WITH
                       52 STORE_FAST               0 (conn)
          
-         223          54 LOAD_FAST                0 (conn)
+         295          54 LOAD_FAST                0 (conn)
                       56 LOAD_METHOD              2 (execute)
          
-         224          78 LOAD_GLOBAL              7 (NULL + sqlalchemy)
+         296          78 LOAD_GLOBAL              7 (NULL + sqlalchemy)
                       90 LOAD_ATTR                4 (text)
-                     100 LOAD_CONST               1 ("SELECT *, meta->>'group' as group FROM search")
-                     102 PRECALL                  1
+         
+         297         100 LOAD_CONST               1 ('\n                SELECT * FROM actor\n                ')
+         
+         296         102 PRECALL                  1
                      106 CALL                     1
          
-         223         116 PRECALL                  1
+         295         116 PRECALL                  1
                      120 CALL                     1
                      130 STORE_FAST               1 (result)
          
-         226         132 LOAD_GLOBAL             11 (NULL + pd)
+         302         132 LOAD_GLOBAL             11 (NULL + pd)
                      144 LOAD_ATTR                6 (DataFrame)
                      154 LOAD_FAST                1 (result)
                      156 LOAD_METHOD              7 (fetchall)
                      178 PRECALL                  0
                      182 CALL                     0
                      192 LOAD_FAST                1 (result)
                      194 LOAD_METHOD              8 (keys)
                      216 PRECALL                  0
                      220 CALL                     0
                      230 KW_NAMES                 2
                      232 PRECALL                  2
                      236 CALL                     2
                      246 STORE_FAST               2 (df)
          
-         222         248 LOAD_CONST               0 (None)
-                     250 LOAD_CONST               0 (None)
-                     252 LOAD_CONST               0 (None)
-                     254 PRECALL                  2
-                     258 CALL                     2
-                     268 POP_TOP
-                     270 JUMP_FORWARD            11 (to 294)
-                 >>  272 PUSH_EXC_INFO
-                     274 WITH_EXCEPT_START
-                     276 POP_JUMP_FORWARD_IF_TRUE     4 (to 286)
-                     278 RERAISE                  2
-                 >>  280 COPY                     3
-                     282 POP_EXCEPT
-                     284 RERAISE                  1
-                 >>  286 POP_TOP
-                     288 POP_EXCEPT
-                     290 POP_TOP
-                     292 POP_TOP
-         
-         227     >>  294 LOAD_FAST                2 (df)
-                     296 RETURN_VALUE
+         303         248 LOAD_FAST                2 (df)
+                     250 LOAD_METHOD              9 (drop)
+                     272 BUILD_LIST               0
+                     274 LOAD_CONST               3 (('id', 'created', 'updated'))
+                     276 LIST_EXTEND              1
+                     278 KW_NAMES                 2
+                     280 PRECALL                  1
+                     284 CALL                     1
+                     294 STORE_FAST               2 (df)
+         
+         304         296 LOAD_FAST                2 (df)
+         
+         294         298 SWAP                     2
+                     300 LOAD_CONST               0 (None)
+                     302 LOAD_CONST               0 (None)
+                     304 LOAD_CONST               0 (None)
+                     306 PRECALL                  2
+                     310 CALL                     2
+                     320 POP_TOP
+                     322 RETURN_VALUE
+                 >>  324 PUSH_EXC_INFO
+                     326 WITH_EXCEPT_START
+                     328 POP_JUMP_FORWARD_IF_TRUE     4 (to 338)
+                     330 RERAISE                  2
+                 >>  332 COPY                     3
+                     334 POP_EXCEPT
+                     336 RERAISE                  1
+                 >>  338 POP_TOP
+                     340 POP_EXCEPT
+                     342 POP_TOP
+                     344 POP_TOP
+                     346 LOAD_CONST               0 (None)
+                     348 RETURN_VALUE
          ExceptionTable:
-           52 to 246 -> 272 [1] lasti
-           272 to 278 -> 280 [3] lasti
-           286 to 286 -> 280 [3] lasti
+           52 to 296 -> 324 [1] lasti
+           324 to 330 -> 332 [3] lasti
+           338 to 338 -> 332 [3] lasti
          consts
             None
-            "SELECT *, meta->>'group' as group FROM search"
+            '\n                SELECT * FROM actor\n                '
             ('columns',)
-         names      ('db', 'connect', 'execute', 'sqlalchemy', 'text', 'pd', 'DataFrame', 'fetchall', 'keys')
+            ('id', 'created', 'updated')
+         names      ('db', 'connect', 'execute', 'sqlalchemy', 'text', 'pd', 'DataFrame', 'fetchall', 'keys', 'drop')
          varnames   ('conn', 'result', 'df')
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py'
-         name       'search'
-         firstlineno 221
-         lnotab 0x02013401180126ff100374fc2e05
-      'last_event_type'
+         name       'actor'
+         firstlineno 293
+         lnotab 0x020134011801160102ff0eff10077401300102f6
       code
          argcount  : 2
          nlocals   : 8
          stacksize : 7
          flags     : 3
          code
-            0x9700740000000000000000000000a00100000000000000000000000000
-            00000000000000a6000000ab00000000000000000035007d027c01812e64
-            017d037c02a0020000000000000000000000000000000000000000740700
-            0000000000000000006a0400000000000000007c03a6010000ab01000000
-            00000000007c007c0164029c02a6020000ab0200000000000000007d046e
-            2c64037d037c02a002000000000000000000000000000000000000000074
-            07000000000000000000006a0400000000000000007c03a6010000ab0100
-            0000000000000064047c006901a6020000ab0200000000000000007d0474
-            0b000000000000000000006a0600000000000000007c04a0070000000000
-            000000000000000000000000000000a6000000ab0000000000000000007c
-            04a0080000000000000000000000000000000000000000a6000000ab0000
-            00000000000000ac05a6020000ab0200000000000000007d056400640064
-            00a6020000ab02000000000000000001006e0b2300310073047702780359
-            00770101005900010001007413000000000000000000007c00a6010000ab
-            0100000000000000007d067c05a00a000000000000000000000000000000
-            00000000007c0664066407ac08a6030000ab0300000000000000007d0574
-            17000000000000000000007c00a6010000ab0100000000000000007d077c
-            05a00c00000000000000000000000000000000000000007c076a0d000000
-            0000000000a00e0000000000000000000000000000000000000000640964
-            06a6020000ab0200000000000000007c076a0d0000000000000000a00e00
-            00000000000000000000000000000000000000640aa6010000ab01000000
-            0000000000640b6b0200000000ac0ca6020000ab0200000000000000007d
-            057c055300
-         230           0 RESUME                   0
+            0x970064017d02740000000000000000000000a001000000000000000000
+            0000000000000000000000a6000000ab00000000000000000035007d037c
+            03a002000000000000000000000000000000000000000074070000000000
+            00000000006a0400000000000000007c02a6010000ab0100000000000000
+            007c007c0164029c02a6020000ab0200000000000000007d04740b000000
+            000000000000006a0600000000000000007c04a007000000000000000000
+            0000000000000000000000a6000000ab0000000000000000007c04a00800
+            00000000000000000000000000000000000000a6000000ab000000000000
+            000000ac03a6020000ab0200000000000000007d05640064006400a60200
+            00ab02000000000000000001006e0b230031007304770278035900770101
+            005900010001007c057c056404190000000000000000007c016b02000000
+            00190000000000000000007d057413000000000000000000007c00a60100
+            00ab0100000000000000007d067c05a00a00000000000000000000000000
+            000000000000007c0664056406ac07a6030000ab0300000000000000007d
+            057417000000000000000000007c00a6010000ab0100000000000000007d
+            077c05a00c00000000000000000000000000000000000000007c076a0d00
+            00000000000000a00e000000000000000000000000000000000000000064
+            086405a6020000ab0200000000000000007c076a0d0000000000000000a0
+            0e00000000000000000000000000000000000000006409a6010000ab0100
+            00000000000000640a6b0200000000ac0ba6020000ab0200000000000000
+            007d057c055300
+         307           0 RESUME                   0
+         
+         308           2 LOAD_CONST               1 ("\n        SELECT \n            e.id, \n            e.search_uid, \n            e.domain, \n            e.data, \n            e.type AS last_event_type, \n            e.created AS updated,\n            a.name AS updated_by,\n            c.name as name,\n            c.uid as dealcloud_id,\n            c.description as description,\n            c.meta as meta,\n            (c.meta->>'employees') AS employees,\n            (c.meta->>'ownership') AS ownership,\n            (c.meta->>'linkedin') AS linkedin,\n            (r.data->>'rating') AS rating\n        FROM (\n            SELECT \n                search_uid, \n                domain, \n                MAX(created) AS max_created\n            FROM \n                event\n            WHERE \n                type NOT IN ('comment','rating','generate','criteria')\n                AND search_uid = :search_uid\n            GROUP BY \n                domain, search_uid\n        ) AS max_event\n        JOIN event e ON e.domain = max_event.domain AND e.created = max_event.max_created AND e.search_uid = max_event.search_uid \n        JOIN company c ON c.domain = e.domain\n        JOIN actor a ON a.key = e.actor_key\n        LEFT JOIN (\n            SELECT \n                search_uid,\n                domain, \n                MAX(created) AS max_created\n            FROM \n                event\n            WHERE \n                type = 'rating'\n            GROUP BY \n                domain, search_uid\n        ) AS max_rating ON e.domain = max_rating.domain AND e.search_uid = max_rating.search_uid\n        LEFT JOIN event r ON r.domain = max_rating.domain AND r.created = max_rating.max_created;\n    ")
+                       4 STORE_FAST               2 (statement)
+         
+         355           6 LOAD_GLOBAL              0 (db)
+                      18 LOAD_METHOD              1 (connect)
+                      40 PRECALL                  0
+                      44 CALL                     0
+                      54 BEFORE_WITH
+                      56 STORE_FAST               3 (conn)
          
-         231           2 LOAD_GLOBAL              0 (db)
-                      14 LOAD_METHOD              1 (connect)
-                      36 PRECALL                  0
-                      40 CALL                     0
-                      50 BEFORE_WITH
-                      52 STORE_FAST               2 (conn)
+         356          58 LOAD_FAST                3 (conn)
+                      60 LOAD_METHOD              2 (execute)
          
-         232          54 LOAD_FAST                1 (last_event_type)
-                      56 POP_JUMP_FORWARD_IF_NONE    46 (to 150)
+         357          82 LOAD_GLOBAL              7 (NULL + sqlalchemy)
+                      94 LOAD_ATTR                4 (text)
+                     104 LOAD_FAST                2 (statement)
+                     106 PRECALL                  1
+                     110 CALL                     1
          
-         233          58 LOAD_CONST               1 ('SELECT * FROM target WHERE search_uid = :search_uid AND last_event_type = :last_event_type')
-                      60 STORE_FAST               3 (statement)
+         358         120 LOAD_FAST                0 (search_uid)
+                     122 LOAD_FAST                1 (last_event_type)
+                     124 LOAD_CONST               2 (('search_uid', 'last_event_type'))
+                     126 BUILD_CONST_KEY_MAP      2
+         
+         356         128 PRECALL                  2
+                     132 CALL                     2
+                     142 STORE_FAST               4 (result)
+         
+         360         144 LOAD_GLOBAL             11 (NULL + pd)
+                     156 LOAD_ATTR                6 (DataFrame)
+                     166 LOAD_FAST                4 (result)
+                     168 LOAD_METHOD              7 (fetchall)
+                     190 PRECALL                  0
+                     194 CALL                     0
+                     204 LOAD_FAST                4 (result)
+                     206 LOAD_METHOD              8 (keys)
+                     228 PRECALL                  0
+                     232 CALL                     0
+                     242 KW_NAMES                 3
+                     244 PRECALL                  2
+                     248 CALL                     2
+                     258 STORE_FAST               5 (targets)
          
-         234          62 LOAD_FAST                2 (conn)
-                      64 LOAD_METHOD              2 (execute)
-         
-         235          86 LOAD_GLOBAL              7 (NULL + sqlalchemy)
-                      98 LOAD_ATTR                4 (text)
-                     108 LOAD_FAST                3 (statement)
-                     110 PRECALL                  1
-                     114 CALL                     1
-         
-         236         124 LOAD_FAST                0 (search_uid)
-                     126 LOAD_FAST                1 (last_event_type)
-                     128 LOAD_CONST               2 (('search_uid', 'last_event_type'))
-                     130 BUILD_CONST_KEY_MAP      2
-         
-         234         132 PRECALL                  2
-                     136 CALL                     2
-                     146 STORE_FAST               4 (result)
-                     148 JUMP_FORWARD            44 (to 238)
-         
-         240     >>  150 LOAD_CONST               3 ('SELECT * FROM target WHERE search_uid = :search_uid')
-                     152 STORE_FAST               3 (statement)
-         
-         241         154 LOAD_FAST                2 (conn)
-                     156 LOAD_METHOD              2 (execute)
-         
-         242         178 LOAD_GLOBAL              7 (NULL + sqlalchemy)
-                     190 LOAD_ATTR                4 (text)
-                     200 LOAD_FAST                3 (statement)
-                     202 PRECALL                  1
-                     206 CALL                     1
-         
-         243         216 LOAD_CONST               4 ('search_uid')
-                     218 LOAD_FAST                0 (search_uid)
-                     220 BUILD_MAP                1
-         
-         241         222 PRECALL                  2
-                     226 CALL                     2
-                     236 STORE_FAST               4 (result)
-         
-         246     >>  238 LOAD_GLOBAL             11 (NULL + pd)
-                     250 LOAD_ATTR                6 (DataFrame)
-                     260 LOAD_FAST                4 (result)
-                     262 LOAD_METHOD              7 (fetchall)
-                     284 PRECALL                  0
-                     288 CALL                     0
-                     298 LOAD_FAST                4 (result)
-                     300 LOAD_METHOD              8 (keys)
-                     322 PRECALL                  0
-                     326 CALL                     0
-                     336 KW_NAMES                 5
-                     338 PRECALL                  2
-                     342 CALL                     2
-                     352 STORE_FAST               5 (targets)
+         355         260 LOAD_CONST               0 (None)
+                     262 LOAD_CONST               0 (None)
+                     264 LOAD_CONST               0 (None)
+                     266 PRECALL                  2
+                     270 CALL                     2
+                     280 POP_TOP
+                     282 JUMP_FORWARD            11 (to 306)
+                 >>  284 PUSH_EXC_INFO
+                     286 WITH_EXCEPT_START
+                     288 POP_JUMP_FORWARD_IF_TRUE     4 (to 298)
+                     290 RERAISE                  2
+                 >>  292 COPY                     3
+                     294 POP_EXCEPT
+                     296 RERAISE                  1
+                 >>  298 POP_TOP
+                     300 POP_EXCEPT
+                     302 POP_TOP
+                     304 POP_TOP
          
-         231         354 LOAD_CONST               0 (None)
-                     356 LOAD_CONST               0 (None)
-                     358 LOAD_CONST               0 (None)
-                     360 PRECALL                  2
-                     364 CALL                     2
-                     374 POP_TOP
-                     376 JUMP_FORWARD            11 (to 400)
-                 >>  378 PUSH_EXC_INFO
-                     380 WITH_EXCEPT_START
-                     382 POP_JUMP_FORWARD_IF_TRUE     4 (to 392)
-                     384 RERAISE                  2
-                 >>  386 COPY                     3
-                     388 POP_EXCEPT
-                     390 RERAISE                  1
-                 >>  392 POP_TOP
-                     394 POP_EXCEPT
-                     396 POP_TOP
-                     398 POP_TOP
+         362     >>  306 LOAD_FAST                5 (targets)
+                     308 LOAD_FAST                5 (targets)
+                     310 LOAD_CONST               4 ('last_event_type')
+                     312 BINARY_SUBSCR
+                     322 LOAD_FAST                1 (last_event_type)
+                     324 COMPARE_OP               2 (==)
+                     330 BINARY_SUBSCR
+                     340 STORE_FAST               5 (targets)
+         
+         363         342 LOAD_GLOBAL             19 (NULL + comment_by_domain)
+                     354 LOAD_FAST                0 (search_uid)
+                     356 PRECALL                  1
+                     360 CALL                     1
+                     370 STORE_FAST               6 (comments)
+         
+         364         372 LOAD_FAST                5 (targets)
+                     374 LOAD_METHOD             10 (merge)
+                     396 LOAD_FAST                6 (comments)
+                     398 LOAD_CONST               5 ('domain')
+                     400 LOAD_CONST               6 ('left')
+                     402 KW_NAMES                 7
+                     404 PRECALL                  3
+                     408 CALL                     3
+                     418 STORE_FAST               5 (targets)
+         
+         367         420 LOAD_GLOBAL             23 (NULL + find_search_by_uid)
+                     432 LOAD_FAST                0 (search_uid)
+                     434 PRECALL                  1
+                     438 CALL                     1
+                     448 STORE_FAST               7 (search)
+         
+         368         450 LOAD_FAST                5 (targets)
+                     452 LOAD_METHOD             12 (sort_values)
+         
+         369         474 LOAD_FAST                7 (search)
+                     476 LOAD_ATTR               13 (sort)
+                     486 LOAD_METHOD             14 (get)
+                     508 LOAD_CONST               8 ('field')
+                     510 LOAD_CONST               5 ('domain')
+                     512 PRECALL                  2
+                     516 CALL                     2
+         
+         370         526 LOAD_FAST                7 (search)
+                     528 LOAD_ATTR               13 (sort)
+                     538 LOAD_METHOD             14 (get)
+                     560 LOAD_CONST               9 ('order')
+                     562 PRECALL                  1
+                     566 CALL                     1
+                     576 LOAD_CONST              10 ('asc')
+                     578 COMPARE_OP               2 (==)
+         
+         368         584 KW_NAMES                11
+                     586 PRECALL                  2
+                     590 CALL                     2
+                     600 STORE_FAST               5 (targets)
          
-         248     >>  400 LOAD_GLOBAL             19 (NULL + comment_by_domain)
-                     412 LOAD_FAST                0 (search_uid)
-                     414 PRECALL                  1
-                     418 CALL                     1
-                     428 STORE_FAST               6 (comments)
-         
-         249         430 LOAD_FAST                5 (targets)
-                     432 LOAD_METHOD             10 (merge)
-                     454 LOAD_FAST                6 (comments)
-                     456 LOAD_CONST               6 ('domain')
-                     458 LOAD_CONST               7 ('left')
-                     460 KW_NAMES                 8
-                     462 PRECALL                  3
-                     466 CALL                     3
-                     476 STORE_FAST               5 (targets)
-         
-         252         478 LOAD_GLOBAL             23 (NULL + find_search_by_uid)
-                     490 LOAD_FAST                0 (search_uid)
-                     492 PRECALL                  1
-                     496 CALL                     1
-                     506 STORE_FAST               7 (search)
-         
-         253         508 LOAD_FAST                5 (targets)
-                     510 LOAD_METHOD             12 (sort_values)
-         
-         254         532 LOAD_FAST                7 (search)
-                     534 LOAD_ATTR               13 (sort)
-                     544 LOAD_METHOD             14 (get)
-                     566 LOAD_CONST               9 ('field')
-                     568 LOAD_CONST               6 ('domain')
-                     570 PRECALL                  2
-                     574 CALL                     2
-         
-         255         584 LOAD_FAST                7 (search)
-                     586 LOAD_ATTR               13 (sort)
-                     596 LOAD_METHOD             14 (get)
-                     618 LOAD_CONST              10 ('order')
-                     620 PRECALL                  1
-                     624 CALL                     1
-                     634 LOAD_CONST              11 ('asc')
-                     636 COMPARE_OP               2 (==)
-         
-         253         642 KW_NAMES                12
-                     644 PRECALL                  2
-                     648 CALL                     2
-                     658 STORE_FAST               5 (targets)
-         
-         258         660 LOAD_FAST                5 (targets)
-                     662 RETURN_VALUE
-         ExceptionTable:
-           52 to 352 -> 378 [1] lasti
-           378 to 384 -> 386 [3] lasti
-           392 to 392 -> 386 [3] lasti
+         373         602 LOAD_FAST                5 (targets)
+                     604 RETURN_VALUE
+         ExceptionTable:
+           56 to 258 -> 284 [1] lasti
+           284 to 290 -> 292 [3] lasti
+           298 to 298 -> 292 [3] lasti
          consts
             None
-            'SELECT * FROM target WHERE search_uid = :search_uid AND last_event_type = :last_event_type'
+            "\n        SELECT \n            e.id, \n            e.search_uid, \n            e.domain, \n            e.data, \n            e.type AS last_event_type, \n            e.created AS updated,\n            a.name AS updated_by,\n            c.name as name,\n            c.uid as dealcloud_id,\n            c.description as description,\n            c.meta as meta,\n            (c.meta->>'employees') AS employees,\n            (c.meta->>'ownership') AS ownership,\n            (c.meta->>'linkedin') AS linkedin,\n            (r.data->>'rating') AS rating\n        FROM (\n            SELECT \n                search_uid, \n                domain, \n                MAX(created) AS max_created\n            FROM \n                event\n            WHERE \n                type NOT IN ('comment','rating','generate','criteria')\n                AND search_uid = :search_uid\n            GROUP BY \n                domain, search_uid\n        ) AS max_event\n        JOIN event e ON e.domain = max_event.domain AND e.created = max_event.max_created AND e.search_uid = max_event.search_uid \n        JOIN company c ON c.domain = e.domain\n        JOIN actor a ON a.key = e.actor_key\n        LEFT JOIN (\n            SELECT \n                search_uid,\n                domain, \n                MAX(created) AS max_created\n            FROM \n                event\n            WHERE \n                type = 'rating'\n            GROUP BY \n                domain, search_uid\n        ) AS max_rating ON e.domain = max_rating.domain AND e.search_uid = max_rating.search_uid\n        LEFT JOIN event r ON r.domain = max_rating.domain AND r.created = max_rating.max_created;\n    "
             ('search_uid', 'last_event_type')
-            'SELECT * FROM target WHERE search_uid = :search_uid'
-            'search_uid'
             ('columns',)
+            'last_event_type'
             'domain'
             'left'
             ('on', 'how')
             'field'
             'order'
             'asc'
             ('by', 'ascending')
          names      ('db', 'connect', 'execute', 'sqlalchemy', 'text', 'pd', 'DataFrame', 'fetchall', 'keys', 'comment_by_domain', 'merge', 'find_search_by_uid', 'sort_values', 'sort', 'get')
-         varnames   ('search_uid', 'last_event_type', 'conn', 'statement', 'result', 'targets', 'comments', 'search')
+         varnames   ('search_uid', 'last_event_type', 'statement', 'conn', 'result', 'targets', 'comments', 'search')
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py'
-         name       'target'
-         firstlineno 230
+         name       'search_target_by_last_event_type'
+         firstlineno 307
          lnotab
-            0x02013401040104011801260108fe120604011801260106fe100574f12e
-            111e0130031e01180134013afe1205
+            0x0201042f34011801260108fe100474fb2e0724011e0130031e01180134
+            013afe1205
+      code
+         argcount  : 1
+         nlocals   : 5
+         stacksize : 6
+         flags     : 3
+         code
+            0x970064017d01740000000000000000000000a001000000000000000000
+            0000000000000000000000a6000000ab00000000000000000035007d027c
+            02a002000000000000000000000000000000000000000074070000000000
+            00000000006a0400000000000000007c01a6010000ab0100000000000000
+            0064027c006901a6020000ab0200000000000000007d03740b0000000000
+            00000000006a0600000000000000007c03a0070000000000000000000000
+            000000000000000000a6000000ab0000000000000000007c03a008000000
+            0000000000000000000000000000000000a6000000ab0000000000000000
+            00ac03a6020000ab0200000000000000007d04640464046404a6020000ab
+            02000000000000000001006e0b2300310073047702780359007701010059
+            00010001007c045300
+         376           0 RESUME                   0
+         
+         379           2 LOAD_CONST               1 ("\n        SELECT \n            e.id, \n            e.search_uid, \n            e.domain, \n            e.type AS last_event_type, \n            to_timestamp(e.created) AS updated,\n            c.meta as meta,\n            (r.data->>'rating') AS rating\n        FROM (\n            SELECT \n                search_uid, \n                domain, \n                MAX(created) AS max_created\n            FROM \n                event\n            WHERE \n                type NOT IN ('comment','rating','generate','criteria') \n                AND search_uid = :search_uid\n            GROUP BY \n                domain, search_uid\n        ) AS max_event\n        JOIN event e ON e.domain = max_event.domain AND e.created = max_event.max_created AND e.search_uid = max_event.search_uid \n        JOIN company c ON c.domain = e.domain\n        LEFT JOIN (\n            SELECT \n                search_uid,\n                domain, \n                MAX(created) AS max_created\n            FROM \n                event\n            WHERE \n                type = 'rating'\n            GROUP BY \n                domain, search_uid\n        ) AS max_rating ON e.domain = max_rating.domain AND e.search_uid = max_rating.search_uid\n        LEFT JOIN event r ON r.domain = max_rating.domain AND r.created = max_rating.max_created;\n    ")
+                       4 STORE_FAST               1 (statement)
+         
+         417           6 LOAD_GLOBAL              0 (db)
+                      18 LOAD_METHOD              1 (connect)
+                      40 PRECALL                  0
+                      44 CALL                     0
+                      54 BEFORE_WITH
+                      56 STORE_FAST               2 (conn)
+         
+         418          58 LOAD_FAST                2 (conn)
+                      60 LOAD_METHOD              2 (execute)
+         
+         419          82 LOAD_GLOBAL              7 (NULL + sqlalchemy)
+                      94 LOAD_ATTR                4 (text)
+                     104 LOAD_FAST                1 (statement)
+                     106 PRECALL                  1
+                     110 CALL                     1
+         
+         420         120 LOAD_CONST               2 ('search_uid')
+                     122 LOAD_FAST                0 (search_uid)
+                     124 BUILD_MAP                1
+         
+         418         126 PRECALL                  2
+                     130 CALL                     2
+                     140 STORE_FAST               3 (result)
+         
+         422         142 LOAD_GLOBAL             11 (NULL + pd)
+                     154 LOAD_ATTR                6 (DataFrame)
+                     164 LOAD_FAST                3 (result)
+                     166 LOAD_METHOD              7 (fetchall)
+                     188 PRECALL                  0
+                     192 CALL                     0
+                     202 LOAD_FAST                3 (result)
+                     204 LOAD_METHOD              8 (keys)
+                     226 PRECALL                  0
+                     230 CALL                     0
+                     240 KW_NAMES                 3
+                     242 PRECALL                  2
+                     246 CALL                     2
+                     256 STORE_FAST               4 (targets)
+         
+         417         258 LOAD_CONST               4 (None)
+                     260 LOAD_CONST               4 (None)
+                     262 LOAD_CONST               4 (None)
+                     264 PRECALL                  2
+                     268 CALL                     2
+                     278 POP_TOP
+                     280 JUMP_FORWARD            11 (to 304)
+                 >>  282 PUSH_EXC_INFO
+                     284 WITH_EXCEPT_START
+                     286 POP_JUMP_FORWARD_IF_TRUE     4 (to 296)
+                     288 RERAISE                  2
+                 >>  290 COPY                     3
+                     292 POP_EXCEPT
+                     294 RERAISE                  1
+                 >>  296 POP_TOP
+                     298 POP_EXCEPT
+                     300 POP_TOP
+                     302 POP_TOP
+         
+         431     >>  304 LOAD_FAST                4 (targets)
+                     306 RETURN_VALUE
+         ExceptionTable:
+           56 to 256 -> 282 [1] lasti
+           282 to 288 -> 290 [3] lasti
+           296 to 296 -> 290 [3] lasti
+         consts
+            'Returns all the targets not in rejected or created'
+            "\n        SELECT \n            e.id, \n            e.search_uid, \n            e.domain, \n            e.type AS last_event_type, \n            to_timestamp(e.created) AS updated,\n            c.meta as meta,\n            (r.data->>'rating') AS rating\n        FROM (\n            SELECT \n                search_uid, \n                domain, \n                MAX(created) AS max_created\n            FROM \n                event\n            WHERE \n                type NOT IN ('comment','rating','generate','criteria') \n                AND search_uid = :search_uid\n            GROUP BY \n                domain, search_uid\n        ) AS max_event\n        JOIN event e ON e.domain = max_event.domain AND e.created = max_event.max_created AND e.search_uid = max_event.search_uid \n        JOIN company c ON c.domain = e.domain\n        LEFT JOIN (\n            SELECT \n                search_uid,\n                domain, \n                MAX(created) AS max_created\n            FROM \n                event\n            WHERE \n                type = 'rating'\n            GROUP BY \n                domain, search_uid\n        ) AS max_rating ON e.domain = max_rating.domain AND e.search_uid = max_rating.search_uid\n        LEFT JOIN event r ON r.domain = max_rating.domain AND r.created = max_rating.max_created;\n    "
+            'search_uid'
+            ('columns',)
+            None
+         names      ('db', 'connect', 'execute', 'sqlalchemy', 'text', 'pd', 'DataFrame', 'fetchall', 'keys')
+         varnames   ('search_uid', 'statement', 'conn', 'result', 'targets')
+         freevars   ()
+         cellvars   ()
+         filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py'
+         name       'search_target_export'
+         firstlineno 376
+         lnotab 0x0203042634011801260106fe100474fb2e0e
       code
          argcount  : 1
          nlocals   : 5
          stacksize : 6
          flags     : 3
          code
             0x9700740000000000000000000000a00100000000000000000000000000
@@ -1668,59 +2068,59 @@
             0064027c006901a6020000ab0200000000000000007d03740b0000000000
             00000000006a0600000000000000007c03a0070000000000000000000000
             000000000000000000a6000000ab0000000000000000007c03a008000000
             0000000000000000000000000000000000a6000000ab0000000000000000
             00ac03a6020000ab0200000000000000007d04640064006400a6020000ab
             02000000000000000001006e0b2300310073047702780359007701010059
             00010001007c045300
-         261           0 RESUME                   0
+         465           0 RESUME                   0
          
-         262           2 LOAD_GLOBAL              0 (db)
+         466           2 LOAD_GLOBAL              0 (db)
                       14 LOAD_METHOD              1 (connect)
                       36 PRECALL                  0
                       40 CALL                     0
                       50 BEFORE_WITH
                       52 STORE_FAST               1 (conn)
          
-         263          54 LOAD_CONST               1 ('\n                SELECT last_event_type, count(*)\n                FROM target\n                WHERE search_uid = :search_uid\n                GROUP BY last_event_type\n            ')
+         467          54 LOAD_CONST               1 ("\n            SELECT \n                e.type AS last_event_type,\n                COUNT(e.type)\n            FROM (\n                SELECT \n                    search_uid, \n                    domain, \n                    MAX(created) AS max_created\n                FROM \n                    event\n                WHERE \n                    type NOT IN ('comment','rating','generate','criteria')\n                    and search_uid = :search_uid\n                GROUP BY \n                    domain, search_uid\n            ) AS max_event\n            JOIN event e ON e.domain = max_event.domain AND e.created = max_event.max_created AND e.search_uid = max_event.search_uid\n            GROUP BY e.type;\n        ")
                       56 STORE_FAST               2 (statement)
          
-         269          58 LOAD_FAST                1 (conn)
+         487          58 LOAD_FAST                1 (conn)
                       60 LOAD_METHOD              2 (execute)
          
-         270          82 LOAD_GLOBAL              7 (NULL + sqlalchemy)
+         488          82 LOAD_GLOBAL              7 (NULL + sqlalchemy)
                       94 LOAD_ATTR                4 (text)
                      104 LOAD_FAST                2 (statement)
                      106 PRECALL                  1
                      110 CALL                     1
          
-         271         120 LOAD_CONST               2 ('search_uid')
+         489         120 LOAD_CONST               2 ('search_uid')
                      122 LOAD_FAST                0 (search_uid)
                      124 BUILD_MAP                1
          
-         269         126 PRECALL                  2
+         487         126 PRECALL                  2
                      130 CALL                     2
                      140 STORE_FAST               3 (result)
          
-         273         142 LOAD_GLOBAL             11 (NULL + pd)
+         491         142 LOAD_GLOBAL             11 (NULL + pd)
                      154 LOAD_ATTR                6 (DataFrame)
                      164 LOAD_FAST                3 (result)
                      166 LOAD_METHOD              7 (fetchall)
                      188 PRECALL                  0
                      192 CALL                     0
                      202 LOAD_FAST                3 (result)
                      204 LOAD_METHOD              8 (keys)
                      226 PRECALL                  0
                      230 CALL                     0
                      240 KW_NAMES                 3
                      242 PRECALL                  2
                      246 CALL                     2
                      256 STORE_FAST               4 (df)
          
-         262         258 LOAD_CONST               0 (None)
+         466         258 LOAD_CONST               0 (None)
                      260 LOAD_CONST               0 (None)
                      262 LOAD_CONST               0 (None)
                      264 PRECALL                  2
                      268 CALL                     2
                      278 POP_TOP
                      280 JUMP_FORWARD            11 (to 304)
                  >>  282 PUSH_EXC_INFO
@@ -1731,33 +2131,33 @@
                      292 POP_EXCEPT
                      294 RERAISE                  1
                  >>  296 POP_TOP
                      298 POP_EXCEPT
                      300 POP_TOP
                      302 POP_TOP
          
-         274     >>  304 LOAD_FAST                4 (df)
+         492     >>  304 LOAD_FAST                4 (df)
                      306 RETURN_VALUE
          ExceptionTable:
            52 to 256 -> 282 [1] lasti
            282 to 288 -> 290 [3] lasti
            296 to 296 -> 290 [3] lasti
          consts
             None
-            '\n                SELECT last_event_type, count(*)\n                FROM target\n                WHERE search_uid = :search_uid\n                GROUP BY last_event_type\n            '
+            "\n            SELECT \n                e.type AS last_event_type,\n                COUNT(e.type)\n            FROM (\n                SELECT \n                    search_uid, \n                    domain, \n                    MAX(created) AS max_created\n                FROM \n                    event\n                WHERE \n                    type NOT IN ('comment','rating','generate','criteria')\n                    and search_uid = :search_uid\n                GROUP BY \n                    domain, search_uid\n            ) AS max_event\n            JOIN event e ON e.domain = max_event.domain AND e.created = max_event.max_created AND e.search_uid = max_event.search_uid\n            GROUP BY e.type;\n        "
             'search_uid'
             ('columns',)
          names      ('db', 'connect', 'execute', 'sqlalchemy', 'text', 'pd', 'DataFrame', 'fetchall', 'keys')
          varnames   ('search_uid', 'conn', 'statement', 'result', 'df')
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py'
          name       'target_count'
-         firstlineno 261
-         lnotab 0x0201340104061801260106fe100474f52e0c
+         firstlineno 465
+         lnotab 0x0201340104141801260106fe100474e72e1a
       code
          argcount  : 1
          nlocals   : 5
          stacksize : 6
          flags     : 3
          code
             0x9700740000000000000000000000a00100000000000000000000000000
@@ -1767,56 +2167,56 @@
             0064027c006901a6020000ab0200000000000000007d03740b0000000000
             00000000006a0600000000000000007c03a0070000000000000000000000
             000000000000000000a6000000ab0000000000000000007c03a008000000
             0000000000000000000000000000000000a6000000ab0000000000000000
             00ac03a6020000ab0200000000000000007d04640064006400a6020000ab
             02000000000000000001006e0b2300310073047702780359007701010059
             00010001007c045300
-         277           0 RESUME                   0
+         495           0 RESUME                   0
          
-         278           2 LOAD_GLOBAL              0 (db)
+         496           2 LOAD_GLOBAL              0 (db)
                       14 LOAD_METHOD              1 (connect)
                       36 PRECALL                  0
                       40 CALL                     0
                       50 BEFORE_WITH
                       52 STORE_FAST               1 (conn)
          
-         279          54 LOAD_CONST               1 ('\n                SELECT *\n                FROM event\n                WHERE search_uid = :search_uid\n            ')
+         497          54 LOAD_CONST               1 ('\n                SELECT *\n                FROM event\n                WHERE search_uid = :search_uid\n            ')
                       56 STORE_FAST               2 (statement)
          
-         284          58 LOAD_FAST                1 (conn)
+         502          58 LOAD_FAST                1 (conn)
                       60 LOAD_METHOD              2 (execute)
                       82 LOAD_GLOBAL              7 (NULL + sqlalchemy)
                       94 LOAD_ATTR                4 (text)
                      104 LOAD_FAST                2 (statement)
                      106 PRECALL                  1
                      110 CALL                     1
                      120 LOAD_CONST               2 ('search_uid')
                      122 LOAD_FAST                0 (search_uid)
                      124 BUILD_MAP                1
                      126 PRECALL                  2
                      130 CALL                     2
                      140 STORE_FAST               3 (result)
          
-         285         142 LOAD_GLOBAL             11 (NULL + pd)
+         503         142 LOAD_GLOBAL             11 (NULL + pd)
                      154 LOAD_ATTR                6 (DataFrame)
                      164 LOAD_FAST                3 (result)
                      166 LOAD_METHOD              7 (fetchall)
                      188 PRECALL                  0
                      192 CALL                     0
                      202 LOAD_FAST                3 (result)
                      204 LOAD_METHOD              8 (keys)
                      226 PRECALL                  0
                      230 CALL                     0
                      240 KW_NAMES                 3
                      242 PRECALL                  2
                      246 CALL                     2
                      256 STORE_FAST               4 (df)
          
-         278         258 LOAD_CONST               0 (None)
+         496         258 LOAD_CONST               0 (None)
                      260 LOAD_CONST               0 (None)
                      262 LOAD_CONST               0 (None)
                      264 PRECALL                  2
                      268 CALL                     2
                      278 POP_TOP
                      280 JUMP_FORWARD            11 (to 304)
                  >>  282 PUSH_EXC_INFO
@@ -1827,15 +2227,15 @@
                      292 POP_EXCEPT
                      294 RERAISE                  1
                  >>  296 POP_TOP
                      298 POP_EXCEPT
                      300 POP_TOP
                      302 POP_TOP
          
-         286     >>  304 LOAD_FAST                4 (df)
+         504     >>  304 LOAD_FAST                4 (df)
                      306 RETURN_VALUE
          ExceptionTable:
            52 to 256 -> 282 [1] lasti
            282 to 288 -> 290 [3] lasti
            296 to 296 -> 290 [3] lasti
          consts
             None
@@ -1844,15 +2244,111 @@
             ('columns',)
          names      ('db', 'connect', 'execute', 'sqlalchemy', 'text', 'pd', 'DataFrame', 'fetchall', 'keys')
          varnames   ('search_uid', 'conn', 'statement', 'result', 'df')
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py'
          name       'event'
-         firstlineno 277
+         firstlineno 495
+         lnotab 0x020134010405540174f92e08
+      code
+         argcount  : 1
+         nlocals   : 5
+         stacksize : 6
+         flags     : 3
+         code
+            0x9700740000000000000000000000a00100000000000000000000000000
+            00000000000000a6000000ab00000000000000000035007d0164017d027c
+            01a002000000000000000000000000000000000000000074070000000000
+            00000000006a0400000000000000007c02a6010000ab0100000000000000
+            0064027c006901a6020000ab0200000000000000007d03740b0000000000
+            00000000006a0600000000000000007c03a0070000000000000000000000
+            000000000000000000a6000000ab0000000000000000007c03a008000000
+            0000000000000000000000000000000000a6000000ab0000000000000000
+            00ac03a6020000ab0200000000000000007d04640064006400a6020000ab
+            02000000000000000001006e0b2300310073047702780359007701010059
+            00010001007c045300
+         507           0 RESUME                   0
+         
+         508           2 LOAD_GLOBAL              0 (db)
+                      14 LOAD_METHOD              1 (connect)
+                      36 PRECALL                  0
+                      40 CALL                     0
+                      50 BEFORE_WITH
+                      52 STORE_FAST               1 (conn)
+         
+         509          54 LOAD_CONST               1 ('\n                SELECT distinct(domain)\n                FROM event\n                WHERE search_uid = :search_uid\n            ')
+                      56 STORE_FAST               2 (statement)
+         
+         514          58 LOAD_FAST                1 (conn)
+                      60 LOAD_METHOD              2 (execute)
+                      82 LOAD_GLOBAL              7 (NULL + sqlalchemy)
+                      94 LOAD_ATTR                4 (text)
+                     104 LOAD_FAST                2 (statement)
+                     106 PRECALL                  1
+                     110 CALL                     1
+                     120 LOAD_CONST               2 ('search_uid')
+                     122 LOAD_FAST                0 (search_uid)
+                     124 BUILD_MAP                1
+                     126 PRECALL                  2
+                     130 CALL                     2
+                     140 STORE_FAST               3 (result)
+         
+         515         142 LOAD_GLOBAL             11 (NULL + pd)
+                     154 LOAD_ATTR                6 (DataFrame)
+                     164 LOAD_FAST                3 (result)
+                     166 LOAD_METHOD              7 (fetchall)
+                     188 PRECALL                  0
+                     192 CALL                     0
+                     202 LOAD_FAST                3 (result)
+                     204 LOAD_METHOD              8 (keys)
+                     226 PRECALL                  0
+                     230 CALL                     0
+                     240 KW_NAMES                 3
+                     242 PRECALL                  2
+                     246 CALL                     2
+                     256 STORE_FAST               4 (df)
+         
+         508         258 LOAD_CONST               0 (None)
+                     260 LOAD_CONST               0 (None)
+                     262 LOAD_CONST               0 (None)
+                     264 PRECALL                  2
+                     268 CALL                     2
+                     278 POP_TOP
+                     280 JUMP_FORWARD            11 (to 304)
+                 >>  282 PUSH_EXC_INFO
+                     284 WITH_EXCEPT_START
+                     286 POP_JUMP_FORWARD_IF_TRUE     4 (to 296)
+                     288 RERAISE                  2
+                 >>  290 COPY                     3
+                     292 POP_EXCEPT
+                     294 RERAISE                  1
+                 >>  296 POP_TOP
+                     298 POP_EXCEPT
+                     300 POP_TOP
+                     302 POP_TOP
+         
+         516     >>  304 LOAD_FAST                4 (df)
+                     306 RETURN_VALUE
+         ExceptionTable:
+           52 to 256 -> 282 [1] lasti
+           282 to 288 -> 290 [3] lasti
+           296 to 296 -> 290 [3] lasti
+         consts
+            None
+            '\n                SELECT distinct(domain)\n                FROM event\n                WHERE search_uid = :search_uid\n            '
+            'search_uid'
+            ('columns',)
+         names      ('db', 'connect', 'execute', 'sqlalchemy', 'text', 'pd', 'DataFrame', 'fetchall', 'keys')
+         varnames   ('search_uid', 'conn', 'statement', 'result', 'df')
+         freevars   ()
+         cellvars   ()
+         filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py'
+         name       'unique_domains'
+         firstlineno 507
          lnotab 0x020134010405540174f92e08
       code
          argcount  : 0
          nlocals   : 4
          stacksize : 6
          flags     : 3
          code
@@ -1863,53 +2359,53 @@
             00a6010000ab0100000000000000007d02740b000000000000000000006a
             0600000000000000007c02a0070000000000000000000000000000000000
             000000a6000000ab0000000000000000007c02a008000000000000000000
             0000000000000000000000a6000000ab000000000000000000ac02a60200
             00ab0200000000000000007d03640064006400a6020000ab020000000000
             00000001006e0b230031007304770278035900770101005900010001007c
             035300
-         289           0 RESUME                   0
+         519           0 RESUME                   0
          
-         290           2 LOAD_GLOBAL              0 (db)
+         520           2 LOAD_GLOBAL              0 (db)
                       14 LOAD_METHOD              1 (connect)
                       36 PRECALL                  0
                       40 CALL                     0
                       50 BEFORE_WITH
                       52 STORE_FAST               0 (conn)
          
-         291          54 LOAD_CONST               1 ('\n                SELECT *\n                FROM company\n            ')
+         521          54 LOAD_CONST               1 ('\n                SELECT *\n                FROM company\n            ')
                       56 STORE_FAST               1 (statement)
          
-         295          58 LOAD_FAST                0 (conn)
+         525          58 LOAD_FAST                0 (conn)
                       60 LOAD_METHOD              2 (execute)
                       82 LOAD_GLOBAL              7 (NULL + sqlalchemy)
                       94 LOAD_ATTR                4 (text)
                      104 LOAD_FAST                1 (statement)
                      106 PRECALL                  1
                      110 CALL                     1
                      120 PRECALL                  1
                      124 CALL                     1
                      134 STORE_FAST               2 (result)
          
-         296         136 LOAD_GLOBAL             11 (NULL + pd)
+         526         136 LOAD_GLOBAL             11 (NULL + pd)
                      148 LOAD_ATTR                6 (DataFrame)
                      158 LOAD_FAST                2 (result)
                      160 LOAD_METHOD              7 (fetchall)
                      182 PRECALL                  0
                      186 CALL                     0
                      196 LOAD_FAST                2 (result)
                      198 LOAD_METHOD              8 (keys)
                      220 PRECALL                  0
                      224 CALL                     0
                      234 KW_NAMES                 2
                      236 PRECALL                  2
                      240 CALL                     2
                      250 STORE_FAST               3 (df)
          
-         290         252 LOAD_CONST               0 (None)
+         520         252 LOAD_CONST               0 (None)
                      254 LOAD_CONST               0 (None)
                      256 LOAD_CONST               0 (None)
                      258 PRECALL                  2
                      262 CALL                     2
                      272 POP_TOP
                      274 JUMP_FORWARD            11 (to 298)
                  >>  276 PUSH_EXC_INFO
@@ -1920,15 +2416,15 @@
                      286 POP_EXCEPT
                      288 RERAISE                  1
                  >>  290 POP_TOP
                      292 POP_EXCEPT
                      294 POP_TOP
                      296 POP_TOP
          
-         297     >>  298 LOAD_FAST                3 (df)
+         527     >>  298 LOAD_FAST                3 (df)
                      300 RETURN_VALUE
          ExceptionTable:
            52 to 250 -> 276 [1] lasti
            276 to 282 -> 284 [3] lasti
            290 to 290 -> 284 [3] lasti
          consts
             None
@@ -1936,15 +2432,15 @@
             ('columns',)
          names      ('db', 'connect', 'execute', 'sqlalchemy', 'text', 'pd', 'DataFrame', 'fetchall', 'keys')
          varnames   ('conn', 'statement', 'result', 'df')
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py'
          name       'company'
-         firstlineno 289
+         firstlineno 519
          lnotab 0x0201340104044e0174fa2e07
       code
          argcount  : 1
          nlocals   : 5
          stacksize : 6
          flags     : 3
          code
@@ -1955,56 +2451,56 @@
             0064027c006901a6020000ab0200000000000000007d03740b0000000000
             00000000006a0600000000000000007c03a0070000000000000000000000
             000000000000000000a6000000ab0000000000000000007c03a008000000
             0000000000000000000000000000000000a6000000ab0000000000000000
             00ac03a6020000ab0200000000000000007d04640064006400a6020000ab
             02000000000000000001006e0b2300310073047702780359007701010059
             00010001007c045300
-         300           0 RESUME                   0
+         530           0 RESUME                   0
          
-         301           2 LOAD_GLOBAL              0 (db)
+         531           2 LOAD_GLOBAL              0 (db)
                       14 LOAD_METHOD              1 (connect)
                       36 PRECALL                  0
                       40 CALL                     0
                       50 BEFORE_WITH
                       52 STORE_FAST               1 (conn)
          
-         302          54 LOAD_CONST               1 ('\n                SELECT *\n                FROM checkpoint\n                JOIN event ON checkpoint.event_id = event.id\n                WHERE search_uid = :search_uid\n            ')
+         532          54 LOAD_CONST               1 ('\n                SELECT *\n                FROM checkpoint\n                JOIN event ON checkpoint.event_id = event.id\n                WHERE search_uid = :search_uid\n            ')
                       56 STORE_FAST               2 (statement)
          
-         308          58 LOAD_FAST                1 (conn)
+         538          58 LOAD_FAST                1 (conn)
                       60 LOAD_METHOD              2 (execute)
                       82 LOAD_GLOBAL              7 (NULL + sqlalchemy)
                       94 LOAD_ATTR                4 (text)
                      104 LOAD_FAST                2 (statement)
                      106 PRECALL                  1
                      110 CALL                     1
                      120 LOAD_CONST               2 ('search_uid')
                      122 LOAD_FAST                0 (search_uid)
                      124 BUILD_MAP                1
                      126 PRECALL                  2
                      130 CALL                     2
                      140 STORE_FAST               3 (result)
          
-         309         142 LOAD_GLOBAL             11 (NULL + pd)
+         539         142 LOAD_GLOBAL             11 (NULL + pd)
                      154 LOAD_ATTR                6 (DataFrame)
                      164 LOAD_FAST                3 (result)
                      166 LOAD_METHOD              7 (fetchall)
                      188 PRECALL                  0
                      192 CALL                     0
                      202 LOAD_FAST                3 (result)
                      204 LOAD_METHOD              8 (keys)
                      226 PRECALL                  0
                      230 CALL                     0
                      240 KW_NAMES                 3
                      242 PRECALL                  2
                      246 CALL                     2
                      256 STORE_FAST               4 (df)
          
-         301         258 LOAD_CONST               0 (None)
+         531         258 LOAD_CONST               0 (None)
                      260 LOAD_CONST               0 (None)
                      262 LOAD_CONST               0 (None)
                      264 PRECALL                  2
                      268 CALL                     2
                      278 POP_TOP
                      280 JUMP_FORWARD            11 (to 304)
                  >>  282 PUSH_EXC_INFO
@@ -2015,15 +2511,15 @@
                      292 POP_EXCEPT
                      294 RERAISE                  1
                  >>  296 POP_TOP
                      298 POP_EXCEPT
                      300 POP_TOP
                      302 POP_TOP
          
-         310     >>  304 LOAD_FAST                4 (df)
+         540     >>  304 LOAD_FAST                4 (df)
                      306 RETURN_VALUE
          ExceptionTable:
            52 to 256 -> 282 [1] lasti
            282 to 288 -> 290 [3] lasti
            296 to 296 -> 290 [3] lasti
          consts
             None
@@ -2032,15 +2528,15 @@
             ('columns',)
          names      ('db', 'connect', 'execute', 'sqlalchemy', 'text', 'pd', 'DataFrame', 'fetchall', 'keys')
          varnames   ('search_uid', 'conn', 'statement', 'result', 'df')
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py'
          name       'checkpoint'
-         firstlineno 300
+         firstlineno 530
          lnotab 0x020134010406540174f82e09
       code
          argcount  : 1
          nlocals   : 5
          stacksize : 6
          flags     : 3
          code
@@ -2055,59 +2551,59 @@
             00ac03a6020000ab0200000000000000007d04640064006400a6020000ab
             02000000000000000001006e0b2300310073047702780359007701010059
             00010001007c04a009000000000000000000000000000000000000000064
             04a6010000ab010000000000000000a00a00000000000000000000000000
             000000000000006405640684006901a6010000ab010000000000000000a0
             0b0000000000000000000000000000000000000000a6000000ab00000000
             00000000005300
-         313           0 RESUME                   0
+         543           0 RESUME                   0
          
-         314           2 LOAD_GLOBAL              0 (db)
+         544           2 LOAD_GLOBAL              0 (db)
                       14 LOAD_METHOD              1 (connect)
                       36 PRECALL                  0
                       40 CALL                     0
                       50 BEFORE_WITH
                       52 STORE_FAST               1 (conn)
          
-         315          54 LOAD_CONST               1 ("\n                SELECT *, data->>'comment' AS comment\n                FROM event e\n                WHERE \n                    search_uid = :search_uid AND\n                    type = 'comment'\n            ")
+         545          54 LOAD_CONST               1 ("\n                SELECT *, data->>'comment' AS comment\n                FROM event e\n                WHERE \n                    search_uid = :search_uid AND\n                    type = 'comment'\n            ")
                       56 STORE_FAST               2 (statement)
          
-         322          58 LOAD_FAST                1 (conn)
+         552          58 LOAD_FAST                1 (conn)
                       60 LOAD_METHOD              2 (execute)
          
-         323          82 LOAD_GLOBAL              7 (NULL + sqlalchemy)
+         553          82 LOAD_GLOBAL              7 (NULL + sqlalchemy)
                       94 LOAD_ATTR                4 (text)
                      104 LOAD_FAST                2 (statement)
                      106 PRECALL                  1
                      110 CALL                     1
          
-         324         120 LOAD_CONST               2 ('search_uid')
+         554         120 LOAD_CONST               2 ('search_uid')
                      122 LOAD_FAST                0 (search_uid)
                      124 BUILD_MAP                1
          
-         322         126 PRECALL                  2
+         552         126 PRECALL                  2
                      130 CALL                     2
                      140 STORE_FAST               3 (result)
          
-         326         142 LOAD_GLOBAL             11 (NULL + pd)
+         556         142 LOAD_GLOBAL             11 (NULL + pd)
                      154 LOAD_ATTR                6 (DataFrame)
                      164 LOAD_FAST                3 (result)
                      166 LOAD_METHOD              7 (fetchall)
                      188 PRECALL                  0
                      192 CALL                     0
                      202 LOAD_FAST                3 (result)
                      204 LOAD_METHOD              8 (keys)
                      226 PRECALL                  0
                      230 CALL                     0
                      240 KW_NAMES                 3
                      242 PRECALL                  2
                      246 CALL                     2
                      256 STORE_FAST               4 (df)
          
-         314         258 LOAD_CONST               0 (None)
+         544         258 LOAD_CONST               0 (None)
                      260 LOAD_CONST               0 (None)
                      262 LOAD_CONST               0 (None)
                      264 PRECALL                  2
                      268 CALL                     2
                      278 POP_TOP
                      280 JUMP_FORWARD            11 (to 304)
                  >>  282 PUSH_EXC_INFO
@@ -2118,22 +2614,22 @@
                      292 POP_EXCEPT
                      294 RERAISE                  1
                  >>  296 POP_TOP
                      298 POP_EXCEPT
                      300 POP_TOP
                      302 POP_TOP
          
-         328     >>  304 LOAD_FAST                4 (df)
+         558     >>  304 LOAD_FAST                4 (df)
                      306 LOAD_METHOD              9 (groupby)
                      328 LOAD_CONST               4 ('domain')
                      330 PRECALL                  1
                      334 CALL                     1
                      344 LOAD_METHOD             10 (agg)
                      366 LOAD_CONST               5 ('comment')
-                     368 LOAD_CONST               6 (<code object <lambda>, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 328>)
+                     368 LOAD_CONST               6 (<code object <lambda>, file "/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py", line 558>)
                      370 MAKE_FUNCTION            0
                      372 BUILD_MAP                1
                      374 PRECALL                  1
                      378 CALL                     1
                      388 LOAD_METHOD             11 (reset_index)
                      410 PRECALL                  0
                      414 CALL                     0
@@ -2153,41 +2649,41 @@
                argcount  : 1
                nlocals   : 1
                stacksize : 3
                flags     : 19
                code
                   0x97007401000000000000000000007c00a6010000ab0100000000000000
                   005300
-               328           0 RESUME                   0
+               558           0 RESUME                   0
                              2 LOAD_GLOBAL              1 (NULL + list)
                             14 LOAD_FAST                0 (x)
                             16 PRECALL                  1
                             20 CALL                     1
                             30 RETURN_VALUE
                consts
                   None
                names      ('list',)
                varnames   ('x',)
                freevars   ()
                cellvars   ()
                filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py'
                name       '<lambda>'
-               firstlineno 328
+               firstlineno 558
                lnotab 0x
          names      ('db', 'connect', 'execute', 'sqlalchemy', 'text', 'pd', 'DataFrame', 'fetchall', 'keys', 'groupby', 'agg', 'reset_index')
          varnames   ('search_uid', 'conn', 'statement', 'result', 'df')
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py'
          name       'comment_by_domain'
-         firstlineno 313
+         firstlineno 543
          lnotab 0x0201340104071801260106fe100474f42e0e
       code
          argcount  : 1
-         nlocals   : 5
+         nlocals   : 6
          stacksize : 7
          flags     : 3
          code
             0x9700740000000000000000000000a00100000000000000000000000000
             00000000000000a6000000ab00000000000000000035007d0164017d027c
             01a002000000000000000000000000000000000000000074070000000000
             00000000006a0400000000000000007c02a6010000ab0100000000000000
@@ -2195,42 +2691,44 @@
             020000ab02000000000000000001006e0b23003100730477027803590077
             0101005900010001007c036a05000000000000000064036b020000000072
             0264005300740d00000000000000000000740f000000000000000000007c
             03a0080000000000000000000000000000000000000000a6000000ab0000
             000000000000007c03a00900000000000000000000000000000000000000
             00a6000000ab000000000000000000a6020000ab020000000000000000a6
             010000ab0100000000000000007d04741500000000000000000000741600
-            0000000000000000007c04a6020000ab0200000000000000005300
-         334           0 RESUME                   0
+            0000000000000000007c04a6020000ab0200000000000000007d05741900
+            0000000000000000007c056a0d0000000000000000a6010000ab01000000
+            000000000001007c055300
+         564           0 RESUME                   0
          
-         335           2 LOAD_GLOBAL              0 (db)
+         565           2 LOAD_GLOBAL              0 (db)
                       14 LOAD_METHOD              1 (connect)
                       36 PRECALL                  0
                       40 CALL                     0
                       50 BEFORE_WITH
                       52 STORE_FAST               1 (conn)
          
-         336          54 LOAD_CONST               1 ('\n                SELECT *\n                FROM search\n                WHERE uid = :search_uid\n            ')
+         566          54 LOAD_CONST               1 ('\n                SELECT *\n                FROM search\n                WHERE uid = :search_uid\n            ')
                       56 STORE_FAST               2 (statement)
          
-         341          58 LOAD_FAST                1 (conn)
+         571          58 LOAD_FAST                1 (conn)
                       60 LOAD_METHOD              2 (execute)
                       82 LOAD_GLOBAL              7 (NULL + sqlalchemy)
                       94 LOAD_ATTR                4 (text)
                      104 LOAD_FAST                2 (statement)
                      106 PRECALL                  1
                      110 CALL                     1
                      120 LOAD_CONST               2 ('search_uid')
                      122 LOAD_FAST                0 (search_uid)
                      124 BUILD_MAP                1
                      126 PRECALL                  2
                      130 CALL                     2
                      140 STORE_FAST               3 (result)
          
-         335         142 LOAD_CONST               0 (None)
+         565         142 LOAD_CONST               0 (None)
                      144 LOAD_CONST               0 (None)
                      146 LOAD_CONST               0 (None)
                      148 PRECALL                  2
                      152 CALL                     2
                      162 POP_TOP
                      164 JUMP_FORWARD            11 (to 188)
                  >>  166 PUSH_EXC_INFO
@@ -2241,24 +2739,24 @@
                      176 POP_EXCEPT
                      178 RERAISE                  1
                  >>  180 POP_TOP
                      182 POP_EXCEPT
                      184 POP_TOP
                      186 POP_TOP
          
-         343     >>  188 LOAD_FAST                3 (result)
+         573     >>  188 LOAD_FAST                3 (result)
                      190 LOAD_ATTR                5 (rowcount)
                      200 LOAD_CONST               3 (0)
                      202 COMPARE_OP               2 (==)
                      208 POP_JUMP_FORWARD_IF_FALSE     2 (to 214)
          
-         344         210 LOAD_CONST               0 (None)
+         574         210 LOAD_CONST               0 (None)
                      212 RETURN_VALUE
          
-         346     >>  214 LOAD_GLOBAL             13 (NULL + dict)
+         576     >>  214 LOAD_GLOBAL             13 (NULL + dict)
                      226 LOAD_GLOBAL             15 (NULL + zip)
                      238 LOAD_FAST                3 (result)
                      240 LOAD_METHOD              8 (keys)
                      262 PRECALL                  0
                      266 CALL                     0
                      276 LOAD_FAST                3 (result)
                      278 LOAD_METHOD              9 (fetchone)
@@ -2266,37 +2764,47 @@
                      304 CALL                     0
                      314 PRECALL                  2
                      318 CALL                     2
                      328 PRECALL                  1
                      332 CALL                     1
                      342 STORE_FAST               4 (obj)
          
-         347         344 LOAD_GLOBAL             21 (NULL + from_dict)
+         577         344 LOAD_GLOBAL             21 (NULL + from_dict)
                      356 LOAD_GLOBAL             22 (Search)
                      368 LOAD_FAST                4 (obj)
                      370 PRECALL                  2
                      374 CALL                     2
-                     384 RETURN_VALUE
+                     384 STORE_FAST               5 (search)
+         
+         578         386 LOAD_GLOBAL             25 (NULL + print)
+                     398 LOAD_FAST                5 (search)
+                     400 LOAD_ATTR               13 (label)
+                     410 PRECALL                  1
+                     414 CALL                     1
+                     424 POP_TOP
+         
+         579         426 LOAD_FAST                5 (search)
+                     428 RETURN_VALUE
          ExceptionTable:
            52 to 140 -> 166 [1] lasti
            166 to 172 -> 174 [3] lasti
            180 to 180 -> 174 [3] lasti
          consts
             None
             '\n                SELECT *\n                FROM search\n                WHERE uid = :search_uid\n            '
             'search_uid'
             0
-         names      ('db', 'connect', 'execute', 'sqlalchemy', 'text', 'rowcount', 'dict', 'zip', 'keys', 'fetchone', 'from_dict', 'Search')
-         varnames   ('search_uid', 'conn', 'statement', 'result', 'obj')
+         names      ('db', 'connect', 'execute', 'sqlalchemy', 'text', 'rowcount', 'dict', 'zip', 'keys', 'fetchone', 'from_dict', 'Search', 'print', 'label')
+         varnames   ('search_uid', 'conn', 'statement', 'result', 'obj', 'search')
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py'
          name       'find_search_by_uid'
-         firstlineno 334
-         lnotab 0x02013401040554fa2e08160104028201
+         firstlineno 564
+         lnotab 0x02013401040554fa2e081601040282012a012801
       'domain'
       code
          argcount  : 1
          nlocals   : 5
          stacksize : 7
          flags     : 3
          code
@@ -2309,41 +2817,41 @@
             0101005900010001007c036a05000000000000000064036b020000000072
             0264005300740d00000000000000000000740f000000000000000000007c
             03a0080000000000000000000000000000000000000000a6000000ab0000
             000000000000007c03a00900000000000000000000000000000000000000
             00a6000000ab000000000000000000a6020000ab020000000000000000a6
             010000ab0100000000000000007d04741500000000000000000000741600
             0000000000000000007c04a6020000ab0200000000000000005300
-         350           0 RESUME                   0
+         582           0 RESUME                   0
          
-         351           2 LOAD_GLOBAL              0 (db)
+         583           2 LOAD_GLOBAL              0 (db)
                       14 LOAD_METHOD              1 (connect)
                       36 PRECALL                  0
                       40 CALL                     0
                       50 BEFORE_WITH
                       52 STORE_FAST               1 (conn)
          
-         352          54 LOAD_CONST               1 ('\n                SELECT *\n                FROM company\n                WHERE domain = :domain\n            ')
+         584          54 LOAD_CONST               1 ('\n                SELECT *\n                FROM company\n                WHERE domain = :domain\n            ')
                       56 STORE_FAST               2 (statement)
          
-         357          58 LOAD_FAST                1 (conn)
+         589          58 LOAD_FAST                1 (conn)
                       60 LOAD_METHOD              2 (execute)
                       82 LOAD_GLOBAL              7 (NULL + sqlalchemy)
                       94 LOAD_ATTR                4 (text)
                      104 LOAD_FAST                2 (statement)
                      106 PRECALL                  1
                      110 CALL                     1
                      120 LOAD_CONST               2 ('domain')
                      122 LOAD_FAST                0 (domain)
                      124 BUILD_MAP                1
                      126 PRECALL                  2
                      130 CALL                     2
                      140 STORE_FAST               3 (result)
          
-         351         142 LOAD_CONST               0 (None)
+         583         142 LOAD_CONST               0 (None)
                      144 LOAD_CONST               0 (None)
                      146 LOAD_CONST               0 (None)
                      148 PRECALL                  2
                      152 CALL                     2
                      162 POP_TOP
                      164 JUMP_FORWARD            11 (to 188)
                  >>  166 PUSH_EXC_INFO
@@ -2354,24 +2862,24 @@
                      176 POP_EXCEPT
                      178 RERAISE                  1
                  >>  180 POP_TOP
                      182 POP_EXCEPT
                      184 POP_TOP
                      186 POP_TOP
          
-         359     >>  188 LOAD_FAST                3 (result)
+         591     >>  188 LOAD_FAST                3 (result)
                      190 LOAD_ATTR                5 (rowcount)
                      200 LOAD_CONST               3 (0)
                      202 COMPARE_OP               2 (==)
                      208 POP_JUMP_FORWARD_IF_FALSE     2 (to 214)
          
-         360         210 LOAD_CONST               0 (None)
+         592         210 LOAD_CONST               0 (None)
                      212 RETURN_VALUE
          
-         362     >>  214 LOAD_GLOBAL             13 (NULL + dict)
+         594     >>  214 LOAD_GLOBAL             13 (NULL + dict)
                      226 LOAD_GLOBAL             15 (NULL + zip)
                      238 LOAD_FAST                3 (result)
                      240 LOAD_METHOD              8 (keys)
                      262 PRECALL                  0
                      266 CALL                     0
                      276 LOAD_FAST                3 (result)
                      278 LOAD_METHOD              9 (fetchone)
@@ -2379,15 +2887,15 @@
                      304 CALL                     0
                      314 PRECALL                  2
                      318 CALL                     2
                      328 PRECALL                  1
                      332 CALL                     1
                      342 STORE_FAST               4 (obj)
          
-         363         344 LOAD_GLOBAL             21 (NULL + from_dict)
+         595         344 LOAD_GLOBAL             21 (NULL + from_dict)
                      356 LOAD_GLOBAL             22 (Company)
                      368 LOAD_FAST                4 (obj)
                      370 PRECALL                  2
                      374 CALL                     2
                      384 RETURN_VALUE
          ExceptionTable:
            52 to 140 -> 166 [1] lasti
@@ -2400,15 +2908,15 @@
             0
          names      ('db', 'connect', 'execute', 'sqlalchemy', 'text', 'rowcount', 'dict', 'zip', 'keys', 'fetchone', 'from_dict', 'Company')
          varnames   ('domain', 'conn', 'statement', 'result', 'obj')
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py'
          name       'find_company_by_domain'
-         firstlineno 350
+         firstlineno 582
          lnotab 0x02013401040554fa2e08160104028201
       'event_id'
       code
          argcount  : 1
          nlocals   : 5
          stacksize : 7
          flags     : 3
@@ -2422,41 +2930,41 @@
             0101005900010001007c036a05000000000000000064036b020000000072
             0264005300740d00000000000000000000740f000000000000000000007c
             03a0080000000000000000000000000000000000000000a6000000ab0000
             000000000000007c03a00900000000000000000000000000000000000000
             00a6000000ab000000000000000000a6020000ab020000000000000000a6
             010000ab0100000000000000007d04741500000000000000000000741600
             0000000000000000007c04a6020000ab0200000000000000005300
-         366           0 RESUME                   0
+         598           0 RESUME                   0
          
-         367           2 LOAD_GLOBAL              0 (db)
+         599           2 LOAD_GLOBAL              0 (db)
                       14 LOAD_METHOD              1 (connect)
                       36 PRECALL                  0
                       40 CALL                     0
                       50 BEFORE_WITH
                       52 STORE_FAST               1 (conn)
          
-         368          54 LOAD_CONST               1 ('\n                SELECT *\n                FROM event\n                WHERE id = :event_id\n            ')
+         600          54 LOAD_CONST               1 ('\n                SELECT *\n                FROM event\n                WHERE id = :event_id\n            ')
                       56 STORE_FAST               2 (statement)
          
-         373          58 LOAD_FAST                1 (conn)
+         605          58 LOAD_FAST                1 (conn)
                       60 LOAD_METHOD              2 (execute)
                       82 LOAD_GLOBAL              7 (NULL + sqlalchemy)
                       94 LOAD_ATTR                4 (text)
                      104 LOAD_FAST                2 (statement)
                      106 PRECALL                  1
                      110 CALL                     1
                      120 LOAD_CONST               2 ('event_id')
                      122 LOAD_FAST                0 (event_id)
                      124 BUILD_MAP                1
                      126 PRECALL                  2
                      130 CALL                     2
                      140 STORE_FAST               3 (result)
          
-         367         142 LOAD_CONST               0 (None)
+         599         142 LOAD_CONST               0 (None)
                      144 LOAD_CONST               0 (None)
                      146 LOAD_CONST               0 (None)
                      148 PRECALL                  2
                      152 CALL                     2
                      162 POP_TOP
                      164 JUMP_FORWARD            11 (to 188)
                  >>  166 PUSH_EXC_INFO
@@ -2467,24 +2975,24 @@
                      176 POP_EXCEPT
                      178 RERAISE                  1
                  >>  180 POP_TOP
                      182 POP_EXCEPT
                      184 POP_TOP
                      186 POP_TOP
          
-         375     >>  188 LOAD_FAST                3 (result)
+         607     >>  188 LOAD_FAST                3 (result)
                      190 LOAD_ATTR                5 (rowcount)
                      200 LOAD_CONST               3 (0)
                      202 COMPARE_OP               2 (==)
                      208 POP_JUMP_FORWARD_IF_FALSE     2 (to 214)
          
-         376         210 LOAD_CONST               0 (None)
+         608         210 LOAD_CONST               0 (None)
                      212 RETURN_VALUE
          
-         378     >>  214 LOAD_GLOBAL             13 (NULL + dict)
+         610     >>  214 LOAD_GLOBAL             13 (NULL + dict)
                      226 LOAD_GLOBAL             15 (NULL + zip)
                      238 LOAD_FAST                3 (result)
                      240 LOAD_METHOD              8 (keys)
                      262 PRECALL                  0
                      266 CALL                     0
                      276 LOAD_FAST                3 (result)
                      278 LOAD_METHOD              9 (fetchone)
@@ -2492,15 +3000,15 @@
                      304 CALL                     0
                      314 PRECALL                  2
                      318 CALL                     2
                      328 PRECALL                  1
                      332 CALL                     1
                      342 STORE_FAST               4 (obj)
          
-         379         344 LOAD_GLOBAL             21 (NULL + from_dict)
+         611         344 LOAD_GLOBAL             21 (NULL + from_dict)
                      356 LOAD_GLOBAL             22 (Event)
                      368 LOAD_FAST                4 (obj)
                      370 PRECALL                  2
                      374 CALL                     2
                      384 RETURN_VALUE
          ExceptionTable:
            52 to 140 -> 166 [1] lasti
@@ -2513,135 +3021,120 @@
             0
          names      ('db', 'connect', 'execute', 'sqlalchemy', 'text', 'rowcount', 'dict', 'zip', 'keys', 'fetchone', 'from_dict', 'Event')
          varnames   ('event_id', 'conn', 'statement', 'result', 'obj')
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py'
          name       'find_event_by_id'
-         firstlineno 366
+         firstlineno 598
          lnotab 0x02013401040554fa2e08160104028201
       code
          argcount  : 1
          nlocals   : 3
          stacksize : 10
          flags     : 3
          code
             0x9700740000000000000000000000a00100000000000000000000000000
             00000000000000a6000000ab00000000000000000035007d0164017d027c
             01a002000000000000000000000000000000000000000074070000000000
             00000000006a0400000000000000007c02a6010000ab0100000000000000
             007c006a0500000000000000007c006a0600000000000000007c006a0700
             000000000000007411000000000000000000006a0900000000000000007c
             006a0a0000000000000000a6010000ab01000000000000000064029c04a6
-            020000ab02000000000000000001007c01a0020000000000000000000000
-            0000000000000000007407000000000000000000006a0400000000000000
-            006403a6010000ab010000000000000000a6010000ab0100000000000000
-            0001007c01a00b0000000000000000000000000000000000000000a60000
-            00ab0000000000000000000100640064006400a6020000ab020000000000
-            000000010064005300230031007304770278035900770101005900010001
-            0064005300
-         385           0 RESUME                   0
+            020000ab02000000000000000001007c01a00b0000000000000000000000
+            000000000000000000a6000000ab00000000000000000001006400640064
+            00a6020000ab020000000000000000010064005300230031007304770278
+            0359007701010059000100010064005300
+         617           0 RESUME                   0
          
-         386           2 LOAD_GLOBAL              0 (db)
+         618           2 LOAD_GLOBAL              0 (db)
                       14 LOAD_METHOD              1 (connect)
                       36 PRECALL                  0
                       40 CALL                     0
                       50 BEFORE_WITH
                       52 STORE_FAST               1 (conn)
          
-         387          54 LOAD_CONST               1 ('\n            UPDATE company\n            SET\n                name = :name,\n                description = :description,\n                meta = :meta\n            WHERE domain = :domain\n            ')
+         619          54 LOAD_CONST               1 ('\n            UPDATE company\n            SET\n                name = :name,\n                description = :description,\n                meta = :meta,\n                updated = FLOOR(EXTRACT(EPOCH FROM NOW()))\n            WHERE domain = :domain\n            ')
                       56 STORE_FAST               2 (statement)
          
-         396          58 LOAD_FAST                1 (conn)
+         629          58 LOAD_FAST                1 (conn)
                       60 LOAD_METHOD              2 (execute)
          
-         397          82 LOAD_GLOBAL              7 (NULL + sqlalchemy)
+         630          82 LOAD_GLOBAL              7 (NULL + sqlalchemy)
                       94 LOAD_ATTR                4 (text)
                      104 LOAD_FAST                2 (statement)
                      106 PRECALL                  1
                      110 CALL                     1
          
-         399         120 LOAD_FAST                0 (company)
+         632         120 LOAD_FAST                0 (company)
                      122 LOAD_ATTR                5 (name)
          
-         400         132 LOAD_FAST                0 (company)
+         633         132 LOAD_FAST                0 (company)
                      134 LOAD_ATTR                6 (description)
          
-         401         144 LOAD_FAST                0 (company)
+         634         144 LOAD_FAST                0 (company)
                      146 LOAD_ATTR                7 (domain)
          
-         402         156 LOAD_GLOBAL             17 (NULL + json)
+         635         156 LOAD_GLOBAL             17 (NULL + json)
                      168 LOAD_ATTR                9 (dumps)
                      178 LOAD_FAST                0 (company)
                      180 LOAD_ATTR               10 (meta)
                      190 PRECALL                  1
                      194 CALL                     1
          
-         398         204 LOAD_CONST               2 (('name', 'description', 'domain', 'meta'))
+         631         204 LOAD_CONST               2 (('name', 'description', 'domain', 'meta'))
                      206 BUILD_CONST_KEY_MAP      4
          
-         396         208 PRECALL                  2
+         629         208 PRECALL                  2
                      212 CALL                     2
                      222 POP_TOP
          
-         405         224 LOAD_FAST                1 (conn)
-                     226 LOAD_METHOD              2 (execute)
-                     248 LOAD_GLOBAL              7 (NULL + sqlalchemy)
-                     260 LOAD_ATTR                4 (text)
-                     270 LOAD_CONST               3 ('REFRESH MATERIALIZED VIEW target')
-                     272 PRECALL                  1
-                     276 CALL                     1
-                     286 PRECALL                  1
-                     290 CALL                     1
-                     300 POP_TOP
-         
-         406         302 LOAD_FAST                1 (conn)
-                     304 LOAD_METHOD             11 (commit)
-                     326 PRECALL                  0
-                     330 CALL                     0
-                     340 POP_TOP
-         
-         386         342 LOAD_CONST               0 (None)
-                     344 LOAD_CONST               0 (None)
-                     346 LOAD_CONST               0 (None)
-                     348 PRECALL                  2
-                     352 CALL                     2
-                     362 POP_TOP
-                     364 LOAD_CONST               0 (None)
-                     366 RETURN_VALUE
-                 >>  368 PUSH_EXC_INFO
-                     370 WITH_EXCEPT_START
-                     372 POP_JUMP_FORWARD_IF_TRUE     4 (to 382)
-                     374 RERAISE                  2
-                 >>  376 COPY                     3
-                     378 POP_EXCEPT
-                     380 RERAISE                  1
-                 >>  382 POP_TOP
-                     384 POP_EXCEPT
-                     386 POP_TOP
-                     388 POP_TOP
-                     390 LOAD_CONST               0 (None)
-                     392 RETURN_VALUE
-         ExceptionTable:
-           52 to 340 -> 368 [1] lasti
-           368 to 374 -> 376 [3] lasti
-           382 to 382 -> 376 [3] lasti
+         639         224 LOAD_FAST                1 (conn)
+                     226 LOAD_METHOD             11 (commit)
+                     248 PRECALL                  0
+                     252 CALL                     0
+                     262 POP_TOP
+         
+         618         264 LOAD_CONST               0 (None)
+                     266 LOAD_CONST               0 (None)
+                     268 LOAD_CONST               0 (None)
+                     270 PRECALL                  2
+                     274 CALL                     2
+                     284 POP_TOP
+                     286 LOAD_CONST               0 (None)
+                     288 RETURN_VALUE
+                 >>  290 PUSH_EXC_INFO
+                     292 WITH_EXCEPT_START
+                     294 POP_JUMP_FORWARD_IF_TRUE     4 (to 304)
+                     296 RERAISE                  2
+                 >>  298 COPY                     3
+                     300 POP_EXCEPT
+                     302 RERAISE                  1
+                 >>  304 POP_TOP
+                     306 POP_EXCEPT
+                     308 POP_TOP
+                     310 POP_TOP
+                     312 LOAD_CONST               0 (None)
+                     314 RETURN_VALUE
+         ExceptionTable:
+           52 to 262 -> 290 [1] lasti
+           290 to 296 -> 298 [3] lasti
+           304 to 304 -> 298 [3] lasti
          consts
             None
-            '\n            UPDATE company\n            SET\n                name = :name,\n                description = :description,\n                meta = :meta\n            WHERE domain = :domain\n            '
+            '\n            UPDATE company\n            SET\n                name = :name,\n                description = :description,\n                meta = :meta,\n                updated = FLOOR(EXTRACT(EPOCH FROM NOW()))\n            WHERE domain = :domain\n            '
             ('name', 'description', 'domain', 'meta')
-            'REFRESH MATERIALIZED VIEW target'
          names      ('db', 'connect', 'execute', 'sqlalchemy', 'text', 'name', 'description', 'domain', 'json', 'dumps', 'meta', 'commit')
          varnames   ('company', 'conn', 'statement')
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py'
          name       'update_company'
-         firstlineno 385
-         lnotab 0x020134010409180126020c010c010c0130fc04fe10094e0128ec
+         firstlineno 617
+         lnotab 0x02013401040a180126020c010c010c0130fc04fe100a28eb
       code
          argcount  : 1
          nlocals   : 2
          stacksize : 9
          flags     : 3
          code
             0x9700740000000000000000000000a00100000000000000000000000000
@@ -2653,72 +3146,72 @@
             000000000000007c006a080000000000000000a6010000ab010000000000
             000000740b000000000000000000006a0600000000000000007c006a0900
             00000000000000a6010000ab0100000000000000007c006a0a0000000000
             00000064029c04a6020000ab02000000000000000001007c01a00b000000
             0000000000000000000000000000000000a6000000ab0000000000000000
             000100640064006400a6020000ab02000000000000000001006400530023
             00310073047702780359007701010059000100010064005300
-         409           0 RESUME                   0
+         642           0 RESUME                   0
          
-         410           2 LOAD_GLOBAL              0 (db)
+         643           2 LOAD_GLOBAL              0 (db)
                       14 LOAD_METHOD              1 (connect)
                       36 PRECALL                  0
                       40 CALL                     0
                       50 BEFORE_WITH
                       52 STORE_FAST               1 (conn)
          
-         411          54 LOAD_FAST                1 (conn)
+         644          54 LOAD_FAST                1 (conn)
                       56 LOAD_METHOD              2 (execute)
          
-         412          78 LOAD_GLOBAL              7 (NULL + sqlalchemy)
+         645          78 LOAD_GLOBAL              7 (NULL + sqlalchemy)
                       90 LOAD_ATTR                4 (text)
          
-         413         100 LOAD_CONST               1 ('\n                UPDATE search\n                SET\n                    sort = :sort,\n                    inclusion = :inclusion,\n                    exclusion = :exclusion\n                WHERE uid = :uid\n                ')
+         646         100 LOAD_CONST               1 ('\n                UPDATE search\n                SET\n                    sort = :sort,\n                    inclusion = :inclusion,\n                    exclusion = :exclusion\n                WHERE uid = :uid\n                ')
          
-         412         102 PRECALL                  1
+         645         102 PRECALL                  1
                      106 CALL                     1
          
-         423         116 LOAD_GLOBAL             11 (NULL + json)
+         656         116 LOAD_GLOBAL             11 (NULL + json)
                      128 LOAD_ATTR                6 (dumps)
                      138 LOAD_FAST                0 (search)
                      140 LOAD_ATTR                7 (sort)
                      150 PRECALL                  1
                      154 CALL                     1
          
-         424         164 LOAD_GLOBAL             11 (NULL + json)
+         657         164 LOAD_GLOBAL             11 (NULL + json)
                      176 LOAD_ATTR                6 (dumps)
                      186 LOAD_FAST                0 (search)
                      188 LOAD_ATTR                8 (inclusion)
                      198 PRECALL                  1
                      202 CALL                     1
          
-         425         212 LOAD_GLOBAL             11 (NULL + json)
+         658         212 LOAD_GLOBAL             11 (NULL + json)
                      224 LOAD_ATTR                6 (dumps)
                      234 LOAD_FAST                0 (search)
                      236 LOAD_ATTR                9 (exclusion)
                      246 PRECALL                  1
                      250 CALL                     1
          
-         426         260 LOAD_FAST                0 (search)
+         659         260 LOAD_FAST                0 (search)
                      262 LOAD_ATTR               10 (uid)
          
-         422         272 LOAD_CONST               2 (('sort', 'inclusion', 'exclusion', 'uid'))
+         655         272 LOAD_CONST               2 (('sort', 'inclusion', 'exclusion', 'uid'))
                      274 BUILD_CONST_KEY_MAP      4
          
-         411         276 PRECALL                  2
+         644         276 PRECALL                  2
                      280 CALL                     2
                      290 POP_TOP
          
-         429         292 LOAD_FAST                1 (conn)
+         662         292 LOAD_FAST                1 (conn)
                      294 LOAD_METHOD             11 (commit)
                      316 PRECALL                  0
                      320 CALL                     0
                      330 POP_TOP
          
-         410         332 LOAD_CONST               0 (None)
+         643         332 LOAD_CONST               0 (None)
                      334 LOAD_CONST               0 (None)
                      336 LOAD_CONST               0 (None)
                      338 PRECALL                  2
                      342 CALL                     2
                      352 POP_TOP
                      354 LOAD_CONST               0 (None)
                      356 RETURN_VALUE
@@ -2745,22 +3238,22 @@
             ('sort', 'inclusion', 'exclusion', 'uid')
          names      ('db', 'connect', 'execute', 'sqlalchemy', 'text', 'json', 'dumps', 'sort', 'inclusion', 'exclusion', 'uid', 'commit')
          varnames   ('search', 'conn')
          freevars   ()
          cellvars   ()
          filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py'
          name       'update_search'
-         firstlineno 409
+         firstlineno 642
          lnotab 0x020134011801160102ff0e0b3001300130010cfc04f5101228ed
       (None,)
-   names      ('json', 'pandas', 'pd', 'typing', 'List', 'Any', 'dataclasses', 'asdict', 'dacite', 'from_dict', 'gandai.models', 'Event', 'Company', 'EventType', 'Actor', 'Search', 'Checkpoint', 'sqlalchemy', 'google.cloud.sql.connector', 'Connector', 'dotenv', 'load_dotenv', 'gandai.db', 'connect_with_connector', 'db', 'insert_company', 'insert_event', 'insert_actor', 'insert_search', 'insert_checkpoint', 'str', 'int', 'insert_and_advance_targets_from_domains', 'insert_companies_as_targets', 'search', 'target', 'DataFrame', 'target_count', 'event', 'company', 'checkpoint', 'comment_by_domain', 'find_search_by_uid', 'find_company_by_domain', 'find_event_by_id', 'update_company', 'update_search')
+   names      ('json', 'dataclasses', 'asdict', 'typing', 'Any', 'List', 'pandas', 'pd', 'sqlalchemy', 'dacite', 'from_dict', 'dotenv', 'load_dotenv', 'google.cloud.sql.connector', 'Connector', 'gandai', 'helpers', 'gandai.db', 'connect_with_connector', 'gandai.models', 'Actor', 'Checkpoint', 'Company', 'Event', 'EventType', 'Search', 'db', 'insert_company', 'insert_event', 'insert_actor', 'insert_search', 'insert_checkpoint', 'str', 'int', 'insert_targets_from_domains', 'insert_companies_as_targets', 'DataFrame', 'top_actor_per_search', 'search', 'actor', 'search_target_by_last_event_type', 'search_target_export', 'target_count', 'event', 'unique_domains', 'company', 'checkpoint', 'comment_by_domain', 'find_search_by_uid', 'find_company_by_domain', 'find_event_by_id', 'update_company', 'update_search')
    varnames   ()
    freevars   ()
    cellvars   ()
    filename   '/Users/parker/Development/gandai-workspace/repo/src/gandai/query.py'
    name       '<module>'
    firstlineno 1
    lnotab
-      0x00ff02010801080110010c010c01200a08020c010c0214020c0214060c
-      0e1015100f1013100d02010eff020102ff020102ff020202fe083602010e
-      ff020102ff020102ff020202fe08360609121f1a101a0c160b1a0d1a1510
-      10101010131018
+      0x00ff020108010c011002080108010c010c010c0214020c010c01200214
+      060c0e1015100f1013100d02010eff020102ff020102ff020102ff020202
+      fe083702010eff020102ff020102ff020202fe083716270627160e12451a
+      591a1e1a0c1a0c160b1a0d1a151012101010131019
```

### Comparing `gandai-1.2.0/gandai/__pycache__/services.cpython-311.pyc` & `gandai-1.3.0/gandai/__pycache__/services.cpython-311.pyc`

 * *Files identical despite different names*

### Comparing `gandai-1.2.0/gandai/auth.py` & `gandai-1.3.0/gandai/auth.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,19 +1,20 @@
-import pandas as pd
+import os
 import random
 from dataclasses import asdict, dataclass, field
 from hashlib import md5
 from time import time
-import os
+
+import pandas as pd
 from twilio.rest import Client
 
-# from gandai.models.User import user_exists # create_user
+from gandai.secrets import access_secret_version
 
+# from gandai.models.User import user_exists # create_user
 
-from gandai.secrets import access_secret_version
 
 # from gandai.datastore import Cloudstore
 # ds = Cloudstore()
 ds = {}
 twilio_client = Client(
     access_secret_version("TWILIO_APP"), access_secret_version("TWILIO_TOKEN")
 )
@@ -35,31 +36,32 @@
         self.key = f"auth/{self.phone}/{self.expires}"
         self.token = md5(self.key.encode()).hexdigest()
 
 
 def _send_code(auth: Auth) -> None:
     message = twilio_client.messages.create(
         to=auth.phone,
-        from_=os.getenv("TWILIO_NUMBER"),
-        body=f"{auth.code} is your GA Research authentication code.",
+        from_=access_secret_version("TWILIO_NUMBER"),
+        body=f"{auth.code} is your TargetSelect authentication code.",
     )
     print(f"Login Sent to {auth.phone}")
 
 
 def send_code(phone: str) -> None:
     # Event.create(actor_key=phone)
     auth_code = str(random.randint(100000, 999999))
     auth = Auth(phone=phone, code=auth_code)
     ds[auth.key] = asdict(auth)
     _send_code(auth)
 
 
 def authenticate(code: str) -> Auth:
-    keys = ds.keys("auth/")[1::]
-    df = pd.DataFrame(ds.load_async(keys))
+    code = code.strip()
+    keys = ds.keys()
+    df = pd.DataFrame([ds[k] for k in keys])
     df = df[df["expires"] > int(time())]
     df = df[df["code"] == code]
     if len(df) > 0:
         # could parse to Auth and back to dict
         return df.to_dict(orient="records")[0]
     else:
         return None
```

### Comparing `gandai-1.2.0/gandai/datastore.py` & `gandai-1.3.0/gandai/datastore.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,18 +1,19 @@
 import datetime
 import json
 import os
 from concurrent.futures import ThreadPoolExecutor
-
 from typing import Any, Dict, List
-from google.cloud import storage
-import os
+
 from dotenv import load_dotenv
+from google.cloud import storage
+
 load_dotenv()
 
+
 class Cloudstore:
     def __init__(self):
         GCP_PROJECT = os.getenv("PROJECT_ID")
         self.BUCKET_NAME = f"{GCP_PROJECT}"
         self.client = storage.Client(project=GCP_PROJECT)
         self.bucket = self.client.get_bucket(self.BUCKET_NAME)
```

### Comparing `gandai-1.2.0/gandai/db.py` & `gandai-1.3.0/gandai/db.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,22 +1,22 @@
 import os
 
-from google.cloud.sql.connector import Connector, IPTypes
 import pg8000
-
 import sqlalchemy
+from google.cloud.sql.connector import Connector, IPTypes
+
 from gandai.secrets import access_secret_version
 
-def connect_with_connector() -> sqlalchemy.engine.base.Engine:
 
-    ## Connect to Dev DB 
+def connect_with_connector() -> sqlalchemy.engine.base.Engine:
+    ## Connect to Dev DB
     if os.getenv("LOCAL_DB", False):
         print("📀 connecting to local db")
         return sqlalchemy.create_engine("postgresql://localhost:5432/postgres")
-    
+
     connector = Connector()
     instance_connection_name = access_secret_version("INSTANCE_CONNECTION_NAME")
     db_pass = access_secret_version("DB_PASS")
     print(instance_connection_name)
 
     def getconn() -> pg8000.dbapi.Connection:
         conn: pg8000.dbapi.Connection = connector.connect(
```

### Comparing `gandai-1.2.0/gandai/main.py` & `gandai-1.3.0/gandai/main.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,40 +1,40 @@
-import pandas as pd
-from dacite import from_dict
-from dataclasses import dataclass, field
 from concurrent.futures import ThreadPoolExecutor
+from dataclasses import dataclass, field
 from time import time
 
+import pandas as pd
+from dacite import from_dict
 
-from gandai.models import Event, Company, Checkpoint
 from gandai import query
+from gandai.models import Checkpoint, Company, Event
 from gandai.sources import GrataWrapper as grata
 
 
 def process_event(event_id: int) -> None:
     """
     May trigger additional targets adding to inbox, or something else
     (e.g. a notification)
     """
-    
-    e = query.find_event_by_id(event_id)
+
+    e: Event = query.find_event_by_id(event_id)
     search_uid = e.search_uid
 
     if e.type == "create":
         pass
     elif e.type == "advance":
         # enrich the company
         company = query.find_company_by_domain(e.domain)
-        
-        if len(company.meta.keys()) < 10:
+
+        if "company_uid" not in company.meta.keys():
             # adding this check to mitigate API usage
             # revisit this number
             resp = grata.enrich(company.domain)
             if resp.get("status") == 404:
-                print(f"{company} not found") # are we charged for "not found"?
+                print(f"{company} not found")  # are we charged for "not found"?
             else:
                 print(resp)
                 company.name = resp.get("name")
                 company.description = resp.get("description")
                 company.meta = {**company.meta, **resp}  # merge 3.5+
                 query.update_company(company)
         else:
@@ -58,15 +58,15 @@
     elif e.type == "criteria":
         print(f"criteria search for {search_uid}")
         search = query.find_search_by_uid(search_uid)
         grata_companies = grata.find_by_criteria(search)
         query.insert_companies_as_targets(
             companies=grata_companies, search_uid=search_uid, actor_key="grata"
         )
-        
+
     # finally, record we processed the event
     # could make these async
     query.insert_checkpoint(Checkpoint(event_id=e.id))
     print(f"processed: {e}")
 
 
 def process_events(search_uid: int) -> int:
@@ -75,16 +75,16 @@
     """
 
     events = query.event(search_uid=search_uid)
     checkpoints = query.checkpoint(search_uid=search_uid)
 
     q = list(set(events["id"].tolist()) - set(checkpoints["event_id"].tolist()))
 
-    for event_id in q:
-        print(event_id)
-        process_event(event_id)
-
-    # 
-    # with ThreadPoolExecutor(max_workers=4) as executor:
-    #     executor.map(process_event, q)
+    # for event_id in q:
+    #     print(event_id)
+    #     process_event(event_id)
+
+    # F2 instance_class defaults to 4 workers
+    with ThreadPoolExecutor(max_workers=4) as executor:
+        executor.map(process_event, q)
 
     return len(q)
```

### Comparing `gandai-1.2.0/gandai/migrations/__pycache__/dealcloud.cpython-311.pyc` & `gandai-1.3.0/gandai/migrations/__pycache__/dealcloud.cpython-311.pyc`

 * *Files identical despite different names*

### Comparing `gandai-1.2.0/gandai/migrations/db_seed.py` & `gandai-1.3.0/gandai/migrations/db_seed.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,11 @@
 from gandai import query
-from gandai.models import Company, Actor, Search, Event
 from gandai.migrations.dealcloud import migrate_engagements
+from gandai.models import Actor, Company, Event, Search
+
 
 def seed_actors():
     actors = {
         "7138248581": "Parker",
         "6508620943": "Gabe",
         "9413500954": "Skye",
         "3102835279": "Chris",
@@ -17,14 +18,15 @@
         "chatgpt": "ChatGPT",
     }
 
     for key, name in actors.items():
         actor = query.insert_actor(Actor(key=key, type="research", name=name))
         print(f"Added: {actor}")
 
+
 def seed_hello_world():
     search = query.insert_search(
         Search(
             uid=1,
             client_domain="parkerholcomb.com",
             label="Hello World",
             meta={"research": "Parker", "status": "In Progress"},
@@ -55,11 +57,11 @@
         )
     )
 
 
 def main():
     seed_actors()
     seed_hello_world()
-    
+
 
 if __name__ == "__main__":
     main()
```

### Comparing `gandai-1.2.0/gandai/migrations/dealcloud.py` & `gandai-1.3.0/gandai/migrations/dealcloud.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,13 +1,14 @@
-from gandai import query
-from gandai.models import Search
-
 import re
+
 import pandas as pd
 
+from gandai import query
+from gandai.models import Search
+
 
 def dealcloud_company_query(
     fp="/Users/parker/Development/gandai-workspace/notebooks/2023-05-13/data/Company_05132023.xlsx",
 ) -> pd.DataFrame:
     print("dealcloud_company_query")
 
     def _get_domain(url) -> str:
```

### Comparing `gandai-1.2.0/gandai/migrations/sql/schema.sql` & `gandai-1.3.0/gandai/migrations/sql/schema.sql`

 * *Files 4% similar despite different names*

```diff
@@ -56,42 +56,44 @@
 CREATE MATERIALIZED VIEW IF NOT EXISTS target AS
 SELECT 
     e.id, 
     e.search_uid, 
     e.domain, 
     e.data, 
     e.type AS last_event_type, 
-    e.created AS last_event_dt,
+    e.created AS updated,
     c.name as name,
     c.uid as dealcloud_id,
     c.description as description,
     c.meta as meta,
     (c.meta->>'employees') AS employees,
     (c.meta->>'ownership') AS ownership,
-    (c.meta->>'linkedin') AS linkedin,    
+    (c.meta->>'linkedin') AS linkedin,
     (r.data->>'rating') AS rating
 FROM (
     SELECT 
+        search_uid, 
         domain, 
         MAX(created) AS max_created
     FROM 
         event
     WHERE 
         type NOT IN ('comment','rating','generate','criteria')
     GROUP BY 
-        domain
+        domain, search_uid
 ) AS max_event
-JOIN event e ON e.domain = max_event.domain AND e.created = max_event.max_created
+JOIN event e ON e.domain = max_event.domain AND e.created = max_event.max_created AND e.search_uid = max_event.search_uid 
 JOIN company c ON c.domain = e.domain
 LEFT JOIN (
     SELECT 
+        search_uid,
         domain, 
         MAX(created) AS max_created
     FROM 
         event
     WHERE 
         type = 'rating'
     GROUP BY 
-        domain
-) AS max_rating ON e.domain = max_rating.domain
+        domain, search_uid
+) AS max_rating ON e.domain = max_rating.domain AND e.search_uid = max_rating.search_uid
 LEFT JOIN event r ON r.domain = max_rating.domain AND r.created = max_rating.max_created;
```

### Comparing `gandai-1.2.0/gandai/models.py` & `gandai-1.3.0/gandai/models.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,11 @@
-from typing import List, Optional
-from enum import Enum, auto
 from dataclasses import asdict, dataclass, field
+from enum import Enum, auto
+from typing import List, Optional
+
 
 @dataclass
 class Actor:
     # id: int = field(init=False)  # pk
     key: str  # phone number
     type: str
     name: str
@@ -31,42 +32,44 @@
     CONFLICT = auto()
     REJECT = auto()
     CRITERIA = auto()
 
 
 @dataclass
 class Event:
-    
-    search_uid: int  # fk # add index 
+    search_uid: int  # fk # add index
     domain: Optional[str]  # fk
     actor_key: str  # fk
     type: str  # build, advance, qualify, reject, conflict, rate
     data: dict = field(default_factory=dict)
     id: int = field(default=None)  # pk
     # created: int = field(init=False)
 
 
 @dataclass
 class Comment(Event):
     def __post_init__(self):
+        # self.type = EventType.COMMENT
         assert isinstance(self.data["comment"], str)
 
 
 @dataclass
 class Rating(Event):
     def __post_init__(self):
         assert isinstance(self.data["rating"], int)
 
+
 @dataclass
 class Checkpoint:
     # actor_key: str  # foreign key
     event_id: int  # foreign key
-    id: int  = field(default=None) # primary key
+    id: int = field(default=None)  # primary key
     # created: int  # timestamp
 
+
 @dataclass(order=True)
 class Target:
     domain: str  # enforce unique
     name: str
     search_id: int  # fk
     description: str
     event: List
@@ -89,23 +92,22 @@
     services: list
     updated: int
     actor_id: int  # fk
 
 
 @dataclass
 class Search:
-    
     uid: int  # foreign key, dealcloud id
-    client_domain: str  # 
+    client_domain: str  #
     label: str
     meta: dict = field(default_factory=dict)
     inclusion: dict = field(default_factory=dict)
     exclusion: dict = field(default_factory=dict)
     sort: dict = field(default_factory=dict)
-    id: int  = field(default=None) # primary key
+    id: int = field(default=None)  # primary key
     # created: int = field(init=False)
     # updated: int = field(init=False)
 
 
 @dataclass
 class Sort:
     FIELDS = ["employee_count", "rating", "state", "country", "year_founded", "name"]
```

### Comparing `gandai-1.2.0/gandai/query.py` & `gandai-1.3.0/gandai/query.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,30 +1,22 @@
 import json
-import pandas as pd
-from typing import List, Any
 from dataclasses import asdict
-from dacite import from_dict
-from gandai.models import (
-    Event,
-    Company,
-    EventType,
-    Actor,
-    Search,
-    Checkpoint,
-)
-
+from typing import Any, List
 
+import pandas as pd
 import sqlalchemy
-
-from google.cloud.sql.connector import Connector
+from dacite import from_dict
 from dotenv import load_dotenv
+from google.cloud.sql.connector import Connector
 
 load_dotenv()
 
+from gandai import helpers
 from gandai.db import connect_with_connector
+from gandai.models import Actor, Checkpoint, Company, Event, EventType, Search
 
 db = connect_with_connector()
 
 
 ### WRITES ###
 
 
@@ -35,15 +27,15 @@
                 INSERT INTO company (domain, name, description) 
                 VALUES(:domain, :name, :description)
                 ON CONFLICT DO NOTHING
             """
         )
         con.execute(statement, asdict(company))
         con.commit()
-    return company
+    return company  # todo this should return the id
 
 
 def insert_event(event: Event) -> Event:
     with db.connect() as con:
         statement = sqlalchemy.text(
             """
                 INSERT INTO event (search_uid, domain, actor_key, type, data) 
@@ -54,15 +46,15 @@
         )
         obj = asdict(event)
         obj["data"] = json.dumps(obj["data"])
         result = con.execute(statement, obj)
         # print(result.first())
         _id = result.first()
         event.id = _id[0] if _id else None
-        con.execute(sqlalchemy.text("REFRESH MATERIALIZED VIEW target"))
+        # con.execute(sqlalchemy.text("REFRESH MATERIALIZED VIEW target"))
         con.commit()
     return event
 
 
 def insert_actor(actor: Actor) -> Actor:
     with db.connect() as con:
         statement = sqlalchemy.text(
@@ -106,39 +98,40 @@
             """
         )
         con.execute(statement, asdict(checkpoint))
         con.commit()
     return checkpoint
 
 
-def insert_and_advance_targets_from_domains(
-    domains: List[str], search_uid: int, actor_key: str
+def insert_targets_from_domains(
+    domains: List[str], search_uid: int, actor_key: str, last_event_type: str
 ) -> None:
     """
     Takes in domains, inserts targets into a review stage, where they will
     try to be enriched on process event
 
     """
-    targets = target(search_uid=search_uid)
+    existing_search_domains = unique_domains(search_uid=search_uid)[
+        "domain"
+    ].to_list()  
     with db.connect() as con:
         for domain in domains:
-            # consider upstream formatter/validator
-            domain = (
-                domain.lower()
-                .strip()
-                .replace("www.", "")
-                .replace("https://", "")
-                .replace("https://", "")
-            )
-            if targets['domain'].str.contains(domain).any():
+            if "." not in domain:
+                print(f"Skipping {domain} as not a valid domain")
+                continue
+            else:
+                domain = helpers.clean_domain(domain)  # removes http, https, www, etc
+
+            if domain in existing_search_domains:
                 print(f"Skipping {domain} as already a target")
                 continue
             else:
                 print(f"Adding {domain} as target")
 
+            # should these be in same transaction?
             con.execute(
                 sqlalchemy.text(
                     """
                     INSERT INTO company (domain) 
                     VALUES(:domain)
                     ON CONFLICT DO NOTHING
                     """
@@ -153,33 +146,34 @@
                     VALUES(:search_uid, :domain, :actor_key, :type)
                     """
                 ),
                 {
                     "search_uid": search_uid,
                     "actor_key": actor_key,
                     "domain": domain,
-                    "type": "advance",
+                    "type": last_event_type,
                 },
             )
-        con.execute(sqlalchemy.text("REFRESH MATERIALIZED VIEW target"))
+        
         con.commit()
 
 
 def insert_companies_as_targets(
     companies: List[Any], search_uid: int, actor_key: str
 ) -> None:
-    targets = target(search_uid=search_uid)
+    """Takes Structured Companies (e.g. from source.find_similiar()) and inserts to Review phase"""
+    existing_search_domains = unique_domains(search_uid=search_uid)["domain"].to_list()
     with db.connect() as con:
         for company in companies:
             if company.get("domain") is None:
                 print(f"Missing domain: {company}. Skipping")
                 continue
 
             # elif company["domain"] in targets["domain"]:
-            elif targets['domain'].str.contains(company['domain']).any():
+            elif company["domain"] in existing_search_domains:
                 print(f"Skipping {company['domain']} as already a target")
                 continue
             else:
                 print(f"Adding {company['domain']} as target")
 
             con.execute(
                 sqlalchemy.text(
@@ -206,70 +200,294 @@
                 {
                     "search_uid": search_uid,
                     "actor_key": actor_key,
                     "domain": company.get("domain"),
                     "type": "create",
                 },
             )
-        
-        con.execute(sqlalchemy.text("REFRESH MATERIALIZED VIEW target"))
+
+        # con.execute(sqlalchemy.text("REFRESH MATERIALIZED VIEW target"))
         con.commit()
 
 
 ### READS ###
 
 
-def search():
+def top_actor_per_search() -> pd.DataFrame:
     with db.connect() as conn:
-        result = conn.execute(
-            sqlalchemy.text("SELECT *, meta->>'group' as group FROM search")
+        statement = """
+        WITH ranked_actors AS (
+            SELECT 
+                a.name,
+                s.uid AS search_uid,
+                COUNT(e.id) AS total_validate_count,
+                ROW_NUMBER() OVER (
+                    PARTITION BY s.uid
+                    ORDER BY COUNT(e.id) DESC
+                ) as rn
+            FROM 
+                event e
+            INNER JOIN 
+                actor a ON a.key = e.actor_key
+            INNER JOIN 
+                search s ON s.uid = e.search_uid
+            WHERE
+                a.type = 'research' AND 
+                e.type = 'validate' 
+            GROUP BY 
+                a.name, s.uid
         )
+        SELECT 
+            name, 
+            search_uid, 
+            total_validate_count
+        FROM 
+            ranked_actors
+        WHERE 
+            rn = 1;
+        """
+
+        result = conn.execute(sqlalchemy.text(statement))
         df = pd.DataFrame(result.fetchall(), columns=result.keys())
-    return df
+        return df
 
 
-def target(search_uid: int, last_event_type: str = None):
+def search():
     with db.connect() as conn:
-        if last_event_type is not None:
-            statement = "SELECT * FROM target WHERE search_uid = :search_uid AND last_event_type = :last_event_type"
-            result = conn.execute(
-                sqlalchemy.text(statement),
-                {"search_uid": search_uid, "last_event_type": last_event_type},
-            )
+        statement = """
+        SELECT 
+            s.uid,
+            s.label,
+            (SELECT COUNT(*) 
+            FROM event e
+            WHERE 
+            e.search_uid = s.uid AND e.created >= EXTRACT(EPOCH FROM (NOW() - INTERVAL '7 days')) and type = 'validate'
+            ) AS recent_validate_count
+        FROM 
+            search s;
+        """
+        result = conn.execute(sqlalchemy.text(statement))
+        df = pd.DataFrame(result.fetchall(), columns=result.keys())
 
-        else:
-            statement = "SELECT * FROM target WHERE search_uid = :search_uid"
-            result = conn.execute(
-                sqlalchemy.text(statement),
-                {"search_uid": search_uid},
+        df = df.merge(
+            top_actor_per_search(), left_on="uid", right_on="search_uid", how="left"
+        )  # maybe do this in the SQL above instead
+
+        def _set_group(row):
+            if row["recent_validate_count"] > 0:
+                return "Trending Searches"
+            elif row["total_validate_count"] > 25:
+                return "Top Searches"
+            else:
+                return "All Searches"
+
+        df["group"] = df.apply(_set_group, axis=1)
+        df = df.sort_values(
+            by=["group", "recent_validate_count","total_validate_count", "label"],
+            ascending=[False, False, False, True],
+        )
+
+        df = df.fillna("")
+        # df['label'] = df['label'] + "      (" + df['name'] + ")"
+    return df
+
+def actor() -> pd.DataFrame:
+    with db.connect() as conn:
+        result = conn.execute(
+            sqlalchemy.text(
+                """
+                SELECT * FROM actor
+                """
             )
+        )
+        df = pd.DataFrame(result.fetchall(), columns=result.keys())
+        df = df.drop(columns=["id","created","updated"])
+        return df
+
 
+def search_target_by_last_event_type(search_uid: int, last_event_type: str = None):
+    statement = """
+        SELECT 
+            e.id, 
+            e.search_uid, 
+            e.domain, 
+            e.data, 
+            e.type AS last_event_type, 
+            e.created AS updated,
+            a.name AS updated_by,
+            c.name as name,
+            c.uid as dealcloud_id,
+            c.description as description,
+            c.meta as meta,
+            (c.meta->>'employees') AS employees,
+            (c.meta->>'ownership') AS ownership,
+            (c.meta->>'linkedin') AS linkedin,
+            (r.data->>'rating') AS rating
+        FROM (
+            SELECT 
+                search_uid, 
+                domain, 
+                MAX(created) AS max_created
+            FROM 
+                event
+            WHERE 
+                type NOT IN ('comment','rating','generate','criteria')
+                AND search_uid = :search_uid
+            GROUP BY 
+                domain, search_uid
+        ) AS max_event
+        JOIN event e ON e.domain = max_event.domain AND e.created = max_event.max_created AND e.search_uid = max_event.search_uid 
+        JOIN company c ON c.domain = e.domain
+        JOIN actor a ON a.key = e.actor_key
+        LEFT JOIN (
+            SELECT 
+                search_uid,
+                domain, 
+                MAX(created) AS max_created
+            FROM 
+                event
+            WHERE 
+                type = 'rating'
+            GROUP BY 
+                domain, search_uid
+        ) AS max_rating ON e.domain = max_rating.domain AND e.search_uid = max_rating.search_uid
+        LEFT JOIN event r ON r.domain = max_rating.domain AND r.created = max_rating.max_created;
+    """
+    with db.connect() as conn:
+        result = conn.execute(
+            sqlalchemy.text(statement),
+            {"search_uid": search_uid, "last_event_type": last_event_type},
+        )
         targets = pd.DataFrame(result.fetchall(), columns=result.keys())
 
+    targets = targets[targets["last_event_type"] == last_event_type]
     comments = comment_by_domain(search_uid)
     targets = targets.merge(comments, on="domain", how="left")
 
     # handle sorting
     search = find_search_by_uid(search_uid)
     targets = targets.sort_values(
         by=search.sort.get("field", "domain"),
         ascending=search.sort.get("order") == "asc",
     )
 
     return targets
 
 
+def search_target_export(search_uid: int) -> pd.DataFrame:
+    """Returns all the targets not in rejected or created"""
+
+    statement = """
+        SELECT 
+            e.id, 
+            e.search_uid, 
+            e.domain, 
+            e.type AS last_event_type, 
+            to_timestamp(e.created) AS updated,
+            c.meta as meta,
+            (r.data->>'rating') AS rating
+        FROM (
+            SELECT 
+                search_uid, 
+                domain, 
+                MAX(created) AS max_created
+            FROM 
+                event
+            WHERE 
+                type NOT IN ('comment','rating','generate','criteria') 
+                AND search_uid = :search_uid
+            GROUP BY 
+                domain, search_uid
+        ) AS max_event
+        JOIN event e ON e.domain = max_event.domain AND e.created = max_event.max_created AND e.search_uid = max_event.search_uid 
+        JOIN company c ON c.domain = e.domain
+        LEFT JOIN (
+            SELECT 
+                search_uid,
+                domain, 
+                MAX(created) AS max_created
+            FROM 
+                event
+            WHERE 
+                type = 'rating'
+            GROUP BY 
+                domain, search_uid
+        ) AS max_rating ON e.domain = max_rating.domain AND e.search_uid = max_rating.search_uid
+        LEFT JOIN event r ON r.domain = max_rating.domain AND r.created = max_rating.max_created;
+    """
+    with db.connect() as conn:
+        result = conn.execute(
+            sqlalchemy.text(statement),
+            {"search_uid": search_uid},
+        )
+        targets = pd.DataFrame(result.fetchall(), columns=result.keys())
+        # if len(targets) > 0:
+        #     targets = targets[~targets["last_event_type"].isin(["reject", "create"])]
+        #     meta = pd.json_normalize(targets["meta"], max_level=0)
+        #     targets = targets.merge(
+        #         meta, left_on=["domain"], right_on=["domain"], how="left"
+        #     )
+        #     targets = targets.drop(columns=["meta"])
+        #     targets = targets.sort_values(by=["last_event_type", "domain"])
+    return targets
+
+
+# def target(search_uid: int, last_event_type: str = None):
+#     with db.connect() as conn:
+#         if last_event_type is not None:
+#             statement = "SELECT * FROM target WHERE search_uid = :search_uid AND last_event_type = :last_event_type"
+#             result = conn.execute(
+#                 sqlalchemy.text(statement),
+#                 {"search_uid": search_uid, "last_event_type": last_event_type},
+#             )
+
+#         else:
+#             statement = "SELECT * FROM target WHERE search_uid = :search_uid"
+#             result = conn.execute(
+#                 sqlalchemy.text(statement),
+#                 {"search_uid": search_uid},
+#             )
+
+#         targets = pd.DataFrame(result.fetchall(), columns=result.keys())
+
+#     comments = comment_by_domain(search_uid)
+#     targets = targets.merge(comments, on="domain", how="left")
+
+#     # handle sorting
+#     search = find_search_by_uid(search_uid)
+#     targets = targets.sort_values(
+#         by=search.sort.get("field", "domain"),
+#         ascending=search.sort.get("order") == "asc",
+#     )
+
+#     return targets
+
+
 def target_count(search_uid: int) -> pd.DataFrame:
     with db.connect() as conn:
         statement = """
-                SELECT last_event_type, count(*)
-                FROM target
-                WHERE search_uid = :search_uid
-                GROUP BY last_event_type
-            """
+            SELECT 
+                e.type AS last_event_type,
+                COUNT(e.type)
+            FROM (
+                SELECT 
+                    search_uid, 
+                    domain, 
+                    MAX(created) AS max_created
+                FROM 
+                    event
+                WHERE 
+                    type NOT IN ('comment','rating','generate','criteria')
+                    and search_uid = :search_uid
+                GROUP BY 
+                    domain, search_uid
+            ) AS max_event
+            JOIN event e ON e.domain = max_event.domain AND e.created = max_event.max_created AND e.search_uid = max_event.search_uid
+            GROUP BY e.type;
+        """
         result = conn.execute(
             sqlalchemy.text(statement),
             {"search_uid": search_uid},
         )
         df = pd.DataFrame(result.fetchall(), columns=result.keys())
     return df
 
@@ -282,14 +500,26 @@
                 WHERE search_uid = :search_uid
             """
         result = conn.execute(sqlalchemy.text(statement), {"search_uid": search_uid})
         df = pd.DataFrame(result.fetchall(), columns=result.keys())
     return df
 
 
+def unique_domains(search_uid: int) -> pd.DataFrame:
+    with db.connect() as conn:
+        statement = """
+                SELECT distinct(domain)
+                FROM event
+                WHERE search_uid = :search_uid
+            """
+        result = conn.execute(sqlalchemy.text(statement), {"search_uid": search_uid})
+        df = pd.DataFrame(result.fetchall(), columns=result.keys())
+    return df
+
+
 def company() -> pd.DataFrame:
     with db.connect() as conn:
         statement = """
                 SELECT *
                 FROM company
             """
         result = conn.execute(sqlalchemy.text(statement))
@@ -340,15 +570,17 @@
             """
         result = conn.execute(sqlalchemy.text(statement), {"search_uid": search_uid})
 
     if result.rowcount == 0:
         return None
     else:
         obj = dict(zip(result.keys(), result.fetchone()))
-        return from_dict(Search, obj)
+        search = from_dict(Search, obj)
+        print(search.label)
+        return search
 
 
 def find_company_by_domain(domain: str) -> Company:
     with db.connect() as conn:
         statement = """
                 SELECT *
                 FROM company
@@ -385,28 +617,29 @@
 def update_company(company: Company) -> None:
     with db.connect() as conn:
         statement = """
             UPDATE company
             SET
                 name = :name,
                 description = :description,
-                meta = :meta
+                meta = :meta,
+                updated = FLOOR(EXTRACT(EPOCH FROM NOW()))
             WHERE domain = :domain
             """
 
         conn.execute(
             sqlalchemy.text(statement),
             {
                 "name": company.name,
                 "description": company.description,
                 "domain": company.domain,
                 "meta": json.dumps(company.meta),
             },
         )
-        conn.execute(sqlalchemy.text("REFRESH MATERIALIZED VIEW target"))
+        # conn.execute(sqlalchemy.text("REFRESH MATERIALIZED VIEW target"))
         conn.commit()
 
 
 def update_search(search: Search) -> None:
     with db.connect() as conn:
         conn.execute(
             sqlalchemy.text(
```

### Comparing `gandai-1.2.0/gandai/secrets.py` & `gandai-1.3.0/gandai/secrets.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,30 +1,38 @@
-from google.cloud import secretmanager
 import os
+
 from dotenv import load_dotenv
+from google.cloud import secretmanager
 
 load_dotenv()
 
 PROJECT_ID = os.getenv("PROJECT_ID")
+print(PROJECT_ID)
 
 client = secretmanager.SecretManagerServiceClient()
 
+
 def create_secret(secret_id) -> None:
-    client.create_secret(
-        request={
-            "parent": f"projects/{PROJECT_ID}",
-            "secret_id": secret_id,
-            "secret": {"replication": {"automatic": {}}},
-        }
-    )
+    try:
+        client.create_secret(
+            request={
+                "parent": f"projects/{PROJECT_ID}",
+                "secret_id": secret_id,
+                "secret": {"replication": {"automatic": {}}},
+            }
+        )
+    except Exception as e:
+        print(e)
+
 
 def add_secret_version(secret_id, payload) -> None:
     parent = client.secret_path(PROJECT_ID, secret_id)
     response = client.add_secret_version(
         request={"parent": parent, "payload": {"data": payload.encode("UTF-8")}}
     )
     print("Added secret version: {}".format(response.name))
 
+
 def access_secret_version(secret_id, version_id="latest"):
     name = f"projects/{PROJECT_ID}/secrets/{secret_id}/versions/{version_id}"
     response = client.access_secret_version(name=name)
-    return response.payload.data.decode('UTF-8')
+    return response.payload.data.decode("UTF-8")
```

### Comparing `gandai-1.2.0/gandai.egg-info/SOURCES.txt` & `gandai-1.3.0/gandai.egg-info/SOURCES.txt`

 * *Files 17% similar despite different names*

```diff
@@ -1,29 +1,35 @@
 MANIFEST.in
 pyproject.toml
 setup.py
 gandai/__init__.py
+gandai/analytics.py
 gandai/auth.py
 gandai/datastore.py
 gandai/db.py
+gandai/gpt.py
+gandai/helpers.py
 gandai/main.py
 gandai/models.py
 gandai/query.py
 gandai/secrets.py
 gandai/sources.py
 gandai.egg-info/PKG-INFO
 gandai.egg-info/SOURCES.txt
 gandai.egg-info/dependency_links.txt
 gandai.egg-info/top_level.txt
 gandai/__pycache__/__init__.cpython-311.pyc
 gandai/__pycache__/adapters.cpython-311.pyc
+gandai/__pycache__/analytics.cpython-311.pyc
 gandai/__pycache__/auth.cpython-311.pyc
 gandai/__pycache__/datastore.cpython-311.pyc
 gandai/__pycache__/db.cpython-311.pyc
+gandai/__pycache__/gpt.cpython-311.pyc
 gandai/__pycache__/grata.cpython-311.pyc
+gandai/__pycache__/helpers.cpython-311.pyc
 gandai/__pycache__/main.cpython-311.pyc
 gandai/__pycache__/models.cpython-311.pyc
 gandai/__pycache__/query.cpython-311.pyc
 gandai/__pycache__/secrets.cpython-311.pyc
 gandai/__pycache__/services.cpython-311.pyc
 gandai/__pycache__/sources.cpython-311.pyc
 gandai/migrations/__init__.py
```

