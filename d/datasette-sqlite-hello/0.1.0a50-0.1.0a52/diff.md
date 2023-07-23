# Comparing `tmp/datasette_sqlite_hello-0.1.0a50-py3-none-any.whl.zip` & `tmp/datasette_sqlite_hello-0.1.0a52-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,9 +1,9 @@
-Zip file size: 2205 bytes, number of entries: 7
--rw-r--r--  2.0 unx      269 b- defN 23-May-31 22:00 datasette_sqlite_hello/__init__.py
--rw-r--r--  2.0 unx       80 b- defN 23-May-31 22:00 datasette_sqlite_hello/version.py
--rw-r--r--  2.0 unx      570 b- defN 23-May-31 22:00 datasette_sqlite_hello-0.1.0a50.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 23-May-31 22:00 datasette_sqlite_hello-0.1.0a50.dist-info/WHEEL
--rw-r--r--  2.0 unx       50 b- defN 23-May-31 22:00 datasette_sqlite_hello-0.1.0a50.dist-info/entry_points.txt
--rw-r--r--  2.0 unx       23 b- defN 23-May-31 22:00 datasette_sqlite_hello-0.1.0a50.dist-info/top_level.txt
--rw-rw-r--  2.0 unx      660 b- defN 23-May-31 22:00 datasette_sqlite_hello-0.1.0a50.dist-info/RECORD
-7 files, 1744 bytes uncompressed, 1001 bytes compressed:  42.6%
+Zip file size: 2204 bytes, number of entries: 7
+-rw-r--r--  2.0 unx      269 b- defN 23-Jul-23 19:04 datasette_sqlite_hello/__init__.py
+-rw-r--r--  2.0 unx       80 b- defN 23-Jul-23 19:04 datasette_sqlite_hello/version.py
+-rw-r--r--  2.0 unx      570 b- defN 23-Jul-23 19:05 datasette_sqlite_hello-0.1.0a52.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 19:05 datasette_sqlite_hello-0.1.0a52.dist-info/WHEEL
+-rw-r--r--  2.0 unx       50 b- defN 23-Jul-23 19:05 datasette_sqlite_hello-0.1.0a52.dist-info/entry_points.txt
+-rw-r--r--  2.0 unx       23 b- defN 23-Jul-23 19:05 datasette_sqlite_hello-0.1.0a52.dist-info/top_level.txt
+-rw-rw-r--  2.0 unx      660 b- defN 23-Jul-23 19:05 datasette_sqlite_hello-0.1.0a52.dist-info/RECORD
+7 files, 1744 bytes uncompressed, 1000 bytes compressed:  42.7%
```

## zipnote {}

```diff
@@ -1,22 +1,22 @@
 Filename: datasette_sqlite_hello/__init__.py
 Comment: 
 
 Filename: datasette_sqlite_hello/version.py
 Comment: 
 
-Filename: datasette_sqlite_hello-0.1.0a50.dist-info/METADATA
+Filename: datasette_sqlite_hello-0.1.0a52.dist-info/METADATA
 Comment: 
 
-Filename: datasette_sqlite_hello-0.1.0a50.dist-info/WHEEL
+Filename: datasette_sqlite_hello-0.1.0a52.dist-info/WHEEL
 Comment: 
 
-Filename: datasette_sqlite_hello-0.1.0a50.dist-info/entry_points.txt
+Filename: datasette_sqlite_hello-0.1.0a52.dist-info/entry_points.txt
 Comment: 
 
-Filename: datasette_sqlite_hello-0.1.0a50.dist-info/top_level.txt
+Filename: datasette_sqlite_hello-0.1.0a52.dist-info/top_level.txt
 Comment: 
 
-Filename: datasette_sqlite_hello-0.1.0a50.dist-info/RECORD
+Filename: datasette_sqlite_hello-0.1.0a52.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## datasette_sqlite_hello/version.py

```diff
@@ -1,2 +1,2 @@
-__version__ = "0.1.0-alpha.50"
+__version__ = "0.1.0-alpha.52"
 __version_info__ = tuple(__version__.split("."))
```

## Comparing `datasette_sqlite_hello-0.1.0a50.dist-info/METADATA` & `datasette_sqlite_hello-0.1.0a52.dist-info/METADATA`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: datasette-sqlite-hello
-Version: 0.1.0a50
+Version: 0.1.0a52
 Home-page: https://github.com/asg017/sqlite-hello
 Author: Alex Garcia
 License: MIT License, Apache License, Version 2.0
 Project-URL: Issues, https://github.com/asg017/sqlite-hello/issues
 Project-URL: CI, https://github.com/asg017/sqlite-hello/actions
 Project-URL: Changelog, https://github.com/asg017/sqlite-hello/releases
 Requires-Python: >=3.6
```

## Comparing `datasette_sqlite_hello-0.1.0a50.dist-info/RECORD` & `datasette_sqlite_hello-0.1.0a52.dist-info/RECORD`

 * *Files 11% similar despite different names*

```diff
@@ -1,7 +1,7 @@
 datasette_sqlite_hello/__init__.py,sha256=GiwcIRu3EMST18OdDMuooqh_Ncg2ePiuYkVT46SHliE,269
-datasette_sqlite_hello/version.py,sha256=xhni3-4xHkHvM2f652mWciQ-IzK7cBnDZf62U0EbY1A,80
-datasette_sqlite_hello-0.1.0a50.dist-info/METADATA,sha256=knNBMlgTErNGMfOQ_G3qPyLU-LPgwB2fFsDe38XWyf4,570
-datasette_sqlite_hello-0.1.0a50.dist-info/WHEEL,sha256=pkctZYzUS4AYVn6dJ-7367OJZivF2e8RA9b_ZBjif18,92
-datasette_sqlite_hello-0.1.0a50.dist-info/entry_points.txt,sha256=X0FnrOoDf3sGgQlWdM3s86QQSGuAZRKfOVfLJcXocpI,50
-datasette_sqlite_hello-0.1.0a50.dist-info/top_level.txt,sha256=klX1wE-1onKhiIgleurv_OT4mMGfe2GmHvNwpSMuYic,23
-datasette_sqlite_hello-0.1.0a50.dist-info/RECORD,,
+datasette_sqlite_hello/version.py,sha256=4DvH3DSUIQ0_fqmao9L7ueq7-hU7H0DxK3E4WljmKhY,80
+datasette_sqlite_hello-0.1.0a52.dist-info/METADATA,sha256=u6Ew4hW41ZqXXS0h-r39vYHO54URUzNsd_S_5bUak5c,570
+datasette_sqlite_hello-0.1.0a52.dist-info/WHEEL,sha256=AtBG6SXL3KF_v0NxLf0ehyVOh0cold-JbJYXNGorC6Q,92
+datasette_sqlite_hello-0.1.0a52.dist-info/entry_points.txt,sha256=X0FnrOoDf3sGgQlWdM3s86QQSGuAZRKfOVfLJcXocpI,50
+datasette_sqlite_hello-0.1.0a52.dist-info/top_level.txt,sha256=klX1wE-1onKhiIgleurv_OT4mMGfe2GmHvNwpSMuYic,23
+datasette_sqlite_hello-0.1.0a52.dist-info/RECORD,,
```

