# Comparing `tmp/hassfeld-0.3.8a1.tar.gz` & `tmp/hassfeld-0.3.9a1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "hassfeld-0.3.8a1.tar", last modified: Thu Apr  1 18:34:17 2021, max compression
+gzip compressed data, was "hassfeld-0.3.9a1.tar", last modified: Wed Aug 18 10:13:31 2021, max compression
```

## Comparing `hassfeld-0.3.8a1.tar` & `hassfeld-0.3.9a1.tar`

### file list

```diff
@@ -1,18 +1,18 @@
-drwxrwxr-x   0 marc      (1000) marc      (1000)        0 2021-04-01 18:34:17.927013 hassfeld-0.3.8a1/
--rw-rw-r--   0 marc      (1000) marc      (1000)     1587 2021-04-01 18:34:17.926013 hassfeld-0.3.8a1/PKG-INFO
--rw-rw-r--   0 marc      (1000) marc      (1000)      845 2021-01-31 22:38:38.000000 hassfeld-0.3.8a1/README.rst
-drwxrwxr-x   0 marc      (1000) marc      (1000)        0 2021-04-01 18:34:17.926013 hassfeld-0.3.8a1/hassfeld/
--rw-rw-r--   0 marc      (1000) marc      (1000)    42178 2021-04-01 18:32:47.000000 hassfeld-0.3.8a1/hassfeld/__init__.py
--rw-r--r--   0 marc      (1000) marc      (1000)      295 2021-02-25 19:47:12.000000 hassfeld-0.3.8a1/hassfeld/auxilliary.py
--rw-rw-r--   0 marc      (1000) marc      (1000)      782 2021-03-28 15:13:53.000000 hassfeld-0.3.8a1/hassfeld/common.py
--rw-rw-r--   0 marc      (1000) marc      (1000)     2021 2021-03-28 15:18:48.000000 hassfeld-0.3.8a1/hassfeld/constants.py
--rw-rw-r--   0 marc      (1000) marc      (1000)    14766 2021-04-01 18:32:47.000000 hassfeld-0.3.8a1/hassfeld/upnp.py
--rw-rw-r--   0 marc      (1000) marc      (1000)     3151 2021-03-21 21:02:45.000000 hassfeld-0.3.8a1/hassfeld/webservice.py
-drwxrwxr-x   0 marc      (1000) marc      (1000)        0 2021-04-01 18:34:17.926013 hassfeld-0.3.8a1/hassfeld.egg-info/
--rw-r--r--   0 marc      (1000) marc      (1000)     1587 2021-04-01 18:34:17.000000 hassfeld-0.3.8a1/hassfeld.egg-info/PKG-INFO
--rw-r--r--   0 marc      (1000) marc      (1000)      303 2021-04-01 18:34:17.000000 hassfeld-0.3.8a1/hassfeld.egg-info/SOURCES.txt
--rw-r--r--   0 marc      (1000) marc      (1000)        1 2021-04-01 18:34:17.000000 hassfeld-0.3.8a1/hassfeld.egg-info/dependency_links.txt
--rw-r--r--   0 marc      (1000) marc      (1000)       53 2021-04-01 18:34:17.000000 hassfeld-0.3.8a1/hassfeld.egg-info/requires.txt
--rw-r--r--   0 marc      (1000) marc      (1000)        9 2021-04-01 18:34:17.000000 hassfeld-0.3.8a1/hassfeld.egg-info/top_level.txt
--rw-rw-r--   0 marc      (1000) marc      (1000)       38 2021-04-01 18:34:17.927013 hassfeld-0.3.8a1/setup.cfg
--rw-rw-r--   0 marc      (1000) marc      (1000)      766 2021-04-01 18:33:21.000000 hassfeld-0.3.8a1/setup.py
+drwxrwxr-x   0 marc      (1000) marc      (1000)        0 2021-08-18 10:13:31.518008 hassfeld-0.3.9a1/
+-rw-rw-r--   0 marc      (1000) marc      (1000)     1587 2021-08-18 10:13:31.518008 hassfeld-0.3.9a1/PKG-INFO
+-rw-rw-r--   0 marc      (1000) marc      (1000)      845 2021-01-31 22:38:38.000000 hassfeld-0.3.9a1/README.rst
+drwxrwxr-x   0 marc      (1000) marc      (1000)        0 2021-08-18 10:13:31.517008 hassfeld-0.3.9a1/hassfeld/
+-rw-rw-r--   0 marc      (1000) marc      (1000)    42202 2021-08-18 10:09:13.000000 hassfeld-0.3.9a1/hassfeld/__init__.py
+-rw-r--r--   0 marc      (1000) marc      (1000)      295 2021-02-25 19:47:12.000000 hassfeld-0.3.9a1/hassfeld/auxilliary.py
+-rw-rw-r--   0 marc      (1000) marc      (1000)      782 2021-03-28 15:13:53.000000 hassfeld-0.3.9a1/hassfeld/common.py
+-rw-rw-r--   0 marc      (1000) marc      (1000)     2021 2021-03-28 15:18:48.000000 hassfeld-0.3.9a1/hassfeld/constants.py
+-rw-rw-r--   0 marc      (1000) marc      (1000)    14766 2021-04-01 18:32:47.000000 hassfeld-0.3.9a1/hassfeld/upnp.py
+-rw-rw-r--   0 marc      (1000) marc      (1000)     3151 2021-03-21 21:02:45.000000 hassfeld-0.3.9a1/hassfeld/webservice.py
+drwxrwxr-x   0 marc      (1000) marc      (1000)        0 2021-08-18 10:13:31.517008 hassfeld-0.3.9a1/hassfeld.egg-info/
+-rw-r--r--   0 marc      (1000) marc      (1000)     1587 2021-08-18 10:13:31.000000 hassfeld-0.3.9a1/hassfeld.egg-info/PKG-INFO
+-rw-r--r--   0 marc      (1000) marc      (1000)      303 2021-08-18 10:13:31.000000 hassfeld-0.3.9a1/hassfeld.egg-info/SOURCES.txt
+-rw-r--r--   0 marc      (1000) marc      (1000)        1 2021-08-18 10:13:31.000000 hassfeld-0.3.9a1/hassfeld.egg-info/dependency_links.txt
+-rw-r--r--   0 marc      (1000) marc      (1000)       53 2021-08-18 10:13:31.000000 hassfeld-0.3.9a1/hassfeld.egg-info/requires.txt
+-rw-r--r--   0 marc      (1000) marc      (1000)        9 2021-08-18 10:13:31.000000 hassfeld-0.3.9a1/hassfeld.egg-info/top_level.txt
+-rw-rw-r--   0 marc      (1000) marc      (1000)       38 2021-08-18 10:13:31.518008 hassfeld-0.3.9a1/setup.cfg
+-rw-rw-r--   0 marc      (1000) marc      (1000)      766 2021-08-18 10:10:47.000000 hassfeld-0.3.9a1/setup.py
```

### Comparing `hassfeld-0.3.8a1/PKG-INFO` & `hassfeld-0.3.9a1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hassfeld
-Version: 0.3.8a1
+Version: 0.3.9a1
 Summary: Integration of Raumfeld into Home Assistant
 Home-page: https://github.com/B5r1oJ0A9G/hassfeld
 License: UNKNOWN
 Description: 
         hassfeld
         ========
