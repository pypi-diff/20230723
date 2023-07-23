# Comparing `tmp/keyrings_envvars-1.0.1.tar.gz` & `tmp/keyrings_envvars-1.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "keyrings_envvars-1.0.1.tar", last modified: Fri Jan  1 00:00:00 2016, max compression
+gzip compressed data, was "keyrings_envvars-1.0.2.tar", last modified: Fri Jan  1 00:00:00 2016, max compression
```

## Comparing `keyrings_envvars-1.0.1.tar` & `keyrings_envvars-1.0.2.tar`

### file list

```diff
@@ -1,10 +1,10 @@
--rw-r--r--   0        0        0     3983 2023-07-23 13:34:22.085752 keyrings_envvars-1.0.1/README.rst
--rw-r--r--   0        0        0     2054 2023-07-23 15:10:16.477771 keyrings_envvars-1.0.1/pyproject.toml
--rw-r--r--   0        0        0       76 2023-07-23 13:08:55.954574 keyrings_envvars-1.0.1/src/keyrings/envvars/__init__.py
--rw-r--r--   0        0        0     3561 2023-07-23 13:08:55.950574 keyrings_envvars-1.0.1/src/keyrings/envvars/keyring.py
--rw-r--r--   0        0        0        0 2023-07-23 13:08:55.946574 keyrings_envvars-1.0.1/src/keyrings/envvars/py.typed
--rw-r--r--   0        0        0       30 2023-07-23 13:08:55.954574 keyrings_envvars-1.0.1/src/keyrings/envvars/tests/__init__.py
--rw-r--r--   0        0        0     1774 2023-07-23 13:08:55.950574 keyrings_envvars-1.0.1/src/keyrings/envvars/tests/conftest.py
--rw-r--r--   0        0        0     2919 2023-07-23 13:08:55.954574 keyrings_envvars-1.0.1/src/keyrings/envvars/tests/keyring_test.py
--rw-r--r--   0        0        0     6866 2023-07-23 13:08:55.954574 keyrings_envvars-1.0.1/src/keyrings/envvars/tests/keyrings_envvars_test.py
--rw-r--r--   0        0        0     5290 1970-01-01 00:00:00.000000 keyrings_envvars-1.0.1/PKG-INFO
+-rw-r--r--   0        0        0     3983 2023-07-23 13:34:22.085752 keyrings_envvars-1.0.2/README.rst
+-rw-r--r--   0        0        0     2245 2023-07-23 15:49:52.914723 keyrings_envvars-1.0.2/pyproject.toml
+-rw-r--r--   0        0        0       76 2023-07-23 13:08:55.954574 keyrings_envvars-1.0.2/src/keyrings/envvars/__init__.py
+-rw-r--r--   0        0        0     3561 2023-07-23 13:08:55.950574 keyrings_envvars-1.0.2/src/keyrings/envvars/keyring.py
+-rw-r--r--   0        0        0        0 2023-07-23 13:08:55.946574 keyrings_envvars-1.0.2/src/keyrings/envvars/py.typed
+-rw-r--r--   0        0        0       30 2023-07-23 13:08:55.954574 keyrings_envvars-1.0.2/src/keyrings/envvars/tests/__init__.py
+-rw-r--r--   0        0        0     1774 2023-07-23 13:08:55.950574 keyrings_envvars-1.0.2/src/keyrings/envvars/tests/conftest.py
+-rw-r--r--   0        0        0     2919 2023-07-23 13:08:55.954574 keyrings_envvars-1.0.2/src/keyrings/envvars/tests/keyring_test.py
+-rw-r--r--   0        0        0     6866 2023-07-23 13:08:55.954574 keyrings_envvars-1.0.2/src/keyrings/envvars/tests/keyrings_envvars_test.py
+-rw-r--r--   0        0        0     5511 1970-01-01 00:00:00.000000 keyrings_envvars-1.0.2/PKG-INFO
```

### Comparing `keyrings_envvars-1.0.1/README.rst` & `keyrings_envvars-1.0.2/README.rst`

 * *Files identical despite different names*

### Comparing `keyrings_envvars-1.0.1/src/keyrings/envvars/keyring.py` & `keyrings_envvars-1.0.2/src/keyrings/envvars/keyring.py`

 * *Files identical despite different names*

### Comparing `keyrings_envvars-1.0.1/src/keyrings/envvars/tests/conftest.py` & `keyrings_envvars-1.0.2/src/keyrings/envvars/tests/conftest.py`

 * *Files identical despite different names*

### Comparing `keyrings_envvars-1.0.1/src/keyrings/envvars/tests/keyring_test.py` & `keyrings_envvars-1.0.2/src/keyrings/envvars/tests/keyring_test.py`

 * *Files identical despite different names*

### Comparing `keyrings_envvars-1.0.1/src/keyrings/envvars/tests/keyrings_envvars_test.py` & `keyrings_envvars-1.0.2/src/keyrings/envvars/tests/keyrings_envvars_test.py`

 * *Files identical despite different names*

### Comparing `keyrings_envvars-1.0.1/PKG-INFO` & `keyrings_envvars-1.0.2/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: keyrings.envvars
-Version: 1.0.1
+Version: 1.0.2
 Summary: keyring backend plugin to retrieve credentials from environment variables.
 Author-email: Tom Cassidy <wirelessduck+py@gmail.com>
 Requires-Python: >=3.9,<4
 Description-Content-Type: text/x-rst
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
@@ -20,15 +20,18 @@
 Requires-Dist: pytest-antilru==1.1.1 ; extra == "pytest"
 Requires-Dist: pytest-cov==4.1.0 ; extra == "pytest"
 Requires-Dist: pytest-flakefinder==1.1.0 ; extra == "pytest"
 Requires-Dist: pytest-openfiles==0.5.0 ; extra == "pytest"
 Requires-Dist: pytest-randomly==3.13.0 ; extra == "pytest"
 Requires-Dist: pytest-xdist[psutil]==3.3.1 ; extra == "pytest"
 Requires-Dist: pytest==7.4.0 ; extra == "pytest"
-Project-URL: Home, https://github.com/wwuck
+Project-URL: Documentation, https://github.com/wwuck/keyrings.envvars
+Project-URL: Home, https://github.com/wwuck/keyrings.envvars
+Project-URL: Source, https://github.com/wwuck/keyrings.envvars
+Project-URL: Tracker, https://github.com/wwuck/keyrings.envvars/issues
 Provides-Extra: mypy
 Provides-Extra: pytest
 
 keyrings.envvars
 ================
 
 |PyPI| |Status| |Python Version| |License|
```

