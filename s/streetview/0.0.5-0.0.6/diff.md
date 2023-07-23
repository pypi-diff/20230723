# Comparing `tmp/streetview-0.0.5.tar.gz` & `tmp/streetview-0.0.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "streetview-0.0.5.tar", last modified: Thu Jun 15 07:46:16 2023, max compression
+gzip compressed data, was "streetview-0.0.6.tar", last modified: Sun Jul 23 17:28:00 2023, max compression
```

## Comparing `streetview-0.0.5.tar` & `streetview-0.0.6.tar`

### file list

```diff
@@ -1,23 +1,23 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-15 07:46:16.427043 streetview-0.0.5/
--rw-r--r--   0 runner    (1001) docker     (123)       36 2023-06-15 07:45:56.000000 streetview-0.0.5/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     2692 2023-06-15 07:46:16.427043 streetview-0.0.5/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2407 2023-06-15 07:45:56.000000 streetview-0.0.5/readme.md
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-06-15 07:46:16.427043 streetview-0.0.5/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      623 2023-06-15 07:45:56.000000 streetview-0.0.5/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-15 07:46:16.427043 streetview-0.0.5/streetview/
--rw-r--r--   0 runner    (1001) docker     (123)      147 2023-06-15 07:45:56.000000 streetview-0.0.5/streetview/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2129 2023-06-15 07:45:56.000000 streetview-0.0.5/streetview/api.py
--rw-r--r--   0 runner    (1001) docker     (123)     2298 2023-06-15 07:45:56.000000 streetview-0.0.5/streetview/download.py
--rw-r--r--   0 runner    (1001) docker     (123)     2645 2023-06-15 07:45:56.000000 streetview-0.0.5/streetview/search.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-15 07:46:16.427043 streetview-0.0.5/streetview.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2692 2023-06-15 07:46:16.000000 streetview-0.0.5/streetview.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      390 2023-06-15 07:46:16.000000 streetview-0.0.5/streetview.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-06-15 07:46:16.000000 streetview-0.0.5/streetview.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-06-15 07:46:16.000000 streetview-0.0.5/streetview.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)       25 2023-06-15 07:46:16.000000 streetview-0.0.5/streetview.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       11 2023-06-15 07:46:16.000000 streetview-0.0.5/streetview.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-15 07:46:16.427043 streetview-0.0.5/tests/
--rw-r--r--   0 runner    (1001) docker     (123)     1138 2023-06-15 07:45:56.000000 streetview-0.0.5/tests/test_api.py
--rw-r--r--   0 runner    (1001) docker     (123)     2554 2023-06-15 07:45:56.000000 streetview-0.0.5/tests/test_download.py
--rw-r--r--   0 runner    (1001) docker     (123)     2551 2023-06-15 07:45:56.000000 streetview-0.0.5/tests/test_search.py
--rw-r--r--   0 runner    (1001) docker     (123)       19 2023-06-15 07:45:56.000000 streetview-0.0.5/version.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:28:00.188691 streetview-0.0.6/
+-rw-r--r--   0 runner    (1001) docker     (123)       36 2023-07-23 17:27:41.000000 streetview-0.0.6/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     2692 2023-07-23 17:28:00.188691 streetview-0.0.6/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2407 2023-07-23 17:27:41.000000 streetview-0.0.6/readme.md
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 17:28:00.188691 streetview-0.0.6/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      623 2023-07-23 17:27:41.000000 streetview-0.0.6/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:28:00.188691 streetview-0.0.6/streetview/
+-rw-r--r--   0 runner    (1001) docker     (123)      147 2023-07-23 17:27:41.000000 streetview-0.0.6/streetview/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2129 2023-07-23 17:27:41.000000 streetview-0.0.6/streetview/api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2341 2023-07-23 17:27:41.000000 streetview-0.0.6/streetview/download.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2733 2023-07-23 17:27:41.000000 streetview-0.0.6/streetview/search.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:28:00.188691 streetview-0.0.6/streetview.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2692 2023-07-23 17:28:00.000000 streetview-0.0.6/streetview.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      390 2023-07-23 17:28:00.000000 streetview-0.0.6/streetview.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 17:28:00.000000 streetview-0.0.6/streetview.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 17:28:00.000000 streetview-0.0.6/streetview.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)       25 2023-07-23 17:28:00.000000 streetview-0.0.6/streetview.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       11 2023-07-23 17:28:00.000000 streetview-0.0.6/streetview.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:28:00.188691 streetview-0.0.6/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     1138 2023-07-23 17:27:41.000000 streetview-0.0.6/tests/test_api.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2554 2023-07-23 17:27:41.000000 streetview-0.0.6/tests/test_download.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2939 2023-07-23 17:27:41.000000 streetview-0.0.6/tests/test_search.py
+-rw-r--r--   0 runner    (1001) docker     (123)       19 2023-07-23 17:27:42.000000 streetview-0.0.6/version.py
```

### Comparing `streetview-0.0.5/PKG-INFO` & `streetview-0.0.6/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: streetview
-Version: 0.0.5
+Version: 0.0.6
 Summary: Retrieve current and historical photos from Google Street View
 Home-page: https://github.com/robolyst/streetview
 Author: Adrian Letchford
 Author-email: me@dradrian.com
 License: MIT
 Description-Content-Type: text/markdown
