# Comparing `tmp/goecharger-api-lite-1.1.1.tar.gz` & `tmp/goecharger-api-lite-1.5.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "goecharger-api-lite-1.1.1.tar", last modified: Mon Dec 26 19:22:52 2022, max compression
+gzip compressed data, was "goecharger-api-lite-1.5.0.tar", last modified: Sun Jul 23 18:40:13 2023, max compression
```

## Comparing `goecharger-api-lite-1.1.1.tar` & `goecharger-api-lite-1.5.0.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2022-12-26 19:22:52.606703 goecharger-api-lite-1.1.1/
--rw-r--r--   0 runner    (1001) docker     (123)     1064 2022-12-26 19:22:42.000000 goecharger-api-lite-1.1.1/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     3398 2022-12-26 19:22:52.606703 goecharger-api-lite-1.1.1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2729 2022-12-26 19:22:42.000000 goecharger-api-lite-1.1.1/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2022-12-26 19:22:52.602703 goecharger-api-lite-1.1.1/goecharger/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2022-12-26 19:22:42.000000 goecharger-api-lite-1.1.1/goecharger/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)       89 2022-12-26 19:22:42.000000 goecharger-api-lite-1.1.1/goecharger/excpetion.py
--rw-r--r--   0 runner    (1001) docker     (123)    14891 2022-12-26 19:22:42.000000 goecharger-api-lite-1.1.1/goecharger/goecharger.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2022-12-26 19:22:52.606703 goecharger-api-lite-1.1.1/goecharger_api_lite.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     3398 2022-12-26 19:22:52.000000 goecharger-api-lite-1.1.1/goecharger_api_lite.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      312 2022-12-26 19:22:52.000000 goecharger-api-lite-1.1.1/goecharger_api_lite.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2022-12-26 19:22:52.000000 goecharger-api-lite-1.1.1/goecharger_api_lite.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        8 2022-12-26 19:22:52.000000 goecharger-api-lite-1.1.1/goecharger_api_lite.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       11 2022-12-26 19:22:52.000000 goecharger-api-lite-1.1.1/goecharger_api_lite.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2022-12-26 19:22:52.606703 goecharger-api-lite-1.1.1/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1044 2022-12-26 19:22:42.000000 goecharger-api-lite-1.1.1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 18:40:13.909985 goecharger-api-lite-1.5.0/
+-rw-r--r--   0 runner    (1001) docker     (123)     1064 2023-07-23 18:39:56.000000 goecharger-api-lite-1.5.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     3511 2023-07-23 18:40:13.909985 goecharger-api-lite-1.5.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2842 2023-07-23 18:39:56.000000 goecharger-api-lite-1.5.0/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 18:40:13.909985 goecharger-api-lite-1.5.0/goecharger_api_lite/
+-rw-r--r--   0 runner    (1001) docker     (123)       51 2023-07-23 18:39:56.000000 goecharger-api-lite-1.5.0/goecharger_api_lite/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)       89 2023-07-23 18:39:56.000000 goecharger-api-lite-1.5.0/goecharger_api_lite/exception.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14900 2023-07-23 18:39:56.000000 goecharger-api-lite-1.5.0/goecharger_api_lite/goecharger_api_lite.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 18:40:13.909985 goecharger-api-lite-1.5.0/goecharger_api_lite.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     3511 2023-07-23 18:40:13.000000 goecharger-api-lite-1.5.0/goecharger_api_lite.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      348 2023-07-23 18:40:13.000000 goecharger-api-lite-1.5.0/goecharger_api_lite.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 18:40:13.000000 goecharger-api-lite-1.5.0/goecharger_api_lite.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       15 2023-07-23 18:40:13.000000 goecharger-api-lite-1.5.0/goecharger_api_lite.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       20 2023-07-23 18:40:13.000000 goecharger-api-lite-1.5.0/goecharger_api_lite.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 18:40:13.909985 goecharger-api-lite-1.5.0/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1070 2023-07-23 18:39:56.000000 goecharger-api-lite-1.5.0/setup.py
```

### Comparing `goecharger-api-lite-1.1.1/LICENSE` & `goecharger-api-lite-1.5.0/LICENSE`

 * *Files identical despite different names*

### Comparing `goecharger-api-lite-1.1.1/PKG-INFO` & `goecharger-api-lite-1.5.0/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: goecharger-api-lite
-Version: 1.1.1
+Version: 1.5.0
 Summary: Lightweight Python API for accessing go-eCharger EV wallboxes using local HTTP API v2
 Home-page: https://github.com/bkogler/goecharger-api-lite
 Author: Bernhard Kogler
 Author-email: bernhard.kogler@supersonnig.org
 License: MIT
 Keywords: go-e EV wallbox electric charger Gemini flex HOMEfix HOME+ HTTP API v2
 Classifier: Development Status :: 5 - Production/Stable
@@ -43,15 +43,15 @@
 # Installation
 `pip install goecharger-api-lite`
 
 # Usage Examples
 
 ## Query Status
 ````python
