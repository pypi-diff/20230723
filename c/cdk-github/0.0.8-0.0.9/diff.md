# Comparing `tmp/cdk-github-0.0.8.tar.gz` & `tmp/cdk-github-0.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "cdk-github-0.0.8.tar", last modified: Tue Jun 14 11:53:46 2022, max compression
+gzip compressed data, was "cdk-github-0.0.9.tar", last modified: Tue Jun 14 12:03:56 2022, max compression
```

## Comparing `cdk-github-0.0.8.tar` & `cdk-github-0.0.9.tar`

### file list

```diff
@@ -1,21 +1,21 @@
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-06-14 11:53:46.358947 cdk-github-0.0.8/
--rw-r--r--   0 runner    (1001) docker     (121)     1060 2022-06-14 11:53:34.000000 cdk-github-0.0.8/LICENSE
--rw-r--r--   0 runner    (1001) docker     (121)       23 2022-06-14 11:53:34.000000 cdk-github-0.0.8/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (121)     5121 2022-06-14 11:53:46.358947 cdk-github-0.0.8/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     4257 2022-06-14 11:53:34.000000 cdk-github-0.0.8/README.md
--rw-r--r--   0 runner    (1001) docker     (121)      106 2022-06-14 11:53:34.000000 cdk-github-0.0.8/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (121)       38 2022-06-14 11:53:46.358947 cdk-github-0.0.8/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (121)     1635 2022-06-14 11:53:34.000000 cdk-github-0.0.8/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-06-14 11:53:46.354947 cdk-github-0.0.8/src/
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-06-14 11:53:46.358947 cdk-github-0.0.8/src/cdk_github.egg-info/
--rw-r--r--   0 runner    (1001) docker     (121)     5121 2022-06-14 11:53:45.000000 cdk-github-0.0.8/src/cdk_github.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)      369 2022-06-14 11:53:46.000000 cdk-github-0.0.8/src/cdk_github.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2022-06-14 11:53:45.000000 cdk-github-0.0.8/src/cdk_github.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (121)       93 2022-06-14 11:53:46.000000 cdk-github-0.0.8/src/cdk_github.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (121)       10 2022-06-14 11:53:46.000000 cdk-github-0.0.8/src/cdk_github.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-06-14 11:53:46.358947 cdk-github-0.0.8/src/cdkgithub/
--rw-r--r--   0 runner    (1001) docker     (121)    16510 2022-06-14 11:53:34.000000 cdk-github-0.0.8/src/cdkgithub/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-06-14 11:53:46.358947 cdk-github-0.0.8/src/cdkgithub/_jsii/
--rw-r--r--   0 runner    (1001) docker     (121)      353 2022-06-14 11:53:34.000000 cdk-github-0.0.8/src/cdkgithub/_jsii/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)  2596561 2022-06-14 11:53:34.000000 cdk-github-0.0.8/src/cdkgithub/_jsii/cdk-github@0.0.8.jsii.tgz
--rw-r--r--   0 runner    (1001) docker     (121)        1 2022-06-14 11:53:34.000000 cdk-github-0.0.8/src/cdkgithub/py.typed
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-06-14 12:03:56.813583 cdk-github-0.0.9/
+-rw-r--r--   0 runner    (1001) docker     (121)     1060 2022-06-14 12:03:44.000000 cdk-github-0.0.9/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (121)       23 2022-06-14 12:03:44.000000 cdk-github-0.0.9/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (121)     5121 2022-06-14 12:03:56.813583 cdk-github-0.0.9/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (121)     4257 2022-06-14 12:03:44.000000 cdk-github-0.0.9/README.md
+-rw-r--r--   0 runner    (1001) docker     (121)      106 2022-06-14 12:03:44.000000 cdk-github-0.0.9/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (121)       38 2022-06-14 12:03:56.813583 cdk-github-0.0.9/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (121)     1635 2022-06-14 12:03:44.000000 cdk-github-0.0.9/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-06-14 12:03:56.809583 cdk-github-0.0.9/src/
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-06-14 12:03:56.809583 cdk-github-0.0.9/src/cdk_github.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (121)     5121 2022-06-14 12:03:56.000000 cdk-github-0.0.9/src/cdk_github.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (121)      369 2022-06-14 12:03:56.000000 cdk-github-0.0.9/src/cdk_github.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (121)        1 2022-06-14 12:03:56.000000 cdk-github-0.0.9/src/cdk_github.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (121)       93 2022-06-14 12:03:56.000000 cdk-github-0.0.9/src/cdk_github.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (121)       10 2022-06-14 12:03:56.000000 cdk-github-0.0.9/src/cdk_github.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-06-14 12:03:56.809583 cdk-github-0.0.9/src/cdkgithub/
+-rw-r--r--   0 runner    (1001) docker     (121)    16510 2022-06-14 12:03:44.000000 cdk-github-0.0.9/src/cdkgithub/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-06-14 12:03:56.813583 cdk-github-0.0.9/src/cdkgithub/_jsii/
+-rw-r--r--   0 runner    (1001) docker     (121)      353 2022-06-14 12:03:44.000000 cdk-github-0.0.9/src/cdkgithub/_jsii/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)  2596565 2022-06-14 12:03:44.000000 cdk-github-0.0.9/src/cdkgithub/_jsii/cdk-github@0.0.9.jsii.tgz
+-rw-r--r--   0 runner    (1001) docker     (121)        1 2022-06-14 12:03:44.000000 cdk-github-0.0.9/src/cdkgithub/py.typed
```

### Comparing `cdk-github-0.0.8/LICENSE` & `cdk-github-0.0.9/LICENSE`

 * *Files identical despite different names*

### Comparing `cdk-github-0.0.8/PKG-INFO` & `cdk-github-0.0.9/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cdk-github
-Version: 0.0.8
+Version: 0.0.9
 Summary: AWS CDK Construct Library to interact with GitHub's API.
 Home-page: https://github.com/WtfJoke/cdk-github
 Author: Manuel
 License: MIT
 Project-URL: Source, https://github.com/WtfJoke/cdk-github
 Platform: UNKNOWN
 Classifier: Intended Audience :: Developers
