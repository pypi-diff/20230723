# Comparing `tmp/cdk8s-plus-24-2.8.99.tar.gz` & `tmp/cdk8s-plus-24-2.9.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "cdk8s-plus-24-2.8.99.tar", last modified: Wed Jul 19 03:09:50 2023, max compression
+gzip compressed data, was "cdk8s-plus-24-2.9.0.tar", last modified: Sat Jul 22 00:18:14 2023, max compression
```

## Comparing `cdk8s-plus-24-2.8.99.tar` & `cdk8s-plus-24-2.9.0.tar`

### file list

```diff
@@ -1,24 +1,24 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-19 03:09:50.968593 cdk8s-plus-24-2.8.99/
--rw-r--r--   0 runner    (1001) docker     (123)    11358 2023-07-19 03:09:38.000000 cdk8s-plus-24-2.8.99/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       23 2023-07-19 03:09:38.000000 cdk8s-plus-24-2.8.99/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)       67 2023-07-19 03:09:38.000000 cdk8s-plus-24-2.8.99/NOTICE
--rw-r--r--   0 runner    (1001) docker     (123)     3241 2023-07-19 03:09:50.968593 cdk8s-plus-24-2.8.99/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2142 2023-07-19 03:09:38.000000 cdk8s-plus-24-2.8.99/README.md
--rw-r--r--   0 runner    (1001) docker     (123)      234 2023-07-19 03:09:38.000000 cdk8s-plus-24-2.8.99/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-19 03:09:50.968593 cdk8s-plus-24-2.8.99/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1942 2023-07-19 03:09:38.000000 cdk8s-plus-24-2.8.99/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-19 03:09:50.960593 cdk8s-plus-24-2.8.99/src/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-19 03:09:50.964593 cdk8s-plus-24-2.8.99/src/cdk8s_plus_24/
--rw-r--r--   0 runner    (1001) docker     (123)  1161790 2023-07-19 03:09:38.000000 cdk8s-plus-24-2.8.99/src/cdk8s_plus_24/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-19 03:09:50.964593 cdk8s-plus-24-2.8.99/src/cdk8s_plus_24/_jsii/
--rw-r--r--   0 runner    (1001) docker     (123)      393 2023-07-19 03:09:38.000000 cdk8s-plus-24-2.8.99/src/cdk8s_plus_24/_jsii/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)  1279961 2023-07-19 03:09:38.000000 cdk8s-plus-24-2.8.99/src/cdk8s_plus_24/_jsii/cdk8s-plus-24@2.8.99.jsii.tgz
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-19 03:09:50.964593 cdk8s-plus-24-2.8.99/src/cdk8s_plus_24/k8s/
--rw-r--r--   0 runner    (1001) docker     (123)  2878966 2023-07-19 03:09:38.000000 cdk8s-plus-24-2.8.99/src/cdk8s_plus_24/k8s/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-19 03:09:38.000000 cdk8s-plus-24-2.8.99/src/cdk8s_plus_24/py.typed
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-19 03:09:50.964593 cdk8s-plus-24-2.8.99/src/cdk8s_plus_24.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     3241 2023-07-19 03:09:50.000000 cdk8s-plus-24-2.8.99/src/cdk8s_plus_24.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      445 2023-07-19 03:09:50.000000 cdk8s-plus-24-2.8.99/src/cdk8s_plus_24.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-19 03:09:50.000000 cdk8s-plus-24-2.8.99/src/cdk8s_plus_24.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      107 2023-07-19 03:09:50.000000 cdk8s-plus-24-2.8.99/src/cdk8s_plus_24.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       14 2023-07-19 03:09:50.000000 cdk8s-plus-24-2.8.99/src/cdk8s_plus_24.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 00:18:14.349669 cdk8s-plus-24-2.9.0/
+-rw-r--r--   0 runner    (1001) docker     (123)    11358 2023-07-22 00:18:00.000000 cdk8s-plus-24-2.9.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       23 2023-07-22 00:18:00.000000 cdk8s-plus-24-2.9.0/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)       67 2023-07-22 00:18:00.000000 cdk8s-plus-24-2.9.0/NOTICE
+-rw-r--r--   0 runner    (1001) docker     (123)     3240 2023-07-22 00:18:14.349669 cdk8s-plus-24-2.9.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2142 2023-07-22 00:18:00.000000 cdk8s-plus-24-2.9.0/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      234 2023-07-22 00:18:00.000000 cdk8s-plus-24-2.9.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-22 00:18:14.349669 cdk8s-plus-24-2.9.0/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1938 2023-07-22 00:18:00.000000 cdk8s-plus-24-2.9.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 00:18:14.341669 cdk8s-plus-24-2.9.0/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 00:18:14.345669 cdk8s-plus-24-2.9.0/src/cdk8s_plus_24/
+-rw-r--r--   0 runner    (1001) docker     (123)  1161790 2023-07-22 00:18:00.000000 cdk8s-plus-24-2.9.0/src/cdk8s_plus_24/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 00:18:14.345669 cdk8s-plus-24-2.9.0/src/cdk8s_plus_24/_jsii/
+-rw-r--r--   0 runner    (1001) docker     (123)      391 2023-07-22 00:18:00.000000 cdk8s-plus-24-2.9.0/src/cdk8s_plus_24/_jsii/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)  1279996 2023-07-22 00:18:00.000000 cdk8s-plus-24-2.9.0/src/cdk8s_plus_24/_jsii/cdk8s-plus-24@2.9.0.jsii.tgz
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 00:18:14.345669 cdk8s-plus-24-2.9.0/src/cdk8s_plus_24/k8s/
+-rw-r--r--   0 runner    (1001) docker     (123)  2878966 2023-07-22 00:18:00.000000 cdk8s-plus-24-2.9.0/src/cdk8s_plus_24/k8s/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-22 00:18:00.000000 cdk8s-plus-24-2.9.0/src/cdk8s_plus_24/py.typed
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 00:18:14.345669 cdk8s-plus-24-2.9.0/src/cdk8s_plus_24.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     3240 2023-07-22 00:18:14.000000 cdk8s-plus-24-2.9.0/src/cdk8s_plus_24.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      444 2023-07-22 00:18:14.000000 cdk8s-plus-24-2.9.0/src/cdk8s_plus_24.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-22 00:18:14.000000 cdk8s-plus-24-2.9.0/src/cdk8s_plus_24.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      105 2023-07-22 00:18:14.000000 cdk8s-plus-24-2.9.0/src/cdk8s_plus_24.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       14 2023-07-22 00:18:14.000000 cdk8s-plus-24-2.9.0/src/cdk8s_plus_24.egg-info/top_level.txt
```

### Comparing `cdk8s-plus-24-2.8.99/LICENSE` & `cdk8s-plus-24-2.9.0/LICENSE`

 * *Files identical despite different names*

### Comparing `cdk8s-plus-24-2.8.99/PKG-INFO` & `cdk8s-plus-24-2.9.0/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cdk8s-plus-24
-Version: 2.8.99
+Version: 2.9.0
 Summary: cdk8s+ is a software development framework that provides high level abstractions for authoring Kubernetes applications. cdk8s-plus-24 synthesizes Kubernetes manifests for Kubernetes 1.24.0
 Home-page: https://github.com/cdk8s-team/cdk8s-plus.git
 Author: Amazon Web Services
 License: Apache-2.0
 Project-URL: Source, https://github.com/cdk8s-team/cdk8s-plus.git
 Classifier: Intended Audience :: Developers
 Classifier: Operating System :: OS Independent
