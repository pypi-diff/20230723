# Comparing `tmp/pygeoops-0.1.1.tar.gz` & `tmp/pygeoops-0.2.0a1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pygeoops-0.1.1.tar", last modified: Tue Apr 11 23:35:07 2023, max compression
+gzip compressed data, was "pygeoops-0.2.0a1.tar", last modified: Sat Jul 22 22:03:44 2023, max compression
```

## Comparing `pygeoops-0.1.1.tar` & `pygeoops-0.2.0a1.tar`

### file list

```diff
@@ -1,23 +1,34 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-11 23:35:07.326212 pygeoops-0.1.1/
--rw-r--r--   0 runner    (1001) docker     (123)     1495 2023-04-11 23:34:56.000000 pygeoops-0.1.1/LICENSE.txt
--rw-r--r--   0 runner    (1001) docker     (123)       60 2023-04-11 23:34:56.000000 pygeoops-0.1.1/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     1932 2023-04-11 23:35:07.326212 pygeoops-0.1.1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1334 2023-04-11 23:34:56.000000 pygeoops-0.1.1/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-11 23:35:07.322212 pygeoops-0.1.1/pygeoops/
--rw-r--r--   0 runner    (1001) docker     (123)      333 2023-04-11 23:34:56.000000 pygeoops-0.1.1/pygeoops/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    11510 2023-04-11 23:34:56.000000 pygeoops-0.1.1/pygeoops/centerline.py
--rw-r--r--   0 runner    (1001) docker     (123)        5 2023-04-11 23:34:56.000000 pygeoops-0.1.1/pygeoops/version.txt
--rw-r--r--   0 runner    (1001) docker     (123)     7657 2023-04-11 23:34:56.000000 pygeoops-0.1.1/pygeoops/view_angles.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-11 23:35:07.326212 pygeoops-0.1.1/pygeoops.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1932 2023-04-11 23:35:07.000000 pygeoops-0.1.1/pygeoops.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      387 2023-04-11 23:35:07.000000 pygeoops-0.1.1/pygeoops.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-04-11 23:35:07.000000 pygeoops-0.1.1/pygeoops.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       10 2023-04-11 23:35:07.000000 pygeoops-0.1.1/pygeoops.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        9 2023-04-11 23:35:07.000000 pygeoops-0.1.1/pygeoops.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)      793 2023-04-11 23:34:56.000000 pygeoops-0.1.1/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       96 2023-04-11 23:35:07.326212 pygeoops-0.1.1/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      165 2023-04-11 23:34:56.000000 pygeoops-0.1.1/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-11 23:35:07.326212 pygeoops-0.1.1/tests/
--rw-r--r--   0 runner    (1001) docker     (123)     4355 2023-04-11 23:34:56.000000 pygeoops-0.1.1/tests/test_centerline.py
--rw-r--r--   0 runner    (1001) docker     (123)     1936 2023-04-11 23:34:56.000000 pygeoops-0.1.1/tests/test_helper.py
--rw-r--r--   0 runner    (1001) docker     (123)     5356 2023-04-11 23:34:56.000000 pygeoops-0.1.1/tests/test_view_angles.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:03:44.766509 pygeoops-0.2.0a1/
+-rw-r--r--   0 runner    (1001) docker     (123)     1495 2023-07-22 22:03:29.000000 pygeoops-0.2.0a1/LICENSE.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       60 2023-07-22 22:03:29.000000 pygeoops-0.2.0a1/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     1934 2023-07-22 22:03:44.766509 pygeoops-0.2.0a1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1334 2023-07-22 22:03:29.000000 pygeoops-0.2.0a1/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:03:44.762508 pygeoops-0.2.0a1/pygeoops/
+-rw-r--r--   0 runner    (1001) docker     (123)      503 2023-07-22 22:03:29.000000 pygeoops-0.2.0a1/pygeoops/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11495 2023-07-22 22:03:29.000000 pygeoops-0.2.0a1/pygeoops/_centerline.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10017 2023-07-22 22:03:29.000000 pygeoops-0.2.0a1/pygeoops/_general.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9272 2023-07-22 22:03:29.000000 pygeoops-0.2.0a1/pygeoops/_grid.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9235 2023-07-22 22:03:29.000000 pygeoops-0.2.0a1/pygeoops/_simplify.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5647 2023-07-22 22:03:29.000000 pygeoops-0.2.0a1/pygeoops/_simplify_lang.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5507 2023-07-22 22:03:29.000000 pygeoops-0.2.0a1/pygeoops/_types.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7625 2023-07-22 22:03:29.000000 pygeoops-0.2.0a1/pygeoops/_view_angles.py
+-rw-r--r--   0 runner    (1001) docker     (123)        7 2023-07-22 22:03:29.000000 pygeoops-0.2.0a1/pygeoops/version.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:03:44.762508 pygeoops-0.2.0a1/pygeoops.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1934 2023-07-22 22:03:44.000000 pygeoops-0.2.0a1/pygeoops.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      632 2023-07-22 22:03:44.000000 pygeoops-0.2.0a1/pygeoops.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-22 22:03:44.000000 pygeoops-0.2.0a1/pygeoops.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       20 2023-07-22 22:03:44.000000 pygeoops-0.2.0a1/pygeoops.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-22 22:03:44.000000 pygeoops-0.2.0a1/pygeoops.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     3968 2023-07-22 22:03:29.000000 pygeoops-0.2.0a1/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       96 2023-07-22 22:03:44.766509 pygeoops-0.2.0a1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      165 2023-07-22 22:03:29.000000 pygeoops-0.2.0a1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:03:44.766509 pygeoops-0.2.0a1/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     4439 2023-07-22 22:03:29.000000 pygeoops-0.2.0a1/tests/test_centerline.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6595 2023-07-22 22:03:29.000000 pygeoops-0.2.0a1/tests/test_general.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1456 2023-07-22 22:03:29.000000 pygeoops-0.2.0a1/tests/test_geopandas.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3134 2023-07-22 22:03:29.000000 pygeoops-0.2.0a1/tests/test_grid.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3489 2023-07-22 22:03:29.000000 pygeoops-0.2.0a1/tests/test_helper.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10503 2023-07-22 22:03:29.000000 pygeoops-0.2.0a1/tests/test_simplify.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2781 2023-07-22 22:03:29.000000 pygeoops-0.2.0a1/tests/test_simplify_lang.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4661 2023-07-22 22:03:29.000000 pygeoops-0.2.0a1/tests/test_types.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5357 2023-07-22 22:03:29.000000 pygeoops-0.2.0a1/tests/test_view_angles.py
```

### Comparing `pygeoops-0.1.1/LICENSE.txt` & `pygeoops-0.2.0a1/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `pygeoops-0.1.1/PKG-INFO` & `pygeoops-0.2.0a1/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pygeoops
-Version: 0.1.1
+Version: 0.2.0a1
 Summary: Library with some less common or extended spatial functions
 Author-email: Pieter Roggemans <pieter.roggemans@gmail.com>
 Project-URL: Homepage, https://github.com/pygeoops/pygeoops
 Project-URL: Bug Tracker, https://github.com/pygeoops/pygeoops/issues
 Keywords: GIS,cartography,pandas,shapely,geopandas
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: BSD License
```

