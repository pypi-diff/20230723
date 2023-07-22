# Comparing `tmp/bergwerkapp-1.0.0.tar.gz` & `tmp/bergwerkapp-1.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "bergwerkapp-1.0.0.tar", last modified: Sat Jul 22 22:22:56 2023, max compression
+gzip compressed data, was "bergwerkapp-1.0.1.tar", last modified: Sat Jul 22 22:45:29 2023, max compression
```

## Comparing `bergwerkapp-1.0.0.tar` & `bergwerkapp-1.0.1.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxr-xr-x   0 zahnd      (501) staff       (20)        0 2023-07-22 22:22:56.801028 bergwerkapp-1.0.0/
--rw-r--r--   0 zahnd      (501) staff       (20)        0 2023-07-22 21:49:32.000000 bergwerkapp-1.0.0/LICENSE.txt
--rw-r--r--   0 zahnd      (501) staff       (20)      652 2023-07-22 22:22:56.801168 bergwerkapp-1.0.0/PKG-INFO
--rw-r--r--   0 zahnd      (501) staff       (20)       94 2023-07-22 22:06:01.000000 bergwerkapp-1.0.0/README.md
--rw-r--r--   0 zahnd      (501) staff       (20)        0 2023-07-22 21:49:49.000000 bergwerkapp-1.0.0/pyproject.toml
--rw-r--r--   0 zahnd      (501) staff       (20)      691 2023-07-22 22:22:56.801807 bergwerkapp-1.0.0/setup.cfg
-drwxr-xr-x   0 zahnd      (501) staff       (20)        0 2023-07-22 22:22:56.797444 bergwerkapp-1.0.0/src/
-drwxr-xr-x   0 zahnd      (501) staff       (20)        0 2023-07-22 22:22:56.800069 bergwerkapp-1.0.0/src/bergwerkapp.egg-info/
--rw-r--r--   0 zahnd      (501) staff       (20)      652 2023-07-22 22:22:56.000000 bergwerkapp-1.0.0/src/bergwerkapp.egg-info/PKG-INFO
--rw-r--r--   0 zahnd      (501) staff       (20)      249 2023-07-22 22:22:56.000000 bergwerkapp-1.0.0/src/bergwerkapp.egg-info/SOURCES.txt
--rw-r--r--   0 zahnd      (501) staff       (20)        1 2023-07-22 22:22:56.000000 bergwerkapp-1.0.0/src/bergwerkapp.egg-info/dependency_links.txt
--rw-r--r--   0 zahnd      (501) staff       (20)        7 2023-07-22 22:22:56.000000 bergwerkapp-1.0.0/src/bergwerkapp.egg-info/top_level.txt
-drwxr-xr-x   0 zahnd      (501) staff       (20)        0 2023-07-22 22:22:56.800716 bergwerkapp-1.0.0/src/indeed/
--rw-r--r--   0 zahnd      (501) staff       (20)        0 2023-07-22 21:32:31.000000 bergwerkapp-1.0.0/src/indeed/__init__.py
--rw-r--r--   0 zahnd      (501) staff       (20)     4319 2023-07-22 22:05:45.000000 bergwerkapp-1.0.0/src/indeed/functions.py
+drwxr-xr-x   0 zahnd      (501) staff       (20)        0 2023-07-22 22:45:29.432014 bergwerkapp-1.0.1/
+-rw-r--r--   0 zahnd      (501) staff       (20)        0 2023-07-22 21:49:32.000000 bergwerkapp-1.0.1/LICENSE.txt
+-rw-r--r--   0 zahnd      (501) staff       (20)      652 2023-07-22 22:45:29.432187 bergwerkapp-1.0.1/PKG-INFO
+-rw-r--r--   0 zahnd      (501) staff       (20)       94 2023-07-22 22:06:01.000000 bergwerkapp-1.0.1/README.md
+-rw-r--r--   0 zahnd      (501) staff       (20)        0 2023-07-22 21:49:49.000000 bergwerkapp-1.0.1/pyproject.toml
+-rw-r--r--   0 zahnd      (501) staff       (20)      691 2023-07-22 22:45:29.433029 bergwerkapp-1.0.1/setup.cfg
+drwxr-xr-x   0 zahnd      (501) staff       (20)        0 2023-07-22 22:45:29.426569 bergwerkapp-1.0.1/src/
+drwxr-xr-x   0 zahnd      (501) staff       (20)        0 2023-07-22 22:45:29.430469 bergwerkapp-1.0.1/src/bergwerkapp.egg-info/
+-rw-r--r--   0 zahnd      (501) staff       (20)      652 2023-07-22 22:45:29.000000 bergwerkapp-1.0.1/src/bergwerkapp.egg-info/PKG-INFO
+-rw-r--r--   0 zahnd      (501) staff       (20)      249 2023-07-22 22:45:29.000000 bergwerkapp-1.0.1/src/bergwerkapp.egg-info/SOURCES.txt
+-rw-r--r--   0 zahnd      (501) staff       (20)        1 2023-07-22 22:45:29.000000 bergwerkapp-1.0.1/src/bergwerkapp.egg-info/dependency_links.txt
+-rw-r--r--   0 zahnd      (501) staff       (20)        7 2023-07-22 22:45:29.000000 bergwerkapp-1.0.1/src/bergwerkapp.egg-info/top_level.txt
+drwxr-xr-x   0 zahnd      (501) staff       (20)        0 2023-07-22 22:45:29.431499 bergwerkapp-1.0.1/src/indeed/
+-rw-r--r--   0 zahnd      (501) staff       (20)        0 2023-07-22 21:32:31.000000 bergwerkapp-1.0.1/src/indeed/__init__.py
+-rw-r--r--   0 zahnd      (501) staff       (20)     4319 2023-07-22 22:44:53.000000 bergwerkapp-1.0.1/src/indeed/functions.py
```

### Comparing `bergwerkapp-1.0.0/PKG-INFO` & `bergwerkapp-1.0.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: bergwerkapp
-Version: 1.0.0
+Version: 1.0.1
 Summary: A package to be used for Bergwer Digital Experiences AG
 Home-page: https://github.com/bergwerk-li/bergwerkapp
 Author: Stefan Zahnd
 Author-email: szahnd@gmail.com
 Project-URL: Bug Tracker, https://github.com/bergwerk-li/bergwerkapp/-/issues
 Project-URL: repository, https://github.com/bergwerk-li/bergwerkapp
 Classifier: Programming Language :: Python :: 3
