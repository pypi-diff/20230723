# Comparing `tmp/NASTI-0.1.1.tar.gz` & `tmp/NASTI-0.1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "NASTI-0.1.1.tar", last modified: Sun Jul 23 18:20:31 2023, max compression
+gzip compressed data, was "NASTI-0.1.2.tar", last modified: Sun Jul 23 18:25:25 2023, max compression
```

## Comparing `NASTI-0.1.1.tar` & `NASTI-0.1.2.tar`

### file list

```diff
@@ -1,27 +1,29 @@
-drwxr-xr-x   0 adamdrew  (1000) adamdrew  (1000)        0 2023-07-23 18:20:31.053265 NASTI-0.1.1/
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)    35149 2023-07-23 17:23:07.000000 NASTI-0.1.1/LICENSE
-drwxr-xr-x   0 adamdrew  (1000) adamdrew  (1000)        0 2023-07-23 18:20:31.052266 NASTI-0.1.1/NASTI.egg-info/
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     7237 2023-07-23 18:20:31.000000 NASTI-0.1.1/NASTI.egg-info/PKG-INFO
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)      441 2023-07-23 18:20:31.000000 NASTI-0.1.1/NASTI.egg-info/SOURCES.txt
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)        1 2023-07-23 18:20:31.000000 NASTI-0.1.1/NASTI.egg-info/dependency_links.txt
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)       12 2023-07-23 18:20:31.000000 NASTI-0.1.1/NASTI.egg-info/top_level.txt
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     7237 2023-07-23 18:20:31.053265 NASTI-0.1.1/PKG-INFO
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     6772 2023-07-23 17:17:03.000000 NASTI-0.1.1/README.md
-drwxr-xr-x   0 adamdrew  (1000) adamdrew  (1000)        0 2023-07-23 18:20:31.052266 NASTI-0.1.1/nasti/
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)        0 2023-07-22 16:17:53.000000 NASTI-0.1.1/nasti/__init__.py
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     1256 2023-07-23 12:54:01.000000 NASTI-0.1.1/nasti/cli.py
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     1048 2023-07-23 15:52:01.000000 NASTI-0.1.1/nasti/exceptions.py
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     4272 2023-07-23 16:09:18.000000 NASTI-0.1.1/nasti/mutation.py
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     3043 2023-07-23 12:55:39.000000 NASTI-0.1.1/nasti/nasti.py
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     2583 2023-07-23 15:49:29.000000 NASTI-0.1.1/nasti/nastifile.py
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     3200 2023-07-23 15:42:52.000000 NASTI-0.1.1/nasti/source_handlers.py
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     1940 2023-07-23 15:32:28.000000 NASTI-0.1.1/nasti/validation.py
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)      103 2023-07-23 18:18:02.000000 NASTI-0.1.1/pyproject.toml
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)      554 2023-07-23 18:20:31.053265 NASTI-0.1.1/setup.cfg
-drwxr-xr-x   0 adamdrew  (1000) adamdrew  (1000)        0 2023-07-23 18:20:31.052266 NASTI-0.1.1/tests/
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)      335 2023-07-23 13:21:15.000000 NASTI-0.1.1/tests/__init__.py
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     1330 2023-07-23 16:12:36.000000 NASTI-0.1.1/tests/mocks.py
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     4908 2023-07-23 16:17:51.000000 NASTI-0.1.1/tests/test_mutation.py
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     1726 2023-07-23 15:49:17.000000 NASTI-0.1.1/tests/test_nastifile.py
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     2660 2023-07-23 15:43:52.000000 NASTI-0.1.1/tests/test_source_handlers.py
--rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     1505 2023-07-23 15:34:43.000000 NASTI-0.1.1/tests/test_validation.py
+drwxr-xr-x   0 adamdrew  (1000) adamdrew  (1000)        0 2023-07-23 18:25:25.386651 NASTI-0.1.2/
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)    35149 2023-07-23 17:23:07.000000 NASTI-0.1.2/LICENSE
+drwxr-xr-x   0 adamdrew  (1000) adamdrew  (1000)        0 2023-07-23 18:25:25.385651 NASTI-0.1.2/NASTI.egg-info/
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     7237 2023-07-23 18:25:25.000000 NASTI-0.1.2/NASTI.egg-info/PKG-INFO
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)      490 2023-07-23 18:25:25.000000 NASTI-0.1.2/NASTI.egg-info/SOURCES.txt
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)        1 2023-07-23 18:25:25.000000 NASTI-0.1.2/NASTI.egg-info/dependency_links.txt
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)       40 2023-07-23 18:25:25.000000 NASTI-0.1.2/NASTI.egg-info/entry_points.txt
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)       12 2023-07-23 18:25:25.000000 NASTI-0.1.2/NASTI.egg-info/top_level.txt
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     7237 2023-07-23 18:25:25.386651 NASTI-0.1.2/PKG-INFO
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     6772 2023-07-23 17:17:03.000000 NASTI-0.1.2/README.md
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)       39 2023-07-23 18:24:48.000000 NASTI-0.1.2/entry_points.txt
+drwxr-xr-x   0 adamdrew  (1000) adamdrew  (1000)        0 2023-07-23 18:25:25.386651 NASTI-0.1.2/nasti/
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)        0 2023-07-22 16:17:53.000000 NASTI-0.1.2/nasti/__init__.py
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     1256 2023-07-23 12:54:01.000000 NASTI-0.1.2/nasti/cli.py
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     1048 2023-07-23 15:52:01.000000 NASTI-0.1.2/nasti/exceptions.py
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     4272 2023-07-23 16:09:18.000000 NASTI-0.1.2/nasti/mutation.py
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     3043 2023-07-23 12:55:39.000000 NASTI-0.1.2/nasti/nasti.py
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     2583 2023-07-23 15:49:29.000000 NASTI-0.1.2/nasti/nastifile.py
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     3200 2023-07-23 15:42:52.000000 NASTI-0.1.2/nasti/source_handlers.py
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     1940 2023-07-23 15:32:28.000000 NASTI-0.1.2/nasti/validation.py
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)      105 2023-07-23 18:23:16.000000 NASTI-0.1.2/pyproject.toml
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)      592 2023-07-23 18:25:25.387651 NASTI-0.1.2/setup.cfg
+drwxr-xr-x   0 adamdrew  (1000) adamdrew  (1000)        0 2023-07-23 18:25:25.386651 NASTI-0.1.2/tests/
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)      335 2023-07-23 13:21:15.000000 NASTI-0.1.2/tests/__init__.py
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     1330 2023-07-23 16:12:36.000000 NASTI-0.1.2/tests/mocks.py
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     4908 2023-07-23 16:17:51.000000 NASTI-0.1.2/tests/test_mutation.py
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     1726 2023-07-23 15:49:17.000000 NASTI-0.1.2/tests/test_nastifile.py
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     2660 2023-07-23 15:43:52.000000 NASTI-0.1.2/tests/test_source_handlers.py
+-rw-r--r--   0 adamdrew  (1000) adamdrew  (1000)     1505 2023-07-23 15:34:43.000000 NASTI-0.1.2/tests/test_validation.py
```

### Comparing `NASTI-0.1.1/LICENSE` & `NASTI-0.1.2/LICENSE`

 * *Files identical despite different names*

### Comparing `NASTI-0.1.1/NASTI.egg-info/PKG-INFO` & `NASTI-0.1.2/NASTI.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: NASTI
-Version: 0.1.1
+Version: 0.1.2
 Summary: NASTI is Not A Starndard Templating Implementation
 Home-page: https://github.com/adamrdrew/nasti
 Author: Adam Drew
 Author-email: adamrdrew@live.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU General Public License v3 (GPLv3)
 Classifier: Operating System :: OS Independent
