# Comparing `tmp/py4D_browser-0.99.tar.gz` & `tmp/py4D_browser-0.999.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "py4D_browser-0.99.tar", last modified: Fri May 12 19:28:20 2023, max compression
+gzip compressed data, was "py4D_browser-0.999.tar", last modified: Sun Jul 23 13:43:59 2023, max compression
```

## Comparing `py4D_browser-0.99.tar` & `py4D_browser-0.999.tar`

### file list

```diff
@@ -1,21 +1,21 @@
-drwxrwxr-x   0 sez       (1001) sez       (1001)        0 2023-05-12 19:28:20.440576 py4D_browser-0.99/
--rw-rw-r--   0 sez       (1001) sez       (1001)    35135 2023-02-15 14:51:18.000000 py4D_browser-0.99/LICENSE.txt
--rw-rw-r--   0 sez       (1001) sez       (1001)     1965 2023-05-12 19:28:20.440576 py4D_browser-0.99/PKG-INFO
--rw-rw-r--   0 sez       (1001) sez       (1001)     1475 2023-05-11 18:22:43.000000 py4D_browser-0.99/README.md
--rw-rw-r--   0 sez       (1001) sez       (1001)      751 2023-05-12 18:58:53.000000 py4D_browser-0.99/pyproject.toml
--rw-rw-r--   0 sez       (1001) sez       (1001)       38 2023-05-12 19:28:20.440576 py4D_browser-0.99/setup.cfg
-drwxrwxr-x   0 sez       (1001) sez       (1001)        0 2023-05-12 19:28:20.440576 py4D_browser-0.99/src/
-drwxrwxr-x   0 sez       (1001) sez       (1001)        0 2023-05-12 19:28:20.440576 py4D_browser-0.99/src/py4D_browser/
--rw-rw-r--   0 sez       (1001) sez       (1001)       48 2023-02-15 14:51:18.000000 py4D_browser-0.99/src/py4D_browser/__init__.py
--rw-rw-r--   0 sez       (1001) sez       (1001)    12228 2023-05-11 18:22:18.000000 py4D_browser-0.99/src/py4D_browser/main_window.py
--rw-rw-r--   0 sez       (1001) sez       (1001)     2079 2023-05-11 18:22:18.000000 py4D_browser-0.99/src/py4D_browser/menu_actions.py
--rw-rw-r--   0 sez       (1001) sez       (1001)      271 2023-02-15 14:51:18.000000 py4D_browser-0.99/src/py4D_browser/runGUI.py
--rw-rw-r--   0 sez       (1001) sez       (1001)    11785 2023-05-11 18:22:18.000000 py4D_browser-0.99/src/py4D_browser/update_views.py
--rw-rw-r--   0 sez       (1001) sez       (1001)      490 2023-05-11 18:22:18.000000 py4D_browser-0.99/src/py4D_browser/utils.py
-drwxrwxr-x   0 sez       (1001) sez       (1001)        0 2023-05-12 19:28:20.440576 py4D_browser-0.99/src/py4D_browser.egg-info/
--rw-rw-r--   0 sez       (1001) sez       (1001)     1965 2023-05-12 19:28:20.000000 py4D_browser-0.99/src/py4D_browser.egg-info/PKG-INFO
--rw-rw-r--   0 sez       (1001) sez       (1001)      458 2023-05-12 19:28:20.000000 py4D_browser-0.99/src/py4D_browser.egg-info/SOURCES.txt
--rw-rw-r--   0 sez       (1001) sez       (1001)        1 2023-05-12 19:28:20.000000 py4D_browser-0.99/src/py4D_browser.egg-info/dependency_links.txt
--rw-rw-r--   0 sez       (1001) sez       (1001)       55 2023-05-12 19:28:20.000000 py4D_browser-0.99/src/py4D_browser.egg-info/entry_points.txt
--rw-rw-r--   0 sez       (1001) sez       (1001)       75 2023-05-12 19:28:20.000000 py4D_browser-0.99/src/py4D_browser.egg-info/requires.txt
--rw-rw-r--   0 sez       (1001) sez       (1001)       13 2023-05-12 19:28:20.000000 py4D_browser-0.99/src/py4D_browser.egg-info/top_level.txt
+drwxr-xr-x   0 sez        (501) staff       (20)        0 2023-07-23 13:43:59.323346 py4D_browser-0.999/
+-rw-r--r--   0 sez        (501) staff       (20)    35135 2022-06-01 20:45:18.000000 py4D_browser-0.999/LICENSE.txt
+-rw-r--r--   0 sez        (501) staff       (20)     1851 2023-07-23 13:43:59.323210 py4D_browser-0.999/PKG-INFO
+-rw-r--r--   0 sez        (501) staff       (20)     1360 2023-07-23 13:41:15.000000 py4D_browser-0.999/README.md
+-rw-r--r--   0 sez        (501) staff       (20)      752 2023-07-23 13:40:14.000000 py4D_browser-0.999/pyproject.toml
+-rw-r--r--   0 sez        (501) staff       (20)       38 2023-07-23 13:43:59.323386 py4D_browser-0.999/setup.cfg
+drwxr-xr-x   0 sez        (501) staff       (20)        0 2023-07-23 13:43:59.320032 py4D_browser-0.999/src/
+drwxr-xr-x   0 sez        (501) staff       (20)        0 2023-07-23 13:43:59.322174 py4D_browser-0.999/src/py4D_browser/
+-rw-r--r--   0 sez        (501) staff       (20)       48 2023-05-15 18:50:54.000000 py4D_browser-0.999/src/py4D_browser/__init__.py
+-rw-r--r--   0 sez        (501) staff       (20)    12228 2023-05-15 18:50:54.000000 py4D_browser-0.999/src/py4D_browser/main_window.py
+-rw-r--r--   0 sez        (501) staff       (20)     2166 2023-07-23 13:37:16.000000 py4D_browser-0.999/src/py4D_browser/menu_actions.py
+-rw-r--r--   0 sez        (501) staff       (20)      271 2023-05-15 18:50:54.000000 py4D_browser-0.999/src/py4D_browser/runGUI.py
+-rw-r--r--   0 sez        (501) staff       (20)    11831 2023-07-23 13:36:49.000000 py4D_browser-0.999/src/py4D_browser/update_views.py
+-rw-r--r--   0 sez        (501) staff       (20)      490 2023-05-15 18:50:54.000000 py4D_browser-0.999/src/py4D_browser/utils.py
+drwxr-xr-x   0 sez        (501) staff       (20)        0 2023-07-23 13:43:59.323039 py4D_browser-0.999/src/py4D_browser.egg-info/
+-rw-r--r--   0 sez        (501) staff       (20)     1851 2023-07-23 13:43:59.000000 py4D_browser-0.999/src/py4D_browser.egg-info/PKG-INFO
+-rw-r--r--   0 sez        (501) staff       (20)      458 2023-07-23 13:43:59.000000 py4D_browser-0.999/src/py4D_browser.egg-info/SOURCES.txt
+-rw-r--r--   0 sez        (501) staff       (20)        1 2023-07-23 13:43:59.000000 py4D_browser-0.999/src/py4D_browser.egg-info/dependency_links.txt
+-rw-r--r--   0 sez        (501) staff       (20)       55 2023-07-23 13:43:59.000000 py4D_browser-0.999/src/py4D_browser.egg-info/entry_points.txt
+-rw-r--r--   0 sez        (501) staff       (20)       75 2023-07-23 13:43:59.000000 py4D_browser-0.999/src/py4D_browser.egg-info/requires.txt
+-rw-r--r--   0 sez        (501) staff       (20)       13 2023-07-23 13:43:59.000000 py4D_browser-0.999/src/py4D_browser.egg-info/top_level.txt
```

### Comparing `py4D_browser-0.99/LICENSE.txt` & `py4D_browser-0.999/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `py4D_browser-0.99/PKG-INFO` & `py4D_browser-0.999/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: py4D_browser
-Version: 0.99
+Version: 0.999
 Summary: A 4D-STEM data browser built on py4DSTEM.
 Author-email: Steven Zeltmann <steven.zeltmann@berkeley.edu>
 Project-URL: Homepage, https://github.com/py4dstem/py4D-browser
 Project-URL: Bug Tracker, https://github.com/py4dstem/py4D-browser/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.9
@@ -13,18 +13,20 @@
 
 
 # The `py4DSTEM` GUI
 
 This repository hosts the `pyqt` based graphical 4D--STEM data browser that was originally part of **py4DSTEM** until version 0.13.11. 
 
 ## Installation 
-Currently, to install you must download or clone the repo and run `python setup.py`.
-`pip` and `conda` installation will be available shortly.
+The GUI is available on PyPI and conda-forge: 
+
+`pip install py4D-browser`
+
+`conda install -c conda-forge py4d-browser`
 
-You can shortcut this by running `pip install git+https://github.com/py4dstem/py4D-browser`
 
 ## Usage
 Run `py4DGUI` in your terminal to open the GUI. Then just drag and drop a 4D-STEM dataset into the window!
 
 ![Demonstration](/images/demo.gif)
 
 ## About
