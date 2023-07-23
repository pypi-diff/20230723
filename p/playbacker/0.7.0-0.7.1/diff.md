# Comparing `tmp/playbacker-0.7.0.tar.gz` & `tmp/playbacker-0.7.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "playbacker-0.7.0.tar", max compression
+gzip compressed data, was "playbacker-0.7.1.tar", max compression
```

## Comparing `playbacker-0.7.0.tar` & `playbacker-0.7.1.tar`

### file list

```diff
@@ -1,24 +1,24 @@
--rw-r--r--   0        0        0     1254 2023-07-22 06:54:02.513766 playbacker-0.7.0/pyproject.toml
--rw-r--r--   0        0        0        0 2023-07-22 06:53:31.345172 playbacker-0.7.0/src/playbacker/__init__.py
--rw-r--r--   0        0        0     5020 2023-07-22 06:53:31.345172 playbacker-0.7.0/src/playbacker/app.py
--rw-r--r--   0        0        0      527 2023-07-22 06:53:31.345172 playbacker-0.7.0/src/playbacker/config.py
--rw-r--r--   0        0        0        0 2023-07-22 06:53:31.345172 playbacker-0.7.0/src/playbacker/core/__init__.py
--rw-r--r--   0        0        0      850 2023-07-22 06:53:31.345172 playbacker-0.7.0/src/playbacker/core/audiofile.py
--rw-r--r--   0        0        0     1292 2023-07-22 06:53:31.345172 playbacker-0.7.0/src/playbacker/core/clock.py
--rw-r--r--   0        0        0     3423 2023-07-22 06:53:31.345172 playbacker-0.7.0/src/playbacker/core/playback.py
--rw-r--r--   0        0        0     1444 2023-07-22 06:53:31.345172 playbacker-0.7.0/src/playbacker/core/player.py
--rw-r--r--   0        0        0      974 2023-07-22 06:53:31.345172 playbacker-0.7.0/src/playbacker/core/setlist.py
--rw-r--r--   0        0        0     3497 2023-07-22 06:53:31.345172 playbacker-0.7.0/src/playbacker/core/settings.py
--rw-r--r--   0        0        0      892 2023-07-22 06:53:31.345172 playbacker-0.7.0/src/playbacker/core/song.py
--rw-r--r--   0        0        0     3137 2023-07-22 06:53:31.345172 playbacker-0.7.0/src/playbacker/core/stream.py
--rw-r--r--   0        0        0      765 2023-07-22 06:53:31.345172 playbacker-0.7.0/src/playbacker/core/tempo.py
--rw-r--r--   0        0        0     2607 2023-07-22 06:53:31.345172 playbacker-0.7.0/src/playbacker/core/track.py
--rw-r--r--   0        0        0        0 2023-07-22 06:53:31.345172 playbacker-0.7.0/src/playbacker/core/tracks/__init__.py
--rw-r--r--   0        0        0     2066 2023-07-22 06:53:31.345172 playbacker-0.7.0/src/playbacker/core/tracks/countdown.py
--rw-r--r--   0        0        0     2611 2023-07-22 06:53:31.345172 playbacker-0.7.0/src/playbacker/core/tracks/metronome.py
--rw-r--r--   0        0        0     1122 2023-07-22 06:53:31.345172 playbacker-0.7.0/src/playbacker/core/validate.py
--rw-r--r--   0        0        0    21934 2023-07-22 06:54:01.937755 playbacker-0.7.0/src/playbacker/dist/assets/index-04f532a9.js
--rw-r--r--   0        0        0     8295 2023-07-22 06:54:01.937755 playbacker-0.7.0/src/playbacker/dist/assets/index-c1f1d727.css
--rw-r--r--   0        0        0      388 2023-07-22 06:54:01.937755 playbacker-0.7.0/src/playbacker/dist/index.html
--rw-r--r--   0        0        0     2807 2023-07-22 06:53:31.345172 playbacker-0.7.0/src/playbacker/main.py
--rw-r--r--   0        0        0      762 1970-01-01 00:00:00.000000 playbacker-0.7.0/PKG-INFO
+-rw-r--r--   0        0        0     1254 2023-07-23 06:52:04.460126 playbacker-0.7.1/pyproject.toml
+-rw-r--r--   0        0        0        0 2023-07-23 06:51:35.828123 playbacker-0.7.1/src/playbacker/__init__.py
+-rw-r--r--   0        0        0     5020 2023-07-23 06:51:35.828123 playbacker-0.7.1/src/playbacker/app.py
+-rw-r--r--   0        0        0      527 2023-07-23 06:51:35.828123 playbacker-0.7.1/src/playbacker/config.py
+-rw-r--r--   0        0        0        0 2023-07-23 06:51:35.828123 playbacker-0.7.1/src/playbacker/core/__init__.py
+-rw-r--r--   0        0        0      850 2023-07-23 06:51:35.828123 playbacker-0.7.1/src/playbacker/core/audiofile.py
+-rw-r--r--   0        0        0     1292 2023-07-23 06:51:35.828123 playbacker-0.7.1/src/playbacker/core/clock.py
+-rw-r--r--   0        0        0     3423 2023-07-23 06:51:35.828123 playbacker-0.7.1/src/playbacker/core/playback.py
+-rw-r--r--   0        0        0     1444 2023-07-23 06:51:35.828123 playbacker-0.7.1/src/playbacker/core/player.py
+-rw-r--r--   0        0        0      974 2023-07-23 06:51:35.828123 playbacker-0.7.1/src/playbacker/core/setlist.py
+-rw-r--r--   0        0        0     3497 2023-07-23 06:51:35.828123 playbacker-0.7.1/src/playbacker/core/settings.py
+-rw-r--r--   0        0        0      892 2023-07-23 06:51:35.828123 playbacker-0.7.1/src/playbacker/core/song.py
+-rw-r--r--   0        0        0     3137 2023-07-23 06:51:35.828123 playbacker-0.7.1/src/playbacker/core/stream.py
+-rw-r--r--   0        0        0      765 2023-07-23 06:51:35.828123 playbacker-0.7.1/src/playbacker/core/tempo.py
+-rw-r--r--   0        0        0     2607 2023-07-23 06:51:35.828123 playbacker-0.7.1/src/playbacker/core/track.py
+-rw-r--r--   0        0        0        0 2023-07-23 06:51:35.828123 playbacker-0.7.1/src/playbacker/core/tracks/__init__.py
+-rw-r--r--   0        0        0     2066 2023-07-23 06:51:35.828123 playbacker-0.7.1/src/playbacker/core/tracks/countdown.py
+-rw-r--r--   0        0        0     2613 2023-07-23 06:51:35.828123 playbacker-0.7.1/src/playbacker/core/tracks/metronome.py
+-rw-r--r--   0        0        0     1122 2023-07-23 06:51:35.828123 playbacker-0.7.1/src/playbacker/core/validate.py
+-rw-r--r--   0        0        0    21934 2023-07-23 06:52:03.936126 playbacker-0.7.1/src/playbacker/dist/assets/index-04f532a9.js
+-rw-r--r--   0        0        0     8295 2023-07-23 06:52:03.936126 playbacker-0.7.1/src/playbacker/dist/assets/index-c1f1d727.css
+-rw-r--r--   0        0        0      388 2023-07-23 06:52:03.936126 playbacker-0.7.1/src/playbacker/dist/index.html
+-rw-r--r--   0        0        0     2807 2023-07-23 06:51:35.828123 playbacker-0.7.1/src/playbacker/main.py
+-rw-r--r--   0        0        0      762 1970-01-01 00:00:00.000000 playbacker-0.7.1/PKG-INFO
```

### Comparing `playbacker-0.7.0/pyproject.toml` & `playbacker-0.7.1/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "playbacker"
-version = "v0.7.0"
+version = "v0.7.1"
 description = "Live music performance playback"
 authors = ["Lev Vereshchagin <mail@vrslev.com>"]
 license = "MIT"
 # TODO: readme
 # readme = "../README.md"
 include = ["src/playbacker/dist/**/*"]
