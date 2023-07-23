# Comparing `tmp/rec_spotify-1.2.1.tar.gz` & `tmp/rec_spotify-1.2.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "rec_spotify-1.2.1.tar", max compression
+gzip compressed data, was "rec_spotify-1.2.2.tar", max compression
```

## Comparing `rec_spotify-1.2.1.tar` & `rec_spotify-1.2.2.tar`

### file list

```diff
@@ -1,16 +1,16 @@
--rw-r--r--   0        0        0    41650 2023-07-23 20:18:21.052582 rec_spotify-1.2.1/etc/screen.png
--rw-r--r--   0        0        0     1291 2023-07-23 20:27:20.288282 rec_spotify-1.2.1/pyproject.toml
--rw-r--r--   0        0        0     2289 2023-07-23 20:20:05.543332 rec_spotify-1.2.1/README.md
--rw-r--r--   0        0        0        0 2023-07-22 09:49:59.044263 rec_spotify-1.2.1/rec_spotify/__init__.py
--rw-r--r--   0        0        0     1554 2023-07-23 19:52:10.190507 rec_spotify-1.2.1/rec_spotify/cli.py
--rw-r--r--   0        0        0     3915 2023-07-23 18:15:50.766094 rec_spotify-1.2.1/rec_spotify/config.py
--rw-r--r--   0        0        0      758 2023-07-23 15:35:03.891743 rec_spotify-1.2.1/rec_spotify/console.py
--rw-r--r--   0        0        0     7310 2023-07-23 19:42:31.072891 rec_spotify-1.2.1/rec_spotify/database.py
--rw-r--r--   0        0        0     6427 2023-07-23 15:53:09.981754 rec_spotify-1.2.1/rec_spotify/items.py
--rw-r--r--   0        0        0     2195 2023-07-23 16:28:40.968471 rec_spotify-1.2.1/rec_spotify/lyrics.py
--rw-r--r--   0        0        0     6405 2023-07-23 19:54:00.000154 rec_spotify-1.2.1/rec_spotify/manager.py
--rw-r--r--   0        0        0     1968 2023-07-23 16:07:01.827794 rec_spotify-1.2.1/rec_spotify/messages.py
--rw-r--r--   0        0        0     3317 2023-07-23 18:16:28.832707 rec_spotify-1.2.1/rec_spotify/recorder.py
--rw-r--r--   0        0        0     5375 2023-07-23 17:02:19.699967 rec_spotify-1.2.1/rec_spotify/spotify.py
--rw-r--r--   0        0        0     1457 2023-07-23 16:26:57.110938 rec_spotify-1.2.1/rec_spotify/utils.py
--rw-r--r--   0        0        0     3005 1970-01-01 00:00:00.000000 rec_spotify-1.2.1/PKG-INFO
+-rw-r--r--   0        0        0    41650 2023-07-23 20:18:21.052582 rec_spotify-1.2.2/etc/screen.png
+-rw-r--r--   0        0        0     1291 2023-07-23 20:44:03.304974 rec_spotify-1.2.2/pyproject.toml
+-rw-r--r--   0        0        0     2289 2023-07-23 20:20:05.543332 rec_spotify-1.2.2/README.md
+-rw-r--r--   0        0        0       21 2023-07-23 20:45:10.978234 rec_spotify-1.2.2/rec_spotify/__init__.py
+-rw-r--r--   0        0        0     1735 2023-07-23 20:50:02.825572 rec_spotify-1.2.2/rec_spotify/cli.py
+-rw-r--r--   0        0        0     3915 2023-07-23 18:15:50.766094 rec_spotify-1.2.2/rec_spotify/config.py
+-rw-r--r--   0        0        0      758 2023-07-23 15:35:03.891743 rec_spotify-1.2.2/rec_spotify/console.py
+-rw-r--r--   0        0        0     7310 2023-07-23 19:42:31.072891 rec_spotify-1.2.2/rec_spotify/database.py
+-rw-r--r--   0        0        0     6427 2023-07-23 15:53:09.981754 rec_spotify-1.2.2/rec_spotify/items.py
+-rw-r--r--   0        0        0     2195 2023-07-23 16:28:40.968471 rec_spotify-1.2.2/rec_spotify/lyrics.py
+-rw-r--r--   0        0        0     6405 2023-07-23 19:54:00.000154 rec_spotify-1.2.2/rec_spotify/manager.py
+-rw-r--r--   0        0        0     1968 2023-07-23 16:07:01.827794 rec_spotify-1.2.2/rec_spotify/messages.py
+-rw-r--r--   0        0        0     3317 2023-07-23 18:16:28.832707 rec_spotify-1.2.2/rec_spotify/recorder.py
+-rw-r--r--   0        0        0     5375 2023-07-23 17:02:19.699967 rec_spotify-1.2.2/rec_spotify/spotify.py
+-rw-r--r--   0        0        0     1457 2023-07-23 16:26:57.110938 rec_spotify-1.2.2/rec_spotify/utils.py
+-rw-r--r--   0        0        0     3005 1970-01-01 00:00:00.000000 rec_spotify-1.2.2/PKG-INFO
```

### Comparing `rec_spotify-1.2.1/etc/screen.png` & `rec_spotify-1.2.2/etc/screen.png`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.2.1/pyproject.toml` & `rec_spotify-1.2.2/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "rec-spotify"
-version = "1.2.1"
+version = "1.2.2"
 description = "📻 Record and sync Spotify tracks, albums, and playlists."
 repository = "https://github.com/oSeeLight/rec-spotify"
 authors = ["Jacov Rainz <oSeeLight@proton.me>"]
 license = "MIT"
 readme = "README.md"
 packages = [{include = "rec_spotify"}]
 include = ["README.md", "etc"]
```

