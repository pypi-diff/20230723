# Comparing `tmp/terminal_manager-0.8.6.tar.gz` & `tmp/terminal_manager-0.8.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "terminal_manager-0.8.6.tar", last modified: Sat Jul 22 10:02:04 2023, max compression
+gzip compressed data, was "terminal_manager-0.8.7.tar", last modified: Sun Jul 23 02:49:54 2023, max compression
```

## Comparing `terminal_manager-0.8.6.tar` & `terminal_manager-0.8.7.tar`

### file list

```diff
@@ -1,28 +1,28 @@
-drwxrwxr-x   0 adrian    (1000) adrian    (1000)        0 2023-07-22 10:02:04.523716 terminal_manager-0.8.6/
--rw-rw-r--   0 adrian    (1000) adrian    (1000)     1063 2023-07-11 04:42:30.000000 terminal_manager-0.8.6/LICENSE
--rw-rw-r--   0 adrian    (1000) adrian    (1000)      681 2023-07-22 10:02:04.523716 terminal_manager-0.8.6/PKG-INFO
--rw-rw-r--   0 adrian    (1000) adrian    (1000)      107 2023-07-11 04:42:30.000000 terminal_manager-0.8.6/README.md
--rw-rw-r--   0 adrian    (1000) adrian    (1000)      706 2023-07-22 09:59:03.000000 terminal_manager-0.8.6/pyproject.toml
--rw-rw-r--   0 adrian    (1000) adrian    (1000)       38 2023-07-22 10:02:04.523716 terminal_manager-0.8.6/setup.cfg
-drwxrwxr-x   0 adrian    (1000) adrian    (1000)        0 2023-07-22 10:02:04.515716 terminal_manager-0.8.6/src/
-drwxrwxr-x   0 adrian    (1000) adrian    (1000)        0 2023-07-22 10:02:04.519716 terminal_manager-0.8.6/src/terminal_manager/
--rw-r--r--   0 adrian    (1000) adrian    (1000)     7023 2023-07-22 09:12:06.000000 terminal_manager-0.8.6/src/terminal_manager/__init__.py
--rw-r--r--   0 adrian    (1000) adrian    (1000)     3352 2023-07-22 09:12:06.000000 terminal_manager-0.8.6/src/terminal_manager/collection.py
--rw-r--r--   0 adrian    (1000) adrian    (1000)     6319 2023-07-22 09:12:06.000000 terminal_manager-0.8.6/src/terminal_manager/command.py
-drwxrwxr-x   0 adrian    (1000) adrian    (1000)        0 2023-07-22 10:02:04.523716 terminal_manager-0.8.6/src/terminal_manager/default_collections/
--rw-r--r--   0 adrian    (1000) adrian    (1000)      161 2023-07-22 09:12:06.000000 terminal_manager-0.8.6/src/terminal_manager/default_collections/__init__.py
--rw-r--r--   0 adrian    (1000) adrian    (1000)     1084 2023-07-22 09:12:06.000000 terminal_manager-0.8.6/src/terminal_manager/default_collections/const.py
--rw-r--r--   0 adrian    (1000) adrian    (1000)     4371 2023-07-22 09:12:06.000000 terminal_manager-0.8.6/src/terminal_manager/default_collections/linux.py
--rw-r--r--   0 adrian    (1000) adrian    (1000)     5206 2023-07-22 09:12:06.000000 terminal_manager-0.8.6/src/terminal_manager/default_collections/windows_cmd.py
--rw-r--r--   0 adrian    (1000) adrian    (1000)     5368 2023-07-22 09:12:06.000000 terminal_manager-0.8.6/src/terminal_manager/default_collections/windows_ps.py
--rw-r--r--   0 adrian    (1000) adrian    (1000)       94 2023-07-22 09:12:06.000000 terminal_manager-0.8.6/src/terminal_manager/errors.py
--rw-r--r--   0 adrian    (1000) adrian    (1000)      617 2023-07-22 09:12:06.000000 terminal_manager-0.8.6/src/terminal_manager/event.py
--rw-r--r--   0 adrian    (1000) adrian    (1000)      222 2023-07-22 09:12:06.000000 terminal_manager-0.8.6/src/terminal_manager/helpers.py
--rw-r--r--   0 adrian    (1000) adrian    (1000)     8379 2023-07-22 09:12:06.000000 terminal_manager-0.8.6/src/terminal_manager/sensor.py
--rw-r--r--   0 adrian    (1000) adrian    (1000)     1248 2023-07-22 09:12:06.000000 terminal_manager-0.8.6/src/terminal_manager/synchronizer.py
-drwxrwxr-x   0 adrian    (1000) adrian    (1000)        0 2023-07-22 10:02:04.523716 terminal_manager-0.8.6/src/terminal_manager.egg-info/
--rw-rw-r--   0 adrian    (1000) adrian    (1000)      681 2023-07-22 10:02:04.000000 terminal_manager-0.8.6/src/terminal_manager.egg-info/PKG-INFO
--rw-rw-r--   0 adrian    (1000) adrian    (1000)      776 2023-07-22 10:02:04.000000 terminal_manager-0.8.6/src/terminal_manager.egg-info/SOURCES.txt
--rw-rw-r--   0 adrian    (1000) adrian    (1000)        1 2023-07-22 10:02:04.000000 terminal_manager-0.8.6/src/terminal_manager.egg-info/dependency_links.txt
--rw-rw-r--   0 adrian    (1000) adrian    (1000)       22 2023-07-22 10:02:04.000000 terminal_manager-0.8.6/src/terminal_manager.egg-info/requires.txt
--rw-rw-r--   0 adrian    (1000) adrian    (1000)       17 2023-07-22 10:02:04.000000 terminal_manager-0.8.6/src/terminal_manager.egg-info/top_level.txt
+drwxrwxr-x   0 adrian    (1000) adrian    (1000)        0 2023-07-23 02:49:54.397739 terminal_manager-0.8.7/
+-rw-rw-r--   0 adrian    (1000) adrian    (1000)     1063 2023-07-11 04:42:30.000000 terminal_manager-0.8.7/LICENSE
+-rw-rw-r--   0 adrian    (1000) adrian    (1000)      681 2023-07-23 02:49:54.397739 terminal_manager-0.8.7/PKG-INFO
+-rw-rw-r--   0 adrian    (1000) adrian    (1000)      107 2023-07-11 04:42:30.000000 terminal_manager-0.8.7/README.md
+-rw-rw-r--   0 adrian    (1000) adrian    (1000)      706 2023-07-23 02:47:40.000000 terminal_manager-0.8.7/pyproject.toml
+-rw-rw-r--   0 adrian    (1000) adrian    (1000)       38 2023-07-23 02:49:54.397739 terminal_manager-0.8.7/setup.cfg
+drwxrwxr-x   0 adrian    (1000) adrian    (1000)        0 2023-07-23 02:49:54.389739 terminal_manager-0.8.7/src/
+drwxrwxr-x   0 adrian    (1000) adrian    (1000)        0 2023-07-23 02:49:54.393739 terminal_manager-0.8.7/src/terminal_manager/
+-rw-r--r--   0 adrian    (1000) adrian    (1000)     7023 2023-07-22 10:32:33.000000 terminal_manager-0.8.7/src/terminal_manager/__init__.py
+-rw-r--r--   0 adrian    (1000) adrian    (1000)     3352 2023-07-22 10:32:33.000000 terminal_manager-0.8.7/src/terminal_manager/collection.py
+-rw-r--r--   0 adrian    (1000) adrian    (1000)     6319 2023-07-23 02:34:53.000000 terminal_manager-0.8.7/src/terminal_manager/command.py
+drwxrwxr-x   0 adrian    (1000) adrian    (1000)        0 2023-07-23 02:49:54.397739 terminal_manager-0.8.7/src/terminal_manager/default_collections/
+-rw-r--r--   0 adrian    (1000) adrian    (1000)      161 2023-07-22 10:32:33.000000 terminal_manager-0.8.7/src/terminal_manager/default_collections/__init__.py
+-rw-r--r--   0 adrian    (1000) adrian    (1000)     1084 2023-07-22 10:32:33.000000 terminal_manager-0.8.7/src/terminal_manager/default_collections/const.py
+-rw-r--r--   0 adrian    (1000) adrian    (1000)     4371 2023-07-23 02:33:51.000000 terminal_manager-0.8.7/src/terminal_manager/default_collections/linux.py
+-rw-r--r--   0 adrian    (1000) adrian    (1000)     5206 2023-07-22 10:32:33.000000 terminal_manager-0.8.7/src/terminal_manager/default_collections/windows_cmd.py
+-rw-r--r--   0 adrian    (1000) adrian    (1000)     5368 2023-07-23 02:34:08.000000 terminal_manager-0.8.7/src/terminal_manager/default_collections/windows_ps.py
+-rw-r--r--   0 adrian    (1000) adrian    (1000)       94 2023-07-22 10:32:33.000000 terminal_manager-0.8.7/src/terminal_manager/errors.py
+-rw-r--r--   0 adrian    (1000) adrian    (1000)      617 2023-07-22 10:32:33.000000 terminal_manager-0.8.7/src/terminal_manager/event.py
+-rw-r--r--   0 adrian    (1000) adrian    (1000)      222 2023-07-22 10:32:33.000000 terminal_manager-0.8.7/src/terminal_manager/helpers.py
+-rw-r--r--   0 adrian    (1000) adrian    (1000)     8379 2023-07-22 10:32:33.000000 terminal_manager-0.8.7/src/terminal_manager/sensor.py
+-rw-r--r--   0 adrian    (1000) adrian    (1000)     1248 2023-07-22 10:32:33.000000 terminal_manager-0.8.7/src/terminal_manager/synchronizer.py
+drwxrwxr-x   0 adrian    (1000) adrian    (1000)        0 2023-07-23 02:49:54.397739 terminal_manager-0.8.7/src/terminal_manager.egg-info/
+-rw-rw-r--   0 adrian    (1000) adrian    (1000)      681 2023-07-23 02:49:54.000000 terminal_manager-0.8.7/src/terminal_manager.egg-info/PKG-INFO
+-rw-rw-r--   0 adrian    (1000) adrian    (1000)      776 2023-07-23 02:49:54.000000 terminal_manager-0.8.7/src/terminal_manager.egg-info/SOURCES.txt
+-rw-rw-r--   0 adrian    (1000) adrian    (1000)        1 2023-07-23 02:49:54.000000 terminal_manager-0.8.7/src/terminal_manager.egg-info/dependency_links.txt
+-rw-rw-r--   0 adrian    (1000) adrian    (1000)       22 2023-07-23 02:49:54.000000 terminal_manager-0.8.7/src/terminal_manager.egg-info/requires.txt
+-rw-rw-r--   0 adrian    (1000) adrian    (1000)       17 2023-07-23 02:49:54.000000 terminal_manager-0.8.7/src/terminal_manager.egg-info/top_level.txt
```

### Comparing `terminal_manager-0.8.6/LICENSE` & `terminal_manager-0.8.7/LICENSE`

 * *Files identical despite different names*

### Comparing `terminal_manager-0.8.6/PKG-INFO` & `terminal_manager-0.8.7/PKG-INFO`

 * *Files 15% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: terminal_manager
-Version: 0.8.6
+Version: 0.8.7
 Summary: Use terminal commands to control and monitor devices
 Author-email: zhbjsh <zhbjsh@outlook.com>
 Project-URL: Homepage, https://github.com/zhbjsh/terminal-manager
 Project-URL: Bug Tracker, https://github.com/zhbjsh/terminal-manager/issues
 Keywords: terminal,command line
 Classifier: Programming Language :: Python :: 3.10
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `terminal_manager-0.8.6/pyproject.toml` & `terminal_manager-0.8.7/pyproject.toml`

 * *Files 18% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "terminal_manager"
-version = "0.8.6"
+version = "0.8.7"
 authors = [
   { name="zhbjsh", email="zhbjsh@outlook.com" },
 ]
 description = "Use terminal commands to control and monitor devices"
 readme = "README.md"
 requires-python = ">=3.10"
 classifiers = [
```

