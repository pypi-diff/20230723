# Comparing `tmp/confluentfucci-0.0.18.tar.gz` & `tmp/confluentfucci-0.0.19.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "confluentfucci-0.0.18.tar", max compression
+gzip compressed data, was "confluentfucci-0.0.19.tar", max compression
```

## Comparing `confluentfucci-0.0.18.tar` & `confluentfucci-0.0.19.tar`

### file list

```diff
@@ -1,8 +1,9 @@
--rw-r--r--   0        0        0     1061 2023-07-21 16:28:40.806139 confluentfucci-0.0.18/LICENSE.txt
--rw-r--r--   0        0        0     1617 2023-07-21 16:28:40.806139 confluentfucci-0.0.18/README.md
--rw-r--r--   0        0        0      351 2023-07-21 16:28:40.806139 confluentfucci-0.0.18/confluentfucci/__init__.py
--rw-r--r--   0        0        0    22575 2023-07-21 16:28:40.806139 confluentfucci-0.0.18/confluentfucci/gui.py
--rw-r--r--   0        0        0    22441 2023-07-21 16:28:40.806139 confluentfucci-0.0.18/confluentfucci/math.py
--rw-r--r--   0        0        0     3909 2023-07-21 16:28:40.806139 confluentfucci-0.0.18/confluentfucci/utils.py
--rw-r--r--   0        0        0     4793 2023-07-21 16:31:47.221152 confluentfucci-0.0.18/pyproject.toml
--rw-r--r--   0        0        0     2695 1970-01-01 00:00:00.000000 confluentfucci-0.0.18/PKG-INFO
+-rw-r--r--   0        0        0     1061 2023-07-23 00:47:30.877846 confluentfucci-0.0.19/LICENSE.txt
+-rw-r--r--   0        0        0     1617 2023-07-23 00:47:30.877846 confluentfucci-0.0.19/README.md
+-rw-r--r--   0        0        0      351 2023-07-23 00:47:30.877846 confluentfucci-0.0.19/confluentfucci/__init__.py
+-rw-r--r--   0        0        0     3841 2023-07-23 00:47:30.877846 confluentfucci-0.0.19/confluentfucci/data.py
+-rw-r--r--   0        0        0    22562 2023-07-23 00:47:30.877846 confluentfucci-0.0.19/confluentfucci/gui.py
+-rw-r--r--   0        0        0    22441 2023-07-23 00:47:30.877846 confluentfucci-0.0.19/confluentfucci/math.py
+-rw-r--r--   0        0        0     4428 2023-07-23 00:47:30.877846 confluentfucci-0.0.19/confluentfucci/utils.py
+-rw-r--r--   0        0        0     4838 2023-07-23 00:50:37.767958 confluentfucci-0.0.19/pyproject.toml
+-rw-r--r--   0        0        0     2776 1970-01-01 00:00:00.000000 confluentfucci-0.0.19/PKG-INFO
```

### Comparing `confluentfucci-0.0.18/LICENSE.txt` & `confluentfucci-0.0.19/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `confluentfucci-0.0.18/README.md` & `confluentfucci-0.0.19/README.md`

 * *Files identical despite different names*

### Comparing `confluentfucci-0.0.18/confluentfucci/gui.py` & `confluentfucci-0.0.19/confluentfucci/gui.py`

 * *Files 5% similar despite different names*

```diff
@@ -15,14 +15,15 @@
 import pandas as pd
 import panel as pn
 import param
 from dask_image.imread import imread
 from shapely import Polygon
 from skimage.exposure import equalize_adapthist
 
+from confluentfucci import data
 from confluentfucci.math import (
     CartesianSimilarity,
     CartesianSimilarityFromFile,
     TrackmateXML,
     compute_voronoi,
     compute_voronoi_stats,
     filter_voronoi_tiling,
@@ -208,18 +209,19 @@
         )
         fig.opts(show_legend=False)
 
         return fig
 
 
 def select_files_model():
+    red_model, green_model = data.fetch_red_model(), data.fetch_green_model()
     root = Tk()
     root.withdraw()
     root.call("wm", "attributes", ".", "-topmost", True)
-    files = filedialog.askopenfilename(initialdir=Path("__file__").cwd().parent / "models/cellpose")
+    files = filedialog.askopenfilename(initialdir=red_model.parent)
     print(files)
     return Path(files)
 
 
 def view_segmented(data_dir_path):
     base_data_path = Path(data_dir_path)
     viewer = napari.Viewer(title="PyFucciTrack Viewer")
@@ -350,22 +352,21 @@
             self.validate_btn.button_type = "danger"
         self.validate_btn.disabled = False
 
     def select_data_folder(self, *b):
         root = Tk()
         root.withdraw()
         root.call("wm", "attributes", ".", "-topmost", True)
-        initial_dir = Path("__file__").cwd().parent.parent / "data"
-        print(initial_dir.absolute(), initial_dir.exists())
-        files = filedialog.askdirectory(initialdir=initial_dir)
+        short_data, long_data = data.fetch_short_example_data(), data.fetch_long_example_data()
+        files = filedialog.askdirectory(initialdir=short_data[0].parent.parent)
         # files = filedialog.askdirectory(
         #     initialdir=r"D:\Data\full_pipeline_tests\left_60_frames"
         # )
 
-        print(files)
+        # print(files)
         self.data_dir_path = Path(files)
 
         red_path = Path(self.data_dir_path) / "red.tif"
         green_path = Path(self.data_dir_path) / "green.tif"
         phase_path = Path(self.data_dir_path) / "phase.tif"
 
         self.red_path = red_path if red_path.exists() else None
@@ -389,19 +390,19 @@
 
     def track(self, event):
         self.run_tracking_btn.disabled = True
         sys.stdout = self.tracking_terminal
 
         (Path(self.data_dir_path) / "metric.h5").unlink(missing_ok=True)
         run_trackmate(
-            Path("__file__").cwd().parent / "models/trackmate/basic_settings.xml",
+            data.fetch_trackmate_settings(),
             Path(self.data_dir_path) / "red_segmented.tiff",
         )
         run_trackmate(
-            Path("__file__").cwd().parent / "models/trackmate/basic_settings.xml",
+            data.fetch_trackmate_settings(),
             Path(self.data_dir_path) / "green_segmented.tiff",
         )
 
         sys.stdout = sys.__stdout__
         self.run_tracking_btn.disabled = False
 
     def segment_one(self):
```

