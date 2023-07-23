# Comparing `tmp/deformable-attention-0.0.8.tar.gz` & `tmp/deformable-attention-0.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "deformable-attention-0.0.8.tar", last modified: Mon Mar 21 19:00:29 2022, max compression
+gzip compressed data, was "deformable-attention-0.0.9.tar", last modified: Mon Mar 21 19:23:35 2022, max compression
```

## Comparing `deformable-attention-0.0.8.tar` & `deformable-attention-0.0.9.tar`

### file list

```diff
@@ -1,17 +1,17 @@
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-03-21 19:00:29.517705 deformable-attention-0.0.8/
--rw-r--r--   0 runner    (1001) docker     (121)     1066 2022-03-21 19:00:17.000000 deformable-attention-0.0.8/LICENSE
--rw-r--r--   0 runner    (1001) docker     (121)      676 2022-03-21 19:00:29.517705 deformable-attention-0.0.8/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     1830 2022-03-21 19:00:17.000000 deformable-attention-0.0.8/README.md
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-03-21 19:00:29.517705 deformable-attention-0.0.8/deformable_attention/
--rw-r--r--   0 runner    (1001) docker     (121)      282 2022-03-21 19:00:17.000000 deformable-attention-0.0.8/deformable_attention/__init__.py
--rw-r--r--   0 runner    (1001) docker     (121)     5939 2022-03-21 19:00:17.000000 deformable-attention-0.0.8/deformable_attention/deformable_attention_1d.py
--rw-r--r--   0 runner    (1001) docker     (121)     5804 2022-03-21 19:00:17.000000 deformable-attention-0.0.8/deformable_attention/deformable_attention_2d.py
--rw-r--r--   0 runner    (1001) docker     (121)     5950 2022-03-21 19:00:17.000000 deformable-attention-0.0.8/deformable_attention/deformable_attention_3d.py
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-03-21 19:00:29.517705 deformable-attention-0.0.8/deformable_attention.egg-info/
--rw-r--r--   0 runner    (1001) docker     (121)      676 2022-03-21 19:00:29.000000 deformable-attention-0.0.8/deformable_attention.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)      422 2022-03-21 19:00:29.000000 deformable-attention-0.0.8/deformable_attention.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2022-03-21 19:00:29.000000 deformable-attention-0.0.8/deformable_attention.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (121)       23 2022-03-21 19:00:29.000000 deformable-attention-0.0.8/deformable_attention.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (121)       21 2022-03-21 19:00:29.000000 deformable-attention-0.0.8/deformable_attention.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (121)       38 2022-03-21 19:00:29.517705 deformable-attention-0.0.8/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (121)      831 2022-03-21 19:00:17.000000 deformable-attention-0.0.8/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-03-21 19:23:35.804187 deformable-attention-0.0.9/
+-rw-r--r--   0 runner    (1001) docker     (121)     1066 2022-03-21 19:23:23.000000 deformable-attention-0.0.9/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (121)      676 2022-03-21 19:23:35.804187 deformable-attention-0.0.9/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (121)     1925 2022-03-21 19:23:23.000000 deformable-attention-0.0.9/README.md
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-03-21 19:23:35.804187 deformable-attention-0.0.9/deformable_attention/
+-rw-r--r--   0 runner    (1001) docker     (121)      282 2022-03-21 19:23:23.000000 deformable-attention-0.0.9/deformable_attention/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)     6006 2022-03-21 19:23:23.000000 deformable-attention-0.0.9/deformable_attention/deformable_attention_1d.py
+-rw-r--r--   0 runner    (1001) docker     (121)     5871 2022-03-21 19:23:23.000000 deformable-attention-0.0.9/deformable_attention/deformable_attention_2d.py
+-rw-r--r--   0 runner    (1001) docker     (121)     6373 2022-03-21 19:23:23.000000 deformable-attention-0.0.9/deformable_attention/deformable_attention_3d.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-03-21 19:23:35.804187 deformable-attention-0.0.9/deformable_attention.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (121)      676 2022-03-21 19:23:35.000000 deformable-attention-0.0.9/deformable_attention.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (121)      422 2022-03-21 19:23:35.000000 deformable-attention-0.0.9/deformable_attention.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (121)        1 2022-03-21 19:23:35.000000 deformable-attention-0.0.9/deformable_attention.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (121)       23 2022-03-21 19:23:35.000000 deformable-attention-0.0.9/deformable_attention.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (121)       21 2022-03-21 19:23:35.000000 deformable-attention-0.0.9/deformable_attention.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (121)       38 2022-03-21 19:23:35.804187 deformable-attention-0.0.9/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (121)      831 2022-03-21 19:23:23.000000 deformable-attention-0.0.9/setup.py
```

### Comparing `deformable-attention-0.0.8/LICENSE` & `deformable-attention-0.0.9/LICENSE`

 * *Files identical despite different names*

### Comparing `deformable-attention-0.0.8/PKG-INFO` & `deformable-attention-0.0.9/PKG-INFO`

 * *Files 15% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: deformable-attention
-Version: 0.0.8
+Version: 0.0.9
 Summary: Deformable Attention - from the paper "Vision Transformer with Deformable Attention"
 Home-page: https://github.com/lucidrains/deformable-attention
 Author: Phil Wang
 Author-email: lucidrains@gmail.com
 License: MIT
 Keywords: artificial intelligence,deep learning,transformers,attention mechanism
 Platform: UNKNOWN
```

