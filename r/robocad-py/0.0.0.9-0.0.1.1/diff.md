# Comparing `tmp/robocad-py-0.0.0.9.tar.gz` & `tmp/robocad-py-0.0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist\robocad-py-0.0.0.9.tar", last modified: Tue Apr  4 20:42:30 2023, max compression
+gzip compressed data, was "dist\robocad-py-0.0.1.1.tar", last modified: Sun Jul 23 09:25:10 2023, max compression
```

## Comparing `robocad-py-0.0.0.9.tar` & `robocad-py-0.0.1.1.tar`

### file list

```diff
@@ -1,25 +1,25 @@
-drwxrwxrwx   0        0        0        0 2023-04-04 20:42:30.000000 robocad-py-0.0.0.9/
--rw-rw-rw-   0        0        0      291 2023-04-04 20:42:24.000000 robocad-py-0.0.0.9/CHANGELOG.md
--rw-rw-rw-   0        0        0     1090 2023-03-30 12:51:13.000000 robocad-py-0.0.0.9/LICENSE
--rw-rw-rw-   0        0        0      109 2023-04-03 12:09:29.000000 robocad-py-0.0.0.9/MANIFEST.in
--rw-rw-rw-   0        0        0     1121 2023-04-04 20:42:30.000000 robocad-py-0.0.0.9/PKG-INFO
-drwxrwxrwx   0        0        0        0 2023-04-04 20:42:30.000000 robocad-py-0.0.0.9/robocad/
--rw-rw-rw-   0        0        0        0 2023-04-03 12:05:15.000000 robocad-py-0.0.0.9/robocad/__init__.py
-drwxrwxrwx   0        0        0        0 2023-04-04 20:42:30.000000 robocad-py-0.0.0.9/robocad/pycad/
--rw-rw-rw-   0        0        0     6309 2023-04-04 20:20:17.000000 robocad-py-0.0.0.9/robocad/pycad/COM.py
--rw-rw-rw-   0        0        0     4195 2023-04-04 20:21:46.000000 robocad-py-0.0.0.9/robocad/pycad/SPI.py
--rw-rw-rw-   0        0        0        0 2023-03-30 13:39:56.000000 robocad-py-0.0.0.9/robocad/pycad/__init__.py
--rw-rw-rw-   0        0        0     2226 2023-03-31 09:48:29.000000 robocad-py-0.0.0.9/robocad/pycad/shared.py
--rw-rw-rw-   0        0        0    12812 2023-04-04 20:42:24.000000 robocad-py-0.0.0.9/robocad/robocad.py
-drwxrwxrwx   0        0        0        0 2023-04-04 20:42:30.000000 robocad-py-0.0.0.9/robocad/robocadSim/
--rw-rw-rw-   0        0        0        0 2023-03-30 13:43:09.000000 robocad-py-0.0.0.9/robocad/robocadSim/__init__.py
--rw-rw-rw-   0        0        0     7050 2023-03-30 15:17:29.000000 robocad-py-0.0.0.9/robocad/robocadSim/connection.py
--rw-rw-rw-   0        0        0     4121 2023-03-30 15:47:19.000000 robocad-py-0.0.0.9/robocad/robocadSim/connection_helper.py
-drwxrwxrwx   0        0        0        0 2023-04-04 20:42:30.000000 robocad-py-0.0.0.9/robocad_py.egg-info/
--rw-rw-rw-   0        0        0     1121 2023-04-04 20:42:30.000000 robocad-py-0.0.0.9/robocad_py.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      445 2023-04-04 20:42:30.000000 robocad-py-0.0.0.9/robocad_py.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-04-04 20:42:30.000000 robocad-py-0.0.0.9/robocad_py.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       27 2023-04-04 20:42:30.000000 robocad-py-0.0.0.9/robocad_py.egg-info/requires.txt
--rw-rw-rw-   0        0        0        8 2023-04-04 20:42:30.000000 robocad-py-0.0.0.9/robocad_py.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-04-04 20:42:30.000000 robocad-py-0.0.0.9/setup.cfg
--rw-rw-rw-   0        0        0      887 2023-04-04 20:42:23.000000 robocad-py-0.0.0.9/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 09:25:10.000000 robocad-py-0.0.1.1/
+-rw-rw-rw-   0        0        0      364 2023-07-23 09:23:41.000000 robocad-py-0.0.1.1/CHANGELOG.md
+-rw-rw-rw-   0        0        0     1090 2023-03-30 12:51:13.000000 robocad-py-0.0.1.1/LICENSE
+-rw-rw-rw-   0        0        0      109 2023-04-03 12:09:29.000000 robocad-py-0.0.1.1/MANIFEST.in
+-rw-rw-rw-   0        0        0     1218 2023-07-23 09:25:10.000000 robocad-py-0.0.1.1/PKG-INFO
+drwxrwxrwx   0        0        0        0 2023-07-23 09:25:10.000000 robocad-py-0.0.1.1/robocad/
+-rw-rw-rw-   0        0        0        0 2023-04-03 12:05:15.000000 robocad-py-0.0.1.1/robocad/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 09:25:10.000000 robocad-py-0.0.1.1/robocad/pycad/
+-rw-rw-rw-   0        0        0     6309 2023-04-04 20:20:17.000000 robocad-py-0.0.1.1/robocad/pycad/COM.py
+-rw-rw-rw-   0        0        0     4195 2023-04-04 20:21:46.000000 robocad-py-0.0.1.1/robocad/pycad/SPI.py
+-rw-rw-rw-   0        0        0        0 2023-03-30 13:39:56.000000 robocad-py-0.0.1.1/robocad/pycad/__init__.py
+-rw-rw-rw-   0        0        0     2226 2023-03-31 09:48:29.000000 robocad-py-0.0.1.1/robocad/pycad/shared.py
+-rw-rw-rw-   0        0        0    12552 2023-07-23 09:22:16.000000 robocad-py-0.0.1.1/robocad/robocad.py
+drwxrwxrwx   0        0        0        0 2023-07-23 09:25:10.000000 robocad-py-0.0.1.1/robocad/robocadSim/
+-rw-rw-rw-   0        0        0        0 2023-03-30 13:43:09.000000 robocad-py-0.0.1.1/robocad/robocadSim/__init__.py
+-rw-rw-rw-   0        0        0     7050 2023-03-30 15:17:29.000000 robocad-py-0.0.1.1/robocad/robocadSim/connection.py
+-rw-rw-rw-   0        0        0     1201 2023-07-23 09:12:30.000000 robocad-py-0.0.1.1/robocad/robocadSim/connection_helper_vmx_titan.py
+drwxrwxrwx   0        0        0        0 2023-07-23 09:25:10.000000 robocad-py-0.0.1.1/robocad_py.egg-info/
+-rw-rw-rw-   0        0        0     1218 2023-07-23 09:25:09.000000 robocad-py-0.0.1.1/robocad_py.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      455 2023-07-23 09:25:09.000000 robocad-py-0.0.1.1/robocad_py.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 09:25:09.000000 robocad-py-0.0.1.1/robocad_py.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       27 2023-07-23 09:25:09.000000 robocad-py-0.0.1.1/robocad_py.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        8 2023-07-23 09:25:09.000000 robocad-py-0.0.1.1/robocad_py.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 09:25:10.000000 robocad-py-0.0.1.1/setup.cfg
+-rw-rw-rw-   0        0        0      887 2023-07-23 09:23:41.000000 robocad-py-0.0.1.1/setup.py
```

### Comparing `robocad-py-0.0.0.9/LICENSE` & `robocad-py-0.0.1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `robocad-py-0.0.0.9/PKG-INFO` & `robocad-py-0.0.1.1/PKG-INFO`

 * *Files 11% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 1.1
 Name: robocad-py
