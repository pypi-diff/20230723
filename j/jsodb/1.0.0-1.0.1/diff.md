# Comparing `tmp/jsodb-1.0.0.tar.gz` & `tmp/jsodb-1.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "jsodb-1.0.0.tar", last modified: Sat Jul 22 18:56:33 2023, max compression
+gzip compressed data, was "jsodb-1.0.1.tar", last modified: Sun Jul 23 07:59:35 2023, max compression
```

## Comparing `jsodb-1.0.0.tar` & `jsodb-1.0.1.tar`

### file list

```diff
@@ -1,13 +1,13 @@
-drwxrwxrwx   0        0        0        0 2023-07-22 18:56:33.191203 jsodb-1.0.0/
--rw-rw-rw-   0        0        0     1059 2023-07-22 16:34:12.000000 jsodb-1.0.0/LICENSE
--rw-rw-rw-   0        0        0     1303 2023-07-22 18:56:33.190203 jsodb-1.0.0/PKG-INFO
--rw-rw-rw-   0        0        0      806 2023-07-22 18:04:29.000000 jsodb-1.0.0/README.md
--rw-rw-rw-   0        0        0      573 2023-07-22 18:06:32.000000 jsodb-1.0.0/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-07-22 18:56:33.192204 jsodb-1.0.0/setup.cfg
-drwxrwxrwx   0        0        0        0 2023-07-22 18:56:33.168205 jsodb-1.0.0/src/
--rw-rw-rw-   0        0        0      513 2023-07-22 18:04:30.000000 jsodb-1.0.0/src/jdb.py
-drwxrwxrwx   0        0        0        0 2023-07-22 18:56:33.188203 jsodb-1.0.0/src/jsodb.egg-info/
--rw-rw-rw-   0        0        0     1303 2023-07-22 18:56:33.000000 jsodb-1.0.0/src/jsodb.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      175 2023-07-22 18:56:33.000000 jsodb-1.0.0/src/jsodb.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-22 18:56:33.000000 jsodb-1.0.0/src/jsodb.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        4 2023-07-22 18:56:33.000000 jsodb-1.0.0/src/jsodb.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 07:59:35.848995 jsodb-1.0.1/
+-rw-rw-rw-   0        0        0     1059 2023-07-23 07:32:25.000000 jsodb-1.0.1/LICENSE
+-rw-rw-rw-   0        0        0     1314 2023-07-23 07:59:35.847994 jsodb-1.0.1/PKG-INFO
+-rw-rw-rw-   0        0        0      819 2023-07-23 07:32:25.000000 jsodb-1.0.1/README.md
+-rw-rw-rw-   0        0        0      573 2023-07-23 07:35:45.000000 jsodb-1.0.1/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-07-23 07:59:35.849993 jsodb-1.0.1/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-07-23 07:59:35.816991 jsodb-1.0.1/src/
+-rw-rw-rw-   0        0        0      495 2023-07-23 07:33:56.000000 jsodb-1.0.1/src/jdb.py
+drwxrwxrwx   0        0        0        0 2023-07-23 07:59:35.844993 jsodb-1.0.1/src/jsodb.egg-info/
+-rw-rw-rw-   0        0        0     1314 2023-07-23 07:59:35.000000 jsodb-1.0.1/src/jsodb.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      175 2023-07-23 07:59:35.000000 jsodb-1.0.1/src/jsodb.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 07:59:35.000000 jsodb-1.0.1/src/jsodb.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        4 2023-07-23 07:59:35.000000 jsodb-1.0.1/src/jsodb.egg-info/top_level.txt
```

### Comparing `jsodb-1.0.0/LICENSE` & `jsodb-1.0.1/LICENSE`

 * *Files identical despite different names*

### Comparing `jsodb-1.0.0/PKG-INFO` & `jsodb-1.0.1/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: jsodb
-Version: 1.0.0
+Version: 1.0.1
 Summary: simple json database lib
 Author-email: dttric <chudinovd222@gmail.com>
 Project-URL: Homepage, https://github.com/dttric/jsodb
 Project-URL: Bug Tracker, https://github.com/dttric/jsodb/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
@@ -17,15 +17,15 @@
 
 ### How to work with it?
 Instalation:
 `python3 -m pip install jsodb`
 
 Basic funcs:
 ```py
-import jdb
+from jsodb import jdb
 getkeyval("key") # returns key val
 addkey("key"=val) # adds keys to json
 changekey("key", val) # changes key to new val
 createjson("/path/to/file") # new .json file (without decorator)
 @json("/path/to/file") # main decorator
 ```
```

### Comparing `jsodb-1.0.0/README.md` & `jsodb-1.0.1/README.md`

 * *Files 16% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 
 ### How to work with it?
 Instalation:
 `python3 -m pip install jsodb`
 
 Basic funcs:
 ```py
-import jdb
+from jsodb import jdb
 getkeyval("key") # returns key val
 addkey("key"=val) # adds keys to json
 changekey("key", val) # changes key to new val
 createjson("/path/to/file") # new .json file (without decorator)
 @json("/path/to/file") # main decorator
 ```
 
@@ -27,8 +27,8 @@
 	print(f"{getkeyval(balance)}\n{getkeyval(deposit)}")
 	"""
 	10
 	100
 	"""
 
 func() ### changes applied
-```
+```
```

### Comparing `jsodb-1.0.0/pyproject.toml` & `jsodb-1.0.1/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 [project]
 name = "jsodb"
-version = "1.0.0"
+version = "1.0.1"
 authors = [
   { name="dttric", email="chudinovd222@gmail.com" },
 ]
 description = "simple json database lib"
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = [
```

### Comparing `jsodb-1.0.0/src/jsodb.egg-info/PKG-INFO` & `jsodb-1.0.1/src/jsodb.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: jsodb
-Version: 1.0.0
+Version: 1.0.1
 Summary: simple json database lib
 Author-email: dttric <chudinovd222@gmail.com>
 Project-URL: Homepage, https://github.com/dttric/jsodb
 Project-URL: Bug Tracker, https://github.com/dttric/jsodb/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
@@ -17,15 +17,15 @@
 
 ### How to work with it?
 Instalation:
 `python3 -m pip install jsodb`
 
 Basic funcs:
 ```py
-import jdb
+from jsodb import jdb
 getkeyval("key") # returns key val
 addkey("key"=val) # adds keys to json
 changekey("key", val) # changes key to new val
 createjson("/path/to/file") # new .json file (without decorator)
 @json("/path/to/file") # main decorator
 ```
```

