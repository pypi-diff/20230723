# Comparing `tmp/sqlite_utils_sqlite_hello-0.1.0a54-py3-none-any.whl.zip` & `tmp/sqlite_utils_sqlite_hello-0.1.0a55-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,9 +1,9 @@
-Zip file size: 2239 bytes, number of entries: 7
--rw-r--r--  2.0 unx      275 b- defN 23-Jul-23 19:18 sqlite_utils_sqlite_hello/__init__.py
--rw-r--r--  2.0 unx       80 b- defN 23-Jul-23 19:18 sqlite_utils_sqlite_hello/version.py
--rw-r--r--  2.0 unx      524 b- defN 23-Jul-23 19:18 sqlite_utils_sqlite_hello-0.1.0a54.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 19:18 sqlite_utils_sqlite_hello-0.1.0a54.dist-info/WHEEL
--rw-r--r--  2.0 unx       63 b- defN 23-Jul-23 19:18 sqlite_utils_sqlite_hello-0.1.0a54.dist-info/entry_points.txt
--rw-r--r--  2.0 unx       26 b- defN 23-Jul-23 19:18 sqlite_utils_sqlite_hello-0.1.0a54.dist-info/top_level.txt
--rw-rw-r--  2.0 unx      681 b- defN 23-Jul-23 19:18 sqlite_utils_sqlite_hello-0.1.0a54.dist-info/RECORD
-7 files, 1741 bytes uncompressed, 993 bytes compressed:  43.0%
+Zip file size: 2259 bytes, number of entries: 7
+-rw-rw-rw-  2.0 fat      286 b- defN 23-Jul-23 19:42 sqlite_utils_sqlite_hello/__init__.py
+-rw-rw-rw-  2.0 fat       82 b- defN 23-Jul-23 19:42 sqlite_utils_sqlite_hello/version.py
+-rw-rw-rw-  2.0 fat      540 b- defN 23-Jul-23 19:44 sqlite_utils_sqlite_hello-0.1.0a55.dist-info/METADATA
+-rw-rw-rw-  2.0 fat       92 b- defN 23-Jul-23 19:44 sqlite_utils_sqlite_hello-0.1.0a55.dist-info/WHEEL
+-rw-rw-rw-  2.0 fat       63 b- defN 23-Jul-23 19:44 sqlite_utils_sqlite_hello-0.1.0a55.dist-info/entry_points.txt
+-rw-rw-rw-  2.0 fat       26 b- defN 23-Jul-23 19:44 sqlite_utils_sqlite_hello-0.1.0a55.dist-info/top_level.txt
+-rw-rw-r--  2.0 fat      681 b- defN 23-Jul-23 19:44 sqlite_utils_sqlite_hello-0.1.0a55.dist-info/RECORD
+7 files, 1770 bytes uncompressed, 1013 bytes compressed:  42.8%
```

## zipnote {}

```diff
@@ -1,22 +1,22 @@
 Filename: sqlite_utils_sqlite_hello/__init__.py
 Comment: 
 
 Filename: sqlite_utils_sqlite_hello/version.py
 Comment: 
 
-Filename: sqlite_utils_sqlite_hello-0.1.0a54.dist-info/METADATA
+Filename: sqlite_utils_sqlite_hello-0.1.0a55.dist-info/METADATA
 Comment: 
 
-Filename: sqlite_utils_sqlite_hello-0.1.0a54.dist-info/WHEEL
+Filename: sqlite_utils_sqlite_hello-0.1.0a55.dist-info/WHEEL
 Comment: 
 
-Filename: sqlite_utils_sqlite_hello-0.1.0a54.dist-info/entry_points.txt
+Filename: sqlite_utils_sqlite_hello-0.1.0a55.dist-info/entry_points.txt
 Comment: 
 
-Filename: sqlite_utils_sqlite_hello-0.1.0a54.dist-info/top_level.txt
+Filename: sqlite_utils_sqlite_hello-0.1.0a55.dist-info/top_level.txt
 Comment: 
 
-Filename: sqlite_utils_sqlite_hello-0.1.0a54.dist-info/RECORD
+Filename: sqlite_utils_sqlite_hello-0.1.0a55.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## sqlite_utils_sqlite_hello/__init__.py

 * *Ordering differences only*

```diff
@@ -1,11 +1,11 @@
-from sqlite_utils import hookimpl
-import sqlite_hello
-
-from sqite_utils_sqlite_hello.version import __version_info__, __version__
-
-
-@hookimpl
-def prepare_connection(conn):
-    conn.enable_load_extension(True)
-    sqlite_hello.load(conn)
-    conn.enable_load_extension(False)
+from sqlite_utils import hookimpl
+import sqlite_hello
+
+from sqite_utils_sqlite_hello.version import __version_info__, __version__
+
+
+@hookimpl
+def prepare_connection(conn):
+    conn.enable_load_extension(True)
+    sqlite_hello.load(conn)
+    conn.enable_load_extension(False)
```

