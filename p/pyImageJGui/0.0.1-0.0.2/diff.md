# Comparing `tmp/pyImageJGui-0.0.1.tar.gz` & `tmp/pyImageJGui-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pyImageJGui-0.0.1.tar", last modified: Sun Jul 23 17:00:41 2023, max compression
+gzip compressed data, was "pyImageJGui-0.0.2.tar", last modified: Sun Jul 23 17:21:33 2023, max compression
```

## Comparing `pyImageJGui-0.0.1.tar` & `pyImageJGui-0.0.2.tar`

### file list

```diff
@@ -1,50 +1,50 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:00:41.329709 pyImageJGui-0.0.1/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:00:41.325709 pyImageJGui-0.0.1/.github/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:00:41.325709 pyImageJGui-0.0.1/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)     1149 2023-07-23 17:00:26.000000 pyImageJGui-0.0.1/.github/workflows/python-publish.yml
--rw-r--r--   0 runner    (1001) docker     (123)       54 2023-07-23 17:00:26.000000 pyImageJGui-0.0.1/ABOUT.rst
--rw-r--r--   0 runner    (1001) docker     (123)       28 2023-07-23 17:00:41.000000 pyImageJGui-0.0.1/AUTHORS
--rw-r--r--   0 runner    (1001) docker     (123)       51 2023-07-23 17:00:41.000000 pyImageJGui-0.0.1/ChangeLog
--rw-r--r--   0 runner    (1001) docker     (123)     1087 2023-07-23 17:00:26.000000 pyImageJGui-0.0.1/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      635 2023-07-23 17:00:41.329709 pyImageJGui-0.0.1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)       10 2023-07-23 17:00:26.000000 pyImageJGui-0.0.1/README.md
--rw-r--r--   0 runner    (1001) docker     (123)      346 2023-07-23 17:00:26.000000 pyImageJGui-0.0.1/init.bat
--rw-r--r--   0 runner    (1001) docker     (123)      297 2023-07-23 17:00:26.000000 pyImageJGui-0.0.1/init.sh
--rw-r--r--   0 runner    (1001) docker     (123)      742 2023-07-23 17:00:26.000000 pyImageJGui-0.0.1/main.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:00:41.325709 pyImageJGui-0.0.1/pyImageJGui.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)      635 2023-07-23 17:00:41.000000 pyImageJGui-0.0.1/pyImageJGui.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      932 2023-07-23 17:00:41.000000 pyImageJGui-0.0.1/pyImageJGui.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 17:00:41.000000 pyImageJGui-0.0.1/pyImageJGui.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 17:00:41.000000 pyImageJGui-0.0.1/pyImageJGui.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)       47 2023-07-23 17:00:41.000000 pyImageJGui-0.0.1/pyImageJGui.egg-info/pbr.json
--rw-r--r--   0 runner    (1001) docker     (123)      120 2023-07-23 17:00:41.000000 pyImageJGui-0.0.1/pyImageJGui.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-23 17:00:41.000000 pyImageJGui-0.0.1/pyImageJGui.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:00:41.329709 pyImageJGui-0.0.1/pyimagej/
--rw-r--r--   0 runner    (1001) docker     (123)      127 2023-07-23 17:00:26.000000 pyImageJGui-0.0.1/pyimagej/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:00:41.329709 pyImageJGui-0.0.1/pyimagej/icon/
--rw-r--r--   0 runner    (1001) docker     (123)      544 2023-07-23 17:00:26.000000 pyImageJGui-0.0.1/pyimagej/icon/angle.svg
--rw-r--r--   0 runner    (1001) docker     (123)      873 2023-07-23 17:00:26.000000 pyImageJGui-0.0.1/pyimagej/icon/circle.svg
--rw-r--r--   0 runner    (1001) docker     (123)      870 2023-07-23 17:00:26.000000 pyImageJGui-0.0.1/pyimagej/icon/clear.svg
--rw-r--r--   0 runner    (1001) docker     (123)      757 2023-07-23 17:00:26.000000 pyImageJGui-0.0.1/pyimagej/icon/elliptical.svg
--rw-r--r--   0 runner    (1001) docker     (123)     1270 2023-07-23 17:00:26.000000 pyImageJGui-0.0.1/pyimagej/icon/file.svg
--rw-r--r--   0 runner    (1001) docker     (123)      867 2023-07-23 17:00:26.000000 pyImageJGui-0.0.1/pyimagej/icon/freehand.svg
--rw-r--r--   0 runner    (1001) docker     (123)     4005 2023-07-23 17:00:26.000000 pyImageJGui-0.0.1/pyimagej/icon/hand.svg
--rw-r--r--   0 runner    (1001) docker     (123)      353 2023-07-23 17:00:26.000000 pyImageJGui-0.0.1/pyimagej/icon/line.svg
--rw-r--r--   0 runner    (1001) docker     (123)      582 2023-07-23 17:00:26.000000 pyImageJGui-0.0.1/pyimagej/icon/magnifier.svg
--rw-r--r--   0 runner    (1001) docker     (123)      565 2023-07-23 17:00:26.000000 pyImageJGui-0.0.1/pyimagej/icon/polygon.svg
--rw-r--r--   0 runner    (1001) docker     (123)      370 2023-07-23 17:00:26.000000 pyImageJGui-0.0.1/pyimagej/icon/rectangle.svg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:00:41.329709 pyImageJGui-0.0.1/pyimagej/style/
--rwxr-xr-x   0 runner    (1001) docker     (123)     4254 2023-07-23 17:00:26.000000 pyImageJGui-0.0.1/pyimagej/style/main.qss
--rwxr-xr-x   0 runner    (1001) docker     (123)      362 2023-07-23 17:00:26.000000 pyImageJGui-0.0.1/pyimagej/style/qssloader.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:00:41.329709 pyImageJGui-0.0.1/pyimagej/ui/
--rw-r--r--   0 runner    (1001) docker     (123)     6538 2023-07-23 17:00:27.000000 pyImageJGui-0.0.1/pyimagej/ui/AngleRoi.py
--rw-r--r--   0 runner    (1001) docker     (123)     6388 2023-07-23 17:00:27.000000 pyImageJGui-0.0.1/pyimagej/ui/CircleRoi.py
--rw-r--r--   0 runner    (1001) docker     (123)     7092 2023-07-23 17:00:27.000000 pyImageJGui-0.0.1/pyimagej/ui/EllipseRoi.py
--rw-r--r--   0 runner    (1001) docker     (123)     4365 2023-07-23 17:00:27.000000 pyImageJGui-0.0.1/pyimagej/ui/LineRoi.py
--rw-r--r--   0 runner    (1001) docker     (123)     6110 2023-07-23 17:00:27.000000 pyImageJGui-0.0.1/pyimagej/ui/RectangleRoi.py
--rw-r--r--   0 runner    (1001) docker     (123)      303 2023-07-23 17:00:27.000000 pyImageJGui-0.0.1/pyimagej/ui/constant.py
--rw-r--r--   0 runner    (1001) docker     (123)    13530 2023-07-23 17:00:27.000000 pyImageJGui-0.0.1/pyimagej/ui/imageView.py
--rw-r--r--   0 runner    (1001) docker     (123)     6050 2023-07-23 17:00:27.000000 pyImageJGui-0.0.1/pyimagej/ui/main_ui.py
--rw-r--r--   0 runner    (1001) docker     (123)      119 2023-07-23 17:00:27.000000 pyImageJGui-0.0.1/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)      560 2023-07-23 17:00:41.333709 pyImageJGui-0.0.1/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      193 2023-07-23 17:00:27.000000 pyImageJGui-0.0.1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:21:33.487533 pyImageJGui-0.0.2/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:21:33.483533 pyImageJGui-0.0.2/.github/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:21:33.483533 pyImageJGui-0.0.2/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)     1149 2023-07-23 17:21:20.000000 pyImageJGui-0.0.2/.github/workflows/python-publish.yml
+-rw-r--r--   0 runner    (1001) docker     (123)       54 2023-07-23 17:21:20.000000 pyImageJGui-0.0.2/ABOUT.rst
+-rw-r--r--   0 runner    (1001) docker     (123)       28 2023-07-23 17:21:33.000000 pyImageJGui-0.0.2/AUTHORS
+-rw-r--r--   0 runner    (1001) docker     (123)       51 2023-07-23 17:21:33.000000 pyImageJGui-0.0.2/ChangeLog
+-rw-r--r--   0 runner    (1001) docker     (123)     1087 2023-07-23 17:21:20.000000 pyImageJGui-0.0.2/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      635 2023-07-23 17:21:33.487533 pyImageJGui-0.0.2/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)       10 2023-07-23 17:21:20.000000 pyImageJGui-0.0.2/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      346 2023-07-23 17:21:20.000000 pyImageJGui-0.0.2/init.bat
+-rw-r--r--   0 runner    (1001) docker     (123)      297 2023-07-23 17:21:20.000000 pyImageJGui-0.0.2/init.sh
+-rw-r--r--   0 runner    (1001) docker     (123)      663 2023-07-23 17:21:20.000000 pyImageJGui-0.0.2/main.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:21:33.483533 pyImageJGui-0.0.2/pyImageJGui.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)      635 2023-07-23 17:21:33.000000 pyImageJGui-0.0.2/pyImageJGui.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      932 2023-07-23 17:21:33.000000 pyImageJGui-0.0.2/pyImageJGui.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 17:21:33.000000 pyImageJGui-0.0.2/pyImageJGui.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 17:21:33.000000 pyImageJGui-0.0.2/pyImageJGui.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)       47 2023-07-23 17:21:33.000000 pyImageJGui-0.0.2/pyImageJGui.egg-info/pbr.json
+-rw-r--r--   0 runner    (1001) docker     (123)      120 2023-07-23 17:21:33.000000 pyImageJGui-0.0.2/pyImageJGui.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-23 17:21:33.000000 pyImageJGui-0.0.2/pyImageJGui.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:21:33.483533 pyImageJGui-0.0.2/pyimagej/
+-rw-r--r--   0 runner    (1001) docker     (123)      127 2023-07-23 17:21:20.000000 pyImageJGui-0.0.2/pyimagej/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:21:33.487533 pyImageJGui-0.0.2/pyimagej/icon/
+-rw-r--r--   0 runner    (1001) docker     (123)      544 2023-07-23 17:21:20.000000 pyImageJGui-0.0.2/pyimagej/icon/angle.svg
+-rw-r--r--   0 runner    (1001) docker     (123)      873 2023-07-23 17:21:20.000000 pyImageJGui-0.0.2/pyimagej/icon/circle.svg
+-rw-r--r--   0 runner    (1001) docker     (123)      870 2023-07-23 17:21:20.000000 pyImageJGui-0.0.2/pyimagej/icon/clear.svg
+-rw-r--r--   0 runner    (1001) docker     (123)      757 2023-07-23 17:21:20.000000 pyImageJGui-0.0.2/pyimagej/icon/elliptical.svg
+-rw-r--r--   0 runner    (1001) docker     (123)     1270 2023-07-23 17:21:20.000000 pyImageJGui-0.0.2/pyimagej/icon/file.svg
+-rw-r--r--   0 runner    (1001) docker     (123)      867 2023-07-23 17:21:20.000000 pyImageJGui-0.0.2/pyimagej/icon/freehand.svg
+-rw-r--r--   0 runner    (1001) docker     (123)     4005 2023-07-23 17:21:20.000000 pyImageJGui-0.0.2/pyimagej/icon/hand.svg
+-rw-r--r--   0 runner    (1001) docker     (123)      353 2023-07-23 17:21:20.000000 pyImageJGui-0.0.2/pyimagej/icon/line.svg
+-rw-r--r--   0 runner    (1001) docker     (123)      582 2023-07-23 17:21:20.000000 pyImageJGui-0.0.2/pyimagej/icon/magnifier.svg
+-rw-r--r--   0 runner    (1001) docker     (123)      565 2023-07-23 17:21:20.000000 pyImageJGui-0.0.2/pyimagej/icon/polygon.svg
+-rw-r--r--   0 runner    (1001) docker     (123)      370 2023-07-23 17:21:20.000000 pyImageJGui-0.0.2/pyimagej/icon/rectangle.svg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:21:33.487533 pyImageJGui-0.0.2/pyimagej/style/
+-rwxr-xr-x   0 runner    (1001) docker     (123)     4254 2023-07-23 17:21:20.000000 pyImageJGui-0.0.2/pyimagej/style/main.qss
+-rwxr-xr-x   0 runner    (1001) docker     (123)      478 2023-07-23 17:21:20.000000 pyImageJGui-0.0.2/pyimagej/style/qssloader.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:21:33.487533 pyImageJGui-0.0.2/pyimagej/ui/
+-rw-r--r--   0 runner    (1001) docker     (123)     6538 2023-07-23 17:21:20.000000 pyImageJGui-0.0.2/pyimagej/ui/AngleRoi.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6388 2023-07-23 17:21:20.000000 pyImageJGui-0.0.2/pyimagej/ui/CircleRoi.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7092 2023-07-23 17:21:20.000000 pyImageJGui-0.0.2/pyimagej/ui/EllipseRoi.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4365 2023-07-23 17:21:20.000000 pyImageJGui-0.0.2/pyimagej/ui/LineRoi.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6110 2023-07-23 17:21:20.000000 pyImageJGui-0.0.2/pyimagej/ui/RectangleRoi.py
+-rw-r--r--   0 runner    (1001) docker     (123)      303 2023-07-23 17:21:20.000000 pyImageJGui-0.0.2/pyimagej/ui/constant.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13530 2023-07-23 17:21:20.000000 pyImageJGui-0.0.2/pyimagej/ui/imageView.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6206 2023-07-23 17:21:20.000000 pyImageJGui-0.0.2/pyimagej/ui/main_ui.py
+-rw-r--r--   0 runner    (1001) docker     (123)      119 2023-07-23 17:21:20.000000 pyImageJGui-0.0.2/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      560 2023-07-23 17:21:33.487533 pyImageJGui-0.0.2/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      193 2023-07-23 17:21:20.000000 pyImageJGui-0.0.2/setup.py
```

### Comparing `pyImageJGui-0.0.1/.github/workflows/python-publish.yml` & `pyImageJGui-0.0.2/.github/workflows/python-publish.yml`

 * *Files identical despite different names*

### Comparing `pyImageJGui-0.0.1/LICENSE` & `pyImageJGui-0.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `pyImageJGui-0.0.1/PKG-INFO` & `pyImageJGui-0.0.2/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyImageJGui
-Version: 0.0.1
+Version: 0.0.2
 Summary: Python for ImageJ GUI
 Home-page: https://github.com/aghb123/pyimagej
 Author: sdb
 License: MIT
 Classifier: Development Status :: 3 - Alpha
 Classifier: Environment :: Console
 Classifier: Intended Audience :: Developers
```