### Comparing `pygeoops-0.1.1/README.md` & `pygeoops-0.2.0a1/README.md`

 * *Files identical despite different names*

### Comparing `pygeoops-0.1.1/pygeoops/centerline.py` & `pygeoops-0.2.0a1/pygeoops/_centerline.py`

 * *Files 2% similar despite different names*

```diff
@@ -54,31 +54,32 @@
 
     Returns:
         geometry or array_like: the centerline for each of the input geometries.
 
     .. |centerline_L_shape| image:: ../_static/images/centerline_fancy_Lshape.png
         :alt: Centerline of a fancy L shaped polygon
     """
-    # Check if input is an array or not
-    if isinstance(geometry, np.ndarray) or isinstance(geometry, list):
-        # Treat every geometry
-        result = []
-        for geom in geometry:  # type: ignore
-            result.append(
-                _centerline(
-                    geom,
-                    densify_distance=densify_distance,
-                    min_branch_length=min_branch_length,
-                    simplifytolerance=simplifytolerance,
-                )
+    if geometry is None:
+        return None
+
+    # If input is arraylike, treat every geometry in loop
+    if hasattr(geometry, "__len__"):
+        result = [
+            _centerline(
+                geom=geom,
+                densify_distance=densify_distance,
+                min_branch_length=min_branch_length,
+                simplifytolerance=simplifytolerance,
             )
+            for geom in geometry
+        ]
         return result
     else:
         return _centerline(
-            geometry,
+            geom=geometry,
             densify_distance=densify_distance,
             min_branch_length=min_branch_length,
             simplifytolerance=simplifytolerance,
         )
 
 
 def _centerline(
@@ -124,15 +125,17 @@
     min_branch_length_cur = min_branch_length
     if min_branch_length_cur < 0:
         # If < 0, calculate
         if average_width is None:
             average_width = _average_width(geom)
         min_branch_length_cur = abs(min_branch_length_cur) * average_width
     if min_branch_length_cur > 0:
-        lines = _remove_short_branches_notempty(lines, min_branch_length_cur)
+        lines = _remove_short_branches_notempty(
+            line=lines, min_branch_length=min_branch_length_cur
+        )
 
     # Simplify if needed
     if simplifytolerance is not None:
         tol = simplifytolerance
         if simplifytolerance < 0:
             # Automatically determine tol
             if average_width is None:
```

