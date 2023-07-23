# Comparing `tmp/SageLogger-1.0.tar.gz` & `tmp/SageLogger-1.3.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "SageLogger-1.0.tar", last modified: Sat Jul 22 21:58:50 2023, max compression
+gzip compressed data, was "SageLogger-1.3.1.tar", last modified: Sun Jul 23 11:36:02 2023, max compression
```

## Comparing `SageLogger-1.0.tar` & `SageLogger-1.3.1.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxrwxrwx   0        0        0        0 2023-07-22 21:58:50.489445 SageLogger-1.0/
--rw-rw-rw-   0        0        0     4355 2023-07-22 21:58:50.488444 SageLogger-1.0/PKG-INFO
-drwxrwxrwx   0        0        0        0 2023-07-22 21:58:50.475735 SageLogger-1.0/SageLogger/
--rw-rw-rw-   0        0        0    11724 2023-07-22 21:46:42.000000 SageLogger-1.0/SageLogger/Logger.py
--rw-rw-rw-   0        0        0       93 2023-07-22 18:28:14.000000 SageLogger-1.0/SageLogger/SageException.py
--rw-rw-rw-   0        0        0      642 2023-07-22 19:24:28.000000 SageLogger-1.0/SageLogger/SageFactory.py
--rw-rw-rw-   0        0        0       15 2023-07-22 20:32:47.000000 SageLogger-1.0/SageLogger/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-22 21:58:50.486442 SageLogger-1.0/SageLogger.egg-info/
--rw-rw-rw-   0        0        0     4355 2023-07-22 21:58:50.000000 SageLogger-1.0/SageLogger.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      290 2023-07-22 21:58:50.000000 SageLogger-1.0/SageLogger.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-22 21:58:50.000000 SageLogger-1.0/SageLogger.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       18 2023-07-22 21:58:50.000000 SageLogger-1.0/SageLogger.egg-info/requires.txt
--rw-rw-rw-   0        0        0       11 2023-07-22 21:58:50.000000 SageLogger-1.0/SageLogger.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      659 2023-07-22 21:58:39.000000 SageLogger-1.0/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-07-22 21:58:50.489445 SageLogger-1.0/setup.cfg
--rw-rw-rw-   0        0        0     1067 2023-07-22 21:58:44.000000 SageLogger-1.0/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 11:36:02.139053 SageLogger-1.3.1/
+-rw-rw-rw-   0        0        0     4701 2023-07-23 11:36:02.136546 SageLogger-1.3.1/PKG-INFO
+drwxrwxrwx   0        0        0        0 2023-07-23 11:36:02.122835 SageLogger-1.3.1/SageLogger/
+-rw-rw-rw-   0        0        0    13166 2023-07-23 11:26:27.000000 SageLogger-1.3.1/SageLogger/Logger.py
+-rw-rw-rw-   0        0        0     1562 2023-07-23 11:22:55.000000 SageLogger-1.3.1/SageLogger/SageException.py
+-rw-rw-rw-   0        0        0     2954 2023-07-23 11:11:02.000000 SageLogger-1.3.1/SageLogger/SageFactory.py
+-rw-rw-rw-   0        0        0       15 2023-07-22 20:32:47.000000 SageLogger-1.3.1/SageLogger/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 11:36:02.133543 SageLogger-1.3.1/SageLogger.egg-info/
+-rw-rw-rw-   0        0        0     4701 2023-07-23 11:36:01.000000 SageLogger-1.3.1/SageLogger.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      290 2023-07-23 11:36:02.000000 SageLogger-1.3.1/SageLogger.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 11:36:01.000000 SageLogger-1.3.1/SageLogger.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       18 2023-07-23 11:36:01.000000 SageLogger-1.3.1/SageLogger.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       11 2023-07-23 11:36:01.000000 SageLogger-1.3.1/SageLogger.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      661 2023-07-23 11:33:55.000000 SageLogger-1.3.1/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-07-23 11:36:02.139053 SageLogger-1.3.1/setup.cfg
+-rw-rw-rw-   0        0        0     1069 2023-07-23 11:33:01.000000 SageLogger-1.3.1/setup.py
```

### Comparing `SageLogger-1.0/PKG-INFO` & `SageLogger-1.3.1/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: SageLogger
-Version: 1.0
+Version: 1.3.1
 Summary: Yet another python logger, or is it like any other?
 Home-page: https://github.com/PanSageYT/SageLogger
 Author: PanSageYT
 Author-email: PanSageYT <pansage@hugedick.fyi>
 Project-URL: Homepage, https://github.com/PanSageYT/SageLogger
 Project-URL: Bug Tracker, https://github.com/PanSageYT/SageLogger/issues
 Classifier: Programming Language :: Python :: 3
