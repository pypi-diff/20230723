# Comparing `tmp/subarulink-0.7.6.post1.tar.gz` & `tmp/subarulink-0.7.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "subarulink-0.7.6.post1.tar", last modified: Sun May 21 15:46:10 2023, max compression
+gzip compressed data, was "subarulink-0.7.7.tar", last modified: Sun Jul 23 01:05:57 2023, max compression
```

## Comparing `subarulink-0.7.6.post1.tar` & `subarulink-0.7.7.tar`

### file list

```diff
@@ -1,35 +1,35 @@
-drwxr-xr-x   0 gg         (501) wheel        (0)        0 2023-05-21 15:46:10.524129 subarulink-0.7.6.post1/
--rw-r--r--   0 gg         (501) wheel        (0)      195 2022-02-12 17:50:33.000000 subarulink-0.7.6.post1/AUTHORS.md
--rw-r--r--   0 gg         (501) wheel        (0)     6362 2022-03-30 01:34:05.000000 subarulink-0.7.6.post1/DEVELOPERS.md
--rw-r--r--   0 gg         (501) wheel        (0)    11358 2020-10-11 22:38:54.000000 subarulink-0.7.6.post1/LICENSE
--rw-r--r--   0 gg         (501) wheel        (0)       30 2022-02-12 17:49:18.000000 subarulink-0.7.6.post1/MANIFEST.in
--rw-r--r--   0 gg         (501) wheel        (0)     8203 2023-05-21 15:46:10.524201 subarulink-0.7.6.post1/PKG-INFO
--rw-r--r--   0 gg         (501) wheel        (0)     7591 2023-05-21 15:44:58.000000 subarulink-0.7.6.post1/README.md
--rw-r--r--   0 gg         (501) wheel        (0)     2479 2022-12-18 23:12:31.000000 subarulink-0.7.6.post1/pyproject.toml
--rw-r--r--   0 gg         (501) wheel        (0)      509 2023-05-21 15:46:10.524511 subarulink-0.7.6.post1/setup.cfg
--rw-r--r--   0 gg         (501) wheel        (0)     3971 2022-12-08 02:51:09.000000 subarulink-0.7.6.post1/setup.py
-drwxr-xr-x   0 gg         (501) wheel        (0)        0 2023-05-21 15:46:10.520447 subarulink-0.7.6.post1/subarulink/
--rw-r--r--   0 gg         (501) wheel        (0)      808 2022-12-03 21:57:17.000000 subarulink-0.7.6.post1/subarulink/__init__.py
--rw-r--r--   0 gg         (501) wheel        (0)      266 2023-05-21 15:45:55.000000 subarulink-0.7.6.post1/subarulink/__version__.py
-drwxr-xr-x   0 gg         (501) wheel        (0)        0 2023-05-21 15:46:10.521929 subarulink-0.7.6.post1/subarulink/_subaru_api/
--rw-r--r--   0 gg         (501) wheel        (0)      204 2022-12-08 02:51:09.000000 subarulink-0.7.6.post1/subarulink/_subaru_api/__init__.py
--rw-r--r--   0 gg         (501) wheel        (0)     7266 2023-04-07 05:56:35.000000 subarulink-0.7.6.post1/subarulink/_subaru_api/const.py
-drwxr-xr-x   0 gg         (501) wheel        (0)        0 2023-05-21 15:46:10.522491 subarulink-0.7.6.post1/subarulink/app/
--rw-r--r--   0 gg         (501) wheel        (0)      219 2022-02-12 17:50:33.000000 subarulink-0.7.6.post1/subarulink/app/__init__.py
--rw-r--r--   0 gg         (501) wheel        (0)    29784 2023-02-18 01:13:37.000000 subarulink-0.7.6.post1/subarulink/app/cli.py
--rw-r--r--   0 gg         (501) wheel        (0)    13734 2023-04-08 01:17:29.000000 subarulink-0.7.6.post1/subarulink/connection.py
--rw-r--r--   0 gg         (501) wheel        (0)     7433 2023-01-21 17:52:41.000000 subarulink-0.7.6.post1/subarulink/const.py
--rw-r--r--   0 gg         (501) wheel        (0)    56337 2023-04-08 01:17:38.000000 subarulink-0.7.6.post1/subarulink/controller.py
--rw-r--r--   0 gg         (501) wheel        (0)     1187 2020-12-24 00:13:12.000000 subarulink-0.7.6.post1/subarulink/exceptions.py
-drwxr-xr-x   0 gg         (501) wheel        (0)        0 2023-05-21 15:46:10.521528 subarulink-0.7.6.post1/subarulink.egg-info/
--rw-r--r--   0 gg         (501) wheel        (0)     8203 2023-05-21 15:46:10.000000 subarulink-0.7.6.post1/subarulink.egg-info/PKG-INFO
--rw-r--r--   0 gg         (501) wheel        (0)      656 2023-05-21 15:46:10.000000 subarulink-0.7.6.post1/subarulink.egg-info/SOURCES.txt
--rw-r--r--   0 gg         (501) wheel        (0)        1 2023-05-21 15:46:10.000000 subarulink-0.7.6.post1/subarulink.egg-info/dependency_links.txt
--rw-r--r--   0 gg         (501) wheel        (0)       55 2023-05-21 15:46:10.000000 subarulink-0.7.6.post1/subarulink.egg-info/entry_points.txt
--rw-r--r--   0 gg         (501) wheel        (0)       18 2023-05-21 15:46:10.000000 subarulink-0.7.6.post1/subarulink.egg-info/requires.txt
--rw-r--r--   0 gg         (501) wheel        (0)       11 2023-05-21 15:46:10.000000 subarulink-0.7.6.post1/subarulink.egg-info/top_level.txt
-drwxr-xr-x   0 gg         (501) wheel        (0)        0 2023-05-21 15:46:10.523972 subarulink-0.7.6.post1/tests/
--rw-r--r--   0 gg         (501) wheel        (0)     4575 2023-01-21 17:52:41.000000 subarulink-0.7.6.post1/tests/test_cli.py
--rw-r--r--   0 gg         (501) wheel        (0)    15062 2023-01-21 17:52:41.000000 subarulink-0.7.6.post1/tests/test_connection.py
--rw-r--r--   0 gg         (501) wheel        (0)    15911 2022-12-18 20:24:35.000000 subarulink-0.7.6.post1/tests/test_remote_commands.py
--rw-r--r--   0 gg         (501) wheel        (0)     9684 2023-01-21 17:52:41.000000 subarulink-0.7.6.post1/tests/test_vehicle_status.py
+drwxr-xr-x   0 gg         (501) wheel        (0)        0 2023-07-23 01:05:57.858441 subarulink-0.7.7/
+-rw-r--r--   0 gg         (501) wheel        (0)      195 2022-02-12 17:50:33.000000 subarulink-0.7.7/AUTHORS.md
+-rw-r--r--   0 gg         (501) wheel        (0)     6362 2022-03-30 01:34:05.000000 subarulink-0.7.7/DEVELOPERS.md
+-rw-r--r--   0 gg         (501) wheel        (0)    11358 2020-10-11 22:38:54.000000 subarulink-0.7.7/LICENSE
+-rw-r--r--   0 gg         (501) wheel        (0)       30 2022-02-12 17:49:18.000000 subarulink-0.7.7/MANIFEST.in
+-rw-r--r--   0 gg         (501) wheel        (0)     8197 2023-07-23 01:05:57.858528 subarulink-0.7.7/PKG-INFO
+-rw-r--r--   0 gg         (501) wheel        (0)     7591 2023-05-21 15:44:58.000000 subarulink-0.7.7/README.md
+-rw-r--r--   0 gg         (501) wheel        (0)     2479 2022-12-18 23:12:31.000000 subarulink-0.7.7/pyproject.toml
+-rw-r--r--   0 gg         (501) wheel        (0)      509 2023-07-23 01:05:57.858862 subarulink-0.7.7/setup.cfg
+-rw-r--r--   0 gg         (501) wheel        (0)     3971 2023-07-23 00:15:28.000000 subarulink-0.7.7/setup.py
+drwxr-xr-x   0 gg         (501) wheel        (0)        0 2023-07-23 01:05:57.856151 subarulink-0.7.7/subarulink/
+-rw-r--r--   0 gg         (501) wheel        (0)      808 2023-07-23 00:15:28.000000 subarulink-0.7.7/subarulink/__init__.py
+-rw-r--r--   0 gg         (501) wheel        (0)      264 2023-07-23 00:54:27.000000 subarulink-0.7.7/subarulink/__version__.py
+drwxr-xr-x   0 gg         (501) wheel        (0)        0 2023-07-23 01:05:57.857147 subarulink-0.7.7/subarulink/_subaru_api/
+-rw-r--r--   0 gg         (501) wheel        (0)      204 2022-12-08 02:51:09.000000 subarulink-0.7.7/subarulink/_subaru_api/__init__.py
+-rw-r--r--   0 gg         (501) wheel        (0)     7266 2023-07-23 00:15:28.000000 subarulink-0.7.7/subarulink/_subaru_api/const.py
+drwxr-xr-x   0 gg         (501) wheel        (0)        0 2023-07-23 01:05:57.857369 subarulink-0.7.7/subarulink/app/
+-rw-r--r--   0 gg         (501) wheel        (0)      219 2022-02-12 17:50:33.000000 subarulink-0.7.7/subarulink/app/__init__.py
+-rw-r--r--   0 gg         (501) wheel        (0)    29784 2023-07-23 00:15:28.000000 subarulink-0.7.7/subarulink/app/cli.py
+-rw-r--r--   0 gg         (501) wheel        (0)    13734 2023-07-23 00:15:28.000000 subarulink-0.7.7/subarulink/connection.py
+-rw-r--r--   0 gg         (501) wheel        (0)     7433 2023-01-21 17:52:41.000000 subarulink-0.7.7/subarulink/const.py
+-rw-r--r--   0 gg         (501) wheel        (0)    56258 2023-07-23 00:53:37.000000 subarulink-0.7.7/subarulink/controller.py
+-rw-r--r--   0 gg         (501) wheel        (0)     1187 2020-12-24 00:13:12.000000 subarulink-0.7.7/subarulink/exceptions.py
+drwxr-xr-x   0 gg         (501) wheel        (0)        0 2023-07-23 01:05:57.856899 subarulink-0.7.7/subarulink.egg-info/
+-rw-r--r--   0 gg         (501) wheel        (0)     8197 2023-07-23 01:05:57.000000 subarulink-0.7.7/subarulink.egg-info/PKG-INFO
+-rw-r--r--   0 gg         (501) wheel        (0)      656 2023-07-23 01:05:57.000000 subarulink-0.7.7/subarulink.egg-info/SOURCES.txt
+-rw-r--r--   0 gg         (501) wheel        (0)        1 2023-07-23 01:05:57.000000 subarulink-0.7.7/subarulink.egg-info/dependency_links.txt
+-rw-r--r--   0 gg         (501) wheel        (0)       55 2023-07-23 01:05:57.000000 subarulink-0.7.7/subarulink.egg-info/entry_points.txt
+-rw-r--r--   0 gg         (501) wheel        (0)       18 2023-07-23 01:05:57.000000 subarulink-0.7.7/subarulink.egg-info/requires.txt
+-rw-r--r--   0 gg         (501) wheel        (0)       11 2023-07-23 01:05:57.000000 subarulink-0.7.7/subarulink.egg-info/top_level.txt
+drwxr-xr-x   0 gg         (501) wheel        (0)        0 2023-07-23 01:05:57.858316 subarulink-0.7.7/tests/
+-rw-r--r--   0 gg         (501) wheel        (0)     4575 2023-01-21 17:52:41.000000 subarulink-0.7.7/tests/test_cli.py
+-rw-r--r--   0 gg         (501) wheel        (0)    15062 2023-01-21 17:52:41.000000 subarulink-0.7.7/tests/test_connection.py
+-rw-r--r--   0 gg         (501) wheel        (0)    15911 2022-12-18 20:24:35.000000 subarulink-0.7.7/tests/test_remote_commands.py
+-rw-r--r--   0 gg         (501) wheel        (0)     9684 2023-01-21 17:52:41.000000 subarulink-0.7.7/tests/test_vehicle_status.py
```

### Comparing `subarulink-0.7.6.post1/DEVELOPERS.md` & `subarulink-0.7.7/DEVELOPERS.md`

 * *Files identical despite different names*

### Comparing `subarulink-0.7.6.post1/LICENSE` & `subarulink-0.7.7/LICENSE`

 * *Files identical despite different names*

### Comparing `subarulink-0.7.6.post1/PKG-INFO` & `subarulink-0.7.7/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: subarulink
-Version: 0.7.6.post1
+Version: 0.7.7
 Summary: A package for interacting with Subaru Starlink Remote Services API.
 Home-page: https://github.com/G-Two/subarulink
 Author: G-Two
 Author-email: 
 License: Apache-2.0
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
```

### Comparing `subarulink-0.7.6.post1/README.md` & `subarulink-0.7.7/README.md`

 * *Files identical despite different names*

### Comparing `subarulink-0.7.6.post1/pyproject.toml` & `subarulink-0.7.7/pyproject.toml`

 * *Files identical despite different names*

### Comparing `subarulink-0.7.6.post1/setup.py` & `subarulink-0.7.7/setup.py`

 * *Files identical despite different names*

### Comparing `subarulink-0.7.6.post1/subarulink/__init__.py` & `subarulink-0.7.7/subarulink/__init__.py`

 * *Files identical despite different names*

### Comparing `subarulink-0.7.6.post1/subarulink/_subaru_api/const.py` & `subarulink-0.7.7/subarulink/_subaru_api/const.py`

 * *Files identical despite different names*

### Comparing `subarulink-0.7.6.post1/subarulink/app/cli.py` & `subarulink-0.7.7/subarulink/app/cli.py`

 * *Files identical despite different names*

### Comparing `subarulink-0.7.6.post1/subarulink/connection.py` & `subarulink-0.7.7/subarulink/connection.py`

 * *Files identical despite different names*

### Comparing `subarulink-0.7.6.post1/subarulink/const.py` & `subarulink-0.7.7/subarulink/const.py`

 * *Files identical despite different names*

### Comparing `subarulink-0.7.6.post1/subarulink/controller.py` & `subarulink-0.7.7/subarulink/controller.py`

 * *Files 0% similar despite different names*

```diff
@@ -273,15 +273,15 @@
             vin (str): The VIN to check.
 
         Returns:
             bool: `True` if `vin` reports power window status, `False` if not.
         """
         vehicle = self._vehicles.get(vin.upper())
         if vehicle:
-            status = api.API_FEATURE_POWER_WINDOWS in vehicle[sc.VEHICLE_FEATURES] and self.get_remote_status(vin)
+            status = api.API_FEATURE_POWER_WINDOWS in vehicle[sc.VEHICLE_FEATURES]
             _LOGGER.debug("Getting power window status %s:%s", vin, status)
             return status
         raise SubaruException("Invalid VIN")
 
     def has_sunroof(self, vin: str) -> bool:
         """
         Return whether the specified VIN reports sunroof status.
