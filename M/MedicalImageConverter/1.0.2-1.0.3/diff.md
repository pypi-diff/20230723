# Comparing `tmp/MedicalImageConverter-1.0.2.tar.gz` & `tmp/MedicalImageConverter-1.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "MedicalImageConverter-1.0.2.tar", last modified: Sun Jul 23 06:05:32 2023, max compression
+gzip compressed data, was "MedicalImageConverter-1.0.3.tar", last modified: Sun Jul 23 16:11:22 2023, max compression
```

## Comparing `MedicalImageConverter-1.0.2.tar` & `MedicalImageConverter-1.0.3.tar`

### file list

```diff
@@ -1,17 +1,18 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 06:05:32.471350 MedicalImageConverter-1.0.2/
--rw-rw-rw-   0        0        0    35821 2023-07-22 22:51:40.000000 MedicalImageConverter-1.0.2/LICENSE.txt
-drwxrwxrwx   0        0        0        0 2023-07-23 06:05:32.414403 MedicalImageConverter-1.0.2/MedicalImageConverter.egg-info/
--rw-rw-rw-   0        0        0     4804 2023-07-23 06:05:32.000000 MedicalImageConverter-1.0.2/MedicalImageConverter.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      312 2023-07-23 06:05:32.000000 MedicalImageConverter-1.0.2/MedicalImageConverter.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 06:05:32.000000 MedicalImageConverter-1.0.2/MedicalImageConverter.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       81 2023-07-23 06:05:32.000000 MedicalImageConverter-1.0.2/MedicalImageConverter.egg-info/requires.txt
--rw-rw-rw-   0        0        0       22 2023-07-23 06:05:32.000000 MedicalImageConverter-1.0.2/MedicalImageConverter.egg-info/top_level.txt
--rw-rw-rw-   0        0        0     4804 2023-07-23 06:05:32.449632 MedicalImageConverter-1.0.2/PKG-INFO
--rw-rw-rw-   0        0        0     4339 2023-07-23 00:28:45.000000 MedicalImageConverter-1.0.2/README.md
--rw-rw-rw-   0        0        0       42 2023-07-23 06:05:32.472350 MedicalImageConverter-1.0.2/setup.cfg
--rw-rw-rw-   0        0        0     1016 2023-07-23 05:26:29.000000 MedicalImageConverter-1.0.2/setup.py
-drwxrwxrwx   0        0        0        0 2023-07-23 06:05:32.449632 MedicalImageConverter-1.0.2/src/
--rw-rw-rw-   0        0        0       98 2023-07-23 06:04:45.000000 MedicalImageConverter-1.0.2/src/__init__.py
--rw-rw-rw-   0        0        0      640 2023-07-21 18:29:26.000000 MedicalImageConverter-1.0.2/src/memory.py
--rw-rw-rw-   0        0        0     1239 2023-07-21 18:29:26.000000 MedicalImageConverter-1.0.2/src/parsar.py
--rw-rw-rw-   0        0        0    22943 2023-07-23 02:29:52.000000 MedicalImageConverter-1.0.2/src/reader.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:11:22.353524 MedicalImageConverter-1.0.3/
+-rw-rw-rw-   0        0        0    35821 2023-07-22 22:51:40.000000 MedicalImageConverter-1.0.3/LICENSE.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 16:11:22.303300 MedicalImageConverter-1.0.3/MedicalImageConverter.egg-info/
+-rw-rw-rw-   0        0        0     4804 2023-07-23 16:11:22.000000 MedicalImageConverter-1.0.3/MedicalImageConverter.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      400 2023-07-23 16:11:22.000000 MedicalImageConverter-1.0.3/MedicalImageConverter.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 16:11:22.000000 MedicalImageConverter-1.0.3/MedicalImageConverter.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       81 2023-07-23 16:11:22.000000 MedicalImageConverter-1.0.3/MedicalImageConverter.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       22 2023-07-23 16:11:22.000000 MedicalImageConverter-1.0.3/MedicalImageConverter.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0     4804 2023-07-23 16:11:22.345218 MedicalImageConverter-1.0.3/PKG-INFO
+-rw-rw-rw-   0        0        0     4339 2023-07-23 00:28:45.000000 MedicalImageConverter-1.0.3/README.md
+-rw-rw-rw-   0        0        0       42 2023-07-23 16:11:22.353524 MedicalImageConverter-1.0.3/setup.cfg
+-rw-rw-rw-   0        0        0     1093 2023-07-23 16:10:25.000000 MedicalImageConverter-1.0.3/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:11:22.190144 MedicalImageConverter-1.0.3/src/
+drwxrwxrwx   0        0        0        0 2023-07-23 16:11:22.340808 MedicalImageConverter-1.0.3/src/MedicalImageConverter/
+-rw-rw-rw-   0        0        0        0 2023-07-23 16:07:50.000000 MedicalImageConverter-1.0.3/src/MedicalImageConverter/__init__.py
+-rw-rw-rw-   0        0        0      640 2023-07-21 18:29:26.000000 MedicalImageConverter-1.0.3/src/MedicalImageConverter/memory.py
+-rw-rw-rw-   0        0        0     1239 2023-07-21 18:29:26.000000 MedicalImageConverter-1.0.3/src/MedicalImageConverter/parsar.py
+-rw-rw-rw-   0        0        0    22943 2023-07-23 15:50:20.000000 MedicalImageConverter-1.0.3/src/MedicalImageConverter/reader.py
```

### Comparing `MedicalImageConverter-1.0.2/LICENSE.txt` & `MedicalImageConverter-1.0.3/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `MedicalImageConverter-1.0.2/MedicalImageConverter.egg-info/PKG-INFO` & `MedicalImageConverter-1.0.3/MedicalImageConverter.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: MedicalImageConverter
-Version: 1.0.2
+Version: 1.0.3
 Summary: Reads in medical images and converts them into numpy arrays.
 Home-page: https://github.com/caleb-oconnor/MedicalImageConverter
 Author: Caleb OConnor
 Author-email: csoconnor@mdanderson.org
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU Affero General Public License v3
 Description-Content-Type: text/markdown
```

