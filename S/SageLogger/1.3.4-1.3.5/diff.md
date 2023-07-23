# Comparing `tmp/SageLogger-1.3.4.tar.gz` & `tmp/SageLogger-1.3.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "SageLogger-1.3.4.tar", last modified: Sun Jul 23 11:51:12 2023, max compression
+gzip compressed data, was "SageLogger-1.3.5.tar", last modified: Sun Jul 23 11:58:01 2023, max compression
```

## Comparing `SageLogger-1.3.4.tar` & `SageLogger-1.3.5.tar`

### file list

```diff
@@ -1,17 +1,17 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 11:51:12.482623 SageLogger-1.3.4/
--rw-rw-rw-   0        0        0    14375 2023-07-23 11:51:12.481622 SageLogger-1.3.4/PKG-INFO
--rw-rw-rw-   0        0        0    13781 2023-07-23 11:37:53.000000 SageLogger-1.3.4/README.md
-drwxrwxrwx   0        0        0        0 2023-07-23 11:51:12.081799 SageLogger-1.3.4/SageLogger/
--rw-rw-rw-   0        0        0    13357 2023-07-23 11:50:02.000000 SageLogger-1.3.4/SageLogger/Logger.py
--rw-rw-rw-   0        0        0     1562 2023-07-23 11:22:55.000000 SageLogger-1.3.4/SageLogger/SageException.py
--rw-rw-rw-   0        0        0     2954 2023-07-23 11:11:02.000000 SageLogger-1.3.4/SageLogger/SageFactory.py
--rw-rw-rw-   0        0        0       15 2023-07-22 20:32:47.000000 SageLogger-1.3.4/SageLogger/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 11:51:12.469006 SageLogger-1.3.4/SageLogger.egg-info/
--rw-rw-rw-   0        0        0    14375 2023-07-23 11:51:11.000000 SageLogger-1.3.4/SageLogger.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      300 2023-07-23 11:51:11.000000 SageLogger-1.3.4/SageLogger.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 11:51:11.000000 SageLogger-1.3.4/SageLogger.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       18 2023-07-23 11:51:11.000000 SageLogger-1.3.4/SageLogger.egg-info/requires.txt
--rw-rw-rw-   0        0        0       11 2023-07-23 11:51:11.000000 SageLogger-1.3.4/SageLogger.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      661 2023-07-23 11:51:04.000000 SageLogger-1.3.4/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-07-23 11:51:12.482623 SageLogger-1.3.4/setup.cfg
--rw-rw-rw-   0        0        0     1069 2023-07-23 11:51:02.000000 SageLogger-1.3.4/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 11:58:01.050447 SageLogger-1.3.5/
+-rw-rw-rw-   0        0        0    14387 2023-07-23 11:58:01.049446 SageLogger-1.3.5/PKG-INFO
+-rw-rw-rw-   0        0        0    13793 2023-07-23 11:57:10.000000 SageLogger-1.3.5/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 11:58:01.031460 SageLogger-1.3.5/SageLogger/
+-rw-rw-rw-   0        0        0    13635 2023-07-23 11:56:40.000000 SageLogger-1.3.5/SageLogger/Logger.py
+-rw-rw-rw-   0        0        0     1562 2023-07-23 11:22:55.000000 SageLogger-1.3.5/SageLogger/SageException.py
+-rw-rw-rw-   0        0        0     2954 2023-07-23 11:11:02.000000 SageLogger-1.3.5/SageLogger/SageFactory.py
+-rw-rw-rw-   0        0        0       15 2023-07-22 20:32:47.000000 SageLogger-1.3.5/SageLogger/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 11:58:01.041839 SageLogger-1.3.5/SageLogger.egg-info/
+-rw-rw-rw-   0        0        0    14387 2023-07-23 11:58:00.000000 SageLogger-1.3.5/SageLogger.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      300 2023-07-23 11:58:00.000000 SageLogger-1.3.5/SageLogger.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 11:58:00.000000 SageLogger-1.3.5/SageLogger.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       18 2023-07-23 11:58:00.000000 SageLogger-1.3.5/SageLogger.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       11 2023-07-23 11:58:00.000000 SageLogger-1.3.5/SageLogger.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      661 2023-07-23 11:57:55.000000 SageLogger-1.3.5/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-07-23 11:58:01.050447 SageLogger-1.3.5/setup.cfg
+-rw-rw-rw-   0        0        0     1069 2023-07-23 11:57:53.000000 SageLogger-1.3.5/setup.py
```

### Comparing `SageLogger-1.3.4/PKG-INFO` & `SageLogger-1.3.5/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: SageLogger
-Version: 1.3.4
+Version: 1.3.5
 Summary: Yet another python logger, or is it like any other?
 Home-page: https://github.com/PanSageYT/SageLogger
 Author: PanSageYT
 Author-email: PanSageYT <pansage@hugedick.fyi>
 Project-URL: Homepage, https://github.com/PanSageYT/SageLogger
 Project-URL: Bug Tracker, https://github.com/PanSageYT/SageLogger/issues
 Classifier: Programming Language :: Python :: 3
