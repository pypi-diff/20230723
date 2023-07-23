# Comparing `tmp/terminal_manager-0.9.0.tar.gz` & `tmp/terminal_manager-0.9.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "terminal_manager-0.9.0.tar", last modified: Sun Jul 23 02:56:27 2023, max compression
+gzip compressed data, was "terminal_manager-0.9.1.tar", last modified: Sun Jul 23 03:24:18 2023, max compression
```

## Comparing `terminal_manager-0.9.0.tar` & `terminal_manager-0.9.1.tar`

### file list

```diff
@@ -1,28 +1,28 @@
-drwxrwxr-x   0 adrian    (1000) adrian    (1000)        0 2023-07-23 02:56:27.000528 terminal_manager-0.9.0/
--rw-rw-r--   0 adrian    (1000) adrian    (1000)     1063 2023-07-11 04:42:30.000000 terminal_manager-0.9.0/LICENSE
--rw-rw-r--   0 adrian    (1000) adrian    (1000)      725 2023-07-23 02:56:26.996528 terminal_manager-0.9.0/PKG-INFO
--rw-rw-r--   0 adrian    (1000) adrian    (1000)      107 2023-07-11 04:42:30.000000 terminal_manager-0.9.0/README.md
--rw-rw-r--   0 adrian    (1000) adrian    (1000)      778 2023-07-23 02:56:15.000000 terminal_manager-0.9.0/pyproject.toml
--rw-rw-r--   0 adrian    (1000) adrian    (1000)       38 2023-07-23 02:56:27.000528 terminal_manager-0.9.0/setup.cfg
-drwxrwxr-x   0 adrian    (1000) adrian    (1000)        0 2023-07-23 02:56:26.992528 terminal_manager-0.9.0/src/
-drwxrwxr-x   0 adrian    (1000) adrian    (1000)        0 2023-07-23 02:56:26.996528 terminal_manager-0.9.0/src/terminal_manager/
--rw-r--r--   0 adrian    (1000) adrian    (1000)     7023 2023-07-22 10:32:33.000000 terminal_manager-0.9.0/src/terminal_manager/__init__.py
--rw-r--r--   0 adrian    (1000) adrian    (1000)     3352 2023-07-22 10:32:33.000000 terminal_manager-0.9.0/src/terminal_manager/collection.py
--rw-r--r--   0 adrian    (1000) adrian    (1000)     6319 2023-07-23 02:34:53.000000 terminal_manager-0.9.0/src/terminal_manager/command.py
-drwxrwxr-x   0 adrian    (1000) adrian    (1000)        0 2023-07-23 02:56:26.996528 terminal_manager-0.9.0/src/terminal_manager/default_collections/
--rw-r--r--   0 adrian    (1000) adrian    (1000)      161 2023-07-22 10:32:33.000000 terminal_manager-0.9.0/src/terminal_manager/default_collections/__init__.py
--rw-r--r--   0 adrian    (1000) adrian    (1000)     1084 2023-07-22 10:32:33.000000 terminal_manager-0.9.0/src/terminal_manager/default_collections/const.py
--rw-r--r--   0 adrian    (1000) adrian    (1000)     4371 2023-07-23 02:33:51.000000 terminal_manager-0.9.0/src/terminal_manager/default_collections/linux.py
--rw-r--r--   0 adrian    (1000) adrian    (1000)     5206 2023-07-22 10:32:33.000000 terminal_manager-0.9.0/src/terminal_manager/default_collections/windows_cmd.py
--rw-r--r--   0 adrian    (1000) adrian    (1000)     5368 2023-07-23 02:34:08.000000 terminal_manager-0.9.0/src/terminal_manager/default_collections/windows_ps.py
--rw-r--r--   0 adrian    (1000) adrian    (1000)       94 2023-07-22 10:32:33.000000 terminal_manager-0.9.0/src/terminal_manager/errors.py
--rw-r--r--   0 adrian    (1000) adrian    (1000)      617 2023-07-22 10:32:33.000000 terminal_manager-0.9.0/src/terminal_manager/event.py
--rw-r--r--   0 adrian    (1000) adrian    (1000)      222 2023-07-22 10:32:33.000000 terminal_manager-0.9.0/src/terminal_manager/helpers.py
--rw-r--r--   0 adrian    (1000) adrian    (1000)     8379 2023-07-22 10:32:33.000000 terminal_manager-0.9.0/src/terminal_manager/sensor.py
--rw-r--r--   0 adrian    (1000) adrian    (1000)     1248 2023-07-22 10:32:33.000000 terminal_manager-0.9.0/src/terminal_manager/synchronizer.py
-drwxrwxr-x   0 adrian    (1000) adrian    (1000)        0 2023-07-23 02:56:26.996528 terminal_manager-0.9.0/src/terminal_manager.egg-info/
--rw-rw-r--   0 adrian    (1000) adrian    (1000)      725 2023-07-23 02:56:26.000000 terminal_manager-0.9.0/src/terminal_manager.egg-info/PKG-INFO
--rw-rw-r--   0 adrian    (1000) adrian    (1000)      776 2023-07-23 02:56:26.000000 terminal_manager-0.9.0/src/terminal_manager.egg-info/SOURCES.txt
--rw-rw-r--   0 adrian    (1000) adrian    (1000)        1 2023-07-23 02:56:26.000000 terminal_manager-0.9.0/src/terminal_manager.egg-info/dependency_links.txt
--rw-rw-r--   0 adrian    (1000) adrian    (1000)       22 2023-07-23 02:56:26.000000 terminal_manager-0.9.0/src/terminal_manager.egg-info/requires.txt
--rw-rw-r--   0 adrian    (1000) adrian    (1000)       17 2023-07-23 02:56:26.000000 terminal_manager-0.9.0/src/terminal_manager.egg-info/top_level.txt
+drwxrwxr-x   0 adrian    (1000) adrian    (1000)        0 2023-07-23 03:24:18.133574 terminal_manager-0.9.1/
+-rw-rw-r--   0 adrian    (1000) adrian    (1000)     1063 2023-07-11 04:42:30.000000 terminal_manager-0.9.1/LICENSE
+-rw-rw-r--   0 adrian    (1000) adrian    (1000)      725 2023-07-23 03:24:18.133574 terminal_manager-0.9.1/PKG-INFO
+-rw-rw-r--   0 adrian    (1000) adrian    (1000)      107 2023-07-11 04:42:30.000000 terminal_manager-0.9.1/README.md
+-rw-rw-r--   0 adrian    (1000) adrian    (1000)      778 2023-07-23 03:23:12.000000 terminal_manager-0.9.1/pyproject.toml
+-rw-rw-r--   0 adrian    (1000) adrian    (1000)       38 2023-07-23 03:24:18.133574 terminal_manager-0.9.1/setup.cfg
+drwxrwxr-x   0 adrian    (1000) adrian    (1000)        0 2023-07-23 03:24:18.125574 terminal_manager-0.9.1/src/
+drwxrwxr-x   0 adrian    (1000) adrian    (1000)        0 2023-07-23 03:24:18.129574 terminal_manager-0.9.1/src/terminal_manager/
+-rw-r--r--   0 adrian    (1000) adrian    (1000)     7023 2023-07-22 10:32:33.000000 terminal_manager-0.9.1/src/terminal_manager/__init__.py
+-rw-r--r--   0 adrian    (1000) adrian    (1000)     3352 2023-07-22 10:32:33.000000 terminal_manager-0.9.1/src/terminal_manager/collection.py
+-rw-r--r--   0 adrian    (1000) adrian    (1000)     6319 2023-07-23 02:34:53.000000 terminal_manager-0.9.1/src/terminal_manager/command.py
+drwxrwxr-x   0 adrian    (1000) adrian    (1000)        0 2023-07-23 03:24:18.133574 terminal_manager-0.9.1/src/terminal_manager/default_collections/
+-rw-r--r--   0 adrian    (1000) adrian    (1000)      161 2023-07-22 10:32:33.000000 terminal_manager-0.9.1/src/terminal_manager/default_collections/__init__.py
+-rw-r--r--   0 adrian    (1000) adrian    (1000)     1084 2023-07-22 10:32:33.000000 terminal_manager-0.9.1/src/terminal_manager/default_collections/const.py
+-rw-r--r--   0 adrian    (1000) adrian    (1000)     4371 2023-07-23 02:33:51.000000 terminal_manager-0.9.1/src/terminal_manager/default_collections/linux.py
+-rw-r--r--   0 adrian    (1000) adrian    (1000)     5206 2023-07-22 10:32:33.000000 terminal_manager-0.9.1/src/terminal_manager/default_collections/windows_cmd.py
+-rw-r--r--   0 adrian    (1000) adrian    (1000)     5368 2023-07-23 02:34:08.000000 terminal_manager-0.9.1/src/terminal_manager/default_collections/windows_ps.py
+-rw-r--r--   0 adrian    (1000) adrian    (1000)       94 2023-07-22 10:32:33.000000 terminal_manager-0.9.1/src/terminal_manager/errors.py
+-rw-r--r--   0 adrian    (1000) adrian    (1000)      617 2023-07-22 10:32:33.000000 terminal_manager-0.9.1/src/terminal_manager/event.py
+-rw-r--r--   0 adrian    (1000) adrian    (1000)      222 2023-07-22 10:32:33.000000 terminal_manager-0.9.1/src/terminal_manager/helpers.py
+-rw-r--r--   0 adrian    (1000) adrian    (1000)     8379 2023-07-22 10:32:33.000000 terminal_manager-0.9.1/src/terminal_manager/sensor.py
+-rw-r--r--   0 adrian    (1000) adrian    (1000)     1248 2023-07-22 10:32:33.000000 terminal_manager-0.9.1/src/terminal_manager/synchronizer.py
+drwxrwxr-x   0 adrian    (1000) adrian    (1000)        0 2023-07-23 03:24:18.129574 terminal_manager-0.9.1/src/terminal_manager.egg-info/
+-rw-rw-r--   0 adrian    (1000) adrian    (1000)      725 2023-07-23 03:24:18.000000 terminal_manager-0.9.1/src/terminal_manager.egg-info/PKG-INFO
+-rw-rw-r--   0 adrian    (1000) adrian    (1000)      776 2023-07-23 03:24:18.000000 terminal_manager-0.9.1/src/terminal_manager.egg-info/SOURCES.txt
+-rw-rw-r--   0 adrian    (1000) adrian    (1000)        1 2023-07-23 03:24:18.000000 terminal_manager-0.9.1/src/terminal_manager.egg-info/dependency_links.txt
+-rw-rw-r--   0 adrian    (1000) adrian    (1000)       22 2023-07-23 03:24:18.000000 terminal_manager-0.9.1/src/terminal_manager.egg-info/requires.txt
+-rw-rw-r--   0 adrian    (1000) adrian    (1000)       17 2023-07-23 03:24:18.000000 terminal_manager-0.9.1/src/terminal_manager.egg-info/top_level.txt
```

### Comparing `terminal_manager-0.9.0/LICENSE` & `terminal_manager-0.9.1/LICENSE`

 * *Files identical despite different names*

### Comparing `terminal_manager-0.9.0/PKG-INFO` & `terminal_manager-0.9.1/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: terminal_manager
-Version: 0.9.0
+Version: 0.9.1
 Summary: Use terminal commands to control and monitor devices
 Author-email: zhbjsh <zhbjsh@outlook.com>
 Project-URL: Homepage, https://github.com/zhbjsh/terminal-manager
 Project-URL: Bug Tracker, https://github.com/zhbjsh/terminal-manager/issues
 Keywords: terminal,console,shell,bash,cmd,power shell,commands,command line
 Classifier: Programming Language :: Python :: 3.10
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `terminal_manager-0.9.0/pyproject.toml` & `terminal_manager-0.9.1/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "terminal_manager"
-version = "0.9.0"
+version = "0.9.1"
 authors = [
   { name="zhbjsh", email="zhbjsh@outlook.com" },
 ]
 description = "Use terminal commands to control and monitor devices"
 readme = "README.md"
 requires-python = ">=3.10"
 classifiers = [
```

