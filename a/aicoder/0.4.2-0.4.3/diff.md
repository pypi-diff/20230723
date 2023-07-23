# Comparing `tmp/aicoder-0.4.2-py3-none-any.whl.zip` & `tmp/aicoder-0.4.3-py3-none-any.whl.zip`

## zipinfo {}

```diff
@@ -1,14 +1,14 @@
-Zip file size: 22336 bytes, number of entries: 12
--rw-r--r--  2.0 unx    10950 b- defN 23-Jul-20 09:01 aicoder/AICoder.py
+Zip file size: 22337 bytes, number of entries: 12
+-rw-r--r--  2.0 unx    10951 b- defN 23-Jul-23 15:07 aicoder/AICoder.py
 -rw-r--r--  2.0 unx     9535 b- defN 23-Jul-23 15:06 aicoder/AICoderFull.py
 -rw-r--r--  2.0 unx     7159 b- defN 23-Jul-23 15:06 aicoder/AICoderPartial.py
 -rw-r--r--  2.0 unx     3961 b- defN 23-Jul-23 15:01 aicoder/AICoderPrompts.py
 -rw-r--r--  2.0 unx        0 b- defN 23-Jun-29 11:14 aicoder/__init__.py
 -rw-r--r--  2.0 unx    16637 b- defN 23-Jul-23 15:06 aicoder/main.py
--rw-r--r--  2.0 unx    18809 b- defN 23-Jul-23 15:06 aicoder-0.4.2.dist-info/LICENSE
--rw-r--r--  2.0 unx      473 b- defN 23-Jul-23 15:06 aicoder-0.4.2.dist-info/METADATA
--rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 15:06 aicoder-0.4.2.dist-info/WHEEL
--rw-r--r--  2.0 unx       46 b- defN 23-Jul-23 15:06 aicoder-0.4.2.dist-info/entry_points.txt
--rw-r--r--  2.0 unx        8 b- defN 23-Jul-23 15:06 aicoder-0.4.2.dist-info/top_level.txt
--rw-rw-r--  2.0 unx      945 b- defN 23-Jul-23 15:06 aicoder-0.4.2.dist-info/RECORD
-12 files, 68615 bytes uncompressed, 20756 bytes compressed:  69.8%
+-rw-r--r--  2.0 unx    18809 b- defN 23-Jul-23 15:07 aicoder-0.4.3.dist-info/LICENSE
+-rw-r--r--  2.0 unx      473 b- defN 23-Jul-23 15:07 aicoder-0.4.3.dist-info/METADATA
+-rw-r--r--  2.0 unx       92 b- defN 23-Jul-23 15:07 aicoder-0.4.3.dist-info/WHEEL
+-rw-r--r--  2.0 unx       46 b- defN 23-Jul-23 15:07 aicoder-0.4.3.dist-info/entry_points.txt
+-rw-r--r--  2.0 unx        8 b- defN 23-Jul-23 15:07 aicoder-0.4.3.dist-info/top_level.txt
+-rw-rw-r--  2.0 unx      945 b- defN 23-Jul-23 15:07 aicoder-0.4.3.dist-info/RECORD
+12 files, 68616 bytes uncompressed, 20757 bytes compressed:  69.7%
```

## zipnote {}

```diff
@@ -12,26 +12,26 @@
 
 Filename: aicoder/__init__.py
 Comment: 
 
 Filename: aicoder/main.py
 Comment: 
 
-Filename: aicoder-0.4.2.dist-info/LICENSE
+Filename: aicoder-0.4.3.dist-info/LICENSE
 Comment: 
 
-Filename: aicoder-0.4.2.dist-info/METADATA
+Filename: aicoder-0.4.3.dist-info/METADATA
 Comment: 
 
-Filename: aicoder-0.4.2.dist-info/WHEEL
+Filename: aicoder-0.4.3.dist-info/WHEEL
 Comment: 
 
-Filename: aicoder-0.4.2.dist-info/entry_points.txt
+Filename: aicoder-0.4.3.dist-info/entry_points.txt
 Comment: 
 
-Filename: aicoder-0.4.2.dist-info/top_level.txt
+Filename: aicoder-0.4.3.dist-info/top_level.txt
 Comment: 
 
-Filename: aicoder-0.4.2.dist-info/RECORD
+Filename: aicoder-0.4.3.dist-info/RECORD
 Comment: 
 
 Zip file comment:
```

## aicoder/AICoder.py

```diff
@@ -2,15 +2,15 @@
 import colorlog
 import openai
 import json
 import os
 import re
 import subprocess
 from threading import Lock
-from AICoderPrompts import PERSONALITY, PROGRAM_TO_GENERATE, FINAL_CLARIFICATIONS, ERROR_FIX, GET_ERRORS_JSON, COMPILATION_COMMAND
+from .AICoderPrompts import PERSONALITY, PROGRAM_TO_GENERATE, FINAL_CLARIFICATIONS, ERROR_FIX, GET_ERRORS_JSON, COMPILATION_COMMAND
 
 handler = colorlog.StreamHandler()
 handler.setFormatter(colorlog.ColoredFormatter('%(log_color)s%(levelname)s:%(message)s'))
 
 logger = colorlog.getLogger('file_generator')
 if not logger.hasHandlers():
     logger.addHandler(handler)
```

## Comparing `aicoder-0.4.2.dist-info/LICENSE` & `aicoder-0.4.3.dist-info/LICENSE`

 * *Files identical despite different names*

