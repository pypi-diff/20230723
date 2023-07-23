# Comparing `tmp/smpl-pkg-powly535-0.0.1.tar.gz` & `tmp/smpl-pkg-powly535-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "smpl-pkg-powly535-0.0.1.tar", last modified: Sun Jul 23 14:57:25 2023, max compression
+gzip compressed data, was "smpl-pkg-powly535-0.0.2.tar", last modified: Sun Jul 23 15:13:39 2023, max compression
```

## Comparing `smpl-pkg-powly535-0.0.1.tar` & `smpl-pkg-powly535-0.0.2.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 14:57:25.925835 smpl-pkg-powly535-0.0.1/
--rw-rw-rw-   0        0        0        0 2023-07-23 14:45:30.000000 smpl-pkg-powly535-0.0.1/LICENSE
--rw-rw-rw-   0        0        0      506 2023-07-23 14:57:25.925835 smpl-pkg-powly535-0.0.1/PKG-INFO
--rw-rw-rw-   0        0        0        0 2023-07-23 14:46:09.000000 smpl-pkg-powly535-0.0.1/README.md
--rw-rw-rw-   0        0        0      108 2023-07-23 14:48:45.000000 smpl-pkg-powly535-0.0.1/pyproject.toml
--rw-rw-rw-   0        0        0      647 2023-07-23 14:57:25.932788 smpl-pkg-powly535-0.0.1/setup.cfg
-drwxrwxrwx   0        0        0        0 2023-07-23 14:57:25.836130 smpl-pkg-powly535-0.0.1/src/
-drwxrwxrwx   0        0        0        0 2023-07-23 14:57:25.877675 smpl-pkg-powly535-0.0.1/src/smpl_pkg/
--rw-rw-rw-   0        0        0       22 2023-07-23 14:49:58.000000 smpl-pkg-powly535-0.0.1/src/smpl_pkg/__init__.py
--rw-rw-rw-   0        0        0       32 2023-07-23 14:49:15.000000 smpl-pkg-powly535-0.0.1/src/smpl_pkg/smpl.py
-drwxrwxrwx   0        0        0        0 2023-07-23 14:57:25.923842 smpl-pkg-powly535-0.0.1/src/smpl_pkg_powly535.egg-info/
--rw-rw-rw-   0        0        0      506 2023-07-23 14:57:25.000000 smpl-pkg-powly535-0.0.1/src/smpl_pkg_powly535.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      268 2023-07-23 14:57:25.000000 smpl-pkg-powly535-0.0.1/src/smpl_pkg_powly535.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 14:57:25.000000 smpl-pkg-powly535-0.0.1/src/smpl_pkg_powly535.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        9 2023-07-23 14:57:25.000000 smpl-pkg-powly535-0.0.1/src/smpl_pkg_powly535.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 15:13:39.607363 smpl-pkg-powly535-0.0.2/
+-rw-rw-rw-   0        0        0        0 2023-07-23 14:45:30.000000 smpl-pkg-powly535-0.0.2/LICENSE
+-rw-rw-rw-   0        0        0      513 2023-07-23 15:13:39.608357 smpl-pkg-powly535-0.0.2/PKG-INFO
+-rw-rw-rw-   0        0        0        0 2023-07-23 14:46:09.000000 smpl-pkg-powly535-0.0.2/README.md
+-rw-rw-rw-   0        0        0      108 2023-07-23 14:48:45.000000 smpl-pkg-powly535-0.0.2/pyproject.toml
+-rw-rw-rw-   0        0        0      654 2023-07-23 15:13:39.611350 smpl-pkg-powly535-0.0.2/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-07-23 15:13:39.559346 smpl-pkg-powly535-0.0.2/src/
+drwxrwxrwx   0        0        0        0 2023-07-23 15:13:39.573307 smpl-pkg-powly535-0.0.2/src/smpl_pkg/
+-rw-rw-rw-   0        0        0        9 2023-07-23 15:03:30.000000 smpl-pkg-powly535-0.0.2/src/smpl_pkg/__init__.py
+-rw-rw-rw-   0        0        0       32 2023-07-23 15:10:43.000000 smpl-pkg-powly535-0.0.2/src/smpl_pkg/smpl.py
+drwxrwxrwx   0        0        0        0 2023-07-23 15:13:39.604452 smpl-pkg-powly535-0.0.2/src/smpl_pkg_powly535.egg-info/
+-rw-rw-rw-   0        0        0      513 2023-07-23 15:13:39.000000 smpl-pkg-powly535-0.0.2/src/smpl_pkg_powly535.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      268 2023-07-23 15:13:39.000000 smpl-pkg-powly535-0.0.2/src/smpl_pkg_powly535.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 15:13:39.000000 smpl-pkg-powly535-0.0.2/src/smpl_pkg_powly535.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        9 2023-07-23 15:13:39.000000 smpl-pkg-powly535-0.0.2/src/smpl_pkg_powly535.egg-info/top_level.txt
```

### Comparing `smpl-pkg-powly535-0.0.1/setup.cfg` & `smpl-pkg-powly535-0.0.2/setup.cfg`

 * *Files 17% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 00000000: 5b6d 6574 6164 6174 615d 0d0a 6e61 6d65  [metadata]..name
 00000010: 203d 2073 6d70 6c2d 706b 672d 706f 776c   = smpl-pkg-powl
 00000020: 7935 3335 0d0a 7665 7273 696f 6e20 3d20  y535..version = 
-00000030: 302e 302e 310d 0a61 7574 686f 7220 3d20  0.0.1..author = 
+00000030: 302e 302e 320d 0a61 7574 686f 7220 3d20  0.0.2..author = 
 00000040: 706f 776c 7935 3335 0d0a 6175 7468 6f72  powly535..author
 00000050: 5f65 6d61 696c 203d 2073 6879 616d 6b72  _email = shyamkr
 00000060: 6973 686e 616e 7076 3533 356c 656e 6f76  ishnanpv535lenov
 00000070: 6f40 676d 6169 6c2e 636f 6d0d 0a64 6573  o@gmail.com..des
 00000080: 6372 6970 7469 6f6e 203d 2041 2073 6d61  cription = A sma
 00000090: 6c6c 2065 7861 6d70 6c65 2070 6163 6b61  ll example packa
 000000a0: 6765 0d0a 6c6f 6e67 5f64 6573 6372 6970  ge..long_descrip
@@ -15,27 +15,27 @@
 000000e0: 5f74 7970 6520 3d20 7465 7874 2f6d 6172  _type = text/mar
 000000f0: 6b64 6f77 6e0d 0a75 726c 203d 2068 7474  kdown..url = htt
 00000100: 7073 3a2f 2f67 6974 6875 622e 636f 6d2f  ps://github.com/
 00000110: 7079 7061 2f73 6d70 6c70 6b67 0d0a 7072  pypa/smplpkg..pr
 00000120: 6f6a 6563 745f 7572 6c73 203d 200d 0a09  oject_urls = ...
 00000130: 4275 6720 5472 6163 6b65 7220 3d20 6874  Bug Tracker = ht
 00000140: 7470 733a 2f2f 6769 7468 7562 2e63 6f6d  tps://github.com
-00000150: 2f70 7970 612f 2f69 7373 7565 730d 0a63  /pypa//issues..c
-00000160: 6c61 7373 6966 6965 7273 203d 200d 0a09  lassifiers = ...
-00000170: 5072 6f67 7261 6d6d 696e 6720 4c61 6e67  Programming Lang
-00000180: 7561 6765 203a 3a20 5079 7468 6f6e 203a  uage :: Python :
-00000190: 3a20 330d 0a09 4c69 6365 6e73 6520 3a3a  : 3...License ::
-000001a0: 204f 5349 2041 7070 726f 7665 6420 3a3a   OSI Approved ::
-000001b0: 204d 4954 204c 6963 656e 7365 0d0a 094f   MIT License...O
-000001c0: 7065 7261 7469 6e67 2053 7973 7465 6d20  perating System 
-000001d0: 3a3a 204f 5320 496e 6465 7065 6e64 656e  :: OS Independen
-000001e0: 740d 0a0d 0a5b 6f70 7469 6f6e 735d 0d0a  t....[options]..
-000001f0: 7061 636b 6167 655f 6469 7220 3d20 0d0a  package_dir = ..
-00000200: 093d 2073 7263 0d0a 7061 636b 6167 6573  .= src..packages
-00000210: 203d 2066 696e 643a 0d0a 7079 7468 6f6e   = find:..python
-00000220: 5f72 6571 7569 7265 7320 3d20 3e3d 332e  _requires = >=3.
-00000230: 360d 0a0d 0a5b 6f70 7469 6f6e 732e 7061  6....[options.pa
-00000240: 636b 6167 6573 2e66 696e 645d 0d0a 7768  ckages.find]..wh
-00000250: 6572 6520 3d20 7372 630d 0a0d 0a5b 6567  ere = src....[eg
-00000260: 675f 696e 666f 5d0d 0a74 6167 5f62 7569  g_info]..tag_bui
-00000270: 6c64 203d 200d 0a74 6167 5f64 6174 6520  ld = ..tag_date 
-00000280: 3d20 300d 0a0d 0a                        = 0....
+00000150: 2f70 7970 612f 736d 706c 706b 672f 6973  /pypa/smplpkg/is
+00000160: 7375 6573 0d0a 636c 6173 7369 6669 6572  sues..classifier
+00000170: 7320 3d20 0d0a 0950 726f 6772 616d 6d69  s = ...Programmi
+00000180: 6e67 204c 616e 6775 6167 6520 3a3a 2050  ng Language :: P
+00000190: 7974 686f 6e20 3a3a 2033 0d0a 094c 6963  ython :: 3...Lic
+000001a0: 656e 7365 203a 3a20 4f53 4920 4170 7072  ense :: OSI Appr
+000001b0: 6f76 6564 203a 3a20 4d49 5420 4c69 6365  oved :: MIT Lice
+000001c0: 6e73 650d 0a09 4f70 6572 6174 696e 6720  nse...Operating 
+000001d0: 5379 7374 656d 203a 3a20 4f53 2049 6e64  System :: OS Ind
+000001e0: 6570 656e 6465 6e74 0d0a 0d0a 5b6f 7074  ependent....[opt
+000001f0: 696f 6e73 5d0d 0a70 6163 6b61 6765 5f64  ions]..package_d
+00000200: 6972 203d 200d 0a09 3d20 7372 630d 0a70  ir = ...= src..p
+00000210: 6163 6b61 6765 7320 3d20 6669 6e64 3a0d  ackages = find:.
+00000220: 0a70 7974 686f 6e5f 7265 7175 6972 6573  .python_requires
+00000230: 203d 203e 3d33 2e36 0d0a 0d0a 5b6f 7074   = >=3.6....[opt
+00000240: 696f 6e73 2e70 6163 6b61 6765 732e 6669  ions.packages.fi
+00000250: 6e64 5d0d 0a77 6865 7265 203d 2073 7263  nd]..where = src
+00000260: 0d0a 0d0a 5b65 6767 5f69 6e66 6f5d 0d0a  ....[egg_info]..
+00000270: 7461 675f 6275 696c 6420 3d20 0d0a 7461  tag_build = ..ta
+00000280: 675f 6461 7465 203d 2030 0d0a 0d0a       g_date = 0....
```

