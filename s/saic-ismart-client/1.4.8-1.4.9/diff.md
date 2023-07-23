# Comparing `tmp/saic_ismart_client-1.4.8.tar.gz` & `tmp/saic_ismart_client-1.4.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "saic_ismart_client-1.4.8.tar", last modified: Sat Jul 22 15:44:59 2023, max compression
+gzip compressed data, was "saic_ismart_client-1.4.9.tar", last modified: Sun Jul 23 18:08:36 2023, max compression
```

## Comparing `saic_ismart_client-1.4.8.tar` & `saic_ismart_client-1.4.9.tar`

### file list

```diff
@@ -1,51 +1,51 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 15:44:59.713411 saic_ismart_client-1.4.8/
--rw-r--r--   0 runner    (1001) docker     (123)     1068 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       53 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     1154 2023-07-22 15:44:59.713411 saic_ismart_client-1.4.8/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      598 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/README.md
--rw-r--r--   0 runner    (1001) docker     (123)      730 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-22 15:44:59.713411 saic_ismart_client-1.4.8/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 15:44:59.701411 saic_ismart_client-1.4.8/src/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 15:44:59.705411 saic_ismart_client-1.4.8/src/saic_ismart_client/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 15:44:59.705411 saic_ismart_client-1.4.8/src/saic_ismart_client/ASN.1_schema/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 15:44:59.709411 saic_ismart_client-1.4.8/src/saic_ismart_client/ASN.1_schema/v1_1/
--rw-r--r--   0 runner    (1001) docker     (123)     4863 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/src/saic_ismart_client/ASN.1_schema/v1_1/ApplicationData.asn1
--rw-r--r--   0 runner    (1001) docker     (123)     1585 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/src/saic_ismart_client/ASN.1_schema/v1_1/MP_DispatcherBody.asn1
--rw-r--r--   0 runner    (1001) docker     (123)      257 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/src/saic_ismart_client/ASN.1_schema/v1_1/MP_DispatcherHeader.asn1
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 15:44:59.709411 saic_ismart_client-1.4.8/src/saic_ismart_client/ASN.1_schema/v2_1/
--rw-r--r--   0 runner    (1001) docker     (123)     3609 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/src/saic_ismart_client/ASN.1_schema/v2_1/ApplicationData.asn1
--rw-r--r--   0 runner    (1001) docker     (123)      901 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/src/saic_ismart_client/ASN.1_schema/v2_1/MP_DispatcherBody.asn1
--rw-r--r--   0 runner    (1001) docker     (123)      222 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/src/saic_ismart_client/ASN.1_schema/v2_1/MP_DispatcherHeader.asn1
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 15:44:59.709411 saic_ismart_client-1.4.8/src/saic_ismart_client/ASN.1_schema/v3_0/
--rw-r--r--   0 runner    (1001) docker     (123)     5113 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/src/saic_ismart_client/ASN.1_schema/v3_0/ApplicationData.asn1
--rw-r--r--   0 runner    (1001) docker     (123)      901 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/src/saic_ismart_client/ASN.1_schema/v3_0/MP_DispatcherBody.asn1
--rw-r--r--   0 runner    (1001) docker     (123)      222 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/src/saic_ismart_client/ASN.1_schema/v3_0/MP_DispatcherHeader.asn1
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/src/saic_ismart_client/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4380 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/src/saic_ismart_client/abrp_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    24328 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/src/saic_ismart_client/common_model.py
--rw-r--r--   0 runner    (1001) docker     (123)     4009 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/src/saic_ismart_client/message_decoder.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 15:44:59.709411 saic_ismart_client-1.4.8/src/saic_ismart_client/ota_v1_1/
--rw-r--r--   0 runner    (1001) docker     (123)      866 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/src/saic_ismart_client/ota_v1_1/Message.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/src/saic_ismart_client/ota_v1_1/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    15634 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/src/saic_ismart_client/ota_v1_1/data_model.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 15:44:59.709411 saic_ismart_client-1.4.8/src/saic_ismart_client/ota_v2_1/
--rw-r--r--   0 runner    (1001) docker     (123)      869 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/src/saic_ismart_client/ota_v2_1/Message.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/src/saic_ismart_client/ota_v2_1/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    18407 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/src/saic_ismart_client/ota_v2_1/data_model.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 15:44:59.709411 saic_ismart_client-1.4.8/src/saic_ismart_client/ota_v3_0/
--rw-r--r--   0 runner    (1001) docker     (123)     2442 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/src/saic_ismart_client/ota_v3_0/Message.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/src/saic_ismart_client/ota_v3_0/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    23497 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/src/saic_ismart_client/ota_v3_0/data_model.py
--rw-r--r--   0 runner    (1001) docker     (123)    44737 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/src/saic_ismart_client/saic_api.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 15:44:59.709411 saic_ismart_client-1.4.8/src/saic_ismart_client.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1154 2023-07-22 15:44:59.000000 saic_ismart_client-1.4.8/src/saic_ismart_client.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1561 2023-07-22 15:44:59.000000 saic_ismart_client-1.4.8/src/saic_ismart_client.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-22 15:44:59.000000 saic_ismart_client-1.4.8/src/saic_ismart_client.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       51 2023-07-22 15:44:59.000000 saic_ismart_client-1.4.8/src/saic_ismart_client.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       19 2023-07-22 15:44:59.000000 saic_ismart_client-1.4.8/src/saic_ismart_client.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 15:44:59.713411 saic_ismart_client-1.4.8/tests/
--rw-r--r--   0 runner    (1001) docker     (123)     7936 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/tests/test_Message_v1_1.py
--rw-r--r--   0 runner    (1001) docker     (123)     4243 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/tests/test_Message_v2_1.py
--rw-r--r--   0 runner    (1001) docker     (123)     8581 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/tests/test_Message_v3_0.py
--rw-r--r--   0 runner    (1001) docker     (123)     4217 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/tests/test_abrp_api.py
--rw-r--r--   0 runner    (1001) docker     (123)    16753 2023-07-22 15:44:48.000000 saic_ismart_client-1.4.8/tests/test_saic_api.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 18:08:36.562830 saic_ismart_client-1.4.9/
+-rw-r--r--   0 runner    (1001) docker     (123)     1068 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       53 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     1154 2023-07-23 18:08:36.562830 saic_ismart_client-1.4.9/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      598 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      730 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 18:08:36.562830 saic_ismart_client-1.4.9/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 18:08:36.550830 saic_ismart_client-1.4.9/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 18:08:36.554830 saic_ismart_client-1.4.9/src/saic_ismart_client/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 18:08:36.550830 saic_ismart_client-1.4.9/src/saic_ismart_client/ASN.1_schema/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 18:08:36.558830 saic_ismart_client-1.4.9/src/saic_ismart_client/ASN.1_schema/v1_1/
+-rw-r--r--   0 runner    (1001) docker     (123)     4863 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/src/saic_ismart_client/ASN.1_schema/v1_1/ApplicationData.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)     1585 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/src/saic_ismart_client/ASN.1_schema/v1_1/MP_DispatcherBody.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)      257 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/src/saic_ismart_client/ASN.1_schema/v1_1/MP_DispatcherHeader.asn1
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 18:08:36.558830 saic_ismart_client-1.4.9/src/saic_ismart_client/ASN.1_schema/v2_1/
+-rw-r--r--   0 runner    (1001) docker     (123)     3609 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/src/saic_ismart_client/ASN.1_schema/v2_1/ApplicationData.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)      901 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/src/saic_ismart_client/ASN.1_schema/v2_1/MP_DispatcherBody.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)      222 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/src/saic_ismart_client/ASN.1_schema/v2_1/MP_DispatcherHeader.asn1
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 18:08:36.558830 saic_ismart_client-1.4.9/src/saic_ismart_client/ASN.1_schema/v3_0/
+-rw-r--r--   0 runner    (1001) docker     (123)     5113 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/src/saic_ismart_client/ASN.1_schema/v3_0/ApplicationData.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)      901 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/src/saic_ismart_client/ASN.1_schema/v3_0/MP_DispatcherBody.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)      222 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/src/saic_ismart_client/ASN.1_schema/v3_0/MP_DispatcherHeader.asn1
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/src/saic_ismart_client/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4380 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/src/saic_ismart_client/abrp_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    24328 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/src/saic_ismart_client/common_model.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4009 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/src/saic_ismart_client/message_decoder.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 18:08:36.558830 saic_ismart_client-1.4.9/src/saic_ismart_client/ota_v1_1/
+-rw-r--r--   0 runner    (1001) docker     (123)      866 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/src/saic_ismart_client/ota_v1_1/Message.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/src/saic_ismart_client/ota_v1_1/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15634 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/src/saic_ismart_client/ota_v1_1/data_model.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 18:08:36.558830 saic_ismart_client-1.4.9/src/saic_ismart_client/ota_v2_1/
+-rw-r--r--   0 runner    (1001) docker     (123)      869 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/src/saic_ismart_client/ota_v2_1/Message.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/src/saic_ismart_client/ota_v2_1/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18407 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/src/saic_ismart_client/ota_v2_1/data_model.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 18:08:36.562830 saic_ismart_client-1.4.9/src/saic_ismart_client/ota_v3_0/
+-rw-r--r--   0 runner    (1001) docker     (123)     2442 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/src/saic_ismart_client/ota_v3_0/Message.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/src/saic_ismart_client/ota_v3_0/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    23497 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/src/saic_ismart_client/ota_v3_0/data_model.py
+-rw-r--r--   0 runner    (1001) docker     (123)    43908 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/src/saic_ismart_client/saic_api.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 18:08:36.554830 saic_ismart_client-1.4.9/src/saic_ismart_client.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1154 2023-07-23 18:08:36.000000 saic_ismart_client-1.4.9/src/saic_ismart_client.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1561 2023-07-23 18:08:36.000000 saic_ismart_client-1.4.9/src/saic_ismart_client.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 18:08:36.000000 saic_ismart_client-1.4.9/src/saic_ismart_client.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       51 2023-07-23 18:08:36.000000 saic_ismart_client-1.4.9/src/saic_ismart_client.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       19 2023-07-23 18:08:36.000000 saic_ismart_client-1.4.9/src/saic_ismart_client.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 18:08:36.562830 saic_ismart_client-1.4.9/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     7936 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/tests/test_Message_v1_1.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4243 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/tests/test_Message_v2_1.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8581 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/tests/test_Message_v3_0.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4217 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/tests/test_abrp_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16753 2023-07-23 18:08:22.000000 saic_ismart_client-1.4.9/tests/test_saic_api.py
```

### Comparing `saic_ismart_client-1.4.8/LICENSE` & `saic_ismart_client-1.4.9/LICENSE`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.4.8/PKG-INFO` & `saic_ismart_client-1.4.9/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: saic_ismart_client
-Version: 1.4.8
+Version: 1.4.9
 Summary: SAIC client library (MG iSMART)
 Author-email: Thomas Salm <saic-python-client@devtom.de>
 Project-URL: Homepage, https://github.com/SAIC-iSmart-API/saic-python-client
 Project-URL: Bug Tracker, https://github.com/SAIC-iSmart-API/saic-python-client/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `saic_ismart_client-1.4.8/README.md` & `saic_ismart_client-1.4.9/README.md`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.4.8/pyproject.toml` & `saic_ismart_client-1.4.9/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "saic_ismart_client"
-version = "1.4.8"
+version = "1.4.9"
 authors = [
     { name = "Thomas Salm", email="saic-python-client@devtom.de"},
 ]
 dependencies = [
     "asn1tools >= 0.166.0",
     "requests >= 2.31.0",
     "urllib3 >= 2.0.3",
```

