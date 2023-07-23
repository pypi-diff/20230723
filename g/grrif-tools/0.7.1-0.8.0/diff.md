# Comparing `tmp/grrif_tools-0.7.1.tar.gz` & `tmp/grrif_tools-0.8.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "grrif_tools-0.7.1.tar", last modified: Sat Jun 10 16:08:02 2023, max compression
+gzip compressed data, was "grrif_tools-0.8.0.tar", last modified: Sun Jul 23 15:54:21 2023, max compression
```

## Comparing `grrif_tools-0.7.1.tar` & `grrif_tools-0.8.0.tar`

### file list

```diff
@@ -1,22 +1,22 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-10 16:08:02.861634 grrif_tools-0.7.1/
--rw-r--r--   0 runner    (1001) docker     (123)     1076 2023-06-10 16:07:54.000000 grrif_tools-0.7.1/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       18 2023-06-10 16:07:54.000000 grrif_tools-0.7.1/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     2876 2023-06-10 16:08:02.861634 grrif_tools-0.7.1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1008 2023-06-10 16:07:54.000000 grrif_tools-0.7.1/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-10 16:08:02.861634 grrif_tools-0.7.1/grrif_tools/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-10 16:07:54.000000 grrif_tools-0.7.1/grrif_tools/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6948 2023-06-10 16:07:54.000000 grrif_tools-0.7.1/grrif_tools/cli.py
--rw-r--r--   0 runner    (1001) docker     (123)     8073 2023-06-10 16:07:54.000000 grrif_tools-0.7.1/grrif_tools/grrif_archiver.py
--rw-r--r--   0 runner    (1001) docker     (123)     2538 2023-06-10 16:07:54.000000 grrif_tools-0.7.1/grrif_tools/grrif_player.py
--rw-r--r--   0 runner    (1001) docker     (123)      915 2023-06-10 16:07:54.000000 grrif_tools-0.7.1/grrif_tools/grrif_scrobbler.py
--rw-r--r--   0 runner    (1001) docker     (123)      868 2023-06-10 16:07:54.000000 grrif_tools-0.7.1/grrif_tools/grrif_stats.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-10 16:08:02.861634 grrif_tools-0.7.1/grrif_tools.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2876 2023-06-10 16:08:02.000000 grrif_tools-0.7.1/grrif_tools.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      424 2023-06-10 16:08:02.000000 grrif_tools-0.7.1/grrif_tools.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-06-10 16:08:02.000000 grrif_tools-0.7.1/grrif_tools.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       53 2023-06-10 16:08:02.000000 grrif_tools-0.7.1/grrif_tools.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)       71 2023-06-10 16:08:02.000000 grrif_tools-0.7.1/grrif_tools.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       12 2023-06-10 16:08:02.000000 grrif_tools-0.7.1/grrif_tools.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)      710 2023-06-10 16:07:54.000000 grrif_tools-0.7.1/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-06-10 16:08:02.861634 grrif_tools-0.7.1/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      912 2023-06-10 16:07:54.000000 grrif_tools-0.7.1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:54:21.463362 grrif_tools-0.8.0/
+-rw-r--r--   0 runner    (1001) docker     (123)     1076 2023-07-23 15:54:10.000000 grrif_tools-0.8.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       18 2023-07-23 15:54:10.000000 grrif_tools-0.8.0/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     3329 2023-07-23 15:54:21.463362 grrif_tools-0.8.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1461 2023-07-23 15:54:10.000000 grrif_tools-0.8.0/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:54:21.459362 grrif_tools-0.8.0/grrif_tools/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 15:54:10.000000 grrif_tools-0.8.0/grrif_tools/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7979 2023-07-23 15:54:10.000000 grrif_tools-0.8.0/grrif_tools/cli.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8073 2023-07-23 15:54:10.000000 grrif_tools-0.8.0/grrif_tools/grrif_archiver.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2531 2023-07-23 15:54:10.000000 grrif_tools-0.8.0/grrif_tools/grrif_player.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2391 2023-07-23 15:54:10.000000 grrif_tools-0.8.0/grrif_tools/grrif_scrobbler.py
+-rw-r--r--   0 runner    (1001) docker     (123)      868 2023-07-23 15:54:10.000000 grrif_tools-0.8.0/grrif_tools/grrif_stats.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:54:21.463362 grrif_tools-0.8.0/grrif_tools.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     3329 2023-07-23 15:54:21.000000 grrif_tools-0.8.0/grrif_tools.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      424 2023-07-23 15:54:21.000000 grrif_tools-0.8.0/grrif_tools.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 15:54:21.000000 grrif_tools-0.8.0/grrif_tools.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       53 2023-07-23 15:54:21.000000 grrif_tools-0.8.0/grrif_tools.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       71 2023-07-23 15:54:21.000000 grrif_tools-0.8.0/grrif_tools.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       12 2023-07-23 15:54:21.000000 grrif_tools-0.8.0/grrif_tools.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      710 2023-07-23 15:54:10.000000 grrif_tools-0.8.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 15:54:21.463362 grrif_tools-0.8.0/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      912 2023-07-23 15:54:10.000000 grrif_tools-0.8.0/setup.py
```

### Comparing `grrif_tools-0.7.1/LICENSE` & `grrif_tools-0.8.0/LICENSE`

 * *Files identical despite different names*

### Comparing `grrif_tools-0.7.1/PKG-INFO` & `grrif_tools-0.8.0/PKG-INFO`

 * *Files 10% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: grrif_tools
-Version: 0.7.1
+Version: 0.8.0
 Summary: An unofficial set of tools for Cool Cats™.
 Home-page: https://github.com/fetzu/grrif-tools
 Download-URL: https://github.com/fetzu/grrif-tools/releases/latest
 Author: Julien 'fetzu' Bono
 License: MIT License
         
         Copyright (c) 2023 Julien 'fetzu' Bono
@@ -34,15 +34,15 @@
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.9
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # GRRIF Tools
 
-A set of tools for Cool Cats™. Allows you to archive GRRIF's play history to a SQLite database (or text files), compute/display some stats (top 10/25/100 artists and tracks), stream the radio live in your console,~~and scrobble it to last.fm~~ (upcoming).
+A set of tools for Cool Cats™. Allows you to archive GRRIF's play history to a SQLite database (or text files), compute/display some stats (top 10/25/100 artists and tracks), stream the radio live in your console, and scrobble it to last.fm.
 
 ```
 usage: grrif_tools [-h] {archive,stats,scrobble} ...
 
 A set of tools for Cool Cats™. Allows you to archive GRRIF's play history and scrobble it to last.fm (upcoming).
 
 positional arguments:
