# Comparing `tmp/zheinit-0.0.72.tar.gz` & `tmp/zheinit-0.0.73.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "zheinit-0.0.72.tar", last modified: Sun Jul 23 15:00:49 2023, max compression
+gzip compressed data, was "zheinit-0.0.73.tar", last modified: Sun Jul 23 15:03:36 2023, max compression
```

## Comparing `zheinit-0.0.72.tar` & `zheinit-0.0.73.tar`

### file list

```diff
@@ -1,18 +1,18 @@
-drwxr-xr-x   0 dengyifan   (501) staff       (20)        0 2023-07-23 15:00:49.258760 zheinit-0.0.72/
--rw-r--r--   0 dengyifan   (501) staff       (20)       21 2023-07-23 14:48:03.000000 zheinit-0.0.72/MANIFEST.in
--rw-r--r--   0 dengyifan   (501) staff       (20)      376 2023-07-23 15:00:49.258567 zheinit-0.0.72/PKG-INFO
--rw-r--r--   0 dengyifan   (501) staff       (20)      138 2023-07-23 13:52:05.000000 zheinit-0.0.72/README.md
--rw-r--r--   0 dengyifan   (501) staff       (20)       38 2023-07-23 15:00:49.258811 zheinit-0.0.72/setup.cfg
--rw-r--r--   0 dengyifan   (501) staff       (20)      784 2023-07-23 15:00:47.000000 zheinit-0.0.72/setup.py
-drwxr-xr-x   0 dengyifan   (501) staff       (20)        0 2023-07-23 15:00:49.256911 zheinit-0.0.72/zheinit/
--rw-r--r--   0 dengyifan   (501) staff       (20)        0 2023-07-23 14:24:47.000000 zheinit-0.0.72/zheinit/__init__.py
--rw-r--r--   0 dengyifan   (501) staff       (20)     3773 2023-07-23 13:48:55.000000 zheinit-0.0.72/zheinit/bash_config.txt
--rw-r--r--   0 dengyifan   (501) staff       (20)     5989 2023-07-23 14:32:59.000000 zheinit-0.0.72/zheinit/env.py
--rw-r--r--   0 dengyifan   (501) staff       (20)     4412 2023-07-23 15:00:41.000000 zheinit-0.0.72/zheinit/utils.py
-drwxr-xr-x   0 dengyifan   (501) staff       (20)        0 2023-07-23 15:00:49.258299 zheinit-0.0.72/zheinit.egg-info/
--rw-r--r--   0 dengyifan   (501) staff       (20)      376 2023-07-23 15:00:49.000000 zheinit-0.0.72/zheinit.egg-info/PKG-INFO
--rw-r--r--   0 dengyifan   (501) staff       (20)      294 2023-07-23 15:00:49.000000 zheinit-0.0.72/zheinit.egg-info/SOURCES.txt
--rw-r--r--   0 dengyifan   (501) staff       (20)        1 2023-07-23 15:00:49.000000 zheinit-0.0.72/zheinit.egg-info/dependency_links.txt
--rw-r--r--   0 dengyifan   (501) staff       (20)       42 2023-07-23 15:00:49.000000 zheinit-0.0.72/zheinit.egg-info/entry_points.txt
--rw-r--r--   0 dengyifan   (501) staff       (20)       18 2023-07-23 15:00:49.000000 zheinit-0.0.72/zheinit.egg-info/requires.txt
--rw-r--r--   0 dengyifan   (501) staff       (20)        8 2023-07-23 15:00:49.000000 zheinit-0.0.72/zheinit.egg-info/top_level.txt
+drwxr-xr-x   0 dengyifan   (501) staff       (20)        0 2023-07-23 15:03:36.544463 zheinit-0.0.73/
+-rw-r--r--   0 dengyifan   (501) staff       (20)       21 2023-07-23 14:48:03.000000 zheinit-0.0.73/MANIFEST.in
+-rw-r--r--   0 dengyifan   (501) staff       (20)      376 2023-07-23 15:03:36.544270 zheinit-0.0.73/PKG-INFO
+-rw-r--r--   0 dengyifan   (501) staff       (20)      138 2023-07-23 13:52:05.000000 zheinit-0.0.73/README.md
+-rw-r--r--   0 dengyifan   (501) staff       (20)       38 2023-07-23 15:03:36.544513 zheinit-0.0.73/setup.cfg
+-rw-r--r--   0 dengyifan   (501) staff       (20)      784 2023-07-23 15:03:34.000000 zheinit-0.0.73/setup.py
+drwxr-xr-x   0 dengyifan   (501) staff       (20)        0 2023-07-23 15:03:36.542871 zheinit-0.0.73/zheinit/
+-rw-r--r--   0 dengyifan   (501) staff       (20)        0 2023-07-23 14:24:47.000000 zheinit-0.0.73/zheinit/__init__.py
+-rw-r--r--   0 dengyifan   (501) staff       (20)     3773 2023-07-23 13:48:55.000000 zheinit-0.0.73/zheinit/bash_config.txt
+-rw-r--r--   0 dengyifan   (501) staff       (20)     6000 2023-07-23 15:03:24.000000 zheinit-0.0.73/zheinit/env.py
+-rw-r--r--   0 dengyifan   (501) staff       (20)     4412 2023-07-23 15:00:41.000000 zheinit-0.0.73/zheinit/utils.py
+drwxr-xr-x   0 dengyifan   (501) staff       (20)        0 2023-07-23 15:03:36.544030 zheinit-0.0.73/zheinit.egg-info/
+-rw-r--r--   0 dengyifan   (501) staff       (20)      376 2023-07-23 15:03:36.000000 zheinit-0.0.73/zheinit.egg-info/PKG-INFO
+-rw-r--r--   0 dengyifan   (501) staff       (20)      294 2023-07-23 15:03:36.000000 zheinit-0.0.73/zheinit.egg-info/SOURCES.txt
+-rw-r--r--   0 dengyifan   (501) staff       (20)        1 2023-07-23 15:03:36.000000 zheinit-0.0.73/zheinit.egg-info/dependency_links.txt
+-rw-r--r--   0 dengyifan   (501) staff       (20)       42 2023-07-23 15:03:36.000000 zheinit-0.0.73/zheinit.egg-info/entry_points.txt
+-rw-r--r--   0 dengyifan   (501) staff       (20)       18 2023-07-23 15:03:36.000000 zheinit-0.0.73/zheinit.egg-info/requires.txt
+-rw-r--r--   0 dengyifan   (501) staff       (20)        8 2023-07-23 15:03:36.000000 zheinit-0.0.73/zheinit.egg-info/top_level.txt
```

### Comparing `zheinit-0.0.72/setup.py` & `zheinit-0.0.73/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 #!/usr/bin/env python
 # coding: utf-8
 
 from setuptools import setup, find_packages
 
 setup(
     name='zheinit',
-    version='0.0.72',
+    version='0.0.73',
     author='deng1fan',
     author_email='dengyifan@iie.ac.cn',
     url='https://github.com/deng1fan',
     description=u'Init zhei environment.',
     long_description=open("README.md", "r", encoding='utf-8').read(),
     long_description_content_type="text/markdown",
     packages=find_packages(),
```

### Comparing `zheinit-0.0.72/zheinit/bash_config.txt` & `zheinit-0.0.73/zheinit/bash_config.txt`

 * *Files identical despite different names*

### Comparing `zheinit-0.0.72/zheinit/env.py` & `zheinit-0.0.73/zheinit/env.py`

 * *Files 0% similar despite different names*

```diff
@@ -46,14 +46,15 @@
         echo(" ", "blue")
         echo("1、设置 pip 源", "blue") 
         echo("2、安装 MiniConda", "blue")
         echo("3、安装 ranger 并自动配置", "blue")
         echo("4、创建 Conda  Pytorch 环境", "blue")
         echo("5、生成公钥", "blue")
         echo("0、退出", "blue")
+        echo(" ", "blue")
         echo("请输入操作序号：", "yellow")
         step = input()
         if step == "1":
             # ---------------------------------------------------------------------------- #
             #                         设置 pip 源                                     
             # ---------------------------------------------------------------------------- #
             pip_source = [
@@ -84,16 +85,16 @@
             ]
             run_cmd(ranger)
 
         elif step == "4":
             # ---------------------------------------------------------------------------- #
             #                         创建 zhei 环境                                     
             # ---------------------------------------------------------------------------- #
-            python_version = input("请输入 Python 版本号，默认为 3.9：", "3.9")
-            env_name = input("请输入环境名称，将会自动安装 zhei 包，默认名称为 zhei：", "zhei")
+            python_version = input("请输入 Python 版本号，默认为 3.9：")
+            env_name = input("请输入环境名称，将会自动安装 zhei 包，默认名称为 zhei：")
             zhei = [
                 "conda create -n {} python={}".format(env_name, python_version),
                 "conda activate {}".format(env_name),
                 "pip install zhei --upgrade",
             ]
             run_cmd(zhei)
```

### Comparing `zheinit-0.0.72/zheinit/utils.py` & `zheinit-0.0.73/zheinit/utils.py`

 * *Files identical despite different names*

