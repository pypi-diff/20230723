# Comparing `tmp/trino_query_parser-0.405.5-py3-none-any.whl.zip` & `tmp/trino_query_parser-0.515.6-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,14 +1,14 @@
-Zip file size: 141915 bytes, number of entries: 12
--rw-r--r--  2.0 unx    40788 b- defN 23-Jul-23 15:15 trino_query_parser/SqlBase.g4
--rw-r--r--  2.0 unx    99009 b- defN 23-Jul-23 15:15 trino_query_parser/SqlBaseLexer.py
--rw-r--r--  2.0 unx    89277 b- defN 23-Jul-23 15:15 trino_query_parser/SqlBaseListener.py
--rw-r--r--  2.0 unx   860676 b- defN 23-Jul-23 15:15 trino_query_parser/SqlBaseParser.py
--rw-r--r--  2.0 unx    52767 b- defN 23-Jul-23 15:15 trino_query_parser/SqlBaseVisitor.py
--rw-r--r--  2.0 unx      184 b- defN 23-Jul-23 15:15 trino_query_parser/__init__.py
--rw-r--r--  2.0 unx     1021 b- defN 23-Jul-23 15:15 trino_query_parser/error.py
--rw-r--r--  2.0 unx     2574 b- defN 23-Jul-23 15:15 trino_query_parser/parser.py
--rw-r--r--  2.0 unx     1970 b- defN 23-Jul-23 15:16 trino_query_parser-0.405.5.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 15:16 trino_query_parser-0.405.5.dist-info/WHEEL
--rw-r--r--  2.0 unx       19 b- defN 23-Jul-23 15:16 trino_query_parser-0.405.5.dist-info/top_level.txt
--rw-rw-r--  2.0 unx     1067 b- defN 23-Jul-23 15:16 trino_query_parser-0.405.5.dist-info/RECORD
-12 files, 1149444 bytes uncompressed, 140109 bytes compressed:  87.8%
+Zip file size: 141918 bytes, number of entries: 12
+-rw-r--r--  2.0 unx    40788 b- defN 23-Jul-23 15:41 trino_query_parser/SqlBase.g4
+-rw-r--r--  2.0 unx    99009 b- defN 23-Jul-23 15:41 trino_query_parser/SqlBaseLexer.py
+-rw-r--r--  2.0 unx    89277 b- defN 23-Jul-23 15:41 trino_query_parser/SqlBaseListener.py
+-rw-r--r--  2.0 unx   860676 b- defN 23-Jul-23 15:41 trino_query_parser/SqlBaseParser.py
+-rw-r--r--  2.0 unx    52767 b- defN 23-Jul-23 15:41 trino_query_parser/SqlBaseVisitor.py
+-rw-r--r--  2.0 unx      184 b- defN 23-Jul-23 15:41 trino_query_parser/__init__.py
+-rw-r--r--  2.0 unx     1021 b- defN 23-Jul-23 15:41 trino_query_parser/error.py
+-rw-r--r--  2.0 unx     2574 b- defN 23-Jul-23 15:41 trino_query_parser/parser.py
+-rw-r--r--  2.0 unx     1970 b- defN 23-Jul-23 15:41 trino_query_parser-0.515.6.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 15:41 trino_query_parser-0.515.6.dist-info/WHEEL
+-rw-r--r--  2.0 unx       19 b- defN 23-Jul-23 15:41 trino_query_parser-0.515.6.dist-info/top_level.txt
+-rw-rw-r--  2.0 unx     1067 b- defN 23-Jul-23 15:41 trino_query_parser-0.515.6.dist-info/RECORD
+12 files, 1149444 bytes uncompressed, 140112 bytes compressed:  87.8%
```

## zipnote {}

```diff
@@ -18,20 +18,20 @@
 
 Filename: trino_query_parser/error.py
 Comment: 
 
 Filename: trino_query_parser/parser.py
 Comment: 
 
-Filename: trino_query_parser-0.405.5.dist-info/METADATA
+Filename: trino_query_parser-0.515.6.dist-info/METADATA
 Comment: 
 
-Filename: trino_query_parser-0.405.5.dist-info/WHEEL
+Filename: trino_query_parser-0.515.6.dist-info/WHEEL
 Comment: 
 
-Filename: trino_query_parser-0.405.5.dist-info/top_level.txt
+Filename: trino_query_parser-0.515.6.dist-info/top_level.txt
 Comment: 
 
-Filename: trino_query_parser-0.405.5.dist-info/RECORD
+Filename: trino_query_parser-0.515.6.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## Comparing `trino_query_parser-0.405.5.dist-info/METADATA` & `trino_query_parser-0.515.6.dist-info/METADATA`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: trino-query-parser
-Version: 0.405.5
+Version: 0.515.6
 Summary: Provides a parser for trino queries
 Author-email: Gregory Borodin <grihabor@gmail.com>
 License: Apache 2.0
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
```

## Comparing `trino_query_parser-0.405.5.dist-info/RECORD` & `trino_query_parser-0.515.6.dist-info/RECORD`

 * *Files 12% similar despite different names*

```diff
@@ -2,11 +2,11 @@
 trino_query_parser/SqlBaseLexer.py,sha256=o4PzZQRD6tGC9oo_7pMQfDc_jwdZ9Z-wadMZ5nlvKp4,99009
 trino_query_parser/SqlBaseListener.py,sha256=9rYnWviR44xKLbuE7qh8oqCEvh9xgETJgr0di2mO0jg,89277
 trino_query_parser/SqlBaseParser.py,sha256=dQIN2R0gStuxZWIJDrEEKXmjVWWj4_bB0Qs_z40zi4s,860676
 trino_query_parser/SqlBaseVisitor.py,sha256=_VDfetEWZXM1XUa3d5brNdJcmV_rUoPohD871Hui1Q4,52767
 trino_query_parser/__init__.py,sha256=Q6qhZKq0QZOR3X8mO-vCO68PEwJsBonRKBpppy6LWJc,184
 trino_query_parser/error.py,sha256=j71UWYtRs95lWXPUO3SLljpdZsww3xwGidgNHyfihD8,1021
 trino_query_parser/parser.py,sha256=utCt2D_IYZY_fI2wV6G6FdQEJsiLXZ5sz2K3OJvk9XI,2574
-trino_query_parser-0.405.5.dist-info/METADATA,sha256=4R15KfP2UqDIOSevT66b3QQC40tvB1WOplVSDjNTjmI,1970
-trino_query_parser-0.405.5.dist-info/WHEEL,sha256=AtBG6SXL3KF_v0NxLf0ehyVOh0cold-JbJYXNGorC6Q,92
-trino_query_parser-0.405.5.dist-info/top_level.txt,sha256=exnf7p3DwGiEvSfR3lRtQAjSXg9BoauV-OWd6egD-08,19
-trino_query_parser-0.405.5.dist-info/RECORD,,
+trino_query_parser-0.515.6.dist-info/METADATA,sha256=BztJ7gakbn1bSagTTMADZ2RyBnPMD0xP2DsehMp6erY,1970
+trino_query_parser-0.515.6.dist-info/WHEEL,sha256=AtBG6SXL3KF_v0NxLf0ehyVOh0cold-JbJYXNGorC6Q,92
+trino_query_parser-0.515.6.dist-info/top_level.txt,sha256=exnf7p3DwGiEvSfR3lRtQAjSXg9BoauV-OWd6egD-08,19
+trino_query_parser-0.515.6.dist-info/RECORD,,
```

