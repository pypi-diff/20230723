# Comparing `tmp/vinhvh_package-0.0.5.tar.gz` & `tmp/vinhvh_package-0.0.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "vinhvh_package-0.0.5.tar", last modified: Sun Jul 23 07:04:06 2023, max compression
+gzip compressed data, was "vinhvh_package-0.0.6.tar", last modified: Sun Jul 23 10:37:24 2023, max compression
```

## Comparing `vinhvh_package-0.0.5.tar` & `vinhvh_package-0.0.6.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 07:04:06.629879 vinhvh_package-0.0.5/
--rw-rw-rw-   0        0        0     1091 2023-07-23 05:09:13.000000 vinhvh_package-0.0.5/LICENSE
--rw-rw-rw-   0        0        0      557 2023-07-23 07:04:06.628883 vinhvh_package-0.0.5/PKG-INFO
--rw-rw-rw-   0        0        0       25 2023-07-23 06:07:00.000000 vinhvh_package-0.0.5/README.md
--rw-rw-rw-   0        0        0      612 2023-07-23 07:03:38.000000 vinhvh_package-0.0.5/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-07-23 07:04:06.629879 vinhvh_package-0.0.5/setup.cfg
-drwxrwxrwx   0        0        0        0 2023-07-23 07:04:06.570722 vinhvh_package-0.0.5/src/
-drwxrwxrwx   0        0        0        0 2023-07-23 07:04:06.576738 vinhvh_package-0.0.5/src/vinhvh_package/
--rw-rw-rw-   0        0        0        0 2023-07-23 06:05:35.000000 vinhvh_package-0.0.5/src/vinhvh_package/__init__.py
--rw-rw-rw-   0        0        0    10276 2023-07-23 06:54:41.000000 vinhvh_package-0.0.5/src/vinhvh_package/vinhvh.py
-drwxrwxrwx   0        0        0        0 2023-07-23 07:04:06.595795 vinhvh_package-0.0.5/src/vinhvh_package.egg-info/
--rw-rw-rw-   0        0        0      557 2023-07-23 07:04:06.000000 vinhvh_package-0.0.5/src/vinhvh_package.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      260 2023-07-23 07:04:06.000000 vinhvh_package-0.0.5/src/vinhvh_package.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 07:04:06.000000 vinhvh_package-0.0.5/src/vinhvh_package.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       15 2023-07-23 07:04:06.000000 vinhvh_package-0.0.5/src/vinhvh_package.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 10:37:24.873783 vinhvh_package-0.0.6/
+-rw-rw-rw-   0        0        0     1091 2023-07-23 05:09:13.000000 vinhvh_package-0.0.6/LICENSE
+-rw-rw-rw-   0        0        0      557 2023-07-23 10:37:24.872780 vinhvh_package-0.0.6/PKG-INFO
+-rw-rw-rw-   0        0        0       25 2023-07-23 06:07:00.000000 vinhvh_package-0.0.6/README.md
+-rw-rw-rw-   0        0        0      612 2023-07-23 10:36:52.000000 vinhvh_package-0.0.6/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-07-23 10:37:24.873783 vinhvh_package-0.0.6/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-07-23 10:37:24.495676 vinhvh_package-0.0.6/src/
+drwxrwxrwx   0        0        0        0 2023-07-23 10:37:24.852728 vinhvh_package-0.0.6/src/vinhvh_package/
+-rw-rw-rw-   0        0        0        0 2023-07-23 06:05:35.000000 vinhvh_package-0.0.6/src/vinhvh_package/__init__.py
+-rw-rw-rw-   0        0        0    14125 2023-07-23 10:36:04.000000 vinhvh_package-0.0.6/src/vinhvh_package/vinhvh.py
+drwxrwxrwx   0        0        0        0 2023-07-23 10:37:24.870775 vinhvh_package-0.0.6/src/vinhvh_package.egg-info/
+-rw-rw-rw-   0        0        0      557 2023-07-23 10:37:24.000000 vinhvh_package-0.0.6/src/vinhvh_package.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      260 2023-07-23 10:37:24.000000 vinhvh_package-0.0.6/src/vinhvh_package.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 10:37:24.000000 vinhvh_package-0.0.6/src/vinhvh_package.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       15 2023-07-23 10:37:24.000000 vinhvh_package-0.0.6/src/vinhvh_package.egg-info/top_level.txt
```

### Comparing `vinhvh_package-0.0.5/LICENSE` & `vinhvh_package-0.0.6/LICENSE`

 * *Files identical despite different names*

### Comparing `vinhvh_package-0.0.5/PKG-INFO` & `vinhvh_package-0.0.6/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: vinhvh_package
-Version: 0.0.5
+Version: 0.0.6
 Summary: A small example package
 Author-email: VinhVH <vinhvh89.dc@gmail.com>
 Project-URL: Homepage, https://github.com/VinhVu8x/packaging_tutorial
 Project-URL: Bug Tracker, https://github.com/VinhVu8x/packaging_tutorial/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

### Comparing `vinhvh_package-0.0.5/pyproject.toml` & `vinhvh_package-0.0.6/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "vinhvh_package"
-version = "0.0.5"
+version = "0.0.6"
 authors = [
   { name="VinhVH", email="vinhvh89.dc@gmail.com" },
 ]
 description = "A small example package"
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = [
```

### Comparing `vinhvh_package-0.0.5/src/vinhvh_package.egg-info/PKG-INFO` & `vinhvh_package-0.0.6/src/vinhvh_package.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: vinhvh-package
-Version: 0.0.5
+Version: 0.0.6
 Summary: A small example package
 Author-email: VinhVH <vinhvh89.dc@gmail.com>
 Project-URL: Homepage, https://github.com/VinhVu8x/packaging_tutorial
 Project-URL: Bug Tracker, https://github.com/VinhVu8x/packaging_tutorial/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
```

