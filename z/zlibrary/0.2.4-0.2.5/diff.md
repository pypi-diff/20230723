# Comparing `tmp/zlibrary-0.2.4.tar.gz` & `tmp/zlibrary-0.2.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "zlibrary-0.2.4.tar", last modified: Mon Jul 10 20:51:11 2023, max compression
+gzip compressed data, was "zlibrary-0.2.5.tar", last modified: Sun Jul 23 00:54:51 2023, max compression
```

## Comparing `zlibrary-0.2.4.tar` & `zlibrary-0.2.5.tar`

### file list

```diff
@@ -1,23 +1,23 @@
-drwxr-xr-x   0 desu      (1000) desu      (1000)        0 2023-07-10 20:51:11.844944 zlibrary-0.2.4/
--rw-r--r--   0 desu      (1000) desu      (1000)    35149 2023-07-10 20:08:05.000000 zlibrary-0.2.4/LICENSE
--rw-r--r--   0 desu      (1000) desu      (1000)     6699 2023-07-10 20:51:11.844944 zlibrary-0.2.4/PKG-INFO
--rw-r--r--   0 desu      (1000) desu      (1000)     6187 2023-07-10 20:08:05.000000 zlibrary-0.2.4/README.md
--rw-r--r--   0 desu      (1000) desu      (1000)      104 2023-07-10 20:08:05.000000 zlibrary-0.2.4/pyproject.toml
--rw-r--r--   0 desu      (1000) desu      (1000)      759 2023-07-10 20:51:11.844944 zlibrary-0.2.4/setup.cfg
-drwxr-xr-x   0 desu      (1000) desu      (1000)        0 2023-07-10 20:51:11.844944 zlibrary-0.2.4/src/
-drwxr-xr-x   0 desu      (1000) desu      (1000)        0 2023-07-10 20:51:11.844944 zlibrary-0.2.4/src/zlibrary/
--rw-r--r--   0 desu      (1000) desu      (1000)       84 2023-07-10 20:08:05.000000 zlibrary-0.2.4/src/zlibrary/__init__.py
--rw-r--r--   0 desu      (1000) desu      (1000)    19454 2023-07-10 20:09:20.000000 zlibrary-0.2.4/src/zlibrary/abs.py
--rw-r--r--   0 desu      (1000) desu      (1000)      852 2023-07-10 20:08:05.000000 zlibrary-0.2.4/src/zlibrary/booklists.py
--rw-r--r--   0 desu      (1000) desu      (1000)     4945 2023-07-10 20:08:05.000000 zlibrary-0.2.4/src/zlibrary/const.py
--rw-r--r--   0 desu      (1000) desu      (1000)      769 2023-07-10 20:08:05.000000 zlibrary-0.2.4/src/zlibrary/exception.py
--rw-r--r--   0 desu      (1000) desu      (1000)     7981 2023-07-10 20:26:50.000000 zlibrary-0.2.4/src/zlibrary/libasync.py
--rw-r--r--   0 desu      (1000) desu      (1000)       96 2023-07-10 20:08:05.000000 zlibrary-0.2.4/src/zlibrary/logger.py
--rw-r--r--   0 desu      (1000) desu      (1000)     2664 2023-07-10 20:08:05.000000 zlibrary-0.2.4/src/zlibrary/profile.py
--rw-r--r--   0 desu      (1000) desu      (1000)     2500 2023-07-10 20:08:05.000000 zlibrary-0.2.4/src/zlibrary/util.py
-drwxr-xr-x   0 desu      (1000) desu      (1000)        0 2023-07-10 20:51:11.844944 zlibrary-0.2.4/src/zlibrary.egg-info/
--rw-r--r--   0 desu      (1000) desu      (1000)     6699 2023-07-10 20:51:11.000000 zlibrary-0.2.4/src/zlibrary.egg-info/PKG-INFO
--rw-r--r--   0 desu      (1000) desu      (1000)      433 2023-07-10 20:51:11.000000 zlibrary-0.2.4/src/zlibrary.egg-info/SOURCES.txt
--rw-r--r--   0 desu      (1000) desu      (1000)        1 2023-07-10 20:51:11.000000 zlibrary-0.2.4/src/zlibrary.egg-info/dependency_links.txt
--rw-r--r--   0 desu      (1000) desu      (1000)       90 2023-07-10 20:51:11.000000 zlibrary-0.2.4/src/zlibrary.egg-info/requires.txt
--rw-r--r--   0 desu      (1000) desu      (1000)        9 2023-07-10 20:51:11.000000 zlibrary-0.2.4/src/zlibrary.egg-info/top_level.txt
+drwxr-xr-x   0 desu      (1000) desu      (1000)        0 2023-07-23 00:54:51.200324 zlibrary-0.2.5/
+-rw-r--r--   0 desu      (1000) desu      (1000)    35149 2023-07-21 14:40:47.000000 zlibrary-0.2.5/LICENSE
+-rw-r--r--   0 desu      (1000) desu      (1000)     6699 2023-07-23 00:54:51.200324 zlibrary-0.2.5/PKG-INFO
+-rw-r--r--   0 desu      (1000) desu      (1000)     6187 2023-07-21 14:40:47.000000 zlibrary-0.2.5/README.md
+-rw-r--r--   0 desu      (1000) desu      (1000)      104 2023-07-21 14:40:47.000000 zlibrary-0.2.5/pyproject.toml
+-rw-r--r--   0 desu      (1000) desu      (1000)      769 2023-07-23 00:54:51.200324 zlibrary-0.2.5/setup.cfg
+drwxr-xr-x   0 desu      (1000) desu      (1000)        0 2023-07-23 00:54:51.190324 zlibrary-0.2.5/src/
+drwxr-xr-x   0 desu      (1000) desu      (1000)        0 2023-07-23 00:54:51.200324 zlibrary-0.2.5/src/zlibrary/
+-rw-r--r--   0 desu      (1000) desu      (1000)       84 2023-07-21 14:40:47.000000 zlibrary-0.2.5/src/zlibrary/__init__.py
+-rw-r--r--   0 desu      (1000) desu      (1000)    19454 2023-07-21 14:40:47.000000 zlibrary-0.2.5/src/zlibrary/abs.py
+-rw-r--r--   0 desu      (1000) desu      (1000)      852 2023-07-21 14:40:47.000000 zlibrary-0.2.5/src/zlibrary/booklists.py
+-rw-r--r--   0 desu      (1000) desu      (1000)     4945 2023-07-21 14:40:47.000000 zlibrary-0.2.5/src/zlibrary/const.py
+-rw-r--r--   0 desu      (1000) desu      (1000)      769 2023-07-21 14:40:47.000000 zlibrary-0.2.5/src/zlibrary/exception.py
+-rw-r--r--   0 desu      (1000) desu      (1000)     7981 2023-07-21 14:40:47.000000 zlibrary-0.2.5/src/zlibrary/libasync.py
+-rw-r--r--   0 desu      (1000) desu      (1000)       96 2023-07-21 14:40:47.000000 zlibrary-0.2.5/src/zlibrary/logger.py
+-rw-r--r--   0 desu      (1000) desu      (1000)     2664 2023-07-21 14:40:47.000000 zlibrary-0.2.5/src/zlibrary/profile.py
+-rw-r--r--   0 desu      (1000) desu      (1000)     2500 2023-07-21 14:40:47.000000 zlibrary-0.2.5/src/zlibrary/util.py
+drwxr-xr-x   0 desu      (1000) desu      (1000)        0 2023-07-23 00:54:51.200324 zlibrary-0.2.5/src/zlibrary.egg-info/
+-rw-r--r--   0 desu      (1000) desu      (1000)     6699 2023-07-23 00:54:51.000000 zlibrary-0.2.5/src/zlibrary.egg-info/PKG-INFO
+-rw-r--r--   0 desu      (1000) desu      (1000)      433 2023-07-23 00:54:51.000000 zlibrary-0.2.5/src/zlibrary.egg-info/SOURCES.txt
+-rw-r--r--   0 desu      (1000) desu      (1000)        1 2023-07-23 00:54:51.000000 zlibrary-0.2.5/src/zlibrary.egg-info/dependency_links.txt
+-rw-r--r--   0 desu      (1000) desu      (1000)      100 2023-07-23 00:54:51.000000 zlibrary-0.2.5/src/zlibrary.egg-info/requires.txt
+-rw-r--r--   0 desu      (1000) desu      (1000)        9 2023-07-23 00:54:51.000000 zlibrary-0.2.5/src/zlibrary.egg-info/top_level.txt
```

### Comparing `zlibrary-0.2.4/LICENSE` & `zlibrary-0.2.5/LICENSE`

 * *Files identical despite different names*

### Comparing `zlibrary-0.2.4/PKG-INFO` & `zlibrary-0.2.5/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: zlibrary
-Version: 0.2.4
+Version: 0.2.5
 Summary: Unofficial Z-Library API
 Home-page: https://github.com/sertraline/zlibrary
 Author: Toshiro Iwa
 Author-email: iwa@acid.im
 Project-URL: Bug Tracker, https://github.com/sertraline/zlibrary/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU General Public License v3 (GPLv3)
