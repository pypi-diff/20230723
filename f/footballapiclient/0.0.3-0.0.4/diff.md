# Comparing `tmp/footballapiclient-0.0.3.tar.gz` & `tmp/footballapiclient-0.0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "footballapiclient-0.0.3.tar", max compression
+gzip compressed data, was "footballapiclient-0.0.4.tar", max compression
```

## Comparing `footballapiclient-0.0.3.tar` & `footballapiclient-0.0.4.tar`

### file list

```diff
@@ -1,18 +1,16 @@
--rw-r--r--   0        0        0      211 2023-06-28 15:33:55.442788 footballapiclient-0.0.3/footballAPIClient/__init__.py
--rw-r--r--   0        0        0        0 2023-06-28 15:37:36.756322 footballapiclient-0.0.3/footballAPIClient/__main__.py
--rw-r--r--   0        0        0      185 2023-06-06 15:02:35.081060 footballapiclient-0.0.3/footballAPIClient/_constants.py
--rw-r--r--   0        0        0      547 2023-06-04 08:23:05.053509 footballapiclient-0.0.3/footballAPIClient/Exceptions/__pycache__/ApiKeyMissingError.cpython-39.pyc
--rw-r--r--   0        0        0      556 2023-06-04 14:28:11.403008 footballapiclient-0.0.3/footballAPIClient/Exceptions/__pycache__/APILimitExceededError.cpython-39.pyc
--rw-r--r--   0        0        0      547 2023-06-28 15:30:04.094603 footballapiclient-0.0.3/footballAPIClient/Exceptions/__pycache__/InvalidApiKeyError.cpython-39.pyc
--rw-r--r--   0        0        0      876 2023-06-02 19:58:25.420894 footballapiclient-0.0.3/footballAPIClient/Exceptions/__pycache__/MissingParametersError.cpython-39.pyc
--rw-r--r--   0        0        0      105 2023-06-04 08:03:20.072635 footballapiclient-0.0.3/footballAPIClient/Exceptions/ApiKeyMissingError.py
--rw-r--r--   0        0        0      110 2023-06-04 14:28:10.117768 footballapiclient-0.0.3/footballAPIClient/Exceptions/APILimitExceededError.py
--rw-r--r--   0        0        0      105 2023-06-28 15:24:26.674870 footballapiclient-0.0.3/footballAPIClient/Exceptions/InvalidApiKeyError.py
--rw-r--r--   0        0        0      405 2023-06-02 19:58:24.807867 footballapiclient-0.0.3/footballAPIClient/Exceptions/MissingParametersError.py
--rw-r--r--   0        0        0    42521 2023-06-28 15:30:03.258607 footballapiclient-0.0.3/footballAPIClient/footballAPI.py
--rw-r--r--   0        0        0     7517 2023-06-28 14:48:30.416016 footballapiclient-0.0.3/footballAPIClient/helpers/__pycache__/ParameterValidator.cpython-39.pyc
--rw-r--r--   0        0        0     6870 2023-06-08 20:07:33.392693 footballapiclient-0.0.3/footballAPIClient/helpers/ParameterValidator.py
--rw-r--r--   0        0        0     1092 2023-06-05 18:10:22.673709 footballapiclient-0.0.3/LICENSE
--rw-r--r--   0        0        0      593 2023-06-28 15:34:07.542618 footballapiclient-0.0.3/pyproject.toml
--rw-r--r--   0        0        0     1597 2023-06-08 22:15:44.243327 footballapiclient-0.0.3/README.md
--rw-r--r--   0        0        0     2313 1970-01-01 00:00:00.000000 footballapiclient-0.0.3/PKG-INFO
+-rw-r--r--   0        0        0      211 2023-07-23 18:21:36.354614 footballapiclient-0.0.4/footballAPIClient/__init__.py
+-rw-r--r--   0        0        0     1116 2023-07-10 12:53:41.820780 footballapiclient-0.0.4/footballAPIClient/__main__.py
+-rw-r--r--   0        0        0      185 2023-06-06 15:02:35.081060 footballapiclient-0.0.4/footballAPIClient/_constants.py
+-rw-r--r--   0        0        0      556 2023-06-04 14:28:11.403008 footballapiclient-0.0.4/footballAPIClient/Exceptions/__pycache__/APILimitExceededError.cpython-39.pyc
+-rw-r--r--   0        0        0      876 2023-06-02 19:58:25.420894 footballapiclient-0.0.4/footballAPIClient/Exceptions/__pycache__/MissingParametersError.cpython-39.pyc
+-rw-r--r--   0        0        0      105 2023-06-04 08:03:20.072635 footballapiclient-0.0.4/footballAPIClient/Exceptions/ApiKeyMissingError.py
+-rw-r--r--   0        0        0      110 2023-06-04 14:28:10.117768 footballapiclient-0.0.4/footballAPIClient/Exceptions/APILimitExceededError.py
+-rw-r--r--   0        0        0      107 2023-07-23 18:16:11.161204 footballapiclient-0.0.4/footballAPIClient/Exceptions/InternalApiException.py
+-rw-r--r--   0        0        0      405 2023-06-02 19:58:24.807867 footballapiclient-0.0.4/footballAPIClient/Exceptions/MissingParametersError.py
+-rw-r--r--   0        0        0    42518 2023-07-23 18:16:11.235205 footballapiclient-0.0.4/footballAPIClient/footballAPI.py
+-rw-r--r--   0        0        0     7517 2023-06-28 14:48:30.416016 footballapiclient-0.0.4/footballAPIClient/helpers/__pycache__/ParameterValidator.cpython-39.pyc
+-rw-r--r--   0        0        0     6870 2023-06-08 20:07:33.392693 footballapiclient-0.0.4/footballAPIClient/helpers/ParameterValidator.py
+-rw-r--r--   0        0        0     1092 2023-06-05 18:10:22.673709 footballapiclient-0.0.4/LICENSE
+-rw-r--r--   0        0        0      593 2023-07-23 18:21:27.797734 footballapiclient-0.0.4/pyproject.toml
+-rw-r--r--   0        0        0     1597 2023-06-08 22:15:44.243327 footballapiclient-0.0.4/README.md
+-rw-r--r--   0        0        0     2313 1970-01-01 00:00:00.000000 footballapiclient-0.0.4/PKG-INFO
```

### Comparing `footballapiclient-0.0.3/footballAPIClient/Exceptions/__pycache__/ApiKeyMissingError.cpython-39.pyc` & `footballapiclient-0.0.4/footballAPIClient/Exceptions/__pycache__/APILimitExceededError.cpython-39.pyc`

 * *Format-specific differences are supported for Python .pyc files but no file-specific differences were detected; falling back to a binary diff. file(1) reports: Byte-compiled Python module for CPython 3.9, timestamp-based, .py timestamp: Sun Jun  4 08:03:20 2023 UTC, .py size: 105 bytes*

 * *Could not decompile bytecode: bad marshal data (unknown type code)*

 * *Files 18% similar despite different names*

```diff
@@ -1,35 +1,35 @@
-00000000: 610d 0d0a 0000 0000 4845 7c64 6900 0000  a.......HE|di...
+00000000: 610d 0d0a 0000 0000 7a9f 7c64 6e00 0000  a.......z.|dn...
 00000010: e300 0000 0000 0000 0000 0000 0000 0000  ................
 00000020: 0004 0000 0040 0000 0073 1400 0000 4700  .....@...s....G.
 00000030: 6400 6401 8400 6401 6500 8303 5a01 6402  d.d...d.e...Z.d.
 00000040: 5300 2903 6300 0000 0000 0000 0000 0000  S.).c...........
 00000050: 0000 0000 0003 0000 0000 0000 0073 1c00  .............s..
 00000060: 0000 6500 5a01 6400 5a02 8700 6601 6401  ..e.Z.d.Z...f.d.
 00000070: 6402 8408 5a03 8700 0400 5a04 5300 2903  d...Z.....Z.S.).
