# Comparing `tmp/gogo_cli-0.0.1.tar.gz` & `tmp/gogo_cli-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "gogo_cli-0.0.1.tar", max compression
+gzip compressed data, was "gogo_cli-0.0.2.tar", max compression
```

## Comparing `gogo_cli-0.0.1.tar` & `gogo_cli-0.0.2.tar`

### file list

```diff
@@ -1,12 +1,13 @@
--rw-r--r--   0        0        0    35149 2023-07-23 18:06:36.852700 gogo_cli-0.0.1/LICENSE
--rw-r--r--   0        0        0        0 2023-07-23 18:06:36.852700 gogo_cli-0.0.1/gogo_cli/__init__.py
--rw-r--r--   0        0        0      114 2023-07-23 18:06:36.852700 gogo_cli-0.0.1/gogo_cli/__main__.py
--rw-r--r--   0        0        0     2948 2023-07-23 18:06:36.852700 gogo_cli-0.0.1/gogo_cli/core/__gogo_cli__.py
--rw-r--r--   0        0        0        0 2023-07-23 18:06:36.852700 gogo_cli-0.0.1/gogo_cli/core/__init__.py
--rw-r--r--   0        0        0       19 2023-07-23 18:06:36.852700 gogo_cli-0.0.1/gogo_cli/core/__version__.py
--rw-r--r--   0        0        0      743 2023-07-23 18:06:36.852700 gogo_cli-0.0.1/gogo_cli/core/utils/__downloader__.py
--rw-r--r--   0        0        0        0 2023-07-23 18:06:36.852700 gogo_cli-0.0.1/gogo_cli/core/utils/__init__.py
--rw-r--r--   0        0        0     1054 2023-07-23 18:06:36.852700 gogo_cli-0.0.1/gogo_cli/core/utils/__player__.py
--rw-r--r--   0        0        0      456 2023-07-23 18:06:36.852700 gogo_cli-0.0.1/pyproject.toml
--rw-r--r--   0        0        0        0 2023-07-23 18:06:36.852700 gogo_cli-0.0.1/readme.txt
--rw-r--r--   0        0        0      486 1970-01-01 00:00:00.000000 gogo_cli-0.0.1/PKG-INFO
+-rw-r--r--   0        0        0    35149 2023-07-23 18:56:53.000675 gogo_cli-0.0.2/LICENSE
+-rw-r--r--   0        0        0        0 2023-07-23 18:56:53.000675 gogo_cli-0.0.2/gogo_cli/__init__.py
+-rw-r--r--   0        0        0      114 2023-07-23 18:56:53.000675 gogo_cli-0.0.2/gogo_cli/__main__.py
+-rw-r--r--   0        0        0     3194 2023-07-23 18:56:53.000675 gogo_cli-0.0.2/gogo_cli/core/__gogo_cli__.py
+-rw-r--r--   0        0        0        0 2023-07-23 18:56:53.000675 gogo_cli-0.0.2/gogo_cli/core/__init__.py
+-rw-r--r--   0        0        0       19 2023-07-23 18:56:53.000675 gogo_cli-0.0.2/gogo_cli/core/__version__.py
+-rw-r--r--   0        0        0      743 2023-07-23 18:56:53.000675 gogo_cli-0.0.2/gogo_cli/core/utils/__downloader__.py
+-rw-r--r--   0        0        0        0 2023-07-23 18:56:53.000675 gogo_cli-0.0.2/gogo_cli/core/utils/__init__.py
+-rw-r--r--   0        0        0      744 2023-07-23 18:56:53.000675 gogo_cli-0.0.2/gogo_cli/core/utils/__menu__.py
+-rw-r--r--   0        0        0     1054 2023-07-23 18:56:53.000675 gogo_cli-0.0.2/gogo_cli/core/utils/__player__.py
+-rw-r--r--   0        0        0      456 2023-07-23 18:56:53.000675 gogo_cli-0.0.2/pyproject.toml
+-rw-r--r--   0        0        0        0 2023-07-23 18:56:53.000675 gogo_cli-0.0.2/readme.txt
+-rw-r--r--   0        0        0      486 1970-01-01 00:00:00.000000 gogo_cli-0.0.2/PKG-INFO
```

### Comparing `gogo_cli-0.0.1/LICENSE` & `gogo_cli-0.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `gogo_cli-0.0.1/gogo_cli/core/__gogo_cli__.py` & `gogo_cli-0.0.2/gogo_cli/core/__gogo_cli__.py`

 * *Files 23% similar despite different names*

