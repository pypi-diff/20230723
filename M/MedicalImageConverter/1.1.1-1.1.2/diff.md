# Comparing `tmp/MedicalImageConverter-1.1.1.tar.gz` & `tmp/MedicalImageConverter-1.1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "MedicalImageConverter-1.1.1.tar", last modified: Sun Jul 23 20:29:54 2023, max compression
+gzip compressed data, was "MedicalImageConverter-1.1.2.tar", last modified: Sun Jul 23 20:36:47 2023, max compression
```

## Comparing `MedicalImageConverter-1.1.1.tar` & `MedicalImageConverter-1.1.2.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 20:29:54.718122 MedicalImageConverter-1.1.1/
--rw-rw-rw-   0        0        0    35821 2023-07-22 22:51:40.000000 MedicalImageConverter-1.1.1/LICENSE.txt
-drwxrwxrwx   0        0        0        0 2023-07-23 20:29:54.676233 MedicalImageConverter-1.1.1/MedicalImageConverter/
--rw-rw-rw-   0        0        0        0 2023-07-23 20:21:28.000000 MedicalImageConverter-1.1.1/MedicalImageConverter/__init__.py
--rw-rw-rw-   0        0        0      682 2023-07-23 17:43:51.000000 MedicalImageConverter-1.1.1/MedicalImageConverter/memory.py
--rw-rw-rw-   0        0        0     1281 2023-07-23 17:43:46.000000 MedicalImageConverter-1.1.1/MedicalImageConverter/parsar.py
--rw-rw-rw-   0        0        0    22985 2023-07-23 17:43:58.000000 MedicalImageConverter-1.1.1/MedicalImageConverter/reader.py
-drwxrwxrwx   0        0        0        0 2023-07-23 20:29:54.713152 MedicalImageConverter-1.1.1/MedicalImageConverter.egg-info/
--rw-rw-rw-   0        0        0     4828 2023-07-23 20:29:54.000000 MedicalImageConverter-1.1.1/MedicalImageConverter.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      356 2023-07-23 20:29:54.000000 MedicalImageConverter-1.1.1/MedicalImageConverter.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 20:29:54.000000 MedicalImageConverter-1.1.1/MedicalImageConverter.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       22 2023-07-23 20:29:54.000000 MedicalImageConverter-1.1.1/MedicalImageConverter.egg-info/top_level.txt
--rw-rw-rw-   0        0        0     4828 2023-07-23 20:29:54.719352 MedicalImageConverter-1.1.1/PKG-INFO
--rw-rw-rw-   0        0        0     4339 2023-07-23 00:28:45.000000 MedicalImageConverter-1.1.1/README.md
--rw-rw-rw-   0        0        0       97 2023-07-23 20:12:24.000000 MedicalImageConverter-1.1.1/pyproject.toml
--rw-rw-rw-   0        0        0      594 2023-07-23 20:29:54.725190 MedicalImageConverter-1.1.1/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-07-23 20:36:47.958167 MedicalImageConverter-1.1.2/
+-rw-rw-rw-   0        0        0    35821 2023-07-22 22:51:40.000000 MedicalImageConverter-1.1.2/LICENSE.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 20:36:47.915709 MedicalImageConverter-1.1.2/MedicalImageConverter/
+-rw-rw-rw-   0        0        0      102 2023-07-23 20:35:17.000000 MedicalImageConverter-1.1.2/MedicalImageConverter/__init__.py
+-rw-rw-rw-   0        0        0      682 2023-07-23 17:43:51.000000 MedicalImageConverter-1.1.2/MedicalImageConverter/memory.py
+-rw-rw-rw-   0        0        0     1281 2023-07-23 17:43:46.000000 MedicalImageConverter-1.1.2/MedicalImageConverter/parsar.py
+-rw-rw-rw-   0        0        0    22985 2023-07-23 17:43:58.000000 MedicalImageConverter-1.1.2/MedicalImageConverter/reader.py
+drwxrwxrwx   0        0        0        0 2023-07-23 20:36:47.958167 MedicalImageConverter-1.1.2/MedicalImageConverter.egg-info/
+-rw-rw-rw-   0        0        0     4828 2023-07-23 20:36:47.000000 MedicalImageConverter-1.1.2/MedicalImageConverter.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      356 2023-07-23 20:36:47.000000 MedicalImageConverter-1.1.2/MedicalImageConverter.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 20:36:47.000000 MedicalImageConverter-1.1.2/MedicalImageConverter.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       22 2023-07-23 20:36:47.000000 MedicalImageConverter-1.1.2/MedicalImageConverter.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0     4828 2023-07-23 20:36:47.965752 MedicalImageConverter-1.1.2/PKG-INFO
+-rw-rw-rw-   0        0        0     4339 2023-07-23 00:28:45.000000 MedicalImageConverter-1.1.2/README.md
+-rw-rw-rw-   0        0        0       97 2023-07-23 20:12:24.000000 MedicalImageConverter-1.1.2/pyproject.toml
+-rw-rw-rw-   0        0        0      594 2023-07-23 20:36:47.969566 MedicalImageConverter-1.1.2/setup.cfg
```

### Comparing `MedicalImageConverter-1.1.1/LICENSE.txt` & `MedicalImageConverter-1.1.2/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `MedicalImageConverter-1.1.1/MedicalImageConverter/memory.py` & `MedicalImageConverter-1.1.2/MedicalImageConverter/memory.py`

 * *Files identical despite different names*

