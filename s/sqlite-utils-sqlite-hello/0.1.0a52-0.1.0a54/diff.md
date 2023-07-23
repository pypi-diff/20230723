# Comparing `tmp/sqlite_utils_sqlite_hello-0.1.0a52-py3-none-any.whl.zip` & `tmp/sqlite_utils_sqlite_hello-0.1.0a54-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,9 +1,9 @@
-Zip file size: 2234 bytes, number of entries: 7
--rw-r--r--  2.0 unx      275 b- defN 23-Jul-23 19:10 sqlite_utils_sqlite_hello/__init__.py
--rw-r--r--  2.0 unx       80 b- defN 23-Jul-23 19:10 sqlite_utils_sqlite_hello/version.py
--rw-r--r--  2.0 unx      524 b- defN 23-Jul-23 19:11 sqlite_utils_sqlite_hello-0.1.0a52.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 19:11 sqlite_utils_sqlite_hello-0.1.0a52.dist-info/WHEEL
--rw-r--r--  2.0 unx       63 b- defN 23-Jul-23 19:11 sqlite_utils_sqlite_hello-0.1.0a52.dist-info/entry_points.txt
--rw-r--r--  2.0 unx       26 b- defN 23-Jul-23 19:11 sqlite_utils_sqlite_hello-0.1.0a52.dist-info/top_level.txt
--rw-rw-r--  2.0 unx      681 b- defN 23-Jul-23 19:11 sqlite_utils_sqlite_hello-0.1.0a52.dist-info/RECORD
-7 files, 1741 bytes uncompressed, 988 bytes compressed:  43.3%
+Zip file size: 2239 bytes, number of entries: 7
+-rw-r--r--  2.0 unx      275 b- defN 23-Jul-23 19:18 sqlite_utils_sqlite_hello/__init__.py
+-rw-r--r--  2.0 unx       80 b- defN 23-Jul-23 19:18 sqlite_utils_sqlite_hello/version.py
+-rw-r--r--  2.0 unx      524 b- defN 23-Jul-23 19:18 sqlite_utils_sqlite_hello-0.1.0a54.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 19:18 sqlite_utils_sqlite_hello-0.1.0a54.dist-info/WHEEL
+-rw-r--r--  2.0 unx       63 b- defN 23-Jul-23 19:18 sqlite_utils_sqlite_hello-0.1.0a54.dist-info/entry_points.txt
+-rw-r--r--  2.0 unx       26 b- defN 23-Jul-23 19:18 sqlite_utils_sqlite_hello-0.1.0a54.dist-info/top_level.txt
+-rw-rw-r--  2.0 unx      681 b- defN 23-Jul-23 19:18 sqlite_utils_sqlite_hello-0.1.0a54.dist-info/RECORD
+7 files, 1741 bytes uncompressed, 993 bytes compressed:  43.0%
```

## zipnote {}

```diff
@@ -1,22 +1,22 @@
 Filename: sqlite_utils_sqlite_hello/__init__.py
 Comment: 
 
 Filename: sqlite_utils_sqlite_hello/version.py
 Comment: 
 
-Filename: sqlite_utils_sqlite_hello-0.1.0a52.dist-info/METADATA
+Filename: sqlite_utils_sqlite_hello-0.1.0a54.dist-info/METADATA
 Comment: 
 
-Filename: sqlite_utils_sqlite_hello-0.1.0a52.dist-info/WHEEL
+Filename: sqlite_utils_sqlite_hello-0.1.0a54.dist-info/WHEEL
 Comment: 
 
-Filename: sqlite_utils_sqlite_hello-0.1.0a52.dist-info/entry_points.txt
+Filename: sqlite_utils_sqlite_hello-0.1.0a54.dist-info/entry_points.txt
 Comment: 
 
-Filename: sqlite_utils_sqlite_hello-0.1.0a52.dist-info/top_level.txt
+Filename: sqlite_utils_sqlite_hello-0.1.0a54.dist-info/top_level.txt
 Comment: 
 
