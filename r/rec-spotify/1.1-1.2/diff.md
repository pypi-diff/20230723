# Comparing `tmp/rec_spotify-1.1.tar.gz` & `tmp/rec_spotify-1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "rec_spotify-1.1.tar", max compression
+gzip compressed data, was "rec_spotify-1.2.tar", max compression
```

## Comparing `rec_spotify-1.1.tar` & `rec_spotify-1.2.tar`

### file list

```diff
@@ -1,15 +1,15 @@
--rw-r--r--   0        0        0     1277 2023-07-23 19:58:00.554218 rec_spotify-1.1/pyproject.toml
--rw-r--r--   0        0        0     1994 2023-07-23 18:24:37.260843 rec_spotify-1.1/README.md
--rw-r--r--   0        0        0        0 2023-07-22 09:49:59.044263 rec_spotify-1.1/rec_spotify/__init__.py
--rw-r--r--   0        0        0     1554 2023-07-23 19:52:10.190507 rec_spotify-1.1/rec_spotify/cli.py
--rw-r--r--   0        0        0     3915 2023-07-23 18:15:50.766094 rec_spotify-1.1/rec_spotify/config.py
--rw-r--r--   0        0        0      758 2023-07-23 15:35:03.891743 rec_spotify-1.1/rec_spotify/console.py
--rw-r--r--   0        0        0     7310 2023-07-23 19:42:31.072891 rec_spotify-1.1/rec_spotify/database.py
--rw-r--r--   0        0        0     6427 2023-07-23 15:53:09.981754 rec_spotify-1.1/rec_spotify/items.py
--rw-r--r--   0        0        0     2195 2023-07-23 16:28:40.968471 rec_spotify-1.1/rec_spotify/lyrics.py
--rw-r--r--   0        0        0     6405 2023-07-23 19:54:00.000154 rec_spotify-1.1/rec_spotify/manager.py
--rw-r--r--   0        0        0     1968 2023-07-23 16:07:01.827794 rec_spotify-1.1/rec_spotify/messages.py
--rw-r--r--   0        0        0     3317 2023-07-23 18:16:28.832707 rec_spotify-1.1/rec_spotify/recorder.py
--rw-r--r--   0        0        0     5375 2023-07-23 17:02:19.699967 rec_spotify-1.1/rec_spotify/spotify.py
--rw-r--r--   0        0        0     1457 2023-07-23 16:26:57.110938 rec_spotify-1.1/rec_spotify/utils.py
--rw-r--r--   0        0        0     2709 1970-01-01 00:00:00.000000 rec_spotify-1.1/PKG-INFO
+-rw-r--r--   0        0        0     1282 2023-07-23 20:22:11.580667 rec_spotify-1.2/pyproject.toml
+-rw-r--r--   0        0        0     2289 2023-07-23 20:20:05.543332 rec_spotify-1.2/README.md
+-rw-r--r--   0        0        0        0 2023-07-22 09:49:59.044263 rec_spotify-1.2/rec_spotify/__init__.py
+-rw-r--r--   0        0        0     1554 2023-07-23 19:52:10.190507 rec_spotify-1.2/rec_spotify/cli.py
+-rw-r--r--   0        0        0     3915 2023-07-23 18:15:50.766094 rec_spotify-1.2/rec_spotify/config.py
+-rw-r--r--   0        0        0      758 2023-07-23 15:35:03.891743 rec_spotify-1.2/rec_spotify/console.py
+-rw-r--r--   0        0        0     7310 2023-07-23 19:42:31.072891 rec_spotify-1.2/rec_spotify/database.py
+-rw-r--r--   0        0        0     6427 2023-07-23 15:53:09.981754 rec_spotify-1.2/rec_spotify/items.py
+-rw-r--r--   0        0        0     2195 2023-07-23 16:28:40.968471 rec_spotify-1.2/rec_spotify/lyrics.py
+-rw-r--r--   0        0        0     6405 2023-07-23 19:54:00.000154 rec_spotify-1.2/rec_spotify/manager.py
+-rw-r--r--   0        0        0     1968 2023-07-23 16:07:01.827794 rec_spotify-1.2/rec_spotify/messages.py
+-rw-r--r--   0        0        0     3317 2023-07-23 18:16:28.832707 rec_spotify-1.2/rec_spotify/recorder.py
+-rw-r--r--   0        0        0     5375 2023-07-23 17:02:19.699967 rec_spotify-1.2/rec_spotify/spotify.py
+-rw-r--r--   0        0        0     1457 2023-07-23 16:26:57.110938 rec_spotify-1.2/rec_spotify/utils.py
+-rw-r--r--   0        0        0     3003 1970-01-01 00:00:00.000000 rec_spotify-1.2/PKG-INFO
```

### Comparing `rec_spotify-1.1/pyproject.toml` & `rec_spotify-1.2/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 [tool.poetry]
 name = "rec-spotify"
