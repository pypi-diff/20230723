# Comparing `tmp/fajrGPT-1.4.0.tar.gz` & `tmp/fajrGPT-1.4.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "fajrGPT-1.4.0.tar", last modified: Sat Jul 22 20:01:52 2023, max compression
+gzip compressed data, was "fajrGPT-1.4.1.tar", last modified: Sun Jul 23 17:40:10 2023, max compression
```

## Comparing `fajrGPT-1.4.0.tar` & `fajrGPT-1.4.1.tar`

### file list

```diff
@@ -1,17 +1,17 @@
-drwxr-xr-x   0 malek8     (501) staff       (20)        0 2023-07-22 20:01:52.617955 fajrGPT-1.4.0/
--rw-r--r--   0 malek8     (501) staff       (20)     1062 2023-05-15 07:44:33.000000 fajrGPT-1.4.0/LICENSE
--rw-r--r--   0 malek8     (501) staff       (20)     2946 2023-07-22 20:01:52.617698 fajrGPT-1.4.0/PKG-INFO
--rw-r--r--   0 malek8     (501) staff       (20)     2283 2023-06-12 00:59:24.000000 fajrGPT-1.4.0/README.md
-drwxr-xr-x   0 malek8     (501) staff       (20)        0 2023-07-22 20:01:52.615480 fajrGPT-1.4.0/fajrGPT/
--rw-r--r--   0 malek8     (501) staff       (20)        0 2023-06-12 01:14:16.000000 fajrGPT-1.4.0/fajrGPT/__init__.py
--rw-r--r--   0 malek8     (501) staff       (20)     1400 2023-07-03 14:08:35.000000 fajrGPT-1.4.0/fajrGPT/quran_metadata.py
--rw-r--r--   0 malek8     (501) staff       (20)    17026 2023-07-22 19:27:14.000000 fajrGPT-1.4.0/fajrGPT/wake.py
-drwxr-xr-x   0 malek8     (501) staff       (20)        0 2023-07-22 20:01:52.617421 fajrGPT-1.4.0/fajrGPT.egg-info/
--rw-r--r--   0 malek8     (501) staff       (20)     2946 2023-07-22 20:01:52.000000 fajrGPT-1.4.0/fajrGPT.egg-info/PKG-INFO
--rw-r--r--   0 malek8     (501) staff       (20)      276 2023-07-22 20:01:52.000000 fajrGPT-1.4.0/fajrGPT.egg-info/SOURCES.txt
--rw-r--r--   0 malek8     (501) staff       (20)        1 2023-07-22 20:01:52.000000 fajrGPT-1.4.0/fajrGPT.egg-info/dependency_links.txt
--rw-r--r--   0 malek8     (501) staff       (20)       46 2023-07-22 20:01:52.000000 fajrGPT-1.4.0/fajrGPT.egg-info/entry_points.txt
--rw-r--r--   0 malek8     (501) staff       (20)       54 2023-07-22 20:01:52.000000 fajrGPT-1.4.0/fajrGPT.egg-info/requires.txt
--rw-r--r--   0 malek8     (501) staff       (20)        8 2023-07-22 20:01:52.000000 fajrGPT-1.4.0/fajrGPT.egg-info/top_level.txt
--rw-r--r--   0 malek8     (501) staff       (20)       38 2023-07-22 20:01:52.618137 fajrGPT-1.4.0/setup.cfg
--rw-r--r--   0 malek8     (501) staff       (20)     1129 2023-07-22 19:57:46.000000 fajrGPT-1.4.0/setup.py
+drwxr-xr-x   0 malek8     (501) staff       (20)        0 2023-07-23 17:40:10.973710 fajrGPT-1.4.1/
+-rw-r--r--   0 malek8     (501) staff       (20)     1062 2023-05-15 07:44:33.000000 fajrGPT-1.4.1/LICENSE
+-rw-r--r--   0 malek8     (501) staff       (20)     2946 2023-07-23 17:40:10.973341 fajrGPT-1.4.1/PKG-INFO
+-rw-r--r--   0 malek8     (501) staff       (20)     2283 2023-06-12 00:59:24.000000 fajrGPT-1.4.1/README.md
+drwxr-xr-x   0 malek8     (501) staff       (20)        0 2023-07-23 17:40:10.968775 fajrGPT-1.4.1/fajrGPT/
+-rw-r--r--   0 malek8     (501) staff       (20)        0 2023-06-12 01:14:16.000000 fajrGPT-1.4.1/fajrGPT/__init__.py
+-rw-r--r--   0 malek8     (501) staff       (20)     1400 2023-07-03 14:08:35.000000 fajrGPT-1.4.1/fajrGPT/quran_metadata.py
+-rw-r--r--   0 malek8     (501) staff       (20)    18216 2023-07-23 17:35:37.000000 fajrGPT-1.4.1/fajrGPT/wake.py
+drwxr-xr-x   0 malek8     (501) staff       (20)        0 2023-07-23 17:40:10.972782 fajrGPT-1.4.1/fajrGPT.egg-info/
+-rw-r--r--   0 malek8     (501) staff       (20)     2946 2023-07-23 17:40:10.000000 fajrGPT-1.4.1/fajrGPT.egg-info/PKG-INFO
+-rw-r--r--   0 malek8     (501) staff       (20)      276 2023-07-23 17:40:10.000000 fajrGPT-1.4.1/fajrGPT.egg-info/SOURCES.txt
+-rw-r--r--   0 malek8     (501) staff       (20)        1 2023-07-23 17:40:10.000000 fajrGPT-1.4.1/fajrGPT.egg-info/dependency_links.txt
+-rw-r--r--   0 malek8     (501) staff       (20)       46 2023-07-23 17:40:10.000000 fajrGPT-1.4.1/fajrGPT.egg-info/entry_points.txt
+-rw-r--r--   0 malek8     (501) staff       (20)       54 2023-07-23 17:40:10.000000 fajrGPT-1.4.1/fajrGPT.egg-info/requires.txt
+-rw-r--r--   0 malek8     (501) staff       (20)        8 2023-07-23 17:40:10.000000 fajrGPT-1.4.1/fajrGPT.egg-info/top_level.txt
+-rw-r--r--   0 malek8     (501) staff       (20)       38 2023-07-23 17:40:10.973785 fajrGPT-1.4.1/setup.cfg
+-rw-r--r--   0 malek8     (501) staff       (20)     1129 2023-07-23 17:39:00.000000 fajrGPT-1.4.1/setup.py
```

### Comparing `fajrGPT-1.4.0/LICENSE` & `fajrGPT-1.4.1/LICENSE`

 * *Files identical despite different names*

### Comparing `fajrGPT-1.4.0/PKG-INFO` & `fajrGPT-1.4.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: fajrGPT
-Version: 1.4.0
+Version: 1.4.1
 Summary: A Python application to assist in waking up for Fajr prayer by providing 3 interactive verses/explanations from the Quran + ChatGPT explanations accompanied by a soothing Islamic prayer fade-in and fade-out audio file from YouTube.
 Home-page: https://github.com/malekinho8/quran-wake-up
 Author: Malek Ibrahim
 Author-email: shmeek8@gmail.com
 Classifier: Development Status :: 3 - Alpha
 Classifier: Topic :: Utilities
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `fajrGPT-1.4.0/README.md` & `fajrGPT-1.4.1/README.md`

 * *Files identical despite different names*

