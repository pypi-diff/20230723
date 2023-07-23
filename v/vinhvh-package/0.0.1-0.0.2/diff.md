# Comparing `tmp/vinhvh_package-0.0.1.tar.gz` & `tmp/vinhvh_package-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "vinhvh_package-0.0.1.tar", last modified: Sun Jul 23 06:07:45 2023, max compression
+gzip compressed data, was "vinhvh_package-0.0.2.tar", last modified: Sun Jul 23 06:30:35 2023, max compression
```

## Comparing `vinhvh_package-0.0.1.tar` & `vinhvh_package-0.0.2.tar`

### file list

```diff
@@ -1,15 +1,12 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 06:07:45.468840 vinhvh_package-0.0.1/
--rw-rw-rw-   0        0        0     1091 2023-07-23 05:09:13.000000 vinhvh_package-0.0.1/LICENSE
--rw-rw-rw-   0        0        0      557 2023-07-23 06:07:45.468840 vinhvh_package-0.0.1/PKG-INFO
--rw-rw-rw-   0        0        0       25 2023-07-23 06:07:00.000000 vinhvh_package-0.0.1/README.md
--rw-rw-rw-   0        0        0      612 2023-07-23 06:06:46.000000 vinhvh_package-0.0.1/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-07-23 06:07:45.468840 vinhvh_package-0.0.1/setup.cfg
-drwxrwxrwx   0        0        0        0 2023-07-23 06:07:45.410684 vinhvh_package-0.0.1/src/
-drwxrwxrwx   0        0        0        0 2023-07-23 06:07:45.429736 vinhvh_package-0.0.1/src/vinhvh_package/
--rw-rw-rw-   0        0        0        0 2023-07-23 06:05:35.000000 vinhvh_package-0.0.1/src/vinhvh_package/__init__.py
--rw-rw-rw-   0        0        0    10303 2023-07-23 06:06:31.000000 vinhvh_package-0.0.1/src/vinhvh_package/vinhvh.py
-drwxrwxrwx   0        0        0        0 2023-07-23 06:07:45.466865 vinhvh_package-0.0.1/src/vinhvh_package.egg-info/
--rw-rw-rw-   0        0        0      557 2023-07-23 06:07:45.000000 vinhvh_package-0.0.1/src/vinhvh_package.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      260 2023-07-23 06:07:45.000000 vinhvh_package-0.0.1/src/vinhvh_package.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 06:07:45.000000 vinhvh_package-0.0.1/src/vinhvh_package.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       15 2023-07-23 06:07:45.000000 vinhvh_package-0.0.1/src/vinhvh_package.egg-info/top_level.txt
+drwxrwxrwx   0        0        0        0 2023-07-23 06:30:35.119756 vinhvh_package-0.0.2/
+-rw-rw-rw-   0        0        0     1091 2023-07-23 05:09:13.000000 vinhvh_package-0.0.2/LICENSE
+-rw-rw-rw-   0        0        0      628 2023-07-23 06:30:35.119756 vinhvh_package-0.0.2/PKG-INFO
+-rw-rw-rw-   0        0        0       25 2023-07-23 06:07:00.000000 vinhvh_package-0.0.2/README.md
+-rw-rw-rw-   0        0        0      612 2023-07-23 06:29:19.000000 vinhvh_package-0.0.2/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-07-23 06:30:35.120759 vinhvh_package-0.0.2/setup.cfg
+-rw-rw-rw-   0        0        0      805 2023-07-23 06:29:11.000000 vinhvh_package-0.0.2/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 06:30:35.118753 vinhvh_package-0.0.2/vinhvh_package.egg-info/
+-rw-rw-rw-   0        0        0      628 2023-07-23 06:30:34.000000 vinhvh_package-0.0.2/vinhvh_package.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      193 2023-07-23 06:30:34.000000 vinhvh_package-0.0.2/vinhvh_package.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 06:30:34.000000 vinhvh_package-0.0.2/vinhvh_package.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 06:30:34.000000 vinhvh_package-0.0.2/vinhvh_package.egg-info/top_level.txt
```

### Comparing `vinhvh_package-0.0.1/LICENSE` & `vinhvh_package-0.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `vinhvh_package-0.0.1/PKG-INFO` & `vinhvh_package-0.0.2/vinhvh_package.egg-info/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,16 +1,18 @@
 Metadata-Version: 2.1
-Name: vinhvh_package
-Version: 0.0.1
+Name: vinhvh-package
+Version: 0.0.2
 Summary: A small example package
+Home-page: https://github.com/VinhVu8x/vinhvh_package
+Author: VinhVH
 Author-email: VinhVH <vinhvh89.dc@gmail.com>
 Project-URL: Homepage, https://github.com/VinhVu8x/packaging_tutorial
 Project-URL: Bug Tracker, https://github.com/VinhVu8x/packaging_tutorial/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
-Requires-Python: >=3.7
+Requires-Python: >=3.6
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 This is personal tool
```

### Comparing `vinhvh_package-0.0.1/pyproject.toml` & `vinhvh_package-0.0.2/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=61.0"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "vinhvh_package"
-version = "0.0.1"
+version = "0.0.2"
 authors = [
   { name="VinhVH", email="vinhvh89.dc@gmail.com" },
 ]
 description = "A small example package"
 readme = "README.md"
 requires-python = ">=3.7"
 classifiers = [
```

### Comparing `vinhvh_package-0.0.1/src/vinhvh_package.egg-info/PKG-INFO` & `vinhvh_package-0.0.2/PKG-INFO`

 * *Files 14% similar despite different names*

```diff
@@ -1,16 +1,18 @@
 Metadata-Version: 2.1
-Name: vinhvh-package
-Version: 0.0.1
+Name: vinhvh_package
+Version: 0.0.2
 Summary: A small example package
+Home-page: https://github.com/VinhVu8x/vinhvh_package
+Author: VinhVH
 Author-email: VinhVH <vinhvh89.dc@gmail.com>
 Project-URL: Homepage, https://github.com/VinhVu8x/packaging_tutorial
 Project-URL: Bug Tracker, https://github.com/VinhVu8x/packaging_tutorial/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Operating System :: OS Independent
-Requires-Python: >=3.7
+Requires-Python: >=3.6
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 This is personal tool
```

