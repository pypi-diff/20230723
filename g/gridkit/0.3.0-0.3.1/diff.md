# Comparing `tmp/gridkit-0.3.0.tar.gz` & `tmp/gridkit-0.3.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "gridkit-0.3.0.tar", last modified: Sat Jul 15 23:12:29 2023, max compression
+gzip compressed data, was "gridkit-0.3.1.tar", last modified: Sun Jul 23 13:36:24 2023, max compression
```

## Comparing `gridkit-0.3.0.tar` & `gridkit-0.3.1.tar`

### file list

```diff
@@ -1,22 +1,22 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-15 23:12:29.421086 gridkit-0.3.0/
--rw-r--r--   0 runner    (1001) docker     (123)     1070 2023-07-15 23:12:18.000000 gridkit-0.3.0/LICENSE.txt
--rw-r--r--   0 runner    (1001) docker     (123)     1512 2023-07-15 23:12:29.421086 gridkit-0.3.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1065 2023-07-15 23:12:18.000000 gridkit-0.3.0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-15 23:12:29.417086 gridkit-0.3.0/gridkit/
--rw-r--r--   0 runner    (1001) docker     (123)      114 2023-07-15 23:12:18.000000 gridkit-0.3.0/gridkit/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2362 2023-07-15 23:12:18.000000 gridkit-0.3.0/gridkit/_statistical_functions.py
--rw-r--r--   0 runner    (1001) docker     (123)    16385 2023-07-15 23:12:18.000000 gridkit-0.3.0/gridkit/base_grid.py
--rw-r--r--   0 runner    (1001) docker     (123)    26823 2023-07-15 23:12:18.000000 gridkit-0.3.0/gridkit/bounded_grid.py
--rw-r--r--   0 runner    (1001) docker     (123)      156 2023-07-15 23:12:18.000000 gridkit-0.3.0/gridkit/errors.py
--rw-r--r--   0 runner    (1001) docker     (123)    32572 2023-07-15 23:12:18.000000 gridkit-0.3.0/gridkit/hex_grid.py
--rw-r--r--   0 runner    (1001) docker     (123)     2384 2023-07-15 23:12:18.000000 gridkit-0.3.0/gridkit/io.py
--rw-r--r--   0 runner    (1001) docker     (123)    26464 2023-07-15 23:12:18.000000 gridkit-0.3.0/gridkit/rect_grid.py
--rw-r--r--   0 runner    (1001) docker     (123)       23 2023-07-15 23:12:29.000000 gridkit-0.3.0/gridkit/version.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-15 23:12:29.421086 gridkit-0.3.0/gridkit.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1512 2023-07-15 23:12:29.000000 gridkit-0.3.0/gridkit.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      375 2023-07-15 23:12:29.000000 gridkit-0.3.0/gridkit.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-15 23:12:29.000000 gridkit-0.3.0/gridkit.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      213 2023-07-15 23:12:29.000000 gridkit-0.3.0/gridkit.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        8 2023-07-15 23:12:29.000000 gridkit-0.3.0/gridkit.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-15 23:12:29.421086 gridkit-0.3.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1316 2023-07-15 23:12:18.000000 gridkit-0.3.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:36:24.508059 gridkit-0.3.1/
+-rw-r--r--   0 runner    (1001) docker     (123)     1070 2023-07-23 13:36:15.000000 gridkit-0.3.1/LICENSE.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1552 2023-07-23 13:36:24.508059 gridkit-0.3.1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1105 2023-07-23 13:36:15.000000 gridkit-0.3.1/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:36:24.508059 gridkit-0.3.1/gridkit/
+-rw-r--r--   0 runner    (1001) docker     (123)      114 2023-07-23 13:36:15.000000 gridkit-0.3.1/gridkit/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2330 2023-07-23 13:36:15.000000 gridkit-0.3.1/gridkit/_statistical_functions.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16385 2023-07-23 13:36:15.000000 gridkit-0.3.1/gridkit/base_grid.py
+-rw-r--r--   0 runner    (1001) docker     (123)    26718 2023-07-23 13:36:15.000000 gridkit-0.3.1/gridkit/bounded_grid.py
+-rw-r--r--   0 runner    (1001) docker     (123)      156 2023-07-23 13:36:15.000000 gridkit-0.3.1/gridkit/errors.py
+-rw-r--r--   0 runner    (1001) docker     (123)    33736 2023-07-23 13:36:15.000000 gridkit-0.3.1/gridkit/hex_grid.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2384 2023-07-23 13:36:15.000000 gridkit-0.3.1/gridkit/io.py
+-rw-r--r--   0 runner    (1001) docker     (123)    26464 2023-07-23 13:36:15.000000 gridkit-0.3.1/gridkit/rect_grid.py
+-rw-r--r--   0 runner    (1001) docker     (123)       23 2023-07-23 13:36:24.000000 gridkit-0.3.1/gridkit/version.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:36:24.508059 gridkit-0.3.1/gridkit.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1552 2023-07-23 13:36:24.000000 gridkit-0.3.1/gridkit.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      375 2023-07-23 13:36:24.000000 gridkit-0.3.1/gridkit.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 13:36:24.000000 gridkit-0.3.1/gridkit.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      213 2023-07-23 13:36:24.000000 gridkit-0.3.1/gridkit.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        8 2023-07-23 13:36:24.000000 gridkit-0.3.1/gridkit.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 13:36:24.508059 gridkit-0.3.1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1316 2023-07-23 13:36:15.000000 gridkit-0.3.1/setup.py
```

### Comparing `gridkit-0.3.0/LICENSE.txt` & `gridkit-0.3.1/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `gridkit-0.3.0/PKG-INFO` & `gridkit-0.3.1/PKG-INFO`

 * *Files 20% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: gridkit
