# Comparing `tmp/fdfat-0.1.7.tar.gz` & `tmp/fdfat-0.1.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "fdfat-0.1.7.tar", last modified: Mon Jul 17 10:25:50 2023, max compression
+gzip compressed data, was "fdfat-0.1.8.tar", last modified: Sun Jul 23 03:30:36 2023, max compression
```

## Comparing `fdfat-0.1.7.tar` & `fdfat-0.1.8.tar`

### file list

```diff
@@ -1,52 +1,51 @@
-drwxr-xr-x   0 ryan       (501) staff       (20)        0 2023-07-17 10:25:50.897178 fdfat-0.1.7/
--rw-r--r--   0 ryan       (501) staff       (20)      118 2023-07-16 04:39:56.000000 fdfat-0.1.7/MANIFEST.in
--rw-r--r--   0 ryan       (501) staff       (20)     3348 2023-07-17 10:25:50.897043 fdfat-0.1.7/PKG-INFO
--rw-r--r--   0 ryan       (501) staff       (20)     2067 2023-07-13 09:39:58.000000 fdfat-0.1.7/README.md
-drwxr-xr-x   0 ryan       (501) staff       (20)        0 2023-07-17 10:25:50.890153 fdfat-0.1.7/fdfat/
--rw-r--r--   0 ryan       (501) staff       (20)      239 2023-07-17 10:25:10.000000 fdfat-0.1.7/fdfat/__init__.py
-drwxr-xr-x   0 ryan       (501) staff       (20)        0 2023-07-17 10:25:50.891866 fdfat-0.1.7/fdfat/cfg/
--rw-r--r--   0 ryan       (501) staff       (20)     4734 2023-07-16 08:09:07.000000 fdfat-0.1.7/fdfat/cfg/__init__.py
--rw-r--r--   0 ryan       (501) staff       (20)     1954 2023-07-17 03:59:33.000000 fdfat-0.1.7/fdfat/cfg/default.yaml
--rw-r--r--   0 ryan       (501) staff       (20)      116 2023-07-06 09:39:01.000000 fdfat-0.1.7/fdfat/cfg/default_data.yaml
--rw-r--r--   0 ryan       (501) staff       (20)     3934 2023-07-11 11:08:58.000000 fdfat-0.1.7/fdfat/cfg/yaml_utils.py
-drwxr-xr-x   0 ryan       (501) staff       (20)        0 2023-07-17 10:25:50.892238 fdfat-0.1.7/fdfat/cli/
--rw-r--r--   0 ryan       (501) staff       (20)     1337 2023-07-17 03:57:33.000000 fdfat-0.1.7/fdfat/cli/__init__.py
-drwxr-xr-x   0 ryan       (501) staff       (20)        0 2023-07-17 10:25:50.892504 fdfat-0.1.7/fdfat/data/
--rw-r--r--   0 ryan       (501) staff       (20)        0 2023-07-02 01:58:58.000000 fdfat-0.1.7/fdfat/data/__init__.py
--rw-r--r--   0 ryan       (501) staff       (20)     4138 2023-07-17 08:12:15.000000 fdfat-0.1.7/fdfat/data/dataloader.py
-drwxr-xr-x   0 ryan       (501) staff       (20)        0 2023-07-17 10:25:50.893555 fdfat-0.1.7/fdfat/engine/
--rw-r--r--   0 ryan       (501) staff       (20)        0 2023-07-16 02:52:47.000000 fdfat-0.1.7/fdfat/engine/__init__.py
--rw-r--r--   0 ryan       (501) staff       (20)     3109 2023-07-17 10:23:05.000000 fdfat-0.1.7/fdfat/engine/base.py
--rw-r--r--   0 ryan       (501) staff       (20)     3335 2023-07-17 09:38:40.000000 fdfat-0.1.7/fdfat/engine/exporter.py
-drwxr-xr-x   0 ryan       (501) staff       (20)        0 2023-07-17 10:25:50.894339 fdfat-0.1.7/fdfat/engine/loop/
--rw-r--r--   0 ryan       (501) staff       (20)        0 2023-07-16 02:56:31.000000 fdfat-0.1.7/fdfat/engine/loop/__init__.py
--rw-r--r--   0 ryan       (501) staff       (20)     1922 2023-07-11 13:22:27.000000 fdfat-0.1.7/fdfat/engine/loop/tester.py
--rw-r--r--   0 ryan       (501) staff       (20)     2869 2023-07-17 09:49:49.000000 fdfat-0.1.7/fdfat/engine/loop/trainer.py
--rw-r--r--   0 ryan       (501) staff       (20)     2317 2023-07-17 09:49:52.000000 fdfat-0.1.7/fdfat/engine/loop/validator.py
--rw-r--r--   0 ryan       (501) staff       (20)     1532 2023-07-16 06:07:55.000000 fdfat-0.1.7/fdfat/engine/tester.py
--rw-r--r--   0 ryan       (501) staff       (20)     6611 2023-07-17 09:54:14.000000 fdfat-0.1.7/fdfat/engine/trainer.py
--rw-r--r--   0 ryan       (501) staff       (20)     2169 2023-07-17 06:47:01.000000 fdfat-0.1.7/fdfat/engine/validator.py
-drwxr-xr-x   0 ryan       (501) staff       (20)        0 2023-07-17 10:25:50.894649 fdfat-0.1.7/fdfat/metric/
--rw-r--r--   0 ryan       (501) staff       (20)        0 2023-07-02 01:58:57.000000 fdfat-0.1.7/fdfat/metric/__init__.py
--rw-r--r--   0 ryan       (501) staff       (20)      809 2023-07-09 04:19:57.000000 fdfat-0.1.7/fdfat/metric/metric.py
-drwxr-xr-x   0 ryan       (501) staff       (20)        0 2023-07-17 10:25:50.895522 fdfat-0.1.7/fdfat/nn/
--rw-r--r--   0 ryan       (501) staff       (20)        0 2023-07-02 01:57:26.000000 fdfat-0.1.7/fdfat/nn/__init__.py
--rw-r--r--   0 ryan       (501) staff       (20)     3580 2023-07-17 10:21:41.000000 fdfat-0.1.7/fdfat/nn/conv.py
--rw-r--r--   0 ryan       (501) staff       (20)     4444 2023-07-17 10:21:09.000000 fdfat-0.1.7/fdfat/nn/model.py
--rw-r--r--   0 ryan       (501) staff       (20)     5050 2023-07-17 09:44:34.000000 fdfat-0.1.7/fdfat/nn/module.py
-drwxr-xr-x   0 ryan       (501) staff       (20)        0 2023-07-17 10:25:50.896606 fdfat-0.1.7/fdfat/utils/
--rw-r--r--   0 ryan       (501) staff       (20)        0 2023-07-02 01:59:34.000000 fdfat-0.1.7/fdfat/utils/__init__.py
--rw-r--r--   0 ryan       (501) staff       (20)     4013 2023-07-11 13:22:27.000000 fdfat-0.1.7/fdfat/utils/logger.py
--rw-r--r--   0 ryan       (501) staff       (20)     7948 2023-07-17 10:24:57.000000 fdfat-0.1.7/fdfat/utils/model_utils.py
--rw-r--r--   0 ryan       (501) staff       (20)     8029 2023-07-07 05:05:30.000000 fdfat-0.1.7/fdfat/utils/pose_estimation.py
--rw-r--r--   0 ryan       (501) staff       (20)     4857 2023-07-13 08:42:53.000000 fdfat-0.1.7/fdfat/utils/utils.py
-drwxr-xr-x   0 ryan       (501) staff       (20)        0 2023-07-17 10:25:50.890854 fdfat-0.1.7/fdfat.egg-info/
--rw-r--r--   0 ryan       (501) staff       (20)     3348 2023-07-17 10:25:50.000000 fdfat-0.1.7/fdfat.egg-info/PKG-INFO
--rw-r--r--   0 ryan       (501) staff       (20)      918 2023-07-17 10:25:50.000000 fdfat-0.1.7/fdfat.egg-info/SOURCES.txt
--rw-r--r--   0 ryan       (501) staff       (20)        1 2023-07-17 10:25:50.000000 fdfat-0.1.7/fdfat.egg-info/dependency_links.txt
--rw-r--r--   0 ryan       (501) staff       (20)       48 2023-07-17 10:25:50.000000 fdfat-0.1.7/fdfat.egg-info/entry_points.txt
--rw-r--r--   0 ryan       (501) staff       (20)      179 2023-07-17 10:25:50.000000 fdfat-0.1.7/fdfat.egg-info/requires.txt
--rw-r--r--   0 ryan       (501) staff       (20)        6 2023-07-17 10:25:50.000000 fdfat-0.1.7/fdfat.egg-info/top_level.txt
--rw-r--r--   0 ryan       (501) staff       (20)     1110 2023-06-29 01:21:18.000000 fdfat-0.1.7/requirements.txt
--rw-r--r--   0 ryan       (501) staff       (20)       38 2023-07-17 10:25:50.897230 fdfat-0.1.7/setup.cfg
--rw-r--r--   0 ryan       (501) staff       (20)     2119 2023-07-16 05:53:56.000000 fdfat-0.1.7/setup.py
+drwxr-xr-x   0 ryan       (501) staff       (20)        0 2023-07-23 03:30:36.154784 fdfat-0.1.8/
+-rw-r--r--   0 ryan       (501) staff       (20)      118 2023-07-16 04:39:56.000000 fdfat-0.1.8/MANIFEST.in
+-rw-r--r--   0 ryan       (501) staff       (20)     3473 2023-07-23 03:30:36.154618 fdfat-0.1.8/PKG-INFO
+-rw-r--r--   0 ryan       (501) staff       (20)     2192 2023-07-18 03:39:26.000000 fdfat-0.1.8/README.md
+drwxr-xr-x   0 ryan       (501) staff       (20)        0 2023-07-23 03:30:36.145483 fdfat-0.1.8/fdfat/
+-rw-r--r--   0 ryan       (501) staff       (20)      239 2023-07-23 03:29:24.000000 fdfat-0.1.8/fdfat/__init__.py
+drwxr-xr-x   0 ryan       (501) staff       (20)        0 2023-07-23 03:30:36.147405 fdfat-0.1.8/fdfat/cfg/
+-rw-r--r--   0 ryan       (501) staff       (20)     4751 2023-07-22 12:39:57.000000 fdfat-0.1.8/fdfat/cfg/__init__.py
+-rw-r--r--   0 ryan       (501) staff       (20)     2066 2023-07-22 13:11:56.000000 fdfat-0.1.8/fdfat/cfg/default.yaml
+-rw-r--r--   0 ryan       (501) staff       (20)      116 2023-07-06 09:39:01.000000 fdfat-0.1.8/fdfat/cfg/default_data.yaml
+-rw-r--r--   0 ryan       (501) staff       (20)     3934 2023-07-11 11:08:58.000000 fdfat-0.1.8/fdfat/cfg/yaml_utils.py
+drwxr-xr-x   0 ryan       (501) staff       (20)        0 2023-07-23 03:30:36.148799 fdfat-0.1.8/fdfat/cli/
+-rw-r--r--   0 ryan       (501) staff       (20)     1309 2023-07-19 01:45:05.000000 fdfat-0.1.8/fdfat/cli/__init__.py
+drwxr-xr-x   0 ryan       (501) staff       (20)        0 2023-07-23 03:30:36.149069 fdfat-0.1.8/fdfat/data/
+-rw-r--r--   0 ryan       (501) staff       (20)        0 2023-07-02 01:58:58.000000 fdfat-0.1.8/fdfat/data/__init__.py
+-rw-r--r--   0 ryan       (501) staff       (20)     7464 2023-07-22 13:09:08.000000 fdfat-0.1.8/fdfat/data/dataloader.py
+drwxr-xr-x   0 ryan       (501) staff       (20)        0 2023-07-23 03:30:36.149961 fdfat-0.1.8/fdfat/engine/
+-rw-r--r--   0 ryan       (501) staff       (20)        0 2023-07-16 02:52:47.000000 fdfat-0.1.8/fdfat/engine/__init__.py
+-rw-r--r--   0 ryan       (501) staff       (20)     3389 2023-07-19 03:25:31.000000 fdfat-0.1.8/fdfat/engine/base.py
+-rw-r--r--   0 ryan       (501) staff       (20)     3311 2023-07-18 03:36:34.000000 fdfat-0.1.8/fdfat/engine/exporter.py
+drwxr-xr-x   0 ryan       (501) staff       (20)        0 2023-07-23 03:30:36.150297 fdfat-0.1.8/fdfat/engine/loop/
+-rw-r--r--   0 ryan       (501) staff       (20)        0 2023-07-16 02:56:31.000000 fdfat-0.1.8/fdfat/engine/loop/__init__.py
+-rw-r--r--   0 ryan       (501) staff       (20)     3782 2023-07-23 01:59:53.000000 fdfat-0.1.8/fdfat/engine/loop/trainer.py
+-rw-r--r--   0 ryan       (501) staff       (20)     3458 2023-07-23 02:00:13.000000 fdfat-0.1.8/fdfat/engine/loop/validator.py
+-rw-r--r--   0 ryan       (501) staff       (20)     1535 2023-07-19 01:44:18.000000 fdfat-0.1.8/fdfat/engine/predictor.py
+-rw-r--r--   0 ryan       (501) staff       (20)     6611 2023-07-19 01:06:49.000000 fdfat-0.1.8/fdfat/engine/trainer.py
+-rw-r--r--   0 ryan       (501) staff       (20)     3020 2023-07-19 06:42:33.000000 fdfat-0.1.8/fdfat/engine/validator.py
+drwxr-xr-x   0 ryan       (501) staff       (20)        0 2023-07-23 03:30:36.150501 fdfat-0.1.8/fdfat/metric/
+-rw-r--r--   0 ryan       (501) staff       (20)        0 2023-07-02 01:58:57.000000 fdfat-0.1.8/fdfat/metric/__init__.py
+-rw-r--r--   0 ryan       (501) staff       (20)      809 2023-07-19 05:25:08.000000 fdfat-0.1.8/fdfat/metric/metric.py
+drwxr-xr-x   0 ryan       (501) staff       (20)        0 2023-07-23 03:30:36.151649 fdfat-0.1.8/fdfat/nn/
+-rw-r--r--   0 ryan       (501) staff       (20)        0 2023-07-02 01:57:26.000000 fdfat-0.1.8/fdfat/nn/__init__.py
+-rw-r--r--   0 ryan       (501) staff       (20)     3580 2023-07-18 03:43:41.000000 fdfat-0.1.8/fdfat/nn/conv.py
+-rw-r--r--   0 ryan       (501) staff       (20)     4885 2023-07-19 03:56:24.000000 fdfat-0.1.8/fdfat/nn/model.py
+-rw-r--r--   0 ryan       (501) staff       (20)     5050 2023-07-18 03:43:18.000000 fdfat-0.1.8/fdfat/nn/module.py
+drwxr-xr-x   0 ryan       (501) staff       (20)        0 2023-07-23 03:30:36.152654 fdfat-0.1.8/fdfat/utils/
+-rw-r--r--   0 ryan       (501) staff       (20)        0 2023-07-02 01:59:34.000000 fdfat-0.1.8/fdfat/utils/__init__.py
+-rw-r--r--   0 ryan       (501) staff       (20)     4013 2023-07-11 13:22:27.000000 fdfat-0.1.8/fdfat/utils/logger.py
+-rw-r--r--   0 ryan       (501) staff       (20)     7948 2023-07-17 10:24:57.000000 fdfat-0.1.8/fdfat/utils/model_utils.py
+-rw-r--r--   0 ryan       (501) staff       (20)     8029 2023-07-19 05:38:27.000000 fdfat-0.1.8/fdfat/utils/pose_estimation.py
+-rw-r--r--   0 ryan       (501) staff       (20)     6137 2023-07-19 06:45:12.000000 fdfat-0.1.8/fdfat/utils/utils.py
+drwxr-xr-x   0 ryan       (501) staff       (20)        0 2023-07-23 03:30:36.146200 fdfat-0.1.8/fdfat.egg-info/
+-rw-r--r--   0 ryan       (501) staff       (20)     3473 2023-07-23 03:30:36.000000 fdfat-0.1.8/fdfat.egg-info/PKG-INFO
+-rw-r--r--   0 ryan       (501) staff       (20)      893 2023-07-23 03:30:36.000000 fdfat-0.1.8/fdfat.egg-info/SOURCES.txt
+-rw-r--r--   0 ryan       (501) staff       (20)        1 2023-07-23 03:30:36.000000 fdfat-0.1.8/fdfat.egg-info/dependency_links.txt
+-rw-r--r--   0 ryan       (501) staff       (20)       48 2023-07-23 03:30:36.000000 fdfat-0.1.8/fdfat.egg-info/entry_points.txt
+-rw-r--r--   0 ryan       (501) staff       (20)      179 2023-07-23 03:30:36.000000 fdfat-0.1.8/fdfat.egg-info/requires.txt
+-rw-r--r--   0 ryan       (501) staff       (20)        6 2023-07-23 03:30:36.000000 fdfat-0.1.8/fdfat.egg-info/top_level.txt
+-rw-r--r--   0 ryan       (501) staff       (20)     1110 2023-06-29 01:21:18.000000 fdfat-0.1.8/requirements.txt
+-rw-r--r--   0 ryan       (501) staff       (20)       38 2023-07-23 03:30:36.154846 fdfat-0.1.8/setup.cfg
+-rw-r--r--   0 ryan       (501) staff       (20)     2119 2023-07-16 05:53:56.000000 fdfat-0.1.8/setup.py
```

### Comparing `fdfat-0.1.7/PKG-INFO` & `fdfat-0.1.8/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: fdfat
-Version: 0.1.7
+Version: 0.1.8
 Summary: Fast 6DoF Face Alignment and Tracking
 Home-page: https://github.com/RyanDam/Fast-6DoF-Face-Alignment-and-Tracking
 Author: RyanDam
 License: GPL-3.0
 Keywords: machine-learning,deep-learning,vision,ML,DL,AI
 Platform: UNKNOWN
 Classifier: Development Status :: 4 - Beta
