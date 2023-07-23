# Comparing `tmp/SageLogger-1.3.2.tar.gz` & `tmp/SageLogger-1.3.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "SageLogger-1.3.2.tar", last modified: Sun Jul 23 11:38:45 2023, max compression
+gzip compressed data, was "SageLogger-1.3.3.tar", last modified: Sun Jul 23 11:47:13 2023, max compression
```

## Comparing `SageLogger-1.3.2.tar` & `SageLogger-1.3.3.tar`

### file list

```diff
@@ -1,17 +1,17 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 11:38:45.932696 SageLogger-1.3.2/
--rw-rw-rw-   0        0        0    14375 2023-07-23 11:38:45.931121 SageLogger-1.3.2/PKG-INFO
--rw-rw-rw-   0        0        0    13781 2023-07-23 11:37:53.000000 SageLogger-1.3.2/README.md
-drwxrwxrwx   0        0        0        0 2023-07-23 11:38:45.917469 SageLogger-1.3.2/SageLogger/
--rw-rw-rw-   0        0        0    13166 2023-07-23 11:26:27.000000 SageLogger-1.3.2/SageLogger/Logger.py
--rw-rw-rw-   0        0        0     1562 2023-07-23 11:22:55.000000 SageLogger-1.3.2/SageLogger/SageException.py
--rw-rw-rw-   0        0        0     2954 2023-07-23 11:11:02.000000 SageLogger-1.3.2/SageLogger/SageFactory.py
--rw-rw-rw-   0        0        0       15 2023-07-22 20:32:47.000000 SageLogger-1.3.2/SageLogger/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 11:38:45.928611 SageLogger-1.3.2/SageLogger.egg-info/
--rw-rw-rw-   0        0        0    14375 2023-07-23 11:38:45.000000 SageLogger-1.3.2/SageLogger.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      300 2023-07-23 11:38:45.000000 SageLogger-1.3.2/SageLogger.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 11:38:45.000000 SageLogger-1.3.2/SageLogger.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       18 2023-07-23 11:38:45.000000 SageLogger-1.3.2/SageLogger.egg-info/requires.txt
--rw-rw-rw-   0        0        0       11 2023-07-23 11:38:45.000000 SageLogger-1.3.2/SageLogger.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      661 2023-07-23 11:38:29.000000 SageLogger-1.3.2/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-07-23 11:38:45.933205 SageLogger-1.3.2/setup.cfg
--rw-rw-rw-   0        0        0     1069 2023-07-23 11:38:27.000000 SageLogger-1.3.2/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 11:47:13.398702 SageLogger-1.3.3/
+-rw-rw-rw-   0        0        0    14375 2023-07-23 11:47:13.397700 SageLogger-1.3.3/PKG-INFO
+-rw-rw-rw-   0        0        0    13781 2023-07-23 11:37:53.000000 SageLogger-1.3.3/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 11:47:13.387656 SageLogger-1.3.3/SageLogger/
+-rw-rw-rw-   0        0        0    13216 2023-07-23 11:46:53.000000 SageLogger-1.3.3/SageLogger/Logger.py
+-rw-rw-rw-   0        0        0     1562 2023-07-23 11:22:55.000000 SageLogger-1.3.3/SageLogger/SageException.py
+-rw-rw-rw-   0        0        0     2954 2023-07-23 11:11:02.000000 SageLogger-1.3.3/SageLogger/SageFactory.py
+-rw-rw-rw-   0        0        0       15 2023-07-22 20:32:47.000000 SageLogger-1.3.3/SageLogger/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 11:47:13.395699 SageLogger-1.3.3/SageLogger.egg-info/
+-rw-rw-rw-   0        0        0    14375 2023-07-23 11:47:13.000000 SageLogger-1.3.3/SageLogger.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      300 2023-07-23 11:47:13.000000 SageLogger-1.3.3/SageLogger.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 11:47:13.000000 SageLogger-1.3.3/SageLogger.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       18 2023-07-23 11:47:13.000000 SageLogger-1.3.3/SageLogger.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       11 2023-07-23 11:47:13.000000 SageLogger-1.3.3/SageLogger.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      661 2023-07-23 11:47:10.000000 SageLogger-1.3.3/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-07-23 11:47:13.398702 SageLogger-1.3.3/setup.cfg
+-rw-rw-rw-   0        0        0     1069 2023-07-23 11:38:27.000000 SageLogger-1.3.3/setup.py
```

### Comparing `SageLogger-1.3.2/PKG-INFO` & `SageLogger-1.3.3/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: SageLogger
-Version: 1.3.2
+Version: 1.3.3
 Summary: Yet another python logger, or is it like any other?
 Home-page: https://github.com/PanSageYT/SageLogger
 Author: PanSageYT
 Author-email: PanSageYT <pansage@hugedick.fyi>
 Project-URL: Homepage, https://github.com/PanSageYT/SageLogger
 Project-URL: Bug Tracker, https://github.com/PanSageYT/SageLogger/issues
 Classifier: Programming Language :: Python :: 3
