# Comparing `tmp/tgpy-0.9.6.tar.gz` & `tmp/tgpy-0.9.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "tgpy-0.9.6.tar", max compression
+gzip compressed data, was "tgpy-0.9.7.tar", max compression
```

## Comparing `tgpy-0.9.6.tar` & `tgpy-0.9.7.tar`

### file list

```diff
@@ -1,34 +1,34 @@
--rw-r--r--   0        0        0     1070 2023-06-01 14:48:11.564344 tgpy-0.9.6/LICENSE
--rw-r--r--   0        0        0     3157 2023-06-01 14:48:11.564344 tgpy-0.9.6/README.md
--rw-r--r--   0        0        0     1282 2023-06-01 14:48:27.344173 tgpy-0.9.6/pyproject.toml
--rw-r--r--   0        0        0      478 2023-06-01 14:48:11.568344 tgpy-0.9.6/tgpy/__init__.py
--rw-r--r--   0        0        0       35 2023-06-01 14:48:11.568344 tgpy-0.9.6/tgpy/__main__.py
--rw-r--r--   0        0        0        0 2023-06-01 14:48:11.568344 tgpy-0.9.6/tgpy/_core/__init__.py
--rw-r--r--   0        0        0     1102 2023-06-01 14:48:11.568344 tgpy-0.9.6/tgpy/_core/eval_message.py
--rw-r--r--   0        0        0     2904 2023-06-01 14:48:11.568344 tgpy-0.9.6/tgpy/_core/message_design.py
--rw-r--r--   0        0        0     5442 2023-06-01 14:48:11.568344 tgpy-0.9.6/tgpy/_core/meval.py
--rw-r--r--   0        0        0      429 2023-06-01 14:48:11.568344 tgpy-0.9.6/tgpy/_core/utils.py
--rw-r--r--   0        0        0     3530 2023-06-01 14:48:11.568344 tgpy-0.9.6/tgpy/_handlers/__init__.py
--rw-r--r--   0        0        0     1192 2023-06-01 14:48:11.568344 tgpy-0.9.6/tgpy/api/__init__.py
--rw-r--r--   0        0        0     1525 2023-06-01 14:48:11.568344 tgpy-0.9.6/tgpy/api/config.py
--rw-r--r--   0        0        0      449 2023-06-01 14:48:11.568344 tgpy-0.9.6/tgpy/api/directories.py
--rw-r--r--   0        0        0     4135 2023-06-01 14:48:11.568344 tgpy-0.9.6/tgpy/api/parse_code.py
--rw-r--r--   0        0        0      686 2023-06-01 14:48:11.568344 tgpy-0.9.6/tgpy/api/parse_tgpy_message.py
--rw-r--r--   0        0        0     1829 2023-06-01 14:48:11.572344 tgpy-0.9.6/tgpy/api/tgpy_eval.py
--rw-r--r--   0        0        0     4516 2023-06-01 14:48:11.572344 tgpy-0.9.6/tgpy/api/transformers.py
--rw-r--r--   0        0        0     2556 2023-06-01 14:48:11.572344 tgpy-0.9.6/tgpy/api/utils.py
--rw-r--r--   0        0        0     1542 2023-06-01 14:48:11.572344 tgpy-0.9.6/tgpy/context.py
--rw-r--r--   0        0        0     5758 2023-06-01 14:48:11.572344 tgpy-0.9.6/tgpy/main.py
--rw-r--r--   0        0        0     5251 2023-06-01 14:48:11.572344 tgpy-0.9.6/tgpy/modules.py
--rw-r--r--   0        0        0     1776 2023-06-01 14:48:11.572344 tgpy-0.9.6/tgpy/reactions_fix.py
--rw-r--r--   0        0        0     1198 2023-06-01 14:48:11.572344 tgpy-0.9.6/tgpy/std/compat.py
--rw-r--r--   0        0        0      221 2023-06-01 14:48:11.572344 tgpy-0.9.6/tgpy/std/constants.py
--rw-r--r--   0        0        0     2618 2023-06-01 14:48:11.572344 tgpy-0.9.6/tgpy/std/module_manager.py
--rw-r--r--   0        0        0      364 2023-06-01 14:48:11.572344 tgpy-0.9.6/tgpy/std/ping.py
--rw-r--r--   0        0        0     1263 2023-06-01 14:48:11.572344 tgpy-0.9.6/tgpy/std/postfix_await.py
--rw-r--r--   0        0        0     2360 2023-06-01 14:48:11.572344 tgpy-0.9.6/tgpy/std/prevent_eval.py
--rw-r--r--   0        0        0      915 2023-06-01 14:48:11.572344 tgpy-0.9.6/tgpy/std/restart.py
--rw-r--r--   0        0        0     1273 2023-06-01 14:48:11.572344 tgpy-0.9.6/tgpy/std/update.py
--rw-r--r--   0        0        0     2509 2023-06-01 14:48:11.572344 tgpy-0.9.6/tgpy/utils.py
--rw-r--r--   0        0        0       62 2023-06-01 14:48:28.628143 tgpy-0.9.6/tgpy/version.py
--rw-r--r--   0        0        0     4082 1970-01-01 00:00:00.000000 tgpy-0.9.6/PKG-INFO
+-rw-r--r--   0        0        0     1070 2023-07-23 16:56:12.986341 tgpy-0.9.7/LICENSE
+-rw-r--r--   0        0        0     3157 2023-07-23 16:56:12.986341 tgpy-0.9.7/README.md
+-rw-r--r--   0        0        0     1282 2023-07-23 16:56:32.226642 tgpy-0.9.7/pyproject.toml
+-rw-r--r--   0        0        0      478 2023-07-23 16:56:12.990342 tgpy-0.9.7/tgpy/__init__.py
+-rw-r--r--   0        0        0       35 2023-07-23 16:56:12.990342 tgpy-0.9.7/tgpy/__main__.py
+-rw-r--r--   0        0        0        0 2023-07-23 16:56:12.990342 tgpy-0.9.7/tgpy/_core/__init__.py
+-rw-r--r--   0        0        0     1102 2023-07-23 16:56:12.990342 tgpy-0.9.7/tgpy/_core/eval_message.py
+-rw-r--r--   0        0        0     2904 2023-07-23 16:56:12.990342 tgpy-0.9.7/tgpy/_core/message_design.py
+-rw-r--r--   0        0        0     5442 2023-07-23 16:56:12.990342 tgpy-0.9.7/tgpy/_core/meval.py
+-rw-r--r--   0        0        0      429 2023-07-23 16:56:12.990342 tgpy-0.9.7/tgpy/_core/utils.py
+-rw-r--r--   0        0        0     3530 2023-07-23 16:56:12.990342 tgpy-0.9.7/tgpy/_handlers/__init__.py
+-rw-r--r--   0        0        0     1192 2023-07-23 16:56:12.990342 tgpy-0.9.7/tgpy/api/__init__.py
+-rw-r--r--   0        0        0     1525 2023-07-23 16:56:12.990342 tgpy-0.9.7/tgpy/api/config.py
+-rw-r--r--   0        0        0      449 2023-07-23 16:56:12.990342 tgpy-0.9.7/tgpy/api/directories.py
+-rw-r--r--   0        0        0     4135 2023-07-23 16:56:12.990342 tgpy-0.9.7/tgpy/api/parse_code.py
+-rw-r--r--   0        0        0      686 2023-07-23 16:56:12.990342 tgpy-0.9.7/tgpy/api/parse_tgpy_message.py
+-rw-r--r--   0        0        0     1829 2023-07-23 16:56:12.990342 tgpy-0.9.7/tgpy/api/tgpy_eval.py
+-rw-r--r--   0        0        0     4516 2023-07-23 16:56:12.990342 tgpy-0.9.7/tgpy/api/transformers.py
+-rw-r--r--   0        0        0     2556 2023-07-23 16:56:12.990342 tgpy-0.9.7/tgpy/api/utils.py
+-rw-r--r--   0        0        0     1542 2023-07-23 16:56:12.990342 tgpy-0.9.7/tgpy/context.py
+-rw-r--r--   0        0        0     5824 2023-07-23 16:56:12.990342 tgpy-0.9.7/tgpy/main.py
+-rw-r--r--   0        0        0     5251 2023-07-23 16:56:12.990342 tgpy-0.9.7/tgpy/modules.py
+-rw-r--r--   0        0        0     1776 2023-07-23 16:56:12.990342 tgpy-0.9.7/tgpy/reactions_fix.py
+-rw-r--r--   0        0        0     1198 2023-07-23 16:56:12.990342 tgpy-0.9.7/tgpy/std/compat.py
+-rw-r--r--   0        0        0      221 2023-07-23 16:56:12.990342 tgpy-0.9.7/tgpy/std/constants.py
+-rw-r--r--   0        0        0     2618 2023-07-23 16:56:12.990342 tgpy-0.9.7/tgpy/std/module_manager.py
+-rw-r--r--   0        0        0      364 2023-07-23 16:56:12.990342 tgpy-0.9.7/tgpy/std/ping.py
+-rw-r--r--   0        0        0     1263 2023-07-23 16:56:12.990342 tgpy-0.9.7/tgpy/std/postfix_await.py
+-rw-r--r--   0        0        0     2360 2023-07-23 16:56:12.990342 tgpy-0.9.7/tgpy/std/prevent_eval.py
+-rw-r--r--   0        0        0      915 2023-07-23 16:56:12.990342 tgpy-0.9.7/tgpy/std/restart.py
+-rw-r--r--   0        0        0     1273 2023-07-23 16:56:12.990342 tgpy-0.9.7/tgpy/std/update.py
+-rw-r--r--   0        0        0     2509 2023-07-23 16:56:12.990342 tgpy-0.9.7/tgpy/utils.py
+-rw-r--r--   0        0        0       62 2023-07-23 16:56:33.714665 tgpy-0.9.7/tgpy/version.py
+-rw-r--r--   0        0        0     4082 1970-01-01 00:00:00.000000 tgpy-0.9.7/PKG-INFO
```

### Comparing `tgpy-0.9.6/LICENSE` & `tgpy-0.9.7/LICENSE`

 * *Files identical despite different names*

### Comparing `tgpy-0.9.6/README.md` & `tgpy-0.9.7/README.md`

 * *Files identical despite different names*

### Comparing `tgpy-0.9.6/pyproject.toml` & `tgpy-0.9.7/pyproject.toml`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "tgpy"
-version = "0.9.6"
+version = "0.9.7"
 description = "Run Python code right in your Telegram messages"
 authors = ["tmat <a@tmat.me>", "vanutp <hello@vanutp.dev>", "ntonee <a12286@yandex.com>"]
 license = "MIT"
 documentation = "https://tgpy.tmat.me/"
 repository = "https://github.com/tm-a-t/TGPy/"
 readme = "README.md"
 classifiers = [
```

