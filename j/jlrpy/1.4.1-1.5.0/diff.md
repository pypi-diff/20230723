# Comparing `tmp/jlrpy-1.4.1.tar.gz` & `tmp/jlrpy-1.5.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "jlrpy-1.4.1.tar", last modified: Tue Dec 21 18:48:12 2021, max compression
+gzip compressed data, was "jlrpy-1.5.0.tar", last modified: Sun Jul 23 18:38:04 2023, max compression
```

## Comparing `jlrpy-1.4.1.tar` & `jlrpy-1.5.0.tar`

### file list

```diff
@@ -1,12 +1,13 @@
-drwxrwxr-x   0 eho       (1000) eho       (1000)        0 2021-12-21 18:48:12.164456 jlrpy-1.4.1/
--rw-rw-r--   0 eho       (1000) eho       (1000)     1063 2020-06-11 16:20:23.000000 jlrpy-1.4.1/LICENSE
--rw-rw-r--   0 eho       (1000) eho       (1000)     5356 2021-12-21 18:48:12.164456 jlrpy-1.4.1/PKG-INFO
--rw-rw-r--   0 eho       (1000) eho       (1000)     4825 2021-12-21 18:42:59.000000 jlrpy-1.4.1/README.md
-drwxrwxr-x   0 eho       (1000) eho       (1000)        0 2021-12-21 18:48:12.164456 jlrpy-1.4.1/jlrpy.egg-info/
--rw-rw-r--   0 eho       (1000) eho       (1000)     5356 2021-12-21 18:48:12.000000 jlrpy-1.4.1/jlrpy.egg-info/PKG-INFO
--rw-rw-r--   0 eho       (1000) eho       (1000)      151 2021-12-21 18:48:12.000000 jlrpy-1.4.1/jlrpy.egg-info/SOURCES.txt
--rw-rw-r--   0 eho       (1000) eho       (1000)        1 2021-12-21 18:48:12.000000 jlrpy-1.4.1/jlrpy.egg-info/dependency_links.txt
--rw-rw-r--   0 eho       (1000) eho       (1000)        6 2021-12-21 18:48:12.000000 jlrpy-1.4.1/jlrpy.egg-info/top_level.txt
--rw-rw-r--   0 eho       (1000) eho       (1000)    27019 2021-12-21 18:45:21.000000 jlrpy-1.4.1/jlrpy.py
--rw-rw-r--   0 eho       (1000) eho       (1000)       38 2021-12-21 18:48:12.164456 jlrpy-1.4.1/setup.cfg
--rw-rw-r--   0 eho       (1000) eho       (1000)      713 2021-12-21 18:46:37.000000 jlrpy-1.4.1/setup.py
+drwxr-xr-x   0 vscode    (1000) vscode    (1000)        0 2023-07-23 18:38:04.819311 jlrpy-1.5.0/
+-rw-r--r--   0 vscode    (1000) vscode    (1000)     1063 2023-07-22 16:29:07.000000 jlrpy-1.5.0/LICENSE
+-rw-r--r--   0 vscode    (1000) vscode    (1000)     5319 2023-07-23 18:38:04.818311 jlrpy-1.5.0/PKG-INFO
+-rw-r--r--   0 vscode    (1000) vscode    (1000)     4825 2023-07-22 16:29:07.000000 jlrpy-1.5.0/README.md
+drwxr-xr-x   0 vscode    (1000) vscode    (1000)        0 2023-07-23 18:38:04.818311 jlrpy-1.5.0/jlrpy.egg-info/
+-rw-r--r--   0 vscode    (1000) vscode    (1000)     5319 2023-07-23 18:38:04.000000 jlrpy-1.5.0/jlrpy.egg-info/PKG-INFO
+-rw-r--r--   0 vscode    (1000) vscode    (1000)      179 2023-07-23 18:38:04.000000 jlrpy-1.5.0/jlrpy.egg-info/SOURCES.txt
+-rw-r--r--   0 vscode    (1000) vscode    (1000)        1 2023-07-23 18:38:04.000000 jlrpy-1.5.0/jlrpy.egg-info/dependency_links.txt
+-rw-r--r--   0 vscode    (1000) vscode    (1000)       17 2023-07-23 18:38:04.000000 jlrpy-1.5.0/jlrpy.egg-info/requires.txt
+-rw-r--r--   0 vscode    (1000) vscode    (1000)        6 2023-07-23 18:38:04.000000 jlrpy-1.5.0/jlrpy.egg-info/top_level.txt
+-rwxr-xr-x   0 vscode    (1000) vscode    (1000)    29200 2023-07-23 18:30:44.000000 jlrpy-1.5.0/jlrpy.py
+-rw-r--r--   0 vscode    (1000) vscode    (1000)       38 2023-07-23 18:38:04.819311 jlrpy-1.5.0/setup.cfg
+-rw-r--r--   0 vscode    (1000) vscode    (1000)      749 2023-07-23 18:36:57.000000 jlrpy-1.5.0/setup.py
```

### Comparing `jlrpy-1.4.1/LICENSE` & `jlrpy-1.5.0/LICENSE`

 * *Files identical despite different names*

### Comparing `jlrpy-1.4.1/PKG-INFO` & `jlrpy-1.5.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,16 +1,14 @@
 Metadata-Version: 2.1
 Name: jlrpy
