# Comparing `tmp/pytorch_tabnet-4.0.tar.gz` & `tmp/pytorch_tabnet-4.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pytorch_tabnet-4.0.tar", max compression
+gzip compressed data, was "pytorch_tabnet-4.1.0.tar", max compression
```

## Comparing `pytorch_tabnet-4.0.tar` & `pytorch_tabnet-4.1.0.tar`

### file list

```diff
@@ -1,17 +1,17 @@
--rw-r--r--   0        0        0     1067 2022-09-14 16:42:30.701722 pytorch_tabnet-4.0/LICENSE
--rw-r--r--   0        0        0    13691 2022-09-14 16:42:30.701722 pytorch_tabnet-4.0/README.md
--rw-r--r--   0        0        0      793 2022-09-14 16:42:30.753723 pytorch_tabnet-4.0/pyproject.toml
--rw-r--r--   0        0        0    24764 2022-09-14 16:42:30.753723 pytorch_tabnet-4.0/pytorch_tabnet/abstract_model.py
--rw-r--r--   0        0        0     3232 2022-09-14 16:42:30.753723 pytorch_tabnet-4.0/pytorch_tabnet/augmentations.py
--rw-r--r--   0        0        0     8453 2022-09-14 16:42:30.753723 pytorch_tabnet-4.0/pytorch_tabnet/callbacks.py
--rw-r--r--   0        0        0    13498 2022-09-14 16:42:30.753723 pytorch_tabnet-4.0/pytorch_tabnet/metrics.py
--rw-r--r--   0        0        0    12673 2022-09-14 16:42:30.753723 pytorch_tabnet-4.0/pytorch_tabnet/multiclass_utils.py
--rw-r--r--   0        0        0     5318 2022-09-14 16:42:30.753723 pytorch_tabnet-4.0/pytorch_tabnet/multitask.py
--rw-r--r--   0        0        0    12937 2022-09-14 16:42:30.753723 pytorch_tabnet-4.0/pytorch_tabnet/pretraining.py
--rw-r--r--   0        0        0     3190 2022-09-14 16:42:30.753723 pytorch_tabnet-4.0/pytorch_tabnet/pretraining_utils.py
--rw-r--r--   0        0        0     8540 2022-09-14 16:42:30.753723 pytorch_tabnet-4.0/pytorch_tabnet/sparsemax.py
--rwxr-xr-x   0        0        0     4396 2022-09-14 16:42:30.753723 pytorch_tabnet-4.0/pytorch_tabnet/tab_model.py
--rw-r--r--   0        0        0    30098 2022-09-14 16:42:30.753723 pytorch_tabnet-4.0/pytorch_tabnet/tab_network.py
--rw-r--r--   0        0        0    10875 2022-09-14 16:42:30.753723 pytorch_tabnet-4.0/pytorch_tabnet/utils.py
--rw-r--r--   0        0        0    14858 1970-01-01 00:00:00.000000 pytorch_tabnet-4.0/setup.py
--rw-r--r--   0        0        0    14545 1970-01-01 00:00:00.000000 pytorch_tabnet-4.0/PKG-INFO
+-rw-r--r--   0        0        0     1067 2023-07-23 13:20:37.090402 pytorch_tabnet-4.1.0/LICENSE
+-rw-r--r--   0        0        0    14889 2023-07-23 13:20:38.686448 pytorch_tabnet-4.1.0/README.md
+-rw-r--r--   0        0        0      798 2023-07-23 13:20:38.714449 pytorch_tabnet-4.1.0/pyproject.toml
+-rw-r--r--   0        0        0    26219 2023-07-23 13:20:38.686448 pytorch_tabnet-4.1.0/pytorch_tabnet/abstract_model.py
+-rw-r--r--   0        0        0     3232 2023-07-23 13:20:37.142403 pytorch_tabnet-4.1.0/pytorch_tabnet/augmentations.py
+-rw-r--r--   0        0        0     8453 2023-07-23 13:20:37.142403 pytorch_tabnet-4.1.0/pytorch_tabnet/callbacks.py
+-rw-r--r--   0        0        0    13512 2023-07-23 13:20:38.686448 pytorch_tabnet-4.1.0/pytorch_tabnet/metrics.py
+-rw-r--r--   0        0        0    12673 2023-07-23 13:20:37.142403 pytorch_tabnet-4.1.0/pytorch_tabnet/multiclass_utils.py
+-rw-r--r--   0        0        0     5904 2023-07-23 13:20:38.686448 pytorch_tabnet-4.1.0/pytorch_tabnet/multitask.py
+-rw-r--r--   0        0        0    13539 2023-07-23 13:20:38.690449 pytorch_tabnet-4.1.0/pytorch_tabnet/pretraining.py
+-rw-r--r--   0        0        0     4177 2023-07-23 13:20:38.690449 pytorch_tabnet-4.1.0/pytorch_tabnet/pretraining_utils.py
+-rw-r--r--   0        0        0     8540 2023-07-23 13:20:37.142403 pytorch_tabnet-4.1.0/pytorch_tabnet/sparsemax.py
+-rwxr-xr-x   0        0        0     4706 2023-07-23 13:20:38.690449 pytorch_tabnet-4.1.0/pytorch_tabnet/tab_model.py
+-rw-r--r--   0        0        0    32515 2023-07-23 13:20:38.690449 pytorch_tabnet-4.1.0/pytorch_tabnet/tab_network.py
+-rw-r--r--   0        0        0    17426 2023-07-23 13:20:38.690449 pytorch_tabnet-4.1.0/pytorch_tabnet/utils.py
+-rw-r--r--   0        0        0    16054 1970-01-01 00:00:00.000000 pytorch_tabnet-4.1.0/setup.py
+-rw-r--r--   0        0        0    15680 1970-01-01 00:00:00.000000 pytorch_tabnet-4.1.0/PKG-INFO
```

### Comparing `pytorch_tabnet-4.0/LICENSE` & `pytorch_tabnet-4.1.0/LICENSE`

 * *Files identical despite different names*

### Comparing `pytorch_tabnet-4.0/README.md` & `pytorch_tabnet-4.1.0/README.md`

 * *Files 7% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 # README
 
 # TabNet : Attentive Interpretable Tabular Learning
 
-This is a pyTorch implementation of Tabnet (Arik, S. O., & Pfister, T. (2019). TabNet: Attentive Interpretable Tabular Learning. arXiv preprint arXiv:1908.07442.) https://arxiv.org/pdf/1908.07442.pdf.
+This is a pyTorch implementation of Tabnet (Arik, S. O., & Pfister, T. (2019). TabNet: Attentive Interpretable Tabular Learning. arXiv preprint arXiv:1908.07442.) https://arxiv.org/pdf/1908.07442.pdf. Please note that some different choices have been made overtime to improve the library which can differ from the orginal paper.
 
 <!--- BADGES: START --->
 [![CircleCI](https://circleci.com/gh/dreamquark-ai/tabnet.svg?style=svg)](https://circleci.com/gh/dreamquark-ai/tabnet)
 
 [![PyPI version](https://badge.fury.io/py/pytorch-tabnet.svg)](https://badge.fury.io/py/pytorch-tabnet)
 
 ![PyPI - Downloads](https://img.shields.io/pypi/dm/pytorch-tabnet)
@@ -64,14 +64,18 @@
 
 -----------------
 
 - `poetry install` to install all the dependencies, including jupyter
 
 - `make notebook` inside the same terminal. You can then follow the link to a jupyter notebook with tabnet installed.
 
+# What is new ?
+
+- from version **> 4.0** attention is now embedding aware. This aims to maintain a good attention mechanism even with large number of embedding. It is also now possible to specify attention groups (using `grouped_features`). Attention is now done at the group level and not feature level. This is especially useful if a dataset has a lot of columns coming from on single source of data (exemple: a text column transformed using TD-IDF).
+
 # Contributing
 
 When contributing to the TabNet repository, please make sure to first discuss the change you wish to make via a new or already existing issue.
 
 Our commits follow the rules presented [here](https://www.conventionalcommits.org/en/v1.0.0/).
 
 # What problems does pytorch-tabnet handle?
@@ -312,25 +316,31 @@
 
 - `device_name` : str (default='auto')
     'cpu' for cpu training, 'gpu' for gpu training, 'auto' to automatically detect gpu.
 
 - `mask_type: str` (default='sparsemax')
     Either "sparsemax" or "entmax" : this is the masking function to use for selecting features.
 
+- `grouped_features: list of list of ints` (default=None)
+    This allows the model to share it's attention accross feature inside a same group.
+    This can be especially useful when your preprocessing generates correlated or dependant features: like if you use a TF-IDF or a PCA on a text column.
+    Note that feature importance will be exactly the same between features on a same group.
+    Please also note that embeddings generated for a categorical variable are always inside a same group. 
+
 - `n_shared_decoder` : int (default=1)
 
     Number of shared GLU block in decoder, this is only useful for `TabNetPretrainer`.
 
 - `n_indep_decoder` : int (default=1)
 
     Number of independent GLU block in decoder, this is only useful for `TabNetPretrainer`.
 
 ## Fit parameters
 
-- `X_train` : np.array
+- `X_train` : np.array or scipy.sparse.csr_matrix
 
     Training features
 
 - `y_train` : np.array
 
     Training targets
 
@@ -397,7 +407,11 @@
         /!\ TabNetPretrainer Only : Percentage of input features to mask during pretraining.
 
         Should be between 0 and 1. The bigger the harder the reconstruction task is.
 
 - `warm_start` : bool (default=False)
     In order to match scikit-learn API, this is set to False.
     It allows to fit twice the same model and start from a warm start.
+
+- `compute_importance` : bool (default=True)
+
+    Whether to compute feature importance
```

### Comparing `pytorch_tabnet-4.0/pyproject.toml` & `pytorch_tabnet-4.1.0/pyproject.toml`

 * *Files 6% similar despite different names*

```diff
@@ -1,25 +1,25 @@
 [tool.poetry]
 name = "pytorch_tabnet"
-version = "4.0"
+version = "4.1.0"
 description = "PyTorch implementation of TabNet"
 homepage = "https://github.com/dreamquark-ai/tabnet"
 repository = "https://github.com/dreamquark-ai/tabnet"
 documentation = "https://github.com/dreamquark-ai/tabnet"
 readme = "README.md"
 authors = []
 keywords = ["tabnet", "pytorch", "neural-networks" ]
 exclude = ["tabnet/*.ipynb"]
 
 [tool.poetry.dependencies]
-python = ">=3.6"
+python = ">=3.7"
 
-numpy="^1.17"
-torch="^1.2"
-tqdm="^4.36"
+numpy=">=1.17"
+torch=">=1.3"
+tqdm=">=4.36"
 scikit_learn=">0.21"
 scipy=">1.4"
 
 [tool.poetry.dev-dependencies]
 jupyter="1.0.0"
 xgboost="0.90"
 matplotlib="3.1.1"
```

### Comparing `pytorch_tabnet-4.0/pytorch_tabnet/abstract_model.py` & `pytorch_tabnet-4.1.0/pytorch_tabnet/abstract_model.py`

 * *Files 3% similar despite different names*

