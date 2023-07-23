# Comparing `tmp/UploadHub-0.0.1.tar.gz` & `tmp/UploadHub-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "UploadHub-0.0.1.tar", last modified: Sun Jul 23 05:06:26 2023, max compression
+gzip compressed data, was "UploadHub-0.0.2.tar", last modified: Sun Jul 23 05:11:06 2023, max compression
```

## Comparing `UploadHub-0.0.1.tar` & `UploadHub-0.0.2.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 05:06:26.367210 UploadHub-0.0.1/
--rw-rw-rw-   0        0        0     1088 2023-07-19 04:27:02.000000 UploadHub-0.0.1/LICENSE
--rw-rw-rw-   0        0        0      516 2023-07-23 05:06:26.365211 UploadHub-0.0.1/PKG-INFO
--rw-rw-rw-   0        0        0        0 2023-07-18 18:43:42.000000 UploadHub-0.0.1/README.md
-drwxrwxrwx   0        0        0        0 2023-07-23 05:06:26.311205 UploadHub-0.0.1/UploadHub/
--rw-rw-rw-   0        0        0        0 2023-07-23 05:01:02.000000 UploadHub-0.0.1/UploadHub/__init__.py
--rw-rw-rw-   0        0        0      702 2023-07-23 05:01:23.000000 UploadHub-0.0.1/UploadHub/__main__.py
--rw-rw-rw-   0        0        0     1088 2023-07-19 04:27:06.000000 UploadHub-0.0.1/UploadHub/license.py
--rw-rw-rw-   0        0        0     9814 2023-07-23 05:01:10.000000 UploadHub-0.0.1/UploadHub/new.py
--rw-rw-rw-   0        0        0      651 2023-07-19 04:20:31.000000 UploadHub-0.0.1/UploadHub/setup.py
--rw-rw-rw-   0        0        0     8233 2023-07-23 05:02:24.000000 UploadHub-0.0.1/UploadHub/upload.py
--rw-rw-rw-   0        0        0     2335 2023-07-23 04:57:52.000000 UploadHub-0.0.1/UploadHub/utils.py
-drwxrwxrwx   0        0        0        0 2023-07-23 05:06:26.362209 UploadHub-0.0.1/UploadHub.egg-info/
--rw-rw-rw-   0        0        0      516 2023-07-23 05:06:26.000000 UploadHub-0.0.1/UploadHub.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      330 2023-07-23 05:06:26.000000 UploadHub-0.0.1/UploadHub.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 05:06:26.000000 UploadHub-0.0.1/UploadHub.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       19 2023-07-23 05:06:26.000000 UploadHub-0.0.1/UploadHub.egg-info/requires.txt
--rw-rw-rw-   0        0        0       10 2023-07-23 05:06:26.000000 UploadHub-0.0.1/UploadHub.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-23 05:06:26.367210 UploadHub-0.0.1/setup.cfg
--rw-rw-rw-   0        0        0      811 2023-07-23 05:06:14.000000 UploadHub-0.0.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 05:11:06.469848 UploadHub-0.0.2/
+-rw-rw-rw-   0        0        0     1088 2023-07-19 04:27:02.000000 UploadHub-0.0.2/LICENSE
+-rw-rw-rw-   0        0        0      516 2023-07-23 05:11:06.467849 UploadHub-0.0.2/PKG-INFO
+-rw-rw-rw-   0        0        0        0 2023-07-18 18:43:42.000000 UploadHub-0.0.2/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 05:11:06.428014 UploadHub-0.0.2/UploadHub/
+-rw-rw-rw-   0        0        0        0 2023-07-23 05:01:02.000000 UploadHub-0.0.2/UploadHub/__init__.py
+-rw-rw-rw-   0        0        0      704 2023-07-23 05:09:33.000000 UploadHub-0.0.2/UploadHub/__main__.py
+-rw-rw-rw-   0        0        0     1088 2023-07-19 04:27:06.000000 UploadHub-0.0.2/UploadHub/license.py
+-rw-rw-rw-   0        0        0     9815 2023-07-23 05:09:52.000000 UploadHub-0.0.2/UploadHub/new.py
+-rw-rw-rw-   0        0        0      651 2023-07-19 04:20:31.000000 UploadHub-0.0.2/UploadHub/setup.py
+-rw-rw-rw-   0        0        0     8234 2023-07-23 05:09:49.000000 UploadHub-0.0.2/UploadHub/upload.py
+-rw-rw-rw-   0        0        0     2335 2023-07-23 04:57:52.000000 UploadHub-0.0.2/UploadHub/utils.py
+drwxrwxrwx   0        0        0        0 2023-07-23 05:11:06.464863 UploadHub-0.0.2/UploadHub.egg-info/
+-rw-rw-rw-   0        0        0      516 2023-07-23 05:11:06.000000 UploadHub-0.0.2/UploadHub.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      330 2023-07-23 05:11:06.000000 UploadHub-0.0.2/UploadHub.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 05:11:06.000000 UploadHub-0.0.2/UploadHub.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       19 2023-07-23 05:11:06.000000 UploadHub-0.0.2/UploadHub.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       10 2023-07-23 05:11:06.000000 UploadHub-0.0.2/UploadHub.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 05:11:06.470849 UploadHub-0.0.2/setup.cfg
+-rw-rw-rw-   0        0        0      811 2023-07-23 05:10:44.000000 UploadHub-0.0.2/setup.py
```

### Comparing `UploadHub-0.0.1/LICENSE` & `UploadHub-0.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `UploadHub-0.0.1/PKG-INFO` & `UploadHub-0.0.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: UploadHub
-Version: 0.0.1
+Version: 0.0.2
 Summary: PYPI and GitHub package uploader.
 Author: Armando Chaparro
 Author-email: <pylejandria@gmail.com>
 Keywords: python
 Classifier: Development Status :: 1 - Planning
 Classifier: Intended Audience :: Developers
 Classifier: Programming Language :: Python :: 3
```