-Version: 1.4.1
+Version: 1.5.0
 Summary: Control your Jaguar I-Pace
 Home-page: https://github.com/ardevd/jlrpy
 Author: Edvard
 Author-email: 5gk633atf@relay.firefox.com
-License: UNKNOWN
-Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Classifier: Intended Audience :: Developers
 Classifier: Development Status :: 5 - Production/Stable
 Description-Content-Type: text/markdown
 License-File: LICENSE
@@ -133,9 +131,7 @@
 The examples directory contains example scripts that put jlrpy to good use. 
 
 ### max_min_soc.py
 The `max_min_soc.py` script allows you to specify a desired maximum and minimum state of charge for the vehicle. Charging will be stopped once the maximum state of charge is reached and it will be started if the minimum state of charge is reached. 
 
 ### charge_offpeak.py
 The `charge_offpeak.py` script allows you to specify a desired (off-peak) charging time period and maximum state of charge for the vehicle. Charging will be stopped if the vehicle is charging outside of the specified time period or once the maximum state of charge is reached and it will be started during the specified time period if the state of charge is below the maximum.
-
-
```

### Comparing `jlrpy-1.4.1/README.md` & `jlrpy-1.5.0/README.md`

 * *Files identical despite different names*

### Comparing `jlrpy-1.4.1/jlrpy.egg-info/PKG-INFO` & `jlrpy-1.5.0/jlrpy.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,16 +1,14 @@
 Metadata-Version: 2.1
 Name: jlrpy
-Version: 1.4.1
+Version: 1.5.0
 Summary: Control your Jaguar I-Pace
 Home-page: https://github.com/ardevd/jlrpy
 Author: Edvard
 Author-email: 5gk633atf@relay.firefox.com
-License: UNKNOWN
-Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
 Classifier: Intended Audience :: Developers
 Classifier: Development Status :: 5 - Production/Stable
 Description-Content-Type: text/markdown
 License-File: LICENSE
@@ -133,9 +131,7 @@
 The examples directory contains example scripts that put jlrpy to good use. 
 
 ### max_min_soc.py
 The `max_min_soc.py` script allows you to specify a desired maximum and minimum state of charge for the vehicle. Charging will be stopped once the maximum state of charge is reached and it will be started if the minimum state of charge is reached. 
 
 ### charge_offpeak.py
 The `charge_offpeak.py` script allows you to specify a desired (off-peak) charging time period and maximum state of charge for the vehicle. Charging will be stopped if the vehicle is charging outside of the specified time period or once the maximum state of charge is reached and it will be started during the specified time period if the state of charge is below the maximum.
-
-
```

### Comparing `jlrpy-1.4.1/jlrpy.py` & `jlrpy-1.5.0/jlrpy.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,25 +1,40 @@
 """ Simple Python class to access the JLR Remote Car API
 https://github.com/ardevd/jlrpy
 """
 
-from urllib.request import Request, build_opener
 
-import json
-import datetime
 import calendar
-import uuid
-import sys
+import json
 import logging
+import time
+import uuid
+from datetime import datetime
+
+import requests
+from requests.exceptions import HTTPError
 
 logger = logging.getLogger('jlrpy')
 
