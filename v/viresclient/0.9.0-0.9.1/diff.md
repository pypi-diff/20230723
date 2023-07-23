# Comparing `tmp/viresclient-0.9.0.tar.gz` & `tmp/viresclient-0.9.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "viresclient-0.9.0.tar", last modified: Tue Aug 24 21:43:43 2021, max compression
+gzip compressed data, was "viresclient-0.9.1.tar", last modified: Thu Oct  7 21:35:57 2021, max compression
```

## Comparing `viresclient-0.9.0.tar` & `viresclient-0.9.1.tar`

### file list

```diff
@@ -1,55 +1,57 @@
-drwxrwxr-x   0 ash       (1000) ash       (1000)        0 2021-08-24 21:43:43.474626 viresclient-0.9.0/
--rw-rw-r--   0 ash       (1000) ash       (1000)     6349 2021-08-24 21:43:43.474626 viresclient-0.9.0/PKG-INFO
--rw-r--r--   0 ash       (1000) ash       (1000)     5172 2021-08-23 14:16:00.000000 viresclient-0.9.0/README.rst
--rw-rw-r--   0 ash       (1000) ash       (1000)       38 2021-08-24 21:43:43.474626 viresclient-0.9.0/setup.cfg
--rw-r--r--   0 ash       (1000) ash       (1000)     2882 2021-08-23 14:16:00.000000 viresclient-0.9.0/setup.py
-drwxrwxr-x   0 ash       (1000) ash       (1000)        0 2021-08-24 21:43:43.470626 viresclient-0.9.0/test/
--rw-rw-r--   0 ash       (1000) ash       (1000)        0 2021-08-23 13:57:32.000000 viresclient-0.9.0/test/__init__.py
--rw-rw-r--   0 ash       (1000) ash       (1000)      388 2021-08-23 13:57:32.000000 viresclient-0.9.0/test/conftest.py
--rw-rw-r--   0 ash       (1000) ash       (1000)      751 2021-08-23 13:57:32.000000 viresclient-0.9.0/test/test_ClientRequest.py
--rw-rw-r--   0 ash       (1000) ash       (1000)     8568 2021-08-23 13:57:32.000000 viresclient-0.9.0/test/test_ReturnedData.py
-drwxrwxr-x   0 ash       (1000) ash       (1000)        0 2021-08-24 21:43:43.470626 viresclient-0.9.0/viresclient/
--rw-r--r--   0 ash       (1000) ash       (1000)     1833 2021-08-24 21:40:31.000000 viresclient-0.9.0/viresclient/__init__.py
-drwxrwxr-x   0 ash       (1000) ash       (1000)        0 2021-08-24 21:43:43.470626 viresclient-0.9.0/viresclient/_api/
--rw-rw-r--   0 ash       (1000) ash       (1000)        0 2021-08-23 13:57:32.000000 viresclient-0.9.0/viresclient/_api/__init__.py
--rw-rw-r--   0 ash       (1000) ash       (1000)     3319 2021-08-23 13:57:32.000000 viresclient-0.9.0/viresclient/_api/token.py
--rw-rw-r--   0 ash       (1000) ash       (1000)     7667 2021-08-23 13:57:32.000000 viresclient-0.9.0/viresclient/_api/upload.py
--rw-r--r--   0 ash       (1000) ash       (1000)    24730 2021-08-24 21:40:31.000000 viresclient-0.9.0/viresclient/_client.py
--rw-rw-r--   0 ash       (1000) ash       (1000)     6091 2021-08-23 13:57:32.000000 viresclient-0.9.0/viresclient/_client_aeolus.py
--rw-r--r--   0 ash       (1000) ash       (1000)    63383 2021-08-24 21:40:31.000000 viresclient-0.9.0/viresclient/_client_swarm.py
--rw-r--r--   0 ash       (1000) ash       (1000)     9638 2021-08-24 21:40:31.000000 viresclient-0.9.0/viresclient/_config.py
-drwxrwxr-x   0 ash       (1000) ash       (1000)        0 2021-08-24 21:43:43.470626 viresclient-0.9.0/viresclient/_data/
--rw-r--r--   0 ash       (1000) ash       (1000)      167 2021-08-23 14:18:15.000000 viresclient-0.9.0/viresclient/_data/__init__.py
--rw-r--r--   0 ash       (1000) ash       (1000)     4946 2021-08-23 14:28:32.000000 viresclient-0.9.0/viresclient/_data/config_swarm.json
--rw-r--r--   0 ash       (1000) ash       (1000)    27383 2021-08-24 21:40:31.000000 viresclient-0.9.0/viresclient/_data_handling.py
-drwxrwxr-x   0 ash       (1000) ash       (1000)        0 2021-08-24 21:43:43.474626 viresclient-0.9.0/viresclient/_wps/
--rw-rw-r--   0 ash       (1000) ash       (1000)        0 2021-08-23 13:57:32.000000 viresclient-0.9.0/viresclient/_wps/__init__.py
--rw-rw-r--   0 ash       (1000) ash       (1000)     1832 2021-08-23 13:57:32.000000 viresclient-0.9.0/viresclient/_wps/environment.py
--rw-rw-r--   0 ash       (1000) ash       (1000)     2087 2021-08-23 13:57:32.000000 viresclient-0.9.0/viresclient/_wps/http_util.py
--rw-rw-r--   0 ash       (1000) ash       (1000)     2643 2021-08-23 13:57:32.000000 viresclient-0.9.0/viresclient/_wps/log_util.py
-drwxrwxr-x   0 ash       (1000) ash       (1000)        0 2021-08-24 21:43:43.474626 viresclient-0.9.0/viresclient/_wps/templates/
--rw-rw-r--   0 ash       (1000) ash       (1000)     3659 2021-08-23 13:57:32.000000 viresclient-0.9.0/viresclient/_wps/templates/vires_aeolus_fetch_filtered_data_async.xml
--rw-rw-r--   0 ash       (1000) ash       (1000)     2292 2021-08-23 13:57:32.000000 viresclient-0.9.0/viresclient/_wps/templates/vires_fetch_filtered_data.xml
--rw-rw-r--   0 ash       (1000) ash       (1000)     2402 2021-08-23 13:57:32.000000 viresclient-0.9.0/viresclient/_wps/templates/vires_fetch_filtered_data_async.xml
--rw-r--r--   0 ash       (1000) ash       (1000)     1015 2021-08-23 14:16:00.000000 viresclient-0.9.0/viresclient/_wps/templates/vires_getTimeData.xml
--rw-rw-r--   0 ash       (1000) ash       (1000)      877 2021-08-23 13:57:32.000000 viresclient-0.9.0/viresclient/_wps/templates/vires_get_model_info.xml
--rw-rw-r--   0 ash       (1000) ash       (1000)     1022 2021-08-23 13:57:32.000000 viresclient-0.9.0/viresclient/_wps/templates/vires_get_observatories.xml
--rw-rw-r--   0 ash       (1000) ash       (1000)      392 2021-08-23 13:57:32.000000 viresclient-0.9.0/viresclient/_wps/templates/vires_list_jobs.xml
--rw-rw-r--   0 ash       (1000) ash       (1000)      565 2021-08-23 13:57:32.000000 viresclient-0.9.0/viresclient/_wps/templates/vires_remove_job.xml
--rw-r--r--   0 ash       (1000) ash       (1000)     1231 2021-08-24 21:40:31.000000 viresclient-0.9.0/viresclient/_wps/templates/vires_times_from_orbits.xml
--rw-rw-r--   0 ash       (1000) ash       (1000)     8547 2021-08-23 13:57:32.000000 viresclient-0.9.0/viresclient/_wps/time_util.py
--rw-rw-r--   0 ash       (1000) ash       (1000)    11932 2021-08-23 13:57:32.000000 viresclient-0.9.0/viresclient/_wps/wps.py
--rw-rw-r--   0 ash       (1000) ash       (1000)     2891 2021-08-23 13:57:32.000000 viresclient-0.9.0/viresclient/_wps/wps_vires.py
-drwxrwxr-x   0 ash       (1000) ash       (1000)        0 2021-08-24 21:43:43.474626 viresclient-0.9.0/viresclient/commands/
--rw-rw-r--   0 ash       (1000) ash       (1000)        0 2021-08-23 13:57:32.000000 viresclient-0.9.0/viresclient/commands/__init__.py
--rw-rw-r--   0 ash       (1000) ash       (1000)     2489 2021-08-23 13:57:32.000000 viresclient-0.9.0/viresclient/commands/common.py
--rw-r--r--   0 ash       (1000) ash       (1000)     4473 2021-08-24 21:40:31.000000 viresclient-0.9.0/viresclient/commands/configuration.py
--rw-rw-r--   0 ash       (1000) ash       (1000)     7430 2021-08-23 13:57:32.000000 viresclient-0.9.0/viresclient/commands/upload.py
--rw-r--r--   0 ash       (1000) ash       (1000)     3720 2021-08-24 21:40:31.000000 viresclient-0.9.0/viresclient/commands/viresclient.py
-drwxrwxr-x   0 ash       (1000) ash       (1000)        0 2021-08-24 21:43:43.470626 viresclient-0.9.0/viresclient.egg-info/
--rw-r--r--   0 ash       (1000) ash       (1000)     6349 2021-08-24 21:43:43.000000 viresclient-0.9.0/viresclient.egg-info/PKG-INFO
--rw-r--r--   0 ash       (1000) ash       (1000)     1494 2021-08-24 21:43:43.000000 viresclient-0.9.0/viresclient.egg-info/SOURCES.txt
--rw-r--r--   0 ash       (1000) ash       (1000)        1 2021-08-24 21:43:43.000000 viresclient-0.9.0/viresclient.egg-info/dependency_links.txt
--rw-r--r--   0 ash       (1000) ash       (1000)       72 2021-08-24 21:43:43.000000 viresclient-0.9.0/viresclient.egg-info/entry_points.txt
--rw-r--r--   0 ash       (1000) ash       (1000)      149 2021-08-24 21:43:43.000000 viresclient-0.9.0/viresclient.egg-info/requires.txt
--rw-r--r--   0 ash       (1000) ash       (1000)       17 2021-08-24 21:43:43.000000 viresclient-0.9.0/viresclient.egg-info/top_level.txt
+drwxrwxr-x   0 ash       (1000) ash       (1000)        0 2021-10-07 21:35:57.528681 viresclient-0.9.1/
+-rw-rw-r--   0 ash       (1000) ash       (1000)     1078 2021-08-23 13:57:32.000000 viresclient-0.9.1/LICENSE
+-rw-rw-r--   0 ash       (1000) ash       (1000)     6349 2021-10-07 21:35:57.528681 viresclient-0.9.1/PKG-INFO
+-rw-r--r--   0 ash       (1000) ash       (1000)     5172 2021-08-23 14:16:00.000000 viresclient-0.9.1/README.rst
+-rw-rw-r--   0 ash       (1000) ash       (1000)       38 2021-10-07 21:35:57.528681 viresclient-0.9.1/setup.cfg
+-rw-r--r--   0 ash       (1000) ash       (1000)     2882 2021-08-23 14:16:00.000000 viresclient-0.9.1/setup.py
+drwxrwxr-x   0 ash       (1000) ash       (1000)        0 2021-10-07 21:35:57.528681 viresclient-0.9.1/test/
+-rw-rw-r--   0 ash       (1000) ash       (1000)        0 2021-08-23 13:57:32.000000 viresclient-0.9.1/test/__init__.py
+-rw-rw-r--   0 ash       (1000) ash       (1000)      388 2021-08-23 13:57:32.000000 viresclient-0.9.1/test/conftest.py
+-rw-rw-r--   0 ash       (1000) ash       (1000)      751 2021-08-23 13:57:32.000000 viresclient-0.9.1/test/test_ClientRequest.py
+-rw-rw-r--   0 ash       (1000) ash       (1000)     8568 2021-10-06 20:45:11.000000 viresclient-0.9.1/test/test_ReturnedData.py
+drwxrwxr-x   0 ash       (1000) ash       (1000)        0 2021-10-07 21:35:57.528681 viresclient-0.9.1/viresclient/
+-rw-rw-r--   0 ash       (1000) ash       (1000)     1833 2021-10-07 21:16:52.000000 viresclient-0.9.1/viresclient/__init__.py
+drwxrwxr-x   0 ash       (1000) ash       (1000)        0 2021-10-07 21:35:57.528681 viresclient-0.9.1/viresclient/_api/
+-rw-rw-r--   0 ash       (1000) ash       (1000)        0 2021-08-23 13:57:32.000000 viresclient-0.9.1/viresclient/_api/__init__.py
+-rw-rw-r--   0 ash       (1000) ash       (1000)     3319 2021-08-23 13:57:32.000000 viresclient-0.9.1/viresclient/_api/token.py
+-rw-rw-r--   0 ash       (1000) ash       (1000)     7667 2021-08-23 13:57:32.000000 viresclient-0.9.1/viresclient/_api/upload.py
+-rw-rw-r--   0 ash       (1000) ash       (1000)    24657 2021-10-07 21:13:32.000000 viresclient-0.9.1/viresclient/_client.py
+-rw-rw-r--   0 ash       (1000) ash       (1000)     6091 2021-10-06 22:28:26.000000 viresclient-0.9.1/viresclient/_client_aeolus.py
+-rw-rw-r--   0 ash       (1000) ash       (1000)    66998 2021-10-07 21:15:39.000000 viresclient-0.9.1/viresclient/_client_swarm.py
+-rw-r--r--   0 ash       (1000) ash       (1000)     9638 2021-08-24 21:40:31.000000 viresclient-0.9.1/viresclient/_config.py
+drwxrwxr-x   0 ash       (1000) ash       (1000)        0 2021-10-07 21:35:57.528681 viresclient-0.9.1/viresclient/_data/
+-rw-r--r--   0 ash       (1000) ash       (1000)      167 2021-08-23 14:18:15.000000 viresclient-0.9.1/viresclient/_data/__init__.py
+-rw-r--r--   0 ash       (1000) ash       (1000)     4946 2021-08-23 14:28:32.000000 viresclient-0.9.1/viresclient/_data/config_swarm.json
+-rw-rw-r--   0 ash       (1000) ash       (1000)    27635 2021-10-07 21:16:20.000000 viresclient-0.9.1/viresclient/_data_handling.py
+drwxrwxr-x   0 ash       (1000) ash       (1000)        0 2021-10-07 21:35:57.528681 viresclient-0.9.1/viresclient/_wps/
+-rw-rw-r--   0 ash       (1000) ash       (1000)        0 2021-08-23 13:57:32.000000 viresclient-0.9.1/viresclient/_wps/__init__.py
+-rw-rw-r--   0 ash       (1000) ash       (1000)     1832 2021-08-23 13:57:32.000000 viresclient-0.9.1/viresclient/_wps/environment.py
+-rw-rw-r--   0 ash       (1000) ash       (1000)     2087 2021-08-23 13:57:32.000000 viresclient-0.9.1/viresclient/_wps/http_util.py
+-rw-rw-r--   0 ash       (1000) ash       (1000)     2643 2021-08-23 13:57:32.000000 viresclient-0.9.1/viresclient/_wps/log_util.py
+drwxrwxr-x   0 ash       (1000) ash       (1000)        0 2021-10-07 21:35:57.528681 viresclient-0.9.1/viresclient/_wps/templates/
+-rw-rw-r--   0 ash       (1000) ash       (1000)     3659 2021-08-23 13:57:32.000000 viresclient-0.9.1/viresclient/_wps/templates/vires_aeolus_fetch_filtered_data_async.xml
+-rw-rw-r--   0 ash       (1000) ash       (1000)     2292 2021-08-23 13:57:32.000000 viresclient-0.9.1/viresclient/_wps/templates/vires_fetch_filtered_data.xml
+-rw-rw-r--   0 ash       (1000) ash       (1000)     2402 2021-08-23 13:57:32.000000 viresclient-0.9.1/viresclient/_wps/templates/vires_fetch_filtered_data_async.xml
+-rw-r--r--   0 ash       (1000) ash       (1000)     1015 2021-08-23 14:16:00.000000 viresclient-0.9.1/viresclient/_wps/templates/vires_getTimeData.xml
+-rw-rw-r--   0 ash       (1000) ash       (1000)     1983 2021-10-07 21:13:32.000000 viresclient-0.9.1/viresclient/_wps/templates/vires_get_conjunctions.xml
+-rw-rw-r--   0 ash       (1000) ash       (1000)      877 2021-08-23 13:57:32.000000 viresclient-0.9.1/viresclient/_wps/templates/vires_get_model_info.xml
+-rw-rw-r--   0 ash       (1000) ash       (1000)     1022 2021-08-23 13:57:32.000000 viresclient-0.9.1/viresclient/_wps/templates/vires_get_observatories.xml
+-rw-rw-r--   0 ash       (1000) ash       (1000)      392 2021-08-23 13:57:32.000000 viresclient-0.9.1/viresclient/_wps/templates/vires_list_jobs.xml
+-rw-rw-r--   0 ash       (1000) ash       (1000)      565 2021-08-23 13:57:32.000000 viresclient-0.9.1/viresclient/_wps/templates/vires_remove_job.xml
+-rw-r--r--   0 ash       (1000) ash       (1000)     1231 2021-08-24 21:40:31.000000 viresclient-0.9.1/viresclient/_wps/templates/vires_times_from_orbits.xml
+-rw-rw-r--   0 ash       (1000) ash       (1000)     8547 2021-08-23 13:57:32.000000 viresclient-0.9.1/viresclient/_wps/time_util.py
+-rw-rw-r--   0 ash       (1000) ash       (1000)    11932 2021-08-23 13:57:32.000000 viresclient-0.9.1/viresclient/_wps/wps.py
+-rw-rw-r--   0 ash       (1000) ash       (1000)     2891 2021-08-23 13:57:32.000000 viresclient-0.9.1/viresclient/_wps/wps_vires.py
+drwxrwxr-x   0 ash       (1000) ash       (1000)        0 2021-10-07 21:35:57.528681 viresclient-0.9.1/viresclient/commands/
+-rw-rw-r--   0 ash       (1000) ash       (1000)        0 2021-08-23 13:57:32.000000 viresclient-0.9.1/viresclient/commands/__init__.py
+-rw-rw-r--   0 ash       (1000) ash       (1000)     2489 2021-08-23 13:57:32.000000 viresclient-0.9.1/viresclient/commands/common.py
+-rw-r--r--   0 ash       (1000) ash       (1000)     4473 2021-08-24 21:40:31.000000 viresclient-0.9.1/viresclient/commands/configuration.py
+-rw-rw-r--   0 ash       (1000) ash       (1000)     7430 2021-08-23 13:57:32.000000 viresclient-0.9.1/viresclient/commands/upload.py
+-rw-r--r--   0 ash       (1000) ash       (1000)     3720 2021-08-24 21:40:31.000000 viresclient-0.9.1/viresclient/commands/viresclient.py
+drwxrwxr-x   0 ash       (1000) ash       (1000)        0 2021-10-07 21:35:57.528681 viresclient-0.9.1/viresclient.egg-info/
+-rw-r--r--   0 ash       (1000) ash       (1000)     6349 2021-10-07 21:35:57.000000 viresclient-0.9.1/viresclient.egg-info/PKG-INFO
+-rw-r--r--   0 ash       (1000) ash       (1000)     1556 2021-10-07 21:35:57.000000 viresclient-0.9.1/viresclient.egg-info/SOURCES.txt
+-rw-r--r--   0 ash       (1000) ash       (1000)        1 2021-10-07 21:35:57.000000 viresclient-0.9.1/viresclient.egg-info/dependency_links.txt
+-rw-r--r--   0 ash       (1000) ash       (1000)       72 2021-10-07 21:35:57.000000 viresclient-0.9.1/viresclient.egg-info/entry_points.txt
+-rw-r--r--   0 ash       (1000) ash       (1000)      149 2021-10-07 21:35:57.000000 viresclient-0.9.1/viresclient.egg-info/requires.txt
+-rw-r--r--   0 ash       (1000) ash       (1000)       17 2021-10-07 21:35:57.000000 viresclient-0.9.1/viresclient.egg-info/top_level.txt
```

### Comparing `viresclient-0.9.0/PKG-INFO` & `viresclient-0.9.1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 1.2
 Name: viresclient
