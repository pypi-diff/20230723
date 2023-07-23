# Comparing `tmp/storey-1.5.0.tar.gz` & `tmp/storey-1.5.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "/home/runner/work/storey/storey/dist/.tmp-y_domb5g/storey-1.5.0.tar", last modified: Tue Jul 18 09:46:40 2023, max compression
+gzip compressed data, was "/home/runner/work/storey/storey/dist/.tmp-qh38jxq6/storey-1.5.1.tar", last modified: Sun Jul 23 09:49:19 2023, max compression
```

## Comparing `storey-1.5.0.tar` & `storey-1.5.1.tar`

### file list

```diff
@@ -1,61 +1,61 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 09:46:40.000000 storey-1.5.0/
--rw-r--r--   0 runner    (1001) docker     (123)        5 2023-07-18 09:43:39.000000 storey-1.5.0/.dockerignore
--rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-07-18 09:43:39.000000 storey-1.5.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      132 2023-07-18 09:43:39.000000 storey-1.5.0/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     5551 2023-07-18 09:46:40.000000 storey-1.5.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     4522 2023-07-18 09:43:39.000000 storey-1.5.0/README.md
--rw-r--r--   0 runner    (1001) docker     (123)      260 2023-07-18 09:43:39.000000 storey-1.5.0/dev-requirements.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 09:46:40.000000 storey-1.5.0/integration/
--rw-r--r--   0 runner    (1001) docker     (123)      571 2023-07-18 09:43:39.000000 storey-1.5.0/integration/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5863 2023-07-18 09:43:39.000000 storey-1.5.0/integration/conftest.py
--rw-r--r--   0 runner    (1001) docker     (123)     9748 2023-07-18 09:43:39.000000 storey-1.5.0/integration/integration_test_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)   170272 2023-07-18 09:43:39.000000 storey-1.5.0/integration/test_aggregation_integration.py
--rw-r--r--   0 runner    (1001) docker     (123)     9898 2023-07-18 09:43:39.000000 storey-1.5.0/integration/test_azure_filesystem_integration.py
--rw-r--r--   0 runner    (1001) docker     (123)    21737 2023-07-18 09:43:39.000000 storey-1.5.0/integration/test_filesystems_integration.py
--rw-r--r--   0 runner    (1001) docker     (123)    42755 2023-07-18 09:43:39.000000 storey-1.5.0/integration/test_flow_integration.py
--rw-r--r--   0 runner    (1001) docker     (123)     4308 2023-07-18 09:43:39.000000 storey-1.5.0/integration/test_kafka_integration.py
--rw-r--r--   0 runner    (1001) docker     (123)     2984 2023-07-18 09:43:39.000000 storey-1.5.0/integration/test_redis_specific.py
--rw-r--r--   0 runner    (1001) docker     (123)    10369 2023-07-18 09:43:39.000000 storey-1.5.0/integration/test_s3_filesystem_integration.py
--rw-r--r--   0 runner    (1001) docker     (123)      288 2023-07-18 09:43:39.000000 storey-1.5.0/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)       93 2023-07-18 09:46:40.000000 storey-1.5.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     2603 2023-07-18 09:43:39.000000 storey-1.5.0/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 09:46:40.000000 storey-1.5.0/storey/
--rw-r--r--   0 runner    (1001) docker     (123)     3118 2023-07-18 09:46:35.000000 storey-1.5.0/storey/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3709 2023-07-18 09:43:39.000000 storey-1.5.0/storey/aggregation_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)    17706 2023-07-18 09:43:39.000000 storey-1.5.0/storey/aggregations.py
--rw-r--r--   0 runner    (1001) docker     (123)     4692 2023-07-18 09:43:39.000000 storey-1.5.0/storey/dataframe.py
--rw-r--r--   0 runner    (1001) docker     (123)    28065 2023-07-18 09:43:39.000000 storey-1.5.0/storey/drivers.py
--rw-r--r--   0 runner    (1001) docker     (123)    15755 2023-07-18 09:43:39.000000 storey-1.5.0/storey/dtypes.py
--rw-r--r--   0 runner    (1001) docker     (123)    51518 2023-07-18 09:43:39.000000 storey-1.5.0/storey/flow.py
--rw-r--r--   0 runner    (1001) docker     (123)     1828 2023-07-18 09:43:39.000000 storey-1.5.0/storey/queue.py
--rw-r--r--   0 runner    (1001) docker     (123)    27610 2023-07-18 09:43:39.000000 storey-1.5.0/storey/redis_driver.py
--rw-r--r--   0 runner    (1001) docker     (123)    43777 2023-07-18 09:43:39.000000 storey-1.5.0/storey/sources.py
--rw-r--r--   0 runner    (1001) docker     (123)     4755 2023-07-18 09:43:39.000000 storey-1.5.0/storey/sql_driver.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 09:46:40.000000 storey-1.5.0/storey/steps/
--rw-r--r--   0 runner    (1001) docker     (123)      807 2023-07-18 09:43:39.000000 storey-1.5.0/storey/steps/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5418 2023-07-18 09:43:39.000000 storey-1.5.0/storey/steps/assertion.py
--rw-r--r--   0 runner    (1001) docker     (123)      886 2023-07-18 09:43:39.000000 storey-1.5.0/storey/steps/flatten.py
--rw-r--r--   0 runner    (1001) docker     (123)      903 2023-07-18 09:43:39.000000 storey-1.5.0/storey/steps/foreach.py
--rw-r--r--   0 runner    (1001) docker     (123)     1763 2023-07-18 09:43:39.000000 storey-1.5.0/storey/steps/partition.py
--rw-r--r--   0 runner    (1001) docker     (123)     4620 2023-07-18 09:43:39.000000 storey-1.5.0/storey/steps/sample.py
--rw-r--r--   0 runner    (1001) docker     (123)    80029 2023-07-18 09:43:39.000000 storey-1.5.0/storey/table.py
--rw-r--r--   0 runner    (1001) docker     (123)    52048 2023-07-18 09:43:39.000000 storey-1.5.0/storey/targets.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 09:46:40.000000 storey-1.5.0/storey/transformations/
--rw-r--r--   0 runner    (1001) docker     (123)     1564 2023-07-18 09:43:39.000000 storey-1.5.0/storey/transformations/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    11371 2023-07-18 09:43:39.000000 storey-1.5.0/storey/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     8226 2023-07-18 09:43:39.000000 storey-1.5.0/storey/windowed_store.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 09:46:40.000000 storey-1.5.0/storey.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     5551 2023-07-18 09:46:40.000000 storey-1.5.0/storey.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1290 2023-07-18 09:46:40.000000 storey-1.5.0/storey.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-18 09:46:40.000000 storey-1.5.0/storey.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      269 2023-07-18 09:46:40.000000 storey-1.5.0/storey.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       25 2023-07-18 09:46:40.000000 storey-1.5.0/storey.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 09:46:40.000000 storey-1.5.0/tests/
--rw-r--r--   0 runner    (1001) docker     (123)      571 2023-07-18 09:43:39.000000 storey-1.5.0/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)   144374 2023-07-18 09:43:39.000000 storey-1.5.0/tests/test_aggregate_by_key.py
--rw-r--r--   0 runner    (1001) docker     (123)     4853 2023-07-18 09:43:39.000000 storey-1.5.0/tests/test_aggregate_store.py
--rw-r--r--   0 runner    (1001) docker     (123)   131843 2023-07-18 09:43:39.000000 storey-1.5.0/tests/test_flow.py
--rw-r--r--   0 runner    (1001) docker     (123)    11002 2023-07-18 09:43:39.000000 storey-1.5.0/tests/test_steps.py
--rw-r--r--   0 runner    (1001) docker     (123)     2506 2023-07-18 09:43:39.000000 storey-1.5.0/tests/test_types.py
--rw-r--r--   0 runner    (1001) docker     (123)     1459 2023-07-18 09:43:39.000000 storey-1.5.0/tests/test_v3io.py
--rw-r--r--   0 runner    (1001) docker     (123)     2622 2023-07-18 09:43:39.000000 storey-1.5.0/tests/test_windowed_store.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:49:19.000000 storey-1.5.1/
+-rw-r--r--   0 runner    (1001) docker     (123)        5 2023-07-23 09:44:13.000000 storey-1.5.1/.dockerignore
+-rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-07-23 09:44:13.000000 storey-1.5.1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      132 2023-07-23 09:44:13.000000 storey-1.5.1/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     5551 2023-07-23 09:49:19.000000 storey-1.5.1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     4522 2023-07-23 09:44:13.000000 storey-1.5.1/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      260 2023-07-23 09:44:13.000000 storey-1.5.1/dev-requirements.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:49:19.000000 storey-1.5.1/integration/
+-rw-r--r--   0 runner    (1001) docker     (123)      571 2023-07-23 09:44:13.000000 storey-1.5.1/integration/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5863 2023-07-23 09:44:13.000000 storey-1.5.1/integration/conftest.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9748 2023-07-23 09:44:13.000000 storey-1.5.1/integration/integration_test_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)   170272 2023-07-23 09:44:13.000000 storey-1.5.1/integration/test_aggregation_integration.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9898 2023-07-23 09:44:13.000000 storey-1.5.1/integration/test_azure_filesystem_integration.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21737 2023-07-23 09:44:13.000000 storey-1.5.1/integration/test_filesystems_integration.py
+-rw-r--r--   0 runner    (1001) docker     (123)    42956 2023-07-23 09:44:13.000000 storey-1.5.1/integration/test_flow_integration.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4308 2023-07-23 09:44:13.000000 storey-1.5.1/integration/test_kafka_integration.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3179 2023-07-23 09:44:13.000000 storey-1.5.1/integration/test_redis_specific.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10369 2023-07-23 09:44:13.000000 storey-1.5.1/integration/test_s3_filesystem_integration.py
+-rw-r--r--   0 runner    (1001) docker     (123)      288 2023-07-23 09:44:13.000000 storey-1.5.1/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       93 2023-07-23 09:49:19.000000 storey-1.5.1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     2603 2023-07-23 09:44:13.000000 storey-1.5.1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:49:19.000000 storey-1.5.1/storey/
+-rw-r--r--   0 runner    (1001) docker     (123)     3118 2023-07-23 09:49:14.000000 storey-1.5.1/storey/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3709 2023-07-23 09:44:13.000000 storey-1.5.1/storey/aggregation_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17706 2023-07-23 09:44:13.000000 storey-1.5.1/storey/aggregations.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4692 2023-07-23 09:44:13.000000 storey-1.5.1/storey/dataframe.py
+-rw-r--r--   0 runner    (1001) docker     (123)    28065 2023-07-23 09:44:13.000000 storey-1.5.1/storey/drivers.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15755 2023-07-23 09:44:13.000000 storey-1.5.1/storey/dtypes.py
+-rw-r--r--   0 runner    (1001) docker     (123)    51518 2023-07-23 09:44:13.000000 storey-1.5.1/storey/flow.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1828 2023-07-23 09:44:13.000000 storey-1.5.1/storey/queue.py
+-rw-r--r--   0 runner    (1001) docker     (123)    27946 2023-07-23 09:44:13.000000 storey-1.5.1/storey/redis_driver.py
+-rw-r--r--   0 runner    (1001) docker     (123)    43777 2023-07-23 09:44:13.000000 storey-1.5.1/storey/sources.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4755 2023-07-23 09:44:13.000000 storey-1.5.1/storey/sql_driver.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:49:19.000000 storey-1.5.1/storey/steps/
+-rw-r--r--   0 runner    (1001) docker     (123)      807 2023-07-23 09:44:13.000000 storey-1.5.1/storey/steps/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5418 2023-07-23 09:44:13.000000 storey-1.5.1/storey/steps/assertion.py
+-rw-r--r--   0 runner    (1001) docker     (123)      886 2023-07-23 09:44:13.000000 storey-1.5.1/storey/steps/flatten.py
+-rw-r--r--   0 runner    (1001) docker     (123)      903 2023-07-23 09:44:13.000000 storey-1.5.1/storey/steps/foreach.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1763 2023-07-23 09:44:13.000000 storey-1.5.1/storey/steps/partition.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4620 2023-07-23 09:44:13.000000 storey-1.5.1/storey/steps/sample.py
+-rw-r--r--   0 runner    (1001) docker     (123)    80029 2023-07-23 09:44:13.000000 storey-1.5.1/storey/table.py
+-rw-r--r--   0 runner    (1001) docker     (123)    52048 2023-07-23 09:44:13.000000 storey-1.5.1/storey/targets.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:49:19.000000 storey-1.5.1/storey/transformations/
+-rw-r--r--   0 runner    (1001) docker     (123)     1564 2023-07-23 09:44:13.000000 storey-1.5.1/storey/transformations/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11371 2023-07-23 09:44:13.000000 storey-1.5.1/storey/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8226 2023-07-23 09:44:13.000000 storey-1.5.1/storey/windowed_store.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:49:19.000000 storey-1.5.1/storey.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     5551 2023-07-23 09:49:19.000000 storey-1.5.1/storey.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1290 2023-07-23 09:49:19.000000 storey-1.5.1/storey.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 09:49:19.000000 storey-1.5.1/storey.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      269 2023-07-23 09:49:19.000000 storey-1.5.1/storey.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       25 2023-07-23 09:49:19.000000 storey-1.5.1/storey.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:49:19.000000 storey-1.5.1/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)      571 2023-07-23 09:44:13.000000 storey-1.5.1/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)   144374 2023-07-23 09:44:13.000000 storey-1.5.1/tests/test_aggregate_by_key.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4853 2023-07-23 09:44:13.000000 storey-1.5.1/tests/test_aggregate_store.py
+-rw-r--r--   0 runner    (1001) docker     (123)   131843 2023-07-23 09:44:13.000000 storey-1.5.1/tests/test_flow.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11002 2023-07-23 09:44:13.000000 storey-1.5.1/tests/test_steps.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2506 2023-07-23 09:44:13.000000 storey-1.5.1/tests/test_types.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1459 2023-07-23 09:44:13.000000 storey-1.5.1/tests/test_v3io.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2622 2023-07-23 09:44:13.000000 storey-1.5.1/tests/test_windowed_store.py
```

### Comparing `storey-1.5.0/LICENSE` & `storey-1.5.1/LICENSE`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/PKG-INFO` & `storey-1.5.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: storey
-Version: 1.5.0
+Version: 1.5.1
 Summary: Async flows
 Home-page: https://github.com/mlrun/storey
 Author: Iguazio
 Author-email: yaronh@iguazio.com
 License: Apache
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers
```

