# Comparing `tmp/grrif_tools-0.8.0.tar.gz` & `tmp/grrif_tools-0.8.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "grrif_tools-0.8.0.tar", last modified: Sun Jul 23 15:54:21 2023, max compression
+gzip compressed data, was "grrif_tools-0.8.1.tar", last modified: Sun Jul 23 16:24:56 2023, max compression
```

## Comparing `grrif_tools-0.8.0.tar` & `grrif_tools-0.8.1.tar`

### file list

```diff
@@ -1,22 +1,22 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:54:21.463362 grrif_tools-0.8.0/
--rw-r--r--   0 runner    (1001) docker     (123)     1076 2023-07-23 15:54:10.000000 grrif_tools-0.8.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       18 2023-07-23 15:54:10.000000 grrif_tools-0.8.0/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     3329 2023-07-23 15:54:21.463362 grrif_tools-0.8.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1461 2023-07-23 15:54:10.000000 grrif_tools-0.8.0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:54:21.459362 grrif_tools-0.8.0/grrif_tools/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 15:54:10.000000 grrif_tools-0.8.0/grrif_tools/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7979 2023-07-23 15:54:10.000000 grrif_tools-0.8.0/grrif_tools/cli.py
--rw-r--r--   0 runner    (1001) docker     (123)     8073 2023-07-23 15:54:10.000000 grrif_tools-0.8.0/grrif_tools/grrif_archiver.py
--rw-r--r--   0 runner    (1001) docker     (123)     2531 2023-07-23 15:54:10.000000 grrif_tools-0.8.0/grrif_tools/grrif_player.py
--rw-r--r--   0 runner    (1001) docker     (123)     2391 2023-07-23 15:54:10.000000 grrif_tools-0.8.0/grrif_tools/grrif_scrobbler.py
--rw-r--r--   0 runner    (1001) docker     (123)      868 2023-07-23 15:54:10.000000 grrif_tools-0.8.0/grrif_tools/grrif_stats.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:54:21.463362 grrif_tools-0.8.0/grrif_tools.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     3329 2023-07-23 15:54:21.000000 grrif_tools-0.8.0/grrif_tools.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      424 2023-07-23 15:54:21.000000 grrif_tools-0.8.0/grrif_tools.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 15:54:21.000000 grrif_tools-0.8.0/grrif_tools.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       53 2023-07-23 15:54:21.000000 grrif_tools-0.8.0/grrif_tools.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)       71 2023-07-23 15:54:21.000000 grrif_tools-0.8.0/grrif_tools.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       12 2023-07-23 15:54:21.000000 grrif_tools-0.8.0/grrif_tools.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)      710 2023-07-23 15:54:10.000000 grrif_tools-0.8.0/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 15:54:21.463362 grrif_tools-0.8.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      912 2023-07-23 15:54:10.000000 grrif_tools-0.8.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:24:56.318163 grrif_tools-0.8.1/
+-rw-r--r--   0 runner    (1001) docker     (123)     1076 2023-07-23 16:24:50.000000 grrif_tools-0.8.1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       18 2023-07-23 16:24:50.000000 grrif_tools-0.8.1/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     3331 2023-07-23 16:24:56.318163 grrif_tools-0.8.1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1463 2023-07-23 16:24:50.000000 grrif_tools-0.8.1/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:24:56.314164 grrif_tools-0.8.1/grrif_tools/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 16:24:50.000000 grrif_tools-0.8.1/grrif_tools/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7979 2023-07-23 16:24:50.000000 grrif_tools-0.8.1/grrif_tools/cli.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8073 2023-07-23 16:24:50.000000 grrif_tools-0.8.1/grrif_tools/grrif_archiver.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2531 2023-07-23 16:24:50.000000 grrif_tools-0.8.1/grrif_tools/grrif_player.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2391 2023-07-23 16:24:50.000000 grrif_tools-0.8.1/grrif_tools/grrif_scrobbler.py
+-rw-r--r--   0 runner    (1001) docker     (123)      868 2023-07-23 16:24:50.000000 grrif_tools-0.8.1/grrif_tools/grrif_stats.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:24:56.318163 grrif_tools-0.8.1/grrif_tools.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     3331 2023-07-23 16:24:56.000000 grrif_tools-0.8.1/grrif_tools.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      424 2023-07-23 16:24:56.000000 grrif_tools-0.8.1/grrif_tools.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 16:24:56.000000 grrif_tools-0.8.1/grrif_tools.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       53 2023-07-23 16:24:56.000000 grrif_tools-0.8.1/grrif_tools.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       71 2023-07-23 16:24:56.000000 grrif_tools-0.8.1/grrif_tools.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       12 2023-07-23 16:24:56.000000 grrif_tools-0.8.1/grrif_tools.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      710 2023-07-23 16:24:50.000000 grrif_tools-0.8.1/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 16:24:56.318163 grrif_tools-0.8.1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      912 2023-07-23 16:24:50.000000 grrif_tools-0.8.1/setup.py
```

### Comparing `grrif_tools-0.8.0/LICENSE` & `grrif_tools-0.8.1/LICENSE`

 * *Files identical despite different names*

### Comparing `grrif_tools-0.8.0/PKG-INFO` & `grrif_tools-0.8.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: grrif_tools
-Version: 0.8.0
+Version: 0.8.1
 Summary: An unofficial set of tools for Cool Cats™.
 Home-page: https://github.com/fetzu/grrif-tools
 Download-URL: https://github.com/fetzu/grrif-tools/releases/latest
 Author: Julien 'fetzu' Bono
 License: MIT License
         
         Copyright (c) 2023 Julien 'fetzu' Bono