```

### Comparing `NASTI-0.1.1/PKG-INFO` & `NASTI-0.1.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: NASTI
-Version: 0.1.1
+Version: 0.1.2
 Summary: NASTI is Not A Starndard Templating Implementation
 Home-page: https://github.com/adamrdrew/nasti
 Author: Adam Drew
 Author-email: adamrdrew@live.com
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU General Public License v3 (GPLv3)
 Classifier: Operating System :: OS Independent
```

### Comparing `NASTI-0.1.1/README.md` & `NASTI-0.1.2/README.md`

 * *Files identical despite different names*

### Comparing `NASTI-0.1.1/nasti/cli.py` & `NASTI-0.1.2/nasti/cli.py`

 * *Files identical despite different names*

### Comparing `NASTI-0.1.1/nasti/exceptions.py` & `NASTI-0.1.2/nasti/exceptions.py`

 * *Files identical despite different names*

### Comparing `NASTI-0.1.1/nasti/mutation.py` & `NASTI-0.1.2/nasti/mutation.py`

 * *Files identical despite different names*

### Comparing `NASTI-0.1.1/nasti/nasti.py` & `NASTI-0.1.2/nasti/nasti.py`

 * *Files identical despite different names*

### Comparing `NASTI-0.1.1/nasti/nastifile.py` & `NASTI-0.1.2/nasti/nastifile.py`

 * *Files identical despite different names*

### Comparing `NASTI-0.1.1/nasti/source_handlers.py` & `NASTI-0.1.2/nasti/source_handlers.py`

 * *Files identical despite different names*

### Comparing `NASTI-0.1.1/nasti/validation.py` & `NASTI-0.1.2/nasti/validation.py`

 * *Files identical despite different names*

### Comparing `NASTI-0.1.1/setup.cfg` & `NASTI-0.1.2/setup.cfg`

 * *Files 12% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = NASTI
-version = 0.1.1
+version = 0.1.2
 author = Adam Drew
 author_email = adamrdrew@live.com
 description = NASTI is Not A Starndard Templating Implementation
 long_description = file: README.md
 long_description_content_type = text/markdown
 url = https://github.com/adamrdrew/nasti
 classifiers = 
@@ -12,12 +12,13 @@
 	License :: OSI Approved :: GNU General Public License v3 (GPLv3)
 	Operating System :: OS Independent
 
 [options]
 packages = find:
 python_requires = >=3.10
 include_package_data = True
+entry_points = file: entry_points.txt
 
 [egg_info]
 tag_build = 
 tag_date = 0
```

### Comparing `NASTI-0.1.1/tests/mocks.py` & `NASTI-0.1.2/tests/mocks.py`

 * *Files identical despite different names*

### Comparing `NASTI-0.1.1/tests/test_mutation.py` & `NASTI-0.1.2/tests/test_mutation.py`

 * *Files identical despite different names*

### Comparing `NASTI-0.1.1/tests/test_nastifile.py` & `NASTI-0.1.2/tests/test_nastifile.py`

 * *Files identical despite different names*

### Comparing `NASTI-0.1.1/tests/test_source_handlers.py` & `NASTI-0.1.2/tests/test_source_handlers.py`

 * *Files identical despite different names*

### Comparing `NASTI-0.1.1/tests/test_validation.py` & `NASTI-0.1.2/tests/test_validation.py`

 * *Files identical despite different names*