### Comparing `terminal_manager-0.8.6/src/terminal_manager/__init__.py` & `terminal_manager-0.8.7/src/terminal_manager/__init__.py`

 * *Files identical despite different names*

### Comparing `terminal_manager-0.8.6/src/terminal_manager/collection.py` & `terminal_manager-0.8.7/src/terminal_manager/collection.py`

 * *Files identical despite different names*

### Comparing `terminal_manager-0.8.6/src/terminal_manager/command.py` & `terminal_manager-0.8.7/src/terminal_manager/command.py`

 * *Files 0% similar despite different names*

```diff
@@ -10,15 +10,15 @@
 from .errors import CommandError
 from .helpers import name_to_key
 from .sensor import Sensor
 
 if TYPE_CHECKING:
     from . import CommandOutput, Manager
 
-SENSOR_DELIMITER = "#"
+SENSOR_DELIMITER = "&"
 VARIABLE_DELIMITER = "@"
 PLACEHOLDER_KEY = "_"
 
 
 # Not needed anymore after python 3.11
 class Template(Template):
     def get_identifiers(self):
```

### Comparing `terminal_manager-0.8.6/src/terminal_manager/default_collections/const.py` & `terminal_manager-0.8.7/src/terminal_manager/default_collections/const.py`

 * *Files identical despite different names*