-Version: 0.3.0
+Version: 0.3.1
 Summary: Powerful abstractions of infinite grids for grid-vector interactions, tesselation, resampling and interactions between related grids.
 Author: Timo Millenaar
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 Provides-Extra: test
@@ -23,14 +23,14 @@
 
 Documentation
 =============
 Find the docs on [GitHub Pages](https://tmillenaar.github.io/GridKit).
 
 Examples
 ========
-Find the examples in the [Example Gallery](https://tmillenaar.github.io/GridKit/example_gallery/index.html) section of the documentation.
+Find examples in the [Example Gallery](https://tmillenaar.github.io/GridKit/example_gallery/index.html) section of the documentation.
 
 Installation
 ============
 To install through PyPi, run `pip install gridkit`.
-Alternatively, clone from [GitHub](https://github.com/tmillenaar/GridKit) and run 
-`pip install ./`
+
+Alternatively, install from source. For this, please refer to the [Contributing guide](https://tmillenaar.github.io/GridKit/contributing.html)
```

### Comparing `gridkit-0.3.0/README.md` & `gridkit-0.3.1/README.md`

 * *Files 8% similar despite different names*

```diff
@@ -10,14 +10,14 @@
 
 Documentation
 =============
 Find the docs on [GitHub Pages](https://tmillenaar.github.io/GridKit).
 
 Examples
 ========
-Find the examples in the [Example Gallery](https://tmillenaar.github.io/GridKit/example_gallery/index.html) section of the documentation.
+Find examples in the [Example Gallery](https://tmillenaar.github.io/GridKit/example_gallery/index.html) section of the documentation.
 
 Installation
 ============
 To install through PyPi, run `pip install gridkit`.
-Alternatively, clone from [GitHub](https://github.com/tmillenaar/GridKit) and run 
-`pip install ./`
+
+Alternatively, install from source. For this, please refer to the [Contributing guide](https://tmillenaar.github.io/GridKit/contributing.html)
```

### Comparing `gridkit-0.3.0/gridkit/_statistical_functions.py` & `gridkit-0.3.1/gridkit/_statistical_functions.py`

 * *Files 4% similar despite different names*

```diff
@@ -26,24 +26,24 @@
     reference = grids[0]
     if not all([grid.is_aligned_with(reference)[0] for grid in grids[1:]]):
         raise AlignmentError(
             "Not all grids are aligned. Please `resample` all grids on the same grid."
         )
 
     combined_bounds = total_bounds(grids)
+    _, shape = grids[0].cells_in_bounds(
+        combined_bounds
+    )  # TODO: split ids and shape outputs into different methods
     combined_data = numpy.full(  # data shape is y,x
-        (
-            round((combined_bounds[3] - combined_bounds[1]) / reference.dy),
-            round((combined_bounds[2] - combined_bounds[0]) / reference.dx),
-        ),
+        shape,
         value,
         dtype=float,  # Fixme: don't hardcode dtype. This if workaround for working with NaNs
     )
 
-    return reference.__class__(combined_data, bounds=combined_bounds, crs=reference.crs)
+    return reference.update(combined_data, bounds=combined_bounds, crs=reference.crs)
 
 
 def count(grids):
     empty_grid = _empty_combined_grid(grids, value=0)
     combined_grid = empty_grid.copy()
     for grid in grids:
         if grid.nodata_value is None:
```

### Comparing `gridkit-0.3.0/gridkit/base_grid.py` & `gridkit-0.3.1/gridkit/base_grid.py`

 * *Files identical despite different names*

### Comparing `gridkit-0.3.0/gridkit/bounded_grid.py` & `gridkit-0.3.1/gridkit/bounded_grid.py`

 * *Files 2% similar despite different names*

```diff
@@ -145,26 +145,26 @@
                         )
                 return dtype, nodata_value
 
             dtype, nodata_value = dominant_dtype_and_nodata_value(left, right)
 
             # create combined grid, spanning both inputs
             combined_bounds = left.combined_bounds(right)
+            _, shape = left.cells_in_bounds(
+                combined_bounds
+            )  # TODO: split ids and shape outputs into different methods
             combined_data = numpy.full(
-                (  # data shape is y,x
-                    round((combined_bounds[3] - combined_bounds[1]) / left.dy),
-                    round((combined_bounds[2] - combined_bounds[0]) / left.dx),
-                ),
+                shape,
                 fill_value=dtype.type(0) if nodata_value is None else nodata_value,
                 dtype=dtype,
             )
-            combined_grid = left.__class__(
+
+            combined_grid = left.update(
                 combined_data,
                 bounds=combined_bounds,
-                crs=left.crs,
                 nodata_value=nodata_value,
             )
 
             shared_bounds = left.shared_bounds(right)
             left_shared = left.crop(shared_bounds)
             right_shared = right.crop(shared_bounds)
 
@@ -176,15 +176,14 @@
             right_data = numpy.ma.masked_array(
                 right_shared._data,
                 right_shared.data == right_shared.nodata_value,
                 dtype=dtype,
             )
 
             result = op(left_data, right_data)
-
             # assign data of `left` to combined_grid
             left_data = left._data.astype(dtype)
             if left.nodata_value is not None:
                 left_data[left._data == left.nodata_value] = nodata_value
             combined_grid.assign(
                 left_data, bounds=left.bounds, in_place=True, assign_nodata=False
             )
@@ -482,16 +481,15 @@
                 crop[mask] = data[mask]
             else:
                 crop[:] = data
         elif anchor:  # a corner or center
             raise NotImplementedError()
         else:
             raise ValueError("Please supply one of: {anchor, bounds}")
-
-        return self.__class__(new_data, bounds=self.bounds, crs=self.crs)
+        return self.update(new_data)
 
     def value(self, index, oob_value=None):
         """Return the value at the given cell index"""
 
         index = numpy.array(index)
         index = index[numpy.newaxis, :] if len(index.shape) == 1 else index
         index = index.T  # TODO: maybe always work with xy axis first
@@ -520,15 +518,15 @@
             )  # the oob_value does not matter if no ids are out of bounds
 
         # Return array's `dtype` needs to be float instead of integer if an id falls outside of bounds
         # For NaNs don't make sense as integer
         if (
             numpy.any(oob_mask)
             and not numpy.isfinite(oob_value)
-            and not numpy.issubdtype(self._data.dtype, float)
+            and not numpy.issubdtype(self._data.dtype, numpy.floating)
         ):
             print(
                 f"Warning: dtype `{self._data.dtype}` might not support an `oob_value` of `{oob_value}`."
             )
 
         values = numpy.full(np_id.shape[1], oob_value, dtype=self._data.dtype)
 
@@ -643,15 +641,15 @@
          3. Find the cells of the original grid that are nearby each of the centroids of the cells found in 2.
             How many nearby cells are selected depends on the selected ``method``
          4. Interpolate the values using the supplied ``method`` at each of the centroids of the alignment grid cells selected in 2.
          5. Create a new bounded grid using the attributes of the alignment grid
 
         Parameters
         ----------
-        alignment_grid: :class:`BaseGrid`
+        alignment_grid: :class:`.BaseGrid`
             The grid with the desired attributes on which to resample.
 
         method: :class:`str`, `'nearest', 'bilinear'`, optional
             The interpolation method used to determine the value at the supplied `sample_points`.
             Supported methods:
             - "nearest", for nearest neigbour interpolation, effectively sampling the value of the data cell containing the point
             - "bilinear", linear interpolation using the four cells surrounding the point
```

### Comparing `gridkit-0.3.0/gridkit/hex_grid.py` & `gridkit-0.3.1/gridkit/hex_grid.py`

 * *Files 2% similar despite different names*

```diff
@@ -483,16 +483,15 @@
 
     def is_aligned_with(self, other):
         if not isinstance(other, BaseGrid):
             raise ValueError(f"Expected a (child of) BaseGrid, got {type(other)}")
         aligned = True
         reason = ""
         reasons = []
-
-        if not isinstance(other.parent_grid_class, self.parent_grid_class):
+        if not other.parent_grid_class == self.parent_grid_class:
             aligned = False
             return (
                 False,
                 f"Grid type is not the same. This is a {self.parent_grid_class}, the other is a {other.parent_grid_class}",
             )
 
         if self.crs is None and other.crs is None:
@@ -806,20 +805,44 @@
     def to_crs(self, crs, resample_method="nearest"):
         new_inf_grid = super(BoundedHexGrid, self).to_crs(
             crs, resample_method=resample_method
         )
         return self.resample(new_inf_grid, method=resample_method)
 
     def numpy_id_to_grid_id(self, np_index):
-        raise NotImplementedError()
         centroid_topleft = (self.bounds[0] + self.dx / 2, self.bounds[3] - self.dy / 2)
         index_topleft = self.cell_at_point(centroid_topleft)
-        return (index_topleft[0] + np_index[1], index_topleft[1] - np_index[0])
+
+        if self._shape == "pointy":
+            index = numpy.array(
+                [
+                    index_topleft[0] + np_index[1],
+                    index_topleft[1]
+                    - np_index[
+                        0
+                    ],  # grid y is numpy [0] and is positive from top to bottom
+                ]
+            )
+            offset_rows = index[1] % 2 == 1
+            index[0][offset_rows] -= 1
+        elif self._shape == "flat":
+            index = numpy.array(
+                [
+                    index_topleft[0] + np_index[0],
+                    index_topleft[1] - np_index[1],
+                ]
+            )
+            offset_rows = index[0] % 2 == 1
+            index[1, offset_rows] -= 1
+
+        return index
 
     def grid_id_to_numpy_id(self, index):
+        index = numpy.array(index)
+
         if self._shape == "pointy":
             offset_rows = index[1] % 2 == 1
             index[0, offset_rows] += 1
         elif self._shape == "flat":
             offset_rows = index[0] % 2 == 1
             index[1, offset_rows] += 1
 
@@ -836,7 +859,21 @@
         # Fixme: in the case of a rectangular grid, a performance improvement can be obtained by using scipy.interpolate.interpn
         return super(BoundedHexGrid, self).interp_nodata(*args, **kwargs)
 
     def centroid(self, index=None):
         if index is None:
             index = self.indices
         return super(BoundedHexGrid, self).centroid(index)
+
+    def update(self, new_data, bounds=None, crs=None, nodata_value=None, shape=None):
+        # TODO figure out how to update size, offset
+        if not bounds:
+            bounds = self.bounds
+        if not crs:
+            crs = self.crs
+        if not nodata_value:
+            nodata_value = self.nodata_value
+        if not shape:
+            shape = self.shape
+        return self.__class__(
+            new_data, bounds=bounds, crs=crs, nodata_value=nodata_value, shape=shape
+        )
```

### Comparing `gridkit-0.3.0/gridkit/io.py` & `gridkit-0.3.1/gridkit/io.py`

 * *Files identical despite different names*

### Comparing `gridkit-0.3.0/gridkit/rect_grid.py` & `gridkit-0.3.1/gridkit/rect_grid.py`

 * *Files identical despite different names*

### Comparing `gridkit-0.3.0/gridkit.egg-info/PKG-INFO` & `gridkit-0.3.1/gridkit.egg-info/PKG-INFO`

 * *Files 20% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: gridkit
-Version: 0.3.0
+Version: 0.3.1
 Summary: Powerful abstractions of infinite grids for grid-vector interactions, tesselation, resampling and interactions between related grids.
 Author: Timo Millenaar
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 Provides-Extra: test
@@ -23,14 +23,14 @@
 
 Documentation
 =============
 Find the docs on [GitHub Pages](https://tmillenaar.github.io/GridKit).
 
 Examples
 ========
-Find the examples in the [Example Gallery](https://tmillenaar.github.io/GridKit/example_gallery/index.html) section of the documentation.
+Find examples in the [Example Gallery](https://tmillenaar.github.io/GridKit/example_gallery/index.html) section of the documentation.
 
 Installation
 ============
 To install through PyPi, run `pip install gridkit`.
-Alternatively, clone from [GitHub](https://github.com/tmillenaar/GridKit) and run 
-`pip install ./`
+
+Alternatively, install from source. For this, please refer to the [Contributing guide](https://tmillenaar.github.io/GridKit/contributing.html)
```

### Comparing `gridkit-0.3.0/setup.py` & `gridkit-0.3.1/setup.py`

 * *Files identical despite different names*

