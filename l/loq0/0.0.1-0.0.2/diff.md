# Comparing `tmp/loq0-0.0.1.tar.gz` & `tmp/loq0-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "loq0-0.0.1.tar", last modified: Sat Jul 22 16:48:02 2023, max compression
+gzip compressed data, was "loq0-0.0.2.tar", last modified: Sun Jul 23 14:53:38 2023, max compression
```

## Comparing `loq0-0.0.1.tar` & `loq0-0.0.2.tar`

### file list

```diff
@@ -1,9 +1,9 @@
-drwxr-xr-x   0 seo_hyun   (501) staff       (20)        0 2023-07-22 16:48:02.258436 loq0-0.0.1/
--rw-r--r--   0 seo_hyun   (501) staff       (20)      557 2023-07-22 16:48:02.258069 loq0-0.0.1/PKG-INFO
-drwxr-xr-x   0 seo_hyun   (501) staff       (20)        0 2023-07-22 16:48:02.257484 loq0-0.0.1/loq0.egg-info/
--rw-r--r--   0 seo_hyun   (501) staff       (20)      557 2023-07-22 16:48:02.000000 loq0-0.0.1/loq0.egg-info/PKG-INFO
--rw-r--r--   0 seo_hyun   (501) staff       (20)      120 2023-07-22 16:48:02.000000 loq0-0.0.1/loq0.egg-info/SOURCES.txt
--rw-r--r--   0 seo_hyun   (501) staff       (20)        1 2023-07-22 16:48:02.000000 loq0-0.0.1/loq0.egg-info/dependency_links.txt
--rw-r--r--   0 seo_hyun   (501) staff       (20)        1 2023-07-22 16:48:02.000000 loq0-0.0.1/loq0.egg-info/top_level.txt
--rw-r--r--   0 seo_hyun   (501) staff       (20)       38 2023-07-22 16:48:02.258584 loq0-0.0.1/setup.cfg
--rw-r--r--   0 seo_hyun   (501) staff       (20)      615 2023-07-22 16:29:56.000000 loq0-0.0.1/setup.py
+drwxr-xr-x   0 seo_hyun   (501) staff       (20)        0 2023-07-23 14:53:38.303508 loq0-0.0.2/
+-rw-r--r--   0 seo_hyun   (501) staff       (20)      817 2023-07-23 14:53:38.303335 loq0-0.0.2/PKG-INFO
+drwxr-xr-x   0 seo_hyun   (501) staff       (20)        0 2023-07-23 14:53:38.303090 loq0-0.0.2/loq0.egg-info/
+-rw-r--r--   0 seo_hyun   (501) staff       (20)      817 2023-07-23 14:53:38.000000 loq0-0.0.2/loq0.egg-info/PKG-INFO
+-rw-r--r--   0 seo_hyun   (501) staff       (20)      120 2023-07-23 14:53:38.000000 loq0-0.0.2/loq0.egg-info/SOURCES.txt
+-rw-r--r--   0 seo_hyun   (501) staff       (20)        1 2023-07-23 14:53:38.000000 loq0-0.0.2/loq0.egg-info/dependency_links.txt
+-rw-r--r--   0 seo_hyun   (501) staff       (20)        1 2023-07-23 14:53:38.000000 loq0-0.0.2/loq0.egg-info/top_level.txt
+-rw-r--r--   0 seo_hyun   (501) staff       (20)       38 2023-07-23 14:53:38.303587 loq0-0.0.2/setup.cfg
+-rw-r--r--   0 seo_hyun   (501) staff       (20)      615 2023-07-23 14:51:38.000000 loq0-0.0.2/setup.py
```

### Comparing `loq0-0.0.1/setup.py` & `loq0-0.0.2/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import setuptools
 
 with open("../README.md", "r") as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="loq0",
-    version="0.0.1",
+    version="0.0.2",
     author="seorii",
     author_email="me@seorii.page",
     description="League of Quoridor",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/dastyinc/loq0",
     packages=setuptools.find_packages(),
```

