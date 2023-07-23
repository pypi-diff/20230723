# Comparing `tmp/IDsys-0.0.8.tar.gz` & `tmp/IDsys-0.0.8.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "IDsys-0.0.8.tar", last modified: Sun Jul 23 12:59:44 2023, max compression
+gzip compressed data, was "IDsys-0.0.8.5.tar", last modified: Sun Jul 23 13:05:21 2023, max compression
```

## Comparing `IDsys-0.0.8.tar` & `IDsys-0.0.8.5.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 12:59:44.210907 IDsys-0.0.8/
--rw-rw-rw-   0        0        0     1091 2023-07-23 11:51:48.000000 IDsys-0.0.8/LICENSE
--rw-rw-rw-   0        0        0      702 2023-07-23 12:59:44.210907 IDsys-0.0.8/PKG-INFO
--rw-rw-rw-   0        0        0      174 2023-07-23 11:52:27.000000 IDsys-0.0.8/README.md
--rw-rw-rw-   0        0        0      110 2023-07-22 14:43:25.000000 IDsys-0.0.8/pyproject.toml
--rw-rw-rw-   0        0        0      665 2023-07-23 12:59:44.212407 IDsys-0.0.8/setup.cfg
-drwxrwxrwx   0        0        0        0 2023-07-23 12:59:44.182908 IDsys-0.0.8/src/
-drwxrwxrwx   0        0        0        0 2023-07-23 12:59:44.195905 IDsys-0.0.8/src/IDsys/
--rw-rw-rw-   0        0        0     2067 2023-07-23 12:59:21.000000 IDsys-0.0.8/src/IDsys/ID.py
--rw-rw-rw-   0        0        0        0 2023-07-22 14:41:03.000000 IDsys-0.0.8/src/IDsys/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 12:59:44.209410 IDsys-0.0.8/src/IDsys.egg-info/
--rw-rw-rw-   0        0        0      702 2023-07-23 12:59:44.000000 IDsys-0.0.8/src/IDsys.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      212 2023-07-23 12:59:44.000000 IDsys-0.0.8/src/IDsys.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 12:59:44.000000 IDsys-0.0.8/src/IDsys.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        6 2023-07-23 12:59:44.000000 IDsys-0.0.8/src/IDsys.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 13:05:21.897647 IDsys-0.0.8.5/
+-rw-rw-rw-   0        0        0     1091 2023-07-23 11:51:48.000000 IDsys-0.0.8.5/LICENSE
+-rw-rw-rw-   0        0        0      704 2023-07-23 13:05:21.897647 IDsys-0.0.8.5/PKG-INFO
+-rw-rw-rw-   0        0        0      174 2023-07-23 11:52:27.000000 IDsys-0.0.8.5/README.md
+-rw-rw-rw-   0        0        0      110 2023-07-22 14:43:25.000000 IDsys-0.0.8.5/pyproject.toml
+-rw-rw-rw-   0        0        0      667 2023-07-23 13:05:21.899147 IDsys-0.0.8.5/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-07-23 13:05:21.873647 IDsys-0.0.8.5/src/
+drwxrwxrwx   0        0        0        0 2023-07-23 13:05:21.886646 IDsys-0.0.8.5/src/IDsys/
+-rw-rw-rw-   0        0        0     2081 2023-07-23 13:04:34.000000 IDsys-0.0.8.5/src/IDsys/ID.py
+-rw-rw-rw-   0        0        0        0 2023-07-22 14:41:03.000000 IDsys-0.0.8.5/src/IDsys/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 13:05:21.896645 IDsys-0.0.8.5/src/IDsys.egg-info/
+-rw-rw-rw-   0        0        0      704 2023-07-23 13:05:21.000000 IDsys-0.0.8.5/src/IDsys.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      212 2023-07-23 13:05:21.000000 IDsys-0.0.8.5/src/IDsys.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 13:05:21.000000 IDsys-0.0.8.5/src/IDsys.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        6 2023-07-23 13:05:21.000000 IDsys-0.0.8.5/src/IDsys.egg-info/top_level.txt
```

### Comparing `IDsys-0.0.8/LICENSE` & `IDsys-0.0.8.5/LICENSE`

 * *Files identical despite different names*

### Comparing `IDsys-0.0.8/PKG-INFO` & `IDsys-0.0.8.5/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: IDsys
-Version: 0.0.8
+Version: 0.0.8.5
 Summary: Creating systeme of identification
 Home-page: https://github.com/Creariax5/IDlib
 Author: Florian Demartini
 Author-email: florian.demartini.dev@gmail.com
 Project-URL: Bug Tracker, https://github.com/Creariax5/IDlib/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `IDsys-0.0.8/setup.cfg` & `IDsys-0.0.8.5/setup.cfg`

 * *Files 2% similar despite different names*