```

### Comparing `py4D_browser-0.99/README.md` & `py4D_browser-0.999/README.md`

 * *Files 10% similar despite different names*

```diff
@@ -1,17 +1,19 @@
 
 # The `py4DSTEM` GUI
 
 This repository hosts the `pyqt` based graphical 4D--STEM data browser that was originally part of **py4DSTEM** until version 0.13.11. 
 
 ## Installation 
-Currently, to install you must download or clone the repo and run `python setup.py`.
-`pip` and `conda` installation will be available shortly.
+The GUI is available on PyPI and conda-forge: 
+
+`pip install py4D-browser`
+
+`conda install -c conda-forge py4d-browser`
 
-You can shortcut this by running `pip install git+https://github.com/py4dstem/py4D-browser`
 
 ## Usage
 Run `py4DGUI` in your terminal to open the GUI. Then just drag and drop a 4D-STEM dataset into the window!
 
 ![Demonstration](/images/demo.gif)
 
 ## About
```

### Comparing `py4D_browser-0.99/pyproject.toml` & `py4D_browser-0.999/pyproject.toml`

 * *Files 16% similar despite different names*

```diff
@@ -1,26 +1,26 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "py4D_browser"
-version = "0.99"
+version = "0.999"
 authors = [
   { name="Steven Zeltmann", email="steven.zeltmann@berkeley.edu" },
 ]
 description = "A 4D-STEM data browser built on py4DSTEM."
 readme = "README.md"
 requires-python = ">=3.9"
 classifiers = [
     "Programming Language :: Python :: 3",
     "Operating System :: OS Independent",
 ]
 dependencies = [
-  "py4dstem >= 0.14.0",
+  "py4dstem >= 0.14.3",
   "numpy >= 1.19",
   "matplotlib >= 3.2.2",
   "PyQt5 >= 5.10",
   "pyqtgraph >= 0.11",
 ]
 
 [project.scripts]
