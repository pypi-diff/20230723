# Comparing `tmp/jsodb-1.0.1.tar.gz` & `tmp/jsodb-1.5.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "jsodb-1.0.1.tar", last modified: Sun Jul 23 07:59:35 2023, max compression
+gzip compressed data, was "jsodb-1.5.0.tar", last modified: Sun Jul 23 10:09:55 2023, max compression
```

## Comparing `jsodb-1.0.1.tar` & `jsodb-1.5.0.tar`

### file list

```diff
@@ -1,13 +1,13 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 07:59:35.848995 jsodb-1.0.1/
--rw-rw-rw-   0        0        0     1059 2023-07-23 07:32:25.000000 jsodb-1.0.1/LICENSE
--rw-rw-rw-   0        0        0     1314 2023-07-23 07:59:35.847994 jsodb-1.0.1/PKG-INFO
--rw-rw-rw-   0        0        0      819 2023-07-23 07:32:25.000000 jsodb-1.0.1/README.md
--rw-rw-rw-   0        0        0      573 2023-07-23 07:35:45.000000 jsodb-1.0.1/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-07-23 07:59:35.849993 jsodb-1.0.1/setup.cfg
-drwxrwxrwx   0        0        0        0 2023-07-23 07:59:35.816991 jsodb-1.0.1/src/
--rw-rw-rw-   0        0        0      495 2023-07-23 07:33:56.000000 jsodb-1.0.1/src/jdb.py
-drwxrwxrwx   0        0        0        0 2023-07-23 07:59:35.844993 jsodb-1.0.1/src/jsodb.egg-info/
--rw-rw-rw-   0        0        0     1314 2023-07-23 07:59:35.000000 jsodb-1.0.1/src/jsodb.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      175 2023-07-23 07:59:35.000000 jsodb-1.0.1/src/jsodb.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 07:59:35.000000 jsodb-1.0.1/src/jsodb.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        4 2023-07-23 07:59:35.000000 jsodb-1.0.1/src/jsodb.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:09:55.616820 jsodb-1.5.0/
+-rw-r--r--   0 runner    (1001) docker     (123)     1059 2023-07-23 10:09:36.000000 jsodb-1.5.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     1255 2023-07-23 10:09:55.616820 jsodb-1.5.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      808 2023-07-23 10:09:36.000000 jsodb-1.5.0/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-23 10:09:36.000000 jsodb-1.5.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 10:09:55.616820 jsodb-1.5.0/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:09:55.616820 jsodb-1.5.0/src/
+-rw-r--r--   0 runner    (1001) docker     (123)      495 2023-07-23 10:09:36.000000 jsodb-1.5.0/src/jdb.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:09:55.616820 jsodb-1.5.0/src/jsodb.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1255 2023-07-23 10:09:55.000000 jsodb-1.5.0/src/jsodb.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      175 2023-07-23 10:09:55.000000 jsodb-1.5.0/src/jsodb.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 10:09:55.000000 jsodb-1.5.0/src/jsodb.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        4 2023-07-23 10:09:55.000000 jsodb-1.5.0/src/jsodb.egg-info/top_level.txt
```

### Comparing `jsodb-1.0.1/LICENSE` & `jsodb-1.5.0/LICENSE`

 * *Files identical despite different names*

### Comparing `jsodb-1.0.1/README.md` & `jsodb-1.5.0/README.md`

 * *Files 3% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 
 ### How to work with it?
 Instalation:
 `python3 -m pip install jsodb`
 
 Basic funcs:
 ```py
-from jsodb import jdb
+import jdb
 getkeyval("key") # returns key val
 addkey("key"=val) # adds keys to json
 changekey("key", val) # changes key to new val
 createjson("/path/to/file") # new .json file (without decorator)
 @json("/path/to/file") # main decorator
 ```
```

### Comparing `jsodb-1.0.1/pyproject.toml` & `jsodb-1.5.0/pyproject.toml`

 * *Files 21% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 [project]
 name = "jsodb"
-version = "1.0.1"
+version = "1.5.0"
 authors = [
   { name="dttric", email="chudinovd222@gmail.com" },
 ]
 description = "simple json database lib"
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = [
```

