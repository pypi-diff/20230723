# Comparing `tmp/spotRiver-0.0.95.tar.gz` & `tmp/spotRiver-0.0.96.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "spotRiver-0.0.95.tar", last modified: Fri Jul  7 07:12:45 2023, max compression
+gzip compressed data, was "spotRiver-0.0.96.tar", last modified: Sun Jul 23 12:28:50 2023, max compression
```

## Comparing `spotRiver-0.0.95.tar` & `spotRiver-0.0.96.tar`

### file list

```diff
@@ -1,46 +1,47 @@
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-07 07:12:45.069869 spotRiver-0.0.95/
--rw-r--r--   0 bartz      (501) staff       (20)     1520 2023-01-29 11:49:35.000000 spotRiver-0.0.95/LICENSE
--rw-r--r--   0 bartz      (501) staff       (20)      164 2023-03-22 20:43:16.000000 spotRiver-0.0.95/MANIFEST.in
--rw-r--r--   0 bartz      (501) staff       (20)     3383 2023-07-07 07:12:45.069758 spotRiver-0.0.95/PKG-INFO
--rw-r--r--   0 bartz      (501) staff       (20)     2912 2023-01-29 16:41:52.000000 spotRiver-0.0.95/README.md
--rw-r--r--   0 bartz      (501) staff       (20)     1046 2023-07-06 18:58:29.000000 spotRiver-0.0.95/pyproject.toml
--rw-r--r--   0 bartz      (501) staff       (20)       38 2023-07-07 07:12:45.069908 spotRiver-0.0.95/setup.cfg
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-07 07:12:45.064656 spotRiver-0.0.95/src/
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-07 07:12:45.065341 spotRiver-0.0.95/src/spotRiver/
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-07 07:12:45.068029 spotRiver-0.0.95/src/spotRiver/data/
--rw-r--r--   0 bartz      (501) staff       (20)      413 2023-01-29 11:52:00.000000 spotRiver-0.0.95/src/spotRiver/data/__init__.py
--rw-r--r--   0 bartz      (501) staff       (20)     2182 2023-01-17 12:39:58.000000 spotRiver-0.0.95/src/spotRiver/data/airline-passengers.csv
--rw-r--r--   0 bartz      (501) staff       (20)     1023 2023-03-27 20:31:30.000000 spotRiver-0.0.95/src/spotRiver/data/airline_passengers.py
--rw-r--r--   0 bartz      (501) staff       (20)    13646 2023-03-22 20:37:51.000000 spotRiver-0.0.95/src/spotRiver/data/base.py
--rw-r--r--   0 bartz      (501) staff       (20)     1113 2023-03-13 20:26:53.000000 spotRiver-0.0.95/src/spotRiver/data/bike_sharing.py
--rw-r--r--   0 bartz      (501) staff       (20)     1870 2023-03-07 16:50:39.000000 spotRiver-0.0.95/src/spotRiver/data/generic.py
--rw-r--r--   0 bartz      (501) staff       (20)     7751 2023-03-07 16:50:39.000000 spotRiver-0.0.95/src/spotRiver/data/opm.py
--rw-r--r--   0 bartz      (501) staff       (20)    17554 2023-04-08 14:44:16.000000 spotRiver-0.0.95/src/spotRiver/data/river_hyper_dict.json
--rw-r--r--   0 bartz      (501) staff       (20)      329 2023-03-31 21:04:02.000000 spotRiver-0.0.95/src/spotRiver/data/river_hyper_dict.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-07 07:12:45.068256 spotRiver-0.0.95/src/spotRiver/data/synth/
--rw-r--r--   0 bartz      (501) staff       (20)      328 2023-01-18 17:25:51.000000 spotRiver-0.0.95/src/spotRiver/data/synth/__init__.py
--rw-r--r--   0 bartz      (501) staff       (20)     2442 2023-02-20 15:46:37.000000 spotRiver-0.0.95/src/spotRiver/data/synth/sea.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-07 07:12:45.068368 spotRiver-0.0.95/src/spotRiver/drift/
--rw-r--r--   0 bartz      (501) staff       (20)      767 2023-02-20 15:46:37.000000 spotRiver-0.0.95/src/spotRiver/drift/drift_generator.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-07 07:12:45.068718 spotRiver-0.0.95/src/spotRiver/evaluation/
--rw-r--r--   0 bartz      (501) staff       (20)    29393 2023-04-06 12:46:27.000000 spotRiver-0.0.95/src/spotRiver/evaluation/eval_bml.py
--rw-r--r--   0 bartz      (501) staff       (20)     3958 2023-02-26 22:39:12.000000 spotRiver-0.0.95/src/spotRiver/evaluation/eval_nowcast.py
--rw-r--r--   0 bartz      (501) staff       (20)     6752 2023-04-06 12:44:54.000000 spotRiver-0.0.95/src/spotRiver/evaluation/eval_oml.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-07 07:12:45.068942 spotRiver-0.0.95/src/spotRiver/fun/
--rw-r--r--   0 bartz      (501) staff       (20)     5391 2023-06-10 18:01:21.000000 spotRiver-0.0.95/src/spotRiver/fun/hyperriver.py
--rw-r--r--   0 bartz      (501) staff       (20)    32460 2023-04-22 19:31:59.000000 spotRiver-0.0.95/src/spotRiver/fun/hyperriver_old.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-07 07:12:45.069059 spotRiver-0.0.95/src/spotRiver/plot/
--rw-r--r--   0 bartz      (501) staff       (20)     1340 2023-03-11 14:52:45.000000 spotRiver-0.0.95/src/spotRiver/plot/stats.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-07 07:12:45.069158 spotRiver-0.0.95/src/spotRiver/preprocess/
--rw-r--r--   0 bartz      (501) staff       (20)     2488 2023-03-07 16:50:39.000000 spotRiver-0.0.95/src/spotRiver/preprocess/impute.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-07 07:12:45.069393 spotRiver-0.0.95/src/spotRiver/utils/
--rw-r--r--   0 bartz      (501) staff       (20)     2284 2023-07-06 19:04:13.000000 spotRiver-0.0.95/src/spotRiver/utils/data_conversion.py
--rw-r--r--   0 bartz      (501) staff       (20)     5549 2023-04-13 20:07:21.000000 spotRiver-0.0.95/src/spotRiver/utils/features.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-07 07:12:45.066568 spotRiver-0.0.95/src/spotRiver.egg-info/
--rw-r--r--   0 bartz      (501) staff       (20)     3383 2023-07-07 07:12:45.000000 spotRiver-0.0.95/src/spotRiver.egg-info/PKG-INFO
--rw-r--r--   0 bartz      (501) staff       (20)      987 2023-07-07 07:12:45.000000 spotRiver-0.0.95/src/spotRiver.egg-info/SOURCES.txt
--rw-r--r--   0 bartz      (501) staff       (20)        1 2023-07-07 07:12:45.000000 spotRiver-0.0.95/src/spotRiver.egg-info/dependency_links.txt
--rw-r--r--   0 bartz      (501) staff       (20)       20 2023-07-07 07:12:45.000000 spotRiver-0.0.95/src/spotRiver.egg-info/requires.txt
--rw-r--r--   0 bartz      (501) staff       (20)       10 2023-07-07 07:12:45.000000 spotRiver-0.0.95/src/spotRiver.egg-info/top_level.txt
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-07 07:12:45.069511 spotRiver-0.0.95/test/
--rw-r--r--   0 bartz      (501) staff       (20)      510 2023-02-25 09:55:05.000000 spotRiver-0.0.95/test/test_features.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 12:28:50.529826 spotRiver-0.0.96/
+-rw-r--r--   0 bartz      (501) staff       (20)     1520 2023-01-29 11:49:35.000000 spotRiver-0.0.96/LICENSE
+-rw-r--r--   0 bartz      (501) staff       (20)      164 2023-03-22 20:43:16.000000 spotRiver-0.0.96/MANIFEST.in
+-rw-r--r--   0 bartz      (501) staff       (20)     3383 2023-07-23 12:28:50.529670 spotRiver-0.0.96/PKG-INFO
+-rw-r--r--   0 bartz      (501) staff       (20)     2912 2023-01-29 16:41:52.000000 spotRiver-0.0.96/README.md
+-rw-r--r--   0 bartz      (501) staff       (20)     1347 2023-07-23 12:21:29.000000 spotRiver-0.0.96/pyproject.toml
+-rw-r--r--   0 bartz      (501) staff       (20)       38 2023-07-23 12:28:50.529876 spotRiver-0.0.96/setup.cfg
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 12:28:50.523872 spotRiver-0.0.96/src/
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 12:28:50.524355 spotRiver-0.0.96/src/spotRiver/
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 12:28:50.527679 spotRiver-0.0.96/src/spotRiver/data/
+-rw-r--r--   0 bartz      (501) staff       (20)  1993321 2023-07-23 12:15:18.000000 spotRiver-0.0.96/src/spotRiver/data/UnivariateData.csv
+-rw-r--r--   0 bartz      (501) staff       (20)      413 2023-01-29 11:52:00.000000 spotRiver-0.0.96/src/spotRiver/data/__init__.py
+-rw-r--r--   0 bartz      (501) staff       (20)     2182 2023-01-17 12:39:58.000000 spotRiver-0.0.96/src/spotRiver/data/airline-passengers.csv
+-rw-r--r--   0 bartz      (501) staff       (20)     1023 2023-03-27 20:31:30.000000 spotRiver-0.0.96/src/spotRiver/data/airline_passengers.py
+-rw-r--r--   0 bartz      (501) staff       (20)    13646 2023-03-22 20:37:51.000000 spotRiver-0.0.96/src/spotRiver/data/base.py
+-rw-r--r--   0 bartz      (501) staff       (20)     1113 2023-03-13 20:26:53.000000 spotRiver-0.0.96/src/spotRiver/data/bike_sharing.py
+-rw-r--r--   0 bartz      (501) staff       (20)     2795 2023-07-23 12:28:36.000000 spotRiver-0.0.96/src/spotRiver/data/generic.py
+-rw-r--r--   0 bartz      (501) staff       (20)     7751 2023-03-07 16:50:39.000000 spotRiver-0.0.96/src/spotRiver/data/opm.py
+-rw-r--r--   0 bartz      (501) staff       (20)    17554 2023-04-08 14:44:16.000000 spotRiver-0.0.96/src/spotRiver/data/river_hyper_dict.json
+-rw-r--r--   0 bartz      (501) staff       (20)      329 2023-03-31 21:04:02.000000 spotRiver-0.0.96/src/spotRiver/data/river_hyper_dict.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 12:28:50.527924 spotRiver-0.0.96/src/spotRiver/data/synth/
+-rw-r--r--   0 bartz      (501) staff       (20)      328 2023-01-18 17:25:51.000000 spotRiver-0.0.96/src/spotRiver/data/synth/__init__.py
+-rw-r--r--   0 bartz      (501) staff       (20)     2442 2023-02-20 15:46:37.000000 spotRiver-0.0.96/src/spotRiver/data/synth/sea.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 12:28:50.528064 spotRiver-0.0.96/src/spotRiver/drift/
+-rw-r--r--   0 bartz      (501) staff       (20)      767 2023-02-20 15:46:37.000000 spotRiver-0.0.96/src/spotRiver/drift/drift_generator.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 12:28:50.528467 spotRiver-0.0.96/src/spotRiver/evaluation/
+-rw-r--r--   0 bartz      (501) staff       (20)    30967 2023-07-23 10:56:04.000000 spotRiver-0.0.96/src/spotRiver/evaluation/eval_bml.py
+-rw-r--r--   0 bartz      (501) staff       (20)     3958 2023-02-26 22:39:12.000000 spotRiver-0.0.96/src/spotRiver/evaluation/eval_nowcast.py
+-rw-r--r--   0 bartz      (501) staff       (20)     6752 2023-04-06 12:44:54.000000 spotRiver-0.0.96/src/spotRiver/evaluation/eval_oml.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 12:28:50.528713 spotRiver-0.0.96/src/spotRiver/fun/
+-rw-r--r--   0 bartz      (501) staff       (20)     5391 2023-06-10 18:01:21.000000 spotRiver-0.0.96/src/spotRiver/fun/hyperriver.py
+-rw-r--r--   0 bartz      (501) staff       (20)    32460 2023-04-22 19:31:59.000000 spotRiver-0.0.96/src/spotRiver/fun/hyperriver_old.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 12:28:50.528864 spotRiver-0.0.96/src/spotRiver/plot/
+-rw-r--r--   0 bartz      (501) staff       (20)     1340 2023-03-11 14:52:45.000000 spotRiver-0.0.96/src/spotRiver/plot/stats.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 12:28:50.528990 spotRiver-0.0.96/src/spotRiver/preprocess/
+-rw-r--r--   0 bartz      (501) staff       (20)     2488 2023-03-07 16:50:39.000000 spotRiver-0.0.96/src/spotRiver/preprocess/impute.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 12:28:50.529234 spotRiver-0.0.96/src/spotRiver/utils/
+-rw-r--r--   0 bartz      (501) staff       (20)     2284 2023-07-06 19:04:13.000000 spotRiver-0.0.96/src/spotRiver/utils/data_conversion.py
+-rw-r--r--   0 bartz      (501) staff       (20)     5549 2023-04-13 20:07:21.000000 spotRiver-0.0.96/src/spotRiver/utils/features.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 12:28:50.525547 spotRiver-0.0.96/src/spotRiver.egg-info/
+-rw-r--r--   0 bartz      (501) staff       (20)     3383 2023-07-23 12:28:50.000000 spotRiver-0.0.96/src/spotRiver.egg-info/PKG-INFO
+-rw-r--r--   0 bartz      (501) staff       (20)     1025 2023-07-23 12:28:50.000000 spotRiver-0.0.96/src/spotRiver.egg-info/SOURCES.txt
+-rw-r--r--   0 bartz      (501) staff       (20)        1 2023-07-23 12:28:50.000000 spotRiver-0.0.96/src/spotRiver.egg-info/dependency_links.txt
+-rw-r--r--   0 bartz      (501) staff       (20)      227 2023-07-23 12:28:50.000000 spotRiver-0.0.96/src/spotRiver.egg-info/requires.txt
+-rw-r--r--   0 bartz      (501) staff       (20)       10 2023-07-23 12:28:50.000000 spotRiver-0.0.96/src/spotRiver.egg-info/top_level.txt
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 12:28:50.529359 spotRiver-0.0.96/test/
+-rw-r--r--   0 bartz      (501) staff       (20)      510 2023-02-25 09:55:05.000000 spotRiver-0.0.96/test/test_features.py
```

### Comparing `spotRiver-0.0.95/LICENSE` & `spotRiver-0.0.96/LICENSE`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.95/PKG-INFO` & `spotRiver-0.0.96/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: spotRiver
-Version: 0.0.95
+Version: 0.0.96
 Summary: spotRiver - Sequential Parameter Optimization Interface to River
 Author-email: "T. Bartz-Beielstein" <tbb@bartzundbartz.de>
 Project-URL: Homepage, https://www.spotseven.de
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.10
```