```

### Comparing `bergwerkapp-1.0.0/setup.cfg` & `bergwerkapp-1.0.1/setup.cfg`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = bergwerkapp
-version = 1.0.0
+version = 1.0.1
 author = Stefan Zahnd
 author_email = szahnd@gmail.com
 description = A package to be used for Bergwer Digital Experiences AG
 long_description = file: README.md, LICENSE.txt
 long_description_content_type = text/markdown
 url = https://github.com/bergwerk-li/bergwerkapp
 project_urls =
```

### Comparing `bergwerkapp-1.0.0/src/bergwerkapp.egg-info/PKG-INFO` & `bergwerkapp-1.0.1/src/bergwerkapp.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: bergwerkapp
-Version: 1.0.0
+Version: 1.0.1
 Summary: A package to be used for Bergwer Digital Experiences AG
 Home-page: https://github.com/bergwerk-li/bergwerkapp
 Author: Stefan Zahnd
 Author-email: szahnd@gmail.com
 Project-URL: Bug Tracker, https://github.com/bergwerk-li/bergwerkapp/-/issues
 Project-URL: repository, https://github.com/bergwerk-li/bergwerkapp
 Classifier: Programming Language :: Python :: 3
```

### Comparing `bergwerkapp-1.0.0/src/indeed/functions.py` & `bergwerkapp-1.0.1/src/indeed/functions.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 import googlemaps
 
-def getGeodataByAddress(location, components=None, google_key):
+def getGeodataByAddress(location, google_key, components=None):
   gmaps = googlemaps.Client(key=google_key)
   geocode_result = gmaps.geocode(location, language='de_DE', components=components)
   #print(geocode_result)
   if len(geocode_result) == 0:
     return{"type":"error","error":"Warning: Location \""+location+"\" not found. Continue but skipping job...\n"}
 
   for address in geocode_result:
```

