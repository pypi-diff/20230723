# Comparing `tmp/volvopy-0.1.8.tar.gz` & `tmp/volvopy-0.1.9.tar.gz`

## Comparing `volvopy-0.1.8.tar` & `volvopy-0.1.9.tar`

### file list

```diff
@@ -1,24 +1,24 @@
--rwxr-xr-x   0        0        0      214 2020-02-02 00:00:00.000000 volvopy-0.1.8/.editorconfig
--rw-r--r--   0        0        0     2579 2020-02-02 00:00:00.000000 volvopy-0.1.8/BUILDING.md
--rwxr-xr-x   0        0        0     2157 2020-02-02 00:00:00.000000 volvopy-0.1.8/mkbld
--rw-r--r--   0        0        0       31 2020-02-02 00:00:00.000000 volvopy-0.1.8/requirements.txt
--rw-r--r--   0        0        0      618 2020-02-02 00:00:00.000000 volvopy-0.1.8/tox.ini
--rw-r--r--   0        0        0      502 2020-02-02 00:00:00.000000 volvopy-0.1.8/.github/dependabot.yml
--rwxr-xr-x   0        0        0     1867 2020-02-02 00:00:00.000000 volvopy-0.1.8/examples/demo.py
--rwxr-xr-x   0        0        0    18668 2020-02-02 00:00:00.000000 volvopy-0.1.8/examples/omed.py
--rwxr-xr-x   0        0        0     1800 2020-02-02 00:00:00.000000 volvopy-0.1.8/src/volvopy/__constants__.py
--rwxr-xr-x   0        0        0      148 2020-02-02 00:00:00.000000 volvopy-0.1.8/src/volvopy/__init__.py
--rw-r--r--   0        0        0     1057 2020-02-02 00:00:00.000000 volvopy-0.1.8/src/volvopy/connected.py
--rw-r--r--   0        0        0      977 2020-02-02 00:00:00.000000 volvopy-0.1.8/src/volvopy/energy.py
--rw-r--r--   0        0        0     1057 2020-02-02 00:00:00.000000 volvopy-0.1.8/src/volvopy/extended.py
--rw-r--r--   0        0        0      983 2020-02-02 00:00:00.000000 volvopy-0.1.8/src/volvopy/location.py
--rw-r--r--   0        0        0     2408 2020-02-02 00:00:00.000000 volvopy-0.1.8/src/volvopy/volvo_api.py
--rw-r--r--   0        0        0   377649 2020-02-02 00:00:00.000000 volvopy-0.1.8/src/volvopy/specification/connected-vehicle-c3-specification.v1.json
--rw-r--r--   0        0        0    56534 2020-02-02 00:00:00.000000 volvopy-0.1.8/src/volvopy/specification/energy-api-specification.v1.json
--rw-r--r--   0        0        0    23483 2020-02-02 00:00:00.000000 volvopy-0.1.8/src/volvopy/specification/extended-vehicle-c3-specification.v1.json
--rw-r--r--   0        0        0    11391 2020-02-02 00:00:00.000000 volvopy-0.1.8/src/volvopy/specification/location-specification.v1.json
--rwxr-xr-x   0        0        0     1906 2020-02-02 00:00:00.000000 volvopy-0.1.8/.gitignore
--rw-r--r--   0        0        0     1084 2020-02-02 00:00:00.000000 volvopy-0.1.8/LICENSE
--rw-r--r--   0        0        0      672 2020-02-02 00:00:00.000000 volvopy-0.1.8/README.md
--rw-r--r--   0        0        0      957 2020-02-02 00:00:00.000000 volvopy-0.1.8/pyproject.toml
--rw-r--r--   0        0        0     1413 2020-02-02 00:00:00.000000 volvopy-0.1.8/PKG-INFO
+-rwxr-xr-x   0        0        0      214 2020-02-02 00:00:00.000000 volvopy-0.1.9/.editorconfig
+-rw-r--r--   0        0        0     2579 2020-02-02 00:00:00.000000 volvopy-0.1.9/BUILDING.md
+-rwxr-xr-x   0        0        0     2157 2020-02-02 00:00:00.000000 volvopy-0.1.9/mkbld
+-rw-r--r--   0        0        0       31 2020-02-02 00:00:00.000000 volvopy-0.1.9/requirements.txt
+-rw-r--r--   0        0        0      618 2020-02-02 00:00:00.000000 volvopy-0.1.9/tox.ini
+-rw-r--r--   0        0        0      502 2020-02-02 00:00:00.000000 volvopy-0.1.9/.github/dependabot.yml
+-rwxr-xr-x   0        0        0     1866 2020-02-02 00:00:00.000000 volvopy-0.1.9/examples/demo.py
+-rwxr-xr-x   0        0        0    18668 2020-02-02 00:00:00.000000 volvopy-0.1.9/examples/omed.py
+-rwxr-xr-x   0        0        0     1936 2020-02-02 00:00:00.000000 volvopy-0.1.9/src/volvopy/__constants__.py
+-rwxr-xr-x   0        0        0      148 2020-02-02 00:00:00.000000 volvopy-0.1.9/src/volvopy/__init__.py
+-rw-r--r--   0        0        0     1293 2020-02-02 00:00:00.000000 volvopy-0.1.9/src/volvopy/connected.py
+-rw-r--r--   0        0        0     1134 2020-02-02 00:00:00.000000 volvopy-0.1.9/src/volvopy/energy.py
+-rw-r--r--   0        0        0     1142 2020-02-02 00:00:00.000000 volvopy-0.1.9/src/volvopy/extended.py
+-rw-r--r--   0        0        0     1068 2020-02-02 00:00:00.000000 volvopy-0.1.9/src/volvopy/location.py
+-rw-r--r--   0        0        0     2828 2020-02-02 00:00:00.000000 volvopy-0.1.9/src/volvopy/volvo_api.py
+-rw-r--r--   0        0        0   377649 2020-02-02 00:00:00.000000 volvopy-0.1.9/src/volvopy/specification/connected-vehicle-c3-specification.v1.json
+-rw-r--r--   0        0        0    56534 2020-02-02 00:00:00.000000 volvopy-0.1.9/src/volvopy/specification/energy-api-specification.v1.json
+-rw-r--r--   0        0        0    23483 2020-02-02 00:00:00.000000 volvopy-0.1.9/src/volvopy/specification/extended-vehicle-c3-specification.v1.json
+-rw-r--r--   0        0        0    11391 2020-02-02 00:00:00.000000 volvopy-0.1.9/src/volvopy/specification/location-specification.v1.json
+-rwxr-xr-x   0        0        0     1906 2020-02-02 00:00:00.000000 volvopy-0.1.9/.gitignore
+-rw-r--r--   0        0        0     1084 2020-02-02 00:00:00.000000 volvopy-0.1.9/LICENSE
+-rw-r--r--   0        0        0     1262 2020-02-02 00:00:00.000000 volvopy-0.1.9/README.md
+-rw-r--r--   0        0        0      957 2020-02-02 00:00:00.000000 volvopy-0.1.9/pyproject.toml
+-rw-r--r--   0        0        0     2003 2020-02-02 00:00:00.000000 volvopy-0.1.9/PKG-INFO
```