### Comparing `fajrGPT-1.4.0/fajrGPT/quran_metadata.py` & `fajrGPT-1.4.1/fajrGPT/quran_metadata.py`

 * *Files identical despite different names*

### Comparing `fajrGPT-1.4.0/fajrGPT/wake.py` & `fajrGPT-1.4.1/fajrGPT/wake.py`

 * *Files 4% similar despite different names*

```diff
@@ -15,34 +15,41 @@
 from tqdm import tqdm
 from Quran_Module import Project_Quran
 
 openai.api_key = os.getenv("OPENAI_API_KEY")
 COMPLETIONS_MODEL = "gpt-3.5-turbo"
 
 @click.command()
-@click.option('--url', required=True, help='YouTube video URL.')
+@click.option('--url', required=True, help='YouTube URL containing desired audio data.')
 @click.option('--time', required=True, help='Countdown time in format [number][h/m/s], i.e. 1h would create a 1 hour timer.')
 @click.option('--output', required=True, help='Name of the output file.')
 @click.option('--names-flag', required=False, help='Whether or not to include a randomly selected name of Allah in the preamble.', default=True)
+@click.option('--surah', required=False, help='Specific Surah from the Quran. Should be given as integer.')
 
-def main(url, time, output, names_flag):
-    # Download video
-    flag = download_video(url,output)
+def main(url, time, output, names_flag, surah=None):
+    # Check surah option
+    if surah:
+        # make the output file name the same as the surah
+        output = 'quran-' + '{:03d}'.format(int(surah))
+        flag = download_surah(surah, output)
+    else:
+        # Download video
+        flag = download_video(url, output)
 
     # test audio
     test_audio(f'{output}.mp3',output,flag)
 
     # convert time to seconds
     countdown_seconds = convert_to_seconds(time)
 
     # Start countdown
     countdown(countdown_seconds)
 
     # Play audio with fade-in effect on a separate thread
-    play_audio_thread = Thread(target=play_audio, args=(f'{output}.mp3',))
+    play_audio_thread = Thread(target=play_audio, args=(f'{output}.mp3',5))
     play_audio_thread.start()
 
     # display a name of Allah
     get_name_of_allah_and_explanation(names_flag)
 
     # stop the misharay audio once the user has finished reading the name of Allah on a separate thread
     stop_audio(5)
@@ -64,14 +71,38 @@
 
     # stop the audio once the user has completed reading the verses
     stop_audio()
 
     # return back to the main thread
     play_audio_thread.join()
 
+def download_surah(surah, output):
+    # obtain the number of verses in the surah
+    num_verses = quran_chapter_to_verse[int(surah)]
+    
+    # loop over all the verses in the surah and construct the urls
+    urls = [quran_verse_to_mp3_url(f'{surah}:{verse}') for verse in range(1,num_verses+1)]
+
+    # download the verse audio and sleep for 0.5 seconds between each download
+    file_paths = [download_file_and_sleep(url,0.5) for url in urls]
+
+    # combine the audio files
+    combined_audio = AudioSegment.empty()
+    for file_path in file_paths:
+        combined_audio += AudioSegment.from_mp3(file_path)
+    
+    # save the mp3 to the output file
+    combined_audio.export(f'{output}.mp3', format="mp3")
+
+    # delete the temporary files
+    for file_path in file_paths:
+        os.remove(file_path)
+
+    return True    
+
 def play_quran_verses_audio(verses,transition_time=0.5):
     # convert verses to urls
     urls = [quran_verse_to_mp3_url(verse) for verse in verses]
 
     # download the verse audio
     file_paths = [download_file_and_sleep(url,0.5) for url in urls]
```

### Comparing `fajrGPT-1.4.0/fajrGPT.egg-info/PKG-INFO` & `fajrGPT-1.4.1/fajrGPT.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: fajrGPT
-Version: 1.4.0
+Version: 1.4.1
 Summary: A Python application to assist in waking up for Fajr prayer by providing 3 interactive verses/explanations from the Quran + ChatGPT explanations accompanied by a soothing Islamic prayer fade-in and fade-out audio file from YouTube.
 Home-page: https://github.com/malekinho8/quran-wake-up
 Author: Malek Ibrahim
 Author-email: shmeek8@gmail.com
 Classifier: Development Status :: 3 - Alpha
 Classifier: Topic :: Utilities
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `fajrGPT-1.4.0/setup.py` & `fajrGPT-1.4.1/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name="fajrGPT",
-    version="1.4.0",
+    version="1.4.1",
     author="Malek Ibrahim",
     author_email="shmeek8@gmail.com",
     description=("A Python application to assist in waking up for Fajr prayer "
                  "by providing 3 interactive verses/explanations from the Quran + ChatGPT explanations "
                  "accompanied by a soothing Islamic prayer fade-in and fade-out audio file from YouTube."),
     long_description=open('README.md').read(),
     long_description_content_type='text/markdown',
```

