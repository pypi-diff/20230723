# Comparing `tmp/tftui-0.2.0.tar.gz` & `tmp/tftui-0.3.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "tftui-0.2.0.tar", last modified: Fri Jul 21 07:48:34 2023, max compression
+gzip compressed data, was "tftui-0.3.0.tar", last modified: Sun Jul 23 14:02:06 2023, max compression
```

## Comparing `tftui-0.2.0.tar` & `tftui-0.3.0.tar`

### file list

```diff
@@ -1,19 +1,19 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-21 07:48:34.600214 tftui-0.2.0/
--rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-07-21 07:48:22.000000 tftui-0.2.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       24 2023-07-21 07:48:22.000000 tftui-0.2.0/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)    13953 2023-07-21 07:48:34.592214 tftui-0.2.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      538 2023-07-21 07:48:22.000000 tftui-0.2.0/README.md
--rw-r--r--   0 runner    (1001) docker     (123)      673 2023-07-21 07:48:22.000000 tftui-0.2.0/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-21 07:48:34.600214 tftui-0.2.0/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-21 07:48:34.592214 tftui-0.2.0/src/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-21 07:48:34.592214 tftui-0.2.0/src/tftui/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-21 07:48:22.000000 tftui-0.2.0/src/tftui/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5193 2023-07-21 07:48:22.000000 tftui-0.2.0/src/tftui/__main__.py
--rw-r--r--   0 runner    (1001) docker     (123)      218 2023-07-21 07:48:22.000000 tftui-0.2.0/src/tftui/ui.css
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-21 07:48:34.592214 tftui-0.2.0/src/tftui.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)    13953 2023-07-21 07:48:34.000000 tftui-0.2.0/src/tftui.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      305 2023-07-21 07:48:34.000000 tftui-0.2.0/src/tftui.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-21 07:48:34.000000 tftui-0.2.0/src/tftui.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       46 2023-07-21 07:48:34.000000 tftui-0.2.0/src/tftui.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)       20 2023-07-21 07:48:34.000000 tftui-0.2.0/src/tftui.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        6 2023-07-21 07:48:34.000000 tftui-0.2.0/src/tftui.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:02:06.991974 tftui-0.3.0/
+-rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-07-23 14:01:52.000000 tftui-0.3.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       24 2023-07-23 14:01:52.000000 tftui-0.3.0/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)    14254 2023-07-23 14:02:06.991974 tftui-0.3.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      839 2023-07-23 14:01:52.000000 tftui-0.3.0/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      673 2023-07-23 14:01:52.000000 tftui-0.3.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 14:02:06.991974 tftui-0.3.0/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:02:06.987974 tftui-0.3.0/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:02:06.987974 tftui-0.3.0/src/tftui/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 14:01:52.000000 tftui-0.3.0/src/tftui/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9278 2023-07-23 14:01:52.000000 tftui-0.3.0/src/tftui/__main__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      544 2023-07-23 14:01:52.000000 tftui-0.3.0/src/tftui/ui.css
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 14:02:06.991974 tftui-0.3.0/src/tftui.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)    14254 2023-07-23 14:02:06.000000 tftui-0.3.0/src/tftui.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      305 2023-07-23 14:02:06.000000 tftui-0.3.0/src/tftui.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 14:02:06.000000 tftui-0.3.0/src/tftui.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       46 2023-07-23 14:02:06.000000 tftui-0.3.0/src/tftui.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       20 2023-07-23 14:02:06.000000 tftui-0.3.0/src/tftui.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        6 2023-07-23 14:02:06.000000 tftui-0.3.0/src/tftui.egg-info/top_level.txt
```

### Comparing `tftui-0.2.0/LICENSE` & `tftui-0.3.0/LICENSE`

 * *Files identical despite different names*

### Comparing `tftui-0.2.0/PKG-INFO` & `tftui-0.3.0/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: tftui
-Version: 0.2.0
+Version: 0.3.0
 Summary: Terraform Textual User Interface
 Author: Ido Avraham
 License:                                  Apache License
                                    Version 2.0, January 2004
                                 http://www.apache.org/licenses/
         
            TERMS AND CONDITIONS FOR USE, REPRODUCTION, AND DISTRIBUTION
@@ -211,24 +211,33 @@
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
 Requires-Python: >=3.9
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # TFTUI - The terraform textual UI
-`TFTUI` is a textual gui that disaplys a terraform state, and allows the user to read and interact with it.
+`TFTUI` is a textual gui that disaplys a terraform state and allows the user to read and interact with it.
 
 ## Features
-### version 0.1.0
+
+### version 0.3
+- [x] Added loading screen and status bar
+- [x] Added selection of resources
+- [x] Added refresh state functionality
+- [x] Added taint/untaint functionality
+- [x] Refactoring
+
+### version 0.2
 - [x] Display terraform state tree
 - [x] Display a single resource state
 
-## Preview
+## Demo
 
-![](https://link.to.image "preview")
+![](https://github.com/idoavrah/terraform-tui/raw/main/demo/demo.gif "demo")
 
 ## Installation
 
 | Tool            | Install             | Upgrade                       |
 |-----------------| ------------------- | ----------------------------- |
 | PIP             | `pip install tftui` | `pip install --upgrade tftui` |
+| PIPX            | `pipx install tftui`| `pipx upgrade tftui`          |
```

### Comparing `tftui-0.2.0/pyproject.toml` & `tftui-0.3.0/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires      = ["setuptools>=61.0.0", "wheel"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "tftui"
-version = "0.2.0"
+version = "0.3.0"
 description = "Terraform Textual User Interface"
 readme = "README.md"
 authors = [{ name = "Ido Avraham" }]
 license = { file = "LICENSE" }
 classifiers = [
     "License :: OSI Approved :: Apache Software License",
     "Programming Language :: Python",
```

### Comparing `tftui-0.2.0/src/tftui.egg-info/PKG-INFO` & `tftui-0.3.0/src/tftui.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: tftui
-Version: 0.2.0
+Version: 0.3.0
 Summary: Terraform Textual User Interface
 Author: Ido Avraham
 License:                                  Apache License
                                    Version 2.0, January 2004
                                 http://www.apache.org/licenses/
         
            TERMS AND CONDITIONS FOR USE, REPRODUCTION, AND DISTRIBUTION
@@ -211,24 +211,33 @@
 Classifier: Programming Language :: Python
 Classifier: Programming Language :: Python :: 3
 Requires-Python: >=3.9
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # TFTUI - The terraform textual UI
-`TFTUI` is a textual gui that disaplys a terraform state, and allows the user to read and interact with it.
+`TFTUI` is a textual gui that disaplys a terraform state and allows the user to read and interact with it.
 
 ## Features
-### version 0.1.0
+
+### version 0.3
+- [x] Added loading screen and status bar
+- [x] Added selection of resources
+- [x] Added refresh state functionality
+- [x] Added taint/untaint functionality
+- [x] Refactoring
+
+### version 0.2
 - [x] Display terraform state tree
 - [x] Display a single resource state
 
-## Preview
+## Demo
 
-![](https://link.to.image "preview")
+![](https://github.com/idoavrah/terraform-tui/raw/main/demo/demo.gif "demo")
 
 ## Installation
 
 | Tool            | Install             | Upgrade                       |
 |-----------------| ------------------- | ----------------------------- |
 | PIP             | `pip install tftui` | `pip install --upgrade tftui` |
+| PIPX            | `pipx install tftui`| `pipx upgrade tftui`          |
```

