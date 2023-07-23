# Comparing `tmp/rec_spotify-1.0.tar.gz` & `tmp/rec_spotify-1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "rec_spotify-1.0.tar", max compression
+gzip compressed data, was "rec_spotify-1.1.tar", max compression
```

## Comparing `rec_spotify-1.0.tar` & `rec_spotify-1.1.tar`

### file list

```diff
@@ -1,15 +1,15 @@
--rw-r--r--   0        0        0     1277 2023-07-23 18:07:09.621751 rec_spotify-1.0/pyproject.toml
--rw-r--r--   0        0        0     1994 2023-07-23 18:24:37.260843 rec_spotify-1.0/README.md
--rw-r--r--   0        0        0        0 2023-07-22 09:49:59.044263 rec_spotify-1.0/rec_spotify/__init__.py
--rw-r--r--   0        0        0     1550 2023-07-23 17:02:14.750976 rec_spotify-1.0/rec_spotify/cli.py
--rw-r--r--   0        0        0     3915 2023-07-23 18:15:50.766094 rec_spotify-1.0/rec_spotify/config.py
--rw-r--r--   0        0        0      758 2023-07-23 15:35:03.891743 rec_spotify-1.0/rec_spotify/console.py
--rw-r--r--   0        0        0     7228 2023-07-23 16:28:14.668973 rec_spotify-1.0/rec_spotify/database.py
--rw-r--r--   0        0        0     6427 2023-07-23 15:53:09.981754 rec_spotify-1.0/rec_spotify/items.py
--rw-r--r--   0        0        0     2195 2023-07-23 16:28:40.968471 rec_spotify-1.0/rec_spotify/lyrics.py
--rw-r--r--   0        0        0     6336 2023-07-23 17:02:50.320967 rec_spotify-1.0/rec_spotify/manager.py
--rw-r--r--   0        0        0     1968 2023-07-23 16:07:01.827794 rec_spotify-1.0/rec_spotify/messages.py
--rw-r--r--   0        0        0     3317 2023-07-23 18:16:28.832707 rec_spotify-1.0/rec_spotify/recorder.py
--rw-r--r--   0        0        0     5375 2023-07-23 17:02:19.699967 rec_spotify-1.0/rec_spotify/spotify.py
--rw-r--r--   0        0        0     1457 2023-07-23 16:26:57.110938 rec_spotify-1.0/rec_spotify/utils.py
--rw-r--r--   0        0        0     2709 1970-01-01 00:00:00.000000 rec_spotify-1.0/PKG-INFO
+-rw-r--r--   0        0        0     1277 2023-07-23 19:58:00.554218 rec_spotify-1.1/pyproject.toml
+-rw-r--r--   0        0        0     1994 2023-07-23 18:24:37.260843 rec_spotify-1.1/README.md
+-rw-r--r--   0        0        0        0 2023-07-22 09:49:59.044263 rec_spotify-1.1/rec_spotify/__init__.py
+-rw-r--r--   0        0        0     1554 2023-07-23 19:52:10.190507 rec_spotify-1.1/rec_spotify/cli.py
+-rw-r--r--   0        0        0     3915 2023-07-23 18:15:50.766094 rec_spotify-1.1/rec_spotify/config.py
+-rw-r--r--   0        0        0      758 2023-07-23 15:35:03.891743 rec_spotify-1.1/rec_spotify/console.py
+-rw-r--r--   0        0        0     7310 2023-07-23 19:42:31.072891 rec_spotify-1.1/rec_spotify/database.py
+-rw-r--r--   0        0        0     6427 2023-07-23 15:53:09.981754 rec_spotify-1.1/rec_spotify/items.py
+-rw-r--r--   0        0        0     2195 2023-07-23 16:28:40.968471 rec_spotify-1.1/rec_spotify/lyrics.py
+-rw-r--r--   0        0        0     6405 2023-07-23 19:54:00.000154 rec_spotify-1.1/rec_spotify/manager.py
+-rw-r--r--   0        0        0     1968 2023-07-23 16:07:01.827794 rec_spotify-1.1/rec_spotify/messages.py
+-rw-r--r--   0        0        0     3317 2023-07-23 18:16:28.832707 rec_spotify-1.1/rec_spotify/recorder.py
+-rw-r--r--   0        0        0     5375 2023-07-23 17:02:19.699967 rec_spotify-1.1/rec_spotify/spotify.py
+-rw-r--r--   0        0        0     1457 2023-07-23 16:26:57.110938 rec_spotify-1.1/rec_spotify/utils.py
+-rw-r--r--   0        0        0     2709 1970-01-01 00:00:00.000000 rec_spotify-1.1/PKG-INFO
```

### Comparing `rec_spotify-1.0/pyproject.toml` & `rec_spotify-1.1/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "rec-spotify"
-version = "1.0"
+version = "1.1"
 description = "Record and sync Spotify tracks, albums, and playlists."
 repository = "https://github.com/oSeeLight/rec-spotify"
 authors = ["Jacov Rainz <oSeeLight@proton.me>"]
 license = "MIT"
 readme = "README.md"
 packages = [{include = "rec_spotify"}]
 include = ["README.md"]
