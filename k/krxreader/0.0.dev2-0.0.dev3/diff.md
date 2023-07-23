# Comparing `tmp/krxreader-0.0.dev2.tar.gz` & `tmp/krxreader-0.0.dev3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "krxreader-0.0.dev2.tar", last modified: Sun May 21 08:16:18 2023, max compression
+gzip compressed data, was "krxreader-0.0.dev3.tar", last modified: Sun Jul 23 06:57:52 2023, max compression
```

## Comparing `krxreader-0.0.dev2.tar` & `krxreader-0.0.dev3.tar`

### file list

```diff
@@ -1,28 +1,29 @@
-drwxr-xr-x   0 gunhoon    (501) staff       (20)        0 2023-05-21 08:16:18.442472 krxreader-0.0.dev2/
--rw-r--r--   0 gunhoon    (501) staff       (20)     1068 2023-05-21 08:12:21.000000 krxreader-0.0.dev2/LICENSE
--rw-r--r--   0 gunhoon    (501) staff       (20)     1939 2023-05-21 08:16:18.441879 krxreader-0.0.dev2/PKG-INFO
--rw-r--r--   0 gunhoon    (501) staff       (20)      120 2023-05-21 08:12:21.000000 krxreader-0.0.dev2/README.md
--rw-r--r--   0 gunhoon    (501) staff       (20)      714 2023-05-21 08:12:21.000000 krxreader-0.0.dev2/pyproject.toml
--rw-r--r--   0 gunhoon    (501) staff       (20)       38 2023-05-21 08:16:18.442654 krxreader-0.0.dev2/setup.cfg
-drwxr-xr-x   0 gunhoon    (501) staff       (20)        0 2023-05-21 08:16:18.430667 krxreader-0.0.dev2/src/
-drwxr-xr-x   0 gunhoon    (501) staff       (20)        0 2023-05-21 08:16:18.435818 krxreader-0.0.dev2/src/krxreader/
--rw-r--r--   0 gunhoon    (501) staff       (20)        0 2023-05-21 08:12:21.000000 krxreader-0.0.dev2/src/krxreader/__init__.py
--rw-r--r--   0 gunhoon    (501) staff       (20)      628 2023-05-21 08:12:21.000000 krxreader-0.0.dev2/src/krxreader/_calendar.py
--rw-r--r--   0 gunhoon    (501) staff       (20)     1094 2023-05-21 08:12:21.000000 krxreader-0.0.dev2/src/krxreader/base.py
--rw-r--r--   0 gunhoon    (501) staff       (20)     1259 2023-05-21 08:12:21.000000 krxreader-0.0.dev2/src/krxreader/bond.py
--rw-r--r--   0 gunhoon    (501) staff       (20)      627 2023-05-21 08:12:21.000000 krxreader-0.0.dev2/src/krxreader/fetch.py
--rw-r--r--   0 gunhoon    (501) staff       (20)     2129 2023-05-21 08:12:21.000000 krxreader-0.0.dev2/src/krxreader/index.py
--rw-r--r--   0 gunhoon    (501) staff       (20)       29 2023-05-21 08:12:21.000000 krxreader-0.0.dev2/src/krxreader/sample.py
--rw-r--r--   0 gunhoon    (501) staff       (20)     1232 2023-05-21 08:12:21.000000 krxreader-0.0.dev2/src/krxreader/stock.py
-drwxr-xr-x   0 gunhoon    (501) staff       (20)        0 2023-05-21 08:16:18.438326 krxreader-0.0.dev2/src/krxreader.egg-info/
--rw-r--r--   0 gunhoon    (501) staff       (20)     1939 2023-05-21 08:16:18.000000 krxreader-0.0.dev2/src/krxreader.egg-info/PKG-INFO
--rw-r--r--   0 gunhoon    (501) staff       (20)      506 2023-05-21 08:16:18.000000 krxreader-0.0.dev2/src/krxreader.egg-info/SOURCES.txt
--rw-r--r--   0 gunhoon    (501) staff       (20)        1 2023-05-21 08:16:18.000000 krxreader-0.0.dev2/src/krxreader.egg-info/dependency_links.txt
--rw-r--r--   0 gunhoon    (501) staff       (20)        9 2023-05-21 08:16:18.000000 krxreader-0.0.dev2/src/krxreader.egg-info/requires.txt
--rw-r--r--   0 gunhoon    (501) staff       (20)       10 2023-05-21 08:16:18.000000 krxreader-0.0.dev2/src/krxreader.egg-info/top_level.txt
-drwxr-xr-x   0 gunhoon    (501) staff       (20)        0 2023-05-21 08:16:18.441142 krxreader-0.0.dev2/tests/
--rw-r--r--   0 gunhoon    (501) staff       (20)      827 2023-05-21 08:12:21.000000 krxreader-0.0.dev2/tests/test_base.py
--rw-r--r--   0 gunhoon    (501) staff       (20)      923 2023-05-21 08:12:21.000000 krxreader-0.0.dev2/tests/test_fetch.py
--rw-r--r--   0 gunhoon    (501) staff       (20)      413 2023-05-21 08:12:21.000000 krxreader-0.0.dev2/tests/test_index.py
--rw-r--r--   0 gunhoon    (501) staff       (20)       74 2023-05-21 08:12:21.000000 krxreader-0.0.dev2/tests/test_sample.py
--rw-r--r--   0 gunhoon    (501) staff       (20)      912 2023-05-21 08:12:21.000000 krxreader-0.0.dev2/tests/test_stock.py
+drwxr-xr-x   0 gunhoon    (501) staff       (20)        0 2023-07-23 06:57:52.124338 krxreader-0.0.dev3/
+-rw-r--r--   0 gunhoon    (501) staff       (20)     1068 2023-07-23 06:55:55.000000 krxreader-0.0.dev3/LICENSE
+-rw-r--r--   0 gunhoon    (501) staff       (20)     1939 2023-07-23 06:57:52.123674 krxreader-0.0.dev3/PKG-INFO
+-rw-r--r--   0 gunhoon    (501) staff       (20)      120 2023-07-23 06:55:55.000000 krxreader-0.0.dev3/README.md
+-rw-r--r--   0 gunhoon    (501) staff       (20)      714 2023-07-23 06:55:55.000000 krxreader-0.0.dev3/pyproject.toml
+-rw-r--r--   0 gunhoon    (501) staff       (20)       38 2023-07-23 06:57:52.124562 krxreader-0.0.dev3/setup.cfg
+drwxr-xr-x   0 gunhoon    (501) staff       (20)        0 2023-07-23 06:57:52.112168 krxreader-0.0.dev3/src/
+drwxr-xr-x   0 gunhoon    (501) staff       (20)        0 2023-07-23 06:57:52.117151 krxreader-0.0.dev3/src/krxreader/
+-rw-r--r--   0 gunhoon    (501) staff       (20)        0 2023-07-23 06:55:55.000000 krxreader-0.0.dev3/src/krxreader/__init__.py
+-rw-r--r--   0 gunhoon    (501) staff       (20)     2755 2023-07-23 06:55:55.000000 krxreader-0.0.dev3/src/krxreader/base.py
+-rw-r--r--   0 gunhoon    (501) staff       (20)     1259 2023-07-23 06:55:55.000000 krxreader-0.0.dev3/src/krxreader/bond.py
+-rw-r--r--   0 gunhoon    (501) staff       (20)     1961 2023-07-23 06:55:55.000000 krxreader-0.0.dev3/src/krxreader/calendar.py
+-rw-r--r--   0 gunhoon    (501) staff       (20)     2067 2023-07-23 06:55:55.000000 krxreader-0.0.dev3/src/krxreader/chrome.py
+-rw-r--r--   0 gunhoon    (501) staff       (20)     1914 2023-07-23 06:55:55.000000 krxreader-0.0.dev3/src/krxreader/fetch.py
+-rw-r--r--   0 gunhoon    (501) staff       (20)     4413 2023-07-23 06:55:55.000000 krxreader-0.0.dev3/src/krxreader/index.py
+-rw-r--r--   0 gunhoon    (501) staff       (20)     3648 2023-07-23 06:55:55.000000 krxreader-0.0.dev3/src/krxreader/stock.py
+drwxr-xr-x   0 gunhoon    (501) staff       (20)        0 2023-07-23 06:57:52.119737 krxreader-0.0.dev3/src/krxreader.egg-info/
+-rw-r--r--   0 gunhoon    (501) staff       (20)     1939 2023-07-23 06:57:52.000000 krxreader-0.0.dev3/src/krxreader.egg-info/PKG-INFO
+-rw-r--r--   0 gunhoon    (501) staff       (20)      528 2023-07-23 06:57:52.000000 krxreader-0.0.dev3/src/krxreader.egg-info/SOURCES.txt
+-rw-r--r--   0 gunhoon    (501) staff       (20)        1 2023-07-23 06:57:52.000000 krxreader-0.0.dev3/src/krxreader.egg-info/dependency_links.txt
+-rw-r--r--   0 gunhoon    (501) staff       (20)        9 2023-07-23 06:57:52.000000 krxreader-0.0.dev3/src/krxreader.egg-info/requires.txt
+-rw-r--r--   0 gunhoon    (501) staff       (20)       10 2023-07-23 06:57:52.000000 krxreader-0.0.dev3/src/krxreader.egg-info/top_level.txt
+drwxr-xr-x   0 gunhoon    (501) staff       (20)        0 2023-07-23 06:57:52.122875 krxreader-0.0.dev3/tests/
+-rw-r--r--   0 gunhoon    (501) staff       (20)     2499 2023-07-23 06:55:55.000000 krxreader-0.0.dev3/tests/test_base.py
+-rw-r--r--   0 gunhoon    (501) staff       (20)     5702 2023-07-23 06:55:55.000000 krxreader-0.0.dev3/tests/test_calendar.py
+-rw-r--r--   0 gunhoon    (501) staff       (20)     2060 2023-07-23 06:55:55.000000 krxreader-0.0.dev3/tests/test_chrome.py
+-rw-r--r--   0 gunhoon    (501) staff       (20)     1972 2023-07-23 06:55:55.000000 krxreader-0.0.dev3/tests/test_fetch.py
+-rw-r--r--   0 gunhoon    (501) staff       (20)     3217 2023-07-23 06:55:55.000000 krxreader-0.0.dev3/tests/test_index.py
+-rw-r--r--   0 gunhoon    (501) staff       (20)     2173 2023-07-23 06:55:55.000000 krxreader-0.0.dev3/tests/test_stock.py
```

### Comparing `krxreader-0.0.dev2/LICENSE` & `krxreader-0.0.dev3/LICENSE`

 * *Files identical despite different names*

### Comparing `krxreader-0.0.dev2/PKG-INFO` & `krxreader-0.0.dev3/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: krxreader
-Version: 0.0.dev2
+Version: 0.0.dev3
 Summary: KRXReader is a library for scraping financial data from the KRX(Korea Exchange) Market Data System.
 Author-email: Gunhoon Lee <gunhoon@gmail.com>
 License: MIT License
         
         Copyright (c) 2022 Gunhoon Lee
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
```

### Comparing `krxreader-0.0.dev2/pyproject.toml` & `krxreader-0.0.dev3/pyproject.toml`

 * *Files 24% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [project]
 name = "krxreader"
-version = "0.0.dev2"
+version = "0.0.dev3"
 description = "KRXReader is a library for scraping financial data from the KRX(Korea Exchange) Market Data System."
 readme = "README.md"
 requires-python = ">=3.7"
 license = {file = "LICENSE"}
 authors = [
     {name = "Gunhoon Lee", email = "gunhoon@gmail.com"}
 ]
```

### Comparing `krxreader-0.0.dev2/src/krxreader/bond.py` & `krxreader-0.0.dev3/src/krxreader/bond.py`

 * *Files identical despite different names*

### Comparing `krxreader-0.0.dev2/src/krxreader.egg-info/PKG-INFO` & `krxreader-0.0.dev3/src/krxreader.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: krxreader
-Version: 0.0.dev2
+Version: 0.0.dev3
 Summary: KRXReader is a library for scraping financial data from the KRX(Korea Exchange) Market Data System.
 Author-email: Gunhoon Lee <gunhoon@gmail.com>
 License: MIT License
         
         Copyright (c) 2022 Gunhoon Lee
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
```