### Comparing `confluentfucci-0.0.18/confluentfucci/math.py` & `confluentfucci-0.0.19/confluentfucci/math.py`

 * *Files identical despite different names*

### Comparing `confluentfucci-0.0.18/confluentfucci/utils.py` & `confluentfucci-0.0.19/confluentfucci/utils.py`

 * *Files 5% similar despite different names*

```diff
@@ -6,14 +6,17 @@
 from pathlib import Path
 from typing import Any
 
 import h5py
 import numpy as np
 import psutil
 import tifffile
+
+# from aicsimageio.transforms import reshape_data
+from aicsimageio.writers import OmeTiffWriter
 from cellpose import models
 from docker.client import DockerClient
 from docker.types import Mount
 from scipy.spatial import Voronoi
 from tqdm import trange
 
 
@@ -51,16 +54,21 @@
         for frame in frame_itertor:
             masks, center_of_mass = _segment_frame(stack[frame, ...], model, gpu=True)
             dataset[frame, :, :] = masks
 
         if export_tiff:
             new_tiff_path = path.parent / f"{path.stem}_segmented.tiff"
             print(f"exporting to tiff at {new_tiff_path}")
-            with tifffile.TiffWriter(new_tiff_path, bigtiff=True) as tif:
-                tif.write(f.get(dataset_name), shape=(frames, Y, X))
+            # TODO wtf? why is tifffile stopped writing TrackMate compatible files?
+            OmeTiffWriter.save(f.get(dataset_name).__array__(), new_tiff_path, dim_order='TYX')
+            # reshaped = reshape_data(f.get(dataset_name), "TYX", "ZTCYX")
+            # tifffile.imwrite(new_tiff_path, f.get(dataset_name), bigtiff=True)
+            # with tifffile.TiffWriter(new_tiff_path, bigtiff=True) as tif:
+            #     tif.write(f.get(dataset_name), shape=(frames, Y, X), metadata={'axes': 'TYX'})
+            # tif.write(reshaped, shape=reshaped.shape)
 
     print("segmentation complete")
 
 
 def _segment_frame(img, model: Path, gpu: bool = False, diameter: int = 18):
     channels = [0, 0]
     net_avg = False
```

### Comparing `confluentfucci-0.0.18/pyproject.toml` & `confluentfucci-0.0.19/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "ConfluentFUCCI"
-version = "0.0.18"
+version = "0.0.19"
 description = ""
 authors = ["Leo Goldstien <leogoldstien@gmail.com>"]
 readme = "README.md"
 packages = [{include = "confluentfucci"}]
 
 [tool.poetry.dependencies]
 loguru = "^0.7.0"
@@ -22,14 +22,16 @@
 torch = [
      {version = "1.12.0", platform = "darwin"},
      {version = "1.12.0", platform = "linux", source = "torch"},
      {version = "1.12.0", platform = "win32", source = "torch"},
  ]
 tables = "^3.8.0"
 tifffile = "2022.5.4"
+botocore = "1.27.26"
+aicsimageio = "^4.11.0"
 
 [[tool.poetry.source]]
 name = "torch"
 url = "https://download.pytorch.org/whl/cu116"
 priority = "supplemental"
 
 [[tool.poetry.source]]
```

### Comparing `confluentfucci-0.0.18/PKG-INFO` & `confluentfucci-0.0.19/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,18 +1,20 @@
 Metadata-Version: 2.1
 Name: confluentfucci
-Version: 0.0.18
+Version: 0.0.19
 Summary: 
 Author: Leo Goldstien
 Author-email: leogoldstien@gmail.com
 Requires-Python: >=3.9,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
+Requires-Dist: aicsimageio (>=4.11.0,<5.0.0)
+Requires-Dist: botocore (==1.27.26)
 Requires-Dist: cellpose (==2.1.0)
 Requires-Dist: dask-image (>=2023.3.0,<2024.0.0)
 Requires-Dist: docker (>=6.1.3,<7.0.0)
 Requires-Dist: h5py (>=3.9.0,<4.0.0)
 Requires-Dist: holoviews (>=1.16.2,<2.0.0)
 Requires-Dist: hvplot (>=0.8.4,<0.9.0)
 Requires-Dist: loguru (>=0.7.0,<0.8.0)
```

