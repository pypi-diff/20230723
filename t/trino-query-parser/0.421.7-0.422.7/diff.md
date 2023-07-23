# Comparing `tmp/trino_query_parser-0.421.7-py3-none-any.whl.zip` & `tmp/trino_query_parser-0.422.7-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,14 +1,14 @@
-Zip file size: 149381 bytes, number of entries: 12
--rw-r--r--  2.0 unx    43431 b- defN 23-Jul-23 16:04 trino_query_parser/SqlBase.g4
+Zip file size: 149383 bytes, number of entries: 12
+-rw-r--r--  2.0 unx    43434 b- defN 23-Jul-23 16:04 trino_query_parser/SqlBase.g4
 -rw-r--r--  2.0 unx   102372 b- defN 23-Jul-23 16:04 trino_query_parser/SqlBaseLexer.py
--rw-r--r--  2.0 unx    93804 b- defN 23-Jul-23 16:04 trino_query_parser/SqlBaseListener.py
--rw-r--r--  2.0 unx   917534 b- defN 23-Jul-23 16:04 trino_query_parser/SqlBaseParser.py
--rw-r--r--  2.0 unx    55443 b- defN 23-Jul-23 16:04 trino_query_parser/SqlBaseVisitor.py
+-rw-r--r--  2.0 unx    93804 b- defN 23-Jul-23 16:05 trino_query_parser/SqlBaseListener.py
+-rw-r--r--  2.0 unx   917543 b- defN 23-Jul-23 16:05 trino_query_parser/SqlBaseParser.py
+-rw-r--r--  2.0 unx    55443 b- defN 23-Jul-23 16:05 trino_query_parser/SqlBaseVisitor.py
 -rw-r--r--  2.0 unx      184 b- defN 23-Jul-23 16:04 trino_query_parser/__init__.py
 -rw-r--r--  2.0 unx     1021 b- defN 23-Jul-23 16:04 trino_query_parser/error.py
 -rw-r--r--  2.0 unx     2574 b- defN 23-Jul-23 16:04 trino_query_parser/parser.py
--rw-r--r--  2.0 unx     1970 b- defN 23-Jul-23 16:05 trino_query_parser-0.421.7.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 16:05 trino_query_parser-0.421.7.dist-info/WHEEL
--rw-r--r--  2.0 unx       19 b- defN 23-Jul-23 16:05 trino_query_parser-0.421.7.dist-info/top_level.txt
--rw-rw-r--  2.0 unx     1068 b- defN 23-Jul-23 16:05 trino_query_parser-0.421.7.dist-info/RECORD
-12 files, 1219512 bytes uncompressed, 147575 bytes compressed:  87.9%
+-rw-r--r--  2.0 unx     1970 b- defN 23-Jul-23 16:05 trino_query_parser-0.422.7.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 16:05 trino_query_parser-0.422.7.dist-info/WHEEL
+-rw-r--r--  2.0 unx       19 b- defN 23-Jul-23 16:05 trino_query_parser-0.422.7.dist-info/top_level.txt
+-rw-rw-r--  2.0 unx     1068 b- defN 23-Jul-23 16:05 trino_query_parser-0.422.7.dist-info/RECORD
+12 files, 1219524 bytes uncompressed, 147577 bytes compressed:  87.9%
```

## zipnote {}

```diff
@@ -18,20 +18,20 @@
 
 Filename: trino_query_parser/error.py
 Comment: 
 
 Filename: trino_query_parser/parser.py
 Comment: 
 
-Filename: trino_query_parser-0.421.7.dist-info/METADATA
+Filename: trino_query_parser-0.422.7.dist-info/METADATA
 Comment: 
 
-Filename: trino_query_parser-0.421.7.dist-info/WHEEL
+Filename: trino_query_parser-0.422.7.dist-info/WHEEL
 Comment: 
 