-00000080: da12 4170 694b 6579 4d69 7373 696e 6745  ..ApiKeyMissingE
-00000090: 7272 6f72 6302 0000 0000 0000 0000 0000  rrorc...........
-000000a0: 0002 0000 0003 0000 0003 0000 0073 1000  .............s..
-000000b0: 0000 7400 8300 a001 7c01 a101 0100 6400  ..t.....|.....d.
-000000c0: 5300 2901 4e29 02da 0573 7570 6572 da08  S.).N)...super..
-000000d0: 5f5f 696e 6974 5f5f 2902 da04 7365 6c66  __init__)...self
-000000e0: da07 6d65 7373 6167 65a9 01da 095f 5f63  ..message....__c
-000000f0: 6c61 7373 5f5f a900 fa5f 453a 5c43 6f64  lass__..._E:\Cod
-00000100: 6573 5c50 7963 6861 726d 5072 6f6a 6563  es\PycharmProjec
-00000110: 7473 5c66 6f6f 7462 616c 6c2d 4150 492d  ts\football-API-
-00000120: 636c 6965 6e74 5c66 6f6f 7462 616c 6c41  client\footballA
-00000130: 5049 436c 6965 6e74 5c45 7863 6570 7469  PIClient\Excepti
-00000140: 6f6e 735c 4170 694b 6579 4d69 7373 696e  ons\ApiKeyMissin
-00000150: 6745 7272 6f72 2e70 7972 0300 0000 0200  gError.pyr......
-00000160: 0000 7302 0000 0000 017a 1b41 7069 4b65  ..s......z.ApiKe
-00000170: 794d 6973 7369 6e67 4572 726f 722e 5f5f  yMissingError.__
-00000180: 696e 6974 5f5f 2905 da08 5f5f 6e61 6d65  init__)...__name
-00000190: 5f5f da0a 5f5f 6d6f 6475 6c65 5f5f da0c  __..__module__..
-000001a0: 5f5f 7175 616c 6e61 6d65 5f5f 7203 0000  __qualname__r...
-000001b0: 00da 0d5f 5f63 6c61 7373 6365 6c6c 5f5f  ...__classcell__
-000001c0: 7208 0000 0072 0800 0000 7206 0000 0072  r....r....r....r
-000001d0: 0900 0000 7201 0000 0001 0000 0073 0200  ....r........s..
-000001e0: 0000 0801 7201 0000 004e 2902 da09 4578  ....r....N)...Ex
-000001f0: 6365 7074 696f 6e72 0100 0000 7208 0000  ceptionr....r...
-00000200: 0072 0800 0000 7208 0000 0072 0900 0000  .r....r....r....
-00000210: da08 3c6d 6f64 756c 653e 0100 0000 f300  ..<module>......
-00000220: 0000 00                                  ...
+00000080: da15 4150 494c 696d 6974 4578 6365 6564  ..APILimitExceed
+00000090: 6564 4572 726f 7263 0200 0000 0000 0000  edErrorc........
+000000a0: 0000 0000 0200 0000 0300 0000 0300 0000  ................
+000000b0: 7310 0000 0074 0083 00a0 017c 01a1 0101  s....t.....|....
+000000c0: 0064 0053 0029 014e 2902 da05 7375 7065  .d.S.).N)...supe
+000000d0: 72da 085f 5f69 6e69 745f 5f29 02da 0473  r..__init__)...s
+000000e0: 656c 66da 076d 6573 7361 6765 a901 da09  elf..message....
+000000f0: 5f5f 636c 6173 735f 5fa9 00fa 6245 3a5c  __class__...bE:\
+00000100: 436f 6465 735c 5079 6368 6172 6d50 726f  Codes\PycharmPro
+00000110: 6a65 6374 735c 666f 6f74 6261 6c6c 2d41  jects\football-A
+00000120: 5049 2d63 6c69 656e 745c 666f 6f74 6261  PI-client\footba
+00000130: 6c6c 4150 4943 6c69 656e 745c 4578 6365  llAPIClient\Exce
+00000140: 7074 696f 6e73 5c41 5049 4c69 6d69 7445  ptions\APILimitE
+00000150: 7863 6565 6465 6445 7272 6f72 2e70 7972  xceededError.pyr
+00000160: 0300 0000 0200 0000 7302 0000 0000 017a  ........s......z
+00000170: 1e41 5049 4c69 6d69 7445 7863 6565 6465  .APILimitExceede
+00000180: 6445 7272 6f72 2e5f 5f69 6e69 745f 5f29  dError.__init__)
+00000190: 05da 085f 5f6e 616d 655f 5fda 0a5f 5f6d  ...__name__..__m
+000001a0: 6f64 756c 655f 5fda 0c5f 5f71 7561 6c6e  odule__..__qualn
+000001b0: 616d 655f 5f72 0300 0000 da0d 5f5f 636c  ame__r......__cl
+000001c0: 6173 7363 656c 6c5f 5f72 0800 0000 7208  asscell__r....r.
+000001d0: 0000 0072 0600 0000 7209 0000 0072 0100  ...r....r....r..
+000001e0: 0000 0100 0000 7302 0000 0008 0172 0100  ......s......r..
+000001f0: 0000 4e29 02da 0945 7863 6570 7469 6f6e  ..N)...Exception
+00000200: 7201 0000 0072 0800 0000 7208 0000 0072  r....r....r....r
+00000210: 0800 0000 7209 0000 00da 083c 6d6f 6475  ....r......<modu
+00000220: 6c65 3e01 0000 00f3 0000 0000            le>.........
```

### Comparing `footballapiclient-0.0.3/footballAPIClient/Exceptions/__pycache__/MissingParametersError.cpython-39.pyc` & `footballapiclient-0.0.4/footballAPIClient/Exceptions/__pycache__/MissingParametersError.cpython-39.pyc`

 * *Files identical despite different names*

### Comparing `footballapiclient-0.0.3/footballAPIClient/footballAPI.py` & `footballapiclient-0.0.4/footballAPIClient/footballAPI.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 import os
 from http.client import HTTPException
 
 import requests
 import logging
 
