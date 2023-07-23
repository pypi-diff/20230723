# Comparing `tmp/nb-thumb-0.0.8.tar.gz` & `tmp/nb-thumb-0.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nb-thumb-0.0.8.tar", last modified: Sat Jul 15 06:20:57 2023, max compression
+gzip compressed data, was "nb-thumb-0.0.9.tar", last modified: Sun Jul 23 16:20:02 2023, max compression
```

## Comparing `nb-thumb-0.0.8.tar` & `nb-thumb-0.0.9.tar`

### file list

```diff
@@ -1,22 +1,22 @@
-drwxr-xr-x   0 hamel      (501) staff       (20)        0 2023-07-15 06:20:57.576291 nb-thumb-0.0.8/
--rw-rw-r--   0 hamel      (501) staff       (20)    11337 2023-04-27 10:12:58.000000 nb-thumb-0.0.8/LICENSE
--rw-rw-r--   0 hamel      (501) staff       (20)      111 2023-04-27 10:12:58.000000 nb-thumb-0.0.8/MANIFEST.in
--rw-r--r--   0 hamel      (501) staff       (20)     2424 2023-07-15 06:20:57.576148 nb-thumb-0.0.8/PKG-INFO
--rw-r--r--   0 hamel      (501) staff       (20)     1623 2023-07-15 06:20:37.000000 nb-thumb-0.0.8/README.md
-drwxr-xr-x   0 hamel      (501) staff       (20)        0 2023-07-15 06:20:57.574983 nb-thumb-0.0.8/nb_thumb/
--rw-r--r--   0 hamel      (501) staff       (20)       96 2023-07-15 06:20:43.000000 nb-thumb-0.0.8/nb_thumb/__init__.py
--rw-r--r--   0 hamel      (501) staff       (20)     1014 2023-07-15 06:20:43.000000 nb-thumb-0.0.8/nb_thumb/_modidx.py
--rw-r--r--   0 hamel      (501) staff       (20)      142 2023-07-14 03:45:28.000000 nb-thumb-0.0.8/nb_thumb/core.py
--rw-r--r--   0 hamel      (501) staff       (20)     1665 2023-07-15 06:20:43.000000 nb-thumb-0.0.8/nb_thumb/gallery.py
--rw-r--r--   0 hamel      (501) staff       (20)     1948 2023-07-15 06:20:43.000000 nb-thumb-0.0.8/nb_thumb/thumb.py
-drwxr-xr-x   0 hamel      (501) staff       (20)        0 2023-07-15 06:20:57.575967 nb-thumb-0.0.8/nb_thumb.egg-info/
--rw-r--r--   0 hamel      (501) staff       (20)     2424 2023-07-15 06:20:57.000000 nb-thumb-0.0.8/nb_thumb.egg-info/PKG-INFO
--rw-r--r--   0 hamel      (501) staff       (20)      372 2023-07-15 06:20:57.000000 nb-thumb-0.0.8/nb_thumb.egg-info/SOURCES.txt
--rw-r--r--   0 hamel      (501) staff       (20)        1 2023-07-15 06:20:57.000000 nb-thumb-0.0.8/nb_thumb.egg-info/dependency_links.txt
--rw-r--r--   0 hamel      (501) staff       (20)       38 2023-07-15 06:20:57.000000 nb-thumb-0.0.8/nb_thumb.egg-info/entry_points.txt
--rw-r--r--   0 hamel      (501) staff       (20)        1 2023-07-14 05:34:35.000000 nb-thumb-0.0.8/nb_thumb.egg-info/not-zip-safe
--rw-r--r--   0 hamel      (501) staff       (20)       46 2023-07-15 06:20:57.000000 nb-thumb-0.0.8/nb_thumb.egg-info/requires.txt
--rw-r--r--   0 hamel      (501) staff       (20)        9 2023-07-15 06:20:57.000000 nb-thumb-0.0.8/nb_thumb.egg-info/top_level.txt
--rw-r--r--   0 hamel      (501) staff       (20)      850 2023-07-15 06:20:43.000000 nb-thumb-0.0.8/settings.ini
--rw-r--r--   0 hamel      (501) staff       (20)       38 2023-07-15 06:20:57.576341 nb-thumb-0.0.8/setup.cfg
--rw-rw-r--   0 hamel      (501) staff       (20)     2596 2023-04-27 10:12:58.000000 nb-thumb-0.0.8/setup.py
+drwxr-xr-x   0 hamel      (501) staff       (20)        0 2023-07-23 16:20:02.899628 nb-thumb-0.0.9/
+-rw-rw-r--   0 hamel      (501) staff       (20)    11337 2023-04-27 10:12:58.000000 nb-thumb-0.0.9/LICENSE
+-rw-rw-r--   0 hamel      (501) staff       (20)      111 2023-04-27 10:12:58.000000 nb-thumb-0.0.9/MANIFEST.in
+-rw-r--r--   0 hamel      (501) staff       (20)     2424 2023-07-23 16:20:02.899474 nb-thumb-0.0.9/PKG-INFO
+-rw-r--r--   0 hamel      (501) staff       (20)     1623 2023-07-23 16:19:41.000000 nb-thumb-0.0.9/README.md
+drwxr-xr-x   0 hamel      (501) staff       (20)        0 2023-07-23 16:20:02.898113 nb-thumb-0.0.9/nb_thumb/
+-rw-r--r--   0 hamel      (501) staff       (20)       96 2023-07-23 16:19:46.000000 nb-thumb-0.0.9/nb_thumb/__init__.py
+-rw-r--r--   0 hamel      (501) staff       (20)     1014 2023-07-23 16:19:46.000000 nb-thumb-0.0.9/nb_thumb/_modidx.py
+-rw-r--r--   0 hamel      (501) staff       (20)      142 2023-07-14 03:45:28.000000 nb-thumb-0.0.9/nb_thumb/core.py
+-rw-r--r--   0 hamel      (501) staff       (20)     1692 2023-07-23 16:19:46.000000 nb-thumb-0.0.9/nb_thumb/gallery.py
+-rw-r--r--   0 hamel      (501) staff       (20)     1948 2023-07-23 16:19:46.000000 nb-thumb-0.0.9/nb_thumb/thumb.py
+drwxr-xr-x   0 hamel      (501) staff       (20)        0 2023-07-23 16:20:02.899240 nb-thumb-0.0.9/nb_thumb.egg-info/
+-rw-r--r--   0 hamel      (501) staff       (20)     2424 2023-07-23 16:20:02.000000 nb-thumb-0.0.9/nb_thumb.egg-info/PKG-INFO
+-rw-r--r--   0 hamel      (501) staff       (20)      372 2023-07-23 16:20:02.000000 nb-thumb-0.0.9/nb_thumb.egg-info/SOURCES.txt
+-rw-r--r--   0 hamel      (501) staff       (20)        1 2023-07-23 16:20:02.000000 nb-thumb-0.0.9/nb_thumb.egg-info/dependency_links.txt
+-rw-r--r--   0 hamel      (501) staff       (20)       38 2023-07-23 16:20:02.000000 nb-thumb-0.0.9/nb_thumb.egg-info/entry_points.txt
+-rw-r--r--   0 hamel      (501) staff       (20)        1 2023-07-14 05:34:35.000000 nb-thumb-0.0.9/nb_thumb.egg-info/not-zip-safe
+-rw-r--r--   0 hamel      (501) staff       (20)       46 2023-07-23 16:20:02.000000 nb-thumb-0.0.9/nb_thumb.egg-info/requires.txt
+-rw-r--r--   0 hamel      (501) staff       (20)        9 2023-07-23 16:20:02.000000 nb-thumb-0.0.9/nb_thumb.egg-info/top_level.txt
+-rw-r--r--   0 hamel      (501) staff       (20)      850 2023-07-23 16:19:46.000000 nb-thumb-0.0.9/settings.ini
+-rw-r--r--   0 hamel      (501) staff       (20)       38 2023-07-23 16:20:02.899672 nb-thumb-0.0.9/setup.cfg
+-rw-rw-r--   0 hamel      (501) staff       (20)     2596 2023-04-27 10:12:58.000000 nb-thumb-0.0.9/setup.py
```

### Comparing `nb-thumb-0.0.8/LICENSE` & `nb-thumb-0.0.9/LICENSE`

 * *Files identical despite different names*

### Comparing `nb-thumb-0.0.8/PKG-INFO` & `nb-thumb-0.0.9/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nb-thumb
-Version: 0.0.8
+Version: 0.0.9
 Summary: Extract thumbnails from Jupyter notebooks
 Home-page: https://github.com/fastai/nb-thumb
 Author: Hamel Husain
 Author-email: hamel.husain@gmail.com
 License: Apache Software License 2.0
 Keywords: nbdev jupyter notebook python
 Platform: UNKNOWN