-Version: 0.0.0.9
+Version: 0.0.1.1
 Summary: python lib for real and virtual robots
 Home-page: https://github.com/CrackAndDie/robocad-py
 Author: Abdrakov Airat
 Author-email: abdrakovairat@gmail.com
 License: MIT
 Description: Python library for real and virtual robots
         
@@ -26,14 +26,17 @@
         - Thread joins added
         
         ## 0.0.0.8
         - Thread joins fixed :)
         
         ## 0.0.0.9
         - Thread joins fixed 2 :)
+        
+        ## 0.0.1.1
+        - Library fully changed according to the new requirements
 Keywords: simulator,robotics,robot,3d,raspberry,control
 Platform: UNKNOWN
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Education
 Classifier: Operating System :: Microsoft :: Windows :: Windows 10
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
```

### Comparing `robocad-py-0.0.0.9/robocad/pycad/COM.py` & `robocad-py-0.0.1.1/robocad/pycad/COM.py`

 * *Files identical despite different names*

### Comparing `robocad-py-0.0.0.9/robocad/pycad/SPI.py` & `robocad-py-0.0.1.1/robocad/pycad/SPI.py`

 * *Files identical despite different names*

### Comparing `robocad-py-0.0.0.9/robocad/pycad/shared.py` & `robocad-py-0.0.1.1/robocad/pycad/shared.py`

 * *Files identical despite different names*

### Comparing `robocad-py-0.0.0.9/robocad/robocad.py` & `robocad-py-0.0.1.1/robocad/robocad.py`

 * *Files 3% similar despite different names*

```diff
@@ -4,14 +4,16 @@
 import signal
 from threading import Thread
 import subprocess
 
 from shufflecad.shufflecad import Shufflecad
 from shufflecad.shared import InfoHolder
 
