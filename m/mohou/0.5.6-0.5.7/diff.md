# Comparing `tmp/mohou-0.5.6.tar.gz` & `tmp/mohou-0.5.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "mohou-0.5.6.tar", last modified: Thu Mar  2 21:18:32 2023, max compression
+gzip compressed data, was "mohou-0.5.7.tar", last modified: Sun Jul 23 07:00:49 2023, max compression
```

## Comparing `mohou-0.5.6.tar` & `mohou-0.5.7.tar`

### file list

```diff
@@ -1,53 +1,53 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-02 21:18:32.366606 mohou-0.5.6/
--rw-r--r--   0 runner    (1001) docker     (123)     1072 2023-03-02 21:18:22.000000 mohou-0.5.6/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     9237 2023-03-02 21:18:32.366606 mohou-0.5.6/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     8604 2023-03-02 21:18:22.000000 mohou-0.5.6/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-02 21:18:32.362606 mohou-0.5.6/mohou/
--rw-r--r--   0 runner    (1001) docker     (123)      122 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1073 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/asset.py
--rw-r--r--   0 runner    (1001) docker     (123)       67 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/constant.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-02 21:18:32.362606 mohou-0.5.6/mohou/dataset/
--rw-r--r--   0 runner    (1001) docker     (123)      342 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/dataset/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1507 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/dataset/autoencoder_dataset.py
--rw-r--r--   0 runner    (1001) docker     (123)     2947 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/dataset/chimera_dataset.py
--rw-r--r--   0 runner    (1001) docker     (123)    12504 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/dataset/sequence_dataset.py
--rw-r--r--   0 runner    (1001) docker     (123)     8390 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/encoder.py
--rw-r--r--   0 runner    (1001) docker     (123)    18603 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/encoding_rule.py
--rw-r--r--   0 runner    (1001) docker     (123)     4520 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/file.py
--rw-r--r--   0 runner    (1001) docker     (123)     1601 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/image_randomizer.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-02 21:18:32.362606 mohou-0.5.6/mohou/model/
--rw-r--r--   0 runner    (1001) docker     (123)      446 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/model/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    10331 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/model/autoencoder.py
--rw-r--r--   0 runner    (1001) docker     (123)     4627 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/model/chimera.py
--rw-r--r--   0 runner    (1001) docker     (123)     3982 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/model/common.py
--rw-r--r--   0 runner    (1001) docker     (123)     9640 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/model/experimental.py
--rw-r--r--   0 runner    (1001) docker     (123)     9421 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/model/lstm.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-02 21:18:32.362606 mohou-0.5.6/mohou/model/third_party/
--rw-r--r--   0 runner    (1001) docker     (123)       85 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/model/third_party/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    10663 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/model/third_party/variational_lstm.py
--rw-r--r--   0 runner    (1001) docker     (123)    12847 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/propagator.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/py.typed
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-02 21:18:32.366606 mohou-0.5.6/mohou/script/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/script/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2839 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/script/train_autoencoder.py
--rw-r--r--   0 runner    (1001) docker     (123)     3508 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/script/train_chimera.py
--rw-r--r--   0 runner    (1001) docker     (123)     2259 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/script/train_control_model.py
--rw-r--r--   0 runner    (1001) docker     (123)     4255 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/script/train_lstm.py
--rw-r--r--   0 runner    (1001) docker     (123)     2490 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/script/train_pblstm.py
--rw-r--r--   0 runner    (1001) docker     (123)     1067 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/script/visualize_autoencoder_result.py
--rw-r--r--   0 runner    (1001) docker     (123)     1181 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/script/visualize_lstm_result.py
--rw-r--r--   0 runner    (1001) docker     (123)      747 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/script/visualize_train_history.py
--rw-r--r--   0 runner    (1001) docker     (123)    16393 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/script_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     1931 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/setting.py
--rw-r--r--   0 runner    (1001) docker     (123)    16369 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/trainer.py
--rw-r--r--   0 runner    (1001) docker     (123)    44404 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/types.py
--rw-r--r--   0 runner    (1001) docker     (123)     5844 2023-03-02 21:18:22.000000 mohou-0.5.6/mohou/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-03-02 21:18:32.362606 mohou-0.5.6/mohou.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     9237 2023-03-02 21:18:32.000000 mohou-0.5.6/mohou.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1095 2023-03-02 21:18:32.000000 mohou-0.5.6/mohou.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-03-02 21:18:32.000000 mohou-0.5.6/mohou.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      268 2023-03-02 21:18:32.000000 mohou-0.5.6/mohou.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        6 2023-03-02 21:18:32.000000 mohou-0.5.6/mohou.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       63 2023-03-02 21:18:22.000000 mohou-0.5.6/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-03-02 21:18:32.366606 mohou-0.5.6/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1405 2023-03-02 21:18:22.000000 mohou-0.5.6/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:00:49.474302 mohou-0.5.7/
+-rw-r--r--   0 runner    (1001) docker     (123)     1072 2023-07-23 07:00:39.000000 mohou-0.5.7/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     9237 2023-07-23 07:00:49.474302 mohou-0.5.7/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     8604 2023-07-23 07:00:39.000000 mohou-0.5.7/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:00:49.470302 mohou-0.5.7/mohou/
+-rw-r--r--   0 runner    (1001) docker     (123)      122 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1073 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/asset.py
+-rw-r--r--   0 runner    (1001) docker     (123)       67 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/constant.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:00:49.470302 mohou-0.5.7/mohou/dataset/
+-rw-r--r--   0 runner    (1001) docker     (123)      342 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/dataset/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1507 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/dataset/autoencoder_dataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2947 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/dataset/chimera_dataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12504 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/dataset/sequence_dataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8390 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/encoder.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18603 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/encoding_rule.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4520 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/file.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1601 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/image_randomizer.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:00:49.470302 mohou-0.5.7/mohou/model/
+-rw-r--r--   0 runner    (1001) docker     (123)      446 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/model/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10331 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/model/autoencoder.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4627 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/model/chimera.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3982 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/model/common.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9640 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/model/experimental.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9421 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/model/lstm.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:00:49.470302 mohou-0.5.7/mohou/model/third_party/
+-rw-r--r--   0 runner    (1001) docker     (123)       85 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/model/third_party/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10691 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/model/third_party/variational_lstm.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12847 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/propagator.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/py.typed
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:00:49.474302 mohou-0.5.7/mohou/script/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/script/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2839 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/script/train_autoencoder.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3508 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/script/train_chimera.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2259 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/script/train_control_model.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4255 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/script/train_lstm.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2490 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/script/train_pblstm.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1067 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/script/visualize_autoencoder_result.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1181 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/script/visualize_lstm_result.py
+-rw-r--r--   0 runner    (1001) docker     (123)      747 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/script/visualize_train_history.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16393 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/script_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1931 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/setting.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16818 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/trainer.py
+-rw-r--r--   0 runner    (1001) docker     (123)    44434 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/types.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5844 2023-07-23 07:00:39.000000 mohou-0.5.7/mohou/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:00:49.470302 mohou-0.5.7/mohou.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     9237 2023-07-23 07:00:49.000000 mohou-0.5.7/mohou.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1095 2023-07-23 07:00:49.000000 mohou-0.5.7/mohou.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 07:00:49.000000 mohou-0.5.7/mohou.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      265 2023-07-23 07:00:49.000000 mohou-0.5.7/mohou.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        6 2023-07-23 07:00:49.000000 mohou-0.5.7/mohou.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       63 2023-07-23 07:00:39.000000 mohou-0.5.7/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 07:00:49.474302 mohou-0.5.7/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1402 2023-07-23 07:00:39.000000 mohou-0.5.7/setup.py
```

### Comparing `mohou-0.5.6/LICENSE` & `mohou-0.5.7/LICENSE`

 * *Files identical despite different names*

### Comparing `mohou-0.5.6/PKG-INFO` & `mohou-0.5.7/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: mohou
-Version: 0.5.6
+Version: 0.5.7
 Summary: Visuomotor imitation learning framework
 Home-page: https://github.com/HiroIshida/mohou
 Author: Hirokazu Ishida
 Author-email: h-ishida@jsk.imi.i.u-tokyo.ac.jp
 License: MIT
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Developers
```

### Comparing `mohou-0.5.6/README.md` & `mohou-0.5.7/README.md`

 * *Files identical despite different names*

### Comparing `mohou-0.5.6/mohou/asset.py` & `mohou-0.5.7/mohou/asset.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.6/mohou/dataset/autoencoder_dataset.py` & `mohou-0.5.7/mohou/dataset/autoencoder_dataset.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.6/mohou/dataset/chimera_dataset.py` & `mohou-0.5.7/mohou/dataset/chimera_dataset.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.6/mohou/dataset/sequence_dataset.py` & `mohou-0.5.7/mohou/dataset/sequence_dataset.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.6/mohou/encoder.py` & `mohou-0.5.7/mohou/encoder.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.6/mohou/encoding_rule.py` & `mohou-0.5.7/mohou/encoding_rule.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.6/mohou/file.py` & `mohou-0.5.7/mohou/file.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.6/mohou/image_randomizer.py` & `mohou-0.5.7/mohou/image_randomizer.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.6/mohou/model/autoencoder.py` & `mohou-0.5.7/mohou/model/autoencoder.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.6/mohou/model/chimera.py` & `mohou-0.5.7/mohou/model/chimera.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.6/mohou/model/common.py` & `mohou-0.5.7/mohou/model/common.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.6/mohou/model/experimental.py` & `mohou-0.5.7/mohou/model/experimental.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.6/mohou/model/lstm.py` & `mohou-0.5.7/mohou/model/lstm.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.6/mohou/model/third_party/variational_lstm.py` & `mohou-0.5.7/mohou/model/third_party/variational_lstm.py`

 * *Files 1% similar despite different names*

```diff
@@ -127,15 +127,15 @@
         """
         for name_w in self.weights:
             raw_w = getattr(self.module, name_w + "_raw")
             w = None
 
             mask = torch.autograd.Variable(torch.ones(raw_w.size(0), 1))
             if raw_w.is_cuda:
-                mask = mask.cuda()
+                mask = mask.cuda()  # type: ignore[assignment]
             mask = dropout(mask, p=self.dropout, training=True)  # type: ignore
             w = mask.expand_as(raw_w) * raw_w
             setattr(self.module, name_w, w)
 
     def forward(self, *args):
         if self.training:
             self._setweights()
```

### Comparing `mohou-0.5.6/mohou/propagator.py` & `mohou-0.5.7/mohou/propagator.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.6/mohou/script/train_autoencoder.py` & `mohou-0.5.7/mohou/script/train_autoencoder.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.6/mohou/script/train_chimera.py` & `mohou-0.5.7/mohou/script/train_chimera.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.6/mohou/script/train_control_model.py` & `mohou-0.5.7/mohou/script/train_control_model.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.6/mohou/script/train_lstm.py` & `mohou-0.5.7/mohou/script/train_lstm.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.6/mohou/script/train_pblstm.py` & `mohou-0.5.7/mohou/script/train_pblstm.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.6/mohou/script/visualize_autoencoder_result.py` & `mohou-0.5.7/mohou/script/visualize_autoencoder_result.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.6/mohou/script/visualize_lstm_result.py` & `mohou-0.5.7/mohou/script/visualize_lstm_result.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.6/mohou/script/visualize_train_history.py` & `mohou-0.5.7/mohou/script/visualize_train_history.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.6/mohou/script_utils.py` & `mohou-0.5.7/mohou/script_utils.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.6/mohou/setting.py` & `mohou-0.5.7/mohou/setting.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.6/mohou/trainer.py` & `mohou-0.5.7/mohou/trainer.py`

 * *Files 2% similar despite different names*

```diff
@@ -4,15 +4,25 @@
 import re
 import uuid
 import warnings
 from dataclasses import dataclass
 from datetime import datetime, timezone
 from enum import Enum
 from pathlib import Path
-from typing import Dict, Generic, Iterable, List, Optional, Tuple, Type, TypeVar
+from typing import (
+    Callable,
+    Dict,
+    Generic,
+    Iterable,
+    List,
+    Optional,
+    Tuple,
+    Type,
+    TypeVar,
+)
 
 import matplotlib.pyplot as plt
 import numpy as np
 import torch
 import tqdm
 from torch.optim import Adam
 from torch.utils.data import DataLoader, Dataset
@@ -368,19 +378,19 @@
 def train_lower(
     project_path: Path,
     tcache: TrainCache,
     train_loader: Iterable,
     validate_loader: Iterable,
     config: TrainConfig = TrainConfig(),
     device: Optional[torch.device] = None,
+    is_stoppable: Optional[Callable[[TrainCache], None]] = None,
 ) -> None:
     r"""
     low-level train function that accepts train loader
     """
-
     log_package_version_info(logger, mohou)
     log_text_with_box(logger, "train log")
     logger.info("train start with config: {}".format(config))
     logger.info("model cache path: {}".format(tcache.cache_path(project_path)))
 
     model = tcache.best_model
     if device is None:
@@ -428,26 +438,40 @@
 
         # update
         logger.info("epoch: {}".format(epoch))
         logger.info("train loss => {}".format(train_ld_mean))
         logger.info("validate loss => {}".format(validate_ld_mean))
         tcache.update_and_save(model, train_ld_mean, validate_ld_mean, project_path)
 
+        if is_stoppable is not None:
+            if is_stoppable(tcache):
+                logger.info("meet stop criterion. exit from trainning session.")
+                return
+
 
 def train(
     project_path: Path,
     tcache: TrainCache,
     dataset: Dataset,
     config: TrainConfig = TrainConfig(),
     device: Optional[torch.device] = None,
+    is_stoppable: Optional[Callable[[TrainCache], None]] = None,
 ) -> None:
     r"""
     higher-level train function that auto create dataloader from the dataset
     """
 
     dataset_train, dataset_validate = split_with_ratio(dataset, config.valid_data_ratio)
 
     train_loader = DataLoader(dataset=dataset_train, batch_size=config.batch_size, shuffle=True)
     validate_loader = DataLoader(
         dataset=dataset_validate, batch_size=config.batch_size, shuffle=True
     )
-    train_lower(project_path, tcache, train_loader, validate_loader, config=config, device=device)
+    train_lower(
+        project_path,
+        tcache,
+        train_loader,
+        validate_loader,
+        config=config,
+        device=device,
+        is_stoppable=is_stoppable,
+    )
```

### Comparing `mohou-0.5.6/mohou/types.py` & `mohou-0.5.7/mohou/types.py`

 * *Files 1% similar despite different names*

```diff
@@ -321,15 +321,15 @@
     rgb: RGBImage, laplace_kernel_size: int = 3, blur_kernel_size: Optional[Tuple[int, int]] = None
 ) -> GrayImage:
 
     if blur_kernel_size is None:
         blur_kernel_size = (int(rgb.shape[0] * 0.02), int(rgb.shape[1] * 0.02))
 
     src_gray = cv2.cvtColor(rgb.numpy(), cv2.COLOR_BGR2GRAY)
-    dst = cv2.Laplacian(src_gray, cv2.CV_8U, ksize=laplace_kernel_size)
+    dst = cv2.Laplacian(src_gray, cv2.CV_8U, ksize=laplace_kernel_size)  # type: ignore[attr-defined]
     dst2 = cv2.blur(dst, (blur_kernel_size[0], blur_kernel_size[1]))
     return GrayImage(np.expand_dims(np.uint8(dst2), axis=2))
 
 
 class DepthImage(PrimitiveImageBase):
     _channel: ClassVar[int] = 1
     _max_value: ClassVar[float] = 4.0
```

### Comparing `mohou-0.5.6/mohou/utils.py` & `mohou-0.5.7/mohou/utils.py`

 * *Files identical despite different names*

### Comparing `mohou-0.5.6/mohou.egg-info/PKG-INFO` & `mohou-0.5.7/mohou.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: mohou
-Version: 0.5.6
+Version: 0.5.7
 Summary: Visuomotor imitation learning framework
 Home-page: https://github.com/HiroIshida/mohou
 Author: Hirokazu Ishida
 Author-email: h-ishida@jsk.imi.i.u-tokyo.ac.jp
 License: MIT
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Developers
```

### Comparing `mohou-0.5.6/mohou.egg-info/SOURCES.txt` & `mohou-0.5.7/mohou.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `mohou-0.5.6/setup.py` & `mohou-0.5.7/setup.py`

 * *Files 8% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 install_requires = [
     "natsort",
     "numpy",
     "psutil",
     "scikit-learn",
     "torch",
     "torchvision",
-    "tinyfk>=0.4.8",
+    "tinyfk<0.6",
     "tqdm",
     "matplotlib",
     "albumentations",
     'opencv-python-headless<4.3.0;python_version<"3.7"',  # because it takes too long to build
     'opencv-python-headless;python_version>="3.8"',
     "pybullet",
     'imageio==2.15.0;python_version<"3.7"',  # dependency of moviepy
@@ -21,15 +21,15 @@
     "PyYAML>=5.1",
     "types-PyYAML",
     "gdown",
 ]
 
 setup(
     name="mohou",
-    version="0.5.6",
+    version="0.5.7",
     description="Visuomotor imitation learning framework",
     author="Hirokazu Ishida",
     author_email="h-ishida@jsk.imi.i.u-tokyo.ac.jp",
     url="https://github.com/HiroIshida/mohou",
     long_description=open("README.md").read(),
     long_description_content_type="text/markdown",
     license="MIT",
```

