# Comparing `tmp/IDsys-0.0.6.tar.gz` & `tmp/IDsys-0.0.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "IDsys-0.0.6.tar", last modified: Sun Jul 23 12:12:32 2023, max compression
+gzip compressed data, was "IDsys-0.0.7.tar", last modified: Sun Jul 23 12:26:13 2023, max compression
```

## Comparing `IDsys-0.0.6.tar` & `IDsys-0.0.7.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 12:12:32.650398 IDsys-0.0.6/
--rw-rw-rw-   0        0        0     1091 2023-07-23 11:51:48.000000 IDsys-0.0.6/LICENSE
--rw-rw-rw-   0        0        0      702 2023-07-23 12:12:32.650398 IDsys-0.0.6/PKG-INFO
--rw-rw-rw-   0        0        0      174 2023-07-23 11:52:27.000000 IDsys-0.0.6/README.md
--rw-rw-rw-   0        0        0      110 2023-07-22 14:43:25.000000 IDsys-0.0.6/pyproject.toml
--rw-rw-rw-   0        0        0      665 2023-07-23 12:12:32.651901 IDsys-0.0.6/setup.cfg
-drwxrwxrwx   0        0        0        0 2023-07-23 12:12:32.625898 IDsys-0.0.6/src/
-drwxrwxrwx   0        0        0        0 2023-07-23 12:12:32.637399 IDsys-0.0.6/src/IDsys/
--rw-rw-rw-   0        0        0      912 2023-07-23 12:11:09.000000 IDsys-0.0.6/src/IDsys/ID.py
--rw-rw-rw-   0        0        0        0 2023-07-22 14:41:03.000000 IDsys-0.0.6/src/IDsys/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 12:12:32.649402 IDsys-0.0.6/src/IDsys.egg-info/
--rw-rw-rw-   0        0        0      702 2023-07-23 12:12:32.000000 IDsys-0.0.6/src/IDsys.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      212 2023-07-23 12:12:32.000000 IDsys-0.0.6/src/IDsys.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 12:12:32.000000 IDsys-0.0.6/src/IDsys.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        6 2023-07-23 12:12:32.000000 IDsys-0.0.6/src/IDsys.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 12:26:13.916705 IDsys-0.0.7/
+-rw-rw-rw-   0        0        0     1091 2023-07-23 11:51:48.000000 IDsys-0.0.7/LICENSE
+-rw-rw-rw-   0        0        0      702 2023-07-23 12:26:13.916705 IDsys-0.0.7/PKG-INFO
+-rw-rw-rw-   0        0        0      174 2023-07-23 11:52:27.000000 IDsys-0.0.7/README.md
+-rw-rw-rw-   0        0        0      110 2023-07-22 14:43:25.000000 IDsys-0.0.7/pyproject.toml
+-rw-rw-rw-   0        0        0      665 2023-07-23 12:26:13.918205 IDsys-0.0.7/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-07-23 12:26:13.878206 IDsys-0.0.7/src/
+drwxrwxrwx   0        0        0        0 2023-07-23 12:26:13.904706 IDsys-0.0.7/src/IDsys/
+-rw-rw-rw-   0        0        0     1022 2023-07-23 12:25:46.000000 IDsys-0.0.7/src/IDsys/ID.py
+-rw-rw-rw-   0        0        0        0 2023-07-22 14:41:03.000000 IDsys-0.0.7/src/IDsys/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 12:26:13.915705 IDsys-0.0.7/src/IDsys.egg-info/
+-rw-rw-rw-   0        0        0      702 2023-07-23 12:26:13.000000 IDsys-0.0.7/src/IDsys.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      212 2023-07-23 12:26:13.000000 IDsys-0.0.7/src/IDsys.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 12:26:13.000000 IDsys-0.0.7/src/IDsys.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        6 2023-07-23 12:26:13.000000 IDsys-0.0.7/src/IDsys.egg-info/top_level.txt
```

### Comparing `IDsys-0.0.6/LICENSE` & `IDsys-0.0.7/LICENSE`

 * *Files identical despite different names*

### Comparing `IDsys-0.0.6/PKG-INFO` & `IDsys-0.0.7/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: IDsys
-Version: 0.0.6
+Version: 0.0.7
 Summary: Creating systeme of identification
 Home-page: https://github.com/Creariax5/IDlib
 Author: Florian Demartini
 Author-email: florian.demartini.dev@gmail.com
 Project-URL: Bug Tracker, https://github.com/Creariax5/IDlib/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `IDsys-0.0.6/setup.cfg` & `IDsys-0.0.7/setup.cfg`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 00000000: 5b6d 6574 6164 6174 615d 0d0a 6e61 6d65  [metadata]..name
 00000010: 203d 2049 4473 7973 0d0a 7665 7273 696f   = IDsys..versio
-00000020: 6e20 3d20 302e 302e 360d 0a61 7574 686f  n = 0.0.6..autho
+00000020: 6e20 3d20 302e 302e 370d 0a61 7574 686f  n = 0.0.7..autho
 00000030: 7220 3d20 466c 6f72 6961 6e20 4465 6d61  r = Florian Dema
 00000040: 7274 696e 690d 0a61 7574 686f 725f 656d  rtini..author_em
 00000050: 6169 6c20 3d20 666c 6f72 6961 6e2e 6465  ail = florian.de
 00000060: 6d61 7274 696e 692e 6465 7640 676d 6169  martini.dev@gmai
 00000070: 6c2e 636f 6d0d 0a64 6573 6372 6970 7469  l.com..descripti
 00000080: 6f6e 203d 2043 7265 6174 696e 6720 7379  on = Creating sy
 00000090: 7374 656d 6520 6f66 2069 6465 6e74 6966  steme of identif
```

### Comparing `IDsys-0.0.6/src/IDsys/ID.py` & `IDsys-0.0.7/src/IDsys/ID.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 class IdSys:
-    def __init__(self):
-        self.idLength = 4
+    def __init__(self, idLength=4):
+        self.idLength = idLength
         self.ids = 0
         self.elements = []
         self.type = "IdSys"
 
     def setId(self, obj):
         myIdTmp = str(self.ids)
         nbZero = self.idLength - len(myIdTmp)
@@ -32,7 +32,11 @@
         self.idSys = idSys
         self.myId = self.idSys.setId(self)
         self.type = self.__class__.__name__
 
 
 class ObjectExemple(Element):
     isObj = True
+
+    def __init__(self, idSys):
+        super().__init__(idSys)
+        self.nb = None
```

### Comparing `IDsys-0.0.6/src/IDsys.egg-info/PKG-INFO` & `IDsys-0.0.7/src/IDsys.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: IDsys
-Version: 0.0.6
+Version: 0.0.7
 Summary: Creating systeme of identification
 Home-page: https://github.com/Creariax5/IDlib
 Author: Florian Demartini
 Author-email: florian.demartini.dev@gmail.com
 Project-URL: Bug Tracker, https://github.com/Creariax5/IDlib/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