### Comparing `saic_ismart_client-1.4.8/src/saic_ismart_client/ASN.1_schema/v1_1/ApplicationData.asn1` & `saic_ismart_client-1.4.9/src/saic_ismart_client/ASN.1_schema/v1_1/ApplicationData.asn1`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.4.8/src/saic_ismart_client/ASN.1_schema/v1_1/MP_DispatcherBody.asn1` & `saic_ismart_client-1.4.9/src/saic_ismart_client/ASN.1_schema/v1_1/MP_DispatcherBody.asn1`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.4.8/src/saic_ismart_client/ASN.1_schema/v2_1/ApplicationData.asn1` & `saic_ismart_client-1.4.9/src/saic_ismart_client/ASN.1_schema/v2_1/ApplicationData.asn1`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.4.8/src/saic_ismart_client/ASN.1_schema/v2_1/MP_DispatcherBody.asn1` & `saic_ismart_client-1.4.9/src/saic_ismart_client/ASN.1_schema/v2_1/MP_DispatcherBody.asn1`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.4.8/src/saic_ismart_client/ASN.1_schema/v3_0/ApplicationData.asn1` & `saic_ismart_client-1.4.9/src/saic_ismart_client/ASN.1_schema/v3_0/ApplicationData.asn1`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.4.8/src/saic_ismart_client/ASN.1_schema/v3_0/MP_DispatcherBody.asn1` & `saic_ismart_client-1.4.9/src/saic_ismart_client/ASN.1_schema/v3_0/MP_DispatcherBody.asn1`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.4.8/src/saic_ismart_client/abrp_api.py` & `saic_ismart_client-1.4.9/src/saic_ismart_client/abrp_api.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.4.8/src/saic_ismart_client/common_model.py` & `saic_ismart_client-1.4.9/src/saic_ismart_client/common_model.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.4.8/src/saic_ismart_client/message_decoder.py` & `saic_ismart_client-1.4.9/src/saic_ismart_client/message_decoder.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.4.8/src/saic_ismart_client/ota_v1_1/Message.py` & `saic_ismart_client-1.4.9/src/saic_ismart_client/ota_v1_1/Message.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.4.8/src/saic_ismart_client/ota_v1_1/data_model.py` & `saic_ismart_client-1.4.9/src/saic_ismart_client/ota_v1_1/data_model.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.4.8/src/saic_ismart_client/ota_v2_1/Message.py` & `saic_ismart_client-1.4.9/src/saic_ismart_client/ota_v2_1/Message.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.4.8/src/saic_ismart_client/ota_v2_1/data_model.py` & `saic_ismart_client-1.4.9/src/saic_ismart_client/ota_v2_1/data_model.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.4.8/src/saic_ismart_client/ota_v3_0/Message.py` & `saic_ismart_client-1.4.9/src/saic_ismart_client/ota_v3_0/Message.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.4.8/src/saic_ismart_client/ota_v3_0/data_model.py` & `saic_ismart_client-1.4.9/src/saic_ismart_client/ota_v3_0/data_model.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.4.8/src/saic_ismart_client/saic_api.py` & `saic_ismart_client-1.4.9/src/saic_ismart_client/saic_api.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,8 +1,9 @@
 import datetime