```

### Comparing `py4D_browser-0.99/src/py4D_browser/main_window.py` & `py4D_browser-0.999/src/py4D_browser/main_window.py`

 * *Files identical despite different names*

### Comparing `py4D_browser-0.99/src/py4D_browser/menu_actions.py` & `py4D_browser-0.999/src/py4D_browser/menu_actions.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,10 +1,11 @@
 import py4DSTEM
 from PyQt5.QtWidgets import QFileDialog
 import h5py
+import os
 
 
 def load_data_auto(self):
     filename = self.show_file_dialog()
     self.load_file(filename)
 
 
@@ -17,17 +18,16 @@
     # TODO: Ask user for binning level
     filename = self.show_file_dialog()
     self.load_file(filename, mmap=False, binning=4)
 
 
 def load_file(self, filepath, mmap=False, binning=1):
     print(f"Loading file {filepath}")
-
-    from py4DSTEM.io.parsefiletype import _parse_filetype
-    if _parse_filetype(filepath) == "H5":
+    print(f"Type: {os.path.splitext(filepath)[-1].lower()}")
+    if os.path.splitext(filepath)[-1].lower() in (".h5", ".hdf5", ".py4dstem", ".emd"):
         datacubes = get_4D(h5py.File(filepath, "r"))
         print(f"Found {len(datacubes)} 4D datasets inside the HDF5 file...")
         if len(datacubes) >= 1:
             # Read the first datacube in the HDF5 file into RAM
             print(f"Reading dataset at location {datacubes[0].name}")
             self.datacube = py4DSTEM.DataCube(
                 datacubes[0] if mmap else datacubes[0][()]
@@ -46,15 +46,15 @@
 
 
 def show_file_dialog(self):
     filename = QFileDialog.getOpenFileName(
         self,
         "Open 4D-STEM Data",
         "",
-        "4D-STEM Data (*.dm3 *.dm4 *.raw *.mib *.gtg);;Any file (*)",
+        "4D-STEM Data (*.dm3 *.dm4 *.raw *.mib *.gtg *.h5 *.hdf5 *.emd *.py4dstem);;Any file (*)",
     )
     if filename is not None and len(filename[0]) > 0:
         return filename[0]
     else:
         print("File was invalid, or something?")
         raise ValueError("Could not read file")
```

### Comparing `py4D_browser-0.99/src/py4D_browser/update_views.py` & `py4D_browser-0.999/src/py4D_browser/update_views.py`

 * *Files 2% similar despite different names*

```diff
@@ -60,15 +60,15 @@
         )
         x0 = (slice_x.start + slice_x.stop) / 2.0
         y0 = (slice_y.start + slice_y.stop) / 2.0
         R = (slice_y.stop - slice_y.start) / 2.0
 
         self.diffraction_space_view_text.setText(f"[({x0},{y0}),{R}]")
 
