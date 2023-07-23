# Comparing `tmp/MedicalImageConverter-1.0.8.tar.gz` & `tmp/MedicalImageConverter-1.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "MedicalImageConverter-1.0.8.tar", last modified: Sun Jul 23 20:06:25 2023, max compression
+gzip compressed data, was "MedicalImageConverter-1.0.9.tar", last modified: Sun Jul 23 20:16:28 2023, max compression
```

## Comparing `MedicalImageConverter-1.0.8.tar` & `MedicalImageConverter-1.0.9.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 20:06:25.068453 MedicalImageConverter-1.0.8/
--rw-rw-rw-   0        0        0    35821 2023-07-22 22:51:40.000000 MedicalImageConverter-1.0.8/LICENSE.txt
--rw-rw-rw-   0        0        0     4833 2023-07-23 20:06:25.056348 MedicalImageConverter-1.0.8/PKG-INFO
--rw-rw-rw-   0        0        0     4339 2023-07-23 00:28:45.000000 MedicalImageConverter-1.0.8/README.md
--rw-rw-rw-   0        0        0      584 2023-07-23 20:05:22.000000 MedicalImageConverter-1.0.8/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-07-23 20:06:25.068453 MedicalImageConverter-1.0.8/setup.cfg
-drwxrwxrwx   0        0        0        0 2023-07-23 20:06:24.963335 MedicalImageConverter-1.0.8/src/
-drwxrwxrwx   0        0        0        0 2023-07-23 20:06:25.052948 MedicalImageConverter-1.0.8/src/MedicalImageConverter.egg-info/
--rw-rw-rw-   0        0        0     4833 2023-07-23 20:06:24.000000 MedicalImageConverter-1.0.8/src/MedicalImageConverter.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      290 2023-07-23 20:06:24.000000 MedicalImageConverter-1.0.8/src/MedicalImageConverter.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 20:06:24.000000 MedicalImageConverter-1.0.8/src/MedicalImageConverter.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       30 2023-07-23 20:06:24.000000 MedicalImageConverter-1.0.8/src/MedicalImageConverter.egg-info/top_level.txt
--rw-rw-rw-   0        0        0        2 2023-07-23 20:05:06.000000 MedicalImageConverter-1.0.8/src/__init__.py
--rw-rw-rw-   0        0        0      682 2023-07-23 17:43:51.000000 MedicalImageConverter-1.0.8/src/memory.py
--rw-rw-rw-   0        0        0     1281 2023-07-23 17:43:46.000000 MedicalImageConverter-1.0.8/src/parsar.py
--rw-rw-rw-   0        0        0    22985 2023-07-23 17:43:58.000000 MedicalImageConverter-1.0.8/src/reader.py
+drwxrwxrwx   0        0        0        0 2023-07-23 20:16:28.551686 MedicalImageConverter-1.0.9/
+-rw-rw-rw-   0        0        0    35821 2023-07-22 22:51:40.000000 MedicalImageConverter-1.0.9/LICENSE.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 20:16:28.500258 MedicalImageConverter-1.0.9/MedicalImageConverter.egg-info/
+-rw-rw-rw-   0        0        0     4828 2023-07-23 20:16:28.000000 MedicalImageConverter-1.0.9/MedicalImageConverter.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      284 2023-07-23 20:16:28.000000 MedicalImageConverter-1.0.9/MedicalImageConverter.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 20:16:28.000000 MedicalImageConverter-1.0.9/MedicalImageConverter.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        4 2023-07-23 20:16:28.000000 MedicalImageConverter-1.0.9/MedicalImageConverter.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0     4828 2023-07-23 20:16:28.551686 MedicalImageConverter-1.0.9/PKG-INFO
+-rw-rw-rw-   0        0        0     4339 2023-07-23 00:28:45.000000 MedicalImageConverter-1.0.9/README.md
+-rw-rw-rw-   0        0        0       97 2023-07-23 20:12:24.000000 MedicalImageConverter-1.0.9/pyproject.toml
+-rw-rw-rw-   0        0        0      594 2023-07-23 20:16:28.565819 MedicalImageConverter-1.0.9/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-07-23 20:16:28.551148 MedicalImageConverter-1.0.9/src/
+-rw-rw-rw-   0        0        0        2 2023-07-23 20:05:06.000000 MedicalImageConverter-1.0.9/src/__init__.py
+-rw-rw-rw-   0        0        0      682 2023-07-23 17:43:51.000000 MedicalImageConverter-1.0.9/src/memory.py
+-rw-rw-rw-   0        0        0     1281 2023-07-23 17:43:46.000000 MedicalImageConverter-1.0.9/src/parsar.py
+-rw-rw-rw-   0        0        0    22985 2023-07-23 17:43:58.000000 MedicalImageConverter-1.0.9/src/reader.py
```

### Comparing `MedicalImageConverter-1.0.8/LICENSE.txt` & `MedicalImageConverter-1.0.9/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `MedicalImageConverter-1.0.8/PKG-INFO` & `MedicalImageConverter-1.0.9/MedicalImageConverter.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,14 @@
 Metadata-Version: 2.1
 Name: MedicalImageConverter
-Version: 1.0.8
+Version: 1.0.9
 Summary: Reads in medical images and converts them into numpy arrays.
-Author-email: Caleb OConnor <csoconnor@mdanderson.org>
-Project-URL: Homepage, https://github.com/caleb-oconnor/MedicalImageConverter
+Home-page: https://github.com/caleb-oconnor/MedicalImageConverter
+Author: Caleb OConnor
+Author-email: csoconnor@mdanderson.org
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU Affero General Public License v3
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 License-File: LICENSE.txt
```

### Comparing `MedicalImageConverter-1.0.8/README.md` & `MedicalImageConverter-1.0.9/README.md`

 * *Files identical despite different names*

### Comparing `MedicalImageConverter-1.0.8/src/MedicalImageConverter.egg-info/PKG-INFO` & `MedicalImageConverter-1.0.9/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,14 @@
 Metadata-Version: 2.1
 Name: MedicalImageConverter
-Version: 1.0.8
+Version: 1.0.9
 Summary: Reads in medical images and converts them into numpy arrays.
-Author-email: Caleb OConnor <csoconnor@mdanderson.org>
-Project-URL: Homepage, https://github.com/caleb-oconnor/MedicalImageConverter
+Home-page: https://github.com/caleb-oconnor/MedicalImageConverter
+Author: Caleb OConnor
+Author-email: csoconnor@mdanderson.org
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU Affero General Public License v3
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 License-File: LICENSE.txt
```

### Comparing `MedicalImageConverter-1.0.8/src/memory.py` & `MedicalImageConverter-1.0.9/src/memory.py`

 * *Files identical despite different names*

### Comparing `MedicalImageConverter-1.0.8/src/parsar.py` & `MedicalImageConverter-1.0.9/src/parsar.py`

 * *Files identical despite different names*

### Comparing `MedicalImageConverter-1.0.8/src/reader.py` & `MedicalImageConverter-1.0.9/src/reader.py`

 * *Files identical despite different names*

