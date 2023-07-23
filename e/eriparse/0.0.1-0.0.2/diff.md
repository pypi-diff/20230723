# Comparing `tmp/eriparse-0.0.1.tar.gz` & `tmp/eriparse-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "eriparse-0.0.1.tar", last modified: Sun Jul 23 02:48:32 2023, max compression
+gzip compressed data, was "eriparse-0.0.2.tar", last modified: Sun Jul 23 03:29:49 2023, max compression
```

## Comparing `eriparse-0.0.1.tar` & `eriparse-0.0.2.tar`

### file list

```diff
@@ -1,22 +1,27 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:48:32.602825 eriparse-0.0.1/
--rw-r--r--   0 runner    (1001) docker     (123)      869 2023-07-23 02:48:32.602825 eriparse-0.0.1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      662 2023-07-23 02:47:54.000000 eriparse-0.0.1/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:48:32.602825 eriparse-0.0.1/eriparse.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)      869 2023-07-23 02:48:32.000000 eriparse-0.0.1/eriparse.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      413 2023-07-23 02:48:32.000000 eriparse-0.0.1/eriparse.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 02:48:32.000000 eriparse-0.0.1/eriparse.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 02:48:32.000000 eriparse-0.0.1/eriparse.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 02:48:32.000000 eriparse-0.0.1/eriparse.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)      441 2023-07-23 02:47:54.000000 eriparse-0.0.1/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)      176 2023-07-23 02:48:32.602825 eriparse-0.0.1/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      220 2023-07-23 02:47:54.000000 eriparse-0.0.1/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:48:32.602825 eriparse-0.0.1/tests/
--rw-r--r--   0 runner    (1001) docker     (123)     3837 2023-07-23 02:47:55.000000 eriparse-0.0.1/tests/test_atlanta.py
--rw-r--r--   0 runner    (1001) docker     (123)     1762 2023-07-23 02:47:55.000000 eriparse-0.0.1/tests/test_baltimore.py
--rw-r--r--   0 runner    (1001) docker     (123)     3810 2023-07-23 02:47:55.000000 eriparse-0.0.1/tests/test_boston.py
--rw-r--r--   0 runner    (1001) docker     (123)     3829 2023-07-23 02:47:55.000000 eriparse-0.0.1/tests/test_charlottesville.py
--rw-r--r--   0 runner    (1001) docker     (123)     3829 2023-07-23 02:47:55.000000 eriparse-0.0.1/tests/test_chicago.py
--rw-r--r--   0 runner    (1001) docker     (123)     3829 2023-07-23 02:47:55.000000 eriparse-0.0.1/tests/test_durham.py
--rw-r--r--   0 runner    (1001) docker     (123)     1808 2023-07-23 02:47:55.000000 eriparse-0.0.1/tests/test_philadelphia.py
--rw-r--r--   0 runner    (1001) docker     (123)     1804 2023-07-23 02:47:55.000000 eriparse-0.0.1/tests/test_pittsburg.py
--rw-r--r--   0 runner    (1001) docker     (123)      609 2023-07-23 02:47:55.000000 eriparse-0.0.1/tests/test_utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 03:29:49.119241 eriparse-0.0.2/
+-rw-r--r--   0 runner    (1001) docker     (123)     1079 2023-07-23 03:29:20.000000 eriparse-0.0.2/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     1142 2023-07-23 03:29:49.119241 eriparse-0.0.2/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      785 2023-07-23 03:29:20.000000 eriparse-0.0.2/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)        5 2023-07-23 03:29:20.000000 eriparse-0.0.2/VERSION
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 03:29:49.115241 eriparse-0.0.2/eriparse/
+-rw-r--r--   0 runner    (1001) docker     (123)       54 2023-07-23 03:29:20.000000 eriparse-0.0.2/eriparse/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      280 2023-07-23 03:29:20.000000 eriparse-0.0.2/eriparse/main.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3409 2023-07-23 03:29:20.000000 eriparse-0.0.2/eriparse/parse.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 03:29:49.115241 eriparse-0.0.2/eriparse.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1142 2023-07-23 03:29:49.000000 eriparse-0.0.2/eriparse.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      466 2023-07-23 03:29:49.000000 eriparse-0.0.2/eriparse.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 03:29:49.000000 eriparse-0.0.2/eriparse.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 03:29:49.000000 eriparse-0.0.2/eriparse.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-23 03:29:49.000000 eriparse-0.0.2/eriparse.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      767 2023-07-23 03:29:20.000000 eriparse-0.0.2/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 03:29:49.119241 eriparse-0.0.2/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 03:29:49.115241 eriparse-0.0.2/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     3837 2023-07-23 03:29:20.000000 eriparse-0.0.2/tests/test_atlanta.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1762 2023-07-23 03:29:20.000000 eriparse-0.0.2/tests/test_baltimore.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3810 2023-07-23 03:29:20.000000 eriparse-0.0.2/tests/test_boston.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3829 2023-07-23 03:29:20.000000 eriparse-0.0.2/tests/test_charlottesville.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3829 2023-07-23 03:29:20.000000 eriparse-0.0.2/tests/test_chicago.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3829 2023-07-23 03:29:20.000000 eriparse-0.0.2/tests/test_durham.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1808 2023-07-23 03:29:20.000000 eriparse-0.0.2/tests/test_philadelphia.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1804 2023-07-23 03:29:20.000000 eriparse-0.0.2/tests/test_pittsburg.py
+-rw-r--r--   0 runner    (1001) docker     (123)      609 2023-07-23 03:29:20.000000 eriparse-0.0.2/tests/test_utils.py
```

### Comparing `eriparse-0.0.1/PKG-INFO` & `eriparse-0.0.2/PKG-INFO`

 * *Files 22% similar despite different names*

```diff
@@ -1,30 +1,33 @@
 Metadata-Version: 2.1
 Name: eriparse
