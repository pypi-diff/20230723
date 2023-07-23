# Comparing `tmp/SageLogger-1.3.3.tar.gz` & `tmp/SageLogger-1.3.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "SageLogger-1.3.3.tar", last modified: Sun Jul 23 11:47:13 2023, max compression
+gzip compressed data, was "SageLogger-1.3.4.tar", last modified: Sun Jul 23 11:51:12 2023, max compression
```

## Comparing `SageLogger-1.3.3.tar` & `SageLogger-1.3.4.tar`

### file list

```diff
@@ -1,17 +1,17 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 11:47:13.398702 SageLogger-1.3.3/
--rw-rw-rw-   0        0        0    14375 2023-07-23 11:47:13.397700 SageLogger-1.3.3/PKG-INFO
--rw-rw-rw-   0        0        0    13781 2023-07-23 11:37:53.000000 SageLogger-1.3.3/README.md
-drwxrwxrwx   0        0        0        0 2023-07-23 11:47:13.387656 SageLogger-1.3.3/SageLogger/
--rw-rw-rw-   0        0        0    13216 2023-07-23 11:46:53.000000 SageLogger-1.3.3/SageLogger/Logger.py
--rw-rw-rw-   0        0        0     1562 2023-07-23 11:22:55.000000 SageLogger-1.3.3/SageLogger/SageException.py
--rw-rw-rw-   0        0        0     2954 2023-07-23 11:11:02.000000 SageLogger-1.3.3/SageLogger/SageFactory.py
--rw-rw-rw-   0        0        0       15 2023-07-22 20:32:47.000000 SageLogger-1.3.3/SageLogger/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 11:47:13.395699 SageLogger-1.3.3/SageLogger.egg-info/
--rw-rw-rw-   0        0        0    14375 2023-07-23 11:47:13.000000 SageLogger-1.3.3/SageLogger.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      300 2023-07-23 11:47:13.000000 SageLogger-1.3.3/SageLogger.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 11:47:13.000000 SageLogger-1.3.3/SageLogger.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       18 2023-07-23 11:47:13.000000 SageLogger-1.3.3/SageLogger.egg-info/requires.txt
--rw-rw-rw-   0        0        0       11 2023-07-23 11:47:13.000000 SageLogger-1.3.3/SageLogger.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      661 2023-07-23 11:47:10.000000 SageLogger-1.3.3/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-07-23 11:47:13.398702 SageLogger-1.3.3/setup.cfg
--rw-rw-rw-   0        0        0     1069 2023-07-23 11:38:27.000000 SageLogger-1.3.3/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 11:51:12.482623 SageLogger-1.3.4/
+-rw-rw-rw-   0        0        0    14375 2023-07-23 11:51:12.481622 SageLogger-1.3.4/PKG-INFO
+-rw-rw-rw-   0        0        0    13781 2023-07-23 11:37:53.000000 SageLogger-1.3.4/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 11:51:12.081799 SageLogger-1.3.4/SageLogger/
+-rw-rw-rw-   0        0        0    13357 2023-07-23 11:50:02.000000 SageLogger-1.3.4/SageLogger/Logger.py
+-rw-rw-rw-   0        0        0     1562 2023-07-23 11:22:55.000000 SageLogger-1.3.4/SageLogger/SageException.py
+-rw-rw-rw-   0        0        0     2954 2023-07-23 11:11:02.000000 SageLogger-1.3.4/SageLogger/SageFactory.py
+-rw-rw-rw-   0        0        0       15 2023-07-22 20:32:47.000000 SageLogger-1.3.4/SageLogger/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 11:51:12.469006 SageLogger-1.3.4/SageLogger.egg-info/
+-rw-rw-rw-   0        0        0    14375 2023-07-23 11:51:11.000000 SageLogger-1.3.4/SageLogger.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      300 2023-07-23 11:51:11.000000 SageLogger-1.3.4/SageLogger.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 11:51:11.000000 SageLogger-1.3.4/SageLogger.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       18 2023-07-23 11:51:11.000000 SageLogger-1.3.4/SageLogger.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       11 2023-07-23 11:51:11.000000 SageLogger-1.3.4/SageLogger.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      661 2023-07-23 11:51:04.000000 SageLogger-1.3.4/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-07-23 11:51:12.482623 SageLogger-1.3.4/setup.cfg
+-rw-rw-rw-   0        0        0     1069 2023-07-23 11:51:02.000000 SageLogger-1.3.4/setup.py
```

### Comparing `SageLogger-1.3.3/PKG-INFO` & `SageLogger-1.3.4/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: SageLogger
-Version: 1.3.3
+Version: 1.3.4
 Summary: Yet another python logger, or is it like any other?
 Home-page: https://github.com/PanSageYT/SageLogger
 Author: PanSageYT
 Author-email: PanSageYT <pansage@hugedick.fyi>
 Project-URL: Homepage, https://github.com/PanSageYT/SageLogger
 Project-URL: Bug Tracker, https://github.com/PanSageYT/SageLogger/issues
 Classifier: Programming Language :: Python :: 3
