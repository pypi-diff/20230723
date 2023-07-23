# Comparing `tmp/rubpy-6.3.1.tar.gz` & `tmp/rubpy-6.3.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "rubpy-6.3.1.tar", last modified: Thu Jul 20 09:51:42 2023, max compression
+gzip compressed data, was "rubpy-6.3.2.tar", last modified: Sun Jul 23 18:20:35 2023, max compression
```

## Comparing `rubpy-6.3.1.tar` & `rubpy-6.3.2.tar`

### file list

```diff
@@ -1,38 +1,38 @@
-drwxrwxrwx   0        0        0        0 2023-07-20 09:51:42.118984 rubpy-6.3.1/
--rw-rw-rw-   0        0        0     3378 2023-07-20 09:51:42.118984 rubpy-6.3.1/PKG-INFO
--rw-rw-rw-   0        0        0     2238 2023-04-26 17:35:11.000000 rubpy-6.3.1/README.md
-drwxrwxrwx   0        0        0        0 2023-07-20 09:51:42.024793 rubpy-6.3.1/rubpy/
--rw-rw-rw-   0        0        0      240 2023-07-20 09:50:59.000000 rubpy-6.3.1/rubpy/__init__.py
--rw-rw-rw-   0        0        0    44693 2023-07-19 15:51:55.000000 rubpy-6.3.1/rubpy/client.py
-drwxrwxrwx   0        0        0        0 2023-07-20 09:51:42.056162 rubpy-6.3.1/rubpy/crypto/
--rw-rw-rw-   0        0        0       26 2022-09-12 11:03:20.000000 rubpy-6.3.1/rubpy/crypto/__init__.py
--rw-rw-rw-   0        0        0     3288 2023-07-19 15:43:06.000000 rubpy-6.3.1/rubpy/crypto/crypto.py
-drwxrwxrwx   0        0        0        0 2023-07-20 09:51:42.084547 rubpy-6.3.1/rubpy/gadgets/
--rw-rw-rw-   0        0        0      106 2022-09-12 11:03:20.000000 rubpy-6.3.1/rubpy/gadgets/__init__.py
--rw-rw-rw-   0        0        0      892 2023-06-14 19:16:37.000000 rubpy-6.3.1/rubpy/gadgets/classino.py
--rw-rw-rw-   0        0        0     2118 2023-04-26 18:12:01.000000 rubpy-6.3.1/rubpy/gadgets/exceptions.py
--rw-rw-rw-   0        0        0    27137 2023-06-15 19:36:00.000000 rubpy-6.3.1/rubpy/gadgets/grouping.py
--rw-rw-rw-   0        0        0    14188 2023-04-26 17:30:17.000000 rubpy-6.3.1/rubpy/gadgets/methods.py
--rw-rw-rw-   0        0        0     6772 2023-06-29 12:36:38.000000 rubpy-6.3.1/rubpy/gadgets/thumbnail.py
-drwxrwxrwx   0        0        0        0 2023-07-20 09:51:42.094680 rubpy-6.3.1/rubpy/network/
--rw-rw-rw-   0        0        0       64 2022-09-12 11:03:20.000000 rubpy-6.3.1/rubpy/network/__init__.py
--rw-rw-rw-   0        0        0    12184 2023-07-20 09:50:47.000000 rubpy-6.3.1/rubpy/network/connection.py
--rw-rw-rw-   0        0        0    14807 2022-09-12 11:03:20.000000 rubpy-6.3.1/rubpy/network/proxies.py
-drwxrwxrwx   0        0        0        0 2023-07-20 09:51:42.104908 rubpy-6.3.1/rubpy/sessions/
--rw-rw-rw-   0        0        0       82 2022-09-12 11:03:20.000000 rubpy-6.3.1/rubpy/sessions/__init__.py
--rw-rw-rw-   0        0        0     2295 2023-06-14 11:13:33.000000 rubpy-6.3.1/rubpy/sessions/sqliteSession.py
--rw-rw-rw-   0        0        0     1223 2022-09-12 11:03:20.000000 rubpy-6.3.1/rubpy/sessions/stringSession.py
-drwxrwxrwx   0        0        0        0 2023-07-20 09:51:42.114796 rubpy-6.3.1/rubpy/structs/
--rw-rw-rw-   0        0        0       99 2022-09-12 11:03:20.000000 rubpy-6.3.1/rubpy/structs/__init__.py
--rw-rw-rw-   0        0        0     1985 2022-09-12 11:03:20.000000 rubpy-6.3.1/rubpy/structs/handlers.py
--rw-rw-rw-   0        0        0     4585 2022-09-12 11:03:20.000000 rubpy-6.3.1/rubpy/structs/models.py
--rw-rw-rw-   0        0        0      702 2022-09-12 11:03:20.000000 rubpy-6.3.1/rubpy/structs/results.py
--rw-rw-rw-   0        0        0    15140 2023-04-23 17:55:22.000000 rubpy-6.3.1/rubpy/structs/struct.py
-drwxrwxrwx   0        0        0        0 2023-07-20 09:51:42.056162 rubpy-6.3.1/rubpy.egg-info/
--rw-rw-rw-   0        0        0     3378 2023-07-20 09:51:41.000000 rubpy-6.3.1/rubpy.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      697 2023-07-20 09:51:41.000000 rubpy-6.3.1/rubpy.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-20 09:51:41.000000 rubpy-6.3.1/rubpy.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       61 2023-07-20 09:51:41.000000 rubpy-6.3.1/rubpy.egg-info/requires.txt
--rw-rw-rw-   0        0        0        6 2023-07-20 09:51:41.000000 rubpy-6.3.1/rubpy.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-20 09:51:42.118984 rubpy-6.3.1/setup.cfg
--rw-rw-rw-   0        0        0     1547 2023-07-20 09:51:21.000000 rubpy-6.3.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 18:20:35.926236 rubpy-6.3.2/
+-rw-rw-rw-   0        0        0     3378 2023-07-23 18:20:35.926236 rubpy-6.3.2/PKG-INFO
+-rw-rw-rw-   0        0        0     2238 2023-04-26 17:35:11.000000 rubpy-6.3.2/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 18:20:35.875981 rubpy-6.3.2/rubpy/
+-rw-rw-rw-   0        0        0      240 2023-07-23 18:19:36.000000 rubpy-6.3.2/rubpy/__init__.py
+-rw-rw-rw-   0        0        0    43761 2023-07-23 18:19:04.000000 rubpy-6.3.2/rubpy/client.py
+drwxrwxrwx   0        0        0        0 2023-07-23 18:20:35.905907 rubpy-6.3.2/rubpy/crypto/
+-rw-rw-rw-   0        0        0       26 2022-09-12 11:03:20.000000 rubpy-6.3.2/rubpy/crypto/__init__.py
+-rw-rw-rw-   0        0        0     3288 2023-07-19 15:43:06.000000 rubpy-6.3.2/rubpy/crypto/crypto.py
+drwxrwxrwx   0        0        0        0 2023-07-23 18:20:35.919729 rubpy-6.3.2/rubpy/gadgets/
+-rw-rw-rw-   0        0        0      106 2022-09-12 11:03:20.000000 rubpy-6.3.2/rubpy/gadgets/__init__.py
+-rw-rw-rw-   0        0        0      892 2023-06-14 19:16:37.000000 rubpy-6.3.2/rubpy/gadgets/classino.py
+-rw-rw-rw-   0        0        0     2118 2023-04-26 18:12:01.000000 rubpy-6.3.2/rubpy/gadgets/exceptions.py
+-rw-rw-rw-   0        0        0    27137 2023-06-15 19:36:00.000000 rubpy-6.3.2/rubpy/gadgets/grouping.py
+-rw-rw-rw-   0        0        0    14188 2023-04-26 17:30:17.000000 rubpy-6.3.2/rubpy/gadgets/methods.py
+-rw-rw-rw-   0        0        0     6772 2023-06-29 12:36:38.000000 rubpy-6.3.2/rubpy/gadgets/thumbnail.py
+drwxrwxrwx   0        0        0        0 2023-07-23 18:20:35.926236 rubpy-6.3.2/rubpy/network/
+-rw-rw-rw-   0        0        0       64 2022-09-12 11:03:20.000000 rubpy-6.3.2/rubpy/network/__init__.py
+-rw-rw-rw-   0        0        0    12184 2023-07-20 09:50:47.000000 rubpy-6.3.2/rubpy/network/connection.py
+-rw-rw-rw-   0        0        0    14807 2022-09-12 11:03:20.000000 rubpy-6.3.2/rubpy/network/proxies.py
+drwxrwxrwx   0        0        0        0 2023-07-23 18:20:35.926236 rubpy-6.3.2/rubpy/sessions/
+-rw-rw-rw-   0        0        0       82 2022-09-12 11:03:20.000000 rubpy-6.3.2/rubpy/sessions/__init__.py
+-rw-rw-rw-   0        0        0     2295 2023-06-14 11:13:33.000000 rubpy-6.3.2/rubpy/sessions/sqliteSession.py
+-rw-rw-rw-   0        0        0     1223 2022-09-12 11:03:20.000000 rubpy-6.3.2/rubpy/sessions/stringSession.py
+drwxrwxrwx   0        0        0        0 2023-07-23 18:20:35.926236 rubpy-6.3.2/rubpy/structs/
+-rw-rw-rw-   0        0        0       99 2022-09-12 11:03:20.000000 rubpy-6.3.2/rubpy/structs/__init__.py
+-rw-rw-rw-   0        0        0     1985 2022-09-12 11:03:20.000000 rubpy-6.3.2/rubpy/structs/handlers.py
+-rw-rw-rw-   0        0        0     4585 2022-09-12 11:03:20.000000 rubpy-6.3.2/rubpy/structs/models.py
+-rw-rw-rw-   0        0        0      702 2022-09-12 11:03:20.000000 rubpy-6.3.2/rubpy/structs/results.py
+-rw-rw-rw-   0        0        0    15140 2023-04-23 17:55:22.000000 rubpy-6.3.2/rubpy/structs/struct.py
+drwxrwxrwx   0        0        0        0 2023-07-23 18:20:35.905907 rubpy-6.3.2/rubpy.egg-info/
+-rw-rw-rw-   0        0        0     3378 2023-07-23 18:20:35.000000 rubpy-6.3.2/rubpy.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      697 2023-07-23 18:20:35.000000 rubpy-6.3.2/rubpy.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 18:20:35.000000 rubpy-6.3.2/rubpy.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       69 2023-07-23 18:20:35.000000 rubpy-6.3.2/rubpy.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        6 2023-07-23 18:20:35.000000 rubpy-6.3.2/rubpy.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 18:20:35.926236 rubpy-6.3.2/setup.cfg
+-rw-rw-rw-   0        0        0     1558 2023-07-23 18:20:09.000000 rubpy-6.3.2/setup.py
```

### Comparing `rubpy-6.3.1/PKG-INFO` & `rubpy-6.3.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: rubpy
-Version: 6.3.1
+Version: 6.3.2
 Summary: This is an unofficial library and fastest library for deploying robots on Rubika accounts.
 Home-page: https://github.com/shayanheidari01/rubika
 Author: Shayan Heidari
 Author-email: contact@shayanheidari.info
 Keywords: rubika,rubpy,chat,bot,robot,asyncio
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: rubpy Version: 6.3.1 Summary: This is an unofficial
+Metadata-Version: 2.1 Name: rubpy Version: 6.3.2 Summary: This is an unofficial
 library and fastest library for deploying robots on Rubika accounts. Home-page:
 https://github.com/shayanheidari01/rubika Author: Shayan Heidari Author-email:
 contact@shayanheidari.info Keywords: rubika,rubpy,chat,bot,robot,asyncio
 Classifier: Programming Language :: Python :: 3.7 Classifier: Programming
 Language :: Python :: 3.8 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10 Classifier: Programming
 Language :: Python :: 3.11 Classifier: Programming Language :: Python :: 3.12