+from .robocadSim.connection_helper_vmx_titan import ConnectionHelperVMXTitan
+
 
 class RobocadVMXTitan:
     def __init__(self, is_real_robot: bool = True):
         self.__motor_speed_0 = 0.0
         self.__motor_speed_1 = 0.0
         self.__motor_speed_2 = 0.0
         self.__motor_speed_3 = 0.0
@@ -58,16 +60,15 @@
         InfoHolder.on_real_robot = is_real_robot
         Shufflecad.start()
 
         signal.signal(signal.SIGTERM, self.handler)
         signal.signal(signal.SIGINT, self.handler)
 
         if not self.is_real_robot:
-            from .robocadSim.connection_helper import ConnectionHelper
-            self.__connection_helper = ConnectionHelper(ConnectionHelper.CONN_ALL)
+            self.__connection_helper = ConnectionHelperVMXTitan()
             self.__connection_helper.start_channels()
 
             InfoHolder.power = "12"  # :)
         else:
             try:
                 self.__camera_instance = cv2.VideoCapture(0)
             except Exception as e:
@@ -119,51 +120,51 @@
     def motor_speed_0(self):
         return self.__motor_speed_0
 
     @motor_speed_0.setter
     def motor_speed_0(self, value):
         self.__motor_speed_0 = value
         if not self.is_real_robot:
-            self.__update_motors()
+            self.__update_set_data()
         else:
             TitanStatic.speed_motor_0 = value
 
     @property
     def motor_speed_1(self):
         return self.__motor_speed_1
 
     @motor_speed_1.setter
     def motor_speed_1(self, value):
         self.__motor_speed_1 = value
         if not self.is_real_robot:
-            self.__update_motors()
+            self.__update_set_data()
         else:
             TitanStatic.speed_motor_1 = value
 
     @property
     def motor_speed_2(self):
         return self.__motor_speed_2
 
     @motor_speed_2.setter
     def motor_speed_2(self, value):
         self.__motor_speed_2 = value
         if not self.is_real_robot:
-            self.__update_motors()
+            self.__update_set_data()
         else:
             TitanStatic.speed_motor_2 = value
 
     @property
     def motor_speed_3(self):
         return self.__motor_speed_3
 
     @motor_speed_3.setter
     def motor_speed_3(self, value):
         self.__motor_speed_3 = value
         if not self.is_real_robot:
-            self.__update_motors()
+            self.__update_set_data()
         else:
             TitanStatic.speed_motor_3 = value
 
     @property
     def motor_enc_0(self):
         if not self.is_real_robot:
             self.__update_encs()
@@ -294,99 +295,83 @@
         return self.__camera_image
 
     # port is from 1 to 10 included
     def set_angle_hcdio(self, value: float, port: int):
         if not self.is_real_robot:
             dut: float = 0.000666 * value + 0.05
             self.__hcdio_values[port - 1] = dut
-            self.__update_oms()
+            self.__update_set_data()
         else:
             VMXStatic.set_servo_angle(value, port - 1)
 
     # port is from 1 to 10 included
     def set_pwm_hcdio(self, value: float, port: int):
         if not self.is_real_robot:
             self.__hcdio_values[port - 1] = value
-            self.__update_oms()
+            self.__update_set_data()
         else:
             VMXStatic.set_servo_pwm(value, port - 1)
 
     # port is from 1 to 10 included
     def set_bool_hcdio(self, value: bool, port: int):
         if not self.is_real_robot:
             dut: float = 0.2 if value else 0.0
             self.__hcdio_values[port - 1] = dut
-            self.__update_oms()
+            self.__update_set_data()
         else:
             VMXStatic.set_led_state(value, port - 1)
 
     # for virtual robot
-    def __update_other(self):
-        self.__connection_helper.set_other(
-                (
-                    0, 0, 0,  # there is no other now
-                ))
-
-    def __update_motors(self):
-        self.__connection_helper.set_motors(
-            (
-                self.__motor_speed_0,
-                self.__motor_speed_1,
-                self.__motor_speed_2,
-                self.__motor_speed_3,
-            ))
-
-    def __update_oms(self):
-        self.__connection_helper.set_oms(tuple(self.__hcdio_values))
-
-    def __update_resets(self):
-        self.__connection_helper.set_resets(
-            (
-                0, 0, 0  # there are no resets now
-            ))
+    def __update_set_data(self):
+        values = [self.__motor_speed_0,
+                  self.__motor_speed_1,
+                  self.__motor_speed_2,
+                  self.__motor_speed_3]
+        values.extend(self.__hcdio_values)
+        self.__connection_helper.set_data(tuple(values))
 
     def __update_encs(self):
-        values = self.__connection_helper.get_encs()
-        if len(values) == 4:
+        values = self.__connection_helper.get_data()
+        if len(values) == ConnectionHelperVMXTitan.MAX_DATA_RECEIVE:
             self.__motor_enc_0 = values[0]
             self.__motor_enc_1 = values[1]
             self.__motor_enc_2 = values[2]
             self.__motor_enc_3 = values[3]
 
     def __update_sensors(self):
-        values = self.__connection_helper.get_sens()
-        if len(values) == 7:
-            self.__ultrasound_1 = values[0]
-            self.__ultrasound_2 = values[1]
-            self.__analog_1 = values[2]
-            self.__analog_2 = values[3]
-            self.__analog_3 = values[4]
-            self.__analog_4 = values[5]
-            self.__yaw = values[6]
+        values = self.__connection_helper.get_data()
+        if len(values) == ConnectionHelperVMXTitan.MAX_DATA_RECEIVE:
+            self.__ultrasound_1 = values[4]
+            self.__ultrasound_2 = values[5]
+            self.__analog_1 = values[6]
+            self.__analog_2 = values[7]
+            self.__analog_3 = values[8]
+            self.__analog_4 = values[9]
+            self.__yaw = values[10]
 
     def __update_buttons(self):
