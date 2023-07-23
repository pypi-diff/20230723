# Comparing `tmp/trino_query_parser-0.405.4-py3-none-any.whl.zip` & `tmp/trino_query_parser-0.405.5-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,14 +1,14 @@
-Zip file size: 141935 bytes, number of entries: 12
--rw-rw-r--  2.0 unx    40788 b- defN 23-Feb-16 13:09 trino_query_parser/SqlBase.g4
--rw-rw-r--  2.0 unx    99009 b- defN 23-Jan-23 07:52 trino_query_parser/SqlBaseLexer.py
--rw-rw-r--  2.0 unx    89302 b- defN 23-Jan-23 07:52 trino_query_parser/SqlBaseListener.py
--rw-rw-r--  2.0 unx   860508 b- defN 23-Jan-23 07:52 trino_query_parser/SqlBaseParser.py
--rw-rw-r--  2.0 unx    52792 b- defN 23-Jan-23 07:52 trino_query_parser/SqlBaseVisitor.py
--rw-rw-r--  2.0 unx      184 b- defN 23-Jul-23 12:06 trino_query_parser/__init__.py
--rw-rw-r--  2.0 unx     1021 b- defN 23-Jul-23 12:07 trino_query_parser/error.py
--rw-rw-r--  2.0 unx     2574 b- defN 23-Jul-23 12:16 trino_query_parser/parser.py
--rw-rw-r--  2.0 unx     2037 b- defN 23-Jul-23 12:52 trino_query_parser-0.405.4.dist-info/METADATA
--rw-rw-r--  2.0 unx       92 b- defN 23-Jul-23 12:52 trino_query_parser-0.405.4.dist-info/WHEEL
--rw-rw-r--  2.0 unx       19 b- defN 23-Jul-23 12:52 trino_query_parser-0.405.4.dist-info/top_level.txt
--rw-rw-r--  2.0 unx     1067 b- defN 23-Jul-23 12:52 trino_query_parser-0.405.4.dist-info/RECORD
-12 files, 1149393 bytes uncompressed, 140129 bytes compressed:  87.8%
+Zip file size: 141915 bytes, number of entries: 12
+-rw-r--r--  2.0 unx    40788 b- defN 23-Jul-23 15:15 trino_query_parser/SqlBase.g4
+-rw-r--r--  2.0 unx    99009 b- defN 23-Jul-23 15:15 trino_query_parser/SqlBaseLexer.py
+-rw-r--r--  2.0 unx    89277 b- defN 23-Jul-23 15:15 trino_query_parser/SqlBaseListener.py
+-rw-r--r--  2.0 unx   860676 b- defN 23-Jul-23 15:15 trino_query_parser/SqlBaseParser.py
+-rw-r--r--  2.0 unx    52767 b- defN 23-Jul-23 15:15 trino_query_parser/SqlBaseVisitor.py
+-rw-r--r--  2.0 unx      184 b- defN 23-Jul-23 15:15 trino_query_parser/__init__.py
+-rw-r--r--  2.0 unx     1021 b- defN 23-Jul-23 15:15 trino_query_parser/error.py
+-rw-r--r--  2.0 unx     2574 b- defN 23-Jul-23 15:15 trino_query_parser/parser.py
+-rw-r--r--  2.0 unx     1970 b- defN 23-Jul-23 15:16 trino_query_parser-0.405.5.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 15:16 trino_query_parser-0.405.5.dist-info/WHEEL
+-rw-r--r--  2.0 unx       19 b- defN 23-Jul-23 15:16 trino_query_parser-0.405.5.dist-info/top_level.txt
+-rw-rw-r--  2.0 unx     1067 b- defN 23-Jul-23 15:16 trino_query_parser-0.405.5.dist-info/RECORD
+12 files, 1149444 bytes uncompressed, 140109 bytes compressed:  87.8%
```

## zipnote {}

```diff
@@ -18,20 +18,20 @@
 
 Filename: trino_query_parser/error.py
 Comment: 
 
 Filename: trino_query_parser/parser.py
 Comment: 
 
-Filename: trino_query_parser-0.405.4.dist-info/METADATA
+Filename: trino_query_parser-0.405.5.dist-info/METADATA
 Comment: 
 
-Filename: trino_query_parser-0.405.4.dist-info/WHEEL
+Filename: trino_query_parser-0.405.5.dist-info/WHEEL
 Comment: 
 
-Filename: trino_query_parser-0.405.4.dist-info/top_level.txt
+Filename: trino_query_parser-0.405.5.dist-info/top_level.txt
 Comment: 
 
-Filename: trino_query_parser-0.405.4.dist-info/RECORD
+Filename: trino_query_parser-0.405.5.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## trino_query_parser/SqlBaseLexer.py