### Comparing `tgpy-0.9.6/tgpy/_core/eval_message.py` & `tgpy-0.9.7/tgpy/_core/eval_message.py`

 * *Files identical despite different names*

### Comparing `tgpy-0.9.6/tgpy/_core/message_design.py` & `tgpy-0.9.7/tgpy/_core/message_design.py`

 * *Files identical despite different names*

### Comparing `tgpy-0.9.6/tgpy/_core/meval.py` & `tgpy-0.9.7/tgpy/_core/meval.py`

 * *Files identical despite different names*

### Comparing `tgpy-0.9.6/tgpy/_handlers/__init__.py` & `tgpy-0.9.7/tgpy/_handlers/__init__.py`

 * *Files identical despite different names*

### Comparing `tgpy-0.9.6/tgpy/api/__init__.py` & `tgpy-0.9.7/tgpy/api/__init__.py`

 * *Files identical despite different names*

### Comparing `tgpy-0.9.6/tgpy/api/config.py` & `tgpy-0.9.7/tgpy/api/config.py`

 * *Files identical despite different names*

### Comparing `tgpy-0.9.6/tgpy/api/parse_code.py` & `tgpy-0.9.7/tgpy/api/parse_code.py`

 * *Files identical despite different names*

### Comparing `tgpy-0.9.6/tgpy/api/parse_tgpy_message.py` & `tgpy-0.9.7/tgpy/api/parse_tgpy_message.py`

 * *Files identical despite different names*

