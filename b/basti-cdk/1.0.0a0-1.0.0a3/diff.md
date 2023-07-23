# Comparing `tmp/basti-cdk-1.0.0a0.tar.gz` & `tmp/basti-cdk-1.0.0a3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "basti-cdk-1.0.0a0.tar", last modified: Fri Jul 21 18:39:33 2023, max compression
+gzip compressed data, was "basti-cdk-1.0.0a3.tar", last modified: Sun Jul 23 15:55:34 2023, max compression
```

## Comparing `basti-cdk-1.0.0a0.tar` & `basti-cdk-1.0.0a3.tar`

### file list

```diff
@@ -1,21 +1,21 @@
-drwxr-xr-x   0 bohdanpetryshyn   (501) staff       (20)        0 2023-07-21 18:39:33.562828 basti-cdk-1.0.0a0/
--rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)     1077 2023-07-21 18:39:24.000000 basti-cdk-1.0.0a0/LICENSE
--rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)       23 2023-07-21 18:39:24.000000 basti-cdk-1.0.0a0/MANIFEST.in
--rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)     4573 2023-07-21 18:39:33.562505 basti-cdk-1.0.0a0/PKG-INFO
--rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)     3642 2023-07-21 18:39:24.000000 basti-cdk-1.0.0a0/README.md
--rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)      234 2023-07-21 18:39:24.000000 basti-cdk-1.0.0a0/pyproject.toml
--rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)       38 2023-07-21 18:39:33.562923 basti-cdk-1.0.0a0/setup.cfg
--rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)     1741 2023-07-21 18:39:24.000000 basti-cdk-1.0.0a0/setup.py
-drwxr-xr-x   0 bohdanpetryshyn   (501) staff       (20)        0 2023-07-21 18:39:33.555830 basti-cdk-1.0.0a0/src/
-drwxr-xr-x   0 bohdanpetryshyn   (501) staff       (20)        0 2023-07-21 18:39:33.558996 basti-cdk-1.0.0a0/src/basti_cdk/
--rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)    33686 2023-07-21 18:39:24.000000 basti-cdk-1.0.0a0/src/basti_cdk/__init__.py
-drwxr-xr-x   0 bohdanpetryshyn   (501) staff       (20)        0 2023-07-21 18:39:33.561815 basti-cdk-1.0.0a0/src/basti_cdk/_jsii/
--rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)      401 2023-07-21 18:39:24.000000 basti-cdk-1.0.0a0/src/basti_cdk/_jsii/__init__.py
--rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)   136856 2023-07-21 18:39:24.000000 basti-cdk-1.0.0a0/src/basti_cdk/_jsii/basti-cdk@1.0.0-alpha.0.jsii.tgz
--rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)        1 2023-07-21 18:39:24.000000 basti-cdk-1.0.0a0/src/basti_cdk/py.typed
-drwxr-xr-x   0 bohdanpetryshyn   (501) staff       (20)        0 2023-07-21 18:39:33.561010 basti-cdk-1.0.0a0/src/basti_cdk.egg-info/
--rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)     4573 2023-07-21 18:39:33.000000 basti-cdk-1.0.0a0/src/basti_cdk.egg-info/PKG-INFO
--rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)      371 2023-07-21 18:39:33.000000 basti-cdk-1.0.0a0/src/basti_cdk.egg-info/SOURCES.txt
--rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)        1 2023-07-21 18:39:33.000000 basti-cdk-1.0.0a0/src/basti_cdk.egg-info/dependency_links.txt
--rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)       96 2023-07-21 18:39:33.000000 basti-cdk-1.0.0a0/src/basti_cdk.egg-info/requires.txt
--rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)       10 2023-07-21 18:39:33.000000 basti-cdk-1.0.0a0/src/basti_cdk.egg-info/top_level.txt
+drwxr-xr-x   0 bohdanpetryshyn   (501) staff       (20)        0 2023-07-23 15:55:34.658405 basti-cdk-1.0.0a3/
+-rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)     1073 2023-07-23 15:55:27.000000 basti-cdk-1.0.0a3/LICENSE
+-rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)       23 2023-07-23 15:55:27.000000 basti-cdk-1.0.0a3/MANIFEST.in
+-rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)     4598 2023-07-23 15:55:34.658152 basti-cdk-1.0.0a3/PKG-INFO
+-rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)     3642 2023-07-23 15:55:27.000000 basti-cdk-1.0.0a3/README.md
+-rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)      234 2023-07-23 15:55:27.000000 basti-cdk-1.0.0a3/pyproject.toml
+-rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)       38 2023-07-23 15:55:34.658476 basti-cdk-1.0.0a3/setup.cfg
+-rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)     1783 2023-07-23 15:55:27.000000 basti-cdk-1.0.0a3/setup.py
+drwxr-xr-x   0 bohdanpetryshyn   (501) staff       (20)        0 2023-07-23 15:55:34.652686 basti-cdk-1.0.0a3/src/
+drwxr-xr-x   0 bohdanpetryshyn   (501) staff       (20)        0 2023-07-23 15:55:34.655361 basti-cdk-1.0.0a3/src/basti_cdk/
+-rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)    33686 2023-07-23 15:55:27.000000 basti-cdk-1.0.0a3/src/basti_cdk/__init__.py
+drwxr-xr-x   0 bohdanpetryshyn   (501) staff       (20)        0 2023-07-23 15:55:34.657642 basti-cdk-1.0.0a3/src/basti_cdk/_jsii/
+-rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)      401 2023-07-23 15:55:27.000000 basti-cdk-1.0.0a3/src/basti_cdk/_jsii/__init__.py
+-rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)   141508 2023-07-23 15:55:27.000000 basti-cdk-1.0.0a3/src/basti_cdk/_jsii/basti-cdk@1.0.0-alpha.3.jsii.tgz
+-rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)        1 2023-07-23 15:55:27.000000 basti-cdk-1.0.0a3/src/basti_cdk/py.typed
+drwxr-xr-x   0 bohdanpetryshyn   (501) staff       (20)        0 2023-07-23 15:55:34.656945 basti-cdk-1.0.0a3/src/basti_cdk.egg-info/
+-rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)     4598 2023-07-23 15:55:34.000000 basti-cdk-1.0.0a3/src/basti_cdk.egg-info/PKG-INFO
+-rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)      371 2023-07-23 15:55:34.000000 basti-cdk-1.0.0a3/src/basti_cdk.egg-info/SOURCES.txt
+-rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)        1 2023-07-23 15:55:34.000000 basti-cdk-1.0.0a3/src/basti_cdk.egg-info/dependency_links.txt
+-rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)      111 2023-07-23 15:55:34.000000 basti-cdk-1.0.0a3/src/basti_cdk.egg-info/requires.txt
+-rw-r--r--   0 bohdanpetryshyn   (501) staff       (20)       10 2023-07-23 15:55:34.000000 basti-cdk-1.0.0a3/src/basti_cdk.egg-info/top_level.txt
```

### Comparing `basti-cdk-1.0.0a0/LICENSE` & `basti-cdk-1.0.0a3/LICENSE`

 * *Files 8% similar despite different names*

```diff
@@ -1,9 +1,21 @@
 MIT License
 