@@ -218,17 +218,14 @@
 
 ## Classes
 
 ### SageConsoleLogger
 - Description: Provides console logging capabilities.
 - Methods:
   - `is_enabled_type(type)`: Checks if the given log type is enabled.
-  - `toggle_type(type)`: Toggles the given log type on/off.
-  - `enable_type(type)`: Enables the given log type.
-  - `disable_type(type)`: Disables the given log type.
   - `log(message, type = Type.DEFAULT.value, color = colorama.Fore.RESET, id = -2137, date = False, time = False, datecolor = colorama.Fore.RESET, timecolor = colorama.Fore.RESET, showname = True, ending = "\n")`: Logs a message with the specified log type and customization options.
   - `ask(message, type = Type.DEFAULT.value, color = colorama.Fore.RESET, answercolor = colorama.Fore.RESET, id = -2137, date = False, time = False, datecolor = colorama.Fore.RESET, timecolor = colorama.Fore.RESET)`: Asks a question with the specified log type and customization options.
 
 ### SageRemoteLogger (Based on SageConsoleLogger)
 - Description: Provides remote logging capabilities using HTTP requests.
 - Methods:
   - `log(message, print_on_console = False, ending = "\n")`: Logs a message and sends it remotely using an HTTP request.
@@ -243,14 +240,18 @@
 - Methods:
   - `set_border_style(border_colorama, borders)`: Sets the border style for log messages.
   - `setup_custom_border(cos)`: Sets up a custom border for the log message.
 
 ### SageConsoleLogger.Type
 - Description: Enumerates different log types with customizations.
 - Properties: `DEFAULT`, `POSITIVE`, `ONHOLD`, `NEGATIVE`, `FROZEN`, `INFORMATION`, `MILD_EXCEPTION`, `DEBUG`, `AMONGUS`, `SAGE_LOGGER_DEBUG`
+- Methods:
+  - `toggle_type(type)`: Toggles the given log type on/off.
+  - `enable_type(type)`: Enables the given log type.
+  - `disable_type(type)`: Disables the given log type.
 
 ### SageConsoleLogger.Type.XYZ (PartType)
 - Description: Defines a part of a log type with customization options.
 - Properties: `name`, `Id`, `customization`, `value`, `enabled`, `lockedup`
 
 ### DynamicType
 - Description: Represents dynamic log types.
```

### Comparing `SageLogger-1.3.4/README.md` & `SageLogger-1.3.5/README.md`

 * *Files 0% similar despite different names*

```diff
@@ -203,17 +203,14 @@
 
 ## Classes
 
 ### SageConsoleLogger
 - Description: Provides console logging capabilities.
 - Methods:
   - `is_enabled_type(type)`: Checks if the given log type is enabled.
-  - `toggle_type(type)`: Toggles the given log type on/off.
-  - `enable_type(type)`: Enables the given log type.
-  - `disable_type(type)`: Disables the given log type.
   - `log(message, type = Type.DEFAULT.value, color = colorama.Fore.RESET, id = -2137, date = False, time = False, datecolor = colorama.Fore.RESET, timecolor = colorama.Fore.RESET, showname = True, ending = "\n")`: Logs a message with the specified log type and customization options.
   - `ask(message, type = Type.DEFAULT.value, color = colorama.Fore.RESET, answercolor = colorama.Fore.RESET, id = -2137, date = False, time = False, datecolor = colorama.Fore.RESET, timecolor = colorama.Fore.RESET)`: Asks a question with the specified log type and customization options.
 
 ### SageRemoteLogger (Based on SageConsoleLogger)
 - Description: Provides remote logging capabilities using HTTP requests.
 - Methods:
   - `log(message, print_on_console = False, ending = "\n")`: Logs a message and sends it remotely using an HTTP request.
@@ -228,14 +225,18 @@
 - Methods:
   - `set_border_style(border_colorama, borders)`: Sets the border style for log messages.
   - `setup_custom_border(cos)`: Sets up a custom border for the log message.
 
 ### SageConsoleLogger.Type
 - Description: Enumerates different log types with customizations.
 - Properties: `DEFAULT`, `POSITIVE`, `ONHOLD`, `NEGATIVE`, `FROZEN`, `INFORMATION`, `MILD_EXCEPTION`, `DEBUG`, `AMONGUS`, `SAGE_LOGGER_DEBUG`
