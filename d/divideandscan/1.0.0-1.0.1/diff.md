# Comparing `tmp/divideandscan-1.0.0.tar.gz` & `tmp/divideandscan-1.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "divideandscan-1.0.0.tar", max compression
+gzip compressed data, was "divideandscan-1.0.1.tar", max compression
```

## Comparing `divideandscan-1.0.0.tar` & `divideandscan-1.0.1.tar`

### file list

```diff
@@ -1,19 +1,21 @@
--rw-r--r--   0        0        0     1320 2023-07-23 10:57:37.040373 divideandscan-1.0.0/LICENSE
--rw-r--r--   0        0        0    15194 2023-07-23 10:57:37.040373 divideandscan-1.0.0/README.md
--rw-r--r--   0        0        0       29 2023-07-23 10:57:37.040373 divideandscan-1.0.0/das/__init__.py
--rw-r--r--   0        0        0     4286 2023-07-23 10:57:37.040373 divideandscan-1.0.0/das/common.py
--rwxr-xr-x   0        0        0    14385 2023-07-23 10:57:37.040373 divideandscan-1.0.0/das/divideandscan.py
--rw-r--r--   0        0        0     2614 2023-07-23 10:57:37.040373 divideandscan-1.0.0/das/dns.py
--rw-r--r--   0        0        0     7856 2023-07-23 10:57:37.040373 divideandscan-1.0.0/das/drawnmap.py
--rw-r--r--   0        0        0     2314 2023-07-23 10:57:37.040373 divideandscan-1.0.0/das/parsenmap.py
--rw-r--r--   0        0        0     1723 2023-07-23 10:57:37.040373 divideandscan-1.0.0/das/parsers/__init__.py
--rw-r--r--   0        0        0      665 2023-07-23 10:57:37.040373 divideandscan-1.0.0/das/parsers/masscan.py
--rw-r--r--   0        0        0      596 2023-07-23 10:57:37.040373 divideandscan-1.0.0/das/parsers/naabu.py
--rw-r--r--   0        0        0      865 2023-07-23 10:57:37.040373 divideandscan-1.0.0/das/parsers/nimscan.py
--rw-r--r--   0        0        0      645 2023-07-23 10:57:37.040373 divideandscan-1.0.0/das/parsers/nmap.py
--rw-r--r--   0        0        0      661 2023-07-23 10:57:37.040373 divideandscan-1.0.0/das/parsers/rustscan.py
--rw-r--r--   0        0        0      587 2023-07-23 10:57:37.040373 divideandscan-1.0.0/das/parsers/sx.py
--rw-r--r--   0        0        0     9261 2023-07-23 10:57:37.040373 divideandscan-1.0.0/das/report.py
--rw-r--r--   0        0        0     7224 2023-07-23 10:57:37.040373 divideandscan-1.0.0/das/scan.py
--rw-r--r--   0        0        0     1139 2023-07-23 10:57:37.040373 divideandscan-1.0.0/pyproject.toml
--rw-r--r--   0        0        0    16364 1970-01-01 00:00:00.000000 divideandscan-1.0.0/PKG-INFO
+-rw-r--r--   0        0        0     1320 2023-07-23 11:03:30.223242 divideandscan-1.0.1/LICENSE
+-rw-r--r--   0        0        0    15194 2023-07-23 11:03:30.223242 divideandscan-1.0.1/README.md
+-rw-r--r--   0        0        0       29 2023-07-23 11:03:30.223242 divideandscan-1.0.1/das/__init__.py
+-rw-r--r--   0        0        0     4286 2023-07-23 11:03:30.223242 divideandscan-1.0.1/das/common.py
+-rw-r--r--   0        0        0     2059 2023-07-23 11:03:30.223242 divideandscan-1.0.1/das/db.py
+-rwxr-xr-x   0        0        0    14385 2023-07-23 11:03:30.223242 divideandscan-1.0.1/das/divideandscan.py
+-rw-r--r--   0        0        0     2614 2023-07-23 11:03:30.223242 divideandscan-1.0.1/das/dns.py
+-rw-r--r--   0        0        0     7856 2023-07-23 11:03:30.223242 divideandscan-1.0.1/das/drawnmap.py
+-rw-r--r--   0        0        0     2314 2023-07-23 11:03:30.223242 divideandscan-1.0.1/das/parsenmap.py
+-rw-r--r--   0        0        0     1723 2023-07-23 11:03:30.223242 divideandscan-1.0.1/das/parsers/__init__.py
+-rw-r--r--   0        0        0      665 2023-07-23 11:03:30.223242 divideandscan-1.0.1/das/parsers/masscan.py
+-rw-r--r--   0        0        0      691 2023-07-23 11:03:30.223242 divideandscan-1.0.1/das/parsers/masscan_import.py
+-rw-r--r--   0        0        0      596 2023-07-23 11:03:30.223242 divideandscan-1.0.1/das/parsers/naabu.py
+-rw-r--r--   0        0        0      865 2023-07-23 11:03:30.223242 divideandscan-1.0.1/das/parsers/nimscan.py
+-rw-r--r--   0        0        0      645 2023-07-23 11:03:30.223242 divideandscan-1.0.1/das/parsers/nmap.py
+-rw-r--r--   0        0        0      661 2023-07-23 11:03:30.223242 divideandscan-1.0.1/das/parsers/rustscan.py
+-rw-r--r--   0        0        0      587 2023-07-23 11:03:30.223242 divideandscan-1.0.1/das/parsers/sx.py
+-rw-r--r--   0        0        0     9261 2023-07-23 11:03:30.223242 divideandscan-1.0.1/das/report.py
+-rw-r--r--   0        0        0     7224 2023-07-23 11:03:30.223242 divideandscan-1.0.1/das/scan.py
+-rw-r--r--   0        0        0     1139 2023-07-23 11:03:30.227242 divideandscan-1.0.1/pyproject.toml
+-rw-r--r--   0        0        0    16364 1970-01-01 00:00:00.000000 divideandscan-1.0.1/PKG-INFO
```

### Comparing `divideandscan-1.0.0/LICENSE` & `divideandscan-1.0.1/LICENSE`

 * *Files identical despite different names*

### Comparing `divideandscan-1.0.0/README.md` & `divideandscan-1.0.1/README.md`

 * *Files 0% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 </p>
 
 <p align="center">
   <strong>Divide <strike>Et Impera</strike> And Scan (and also merge the scan results)</strong>
 </p>
 
 <p align="center">
-  <a href="https://github.com/snovvcrash/DivideAndScan/blob/main/pyproject.toml#L3"><img src="https://img.shields.io/badge/version-1.0.0-success" alt="version" /></a>
+  <a href="https://github.com/snovvcrash/DivideAndScan/blob/main/pyproject.toml#L3"><img src="https://img.shields.io/badge/version-1.0.1-success" alt="version" /></a>
   <a href="https://github.com/snovvcrash/DivideAndScan/search?l=python"><img src="https://img.shields.io/badge/python-3.9-blue?logo=python&logoColor=white" alt="python" /></a>
   <a href="https://www.codacy.com/gh/snovvcrash/DivideAndScan/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=snovvcrash/DivideAndScan&amp;utm_campaign=Badge_Grade"><img src="https://app.codacy.com/project/badge/Grade/35f0bdfece9846d7aab3888b01642813" alt="codacy" /></a>
   <a href="https://github.com/snovvcrash/DivideAndScan/actions/workflows/publish-to-pypi.yml"><img src="https://github.com/snovvcrash/DivideAndScan/actions/workflows/publish-to-pypi.yml/badge.svg" alt="pypi" /></a>
   <a href="https://github.com/snovvcrash/DivideAndScan/actions/workflows/publish-to-docker-hub.yml"><img src="https://github.com/snovvcrash/DivideAndScan/actions/workflows/publish-to-docker-hub.yml/badge.svg" alt="docker" /></a>
 </p>
 
 ---
```