```diff
@@ -1,8 +1,8 @@
-# Generated from src/trino_query_parser/SqlBase.g4 by ANTLR 4.11.1
+# Generated from src/trino_query_parser/SqlBase.g4 by ANTLR 4.13.0
 from antlr4 import *
 from io import StringIO
 import sys
 if sys.version_info[1] > 5:
     from typing import TextIO
 else:
     from typing.io import TextIO
@@ -1583,13 +1583,13 @@
                   "BACKQUOTED_IDENTIFIER", "EXPONENT", "DIGIT", "LETTER", 
                   "SIMPLE_COMMENT", "BRACKETED_COMMENT", "WS", "UNRECOGNIZED" ]
 
     grammarFileName = "SqlBase.g4"
 
     def __init__(self, input=None, output:TextIO = sys.stdout):
         super().__init__(input, output)
-        self.checkVersion("4.11.1")
+        self.checkVersion("4.13.0")
         self._interp = LexerATNSimulator(self, self.atn, self.decisionsToDFA, PredictionContextCache())
         self._actions = None
         self._predicates = None
```

## trino_query_parser/SqlBaseListener.py

```diff
@@ -1,10 +1,10 @@
-# Generated from src/trino_query_parser/SqlBase.g4 by ANTLR 4.11.1
+# Generated from src/trino_query_parser/SqlBase.g4 by ANTLR 4.13.0
 from antlr4 import *
-if __name__ is not None and "." in __name__:
+if "." in __name__:
     from .SqlBaseParser import SqlBaseParser
 else:
     from SqlBaseParser import SqlBaseParser
 
 # This class defines a complete listener for a parse tree produced by SqlBaseParser.
 class SqlBaseListener(ParseTreeListener):
```

## trino_query_parser/SqlBaseParser.py