-from footballAPIClient.Exceptions.InvalidApiKeyError import InvalidApiKeyError
+from footballAPIClient.Exceptions.InternalApiException import InternalApiException
 from footballAPIClient.Exceptions.MissingParametersError import MissingParametersError
 from footballAPIClient.Exceptions.ApiKeyMissingError import ApiKeyMissingError
 from footballAPIClient.helpers.ParameterValidator import ParameterValidator
 from footballAPIClient.Exceptions.APILimitExceededError import APILimitExceededError
 from footballAPIClient._constants import RAPID_API, FOOTBALL_API, FOOTBALL_API_URI, RAPID_API_URI
 
 
@@ -259,15 +259,15 @@
         - To follow your consumption in real time
         - Check the status of our servers
         Note: This call does not count against the daily quota.
         :return: Returns the status json schema
         """
         data = self._get('status')
         if data["errors"]:
-            raise InvalidApiKeyError(data["errors"]["token"])
+            raise InternalApiException(data["errors"])
         return data
 
     def get_countries(self, name: str = None, code: str = None, search: str = None):
         """
         Get the list of available countries for the leagues endpoint.
 
         :param name: The name of the country
```

### Comparing `footballapiclient-0.0.3/footballAPIClient/helpers/__pycache__/ParameterValidator.cpython-39.pyc` & `footballapiclient-0.0.4/footballAPIClient/helpers/__pycache__/ParameterValidator.cpython-39.pyc`

 * *Files identical despite different names*

### Comparing `footballapiclient-0.0.3/footballAPIClient/helpers/ParameterValidator.py` & `footballapiclient-0.0.4/footballAPIClient/helpers/ParameterValidator.py`

 * *Files identical despite different names*

### Comparing `footballapiclient-0.0.3/LICENSE` & `footballapiclient-0.0.4/LICENSE`

 * *Files identical despite different names*

### Comparing `footballapiclient-0.0.3/pyproject.toml` & `footballapiclient-0.0.4/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["poetry-core>=1.0.0"]
 build-backend = "poetry.core.masonry.api"
 
 [tool.poetry]
 name = "footballAPIClient"
-version = "0.0.3"
+version = "0.0.4"
 description = "Python Binding (API wrapper) for the Football API."
 authors = ["Rishav Ganguly <rishav.ganguly07@gmail.com>"]
 readme = "README.md"
 classifiers = [
     "Development Status :: 4 - Beta",
     "Programming Language :: Python :: 3",
     "License :: OSI Approved :: MIT License",
```

### Comparing `footballapiclient-0.0.3/README.md` & `footballapiclient-0.0.4/README.md`

 * *Files identical despite different names*

### Comparing `footballapiclient-0.0.3/PKG-INFO` & `footballapiclient-0.0.4/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: footballapiclient
-Version: 0.0.3
+Version: 0.0.4
 Summary: Python Binding (API wrapper) for the Football API.
 Author: Rishav Ganguly
 Author-email: rishav.ganguly07@gmail.com
 Requires-Python: >=3.7,<4.0
 Classifier: Development Status :: 4 - Beta
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

