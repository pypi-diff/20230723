# Comparing `tmp/ktkkt-downloader-1.0.0.tar.gz` & `tmp/ktkkt-downloader-1.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ktkkt-downloader-1.0.0.tar", last modified: Sun Jul 23 00:39:18 2023, max compression
+gzip compressed data, was "ktkkt-downloader-1.0.1.tar", last modified: Sun Jul 23 01:25:47 2023, max compression
```

## Comparing `ktkkt-downloader-1.0.0.tar` & `ktkkt-downloader-1.0.1.tar`

### file list

```diff
@@ -1,32 +1,33 @@
-drwxr-xr-x   0 rayyu      (501) staff       (20)        0 2023-07-23 00:39:18.472653 ktkkt-downloader-1.0.0/
--rw-r--r--   0 rayyu      (501) staff       (20)    35142 2023-07-22 15:37:02.000000 ktkkt-downloader-1.0.0/LICENSE.md
--rw-r--r--   0 rayyu      (501) staff       (20)     2583 2023-07-23 00:39:18.472801 ktkkt-downloader-1.0.0/PKG-INFO
--rw-r--r--   0 rayyu      (501) staff       (20)     2166 2023-07-23 00:38:48.000000 ktkkt-downloader-1.0.0/README.md
-drwxr-xr-x   0 rayyu      (501) staff       (20)        0 2023-07-23 00:39:18.466180 ktkkt-downloader-1.0.0/ktkkt_downloader/
--rw-r--r--   0 rayyu      (501) staff       (20)       46 2023-07-22 23:00:37.000000 ktkkt-downloader-1.0.0/ktkkt_downloader/__init__.py
-drwxr-xr-x   0 rayyu      (501) staff       (20)        0 2023-07-23 00:39:18.467734 ktkkt-downloader-1.0.0/ktkkt_downloader/downloader/
--rw-r--r--   0 rayyu      (501) staff       (20)       35 2023-07-22 22:59:52.000000 ktkkt-downloader-1.0.0/ktkkt_downloader/downloader/__init__.py
--rw-r--r--   0 rayyu      (501) staff       (20)      937 2023-07-22 23:16:31.000000 ktkkt-downloader-1.0.0/ktkkt_downloader/downloader/downloader.py
--rw-r--r--   0 rayyu      (501) staff       (20)     1202 2023-07-22 23:28:18.000000 ktkkt-downloader-1.0.0/ktkkt_downloader/ktkkt_downloader.py
-drwxr-xr-x   0 rayyu      (501) staff       (20)        0 2023-07-23 00:39:18.468438 ktkkt-downloader-1.0.0/ktkkt_downloader/logger/
--rw-r--r--   0 rayyu      (501) staff       (20)       27 2023-07-22 22:59:55.000000 ktkkt-downloader-1.0.0/ktkkt_downloader/logger/__init__.py
--rw-r--r--   0 rayyu      (501) staff       (20)      554 2023-07-22 22:08:24.000000 ktkkt-downloader-1.0.0/ktkkt_downloader/logger/logger.py
-drwxr-xr-x   0 rayyu      (501) staff       (20)        0 2023-07-23 00:39:18.469269 ktkkt-downloader-1.0.0/ktkkt_downloader/object/
--rw-r--r--   0 rayyu      (501) staff       (20)       29 2023-07-22 22:59:59.000000 ktkkt-downloader-1.0.0/ktkkt_downloader/object/__init__.py
--rw-r--r--   0 rayyu      (501) staff       (20)      232 2023-07-22 23:19:36.000000 ktkkt-downloader-1.0.0/ktkkt_downloader/object/episode.py
-drwxr-xr-x   0 rayyu      (501) staff       (20)        0 2023-07-23 00:39:18.471017 ktkkt-downloader-1.0.0/ktkkt_downloader/scraper/
--rw-r--r--   0 rayyu      (501) staff       (20)       71 2023-07-22 23:00:02.000000 ktkkt-downloader-1.0.0/ktkkt_downloader/scraper/__init__.py
--rw-r--r--   0 rayyu      (501) staff       (20)     2192 2023-07-22 23:22:20.000000 ktkkt-downloader-1.0.0/ktkkt_downloader/scraper/ktkkt_strategy.py
--rw-r--r--   0 rayyu      (501) staff       (20)      504 2023-07-22 23:18:19.000000 ktkkt-downloader-1.0.0/ktkkt_downloader/scraper/scraper.py
--rw-r--r--   0 rayyu      (501) staff       (20)      328 2023-07-22 23:18:04.000000 ktkkt-downloader-1.0.0/ktkkt_downloader/scraper/strategy.py
-drwxr-xr-x   0 rayyu      (501) staff       (20)        0 2023-07-23 00:39:18.467095 ktkkt-downloader-1.0.0/ktkkt_downloader.egg-info/
--rw-r--r--   0 rayyu      (501) staff       (20)     2583 2023-07-23 00:39:18.000000 ktkkt-downloader-1.0.0/ktkkt_downloader.egg-info/PKG-INFO
--rw-r--r--   0 rayyu      (501) staff       (20)      708 2023-07-23 00:39:18.000000 ktkkt-downloader-1.0.0/ktkkt_downloader.egg-info/SOURCES.txt
--rw-r--r--   0 rayyu      (501) staff       (20)        1 2023-07-23 00:39:18.000000 ktkkt-downloader-1.0.0/ktkkt_downloader.egg-info/dependency_links.txt
--rw-r--r--   0 rayyu      (501) staff       (20)       23 2023-07-23 00:39:18.000000 ktkkt-downloader-1.0.0/ktkkt_downloader.egg-info/top_level.txt
--rw-r--r--   0 rayyu      (501) staff       (20)       93 2023-07-23 00:00:10.000000 ktkkt-downloader-1.0.0/pyproject.toml
--rw-r--r--   0 rayyu      (501) staff       (20)      502 2023-07-23 00:39:18.473236 ktkkt-downloader-1.0.0/setup.cfg
-drwxr-xr-x   0 rayyu      (501) staff       (20)        0 2023-07-23 00:39:18.472212 ktkkt-downloader-1.0.0/tests/
--rw-r--r--   0 rayyu      (501) staff       (20)        0 2023-07-22 17:25:05.000000 ktkkt-downloader-1.0.0/tests/__init__.py
--rw-r--r--   0 rayyu      (501) staff       (20)     1096 2023-07-22 22:58:26.000000 ktkkt-downloader-1.0.0/tests/test_logger.py
--rw-r--r--   0 rayyu      (501) staff       (20)     1176 2023-07-22 23:23:19.000000 ktkkt-downloader-1.0.0/tests/test_scraper.py
+drwxr-xr-x   0 rayyu      (501) staff       (20)        0 2023-07-23 01:25:47.426435 ktkkt-downloader-1.0.1/
+-rw-r--r--   0 rayyu      (501) staff       (20)    35142 2023-07-22 15:37:02.000000 ktkkt-downloader-1.0.1/LICENSE.md
+-rw-r--r--   0 rayyu      (501) staff       (20)     2627 2023-07-23 01:25:47.426515 ktkkt-downloader-1.0.1/PKG-INFO
+-rw-r--r--   0 rayyu      (501) staff       (20)     2166 2023-07-23 00:38:48.000000 ktkkt-downloader-1.0.1/README.md
+drwxr-xr-x   0 rayyu      (501) staff       (20)        0 2023-07-23 01:25:47.420628 ktkkt-downloader-1.0.1/ktkkt_downloader/
+-rw-r--r--   0 rayyu      (501) staff       (20)       46 2023-07-22 23:00:37.000000 ktkkt-downloader-1.0.1/ktkkt_downloader/__init__.py
+drwxr-xr-x   0 rayyu      (501) staff       (20)        0 2023-07-23 01:25:47.421972 ktkkt-downloader-1.0.1/ktkkt_downloader/downloader/
+-rw-r--r--   0 rayyu      (501) staff       (20)       35 2023-07-22 22:59:52.000000 ktkkt-downloader-1.0.1/ktkkt_downloader/downloader/__init__.py
+-rw-r--r--   0 rayyu      (501) staff       (20)      937 2023-07-22 23:16:31.000000 ktkkt-downloader-1.0.1/ktkkt_downloader/downloader/downloader.py
+-rw-r--r--   0 rayyu      (501) staff       (20)     1202 2023-07-22 23:28:18.000000 ktkkt-downloader-1.0.1/ktkkt_downloader/ktkkt_downloader.py
+drwxr-xr-x   0 rayyu      (501) staff       (20)        0 2023-07-23 01:25:47.422562 ktkkt-downloader-1.0.1/ktkkt_downloader/logger/
+-rw-r--r--   0 rayyu      (501) staff       (20)       27 2023-07-22 22:59:55.000000 ktkkt-downloader-1.0.1/ktkkt_downloader/logger/__init__.py
+-rw-r--r--   0 rayyu      (501) staff       (20)      554 2023-07-22 22:08:24.000000 ktkkt-downloader-1.0.1/ktkkt_downloader/logger/logger.py
+drwxr-xr-x   0 rayyu      (501) staff       (20)        0 2023-07-23 01:25:47.423143 ktkkt-downloader-1.0.1/ktkkt_downloader/object/
+-rw-r--r--   0 rayyu      (501) staff       (20)       29 2023-07-22 22:59:59.000000 ktkkt-downloader-1.0.1/ktkkt_downloader/object/__init__.py
+-rw-r--r--   0 rayyu      (501) staff       (20)      232 2023-07-22 23:19:36.000000 ktkkt-downloader-1.0.1/ktkkt_downloader/object/episode.py
+drwxr-xr-x   0 rayyu      (501) staff       (20)        0 2023-07-23 01:25:47.424277 ktkkt-downloader-1.0.1/ktkkt_downloader/scraper/
+-rw-r--r--   0 rayyu      (501) staff       (20)       71 2023-07-22 23:00:02.000000 ktkkt-downloader-1.0.1/ktkkt_downloader/scraper/__init__.py
+-rw-r--r--   0 rayyu      (501) staff       (20)     2192 2023-07-22 23:22:20.000000 ktkkt-downloader-1.0.1/ktkkt_downloader/scraper/ktkkt_strategy.py
+-rw-r--r--   0 rayyu      (501) staff       (20)      504 2023-07-22 23:18:19.000000 ktkkt-downloader-1.0.1/ktkkt_downloader/scraper/scraper.py
+-rw-r--r--   0 rayyu      (501) staff       (20)      328 2023-07-22 23:18:04.000000 ktkkt-downloader-1.0.1/ktkkt_downloader/scraper/strategy.py
+drwxr-xr-x   0 rayyu      (501) staff       (20)        0 2023-07-23 01:25:47.421583 ktkkt-downloader-1.0.1/ktkkt_downloader.egg-info/
+-rw-r--r--   0 rayyu      (501) staff       (20)     2627 2023-07-23 01:25:47.000000 ktkkt-downloader-1.0.1/ktkkt_downloader.egg-info/PKG-INFO
+-rw-r--r--   0 rayyu      (501) staff       (20)      747 2023-07-23 01:25:47.000000 ktkkt-downloader-1.0.1/ktkkt_downloader.egg-info/SOURCES.txt
+-rw-r--r--   0 rayyu      (501) staff       (20)        1 2023-07-23 01:25:47.000000 ktkkt-downloader-1.0.1/ktkkt_downloader.egg-info/dependency_links.txt
+-rw-r--r--   0 rayyu      (501) staff       (20)       98 2023-07-23 01:25:47.000000 ktkkt-downloader-1.0.1/ktkkt_downloader.egg-info/requires.txt
+-rw-r--r--   0 rayyu      (501) staff       (20)       23 2023-07-23 01:25:47.000000 ktkkt-downloader-1.0.1/ktkkt_downloader.egg-info/top_level.txt
+-rw-r--r--   0 rayyu      (501) staff       (20)      624 2023-07-23 01:25:40.000000 ktkkt-downloader-1.0.1/pyproject.toml
+-rw-r--r--   0 rayyu      (501) staff       (20)      629 2023-07-23 01:25:47.426809 ktkkt-downloader-1.0.1/setup.cfg
+drwxr-xr-x   0 rayyu      (501) staff       (20)        0 2023-07-23 01:25:47.426159 ktkkt-downloader-1.0.1/tests/
+-rw-r--r--   0 rayyu      (501) staff       (20)        0 2023-07-22 17:25:05.000000 ktkkt-downloader-1.0.1/tests/__init__.py
+-rw-r--r--   0 rayyu      (501) staff       (20)     1096 2023-07-22 22:58:26.000000 ktkkt-downloader-1.0.1/tests/test_logger.py
+-rw-r--r--   0 rayyu      (501) staff       (20)     1176 2023-07-22 23:23:19.000000 ktkkt-downloader-1.0.1/tests/test_scraper.py
```

### Comparing `ktkkt-downloader-1.0.0/LICENSE.md` & `ktkkt-downloader-1.0.1/LICENSE.md`

 * *Files identical despite different names*

### Comparing `ktkkt-downloader-1.0.0/PKG-INFO` & `ktkkt-downloader-1.0.1/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,13 +1,14 @@
 Metadata-Version: 2.1
 Name: ktkkt-downloader
