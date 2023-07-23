# Comparing `tmp/lb-telemetry-0.2.1.tar.gz` & `tmp/lb-telemetry-0.3.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "/builds/lhcb/lb-telemetry/dist/.tmp-5nd60wga/lb-telemetry-0.2.1.tar", last modified: Sat Jul 22 12:06:02 2023, max compression
+gzip compressed data, was "/builds/lhcb/lb-telemetry/dist/.tmp-huk113xd/lb-telemetry-0.3.0.tar", last modified: Sun Jul 23 06:09:11 2023, max compression
```

## Comparing `lb-telemetry-0.2.1.tar` & `lb-telemetry-0.3.0.tar`

### file list

```diff
@@ -1,23 +1,24 @@
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-22 12:06:02.000000 lb-telemetry-0.2.1/
--rw-r--r--   0 root         (0) root         (0)     2191 2023-07-22 12:05:27.000000 lb-telemetry-0.2.1/.gitignore
--rw-r--r--   0 root         (0) root         (0)     1967 2023-07-22 12:05:27.000000 lb-telemetry-0.2.1/.gitlab-ci.yml
--rw-r--r--   0 root         (0) root         (0)       37 2023-07-22 12:05:27.000000 lb-telemetry-0.2.1/.mypy.ini
--rw-r--r--   0 root         (0) root         (0)      594 2023-07-22 12:05:27.000000 lb-telemetry-0.2.1/.pre-commit-config.yaml
--rw-r--r--   0 root         (0) root         (0)    18151 2023-07-22 12:05:27.000000 lb-telemetry-0.2.1/.pylintrc
--rw-r--r--   0 root         (0) root         (0)    35065 2023-07-22 12:05:27.000000 lb-telemetry-0.2.1/LICENSE
--rw-r--r--   0 root         (0) root         (0)     2214 2023-07-22 12:06:02.000000 lb-telemetry-0.2.1/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)     1540 2023-07-22 12:05:27.000000 lb-telemetry-0.2.1/README.md
--rw-r--r--   0 root         (0) root         (0)     1210 2023-07-22 12:05:27.000000 lb-telemetry-0.2.1/pyproject.toml
--rw-r--r--   0 root         (0) root         (0)       38 2023-07-22 12:06:02.000000 lb-telemetry-0.2.1/setup.cfg
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-22 12:06:02.000000 lb-telemetry-0.2.1/src/
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-22 12:06:02.000000 lb-telemetry-0.2.1/src/lb_telemetry/
--rw-r--r--   0 root         (0) root         (0)     6374 2023-07-22 12:05:27.000000 lb-telemetry-0.2.1/src/lb_telemetry/__init__.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-22 12:06:02.000000 lb-telemetry-0.2.1/src/lb_telemetry.egg-info/
--rw-r--r--   0 root         (0) root         (0)     2214 2023-07-22 12:06:02.000000 lb-telemetry-0.2.1/src/lb_telemetry.egg-info/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)      369 2023-07-22 12:06:02.000000 lb-telemetry-0.2.1/src/lb_telemetry.egg-info/SOURCES.txt
--rw-r--r--   0 root         (0) root         (0)        1 2023-07-22 12:06:02.000000 lb-telemetry-0.2.1/src/lb_telemetry.egg-info/dependency_links.txt
--rw-r--r--   0 root         (0) root         (0)      110 2023-07-22 12:06:02.000000 lb-telemetry-0.2.1/src/lb_telemetry.egg-info/requires.txt
--rw-r--r--   0 root         (0) root         (0)       13 2023-07-22 12:06:02.000000 lb-telemetry-0.2.1/src/lb_telemetry.egg-info/top_level.txt
-drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-22 12:06:02.000000 lb-telemetry-0.2.1/tests/
--rw-r--r--   0 root         (0) root         (0)       60 2023-07-22 12:05:27.000000 lb-telemetry-0.2.1/tests/__init__.py
--rw-r--r--   0 root         (0) root         (0)     6052 2023-07-22 12:05:27.000000 lb-telemetry-0.2.1/tests/test_logger.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 06:09:11.000000 lb-telemetry-0.3.0/
+-rw-r--r--   0 root         (0) root         (0)     2191 2023-07-23 06:09:03.000000 lb-telemetry-0.3.0/.gitignore
+-rw-r--r--   0 root         (0) root         (0)     1967 2023-07-23 06:09:03.000000 lb-telemetry-0.3.0/.gitlab-ci.yml
+-rw-r--r--   0 root         (0) root         (0)       37 2023-07-23 06:09:03.000000 lb-telemetry-0.3.0/.mypy.ini
+-rw-r--r--   0 root         (0) root         (0)      594 2023-07-23 06:09:03.000000 lb-telemetry-0.3.0/.pre-commit-config.yaml
+-rw-r--r--   0 root         (0) root         (0)    18151 2023-07-23 06:09:03.000000 lb-telemetry-0.3.0/.pylintrc
+-rw-r--r--   0 root         (0) root         (0)    35065 2023-07-23 06:09:03.000000 lb-telemetry-0.3.0/LICENSE
+-rw-r--r--   0 root         (0) root         (0)     2214 2023-07-23 06:09:11.000000 lb-telemetry-0.3.0/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)     1540 2023-07-23 06:09:03.000000 lb-telemetry-0.3.0/README.md
+-rw-r--r--   0 root         (0) root         (0)     1352 2023-07-23 06:09:03.000000 lb-telemetry-0.3.0/pyproject.toml
+-rw-r--r--   0 root         (0) root         (0)       38 2023-07-23 06:09:11.000000 lb-telemetry-0.3.0/setup.cfg
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 06:09:11.000000 lb-telemetry-0.3.0/src/
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 06:09:11.000000 lb-telemetry-0.3.0/src/lb_telemetry/
+-rw-r--r--   0 root         (0) root         (0)     6386 2023-07-23 06:09:03.000000 lb-telemetry-0.3.0/src/lb_telemetry/__init__.py
+-rw-r--r--   0 root         (0) root         (0)        0 2023-07-23 06:09:03.000000 lb-telemetry-0.3.0/src/lb_telemetry/py.typed
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 06:09:11.000000 lb-telemetry-0.3.0/src/lb_telemetry.egg-info/
+-rw-r--r--   0 root         (0) root         (0)     2214 2023-07-23 06:09:11.000000 lb-telemetry-0.3.0/src/lb_telemetry.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)      395 2023-07-23 06:09:11.000000 lb-telemetry-0.3.0/src/lb_telemetry.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-07-23 06:09:11.000000 lb-telemetry-0.3.0/src/lb_telemetry.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)      110 2023-07-23 06:09:11.000000 lb-telemetry-0.3.0/src/lb_telemetry.egg-info/requires.txt
+-rw-r--r--   0 root         (0) root         (0)       13 2023-07-23 06:09:11.000000 lb-telemetry-0.3.0/src/lb_telemetry.egg-info/top_level.txt
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 06:09:11.000000 lb-telemetry-0.3.0/tests/
+-rw-r--r--   0 root         (0) root         (0)       60 2023-07-23 06:09:03.000000 lb-telemetry-0.3.0/tests/__init__.py
+-rw-r--r--   0 root         (0) root         (0)     6073 2023-07-23 06:09:03.000000 lb-telemetry-0.3.0/tests/test_logger.py
```

### Comparing `lb-telemetry-0.2.1/.gitignore` & `lb-telemetry-0.3.0/.gitignore`

 * *Files identical despite different names*

### Comparing `lb-telemetry-0.2.1/.gitlab-ci.yml` & `lb-telemetry-0.3.0/.gitlab-ci.yml`

 * *Files identical despite different names*

### Comparing `lb-telemetry-0.2.1/.pre-commit-config.yaml` & `lb-telemetry-0.3.0/.pre-commit-config.yaml`

 * *Files identical despite different names*

### Comparing `lb-telemetry-0.2.1/.pylintrc` & `lb-telemetry-0.3.0/.pylintrc`

 * *Files identical despite different names*

### Comparing `lb-telemetry-0.2.1/LICENSE` & `lb-telemetry-0.3.0/LICENSE`

 * *Files identical despite different names*

### Comparing `lb-telemetry-0.2.1/PKG-INFO` & `lb-telemetry-0.3.0/PKG-INFO`

 * *Files 9% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: lb-telemetry
-Version: 0.2.1
+Version: 0.3.0
 Summary: A utility for logging telemetry data from LHCb packages to MONIT
 Author-email: Cameron McClymont <cameron.duncan.mcclymont@cern.ch>, Daniel Cervenkov <daniel.cervenkov@cern.ch>, Chris Burr <christopher.burr@cern.ch>
 Project-URL: Homepage, https://gitlab.cern.ch/lhcb/lb-telemetry
 Project-URL: Bug Tracker, https://gitlab.cern.ch/lhcb/lb-telemetry/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU General Public License v3 (GPLv3)
 Classifier: Operating System :: OS Independent
```

