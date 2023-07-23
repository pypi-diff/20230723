# Comparing `tmp/smpl-pkg-powly535-0.0.2.tar.gz` & `tmp/smpl-pkg-powly535-0.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "smpl-pkg-powly535-0.0.2.tar", last modified: Sun Jul 23 15:13:39 2023, max compression
+gzip compressed data, was "smpl-pkg-powly535-0.0.3.tar", last modified: Sun Jul 23 15:27:01 2023, max compression
```

## Comparing `smpl-pkg-powly535-0.0.2.tar` & `smpl-pkg-powly535-0.0.3.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 15:13:39.607363 smpl-pkg-powly535-0.0.2/
--rw-rw-rw-   0        0        0        0 2023-07-23 14:45:30.000000 smpl-pkg-powly535-0.0.2/LICENSE
--rw-rw-rw-   0        0        0      513 2023-07-23 15:13:39.608357 smpl-pkg-powly535-0.0.2/PKG-INFO
--rw-rw-rw-   0        0        0        0 2023-07-23 14:46:09.000000 smpl-pkg-powly535-0.0.2/README.md
--rw-rw-rw-   0        0        0      108 2023-07-23 14:48:45.000000 smpl-pkg-powly535-0.0.2/pyproject.toml
--rw-rw-rw-   0        0        0      654 2023-07-23 15:13:39.611350 smpl-pkg-powly535-0.0.2/setup.cfg
-drwxrwxrwx   0        0        0        0 2023-07-23 15:13:39.559346 smpl-pkg-powly535-0.0.2/src/
-drwxrwxrwx   0        0        0        0 2023-07-23 15:13:39.573307 smpl-pkg-powly535-0.0.2/src/smpl_pkg/
--rw-rw-rw-   0        0        0        9 2023-07-23 15:03:30.000000 smpl-pkg-powly535-0.0.2/src/smpl_pkg/__init__.py
--rw-rw-rw-   0        0        0       32 2023-07-23 15:10:43.000000 smpl-pkg-powly535-0.0.2/src/smpl_pkg/smpl.py
-drwxrwxrwx   0        0        0        0 2023-07-23 15:13:39.604452 smpl-pkg-powly535-0.0.2/src/smpl_pkg_powly535.egg-info/
--rw-rw-rw-   0        0        0      513 2023-07-23 15:13:39.000000 smpl-pkg-powly535-0.0.2/src/smpl_pkg_powly535.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      268 2023-07-23 15:13:39.000000 smpl-pkg-powly535-0.0.2/src/smpl_pkg_powly535.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 15:13:39.000000 smpl-pkg-powly535-0.0.2/src/smpl_pkg_powly535.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        9 2023-07-23 15:13:39.000000 smpl-pkg-powly535-0.0.2/src/smpl_pkg_powly535.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 15:27:01.722997 smpl-pkg-powly535-0.0.3/
+-rw-rw-rw-   0        0        0        0 2023-07-23 14:45:30.000000 smpl-pkg-powly535-0.0.3/LICENSE
+-rw-rw-rw-   0        0        0      513 2023-07-23 15:27:01.723596 smpl-pkg-powly535-0.0.3/PKG-INFO
+-rw-rw-rw-   0        0        0        0 2023-07-23 14:46:09.000000 smpl-pkg-powly535-0.0.3/README.md
+-rw-rw-rw-   0        0        0      108 2023-07-23 14:48:45.000000 smpl-pkg-powly535-0.0.3/pyproject.toml
+-rw-rw-rw-   0        0        0      654 2023-07-23 15:27:01.728059 smpl-pkg-powly535-0.0.3/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-07-23 15:27:01.685915 smpl-pkg-powly535-0.0.3/src/
+drwxrwxrwx   0        0        0        0 2023-07-23 15:27:01.700001 smpl-pkg-powly535-0.0.3/src/smpl_pkg/
+-rw-rw-rw-   0        0        0        0 2023-07-23 15:26:29.000000 smpl-pkg-powly535-0.0.3/src/smpl_pkg/__init__.py
+-rw-rw-rw-   0        0        0       32 2023-07-23 15:10:43.000000 smpl-pkg-powly535-0.0.3/src/smpl_pkg/smpl.py
+drwxrwxrwx   0        0        0        0 2023-07-23 15:27:01.721995 smpl-pkg-powly535-0.0.3/src/smpl_pkg_powly535.egg-info/
+-rw-rw-rw-   0        0        0      513 2023-07-23 15:27:01.000000 smpl-pkg-powly535-0.0.3/src/smpl_pkg_powly535.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      268 2023-07-23 15:27:01.000000 smpl-pkg-powly535-0.0.3/src/smpl_pkg_powly535.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 15:27:01.000000 smpl-pkg-powly535-0.0.3/src/smpl_pkg_powly535.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        9 2023-07-23 15:27:01.000000 smpl-pkg-powly535-0.0.3/src/smpl_pkg_powly535.egg-info/top_level.txt
```

### Comparing `smpl-pkg-powly535-0.0.2/PKG-INFO` & `smpl-pkg-powly535-0.0.3/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: smpl-pkg-powly535
-Version: 0.0.2
+Version: 0.0.3
 Summary: A small example package
 Home-page: https://github.com/pypa/smplpkg
 Author: powly535
 Author-email: shyamkrishnanpv535lenovo@gmail.com
 Project-URL: Bug Tracker, https://github.com/pypa/smplpkg/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `smpl-pkg-powly535-0.0.2/setup.cfg` & `smpl-pkg-powly535-0.0.3/setup.cfg`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 00000000: 5b6d 6574 6164 6174 615d 0d0a 6e61 6d65  [metadata]..name
 00000010: 203d 2073 6d70 6c2d 706b 672d 706f 776c   = smpl-pkg-powl
 00000020: 7935 3335 0d0a 7665 7273 696f 6e20 3d20  y535..version = 
-00000030: 302e 302e 320d 0a61 7574 686f 7220 3d20  0.0.2..author = 
+00000030: 302e 302e 330d 0a61 7574 686f 7220 3d20  0.0.3..author = 
 00000040: 706f 776c 7935 3335 0d0a 6175 7468 6f72  powly535..author
 00000050: 5f65 6d61 696c 203d 2073 6879 616d 6b72  _email = shyamkr
 00000060: 6973 686e 616e 7076 3533 356c 656e 6f76  ishnanpv535lenov
 00000070: 6f40 676d 6169 6c2e 636f 6d0d 0a64 6573  o@gmail.com..des
 00000080: 6372 6970 7469 6f6e 203d 2041 2073 6d61  cription = A sma
 00000090: 6c6c 2065 7861 6d70 6c65 2070 6163 6b61  ll example packa
 000000a0: 6765 0d0a 6c6f 6e67 5f64 6573 6372 6970  ge..long_descrip
```

### Comparing `smpl-pkg-powly535-0.0.2/src/smpl_pkg_powly535.egg-info/PKG-INFO` & `smpl-pkg-powly535-0.0.3/src/smpl_pkg_powly535.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: smpl-pkg-powly535
-Version: 0.0.2
+Version: 0.0.3
 Summary: A small example package
 Home-page: https://github.com/pypa/smplpkg
 Author: powly535
 Author-email: shyamkrishnanpv535lenovo@gmail.com
 Project-URL: Bug Tracker, https://github.com/pypa/smplpkg/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
```