```

### Comparing `nb-thumb-0.0.8/README.md` & `nb-thumb-0.0.9/README.md`

 * *Files identical despite different names*

### Comparing `nb-thumb-0.0.8/nb_thumb/_modidx.py` & `nb-thumb-0.0.9/nb_thumb/_modidx.py`

 * *Files identical despite different names*

### Comparing `nb-thumb-0.0.8/nb_thumb/gallery.py` & `nb-thumb-0.0.9/nb_thumb/gallery.py`

 * *Files 6% similar despite different names*

```diff
@@ -15,15 +15,15 @@
             label:str, # the label indicating the cell where the plot is, see https://quarto.org/docs/authoring/notebook-embed.html#code-cell-options for an example.
             caption:str='', # the caption, will be inferred from label if not specified.
             anchor='#example', # anchor tag in source page, this defaults to `#example` for plotnine: https://plotnine.readthedocs.io
            size=(150,150) # size of the thumbnail
            ) -> str:
     "Embed a thumbnail image as a markdown cell."
     if not caption: caption = label.replace('_', ' ').title()
-    d = mkdir(f'{Path(nb_path).stem}_data', exist_ok=True)
+    d = mkdir(f'gallery_plot_data/{Path(nb_path).stem}', exist_ok=True, parents=True)
     img = nb2thumb(nb_path, label=label, size=size)
     outfile = d/f'{label}.png'
     img.save(outfile)
     
     return f"""
 ::: {{.g-col-6 .g-col-md-6 .mb-4 .border .rounded .shadow-sm .d-flex .flex-column .justify-content-center .align-items-center .px-3}}
```

### Comparing `nb-thumb-0.0.8/nb_thumb/thumb.py` & `nb-thumb-0.0.9/nb_thumb/thumb.py`

 * *Files identical despite different names*

### Comparing `nb-thumb-0.0.8/nb_thumb.egg-info/PKG-INFO` & `nb-thumb-0.0.9/nb_thumb.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nb-thumb
-Version: 0.0.8
+Version: 0.0.9
 Summary: Extract thumbnails from Jupyter notebooks
 Home-page: https://github.com/fastai/nb-thumb
 Author: Hamel Husain
 Author-email: hamel.husain@gmail.com
 License: Apache Software License 2.0
 Keywords: nbdev jupyter notebook python
 Platform: UNKNOWN
```

### Comparing `nb-thumb-0.0.8/settings.ini` & `nb-thumb-0.0.9/settings.ini`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 [DEFAULT]
 repo = nb-thumb
 lib_name = nb-thumb
-version = 0.0.8
+version = 0.0.9
 min_python = 3.7
 license = apache2
 black_formatting = False
 doc_path = _docs
 lib_path = nb_thumb
 nbs_path = nbs
 recursive = True
```

### Comparing `nb-thumb-0.0.8/setup.py` & `nb-thumb-0.0.9/setup.py`

 * *Files identical despite different names*

