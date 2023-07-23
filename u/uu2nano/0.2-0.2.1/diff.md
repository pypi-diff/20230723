# Comparing `tmp/uu2nano-0.2-py3-none-any.whl.zip` & `tmp/uu2nano-0.2.1-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,7 +1,7 @@
-Zip file size: 2656 bytes, number of entries: 5
--rw-r--r--  2.0 unx     1065 b- defN 23-Jul-23 16:29 uu2nano.py
--rw-r--r--  2.0 unx     2082 b- defN 23-Jul-23 16:32 uu2nano-0.2.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 16:32 uu2nano-0.2.dist-info/WHEEL
--rw-r--r--  2.0 unx        8 b- defN 23-Jul-23 16:32 uu2nano-0.2.dist-info/top_level.txt
--rw-rw-r--  2.0 unx      356 b- defN 23-Jul-23 16:32 uu2nano-0.2.dist-info/RECORD
-5 files, 3603 bytes uncompressed, 1994 bytes compressed:  44.7%
+Zip file size: 2674 bytes, number of entries: 5
+-rw-r--r--  2.0 unx     1067 b- defN 23-Jul-23 16:33 uu2nano.py
+-rw-r--r--  2.0 unx     2084 b- defN 23-Jul-23 16:34 uu2nano-0.2.1.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 16:34 uu2nano-0.2.1.dist-info/WHEEL
+-rw-r--r--  2.0 unx        8 b- defN 23-Jul-23 16:34 uu2nano-0.2.1.dist-info/top_level.txt
+-rw-rw-r--  2.0 unx      364 b- defN 23-Jul-23 16:34 uu2nano-0.2.1.dist-info/RECORD
+5 files, 3615 bytes uncompressed, 1996 bytes compressed:  44.8%
```

## zipnote {}

```diff
@@ -1,16 +1,16 @@
 Filename: uu2nano.py
 Comment: 
 
-Filename: uu2nano-0.2.dist-info/METADATA
+Filename: uu2nano-0.2.1.dist-info/METADATA
 Comment: 
 
-Filename: uu2nano-0.2.dist-info/WHEEL
+Filename: uu2nano-0.2.1.dist-info/WHEEL
 Comment: 
 
-Filename: uu2nano-0.2.dist-info/top_level.txt
+Filename: uu2nano-0.2.1.dist-info/top_level.txt
 Comment: 
 
-Filename: uu2nano-0.2.dist-info/RECORD
+Filename: uu2nano-0.2.1.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## uu2nano.py

```diff
@@ -1,11 +1,11 @@
 import uuid
 
 
-__version__ = '0.2'
+__version__ = '0.2.1'
 
 
 def _make_alpharev(alphabet):
     alpharev = bytearray(max(c for c in alphabet) + 1)
     for i, c in enumerate(alphabet):
         alpharev[c] = i
     return bytes(alpharev)
```

## Comparing `uu2nano-0.2.dist-info/METADATA` & `uu2nano-0.2.1.dist-info/METADATA`

 * *Files 9% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: uu2nano
-Version: 0.2
+Version: 0.2.1
 Summary: Conversion tool from UUID to nanoid and vice versa
 Author-email: Aleksandr Karpinskii <homm86@gmail.com>
 Project-URL: Repository, https://github.com/homm/uu2nano
 Keywords: uuid,nanoid
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 
@@ -27,15 +27,15 @@
 
 For example: `492b6acb-05c7-4914-b139-253070a085e9`
 
 Nanoid is encoded using 64 URL-safe symbols (`A-Za-z0-9_-`) which makes possible
 to store 6 bits of information per symbol. To store 126 UUID bits, only 
 126 / 6 = 21 characters are used in the string representation.
 
-For example: `Dl6CK-h7T2hfg5lKMEHgg`
+For example: `ggHEMKl5gfh2T7h-KC6lD`
 
 
 ## Usage
 
 Convert one to another:
 
 ```python
```

