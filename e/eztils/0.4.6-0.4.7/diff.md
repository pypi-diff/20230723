# Comparing `tmp/eztils-0.4.6.tar.gz` & `tmp/eztils-0.4.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "eztils-0.4.6.tar", max compression
+gzip compressed data, was "eztils-0.4.7.tar", max compression
```

## Comparing `eztils-0.4.6.tar` & `eztils-0.4.7.tar`

### file list

```diff
@@ -1,20 +1,20 @@
--rw-r--r--   0        0        0     1075 2023-07-22 06:01:58.988271 eztils-0.4.6/LICENSE
--rw-r--r--   0        0        0    12741 2023-07-22 06:01:58.988271 eztils-0.4.6/README.md
--rw-r--r--   0        0        0      542 2023-07-22 06:01:58.988271 eztils-0.4.6/eztils/__init__.py
--rw-r--r--   0        0        0     2465 2023-07-22 06:01:58.988271 eztils-0.4.6/eztils/default/__init__.py
--rw-r--r--   0        0        0     3689 2023-07-22 06:01:58.988271 eztils-0.4.6/eztils/default/dict_operations.py
--rw-r--r--   0        0        0     2246 2023-07-22 06:01:58.988271 eztils-0.4.6/eztils/default/itertools.py
--rw-r--r--   0        0        0     2458 2023-07-22 06:01:58.988271 eztils-0.4.6/eztils/default/logging.py
--rw-r--r--   0        0        0     1412 2023-07-22 06:01:58.988271 eztils-0.4.6/eztils/default/math.py
--rw-r--r--   0        0        0     1091 2023-07-22 06:01:58.988271 eztils-0.4.6/eztils/default/structures.py
--rw-r--r--   0        0        0     4296 2023-07-22 06:01:58.988271 eztils-0.4.6/eztils/git/__init__.py
--rw-r--r--   0        0        0     1607 2023-07-22 06:01:58.988271 eztils-0.4.6/eztils/torch/__init__.py
--rw-r--r--   0        0        0    15657 2023-07-22 06:01:58.988271 eztils-0.4.6/eztils/torch/distributions.py
--rw-r--r--   0        0        0      155 2023-07-22 06:01:58.988271 eztils-0.4.6/eztils/torch/lightning.py
--rw-r--r--   0        0        0      173 2023-07-22 06:01:58.988271 eztils-0.4.6/eztils/torch/math.py
--rw-r--r--   0        0        0     2550 2023-07-22 06:01:58.988271 eztils-0.4.6/eztils/torch/modules.py
--rw-r--r--   0        0        0     1420 2023-07-22 06:01:58.988271 eztils-0.4.6/eztils/torch/parameters.py
--rw-r--r--   0        0        0     1668 2023-07-22 06:01:58.988271 eztils-0.4.6/eztils/torch/tensor_creators.py
--rw-r--r--   0        0        0     2858 2023-07-22 06:01:58.988271 eztils-0.4.6/eztils/torch/to.py
--rw-r--r--   0        0        0     3624 2023-07-22 06:01:58.988271 eztils-0.4.6/pyproject.toml
--rw-r--r--   0        0        0    13903 1970-01-01 00:00:00.000000 eztils-0.4.6/PKG-INFO
+-rw-r--r--   0        0        0     1075 2023-07-23 00:52:06.291815 eztils-0.4.7/LICENSE
+-rw-r--r--   0        0        0    12741 2023-07-23 00:52:06.291815 eztils-0.4.7/README.md
+-rw-r--r--   0        0        0      542 2023-07-23 00:52:06.291815 eztils-0.4.7/eztils/__init__.py
+-rw-r--r--   0        0        0     2465 2023-07-23 00:52:06.291815 eztils-0.4.7/eztils/default/__init__.py
+-rw-r--r--   0        0        0     3689 2023-07-23 00:52:06.291815 eztils-0.4.7/eztils/default/dict_operations.py
+-rw-r--r--   0        0        0     2246 2023-07-23 00:52:06.291815 eztils-0.4.7/eztils/default/itertools.py
+-rw-r--r--   0        0        0     2458 2023-07-23 00:52:06.291815 eztils-0.4.7/eztils/default/logging.py
+-rw-r--r--   0        0        0     1432 2023-07-23 00:52:06.291815 eztils-0.4.7/eztils/default/math.py
+-rw-r--r--   0        0        0     1091 2023-07-23 00:52:06.291815 eztils-0.4.7/eztils/default/structures.py
+-rw-r--r--   0        0        0     4296 2023-07-23 00:52:06.291815 eztils-0.4.7/eztils/git/__init__.py
+-rw-r--r--   0        0        0     1607 2023-07-23 00:52:06.291815 eztils-0.4.7/eztils/torch/__init__.py
+-rw-r--r--   0        0        0    15657 2023-07-23 00:52:06.291815 eztils-0.4.7/eztils/torch/distributions.py
+-rw-r--r--   0        0        0      155 2023-07-23 00:52:06.291815 eztils-0.4.7/eztils/torch/lightning.py
+-rw-r--r--   0        0        0      173 2023-07-23 00:52:06.291815 eztils-0.4.7/eztils/torch/math.py
+-rw-r--r--   0        0        0     2550 2023-07-23 00:52:06.291815 eztils-0.4.7/eztils/torch/modules.py
+-rw-r--r--   0        0        0     1420 2023-07-23 00:52:06.291815 eztils-0.4.7/eztils/torch/parameters.py
+-rw-r--r--   0        0        0     1746 2023-07-23 00:52:06.291815 eztils-0.4.7/eztils/torch/tensor_creators.py
+-rw-r--r--   0        0        0     2929 2023-07-23 00:52:06.291815 eztils-0.4.7/eztils/torch/to.py
+-rw-r--r--   0        0        0     3618 2023-07-23 00:52:06.291815 eztils-0.4.7/pyproject.toml
+-rw-r--r--   0        0        0    13903 1970-01-01 00:00:00.000000 eztils-0.4.7/PKG-INFO
```

### Comparing `eztils-0.4.6/LICENSE` & `eztils-0.4.7/LICENSE`

 * *Files identical despite different names*

### Comparing `eztils-0.4.6/README.md` & `eztils-0.4.7/README.md`

 * *Files identical despite different names*

### Comparing `eztils-0.4.6/eztils/__init__.py` & `eztils-0.4.7/eztils/__init__.py`

 * *Files identical despite different names*

### Comparing `eztils-0.4.6/eztils/default/__init__.py` & `eztils-0.4.7/eztils/default/__init__.py`

 * *Files identical despite different names*

### Comparing `eztils-0.4.6/eztils/default/dict_operations.py` & `eztils-0.4.7/eztils/default/dict_operations.py`

 * *Files identical despite different names*

### Comparing `eztils-0.4.6/eztils/default/itertools.py` & `eztils-0.4.7/eztils/default/itertools.py`

 * *Files identical despite different names*

### Comparing `eztils-0.4.6/eztils/default/logging.py` & `eztils-0.4.7/eztils/default/logging.py`

 * *Files identical despite different names*

### Comparing `eztils-0.4.6/eztils/default/math.py` & `eztils-0.4.7/eztils/default/math.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,12 @@
 from collections import OrderedDict
 from numbers import Number
 
