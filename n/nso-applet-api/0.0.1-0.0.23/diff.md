# Comparing `tmp/nso-applet-api-0.0.1.tar.gz` & `tmp/nso-applet-api-0.0.23.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nso-applet-api-0.0.1.tar", last modified: Fri Jul  7 23:19:45 2023, max compression
+gzip compressed data, was "nso-applet-api-0.0.23.tar", last modified: Sun Jul 23 03:37:13 2023, max compression
```

## Comparing `nso-applet-api-0.0.1.tar` & `nso-applet-api-0.0.23.tar`

### file list

```diff
@@ -1,18 +1,19 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-07 23:19:45.901434 nso-applet-api-0.0.1/
--rw-r--r--   0 runner    (1001) docker     (123)      301 2023-07-07 23:19:45.901434 nso-applet-api-0.0.1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      101 2023-07-07 23:19:36.000000 nso-applet-api-0.0.1/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-07 23:19:45.897434 nso-applet-api-0.0.1/nso/
--rw-r--r--   0 runner    (1001) docker     (123)      199 2023-07-07 23:19:36.000000 nso-applet-api-0.0.1/nso/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      767 2023-07-07 23:19:36.000000 nso-applet-api-0.0.1/nso/__main__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6945 2023-07-07 23:19:36.000000 nso-applet-api-0.0.1/nso/api.py
--rw-r--r--   0 runner    (1001) docker     (123)      395 2023-07-07 23:19:36.000000 nso-applet-api-0.0.1/nso/exceptions.py
--rw-r--r--   0 runner    (1001) docker     (123)     8384 2023-07-07 23:19:36.000000 nso-applet-api-0.0.1/nso/structures.py
--rw-r--r--   0 runner    (1001) docker     (123)      980 2023-07-07 23:19:36.000000 nso-applet-api-0.0.1/nso/util.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-07 23:19:45.901434 nso-applet-api-0.0.1/nso_applet_api.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)      301 2023-07-07 23:19:45.000000 nso-applet-api-0.0.1/nso_applet_api.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      298 2023-07-07 23:19:45.000000 nso-applet-api-0.0.1/nso_applet_api.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-07 23:19:45.000000 nso-applet-api-0.0.1/nso_applet_api.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       15 2023-07-07 23:19:45.000000 nso-applet-api-0.0.1/nso_applet_api.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        4 2023-07-07 23:19:45.000000 nso-applet-api-0.0.1/nso_applet_api.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-07 23:19:45.901434 nso-applet-api-0.0.1/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      512 2023-07-07 23:19:36.000000 nso-applet-api-0.0.1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 03:37:13.430302 nso-applet-api-0.0.23/
+-rw-r--r--   0 runner    (1001) docker     (123)     1069 2023-07-23 03:37:04.000000 nso-applet-api-0.0.23/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      834 2023-07-23 03:37:13.430302 nso-applet-api-0.0.23/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      549 2023-07-23 03:37:04.000000 nso-applet-api-0.0.23/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 03:37:13.430302 nso-applet-api-0.0.23/nso/
+-rw-r--r--   0 runner    (1001) docker     (123)      199 2023-07-23 03:37:04.000000 nso-applet-api-0.0.23/nso/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      771 2023-07-23 03:37:04.000000 nso-applet-api-0.0.23/nso/__main__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6710 2023-07-23 03:37:04.000000 nso-applet-api-0.0.23/nso/api.py
+-rw-r--r--   0 runner    (1001) docker     (123)      404 2023-07-23 03:37:04.000000 nso-applet-api-0.0.23/nso/exceptions.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14183 2023-07-23 03:37:04.000000 nso-applet-api-0.0.23/nso/structures.py
+-rw-r--r--   0 runner    (1001) docker     (123)      989 2023-07-23 03:37:04.000000 nso-applet-api-0.0.23/nso/util.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 03:37:13.430302 nso-applet-api-0.0.23/nso_applet_api.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)      834 2023-07-23 03:37:13.000000 nso-applet-api-0.0.23/nso_applet_api.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      306 2023-07-23 03:37:13.000000 nso-applet-api-0.0.23/nso_applet_api.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 03:37:13.000000 nso-applet-api-0.0.23/nso_applet_api.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       15 2023-07-23 03:37:13.000000 nso-applet-api-0.0.23/nso_applet_api.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        4 2023-07-23 03:37:13.000000 nso-applet-api-0.0.23/nso_applet_api.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 03:37:13.430302 nso-applet-api-0.0.23/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      616 2023-07-23 03:37:04.000000 nso-applet-api-0.0.23/setup.py
```

### Comparing `nso-applet-api-0.0.1/nso/__main__.py` & `nso-applet-api-0.0.23/nso/__main__.py`

 * *Files 1% similar despite different names*

```diff
@@ -9,9 +9,9 @@
         print(Color.DEFAULT, end = '')
 
         try:
             import readline
         except ImportError:
             pass
         while True:
-            endpoint = input('>>> ' + Color.WHITE)
+            endpoint:str = input('>>> ' + Color.WHITE)
             exec(endpoint, globals(), locals())
```

### Comparing `nso-applet-api-0.0.1/nso/api.py` & `nso-applet-api-0.0.23/nso/api.py`

 * *Files 4% similar despite different names*

```diff
@@ -135,30 +135,22 @@
         Parameters
         ----------
         country : str
         the account's country code
 
         Returns
         -------
-        dict
-        a dictionary that contains information regarding the user's My Nintendo point balance
-            Keys:
-                received_points : list
-                point_wallet : dict
-                    Keys:
-                        total_point : dict
-                            Keys:
-                                platinum : int
-                        expirations : list
+        Login
+        an object that contains information regarding the user's My Nintendo point balance
         """
-        return self._post('/api/v1/login',
+        return Login(**self._post('/api/v1/login',
             query = {
                 'country': country,
             }
-        ).json()
+        ).json())
 
     def getV1LClassicsTitles(self, statuses:str, country:str) -> list:
         """GET - Gets the current titles available under NSO's emulation softwares
 
         Parameters
         ----------
         statuses : str
@@ -199,12 +191,12 @@
             }
         ).json() ]
 
     def getV2PickupItems(self, country:str) -> dict:
         """
         Unfinished
         """
-        return self._get('/api/v2/pickup_items',
+        return [ Pickup_Item(**iterable) for iterable in self._get('/api/v2/pickup_items',
             query = {
                 'country': country,
             }
-        ).json()
+        ).json() ]
```

### Comparing `nso-applet-api-0.0.1/nso/util.py` & `nso-applet-api-0.0.23/nso/util.py`

 * *Files 11% similar despite different names*

```diff
@@ -7,18 +7,18 @@
     RED = '\033[91m'
     PURPLE = '\033[0;35m'
     YELLOW = '\033[93m'
     BLUE = '\033[94m'
     GREEN = '\033[92m'
     WHITE = '\033[1;37m'
 
-def toString(self, indent = 0) -> str:
+def toString(self, indent:int = 0) -> str:
     ret = []
     for key in dir(self):
         if not callable(getattr(self, key)) and not key.startswith('__'):
             value = self.__dict__[key]
             if hasattr(value, '__dict__'):
                 value = '\n' + toString(value, indent + 1)
             if isinstance(value, list):
-                value = '[\n' + ',\n\n'.join( (toString(object, indent + 1) if hasattr(object, '__dict__') else (('    ' * (indent + 1)) + object)) for object in value ) + '\n' + ('    ' * indent) + ']'
+                value = '[\n' + ',\n\n'.join( (toString(object, indent + 1) if hasattr(object, '__dict__') else (('    ' * (indent + 1)) + str(object))) for object in value ) + '\n' + ('    ' * indent) + ']'
             ret.append((key, value))
     return ('    ' * indent) + 'Object: ' + type(self).__name__ + '\n' + '\n'.join([ ('    ' * indent) + '%s: %s' % (key, value) for key, value in ret ])
```

### Comparing `nso-applet-api-0.0.1/setup.py` & `nso-applet-api-0.0.23/setup.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,15 +1,20 @@
 # Made by Deltaion Lee (MCMi460) on Github
 import setuptools
 
+from pathlib import Path
+directory = Path(__file__).parent
+long_description = (directory / 'README.md').read_text()
+
 setuptools.setup(
 	name = 'nso-applet-api',
-	version = '0.0.1',
-	description = 'Nintendo NSO applet API',
-	long_description = 'This library implements in Python various API endpoints from the NSO Webapplet',
+	version = '0.0.23',
+	description = 'Nintendo NSO Applet API',
+	long_description = long_description,
+	long_description_content_type = 'text/markdown',
 	author = 'Deltaion Lee',
 	author_email = '32529306+MCMi460@users.noreply.github.com',
 	url = 'https://github.com/MCMi460/nso-applet-api',
 	packages = [
 		'nso',
 	],
 	package_data = {
```