-        mask = py4DSTEM.process.virtualimage.make_detector(
+        mask = py4DSTEM.datacube.virtualimage.DataCubeVirtualImager.make_detector(
             (self.datacube.Q_Nx, self.datacube.Q_Ny), "circle", ((x0, y0), R)
         )
     elif detector_shape == "Annulus":
         (slice_x, slice_y), _ = self.virtual_detector_roi_outer.getArraySlice(
             self.datacube.data[0, 0, :, :], self.diffraction_space_widget.getImageItem()
         )
         x0 = (slice_x.start + slice_x.stop) / 2.0
@@ -81,15 +81,15 @@
         R_inner = (slice_iy.stop - slice_iy.start) / 2.0
 
         if R_inner == R_outer:
             R_inner -= 1
 
         self.diffraction_space_view_text.setText(f"[({x0},{y0}),({R_inner},{R_outer})]")
 
-        mask = py4DSTEM.process.virtualimage.make_detector(
+        mask = py4DSTEM.datacube.virtualimage.DataCubeVirtualImager.make_detector(
             (self.datacube.Q_Nx, self.datacube.Q_Ny),
             "annulus",
             ((x0, y0), (R_inner, R_outer)),
         )
     elif detector_shape == "Point":
         roi_state = self.virtual_detector_point.saveState()
         y0, x0 = roi_state["pos"]
```

### Comparing `py4D_browser-0.99/src/py4D_browser.egg-info/PKG-INFO` & `py4D_browser-0.999/src/py4D_browser.egg-info/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: py4D-browser
-Version: 0.99
+Version: 0.999
 Summary: A 4D-STEM data browser built on py4DSTEM.
 Author-email: Steven Zeltmann <steven.zeltmann@berkeley.edu>
 Project-URL: Homepage, https://github.com/py4dstem/py4D-browser
 Project-URL: Bug Tracker, https://github.com/py4dstem/py4D-browser/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.9
@@ -13,18 +13,20 @@
 
 
 # The `py4DSTEM` GUI
 
 This repository hosts the `pyqt` based graphical 4D--STEM data browser that was originally part of **py4DSTEM** until version 0.13.11. 
 
 ## Installation 
-Currently, to install you must download or clone the repo and run `python setup.py`.
-`pip` and `conda` installation will be available shortly.
+The GUI is available on PyPI and conda-forge: 
+
+`pip install py4D-browser`
+
+`conda install -c conda-forge py4d-browser`
 
-You can shortcut this by running `pip install git+https://github.com/py4dstem/py4D-browser`
 
 ## Usage
 Run `py4DGUI` in your terminal to open the GUI. Then just drag and drop a 4D-STEM dataset into the window!
 
 ![Demonstration](/images/demo.gif)
 
 ## About
```