### Comparing `storey-1.5.0/README.md` & `storey-1.5.1/README.md`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/integration/__init__.py` & `storey-1.5.1/integration/__init__.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/integration/conftest.py` & `storey-1.5.1/integration/conftest.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/integration/integration_test_utils.py` & `storey-1.5.1/integration/integration_test_utils.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/integration/test_aggregation_integration.py` & `storey-1.5.1/integration/test_aggregation_integration.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/integration/test_azure_filesystem_integration.py` & `storey-1.5.1/integration/test_azure_filesystem_integration.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/integration/test_filesystems_integration.py` & `storey-1.5.1/integration/test_filesystems_integration.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/integration/test_flow_integration.py` & `storey-1.5.1/integration/test_flow_integration.py`

 * *Files 1% similar despite different names*

```diff
@@ -107,15 +107,24 @@
 
     from .integration_test_utils import get_redis_client
 
     table_name = setup_teardown_test.table_name
     hash_key = RedisDriver.make_key("storey-test:", table_name, key)
     redis_key = RedisDriver._static_data_key(hash_key)
     redis_fake_server = setup_teardown_test.redis_fake_server
-    values = get_redis_client(redis_fake_server=redis_fake_server).hgetall(redis_key)
+
+    cursor = 0
+    values = {}
+    while True:
+        cursor, v = get_redis_client(redis_fake_server=redis_fake_server).hscan(
+            redis_key, cursor, match=f"[^{RedisDriver.INTERFNAL_FIELD_PREFIX}]*"
+        )
+        values.update(v)
+        if cursor == 0:
+            break
     return {
         RedisDriver.convert_to_str(key): RedisDriver.convert_redis_value_to_python_obj(val)
         for key, val in values.items()
     }
 
 
 def _get_sql_by_key_all_attrs(
```

