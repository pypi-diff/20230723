# Comparing `tmp/audio_extract-0.3.2.tar.gz` & `tmp/audio_extract-0.4.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "audio_extract-0.3.2.tar", last modified: Mon Apr 24 06:55:18 2023, max compression
+gzip compressed data, was "audio_extract-0.4.0.tar", last modified: Sun Jul 23 14:28:09 2023, max compression
```

## Comparing `audio_extract-0.3.2.tar` & `audio_extract-0.4.0.tar`

### file list

```diff
@@ -1,20 +1,19 @@
-drwxrwxrwx   0        0        0        0 2023-04-24 06:55:18.064015 audio_extract-0.3.2/
--rw-rw-rw-   0        0        0     1090 2023-04-22 17:27:29.000000 audio_extract-0.3.2/LICENSE.md
--rw-rw-rw-   0        0        0     4420 2023-04-24 06:55:18.063016 audio_extract-0.3.2/PKG-INFO
--rw-rw-rw-   0        0        0     3505 2023-04-24 06:53:56.000000 audio_extract-0.3.2/README.md
-drwxrwxrwx   0        0        0        0 2023-04-24 06:55:18.016018 audio_extract-0.3.2/audio_extract/
--rw-rw-rw-   0        0        0     1723 2023-04-22 22:19:55.000000 audio_extract-0.3.2/audio_extract/__init__.py
--rw-rw-rw-   0        0        0      142 2023-04-22 18:09:12.000000 audio_extract-0.3.2/audio_extract/exceptions.py
--rw-rw-rw-   0        0        0     1123 2023-04-22 21:31:51.000000 audio_extract-0.3.2/audio_extract/execute.py
--rw-rw-rw-   0        0        0     1798 2023-04-22 21:45:01.000000 audio_extract-0.3.2/audio_extract/ffmpeg_tools.py
--rw-rw-rw-   0        0        0     1314 2023-04-22 22:19:05.000000 audio_extract-0.3.2/audio_extract/utils.py
--rw-rw-rw-   0        0        0     2859 2023-04-22 19:49:07.000000 audio_extract-0.3.2/audio_extract/validators.py
-drwxrwxrwx   0        0        0        0 2023-04-24 06:55:18.061015 audio_extract-0.3.2/audio_extract.egg-info/
--rw-rw-rw-   0        0        0     4420 2023-04-24 06:55:17.000000 audio_extract-0.3.2/audio_extract.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      413 2023-04-24 06:55:17.000000 audio_extract-0.3.2/audio_extract.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-04-24 06:55:17.000000 audio_extract-0.3.2/audio_extract.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       61 2023-04-24 06:55:17.000000 audio_extract-0.3.2/audio_extract.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0       86 2023-04-24 06:55:17.000000 audio_extract-0.3.2/audio_extract.egg-info/requires.txt
--rw-rw-rw-   0        0        0       14 2023-04-24 06:55:17.000000 audio_extract-0.3.2/audio_extract.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-04-24 06:55:18.064015 audio_extract-0.3.2/setup.cfg
--rw-rw-rw-   0        0        0     2460 2023-04-24 06:54:38.000000 audio_extract-0.3.2/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 14:28:09.846562 audio_extract-0.4.0/
+-rw-rw-rw-   0        0        0     1090 2023-07-23 12:21:48.000000 audio_extract-0.4.0/LICENSE.md
+-rw-rw-rw-   0        0        0     5567 2023-07-23 14:28:09.845492 audio_extract-0.4.0/PKG-INFO
+-rw-rw-rw-   0        0        0     4654 2023-07-23 14:27:02.000000 audio_extract-0.4.0/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 14:28:09.814720 audio_extract-0.4.0/audio_extract/
+-rw-rw-rw-   0        0        0       79 2023-07-23 13:07:18.000000 audio_extract-0.4.0/audio_extract/__init__.py
+-rw-rw-rw-   0        0        0     1760 2023-07-23 14:18:51.000000 audio_extract-0.4.0/audio_extract/execute.py
+-rw-rw-rw-   0        0        0     1467 2023-07-23 13:06:26.000000 audio_extract-0.4.0/audio_extract/ffmpeg.py
+-rw-rw-rw-   0        0        0     1054 2023-07-23 13:06:37.000000 audio_extract-0.4.0/audio_extract/utils.py
+-rw-rw-rw-   0        0        0     3943 2023-07-23 13:56:18.000000 audio_extract-0.4.0/audio_extract/validators.py
+drwxrwxrwx   0        0        0        0 2023-07-23 14:28:09.843657 audio_extract-0.4.0/audio_extract.egg-info/
+-rw-rw-rw-   0        0        0     5567 2023-07-23 14:28:09.000000 audio_extract-0.4.0/audio_extract.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      379 2023-07-23 14:28:09.000000 audio_extract-0.4.0/audio_extract.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 14:28:09.000000 audio_extract-0.4.0/audio_extract.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       61 2023-07-23 14:28:09.000000 audio_extract-0.4.0/audio_extract.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0       59 2023-07-23 14:28:09.000000 audio_extract-0.4.0/audio_extract.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       14 2023-07-23 14:28:09.000000 audio_extract-0.4.0/audio_extract.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 14:28:09.847013 audio_extract-0.4.0/setup.cfg
+-rw-rw-rw-   0        0        0     2416 2023-07-23 13:15:18.000000 audio_extract-0.4.0/setup.py
```

### Comparing `audio_extract-0.3.2/LICENSE.md` & `audio_extract-0.4.0/LICENSE.md`

 * *Files identical despite different names*

### Comparing `audio_extract-0.3.2/audio_extract/utils.py` & `audio_extract-0.4.0/audio_extract/utils.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,46 +1,33 @@
-import os
 import mutagen