-Filename: sqlite_utils_sqlite_hello-0.1.0a52.dist-info/RECORD
+Filename: sqlite_utils_sqlite_hello-0.1.0a54.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## sqlite_utils_sqlite_hello/version.py

```diff
@@ -1,2 +1,2 @@
-__version__ = "0.1.0-alpha.50"
+__version__ = "0.1.0-alpha.54"
 __version_info__ = tuple(__version__.split("."))
```

## Comparing `sqlite_utils_sqlite_hello-0.1.0a52.dist-info/METADATA` & `sqlite_utils_sqlite_hello-0.1.0a54.dist-info/METADATA`

 * *Files 20% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: sqlite-utils-sqlite-hello
-Version: 0.1.0a52
+Version: 0.1.0a54
 Summary: TODO
 Author: Alex Garcia
 License: Apache-2.0
 Project-URL: Homepage, https://github.com/asg017/sqlite-hello
 Project-URL: Changelog, https://github.com/asg017/sqlite-hello/releases
 Project-URL: Issues, https://github.com/asg017/sqlite-hello/issues
 Description-Content-Type: text/markdown
```

## Comparing `sqlite_utils_sqlite_hello-0.1.0a52.dist-info/RECORD` & `sqlite_utils_sqlite_hello-0.1.0a54.dist-info/RECORD`

 * *Files 22% similar despite different names*

```diff
@@ -1,7 +1,7 @@
 sqlite_utils_sqlite_hello/__init__.py,sha256=JgWdsMjIkHfAB-LNthiMSrtmR1j7dntdlpgBUHtT234,275
-sqlite_utils_sqlite_hello/version.py,sha256=xhni3-4xHkHvM2f652mWciQ-IzK7cBnDZf62U0EbY1A,80
-sqlite_utils_sqlite_hello-0.1.0a52.dist-info/METADATA,sha256=SWrNoH1uhkMT2tgMF9Vr8nwlLcKTMHpviY3rm1XCKDI,524
-sqlite_utils_sqlite_hello-0.1.0a52.dist-info/WHEEL,sha256=AtBG6SXL3KF_v0NxLf0ehyVOh0cold-JbJYXNGorC6Q,92
-sqlite_utils_sqlite_hello-0.1.0a52.dist-info/entry_points.txt,sha256=mjsM58WaDOO7MpDJ8fBszvDg-tuE0zmB6mqqUH2qJoo,63
-sqlite_utils_sqlite_hello-0.1.0a52.dist-info/top_level.txt,sha256=RDXX67SyuHEZi7qGbD-6OKES0y-shx1CMoviTs_KLjM,26
-sqlite_utils_sqlite_hello-0.1.0a52.dist-info/RECORD,,
+sqlite_utils_sqlite_hello/version.py,sha256=AVh0GHdxzv4yOSh2XtJJ8P0nJrKyeCxNLFVLGxswTPI,80
+sqlite_utils_sqlite_hello-0.1.0a54.dist-info/METADATA,sha256=jM9mQ0aQkIZsa2dO6I0iwumLVTWGcccyY5a8k6IYBuw,524
+sqlite_utils_sqlite_hello-0.1.0a54.dist-info/WHEEL,sha256=AtBG6SXL3KF_v0NxLf0ehyVOh0cold-JbJYXNGorC6Q,92
+sqlite_utils_sqlite_hello-0.1.0a54.dist-info/entry_points.txt,sha256=mjsM58WaDOO7MpDJ8fBszvDg-tuE0zmB6mqqUH2qJoo,63
+sqlite_utils_sqlite_hello-0.1.0a54.dist-info/top_level.txt,sha256=RDXX67SyuHEZi7qGbD-6OKES0y-shx1CMoviTs_KLjM,26
+sqlite_utils_sqlite_hello-0.1.0a54.dist-info/RECORD,,
```