### Comparing `terminal_manager-0.9.0/src/terminal_manager/__init__.py` & `terminal_manager-0.9.1/src/terminal_manager/__init__.py`

 * *Files identical despite different names*

### Comparing `terminal_manager-0.9.0/src/terminal_manager/collection.py` & `terminal_manager-0.9.1/src/terminal_manager/collection.py`

 * *Files identical despite different names*

### Comparing `terminal_manager-0.9.0/src/terminal_manager/command.py` & `terminal_manager-0.9.1/src/terminal_manager/command.py`

 * *Files identical despite different names*

### Comparing `terminal_manager-0.9.0/src/terminal_manager/default_collections/const.py` & `terminal_manager-0.9.1/src/terminal_manager/default_collections/const.py`

 * *Files identical despite different names*

### Comparing `terminal_manager-0.9.0/src/terminal_manager/default_collections/linux.py` & `terminal_manager-0.9.1/src/terminal_manager/default_collections/linux.py`

 * *Files identical despite different names*

### Comparing `terminal_manager-0.9.0/src/terminal_manager/default_collections/windows_cmd.py` & `terminal_manager-0.9.1/src/terminal_manager/default_collections/windows_cmd.py`

 * *Files identical despite different names*

### Comparing `terminal_manager-0.9.0/src/terminal_manager/default_collections/windows_ps.py` & `terminal_manager-0.9.1/src/terminal_manager/default_collections/windows_ps.py`

 * *Files identical despite different names*