@@ -291,20 +291,19 @@
 
         Returns:
             bool: `True` if `vin` reports sunroof status, `False` if not.
         """
         vehicle = self._vehicles.get(vin.upper())
         if vehicle:
             status = False
-            if self.has_power_windows(vin):
-                if (
-                    api.API_FEATURE_MOONROOF_PANORAMIC in vehicle[sc.VEHICLE_FEATURES]
-                    or api.API_FEATURE_MOONROOF_POWER in vehicle[sc.VEHICLE_FEATURES]
-                ):
-                    status = True
+            if (
+                api.API_FEATURE_MOONROOF_PANORAMIC in vehicle[sc.VEHICLE_FEATURES]
+                or api.API_FEATURE_MOONROOF_POWER in vehicle[sc.VEHICLE_FEATURES]
+            ):
+                status = True
             _LOGGER.debug("Getting moonroof status %s:%s", vin, status)
             return status
         raise SubaruException("Invalid VIN")
 
     def get_safety_status(self, vin: str) -> bool:
         """
         Get whether the specified VIN is has an active Starlink Safety Plus service plan.
@@ -1291,26 +1290,26 @@
         keep_data[sc.TIMESTAMP] = datetime.strptime(data[api.API_LAST_UPDATED_DATE], api.API_TIMESTAMP_FMT)
 
         # Only some (probably G3) vehicles properly report fuel remaining
         if data[api.API_REMAINING_FUEL_PERCENT]:
             keep_data[sc.REMAINING_FUEL_PERCENT] = data[api.API_REMAINING_FUEL_PERCENT]
 
         # Parse window/sunroof status for supported vehicles