### Comparing `storey-1.5.0/integration/test_kafka_integration.py` & `storey-1.5.1/integration/test_kafka_integration.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/integration/test_redis_specific.py` & `storey-1.5.1/integration/test_redis_specific.py`

 * *Files 4% similar despite different names*

```diff
@@ -35,15 +35,21 @@
         controller.terminate()
         controller.await_termination()
 
         table_name = f"{table_name}/"
         hash_key = RedisDriver.make_key("storey:", table_name, "key")
         redis_key = RedisDriver._static_data_key(hash_key)
 
-        data = driver.redis.hgetall(redis_key)
+        cursor = 0
+        data = {}
+        while True:
+            cursor, v = driver.redis.hscan(redis_key, cursor, match=f"[^{driver.INTERFNAL_FIELD_PREFIX}]*")
+            data.update(v)
+            if cursor == 0:
+                break
         data_strings = {}
         for key, val in data.items():
             if isinstance(key, bytes):
                 data_strings[key.decode("utf-8")] = val.decode("utf-8")
             else:
                 data_strings[key] = val
```

### Comparing `storey-1.5.0/integration/test_s3_filesystem_integration.py` & `storey-1.5.1/integration/test_s3_filesystem_integration.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/setup.py` & `storey-1.5.1/setup.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/storey/__init__.py` & `storey-1.5.1/storey/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -8,15 +8,15 @@
 #
 # Unless required by applicable law or agreed to in writing, software
 # distributed under the License is distributed on an "AS IS" BASIS,
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 #
-__version__ = "1.5.0"
+__version__ = "1.5.1"
 
 # Importing supported filesystems explicitly so that they will get registered as an fsspec filesystem
 import v3iofs  # noqa: F401
 
 from .aggregations import AggregateByKey, QueryByKey  # noqa: F401
 from .dataframe import ReduceToDataFrame, ToDataFrame  # noqa: F401
 from .drivers import Driver, NoopDriver, V3ioDriver  # noqa: F401