### Comparing `pygeoops-0.1.1/pygeoops/view_angles.py` & `pygeoops-0.2.0a1/pygeoops/_view_angles.py`

 * *Files 1% similar despite different names*

```diff
@@ -58,16 +58,16 @@
         raise ValueError(
             "viewpoint and visible_geom are arrays, so they must be the same length"
         )
 
     # Combine both input arrays
     geoms_arr = np.concatenate(
         [
-            np.expand_dims(viewpoint_arr, 1),  # type: ignore
-            np.expand_dims(visible_geom_arr, 1),  # type: ignore
+            np.expand_dims(viewpoint_arr, 1),
+            np.expand_dims(visible_geom_arr, 1),
         ],
         axis=1,
     )
 
     # Function to calculate the view angles for one viewpoint, visible_geom pair
     def calculate_angles(input) -> Tuple[float, float]:
         viewpoint_geom, visible_geom = input
```

### Comparing `pygeoops-0.1.1/pygeoops.egg-info/PKG-INFO` & `pygeoops-0.2.0a1/pygeoops.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pygeoops
-Version: 0.1.1
+Version: 0.2.0a1
 Summary: Library with some less common or extended spatial functions
 Author-email: Pieter Roggemans <pieter.roggemans@gmail.com>
 Project-URL: Homepage, https://github.com/pygeoops/pygeoops
 Project-URL: Bug Tracker, https://github.com/pygeoops/pygeoops/issues
 Keywords: GIS,cartography,pandas,shapely,geopandas
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: BSD License
```

### Comparing `pygeoops-0.1.1/tests/test_centerline.py` & `pygeoops-0.2.0a1/tests/test_centerline.py`

 * *Files 1% similar despite different names*

```diff
@@ -48,14 +48,18 @@
     assert centerlines is not None
     for test_idx, box_test in enumerate(box_tests):
         output_path = tmp_path / f"test_centerline_box_arr_{box_test[0]}.png"
         test_helper.plot([centerlines[test_idx], centerlines[test_idx]], output_path)
         assert centerlines[test_idx].wkt == box_test[2]
 
 
+def test_centerline_None_geometry():
+    assert pygeoops.centerline(None) is None
+
+
 @pytest.mark.parametrize(
     "test, min_branch_length, poly_wkt, expected_centerline_wkt",
     [
         (
             "input: elleptical shape, resulted in small branch not being removed",
             0.0,
             "MULTIPOLYGON (((0 1, 1 3.25, 2 4.5, 3 5.75, 3.5 6.25, 5 3.25, 3.75 1.75, 2.5 0.5, 1 0, 0 1)))",  # noqa: E501
```

### Comparing `pygeoops-0.1.1/tests/test_view_angles.py` & `pygeoops-0.2.0a1/tests/test_view_angles.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,8 +1,9 @@
 from typing import List, Tuple
+
 import numpy as np
 import pytest
 import shapely
 import shapely.affinity
 from shapely import from_wkt
 
 import pygeoops
```

