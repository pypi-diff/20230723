# Comparing `tmp/IDsys-0.0.4.tar.gz` & `tmp/IDsys-0.0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "IDsys-0.0.4.tar", last modified: Sun Jul 23 11:39:54 2023, max compression
+gzip compressed data, was "IDsys-0.0.5.tar", last modified: Sun Jul 23 12:02:36 2023, max compression
```

## Comparing `IDsys-0.0.4.tar` & `IDsys-0.0.5.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 11:39:54.896979 IDsys-0.0.4/
--rw-rw-rw-   0        0        0        0 2023-07-22 14:41:03.000000 IDsys-0.0.4/LICENSE
--rw-rw-rw-   0        0        0      518 2023-07-23 11:39:54.896979 IDsys-0.0.4/PKG-INFO
--rw-rw-rw-   0        0        0        0 2023-07-22 14:45:24.000000 IDsys-0.0.4/README.md
--rw-rw-rw-   0        0        0      110 2023-07-22 14:43:25.000000 IDsys-0.0.4/pyproject.toml
--rw-rw-rw-   0        0        0      659 2023-07-23 11:39:54.898482 IDsys-0.0.4/setup.cfg
-drwxrwxrwx   0        0        0        0 2023-07-23 11:39:54.872978 IDsys-0.0.4/src/
-drwxrwxrwx   0        0        0        0 2023-07-23 11:39:54.888978 IDsys-0.0.4/src/IDsys.egg-info/
--rw-rw-rw-   0        0        0      518 2023-07-23 11:39:54.000000 IDsys-0.0.4/src/IDsys.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      220 2023-07-23 11:39:54.000000 IDsys-0.0.4/src/IDsys.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 11:39:54.000000 IDsys-0.0.4/src/IDsys.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       10 2023-07-23 11:39:54.000000 IDsys-0.0.4/src/IDsys.egg-info/top_level.txt
-drwxrwxrwx   0        0        0        0 2023-07-23 11:39:54.895979 IDsys-0.0.4/src/mypackage/
--rw-rw-rw-   0        0        0      933 2023-07-23 11:39:19.000000 IDsys-0.0.4/src/mypackage/ID.py
--rw-rw-rw-   0        0        0        0 2023-07-22 14:41:03.000000 IDsys-0.0.4/src/mypackage/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 12:02:36.835053 IDsys-0.0.5/
+-rw-rw-rw-   0        0        0     1091 2023-07-23 11:51:48.000000 IDsys-0.0.5/LICENSE
+-rw-rw-rw-   0        0        0      702 2023-07-23 12:02:36.835053 IDsys-0.0.5/PKG-INFO
+-rw-rw-rw-   0        0        0      174 2023-07-23 11:52:27.000000 IDsys-0.0.5/README.md
+-rw-rw-rw-   0        0        0      110 2023-07-22 14:43:25.000000 IDsys-0.0.5/pyproject.toml
+-rw-rw-rw-   0        0        0      665 2023-07-23 12:02:36.837051 IDsys-0.0.5/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-07-23 12:02:36.815549 IDsys-0.0.5/src/
+drwxrwxrwx   0        0        0        0 2023-07-23 12:02:36.822550 IDsys-0.0.5/src/IDsys/
+-rw-rw-rw-   0        0        0      933 2023-07-23 11:39:19.000000 IDsys-0.0.5/src/IDsys/ID.py
+-rw-rw-rw-   0        0        0        0 2023-07-22 14:41:03.000000 IDsys-0.0.5/src/IDsys/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 12:02:36.834051 IDsys-0.0.5/src/IDsys.egg-info/
+-rw-rw-rw-   0        0        0      702 2023-07-23 12:02:36.000000 IDsys-0.0.5/src/IDsys.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      212 2023-07-23 12:02:36.000000 IDsys-0.0.5/src/IDsys.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 12:02:36.000000 IDsys-0.0.5/src/IDsys.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        6 2023-07-23 12:02:36.000000 IDsys-0.0.5/src/IDsys.egg-info/top_level.txt
```

### Comparing `IDsys-0.0.4/setup.cfg` & `IDsys-0.0.5/setup.cfg`

 * *Files 26% similar despite different names*

```diff
@@ -1,42 +1,42 @@
 00000000: 5b6d 6574 6164 6174 615d 0d0a 6e61 6d65  [metadata]..name
 00000010: 203d 2049 4473 7973 0d0a 7665 7273 696f   = IDsys..versio