```diff
@@ -1,8 +1,8 @@
-# Generated from src/trino_query_parser/SqlBase.g4 by ANTLR 4.11.1
+# Generated from src/trino_query_parser/SqlBase.g4 by ANTLR 4.13.0
 # encoding: utf-8
 from antlr4 import *
 from io import StringIO
 import sys
 if sys.version_info[1] > 5:
 	from typing import TextIO
 else:
@@ -1868,15 +1868,15 @@
     BRACKETED_COMMENT=315
     WS=316
     UNRECOGNIZED=317
     DELIMITER=318
 
     def __init__(self, input:TokenStream, output:TextIO = sys.stdout):
         super().__init__(input, output)
-        self.checkVersion("4.11.1")
+        self.checkVersion("4.13.0")
         self._interp = ParserATNSimulator(self, self.atn, self.decisionsToDFA, self.sharedContextCache)
         self._predicates = None
 
 
 
 
     class SingleStatementContext(ParserRuleContext):
@@ -5670,15 +5670,15 @@
                 _la = self._input.LA(1)
                 if _la==2:
                     self.state = 486
                     self.match(SqlBaseParser.T__1)
                     self.state = 495
                     self._errHandler.sync(self)
                     _la = self._input.LA(1)
-                    if ((_la) & ~0x3f) == 0 and ((1 << _la) & -152137268172423164) != 0 or (((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967872094478427427) != 0 or (((_la - 128)) & ~0x3f) == 0 and ((1 << (_la - 128)) & -24910536512645121) != 0 or (((_la - 192)) & ~0x3f) == 0 and ((1 << (_la - 192)) & -18577486044471361) != 0 or (((_la - 256)) & ~0x3f) == 0 and ((1 << (_la - 256)) & 288096269907246011) != 0:
+                    if (((_la) & ~0x3f) == 0 and ((1 << _la) & -152137268172423164) != 0) or ((((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967872094478427427) != 0) or ((((_la - 128)) & ~0x3f) == 0 and ((1 << (_la - 128)) & -24910536512645121) != 0) or ((((_la - 192)) & ~0x3f) == 0 and ((1 << (_la - 192)) & -18577486044471361) != 0) or ((((_la - 256)) & ~0x3f) == 0 and ((1 << (_la - 256)) & 288096269907246011) != 0):
                         self.state = 487
                         self.callArgument()
                         self.state = 492
                         self._errHandler.sync(self)
                         _la = self._input.LA(1)
                         while _la==4:
                             self.state = 488
@@ -5994,15 +5994,15 @@
                 self.state = 611
                 self.qualifiedName()
                 self.state = 612
                 self.match(SqlBaseParser.T__1)
                 self.state = 621
                 self._errHandler.sync(self)
                 _la = self._input.LA(1)
-                if ((_la) & ~0x3f) == 0 and ((1 << _la) & -152137268172423164) != 0 or (((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967872094478427427) != 0 or (((_la - 128)) & ~0x3f) == 0 and ((1 << (_la - 128)) & -24910536512645121) != 0 or (((_la - 192)) & ~0x3f) == 0 and ((1 << (_la - 192)) & -18577486044471361) != 0 or (((_la - 256)) & ~0x3f) == 0 and ((1 << (_la - 256)) & 288096269907246011) != 0:
+                if (((_la) & ~0x3f) == 0 and ((1 << _la) & -152137268172423164) != 0) or ((((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967872094478427427) != 0) or ((((_la - 128)) & ~0x3f) == 0 and ((1 << (_la - 128)) & -24910536512645121) != 0) or ((((_la - 192)) & ~0x3f) == 0 and ((1 << (_la - 192)) & -18577486044471361) != 0) or ((((_la - 256)) & ~0x3f) == 0 and ((1 << (_la - 256)) & 288096269907246011) != 0):
                     self.state = 613
                     self.callArgument()
                     self.state = 618
                     self._errHandler.sync(self)
                     _la = self._input.LA(1)
                     while _la==4:
                         self.state = 614
@@ -6684,15 +6684,15 @@
                     self._errHandler.recoverInline(self)
                 else:
                     self._errHandler.reportMatch(self)
                     self.consume()
                 self.state = 866
                 self._errHandler.sync(self)
                 _la = self._input.LA(1)
-                if ((_la) & ~0x3f) == 0 and ((1 << _la) & -4601694524648194048) != 0 or (((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967880890680501539) != 0 or (((_la - 133)) & ~0x3f) == 0 and ((1 << (_la - 133)) & -778514395575617) != 0 or (((_la - 197)) & ~0x3f) == 0 and ((1 << (_la - 197)) & -2522596337766367491) != 0 or (((_la - 261)) & ~0x3f) == 0 and ((1 << (_la - 261)) & 8444250369261021) != 0:
+                if (((_la) & ~0x3f) == 0 and ((1 << _la) & -4601694524648194048) != 0) or ((((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967880890680501539) != 0) or ((((_la - 133)) & ~0x3f) == 0 and ((1 << (_la - 133)) & -778514395575617) != 0) or ((((_la - 197)) & ~0x3f) == 0 and ((1 << (_la - 197)) & -2522596337766367491) != 0) or ((((_la - 261)) & ~0x3f) == 0 and ((1 << (_la - 261)) & 8444250369261021) != 0):
                     self.state = 865
                     self.qualifiedName()
 
 
                 self.state = 874
                 self._errHandler.sync(self)
                 _la = self._input.LA(1)
@@ -7120,15 +7120,15 @@
                 self.state = 1009
                 self.match(SqlBaseParser.INTO)
                 self.state = 1010
                 self.qualifiedName()
                 self.state = 1015
                 self._errHandler.sync(self)
                 _la = self._input.LA(1)
-                if ((_la) & ~0x3f) == 0 and ((1 << _la) & -4601694524379758592) != 0 or (((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967880890680501539) != 0 or (((_la - 133)) & ~0x3f) == 0 and ((1 << (_la - 133)) & -778514395575617) != 0 or (((_la - 197)) & ~0x3f) == 0 and ((1 << (_la - 197)) & -2522596337766367491) != 0 or (((_la - 261)) & ~0x3f) == 0 and ((1 << (_la - 261)) & 8444250369261021) != 0:
+                if (((_la) & ~0x3f) == 0 and ((1 << _la) & -4601694524379758592) != 0) or ((((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967880890680501539) != 0) or ((((_la - 133)) & ~0x3f) == 0 and ((1 << (_la - 133)) & -778514395575617) != 0) or ((((_la - 197)) & ~0x3f) == 0 and ((1 << (_la - 197)) & -2522596337766367491) != 0) or ((((_la - 261)) & ~0x3f) == 0 and ((1 << (_la - 261)) & 8444250369261021) != 0):
                     self.state = 1012
                     self._errHandler.sync(self)
                     _la = self._input.LA(1)
                     if _la==28:
                         self.state = 1011
                         self.match(SqlBaseParser.AS)
 
@@ -9065,15 +9065,15 @@
                 self.state = 1235
                 self.match(SqlBaseParser.ROLLUP)
                 self.state = 1236
                 self.match(SqlBaseParser.T__1)
                 self.state = 1245
                 self._errHandler.sync(self)
                 _la = self._input.LA(1)
-                if ((_la) & ~0x3f) == 0 and ((1 << _la) & -152137268172423164) != 0 or (((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967872094478427427) != 0 or (((_la - 128)) & ~0x3f) == 0 and ((1 << (_la - 128)) & -24910536512645121) != 0 or (((_la - 192)) & ~0x3f) == 0 and ((1 << (_la - 192)) & -18577486044471361) != 0 or (((_la - 256)) & ~0x3f) == 0 and ((1 << (_la - 256)) & 288096269907246011) != 0:
+                if (((_la) & ~0x3f) == 0 and ((1 << _la) & -152137268172423164) != 0) or ((((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967872094478427427) != 0) or ((((_la - 128)) & ~0x3f) == 0 and ((1 << (_la - 128)) & -24910536512645121) != 0) or ((((_la - 192)) & ~0x3f) == 0 and ((1 << (_la - 192)) & -18577486044471361) != 0) or ((((_la - 256)) & ~0x3f) == 0 and ((1 << (_la - 256)) & 288096269907246011) != 0):
                     self.state = 1237
                     self.expression()
                     self.state = 1242
                     self._errHandler.sync(self)
                     _la = self._input.LA(1)
                     while _la==4:
                         self.state = 1238
@@ -9096,15 +9096,15 @@
                 self.state = 1248
                 self.match(SqlBaseParser.CUBE)
                 self.state = 1249
                 self.match(SqlBaseParser.T__1)
                 self.state = 1258
                 self._errHandler.sync(self)
                 _la = self._input.LA(1)
-                if ((_la) & ~0x3f) == 0 and ((1 << _la) & -152137268172423164) != 0 or (((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967872094478427427) != 0 or (((_la - 128)) & ~0x3f) == 0 and ((1 << (_la - 128)) & -24910536512645121) != 0 or (((_la - 192)) & ~0x3f) == 0 and ((1 << (_la - 192)) & -18577486044471361) != 0 or (((_la - 256)) & ~0x3f) == 0 and ((1 << (_la - 256)) & 288096269907246011) != 0:
+                if (((_la) & ~0x3f) == 0 and ((1 << _la) & -152137268172423164) != 0) or ((((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967872094478427427) != 0) or ((((_la - 128)) & ~0x3f) == 0 and ((1 << (_la - 128)) & -24910536512645121) != 0) or ((((_la - 192)) & ~0x3f) == 0 and ((1 << (_la - 192)) & -18577486044471361) != 0) or ((((_la - 256)) & ~0x3f) == 0 and ((1 << (_la - 256)) & 288096269907246011) != 0):
                     self.state = 1250
                     self.expression()
                     self.state = 1255
                     self._errHandler.sync(self)
                     _la = self._input.LA(1)
                     while _la==4:
                         self.state = 1251
@@ -9204,15 +9204,15 @@
             if la_ == 1:
                 self.enterOuterAlt(localctx, 1)
                 self.state = 1276
                 self.match(SqlBaseParser.T__1)
                 self.state = 1285
                 self._errHandler.sync(self)
                 _la = self._input.LA(1)
-                if ((_la) & ~0x3f) == 0 and ((1 << _la) & -152137268172423164) != 0 or (((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967872094478427427) != 0 or (((_la - 128)) & ~0x3f) == 0 and ((1 << (_la - 128)) & -24910536512645121) != 0 or (((_la - 192)) & ~0x3f) == 0 and ((1 << (_la - 192)) & -18577486044471361) != 0 or (((_la - 256)) & ~0x3f) == 0 and ((1 << (_la - 256)) & 288096269907246011) != 0:
+                if (((_la) & ~0x3f) == 0 and ((1 << _la) & -152137268172423164) != 0) or ((((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967872094478427427) != 0) or ((((_la - 128)) & ~0x3f) == 0 and ((1 << (_la - 128)) & -24910536512645121) != 0) or ((((_la - 192)) & ~0x3f) == 0 and ((1 << (_la - 192)) & -18577486044471361) != 0) or ((((_la - 256)) & ~0x3f) == 0 and ((1 << (_la - 256)) & 288096269907246011) != 0):
                     self.state = 1277
                     self.expression()
                     self.state = 1282
                     self._errHandler.sync(self)
                     _la = self._input.LA(1)
                     while _la==4:
                         self.state = 1278
@@ -12051,15 +12051,15 @@
                 la_ = self._interp.adaptivePredict(self._input,215,self._ctx)
                 if la_ == 1:
                     self.state = 1688
                     self.match(SqlBaseParser.T__1)
                     self.state = 1697
                     self._errHandler.sync(self)
                     _la = self._input.LA(1)
-                    if ((_la) & ~0x3f) == 0 and ((1 << _la) & -152137268172423164) != 0 or (((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967872094478427427) != 0 or (((_la - 128)) & ~0x3f) == 0 and ((1 << (_la - 128)) & -24910536512645121) != 0 or (((_la - 192)) & ~0x3f) == 0 and ((1 << (_la - 192)) & -18577486044471361) != 0 or (((_la - 256)) & ~0x3f) == 0 and ((1 << (_la - 256)) & 288096269907246011) != 0:
+                    if (((_la) & ~0x3f) == 0 and ((1 << _la) & -152137268172423164) != 0) or ((((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967872094478427427) != 0) or ((((_la - 128)) & ~0x3f) == 0 and ((1 << (_la - 128)) & -24910536512645121) != 0) or ((((_la - 192)) & ~0x3f) == 0 and ((1 << (_la - 192)) & -18577486044471361) != 0) or ((((_la - 256)) & ~0x3f) == 0 and ((1 << (_la - 256)) & 288096269907246011) != 0):
                         self.state = 1689
                         self.expression()
                         self.state = 1694
                         self._errHandler.sync(self)
                         _la = self._input.LA(1)
                         while _la==4:
                             self.state = 1690
@@ -12485,15 +12485,15 @@
         try:
             self.enterOuterAlt(localctx, 1)
             self.state = 1779
             self.identifier()
             self.state = 1781
             self._errHandler.sync(self)
             _la = self._input.LA(1)
-            if ((_la) & ~0x3f) == 0 and ((1 << _la) & -4601694524648194048) != 0 or (((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967880890680501539) != 0 or (((_la - 133)) & ~0x3f) == 0 and ((1 << (_la - 133)) & -778514395575617) != 0 or (((_la - 197)) & ~0x3f) == 0 and ((1 << (_la - 197)) & -2522596337766367491) != 0 or (((_la - 261)) & ~0x3f) == 0 and ((1 << (_la - 261)) & 8444250369261021) != 0:
+            if (((_la) & ~0x3f) == 0 and ((1 << _la) & -4601694524648194048) != 0) or ((((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967880890680501539) != 0) or ((((_la - 133)) & ~0x3f) == 0 and ((1 << (_la - 133)) & -778514395575617) != 0) or ((((_la - 197)) & ~0x3f) == 0 and ((1 << (_la - 197)) & -2522596337766367491) != 0) or ((((_la - 261)) & ~0x3f) == 0 and ((1 << (_la - 261)) & 8444250369261021) != 0):
                 self.state = 1780
                 self.type_(0)
 
 
         except RecognitionException as re:
             localctx.exception = re
             self._errHandler.reportError(self, re)
@@ -13540,15 +13540,15 @@
                         self.state = 1887
                         if not self.precpred(self._ctx, 3):
                             from antlr4.error.Errors import FailedPredicateException
                             raise FailedPredicateException(self, "self.precpred(self._ctx, 3)")
                         self.state = 1888
                         localctx.operator = self._input.LT(1)
                         _la = self._input.LA(1)
-                        if not((((_la - 299)) & ~0x3f) == 0 and ((1 << (_la - 299)) & 7) != 0):
+                        if not(((((_la - 299)) & ~0x3f) == 0 and ((1 << (_la - 299)) & 7) != 0)):
                             localctx.operator = self._errHandler.recoverInline(self)
                         else:
                             self._errHandler.reportMatch(self)
                             self.consume()
                         self.state = 1889
                         localctx.right = self.valueExpression(4)
                         pass
@@ -15184,15 +15184,15 @@
                 self.state = 1981
                 self.qualifiedName()
                 self.state = 1982
                 self.match(SqlBaseParser.T__1)
                 self.state = 1986
                 self._errHandler.sync(self)
                 _la = self._input.LA(1)
-                if ((_la) & ~0x3f) == 0 and ((1 << _la) & -4601694524648194048) != 0 or (((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967880890680501539) != 0 or (((_la - 133)) & ~0x3f) == 0 and ((1 << (_la - 133)) & -778514395575617) != 0 or (((_la - 197)) & ~0x3f) == 0 and ((1 << (_la - 197)) & -2522596337766367491) != 0 or (((_la - 261)) & ~0x3f) == 0 and ((1 << (_la - 261)) & 8444250369261021) != 0:
+                if (((_la) & ~0x3f) == 0 and ((1 << _la) & -4601694524648194048) != 0) or ((((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967880890680501539) != 0) or ((((_la - 133)) & ~0x3f) == 0 and ((1 << (_la - 133)) & -778514395575617) != 0) or ((((_la - 197)) & ~0x3f) == 0 and ((1 << (_la - 197)) & -2522596337766367491) != 0) or ((((_la - 261)) & ~0x3f) == 0 and ((1 << (_la - 261)) & 8444250369261021) != 0):
                     self.state = 1983
                     localctx.label = self.identifier()
                     self.state = 1984
                     self.match(SqlBaseParser.T__0)
 
 
                 self.state = 1988
@@ -15232,15 +15232,15 @@
                 self.state = 1999
                 self.qualifiedName()
                 self.state = 2000
                 self.match(SqlBaseParser.T__1)
                 self.state = 2012
                 self._errHandler.sync(self)
                 _la = self._input.LA(1)
-                if ((_la) & ~0x3f) == 0 and ((1 << _la) & -152137268172423164) != 0 or (((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967872094478426403) != 0 or (((_la - 128)) & ~0x3f) == 0 and ((1 << (_la - 128)) & -24910536512645121) != 0 or (((_la - 192)) & ~0x3f) == 0 and ((1 << (_la - 192)) & -18577486044471361) != 0 or (((_la - 256)) & ~0x3f) == 0 and ((1 << (_la - 256)) & 288096269907246011) != 0:
+                if (((_la) & ~0x3f) == 0 and ((1 << _la) & -152137268172423164) != 0) or ((((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967872094478426403) != 0) or ((((_la - 128)) & ~0x3f) == 0 and ((1 << (_la - 128)) & -24910536512645121) != 0) or ((((_la - 192)) & ~0x3f) == 0 and ((1 << (_la - 192)) & -18577486044471361) != 0) or ((((_la - 256)) & ~0x3f) == 0 and ((1 << (_la - 256)) & 288096269907246011) != 0):
                     self.state = 2002
                     self._errHandler.sync(self)
                     la_ = self._interp.adaptivePredict(self._input,259,self._ctx)
                     if la_ == 1:
                         self.state = 2001
                         self.setQuantifier()
 
@@ -15340,15 +15340,15 @@
                 self._ctx = localctx
                 _prevctx = localctx
                 self.state = 2043
                 self.match(SqlBaseParser.T__1)
                 self.state = 2052
                 self._errHandler.sync(self)
                 _la = self._input.LA(1)
-                if ((_la) & ~0x3f) == 0 and ((1 << _la) & -4601694524648194048) != 0 or (((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967880890680501539) != 0 or (((_la - 133)) & ~0x3f) == 0 and ((1 << (_la - 133)) & -778514395575617) != 0 or (((_la - 197)) & ~0x3f) == 0 and ((1 << (_la - 197)) & -2522596337766367491) != 0 or (((_la - 261)) & ~0x3f) == 0 and ((1 << (_la - 261)) & 8444250369261021) != 0:
+                if (((_la) & ~0x3f) == 0 and ((1 << _la) & -4601694524648194048) != 0) or ((((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967880890680501539) != 0) or ((((_la - 133)) & ~0x3f) == 0 and ((1 << (_la - 133)) & -778514395575617) != 0) or ((((_la - 197)) & ~0x3f) == 0 and ((1 << (_la - 197)) & -2522596337766367491) != 0) or ((((_la - 261)) & ~0x3f) == 0 and ((1 << (_la - 261)) & 8444250369261021) != 0):
                     self.state = 2044
                     self.identifier()
                     self.state = 2049
                     self._errHandler.sync(self)
                     _la = self._input.LA(1)
                     while _la==4:
                         self.state = 2045
@@ -15504,15 +15504,15 @@
                 self.state = 2105
                 self.match(SqlBaseParser.ARRAY)
                 self.state = 2106
                 self.match(SqlBaseParser.T__7)
                 self.state = 2115
                 self._errHandler.sync(self)
                 _la = self._input.LA(1)
-                if ((_la) & ~0x3f) == 0 and ((1 << _la) & -152137268172423164) != 0 or (((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967872094478427427) != 0 or (((_la - 128)) & ~0x3f) == 0 and ((1 << (_la - 128)) & -24910536512645121) != 0 or (((_la - 192)) & ~0x3f) == 0 and ((1 << (_la - 192)) & -18577486044471361) != 0 or (((_la - 256)) & ~0x3f) == 0 and ((1 << (_la - 256)) & 288096269907246011) != 0:
+                if (((_la) & ~0x3f) == 0 and ((1 << _la) & -152137268172423164) != 0) or ((((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967872094478427427) != 0) or ((((_la - 128)) & ~0x3f) == 0 and ((1 << (_la - 128)) & -24910536512645121) != 0) or ((((_la - 192)) & ~0x3f) == 0 and ((1 << (_la - 192)) & -18577486044471361) != 0) or ((((_la - 256)) & ~0x3f) == 0 and ((1 << (_la - 256)) & 288096269907246011) != 0):
                     self.state = 2107
                     self.expression()
                     self.state = 2112
                     self._errHandler.sync(self)
                     _la = self._input.LA(1)
                     while _la==4:
                         self.state = 2108
@@ -15676,15 +15676,15 @@
                         self.state = 2150
                         self.trimsSpecification()
 
 
                     self.state = 2154
                     self._errHandler.sync(self)
                     _la = self._input.LA(1)
-                    if ((_la) & ~0x3f) == 0 and ((1 << _la) & -152137268172423164) != 0 or (((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967872094478427427) != 0 or (((_la - 128)) & ~0x3f) == 0 and ((1 << (_la - 128)) & -24911086268459009) != 0 or (((_la - 192)) & ~0x3f) == 0 and ((1 << (_la - 192)) & -18577486044471361) != 0 or (((_la - 256)) & ~0x3f) == 0 and ((1 << (_la - 256)) & 288096269907246011) != 0:
+                    if (((_la) & ~0x3f) == 0 and ((1 << _la) & -152137268172423164) != 0) or ((((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967872094478427427) != 0) or ((((_la - 128)) & ~0x3f) == 0 and ((1 << (_la - 128)) & -24911086268459009) != 0) or ((((_la - 192)) & ~0x3f) == 0 and ((1 << (_la - 192)) & -18577486044471361) != 0) or ((((_la - 256)) & ~0x3f) == 0 and ((1 << (_la - 256)) & 288096269907246011) != 0):
                         self.state = 2153
                         localctx.trimChar = self.valueExpression(0)
 
 
                     self.state = 2156
                     self.match(SqlBaseParser.FROM)
 
@@ -15802,15 +15802,15 @@
                 self.state = 2200
                 self.match(SqlBaseParser.GROUPING)
                 self.state = 2201
                 self.match(SqlBaseParser.T__1)
                 self.state = 2210
                 self._errHandler.sync(self)
                 _la = self._input.LA(1)
-                if ((_la) & ~0x3f) == 0 and ((1 << _la) & -4601694524648194048) != 0 or (((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967880890680501539) != 0 or (((_la - 133)) & ~0x3f) == 0 and ((1 << (_la - 133)) & -778514395575617) != 0 or (((_la - 197)) & ~0x3f) == 0 and ((1 << (_la - 197)) & -2522596337766367491) != 0 or (((_la - 261)) & ~0x3f) == 0 and ((1 << (_la - 261)) & 8444250369261021) != 0:
+                if (((_la) & ~0x3f) == 0 and ((1 << _la) & -4601694524648194048) != 0) or ((((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967880890680501539) != 0) or ((((_la - 133)) & ~0x3f) == 0 and ((1 << (_la - 133)) & -778514395575617) != 0) or ((((_la - 197)) & ~0x3f) == 0 and ((1 << (_la - 197)) & -2522596337766367491) != 0) or ((((_la - 261)) & ~0x3f) == 0 and ((1 << (_la - 261)) & 8444250369261021) != 0):
                     self.state = 2202
                     self.qualifiedName()
                     self.state = 2207
                     self._errHandler.sync(self)
                     _la = self._input.LA(1)
                     while _la==4:
                         self.state = 2203
@@ -16449,15 +16449,15 @@
             self._errHandler.sync(self)
             _la = self._input.LA(1)
             if _la==80:
                 self.state = 2389
                 self.match(SqlBaseParser.ENCODING)
                 self.state = 2390
                 _la = self._input.LA(1)
-                if not((((_la - 271)) & ~0x3f) == 0 and ((1 << (_la - 271)) & 7) != 0):
+                if not(((((_la - 271)) & ~0x3f) == 0 and ((1 << (_la - 271)) & 7) != 0)):
                     self._errHandler.recoverInline(self)
                 else:
                     self._errHandler.reportMatch(self)
                     self.consume()
 
 
         except RecognitionException as re:
@@ -17348,15 +17348,15 @@
         localctx = SqlBaseParser.ComparisonOperatorContext(self, self._ctx, self.state)
         self.enterRule(localctx, 146, self.RULE_comparisonOperator)
         self._la = 0 # Token type
         try:
             self.enterOuterAlt(localctx, 1)
             self.state = 2463
             _la = self._input.LA(1)
-            if not((((_la - 291)) & ~0x3f) == 0 and ((1 << (_la - 291)) & 63) != 0):
+            if not(((((_la - 291)) & ~0x3f) == 0 and ((1 << (_la - 291)) & 63) != 0)):
                 self._errHandler.recoverInline(self)
             else:
                 self._errHandler.reportMatch(self)
                 self.consume()
         except RecognitionException as re:
             localctx.exception = re
             self._errHandler.reportError(self, re)
@@ -17692,15 +17692,15 @@
         localctx = SqlBaseParser.NormalFormContext(self, self._ctx, self.state)
         self.enterRule(localctx, 156, self.RULE_normalForm)
         self._la = 0 # Token type
         try:
             self.enterOuterAlt(localctx, 1)
             self.state = 2481
             _la = self._input.LA(1)
-            if not((((_la - 160)) & ~0x3f) == 0 and ((1 << (_la - 160)) & 15) != 0):
+            if not(((((_la - 160)) & ~0x3f) == 0 and ((1 << (_la - 160)) & 15) != 0)):
                 self._errHandler.recoverInline(self)
             else:
                 self._errHandler.reportMatch(self)
                 self.consume()
         except RecognitionException as re:
             localctx.exception = re
             self._errHandler.reportError(self, re)
@@ -22442,15 +22442,15 @@
         localctx = SqlBaseParser.NonReservedContext(self, self._ctx, self.state)
         self.enterRule(localctx, 216, self.RULE_nonReserved)
         self._la = 0 # Token type
         try:
             self.enterOuterAlt(localctx, 1)
             self.state = 2950
             _la = self._input.LA(1)
-            if not(((_la) & ~0x3f) == 0 and ((1 << _la) & -4601694524648194048) != 0 or (((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967880890680501539) != 0 or (((_la - 133)) & ~0x3f) == 0 and ((1 << (_la - 133)) & -778514395575617) != 0 or (((_la - 197)) & ~0x3f) == 0 and ((1 << (_la - 197)) & -2522596337766367491) != 0 or (((_la - 261)) & ~0x3f) == 0 and ((1 << (_la - 261)) & 1067941341) != 0):
+            if not((((_la) & ~0x3f) == 0 and ((1 << _la) & -4601694524648194048) != 0) or ((((_la - 64)) & ~0x3f) == 0 and ((1 << (_la - 64)) & -5967880890680501539) != 0) or ((((_la - 133)) & ~0x3f) == 0 and ((1 << (_la - 133)) & -778514395575617) != 0) or ((((_la - 197)) & ~0x3f) == 0 and ((1 << (_la - 197)) & -2522596337766367491) != 0) or ((((_la - 261)) & ~0x3f) == 0 and ((1 << (_la - 261)) & 1067941341) != 0)):
                 self._errHandler.recoverInline(self)
             else:
                 self._errHandler.reportMatch(self)
                 self.consume()
         except RecognitionException as re:
             localctx.exception = re
             self._errHandler.reportError(self, re)
```