-Version: 0.0.1
-Summary: Web Scraper of Economic Research Institude HTML.
+Version: 0.0.2
+Summary: HTML Parser of Economic Research Institute Cost of Living HTML.
 Author: Nicholas Grillini-Lawrence
+License: MIT
+Keywords: webscraper,webscraping,web-scraper,web-scraping,html,eri,erieri.com,cost-of-living,python
 Description-Content-Type: text/markdown
 Provides-Extra: dev
+License-File: LICENSE
 
 
 # Eriparse
+![is_still_valid_workflow](https://github.com/ncgl-git/eriparse/actions/workflows/is_still_valid.yaml/badge.svg)
 
 *HTML parsing logic for `https://www.erieri.com/cost-of-living-calculator`. Was written to help my wife and I better understand the differences between potential cities for her fellowship.*
 
 
-## Notes
-Be aware that website frontend can change _whenver_, so, rely on the build badge above for is_valid to know whether the website HTML has changed.
+#### Notes
+Be aware that website frontend can change _whenver_, so, rely on the build badge above for is_still_valid to know whether the website HTML has changed.
 
 
 ## Usage
 
 Intended to be called like: 
 ```
-wget -q https://www.erieri.com/cost-of-living/united-states/illinois/chicago -O - | pipenv run python main.py >> chicago.json
-
+wget -q https://www.erieri.com/cost-of-living/united-states/illinois/chicago -O - | pipenv run python eriparse/main.py >> chicago.json
 ```
 
 Or, if you'd like to integrate it into your Python code,  `>>> pip install eriparse`
 ```
-from eriparse.parse import parse
+from eriparse import parse
 ```
```

### Comparing `eriparse-0.0.1/eriparse.egg-info/PKG-INFO` & `eriparse-0.0.2/eriparse.egg-info/PKG-INFO`

 * *Files 22% similar despite different names*

```diff
@@ -1,30 +1,33 @@
 Metadata-Version: 2.1
 Name: eriparse
-Version: 0.0.1
-Summary: Web Scraper of Economic Research Institude HTML.
+Version: 0.0.2
+Summary: HTML Parser of Economic Research Institute Cost of Living HTML.
 Author: Nicholas Grillini-Lawrence
+License: MIT
+Keywords: webscraper,webscraping,web-scraper,web-scraping,html,eri,erieri.com,cost-of-living,python
 Description-Content-Type: text/markdown
 Provides-Extra: dev
+License-File: LICENSE
 
 
 # Eriparse
+![is_still_valid_workflow](https://github.com/ncgl-git/eriparse/actions/workflows/is_still_valid.yaml/badge.svg)
 
 *HTML parsing logic for `https://www.erieri.com/cost-of-living-calculator`. Was written to help my wife and I better understand the differences between potential cities for her fellowship.*
 
 
-## Notes
-Be aware that website frontend can change _whenver_, so, rely on the build badge above for is_valid to know whether the website HTML has changed.
+#### Notes
+Be aware that website frontend can change _whenver_, so, rely on the build badge above for is_still_valid to know whether the website HTML has changed.
 
 
 ## Usage
 
 Intended to be called like: 
 ```
-wget -q https://www.erieri.com/cost-of-living/united-states/illinois/chicago -O - | pipenv run python main.py >> chicago.json
-
+wget -q https://www.erieri.com/cost-of-living/united-states/illinois/chicago -O - | pipenv run python eriparse/main.py >> chicago.json
 ```
 
 Or, if you'd like to integrate it into your Python code,  `>>> pip install eriparse`
 ```
-from eriparse.parse import parse
+from eriparse import parse
 ```
```

### Comparing `eriparse-0.0.1/tests/test_atlanta.py` & `eriparse-0.0.2/tests/test_atlanta.py`

 * *Files identical despite different names*

### Comparing `eriparse-0.0.1/tests/test_baltimore.py` & `eriparse-0.0.2/tests/test_baltimore.py`

 * *Files identical despite different names*

### Comparing `eriparse-0.0.1/tests/test_boston.py` & `eriparse-0.0.2/tests/test_boston.py`

 * *Files identical despite different names*

### Comparing `eriparse-0.0.1/tests/test_charlottesville.py` & `eriparse-0.0.2/tests/test_charlottesville.py`

 * *Files identical despite different names*

### Comparing `eriparse-0.0.1/tests/test_chicago.py` & `eriparse-0.0.2/tests/test_chicago.py`

 * *Files identical despite different names*

### Comparing `eriparse-0.0.1/tests/test_durham.py` & `eriparse-0.0.2/tests/test_durham.py`

 * *Files identical despite different names*

### Comparing `eriparse-0.0.1/tests/test_philadelphia.py` & `eriparse-0.0.2/tests/test_philadelphia.py`

 * *Files identical despite different names*

### Comparing `eriparse-0.0.1/tests/test_pittsburg.py` & `eriparse-0.0.2/tests/test_pittsburg.py`

 * *Files identical despite different names*

### Comparing `eriparse-0.0.1/tests/test_utils.py` & `eriparse-0.0.2/tests/test_utils.py`

 * *Files identical despite different names*