```

### Comparing `cdk8s-plus-24-2.8.99/README.md` & `cdk8s-plus-24-2.9.0/README.md`

 * *Files identical despite different names*

### Comparing `cdk8s-plus-24-2.8.99/setup.py` & `cdk8s-plus-24-2.9.0/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import json
 import setuptools
 
 kwargs = json.loads(
     """
 {
     "name": "cdk8s-plus-24",
-    "version": "2.8.99",
+    "version": "2.9.0",
     "description": "cdk8s+ is a software development framework that provides high level abstractions for authoring Kubernetes applications. cdk8s-plus-24 synthesizes Kubernetes manifests for Kubernetes 1.24.0",
     "license": "Apache-2.0",
     "url": "https://github.com/cdk8s-team/cdk8s-plus.git",
     "long_description_content_type": "text/markdown",
     "author": "Amazon Web Services",
     "bdist_wheel": {
         "universal": true
@@ -23,23 +23,23 @@
     "packages": [
         "cdk8s_plus_24",
         "cdk8s_plus_24._jsii",
         "cdk8s_plus_24.k8s"
     ],
     "package_data": {
         "cdk8s_plus_24._jsii": [
-            "cdk8s-plus-24@2.8.99.jsii.tgz"
+            "cdk8s-plus-24@2.9.0.jsii.tgz"
         ],
         "cdk8s_plus_24": [
             "py.typed"
         ]
     },
     "python_requires": "~=3.7",
     "install_requires": [
-        "cdk8s>=2.7.115, <3.0.0",
+        "cdk8s>=2.8.0, <3.0.0",
         "constructs>=10.2.69, <11.0.0",
         "jsii>=1.85.0, <2.0.0",
         "publication>=0.0.3",
         "typeguard~=2.13.3"
     ],
     "classifiers": [
         "Intended Audience :: Developers",
```

### Comparing `cdk8s-plus-24-2.8.99/src/cdk8s_plus_24/__init__.py` & `cdk8s-plus-24-2.9.0/src/cdk8s_plus_24/__init__.py`

 * *Files identical despite different names*

### Comparing `cdk8s-plus-24-2.8.99/src/cdk8s_plus_24/k8s/__init__.py` & `cdk8s-plus-24-2.9.0/src/cdk8s_plus_24/k8s/__init__.py`

 * *Files identical despite different names*

### Comparing `cdk8s-plus-24-2.8.99/src/cdk8s_plus_24.egg-info/PKG-INFO` & `cdk8s-plus-24-2.9.0/src/cdk8s_plus_24.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: cdk8s-plus-24
-Version: 2.8.99
+Version: 2.9.0
 Summary: cdk8s+ is a software development framework that provides high level abstractions for authoring Kubernetes applications. cdk8s-plus-24 synthesizes Kubernetes manifests for Kubernetes 1.24.0
 Home-page: https://github.com/cdk8s-team/cdk8s-plus.git
 Author: Amazon Web Services
 License: Apache-2.0
 Project-URL: Source, https://github.com/cdk8s-team/cdk8s-plus.git
 Classifier: Intended Audience :: Developers
 Classifier: Operating System :: OS Independent
```