-IFAS_BASE_URL = "https://ifas.prod-row.jlrmotor.com/ifas/jlr"
-IFOP_BASE_ULR = "https://ifop.prod-row.jlrmotor.com/ifop/jlr"
-IF9_BASE_URL = "https://if9.prod-row.jlrmotor.com/if9/jlr"
+
+class BaseURLs:
+    """Rest Of World Base URLs"""
+    IFAS = "https://ifas.prod-row.jlrmotor.com/ifas/jlr"
+    IFOP = "https://ifop.prod-row.jlrmotor.com/ifop/jlr"
+    IF9 = "https://if9.prod-row.jlrmotor.com/if9/jlr"
+
+
+class ChinaBaseURLs:
+    """China Base URLs"""
+    IFAS = "https://ifas.prod-chn.jlrmotor.com/ifas/jlr"
+    IFOP = "https://ifop.prod-chn.jlrmotor.com/ifop/jlr"
+    IF9 = "https://ifoa.prod-chn.jlrmotor.com/if9/jlr"
+
+
+TIMEOUT = 15
 
 
 class Connection:
     """Connection to the JLR Remote Car API"""
 
     def __init__(self,
                  email='',
@@ -29,23 +44,27 @@
                  use_china_servers=False):
         """Init the connection object
 
         The email address and password associated with your Jaguar InControl account is required.
         A device Id can optionally be specified. If not one will be generated at runtime.
         A refresh token can be supplied for authentication instead of a password
         """
-        self.email = email
+        self.email: str = email
+        self.expiration: int = 0  # force credential refresh
+        self.access_token: str
+        self.auth_token: str
+        self.head: dict = {}
+        self.refresh_token: str
+        self.user_id: str
+        self.vehicles: list = []
 
         if use_china_servers:
-            global IFAS_BASE_URL
-            IFAS_BASE_URL = "https://ifas.prod-chn.jlrmotor.com/ifas/jlr"
-            global IFOP_BASE_ULR
-            IFOP_BASE_ULR = "https://ifop.prod-chn.jlrmotor.com/ifop/jlr"
-            global IF9_BASE_URL
-            IF9_BASE_URL = "https://ifoa.prod-chn.jlrmotor.com/if9/jlr"
+            self.base = ChinaBaseURLs
+        else:
+            self.base = BaseURLs
 
         if device_id:
             self.device_id = device_id
         else:
             self.device_id = str(uuid.uuid4())
 
         if refresh_token:
@@ -54,147 +73,158 @@
                 "refresh_token": refresh_token}
         else:
             self.oauth = {
                 "grant_type": "password",
                 "username": email,
                 "password": password}
 
-        self.expiration = 0  # force credential refresh
-
         self.connect()
 
-        self.vehicles = []
         try:
-            for v in self.get_vehicles(self.head)['vehicles']:
-                self.vehicles.append(Vehicle(v, self))
+            for vehicle in self.get_vehicles(self.head)['vehicles']:
+                self.vehicles.append(Vehicle(vehicle, self))
         except TypeError:
             logger.error("No vehicles associated with this account")
 
+    def validate_token(self):
+        """Is token still valid"""
+        now = calendar.timegm(datetime.now().timetuple())
+        if now > self.expiration:
+            # Auth expired, reconnect
+            self.connect()
+
     def get(self, command, url, headers):
         """GET data from API"""
-        return self.post(command, url, headers, None)
+        self.validate_token()
+        if headers['Authorization']:
+            headers['Authorization'] = self.head['Authorization']
+        return self._request(f"{url}/{command}", headers=headers, method="GET")
 
     def post(self, command, url, headers, data=None):
         """POST data to API"""
-        now = calendar.timegm(datetime.datetime.now().timetuple())
-        logger.debug(url)
-        if now > self.expiration:
-            # Auth expired, reconnect
-            self.connect()
-            if headers['Authorization']:
-                headers['Authorization'] = self.head['Authorization']
-        return self.__open("%s/%s" % (url, command), headers=headers, data=data)
+        self.validate_token()
+        if headers['Authorization']:
+            headers['Authorization'] = self.head['Authorization']
+        return self._request(f"{url}/{command}", headers=headers, data=data, method="POST")
+
+    def delete(self, command, url, headers):
+        """DELETE data from api"""
+        self.validate_token()
+        if headers['Authorization']:
+            headers['Authorization'] = self.head['Authorization']
+        if headers["Accept"]:
+            del headers["Accept"]
+        return self._request(url=f"{url}/{command}", headers=headers, method="DELETE")
 
     def connect(self):
+        """Connect to JLR API"""
         logger.info("Connecting...")
