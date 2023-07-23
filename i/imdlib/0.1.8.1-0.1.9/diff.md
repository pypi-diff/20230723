# Comparing `tmp/imdlib-0.1.8.1.tar.gz` & `tmp/imdlib-0.1.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/imdlib-0.1.8.1.tar", last modified: Tue Dec 29 20:23:17 2020, max compression
+gzip compressed data, was "dist/imdlib-0.1.9.tar", last modified: Tue Dec 29 20:53:47 2020, max compression
```

## Comparing `imdlib-0.1.8.1.tar` & `imdlib-0.1.9.tar`

### file list

```diff
@@ -1,17 +1,17 @@
-drwxrwxr-x   0 travis    (2000) travis    (2000)        0 2020-12-29 20:23:17.000000 imdlib-0.1.8.1/
--rw-rw-r--   0 travis    (2000) travis    (2000)     1937 2020-12-29 20:23:17.000000 imdlib-0.1.8.1/PKG-INFO
--rw-rw-r--   0 travis    (2000) travis    (2000)      877 2020-12-29 20:21:45.000000 imdlib-0.1.8.1/README.md
-drwxrwxr-x   0 travis    (2000) travis    (2000)        0 2020-12-29 20:23:17.000000 imdlib-0.1.8.1/imdlib/
--rw-rw-r--   0 travis    (2000) travis    (2000)      121 2020-12-29 20:21:45.000000 imdlib-0.1.8.1/imdlib/__init__.py
--rw-rw-r--   0 travis    (2000) travis    (2000)    17740 2020-12-29 20:21:45.000000 imdlib-0.1.8.1/imdlib/core.py
--rw-rw-r--   0 travis    (2000) travis    (2000)     4897 2020-12-29 20:21:45.000000 imdlib-0.1.8.1/imdlib/util.py
-drwxrwxr-x   0 travis    (2000) travis    (2000)        0 2020-12-29 20:23:17.000000 imdlib-0.1.8.1/imdlib.egg-info/
--rw-rw-r--   0 travis    (2000) travis    (2000)     1937 2020-12-29 20:23:17.000000 imdlib-0.1.8.1/imdlib.egg-info/PKG-INFO
--rw-rw-r--   0 travis    (2000) travis    (2000)      229 2020-12-29 20:23:17.000000 imdlib-0.1.8.1/imdlib.egg-info/SOURCES.txt
--rw-rw-r--   0 travis    (2000) travis    (2000)        1 2020-12-29 20:23:17.000000 imdlib-0.1.8.1/imdlib.egg-info/dependency_links.txt
--rw-rw-r--   0 travis    (2000) travis    (2000)       78 2020-12-29 20:23:17.000000 imdlib-0.1.8.1/imdlib.egg-info/requires.txt
--rw-rw-r--   0 travis    (2000) travis    (2000)        7 2020-12-29 20:23:17.000000 imdlib-0.1.8.1/imdlib.egg-info/top_level.txt
--rw-rw-r--   0 travis    (2000) travis    (2000)       38 2020-12-29 20:23:17.000000 imdlib-0.1.8.1/setup.cfg
--rw-rw-r--   0 travis    (2000) travis    (2000)     1781 2020-12-29 20:21:45.000000 imdlib-0.1.8.1/setup.py
-drwxrwxr-x   0 travis    (2000) travis    (2000)        0 2020-12-29 20:23:17.000000 imdlib-0.1.8.1/test/
--rw-rw-r--   0 travis    (2000) travis    (2000)      311 2020-12-29 20:21:45.000000 imdlib-0.1.8.1/test/test.py
+drwxrwxr-x   0 travis    (2000) travis    (2000)        0 2020-12-29 20:53:47.000000 imdlib-0.1.9/
+-rw-rw-r--   0 travis    (2000) travis    (2000)     1950 2020-12-29 20:53:47.000000 imdlib-0.1.9/PKG-INFO
+-rw-rw-r--   0 travis    (2000) travis    (2000)      877 2020-12-29 20:52:23.000000 imdlib-0.1.9/README.md
+drwxrwxr-x   0 travis    (2000) travis    (2000)        0 2020-12-29 20:53:47.000000 imdlib-0.1.9/imdlib.egg-info/
+-rw-rw-r--   0 travis    (2000) travis    (2000)     1950 2020-12-29 20:53:47.000000 imdlib-0.1.9/imdlib.egg-info/PKG-INFO
+-rw-rw-r--   0 travis    (2000) travis    (2000)        1 2020-12-29 20:53:47.000000 imdlib-0.1.9/imdlib.egg-info/dependency_links.txt
+-rw-rw-r--   0 travis    (2000) travis    (2000)        7 2020-12-29 20:53:47.000000 imdlib-0.1.9/imdlib.egg-info/top_level.txt
+-rw-rw-r--   0 travis    (2000) travis    (2000)      229 2020-12-29 20:53:47.000000 imdlib-0.1.9/imdlib.egg-info/SOURCES.txt
+-rw-rw-r--   0 travis    (2000) travis    (2000)       78 2020-12-29 20:53:47.000000 imdlib-0.1.9/imdlib.egg-info/requires.txt
+-rw-rw-r--   0 travis    (2000) travis    (2000)       38 2020-12-29 20:53:47.000000 imdlib-0.1.9/setup.cfg
+drwxrwxr-x   0 travis    (2000) travis    (2000)        0 2020-12-29 20:53:47.000000 imdlib-0.1.9/imdlib/
+-rw-rw-r--   0 travis    (2000) travis    (2000)     4897 2020-12-29 20:52:23.000000 imdlib-0.1.9/imdlib/util.py
+-rw-rw-r--   0 travis    (2000) travis    (2000)    17740 2020-12-29 20:52:23.000000 imdlib-0.1.9/imdlib/core.py
+-rw-rw-r--   0 travis    (2000) travis    (2000)      121 2020-12-29 20:52:23.000000 imdlib-0.1.9/imdlib/__init__.py
+drwxrwxr-x   0 travis    (2000) travis    (2000)        0 2020-12-29 20:53:47.000000 imdlib-0.1.9/test/
+-rw-rw-r--   0 travis    (2000) travis    (2000)      311 2020-12-29 20:52:23.000000 imdlib-0.1.9/test/test.py
+-rw-rw-r--   0 travis    (2000) travis    (2000)     1794 2020-12-29 20:52:23.000000 imdlib-0.1.9/setup.py
```

### Comparing `imdlib-0.1.8.1/PKG-INFO` & `imdlib-0.1.9/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: imdlib
-Version: 0.1.8.1
+Version: 0.1.9
 Summary: A tool for handling and downloading IMD gridded data
 Home-page: https://github.com/iamsaswata/
 Author: Saswata Nandi
 Author-email: iamsaswata@yahoo.com
 License: MIT
 Description: # imdlib
         
