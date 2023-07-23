# Comparing `tmp/MedicalImageConverter-1.0.0.tar.gz` & `tmp/MedicalImageConverter-1.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "MedicalImageConverter-1.0.0.tar", last modified: Sun Jul 23 02:46:32 2023, max compression
+gzip compressed data, was "MedicalImageConverter-1.0.1.tar", last modified: Sun Jul 23 05:28:02 2023, max compression
```

## Comparing `MedicalImageConverter-1.0.0.tar` & `MedicalImageConverter-1.0.1.tar`

### file list

```diff
@@ -1,17 +1,17 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 02:46:32.204641 MedicalImageConverter-1.0.0/
--rw-rw-rw-   0        0        0    35821 2023-07-22 22:51:40.000000 MedicalImageConverter-1.0.0/LICENSE.txt
-drwxrwxrwx   0        0        0        0 2023-07-23 02:46:32.091965 MedicalImageConverter-1.0.0/MedicalImageConverter.egg-info/
--rw-rw-rw-   0        0        0     4804 2023-07-23 02:46:31.000000 MedicalImageConverter-1.0.0/MedicalImageConverter.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      312 2023-07-23 02:46:31.000000 MedicalImageConverter-1.0.0/MedicalImageConverter.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 02:46:31.000000 MedicalImageConverter-1.0.0/MedicalImageConverter.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0      120 2023-07-23 02:46:31.000000 MedicalImageConverter-1.0.0/MedicalImageConverter.egg-info/requires.txt
--rw-rw-rw-   0        0        0       22 2023-07-23 02:46:31.000000 MedicalImageConverter-1.0.0/MedicalImageConverter.egg-info/top_level.txt
--rw-rw-rw-   0        0        0     4804 2023-07-23 02:46:32.185586 MedicalImageConverter-1.0.0/PKG-INFO
--rw-rw-rw-   0        0        0     4339 2023-07-23 00:28:45.000000 MedicalImageConverter-1.0.0/README.md
--rw-rw-rw-   0        0        0       42 2023-07-23 02:46:32.204641 MedicalImageConverter-1.0.0/setup.cfg
--rw-rw-rw-   0        0        0      912 2023-07-22 23:21:25.000000 MedicalImageConverter-1.0.0/setup.py
-drwxrwxrwx   0        0        0        0 2023-07-23 02:46:32.154350 MedicalImageConverter-1.0.0/src/
--rw-rw-rw-   0        0        0       98 2023-07-22 22:41:13.000000 MedicalImageConverter-1.0.0/src/__init__.py
--rw-rw-rw-   0        0        0      640 2023-07-21 18:29:26.000000 MedicalImageConverter-1.0.0/src/memory.py
--rw-rw-rw-   0        0        0     1239 2023-07-21 18:29:26.000000 MedicalImageConverter-1.0.0/src/parsar.py
--rw-rw-rw-   0        0        0    22943 2023-07-23 02:29:52.000000 MedicalImageConverter-1.0.0/src/reader.py
+drwxrwxrwx   0        0        0        0 2023-07-23 05:28:02.896764 MedicalImageConverter-1.0.1/
+-rw-rw-rw-   0        0        0    35821 2023-07-22 22:51:40.000000 MedicalImageConverter-1.0.1/LICENSE.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 05:28:02.846413 MedicalImageConverter-1.0.1/MedicalImageConverter.egg-info/
+-rw-rw-rw-   0        0        0     4804 2023-07-23 05:28:02.000000 MedicalImageConverter-1.0.1/MedicalImageConverter.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      312 2023-07-23 05:28:02.000000 MedicalImageConverter-1.0.1/MedicalImageConverter.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 05:28:02.000000 MedicalImageConverter-1.0.1/MedicalImageConverter.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       81 2023-07-23 05:28:02.000000 MedicalImageConverter-1.0.1/MedicalImageConverter.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       22 2023-07-23 05:28:02.000000 MedicalImageConverter-1.0.1/MedicalImageConverter.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0     4804 2023-07-23 05:28:02.894266 MedicalImageConverter-1.0.1/PKG-INFO
+-rw-rw-rw-   0        0        0     4339 2023-07-23 00:28:45.000000 MedicalImageConverter-1.0.1/README.md
+-rw-rw-rw-   0        0        0       42 2023-07-23 05:28:02.896764 MedicalImageConverter-1.0.1/setup.cfg
+-rw-rw-rw-   0        0        0     1016 2023-07-23 05:26:29.000000 MedicalImageConverter-1.0.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 05:28:02.881680 MedicalImageConverter-1.0.1/src/
+-rw-rw-rw-   0        0        0       98 2023-07-23 04:33:09.000000 MedicalImageConverter-1.0.1/src/__init__.py
+-rw-rw-rw-   0        0        0      640 2023-07-21 18:29:26.000000 MedicalImageConverter-1.0.1/src/memory.py
+-rw-rw-rw-   0        0        0     1239 2023-07-21 18:29:26.000000 MedicalImageConverter-1.0.1/src/parsar.py
+-rw-rw-rw-   0        0        0    22943 2023-07-23 02:29:52.000000 MedicalImageConverter-1.0.1/src/reader.py
```

### Comparing `MedicalImageConverter-1.0.0/LICENSE.txt` & `MedicalImageConverter-1.0.1/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `MedicalImageConverter-1.0.0/MedicalImageConverter.egg-info/PKG-INFO` & `MedicalImageConverter-1.0.1/MedicalImageConverter.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: MedicalImageConverter
-Version: 1.0.0
+Version: 1.0.1
 Summary: Reads in medical images and converts them into numpy arrays.
 Home-page: https://github.com/caleb-oconnor/MedicalImageConverter
 Author: Caleb OConnor
 Author-email: csoconnor@mdanderson.org
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU Affero General Public License v3
 Description-Content-Type: text/markdown
```

### Comparing `MedicalImageConverter-1.0.0/PKG-INFO` & `MedicalImageConverter-1.0.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: MedicalImageConverter
-Version: 1.0.0
+Version: 1.0.1
 Summary: Reads in medical images and converts them into numpy arrays.
 Home-page: https://github.com/caleb-oconnor/MedicalImageConverter
 Author: Caleb OConnor
 Author-email: csoconnor@mdanderson.org
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU Affero General Public License v3
 Description-Content-Type: text/markdown
```

### Comparing `MedicalImageConverter-1.0.0/README.md` & `MedicalImageConverter-1.0.1/README.md`

 * *Files identical despite different names*

### Comparing `MedicalImageConverter-1.0.0/src/memory.py` & `MedicalImageConverter-1.0.1/src/memory.py`

 * *Files identical despite different names*

### Comparing `MedicalImageConverter-1.0.0/src/parsar.py` & `MedicalImageConverter-1.0.1/src/parsar.py`

 * *Files identical despite different names*

### Comparing `MedicalImageConverter-1.0.0/src/reader.py` & `MedicalImageConverter-1.0.1/src/reader.py`

 * *Files identical despite different names*

