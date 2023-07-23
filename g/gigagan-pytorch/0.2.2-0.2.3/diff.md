# Comparing `tmp/gigagan-pytorch-0.2.2.tar.gz` & `tmp/gigagan-pytorch-0.2.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "gigagan-pytorch-0.2.2.tar", last modified: Sun Jul 23 17:30:20 2023, max compression
+gzip compressed data, was "gigagan-pytorch-0.2.3.tar", last modified: Sun Jul 23 19:02:52 2023, max compression
```

## Comparing `gigagan-pytorch-0.2.2.tar` & `gigagan-pytorch-0.2.3.tar`

### file list

```diff
@@ -1,22 +1,22 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:30:20.833708 gigagan-pytorch-0.2.2/
--rw-r--r--   0 runner    (1001) docker     (123)     1066 2023-07-23 17:30:09.000000 gigagan-pytorch-0.2.2/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      612 2023-07-23 17:30:20.833708 gigagan-pytorch-0.2.2/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     9314 2023-07-23 17:30:09.000000 gigagan-pytorch-0.2.2/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:30:20.833708 gigagan-pytorch-0.2.2/gigagan_pytorch/
--rw-r--r--   0 runner    (1001) docker     (123)      577 2023-07-23 17:30:09.000000 gigagan-pytorch-0.2.2/gigagan_pytorch/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2934 2023-07-23 17:30:09.000000 gigagan-pytorch-0.2.2/gigagan_pytorch/attend.py
--rw-r--r--   0 runner    (1001) docker     (123)     3136 2023-07-23 17:30:09.000000 gigagan-pytorch-0.2.2/gigagan_pytorch/data.py
--rw-r--r--   0 runner    (1001) docker     (123)    81269 2023-07-23 17:30:09.000000 gigagan-pytorch-0.2.2/gigagan_pytorch/gigagan_pytorch.py
--rw-r--r--   0 runner    (1001) docker     (123)     4617 2023-07-23 17:30:09.000000 gigagan-pytorch-0.2.2/gigagan_pytorch/open_clip.py
--rw-r--r--   0 runner    (1001) docker     (123)      953 2023-07-23 17:30:09.000000 gigagan-pytorch-0.2.2/gigagan_pytorch/optimizer.py
--rw-r--r--   0 runner    (1001) docker     (123)    18170 2023-07-23 17:30:09.000000 gigagan-pytorch-0.2.2/gigagan_pytorch/unet_upsampler.py
--rw-r--r--   0 runner    (1001) docker     (123)       22 2023-07-23 17:30:09.000000 gigagan-pytorch-0.2.2/gigagan_pytorch/version.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 17:30:20.833708 gigagan-pytorch-0.2.2/gigagan_pytorch.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)      612 2023-07-23 17:30:20.000000 gigagan-pytorch-0.2.2/gigagan_pytorch.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      467 2023-07-23 17:30:20.000000 gigagan-pytorch-0.2.2/gigagan_pytorch.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 17:30:20.000000 gigagan-pytorch-0.2.2/gigagan_pytorch.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      125 2023-07-23 17:30:20.000000 gigagan-pytorch-0.2.2/gigagan_pytorch.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       16 2023-07-23 17:30:20.000000 gigagan-pytorch-0.2.2/gigagan_pytorch.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       87 2023-07-23 17:30:09.000000 gigagan-pytorch-0.2.2/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 17:30:20.833708 gigagan-pytorch-0.2.2/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1017 2023-07-23 17:30:09.000000 gigagan-pytorch-0.2.2/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:02:52.427186 gigagan-pytorch-0.2.3/
+-rw-r--r--   0 runner    (1001) docker     (123)     1066 2023-07-23 19:02:37.000000 gigagan-pytorch-0.2.3/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      612 2023-07-23 19:02:52.427186 gigagan-pytorch-0.2.3/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     9289 2023-07-23 19:02:37.000000 gigagan-pytorch-0.2.3/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:02:52.423186 gigagan-pytorch-0.2.3/gigagan_pytorch/
+-rw-r--r--   0 runner    (1001) docker     (123)      577 2023-07-23 19:02:37.000000 gigagan-pytorch-0.2.3/gigagan_pytorch/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2934 2023-07-23 19:02:37.000000 gigagan-pytorch-0.2.3/gigagan_pytorch/attend.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3136 2023-07-23 19:02:37.000000 gigagan-pytorch-0.2.3/gigagan_pytorch/data.py
+-rw-r--r--   0 runner    (1001) docker     (123)    83421 2023-07-23 19:02:37.000000 gigagan-pytorch-0.2.3/gigagan_pytorch/gigagan_pytorch.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4617 2023-07-23 19:02:37.000000 gigagan-pytorch-0.2.3/gigagan_pytorch/open_clip.py
+-rw-r--r--   0 runner    (1001) docker     (123)      953 2023-07-23 19:02:37.000000 gigagan-pytorch-0.2.3/gigagan_pytorch/optimizer.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18170 2023-07-23 19:02:37.000000 gigagan-pytorch-0.2.3/gigagan_pytorch/unet_upsampler.py
+-rw-r--r--   0 runner    (1001) docker     (123)       22 2023-07-23 19:02:37.000000 gigagan-pytorch-0.2.3/gigagan_pytorch/version.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 19:02:52.423186 gigagan-pytorch-0.2.3/gigagan_pytorch.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)      612 2023-07-23 19:02:52.000000 gigagan-pytorch-0.2.3/gigagan_pytorch.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      467 2023-07-23 19:02:52.000000 gigagan-pytorch-0.2.3/gigagan_pytorch.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 19:02:52.000000 gigagan-pytorch-0.2.3/gigagan_pytorch.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      125 2023-07-23 19:02:52.000000 gigagan-pytorch-0.2.3/gigagan_pytorch.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       16 2023-07-23 19:02:52.000000 gigagan-pytorch-0.2.3/gigagan_pytorch.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       87 2023-07-23 19:02:37.000000 gigagan-pytorch-0.2.3/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 19:02:52.427186 gigagan-pytorch-0.2.3/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1017 2023-07-23 19:02:37.000000 gigagan-pytorch-0.2.3/setup.py
```

### Comparing `gigagan-pytorch-0.2.2/LICENSE` & `gigagan-pytorch-0.2.3/LICENSE`

 * *Files identical despite different names*

### Comparing `gigagan-pytorch-0.2.2/PKG-INFO` & `gigagan-pytorch-0.2.3/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: gigagan-pytorch
-Version: 0.2.2
+Version: 0.2.3
 Summary: GigaGAN - Pytorch
 Home-page: https://github.com/lucidrains/ETSformer-pytorch
 Author: Phil Wang
 Author-email: lucidrains@gmail.com
 License: MIT
 Keywords: artificial intelligence,deep learning,generative adversarial networks
 Classifier: Development Status :: 4 - Beta
