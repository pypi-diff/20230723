# Comparing `tmp/fly_python_sdk-0.2.0.tar.gz` & `tmp/fly_python_sdk-0.2.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "fly_python_sdk-0.2.0.tar", max compression
+gzip compressed data, was "fly_python_sdk-0.2.1.tar", max compression
```

## Comparing `fly_python_sdk-0.2.0.tar` & `fly_python_sdk-0.2.1.tar`

### file list

```diff
@@ -1,11 +1,11 @@
--rw-r--r--   0        0        0     1075 2023-07-12 06:38:46.580732 fly_python_sdk-0.2.0/LICENSE
--rw-r--r--   0        0        0      111 2023-07-13 13:15:49.336273 fly_python_sdk-0.2.0/README.md
--rw-r--r--   0        0        0     2055 2023-07-13 13:06:08.894504 fly_python_sdk-0.2.0/fly_python_sdk/__init__.py
--rw-r--r--   0        0        0     1186 2023-07-19 14:03:34.056345 fly_python_sdk-0.2.0/fly_python_sdk/copilot/main.py
--rw-r--r--   0        0        0     7357 2023-07-14 05:05:04.571518 fly_python_sdk-0.2.0/fly_python_sdk/copilot/templates/htmx/machines_grid.html
--rw-r--r--   0        0        0      938 2023-07-14 05:05:04.571617 fly_python_sdk-0.2.0/fly_python_sdk/copilot/templates/index.html
--rw-r--r--   0        0        0     1268 2023-07-13 13:08:39.186273 fly_python_sdk-0.2.0/fly_python_sdk/exceptions.py
--rw-r--r--   0        0        0    12966 2023-07-14 05:05:04.571811 fly_python_sdk-0.2.0/fly_python_sdk/fly.py
--rw-r--r--   0        0        0     3543 2023-07-23 00:49:17.240139 fly_python_sdk-0.2.0/fly_python_sdk/models.py
--rw-r--r--   0        0        0      498 2023-07-23 00:50:15.312401 fly_python_sdk-0.2.0/pyproject.toml
--rw-r--r--   0        0        0      604 1970-01-01 00:00:00.000000 fly_python_sdk-0.2.0/PKG-INFO
+-rw-r--r--   0        0        0     1075 2023-07-12 06:38:46.580732 fly_python_sdk-0.2.1/LICENSE
+-rw-r--r--   0        0        0      111 2023-07-13 13:15:49.336273 fly_python_sdk-0.2.1/README.md
+-rw-r--r--   0        0        0     2055 2023-07-13 13:06:08.894504 fly_python_sdk-0.2.1/fly_python_sdk/__init__.py
+-rw-r--r--   0        0        0     1186 2023-07-19 14:03:34.056345 fly_python_sdk-0.2.1/fly_python_sdk/copilot/main.py
+-rw-r--r--   0        0        0     7357 2023-07-14 05:05:04.571518 fly_python_sdk-0.2.1/fly_python_sdk/copilot/templates/htmx/machines_grid.html
+-rw-r--r--   0        0        0      938 2023-07-14 05:05:04.571617 fly_python_sdk-0.2.1/fly_python_sdk/copilot/templates/index.html
+-rw-r--r--   0        0        0     1268 2023-07-13 13:08:39.186273 fly_python_sdk-0.2.1/fly_python_sdk/exceptions.py
+-rw-r--r--   0        0        0    12966 2023-07-14 05:05:04.571811 fly_python_sdk-0.2.1/fly_python_sdk/fly.py
+-rw-r--r--   0        0        0     3543 2023-07-23 00:49:17.240139 fly_python_sdk-0.2.1/fly_python_sdk/models.py
+-rw-r--r--   0        0        0      498 2023-07-23 00:51:26.236906 fly_python_sdk-0.2.1/pyproject.toml
+-rw-r--r--   0        0        0      604 1970-01-01 00:00:00.000000 fly_python_sdk-0.2.1/PKG-INFO
```

### Comparing `fly_python_sdk-0.2.0/LICENSE` & `fly_python_sdk-0.2.1/LICENSE`

 * *Files identical despite different names*

### Comparing `fly_python_sdk-0.2.0/fly_python_sdk/__init__.py` & `fly_python_sdk-0.2.1/fly_python_sdk/__init__.py`

 * *Files identical despite different names*

### Comparing `fly_python_sdk-0.2.0/fly_python_sdk/copilot/main.py` & `fly_python_sdk-0.2.1/fly_python_sdk/copilot/main.py`

 * *Files identical despite different names*

### Comparing `fly_python_sdk-0.2.0/fly_python_sdk/copilot/templates/htmx/machines_grid.html` & `fly_python_sdk-0.2.1/fly_python_sdk/copilot/templates/htmx/machines_grid.html`

 * *Files identical despite different names*

### Comparing `fly_python_sdk-0.2.0/fly_python_sdk/copilot/templates/index.html` & `fly_python_sdk-0.2.1/fly_python_sdk/copilot/templates/index.html`

 * *Files identical despite different names*

### Comparing `fly_python_sdk-0.2.0/fly_python_sdk/exceptions.py` & `fly_python_sdk-0.2.1/fly_python_sdk/exceptions.py`

 * *Files identical despite different names*

### Comparing `fly_python_sdk-0.2.0/fly_python_sdk/fly.py` & `fly_python_sdk-0.2.1/fly_python_sdk/fly.py`

 * *Files identical despite different names*

### Comparing `fly_python_sdk-0.2.0/fly_python_sdk/models.py` & `fly_python_sdk-0.2.1/fly_python_sdk/models.py`

 * *Files identical despite different names*

### Comparing `fly_python_sdk-0.2.0/PKG-INFO` & `fly_python_sdk-0.2.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: fly-python-sdk
-Version: 0.2.0
+Version: 0.2.1
 Summary: 
 Author: Brian Li
 Author-email: brian@brianli.com
 Requires-Python: >=3.11,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.11
 Requires-Dist: fastapi (>=0.100.0,<0.101.0)
```

