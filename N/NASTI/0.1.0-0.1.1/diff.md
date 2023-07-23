# Comparing `tmp/NASTI-0.1.0.tar.gz` & `tmp/NASTI-0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "NASTI-0.1.0.tar", last modified: Sun Jul 23 17:46:28 2023, max compression
+gzip compressed data, was "NASTI-0.1.1.tar", last modified: Sun Jul 23 18:20:31 2023, max compression
```

## Comparing `NASTI-0.1.0.tar` & `NASTI-0.1.1.tar`

### file list

```diff
@@ -1,27 +1,27 @@
-drwxr-xr-x   0 adamdrew  (1000) adamdrew  (1000)        0 2023-07-23 17:46:28.670265 NASTI-0.1.0/
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)    35149 2023-07-23 17:23:07.000000 NASTI-0.1.0/LICENSE
-drwxr-xr-x   0 adamdrew  (1000) adamdrew  (1000)        0 2023-07-23 17:46:28.668265 NASTI-0.1.0/NASTI.egg-info/
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     7512 2023-07-23 17:46:28.000000 NASTI-0.1.0/NASTI.egg-info/PKG-INFO
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)      452 2023-07-23 17:46:28.000000 NASTI-0.1.0/NASTI.egg-info/SOURCES.txt
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)        1 2023-07-23 17:46:28.000000 NASTI-0.1.0/NASTI.egg-info/dependency_links.txt
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)       27 2023-07-23 17:46:28.000000 NASTI-0.1.0/NASTI.egg-info/entry_points.txt
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)      992 2023-07-23 17:46:28.000000 NASTI-0.1.0/NASTI.egg-info/requires.txt
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)        6 2023-07-23 17:46:28.000000 NASTI-0.1.0/NASTI.egg-info/top_level.txt
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     7512 2023-07-23 17:46:28.670265 NASTI-0.1.0/PKG-INFO
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     6772 2023-07-23 17:17:03.000000 NASTI-0.1.0/README.md
-drwxr-xr-x   0 adamdrew  (1000) adamdrew  (1000)        0 2023-07-23 17:46:28.669265 NASTI-0.1.0/nasti/
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)        0 2023-07-22 16:17:53.000000 NASTI-0.1.0/nasti/__init__.py
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     1256 2023-07-23 12:54:01.000000 NASTI-0.1.0/nasti/cli.py
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     1048 2023-07-23 15:52:01.000000 NASTI-0.1.0/nasti/exceptions.py
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     4272 2023-07-23 16:09:18.000000 NASTI-0.1.0/nasti/mutation.py
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     3043 2023-07-23 12:55:39.000000 NASTI-0.1.0/nasti/nasti.py
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     2583 2023-07-23 15:49:29.000000 NASTI-0.1.0/nasti/nastifile.py
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     3200 2023-07-23 15:42:52.000000 NASTI-0.1.0/nasti/source_handlers.py
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     1940 2023-07-23 15:32:28.000000 NASTI-0.1.0/nasti/validation.py
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)       38 2023-07-23 17:46:28.670265 NASTI-0.1.0/setup.cfg
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)    10255 2023-07-23 17:46:25.000000 NASTI-0.1.0/setup.py
-drwxr-xr-x   0 adamdrew  (1000) adamdrew  (1000)        0 2023-07-23 17:46:28.669265 NASTI-0.1.0/tests/
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     4908 2023-07-23 16:17:51.000000 NASTI-0.1.0/tests/test_mutation.py
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     1726 2023-07-23 15:49:17.000000 NASTI-0.1.0/tests/test_nastifile.py
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     2660 2023-07-23 15:43:52.000000 NASTI-0.1.0/tests/test_source_handlers.py
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     1505 2023-07-23 15:34:43.000000 NASTI-0.1.0/tests/test_validation.py
+drwxr-xr-x   0 adamdrew  (1000) adamdrew  (1000)        0 2023-07-23 18:20:31.053265 NASTI-0.1.1/
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)    35149 2023-07-23 17:23:07.000000 NASTI-0.1.1/LICENSE
+drwxr-xr-x   0 adamdrew  (1000) adamdrew  (1000)        0 2023-07-23 18:20:31.052266 NASTI-0.1.1/NASTI.egg-info/
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     7237 2023-07-23 18:20:31.000000 NASTI-0.1.1/NASTI.egg-info/PKG-INFO
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)      441 2023-07-23 18:20:31.000000 NASTI-0.1.1/NASTI.egg-info/SOURCES.txt
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)        1 2023-07-23 18:20:31.000000 NASTI-0.1.1/NASTI.egg-info/dependency_links.txt
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)       12 2023-07-23 18:20:31.000000 NASTI-0.1.1/NASTI.egg-info/top_level.txt
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     7237 2023-07-23 18:20:31.053265 NASTI-0.1.1/PKG-INFO
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     6772 2023-07-23 17:17:03.000000 NASTI-0.1.1/README.md
+drwxr-xr-x   0 adamdrew  (1000) adamdrew  (1000)        0 2023-07-23 18:20:31.052266 NASTI-0.1.1/nasti/
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)        0 2023-07-22 16:17:53.000000 NASTI-0.1.1/nasti/__init__.py
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     1256 2023-07-23 12:54:01.000000 NASTI-0.1.1/nasti/cli.py
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     1048 2023-07-23 15:52:01.000000 NASTI-0.1.1/nasti/exceptions.py
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     4272 2023-07-23 16:09:18.000000 NASTI-0.1.1/nasti/mutation.py
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     3043 2023-07-23 12:55:39.000000 NASTI-0.1.1/nasti/nasti.py
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     2583 2023-07-23 15:49:29.000000 NASTI-0.1.1/nasti/nastifile.py
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     3200 2023-07-23 15:42:52.000000 NASTI-0.1.1/nasti/source_handlers.py
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     1940 2023-07-23 15:32:28.000000 NASTI-0.1.1/nasti/validation.py
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)      103 2023-07-23 18:18:02.000000 NASTI-0.1.1/pyproject.toml
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)      554 2023-07-23 18:20:31.053265 NASTI-0.1.1/setup.cfg
+drwxr-xr-x   0 adamdrew  (1000) adamdrew  (1000)        0 2023-07-23 18:20:31.052266 NASTI-0.1.1/tests/
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)      335 2023-07-23 13:21:15.000000 NASTI-0.1.1/tests/__init__.py
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     1330 2023-07-23 16:12:36.000000 NASTI-0.1.1/tests/mocks.py
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     4908 2023-07-23 16:17:51.000000 NASTI-0.1.1/tests/test_mutation.py
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     1726 2023-07-23 15:49:17.000000 NASTI-0.1.1/tests/test_nastifile.py
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     2660 2023-07-23 15:43:52.000000 NASTI-0.1.1/tests/test_source_handlers.py
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     1505 2023-07-23 15:34:43.000000 NASTI-0.1.1/tests/test_validation.py
```

### Comparing `NASTI-0.1.0/LICENSE` & `NASTI-0.1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `NASTI-0.1.0/NASTI.egg-info/PKG-INFO` & `NASTI-0.1.1/NASTI.egg-info/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,25 +1,19 @@
 Metadata-Version: 2.1
 Name: NASTI
-Version: 0.1.0
-Summary: NASTI is A Strange Templating Implementation
+Version: 0.1.1
+Summary: NASTI is Not A Starndard Templating Implementation
 Home-page: https://github.com/adamrdrew/nasti
 Author: Adam Drew
 Author-email: adamrdrew@live.com
-Project-URL: Bug Reports, https://github.com/adamrdrew/nasti/issues
-Project-URL: Source, https://github.com/adamrdrew/nasti/
-Keywords: template project-template
-Classifier: Development Status :: 4 - Beta
-Classifier: Intended Audience :: Developers
-Classifier: Topic :: Software Development :: Build Tools
+Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU General Public License v3 (GPLv3)
-Classifier: Programming Language :: Python :: 3.11
-Requires-Python: >=3.11
+Classifier: Operating System :: OS Independent
+Requires-Python: >=3.10
 Description-Content-Type: text/markdown
-Provides-Extra: dev
 License-File: LICENSE
 
 [![Build Status](https://github.com/adamrdrew/nasti/actions/workflows/tests.yml/badge.svg?branch=master)](https://github.com/adamrdrew/nasti/actions)
 [![codecov](https://codecov.io/gh/adamrdrew/nasti/branch/master/graphs/badge.svg?branch=master)](https://codecov.io/github/adamrdrew/nasti?branch=master)
 
 # NASTI
 NASTI is A Strange Templating Implementation.
```