```

### Comparing `rubpy-6.3.1/README.md` & `rubpy-6.3.2/README.md`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.1/rubpy/client.py` & `rubpy-6.3.2/rubpy/client.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,26 +1,20 @@
-import os
-#import io
-import aiofiles
-import asyncio
-#import asyncio
-import logging
-from .crypto import Crypto
-from .structs import Struct
-from Crypto.PublicKey import RSA
-from . import __name__ as logger_name
-from .network import Connection, Proxies
 from .gadgets import exceptions, methods, thumbnail
 from .sessions import StringSession, SQLiteSession
-try:
-    import cv2
-    import numpy
-except ImportError:
-    cv2 = None
-    numpy = None
+from .network import Connection, Proxies
+from . import __name__ as logger_name
+from mutagen.mp3 import MP3
+from .structs import Struct
+from aiofiles import aiopen
+from .crypto import Crypto
+from io import BytesIO
+from re import compile
+import logging
+import os
+
 
 class Client:
     configuire = {
         'package': 'web.rubika.ir',
         'platform': 'Web',
         'app_name': 'Main',
         'user_agent': ('Mozilla/5.0 (Windows NT 10.0; Win64; x64) '
@@ -234,24 +228,27 @@
 
     async def get_me(self, *args, **kwargs):
         return await self(methods.users.GetUserInfo(self._guid))
 
     async def upload(self, file, *args, **kwargs):
         return await self._connection.upload_file(file=file, *args, **kwargs)
 
-    async def download_file_inline(self, file_inline, file: str = None, *args, **kwargs):
+    async def download_file_inline(self, file_inline, save_as: str = None, chunk_size: int = 131072, callback=None, *args, **kwargs):
         result = await self._connection.download(
             file_inline.dc_id,
             file_inline.file_id,
-            file_inline.access_hash_rec)
-
-        if isinstance(file, str):
-            with open(file, 'wb+') as _file:
-                _file.write(result)
-                return file
+            file_inline.access_hash_rec,
+            file_inline.size,
+            chunk=chunk_size,
+            callback=callback)
+
+        if isinstance(save_as, str):
+            async with aiopen(save_as, 'wb+') as _file:
+                await _file.write(result)
+                return save_as
 
         return result
 
 # ---------------- Users Methods ----------------
 
     async def get_user_info(self, user_guid: str):
         return await self(methods.users.GetUserInfo(user_guid))
@@ -431,15 +428,15 @@
         object_guid: str,
         message=None,
         reply_to_message_id: str = None,
         file: bytes = None,
         file_inline: dict = None,
         *args, **kwargs
     ) -> dict:
-        if object_guid.lower() in ['me', 'self', 'cloud']:
+        if compile(r'(?i)^(me|self|cloud)$').match(object_guid):
             object_guid = self._guid
 
         if file:
             file = await self.upload(file, *args, **kwargs)
             for key, value in file_inline.items():
                 file[key] = value
 
@@ -485,24 +482,24 @@
             thumb (bool, optional):
                 if value is "True",
                     the lib will try to build the thumb ( require cv2 )
                 if value is thumbnail.Thumbnail, to set custom
                 Defaults to True.
         """
 
-        if object_guid.lower() in ['me', 'self', 'cloud']:
+        if compile(r'(?i)^(me|self|cloud)$').match(object_guid):
             object_guid = self._guid
 
         if file_inline is not None:
             if not isinstance(file_inline, Struct):
                 if isinstance(file_inline, str):
-                    with open(file_inline, 'rb') as file:
+                    async with aiopen(file_inline, 'rb') as file:
                         kwargs['file_name'] = kwargs.get(
                             'file_name', os.path.basename(file_inline))
-                        file_inline = file.read()
+                        file_inline = await file.read()
 
                 if thumb is True:
                     if type == methods.messages.Image:
                         thumb = thumbnail.MakeThumbnail(file_inline)
 
                     elif type in [methods.messages.Gif, methods.messages.Video]:
                         thumb = thumbnail.MakeThumbnail.from_video(file_inline)
@@ -537,50 +534,43 @@
     async def send_photo(self,
         object_guid: str,
         photo: bytes,
         caption: str = None,
         file_name: str = None,
         width: int = None,
         height: int = None,
-        thumb: str = None,
+        thumb_inline: str = None,
         reply_to_message_id: str = None,
         *args,
         **kwargs,
     ):
-        if cv2 == None and numpy == None:
-            thumb, width, height = (thumbnail.thumb,
-                                          thumbnail.width,
-                                          thumbnail.height
-            )
-
-        if object_guid.lower() in ('me', 'self', 'cloud'):
+        if compile(r'(?i)^(me|self|cloud)$').match(object_guid):
             object_guid = self._guid
 
-        if type(photo) != bytes:
-            async with aiofiles.open(photo, 'rb') as file:
+        if isinstance(photo, str):
+            async with aiopen(photo, 'rb') as file:
                 file_name = os.path.basename(photo)
                 kwargs['file_name'] = kwargs.get('file_name', file_name)
                 photo = await file.read()
-                await file.close()
+
         else:
             kwargs['file_name'] = kwargs.get('file_name', file_name)
 
         file_inline = await self.upload(photo, *args, **kwargs)
         file_inline['type'] = 'Image'
+        thumb = thumbnail.MakeThumbnail(photo)
 
-        if cv2 == None and numpy == None:
+        if isinstance(thumb, thumbnail.Thumbnail):
+            file_inline['width'] = thumb.width
+            file_inline['height'] = thumb.height
+            file_inline['thumb_inline'] = thumb.to_base64()
+        else:
             file_inline['width'] = width
             file_inline['height'] = height
-            file_inline['thumb_inline'] = thumb
-        else:
-            thumb = thumbnail.MakeThumbnail(photo)
-            if isinstance(thumb, thumbnail.Thumbnail):
-                file_inline['width'] = thumb.width
-                file_inline['height'] = thumb.height
-                file_inline['thumb_inline'] = thumb.to_base64()
+            file_inline['thumb_inline'] = thumb_inline
 
         return await self(
             methods.messages.SendMessage(
                 object_guid,
                 message=caption,
                 file_inline=file_inline,
                 reply_to_message_id=reply_to_message_id))
@@ -590,23 +580,22 @@
         file: bytes,
         caption: str = None,
         file_name: str = None,
         reply_to_message_id: str = None,
         *args,
         **kwargs,
     ):
-        if object_guid.lower() in ('me', 'self', 'cloud'):
+        if compile(r'(?i)^(me|self|cloud)$').match(object_guid):
             object_guid = self._guid
 
-        if type(file) != bytes:
-            async with aiofiles.open(file, 'rb') as ofile:
+        if isinstance(file, str):
+            async with aiopen(file, 'rb') as ofile:
                 file_name = os.path.basename(file)
                 kwargs['file_name'] = kwargs.get('file_name', file_name)
                 file = await ofile.read()
-                await ofile.close()
         else:
             kwargs['file_name'] = kwargs.get('file_name', file_name)
 
         file_inline = await self.upload(file, *args, **kwargs)
         file_inline['type'] = 'File'
 
         return await self(
@@ -617,111 +606,93 @@
                 reply_to_message_id=reply_to_message_id))
 
     async def send_gif(self,
         object_guid: str,
         gif: bytes,
         caption: str = None,
         file_name: str = None,
-        thumb: str = None,
+        thumb_inline: str = None,
         time: str = None,
         width: int = None,
         height: int = None,
         reply_to_message_id: str = None,
         *args,
         **kwargs,
     ):
-        if cv2 == None and numpy == None:
-            thumb, time, width, height = (thumbnail.thumb,
-                                          thumbnail.time,
-                                          thumbnail.width,
-                                          thumbnail.height
-            )
-
-        if object_guid.lower() in ('me', 'self', 'cloud'):
+        if compile(r'(?i)^(me|self|cloud)$').match(object_guid):
             object_guid = self._guid
 
-        if type(gif) != bytes:
-            async with aiofiles.open(gif, 'rb') as file:
+        if isinstance(gif, str):
+            async with aiopen(gif, 'rb') as file:
                 file_name = os.path.basename(gif)
                 kwargs['file_name'] = kwargs.get('file_name', file_name)
                 file = await file.read()
-                await file.close()
         else:
             kwargs['file_name'] = kwargs.get('file_name', file_name)
 
         file_inline = await self.upload(gif, *args, **kwargs)
         file_inline['type'] = 'Gif'
+        thumb = thumbnail.MakeThumbnail.from_video(gif)
 
-        if cv2 == None and numpy == None:
+        if isinstance(thumb, thumbnail.Thumbnail):
+            file_inline['time'] = thumb.seconds
+            file_inline['width'] = thumb.width
+            file_inline['height'] = thumb.height
+            file_inline['thumb_inline'] = thumb.to_base64()
+        else:
+            file_inline['time'] = time
             file_inline['width'] = width
             file_inline['height'] = height
-            file_inline['thumb_inline'] = thumb
-            file_inline['time'] = time
-        else:
-            thumb = thumbnail.MakeThumbnail.from_video(gif)
-            if isinstance(thumb, thumbnail.Thumbnail):
-                file_inline['time'] = thumb.seconds
-                file_inline['width'] = thumb.width
-                file_inline['height'] = thumb.height
-                file_inline['thumb_inline'] = thumb.to_base64()
+            file_inline['thumb_inline'] = thumb_inline
 
         return await self(
             methods.messages.SendMessage(
                 object_guid,
                 message=caption,
                 file_inline=file_inline,
                 reply_to_message_id=reply_to_message_id))
 
     async def send_video(self,
         object_guid: str,
         video: bytes,
         caption: str = None,
         file_name: str = None,
-        thumb: str = None,
+        thumb_inline: str = None,
         time: str = None,
         width: int = None,
         height: int = None,
         reply_to_message_id: str = None,
         *args,
         **kwargs,
     ):
-        if cv2 == None and numpy == None:
-            thumb, time, width, height = (thumbnail.thumb,
-                                          thumbnail.time,
-                                          thumbnail.width,
-                                          thumbnail.height
-            )
-
-        if object_guid.lower() in ('me', 'self', 'cloud'):
+        if compile(r'(?i)^(me|self|cloud)$').match(object_guid):
             object_guid = self._guid
 
-        if type(video) != bytes:
-            async with aiofiles.open(video, 'rb') as file:
+        if isinstance(video, str):
+            async with aiopen(video, 'rb') as file:
                 file_name = os.path.basename(video)
                 kwargs['file_name'] = kwargs.get('file_name', file_name)
                 video = await file.read()
-                await file.close()
         else:
             kwargs['file_name'] = kwargs.get('file_name', file_name)
 
         file_inline = await self.upload(video, *args, **kwargs)
         file_inline['type'] = 'Video'
+        thumb = thumbnail.MakeThumbnail.from_video(video)
 
-        if cv2 == None and numpy == None:
+        if isinstance(thumb, thumbnail.Thumbnail):
+            file_inline['time'] = thumb.seconds
+            file_inline['width'] = thumb.width
+            file_inline['height'] = thumb.height
+            file_inline['thumb_inline'] = thumb.to_base64()
+        else:
+            file_inline['time'] = time
             file_inline['width'] = width
             file_inline['height'] = height
-            file_inline['thumb_inline'] = thumb
-            file_inline['time'] = time
-        else:
-            thumb = thumbnail.MakeThumbnail.from_video(video)
-            if isinstance(thumb, thumbnail.Thumbnail):
-                file_inline['time'] = thumb.seconds
-                file_inline['width'] = thumb.width
-                file_inline['height'] = thumb.height
-                file_inline['thumb_inline'] = thumb.to_base64()
+            file_inline['thumb_inline'] = thumb_inline
 
         return await self(
             methods.messages.SendMessage(
                 object_guid,
                 message=caption,
                 file_inline=file_inline,
                 reply_to_message_id=reply_to_message_id))
@@ -733,68 +704,69 @@
         file_name: str = None,
         time: str = None,
         performer: str = None,
         reply_to_message_id: str = None,
         *args,
         **kwargs,
     ):
-        if object_guid.lower() in ('me', 'self', 'cloud'):
+        if compile(r'(?i)^(me|self|cloud)$').match(object_guid):
             object_guid = self._guid
 
         if isinstance(music, bytes):
             kwargs['file_name'] = kwargs.get('file_name', file_name)
         else:
-            async with aiofiles.open(music, 'rb') as file:
+            async with aiopen(music, 'rb') as file:
                 kwargs['file_name'] = kwargs.get('file_name', os.path.basename(music))
                 music = await file.read()
 
         file_inline = await self.upload(music, *args, **kwargs)
         file_inline['type'] = 'Music'
         file_inline['auto_play'] = False
         file_inline['music_performer'] = kwargs.get('performer', performer or '')
-        file_inline['time'] = time or 60
+        file = BytesIO()
+        file.write(music)
+        file.seek(0)
+        file_inline['time'] = time or MP3(file).info.length * 1000
 
         return await self(
             methods.messages.SendMessage(
                 object_guid,
                 message=caption,
                 file_inline=file_inline,
                 reply_to_message_id=reply_to_message_id))
 
     async def send_voice(self,
         object_guid: str,
-        music: bytes,
+        voice: bytes,
         caption: str = None,
         file_name: str = None,
         time: str = None,
         reply_to_message_id: str = None,
         *args,
         **kwargs,
     ):
-        if object_guid.lower() in ('me', 'self', 'cloud'):
+        if compile(r'(?i)^(me|self|cloud)$').match(object_guid):
             object_guid = self._guid
 
-        if type(music) != bytes:
-            async with aiofiles.open(music, 'rb') as file:
-                file_name = os.path.basename(music)
+        if isinstance(voice, str):
+            async with aiopen(voice, 'rb') as file:
+                file_name = os.path.basename(voice)
                 kwargs['file_name'] = kwargs.get('file_name', file_name)
                 file = await file.read()
-                await file.close()
         else:
             kwargs['file_name'] = kwargs.get('file_name', file_name)
 
-        file_inline = await self.upload(music, *args, **kwargs)
+        file_inline = await self.upload(voice, *args, **kwargs)
         file_inline['type'] = 'Voice'
         file_inline['mime'] = 'ogg'
         file_inline['auto_play'] = False
-
-        if time != None:
-            file_inline['time'] = time
-        else:
-            file_inline['time'] = '60'
+        file = BytesIO()
+        file.write(voice)
+        file.seek(0)
+        file_inline['time'] = str(time or MP3(file).info.length * 1000)
 
         return await self(
             methods.messages.SendMessage(
                 object_guid,
                 message=caption,
                 file_inline=file_inline,
                 reply_to_message_id=reply_to_message_id))
```