```diff
@@ -1,42 +1,42 @@
 00000000: 5b6d 6574 6164 6174 615d 0d0a 6e61 6d65  [metadata]..name
 00000010: 203d 2049 4473 7973 0d0a 7665 7273 696f   = IDsys..versio
-00000020: 6e20 3d20 302e 302e 380d 0a61 7574 686f  n = 0.0.8..autho
-00000030: 7220 3d20 466c 6f72 6961 6e20 4465 6d61  r = Florian Dema
-00000040: 7274 696e 690d 0a61 7574 686f 725f 656d  rtini..author_em
-00000050: 6169 6c20 3d20 666c 6f72 6961 6e2e 6465  ail = florian.de
-00000060: 6d61 7274 696e 692e 6465 7640 676d 6169  martini.dev@gmai
-00000070: 6c2e 636f 6d0d 0a64 6573 6372 6970 7469  l.com..descripti
-00000080: 6f6e 203d 2043 7265 6174 696e 6720 7379  on = Creating sy
-00000090: 7374 656d 6520 6f66 2069 6465 6e74 6966  steme of identif
-000000a0: 6963 6174 696f 6e0d 0a6c 6f6e 675f 6465  ication..long_de
-000000b0: 7363 7269 7074 696f 6e20 3d20 6669 6c65  scription = file
-000000c0: 3a20 5245 4144 4d45 2e6d 640d 0a6c 6f6e  : README.md..lon
-000000d0: 675f 6465 7363 7269 7074 696f 6e5f 636f  g_description_co
-000000e0: 6e74 656e 745f 7479 7065 203d 2074 6578  ntent_type = tex
-000000f0: 742f 6d61 726b 646f 776e 0d0a 7572 6c20  t/markdown..url 
-00000100: 3d20 6874 7470 733a 2f2f 6769 7468 7562  = https://github
-00000110: 2e63 6f6d 2f43 7265 6172 6961 7835 2f49  .com/Creariax5/I
-00000120: 446c 6962 0d0a 7072 6f6a 6563 745f 7572  Dlib..project_ur
-00000130: 6c73 203d 200d 0a09 4275 6720 5472 6163  ls = ...Bug Trac
-00000140: 6b65 7220 3d20 6874 7470 733a 2f2f 6769  ker = https://gi
-00000150: 7468 7562 2e63 6f6d 2f43 7265 6172 6961  thub.com/Crearia
-00000160: 7835 2f49 446c 6962 2f69 7373 7565 730d  x5/IDlib/issues.
-00000170: 0a63 6c61 7373 6966 6965 7273 203d 200d  .classifiers = .
-00000180: 0a09 5072 6f67 7261 6d6d 696e 6720 4c61  ..Programming La
-00000190: 6e67 7561 6765 203a 3a20 5079 7468 6f6e  nguage :: Python
-000001a0: 203a 3a20 330d 0a09 4c69 6365 6e73 6520   :: 3...License 
-000001b0: 3a3a 204f 5349 2041 7070 726f 7665 6420  :: OSI Approved 
-000001c0: 3a3a 204d 4954 204c 6963 656e 7365 0d0a  :: MIT License..
-000001d0: 094f 7065 7261 7469 6e67 2053 7973 7465  .Operating Syste
-000001e0: 6d20 3a3a 204f 5320 496e 6465 7065 6e64  m :: OS Independ
-000001f0: 656e 740d 0a0d 0a5b 6f70 7469 6f6e 735d  ent....[options]
-00000200: 0d0a 7061 636b 6167 655f 6469 7220 3d20  ..package_dir = 
-00000210: 0d0a 093d 2073 7263 0d0a 7061 636b 6167  ...= src..packag
-00000220: 6573 203d 2066 696e 643a 0d0a 7079 7468  es = find:..pyth
-00000230: 6f6e 5f72 6571 7569 7265 7320 3d20 3e3d  on_requires = >=
-00000240: 332e 360d 0a0d 0a5b 6f70 7469 6f6e 732e  3.6....[options.
-00000250: 7061 636b 6167 6573 2e66 696e 645d 0d0a  packages.find]..
-00000260: 7768 6572 6520 3d20 7372 630d 0a0d 0a5b  where = src....[
-00000270: 6567 675f 696e 666f 5d0d 0a74 6167 5f62  egg_info]..tag_b
-00000280: 7569 6c64 203d 200d 0a74 6167 5f64 6174  uild = ..tag_dat
-00000290: 6520 3d20 300d 0a0d 0a                   e = 0....
+00000020: 6e20 3d20 302e 302e 382e 350d 0a61 7574  n = 0.0.8.5..aut
+00000030: 686f 7220 3d20 466c 6f72 6961 6e20 4465  hor = Florian De
+00000040: 6d61 7274 696e 690d 0a61 7574 686f 725f  martini..author_
+00000050: 656d 6169 6c20 3d20 666c 6f72 6961 6e2e  email = florian.
+00000060: 6465 6d61 7274 696e 692e 6465 7640 676d  demartini.dev@gm
+00000070: 6169 6c2e 636f 6d0d 0a64 6573 6372 6970  ail.com..descrip
+00000080: 7469 6f6e 203d 2043 7265 6174 696e 6720  tion = Creating 
+00000090: 7379 7374 656d 6520 6f66 2069 6465 6e74  systeme of ident
+000000a0: 6966 6963 6174 696f 6e0d 0a6c 6f6e 675f  ification..long_
+000000b0: 6465 7363 7269 7074 696f 6e20 3d20 6669  description = fi
+000000c0: 6c65 3a20 5245 4144 4d45 2e6d 640d 0a6c  le: README.md..l
+000000d0: 6f6e 675f 6465 7363 7269 7074 696f 6e5f  ong_description_
+000000e0: 636f 6e74 656e 745f 7479 7065 203d 2074  content_type = t
+000000f0: 6578 742f 6d61 726b 646f 776e 0d0a 7572  ext/markdown..ur
+00000100: 6c20 3d20 6874 7470 733a 2f2f 6769 7468  l = https://gith
+00000110: 7562 2e63 6f6d 2f43 7265 6172 6961 7835  ub.com/Creariax5
+00000120: 2f49 446c 6962 0d0a 7072 6f6a 6563 745f  /IDlib..project_
+00000130: 7572 6c73 203d 200d 0a09 4275 6720 5472  urls = ...Bug Tr
+00000140: 6163 6b65 7220 3d20 6874 7470 733a 2f2f  acker = https://
+00000150: 6769 7468 7562 2e63 6f6d 2f43 7265 6172  github.com/Crear
+00000160: 6961 7835 2f49 446c 6962 2f69 7373 7565  iax5/IDlib/issue
+00000170: 730d 0a63 6c61 7373 6966 6965 7273 203d  s..classifiers =
+00000180: 200d 0a09 5072 6f67 7261 6d6d 696e 6720   ...Programming 
+00000190: 4c61 6e67 7561 6765 203a 3a20 5079 7468  Language :: Pyth
+000001a0: 6f6e 203a 3a20 330d 0a09 4c69 6365 6e73  on :: 3...Licens
+000001b0: 6520 3a3a 204f 5349 2041 7070 726f 7665  e :: OSI Approve
+000001c0: 6420 3a3a 204d 4954 204c 6963 656e 7365  d :: MIT License
+000001d0: 0d0a 094f 7065 7261 7469 6e67 2053 7973  ...Operating Sys
+000001e0: 7465 6d20 3a3a 204f 5320 496e 6465 7065  tem :: OS Indepe
+000001f0: 6e64 656e 740d 0a0d 0a5b 6f70 7469 6f6e  ndent....[option
+00000200: 735d 0d0a 7061 636b 6167 655f 6469 7220  s]..package_dir 
+00000210: 3d20 0d0a 093d 2073 7263 0d0a 7061 636b  = ...= src..pack
+00000220: 6167 6573 203d 2066 696e 643a 0d0a 7079  ages = find:..py
+00000230: 7468 6f6e 5f72 6571 7569 7265 7320 3d20  thon_requires = 
+00000240: 3e3d 332e 360d 0a0d 0a5b 6f70 7469 6f6e  >=3.6....[option
+00000250: 732e 7061 636b 6167 6573 2e66 696e 645d  s.packages.find]
+00000260: 0d0a 7768 6572 6520 3d20 7372 630d 0a0d  ..where = src...
+00000270: 0a5b 6567 675f 696e 666f 5d0d 0a74 6167  .[egg_info]..tag
+00000280: 5f62 7569 6c64 203d 200d 0a74 6167 5f64  _build = ..tag_d
+00000290: 6174 6520 3d20 300d 0a0d 0a              ate = 0....
```