-from goecharger import GoeCharger
+from goecharger_api_lite import GoeCharger
 
 charger = GoeCharger("192.168.1.150") # --> change to your IP
 
 # get full status
 status = charger.get_status(status_type=GoeCharger.STATUS_FULL)
 
 # essential status (car state, wallbox state, wallbox error)
@@ -74,51 +74,53 @@
 }
 ````
 
 ## Set Configuration
 
 ### Interrupt and restart EV charging session
 ````python
-from goecharger import GoeCharger
+from goecharger_api_lite import GoeCharger
 
 charger = GoeCharger("192.168.1.150") # --> change to your IP
 
 # STOP current charging session
 charger.set_charging_mode(charger.SettableValueEnums.ChargingMode.off)
 
 # restart charging session again
 charger.set_charging_mode(charger.SettableValueEnums.ChargingMode.neutral)
 ````
 
 ### Set charge rate (ampere) and number of phases
 ````python
-from goecharger import GoeCharger
+from goecharger_api_lite import GoeCharger
 
 charger = GoeCharger("192.168.1.150") # --> change to your IP
 
 # set to 1 phase, 13 ampere
 charger.set_phase_mode(charger.SettableValueEnum.PhaseMode.one)
 charger.set_ampere(13)
 
 # set to 3 phases, 16 ampere
 charger.set_phase_mode(charger.SettableValueEnum.PhaseMode.three)
 charger.set_ampere(16)
 ````
 
 ### Set Generic API Key
 ````python