```

### Comparing `SageLogger-1.3.3/README.md` & `SageLogger-1.3.4/README.md`

 * *Files identical despite different names*

### Comparing `SageLogger-1.3.3/SageLogger/Logger.py` & `SageLogger-1.3.4/SageLogger/Logger.py`

 * *Files 1% similar despite different names*

```diff
@@ -124,14 +124,15 @@
             yield SageException.UhOhSomeoneTooCurious()
         type.enabled = True
         
     def disable_type(self, type):
         type.enabled = False
         
     def unlock_type_not_recommended_please_leave_it_alone_it_will_spam(self, type):
+        self.log("Unlocked, it isn't recommended, remember. This message cannot be turned off.", type=self.DynamicType.fromChar(self, "O"))
         type.lockedup = False
     
     def log(self, message : str, type : Union[tuple[int, str, bool], xxPartType] = Type.DEFAULT.value, color = colorama.Fore.RESET, id : int = -2137, date : bool = False, time : bool = False, datecolor : str = colorama.Fore.RESET, timecolor : str = colorama.Fore.RESET, showname : bool = True, ending : str = "\n"):
         typefinish = None
         if(isinstance(type, xxPartType)):
             typefinish = (type.Id, type.customization, type.enabled)
         else:
```

### Comparing `SageLogger-1.3.3/SageLogger/SageException.py` & `SageLogger-1.3.4/SageLogger/SageException.py`

 * *Files identical despite different names*

### Comparing `SageLogger-1.3.3/SageLogger/SageFactory.py` & `SageLogger-1.3.4/SageLogger/SageFactory.py`

 * *Files identical despite different names*

### Comparing `SageLogger-1.3.3/SageLogger.egg-info/PKG-INFO` & `SageLogger-1.3.4/SageLogger.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: SageLogger
-Version: 1.3.3
+Version: 1.3.4
 Summary: Yet another python logger, or is it like any other?
 Home-page: https://github.com/PanSageYT/SageLogger
 Author: PanSageYT
 Author-email: PanSageYT <pansage@hugedick.fyi>
 Project-URL: Homepage, https://github.com/PanSageYT/SageLogger
 Project-URL: Bug Tracker, https://github.com/PanSageYT/SageLogger/issues
 Classifier: Programming Language :: Python :: 3
```

### Comparing `SageLogger-1.3.3/pyproject.toml` & `SageLogger-1.3.4/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["hatchling"]
 build-backend = "hatchling.build"
 
 [project]
 name = "SageLogger"
-version = "1.3.3"
+version = "1.3.4"
 authors = [
   { name="PanSageYT", email="pansage@hugedick.fyi" },
 ]
 description = "Yet another python logger, or is it like any other?"
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = [
```

### Comparing `SageLogger-1.3.3/setup.py` & `SageLogger-1.3.4/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 # Dane projektu
 project_name = "SageLogger"
-project_version = "1.3.2"
+project_version = "1.3.4"
 project_description = "Yet another python logger, or is it like any other?"
 project_author = "PanSageYT"
 project_author_email = "pansage@hugedick.fyi"
 
 # Zależności
 dependencies = [
     "colorama",
```