### Comparing `volvopy-0.1.8/BUILDING.md` & `volvopy-0.1.9/BUILDING.md`

 * *Files identical despite different names*

### Comparing `volvopy-0.1.8/mkbld` & `volvopy-0.1.9/mkbld`

 * *Files identical despite different names*

### Comparing `volvopy-0.1.8/tox.ini` & `volvopy-0.1.9/tox.ini`

 * *Files identical despite different names*

### Comparing `volvopy-0.1.8/examples/demo.py` & `volvopy-0.1.9/examples/demo.py`

 * *Files 0% similar despite different names*

```diff
@@ -10,15 +10,14 @@
 
 pp2 = pprint.PrettyPrinter(sort_dicts=False, indent=1, depth=2)
 DEBUG = True
 MYAPP = volvopy.MYAPP
 MYID = "demo"
 
 
-
 def main():
     """Demonstrate use of the Volvo APIs"""
 
     print(f"Calling: {call_url}\n")
     accept = "application/json"
     headers = {
         "Content-type": "application/json",
```

### Comparing `volvopy-0.1.8/examples/omed.py` & `volvopy-0.1.9/examples/omed.py`

 * *Files identical despite different names*

### Comparing `volvopy-0.1.8/src/volvopy/__constants__.py` & `volvopy-0.1.9/src/volvopy/__constants__.py`

 * *Files 7% similar despite different names*

```diff
@@ -48,16 +48,22 @@
         _data = json.load(_json_file)
     API_SPECIFICATIONS[_key] = _data
 
 # load the configuration file and store the carious keys in constants
 _inifile = configparser.ConfigParser()
 _inifile.read(_api_keys_file)
 API_KEY = [_inifile.get("API", "vcc_primary"), _inifile.get("API", "vcc_secondary")]
-API_TOKEN = _inifile.get("API", "connected_token")
+API_TOKEN = {}
+for _name in API_SPECIFICATIONS:
+    try:
+        API_TOKEN[_name] = _inifile.get("API", f"{_name}_token")
+    except:
+        API_TOKEN[_name] = None
 API_VIN = _inifile.get("API", "vin")
 
 
 if __name__ == "__main__":
     _pp2.pprint(API_SPECIFICATIONS)
     print()
     print(API_KEY)
     print(API_VIN)
+    print(API_TOKEN)
```

