# Comparing `tmp/webdriver_manager-3.9.0.tar.gz` & `tmp/webdriver_manager-3.9.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/webdriver_manager-3.9.0.tar", last modified: Sat Jul 22 15:06:22 2023, max compression
+gzip compressed data, was "dist/webdriver_manager-3.9.1.tar", last modified: Sun Jul 23 15:07:42 2023, max compression
```

## Comparing `webdriver_manager-3.9.0.tar` & `webdriver_manager-3.9.1.tar`

### file list

```diff
@@ -1,51 +1,53 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 15:06:22.000000 webdriver_manager-3.9.0/
--rw-r--r--   0 runner    (1001) docker     (123)    11328 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)    11203 2023-07-22 15:06:22.000000 webdriver_manager-3.9.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)    10136 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/README.md
--rw-r--r--   0 runner    (1001) docker     (123)      407 2023-07-22 15:06:22.000000 webdriver_manager-3.9.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     2127 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 15:06:22.000000 webdriver_manager-3.9.0/tests/
--rw-r--r--   0 runner    (1001) docker     (123)     2043 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/tests/test_brave_driver.py
--rw-r--r--   0 runner    (1001) docker     (123)     3043 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/tests/test_chrome_driver.py
--rw-r--r--   0 runner    (1001) docker     (123)     1605 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/tests/test_chromium_driver.py
--rw-r--r--   0 runner    (1001) docker     (123)      753 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/tests/test_custom_http_client.py
--rw-r--r--   0 runner    (1001) docker     (123)      897 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/tests/test_custom_logger.py
--rw-r--r--   0 runner    (1001) docker     (123)     2112 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/tests/test_downloader.py
--rw-r--r--   0 runner    (1001) docker     (123)     2378 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/tests/test_edge_driver.py
--rw-r--r--   0 runner    (1001) docker     (123)     1983 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/tests/test_firefox_manager.py
--rw-r--r--   0 runner    (1001) docker     (123)     1555 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/tests/test_ie_driver.py
--rwxr-xr-x   0 runner    (1001) docker     (123)     2742 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/tests/test_opera_manager.py
--rw-r--r--   0 runner    (1001) docker     (123)      372 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/tests/test_silent_global_logs.py
--rw-r--r--   0 runner    (1001) docker     (123)     1062 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/tests/test_utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 15:06:22.000000 webdriver_manager-3.9.0/webdriver_manager/
--rw-r--r--   0 runner    (1001) docker     (123)       22 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/webdriver_manager/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1510 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/webdriver_manager/chrome.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 15:06:22.000000 webdriver_manager-3.9.0/webdriver_manager/core/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/webdriver_manager/core/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2407 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/webdriver_manager/core/archive.py
--rw-r--r--   0 runner    (1001) docker     (123)      740 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/webdriver_manager/core/config.py
--rw-r--r--   0 runner    (1001) docker     (123)      218 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/webdriver_manager/core/constants.py
--rw-r--r--   0 runner    (1001) docker     (123)     1296 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/webdriver_manager/core/download_manager.py
--rw-r--r--   0 runner    (1001) docker     (123)     2912 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/webdriver_manager/core/driver.py
--rw-r--r--   0 runner    (1001) docker     (123)     5338 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/webdriver_manager/core/driver_cache.py
--rw-r--r--   0 runner    (1001) docker     (123)     1331 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/webdriver_manager/core/http.py
--rw-r--r--   0 runner    (1001) docker     (123)      686 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/webdriver_manager/core/logger.py
--rw-r--r--   0 runner    (1001) docker     (123)     1133 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/webdriver_manager/core/manager.py
--rw-r--r--   0 runner    (1001) docker     (123)    12151 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/webdriver_manager/core/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 15:06:22.000000 webdriver_manager-3.9.0/webdriver_manager/drivers/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/webdriver_manager/drivers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3393 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/webdriver_manager/drivers/chrome.py
--rw-r--r--   0 runner    (1001) docker     (123)     1954 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/webdriver_manager/drivers/edge.py
--rw-r--r--   0 runner    (1001) docker     (123)     2288 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/webdriver_manager/drivers/firefox.py
--rw-r--r--   0 runner    (1001) docker     (123)     2722 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/webdriver_manager/drivers/ie.py
--rw-r--r--   0 runner    (1001) docker     (123)     1700 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/webdriver_manager/drivers/opera.py
--rw-r--r--   0 runner    (1001) docker     (123)     1409 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/webdriver_manager/firefox.py
--rw-r--r--   0 runner    (1001) docker     (123)     2335 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/webdriver_manager/microsoft.py
--rwxr-xr-x   0 runner    (1001) docker     (123)     1743 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/webdriver_manager/opera.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-22 15:05:57.000000 webdriver_manager-3.9.0/webdriver_manager/py.typed
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 15:06:22.000000 webdriver_manager-3.9.0/webdriver_manager.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)    11203 2023-07-22 15:06:22.000000 webdriver_manager-3.9.0/webdriver_manager.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1339 2023-07-22 15:06:22.000000 webdriver_manager-3.9.0/webdriver_manager.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-22 15:06:22.000000 webdriver_manager-3.9.0/webdriver_manager.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-22 15:06:22.000000 webdriver_manager-3.9.0/webdriver_manager.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       18 2023-07-22 15:06:22.000000 webdriver_manager-3.9.0/webdriver_manager.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:07:42.000000 webdriver_manager-3.9.1/
+-rw-r--r--   0 runner    (1001) docker     (123)    11328 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)    11227 2023-07-23 15:07:42.000000 webdriver_manager-3.9.1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    10160 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      407 2023-07-23 15:07:42.000000 webdriver_manager-3.9.1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     2111 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:07:42.000000 webdriver_manager-3.9.1/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     2238 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/tests/test_brave_driver.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3332 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/tests/test_chrome_driver.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1845 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/tests/test_chromium_driver.py
+-rw-r--r--   0 runner    (1001) docker     (123)      753 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/tests/test_custom_http_client.py
+-rw-r--r--   0 runner    (1001) docker     (123)      897 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/tests/test_custom_logger.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2465 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/tests/test_downloader.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2674 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/tests/test_edge_driver.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2306 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/tests/test_firefox_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1822 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/tests/test_ie_driver.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     2974 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/tests/test_opera_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)      372 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/tests/test_silent_global_logs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1062 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/tests/test_utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:07:42.000000 webdriver_manager-3.9.1/webdriver_manager/
+-rw-r--r--   0 runner    (1001) docker     (123)       22 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/webdriver_manager/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1648 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/webdriver_manager/chrome.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:07:42.000000 webdriver_manager-3.9.1/webdriver_manager/core/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/webdriver_manager/core/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      632 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/webdriver_manager/core/archive.py
+-rw-r--r--   0 runner    (1001) docker     (123)      740 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/webdriver_manager/core/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)      218 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/webdriver_manager/core/constants.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1303 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/webdriver_manager/core/download_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3020 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/webdriver_manager/core/driver.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6109 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/webdriver_manager/core/driver_cache.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3628 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/webdriver_manager/core/file_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1249 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/webdriver_manager/core/http.py
+-rw-r--r--   0 runner    (1001) docker     (123)      686 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/webdriver_manager/core/logger.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1201 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/webdriver_manager/core/manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8804 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/webdriver_manager/core/os_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1949 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/webdriver_manager/core/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:07:42.000000 webdriver_manager-3.9.1/webdriver_manager/drivers/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/webdriver_manager/drivers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3548 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/webdriver_manager/drivers/chrome.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2000 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/webdriver_manager/drivers/edge.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2309 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/webdriver_manager/drivers/firefox.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2786 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/webdriver_manager/drivers/ie.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1799 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/webdriver_manager/drivers/opera.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1646 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/webdriver_manager/firefox.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2673 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/webdriver_manager/microsoft.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     2057 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/webdriver_manager/opera.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 15:07:13.000000 webdriver_manager-3.9.1/webdriver_manager/py.typed
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:07:42.000000 webdriver_manager-3.9.1/webdriver_manager.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)    11227 2023-07-23 15:07:42.000000 webdriver_manager-3.9.1/webdriver_manager.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1415 2023-07-23 15:07:42.000000 webdriver_manager-3.9.1/webdriver_manager.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 15:07:42.000000 webdriver_manager-3.9.1/webdriver_manager.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       33 2023-07-23 15:07:42.000000 webdriver_manager-3.9.1/webdriver_manager.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       18 2023-07-23 15:07:42.000000 webdriver_manager-3.9.1/webdriver_manager.egg-info/top_level.txt
```

### Comparing `webdriver_manager-3.9.0/LICENSE` & `webdriver_manager-3.9.1/LICENSE`

 * *Files identical despite different names*

### Comparing `webdriver_manager-3.9.0/PKG-INFO` & `webdriver_manager-3.9.1/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: webdriver_manager
-Version: 3.9.0
+Version: 3.9.1
 Summary: Library provides the way to automatically manage drivers for different browsers
 Home-page: https://github.com/SergeyPirogov/webdriver_manager
 Author: Sergey Pirogov
 Author-email: automationremarks@gmail.com
 Keywords: testing,selenium,driver,test automation
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Intended Audience :: Information Technology
@@ -221,14 +221,21 @@
 
 ```python
 from webdriver_manager.core.utils import read_version_from_cmd, PATTERN
 version = read_version_from_cmd("/usr/bin/firefox-bin --version", PATTERN["firefox"])
 driver_binary = FirefoxDriverManager(version=version).install()
 ```
 