-        auth = self.__authenticate(data=self.oauth)
-        self.__register_auth(auth)
-        self.__set_header(auth['access_token'])
+        auth = self._authenticate(data=self.oauth)
+        self._register_auth(auth)
+        self._set_header(auth['access_token'])
         logger.info("[+] authenticated")
-        self.__register_device_and_log_in()
+        self._register_device_and_log_in()
 
-    def __register_device_and_log_in(self):
-        self.__register_device(self.head)
+    def _register_device_and_log_in(self):
+        self._register_device(self.head)
         logger.info("1/2 device id registered")
-        self.__login_user(self.head)
+        self._login_user(self.head)
         logger.info("2/2 user logged in, user id retrieved")
 
-    def __open(self, url, headers=None, data=None):
-        req = Request(url, headers=headers)
-        if data:
-            req.data = bytes(json.dumps(data), encoding="utf8")
-
-        opener = build_opener()
-        resp = opener.open(req)
-        charset = resp.info().get('charset', 'utf-8')
-        resp_data = resp.read().decode(charset)
-        if resp_data:
-            return json.loads(resp_data)
-        else:
-            return None
+    def _request(self, url, headers=None, data=None, method="GET"):
+        print(f"URL: {url} \nHEADERS: {headers} \nDATA: {data} \nMETHOD: {method}")
+        ret = requests.request(method=method, url=url, headers=headers, json=data, timeout=TIMEOUT)
+        print(ret.text)
+        if ret.text:
+            try:
+                return json.loads(ret.text)
+            except json.JSONDecodeError:
+                return None
+        return None
 
-    def __register_auth(self, auth):
+    def _register_auth(self, auth):
         self.access_token = auth['access_token']
-        now = calendar.timegm(datetime.datetime.now().timetuple())
+        now = calendar.timegm(datetime.now().timetuple())
         self.expiration = now + int(auth['expires_in'])
         self.auth_token = auth['authorization_token']
         self.refresh_token = auth['refresh_token']
 
-    def __set_header(self, access_token):
+    def _set_header(self, access_token):
         """Set HTTP header fields"""
         self.head = {
-            "Authorization": "Bearer %s" % access_token,
+            "Authorization": f"Bearer {access_token}",
             "X-Device-Id": self.device_id,
             "x-telematicsprogramtype": "jlrpy",
             "Content-Type": "application/json"}
 
-    def __authenticate(self, data=None):
+    def _authenticate(self, data=None):
         """Raw urlopen command to the auth url"""
-        url = "%s/tokens" % IFAS_BASE_URL
+        url = f"{self.base.IFAS}/tokens"
         auth_headers = {
             "Authorization": "Basic YXM6YXNwYXNz",
             "Content-Type": "application/json",
             "X-Device-Id": self.device_id}
 
-        return self.__open(url, auth_headers, data)
+        return self._request(url, auth_headers, data, "POST")
 
-    def __register_device(self, headers=None):
+    def _register_device(self, headers=None):
         """Register the device Id"""
-        url = "%s/users/%s/clients" % (IFOP_BASE_ULR, self.email)
+        url = f"{self.base.IFOP}/users/{self.email}/clients"
         data = {
             "access_token": self.access_token,
             "authorization_token": self.auth_token,
             "expires_in": "86400",
             "deviceID": self.device_id
         }
 
-        return self.__open(url, headers, data)
+        return self._request(url, headers, data, "POST")
 
-    def __login_user(self, headers=None):
+    def _login_user(self, headers=None):
         """Login the user"""
-        url = "%s/users?loginName=%s" % (IF9_BASE_URL, self.email)
+        url = f"{self.base.IF9}/users?loginName={self.email}"
         user_login_header = headers.copy()
         user_login_header["Accept"] = "application/vnd.wirelesscar.ngtp.if9.User-v3+json"
 
-        user_data = self.__open(url, user_login_header)
+        user_data = self._request(url, user_login_header)
         self.user_id = user_data['userId']
         return user_data
 
     def refresh_tokens(self):
         """Refresh tokens."""
         self.oauth = {
             "grant_type": "refresh_token",
             "refresh_token": self.refresh_token}
 
-        auth = self.__authenticate(self.oauth)
-        self.__register_auth(auth)
-        self.__set_header(auth['access_token'])
+        auth = self._authenticate(self.oauth)
+        self._register_auth(auth)
+        self._set_header(auth['access_token'])
         logger.info("[+] Tokens refreshed")