```

### Comparing `zlibrary-0.2.4/README.md` & `zlibrary-0.2.5/README.md`

 * *Files identical despite different names*

### Comparing `zlibrary-0.2.4/setup.cfg` & `zlibrary-0.2.5/setup.cfg`

 * *Files 18% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = zlibrary
-version = 0.2.4
+version = 0.2.5
 author = Toshiro Iwa
 author_email = iwa@acid.im
 description = Unofficial Z-Library API
 long_description = file: README.md
 long_description_content_type = text/markdown
 url = https://github.com/sertraline/zlibrary
 project_urls = 
@@ -21,15 +21,15 @@
 python_requires = >=3.7
 install_requires = 
 	aiodns
 	aiohttp
 	aiohttp-socks
 	beautifulsoup4
 	bs4
-	cchardet
+	charset-normalizer
 	cffi
 	Brotli
 	lxml
 	ujson
 	idna
 	yarl
```

### Comparing `zlibrary-0.2.4/src/zlibrary/abs.py` & `zlibrary-0.2.5/src/zlibrary/abs.py`

 * *Files identical despite different names*

### Comparing `zlibrary-0.2.4/src/zlibrary/booklists.py` & `zlibrary-0.2.5/src/zlibrary/booklists.py`

 * *Files identical despite different names*