### Comparing `lb-telemetry-0.2.1/README.md` & `lb-telemetry-0.3.0/README.md`

 * *Files identical despite different names*

### Comparing `lb-telemetry-0.2.1/pyproject.toml` & `lb-telemetry-0.3.0/pyproject.toml`

 * *Files 8% similar despite different names*

```diff
@@ -48,7 +48,13 @@
     "mypy-extensions",
     "pre-commit",
     "pytest",
     "pytest-cov",
     "ruff",
     "types-requests"
 ]
+
+[tool.ruff]
+select = ["E", "F", "B", "I", "PLE", "RUF", "UP"]
+target-version = "py39"
+[tool.ruff.isort]
+known-first-party = ["lb_telemetry"]
```

### Comparing `lb-telemetry-0.2.1/src/lb_telemetry/__init__.py` & `lb-telemetry-0.3.0/src/lb_telemetry/__init__.py`

 * *Files 3% similar despite different names*

```diff
@@ -10,19 +10,19 @@
 ###############################################################################
 
 import json
 import platform
 import time
 from typing import Optional
 
-from LbPlatformUtils import inspect
 import requests
+from LbPlatformUtils import inspect
 from logzero import logger as logzero
 
-INFLUXDB_LEGAL_TYPES = [bool, int, float, str]
+INFLUXDB_LEGAL_TYPES = (bool, int, float, str)
 
 
 class Logger:
     def __init__(
         self,
         producer="lb-telemetry",
         datasource_id="10459",
@@ -49,27 +49,27 @@
         """
         if not data:
             logzero.warning("'data' arg should not be empty")
             return False
 
         # Ensure all data sent has a legal type
         for value in data.values():
-            if type(value) not in INFLUXDB_LEGAL_TYPES:
+            if not isinstance(value, INFLUXDB_LEGAL_TYPES):
                 logzero.warning(
                     f"{value} has type {type(value)} "
                     f"which isn't a type supported by InfluxDB"
                 )
                 return False
 
         # Every declared tag should also appear in the data dictionary
         for tag in tags:
             if tag not in data.keys():
                 logzero.warning(f"The tag {tag} does not appear in the data dictionary")
                 return False
-            elif type(data[tag]) != str:
+            elif not isinstance(data[tag], str):
                 logzero.warning(
                     f"The tag {tag}: ({data[tag]}) has a value of type "
                     f"{type(data[tag])} so will be converted to a string"
                 )
 
         return True
```

