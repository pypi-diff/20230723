# Comparing `tmp/phylotrackpy-0.1.15.tar.gz` & `tmp/phylotrackpy-0.1.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "phylotrackpy-0.1.15.tar", last modified: Sun Jul 23 00:39:37 2023, max compression
+gzip compressed data, was "phylotrackpy-0.1.5.tar", last modified: Tue Mar  7 22:26:56 2023, max compression
```

## Comparing `phylotrackpy-0.1.15.tar` & `phylotrackpy-0.1.5.tar`

### file list

```diff
@@ -1,19 +1,19 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 00:39:37.828806 phylotrackpy-0.1.15/
--rw-r--r--   0 runner    (1001) docker     (123)     1069 2023-07-23 00:39:22.000000 phylotrackpy-0.1.15/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     6824 2023-07-23 00:39:37.828806 phylotrackpy-0.1.15/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     6491 2023-07-23 00:39:22.000000 phylotrackpy-0.1.15/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 00:39:37.828806 phylotrackpy-0.1.15/phylotrackpy/
--rw-r--r--   0 runner    (1001) docker     (123)      201 2023-07-23 00:39:22.000000 phylotrackpy-0.1.15/phylotrackpy/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 00:39:37.828806 phylotrackpy-0.1.15/phylotrackpy.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     6824 2023-07-23 00:39:37.000000 phylotrackpy-0.1.15/phylotrackpy.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      340 2023-07-23 00:39:37.000000 phylotrackpy-0.1.15/phylotrackpy.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 00:39:37.000000 phylotrackpy-0.1.15/phylotrackpy.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 00:39:37.000000 phylotrackpy-0.1.15/phylotrackpy.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)       15 2023-07-23 00:39:37.000000 phylotrackpy-0.1.15/phylotrackpy.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       13 2023-07-23 00:39:37.000000 phylotrackpy-0.1.15/phylotrackpy.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)      299 2023-07-23 00:39:22.000000 phylotrackpy-0.1.15/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)      528 2023-07-23 00:39:37.828806 phylotrackpy-0.1.15/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1463 2023-07-23 00:39:22.000000 phylotrackpy-0.1.15/setup.py
--rw-r--r--   0 runner    (1001) docker     (123)    43604 2023-07-23 00:39:22.000000 phylotrackpy-0.1.15/systematics_bindings.cpp
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 00:39:37.828806 phylotrackpy-0.1.15/test/
--rw-r--r--   0 runner    (1001) docker     (123)     5025 2023-07-23 00:39:22.000000 phylotrackpy-0.1.15/test/test_systematics.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-07 22:26:56.720024 phylotrackpy-0.1.5/
+-rw-r--r--   0 runner    (1001) docker     (123)     1069 2023-03-07 22:26:42.000000 phylotrackpy-0.1.5/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     1864 2023-03-07 22:26:56.720024 phylotrackpy-0.1.5/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1532 2023-03-07 22:26:42.000000 phylotrackpy-0.1.5/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-07 22:26:56.716024 phylotrackpy-0.1.5/phylotrackpy/
+-rw-r--r--   0 runner    (1001) docker     (123)      200 2023-03-07 22:26:42.000000 phylotrackpy-0.1.5/phylotrackpy/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-07 22:26:56.720024 phylotrackpy-0.1.5/phylotrackpy.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1864 2023-03-07 22:26:56.000000 phylotrackpy-0.1.5/phylotrackpy.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      340 2023-03-07 22:26:56.000000 phylotrackpy-0.1.5/phylotrackpy.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-03-07 22:26:56.000000 phylotrackpy-0.1.5/phylotrackpy.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-03-07 22:26:56.000000 phylotrackpy-0.1.5/phylotrackpy.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)       15 2023-03-07 22:26:56.000000 phylotrackpy-0.1.5/phylotrackpy.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       13 2023-03-07 22:26:56.000000 phylotrackpy-0.1.5/phylotrackpy.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      229 2023-03-07 22:26:42.000000 phylotrackpy-0.1.5/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)      527 2023-03-07 22:26:56.720024 phylotrackpy-0.1.5/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1462 2023-03-07 22:26:42.000000 phylotrackpy-0.1.5/setup.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17747 2023-03-07 22:26:42.000000 phylotrackpy-0.1.5/systematics_bindings.cpp
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-07 22:26:56.720024 phylotrackpy-0.1.5/test/
+-rw-r--r--   0 runner    (1001) docker     (123)     2529 2023-03-07 22:26:42.000000 phylotrackpy-0.1.5/test/test_systematics.py
```

### Comparing `phylotrackpy-0.1.15/LICENSE` & `phylotrackpy-0.1.5/LICENSE`

 * *Files identical despite different names*

### Comparing `phylotrackpy-0.1.15/setup.cfg` & `phylotrackpy-0.1.5/setup.cfg`

 * *Files 1% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 [bumpversion]
-current_version = 0.1.15
+current_version = 0.1.5
 commit = True
 tag = True
 
 [bumpversion:file:docs/conf.py]
 search = = "{current_version}"
 replace = = "{new_version}"
```

### Comparing `phylotrackpy-0.1.15/setup.py` & `phylotrackpy-0.1.5/setup.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import sys
 
 from pybind11 import get_cmake_dir
 # Available at setup time due to pyproject.toml
 from pybind11.setup_helpers import Pybind11Extension, build_ext
 from setuptools import setup
 
-__version__ = "0.1.15"
+__version__ = "0.1.5"
 
 # The main interface is through Pybind11Extension.
 # * You can add cxx_std=11/14/17, and then build_ext can be removed.
 # * You can set include_pybind11=false to add the include directory yourself,
 #   say from a submodule.
 #
 # Note:
```