-Version: 0.9.0
+Version: 0.9.1
 Summary: A Python client for interacting with a VirES server
 Home-page: https://github.com/ESA-VirES/VirES-Python-Client
 Author: Ashley Smith
 Author-email: ashley.smith@ed.ac.uk
 License: EOX licence (MIT style)
 Description: 
         .. image:: https://badge.fury.io/py/viresclient.svg
```

### Comparing `viresclient-0.9.0/README.rst` & `viresclient-0.9.1/README.rst`

 * *Files identical despite different names*

### Comparing `viresclient-0.9.0/setup.py` & `viresclient-0.9.1/setup.py`

 * *Files identical despite different names*

### Comparing `viresclient-0.9.0/test/test_ClientRequest.py` & `viresclient-0.9.1/test/test_ClientRequest.py`

 * *Files identical despite different names*

### Comparing `viresclient-0.9.0/test/test_ReturnedData.py` & `viresclient-0.9.1/test/test_ReturnedData.py`

 * *Files identical despite different names*

### Comparing `viresclient-0.9.0/viresclient/__init__.py` & `viresclient-0.9.1/viresclient/__init__.py`

 * *Files 5% similar despite different names*

```diff
@@ -33,8 +33,8 @@
 from ._data_handling import ReturnedData
 from ._data_handling import ReturnedDataFile
 from ._api.upload import DataUpload
 from ._api.token import TokenManager
 from . import _data
 
 