```

### Comparing `gigagan-pytorch-0.2.2/README.md` & `gigagan-pytorch-0.2.3/README.md`

 * *Files 4% similar despite different names*

```diff
@@ -193,28 +193,27 @@
     - [x] add contrastive loss for generator
     - [x] add vision aided loss
     - [x] add gradient penalty for vision aided discr - make optional
     - [x] add matching awareness loss - figure out if rotating text conditions by one is good enough for mismatching (without drawing an additional batch from dataloader)
     - [x] make sure gradient accumulation works with matching aware loss
     - [x] matching awareness loss runs and is stable
     - [x] vision aided trains
+- [x] add some differentiable augmentations, proven technique from the old GAN days
+    - [x] remove any magic being done with automatic rgbs processing, and have it explicitly passed in - offer functions on the discriminator that can process real images into the right multi-scales
+    - [x] add horizontal flip for starters
 
 - [ ] add accelerate
     - [x] works single machine
     - [x] works for mixed precision (make sure gradient penalty is scaled correctly), take care of manual scaler saving and reloading, borrow from imagen-pytorch
     - [x] make sure it works multi-GPU for one machine
     - [ ] have someone else try multiple machines
 
 - [ ] clip should be optional for all modules, and managed by `GigaGAN`, with text -> text embeds processed once
 - [ ] add ability to select a random subset from multiscale dimension, for efficiency
 