@@ -88,14 +88,20 @@
 
 ## Predict
 
 ```bash
 fdfat --task predict --model LightWeightModel --checkpoint <path-to-checkoint> --input <path-to-test-img>
 ```
 
+## Export
+
+```bash
+fdfat --task export --model LightWeightModel --checkpoint <path-to-checkoint> --export_format tflite
+```
+
 ## Credit
 
 - [YOLOv8](https://github.com/ultralytics/ultralytics) : Thanks for ultralytics awesome project, I borrow some code from here.
 - [Ultra-Light-Fast-Generic-Face-Detector-1MB](https://github.com/Linzaer/Ultra-Light-Fast-Generic-Face-Detector-1MB) : Thanks for your lightweight face detector
 - [FaceSynthetics](https://github.com/microsoft/FaceSynthetics) : Thanks for expressive face landmark dataset, it's a good starting point
 - [head-pose-estimation](https://github.com/yinguobing/head-pose-estimation) : Thanks for head pose estimation code
```

### Comparing `fdfat-0.1.7/README.md` & `fdfat-0.1.8/README.md`

 * *Files 8% similar despite different names*

```diff
@@ -58,13 +58,19 @@
 
 ## Predict
 
 ```bash
 fdfat --task predict --model LightWeightModel --checkpoint <path-to-checkoint> --input <path-to-test-img>
 ```
 
+## Export
+
+```bash
+fdfat --task export --model LightWeightModel --checkpoint <path-to-checkoint> --export_format tflite
+```
+
 ## Credit
 
 - [YOLOv8](https://github.com/ultralytics/ultralytics) : Thanks for ultralytics awesome project, I borrow some code from here.
 - [Ultra-Light-Fast-Generic-Face-Detector-1MB](https://github.com/Linzaer/Ultra-Light-Fast-Generic-Face-Detector-1MB) : Thanks for your lightweight face detector
 - [FaceSynthetics](https://github.com/microsoft/FaceSynthetics) : Thanks for expressive face landmark dataset, it's a good starting point
 - [head-pose-estimation](https://github.com/yinguobing/head-pose-estimation) : Thanks for head pose estimation code
```

### Comparing `fdfat-0.1.7/fdfat/cfg/__init__.py` & `fdfat-0.1.8/fdfat/cfg/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,18 +1,18 @@
 from difflib import get_close_matches
 from pathlib import Path
 from types import SimpleNamespace
 from typing import Dict, Union
 
 from fdfat.cfg.yaml_utils import yaml_load, yaml_save, yaml_print, DEFAULT_CFG_DICT, DEFAULT_CFG_DATA, IterableSimpleNamespace
 
-CFG_INT_KEYS= 'seed', 'workers', 'imgsz', 'epoch', 'batch_size', 'dump_batch', 'patience', 'warmup'
-CFG_FRACTION_KEYS = ('lr', 'lr0_factor', 'lr_factor', 'aux_pose_weight')
-CFG_FLOAT_KEYS = ("aug", 'muliplier', 'w_jaw', 'w_leyeb', 'w_reyeb', 'w_nose', 'w_nosetip', 'w_leye', 'w_reye', 'w_mount', 'w_purpil')
-CFG_BOOL_KEYS = ("save", "override", "pin_memory", "aux_pose", "lossw_enabled", "resume", "warmup", "pre_norm", "export_simplify", "export_pose")
+CFG_INT_KEYS= 'seed', 'workers', 'imgsz', 'epoch', 'batch_size', 'dump_batch', 'patience', 'warmup', "lmk_num"
+CFG_FRACTION_KEYS = 'lr', 'lr0_factor', 'lr_factor', 'aux_pose_weight'
+CFG_FLOAT_KEYS = "aug", 'muliplier', 'w_jaw', 'w_leyeb', 'w_reyeb', 'w_nose', 'w_nosetip', 'w_leye', 'w_reye', 'w_mount', 'w_purpil'
+CFG_BOOL_KEYS = "save", "override", "pin_memory", "aux_pose", "lossw_enabled", "resume", "warmup", "pre_norm", "export_simplify", "export_pose", "lmk_mean"
 
 def cfg2dict(cfg):
     """
     Convert a configuration object to a dictionary, whether it is a file path, a string, or a SimpleNamespace object.
 
     Inputs:
         cfg (str) or (Path) or (SimpleNamespace): Configuration object to be converted to a dictionary.
```

### Comparing `fdfat-0.1.7/fdfat/cfg/default.yaml` & `fdfat-0.1.8/fdfat/cfg/default.yaml`

 * *Files 7% similar despite different names*

```diff
@@ -8,21 +8,23 @@
 # data
 data: # path to dataset file, ie. face_synth.yaml
 workers: 8 # number of workers for dataloader
 aug: 0.5 # aug
 input: # input file path/url for prediction
 validation: val # validation target set in the data yaml, one of train, val, test
 pre_norm: True # normalize data in dataloader instead of normalizing right before feeding to model 
+lmk_num: 70 # number of landmark points, 70 for face synthetic, 68 for 300w
 
 # model
 model: LightWeightModel # modelname
 imgsz: 128 # size of input image as integer
 aux_pose: True # model with auxiliary pose esimation
 muliplier: 1.0 # model depth multiplier
 checkpoint: # target checkpoint to load
+lmk_mean: False # use landmark mean
 
 # training
 resume: False # resume training
 epoch: 500 # number of training epoch
 patience: 10 # number of epoch to adjust lr if val loss is not improve
 warmup_epoch: 2 # number of epoch to warmup model using lr0, after that use lr
 optimizer: NAdam # torch.optim class
```

### Comparing `fdfat-0.1.7/fdfat/cfg/yaml_utils.py` & `fdfat-0.1.8/fdfat/cfg/yaml_utils.py`

 * *Files identical despite different names*

### Comparing `fdfat-0.1.7/fdfat/engine/base.py` & `fdfat-0.1.8/fdfat/engine/base.py`

 * *Files 8% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 
 import torch
 from torch import nn
 
 from fdfat.nn import model
 from fdfat.utils.logger import LOGGER
 from fdfat.cfg import get_cfg, get_cfg_data, yaml_save, cfg2dict, yaml_print
-from fdfat.utils.utils import LMK_PART_NAMES, increment_path, generate_graph, read_file_list, render_lmk
+from fdfat.utils.utils import LMK_PARTS, LMK_PART_NAMES, increment_path, generate_graph, read_file_list, render_lmk
 from fdfat.utils.model_utils import init_seeds, select_device, model_info
 
 class BaseEngine:
 
     def __init__(self, cfg_: Union[str, Path, Dict, SimpleNamespace]):
 
         if isinstance(cfg_, (str, Path)):
@@ -45,14 +45,21 @@
 
         LOGGER.info(f"Using {self.cfgs.device} device")
 
         self.start_epoch = 0
         self.best_epoch_loss = 999
         self.best_epoch_no = 0
 
+        if self.cfgs.lmk_num == 70:
+            self.cfgs.lmk_parts = LMK_PARTS
+            self.cfgs.lmk_part_names = LMK_PART_NAMES
+        else: # 68 points
+            self.cfgs.lmk_parts = LMK_PARTS[:-1]
+            self.cfgs.lmk_part_names = LMK_PART_NAMES[:-1]
+
     def load_database(self):
         raise NotImplementedError("Not implemented")
     
     def prepare(self):
         raise NotImplementedError("Not implemented")
 
     def load_model(self, verbose=True):
```

### Comparing `fdfat-0.1.7/fdfat/engine/exporter.py` & `fdfat-0.1.8/fdfat/engine/exporter.py`

 * *Files 1% similar despite different names*

```diff
@@ -70,12 +70,12 @@
                 import onnx2tf
                 
                 tf_saved_path = self.save_wdir / 'saved_model'
 
                 onnx2tf.convert(
                     input_onnx_file_path=onnx_saved_path,
                     output_folder_path=tf_saved_path,
-                    copy_onnx_input_output_names_to_tflite=True,
+                    not_use_onnxsim=True,
                     non_verbose=True
                 )
 
-                LOGGER.info(f"Model saved to: {tf_saved_path}")
+                LOGGER.info(f"Model saved to: {tf_saved_path}")
```

### Comparing `fdfat-0.1.7/fdfat/engine/loop/trainer.py` & `fdfat-0.1.8/fdfat/engine/loop/trainer.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,79 +1,100 @@
 import tqdm
-from collections import defaultdict
-
 import torch
+import numpy as np
+from collections import defaultdict
 
-from fdfat.utils.utils import LMK_PARTS, LMK_PART_NAMES, render_batch
+from fdfat.utils.utils import render_batch
 from fdfat import TQDM_BAR_FORMAT
 from fdfat.metric.metric import nme
+from fdfat.data.dataloader import LMK_POINT_MEANS
 from fdfat.utils.model_utils import normalize_tensor
 
 def train_loop(cfgs, current_epoch, dataloader, model, loss_fn, optimizer, name="Train"):
     loss_dict = defaultdict(lambda: 0)
+    nme_list = []
 
     if cfgs.lossw_enabled:
-        loss_weight = torch.zeros((cfgs.batch_size, 70))
+        loss_weight = torch.zeros((cfgs.batch_size, cfgs.lmk_num*2))
         all_weights = [
                 cfgs.w_jaw, 
                 cfgs.w_leyeb, cfgs.w_reyeb, 
                 cfgs.w_nose, cfgs.w_nosetip, 
                 cfgs.w_leye, cfgs.w_reye, 
                 cfgs.w_mount, cfgs.w_purpil
             ]
-        for idx, (b, e) in enumerate(LMK_PARTS):
-            loss_weight[:, b:e] = all_weights[idx]
+        for idx, (b, e) in enumerate(cfgs.lmk_parts):
+            loss_weight[:, b*2:e*2] = all_weights[idx]
         loss_weight = loss_weight.to(cfgs.device)
 
+    # if cfgs.lmk_mean:
+    #     lmk_means = torch.from_numpy(LMK_POINT_MEANS)
+
     num_batches = len(dataloader)
     pbar = tqdm.tqdm(enumerate(dataloader), total=num_batches, bar_format=TQDM_BAR_FORMAT)
 
     model.train()
     for batch, (x, y) in pbar:
         x_device = x.to(cfgs.device, non_blocking=True)
         if not cfgs.pre_norm:
             x_device = normalize_tensor(x_device).type(torch.float32)
         y_device = y.to(cfgs.device, non_blocking=True)
 
         pred = model(x_device)
 
         if cfgs.aux_pose:
-            loss = loss_fn(pred, y_device[:,:-1])
+            main_loss = loss_fn(pred[:,:cfgs.lmk_num*2], y_device[:,:cfgs.lmk_num*2])
+            pose_loss = loss_fn(pred[:,-3:], y_device[:,-4:-1])
 
             if cfgs.lossw_enabled:
-                loss[:, :70] *= loss_weight[:loss.shape[0], :]
+                main_loss[:, :cfgs.lmk_num*2] *= loss_weight[:main_loss.shape[0], :cfgs.lmk_num*2]
 
             pose_weight = y_device[:,-1:]
-            loss[:,-3:] *= cfgs.aux_pose_weight * pose_weight
-        else:
-            loss = loss_fn(pred, y_device)
+            pose_loss *= cfgs.aux_pose_weight * pose_weight
 
-        total_loss = loss.mean()
+            total_loss = (main_loss.mean() + pose_loss.mean())/2
+
+        else:
+            main_loss = loss_fn(pred[:,:cfgs.lmk_num*2], y_device[:,:cfgs.lmk_num*2])
+            total_loss = main_loss.mean()
 
         # Backpropagation
         total_loss.backward()
         optimizer.step()
         optimizer.zero_grad()
 
         loss_dict["total"] += total_loss.item()
-        loss_dict["nme"] += nme(pred[:,:68*2], y_device[:,:68*2]).mean()
-        for (b, e), pname in zip(LMK_PARTS, LMK_PART_NAMES):
-            loss_dict[pname] += loss[:, b*2:e*2].mean().item()
+        # if cfgs.lmk_mean:
+        #     nme_val = nme(pred[:,:68*2], y_device[:,:68*2]).mean().cpu().detach().numpy()
+        # else:
+        nme_val = nme(pred[:,:68*2], y_device[:,:68*2]).mean().cpu().detach().numpy()
+        loss_dict["nme"] += nme_val
+        nme_list.append(nme_val)
+
+        for (b, e), pname in zip(cfgs.lmk_parts, cfgs.lmk_part_names):
+            loss_dict[pname] += main_loss[:, b*2:e*2].mean().item()
 
         losses_str = f"Total: {loss_dict['total']/(batch+1):>7f}, nmei: {loss_dict['nme']/(batch+1):>7f}"
-        for n in LMK_PART_NAMES:
+        for n in cfgs.lmk_part_names:
             losses_str = f"{losses_str}, {n}: {loss_dict[n]/(batch+1):>7f}"
 
         if cfgs.aux_pose:
-            loss_dict["pose"] += (loss[:,-3:] / cfgs.aux_pose_weight).mean().item()
+            loss_dict["pose"] += (pose_loss / cfgs.aux_pose_weight).mean().item()
             losses_str = f"{losses_str}, pose: {loss_dict['pose']/(batch+1):>7f}"
 
         pbar.set_description(f"{name} epoch [{current_epoch+1:3d}/{cfgs.epoch:3d}] {losses_str}")
         
         if current_epoch == 0 and batch < cfgs.dump_batch:
             save_batch_png = cfgs.save_dir / f'{name}_batch{batch}.png'
             render_batch(x_device.cpu().detach().numpy(), y_device[:,:70*2].cpu().detach().numpy(), save_batch_png)
 
     for k in loss_dict.keys():
         loss_dict[k] /= num_batches
 
+    nme_list = np.array(nme_list)
+    loss_dict["nme_min"] = np.min(nme_list)
+    loss_dict["nme_max"] = np.max(nme_list)
+    loss_dict["nme_mean"] = np.mean(nme_list)
+    loss_dict["nme_median"] = np.median(nme_list)
+    loss_dict["nme_std"] = np.std(nme_list)
+
     return loss_dict
```

### Comparing `fdfat-0.1.7/fdfat/engine/tester.py` & `fdfat-0.1.8/fdfat/engine/predictor.py`

 * *Files 2% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 
 from fdfat import __version__
 from fdfat.utils.logger import LOGGER
 from fdfat.engine.base import BaseEngine
 from fdfat.utils.model_utils import preprocess
 from fdfat.utils.utils import render_lmk
 
-class TestEngine(BaseEngine):
+class PredictEngine(BaseEngine):
 
     def __init__(self, cfg_: Union[str, Path, Dict, SimpleNamespace]):
         super().__init__(cfg_)
         self.load_model()
 
         self.target_checkpoint_path = self.cfgs.checkpoint if self.cfgs.checkpoint is not None else self.save_best
         self.load_checkpoint(self.target_checkpoint_path)
```

### Comparing `fdfat-0.1.7/fdfat/engine/trainer.py` & `fdfat-0.1.8/fdfat/engine/trainer.py`

 * *Files identical despite different names*

### Comparing `fdfat-0.1.7/fdfat/metric/metric.py` & `fdfat-0.1.8/fdfat/metric/metric.py`

 * *Files identical despite different names*

### Comparing `fdfat-0.1.7/fdfat/nn/conv.py` & `fdfat-0.1.8/fdfat/nn/conv.py`

 * *Files identical despite different names*

### Comparing `fdfat-0.1.7/fdfat/nn/model.py` & `fdfat-0.1.8/fdfat/nn/model.py`

 * *Files 12% similar despite different names*

```diff
@@ -30,29 +30,33 @@
         csd = intersect_dicts(csd, self.state_dict())  # intersect
         self.load_state_dict(csd, strict=False)  # load
         if verbose:
             LOGGER.info(f'Transferred {len(csd)}/{len(self.state_dict())} items from pretrained weights')
 
 class LightWeightModel(BaseModel):
 
-    def __init__(self, imgz=128, muliplier=1, pose_rotation=False):
+    default_act = nn.ReLU6()  # default activation
+
+    def __init__(self, imgz=128, muliplier=1, pose_rotation=False, act=True):
         super().__init__()
         self.pose_rotation = pose_rotation
 
+        self.act = self.default_act if act is True else act if isinstance(act, nn.Module) else nn.Identity()
+
         # backbone, output size = size/4
-        self.backbone = module.LightWeightBackbone(muliplier=muliplier)
+        self.backbone = module.LightWeightBackbone(muliplier=muliplier, act=self.act)
 
         # mainstream, output size:
         # x1 = size/8
         # x2 = size/16
         # x3 = size/16
-        self.mainstream = module.MainStreamModule(muliplier=muliplier)
+        self.mainstream = module.MainStreamModule(muliplier=muliplier, act=self.act)
 
         if pose_rotation:
-            self.aux = module.AuxiliaryBackbone(int(16*muliplier), 3, muliplier=muliplier)
+            self.aux = module.AuxiliaryBackbone(int(16*muliplier), 3, muliplier=muliplier, act=self.act)
             
         output_ch = int((128 + 128 + 128)*muliplier)
         self.logit = module.FERegress(output_ch, 70*2)
 
         self.concat = Concat()
 
         initialize_weights(self)
@@ -69,14 +73,19 @@
         x = self.logit(x)
 
         if self.pose_rotation:
             x = self.concat([x, aux])
 
         return x
 
+class LightWeightModelSiLU(LightWeightModel):
+
+    def __init__(self, imgz=128, muliplier=1, pose_rotation=False, act=True):
+        super().__init__(imgz=imgz, muliplier=muliplier, pose_rotation=pose_rotation, act=nn.SiLU())
+
 class LandmarkModel(BaseModel):
 
     def __init__(self, imgz=128, muliplier=1, pose_rotation=False):
         super().__init__()
         
         self.stack1 = nn.Sequential(
             nn.Conv2d( 3, int(32*muliplier), 3, stride=2, padding=2),
```

### Comparing `fdfat-0.1.7/fdfat/nn/module.py` & `fdfat-0.1.8/fdfat/nn/module.py`

 * *Files identical despite different names*

### Comparing `fdfat-0.1.7/fdfat/utils/logger.py` & `fdfat-0.1.8/fdfat/utils/logger.py`

 * *Files identical despite different names*

### Comparing `fdfat-0.1.7/fdfat/utils/model_utils.py` & `fdfat-0.1.8/fdfat/utils/model_utils.py`

 * *Files identical despite different names*

### Comparing `fdfat-0.1.7/fdfat/utils/pose_estimation.py` & `fdfat-0.1.8/fdfat/utils/pose_estimation.py`

 * *Files identical despite different names*

### Comparing `fdfat-0.1.7/fdfat.egg-info/PKG-INFO` & `fdfat-0.1.8/fdfat.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: fdfat
-Version: 0.1.7
+Version: 0.1.8
 Summary: Fast 6DoF Face Alignment and Tracking
 Home-page: https://github.com/RyanDam/Fast-6DoF-Face-Alignment-and-Tracking
 Author: RyanDam
 License: GPL-3.0
 Keywords: machine-learning,deep-learning,vision,ML,DL,AI
 Platform: UNKNOWN
 Classifier: Development Status :: 4 - Beta
@@ -88,14 +88,20 @@
 
 ## Predict
 
 ```bash
 fdfat --task predict --model LightWeightModel --checkpoint <path-to-checkoint> --input <path-to-test-img>
 ```
 
+## Export
+
+```bash
+fdfat --task export --model LightWeightModel --checkpoint <path-to-checkoint> --export_format tflite
+```
+
 ## Credit
 
 - [YOLOv8](https://github.com/ultralytics/ultralytics) : Thanks for ultralytics awesome project, I borrow some code from here.
 - [Ultra-Light-Fast-Generic-Face-Detector-1MB](https://github.com/Linzaer/Ultra-Light-Fast-Generic-Face-Detector-1MB) : Thanks for your lightweight face detector
 - [FaceSynthetics](https://github.com/microsoft/FaceSynthetics) : Thanks for expressive face landmark dataset, it's a good starting point
 - [head-pose-estimation](https://github.com/yinguobing/head-pose-estimation) : Thanks for head pose estimation code
```

### Comparing `fdfat-0.1.7/fdfat.egg-info/SOURCES.txt` & `fdfat-0.1.8/fdfat.egg-info/SOURCES.txt`

 * *Files 4% similar despite different names*

```diff
@@ -15,19 +15,18 @@
 fdfat/cfg/yaml_utils.py
 fdfat/cli/__init__.py
 fdfat/data/__init__.py
 fdfat/data/dataloader.py
 fdfat/engine/__init__.py
 fdfat/engine/base.py
 fdfat/engine/exporter.py
-fdfat/engine/tester.py
+fdfat/engine/predictor.py
 fdfat/engine/trainer.py
 fdfat/engine/validator.py
 fdfat/engine/loop/__init__.py
-fdfat/engine/loop/tester.py
 fdfat/engine/loop/trainer.py
 fdfat/engine/loop/validator.py
 fdfat/metric/__init__.py
 fdfat/metric/metric.py
 fdfat/nn/__init__.py
 fdfat/nn/conv.py
 fdfat/nn/model.py
```

### Comparing `fdfat-0.1.7/requirements.txt` & `fdfat-0.1.8/requirements.txt`

 * *Files identical despite different names*

### Comparing `fdfat-0.1.7/setup.py` & `fdfat-0.1.8/setup.py`

 * *Files identical despite different names*