@@ -52,9 +52,9 @@
     play                Streams GRRIF to the console and displays the currently playing track.
     scrobble            Scrobble to Last.fm.
 
 options:
   -h, --help            show this help message and exit
   ```
   
-  **NOTE:** This package is unofficial and meant mostly as a playground to experiment with some new things (argparse, python packaging, etc...). Please do not DDoS GRRIF's website !
+  **NOTE:** This package is unofficial and meant mostly as a playground to experiment with some new things (argparse, python packaging, etc...). Please do not DDoS GRRIF's website !  
   **NOTE2:** Last.fm scrobbling is working and active while either streaming ("play") or using "scrobble start". This library will not handle authentification and requires some manual setup for last.fm's API access. Please create your own app on last.fm (https://www.last.fm/api/account/create) to get your API_KEY and API_SECRET, and see https://www.last.fm/api/authspec on how to get your SESSION_KEY (hint: it involves getting a token first and some md5 hashing).
```

### Comparing `grrif_tools-0.8.0/README.md` & `grrif_tools-0.8.1/README.md`

 * *Files 8% similar despite different names*

```diff
@@ -14,9 +14,9 @@
     play                Streams GRRIF to the console and displays the currently playing track.
     scrobble            Scrobble to Last.fm.
 
 options:
   -h, --help            show this help message and exit
   ```
   
-  **NOTE:** This package is unofficial and meant mostly as a playground to experiment with some new things (argparse, python packaging, etc...). Please do not DDoS GRRIF's website !
+  **NOTE:** This package is unofficial and meant mostly as a playground to experiment with some new things (argparse, python packaging, etc...). Please do not DDoS GRRIF's website !  
   **NOTE2:** Last.fm scrobbling is working and active while either streaming ("play") or using "scrobble start". This library will not handle authentification and requires some manual setup for last.fm's API access. Please create your own app on last.fm (https://www.last.fm/api/account/create) to get your API_KEY and API_SECRET, and see https://www.last.fm/api/authspec on how to get your SESSION_KEY (hint: it involves getting a token first and some md5 hashing).
```

### Comparing `grrif_tools-0.8.0/grrif_tools/cli.py` & `grrif_tools-0.8.1/grrif_tools/cli.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 ### [ GRRIF Tools by Julien 'fetzu' Bono ]
 ## [ IMPORTS ]
 import sys
 import argparse
 from datetime import date, datetime
 
 ## [ CONFIGURATION ]