### Comparing `rec_spotify-1.2.1/README.md` & `rec_spotify-1.2.2/README.md`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.2.1/rec_spotify/cli.py` & `rec_spotify-1.2.2/rec_spotify/cli.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,22 +1,23 @@
 import argparse
 import sys
+import rec_spotify
 
 import rec_spotify.messages as m
 from rec_spotify.items import Collection, Track
 from rec_spotify.manager import Manager
 from rec_spotify.config import Config
 from rec_spotify.console import console, get_logo
 from rec_spotify.utils import parse_spotify_url
 
 
 def app() -> None:
     """CLI entrypoint."""
 
-    console.print(get_logo())
+    console.print(get_logo(), style="green")
 
     parser = argparse.ArgumentParser()
 
     parser.add_argument(
         "-u",
         "--url",
         type=str,
@@ -26,14 +27,17 @@
     parser.add_argument(
         "-p",
         "--path",
         type=str,
         required=False,
         help="The output directory for saving recorded files",
     )
+    ver = f"Author: oSeeLight | Version: {rec_spotify.__version__}"
+    parser.add_argument('-v', '--version', action='version', version=ver)
+
 
     args = parser.parse_args()
     manager = Manager()
     if args.url and args.path:
         match = parse_spotify_url(args.url)
         if match is not None:
             link_type, id = match
```

### Comparing `rec_spotify-1.2.1/rec_spotify/config.py` & `rec_spotify-1.2.2/rec_spotify/config.py`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.2.1/rec_spotify/console.py` & `rec_spotify-1.2.2/rec_spotify/console.py`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.2.1/rec_spotify/database.py` & `rec_spotify-1.2.2/rec_spotify/database.py`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.2.1/rec_spotify/items.py` & `rec_spotify-1.2.2/rec_spotify/items.py`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.2.1/rec_spotify/lyrics.py` & `rec_spotify-1.2.2/rec_spotify/lyrics.py`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.2.1/rec_spotify/manager.py` & `rec_spotify-1.2.2/rec_spotify/manager.py`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.2.1/rec_spotify/messages.py` & `rec_spotify-1.2.2/rec_spotify/messages.py`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.2.1/rec_spotify/recorder.py` & `rec_spotify-1.2.2/rec_spotify/recorder.py`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.2.1/rec_spotify/spotify.py` & `rec_spotify-1.2.2/rec_spotify/spotify.py`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.2.1/rec_spotify/utils.py` & `rec_spotify-1.2.2/rec_spotify/utils.py`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.2.1/PKG-INFO` & `rec_spotify-1.2.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: rec-spotify
-Version: 1.2.1
+Version: 1.2.2
 Summary: 📻 Record and sync Spotify tracks, albums, and playlists.
 Home-page: https://github.com/oSeeLight/rec-spotify
 License: MIT
 Keywords: spotify,record
 Author: Jacov Rainz
 Author-email: oSeeLight@proton.me
 Requires-Python: >=3.11,<4.0
```