### Comparing `volvopy-0.1.8/src/volvopy/connected.py` & `volvopy-0.1.9/src/volvopy/extended.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,36 +1,40 @@
 #!/usr/bin/env python3
 
 import __constants__ as vc
 from volvo_api import VolvoAPI
 import os
 
 import mausy5043_common.funfile as mf
+
 DEBUG = False
 HERE = os.path.realpath(__file__).split("/")
 MYID = HERE[-1]
 
 
-class Connected_Vehicle(VolvoAPI):
-    """Class to connect and interact with the Volvo Connected Vehicle API.
+class Extended_Vehicle(VolvoAPI):
+    """Class to connect and interact with the Volvo Extended Vehicle API.
 
-    ref.: https://developer.volvocars.com/apis/connected-vehicle/v1/specification/
+    ref.:https://developer.volvocars.com/apis/extended-vehicle/v1/specification/
     """
+
     def __init__(self, debug=False):
         super().__init__(debug=debug)
 
-        api = 'connected'
+        api = "extended"
         self.base_url = f"{vc.API_SPECIFICATIONS[api]['servers'][0]['url']}"
         vin = self.vin  # noqa
-        id = "NOT-AVAILABLE"  # noqa
-        for path in vc.API_SPECIFICATIONS[api]['paths']:
+        resource = "NOT-AVAILABLE"  # noqa
+        for path in vc.API_SPECIFICATIONS[api]["paths"]:
             url_path = eval(f"f'{path}'")
             self.call_urls.append(f"{self.base_url}{url_path}")
         print(f"Number of URLs: {len(self.call_urls)}")
         for item in self.call_urls:
             mf.syslog_trace(item, False, DEBUG)
+        if self.api_tokens[api]:
+            self.api_token = self.api_tokens[api]
 
 
 if __name__ == "__main__":
     DEBUG = True
-    a = Connected_Vehicle(debug=DEBUG)
+    a = Extended_Vehicle(debug=DEBUG)
     a.get()
```

### Comparing `volvopy-0.1.8/src/volvopy/energy.py` & `volvopy-0.1.9/src/volvopy/location.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,34 +1,39 @@
 #!/usr/bin/env python3
 
 import __constants__ as vc
 from volvo_api import VolvoAPI
 import os
 
 import mausy5043_common.funfile as mf
+
 DEBUG = False
 HERE = os.path.realpath(__file__).split("/")
 MYID = HERE[-1]
 
 
-class Energy(VolvoAPI):
-    """Class to connect and interact with the Volvo Energy API.
+class Location(VolvoAPI):
+    """Class to connect and interact with the Volvo Location API.
 
-    ref.: https://developer.volvocars.com/apis/energy/v1/specification/
+    ref.: https://developer.volvocars.com/apis/location/v1/specification/
     """
+
     def __init__(self, debug=False):
         super().__init__(debug=debug)
 
-        api = 'energy'
+        api = "location"
         self.base_url = f"{vc.API_SPECIFICATIONS[api]['servers'][0]['url']}"
         vin = self.vin  # noqa
-        for path in vc.API_SPECIFICATIONS[api]['paths']:
+        for path in vc.API_SPECIFICATIONS[api]["paths"]:
             url_path = eval(f"f'{path}'")
             self.call_urls.append(f"{self.base_url}{url_path}")
         print(f"Number of URLs: {len(self.call_urls)}")
         for item in self.call_urls:
-            mf.syslog_trace(f"{item}", False, DEBUG)
+            mf.syslog_trace(item, False, DEBUG)
+        if self.api_tokens[api]:
+            self.api_token = self.api_tokens[api]
+
 
 if __name__ == "__main__":
     DEBUG = True
-    a = Energy(debug=DEBUG)
+    a = Location(debug=DEBUG)
     a.get()
```

### Comparing `volvopy-0.1.8/src/volvopy/extended.py` & `volvopy-0.1.9/src/volvopy/connected.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,36 +1,42 @@
 #!/usr/bin/env python3
 
 import __constants__ as vc
 from volvo_api import VolvoAPI
 import os
 
 import mausy5043_common.funfile as mf
+
 DEBUG = False
 HERE = os.path.realpath(__file__).split("/")
 MYID = HERE[-1]
 
 
-class Extended_Vehicle(VolvoAPI):
-    """Class to connect and interact with the Volvo Extended Vehicle API.
+class Connected_Vehicle(VolvoAPI):
+    """Class to connect and interact with the Volvo Connected Vehicle API.
 
