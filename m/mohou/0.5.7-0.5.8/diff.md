# Comparing `tmp/mohou-0.5.7.tar.gz` & `tmp/mohou-0.5.8.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "mohou-0.5.7.tar", last modified: Sun Jul 23 07:00:49 2023, max compression
+gzip compressed data, was "mohou-0.5.8.tar", last modified: Sun Jul 23 07:34:33 2023, max compression
```

## Comparing `mohou-0.5.7.tar` & `mohou-0.5.8.tar`

### file list

```diff
@@ -1,53 +1,53 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:00:49.474302 mohou-0.5.7/
--rw-r--r--   0 runner    (1001) docker     (123)     1072 2023-07-23 07:00:39.000000 mohou-0.5.7/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     9237 2023-07-23 07:00:49.474302 mohou-0.5.7/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     8604 2023-07-23 07:00:39.000000 mohou-0.5.7/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:00:49.470302 mohou-0.5.7/mohou/
--rw-r--r--   0 runner    (1001) docker     (123)      122 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1073 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/asset.py
--rw-r--r--   0 runner    (1001) docker     (123)       67 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/constant.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:00:49.470302 mohou-0.5.7/mohou/dataset/
--rw-r--r--   0 runner    (1001) docker     (123)      342 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/dataset/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1507 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/dataset/autoencoder_dataset.py
--rw-r--r--   0 runner    (1001) docker     (123)     2947 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/dataset/chimera_dataset.py
--rw-r--r--   0 runner    (1001) docker     (123)    12504 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/dataset/sequence_dataset.py
--rw-r--r--   0 runner    (1001) docker     (123)     8390 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/encoder.py
--rw-r--r--   0 runner    (1001) docker     (123)    18603 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/encoding_rule.py
--rw-r--r--   0 runner    (1001) docker     (123)     4520 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/file.py
--rw-r--r--   0 runner    (1001) docker     (123)     1601 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/image_randomizer.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:00:49.470302 mohou-0.5.7/mohou/model/
--rw-r--r--   0 runner    (1001) docker     (123)      446 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/model/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    10331 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/model/autoencoder.py
--rw-r--r--   0 runner    (1001) docker     (123)     4627 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/model/chimera.py
--rw-r--r--   0 runner    (1001) docker     (123)     3982 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/model/common.py
--rw-r--r--   0 runner    (1001) docker     (123)     9640 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/model/experimental.py
--rw-r--r--   0 runner    (1001) docker     (123)     9421 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/model/lstm.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:00:49.470302 mohou-0.5.7/mohou/model/third_party/
--rw-r--r--   0 runner    (1001) docker     (123)       85 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/model/third_party/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    10691 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/model/third_party/variational_lstm.py
--rw-r--r--   0 runner    (1001) docker     (123)    12847 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/propagator.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/py.typed
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:00:49.474302 mohou-0.5.7/mohou/script/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/script/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2839 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/script/train_autoencoder.py
--rw-r--r--   0 runner    (1001) docker     (123)     3508 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/script/train_chimera.py
--rw-r--r--   0 runner    (1001) docker     (123)     2259 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/script/train_control_model.py
--rw-r--r--   0 runner    (1001) docker     (123)     4255 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/script/train_lstm.py
--rw-r--r--   0 runner    (1001) docker     (123)     2490 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/script/train_pblstm.py
--rw-r--r--   0 runner    (1001) docker     (123)     1067 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/script/visualize_autoencoder_result.py
--rw-r--r--   0 runner    (1001) docker     (123)     1181 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/script/visualize_lstm_result.py
--rw-r--r--   0 runner    (1001) docker     (123)      747 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/script/visualize_train_history.py
--rw-r--r--   0 runner    (1001) docker     (123)    16393 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/script_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     1931 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/setting.py
--rw-r--r--   0 runner    (1001) docker     (123)    16818 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/trainer.py
--rw-r--r--   0 runner    (1001) docker     (123)    44434 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/types.py
--rw-r--r--   0 runner    (1001) docker     (123)     5844 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:00:49.470302 mohou-0.5.7/mohou.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     9237 2023-07-23 07:00:49.000000 mohou-0.5.7/mohou.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1095 2023-07-23 07:00:49.000000 mohou-0.5.7/mohou.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 07:00:49.000000 mohou-0.5.7/mohou.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      265 2023-07-23 07:00:49.000000 mohou-0.5.7/mohou.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        6 2023-07-23 07:00:49.000000 mohou-0.5.7/mohou.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       63 2023-07-23 07:00:39.000000 mohou-0.5.7/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 07:00:49.474302 mohou-0.5.7/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1402 2023-07-23 07:00:39.000000 mohou-0.5.7/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:33.814158 mohou-0.5.8/
+-rw-r--r--   0 runner    (1001) docker     (123)     1072 2023-07-23 07:34:18.000000 mohou-0.5.8/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     9257 2023-07-23 07:34:33.814158 mohou-0.5.8/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     8604 2023-07-23 07:34:18.000000 mohou-0.5.8/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:33.806157 mohou-0.5.8/mohou/
+-rw-r--r--   0 runner    (1001) docker     (123)      122 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1073 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/asset.py
+-rw-r--r--   0 runner    (1001) docker     (123)       67 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/constant.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:33.810158 mohou-0.5.8/mohou/dataset/
+-rw-r--r--   0 runner    (1001) docker     (123)      342 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/dataset/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1507 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/dataset/autoencoder_dataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2947 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/dataset/chimera_dataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12504 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/dataset/sequence_dataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8390 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/encoder.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18603 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/encoding_rule.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4520 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/file.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1601 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/image_randomizer.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:33.814158 mohou-0.5.8/mohou/model/
+-rw-r--r--   0 runner    (1001) docker     (123)      446 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/model/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10331 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/model/autoencoder.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4627 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/model/chimera.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3982 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/model/common.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9640 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/model/experimental.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9421 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/model/lstm.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:33.814158 mohou-0.5.8/mohou/model/third_party/
+-rw-r--r--   0 runner    (1001) docker     (123)       85 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/model/third_party/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10691 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/model/third_party/variational_lstm.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12847 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/propagator.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/py.typed
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:33.814158 mohou-0.5.8/mohou/script/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/script/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2839 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/script/train_autoencoder.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3508 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/script/train_chimera.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2259 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/script/train_control_model.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4255 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/script/train_lstm.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2490 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/script/train_pblstm.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1067 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/script/visualize_autoencoder_result.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1181 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/script/visualize_lstm_result.py
+-rw-r--r--   0 runner    (1001) docker     (123)      747 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/script/visualize_train_history.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16393 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/script_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1931 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/setting.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16818 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/trainer.py
+-rw-r--r--   0 runner    (1001) docker     (123)    44434 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/types.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5844 2023-07-23 07:34:18.000000 mohou-0.5.8/mohou/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:33.810158 mohou-0.5.8/mohou.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     9257 2023-07-23 07:34:33.000000 mohou-0.5.8/mohou.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1095 2023-07-23 07:34:33.000000 mohou-0.5.8/mohou.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 07:34:33.000000 mohou-0.5.8/mohou.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      272 2023-07-23 07:34:33.000000 mohou-0.5.8/mohou.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        6 2023-07-23 07:34:33.000000 mohou-0.5.8/mohou.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       63 2023-07-23 07:34:18.000000 mohou-0.5.8/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 07:34:33.814158 mohou-0.5.8/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1465 2023-07-23 07:34:18.000000 mohou-0.5.8/setup.py
```

### Comparing `mohou-0.5.7/LICENSE` & `mohou-0.5.8/LICENSE`

 * *Files identical despite different names*

### Comparing `mohou-0.5.7/PKG-INFO` & `mohou-0.5.8/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,23 +1,24 @@
 Metadata-Version: 2.1
 Name: mohou
