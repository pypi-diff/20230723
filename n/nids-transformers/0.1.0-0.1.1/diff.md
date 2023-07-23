# Comparing `tmp/nids_transformers-0.1.0.tar.gz` & `tmp/nids_transformers-0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nids_transformers-0.1.0.tar", last modified: Wed Jul 19 06:17:21 2023, max compression
+gzip compressed data, was "nids_transformers-0.1.1.tar", last modified: Sat Jul 22 14:59:08 2023, max compression
```

## Comparing `nids_transformers-0.1.0.tar` & `nids_transformers-0.1.1.tar`

### file list

```diff
@@ -1,19 +1,19 @@
-drwxr-xr-x   0 rdp        (501) staff       (20)        0 2023-07-19 06:17:21.665976 nids_transformers-0.1.0/
--rw-r--r--   0 rdp        (501) staff       (20)      178 2023-07-19 01:47:15.000000 nids_transformers-0.1.0/MANIFEST.in
--rw-r--r--   0 rdp        (501) staff       (20)      515 2023-07-19 06:17:21.665758 nids_transformers-0.1.0/PKG-INFO
--rw-r--r--   0 rdp        (501) staff       (20)        0 2023-07-19 01:11:31.000000 nids_transformers-0.1.0/README.md
-drwxr-xr-x   0 rdp        (501) staff       (20)        0 2023-07-19 06:17:21.664171 nids_transformers-0.1.0/nids_transformers/
--rw-r--r--   0 rdp        (501) staff       (20)  5495089 2023-07-06 03:59:04.000000 nids_transformers-0.1.0/nids_transformers/CORPUS.txt
--rw-r--r--   0 rdp        (501) staff       (20)  1585280 2023-07-19 01:16:55.000000 nids_transformers-0.1.0/nids_transformers/KMEANS-CLUSTER-CENTERS.npy
--rw-r--r--   0 rdp        (501) staff       (20)    10066 2023-07-19 06:17:00.000000 nids_transformers-0.1.0/nids_transformers/NIDSTransformers.py
--rw-r--r--   0 rdp        (501) staff       (20)    23489 2023-07-19 01:14:48.000000 nids_transformers-0.1.0/nids_transformers/SCALER.pkl
--rw-r--r--   0 rdp        (501) staff       (20)  3170432 2023-07-19 01:17:11.000000 nids_transformers-0.1.0/nids_transformers/TAGS-NAMES-EMBEDDINGS.npy
--rw-r--r--   0 rdp        (501) staff       (20)       35 2023-07-19 00:52:36.000000 nids_transformers-0.1.0/nids_transformers/__init__.py
-drwxr-xr-x   0 rdp        (501) staff       (20)        0 2023-07-19 06:17:21.665445 nids_transformers-0.1.0/nids_transformers.egg-info/
--rw-r--r--   0 rdp        (501) staff       (20)      515 2023-07-19 06:17:21.000000 nids_transformers-0.1.0/nids_transformers.egg-info/PKG-INFO
--rw-r--r--   0 rdp        (501) staff       (20)      449 2023-07-19 06:17:21.000000 nids_transformers-0.1.0/nids_transformers.egg-info/SOURCES.txt
--rw-r--r--   0 rdp        (501) staff       (20)        1 2023-07-19 06:17:21.000000 nids_transformers-0.1.0/nids_transformers.egg-info/dependency_links.txt
--rw-r--r--   0 rdp        (501) staff       (20)      212 2023-07-19 06:17:21.000000 nids_transformers-0.1.0/nids_transformers.egg-info/requires.txt
--rw-r--r--   0 rdp        (501) staff       (20)       18 2023-07-19 06:17:21.000000 nids_transformers-0.1.0/nids_transformers.egg-info/top_level.txt
--rw-r--r--   0 rdp        (501) staff       (20)       38 2023-07-19 06:17:21.666030 nids_transformers-0.1.0/setup.cfg
--rw-r--r--   0 rdp        (501) staff       (20)      924 2023-07-19 06:16:51.000000 nids_transformers-0.1.0/setup.py
+drwxr-xr-x   0 rdp        (501) staff       (20)        0 2023-07-22 14:59:08.192129 nids_transformers-0.1.1/
+-rw-r--r--   0 rdp        (501) staff       (20)      178 2023-07-19 01:47:15.000000 nids_transformers-0.1.1/MANIFEST.in
+-rw-r--r--   0 rdp        (501) staff       (20)     9212 2023-07-22 14:59:08.191792 nids_transformers-0.1.1/PKG-INFO
+-rw-r--r--   0 rdp        (501) staff       (20)     8658 2023-07-22 14:57:22.000000 nids_transformers-0.1.1/README.md
+drwxr-xr-x   0 rdp        (501) staff       (20)        0 2023-07-22 14:59:08.190281 nids_transformers-0.1.1/nids_transformers/
+-rw-r--r--   0 rdp        (501) staff       (20)  5495089 2023-07-06 03:59:04.000000 nids_transformers-0.1.1/nids_transformers/CORPUS.txt
+-rw-r--r--   0 rdp        (501) staff       (20)  1585280 2023-07-19 01:16:55.000000 nids_transformers-0.1.1/nids_transformers/KMEANS-CLUSTER-CENTERS.npy
+-rw-r--r--   0 rdp        (501) staff       (20)    10066 2023-07-19 06:17:00.000000 nids_transformers-0.1.1/nids_transformers/NIDSTransformers.py
+-rw-r--r--   0 rdp        (501) staff       (20)    23489 2023-07-19 01:14:48.000000 nids_transformers-0.1.1/nids_transformers/SCALER.pkl
+-rw-r--r--   0 rdp        (501) staff       (20)  3170432 2023-07-19 01:17:11.000000 nids_transformers-0.1.1/nids_transformers/TAGS-NAMES-EMBEDDINGS.npy
+-rw-r--r--   0 rdp        (501) staff       (20)       35 2023-07-19 00:52:36.000000 nids_transformers-0.1.1/nids_transformers/__init__.py
+drwxr-xr-x   0 rdp        (501) staff       (20)        0 2023-07-22 14:59:08.191506 nids_transformers-0.1.1/nids_transformers.egg-info/
+-rw-r--r--   0 rdp        (501) staff       (20)     9212 2023-07-22 14:59:08.000000 nids_transformers-0.1.1/nids_transformers.egg-info/PKG-INFO
+-rw-r--r--   0 rdp        (501) staff       (20)      449 2023-07-22 14:59:08.000000 nids_transformers-0.1.1/nids_transformers.egg-info/SOURCES.txt
+-rw-r--r--   0 rdp        (501) staff       (20)        1 2023-07-22 14:59:08.000000 nids_transformers-0.1.1/nids_transformers.egg-info/dependency_links.txt
+-rw-r--r--   0 rdp        (501) staff       (20)      212 2023-07-22 14:59:08.000000 nids_transformers-0.1.1/nids_transformers.egg-info/requires.txt
+-rw-r--r--   0 rdp        (501) staff       (20)       18 2023-07-22 14:59:08.000000 nids_transformers-0.1.1/nids_transformers.egg-info/top_level.txt
+-rw-r--r--   0 rdp        (501) staff       (20)       38 2023-07-22 14:59:08.192233 nids_transformers-0.1.1/setup.cfg
+-rw-r--r--   0 rdp        (501) staff       (20)      961 2023-07-22 14:58:41.000000 nids_transformers-0.1.1/setup.py
```

### Comparing `nids_transformers-0.1.0/nids_transformers/CORPUS.txt` & `nids_transformers-0.1.1/nids_transformers/CORPUS.txt`

 * *Files identical despite different names*

### Comparing `nids_transformers-0.1.0/nids_transformers/KMEANS-CLUSTER-CENTERS.npy` & `nids_transformers-0.1.1/nids_transformers/KMEANS-CLUSTER-CENTERS.npy`

 * *Files identical despite different names*

### Comparing `nids_transformers-0.1.0/nids_transformers/NIDSTransformers.py` & `nids_transformers-0.1.1/nids_transformers/NIDSTransformers.py`

 * *Files identical despite different names*

### Comparing `nids_transformers-0.1.0/nids_transformers/SCALER.pkl` & `nids_transformers-0.1.1/nids_transformers/SCALER.pkl`

 * *Files identical despite different names*

### Comparing `nids_transformers-0.1.0/nids_transformers/TAGS-NAMES-EMBEDDINGS.npy` & `nids_transformers-0.1.1/nids_transformers/TAGS-NAMES-EMBEDDINGS.npy`

 * *Files identical despite different names*

### Comparing `nids_transformers-0.1.0/setup.py` & `nids_transformers-0.1.1/setup.py`

 * *Files 16% similar despite different names*

```diff
@@ -4,26 +4,26 @@
     requirements = f.read().splitlines()
 
 with open("README.md", "r", encoding="utf-8") as f:
     long_description = f.read()
 
 setuptools.setup(
     name='nids_transformers',
-    version='0.1.0',
-    description="Tag Generation and Text Generation for Network Packets using Transformers",
+    version='0.1.1',
+    description="Tag Generation and Text Generation Inference for Network Packets using Transformers",
     keywords="NIDS Transformers",
     long_description=long_description,
     long_description_content_type="text/markdown",
-    license='MIT',
+    license='Apache License 2.0',
     author="Pahalavan R D",
     author_email='rdpahalavan24@gmail.com',
     packages=['nids_transformers'],
     python_requires='>=3.7.0',
     url='https://github.com/rdpahalavan/BERTSimilarWords',
     classifiers=[
         "Programming Language :: Python :: 3",
-        "License :: OSI Approved :: MIT License",
+        "License :: OSI Approved :: Apache Software License",
         "Operating System :: OS Independent",
     ],
     include_package_data=True,
     install_requires=requirements
 )
```