```

### Comparing `storey-1.5.0/storey/aggregation_utils.py` & `storey-1.5.1/storey/aggregation_utils.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/storey/aggregations.py` & `storey-1.5.1/storey/aggregations.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/storey/dataframe.py` & `storey-1.5.1/storey/dataframe.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/storey/drivers.py` & `storey-1.5.1/storey/drivers.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/storey/dtypes.py` & `storey-1.5.1/storey/dtypes.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/storey/flow.py` & `storey-1.5.1/storey/flow.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/storey/queue.py` & `storey-1.5.1/storey/queue.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/storey/redis_driver.py` & `storey-1.5.1/storey/redis_driver.py`

 * *Files 4% similar despite different names*

```diff
@@ -42,22 +42,23 @@
         if not redis_url:
             raise ValueError("no redis_client object or MLRUN_REDIS_URL environment-var provided, aborting")
 
         self._redis_url = redis_url
 
 
 class RedisDriver(NeedsRedisAccess, Driver):
+    INTERFNAL_FIELD_PREFIX = chr(0x1)
     REDIS_TIMEOUT = 5  # Seconds
     REDIS_WATCH_INTERVAL = 1  # Seconds
     DATETIME_FIELD_PREFIX = "_dt:"
     TIMEDELTA_FIELD_PREFIX = "_td:"
     DEFAULT_KEY_PREFIX = "storey:"