```

### Comparing `cdk-github-0.0.8/README.md` & `cdk-github-0.0.9/README.md`

 * *Files identical despite different names*

### Comparing `cdk-github-0.0.8/setup.py` & `cdk-github-0.0.9/setup.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import json
 import setuptools
 
 kwargs = json.loads(
     """
 {
     "name": "cdk-github",
-    "version": "0.0.8",
+    "version": "0.0.9",
     "description": "AWS CDK Construct Library to interact with GitHub's API.",
     "license": "MIT",
     "url": "https://github.com/WtfJoke/cdk-github",
     "long_description_content_type": "text/markdown",
     "author": "Manuel",
     "bdist_wheel": {
         "universal": true
@@ -22,15 +22,15 @@
     },
     "packages": [
         "cdkgithub",
         "cdkgithub._jsii"
     ],
     "package_data": {
         "cdkgithub._jsii": [
-            "cdk-github@0.0.8.jsii.tgz"
+            "cdk-github@0.0.9.jsii.tgz"
         ],
         "cdkgithub": [
             "py.typed"
         ]
     },
     "python_requires": "~=3.7",
     "install_requires": [
```

### Comparing `cdk-github-0.0.8/src/cdk_github.egg-info/PKG-INFO` & `cdk-github-0.0.9/src/cdk_github.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cdk-github
-Version: 0.0.8
+Version: 0.0.9
 Summary: AWS CDK Construct Library to interact with GitHub's API.
 Home-page: https://github.com/WtfJoke/cdk-github
 Author: Manuel
 License: MIT
 Project-URL: Source, https://github.com/WtfJoke/cdk-github
 Platform: UNKNOWN
 Classifier: Intended Audience :: Developers
```

### Comparing `cdk-github-0.0.8/src/cdkgithub/__init__.py` & `cdk-github-0.0.9/src/cdkgithub/__init__.py`

 * *Files identical despite different names*