### Comparing `pyImageJGui-0.0.1/main.py` & `pyImageJGui-0.0.2/main.py`

 * *Files 24% similar despite different names*

```diff
@@ -7,20 +7,19 @@
 """
 import multiprocessing
 import sys
 
 multiprocessing.freeze_support()
 from pyimagej.ui.main_ui import *
 from qt_material import apply_stylesheet
-from pyimagej.style.qssloader import QSSLoader
+from pyimagej.style.qssloader import style
 
 if __name__ == "__main__":
     app = QApplication([])
     window = QMainWindow()
     window.setMinimumSize(QSize(600, 400))
     window.setCentralWidget(ImageWidget())
     apply_stylesheet(app, theme='light_blue.xml', invert_secondary=True)
     window.setWindowTitle("PyImageJ")
-    style_sheet = QSSLoader.read_qss_file("pyimagej/style/main.qss")
-    window.setStyleSheet(style_sheet)
+    window.setStyleSheet(style)
     window.show()
     sys.exit(app.exec())
```

### Comparing `pyImageJGui-0.0.1/pyImageJGui.egg-info/PKG-INFO` & `pyImageJGui-0.0.2/pyImageJGui.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pyImageJGui
-Version: 0.0.1
+Version: 0.0.2
 Summary: Python for ImageJ GUI
 Home-page: https://github.com/aghb123/pyimagej
 Author: sdb
 License: MIT
 Classifier: Development Status :: 3 - Alpha
 Classifier: Environment :: Console
 Classifier: Intended Audience :: Developers
