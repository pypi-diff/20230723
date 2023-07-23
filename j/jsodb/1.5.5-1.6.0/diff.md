# Comparing `tmp/jsodb-1.5.5.tar.gz` & `tmp/jsodb-1.6.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "jsodb-1.5.5.tar", last modified: Sun Jul 23 12:50:00 2023, max compression
+gzip compressed data, was "jsodb-1.6.0.tar", last modified: Sun Jul 23 14:30:50 2023, max compression
```

## Comparing `jsodb-1.5.5.tar` & `jsodb-1.6.0.tar`

### file list

```diff
@@ -1,13 +1,13 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:50:00.275671 jsodb-1.5.5/
--rw-r--r--   0 runner    (1001) docker     (123)     1059 2023-07-23 12:49:48.000000 jsodb-1.5.5/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     1325 2023-07-23 12:50:00.275671 jsodb-1.5.5/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      880 2023-07-23 12:49:48.000000 jsodb-1.5.5/README.md
--rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-23 12:49:48.000000 jsodb-1.5.5/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 12:50:00.275671 jsodb-1.5.5/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:50:00.275671 jsodb-1.5.5/src/
--rw-r--r--   0 runner    (1001) docker     (123)      739 2023-07-23 12:49:48.000000 jsodb-1.5.5/src/jdb.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:50:00.275671 jsodb-1.5.5/src/jsodb.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1325 2023-07-23 12:50:00.000000 jsodb-1.5.5/src/jsodb.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      175 2023-07-23 12:50:00.000000 jsodb-1.5.5/src/jsodb.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 12:50:00.000000 jsodb-1.5.5/src/jsodb.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        4 2023-07-23 12:50:00.000000 jsodb-1.5.5/src/jsodb.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:30:50.293114 jsodb-1.6.0/
+-rw-r--r--   0 runner    (1001) docker     (123)     1059 2023-07-23 14:30:37.000000 jsodb-1.6.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     1436 2023-07-23 14:30:50.293114 jsodb-1.6.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      992 2023-07-23 14:30:37.000000 jsodb-1.6.0/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-23 14:30:37.000000 jsodb-1.6.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 14:30:50.293114 jsodb-1.6.0/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:30:50.293114 jsodb-1.6.0/src/
+-rw-r--r--   0 runner    (1001) docker     (123)      993 2023-07-23 14:30:37.000000 jsodb-1.6.0/src/jdb.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:30:50.293114 jsodb-1.6.0/src/jsodb.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1436 2023-07-23 14:30:50.000000 jsodb-1.6.0/src/jsodb.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      175 2023-07-23 14:30:50.000000 jsodb-1.6.0/src/jsodb.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 14:30:50.000000 jsodb-1.6.0/src/jsodb.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        4 2023-07-23 14:30:50.000000 jsodb-1.6.0/src/jsodb.egg-info/top_level.txt
```

### Comparing `jsodb-1.5.5/LICENSE` & `jsodb-1.6.0/LICENSE`

 * *Files identical despite different names*

### Comparing `jsodb-1.5.5/PKG-INFO` & `jsodb-1.6.0/PKG-INFO`

 * *Files 10% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: jsodb
-Version: 1.5.5
+Version: 1.6.0
 Summary: simple json database lib
 Author-email: dttric <chudinovd222@gmail.com>
 Project-URL: Homepage, https://github.com/dttric/jsodb
 Project-URL: Bug Tracker, https://github.com/dttric/jsodb/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
@@ -19,19 +19,20 @@
 Instalation:
 `python3 -m pip install jsodb`
 
 Basic funcs:
 ```py
 import jdb
 getkeyval("key") # returns key val
-addkey("key"=val) # adds keys to json
+addkey(key=val) # adds keys to json
 changekey("key", val) # changes key to new val
-createjson("/path/to/file") # new .json file (without decorator)
+createjson("/path/to/file" """without .json""") # new .json file (without decorator)
 addtokey("key", int) # key += int
 subfromkey("key", int) # key -= int
+addmultikey("key", key=val, key2=val2) # new multi key {key: {"key": "val", "key2", "val2"}}
 @json("/path/to/file") # main decorator
 ```
 
 To use all that functions you need function with decorator, json file will be: opened, edited, saved.
 
 Basic usage:
 ```py
```

### Comparing `jsodb-1.5.5/README.md` & `jsodb-1.6.0/README.md`

 * *Files 18% similar despite different names*

```diff
@@ -5,19 +5,20 @@
 Instalation:
 `python3 -m pip install jsodb`
 
 Basic funcs:
 ```py
 import jdb
 getkeyval("key") # returns key val
-addkey("key"=val) # adds keys to json
+addkey(key=val) # adds keys to json
 changekey("key", val) # changes key to new val
-createjson("/path/to/file") # new .json file (without decorator)
+createjson("/path/to/file" """without .json""") # new .json file (without decorator)
 addtokey("key", int) # key += int
 subfromkey("key", int) # key -= int
+addmultikey("key", key=val, key2=val2) # new multi key {key: {"key": "val", "key2", "val2"}}
 @json("/path/to/file") # main decorator
 ```
 
 To use all that functions you need function with decorator, json file will be: opened, edited, saved.
 
 Basic usage:
 ```py
```

### Comparing `jsodb-1.5.5/pyproject.toml` & `jsodb-1.6.0/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 [project]
 name = "jsodb"
-version = "1.5.5"
+version = "1.6.0"
 authors = [
   { name="dttric", email="chudinovd222@gmail.com" },
 ]
 description = "simple json database lib"
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = [
```

### Comparing `jsodb-1.5.5/src/jsodb.egg-info/PKG-INFO` & `jsodb-1.6.0/src/jsodb.egg-info/PKG-INFO`

 * *Files 10% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: jsodb
-Version: 1.5.5
+Version: 1.6.0
 Summary: simple json database lib
 Author-email: dttric <chudinovd222@gmail.com>
 Project-URL: Homepage, https://github.com/dttric/jsodb
 Project-URL: Bug Tracker, https://github.com/dttric/jsodb/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
@@ -19,19 +19,20 @@
 Instalation:
 `python3 -m pip install jsodb`
 
 Basic funcs:
 ```py
 import jdb
 getkeyval("key") # returns key val
-addkey("key"=val) # adds keys to json
+addkey(key=val) # adds keys to json
 changekey("key", val) # changes key to new val
-createjson("/path/to/file") # new .json file (without decorator)
+createjson("/path/to/file" """without .json""") # new .json file (without decorator)
 addtokey("key", int) # key += int
 subfromkey("key", int) # key -= int
+addmultikey("key", key=val, key2=val2) # new multi key {key: {"key": "val", "key2", "val2"}}
 @json("/path/to/file") # main decorator
 ```
 
 To use all that functions you need function with decorator, json file will be: opened, edited, saved.
 
 Basic usage:
 ```py
```