### Comparing `rubpy-6.3.1/rubpy/crypto/crypto.py` & `rubpy-6.3.2/rubpy/crypto/crypto.py`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.1/rubpy/gadgets/classino.py` & `rubpy-6.3.2/rubpy/gadgets/classino.py`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.1/rubpy/gadgets/exceptions.py` & `rubpy-6.3.2/rubpy/gadgets/exceptions.py`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.1/rubpy/gadgets/grouping.py` & `rubpy-6.3.2/rubpy/gadgets/grouping.py`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.1/rubpy/gadgets/methods.py` & `rubpy-6.3.2/rubpy/gadgets/methods.py`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.1/rubpy/gadgets/thumbnail.py` & `rubpy-6.3.2/rubpy/gadgets/thumbnail.py`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.1/rubpy/network/connection.py` & `rubpy-6.3.2/rubpy/network/connection.py`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.1/rubpy/network/proxies.py` & `rubpy-6.3.2/rubpy/network/proxies.py`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.1/rubpy/sessions/sqliteSession.py` & `rubpy-6.3.2/rubpy/sessions/sqliteSession.py`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.1/rubpy/sessions/stringSession.py` & `rubpy-6.3.2/rubpy/sessions/stringSession.py`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.1/rubpy/structs/handlers.py` & `rubpy-6.3.2/rubpy/structs/handlers.py`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.1/rubpy/structs/models.py` & `rubpy-6.3.2/rubpy/structs/models.py`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.1/rubpy/structs/results.py` & `rubpy-6.3.2/rubpy/structs/results.py`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.1/rubpy/structs/struct.py` & `rubpy-6.3.2/rubpy/structs/struct.py`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.1/rubpy.egg-info/PKG-INFO` & `rubpy-6.3.2/rubpy.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: rubpy
-Version: 6.3.1
+Version: 6.3.2
 Summary: This is an unofficial library and fastest library for deploying robots on Rubika accounts.
 Home-page: https://github.com/shayanheidari01/rubika
 Author: Shayan Heidari
 Author-email: contact@shayanheidari.info
 Keywords: rubika,rubpy,chat,bot,robot,asyncio
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: rubpy Version: 6.3.1 Summary: This is an unofficial
+Metadata-Version: 2.1 Name: rubpy Version: 6.3.2 Summary: This is an unofficial
 library and fastest library for deploying robots on Rubika accounts. Home-page:
 https://github.com/shayanheidari01/rubika Author: Shayan Heidari Author-email:
 contact@shayanheidari.info Keywords: rubika,rubpy,chat,bot,robot,asyncio
 Classifier: Programming Language :: Python :: 3.7 Classifier: Programming
 Language :: Python :: 3.8 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10 Classifier: Programming
 Language :: Python :: 3.11 Classifier: Programming Language :: Python :: 3.12
```

### Comparing `rubpy-6.3.1/rubpy.egg-info/SOURCES.txt` & `rubpy-6.3.2/rubpy.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `rubpy-6.3.1/setup.py` & `rubpy-6.3.2/setup.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,17 +1,17 @@
 from setuptools import setup, find_packages
 
-requirements = ['aiohttp', 'pycryptodome', 'aiofiles']
+requirements = ['aiohttp', 'pycryptodome', 'aiofiles', 'mutagen']
 
 with open("README.md", encoding="UTF-8") as f:
     readme = f.read()
 
 setup(
     name = 'rubpy',
-    version = '6.3.1',
+    version = '6.3.2',
     author='Shayan Heidari',
     author_email = 'contact@shayanheidari.info',
     description = 'This is an unofficial library and fastest library for deploying robots on Rubika accounts.',
     keywords = ['rubika', 'rubpy', 'chat', 'bot', 'robot', 'asyncio'],
     long_description = readme,
     python_requires="~=3.7",
     long_description_content_type = 'text/markdown',
```

