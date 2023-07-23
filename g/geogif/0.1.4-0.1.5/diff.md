# Comparing `tmp/geogif-0.1.4.tar.gz` & `tmp/geogif-0.1.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "geogif-0.1.4.tar", max compression
+gzip compressed data, was "geogif-0.1.5.tar", max compression
```

## Comparing `geogif-0.1.4.tar` & `geogif-0.1.5.tar`

### file list

```diff
@@ -1,13 +1,6 @@
--rw-r--r--   0        0        0     1067 2021-05-01 05:47:29.391768 geogif-0.1.4/LICENSE
--rw-r--r--   0        0        0     1829 2023-02-10 04:19:12.431810 geogif-0.1.4/README.md
--rw-r--r--   0        0        0    20988 2021-05-01 06:26:58.983187 geogif-0.1.4/geogif/.hypothesis/unicode_data/13.0.0/charmap.json.gz
--rw-r--r--   0        0        0       37 2021-05-01 07:10:48.729947 geogif-0.1.4/geogif/.pytest_cache/.gitignore
--rw-r--r--   0        0        0      194 2021-05-01 07:10:48.730075 geogif-0.1.4/geogif/.pytest_cache/CACHEDIR.TAG
--rw-r--r--   0        0        0      295 2021-05-01 07:10:48.729805 geogif-0.1.4/geogif/.pytest_cache/README.md
--rw-r--r--   0        0        0        2 2021-05-01 07:10:48.730226 geogif-0.1.4/geogif/.pytest_cache/v/cache/nodeids
--rw-r--r--   0        0        0        2 2021-05-01 07:10:48.730465 geogif-0.1.4/geogif/.pytest_cache/v/cache/stepwise
--rw-r--r--   0        0        0      321 2022-03-17 03:06:09.675312 geogif-0.1.4/geogif/__init__.py
--rw-r--r--   0        0        0    15973 2021-05-03 05:29:36.977366 geogif-0.1.4/geogif/gif.py
--rw-r--r--   0        0        0     1144 2023-02-10 04:19:12.433764 geogif-0.1.4/pyproject.toml
--rw-r--r--   0        0        0     2772 1970-01-01 00:00:00.000000 geogif-0.1.4/setup.py
--rw-r--r--   0        0        0     2615 1970-01-01 00:00:00.000000 geogif-0.1.4/PKG-INFO
+-rw-r--r--   0        0        0     1067 2021-05-01 05:47:29.391768 geogif-0.1.5/LICENSE
+-rw-r--r--   0        0        0     1829 2023-02-10 04:19:12.431810 geogif-0.1.5/README.md
+-rw-r--r--   0        0        0      321 2022-03-17 03:06:09.675312 geogif-0.1.5/geogif/__init__.py
+-rw-r--r--   0        0        0    16117 2023-07-23 19:04:01.315151 geogif-0.1.5/geogif/gif.py
+-rw-r--r--   0        0        0     1141 2023-07-23 19:04:01.317492 geogif-0.1.5/pyproject.toml
+-rw-r--r--   0        0        0     2608 1970-01-01 00:00:00.000000 geogif-0.1.5/PKG-INFO
```

### Comparing `geogif-0.1.4/LICENSE` & `geogif-0.1.5/LICENSE`

 * *Files identical despite different names*

### Comparing `geogif-0.1.4/README.md` & `geogif-0.1.5/README.md`

 * *Files identical despite different names*

### Comparing `geogif-0.1.4/geogif/gif.py` & `geogif-0.1.5/geogif/gif.py`

 * *Files 1% similar despite different names*

```diff
@@ -31,14 +31,17 @@
         )
     if arr.ndim == 3:
         arr = arr.expand_dims("band", axis=1)
 
     if arr.shape[1] not in (1, 3):
         raise ValueError(f"Array must have 1 or 3 bands, not {arr.shape[1]}")
 
+    if arr.size == 0:
+        raise ValueError("Array is empty")
+
     if arr.shape[1] == 1:
         cmap = (
             # this will use the default colormap (usually viridis) if it's None
             matplotlib.cm.get_cmap(cmap)
             if not isinstance(cmap, matplotlib.colors.Colormap)
             else cmap
         )
@@ -207,15 +210,17 @@
         fnt = ImageFont.load_default()
         for label, img in zip(labels, imgs):
             # get a drawing context
             d = ImageDraw.Draw(img)
             d = cast(ImageDraw.ImageDraw, d)
 
             width, height = img.size
-            t_width, t_height = fnt.getsize(label)
+            t_bbox = fnt.getbbox(label)
+            t_width = t_bbox[2] - t_bbox[0]
+            t_height = t_bbox[3] - t_bbox[1]
 
             offset = 15
             if date_position[0] == "u":
                 y = offset
             else:
                 y = height - t_height - offset
```

### Comparing `geogif-0.1.4/pyproject.toml` & `geogif-0.1.5/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,21 +1,21 @@
 [tool.poetry]
 name = "geogif"
-version = "0.1.4"
+version = "0.1.5"
 description = "Render xarray timestacks into GIFs"
 authors = ["Gabe Joseph <gjoseph92@gmail.com>"]
 readme = "README.md"
 repository = "https://github.com/gjoseph92/geogif"
 homepage = "https://geogif.readthedocs.io/en/latest/index.html"
 
 [tool.poetry.dependencies]
 python = "^3.8"
 dask = {extras = ["delayed"], version = ">= 2021.4.1"}
 numpy = "^1.20.2"
-Pillow = "^9.0.1"
+Pillow = "^10"
 matplotlib = "^3.4.1"
 xarray = ">=0.18"
 
 [tool.poetry.group.dev.dependencies]
 jupyterlab = "^3.0.14"
 ipython = "^7.23.0"
 black = "^21.4b2"
```

### Comparing `geogif-0.1.4/PKG-INFO` & `geogif-0.1.5/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,21 +1,21 @@
 Metadata-Version: 2.1
 Name: geogif
-Version: 0.1.4
+Version: 0.1.5
 Summary: Render xarray timestacks into GIFs
 Home-page: https://geogif.readthedocs.io/en/latest/index.html
 Author: Gabe Joseph
 Author-email: gjoseph92@gmail.com
 Requires-Python: >=3.8,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
-Requires-Dist: Pillow (>=9.0.1,<10.0.0)
+Requires-Dist: Pillow (>=10,<11)
 Requires-Dist: dask[delayed] (>=2021.4.1)
 Requires-Dist: matplotlib (>=3.4.1,<4.0.0)
 Requires-Dist: numpy (>=1.20.2,<2.0.0)
 Requires-Dist: xarray (>=0.18)
 Project-URL: Repository, https://github.com/gjoseph92/geogif
 Description-Content-Type: text/markdown
```