### Comparing `IDsys-0.0.8/src/IDsys/ID.py` & `IDsys-0.0.8.5/src/IDsys/ID.py`

 * *Files 2% similar despite different names*

```diff
@@ -14,15 +14,15 @@
                 if id == definedId:
                     return True
         return False
 
     def setId(self, obj, definedID):
         if definedID == None:
             myIdTmp = str(self.ids)
-            if not self.idExist(definedID):
+            if not self.idExist(myIdTmp):
                 nbZero = self.idLength - len(myIdTmp)
                 myId = ""
                 for i in range(nbZero):
                     myId += "0"
                 myId += myIdTmp
                 return
             self.ids += 1
@@ -64,9 +64,9 @@
         self.type = self.__class__.__name__
 
 
 class ObjectExemple(Element):
     isObj = True
 
     def __init__(self, idSys):
-        super().__init__(idSys)
+        super().__init__(idSys, definedID=None)
         self.nb = None
```

### Comparing `IDsys-0.0.8/src/IDsys.egg-info/PKG-INFO` & `IDsys-0.0.8.5/src/IDsys.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: IDsys
-Version: 0.0.8
+Version: 0.0.8.5
 Summary: Creating systeme of identification
 Home-page: https://github.com/Creariax5/IDlib
 Author: Florian Demartini
 Author-email: florian.demartini.dev@gmail.com
 Project-URL: Bug Tracker, https://github.com/Creariax5/IDlib/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

