# Comparing `tmp/pyassorted-0.7.5.tar.gz` & `tmp/pyassorted-0.7.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyassorted-0.7.5.tar", max compression
+gzip compressed data, was "pyassorted-0.7.6.tar", max compression
```

## Comparing `pyassorted-0.7.5.tar` & `pyassorted-0.7.6.tar`

### file list

```diff
@@ -1,30 +1,30 @@
--rw-r--r--   0        0        0     1066 2023-02-15 09:16:45.010069 pyassorted-0.7.5/LICENSE
--rw-r--r--   0        0        0     6993 2023-05-27 10:25:12.261799 pyassorted-0.7.5/README.md
--rw-r--r--   0        0        0       52 2023-07-14 09:33:12.416992 pyassorted-0.7.5/pyassorted/__init__.py
--rw-r--r--   0        0        0      115 2023-07-14 09:33:12.449633 pyassorted-0.7.5/pyassorted/asyncio/__init__.py
--rw-r--r--   0        0        0     1349 2023-07-14 09:33:12.453353 pyassorted-0.7.5/pyassorted/asyncio/executor.py
--rw-r--r--   0        0        0     2943 2023-07-14 09:33:12.448926 pyassorted-0.7.5/pyassorted/asyncio/io.py
--rw-r--r--   0        0        0     1017 2023-07-14 09:33:12.451637 pyassorted-0.7.5/pyassorted/asyncio/utils.py
--rw-r--r--   0        0        0       60 2023-07-14 09:33:12.424129 pyassorted-0.7.5/pyassorted/cache/__init__.py
--rw-r--r--   0        0        0     8108 2023-07-14 09:33:12.423115 pyassorted-0.7.5/pyassorted/cache/cache.py
--rw-r--r--   0        0        0        0 2023-05-15 11:57:33.581794 pyassorted-0.7.5/pyassorted/collections/__init__.py
--rw-r--r--   0        0        0     4047 2023-07-14 09:33:12.445122 pyassorted-0.7.5/pyassorted/collections/sqlitedict.py
--rw-r--r--   0        0        0      147 2023-07-14 09:33:12.427231 pyassorted-0.7.5/pyassorted/datetime/__init__.py
--rw-r--r--   0        0        0     1053 2023-07-14 09:33:12.428569 pyassorted-0.7.5/pyassorted/datetime/datetime.py
--rw-r--r--   0        0        0     2013 2023-05-15 11:57:33.582972 pyassorted-0.7.5/pyassorted/datetime/timer.py
--rw-r--r--   0        0        0        0 2023-06-12 12:04:26.629790 pyassorted-0.7.5/pyassorted/encrypt/__init__.py
--rw-r--r--   0        0        0     2257 2023-07-07 10:20:46.735970 pyassorted-0.7.5/pyassorted/encrypt/io.py
--rw-r--r--   0        0        0       54 2023-07-14 09:50:51.578045 pyassorted-0.7.5/pyassorted/hash/__init__.py
--rw-r--r--   0        0        0      403 2023-07-14 09:50:30.931630 pyassorted-0.7.5/pyassorted/hash/_string.py
--rw-r--r--   0        0        0     2602 2023-07-14 09:33:12.434006 pyassorted-0.7.5/pyassorted/io/__init__.py
--rw-r--r--   0        0        0     2364 2023-07-14 09:33:12.435706 pyassorted-0.7.5/pyassorted/io/watch.py
--rw-r--r--   0        0        0       55 2023-07-14 09:33:12.437117 pyassorted-0.7.5/pyassorted/lock/__init__.py
--rw-r--r--   0        0        0     4191 2023-04-01 13:44:09.335570 pyassorted-0.7.5/pyassorted/lock/filelock.py
--rw-r--r--   0        0        0        0 2023-07-07 10:23:45.350340 pyassorted-0.7.5/pyassorted/standard/__init__.py
--rw-r--r--   0        0        0     2788 2023-07-07 10:57:46.398428 pyassorted-0.7.5/pyassorted/standard/language_code.py
--rw-r--r--   0        0        0      129 2023-07-14 09:33:12.441354 pyassorted-0.7.5/pyassorted/string/__init__.py
--rw-r--r--   0        0        0      269 2023-06-08 14:18:59.300447 pyassorted-0.7.5/pyassorted/string/rand.py
--rw-r--r--   0        0        0     1924 2023-06-06 09:03:20.787667 pyassorted-0.7.5/pyassorted/string/replace.py
--rw-r--r--   0        0        0       18 2023-07-14 09:54:22.732319 pyassorted-0.7.5/pyassorted/version.py
--rw-r--r--   0        0        0      558 2023-07-14 09:54:16.130389 pyassorted-0.7.5/pyproject.toml
--rw-r--r--   0        0        0     7597 1970-01-01 00:00:00.000000 pyassorted-0.7.5/PKG-INFO
+-rw-r--r--   0        0        0     1066 2023-02-15 09:16:45.010069 pyassorted-0.7.6/LICENSE
+-rw-r--r--   0        0        0     7120 2023-07-23 12:23:17.220118 pyassorted-0.7.6/README.md
+-rw-r--r--   0        0        0       52 2023-07-14 09:33:12.416992 pyassorted-0.7.6/pyassorted/__init__.py
+-rw-r--r--   0        0        0      115 2023-07-14 09:33:12.449633 pyassorted-0.7.6/pyassorted/asyncio/__init__.py
+-rw-r--r--   0        0        0     1349 2023-07-14 09:33:12.453353 pyassorted-0.7.6/pyassorted/asyncio/executor.py
+-rw-r--r--   0        0        0     2943 2023-07-14 09:33:12.448926 pyassorted-0.7.6/pyassorted/asyncio/io.py
+-rw-r--r--   0        0        0     1017 2023-07-14 09:33:12.451637 pyassorted-0.7.6/pyassorted/asyncio/utils.py
+-rw-r--r--   0        0        0       60 2023-07-14 09:33:12.424129 pyassorted-0.7.6/pyassorted/cache/__init__.py
+-rw-r--r--   0        0        0     8108 2023-07-14 09:33:12.423115 pyassorted-0.7.6/pyassorted/cache/cache.py
+-rw-r--r--   0        0        0        0 2023-05-15 11:57:33.581794 pyassorted-0.7.6/pyassorted/collections/__init__.py
+-rw-r--r--   0        0        0     4047 2023-07-14 09:33:12.445122 pyassorted-0.7.6/pyassorted/collections/sqlitedict.py
+-rw-r--r--   0        0        0      147 2023-07-14 09:33:12.427231 pyassorted-0.7.6/pyassorted/datetime/__init__.py
+-rw-r--r--   0        0        0     1053 2023-07-14 09:33:12.428569 pyassorted-0.7.6/pyassorted/datetime/datetime.py
+-rw-r--r--   0        0        0     2013 2023-05-15 11:57:33.582972 pyassorted-0.7.6/pyassorted/datetime/timer.py
+-rw-r--r--   0        0        0        0 2023-06-12 12:04:26.629790 pyassorted-0.7.6/pyassorted/encrypt/__init__.py
+-rw-r--r--   0        0        0     2257 2023-07-07 10:20:46.735970 pyassorted-0.7.6/pyassorted/encrypt/io.py
+-rw-r--r--   0        0        0       54 2023-07-14 09:50:51.578045 pyassorted-0.7.6/pyassorted/hash/__init__.py
+-rw-r--r--   0        0        0      403 2023-07-14 09:50:30.931630 pyassorted-0.7.6/pyassorted/hash/_string.py
+-rw-r--r--   0        0        0     2602 2023-07-14 09:33:12.434006 pyassorted-0.7.6/pyassorted/io/__init__.py
+-rw-r--r--   0        0        0     2364 2023-07-14 09:33:12.435706 pyassorted-0.7.6/pyassorted/io/watch.py
+-rw-r--r--   0        0        0       55 2023-07-14 09:33:12.437117 pyassorted-0.7.6/pyassorted/lock/__init__.py
+-rw-r--r--   0        0        0     4191 2023-04-01 13:44:09.335570 pyassorted-0.7.6/pyassorted/lock/filelock.py
+-rw-r--r--   0        0        0        0 2023-07-07 10:23:45.350340 pyassorted-0.7.6/pyassorted/standard/__init__.py
+-rw-r--r--   0        0        0     2788 2023-07-07 10:57:46.398428 pyassorted-0.7.6/pyassorted/standard/language_code.py
+-rw-r--r--   0        0        0      129 2023-07-14 09:33:12.441354 pyassorted-0.7.6/pyassorted/string/__init__.py
+-rw-r--r--   0        0        0      269 2023-06-08 14:18:59.300447 pyassorted-0.7.6/pyassorted/string/rand.py
+-rw-r--r--   0        0        0     1924 2023-06-06 09:03:20.787667 pyassorted-0.7.6/pyassorted/string/replace.py
+-rw-r--r--   0        0        0       18 2023-07-23 12:27:55.366646 pyassorted-0.7.6/pyassorted/version.py
+-rw-r--r--   0        0        0      558 2023-07-23 12:27:26.253912 pyassorted-0.7.6/pyproject.toml
+-rw-r--r--   0        0        0     7774 1970-01-01 00:00:00.000000 pyassorted-0.7.6/PKG-INFO
```

### Comparing `pyassorted-0.7.5/LICENSE` & `pyassorted-0.7.6/LICENSE`

 * *Files identical despite different names*

### Comparing `pyassorted-0.7.5/README.md` & `pyassorted-0.7.6/README.md`

 * *Files 4% similar despite different names*

```diff
@@ -1,8 +1,9 @@
 # pyassorted #
