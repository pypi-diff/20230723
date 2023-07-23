# Comparing `tmp/ak_selenium-0.0.3.tar.gz` & `tmp/ak_selenium-0.0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ak_selenium-0.0.3.tar", last modified: Fri Jan  1 00:00:00 2016, max compression
+gzip compressed data, was "ak_selenium-0.0.4.tar", last modified: Fri Jan  1 00:00:00 2016, max compression
```

## Comparing `ak_selenium-0.0.3.tar` & `ak_selenium-0.0.4.tar`

### file list

```diff
@@ -1,12 +1,12 @@
--rw-r--r--   0        0        0      700 2023-07-18 23:12:31.448394 ak_selenium-0.0.3/.github/workflows/test.yml
--rw-r--r--   0        0        0     2004 2023-07-18 23:12:31.455511 ak_selenium-0.0.3/.gitignore
--rw-r--r--   0        0        0     1100 2023-04-21 15:49:54.583006 ak_selenium-0.0.3/LICENSE
--rw-r--r--   0        0        0     3596 2023-07-18 23:28:48.146334 ak_selenium-0.0.3/README.md
--rw-r--r--   0        0        0    46704 2023-07-18 23:12:31.472797 ak_selenium-0.0.3/assets/Addl_Options.png
--rw-r--r--   0        0        0    80746 2023-07-18 23:12:31.482825 ak_selenium-0.0.3/assets/usage.png
--rw-r--r--   0        0        0      576 2023-07-18 23:13:20.553573 ak_selenium-0.0.3/pyproject.toml
--rw-r--r--   0        0        0      239 2023-07-18 23:34:22.876989 ak_selenium-0.0.3/src/ak_selenium/__init__.py
--rw-r--r--   0        0        0     8235 2023-07-18 23:31:55.901692 ak_selenium-0.0.3/src/ak_selenium/browser.py
--rw-r--r--   0        0        0        0 2023-04-21 17:00:43.559845 ak_selenium-0.0.3/src/tests/__init__.py
--rw-r--r--   0        0        0     1260 2023-07-18 23:20:16.831814 ak_selenium-0.0.3/src/tests/test_browser.py
--rw-r--r--   0        0        0     3983 1970-01-01 00:00:00.000000 ak_selenium-0.0.3/PKG-INFO
+-rw-r--r--   0        0        0      701 2023-07-23 20:36:50.283199 ak_selenium-0.0.4/.github/workflows/test.yml
+-rw-r--r--   0        0        0     2003 2023-06-21 08:31:27.810982 ak_selenium-0.0.4/.gitignore
+-rw-r--r--   0        0        0     1100 2023-06-21 07:45:53.041694 ak_selenium-0.0.4/LICENSE
+-rw-r--r--   0        0        0     3596 2023-07-23 20:36:50.287199 ak_selenium-0.0.4/README.md
+-rw-r--r--   0        0        0    46704 2023-06-21 09:05:19.849182 ak_selenium-0.0.4/assets/Addl_Options.png
+-rw-r--r--   0        0        0    80746 2023-06-21 08:59:29.420231 ak_selenium-0.0.4/assets/usage.png
+-rw-r--r--   0        0        0      612 2023-07-23 20:37:01.367858 ak_selenium-0.0.4/pyproject.toml
+-rw-r--r--   0        0        0      239 2023-07-23 20:39:42.375176 ak_selenium-0.0.4/src/ak_selenium/__init__.py
+-rw-r--r--   0        0        0     8235 2023-07-23 20:36:50.299199 ak_selenium-0.0.4/src/ak_selenium/browser.py
+-rw-r--r--   0        0        0        0 2023-06-21 07:45:53.042694 ak_selenium-0.0.4/src/tests/__init__.py
+-rw-r--r--   0        0        0     1260 2023-07-23 20:36:50.303199 ak_selenium-0.0.4/src/tests/test_browser.py
+-rw-r--r--   0        0        0     4015 1970-01-01 00:00:00.000000 ak_selenium-0.0.4/PKG-INFO
```

### Comparing `ak_selenium-0.0.3/.github/workflows/test.yml` & `ak_selenium-0.0.4/.github/workflows/test.yml`

 * *Files 1% similar despite different names*

```diff
@@ -6,15 +6,15 @@
       - '**/README.md'
 
 jobs:
   build:
     runs-on: '${{ matrix.os }}'
     strategy:
       matrix:
-        python-version: ["3.9", "3.10"]
+        python-version: ["3.10", "3.11"]
         os: [ubuntu-latest, macos-latest, windows-latest]
 
     steps:
       - uses: actions/checkout@v3
       - name: Set up Python ${{ matrix.python-version }}
         uses: actions/setup-python@v4
         with:
```

### Comparing `ak_selenium-0.0.3/.gitignore` & `ak_selenium-0.0.4/.gitignore`

 * *Ordering differences only*

 * *Files 0% similar despite different names*

```diff
@@ -127,8 +127,8 @@
 
 # Pyre type checker
 .pyre/
 .vscode/settings.json
 WebDriver/chromedriver.exe
 nosync*
 *.pkl
-.pypirc
+.pypirc
```

### Comparing `ak_selenium-0.0.3/LICENSE` & `ak_selenium-0.0.4/LICENSE`

 * *Files identical despite different names*

### Comparing `ak_selenium-0.0.3/README.md` & `ak_selenium-0.0.4/README.md`

 * *Files identical despite different names*

### Comparing `ak_selenium-0.0.3/assets/Addl_Options.png` & `ak_selenium-0.0.4/assets/Addl_Options.png`

 * *Files identical despite different names*

### Comparing `ak_selenium-0.0.3/assets/usage.png` & `ak_selenium-0.0.4/assets/usage.png`

 * *Files identical despite different names*

### Comparing `ak_selenium-0.0.3/src/ak_selenium/browser.py` & `ak_selenium-0.0.4/src/ak_selenium/browser.py`

 * *Files identical despite different names*

### Comparing `ak_selenium-0.0.3/src/tests/test_browser.py` & `ak_selenium-0.0.4/src/tests/test_browser.py`

 * *Files identical despite different names*

### Comparing `ak_selenium-0.0.3/PKG-INFO` & `ak_selenium-0.0.4/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,16 +1,17 @@
 Metadata-Version: 2.1
 Name: ak_selenium
-Version: 0.0.3
+Version: 0.0.4
 Summary: Selenium package with requests integration and anti-bot detection measures
 Author-email: Arun Kishore <pypi@rpakishore.co.in>
+Requires-Python: >3.10.0
 Description-Content-Type: text/markdown
 Classifier: License :: OSI Approved :: MIT License
 Requires-Dist: selenium
-Requires-Dist: webdriver-manager
+Requires-Dist: webdriver-manager>=3.9.1
 Requires-Dist: requests
 Requires-Dist: pytest ; extra == "test"
 Requires-Dist: ipykernel ; extra == "test"
 Project-URL: Home, https://github.com/rpakishore/ak_selenium
 Provides-Extra: test
 
 <!--- Heading --->
```

#### html2text {}

```diff
@@ -1,15 +1,16 @@
-Metadata-Version: 2.1 Name: ak_selenium Version: 0.0.3 Summary: Selenium
+Metadata-Version: 2.1 Name: ak_selenium Version: 0.0.4 Summary: Selenium
 package with requests integration and anti-bot detection measures Author-email:
 Arun Kishore
-rpakishore.co.in> Description-Content-Type: text/markdown Classifier: License
-:: OSI Approved :: MIT License Requires-Dist: selenium Requires-Dist:
-webdriver-manager Requires-Dist: requests Requires-Dist: pytest ; extra ==
-"test" Requires-Dist: ipykernel ; extra == "test" Project-URL: Home, https://
-github.com/rpakishore/ak_selenium Provides-Extra: test
+rpakishore.co.in> Requires-Python: >3.10.0 Description-Content-Type: text/
+markdown Classifier: License :: OSI Approved :: MIT License Requires-Dist:
+selenium Requires-Dist: webdriver-manager>=3.9.1 Requires-Dist: requests
+Requires-Dist: pytest ; extra == "test" Requires-Dist: ipykernel ; extra ==
+"test" Project-URL: Home, https://github.com/rpakishore/ak_selenium Provides-
+Extra: test
                            ****** ak_selenium ******
   Selenium package with requests integration and anti-bot detection measures
           *** Documentation  Â·  Report_Bug  Â·  Request_Feature ***
 
 ![GitHub commit activity](https://img.shields.io/github/commit-activity/m/
 rpakishore/ak_selenium) ![GitHub last commit](https://img.shields.io/github/
 last-commit/rpakishore/ak_selenium) [![tests](https://github.com/rpakishore/
```