-Filename: trino_query_parser-0.421.7.dist-info/top_level.txt
+Filename: trino_query_parser-0.422.7.dist-info/top_level.txt
 Comment: 
 
-Filename: trino_query_parser-0.421.7.dist-info/RECORD
+Filename: trino_query_parser-0.422.7.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## trino_query_parser/SqlBase.g4

```diff
@@ -194,15 +194,15 @@
 
 tableElement
     : columnDefinition
     | likeClause
     ;
 
 columnDefinition
-    : identifier type (NOT NULL)? (COMMENT string)? (WITH properties)?
+    : qualifiedName type (NOT NULL)? (COMMENT string)? (WITH properties)?
     ;
 
 likeClause
     : LIKE qualifiedName (optionType=(INCLUDING | EXCLUDING) PROPERTIES)?
     ;
 
 properties
```

## trino_query_parser/SqlBaseParser.py

```diff
@@ -621,15 +621,15 @@
         1092,1094,3,14,7,0,1093,1092,1,0,0,0,1093,1094,1,0,0,0,1094,1095,
         1,0,0,0,1095,1096,3,30,15,0,1096,13,1,0,0,0,1097,1099,5,288,0,0,
         1098,1100,5,210,0,0,1099,1098,1,0,0,0,1099,1100,1,0,0,0,1100,1101,
         1,0,0,0,1101,1106,3,54,27,0,1102,1103,5,4,0,0,1103,1105,3,54,27,
         0,1104,1102,1,0,0,0,1105,1108,1,0,0,0,1106,1104,1,0,0,0,1106,1107,
         1,0,0,0,1107,15,1,0,0,0,1108,1106,1,0,0,0,1109,1112,3,18,9,0,1110,
         1112,3,20,10,0,1111,1109,1,0,0,0,1111,1110,1,0,0,0,1112,17,1,0,0,
-        0,1113,1114,3,222,111,0,1114,1117,3,168,84,0,1115,1116,5,171,0,0,
+        0,1113,1114,3,210,105,0,1114,1117,3,168,84,0,1115,1116,5,171,0,0,
         1116,1118,5,172,0,0,1117,1115,1,0,0,0,1117,1118,1,0,0,0,1118,1121,
         1,0,0,0,1119,1120,5,44,0,0,1120,1122,3,152,76,0,1121,1119,1,0,0,
         0,1121,1122,1,0,0,0,1122,1125,1,0,0,0,1123,1124,5,288,0,0,1124,1126,
         3,22,11,0,1125,1123,1,0,0,0,1125,1126,1,0,0,0,1126,19,1,0,0,0,1127,
         1128,5,144,0,0,1128,1131,3,210,105,0,1129,1130,7,4,0,0,1130,1132,
         5,205,0,0,1131,1129,1,0,0,0,1131,1132,1,0,0,0,1132,21,1,0,0,0,1133,
         1134,5,2,0,0,1134,1135,3,24,12,0,1135,1136,5,3,0,0,1136,23,1,0,0,
@@ -7779,16 +7779,16 @@
     class ColumnDefinitionContext(ParserRuleContext):
         __slots__ = 'parser'
 
         def __init__(self, parser, parent:ParserRuleContext=None, invokingState:int=-1):
             super().__init__(parent, invokingState)
             self.parser = parser
 
-        def identifier(self):
-            return self.getTypedRuleContext(SqlBaseParser.IdentifierContext,0)
+        def qualifiedName(self):
+            return self.getTypedRuleContext(SqlBaseParser.QualifiedNameContext,0)
 
 
         def type_(self):
             return self.getTypedRuleContext(SqlBaseParser.TypeContext,0)
 
 
         def NOT(self):
@@ -7835,15 +7835,15 @@
 
         localctx = SqlBaseParser.ColumnDefinitionContext(self, self._ctx, self.state)
         self.enterRule(localctx, 18, self.RULE_columnDefinition)
         self._la = 0 # Token type
         try:
             self.enterOuterAlt(localctx, 1)
             self.state = 1113
-            self.identifier()
+            self.qualifiedName()
             self.state = 1114
             self.type_(0)
             self.state = 1117
             self._errHandler.sync(self)
             _la = self._input.LA(1)
             if _la==171:
                 self.state = 1115
```

