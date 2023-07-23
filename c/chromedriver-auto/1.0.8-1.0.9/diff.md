# Comparing `tmp/chromedriver_auto-1.0.8.tar.gz` & `tmp/chromedriver_auto-1.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "chromedriver_auto-1.0.8.tar", last modified: Sun Jul 23 19:27:57 2023, max compression
+gzip compressed data, was "chromedriver_auto-1.0.9.tar", last modified: Sun Jul 23 19:39:50 2023, max compression
```

## Comparing `chromedriver_auto-1.0.8.tar` & `chromedriver_auto-1.0.9.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 19:27:57.035571 chromedriver_auto-1.0.8/
--rw-r--r--   0 sorowerhossan   (501) staff       (20)     1074 2023-07-23 17:17:05.000000 chromedriver_auto-1.0.8/LICENSE
--rw-r--r--   0 sorowerhossan   (501) staff       (20)      791 2023-07-23 19:27:57.035622 chromedriver_auto-1.0.8/PKG-INFO
--rw-r--r--   0 sorowerhossan   (501) staff       (20)      155 2023-07-23 17:34:22.000000 chromedriver_auto-1.0.8/README.md
--rw-r--r--   0 sorowerhossan   (501) staff       (20)      339 2023-07-23 19:18:53.000000 chromedriver_auto-1.0.8/pyproject.toml
--rw-r--r--   0 sorowerhossan   (501) staff       (20)      761 2023-07-23 19:27:57.035842 chromedriver_auto-1.0.8/setup.cfg
-drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 19:27:57.033757 chromedriver_auto-1.0.8/src/
-drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 19:27:57.034815 chromedriver_auto-1.0.8/src/chromedriver_auto/
--rw-r--r--   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 17:06:12.000000 chromedriver_auto-1.0.8/src/chromedriver_auto/__init__.py
--rw-r--r--   0 sorowerhossan   (501) staff       (20)     4386 2023-07-23 19:27:17.000000 chromedriver_auto-1.0.8/src/chromedriver_auto/driver_ready.py
-drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 19:27:57.035454 chromedriver_auto-1.0.8/src/chromedriver_auto.egg-info/
--rw-r--r--   0 sorowerhossan   (501) staff       (20)      791 2023-07-23 19:27:57.000000 chromedriver_auto-1.0.8/src/chromedriver_auto.egg-info/PKG-INFO
--rw-r--r--   0 sorowerhossan   (501) staff       (20)      294 2023-07-23 19:27:57.000000 chromedriver_auto-1.0.8/src/chromedriver_auto.egg-info/SOURCES.txt
--rw-r--r--   0 sorowerhossan   (501) staff       (20)        1 2023-07-23 19:27:57.000000 chromedriver_auto-1.0.8/src/chromedriver_auto.egg-info/dependency_links.txt
--rw-r--r--   0 sorowerhossan   (501) staff       (20)       18 2023-07-23 19:27:57.000000 chromedriver_auto-1.0.8/src/chromedriver_auto.egg-info/top_level.txt
+drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 19:39:50.506543 chromedriver_auto-1.0.9/
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)     1074 2023-07-23 17:17:05.000000 chromedriver_auto-1.0.9/LICENSE
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)     1401 2023-07-23 19:39:50.506626 chromedriver_auto-1.0.9/PKG-INFO
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)      765 2023-07-23 19:39:23.000000 chromedriver_auto-1.0.9/README.md
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)      339 2023-07-23 19:18:53.000000 chromedriver_auto-1.0.9/pyproject.toml
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)      761 2023-07-23 19:39:50.506877 chromedriver_auto-1.0.9/setup.cfg
+drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 19:39:50.504749 chromedriver_auto-1.0.9/src/
+drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 19:39:50.505644 chromedriver_auto-1.0.9/src/chromedriver_auto/
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 17:06:12.000000 chromedriver_auto-1.0.9/src/chromedriver_auto/__init__.py
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)     4321 2023-07-23 19:32:12.000000 chromedriver_auto-1.0.9/src/chromedriver_auto/driver_ready.py
+drwxr-xr-x   0 sorowerhossan   (501) staff       (20)        0 2023-07-23 19:39:50.506378 chromedriver_auto-1.0.9/src/chromedriver_auto.egg-info/
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)     1401 2023-07-23 19:39:50.000000 chromedriver_auto-1.0.9/src/chromedriver_auto.egg-info/PKG-INFO
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)      294 2023-07-23 19:39:50.000000 chromedriver_auto-1.0.9/src/chromedriver_auto.egg-info/SOURCES.txt
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)        1 2023-07-23 19:39:50.000000 chromedriver_auto-1.0.9/src/chromedriver_auto.egg-info/dependency_links.txt
+-rw-r--r--   0 sorowerhossan   (501) staff       (20)       18 2023-07-23 19:39:50.000000 chromedriver_auto-1.0.9/src/chromedriver_auto.egg-info/top_level.txt
```

### Comparing `chromedriver_auto-1.0.8/LICENSE` & `chromedriver_auto-1.0.9/LICENSE`

 * *Files identical despite different names*

### Comparing `chromedriver_auto-1.0.8/setup.cfg` & `chromedriver_auto-1.0.9/setup.cfg`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = chromedriver_auto
-version = 1.0.8
+version = 1.0.9
 author = Sorower Hossan
 author_email = sorower37@gmail.com
 description = This package downloads and helps you use chromedriver without needing to keep chromedriver updated regularly. Works for version no: 115.XX.XX.X and upwords.
 long_description = file: README.md
 long_description_content_type = text/markdown
 url = https://github.com/pypa/sampleproject
 project_urls =
```

### Comparing `chromedriver_auto-1.0.8/src/chromedriver_auto/driver_ready.py` & `chromedriver_auto-1.0.9/src/chromedriver_auto/driver_ready.py`

 * *Files 6% similar despite different names*

```diff
@@ -105,10 +105,8 @@
             os.remove(f'{file_path}/chromedriver-mac-arm64.zip')
         except:
             pass
 
 
         file_path= str(os.getcwd()) + '/chrome/chromedriver-mac-arm64'
     service = Service(executable_path=file_path)
-    driver = webdriver.Chrome(service=service)
-    driver.get('https://www.google.com')
-    print(driver.title)
+    driver = webdriver.Chrome(service=service)
```

