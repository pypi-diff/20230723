# Comparing `tmp/infobvc-0.0.3.tar.gz` & `tmp/infobvc-0.0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "infobvc-0.0.3.tar", last modified: Tue Jul 18 22:16:10 2023, max compression
+gzip compressed data, was "C:\Users\USER\Documents\Github_Projects\infobvc\dist\.tmp-_ioeq3bt\infobvc-0.0.4.tar", last modified: Sun Jul 23 16:52:09 2023, max compression
```

## Comparing `infobvc-0.0.3.tar` & `infobvc-0.0.4.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxrwxrwx   0        0        0        0 2023-07-18 22:16:10.251144 infobvc-0.0.3/
--rw-rw-rw-   0        0        0        2 2023-07-18 21:22:29.000000 infobvc-0.0.3/LICENSE
--rw-rw-rw-   0        0        0      643 2023-07-18 22:16:10.251144 infobvc-0.0.3/PKG-INFO
--rw-rw-rw-   0        0        0       97 2023-07-18 21:22:29.000000 infobvc-0.0.3/README.md
--rw-rw-rw-   0        0        0      932 2023-07-18 21:39:17.000000 infobvc-0.0.3/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-07-18 22:16:10.251144 infobvc-0.0.3/setup.cfg
-drwxrwxrwx   0        0        0        0 2023-07-18 22:16:10.123096 infobvc-0.0.3/src/
-drwxrwxrwx   0        0        0        0 2023-07-18 22:16:10.138724 infobvc-0.0.3/src/infobvc/
--rw-rw-rw-   0        0        0        2 2023-07-18 21:22:29.000000 infobvc-0.0.3/src/infobvc/__init__.py
--rw-rw-rw-   0        0        0    15868 2023-07-18 21:38:55.000000 infobvc-0.0.3/src/infobvc/core.py
-drwxrwxrwx   0        0        0        0 2023-07-18 22:16:10.251144 infobvc-0.0.3/src/infobvc.egg-info/
--rw-rw-rw-   0        0        0      643 2023-07-18 22:16:10.000000 infobvc-0.0.3/src/infobvc.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      250 2023-07-18 22:16:10.000000 infobvc-0.0.3/src/infobvc.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-18 22:16:10.000000 infobvc-0.0.3/src/infobvc.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0      141 2023-07-18 22:16:10.000000 infobvc-0.0.3/src/infobvc.egg-info/requires.txt
--rw-rw-rw-   0        0        0        8 2023-07-18 22:16:10.000000 infobvc-0.0.3/src/infobvc.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 16:52:09.925960 infobvc-0.0.4/
+-rw-rw-rw-   0        0        0        2 2023-07-23 16:40:00.000000 infobvc-0.0.4/LICENSE
+-rw-rw-rw-   0        0        0      643 2023-07-23 16:52:09.924963 infobvc-0.0.4/PKG-INFO
+-rw-rw-rw-   0        0        0       97 2023-07-23 16:40:00.000000 infobvc-0.0.4/README.md
+-rw-rw-rw-   0        0        0      951 2023-07-23 16:41:31.000000 infobvc-0.0.4/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-07-23 16:52:09.925960 infobvc-0.0.4/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-07-23 16:52:09.896041 infobvc-0.0.4/src/
+drwxrwxrwx   0        0        0        0 2023-07-23 16:52:09.902025 infobvc-0.0.4/src/infobvc/
+-rw-rw-rw-   0        0        0        2 2023-07-23 16:40:00.000000 infobvc-0.0.4/src/infobvc/__init__.py
+-rw-rw-rw-   0        0        0    15901 2023-07-23 16:42:53.000000 infobvc-0.0.4/src/infobvc/core.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:52:09.922968 infobvc-0.0.4/src/infobvc.egg-info/
+-rw-rw-rw-   0        0        0      643 2023-07-23 16:52:09.000000 infobvc-0.0.4/src/infobvc.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      250 2023-07-23 16:52:09.000000 infobvc-0.0.4/src/infobvc.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 16:52:09.000000 infobvc-0.0.4/src/infobvc.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0      152 2023-07-23 16:52:09.000000 infobvc-0.0.4/src/infobvc.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        8 2023-07-23 16:52:09.000000 infobvc-0.0.4/src/infobvc.egg-info/top_level.txt
```

### Comparing `infobvc-0.0.3/PKG-INFO` & `infobvc-0.0.4/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: infobvc
-Version: 0.0.3
+Version: 0.0.4
 Summary: Get data about Bolsa de Valores de Colombia (BVC)
 Author-email: Fabian Triana <fatrianaa1@gmail.com>
 License: 
         
 Project-URL: Homepage, https://github.com/FabianTriana/infobvc
 Keywords: bvc,stocks,finance,colombia
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `infobvc-0.0.3/pyproject.toml` & `infobvc-0.0.4/pyproject.toml`

 * *Files 5% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 
 [build-system]
 requires = ["setuptools>=61.0.0", "wheel"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "infobvc"
-version = "0.0.3"
+version = "0.0.4"
 description = "Get data about Bolsa de Valores de Colombia (BVC)"
 readme = "README.md"
 authors = [{ name = "Fabian Triana", email = "fatrianaa1@gmail.com" }]
 license = { file = "LICENSE" }
 classifiers = [
     "License :: OSI Approved :: MIT License",
     "Programming Language :: Python",
@@ -19,14 +19,15 @@
 keywords = ["bvc", "stocks", "finance", "colombia"]
 dependencies = [
     "pandas >= 1.5.0",
     "numpy >= 1.22.1",
     "requests >= 2.22.0", 
     "seaborn", 
     "pandas-ta",
+    "matplotlib",
     'tomli; python_version < "3.11"',
 ]
 requires-python = ">=3.9"
 
 [project.optional-dependencies]
 dev = ["black", "bumpver", "isort", "pip-tools", "pytest"]
```

### Comparing `infobvc-0.0.3/src/infobvc/core.py` & `infobvc-0.0.4/src/infobvc/core.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,13 @@
 # Libraries:
 import pandas as pd
 import numpy as np
 import requests
 import seaborn as sns
+import matplotlib.pyplot as plt
 import pandas_ta as ta
 from datetime import date, datetime
 from functools import reduce
 
 
 # Data Info:
 host = 'https://gist.githubusercontent.com/FabianTriana/'
```

### Comparing `infobvc-0.0.3/src/infobvc.egg-info/PKG-INFO` & `infobvc-0.0.4/src/infobvc.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: infobvc
-Version: 0.0.3
+Version: 0.0.4
 Summary: Get data about Bolsa de Valores de Colombia (BVC)
 Author-email: Fabian Triana <fatrianaa1@gmail.com>
 License: 
         
 Project-URL: Homepage, https://github.com/FabianTriana/infobvc
 Keywords: bvc,stocks,finance,colombia
 Classifier: License :: OSI Approved :: MIT License
```