## Comparing `trino_query_parser-0.421.7.dist-info/METADATA` & `trino_query_parser-0.422.7.dist-info/METADATA`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: trino-query-parser
-Version: 0.421.7
+Version: 0.422.7
 Summary: Provides a parser for trino queries
 Author-email: Gregory Borodin <grihabor@gmail.com>
 License: Apache 2.0
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
```

## Comparing `trino_query_parser-0.421.7.dist-info/RECORD` & `trino_query_parser-0.422.7.dist-info/RECORD`

 * *Files 8% similar despite different names*

```diff
@@ -1,12 +1,12 @@
-trino_query_parser/SqlBase.g4,sha256=okfFQesrlLuIbvIvTSzt7qFV3DfuAQoTUxw2MRQhF2Y,43431
+trino_query_parser/SqlBase.g4,sha256=OSQ8TNwmlJ0kwPv0KQiCHb8MaPxTJIV45SgqLdkoLMs,43434
 trino_query_parser/SqlBaseLexer.py,sha256=gmzkVEGVr1U1J8-4lroXwdJToB-dm62ScNFOR2NBV7k,102372
 trino_query_parser/SqlBaseListener.py,sha256=4sWBfVOTPbGVmOMnugbTPP9zHl5dfJj5XklGZOLWg-Y,93804
-trino_query_parser/SqlBaseParser.py,sha256=4g7tPCP0lyHLu2VaQYM0wDHHRzRtSgvrESNIRwc1Bzs,917534
+trino_query_parser/SqlBaseParser.py,sha256=pfLQb_AFoIcLyMubz3TgAPjq62nM9seN4LgUyUyrtWo,917543
 trino_query_parser/SqlBaseVisitor.py,sha256=6Yjki7jIfKgOKBGmf5K2p7YQCvxgLgPxI-qJ-QcYu7I,55443
 trino_query_parser/__init__.py,sha256=Q6qhZKq0QZOR3X8mO-vCO68PEwJsBonRKBpppy6LWJc,184
 trino_query_parser/error.py,sha256=j71UWYtRs95lWXPUO3SLljpdZsww3xwGidgNHyfihD8,1021
 trino_query_parser/parser.py,sha256=utCt2D_IYZY_fI2wV6G6FdQEJsiLXZ5sz2K3OJvk9XI,2574
-trino_query_parser-0.421.7.dist-info/METADATA,sha256=gVnwC9e6gz0k5XPnqlVJe4jYqVm0Vg7vmKMU1JTRe0k,1970
-trino_query_parser-0.421.7.dist-info/WHEEL,sha256=AtBG6SXL3KF_v0NxLf0ehyVOh0cold-JbJYXNGorC6Q,92
-trino_query_parser-0.421.7.dist-info/top_level.txt,sha256=exnf7p3DwGiEvSfR3lRtQAjSXg9BoauV-OWd6egD-08,19
-trino_query_parser-0.421.7.dist-info/RECORD,,
+trino_query_parser-0.422.7.dist-info/METADATA,sha256=IgKnKVfPZAVLVIQ2GJMYbXAfM3IvkwtnniZKwH8QyZk,1970
+trino_query_parser-0.422.7.dist-info/WHEEL,sha256=AtBG6SXL3KF_v0NxLf0ehyVOh0cold-JbJYXNGorC6Q,92
+trino_query_parser-0.422.7.dist-info/top_level.txt,sha256=exnf7p3DwGiEvSfR3lRtQAjSXg9BoauV-OWd6egD-08,19
+trino_query_parser-0.422.7.dist-info/RECORD,,
```

