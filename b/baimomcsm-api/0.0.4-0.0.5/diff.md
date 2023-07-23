# Comparing `tmp/baimomcsm_api-0.0.4.tar.gz` & `tmp/baimomcsm_api-0.0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist\baimomcsm_api-0.0.4.tar", last modified: Sat Jul 22 23:39:08 2023, max compression
+gzip compressed data, was "dist\baimomcsm_api-0.0.5.tar", last modified: Sun Jul 23 00:09:55 2023, max compression
```

## Comparing `baimomcsm_api-0.0.4.tar` & `baimomcsm_api-0.0.5.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxrwxrwx   0        0        0        0 2023-07-22 23:39:08.921743 baimomcsm_api-0.0.4/
--rw-rw-rw-   0        0        0       37 2023-07-21 05:42:37.000000 baimomcsm_api-0.0.4/MANIFEST.in
--rw-rw-rw-   0        0        0     2203 2023-07-22 23:39:08.920722 baimomcsm_api-0.0.4/PKG-INFO
--rw-rw-rw-   0        0        0      873 2023-07-22 23:32:50.000000 baimomcsm_api-0.0.4/README.md
-drwxrwxrwx   0        0        0        0 2023-07-22 23:39:08.908517 baimomcsm_api-0.0.4/baimomcsm_api/
--rw-rw-rw-   0        0        0       45 2023-07-21 05:33:57.000000 baimomcsm_api-0.0.4/baimomcsm_api/__init__.py
--rw-rw-rw-   0        0        0     3278 2023-07-22 13:03:27.000000 baimomcsm_api-0.0.4/baimomcsm_api/applications.py
--rw-rw-rw-   0        0        0      196 2023-07-20 11:37:00.000000 baimomcsm_api-0.0.4/baimomcsm_api/baimomcsm_error.py
--rw-rw-rw-   0        0        0     2555 2023-07-22 13:08:53.000000 baimomcsm_api-0.0.4/baimomcsm_api/common.py
--rw-rw-rw-   0        0        0      183 2023-07-20 08:13:27.000000 baimomcsm_api-0.0.4/baimomcsm_api/log_writer.py
--rw-rw-rw-   0        0        0     1740 2023-07-22 13:15:51.000000 baimomcsm_api-0.0.4/baimomcsm_api/request_sender.py
--rw-rw-rw-   0        0        0     3414 2023-07-22 23:32:21.000000 baimomcsm_api-0.0.4/baimomcsm_api/users.py
-drwxrwxrwx   0        0        0        0 2023-07-22 23:39:08.918398 baimomcsm_api-0.0.4/baimomcsm_api.egg-info/
--rw-rw-rw-   0        0        0     2203 2023-07-22 23:39:08.000000 baimomcsm_api-0.0.4/baimomcsm_api.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      410 2023-07-22 23:39:08.000000 baimomcsm_api-0.0.4/baimomcsm_api.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-22 23:39:08.000000 baimomcsm_api-0.0.4/baimomcsm_api.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        9 2023-07-22 23:39:08.000000 baimomcsm_api-0.0.4/baimomcsm_api.egg-info/requires.txt
--rw-rw-rw-   0        0        0       14 2023-07-22 23:39:08.000000 baimomcsm_api-0.0.4/baimomcsm_api.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-22 23:39:08.921743 baimomcsm_api-0.0.4/setup.cfg
--rw-rw-rw-   0        0        0     1568 2023-07-22 23:38:36.000000 baimomcsm_api-0.0.4/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 00:09:55.163041 baimomcsm_api-0.0.5/
+-rw-rw-rw-   0        0        0       37 2023-07-21 05:42:37.000000 baimomcsm_api-0.0.5/MANIFEST.in
+-rw-rw-rw-   0        0        0     2203 2023-07-23 00:09:55.162220 baimomcsm_api-0.0.5/PKG-INFO
+-rw-rw-rw-   0        0        0      873 2023-07-22 23:32:50.000000 baimomcsm_api-0.0.5/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 00:09:55.091860 baimomcsm_api-0.0.5/baimomcsm_api/
+-rw-rw-rw-   0        0        0      200 2023-07-22 23:58:58.000000 baimomcsm_api-0.0.5/baimomcsm_api/__init__.py
+-rw-rw-rw-   0        0        0     3278 2023-07-22 13:03:27.000000 baimomcsm_api-0.0.5/baimomcsm_api/applications.py
+-rw-rw-rw-   0        0        0      196 2023-07-20 11:37:00.000000 baimomcsm_api-0.0.5/baimomcsm_api/baimomcsm_error.py
+-rw-rw-rw-   0        0        0     2555 2023-07-22 13:08:53.000000 baimomcsm_api-0.0.5/baimomcsm_api/common.py
+-rw-rw-rw-   0        0        0      183 2023-07-20 08:13:27.000000 baimomcsm_api-0.0.5/baimomcsm_api/log_writer.py
+-rw-rw-rw-   0        0        0     1740 2023-07-22 13:15:51.000000 baimomcsm_api-0.0.5/baimomcsm_api/request_sender.py
+-rw-rw-rw-   0        0        0     3414 2023-07-22 23:32:21.000000 baimomcsm_api-0.0.5/baimomcsm_api/users.py
+drwxrwxrwx   0        0        0        0 2023-07-23 00:09:55.103338 baimomcsm_api-0.0.5/baimomcsm_api.egg-info/
+-rw-rw-rw-   0        0        0     2203 2023-07-23 00:09:54.000000 baimomcsm_api-0.0.5/baimomcsm_api.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      410 2023-07-23 00:09:54.000000 baimomcsm_api-0.0.5/baimomcsm_api.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 00:09:54.000000 baimomcsm_api-0.0.5/baimomcsm_api.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        9 2023-07-23 00:09:54.000000 baimomcsm_api-0.0.5/baimomcsm_api.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       14 2023-07-23 00:09:54.000000 baimomcsm_api-0.0.5/baimomcsm_api.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 00:09:55.163041 baimomcsm_api-0.0.5/setup.cfg
+-rw-rw-rw-   0        0        0     1568 2023-07-23 00:09:41.000000 baimomcsm_api-0.0.5/setup.py
```

### Comparing `baimomcsm_api-0.0.4/PKG-INFO` & `baimomcsm_api-0.0.5/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: baimomcsm_api
-Version: 0.0.4
+Version: 0.0.5
 Summary: MCSManager API for Python (开发中)
 Home-page: https://github.com/Zhou-Shilin/BaimoMCSManager-API
 Author: BaimoQilin
 Author-email: admin@baimoqilin.top
 License: Apache 2.0
 Description: # BaimoMCSManager API for `Python`
         [![PRs welcome](https://img.shields.io/badge/PRs-welcome-20BF20)](https://github.com/Zhou-Shilin/BaimoMCSManager-API/pulls)
```

### Comparing `baimomcsm_api-0.0.4/README.md` & `baimomcsm_api-0.0.5/README.md`

 * *Files identical despite different names*

### Comparing `baimomcsm_api-0.0.4/baimomcsm_api/applications.py` & `baimomcsm_api-0.0.5/baimomcsm_api/applications.py`

 * *Files identical despite different names*

### Comparing `baimomcsm_api-0.0.4/baimomcsm_api/common.py` & `baimomcsm_api-0.0.5/baimomcsm_api/common.py`

 * *Files identical despite different names*

### Comparing `baimomcsm_api-0.0.4/baimomcsm_api/request_sender.py` & `baimomcsm_api-0.0.5/baimomcsm_api/request_sender.py`

 * *Files identical despite different names*

### Comparing `baimomcsm_api-0.0.4/baimomcsm_api/users.py` & `baimomcsm_api-0.0.5/baimomcsm_api/users.py`

 * *Files identical despite different names*

### Comparing `baimomcsm_api-0.0.4/baimomcsm_api.egg-info/PKG-INFO` & `baimomcsm_api-0.0.5/baimomcsm_api.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: baimomcsm-api
-Version: 0.0.4
+Version: 0.0.5
 Summary: MCSManager API for Python (开发中)
 Home-page: https://github.com/Zhou-Shilin/BaimoMCSManager-API
 Author: BaimoQilin
 Author-email: admin@baimoqilin.top
 License: Apache 2.0
 Description: # BaimoMCSManager API for `Python`
         [![PRs welcome](https://img.shields.io/badge/PRs-welcome-20BF20)](https://github.com/Zhou-Shilin/BaimoMCSManager-API/pulls)
```

### Comparing `baimomcsm_api-0.0.4/setup.py` & `baimomcsm_api-0.0.5/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from distutils.core import setup
 from setuptools import find_packages
 
 with open("README.md", "r", encoding="utf-8") as f:
   long_description = f.read()
 
 setup(name='baimomcsm_api',  # 包名
-      version='0.0.4',  # 版本号
+      version='0.0.5',  # 版本号
       description='MCSManager API for Python (开发中)',
       long_description=long_description,
       long_description_content_type="text/markdown",
       author='BaimoQilin',
       author_email='admin@baimoqilin.top',
       url='https://github.com/Zhou-Shilin/BaimoMCSManager-API',
       install_requires=["requests"],
```

