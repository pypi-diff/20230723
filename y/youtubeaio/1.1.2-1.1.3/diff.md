# Comparing `tmp/youtubeaio-1.1.2.tar.gz` & `tmp/youtubeaio-1.1.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "youtubeaio-1.1.2.tar", max compression
+gzip compressed data, was "youtubeaio-1.1.3.tar", max compression
```

## Comparing `youtubeaio-1.1.2.tar` & `youtubeaio-1.1.3.tar`

### file list

```diff
@@ -1,12 +1,12 @@
--rw-r--r--   0        0        0     1077 2023-07-22 23:43:54.893722 youtubeaio-1.1.2/LICENSE.md
--rw-r--r--   0        0        0     4864 2023-07-22 23:43:54.893722 youtubeaio-1.1.2/README.md
--rw-r--r--   0        0        0     3873 2023-07-22 23:44:12.217913 youtubeaio-1.1.2/pyproject.toml
--rw-r--r--   0        0        0       57 2023-07-22 23:43:54.893722 youtubeaio-1.1.2/src/youtubeaio/__init__.py
--rw-r--r--   0        0        0      831 2023-07-22 23:43:54.893722 youtubeaio-1.1.2/src/youtubeaio/const.py
--rw-r--r--   0        0        0     3149 2023-07-22 23:43:54.893722 youtubeaio-1.1.2/src/youtubeaio/helper.py
--rw-r--r--   0        0        0     7429 2023-07-22 23:43:54.893722 youtubeaio-1.1.2/src/youtubeaio/models.py
--rw-r--r--   0        0        0     1772 2023-07-22 23:43:54.893722 youtubeaio-1.1.2/src/youtubeaio/oauth.py
--rw-r--r--   0        0        0        0 2023-07-22 23:43:54.893722 youtubeaio-1.1.2/src/youtubeaio/py.typed
--rw-r--r--   0        0        0     2139 2023-07-22 23:43:54.893722 youtubeaio-1.1.2/src/youtubeaio/types.py
--rw-r--r--   0        0        0     9463 2023-07-22 23:43:54.893722 youtubeaio-1.1.2/src/youtubeaio/youtube.py
--rw-r--r--   0        0        0     6115 1970-01-01 00:00:00.000000 youtubeaio-1.1.2/PKG-INFO
+-rw-r--r--   0        0        0     1077 2023-07-23 20:40:32.208353 youtubeaio-1.1.3/LICENSE.md
+-rw-r--r--   0        0        0     4864 2023-07-23 20:40:32.208353 youtubeaio-1.1.3/README.md
+-rw-r--r--   0        0        0     3873 2023-07-23 20:40:50.976369 youtubeaio-1.1.3/pyproject.toml
+-rw-r--r--   0        0        0       57 2023-07-23 20:40:32.208353 youtubeaio-1.1.3/src/youtubeaio/__init__.py
+-rw-r--r--   0        0        0      831 2023-07-23 20:40:32.208353 youtubeaio-1.1.3/src/youtubeaio/const.py
+-rw-r--r--   0        0        0     3149 2023-07-23 20:40:32.208353 youtubeaio-1.1.3/src/youtubeaio/helper.py
+-rw-r--r--   0        0        0     7429 2023-07-23 20:40:32.208353 youtubeaio-1.1.3/src/youtubeaio/models.py
+-rw-r--r--   0        0        0     1772 2023-07-23 20:40:32.208353 youtubeaio-1.1.3/src/youtubeaio/oauth.py
+-rw-r--r--   0        0        0        0 2023-07-23 20:40:32.208353 youtubeaio-1.1.3/src/youtubeaio/py.typed
+-rw-r--r--   0        0        0     2139 2023-07-23 20:40:32.208353 youtubeaio-1.1.3/src/youtubeaio/types.py
+-rw-r--r--   0        0        0     9483 2023-07-23 20:40:32.208353 youtubeaio-1.1.3/src/youtubeaio/youtube.py
+-rw-r--r--   0        0        0     6115 1970-01-01 00:00:00.000000 youtubeaio-1.1.3/PKG-INFO
```

### Comparing `youtubeaio-1.1.2/LICENSE.md` & `youtubeaio-1.1.3/LICENSE.md`

 * *Files identical despite different names*

### Comparing `youtubeaio-1.1.2/README.md` & `youtubeaio-1.1.3/README.md`

 * *Files identical despite different names*

### Comparing `youtubeaio-1.1.2/pyproject.toml` & `youtubeaio-1.1.3/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "youtubeaio"
-version = "1.1.2"
+version = "1.1.3"
 description = "Asynchronous Python client for YouTube V3 API."
 authors = ["Joost Lekkerkerker <joostlek@outlook.com>"]
 maintainers = ["Joost Lekkerkerker <joostlek@outlook.com>"]
 license = "MIT"
 readme = "README.md"
 homepage = "https://github.com/joostlek/python-youtube"
 repository = "https://github.com/joostlek/python-youtube"
```

### Comparing `youtubeaio-1.1.2/src/youtubeaio/const.py` & `youtubeaio-1.1.3/src/youtubeaio/const.py`

 * *Files identical despite different names*

### Comparing `youtubeaio-1.1.2/src/youtubeaio/helper.py` & `youtubeaio-1.1.3/src/youtubeaio/helper.py`

 * *Files identical despite different names*

### Comparing `youtubeaio-1.1.2/src/youtubeaio/models.py` & `youtubeaio-1.1.3/src/youtubeaio/models.py`

 * *Files identical despite different names*

### Comparing `youtubeaio-1.1.2/src/youtubeaio/oauth.py` & `youtubeaio-1.1.3/src/youtubeaio/oauth.py`

 * *Files identical despite different names*

### Comparing `youtubeaio-1.1.2/src/youtubeaio/types.py` & `youtubeaio-1.1.3/src/youtubeaio/types.py`

 * *Files identical despite different names*

### Comparing `youtubeaio-1.1.2/src/youtubeaio/youtube.py` & `youtubeaio-1.1.3/src/youtubeaio/youtube.py`

 * *Files 0% similar despite different names*

```diff
@@ -187,15 +187,15 @@
     ) -> AsyncGenerator[YouTubeVideo, None]:
         """Get videos by id."""
         if not video_ids:
             msg = "at least one video id has to be set"
             raise ValueError(msg)
         param = {
             "part": "snippet",
-            "id": video_ids,
+            "id": ",".join(video_ids),
         }
         async for item in self._build_generator(
             "GET",
             "videos",
             param,
             YouTubeVideo,
         ):
@@ -230,15 +230,15 @@
     async def get_channels(
         self,
         channel_ids: list[str],
     ) -> AsyncGenerator[YouTubeChannel, None]:
         """Return list of channels."""
         param = {
             "part": "snippet,contentDetails,statistics",
-            "id": channel_ids,
+            "id": ",".join(channel_ids),
         }
         async for item in self._get_channels(param):
             yield item
 
     async def get_user_subscriptions(
         self,
     ) -> AsyncGenerator[YouTubeSubscription, None]:
```

### Comparing `youtubeaio-1.1.2/PKG-INFO` & `youtubeaio-1.1.3/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: youtubeaio
-Version: 1.1.2
+Version: 1.1.3
 Summary: Asynchronous Python client for YouTube V3 API.
 Home-page: https://github.com/joostlek/python-youtube
 License: MIT
 Keywords: youtube,api,async,client
 Author: Joost Lekkerkerker
 Author-email: joostlek@outlook.com
 Maintainer: Joost Lekkerkerker
```