### Comparing `zlibrary-0.2.4/src/zlibrary/const.py` & `zlibrary-0.2.5/src/zlibrary/const.py`

 * *Files identical despite different names*

### Comparing `zlibrary-0.2.4/src/zlibrary/exception.py` & `zlibrary-0.2.5/src/zlibrary/exception.py`

 * *Files identical despite different names*

### Comparing `zlibrary-0.2.4/src/zlibrary/libasync.py` & `zlibrary-0.2.5/src/zlibrary/libasync.py`

 * *Files identical despite different names*

### Comparing `zlibrary-0.2.4/src/zlibrary/profile.py` & `zlibrary-0.2.5/src/zlibrary/profile.py`

 * *Files identical despite different names*

### Comparing `zlibrary-0.2.4/src/zlibrary/util.py` & `zlibrary-0.2.5/src/zlibrary/util.py`

 * *Files identical despite different names*

### Comparing `zlibrary-0.2.4/src/zlibrary.egg-info/PKG-INFO` & `zlibrary-0.2.5/src/zlibrary.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: zlibrary
-Version: 0.2.4
+Version: 0.2.5
 Summary: Unofficial Z-Library API
 Home-page: https://github.com/sertraline/zlibrary
 Author: Toshiro Iwa
 Author-email: iwa@acid.im
 Project-URL: Bug Tracker, https://github.com/sertraline/zlibrary/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU General Public License v3 (GPLv3)
```

