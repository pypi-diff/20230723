# Comparing `tmp/SageLogger-1.3.7.tar.gz` & `tmp/SageLogger-1.3.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "SageLogger-1.3.7.tar", last modified: Sun Jul 23 12:06:40 2023, max compression
+gzip compressed data, was "SageLogger-1.3.8.tar", last modified: Sun Jul 23 12:09:33 2023, max compression
```

## Comparing `SageLogger-1.3.7.tar` & `SageLogger-1.3.8.tar`

### file list

```diff
@@ -1,17 +1,17 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 12:06:40.565559 SageLogger-1.3.7/
--rw-rw-rw-   0        0        0    14387 2023-07-23 12:06:40.565035 SageLogger-1.3.7/PKG-INFO
--rw-rw-rw-   0        0        0    13793 2023-07-23 11:57:10.000000 SageLogger-1.3.7/README.md
-drwxrwxrwx   0        0        0        0 2023-07-23 12:06:40.552409 SageLogger-1.3.7/SageLogger/
--rw-rw-rw-   0        0        0    13885 2023-07-23 12:06:15.000000 SageLogger-1.3.7/SageLogger/Logger.py
--rw-rw-rw-   0        0        0     1562 2023-07-23 11:22:55.000000 SageLogger-1.3.7/SageLogger/SageException.py
--rw-rw-rw-   0        0        0     2954 2023-07-23 11:11:02.000000 SageLogger-1.3.7/SageLogger/SageFactory.py
--rw-rw-rw-   0        0        0       15 2023-07-22 20:32:47.000000 SageLogger-1.3.7/SageLogger/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 12:06:40.562966 SageLogger-1.3.7/SageLogger.egg-info/
--rw-rw-rw-   0        0        0    14387 2023-07-23 12:06:40.000000 SageLogger-1.3.7/SageLogger.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      300 2023-07-23 12:06:40.000000 SageLogger-1.3.7/SageLogger.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 12:06:40.000000 SageLogger-1.3.7/SageLogger.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       18 2023-07-23 12:06:40.000000 SageLogger-1.3.7/SageLogger.egg-info/requires.txt
--rw-rw-rw-   0        0        0       11 2023-07-23 12:06:40.000000 SageLogger-1.3.7/SageLogger.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      661 2023-07-23 12:06:32.000000 SageLogger-1.3.7/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-07-23 12:06:40.566071 SageLogger-1.3.7/setup.cfg
--rw-rw-rw-   0        0        0     1069 2023-07-23 12:06:30.000000 SageLogger-1.3.7/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 12:09:33.241176 SageLogger-1.3.8/
+-rw-rw-rw-   0        0        0    14387 2023-07-23 12:09:33.240175 SageLogger-1.3.8/PKG-INFO
+-rw-rw-rw-   0        0        0    13793 2023-07-23 11:57:10.000000 SageLogger-1.3.8/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 12:09:33.224201 SageLogger-1.3.8/SageLogger/
+-rw-rw-rw-   0        0        0    13884 2023-07-23 12:09:10.000000 SageLogger-1.3.8/SageLogger/Logger.py
+-rw-rw-rw-   0        0        0     1562 2023-07-23 11:22:55.000000 SageLogger-1.3.8/SageLogger/SageException.py
+-rw-rw-rw-   0        0        0     2954 2023-07-23 11:11:02.000000 SageLogger-1.3.8/SageLogger/SageFactory.py
+-rw-rw-rw-   0        0        0       15 2023-07-22 20:32:47.000000 SageLogger-1.3.8/SageLogger/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 12:09:33.236181 SageLogger-1.3.8/SageLogger.egg-info/
+-rw-rw-rw-   0        0        0    14387 2023-07-23 12:09:33.000000 SageLogger-1.3.8/SageLogger.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      300 2023-07-23 12:09:33.000000 SageLogger-1.3.8/SageLogger.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 12:09:33.000000 SageLogger-1.3.8/SageLogger.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       18 2023-07-23 12:09:33.000000 SageLogger-1.3.8/SageLogger.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       11 2023-07-23 12:09:33.000000 SageLogger-1.3.8/SageLogger.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      661 2023-07-23 12:09:20.000000 SageLogger-1.3.8/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-07-23 12:09:33.241689 SageLogger-1.3.8/setup.cfg
+-rw-rw-rw-   0        0        0     1069 2023-07-23 12:09:18.000000 SageLogger-1.3.8/setup.py
```

### Comparing `SageLogger-1.3.7/PKG-INFO` & `SageLogger-1.3.8/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: SageLogger
-Version: 1.3.7
+Version: 1.3.8
 Summary: Yet another python logger, or is it like any other?
 Home-page: https://github.com/PanSageYT/SageLogger
 Author: PanSageYT
 Author-email: PanSageYT <pansage@hugedick.fyi>
 Project-URL: Homepage, https://github.com/PanSageYT/SageLogger
 Project-URL: Bug Tracker, https://github.com/PanSageYT/SageLogger/issues
 Classifier: Programming Language :: Python :: 3
