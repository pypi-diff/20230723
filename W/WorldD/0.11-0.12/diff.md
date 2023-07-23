# Comparing `tmp/WorldD-0.11.tar.gz` & `tmp/WorldD-0.12.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "WorldD-0.11.tar", last modified: Sun Jul 23 14:47:55 2023, max compression
+gzip compressed data, was "WorldD-0.12.tar", last modified: Sun Jul 23 15:50:17 2023, max compression
```

## Comparing `WorldD-0.11.tar` & `WorldD-0.12.tar`

### file list

```diff
@@ -1,12 +1,17 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:47:55.073593 WorldD-0.11/
--rw-r--r--   0 runner    (1001) docker     (123)     1060 2023-07-23 14:47:43.000000 WorldD-0.11/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     1151 2023-07-23 14:47:55.073593 WorldD-0.11/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      734 2023-07-23 14:47:43.000000 WorldD-0.11/README.md
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 14:47:55.073593 WorldD-0.11/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      597 2023-07-23 14:47:43.000000 WorldD-0.11/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:47:55.073593 WorldD-0.11/src/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:47:55.073593 WorldD-0.11/src/WorldD.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1151 2023-07-23 14:47:55.000000 WorldD-0.11/src/WorldD.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      162 2023-07-23 14:47:55.000000 WorldD-0.11/src/WorldD.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 14:47:55.000000 WorldD-0.11/src/WorldD.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 14:47:55.000000 WorldD-0.11/src/WorldD.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:50:17.461399 WorldD-0.12/
+-rw-r--r--   0 runner    (1001) docker     (123)     1060 2023-07-23 15:50:06.000000 WorldD-0.12/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     1186 2023-07-23 15:50:17.461399 WorldD-0.12/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      734 2023-07-23 15:50:06.000000 WorldD-0.12/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:50:17.461399 WorldD-0.12/WorldD.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1186 2023-07-23 15:50:17.000000 WorldD-0.12/WorldD.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      237 2023-07-23 15:50:17.000000 WorldD-0.12/WorldD.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 15:50:17.000000 WorldD-0.12/WorldD.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        7 2023-07-23 15:50:17.000000 WorldD-0.12/WorldD.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 15:50:17.461399 WorldD-0.12/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      665 2023-07-23 15:50:06.000000 WorldD-0.12/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:50:17.461399 WorldD-0.12/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:50:17.461399 WorldD-0.12/src/WorldD/
+-rw-r--r--   0 runner    (1001) docker     (123)       23 2023-07-23 15:50:06.000000 WorldD-0.12/src/WorldD/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    30996 2023-07-23 15:50:06.000000 WorldD-0.12/src/WorldD/main.py
+-rw-r--r--   0 runner    (1001) docker     (123)      908 2023-07-23 15:50:06.000000 WorldD-0.12/src/WorldD/options.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       84 2023-07-23 15:50:06.000000 WorldD-0.12/src/WorldD/profilling.py
```

### Comparing `WorldD-0.11/LICENSE` & `WorldD-0.12/LICENSE`

 * *Files identical despite different names*

### Comparing `WorldD-0.11/PKG-INFO` & `WorldD-0.12/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,17 +1,19 @@
 Metadata-Version: 2.1
 Name: WorldD
-Version: 0.11
+Version: 0.12
 Summary: Level editor made specifically for pygame games
 Home-page: https://github.com/NotMEE12/WorldD
 Author: Aleks Baran
 Author-email: legominefan@gmail.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
+Requires: pygame
+Requires: tomlkit
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # WorldD - level designer for pygame
 [![Upload Python Package](https://github.com/NOTMEE12/WorldD/actions/workflows/python-publish.yml/badge.svg)](https://github.com/NOTMEE12/WorldD/actions/workflows/python-publish.yml)
 ### Shortcuts:
 - `SHIFT + ESCAPE` - quit the application,
```

### Comparing `WorldD-0.11/README.md` & `WorldD-0.12/README.md`

 * *Files identical despite different names*

### Comparing `WorldD-0.11/src/WorldD.egg-info/PKG-INFO` & `WorldD-0.12/WorldD.egg-info/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,17 +1,19 @@
 Metadata-Version: 2.1
 Name: WorldD
-Version: 0.11
+Version: 0.12
 Summary: Level editor made specifically for pygame games
 Home-page: https://github.com/NotMEE12/WorldD
 Author: Aleks Baran
 Author-email: legominefan@gmail.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
+Requires: pygame
+Requires: tomlkit
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # WorldD - level designer for pygame
 [![Upload Python Package](https://github.com/NOTMEE12/WorldD/actions/workflows/python-publish.yml/badge.svg)](https://github.com/NOTMEE12/WorldD/actions/workflows/python-publish.yml)
 ### Shortcuts:
 - `SHIFT + ESCAPE` - quit the application,
```

