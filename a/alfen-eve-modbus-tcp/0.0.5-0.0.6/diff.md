# Comparing `tmp/alfen_eve_modbus_tcp-0.0.5.tar.gz` & `tmp/alfen_eve_modbus_tcp-0.0.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "alfen_eve_modbus_tcp-0.0.5.tar", last modified: Fri Jul 21 21:03:37 2023, max compression
+gzip compressed data, was "alfen_eve_modbus_tcp-0.0.6.tar", last modified: Sun Jul 23 13:18:43 2023, max compression
```

## Comparing `alfen_eve_modbus_tcp-0.0.5.tar` & `alfen_eve_modbus_tcp-0.0.6.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxrwxr-x   0 luc       (1000) luc       (1000)        0 2023-07-21 21:03:37.978254 alfen_eve_modbus_tcp-0.0.5/
--rw-rw-r--   0 luc       (1000) luc       (1000)     1063 2023-07-14 13:22:32.000000 alfen_eve_modbus_tcp-0.0.5/LICENSE
--rw-rw-r--   0 luc       (1000) luc       (1000)    12403 2023-07-21 21:03:37.978254 alfen_eve_modbus_tcp-0.0.5/PKG-INFO
--rw-rw-r--   0 luc       (1000) luc       (1000)    11717 2023-07-16 19:44:24.000000 alfen_eve_modbus_tcp-0.0.5/README.md
--rw-rw-r--   0 luc       (1000) luc       (1000)      861 2023-07-21 21:03:37.978254 alfen_eve_modbus_tcp-0.0.5/setup.cfg
--rwxrwxr-x   0 luc       (1000) luc       (1000)       38 2023-07-14 13:22:32.000000 alfen_eve_modbus_tcp-0.0.5/setup.py
-drwxrwxr-x   0 luc       (1000) luc       (1000)        0 2023-07-21 21:03:37.978254 alfen_eve_modbus_tcp-0.0.5/src/
-drwxrwxr-x   0 luc       (1000) luc       (1000)        0 2023-07-21 21:03:37.978254 alfen_eve_modbus_tcp-0.0.5/src/alfen_eve_modbus_tcp/
--rw-rw-r--   0 luc       (1000) luc       (1000)    24155 2023-07-21 20:57:35.000000 alfen_eve_modbus_tcp-0.0.5/src/alfen_eve_modbus_tcp/__init__.py
-drwxrwxr-x   0 luc       (1000) luc       (1000)        0 2023-07-21 21:03:37.978254 alfen_eve_modbus_tcp-0.0.5/src/alfen_eve_modbus_tcp.egg-info/
--rw-rw-r--   0 luc       (1000) luc       (1000)    12403 2023-07-21 21:03:37.000000 alfen_eve_modbus_tcp-0.0.5/src/alfen_eve_modbus_tcp.egg-info/PKG-INFO
--rw-rw-r--   0 luc       (1000) luc       (1000)      312 2023-07-21 21:03:37.000000 alfen_eve_modbus_tcp-0.0.5/src/alfen_eve_modbus_tcp.egg-info/SOURCES.txt
--rw-rw-r--   0 luc       (1000) luc       (1000)        1 2023-07-21 21:03:37.000000 alfen_eve_modbus_tcp-0.0.5/src/alfen_eve_modbus_tcp.egg-info/dependency_links.txt
--rw-rw-r--   0 luc       (1000) luc       (1000)       40 2023-07-21 21:03:37.000000 alfen_eve_modbus_tcp-0.0.5/src/alfen_eve_modbus_tcp.egg-info/requires.txt
--rw-rw-r--   0 luc       (1000) luc       (1000)       21 2023-07-21 21:03:37.000000 alfen_eve_modbus_tcp-0.0.5/src/alfen_eve_modbus_tcp.egg-info/top_level.txt
+drwxrwxr-x   0 luc       (1000) luc       (1000)        0 2023-07-23 13:18:43.593149 alfen_eve_modbus_tcp-0.0.6/
+-rw-rw-r--   0 luc       (1000) luc       (1000)     1063 2023-07-14 13:22:32.000000 alfen_eve_modbus_tcp-0.0.6/LICENSE
+-rw-rw-r--   0 luc       (1000) luc       (1000)    12403 2023-07-23 13:18:43.593149 alfen_eve_modbus_tcp-0.0.6/PKG-INFO
+-rw-rw-r--   0 luc       (1000) luc       (1000)    11717 2023-07-16 19:44:24.000000 alfen_eve_modbus_tcp-0.0.6/README.md
+-rw-rw-r--   0 luc       (1000) luc       (1000)      861 2023-07-23 13:18:43.593149 alfen_eve_modbus_tcp-0.0.6/setup.cfg
+-rwxrwxr-x   0 luc       (1000) luc       (1000)       38 2023-07-14 13:22:32.000000 alfen_eve_modbus_tcp-0.0.6/setup.py
+drwxrwxr-x   0 luc       (1000) luc       (1000)        0 2023-07-23 13:18:43.589149 alfen_eve_modbus_tcp-0.0.6/src/
+drwxrwxr-x   0 luc       (1000) luc       (1000)        0 2023-07-23 13:18:43.593149 alfen_eve_modbus_tcp-0.0.6/src/alfen_eve_modbus_tcp/
+-rw-rw-r--   0 luc       (1000) luc       (1000)    24382 2023-07-23 13:12:31.000000 alfen_eve_modbus_tcp-0.0.6/src/alfen_eve_modbus_tcp/__init__.py
+drwxrwxr-x   0 luc       (1000) luc       (1000)        0 2023-07-23 13:18:43.593149 alfen_eve_modbus_tcp-0.0.6/src/alfen_eve_modbus_tcp.egg-info/
+-rw-rw-r--   0 luc       (1000) luc       (1000)    12403 2023-07-23 13:18:43.000000 alfen_eve_modbus_tcp-0.0.6/src/alfen_eve_modbus_tcp.egg-info/PKG-INFO
+-rw-rw-r--   0 luc       (1000) luc       (1000)      312 2023-07-23 13:18:43.000000 alfen_eve_modbus_tcp-0.0.6/src/alfen_eve_modbus_tcp.egg-info/SOURCES.txt
+-rw-rw-r--   0 luc       (1000) luc       (1000)        1 2023-07-23 13:18:43.000000 alfen_eve_modbus_tcp-0.0.6/src/alfen_eve_modbus_tcp.egg-info/dependency_links.txt
+-rw-rw-r--   0 luc       (1000) luc       (1000)       40 2023-07-23 13:18:43.000000 alfen_eve_modbus_tcp-0.0.6/src/alfen_eve_modbus_tcp.egg-info/requires.txt
+-rw-rw-r--   0 luc       (1000) luc       (1000)       21 2023-07-23 13:18:43.000000 alfen_eve_modbus_tcp-0.0.6/src/alfen_eve_modbus_tcp.egg-info/top_level.txt
```

### Comparing `alfen_eve_modbus_tcp-0.0.5/LICENSE` & `alfen_eve_modbus_tcp-0.0.6/LICENSE`

 * *Files identical despite different names*

### Comparing `alfen_eve_modbus_tcp-0.0.5/PKG-INFO` & `alfen_eve_modbus_tcp-0.0.6/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: alfen_eve_modbus_tcp
-Version: 0.0.5
+Version: 0.0.6
 Summary: Alfen Eve Car Charger parser library
 Home-page: https://github.com/nessnaj/alfen_eve_modbus_tcp
 Author: nessnaj
 License: MIT License
 Project-URL: Issue Tracker, https://github.com/nessnaj/alfen_eve_modbus_tcp/issues
 Classifier: Development Status :: 4 - Beta
 Classifier: Programming Language :: Python :: 3.8