-    AGGREGATION_ATTRIBUTE_PREFIX = "moving_windows"
-    AGGREGATION_TIME_ATTRIBUTE_PREFIX = "_"
-    AGGREGATION_PREFIXES = AGGREGATION_TIME_ATTRIBUTE_PREFIX
+    AGGREGATION_ATTRIBUTE_PREFIX = INTERFNAL_FIELD_PREFIX + "aggr_"
+    AGGREGATION_TIME_ATTRIBUTE_PREFIX = INTERFNAL_FIELD_PREFIX + "mtaggr_"
+    OBJECT_MTIME_ATTRIBUTE_PREFIX = INTERFNAL_FIELD_PREFIX + "_mtime_"
 
     def __init__(
         self,
         redis_client: Optional[Union[redis.Redis, redis.cluster.RedisCluster]] = None,
         key_prefix: str = None,
         redis_url: Optional[str] = None,
         use_parallel_operations: bool = True,  # unused
@@ -67,15 +68,15 @@
         if redis_client is not None:
             self._redis = redis_client
         else:
             NeedsRedisAccess.__init__(self, redis_url)
             self._redis = None
 
         self._key_prefix = key_prefix if key_prefix is not None else self.DEFAULT_KEY_PREFIX
-        self._mtime_name = "$_mtime_"
+        self._mtime_name = self.OBJECT_MTIME_ATTRIBUTE_PREFIX
 
     @staticmethod
     def asyncify(fn):
         """Run a synchronous function asynchronously."""
 
         async def inner_fn(*args, **kwargs):
             loop = asyncio.get_event_loop()
@@ -233,33 +234,31 @@
         redis_keys_involved = []
         pending_updates = {}
         condition_expression = None
         additional_data_lua_script = ""
 
         # Static attributes, like "name," "age," -- everything that isn't an agg.
         if additional_data:
-            redis_keys_involved.append(self._static_data_key(redis_key_prefix))
-            additional_data_lua_script = f'local additional_data_key="{self._static_data_key(redis_key_prefix)}";\n'
+            additional_data_lua_script = f'local redis_hash="{self._static_data_key(redis_key_prefix)}";\n'
             for name, value in additional_data.items():
                 expression_value = self._convert_python_obj_to_lua_value(value)
                 # NOTE: This logic assumes that static attributes we're supposed
                 # to delete will appear in the `additional_data` dict with a
                 # "falsey" value. This is the same logic the V3ioDriver uses.
                 if expression_value:
                     additional_data_lua_script = (
                         f"{additional_data_lua_script}redis.call("
-                        f'"HSET",additional_data_key, "{name}", {expression_value});\n'
+                        f'"HSET",redis_hash, "{name}", {expression_value});\n'
                     )
                 else:
                     additional_data_lua_script = (
-                        f'{additional_data_lua_script}redis.call("HDEL",additional_data_key, "{name}");\n'
+                        f'{additional_data_lua_script}redis.call("HDEL",redis_hash, "{name}");\n'
                     )
 
         lua_script = additional_data_lua_script
-        list_attribute_key_aggr = self._list_key(redis_key_prefix, RedisDriver.AGGREGATION_ATTRIBUTE_PREFIX)
 
         if aggregation_element:
             times_updates = {}
             new_cached_times = {}
             initialized_attributes = {}
             if partitioned_by_key:
                 condition_expression = aggregation_element.storage_specific_cache.get(self._mtime_name, None)
@@ -273,17 +272,15 @@
                 "    if input == nil or input == false then return {} end\n"
                 '    for value in string.gmatch(input, "([^,]+)") do\n'
                 "        table.insert(result, value)\n"
                 "    end\n"
                 "    return result\n"
                 "end\n"
             )