-00000020: 6e20 3d20 302e 302e 340d 0a61 7574 686f  n = 0.0.4..autho
+00000020: 6e20 3d20 302e 302e 350d 0a61 7574 686f  n = 0.0.5..autho
 00000030: 7220 3d20 466c 6f72 6961 6e20 4465 6d61  r = Florian Dema
 00000040: 7274 696e 690d 0a61 7574 686f 725f 656d  rtini..author_em
 00000050: 6169 6c20 3d20 666c 6f72 6961 6e2e 6465  ail = florian.de
 00000060: 6d61 7274 696e 692e 6465 7640 676d 6169  martini.dev@gmai
 00000070: 6c2e 636f 6d0d 0a64 6573 6372 6970 7469  l.com..descripti
-00000080: 6f6e 203d 2043 7265 6174 6520 6120 7379  on = Create a sy
-00000090: 7374 656d 6520 6f66 2049 440d 0a6c 6f6e  steme of ID..lon
-000000a0: 675f 6465 7363 7269 7074 696f 6e20 3d20  g_description = 
-000000b0: 6669 6c65 3a20 5245 4144 4d45 2e6d 640d  file: README.md.
-000000c0: 0a6c 6f6e 675f 6465 7363 7269 7074 696f  .long_descriptio
-000000d0: 6e5f 636f 6e74 656e 745f 7479 7065 203d  n_content_type =
-000000e0: 2074 6578 742f 6d61 726b 646f 776e 0d0a   text/markdown..
-000000f0: 7572 6c20 3d20 6874 7470 733a 2f2f 6769  url = https://gi
-00000100: 7468 7562 2e63 6f6d 2f70 7970 612f 7361  thub.com/pypa/sa
-00000110: 6d70 6c65 7072 6f6a 6563 740d 0a70 726f  mpleproject..pro
-00000120: 6a65 6374 5f75 726c 7320 3d20 0d0a 0942  ject_urls = ...B
-00000130: 7567 2054 7261 636b 6572 203d 2068 7474  ug Tracker = htt
-00000140: 7073 3a2f 2f67 6974 6875 622e 636f 6d2f  ps://github.com/
-00000150: 7079 7061 2f73 616d 706c 6570 726f 6a65  pypa/sampleproje
-00000160: 6374 2f69 7373 7565 730d 0a63 6c61 7373  ct/issues..class
-00000170: 6966 6965 7273 203d 200d 0a09 5072 6f67  ifiers = ...Prog
-00000180: 7261 6d6d 696e 6720 4c61 6e67 7561 6765  ramming Language
-00000190: 203a 3a20 5079 7468 6f6e 203a 3a20 330d   :: Python :: 3.
-000001a0: 0a09 4c69 6365 6e73 6520 3a3a 204f 5349  ..License :: OSI
-000001b0: 2041 7070 726f 7665 6420 3a3a 204d 4954   Approved :: MIT
-000001c0: 204c 6963 656e 7365 0d0a 094f 7065 7261   License...Opera
-000001d0: 7469 6e67 2053 7973 7465 6d20 3a3a 204f  ting System :: O
-000001e0: 5320 496e 6465 7065 6e64 656e 740d 0a0d  S Independent...
-000001f0: 0a5b 6f70 7469 6f6e 735d 0d0a 7061 636b  .[options]..pack
-00000200: 6167 655f 6469 7220 3d20 0d0a 093d 2073  age_dir = ...= s
-00000210: 7263 0d0a 7061 636b 6167 6573 203d 2066  rc..packages = f
-00000220: 696e 643a 0d0a 7079 7468 6f6e 5f72 6571  ind:..python_req
-00000230: 7569 7265 7320 3d20 3e3d 332e 360d 0a0d  uires = >=3.6...
-00000240: 0a5b 6f70 7469 6f6e 732e 7061 636b 6167  .[options.packag
-00000250: 6573 2e66 696e 645d 0d0a 7768 6572 6520  es.find]..where 
-00000260: 3d20 7372 630d 0a0d 0a5b 6567 675f 696e  = src....[egg_in
-00000270: 666f 5d0d 0a74 6167 5f62 7569 6c64 203d  fo]..tag_build =
-00000280: 200d 0a74 6167 5f64 6174 6520 3d20 300d   ..tag_date = 0.
-00000290: 0a0d 0a                                  ...
+00000080: 6f6e 203d 2043 7265 6174 696e 6720 7379  on = Creating sy
+00000090: 7374 656d 6520 6f66 2069 6465 6e74 6966  steme of identif
+000000a0: 6963 6174 696f 6e0d 0a6c 6f6e 675f 6465  ication..long_de
+000000b0: 7363 7269 7074 696f 6e20 3d20 6669 6c65  scription = file
+000000c0: 3a20 5245 4144 4d45 2e6d 640d 0a6c 6f6e  : README.md..lon
+000000d0: 675f 6465 7363 7269 7074 696f 6e5f 636f  g_description_co
+000000e0: 6e74 656e 745f 7479 7065 203d 2074 6578  ntent_type = tex
+000000f0: 742f 6d61 726b 646f 776e 0d0a 7572 6c20  t/markdown..url 
+00000100: 3d20 6874 7470 733a 2f2f 6769 7468 7562  = https://github
+00000110: 2e63 6f6d 2f43 7265 6172 6961 7835 2f49  .com/Creariax5/I
+00000120: 446c 6962 0d0a 7072 6f6a 6563 745f 7572  Dlib..project_ur
+00000130: 6c73 203d 200d 0a09 4275 6720 5472 6163  ls = ...Bug Trac
+00000140: 6b65 7220 3d20 6874 7470 733a 2f2f 6769  ker = https://gi
+00000150: 7468 7562 2e63 6f6d 2f43 7265 6172 6961  thub.com/Crearia
+00000160: 7835 2f49 446c 6962 2f69 7373 7565 730d  x5/IDlib/issues.
+00000170: 0a63 6c61 7373 6966 6965 7273 203d 200d  .classifiers = .
+00000180: 0a09 5072 6f67 7261 6d6d 696e 6720 4c61  ..Programming La
+00000190: 6e67 7561 6765 203a 3a20 5079 7468 6f6e  nguage :: Python
+000001a0: 203a 3a20 330d 0a09 4c69 6365 6e73 6520   :: 3...License 
+000001b0: 3a3a 204f 5349 2041 7070 726f 7665 6420  :: OSI Approved 
+000001c0: 3a3a 204d 4954 204c 6963 656e 7365 0d0a  :: MIT License..
+000001d0: 094f 7065 7261 7469 6e67 2053 7973 7465  .Operating Syste
+000001e0: 6d20 3a3a 204f 5320 496e 6465 7065 6e64  m :: OS Independ
+000001f0: 656e 740d 0a0d 0a5b 6f70 7469 6f6e 735d  ent....[options]
+00000200: 0d0a 7061 636b 6167 655f 6469 7220 3d20  ..package_dir = 
+00000210: 0d0a 093d 2073 7263 0d0a 7061 636b 6167  ...= src..packag
+00000220: 6573 203d 2066 696e 643a 0d0a 7079 7468  es = find:..pyth
+00000230: 6f6e 5f72 6571 7569 7265 7320 3d20 3e3d  on_requires = >=
+00000240: 332e 360d 0a0d 0a5b 6f70 7469 6f6e 732e  3.6....[options.
+00000250: 7061 636b 6167 6573 2e66 696e 645d 0d0a  packages.find]..
+00000260: 7768 6572 6520 3d20 7372 630d 0a0d 0a5b  where = src....[
+00000270: 6567 675f 696e 666f 5d0d 0a74 6167 5f62  egg_info]..tag_b
+00000280: 7569 6c64 203d 200d 0a74 6167 5f64 6174  uild = ..tag_dat
+00000290: 6520 3d20 300d 0a0d 0a                   e = 0....
```

### Comparing `IDsys-0.0.4/src/mypackage/ID.py` & `IDsys-0.0.5/src/IDsys/ID.py`

 * *Files identical despite different names*

