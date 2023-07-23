# Comparing `tmp/SpotifyUtil-0.0.4.tar.gz` & `tmp/SpotifyUtil-0.0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "SpotifyUtil-0.0.4.tar", last modified: Sat Jul 22 17:33:22 2023, max compression
+gzip compressed data, was "SpotifyUtil-0.0.5.tar", last modified: Sun Jul 23 07:29:21 2023, max compression
```

## Comparing `SpotifyUtil-0.0.4.tar` & `SpotifyUtil-0.0.5.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxrwxrwx   0        0        0        0 2023-07-22 17:33:22.757367 SpotifyUtil-0.0.4/
--rw-rw-rw-   0        0        0    35823 2023-07-13 08:37:27.000000 SpotifyUtil-0.0.4/LICENSE
--rw-rw-rw-   0        0        0     2006 2023-07-22 17:33:22.755355 SpotifyUtil-0.0.4/PKG-INFO
--rw-rw-rw-   0        0        0     1284 2023-07-17 13:09:57.000000 SpotifyUtil-0.0.4/README.md
-drwxrwxrwx   0        0        0        0 2023-07-22 17:33:22.719359 SpotifyUtil-0.0.4/SpotifyUtil/
--rw-rw-rw-   0        0        0    16390 2023-07-22 17:32:32.000000 SpotifyUtil-0.0.4/SpotifyUtil/SpotifyUtil.py
--rw-rw-rw-   0        0        0      139 2023-07-18 16:53:30.000000 SpotifyUtil-0.0.4/SpotifyUtil/__init__.py
--rw-rw-rw-   0        0        0     1387 2023-07-17 18:50:45.000000 SpotifyUtil-0.0.4/SpotifyUtil/config.py
--rw-rw-rw-   0        0        0      262 2023-07-16 14:31:36.000000 SpotifyUtil-0.0.4/SpotifyUtil/file_reader.py
--rw-rw-rw-   0        0        0      157 2023-07-17 14:31:47.000000 SpotifyUtil-0.0.4/SpotifyUtil/secret.py
--rw-rw-rw-   0        0        0     1492 2023-07-22 14:08:57.000000 SpotifyUtil-0.0.4/SpotifyUtil/utilityTest.py
-drwxrwxrwx   0        0        0        0 2023-07-22 17:33:22.751362 SpotifyUtil-0.0.4/SpotifyUtil.egg-info/
--rw-rw-rw-   0        0        0     2006 2023-07-22 17:33:22.000000 SpotifyUtil-0.0.4/SpotifyUtil.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      364 2023-07-22 17:33:22.000000 SpotifyUtil-0.0.4/SpotifyUtil.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-22 17:33:22.000000 SpotifyUtil-0.0.4/SpotifyUtil.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        8 2023-07-22 17:33:22.000000 SpotifyUtil-0.0.4/SpotifyUtil.egg-info/requires.txt
--rw-rw-rw-   0        0        0       12 2023-07-22 17:33:22.000000 SpotifyUtil-0.0.4/SpotifyUtil.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      768 2023-07-22 14:01:32.000000 SpotifyUtil-0.0.4/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-07-22 17:33:22.758389 SpotifyUtil-0.0.4/setup.cfg
--rw-rw-rw-   0        0        0      962 2023-07-22 14:01:37.000000 SpotifyUtil-0.0.4/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 07:29:21.912008 SpotifyUtil-0.0.5/
+-rw-rw-rw-   0        0        0    35823 2023-07-13 08:37:27.000000 SpotifyUtil-0.0.5/LICENSE
+-rw-rw-rw-   0        0        0     2006 2023-07-23 07:29:21.906014 SpotifyUtil-0.0.5/PKG-INFO
+-rw-rw-rw-   0        0        0     1284 2023-07-17 13:09:57.000000 SpotifyUtil-0.0.5/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 07:29:21.854483 SpotifyUtil-0.0.5/SpotifyUtil/
+-rw-rw-rw-   0        0        0    16390 2023-07-23 07:29:00.000000 SpotifyUtil-0.0.5/SpotifyUtil/SpotifyUtil.py
+-rw-rw-rw-   0        0        0      139 2023-07-18 16:53:30.000000 SpotifyUtil-0.0.5/SpotifyUtil/__init__.py
+-rw-rw-rw-   0        0        0     1387 2023-07-17 18:50:45.000000 SpotifyUtil-0.0.5/SpotifyUtil/config.py
+-rw-rw-rw-   0        0        0      262 2023-07-16 14:31:36.000000 SpotifyUtil-0.0.5/SpotifyUtil/file_reader.py
+-rw-rw-rw-   0        0        0      157 2023-07-17 14:31:47.000000 SpotifyUtil-0.0.5/SpotifyUtil/secret.py
+-rw-rw-rw-   0        0        0     1594 2023-07-22 17:47:21.000000 SpotifyUtil-0.0.5/SpotifyUtil/utilityTest.py
+drwxrwxrwx   0        0        0        0 2023-07-23 07:29:21.902007 SpotifyUtil-0.0.5/SpotifyUtil.egg-info/
+-rw-rw-rw-   0        0        0     2006 2023-07-23 07:29:21.000000 SpotifyUtil-0.0.5/SpotifyUtil.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      364 2023-07-23 07:29:21.000000 SpotifyUtil-0.0.5/SpotifyUtil.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 07:29:21.000000 SpotifyUtil-0.0.5/SpotifyUtil.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        8 2023-07-23 07:29:21.000000 SpotifyUtil-0.0.5/SpotifyUtil.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       12 2023-07-23 07:29:21.000000 SpotifyUtil-0.0.5/SpotifyUtil.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      768 2023-07-23 07:28:44.000000 SpotifyUtil-0.0.5/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-07-23 07:29:21.912008 SpotifyUtil-0.0.5/setup.cfg
+-rw-rw-rw-   0        0        0      962 2023-07-23 07:28:51.000000 SpotifyUtil-0.0.5/setup.py
```

### Comparing `SpotifyUtil-0.0.4/LICENSE` & `SpotifyUtil-0.0.5/LICENSE`

 * *Files identical despite different names*

### Comparing `SpotifyUtil-0.0.4/PKG-INFO` & `SpotifyUtil-0.0.5/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: SpotifyUtil
-Version: 0.0.4
+Version: 0.0.5
 Summary: SpotifyUtils is a very useful library made over Spotipy to automate some rather tiring tasks.
 Home-page: https://github.com/Arg0naut18/SpotifyUtil
 Author: Arg0naut18
 Author-email: Arg0naut18 <gaming.genos1729@gmail.com>
 Project-URL: Homepage, https://github.com/Arg0naut18/SpotifyUtil
 Keywords: Spotify,Spotipy,SpotifyUtil,SpotifyUtils
 Classifier: Programming Language :: Python :: 3