### Comparing `spotRiver-0.0.95/README.md` & `spotRiver-0.0.96/README.md`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.95/pyproject.toml` & `spotRiver-0.0.96/pyproject.toml`

 * *Files 12% similar despite different names*

```diff
@@ -5,32 +5,50 @@
             "numpy",
             "scikit-learn",
             "matplotlib"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "spotRiver"
-version = "0.0.95"
+version = "0.0.96"
 authors = [
   { name="T. Bartz-Beielstein", email="tbb@bartzundbartz.de" }
 ]
 description = "spotRiver - Sequential Parameter Optimization Interface to River"
 readme = "README.md"
 requires-python = ">=3.10"
 classifiers = [
   "Programming Language :: Python :: 3.10",
   "Programming Language :: Python :: 3.11",
   "Operating System :: OS Independent",
 ]
 # PEP 621 dependencies declaration
 # adapt to your dependencies manager
 dependencies = [
-  "mkdocstrings-python"
+  "importlib",
+  "lightning>=2.0.0rc0",
+  "matplotlib",
+  "numpy",
+  "nbformat",
+  "mkdocstrings-python",
+  "pandas",
+  "plotly",
+  "pytorch-lightning>=1.4",
+  "river",
+  "scikit-learn",
+  "scipy",
+  "spotPython",
+  "seaborn",
+  "tabulate",
+  "tensorboard",
+  "torch",
+  "torch-tb-profiler",
+  "torchmetrics",
+  "torchvision"
 ]
-
 [project.urls]
 "Homepage" = "https://www.spotseven.de"
 
 [tool.setuptools]
 # ...
 # By default, include-package-data is true in pyproject.toml, so you do
 # NOT have to specify this line.
```

