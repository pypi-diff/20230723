# Comparing `tmp/recompose-1.0.0a1-py3-none-any.whl.zip` & `tmp/recompose-1.0.0b0-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,10 +1,29 @@
-Zip file size: 2943 bytes, number of entries: 8
--rw-r--r--  2.0 unx       14 b- defN 23-Jul-22 06:59 recompose/VERSION
--rw-r--r--  2.0 unx      200 b- defN 23-Jul-22 06:59 recompose/__init__.py
--rw-r--r--  2.0 unx        0 b- defN 23-Jul-22 06:59 recompose/py.typed
--rw-r--r--  2.0 unx     1073 b- defN 23-Jul-22 06:59 recompose-1.0.0a1.dist-info/LICENSE
--rw-r--r--  2.0 unx     1058 b- defN 23-Jul-22 06:59 recompose-1.0.0a1.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 23-Jul-22 06:59 recompose-1.0.0a1.dist-info/WHEEL
--rw-r--r--  2.0 unx       10 b- defN 23-Jul-22 06:59 recompose-1.0.0a1.dist-info/top_level.txt
--rw-rw-r--  2.0 unx      627 b- defN 23-Jul-22 06:59 recompose-1.0.0a1.dist-info/RECORD
-8 files, 3074 bytes uncompressed, 1843 bytes compressed:  40.0%
+Zip file size: 10807 bytes, number of entries: 27
+-rw-r--r--  2.0 unx       13 b- defN 23-Jul-22 17:54 recompose/VERSION
+-rw-r--r--  2.0 unx     1031 b- defN 23-Jul-22 17:54 recompose/__init__.py
+-rw-r--r--  2.0 unx     1264 b- defN 23-Jul-22 17:54 recompose/cursor.py
+-rw-r--r--  2.0 unx     1019 b- defN 23-Jul-22 17:54 recompose/cursors.py
+-rw-r--r--  2.0 unx       60 b- defN 23-Jul-22 17:54 recompose/logging.py
+-rw-r--r--  2.0 unx        0 b- defN 23-Jul-22 17:54 recompose/py.typed
+-rw-r--r--  2.0 unx     1184 b- defN 23-Jul-22 17:54 recompose/transformer.py
+-rw-r--r--  2.0 unx      695 b- defN 23-Jul-22 17:54 recompose/transformers.py
+-rw-r--r--  2.0 unx      389 b- defN 23-Jul-22 17:54 recompose/types.py
+-rw-r--r--  2.0 unx     1174 b- defN 23-Jul-22 17:54 recompose/with_reader.py
+-rw-r--r--  2.0 unx      165 b- defN 23-Jul-22 17:54 recompose/cursor_classes/__init__.py
+-rw-r--r--  2.0 unx     1331 b- defN 23-Jul-22 17:54 recompose/cursor_classes/each_value.py
+-rw-r--r--  2.0 unx        0 b- defN 23-Jul-22 17:54 recompose/cursor_classes/py.typed
+-rw-r--r--  2.0 unx      392 b- defN 23-Jul-22 17:54 recompose/cursor_classes/this_value.py
+-rw-r--r--  2.0 unx      177 b- defN 23-Jul-22 17:54 recompose/transformer_classes/__init__.py
+-rw-r--r--  2.0 unx      309 b- defN 23-Jul-22 17:54 recompose/transformer_classes/list_to_object.py
+-rw-r--r--  2.0 unx      898 b- defN 23-Jul-22 17:54 recompose/transformer_classes/pass_through.py
+-rw-r--r--  2.0 unx        0 b- defN 23-Jul-22 17:54 recompose/transformer_classes/py.typed
+-rw-r--r--  2.0 unx      204 b- defN 23-Jul-22 17:54 recompose/with_readers/__init__.py
+-rw-r--r--  2.0 unx        0 b- defN 23-Jul-22 17:54 recompose/with_readers/py.typed
+-rw-r--r--  2.0 unx      568 b- defN 23-Jul-22 17:54 recompose/with_readers/with_cursor_schema.py
+-rw-r--r--  2.0 unx      471 b- defN 23-Jul-22 17:54 recompose/with_readers/with_path.py
+-rw-r--r--  2.0 unx     1073 b- defN 23-Jul-22 17:54 recompose-1.0.0b0.dist-info/LICENSE
+-rw-r--r--  2.0 unx     1057 b- defN 23-Jul-22 17:54 recompose-1.0.0b0.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 23-Jul-22 17:54 recompose-1.0.0b0.dist-info/WHEEL
+-rw-r--r--  2.0 unx       10 b- defN 23-Jul-22 17:54 recompose-1.0.0b0.dist-info/top_level.txt
+-rw-rw-r--  2.0 unx     2300 b- defN 23-Jul-22 17:54 recompose-1.0.0b0.dist-info/RECORD
+27 files, 15876 bytes uncompressed, 7043 bytes compressed:  55.6%
```

## zipnote {}

```diff
@@ -1,25 +1,82 @@
 Filename: recompose/VERSION
 Comment: 
 
 Filename: recompose/__init__.py
 Comment: 
 