### Comparing `tgpy-0.9.6/tgpy/api/tgpy_eval.py` & `tgpy-0.9.7/tgpy/api/tgpy_eval.py`

 * *Files identical despite different names*

### Comparing `tgpy-0.9.6/tgpy/api/transformers.py` & `tgpy-0.9.7/tgpy/api/transformers.py`

 * *Files identical despite different names*

### Comparing `tgpy-0.9.6/tgpy/api/utils.py` & `tgpy-0.9.7/tgpy/api/utils.py`

 * *Files identical despite different names*

### Comparing `tgpy-0.9.6/tgpy/context.py` & `tgpy-0.9.7/tgpy/context.py`

 * *Files identical despite different names*

### Comparing `tgpy-0.9.6/tgpy/main.py` & `tgpy-0.9.7/tgpy/main.py`

 * *Files 3% similar despite different names*

```diff
@@ -74,40 +74,42 @@
         password=functools.partial(
             ainput, '| Please enter your 2FA password: ', password=True
         ),
     )
 
 
 async def initial_setup():
-    console.print('[bold on bright_cyan] Welcome to TGPy ')
+    console.print('[bold #ffffff on #16a085] Welcome to TGPy ')
     console.print('Starting setup...')
     console.print()
-    console.print('[bold black on white] Step 1 of 2 ')
+    console.print('[bold #7f8c8d on #ffffff] Step 1 of 2 ')
     console.print(
         '│ TGPy uses Telegram API, so you\'ll need to register your Telegram app.\n'
-        '│  [cyan]1.[/] Go to https://my.telegram.org\n'
-        '│  [cyan]2.[/] Login with your Telegram account\n'
-        '│  [cyan]3.[/] Go to "API development tools"\n'
-        '│  [cyan]4.[/] Create your app. Choose any app title and short_title. You can leave other fields empty.\n'
+        '│  [#1abc9c]1.[/] Go to https://my.telegram.org\n'
+        '│  [#1abc9c]2.[/] Login with your Telegram account\n'
+        '│  [#1abc9c]3.[/] Go to "API development tools"\n'
+        '│  [#1abc9c]4.[/] Create your app. Choose any app title and short_title. You can leave other fields empty.\n'
         '│ You will get api_id and api_hash.'
     )
     success = False
     while not success:
         config.set('core.api_id', int(await ainput('│ Please enter api_id: ')))
         config.set('core.api_hash', await ainput('│ ...and api_hash: '))
         try:
             app.client = create_client()
             console.print()
-            console.print('[bold black on white] Step 2 of 2 ')
+            console.print('[bold #7f8c8d on #ffffff] Step 2 of 2 ')
             console.print('│ Now login to Telegram.')
             await app.client.connect()
             await start_client()
             success = True
         except (errors.ApiIdInvalidError, errors.ApiIdPublishedFloodError, ValueError):
-            console.print('│ [bold on red]Incorrect api_id/api_hash, try again')
+            console.print(
+                '│ [bold #ffffff on #ed1515]Incorrect api_id/api_hash, try again'
+            )
         finally:
             if app.client:
                 await app.client.disconnect()
                 del app.client
     console.print('│ Login successful!')
```