### Comparing `terminal_manager-0.8.6/src/terminal_manager/default_collections/linux.py` & `terminal_manager-0.8.7/src/terminal_manager/default_collections/linux.py`

 * *Files 0% similar despite different names*

```diff
@@ -25,24 +25,24 @@
                 TextSensor(
                     SensorName.NETWORK_INTERFACE,
                     SensorKey.NETWORK_INTERFACE,
                 )
             ],
         ),
         SensorCommand(
-            "cat /sys/class/net/#{network_interface}/address",
+            "cat /sys/class/net/&{network_interface}/address",
             sensors=[
                 TextSensor(
                     SensorName.MAC_ADDRESS,
                     SensorKey.MAC_ADDRESS,
                 )
             ],
         ),
         SensorCommand(
-            "cat /sys/class/net/#{network_interface}/device/power/wakeup 2>/dev/null",
+            "cat /sys/class/net/&{network_interface}/device/power/wakeup 2>/dev/null",
             sensors=[
                 BinarySensor(
                     SensorName.WAKE_ON_LAN,
                     SensorKey.WAKE_ON_LAN,
                 )
             ],
         ),
```

### Comparing `terminal_manager-0.8.6/src/terminal_manager/default_collections/windows_cmd.py` & `terminal_manager-0.8.7/src/terminal_manager/default_collections/windows_cmd.py`

 * *Files identical despite different names*

