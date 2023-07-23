# Comparing `tmp/zhei-init-0.0.3.tar.gz` & `tmp/zhei-init-0.0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "zhei-init-0.0.3.tar", last modified: Sun Jul 23 14:22:43 2023, max compression
+gzip compressed data, was "zhei-init-0.0.4.tar", last modified: Sun Jul 23 14:25:00 2023, max compression
```

## Comparing `zhei-init-0.0.3.tar` & `zhei-init-0.0.4.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxr-xr-x   0 dengyifan   (501) staff       (20)        0 2023-07-23 14:22:43.656100 zhei-init-0.0.3/
--rw-r--r--   0 dengyifan   (501) staff       (20)      377 2023-07-23 14:22:43.655924 zhei-init-0.0.3/PKG-INFO
--rw-r--r--   0 dengyifan   (501) staff       (20)      138 2023-07-23 13:52:05.000000 zhei-init-0.0.3/README.md
-drwxr-xr-x   0 dengyifan   (501) staff       (20)        0 2023-07-23 14:22:43.654650 zhei-init-0.0.3/init/
--rw-r--r--   0 dengyifan   (501) staff       (20)       22 2023-07-23 14:20:40.000000 zhei-init-0.0.3/init/__init__.py
--rw-r--r--   0 dengyifan   (501) staff       (20)     5986 2023-07-23 14:20:01.000000 zhei-init-0.0.3/init/env.py
--rw-r--r--   0 dengyifan   (501) staff       (20)     4378 2023-07-23 13:44:42.000000 zhei-init-0.0.3/init/utils.py
--rw-r--r--   0 dengyifan   (501) staff       (20)       38 2023-07-23 14:22:43.656150 zhei-init-0.0.3/setup.cfg
--rw-r--r--   0 dengyifan   (501) staff       (20)      761 2023-07-23 14:22:41.000000 zhei-init-0.0.3/setup.py
-drwxr-xr-x   0 dengyifan   (501) staff       (20)        0 2023-07-23 14:22:43.655713 zhei-init-0.0.3/zhei_init.egg-info/
--rw-r--r--   0 dengyifan   (501) staff       (20)      377 2023-07-23 14:22:43.000000 zhei-init-0.0.3/zhei_init.egg-info/PKG-INFO
--rw-r--r--   0 dengyifan   (501) staff       (20)      261 2023-07-23 14:22:43.000000 zhei-init-0.0.3/zhei_init.egg-info/SOURCES.txt
--rw-r--r--   0 dengyifan   (501) staff       (20)        1 2023-07-23 14:22:43.000000 zhei-init-0.0.3/zhei_init.egg-info/dependency_links.txt
--rw-r--r--   0 dengyifan   (501) staff       (20)       34 2023-07-23 14:22:43.000000 zhei-init-0.0.3/zhei_init.egg-info/entry_points.txt
--rw-r--r--   0 dengyifan   (501) staff       (20)       13 2023-07-23 14:22:43.000000 zhei-init-0.0.3/zhei_init.egg-info/requires.txt
--rw-r--r--   0 dengyifan   (501) staff       (20)        5 2023-07-23 14:22:43.000000 zhei-init-0.0.3/zhei_init.egg-info/top_level.txt
+drwxr-xr-x   0 dengyifan   (501) staff       (20)        0 2023-07-23 14:25:00.977919 zhei-init-0.0.4/
+-rw-r--r--   0 dengyifan   (501) staff       (20)      377 2023-07-23 14:25:00.977721 zhei-init-0.0.4/PKG-INFO
+-rw-r--r--   0 dengyifan   (501) staff       (20)      138 2023-07-23 13:52:05.000000 zhei-init-0.0.4/README.md
+-rw-r--r--   0 dengyifan   (501) staff       (20)       38 2023-07-23 14:25:00.977979 zhei-init-0.0.4/setup.cfg
+-rw-r--r--   0 dengyifan   (501) staff       (20)      761 2023-07-23 14:24:58.000000 zhei-init-0.0.4/setup.py
+drwxr-xr-x   0 dengyifan   (501) staff       (20)        0 2023-07-23 14:25:00.976559 zhei-init-0.0.4/zhei-init/
+-rw-r--r--   0 dengyifan   (501) staff       (20)        0 2023-07-23 14:24:47.000000 zhei-init-0.0.4/zhei-init/__init__.py
+-rw-r--r--   0 dengyifan   (501) staff       (20)     5986 2023-07-23 14:20:01.000000 zhei-init-0.0.4/zhei-init/env.py
+-rw-r--r--   0 dengyifan   (501) staff       (20)     4378 2023-07-23 13:44:42.000000 zhei-init-0.0.4/zhei-init/utils.py
+drwxr-xr-x   0 dengyifan   (501) staff       (20)        0 2023-07-23 14:25:00.977489 zhei-init-0.0.4/zhei_init.egg-info/
+-rw-r--r--   0 dengyifan   (501) staff       (20)      377 2023-07-23 14:25:00.000000 zhei-init-0.0.4/zhei_init.egg-info/PKG-INFO
+-rw-r--r--   0 dengyifan   (501) staff       (20)      276 2023-07-23 14:25:00.000000 zhei-init-0.0.4/zhei_init.egg-info/SOURCES.txt
+-rw-r--r--   0 dengyifan   (501) staff       (20)        1 2023-07-23 14:25:00.000000 zhei-init-0.0.4/zhei_init.egg-info/dependency_links.txt
+-rw-r--r--   0 dengyifan   (501) staff       (20)       34 2023-07-23 14:25:00.000000 zhei-init-0.0.4/zhei_init.egg-info/entry_points.txt
+-rw-r--r--   0 dengyifan   (501) staff       (20)       13 2023-07-23 14:25:00.000000 zhei-init-0.0.4/zhei_init.egg-info/requires.txt
+-rw-r--r--   0 dengyifan   (501) staff       (20)       10 2023-07-23 14:25:00.000000 zhei-init-0.0.4/zhei_init.egg-info/top_level.txt
```

### Comparing `zhei-init-0.0.3/init/env.py` & `zhei-init-0.0.4/zhei-init/env.py`

 * *Files identical despite different names*

### Comparing `zhei-init-0.0.3/init/utils.py` & `zhei-init-0.0.4/zhei-init/utils.py`

 * *Files identical despite different names*

### Comparing `zhei-init-0.0.3/setup.py` & `zhei-init-0.0.4/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 #!/usr/bin/env python
 # coding: utf-8
 
 from setuptools import setup, find_packages
 
 setup(
     name='zhei-init',
-    version='0.0.3',
+    version='0.0.4',
     author='deng1fan',
     author_email='dengyifan@iie.ac.cn',
     url='https://github.com/deng1fan',
     description=u'Init zhei environment.',
     long_description=open("README.md", "r", encoding='utf-8').read(),
     long_description_content_type="text/markdown",
     packages=find_packages(),
```

