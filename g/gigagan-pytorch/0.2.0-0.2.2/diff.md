# Comparing `tmp/gigagan-pytorch-0.2.0.tar.gz` & `tmp/gigagan-pytorch-0.2.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "gigagan-pytorch-0.2.0.tar", last modified: Sun Jul 23 16:49:34 2023, max compression
+gzip compressed data, was "gigagan-pytorch-0.2.2.tar", last modified: Sun Jul 23 17:30:20 2023, max compression
```

## Comparing `gigagan-pytorch-0.2.0.tar` & `gigagan-pytorch-0.2.2.tar`

### file list

```diff
@@ -1,22 +1,22 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:49:34.227234 gigagan-pytorch-0.2.0/
--rw-r--r--   0 runner    (1001) docker     (123)     1066 2023-07-23 16:49:23.000000 gigagan-pytorch-0.2.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      612 2023-07-23 16:49:34.227234 gigagan-pytorch-0.2.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     9314 2023-07-23 16:49:23.000000 gigagan-pytorch-0.2.0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:49:34.227234 gigagan-pytorch-0.2.0/gigagan_pytorch/
--rw-r--r--   0 runner    (1001) docker     (123)      577 2023-07-23 16:49:23.000000 gigagan-pytorch-0.2.0/gigagan_pytorch/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2934 2023-07-23 16:49:23.000000 gigagan-pytorch-0.2.0/gigagan_pytorch/attend.py
--rw-r--r--   0 runner    (1001) docker     (123)     3136 2023-07-23 16:49:23.000000 gigagan-pytorch-0.2.0/gigagan_pytorch/data.py
--rw-r--r--   0 runner    (1001) docker     (123)    81269 2023-07-23 16:49:23.000000 gigagan-pytorch-0.2.0/gigagan_pytorch/gigagan_pytorch.py
--rw-r--r--   0 runner    (1001) docker     (123)     4617 2023-07-23 16:49:23.000000 gigagan-pytorch-0.2.0/gigagan_pytorch/open_clip.py
--rw-r--r--   0 runner    (1001) docker     (123)      953 2023-07-23 16:49:23.000000 gigagan-pytorch-0.2.0/gigagan_pytorch/optimizer.py
--rw-r--r--   0 runner    (1001) docker     (123)    17976 2023-07-23 16:49:23.000000 gigagan-pytorch-0.2.0/gigagan_pytorch/unet_upsampler.py
--rw-r--r--   0 runner    (1001) docker     (123)       22 2023-07-23 16:49:23.000000 gigagan-pytorch-0.2.0/gigagan_pytorch/version.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:49:34.227234 gigagan-pytorch-0.2.0/gigagan_pytorch.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)      612 2023-07-23 16:49:34.000000 gigagan-pytorch-0.2.0/gigagan_pytorch.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      467 2023-07-23 16:49:34.000000 gigagan-pytorch-0.2.0/gigagan_pytorch.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 16:49:34.000000 gigagan-pytorch-0.2.0/gigagan_pytorch.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      125 2023-07-23 16:49:34.000000 gigagan-pytorch-0.2.0/gigagan_pytorch.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       16 2023-07-23 16:49:34.000000 gigagan-pytorch-0.2.0/gigagan_pytorch.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       87 2023-07-23 16:49:23.000000 gigagan-pytorch-0.2.0/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 16:49:34.227234 gigagan-pytorch-0.2.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1017 2023-07-23 16:49:23.000000 gigagan-pytorch-0.2.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:30:20.833708 gigagan-pytorch-0.2.2/
+-rw-r--r--   0 runner    (1001) docker     (123)     1066 2023-07-23 17:30:09.000000 gigagan-pytorch-0.2.2/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      612 2023-07-23 17:30:20.833708 gigagan-pytorch-0.2.2/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     9314 2023-07-23 17:30:09.000000 gigagan-pytorch-0.2.2/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:30:20.833708 gigagan-pytorch-0.2.2/gigagan_pytorch/
+-rw-r--r--   0 runner    (1001) docker     (123)      577 2023-07-23 17:30:09.000000 gigagan-pytorch-0.2.2/gigagan_pytorch/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2934 2023-07-23 17:30:09.000000 gigagan-pytorch-0.2.2/gigagan_pytorch/attend.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3136 2023-07-23 17:30:09.000000 gigagan-pytorch-0.2.2/gigagan_pytorch/data.py
+-rw-r--r--   0 runner    (1001) docker     (123)    81269 2023-07-23 17:30:09.000000 gigagan-pytorch-0.2.2/gigagan_pytorch/gigagan_pytorch.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4617 2023-07-23 17:30:09.000000 gigagan-pytorch-0.2.2/gigagan_pytorch/open_clip.py
+-rw-r--r--   0 runner    (1001) docker     (123)      953 2023-07-23 17:30:09.000000 gigagan-pytorch-0.2.2/gigagan_pytorch/optimizer.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18170 2023-07-23 17:30:09.000000 gigagan-pytorch-0.2.2/gigagan_pytorch/unet_upsampler.py
+-rw-r--r--   0 runner    (1001) docker     (123)       22 2023-07-23 17:30:09.000000 gigagan-pytorch-0.2.2/gigagan_pytorch/version.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:30:20.833708 gigagan-pytorch-0.2.2/gigagan_pytorch.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)      612 2023-07-23 17:30:20.000000 gigagan-pytorch-0.2.2/gigagan_pytorch.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      467 2023-07-23 17:30:20.000000 gigagan-pytorch-0.2.2/gigagan_pytorch.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 17:30:20.000000 gigagan-pytorch-0.2.2/gigagan_pytorch.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      125 2023-07-23 17:30:20.000000 gigagan-pytorch-0.2.2/gigagan_pytorch.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       16 2023-07-23 17:30:20.000000 gigagan-pytorch-0.2.2/gigagan_pytorch.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       87 2023-07-23 17:30:09.000000 gigagan-pytorch-0.2.2/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 17:30:20.833708 gigagan-pytorch-0.2.2/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1017 2023-07-23 17:30:09.000000 gigagan-pytorch-0.2.2/setup.py
```

### Comparing `gigagan-pytorch-0.2.0/LICENSE` & `gigagan-pytorch-0.2.2/LICENSE`

 * *Files identical despite different names*

### Comparing `gigagan-pytorch-0.2.0/PKG-INFO` & `gigagan-pytorch-0.2.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: gigagan-pytorch
-Version: 0.2.0
+Version: 0.2.2
 Summary: GigaGAN - Pytorch
 Home-page: https://github.com/lucidrains/ETSformer-pytorch
 Author: Phil Wang
 Author-email: lucidrains@gmail.com
 License: MIT
 Keywords: artificial intelligence,deep learning,generative adversarial networks
 Classifier: Development Status :: 4 - Beta
