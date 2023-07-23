# Comparing `tmp/gammarer.aws-secure-bucket-0.9.5.tar.gz` & `tmp/gammarer.aws-secure-bucket-0.9.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "gammarer.aws-secure-bucket-0.9.5.tar", last modified: Sat Jul 22 17:23:02 2023, max compression
+gzip compressed data, was "gammarer.aws-secure-bucket-0.9.6.tar", last modified: Sun Jul 23 17:22:21 2023, max compression
```

## Comparing `gammarer.aws-secure-bucket-0.9.5.tar` & `gammarer.aws-secure-bucket-0.9.6.tar`

### file list

```diff
@@ -1,22 +1,22 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 17:23:02.484448 gammarer.aws-secure-bucket-0.9.5/
--rw-r--r--   0 runner    (1001) docker     (123)    11358 2023-07-22 17:22:47.000000 gammarer.aws-secure-bucket-0.9.5/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       23 2023-07-22 17:22:47.000000 gammarer.aws-secure-bucket-0.9.5/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     1597 2023-07-22 17:23:02.484448 gammarer.aws-secure-bucket-0.9.5/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      643 2023-07-22 17:22:47.000000 gammarer.aws-secure-bucket-0.9.5/README.md
--rw-r--r--   0 runner    (1001) docker     (123)      234 2023-07-22 17:22:47.000000 gammarer.aws-secure-bucket-0.9.5/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-22 17:23:02.488448 gammarer.aws-secure-bucket-0.9.5/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1848 2023-07-22 17:22:47.000000 gammarer.aws-secure-bucket-0.9.5/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 17:23:02.484448 gammarer.aws-secure-bucket-0.9.5/src/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 17:23:02.484448 gammarer.aws-secure-bucket-0.9.5/src/gammarer/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 17:23:02.484448 gammarer.aws-secure-bucket-0.9.5/src/gammarer/aws_secure_bucket/
--rw-r--r--   0 runner    (1001) docker     (123)     7909 2023-07-22 17:22:47.000000 gammarer.aws-secure-bucket-0.9.5/src/gammarer/aws_secure_bucket/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 17:23:02.484448 gammarer.aws-secure-bucket-0.9.5/src/gammarer/aws_secure_bucket/_jsii/
--rw-r--r--   0 runner    (1001) docker     (123)      424 2023-07-22 17:22:47.000000 gammarer.aws-secure-bucket-0.9.5/src/gammarer/aws_secure_bucket/_jsii/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    30735 2023-07-22 17:22:47.000000 gammarer.aws-secure-bucket-0.9.5/src/gammarer/aws_secure_bucket/_jsii/aws-secure-bucket@0.9.5.jsii.tgz
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-22 17:22:47.000000 gammarer.aws-secure-bucket-0.9.5/src/gammarer/aws_secure_bucket/py.typed
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 17:23:02.484448 gammarer.aws-secure-bucket-0.9.5/src/gammarer.aws_secure_bucket.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1597 2023-07-22 17:23:02.000000 gammarer.aws-secure-bucket-0.9.5/src/gammarer.aws_secure_bucket.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      524 2023-07-22 17:23:02.000000 gammarer.aws-secure-bucket-0.9.5/src/gammarer.aws_secure_bucket.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-22 17:23:02.000000 gammarer.aws-secure-bucket-0.9.5/src/gammarer.aws_secure_bucket.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      111 2023-07-22 17:23:02.000000 gammarer.aws-secure-bucket-0.9.5/src/gammarer.aws_secure_bucket.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-22 17:23:02.000000 gammarer.aws-secure-bucket-0.9.5/src/gammarer.aws_secure_bucket.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:22:21.868121 gammarer.aws-secure-bucket-0.9.6/
+-rw-r--r--   0 runner    (1001) docker     (123)    11358 2023-07-23 17:22:08.000000 gammarer.aws-secure-bucket-0.9.6/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       23 2023-07-23 17:22:08.000000 gammarer.aws-secure-bucket-0.9.6/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     1597 2023-07-23 17:22:21.868121 gammarer.aws-secure-bucket-0.9.6/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      643 2023-07-23 17:22:08.000000 gammarer.aws-secure-bucket-0.9.6/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      234 2023-07-23 17:22:08.000000 gammarer.aws-secure-bucket-0.9.6/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 17:22:21.868121 gammarer.aws-secure-bucket-0.9.6/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1848 2023-07-23 17:22:08.000000 gammarer.aws-secure-bucket-0.9.6/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:22:21.864121 gammarer.aws-secure-bucket-0.9.6/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:22:21.864121 gammarer.aws-secure-bucket-0.9.6/src/gammarer/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:22:21.868121 gammarer.aws-secure-bucket-0.9.6/src/gammarer/aws_secure_bucket/
+-rw-r--r--   0 runner    (1001) docker     (123)     7909 2023-07-23 17:22:08.000000 gammarer.aws-secure-bucket-0.9.6/src/gammarer/aws_secure_bucket/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:22:21.868121 gammarer.aws-secure-bucket-0.9.6/src/gammarer/aws_secure_bucket/_jsii/
+-rw-r--r--   0 runner    (1001) docker     (123)      424 2023-07-23 17:22:08.000000 gammarer.aws-secure-bucket-0.9.6/src/gammarer/aws_secure_bucket/_jsii/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    30735 2023-07-23 17:22:08.000000 gammarer.aws-secure-bucket-0.9.6/src/gammarer/aws_secure_bucket/_jsii/aws-secure-bucket@0.9.6.jsii.tgz
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 17:22:08.000000 gammarer.aws-secure-bucket-0.9.6/src/gammarer/aws_secure_bucket/py.typed
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:22:21.868121 gammarer.aws-secure-bucket-0.9.6/src/gammarer.aws_secure_bucket.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1597 2023-07-23 17:22:21.000000 gammarer.aws-secure-bucket-0.9.6/src/gammarer.aws_secure_bucket.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      524 2023-07-23 17:22:21.000000 gammarer.aws-secure-bucket-0.9.6/src/gammarer.aws_secure_bucket.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 17:22:21.000000 gammarer.aws-secure-bucket-0.9.6/src/gammarer.aws_secure_bucket.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      111 2023-07-23 17:22:21.000000 gammarer.aws-secure-bucket-0.9.6/src/gammarer.aws_secure_bucket.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-23 17:22:21.000000 gammarer.aws-secure-bucket-0.9.6/src/gammarer.aws_secure_bucket.egg-info/top_level.txt
```

### Comparing `gammarer.aws-secure-bucket-0.9.5/LICENSE` & `gammarer.aws-secure-bucket-0.9.6/LICENSE`

 * *Files identical despite different names*

### Comparing `gammarer.aws-secure-bucket-0.9.5/PKG-INFO` & `gammarer.aws-secure-bucket-0.9.6/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: gammarer.aws-secure-bucket
-Version: 0.9.5
+Version: 0.9.6
 Summary: This is a Simple S3 Secure Bucket.
 Home-page: https://github.com/yicr/aws-secure-bucket.git
 Author: yicr<yicr@users.noreply.github.com>
 License: Apache-2.0
 Project-URL: Source, https://github.com/yicr/aws-secure-bucket.git
 Classifier: Intended Audience :: Developers
 Classifier: Operating System :: OS Independent
