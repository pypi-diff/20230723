# Comparing `tmp/SageLogger-1.3.1.tar.gz` & `tmp/SageLogger-1.3.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "SageLogger-1.3.1.tar", last modified: Sun Jul 23 11:36:02 2023, max compression
+gzip compressed data, was "SageLogger-1.3.2.tar", last modified: Sun Jul 23 11:38:45 2023, max compression
```

## Comparing `SageLogger-1.3.1.tar` & `SageLogger-1.3.2.tar`

### file list

```diff
@@ -1,16 +1,17 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 11:36:02.139053 SageLogger-1.3.1/
--rw-rw-rw-   0        0        0     4701 2023-07-23 11:36:02.136546 SageLogger-1.3.1/PKG-INFO
-drwxrwxrwx   0        0        0        0 2023-07-23 11:36:02.122835 SageLogger-1.3.1/SageLogger/
--rw-rw-rw-   0        0        0    13166 2023-07-23 11:26:27.000000 SageLogger-1.3.1/SageLogger/Logger.py
--rw-rw-rw-   0        0        0     1562 2023-07-23 11:22:55.000000 SageLogger-1.3.1/SageLogger/SageException.py
--rw-rw-rw-   0        0        0     2954 2023-07-23 11:11:02.000000 SageLogger-1.3.1/SageLogger/SageFactory.py
--rw-rw-rw-   0        0        0       15 2023-07-22 20:32:47.000000 SageLogger-1.3.1/SageLogger/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 11:36:02.133543 SageLogger-1.3.1/SageLogger.egg-info/
--rw-rw-rw-   0        0        0     4701 2023-07-23 11:36:01.000000 SageLogger-1.3.1/SageLogger.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      290 2023-07-23 11:36:02.000000 SageLogger-1.3.1/SageLogger.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 11:36:01.000000 SageLogger-1.3.1/SageLogger.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       18 2023-07-23 11:36:01.000000 SageLogger-1.3.1/SageLogger.egg-info/requires.txt
--rw-rw-rw-   0        0        0       11 2023-07-23 11:36:01.000000 SageLogger-1.3.1/SageLogger.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      661 2023-07-23 11:33:55.000000 SageLogger-1.3.1/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-07-23 11:36:02.139053 SageLogger-1.3.1/setup.cfg
--rw-rw-rw-   0        0        0     1069 2023-07-23 11:33:01.000000 SageLogger-1.3.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 11:38:45.932696 SageLogger-1.3.2/
+-rw-rw-rw-   0        0        0    14375 2023-07-23 11:38:45.931121 SageLogger-1.3.2/PKG-INFO
+-rw-rw-rw-   0        0        0    13781 2023-07-23 11:37:53.000000 SageLogger-1.3.2/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 11:38:45.917469 SageLogger-1.3.2/SageLogger/
+-rw-rw-rw-   0        0        0    13166 2023-07-23 11:26:27.000000 SageLogger-1.3.2/SageLogger/Logger.py
+-rw-rw-rw-   0        0        0     1562 2023-07-23 11:22:55.000000 SageLogger-1.3.2/SageLogger/SageException.py
+-rw-rw-rw-   0        0        0     2954 2023-07-23 11:11:02.000000 SageLogger-1.3.2/SageLogger/SageFactory.py
+-rw-rw-rw-   0        0        0       15 2023-07-22 20:32:47.000000 SageLogger-1.3.2/SageLogger/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 11:38:45.928611 SageLogger-1.3.2/SageLogger.egg-info/
+-rw-rw-rw-   0        0        0    14375 2023-07-23 11:38:45.000000 SageLogger-1.3.2/SageLogger.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      300 2023-07-23 11:38:45.000000 SageLogger-1.3.2/SageLogger.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 11:38:45.000000 SageLogger-1.3.2/SageLogger.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       18 2023-07-23 11:38:45.000000 SageLogger-1.3.2/SageLogger.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       11 2023-07-23 11:38:45.000000 SageLogger-1.3.2/SageLogger.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      661 2023-07-23 11:38:29.000000 SageLogger-1.3.2/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-07-23 11:38:45.933205 SageLogger-1.3.2/setup.cfg
+-rw-rw-rw-   0        0        0     1069 2023-07-23 11:38:27.000000 SageLogger-1.3.2/setup.py
```

### Comparing `SageLogger-1.3.1/SageLogger/Logger.py` & `SageLogger-1.3.2/SageLogger/Logger.py`

 * *Files identical despite different names*

### Comparing `SageLogger-1.3.1/SageLogger/SageException.py` & `SageLogger-1.3.2/SageLogger/SageException.py`

 * *Files identical despite different names*

### Comparing `SageLogger-1.3.1/SageLogger/SageFactory.py` & `SageLogger-1.3.2/SageLogger/SageFactory.py`

 * *Files identical despite different names*

### Comparing `SageLogger-1.3.1/pyproject.toml` & `SageLogger-1.3.2/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["hatchling"]
 build-backend = "hatchling.build"
 
 [project]
 name = "SageLogger"
-version = "1.3.1"
+version = "1.3.2"
 authors = [
   { name="PanSageYT", email="pansage@hugedick.fyi" },
 ]
 description = "Yet another python logger, or is it like any other?"
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = [
```

### Comparing `SageLogger-1.3.1/setup.py` & `SageLogger-1.3.2/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 # Dane projektu
 project_name = "SageLogger"
-project_version = "1.3.1"
+project_version = "1.3.2"
 project_description = "Yet another python logger, or is it like any other?"
 project_author = "PanSageYT"
 project_author_email = "pansage@hugedick.fyi"
 
 # Zależności
 dependencies = [
     "colorama",
```

