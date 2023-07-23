# Comparing `tmp/septem-circumstantiae-0.0.4.tar.gz` & `tmp/septem-circumstantiae-0.0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "septem-circumstantiae-0.0.4.tar", last modified: Sat Jul 22 00:48:00 2023, max compression
+gzip compressed data, was "septem-circumstantiae-0.0.5.tar", last modified: Sun Jul 23 19:04:11 2023, max compression
```

## Comparing `septem-circumstantiae-0.0.4.tar` & `septem-circumstantiae-0.0.5.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxrwxr-x   0 alxfed    (1001) alxfed    (1001)        0 2023-07-22 00:48:00.294982 septem-circumstantiae-0.0.4/
--rw-rw-r--   0 alxfed    (1001) alxfed    (1001)     1078 2023-07-09 23:53:45.000000 septem-circumstantiae-0.0.4/LICENSE
--rw-rw-r--   0 alxfed    (1001) alxfed    (1001)      657 2023-07-22 00:48:00.290982 septem-circumstantiae-0.0.4/PKG-INFO
--rw-rw-r--   0 alxfed    (1001) alxfed    (1001)       91 2023-07-09 23:53:45.000000 septem-circumstantiae-0.0.4/README.md
--rw-rw-r--   0 alxfed    (1001) alxfed    (1001)      647 2023-07-22 00:46:06.000000 septem-circumstantiae-0.0.4/pyproject.toml
--rw-rw-r--   0 alxfed    (1001) alxfed    (1001)       38 2023-07-22 00:48:00.294982 septem-circumstantiae-0.0.4/setup.cfg
-drwxrwxr-x   0 alxfed    (1001) alxfed    (1001)        0 2023-07-22 00:48:00.290982 septem-circumstantiae-0.0.4/src/
-drwxrwxr-x   0 alxfed    (1001) alxfed    (1001)        0 2023-07-22 00:48:00.290982 septem-circumstantiae-0.0.4/src/septem-circumstantiae/
--rw-rw-r--   0 alxfed    (1001) alxfed    (1001)      245 2023-07-22 00:46:06.000000 septem-circumstantiae-0.0.4/src/septem-circumstantiae/__init__.py
--rw-rw-r--   0 alxfed    (1001) alxfed    (1001)      620 2023-07-22 00:37:34.000000 septem-circumstantiae-0.0.4/src/septem-circumstantiae/events.py
-drwxrwxr-x   0 alxfed    (1001) alxfed    (1001)        0 2023-07-22 00:48:00.290982 septem-circumstantiae-0.0.4/src/septem_circumstantiae.egg-info/
--rw-rw-r--   0 alxfed    (1001) alxfed    (1001)      657 2023-07-22 00:48:00.000000 septem-circumstantiae-0.0.4/src/septem_circumstantiae.egg-info/PKG-INFO
--rw-rw-r--   0 alxfed    (1001) alxfed    (1001)      302 2023-07-22 00:48:00.000000 septem-circumstantiae-0.0.4/src/septem_circumstantiae.egg-info/SOURCES.txt
--rw-rw-r--   0 alxfed    (1001) alxfed    (1001)        1 2023-07-22 00:48:00.000000 septem-circumstantiae-0.0.4/src/septem_circumstantiae.egg-info/dependency_links.txt
--rw-rw-r--   0 alxfed    (1001) alxfed    (1001)       22 2023-07-22 00:48:00.000000 septem-circumstantiae-0.0.4/src/septem_circumstantiae.egg-info/top_level.txt
+drwxrwxr-x   0 alxfed    (1001) alxfed    (1001)        0 2023-07-23 19:04:11.984641 septem-circumstantiae-0.0.5/
+-rw-rw-r--   0 alxfed    (1001) alxfed    (1001)     1078 2023-07-09 23:53:45.000000 septem-circumstantiae-0.0.5/LICENSE
+-rw-rw-r--   0 alxfed    (1001) alxfed    (1001)      657 2023-07-23 19:04:11.984641 septem-circumstantiae-0.0.5/PKG-INFO
+-rw-rw-r--   0 alxfed    (1001) alxfed    (1001)       91 2023-07-09 23:53:45.000000 septem-circumstantiae-0.0.5/README.md
+-rw-rw-r--   0 alxfed    (1001) alxfed    (1001)      647 2023-07-23 19:00:55.000000 septem-circumstantiae-0.0.5/pyproject.toml
+-rw-rw-r--   0 alxfed    (1001) alxfed    (1001)       38 2023-07-23 19:04:11.984641 septem-circumstantiae-0.0.5/setup.cfg
+drwxrwxr-x   0 alxfed    (1001) alxfed    (1001)        0 2023-07-23 19:04:11.980641 septem-circumstantiae-0.0.5/src/
+drwxrwxr-x   0 alxfed    (1001) alxfed    (1001)        0 2023-07-23 19:04:11.984641 septem-circumstantiae-0.0.5/src/septem-circumstantiae/
+-rw-rw-r--   0 alxfed    (1001) alxfed    (1001)      245 2023-07-22 00:46:06.000000 septem-circumstantiae-0.0.5/src/septem-circumstantiae/__init__.py
+-rw-rw-r--   0 alxfed    (1001) alxfed    (1001)     2036 2023-07-23 19:00:55.000000 septem-circumstantiae-0.0.5/src/septem-circumstantiae/events.py
+drwxrwxr-x   0 alxfed    (1001) alxfed    (1001)        0 2023-07-23 19:04:11.984641 septem-circumstantiae-0.0.5/src/septem_circumstantiae.egg-info/
+-rw-rw-r--   0 alxfed    (1001) alxfed    (1001)      657 2023-07-23 19:04:11.000000 septem-circumstantiae-0.0.5/src/septem_circumstantiae.egg-info/PKG-INFO
+-rw-rw-r--   0 alxfed    (1001) alxfed    (1001)      302 2023-07-23 19:04:11.000000 septem-circumstantiae-0.0.5/src/septem_circumstantiae.egg-info/SOURCES.txt
+-rw-rw-r--   0 alxfed    (1001) alxfed    (1001)        1 2023-07-23 19:04:11.000000 septem-circumstantiae-0.0.5/src/septem_circumstantiae.egg-info/dependency_links.txt
+-rw-rw-r--   0 alxfed    (1001) alxfed    (1001)       22 2023-07-23 19:04:11.000000 septem-circumstantiae-0.0.5/src/septem_circumstantiae.egg-info/top_level.txt
```

### Comparing `septem-circumstantiae-0.0.4/LICENSE` & `septem-circumstantiae-0.0.5/LICENSE`

 * *Files identical despite different names*

### Comparing `septem-circumstantiae-0.0.4/PKG-INFO` & `septem-circumstantiae-0.0.5/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: septem-circumstantiae
-Version: 0.0.4
+Version: 0.0.5
 Summary: Septem Circumstantiae
 Author-email: Alexander Fedotov <alex.fedotov@aol.com>
 Project-URL: Homepage, https://github.com/septem-circumstantiae/septem-circumstantiae
 Project-URL: Bug Tracker, https://github.com/septem-circumstantiae/septem-circumstantiae/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `septem-circumstantiae-0.0.4/pyproject.toml` & `septem-circumstantiae-0.0.5/pyproject.toml`

 * *Files 21% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 [build-system]
 requires = ["setuptools>=67.0"]
 build-backend = "setuptools.build_meta"
 [project]
 name = "septem-circumstantiae"
-version = "0.0.4"
+version = "0.0.5"
 authors = [
     {name="Alexander Fedotov", email="alex.fedotov@aol.com"},
 ]
 description = "Septem Circumstantiae"
 readme = "README.md"
 requires-python = ">=3.10"
 classifiers=[
```

### Comparing `septem-circumstantiae-0.0.4/src/septem_circumstantiae.egg-info/PKG-INFO` & `septem-circumstantiae-0.0.5/src/septem_circumstantiae.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: septem-circumstantiae
-Version: 0.0.4
+Version: 0.0.5
 Summary: Septem Circumstantiae
 Author-email: Alexander Fedotov <alex.fedotov@aol.com>
 Project-URL: Homepage, https://github.com/septem-circumstantiae/septem-circumstantiae
 Project-URL: Bug Tracker, https://github.com/septem-circumstantiae/septem-circumstantiae/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