### Comparing `spotRiver-0.0.95/src/spotRiver/data/airline-passengers.csv` & `spotRiver-0.0.96/src/spotRiver/data/airline-passengers.csv`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.95/src/spotRiver/data/airline_passengers.py` & `spotRiver-0.0.96/src/spotRiver/data/airline_passengers.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.95/src/spotRiver/data/base.py` & `spotRiver-0.0.96/src/spotRiver/data/base.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.95/src/spotRiver/data/bike_sharing.py` & `spotRiver-0.0.96/src/spotRiver/data/bike_sharing.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.95/src/spotRiver/data/opm.py` & `spotRiver-0.0.96/src/spotRiver/data/opm.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.95/src/spotRiver/data/river_hyper_dict.json` & `spotRiver-0.0.96/src/spotRiver/data/river_hyper_dict.json`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.95/src/spotRiver/data/synth/sea.py` & `spotRiver-0.0.96/src/spotRiver/data/synth/sea.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.95/src/spotRiver/drift/drift_generator.py` & `spotRiver-0.0.96/src/spotRiver/drift/drift_generator.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.95/src/spotRiver/evaluation/eval_bml.py` & `spotRiver-0.0.96/src/spotRiver/evaluation/eval_bml.py`

 * *Files 10% similar despite different names*

