# Comparing `tmp/chromedriver_auto-1.0.5.tar.gz` & `tmp/chromedriver_auto-1.0.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "chromedriver_auto-1.0.5.tar", last modified: Sun Jul 23 19:10:01 2023, max compression
+gzip compressed data, was "chromedriver_auto-1.0.7.tar", last modified: Sun Jul 23 19:23:31 2023, max compression
```

## Comparing `chromedriver_auto-1.0.5.tar` & `chromedriver_auto-1.0.7.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 19:10:01.200703 chromedriver_auto-1.0.5/
--rw-r--r--   0 sorowerhossan   (501) staff       (20)     1074 2023-07-23 17:17:05.000000 chromedriver_auto-1.0.5/LICENSE
--rw-r--r--   0 sorowerhossan   (501) staff       (20)      791 2023-07-23 19:10:01.200758 chromedriver_auto-1.0.5/PKG-INFO
--rw-r--r--   0 sorowerhossan   (501) staff       (20)      155 2023-07-23 17:34:22.000000 chromedriver_auto-1.0.5/README.md
--rw-r--r--   0 sorowerhossan   (501) staff       (20)      200 2023-07-23 19:09:39.000000 chromedriver_auto-1.0.5/pyproject.toml
--rw-r--r--   0 sorowerhossan   (501) staff       (20)      761 2023-07-23 19:10:01.200993 chromedriver_auto-1.0.5/setup.cfg
-drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 19:10:01.198738 chromedriver_auto-1.0.5/src/
-drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 19:10:01.199836 chromedriver_auto-1.0.5/src/chromedriver_auto/
--rw-r--r--   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 17:06:12.000000 chromedriver_auto-1.0.5/src/chromedriver_auto/__init__.py
--rw-r--r--   0 sorowerhossan   (501) staff       (20)     4710 2023-07-23 17:58:25.000000 chromedriver_auto-1.0.5/src/chromedriver_auto/driver_ready.py
-drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 19:10:01.200585 chromedriver_auto-1.0.5/src/chromedriver_auto.egg-info/
--rw-r--r--   0 sorowerhossan   (501) staff       (20)      791 2023-07-23 19:10:01.000000 chromedriver_auto-1.0.5/src/chromedriver_auto.egg-info/PKG-INFO
--rw-r--r--   0 sorowerhossan   (501) staff       (20)      294 2023-07-23 19:10:01.000000 chromedriver_auto-1.0.5/src/chromedriver_auto.egg-info/SOURCES.txt
--rw-r--r--   0 sorowerhossan   (501) staff       (20)        1 2023-07-23 19:10:01.000000 chromedriver_auto-1.0.5/src/chromedriver_auto.egg-info/dependency_links.txt
--rw-r--r--   0 sorowerhossan   (501) staff       (20)       18 2023-07-23 19:10:01.000000 chromedriver_auto-1.0.5/src/chromedriver_auto.egg-info/top_level.txt
+drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 19:23:31.957149 chromedriver_auto-1.0.7/
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)     1074 2023-07-23 17:17:05.000000 chromedriver_auto-1.0.7/LICENSE
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)      791 2023-07-23 19:23:31.957200 chromedriver_auto-1.0.7/PKG-INFO
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)      155 2023-07-23 17:34:22.000000 chromedriver_auto-1.0.7/README.md
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)      339 2023-07-23 19:18:53.000000 chromedriver_auto-1.0.7/pyproject.toml
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)      761 2023-07-23 19:23:31.957418 chromedriver_auto-1.0.7/setup.cfg
+drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 19:23:31.955580 chromedriver_auto-1.0.7/src/
+drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 19:23:31.956456 chromedriver_auto-1.0.7/src/chromedriver_auto/
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 17:06:12.000000 chromedriver_auto-1.0.7/src/chromedriver_auto/__init__.py
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)     4786 2023-07-23 19:14:56.000000 chromedriver_auto-1.0.7/src/chromedriver_auto/driver_ready.py
+drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 19:23:31.957018 chromedriver_auto-1.0.7/src/chromedriver_auto.egg-info/
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)      791 2023-07-23 19:23:31.000000 chromedriver_auto-1.0.7/src/chromedriver_auto.egg-info/PKG-INFO
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)      294 2023-07-23 19:23:31.000000 chromedriver_auto-1.0.7/src/chromedriver_auto.egg-info/SOURCES.txt
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)        1 2023-07-23 19:23:31.000000 chromedriver_auto-1.0.7/src/chromedriver_auto.egg-info/dependency_links.txt
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)       18 2023-07-23 19:23:31.000000 chromedriver_auto-1.0.7/src/chromedriver_auto.egg-info/top_level.txt
```

### Comparing `chromedriver_auto-1.0.5/LICENSE` & `chromedriver_auto-1.0.7/LICENSE`

 * *Files identical despite different names*

### Comparing `chromedriver_auto-1.0.5/PKG-INFO` & `chromedriver_auto-1.0.7/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: chromedriver_auto
-Version: 1.0.5
+Version: 1.0.7
 Summary: This package downloads and helps you use chromedriver without needing to keep chromedriver updated regularly. Works for version no: 115.XX.XX.X and upwords.
 Home-page: https://github.com/pypa/sampleproject
 Author: Sorower Hossan
 Author-email: sorower37@gmail.com
 Project-URL: Bug Tracker, https://github.com/pypa/sampleproject/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `chromedriver_auto-1.0.5/setup.cfg` & `chromedriver_auto-1.0.7/setup.cfg`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = chromedriver_auto