```diff
@@ -2,14 +2,15 @@
 
 import json
 import subprocess
 import sys
 
 from .utils.__player__ import play as pl
 from .utils.__downloader__ import download as dl
+from .utils.__menu__ import menu
 
 headers = {
     "User-Agent": "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.0.0 Safari/537.36 Edg/114.0.1823.82"
 }
 
 client = httpx.Client(headers=headers, follow_redirects=True, timeout=None)
 
@@ -20,26 +21,43 @@
     "\u001b[34m",
     "\u001b[35m",
     "\u001b[36m",
     "\u001b[37m"
 ]
 
 if len(sys.argv) == 1:
-    query = input("Search: ")
-    if query == "":
-        print("ValueError: no query parameter provided")
-        exit(1)
+    try:
+        query = input("Search: ")
+        if query == "":
+            print("ValueError: no query parameter provided")
+            exit(1)
+    except KeyboardInterrupt:
+        exit(0)
 else:
     query = " ".join(sys.argv[1:])
 
 query = query.replace(' ', '%20')
 
 url = f"https://api.consumet.org/anime/gogoanime/{query}"
 
-def play(anime, episode):
+
+"""
+def play_next(anime, episode):
+    anime_url = f"https://api.consumet.org/anime/gogoanime/info/{anime}"
+    data = client.get(anime_url).text
+    parsed_data = json.loads(data)
+    total_episodes = parsed_data["totalEpisodes"]
+    new_episode = episode + 1
+    if episode > total_episodes:
+        exit(1)
+"""
+
+def play(anime, episode, playNext):
+    if playNext == 1:
+        episode = episode + 1
     play_url = f"https://api.consumet.org/anime/gogoanime/watch/{anime}-episode-{episode}"
     data = client.get(play_url, params = { "server": "gogocdn" },).text
     parsed_data = json.loads(data)
     referrer = parsed_data["headers"]["Referer"]
     quality_options = [source["quality"] for source in parsed_data["sources"]]
    
     if len(quality_options) > 1:
@@ -51,34 +69,27 @@
     
     if 1 <= ch <= len(quality_options):
         chosen_quality = quality_options[ch - 1]
     
     for source in parsed_data["sources"]:
         if source["quality"] == chosen_quality:
             #print(source["url"] + ' ' + referrer)
-            print("\n1. Play\n2. Download\n")
-            e = int(input(": "))
-            if e == 1:
-                pl(source["url"], referrer, anime, episode)
-            elif e == 2:
-                dl(anime, source["url"], referrer, episode)
-            else:
-                print("[!] Invalid option")
-                exit(1)
-
+            menu(source["url"], referrer, anime, episode)
+            
 def get_info(anime):
     info_url = f"https://api.consumet.org/anime/gogoanime/info/{anime}"
     data = client.get(info_url).text
     parsed_data = json.loads(data)
     total_episodes = parsed_data['totalEpisodes']
     if total_episodes > 1:
         ch = int(input(f"Total Episodes: {total_episodes}, Enter episode to play: "))
     else:
         ch = 1
-    uwu = play(anime, ch)
+    playNext = 0
+    uwu = play(anime, ch, playNext)
 
 def search():
     try:
         result = client.get(url).text
         parsed_data = json.loads(result)
         result_ids = [result['id'] for result in parsed_data['results']]
         for idx, result_id in enumerate(result_ids, start=1):
```

### Comparing `gogo_cli-0.0.1/gogo_cli/core/utils/__downloader__.py` & `gogo_cli-0.0.2/gogo_cli/core/utils/__downloader__.py`

 * *Files identical despite different names*

### Comparing `gogo_cli-0.0.1/gogo_cli/core/utils/__player__.py` & `gogo_cli-0.0.2/gogo_cli/core/utils/__player__.py`

 * *Files identical despite different names*

