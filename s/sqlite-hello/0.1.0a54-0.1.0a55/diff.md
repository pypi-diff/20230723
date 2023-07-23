# Comparing `tmp/sqlite_hello-0.1.0a54-py3-none-manylinux_2_17_x86_64.manylinux2014_x86_64.manylinux1_x86_64.whl.zip` & `tmp/sqlite_hello-0.1.0a55-py3-none-win_amd64.whl.zip`

## zipinfo {}

```diff
@@ -1,11 +1,11 @@
-Zip file size: 8408 bytes, number of entries: 9
--rwxr-xr-x  2.0 unx    15784 b- defN 23-Jul-23 19:18 noop.cpython-311-x86_64-linux-gnu.so
--rw-r--r--  2.0 unx      305 b- defN 23-Jul-23 19:18 sqlite_hello/__init__.py
--rwxr-xr-x  2.0 unx    15856 b- defN 23-Jul-23 19:18 sqlite_hello/hello0.so
--rwxr-xr-x  2.0 unx    15848 b- defN 23-Jul-23 19:18 sqlite_hello/hola0.so
--rw-r--r--  2.0 unx       80 b- defN 23-Jul-23 19:18 sqlite_hello/version.py
--rw-r--r--  2.0 unx      507 b- defN 23-Jul-23 19:18 sqlite_hello-0.1.0a54.dist-info/METADATA
--rw-r--r--  2.0 unx      105 b- defN 23-Jul-23 19:18 sqlite_hello-0.1.0a54.dist-info/WHEEL
--rw-r--r--  2.0 unx       18 b- defN 23-Jul-23 19:18 sqlite_hello-0.1.0a54.dist-info/top_level.txt
--rw-rw-r--  2.0 unx      741 b- defN 23-Jul-23 19:18 sqlite_hello-0.1.0a54.dist-info/RECORD
-9 files, 49244 bytes uncompressed, 7130 bytes compressed:  85.5%
+Zip file size: 33706 bytes, number of entries: 9
+-rw-rw-rw-  2.0 fat        0 b- defN 23-Jul-23 19:43 noop.cp311-win_amd64.pyd
+-rw-rw-rw-  2.0 fat      316 b- defN 23-Jul-23 19:42 sqlite_hello/__init__.py
+-rw-rw-rw-  2.0 fat    47925 b- defN 23-Jul-23 19:43 sqlite_hello/hello0.dll
+-rw-rw-rw-  2.0 fat    47923 b- defN 23-Jul-23 19:43 sqlite_hello/hola0.dll
+-rw-rw-rw-  2.0 fat       82 b- defN 23-Jul-23 19:42 sqlite_hello/version.py
+-rw-rw-rw-  2.0 fat      521 b- defN 23-Jul-23 19:43 sqlite_hello-0.1.0a55.dist-info/METADATA
+-rw-rw-rw-  2.0 fat      102 b- defN 23-Jul-23 19:43 sqlite_hello-0.1.0a55.dist-info/WHEEL
+-rw-rw-rw-  2.0 fat       18 b- defN 23-Jul-23 19:43 sqlite_hello-0.1.0a55.dist-info/top_level.txt
+-rw-rw-r--  2.0 fat      727 b- defN 23-Jul-23 19:43 sqlite_hello-0.1.0a55.dist-info/RECORD
+9 files, 97614 bytes uncompressed, 32448 bytes compressed:  66.8%
```

## zipnote {}

```diff
@@ -1,28 +1,28 @@
-Filename: noop.cpython-311-x86_64-linux-gnu.so
+Filename: noop.cp311-win_amd64.pyd
 Comment: 
 
 Filename: sqlite_hello/__init__.py
 Comment: 
 
-Filename: sqlite_hello/hello0.so
+Filename: sqlite_hello/hello0.dll
 Comment: 
 
-Filename: sqlite_hello/hola0.so
+Filename: sqlite_hello/hola0.dll
 Comment: 
 
 Filename: sqlite_hello/version.py
 Comment: 
 
-Filename: sqlite_hello-0.1.0a54.dist-info/METADATA
+Filename: sqlite_hello-0.1.0a55.dist-info/METADATA
 Comment: 
 
-Filename: sqlite_hello-0.1.0a54.dist-info/WHEEL
+Filename: sqlite_hello-0.1.0a55.dist-info/WHEEL
 Comment: 
 
-Filename: sqlite_hello-0.1.0a54.dist-info/top_level.txt
+Filename: sqlite_hello-0.1.0a55.dist-info/top_level.txt
 Comment: 
 
-Filename: sqlite_hello-0.1.0a54.dist-info/RECORD
+Filename: sqlite_hello-0.1.0a55.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## sqlite_hello/__init__.py

 * *Ordering differences only*

```diff
@@ -1,11 +1,11 @@
-from sqlite_hello.version import __version_info__, __version__
-
-import os
-import sqlite3
-
-def loadable_path():
-  loadable_path = os.path.join(os.path.dirname(__file__), "hello0")
-  return os.path.normpath(loadable_path)
-
-def load(conn: sqlite3.Connection)  -> None:
-  conn.load_extension(loadable_path())
+from sqlite_hello.version import __version_info__, __version__
+
+import os
+import sqlite3
+
+def loadable_path():
+  loadable_path = os.path.join(os.path.dirname(__file__), "hello0")
+  return os.path.normpath(loadable_path)
+
+def load(conn: sqlite3.Connection)  -> None:
+  conn.load_extension(loadable_path())
```

## sqlite_hello/version.py

```diff
@@ -1,2 +1,2 @@
-__version__ = "0.1.0-alpha.54"
-__version_info__ = tuple(__version__.split("."))
+__version__ = "0.1.0-alpha.55"
+__version_info__ = tuple(__version__.split("."))
```