## trino_query_parser/SqlBaseVisitor.py

```diff
@@ -1,10 +1,10 @@
-# Generated from src/trino_query_parser/SqlBase.g4 by ANTLR 4.11.1
+# Generated from src/trino_query_parser/SqlBase.g4 by ANTLR 4.13.0
 from antlr4 import *
-if __name__ is not None and "." in __name__:
+if "." in __name__:
     from .SqlBaseParser import SqlBaseParser
 else:
     from SqlBaseParser import SqlBaseParser
 
 # This class defines a complete generic visitor for a parse tree produced by SqlBaseParser.
 
 class SqlBaseVisitor(ParseTreeVisitor):
```

## trino_query_parser/parser.py

```diff
@@ -1,18 +1,18 @@
 import functools
 import re
-from typing import Callable, Generic, TypeVar, Type, Iterator, Any, Tuple
+from typing import Any, Callable, Generic, Iterator, Tuple, Type, TypeVar
 
 from antlr4 import CommonTokenStream, InputStream
 from antlr4.error.ErrorListener import ConsoleErrorListener
 
+from .error import TrinoErrorListener
 from .SqlBaseLexer import SqlBaseLexer
 from .SqlBaseParser import SqlBaseParser
 from .SqlBaseVisitor import SqlBaseVisitor
-from .error import TrinoErrorListener
 
 
 class _TokenVisitor(SqlBaseVisitor):
     def visitTerminal(self, node):
         return str(node)
 
     def aggregateResult(self, aggregate, nextResult):
```