@@ -34,15 +34,15 @@
         [Tutorial](https://saswatanandi.github.io/softwares/imdlib)
         [Tutorial](https://pratiman-91.github.io/blog.html)
         
         ## License
         
         imdlib is available under the open source [MIT](https://opensource.org/licenses/MIT).
         
-Keywords: imd,India,rainfall,IMD,grid,grided,gridded
+Keywords: imd,India,rainfall,data,hydrology,IMD,grid,grided,gridded
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers
 Classifier: Intended Audience :: Science/Research
```

### Comparing `imdlib-0.1.8.1/README.md` & `imdlib-0.1.9/README.md`

 * *Files identical despite different names*

### Comparing `imdlib-0.1.8.1/imdlib/core.py` & `imdlib-0.1.9/imdlib/core.py`

 * *Files identical despite different names*

### Comparing `imdlib-0.1.8.1/imdlib/util.py` & `imdlib-0.1.9/imdlib/util.py`

 * *Files identical despite different names*

### Comparing `imdlib-0.1.8.1/imdlib.egg-info/PKG-INFO` & `imdlib-0.1.9/imdlib.egg-info/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: imdlib
-Version: 0.1.8.1
+Version: 0.1.9
 Summary: A tool for handling and downloading IMD gridded data
 Home-page: https://github.com/iamsaswata/
 Author: Saswata Nandi
 Author-email: iamsaswata@yahoo.com
 License: MIT
 Description: # imdlib
         
@@ -34,15 +34,15 @@
         [Tutorial](https://saswatanandi.github.io/softwares/imdlib)
         [Tutorial](https://pratiman-91.github.io/blog.html)
         
         ## License
         
         imdlib is available under the open source [MIT](https://opensource.org/licenses/MIT).
         
-Keywords: imd,India,rainfall,IMD,grid,grided,gridded
+Keywords: imd,India,rainfall,data,hydrology,IMD,grid,grided,gridded
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers
 Classifier: Intended Audience :: Science/Research
```

### Comparing `imdlib-0.1.8.1/setup.py` & `imdlib-0.1.9/setup.py`

 * *Files 17% similar despite different names*

```diff
@@ -7,24 +7,24 @@
 import os
 import sys
 
 from setuptools import setup, find_packages
 from setuptools.command.install import install
 
 # imdlib version
-VERSION = "0.1.8.1"
+VERSION = "0.1.9"
 
 def readme():
     """print long description"""
     with open('README.md') as f:
         return f.read()
 
 setup(
     name="imdlib",
-    version="0.1.8.1",
+    version="0.1.9",
     author="Saswata Nandi",
     author_email="iamsaswata@yahoo.com",
     description="A tool for handling and downloading IMD gridded data",
     long_description=readme(),
     long_description_content_type="text/markdown",
     url="https://github.com/iamsaswata/",
     license="MIT",
@@ -38,15 +38,15 @@
                  "Intended Audience :: Science/Research",
                  "License :: OSI Approved :: MIT License",
                  "Operating System :: OS Independent",
                  "Topic :: Scientific/Engineering :: Hydrology",                 
                 ],
     python_requires='>=3.0',
 
-    keywords='imd, India, rainfall, IMD, grid, grided, gridded',
+    keywords='imd, India, rainfall, data, hydrology, IMD, grid, grided, gridded',
     # packages=['':'cct_nn'],
     install_requires=['matplotlib',
                       'numpy',
                       'pandas',
                       'six',
                       'pandas',
                       'python-dateutil',
```