@@ -25,14 +25,15 @@
 1. DEFAULT: The default log type.
 2. POSITIVE: For positive events and actions.
 3. ONHOLD: To indicate events that are on hold or waiting for further action.
 4. NEGATIVE: For negative events or errors.
 5. FROZEN: To represent frozen states or events.
 6. INFORMATION: For general information logging.
 7. MILD_EXCEPTION: To log minor exceptions or errors.
+8. DEBUG: To troubleshoot some things. (disabled by default)
 
 ### Custom Local Log Types
 Apart from the predefined log types, you can create custom log types using the `SageLogger.DynamicType.fromChar` method or the `SageLogger.DynamicType.fromColoredChar` method for colored logs.
 
 ### Remote Logging
 SageLogger enables remote logging capabilities through the SageRemoteLogger class. You can load custom APIs for remote logging, and it also provides built-in support for Discord webhook integration.
 
@@ -84,9 +85,17 @@
 sagelogs.log("It's debug", type=sagelogs.Type.DEBUG)
 sagelogs.log("Sent to discord", type=sagelogs.Type.INFORMATION)
 sageremotelog.log("I sent to discord!")
 ```
 
 IntelliSense should show you around!
 
-Big issue:
-In logs it writes color codes.
+### Big issue:
+In log files it writes color codes.
+
+### Version numbers:
+<Major\>.<Minor\>.<Revision\>
+
+### Changelogs:
+v1.0 - Initial version
+v1.1/v1.2 - Skipped due to version naming fails :(
+v1.3 - Logger arrays in SageFactory and getLoggerByName(name), 3 more loggers (1 secret shh). More functions of enabling.
```

### Comparing `SageLogger-1.0/SageLogger/Logger.py` & `SageLogger-1.3.1/SageLogger/Logger.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 import colorama
 import datetime
 import requests
 from typing import Union
-from . import SageException, SageFactory
 from enum import Enum
 import os
+from . import SageException, SageFactory
 
 thislogger = None
 
 class DynamicType:
     @staticmethod
     def fromChar(logger, char) -> tuple[int, str, bool]:
         #if len(char) != 1:
@@ -27,47 +27,53 @@
 
 class xxPartType:
     name : str = ""
     Id : int = 0
     customization : str = ""
     value : tuple[int, str, bool] = (-2, "", False)
     enabled = False
-    def __init__(self, name, Id, customization, enabled) -> None:
+    lockedup = False
+    def __init__(self, name, Id, customization, enabled, lockedup : bool = False) -> None:
         self.name = name
         self.Id = Id
         self.customization = customization
         self.value = (self.Id, self.customization, self.enabled)
         self.enabled = enabled
+        self.lockedup = lockedup
 
 class xxType:
     DEFAULT : xxPartType = xxPartType("DEFAULT", -2, "", True)
     POSITIVE : xxPartType = xxPartType("POSITIVE", -2, "", True)
     ONHOLD : xxPartType = xxPartType("ONHOLD", -2, "", True)
     NEGATIVE : xxPartType = xxPartType("NEGATIVE", -2, "", True)
     FROZEN : xxPartType = xxPartType("FROZEN", -2, "", True)
     INFORMATION : xxPartType = xxPartType("INFORMATION", -2, "", True)
     MILD_EXCEPTION : xxPartType = xxPartType("MILD_EXCEPTION", -2, "", True)
     DEBUG : xxPartType = xxPartType("DEBUG", -2, "", False)