## Comparing `trino_query_parser-0.405.4.dist-info/METADATA` & `trino_query_parser-0.405.5.dist-info/METADATA`

 * *Files 10% similar despite different names*

```diff
@@ -1,22 +1,20 @@
 Metadata-Version: 2.1
 Name: trino-query-parser
-Version: 0.405.4
+Version: 0.405.5
 Summary: Provides a parser for trino queries
 Author-email: Gregory Borodin <grihabor@gmail.com>
 License: Apache 2.0
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Description-Content-Type: text/x-rst
-Requires-Dist: antlr4-python3-runtime (~=4.11)
-Provides-Extra: dev
-Requires-Dist: antlr4-tools ; extra == 'dev'
+Requires-Dist: antlr4-python3-runtime (==4.13.0)
 Provides-Extra: test
 Requires-Dist: pytest ; extra == 'test'
 
 trino-query-parser
 ==================
 
 |pypi| |python|
@@ -65,18 +63,18 @@
 .. warning::
 
     Be careful, API is not stable, it might change in new versions
 
 Development
 -----------
 
-To install development dependencies run:
+To generate antlr4 parser code run:
 
 .. code-block:: bash
 
-    pip install -e .[test,dev]
+    make generate-code
 
-To generate antlr4 parser code run:
+To install development dependencies run:
 
 .. code-block:: bash
 
-    make generate-code
+    pip install -e .[test]
```

