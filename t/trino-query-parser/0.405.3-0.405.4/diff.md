# Comparing `tmp/trino_query_parser-0.405.3-py3-none-any.whl.zip` & `tmp/trino_query_parser-0.405.4-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,14 +1,14 @@
-Zip file size: 141892 bytes, number of entries: 12
--rw-rw-r--  2.0 unx    40788 b- defN 23-Jan-21 21:25 trino_query_parser/SqlBase.g4
+Zip file size: 141935 bytes, number of entries: 12
+-rw-rw-r--  2.0 unx    40788 b- defN 23-Feb-16 13:09 trino_query_parser/SqlBase.g4
 -rw-rw-r--  2.0 unx    99009 b- defN 23-Jan-23 07:52 trino_query_parser/SqlBaseLexer.py
 -rw-rw-r--  2.0 unx    89302 b- defN 23-Jan-23 07:52 trino_query_parser/SqlBaseListener.py
 -rw-rw-r--  2.0 unx   860508 b- defN 23-Jan-23 07:52 trino_query_parser/SqlBaseParser.py
 -rw-rw-r--  2.0 unx    52792 b- defN 23-Jan-23 07:52 trino_query_parser/SqlBaseVisitor.py
--rw-rw-r--  2.0 unx      184 b- defN 23-Jan-22 21:41 trino_query_parser/__init__.py
--rw-rw-r--  2.0 unx     1021 b- defN 23-Jan-23 07:57 trino_query_parser/error.py
--rw-rw-r--  2.0 unx     2580 b- defN 23-Jan-23 08:06 trino_query_parser/parser.py
--rw-rw-r--  2.0 unx     1746 b- defN 23-Jan-23 08:07 trino_query_parser-0.405.3.dist-info/METADATA
--rw-rw-r--  2.0 unx       92 b- defN 23-Jan-23 08:07 trino_query_parser-0.405.3.dist-info/WHEEL
--rw-rw-r--  2.0 unx       19 b- defN 23-Jan-23 08:07 trino_query_parser-0.405.3.dist-info/top_level.txt
-?rw-rw-r--  2.0 unx     1067 b- defN 23-Jan-23 08:07 trino_query_parser-0.405.3.dist-info/RECORD
-12 files, 1149108 bytes uncompressed, 140086 bytes compressed:  87.8%
+-rw-rw-r--  2.0 unx      184 b- defN 23-Jul-23 12:06 trino_query_parser/__init__.py
+-rw-rw-r--  2.0 unx     1021 b- defN 23-Jul-23 12:07 trino_query_parser/error.py
+-rw-rw-r--  2.0 unx     2574 b- defN 23-Jul-23 12:16 trino_query_parser/parser.py
+-rw-rw-r--  2.0 unx     2037 b- defN 23-Jul-23 12:52 trino_query_parser-0.405.4.dist-info/METADATA
+-rw-rw-r--  2.0 unx       92 b- defN 23-Jul-23 12:52 trino_query_parser-0.405.4.dist-info/WHEEL
+-rw-rw-r--  2.0 unx       19 b- defN 23-Jul-23 12:52 trino_query_parser-0.405.4.dist-info/top_level.txt
+-rw-rw-r--  2.0 unx     1067 b- defN 23-Jul-23 12:52 trino_query_parser-0.405.4.dist-info/RECORD
+12 files, 1149393 bytes uncompressed, 140129 bytes compressed:  87.8%
```

## zipnote {}

```diff
@@ -18,20 +18,20 @@
 
 Filename: trino_query_parser/error.py
 Comment: 
 
 Filename: trino_query_parser/parser.py
 Comment: 
 
-Filename: trino_query_parser-0.405.3.dist-info/METADATA
+Filename: trino_query_parser-0.405.4.dist-info/METADATA
 Comment: 
 
-Filename: trino_query_parser-0.405.3.dist-info/WHEEL
+Filename: trino_query_parser-0.405.4.dist-info/WHEEL
 Comment: 
 
-Filename: trino_query_parser-0.405.3.dist-info/top_level.txt
+Filename: trino_query_parser-0.405.4.dist-info/top_level.txt
 Comment: 
 
-Filename: trino_query_parser-0.405.3.dist-info/RECORD
+Filename: trino_query_parser-0.405.4.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## trino_query_parser/parser.py

```diff
@@ -1,10 +1,10 @@
 import functools
 import re
-from typing import Callable, Generic, TypeVar, Type, Iterator, Any, Union, List
+from typing import Callable, Generic, TypeVar, Type, Iterator, Any, Tuple
 
 from antlr4 import CommonTokenStream, InputStream
 from antlr4.error.ErrorListener import ConsoleErrorListener
 
 from .SqlBaseLexer import SqlBaseLexer
 from .SqlBaseParser import SqlBaseParser
 from .SqlBaseVisitor import SqlBaseVisitor
@@ -51,15 +51,15 @@
     return visitor.visit(tree)
 
 
 F = TypeVar("F", bound=Callable)
 
 
 class OverrideMethods(Generic[F]):
-    def __init__(self, methods: Iterator[tuple[str, Callable]]):
+    def __init__(self, methods: Iterator[Tuple[str, Callable]]):
         self.methods = methods
 
     def __call__(self, cls: Type):
         for name, method in self.methods:
             setattr(cls, name, method)
 
         return cls
```

