# Comparing `tmp/wf-cv-utils-3.6.0.tar.gz` & `tmp/wf-cv-utils-3.6.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "wf-cv-utils-3.6.0.tar", last modified: Sun Jul 16 23:35:06 2023, max compression
+gzip compressed data, was "wf-cv-utils-3.6.1.tar", last modified: Sun Jul 23 14:48:13 2023, max compression
```

## Comparing `wf-cv-utils-3.6.0.tar` & `wf-cv-utils-3.6.1.tar`

### file list

```diff
@@ -1,26 +1,26 @@
-drwxrwxr-x   0 tcquinn   (1001) tcquinn   (1001)        0 2023-07-16 23:35:05.995186 wf-cv-utils-3.6.0/
--rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)     1088 2022-12-08 20:56:25.000000 wf-cv-utils-3.6.0/LICENSE
--rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)       34 2022-12-08 20:56:25.000000 wf-cv-utils-3.6.0/MANIFEST.in
--rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)     1999 2023-07-16 23:35:05.995186 wf-cv-utils-3.6.0/PKG-INFO
--rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)     1495 2022-12-08 20:56:25.000000 wf-cv-utils-3.6.0/README.md
--rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)        5 2023-07-16 23:32:31.000000 wf-cv-utils-3.6.0/VERSION
-drwxrwxr-x   0 tcquinn   (1001) tcquinn   (1001)        0 2023-07-16 23:35:05.995186 wf-cv-utils-3.6.0/cv_utils/
--rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)      225 2023-07-16 22:05:06.000000 wf-cv-utils-3.6.0/cv_utils/__init__.py
--rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)    34095 2023-07-16 22:03:30.000000 wf-cv-utils-3.6.0/cv_utils/aruco.py
--rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)    16002 2023-07-16 23:25:41.000000 wf-cv-utils-3.6.0/cv_utils/colmap.py
--rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)      380 2023-07-16 22:03:25.000000 wf-cv-utils-3.6.0/cv_utils/color.py
--rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)    24991 2023-07-16 22:03:24.000000 wf-cv-utils-3.6.0/cv_utils/core.py
-drwxrwxr-x   0 tcquinn   (1001) tcquinn   (1001)        0 2023-07-16 23:35:05.995186 wf-cv-utils-3.6.0/cv_utils/drawing/
--rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)        0 2022-12-08 20:56:25.000000 wf-cv-utils-3.6.0/cv_utils/drawing/__init__.py
--rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)     4204 2023-07-16 22:03:44.000000 wf-cv-utils-3.6.0/cv_utils/drawing/matplotlib.py
--rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)    11056 2023-07-16 22:03:39.000000 wf-cv-utils-3.6.0/cv_utils/drawing/opencv.py
--rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)     4966 2023-07-16 22:03:21.000000 wf-cv-utils-3.6.0/cv_utils/eager_video_capture.py
--rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)     7160 2023-07-16 22:03:19.000000 wf-cv-utils-3.6.0/cv_utils/video.py
--rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)       38 2023-07-16 23:35:05.995186 wf-cv-utils-3.6.0/setup.cfg
--rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)     1011 2023-07-16 17:56:52.000000 wf-cv-utils-3.6.0/setup.py
-drwxrwxr-x   0 tcquinn   (1001) tcquinn   (1001)        0 2023-07-16 23:35:05.995186 wf-cv-utils-3.6.0/wf_cv_utils.egg-info/
--rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)     1999 2023-07-16 23:35:05.000000 wf-cv-utils-3.6.0/wf_cv_utils.egg-info/PKG-INFO
--rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)      450 2023-07-16 23:35:05.000000 wf-cv-utils-3.6.0/wf_cv_utils.egg-info/SOURCES.txt
--rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)        1 2023-07-16 23:35:05.000000 wf-cv-utils-3.6.0/wf_cv_utils.egg-info/dependency_links.txt
--rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)       67 2023-07-16 23:35:05.000000 wf-cv-utils-3.6.0/wf_cv_utils.egg-info/requires.txt
--rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)        9 2023-07-16 23:35:05.000000 wf-cv-utils-3.6.0/wf_cv_utils.egg-info/top_level.txt
+drwxrwxr-x   0 tcquinn   (1001) tcquinn   (1001)        0 2023-07-23 14:48:13.084684 wf-cv-utils-3.6.1/
+-rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)     1088 2022-12-08 20:56:25.000000 wf-cv-utils-3.6.1/LICENSE
+-rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)       34 2022-12-08 20:56:25.000000 wf-cv-utils-3.6.1/MANIFEST.in
+-rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)     1999 2023-07-23 14:48:13.084684 wf-cv-utils-3.6.1/PKG-INFO
+-rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)     1495 2022-12-08 20:56:25.000000 wf-cv-utils-3.6.1/README.md
+-rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)        5 2023-07-23 14:46:13.000000 wf-cv-utils-3.6.1/VERSION
+drwxrwxr-x   0 tcquinn   (1001) tcquinn   (1001)        0 2023-07-23 14:48:13.080685 wf-cv-utils-3.6.1/cv_utils/
+-rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)      225 2023-07-16 23:36:12.000000 wf-cv-utils-3.6.1/cv_utils/__init__.py
+-rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)    34095 2023-07-16 22:03:30.000000 wf-cv-utils-3.6.1/cv_utils/aruco.py
+-rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)    15951 2023-07-23 14:21:19.000000 wf-cv-utils-3.6.1/cv_utils/colmap.py
+-rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)      380 2023-07-16 23:36:12.000000 wf-cv-utils-3.6.1/cv_utils/color.py
+-rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)    24991 2023-07-16 23:36:12.000000 wf-cv-utils-3.6.1/cv_utils/core.py
+drwxrwxr-x   0 tcquinn   (1001) tcquinn   (1001)        0 2023-07-23 14:48:13.084684 wf-cv-utils-3.6.1/cv_utils/drawing/
+-rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)        0 2022-12-08 20:56:25.000000 wf-cv-utils-3.6.1/cv_utils/drawing/__init__.py
+-rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)     4204 2023-07-16 23:36:12.000000 wf-cv-utils-3.6.1/cv_utils/drawing/matplotlib.py
+-rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)    11056 2023-07-16 23:36:12.000000 wf-cv-utils-3.6.1/cv_utils/drawing/opencv.py
+-rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)     4966 2023-07-16 22:03:21.000000 wf-cv-utils-3.6.1/cv_utils/eager_video_capture.py
+-rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)     7160 2023-07-16 22:03:19.000000 wf-cv-utils-3.6.1/cv_utils/video.py
+-rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)       38 2023-07-23 14:48:13.084684 wf-cv-utils-3.6.1/setup.cfg
+-rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)     1011 2023-07-16 17:56:52.000000 wf-cv-utils-3.6.1/setup.py
+drwxrwxr-x   0 tcquinn   (1001) tcquinn   (1001)        0 2023-07-23 14:48:13.084684 wf-cv-utils-3.6.1/wf_cv_utils.egg-info/
+-rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)     1999 2023-07-23 14:48:13.000000 wf-cv-utils-3.6.1/wf_cv_utils.egg-info/PKG-INFO
+-rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)      450 2023-07-23 14:48:13.000000 wf-cv-utils-3.6.1/wf_cv_utils.egg-info/SOURCES.txt
+-rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)        1 2023-07-23 14:48:13.000000 wf-cv-utils-3.6.1/wf_cv_utils.egg-info/dependency_links.txt
+-rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)       67 2023-07-23 14:48:13.000000 wf-cv-utils-3.6.1/wf_cv_utils.egg-info/requires.txt
+-rw-rw-r--   0 tcquinn   (1001) tcquinn   (1001)        9 2023-07-23 14:48:13.000000 wf-cv-utils-3.6.1/wf_cv_utils.egg-info/top_level.txt
```

### Comparing `wf-cv-utils-3.6.0/LICENSE` & `wf-cv-utils-3.6.1/LICENSE`

 * *Files identical despite different names*

### Comparing `wf-cv-utils-3.6.0/PKG-INFO` & `wf-cv-utils-3.6.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: wf-cv-utils
-Version: 3.6.0
+Version: 3.6.1
 Summary: Miscellaneous utilities for working with camera data
 Home-page: https://github.com/WildflowerSchools/wf-cv-utils
 Author: Theodore Quinn
 Author-email: ted.quinn@wildflowerschools.org
 License: UNKNOWN
 Keywords: cv
 Platform: UNKNOWN