## Comparing `trino_query_parser-0.405.4.dist-info/RECORD` & `trino_query_parser-0.405.5.dist-info/RECORD`

 * *Files 16% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 trino_query_parser/SqlBase.g4,sha256=1NiejvPV8cYoc8VZ68z8iRFNxGTrnsmzEkZdiV29-h4,40788
-trino_query_parser/SqlBaseLexer.py,sha256=dptL459RN1KSkskgBChcF5Ku0UhFM49BhR7pq86fXnc,99009
-trino_query_parser/SqlBaseListener.py,sha256=v9N3BpSuF3BmkK1hhomy0_gsXS59ULAvdV6tQEQe1gk,89302
-trino_query_parser/SqlBaseParser.py,sha256=YU92e3cJK6qqRTSflI3cvseHPTKm3GkL8V6OMK7OGUY,860508
-trino_query_parser/SqlBaseVisitor.py,sha256=t9AumleaH6Dsnfk5ErPzoC465R_ICrEcMx-ybnYp_MY,52792
+trino_query_parser/SqlBaseLexer.py,sha256=o4PzZQRD6tGC9oo_7pMQfDc_jwdZ9Z-wadMZ5nlvKp4,99009
+trino_query_parser/SqlBaseListener.py,sha256=9rYnWviR44xKLbuE7qh8oqCEvh9xgETJgr0di2mO0jg,89277
+trino_query_parser/SqlBaseParser.py,sha256=dQIN2R0gStuxZWIJDrEEKXmjVWWj4_bB0Qs_z40zi4s,860676
+trino_query_parser/SqlBaseVisitor.py,sha256=_VDfetEWZXM1XUa3d5brNdJcmV_rUoPohD871Hui1Q4,52767
 trino_query_parser/__init__.py,sha256=Q6qhZKq0QZOR3X8mO-vCO68PEwJsBonRKBpppy6LWJc,184
 trino_query_parser/error.py,sha256=j71UWYtRs95lWXPUO3SLljpdZsww3xwGidgNHyfihD8,1021