-        values = self.__connection_helper.get_buttons()
-        if len(values) == 16:
-            self.__limit_h_0 = values[0]
-            self.__limit_l_0 = values[1]
-            self.__limit_h_1 = values[2]
-            self.__limit_l_1 = values[3]
-            self.__limit_h_2 = values[4]
-            self.__limit_l_2 = values[5]
-            self.__limit_h_3 = values[6]
-            self.__limit_l_3 = values[7]
-
-            self.__flex_0 = values[8]
-            self.__flex_1 = values[9]
-            self.__flex_2 = values[10]
-            self.__flex_3 = values[11]
-            self.__flex_4 = values[12]
-            self.__flex_5 = values[13]
-            self.__flex_6 = values[14]
-            self.__flex_7 = values[15]
+        values = self.__connection_helper.get_data()
+        if len(values) == ConnectionHelperVMXTitan.MAX_DATA_RECEIVE:
+            self.__limit_h_0 = values[11]
+            self.__limit_l_0 = values[12]
+            self.__limit_h_1 = values[13]
+            self.__limit_l_1 = values[14]
+            self.__limit_h_2 = values[15]
+            self.__limit_l_2 = values[16]
+            self.__limit_h_3 = values[17]
+            self.__limit_l_3 = values[18]
+
+            self.__flex_0 = values[19]
+            self.__flex_1 = values[20]
+            self.__flex_2 = values[21]
+            self.__flex_3 = values[22]
+            self.__flex_4 = values[23]
+            self.__flex_5 = values[24]
+            self.__flex_6 = values[25]
+            self.__flex_7 = values[26]
 
     def __update_camera(self):
         # because of 640x480
         camera_data = self.__connection_helper.get_camera()
         if len(camera_data) == 921600:
             nparr = np.frombuffer(camera_data, np.uint8)
             if nparr.size > 0:
```

### Comparing `robocad-py-0.0.0.9/robocad/robocadSim/connection.py` & `robocad-py-0.0.1.1/robocad/robocadSim/connection.py`

 * *Files identical despite different names*

### Comparing `robocad-py-0.0.0.9/robocad_py.egg-info/PKG-INFO` & `robocad-py-0.0.1.1/robocad_py.egg-info/PKG-INFO`

 * *Files 11% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 1.1
 Name: robocad-py
-Version: 0.0.0.9
+Version: 0.0.1.1
 Summary: python lib for real and virtual robots
 Home-page: https://github.com/CrackAndDie/robocad-py
 Author: Abdrakov Airat
 Author-email: abdrakovairat@gmail.com
 License: MIT
 Description: Python library for real and virtual robots
         
@@ -26,14 +26,17 @@
         - Thread joins added
         
         ## 0.0.0.8
         - Thread joins fixed :)
         
         ## 0.0.0.9
         - Thread joins fixed 2 :)
+        
+        ## 0.0.1.1
+        - Library fully changed according to the new requirements
 Keywords: simulator,robotics,robot,3d,raspberry,control
 Platform: UNKNOWN
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Education
 Classifier: Operating System :: Microsoft :: Windows :: Windows 10
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
```

### Comparing `robocad-py-0.0.0.9/setup.py` & `robocad-py-0.0.1.1/setup.py`

 * *Files 11% similar despite different names*

```diff
@@ -6,15 +6,15 @@
     'Operating System :: Microsoft :: Windows :: Windows 10',
     'License :: OSI Approved :: MIT License',
     'Programming Language :: Python :: 3'
 ]
 
 setup(
     name='robocad-py',
-    version='0.0.0.9',
+    version='0.0.1.1',
     description='python lib for real and virtual robots',
     long_description="Python library for real and virtual robots" + '\n\n' + open('CHANGELOG.md').read(),
     url='https://github.com/CrackAndDie/robocad-py',
     author='Abdrakov Airat',
     author_email='abdrakovairat@gmail.com',
     license='MIT',
     classifiers=classifiers,
```