```

### Comparing `gammarer.aws-secure-bucket-0.9.5/README.md` & `gammarer.aws-secure-bucket-0.9.6/README.md`

 * *Files identical despite different names*

### Comparing `gammarer.aws-secure-bucket-0.9.5/setup.py` & `gammarer.aws-secure-bucket-0.9.6/setup.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import json
 import setuptools
 
 kwargs = json.loads(
     """
 {
     "name": "gammarer.aws-secure-bucket",
-    "version": "0.9.5",
+    "version": "0.9.6",
     "description": "This is a Simple S3 Secure Bucket.",
     "license": "Apache-2.0",
     "url": "https://github.com/yicr/aws-secure-bucket.git",
     "long_description_content_type": "text/markdown",
     "author": "yicr<yicr@users.noreply.github.com>",
     "bdist_wheel": {
         "universal": true
@@ -22,15 +22,15 @@
     },
     "packages": [
         "gammarer.aws_secure_bucket",
         "gammarer.aws_secure_bucket._jsii"
     ],
     "package_data": {
         "gammarer.aws_secure_bucket._jsii": [
-            "aws-secure-bucket@0.9.5.jsii.tgz"
+            "aws-secure-bucket@0.9.6.jsii.tgz"
         ],
         "gammarer.aws_secure_bucket": [
             "py.typed"
         ]
     },
     "python_requires": "~=3.7",
     "install_requires": [
```

### Comparing `gammarer.aws-secure-bucket-0.9.5/src/gammarer/aws_secure_bucket/__init__.py` & `gammarer.aws-secure-bucket-0.9.6/src/gammarer/aws_secure_bucket/__init__.py`

 * *Files identical despite different names*

### Comparing `gammarer.aws-secure-bucket-0.9.5/src/gammarer.aws_secure_bucket.egg-info/PKG-INFO` & `gammarer.aws-secure-bucket-0.9.6/src/gammarer.aws_secure_bucket.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: gammarer.aws-secure-bucket
-Version: 0.9.5
+Version: 0.9.6
 Summary: This is a Simple S3 Secure Bucket.
 Home-page: https://github.com/yicr/aws-secure-bucket.git
 Author: yicr<yicr@users.noreply.github.com>
 License: Apache-2.0
 Project-URL: Source, https://github.com/yicr/aws-secure-bucket.git
 Classifier: Intended Audience :: Developers
 Classifier: Operating System :: OS Independent
```

### Comparing `gammarer.aws-secure-bucket-0.9.5/src/gammarer.aws_secure_bucket.egg-info/SOURCES.txt` & `gammarer.aws-secure-bucket-0.9.6/src/gammarer.aws_secure_bucket.egg-info/SOURCES.txt`

 * *Files 2% similar despite different names*

```diff
@@ -7,8 +7,8 @@
 src/gammarer.aws_secure_bucket.egg-info/SOURCES.txt
 src/gammarer.aws_secure_bucket.egg-info/dependency_links.txt
 src/gammarer.aws_secure_bucket.egg-info/requires.txt
 src/gammarer.aws_secure_bucket.egg-info/top_level.txt
 src/gammarer/aws_secure_bucket/__init__.py
 src/gammarer/aws_secure_bucket/py.typed
 src/gammarer/aws_secure_bucket/_jsii/__init__.py
-src/gammarer/aws_secure_bucket/_jsii/aws-secure-bucket@0.9.5.jsii.tgz
+src/gammarer/aws_secure_bucket/_jsii/aws-secure-bucket@0.9.6.jsii.tgz
```

