# Comparing `tmp/spotRiver-0.0.97.tar.gz` & `tmp/spotRiver-0.0.98.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "spotRiver-0.0.97.tar", last modified: Sun Jul 23 17:53:34 2023, max compression
+gzip compressed data, was "spotRiver-0.0.98.tar", last modified: Sun Jul 23 18:04:19 2023, max compression
```

## Comparing `spotRiver-0.0.97.tar` & `spotRiver-0.0.98.tar`

### file list

```diff
@@ -1,47 +1,47 @@
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 17:53:34.927972 spotRiver-0.0.97/
--rw-r--r--   0 bartz      (501) staff       (20)     1520 2023-01-29 11:49:35.000000 spotRiver-0.0.97/LICENSE
--rw-r--r--   0 bartz      (501) staff       (20)      164 2023-03-22 20:43:16.000000 spotRiver-0.0.97/MANIFEST.in
--rw-r--r--   0 bartz      (501) staff       (20)     3383 2023-07-23 17:53:34.927856 spotRiver-0.0.97/PKG-INFO
--rw-r--r--   0 bartz      (501) staff       (20)     2912 2023-01-29 16:41:52.000000 spotRiver-0.0.97/README.md
--rw-r--r--   0 bartz      (501) staff       (20)     1347 2023-07-23 16:28:32.000000 spotRiver-0.0.97/pyproject.toml
--rw-r--r--   0 bartz      (501) staff       (20)       38 2023-07-23 17:53:34.928006 spotRiver-0.0.97/setup.cfg
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 17:53:34.922153 spotRiver-0.0.97/src/
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 17:53:34.922646 spotRiver-0.0.97/src/spotRiver/
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 17:53:34.926015 spotRiver-0.0.97/src/spotRiver/data/
--rw-r--r--   0 bartz      (501) staff       (20)  1993321 2023-07-23 12:15:18.000000 spotRiver-0.0.97/src/spotRiver/data/UnivariateData.csv
--rw-r--r--   0 bartz      (501) staff       (20)      413 2023-01-29 11:52:00.000000 spotRiver-0.0.97/src/spotRiver/data/__init__.py
--rw-r--r--   0 bartz      (501) staff       (20)     2182 2023-01-17 12:39:58.000000 spotRiver-0.0.97/src/spotRiver/data/airline-passengers.csv
--rw-r--r--   0 bartz      (501) staff       (20)     1925 2023-07-23 17:22:39.000000 spotRiver-0.0.97/src/spotRiver/data/airline_passengers.py
--rw-r--r--   0 bartz      (501) staff       (20)    13254 2023-07-23 17:38:31.000000 spotRiver-0.0.97/src/spotRiver/data/base.py
--rw-r--r--   0 bartz      (501) staff       (20)     1251 2023-07-23 17:40:53.000000 spotRiver-0.0.97/src/spotRiver/data/bike_sharing.py
--rw-r--r--   0 bartz      (501) staff       (20)     2806 2023-07-23 17:05:39.000000 spotRiver-0.0.97/src/spotRiver/data/generic.py
--rw-r--r--   0 bartz      (501) staff       (20)     7751 2023-03-07 16:50:39.000000 spotRiver-0.0.97/src/spotRiver/data/opm.py
--rw-r--r--   0 bartz      (501) staff       (20)    17554 2023-04-08 14:44:16.000000 spotRiver-0.0.97/src/spotRiver/data/river_hyper_dict.json
--rw-r--r--   0 bartz      (501) staff       (20)      329 2023-03-31 21:04:02.000000 spotRiver-0.0.97/src/spotRiver/data/river_hyper_dict.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 17:53:34.926259 spotRiver-0.0.97/src/spotRiver/data/synth/
--rw-r--r--   0 bartz      (501) staff       (20)      328 2023-01-18 17:25:51.000000 spotRiver-0.0.97/src/spotRiver/data/synth/__init__.py
--rw-r--r--   0 bartz      (501) staff       (20)     2427 2023-07-23 17:09:13.000000 spotRiver-0.0.97/src/spotRiver/data/synth/sea.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 17:53:34.926402 spotRiver-0.0.97/src/spotRiver/drift/
--rw-r--r--   0 bartz      (501) staff       (20)     1080 2023-07-23 16:42:10.000000 spotRiver-0.0.97/src/spotRiver/drift/drift_generator.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 17:53:34.926762 spotRiver-0.0.97/src/spotRiver/evaluation/
--rw-r--r--   0 bartz      (501) staff       (20)    30967 2023-07-23 10:56:04.000000 spotRiver-0.0.97/src/spotRiver/evaluation/eval_bml.py
--rw-r--r--   0 bartz      (501) staff       (20)     4018 2023-07-23 16:38:15.000000 spotRiver-0.0.97/src/spotRiver/evaluation/eval_nowcast.py
--rw-r--r--   0 bartz      (501) staff       (20)     9240 2023-07-23 16:49:02.000000 spotRiver-0.0.97/src/spotRiver/evaluation/eval_oml.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 17:53:34.927005 spotRiver-0.0.97/src/spotRiver/fun/
--rw-r--r--   0 bartz      (501) staff       (20)     9145 2023-07-23 17:52:18.000000 spotRiver-0.0.97/src/spotRiver/fun/hyperriver.py
--rw-r--r--   0 bartz      (501) staff       (20)    32460 2023-04-22 19:31:59.000000 spotRiver-0.0.97/src/spotRiver/fun/hyperriver_old.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 17:53:34.927144 spotRiver-0.0.97/src/spotRiver/plot/
--rw-r--r--   0 bartz      (501) staff       (20)     1521 2023-07-23 17:01:45.000000 spotRiver-0.0.97/src/spotRiver/plot/stats.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 17:53:34.927265 spotRiver-0.0.97/src/spotRiver/preprocess/
--rw-r--r--   0 bartz      (501) staff       (20)     2488 2023-03-07 16:50:39.000000 spotRiver-0.0.97/src/spotRiver/preprocess/impute.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 17:53:34.927517 spotRiver-0.0.97/src/spotRiver/utils/
--rw-r--r--   0 bartz      (501) staff       (20)     2289 2023-07-23 16:50:36.000000 spotRiver-0.0.97/src/spotRiver/utils/data_conversion.py
--rw-r--r--   0 bartz      (501) staff       (20)     6091 2023-07-23 16:57:32.000000 spotRiver-0.0.97/src/spotRiver/utils/features.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 17:53:34.923823 spotRiver-0.0.97/src/spotRiver.egg-info/
--rw-r--r--   0 bartz      (501) staff       (20)     3383 2023-07-23 17:53:34.000000 spotRiver-0.0.97/src/spotRiver.egg-info/PKG-INFO
--rw-r--r--   0 bartz      (501) staff       (20)     1025 2023-07-23 17:53:34.000000 spotRiver-0.0.97/src/spotRiver.egg-info/SOURCES.txt
--rw-r--r--   0 bartz      (501) staff       (20)        1 2023-07-23 17:53:34.000000 spotRiver-0.0.97/src/spotRiver.egg-info/dependency_links.txt
--rw-r--r--   0 bartz      (501) staff       (20)      227 2023-07-23 17:53:34.000000 spotRiver-0.0.97/src/spotRiver.egg-info/requires.txt
--rw-r--r--   0 bartz      (501) staff       (20)       10 2023-07-23 17:53:34.000000 spotRiver-0.0.97/src/spotRiver.egg-info/top_level.txt
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 17:53:34.927666 spotRiver-0.0.97/test/
--rw-r--r--   0 bartz      (501) staff       (20)      510 2023-02-25 09:55:05.000000 spotRiver-0.0.97/test/test_features.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 18:04:19.717479 spotRiver-0.0.98/
+-rw-r--r--   0 bartz      (501) staff       (20)     1520 2023-01-29 11:49:35.000000 spotRiver-0.0.98/LICENSE
+-rw-r--r--   0 bartz      (501) staff       (20)      164 2023-03-22 20:43:16.000000 spotRiver-0.0.98/MANIFEST.in
+-rw-r--r--   0 bartz      (501) staff       (20)     3383 2023-07-23 18:04:19.717341 spotRiver-0.0.98/PKG-INFO
+-rw-r--r--   0 bartz      (501) staff       (20)     2912 2023-01-29 16:41:52.000000 spotRiver-0.0.98/README.md
+-rw-r--r--   0 bartz      (501) staff       (20)     1347 2023-07-23 18:04:09.000000 spotRiver-0.0.98/pyproject.toml
+-rw-r--r--   0 bartz      (501) staff       (20)       38 2023-07-23 18:04:19.717524 spotRiver-0.0.98/setup.cfg
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 18:04:19.710917 spotRiver-0.0.98/src/
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 18:04:19.711442 spotRiver-0.0.98/src/spotRiver/
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 18:04:19.715272 spotRiver-0.0.98/src/spotRiver/data/
+-rw-r--r--   0 bartz      (501) staff       (20)  1993321 2023-07-23 12:15:18.000000 spotRiver-0.0.98/src/spotRiver/data/UnivariateData.csv
+-rw-r--r--   0 bartz      (501) staff       (20)      413 2023-01-29 11:52:00.000000 spotRiver-0.0.98/src/spotRiver/data/__init__.py
+-rw-r--r--   0 bartz      (501) staff       (20)     2182 2023-01-17 12:39:58.000000 spotRiver-0.0.98/src/spotRiver/data/airline-passengers.csv
+-rw-r--r--   0 bartz      (501) staff       (20)     1925 2023-07-23 17:22:39.000000 spotRiver-0.0.98/src/spotRiver/data/airline_passengers.py
+-rw-r--r--   0 bartz      (501) staff       (20)    13254 2023-07-23 17:38:31.000000 spotRiver-0.0.98/src/spotRiver/data/base.py
+-rw-r--r--   0 bartz      (501) staff       (20)     1251 2023-07-23 17:40:53.000000 spotRiver-0.0.98/src/spotRiver/data/bike_sharing.py
+-rw-r--r--   0 bartz      (501) staff       (20)     2806 2023-07-23 17:05:39.000000 spotRiver-0.0.98/src/spotRiver/data/generic.py
+-rw-r--r--   0 bartz      (501) staff       (20)     7751 2023-03-07 16:50:39.000000 spotRiver-0.0.98/src/spotRiver/data/opm.py
+-rw-r--r--   0 bartz      (501) staff       (20)    17554 2023-04-08 14:44:16.000000 spotRiver-0.0.98/src/spotRiver/data/river_hyper_dict.json
+-rw-r--r--   0 bartz      (501) staff       (20)      329 2023-03-31 21:04:02.000000 spotRiver-0.0.98/src/spotRiver/data/river_hyper_dict.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 18:04:19.715542 spotRiver-0.0.98/src/spotRiver/data/synth/
+-rw-r--r--   0 bartz      (501) staff       (20)      328 2023-01-18 17:25:51.000000 spotRiver-0.0.98/src/spotRiver/data/synth/__init__.py
+-rw-r--r--   0 bartz      (501) staff       (20)     2427 2023-07-23 17:09:13.000000 spotRiver-0.0.98/src/spotRiver/data/synth/sea.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 18:04:19.715682 spotRiver-0.0.98/src/spotRiver/drift/
+-rw-r--r--   0 bartz      (501) staff       (20)     1080 2023-07-23 16:42:10.000000 spotRiver-0.0.98/src/spotRiver/drift/drift_generator.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 18:04:19.716051 spotRiver-0.0.98/src/spotRiver/evaluation/
+-rw-r--r--   0 bartz      (501) staff       (20)    30967 2023-07-23 10:56:04.000000 spotRiver-0.0.98/src/spotRiver/evaluation/eval_bml.py
+-rw-r--r--   0 bartz      (501) staff       (20)     4018 2023-07-23 16:38:15.000000 spotRiver-0.0.98/src/spotRiver/evaluation/eval_nowcast.py
+-rw-r--r--   0 bartz      (501) staff       (20)     9240 2023-07-23 16:49:02.000000 spotRiver-0.0.98/src/spotRiver/evaluation/eval_oml.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 18:04:19.716398 spotRiver-0.0.98/src/spotRiver/fun/
+-rw-r--r--   0 bartz      (501) staff       (20)     9192 2023-07-23 18:03:14.000000 spotRiver-0.0.98/src/spotRiver/fun/hyperriver.py
+-rw-r--r--   0 bartz      (501) staff       (20)    32460 2023-04-22 19:31:59.000000 spotRiver-0.0.98/src/spotRiver/fun/hyperriver_old.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 18:04:19.716575 spotRiver-0.0.98/src/spotRiver/plot/
+-rw-r--r--   0 bartz      (501) staff       (20)     1521 2023-07-23 17:01:45.000000 spotRiver-0.0.98/src/spotRiver/plot/stats.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 18:04:19.716715 spotRiver-0.0.98/src/spotRiver/preprocess/
+-rw-r--r--   0 bartz      (501) staff       (20)     2488 2023-03-07 16:50:39.000000 spotRiver-0.0.98/src/spotRiver/preprocess/impute.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 18:04:19.716986 spotRiver-0.0.98/src/spotRiver/utils/
+-rw-r--r--   0 bartz      (501) staff       (20)     2289 2023-07-23 16:50:36.000000 spotRiver-0.0.98/src/spotRiver/utils/data_conversion.py
+-rw-r--r--   0 bartz      (501) staff       (20)     6091 2023-07-23 16:57:32.000000 spotRiver-0.0.98/src/spotRiver/utils/features.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 18:04:19.712728 spotRiver-0.0.98/src/spotRiver.egg-info/
+-rw-r--r--   0 bartz      (501) staff       (20)     3383 2023-07-23 18:04:19.000000 spotRiver-0.0.98/src/spotRiver.egg-info/PKG-INFO
+-rw-r--r--   0 bartz      (501) staff       (20)     1025 2023-07-23 18:04:19.000000 spotRiver-0.0.98/src/spotRiver.egg-info/SOURCES.txt
+-rw-r--r--   0 bartz      (501) staff       (20)        1 2023-07-23 18:04:19.000000 spotRiver-0.0.98/src/spotRiver.egg-info/dependency_links.txt
+-rw-r--r--   0 bartz      (501) staff       (20)      227 2023-07-23 18:04:19.000000 spotRiver-0.0.98/src/spotRiver.egg-info/requires.txt
+-rw-r--r--   0 bartz      (501) staff       (20)       10 2023-07-23 18:04:19.000000 spotRiver-0.0.98/src/spotRiver.egg-info/top_level.txt
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 18:04:19.717148 spotRiver-0.0.98/test/
+-rw-r--r--   0 bartz      (501) staff       (20)      510 2023-02-25 09:55:05.000000 spotRiver-0.0.98/test/test_features.py
```

### Comparing `spotRiver-0.0.97/LICENSE` & `spotRiver-0.0.98/LICENSE`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.97/PKG-INFO` & `spotRiver-0.0.98/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: spotRiver
-Version: 0.0.97
+Version: 0.0.98
 Summary: spotRiver - Sequential Parameter Optimization Interface to River
 Author-email: "T. Bartz-Beielstein" <tbb@bartzundbartz.de>
 Project-URL: Homepage, https://www.spotseven.de
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.10
```