```

### Comparing `gigagan-pytorch-0.2.0/README.md` & `gigagan-pytorch-0.2.2/README.md`

 * *Files identical despite different names*

### Comparing `gigagan-pytorch-0.2.0/gigagan_pytorch/__init__.py` & `gigagan-pytorch-0.2.2/gigagan_pytorch/__init__.py`

 * *Files identical despite different names*

### Comparing `gigagan-pytorch-0.2.0/gigagan_pytorch/attend.py` & `gigagan-pytorch-0.2.2/gigagan_pytorch/attend.py`

 * *Files identical despite different names*

### Comparing `gigagan-pytorch-0.2.0/gigagan_pytorch/data.py` & `gigagan-pytorch-0.2.2/gigagan_pytorch/data.py`

 * *Files identical despite different names*

### Comparing `gigagan-pytorch-0.2.0/gigagan_pytorch/gigagan_pytorch.py` & `gigagan-pytorch-0.2.2/gigagan_pytorch/gigagan_pytorch.py`

 * *Files identical despite different names*

### Comparing `gigagan-pytorch-0.2.0/gigagan_pytorch/open_clip.py` & `gigagan-pytorch-0.2.2/gigagan_pytorch/open_clip.py`

 * *Files identical despite different names*

### Comparing `gigagan-pytorch-0.2.0/gigagan_pytorch/optimizer.py` & `gigagan-pytorch-0.2.2/gigagan_pytorch/optimizer.py`

 * *Files identical despite different names*

### Comparing `gigagan-pytorch-0.2.0/gigagan_pytorch/unet_upsampler.py` & `gigagan-pytorch-0.2.2/gigagan_pytorch/unet_upsampler.py`

 * *Files 2% similar despite different names*

```diff
@@ -314,15 +314,16 @@
         attn_depths = (1, 1, 1, 1),
         cross_attn_dim_head = 64,
         cross_attn_heads = 8,
         cross_ff_mult = 4,
         mid_attn_depth = 1,
         num_conv_kernels = 2,
         resize_mode = 'bilinear',
-        unconditional = True
+        unconditional = True,
+        skip_connect_scale = None
     ):
         super().__init__()
 
         # style network
 
         if isinstance(text_encoder, dict):
             text_encoder = TextEncoder(**text_encoder)
@@ -383,14 +384,18 @@
         assert len(full_attn) == len(dim_mults)
 
         FullAttention = partial(Transformer, flash_attn = flash_attn)
 
         cross_attn = cast_tuple(cross_attn, length = len(dim_mults))
         assert unconditional or len(full_attn) == len(dim_mults)
 
+        # skip connection scale
+
+        self.skip_connect_scale = default(skip_connect_scale, 2 ** -0.5)
+
         # layers
 
         self.downs = nn.ModuleList([])
         self.ups = nn.ModuleList([])
         num_resolutions = len(in_out)
 
         for ind, ((dim_in, dim_out), layer_full_attn, layer_cross_attn, layer_attn_depth) in enumerate(zip(in_out, full_attn, cross_attn, attn_depths)):
@@ -540,16 +545,16 @@
         # upsample stages
 
         for upsample, upsample_rgb, to_rgb, block1, block2, cross_attn, attn in self.ups:
 
             x = upsample(x)
             rgb = upsample_rgb(rgb)
 
-            res1 = h.pop()
-            res2 = h.pop()
+            res1 = h.pop() * self.skip_connect_scale
+            res2 = h.pop() * self.skip_connect_scale
 
             fmap_size = x.shape[-1]
             residual_fmap_size = res1.shape[-1]
 
             if residual_fmap_size != fmap_size:
                 res1 = self.resize_image_to(res1, fmap_size)
                 res2 = self.resize_image_to(res2, fmap_size)
```

### Comparing `gigagan-pytorch-0.2.0/gigagan_pytorch.egg-info/PKG-INFO` & `gigagan-pytorch-0.2.2/gigagan_pytorch.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: gigagan-pytorch
-Version: 0.2.0
+Version: 0.2.2
 Summary: GigaGAN - Pytorch
 Home-page: https://github.com/lucidrains/ETSformer-pytorch
 Author: Phil Wang
 Author-email: lucidrains@gmail.com
 License: MIT
 Keywords: artificial intelligence,deep learning,generative adversarial networks
 Classifier: Development Status :: 4 - Beta
```

### Comparing `gigagan-pytorch-0.2.0/setup.py` & `gigagan-pytorch-0.2.2/setup.py`

 * *Files identical despite different names*