### Comparing `divideandscan-1.0.0/das/common.py` & `divideandscan-1.0.1/das/common.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python3
 
 __author__ = '@snovvcrash'
 __site__ = 'https://github.com/snovvcrash/DivideAndScan'
-__version__ = '1.0.0'
+__version__ = '1.0.1'
 
 import time
 import shlex
 import subprocess
 from datetime import datetime, timedelta
 
 BANNER = """\
```

### Comparing `divideandscan-1.0.0/das/divideandscan.py` & `divideandscan-1.0.1/das/divideandscan.py`

 * *Files identical despite different names*

### Comparing `divideandscan-1.0.0/das/dns.py` & `divideandscan-1.0.1/das/dns.py`

 * *Files identical despite different names*

### Comparing `divideandscan-1.0.0/das/drawnmap.py` & `divideandscan-1.0.1/das/drawnmap.py`

 * *Files identical despite different names*

### Comparing `divideandscan-1.0.0/das/parsenmap.py` & `divideandscan-1.0.1/das/parsenmap.py`

 * *Files identical despite different names*

### Comparing `divideandscan-1.0.0/das/parsers/__init__.py` & `divideandscan-1.0.1/das/parsers/__init__.py`

 * *Files identical despite different names*

### Comparing `divideandscan-1.0.0/das/parsers/masscan.py` & `divideandscan-1.0.1/das/parsers/masscan.py`

 * *Files identical despite different names*

### Comparing `divideandscan-1.0.0/das/parsers/naabu.py` & `divideandscan-1.0.1/das/parsers/naabu.py`

 * *Files identical despite different names*

### Comparing `divideandscan-1.0.0/das/parsers/nimscan.py` & `divideandscan-1.0.1/das/parsers/nimscan.py`

 * *Files identical despite different names*

### Comparing `divideandscan-1.0.0/das/parsers/nmap.py` & `divideandscan-1.0.1/das/parsers/nmap.py`

 * *Files identical despite different names*

### Comparing `divideandscan-1.0.0/das/parsers/rustscan.py` & `divideandscan-1.0.1/das/parsers/rustscan.py`

 * *Files identical despite different names*

### Comparing `divideandscan-1.0.0/das/parsers/sx.py` & `divideandscan-1.0.1/das/parsers/sx.py`

 * *Files identical despite different names*

### Comparing `divideandscan-1.0.0/das/report.py` & `divideandscan-1.0.1/das/report.py`

 * *Files identical despite different names*

### Comparing `divideandscan-1.0.0/das/scan.py` & `divideandscan-1.0.1/das/scan.py`

 * *Files identical despite different names*

### Comparing `divideandscan-1.0.0/pyproject.toml` & `divideandscan-1.0.1/pyproject.toml`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "divideandscan"
-version = "1.0.0"
+version = "1.0.1"
 description = "Divide full port scan results and use it for targeted Nmap runs"
 authors = ["Sam Freeside <snovvcrash@protonmail.ch>"]
 license = "BSD-2-Clause"
 readme = "README.md"
 homepage = "https://github.com/snovvcrash/DivideAndScan"
 repository = "https://github.com/snovvcrash/DivideAndScan"
 keywords = ["pentest", "scan", "nmap", "masscan", "rustscan"]
@@ -27,20 +27,20 @@
 python = ">=3.9,<3.12"
 tinydb = "^4.6.1"
 netaddr = "^0.8.0"
 defusedxml = "^0.7.1"
 plotly = "^5.8.2"
 dash = "^2.5.1"
 networkx = "^2.8.4"
-pandas = "^1.4.2"
+pandas = "^2.0.0"
 scipy = "^1.8.1"
 dnspython = "^2.3.0"
 python-nmap = "^0.7.1"
 
 [tool.poetry.dev-dependencies]
 flake8 = "^4.0.1"
 pylint = "^2.12.2"
 twine = "^3.8.0"
 
 [build-system]
-requires = ["poetry-core>=1.0.0"]
+requires = ["poetry-core>=1.0.1"]
 build-backend = "poetry.core.masonry.api"
```

### Comparing `divideandscan-1.0.0/PKG-INFO` & `divideandscan-1.0.1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: divideandscan
-Version: 1.0.0
+Version: 1.0.1
 Summary: Divide full port scan results and use it for targeted Nmap runs
 Home-page: https://github.com/snovvcrash/DivideAndScan
 License: BSD-2-Clause
 Keywords: pentest,scan,nmap,masscan,rustscan
 Author: Sam Freeside
 Author-email: snovvcrash@protonmail.ch
 Requires-Python: >=3.9,<3.12
@@ -16,15 +16,15 @@
 Classifier: Programming Language :: Python :: 3.11
 Classifier: Topic :: Security
 Requires-Dist: dash (>=2.5.1,<3.0.0)
 Requires-Dist: defusedxml (>=0.7.1,<0.8.0)
 Requires-Dist: dnspython (>=2.3.0,<3.0.0)
 Requires-Dist: netaddr (>=0.8.0,<0.9.0)
 Requires-Dist: networkx (>=2.8.4,<3.0.0)
-Requires-Dist: pandas (>=1.4.2,<2.0.0)
+Requires-Dist: pandas (>=2.0.0,<3.0.0)
 Requires-Dist: plotly (>=5.8.2,<6.0.0)
 Requires-Dist: python-nmap (>=0.7.1,<0.8.0)
 Requires-Dist: scipy (>=1.8.1,<2.0.0)
 Requires-Dist: tinydb (>=4.6.1,<5.0.0)
 Project-URL: Repository, https://github.com/snovvcrash/DivideAndScan
 Description-Content-Type: text/markdown
 
@@ -33,15 +33,15 @@
 </p>
 
 <p align="center">
   <strong>Divide <strike>Et Impera</strike> And Scan (and also merge the scan results)</strong>
 </p>
 
 <p align="center">
-  <a href="https://github.com/snovvcrash/DivideAndScan/blob/main/pyproject.toml#L3"><img src="https://img.shields.io/badge/version-1.0.0-success" alt="version" /></a>
+  <a href="https://github.com/snovvcrash/DivideAndScan/blob/main/pyproject.toml#L3"><img src="https://img.shields.io/badge/version-1.0.1-success" alt="version" /></a>
   <a href="https://github.com/snovvcrash/DivideAndScan/search?l=python"><img src="https://img.shields.io/badge/python-3.9-blue?logo=python&logoColor=white" alt="python" /></a>
   <a href="https://www.codacy.com/gh/snovvcrash/DivideAndScan/dashboard?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=snovvcrash/DivideAndScan&amp;utm_campaign=Badge_Grade"><img src="https://app.codacy.com/project/badge/Grade/35f0bdfece9846d7aab3888b01642813" alt="codacy" /></a>
   <a href="https://github.com/snovvcrash/DivideAndScan/actions/workflows/publish-to-pypi.yml"><img src="https://github.com/snovvcrash/DivideAndScan/actions/workflows/publish-to-pypi.yml/badge.svg" alt="pypi" /></a>
   <a href="https://github.com/snovvcrash/DivideAndScan/actions/workflows/publish-to-docker-hub.yml"><img src="https://github.com/snovvcrash/DivideAndScan/actions/workflows/publish-to-docker-hub.yml/badge.svg" alt="docker" /></a>
 </p>
 
 ---
```

#### html2text {}

```diff
@@ -1,20 +1,20 @@
-Metadata-Version: 2.1 Name: divideandscan Version: 1.0.0 Summary: Divide full
+Metadata-Version: 2.1 Name: divideandscan Version: 1.0.1 Summary: Divide full
 port scan results and use it for targeted Nmap runs Home-page: https://
 github.com/snovvcrash/DivideAndScan License: BSD-2-Clause Keywords:
 pentest,scan,nmap,masscan,rustscan Author: Sam Freeside Author-email:
 snovvcrash@protonmail.ch Requires-Python: >=3.9,<3.12 Classifier: Environment
 :: Console Classifier: License :: OSI Approved :: BSD License Classifier:
 Programming Language :: Python :: 3 Classifier: Programming Language :: Python
 :: 3.9 Classifier: Programming Language :: Python :: 3.10 Classifier:
 Programming Language :: Python :: 3.11 Classifier: Topic :: Security Requires-
 Dist: dash (>=2.5.1,<3.0.0) Requires-Dist: defusedxml (>=0.7.1,<0.8.0)
 Requires-Dist: dnspython (>=2.3.0,<3.0.0) Requires-Dist: netaddr
 (>=0.8.0,<0.9.0) Requires-Dist: networkx (>=2.8.4,<3.0.0) Requires-Dist: pandas
-(>=1.4.2,<2.0.0) Requires-Dist: plotly (>=5.8.2,<6.0.0) Requires-Dist: python-
+(>=2.0.0,<3.0.0) Requires-Dist: plotly (>=5.8.2,<6.0.0) Requires-Dist: python-
 nmap (>=0.7.1,<0.8.0) Requires-Dist: scipy (>=1.8.1,<2.0.0) Requires-Dist:
 tinydb (>=4.6.1,<5.0.0) Project-URL: Repository, https://github.com/snovvcrash/
 DivideAndScan Description-Content-Type: text/markdown
                                 [DivideAndScan]
           Divide Et Impera And Scan (and also merge the scan results)
                   [version] [python] [codacy] [pypi] [docker]
 --- **D**ivide**A**nd**S**can is used to efficiently automate port scanning
```