@@ -53,7 +53,8 @@
     scrobble            Scrobble to Last.fm.
 
 options:
   -h, --help            show this help message and exit
   ```
   
   **NOTE:** This package is unofficial and meant mostly as a playground to experiment with some new things (argparse, python packaging, etc...). Please do not DDoS GRRIF's website !
+  **NOTE2:** Last.fm scrobbling is working and active while either streaming ("play") or using "scrobble start". This library will not handle authentification and requires some manual setup for last.fm's API access. Please create your own app on last.fm (https://www.last.fm/api/account/create) to get your API_KEY and API_SECRET, and see https://www.last.fm/api/authspec on how to get your SESSION_KEY (hint: it involves getting a token first and some md5 hashing).
```

### Comparing `grrif_tools-0.7.1/grrif_tools/cli.py` & `grrif_tools-0.8.0/grrif_tools/cli.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 ### [ GRRIF Tools by Julien 'fetzu' Bono ]
 ## [ IMPORTS ]
 import sys
 import argparse
 from datetime import date, datetime
 
 ## [ CONFIGURATION ]
-__version__ = "0.7.1"
+__version__ = "0.8.0"
 
 ## [ Is CLI even cooler with argparse? ]
 parser = argparse.ArgumentParser(
     description="A set of tools for Cool Cats™. Allows you to archive GRRIF's play history and scrobble it to last.fm (upcoming)."
 )
 
 subparsers = parser.add_subparsers(dest="command")
