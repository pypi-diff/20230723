# Comparing `tmp/stigg_api_client-0.501.0.tar.gz` & `tmp/stigg_api_client-0.502.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "stigg_api_client-0.501.0.tar", max compression
+gzip compressed data, was "stigg_api_client-0.502.0.tar", max compression
```

## Comparing `stigg_api_client-0.501.0.tar` & `stigg_api_client-0.502.0.tar`

### file list

```diff
@@ -1,8 +1,8 @@
--rw-r--r--   0        0        0     2479 2023-07-23 13:40:18.388161 stigg_api_client-0.501.0/README.md
--rw-r--r--   0        0        0      460 2023-07-23 13:40:51.171780 stigg_api_client-0.501.0/pyproject.toml
--rw-r--r--   0        0        0       44 2023-07-23 13:40:18.388161 stigg_api_client-0.501.0/stigg/__init__.py
--rw-r--r--   0        0        0     1141 2023-07-23 13:40:18.388161 stigg_api_client-0.501.0/stigg/client.py
--rw-r--r--   0        0        0        0 2023-07-23 13:40:49.295804 stigg_api_client-0.501.0/stigg/generated/__init__.py
--rw-r--r--   0        0        0    49477 2023-07-23 13:40:49.707799 stigg_api_client-0.501.0/stigg/generated/operations.py
--rw-r--r--   0        0        0   465269 2023-07-23 13:40:49.559801 stigg_api_client-0.501.0/stigg/generated/schema.py
--rw-r--r--   0        0        0     3081 1970-01-01 00:00:00.000000 stigg_api_client-0.501.0/PKG-INFO
+-rw-r--r--   0        0        0     2479 2023-07-23 16:25:27.250014 stigg_api_client-0.502.0/README.md
+-rw-r--r--   0        0        0      460 2023-07-23 16:26:00.458070 stigg_api_client-0.502.0/pyproject.toml
+-rw-r--r--   0        0        0       44 2023-07-23 16:25:27.250014 stigg_api_client-0.502.0/stigg/__init__.py
+-rw-r--r--   0        0        0     1141 2023-07-23 16:25:27.250014 stigg_api_client-0.502.0/stigg/client.py
+-rw-r--r--   0        0        0        0 2023-07-23 16:25:58.542063 stigg_api_client-0.502.0/stigg/generated/__init__.py
+-rw-r--r--   0        0        0    49477 2023-07-23 16:25:58.954065 stigg_api_client-0.502.0/stigg/generated/operations.py
+-rw-r--r--   0        0        0   465343 2023-07-23 16:25:58.802064 stigg_api_client-0.502.0/stigg/generated/schema.py
+-rw-r--r--   0        0        0     3081 1970-01-01 00:00:00.000000 stigg_api_client-0.502.0/PKG-INFO
```

### Comparing `stigg_api_client-0.501.0/README.md` & `stigg_api_client-0.502.0/README.md`

 * *Files identical despite different names*

### Comparing `stigg_api_client-0.501.0/stigg/client.py` & `stigg_api_client-0.502.0/stigg/client.py`

 * *Files identical despite different names*

### Comparing `stigg_api_client-0.501.0/stigg/generated/operations.py` & `stigg_api_client-0.502.0/stigg/generated/operations.py`

 * *Files identical despite different names*

### Comparing `stigg_api_client-0.501.0/stigg/generated/schema.py` & `stigg_api_client-0.502.0/stigg/generated/schema.py`

 * *Files 0% similar despite different names*

```diff
@@ -3080,21 +3080,22 @@
     meter_type = sgqlc.types.Field(MeterType, graphql_name='meterType')
     ref_id = sgqlc.types.Field(String, graphql_name='refId')
     updated_at = sgqlc.types.Field(DateTime, graphql_name='updatedAt')
 
 
 class UpdateFeatureInput(sgqlc.types.Input):
     __schema__ = schema
-    __field_names__ = ('additional_meta_data', 'description', 'display_name', 'environment_id', 'feature_units', 'feature_units_plural', 'ref_id')
+    __field_names__ = ('additional_meta_data', 'description', 'display_name', 'environment_id', 'feature_units', 'feature_units_plural', 'meter', 'ref_id')
     additional_meta_data = sgqlc.types.Field(JSON, graphql_name='additionalMetaData')
     description = sgqlc.types.Field(String, graphql_name='description')
     display_name = sgqlc.types.Field(String, graphql_name='displayName')
     environment_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='environmentId')
     feature_units = sgqlc.types.Field(String, graphql_name='featureUnits')
     feature_units_plural = sgqlc.types.Field(String, graphql_name='featureUnitsPlural')
+    meter = sgqlc.types.Field(CreateMeter, graphql_name='meter')
     ref_id = sgqlc.types.Field(sgqlc.types.non_null(String), graphql_name='refId')
 
 
 class UpdateHook(sgqlc.types.Input):
     __schema__ = schema
     __field_names__ = ('created_at', 'description', 'endpoint', 'environment_id', 'event_log_types', 'id', 'secret_key', 'status')
     created_at = sgqlc.types.Field(DateTime, graphql_name='createdAt')
```

### Comparing `stigg_api_client-0.501.0/PKG-INFO` & `stigg_api_client-0.502.0/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: stigg-api-client
-Version: 0.501.0
+Version: 0.502.0
 Summary: 
 Author: Stigg
 Author-email: support@stigg.io
 Requires-Python: >=3.7,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
```