+#### Custom Cache and File manager
+
+```python
+cache_manager = DriverCacheManager(file_manager=FileManager())
+manager = ChromeDriverManager(cache_manager=cache_manager)
+```
+
 ## Configuration
 
 **webdriver_manager** has several configuration variables you can be interested in.
 Any variable can be set using either .env file or via python directly
 
 ### `GH_TOKEN`
 **webdriver_manager** downloading some webdrivers from their official GitHub repositories but GitHub has [limitations](https://docs.github.com/en/rest/overview/resources-in-the-rest-api#rate-limiting) like 60 requests per hour for unauthenticated users.
@@ -256,23 +263,14 @@
 ```python
 import logging
 import os
 
 os.environ['WDM_LOG'] = str(logging.NOTSET)
 ```
 
-### `WDM_PROGRESS_BAR`
-Turn off the progress bar which is displayed on downloads:
-
-```python
-import os
-
-os.environ['WDM_PROGRESS_BAR'] = str(0)
-```
-
 ### `WDM_LOCAL`
 By default, all driver binaries are saved to user.home/.wdm folder. You can override this setting and save binaries to project.root/.wdm.
 
 ```python
 import os
 
 os.environ['WDM_LOCAL'] = '1'
```

### Comparing `webdriver_manager-3.9.0/README.md` & `webdriver_manager-3.9.1/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -196,14 +196,21 @@
 
 ```python
 from webdriver_manager.core.utils import read_version_from_cmd, PATTERN
 version = read_version_from_cmd("/usr/bin/firefox-bin --version", PATTERN["firefox"])
 driver_binary = FirefoxDriverManager(version=version).install()
 ```
 
+#### Custom Cache and File manager
+
+```python
+cache_manager = DriverCacheManager(file_manager=FileManager())
+manager = ChromeDriverManager(cache_manager=cache_manager)
+```
+
 ## Configuration
 
 **webdriver_manager** has several configuration variables you can be interested in.
 Any variable can be set using either .env file or via python directly
 
 ### `GH_TOKEN`
 **webdriver_manager** downloading some webdrivers from their official GitHub repositories but GitHub has [limitations](https://docs.github.com/en/rest/overview/resources-in-the-rest-api#rate-limiting) like 60 requests per hour for unauthenticated users.
@@ -231,23 +238,14 @@
 ```python
 import logging
 import os
 
 os.environ['WDM_LOG'] = str(logging.NOTSET)
 ```
 
-### `WDM_PROGRESS_BAR`
-Turn off the progress bar which is displayed on downloads:
-
-```python
-import os
-
-os.environ['WDM_PROGRESS_BAR'] = str(0)
-```
-
 ### `WDM_LOCAL`
 By default, all driver binaries are saved to user.home/.wdm folder. You can override this setting and save binaries to project.root/.wdm.
 
 ```python
 import os
 
 os.environ['WDM_LOCAL'] = '1'
```

### Comparing `webdriver_manager-3.9.0/setup.py` & `webdriver_manager-3.9.1/setup.py`

 * *Files 4% similar despite different names*

```diff
@@ -19,15 +19,15 @@
 setuptools.setup(
     name='webdriver_manager',
     python_requires=">=3.7",
     long_description=readme,
     long_description_content_type="text/markdown",
     packages=setuptools.find_packages(include=['webdriver_manager*']),
     include_package_data=True,
-    version='3.9.0',
+    version='3.9.1',
     description='Library provides the way to automatically manage drivers for different browsers',
     author='Sergey Pirogov',
     author_email='automationremarks@gmail.com',
     url='https://github.com/SergeyPirogov/webdriver_manager',
     keywords=['testing', 'selenium', 'driver', 'test automation'],
     classifiers=[
         'License :: OSI Approved :: Apache Software License',
@@ -44,14 +44,13 @@
         'Operating System :: POSIX',
         'Operating System :: Unix',
         'Operating System :: MacOS',
     ],
     install_requires=[
         'requests',
         'python-dotenv',
-        'tqdm',
         'packaging'
     ],
     package_data={
         "webdriver_manager": ["py.typed"]
     },
 )
```

### Comparing `webdriver_manager-3.9.0/tests/test_brave_driver.py` & `webdriver_manager-3.9.1/tests/test_brave_driver.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,27 +1,28 @@
 import os
 
 import pytest
 from selenium import webdriver
 
 from webdriver_manager.chrome import ChromeDriverManager
+from webdriver_manager.core.driver_cache import DriverCacheManager
 from webdriver_manager.core.logger import log
-from webdriver_manager.core.utils import ChromeType, os_name, OSType
+from webdriver_manager.core.os_manager import ChromeType, OSType, OperationSystemManager
 
 
 def test_driver_with_ssl_verify_disabled_can_be_downloaded(ssl_verify_enable):
     os.environ['WDM_SSL_VERIFY'] = '0'
     custom_path = os.path.join(
         os.path.dirname(os.path.dirname(__file__)),
         '.wdm',
         "ssl_disabled",
     )
     driver_path = ChromeDriverManager(
-        version="87.0.4280.88",
-        path=custom_path,
+        driver_version="87.0.4280.88",
+        cache_manager=DriverCacheManager(custom_path),
         chrome_type=ChromeType.BRAVE,
     ).install()
 
     assert os.path.exists(driver_path)
 
 
 def test_brave_manager_with_specific_version():
@@ -50,10 +51,11 @@
     with pytest.raises(ValueError) as ex:
         ChromeDriverManager("0.2", chrome_type=ChromeType.BRAVE).install()
     assert "There is no such driver by url" in ex.value.args[0]
 
 
 @pytest.mark.parametrize('os_type', ['win32', 'win64'])
 def test_can_get_brave_for_win(os_type):
-    path = ChromeDriverManager(version="83.0.4103.39", os_type=os_type,
+    path = ChromeDriverManager(driver_version="83.0.4103.39",
+                               os_system_manager=OperationSystemManager(os_type),
                                chrome_type=ChromeType.BRAVE).install()
     assert os.path.exists(path)
```

### Comparing `webdriver_manager-3.9.0/tests/test_chrome_driver.py` & `webdriver_manager-3.9.1/tests/test_opera_manager.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,91 +1,79 @@
-import json
+import glob
 import os
 
 import pytest
 from selenium import webdriver
+from selenium.webdriver.chrome.service import Service
 
-from webdriver_manager.chrome import ChromeDriverManager
-from webdriver_manager.core.constants import ROOT_FOLDER_NAME
-from selenium.webdriver.chrome.service import Service as ChromeService
+from webdriver_manager.core.driver_cache import DriverCacheManager
+from webdriver_manager.core.os_manager import OperationSystemManager
+from webdriver_manager.opera import OperaDriverManager
 
-os.environ.setdefault("WDM_LOCAL", "true")
 
-
-def test_chrome_manager_with_cache(delete_drivers_dir):
-    ChromeDriverManager().install()
-    driver_binary = ChromeDriverManager().install()
-    assert os.path.exists(driver_binary)
-
-
-def test_chrome_manager_with_specific_version(delete_drivers_dir):
-    driver_binary = ChromeDriverManager("87.0.4280.88").install()
-    assert os.path.exists(driver_binary)
-
-
-def test_106_0_5249_61_chrome_version(delete_drivers_dir):
-    driver_binary = ChromeDriverManager("106.0.5249.61").install()
-    assert os.path.exists(driver_binary)
-
-
-def test_chrome_manager_with_project_root_local_folder(delete_drivers_dir):
-    os.environ['WDM_LOCAL'] = "1"
-    driver_binary = ChromeDriverManager("87.0.4280.88").install()
-    os.environ['WDM_LOCAL'] = "0"
-    assert os.path.exists(driver_binary)
-
-
-def test_driver_can_be_saved_to_custom_path():
-    custom_path = os.path.join(os.path.dirname(os.path.dirname(__file__)), "custom")
-    path = ChromeDriverManager(version="87.0.4280.88", path=custom_path).install()
-    assert os.path.exists(path)
-    assert custom_path in path
-
-
-def test_chrome_manager_with_wrong_version():
-    with pytest.raises(ValueError) as ex:
-        ChromeDriverManager("0.2").install()
-    assert "There is no such driver by url" in ex.value.args[0]
-
-
-def test_chrome_manager_with_selenium():
-    driver_path = ChromeDriverManager().install()
-    driver = webdriver.Chrome(service=ChromeService(driver_path))
-    driver.get("http://automation-remarks.com")
-    driver.close()
+def test_opera_driver_manager_with_correct_version():
+    driver_path = OperaDriverManager("v.2.45").install()
+    assert os.path.exists(driver_path)
 
 
 def test_driver_with_ssl_verify_disabled_can_be_downloaded(ssl_verify_enable):
     os.environ['WDM_SSL_VERIFY'] = '0'
-    custom_path = os.path.join(os.path.dirname(
-        os.path.dirname(__file__)),
+    custom_path = os.path.join(
+        os.path.dirname(os.path.dirname(__file__)),
         "ssl_disabled",
     )
-    driver_path = ChromeDriverManager(path=custom_path).install()
+    driver_path = OperaDriverManager(cache_manager=DriverCacheManager(custom_path)).install()
     os.environ['WDM_SSL_VERIFY'] = '1'
     assert os.path.exists(driver_path)
 
 
-def test_chrome_manager_cached_driver_with_selenium():
-    custom_path = os.path.join(os.path.dirname(os.path.dirname(__file__)), "custom-cache")
-    manager = ChromeDriverManager(path=custom_path)
-    driver = webdriver.Chrome(manager.install())
-    driver.get("http://automation-remarks.com")
+def test_operadriver_manager_with_selenium():
+    driver_path = OperaDriverManager().install()
+    options = webdriver.ChromeOptions()
+    options.add_experimental_option('w3c', True)
+    os_type = OperationSystemManager().get_os_type()
+    if os_type in ["win64", "win32"]:
+        paths = [f for f in glob.glob(
+            f"C:/Users/{os.getlogin()}/AppData/Local/Programs/Opera/**",
+            recursive=True
+        )]
+        for path in paths:
+            if os.path.isfile(path) and path.endswith("opera.exe"):
+                options.binary_location = path
+    elif (
+            (os_type in ["linux64", "linux32"])
+            and not os.path.exists('/usr/bin/opera')
+    ):
+        options.binary_location = "/usr/bin/opera"
+    elif os_type in "mac64":
+        options.binary_location = "/Applications/Opera.app/Contents/MacOS/Opera"
+    web_service = Service(driver_path)
+    web_service.start()
+
+    opera_driver = webdriver.Remote(web_service.service_url, options=options)
+    opera_driver.get("http://automation-remarks.com")
+    opera_driver.quit()
 
-    metadata_file = os.path.join(custom_path, ROOT_FOLDER_NAME, 'drivers.json')
 
-    with open(metadata_file) as json_file:
-        data = json.load(json_file)
+def test_opera_driver_manager_with_wrong_version():
+    with pytest.raises(ValueError) as ex:
+        OperaDriverManager("0.2").install()
 
-    for k in data.keys():
-        data[k]['timestamp'] = "08/06/2019"
+    assert "There is no such driver by url " \
+           "https://api.github.com/repos/operasoftware/operachromiumdriver/" \
+           "releases/tags/0.2" in ex.value.args[0]
 
-    with open(metadata_file, 'w') as outfile:
-        json.dump(data, outfile)
 
-    ChromeDriverManager(path=custom_path).install()
+@pytest.mark.parametrize('path', ['.', None])
+def test_opera_driver_manager_with_correct_version_and_token(path):
+    driver_path = OperaDriverManager(version="v.2.45", cache_manager=DriverCacheManager(path)).install()
+    assert os.path.exists(driver_path)
 
 
-@pytest.mark.parametrize('os_type', ['win32', 'win64', 'mac64', 'mac64_m1'])
-def test_can_get_chrome_for_os(os_type):
-    path = ChromeDriverManager(os_type=os_type).install()
-    assert os.path.exists(path)
+@pytest.mark.parametrize('os_type', ['win32',
+                                     'win64',
+                                     'linux64',
+                                     'mac64'])
+def test_can_get_driver_from_cache(os_type):
+    OperaDriverManager(os_system_manager=OperationSystemManager(os_type)).install()
+    driver_path = OperaDriverManager(os_system_manager=OperationSystemManager(os_type)).install()
+    assert os.path.exists(driver_path)
```

### Comparing `webdriver_manager-3.9.0/tests/test_chromium_driver.py` & `webdriver_manager-3.9.1/tests/test_chromium_driver.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,48 +1,50 @@
 import os
 
 import pytest
 
 from webdriver_manager.chrome import ChromeDriverManager
-from webdriver_manager.core.utils import ChromeType
+from webdriver_manager.core.driver_cache import DriverCacheManager
+from webdriver_manager.core.os_manager import ChromeType, OperationSystemManager
 
 
 def test_driver_with_ssl_verify_disabled_can_be_downloaded(ssl_verify_enable):
     os.environ['WDM_SSL_VERIFY'] = '0'
     custom_path = os.path.join(
         os.path.dirname(os.path.dirname(__file__)),
         "ssl_disabled",
     )
     driver_path = ChromeDriverManager(
-        version="87.0.4280.88",
-        path=custom_path,
+        driver_version="87.0.4280.88",
+        cache_manager=DriverCacheManager(custom_path),
         chrome_type=ChromeType.CHROMIUM,
     ).install()
 
     assert os.path.exists(driver_path)
 
 
 def test_chromium_manager_with_specific_version():
     bin_path = ChromeDriverManager("87.0.4280.88", chrome_type=ChromeType.CHROMIUM).install()
     assert os.path.exists(bin_path)
 
 
 def test_driver_can_be_saved_to_custom_path():
     custom_path = os.path.join(os.path.dirname(os.path.dirname(__file__)), "custom")
 
-    path = ChromeDriverManager(version="87.0.4280.88", path=custom_path,
+    path = ChromeDriverManager(driver_version="87.0.4280.88", cache_manager=DriverCacheManager(custom_path),
                                chrome_type=ChromeType.CHROMIUM).install()
     assert os.path.exists(path)
     assert custom_path in path
 
 
 def test_chromium_manager_with_wrong_version():
     with pytest.raises(ValueError) as ex:
         ChromeDriverManager("0.2", chrome_type=ChromeType.CHROMIUM).install()
     assert "There is no such driver by url" in ex.value.args[0]
 
 
 @pytest.mark.parametrize('os_type', ['win32', 'win64'])
 def test_can_get_chromium_for_win(os_type):
-    path = ChromeDriverManager(version="83.0.4103.39", os_type=os_type,
+    path = ChromeDriverManager(driver_version="83.0.4103.39",
+                               os_system_manager=OperationSystemManager(os_type),
                                chrome_type=ChromeType.CHROMIUM).install()
     assert os.path.exists(path)
```

### Comparing `webdriver_manager-3.9.0/tests/test_custom_http_client.py` & `webdriver_manager-3.9.1/tests/test_custom_http_client.py`

 * *Files identical despite different names*

### Comparing `webdriver_manager-3.9.0/tests/test_custom_logger.py` & `webdriver_manager-3.9.1/tests/test_custom_logger.py`

 * *Files identical despite different names*

### Comparing `webdriver_manager-3.9.0/tests/test_downloader.py` & `webdriver_manager-3.9.1/tests/test_downloader.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,41 +1,45 @@
 import os
 
 import pytest
 
 from webdriver_manager.core.constants import DEFAULT_PROJECT_ROOT_CACHE_PATH
 from webdriver_manager.core.download_manager import WDMDownloadManager
+from webdriver_manager.core.file_manager import FileManager
 from webdriver_manager.core.http import WDMHttpClient
-from webdriver_manager.core.utils import save_file, ChromeType
+from webdriver_manager.core.os_manager import OperationSystemManager, ChromeType
 from webdriver_manager.drivers.chrome import ChromeDriver
 
 download_manager = WDMDownloadManager()
+file_manager = FileManager(OperationSystemManager())
 
 
 def test_can_download_driver_as_zip_file(delete_drivers_dir):
     file = download_manager.download_file("http://chromedriver.storage.googleapis.com/2.26/chromedriver_win32.zip")
     assert file.filename == "chromedriver_win32.zip"
-    archive = save_file(file, DEFAULT_PROJECT_ROOT_CACHE_PATH)
+    archive = file_manager.save_archive_file(file, DEFAULT_PROJECT_ROOT_CACHE_PATH)
     assert archive.file_path == f"{DEFAULT_PROJECT_ROOT_CACHE_PATH}{os.sep}{file.filename}"
-    assert archive.unpack(DEFAULT_PROJECT_ROOT_CACHE_PATH) == ["chromedriver.exe"]
+    assert file_manager.unpack_archive(archive, DEFAULT_PROJECT_ROOT_CACHE_PATH) == ["chromedriver.exe"]
 
 
 def test_can_download_driver_as_tar_gz(delete_drivers_dir):
     file = download_manager.download_file(
         "https://github.com/mozilla/geckodriver/releases/download/v0.26.0/geckodriver-v0.26.0-linux32.tar.gz")
     assert file.filename == 'geckodriver-v0.26.0-linux32.tar.gz'
-    archive = save_file(file, DEFAULT_PROJECT_ROOT_CACHE_PATH)
+    archive = file_manager.save_archive_file(file, DEFAULT_PROJECT_ROOT_CACHE_PATH)
     assert archive.file_path == f"{DEFAULT_PROJECT_ROOT_CACHE_PATH}{os.sep}{file.filename}"
-    assert archive.unpack(DEFAULT_PROJECT_ROOT_CACHE_PATH) == ["geckodriver"]
+    assert file_manager.unpack_archive(archive, DEFAULT_PROJECT_ROOT_CACHE_PATH) == ["geckodriver"]
 
 
 @pytest.mark.parametrize('version', ["2.26"])
 def test_can_download_chrome_driver(delete_drivers_dir, version):
-    driver = ChromeDriver(name="chromedriver", version=version, os_type="win32",
+    driver = ChromeDriver(name="chromedriver",
+                          driver_version=version,
+                          os_system_manager=OperationSystemManager("win32"),
                           url="http://chromedriver.storage.googleapis.com",
                           latest_release_url="http://chromedriver.storage.googleapis.com/LATEST_RELEASE",
                           chrome_type=ChromeType.GOOGLE, http_client=WDMHttpClient())
 
     file = download_manager.download_file(driver.get_driver_download_url())
     assert file.filename == "chromedriver_win32.zip"
-    archive = save_file(file, DEFAULT_PROJECT_ROOT_CACHE_PATH)
-    assert "chromedriver.exe" in archive.unpack(DEFAULT_PROJECT_ROOT_CACHE_PATH)
+    archive = file_manager.save_archive_file(file, DEFAULT_PROJECT_ROOT_CACHE_PATH)
+    assert "chromedriver.exe" in file_manager.unpack_archive(archive, DEFAULT_PROJECT_ROOT_CACHE_PATH)
```

### Comparing `webdriver_manager-3.9.0/tests/test_edge_driver.py` & `webdriver_manager-3.9.1/tests/test_edge_driver.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,68 +1,70 @@
 import os
 import re
 
 import pytest
 from selenium import webdriver
+from selenium.webdriver.edge.service import Service
 
+from webdriver_manager.core.driver_cache import DriverCacheManager
+from webdriver_manager.core.os_manager import PATTERN, ChromeType, OperationSystemManager
 from webdriver_manager.microsoft import EdgeChromiumDriverManager
-from webdriver_manager.core.utils import PATTERN, ChromeType
 
 
 def test_edge_manager_with_selenium():
     driver_path = EdgeChromiumDriverManager().install()
-    driver = webdriver.Edge(executable_path=driver_path, capabilities={})
+    driver = webdriver.Edge(service=Service(driver_path))
     driver.get("http://automation-remarks.com")
     driver.quit()
 
 
 def test_driver_with_ssl_verify_disabled_can_be_downloaded(ssl_verify_enable):
     os.environ['WDM_SSL_VERIFY'] = '0'
     custom_path = os.path.join(
         os.path.dirname(os.path.dirname(__file__)),
         "ssl_disabled",
     )
-    driver_path = EdgeChromiumDriverManager(path=custom_path).install()
+    driver_path = EdgeChromiumDriverManager(cache_manager=DriverCacheManager(custom_path)).install()
     os.environ['WDM_SSL_VERIFY'] = '1'
     assert os.path.exists(driver_path)
 
 
 def test_edge_manager_with_wrong_version():
     with pytest.raises(ValueError) as ex:
         EdgeChromiumDriverManager(
             version="0.2",
-            os_type='win64',
+            os_system_manager=OperationSystemManager("win64")
         ).install()
 
     assert (
                "There is no such driver by url "
                "https://msedgedriver.azureedge.net/0.2/edgedriver_win64.zip"
            ) in ex.value.args[0]
 
 
 @pytest.mark.parametrize('os_type', ['win32', 'win64', 'mac64', 'linux64'])
 @pytest.mark.parametrize('specific_version', ['86.0.600.0'])
 def test_edge_with_specific_version(os_type, specific_version):
     bin_path = EdgeChromiumDriverManager(
         version=specific_version,
-        os_type=os_type,
+        os_system_manager=OperationSystemManager(os_type),
     ).install()
     assert os.path.exists(bin_path)
 
 
 @pytest.mark.parametrize('os_type', ['win32', 'win64', 'mac64', 'linux64'])
 @pytest.mark.parametrize('specific_version', ['87.0.637.0'])
 def test_can_get_edge_driver_from_cache(os_type, specific_version):
     EdgeChromiumDriverManager(
         version=specific_version,
-        os_type=os_type,
+        os_system_manager=OperationSystemManager(os_type),
     ).install()
     driver_path = EdgeChromiumDriverManager(
         version=specific_version,
-        os_type=os_type
+        os_system_manager=OperationSystemManager(os_type)
     ).install()
     assert os.path.exists(driver_path)
 
 
 def test_get_stable_release_version():
     pattern = PATTERN[ChromeType.MSEDGE]
     edge_driver = EdgeChromiumDriverManager(
```

### Comparing `webdriver_manager-3.9.0/tests/test_firefox_manager.py` & `webdriver_manager-3.9.1/tests/test_firefox_manager.py`

 * *Files 24% similar despite different names*

```diff
@@ -1,35 +1,38 @@
 import os
 
 import pytest
 from selenium import webdriver
+from selenium.webdriver.firefox.service import Service
 
+from webdriver_manager.core.driver_cache import DriverCacheManager
+from webdriver_manager.core.os_manager import OperationSystemManager
 from webdriver_manager.firefox import GeckoDriverManager
 
 
 def test_firefox_manager_with_cache(delete_drivers_dir):
     GeckoDriverManager().install()
     binary = GeckoDriverManager().install()
     assert os.path.exists(binary)
 
 
 def test_gecko_manager_with_selenium():
     driver_path = GeckoDriverManager().install()
-    ff = webdriver.Firefox(executable_path=driver_path)
+    ff = webdriver.Firefox(service=Service(driver_path))
     ff.get("http://automation-remarks.com")
     ff.quit()
 
 
 def test_driver_with_ssl_verify_disabled_can_be_downloaded(ssl_verify_enable):
     os.environ['WDM_SSL_VERIFY'] = '0'
     custom_path = os.path.join(
         os.path.dirname(os.path.dirname(__file__)),
         "ssl_disabled",
     )
-    driver_path = GeckoDriverManager(path=custom_path).install()
+    driver_path = GeckoDriverManager(cache_manager=DriverCacheManager(custom_path)).install()
     os.environ['WDM_SSL_VERIFY'] = '1'
     assert os.path.exists(driver_path)
 
 
 def test_gecko_manager_with_wrong_version():
     with pytest.raises(ValueError) as ex:
         GeckoDriverManager("0.2").install()
@@ -41,21 +44,21 @@
 
 def test_gecko_manager_with_correct_version_and_token(delete_drivers_dir):
     driver_path = GeckoDriverManager(version="v0.11.0").install()
     assert os.path.exists(driver_path)
 
 
 def test_can_download_ff_x64(delete_drivers_dir):
-    driver_path = GeckoDriverManager(os_type="win64").install()
+    driver_path = GeckoDriverManager(os_system_manager=OperationSystemManager("win64")).install()
     assert os.path.exists(driver_path)
 
 
 @pytest.mark.parametrize('os_type', ['win32',
                                      'win64',
                                      'linux32',
                                      'linux64',
                                      'mac64',
                                      'mac64_m1'])
 def test_can_get_driver_from_cache(os_type):
-    GeckoDriverManager(os_type=os_type).install()
-    driver_path = GeckoDriverManager(os_type=os_type).install()
+    GeckoDriverManager(os_system_manager=OperationSystemManager(os_type)).install()
+    driver_path = GeckoDriverManager(os_system_manager=OperationSystemManager(os_type)).install()
     assert os.path.exists(driver_path)
```

### Comparing `webdriver_manager-3.9.0/tests/test_ie_driver.py` & `webdriver_manager-3.9.1/tests/test_ie_driver.py`

 * *Files 23% similar despite different names*

```diff
@@ -1,11 +1,13 @@
 import os
 
 import pytest
 
+from webdriver_manager.core.driver_cache import DriverCacheManager
+from webdriver_manager.core.os_manager import OperationSystemManager
 from webdriver_manager.microsoft import IEDriverManager
 
 
 @pytest.mark.parametrize("version", [
     "3.0",
     "3.150.0"
 ])
@@ -16,29 +18,29 @@
 
 def test_driver_with_ssl_verify_disabled_can_be_downloaded(ssl_verify_enable):
     os.environ['WDM_SSL_VERIFY'] = '0'
     custom_path = os.path.join(
         os.path.dirname(os.path.dirname(__file__)),
         "ssl_disabled",
     )
-    driver_path = IEDriverManager(path=custom_path).install()
+    driver_path = IEDriverManager(cache_manager=DriverCacheManager(custom_path)).install()
     os.environ['WDM_SSL_VERIFY'] = '1'
     assert os.path.exists(driver_path)
 
 
 @pytest.mark.parametrize('os_type', ['win32', 'win64'])
 def test_can_download_ie_driver_x64(os_type):
-    path = IEDriverManager(os_type=os_type).install()
+    path = IEDriverManager(os_system_manager=OperationSystemManager(os_type)).install()
     assert os.path.exists(path)
 
 
 @pytest.mark.parametrize('os_type', ['win32', 'win64'])
 def test_can_get_ie_driver_from_cache(os_type):
-    IEDriverManager(os_type=os_type).install()
-    driver_path = IEDriverManager(os_type=os_type).install()
+    IEDriverManager(os_system_manager=OperationSystemManager(os_type)).install()
+    driver_path = IEDriverManager(os_system_manager=OperationSystemManager(os_type)).install()
     assert os.path.exists(driver_path)
 
 
 @pytest.mark.parametrize('version', ['', '3', '3.4.5.6'])
 def test__get_divided_version_raises_exception(version):
     iedriver = IEDriverManager().driver
```

### Comparing `webdriver_manager-3.9.0/tests/test_utils.py` & `webdriver_manager-3.9.1/tests/test_utils.py`

 * *Files identical despite different names*

### Comparing `webdriver_manager-3.9.0/webdriver_manager/core/config.py` & `webdriver_manager-3.9.1/webdriver_manager/core/config.py`

 * *Files identical despite different names*

### Comparing `webdriver_manager-3.9.0/webdriver_manager/core/download_manager.py` & `webdriver_manager-3.9.1/webdriver_manager/core/download_manager.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 import os
 from abc import ABC
 
+from webdriver_manager.core.file_manager import File
 from webdriver_manager.core.http import WDMHttpClient
 from webdriver_manager.core.logger import log
-from webdriver_manager.core.utils import File
 
 
 class DownloadManager(ABC):
     def __init__(self, http_client):
         self._http_client = http_client
 
     def download_file(self, url: str) -> File:
```

### Comparing `webdriver_manager-3.9.0/webdriver_manager/core/driver.py` & `webdriver_manager-3.9.1/webdriver_manager/core/driver.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,58 +1,57 @@
-from webdriver_manager.core import utils
 from webdriver_manager.core.logger import log
 from webdriver_manager.core.config import gh_token
-from webdriver_manager.core.utils import get_browser_version_from_os
+from webdriver_manager.core.os_manager import OperationSystemManager
 
 
 class Driver(object):
     def __init__(
             self,
             name,
-            version,
-            os_type,
+            driver_version,
             url,
             latest_release_url,
-            http_client):
+            http_client,
+            os_system_manager):
         self._name = name
         self._url = url
-        self._version = version
-        self._os_type = os_type
-        if os_type is None:
-            self._os_type = utils.os_type()
+        self._driver_version = driver_version
         self._latest_release_url = latest_release_url
         self._http_client = http_client
         self._browser_version = None
         self._driver_to_download_version = None
+        self._os_system_manager = os_system_manager
+        if not self._os_system_manager:
+            self._os_system_manager = OperationSystemManager()
 
     @property
     def auth_header(self):
         token = gh_token()
         if token:
             log("GH_TOKEN will be used to perform requests")
             return {"Authorization": f"token {token}"}
         return None
 
     def get_name(self):
         return self._name
 
     def get_os_type(self):
-        return self._os_type
+        return self._os_system_manager.get_os_type()
 
     def get_driver_download_url(self):
-        return f"{self._url}/{self.get_driver_version_to_download()}/{self._name}_{self._os_type}.zip"
+        return f"{self._url}/{self.get_driver_version_to_download()}/{self._name}_{self.get_os_type()}.zip"
 
     def get_driver_version_to_download(self):
         """
         Downloads version from parameter if version not None or "latest".
         Downloads latest, if version is "latest" or browser could not been determined.
         Downloads determined browser version driver in all other ways as a bonus fallback for lazy users.
         """
         if not self._driver_to_download_version:
-            self._driver_to_download_version = self._version if self._version not in (None, "latest") \
+            self._driver_to_download_version = self._driver_version if self._driver_version not in (None, "latest") \
                 else self.get_latest_release_version()
         return self._driver_to_download_version
 
     def get_latest_release_version(self):
         # type: () -> str
         raise NotImplementedError("Please implement this method")
 
@@ -61,15 +60,15 @@
         Use-cases:
         - for key in metadata;
         - for printing nice logs;
         - for fallback if version was not set at all.
         Note: the fallback may have collisions in user cases when previous browser was not uninstalled properly.
         """
         if self._browser_version is None:
-            self._browser_version = get_browser_version_from_os(self.get_browser_type())
+            self._browser_version = self._os_system_manager.get_browser_version_from_os(self.get_browser_type())
         return self._browser_version
 
     def get_browser_type(self):
         raise NotImplementedError("Please implement this method")
 
     def get_binary_name(self):
         driver_name = self.get_name()
```

### Comparing `webdriver_manager-3.9.0/webdriver_manager/core/driver_cache.py` & `webdriver_manager-3.9.1/webdriver_manager/core/driver_cache.py`

 * *Files 24% similar despite different names*

```diff
@@ -4,45 +4,58 @@
 
 from webdriver_manager.core.config import wdm_local, get_xdist_worker_id
 from webdriver_manager.core.constants import (
     DEFAULT_PROJECT_ROOT_CACHE_PATH,
     DEFAULT_USER_HOME_CACHE_PATH, ROOT_FOLDER_NAME,
 )
 from webdriver_manager.core.driver import Driver
+from webdriver_manager.core.file_manager import FileManager, File
 from webdriver_manager.core.logger import log
-from webdriver_manager.core.utils import get_date_diff, File, save_file
+from webdriver_manager.core.os_manager import OperationSystemManager
+from webdriver_manager.core.utils import get_date_diff
 
 
-class DriverCache(object):
-    def __init__(self, root_dir=None, valid_range=1):
+class DriverCacheManager(object):
+    def __init__(self, root_dir=None, valid_range=1, file_manager=None):
         self._root_dir = DEFAULT_USER_HOME_CACHE_PATH
         is_wdm_local = wdm_local()
         xdist_worker_id = get_xdist_worker_id()
         if xdist_worker_id:
             log(f"xdist worker is: {xdist_worker_id}")
             self._root_dir = os.path.join(self._root_dir, xdist_worker_id)
 
-        if root_dir is not None:
+        if root_dir:
             self._root_dir = os.path.join(root_dir, ROOT_FOLDER_NAME, xdist_worker_id)
+
         if is_wdm_local:
             self._root_dir = os.path.join(DEFAULT_PROJECT_ROOT_CACHE_PATH, xdist_worker_id)
 
         self._drivers_root = "drivers"
         self._drivers_json_path = os.path.join(self._root_dir, "drivers.json")
         self._date_format = "%d/%m/%Y"
         self._drivers_directory = os.path.join(self._root_dir, self._drivers_root)
-        self.valid_range = valid_range
+        self._cache_valid_days_range = valid_range
         self._cache_key_driver_version = None
         self._metadata_key = None
         self._driver_binary_path = None
+        self._file_manager = file_manager
+        self._os_system_manager = OperationSystemManager()
+        if not self._file_manager:
+            self._file_manager = FileManager(self._os_system_manager)
+
+    def save_archive_file(self, file: File, path):
+        return self._file_manager.save_archive_file(file, path)
+
+    def unpack_archive(self, archive, path):
+        return self._file_manager.unpack_archive(archive, path)
 
     def save_file_to_cache(self, driver: Driver, file: File):
         path = self.__get_path(driver)
-        archive = save_file(file, path)
-        files = archive.unpack(path)
+        archive = self.save_archive_file(file, path)
+        files = self.unpack_archive(archive, path)
         binary = self.__get_binary(files, driver.get_name())
         binary_path = os.path.join(path, binary)
         self.__save_metadata(driver, binary_path)
         log(f"Driver has been saved in cache [{path}]")
         return binary_path
 
     def __get_binary(self, files, driver_name):
@@ -73,26 +86,30 @@
             }
         }
 
         metadata.update(data)
         with open(self._drivers_json_path, "w+") as outfile:
             json.dump(metadata, outfile, indent=4)
 
+    def get_os_type(self):
+        return self._os_system_manager.get_os_type()
+
     def find_driver(self, driver: Driver):
         """Find driver by '{os_type}_{driver_name}_{driver_version}_{browser_version}'."""
-        os_type = driver.get_os_type()
+        os_type = self.get_os_type()
         driver_name = driver.get_name()
-        browser_version = driver.get_browser_version_from_os()
-        driver_version = self.get_cache_key_driver_version(driver)
         browser_type = driver.get_browser_type()
+        browser_version = self._os_system_manager.get_browser_version_from_os(browser_type)
+        driver_version = self.get_cache_key_driver_version(driver)
         metadata = self.load_metadata_content()
 
         key = self.__get_metadata_key(driver)
         if key not in metadata:
-            log(f'There is no [{os_type}] {driver_name} "{driver_version}" for browser {browser_type} "{browser_version}" in cache')
+            log(f'There is no [{os_type}] {driver_name} "{driver_version}" for browser {browser_type} '
+                f'"{browser_version}" in cache')
             return None
 
         driver_info = metadata[key]
         path = driver_info["binary_path"]
         if not os.path.exists(path):
             return None
 
@@ -103,15 +120,15 @@
         log(f"Driver [{path}] found in cache")
         return path
 
     def __is_valid(self, driver_info):
         dates_diff = get_date_diff(
             driver_info["timestamp"], datetime.date.today(), self._date_format
         )
-        return dates_diff < self.valid_range
+        return dates_diff < self._cache_valid_days_range
 
     def load_metadata_content(self):
         if os.path.exists(self._drivers_json_path):
             with open(self._drivers_json_path, "r") as outfile:
                 return json.load(outfile)
         return {}
 
@@ -121,15 +138,16 @@
             browser_version = driver.get_browser_version_from_os()
             browser_version = browser_version if browser_version else ""
             self._metadata_key = f"{driver.get_os_type()}_{driver.get_name()}_{driver_version}_for_{browser_version}"
         return self._metadata_key
 
     def get_cache_key_driver_version(self, driver: Driver):
         if self._cache_key_driver_version is None:
-            self._cache_key_driver_version = "latest" if driver._version in (None, "latest") else driver._version
+            self._cache_key_driver_version = "latest" if driver._driver_version in (
+            None, "latest") else driver._driver_version
         return self._cache_key_driver_version
 
     def __get_path(self, driver: Driver):
         if self._driver_binary_path is None:
             self._driver_binary_path = os.path.join(
                 self._drivers_directory,
                 driver.get_name(),
```

### Comparing `webdriver_manager-3.9.0/webdriver_manager/core/http.py` & `webdriver_manager-3.9.1/webdriver_manager/core/http.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,12 +1,11 @@
 import requests
 from requests import Response, exceptions
 
-from webdriver_manager.core.config import ssl_verify, wdm_progress_bar
-from webdriver_manager.core.utils import show_download_progress
+from webdriver_manager.core.config import ssl_verify
 
 
 class HttpClient:
     def get(self, url, params=None, **kwargs) -> Response:
         raise NotImplementedError
 
     @staticmethod
```

### Comparing `webdriver_manager-3.9.0/webdriver_manager/core/logger.py` & `webdriver_manager-3.9.1/webdriver_manager/core/logger.py`

 * *Files identical despite different names*

### Comparing `webdriver_manager-3.9.0/webdriver_manager/core/manager.py` & `webdriver_manager-3.9.1/webdriver_manager/core/manager.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,32 +1,35 @@
 from webdriver_manager.core.download_manager import WDMDownloadManager
-from webdriver_manager.core.driver_cache import DriverCache
+from webdriver_manager.core.driver_cache import DriverCacheManager
 from webdriver_manager.core.logger import log
 
 
 class DriverManager(object):
     def __init__(
             self,
-            root_dir=None,
-            cache_valid_range=1,
-            download_manager=None):
-        self.driver_cache = DriverCache(root_dir, cache_valid_range)
+            download_manager=None,
+            cache_manager=None
+    ):
+        self._cache_manager = cache_manager
+        if not self._cache_manager:
+            self._cache_manager = DriverCacheManager()
+
         self._download_manager = download_manager
-        if download_manager is None:
+        if self._download_manager is None:
             self._download_manager = WDMDownloadManager()
         log("====== WebDriver manager ======")
 
     @property
     def http_client(self):
         return self._download_manager.http_client
 
     def install(self) -> str:
         raise NotImplementedError("Please Implement this method")
 
-    def _get_driver_path(self, driver):
-        binary_path = self.driver_cache.find_driver(driver)
+    def _get_driver_binary_path(self, driver):
+        binary_path = self._cache_manager.find_driver(driver)
         if binary_path:
             return binary_path
 
         file = self._download_manager.download_file(driver.get_driver_download_url())
-        binary_path = self.driver_cache.save_file_to_cache(driver, file)
+        binary_path = self._cache_manager.save_file_to_cache(driver, file)
         return binary_path
```

### Comparing `webdriver_manager-3.9.0/webdriver_manager/drivers/chrome.py` & `webdriver_manager-3.9.1/webdriver_manager/drivers/chrome.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,55 +1,60 @@
 from packaging import version
 
 from webdriver_manager.core.driver import Driver
 from webdriver_manager.core.logger import log
-from webdriver_manager.core.utils import ChromeType, is_arch, is_mac_os
+from webdriver_manager.core.os_manager import OperationSystemManager, ChromeType
 
 
 class ChromeDriver(Driver):
 
     def __init__(
             self,
             name,
-            version,
-            os_type,
+            driver_version,
             url,
             latest_release_url,
             http_client,
-            chrome_type=ChromeType.GOOGLE,
+            os_system_manager,
+            chrome_type=ChromeType.GOOGLE
     ):
         super(ChromeDriver, self).__init__(
-            name, version, os_type, url, latest_release_url, http_client
+            name,
+            driver_version,
+            url,
+            latest_release_url,
+            http_client,
+            os_system_manager
         )
         self._browser_type = chrome_type
         self._os_type = self.get_os_type()
 
     def get_os_type(self):
         os_type = super().get_os_type()
         if "win" in os_type:
             return "win32"
 
-        if not is_mac_os(os_type):
+        if not OperationSystemManager.is_mac_os(os_type):
             return os_type
 
-        if is_arch(os_type):
+        if OperationSystemManager.is_arch(os_type):
             return "mac_arm64"
 
         return os_type
 
     def get_driver_download_url(self):
         driver_version_to_download = self.get_driver_version_to_download()
         os_type = self._os_type
         # For Mac ARM CPUs after version 106.0.5249.61 the format of OS type changed
         # to more unified "mac_arm64". For newer versions, it'll be "mac_arm64"
         # by default, for lower versions we replace "mac_arm64" to old format - "mac64_m1".
         if version.parse(driver_version_to_download) < version.parse("106.0.5249.61"):
             os_type = os_type.replace("mac_arm64", "mac64_m1")
 
-        if version.parse(driver_version_to_download) >= version.parse("113"):
+        if version.parse(driver_version_to_download) >= version.parse("115"):
             if os_type == "mac64":
                 os_type = "mac-x64"
             if os_type in ["mac_64", "mac64_m1", "mac_arm64"]:
                 os_type = "mac-arm64"
 
             modern_version_url = self.get_url_for_version_and_platform(driver_version_to_download, os_type)
             log(f"Modern chrome version {modern_version_url}")
@@ -64,15 +69,15 @@
         determined_browser_version = self.get_browser_version_from_os()
         log(f"Get LATEST {self._name} version for {self._browser_type}")
         if version.parse(determined_browser_version) >= version.parse("113"):
             return determined_browser_version
 
         latest_release_url = (
             self._latest_release_url
-            if (self._version == "latest" or determined_browser_version is None)
+            if (self._driver_version == "latest" or determined_browser_version is None)
             else f"{self._latest_release_url}_{determined_browser_version}"
         )
         resp = self._http_client.get(url=latest_release_url)
         return resp.text.rstrip()
 
     def get_url_for_version_and_platform(self, browser_version, platform):
         url = "https://googlechromelabs.github.io/chrome-for-testing/known-good-versions-with-downloads.json"
```

### Comparing `webdriver_manager-3.9.0/webdriver_manager/drivers/edge.py` & `webdriver_manager-3.9.1/webdriver_manager/drivers/edge.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,30 +1,30 @@
 from webdriver_manager.core.driver import Driver
 from webdriver_manager.core.logger import log
-from webdriver_manager.core.utils import OSType, ChromeType
+from webdriver_manager.core.os_manager import OSType, ChromeType
 
 
 class EdgeChromiumDriver(Driver):
 
     def __init__(
             self,
             name,
-            version,
-            os_type,
+            driver_version,
             url,
             latest_release_url,
-            http_client
+            http_client,
+            os_system_manager
     ):
         super(EdgeChromiumDriver, self).__init__(
             name,
-            version,
-            os_type,
+            driver_version,
             url,
             latest_release_url,
-            http_client
+            http_client,
+            os_system_manager
         )
         self._os_type = self.get_os_type()
 
     def get_stable_release_version(self):
         """Stable driver version when browser version was not determined."""
         stable_url = self._latest_release_url.replace("LATEST_RELEASE", "LATEST_STABLE")
         resp = self._http_client.get(url=stable_url)
@@ -32,15 +32,15 @@
 
     def get_latest_release_version(self) -> str:
         determined_browser_version = self.get_browser_version_from_os()
         log(f"Get LATEST {self._name} version for Edge {determined_browser_version}")
 
         edge_driver_version_to_download = (
             self.get_stable_release_version()
-            if (self._version == "latest" or determined_browser_version is None)
+            if (self._driver_version == "latest" or determined_browser_version is None)
             else determined_browser_version
         )
         major_edge_version = edge_driver_version_to_download.split(".")[0]
         latest_release_url = {
             OSType.WIN
             in self._os_type: f"{self._latest_release_url}_{major_edge_version}_WINDOWS",
             OSType.MAC
```

### Comparing `webdriver_manager-3.9.0/webdriver_manager/drivers/ie.py` & `webdriver_manager-3.9.1/webdriver_manager/drivers/ie.py`

 * *Files 6% similar despite different names*

```diff
@@ -3,30 +3,30 @@
 
 
 class IEDriver(Driver):
 
     def __init__(
             self,
             name,
-            version,
-            os_type,
+            driver_version,
             url,
             latest_release_url,
             ie_release_tag,
-            http_client
+            http_client,
+            os_system_manager
     ):
         super(IEDriver, self).__init__(
             name,
-            version,
-            os_type,
+            driver_version,
             url,
             latest_release_url,
-            http_client
+            http_client,
+            os_system_manager
         )
-        self.os_type = "x64" if os_type == "win64" else "Win32"
+        self.os_type = "x64" if self._os_system_manager.get_os_type() == "win64" else "Win32"
         self._ie_release_tag = ie_release_tag
         # todo: for 'browser_version' implement installed IE version detection
         #       like chrome or firefox
 
     def get_latest_release_version(self) -> str:
         log(f"Get LATEST driver version for Internet Explorer")
         resp = self._http_client.get(
```

### Comparing `webdriver_manager-3.9.0/webdriver_manager/drivers/opera.py` & `webdriver_manager-3.9.1/webdriver_manager/drivers/opera.py`

 * *Files 11% similar despite different names*

```diff
@@ -2,22 +2,28 @@
 from webdriver_manager.core.logger import log
 
 
 class OperaDriver(Driver):
     def __init__(
             self,
             name,
-            version,
-            os_type,
+            driver_version,
             url,
             latest_release_url,
             opera_release_tag,
-            http_client):
+            http_client,
+            os_system_manager
+    ):
         super(OperaDriver, self).__init__(
-            name, version, os_type, url, latest_release_url, http_client
+            name,
+            driver_version,
+            url,
+            latest_release_url,
+            http_client,
+            os_system_manager
         )
         self.opera_release_tag = opera_release_tag
 
     def get_latest_release_version(self) -> str:
         resp = self._http_client.get(
             url=self.latest_release_url,
             headers=self.auth_header
```

### Comparing `webdriver_manager-3.9.0/webdriver_manager/firefox.py` & `webdriver_manager-3.9.1/webdriver_manager/firefox.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,39 +1,41 @@
 import os
 from typing import Optional
 
 from webdriver_manager.core.download_manager import DownloadManager
+from webdriver_manager.core.driver_cache import DriverCacheManager
 from webdriver_manager.core.manager import DriverManager
+from webdriver_manager.core.os_manager import OperationSystemManager
 from webdriver_manager.drivers.firefox import GeckoDriver
 
 
 class GeckoDriverManager(DriverManager):
     def __init__(
-        self,
-        version: Optional[str] = None,
-        os_type: Optional[str] = None,
-        path: Optional[str] = None,
-        name: str = "geckodriver",
-        url: str = "https://github.com/mozilla/geckodriver/releases/download",
-        latest_release_url: str = "https://api.github.com/repos/mozilla/geckodriver/releases/latest",
-        mozila_release_tag: str = "https://api.github.com/repos/mozilla/geckodriver/releases/tags/{0}",
-        cache_valid_range: int = 1,
-        download_manager: Optional[DownloadManager] = None,
+            self,
+            version: Optional[str] = None,
+            name: str = "geckodriver",
+            url: str = "https://github.com/mozilla/geckodriver/releases/download",
+            latest_release_url: str = "https://api.github.com/repos/mozilla/geckodriver/releases/latest",
+            mozila_release_tag: str = "https://api.github.com/repos/mozilla/geckodriver/releases/tags/{0}",
+            download_manager: Optional[DownloadManager] = None,
+            cache_manager: Optional[DriverCacheManager] = None,
+            os_system_manager: Optional[OperationSystemManager] = None
     ):
         super(GeckoDriverManager, self).__init__(
-            path, cache_valid_range, download_manager=download_manager
+            download_manager=download_manager,
+            cache_manager=cache_manager
         )
 
         self.driver = GeckoDriver(
-            version=version,
-            os_type=os_type,
+            driver_version=version,
             name=name,
             url=url,
             latest_release_url=latest_release_url,
             mozila_release_tag=mozila_release_tag,
             http_client=self.http_client,
+            os_system_manager=os_system_manager
         )
 
     def install(self) -> str:
-        driver_path = self._get_driver_path(self.driver)
+        driver_path = self._get_driver_binary_path(self.driver)
         os.chmod(driver_path, 0o755)
         return driver_path
```

### Comparing `webdriver_manager-3.9.0/webdriver_manager/microsoft.py` & `webdriver_manager-3.9.1/webdriver_manager/microsoft.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,64 +1,71 @@
 import os
 from typing import Optional
 
-from webdriver_manager.core import utils
 from webdriver_manager.core.download_manager import DownloadManager
+from webdriver_manager.core.driver_cache import DriverCacheManager
+from webdriver_manager.core.os_manager import OperationSystemManager
 from webdriver_manager.drivers.edge import EdgeChromiumDriver
 from webdriver_manager.drivers.ie import IEDriver
 from webdriver_manager.core.manager import DriverManager
 
 
 class IEDriverManager(DriverManager):
     def __init__(
-        self,
-        version: Optional[str] = None,
-        os_type: Optional[str] = None,
-        path: Optional[str] = None,
-        name: str = "IEDriverServer",
-        url: str = "https://github.com/seleniumhq/selenium/releases/download",
-        latest_release_url: str = "https://api.github.com/repos/seleniumhq/selenium/releases",
-        ie_release_tag: str = "https://api.github.com/repos/seleniumhq/selenium/releases/tags/selenium-{0}",
-        cache_valid_range: int = 1,
-        download_manager: Optional[DownloadManager] = None,
+            self,
+            version: Optional[str] = None,
+            name: str = "IEDriverServer",
+            url: str = "https://github.com/seleniumhq/selenium/releases/download",
+            latest_release_url: str = "https://api.github.com/repos/seleniumhq/selenium/releases",
+            ie_release_tag: str = "https://api.github.com/repos/seleniumhq/selenium/releases/tags/selenium-{0}",
+            download_manager: Optional[DownloadManager] = None,
+            cache_manager: Optional[DriverCacheManager] = None,
+            os_system_manager: Optional[OperationSystemManager] = None
     ):
-        super().__init__(path, cache_valid_range, download_manager=download_manager)
+        super().__init__(
+            download_manager=download_manager,
+            cache_manager=cache_manager
+        )
+
         self.driver = IEDriver(
-            version=version,
-            os_type=os_type,
+            driver_version=version,
             name=name,
             url=url,
             latest_release_url=latest_release_url,
             ie_release_tag=ie_release_tag,
             http_client=self.http_client,
+            os_system_manager=os_system_manager
         )
 
     def install(self) -> str:
-        return self._get_driver_path(self.driver)
+        return self._get_driver_binary_path(self.driver)
 
 
 class EdgeChromiumDriverManager(DriverManager):
     def __init__(
-        self,
-        version: Optional[str] = None,
-        os_type: str = utils.os_type(),
-        path: Optional[str] = None,
-        name: str = "edgedriver",
-        url: str = "https://msedgedriver.azureedge.net",
-        latest_release_url: str = "https://msedgedriver.azureedge.net/LATEST_RELEASE",
-        cache_valid_range: int = 1,
-        download_manager: Optional[DownloadManager] = None,
+            self,
+            version: Optional[str] = None,
+            name: str = "edgedriver",
+            url: str = "https://msedgedriver.azureedge.net",
+            latest_release_url: str = "https://msedgedriver.azureedge.net/LATEST_RELEASE",
+            download_manager: Optional[DownloadManager] = None,
+            cache_manager: Optional[DriverCacheManager] = None,
+            os_system_manager: Optional[OperationSystemManager] = None
     ):
-        super().__init__(path, cache_valid_range, download_manager=download_manager)
+        super().__init__(
+            download_manager=download_manager,
+            cache_manager=cache_manager
+        )
+
         self.driver = EdgeChromiumDriver(
-            version=version,
-            os_type=os_type,
+            driver_version=version,
             name=name,
             url=url,
             latest_release_url=latest_release_url,
             http_client=self.http_client,
+            os_system_manager=os_system_manager
         )
 
     def install(self) -> str:
-        driver_path = self._get_driver_path(self.driver)
+        driver_path = self._get_driver_binary_path(self.driver)
         os.chmod(driver_path, 0o755)
         return driver_path
```

### Comparing `webdriver_manager-3.9.0/webdriver_manager.egg-info/PKG-INFO` & `webdriver_manager-3.9.1/webdriver_manager.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: webdriver-manager
-Version: 3.9.0
+Version: 3.9.1
 Summary: Library provides the way to automatically manage drivers for different browsers
 Home-page: https://github.com/SergeyPirogov/webdriver_manager
 Author: Sergey Pirogov
 Author-email: automationremarks@gmail.com
 Keywords: testing,selenium,driver,test automation
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Intended Audience :: Information Technology
@@ -221,14 +221,21 @@
 
 ```python
 from webdriver_manager.core.utils import read_version_from_cmd, PATTERN
 version = read_version_from_cmd("/usr/bin/firefox-bin --version", PATTERN["firefox"])
 driver_binary = FirefoxDriverManager(version=version).install()
 ```
 
+#### Custom Cache and File manager
+
+```python
+cache_manager = DriverCacheManager(file_manager=FileManager())
+manager = ChromeDriverManager(cache_manager=cache_manager)
+```
+
 ## Configuration
 
 **webdriver_manager** has several configuration variables you can be interested in.
 Any variable can be set using either .env file or via python directly
 
 ### `GH_TOKEN`
 **webdriver_manager** downloading some webdrivers from their official GitHub repositories but GitHub has [limitations](https://docs.github.com/en/rest/overview/resources-in-the-rest-api#rate-limiting) like 60 requests per hour for unauthenticated users.
@@ -256,23 +263,14 @@
 ```python
 import logging
 import os
 
 os.environ['WDM_LOG'] = str(logging.NOTSET)
 ```
 
-### `WDM_PROGRESS_BAR`
-Turn off the progress bar which is displayed on downloads:
-
-```python
-import os
-
-os.environ['WDM_PROGRESS_BAR'] = str(0)
-```
-
 ### `WDM_LOCAL`
 By default, all driver binaries are saved to user.home/.wdm folder. You can override this setting and save binaries to project.root/.wdm.
 
 ```python
 import os
 
 os.environ['WDM_LOCAL'] = '1'
```

### Comparing `webdriver_manager-3.9.0/webdriver_manager.egg-info/SOURCES.txt` & `webdriver_manager-3.9.1/webdriver_manager.egg-info/SOURCES.txt`

 * *Files 1% similar despite different names*

```diff
@@ -28,17 +28,19 @@
 webdriver_manager/core/__init__.py
 webdriver_manager/core/archive.py
 webdriver_manager/core/config.py
 webdriver_manager/core/constants.py
 webdriver_manager/core/download_manager.py
 webdriver_manager/core/driver.py
 webdriver_manager/core/driver_cache.py
+webdriver_manager/core/file_manager.py
 webdriver_manager/core/http.py
 webdriver_manager/core/logger.py
 webdriver_manager/core/manager.py
+webdriver_manager/core/os_manager.py
 webdriver_manager/core/utils.py
 webdriver_manager/drivers/__init__.py
 webdriver_manager/drivers/chrome.py
 webdriver_manager/drivers/edge.py
 webdriver_manager/drivers/firefox.py
 webdriver_manager/drivers/ie.py
 webdriver_manager/drivers/opera.py
```