-trino_query_parser/parser.py,sha256=JZ-FlwyeDm4cj4gaSM1WqPUJhVaW2LIST-eEu3bvwTw,2574
-trino_query_parser-0.405.4.dist-info/METADATA,sha256=Vo_MTKBYHRrLlpA6hFVh4CO6OLv_dZlGbd0pGL7BLYg,2037
-trino_query_parser-0.405.4.dist-info/WHEEL,sha256=AtBG6SXL3KF_v0NxLf0ehyVOh0cold-JbJYXNGorC6Q,92
-trino_query_parser-0.405.4.dist-info/top_level.txt,sha256=exnf7p3DwGiEvSfR3lRtQAjSXg9BoauV-OWd6egD-08,19
-trino_query_parser-0.405.4.dist-info/RECORD,,
+trino_query_parser/parser.py,sha256=utCt2D_IYZY_fI2wV6G6FdQEJsiLXZ5sz2K3OJvk9XI,2574
+trino_query_parser-0.405.5.dist-info/METADATA,sha256=4R15KfP2UqDIOSevT66b3QQC40tvB1WOplVSDjNTjmI,1970
+trino_query_parser-0.405.5.dist-info/WHEEL,sha256=AtBG6SXL3KF_v0NxLf0ehyVOh0cold-JbJYXNGorC6Q,92
+trino_query_parser-0.405.5.dist-info/top_level.txt,sha256=exnf7p3DwGiEvSfR3lRtQAjSXg9BoauV-OWd6egD-08,19
+trino_query_parser-0.405.5.dist-info/RECORD,,
```