```diff
@@ -3,22 +3,25 @@
 import torch
 from torch.nn.utils import clip_grad_norm_
 import numpy as np
 from scipy.sparse import csc_matrix
 from abc import abstractmethod
 from pytorch_tabnet import tab_network
 from pytorch_tabnet.utils import (
+    SparsePredictDataset,
     PredictDataset,
     create_explain_matrix,
     validate_eval_set,
     create_dataloaders,
     define_device,
     ComplexEncoder,
     check_input,
-    check_warm_start
+    check_warm_start,
+    create_group_matrix,
+    check_embedding_parameters
 )
 from pytorch_tabnet.callbacks import (
     CallbackContainer,
     History,
     EarlyStopping,
     LRSchedulerCallback,
 )
@@ -29,14 +32,15 @@
 import io
 import json
 from pathlib import Path
 import shutil
 import zipfile
 import warnings
 import copy
+import scipy
 
 
 @dataclass
 class TabModel(BaseEstimator):
     """ Class for TabNet model."""
 
     n_d: int = 8
@@ -60,28 +64,36 @@
     scheduler_params: Dict = field(default_factory=dict)
     mask_type: str = "sparsemax"
     input_dim: int = None
     output_dim: int = None
     device_name: str = "auto"
     n_shared_decoder: int = 1
     n_indep_decoder: int = 1
+    grouped_features: List[List[int]] = field(default_factory=list)
 
     def __post_init__(self):
+        # These are default values needed for saving model
         self.batch_size = 1024
         self.virtual_batch_size = 128
+
         torch.manual_seed(self.seed)
         # Defining device
         self.device = torch.device(define_device(self.device_name))
         if self.verbose != 0:
             warnings.warn(f"Device used : {self.device}")
 
         # create deep copies of mutable parameters
         self.optimizer_fn = copy.deepcopy(self.optimizer_fn)
         self.scheduler_fn = copy.deepcopy(self.scheduler_fn)
 
+        updated_params = check_embedding_parameters(self.cat_dims,
+                                                    self.cat_idxs,
+                                                    self.cat_emb_dim)
+        self.cat_dims, self.cat_idxs, self.cat_emb_dim = updated_params
+
     def __update__(self, **kwargs):
         """
         Updates parameters.
         If does not already exists, creates it.
         Otherwise overwrite with warnings.
         """
         update_list = [
@@ -91,14 +103,15 @@
             "input_dim",
             "mask_type",
             "n_a",
             "n_d",
             "n_independent",
             "n_shared",
             "n_steps",
+            "grouped_features",
         ]
         for var_name, value in kwargs.items():
             if var_name in update_list:
                 try:
                     exec(f"global previous_val; previous_val = self.{var_name}")
                     if previous_val != value:  # noqa
                         wrn_msg = f"Pretraining: {var_name} changed from {previous_val} to {value}"  # noqa
@@ -123,14 +136,15 @@
         num_workers=0,
         drop_last=True,
         callbacks=None,
         pin_memory=True,
         from_unsupervised=None,
         warm_start=False,
         augmentations=None,
+        compute_importance=True
     ):
         """Train a neural network stored in self.network
         Using train_dataloader for training data and
         valid_dataloader for validation.
 
         Parameters
         ----------
@@ -168,27 +182,30 @@
             List of custom callbacks
         pin_memory: bool
             Whether to set pin_memory to True or False during training
         from_unsupervised: unsupervised trained model
             Use a previously self supervised model as starting weights
         warm_start: bool
             If True, current model parameters are used to start training
+        compute_importance : bool
+            Whether to compute feature importance
         """
         # update model name
 
         self.max_epochs = max_epochs
         self.patience = patience
         self.batch_size = batch_size
         self.virtual_batch_size = virtual_batch_size
         self.num_workers = num_workers
         self.drop_last = drop_last
         self.input_dim = X_train.shape[1]
         self._stop_training = False
         self.pin_memory = pin_memory and (self.device.type != "cpu")
         self.augmentations = augmentations
+        self.compute_importance = compute_importance
 
         if self.augmentations is not None:
             # This ensure reproducibility
             self.augmentations._set_seed()
 
         eval_set = eval_set if eval_set else []
 
@@ -252,37 +269,46 @@
             if self._stop_training:
                 break
 
         # Call method on_train_end for all callbacks
         self._callback_container.on_train_end()
         self.network.eval()
 
-        # compute feature importance once the best model is defined
-        self.feature_importances_ = self._compute_feature_importances(X_train)
+        if self.compute_importance:
+            # compute feature importance once the best model is defined
+            self.feature_importances_ = self._compute_feature_importances(X_train)
 
     def predict(self, X):
         """
         Make predictions on a batch (valid)
 
         Parameters
         ----------
-        X : a :tensor: `torch.Tensor`
+        X : a :tensor: `torch.Tensor` or matrix: `scipy.sparse.csr_matrix`
             Input data
 
         Returns
         -------
         predictions : np.array
             Predictions of the regression problem
         """
         self.network.eval()
-        dataloader = DataLoader(
-            PredictDataset(X),
-            batch_size=self.batch_size,
-            shuffle=False,
-        )
+
+        if scipy.sparse.issparse(X):
+            dataloader = DataLoader(
+                SparsePredictDataset(X),
+                batch_size=self.batch_size,
+                shuffle=False,
+            )
+        else:
+            dataloader = DataLoader(
+                PredictDataset(X),
+                batch_size=self.batch_size,
+                shuffle=False,
+            )
 
         results = []
         for batch_nb, data in enumerate(dataloader):
             data = data.to(self.device).float()
             output, M_loss = self.network(data)
             predictions = output.cpu().detach().numpy()
             results.append(predictions)
@@ -291,45 +317,51 @@
 
     def explain(self, X, normalize=False):
         """
         Return local explanation
 
         Parameters
         ----------
-        X : tensor: `torch.Tensor`
+        X : tensor: `torch.Tensor` or matrix: `scipy.sparse.csr_matrix`
             Input data
         normalize : bool (default False)
             Wheter to normalize so that sum of features are equal to 1
 
         Returns
         -------
         M_explain : matrix
             Importance per sample, per columns.
         masks : matrix
             Sparse matrix showing attention masks used by network.
         """
         self.network.eval()
 
-        dataloader = DataLoader(
-            PredictDataset(X),
-            batch_size=self.batch_size,
-            shuffle=False,
-        )
+        if scipy.sparse.issparse(X):
+            dataloader = DataLoader(
+                SparsePredictDataset(X),
+                batch_size=self.batch_size,
+                shuffle=False,
+            )
+        else:
+            dataloader = DataLoader(
+                PredictDataset(X),
+                batch_size=self.batch_size,
+                shuffle=False,
+            )
 
         res_explain = []
 
         for batch_nb, data in enumerate(dataloader):
             data = data.to(self.device).float()
 
             M_explain, masks = self.network.forward_masks(data)
             for key, value in masks.items():
                 masks[key] = csc_matrix.dot(
                     value.cpu().detach().numpy(), self.reducing_matrix
                 )
-
             original_feat_explain = csc_matrix.dot(M_explain.cpu().detach().numpy(),
                                                    self.reducing_matrix)
             res_explain.append(original_feat_explain)
 
             if batch_nb == 0:
                 res_masks = masks
             else:
@@ -563,14 +595,17 @@
             scores = scores.cpu().detach().numpy()
 
         return scores
 
     def _set_network(self):
         """Setup the network and explain matrix."""
         torch.manual_seed(self.seed)
+
+        self.group_matrix = create_group_matrix(self.grouped_features, self.input_dim)
+
         self.network = tab_network.TabNet(
             self.input_dim,
             self.output_dim,
             n_d=self.n_d,
             n_a=self.n_a,
             n_steps=self.n_steps,
             gamma=self.gamma,
@@ -579,14 +614,15 @@
             cat_emb_dim=self.cat_emb_dim,
             n_independent=self.n_independent,
             n_shared=self.n_shared,
             epsilon=self.epsilon,
             virtual_batch_size=self.virtual_batch_size,
             momentum=self.momentum,
             mask_type=self.mask_type,
+            group_attention_matrix=self.group_matrix.to(self.device),
         ).to(self.device)
 
         self.reducing_matrix = create_explain_matrix(
             self.network.input_dim,
             self.network.cat_emb_dim,
             self.network.cat_idxs,
             self.network.post_embed_dim,
```

### Comparing `pytorch_tabnet-4.0/pytorch_tabnet/augmentations.py` & `pytorch_tabnet-4.1.0/pytorch_tabnet/augmentations.py`

 * *Files identical despite different names*

### Comparing `pytorch_tabnet-4.0/pytorch_tabnet/callbacks.py` & `pytorch_tabnet-4.1.0/pytorch_tabnet/callbacks.py`

 * *Files identical despite different names*

### Comparing `pytorch_tabnet-4.0/pytorch_tabnet/metrics.py` & `pytorch_tabnet-4.1.0/pytorch_tabnet/metrics.py`

 * *Files 1% similar despite different names*

```diff
@@ -368,15 +368,15 @@
             MSE of predictions vs targets.
         """
         return mean_squared_error(y_true, y_score)
 
 
 class RMSLE(Metric):
     """
-    Mean squared logarithmic error regression loss.
+    Root Mean squared logarithmic error regression loss.
     Scikit-implementation:
     https://scikit-learn.org/stable/modules/generated/sklearn.metrics.mean_squared_log_error.html
     Note: In order to avoid error, negative predictions are clipped to 0.
     This means that you should clip negative predictions manually after calling predict.
     """
 
     def __init__(self):
@@ -396,15 +396,15 @@
 
         Returns
         -------
         float
             RMSLE of predictions vs targets.
         """
         y_score = np.clip(y_score, a_min=0, a_max=None)
-        return mean_squared_log_error(y_true, y_score)
+        return np.sqrt(mean_squared_log_error(y_true, y_score))
 
 
 class UnsupervisedMetric(Metric):
     """
     Unsupervised metric
     """
```

### Comparing `pytorch_tabnet-4.0/pytorch_tabnet/multiclass_utils.py` & `pytorch_tabnet-4.1.0/pytorch_tabnet/multiclass_utils.py`

 * *Files identical despite different names*

### Comparing `pytorch_tabnet-4.0/pytorch_tabnet/multitask.py` & `pytorch_tabnet-4.1.0/pytorch_tabnet/multitask.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,14 +1,15 @@
 import torch
 import numpy as np
 from scipy.special import softmax
-from pytorch_tabnet.utils import PredictDataset, filter_weights
+from pytorch_tabnet.utils import SparsePredictDataset, PredictDataset, filter_weights
 from pytorch_tabnet.abstract_model import TabModel
 from pytorch_tabnet.multiclass_utils import infer_multitask_output, check_output_dim
 from torch.utils.data import DataLoader
+import scipy
 
 
 class TabNetMultiTaskClassifier(TabModel):
     def __post_init__(self):
         super(TabNetMultiTaskClassifier, self).__post_init__()
         self._task = 'classification'
         self._default_loss = torch.nn.functional.cross_entropy
@@ -83,28 +84,36 @@
 
     def predict(self, X):
         """
         Make predictions on a batch (valid)
 
         Parameters
         ----------
-        X : a :tensor: `torch.Tensor`
+        X : a :tensor: `torch.Tensor` or matrix: `scipy.sparse.csr_matrix`
             Input data
 
         Returns
         -------
         results : np.array
             Predictions of the most probable class
         """
         self.network.eval()