```diff
@@ -4,14 +4,15 @@
 import pandas as pd
 from river import stream as river_stream
 from typing import Optional
 from dataclasses import dataclass
 from typing import Tuple, Generator
 import matplotlib.pyplot as plt
 import copy
+from typing import Optional, Any
 
 
 class ResourceMonitorError(Exception):
     pass
 
 
 @dataclass
@@ -31,40 +32,30 @@
 
     def __repr__(self):
         return str(self)
 
 
 class ResourceMonitor:
     """
-    A class to monitor resource usage such as memory and time.
-
-    Attributes
-    ----------
-    name : str
-        The name of the resource monitor.
-    r_time : float
-        The time taken for the monitored code to execute in seconds.
-    memory : float
-        The peak memory usage during the execution of the monitored code in MB.
-
-    Methods
-    -------
-    result():
-        Returns a ResourceUsage object containing the name, time and memory usage of the monitored code.
-
-    Example
-    -------
-        >>> rm = ResourceMonitor()
-            with rm:
-                x = 10 ** 6
-            print(rm.result())
-            # Output:
-            #   Resource usage for None:
-            #   Time [s]: 2.917e-06
-            #   Memory [b]: 8.7738037109375e-05
+    A context manager for monitoring resource usage.
+    Args:
+        name (str, optional): A description of the resource usage. Defaults to None.
+    Raises:
+        (ResourceMonitorError): If the resource monitor is already tracing memory usage.
+    Returns:
+        (ResourceMonitor): A ResourceMonitor object.
+    Examples:
+        >>> import time
+        >>> from spotRiver.evaluation.eval_bml import ResourceMonitor
+        >>> with ResourceMonitor() as rm:
+        ...     time.sleep(1)
+        ...     print(rm.result())
+        Resource usage:
+            Time [s]: 1.000000001
+            Memory [b]: 0.0
     """
 
     def __init__(self, name: Optional[str] = None):
         self.name = name
         self.r_time = None
         self.memory = None
         self.current_memory = None
@@ -81,52 +72,65 @@
     def __exit__(self, type, value, traceback):
         self.r_time = (time.perf_counter_ns() - self._start) / 1.0e9
         _, peak = tracemalloc.get_traced_memory()
         self.memory = peak / (1024 * 1024)
         tracemalloc.stop()
 
     def result(self):
+        """ Returns a ResourceUsage object with the results of the resource monitor.
+        Raises:
+            (ResourceMonitorError):
+                If the resource monitor has not been used yet.
+        Returns:
+            (ResourceUsage):
+                A ResourceUsage object with the results of the resource monitor.
+        Examples:
+        >>> from time import sleep
+        >>> from spotRiver.evaluation.eval_bml import ResourceMonitor
+        >>> with ResourceMonitor() as rm:
+        >>> sleep(1)
+        >>> print(rm.result())
+        Resource usage:
+            Time [s]: 1.000000001
+            Memory [b]: 0.0
+        """
         if self.r_time is None or self.memory is None:
             raise ResourceMonitorError("No resources monitored yet.")
         return ResourceUsage(name=self.name, r_time=self.r_time, memory=self.memory)
 
 
-def evaluate_model(y_true: np.ndarray, y_pred: np.ndarray, memory: float, r_time: float, metric) -> dict:
+def evaluate_model(y_true: np.ndarray,
+                   y_pred: np.ndarray,
+                   memory: float,
+                   r_time: float,
+                   metric) -> dict:
     """
-    Evaluate a model's performance based on its predictions and ground truth values.
+    Evaluate a machine learning model on a test dataset.
 
-    Parameters
-    ----------
-    y_true: Ground truth values as a numpy array.
-    y_pred: Predicted values as a numpy array.
-    memory: Memory usage in MB.
-    r_time: Computation time in seconds.
-    metric: A function that takes in two arguments (y_true and y_pred) and returns a score.
-
-    Returns
-    -------
-    A dictionary containing the evaluation results including the metric score, memory usage and computation time.
-
-    Example
-    ------
-    >>> from sklearn.metrics import mean_squared_error
-        import numpy as np
-        y_true = np.array([1.0, 2.0, 3.0])
-        y_pred = np.array([1.1, 2.1, 2.9])
-        memory = 100
-        r_time = 0.5
-        result = evaluate_model(y_true=y_true,
-                                y_pred=y_pred,
-                                memory=memory,
-                                r_time=r_time,
-                                metric=mean_squared_error)
-        print(result)
+    This function evaluates a machine learning model on a test dataset using a given evaluation metric.
+    The evaluation results are returned as a dictionary.
 
-        # Output:
-        # {'Metric': 0.00666666666666671, 'Memory (MB)': 100, 'CompTime (s)': 0.5}
+    Args:
+        y_true (np.ndarray): A numpy array containing the true values.
+        y_pred (np.ndarray): A numpy array containing the predicted values.
+        memory (float): The memory usage of the model.
+        r_time (float): The computation time of the model.
+        metric (object): An evaluation metric object that has an `evaluate` method.
+            This metric will be used to evaluate the model's performance on the test dataset.
+    Returns:
+        dict: A dictionary containing the evaluation results.
+    Examples:
+        >>> from sklearn.metrics import accuracy_score
+        >>> y_true = np.array([0, 1, 0, 1])
+        >>> y_pred = np.array([0, 1, 1, 1])
+        >>> memory = 0.0
+        >>> r_time = 0.0
+        >>> metric = accuracy_score
+        >>> evaluate_model(y_true, y_pred, memory, r_time, metric)
+        {'Metric': 0.75, 'Memory (MB)': 0.0, 'CompTime (s)': 0.0}
     """
     if len(y_true) != len(y_pred):
         raise ValueError("y_true and y_pred must have the same size")
     if (len(y_true) == 0) or (len(y_pred) == 0):
         res_dict = {
             "Metric": None,
             "Memory (MB)": memory,
@@ -146,73 +150,42 @@
     horizon: int,
     include_remainder: bool = True,
     metric: object = None,
 ) -> tuple:
     """
     Evaluate a machine learning model on a rolling horizon basis.
 
-    This function evaluates a machine learning model on a test dataset by making
-    predictions on batches of size `horizon` from the test dataset. The model is
-    first fit on the training dataset. The evaluation results are returned as a
-    dataframe along with a dataframe containing the true values, predictions and
-    differences for each observation in the test dataset.
-
-    Parameters
-    ----------
-    model : object
-        A machine learning model object that has `fit` and `predict` methods.
-
-    train : pd.DataFrame
-        A pandas DataFrame containing the training data. The target column should be included in this dataframe.
-
-     test : pd.DataFrame
-         A pandas DataFrame containing the test data. The target column should be included in this dataframe.
-
-     target_column : str
-         The name of the target column in the train and test dataframes.
-
-     horizon : int
-         The size of each batch from the test dataframe to make predictions on.
-
-     include_remainder : bool, optional (default=True)
-         Whether to include remainder rows from the test dataframe when making predictions.
-         If False, remainder rows will be removed before making predictions.
-
-     metric : object
-         An evaluation metric object that has an `evaluate` method.
-         This metric will be used to evaluate the model's performance on each batch from the test dataframe.
-
-     Returns
-     -------
-     tuple of pd.DataFrame
-         A tuple containing two pandas DataFrames. The first dataframe contains evaluation results for
-         each batch from the test dataframe along with initial resource usage from fitting the model
-         on the training data. The second dataframe contains true values, predictions and differences
-         for each observation in the test dataset.
-
-     Example
-     -------
-        >>> from sklearn.datasets import make_classification
-            from sklearn.tree import DecisionTreeClassifier
-            from sklearn.metrics import accuracy_score
-            # Generate synthetic data for classification
-            X_train, y_train = make_classification(n_samples=1000)
-            X_test, y_test = make_classification(n_samples=1000)
-            # Convert to DataFrames and add target column
-            train_df = pd.DataFrame(X_train)
-            train_df['target'] = y_train
-            test_df = pd.DataFrame(X_test)
-            test_df['target'] = y_test
-            # Initialize Decision Tree Classifier and evaluate using eval_bml_horizon function
-            dtc = DecisionTreeClassifier()
-            eval_results_df, true_preds_diffs_df = eval_bml_horizon(dtc, train_df,test_df,'target', 10, True, accuracy_score)
-            # Print first 5 rows of evaluation results DataFrame
-            print(eval_results_df.head())
-            # Print first 5 rows of true values/predictions/differences DataFrame
-            print(true_preds_diffs_df.head())
+    This function evaluates a machine learning model on a rolling horizon basis.
+    The model is trained on the training data and then evaluated on the test data
+    using a given evaluation metric. The evaluation results are returned as a tuple
+    of two data frames. The first one contains evaluation metrics for each window.
+    The second one contains the true and predicted values for each observation in the test set.
+
+    Args:
+        model (object): The model to be evaluated.
+        train (pd.DataFrame): The training data set.
+        test (pd.DataFrame): The testing data set.
+        target_column (str): The name of the column containing the target variable.
+        horizon (int, optional): The number of steps ahead to forecast.
+        include_remainder (bool): Whether to include the remainder of the test dataframe if its length is not divisible by the horizon. Defaults to True.
+        metric (object): An evaluation metric object that has an `evaluate` method. This metric will be used to evaluate the model's performance on the test dataset.
+    Returns:
+        tuple: A tuple of two data frames. The first one contains evaluation metrics for each window. The second one contains the true and predicted values for each observation in the test set.
+    Examples:
+        >>> from sklearn.linear_model import LinearRegression
+        >>> model = LinearRegression()
+        >>> train = pd.DataFrame({"x": [1, 2, 3], "y": [2, 4, 6]})
+        >>> test = pd.DataFrame({"x": [4, 5], "y": [8, 10]})
+        >>> df_eval, df_true = eval_bml_horizon(model, train, test, "y", horizon=1)
+        >>> print(df_eval)
+              Metric  Memory (MB)  CompTime (s)
+        0  0.000000          0.0           0.0
+        1  0.000000          0.0           0.0
+        ...        ...          ...           ...
+
     """
     # Check if metric is None or null and raise ValueError if it is
     if metric is None:
         raise ValueError("The 'metric' parameter must not be None or null.")
     # Reset index of train and test dataframes
     train = train.reset_index(drop=True)
     test = test.reset_index(drop=True)
@@ -265,14 +238,45 @@
     train: pd.DataFrame,
     test: pd.DataFrame,
     target_column: str,
     horizon: int,
     include_remainder: bool = True,
     metric: object = None,
 ) -> tuple:
+    """Evaluate a machine learning model on a rolling landmark basis.
+
+    This function evaluates a machine learning model on a rolling landmark basis.
+    The model is trained on the training data and then evaluated on the test data
+    using a given evaluation metric. The evaluation results are returned as a tuple
+    of two data frames. The first one contains evaluation metrics for each window.
+    The second one contains the true and predicted values for each observation in the test set.
+
+    Args:
+        model (object): The model to be evaluated.
+        train (pd.DataFrame): The training data set.
+        test (pd.DataFrame): The testing data set.
+        target_column (str): The name of the column containing the target variable.
+        horizon (int, optional): The number of steps ahead to forecast.
+        include_remainder (bool): Whether to include the remainder of the test dataframe if its length is not divisible by the horizon. Defaults to True.
+        metric (object): An evaluation metric object that has an `evaluate` method. This metric will be used to evaluate the model's performance on the test dataset.
+    Returns:
+        tuple: A tuple of two data frames. The first one contains evaluation metrics for each window. The second one contains the true and predicted values for each observation in the test set.
+    Examples:
+        >>> from sklearn.linear_model import LinearRegression
+        >>> model = LinearRegression()
+        >>> train = pd.DataFrame({"x": [1, 2, 3], "y": [2, 4, 6]})
+        >>> test = pd.DataFrame({"x": [4, 5], "y": [8, 10]})
+        >>> df_eval, df_true = eval_bml_landmark(model, train, test, "y", horizon=1)
+        >>> print(df_eval)
+                Metric  Memory (MB)  CompTime (s)
+        0  0.000000          0.0           0.0
+        1  0.000000          0.0           0.0
+        ...        ...          ...           ...
+
+    """
     train = train.reset_index(drop=True)
     test = test.reset_index(drop=True)
     series_preds = pd.Series(dtype=float)
     series_diffs = pd.Series(dtype=float)
     rm = ResourceMonitor()
     with rm:
         model.fit(train.loc[:, train.columns != target_column], train[target_column])
@@ -286,15 +290,14 @@
     # Landmark Evaluation
     for i, new_df in enumerate(gen_sliding_window(test, horizon)):
         train = pd.concat([train, new_df], ignore_index=True)
         rm = ResourceMonitor()
         with rm:
             preds = pd.Series(model.predict(new_df.loc[:, new_df.columns != target_column]))
             model.fit(train.loc[:, train.columns != target_column], train[target_column])
-
         diffs = new_df[target_column].values - preds
         df_eval.loc[i + 1] = pd.Series(
             evaluate_model(
                 y_true=new_df[target_column],
                 y_pred=preds,
                 memory=rm.memory,
                 r_time=rm.r_time,
@@ -305,28 +308,32 @@
         series_diffs = pd.concat([series_diffs, diffs], ignore_index=True)
     df_true = pd.DataFrame(test[target_column])
     df_true["Prediction"] = series_preds
     df_true["Difference"] = series_diffs
     return df_eval, df_true
 
 
-def gen_sliding_window(
-    df: pd.DataFrame, horizon: int, include_remainder: bool = True
-) -> Generator[pd.DataFrame, None, None]:
+def gen_sliding_window(df: pd.DataFrame,
+                       horizon: int,
+                       include_remainder: bool = True
+                       ) -> Generator[pd.DataFrame, None, None]:
     """Generates sliding windows of a given size from a DataFrame.
 
     Args:
         df (pd.DataFrame): The input DataFrame.
         horizon (int): The size of the sliding window.
-        include_remainder (bool): Whether to include the remainder of the DataFrame if its length is not divisible by the horizon. Defaults to False.
+        include_remainder (bool):
+            Whether to include the remainder of the DataFrame
+            if its length is not divisible by the horizon. Defaults to False.
 
     Yields:
-        pd.DataFrame: A sliding window of the input DataFrame.
+        (pd.DataFrame):
+            A sliding window of the input DataFrame.
 
-    Example:
+    Examples:
         >>> df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})
         >>> for window in gen_sliding_window(df, 2):
         ...     print(window)
            A  B
         0  1  4
         1  2  5
            A  B
@@ -363,15 +370,15 @@
         target_column (str): The name of the column containing the target variable.
         horizon (int, optional): The number of steps ahead to forecast.
 
     Returns:
         tuple: A tuple of two data frames. The first one contains evaluation metrics for each window.
         The second one contains the true and predicted values for each observation in the test set.
 
-    Example:
+    Examples:
         >>> from sklearn.linear_model import LinearRegression
         >>> model = LinearRegression()
         >>> train = pd.DataFrame({"x": [1, 2, 3], "y": [2, 4, 6]})
         >>> test = pd.DataFrame({"x": [4, 5], "y": [8, 10]})
         >>> df_eval, df_true = eval_bml_window(model, train, test, "y", horizon=1)
         >>> print(df_eval)
     """
@@ -391,15 +398,14 @@
         if rem > 0:
             test = test[:-rem]
     for i, (w_train, w_test) in enumerate(gen_horizon_shifted_window(df_all, len(train), horizon)):
         rm = ResourceMonitor()
         with rm:
             model.fit(w_train.loc[:, w_train.columns != target_column], w_train[target_column])
             preds = pd.Series(model.predict(w_test.loc[:, w_test.columns != target_column]))
-
         diffs = w_test[target_column].values - preds
         df_eval.loc[i + 1] = pd.Series(
             evaluate_model(
                 y_true=w_test[target_column],
                 y_pred=preds,
                 memory=rm.memory,
                 r_time=rm.r_time,
@@ -412,15 +418,17 @@
 
     df_true = pd.DataFrame(test[target_column])
     df_true["Prediction"] = series_preds
     df_true["Difference"] = series_diffs
     return df_eval, df_true
 
 
-def gen_horizon_shifted_window(df, window_size, horizon):
+def gen_horizon_shifted_window(df: pd.DataFrame,
+                               window_size: int,
+                               horizon: int):
     i = 0
     while True:
         train_window = df[i * horizon : i * horizon + window_size]
         test_window = df[i * horizon + window_size : (i + 1) * horizon + window_size]
         if len(test_window) == 0:
             break
         elif len(test_window) < horizon:
@@ -437,57 +445,44 @@
     target_column: str,
     horizon: int,
     include_remainder: bool = True,
     metric: object = None,
     oml_grace_period: int = None,
 ) -> Tuple[pd.DataFrame, pd.DataFrame]:
     """
-    Evaluate an online machine learning model.
+    Evaluate a machine learning model on a rolling horizon basis.
+
+    This function evaluates a machine learning model on a rolling horizon basis.
+    The model is trained on the training data and then evaluated on the test data
+    using a given evaluation metric. The evaluation results are returned as a tuple
+    of two data frames. The first one contains evaluation metrics for each window.
+    The second one contains the true and predicted values for each observation in the test set.
 
-    Parameters
-    ----------
-    model : object
-        The online machine learning model to be evaluated.
-    train : pd.DataFrame
-        The training data for the model.
-    test : pd.DataFrame
-        The testing data for the model.
-    target_column : str
-        The name of the column that contains the target variable.
-    horizon : int, optional
-        The number of rows to use for each landmark evaluation.
-    metric: object
-        Metric, e.g., from sklearn.metrics: mean_squared_error
-    oml_grace_period: int, optional
-        (Short) period used for training the OML before evaluation starts. Can be zero.
-        If set to None, horizon will be used.
-
-    Returns
-    -------
-    tuple of pd.DataFrame
-        The first element is a dataframe with evaluation metrics (RMSE, MAE, ACC, memory usage and time elapsed) for each iteration.
-        The second element is a dataframe with the true values, predictions and differences for the test data.
-
-    Examples
-    -------
-    >>> import pandas as pd
-        import numpy as np
-        from river import linear_model
-        from river import preprocessing
-        from sklearn.metrics import mean_squared_error
-        model = preprocessing.StandardScaler() | linear_model.LinearRegression()
-        dataset = datasets.TrumpApproval()
-        train = pd.DataFrame(dataset.take(100))
-        test = pd.DataFrame(dataset.take(100))
-        target_column = "Approve"
-        horizon = 10
-        metric = mean_squared_error
-        df_eval, df_preds = eval_oml_horizon(model, train, test, target_column, horizon, oml_grace_period, metric=metric)
-        print(df_eval)
-        print(df_preds)
+    Args:
+        model (object): The model to be evaluated.
+        train (pd.DataFrame): The training data set.
+        test (pd.DataFrame): The testing data set.
+        target_column (str): The name of the column containing the target variable.
+        horizon (int, optional): The number of steps ahead to forecast.
+        include_remainder (bool): Whether to include the remainder of the test dataframe if its length is not divisible by the horizon. Defaults to True.
+        metric (object): An evaluation metric object that has an `evaluate` method. This metric will be used to evaluate the model's performance on the test dataset.
+        oml_grace_period (int, optional): The number of observations to use for initial training. Defaults to None, in which case the horizon is used.
+    Returns:
+        tuple: A tuple of two data frames. The first one contains evaluation metrics for each window. The second one contains the true and predicted values for each observation in the test set.
+    Examples:
+        >>> from sklearn.linear_model import LinearRegression
+        >>> model = LinearRegression()
+        >>> train = pd.DataFrame({"x": [1, 2, 3], "y": [2, 4, 6]})
+        >>> test = pd.DataFrame({"x": [4, 5], "y": [8, 10]})
+        >>> df_eval, df_true = eval_oml_horizon(model, train, test, "y", horizon=1)
+        >>> print(df_eval)
+                Metric  Memory (MB)  CompTime (s)
+        0  0.000000          0.0           0.0
+        1  0.000000          0.0           0.0
+        ...        ...          ...           ...
     """
     # Check if metric is None or null and raise ValueError if it is
     if metric is None:
         raise ValueError("The 'metric' parameter must not be None or null.")
     if oml_grace_period is None:
         oml_grace_period = horizon
     train = train.reset_index(drop=True)
@@ -508,18 +503,19 @@
     rm = ResourceMonitor()
     with rm:
         for xi, yi in river_stream.iter_pandas(train_X, train_y):
             # The following line returns y_pred, which is not used, therefore set to "_":
             _ = model.predict_one(xi)
             # metric = metric.update(yi, y_pred)
             model = model.learn_one(xi, yi)
+    # TODO: Add error handling
+    # Return res_dict = {"Metric": score, "Memory (MB)": memory, "CompTime (s)": r_time}
     df_eval = pd.DataFrame.from_dict(
         [evaluate_model(y_true=np.array([]), y_pred=np.array([]), memory=rm.memory, r_time=rm.r_time, metric=metric)]
     )
-
     # Test Data Evaluation
     for i, new_df in enumerate(gen_sliding_window(test, horizon)):
         preds = []
         test_X = new_df.loc[:, new_df.columns != target_column]
         test_y = new_df[target_column]
         rm = ResourceMonitor()
         with rm:
@@ -554,80 +550,43 @@
     cumulative=True,
     grid=True,
     figsize=None,
     metric=None,
     filename=None,
     **kwargs,
 ) -> None:
-    """Plot metrics for benchmarking machine learning models.
+    """Plot evaluation metrics for machine learning models.
+
+    This function plots the evaluation metrics for different machine learning models
+    on a given dataset. The function takes a list of pandas dataframes as input,
+    each containing the evaluation metrics for one model. The function also takes
+    an optional list of labels for each model and boolean flags to indicate whether
+    to use logarithmic scales for the x-axis and y-axis.
+
+    Args:
+        df_eval (list[pd.DataFrame], optional): A list of pandas dataframes containing the evaluation metrics for each model. Each dataframe should have an index column with the dataset name and three columns with the label names: e.g., "Metric", "CompTime (s)" and "Memory (MB)". If None, no plot is generated. Default is None.
+        df_labels (list, optional): A list of strings containing the labels for each model. The length of this list should match the length of df_eval. If None, numeric indices are used as labels. Default is None.
+        log_x (bool, optional): A flag indicating whether to use logarithmic scale for the x-axis. If True, log scale is used. If False, linear scale is used. Default is False.
+        log_y (bool, optional): A flag indicating whether to use logarithmic scale for the y-axis. If True, log scale is used. If False, linear scale is used. Default is False.
+        cumulative (bool, optional): A flag indicating whether to plot cumulative metrics. If True, cumulative metrics are plotted. If False, non-cumulative metrics are plotted. Default is True.
+        grid (bool, optional): A flag indicating whether to plot a grid. If True, grid is shown. Default is True.
+        figsize (tuple, optional): The size of the figure. Default is None.
+        metric (object): An evaluation metric object that has an `evaluate` method. This metric will be used to evaluate the model's performance on the test dataset.
+        filename (str, optional): The name of the file to save the plot to. If None, the plot is not saved. Default is None.
+        **kwargs (Any): Additional keyword arguments to be passed to the plot function.
 
-    This function plots three metrics: mean absolute error (MAE)/ Accuracy, memory usage (MB),
-    and computation time (s) for different machine learning models on a given dataset.
-    The function takes a list of pandas dataframes as input, each containing the metrics
-    for one model. The function also takes an optional list of labels for each model
-    and boolean flags to indicate whether to use logarithmic scales for the x-axis
-    and y-axis.
-
-    Parameters
-    ----------
-    df_eval : list[pd.DataFrame], optional
-        A list of pandas dataframes containing the metrics for each model.
-        Each dataframe should have an index column with the dataset name
-        and three columns with the metric names: "MAE"/"ACC", "Memory (MB)", "CompTime (s)".
-        If None, no plot is generated. Default is None.
-
-    df_labels : list, optional
-        A list of strings containing the labels for each model.
-        The length of this list should match the length of df_eval.
-        If None, numeric indices are used as labels. Default is None.
-
-    log_x : bool, optional
-        A flag indicating whether to use logarithmic scale for the x-axis.
-        If True, log scale is used. If False, linear scale is used. Default is False.
-
-    log_y : bool, optional
-        A flag indicating whether to use logarithmic scale for the y-axis.
-        If True, log scale is used. If False, linear scale is used. Default is False.
-
-    cumulative : bool, optional:
-        A flag indicating whether to plot the cumulative average error as it is done in
-        `plot_oml_iter_progressive()` and in `river`'s ` evaluate.iter_progressive_val_score()`
-        method. Time is shown as a cumulative sum (not averaged). Since memory is calculated
-        in a different way than in `river`'s ` evaluate.iter_progressive_val_score()`, the peak
-        memory from `_ , peak = tracemalloc.get_traced_memory()` is shown in a non-aggregated way.
-        Default is True.
-
-    grid: bool, optional
-        A flag indicating whether to plot a grid.
-        If True, grid is shown. Default is True.
-
-    figsize (tuple, optional): The size of the figure. Defaults to None, in which case
-            the default figure size `(10, 5)` is used.
-
-    filename: str, optional. Default: None.
-        If not None, the plot is saved to the specified file.
-
-    **kwargs : dict
-        Additional keyword arguments passed to plt.plot() function.
-
-    Returns
-    -------
-    None
-
-    Example
-    -------
-    >>> d1 = {'MAE': [0.1, 0.2], 'Memory (MB)': [10 , 20], 'CompTime (s)': [1 , 2]}
-        d2 = {'MAE': [0.3 , 0.4], 'Memory (MB)': [30 , 40], 'CompTime (s)': [3 , 4]}
-        # create dataframes from dictionaries
-        df_eval1 = pd.DataFrame(data=d1)
-        df_eval2 = pd.DataFrame(data=d2)
-        # create a list of dataframes
-        df_eval_list = [df_eval1 , df_eval2]
-        # plot evaluation metrics for each element of df_eval_list
-        plot_bml_oml_metrics(df_eval=df_eval_list)
+    Returns:
+        (NoneType): This function does not return anything.
+
+    Examples:
+        >>> from sklearn.metrics import accuracy_score
+        >>> from spotRiver.evaluation.eval_bml import plot_bml_oml_horizon_metrics
+        >>> df_eval = pd.DataFrame({"Metric": [0.5, 0.75, 0.9], "CompTime (s)": [0.1, 0.2, 0.3], "Memory (MB)": [0.1, 0.2, 0.3]})
+        >>> df_labels = ["Model 1", "Model 2", "Model 3"]
+        >>> plot_bml_oml_horizon_metrics(df_eval, df_labels, metric=accuracy_score)
     """
     if figsize is None:
         figsize = (10, 5)
     # Check if metric is None or null and raise ValueError if it is
     if metric is None:
         raise ValueError("The 'metric' parameter must not be None or null.")
     # Check if input dataframes are provided
@@ -679,76 +638,43 @@
     log_y=False,
     skip_first_n=0,
     grid=True,
     figsize: tuple = None,
     filename=None,
     **kwargs,
 ) -> None:
-    """Plot actual vs predicted values for machine learning models.
+    """ Plot actual vs predicted values for machine learning models.
+
+    This function plots the actual vs predicted values for different machine learning models
+    on a given dataset. The function takes a list of pandas dataframes as input,
+    each containing the actual and predicted values for one model. The function also takes
+    an optional list of labels for each model and boolean flags to indicate whether
+    to use logarithmic scales for the x-axis and y-axis.
+
+    Args:
+        df_true (list[pd.DataFrame], optional): A list of pandas dataframes containing the actual and predicted values for each model. Each dataframe should have an index column with the dataset name and two columns with the label names: e.g., "Actual" and "Prediction". If None, no plot is generated. Default is None.
+        df_labels (list, optional): A list of strings containing the labels for each model. The length of this list should match the length of df_true. If None, numeric indices are used as labels. Default is None.
+        target_column (str, optional): The name of the column containing the target variable. Default is "Actual".
+        log_x (bool, optional): A flag indicating whether to use logarithmic scale for the x-axis. If True, log scale is used. If False, linear scale is used. Default is False.
+        log_y (bool, optional): A flag indicating whether to use logarithmic scale for the y-axis. If True, log scale is used. If False, linear scale is used. Default is False.
+        skip_first_n (int, optional): The number of rows to skip from the beginning of the dataframes. Default is 0.
+        grid (bool, optional): A flag indicating whether to plot a grid. If True, grid is shown. Default is True.
+        figsize (tuple, optional): The size of the figure. Default is None.
+        filename (str, optional): The name of the file to save the plot to. If None, the plot is not saved. Default is None.
+        **kwargs (Any): Additional keyword arguments to be passed to the plot function.
+
+    Returns:
+        (NoneType): This function does not return anything.
 
-    This function plots the actual values of a target variable (e.g., vibration)
-    against the predicted values from different machine learning models on
-    a given dataset. The function takes a list of pandas dataframes as input,
-    each containing the actual and predicted values for one model. The function
-    also takes an optional list of labels for each model and boolean flags
-    to indicate whether to use logarithmic scales for the x-axis and y-axis.
-
-    Parameters
-    ----------
-    df_true : list[pd.DataFrame], optional
-        A list of pandas dataframes containing the actual and predicted values
-        for each model. Each dataframe should have an index column with the
-        dataset name and two columns with the label names: e.g., "Vibration"
-        and "Prediction". If None, no plot is generated. Default is None.
-
-    df_labels : list, optional
-        A list of strings containing the labels for each model.
-        The length of this list should match the length of df_eval.
-        If None, numeric indices are used as labels. Default is None.
-
-    target_column : optional
-        String containing the target column.
-        Default is "Actual".
-
-    log_x : bool, optional
-        A flag indicating whether to use logarithmic scale for the x-axis.
-        If True, log scale is used. If False, linear scale is used. Default is False.
-
-    log_y : bool, optional
-        A flag indicating whether to use logarithmic scale for the y-axis.
-        If True, log scale is used. If False, linear scale is used. Default is False.
-
-    skip_first_n: int, optional
-        Skip the first n entries in the plot.
-
-    grid: bool, optional
-        A flag indicating whether to plot a grid.
-        If True, grid is shown. Default is True.
-
-    figsize (tuple, optional): The size of the figure in inches.
-            Defaults to None, in which case
-            the default figure size `(10, 5)` is used.
-
-    filename: str, optional. Default: None
-        If not None, save the plot to a file.
-
-    **kwargs : dict
-        Additional keyword arguments passed to plt.plot() function.
-
-    Returns
-    -------
-    None
-
-    Example
-    -------
-    >>> d3 = {'Vibration': [0.5 , 0.6], 'Prediction': [0.7 , 0.8]}
-        # create dataframes from dictionaries
-        df_true = pd.DataFrame(data=d3)
-        # plot actual vs predicted values from df_true
-        plot_bml_oml_horizon_predictions(df_true=df_true)
+    Examples:
+        >>> from sklearn.metrics import accuracy_score
+        >>> from spotRiver.evaluation.eval_bml import plot_bml_oml_horizon_predictions
+        >>> df_true = pd.DataFrame({"Actual": [0.5, 0.75, 0.9], "Prediction": [0.1, 0.2, 0.3]})
+        >>> df_labels = ["Model 1", "Model 2", "Model 3"]
+        >>> plot_bml_oml_horizon_predictions(df_true, df_labels, target_column="Actual")
 
     """
     if figsize is None:
         figsize = (10, 5)
     if df_true is not None:
         df_plot = copy.deepcopy(df_true)
         if df_plot.__class__ != list:
```