### Comparing `terminal_manager-0.8.6/src/terminal_manager/default_collections/windows_ps.py` & `terminal_manager-0.8.7/src/terminal_manager/default_collections/windows_ps.py`

 * *Files 2% similar despite different names*

```diff
@@ -16,15 +16,15 @@
             ActionName.RESTART,
             ActionKey.RESTART,
         ),
     ],
     [
         SensorCommand(
             "$x = Get-NetAdapterPowerManagement "
-            + '-Name "#{network_interface}" | '
+            + '-Name "&{network_interface}" | '
             + "Select WakeOnMagicPacket; "
             + "$x.WakeOnMagicPacket",
             sensors=[
                 BinarySensor(
                     SensorName.WAKE_ON_LAN,
                     SensorKey.WAKE_ON_LAN,
                 )
```

### Comparing `terminal_manager-0.8.6/src/terminal_manager/event.py` & `terminal_manager-0.8.7/src/terminal_manager/event.py`

 * *Files identical despite different names*

### Comparing `terminal_manager-0.8.6/src/terminal_manager/sensor.py` & `terminal_manager-0.8.7/src/terminal_manager/sensor.py`

 * *Files identical despite different names*

### Comparing `terminal_manager-0.8.6/src/terminal_manager/synchronizer.py` & `terminal_manager-0.8.7/src/terminal_manager/synchronizer.py`

 * *Files identical despite different names*

### Comparing `terminal_manager-0.8.6/src/terminal_manager.egg-info/PKG-INFO` & `terminal_manager-0.8.7/src/terminal_manager.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: terminal-manager
-Version: 0.8.6
+Version: 0.8.7
 Summary: Use terminal commands to control and monitor devices
 Author-email: zhbjsh <zhbjsh@outlook.com>
 Project-URL: Homepage, https://github.com/zhbjsh/terminal-manager
 Project-URL: Bug Tracker, https://github.com/zhbjsh/terminal-manager/issues
 Keywords: terminal,command line
 Classifier: Programming Language :: Python :: 3.10
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `terminal_manager-0.8.6/src/terminal_manager.egg-info/SOURCES.txt` & `terminal_manager-0.8.7/src/terminal_manager.egg-info/SOURCES.txt`

 * *Files identical despite different names*