### Comparing `lb-telemetry-0.2.1/src/lb_telemetry.egg-info/PKG-INFO` & `lb-telemetry-0.3.0/src/lb_telemetry.egg-info/PKG-INFO`

 * *Files 9% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: lb-telemetry
-Version: 0.2.1
+Version: 0.3.0
 Summary: A utility for logging telemetry data from LHCb packages to MONIT
 Author-email: Cameron McClymont <cameron.duncan.mcclymont@cern.ch>, Daniel Cervenkov <daniel.cervenkov@cern.ch>, Chris Burr <christopher.burr@cern.ch>
 Project-URL: Homepage, https://gitlab.cern.ch/lhcb/lb-telemetry
 Project-URL: Bug Tracker, https://gitlab.cern.ch/lhcb/lb-telemetry/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: GNU General Public License v3 (GPLv3)
 Classifier: Operating System :: OS Independent
```

### Comparing `lb-telemetry-0.2.1/tests/test_logger.py` & `lb-telemetry-0.3.0/tests/test_logger.py`

 * *Files 3% similar despite different names*

```diff
@@ -101,26 +101,28 @@
 
     return token
 
 
 def fetch_test_log(logger: Logger, ts: int, token: str) -> Optional[dict]:
     base_url = "https://monit-grafana.cern.ch/api/datasources"
     path = f"proxy/{logger.datasource_id}/query?db={logger.database}"
-    query = f"select * from {TEST_TABLE} where time = {ts}ms"  # noqa
+    query = f"select * from {TEST_TABLE} where time = {ts}ms"
 
     try:
         response = requests.post(
             f"{base_url}/{path}",
             headers={
                 "Authorization": f"Bearer {token}",
             },
             files={"q": query.encode("utf-8")},
         )
     except requests.exceptions.RequestException as e:
-        raise LogFetchError(f"An error occurred while verifying the test log: {e}")
+        raise LogFetchError(
+            f"An error occurred while verifying the test log: {e}"
+        ) from e
 
     if response.status_code != 200:
         raise LogFetchError(
             f"Unexpected status code {response.status_code}: " f"{response.text}"
         )
 
     results: dict = json.loads(response.text)["results"][0]
```