## sqlite_utils_sqlite_hello/version.py

```diff
@@ -1,2 +1,2 @@
-__version__ = "0.1.0-alpha.54"
-__version_info__ = tuple(__version__.split("."))
+__version__ = "0.1.0-alpha.55"
+__version_info__ = tuple(__version__.split("."))
```

## Comparing `sqlite_utils_sqlite_hello-0.1.0a54.dist-info/METADATA` & `sqlite_utils_sqlite_hello-0.1.0a55.dist-info/METADATA`

 * *Files 26% similar despite different names*

```diff
@@ -1,16 +1,16 @@
-Metadata-Version: 2.1
-Name: sqlite-utils-sqlite-hello
-Version: 0.1.0a54
-Summary: TODO
-Author: Alex Garcia
-License: Apache-2.0
-Project-URL: Homepage, https://github.com/asg017/sqlite-hello
-Project-URL: Changelog, https://github.com/asg017/sqlite-hello/releases
-Project-URL: Issues, https://github.com/asg017/sqlite-hello/issues
-Description-Content-Type: text/markdown
-Requires-Dist: sqlite-utils
-Requires-Dist: sqlite-hello
-
-# `sqlite-utils-sqlite-hello`
-
-A `sqlite-utils` plugin that registers the `sqlite-hello` extension.
+Metadata-Version: 2.1
+Name: sqlite-utils-sqlite-hello
+Version: 0.1.0a55
+Summary: TODO
+Author: Alex Garcia
+License: Apache-2.0
+Project-URL: Homepage, https://github.com/asg017/sqlite-hello
+Project-URL: Changelog, https://github.com/asg017/sqlite-hello/releases
+Project-URL: Issues, https://github.com/asg017/sqlite-hello/issues
+Description-Content-Type: text/markdown
+Requires-Dist: sqlite-utils
+Requires-Dist: sqlite-hello
+
+# `sqlite-utils-sqlite-hello`
+
+A `sqlite-utils` plugin that registers the `sqlite-hello` extension.
```

## Comparing `sqlite_utils_sqlite_hello-0.1.0a54.dist-info/RECORD` & `sqlite_utils_sqlite_hello-0.1.0a55.dist-info/RECORD`

 * *Files 23% similar despite different names*

```diff
@@ -1,7 +1,7 @@
-sqlite_utils_sqlite_hello/__init__.py,sha256=JgWdsMjIkHfAB-LNthiMSrtmR1j7dntdlpgBUHtT234,275
-sqlite_utils_sqlite_hello/version.py,sha256=AVh0GHdxzv4yOSh2XtJJ8P0nJrKyeCxNLFVLGxswTPI,80
-sqlite_utils_sqlite_hello-0.1.0a54.dist-info/METADATA,sha256=jM9mQ0aQkIZsa2dO6I0iwumLVTWGcccyY5a8k6IYBuw,524
-sqlite_utils_sqlite_hello-0.1.0a54.dist-info/WHEEL,sha256=AtBG6SXL3KF_v0NxLf0ehyVOh0cold-JbJYXNGorC6Q,92
-sqlite_utils_sqlite_hello-0.1.0a54.dist-info/entry_points.txt,sha256=mjsM58WaDOO7MpDJ8fBszvDg-tuE0zmB6mqqUH2qJoo,63
-sqlite_utils_sqlite_hello-0.1.0a54.dist-info/top_level.txt,sha256=RDXX67SyuHEZi7qGbD-6OKES0y-shx1CMoviTs_KLjM,26
-sqlite_utils_sqlite_hello-0.1.0a54.dist-info/RECORD,,
+sqlite_utils_sqlite_hello/__init__.py,sha256=i_81chMPv07EGQdIYYb9FuiBAb-i1fBVi3ImYHXXVho,286
+sqlite_utils_sqlite_hello/version.py,sha256=D1ohCmf7mGH5dOtHOjABGeSG_fY-JdpjpeCo734mcEw,82
+sqlite_utils_sqlite_hello-0.1.0a55.dist-info/METADATA,sha256=pr79V_Cl5Nz-tBXjvCB7eKo766iOW9TFuV4l8W3yn7I,540
+sqlite_utils_sqlite_hello-0.1.0a55.dist-info/WHEEL,sha256=AtBG6SXL3KF_v0NxLf0ehyVOh0cold-JbJYXNGorC6Q,92
+sqlite_utils_sqlite_hello-0.1.0a55.dist-info/entry_points.txt,sha256=mjsM58WaDOO7MpDJ8fBszvDg-tuE0zmB6mqqUH2qJoo,63
+sqlite_utils_sqlite_hello-0.1.0a55.dist-info/top_level.txt,sha256=RDXX67SyuHEZi7qGbD-6OKES0y-shx1CMoviTs_KLjM,26
+sqlite_utils_sqlite_hello-0.1.0a55.dist-info/RECORD,,
```