### Comparing `NASTI-0.1.0/PKG-INFO` & `NASTI-0.1.1/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,25 +1,19 @@
 Metadata-Version: 2.1
 Name: NASTI
-Version: 0.1.0
-Summary: NASTI is A Strange Templating Implementation
+Version: 0.1.1
+Summary: NASTI is Not A Starndard Templating Implementation
 Home-page: https://github.com/adamrdrew/nasti
 Author: Adam Drew
 Author-email: adamrdrew@live.com
-Project-URL: Bug Reports, https://github.com/adamrdrew/nasti/issues
-Project-URL: Source, https://github.com/adamrdrew/nasti/
-Keywords: template project-template
-Classifier: Development Status :: 4 - Beta
-Classifier: Intended Audience :: Developers
-Classifier: Topic :: Software Development :: Build Tools
+Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU General Public License v3 (GPLv3)
-Classifier: Programming Language :: Python :: 3.11
-Requires-Python: >=3.11
+Classifier: Operating System :: OS Independent
+Requires-Python: >=3.10
 Description-Content-Type: text/markdown
-Provides-Extra: dev
 License-File: LICENSE
 
 [![Build Status](https://github.com/adamrdrew/nasti/actions/workflows/tests.yml/badge.svg?branch=master)](https://github.com/adamrdrew/nasti/actions)
 [![codecov](https://codecov.io/gh/adamrdrew/nasti/branch/master/graphs/badge.svg?branch=master)](https://codecov.io/github/adamrdrew/nasti?branch=master)
 
 # NASTI
 NASTI is A Strange Templating Implementation.
```

### Comparing `NASTI-0.1.0/README.md` & `NASTI-0.1.1/README.md`

 * *Files identical despite different names*

### Comparing `NASTI-0.1.0/nasti/cli.py` & `NASTI-0.1.1/nasti/cli.py`

 * *Files identical despite different names*

### Comparing `NASTI-0.1.0/nasti/exceptions.py` & `NASTI-0.1.1/nasti/exceptions.py`

 * *Files identical despite different names*

### Comparing `NASTI-0.1.0/nasti/mutation.py` & `NASTI-0.1.1/nasti/mutation.py`

 * *Files identical despite different names*

### Comparing `NASTI-0.1.0/nasti/nasti.py` & `NASTI-0.1.1/nasti/nasti.py`

 * *Files identical despite different names*

### Comparing `NASTI-0.1.0/nasti/nastifile.py` & `NASTI-0.1.1/nasti/nastifile.py`

 * *Files identical despite different names*

### Comparing `NASTI-0.1.0/nasti/source_handlers.py` & `NASTI-0.1.1/nasti/source_handlers.py`

 * *Files identical despite different names*

### Comparing `NASTI-0.1.0/nasti/validation.py` & `NASTI-0.1.1/nasti/validation.py`

 * *Files identical despite different names*

### Comparing `NASTI-0.1.0/tests/test_mutation.py` & `NASTI-0.1.1/tests/test_mutation.py`

 * *Files identical despite different names*

### Comparing `NASTI-0.1.0/tests/test_nastifile.py` & `NASTI-0.1.1/tests/test_nastifile.py`

 * *Files identical despite different names*

### Comparing `NASTI-0.1.0/tests/test_source_handlers.py` & `NASTI-0.1.1/tests/test_source_handlers.py`

 * *Files identical despite different names*

### Comparing `NASTI-0.1.0/tests/test_validation.py` & `NASTI-0.1.1/tests/test_validation.py`

 * *Files identical despite different names*