-Copyright (c) <year> <copyright holders>
+Copyright (c) 2022 Bohdan Petryshyn
 
-Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
+Permission is hereby granted, free of charge, to any person obtaining a copy
+of this software and associated documentation files (the "Software"), to deal
+in the Software without restriction, including without limitation the rights
+to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
+copies of the Software, and to permit persons to whom the Software is
+furnished to do so, subject to the following conditions:
 
-The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.
+The above copyright notice and this permission notice shall be included in all
+copies or substantial portions of the Software.
 
-THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
+THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
+IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
+FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
+AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
+LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
+OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
+SOFTWARE.
```

### Comparing `basti-cdk-1.0.0a0/PKG-INFO` & `basti-cdk-1.0.0a3/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 Metadata-Version: 2.1
 Name: basti-cdk
-Version: 1.0.0a0
+Version: 1.0.0a3
 Summary: A CDK Construct for Basti
-Home-page: https://github.com/BohdanPetryshyn/basti.git
+Home-page: https://github.com/BohdanPetryshyn/basti/tree/main/packages/basti-cdk
 Author: BohdanPetryshyn<bohdan.y.petryshyn@gmail.com>
 License: MIT
 Project-URL: Source, https://github.com/BohdanPetryshyn/basti.git
 Classifier: Intended Audience :: Developers
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: JavaScript
 Classifier: Programming Language :: Python :: 3 :: Only