+Filename: recompose/cursor.py
+Comment: 
+
+Filename: recompose/cursors.py
+Comment: 
+
+Filename: recompose/logging.py
+Comment: 
+
 Filename: recompose/py.typed
 Comment: 
 
-Filename: recompose-1.0.0a1.dist-info/LICENSE
+Filename: recompose/transformer.py
+Comment: 
+
+Filename: recompose/transformers.py
+Comment: 
+
+Filename: recompose/types.py
+Comment: 
+
+Filename: recompose/with_reader.py
+Comment: 
+
+Filename: recompose/cursor_classes/__init__.py
+Comment: 
+
+Filename: recompose/cursor_classes/each_value.py
+Comment: 
+
+Filename: recompose/cursor_classes/py.typed
+Comment: 
+
+Filename: recompose/cursor_classes/this_value.py
+Comment: 
+
+Filename: recompose/transformer_classes/__init__.py
+Comment: 
+
+Filename: recompose/transformer_classes/list_to_object.py
+Comment: 
+
+Filename: recompose/transformer_classes/pass_through.py
+Comment: 
+
+Filename: recompose/transformer_classes/py.typed
+Comment: 
+
+Filename: recompose/with_readers/__init__.py
+Comment: 
+
+Filename: recompose/with_readers/py.typed
+Comment: 
+
+Filename: recompose/with_readers/with_cursor_schema.py
+Comment: 
+
+Filename: recompose/with_readers/with_path.py
+Comment: 
+
+Filename: recompose-1.0.0b0.dist-info/LICENSE
 Comment: 
 
-Filename: recompose-1.0.0a1.dist-info/METADATA
+Filename: recompose-1.0.0b0.dist-info/METADATA
 Comment: 
 
-Filename: recompose-1.0.0a1.dist-info/WHEEL
+Filename: recompose-1.0.0b0.dist-info/WHEEL
 Comment: 
 
-Filename: recompose-1.0.0a1.dist-info/top_level.txt
+Filename: recompose-1.0.0b0.dist-info/top_level.txt
 Comment: 
 
-Filename: recompose-1.0.0a1.dist-info/RECORD
+Filename: recompose-1.0.0b0.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## recompose/VERSION

```diff
@@ -1 +1 @@
-1.0.0-alpha.1
+1.0.0-beta.0
```

## recompose/__init__.py

```diff
@@ -1,8 +1,40 @@
 """
 Recompose is a Python package for templated data recomposition.
 """
 
 from importlib.resources import open_text
 
+import recompose.cursor_classes
+import recompose.transformer_classes
+from recompose.cursors import make_cursor, register_cursor
+from recompose.exceptions import (
+    InvalidSchema,
+    NoCursorForCondition,
+    NotATransformerType,
+    RecomposeError,
+    UnsupportedVersion,
+)
+from recompose.transformer import Transformer
+from recompose.transformers import find_transformer, register_transformer
+
 with open_text(__package__, "VERSION") as t:
     __version__ = t.readline().strip()
+
+
+register_cursor(recompose.cursor_classes.EachValue)
+register_cursor(recompose.cursor_classes.ThisValue)
+
+register_transformer(recompose.transformer_classes.ListToObject)
+register_transformer(recompose.transformer_classes.Pass)
+
+
+__all__ = [
+    "InvalidSchema",
+    "NoCursorForCondition",
+    "NotATransformerType",
+    "RecomposeError",
+    "Transformer",
+    "UnsupportedVersion",
+    "make_cursor",
+    "find_transformer",
+]
```

## Comparing `recompose-1.0.0a1.dist-info/LICENSE` & `recompose-1.0.0b0.dist-info/LICENSE`

 * *Files identical despite different names*

## Comparing `recompose-1.0.0a1.dist-info/METADATA` & `recompose-1.0.0b0.dist-info/METADATA`

 * *Files 8% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 Metadata-Version: 2.1
 Name: recompose
-Version: 1.0.0a1
+Version: 1.0.0b0
 Summary: Templated data recomposition
 Home-page: https://github.com/cariad/recompose
 Author: Cariad Eccleston
 Author-email: cariad@cariad.earth
 License: MIT
-Classifier: Development Status :: 3 - Alpha
+Classifier: Development Status :: 4 - Beta
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Natural Language :: English
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3 :: Only
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Typing :: Typed
 Requires-Python: >=3.9
```