### Comparing `deformable-attention-0.0.8/README.md` & `deformable-attention-0.0.9/README.md`

 * *Files 4% similar despite different names*

```diff
@@ -27,14 +27,18 @@
     offset_kernel_size = 6,      # offset kernel size
 )
 
 x = torch.randn(1, 512, 64, 64)
 attn(x) # (1, 512, 64, 64)
 ```
 
+## Todo
+
+- [ ] for video, allow for asymmetric kernel dimensions (frames may be small number)
+
 ## Citation
 
 ```bibtex
 @misc{xia2022vision,
     title   = {Vision Transformer with Deformable Attention}, 
     author  = {Zhuofan Xia and Xuran Pan and Shiji Song and Li Erran Li and Gao Huang},
     year    = {2022},
```

#### html2text {}

```diff
@@ -5,17 +5,18 @@
 Embedding proposed in SwinV2. ## Install ```bash $ pip install deformable-
 attention ``` ## Usage ```python import torch from deformable_attention import
 DeformableAttention attn = DeformableAttention( dim = 512, # feature dimensions
 dim_head = 64, # dimension per head heads = 8, # attention heads dropout = 0.,
 # dropout downsample_factor = 4, # downsample factor (r in paper) offset_scale
 = 4, # scale of offset, maximum offset offset_groups = None, # number of offset
 groups, should be multiple of heads offset_kernel_size = 6, # offset kernel
-size ) x = torch.randn(1, 512, 64, 64) attn(x) # (1, 512, 64, 64) ``` ##
-Citation ```bibtex @misc{xia2022vision, title = {Vision Transformer with
-Deformable Attention}, author = {Zhuofan Xia and Xuran Pan and Shiji Song and
-Li Erran Li and Gao Huang}, year = {2022}, eprint = {2201.00520}, archivePrefix
-= {arXiv}, primaryClass = {cs.CV} } ``` ```bibtex @misc{liu2021swin, title =
-{Swin Transformer V2: Scaling Up Capacity and Resolution}, author = {Ze Liu and
-Han Hu and Yutong Lin and Zhuliang Yao and Zhenda Xie and Yixuan Wei and Jia
-Ning and Yue Cao and Zheng Zhang and Li Dong and Furu Wei and Baining Guo},
-year = {2021}, eprint = {2111.09883}, archivePrefix = {arXiv}, primaryClass =
-{cs.CV} } ```
+size ) x = torch.randn(1, 512, 64, 64) attn(x) # (1, 512, 64, 64) ``` ## Todo -
+[ ] for video, allow for asymmetric kernel dimensions (frames may be small
+number) ## Citation ```bibtex @misc{xia2022vision, title = {Vision Transformer
+with Deformable Attention}, author = {Zhuofan Xia and Xuran Pan and Shiji Song
+and Li Erran Li and Gao Huang}, year = {2022}, eprint = {2201.00520},
+archivePrefix = {arXiv}, primaryClass = {cs.CV} } ``` ```bibtex @misc
+{liu2021swin, title = {Swin Transformer V2: Scaling Up Capacity and
+Resolution}, author = {Ze Liu and Han Hu and Yutong Lin and Zhuliang Yao and
+Zhenda Xie and Yixuan Wei and Jia Ning and Yue Cao and Zheng Zhang and Li Dong
+and Furu Wei and Baining Guo}, year = {2021}, eprint = {2111.09883},
+archivePrefix = {arXiv}, primaryClass = {cs.CV} } ```
```

### Comparing `deformable-attention-0.0.8/deformable_attention/deformable_attention_1d.py` & `deformable-attention-0.0.9/deformable_attention/deformable_attention_1d.py`

 * *Files 2% similar despite different names*

```diff
@@ -93,20 +93,21 @@
         self,
         *,
         dim,
         dim_head = 64,
         heads = 8,
         dropout = 0.,
         downsample_factor = 4,
-        offset_scale = 4,
+        offset_scale = None,
         offset_groups = None,
         offset_kernel_size = 6,
         cpb_log_distance = True
     ):
         super().__init__()
+        offset_scale = default(offset_scale, downsample_factor)
         assert divisible_by(offset_kernel_size - downsample_factor, 2)
 
         offset_groups = default(offset_groups, heads)
         assert divisible_by(heads, offset_groups)
 
         inner_dim = dim_head * heads
         self.scale = dim_head ** -0.5
```

### Comparing `deformable-attention-0.0.8/deformable_attention/deformable_attention_2d.py` & `deformable-attention-0.0.9/deformable_attention/deformable_attention_2d.py`

 * *Files 1% similar despite different names*