-        dataloader = DataLoader(
-            PredictDataset(X),
-            batch_size=self.batch_size,
-            shuffle=False,
-        )
+
+        if scipy.sparse.issparse(X):
+            dataloader = DataLoader(
+                SparsePredictDataset(X),
+                batch_size=self.batch_size,
+                shuffle=False,
+            )
+        else:
+            dataloader = DataLoader(
+                PredictDataset(X),
+                batch_size=self.batch_size,
+                shuffle=False,
+            )
 
         results = {}
         for data in dataloader:
             data = data.to(self.device).float()
             output, _ = self.network(data)
             predictions = [
                 torch.argmax(torch.nn.Softmax(dim=1)(task_output), dim=1)
@@ -128,29 +137,36 @@
 
     def predict_proba(self, X):
         """
         Make predictions for classification on a batch (valid)
 
         Parameters
         ----------
-        X : a :tensor: `torch.Tensor`
+        X : a :tensor: `torch.Tensor` or matrix: `scipy.sparse.csr_matrix`
             Input data
 
         Returns
         -------
         res : list of np.ndarray
 
         """
         self.network.eval()
 
-        dataloader = DataLoader(
-            PredictDataset(X),
-            batch_size=self.batch_size,
-            shuffle=False,
-        )
+        if scipy.sparse.issparse(X):
+            dataloader = DataLoader(
+                SparsePredictDataset(X),
+                batch_size=self.batch_size,
+                shuffle=False,
+            )
+        else:
+            dataloader = DataLoader(
+                PredictDataset(X),
+                batch_size=self.batch_size,
+                shuffle=False,
+            )
 
         results = {}
         for data in dataloader:
             data = data.to(self.device).float()
             output, _ = self.network(data)
             predictions = [
                 torch.nn.Softmax(dim=1)(task_output).cpu().detach().numpy()
```

### Comparing `pytorch_tabnet-4.0/pytorch_tabnet/pretraining.py` & `pytorch_tabnet-4.1.0/pytorch_tabnet/pretraining.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,28 +1,31 @@
 import torch
 import numpy as np
 from torch.utils.data import DataLoader
 from pytorch_tabnet import tab_network
 from pytorch_tabnet.utils import (
     create_explain_matrix,
     filter_weights,
+    SparsePredictDataset,
     PredictDataset,
-    check_input
+    check_input,
+    create_group_matrix,
 )
 from torch.nn.utils import clip_grad_norm_
 from pytorch_tabnet.pretraining_utils import (
     create_dataloaders,
     validate_eval_set,
 )
 from pytorch_tabnet.metrics import (
     UnsupMetricContainer,
     check_metrics,
     UnsupervisedLoss,
 )
 from pytorch_tabnet.abstract_model import TabModel
+import scipy
 
 
 class TabNetPretrainer(TabModel):
     def __post_init__(self):
         super(TabNetPretrainer, self).__post_init__()
         self._task = 'unsupervised'
         self._default_loss = UnsupervisedLoss
@@ -168,30 +171,36 @@
         self.network.eval()
 
     def _set_network(self):
         """Setup the network and explain matrix."""
         if not hasattr(self, 'pretraining_ratio'):
             self.pretraining_ratio = 0.5
         torch.manual_seed(self.seed)
+
+        self.group_matrix = create_group_matrix(self.grouped_features, self.input_dim)
+
         self.network = tab_network.TabNetPretraining(
             self.input_dim,
             pretraining_ratio=self.pretraining_ratio,
             n_d=self.n_d,
             n_a=self.n_a,
             n_steps=self.n_steps,
             gamma=self.gamma,
             cat_idxs=self.cat_idxs,
             cat_dims=self.cat_dims,
             cat_emb_dim=self.cat_emb_dim,
             n_independent=self.n_independent,
             n_shared=self.n_shared,
+            n_shared_decoder=self.n_shared_decoder,
+            n_indep_decoder=self.n_indep_decoder,
             epsilon=self.epsilon,
             virtual_batch_size=self.virtual_batch_size,
             momentum=self.momentum,
             mask_type=self.mask_type,
+            group_attention_matrix=self.group_matrix.to(self.device),
         ).to(self.device)
 
         self.reducing_matrix = create_explain_matrix(
             self.network.input_dim,
             self.network.cat_emb_dim,
             self.network.cat_idxs,
             self.network.post_embed_dim,
@@ -379,28 +388,36 @@
 
     def predict(self, X):
         """
         Make predictions on a batch (valid)
 
         Parameters
         ----------
-        X : a :tensor: `torch.Tensor`
+        X : a :tensor: `torch.Tensor` or matrix: `scipy.sparse.csr_matrix`
             Input data
 
         Returns
         -------
         predictions : np.array
             Predictions of the regression problem
         """
         self.network.eval()
-        dataloader = DataLoader(
-            PredictDataset(X),
-            batch_size=self.batch_size,
-            shuffle=False,
-        )
+
+        if scipy.sparse.issparse(X):
+            dataloader = DataLoader(
+                SparsePredictDataset(X),
+                batch_size=self.batch_size,
+                shuffle=False,
+            )
+        else:
+            dataloader = DataLoader(
+                PredictDataset(X),
+                batch_size=self.batch_size,
+                shuffle=False,
+            )
 
         results = []
         embedded_res = []
         for batch_nb, data in enumerate(dataloader):
             data = data.to(self.device).float()
             output, embeded_x, _ = self.network(data)
             predictions = output.cpu().detach().numpy()
```

### Comparing `pytorch_tabnet-4.0/pytorch_tabnet/pretraining_utils.py` & `pytorch_tabnet-4.1.0/pytorch_tabnet/pretraining_utils.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,26 +1,28 @@
 from torch.utils.data import DataLoader
 from pytorch_tabnet.utils import (
     create_sampler,
+    SparsePredictDataset,
     PredictDataset,
     check_input
 )
+import scipy
 
 
 def create_dataloaders(
     X_train, eval_set, weights, batch_size, num_workers, drop_last, pin_memory
 ):
     """
     Create dataloaders with or without subsampling depending on weights and balanced.
 
     Parameters
     ----------
-    X_train : np.ndarray
+    X_train : np.ndarray or scipy.sparse.csr_matrix
         Training data
-    eval_set : list of np.array
+    eval_set : list of np.array (for Xs and ys) or scipy.sparse.csr_matrix (for Xs)
         List of eval sets
     weights : either 0, 1, dict or iterable
         if 0 (default) : no weights will be applied
         if 1 : classification only, will balanced class with inverse frequency
         if dict : keys are corresponding class values are sample weights
         if iterable : list or np array must be of length equal to nb elements
                       in the training set
@@ -39,37 +41,61 @@
     Returns
     -------
     train_dataloader, valid_dataloader : torch.DataLoader, torch.DataLoader
         Training and validation dataloaders
     """
     need_shuffle, sampler = create_sampler(weights, X_train)
 
-    train_dataloader = DataLoader(
-        PredictDataset(X_train),
-        batch_size=batch_size,
-        sampler=sampler,
-        shuffle=need_shuffle,
-        num_workers=num_workers,
-        drop_last=drop_last,
-        pin_memory=pin_memory,
-    )
+    if scipy.sparse.issparse(X_train):
+        train_dataloader = DataLoader(
+            SparsePredictDataset(X_train),
+            batch_size=batch_size,
+            sampler=sampler,
+            shuffle=need_shuffle,
+            num_workers=num_workers,
+            drop_last=drop_last,
+            pin_memory=pin_memory,
+        )
+    else:
+        train_dataloader = DataLoader(
+            PredictDataset(X_train),
+            batch_size=batch_size,
+            sampler=sampler,
+            shuffle=need_shuffle,
+            num_workers=num_workers,
+            drop_last=drop_last,
+            pin_memory=pin_memory,
+        )
 
     valid_dataloaders = []
     for X in eval_set:
-        valid_dataloaders.append(
-            DataLoader(
-                PredictDataset(X),
-                batch_size=batch_size,
-                sampler=sampler,
-                shuffle=need_shuffle,
-                num_workers=num_workers,
-                drop_last=drop_last,
-                pin_memory=pin_memory,
+        if scipy.sparse.issparse(X):
+            valid_dataloaders.append(
+                DataLoader(
+                    SparsePredictDataset(X),
+                    batch_size=batch_size,
+                    sampler=sampler,
+                    shuffle=need_shuffle,
+                    num_workers=num_workers,
+                    drop_last=drop_last,
+                    pin_memory=pin_memory,
+                )
+            )
+        else:
+            valid_dataloaders.append(
+                DataLoader(
+                    PredictDataset(X),
+                    batch_size=batch_size,
+                    sampler=sampler,
+                    shuffle=need_shuffle,
+                    num_workers=num_workers,
+                    drop_last=drop_last,
+                    pin_memory=pin_memory,
+                )
             )
-        )
 
     return train_dataloader, valid_dataloaders
 
 
 def validate_eval_set(eval_set, eval_name, X_train):
     """Check if the shapes of eval_set are compatible with X_train.
```

### Comparing `pytorch_tabnet-4.0/pytorch_tabnet/sparsemax.py` & `pytorch_tabnet-4.1.0/pytorch_tabnet/sparsemax.py`

 * *Files identical despite different names*

### Comparing `pytorch_tabnet-4.0/pytorch_tabnet/tab_model.py` & `pytorch_tabnet-4.1.0/pytorch_tabnet/tab_model.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,14 +1,15 @@
 import torch
 import numpy as np
 from scipy.special import softmax
-from pytorch_tabnet.utils import PredictDataset, filter_weights
+from pytorch_tabnet.utils import SparsePredictDataset, PredictDataset, filter_weights
 from pytorch_tabnet.abstract_model import TabModel
 from pytorch_tabnet.multiclass_utils import infer_output_dim, check_output_dim
 from torch.utils.data import DataLoader
+import scipy
 
 
 class TabNetClassifier(TabModel):
     def __post_init__(self):
         super(TabNetClassifier, self).__post_init__()
         self._task = 'classification'
         self._default_loss = torch.nn.functional.cross_entropy
@@ -75,29 +76,36 @@
 
     def predict_proba(self, X):
         """
         Make predictions for classification on a batch (valid)
 
         Parameters
         ----------
-        X : a :tensor: `torch.Tensor`
+        X : a :tensor: `torch.Tensor` or matrix: `scipy.sparse.csr_matrix`
             Input data
 
         Returns
         -------
         res : np.ndarray
 
         """
         self.network.eval()
 
-        dataloader = DataLoader(
-            PredictDataset(X),
-            batch_size=self.batch_size,
-            shuffle=False,
-        )
+        if scipy.sparse.issparse(X):
+            dataloader = DataLoader(
+                SparsePredictDataset(X),
+                batch_size=self.batch_size,
+                shuffle=False,
+            )
+        else:
+            dataloader = DataLoader(
+                PredictDataset(X),
+                batch_size=self.batch_size,
+                shuffle=False,
+            )
 
         results = []
         for batch_nb, data in enumerate(dataloader):
             data = data.to(self.device).float()
 
             output, M_loss = self.network(data)
             predictions = torch.nn.Softmax(dim=1)(output).cpu().detach().numpy()
```

### Comparing `pytorch_tabnet-4.0/pytorch_tabnet/tab_network.py` & `pytorch_tabnet-4.1.0/pytorch_tabnet/tab_network.py`

 * *Files 22% similar despite different names*

```diff
@@ -49,14 +49,15 @@
         gamma=1.3,
         n_independent=2,
         n_shared=2,
         epsilon=1e-15,
         virtual_batch_size=128,
         momentum=0.02,
         mask_type="sparsemax",
+        group_attention_matrix=None,
     ):
         """
         Defines main part of the TabNet network without the embedding layers.
 
         Parameters
         ----------
         input_dim : int
@@ -80,14 +81,16 @@
             Avoid log(0), this should be kept very low
         virtual_batch_size : int
             Batch size for Ghost Batch Normalization
         momentum : float
             Float value between 0 and 1 which will be used for momentum in all batch norm
         mask_type : str
             Either "sparsemax" or "entmax" : this is the masking function to use
+        group_attention_matrix : torch matrix
+            Matrix of size (n_groups, input_dim), m_ij = importance within group i of feature j
         """
         super(TabNetEncoder, self).__init__()
         self.input_dim = input_dim
         self.output_dim = output_dim
         self.is_multi_task = isinstance(output_dim, list)
         self.n_d = n_d
         self.n_a = n_a
@@ -95,14 +98,22 @@
         self.gamma = gamma
         self.epsilon = epsilon
         self.n_independent = n_independent
         self.n_shared = n_shared
         self.virtual_batch_size = virtual_batch_size
         self.mask_type = mask_type
         self.initial_bn = BatchNorm1d(self.input_dim, momentum=0.01)
+        self.group_attention_matrix = group_attention_matrix
+
+        if self.group_attention_matrix is None:
+            # no groups
+            self.group_attention_matrix = torch.eye(self.input_dim)
+            self.attention_dim = self.input_dim
+        else:
+            self.attention_dim = self.group_attention_matrix.shape[0]
 
         if self.n_shared > 0:
             shared_feat_transform = torch.nn.ModuleList()
             for i in range(self.n_shared):
                 if i == 0:
                     shared_feat_transform.append(
                         Linear(self.input_dim, 2 * (n_d + n_a), bias=False)
@@ -134,70 +145,73 @@
                 shared_feat_transform,
                 n_glu_independent=self.n_independent,
                 virtual_batch_size=self.virtual_batch_size,
                 momentum=momentum,
             )
             attention = AttentiveTransformer(
                 n_a,
-                self.input_dim,
+                self.attention_dim,
+                group_matrix=group_attention_matrix,
                 virtual_batch_size=self.virtual_batch_size,
                 momentum=momentum,
                 mask_type=self.mask_type,
             )
             self.feat_transformers.append(transformer)
             self.att_transformers.append(attention)
 
     def forward(self, x, prior=None):
         x = self.initial_bn(x)
 
+        bs = x.shape[0]  # batch size
         if prior is None:
-            prior = torch.ones(x.shape).to(x.device)
+            prior = torch.ones((bs, self.attention_dim)).to(x.device)
 
         M_loss = 0
         att = self.initial_splitter(x)[:, self.n_d :]
-
         steps_output = []
         for step in range(self.n_steps):
             M = self.att_transformers[step](prior, att)
             M_loss += torch.mean(
                 torch.sum(torch.mul(M, torch.log(M + self.epsilon)), dim=1)
             )
             # update prior
             prior = torch.mul(self.gamma - M, prior)
             # output
-            masked_x = torch.mul(M, x)
+            M_feature_level = torch.matmul(M, self.group_attention_matrix)
+            masked_x = torch.mul(M_feature_level, x)
             out = self.feat_transformers[step](masked_x)
             d = ReLU()(out[:, : self.n_d])
             steps_output.append(d)
             # update attention
             att = out[:, self.n_d :]
 
         M_loss /= self.n_steps
         return steps_output, M_loss
 
     def forward_masks(self, x):
         x = self.initial_bn(x)
-
-        prior = torch.ones(x.shape).to(x.device)
+        bs = x.shape[0]  # batch size
+        prior = torch.ones((bs, self.attention_dim)).to(x.device)
         M_explain = torch.zeros(x.shape).to(x.device)
         att = self.initial_splitter(x)[:, self.n_d :]
         masks = {}
 
         for step in range(self.n_steps):
             M = self.att_transformers[step](prior, att)
-            masks[step] = M
+            M_feature_level = torch.matmul(M, self.group_attention_matrix)
+            masks[step] = M_feature_level
             # update prior
             prior = torch.mul(self.gamma - M, prior)
             # output
-            masked_x = torch.mul(M, x)
+            masked_x = torch.mul(M_feature_level, x)
             out = self.feat_transformers[step](masked_x)
             d = ReLU()(out[:, : self.n_d])
             # explain
             step_importance = torch.sum(d, dim=1)
-            M_explain += torch.mul(M, step_importance.unsqueeze(dim=1))
+            M_explain += torch.mul(M_feature_level, step_importance.unsqueeze(dim=1))
             # update attention
             att = out[:, self.n_d :]
 
         return M_explain, masks
 
 
 class TabNetDecoder(torch.nn.Module):
@@ -245,19 +259,15 @@
         self.virtual_batch_size = virtual_batch_size
 
         self.feat_transformers = torch.nn.ModuleList()
 
         if self.n_shared > 0:
             shared_feat_transform = torch.nn.ModuleList()
             for i in range(self.n_shared):
-                if i == 0:
-                    shared_feat_transform.append(Linear(n_d, 2 * n_d, bias=False))
-                else:
-                    shared_feat_transform.append(Linear(n_d, 2 * n_d, bias=False))
-
+                shared_feat_transform.append(Linear(n_d, 2 * n_d, bias=False))
         else:
             shared_feat_transform = None
 
         for step in range(n_steps):
             transformer = FeatTransformer(
                 n_d,
                 n_d,
@@ -296,14 +306,15 @@
         n_shared=2,
         epsilon=1e-15,
         virtual_batch_size=128,
         momentum=0.02,
         mask_type="sparsemax",
         n_shared_decoder=1,
         n_indep_decoder=1,
+        group_attention_matrix=None,
     ):
         super(TabNetPretraining, self).__init__()
 
         self.cat_idxs = cat_idxs or []
         self.cat_dims = cat_dims or []
         self.cat_emb_dim = cat_emb_dim
 
@@ -322,31 +333,37 @@
 
         if self.n_steps <= 0:
             raise ValueError("n_steps should be a positive integer.")
         if self.n_independent == 0 and self.n_shared == 0:
             raise ValueError("n_shared and n_independent can't be both zero.")
 
         self.virtual_batch_size = virtual_batch_size
-        self.embedder = EmbeddingGenerator(input_dim, cat_dims, cat_idxs, cat_emb_dim)
+        self.embedder = EmbeddingGenerator(input_dim,
+                                           cat_dims,
+                                           cat_idxs,
+                                           cat_emb_dim,
+                                           group_attention_matrix)
         self.post_embed_dim = self.embedder.post_embed_dim
 
-        self.masker = RandomObfuscator(self.pretraining_ratio)
+        self.masker = RandomObfuscator(self.pretraining_ratio,
+                                       group_matrix=self.embedder.embedding_group_matrix)
         self.encoder = TabNetEncoder(
             input_dim=self.post_embed_dim,
             output_dim=self.post_embed_dim,
             n_d=n_d,
             n_a=n_a,
             n_steps=n_steps,
             gamma=gamma,
             n_independent=n_independent,
             n_shared=n_shared,
             epsilon=epsilon,
             virtual_batch_size=virtual_batch_size,
             momentum=momentum,
             mask_type=mask_type,
+            group_attention_matrix=self.embedder.embedding_group_matrix,
         )
         self.decoder = TabNetDecoder(
             self.post_embed_dim,
             n_d=n_d,
             n_steps=n_steps,
             n_independent=self.n_indep_decoder,
             n_shared=self.n_shared_decoder,
@@ -359,20 +376,20 @@
         Returns: res, embedded_x, obf_vars
             res : output of reconstruction
             embedded_x : embedded input
             obf_vars : which variable where obfuscated
         """
         embedded_x = self.embedder(x)
         if self.training:
-            masked_x, obf_vars = self.masker(embedded_x)
-            # set prior of encoder with obf_mask
-            prior = 1 - obf_vars
+            masked_x, obfuscated_groups, obfuscated_vars = self.masker(embedded_x)
+            # set prior of encoder with obfuscated groups
+            prior = 1 - obfuscated_groups
             steps_out, _ = self.encoder(masked_x, prior=prior)
             res = self.decoder(steps_out)
-            return res, embedded_x, obf_vars
+            return res, embedded_x, obfuscated_vars
         else:
             steps_out, _ = self.encoder(embedded_x)
             res = self.decoder(steps_out)
             return res, embedded_x, torch.ones(embedded_x.shape).to(x.device)
 
     def forward_masks(self, x):
         embedded_x = self.embedder(x)
@@ -390,14 +407,15 @@
         gamma=1.3,
         n_independent=2,
         n_shared=2,
         epsilon=1e-15,
         virtual_batch_size=128,
         momentum=0.02,
         mask_type="sparsemax",
+        group_attention_matrix=None,
     ):
         """
         Defines main part of the TabNet network without the embedding layers.
 
         Parameters
         ----------
         input_dim : int
@@ -421,14 +439,16 @@
             Avoid log(0), this should be kept very low
         virtual_batch_size : int
             Batch size for Ghost Batch Normalization
         momentum : float
             Float value between 0 and 1 which will be used for momentum in all batch norm
         mask_type : str
             Either "sparsemax" or "entmax" : this is the masking function to use
+        group_attention_matrix : torch matrix
+            Matrix of size (n_groups, input_dim), m_ij = importance within group i of feature j
         """
         super(TabNetNoEmbeddings, self).__init__()
         self.input_dim = input_dim
         self.output_dim = output_dim
         self.is_multi_task = isinstance(output_dim, list)
         self.n_d = n_d
         self.n_a = n_a
@@ -450,14 +470,15 @@
             gamma=gamma,
             n_independent=n_independent,
             n_shared=n_shared,
             epsilon=epsilon,
             virtual_batch_size=virtual_batch_size,
             momentum=momentum,
             mask_type=mask_type,
+            group_attention_matrix=group_attention_matrix
         )
 
         if self.is_multi_task:
             self.multi_task_mappings = torch.nn.ModuleList()
             for task_dim in output_dim:
                 task_mapping = Linear(n_d, task_dim, bias=False)
                 initialize_non_glu(task_mapping, n_d, task_dim)
@@ -498,14 +519,15 @@
         cat_emb_dim=1,
         n_independent=2,
         n_shared=2,
         epsilon=1e-15,
         virtual_batch_size=128,
         momentum=0.02,
         mask_type="sparsemax",
+        group_attention_matrix=[],
     ):
         """
         Defines TabNet network
 
         Parameters
         ----------
         input_dim : int
@@ -537,14 +559,16 @@
             Avoid log(0), this should be kept very low
         virtual_batch_size : int
             Batch size for Ghost Batch Normalization
         momentum : float
             Float value between 0 and 1 which will be used for momentum in all batch norm
         mask_type : str
             Either "sparsemax" or "entmax" : this is the masking function to use
+        group_attention_matrix : torch matrix
+            Matrix of size (n_groups, input_dim), m_ij = importance within group i of feature j
         """
         super(TabNet, self).__init__()
         self.cat_idxs = cat_idxs or []
         self.cat_dims = cat_dims or []
         self.cat_emb_dim = cat_emb_dim
 
         self.input_dim = input_dim
@@ -560,29 +584,35 @@
 
         if self.n_steps <= 0:
             raise ValueError("n_steps should be a positive integer.")
         if self.n_independent == 0 and self.n_shared == 0:
             raise ValueError("n_shared and n_independent can't be both zero.")
 
         self.virtual_batch_size = virtual_batch_size
-        self.embedder = EmbeddingGenerator(input_dim, cat_dims, cat_idxs, cat_emb_dim)
+        self.embedder = EmbeddingGenerator(input_dim,
+                                           cat_dims,
+                                           cat_idxs,
+                                           cat_emb_dim,
+                                           group_attention_matrix)
         self.post_embed_dim = self.embedder.post_embed_dim
+
         self.tabnet = TabNetNoEmbeddings(
             self.post_embed_dim,
             output_dim,
             n_d,
             n_a,
             n_steps,
             gamma,
             n_independent,
             n_shared,
             epsilon,
             virtual_batch_size,
             momentum,
             mask_type,
+            self.embedder.embedding_group_matrix
         )
 
     def forward(self, x):
         x = self.embedder(x)
         return self.tabnet(x)
 
     def forward_masks(self, x):
@@ -590,40 +620,41 @@
         return self.tabnet.forward_masks(x)
 
 
 class AttentiveTransformer(torch.nn.Module):
     def __init__(
         self,
         input_dim,
-        output_dim,
+        group_dim,
+        group_matrix,
         virtual_batch_size=128,
         momentum=0.02,
         mask_type="sparsemax",
     ):
         """
         Initialize an attention transformer.
 
         Parameters
         ----------
         input_dim : int
             Input size
-        output_dim : int
-            Output_size
+        group_dim : int
+            Number of groups for features
         virtual_batch_size : int
             Batch size for Ghost Batch Normalization
         momentum : float
             Float value between 0 and 1 which will be used for momentum in batch norm
         mask_type : str
             Either "sparsemax" or "entmax" : this is the masking function to use
         """
         super(AttentiveTransformer, self).__init__()
-        self.fc = Linear(input_dim, output_dim, bias=False)
-        initialize_non_glu(self.fc, input_dim, output_dim)
+        self.fc = Linear(input_dim, group_dim, bias=False)
+        initialize_non_glu(self.fc, input_dim, group_dim)
         self.bn = GBN(
-            output_dim, virtual_batch_size=virtual_batch_size, momentum=momentum
+            group_dim, virtual_batch_size=virtual_batch_size, momentum=momentum
         )
 
         if mask_type == "sparsemax":
             # Sparsemax
             self.selector = sparsemax.Sparsemax(dim=-1)
         elif mask_type == "entmax":
             # Entmax
@@ -776,74 +807,72 @@
 
 
 class EmbeddingGenerator(torch.nn.Module):
     """
     Classical embeddings generator
     """
 
-    def __init__(self, input_dim, cat_dims, cat_idxs, cat_emb_dim):
+    def __init__(self, input_dim, cat_dims, cat_idxs, cat_emb_dims, group_matrix):
         """This is an embedding module for an entire set of features
 
         Parameters
         ----------
         input_dim : int
             Number of features coming as input (number of columns)
         cat_dims : list of int
             Number of modalities for each categorial features
             If the list is empty, no embeddings will be done
         cat_idxs : list of int
             Positional index for each categorical features in inputs
-        cat_emb_dim : int or list of int
+        cat_emb_dim : list of int
             Embedding dimension for each categorical features
             If int, the same embedding dimension will be used for all categorical features
+        group_matrix : torch matrix
+            Original group matrix before embeddings
         """
         super(EmbeddingGenerator, self).__init__()
+
         if cat_dims == [] and cat_idxs == []:
             self.skip_embedding = True
             self.post_embed_dim = input_dim
+            self.embedding_group_matrix = group_matrix.to(group_matrix.device)
             return
-        elif (cat_dims == []) ^ (cat_idxs == []):
-            if cat_dims == []:
-                msg = "If cat_idxs is non-empty, cat_dims must be defined as a list of same length."
-            else:
-                msg = "If cat_dims is non-empty, cat_idxs must be defined as a list of same length."
-            raise ValueError(msg)
-        elif len(cat_dims) != len(cat_idxs):
-            msg = "The lists cat_dims and cat_idxs must have the same length."
-            raise ValueError(msg)
-
-        self.skip_embedding = False
-        if isinstance(cat_emb_dim, int):
-            self.cat_emb_dims = [cat_emb_dim] * len(cat_idxs)
-        else:
-            self.cat_emb_dims = cat_emb_dim
-
-        # check that all embeddings are provided
-        if len(self.cat_emb_dims) != len(cat_dims):
-            msg = f"""cat_emb_dim and cat_dims must be lists of same length, got {len(self.cat_emb_dims)}
-                      and {len(cat_dims)}"""
-            raise ValueError(msg)
-        self.post_embed_dim = int(
-            input_dim + np.sum(self.cat_emb_dims) - len(self.cat_emb_dims)
-        )
+        else:
+            self.skip_embedding = False
 
-        self.embeddings = torch.nn.ModuleList()
+        self.post_embed_dim = int(input_dim + np.sum(cat_emb_dims) - len(cat_emb_dims))
 
-        # Sort dims by cat_idx
-        sorted_idxs = np.argsort(cat_idxs)
-        cat_dims = [cat_dims[i] for i in sorted_idxs]
-        self.cat_emb_dims = [self.cat_emb_dims[i] for i in sorted_idxs]
+        self.embeddings = torch.nn.ModuleList()
 
-        for cat_dim, emb_dim in zip(cat_dims, self.cat_emb_dims):
+        for cat_dim, emb_dim in zip(cat_dims, cat_emb_dims):
             self.embeddings.append(torch.nn.Embedding(cat_dim, emb_dim))
 
         # record continuous indices
         self.continuous_idx = torch.ones(input_dim, dtype=torch.bool)
         self.continuous_idx[cat_idxs] = 0
 
+        # update group matrix
+        n_groups = group_matrix.shape[0]
+        self.embedding_group_matrix = torch.empty((n_groups, self.post_embed_dim),
+                                                  device=group_matrix.device)
+        for group_idx in range(n_groups):
+            post_emb_idx = 0
+            cat_feat_counter = 0
+            for init_feat_idx in range(input_dim):
+                if self.continuous_idx[init_feat_idx] == 1:
+                    # this means that no embedding is applied to this column
+                    self.embedding_group_matrix[group_idx, post_emb_idx] = group_matrix[group_idx, init_feat_idx]  # noqa
+                    post_emb_idx += 1
+                else:
+                    # this is a categorical feature which creates multiple embeddings
+                    n_embeddings = cat_emb_dims[cat_feat_counter]
+                    self.embedding_group_matrix[group_idx, post_emb_idx:post_emb_idx+n_embeddings] = group_matrix[group_idx, init_feat_idx] / n_embeddings  # noqa
+                    post_emb_idx += n_embeddings
+                    cat_feat_counter += 1
+
     def forward(self, x):
         """
         Apply embeddings to inputs
         Inputs should be (batch_size, input_dim)
         Outputs will be of size (batch_size, self.post_embed_dim)
         """
         if self.skip_embedding:
@@ -864,34 +893,42 @@
         # concat
         post_embeddings = torch.cat(cols, dim=1)
         return post_embeddings
 
 
 class RandomObfuscator(torch.nn.Module):
     """
-    Create and applies obfuscation masks
+    Create and applies obfuscation masks.
+    The obfuscation is done at group level to match attention.
     """
 
-    def __init__(self, pretraining_ratio):
+    def __init__(self, pretraining_ratio, group_matrix):
         """
         This create random obfuscation for self suppervised pretraining
         Parameters
         ----------
         pretraining_ratio : float
             Ratio of feature to randomly discard for reconstruction
+
         """
         super(RandomObfuscator, self).__init__()
         self.pretraining_ratio = pretraining_ratio
+        # group matrix is set to boolean here to pass all posssible information
+        self.group_matrix = (group_matrix > 0) + 0.
+        self.num_groups = group_matrix.shape[0]
 
     def forward(self, x):
         """
         Generate random obfuscation mask.
 
         Returns
         -------
         masked input and obfuscated variables.
         """
-        obfuscated_vars = torch.bernoulli(
-            self.pretraining_ratio * torch.ones(x.shape)
-        ).to(x.device)
+        bs = x.shape[0]
+
+        obfuscated_groups = torch.bernoulli(
+            self.pretraining_ratio * torch.ones((bs, self.num_groups), device=x.device)
+        )
+        obfuscated_vars = torch.matmul(obfuscated_groups, self.group_matrix)
         masked_input = torch.mul(1 - obfuscated_vars, x)
-        return masked_input, obfuscated_vars
+        return masked_input, obfuscated_groups, obfuscated_vars
```

### Comparing `pytorch_tabnet-4.0/setup.py` & `pytorch_tabnet-4.1.0/setup.py`

 * *Files 4% similar despite different names*

```diff
@@ -4,31 +4,27 @@
 packages = \
 ['pytorch_tabnet']
 
 package_data = \
 {'': ['*']}
 
 install_requires = \
-['numpy>=1.17,<2.0',
- 'scikit_learn>0.21',
- 'scipy>1.4',
- 'torch>=1.2,<2.0',
- 'tqdm>=4.36,<5.0']
+['numpy>=1.17', 'scikit_learn>0.21', 'scipy>1.4', 'torch>=1.3', 'tqdm>=4.36']
 
 setup_kwargs = {
     'name': 'pytorch-tabnet',
-    'version': '4.0',
+    'version': '4.1.0',
     'description': 'PyTorch implementation of TabNet',
-    'long_description': '# README\n\n# TabNet : Attentive Interpretable Tabular Learning\n\nThis is a pyTorch implementation of Tabnet (Arik, S. O., & Pfister, T. (2019). TabNet: Attentive Interpretable Tabular Learning. arXiv preprint arXiv:1908.07442.) https://arxiv.org/pdf/1908.07442.pdf.\n\n<!--- BADGES: START --->\n[![CircleCI](https://circleci.com/gh/dreamquark-ai/tabnet.svg?style=svg)](https://circleci.com/gh/dreamquark-ai/tabnet)\n\n[![PyPI version](https://badge.fury.io/py/pytorch-tabnet.svg)](https://badge.fury.io/py/pytorch-tabnet)\n\n![PyPI - Downloads](https://img.shields.io/pypi/dm/pytorch-tabnet)\n\n[![PyPI - Python Version](https://img.shields.io/pypi/pyversions/pytorch-tabnet?logo=pypi&style=flat&color=blue)][#pypi-package]\n\n[![Conda - Platform](https://img.shields.io/conda/pn/conda-forge/pytorch-tabnet?logo=anaconda&style=flat)][#conda-forge-package]\n\n[![Conda (channel only)](https://img.shields.io/conda/vn/conda-forge/pytorch-tabnet?logo=anaconda&style=flat&color=orange)][#conda-forge-package]\n\n[![GitHub - License](https://img.shields.io/github/license/dreamquark-ai/tabnet?logo=github&style=flat&color=green)][#github-license]\n\n[#github-license]: https://github.com/dreamquark-ai/tabnet/blob/main/LICENSE\n[#pypi-package]: https://pypi.org/project/pytorch-tabnet/\n[#conda-forge-package]: https://anaconda.org/conda-forge/pytorch-tabnet\n<!--- BADGES: END --->\n\nAny questions ? Want to contribute ? To talk with us ? You can join us on [Slack](https://join.slack.com/t/mltooling/shared_invite/zt-fxaj0qk7-SWy2_~EWyhj4x9SD6gbRvg)\n\n# Installation\n\n## Easy installation\n\nYou can install using `pip` or `conda` as follows.\n\n**with pip**\n\n```sh\npip install pytorch-tabnet\n```\n\n**with conda**\n\n```sh\nconda install -c conda-forge pytorch-tabnet\n```\n\n## Source code\n\nIf you wan to use it locally within a docker container:\n\n- `git clone git@github.com:dreamquark-ai/tabnet.git`\n\n- `cd tabnet` to get inside the repository\n\n-----------------\n\n#### CPU only\n\n- `make start` to build and get inside the container\n\n#### GPU\n\n- `make start-gpu` to build and get inside the GPU container\n\n-----------------\n\n- `poetry install` to install all the dependencies, including jupyter\n\n- `make notebook` inside the same terminal. You can then follow the link to a jupyter notebook with tabnet installed.\n\n# Contributing\n\nWhen contributing to the TabNet repository, please make sure to first discuss the change you wish to make via a new or already existing issue.\n\nOur commits follow the rules presented [here](https://www.conventionalcommits.org/en/v1.0.0/).\n\n# What problems does pytorch-tabnet handle?\n\n- TabNetClassifier : binary classification and multi-class classification problems\n- TabNetRegressor : simple and multi-task regression problems\n- TabNetMultiTaskClassifier:  multi-task multi-classification problems\n\n# How to use it?\n\nTabNet is now scikit-compatible, training a TabNetClassifier or TabNetRegressor is really easy.\n\n```python\nfrom pytorch_tabnet.tab_model import TabNetClassifier, TabNetRegressor\n\nclf = TabNetClassifier()  #TabNetRegressor()\nclf.fit(\n  X_train, Y_train,\n  eval_set=[(X_valid, y_valid)]\n)\npreds = clf.predict(X_test)\n```\n\nor for TabNetMultiTaskClassifier :\n\n```python\nfrom pytorch_tabnet.multitask import TabNetMultiTaskClassifier\nclf = TabNetMultiTaskClassifier()\nclf.fit(\n  X_train, Y_train,\n  eval_set=[(X_valid, y_valid)]\n)\npreds = clf.predict(X_test)\n```\n\nThe targets on `y_train/y_valid` should contain a unique type (e.g. they must all be strings or integers).\n\n### Default eval_metric\n\nA few classic evaluation metrics are implemented (see further below for custom ones):\n- binary classification metrics : \'auc\', \'accuracy\', \'balanced_accuracy\', \'logloss\'\n- multiclass classification : \'accuracy\', \'balanced_accuracy\', \'logloss\'\n- regression: \'mse\', \'mae\', \'rmse\', \'rmsle\'\n\n\nImportant Note : \'rmsle\' will automatically clip negative predictions to 0, because the model can predict negative values.\nIn order to match the given scores, you need to use `np.clip(clf.predict(X_predict), a_min=0, a_max=None)` when doing predictions.\n\n\n### Custom evaluation metrics\n\nYou can create a metric for your specific need. Here is an example for gini score (note that you need to specifiy whether this metric should be maximized or not):\n\n```python\nfrom pytorch_tabnet.metrics import Metric\nfrom sklearn.metrics import roc_auc_score\n\nclass Gini(Metric):\n    def __init__(self):\n        self._name = "gini"\n        self._maximize = True\n\n    def __call__(self, y_true, y_score):\n        auc = roc_auc_score(y_true, y_score[:, 1])\n        return max(2*auc - 1, 0.)\n\nclf = TabNetClassifier()\nclf.fit(\n  X_train, Y_train,\n  eval_set=[(X_valid, y_valid)],\n  eval_metric=[Gini]\n)\n\n```\n\nA specific customization example notebook is available here : https://github.com/dreamquark-ai/tabnet/blob/develop/customizing_example.ipynb\n\n# Semi-supervised pre-training\n\nAdded later to TabNet\'s original paper, semi-supervised pre-training is now available via the class `TabNetPretrainer`:\n\n```python\n# TabNetPretrainer\nunsupervised_model = TabNetPretrainer(\n    optimizer_fn=torch.optim.Adam,\n    optimizer_params=dict(lr=2e-2),\n    mask_type=\'entmax\' # "sparsemax"\n)\n\nunsupervised_model.fit(\n    X_train=X_train,\n    eval_set=[X_valid],\n    pretraining_ratio=0.8,\n)\n\nclf = TabNetClassifier(\n    optimizer_fn=torch.optim.Adam,\n    optimizer_params=dict(lr=2e-2),\n    scheduler_params={"step_size":10, # how to use learning rate scheduler\n                      "gamma":0.9},\n    scheduler_fn=torch.optim.lr_scheduler.StepLR,\n    mask_type=\'sparsemax\' # This will be overwritten if using pretrain model\n)\n\nclf.fit(\n    X_train=X_train, y_train=y_train,\n    eval_set=[(X_train, y_train), (X_valid, y_valid)],\n    eval_name=[\'train\', \'valid\'],\n    eval_metric=[\'auc\'],\n    from_unsupervised=unsupervised_model\n)\n```\n\nThe loss function has been normalized to be independent of `pretraining_ratio`, `batch_size` and the number of features in the problem.\nA self supervised loss greater than 1 means that your model is reconstructing worse than predicting the mean for each feature, a loss bellow 1 means that the model is doing better than predicting the mean.\n\nA complete example can be found within the notebook `pretraining_example.ipynb`.\n\n/!\\ : current implementation is trying to reconstruct the original inputs, but Batch Normalization applies a random transformation that can\'t be deduced by a single line, making the reconstruction harder. Lowering the `batch_size` might make the pretraining easier.\n\n# Data augmentation on the fly\n\nIt is now possible to apply custom data augmentation pipeline during training.\nTemplates for ClassificationSMOTE and RegressionSMOTE have been added in `pytorch-tabnet/augmentations.py` and can be used as is.\n\n\n# Easy saving and loading\n\nIt\'s really easy to save and re-load a trained model, this makes TabNet production ready.\n```\n# save tabnet model\nsaving_path_name = "./tabnet_model_test_1"\nsaved_filepath = clf.save_model(saving_path_name)\n\n# define new model with basic parameters and load state dict weights\nloaded_clf = TabNetClassifier()\nloaded_clf.load_model(saved_filepath)\n```\n\n# Useful links\n\n- [explanatory video](https://youtu.be/ysBaZO8YmX8)\n- [binary classification examples](https://github.com/dreamquark-ai/tabnet/blob/develop/census_example.ipynb)\n- [multi-class classification examples](https://github.com/dreamquark-ai/tabnet/blob/develop/forest_example.ipynb)\n- [regression examples](https://github.com/dreamquark-ai/tabnet/blob/develop/regression_example.ipynb)\n- [multi-task regression examples](https://github.com/dreamquark-ai/tabnet/blob/develop/multi_regression_example.ipynb)\n- [multi-task multi-class classification examples](https://www.kaggle.com/optimo/tabnetmultitaskclassifier)\n- [kaggle moa 1st place solution using tabnet](https://www.kaggle.com/c/lish-moa/discussion/201510)\n\n## Model parameters\n\n- `n_d` : int (default=8)\n\n    Width of the decision prediction layer. Bigger values gives more capacity to the model with the risk of overfitting.\n    Values typically range from 8 to 64.\n\n- `n_a`: int (default=8)\n\n    Width of the attention embedding for each mask.\n    According to the paper n_d=n_a is usually a good choice. (default=8)\n\n- `n_steps` : int (default=3)\n\n    Number of steps in the architecture (usually between 3 and 10)  \n\n- `gamma` : float  (default=1.3)\n\n    This is the coefficient for feature reusage in the masks.\n    A value close to 1 will make mask selection least correlated between layers.\n    Values range from 1.0 to 2.0.\n\n- `cat_idxs` : list of int (default=[] - Mandatory for embeddings) \n\n    List of categorical features indices.\n\n- `cat_dims` : list of int (default=[] - Mandatory for embeddings)\n\n    List of categorical features number of modalities (number of unique values for a categorical feature)\n    /!\\ no new modalities can be predicted\n\n- `cat_emb_dim` : list of int (optional)\n\n    List of embeddings size for each categorical features. (default =1)\n\n- `n_independent` : int  (default=2)\n\n    Number of independent Gated Linear Units layers at each step.\n    Usual values range from 1 to 5.\n\n- `n_shared` : int (default=2)\n\n    Number of shared Gated Linear Units at each step\n    Usual values range from 1 to 5\n\n- `epsilon` : float  (default 1e-15)\n\n    Should be left untouched.\n\n- `seed` : int (default=0)\n\n    Random seed for reproducibility\n\n- `momentum` : float\n\n    Momentum for batch normalization, typically ranges from 0.01 to 0.4 (default=0.02)\n\n- `clip_value` : float (default None)\n\n    If a float is given this will clip the gradient at clip_value.\n    \n- `lambda_sparse` : float (default = 1e-3)\n\n    This is the extra sparsity loss coefficient as proposed in the original paper. The bigger this coefficient is, the sparser your model will be in terms of feature selection. Depending on the difficulty of your problem, reducing this value could help.\n\n- `optimizer_fn` : torch.optim (default=torch.optim.Adam)\n\n    Pytorch optimizer function\n\n- `optimizer_params`: dict (default=dict(lr=2e-2))\n\n    Parameters compatible with optimizer_fn used initialize the optimizer. Since we have Adam as our default optimizer, we use this to define the initial learning rate used for training. As mentionned in the original paper, a large initial learning rate of ```0.02 ```  with decay is a good option.\n\n- `scheduler_fn` : torch.optim.lr_scheduler (default=None)\n\n    Pytorch Scheduler to change learning rates during training.\n\n- `scheduler_params` : dict\n\n    Dictionnary of parameters to apply to the scheduler_fn. Ex : {"gamma": 0.95, "step_size": 10}\n\n- `model_name` : str (default = \'DreamQuarkTabNet\')\n\n    Name of the model used for saving in disk, you can customize this to easily retrieve and reuse your trained models.\n\n- `verbose` : int (default=1)\n\n    Verbosity for notebooks plots, set to 1 to see every epoch, 0 to get None.\n\n- `device_name` : str (default=\'auto\')\n    \'cpu\' for cpu training, \'gpu\' for gpu training, \'auto\' to automatically detect gpu.\n\n- `mask_type: str` (default=\'sparsemax\')\n    Either "sparsemax" or "entmax" : this is the masking function to use for selecting features.\n\n- `n_shared_decoder` : int (default=1)\n\n    Number of shared GLU block in decoder, this is only useful for `TabNetPretrainer`.\n\n- `n_indep_decoder` : int (default=1)\n\n    Number of independent GLU block in decoder, this is only useful for `TabNetPretrainer`.\n\n## Fit parameters\n\n- `X_train` : np.array\n\n    Training features\n\n- `y_train` : np.array\n\n    Training targets\n\n- `eval_set`: list of tuple  \n\n    List of eval tuple set (X, y).  \n    The last one is used for early stopping  \n\n- `eval_name`: list of str  \n              List of eval set names.  \n\n- `eval_metric` : list of str  \n              List of evaluation metrics.  \n              The last metric is used for early stopping.\n\n- `max_epochs` : int (default = 200)\n\n    Maximum number of epochs for trainng.\n    \n- `patience` : int (default = 10)\n\n    Number of consecutive epochs without improvement before performing early stopping.\n\n    If patience is set to 0, then no early stopping will be performed.\n\n    Note that if patience is enabled, then best weights from best epoch will automatically be loaded at the end of `fit`.\n\n- `weights` : int or dict (default=0)\n\n    /!\\ Only for TabNetClassifier\n    Sampling parameter\n    0 : no sampling\n    1 : automated sampling with inverse class occurrences\n    dict : keys are classes, values are weights for each class\n\n- `loss_fn` : torch.loss or list of torch.loss\n\n    Loss function for training (default to mse for regression and cross entropy for classification)\n    When using TabNetMultiTaskClassifier you can set a list of same length as number of tasks,\n    each task will be assigned its own loss function\n\n- `batch_size` : int (default=1024)\n\n    Number of examples per batch. Large batch sizes are recommended.\n\n- `virtual_batch_size` : int (default=128)\n\n    Size of the mini batches used for "Ghost Batch Normalization".\n    /!\\ `virtual_batch_size` should divide `batch_size`\n\n- `num_workers` : int (default=0)\n\n    Number or workers used in torch.utils.data.Dataloader\n\n- `drop_last` : bool (default=False)\n\n    Whether to drop last batch if not complete during training\n\n- `callbacks` : list of callback function  \n        List of custom callbacks\n\n- `pretraining_ratio` : float\n\n        /!\\ TabNetPretrainer Only : Percentage of input features to mask during pretraining.\n\n        Should be between 0 and 1. The bigger the harder the reconstruction task is.\n\n- `warm_start` : bool (default=False)\n    In order to match scikit-learn API, this is set to False.\n    It allows to fit twice the same model and start from a warm start.\n',
+    'long_description': '# README\n\n# TabNet : Attentive Interpretable Tabular Learning\n\nThis is a pyTorch implementation of Tabnet (Arik, S. O., & Pfister, T. (2019). TabNet: Attentive Interpretable Tabular Learning. arXiv preprint arXiv:1908.07442.) https://arxiv.org/pdf/1908.07442.pdf. Please note that some different choices have been made overtime to improve the library which can differ from the orginal paper.\n\n<!--- BADGES: START --->\n[![CircleCI](https://circleci.com/gh/dreamquark-ai/tabnet.svg?style=svg)](https://circleci.com/gh/dreamquark-ai/tabnet)\n\n[![PyPI version](https://badge.fury.io/py/pytorch-tabnet.svg)](https://badge.fury.io/py/pytorch-tabnet)\n\n![PyPI - Downloads](https://img.shields.io/pypi/dm/pytorch-tabnet)\n\n[![PyPI - Python Version](https://img.shields.io/pypi/pyversions/pytorch-tabnet?logo=pypi&style=flat&color=blue)][#pypi-package]\n\n[![Conda - Platform](https://img.shields.io/conda/pn/conda-forge/pytorch-tabnet?logo=anaconda&style=flat)][#conda-forge-package]\n\n[![Conda (channel only)](https://img.shields.io/conda/vn/conda-forge/pytorch-tabnet?logo=anaconda&style=flat&color=orange)][#conda-forge-package]\n\n[![GitHub - License](https://img.shields.io/github/license/dreamquark-ai/tabnet?logo=github&style=flat&color=green)][#github-license]\n\n[#github-license]: https://github.com/dreamquark-ai/tabnet/blob/main/LICENSE\n[#pypi-package]: https://pypi.org/project/pytorch-tabnet/\n[#conda-forge-package]: https://anaconda.org/conda-forge/pytorch-tabnet\n<!--- BADGES: END --->\n\nAny questions ? Want to contribute ? To talk with us ? You can join us on [Slack](https://join.slack.com/t/mltooling/shared_invite/zt-fxaj0qk7-SWy2_~EWyhj4x9SD6gbRvg)\n\n# Installation\n\n## Easy installation\n\nYou can install using `pip` or `conda` as follows.\n\n**with pip**\n\n```sh\npip install pytorch-tabnet\n```\n\n**with conda**\n\n```sh\nconda install -c conda-forge pytorch-tabnet\n```\n\n## Source code\n\nIf you wan to use it locally within a docker container:\n\n- `git clone git@github.com:dreamquark-ai/tabnet.git`\n\n- `cd tabnet` to get inside the repository\n\n-----------------\n\n#### CPU only\n\n- `make start` to build and get inside the container\n\n#### GPU\n\n- `make start-gpu` to build and get inside the GPU container\n\n-----------------\n\n- `poetry install` to install all the dependencies, including jupyter\n\n- `make notebook` inside the same terminal. You can then follow the link to a jupyter notebook with tabnet installed.\n\n# What is new ?\n\n- from version **> 4.0** attention is now embedding aware. This aims to maintain a good attention mechanism even with large number of embedding. It is also now possible to specify attention groups (using `grouped_features`). Attention is now done at the group level and not feature level. This is especially useful if a dataset has a lot of columns coming from on single source of data (exemple: a text column transformed using TD-IDF).\n\n# Contributing\n\nWhen contributing to the TabNet repository, please make sure to first discuss the change you wish to make via a new or already existing issue.\n\nOur commits follow the rules presented [here](https://www.conventionalcommits.org/en/v1.0.0/).\n\n# What problems does pytorch-tabnet handle?\n\n- TabNetClassifier : binary classification and multi-class classification problems\n- TabNetRegressor : simple and multi-task regression problems\n- TabNetMultiTaskClassifier:  multi-task multi-classification problems\n\n# How to use it?\n\nTabNet is now scikit-compatible, training a TabNetClassifier or TabNetRegressor is really easy.\n\n```python\nfrom pytorch_tabnet.tab_model import TabNetClassifier, TabNetRegressor\n\nclf = TabNetClassifier()  #TabNetRegressor()\nclf.fit(\n  X_train, Y_train,\n  eval_set=[(X_valid, y_valid)]\n)\npreds = clf.predict(X_test)\n```\n\nor for TabNetMultiTaskClassifier :\n\n```python\nfrom pytorch_tabnet.multitask import TabNetMultiTaskClassifier\nclf = TabNetMultiTaskClassifier()\nclf.fit(\n  X_train, Y_train,\n  eval_set=[(X_valid, y_valid)]\n)\npreds = clf.predict(X_test)\n```\n\nThe targets on `y_train/y_valid` should contain a unique type (e.g. they must all be strings or integers).\n\n### Default eval_metric\n\nA few classic evaluation metrics are implemented (see further below for custom ones):\n- binary classification metrics : \'auc\', \'accuracy\', \'balanced_accuracy\', \'logloss\'\n- multiclass classification : \'accuracy\', \'balanced_accuracy\', \'logloss\'\n- regression: \'mse\', \'mae\', \'rmse\', \'rmsle\'\n\n\nImportant Note : \'rmsle\' will automatically clip negative predictions to 0, because the model can predict negative values.\nIn order to match the given scores, you need to use `np.clip(clf.predict(X_predict), a_min=0, a_max=None)` when doing predictions.\n\n\n### Custom evaluation metrics\n\nYou can create a metric for your specific need. Here is an example for gini score (note that you need to specifiy whether this metric should be maximized or not):\n\n```python\nfrom pytorch_tabnet.metrics import Metric\nfrom sklearn.metrics import roc_auc_score\n\nclass Gini(Metric):\n    def __init__(self):\n        self._name = "gini"\n        self._maximize = True\n\n    def __call__(self, y_true, y_score):\n        auc = roc_auc_score(y_true, y_score[:, 1])\n        return max(2*auc - 1, 0.)\n\nclf = TabNetClassifier()\nclf.fit(\n  X_train, Y_train,\n  eval_set=[(X_valid, y_valid)],\n  eval_metric=[Gini]\n)\n\n```\n\nA specific customization example notebook is available here : https://github.com/dreamquark-ai/tabnet/blob/develop/customizing_example.ipynb\n\n# Semi-supervised pre-training\n\nAdded later to TabNet\'s original paper, semi-supervised pre-training is now available via the class `TabNetPretrainer`:\n\n```python\n# TabNetPretrainer\nunsupervised_model = TabNetPretrainer(\n    optimizer_fn=torch.optim.Adam,\n    optimizer_params=dict(lr=2e-2),\n    mask_type=\'entmax\' # "sparsemax"\n)\n\nunsupervised_model.fit(\n    X_train=X_train,\n    eval_set=[X_valid],\n    pretraining_ratio=0.8,\n)\n\nclf = TabNetClassifier(\n    optimizer_fn=torch.optim.Adam,\n    optimizer_params=dict(lr=2e-2),\n    scheduler_params={"step_size":10, # how to use learning rate scheduler\n                      "gamma":0.9},\n    scheduler_fn=torch.optim.lr_scheduler.StepLR,\n    mask_type=\'sparsemax\' # This will be overwritten if using pretrain model\n)\n\nclf.fit(\n    X_train=X_train, y_train=y_train,\n    eval_set=[(X_train, y_train), (X_valid, y_valid)],\n    eval_name=[\'train\', \'valid\'],\n    eval_metric=[\'auc\'],\n    from_unsupervised=unsupervised_model\n)\n```\n\nThe loss function has been normalized to be independent of `pretraining_ratio`, `batch_size` and the number of features in the problem.\nA self supervised loss greater than 1 means that your model is reconstructing worse than predicting the mean for each feature, a loss bellow 1 means that the model is doing better than predicting the mean.\n\nA complete example can be found within the notebook `pretraining_example.ipynb`.\n\n/!\\ : current implementation is trying to reconstruct the original inputs, but Batch Normalization applies a random transformation that can\'t be deduced by a single line, making the reconstruction harder. Lowering the `batch_size` might make the pretraining easier.\n\n# Data augmentation on the fly\n\nIt is now possible to apply custom data augmentation pipeline during training.\nTemplates for ClassificationSMOTE and RegressionSMOTE have been added in `pytorch-tabnet/augmentations.py` and can be used as is.\n\n\n# Easy saving and loading\n\nIt\'s really easy to save and re-load a trained model, this makes TabNet production ready.\n```\n# save tabnet model\nsaving_path_name = "./tabnet_model_test_1"\nsaved_filepath = clf.save_model(saving_path_name)\n\n# define new model with basic parameters and load state dict weights\nloaded_clf = TabNetClassifier()\nloaded_clf.load_model(saved_filepath)\n```\n\n# Useful links\n\n- [explanatory video](https://youtu.be/ysBaZO8YmX8)\n- [binary classification examples](https://github.com/dreamquark-ai/tabnet/blob/develop/census_example.ipynb)\n- [multi-class classification examples](https://github.com/dreamquark-ai/tabnet/blob/develop/forest_example.ipynb)\n- [regression examples](https://github.com/dreamquark-ai/tabnet/blob/develop/regression_example.ipynb)\n- [multi-task regression examples](https://github.com/dreamquark-ai/tabnet/blob/develop/multi_regression_example.ipynb)\n- [multi-task multi-class classification examples](https://www.kaggle.com/optimo/tabnetmultitaskclassifier)\n- [kaggle moa 1st place solution using tabnet](https://www.kaggle.com/c/lish-moa/discussion/201510)\n\n## Model parameters\n\n- `n_d` : int (default=8)\n\n    Width of the decision prediction layer. Bigger values gives more capacity to the model with the risk of overfitting.\n    Values typically range from 8 to 64.\n\n- `n_a`: int (default=8)\n\n    Width of the attention embedding for each mask.\n    According to the paper n_d=n_a is usually a good choice. (default=8)\n\n- `n_steps` : int (default=3)\n\n    Number of steps in the architecture (usually between 3 and 10)  \n\n- `gamma` : float  (default=1.3)\n\n    This is the coefficient for feature reusage in the masks.\n    A value close to 1 will make mask selection least correlated between layers.\n    Values range from 1.0 to 2.0.\n\n- `cat_idxs` : list of int (default=[] - Mandatory for embeddings) \n\n    List of categorical features indices.\n\n- `cat_dims` : list of int (default=[] - Mandatory for embeddings)\n\n    List of categorical features number of modalities (number of unique values for a categorical feature)\n    /!\\ no new modalities can be predicted\n\n- `cat_emb_dim` : list of int (optional)\n\n    List of embeddings size for each categorical features. (default =1)\n\n- `n_independent` : int  (default=2)\n\n    Number of independent Gated Linear Units layers at each step.\n    Usual values range from 1 to 5.\n\n- `n_shared` : int (default=2)\n\n    Number of shared Gated Linear Units at each step\n    Usual values range from 1 to 5\n\n- `epsilon` : float  (default 1e-15)\n\n    Should be left untouched.\n\n- `seed` : int (default=0)\n\n    Random seed for reproducibility\n\n- `momentum` : float\n\n    Momentum for batch normalization, typically ranges from 0.01 to 0.4 (default=0.02)\n\n- `clip_value` : float (default None)\n\n    If a float is given this will clip the gradient at clip_value.\n    \n- `lambda_sparse` : float (default = 1e-3)\n\n    This is the extra sparsity loss coefficient as proposed in the original paper. The bigger this coefficient is, the sparser your model will be in terms of feature selection. Depending on the difficulty of your problem, reducing this value could help.\n\n- `optimizer_fn` : torch.optim (default=torch.optim.Adam)\n\n    Pytorch optimizer function\n\n- `optimizer_params`: dict (default=dict(lr=2e-2))\n\n    Parameters compatible with optimizer_fn used initialize the optimizer. Since we have Adam as our default optimizer, we use this to define the initial learning rate used for training. As mentionned in the original paper, a large initial learning rate of ```0.02 ```  with decay is a good option.\n\n- `scheduler_fn` : torch.optim.lr_scheduler (default=None)\n\n    Pytorch Scheduler to change learning rates during training.\n\n- `scheduler_params` : dict\n\n    Dictionnary of parameters to apply to the scheduler_fn. Ex : {"gamma": 0.95, "step_size": 10}\n\n- `model_name` : str (default = \'DreamQuarkTabNet\')\n\n    Name of the model used for saving in disk, you can customize this to easily retrieve and reuse your trained models.\n\n- `verbose` : int (default=1)\n\n    Verbosity for notebooks plots, set to 1 to see every epoch, 0 to get None.\n\n- `device_name` : str (default=\'auto\')\n    \'cpu\' for cpu training, \'gpu\' for gpu training, \'auto\' to automatically detect gpu.\n\n- `mask_type: str` (default=\'sparsemax\')\n    Either "sparsemax" or "entmax" : this is the masking function to use for selecting features.\n\n- `grouped_features: list of list of ints` (default=None)\n    This allows the model to share it\'s attention accross feature inside a same group.\n    This can be especially useful when your preprocessing generates correlated or dependant features: like if you use a TF-IDF or a PCA on a text column.\n    Note that feature importance will be exactly the same between features on a same group.\n    Please also note that embeddings generated for a categorical variable are always inside a same group. \n\n- `n_shared_decoder` : int (default=1)\n\n    Number of shared GLU block in decoder, this is only useful for `TabNetPretrainer`.\n\n- `n_indep_decoder` : int (default=1)\n\n    Number of independent GLU block in decoder, this is only useful for `TabNetPretrainer`.\n\n## Fit parameters\n\n- `X_train` : np.array or scipy.sparse.csr_matrix\n\n    Training features\n\n- `y_train` : np.array\n\n    Training targets\n\n- `eval_set`: list of tuple  \n\n    List of eval tuple set (X, y).  \n    The last one is used for early stopping  \n\n- `eval_name`: list of str  \n              List of eval set names.  \n\n- `eval_metric` : list of str  \n              List of evaluation metrics.  \n              The last metric is used for early stopping.\n\n- `max_epochs` : int (default = 200)\n\n    Maximum number of epochs for trainng.\n    \n- `patience` : int (default = 10)\n\n    Number of consecutive epochs without improvement before performing early stopping.\n\n    If patience is set to 0, then no early stopping will be performed.\n\n    Note that if patience is enabled, then best weights from best epoch will automatically be loaded at the end of `fit`.\n\n- `weights` : int or dict (default=0)\n\n    /!\\ Only for TabNetClassifier\n    Sampling parameter\n    0 : no sampling\n    1 : automated sampling with inverse class occurrences\n    dict : keys are classes, values are weights for each class\n\n- `loss_fn` : torch.loss or list of torch.loss\n\n    Loss function for training (default to mse for regression and cross entropy for classification)\n    When using TabNetMultiTaskClassifier you can set a list of same length as number of tasks,\n    each task will be assigned its own loss function\n\n- `batch_size` : int (default=1024)\n\n    Number of examples per batch. Large batch sizes are recommended.\n\n- `virtual_batch_size` : int (default=128)\n\n    Size of the mini batches used for "Ghost Batch Normalization".\n    /!\\ `virtual_batch_size` should divide `batch_size`\n\n- `num_workers` : int (default=0)\n\n    Number or workers used in torch.utils.data.Dataloader\n\n- `drop_last` : bool (default=False)\n\n    Whether to drop last batch if not complete during training\n\n- `callbacks` : list of callback function  \n        List of custom callbacks\n\n- `pretraining_ratio` : float\n\n        /!\\ TabNetPretrainer Only : Percentage of input features to mask during pretraining.\n\n        Should be between 0 and 1. The bigger the harder the reconstruction task is.\n\n- `warm_start` : bool (default=False)\n    In order to match scikit-learn API, this is set to False.\n    It allows to fit twice the same model and start from a warm start.\n\n- `compute_importance` : bool (default=True)\n\n    Whether to compute feature importance\n',
     'author': 'None',
     'author_email': 'None',
     'maintainer': 'None',
     'maintainer_email': 'None',
     'url': 'https://github.com/dreamquark-ai/tabnet',
     'packages': packages,
     'package_data': package_data,
     'install_requires': install_requires,
-    'python_requires': '>=3.6',
+    'python_requires': '>=3.7',
 }
 
 
 setup(**setup_kwargs)
```

### Comparing `pytorch_tabnet-4.0/PKG-INFO` & `pytorch_tabnet-4.1.0/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,34 +1,33 @@
 Metadata-Version: 2.1
 Name: pytorch-tabnet
-Version: 4.0
+Version: 4.1.0
 Summary: PyTorch implementation of TabNet
 Home-page: https://github.com/dreamquark-ai/tabnet
 Keywords: tabnet,pytorch,neural-networks
-Requires-Python: >=3.6
+Requires-Python: >=3.7
 Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
-Requires-Dist: numpy (>=1.17,<2.0)
+Requires-Dist: numpy (>=1.17)
 Requires-Dist: scikit_learn (>0.21)
 Requires-Dist: scipy (>1.4)
-Requires-Dist: torch (>=1.2,<2.0)
-Requires-Dist: tqdm (>=4.36,<5.0)
+Requires-Dist: torch (>=1.3)
+Requires-Dist: tqdm (>=4.36)
 Project-URL: Documentation, https://github.com/dreamquark-ai/tabnet
 Project-URL: Repository, https://github.com/dreamquark-ai/tabnet
 Description-Content-Type: text/markdown
 
 # README
 
 # TabNet : Attentive Interpretable Tabular Learning
 
-This is a pyTorch implementation of Tabnet (Arik, S. O., & Pfister, T. (2019). TabNet: Attentive Interpretable Tabular Learning. arXiv preprint arXiv:1908.07442.) https://arxiv.org/pdf/1908.07442.pdf.
+This is a pyTorch implementation of Tabnet (Arik, S. O., & Pfister, T. (2019). TabNet: Attentive Interpretable Tabular Learning. arXiv preprint arXiv:1908.07442.) https://arxiv.org/pdf/1908.07442.pdf. Please note that some different choices have been made overtime to improve the library which can differ from the orginal paper.
 
 <!--- BADGES: START --->
 [![CircleCI](https://circleci.com/gh/dreamquark-ai/tabnet.svg?style=svg)](https://circleci.com/gh/dreamquark-ai/tabnet)
 
 [![PyPI version](https://badge.fury.io/py/pytorch-tabnet.svg)](https://badge.fury.io/py/pytorch-tabnet)
 
 ![PyPI - Downloads](https://img.shields.io/pypi/dm/pytorch-tabnet)
@@ -86,14 +85,18 @@
 
 -----------------
 
 - `poetry install` to install all the dependencies, including jupyter
 
 - `make notebook` inside the same terminal. You can then follow the link to a jupyter notebook with tabnet installed.
 
+# What is new ?
+
+- from version **> 4.0** attention is now embedding aware. This aims to maintain a good attention mechanism even with large number of embedding. It is also now possible to specify attention groups (using `grouped_features`). Attention is now done at the group level and not feature level. This is especially useful if a dataset has a lot of columns coming from on single source of data (exemple: a text column transformed using TD-IDF).
+
 # Contributing
 
 When contributing to the TabNet repository, please make sure to first discuss the change you wish to make via a new or already existing issue.
 
 Our commits follow the rules presented [here](https://www.conventionalcommits.org/en/v1.0.0/).
 
 # What problems does pytorch-tabnet handle?
@@ -334,25 +337,31 @@
 
 - `device_name` : str (default='auto')
     'cpu' for cpu training, 'gpu' for gpu training, 'auto' to automatically detect gpu.
 
 - `mask_type: str` (default='sparsemax')
     Either "sparsemax" or "entmax" : this is the masking function to use for selecting features.
 
+- `grouped_features: list of list of ints` (default=None)
+    This allows the model to share it's attention accross feature inside a same group.
+    This can be especially useful when your preprocessing generates correlated or dependant features: like if you use a TF-IDF or a PCA on a text column.
+    Note that feature importance will be exactly the same between features on a same group.
+    Please also note that embeddings generated for a categorical variable are always inside a same group. 
+
 - `n_shared_decoder` : int (default=1)
 
     Number of shared GLU block in decoder, this is only useful for `TabNetPretrainer`.
 
 - `n_indep_decoder` : int (default=1)
 
     Number of independent GLU block in decoder, this is only useful for `TabNetPretrainer`.
 
 ## Fit parameters
 
-- `X_train` : np.array
+- `X_train` : np.array or scipy.sparse.csr_matrix
 
     Training features
 
 - `y_train` : np.array
 
     Training targets
 
@@ -420,7 +429,11 @@
 
         Should be between 0 and 1. The bigger the harder the reconstruction task is.
 
 - `warm_start` : bool (default=False)
     In order to match scikit-learn API, this is set to False.
     It allows to fit twice the same model and start from a warm start.
 
+- `compute_importance` : bool (default=True)
+
+    Whether to compute feature importance
+
```

