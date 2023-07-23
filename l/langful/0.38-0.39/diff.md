# Comparing `tmp/langful-0.38-py3-none-any.whl.zip` & `tmp/langful-0.39-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,9 +1,9 @@
-Zip file size: 5620 bytes, number of entries: 7
+Zip file size: 5636 bytes, number of entries: 7
 -rw-rw-rw-  2.0 fat      166 b- defN 23-Jul-06 06:25 langful/__init__.py
--rw-rw-rw-  2.0 fat    10241 b- defN 23-Jul-21 02:54 langful/lang.py
--rw-rw-rw-  2.0 fat     1066 b- defN 23-Jul-21 03:18 langful-0.38.dist-info/LICENSE
--rw-rw-rw-  2.0 fat     3050 b- defN 23-Jul-21 03:18 langful-0.38.dist-info/METADATA
--rw-rw-rw-  2.0 fat       92 b- defN 23-Jul-21 03:18 langful-0.38.dist-info/WHEEL
--rw-rw-rw-  2.0 fat        8 b- defN 23-Jul-21 03:18 langful-0.38.dist-info/top_level.txt
--rw-rw-r--  2.0 fat      528 b- defN 23-Jul-21 03:18 langful-0.38.dist-info/RECORD
-7 files, 15151 bytes uncompressed, 4690 bytes compressed:  69.0%
+-rw-rw-rw-  2.0 fat    10313 b- defN 23-Jul-23 16:32 langful/lang.py
+-rw-rw-rw-  2.0 fat     1066 b- defN 23-Jul-23 16:50 langful-0.39.dist-info/LICENSE
+-rw-rw-rw-  2.0 fat     3050 b- defN 23-Jul-23 16:50 langful-0.39.dist-info/METADATA
+-rw-rw-rw-  2.0 fat       92 b- defN 23-Jul-23 16:50 langful-0.39.dist-info/WHEEL
+-rw-rw-rw-  2.0 fat        8 b- defN 23-Jul-23 16:50 langful-0.39.dist-info/top_level.txt
+-rw-rw-r--  2.0 fat      528 b- defN 23-Jul-23 16:50 langful-0.39.dist-info/RECORD
+7 files, 15223 bytes uncompressed, 4706 bytes compressed:  69.1%
```

## zipnote {}

```diff
@@ -1,22 +1,22 @@
 Filename: langful/__init__.py
 Comment: 
 
 Filename: langful/lang.py
 Comment: 
 
-Filename: langful-0.38.dist-info/LICENSE
+Filename: langful-0.39.dist-info/LICENSE
 Comment: 
 
-Filename: langful-0.38.dist-info/METADATA
+Filename: langful-0.39.dist-info/METADATA
 Comment: 
 
-Filename: langful-0.38.dist-info/WHEEL
+Filename: langful-0.39.dist-info/WHEEL
 Comment: 
 
-Filename: langful-0.38.dist-info/top_level.txt
+Filename: langful-0.39.dist-info/top_level.txt
 Comment: 
 
-Filename: langful-0.38.dist-info/RECORD
+Filename: langful-0.39.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## langful/lang.py

```diff
@@ -41,22 +41,23 @@
     else :
         return [ args ]
 
 def getdefaultlocale() -> str :
     """
     getdefaultlocale will deprecated so use this
     """
-    import locale
-    import sys
-    if sys.platform == "win32" :
+    from locale import getlocale
+    from sys import platform
+    if platform == "win32" :
         code = __import__( "_locale" )._getdefaultlocale()[ 0 ]
-        if code[ :2 ] == "0x" :
-            code = locale.windows_locale[ int( code , 0 ) ]
+        if code and code[ : 2 ] == "0x" :
+            from locale import windows_locale
+            code = windows_locale.get( int( code , 0 ) )
     else :
-        code = locale.getlocale()[ 0 ]
+        code = getlocale()[ 0 ]
     return code.replace( "-" , "_" ).lower()
 
 class lang :
     """
     # lang
     """
```

## Comparing `langful-0.38.dist-info/LICENSE` & `langful-0.39.dist-info/LICENSE`

 * *Files identical despite different names*

## Comparing `langful-0.38.dist-info/METADATA` & `langful-0.39.dist-info/METADATA`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: langful
-Version: 0.38
+Version: 0.39
 Summary: Help to localization
 Home-page: https://github.com/cueavy/langful
 Author: cueavyqwp
 Author-email: cueavyqwp@outlook.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