+import numpy as np
+
 
 def normalize(x):
     """
     scales `x` to [0, 1]
     """
     x = x - x.min()
     x = x / x.max()
```

### Comparing `eztils-0.4.6/eztils/default/structures.py` & `eztils-0.4.7/eztils/default/structures.py`

 * *Files identical despite different names*

### Comparing `eztils-0.4.6/eztils/git/__init__.py` & `eztils-0.4.7/eztils/git/__init__.py`

 * *Files identical despite different names*

### Comparing `eztils-0.4.6/eztils/torch/__init__.py` & `eztils-0.4.7/eztils/torch/__init__.py`

 * *Files identical despite different names*

### Comparing `eztils-0.4.6/eztils/torch/distributions.py` & `eztils-0.4.7/eztils/torch/distributions.py`

 * *Files identical despite different names*

### Comparing `eztils-0.4.6/eztils/torch/modules.py` & `eztils-0.4.7/eztils/torch/modules.py`

 * *Files identical despite different names*

### Comparing `eztils-0.4.6/eztils/torch/parameters.py` & `eztils-0.4.7/eztils/torch/parameters.py`

 * *Files identical despite different names*

### Comparing `eztils-0.4.6/eztils/torch/tensor_creators.py` & `eztils-0.4.7/eztils/torch/tensor_creators.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,20 +1,23 @@
 """
 GPU wrappers
 """
 import torch
 
 from eztils import default
-from eztils.torch import DEVICE, DTYPE
 
 
 def device_dtype_decorator(func):
     def wrapper(*args, torch_device=None, **kwargs):
+        from eztils.torch import DEVICE, DTYPE
+
         torch_device = default(torch_device, DEVICE)
         torch_dtype = default(kwargs.get("dtype"), DTYPE)
+        kwargs.pop("device", None)
+        kwargs.pop("dtype", None)
         return func(*args, **kwargs, device=torch_device, dtype=torch_dtype)
 
     return wrapper
 
 
 @device_dtype_decorator
 def from_numpy(*args, **kwargs):