```

### Comparing `hassfeld-0.3.8a1/README.rst` & `hassfeld-0.3.9a1/README.rst`

 * *Files identical despite different names*

### Comparing `hassfeld-0.3.8a1/hassfeld/__init__.py` & `hassfeld-0.3.9a1/hassfeld/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -220,27 +220,27 @@
         self.lists["rooms"] = []
         self.lists["zones"] = []
         self.resolve["roomudn_to_powerstate"] = {}
         self.resolve["room_to_udn"] = {}
         self.resolve["udn_to_room"] = {}
         self.resolve["zoneudn_to_roomudnlst"] = {}
 
-        getzones = xmltodict.parse(content_xml, force_list=("zone", "room"))
+        getzones = xmltodict.parse(content_xml, force_list=("zone", "room", "renderer"))
         self.wsd["zone_config"] = getzones["zoneConfig"]
 
         if "zones" in self.wsd["zone_config"]:
             for zone_itm in self.wsd["zone_config"]["zones"]["zone"]:
                 zone_rooms = []
                 zone_udn = zone_itm["@udn"]
                 self.resolve["zoneudn_to_roomudnlst"][zone_udn] = []
 
                 for room_itm in zone_itm["room"]:
                     room_name = room_itm["@name"]
                     room_udn = room_itm["@udn"]