-- [ ] add some differentiable augmentations, proven technique from the old GAN days
-    - [ ] remove any magic being done with automatic rgbs processing, and have it explicitly passed in - offer functions on the discriminator that can process real images into the right multi-scales
-    - [ ] add horizontal flip for starters
-
 - [ ] port over CLI from lightweight|stylegan2-pytorch
 - [ ] hook up laion dataset for text-image
 
 ## Citations
 
 ```bibtex
 @misc{https://doi.org/10.48550/arxiv.2303.05511,
@@ -242,15 +241,15 @@
     title   = {Flash{A}ttention: Fast and Memory-Efficient Exact Attention with {IO}-Awareness},
     author  = {Dao, Tri and Fu, Daniel Y. and Ermon, Stefano and Rudra, Atri and R{\'e}, Christopher},
     booktitle = {Advances in Neural Information Processing Systems},
     year    = {2022}
 }
 ```
 
-```bibtex
-@inproceedings{Heusel2017GANsTB,
-    title   = {GANs Trained by a Two Time-Scale Update Rule Converge to a Local Nash Equilibrium},
-    author  = {Martin Heusel and Hubert Ramsauer and Thomas Unterthiner and Bernhard Nessler and Sepp Hochreiter},
-    booktitle = {NIPS},
-    year    = {2017}
-}
 ```
+@inproceedings{Karras2020ada,
+  title     = {Training Generative Adversarial Networks with Limited Data},
+  author    = {Tero Karras and Miika Aittala and Janne Hellsten and Samuli Laine and Jaakko Lehtinen and Timo Aila},
+  booktitle = {Proc. NeurIPS},
+  year      = {2020}
+}
+```
```

#### html2text {}