-    ref.:https://developer.volvocars.com/apis/extended-vehicle/v1/specification/
+    ref.: https://developer.volvocars.com/apis/connected-vehicle/v1/specification/
     """
+
     def __init__(self, debug=False):
         super().__init__(debug=debug)
 
-        api = 'extended'
+        api = "connected"
         self.base_url = f"{vc.API_SPECIFICATIONS[api]['servers'][0]['url']}"
         vin = self.vin  # noqa
-        resource = "NOT-AVAILABLE"  # noqa
-        for path in vc.API_SPECIFICATIONS[api]['paths']:
+        id = "NOT-AVAILABLE"  # noqa
+        for path in vc.API_SPECIFICATIONS[api]["paths"]:
             url_path = eval(f"f'{path}'")
             self.call_urls.append(f"{self.base_url}{url_path}")
         print(f"Number of URLs: {len(self.call_urls)}")
         for item in self.call_urls:
             mf.syslog_trace(item, False, DEBUG)
+        if self.api_tokens[api]:
+            self.api_token = self.api_tokens[api]
+        if not self.api_token:
+            raise BaseException("No Token")
 
 
 if __name__ == "__main__":
     DEBUG = True
-    a = Extended_Vehicle(debug=DEBUG)
-    a.get()
+    a = Connected_Vehicle(debug=DEBUG)
+    a.get(accept="application/vnd.volvocars.api.connected-vehicle.vehicledata.v1+json")
```

### Comparing `volvopy-0.1.8/src/volvopy/location.py` & `volvopy-0.1.9/src/volvopy/energy.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,35 +1,40 @@
 #!/usr/bin/env python3
 
 import __constants__ as vc
 from volvo_api import VolvoAPI
 import os
 
 import mausy5043_common.funfile as mf
+
 DEBUG = False
 HERE = os.path.realpath(__file__).split("/")
 MYID = HERE[-1]
 
 
-class Location(VolvoAPI):
-    """Class to connect and interact with the Volvo Location API.
+class Energy(VolvoAPI):
+    """Class to connect and interact with the Volvo Energy API.
 
-    ref.: https://developer.volvocars.com/apis/location/v1/specification/
+    ref.: https://developer.volvocars.com/apis/energy/v1/specification/
     """
+
     def __init__(self, debug=False):
         super().__init__(debug=debug)
 
-        api = 'location'
+        api = "energy"
         self.base_url = f"{vc.API_SPECIFICATIONS[api]['servers'][0]['url']}"
         vin = self.vin  # noqa
-        for path in vc.API_SPECIFICATIONS[api]['paths']:
+        for path in vc.API_SPECIFICATIONS[api]["paths"]:
             url_path = eval(f"f'{path}'")
             self.call_urls.append(f"{self.base_url}{url_path}")
+
         print(f"Number of URLs: {len(self.call_urls)}")
         for item in self.call_urls:
-            mf.syslog_trace(item, False, DEBUG)
+            mf.syslog_trace(f"{item}", False, self.debug)
+        if self.api_tokens[api]:
+            self.api_token = self.api_tokens[api]
 
 
 if __name__ == "__main__":
     DEBUG = True
-    a = Location(debug=DEBUG)
-    a.get()
+    a = Energy(debug=DEBUG)
+    a.get(accept="application/vnd.volvocars.api.energy.vehicledata.v1+json")
```

### Comparing `volvopy-0.1.8/src/volvopy/specification/connected-vehicle-c3-specification.v1.json` & `volvopy-0.1.9/src/volvopy/specification/connected-vehicle-c3-specification.v1.json`

 * *Files identical despite different names*

### Comparing `volvopy-0.1.8/src/volvopy/specification/energy-api-specification.v1.json` & `volvopy-0.1.9/src/volvopy/specification/energy-api-specification.v1.json`

 * *Files identical despite different names*

### Comparing `volvopy-0.1.8/src/volvopy/specification/extended-vehicle-c3-specification.v1.json` & `volvopy-0.1.9/src/volvopy/specification/extended-vehicle-c3-specification.v1.json`

 * *Files identical despite different names*

### Comparing `volvopy-0.1.8/src/volvopy/specification/location-specification.v1.json` & `volvopy-0.1.9/src/volvopy/specification/location-specification.v1.json`

 * *Files identical despite different names*

### Comparing `volvopy-0.1.8/.gitignore` & `volvopy-0.1.9/.gitignore`

 * *Files identical despite different names*

### Comparing `volvopy-0.1.8/LICENSE` & `volvopy-0.1.9/LICENSE`

 * *Files identical despite different names*

### Comparing `volvopy-0.1.8/pyproject.toml` & `volvopy-0.1.9/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 requires = ["hatchling"]
 build-backend = "hatchling.build"
 
 [project]
 name = "volvopy"
 description = "Connect to the Volvo API using Python."
 # version = "0.1.1"  # latest/current distribution version
-version = "0.1.8"  # latest test version
+version = "0.1.9"  # latest test version
 dependencies = []
 license = "MIT"
 authors = [
   { name="Mausy5043" },
 ]
 readme = "README.md"
 requires-python = ">=3.8"
```