### Comparing `MedicalImageConverter-1.1.1/MedicalImageConverter/parsar.py` & `MedicalImageConverter-1.1.2/MedicalImageConverter/parsar.py`

 * *Files identical despite different names*

### Comparing `MedicalImageConverter-1.1.1/MedicalImageConverter/reader.py` & `MedicalImageConverter-1.1.2/MedicalImageConverter/reader.py`

 * *Files identical despite different names*

### Comparing `MedicalImageConverter-1.1.1/MedicalImageConverter.egg-info/PKG-INFO` & `MedicalImageConverter-1.1.2/MedicalImageConverter.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: MedicalImageConverter
-Version: 1.1.1
+Version: 1.1.2
 Summary: Reads in medical images and converts them into numpy arrays.
 Home-page: https://github.com/caleb-oconnor/MedicalImageConverter
 Author: Caleb OConnor
 Author-email: csoconnor@mdanderson.org
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU Affero General Public License v3
 Requires-Python: >=3.7
```

### Comparing `MedicalImageConverter-1.1.1/PKG-INFO` & `MedicalImageConverter-1.1.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: MedicalImageConverter
-Version: 1.1.1
+Version: 1.1.2
 Summary: Reads in medical images and converts them into numpy arrays.
 Home-page: https://github.com/caleb-oconnor/MedicalImageConverter
 Author: Caleb OConnor
 Author-email: csoconnor@mdanderson.org
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU Affero General Public License v3
 Requires-Python: >=3.7
```

### Comparing `MedicalImageConverter-1.1.1/README.md` & `MedicalImageConverter-1.1.2/README.md`

 * *Files identical despite different names*

### Comparing `MedicalImageConverter-1.1.1/setup.cfg` & `MedicalImageConverter-1.1.2/setup.cfg`

 * *Files 19% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 00000000: 5b6d 6574 6164 6174 615d 0d0a 6e61 6d65  [metadata]..name
 00000010: 203d 204d 6564 6963 616c 496d 6167 6543   = MedicalImageC
 00000020: 6f6e 7665 7274 6572 0d0a 7665 7273 696f  onverter..versio
-00000030: 6e20 3d20 312e 312e 310d 0a61 7574 686f  n = 1.1.1..autho
+00000030: 6e20 3d20 312e 312e 320d 0a61 7574 686f  n = 1.1.2..autho
 00000040: 7220 3d20 4361 6c65 6220 4f43 6f6e 6e6f  r = Caleb OConno
 00000050: 720d 0a61 7574 686f 725f 656d 6169 6c20  r..author_email 
 00000060: 3d20 6373 6f63 6f6e 6e6f 7240 6d64 616e  = csoconnor@mdan
 00000070: 6465 7273 6f6e 2e6f 7267 0d0a 6465 7363  derson.org..desc
 00000080: 7269 7074 696f 6e20 3d20 5265 6164 7320  ription = Reads 
 00000090: 696e 206d 6564 6963 616c 2069 6d61 6765  in medical image
 000000a0: 7320 616e 6420 636f 6e76 6572 7473 2074  s and converts t
```