-version = "1.1"
-description = "Record and sync Spotify tracks, albums, and playlists."
+version = "1.2"
+description = "📻 Record and sync Spotify tracks, albums, and playlists."
 repository = "https://github.com/oSeeLight/rec-spotify"
 authors = ["Jacov Rainz <oSeeLight@proton.me>"]
 license = "MIT"
 readme = "README.md"
 packages = [{include = "rec_spotify"}]
 include = ["README.md"]
 keywords = ["spotify", "record"]
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `rec_spotify-1.1/README.md` & `rec_spotify-1.2/README.md`

 * *Files 19% similar despite different names*

```diff
@@ -1,9 +1,11 @@
 # 📻 Rec-Spotify
 
+![](etc/screen.png)
+
 The program allows you to record Spotify tracks, albums, and playlists with a single simple command. It is also able to fully synchronize your Spotify playlists to a local folder and keep them up-to-date.
 
 For now it works **only** on Windows.
 
 ## Requirements
 
 - Python3
@@ -12,14 +14,30 @@
 
 ## Install
 
 ```sh
 pip install rec-spotify
 ```
 
+## Usage
+
+First, you need to create a Spotify app to obtain the credentials. You can create an app at the Spotify Developer Dashboard: https://developer.spotify.com/dashboard
+
+Also change Spotify Output Device to Virtual Audio Cable: [Guide](https://youtu.be/EH-VzIpX7e0?t=86)
+
+```sh
+# Perform a full synchronization.
+rec-spotify
+
+# Record single track/album/playlist.
+# Spotify URL format example: https://open.spotify.com/track/42vwak6ZIFMscDhzz3S52f
+# Output path format example: C:\Users\<username>\Desktop or just "." to save in current directory
+rec-spotify --url <url> --path <where_to_save>
+```
+
 ## Configration
 
 On the first run, the program will launch a setup wizard. This will prompt you to enter your Spotify app credentials and other required information.
 
 The config file is located at: ```C:\Users\<username>\.rec_spotify\config.ini```
 
 Config example:
@@ -33,26 +51,14 @@
 [SETTINGS]
 MUSIC_DIR = D:\Music
 AUDIO_FORMAT = mp3
 AUDIO_QUALITY = 320
 SAMPLE_RATE = 48000
 ```
 
-## Usage
-
-```sh
-# Perform a full synchronization.
-rec-spotify
-
-# Record single track/album/playlist.
-# Spotify URL format example: https://open.spotify.com/track/42vwak6ZIFMscDhzz3S52f
-# Output path format example: C:\Users\<username>\Desktop or just "." to save in current directory
-rec-spotify --url <url> --path <where_to_save>
-```
-
 ## FAQ
 
 ### 1. What is the purpose of this program?
 
 The answer is simple: I want to have local copies of all my Spotify tracks and playlists in original quality. Because who knows maybe one day i will lose access to my account or something else will happen.
 
 ### 2. Why do I need Virtual Audio Cable?
