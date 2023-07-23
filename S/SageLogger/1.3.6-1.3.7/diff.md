# Comparing `tmp/SageLogger-1.3.6.tar.gz` & `tmp/SageLogger-1.3.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "SageLogger-1.3.6.tar", last modified: Sun Jul 23 12:05:00 2023, max compression
+gzip compressed data, was "SageLogger-1.3.7.tar", last modified: Sun Jul 23 12:06:40 2023, max compression
```

## Comparing `SageLogger-1.3.6.tar` & `SageLogger-1.3.7.tar`

### file list

```diff
@@ -1,17 +1,17 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 12:05:00.141785 SageLogger-1.3.6/
--rw-rw-rw-   0        0        0    14387 2023-07-23 12:05:00.141785 SageLogger-1.3.6/PKG-INFO
--rw-rw-rw-   0        0        0    13793 2023-07-23 11:57:10.000000 SageLogger-1.3.6/README.md
-drwxrwxrwx   0        0        0        0 2023-07-23 12:05:00.126751 SageLogger-1.3.6/SageLogger/
--rw-rw-rw-   0        0        0    13857 2023-07-23 12:04:29.000000 SageLogger-1.3.6/SageLogger/Logger.py
--rw-rw-rw-   0        0        0     1562 2023-07-23 11:22:55.000000 SageLogger-1.3.6/SageLogger/SageException.py
--rw-rw-rw-   0        0        0     2954 2023-07-23 11:11:02.000000 SageLogger-1.3.6/SageLogger/SageFactory.py
--rw-rw-rw-   0        0        0       15 2023-07-22 20:32:47.000000 SageLogger-1.3.6/SageLogger/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 12:05:00.138276 SageLogger-1.3.6/SageLogger.egg-info/
--rw-rw-rw-   0        0        0    14387 2023-07-23 12:04:59.000000 SageLogger-1.3.6/SageLogger.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      300 2023-07-23 12:05:00.000000 SageLogger-1.3.6/SageLogger.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 12:04:59.000000 SageLogger-1.3.6/SageLogger.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       18 2023-07-23 12:04:59.000000 SageLogger-1.3.6/SageLogger.egg-info/requires.txt
--rw-rw-rw-   0        0        0       11 2023-07-23 12:04:59.000000 SageLogger-1.3.6/SageLogger.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      661 2023-07-23 12:04:45.000000 SageLogger-1.3.6/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-07-23 12:05:00.142786 SageLogger-1.3.6/setup.cfg
--rw-rw-rw-   0        0        0     1069 2023-07-23 12:04:53.000000 SageLogger-1.3.6/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 12:06:40.565559 SageLogger-1.3.7/
+-rw-rw-rw-   0        0        0    14387 2023-07-23 12:06:40.565035 SageLogger-1.3.7/PKG-INFO
+-rw-rw-rw-   0        0        0    13793 2023-07-23 11:57:10.000000 SageLogger-1.3.7/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 12:06:40.552409 SageLogger-1.3.7/SageLogger/
+-rw-rw-rw-   0        0        0    13885 2023-07-23 12:06:15.000000 SageLogger-1.3.7/SageLogger/Logger.py
+-rw-rw-rw-   0        0        0     1562 2023-07-23 11:22:55.000000 SageLogger-1.3.7/SageLogger/SageException.py
+-rw-rw-rw-   0        0        0     2954 2023-07-23 11:11:02.000000 SageLogger-1.3.7/SageLogger/SageFactory.py
+-rw-rw-rw-   0        0        0       15 2023-07-22 20:32:47.000000 SageLogger-1.3.7/SageLogger/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 12:06:40.562966 SageLogger-1.3.7/SageLogger.egg-info/
+-rw-rw-rw-   0        0        0    14387 2023-07-23 12:06:40.000000 SageLogger-1.3.7/SageLogger.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      300 2023-07-23 12:06:40.000000 SageLogger-1.3.7/SageLogger.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 12:06:40.000000 SageLogger-1.3.7/SageLogger.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       18 2023-07-23 12:06:40.000000 SageLogger-1.3.7/SageLogger.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       11 2023-07-23 12:06:40.000000 SageLogger-1.3.7/SageLogger.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      661 2023-07-23 12:06:32.000000 SageLogger-1.3.7/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-07-23 12:06:40.566071 SageLogger-1.3.7/setup.cfg
+-rw-rw-rw-   0        0        0     1069 2023-07-23 12:06:30.000000 SageLogger-1.3.7/setup.py
```

### Comparing `SageLogger-1.3.6/PKG-INFO` & `SageLogger-1.3.7/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: SageLogger
-Version: 1.3.6
+Version: 1.3.7
 Summary: Yet another python logger, or is it like any other?
 Home-page: https://github.com/PanSageYT/SageLogger
 Author: PanSageYT
 Author-email: PanSageYT <pansage@hugedick.fyi>
 Project-URL: Homepage, https://github.com/PanSageYT/SageLogger
 Project-URL: Bug Tracker, https://github.com/PanSageYT/SageLogger/issues
 Classifier: Programming Language :: Python :: 3
