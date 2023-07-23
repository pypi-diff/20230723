# Comparing `tmp/pymolviz-1.0.tar.gz` & `tmp/pymolviz-1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pymolviz-1.0.tar", last modified: Thu Jul 20 14:36:28 2023, max compression
+gzip compressed data, was "pymolviz-1.1.tar", last modified: Sun Jul 23 17:04:21 2023, max compression
```

## Comparing `pymolviz-1.0.tar` & `pymolviz-1.1.tar`

### file list

```diff
@@ -1,17 +1,44 @@
-drwxr-xr-x   0 highgarden  (1000) highgarden  (1000)        0 2023-07-20 14:36:28.619524 pymolviz-1.0/
--rw-r--r--   0 highgarden  (1000) highgarden  (1000)      228 2023-07-20 14:36:28.619524 pymolviz-1.0/PKG-INFO
-drwxr-xr-x   0 highgarden  (1000) highgarden  (1000)        0 2023-07-20 14:36:28.619524 pymolviz-1.0/pymolviz/
--rw-r--r--   0 highgarden  (1000) highgarden  (1000)     7883 2023-07-20 14:22:32.000000 pymolviz-1.0/pymolviz/ColorMap.py
--rw-r--r--   0 highgarden  (1000) highgarden  (1000)     1597 2023-07-20 14:22:32.000000 pymolviz-1.0/pymolviz/Displayable.py
--rw-r--r--   0 highgarden  (1000) highgarden  (1000)     1865 2023-07-20 14:22:32.000000 pymolviz-1.0/pymolviz/Group.py
--rw-r--r--   0 highgarden  (1000) highgarden  (1000)     2014 2023-07-20 14:22:32.000000 pymolviz-1.0/pymolviz/Script.py
--rw-r--r--   0 highgarden  (1000) highgarden  (1000)      301 2023-07-20 14:22:32.000000 pymolviz-1.0/pymolviz/__init__.py
-drwxr-xr-x   0 highgarden  (1000) highgarden  (1000)        0 2023-07-20 14:36:28.619524 pymolviz-1.0/pymolviz.egg-info/
--rw-r--r--   0 highgarden  (1000) highgarden  (1000)      228 2023-07-20 14:36:28.000000 pymolviz-1.0/pymolviz.egg-info/PKG-INFO
--rw-r--r--   0 highgarden  (1000) highgarden  (1000)      301 2023-07-20 14:36:28.000000 pymolviz-1.0/pymolviz.egg-info/SOURCES.txt
--rw-r--r--   0 highgarden  (1000) highgarden  (1000)        1 2023-07-20 14:36:28.000000 pymolviz-1.0/pymolviz.egg-info/dependency_links.txt
--rw-r--r--   0 highgarden  (1000) highgarden  (1000)        1 2023-07-20 14:30:13.000000 pymolviz-1.0/pymolviz.egg-info/not-zip-safe
--rw-r--r--   0 highgarden  (1000) highgarden  (1000)       23 2023-07-20 14:36:28.000000 pymolviz-1.0/pymolviz.egg-info/requires.txt
--rw-r--r--   0 highgarden  (1000) highgarden  (1000)        9 2023-07-20 14:36:28.000000 pymolviz-1.0/pymolviz.egg-info/top_level.txt
--rw-r--r--   0 highgarden  (1000) highgarden  (1000)       38 2023-07-20 14:36:28.619524 pymolviz-1.0/setup.cfg
--rw-r--r--   0 highgarden  (1000) highgarden  (1000)      491 2023-07-20 14:36:19.000000 pymolviz-1.0/setup.py
+drwxrwxr-x   0 finn      (1000) finn      (1000)        0 2023-07-23 17:04:21.954474 pymolviz-1.1/
+-rw-rw-r--   0 finn      (1000) finn      (1000)      228 2023-07-23 17:04:21.954474 pymolviz-1.1/PKG-INFO
+drwxrwxr-x   0 finn      (1000) finn      (1000)        0 2023-07-23 17:04:21.950475 pymolviz-1.1/pymolviz/
+-rw-rw-r--   0 finn      (1000) finn      (1000)     7883 2023-07-23 16:06:34.000000 pymolviz-1.1/pymolviz/ColorMap.py
+-rw-rw-r--   0 finn      (1000) finn      (1000)     1597 2023-07-23 16:06:34.000000 pymolviz-1.1/pymolviz/Displayable.py
+-rw-rw-r--   0 finn      (1000) finn      (1000)     1865 2023-07-23 16:06:34.000000 pymolviz-1.1/pymolviz/Group.py
+drwxrwxr-x   0 finn      (1000) finn      (1000)        0 2023-07-23 17:04:21.950475 pymolviz-1.1/pymolviz/PyMOLobjects/
+-rw-rw-r--   0 finn      (1000) finn      (1000)      980 2023-07-23 16:06:34.000000 pymolviz-1.1/pymolviz/PyMOLobjects/Labels.py
+-rw-rw-r--   0 finn      (1000) finn      (1000)       26 2023-07-23 16:06:34.000000 pymolviz-1.1/pymolviz/PyMOLobjects/__init__.py
+-rw-rw-r--   0 finn      (1000) finn      (1000)     2014 2023-07-23 16:06:34.000000 pymolviz-1.1/pymolviz/Script.py
+-rw-rw-r--   0 finn      (1000) finn      (1000)      302 2023-07-23 16:57:38.000000 pymolviz-1.1/pymolviz/__init__.py
+drwxrwxr-x   0 finn      (1000) finn      (1000)        0 2023-07-23 17:04:21.950475 pymolviz-1.1/pymolviz/meshes/
+-rw-rw-r--   0 finn      (1000) finn      (1000)     2919 2023-07-23 16:06:34.000000 pymolviz-1.1/pymolviz/meshes/Arrows.py
+-rw-rw-r--   0 finn      (1000) finn      (1000)     2719 2023-07-23 16:06:34.000000 pymolviz-1.1/pymolviz/meshes/CGOCollection.py
+-rw-rw-r--   0 finn      (1000) finn      (1000)     2777 2023-07-23 16:06:34.000000 pymolviz-1.1/pymolviz/meshes/Lines.py
+-rw-rw-r--   0 finn      (1000) finn      (1000)     3166 2023-07-23 16:06:34.000000 pymolviz-1.1/pymolviz/meshes/Mesh.py
+-rw-rw-r--   0 finn      (1000) finn      (1000)     1076 2023-07-23 16:06:34.000000 pymolviz-1.1/pymolviz/meshes/Plane.py
+-rw-rw-r--   0 finn      (1000) finn      (1000)     3762 2023-07-23 16:06:34.000000 pymolviz-1.1/pymolviz/meshes/Points.py
+-rw-rw-r--   0 finn      (1000) finn      (1000)     1172 2023-07-23 16:06:34.000000 pymolviz-1.1/pymolviz/meshes/Sphere.py
+-rw-rw-r--   0 finn      (1000) finn      (1000)      195 2023-07-23 16:06:34.000000 pymolviz-1.1/pymolviz/meshes/__init__.py
+drwxrwxr-x   0 finn      (1000) finn      (1000)        0 2023-07-23 17:04:21.950475 pymolviz-1.1/pymolviz/util/
+-rw-rw-r--   0 finn      (1000) finn      (1000)       81 2023-07-23 16:06:34.000000 pymolviz-1.1/pymolviz/util/__init__.py
+-rw-rw-r--   0 finn      (1000) finn      (1000)    15459 2023-07-23 16:06:34.000000 pymolviz-1.1/pymolviz/util/colors.py
+-rw-rw-r--   0 finn      (1000) finn      (1000)     4799 2023-07-23 16:06:34.000000 pymolviz-1.1/pymolviz/util/geometries.py
+-rw-rw-r--   0 finn      (1000) finn      (1000)     1727 2023-07-23 16:06:34.000000 pymolviz-1.1/pymolviz/util/io.py
+-rw-rw-r--   0 finn      (1000) finn      (1000)      711 2023-07-23 16:06:34.000000 pymolviz-1.1/pymolviz/util/math.py
+drwxrwxr-x   0 finn      (1000) finn      (1000)        0 2023-07-23 17:04:21.954474 pymolviz-1.1/pymolviz/volumetric/
+-rw-rw-r--   0 finn      (1000) finn      (1000)     2266 2023-07-23 16:06:34.000000 pymolviz-1.1/pymolviz/volumetric/ColorRamp.py
+-rw-rw-r--   0 finn      (1000) finn      (1000)     5437 2023-07-23 16:06:34.000000 pymolviz-1.1/pymolviz/volumetric/GridData.py
+-rw-rw-r--   0 finn      (1000) finn      (1000)     5679 2023-07-23 16:06:34.000000 pymolviz-1.1/pymolviz/volumetric/IrregularData.py
+-rw-rw-r--   0 finn      (1000) finn      (1000)     1104 2023-07-23 16:06:34.000000 pymolviz-1.1/pymolviz/volumetric/IsoMesh.py
+-rw-rw-r--   0 finn      (1000) finn      (1000)     3355 2023-07-23 16:06:34.000000 pymolviz-1.1/pymolviz/volumetric/IsoSurface.py
+-rw-rw-r--   0 finn      (1000) finn      (1000)     2529 2023-07-23 16:06:34.000000 pymolviz-1.1/pymolviz/volumetric/IsoVolume.py
+-rw-rw-r--   0 finn      (1000) finn      (1000)     4421 2023-07-23 16:06:34.000000 pymolviz-1.1/pymolviz/volumetric/Volume.py
+-rw-rw-r--   0 finn      (1000) finn      (1000)      228 2023-07-23 16:06:34.000000 pymolviz-1.1/pymolviz/volumetric/__init__.py
+drwxrwxr-x   0 finn      (1000) finn      (1000)        0 2023-07-23 17:04:21.950475 pymolviz-1.1/pymolviz.egg-info/
+-rw-rw-r--   0 finn      (1000) finn      (1000)      228 2023-07-23 17:04:21.000000 pymolviz-1.1/pymolviz.egg-info/PKG-INFO
+-rw-rw-r--   0 finn      (1000) finn      (1000)      962 2023-07-23 17:04:21.000000 pymolviz-1.1/pymolviz.egg-info/SOURCES.txt
+-rw-rw-r--   0 finn      (1000) finn      (1000)        1 2023-07-23 17:04:21.000000 pymolviz-1.1/pymolviz.egg-info/dependency_links.txt
+-rw-rw-r--   0 finn      (1000) finn      (1000)        1 2023-07-23 16:08:50.000000 pymolviz-1.1/pymolviz.egg-info/not-zip-safe
+-rw-rw-r--   0 finn      (1000) finn      (1000)       23 2023-07-23 17:04:21.000000 pymolviz-1.1/pymolviz.egg-info/requires.txt
+-rw-rw-r--   0 finn      (1000) finn      (1000)        9 2023-07-23 17:04:21.000000 pymolviz-1.1/pymolviz.egg-info/top_level.txt
+-rw-rw-r--   0 finn      (1000) finn      (1000)       38 2023-07-23 17:04:21.954474 pymolviz-1.1/setup.cfg
+-rw-rw-r--   0 finn      (1000) finn      (1000)      575 2023-07-23 17:04:18.000000 pymolviz-1.1/setup.py
```

### Comparing `pymolviz-1.0/pymolviz/ColorMap.py` & `pymolviz-1.1/pymolviz/ColorMap.py`

 * *Files identical despite different names*

### Comparing `pymolviz-1.0/pymolviz/Displayable.py` & `pymolviz-1.1/pymolviz/Displayable.py`

 * *Files identical despite different names*

### Comparing `pymolviz-1.0/pymolviz/Group.py` & `pymolviz-1.1/pymolviz/Group.py`

 * *Files identical despite different names*

### Comparing `pymolviz-1.0/pymolviz/Script.py` & `pymolviz-1.1/pymolviz/Script.py`

 * *Files identical despite different names*