+import functools
 import hashlib
 import logging
 import os
 import time
 import urllib.parse
 from typing import cast
 
@@ -268,63 +269,23 @@
 
         param3 = RvcReqParam()
         param3.param_id = 255
         param3.param_value = b'\x00'
         rcv_params.append(param3)
         return self.send_vehicle_ctrl_cmd_with_retry(vin_info, b'\x05', rcv_params, True)
 
-    def start_ac(self, vin_info: VinInfo) -> MessageV2:
-        rcv_params = []
-        param1 = RvcReqParam()
-        param1.param_id = 19
-        param1.param_value = b'\x02'
-        rcv_params.append(param1)
-
-        param2 = RvcReqParam()
-        param2.param_id = 20
-        param2.param_value = b'\x08'
-        rcv_params.append(param2)
-
-        param3 = RvcReqParam()
-        param3.param_id = 255
-        param3.param_value = b'\x00'
-        rcv_params.append(param3)
-
-        return self.send_vehicle_ctrl_cmd_with_retry(vin_info, b'\x06', rcv_params, True)
+    def start_ac(self, vin_info: VinInfo, temperature_idx=8) -> MessageV2:
+        return self.control_climate(vin_info, fan_speed=2, ac_on=None, temperature_idx=temperature_idx)
 
     def stop_ac(self, vin_info: VinInfo) -> MessageV2:
         return self.control_climate(vin_info, fan_speed=0, ac_on=False, temperature_idx=0)
 
     def start_ac_blowing(self, vin_info: VinInfo) -> MessageV2:
         return self.control_climate(vin_info, fan_speed=1, ac_on=False, temperature_idx=0)
 