-from goecharger import GoeCharger
+from goecharger_api_lite import GoeCharger
 
 charger = GoeCharger("192.168.1.150") # --> change to your IP
 
 # set generic API key (friendly name: "myEVCharger")
 charger.set_key("fna", "myEVCharger")
 ````
 
 # Links
 [goecharger-api-lite GitHub repository](https://github.com/bkogler/goecharger-api-lite)
 
+[goecharger-api-lite on Pypi](https://pypi.org/project/goecharger-api-lite)
+
 [go-E Website (manufacturer)](https://go-e.com)
 
 [go-E API v2 specification](https://github.com/goecharger/go-eCharger-API-v2/blob/main/introduction-en.md)
 
 [go-E API Keys (query status, set configuration)](https://github.com/goecharger/go-eCharger-API-v2/blob/main/apikeys-en.md)
```

### Comparing `goecharger-api-lite-1.1.1/README.md` & `goecharger-api-lite-1.5.0/README.md`

 * *Files 6% similar despite different names*

```diff
@@ -26,15 +26,15 @@
 # Installation
 `pip install goecharger-api-lite`
 
 # Usage Examples
 
 ## Query Status
 ````python
-from goecharger import GoeCharger
+from goecharger_api_lite import GoeCharger
 
 charger = GoeCharger("192.168.1.150") # --> change to your IP
 
 # get full status
 status = charger.get_status(status_type=GoeCharger.STATUS_FULL)
 
 # essential status (car state, wallbox state, wallbox error)
@@ -57,51 +57,53 @@
 }
 ````
 
 ## Set Configuration
 
 ### Interrupt and restart EV charging session
 ````python
-from goecharger import GoeCharger
+from goecharger_api_lite import GoeCharger
 
 charger = GoeCharger("192.168.1.150") # --> change to your IP
 
 # STOP current charging session
 charger.set_charging_mode(charger.SettableValueEnums.ChargingMode.off)
 
 # restart charging session again
 charger.set_charging_mode(charger.SettableValueEnums.ChargingMode.neutral)
 ````
 
 ### Set charge rate (ampere) and number of phases
 ````python
-from goecharger import GoeCharger
+from goecharger_api_lite import GoeCharger
 
 charger = GoeCharger("192.168.1.150") # --> change to your IP
 
 # set to 1 phase, 13 ampere
 charger.set_phase_mode(charger.SettableValueEnum.PhaseMode.one)
 charger.set_ampere(13)
 
 # set to 3 phases, 16 ampere
 charger.set_phase_mode(charger.SettableValueEnum.PhaseMode.three)
 charger.set_ampere(16)
 ````
 
 ### Set Generic API Key
 ````python
-from goecharger import GoeCharger
+from goecharger_api_lite import GoeCharger
 
 charger = GoeCharger("192.168.1.150") # --> change to your IP
 
 # set generic API key (friendly name: "myEVCharger")
 charger.set_key("fna", "myEVCharger")
 ````
 
 # Links
 [goecharger-api-lite GitHub repository](https://github.com/bkogler/goecharger-api-lite)
 
+[goecharger-api-lite on Pypi](https://pypi.org/project/goecharger-api-lite)
+
 [go-E Website (manufacturer)](https://go-e.com)
 
 [go-E API v2 specification](https://github.com/goecharger/go-eCharger-API-v2/blob/main/introduction-en.md)
 
 [go-E API Keys (query status, set configuration)](https://github.com/goecharger/go-eCharger-API-v2/blob/main/apikeys-en.md)
```

### Comparing `goecharger-api-lite-1.1.1/goecharger/goecharger.py` & `goecharger-api-lite-1.5.0/goecharger_api_lite/goecharger_api_lite.py`

 * *Files 1% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 from collections import OrderedDict
 from enum import Enum
 from typing import Union, Tuple, Any, Dict, Optional, Coroutine
 
 import aiohttp
 from aiohttp import ClientTimeout, ClientError, ContentTypeError
 
-from goecharger.excpetion import GoeChargerError
+from goecharger_api_lite.exception import GoeChargerError
 
 
 class GoeCharger:
     """
     Lightweight communication class for go-eCharger EV wall boxes using local HTTP API v2
 
     API documentation:
```

### Comparing `goecharger-api-lite-1.1.1/goecharger_api_lite.egg-info/PKG-INFO` & `goecharger-api-lite-1.5.0/goecharger_api_lite.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: goecharger-api-lite
-Version: 1.1.1
+Version: 1.5.0
 Summary: Lightweight Python API for accessing go-eCharger EV wallboxes using local HTTP API v2
 Home-page: https://github.com/bkogler/goecharger-api-lite
 Author: Bernhard Kogler
 Author-email: bernhard.kogler@supersonnig.org
 License: MIT
 Keywords: go-e EV wallbox electric charger Gemini flex HOMEfix HOME+ HTTP API v2
 Classifier: Development Status :: 5 - Production/Stable
@@ -43,15 +43,15 @@
 # Installation
 `pip install goecharger-api-lite`
 
 # Usage Examples
 
 ## Query Status
 ````python
-from goecharger import GoeCharger
+from goecharger_api_lite import GoeCharger
 
 charger = GoeCharger("192.168.1.150") # --> change to your IP
 
 # get full status
 status = charger.get_status(status_type=GoeCharger.STATUS_FULL)
 
 # essential status (car state, wallbox state, wallbox error)
@@ -74,51 +74,53 @@
 }
 ````
 
 ## Set Configuration
 
 ### Interrupt and restart EV charging session
 ````python
-from goecharger import GoeCharger
+from goecharger_api_lite import GoeCharger
 
 charger = GoeCharger("192.168.1.150") # --> change to your IP
 
 # STOP current charging session
 charger.set_charging_mode(charger.SettableValueEnums.ChargingMode.off)
 
 # restart charging session again
 charger.set_charging_mode(charger.SettableValueEnums.ChargingMode.neutral)
 ````
 
 ### Set charge rate (ampere) and number of phases
 ````python
-from goecharger import GoeCharger
+from goecharger_api_lite import GoeCharger
 
 charger = GoeCharger("192.168.1.150") # --> change to your IP
 
 # set to 1 phase, 13 ampere
 charger.set_phase_mode(charger.SettableValueEnum.PhaseMode.one)
 charger.set_ampere(13)
 
 # set to 3 phases, 16 ampere
 charger.set_phase_mode(charger.SettableValueEnum.PhaseMode.three)
 charger.set_ampere(16)
 ````
 
 ### Set Generic API Key
 ````python
-from goecharger import GoeCharger
+from goecharger_api_lite import GoeCharger
 
 charger = GoeCharger("192.168.1.150") # --> change to your IP
 
 # set generic API key (friendly name: "myEVCharger")
 charger.set_key("fna", "myEVCharger")
 ````
 
 # Links
 [goecharger-api-lite GitHub repository](https://github.com/bkogler/goecharger-api-lite)
 
+[goecharger-api-lite on Pypi](https://pypi.org/project/goecharger-api-lite)
+
 [go-E Website (manufacturer)](https://go-e.com)
 
 [go-E API v2 specification](https://github.com/goecharger/go-eCharger-API-v2/blob/main/introduction-en.md)
 
 [go-E API Keys (query status, set configuration)](https://github.com/goecharger/go-eCharger-API-v2/blob/main/apikeys-en.md)
```

### Comparing `goecharger-api-lite-1.1.1/setup.py` & `goecharger-api-lite-1.5.0/setup.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,18 +1,18 @@
-from setuptools import setup  # type: ignore
+from setuptools import setup # type: ignore
 
 # read the contents of README.md file
 from pathlib import Path
 this_directory = Path(__file__).parent
 long_description = (this_directory / "README.md").read_text()
 
 setup(
     name='goecharger-api-lite',
-    version='1.1.1',
-    packages=['goecharger'],
+    version='1.5.0',
+    packages=['goecharger_api_lite'],
     url='https://github.com/bkogler/goecharger-api-lite',
     license='MIT',
     author='Bernhard Kogler',
     author_email='bernhard.kogler@supersonnig.org',
     description='Lightweight Python API for accessing go-eCharger EV wallboxes using local HTTP API v2',
     long_description=long_description,
     long_description_content_type='text/markdown',
@@ -22,9 +22,10 @@
         "License :: OSI Approved :: MIT License",
         "Operating System :: OS Independent",
     ],
     keywords="go-e EV wallbox electric charger Gemini flex HOMEfix HOME+ HTTP API v2",
     python_requires='>=3.10',
     install_requires=[
         'aiohttp',
+        'aiodns',
     ]
 )
```