-from colorama import Fore, Style
 
-os.system("color")
 
-
-def print_success(text: str):
-    print(f"{Fore.LIGHTGREEN_EX}{text}{Style.RESET_ALL}")
-
-
-def print_error(text: str):
-    print(f"{Fore.LIGHTRED_EX}{text}{Style.RESET_ALL}")
-
-
-def media_duration(path: str):
-    file = mutagen.File(path)
+def media_duration(file_path: str):
+    file = mutagen.File(file_path)
     duration = file.info.length
     return duration
 
 
 def seconds_to_hms(seconds: float | int) -> str:
     hours = int(seconds // 3600)
     minutes = int((seconds % 3600) // 60)
     seconds = int(seconds % 60)
     hms = "{:02d}:{:02d}:{:02d}".format(hours, minutes, seconds)
     return hms
 
 
-def hms_to_seconds(time_str) -> float | None:
+def hms_to_seconds(time_str: str) -> float:
     # Split the time string into hours, minutes, and seconds
     time_parts = time_str.split(':')
     if len(time_parts) == 3:  # HH:MM:SS format
         hours, minutes, seconds = map(int, time_parts)
     elif len(time_parts) == 2:  # MM:SS format
         hours = 0
         minutes, seconds = map(int, time_parts)
     else:
-        print_error("Invalid time format. Must be in HH:MM:SS or MM:SS format.")
-        return None
+        raise Exception("Invalid time format. Must be in HH:MM:SS or MM:SS format.")
 
     # Calculate the total number of seconds
     total_seconds = hours * 3600 + minutes * 60 + seconds
 
     # Return the total number of seconds as a float
     return float(total_seconds)
```

### Comparing `audio_extract-0.3.2/setup.py` & `audio_extract-0.4.0/setup.py`

 * *Files 4% similar despite different names*

```diff
@@ -29,27 +29,25 @@
 
         package_dir = Path(__file__).resolve().parent
         if str(package_dir) not in sys.path:
             sys.path.insert(0, str(package_dir))
 
 
 requires = [
-    "colorama>=0.4.6",
-    "ffmpeg>=1.4",
-    "imageio-ffmpeg>=0.4.8",
-    "mutagen>=1.46.0",
-    "py-file-type>=0.1.0",
+    "ffmpeg-python==0.2.0",
+    "imageio-ffmpeg==0.4.8",
+    "mutagen==1.46.0"
 ]
 
 long_description = open('README.md').read()
 long_description_content_type = 'text/markdown'
 
 setup(
     name='audio_extract',
-    version='0.3.2',
+    version='0.4.0',
     author='riad-azz',
     author_email='riadh.azzoun@hotmail.com',
     description='Extract and trim audio from videos or trim audios.',
     long_description=long_description,
     long_description_content_type=long_description_content_type,
     url='https://github.com/riad-azz/audio-extract',
     project_urls={
```