+    AMONGUS : xxPartType = xxPartType("AMONGUS", -2, "", True)
+    SAGE_LOGGER_DEBUG : xxPartType = xxPartType("SAGE_LOGGER_DEBUG", -2, "", False)
     def refresh(self, customization):
         self.DEFAULT = xxPartType("DEFAULT", 0, "", self.DEFAULT.enabled)
         self.POSITIVE = xxPartType("POSITIVE", 1, customization.setup_custom_border(colorama.Fore.GREEN + "+"), self.POSITIVE.enabled)
         self.ONHOLD = xxPartType("ONHOLD", 2, customization.setup_custom_border(colorama.Fore.YELLOW + "/"), self.ONHOLD.enabled)
         self.NEGATIVE = xxPartType("NEGATIVE", 3, customization.setup_custom_border(colorama.Fore.RED + "-"), self.NEGATIVE.enabled)
         self.FROZEN = xxPartType("FROZEN", 4, customization.setup_custom_border(colorama.Fore.LIGHTBLUE_EX + "#"), self.FROZEN.enabled)
         self.INFORMATION = xxPartType("INFORMATION", 5, customization.setup_custom_border(colorama.Fore.CYAN + "i"), self.INFORMATION.enabled)
         self.MILD_EXCEPTION = xxPartType("MILD_EXCEPTION", 6, customization.setup_custom_border(colorama.Fore.LIGHTRED_EX + "X"), self.MILD_EXCEPTION.enabled)
         self.DEBUG = xxPartType("DEBUG", 7, customization.setup_custom_border(colorama.Fore.LIGHTMAGENTA_EX + "*"), self.DEBUG.enabled)
+        self.AMONGUS = xxPartType("AMONGUS", 8, customization.setup_custom_border(colorama.Fore.RED + "ඞ"), self.AMONGUS.enabled)
+        self.SAGE_LOGGER_DEBUG = xxPartType("SAGE_LOGGER_DEBUG", 9, customization.setup_custom_border(colorama.Fore.LIGHTGREEN_EX + "S" + colorama.Fore.GREEN + "L" + colorama.Fore.LIGHTMAGENTA_EX + "D"), False, lockedup=True)
         
     def __iter__(self):
-        return [self.DEFAULT, self.POSITIVE, self.ONHOLD, self.NEGATIVE, self.FROZEN, self.INFORMATION, self.MILD_EXCEPTION, self.DEBUG]
+        return [self.DEFAULT, self.POSITIVE, self.ONHOLD, self.NEGATIVE, self.FROZEN, self.INFORMATION, self.MILD_EXCEPTION, self.DEBUG, self.AMONGUS, self.SAGE_LOGGER_DEBUG]
 
 class MildError:
     @staticmethod
     def throw(logger, name, args):
-        logger.log(f"Mild {name} - {args}, you don't need to catch it, but you may fix it ;)", type=SageLogger.Type.MILD_EXCEPTION)
+        logger.log(f"Mild {name} - {args}, you don't need to catch it, but you may fix it ;)", type=SageConsoleLogger.Type.MILD_EXCEPTION)
         
 class xxCustomization:
     bordcol = colorama.Fore.LIGHTBLACK_EX
     borders = "[]"
     logger = None
     
     def __init__(self, logger):
@@ -79,17 +85,17 @@
             MildError.throw(self.logger, "sagelogs.errors.TooLongChars", "Too much characters in border styling (max 2)")
         self.borders = borders
         self.logger.Type.refresh(self) # type: ignore
 
     def setup_custom_border(self, cos):
         return self.bordcol + self.borders[0] + colorama.Fore.RESET + cos + self.bordcol + self.borders[1] + " "
     
-class SageLogger:
+class SageConsoleLogger:
     customization : xxCustomization = None # type: ignore
-    DynamicType = DynamicType
+    DynamicType = DynamicType()
     
     name = ""
     logfile = ""
     savetofile = True
     Type = xxType()
     def __init__(self, name : str = "", savetofile : bool = False, logfile : str = "log"):
         global thislogger
@@ -100,23 +106,33 @@
         self.name = name
         self.logfile = logfile
         self.savetofile = savetofile
         if savetofile:
             with open(self.name + "." + self.logfile, "a") as wr:
                 wr.write(("-" * 16) + " " + datetime.datetime.now().strftime("%d/%m/%Y, %H:%M:%S") + " " + ("-" * 16) + "\n")
                 wr.close()
-                
+    
+    def is_enabled_type(self, type):
+        return type.enabled
+    
     def toggle_type(self, type):
+        if (type.lockedup):
+            yield SageException.UhOhSomeoneTooCurious()
         type.enabled = not type.enabled
         
     def enable_type(self, type):
+        if (type.lockedup):
+            yield SageException.UhOhSomeoneTooCurious()
         type.enabled = True
         
     def disable_type(self, type):
         type.enabled = False