-        self.__register_device_and_log_in()
+        self._register_device_and_log_in()
 
     def get_vehicles(self, headers):
         """Get vehicles for user"""
-        url = "%s/users/%s/vehicles?primaryOnly=true" % (IF9_BASE_URL, self.user_id)
-        return self.__open(url, headers)
+        url = f"{self.base.IF9}/users/{self.user_id}/vehicles?primaryOnly=true"
+        return self._request(url, headers)
 
     def get_user_info(self):
         """Get user information"""
-        return self.get(self.user_id, "%s/users" % IF9_BASE_URL, self.head)
+        headers = self.head.copy()
+        headers["Accept"] = "application/vnd.wirelesscar.ngtp.if9.User-v3+json"
+        headers["Content-Type"] = "application/json"
+        return self.get(self.user_id, f"{self.base.IF9}/users", self.head)
 
     def update_user_info(self, user_info_data):
         """Update user information"""
         headers = self.head.copy()
         headers["Content-Type"] = "application/vnd.wirelesscar.ngtp.if9.User-v3+json; charset=utf-8"
-        return self.post(self.user_id, "%s/users" % IF9_BASE_URL, headers, user_info_data)
+        return self.post(self.user_id, f"{self.base.IF9}/users", headers, user_info_data)
 
     def reverse_geocode(self, lat, lon):
         """Get geocode information"""
-        return self.get("en",
-                        "%s/geocode/reverse/{0:f}/{1:f}".format(lat, lon) % IF9_BASE_URL,
-                        self.head)
+        return self.get("en", f"{self.base.IF9}/geocode/reverse/{lat}/{lon}", self.head)
 
 
 class Vehicle(dict):
     """Vehicle class.
 
     You can request data or send commands to vehicle. Consult the JLR API documentation for details
     """
@@ -205,41 +235,41 @@
         super().__init__(data)
         self.connection = connection
         self.vin = data['vin']
 
     def get_contact_info(self, mcc):
         """ Get contact info for the specified mobile country code"""
         headers = self.connection.head.copy()
-        return self.get('contactinfo/%s' % mcc, headers)
+        return self.get(f"contactinfo/{mcc}", headers)
 
     def get_attributes(self):
         """Get vehicle attributes"""
         headers = self.connection.head.copy()
-        headers["Accept"] = "application/vnd.ngtp.org.VehicleAttributes-v3+json"
+        headers["Accept"] = "application/vnd.ngtp.org.VehicleAttributes-v8+json"
         return self.get('attributes', headers)
 
     def get_status(self, key=None):
         """Get vehicle status"""
         headers = self.connection.head.copy()
-        headers["Accept"] = "application/vnd.ngtp.org.if9.healthstatus-v3+json"
+        headers["Accept"] = "application/vnd.ngtp.org.if9.healthstatus-v4+json"
         result = self.get('status?includeInactive=true', headers)
 
         if key:
-            coreStatusList = result['vehicleStatus']['coreStatus']
-            evStatusList = result['vehicleStatus']['evStatus']
-            coreStatusList = coreStatusList + evStatusList
-            return {d['key']: d['value'] for d in coreStatusList}[key]
+            core_status = result['vehicleStatus']['coreStatus']
+            ev_status = result['vehicleStatus']['evStatus']
+            core_status = core_status + ev_status
+            return {d['key']: d['value'] for d in core_status}[key]
 
         return result
 
     def get_health_status(self):
         """Get vehicle health status"""
         headers = self.connection.head.copy()
         headers["Accept"] = "application/vnd.wirelesscar.ngtp.if9.ServiceStatus-v4+json"
-        headers["Content-Type"] = "application/vnd.wirelesscar.ngtp.if9.StartServiceConfiguration-v3+json; charset=utf-8"
+        headers["Content-Type"] = "application/vnd.wirelesscar.ngtp.if9.StartServiceConfiguration-v3+json; charset=utf-8"  # noqa: E501, pylint: disable=line-too-long
 
         vhs_data = self._authenticate_vhs()
 
         return self.post('healthstatus', headers, vhs_data)
 
     def get_departure_timers(self):
         """Get vehicle departure timers"""