### Comparing `spotRiver-0.0.97/README.md` & `spotRiver-0.0.98/README.md`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.97/pyproject.toml` & `spotRiver-0.0.98/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -5,15 +5,15 @@
             "numpy",
             "scikit-learn",
             "matplotlib"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "spotRiver"
-version = "0.0.97"
+version = "0.0.98"
 authors = [
   { name="T. Bartz-Beielstein", email="tbb@bartzundbartz.de" }
 ]
 description = "spotRiver - Sequential Parameter Optimization Interface to River"
 readme = "README.md"
 requires-python = ">=3.10"
 classifiers = [
```

### Comparing `spotRiver-0.0.97/src/spotRiver/data/UnivariateData.csv` & `spotRiver-0.0.98/src/spotRiver/data/UnivariateData.csv`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.97/src/spotRiver/data/airline-passengers.csv` & `spotRiver-0.0.98/src/spotRiver/data/airline-passengers.csv`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.97/src/spotRiver/data/airline_passengers.py` & `spotRiver-0.0.98/src/spotRiver/data/airline_passengers.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.97/src/spotRiver/data/base.py` & `spotRiver-0.0.98/src/spotRiver/data/base.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.97/src/spotRiver/data/bike_sharing.py` & `spotRiver-0.0.98/src/spotRiver/data/bike_sharing.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.97/src/spotRiver/data/generic.py` & `spotRiver-0.0.98/src/spotRiver/data/generic.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.97/src/spotRiver/data/opm.py` & `spotRiver-0.0.98/src/spotRiver/data/opm.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.97/src/spotRiver/data/river_hyper_dict.json` & `spotRiver-0.0.98/src/spotRiver/data/river_hyper_dict.json`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.97/src/spotRiver/data/synth/sea.py` & `spotRiver-0.0.98/src/spotRiver/data/synth/sea.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.97/src/spotRiver/drift/drift_generator.py` & `spotRiver-0.0.98/src/spotRiver/drift/drift_generator.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.97/src/spotRiver/evaluation/eval_bml.py` & `spotRiver-0.0.98/src/spotRiver/evaluation/eval_bml.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.97/src/spotRiver/evaluation/eval_nowcast.py` & `spotRiver-0.0.98/src/spotRiver/evaluation/eval_nowcast.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.97/src/spotRiver/evaluation/eval_oml.py` & `spotRiver-0.0.98/src/spotRiver/evaluation/eval_oml.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.97/src/spotRiver/fun/hyperriver.py` & `spotRiver-0.0.98/src/spotRiver/fun/hyperriver.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from numpy.random import default_rng
 import numpy as np
 from numpy import array
 from river import compose
-
+from typing import Optional, Dict, Any, Tuple
 from spotPython.hyperparameters.values import assign_values
 from spotPython.hyperparameters.values import (
     generate_one_config_from_var_dict,
 )
 from spotPython.utils.eda import generate_config_id
 from spotRiver.evaluation.eval_bml import eval_oml_horizon
 
@@ -129,15 +129,15 @@
                 - metric_sklearn (str): The metric to be used for evaluation.
 
         Returns:
             (Tuple[pd.DataFrame, pd.DataFrame]): A tuple containing two dataframes:
                 - df_eval: The evaluation dataframe.
                 - df_preds: The predictions dataframe.
 
-        Example:
+        Examples:
             >>> model = SomeModel()
             >>> fun_control = {
             ...     "train": train_data,
             ...     "test": test_data,
             ...     "target_column": "target",
             ...     "horizon": 5,
             ...     "oml_grace_period": 10,
@@ -195,15 +195,15 @@
                 - horizon (int): The horizon value.
                 - oml_grace_period (int): The oml_grace_period value.
                 - metric_sklearn (str): The metric to be used for evaluation.
 
         Returns:
             (np.ndarray): The objective function values.
 
-        Example:
+        Examples:
             >>> fun_oml_horizon(X, fun_control={'train': train_data, 'test': test_data, 'target_column': 'y', 'horizon': 5, 'oml_grace_period': 10, 'metric_sklearn': 'accuracy'})
             array([0.8, 0.85, 0.9])
         """
         z_res = []
         self.fun_control.update(fun_control)
         self.check_X_shape(X)
         var_dict = assign_values(X, self.fun_control["var_name"])
```

### Comparing `spotRiver-0.0.97/src/spotRiver/fun/hyperriver_old.py` & `spotRiver-0.0.98/src/spotRiver/fun/hyperriver_old.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.97/src/spotRiver/plot/stats.py` & `spotRiver-0.0.98/src/spotRiver/plot/stats.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.97/src/spotRiver/preprocess/impute.py` & `spotRiver-0.0.98/src/spotRiver/preprocess/impute.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.97/src/spotRiver/utils/data_conversion.py` & `spotRiver-0.0.98/src/spotRiver/utils/data_conversion.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.97/src/spotRiver/utils/features.py` & `spotRiver-0.0.98/src/spotRiver/utils/features.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.97/src/spotRiver.egg-info/PKG-INFO` & `spotRiver-0.0.98/src/spotRiver.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: spotRiver
-Version: 0.0.97
+Version: 0.0.98
 Summary: spotRiver - Sequential Parameter Optimization Interface to River
 Author-email: "T. Bartz-Beielstein" <tbb@bartzundbartz.de>
 Project-URL: Homepage, https://www.spotseven.de
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.10
```

### Comparing `spotRiver-0.0.97/src/spotRiver.egg-info/SOURCES.txt` & `spotRiver-0.0.98/src/spotRiver.egg-info/SOURCES.txt`

 * *Files identical despite different names*