```

### Comparing `eztils-0.4.6/eztils/torch/to.py` & `eztils-0.4.7/eztils/torch/to.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,13 @@
 from typing import Any, Union
 
 import numpy as np
 import torch
 
 from eztils import normalize
-from eztils.torch import DEVICE, DTYPE
 
 
 def to_np(x):
     if torch.is_tensor(x):
         x = x.detach().cpu().numpy()
     return x
 
@@ -24,27 +23,33 @@
     normalized = normalize(x)
     array = to_np(normalized)
     array = np.transpose(array, (1, 2, 0))
     return (array * 255).astype(np.uint8)
 
 
 def to_torch(x, dtype=None, device=None):
+    from eztils.torch import DEVICE, DTYPE
+
     dtype = dtype or DTYPE
     device = device or DEVICE
     if type(x) is dict:
         return {k: to_torch(v, dtype, device) for k, v in x.items()}
     elif torch.is_tensor(x):
         return x.to(device).type(dtype)
         # import pdb; pdb.set_trace()
     return torch.tensor(x, dtype=dtype, device=device)
 
 
 def to_device(
-    input: Any, device: Union[str, torch.device, int] = DEVICE, inplace: bool = True
+    input: Any, device: Union[str, torch.device, int] = None, inplace: bool = True
 ) -> Any:
+    from eztils.torch import DEVICE
+
+    device = device or DEVICE
+
     """Recursively places tensors on the appropriate device."""
     if input is None:
         return input
     elif isinstance(input, torch.Tensor):
         return input.to(device)
     elif isinstance(input, tuple):
         return tuple(
```

### Comparing `eztils-0.4.6/pyproject.toml` & `eztils-0.4.7/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 authors = ["ezhang7423 <ezhang7423@student.palomar.edu>"]
 description = "eds utilities"
 homepage = "https://github.com/ezhang7423/eztils"
 license = "MIT"
 name = "eztils"
 readme = "README.md"
 repository = "https://github.com/ezhang7423/eztils"
-version = "0.4.6"
+version = "0.4.7"
 
 # Keywords description https://python-poetry.org/docs/pyproject/#keywords
 keywords = [] #! Update me
 
 # Pypi classifiers: https://pypi.org/classifiers/
 classifiers = [
   #! Update me
@@ -27,46 +27,44 @@
   "Programming Language :: Python :: 3",
   "Programming Language :: Python :: 3.8",
   "Programming Language :: Python :: 3.9",
   "Programming Language :: Python :: 3.10",
 ]
 
 [tool.poetry.dependencies]
+beartype = "^0.14.1"
+einops = "^0.6.1"
+ezjaxtyping = {version = "^0.2.20", optional = true}
+loguru = "^0.7.0"
+numpy = "^1.24.3"
 python = "^3.8"
 rich = "^13.3.3"
-numpy = "^1.24.3"
-loguru = "^0.7.0"
-einops = "^0.6.1"
 tqdm = "^4.65.0"
-ezjaxtyping = { version = "^0.2.20", optional = true }
-beartype = "^0.14.1"
 
 [tool.poetry.group.dev.dependencies]
 bandit = "^1.7.5"
 black = "^23.3.0"
 coverage = "^7.2.2"
 coverage-badge = "^1.1.0"
 darglint = "^1.8.1"
-isort = { extras = ["colors"], version = "^5.12.0" }
+ipython = "^8.11.0"
+isort = {extras = ["colors"], version = "^5.12.0"}
 mypy = "^1.1.1"
 mypy-extensions = "^1.0.0"
 pre-commit = "^3.2.1"
 pydocstyle = "^6.3.0"
 pylint = "^2.17.1"
 pytest = "^7.2.2"
 pytest-cov = "^4.0.0"
 pytest-html = "^3.2.0"
 pyupgrade = "^3.3.1"
-ipython = "^8.11.0"
-
 
 [tool.poetry.extras]
 torch = ["ezjaxtyping"]
 
-
 [tool.black]
 # https://github.com/psf/black
 color = true
 line-length = 88
 target-version = ["py38"]
 
 exclude = '''
```

### Comparing `eztils-0.4.6/PKG-INFO` & `eztils-0.4.7/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: eztils
-Version: 0.4.6
+Version: 0.4.7
 Summary: eds utilities
 Home-page: https://github.com/ezhang7423/eztils
 License: MIT
 Author: ezhang7423
 Author-email: ezhang7423@student.palomar.edu
 Requires-Python: >=3.8,<4.0
 Classifier: Development Status :: 3 - Alpha
```