```

### Comparing `pyImageJGui-0.0.1/pyImageJGui.egg-info/SOURCES.txt` & `pyImageJGui-0.0.2/pyImageJGui.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `pyImageJGui-0.0.1/pyimagej/icon/angle.svg` & `pyImageJGui-0.0.2/pyimagej/icon/angle.svg`

 * *Files identical despite different names*

### Comparing `pyImageJGui-0.0.1/pyimagej/icon/circle.svg` & `pyImageJGui-0.0.2/pyimagej/icon/circle.svg`

 * *Files identical despite different names*

### Comparing `pyImageJGui-0.0.1/pyimagej/icon/clear.svg` & `pyImageJGui-0.0.2/pyimagej/icon/clear.svg`

 * *Files identical despite different names*

### Comparing `pyImageJGui-0.0.1/pyimagej/icon/elliptical.svg` & `pyImageJGui-0.0.2/pyimagej/icon/elliptical.svg`

 * *Files identical despite different names*

### Comparing `pyImageJGui-0.0.1/pyimagej/icon/file.svg` & `pyImageJGui-0.0.2/pyimagej/icon/file.svg`

 * *Files identical despite different names*

### Comparing `pyImageJGui-0.0.1/pyimagej/icon/freehand.svg` & `pyImageJGui-0.0.2/pyimagej/icon/freehand.svg`

 * *Files identical despite different names*