-        if self.has_power_windows(vin):
+        if self.has_power_windows(vin) or self.has_sunroof(vin):
             keep_data.update(
                 {
                     sc.WINDOW_FRONT_LEFT_STATUS: data[api.API_WINDOW_FRONT_LEFT_STATUS],
                     sc.WINDOW_FRONT_RIGHT_STATUS: data[api.API_WINDOW_FRONT_RIGHT_STATUS],
                     sc.WINDOW_REAR_LEFT_STATUS: data[api.API_WINDOW_REAR_LEFT_STATUS],
                     sc.WINDOW_REAR_RIGHT_STATUS: data[api.API_WINDOW_REAR_RIGHT_STATUS],
                 }
             )
 
-            if self.has_sunroof(vin):
-                keep_data[sc.WINDOW_SUNROOF_STATUS] = data[api.API_WINDOW_SUNROOF_STATUS]
+        if self.has_sunroof(vin):
+            keep_data[sc.WINDOW_SUNROOF_STATUS] = data[api.API_WINDOW_SUNROOF_STATUS]
 
         # Parse EV specific values
         if self.get_ev_status(vin):
             # Value is correct unless it is None
             keep_data[sc.EV_DISTANCE_TO_EMPTY] = int(data.get(api.API_EV_DISTANCE_TO_EMPTY) or 0)
             keep_data[sc.EV_STATE_OF_CHARGE_PERCENT] = float(data.get(api.API_EV_STATE_OF_CHARGE_PERCENT) or 0)
             keep_data[sc.EV_IS_PLUGGED_IN] = data.get(api.API_EV_IS_PLUGGED_IN)