-    def stop_ac_blowing(self, vin_info: VinInfo) -> MessageV2:
-        rcv_params = []
-        param1 = RvcReqParam()
-        param1.param_id = 19
-        param1.param_value = b'\x00'
-        rcv_params.append(param1)
-
-        param2 = RvcReqParam()
-        param2.param_id = 20
-        param2.param_value = b'\x00'
-        rcv_params.append(param2)
-
-        param3 = RvcReqParam()
-        param3.param_id = 22
-        param3.param_value = b'\x00'
-        rcv_params.append(param3)
-
-        param4 = RvcReqParam()
-        param4.param_id = 255
-        param4.param_value = b'\x00'
-        rcv_params.append(param4)
-
-        return self.send_vehicle_ctrl_cmd_with_retry(vin_info, b'\x06', rcv_params, True)
-
     def start_front_defrost(self, vin_info: VinInfo) -> MessageV2:
         return self.control_climate(vin_info, fan_speed=5, ac_on=True, temperature_idx=8)
 
     def stop_front_defrost(self, vin_info: VinInfo) -> MessageV2:
         rcv_params = []
         param1 = RvcReqParam()
         param1.param_id = 19
@@ -348,15 +309,15 @@
 
         return self.send_vehicle_ctrl_cmd_with_retry(vin_info, b'\x06', rcv_params, True)
 
     def control_climate(
             self,
             vin_info: VinInfo,
             fan_speed: int = 5,
-            ac_on: bool = True,
+            ac_on: bool | None = True,
             temperature_idx: int = 8
     ) -> MessageV2:
 
         if fan_speed < 0 or fan_speed > 5:
             raise Exception('fan_speed must be between 0 and 5')
 
         if temperature_idx < 0 or temperature_idx > 14:
@@ -368,24 +329,25 @@
 
         rcv_params = []
         param1 = RvcReqParam()
         param1.param_id = 19
         param1.param_value = fan_speed.to_bytes(1, 'big')
         rcv_params.append(param1)
 
-        if fan_speed > 0:
+        if fan_speed > 0 or temperature_idx == 0:
             param2 = RvcReqParam()
             param2.param_id = 20
             param2.param_value = temperature_idx.to_bytes(1, 'big')
             rcv_params.append(param2)
 
-        param3 = RvcReqParam()
-        param3.param_id = 22
-        param3.param_value = bool_to_bit(ac_on)
-        rcv_params.append(param3)
+        if ac_on is not None:
+            param3 = RvcReqParam()
+            param3.param_id = 22
+            param3.param_value = bool_to_bit(ac_on)
+            rcv_params.append(param3)
 
         param4 = RvcReqParam()
         param4.param_id = 255
         param4.param_value = b'\x00'
         rcv_params.append(param4)
         return self.send_vehicle_ctrl_cmd_with_retry(vin_info, b'\x06', rcv_params, True)
 
@@ -468,80 +430,94 @@
         param.param_id = 255
         param.param_value = b'\x00'
         rcv_params.append(param)
 
         return self.send_vehicle_ctrl_cmd_with_retry(vin_info, b'\x00', rcv_params, True)
 
     def send_vehicle_ctrl_cmd_with_retry(self, vin_info: VinInfo, rvc_req_type: bytes, rvc_params: list,
-                                         has_app_data: bool) -> MessageV2:
-        vehicle_control_cmd_rsp_msg = self.send_vehicle_control_command(vin_info, rvc_req_type, rvc_params)
+                                         has_app_data: bool, max_retries=3) -> MessageV2:
 