```

### Comparing `playbacker-0.7.0/src/playbacker/app.py` & `playbacker-0.7.1/src/playbacker/app.py`

 * *Files identical despite different names*

### Comparing `playbacker-0.7.0/src/playbacker/config.py` & `playbacker-0.7.1/src/playbacker/config.py`

 * *Files identical despite different names*

### Comparing `playbacker-0.7.0/src/playbacker/core/audiofile.py` & `playbacker-0.7.1/src/playbacker/core/audiofile.py`

 * *Files identical despite different names*

### Comparing `playbacker-0.7.0/src/playbacker/core/clock.py` & `playbacker-0.7.1/src/playbacker/core/clock.py`

 * *Files identical despite different names*

### Comparing `playbacker-0.7.0/src/playbacker/core/playback.py` & `playbacker-0.7.1/src/playbacker/core/playback.py`

 * *Files identical despite different names*

### Comparing `playbacker-0.7.0/src/playbacker/core/player.py` & `playbacker-0.7.1/src/playbacker/core/player.py`

 * *Files identical despite different names*

### Comparing `playbacker-0.7.0/src/playbacker/core/setlist.py` & `playbacker-0.7.1/src/playbacker/core/setlist.py`

 * *Files identical despite different names*

### Comparing `playbacker-0.7.0/src/playbacker/core/settings.py` & `playbacker-0.7.1/src/playbacker/core/settings.py`

 * *Files identical despite different names*

### Comparing `playbacker-0.7.0/src/playbacker/core/song.py` & `playbacker-0.7.1/src/playbacker/core/song.py`

 * *Files identical despite different names*

### Comparing `playbacker-0.7.0/src/playbacker/core/stream.py` & `playbacker-0.7.1/src/playbacker/core/stream.py`

 * *Files identical despite different names*

### Comparing `playbacker-0.7.0/src/playbacker/core/tempo.py` & `playbacker-0.7.1/src/playbacker/core/tempo.py`

 * *Files identical despite different names*

### Comparing `playbacker-0.7.0/src/playbacker/core/track.py` & `playbacker-0.7.1/src/playbacker/core/track.py`

 * *Files identical despite different names*

### Comparing `playbacker-0.7.0/src/playbacker/core/tracks/countdown.py` & `playbacker-0.7.1/src/playbacker/core/tracks/countdown.py`

 * *Files identical despite different names*

### Comparing `playbacker-0.7.0/src/playbacker/core/tracks/metronome.py` & `playbacker-0.7.1/src/playbacker/core/tracks/metronome.py`

 * *Files 0% similar despite different names*

```diff
@@ -42,15 +42,15 @@
     instruction: _Instruction
 
 
 metronome_schemes: dict[TimeSignature, dict[Duration, list[_Entry]]] = {
     "4/4": {
         "1/4": [_Entry(divider=4, instruction=4)],
         "1/8": [
-            _Entry(divider=16, instruction="accent"),
+            # _Entry(divider=16, instruction="accent"),
             _Entry(divider=4, instruction=4),
             _Entry(divider=2, instruction=8),
         ],
         "1/16": [
             _Entry(divider=4, instruction=4),
             _Entry(divider=2, instruction=8),
             _Entry(divider=1, instruction=16),
```

### Comparing `playbacker-0.7.0/src/playbacker/core/validate.py` & `playbacker-0.7.1/src/playbacker/core/validate.py`

 * *Files identical despite different names*

### Comparing `playbacker-0.7.0/src/playbacker/dist/assets/index-04f532a9.js` & `playbacker-0.7.1/src/playbacker/dist/assets/index-04f532a9.js`

 * *Files identical despite different names*

### Comparing `playbacker-0.7.0/src/playbacker/dist/assets/index-c1f1d727.css` & `playbacker-0.7.1/src/playbacker/dist/assets/index-c1f1d727.css`

 * *Files identical despite different names*

### Comparing `playbacker-0.7.0/src/playbacker/main.py` & `playbacker-0.7.1/src/playbacker/main.py`

 * *Files identical despite different names*

### Comparing `playbacker-0.7.0/PKG-INFO` & `playbacker-0.7.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: playbacker
-Version: 0.7.0
+Version: 0.7.1
 Summary: Live music performance playback
 License: MIT
 Author: Lev Vereshchagin
 Author-email: mail@vrslev.com
 Requires-Python: >=3.11,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
```