```

### Comparing `alfen_eve_modbus_tcp-0.0.5/README.md` & `alfen_eve_modbus_tcp-0.0.6/README.md`

 * *Files identical despite different names*

### Comparing `alfen_eve_modbus_tcp-0.0.5/setup.cfg` & `alfen_eve_modbus_tcp-0.0.6/setup.cfg`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = alfen_eve_modbus_tcp
-version = 0.0.5
+version = 0.0.6
 author = nessnaj
 description = Alfen Eve Car Charger parser library
 long_description = file: README.md
 long_description_content_type = text/markdown
 license = MIT License
 url = https://github.com/nessnaj/alfen_eve_modbus_tcp
 project_urls =
```

### Comparing `alfen_eve_modbus_tcp-0.0.5/src/alfen_eve_modbus_tcp/__init__.py` & `alfen_eve_modbus_tcp-0.0.6/src/alfen_eve_modbus_tcp/__init__.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,14 +1,15 @@
 # Module to read/write Modbus message over TCP to Alfen Eve (Single Pro-Line) car charger
 # This code has been created by heavily making use of the code for SolarEdge inverter
 # created by nmakel/solaredge_modbus on GitHub.com
 # Basically I have adapted that code to reflect the situation for the Alfen CarCharger instead of the SolarEdge Inverter
 
 import enum
 import time