### Comparing `terminal_manager-0.9.0/src/terminal_manager/event.py` & `terminal_manager-0.9.1/src/terminal_manager/event.py`

 * *Files identical despite different names*

### Comparing `terminal_manager-0.9.0/src/terminal_manager/sensor.py` & `terminal_manager-0.9.1/src/terminal_manager/sensor.py`

 * *Files identical despite different names*

### Comparing `terminal_manager-0.9.0/src/terminal_manager/synchronizer.py` & `terminal_manager-0.9.1/src/terminal_manager/synchronizer.py`

 * *Files identical despite different names*

### Comparing `terminal_manager-0.9.0/src/terminal_manager.egg-info/PKG-INFO` & `terminal_manager-0.9.1/src/terminal_manager.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: terminal-manager
-Version: 0.9.0
+Version: 0.9.1
 Summary: Use terminal commands to control and monitor devices
 Author-email: zhbjsh <zhbjsh@outlook.com>
 Project-URL: Homepage, https://github.com/zhbjsh/terminal-manager
 Project-URL: Bug Tracker, https://github.com/zhbjsh/terminal-manager/issues
 Keywords: terminal,console,shell,bash,cmd,power shell,commands,command line
 Classifier: Programming Language :: Python :: 3.10
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `terminal_manager-0.9.0/src/terminal_manager.egg-info/SOURCES.txt` & `terminal_manager-0.9.1/src/terminal_manager.egg-info/SOURCES.txt`

 * *Files identical despite different names*