-__version__ = "0.9.0"
+__version__ = "0.9.1"
```

### Comparing `viresclient-0.9.0/viresclient/_api/token.py` & `viresclient-0.9.1/viresclient/_api/token.py`

 * *Files identical despite different names*

### Comparing `viresclient-0.9.0/viresclient/_api/upload.py` & `viresclient-0.9.1/viresclient/_api/upload.py`

 * *Files identical despite different names*

### Comparing `viresclient-0.9.0/viresclient/_client.py` & `viresclient-0.9.1/viresclient/_client.py`

 * *Files 0% similar despite different names*

```diff
@@ -243,21 +243,21 @@
             self.refresh_tqdm()
 
 
 class ClientRequest(object):
     """Base class handling the requests to and downloads from the server.
     """
 
-    def __init__(self, url=None, username=None, password=None, token=None,
+    def __init__(self, url=None, token=None,
                  config=None, logging_level="NO_LOGGING", server_type=None):
 
         # Check and prompt for token if not already set, then store in config
         # Try to only do this if running in a notebook
         if IN_JUPYTER:
-            if not ((username and password) or token or config):
+            if not (token or config):
                 cc = ClientConfig()
                 # Use production url if none chosen
                 url = url or cc.default_url or "https://vires.services/ows"
                 if not cc.get_site_config(url):
                     print("Access token not found.")
                     set_token(url)
 
@@ -271,15 +271,15 @@
         self._downloaded_chunk_sizes = []
 
         logging_level = get_log_level(logging_level)
         self._logger = getLogger()
         set_stream_handler(self._logger, logging_level)
 
         self._wps_service = self._create_service_proxy_(
-            config, url, username, password, token
+            config, url, None, None, token
         )
         # Test if the token is working; re-enter if not
         if IN_JUPYTER:
             invalid_token = True
             attempts = 0
             while invalid_token:
                 try:
@@ -288,15 +288,15 @@
                 except AuthenticationError:
                     print("Token invalid.")
                     attempts += 1
                     if attempts > 3:
                         raise AuthenticationError(AUTH_ERROR_TEXT)
                     set_token(url)
                     self._wps_service = self._create_service_proxy_(
-                        config, url, username, password, token
+                        config, url, None, None, token
                     )
 
     def _create_service_proxy_(self, config, url, username, password, token):
 
         if not isinstance(config, ClientConfig):
             config = ClientConfig(config)
```

### Comparing `viresclient-0.9.0/viresclient/_client_aeolus.py` & `viresclient-0.9.1/viresclient/_client_aeolus.py`

 * *Files identical despite different names*

### Comparing `viresclient-0.9.0/viresclient/_client_swarm.py` & `viresclient-0.9.1/viresclient/_client_swarm.py`

 * *Files 4% similar despite different names*

```diff
@@ -19,15 +19,16 @@
 
 TEMPLATE_FILES = {
     **TEMPLATE_FILES,
     'sync': "vires_fetch_filtered_data.xml",
     'async': "vires_fetch_filtered_data_async.xml",
     'model_info': "vires_get_model_info.xml",
     'times_from_orbits': "vires_times_from_orbits.xml",
-    'get_observatories': 'vires_get_observatories.xml'
+    'get_observatories': 'vires_get_observatories.xml',
+    'get_conjunctions': 'vires_get_conjunctions.xml',
 }
 
 REFERENCES = {
     'General Swarm': (" Swarm Data Handbook, https://earth.esa.int/web/guest/missions/esa-eo-missions/swarm/data-handbook ",
                       " The Swarm Satellite Constellation Application and Research Facility (SCARF) and Swarm data products, https://doi.org/10.5047/eps.2013.07.001 ",
                       " Swarm Science Data Processing and Products (2013), https://link.springer.com/journal/40623/65/11/page/1 ",
                       " Special issue “Swarm science results after 2 years in space (2016), https://www.springeropen.com/collections/swsr ",
@@ -397,28 +398,30 @@
         request.available_collections(details=False)
         request.available_measurements("MAG")
         request.available_auxiliaries()
         request.available_models(details=False)
 
     Args:
         url (str):
-        username (str):
-        password (str):
         token (str):
         config (str or ClientConfig):
         logging_level (str):
 
     """
     MISSION_SPACECRAFTS = {
         'Swarm': ['A', 'B', 'C'],
         'GRACE': ['1', '2'],
         'GRACE-FO': ['1', '2'],
         'CryoSat-2': None,
     }
 
+    CONJUNCTION_MISISON_SPACECRAFT_PAIRS = {
+        (('Swarm', 'A'), ('Swarm', 'B')),
+    }
+
     COLLECTIONS = {
         "MAG": ["SW_OPER_MAG{}_LR_1B".format(x) for x in "ABC"],
         "MAG_HR": ["SW_OPER_MAG{}_HR_1B".format(x) for x in "ABC"],
         "EFI": ["SW_OPER_EFI{}_LP_1B".format(x) for x in "ABC"],
         "IBI": ["SW_OPER_IBI{}TMS_2F".format(x) for x in "ABC"],
         "TEC": ["SW_OPER_TEC{}TMS_2F".format(x) for x in "ABC"],
         "FAC": ["SW_OPER_FAC{}TMS_2F".format(x) for x in "ABC_"],
@@ -724,15 +727,15 @@
             "Position_Quality", "PointType",
         ],
         "MAG_CS": [
             "F", "B_NEC", "B_mod_NEC", "B_NEC1", "B_NEC2", "B_NEC3",
             "B_FGM1", "B_FGM2", "B_FGM3", "q_NEC_CRF", "q_error",
         ],
         "MAG_GRACE": [
-            "F", "B_NEC", "B_NEC_raw", "B_FGM", "B_mod_NEC",
+            "F", "B_NEC", "B_NEC_raw", "B_FGM",
             "q_NEC_CRF", "q_error",
         ],
         "MAG_GFO": [
             "F", "B_NEC", "B_FGM", "dB_MTQ_FGM", "dB_XI_FGM", "dB_NY_FGM", "dB_BT_FGM",
             "dB_ST_FGM", "dB_SA_FGM", "dB_BAT_FGM", "q_NEC_FGM", "B_FLAG",
         ],
         "MOD_SC": [],
@@ -766,18 +769,18 @@
         "MMA_SHA_2F-Primary", "MMA_SHA_2F-Secondary",
         "MIO_SHA_2C-Primary", "MIO_SHA_2C-Secondary",
         "MIO_SHA_2D-Primary", "MIO_SHA_2D-Secondary",
         "AMPS",
         "MCO_SHA_2X", "CHAOS", "CHAOS-MMA", "MMA_SHA_2C", "MMA_SHA_2F", "MIO_SHA_2C", "MIO_SHA_2D", "SwarmCI",
     ]
 
-    def __init__(self, url=None, username=None, password=None, token=None,
+    def __init__(self, url=None, token=None,
                  config=None, logging_level="NO_LOGGING"):
         super().__init__(
-            url, username, password, token, config, logging_level,
+            url, token, config, logging_level,
             server_type="Swarm"
             )
 
         self._available = self._get_available_data()
         self._request_inputs = SwarmWPSInputs()
         self._templatefiles = TEMPLATE_FILES
         self._filterlist = []
@@ -1305,24 +1308,46 @@
                 "'Swarm', spacecraft)",
                 FutureWarning,
             )
 
         start_orbit = int(start_orbit)
         end_orbit = int(end_orbit)
 
-        if mission not in self.MISSION_SPACECRAFTS:
-            raise ValueError(
-                f"Invalid mission {mission}!"
-                f"Allowed options are: {','.join(self.MISSION_SPACECRAFTS)}"
-            )
+        # Change to spacecraft = "A" etc. for this request
+        spacecraft = self._fix_spacecraft(mission, spacecraft)
+        self._check_mission_spacecraft(mission, spacecraft)
+
+        templatefile = TEMPLATE_FILES["times_from_orbits"]
+        template = JINJA2_ENVIRONMENT.get_template(templatefile)
+        request = template.render(
+            mission=mission,
+            spacecraft=spacecraft,
+            start_orbit=start_orbit,
+            end_orbit=end_orbit
+        ).encode('UTF-8')
+        response = self._get(
+            request, asynchronous=False, show_progress=False)
+        responsedict = json.loads(response.decode('UTF-8'))
+        start_time = parse_datetime(responsedict['start_time'])
+        end_time = parse_datetime(responsedict['end_time'])
+        return start_time, end_time
 
+    def _fix_spacecraft(self, mission, spacecraft):
         # Change to spacecraft = "A" etc. for this request
         spacecraft = str(spacecraft) if spacecraft is not None else None
         if mission == "Swarm" and spacecraft in ("Alpha", "Bravo", "Charlie"):
             spacecraft = spacecraft[0]
+        return spacecraft
+
+    def _check_mission_spacecraft(self, mission, spacecraft):
+        if mission not in self.MISSION_SPACECRAFTS:
+            raise ValueError(
+                f"Invalid mission {mission}!"
+                f"Allowed options are: {','.join(self.MISSION_SPACECRAFTS)}"
+            )
 
         if self.MISSION_SPACECRAFTS[mission]:
             # missions with required spacecraft id
             if not spacecraft:
                 raise ValueError(
                     f"The {mission} spacecraft is required!"
                     f"Allowed options are: {','.join(self.MISSION_SPACECRAFTS[mission])}"
@@ -1335,28 +1360,14 @@
 
         elif spacecraft: # mission without spacecraft id
             raise ValueError(
                 f"No {mission} spacecraft shall be specified! "
                 "Set spacecraft to None."
             )
 
-        templatefile = TEMPLATE_FILES["times_from_orbits"]
-        template = JINJA2_ENVIRONMENT.get_template(templatefile)
-        request = template.render(
-            mission=mission,
-            spacecraft=spacecraft,
-            start_orbit=start_orbit,
-            end_orbit=end_orbit
-        ).encode('UTF-8')
-        response = self._get(
-            request, asynchronous=False, show_progress=False)
-        responsedict = json.loads(response.decode('UTF-8'))
-        start_time = parse_datetime(responsedict['start_time'])
-        end_time = parse_datetime(responsedict['end_time'])
-        return start_time, end_time
 
     def get_orbit_number(self, spacecraft, input_time, mission="Swarm"):
         """Translate a time to an orbit number.
 
         Args:
             spacecraft (str):
                     Swarm: one of ('A','B','C') or ("Alpha", "Bravo", "Charlie")
@@ -1502,7 +1513,93 @@
                 if deprecated_model in model:
                     deprecated_models.append(deprecated_model)
                     break
         for deprecated_model in deprecated_models:
             print("WARNING: Model {} is deprecated. {}".format(
                 deprecated_model, DEPRECATED_MODELS[deprecated_model]
             ), file=sys.stdout)
+
+
+    def get_conjunctions(self, start_time=None, end_time=None, threshold=1.0,
+                         spacecraft1='A', spacecraft2='B',
+                         mission1='Swarm', mission2='Swarm'):
+        """ Get times of the spacecraft conjunctions. Currently available for
+        the following spacecraft pairs:
+          - Swarm-A/Swarm-B
+
+        Args:
+            start_time (datetime / ISO_8601 string): optional start time
+            end_time (datetime / ISO_8601 string): optional end time
+            threshold (float): optional maximum allowed angular separation
+                 in degrees; by default set to 1; allowed values are [0, 180]
+            spacecraft1: identifier of the first spacecraft, default to 'A'
+            spacecraft2: identifier of the second spacecraft, default to 'B'
+            mission1 (str): mission of the first spacecraft, defaults to 'Swarm'
+            mission2 (str): mission of the first spacecraft, defaults to 'Swarm'
+
+        Returns:
+            ReturnedData:
+        """
+        try:
+            start_time = parse_datetime(start_time) if start_time else None
+            end_time = parse_datetime(end_time) if end_time else None
+        except TypeError:
+            raise TypeError(
+                "start_time and end_time must be datetime objects or ISO-8601 "
+                "date/time strings"
+            ) from None
+
+        if not (0 <= threshold <= 180):
+            raise ValueError("Invalid threshold value!")
+
+        spacecraft1 = self._fix_spacecraft(mission1, spacecraft1)
+        spacecraft2 = self._fix_spacecraft(mission2, spacecraft2)
+
+        self._check_mission_spacecraft(mission1, spacecraft1)
+        self._check_mission_spacecraft(mission2, spacecraft2)
+
+        if (mission1, spacecraft1) == (mission2, spacecraft2):
+            raise ValueError(
+                "The first and second spacecraft must not be the same!"
+            )
+
+        spacecraft_pair = tuple(sorted([
+            (mission1, spacecraft1), (mission2, spacecraft2)
+        ]))
+
+        if spacecraft_pair not in self.CONJUNCTION_MISISON_SPACECRAFT_PAIRS:
+            raise ValueError(
+                "Conjunctions not available for the requested "
+                "spacecraft pair {spacecraft_pair}!"
+            )
+
+        templatefile = TEMPLATE_FILES["get_conjunctions"]
+        template = JINJA2_ENVIRONMENT.get_template(templatefile)
+        request = template.render(
+            begin_time=start_time,
+            end_time=end_time,
+            spacecraft1=spacecraft1,
+            spacecraft2=spacecraft2,
+            mission1=mission1,
+            mission2=mission2,
+            threshold=threshold,
+        ).encode('UTF-8')
+
+        show_progress = False
+        leave_progress_bar = False
+        response = ReturnedDataFile(filetype="cdf")
+
+        response_handler = self._response_handler(
+            retdatafile=response,
+            show_progress=show_progress,
+            leave_progress_bar=leave_progress_bar,
+        )
+
+        self._get(
+            request=request,
+            asynchronous=False,
+            show_progress=show_progress,
+            leave_progress_bar=leave_progress_bar,
+            response_handler=response_handler,
+        )
+
+        return response
```

### Comparing `viresclient-0.9.0/viresclient/_config.py` & `viresclient-0.9.1/viresclient/_config.py`

 * *Files identical despite different names*

### Comparing `viresclient-0.9.0/viresclient/_data/config_swarm.json` & `viresclient-0.9.1/viresclient/_data/config_swarm.json`

 * *Files identical despite different names*

### Comparing `viresclient-0.9.0/viresclient/_data_handling.py` & `viresclient-0.9.1/viresclient/_data_handling.py`

 * *Files 1% similar despite different names*

```diff
@@ -212,19 +212,18 @@
         #  (avoids issues with concatenating them)
         #  (this is done in ReturnedData)
         # Initialise dataset with time coordinate
         ds = xarray.Dataset(
             coords={"Timestamp":
                     self._cdftime_to_datetime(self.get_variable("Timestamp"))})
         # Add Spacecraft variable as Categorical to save memory
-        ds["Spacecraft"] = (("Timestamp",), pandas.Categorical(
-            self.get_variable("Spacecraft"), categories=ALLOWED_SPACECRFTS))
-        datanames = set(self.variables)
-        datanames.remove("Timestamp")
-        datanames.remove("Spacecraft")
+        if "Spacecraft" in self.variables:
+            ds["Spacecraft"] = (("Timestamp",), pandas.Categorical(
+                self.get_variable("Spacecraft"), categories=ALLOWED_SPACECRFTS))
+        datanames = set(self.variables) - {"Timestamp", "Spacecraft"}
         # Loop through each variable available and append them to the Dataset,
         #  attaching the Timestamp coordinate to each.
         # Attach dimension names based on the name of the variable,
         #  with coordinate labels if available.
         dims_used = set()
         for dataname in datanames:
             data = self.get_variable(dataname)
@@ -293,48 +292,53 @@
                 Only available for GVO dataset where the "SiteCode"
                 parameter has been requested, or OBS dataset with "IAGA_code"
                 """
             )
         # Create integer "Site" identifier based on SiteCode / IAGA_code
         sites = dict(enumerate(sorted(set(ds[codevar].values))))
         sites_inv = {v: k for k, v in sites.items()}
-        # Identify (V)OBS locations and mapping from integer "Site" identifier
-        pos_vars = ["Longitude", "Latitude", "Radius", codevar]
-        _ds_locs = next(iter(ds[pos_vars].groupby("Timestamp")))[1]
-        if len(sites) > 1:
-            _ds_locs = _ds_locs.drop(("Timestamp")).rename({"Timestamp": "Site"})
+        if len(sites) == 0:
+            _ds_locs = ds
         else:
-            _ds_locs = _ds_locs.drop(("Timestamp")).expand_dims("Site")
-        _ds_locs["Site"] = [sites_inv.get(code) for code in _ds_locs[codevar].values]
-        _ds_locs = _ds_locs.sortby("Site")
+            # Identify (V)OBS locations and mapping from integer "Site" identifier
+            pos_vars = ["Longitude", "Latitude", "Radius", codevar]
+            _ds_locs = next(iter(ds[pos_vars].groupby("Timestamp")))[1]
+            if len(sites) > 1:
+                _ds_locs = _ds_locs.drop(("Timestamp")).rename({"Timestamp": "Site"})
+            else:
+                _ds_locs = _ds_locs.drop(("Timestamp")).expand_dims("Site")
+            _ds_locs["Site"] = [sites_inv.get(code) for code in _ds_locs[codevar].values]
+            _ds_locs = _ds_locs.sortby("Site")
         # Create dataset initialised with the (V)OBS positional info as coords
         # and datavars (empty) reshaped to (Site, Timestamp, ...)
         t = numpy.unique(ds["Timestamp"])
         ds2 = xarray.Dataset(
             coords={
                 "Timestamp": t,
-                codevar: (("Site"), _ds_locs[codevar]),
-                "Latitude": ("Site", _ds_locs["Latitude"]),
-                "Longitude": ("Site", _ds_locs["Longitude"]),
-                "Radius": ("Site", _ds_locs["Radius"]),
+                codevar: (("Site"), _ds_locs[codevar].data),
+                "Latitude": ("Site", _ds_locs["Latitude"].data),
+                "Longitude": ("Site", _ds_locs["Longitude"].data),
+                "Radius": ("Site", _ds_locs["Radius"].data),
                 "NEC": ["N", "E", "C"]
             },
         )
         # (Dropping unused Spacecraft var)
         data_vars = set(ds.data_vars) - {"Latitude", "Longitude", "Radius", codevar, "Spacecraft"}
         N_sites = len(_ds_locs[codevar])
+        # Create empty data variables to be infilled
         for var in data_vars:
             shape = [N_sites, len(t), *ds[var].shape[1:]]
             ds2[var] = ("Site", *ds[var].dims), numpy.empty(shape, dtype=ds[var].dtype)
             ds2[var][...] = None
-        # Loop through each (V)OBS site to insert the datavars into ds2
-        for k, _ds in dict(ds.groupby(codevar)).items():
-            site = sites_inv.get(k)
-            for var in data_vars:
-                ds2[var][site, ...] = _ds[var].values
+        # Loop through each (V)OBS site to infill the data
+        if N_sites != 0:
+            for k, _ds in dict(ds.groupby(codevar)).items():
+                site = sites_inv.get(k)
+                for var in data_vars:
+                    ds2[var][site, ...] = _ds[var].values
         # Revert to using only the "SiteCode"/"IAGA_code" identifier
         ds2 = ds2.set_index({"Site": codevar})
         ds2 = ds2.rename({"Site": codevar})
         return ds2
 
 
 def make_pandas_DataFrame_from_csv(csv_filename):
@@ -517,14 +521,15 @@
         if self.filetype == 'csv':
             raise NotImplementedError("csv to xarray is not supported")
         elif self.filetype == 'cdf':
             with FileReader(self._file) as f:
                 ds = f.as_xarray_dataset(reshape=reshape)
         elif self.filetype == 'nc':
             ds = xarray.open_dataset(self._file.name, group=group)
+        ds.attrs["Sources"] = self.sources
         return ds
 
     @property
     def sources(self):
         with FileReader(self._file) as f:
             sources = f.sources
         return sources
```

### Comparing `viresclient-0.9.0/viresclient/_wps/environment.py` & `viresclient-0.9.1/viresclient/_wps/environment.py`

 * *Files identical despite different names*

### Comparing `viresclient-0.9.0/viresclient/_wps/http_util.py` & `viresclient-0.9.1/viresclient/_wps/http_util.py`

 * *Files identical despite different names*

### Comparing `viresclient-0.9.0/viresclient/_wps/log_util.py` & `viresclient-0.9.1/viresclient/_wps/log_util.py`

 * *Files identical despite different names*

### Comparing `viresclient-0.9.0/viresclient/_wps/templates/vires_aeolus_fetch_filtered_data_async.xml` & `viresclient-0.9.1/viresclient/_wps/templates/vires_aeolus_fetch_filtered_data_async.xml`

 * *Files identical despite different names*

### Comparing `viresclient-0.9.0/viresclient/_wps/templates/vires_fetch_filtered_data.xml` & `viresclient-0.9.1/viresclient/_wps/templates/vires_fetch_filtered_data.xml`

 * *Files identical despite different names*

### Comparing `viresclient-0.9.0/viresclient/_wps/templates/vires_fetch_filtered_data_async.xml` & `viresclient-0.9.1/viresclient/_wps/templates/vires_fetch_filtered_data_async.xml`

 * *Files identical despite different names*

### Comparing `viresclient-0.9.0/viresclient/_wps/templates/vires_getTimeData.xml` & `viresclient-0.9.1/viresclient/_wps/templates/vires_getTimeData.xml`

 * *Files identical despite different names*

### Comparing `viresclient-0.9.0/viresclient/_wps/templates/vires_get_model_info.xml` & `viresclient-0.9.1/viresclient/_wps/templates/vires_get_model_info.xml`

 * *Files identical despite different names*

### Comparing `viresclient-0.9.0/viresclient/_wps/templates/vires_get_observatories.xml` & `viresclient-0.9.1/viresclient/_wps/templates/vires_get_observatories.xml`

 * *Files identical despite different names*

### Comparing `viresclient-0.9.0/viresclient/_wps/templates/vires_remove_job.xml` & `viresclient-0.9.1/viresclient/_wps/templates/vires_remove_job.xml`

 * *Files identical despite different names*

### Comparing `viresclient-0.9.0/viresclient/_wps/templates/vires_times_from_orbits.xml` & `viresclient-0.9.1/viresclient/_wps/templates/vires_times_from_orbits.xml`

 * *Files identical despite different names*

### Comparing `viresclient-0.9.0/viresclient/_wps/time_util.py` & `viresclient-0.9.1/viresclient/_wps/time_util.py`

 * *Files identical despite different names*

### Comparing `viresclient-0.9.0/viresclient/_wps/wps.py` & `viresclient-0.9.1/viresclient/_wps/wps.py`

 * *Files identical despite different names*

### Comparing `viresclient-0.9.0/viresclient/_wps/wps_vires.py` & `viresclient-0.9.1/viresclient/_wps/wps_vires.py`

 * *Files identical despite different names*

### Comparing `viresclient-0.9.0/viresclient/commands/common.py` & `viresclient-0.9.1/viresclient/commands/common.py`

 * *Files identical despite different names*

### Comparing `viresclient-0.9.0/viresclient/commands/configuration.py` & `viresclient-0.9.1/viresclient/commands/configuration.py`

 * *Files identical despite different names*

### Comparing `viresclient-0.9.0/viresclient/commands/upload.py` & `viresclient-0.9.1/viresclient/commands/upload.py`

 * *Files identical despite different names*

### Comparing `viresclient-0.9.0/viresclient/commands/viresclient.py` & `viresclient-0.9.1/viresclient/commands/viresclient.py`

 * *Files identical despite different names*

### Comparing `viresclient-0.9.0/viresclient.egg-info/PKG-INFO` & `viresclient-0.9.1/viresclient.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 1.2
 Name: viresclient
-Version: 0.9.0
+Version: 0.9.1
 Summary: A Python client for interacting with a VirES server
 Home-page: https://github.com/ESA-VirES/VirES-Python-Client
 Author: Ashley Smith
 Author-email: ashley.smith@ed.ac.uk
 License: EOX licence (MIT style)
 Description: 
         .. image:: https://badge.fury.io/py/viresclient.svg
```

### Comparing `viresclient-0.9.0/viresclient.egg-info/SOURCES.txt` & `viresclient-0.9.1/viresclient.egg-info/SOURCES.txt`

 * *Files 5% similar despite different names*

```diff
@@ -1,7 +1,8 @@
+LICENSE
 README.rst
 setup.py
 test/__init__.py
 test/conftest.py
 test/test_ClientRequest.py
 test/test_ReturnedData.py
 viresclient/__init__.py
@@ -28,14 +29,15 @@
 viresclient/_wps/time_util.py
 viresclient/_wps/wps.py
 viresclient/_wps/wps_vires.py
 viresclient/_wps/templates/vires_aeolus_fetch_filtered_data_async.xml
 viresclient/_wps/templates/vires_fetch_filtered_data.xml
 viresclient/_wps/templates/vires_fetch_filtered_data_async.xml
 viresclient/_wps/templates/vires_getTimeData.xml
+viresclient/_wps/templates/vires_get_conjunctions.xml
 viresclient/_wps/templates/vires_get_model_info.xml
 viresclient/_wps/templates/vires_get_observatories.xml
 viresclient/_wps/templates/vires_list_jobs.xml
 viresclient/_wps/templates/vires_remove_job.xml
 viresclient/_wps/templates/vires_times_from_orbits.xml
 viresclient/commands/__init__.py
 viresclient/commands/common.py
```