-            lua_script = (
-                f"{lua_script}local old_value;local attr_name;\n" f'local aggr_key="{list_attribute_key_aggr}";\n'
-            )
+            lua_script = f"{lua_script}local old_value;local aggr_key;\n"
             lua_script = f"{lua_script}{lua_tonum_function}{lua_strToArr_funct}\n"
             for name, bucket in aggregation_element.aggregation_buckets.items():
                 # Only save raw aggregates, not virtual
                 if bucket.should_persist:
                     # In case we have pending data that spreads over more than 2 windows, discard the old ones.
                     pending_updates[name] = self._discard_old_pending_items(
                         bucket.get_and_flush_pending(), bucket.max_window_millis
@@ -292,51 +289,53 @@
                         # the relevant attribute out of the 2 feature attributes
                         feature_attr = "a" if int(bucket_start_time / bucket.max_window_millis) % 2 == 0 else "b"
 
                         aggr_time_attribute_name = f"{bucket.name}_{feature_attr}"
                         array_time_attribute_key = self._aggregation_time_key(
                             redis_key_prefix, aggr_time_attribute_name
                         )
+                        aggr_mtime_attr_name = (
+                            f"{RedisDriver.AGGREGATION_TIME_ATTRIBUTE_PREFIX}{aggr_time_attribute_name}"
+                        )
 
                         cached_time = bucket.storage_specific_cache.get(array_time_attribute_key, -1)
 
                         expected_time = int(bucket_start_time / bucket.max_window_millis) * bucket.max_window_millis
                         expected_time_expr = self._convert_python_obj_to_lua_value(
                             datetime.fromtimestamp(expected_time / 1000)
                         )
                         lua_index_to_update = 1 + int((bucket_start_time - expected_time) / bucket.period_millis)
 
                         for (
                             aggregation,
                             aggregation_value,
                         ) in aggregation_values.items():
                             list_attribute_name = f"{name}_{aggregation}_{feature_attr}"
-                            if list_attribute_key_aggr not in redis_keys_involved:
-                                redis_keys_involved.append(list_attribute_key_aggr)
-                            lua_script = f'{lua_script}attr_name="{list_attribute_name}";\n'
+                            lua_script = f'{lua_script}\
+                                aggr_key="{RedisDriver.AGGREGATION_ATTRIBUTE_PREFIX}{list_attribute_name}";\n'
 
                             if cached_time < expected_time:
                                 list_attribute_key = self._list_key(redis_key_prefix, list_attribute_name)
                                 if not initialized_attributes.get(list_attribute_key, -1) == expected_time:
                                     initialized_attributes[list_attribute_key] = expected_time
                                     lua_script = (
-                                        f'{lua_script}local t=redis.call("GET","{array_time_attribute_key}");\n'
+                                        f'{lua_script}local t=redis.call("HGET",redis_hash,"{aggr_mtime_attr_name}");\n'
                                         f'if (type(t)~="boolean" and (tonumber(t) < {expected_time})) then '
-                                        f'redis.call("HDEL",aggr_key, attr_name); end;\n'
+                                        f'redis.call("HDEL",redis_hash, aggr_key); end;\n'
                                     )
                                     default_value = self._convert_python_obj_to_redis_value(
                                         aggregation_value.default_value
                                     )
                                     lua_script = (
-                                        f'{lua_script}local curr_agg=redis.call("HGET",aggr_key, attr_name)\n'
+                                        f'{lua_script}local curr_agg=redis.call("HGET",redis_hash, aggr_key)\n'
                                         "local arr=strToArr(curr_agg);\n"
                                         f"local org_arr_len=#arr\n"
                                         f"for i=1,({bucket.total_number_of_buckets}-org_arr_len) \
                                             do arr[#arr+1]={default_value};end;\n"
-                                        f'if org_arr_len ~= #arr then redis.call("HSET", aggr_key, attr_name,\
+                                        f'if org_arr_len ~= #arr then redis.call("HSET", redis_hash, aggr_key,\
                                             table.concat(arr, ",")) end;\n'
                                     )
                                 if array_time_attribute_key not in times_updates:
                                     times_updates[array_time_attribute_key] = expected_time_expr
                                 new_cached_times[name] = (
                                     array_time_attribute_key,
                                     expected_time,
@@ -344,50 +343,51 @@
 
                             # Updating the specific cells
                             if cached_time <= expected_time:
                                 new_value_expression = aggregation_value.aggregate_lua_script(
                                     "old_value", aggregation_value.value
                                 )
                                 lua_script = (
-                                    f'{lua_script}arr=strToArr(redis.call("HGET",aggr_key, attr_name))\n'
+                                    f'{lua_script}arr=strToArr(redis.call("HGET",redis_hash, aggr_key))\n'
                                     f"old_value=tonum(arr[{lua_index_to_update}]);\n"
                                     f'arr[{lua_index_to_update}]=string.format("%.17f",{new_value_expression});\n'
-                                    'redis.call("HSET", aggr_key, attr_name, table.concat(arr, ","))\n'
+                                    'redis.call("HSET", redis_hash, aggr_key, table.concat(arr, ","))\n'
                                 )
-
-                        redis_keys_involved.append(array_time_attribute_key)
-                        lua_script = f'{lua_script}redis.call("SET","{array_time_attribute_key}",{expected_time}); \n'
+                        lua_script = f'{lua_script}\
+                            redis.call("HSET",redis_hash,"{aggr_mtime_attr_name}",{expected_time});'
         return lua_script, condition_expression, pending_updates, redis_keys_involved
 
     async def _save_key(self, container, table_path, key, aggr_item, partitioned_by_key, additional_data):
         redis_key_prefix = self._make_key(container, table_path, key)
+        static_redis_key_prefix = self._static_data_key(redis_key_prefix)
         (
             update_expression,
             mtime_condition,
             pending_updates,
             redis_keys_involved,
         ) = self._build_feature_store_lua_update_script(
             redis_key_prefix, aggr_item, partitioned_by_key, additional_data
         )
         if not update_expression:
             return
         current_time = int(time.time_ns() / 1000)
         if mtime_condition is not None:
             update_expression = (
-                f'if redis.call("HGET", "{redis_key_prefix}","{self._mtime_name}") == "{mtime_condition}" then\n'
-                f'{update_expression}redis.call("HSET","{redis_key_prefix}","{self._mtime_name}",{current_time});\n'
+                f'if redis.call("HGET", "{static_redis_key_prefix}","{self._mtime_name}") == "{mtime_condition}" then\n'
+                f'{update_expression}\
+                    redis.call("HSET","{static_redis_key_prefix}","{self._mtime_name}",{current_time});\n'
                 "return 1;else return 0;end;"
             )
         else:
             update_expression = (
                 f"{update_expression}redis.call("
-                f'"HSET","{redis_key_prefix}","{self._mtime_name}",{current_time});return 1;'
+                f'"HSET","{static_redis_key_prefix}","{self._mtime_name}",{current_time});return 1;'
             )
 
-        redis_keys_involved.append(redis_key_prefix)
+        redis_keys_involved.append(static_redis_key_prefix)
         update_ok = await self.asyncify(self.redis.eval)(
             update_expression, len(redis_keys_involved), *redis_keys_involved
         )
 
         if update_ok:
             if aggr_item:
                 aggr_item.storage_specific_cache[self._mtime_name] = current_time
@@ -398,40 +398,33 @@
                 update_expression,
                 _,
                 _,
                 redis_keys_involved,
             ) = self._build_feature_store_lua_update_script(redis_key_prefix, aggr_item, False, additional_data)
             update_expression = (
                 f"{update_expression}redis.call("
-                f'"HSET","{redis_key_prefix}","{self._mtime_name}",{current_time});return 1;'
+                f'"HSET","{static_redis_key_prefix}","{self._mtime_name}",{current_time});return 1;'
             )
