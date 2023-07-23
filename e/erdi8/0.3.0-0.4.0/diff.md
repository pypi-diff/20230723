# Comparing `tmp/erdi8-0.3.0.tar.gz` & `tmp/erdi8-0.4.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "erdi8-0.3.0.tar", last modified: Tue May 30 22:32:34 2023, max compression
+gzip compressed data, was "erdi8-0.4.0.tar", last modified: Sun Jul 23 00:19:47 2023, max compression
```

## Comparing `erdi8-0.3.0.tar` & `erdi8-0.4.0.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxrwxr-x   0 andreas   (1000) andreas   (1000)        0 2023-05-30 22:32:34.852519 erdi8-0.3.0/
--rw-rw-r--   0 andreas   (1000) andreas   (1000)    35149 2022-05-15 15:48:18.000000 erdi8-0.3.0/LICENSE
--rw-rw-r--   0 andreas   (1000) andreas   (1000)       18 2022-05-15 15:48:18.000000 erdi8-0.3.0/MANIFEST.in
--rw-rw-r--   0 andreas   (1000) andreas   (1000)     6691 2023-05-30 22:32:34.852519 erdi8-0.3.0/PKG-INFO
--rw-rw-r--   0 andreas   (1000) andreas   (1000)     5950 2023-05-30 22:26:59.000000 erdi8-0.3.0/README.md
-drwxrwxr-x   0 andreas   (1000) andreas   (1000)        0 2023-05-30 22:32:34.852519 erdi8-0.3.0/erdi8/
--rw-rw-r--   0 andreas   (1000) andreas   (1000)       30 2022-05-15 15:48:18.000000 erdi8-0.3.0/erdi8/__init__.py
--rw-rw-r--   0 andreas   (1000) andreas   (1000)     5178 2023-05-30 21:17:53.000000 erdi8-0.3.0/erdi8/erdi8.py
-drwxrwxr-x   0 andreas   (1000) andreas   (1000)        0 2023-05-30 22:32:34.852519 erdi8-0.3.0/erdi8.egg-info/
--rw-rw-r--   0 andreas   (1000) andreas   (1000)     6691 2023-05-30 22:32:34.000000 erdi8-0.3.0/erdi8.egg-info/PKG-INFO
--rw-rw-r--   0 andreas   (1000) andreas   (1000)      187 2023-05-30 22:32:34.000000 erdi8-0.3.0/erdi8.egg-info/SOURCES.txt
--rw-rw-r--   0 andreas   (1000) andreas   (1000)        1 2023-05-30 22:32:34.000000 erdi8-0.3.0/erdi8.egg-info/dependency_links.txt
--rw-rw-r--   0 andreas   (1000) andreas   (1000)        6 2023-05-30 22:32:34.000000 erdi8-0.3.0/erdi8.egg-info/top_level.txt
--rw-rw-r--   0 andreas   (1000) andreas   (1000)       38 2023-05-30 22:32:34.852519 erdi8-0.3.0/setup.cfg
--rw-rw-r--   0 andreas   (1000) andreas   (1000)     1786 2023-05-30 22:27:49.000000 erdi8-0.3.0/setup.py
+drwxrwxr-x   0 andreas   (1000) andreas   (1000)        0 2023-07-23 00:19:47.220759 erdi8-0.4.0/
+-rw-rw-r--   0 andreas   (1000) andreas   (1000)    35149 2022-05-15 15:48:18.000000 erdi8-0.4.0/LICENSE
+-rw-rw-r--   0 andreas   (1000) andreas   (1000)       18 2022-05-15 15:48:18.000000 erdi8-0.4.0/MANIFEST.in
+-rw-rw-r--   0 andreas   (1000) andreas   (1000)    13923 2023-07-23 00:19:47.220759 erdi8-0.4.0/PKG-INFO
+-rw-rw-r--   0 andreas   (1000) andreas   (1000)    13181 2023-07-23 00:17:38.000000 erdi8-0.4.0/README.md
+drwxrwxr-x   0 andreas   (1000) andreas   (1000)        0 2023-07-23 00:19:47.220759 erdi8-0.4.0/erdi8/
+-rw-rw-r--   0 andreas   (1000) andreas   (1000)       30 2022-05-15 15:48:18.000000 erdi8-0.4.0/erdi8/__init__.py
+-rw-rw-r--   0 andreas   (1000) andreas   (1000)    11296 2023-07-23 00:15:09.000000 erdi8-0.4.0/erdi8/erdi8.py
+drwxrwxr-x   0 andreas   (1000) andreas   (1000)        0 2023-07-23 00:19:47.220759 erdi8-0.4.0/erdi8.egg-info/
+-rw-rw-r--   0 andreas   (1000) andreas   (1000)    13923 2023-07-23 00:19:47.000000 erdi8-0.4.0/erdi8.egg-info/PKG-INFO
+-rw-rw-r--   0 andreas   (1000) andreas   (1000)      187 2023-07-23 00:19:47.000000 erdi8-0.4.0/erdi8.egg-info/SOURCES.txt
+-rw-rw-r--   0 andreas   (1000) andreas   (1000)        1 2023-07-23 00:19:47.000000 erdi8-0.4.0/erdi8.egg-info/dependency_links.txt
+-rw-rw-r--   0 andreas   (1000) andreas   (1000)        6 2023-07-23 00:19:47.000000 erdi8-0.4.0/erdi8.egg-info/top_level.txt
+-rw-rw-r--   0 andreas   (1000) andreas   (1000)       38 2023-07-23 00:19:47.220759 erdi8-0.4.0/setup.cfg
+-rw-rw-r--   0 andreas   (1000) andreas   (1000)     1787 2023-07-23 00:19:23.000000 erdi8-0.4.0/setup.py
```

### Comparing `erdi8-0.3.0/LICENSE` & `erdi8-0.4.0/LICENSE`

 * *Files identical despite different names*

### Comparing `erdi8-0.3.0/setup.py` & `erdi8-0.4.0/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -17,27 +17,27 @@
 from setuptools import setup
 
 with open("README.md", "r") as f:
     long_description = f.read()
 
 setup(
     name='erdi8',
-    version='0.3.0',
+    version='0.4.0',
     url='https://github.com/athalhammer/erdi8',
     author='Andreas Thalhammer',
     author_email='andreas@thalhammer.bayern',
     description='Count according to lower case alphabet and numbers (without ambiguous 0, 1, and l) and always start with a letter',
     long_description=long_description,
     long_description_content_type="text/markdown",
     packages=['erdi8'],
     classifiers=[
-        'Programming Language :: Python :: 3.7',
         'Programming Language :: Python :: 3.8',
         'Programming Language :: Python :: 3.9',
         'Programming Language :: Python :: 3.10',
+        'Programming Language :: Python :: 3.11',
         'License :: OSI Approved :: GNU General Public License v3 (GPLv3)',
         'Operating System :: OS Independent',
         'Topic :: Other/Nonlisted Topic',
     ],
-    python_requires='>=3.7',
+    python_requires='>=3.8',
     install_requires=[]
 )
```