### Comparing `pyImageJGui-0.0.1/pyimagej/icon/hand.svg` & `pyImageJGui-0.0.2/pyimagej/icon/hand.svg`

 * *Files identical despite different names*

### Comparing `pyImageJGui-0.0.1/pyimagej/icon/magnifier.svg` & `pyImageJGui-0.0.2/pyimagej/icon/magnifier.svg`

 * *Files identical despite different names*

### Comparing `pyImageJGui-0.0.1/pyimagej/icon/polygon.svg` & `pyImageJGui-0.0.2/pyimagej/icon/polygon.svg`

 * *Files identical despite different names*

### Comparing `pyImageJGui-0.0.1/pyimagej/style/main.qss` & `pyImageJGui-0.0.2/pyimagej/style/main.qss`

 * *Files identical despite different names*

### Comparing `pyImageJGui-0.0.1/pyimagej/ui/AngleRoi.py` & `pyImageJGui-0.0.2/pyimagej/ui/AngleRoi.py`

 * *Files identical despite different names*

### Comparing `pyImageJGui-0.0.1/pyimagej/ui/CircleRoi.py` & `pyImageJGui-0.0.2/pyimagej/ui/CircleRoi.py`

 * *Files identical despite different names*

### Comparing `pyImageJGui-0.0.1/pyimagej/ui/EllipseRoi.py` & `pyImageJGui-0.0.2/pyimagej/ui/EllipseRoi.py`

 * *Files identical despite different names*