```

### Comparing `SageLogger-1.3.6/README.md` & `SageLogger-1.3.7/README.md`

 * *Files identical despite different names*

### Comparing `SageLogger-1.3.6/SageLogger/Logger.py` & `SageLogger-1.3.7/SageLogger/Logger.py`

 * *Files 1% similar despite different names*

```diff
@@ -66,34 +66,34 @@
     def loggers_in_array(self):
         return [self.DEFAULT, self.POSITIVE, self.ONHOLD, self.NEGATIVE, self.FROZEN, self.INFORMATION, self.MILD_EXCEPTION, self.DEBUG, self.AMONGUS, self.SAGE_LOGGER_DEBUG]
     
     def __iter__(self):
         return self.loggers_in_array()
     
     def is_enabled_type(self, type):
-        return self.loggers_in_array()[type.id].enabled
+        return self.loggers_in_array()[type.Id].enabled
     
     def toggle_type(self, type):
         if (type.lockedup):
             yield SageException.UhOhSomeoneTooCurious()
-        self.loggers_in_array()[type.id].enabled = not self.loggers_in_array()[type.id].enabled
+        self.loggers_in_array()[type.Id].enabled = not self.loggers_in_array()[type.Id].enabled
         
     def enable_type(self, type):
-        if (self.loggers_in_array()[type.id].lockedup):
+        if (self.loggers_in_array()[type.Id].lockedup):
             yield SageException.UhOhSomeoneTooCurious()
-        self.loggers_in_array()[type.id].enabled = True
+        self.loggers_in_array()[type.Id].enabled = True
         
     def disable_type(self, type):
-        self.loggers_in_array()[type.id].enabled = False
+        self.loggers_in_array()[type.Id].enabled = False
         
     def unlock_type_not_recommended_please_leave_it_alone_it_will_spam(self, type):
         customization = xxCustomization(None)
         customization.bordcol = colorama.Back.RED + colorama.Fore.WHITE
         SageFactory.create(name="SageLoggerImportant").log("Unlocked, it isn't recommended, remember. This message cannot be turned off." + colorama.Back.RESET, type=xxPartType("IMPORTANT_HARD_CODED", 1, customization.setup_custom_border(colorama.Fore.LIGHTRED_EX + "!"), True))
-        type.lockedup = False
+        self.loggers_in_array()[type.Id].lockedup = False
 class MildError:
     @staticmethod
     def throw(logger, name, args):
         logger.log(f"Mild {name} - {args}, you don't need to catch it, but you may fix it ;)", type=SageConsoleLogger.Type.MILD_EXCEPTION)
         
 class xxCustomization:
     bordcol = colorama.Fore.LIGHTBLACK_EX
```

### Comparing `SageLogger-1.3.6/SageLogger/SageException.py` & `SageLogger-1.3.7/SageLogger/SageException.py`

 * *Files identical despite different names*

### Comparing `SageLogger-1.3.6/SageLogger/SageFactory.py` & `SageLogger-1.3.7/SageLogger/SageFactory.py`

 * *Files identical despite different names*

### Comparing `SageLogger-1.3.6/SageLogger.egg-info/PKG-INFO` & `SageLogger-1.3.7/SageLogger.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: SageLogger
-Version: 1.3.6
+Version: 1.3.7
 Summary: Yet another python logger, or is it like any other?
 Home-page: https://github.com/PanSageYT/SageLogger
 Author: PanSageYT
 Author-email: PanSageYT <pansage@hugedick.fyi>
 Project-URL: Homepage, https://github.com/PanSageYT/SageLogger
 Project-URL: Bug Tracker, https://github.com/PanSageYT/SageLogger/issues
 Classifier: Programming Language :: Python :: 3
```

### Comparing `SageLogger-1.3.6/pyproject.toml` & `SageLogger-1.3.7/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["hatchling"]
 build-backend = "hatchling.build"
 
 [project]
 name = "SageLogger"
-version = "1.3.6"
+version = "1.3.7"
 authors = [
   { name="PanSageYT", email="pansage@hugedick.fyi" },
 ]
 description = "Yet another python logger, or is it like any other?"
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = [
```

### Comparing `SageLogger-1.3.6/setup.py` & `SageLogger-1.3.7/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 # Dane projektu
 project_name = "SageLogger"
-project_version = "1.3.6"
+project_version = "1.3.7"
 project_description = "Yet another python logger, or is it like any other?"
 project_author = "PanSageYT"
 project_author_email = "pansage@hugedick.fyi"
 
 # Zależności
 dependencies = [
     "colorama",
```

