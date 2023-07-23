# Comparing `tmp/pyarmor.cli.core.windows-3.2.9-cp39-none-any.whl.zip` & `tmp/pyarmor.cli.core.windows-4.3.dev1-cp39-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,11 +1,11 @@
-Zip file size: 1383252 bytes, number of entries: 9
--rw-r--r--  2.0 unx       22 b- defN 23-Jul-01 01:14 pyarmor/cli/core/windows/__init__.py
--rwxr-xr-x  2.0 unx   762894 b- defN 23-Jul-01 01:14 pyarmor/cli/core/windows/x86/pyarmor_runtime.pyd
--rwxr-xr-x  2.0 unx   865280 b- defN 23-Jul-01 01:14 pyarmor/cli/core/windows/x86/pytransform3.pyd
--rwxr-xr-x  2.0 unx   617472 b- defN 23-Jul-01 01:14 pyarmor/cli/core/windows/x86_64/pyarmor_runtime.pyd
--rwxr-xr-x  2.0 unx   724992 b- defN 23-Jul-01 01:14 pyarmor/cli/core/windows/x86_64/pytransform3.pyd
--rw-r--r--  2.0 unx      808 b- defN 23-Jul-01 01:14 pyarmor.cli.core.windows-3.2.9.dist-info/METADATA
--rw-r--r--  2.0 unx       93 b- defN 23-Jul-01 01:14 pyarmor.cli.core.windows-3.2.9.dist-info/WHEEL
--rw-r--r--  2.0 unx        8 b- defN 23-Jul-01 01:14 pyarmor.cli.core.windows-3.2.9.dist-info/top_level.txt
-?rw-rw-r--  2.0 unx      883 b- defN 23-Jul-01 01:14 pyarmor.cli.core.windows-3.2.9.dist-info/RECORD
-9 files, 2972452 bytes uncompressed, 1381698 bytes compressed:  53.5%
+Zip file size: 1383832 bytes, number of entries: 9
+-rw-r--r--  2.0 unx       25 b- defN 23-Jul-23 12:58 pyarmor/cli/core/windows/__init__.py
+-rwxr-xr-x  2.0 unx   762894 b- defN 23-Jul-23 12:58 pyarmor/cli/core/windows/x86/pyarmor_runtime.pyd
+-rwxr-xr-x  2.0 unx   865280 b- defN 23-Jul-23 12:58 pyarmor/cli/core/windows/x86/pytransform3.pyd
+-rwxr-xr-x  2.0 unx   617472 b- defN 23-Jul-23 12:58 pyarmor/cli/core/windows/x86_64/pyarmor_runtime.pyd
+-rwxr-xr-x  2.0 unx   725504 b- defN 23-Jul-23 12:58 pyarmor/cli/core/windows/x86_64/pytransform3.pyd
+-rw-r--r--  2.0 unx      811 b- defN 23-Jul-23 12:58 pyarmor.cli.core.windows-4.3.dev1.dist-info/METADATA
+-rw-r--r--  2.0 unx       93 b- defN 23-Jul-23 12:58 pyarmor.cli.core.windows-4.3.dev1.dist-info/WHEEL
+-rw-r--r--  2.0 unx        8 b- defN 23-Jul-23 12:58 pyarmor.cli.core.windows-4.3.dev1.dist-info/top_level.txt
+?rw-rw-r--  2.0 unx      895 b- defN 23-Jul-23 12:58 pyarmor.cli.core.windows-4.3.dev1.dist-info/RECORD
+9 files, 2972982 bytes uncompressed, 1382254 bytes compressed:  53.5%
```

## zipnote {}

```diff
@@ -9,20 +9,20 @@
 
 Filename: pyarmor/cli/core/windows/x86_64/pyarmor_runtime.pyd
 Comment: 
 
 Filename: pyarmor/cli/core/windows/x86_64/pytransform3.pyd
 Comment: 
 
-Filename: pyarmor.cli.core.windows-3.2.9.dist-info/METADATA
+Filename: pyarmor.cli.core.windows-4.3.dev1.dist-info/METADATA
 Comment: 
 
-Filename: pyarmor.cli.core.windows-3.2.9.dist-info/WHEEL
+Filename: pyarmor.cli.core.windows-4.3.dev1.dist-info/WHEEL
 Comment: 
 
-Filename: pyarmor.cli.core.windows-3.2.9.dist-info/top_level.txt
+Filename: pyarmor.cli.core.windows-4.3.dev1.dist-info/top_level.txt
 Comment: 
 
-Filename: pyarmor.cli.core.windows-3.2.9.dist-info/RECORD
+Filename: pyarmor.cli.core.windows-4.3.dev1.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## pyarmor/cli/core/windows/__init__.py

```diff
@@ -1 +1 @@
-__VERSION__ = '3.2.9'
+__VERSION__ = '4.3.dev1'
```

## Comparing `pyarmor.cli.core.windows-3.2.9.dist-info/METADATA` & `pyarmor.cli.core.windows-4.3.dev1.dist-info/METADATA`

 * *Files 14% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyarmor.cli.core.windows
-Version: 3.2.9
+Version: 4.3.dev1
 Summary: Provide pre-built extension modules `pytransform3` and `pyarmor_runtime` for Pyarmor
 Home-page: https://github.com/dashingsoft/pyarmor
 Author: Jondy Zhao
 Author-email: pyarmor@163.com
 License: Free To Use But Restricted
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
```