-Version: 0.5.7
+Version: 0.5.8
 Summary: Visuomotor imitation learning framework
 Home-page: https://github.com/HiroIshida/mohou
 Author: Hirokazu Ishida
 Author-email: h-ishida@jsk.imi.i.u-tokyo.ac.jp
 License: MIT
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Developers
 Classifier: Natural Language :: English
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Description-Content-Type: text/markdown
+Provides-Extra: all
 License-File: LICENSE
 
 ## mohou [![CI](https://github.com/HiroIshida/mohou/actions/workflows/test.yaml/badge.svg)](https://github.com/HiroIshida/mohou/actions/workflows/test.yaml) [![PypI Auto Release](https://github.com/HiroIshida/mohou/actions/workflows/release.yaml/badge.svg)](https://github.com/HiroIshida/mohou/actions/workflows/release.yaml) [![pypi-version](https://badge.fury.io/py/mohou.svg)](https://pypi.org/project/mohou/) [![python-version](https://img.shields.io/pypi/pyversions/mohou.svg)](https://pypi.org/project/mohou/)
 
 This package implements conv-autoencoder based visuo-motor imitation learning using pytorch. This package focuses on extensibility. One can define custom data types (vector, image and composite-image) and also map/inverse from these custom types to feature vector that fed into the LSTM. Alongside the imitation learning framework, this package provides two demo using pybullet and rlbench to show example usage. Please try [kinematic pybullet demo](/pipeline/pybullet_demo.sh) and [dynamic rlbench demo](/pipeline/rlbench_demo.sh). The results of demo is available on [google drive](https://drive.google.com/drive/folders/1RQU76D5YpKuQ81AZfPMU1YlgIdNrliyt?usp=sharing).
 
 The ros wrapper of this package can be found in [mohou_ros](https://github.com/HiroIshida/mohou_ros). Although `mohou_ros` currently supports only PR2 robot, many useful utilities and scripts for working with a real robot are included.
```

### Comparing `mohou-0.5.7/README.md` & `mohou-0.5.8/README.md`

 * *Files identical despite different names*

### Comparing `mohou-0.5.7/mohou/asset.py` & `mohou-0.5.8/mohou/asset.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.7/mohou/dataset/autoencoder_dataset.py` & `mohou-0.5.8/mohou/dataset/autoencoder_dataset.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.7/mohou/dataset/chimera_dataset.py` & `mohou-0.5.8/mohou/dataset/chimera_dataset.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.7/mohou/dataset/sequence_dataset.py` & `mohou-0.5.8/mohou/dataset/sequence_dataset.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.7/mohou/encoder.py` & `mohou-0.5.8/mohou/encoder.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.7/mohou/encoding_rule.py` & `mohou-0.5.8/mohou/encoding_rule.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.7/mohou/file.py` & `mohou-0.5.8/mohou/file.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.7/mohou/image_randomizer.py` & `mohou-0.5.8/mohou/image_randomizer.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.7/mohou/model/autoencoder.py` & `mohou-0.5.8/mohou/model/autoencoder.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.7/mohou/model/chimera.py` & `mohou-0.5.8/mohou/model/chimera.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.7/mohou/model/common.py` & `mohou-0.5.8/mohou/model/common.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.7/mohou/model/experimental.py` & `mohou-0.5.8/mohou/model/experimental.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.7/mohou/model/lstm.py` & `mohou-0.5.8/mohou/model/lstm.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.7/mohou/model/third_party/variational_lstm.py` & `mohou-0.5.8/mohou/model/third_party/variational_lstm.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.7/mohou/propagator.py` & `mohou-0.5.8/mohou/propagator.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.7/mohou/script/train_autoencoder.py` & `mohou-0.5.8/mohou/script/train_autoencoder.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.7/mohou/script/train_chimera.py` & `mohou-0.5.8/mohou/script/train_chimera.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.7/mohou/script/train_control_model.py` & `mohou-0.5.8/mohou/script/train_control_model.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.7/mohou/script/train_lstm.py` & `mohou-0.5.8/mohou/script/train_lstm.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.7/mohou/script/train_pblstm.py` & `mohou-0.5.8/mohou/script/train_pblstm.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.7/mohou/script/visualize_autoencoder_result.py` & `mohou-0.5.8/mohou/script/visualize_autoencoder_result.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.7/mohou/script/visualize_lstm_result.py` & `mohou-0.5.8/mohou/script/visualize_lstm_result.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.7/mohou/script/visualize_train_history.py` & `mohou-0.5.8/mohou/script/visualize_train_history.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.7/mohou/script_utils.py` & `mohou-0.5.8/mohou/script_utils.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.7/mohou/setting.py` & `mohou-0.5.8/mohou/setting.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.7/mohou/trainer.py` & `mohou-0.5.8/mohou/trainer.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.7/mohou/types.py` & `mohou-0.5.8/mohou/types.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.7/mohou/utils.py` & `mohou-0.5.8/mohou/utils.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.7/mohou.egg-info/PKG-INFO` & `mohou-0.5.8/mohou.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,23 +1,24 @@
 Metadata-Version: 2.1
 Name: mohou
-Version: 0.5.7
+Version: 0.5.8
 Summary: Visuomotor imitation learning framework
 Home-page: https://github.com/HiroIshida/mohou
 Author: Hirokazu Ishida
 Author-email: h-ishida@jsk.imi.i.u-tokyo.ac.jp
 License: MIT
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Developers
 Classifier: Natural Language :: English
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Description-Content-Type: text/markdown
+Provides-Extra: all
 License-File: LICENSE
 
 ## mohou [![CI](https://github.com/HiroIshida/mohou/actions/workflows/test.yaml/badge.svg)](https://github.com/HiroIshida/mohou/actions/workflows/test.yaml) [![PypI Auto Release](https://github.com/HiroIshida/mohou/actions/workflows/release.yaml/badge.svg)](https://github.com/HiroIshida/mohou/actions/workflows/release.yaml) [![pypi-version](https://badge.fury.io/py/mohou.svg)](https://pypi.org/project/mohou/) [![python-version](https://img.shields.io/pypi/pyversions/mohou.svg)](https://pypi.org/project/mohou/)
 
 This package implements conv-autoencoder based visuo-motor imitation learning using pytorch. This package focuses on extensibility. One can define custom data types (vector, image and composite-image) and also map/inverse from these custom types to feature vector that fed into the LSTM. Alongside the imitation learning framework, this package provides two demo using pybullet and rlbench to show example usage. Please try [kinematic pybullet demo](/pipeline/pybullet_demo.sh) and [dynamic rlbench demo](/pipeline/rlbench_demo.sh). The results of demo is available on [google drive](https://drive.google.com/drive/folders/1RQU76D5YpKuQ81AZfPMU1YlgIdNrliyt?usp=sharing).
 
 The ros wrapper of this package can be found in [mohou_ros](https://github.com/HiroIshida/mohou_ros). Although `mohou_ros` currently supports only PR2 robot, many useful utilities and scripts for working with a real robot are included.
```

### Comparing `mohou-0.5.7/mohou.egg-info/SOURCES.txt` & `mohou-0.5.8/mohou.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `mohou-0.5.7/setup.py` & `mohou-0.5.8/setup.py`

 * *Files 19% similar despite different names*

```diff
@@ -5,31 +5,31 @@
 install_requires = [
     "natsort",
     "numpy",
     "psutil",
     "scikit-learn",
     "torch",
     "torchvision",
-    "tinyfk<0.6",
     "tqdm",
     "matplotlib",
     "albumentations",
     'opencv-python-headless<4.3.0;python_version<"3.7"',  # because it takes too long to build
     'opencv-python-headless;python_version>="3.8"',
-    "pybullet",
     'imageio==2.15.0;python_version<"3.7"',  # dependency of moviepy
     "moviepy",
     "PyYAML>=5.1",
     "types-PyYAML",
     "gdown",
 ]
 
+extra_all_requires = ["pybullet", "tinyfk<0.6"]
+
 setup(
     name="mohou",
-    version="0.5.7",
+    version="0.5.8",
     description="Visuomotor imitation learning framework",
     author="Hirokazu Ishida",
     author_email="h-ishida@jsk.imi.i.u-tokyo.ac.jp",
     url="https://github.com/HiroIshida/mohou",
     long_description=open("README.md").read(),
     long_description_content_type="text/markdown",
     license="MIT",
@@ -39,10 +39,11 @@
         "Natural Language :: English",
         "License :: OSI Approved :: MIT License",
         "Programming Language :: Python :: 3.6",
         "Programming Language :: Python :: 3.7",
         "Programming Language :: Python :: 3.8",
     ],
     install_requires=install_requires,
+    extras_require={"all": extra_all_requires},
     packages=find_packages(exclude=("tests", "docs")),
     package_data={"mohou": ["py.typed"]},
 )
```