```

### Comparing `subarulink-0.7.6.post1/subarulink/exceptions.py` & `subarulink-0.7.7/subarulink/exceptions.py`

 * *Files identical despite different names*

### Comparing `subarulink-0.7.6.post1/subarulink.egg-info/PKG-INFO` & `subarulink-0.7.7/subarulink.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: subarulink
-Version: 0.7.6.post1
+Version: 0.7.7
 Summary: A package for interacting with Subaru Starlink Remote Services API.
 Home-page: https://github.com/G-Two/subarulink
 Author: G-Two
 Author-email: 
 License: Apache-2.0
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
```

### Comparing `subarulink-0.7.6.post1/subarulink.egg-info/SOURCES.txt` & `subarulink-0.7.7/subarulink.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `subarulink-0.7.6.post1/tests/test_cli.py` & `subarulink-0.7.7/tests/test_cli.py`

 * *Files identical despite different names*

### Comparing `subarulink-0.7.6.post1/tests/test_connection.py` & `subarulink-0.7.7/tests/test_connection.py`

 * *Files identical despite different names*

### Comparing `subarulink-0.7.6.post1/tests/test_remote_commands.py` & `subarulink-0.7.7/tests/test_remote_commands.py`

 * *Files identical despite different names*

### Comparing `subarulink-0.7.6.post1/tests/test_vehicle_status.py` & `subarulink-0.7.7/tests/test_vehicle_status.py`

 * *Files identical despite different names*

