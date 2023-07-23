# Comparing `tmp/chromedriver_auto-1.0.1.tar.gz` & `tmp/chromedriver_auto-1.0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "chromedriver_auto-1.0.1.tar", last modified: Sun Jul 23 17:50:25 2023, max compression
+gzip compressed data, was "chromedriver_auto-1.0.4.tar", last modified: Sun Jul 23 19:03:21 2023, max compression
```

## Comparing `chromedriver_auto-1.0.1.tar` & `chromedriver_auto-1.0.4.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 17:50:25.492159 chromedriver_auto-1.0.1/
--rw-r--r--   0 sorowerhossan   (501) staff       (20)     1074 2023-07-23 17:17:05.000000 chromedriver_auto-1.0.1/LICENSE
--rw-r--r--   0 sorowerhossan   (501) staff       (20)      791 2023-07-23 17:50:25.492223 chromedriver_auto-1.0.1/PKG-INFO
--rw-r--r--   0 sorowerhossan   (501) staff       (20)      155 2023-07-23 17:34:22.000000 chromedriver_auto-1.0.1/README.md
--rw-r--r--   0 sorowerhossan   (501) staff       (20)      103 2023-07-23 17:08:21.000000 chromedriver_auto-1.0.1/pyproject.toml
--rw-r--r--   0 sorowerhossan   (501) staff       (20)      761 2023-07-23 17:50:25.492443 chromedriver_auto-1.0.1/setup.cfg
-drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 17:50:25.490504 chromedriver_auto-1.0.1/src/
-drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 17:50:25.491416 chromedriver_auto-1.0.1/src/chromedriver_auto/
--rw-r--r--   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 17:06:12.000000 chromedriver_auto-1.0.1/src/chromedriver_auto/__init__.py
--rw-r--r--   0 sorowerhossan   (501) staff       (20)     4669 2023-07-23 17:49:54.000000 chromedriver_auto-1.0.1/src/chromedriver_auto/driver_ready.py
-drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 17:50:25.492051 chromedriver_auto-1.0.1/src/chromedriver_auto.egg-info/
--rw-r--r--   0 sorowerhossan   (501) staff       (20)      791 2023-07-23 17:50:25.000000 chromedriver_auto-1.0.1/src/chromedriver_auto.egg-info/PKG-INFO
--rw-r--r--   0 sorowerhossan   (501) staff       (20)      294 2023-07-23 17:50:25.000000 chromedriver_auto-1.0.1/src/chromedriver_auto.egg-info/SOURCES.txt
--rw-r--r--   0 sorowerhossan   (501) staff       (20)        1 2023-07-23 17:50:25.000000 chromedriver_auto-1.0.1/src/chromedriver_auto.egg-info/dependency_links.txt
--rw-r--r--   0 sorowerhossan   (501) staff       (20)       18 2023-07-23 17:50:25.000000 chromedriver_auto-1.0.1/src/chromedriver_auto.egg-info/top_level.txt
+drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 19:03:21.382007 chromedriver_auto-1.0.4/
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)     1074 2023-07-23 17:17:05.000000 chromedriver_auto-1.0.4/LICENSE
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)      791 2023-07-23 19:03:21.382073 chromedriver_auto-1.0.4/PKG-INFO
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)      155 2023-07-23 17:34:22.000000 chromedriver_auto-1.0.4/README.md
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)      135 2023-07-23 18:57:54.000000 chromedriver_auto-1.0.4/pyproject.toml
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)      761 2023-07-23 19:03:21.382341 chromedriver_auto-1.0.4/setup.cfg
+drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 19:03:21.380093 chromedriver_auto-1.0.4/src/
+drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 19:03:21.381151 chromedriver_auto-1.0.4/src/chromedriver_auto/
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 17:06:12.000000 chromedriver_auto-1.0.4/src/chromedriver_auto/__init__.py
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)     4710 2023-07-23 17:58:25.000000 chromedriver_auto-1.0.4/src/chromedriver_auto/driver_ready.py
+drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 19:03:21.381881 chromedriver_auto-1.0.4/src/chromedriver_auto.egg-info/
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)      791 2023-07-23 19:03:21.000000 chromedriver_auto-1.0.4/src/chromedriver_auto.egg-info/PKG-INFO
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)      294 2023-07-23 19:03:21.000000 chromedriver_auto-1.0.4/src/chromedriver_auto.egg-info/SOURCES.txt
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)        1 2023-07-23 19:03:21.000000 chromedriver_auto-1.0.4/src/chromedriver_auto.egg-info/dependency_links.txt
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)       18 2023-07-23 19:03:21.000000 chromedriver_auto-1.0.4/src/chromedriver_auto.egg-info/top_level.txt
```

### Comparing `chromedriver_auto-1.0.1/LICENSE` & `chromedriver_auto-1.0.4/LICENSE`

 * *Files identical despite different names*

### Comparing `chromedriver_auto-1.0.1/PKG-INFO` & `chromedriver_auto-1.0.4/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: chromedriver_auto
-Version: 1.0.1
+Version: 1.0.4
 Summary: This package downloads and helps you use chromedriver without needing to keep chromedriver updated regularly. Works for version no: 115.XX.XX.X and upwords.
 Home-page: https://github.com/pypa/sampleproject
 Author: Sorower Hossan
 Author-email: sorower37@gmail.com
 Project-URL: Bug Tracker, https://github.com/pypa/sampleproject/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `chromedriver_auto-1.0.1/setup.cfg` & `chromedriver_auto-1.0.4/setup.cfg`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = chromedriver_auto
-version = 1.0.1
+version = 1.0.4
 author = Sorower Hossan
 author_email = sorower37@gmail.com
 description = This package downloads and helps you use chromedriver without needing to keep chromedriver updated regularly. Works for version no: 115.XX.XX.X and upwords.
 long_description = file: README.md
 long_description_content_type = text/markdown
 url = https://github.com/pypa/sampleproject
 project_urls =
```

### Comparing `chromedriver_auto-1.0.1/src/chromedriver_auto/driver_ready.py` & `chromedriver_auto-1.0.4/src/chromedriver_auto/driver_ready.py`

 * *Files 2% similar despite different names*

```diff
@@ -104,8 +104,9 @@
             except:
                 pass
 
 
             file_path= str(os.getcwd()) + '/chrome/chromedriver-mac-arm64'
         service = Service(executable_path=file_path)
         driver = webdriver.Chrome(service=service)
+        driver.get('https://google.com')
         return driver
```

### Comparing `chromedriver_auto-1.0.1/src/chromedriver_auto.egg-info/PKG-INFO` & `chromedriver_auto-1.0.4/src/chromedriver_auto.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: chromedriver-auto
-Version: 1.0.1
+Version: 1.0.4
 Summary: This package downloads and helps you use chromedriver without needing to keep chromedriver updated regularly. Works for version no: 115.XX.XX.X and upwords.
 Home-page: https://github.com/pypa/sampleproject
 Author: Sorower Hossan
 Author-email: sorower37@gmail.com
 Project-URL: Bug Tracker, https://github.com/pypa/sampleproject/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