### Comparing `UploadHub-0.0.1/UploadHub/__main__.py` & `UploadHub-0.0.2/UploadHub/__main__.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 import argparse
-from new import NewPackage
-from upload import UploadPackage
+from .new import NewPackage
+from .upload import UploadPackage
 
 # TERMINAL ARGUMENTS
 parser = argparse.ArgumentParser(prog='UploadHub', description='Manages package uploads')
 parser.add_argument('mode')
 args = parser.parse_args()
 mode = args.mode
```

### Comparing `UploadHub-0.0.1/UploadHub/license.py` & `UploadHub-0.0.2/UploadHub/license.py`

 * *Files identical despite different names*

### Comparing `UploadHub-0.0.1/UploadHub/new.py` & `UploadHub-0.0.2/UploadHub/new.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import os
 import subprocess
 import ttkbootstrap as ttk
-from utils import load_config, StatusBar
+from .utils import load_config, StatusBar
 from tkinter.filedialog import askdirectory
 
 
 class NewPackage(ttk.Window):
     def __init__(self, **kwargs):
         super().__init__(**kwargs)
```

### Comparing `UploadHub-0.0.1/UploadHub/setup.py` & `UploadHub-0.0.2/UploadHub/setup.py`

 * *Files identical despite different names*

### Comparing `UploadHub-0.0.1/UploadHub/upload.py` & `UploadHub-0.0.2/UploadHub/upload.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import os
 import subprocess
 import ttkbootstrap as ttk
-from utils import StatusBar
+from .utils import StatusBar
 from tkinter.filedialog import askdirectory
 
 
 class UploadPackage(ttk.Window):
     def __init__(self, **kwargs):
         super().__init__(**kwargs)
```

### Comparing `UploadHub-0.0.1/UploadHub/utils.py` & `UploadHub-0.0.2/UploadHub/utils.py`

 * *Files identical despite different names*

### Comparing `UploadHub-0.0.1/UploadHub.egg-info/PKG-INFO` & `UploadHub-0.0.2/UploadHub.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: UploadHub
-Version: 0.0.1
+Version: 0.0.2
 Summary: PYPI and GitHub package uploader.
 Author: Armando Chaparro
 Author-email: <pylejandria@gmail.com>
 Keywords: python
 Classifier: Development Status :: 1 - Planning
 Classifier: Intended Audience :: Developers
 Classifier: Programming Language :: Python :: 3
```

### Comparing `UploadHub-0.0.1/setup.py` & `UploadHub-0.0.2/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 from setuptools import setup, find_packages
-VERSION = '0.0.1'
+VERSION = '0.0.2'
 DESCRIPTION = 'PYPI and GitHub package uploader.'
 LONG_DESCRIPTION = 'Manages all the commands to upload a package to PYPI and GitHub repo.'
 
 setup(
     name='UploadHub',
     version=VERSION,
     author="Armando Chaparro",
```

