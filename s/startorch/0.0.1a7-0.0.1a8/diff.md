# Comparing `tmp/startorch-0.0.1a7.tar.gz` & `tmp/startorch-0.0.1a8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "startorch-0.0.1a7.tar", max compression
+gzip compressed data, was "startorch-0.0.1a8.tar", max compression
```

## Comparing `startorch-0.0.1a7.tar` & `startorch-0.0.1a8.tar`

### file list

```diff
@@ -1,13 +1,13 @@
--rw-r--r--   0        0        0     1501 2023-07-23 02:54:18.178444 startorch-0.0.1a7/LICENSE
--rw-r--r--   0        0        0       55 2023-07-23 02:54:18.178527 startorch-0.0.1a7/README.md
--rw-r--r--   0        0        0     4105 2023-07-23 19:05:23.611498 startorch-0.0.1a7/pyproject.toml
--rw-r--r--   0        0        0        0 2023-07-23 03:14:46.011361 startorch-0.0.1a7/src/startorch/__init__.py
--rw-r--r--   0        0        0     1473 2023-07-23 19:05:23.611763 startorch-0.0.1a7/src/startorch/random/__init__.py
--rw-r--r--   0        0        0    36850 2023-07-23 18:03:21.237056 startorch-0.0.1a7/src/startorch/random/bounded.py
--rw-r--r--   0        0        0     1460 2023-07-23 19:05:23.611924 startorch-0.0.1a7/src/startorch/random/discrete.py
--rw-r--r--   0        0        0     5984 2023-07-23 18:03:21.237164 startorch-0.0.1a7/src/startorch/random/infinite.py
--rw-r--r--   0        0        0    10653 2023-07-23 18:03:21.237271 startorch-0.0.1a7/src/startorch/random/semi_infinite.py
--rw-r--r--   0        0        0        0 2023-07-23 03:30:26.842167 startorch-0.0.1a7/src/startorch/utils/__init__.py
--rw-r--r--   0        0        0     1844 2023-07-23 03:41:58.369567 startorch-0.0.1a7/src/startorch/utils/seed.py
--rw-r--r--   0        0        0     1065 2023-07-23 03:30:26.842565 startorch-0.0.1a7/src/startorch/utils/tensor.py
--rw-r--r--   0        0        0     1122 1970-01-01 00:00:00.000000 startorch-0.0.1a7/PKG-INFO
+-rw-r--r--   0        0        0     1501 2023-07-23 19:18:02.377494 startorch-0.0.1a8/LICENSE
+-rw-r--r--   0        0        0       55 2023-07-23 19:18:02.377494 startorch-0.0.1a8/README.md
+-rw-r--r--   0        0        0     4105 2023-07-23 19:18:02.377494 startorch-0.0.1a8/pyproject.toml
+-rw-r--r--   0        0        0        0 2023-07-23 19:18:02.377494 startorch-0.0.1a8/src/startorch/__init__.py
+-rw-r--r--   0        0        0     1473 2023-07-23 19:18:02.377494 startorch-0.0.1a8/src/startorch/random/__init__.py
+-rw-r--r--   0        0        0    36850 2023-07-23 19:18:02.377494 startorch-0.0.1a8/src/startorch/random/bounded.py
+-rw-r--r--   0        0        0     1460 2023-07-23 19:18:02.377494 startorch-0.0.1a8/src/startorch/random/discrete.py
+-rw-r--r--   0        0        0     5984 2023-07-23 19:18:02.377494 startorch-0.0.1a8/src/startorch/random/infinite.py
+-rw-r--r--   0        0        0    10653 2023-07-23 19:18:02.377494 startorch-0.0.1a8/src/startorch/random/semi_infinite.py
+-rw-r--r--   0        0        0        0 2023-07-23 19:18:02.377494 startorch-0.0.1a8/src/startorch/utils/__init__.py
+-rw-r--r--   0        0        0     1844 2023-07-23 19:18:02.377494 startorch-0.0.1a8/src/startorch/utils/seed.py
+-rw-r--r--   0        0        0     1065 2023-07-23 19:18:02.377494 startorch-0.0.1a8/src/startorch/utils/tensor.py
+-rw-r--r--   0        0        0     1122 1970-01-01 00:00:00.000000 startorch-0.0.1a8/PKG-INFO
```

### Comparing `startorch-0.0.1a7/LICENSE` & `startorch-0.0.1a8/LICENSE`

 * *Files identical despite different names*

### Comparing `startorch-0.0.1a7/pyproject.toml` & `startorch-0.0.1a8/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "startorch"
-version = "0.0.1a7"
+version = "0.0.1a8"
 description = "synthetic time-series generator in PyTorch"
 readme = "README.md"
 authors = ["Thibaut Durand <durand.tibo+gh@gmail.com>"]
 homepage = "https://github.com/durandtibo/startorch"
 repository = "https://github.com/durandtibo/startorch"
 keywords = ["synthetic", "time-series", "pytorch"]
 license = "BSD-3-Clause"
```

### Comparing `startorch-0.0.1a7/src/startorch/random/__init__.py` & `startorch-0.0.1a8/src/startorch/random/__init__.py`

 * *Files identical despite different names*

### Comparing `startorch-0.0.1a7/src/startorch/random/bounded.py` & `startorch-0.0.1a8/src/startorch/random/bounded.py`

 * *Files identical despite different names*

### Comparing `startorch-0.0.1a7/src/startorch/random/discrete.py` & `startorch-0.0.1a8/src/startorch/random/discrete.py`

 * *Files identical despite different names*

### Comparing `startorch-0.0.1a7/src/startorch/random/infinite.py` & `startorch-0.0.1a8/src/startorch/random/infinite.py`

 * *Files identical despite different names*

### Comparing `startorch-0.0.1a7/src/startorch/random/semi_infinite.py` & `startorch-0.0.1a8/src/startorch/random/semi_infinite.py`

 * *Files identical despite different names*

### Comparing `startorch-0.0.1a7/src/startorch/utils/seed.py` & `startorch-0.0.1a8/src/startorch/utils/seed.py`

 * *Files identical despite different names*

### Comparing `startorch-0.0.1a7/src/startorch/utils/tensor.py` & `startorch-0.0.1a8/src/startorch/utils/tensor.py`

 * *Files identical despite different names*

### Comparing `startorch-0.0.1a7/PKG-INFO` & `startorch-0.0.1a8/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: startorch
-Version: 0.0.1a7
+Version: 0.0.1a8
 Summary: synthetic time-series generator in PyTorch
 Home-page: https://github.com/durandtibo/startorch
 License: BSD-3-Clause
 Keywords: synthetic,time-series,pytorch
 Author: Thibaut Durand
 Author-email: durand.tibo+gh@gmail.com
 Requires-Python: >=3.9,<4.0
```

