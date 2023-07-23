# Comparing `tmp/gogo_cli-0.0.2.tar.gz` & `tmp/gogo_cli-0.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "gogo_cli-0.0.2.tar", max compression
+gzip compressed data, was "gogo_cli-0.0.3.tar", max compression
```

## Comparing `gogo_cli-0.0.2.tar` & `gogo_cli-0.0.3.tar`

### file list

```diff
@@ -1,13 +1,13 @@
--rw-r--r--   0        0        0    35149 2023-07-23 18:56:53.000675 gogo_cli-0.0.2/LICENSE
--rw-r--r--   0        0        0        0 2023-07-23 18:56:53.000675 gogo_cli-0.0.2/gogo_cli/__init__.py
--rw-r--r--   0        0        0      114 2023-07-23 18:56:53.000675 gogo_cli-0.0.2/gogo_cli/__main__.py
--rw-r--r--   0        0        0     3194 2023-07-23 18:56:53.000675 gogo_cli-0.0.2/gogo_cli/core/__gogo_cli__.py
--rw-r--r--   0        0        0        0 2023-07-23 18:56:53.000675 gogo_cli-0.0.2/gogo_cli/core/__init__.py
--rw-r--r--   0        0        0       19 2023-07-23 18:56:53.000675 gogo_cli-0.0.2/gogo_cli/core/__version__.py
--rw-r--r--   0        0        0      743 2023-07-23 18:56:53.000675 gogo_cli-0.0.2/gogo_cli/core/utils/__downloader__.py
--rw-r--r--   0        0        0        0 2023-07-23 18:56:53.000675 gogo_cli-0.0.2/gogo_cli/core/utils/__init__.py
--rw-r--r--   0        0        0      744 2023-07-23 18:56:53.000675 gogo_cli-0.0.2/gogo_cli/core/utils/__menu__.py
--rw-r--r--   0        0        0     1054 2023-07-23 18:56:53.000675 gogo_cli-0.0.2/gogo_cli/core/utils/__player__.py
--rw-r--r--   0        0        0      456 2023-07-23 18:56:53.000675 gogo_cli-0.0.2/pyproject.toml
--rw-r--r--   0        0        0        0 2023-07-23 18:56:53.000675 gogo_cli-0.0.2/readme.txt
--rw-r--r--   0        0        0      486 1970-01-01 00:00:00.000000 gogo_cli-0.0.2/PKG-INFO
+-rw-r--r--   0        0        0    35149 2023-07-23 19:20:41.719353 gogo_cli-0.0.3/LICENSE
+-rw-r--r--   0        0        0        0 2023-07-23 19:20:41.719353 gogo_cli-0.0.3/gogo_cli/__init__.py
+-rw-r--r--   0        0        0      114 2023-07-23 19:20:41.719353 gogo_cli-0.0.3/gogo_cli/__main__.py
+-rw-r--r--   0        0        0     2894 2023-07-23 19:20:41.719353 gogo_cli-0.0.3/gogo_cli/core/__gogo_cli__.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:20:41.719353 gogo_cli-0.0.3/gogo_cli/core/__init__.py
+-rw-r--r--   0        0        0       19 2023-07-23 19:20:41.719353 gogo_cli-0.0.3/gogo_cli/core/__version__.py
+-rw-r--r--   0        0        0      743 2023-07-23 19:20:41.719353 gogo_cli-0.0.3/gogo_cli/core/utils/__downloader__.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:20:41.719353 gogo_cli-0.0.3/gogo_cli/core/utils/__init__.py
+-rw-r--r--   0        0        0      744 2023-07-23 19:20:41.719353 gogo_cli-0.0.3/gogo_cli/core/utils/__menu__.py
+-rw-r--r--   0        0        0     1054 2023-07-23 19:20:41.719353 gogo_cli-0.0.3/gogo_cli/core/utils/__player__.py
+-rw-r--r--   0        0        0      456 2023-07-23 19:20:41.723353 gogo_cli-0.0.3/pyproject.toml
+-rw-r--r--   0        0        0        0 2023-07-23 19:20:41.723353 gogo_cli-0.0.3/readme.txt
+-rw-r--r--   0        0        0      486 1970-01-01 00:00:00.000000 gogo_cli-0.0.3/PKG-INFO
```

### Comparing `gogo_cli-0.0.2/LICENSE` & `gogo_cli-0.0.3/LICENSE`

 * *Files identical despite different names*

### Comparing `gogo_cli-0.0.2/gogo_cli/core/__gogo_cli__.py` & `gogo_cli-0.0.3/gogo_cli/core/__gogo_cli__.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,12 +1,13 @@
 import httpx
 
 import json
 import subprocess
 import sys
+import random
 
 from .utils.__player__ import play as pl
 from .utils.__downloader__ import download as dl
 from .utils.__menu__ import menu
 
 headers = {
     "User-Agent": "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.0.0 Safari/537.36 Edg/114.0.1823.82"
@@ -36,24 +37,14 @@
     query = " ".join(sys.argv[1:])
 
 query = query.replace(' ', '%20')
 
 url = f"https://api.consumet.org/anime/gogoanime/{query}"
 
 
-"""
-def play_next(anime, episode):
-    anime_url = f"https://api.consumet.org/anime/gogoanime/info/{anime}"
-    data = client.get(anime_url).text
-    parsed_data = json.loads(data)
-    total_episodes = parsed_data["totalEpisodes"]
-    new_episode = episode + 1
-    if episode > total_episodes:
-        exit(1)
-"""
 
 def play(anime, episode, playNext):
     if playNext == 1:
         episode = episode + 1
     play_url = f"https://api.consumet.org/anime/gogoanime/watch/{anime}-episode-{episode}"
     data = client.get(play_url, params = { "server": "gogocdn" },).text
     parsed_data = json.loads(data)
```

### Comparing `gogo_cli-0.0.2/gogo_cli/core/utils/__downloader__.py` & `gogo_cli-0.0.3/gogo_cli/core/utils/__downloader__.py`

 * *Files identical despite different names*

### Comparing `gogo_cli-0.0.2/gogo_cli/core/utils/__menu__.py` & `gogo_cli-0.0.3/gogo_cli/core/utils/__menu__.py`

 * *Files identical despite different names*

### Comparing `gogo_cli-0.0.2/gogo_cli/core/utils/__player__.py` & `gogo_cli-0.0.3/gogo_cli/core/utils/__player__.py`

 * *Files identical despite different names*