### Comparing `tgpy-0.9.6/tgpy/modules.py` & `tgpy-0.9.7/tgpy/modules.py`

 * *Files identical despite different names*

### Comparing `tgpy-0.9.6/tgpy/reactions_fix.py` & `tgpy-0.9.7/tgpy/reactions_fix.py`

 * *Files identical despite different names*

### Comparing `tgpy-0.9.6/tgpy/std/compat.py` & `tgpy-0.9.7/tgpy/std/compat.py`

 * *Files identical despite different names*

### Comparing `tgpy-0.9.6/tgpy/std/module_manager.py` & `tgpy-0.9.7/tgpy/std/module_manager.py`

 * *Files identical despite different names*

### Comparing `tgpy-0.9.6/tgpy/std/postfix_await.py` & `tgpy-0.9.7/tgpy/std/postfix_await.py`

 * *Files identical despite different names*

### Comparing `tgpy-0.9.6/tgpy/std/prevent_eval.py` & `tgpy-0.9.7/tgpy/std/prevent_eval.py`

 * *Files identical despite different names*

### Comparing `tgpy-0.9.6/tgpy/std/restart.py` & `tgpy-0.9.7/tgpy/std/restart.py`

 * *Files identical despite different names*

### Comparing `tgpy-0.9.6/tgpy/std/update.py` & `tgpy-0.9.7/tgpy/std/update.py`

 * *Files identical despite different names*

### Comparing `tgpy-0.9.6/tgpy/utils.py` & `tgpy-0.9.7/tgpy/utils.py`

 * *Files identical despite different names*

### Comparing `tgpy-0.9.6/PKG-INFO` & `tgpy-0.9.7/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: tgpy
-Version: 0.9.6
+Version: 0.9.7
 Summary: Run Python code right in your Telegram messages
 Home-page: https://github.com/tm-a-t/TGPy/
 License: MIT
 Author: tmat
 Author-email: a@tmat.me
 Requires-Python: >=3.9,<4.0
 Classifier: License :: OSI Approved :: MIT License
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: tgpy Version: 0.9.6 Summary: Run Python code right
+Metadata-Version: 2.1 Name: tgpy Version: 0.9.7 Summary: Run Python code right
 in your Telegram messages Home-page: https://github.com/tm-a-t/TGPy/ License:
 MIT Author: tmat Author-email: a@tmat.me Requires-Python: >=3.9,<4.0
 Classifier: License :: OSI Approved :: MIT License Classifier: Operating System
 :: OS Independent Classifier: Programming Language :: Python :: 3 Classifier:
 Programming Language :: Python :: 3.9 Classifier: Programming Language ::
 Python :: 3.10 Classifier: Programming Language :: Python :: 3.11 Requires-
 Dist: PyYAML (>=6.0,<7.0) Requires-Dist: aiorun (>=2022.4.1,<2023.0.0)
```