### Comparing `MedicalImageConverter-1.0.2/PKG-INFO` & `MedicalImageConverter-1.0.3/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: MedicalImageConverter
-Version: 1.0.2
+Version: 1.0.3
 Summary: Reads in medical images and converts them into numpy arrays.
 Home-page: https://github.com/caleb-oconnor/MedicalImageConverter
 Author: Caleb OConnor
 Author-email: csoconnor@mdanderson.org
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU Affero General Public License v3
 Description-Content-Type: text/markdown
```

### Comparing `MedicalImageConverter-1.0.2/README.md` & `MedicalImageConverter-1.0.3/README.md`

 * *Files identical despite different names*

### Comparing `MedicalImageConverter-1.0.2/setup.py` & `MedicalImageConverter-1.0.3/setup.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,24 +1,26 @@
 
-from setuptools import setup
+__version__ = "1.0.3"
+__author__ = 'Caleb OConnor'
+__credits__ = 'MD Anderson Cancer Center'
 
-from src import __version__, __author__
+from setuptools import setup
 
 with open("README.md", "r") as fh:
     long_description = fh.read()
 
 setup(
     name='MedicalImageConverter',
     author=__author__,
     author_email='csoconnor@mdanderson.org',
     version=__version__,
     description='Reads in medical images and converts them into numpy arrays.',
     long_description=long_description,
     long_description_content_type="text/markdown",
-    package_dir={'MedicalImageConverter': 'src'},
+    package_dir={'MedicalImageConverter': 'src/MedicalImageConverter'},
     packages=['MedicalImageConverter'],
     include_package_data=True,
     url='https://github.com/caleb-oconnor/MedicalImageConverter',
     classifiers=[
         "Programming Language :: Python :: 3",
         "License :: OSI Approved :: GNU Affero General Public License v3"
     ],
```

### Comparing `MedicalImageConverter-1.0.2/src/memory.py` & `MedicalImageConverter-1.0.3/src/MedicalImageConverter/memory.py`

 * *Files identical despite different names*

### Comparing `MedicalImageConverter-1.0.2/src/parsar.py` & `MedicalImageConverter-1.0.3/src/MedicalImageConverter/parsar.py`

 * *Files identical despite different names*

### Comparing `MedicalImageConverter-1.0.2/src/reader.py` & `MedicalImageConverter-1.0.3/src/MedicalImageConverter/reader.py`

 * *Files identical despite different names*

