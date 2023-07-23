# Comparing `tmp/gigagan-pytorch-0.1.9.tar.gz` & `tmp/gigagan-pytorch-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "gigagan-pytorch-0.1.9.tar", last modified: Thu Jul 20 19:30:08 2023, max compression
+gzip compressed data, was "gigagan-pytorch-0.2.0.tar", last modified: Sun Jul 23 16:49:34 2023, max compression
```

## Comparing `gigagan-pytorch-0.1.9.tar` & `gigagan-pytorch-0.2.0.tar`

### file list

```diff
@@ -1,22 +1,22 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-20 19:30:08.250156 gigagan-pytorch-0.1.9/
--rw-r--r--   0 runner    (1001) docker     (123)     1066 2023-07-20 19:29:58.000000 gigagan-pytorch-0.1.9/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      612 2023-07-20 19:30:08.250156 gigagan-pytorch-0.1.9/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     8704 2023-07-20 19:29:58.000000 gigagan-pytorch-0.1.9/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-20 19:30:08.246156 gigagan-pytorch-0.1.9/gigagan_pytorch/
--rw-r--r--   0 runner    (1001) docker     (123)      517 2023-07-20 19:29:58.000000 gigagan-pytorch-0.1.9/gigagan_pytorch/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2934 2023-07-20 19:29:58.000000 gigagan-pytorch-0.1.9/gigagan_pytorch/attend.py
--rw-r--r--   0 runner    (1001) docker     (123)     3136 2023-07-20 19:29:58.000000 gigagan-pytorch-0.1.9/gigagan_pytorch/data.py
--rw-r--r--   0 runner    (1001) docker     (123)    71723 2023-07-20 19:29:58.000000 gigagan-pytorch-0.1.9/gigagan_pytorch/gigagan_pytorch.py
--rw-r--r--   0 runner    (1001) docker     (123)     4585 2023-07-20 19:29:58.000000 gigagan-pytorch-0.1.9/gigagan_pytorch/open_clip.py
--rw-r--r--   0 runner    (1001) docker     (123)      953 2023-07-20 19:29:58.000000 gigagan-pytorch-0.1.9/gigagan_pytorch/optimizer.py
--rw-r--r--   0 runner    (1001) docker     (123)    17727 2023-07-20 19:29:58.000000 gigagan-pytorch-0.1.9/gigagan_pytorch/unet_upsampler.py
--rw-r--r--   0 runner    (1001) docker     (123)       22 2023-07-20 19:29:58.000000 gigagan-pytorch-0.1.9/gigagan_pytorch/version.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-20 19:30:08.250156 gigagan-pytorch-0.1.9/gigagan_pytorch.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)      612 2023-07-20 19:30:08.000000 gigagan-pytorch-0.1.9/gigagan_pytorch.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      467 2023-07-20 19:30:08.000000 gigagan-pytorch-0.1.9/gigagan_pytorch.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-20 19:30:08.000000 gigagan-pytorch-0.1.9/gigagan_pytorch.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      118 2023-07-20 19:30:08.000000 gigagan-pytorch-0.1.9/gigagan_pytorch.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       16 2023-07-20 19:30:08.000000 gigagan-pytorch-0.1.9/gigagan_pytorch.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       87 2023-07-20 19:29:58.000000 gigagan-pytorch-0.1.9/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-20 19:30:08.250156 gigagan-pytorch-0.1.9/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1003 2023-07-20 19:29:58.000000 gigagan-pytorch-0.1.9/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:49:34.227234 gigagan-pytorch-0.2.0/
+-rw-r--r--   0 runner    (1001) docker     (123)     1066 2023-07-23 16:49:23.000000 gigagan-pytorch-0.2.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      612 2023-07-23 16:49:34.227234 gigagan-pytorch-0.2.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     9314 2023-07-23 16:49:23.000000 gigagan-pytorch-0.2.0/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:49:34.227234 gigagan-pytorch-0.2.0/gigagan_pytorch/
+-rw-r--r--   0 runner    (1001) docker     (123)      577 2023-07-23 16:49:23.000000 gigagan-pytorch-0.2.0/gigagan_pytorch/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2934 2023-07-23 16:49:23.000000 gigagan-pytorch-0.2.0/gigagan_pytorch/attend.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3136 2023-07-23 16:49:23.000000 gigagan-pytorch-0.2.0/gigagan_pytorch/data.py
+-rw-r--r--   0 runner    (1001) docker     (123)    81269 2023-07-23 16:49:23.000000 gigagan-pytorch-0.2.0/gigagan_pytorch/gigagan_pytorch.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4617 2023-07-23 16:49:23.000000 gigagan-pytorch-0.2.0/gigagan_pytorch/open_clip.py
+-rw-r--r--   0 runner    (1001) docker     (123)      953 2023-07-23 16:49:23.000000 gigagan-pytorch-0.2.0/gigagan_pytorch/optimizer.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17976 2023-07-23 16:49:23.000000 gigagan-pytorch-0.2.0/gigagan_pytorch/unet_upsampler.py
+-rw-r--r--   0 runner    (1001) docker     (123)       22 2023-07-23 16:49:23.000000 gigagan-pytorch-0.2.0/gigagan_pytorch/version.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:49:34.227234 gigagan-pytorch-0.2.0/gigagan_pytorch.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)      612 2023-07-23 16:49:34.000000 gigagan-pytorch-0.2.0/gigagan_pytorch.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      467 2023-07-23 16:49:34.000000 gigagan-pytorch-0.2.0/gigagan_pytorch.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 16:49:34.000000 gigagan-pytorch-0.2.0/gigagan_pytorch.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      125 2023-07-23 16:49:34.000000 gigagan-pytorch-0.2.0/gigagan_pytorch.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       16 2023-07-23 16:49:34.000000 gigagan-pytorch-0.2.0/gigagan_pytorch.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       87 2023-07-23 16:49:23.000000 gigagan-pytorch-0.2.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 16:49:34.227234 gigagan-pytorch-0.2.0/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1017 2023-07-23 16:49:23.000000 gigagan-pytorch-0.2.0/setup.py
```

### Comparing `gigagan-pytorch-0.1.9/LICENSE` & `gigagan-pytorch-0.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `gigagan-pytorch-0.1.9/PKG-INFO` & `gigagan-pytorch-0.2.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: gigagan-pytorch
-Version: 0.1.9
+Version: 0.2.0
 Summary: GigaGAN - Pytorch
 Home-page: https://github.com/lucidrains/ETSformer-pytorch
 Author: Phil Wang
 Author-email: lucidrains@gmail.com
 License: MIT
 Keywords: artificial intelligence,deep learning,generative adversarial networks
 Classifier: Development Status :: 4 - Beta
```

### Comparing `gigagan-pytorch-0.1.9/README.md` & `gigagan-pytorch-0.2.0/README.md`

 * *Files 8% similar despite different names*

```diff
@@ -2,29 +2,29 @@
 
 <img src="./gigagan-architecture.png" width="500px"></img>
 
 ## GigaGAN - Pytorch
 
 Implementation of <a href="https://arxiv.org/abs/2303.05511v2">GigaGAN</a> <a href="https://mingukkang.github.io/GigaGAN/">(project page)</a>, new SOTA GAN out of Adobe.
 
-I will also add a few findings from <a href="https://github.com/lucidrains/lightweight-gan">lightweight gan</a>, for faster convergence (skip layer excitation), better stability (reconstruction auxiliary loss in discriminator), and improved generator results (GLU activations).
+I will also add a few findings from <a href="https://github.com/lucidrains/lightweight-gan">lightweight gan</a>, for faster convergence (skip layer excitation) and better stability (reconstruction auxiliary loss in discriminator)
 
 It will also contain the code for the 1k - 4k upsamplers, which I find to be the highlight of this paper.
 
 Please join <a href="https://discord.gg/xBPBXfcFHd"><img alt="Join us on Discord" src="https://img.shields.io/discord/823813159592001537?color=5865F2&logo=discord&logoColor=white"></a> if you are interested in helping out with the replication with the <a href="https://laion.ai/">LAION</a> community
 
 ## Appreciation
 
 - <a href="https://stability.ai/">StabilityAI</a> and <a href="https://huggingface.co/">🤗 Huggingface</a> for the generous sponsorship, as well as my other sponsors, for affording me the independence to open source artificial intelligence.
 
 - <a href="https://huggingface.co/">🤗 Huggingface</a> for their accelerate library
 
 - All the maintainers at <a href="https://github.com/mlfoundations/open_clip">OpenClip</a>, for their SOTA open sourced contrastive learning text-image models
 
-- <a href="https://github.com/XavierXiao">Xavier</a> for reviewing the discriminator code and pointing out that the scale invariance was not correctly built!
+- <a href="https://github.com/XavierXiao">Xavier</a> for the very helpful code review, and for discussions on how the scale invariance in the discriminator should be built!
 
 - <a href="https://github.com/CerebralSeed">@CerebralSeed</a> for pull requesting the initial sampling code for both the generator and upsampler!
 
 ## Install
 
 ```bash
 $ pip install gigagan-pytorch