-            redis_keys_involved.append(redis_key_prefix)
 
             update_ok = await RedisDriver.asyncify(self.redis.eval)(
                 update_expression, len(redis_keys_involved), *redis_keys_involved
             )
             if update_ok and aggr_item:
                 await self._fetch_state_by_key(aggr_item, container, table_path, key)
 
     async def _get_all_fields(self, redis_key: str):
-        try:
-            # TODO: This should be HSCAN, not HGETALL, to avoid blocking Redis
-            # with very large hashes.
-            values = await RedisDriver.asyncify(self.redis.hgetall)(redis_key)
-        except redis.ResponseError as e:
-            raise RedisError(f"Failed to get key {redis_key}. Response error was: {e}")
+        values = await self.redis_hscan(redis_key, f"[^{self.INTERFNAL_FIELD_PREFIX}]*")
         res = {
             RedisDriver.convert_to_str(key): RedisDriver.convert_redis_value_to_python_obj(val)
             for key, val in values.items()
-            if not str(key).startswith(RedisDriver.AGGREGATION_PREFIXES)
         }
         return res
 
     async def _get_specific_fields(self, redis_key: str, attributes: List[str]):
-        non_aggregation_attrs = [name for name in attributes if not name.startswith(RedisDriver.AGGREGATION_PREFIXES)]
+        non_aggregation_attrs = [name for name in attributes if not name.startswith(RedisDriver.INTERFNAL_FIELD_PREFIX)]
         try:
             values = await RedisDriver.asyncify(self.redis.hmget)(redis_key, non_aggregation_attrs)
         except redis.ResponseError as e:
             raise RedisError(f"Failed to get key {redis_key}. Response error was: {e}") from e
         if len(values) == 1:
             if values == [None]:
                 return {}
@@ -458,16 +451,20 @@
             values = await self._get_specific_fields(static_key, attributes)
         return values
 
     async def _get_associated_time_attr(self, redis_key_prefix, aggr_name):
         aggr_without_relevant_attr = aggr_name[:-2]
         feature_name_only = aggr_without_relevant_attr[: aggr_without_relevant_attr.rindex("_")]
         feature_with_relevant_attr = f"{feature_name_only}{aggr_name[-2:]}"
+        aggr_mtime_attribute_name = f"{RedisDriver.AGGREGATION_TIME_ATTRIBUTE_PREFIX}{feature_with_relevant_attr}"
+
         associated_time_key = self._aggregation_time_key(redis_key_prefix, feature_with_relevant_attr)
-        time_val = await RedisDriver.asyncify(self.redis.get)(associated_time_key)
+        time_val = await RedisDriver.asyncify(self.redis.hget)(
+            self._static_data_key(redis_key_prefix), aggr_mtime_attribute_name
+        )
         time_val = RedisDriver.convert_to_str(time_val)
 
         try:
             time_in_millis = int(time_val)
         except TypeError as e:
             raise RedisError(f"Invalid associated time attribute: {associated_time_key} " f"-> {time_val}") from e
 