```

### Comparing `rec_spotify-1.0/README.md` & `rec_spotify-1.1/README.md`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.0/rec_spotify/cli.py` & `rec_spotify-1.1/rec_spotify/cli.py`

 * *Files 0% similar despite different names*

```diff
@@ -26,23 +26,23 @@
     parser.add_argument(
         "-p",
         "--path",
         type=str,
         required=False,
         help="The output directory for saving recorded files",
     )
+
     args = parser.parse_args()
     manager = Manager()
     if args.url and args.path:
-        Config.MUSIC_DIR = args.path
         match = parse_spotify_url(args.url)
-
         if match is not None:
             link_type, id = match
             manager.init()
+            Config.MUSIC_DIR = args.path
             if link_type == "track":
                 track = Track(id)
                 manager.record_track(track)
             else:
                 collection = Collection(id, kind=link_type)
                 manager.record_collection(collection)
```

### Comparing `rec_spotify-1.0/rec_spotify/config.py` & `rec_spotify-1.1/rec_spotify/config.py`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.0/rec_spotify/console.py` & `rec_spotify-1.1/rec_spotify/console.py`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.0/rec_spotify/database.py` & `rec_spotify-1.1/rec_spotify/database.py`

 * *Files 1% similar despite different names*

```diff
@@ -9,14 +9,16 @@
 
 class Database(object):
     "Database class for working with tracks and playlists."
 
     _connection: sqlite3.Connection
     _cursor: sqlite3.Cursor
 
+    _init: bool = False
+
     CREATE_TABLES_SQL = """
         CREATE TABLE IF NOT EXISTS playlists (
             id TEXT PRIMARY KEY,
             name TEXT,
             dir_path TEXT
         );
         CREATE TABLE IF NOT EXISTS tracks (
@@ -38,14 +40,15 @@
 
         cls._connection = sqlite3.connect(Config.get_database_filepath())
         cls._cursor = cls._connection.cursor()
         cls._cursor.execute("PRAGMA foreign_keys = ON")
         cls._cursor.executescript(cls.CREATE_TABLES_SQL)
         cls._connection.commit()
         console.print(m.DATABASE_OK)
+        cls._init = True
 
     @classmethod
     def get_playlist(cls, id: str) -> t.Union[Collection, None]:
         "Get playlist by id, returns Collection object or None if not found"
         sql = "SELECT * FROM playlists WHERE id = ?;"
         cls._cursor.execute(sql, (id,))
         row = cls._cursor.fetchone()
@@ -189,9 +192,10 @@
         track.filepath = row[6]
         track.downloaded = bool(row[7])
         return track
 
     @classmethod
     def close(cls) -> None:
         "Close database connection"
-        cls._connection.commit()
-        cls._connection.close()
+        if cls._init:
+            cls._connection.commit()
+            cls._connection.close()
```

### Comparing `rec_spotify-1.0/rec_spotify/items.py` & `rec_spotify-1.1/rec_spotify/items.py`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.0/rec_spotify/lyrics.py` & `rec_spotify-1.1/rec_spotify/lyrics.py`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.0/rec_spotify/manager.py` & `rec_spotify-1.1/rec_spotify/manager.py`

 * *Files 1% similar despite different names*

```diff
@@ -109,14 +109,16 @@
         track = SpotifyClient.get_track(track)
         console.print(
             m.JOB_TYPE.format(
                 job_type="track",
                 name=track.title,
             )
         )
+        console.print()
+        console.rule(":radio: Recorder Log")
         cls._record_and_save(track)
 
     @classmethod
     def record_collection(cls, collection: Collection) -> None:
         "Record and save all tracks in a collection."
         collection = SpotifyClient.get_collection(collection)
         collection.create_dir()
@@ -151,15 +153,14 @@
             out_f=track.filepath,
             format=Config.AUDIO_FORMAT,
             codec="libmp3lame",
             parameters=["-b:a", "320k", "-abr", "1"],
             tags=metadata,
             cover=song_cover.name,
         )
-
         lyrics = Lyrics.find(track)
         if lyrics is not None:
             Lyrics.embed_lyrics(track, lyrics)
 
         os.remove(song_cover.name)
         console.print(m.TRACK_SAVED.format(filepath=track.filepath))
         console.print()
```

### Comparing `rec_spotify-1.0/rec_spotify/messages.py` & `rec_spotify-1.1/rec_spotify/messages.py`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.0/rec_spotify/recorder.py` & `rec_spotify-1.1/rec_spotify/recorder.py`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.0/rec_spotify/spotify.py` & `rec_spotify-1.1/rec_spotify/spotify.py`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.0/rec_spotify/utils.py` & `rec_spotify-1.1/rec_spotify/utils.py`

 * *Files identical despite different names*

### Comparing `rec_spotify-1.0/PKG-INFO` & `rec_spotify-1.1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: rec-spotify
-Version: 1.0
+Version: 1.1
 Summary: Record and sync Spotify tracks, albums, and playlists.
 Home-page: https://github.com/oSeeLight/rec-spotify
 License: MIT
 Keywords: spotify,record
 Author: Jacov Rainz
 Author-email: oSeeLight@proton.me
 Requires-Python: >=3.11,<4.0
```