@@ -258,15 +288,15 @@
         result = self.get('subscriptionpackages', self.connection.head)
         return result
 
     def get_trips(self, count=1000):
         """Get the last 1000 trips associated with vehicle"""
         headers = self.connection.head.copy()
         headers["Accept"] = "application/vnd.ngtp.org.triplist-v2+json"
-        return self.get('trips?count=%d' % count, headers)
+        return self.get(f"trips?count={count}", headers)
 
     def get_guardian_mode_alarms(self):
         """Get Guardian Mode Alarms"""
         headers = self.connection.head.copy()
         headers["Accept"] = "application/vnd.wirelesscar.ngtp.if9.GuardianStatus-v1+json"
         headers["Accept-Encoding"] = "gzip,deflate"
         return self.get('gm/alarms', headers)
@@ -294,35 +324,38 @@
         """Get Guardian Mode System Settings"""
         headers = self.connection.head.copy()
         headers["Accept"] = "application/vnd.wirelesscar.ngtp.if9.GuardianSystemSettings-v1+json"
         return self.get('gm/settings/system', headers)
 
     def get_trip(self, trip_id, section=1):
         """Get info on a specific trip"""
-        return self.get('trips/%s/route?pageSize=1000&page=%d' % (trip_id, section), self.connection.head)
+        return self.get(f"trips/{trip_id}/route?pageSize=1000&page={section}", self.connection.head)
 
     def get_position(self):
         """Get current vehicle position"""
         return self.get('position', self.connection.head)
 
     def get_service_status(self, service_id):
         """Get service status"""
         headers = self.connection.head.copy()
         headers["Accept"] = "application/vnd.wirelesscar.ngtp.if9.ServiceStatus-v4+json"
-        return self.get('services/%s' % service_id, headers)
+        return self.get(f"services/{service_id}", headers)
 
     def get_services(self):
         """Get active services"""
         headers = self.connection.head.copy()
         return self.get("services", headers)
 
     def get_rcc_target_value(self):
         """Get Remote Climate Target Value"""
         headers = self.connection.head.copy()
-        return self.get('settings/ClimateControlRccTargetTemp', headers)
+        try:
+            return self.get('settings/ClimateControlRccTargetTemp', headers)
+        except HTTPError:
+            return None
 
     def set_attributes(self, nickname, registration_number):
         """Set vehicle nickname and registration number"""
         attributes_data = {"nickname": nickname,
                            "registrationNumber": registration_number}
         return self.post("attributes", self.connection.head, attributes_data)
 
@@ -341,25 +374,25 @@
         rdu_data = self.authenticate_rdu(pin)
 
         return self.post("unlock", headers, rdu_data)
 
     def reset_alarm(self, pin):
         """Reset vehicle alarm"""
         headers = self.connection.head.copy()
-        headers["Content-Type"] = "application/vnd.wirelesscar.ngtp.if9.StartServiceConfiguration-v3+json; charset=utf-8"
+        headers["Content-Type"] = "application/vnd.wirelesscar.ngtp.if9.StartServiceConfiguration-v3+json; charset=utf-8"  # noqa: E501, pylint: disable=line-too-long
         headers["Accept"] = "application/vnd.wirelesscar.ngtp.if9.ServiceStatus-v4+json"
         aloff_data = self.authenticate_aloff(pin)
 
         return self.post("unlock", headers, aloff_data)
 
     def honk_blink(self):
         """Sound the horn and blink lights"""
         headers = self.connection.head.copy()
         headers["Accept"] = "application/vnd.wirelesscar.ngtp.if9.ServiceStatus-v4+json"
-        headers["Content-Type"] = "application/vnd.wirelesscar.ngtp.if9.StartServiceConfiguration-v3+json; charset=utf-8"
+        headers["Content-Type"] = "application/vnd.wirelesscar.ngtp.if9.StartServiceConfiguration-v3+json; charset=utf-8"  # noqa: E501, pylint: disable=line-too-long
 
         hblf_data = self.authenticate_hblf()
         return self.post("honkBlink", headers, hblf_data)
 
     def remote_engine_start(self, pin, target_value):
         """Start Remote Engine preconditioning"""
         headers = self.connection.head.copy()
@@ -377,38 +410,44 @@
 
         return self.post("engineOff", headers, reoff_data)
 
     def set_rcc_target_value(self, pin, target_value):
         """Set Remote Climate Target Value (value between 31-57, 31 is LO 57 is HOT)"""
         headers = self.connection.head.copy()
         self.enable_provisioning_mode(pin)