-                    renderer_udn = room_itm["renderer"]["@udn"]
+                    renderer_udn = room_itm["renderer"][0]["@udn"]
                     zone_rooms.append(room_name)
                     self.lists["rooms"].append(room_name)
                     if "@powerState" in room_itm:
                         self.resolve["roomudn_to_powerstate"][room_udn] = room_itm[
                             "@powerState"
                         ]
                     else:
@@ -256,30 +256,30 @@
 
                 self.lists["zones"].append(sorted(zone_rooms))
 
         if "unassignedRooms" in self.wsd["zone_config"]:
             for room in self.wsd["zone_config"]["unassignedRooms"]["room"]:
                 room_name = room["@name"]
                 room_udn = room["@udn"]
-                renderer_udn = room["renderer"]["@udn"]
+                renderer_udn = room["renderer"][0]["@udn"]
                 if "@powerState" in room:
                     self.resolve["roomudn_to_powerstate"][room_udn] = room[
                         "@powerState"
                     ]
                 else:
                     log_warn(
                         "No 'powerState' attribute provided for room: %s" % room_name
                     )
                     self.resolve["roomudn_to_powerstate"][room_udn] = None
                 self.resolve["room_to_udn"][room_name] = room_udn
                 self.resolve["udn_to_room"][room_udn] = room_name
                 self.lists["rooms"].append(room_name)
                 self.resolve["roomudn_to_rendudn"][room_udn] = renderer_udn
-                if "@spotifyConnect" in room["renderer"]:
-                    if room["renderer"]["@spotifyConnect"] == SPOTIFY_ACTIVE:
+                if "@spotifyConnect" in room["renderer"][0]:
+                    if room["renderer"][0]["@spotifyConnect"] == SPOTIFY_ACTIVE:
                         self.lists["spotify_renderer"].append(renderer_udn)
 
         self._init_done["zone_config"] = True
 
         if self.callback is not None:
             self.callback(TRIGGER_UPDATE_ZONE_CONFIG)
```

### Comparing `hassfeld-0.3.8a1/hassfeld/common.py` & `hassfeld-0.3.9a1/hassfeld/common.py`

 * *Files identical despite different names*

### Comparing `hassfeld-0.3.8a1/hassfeld/constants.py` & `hassfeld-0.3.9a1/hassfeld/constants.py`

 * *Files identical despite different names*

### Comparing `hassfeld-0.3.8a1/hassfeld/upnp.py` & `hassfeld-0.3.9a1/hassfeld/upnp.py`

 * *Files identical despite different names*

### Comparing `hassfeld-0.3.8a1/hassfeld/webservice.py` & `hassfeld-0.3.9a1/hassfeld/webservice.py`

 * *Files identical despite different names*

### Comparing `hassfeld-0.3.8a1/hassfeld.egg-info/PKG-INFO` & `hassfeld-0.3.9a1/hassfeld.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hassfeld
-Version: 0.3.8a1
+Version: 0.3.9a1
 Summary: Integration of Raumfeld into Home Assistant
 Home-page: https://github.com/B5r1oJ0A9G/hassfeld
 License: UNKNOWN
 Description: 
         hassfeld
         ========
```

### Comparing `hassfeld-0.3.8a1/setup.py` & `hassfeld-0.3.9a1/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import setuptools
 
 with open("README.rst", "r", encoding="utf-8") as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="hassfeld",
-    version="0.3.8-alpha1",
+    version="0.3.9-alpha1",
     description="Integration of Raumfeld into Home Assistant",
     long_description=long_description,
     long_description_content_type="text/x-rst",
     url="https://github.com/B5r1oJ0A9G/hassfeld",
     packages=setuptools.find_packages(),
     classifiers=[
         "Programming Language :: Python :: 3",
```