```diff
@@ -95,19 +95,20 @@
         self,
         *,
         dim,
         dim_head = 64,
         heads = 8,
         dropout = 0.,
         downsample_factor = 4,
-        offset_scale = 4,
+        offset_scale = None,
         offset_groups = None,
         offset_kernel_size = 6
     ):
         super().__init__()
+        offset_scale = default(offset_scale, downsample_factor)
         assert divisible_by(offset_kernel_size - downsample_factor, 2)
 
         offset_groups = default(offset_groups, heads)
         assert divisible_by(heads, offset_groups)
 
         inner_dim = dim_head * heads
         self.scale = dim_head ** -0.5
```

### Comparing `deformable-attention-0.0.8/deformable_attention/deformable_attention_3d.py` & `deformable-attention-0.0.9/deformable_attention/deformable_attention_3d.py`

 * *Files 11% similar despite different names*

```diff
@@ -11,14 +11,17 @@
 
 def default(val, d):
     return val if exists(val) else d
 
 def divisible_by(numer, denom):
     return (numer % denom) == 0
 
+def cast_tuple(x, length = 1):
+    return x if isinstance(x, tuple) else ((x,) * depth)
+
 # tensor helpers
 
 def create_grid_like(t, dim = 0):
     f, h, w, device = *t.shape[-3:], t.device
 
     grid = torch.stack(torch.meshgrid(
         torch.arange(f, device = device),
@@ -40,18 +43,18 @@
     grid_w = 2.0 * grid_w / max(w - 1, 1) - 1.0
 
     return torch.stack((grid_f, grid_h, grid_w), dim = out_dim)
 
 class Scale(nn.Module):
     def __init__(self, scale):
         super().__init__()
-        self.scale = scale
+        self.register_buffer('scale', torch.tensor(scale, dtype = torch.float32))
 
     def forward(self, x):
-        return x * self.scale
+        return x * rearrange(self.scale, 'c -> 1 c 1 1 1')
 
 # continuous positional bias from SwinV2
 
 class CPB(nn.Module):
     """ https://arxiv.org/abs/2111.09883v1 """
 
     def __init__(self, dim, *, heads, offset_groups, depth):
@@ -97,35 +100,39 @@
         self,
         *,
         dim,
         dim_head = 64,
         heads = 8,
         dropout = 0.,
         downsample_factor = 4,
-        offset_scale = 4,
+        offset_scale = None,
         offset_groups = None,
         offset_kernel_size = 6
     ):
         super().__init__()
-        assert divisible_by(offset_kernel_size - downsample_factor, 2)
+        downsample_factor = cast_tuple(downsample_factor, length = 3)
+        offset_scale = default(offset_scale, downsample_factor)
+
+        offset_conv_padding = tuple(map(lambda x: (x[0] - x[1]) / 2, zip(offset_kernel_size, downsample_factor)))
+        assert all([padding.is_integer() for padding in offset_conv_padding])
 
         offset_groups = default(offset_groups, heads)
         assert divisible_by(heads, offset_groups)
 
         inner_dim = dim_head * heads
         self.scale = dim_head ** -0.5
         self.heads = heads
         self.offset_groups = offset_groups
 
         offset_dims = inner_dim // offset_groups
 
         self.downsample_factor = downsample_factor
 
         self.to_offsets = nn.Sequential(
-            nn.Conv3d(offset_dims, offset_dims, offset_kernel_size, groups = offset_dims, stride = downsample_factor, padding = (offset_kernel_size - downsample_factor) // 2),
+            nn.Conv3d(offset_dims, offset_dims, offset_kernel_size, groups = offset_dims, stride = downsample_factor, padding = tuple(map(int, offset_conv_padding))),
             nn.GELU(),
             nn.Conv3d(offset_dims, 3, 1, bias = False),
             nn.Tanh(),
             Scale(offset_scale)
         )
 
         self.rel_pos_bias = CPB(dim // 4, offset_groups = offset_groups, heads = heads, depth = 2)
```

### Comparing `deformable-attention-0.0.8/deformable_attention.egg-info/PKG-INFO` & `deformable-attention-0.0.9/deformable_attention.egg-info/PKG-INFO`

 * *Files 15% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: deformable-attention
-Version: 0.0.8
+Version: 0.0.9
 Summary: Deformable Attention - from the paper "Vision Transformer with Deformable Attention"
 Home-page: https://github.com/lucidrains/deformable-attention
 Author: Phil Wang
 Author-email: lucidrains@gmail.com
 License: MIT
 Keywords: artificial intelligence,deep learning,transformers,attention mechanism
 Platform: UNKNOWN
```

### Comparing `deformable-attention-0.0.8/setup.py` & `deformable-attention-0.0.9/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 from setuptools import setup, find_packages
 
 setup(
   name = 'deformable-attention',
   packages = find_packages(exclude=[]),
-  version = '0.0.8',
+  version = '0.0.9',
   license='MIT',
   description = 'Deformable Attention - from the paper "Vision Transformer with Deformable Attention"',
   author = 'Phil Wang',
   author_email = 'lucidrains@gmail.com',
   url = 'https://github.com/lucidrains/deformable-attention',
   keywords = [
     'artificial intelligence',
```

