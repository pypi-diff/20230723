# Comparing `tmp/zheinit-0.0.7.tar.gz` & `tmp/zheinit-0.0.71.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "zheinit-0.0.7.tar", last modified: Sun Jul 23 14:48:18 2023, max compression
+gzip compressed data, was "zheinit-0.0.71.tar", last modified: Sun Jul 23 14:54:35 2023, max compression
```

## Comparing `zheinit-0.0.7.tar` & `zheinit-0.0.71.tar`

### file list

```diff
@@ -1,18 +1,18 @@
-drwxr-xr-x   0 dengyifan   (501) staff       (20)        0 2023-07-23 14:48:18.154291 zheinit-0.0.7/
--rw-r--r--   0 dengyifan   (501) staff       (20)       21 2023-07-23 14:48:03.000000 zheinit-0.0.7/MANIFEST.in
--rw-r--r--   0 dengyifan   (501) staff       (20)      375 2023-07-23 14:48:18.154101 zheinit-0.0.7/PKG-INFO
--rw-r--r--   0 dengyifan   (501) staff       (20)      138 2023-07-23 13:52:05.000000 zheinit-0.0.7/README.md
--rw-r--r--   0 dengyifan   (501) staff       (20)       38 2023-07-23 14:48:18.154338 zheinit-0.0.7/setup.cfg
--rw-r--r--   0 dengyifan   (501) staff       (20)      767 2023-07-23 14:48:14.000000 zheinit-0.0.7/setup.py
-drwxr-xr-x   0 dengyifan   (501) staff       (20)        0 2023-07-23 14:48:18.152971 zheinit-0.0.7/zheinit/
--rw-r--r--   0 dengyifan   (501) staff       (20)        0 2023-07-23 14:24:47.000000 zheinit-0.0.7/zheinit/__init__.py
--rw-r--r--   0 dengyifan   (501) staff       (20)     3773 2023-07-23 13:48:55.000000 zheinit-0.0.7/zheinit/bash_config.txt
--rw-r--r--   0 dengyifan   (501) staff       (20)     5989 2023-07-23 14:32:59.000000 zheinit-0.0.7/zheinit/env.py
--rw-r--r--   0 dengyifan   (501) staff       (20)     4378 2023-07-23 13:44:42.000000 zheinit-0.0.7/zheinit/utils.py
-drwxr-xr-x   0 dengyifan   (501) staff       (20)        0 2023-07-23 14:48:18.153861 zheinit-0.0.7/zheinit.egg-info/
--rw-r--r--   0 dengyifan   (501) staff       (20)      375 2023-07-23 14:48:18.000000 zheinit-0.0.7/zheinit.egg-info/PKG-INFO
--rw-r--r--   0 dengyifan   (501) staff       (20)      294 2023-07-23 14:48:18.000000 zheinit-0.0.7/zheinit.egg-info/SOURCES.txt
--rw-r--r--   0 dengyifan   (501) staff       (20)        1 2023-07-23 14:48:18.000000 zheinit-0.0.7/zheinit.egg-info/dependency_links.txt
--rw-r--r--   0 dengyifan   (501) staff       (20)       42 2023-07-23 14:48:18.000000 zheinit-0.0.7/zheinit.egg-info/entry_points.txt
--rw-r--r--   0 dengyifan   (501) staff       (20)       13 2023-07-23 14:48:18.000000 zheinit-0.0.7/zheinit.egg-info/requires.txt
--rw-r--r--   0 dengyifan   (501) staff       (20)        8 2023-07-23 14:48:18.000000 zheinit-0.0.7/zheinit.egg-info/top_level.txt
+drwxr-xr-x   0 dengyifan   (501) staff       (20)        0 2023-07-23 14:54:35.280125 zheinit-0.0.71/
+-rw-r--r--   0 dengyifan   (501) staff       (20)       21 2023-07-23 14:48:03.000000 zheinit-0.0.71/MANIFEST.in
+-rw-r--r--   0 dengyifan   (501) staff       (20)      376 2023-07-23 14:54:35.279942 zheinit-0.0.71/PKG-INFO
+-rw-r--r--   0 dengyifan   (501) staff       (20)      138 2023-07-23 13:52:05.000000 zheinit-0.0.71/README.md
+-rw-r--r--   0 dengyifan   (501) staff       (20)       38 2023-07-23 14:54:35.280174 zheinit-0.0.71/setup.cfg
+-rw-r--r--   0 dengyifan   (501) staff       (20)      768 2023-07-23 14:54:32.000000 zheinit-0.0.71/setup.py
+drwxr-xr-x   0 dengyifan   (501) staff       (20)        0 2023-07-23 14:54:35.278604 zheinit-0.0.71/zheinit/
+-rw-r--r--   0 dengyifan   (501) staff       (20)        0 2023-07-23 14:24:47.000000 zheinit-0.0.71/zheinit/__init__.py
+-rw-r--r--   0 dengyifan   (501) staff       (20)     3773 2023-07-23 13:48:55.000000 zheinit-0.0.71/zheinit/bash_config.txt
+-rw-r--r--   0 dengyifan   (501) staff       (20)     5989 2023-07-23 14:32:59.000000 zheinit-0.0.71/zheinit/env.py
+-rw-r--r--   0 dengyifan   (501) staff       (20)     4374 2023-07-23 14:54:21.000000 zheinit-0.0.71/zheinit/utils.py
+drwxr-xr-x   0 dengyifan   (501) staff       (20)        0 2023-07-23 14:54:35.279718 zheinit-0.0.71/zheinit.egg-info/
+-rw-r--r--   0 dengyifan   (501) staff       (20)      376 2023-07-23 14:54:35.000000 zheinit-0.0.71/zheinit.egg-info/PKG-INFO
+-rw-r--r--   0 dengyifan   (501) staff       (20)      294 2023-07-23 14:54:35.000000 zheinit-0.0.71/zheinit.egg-info/SOURCES.txt
+-rw-r--r--   0 dengyifan   (501) staff       (20)        1 2023-07-23 14:54:35.000000 zheinit-0.0.71/zheinit.egg-info/dependency_links.txt
+-rw-r--r--   0 dengyifan   (501) staff       (20)       42 2023-07-23 14:54:35.000000 zheinit-0.0.71/zheinit.egg-info/entry_points.txt
+-rw-r--r--   0 dengyifan   (501) staff       (20)       13 2023-07-23 14:54:35.000000 zheinit-0.0.71/zheinit.egg-info/requires.txt
+-rw-r--r--   0 dengyifan   (501) staff       (20)        8 2023-07-23 14:54:35.000000 zheinit-0.0.71/zheinit.egg-info/top_level.txt
```

### Comparing `zheinit-0.0.7/setup.py` & `zheinit-0.0.71/setup.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 #!/usr/bin/env python
 # coding: utf-8
 
 from setuptools import setup, find_packages
 
 setup(
     name='zheinit',
-    version='0.0.7',
+    version='0.0.71',
     author='deng1fan',
     author_email='dengyifan@iie.ac.cn',
     url='https://github.com/deng1fan',
     description=u'Init zhei environment.',
     long_description=open("README.md", "r", encoding='utf-8').read(),
     long_description_content_type="text/markdown",
     packages=find_packages(),
```

### Comparing `zheinit-0.0.7/zheinit/bash_config.txt` & `zheinit-0.0.71/zheinit/bash_config.txt`

 * *Files identical despite different names*

### Comparing `zheinit-0.0.7/zheinit/env.py` & `zheinit-0.0.71/zheinit/env.py`

 * *Files identical despite different names*

### Comparing `zheinit-0.0.7/zheinit/utils.py` & `zheinit-0.0.71/zheinit/utils.py`

 * *Files 1% similar despite different names*

```diff
@@ -11,15 +11,15 @@
         pkg_resources.get_distribution(package_name)
     except pkg_resources.DistributionNotFound:
         return False
     else:
         return True
 
 def echo(msg, color="green"):
-    os.system("ADD_COLOR \"{}\" {}".format(msg, color))
+    os.system("ADD_COLOR {} {}".format(msg, color))
 
 def run_cmd(cmd_list):
     if not isinstance(cmd_list, list):
         cmd_list = [cmd_list]
     for cmd in cmd_list:
         os.system(cmd)
```