+[![CircleCI](https://circleci.com/gh/dockhardman/pyassorted.svg?style=shield)](https://circleci.com/gh/dockhardman/pyassorted)
 
 A library has assorted utils in Pure-Python. There are 3 principles:
 
 1. Light-weight
 2. No dependencies
 3. Pythonic usage.
```

### Comparing `pyassorted-0.7.5/pyassorted/asyncio/executor.py` & `pyassorted-0.7.6/pyassorted/asyncio/executor.py`

 * *Files identical despite different names*

### Comparing `pyassorted-0.7.5/pyassorted/asyncio/io.py` & `pyassorted-0.7.6/pyassorted/asyncio/io.py`

 * *Files identical despite different names*

### Comparing `pyassorted-0.7.5/pyassorted/asyncio/utils.py` & `pyassorted-0.7.6/pyassorted/asyncio/utils.py`

 * *Files identical despite different names*

### Comparing `pyassorted-0.7.5/pyassorted/cache/cache.py` & `pyassorted-0.7.6/pyassorted/cache/cache.py`

 * *Files identical despite different names*

### Comparing `pyassorted-0.7.5/pyassorted/collections/sqlitedict.py` & `pyassorted-0.7.6/pyassorted/collections/sqlitedict.py`

 * *Files identical despite different names*

### Comparing `pyassorted-0.7.5/pyassorted/datetime/datetime.py` & `pyassorted-0.7.6/pyassorted/datetime/datetime.py`

 * *Files identical despite different names*

### Comparing `pyassorted-0.7.5/pyassorted/datetime/timer.py` & `pyassorted-0.7.6/pyassorted/datetime/timer.py`

 * *Files identical despite different names*

### Comparing `pyassorted-0.7.5/pyassorted/encrypt/io.py` & `pyassorted-0.7.6/pyassorted/encrypt/io.py`

 * *Files identical despite different names*

### Comparing `pyassorted-0.7.5/pyassorted/io/__init__.py` & `pyassorted-0.7.6/pyassorted/io/__init__.py`

 * *Files identical despite different names*

### Comparing `pyassorted-0.7.5/pyassorted/io/watch.py` & `pyassorted-0.7.6/pyassorted/io/watch.py`

 * *Files identical despite different names*

### Comparing `pyassorted-0.7.5/pyassorted/lock/filelock.py` & `pyassorted-0.7.6/pyassorted/lock/filelock.py`

 * *Files identical despite different names*

### Comparing `pyassorted-0.7.5/pyassorted/standard/language_code.py` & `pyassorted-0.7.6/pyassorted/standard/language_code.py`

 * *Files identical despite different names*

### Comparing `pyassorted-0.7.5/pyassorted/string/replace.py` & `pyassorted-0.7.6/pyassorted/string/replace.py`

 * *Files identical despite different names*

### Comparing `pyassorted-0.7.5/pyproject.toml` & `pyassorted-0.7.6/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,17 +1,17 @@
 [tool.poetry]
 name = "pyassorted"
-version = "0.7.5"
+version = "0.7.6"
 description = "A library has light-weight assorted utils in Prue-Python."
 authors = ["Allen Chou <f1470891079@gmail.com>"]
 license = "MIT"
 readme = "README.md"
 
 [tool.poetry.dependencies]
-python = ">=3.7.1, <4.0.0"
+python = ">=3.7.0, <4.0.0"
 rich = "*"
 pytz = "*"
 
 [tool.poetry.group.dev.dependencies]
 black = "*"
 flake8 = "*"
 flake9 = "*"
```

### Comparing `pyassorted-0.7.5/PKG-INFO` & `pyassorted-0.7.6/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,26 +1,28 @@
 Metadata-Version: 2.1
 Name: pyassorted
-Version: 0.7.5
+Version: 0.7.6
 Summary: A library has light-weight assorted utils in Prue-Python.
 License: MIT
 Author: Allen Chou
 Author-email: f1470891079@gmail.com
-Requires-Python: >=3.7.1,<4.0.0
+Requires-Python: >=3.7.0,<4.0.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
+Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Requires-Dist: pytz
 Requires-Dist: rich
 Description-Content-Type: text/markdown
 
 # pyassorted #
+[![CircleCI](https://circleci.com/gh/dockhardman/pyassorted.svg?style=shield)](https://circleci.com/gh/dockhardman/pyassorted)
 
 A library has assorted utils in Pure-Python. There are 3 principles:
 
 1. Light-weight
 2. No dependencies
 3. Pythonic usage.
```