```

### Comparing `SageLogger-1.3.7/README.md` & `SageLogger-1.3.8/README.md`

 * *Files identical despite different names*

### Comparing `SageLogger-1.3.7/SageLogger/Logger.py` & `SageLogger-1.3.8/SageLogger/Logger.py`

 * *Files 0% similar despite different names*

```diff
@@ -46,15 +46,15 @@
     ONHOLD : xxPartType = xxPartType("ONHOLD", -2, "", True)
     NEGATIVE : xxPartType = xxPartType("NEGATIVE", -2, "", True)
     FROZEN : xxPartType = xxPartType("FROZEN", -2, "", True)
     INFORMATION : xxPartType = xxPartType("INFORMATION", -2, "", True)
     MILD_EXCEPTION : xxPartType = xxPartType("MILD_EXCEPTION", -2, "", True)
     DEBUG : xxPartType = xxPartType("DEBUG", -2, "", False)
     AMONGUS : xxPartType = xxPartType("AMONGUS", -2, "", True)
-    SAGE_LOGGER_DEBUG : xxPartType = xxPartType("SAGE_LOGGER_DEBUG", -2, "", False)
+    SAGE_LOGGER_DEBUG : xxPartType = xxPartType("SAGE_LOGGER_DEBUG", -2, "", True)
     def refresh(self, customization):
         self.DEFAULT = xxPartType("DEFAULT", 0, "", self.DEFAULT.enabled)
         self.POSITIVE = xxPartType("POSITIVE", 1, customization.setup_custom_border(colorama.Fore.GREEN + "+"), self.POSITIVE.enabled)
         self.ONHOLD = xxPartType("ONHOLD", 2, customization.setup_custom_border(colorama.Fore.YELLOW + "/"), self.ONHOLD.enabled)
         self.NEGATIVE = xxPartType("NEGATIVE", 3, customization.setup_custom_border(colorama.Fore.RED + "-"), self.NEGATIVE.enabled)
         self.FROZEN = xxPartType("FROZEN", 4, customization.setup_custom_border(colorama.Fore.LIGHTBLUE_EX + "#"), self.FROZEN.enabled)
         self.INFORMATION = xxPartType("INFORMATION", 5, customization.setup_custom_border(colorama.Fore.CYAN + "i"), self.INFORMATION.enabled)
```

### Comparing `SageLogger-1.3.7/SageLogger/SageException.py` & `SageLogger-1.3.8/SageLogger/SageException.py`

 * *Files identical despite different names*

### Comparing `SageLogger-1.3.7/SageLogger/SageFactory.py` & `SageLogger-1.3.8/SageLogger/SageFactory.py`

 * *Files identical despite different names*

### Comparing `SageLogger-1.3.7/SageLogger.egg-info/PKG-INFO` & `SageLogger-1.3.8/SageLogger.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: SageLogger
-Version: 1.3.7
+Version: 1.3.8
 Summary: Yet another python logger, or is it like any other?
 Home-page: https://github.com/PanSageYT/SageLogger
 Author: PanSageYT
 Author-email: PanSageYT <pansage@hugedick.fyi>
 Project-URL: Homepage, https://github.com/PanSageYT/SageLogger
 Project-URL: Bug Tracker, https://github.com/PanSageYT/SageLogger/issues
 Classifier: Programming Language :: Python :: 3
```

### Comparing `SageLogger-1.3.7/pyproject.toml` & `SageLogger-1.3.8/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["hatchling"]
 build-backend = "hatchling.build"
 
 [project]
 name = "SageLogger"
-version = "1.3.7"
+version = "1.3.8"
 authors = [
   { name="PanSageYT", email="pansage@hugedick.fyi" },
 ]
 description = "Yet another python logger, or is it like any other?"
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = [
```

### Comparing `SageLogger-1.3.7/setup.py` & `SageLogger-1.3.8/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 # Dane projektu
 project_name = "SageLogger"
-project_version = "1.3.7"
+project_version = "1.3.8"
 project_description = "Yet another python logger, or is it like any other?"
 project_author = "PanSageYT"
 project_author_email = "pansage@hugedick.fyi"
 
 # Zależności
 dependencies = [
     "colorama",
```

