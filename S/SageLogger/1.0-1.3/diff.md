# Comparing `tmp/SageLogger-1.0.tar.gz` & `tmp/SageLogger-1.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "SageLogger-1.0.tar", last modified: Sat Jul 22 21:58:50 2023, max compression
+gzip compressed data, was "SageLogger-1.3.tar", last modified: Sun Jul 23 12:32:53 2023, max compression
```

## Comparing `SageLogger-1.0.tar` & `SageLogger-1.3.tar`

### file list

```diff
@@ -1,16 +1,17 @@
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
+drwxrwxrwx   0        0        0        0 2023-07-23 12:32:53.521956 SageLogger-1.3/
+-rw-rw-rw-   0        0        0    14198 2023-07-23 12:32:53.520922 SageLogger-1.3/PKG-INFO
+-rw-rw-rw-   0        0        0    13606 2023-07-23 12:32:42.000000 SageLogger-1.3/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 12:32:53.510509 SageLogger-1.3/SageLogger/
+-rw-rw-rw-   0        0        0    13884 2023-07-23 12:09:10.000000 SageLogger-1.3/SageLogger/Logger.py
+-rw-rw-rw-   0        0        0     1093 2023-07-23 12:11:42.000000 SageLogger-1.3/SageLogger/SageException.py
+-rw-rw-rw-   0        0        0     3143 2023-07-23 12:31:15.000000 SageLogger-1.3/SageLogger/SageFactory.py
+-rw-rw-rw-   0        0        0       15 2023-07-22 20:32:47.000000 SageLogger-1.3/SageLogger/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 12:32:53.518766 SageLogger-1.3/SageLogger.egg-info/
+-rw-rw-rw-   0        0        0    14198 2023-07-23 12:32:53.000000 SageLogger-1.3/SageLogger.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      300 2023-07-23 12:32:53.000000 SageLogger-1.3/SageLogger.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 12:32:53.000000 SageLogger-1.3/SageLogger.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       18 2023-07-23 12:32:53.000000 SageLogger-1.3/SageLogger.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       11 2023-07-23 12:32:53.000000 SageLogger-1.3/SageLogger.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      659 2023-07-23 12:31:39.000000 SageLogger-1.3/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-07-23 12:32:53.522476 SageLogger-1.3/setup.cfg
+-rw-rw-rw-   0        0        0     1069 2023-07-23 12:12:29.000000 SageLogger-1.3/setup.py
```

### Comparing `SageLogger-1.0/SageLogger/Logger.py` & `SageLogger-1.3/SageLogger/Logger.py`

 * *Files 14% similar despite different names*

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
@@ -27,47 +27,77 @@
 
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
+    SAGE_LOGGER_DEBUG : xxPartType = xxPartType("SAGE_LOGGER_DEBUG", -2, "", True)
     def refresh(self, customization):
         self.DEFAULT = xxPartType("DEFAULT", 0, "", self.DEFAULT.enabled)
         self.POSITIVE = xxPartType("POSITIVE", 1, customization.setup_custom_border(colorama.Fore.GREEN + "+"), self.POSITIVE.enabled)
         self.ONHOLD = xxPartType("ONHOLD", 2, customization.setup_custom_border(colorama.Fore.YELLOW + "/"), self.ONHOLD.enabled)
         self.NEGATIVE = xxPartType("NEGATIVE", 3, customization.setup_custom_border(colorama.Fore.RED + "-"), self.NEGATIVE.enabled)
         self.FROZEN = xxPartType("FROZEN", 4, customization.setup_custom_border(colorama.Fore.LIGHTBLUE_EX + "#"), self.FROZEN.enabled)
         self.INFORMATION = xxPartType("INFORMATION", 5, customization.setup_custom_border(colorama.Fore.CYAN + "i"), self.INFORMATION.enabled)
         self.MILD_EXCEPTION = xxPartType("MILD_EXCEPTION", 6, customization.setup_custom_border(colorama.Fore.LIGHTRED_EX + "X"), self.MILD_EXCEPTION.enabled)
         self.DEBUG = xxPartType("DEBUG", 7, customization.setup_custom_border(colorama.Fore.LIGHTMAGENTA_EX + "*"), self.DEBUG.enabled)
-        
+        self.AMONGUS = xxPartType("AMONGUS", 8, customization.setup_custom_border(colorama.Fore.RED + "ඞ"), self.AMONGUS.enabled)
+        self.SAGE_LOGGER_DEBUG = xxPartType("SAGE_LOGGER_DEBUG", 9, customization.setup_custom_border(colorama.Fore.LIGHTGREEN_EX + "S" + colorama.Fore.GREEN + "L" + colorama.Fore.LIGHTMAGENTA_EX + "D"), self.SAGE_LOGGER_DEBUG.enabled and not self.SAGE_LOGGER_DEBUG.lockedup)
+    
+    def loggers_in_array(self):
+        return [self.DEFAULT, self.POSITIVE, self.ONHOLD, self.NEGATIVE, self.FROZEN, self.INFORMATION, self.MILD_EXCEPTION, self.DEBUG, self.AMONGUS, self.SAGE_LOGGER_DEBUG]
+    
     def __iter__(self):
-        return [self.DEFAULT, self.POSITIVE, self.ONHOLD, self.NEGATIVE, self.FROZEN, self.INFORMATION, self.MILD_EXCEPTION, self.DEBUG]
-
+        return self.loggers_in_array()
+    
+    def is_enabled_type(self, type):
+        return self.loggers_in_array()[type.Id].enabled
+    
+    def toggle_type(self, type):
+        if (type.lockedup):
+            yield SageException.UhOhSomeoneTooCurious()
+        self.loggers_in_array()[type.Id].enabled = not self.loggers_in_array()[type.Id].enabled
+        
+    def enable_type(self, type):
+        if (self.loggers_in_array()[type.Id].lockedup):
+            yield SageException.UhOhSomeoneTooCurious()
+        self.loggers_in_array()[type.Id].enabled = True
+        
+    def disable_type(self, type):
+        self.loggers_in_array()[type.Id].enabled = False
+        
+    def unlock_type_not_recommended_please_leave_it_alone_it_will_spam(self, type):
+        customization = xxCustomization(None)
+        customization.bordcol = colorama.Back.RED + colorama.Fore.WHITE
+        SageFactory.create(name="SageLoggerImportant").log("Unlocked, it isn't recommended, remember. This message cannot be turned off." + colorama.Back.RESET, type=xxPartType("IMPORTANT_HARD_CODED", 1, customization.setup_custom_border(colorama.Fore.LIGHTRED_EX + "!"), True))
+        self.loggers_in_array()[type.Id].lockedup = False
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
@@ -79,17 +109,17 @@
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
@@ -100,23 +130,14 @@
         self.name = name
         self.logfile = logfile
         self.savetofile = savetofile
         if savetofile:
             with open(self.name + "." + self.logfile, "a") as wr:
                 wr.write(("-" * 16) + " " + datetime.datetime.now().strftime("%d/%m/%Y, %H:%M:%S") + " " + ("-" * 16) + "\n")
                 wr.close()
-                
-    def toggle_type(self, type):
-        type.enabled = not type.enabled
-        
-    def enable_type(self, type):
-        type.enabled = True
-        
-    def disable_type(self, type):
-        type.enabled = False
     
     def log(self, message : str, type : Union[tuple[int, str, bool], xxPartType] = Type.DEFAULT.value, color = colorama.Fore.RESET, id : int = -2137, date : bool = False, time : bool = False, datecolor : str = colorama.Fore.RESET, timecolor : str = colorama.Fore.RESET, showname : bool = True, ending : str = "\n"):
         typefinish = None
         if(isinstance(type, xxPartType)):
             typefinish = (type.Id, type.customization, type.enabled)
         else:
             typefinish = type
@@ -127,15 +148,15 @@
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
@@ -143,23 +164,23 @@
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
@@ -189,37 +210,41 @@
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
@@ -234,8 +259,8 @@
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

### Comparing `SageLogger-1.0/pyproject.toml` & `SageLogger-1.3/pyproject.toml`

 * *Files 20% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["hatchling"]
 build-backend = "hatchling.build"
 
 [project]
 name = "SageLogger"
-version = "1.0"
+version = "1.3"
 authors = [
   { name="PanSageYT", email="pansage@hugedick.fyi" },
 ]
 description = "Yet another python logger, or is it like any other?"
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = [
```

### Comparing `SageLogger-1.0/setup.py` & `SageLogger-1.3/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 # Dane projektu
 project_name = "SageLogger"
-project_version = "1.0"
+project_version = "1.3.9"
 project_description = "Yet another python logger, or is it like any other?"
 project_author = "PanSageYT"
 project_author_email = "pansage@hugedick.fyi"
 
 # Zależności
 dependencies = [
     "colorama",
```