+        
+    def unlock_type_not_recommended_please_leave_it_alone_it_will_spam(self, type):
+        type.lockedup = False
     
     def log(self, message : str, type : Union[tuple[int, str, bool], xxPartType] = Type.DEFAULT.value, color = colorama.Fore.RESET, id : int = -2137, date : bool = False, time : bool = False, datecolor : str = colorama.Fore.RESET, timecolor : str = colorama.Fore.RESET, showname : bool = True, ending : str = "\n"):
         typefinish = None
         if(isinstance(type, xxPartType)):
             typefinish = (type.Id, type.customization, type.enabled)
         else:
             typefinish = type
@@ -127,15 +143,15 @@
             t = self.customization.setup_custom_border(datetime.datetime.now().strftime((datecolor + "%d/%m/%Y" if date else "") + colorama.Fore.RESET + (", " if date and time else "") + (timecolor + "%H:%M:%S" if time else "")))
         x = t + (self.customization.setup_custom_border(str(id)) if id != -2137 else "") + typefinish[1] + color + message
         c = (self.customization.setup_custom_border(self.name) + " " if showname else "")
         x = c + x
         print(x, end=ending)
         if self.savetofile:
             with open(self.name + "." + self.logfile, "a") as wr:
-                wr.write(x + ending)
+                wr.write(x.replace("ඞ", "AMONGUS") + ending)
                 wr.close()
                 
     def ask(self, message : str, type : Union[tuple[int, str, bool], xxPartType] = Type.DEFAULT.value, color = colorama.Fore.RESET, answercolor = colorama.Fore.RESET, id : int = -2137, date : bool = False, time : bool = False, datecolor : str = colorama.Fore.RESET, timecolor : str = colorama.Fore.RESET):
         typefinish = None
         if(isinstance(type, xxPartType)):
             typefinish = (type.Id, type.customization, type.enabled)
         else:
@@ -143,23 +159,23 @@
         t = ""
         if date or time:
             t = self.customization.setup_custom_border(datetime.datetime.now().strftime((datecolor + "%d/%m/%Y" if date else "") + (", " if date and time else "") + (timecolor + "%H:%M:%S" if time else "")))
         x = t + (self.customization.setup_custom_border(str(id)) if id != -2137 else "") + typefinish[1] + color + message + answercolor
         ans = input(x)
         if self.savetofile:
             with open(self.name + "." + self.logfile, "a") as wr:
-                wr.write(x + ">" + ans + "\n")
+                wr.write(x.replace("ඞ", "AMONGUS") + ">" + ans + "\n")
                 wr.close()
 
 class RemoteWhereLog(Enum):
     NOWHERE = 0
     HEADERS = 1
     BODY = 2
 
-class SageRemoteLogger(SageLogger):
+class SageRemoteLogger(SageConsoleLogger):
     @staticmethod
     def search_for_placeholder(headers, body) -> RemoteWhereLog:
         for h in headers.keys():
             if len(headers[h].split("%LOG%")) != 1:
                 return RemoteWhereLog.HEADERS
         for h in body.keys():
             if len(body[h].split("%LOG%")) != 1:
@@ -189,37 +205,41 @@
     body = {}
     remote = RemoteWhereLog.NOWHERE
     
     name = ""
     logfile = ""
     savetofile = ""
     def __init__(self, method, url, headers, body, name: str = "", savetofile: bool = False, logfile: str = "log"):
+        SageFactory.errorlogger.log("Initializing remote logger...", type=SageConsoleLogger.Type.SAGE_LOGGER_DEBUG)
         global thislogger
         if thislogger is None:
             thislogger = self
         self.name = "remote" + ("-" if name != "" else "") + name
         self.logfile = logfile
         self.savetofile = savetofile
         self.url = url
         self.method = method
         self.headers = headers
         self.body = body
+        SageFactory.errorlogger.log("Searching for placeholder %LOG%", type=SageConsoleLogger.Type.SAGE_LOGGER_DEBUG)
         self.remote = SageRemoteLogger.search_for_placeholder(headers, body)
         if self.remote == RemoteWhereLog.NOWHERE:
             raise SageException.NoLogPlaceholder("Remember to somewhere put %LOG%, maybe in the body?")
 
         if savetofile:
             with open(self.name + "." + self.logfile, "a") as wr:
                 wr.write(("-" * 16) + " " + datetime.datetime.now().strftime("%d/%m/%Y, %H:%M:%S") + " " + ("-" * 16) + "\n")
                 wr.close()
     
     def log(self, message : str, print_on_console : bool = False, ending : str = "\n"):
         if print_on_console:
             print(message, end=ending)