```

### Comparing `streetview-0.0.5/readme.md` & `streetview-0.0.6/readme.md`

 * *Files identical despite different names*

### Comparing `streetview-0.0.5/setup.py` & `streetview-0.0.6/setup.py`

 * *Files identical despite different names*

### Comparing `streetview-0.0.5/streetview/api.py` & `streetview-0.0.6/streetview/api.py`

 * *Files identical despite different names*

### Comparing `streetview-0.0.5/streetview/download.py` & `streetview-0.0.6/streetview/download.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 import itertools
 import time
 from dataclasses import dataclass
 from io import BytesIO
-from typing import Generator
+from typing import Generator, Tuple
 
 import requests
 from PIL import Image
 
 
 @dataclass
 class TileInfo:
@@ -18,26 +18,30 @@
 @dataclass
 class Tile:
     x: int
     y: int
     image: Image.Image
 
 
-def get_width_and_height_from_zoom(zoom: int) -> (int, int):
+def get_width_and_height_from_zoom(zoom: int) -> Tuple[int, int]:
     """
-    Returns the width and height of a panorama at a given zoom level, depends on the zoom level.
+    Returns the width and height of a panorama at a given zoom level, depends on the
+    zoom level.
     """
     return 2**zoom, 2 ** (zoom - 1)
 
 
 def make_download_url(pano_id: str, zoom: int, x: int, y: int) -> str:
     """
     Returns the URL to download a tile.
     """
-    return f"https://cbk0.google.com/cbk?output=tile&panoid={pano_id}&zoom={zoom}&x={x}&y={y}"
+    return (
+        "https://cbk0.google.com/cbk"
+        f"?output=tile&panoid={pano_id}&zoom={zoom}&x={x}&y={y}"
+    )
 
 
 def fetch_panorama_tile(tile_info: TileInfo) -> Image.Image:
     """
     Tries to download a tile, returns a PIL Image.
     """
     while True:
```

### Comparing `streetview-0.0.5/streetview/search.py` & `streetview-0.0.6/streetview/search.py`

 * *Files 11% similar despite different names*

```diff
@@ -8,16 +8,16 @@
 
 
 class Panorama(BaseModel):
     pano_id: str
     lat: float
     lon: float
     heading: float
-    pitch: float
-    roll: float
+    pitch: Optional[float]
+    roll: Optional[float]
     date: Optional[str]
 
 
 def make_search_url(lat: float, lon: float) -> str:
     """
     Builds the URL of the script on Google's servers that returns the closest
     panoramas (ids) to a give GPS coordinate.
@@ -75,16 +75,16 @@
 
     return [
         Panorama(
             pano_id=pano[0][1],
             lat=pano[2][0][2],
             lon=pano[2][0][3],
             heading=pano[2][2][0],
-            pitch=pano[2][2][1],
-            roll=pano[2][2][2],
+            pitch=pano[2][2][1] if len(pano[2][2]) >= 2 else None,
+            roll=pano[2][2][2] if len(pano[2][2]) >= 3 else None,
             date=dates[i] if i < len(dates) else None,
         )
         for i, pano in enumerate(raw_panos)
     ]
 
 
 def search_panoramas(lat: float, lon: float) -> List[Panorama]:
```

### Comparing `streetview-0.0.5/streetview.egg-info/PKG-INFO` & `streetview-0.0.6/streetview.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: streetview
-Version: 0.0.5
+Version: 0.0.6
 Summary: Retrieve current and historical photos from Google Street View
 Home-page: https://github.com/robolyst/streetview
 Author: Adrian Letchford
 Author-email: me@dradrian.com
 License: MIT
 Description-Content-Type: text/markdown
```

### Comparing `streetview-0.0.5/tests/test_api.py` & `streetview-0.0.6/tests/test_api.py`

 * *Files identical despite different names*

### Comparing `streetview-0.0.5/tests/test_download.py` & `streetview-0.0.6/tests/test_download.py`

 * *Files identical despite different names*

### Comparing `streetview-0.0.5/tests/test_search.py` & `streetview-0.0.6/tests/test_search.py`

 * *Files 24% similar despite different names*

```diff
@@ -100,7 +100,19 @@
 
 @pytest.mark.vcr
 def test_search_where_there_are_no_dates():
     result = search_panoramas(**TUNIS)
 
     dates = [p.date for p in result]
     assert dates == [None] * len(dates)
+
+
+def test_coordinates_with_missing_pitch():
+    panos = search_panoramas(35.658353457849685, 139.6920989241623)
+    is_pitch_none = [p.pitch is None for p in panos]
+    assert any(is_pitch_none)
+
+
+def test_coordinates_with_missing_roll():
+    panos = search_panoramas(35.658353457849685, 139.6920989241623)
+    is_roll_none = [p.roll is None for p in panos]
+    assert any(is_roll_none)
```