```

### Comparing `SageLogger-1.3.2/README.md` & `SageLogger-1.3.3/README.md`

 * *Files identical despite different names*

### Comparing `SageLogger-1.3.2/SageLogger/Logger.py` & `SageLogger-1.3.3/SageLogger/Logger.py`

 * *Files 1% similar despite different names*

```diff
@@ -57,15 +57,15 @@
         self.ONHOLD = xxPartType("ONHOLD", 2, customization.setup_custom_border(colorama.Fore.YELLOW + "/"), self.ONHOLD.enabled)
         self.NEGATIVE = xxPartType("NEGATIVE", 3, customization.setup_custom_border(colorama.Fore.RED + "-"), self.NEGATIVE.enabled)
         self.FROZEN = xxPartType("FROZEN", 4, customization.setup_custom_border(colorama.Fore.LIGHTBLUE_EX + "#"), self.FROZEN.enabled)
         self.INFORMATION = xxPartType("INFORMATION", 5, customization.setup_custom_border(colorama.Fore.CYAN + "i"), self.INFORMATION.enabled)
         self.MILD_EXCEPTION = xxPartType("MILD_EXCEPTION", 6, customization.setup_custom_border(colorama.Fore.LIGHTRED_EX + "X"), self.MILD_EXCEPTION.enabled)
         self.DEBUG = xxPartType("DEBUG", 7, customization.setup_custom_border(colorama.Fore.LIGHTMAGENTA_EX + "*"), self.DEBUG.enabled)
         self.AMONGUS = xxPartType("AMONGUS", 8, customization.setup_custom_border(colorama.Fore.RED + "ඞ"), self.AMONGUS.enabled)
-        self.SAGE_LOGGER_DEBUG = xxPartType("SAGE_LOGGER_DEBUG", 9, customization.setup_custom_border(colorama.Fore.LIGHTGREEN_EX + "S" + colorama.Fore.GREEN + "L" + colorama.Fore.LIGHTMAGENTA_EX + "D"), False, lockedup=True)
+        self.SAGE_LOGGER_DEBUG = xxPartType("SAGE_LOGGER_DEBUG", 9, customization.setup_custom_border(colorama.Fore.LIGHTGREEN_EX + "S" + colorama.Fore.GREEN + "L" + colorama.Fore.LIGHTMAGENTA_EX + "D"), self.SAGE_LOGGER_DEBUG.enabled and not self.SAGE_LOGGER_DEBUG.lockedup)
         
     def __iter__(self):
         return [self.DEFAULT, self.POSITIVE, self.ONHOLD, self.NEGATIVE, self.FROZEN, self.INFORMATION, self.MILD_EXCEPTION, self.DEBUG, self.AMONGUS, self.SAGE_LOGGER_DEBUG]
 
 class MildError:
     @staticmethod
     def throw(logger, name, args):
```

### Comparing `SageLogger-1.3.2/SageLogger/SageException.py` & `SageLogger-1.3.3/SageLogger/SageException.py`

 * *Files identical despite different names*

### Comparing `SageLogger-1.3.2/SageLogger/SageFactory.py` & `SageLogger-1.3.3/SageLogger/SageFactory.py`

 * *Files identical despite different names*

### Comparing `SageLogger-1.3.2/SageLogger.egg-info/PKG-INFO` & `SageLogger-1.3.3/SageLogger.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: SageLogger
-Version: 1.3.2
+Version: 1.3.3
 Summary: Yet another python logger, or is it like any other?
 Home-page: https://github.com/PanSageYT/SageLogger
 Author: PanSageYT
 Author-email: PanSageYT <pansage@hugedick.fyi>
 Project-URL: Homepage, https://github.com/PanSageYT/SageLogger
 Project-URL: Bug Tracker, https://github.com/PanSageYT/SageLogger/issues
 Classifier: Programming Language :: Python :: 3
```

### Comparing `SageLogger-1.3.2/pyproject.toml` & `SageLogger-1.3.3/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["hatchling"]
 build-backend = "hatchling.build"
 
 [project]
 name = "SageLogger"
-version = "1.3.2"
+version = "1.3.3"
 authors = [
   { name="PanSageYT", email="pansage@hugedick.fyi" },
 ]
 description = "Yet another python logger, or is it like any other?"
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = [
```

### Comparing `SageLogger-1.3.2/setup.py` & `SageLogger-1.3.3/setup.py`

 * *Files identical despite different names*