```diff
@@ -70,36 +70,36 @@
 generator and discriminator can also accept pre-encoded CLIP text encodings -
 [x] do a review of the auxiliary losses - [x] add contrastive loss for
 generator - [x] add vision aided loss - [x] add gradient penalty for vision
 aided discr - make optional - [x] add matching awareness loss - figure out if
 rotating text conditions by one is good enough for mismatching (without drawing
 an additional batch from dataloader) - [x] make sure gradient accumulation
 works with matching aware loss - [x] matching awareness loss runs and is stable
-- [x] vision aided trains - [ ] add accelerate - [x] works single machine - [x]
-works for mixed precision (make sure gradient penalty is scaled correctly),
-take care of manual scaler saving and reloading, borrow from imagen-pytorch -
-[x] make sure it works multi-GPU for one machine - [ ] have someone else try
-multiple machines - [ ] clip should be optional for all modules, and managed by
-`GigaGAN`, with text -> text embeds processed once - [ ] add ability to select
-a random subset from multiscale dimension, for efficiency - [ ] add some
-differentiable augmentations, proven technique from the old GAN days - [ ]
-remove any magic being done with automatic rgbs processing, and have it
-explicitly passed in - offer functions on the discriminator that can process
-real images into the right multi-scales - [ ] add horizontal flip for starters
-- [ ] port over CLI from lightweight|stylegan2-pytorch - [ ] hook up laion
-dataset for text-image ## Citations ```bibtex @misc{https://doi.org/10.48550/
-arxiv.2303.05511, url = {https://arxiv.org/abs/2303.05511}, author = {Kang,
-Minguk and Zhu, Jun-Yan and Zhang, Richard and Park, Jaesik and Shechtman, Eli
-and Paris, Sylvain and Park, Taesung}, title = {Scaling up GANs for Text-to-
-Image Synthesis}, publisher = {arXiv}, year = {2023}, copyright = {arXiv.org
-perpetual, non-exclusive license} } ``` ```bibtex @article{Liu2021TowardsFA,
-title = {Towards Faster and Stabilized GAN Training for High-fidelity Few-shot
-Image Synthesis}, author = {Bingchen Liu and Yizhe Zhu and Kunpeng Song and A.
-Elgammal}, journal = {ArXiv}, year = {2021}, volume = {abs/2101.04775} } ```
-```bibtex @inproceedings{dao2022flashattention, title = {Flash{A}ttention: Fast
-and Memory-Efficient Exact Attention with {IO}-Awareness}, author = {Dao, Tri
-and Fu, Daniel Y. and Ermon, Stefano and Rudra, Atri and R{\'e}, Christopher},
-booktitle = {Advances in Neural Information Processing Systems}, year = {2022}
-} ``` ```bibtex @inproceedings{Heusel2017GANsTB, title = {GANs Trained by a Two
-Time-Scale Update Rule Converge to a Local Nash Equilibrium}, author = {Martin
-Heusel and Hubert Ramsauer and Thomas Unterthiner and Bernhard Nessler and Sepp
-Hochreiter}, booktitle = {NIPS}, year = {2017} } ```
+- [x] vision aided trains - [x] add some differentiable augmentations, proven
+technique from the old GAN days - [x] remove any magic being done with
+automatic rgbs processing, and have it explicitly passed in - offer functions
+on the discriminator that can process real images into the right multi-scales -
+[x] add horizontal flip for starters - [ ] add accelerate - [x] works single
+machine - [x] works for mixed precision (make sure gradient penalty is scaled
+correctly), take care of manual scaler saving and reloading, borrow from
+imagen-pytorch - [x] make sure it works multi-GPU for one machine - [ ] have
+someone else try multiple machines - [ ] clip should be optional for all
+modules, and managed by `GigaGAN`, with text -> text embeds processed once -
+[ ] add ability to select a random subset from multiscale dimension, for
+efficiency - [ ] port over CLI from lightweight|stylegan2-pytorch - [ ] hook up
+laion dataset for text-image ## Citations ```bibtex @misc{https://doi.org/
+10.48550/arxiv.2303.05511, url = {https://arxiv.org/abs/2303.05511}, author =
+{Kang, Minguk and Zhu, Jun-Yan and Zhang, Richard and Park, Jaesik and
+Shechtman, Eli and Paris, Sylvain and Park, Taesung}, title = {Scaling up GANs
+for Text-to-Image Synthesis}, publisher = {arXiv}, year = {2023}, copyright =
+{arXiv.org perpetual, non-exclusive license} } ``` ```bibtex @article
+{Liu2021TowardsFA, title = {Towards Faster and Stabilized GAN Training for
+High-fidelity Few-shot Image Synthesis}, author = {Bingchen Liu and Yizhe Zhu
+and Kunpeng Song and A. Elgammal}, journal = {ArXiv}, year = {2021}, volume =
+{abs/2101.04775} } ``` ```bibtex @inproceedings{dao2022flashattention, title =
+{Flash{A}ttention: Fast and Memory-Efficient Exact Attention with {IO}-
+Awareness}, author = {Dao, Tri and Fu, Daniel Y. and Ermon, Stefano and Rudra,
+Atri and R{\'e}, Christopher}, booktitle = {Advances in Neural Information
+Processing Systems}, year = {2022} } ``` ``` @inproceedings{Karras2020ada,
+title = {Training Generative Adversarial Networks with Limited Data}, author =
+{Tero Karras and Miika Aittala and Janne Hellsten and Samuli Laine and Jaakko
+Lehtinen and Timo Aila}, booktitle = {Proc. NeurIPS}, year = {2020} } ```
```

### Comparing `gigagan-pytorch-0.2.2/gigagan_pytorch/__init__.py` & `gigagan-pytorch-0.2.3/gigagan_pytorch/__init__.py`

 * *Files identical despite different names*

### Comparing `gigagan-pytorch-0.2.2/gigagan_pytorch/attend.py` & `gigagan-pytorch-0.2.3/gigagan_pytorch/attend.py`

 * *Files identical despite different names*

### Comparing `gigagan-pytorch-0.2.2/gigagan_pytorch/data.py` & `gigagan-pytorch-0.2.3/gigagan_pytorch/data.py`

 * *Files identical despite different names*

### Comparing `gigagan-pytorch-0.2.2/gigagan_pytorch/gigagan_pytorch.py` & `gigagan-pytorch-0.2.3/gigagan_pytorch/gigagan_pytorch.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,11 @@
 from collections import namedtuple
 from pathlib import Path
 from math import log2, sqrt
+from random import random
 from functools import partial
 
 from torchvision import utils
 
 import torch
 import torch.nn.functional as F
 from torch import nn, einsum, Tensor
@@ -35,15 +36,15 @@
 
 # helpers
 
 def exists(val):
     return val is not None
 
 @beartype
-def is_empty(arr: Union[Tuple, Dict, List]):
+def is_empty(arr: Iterable):
     return len(arr) == 0
 
 def default(*vals):
     for val in vals:
         if exists(val):
             return val
     return None
@@ -174,14 +175,46 @@
     assert exists(texts) ^ exists(text_embeds)
 
     if exists(texts):
         text_embeds, _ = clip.embed_texts(texts)
 
     return clip.contrastive_loss(images = images, text_embeds = text_embeds)
 
+# differentiable augmentation - Karras et al. stylegan-ada
+# start with horizontal flip
+
+class DiffAugment(nn.Module):
+    def __init__(
+        self,
+        *,
+        prob,
+        horizontal_flip,
+        horizontal_flip_prob = 0.5
+    ):
+        super().__init__()
+        self.prob = prob
+        assert 0 <= prob <= 1.
+
+        self.horizontal_flip = horizontal_flip
+        self.horizontal_flip_prob = horizontal_flip_prob
+
+    def forward(
+        self,
+        images,
+        rgbs: List[Tensor]
+    ):
+        if random() >= self.prob:
+            return images, rgbs
+
+        if random() < self.horizontal_flip_prob:
+            images = torch.flip(images, (-1,))
+            rgbs = [torch.flip(rgb, (-1,)) for rgb in rgbs]
+
+        return images, rgbs
+
 # rmsnorm (newer papers show mean-centering in layernorm not necessary)
 
 class ChannelRMSNorm(nn.Module):
     def __init__(self, dim):
         super().__init__()
         self.scale = dim ** 0.5
         self.gamma = nn.Parameter(torch.ones(dim, 1, 1))
@@ -1547,15 +1580,15 @@
     def device(self):
         return next(self.parameters()).device
 
     @beartype
     def forward(
         self,
         images,
-        rgbs: Optional[List[Tensor]] = None,  # multi-resolution inputs (rgbs) from the generator
+        rgbs: List[Tensor],                   # multi-resolution inputs (rgbs) from the generator
         texts: Optional[List[str]] = None,
         text_encodings: Optional[Tensor] = None,
         text_embeds = None,
         real_images = None,                   # if this were passed in, the network will automatically append the real to the presumably generated images passed in as the first argument, and generate all intermediate resolutions through resizing and concat appropriately
         return_multiscale_outputs = True,     # can force it not to return multi-scale logits
         calc_aux_loss = True
     ):
@@ -1585,14 +1618,18 @@
 
         batch = x.shape[0]
 
         # index the rgbs by resolution
 
         rgbs_index = {t.shape[-1]: t for t in rgbs} if exists(rgbs) else {}
 
+        # assert that the necessary resolutions are there
+
+        assert is_empty(set(self.multiscale_input_resolutions) - set(rgbs_index.keys())), f'rgbs of necessary resolution {self.multiscale_input_resolutions} were not passed in'
+
         # hold multiscale outputs
 
         multiscale_outputs = []
 
         # hold auxiliary recon losses
 
         aux_recon_losses = []
@@ -1616,19 +1653,14 @@
 
             batch_prev_stage = x.shape[0]
             has_multiscale_input = resolution in self.multiscale_input_resolutions
 
             if has_multiscale_input:
                 rgb = rgbs_index.get(resolution, None)
 
-                # if no rgbs passed in, assume all real images, and just resize, though realistically you would concat fake and real images together using helper function `create_real_fake_rgbs` function
-
-                if not exists(rgb):
-                    rgb = self.resize_image_to(images, resolution)
-
                 # multi-scale input features
 
                 multi_scale_input_feats = from_rgb(rgb)
 
                 # expand multi-scale input features, as could include extra scales from previous stage
 
                 multi_scale_input_feats = repeat(multi_scale_input_feats, 'b ... -> (s b) ...', s = x.shape[0] // rgb.shape[0])
@@ -1712,25 +1744,26 @@
     @beartype
     def __init__(
         self,
         *,
         generator: Union[BaseGenerator, Dict],
         discriminator: Union[Discriminator, Dict],
         vision_aided_discriminator: Optional[Union[VisionAidedDiscriminator, Dict]] = None,
+        diff_augment: Optional[Union[DiffAugment, Dict]] = None,
         learning_rate = 2e-4,
         betas = (0.5, 0.9),
         weight_decay = 0.,
         discr_aux_recon_loss_weight = 1.,
         multiscale_divergence_loss_weight = 0.1,
         vision_aided_divergence_loss_weight = 0.5,
         generator_contrastive_loss_weight = 0.1,
         matching_awareness_loss_weight = 0.1,
         calc_multiscale_loss_every = 1,
         apply_gradient_penalty_every = 4,
-        ttur_mult = 1,
+        resize_image_mode = 'bilinear',
         train_upsampler = False,
         upsampler_replace_rgb_with_input_lowres_image = False,
         log_steps_every = 20,
         create_ema_generator_at_init = True,
         save_and_sample_every = 1000,
         early_save_thres_steps = 2500,
         early_save_and_sample_every = 100,
@@ -1784,14 +1817,21 @@
             discriminator = Discriminator(**discriminator)
 
         if exists(vision_aided_discriminator) and isinstance(vision_aided_discriminator, dict):
             vision_aided_discriminator = VisionAidedDiscriminator(**vision_aided_discriminator)
 
         assert isinstance(generator, generator_klass)
 
+        # diff augment
+
+        if isinstance(diff_augment, dict):
+            diff_augment = DiffAugment(**diff_augment)
+
+        self.diff_augment = diff_augment
+
         # use _base to designate unwrapped models
 
         self.G = generator
         self.D = discriminator
         self.VD = vision_aided_discriminator
 
         # ema
@@ -1819,15 +1859,15 @@
         assert not exists(vision_aided_discriminator) or vision_aided_discriminator.unconditional == generator.unconditional
 
         self.unconditional = generator.unconditional
 
         # optimizers
 
         self.G_opt = get_optimizer(self.G.parameters(), lr = learning_rate, betas = betas, weight_decay = weight_decay)
-        self.D_opt = get_optimizer(self.D.parameters(), lr = learning_rate * ttur_mult, betas = betas, weight_decay = weight_decay)
+        self.D_opt = get_optimizer(self.D.parameters(), lr = learning_rate, betas = betas, weight_decay = weight_decay)
 
         # prepare for distributed
 
         self.G, self.D, self.G_opt, self.D_opt = self.accelerator.prepare(self.G, self.D, self.G_opt, self.D_opt)
 
         # vision aided discriminator optimizer
 
@@ -1839,14 +1879,18 @@
 
         self.discr_aux_recon_loss_weight = discr_aux_recon_loss_weight
         self.multiscale_divergence_loss_weight = multiscale_divergence_loss_weight
         self.vision_aided_divergence_loss_weight = vision_aided_divergence_loss_weight
         self.generator_contrastive_loss_weight = generator_contrastive_loss_weight
         self.matching_awareness_loss_weight = matching_awareness_loss_weight
 
+        # resize image mode
+
+        self.resize_image_mode = resize_image_mode
+
         # steps
 
         self.log_steps_every = log_steps_every
 
         self.register_buffer('steps', torch.ones(1, dtype = torch.long))
 
         # save and sample
@@ -1983,14 +2027,17 @@
     def is_main(self):
         return self.accelerator.is_main_process
 
     @property
     def is_local_main(self):
         return self.accelerator.is_local_main_process
 
+    def resize_image_to(self, images, resolution):
+        return F.interpolate(images, resolution, mode = self.resize_image_mode)
+
     @beartype
     def set_dataloader(self, dl: DataLoader):
         assert not exists(self.train_dl), 'training dataloader has already been set'
 
         self.train_dl = dl
         self.train_dl_batch_size = dl.batch_size
 
@@ -2097,14 +2144,23 @@
                 all_texts.extend(texts)
 
             # requires grad for real images, for gradient penalty
 
             real_images = real_images.to(self.device)
             real_images.requires_grad_()
 
+            real_images_rgbs = [self.resize_image_to(real_images, resolution) for resolution in self.D.multiscale_input_resolutions]
+
+            # diff augment real images
+
+            if exists(self.diff_augment):
+                real_images, real_images_rgbs = self.diff_augment(real_images, real_images_rgbs)
+
+            # batch size
+
             batch_size = real_images.shape[0]
 
             # for discriminator training, fit upsampler and image synthesis logic under same function
 
             G_kwargs, maybe_text_kwargs = self.generate_kwargs(dl_iter, batch_size)
 
             # generator
@@ -2115,14 +2171,19 @@
                     **maybe_text_kwargs,
                     return_all_rgbs = True
                 )
 
                 all_fake_images.append(images)
                 all_fake_rgbs.append(rgbs)
 
+                # diff augment
+
+                if exists(self.diff_augment):
+                    images, rgbs = self.diff_augment(images, rgbs)
+
                 # detach output of generator, as training discriminator only
 
                 images.detach_()
 
                 for rgb in rgbs:
                     rgb.detach_()
 
@@ -2135,14 +2196,15 @@
                     **maybe_text_kwargs,
                     return_multiscale_outputs = calc_multiscale_loss,
                     calc_aux_loss = False
                 )
 
                 real_logits, real_multiscale_logits, aux_recon_losses = self.D(
                     real_images,
+                    real_images_rgbs,
                     **maybe_text_kwargs,
                     return_multiscale_outputs = calc_multiscale_loss,
                     calc_aux_loss = True
                 )
 
                 divergence = discriminator_hinge_loss(real_logits, fake_logits)
                 total_divergence += (divergence.item() / grad_accum_every)
@@ -2304,30 +2366,35 @@
         for _ in range(grad_accum_every):
 
             # generator
             
             G_kwargs, maybe_text_kwargs = self.generate_kwargs(dl_iter, batch_size)
 
             with self.accelerator.autocast():
-                image, rgbs = self.G(
+                images, rgbs = self.G(
                     **G_kwargs,
                     **maybe_text_kwargs,
                     return_all_rgbs = True
                 )
 
+                # diff augment
+
+                if exists(self.diff_augment):
+                    images, rgbs = self.diff_augment(images, rgbs)
+
                 # accumulate all images and texts for maybe contrastive loss
 
                 if self.need_contrastive_loss:
-                    all_images.append(image)
+                    all_images.append(images)
                     all_texts.extend(maybe_text_kwargs['texts'])
 
                 # discriminator
 
                 logits, multiscale_logits, _ = self.D(
-                    image,
+                    images,
                     rgbs,
                     **maybe_text_kwargs,
                     return_multiscale_outputs = calc_multiscale_loss,
                     calc_aux_loss = False
                 )
 
                 # generator hinge loss discriminator and multiscale
@@ -2349,15 +2416,15 @@
                     total_loss = total_loss + multiscale_divergence * self.multiscale_divergence_loss_weight
 
                 # vision aided generator hinge loss
 
                 if self.need_vision_aided_discriminator:
                     vd_loss = 0.
 
-                    logits = self.VD(image, **maybe_text_kwargs)
+                    logits = self.VD(images, **maybe_text_kwargs)
 
                     for logit in logits:
                         vd_loss = vd_loss + generator_hinge_loss(logit)
 
                     total_vd_divergence += (vd_loss.item() / grad_accum_every)
 
                     total_loss = total_loss + vd_loss * self.vision_aided_divergence_loss_weight
@@ -2505,15 +2572,31 @@
             if exists(multiscale_d_loss):
                 last_multiscale_d_loss = multiscale_d_loss
 
             if exists(multiscale_g_loss):
                 last_multiscale_g_loss = multiscale_g_loss
 
             if is_first_step or divisible_by(steps, self.log_steps_every):
-                self.print(f' G: {g_loss:.2f} | MSG: {last_multiscale_g_loss:.2f} | VG: {vision_aided_g_loss:.2f} | D: {d_loss:.2f} | MSD: {last_multiscale_d_loss:.2f} | VD: {vision_aided_d_loss:.2f} | GP: {last_gp_loss:.2f} | SSL: {recon_loss:.2f} | CL: {contrastive_loss:.2f} | MAL: {matching_aware_loss:.2f}')
+
+                losses = (
+                    ('G', g_loss),
+                    ('MSG', last_multiscale_g_loss),
+                    ('VG', vision_aided_g_loss),
+                    ('D', d_loss),
+                    ('MSD', last_multiscale_d_loss),
+                    ('VD', vision_aided_d_loss),
+                    ('GP', last_gp_loss),
+                    ('SSL', recon_loss),
+                    ('CL', contrastive_loss),
+                    ('MAL', matching_aware_loss)
+                )
+
+                losses_str = ' | '.join([f'{loss_name}: {loss:.2f}' for loss_name, loss in losses])
+
+                self.print(losses_str)
 
             self.accelerator.wait_for_everyone()
 
             if self.is_main and (is_first_step or divisible_by(steps, self.save_and_sample_every) or (steps <= self.early_save_thres_steps and divisible_by(steps, self.early_save_and_sample_every))):
                 self.save_sample(batch_size, dl_iter)
             
             self.steps += 1
```

### Comparing `gigagan-pytorch-0.2.2/gigagan_pytorch/open_clip.py` & `gigagan-pytorch-0.2.3/gigagan_pytorch/open_clip.py`

 * *Files identical despite different names*

### Comparing `gigagan-pytorch-0.2.2/gigagan_pytorch/optimizer.py` & `gigagan-pytorch-0.2.3/gigagan_pytorch/optimizer.py`

 * *Files identical despite different names*

### Comparing `gigagan-pytorch-0.2.2/gigagan_pytorch/unet_upsampler.py` & `gigagan-pytorch-0.2.3/gigagan_pytorch/unet_upsampler.py`

 * *Files identical despite different names*

### Comparing `gigagan-pytorch-0.2.2/gigagan_pytorch.egg-info/PKG-INFO` & `gigagan-pytorch-0.2.3/gigagan_pytorch.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: gigagan-pytorch
-Version: 0.2.2
+Version: 0.2.3
 Summary: GigaGAN - Pytorch
 Home-page: https://github.com/lucidrains/ETSformer-pytorch
 Author: Phil Wang
 Author-email: lucidrains@gmail.com
 License: MIT
 Keywords: artificial intelligence,deep learning,generative adversarial networks
 Classifier: Development Status :: 4 - Beta
```

### Comparing `gigagan-pytorch-0.2.2/setup.py` & `gigagan-pytorch-0.2.3/setup.py`

 * *Files identical despite different names*