-        if has_app_data:
-            iteration = 1
-            while vehicle_control_cmd_rsp_msg.application_data is None:
-                if vehicle_control_cmd_rsp_msg.body.error_message is not None:
-                    self.handle_error(vehicle_control_cmd_rsp_msg.body, iteration)
-                else:
-                    LOG.debug('API request returned no application data and no error message.')
-                    time.sleep(float(AVG_SMS_DELIVERY_TIME))
-
-                iteration += 1
-                event_id = vehicle_control_cmd_rsp_msg.body.event_id
-                vehicle_control_cmd_rsp_msg = self.send_vehicle_control_command(vin_info, rvc_req_type, rvc_params,
-                                                                                event_id)
-        else:
-            retry = 1
-            while (
-                    vehicle_control_cmd_rsp_msg.body.error_message is not None
-                    and retry <= 3
-            ):
-                self.handle_error(vehicle_control_cmd_rsp_msg.body, retry)
-                event_id = vehicle_control_cmd_rsp_msg.body.event_id
-                vehicle_control_cmd_rsp_msg = self.send_vehicle_control_command(vin_info, rvc_req_type, rvc_params,
-                                                                                event_id)
-                retry += 1
-            if vehicle_control_cmd_rsp_msg.body.error_message is not None:
-                raise SaicApiException(vehicle_control_cmd_rsp_msg.body.error_message.decode(),
-                                       vehicle_control_cmd_rsp_msg.body.result)
-        return vehicle_control_cmd_rsp_msg
+        return self.handle_retry(
+            functools.partial(self.__send_vehicle_control_command, rvc_req_type, rvc_params),
+            vin_info=vin_info,
+            has_app_data=has_app_data,
+            max_retries=max_retries
+        )
 
     def get_message_list_with_retry(self) -> list:
         message_list_rsp_msg = self.handle_retry(self.get_message_list)
 
         result = []
         if message_list_rsp_msg.application_data is not None:
             message_list_rsp = cast(MessageListResp, message_list_rsp_msg.application_data)
             for message in message_list_rsp.messages:
                 result.append(convert(message))
         return result
 
-    def handle_retry(self, func, vin_info: VinInfo = None):
+    def handle_retry(self, func, vin_info: VinInfo = None, has_app_data: bool = True, max_retries: int = 3):
+        if has_app_data:
+            return self.__handle_retry_with_app_data(func, vin_info=vin_info, max_retries=max_retries)
+        else:
+            return self.__handle_retry_without_app_data(func, vin_info=vin_info, max_retries=max_retries)
+
+    def __handle_retry_without_app_data(self, func, vin_info: VinInfo, max_retries: int):
+        if vin_info:
+            rsp = func(vin_info)
+        else:
+            rsp = func()
+        rsp_msg = cast(AbstractMessage, rsp)
+
+        retry = 1
+        while (
+                rsp_msg.body.error_message is not None
+                and retry <= max_retries
+        ):
+            self.handle_error(rsp_msg.body, retry)
+
+            if vin_info:
+                rsp_msg = func(vin_info, rsp_msg.body.event_id)
+            else:
+                rsp_msg = func(rsp_msg.body.event_id)
+
+            retry += 1
+        if rsp_msg.body.error_message is not None:
+            raise SaicApiException(rsp_msg.body.error_message.decode(),
+                                   rsp_msg.body.result)
+        return rsp_msg
+
+    def __handle_retry_with_app_data(self, func, vin_info: VinInfo, max_retries: int):
         if vin_info:
             rsp = func(vin_info)
         else:
             rsp = func()
         rsp_msg = cast(AbstractMessage, rsp)
         iteration = 1
         while rsp_msg.application_data is None:
-            if rsp_msg.body.error_message is not None:
+            error_message = rsp_msg.body.error_message
+            if iteration > max_retries:
+                additional_info = '.'
+                if error_message is not None:
+                    additional_info = f', error message: {error_message.decode()}'
+                raise SaicApiException(f'API request failed after {iteration} retries{additional_info}')
+            elif error_message is not None:
                 self.handle_error(rsp_msg.body, iteration)
             else:
                 LOG.debug('API request returned no application data and no error message.')
                 time.sleep(float(AVG_SMS_DELIVERY_TIME))
 
             iteration += 1
 
             if vin_info:
                 rsp_msg = func(vin_info, rsp_msg.body.event_id)
             else:
                 rsp_msg = func(rsp_msg.body.event_id)
         return rsp_msg
 
-    def send_vehicle_control_command(self, vin_info: VinInfo, rvc_req_type: bytes, rvc_params: list,
-                                     event_id: str = None) -> MessageV2:
+    def __send_vehicle_control_command(self, rvc_req_type: bytes, rvc_params: list,
+                                       vin_info: VinInfo, event_id: str = None) -> MessageV2:
         vehicle_control_req = OtaRvcReq()
         vehicle_control_req.rvc_req_type = rvc_req_type
         for p in rvc_params:
             param = cast(RvcReqParam, p)
             vehicle_control_req.rvc_params.append(param)
 
         vehicle_control_cmd_req_msg = MessageV2(MessageBodyV2(), vehicle_control_req)
@@ -889,14 +865,15 @@
             # The service is not available,please try again later
             LOG.debug(message)
             time.sleep(float(waiting_time))
         elif message_body.result == -1:
             LOG.warning(message)
         else:
             LOG.error(message)
+            raise SaicApiException(message_body.error_message.decode(), message_body.result)
 
 
 def bool_to_bit(flag):
     return b'\x01' if flag else b'\x00'
 
 
 def bool_to_int(flag):
```

### Comparing `saic_ismart_client-1.4.8/src/saic_ismart_client.egg-info/PKG-INFO` & `saic_ismart_client-1.4.9/src/saic_ismart_client.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: saic-ismart-client
-Version: 1.4.8
+Version: 1.4.9
 Summary: SAIC client library (MG iSMART)
 Author-email: Thomas Salm <saic-python-client@devtom.de>
 Project-URL: Homepage, https://github.com/SAIC-iSmart-API/saic-python-client
 Project-URL: Bug Tracker, https://github.com/SAIC-iSmart-API/saic-python-client/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `saic_ismart_client-1.4.8/src/saic_ismart_client.egg-info/SOURCES.txt` & `saic_ismart_client-1.4.9/src/saic_ismart_client.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.4.8/tests/test_Message_v1_1.py` & `saic_ismart_client-1.4.9/tests/test_Message_v1_1.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.4.8/tests/test_Message_v2_1.py` & `saic_ismart_client-1.4.9/tests/test_Message_v2_1.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.4.8/tests/test_Message_v3_0.py` & `saic_ismart_client-1.4.9/tests/test_Message_v3_0.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.4.8/tests/test_abrp_api.py` & `saic_ismart_client-1.4.9/tests/test_abrp_api.py`

 * *Files identical despite different names*

### Comparing `saic_ismart_client-1.4.8/tests/test_saic_api.py` & `saic_ismart_client-1.4.9/tests/test_saic_api.py`

 * *Files identical despite different names*