```

### Comparing `rec_spotify-1.1/rec_spotify/cli.py` & `rec_spotify-1.2/rec_spotify/cli.py`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.1/rec_spotify/config.py` & `rec_spotify-1.2/rec_spotify/config.py`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.1/rec_spotify/console.py` & `rec_spotify-1.2/rec_spotify/console.py`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.1/rec_spotify/database.py` & `rec_spotify-1.2/rec_spotify/database.py`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.1/rec_spotify/items.py` & `rec_spotify-1.2/rec_spotify/items.py`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.1/rec_spotify/lyrics.py` & `rec_spotify-1.2/rec_spotify/lyrics.py`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.1/rec_spotify/manager.py` & `rec_spotify-1.2/rec_spotify/manager.py`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.1/rec_spotify/messages.py` & `rec_spotify-1.2/rec_spotify/messages.py`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.1/rec_spotify/recorder.py` & `rec_spotify-1.2/rec_spotify/recorder.py`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.1/rec_spotify/spotify.py` & `rec_spotify-1.2/rec_spotify/spotify.py`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.1/rec_spotify/utils.py` & `rec_spotify-1.2/rec_spotify/utils.py`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.1/PKG-INFO` & `rec_spotify-1.2/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 Metadata-Version: 2.1
 Name: rec-spotify
-Version: 1.1
-Summary: Record and sync Spotify tracks, albums, and playlists.
+Version: 1.2
+Summary: 📻 Record and sync Spotify tracks, albums, and playlists.
 Home-page: https://github.com/oSeeLight/rec-spotify
 License: MIT
 Keywords: spotify,record
 Author: Jacov Rainz
 Author-email: oSeeLight@proton.me
 Requires-Python: >=3.11,<4.0
 Classifier: License :: OSI Approved :: MIT License
@@ -18,14 +18,16 @@
 Requires-Dist: rich (>=13.4.2,<14.0.0)
 Requires-Dist: spotipy (>=2.23.0,<3.0.0)
 Project-URL: Repository, https://github.com/oSeeLight/rec-spotify
 Description-Content-Type: text/markdown
 
 # 📻 Rec-Spotify
 
+![](etc/screen.png)
+
 The program allows you to record Spotify tracks, albums, and playlists with a single simple command. It is also able to fully synchronize your Spotify playlists to a local folder and keep them up-to-date.
 
 For now it works **only** on Windows.
 
 ## Requirements
 
 - Python3
@@ -34,14 +36,30 @@
 
 ## Install
 
 ```sh
 pip install rec-spotify
 ```
 
+## Usage
+
+First, you need to create a Spotify app to obtain the credentials. You can create an app at the Spotify Developer Dashboard: https://developer.spotify.com/dashboard
+
+Also change Spotify Output Device to Virtual Audio Cable: [Guide](https://youtu.be/EH-VzIpX7e0?t=86)
+
+```sh
+# Perform a full synchronization.
+rec-spotify
+
+# Record single track/album/playlist.
+# Spotify URL format example: https://open.spotify.com/track/42vwak6ZIFMscDhzz3S52f
+# Output path format example: C:\Users\<username>\Desktop or just "." to save in current directory
+rec-spotify --url <url> --path <where_to_save>
+```
+
 ## Configration
 
 On the first run, the program will launch a setup wizard. This will prompt you to enter your Spotify app credentials and other required information.
 
 The config file is located at: ```C:\Users\<username>\.rec_spotify\config.ini```
 
 Config example:
@@ -55,26 +73,14 @@
 [SETTINGS]
 MUSIC_DIR = D:\Music
 AUDIO_FORMAT = mp3
 AUDIO_QUALITY = 320
 SAMPLE_RATE = 48000
 ```
 
-## Usage
-
-```sh
-# Perform a full synchronization.
-rec-spotify
-
-# Record single track/album/playlist.
-# Spotify URL format example: https://open.spotify.com/track/42vwak6ZIFMscDhzz3S52f
-# Output path format example: C:\Users\<username>\Desktop or just "." to save in current directory
-rec-spotify --url <url> --path <where_to_save>
-```
-
 ## FAQ
 
 ### 1. What is the purpose of this program?
 
 The answer is simple: I want to have local copies of all my Spotify tracks and playlists in original quality. Because who knows maybe one day i will lose access to my account or something else will happen.
 
 ### 2. Why do I need Virtual Audio Cable?
```