@@ -76,27 +76,40 @@
     help=f"Specify the start date for the stats in YYYY-MM-DD format. Defaults to today ({date.today().strftime('%Y-%m-%d')}).",
 )
 
 scrobble_parser = subparsers.add_parser(
     "scrobble",
     help="Scrobble to Last.fm.",
 )
-scrobble_parser.add_argument(
-    "from_date",
-    nargs="?",
-    default="2021-01-01",
-    help="Specify the start date for the archive in YYYY-MM-DD format. Defaults to 2021-01-01.",
+scrobble_subparsers = scrobble_parser.add_subparsers(dest="scrobble_command")
+
+settings_parser = scrobble_subparsers.add_parser(
+    "settings", help="Set your last.fm scrobbling settings"
 )
-scrobble_parser.add_argument(
-    "to_date",
-    nargs="?",
-    default=date.today().strftime("%Y-%m-%d"),
-    help=f"Specify the start date for the archive in YYYY-MM-DD format. Defaults to today ({date.today().strftime('%Y-%m-%d')}).",
+settings_parser.add_argument(
+    "API_KEY",
+    type=str,
+    help="Your last.fm API Key",
+)
+settings_parser.add_argument(
+    "API_SECRET",
+    type=str,
+    help="Your last.fm API secret",
+)
+settings_parser.add_argument(
+    "SESSION_KEY",
+    type=str,
+    help="Your last.fm API session key",
 )
 
+livescrobble_parser = scrobble_subparsers.add_parser(
+    "start", help="Start scrobbling to last.fm now."
+)
+
+
 stream_parser = subparsers.add_parser(
     "play",
     help="Play GRRIF in your terminal!",
 ).add_argument(
     "quality",
     choices=["mp3_high", "mp3_low", "aac_high"],
     nargs="?",
@@ -188,13 +201,29 @@
             if args.topofthepop == "top25":
                 topofthepop("artist, title", "25", START_DATE, END_DATE)
             if args.topofthepop == "top100":
                 topofthepop("title", "100", START_DATE, END_DATE)
 
     # Scrobble was passed !
     if args.command == "scrobble":
-        print("Uh-oh, this doesn't exist yet!")
+
+        if args.scrobble_command == "settings":
+            if args.API_KEY is not None and args.API_SECRET is not None and args.SESSION_KEY is not None:
+                # Write the settings to file
+                import os
+                current_path = os.path.dirname(os.path.abspath(__file__))
+                settings_path = os.path.join(current_path, "grrif_secrets.py")
+                settings_content = f"API_KEY = '{args.API_KEY}'\nAPI_SECRET = '{args.API_SECRET}'\nSESSION_KEY = '{args.SESSION_KEY}'\n"
+                with open(settings_path, "w") as settings_file:
+                    settings_file.write(settings_content)
+            else:
+                print("Invalid number of arguments passed, API Key, API Secret and Session Key are needed.")
+
+        if args.scrobble_command == "start":
+            from .grrif_scrobbler import start_scrobbling
+            start_scrobbling("0")
 
     # Play was passed !
     if args.command == "play":
         from .grrif_player import start_playback
         start_playback(args.quality)
+
```

### Comparing `grrif_tools-0.7.1/grrif_tools/grrif_archiver.py` & `grrif_tools-0.8.0/grrif_tools/grrif_archiver.py`

 * *Files identical despite different names*

### Comparing `grrif_tools-0.7.1/grrif_tools/grrif_player.py` & `grrif_tools-0.8.0/grrif_tools/grrif_player.py`

 * *Files 2% similar despite different names*

```diff
@@ -56,25 +56,25 @@
 
     if quality == "mp3_high":
         url = "https://grrif.ice.infomaniak.ch/grrif-high.mp3"
     elif quality == "mp3_low":
         url = "https://grrif.ice.infomaniak.ch/grrif-48.mp3"
     elif quality == "aac_high":
         url = "https://grrif.ice.infomaniak.ch/grrif-128.aac"
-    
+
     if not os.path.exists(buffer_file):
         open(buffer_file, 'w').close()  # Create an empty file if it doesn't exist
         time.sleep(1) # Give the OS a little time to create the file before writing to it
 
     stream_thread = threading.Thread(target=stream_and_write, args=(url, buffer_file, max_file_size, stop_event))
     stream_thread.start()
-    
+
     play_thread = threading.Thread(target=play_stream, args=(buffer_file, stop_event))
     play_thread.start()
 
     # Wait for both threads to complete
     stream_thread.join()
     play_thread.join()
 
     # Delete the buffer file
     if os.path.exists(buffer_file):
-        os.remove(buffer_file)
+        os.remove(buffer_file)
```

### Comparing `grrif_tools-0.7.1/grrif_tools/grrif_stats.py` & `grrif_tools-0.8.0/grrif_tools/grrif_stats.py`

 * *Files identical despite different names*

### Comparing `grrif_tools-0.7.1/grrif_tools.egg-info/PKG-INFO` & `grrif_tools-0.8.0/grrif_tools.egg-info/PKG-INFO`

 * *Files 10% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: grrif-tools
-Version: 0.7.1
+Version: 0.8.0
 Summary: An unofficial set of tools for Cool Cats™.
 Home-page: https://github.com/fetzu/grrif-tools
 Download-URL: https://github.com/fetzu/grrif-tools/releases/latest
 Author: Julien 'fetzu' Bono
 License: MIT License
         
         Copyright (c) 2023 Julien 'fetzu' Bono
@@ -34,15 +34,15 @@
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.9
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # GRRIF Tools
 
-A set of tools for Cool Cats™. Allows you to archive GRRIF's play history to a SQLite database (or text files), compute/display some stats (top 10/25/100 artists and tracks), stream the radio live in your console,~~and scrobble it to last.fm~~ (upcoming).
+A set of tools for Cool Cats™. Allows you to archive GRRIF's play history to a SQLite database (or text files), compute/display some stats (top 10/25/100 artists and tracks), stream the radio live in your console, and scrobble it to last.fm.
 
 ```
 usage: grrif_tools [-h] {archive,stats,scrobble} ...
 
 A set of tools for Cool Cats™. Allows you to archive GRRIF's play history and scrobble it to last.fm (upcoming).
 
 positional arguments:
@@ -53,7 +53,8 @@
     scrobble            Scrobble to Last.fm.
 
 options:
   -h, --help            show this help message and exit
   ```
   
   **NOTE:** This package is unofficial and meant mostly as a playground to experiment with some new things (argparse, python packaging, etc...). Please do not DDoS GRRIF's website !
+  **NOTE2:** Last.fm scrobbling is working and active while either streaming ("play") or using "scrobble start". This library will not handle authentification and requires some manual setup for last.fm's API access. Please create your own app on last.fm (https://www.last.fm/api/account/create) to get your API_KEY and API_SECRET, and see https://www.last.fm/api/authspec on how to get your SESSION_KEY (hint: it involves getting a token first and some md5 hashing).
```

### Comparing `grrif_tools-0.7.1/pyproject.toml` & `grrif_tools-0.8.0/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [project]
 name = "grrif_tools"
-version = "0.7.1"
+version = "0.8.0"
 authors = [
   { name="Julien 'fetzu' Bono" },
 ]
 description = "An unofficial set of tools for Cool Cats™."
 readme = "README.md"
 license = {file = "LICENSE"}
 requires-python = ">=3.9"
```

### Comparing `grrif_tools-0.7.1/setup.py` & `grrif_tools-0.8.0/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -10,15 +10,15 @@
 setup(
     name="grrif_tools",
     description="An unofficial set of tools for Cool Cats™.",
     long_description=long_description,
     long_description_content_type="text/markdown",
     author="Julien 'fetzu' Bono",
     url="https://github.com/fetzu/grrif-tools",
-    version="0.7.1",
+    version="0.8.0",
     download_url="https://github.com/fetzu/grrif-tools/releases/latest",
     packages=find_packages(include=["grrif_tools", "grrif_tools.*"]),
     license="License :: OSI Approved :: MIT License",
     install_requires=[
         "Requests==2.31.0",
         "beautifulsoup4==4.12.2",
         "titlecase==2.4",
```

