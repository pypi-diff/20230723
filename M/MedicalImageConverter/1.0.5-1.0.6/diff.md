# Comparing `tmp/MedicalImageConverter-1.0.5.tar.gz` & `tmp/MedicalImageConverter-1.0.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "MedicalImageConverter-1.0.5.tar", last modified: Sun Jul 23 19:11:58 2023, max compression
+gzip compressed data, was "MedicalImageConverter-1.0.6.tar", last modified: Sun Jul 23 19:24:28 2023, max compression
```

## Comparing `MedicalImageConverter-1.0.5.tar` & `MedicalImageConverter-1.0.6.tar`

### file list

```diff
@@ -1,18 +1,12 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 19:11:58.234288 MedicalImageConverter-1.0.5/
--rw-rw-rw-   0        0        0    35821 2023-07-22 22:51:40.000000 MedicalImageConverter-1.0.5/LICENSE.txt
-drwxrwxrwx   0        0        0        0 2023-07-23 19:11:58.167894 MedicalImageConverter-1.0.5/MedicalImageConverter.egg-info/
--rw-rw-rw-   0        0        0     4823 2023-07-23 19:11:57.000000 MedicalImageConverter-1.0.5/MedicalImageConverter.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      352 2023-07-23 19:11:58.000000 MedicalImageConverter-1.0.5/MedicalImageConverter.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 19:11:57.000000 MedicalImageConverter-1.0.5/MedicalImageConverter.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       81 2023-07-23 19:11:57.000000 MedicalImageConverter-1.0.5/MedicalImageConverter.egg-info/requires.txt
--rw-rw-rw-   0        0        0       10 2023-07-23 19:11:57.000000 MedicalImageConverter-1.0.5/MedicalImageConverter.egg-info/top_level.txt
--rw-rw-rw-   0        0        0     4823 2023-07-23 19:11:58.224232 MedicalImageConverter-1.0.5/PKG-INFO
--rw-rw-rw-   0        0        0     4339 2023-07-23 00:28:45.000000 MedicalImageConverter-1.0.5/README.md
--rw-rw-rw-   0        0        0       42 2023-07-23 19:11:58.235296 MedicalImageConverter-1.0.5/setup.cfg
--rw-rw-rw-   0        0        0     1095 2023-07-23 19:11:02.000000 MedicalImageConverter-1.0.5/setup.py
-drwxrwxrwx   0        0        0        0 2023-07-23 19:11:58.059324 MedicalImageConverter-1.0.5/src/
-drwxrwxrwx   0        0        0        0 2023-07-23 19:11:58.211593 MedicalImageConverter-1.0.5/src/converter/
--rw-rw-rw-   0        0        0      102 2023-07-23 18:58:15.000000 MedicalImageConverter-1.0.5/src/converter/__init__.py
--rw-rw-rw-   0        0        0      682 2023-07-23 17:43:51.000000 MedicalImageConverter-1.0.5/src/converter/memory.py
--rw-rw-rw-   0        0        0     1281 2023-07-23 17:43:46.000000 MedicalImageConverter-1.0.5/src/converter/parsar.py
--rw-rw-rw-   0        0        0    22985 2023-07-23 17:43:58.000000 MedicalImageConverter-1.0.5/src/converter/reader.py
+drwxrwxrwx   0        0        0        0 2023-07-23 19:24:28.509984 MedicalImageConverter-1.0.6/
+-rw-rw-rw-   0        0        0    35821 2023-07-22 22:51:40.000000 MedicalImageConverter-1.0.6/LICENSE.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 19:24:28.492636 MedicalImageConverter-1.0.6/MedicalImageConverter.egg-info/
+-rw-rw-rw-   0        0        0     4823 2023-07-23 19:24:28.000000 MedicalImageConverter-1.0.6/MedicalImageConverter.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      254 2023-07-23 19:24:28.000000 MedicalImageConverter-1.0.6/MedicalImageConverter.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 19:24:28.000000 MedicalImageConverter-1.0.6/MedicalImageConverter.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       81 2023-07-23 19:24:28.000000 MedicalImageConverter-1.0.6/MedicalImageConverter.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 19:24:28.000000 MedicalImageConverter-1.0.6/MedicalImageConverter.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0     4823 2023-07-23 19:24:28.502955 MedicalImageConverter-1.0.6/PKG-INFO
+-rw-rw-rw-   0        0        0     4339 2023-07-23 00:28:45.000000 MedicalImageConverter-1.0.6/README.md
+-rw-rw-rw-   0        0        0       42 2023-07-23 19:24:28.509984 MedicalImageConverter-1.0.6/setup.cfg
+-rw-rw-rw-   0        0        0     1048 2023-07-23 19:23:42.000000 MedicalImageConverter-1.0.6/setup.py
```

### Comparing `MedicalImageConverter-1.0.5/LICENSE.txt` & `MedicalImageConverter-1.0.6/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `MedicalImageConverter-1.0.5/MedicalImageConverter.egg-info/PKG-INFO` & `MedicalImageConverter-1.0.6/MedicalImageConverter.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: MedicalImageConverter
-Version: 1.0.5
+Version: 1.0.6
 Summary: Reads in medical images and converts them into numpy arrays.
 Home-page: https://github.com/caleb-oconnor/MedicalImageConverter
 Author: Caleb OConnor
 Author-email: csoconnor@mdanderson.org
 Keywords: medical
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU Affero General Public License v3
```

### Comparing `MedicalImageConverter-1.0.5/PKG-INFO` & `MedicalImageConverter-1.0.6/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: MedicalImageConverter
-Version: 1.0.5
+Version: 1.0.6
 Summary: Reads in medical images and converts them into numpy arrays.
 Home-page: https://github.com/caleb-oconnor/MedicalImageConverter
 Author: Caleb OConnor
 Author-email: csoconnor@mdanderson.org
 Keywords: medical
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU Affero General Public License v3
```

### Comparing `MedicalImageConverter-1.0.5/README.md` & `MedicalImageConverter-1.0.6/README.md`

 * *Files identical despite different names*

### Comparing `MedicalImageConverter-1.0.5/setup.py` & `MedicalImageConverter-1.0.6/setup.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-__version__ = "1.0.5"
+__version__ = "1.0.6"
 __author__ = 'Caleb OConnor'
 __credits__ = 'MD Anderson Cancer Center'
 
 from setuptools import setup, find_packages
 
 with open("README.md", "r") as fh:
     long_description = fh.read()
@@ -12,16 +12,15 @@
     author=__author__,
     author_email='csoconnor@mdanderson.org',
     version=__version__,
     description='Reads in medical images and converts them into numpy arrays.',
     keywords='medical',
     long_description=long_description,
     long_description_content_type="text/markdown",
-    package_dir={'converter': 'src/converter'},
-    packages=['converter'],
+    packages=find_packages(),
     include_package_data=True,
     url='https://github.com/caleb-oconnor/MedicalImageConverter',
     classifiers=[
         "Programming Language :: Python :: 3",
         "License :: OSI Approved :: GNU Affero General Public License v3"
     ],
     install_requires=['numpy>=1.24.2',
```

