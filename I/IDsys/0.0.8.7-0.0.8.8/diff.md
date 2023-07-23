# Comparing `tmp/IDsys-0.0.8.7.tar.gz` & `tmp/IDsys-0.0.8.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "IDsys-0.0.8.7.tar", last modified: Sun Jul 23 13:10:35 2023, max compression
+gzip compressed data, was "IDsys-0.0.8.8.tar", last modified: Sun Jul 23 13:12:54 2023, max compression
```

## Comparing `IDsys-0.0.8.7.tar` & `IDsys-0.0.8.8.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 13:10:35.409016 IDsys-0.0.8.7/
--rw-rw-rw-   0        0        0     1091 2023-07-23 11:51:48.000000 IDsys-0.0.8.7/LICENSE
--rw-rw-rw-   0        0        0      704 2023-07-23 13:10:35.409016 IDsys-0.0.8.7/PKG-INFO
--rw-rw-rw-   0        0        0      174 2023-07-23 11:52:27.000000 IDsys-0.0.8.7/README.md
--rw-rw-rw-   0        0        0      110 2023-07-22 14:43:25.000000 IDsys-0.0.8.7/pyproject.toml
--rw-rw-rw-   0        0        0      667 2023-07-23 13:10:35.410519 IDsys-0.0.8.7/setup.cfg
-drwxrwxrwx   0        0        0        0 2023-07-23 13:10:35.388519 IDsys-0.0.8.7/src/
-drwxrwxrwx   0        0        0        0 2023-07-23 13:10:35.396517 IDsys-0.0.8.7/src/IDsys/
--rw-rw-rw-   0        0        0     2086 2023-07-23 13:10:13.000000 IDsys-0.0.8.7/src/IDsys/ID.py
--rw-rw-rw-   0        0        0        0 2023-07-22 14:41:03.000000 IDsys-0.0.8.7/src/IDsys/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:10:35.408016 IDsys-0.0.8.7/src/IDsys.egg-info/
--rw-rw-rw-   0        0        0      704 2023-07-23 13:10:35.000000 IDsys-0.0.8.7/src/IDsys.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      212 2023-07-23 13:10:35.000000 IDsys-0.0.8.7/src/IDsys.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 13:10:35.000000 IDsys-0.0.8.7/src/IDsys.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        6 2023-07-23 13:10:35.000000 IDsys-0.0.8.7/src/IDsys.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 13:12:54.134911 IDsys-0.0.8.8/
+-rw-rw-rw-   0        0        0     1091 2023-07-23 11:51:48.000000 IDsys-0.0.8.8/LICENSE
+-rw-rw-rw-   0        0        0      704 2023-07-23 13:12:54.134911 IDsys-0.0.8.8/PKG-INFO
+-rw-rw-rw-   0        0        0      174 2023-07-23 11:52:27.000000 IDsys-0.0.8.8/README.md
+-rw-rw-rw-   0        0        0      110 2023-07-22 14:43:25.000000 IDsys-0.0.8.8/pyproject.toml
+-rw-rw-rw-   0        0        0      667 2023-07-23 13:12:54.136407 IDsys-0.0.8.8/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-07-23 13:12:54.113908 IDsys-0.0.8.8/src/
+drwxrwxrwx   0        0        0        0 2023-07-23 13:12:54.123908 IDsys-0.0.8.8/src/IDsys/
+-rw-rw-rw-   0        0        0     2080 2023-07-23 13:12:32.000000 IDsys-0.0.8.8/src/IDsys/ID.py
+-rw-rw-rw-   0        0        0        0 2023-07-22 14:41:03.000000 IDsys-0.0.8.8/src/IDsys/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 13:12:54.133911 IDsys-0.0.8.8/src/IDsys.egg-info/
+-rw-rw-rw-   0        0        0      704 2023-07-23 13:12:54.000000 IDsys-0.0.8.8/src/IDsys.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      212 2023-07-23 13:12:54.000000 IDsys-0.0.8.8/src/IDsys.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 13:12:54.000000 IDsys-0.0.8.8/src/IDsys.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        6 2023-07-23 13:12:54.000000 IDsys-0.0.8.8/src/IDsys.egg-info/top_level.txt
```

### Comparing `IDsys-0.0.8.7/LICENSE` & `IDsys-0.0.8.8/LICENSE`

 * *Files identical despite different names*

### Comparing `IDsys-0.0.8.7/PKG-INFO` & `IDsys-0.0.8.8/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: IDsys
-Version: 0.0.8.7
+Version: 0.0.8.8
 Summary: Creating systeme of identification
 Home-page: https://github.com/Creariax5/IDlib
 Author: Florian Demartini
 Author-email: florian.demartini.dev@gmail.com
 Project-URL: Bug Tracker, https://github.com/Creariax5/IDlib/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `IDsys-0.0.8.7/setup.cfg` & `IDsys-0.0.8.8/setup.cfg`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 00000000: 5b6d 6574 6164 6174 615d 0d0a 6e61 6d65  [metadata]..name
 00000010: 203d 2049 4473 7973 0d0a 7665 7273 696f   = IDsys..versio
-00000020: 6e20 3d20 302e 302e 382e 370d 0a61 7574  n = 0.0.8.7..aut
+00000020: 6e20 3d20 302e 302e 382e 380d 0a61 7574  n = 0.0.8.8..aut
 00000030: 686f 7220 3d20 466c 6f72 6961 6e20 4465  hor = Florian De
 00000040: 6d61 7274 696e 690d 0a61 7574 686f 725f  martini..author_
 00000050: 656d 6169 6c20 3d20 666c 6f72 6961 6e2e  email = florian.
 00000060: 6465 6d61 7274 696e 692e 6465 7640 676d  demartini.dev@gm
 00000070: 6169 6c2e 636f 6d0d 0a64 6573 6372 6970  ail.com..descrip
 00000080: 7469 6f6e 203d 2043 7265 6174 696e 6720  tion = Creating 
 00000090: 7379 7374 656d 6520 6f66 2069 6465 6e74  systeme of ident
```

### Comparing `IDsys-0.0.8.7/src/IDsys/ID.py` & `IDsys-0.0.8.8/src/IDsys/ID.py`

 * *Files 4% similar despite different names*

```diff
@@ -22,15 +22,15 @@
                 nbZero = self.idLength - len(myIdTmp)
                 myId = ""
                 for i in range(nbZero):
                     myId += "0"
                 myId += myIdTmp
                 return
             self.ids += 1
-            self.setId(self, obj, definedID)
+            self.setId(obj, definedID)
 
         else:
             if not self.idExist(definedID):
                 self.definedIds.append(definedID)
                 if definedID >= 0:
                     myIdTmp = str(definedID)
                     nbZero = self.idLength - len(myIdTmp)
```

### Comparing `IDsys-0.0.8.7/src/IDsys.egg-info/PKG-INFO` & `IDsys-0.0.8.8/src/IDsys.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: IDsys
-Version: 0.0.8.7
+Version: 0.0.8.8
 Summary: Creating systeme of identification
 Home-page: https://github.com/Creariax5/IDlib
 Author: Florian Demartini
 Author-email: florian.demartini.dev@gmail.com
 Project-URL: Bug Tracker, https://github.com/Creariax5/IDlib/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