## Comparing `trino_query_parser-0.405.3.dist-info/METADATA` & `trino_query_parser-0.405.4.dist-info/METADATA`

 * *Files 18% similar despite different names*

```diff
@@ -1,28 +1,35 @@
 Metadata-Version: 2.1
 Name: trino-query-parser
-Version: 0.405.3
+Version: 0.405.4
 Summary: Provides a parser for trino queries
 Author-email: Gregory Borodin <grihabor@gmail.com>
 License: Apache 2.0
-Classifier: Programming Language :: Python :: 3
+Classifier: Programming Language :: Python :: 3.7
+Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Description-Content-Type: text/x-rst
 Requires-Dist: antlr4-python3-runtime (~=4.11)
 Provides-Extra: dev
 Requires-Dist: antlr4-tools ; extra == 'dev'
 Provides-Extra: test
 Requires-Dist: pytest ; extra == 'test'
 
 trino-query-parser
 ==================
 
-.. image:: https://badge.fury.io/py/trino-query-parser.svg
-    :target: https://badge.fury.io/py/trino-query-parser
+|pypi| |python|
 
-|
+.. |pypi| image:: https://img.shields.io/pypi/v/trino-query-parser
+  :alt: PyPI
+
+.. |python| image:: https://img.shields.io/pypi/pyversions/trino-query-parser
+  :alt: PyPI - Python Version
 
 The package provides a parser for trino queries.
 
 Install
 -------
 
 To install the package run:
```

## Comparing `trino_query_parser-0.405.3.dist-info/RECORD` & `trino_query_parser-0.405.4.dist-info/RECORD`

 * *Files 25% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 trino_query_parser/SqlBase.g4,sha256=1NiejvPV8cYoc8VZ68z8iRFNxGTrnsmzEkZdiV29-h4,40788
 trino_query_parser/SqlBaseLexer.py,sha256=dptL459RN1KSkskgBChcF5Ku0UhFM49BhR7pq86fXnc,99009
 trino_query_parser/SqlBaseListener.py,sha256=v9N3BpSuF3BmkK1hhomy0_gsXS59ULAvdV6tQEQe1gk,89302
 trino_query_parser/SqlBaseParser.py,sha256=YU92e3cJK6qqRTSflI3cvseHPTKm3GkL8V6OMK7OGUY,860508
 trino_query_parser/SqlBaseVisitor.py,sha256=t9AumleaH6Dsnfk5ErPzoC465R_ICrEcMx-ybnYp_MY,52792
 trino_query_parser/__init__.py,sha256=Q6qhZKq0QZOR3X8mO-vCO68PEwJsBonRKBpppy6LWJc,184
 trino_query_parser/error.py,sha256=j71UWYtRs95lWXPUO3SLljpdZsww3xwGidgNHyfihD8,1021
-trino_query_parser/parser.py,sha256=IKLhQ2OVnyAxFPLaBmSekRjeul3xDxgJEcbL7gHexpg,2580
-trino_query_parser-0.405.3.dist-info/METADATA,sha256=3kaV_YgVC4hCY9fqjxsO5zCJVwYgajoANDgi0rz2raA,1746
-trino_query_parser-0.405.3.dist-info/WHEEL,sha256=2wepM1nk4DS4eFpYrW1TTqPcoGNfHhhO_i5m4cOimbo,92
-trino_query_parser-0.405.3.dist-info/top_level.txt,sha256=exnf7p3DwGiEvSfR3lRtQAjSXg9BoauV-OWd6egD-08,19
-trino_query_parser-0.405.3.dist-info/RECORD,,
+trino_query_parser/parser.py,sha256=JZ-FlwyeDm4cj4gaSM1WqPUJhVaW2LIST-eEu3bvwTw,2574
+trino_query_parser-0.405.4.dist-info/METADATA,sha256=Vo_MTKBYHRrLlpA6hFVh4CO6OLv_dZlGbd0pGL7BLYg,2037
+trino_query_parser-0.405.4.dist-info/WHEEL,sha256=AtBG6SXL3KF_v0NxLf0ehyVOh0cold-JbJYXNGorC6Q,92
+trino_query_parser-0.405.4.dist-info/top_level.txt,sha256=exnf7p3DwGiEvSfR3lRtQAjSXg9BoauV-OWd6egD-08,19
+trino_query_parser-0.405.4.dist-info/RECORD,,
```