```

### Comparing `wf-cv-utils-3.6.0/README.md` & `wf-cv-utils-3.6.1/README.md`

 * *Files identical despite different names*

### Comparing `wf-cv-utils-3.6.0/cv_utils/aruco.py` & `wf-cv-utils-3.6.1/cv_utils/aruco.py`

 * *Files identical despite different names*

### Comparing `wf-cv-utils-3.6.0/cv_utils/colmap.py` & `wf-cv-utils-3.6.1/cv_utils/colmap.py`

 * *Files 1% similar despite different names*

```diff
@@ -235,15 +235,14 @@
         'colmap_camera_model': 'string',
         'image_width': 'int',
         'image_height': 'int',
         'colmap_parameters': 'object',
         'camera_matrix': 'object',
         'distortion_coefficients': 'object'
     })
-    df.set_index('colmap_camera_id', inplace=True)
     df = (
         df
         .reindex(columns=[
             'colmap_camera_id',
             'colmap_camera_model',
             'image_width',
             'image_height',
```

### Comparing `wf-cv-utils-3.6.0/cv_utils/core.py` & `wf-cv-utils-3.6.1/cv_utils/core.py`

 * *Files identical despite different names*

### Comparing `wf-cv-utils-3.6.0/cv_utils/drawing/matplotlib.py` & `wf-cv-utils-3.6.1/cv_utils/drawing/matplotlib.py`

 * *Files identical despite different names*

### Comparing `wf-cv-utils-3.6.0/cv_utils/drawing/opencv.py` & `wf-cv-utils-3.6.1/cv_utils/drawing/opencv.py`

 * *Files identical despite different names*

### Comparing `wf-cv-utils-3.6.0/cv_utils/eager_video_capture.py` & `wf-cv-utils-3.6.1/cv_utils/eager_video_capture.py`

 * *Files identical despite different names*

### Comparing `wf-cv-utils-3.6.0/cv_utils/video.py` & `wf-cv-utils-3.6.1/cv_utils/video.py`

 * *Files identical despite different names*

### Comparing `wf-cv-utils-3.6.0/setup.py` & `wf-cv-utils-3.6.1/setup.py`

 * *Files identical despite different names*

### Comparing `wf-cv-utils-3.6.0/wf_cv_utils.egg-info/PKG-INFO` & `wf-cv-utils-3.6.1/wf_cv_utils.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: wf-cv-utils
-Version: 3.6.0
+Version: 3.6.1
 Summary: Miscellaneous utilities for working with camera data
 Home-page: https://github.com/WildflowerSchools/wf-cv-utils
 Author: Theodore Quinn
 Author-email: ted.quinn@wildflowerschools.org
 License: UNKNOWN
 Keywords: cv
 Platform: UNKNOWN
```