-        service_parameters = {"key": "ClimateControlRccTargetTemp",
-                               "value": "%s" % str(target_value),
-                               "applied": 1}
+        service_parameters = {
+            "key": "ClimateControlRccTargetTemp",
+            "value": str(target_value),
+            "applied": 1
+        }
         self.post("settings", headers, service_parameters)
 
+    def get_waua_status(self):
+        """Get WAUA status."""
+        headers = self.connection.head.copy()
+        headers["Accept"] = "application/wirelesscar.WauaStatus-v1+json"
+        return self.get("waua/status", headers)
+
     def preconditioning_start(self, target_temp):
         """Start pre-conditioning for specified temperature (celsius)"""
-        service_parameters = [{"key": "PRECONDITIONING",
-                               "value": "START"},
-                              {"key": "TARGET_TEMPERATURE_CELSIUS",
-                               "value": "%s" % target_temp}]
-
+        service_parameters = [
+            {"key": "PRECONDITIONING", "value": "START"},
+            {"key": "TARGET_TEMPERATURE_CELSIUS", "value": str(target_temp)}
+        ]
         return self._preconditioning_control(service_parameters)
 
     def preconditioning_stop(self):
         """Stop climate preconditioning"""
         service_parameters = [{"key": "PRECONDITIONING",
                                "value": "STOP"}]
         return self._preconditioning_control(service_parameters)
 
     def climate_prioritize(self, priority):
         """Optimize climate controls for comfort or range"""
-        service_parameters = [{"key": "PRIORITY_SETTING",
-                               "value": "%s" % priority}]
+        service_parameters = [{"key": "PRIORITY_SETTING", "value": priority}]
         return self._preconditioning_control(service_parameters)
 
     def _preconditioning_control(self, service_parameters):
         """Control the climate preconditioning"""
         headers = self.connection.head.copy()
         headers["Accept"] = "application/vnd.wirelesscar.ngtp.if9.ServiceStatus-v5+json"
         headers["Content-Type"] = "application/vnd.wirelesscar.ngtp.if9.PhevService-v1+json; charset=utf-8"
@@ -517,33 +556,46 @@
         swu_data["serviceCommand"] = "END"
         return self._swu(swu_data)
 
     def _swu(self, swu_data):
         """Set the wakeup time for the specified time (epoch milliseconds)"""
         headers = self.connection.head.copy()
         headers["Accept"] = "application/vnd.wirelesscar.ngtp.if9.ServiceStatus-v3+json"
-        headers["Content-Type"] = "application/vnd.wirelesscar.ngtp.if9.StartServiceConfiguration-v3+json; charset=utf-8"
+        headers["Content-Type"] = "application/vnd.wirelesscar.ngtp.if9.StartServiceConfiguration-v3+json; charset=utf-8"  # noqa: E501, pylint: disable=line-too-long
         return self.post("swu", headers, swu_data)
 
     def enable_provisioning_mode(self, pin):
         """Enable provisioning mode """
         self._prov_command(pin, None, "provisioning")
 
     def enable_service_mode(self, pin, expiration_time):
         """Enable service mode. Will disable at the specified time (epoch millis)"""
         return self._prov_command(pin, expiration_time, "protectionStrategy_serviceMode")
 
+    def disable_service_mode(self, pin):
+        """Disable service mode."""
+        exp = int(time.time() * 1000)
+        return self._prov_command(pin, exp, "protectionStrategy_serviceMode")
+
     def enable_guardian_mode(self, pin, expiration_time):
         """Enable Guardian Mode until the specified time (epoch millis)"""
-        return self._gm_command(pin, expiration_time, "ACTIVE")
+        return self._gm_command(pin, expiration_time, "ACTIVATE")
+
+    def disable_guardian_mode(self, pin):
+        """Disable Guardian Mode"""
+        return self._gm_command(pin, 0, "DEACTIVATE")
 
     def enable_transport_mode(self, pin, expiration_time):
         """Enable transport mode. Will be disabled at the specified time (epoch millis)"""
         return self._prov_command(pin, expiration_time, "protectionStrategy_transportMode")
 