-Version: 1.0.0
+Version: 1.0.1
 Summary: downloader for videos on ktkkt.cc
-Home-page: https://github.com/r1y5i/ktkkt-downloader
-Author: r1y5i
+Home-page: https://github.com/rkwyu/ktkkt-downloader
+Author: rkwyu
+Author-email: rkwyu <ray.yukawai@gmail.com>
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 License-File: LICENSE.md
```

### Comparing `ktkkt-downloader-1.0.0/README.md` & `ktkkt-downloader-1.0.1/README.md`

 * *Files identical despite different names*

### Comparing `ktkkt-downloader-1.0.0/ktkkt_downloader/downloader/downloader.py` & `ktkkt-downloader-1.0.1/ktkkt_downloader/downloader/downloader.py`

 * *Files identical despite different names*

### Comparing `ktkkt-downloader-1.0.0/ktkkt_downloader/ktkkt_downloader.py` & `ktkkt-downloader-1.0.1/ktkkt_downloader/ktkkt_downloader.py`

 * *Files identical despite different names*

### Comparing `ktkkt-downloader-1.0.0/ktkkt_downloader/logger/logger.py` & `ktkkt-downloader-1.0.1/ktkkt_downloader/logger/logger.py`

 * *Files identical despite different names*

### Comparing `ktkkt-downloader-1.0.0/ktkkt_downloader/scraper/ktkkt_strategy.py` & `ktkkt-downloader-1.0.1/ktkkt_downloader/scraper/ktkkt_strategy.py`

 * *Files identical despite different names*

### Comparing `ktkkt-downloader-1.0.0/ktkkt_downloader.egg-info/PKG-INFO` & `ktkkt-downloader-1.0.1/ktkkt_downloader.egg-info/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,13 +1,14 @@
 Metadata-Version: 2.1
 Name: ktkkt-downloader
