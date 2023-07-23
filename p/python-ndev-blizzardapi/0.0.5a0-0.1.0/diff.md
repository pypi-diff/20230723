# Comparing `tmp/python-ndev-blizzardapi-0.0.5a0.tar.gz` & `tmp/python-ndev-blizzardapi-0.1.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "python-ndev-blizzardapi-0.0.5a0.tar", last modified: Sat Jul 15 13:33:02 2023, max compression
+gzip compressed data, was "python-ndev-blizzardapi-0.1.0.tar", last modified: Sun Jul 23 03:42:56 2023, max compression
```

## Comparing `python-ndev-blizzardapi-0.0.5a0.tar` & `python-ndev-blizzardapi-0.1.0.1.tar`

### file list

```diff
@@ -1,23 +1,23 @@
-drwxrwxrwx   0        0        0        0 2023-07-15 13:33:02.947970 python-ndev-blizzardapi-0.0.5a0/
--rw-rw-rw-   0        0        0      134 2023-07-14 20:43:22.000000 python-ndev-blizzardapi-0.0.5a0/MANIFEST.in
--rw-rw-rw-   0        0        0     2311 2023-07-15 13:33:02.946972 python-ndev-blizzardapi-0.0.5a0/PKG-INFO
--rw-rw-rw-   0        0        0     1582 2023-07-14 18:06:48.000000 python-ndev-blizzardapi-0.0.5a0/README.md
-drwxrwxrwx   0        0        0        0 2023-07-15 13:33:02.912859 python-ndev-blizzardapi-0.0.5a0/blizzardAPI/
--rw-rw-rw-   0        0        0      161 2023-03-11 02:36:09.000000 python-ndev-blizzardapi-0.0.5a0/blizzardAPI/__init__.py
--rw-rw-rw-   0        0        0     4981 2023-06-24 20:44:02.000000 python-ndev-blizzardapi-0.0.5a0/blizzardAPI/api.py
-drwxrwxrwx   0        0        0        0 2023-07-15 13:33:02.927924 python-ndev-blizzardapi-0.0.5a0/blizzardAPI/battlenet/
--rw-rw-rw-   0        0        0       25 2023-03-10 03:36:02.000000 python-ndev-blizzardapi-0.0.5a0/blizzardAPI/battlenet/__init__.py
--rw-rw-rw-   0        0        0      458 2023-03-10 03:44:26.000000 python-ndev-blizzardapi-0.0.5a0/blizzardAPI/battlenet/battlenet_api.py
--rw-rw-rw-   0        0        0     1539 2023-03-10 03:47:42.000000 python-ndev-blizzardapi-0.0.5a0/blizzardAPI/battlenet/battlenet_oauth.py
--rw-rw-rw-   0        0        0      539 2023-06-21 18:46:57.000000 python-ndev-blizzardapi-0.0.5a0/blizzardAPI/blizzard_api.py
-drwxrwxrwx   0        0        0        0 2023-07-15 13:33:02.938451 python-ndev-blizzardapi-0.0.5a0/blizzardAPI/tests/
--rw-rw-rw-   0        0        0        0 2023-06-21 22:10:25.000000 python-ndev-blizzardapi-0.0.5a0/blizzardAPI/tests/__init__.py
--rw-rw-rw-   0        0        0     1288 2023-06-22 00:13:18.000000 python-ndev-blizzardapi-0.0.5a0/blizzardAPI/tests/conftest.py
-drwxrwxrwx   0        0        0        0 2023-07-15 13:33:02.944970 python-ndev-blizzardapi-0.0.5a0/python_ndev_blizzardapi.egg-info/
--rw-rw-rw-   0        0        0     2311 2023-07-15 13:33:02.000000 python-ndev-blizzardapi-0.0.5a0/python_ndev_blizzardapi.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      509 2023-07-15 13:33:02.000000 python-ndev-blizzardapi-0.0.5a0/python_ndev_blizzardapi.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-15 13:33:02.000000 python-ndev-blizzardapi-0.0.5a0/python_ndev_blizzardapi.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       17 2023-07-15 13:33:02.000000 python-ndev-blizzardapi-0.0.5a0/python_ndev_blizzardapi.egg-info/requires.txt
--rw-rw-rw-   0        0        0       12 2023-07-15 13:33:02.000000 python-ndev-blizzardapi-0.0.5a0/python_ndev_blizzardapi.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-15 13:33:02.947970 python-ndev-blizzardapi-0.0.5a0/setup.cfg
--rw-rw-rw-   0        0        0     1010 2023-07-15 13:27:51.000000 python-ndev-blizzardapi-0.0.5a0/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 03:42:56.806520 python-ndev-blizzardapi-0.1.0/
+-rw-rw-rw-   0        0        0      134 2023-07-14 20:43:22.000000 python-ndev-blizzardapi-0.1.0/MANIFEST.in
+-rw-rw-rw-   0        0        0     3249 2023-07-23 03:42:56.805520 python-ndev-blizzardapi-0.1.0/PKG-INFO
+-rw-rw-rw-   0        0        0     2522 2023-07-23 03:28:03.000000 python-ndev-blizzardapi-0.1.0/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 03:42:56.793492 python-ndev-blizzardapi-0.1.0/blizzardAPI/
+-rw-rw-rw-   0        0        0      161 2023-03-11 02:36:09.000000 python-ndev-blizzardapi-0.1.0/blizzardAPI/__init__.py
+-rw-rw-rw-   0        0        0     4981 2023-06-24 20:44:02.000000 python-ndev-blizzardapi-0.1.0/blizzardAPI/api.py
+drwxrwxrwx   0        0        0        0 2023-07-23 03:42:56.797527 python-ndev-blizzardapi-0.1.0/blizzardAPI/battlenet/
+-rw-rw-rw-   0        0        0       25 2023-03-10 03:36:02.000000 python-ndev-blizzardapi-0.1.0/blizzardAPI/battlenet/__init__.py
+-rw-rw-rw-   0        0        0      458 2023-03-10 03:44:26.000000 python-ndev-blizzardapi-0.1.0/blizzardAPI/battlenet/battlenet_api.py
+-rw-rw-rw-   0        0        0     1539 2023-03-10 03:47:42.000000 python-ndev-blizzardapi-0.1.0/blizzardAPI/battlenet/battlenet_oauth.py
+-rw-rw-rw-   0        0        0     1475 2023-07-17 03:21:51.000000 python-ndev-blizzardapi-0.1.0/blizzardAPI/blizzard_api.py
+drwxrwxrwx   0        0        0        0 2023-07-23 03:42:56.799495 python-ndev-blizzardapi-0.1.0/blizzardAPI/tests/
+-rw-rw-rw-   0        0        0        0 2023-06-21 22:10:25.000000 python-ndev-blizzardapi-0.1.0/blizzardAPI/tests/__init__.py
+-rw-rw-rw-   0        0        0     3330 2023-07-23 02:33:06.000000 python-ndev-blizzardapi-0.1.0/blizzardAPI/tests/conftest.py
+drwxrwxrwx   0        0        0        0 2023-07-23 03:42:56.804493 python-ndev-blizzardapi-0.1.0/python_ndev_blizzardapi.egg-info/
+-rw-rw-rw-   0        0        0     3249 2023-07-23 03:42:56.000000 python-ndev-blizzardapi-0.1.0/python_ndev_blizzardapi.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      509 2023-07-23 03:42:56.000000 python-ndev-blizzardapi-0.1.0/python_ndev_blizzardapi.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 03:42:56.000000 python-ndev-blizzardapi-0.1.0/python_ndev_blizzardapi.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       38 2023-07-23 03:42:56.000000 python-ndev-blizzardapi-0.1.0/python_ndev_blizzardapi.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       12 2023-07-23 03:42:56.000000 python-ndev-blizzardapi-0.1.0/python_ndev_blizzardapi.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 03:42:56.806520 python-ndev-blizzardapi-0.1.0/setup.cfg
+-rw-rw-rw-   0        0        0     1037 2023-07-17 03:11:52.000000 python-ndev-blizzardapi-0.1.0/setup.py
```

### Comparing `python-ndev-blizzardapi-0.0.5a0/blizzardAPI/api.py` & `python-ndev-blizzardapi-0.1.0/blizzardAPI/api.py`

 * *Files identical despite different names*

### Comparing `python-ndev-blizzardapi-0.0.5a0/blizzardAPI/battlenet/battlenet_oauth.py` & `python-ndev-blizzardapi-0.1.0/blizzardAPI/battlenet/battlenet_oauth.py`

 * *Files identical despite different names*

### Comparing `python-ndev-blizzardapi-0.0.5a0/setup.py` & `python-ndev-blizzardapi-0.1.0/setup.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,15 +1,16 @@
 from setuptools import setup, find_packages
 
 setup(
     name="python-ndev-blizzardapi",
-    version="0.0.5-alpha",
+    version="0.1.0",
     packages=find_packages(),
     install_requires=[
         "requests>=2.28.2",
+        "python-dotenv>=1.0.0",
     ],
     author="natanrmaia",
     author_email="contato@natanael.dev.br",
     description="Python module created to integrate your Python project with the Blizzard API",
     long_description=open('README.md', 'r').read(),
     long_description_content_type='text/markdown',
     url="https://github.com/natanrmaia/python-ndev-blizzardapi",
```