+    def disable_transport_mode(self, pin):
+        """Disable transport mode"""
+        return self._prov_command(pin, None, "protectionStrategy_transportMode")
+
     def enable_privacy_mode(self, pin):
         """Enable privacy mode. Will disable journey logging"""
         return self._prov_command(pin, None, "privacySwitch_on")
 
     def disable_privacy_mode(self, pin):
         """Disable privacy mode. Will enable journey logging"""
         return self._prov_command(pin, None, "privacySwitch_off")
@@ -556,23 +608,26 @@
 
         prov_data["serviceCommand"] = mode
         prov_data["startTime"] = None
         prov_data["endTime"] = expiration_time
 
         return self.post("prov", headers, prov_data)
 
-    def _gm_command(self, pin, expiration_time, status):
+    def _gm_command(self, pin, expiration_time, action):
         """Send GM toggle command"""
         headers = self.connection.head.copy()
         headers["Accept"] = "application/vnd.wirelesscar.ngtp.if9.GuardianAlarmList-v1+json"
         gm_data = self.authenticate_gm(pin)
-        gm_data["endTime"] = expiration_time
-        gm_data["status"] = status
-
-        return self.post("gm/alarms", headers, gm_data)
+        if action == "ACTIVATE":
+            gm_data["endTime"] = expiration_time
+            gm_data["status"] = "ACTIVE"
+            return self.post("gm/alarms", headers, gm_data)
+        if action == "DEACTIVATE":
+            headers["X-servicetoken"] = gm_data.get("token")
+            return self.delete("gm/alarms/INSTANT", headers)
 
     def _authenticate_vhs(self):
         """Authenticate to vhs and get token"""
         return self._authenticate_empty_pin_protected_service("VHS")
 
     def _authenticate_empty_pin_protected_service(self, service_name):
         return self._authenticate_service("", service_name)
@@ -618,27 +673,31 @@
         return self._authenticate_service(pin, "REOFF")
 
     def authenticate_prov(self, pin):
         """Authenticate to PROV service"""
         return self._authenticate_service(pin, "PROV")
 
     def authenticate_gm(self, pin):
+        """Authenticate to GM service"""
         return self._authenticate_service(pin, "GM")
 
     def _authenticate_service(self, pin, service_name):
         """Authenticate to specified service with the provided PIN"""
         data = {
-            "serviceName": "%s" % service_name,
-            "pin": "%s" % pin}
+            "serviceName": service_name,
+            "pin": str(pin)
+        }
         headers = self.connection.head.copy()
         headers["Content-Type"] = "application/vnd.wirelesscar.ngtp.if9.AuthenticateRequest-v2+json; charset=utf-8"
+        return self.post(f"users/{self.connection.user_id}/authenticate", headers, data)
 
-        return self.post("users/%s/authenticate" % self.connection.user_id, headers, data)
+    def get(self, command, headers):
+        """Utility command to get vehicle data from API"""
+        return self.connection.get(command, f"{self.connection.base.IF9}/vehicles/{self.vin}", headers)
 
     def post(self, command, headers, data):
         """Utility command to post data to VHS"""
-        return self.connection.post(command, '%s/vehicles/%s' % (IF9_BASE_URL, self.vin),
-                                    headers, data)
+        return self.connection.post(command, f"{self.connection.base.IF9}/vehicles/{self.vin}", headers, data)
 
-    def get(self, command, headers):
-        """Utility command to get vehicle data from API"""
-        return self.connection.get(command, '%s/vehicles/%s' % (IF9_BASE_URL, self.vin), headers)
+    def delete(self, command, headers):
+        """Utility command to delete active service entry"""
+        return self.connection.delete(command, f"{self.connection.base.IF9}/vehicles/{self.vin}", headers)
```

### Comparing `jlrpy-1.4.1/setup.py` & `jlrpy-1.5.0/setup.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,24 +1,24 @@
 import setuptools
 
 
-with open("README.md", "r") as fh:
+with open("README.md", "r", encoding='UTF-8') as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="jlrpy",
-    version="1.4.1",
+    version="1.5.0",
     author="Edvard",
     author_email="5gk633atf@relay.firefox.com",
     description="Control your Jaguar I-Pace",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/ardevd/jlrpy",
     py_modules=['jlrpy'],
-    install_requires=[],
+    install_requires=['requests>=2.26.0'],
     classifiers=[
         "Programming Language :: Python :: 3",
         "License :: OSI Approved :: MIT License",
         "Operating System :: OS Independent",
         "Intended Audience :: Developers",
         "Development Status :: 5 - Production/Stable",
     ],
```