-Version: 1.0.0
+Version: 1.0.1
 Summary: downloader for videos on ktkkt.cc
-Home-page: https://github.com/r1y5i/ktkkt-downloader
-Author: r1y5i
+Home-page: https://github.com/rkwyu/ktkkt-downloader
+Author: rkwyu
+Author-email: rkwyu <ray.yukawai@gmail.com>
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 License-File: LICENSE.md
```

### Comparing `ktkkt-downloader-1.0.0/ktkkt_downloader.egg-info/SOURCES.txt` & `ktkkt-downloader-1.0.1/ktkkt_downloader.egg-info/SOURCES.txt`

 * *Files 13% similar despite different names*

```diff
@@ -3,14 +3,15 @@
 pyproject.toml
 setup.cfg
 ktkkt_downloader/__init__.py
 ktkkt_downloader/ktkkt_downloader.py
 ktkkt_downloader.egg-info/PKG-INFO
 ktkkt_downloader.egg-info/SOURCES.txt
 ktkkt_downloader.egg-info/dependency_links.txt
+ktkkt_downloader.egg-info/requires.txt
 ktkkt_downloader.egg-info/top_level.txt
 ktkkt_downloader/downloader/__init__.py
 ktkkt_downloader/downloader/downloader.py
 ktkkt_downloader/logger/__init__.py
 ktkkt_downloader/logger/logger.py
 ktkkt_downloader/object/__init__.py
 ktkkt_downloader/object/episode.py
```

### Comparing `ktkkt-downloader-1.0.0/tests/test_logger.py` & `ktkkt-downloader-1.0.1/tests/test_logger.py`

 * *Files identical despite different names*

### Comparing `ktkkt-downloader-1.0.0/tests/test_scraper.py` & `ktkkt-downloader-1.0.1/tests/test_scraper.py`

 * *Files identical despite different names*