### Comparing `spotRiver-0.0.95/src/spotRiver/evaluation/eval_nowcast.py` & `spotRiver-0.0.96/src/spotRiver/evaluation/eval_nowcast.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.95/src/spotRiver/evaluation/eval_oml.py` & `spotRiver-0.0.96/src/spotRiver/evaluation/eval_oml.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.95/src/spotRiver/fun/hyperriver.py` & `spotRiver-0.0.96/src/spotRiver/fun/hyperriver.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.95/src/spotRiver/fun/hyperriver_old.py` & `spotRiver-0.0.96/src/spotRiver/fun/hyperriver_old.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.95/src/spotRiver/plot/stats.py` & `spotRiver-0.0.96/src/spotRiver/plot/stats.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.95/src/spotRiver/preprocess/impute.py` & `spotRiver-0.0.96/src/spotRiver/preprocess/impute.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.95/src/spotRiver/utils/data_conversion.py` & `spotRiver-0.0.96/src/spotRiver/utils/data_conversion.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.95/src/spotRiver/utils/features.py` & `spotRiver-0.0.96/src/spotRiver/utils/features.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.95/src/spotRiver.egg-info/PKG-INFO` & `spotRiver-0.0.96/src/spotRiver.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: spotRiver
-Version: 0.0.95
+Version: 0.0.96
 Summary: spotRiver - Sequential Parameter Optimization Interface to River
 Author-email: "T. Bartz-Beielstein" <tbb@bartzundbartz.de>
 Project-URL: Homepage, https://www.spotseven.de
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.10
```

### Comparing `spotRiver-0.0.95/src/spotRiver.egg-info/SOURCES.txt` & `spotRiver-0.0.96/src/spotRiver.egg-info/SOURCES.txt`

 * *Files 2% similar despite different names*

```diff
@@ -3,14 +3,15 @@
 README.md
 pyproject.toml
 src/spotRiver.egg-info/PKG-INFO
 src/spotRiver.egg-info/SOURCES.txt
 src/spotRiver.egg-info/dependency_links.txt
 src/spotRiver.egg-info/requires.txt
 src/spotRiver.egg-info/top_level.txt
+src/spotRiver/data/UnivariateData.csv
 src/spotRiver/data/__init__.py
 src/spotRiver/data/airline-passengers.csv
 src/spotRiver/data/airline_passengers.py
 src/spotRiver/data/base.py
 src/spotRiver/data/bike_sharing.py
 src/spotRiver/data/generic.py
 src/spotRiver/data/opm.py
```