### Comparing `pyImageJGui-0.0.1/pyimagej/ui/LineRoi.py` & `pyImageJGui-0.0.2/pyimagej/ui/LineRoi.py`

 * *Files identical despite different names*

### Comparing `pyImageJGui-0.0.1/pyimagej/ui/RectangleRoi.py` & `pyImageJGui-0.0.2/pyimagej/ui/RectangleRoi.py`

 * *Files identical despite different names*

### Comparing `pyImageJGui-0.0.1/pyimagej/ui/imageView.py` & `pyImageJGui-0.0.2/pyimagej/ui/imageView.py`

 * *Files identical despite different names*

### Comparing `pyImageJGui-0.0.1/pyimagej/ui/main_ui.py` & `pyImageJGui-0.0.2/pyimagej/ui/main_ui.py`

 * *Files 13% similar despite different names*

```diff
@@ -9,45 +9,47 @@
 from PySide6.QtGui import *
 from PySide6.QtWidgets import *
 from PySide6.QtCore import *
 import cv2 as cv
 from pyimagej.ui.imageView import ImageViewer
 from pyimagej.ui.constant import ROI
 
+path = os.path.dirname(os.path.dirname(__file__))
+
 
 class ImageWidget(QWidget):
     def __init__(self, parent=None):
         QWidget.__init__(self, parent)
         self.layout = QVBoxLayout(self)
         self.button_layout = QHBoxLayout()
 
-        self.last_open_dir = '/Users/sdb/image'
+        self.last_open_dir = '/'
         self.roi = ROI.Hand
 
-        self.rectangle_button = Button(QIcon('./pyimagej/icon/rectangle.svg'), '', ROI.Rectangle)
+        self.rectangle_button = Button(QIcon(os.path.join(path, 'icon', 'rectangle.svg')), '', ROI.Rectangle)
         icon_size = self.rectangle_button.style().pixelMetric(QStyle.PixelMetric.PM_ButtonIconSize)
         self.rectangle_button.setIconSize(QSize(icon_size, icon_size))
-        self.angle_button = Button(QIcon('./pyimagej/icon/angle.svg'), '', ROI.Angle)
+        self.angle_button = Button(QIcon(os.path.join(path, 'icon', 'angle.svg')), '', ROI.Angle)
         self.angle_button.setIconSize(QSize(icon_size, icon_size))
-        self.circle_button = Button(QIcon('./pyimagej/icon/circle.svg'), '', ROI.Circle)
+        self.circle_button = Button(QIcon(os.path.join(path, 'icon', 'circle.svg')), '', ROI.Circle)
         self.circle_button.setIconSize(QSize(icon_size, icon_size))
-        self.freehand_button = Button(QIcon('./pyimagej/icon/freehand.svg'), '', ROI.Freehand)
+        self.freehand_button = Button(QIcon(os.path.join(path, 'icon', 'freehand.svg')), '', ROI.Freehand)
         self.freehand_button.setIconSize(QSize(icon_size, icon_size))
-        self.line_button = Button(QIcon('./pyimagej/icon/line.svg'), '', ROI.Line)
+        self.line_button = Button(QIcon(os.path.join(path, 'icon', 'line.svg')), '', ROI.Line)
         self.line_button.setIconSize(QSize(icon_size, icon_size))
-        self.ellipse_button = Button(QIcon('./pyimagej/icon/elliptical.svg'), '', ROI.Ellipse)
+        self.ellipse_button = Button(QIcon(os.path.join(path, 'icon', 'elliptical.svg')), '', ROI.Ellipse)
         self.ellipse_button.setIconSize(QSize(icon_size, icon_size))
-        self.mag_button = Button(QIcon('./pyimagej/icon/magnifier.svg'), '', ROI.Magnifier)
+        self.mag_button = Button(QIcon(os.path.join(path, 'icon', 'magnifier.svg')), '', ROI.Magnifier)
         self.mag_button.setIconSize(QSize(icon_size, icon_size))
-        self.hand_button = Button(QIcon('./pyimagej/icon/hand.svg'), '', ROI.Hand)
+        self.hand_button = Button(QIcon(os.path.join(path, 'icon', 'hand.svg')), '', ROI.Hand)
         self.hand_button.setIconSize(QSize(icon_size, icon_size))
         self.hand_button.setEnabled(False)
-        self.clear_button = QPushButton(QIcon('./pyimagej/icon/clear.svg'), '')
+        self.clear_button = QPushButton(QIcon(os.path.join(path, 'icon', 'clear.svg')), '')
         self.clear_button.setIconSize(QSize(icon_size, icon_size))
-        self.file_button = QPushButton(QIcon('./pyimagej/icon/file.svg'), '')
+        self.file_button = QPushButton(QIcon(os.path.join(path, 'icon', 'file.svg')), '')
         self.file_button.setIconSize(QSize(icon_size, icon_size))
         self.button_layout.addWidget(self.rectangle_button)
         self.button_layout.addWidget(self.circle_button)
         self.button_layout.addWidget(self.ellipse_button)
         self.button_layout.addWidget(self.line_button)
         self.button_layout.addWidget(self.angle_button)
         self.button_layout.addWidget(self.freehand_button)
```

### Comparing `pyImageJGui-0.0.1/setup.cfg` & `pyImageJGui-0.0.2/setup.cfg`

 * *Files identical despite different names*