@@ -131,22 +131,26 @@
 
 gan(
     steps = 100,
     grad_accum_every = 8
 )
 ```
 
-## Losses (wip)
+## Losses
 
 * `G` - Generator
 * `MSG` - Multiscale Generator
 * `D` - Discriminator
 * `MSD` - Multiscale Discriminator
 * `GP` - Gradient Penalty
 * `SSL` - Auxiliary Reconstruction in Discriminator (from Lightweight GAN)
+* `VD` - Vision-aided Discriminator
+* `VG` - Vision-aided Generator
+* `CL` - Generator Constrastive Loss
+* `MAL` - Matching Aware Loss
 
 A healthy run would have `G`, `MSG`, `D`, `MSD` with values hovering between `0` to `10`, and usually staying pretty constant. If at any time after 1k training steps these values persist at triple digits, that would mean something is wrong. It is ok for generator and discriminator values to occasionally dip negative, but it should swing back up to the range above.
 
 `GP` and `SSL` should be pushed towards `0`. `GP` can occasionally spike; I like to imagine it as the networks undergoing some epiphany
 
 ## Multi-GPU Training
 
@@ -181,30 +185,36 @@
     - [x] do pixel shuffle upsamples for unet
 - [x] get a code review for the multi-scale inputs and outputs, as the paper was a bit vague
 - [x] add upsampling network architecture
 - [x] make unconditional work for both base generator and upsampler
 - [x] make text conditioned training work for both base and upsampler
 - [x] make recon more efficient by random sampling patches
 - [x] make sure generator and discriminator can also accept pre-encoded CLIP text encodings
+- [x] do a review of the auxiliary losses
+    - [x] add contrastive loss for generator
+    - [x] add vision aided loss
+    - [x] add gradient penalty for vision aided discr - make optional
+    - [x] add matching awareness loss - figure out if rotating text conditions by one is good enough for mismatching (without drawing an additional batch from dataloader)
+    - [x] make sure gradient accumulation works with matching aware loss
+    - [x] matching awareness loss runs and is stable
+    - [x] vision aided trains
 
 - [ ] add accelerate
     - [x] works single machine
     - [x] works for mixed precision (make sure gradient penalty is scaled correctly), take care of manual scaler saving and reloading, borrow from imagen-pytorch
     - [x] make sure it works multi-GPU for one machine
     - [ ] have someone else try multiple machines
 
+- [ ] clip should be optional for all modules, and managed by `GigaGAN`, with text -> text embeds processed once
 - [ ] add ability to select a random subset from multiscale dimension, for efficiency
 
 - [ ] add some differentiable augmentations, proven technique from the old GAN days
     - [ ] remove any magic being done with automatic rgbs processing, and have it explicitly passed in - offer functions on the discriminator that can process real images into the right multi-scales
     - [ ] add horizontal flip for starters
 
-- [ ] do a review of the auxiliary losses
-    - [ ] add vision aided loss and make sure it trains, inspect output
-
 - [ ] port over CLI from lightweight|stylegan2-pytorch
 - [ ] hook up laion dataset for text-image
 
 ## Citations
 
 ```bibtex
 @misc{https://doi.org/10.48550/arxiv.2303.05511,
```

#### html2text {}

```diff
@@ -1,98 +1,105 @@
 [./gigagan-sample.png] [./gigagan-architecture.png] ## GigaGAN - Pytorch
 Implementation of GigaGAN (project_page), new SOTA GAN out of Adobe. I will
 also add a few findings from lightweight_gan, for faster convergence (skip
-layer excitation), better stability (reconstruction auxiliary loss in
-discriminator), and improved generator results (GLU activations). It will also
-contain the code for the 1k - 4k upsamplers, which I find to be the highlight
-of this paper. Please join [Join_us_on_Discord] if you are interested in
-helping out with the replication with the LAION community ## Appreciation -
-StabilityAI and ð¤_Huggingface for the generous sponsorship, as well as my
-other sponsors, for affording me the independence to open source artificial
-intelligence. - ð¤_Huggingface for their accelerate library - All the
-maintainers at OpenClip, for their SOTA open sourced contrastive learning text-
-image models - Xavier for reviewing the discriminator code and pointing out
-that the scale invariance was not correctly built! - @CerebralSeed for pull
-requesting the initial sampling code for both the generator and upsampler! ##
-Install ```bash $ pip install gigagan-pytorch ``` ## Usage Simple unconditional
-GAN, for starters ```python import torch from gigagan_pytorch import ( GigaGAN,
-ImageDataset ) gan = GigaGAN( generator = dict( dim_capacity = 8, style_network
-= dict( dim = 64, depth = 4 ), image_size = 256, dim_max = 512,
-num_skip_layers_excite = 4, unconditional = True ), discriminator = dict
-( dim_capacity = 16, dim_max = 512, image_size = 256, num_skip_layers_excite =
-4, unconditional = True ), amp = True ).cuda() # dataset dataset = ImageDataset
-( folder = '/path/to/your/data', image_size = 256 ) dataloader =
-dataset.get_dataloader(batch_size = 1) # you must then set the dataloader for
-the GAN before training gan.set_dataloader(dataloader) # training the
-discriminator and generator alternating # for 100 steps in this example, batch
-size 1, gradient accumulated 8 times gan( steps = 100, grad_accum_every = 8 )
-``` For unconditional Unet Upsampler ```python import torch from
-gigagan_pytorch import ( GigaGAN, ImageDataset ) gan = GigaGAN( train_upsampler
-= True, # set this to True generator = dict( style_network = dict( dim = 64,
-depth = 4 ), dim = 32, image_size = 256, input_image_size = 128, unconditional
-= True ), discriminator = dict( dim_capacity = 16, dim_max = 512, image_size =
-256, num_skip_layers_excite = 4, unconditional = True ), amp = True ).cuda()
-dataset = ImageDataset( folder = '/path/to/your/data', image_size = 256 )
-dataloader = dataset.get_dataloader(batch_size = 1) gan.set_dataloader
-(dataloader) # training the discriminator and generator alternating # for 100
-steps in this example, batch size 1, gradient accumulated 8 times gan( steps =
-100, grad_accum_every = 8 ) ``` ## Losses (wip) * `G` - Generator * `MSG` -
-Multiscale Generator * `D` - Discriminator * `MSD` - Multiscale Discriminator *
-`GP` - Gradient Penalty * `SSL` - Auxiliary Reconstruction in Discriminator
-(from Lightweight GAN) A healthy run would have `G`, `MSG`, `D`, `MSD` with
-values hovering between `0` to `10`, and usually staying pretty constant. If at
-any time after 1k training steps these values persist at triple digits, that
-would mean something is wrong. It is ok for generator and discriminator values
-to occasionally dip negative, but it should swing back up to the range above.
-`GP` and `SSL` should be pushed towards `0`. `GP` can occasionally spike; I
-like to imagine it as the networks undergoing some epiphany ## Multi-GPU
-Training The `GigaGAN` class is now equipped with ð¤_Accelerator. You can
-easily do multi-gpu training in two steps using their `accelerate` CLI At the
-project root directory, where the training script is, run ```python $
-accelerate config ``` Then, in the same directory ```python $ accelerate launch
-train.py ``` ## Todo - [x] make sure it can be trained unconditionally - [x]
-read the relevant papers and knock out all 3 auxiliary losses - [x] matching
-aware loss - [x] clip loss - [x] vision-aided discriminator loss - [x] add
-reconstruction losses on arbitrary stages in the discriminator (lightweight
-gan) - [x] figure out how the random projections are used from projected-gan -
-[x] vision aided discriminator needs to extract N layers from the vision model
-in CLIP - [x] figure out whether to discard CLS token and reshape into image
-dimensions for convolution, or stick with attention and condition with adaptive
-layernorm - also turn off vision aided gan in unconditional case - [x] unet
-upsampler - [x] add adaptive conv - [x] modify latter stage of unet to also
-output rgb residuals, and pass the rgb into discriminator. make discriminator
-agnostic to rgb being passed in - [x] do pixel shuffle upsamples for unet - [x]
-get a code review for the multi-scale inputs and outputs, as the paper was a
-bit vague - [x] add upsampling network architecture - [x] make unconditional
-work for both base generator and upsampler - [x] make text conditioned training
-work for both base and upsampler - [x] make recon more efficient by random
-sampling patches - [x] make sure generator and discriminator can also accept
-pre-encoded CLIP text encodings - [ ] add accelerate - [x] works single machine
-- [x] works for mixed precision (make sure gradient penalty is scaled
-correctly), take care of manual scaler saving and reloading, borrow from
-imagen-pytorch - [x] make sure it works multi-GPU for one machine - [ ] have
-someone else try multiple machines - [ ] add ability to select a random subset
-from multiscale dimension, for efficiency - [ ] add some differentiable
-augmentations, proven technique from the old GAN days - [ ] remove any magic
-being done with automatic rgbs processing, and have it explicitly passed in -
-offer functions on the discriminator that can process real images into the
-right multi-scales - [ ] add horizontal flip for starters - [ ] do a review of
-the auxiliary losses - [ ] add vision aided loss and make sure it trains,
-inspect output - [ ] port over CLI from lightweight|stylegan2-pytorch - [ ]
-hook up laion dataset for text-image ## Citations ```bibtex @misc{https://
-doi.org/10.48550/arxiv.2303.05511, url = {https://arxiv.org/abs/2303.05511},
-author = {Kang, Minguk and Zhu, Jun-Yan and Zhang, Richard and Park, Jaesik and
-Shechtman, Eli and Paris, Sylvain and Park, Taesung}, title = {Scaling up GANs
-for Text-to-Image Synthesis}, publisher = {arXiv}, year = {2023}, copyright =
-{arXiv.org perpetual, non-exclusive license} } ``` ```bibtex @article
-{Liu2021TowardsFA, title = {Towards Faster and Stabilized GAN Training for
-High-fidelity Few-shot Image Synthesis}, author = {Bingchen Liu and Yizhe Zhu
-and Kunpeng Song and A. Elgammal}, journal = {ArXiv}, year = {2021}, volume =
-{abs/2101.04775} } ``` ```bibtex @inproceedings{dao2022flashattention, title =
-{Flash{A}ttention: Fast and Memory-Efficient Exact Attention with {IO}-
-Awareness}, author = {Dao, Tri and Fu, Daniel Y. and Ermon, Stefano and Rudra,
-Atri and R{\'e}, Christopher}, booktitle = {Advances in Neural Information
-Processing Systems}, year = {2022} } ``` ```bibtex @inproceedings
-{Heusel2017GANsTB, title = {GANs Trained by a Two Time-Scale Update Rule
-Converge to a Local Nash Equilibrium}, author = {Martin Heusel and Hubert
-Ramsauer and Thomas Unterthiner and Bernhard Nessler and Sepp Hochreiter},
-booktitle = {NIPS}, year = {2017} } ```
+layer excitation) and better stability (reconstruction auxiliary loss in
+discriminator) It will also contain the code for the 1k - 4k upsamplers, which
+I find to be the highlight of this paper. Please join [Join_us_on_Discord] if
+you are interested in helping out with the replication with the LAION community
+## Appreciation - StabilityAI and ð¤_Huggingface for the generous
+sponsorship, as well as my other sponsors, for affording me the independence to
+open source artificial intelligence. - ð¤_Huggingface for their accelerate
+library - All the maintainers at OpenClip, for their SOTA open sourced
+contrastive learning text-image models - Xavier for the very helpful code
+review, and for discussions on how the scale invariance in the discriminator
+should be built! - @CerebralSeed for pull requesting the initial sampling code
+for both the generator and upsampler! ## Install ```bash $ pip install gigagan-
+pytorch ``` ## Usage Simple unconditional GAN, for starters ```python import
+torch from gigagan_pytorch import ( GigaGAN, ImageDataset ) gan = GigaGAN
+( generator = dict( dim_capacity = 8, style_network = dict( dim = 64, depth = 4
+), image_size = 256, dim_max = 512, num_skip_layers_excite = 4, unconditional =
+True ), discriminator = dict( dim_capacity = 16, dim_max = 512, image_size =
+256, num_skip_layers_excite = 4, unconditional = True ), amp = True ).cuda() #
+dataset dataset = ImageDataset( folder = '/path/to/your/data', image_size = 256
+) dataloader = dataset.get_dataloader(batch_size = 1) # you must then set the
+dataloader for the GAN before training gan.set_dataloader(dataloader) #
+training the discriminator and generator alternating # for 100 steps in this
+example, batch size 1, gradient accumulated 8 times gan( steps = 100,
+grad_accum_every = 8 ) ``` For unconditional Unet Upsampler ```python import
+torch from gigagan_pytorch import ( GigaGAN, ImageDataset ) gan = GigaGAN
+( train_upsampler = True, # set this to True generator = dict( style_network =
+dict( dim = 64, depth = 4 ), dim = 32, image_size = 256, input_image_size =
+128, unconditional = True ), discriminator = dict( dim_capacity = 16, dim_max =
+512, image_size = 256, num_skip_layers_excite = 4, unconditional = True ), amp
+= True ).cuda() dataset = ImageDataset( folder = '/path/to/your/data',
+image_size = 256 ) dataloader = dataset.get_dataloader(batch_size = 1)
+gan.set_dataloader(dataloader) # training the discriminator and generator
+alternating # for 100 steps in this example, batch size 1, gradient accumulated
+8 times gan( steps = 100, grad_accum_every = 8 ) ``` ## Losses * `G` -
+Generator * `MSG` - Multiscale Generator * `D` - Discriminator * `MSD` -
+Multiscale Discriminator * `GP` - Gradient Penalty * `SSL` - Auxiliary
+Reconstruction in Discriminator (from Lightweight GAN) * `VD` - Vision-aided
+Discriminator * `VG` - Vision-aided Generator * `CL` - Generator Constrastive
+Loss * `MAL` - Matching Aware Loss A healthy run would have `G`, `MSG`, `D`,
+`MSD` with values hovering between `0` to `10`, and usually staying pretty
+constant. If at any time after 1k training steps these values persist at triple
+digits, that would mean something is wrong. It is ok for generator and
+discriminator values to occasionally dip negative, but it should swing back up
+to the range above. `GP` and `SSL` should be pushed towards `0`. `GP` can
+occasionally spike; I like to imagine it as the networks undergoing some
+epiphany ## Multi-GPU Training The `GigaGAN` class is now equipped with ð¤
+Accelerator. You can easily do multi-gpu training in two steps using their
+`accelerate` CLI At the project root directory, where the training script is,
+run ```python $ accelerate config ``` Then, in the same directory ```python $
+accelerate launch train.py ``` ## Todo - [x] make sure it can be trained
+unconditionally - [x] read the relevant papers and knock out all 3 auxiliary
+losses - [x] matching aware loss - [x] clip loss - [x] vision-aided
+discriminator loss - [x] add reconstruction losses on arbitrary stages in the
+discriminator (lightweight gan) - [x] figure out how the random projections are
+used from projected-gan - [x] vision aided discriminator needs to extract N
+layers from the vision model in CLIP - [x] figure out whether to discard CLS
+token and reshape into image dimensions for convolution, or stick with
+attention and condition with adaptive layernorm - also turn off vision aided
+gan in unconditional case - [x] unet upsampler - [x] add adaptive conv - [x]
+modify latter stage of unet to also output rgb residuals, and pass the rgb into
+discriminator. make discriminator agnostic to rgb being passed in - [x] do
+pixel shuffle upsamples for unet - [x] get a code review for the multi-scale
+inputs and outputs, as the paper was a bit vague - [x] add upsampling network
+architecture - [x] make unconditional work for both base generator and
+upsampler - [x] make text conditioned training work for both base and upsampler
+- [x] make recon more efficient by random sampling patches - [x] make sure
+generator and discriminator can also accept pre-encoded CLIP text encodings -
+[x] do a review of the auxiliary losses - [x] add contrastive loss for
+generator - [x] add vision aided loss - [x] add gradient penalty for vision
+aided discr - make optional - [x] add matching awareness loss - figure out if
+rotating text conditions by one is good enough for mismatching (without drawing
+an additional batch from dataloader) - [x] make sure gradient accumulation
+works with matching aware loss - [x] matching awareness loss runs and is stable
+- [x] vision aided trains - [ ] add accelerate - [x] works single machine - [x]
+works for mixed precision (make sure gradient penalty is scaled correctly),
+take care of manual scaler saving and reloading, borrow from imagen-pytorch -
+[x] make sure it works multi-GPU for one machine - [ ] have someone else try
+multiple machines - [ ] clip should be optional for all modules, and managed by
+`GigaGAN`, with text -> text embeds processed once - [ ] add ability to select
+a random subset from multiscale dimension, for efficiency - [ ] add some
+differentiable augmentations, proven technique from the old GAN days - [ ]
+remove any magic being done with automatic rgbs processing, and have it
+explicitly passed in - offer functions on the discriminator that can process
+real images into the right multi-scales - [ ] add horizontal flip for starters
+- [ ] port over CLI from lightweight|stylegan2-pytorch - [ ] hook up laion
+dataset for text-image ## Citations ```bibtex @misc{https://doi.org/10.48550/
+arxiv.2303.05511, url = {https://arxiv.org/abs/2303.05511}, author = {Kang,
+Minguk and Zhu, Jun-Yan and Zhang, Richard and Park, Jaesik and Shechtman, Eli
+and Paris, Sylvain and Park, Taesung}, title = {Scaling up GANs for Text-to-
+Image Synthesis}, publisher = {arXiv}, year = {2023}, copyright = {arXiv.org
+perpetual, non-exclusive license} } ``` ```bibtex @article{Liu2021TowardsFA,
+title = {Towards Faster and Stabilized GAN Training for High-fidelity Few-shot
+Image Synthesis}, author = {Bingchen Liu and Yizhe Zhu and Kunpeng Song and A.
+Elgammal}, journal = {ArXiv}, year = {2021}, volume = {abs/2101.04775} } ```
+```bibtex @inproceedings{dao2022flashattention, title = {Flash{A}ttention: Fast
+and Memory-Efficient Exact Attention with {IO}-Awareness}, author = {Dao, Tri
+and Fu, Daniel Y. and Ermon, Stefano and Rudra, Atri and R{\'e}, Christopher},
+booktitle = {Advances in Neural Information Processing Systems}, year = {2022}
+} ``` ```bibtex @inproceedings{Heusel2017GANsTB, title = {GANs Trained by a Two
+Time-Scale Update Rule Converge to a Local Nash Equilibrium}, author = {Martin
+Heusel and Hubert Ramsauer and Thomas Unterthiner and Bernhard Nessler and Sepp
+Hochreiter}, booktitle = {NIPS}, year = {2017} } ```
```

### Comparing `gigagan-pytorch-0.1.9/gigagan_pytorch/attend.py` & `gigagan-pytorch-0.2.0/gigagan_pytorch/attend.py`

 * *Files identical despite different names*

### Comparing `gigagan-pytorch-0.1.9/gigagan_pytorch/data.py` & `gigagan-pytorch-0.2.0/gigagan_pytorch/data.py`

 * *Files identical despite different names*

### Comparing `gigagan-pytorch-0.1.9/gigagan_pytorch/gigagan_pytorch.py` & `gigagan-pytorch-0.2.0/gigagan_pytorch/gigagan_pytorch.py`

 * *Files 14% similar despite different names*

```diff
@@ -14,14 +14,16 @@
 
 from beartype import beartype
 from beartype.typing import List, Optional, Tuple, Dict, Union, Iterable
 
 from einops import rearrange, pack, unpack, repeat, reduce
 from einops.layers.torch import Rearrange, Reduce
 
+from kornia.filters import filter2d
+
 from ema_pytorch import EMA
 
 from gigagan_pytorch.version import __version__
 from gigagan_pytorch.open_clip import OpenClipAdapter
 from gigagan_pytorch.optimizer import get_optimizer
 
 from tqdm import tqdm
@@ -56,14 +58,26 @@
     if len(arr) == 0:
         return None
     return arr.pop(0)
 
 def divisible_by(numer, denom):
     return (numer % denom) == 0
 
+def group_by_num_consecutive(arr, num):
+    out = []
+    for ind, el in enumerate(arr):
+        if ind > 0 and divisible_by(ind, num):
+            yield out
+            out = []
+
+        out.append(el)
+
+    if len(out) > 0:
+        yield out
+
 def is_unique(arr):
     return len(set(arr)) == len(arr)
 
 def cycle(dl):
     while True:
         for data in dl:
             yield data
@@ -141,27 +155,30 @@
 
 def discriminator_hinge_loss(real, fake):
     return (F.relu(1 + real) + F.relu(1 - fake)).mean()
 
 # auxiliary losses
 
 def aux_matching_loss(real, fake):
-    return log(1 + real.exp()) + log(1 + fake.exp())
+    """
+    making logits negative, as in this framework, discriminator is 0 for real, high value for fake. GANs can have this arbitrarily swapped, as it only matters if the generator and discriminator are opposites
+    """
+    return (log(1 + (-real).exp()) + log(1 + (-fake).exp())).mean()
 
 @beartype
 def aux_clip_loss(
     clip: OpenClipAdapter,
     images: Tensor,
     texts: Optional[List[str]] = None,
     text_embeds: Optional[Tensor] = None
 ):
     assert exists(texts) ^ exists(text_embeds)
 
     if exists(texts):
-        text_embeds = clip.embed_texts(texts)
+        text_embeds, _ = clip.embed_texts(texts)
 
     return clip.contrastive_loss(images = images, text_embeds = text_embeds)
 
 # rmsnorm (newer papers show mean-centering in layernorm not necessary)
 
 class ChannelRMSNorm(nn.Module):
     def __init__(self, dim):
@@ -181,15 +198,32 @@
 
     def forward(self, x):
         normed = F.normalize(x, dim = -1)
         return normed * self.scale * self.gamma
 
 # down and upsample
 
-class Upsample(nn.Module):
+class Blur(nn.Module):
+    def __init__(self):
+        super().__init__()
+        f = torch.Tensor([1, 2, 1])
+        self.register_buffer('f', f)
+
+    def forward(self, x):
+        f = self.f
+        f = f[None, None, :] * f [None, :, None]
+        return filter2d(x, f, normalized = True)
+
+def Upsample(*args):
+    return nn.Sequential(
+        nn.Upsample(scale_factor = 2, mode = 'bilinear', align_corners = False),
+        Blur()
+    )
+
+class PixelShuffleUpsample(nn.Module):
     def __init__(self, dim):
         super().__init__()
         conv = nn.Conv2d(dim, dim * 4, 1)
 
         self.net = nn.Sequential(
             conv,
             nn.SiLU(),
@@ -766,35 +800,35 @@
     pass
 
 class Generator(BaseGenerator):
     @beartype
     def __init__(
         self,
         *,
-        dim_capacity = 16,
         image_size,
+        dim_capacity = 16,
         dim_max = 2048,
         channels = 3,
         style_network: Optional[Union[StyleNetwork, Dict]] = None,
         style_network_dim = None,
         text_encoder: Optional[Union[TextEncoder, Dict]] = None,
         dim_latent = 512,
         self_attn_resolutions: Tuple[int, ...] = (32, 16),
         self_attn_dim_head = 64,
         self_attn_heads = 8,
         self_attn_dot_product = True,
-        self_ff_mult = 4,
+        self_attn_ff_mult = 4,
         cross_attn_resolutions: Tuple[int, ...] = (32, 16),
         cross_attn_dim_head = 64,
         cross_attn_heads = 8,
-        cross_ff_mult = 4,
+        cross_attn_ff_mult = 4,
         num_conv_kernels = 2,  # the number of adaptive conv kernels
         num_skip_layers_excite = 0,
         unconditional = False,
-        use_glu = True
+        pixel_shuffle_upsample = False
     ):
         super().__init__()
         self.channels = channels
 
         if isinstance(style_network, dict):
             style_network = StyleNetwork(**style_network)
 
@@ -878,38 +912,49 @@
             has_cross_attn = resolution in cross_attn_resolutions and not unconditional
 
             skip_squeeze_excite = None
             if should_skip_layer_excite:
                 dim_skip_in, _ = dim_pairs[ind + num_skip_layers_excite]
                 skip_squeeze_excite = SqueezeExcite(dim_in, dim_skip_in)
 
-            dim_inner = dim_out * (2 if use_glu else 1)
-            activation = partial(nn.GLU, dim = 1) if use_glu else leaky_relu
-
             resnet_block = nn.ModuleList([
-                adaptive_conv(dim_in, dim_inner),
-                Noise(dim_inner),
-                activation(),
-                adaptive_conv(dim_out, dim_inner),
-                Noise(dim_inner),
-                activation()
+                adaptive_conv(dim_in, dim_out),
+                Noise(dim_out),
+                leaky_relu(),
+                adaptive_conv(dim_out, dim_out),
+                Noise(dim_out),
+                leaky_relu()
             ])
 
             to_rgb = adaptive_conv(dim_out, channels)
 
             self_attn = cross_attn = rgb_upsample = upsample = None
 
-            upsample = Upsample(dim_in) if should_upsample else None
-            rgb_upsample = Upsample(channels) if should_upsample_rgb else None
+            upsample_klass = Upsample if not pixel_shuffle_upsample else PixelShuffleUpsample
+
+            upsample = upsample_klass(dim_in) if should_upsample else None
+            rgb_upsample = upsample_klass(channels) if should_upsample_rgb else None
 
             if has_self_attn:
-                self_attn = SelfAttentionBlock(dim_out, dot_product = self_attn_dot_product)
+                self_attn = SelfAttentionBlock(
+                    dim_out,
+                    dim_head = self_attn_dim_head,
+                    heads = self_attn_heads,
+                    ff_mult = self_attn_ff_mult,
+                    dot_product = self_attn_dot_product
+            )
 
             if has_cross_attn:
-                cross_attn = CrossAttentionBlock(dim_out, dim_context = text_encoder.dim)
+                cross_attn = CrossAttentionBlock(
+                    dim_out,
+                    dim_context = text_encoder.dim,
+                    dim_head = cross_attn_dim_head,
+                    heads = cross_attn_heads,
+                    ff_mult = cross_attn_ff_mult,
+                )
 
             style_embed_split_dims.extend([
                 dim_in,             # for first conv in resnet block
                 dim_kernel_mod,     # first conv kernel selection
                 dim_out,            # second conv in resnet block
                 dim_kernel_mod,     # second conv kernel selection
                 dim_out,            # to RGB conv
@@ -936,15 +981,15 @@
 
     def init_(self, m):
         if type(m) in {nn.Conv2d, nn.Linear}:
             nn.init.kaiming_normal_(m.weight, a = 0, mode = 'fan_in', nonlinearity = 'leaky_relu')
 
     @property
     def total_params(self):
-        return sum([p.numel() for p in self.parameters()])
+        return sum([p.numel() for p in self.parameters() if p.requires_grad])
 
     @property
     def device(self):
         return next(self.parameters()).device
 
     @beartype
     def forward(
@@ -1144,28 +1189,34 @@
         if not self.channel_first:
             return x @ self.fixed_weights
 
         return einsum('b c ..., c d -> b d ...', x, self.fixed_weights)
 
 class VisionAidedDiscriminator(nn.Module):
     """ the vision-aided gan loss """
+
+    @beartype
     def __init__(
         self,
         *,
-        clip: OpenClipAdapter,
         depth = 2,
         dim_head = 64,
         heads = 8,
+        clip: Optional[OpenClipAdapter] = None,
         layer_indices = (-1, -2, -3),
         conv_dim = None,
         text_dim = None,
         unconditional = False,
         num_conv_kernels = 2
     ):
         super().__init__()
+
+        if not exists(clip):
+            clip = OpenClipAdapter()
+
         self.clip = clip
         dim = clip._dim_image_latent
 
         self.unconditional = unconditional
         text_dim = default(text_dim, dim)
         conv_dim = default(conv_dim, dim)
 
@@ -1183,39 +1234,50 @@
                 nn.Sequential(
                     conv2d_3x3(conv_dim, 1),
                     Rearrange('b 1 ... -> b ...')
                 )
             ]))
 
     def parameters(self):
-        return [
-            *self.network.parameters(),
-            *self.to_pred.parameters()
-        ]
+        return self.layer_discriminators.parameters()
 
+    @property
+    def total_params(self):
+        return sum([p.numel() for p in self.parameters()])
+
+    @beartype
     def forward(
         self,
         images,
-        text_embeds = None
+        texts: Optional[List[str]] = None,
+        text_embeds: Optional[Tensor] = None,
+        return_clip_encodings = False
     ):
+
+        assert self.unconditional or (exists(text_embeds) ^ exists(texts))
+
         with torch.no_grad():
-            self.clip.eval()
-            _, image_encodings = self.clip.embed_images(images)
-            image_encodings = image_encodings.detach()
+            if not self.unconditional and exists(texts):
+                self.clip.eval()
+                text_embeds = self.clip.embed_texts
+
+        _, image_encodings = self.clip.embed_images(images)
 
         logits = []
+
         for layer_index, (rand_proj, conv, to_conv_mod, to_conv_kernel_mod, to_logits) in zip(self.layer_indices, self.layer_discriminators):
             image_encoding = image_encodings[layer_index]
 
             cls_token, rest_tokens = image_encoding[:, :1], image_encoding[:, 1:]
             height_width = int(sqrt(rest_tokens.shape[-2])) # assume square
 
             img_fmap = rearrange(rest_tokens, 'b (h w) d -> b d h w', h = height_width)
 
             img_fmap = img_fmap + rearrange(cls_token, 'b 1 d -> b d 1 1 ') # pool the cls token into the rest of the tokens
+
             img_fmap = rand_proj(img_fmap)
 
             if self.unconditional:
                 img_fmap = conv(img_fmap)
             else:
                 assert exists(text_embeds)
 
@@ -1225,15 +1287,18 @@
                     kernel_mod = to_conv_kernel_mod(text_embeds)
                 )
 
             layer_logits = to_logits(img_fmap)
 
             logits.append(layer_logits)
 
-        return logits
+        if not return_clip_encodings:
+            return logits
+
+        return logits, image_encodings
 
 class Predictor(nn.Module):
     def __init__(
         self,
         dim,
         depth = 4,
         num_conv_kernels = 2,
@@ -1626,36 +1691,43 @@
         return logits, multiscale_outputs, aux_recon_losses
 
 # gan
 
 TrainDiscrLosses = namedtuple('TrainDiscrLosses', [
     'divergence',
     'multiscale_divergence',
+    'vision_aided_divergence',
+    'total_matching_aware_loss',
     'gradient_penalty',
     'aux_reconstruction'
 ])
 
 TrainGenLosses = namedtuple('TrainGenLosses', [
     'divergence',
-    'multiscale_divergence'
+    'multiscale_divergence',
+    'total_vd_divergence',
+    'contrastive_loss'
 ])
 
 class GigaGAN(nn.Module):
     @beartype
     def __init__(
         self,
         *,
         generator: Union[BaseGenerator, Dict],
         discriminator: Union[Discriminator, Dict],
-        text_encoder: Optional[Union[TextEncoder, Dict]] = None,
+        vision_aided_discriminator: Optional[Union[VisionAidedDiscriminator, Dict]] = None,
         learning_rate = 2e-4,
         betas = (0.5, 0.9),
         weight_decay = 0.,
         discr_aux_recon_loss_weight = 1.,
         multiscale_divergence_loss_weight = 0.1,
+        vision_aided_divergence_loss_weight = 0.5,
+        generator_contrastive_loss_weight = 0.1,
+        matching_awareness_loss_weight = 0.1,
         calc_multiscale_loss_every = 1,
         apply_gradient_penalty_every = 4,
         ttur_mult = 1,
         train_upsampler = False,
         upsampler_replace_rgb_with_input_lowres_image = False,
         log_steps_every = 20,
         create_ema_generator_at_init = True,
@@ -1707,58 +1779,73 @@
 
         if isinstance(generator, dict):
             generator = generator_klass(**generator)
 
         if isinstance(discriminator, dict):
             discriminator = Discriminator(**discriminator)
 
+        if exists(vision_aided_discriminator) and isinstance(vision_aided_discriminator, dict):
+            vision_aided_discriminator = VisionAidedDiscriminator(**vision_aided_discriminator)
+
         assert isinstance(generator, generator_klass)
 
         # use _base to designate unwrapped models
 
         self.G = generator
         self.D = discriminator
+        self.VD = vision_aided_discriminator
 
         # ema
 
         self.has_ema_generator = False
 
         if self.is_main and create_ema_generator_at_init:
             self.create_ema_generator()
 
         # print number of parameters
 
-        self.print(f'Generator parameters: {numerize.numerize(generator.total_params)}')
-        self.print(f'Discriminator parameters: {numerize.numerize(discriminator.total_params)}')
+        self.print('\n')
 
-        # text encoder
+        self.print(f'Generator: {numerize.numerize(generator.total_params)}')
+        self.print(f'Discriminator: {numerize.numerize(discriminator.total_params)}')
 
-        if exists(text_encoder):
-            if isinstance(text_encoder, dict):
-                text_encoder = TextEncoder(**text_encoder)
+        if exists(self.VD):
+            self.print(f'Vision Discriminator: {numerize.numerize(vision_aided_discriminator.total_params)}')
 
-        self.text_encoder = text_encoder
+        self.print('\n')
+
+        # text encoder
 
         assert generator.unconditional == discriminator.unconditional
+        assert not exists(vision_aided_discriminator) or vision_aided_discriminator.unconditional == generator.unconditional
 
         self.unconditional = generator.unconditional
 
         # optimizers
 
         self.G_opt = get_optimizer(self.G.parameters(), lr = learning_rate, betas = betas, weight_decay = weight_decay)
         self.D_opt = get_optimizer(self.D.parameters(), lr = learning_rate * ttur_mult, betas = betas, weight_decay = weight_decay)
 
         # prepare for distributed
 
         self.G, self.D, self.G_opt, self.D_opt = self.accelerator.prepare(self.G, self.D, self.G_opt, self.D_opt)
 
+        # vision aided discriminator optimizer
+
+        if exists(self.VD):
+            self.VD_opt = get_optimizer(self.VD.parameters(), lr = learning_rate, betas = betas, weight_decay = weight_decay)
+            self.VD_opt = self.accelerator.prepare(self.VD_opt)
+
         # loss related
 
         self.discr_aux_recon_loss_weight = discr_aux_recon_loss_weight
         self.multiscale_divergence_loss_weight = multiscale_divergence_loss_weight
+        self.vision_aided_divergence_loss_weight = vision_aided_divergence_loss_weight
+        self.generator_contrastive_loss_weight = generator_contrastive_loss_weight
+        self.matching_awareness_loss_weight = matching_awareness_loss_weight
 
         # steps
 
         self.log_steps_every = log_steps_every
 
         self.register_buffer('steps', torch.ones(1, dtype = torch.long))
 
@@ -1799,14 +1886,21 @@
 
         if exists(self.G_opt.scaler):
             pkg['G_scaler'] = self.G_opt.scaler.state_dict()
 
         if exists(self.D_opt.scaler):
             pkg['D_scaler'] = self.D_opt.scaler.state_dict()
 
+        if exists(self.VD):
+            pkg['VD'] = self.unwrapped_VD.state_dict()
+            pkg['VD_opt'] = self.VD_opt.state_dict()
+
+            if exists(self.VD_opt.scaler):
+                pkg['VD_scaler'] = self.VD_opt.scaler.state_dict()
+
         if self.has_ema_generator:
             pkg['G_ema'] = self.G_ema.state_dict()
 
         torch.save(pkg, str(path))
 
     def load(self, path, strict = False):
         path = Path(path)
@@ -1816,33 +1910,42 @@
 
         if 'version' in pkg and pkg['version'] != __version__:
             print(f"trying to load from version {pkg['version']}")
 
         self.unwrapped_G.load_state_dict(pkg['G'], strict = strict)
         self.unwrapped_D.load_state_dict(pkg['D'], strict = strict)
 
+        if exists(self.VD):
+            self.unwrapped_VD.load_state_dict(pkg['VD'], strict = strict)
+
         if self.has_ema_generator:
             self.G_ema.load_state_dict(pkg['G_ema'])
 
         if 'steps' in pkg:
             self.steps.copy_(torch.tensor([pkg['steps']]))
 
         if 'G_opt'not in pkg or 'D_opt' not in pkg:
             return
 
         try:
             self.G_opt.load_state_dict(pkg['G_opt'])
             self.D_opt.load_state_dict(pkg['D_opt'])
 
+            if exists(self.VD):
+                self.VD_opt.load_state_dict(pkg['VD_opt'])
+
             if 'G_scaler' in pkg and exists(self.G_opt.scaler):
                 self.G_opt.scaler.load_state_dict(pkg['G_scaler'])
 
             if 'D_scaler' in pkg and exists(self.D_opt.scaler):
                 self.D_opt.scaler.load_state_dict(pkg['D_scaler'])
 
+            if 'VD_scaler' in pkg and exists(self.VD_opt.scaler):
+                self.VD_opt.scaler.load_state_dict(pkg['VD_scaler'])
+
         except Exception as e:
             self.print(f'unable to load optimizers {e.msg}- optimizer states will be reset')
             pass
 
     # accelerate related
 
     @property
@@ -1853,14 +1956,26 @@
     def unwrapped_G(self):
         return self.accelerator.unwrap_model(self.G)
 
     @property
     def unwrapped_D(self):
         return self.accelerator.unwrap_model(self.D)
 
+    @property
+    def unwrapped_VD(self):
+        return self.accelerator.unwrap_model(self.VD)
+
+    @property
+    def need_vision_aided_discriminator(self):
+        return exists(self.VD) and self.vision_aided_divergence_loss_weight > 0.
+
+    @property
+    def need_contrastive_loss(self):
+        return self.generator_contrastive_loss_weight > 0. and not self.unconditional
+
     def print(self, msg):
         self.accelerator.print(msg)
 
     @property
     def is_distributed(self):
         return not (self.accelerator.distributed_type == DistributedType.NO and self.accelerator.num_processes == 1)
 
@@ -1908,15 +2023,15 @@
             if self.unconditional:
                 real_images = next(dl_iter)
             else:
                 result = next(dl_iter)
                 assert isinstance(result, tuple), 'dataset should return a tuple of two items for text conditioned training, (images: Tensor, texts: List[str])'
                 real_images, texts = result
 
-                maybe_text_kwargs['texts'] = texts
+                maybe_text_kwargs['texts'] = texts[:batch_size]
 
             real_images = real_images.to(self.device)
 
         # if training upsample generator, need to downsample real images
 
         if self.train_upsampler:
             size = self.G.input_image_size
@@ -1944,33 +2059,47 @@
         self,
         dl_iter: Iterable,
         grad_accum_every = 1,
         apply_gradient_penalty = False,
         calc_multiscale_loss = True
     ):
         total_divergence = 0.
+        total_vision_aided_divergence = 0.
+
         total_gp_loss = 0.
         total_aux_loss = 0.
 
         total_multiscale_divergence = 0. if calc_multiscale_loss else None
 
+        has_matching_awareness = not self.unconditional and self.matching_awareness_loss_weight > 0.
+
+        total_matching_aware_loss = 0.
+
+        all_texts = []
+        all_fake_images = []
+        all_fake_rgbs = []
+        all_real_images = []
+
         self.G.train()
         self.D.train()
 
         self.D_opt.zero_grad()
 
         for _ in range(grad_accum_every):
 
             if self.unconditional:
                 real_images = next(dl_iter)
             else:
                 result = next(dl_iter)
                 assert isinstance(result, tuple), 'dataset should return a tuple of two items for text conditioned training, (images: Tensor, texts: List[str])'
                 real_images, texts = result
 
+                all_real_images.append(real_images)
+                all_texts.extend(texts)
+
             # requires grad for real images, for gradient penalty
 
             real_images = real_images.to(self.device)
             real_images.requires_grad_()
 
             batch_size = real_images.shape[0]
 
@@ -1983,14 +2112,17 @@
             with torch.no_grad(), self.accelerator.autocast():
                 images, rgbs = self.G(
                     **G_kwargs,
                     **maybe_text_kwargs,
                     return_all_rgbs = True
                 )
 
+                all_fake_images.append(images)
+                all_fake_rgbs.append(rgbs)
+
                 # detach output of generator, as training discriminator only
 
                 images.detach_()
 
                 for rgb in rgbs:
                     rgb.detach_()
 
@@ -2037,76 +2169,172 @@
                         outputs = [real_logits, *real_multiscale_logits],
                         grad_output_weights = [1., *(self.multiscale_divergence_loss_weight,) * len(real_multiscale_logits)],
                         scaler = self.D_opt.scaler
                     )
 
                     total_gp_loss += (gp_loss.item() / grad_accum_every)
 
+                # handle vision aided discriminator, if needed
+
+                vd_loss = 0.
+
+                if self.need_vision_aided_discriminator:
+
+                    fake_vision_aided_logits = self.VD(images, **maybe_text_kwargs)
+                    real_vision_aided_logits, clip_encodings = self.VD(real_images, return_clip_encodings = True, **maybe_text_kwargs)
+
+                    for fake_logits, real_logits in zip(fake_vision_aided_logits, real_vision_aided_logits):
+                        vd_loss = vd_loss + discriminator_hinge_loss(real_logits, fake_logits)
+
+                    total_vision_aided_divergence += (vd_loss.item() / grad_accum_every)
+
+                    # handle gradient penalty for vision aided discriminator
+
+                    if apply_gradient_penalty:
+
+                        vd_gp_loss = gradient_penalty(
+                            clip_encodings,
+                            outputs = real_vision_aided_logits,
+                            grad_output_weights = [self.vision_aided_divergence_loss_weight] * len(real_vision_aided_logits),
+                            scaler = self.VD_opt.scaler
+                        )
+
+                        gp_loss = gp_loss + vd_gp_loss
+
+                        total_gp_loss += (vd_gp_loss.item() / grad_accum_every)
+
                 # sum up losses
 
                 total_loss = divergence + gp_loss
 
                 if self.multiscale_divergence_loss_weight > 0.:
                     total_loss = total_loss + multiscale_divergence * self.multiscale_divergence_loss_weight
 
+                if self.vision_aided_divergence_loss_weight > 0.:
+                    total_loss = total_loss + vd_loss * self.vision_aided_divergence_loss_weight
+
                 if self.discr_aux_recon_loss_weight > 0.:
                     aux_loss = sum(aux_recon_losses)
 
                     total_aux_loss += (aux_loss.item() / grad_accum_every)
 
                     total_loss = total_loss + aux_loss * self.discr_aux_recon_loss_weight
 
             # backwards
 
             self.accelerator.backward(total_loss / grad_accum_every)
 
+
+        # matching awareness loss
+        # strategy would be to rotate the texts by one and assume batch is shuffled enough for mismatched conditions
+
+        if has_matching_awareness:
+
+            # rotate texts
+
+            all_texts = [*all_texts[1:], all_texts[0]]
+            all_texts = group_by_num_consecutive(texts, batch_size)
+
+            zipped_data = zip(
+                all_fake_images,
+                all_fake_rgbs,
+                all_real_images,
+                all_texts
+            )
+
+            total_loss = 0.
+
+            for fake_images, fake_rgbs, real_images, texts in zipped_data:
+
+                with self.accelerator.autocast():
+                    fake_logits, *_ = self.D(
+                        fake_images,
+                        fake_rgbs,
+                        texts = texts,
+                        return_multiscale_outputs = False,
+                        calc_aux_loss = False
+                    )
+
+                    real_logits, *_ = self.D(
+                        real_images,
+                        texts = texts,
+                        return_multiscale_outputs = False,
+                        calc_aux_loss = False
+                    )
+
+                    matching_loss = aux_matching_loss(real_logits, fake_logits)
+
+                    total_matching_aware_loss = (matching_loss.item() / grad_accum_every)
+
+                    loss = matching_loss * self.matching_awareness_loss_weight
+
+                self.accelerator.backward(loss / grad_accum_every)
+
         self.D_opt.step()
 
-        return TrainDiscrLosses(total_divergence, total_multiscale_divergence, total_gp_loss, total_aux_loss)
+        return TrainDiscrLosses(
+            total_divergence,
+            total_multiscale_divergence,
+            total_vision_aided_divergence,
+            total_matching_aware_loss,
+            total_gp_loss,
+            total_aux_loss
+        )
 
     def train_generator_step(
         self,
         batch_size = None,
         dl_iter: Optional[Iterable] = None,
         grad_accum_every = 1,
         calc_multiscale_loss = True
     ):
         total_divergence = 0.
         total_multiscale_divergence = 0. if calc_multiscale_loss else None
+        total_vd_divergence = 0.
+        contrastive_loss = 0.
 
         self.G.train()
         self.D.train()
 
         self.D_opt.zero_grad()
         self.G_opt.zero_grad()
 
+        all_images = []
+        all_texts = []
+
         for _ in range(grad_accum_every):
 
             # generator
             
             G_kwargs, maybe_text_kwargs = self.generate_kwargs(dl_iter, batch_size)
 
             with self.accelerator.autocast():
                 image, rgbs = self.G(
                     **G_kwargs,
                     **maybe_text_kwargs,
                     return_all_rgbs = True
                 )
 
+                # accumulate all images and texts for maybe contrastive loss
+
+                if self.need_contrastive_loss:
+                    all_images.append(image)
+                    all_texts.extend(maybe_text_kwargs['texts'])
+
                 # discriminator
 
                 logits, multiscale_logits, _ = self.D(
                     image,
                     rgbs,
                     **maybe_text_kwargs,
                     return_multiscale_outputs = calc_multiscale_loss,
                     calc_aux_loss = False
                 )
 
-                # hinge loss
+                # generator hinge loss discriminator and multiscale
 
                 divergence = generator_hinge_loss(logits)
 
                 total_divergence += (divergence.item() / grad_accum_every)
 
                 total_loss = divergence
 
@@ -2116,26 +2344,61 @@
                     for multiscale_logit in multiscale_logits:
                         multiscale_divergence = multiscale_divergence + generator_hinge_loss(multiscale_logit)
 
                     total_multiscale_divergence += (multiscale_divergence.item() / grad_accum_every)
 
                     total_loss = total_loss + multiscale_divergence * self.multiscale_divergence_loss_weight
 
-            self.accelerator.backward(total_loss / grad_accum_every)
+                # vision aided generator hinge loss
+
+                if self.need_vision_aided_discriminator:
+                    vd_loss = 0.
+
+                    logits = self.VD(image, **maybe_text_kwargs)
+
+                    for logit in logits:
+                        vd_loss = vd_loss + generator_hinge_loss(logit)
+
+                    total_vd_divergence += (vd_loss.item() / grad_accum_every)
+
+                    total_loss = total_loss + vd_loss * self.vision_aided_divergence_loss_weight
+
+            self.accelerator.backward(total_loss / grad_accum_every, retain_graph = self.need_contrastive_loss)
+
+        # if needs the generator contrastive loss
+        # gather up all images and texts and calculate it
+
+        if self.need_contrastive_loss:
+            all_images = torch.cat(all_images, dim = 0)
+
+            contrastive_loss = aux_clip_loss(
+                clip = self.G.text_encoder.clip,
+                texts = all_texts,
+                images = all_images
+            )
+
+            self.accelerator.backward(contrastive_loss * self.generator_contrastive_loss_weight)
+
+        # generator optimizer step
 
         self.G_opt.step()
 
         # update exponentially moving averaged generator
 
         self.accelerator.wait_for_everyone()
 
         if self.is_main and self.has_ema_generator:
             self.G_ema.update()
 
-        return TrainGenLosses(total_divergence, total_multiscale_divergence)
+        return TrainGenLosses(
+            total_divergence,
+            total_multiscale_divergence,
+            total_vd_divergence,
+            contrastive_loss
+        )
 
     def sample(self, dl_iter, batch_size):
         G_kwargs, maybe_text_kwargs = self.generate_kwargs(dl_iter, batch_size)
 
         with self.accelerator.autocast():
             generator_output = self.G(**G_kwargs, **maybe_text_kwargs)
 
@@ -2204,24 +2467,36 @@
         for _ in tqdm(range(steps), initial = self.steps.item()):
             steps = self.steps.item()
             is_first_step = steps == 1
 
             apply_gradient_penalty = self.apply_gradient_penalty_every > 0 and divisible_by(steps, self.apply_gradient_penalty_every)
             calc_multiscale_loss =  self.calc_multiscale_loss_every > 0 and divisible_by(steps, self.calc_multiscale_loss_every)
 
-            d_loss, multiscale_d_loss, gp_loss, recon_loss = self.train_discriminator_step(
+            (
+                d_loss,
+                multiscale_d_loss,
+                vision_aided_d_loss,
+                matching_aware_loss,
+                gp_loss,
+                recon_loss
+            ) = self.train_discriminator_step(
                 dl_iter = dl_iter,
                 grad_accum_every = grad_accum_every,
                 apply_gradient_penalty = apply_gradient_penalty,
                 calc_multiscale_loss = calc_multiscale_loss
             )
 
             self.accelerator.wait_for_everyone()
 
-            g_loss, multiscale_g_loss = self.train_generator_step(
+            (
+                g_loss,
+                multiscale_g_loss,
+                vision_aided_g_loss,
+                contrastive_loss
+            ) = self.train_generator_step(
                 dl_iter = dl_iter,
                 batch_size = batch_size,
                 grad_accum_every = grad_accum_every,
                 calc_multiscale_loss = calc_multiscale_loss
             )
 
             if exists(gp_loss):
@@ -2230,15 +2505,15 @@
             if exists(multiscale_d_loss):
                 last_multiscale_d_loss = multiscale_d_loss
 
             if exists(multiscale_g_loss):
                 last_multiscale_g_loss = multiscale_g_loss
 
             if is_first_step or divisible_by(steps, self.log_steps_every):
-                self.print(f' G: {g_loss:.2f} | MSG: {last_multiscale_g_loss:.2f} | D: {d_loss:.2f} | MSD: {last_multiscale_d_loss:.2f} | GP: {last_gp_loss:.2f} | SSL: {recon_loss:.2f}')
+                self.print(f' G: {g_loss:.2f} | MSG: {last_multiscale_g_loss:.2f} | VG: {vision_aided_g_loss:.2f} | D: {d_loss:.2f} | MSD: {last_multiscale_d_loss:.2f} | VD: {vision_aided_d_loss:.2f} | GP: {last_gp_loss:.2f} | SSL: {recon_loss:.2f} | CL: {contrastive_loss:.2f} | MAL: {matching_aware_loss:.2f}')
 
             self.accelerator.wait_for_everyone()
 
             if self.is_main and (is_first_step or divisible_by(steps, self.save_and_sample_every) or (steps <= self.early_save_thres_steps and divisible_by(steps, self.early_save_and_sample_every))):
                 self.save_sample(batch_size, dl_iter)
             
             self.steps += 1
```

### Comparing `gigagan-pytorch-0.1.9/gigagan_pytorch/open_clip.py` & `gigagan-pytorch-0.2.0/gigagan_pytorch/open_clip.py`

 * *Files 2% similar despite different names*

```diff
@@ -10,16 +10,16 @@
 
 def exists(val):
     return val is not None
 
 def l2norm(t):
     return F.normalize(t, dim = -1)
 
-@beartype
 class OpenClipAdapter(nn.Module):
+    @beartype
     def __init__(
         self,
         name = 'ViT-B/32',
         pretrained = 'laion400m_e32',
         tokenizer_name = 'ViT-B-32-quickgelu',
         eos_id = 49407
     ):
@@ -96,14 +96,15 @@
     def image_channels(self):
         return 3
 
     @property
     def max_text_len(self):
         return self.clip.positional_embedding.shape[0]
 
+    @beartype
     def embed_texts(
         self,
         texts: List[str]
     ):
         ids = self.tokenizer(texts)
         ids = ids.to(self.device)
         ids = ids[..., :self.max_text_len]
@@ -129,14 +130,15 @@
         image_embeds = self.clip.encode_image(images)
 
         image_encodings = rearrange(self.image_encodings, 'l n b d -> l b n d')
         del self.image_encodings
 
         return l2norm(image_embeds.float()), image_encodings.float()
 
+    @beartype
     def contrastive_loss(
         self,
         images,
         texts: Optional[List[str]] = None,
         text_embeds: Optional[torch.Tensor] = None
     ):
         assert exists(texts) ^ exists(text_embeds)
```

### Comparing `gigagan-pytorch-0.1.9/gigagan_pytorch/optimizer.py` & `gigagan-pytorch-0.2.0/gigagan_pytorch/optimizer.py`

 * *Files identical despite different names*

### Comparing `gigagan-pytorch-0.1.9/gigagan_pytorch/unet_upsampler.py` & `gigagan-pytorch-0.2.0/gigagan_pytorch/unet_upsampler.py`

 * *Files 4% similar despite different names*

```diff
@@ -10,15 +10,16 @@
 
 from gigagan_pytorch.attend import Attend
 from gigagan_pytorch.gigagan_pytorch import (
     BaseGenerator,
     StyleNetwork,
     AdaptiveConv2DMod,
     TextEncoder,
-    CrossAttentionBlock
+    CrossAttentionBlock,
+    Upsample
 )
 
 from beartype import beartype
 from beartype.typing import Optional, List, Union, Dict, Iterable
 
 # helpers functions
 
@@ -43,15 +44,15 @@
 
 def null_iterator():
     while True:
         yield None
 
 # small helper modules
 
-class Upsample(nn.Module):
+class PixelShuffleUpsample(nn.Module):
     def __init__(self, dim, dim_out = None):
         super().__init__()
         dim_out = default(dim_out, dim)
 
         conv = nn.Conv2d(dim, dim_out * 4, 1)
         self.init_conv_(conv)
 
@@ -295,27 +296,29 @@
         *,
         image_size,
         input_image_size,
         init_dim = None,
         out_dim = None,
         text_encoder: Optional[Union[TextEncoder, Dict]] = None,
         style_network: Optional[Union[StyleNetwork, Dict]] = None,
+        style_network_dim = None,
         dim_mults = (1, 2, 4, 8),
         channels = 3,
         resnet_block_groups = 8,
         full_attn = (False, False, False, True),
         cross_attn = (False, False, False, True),
         flash_attn = True,
-        attn_dim_head = 64,
-        attn_heads = 8,
+        self_attn_dim_head = 64,
+        self_attn_heads = 8,
+        self_attn_dot_product = True,
+        self_attn_ff_mult = 4,
         attn_depths = (1, 1, 1, 1),
         cross_attn_dim_head = 64,
         cross_attn_heads = 8,
         cross_ff_mult = 4,
-        ff_mult = 4,
         mid_attn_depth = 1,
         num_conv_kernels = 2,
         resize_mode = 'bilinear',
         unconditional = True
     ):
         super().__init__()
 
@@ -327,14 +330,16 @@
         self.text_encoder = text_encoder
 
         if isinstance(style_network, dict):
             style_network = StyleNetwork(**style_network)
 
         self.style_network = style_network
 
+        assert exists(style_network) ^ exists(style_network_dim), 'either style_network or style_network_dim must be passed in'
+
         # validate text conditioning and style network hparams
 
         self.unconditional = unconditional
         assert unconditional ^ exists(text_encoder), 'if unconditional, text encoder should not be given, and vice versa'
         assert not (unconditional and exists(style_network) and style_network.dim_text_latent > 0)
         assert unconditional or text_encoder.dim == style_network.dim_text_latent, 'the `dim_text_latent` on your StyleNetwork must be equal to the `dim` set for the TextEncoder'
 
@@ -395,45 +400,44 @@
             has_cross_attn = not self.unconditional and layer_cross_attn
 
             attn_klass = FullAttention if layer_full_attn else LinearTransformer
 
             self.downs.append(nn.ModuleList([
                 block_klass(dim_in, dim_in),
                 block_klass(dim_in, dim_in),
-                CrossAttentionBlock(dim_in, dim_context = text_encoder.dim, dim_head = attn_dim_head, heads = attn_heads, ff_mult = ff_mult) if has_cross_attn else None,
-                attn_klass(dim_in, dim_head = attn_dim_head, heads = attn_heads, depth = layer_attn_depth),
+                CrossAttentionBlock(dim_in, dim_context = text_encoder.dim, dim_head = self_attn_dim_head, heads = self_attn_heads, ff_mult = self_attn_ff_mult) if has_cross_attn else None,
+                attn_klass(dim_in, dim_head = self_attn_dim_head, heads = self_attn_heads, depth = layer_attn_depth),
                 Downsample(dim_in, dim_out) if not should_not_downsample else nn.Conv2d(dim_in, dim_out, 3, padding = 1)
             ]))
 
         self.mid_block1 = block_klass(mid_dim, mid_dim)
-        self.mid_attn = FullAttention(mid_dim, dim_head = attn_dim_head, heads = attn_heads, depth = mid_attn_depth)
+        self.mid_attn = FullAttention(mid_dim, dim_head = self_attn_dim_head, heads = self_attn_heads, depth = mid_attn_depth)
         self.mid_block2 = block_klass(mid_dim, mid_dim)
         self.mid_to_rgb = nn.Conv2d(mid_dim, channels, 1)
 
         for ind, ((dim_in, dim_out), layer_cross_attn, layer_full_attn, layer_attn_depth) in enumerate(zip(reversed(in_out), reversed(full_attn), reversed(cross_attn), reversed(attn_depths))):
 
             attn_klass = FullAttention if layer_full_attn else LinearTransformer
             has_cross_attn = not self.unconditional and layer_cross_attn
 
             self.ups.append(nn.ModuleList([
-                Upsample(dim_out, dim_in),
-                Upsample(channels),
+                PixelShuffleUpsample(dim_out, dim_in),
+                Upsample(),
                 nn.Conv2d(dim_in, channels, 1),
                 block_klass(dim_in * 2, dim_in),
                 block_klass(dim_in * 2, dim_in),
-                CrossAttentionBlock(dim_in, dim_context = text_encoder.dim, dim_head = attn_dim_head, heads = attn_heads, ff_mult = ff_mult) if has_cross_attn else None,
-                attn_klass(dim_in, dim_head = attn_dim_head, heads = attn_heads, depth = layer_attn_depth),
+                CrossAttentionBlock(dim_in, dim_context = text_encoder.dim, dim_head = self_attn_dim_head, heads = self_attn_heads, ff_mult = cross_ff_mult) if has_cross_attn else None,
+                attn_klass(dim_in, dim_head = cross_attn_dim_head, heads = self_attn_heads, depth = layer_attn_depth),
             ]))
 
         self.out_dim = default(out_dim, channels)
 
         self.final_res_block = block_klass(dim, dim)
 
         self.final_to_rgb = nn.Conv2d(dim, channels, 1)
-        self.final_conv = nn.Conv2d(dim, self.out_dim, 1)
 
         # resize mode
 
         self.resize_mode = resize_mode
 
         # determine the projection of the style embedding to convolutional modulation weights (+ adaptive kernel selection weights) for all layers
 
@@ -506,24 +510,25 @@
 
         for block1, block2, cross_attn, attn, downsample in self.downs:
             x = block1(x, conv_mods_iter = conv_mods)
             h.append(x)
 
             x = block2(x, conv_mods_iter = conv_mods)
 
+            x = attn(x)
+
             if exists(cross_attn):
                 x = cross_attn(x, context = fine_text_tokens, mask = text_mask)
 
-            x = attn(x) + x
             h.append(x)
 
             x = downsample(x)
 
         x = self.mid_block1(x, conv_mods_iter = conv_mods)
-        x = self.mid_attn(x) + x
+        x = self.mid_attn(x)
         x = self.mid_block2(x, conv_mods_iter = conv_mods)
 
         # rgbs
 
         rgbs = []
 
         init_rgb_shape = list(x.shape)
@@ -554,15 +559,15 @@
 
             x = torch.cat((x, res2), dim = 1)
             x = block2(x, conv_mods_iter = conv_mods)
 
             if exists(cross_attn):
                 x = cross_attn(x, context = fine_text_tokens, mask = text_mask)
 
-            x = attn(x) + x
+            x = attn(x)
 
             rgb = rgb + to_rgb(x)
             rgbs.append(rgb)
 
         x = self.final_res_block(x, conv_mods_iter = conv_mods)
 
         assert len([*conv_mods]) == 0
```

### Comparing `gigagan-pytorch-0.1.9/gigagan_pytorch.egg-info/PKG-INFO` & `gigagan-pytorch-0.2.0/gigagan_pytorch.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: gigagan-pytorch
-Version: 0.1.9
+Version: 0.2.0
 Summary: GigaGAN - Pytorch
 Home-page: https://github.com/lucidrains/ETSformer-pytorch
 Author: Phil Wang
 Author-email: lucidrains@gmail.com
 License: MIT
 Keywords: artificial intelligence,deep learning,generative adversarial networks
 Classifier: Development Status :: 4 - Beta
```

### Comparing `gigagan-pytorch-0.1.9/setup.py` & `gigagan-pytorch-0.2.0/setup.py`

 * *Files 10% similar despite different names*

```diff
@@ -18,14 +18,15 @@
     'generative adversarial networks'
   ],
   install_requires=[
     'accelerate',
     'beartype',
     'einops>=0.6',
     'ema-pytorch',
+    'kornia',
     'numerize',
     'open-clip-torch>=2.0.0,<3.0.0',
     'pillow',
     'torch>=1.6',
     'torchvision',
     'tqdm'
   ],
```