-version = 1.0.5
+version = 1.0.7
 author = Sorower Hossan
 author_email = sorower37@gmail.com
 description = This package downloads and helps you use chromedriver without needing to keep chromedriver updated regularly. Works for version no: 115.XX.XX.X and upwords.
 long_description = file: README.md
 long_description_content_type = text/markdown
 url = https://github.com/pypa/sampleproject
 project_urls =
```

### Comparing `chromedriver_auto-1.0.5/src/chromedriver_auto/driver_ready.py` & `chromedriver_auto-1.0.7/src/chromedriver_auto/driver_ready.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,16 +1,18 @@
 def chrome_driver():
-    import os
-    import platform
-    import subprocess
-    import zipfile
-    from selenium import webdriver
-    import requests
-    from selenium.webdriver.chrome.service import Service
-
+    try:
+        import os
+        import platform
+        import subprocess
+        import zipfile
+        from selenium import webdriver
+        import requests
+        from selenium.webdriver.chrome.service import Service
+    except:
+        print('errros')
 
     def get_operating_system():
         return platform.system()
 
     # Example usage:
     os_name = get_operating_system()
     if os_name == "Windows":
@@ -104,9 +106,9 @@
             except:
                 pass
 
 
             file_path= str(os.getcwd()) + '/chrome/chromedriver-mac-arm64'
         service = Service(executable_path=file_path)
         driver = webdriver.Chrome(service=service)
-        driver.get('https://google.com')
+        driver.get('https://www.google.com')
         return driver
```

### Comparing `chromedriver_auto-1.0.5/src/chromedriver_auto.egg-info/PKG-INFO` & `chromedriver_auto-1.0.7/src/chromedriver_auto.egg-info/PKG-INFO`

 * *Files 15% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: chromedriver-auto
-Version: 1.0.5
+Version: 1.0.7
 Summary: This package downloads and helps you use chromedriver without needing to keep chromedriver updated regularly. Works for version no: 115.XX.XX.X and upwords.
 Home-page: https://github.com/pypa/sampleproject
 Author: Sorower Hossan
 Author-email: sorower37@gmail.com
 Project-URL: Bug Tracker, https://github.com/pypa/sampleproject/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

