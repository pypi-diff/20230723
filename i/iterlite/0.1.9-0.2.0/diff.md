# Comparing `tmp/iterlite-0.1.9.tar.gz` & `tmp/iterlite-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "iterlite-0.1.9.tar", last modified: Tue Jun 27 18:09:25 2023, max compression
+gzip compressed data, was "iterlite-0.2.0.tar", last modified: Sun Jul 23 20:33:28 2023, max compression
```

## Comparing `iterlite-0.1.9.tar` & `iterlite-0.2.0.tar`

### file list

```diff
@@ -1,13 +1,13 @@
-drwxrwxrwx   0        0        0        0 2023-06-27 18:09:25.311889 iterlite-0.1.9/
--rw-rw-rw-   0        0        0     1968 2023-06-27 18:09:25.311889 iterlite-0.1.9/PKG-INFO
--rw-rw-rw-   0        0        0     1432 2023-06-27 16:54:51.000000 iterlite-0.1.9/README.md
-drwxrwxrwx   0        0        0        0 2023-06-27 18:09:25.287091 iterlite-0.1.9/iterlite/
--rw-rw-rw-   0        0        0       58 2023-06-27 16:37:31.000000 iterlite-0.1.9/iterlite/__init__.py
--rw-rw-rw-   0        0        0     4428 2023-06-27 18:09:03.000000 iterlite-0.1.9/iterlite/enumerable.py
-drwxrwxrwx   0        0        0        0 2023-06-27 18:09:25.308868 iterlite-0.1.9/iterlite.egg-info/
--rw-rw-rw-   0        0        0     1968 2023-06-27 18:09:25.000000 iterlite-0.1.9/iterlite.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      190 2023-06-27 18:09:25.000000 iterlite-0.1.9/iterlite.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-06-27 18:09:25.000000 iterlite-0.1.9/iterlite.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        9 2023-06-27 18:09:25.000000 iterlite-0.1.9/iterlite.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-06-27 18:09:25.313092 iterlite-0.1.9/setup.cfg
--rw-rw-rw-   0        0        0      807 2023-06-27 18:09:07.000000 iterlite-0.1.9/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 20:33:28.010592 iterlite-0.2.0/
+-rw-rw-rw-   0        0        0     1968 2023-07-23 20:33:28.009593 iterlite-0.2.0/PKG-INFO
+-rw-rw-rw-   0        0        0     1432 2023-06-27 16:54:51.000000 iterlite-0.2.0/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 20:33:28.002586 iterlite-0.2.0/iterlite/
+-rw-rw-rw-   0        0        0       80 2023-07-23 20:31:24.000000 iterlite-0.2.0/iterlite/__init__.py
+-rw-rw-rw-   0        0        0     7414 2023-07-23 20:31:06.000000 iterlite-0.2.0/iterlite/enumerable.py
+drwxrwxrwx   0        0        0        0 2023-07-23 20:33:28.008594 iterlite-0.2.0/iterlite.egg-info/
+-rw-rw-rw-   0        0        0     1968 2023-07-23 20:33:27.000000 iterlite-0.2.0/iterlite.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      190 2023-07-23 20:33:27.000000 iterlite-0.2.0/iterlite.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 20:33:27.000000 iterlite-0.2.0/iterlite.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        9 2023-07-23 20:33:27.000000 iterlite-0.2.0/iterlite.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 20:33:28.010592 iterlite-0.2.0/setup.cfg
+-rw-rw-rw-   0        0        0      845 2023-07-05 12:40:32.000000 iterlite-0.2.0/setup.py
```

### Comparing `iterlite-0.1.9/PKG-INFO` & `iterlite-0.2.0/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: iterlite
-Version: 0.1.9
+Version: 0.2.0
 Summary: rust like iterators for python
 Home-page: https://github.com/peturparkur/python-rustlite
 Author: Peter Nagymathe
 Author-email: peter@nagymathe.xyz
 License: AGPLv3+
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3 :: Only
```

### Comparing `iterlite-0.1.9/README.md` & `iterlite-0.2.0/README.md`

 * *Files identical despite different names*

### Comparing `iterlite-0.1.9/iterlite.egg-info/PKG-INFO` & `iterlite-0.2.0/iterlite.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: iterlite
-Version: 0.1.9
+Version: 0.2.0
 Summary: rust like iterators for python
 Home-page: https://github.com/peturparkur/python-rustlite
 Author: Peter Nagymathe
 Author-email: peter@nagymathe.xyz
 License: AGPLv3+
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3 :: Only
```

### Comparing `iterlite-0.1.9/setup.py` & `iterlite-0.2.0/setup.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,16 +1,17 @@
 from setuptools import setup
+from iterlite import __version__
 
 from pathlib import Path
 this_directory = Path(__file__).parent
 long_description = (this_directory / "README.md").read_text()
 
 setup(
     name='iterlite',
-    version='0.1.9',    
+    version=__version__,    
     description='rust like iterators for python',
     long_description=long_description,
     long_description_content_type='text/markdown',
     url='https://github.com/peturparkur/python-rustlite',
     author='Peter Nagymathe',
     author_email='peter@nagymathe.xyz',
     license='AGPLv3+',
```