-__version__ = "0.8.0"
+__version__ = "0.8.1"
 
 ## [ Is CLI even cooler with argparse? ]
 parser = argparse.ArgumentParser(
     description="A set of tools for Cool Cats™. Allows you to archive GRRIF's play history and scrobble it to last.fm (upcoming)."
 )
 
 subparsers = parser.add_subparsers(dest="command")
```

### Comparing `grrif_tools-0.8.0/grrif_tools/grrif_archiver.py` & `grrif_tools-0.8.1/grrif_tools/grrif_archiver.py`

 * *Files identical despite different names*

### Comparing `grrif_tools-0.8.0/grrif_tools/grrif_player.py` & `grrif_tools-0.8.1/grrif_tools/grrif_player.py`

 * *Files identical despite different names*

### Comparing `grrif_tools-0.8.0/grrif_tools/grrif_scrobbler.py` & `grrif_tools-0.8.1/grrif_tools/grrif_scrobbler.py`

 * *Files identical despite different names*

### Comparing `grrif_tools-0.8.0/grrif_tools/grrif_stats.py` & `grrif_tools-0.8.1/grrif_tools/grrif_stats.py`

 * *Files identical despite different names*

### Comparing `grrif_tools-0.8.0/grrif_tools.egg-info/PKG-INFO` & `grrif_tools-0.8.1/grrif_tools.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: grrif-tools
-Version: 0.8.0
+Version: 0.8.1
 Summary: An unofficial set of tools for Cool Cats™.
 Home-page: https://github.com/fetzu/grrif-tools
 Download-URL: https://github.com/fetzu/grrif-tools/releases/latest
 Author: Julien 'fetzu' Bono
 License: MIT License
         
         Copyright (c) 2023 Julien 'fetzu' Bono
@@ -52,9 +52,9 @@
     play                Streams GRRIF to the console and displays the currently playing track.
     scrobble            Scrobble to Last.fm.
 
 options:
   -h, --help            show this help message and exit
   ```
   
-  **NOTE:** This package is unofficial and meant mostly as a playground to experiment with some new things (argparse, python packaging, etc...). Please do not DDoS GRRIF's website !
+  **NOTE:** This package is unofficial and meant mostly as a playground to experiment with some new things (argparse, python packaging, etc...). Please do not DDoS GRRIF's website !  
   **NOTE2:** Last.fm scrobbling is working and active while either streaming ("play") or using "scrobble start". This library will not handle authentification and requires some manual setup for last.fm's API access. Please create your own app on last.fm (https://www.last.fm/api/account/create) to get your API_KEY and API_SECRET, and see https://www.last.fm/api/authspec on how to get your SESSION_KEY (hint: it involves getting a token first and some md5 hashing).
```

### Comparing `grrif_tools-0.8.0/pyproject.toml` & `grrif_tools-0.8.1/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [project]
 name = "grrif_tools"
-version = "0.8.0"
+version = "0.8.1"
 authors = [
   { name="Julien 'fetzu' Bono" },
 ]
 description = "An unofficial set of tools for Cool Cats™."
 readme = "README.md"
 license = {file = "LICENSE"}
 requires-python = ">=3.9"
```

### Comparing `grrif_tools-0.8.0/setup.py` & `grrif_tools-0.8.1/setup.py`

 * *Files 16% similar despite different names*

```diff
@@ -10,15 +10,15 @@
 setup(
     name="grrif_tools",
     description="An unofficial set of tools for Cool Cats™.",
     long_description=long_description,
     long_description_content_type="text/markdown",
     author="Julien 'fetzu' Bono",
     url="https://github.com/fetzu/grrif-tools",
-    version="0.8.0",
+    version="0.8.1",
     download_url="https://github.com/fetzu/grrif-tools/releases/latest",
     packages=find_packages(include=["grrif_tools", "grrif_tools.*"]),
     license="License :: OSI Approved :: MIT License",
     install_requires=[
         "Requests==2.31.0",
         "beautifulsoup4==4.12.2",
         "titlecase==2.4",
```