```

### Comparing `SpotifyUtil-0.0.4/README.md` & `SpotifyUtil-0.0.5/README.md`

 * *Files identical despite different names*

### Comparing `SpotifyUtil-0.0.4/SpotifyUtil/SpotifyUtil.py` & `SpotifyUtil-0.0.5/SpotifyUtil/SpotifyUtil.py`

 * *Files 0% similar despite different names*

```diff
@@ -122,15 +122,15 @@
             list2 = [track['uri'] for track in full_list2]
         set1 = set(list1)
         set2 = set(list2)
         if mode=="to_be_added":
             return list(set2.difference(set1))
         return list(set1.difference(set2))
     
-    def get_difference_multi(self, main, mode="to_be_added", *lists):
+    def get_difference_multi(self, main, *lists, mode="to_be_added"):
         result = set()
         if mode=="to_be_removed":
             return list(set(main).difference([set(li) for li in lists]))
         for li in lists:
             result = result.union(set(li).difference(set(main)))
         return list(result)
```

### Comparing `SpotifyUtil-0.0.4/SpotifyUtil/config.py` & `SpotifyUtil-0.0.5/SpotifyUtil/config.py`

 * *Files identical despite different names*

### Comparing `SpotifyUtil-0.0.4/SpotifyUtil/utilityTest.py` & `SpotifyUtil-0.0.5/SpotifyUtil/utilityTest.py`

 * *Files 18% similar despite different names*

```diff
@@ -23,17 +23,23 @@
 
 def get_diff(url1, url2):
     print(sp.get_different_tracks(url1, url2))
 
 def clear_p(url):
     sp.clear_playlist(url)
 
+def create_liked_songs_playlist(name, is_public):
+    sp.add_liked_songs_to_playlist(name=name, is_public=is_public)
+
 # main_url="https://open.spotify.com/playlist/269spiLROhagtO6WNUKHjP?si=f34822da6e6d43d5"
 source_url="https://open.spotify.com/playlist/6Ujd4z9JhEhBR5Bwr7pvsi?si=83bf130895264580"
 
-sp.add_liked_songs_to_playlist(name="Test Liked Songs", is_public=False)
+def test_test():
+    print(sp.test())
+
+test_test()
 
 # make_changes(main_url, source_url)
 # print("===============================================")
 # get_diff(main_url, source_url)
 # print("===============================================")
 # # clear_p(main_url)
```

### Comparing `SpotifyUtil-0.0.4/SpotifyUtil.egg-info/PKG-INFO` & `SpotifyUtil-0.0.5/SpotifyUtil.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: SpotifyUtil
-Version: 0.0.4
+Version: 0.0.5
 Summary: SpotifyUtils is a very useful library made over Spotipy to automate some rather tiring tasks.
 Home-page: https://github.com/Arg0naut18/SpotifyUtil
 Author: Arg0naut18
 Author-email: Arg0naut18 <gaming.genos1729@gmail.com>
 Project-URL: Homepage, https://github.com/Arg0naut18/SpotifyUtil
 Keywords: Spotify,Spotipy,SpotifyUtil,SpotifyUtils
 Classifier: Programming Language :: Python :: 3
```

### Comparing `SpotifyUtil-0.0.4/pyproject.toml` & `SpotifyUtil-0.0.5/pyproject.toml`

 * *Files 14% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [project]
 name = "SpotifyUtil"
-version = "0.0.4"
+version = "0.0.5"
 authors = [
     { name="Arg0naut18", email="gaming.genos1729@gmail.com" },
 ]
 description = "SpotifyUtils is a very useful library made over Spotipy to automate some rather tiring tasks."
 readme = "README.md"
 requires-python = ">=3.8"
 classifiers = [
```

### Comparing `SpotifyUtil-0.0.4/setup.py` & `SpotifyUtil-0.0.5/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import setuptools
 
 with open("README.md", "r", encoding="utf-8", errors="ignore") as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="SpotifyUtil",
-    version="0.0.4",
+    version="0.0.5",
     author="Arg0naut18",
     description="SpotifyUtils is a very useful library made over Spotipy to automate some rather tiring tasks.",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/Arg0naut18/SpotifyUtil",
     packages=setuptools.find_packages(),
     classifiers=[
```

