# Comparing `tmp/MedicalImageConverter-1.0.6.tar.gz` & `tmp/MedicalImageConverter-1.0.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "MedicalImageConverter-1.0.6.tar", last modified: Sun Jul 23 19:24:28 2023, max compression
+gzip compressed data, was "MedicalImageConverter-1.0.7.tar", last modified: Sun Jul 23 19:42:33 2023, max compression
```

## Comparing `MedicalImageConverter-1.0.6.tar` & `MedicalImageConverter-1.0.7.tar`

### file list

```diff
@@ -1,12 +1,17 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 19:24:28.509984 MedicalImageConverter-1.0.6/
--rw-rw-rw-   0        0        0    35821 2023-07-22 22:51:40.000000 MedicalImageConverter-1.0.6/LICENSE.txt
-drwxrwxrwx   0        0        0        0 2023-07-23 19:24:28.492636 MedicalImageConverter-1.0.6/MedicalImageConverter.egg-info/
--rw-rw-rw-   0        0        0     4823 2023-07-23 19:24:28.000000 MedicalImageConverter-1.0.6/MedicalImageConverter.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      254 2023-07-23 19:24:28.000000 MedicalImageConverter-1.0.6/MedicalImageConverter.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 19:24:28.000000 MedicalImageConverter-1.0.6/MedicalImageConverter.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       81 2023-07-23 19:24:28.000000 MedicalImageConverter-1.0.6/MedicalImageConverter.egg-info/requires.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 19:24:28.000000 MedicalImageConverter-1.0.6/MedicalImageConverter.egg-info/top_level.txt
--rw-rw-rw-   0        0        0     4823 2023-07-23 19:24:28.502955 MedicalImageConverter-1.0.6/PKG-INFO
--rw-rw-rw-   0        0        0     4339 2023-07-23 00:28:45.000000 MedicalImageConverter-1.0.6/README.md
--rw-rw-rw-   0        0        0       42 2023-07-23 19:24:28.509984 MedicalImageConverter-1.0.6/setup.cfg
--rw-rw-rw-   0        0        0     1048 2023-07-23 19:23:42.000000 MedicalImageConverter-1.0.6/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 19:42:33.902157 MedicalImageConverter-1.0.7/
+-rw-rw-rw-   0        0        0    35821 2023-07-22 22:51:40.000000 MedicalImageConverter-1.0.7/LICENSE.txt
+-rw-rw-rw-   0        0        0     4833 2023-07-23 19:42:33.890756 MedicalImageConverter-1.0.7/PKG-INFO
+-rw-rw-rw-   0        0        0     4339 2023-07-23 00:28:45.000000 MedicalImageConverter-1.0.7/README.md
+-rw-rw-rw-   0        0        0      745 2023-07-23 19:40:31.000000 MedicalImageConverter-1.0.7/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-07-23 19:42:33.902157 MedicalImageConverter-1.0.7/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-07-23 19:42:33.724574 MedicalImageConverter-1.0.7/src/
+drwxrwxrwx   0        0        0        0 2023-07-23 19:42:33.841995 MedicalImageConverter-1.0.7/src/MedicalImageConverter.egg-info/
+-rw-rw-rw-   0        0        0     4833 2023-07-23 19:42:33.000000 MedicalImageConverter-1.0.7/src/MedicalImageConverter.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      330 2023-07-23 19:42:33.000000 MedicalImageConverter-1.0.7/src/MedicalImageConverter.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 19:42:33.000000 MedicalImageConverter-1.0.7/src/MedicalImageConverter.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       10 2023-07-23 19:42:33.000000 MedicalImageConverter-1.0.7/src/MedicalImageConverter.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 19:42:33.878292 MedicalImageConverter-1.0.7/src/converter/
+-rw-rw-rw-   0        0        0      102 2023-07-23 18:58:15.000000 MedicalImageConverter-1.0.7/src/converter/__init__.py
+-rw-rw-rw-   0        0        0      682 2023-07-23 17:43:51.000000 MedicalImageConverter-1.0.7/src/converter/memory.py
+-rw-rw-rw-   0        0        0     1281 2023-07-23 17:43:46.000000 MedicalImageConverter-1.0.7/src/converter/parsar.py
+-rw-rw-rw-   0        0        0    22985 2023-07-23 17:43:58.000000 MedicalImageConverter-1.0.7/src/converter/reader.py
```

### Comparing `MedicalImageConverter-1.0.6/LICENSE.txt` & `MedicalImageConverter-1.0.7/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `MedicalImageConverter-1.0.6/MedicalImageConverter.egg-info/PKG-INFO` & `MedicalImageConverter-1.0.7/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,17 +1,16 @@
 Metadata-Version: 2.1
 Name: MedicalImageConverter
-Version: 1.0.6
+Version: 1.0.7
 Summary: Reads in medical images and converts them into numpy arrays.
-Home-page: https://github.com/caleb-oconnor/MedicalImageConverter
-Author: Caleb OConnor
-Author-email: csoconnor@mdanderson.org
-Keywords: medical
+Author-email: Caleb OConnor <csoconnor@mdanderson.org>
+Project-URL: Homepage, https://github.com/caleb-oconnor/MedicalImageConverter
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU Affero General Public License v3
+Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 License-File: LICENSE.txt
 
 
 # MedicalImageConverter
 
 *MedicalImageConverter* is a Python package for working with medical image files. It
```

### Comparing `MedicalImageConverter-1.0.6/PKG-INFO` & `MedicalImageConverter-1.0.7/src/MedicalImageConverter.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,17 +1,16 @@
 Metadata-Version: 2.1
 Name: MedicalImageConverter
-Version: 1.0.6
+Version: 1.0.7
 Summary: Reads in medical images and converts them into numpy arrays.
-Home-page: https://github.com/caleb-oconnor/MedicalImageConverter
-Author: Caleb OConnor
-Author-email: csoconnor@mdanderson.org
-Keywords: medical
+Author-email: Caleb OConnor <csoconnor@mdanderson.org>
+Project-URL: Homepage, https://github.com/caleb-oconnor/MedicalImageConverter
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU Affero General Public License v3
+Requires-Python: >=3.7
 Description-Content-Type: text/markdown
 License-File: LICENSE.txt
 
 
 # MedicalImageConverter
 
 *MedicalImageConverter* is a Python package for working with medical image files. It
```

### Comparing `MedicalImageConverter-1.0.6/README.md` & `MedicalImageConverter-1.0.7/README.md`

 * *Files identical despite different names*