+- Methods:
+  - `toggle_type(type)`: Toggles the given log type on/off.
+  - `enable_type(type)`: Enables the given log type.
+  - `disable_type(type)`: Disables the given log type.
 
 ### SageConsoleLogger.Type.XYZ (PartType)
 - Description: Defines a part of a log type with customization options.
 - Properties: `name`, `Id`, `customization`, `value`, `enabled`, `lockedup`
 
 ### DynamicType
 - Description: Represents dynamic log types.
```

### Comparing `SageLogger-1.3.4/SageLogger/Logger.py` & `SageLogger-1.3.5/SageLogger/Logger.py`

 * *Files 2% similar despite different names*

```diff
@@ -58,18 +58,40 @@
         self.NEGATIVE = xxPartType("NEGATIVE", 3, customization.setup_custom_border(colorama.Fore.RED + "-"), self.NEGATIVE.enabled)
         self.FROZEN = xxPartType("FROZEN", 4, customization.setup_custom_border(colorama.Fore.LIGHTBLUE_EX + "#"), self.FROZEN.enabled)
         self.INFORMATION = xxPartType("INFORMATION", 5, customization.setup_custom_border(colorama.Fore.CYAN + "i"), self.INFORMATION.enabled)
         self.MILD_EXCEPTION = xxPartType("MILD_EXCEPTION", 6, customization.setup_custom_border(colorama.Fore.LIGHTRED_EX + "X"), self.MILD_EXCEPTION.enabled)
         self.DEBUG = xxPartType("DEBUG", 7, customization.setup_custom_border(colorama.Fore.LIGHTMAGENTA_EX + "*"), self.DEBUG.enabled)
         self.AMONGUS = xxPartType("AMONGUS", 8, customization.setup_custom_border(colorama.Fore.RED + "ඞ"), self.AMONGUS.enabled)
         self.SAGE_LOGGER_DEBUG = xxPartType("SAGE_LOGGER_DEBUG", 9, customization.setup_custom_border(colorama.Fore.LIGHTGREEN_EX + "S" + colorama.Fore.GREEN + "L" + colorama.Fore.LIGHTMAGENTA_EX + "D"), self.SAGE_LOGGER_DEBUG.enabled and not self.SAGE_LOGGER_DEBUG.lockedup)
-        
-    def __iter__(self):
+    
+    def loggers_in_array(self):
         return [self.DEFAULT, self.POSITIVE, self.ONHOLD, self.NEGATIVE, self.FROZEN, self.INFORMATION, self.MILD_EXCEPTION, self.DEBUG, self.AMONGUS, self.SAGE_LOGGER_DEBUG]
-
+    
+    def __iter__(self):
+        return self.loggers_in_array()
+    
+    def is_enabled_type(self, type):
+        return self.loggers_in_array()[type.id].enabled
+    
+    def toggle_type(self, type):
+        if (type.lockedup):
+            yield SageException.UhOhSomeoneTooCurious()
+        self.loggers_in_array()[type.id].enabled = not self.loggers_in_array()[type.id].enabled
+        
+    def enable_type(self, type):
+        if (self.loggers_in_array()[type.id].lockedup):
+            yield SageException.UhOhSomeoneTooCurious()
+        self.loggers_in_array()[type.id].enabled = True
+        
+    def disable_type(self, type):
+        self.loggers_in_array()[type.id].enabled = False
+        
+    def unlock_type_not_recommended_please_leave_it_alone_it_will_spam(self, type):
+        SageFactory.create(name="SageLoggerImportant").log("Unlocked, it isn't recommended, remember. This message cannot be turned off.", type=DynamicType.fromChar(self, "O"))
+        type.lockedup = False
 class MildError:
     @staticmethod
     def throw(logger, name, args):
         logger.log(f"Mild {name} - {args}, you don't need to catch it, but you may fix it ;)", type=SageConsoleLogger.Type.MILD_EXCEPTION)
         
 class xxCustomization:
     bordcol = colorama.Fore.LIGHTBLACK_EX
@@ -107,34 +129,14 @@
         self.logfile = logfile
         self.savetofile = savetofile
         if savetofile:
             with open(self.name + "." + self.logfile, "a") as wr:
                 wr.write(("-" * 16) + " " + datetime.datetime.now().strftime("%d/%m/%Y, %H:%M:%S") + " " + ("-" * 16) + "\n")
                 wr.close()
     
-    def is_enabled_type(self, type):
-        return type.enabled
-    
-    def toggle_type(self, type):
-        if (type.lockedup):
-            yield SageException.UhOhSomeoneTooCurious()
-        type.enabled = not type.enabled
-        
-    def enable_type(self, type):
-        if (type.lockedup):
-            yield SageException.UhOhSomeoneTooCurious()
-        type.enabled = True
-        
-    def disable_type(self, type):
-        type.enabled = False
-        
-    def unlock_type_not_recommended_please_leave_it_alone_it_will_spam(self, type):
-        self.log("Unlocked, it isn't recommended, remember. This message cannot be turned off.", type=self.DynamicType.fromChar(self, "O"))
-        type.lockedup = False
-    
     def log(self, message : str, type : Union[tuple[int, str, bool], xxPartType] = Type.DEFAULT.value, color = colorama.Fore.RESET, id : int = -2137, date : bool = False, time : bool = False, datecolor : str = colorama.Fore.RESET, timecolor : str = colorama.Fore.RESET, showname : bool = True, ending : str = "\n"):
         typefinish = None
         if(isinstance(type, xxPartType)):
             typefinish = (type.Id, type.customization, type.enabled)
         else:
             typefinish = type
         if not typefinish[2]:
```

### Comparing `SageLogger-1.3.4/SageLogger/SageException.py` & `SageLogger-1.3.5/SageLogger/SageException.py`

 * *Files identical despite different names*

### Comparing `SageLogger-1.3.4/SageLogger/SageFactory.py` & `SageLogger-1.3.5/SageLogger/SageFactory.py`

 * *Files identical despite different names*

### Comparing `SageLogger-1.3.4/SageLogger.egg-info/PKG-INFO` & `SageLogger-1.3.5/SageLogger.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: SageLogger
-Version: 1.3.4
+Version: 1.3.5
 Summary: Yet another python logger, or is it like any other?
 Home-page: https://github.com/PanSageYT/SageLogger
 Author: PanSageYT
 Author-email: PanSageYT <pansage@hugedick.fyi>
 Project-URL: Homepage, https://github.com/PanSageYT/SageLogger
 Project-URL: Bug Tracker, https://github.com/PanSageYT/SageLogger/issues
 Classifier: Programming Language :: Python :: 3
@@ -218,17 +218,14 @@
 
 ## Classes
 
 ### SageConsoleLogger
 - Description: Provides console logging capabilities.
 - Methods:
   - `is_enabled_type(type)`: Checks if the given log type is enabled.
-  - `toggle_type(type)`: Toggles the given log type on/off.
-  - `enable_type(type)`: Enables the given log type.
-  - `disable_type(type)`: Disables the given log type.
   - `log(message, type = Type.DEFAULT.value, color = colorama.Fore.RESET, id = -2137, date = False, time = False, datecolor = colorama.Fore.RESET, timecolor = colorama.Fore.RESET, showname = True, ending = "\n")`: Logs a message with the specified log type and customization options.
   - `ask(message, type = Type.DEFAULT.value, color = colorama.Fore.RESET, answercolor = colorama.Fore.RESET, id = -2137, date = False, time = False, datecolor = colorama.Fore.RESET, timecolor = colorama.Fore.RESET)`: Asks a question with the specified log type and customization options.
 
 ### SageRemoteLogger (Based on SageConsoleLogger)
 - Description: Provides remote logging capabilities using HTTP requests.
 - Methods:
   - `log(message, print_on_console = False, ending = "\n")`: Logs a message and sends it remotely using an HTTP request.
@@ -243,14 +240,18 @@
 - Methods:
   - `set_border_style(border_colorama, borders)`: Sets the border style for log messages.
   - `setup_custom_border(cos)`: Sets up a custom border for the log message.
 
 ### SageConsoleLogger.Type
 - Description: Enumerates different log types with customizations.
 - Properties: `DEFAULT`, `POSITIVE`, `ONHOLD`, `NEGATIVE`, `FROZEN`, `INFORMATION`, `MILD_EXCEPTION`, `DEBUG`, `AMONGUS`, `SAGE_LOGGER_DEBUG`
+- Methods:
+  - `toggle_type(type)`: Toggles the given log type on/off.
+  - `enable_type(type)`: Enables the given log type.
+  - `disable_type(type)`: Disables the given log type.
 
 ### SageConsoleLogger.Type.XYZ (PartType)
 - Description: Defines a part of a log type with customization options.
 - Properties: `name`, `Id`, `customization`, `value`, `enabled`, `lockedup`
 
 ### DynamicType
 - Description: Represents dynamic log types.
```

### Comparing `SageLogger-1.3.4/pyproject.toml` & `SageLogger-1.3.5/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["hatchling"]
 build-backend = "hatchling.build"
 
 [project]
 name = "SageLogger"
-version = "1.3.4"
+version = "1.3.5"
 authors = [
   { name="PanSageYT", email="pansage@hugedick.fyi" },
 ]
 description = "Yet another python logger, or is it like any other?"
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = [
```

### Comparing `SageLogger-1.3.4/setup.py` & `SageLogger-1.3.5/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 # Dane projektu
 project_name = "SageLogger"
-project_version = "1.3.4"
+project_version = "1.3.5"
 project_description = "Yet another python logger, or is it like any other?"
 project_author = "PanSageYT"
 project_author_email = "pansage@hugedick.fyi"
 
 # Zależności
 dependencies = [
     "colorama",
```