```

### Comparing `basti-cdk-1.0.0a0/README.md` & `basti-cdk-1.0.0a3/README.md`

 * *Files identical despite different names*

### Comparing `basti-cdk-1.0.0a0/setup.py` & `basti-cdk-1.0.0a3/setup.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,18 +1,18 @@
 import json
 import setuptools
 
 kwargs = json.loads(
     """
 {
     "name": "basti-cdk",
-    "version": "1.0.0.a0",
+    "version": "1.0.0.a3",
     "description": "A CDK Construct for Basti",
     "license": "MIT",
-    "url": "https://github.com/BohdanPetryshyn/basti.git",
+    "url": "https://github.com/BohdanPetryshyn/basti/tree/main/packages/basti-cdk",
     "long_description_content_type": "text/markdown",
     "author": "BohdanPetryshyn<bohdan.y.petryshyn@gmail.com>",
     "bdist_wheel": {
         "universal": true
     },
     "project_urls": {
         "Source": "https://github.com/BohdanPetryshyn/basti.git"
@@ -22,24 +22,24 @@
     },
     "packages": [
         "basti_cdk",
         "basti_cdk._jsii"
     ],
     "package_data": {
         "basti_cdk._jsii": [
-            "basti-cdk@1.0.0-alpha.0.jsii.tgz"
+            "basti-cdk@1.0.0-alpha.3.jsii.tgz"
         ],
         "basti_cdk": [
             "py.typed"
         ]
     },
     "python_requires": "~=3.7",
     "install_requires": [
-        "aws-cdk-lib==2.86.0",
-        "constructs==10.0.5",
+        "aws-cdk-lib>=2.86.0, <3.0.0",
+        "constructs>=10.0.5, <11.0.0",
         "jsii>=1.85.0, <2.0.0",
         "publication>=0.0.3",
         "typeguard~=2.13.3"
     ],
     "classifiers": [
         "Intended Audience :: Developers",
         "Operating System :: OS Independent",
```

### Comparing `basti-cdk-1.0.0a0/src/basti_cdk/__init__.py` & `basti-cdk-1.0.0a3/src/basti_cdk/__init__.py`

 * *Files identical despite different names*

### Comparing `basti-cdk-1.0.0a0/src/basti_cdk.egg-info/PKG-INFO` & `basti-cdk-1.0.0a3/src/basti_cdk.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 Metadata-Version: 2.1
 Name: basti-cdk
-Version: 1.0.0a0
+Version: 1.0.0a3
 Summary: A CDK Construct for Basti
-Home-page: https://github.com/BohdanPetryshyn/basti.git
+Home-page: https://github.com/BohdanPetryshyn/basti/tree/main/packages/basti-cdk
 Author: BohdanPetryshyn<bohdan.y.petryshyn@gmail.com>
 License: MIT
 Project-URL: Source, https://github.com/BohdanPetryshyn/basti.git
 Classifier: Intended Audience :: Developers
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: JavaScript
 Classifier: Programming Language :: Python :: 3 :: Only
```