+import syslog
 
 from pymodbus.constants import Endian
 from pymodbus.payload import BinaryPayloadBuilder
 from pymodbus.payload import BinaryPayloadDecoder
 from pymodbus.client import ModbusTcpClient
 from pymodbus.register_read_message import ReadHoldingRegistersResponse
 
@@ -476,35 +477,39 @@
             "scn_modbus_slave_max_current_enable": (0xc8, 0x597, 1, registerType.HOLDING, registerDataType.UINT16, int, "1: Enabled; 0: Disabled", "1A",
             8)
 
         }
 
     def pause_charging(self):
         PAUSE_CURRENT = 5
-        print(f"Stop Charging...")
+        syslog.syslog("Stop Charging...")
         value = self.read('modbus_slave_max_current')
         current = value['modbus_slave_max_current']
-        print(f"\tCurrent usage in A: {current}")
+        syslog.syslog(f"Current usage in A: {current}")
         if current > 5.5:
-            print(f"\tPausing...")
+            syslog.syslog("Pausing...")
             self.set_current(PAUSE_CURRENT)
-            print(f"\tPaused...")
+            syslog.syslog("Paused...")
         else:
-            print(f"\tAlready paused charging...")
+            syslog.syslog("Already paused charging...")
 
     def switch_phase(self, phases):
         if (phases == 1 or phases == 3):
             current_phases = self.read('charge_using_1_or_3_phases')['charge_using_1_or_3_phases']
             if current_phases == phases:
-                print(f"No need to switch, already at {phases} phase...")
+                syslog.syslog(f"No need to switch, already at {phases} phase...")
             else:
-                print(f"Switch to {phases} phase(s)...")
-                print(f"\tCurrent phase(s): {current_phases}")
-                self.write('charge_using_1_or_3_phases', phases)
-                print(f"\tSwitched...")
-                current_phases = self.read('charge_using_1_or_3_phases')['charge_using_1_or_3_phases']
-                print(f"\tCurrent phase(s): {current_phases}")
+                try:
+                    syslog.syslog(f"Switch to {phases} phase(s)...")
+                    syslog.syslog(f"Current phase(s): {current_phases}")
+                    self.write('charge_using_1_or_3_phases', phases)
+                    syslog.syslog("Switched...")
+                except Exception as e:
+                    syslog.syslog(e)
+                finally:
+                    current_phases = self.read('charge_using_1_or_3_phases')['charge_using_1_or_3_phases']
+                    syslog.syslog(f"Current phase(s): {current_phases}")
         else:
-            print(f"\tInvalid # of phases: {phases}...")
+            syslog.syslog(f"Invalid # of phases: {phases}...")
 
     def set_current(self, current):
         self.write('modbus_slave_max_current', current)
```

### Comparing `alfen_eve_modbus_tcp-0.0.5/src/alfen_eve_modbus_tcp.egg-info/PKG-INFO` & `alfen_eve_modbus_tcp-0.0.6/src/alfen_eve_modbus_tcp.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: alfen-eve-modbus-tcp
-Version: 0.0.5
+Version: 0.0.6
 Summary: Alfen Eve Car Charger parser library
 Home-page: https://github.com/nessnaj/alfen_eve_modbus_tcp
 Author: nessnaj
 License: MIT License
 Project-URL: Issue Tracker, https://github.com/nessnaj/alfen_eve_modbus_tcp/issues
 Classifier: Development Status :: 4 - Beta
 Classifier: Programming Language :: Python :: 3.8
```