@@ -488,26 +485,27 @@
         """
         redis_key_prefix = self._make_key(container, table_path, key)
         additional_data = await self._get_all_fields(self._static_data_key(redis_key_prefix))
         aggregations = {}
         # Aggregation Redis keys start with the Redis key prefix for this Storey container, table
         # path, and "key," followed by ":aggr_"
         redis_key_prefix = self._make_key(container, table_path, key)
-        aggr_key_prefix = f"{redis_key_prefix}:{RedisDriver.AGGREGATION_ATTRIBUTE_PREFIX}"
-        all_aggr_keys = self.redis.hkeys(aggr_key_prefix)
-        for aggr_key in all_aggr_keys:
-            aggr_key = RedisDriver.convert_to_str(aggr_key)
-            value = await RedisDriver.asyncify(self.redis.hget)(aggr_key_prefix, aggr_key)
+        redis_key = self._static_data_key(redis_key_prefix)
+        values = await self.redis_hscan(redis_key, f"{self.AGGREGATION_ATTRIBUTE_PREFIX}*")
+
+        for aggr_key, value in values.items():
             # Build an attribute for this aggregation in the format that Storey
             # expects to receive from this method. The feature and aggregation
             # name are embedded in the Redis key. Also, drop the "_a" or "_b"
             # portion of the key, which is "the relevant attribute out of the 2
             # feature attributes," according to comments in the V3IO driver.
             value = RedisDriver.convert_to_str(value)
             value = value.split(",")
+            aggr_key = aggr_key[len(self.AGGREGATION_ATTRIBUTE_PREFIX) :]
+            aggr_key = RedisDriver.convert_to_str(aggr_key)
             feature_and_aggr_name = aggr_key[:-2]
 
             # To get the associated time, we need the aggregation name and the relevant
             # attribute (a or b), so we take a second form of the string for that purpose.
             aggr_name_with_relevant_attribute = aggr_key
             associated_time_attr, time_in_millis = await self._get_associated_time_attr(
                 redis_key_prefix, aggr_name_with_relevant_attribute
@@ -521,34 +519,45 @@
 
         # Story expects to get None back if there were no aggregations, and the
         # same for additional data.
         aggregations_to_return = aggregations if aggregations else None
         additional_data_to_return = additional_data if additional_data else None
         return aggregations_to_return, additional_data_to_return
 
+    async def redis_hscan(self, redis_key, match):
+        try:
+            cursor = 0
+            values = {}
+            while True:
+                cursor, v = await RedisDriver.asyncify(self.redis.hscan)(redis_key, cursor, match=match)
+                values.update(v)
+                if cursor == 0:
+                    break
+        except redis.ResponseError as e:
+            raise RedisError(f"Failed to get key {redis_key}. Response error was: {e}")
+        return values
+
     async def _fetch_state_by_key(self, aggr_item, container, table_path, key):
-        key = str(key)
+        redis_key_prefix = self._make_key(container, table_path, key)
+        aggregations = {}
         # Aggregation Redis keys start with the Redis key prefix for this Storey container, table
         # path, and "key," followed by ":aggr_"
-        aggregations = {}
-
         redis_key_prefix = self._make_key(container, table_path, key)
-        aggr_key_prefix = f"{redis_key_prefix}:{RedisDriver.AGGREGATION_ATTRIBUTE_PREFIX}"
-        all_aggr_keys = self.redis.hkeys(aggr_key_prefix)
-        for aggr_key in all_aggr_keys:
-            aggr_key = RedisDriver.convert_to_str(aggr_key)
-            value = await RedisDriver.asyncify(self.redis.hget)(aggr_key_prefix, aggr_key)
+        redis_key = self._static_data_key(redis_key_prefix)
+        values = await self.redis_hscan(redis_key, f"{self.AGGREGATION_ATTRIBUTE_PREFIX}*")
+        for aggr_key, value in values.items():
             # Build an attribute for this aggregation in the format that Storey
             # expects to receive from this method. The feature and aggregation
             # name are embedded in the Redis key. Also, drop the "_a" or "_b"
             # portion of the key, which is "the relevant attribute out of the 2
             # feature attributes," according to comments in the V3IO driver.
             value = RedisDriver.convert_to_str(value)
             value = value.split(",")
-
+            aggr_key = aggr_key[len(self.AGGREGATION_ATTRIBUTE_PREFIX) :]
+            aggr_key = RedisDriver.convert_to_str(aggr_key)
             feature_and_aggr_name = aggr_key[:-2]
 
             # To get the associated time, we need the aggregation name and the relevant
             # attribute (a or b), so we take a second form of the string for that purpose.
             aggr_name_with_relevant_attribute = aggr_key
             associated_time_attr, time_in_millis = await self._get_associated_time_attr(
                 redis_key_prefix, aggr_name_with_relevant_attribute
```

### Comparing `storey-1.5.0/storey/sources.py` & `storey-1.5.1/storey/sources.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/storey/sql_driver.py` & `storey-1.5.1/storey/sql_driver.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/storey/steps/__init__.py` & `storey-1.5.1/storey/steps/__init__.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/storey/steps/assertion.py` & `storey-1.5.1/storey/steps/assertion.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/storey/steps/flatten.py` & `storey-1.5.1/storey/steps/flatten.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/storey/steps/foreach.py` & `storey-1.5.1/storey/steps/foreach.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/storey/steps/partition.py` & `storey-1.5.1/storey/steps/partition.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/storey/steps/sample.py` & `storey-1.5.1/storey/steps/sample.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/storey/table.py` & `storey-1.5.1/storey/table.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/storey/targets.py` & `storey-1.5.1/storey/targets.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/storey/transformations/__init__.py` & `storey-1.5.1/storey/transformations/__init__.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/storey/utils.py` & `storey-1.5.1/storey/utils.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/storey/windowed_store.py` & `storey-1.5.1/storey/windowed_store.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/storey.egg-info/PKG-INFO` & `storey-1.5.1/storey.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: storey
-Version: 1.5.0
+Version: 1.5.1
 Summary: Async flows
 Home-page: https://github.com/mlrun/storey
 Author: Iguazio
 Author-email: yaronh@iguazio.com
 License: Apache
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers
```

### Comparing `storey-1.5.0/storey.egg-info/SOURCES.txt` & `storey-1.5.1/storey.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/tests/__init__.py` & `storey-1.5.1/tests/__init__.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/tests/test_aggregate_by_key.py` & `storey-1.5.1/tests/test_aggregate_by_key.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/tests/test_aggregate_store.py` & `storey-1.5.1/tests/test_aggregate_store.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/tests/test_flow.py` & `storey-1.5.1/tests/test_flow.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/tests/test_steps.py` & `storey-1.5.1/tests/test_steps.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/tests/test_types.py` & `storey-1.5.1/tests/test_types.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/tests/test_v3io.py` & `storey-1.5.1/tests/test_v3io.py`

 * *Files identical despite different names*

### Comparing `storey-1.5.0/tests/test_windowed_store.py` & `storey-1.5.1/tests/test_windowed_store.py`

 * *Files identical despite different names*