+        
         a = requests.request(self.method, self.url, json=SageRemoteLogger.replace_placeholder(message, RemoteWhereLog.BODY, self.remote, self.headers, self.body), headers=SageRemoteLogger.replace_placeholder(message, RemoteWhereLog.HEADERS, self.remote, self.headers, self.body))
+        SageFactory.errorlogger.log(a.text + " - " + str(a.status_code), type=SageConsoleLogger.Type.SAGE_LOGGER_DEBUG)
         if self.savetofile:
             with open(self.name + "." + self.logfile, "a") as wr:
                 wr.write("(" + str(a.status_code) + ") " + message + ending)
                 wr.write(a.text + ending)
                 wr.close()
                 
     def ask(self, its_unsupported_sadly):
@@ -234,8 +254,8 @@
             return SageRemoteLogger("POST", url, {"Content-Type": "application/json"},
                                     {
                                         "content": "%LOG%",
                                         "username": f"Sage Logger - {os.getcwd().split(esc)[-1]}"
                                     }, name, savetofile, logfile)
         else:
             MildError.throw(SageFactory.create_temporary(), "NotDiscordWebhook", "This url isn't a discord webhook, maybe try SageFactory.create_remote method")
-            return SageRemoteLogger("", "", {}, {})
+            return SageRemoteLogger("", "", {"log":"%LOG%"}, {})
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `SageLogger-1.0/SageLogger.egg-info/PKG-INFO` & `SageLogger-1.3.1/SageLogger.egg-info/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: SageLogger
-Version: 1.0
+Version: 1.3.1
 Summary: Yet another python logger, or is it like any other?
 Home-page: https://github.com/PanSageYT/SageLogger
 Author: PanSageYT
 Author-email: PanSageYT <pansage@hugedick.fyi>
 Project-URL: Homepage, https://github.com/PanSageYT/SageLogger
 Project-URL: Bug Tracker, https://github.com/PanSageYT/SageLogger/issues
 Classifier: Programming Language :: Python :: 3
@@ -25,14 +25,15 @@
 1. DEFAULT: The default log type.
 2. POSITIVE: For positive events and actions.
 3. ONHOLD: To indicate events that are on hold or waiting for further action.
 4. NEGATIVE: For negative events or errors.
 5. FROZEN: To represent frozen states or events.
 6. INFORMATION: For general information logging.
 7. MILD_EXCEPTION: To log minor exceptions or errors.
+8. DEBUG: To troubleshoot some things. (disabled by default)
 
 ### Custom Local Log Types
 Apart from the predefined log types, you can create custom log types using the `SageLogger.DynamicType.fromChar` method or the `SageLogger.DynamicType.fromColoredChar` method for colored logs.
 
 ### Remote Logging
 SageLogger enables remote logging capabilities through the SageRemoteLogger class. You can load custom APIs for remote logging, and it also provides built-in support for Discord webhook integration.
 
@@ -84,9 +85,17 @@
 sagelogs.log("It's debug", type=sagelogs.Type.DEBUG)
 sagelogs.log("Sent to discord", type=sagelogs.Type.INFORMATION)
 sageremotelog.log("I sent to discord!")
 ```
 
 IntelliSense should show you around!
 
-Big issue:
-In logs it writes color codes.
+### Big issue:
+In log files it writes color codes.
+
+### Version numbers:
+<Major\>.<Minor\>.<Revision\>
+
+### Changelogs:
+v1.0 - Initial version
+v1.1/v1.2 - Skipped due to version naming fails :(
+v1.3 - Logger arrays in SageFactory and getLoggerByName(name), 3 more loggers (1 secret shh). More functions of enabling.
```

### Comparing `SageLogger-1.0/pyproject.toml` & `SageLogger-1.3.1/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["hatchling"]
 build-backend = "hatchling.build"
 
 [project]
 name = "SageLogger"
-version = "1.0"
+version = "1.3.1"
 authors = [
   { name="PanSageYT", email="pansage@hugedick.fyi" },
 ]
 description = "Yet another python logger, or is it like any other?"
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = [
```

### Comparing `SageLogger-1.0/setup.py` & `SageLogger-1.3.1/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 # Dane projektu
 project_name = "SageLogger"
-project_version = "1.0"
+project_version = "1.3.1"
 project_description = "Yet another python logger, or is it like any other?"
 project_author = "PanSageYT"
 project_author_email = "pansage@hugedick.fyi"
 
 # Zależności
 dependencies = [
     "colorama",
```

