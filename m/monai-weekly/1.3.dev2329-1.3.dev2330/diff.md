# Comparing `tmp/monai-weekly-1.3.dev2329.tar.gz` & `tmp/monai-weekly-1.3.dev2330.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "monai-weekly-1.3.dev2329.tar", last modified: Sun Jul 16 02:38:16 2023, max compression
+gzip compressed data, was "monai-weekly-1.3.dev2330.tar", last modified: Sun Jul 23 02:23:51 2023, max compression
```

## Comparing `monai-weekly-1.3.dev2329.tar` & `monai-weekly-1.3.dev2330.tar`

### file list

```diff
@@ -1,1147 +1,1147 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:16.634372 monai-weekly-1.3.dev2329/
--rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       83 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     7124 2023-07-16 02:38:16.634372 monai-weekly-1.3.dev2329/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     5001 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:16.634372 monai-weekly-1.3.dev2329/monai/
--rw-r--r--   0 runner    (1001) docker     (123)     2335 2023-07-16 02:36:14.000000 monai-weekly-1.3.dev2329/monai/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.906374 monai-weekly-1.3.dev2329/monai/_extensions/
--rw-r--r--   0 runner    (1001) docker     (123)      642 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/_extensions/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.910374 monai-weekly-1.3.dev2329/monai/_extensions/gmm/
--rw-r--r--   0 runner    (1001) docker     (123)     2931 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/_extensions/gmm/gmm.cpp
--rw-r--r--   0 runner    (1001) docker     (123)     1760 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/_extensions/gmm/gmm.h
--rw-r--r--   0 runner    (1001) docker     (123)     1118 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/_extensions/gmm/gmm_cpu.cpp
--rw-r--r--   0 runner    (1001) docker     (123)    15983 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/_extensions/gmm/gmm_cuda.cu
--rw-r--r--   0 runner    (1001) docker     (123)     3520 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/_extensions/gmm/gmm_cuda_linalg.cuh
--rw-r--r--   0 runner    (1001) docker     (123)     3643 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/_extensions/loader.py
--rw-r--r--   0 runner    (1001) docker     (123)      503 2023-07-16 02:38:16.634372 monai-weekly-1.3.dev2329/monai/_version.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.910374 monai-weekly-1.3.dev2329/monai/apps/
--rw-r--r--   0 runner    (1001) docker     (123)      908 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.918373 monai-weekly-1.3.dev2329/monai/apps/auto3dseg/
--rw-r--r--   0 runner    (1001) docker     (123)     1016 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/auto3dseg/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1411 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/auto3dseg/__main__.py
--rw-r--r--   0 runner    (1001) docker     (123)    37154 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/auto3dseg/auto_runner.py
--rw-r--r--   0 runner    (1001) docker     (123)    26165 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/auto3dseg/bundle_gen.py
--rw-r--r--   0 runner    (1001) docker     (123)    17517 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/auto3dseg/data_analyzer.py
--rw-r--r--   0 runner    (1001) docker     (123)    27506 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/auto3dseg/ensemble_builder.py
--rw-r--r--   0 runner    (1001) docker     (123)    16620 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/auto3dseg/hpo_gen.py
--rw-r--r--   0 runner    (1001) docker     (123)     3991 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/auto3dseg/transforms.py
--rw-r--r--   0 runner    (1001) docker     (123)     3138 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/auto3dseg/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)    34568 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/datasets.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.918373 monai-weekly-1.3.dev2329/monai/apps/deepedit/
--rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/deepedit/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4501 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/deepedit/interaction.py
--rw-r--r--   0 runner    (1001) docker     (123)    37435 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/deepedit/transforms.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.922374 monai-weekly-1.3.dev2329/monai/apps/deepgrow/
--rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/deepgrow/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    10054 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/deepgrow/dataset.py
--rw-r--r--   0 runner    (1001) docker     (123)     3739 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/deepgrow/interaction.py
--rw-r--r--   0 runner    (1001) docker     (123)    42011 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/deepgrow/transforms.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.922374 monai-weekly-1.3.dev2329/monai/apps/detection/
--rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/detection/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.926374 monai-weekly-1.3.dev2329/monai/apps/detection/metrics/
--rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/detection/metrics/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    26617 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/detection/metrics/coco.py
--rw-r--r--   0 runner    (1001) docker     (123)    17161 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/detection/metrics/matching.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.926374 monai-weekly-1.3.dev2329/monai/apps/detection/networks/
--rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/detection/networks/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    53640 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/detection/networks/retinanet_detector.py
--rw-r--r--   0 runner    (1001) docker     (123)    19136 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/detection/networks/retinanet_network.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.930374 monai-weekly-1.3.dev2329/monai/apps/detection/transforms/
--rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/detection/transforms/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    24519 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/detection/transforms/array.py
--rw-r--r--   0 runner    (1001) docker     (123)    18051 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/detection/transforms/box_ops.py
--rw-r--r--   0 runner    (1001) docker     (123)    69282 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/detection/transforms/dictionary.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.934373 monai-weekly-1.3.dev2329/monai/apps/detection/utils/
--rw-r--r--   0 runner    (1001) docker     (123)    13531 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/detection/utils/ATSS_matcher.py
--rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/detection/utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    18681 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/detection/utils/anchor_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)    11120 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/detection/utils/box_coder.py
--rw-r--r--   0 runner    (1001) docker     (123)     9031 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/detection/utils/box_selector.py
--rw-r--r--   0 runner    (1001) docker     (123)    10306 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/detection/utils/detector_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)    13890 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/detection/utils/hard_negative_sampler.py
--rw-r--r--   0 runner    (1001) docker     (123)     5818 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/detection/utils/predict_utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.938373 monai-weekly-1.3.dev2329/monai/apps/mmars/
--rw-r--r--   0 runner    (1001) docker     (123)      726 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/mmars/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    13115 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/mmars/mmars.py
--rw-r--r--   0 runner    (1001) docker     (123)     9996 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/mmars/model_desc.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.942374 monai-weekly-1.3.dev2329/monai/apps/nnunet/
--rw-r--r--   0 runner    (1001) docker     (123)      745 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/nnunet/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      832 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/nnunet/__main__.py
--rw-r--r--   0 runner    (1001) docker     (123)    48577 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/nnunet/nnunetv2_runner.py
--rw-r--r--   0 runner    (1001) docker     (123)     6761 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/nnunet/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.942374 monai-weekly-1.3.dev2329/monai/apps/nuclick/
--rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/nuclick/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    24948 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/nuclick/transforms.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.942374 monai-weekly-1.3.dev2329/monai/apps/pathology/
--rw-r--r--   0 runner    (1001) docker     (123)     1030 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/pathology/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.946374 monai-weekly-1.3.dev2329/monai/apps/pathology/engines/
--rw-r--r--   0 runner    (1001) docker     (123)      650 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/pathology/engines/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2397 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/pathology/engines/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.946374 monai-weekly-1.3.dev2329/monai/apps/pathology/handlers/
--rw-r--r--   0 runner    (1001) docker     (123)      609 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/pathology/handlers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2315 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/pathology/handlers/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.946374 monai-weekly-1.3.dev2329/monai/apps/pathology/inferers/
--rw-r--r--   0 runner    (1001) docker     (123)      660 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/pathology/inferers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     9148 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/pathology/inferers/inferer.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.946374 monai-weekly-1.3.dev2329/monai/apps/pathology/losses/
--rw-r--r--   0 runner    (1001) docker     (123)      650 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/pathology/losses/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7293 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/pathology/losses/hovernet_loss.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.950374 monai-weekly-1.3.dev2329/monai/apps/pathology/metrics/
--rw-r--r--   0 runner    (1001) docker     (123)      646 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/pathology/metrics/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7225 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/pathology/metrics/lesion_froc.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.950374 monai-weekly-1.3.dev2329/monai/apps/pathology/transforms/
--rw-r--r--   0 runner    (1001) docker     (123)     2243 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/pathology/transforms/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.950374 monai-weekly-1.3.dev2329/monai/apps/pathology/transforms/post/
--rw-r--r--   0 runner    (1001) docker     (123)     1995 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/pathology/transforms/post/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    37306 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/pathology/transforms/post/array.py
--rw-r--r--   0 runner    (1001) docker     (123)    25928 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/pathology/transforms/post/dictionary.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.954373 monai-weekly-1.3.dev2329/monai/apps/pathology/transforms/stain/
--rw-r--r--   0 runner    (1001) docker     (123)      836 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/pathology/transforms/stain/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     8366 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/pathology/transforms/stain/array.py
--rw-r--r--   0 runner    (1001) docker     (123)     4761 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/pathology/transforms/stain/dictionary.py
--rw-r--r--   0 runner    (1001) docker     (123)     2860 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/pathology/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.954373 monai-weekly-1.3.dev2329/monai/apps/reconstruction/
--rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/reconstruction/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     8393 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/reconstruction/complex_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     3644 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/reconstruction/fastmri_reader.py
--rw-r--r--   0 runner    (1001) docker     (123)     2000 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/reconstruction/mri_utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.954373 monai-weekly-1.3.dev2329/monai/apps/reconstruction/networks/
--rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/reconstruction/networks/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.958373 monai-weekly-1.3.dev2329/monai/apps/reconstruction/networks/blocks/
--rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/reconstruction/networks/blocks/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4183 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/reconstruction/networks/blocks/varnetblock.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.958373 monai-weekly-1.3.dev2329/monai/apps/reconstruction/networks/nets/
--rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/reconstruction/networks/nets/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6215 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/reconstruction/networks/nets/coil_sensitivity_model.py
--rw-r--r--   0 runner    (1001) docker     (123)     4775 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/reconstruction/networks/nets/complex_unet.py
--rw-r--r--   0 runner    (1001) docker     (123)    11377 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/reconstruction/networks/nets/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     3831 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/reconstruction/networks/nets/varnet.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.962373 monai-weekly-1.3.dev2329/monai/apps/reconstruction/transforms/
--rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/reconstruction/transforms/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    12240 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/reconstruction/transforms/array.py
--rw-r--r--   0 runner    (1001) docker     (123)    15829 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/reconstruction/transforms/dictionary.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.962373 monai-weekly-1.3.dev2329/monai/apps/tcia/
--rw-r--r--   0 runner    (1001) docker     (123)      765 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/tcia/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1582 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/tcia/label_desc.py
--rw-r--r--   0 runner    (1001) docker     (123)     6152 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/tcia/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)    14170 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/apps/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.966374 monai-weekly-1.3.dev2329/monai/auto3dseg/
--rw-r--r--   0 runner    (1001) docker     (123)     1164 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/auto3dseg/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4286 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/auto3dseg/algo_gen.py
--rw-r--r--   0 runner    (1001) docker     (123)    41223 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/auto3dseg/analyzer.py
--rw-r--r--   0 runner    (1001) docker     (123)     5110 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/auto3dseg/operations.py
--rw-r--r--   0 runner    (1001) docker     (123)     8725 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/auto3dseg/seg_summarizer.py
--rw-r--r--   0 runner    (1001) docker     (123)    18650 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/auto3dseg/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.974373 monai-weekly-1.3.dev2329/monai/bundle/
--rw-r--r--   0 runner    (1001) docker     (123)     1341 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/bundle/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      926 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/bundle/__main__.py
--rw-r--r--   0 runner    (1001) docker     (123)    16035 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/bundle/config_item.py
--rw-r--r--   0 runner    (1001) docker     (123)    22360 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/bundle/config_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     9814 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/bundle/properties.py
--rw-r--r--   0 runner    (1001) docker     (123)    14353 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/bundle/reference_resolver.py
--rw-r--r--   0 runner    (1001) docker     (123)    64632 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/bundle/scripts.py
--rw-r--r--   0 runner    (1001) docker     (123)     8911 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/bundle/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)    19172 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/bundle/workflows.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.974373 monai-weekly-1.3.dev2329/monai/config/
--rw-r--r--   0 runner    (1001) docker     (123)     1048 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/config/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     9913 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/config/deviceconfig.py
--rw-r--r--   0 runner    (1001) docker     (123)     3485 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/config/type_definitions.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.994373 monai-weekly-1.3.dev2329/monai/data/
--rw-r--r--   0 runner    (1001) docker     (123)     5087 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/data/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    50102 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/data/box_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     4952 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/data/csv_saver.py
--rw-r--r--   0 runner    (1001) docker     (123)     3835 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/data/dataloader.py
--rw-r--r--   0 runner    (1001) docker     (123)    68912 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/data/dataset.py
--rw-r--r--   0 runner    (1001) docker     (123)    10216 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/data/dataset_summary.py
--rw-r--r--   0 runner    (1001) docker     (123)    10318 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/data/decathlon_datalist.py
--rw-r--r--   0 runner    (1001) docker     (123)     4448 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/data/fft_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     6344 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/data/folder_layout.py
--rw-r--r--   0 runner    (1001) docker     (123)    12484 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/data/grid_dataset.py
--rw-r--r--   0 runner    (1001) docker     (123)     7008 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/data/image_dataset.py
--rw-r--r--   0 runner    (1001) docker     (123)    60653 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/data/image_reader.py
--rw-r--r--   0 runner    (1001) docker     (123)    39872 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/data/image_writer.py
--rw-r--r--   0 runner    (1001) docker     (123)    13309 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/data/iterable_dataset.py
--rw-r--r--   0 runner    (1001) docker     (123)    14097 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/data/itk_torch_bridge.py
--rw-r--r--   0 runner    (1001) docker     (123)     8800 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/data/meta_obj.py
--rw-r--r--   0 runner    (1001) docker     (123)    27511 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/data/meta_tensor.py
--rw-r--r--   0 runner    (1001) docker     (123)     5268 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/data/samplers.py
--rw-r--r--   0 runner    (1001) docker     (123)     7375 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/data/synthetic.py
--rw-r--r--   0 runner    (1001) docker     (123)     9780 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/data/test_time_augmentation.py
--rw-r--r--   0 runner    (1001) docker     (123)     8840 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/data/thread_buffer.py
--rw-r--r--   0 runner    (1001) docker     (123)     5500 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/data/torchscript_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)    65554 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/data/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     9059 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/data/video_dataset.py
--rw-r--r--   0 runner    (1001) docker     (123)    18619 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/data/wsi_datasets.py
--rw-r--r--   0 runner    (1001) docker     (123)    49494 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/data/wsi_reader.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:15.998373 monai-weekly-1.3.dev2329/monai/engines/
--rw-r--r--   0 runner    (1001) docker     (123)     1133 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/engines/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    24568 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/engines/evaluator.py
--rw-r--r--   0 runner    (1001) docker     (123)     7278 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/engines/multi_gpu_supervised_trainer.py
--rw-r--r--   0 runner    (1001) docker     (123)    21347 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/engines/trainer.py
--rw-r--r--   0 runner    (1001) docker     (123)    11631 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/engines/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)    15250 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/engines/workflow.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:16.002373 monai-weekly-1.3.dev2329/monai/fl/
--rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/fl/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:16.002373 monai-weekly-1.3.dev2329/monai/fl/client/
--rw-r--r--   0 runner    (1001) docker     (123)      725 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/fl/client/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5097 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/fl/client/client_algo.py
--rw-r--r--   0 runner    (1001) docker     (123)    33232 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/fl/client/monai_algo.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:16.006373 monai-weekly-1.3.dev2329/monai/fl/utils/
--rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/fl/utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1713 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/fl/utils/constants.py
--rw-r--r--   0 runner    (1001) docker     (123)     3527 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/fl/utils/exchange_object.py
--rw-r--r--   0 runner    (1001) docker     (123)     1633 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/fl/utils/filters.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:16.026373 monai-weekly-1.3.dev2329/monai/handlers/
--rw-r--r--   0 runner    (1001) docker     (123)     2372 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6798 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/checkpoint_loader.py
--rw-r--r--   0 runner    (1001) docker     (123)    16071 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/checkpoint_saver.py
--rw-r--r--   0 runner    (1001) docker     (123)     7606 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/classification_saver.py
--rw-r--r--   0 runner    (1001) docker     (123)     7506 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/clearml_handlers.py
--rw-r--r--   0 runner    (1001) docker     (123)     4006 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/confusion_matrix.py
--rw-r--r--   0 runner    (1001) docker     (123)     4425 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/decollate_batch.py
--rw-r--r--   0 runner    (1001) docker     (123)     4381 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/earlystop_handler.py
--rw-r--r--   0 runner    (1001) docker     (123)     3645 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/garbage_collector.py
--rw-r--r--   0 runner    (1001) docker     (123)     3594 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/hausdorff_distance.py
--rw-r--r--   0 runner    (1001) docker     (123)     7460 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/ignite_metric.py
--rw-r--r--   0 runner    (1001) docker     (123)     3931 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/logfile_handler.py
--rw-r--r--   0 runner    (1001) docker     (123)     3575 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/lr_schedule_handler.py
--rw-r--r--   0 runner    (1001) docker     (123)     3234 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/mean_dice.py
--rw-r--r--   0 runner    (1001) docker     (123)     2845 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/mean_iou.py
--rw-r--r--   0 runner    (1001) docker     (123)     5477 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/metric_logger.py
--rw-r--r--   0 runner    (1001) docker     (123)     6195 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/metrics_reloaded_handler.py
--rw-r--r--   0 runner    (1001) docker     (123)     8560 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/metrics_saver.py
--rw-r--r--   0 runner    (1001) docker     (123)    16845 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/mlflow_handler.py
--rw-r--r--   0 runner    (1001) docker     (123)     6819 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/nvtx_handlers.py
--rw-r--r--   0 runner    (1001) docker     (123)     3651 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/panoptic_quality.py
--rw-r--r--   0 runner    (1001) docker     (123)     7119 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/parameter_scheduler.py
--rw-r--r--   0 runner    (1001) docker     (123)     3285 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/postprocessing.py
--rw-r--r--   0 runner    (1001) docker     (123)     5336 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/probability_maps.py
--rw-r--r--   0 runner    (1001) docker     (123)     8457 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/regression_metrics.py
--rw-r--r--   0 runner    (1001) docker     (123)     2744 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/roc_auc.py
--rw-r--r--   0 runner    (1001) docker     (123)     3051 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/smartcache_handler.py
--rw-r--r--   0 runner    (1001) docker     (123)    14251 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/stats_handler.py
--rw-r--r--   0 runner    (1001) docker     (123)     3327 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/surface_distance.py
--rw-r--r--   0 runner    (1001) docker     (123)    23325 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/tensorboard_handlers.py
--rw-r--r--   0 runner    (1001) docker     (123)     9855 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     3269 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/handlers/validation_handler.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:16.030373 monai-weekly-1.3.dev2329/monai/inferers/
--rw-r--r--   0 runner    (1001) docker     (123)      958 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/inferers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    33929 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/inferers/inferer.py
--rw-r--r--   0 runner    (1001) docker     (123)    15566 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/inferers/merger.py
--rw-r--r--   0 runner    (1001) docker     (123)    21149 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/inferers/splitter.py
--rw-r--r--   0 runner    (1001) docker     (123)    20017 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/inferers/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:16.038373 monai-weekly-1.3.dev2329/monai/losses/
--rw-r--r--   0 runner    (1001) docker     (123)     1409 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/losses/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3341 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/losses/contrastive.py
--rw-r--r--   0 runner    (1001) docker     (123)     4979 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/losses/deform.py
--rw-r--r--   0 runner    (1001) docker     (123)    46326 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/losses/dice.py
--rw-r--r--   0 runner    (1001) docker     (123)     3854 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/losses/ds_loss.py
--rw-r--r--   0 runner    (1001) docker     (123)    11733 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/losses/focal_loss.py
--rw-r--r--   0 runner    (1001) docker     (123)     2795 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/losses/giou_loss.py
--rw-r--r--   0 runner    (1001) docker     (123)    15492 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/losses/image_dissimilarity.py
--rw-r--r--   0 runner    (1001) docker     (123)     3636 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/losses/multi_scale.py
--rw-r--r--   0 runner    (1001) docker     (123)     2955 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/losses/spatial_mask.py
--rw-r--r--   0 runner    (1001) docker     (123)     4825 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/losses/ssim_loss.py
--rw-r--r--   0 runner    (1001) docker     (123)     6645 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/losses/tversky.py
--rw-r--r--   0 runner    (1001) docker     (123)    10224 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/losses/unified_focal_loss.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:16.050373 monai-weekly-1.3.dev2329/monai/metrics/
--rw-r--r--   0 runner    (1001) docker     (123)     2001 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/metrics/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     8211 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/metrics/active_learning_metrics.py
--rw-r--r--   0 runner    (1001) docker     (123)    15107 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/metrics/confusion_matrix.py
--rw-r--r--   0 runner    (1001) docker     (123)     5578 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/metrics/cumulative_average.py
--rw-r--r--   0 runner    (1001) docker     (123)     4026 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/metrics/f_beta_score.py
--rw-r--r--   0 runner    (1001) docker     (123)     7981 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/metrics/froc.py
--rw-r--r--   0 runner    (1001) docker     (123)     8265 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/metrics/generalized_dice.py
--rw-r--r--   0 runner    (1001) docker     (123)    11473 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/metrics/hausdorff_distance.py
--rw-r--r--   0 runner    (1001) docker     (123)     4907 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/metrics/loss_metric.py
--rw-r--r--   0 runner    (1001) docker     (123)    12481 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/metrics/meandice.py
--rw-r--r--   0 runner    (1001) docker     (123)     7215 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/metrics/meaniou.py
--rw-r--r--   0 runner    (1001) docker     (123)    15140 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/metrics/metric.py
--rw-r--r--   0 runner    (1001) docker     (123)    13679 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/metrics/panoptic_quality.py
--rw-r--r--   0 runner    (1001) docker     (123)    19719 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/metrics/regression.py
--rw-r--r--   0 runner    (1001) docker     (123)     8038 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/metrics/rocauc.py
--rw-r--r--   0 runner    (1001) docker     (123)    15886 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/metrics/surface_dice.py
--rw-r--r--   0 runner    (1001) docker     (123)    10192 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/metrics/surface_distance.py
--rw-r--r--   0 runner    (1001) docker     (123)    42238 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/metrics/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)    11781 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/metrics/wrapper.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:16.050373 monai-weekly-1.3.dev2329/monai/networks/
--rw-r--r--   0 runner    (1001) docker     (123)     1020 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:16.074373 monai-weekly-1.3.dev2329/monai/networks/blocks/
--rw-r--r--   0 runner    (1001) docker     (123)     2134 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/blocks/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4275 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/blocks/acti_norm.py
--rw-r--r--   0 runner    (1001) docker     (123)     5839 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/blocks/activation.py
--rw-r--r--   0 runner    (1001) docker     (123)     4380 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/blocks/aspp.py
--rw-r--r--   0 runner    (1001) docker     (123)     7488 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/blocks/backbone_fpn_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)    11686 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/blocks/convolutions.py
--rw-r--r--   0 runner    (1001) docker     (123)     5009 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/blocks/crf.py
--rw-r--r--   0 runner    (1001) docker     (123)     4747 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/blocks/denseblock.py
--rw-r--r--   0 runner    (1001) docker     (123)     9255 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/blocks/dints_block.py
--rw-r--r--   0 runner    (1001) docker     (123)     2413 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/blocks/downsample.py
--rw-r--r--   0 runner    (1001) docker     (123)    11062 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/blocks/dynunet_block.py
--rw-r--r--   0 runner    (1001) docker     (123)     3669 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/blocks/encoder.py
--rw-r--r--   0 runner    (1001) docker     (123)     9024 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/blocks/fcn.py
--rw-r--r--   0 runner    (1001) docker     (123)    10586 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/blocks/feature_pyramid_network.py
--rw-r--r--   0 runner    (1001) docker     (123)     8263 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/blocks/fft_utils_t.py
--rw-r--r--   0 runner    (1001) docker     (123)    11454 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/blocks/localnet_block.py
--rw-r--r--   0 runner    (1001) docker     (123)     2813 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/blocks/mlp.py
--rw-r--r--   0 runner    (1001) docker     (123)     8030 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/blocks/patchembedding.py
--rw-r--r--   0 runner    (1001) docker     (123)     8825 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/blocks/regunet_block.py
--rw-r--r--   0 runner    (1001) docker     (123)     3245 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/blocks/segresnet_block.py
--rw-r--r--   0 runner    (1001) docker     (123)     3099 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/blocks/selfattention.py
--rw-r--r--   0 runner    (1001) docker     (123)    12752 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/blocks/squeeze_and_excitation.py
--rw-r--r--   0 runner    (1001) docker     (123)     3814 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/blocks/text_embedding.py
--rw-r--r--   0 runner    (1001) docker     (123)     2322 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/blocks/transformerblock.py
--rw-r--r--   0 runner    (1001) docker     (123)     9049 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/blocks/unetr_block.py
--rw-r--r--   0 runner    (1001) docker     (123)    13312 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/blocks/upsample.py
--rw-r--r--   0 runner    (1001) docker     (123)     6656 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/blocks/warp.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:16.082373 monai-weekly-1.3.dev2329/monai/networks/layers/
--rw-r--r--   0 runner    (1001) docker     (123)     1562 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/layers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     8288 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/layers/convutils.py
--rw-r--r--   0 runner    (1001) docker     (123)     1802 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/layers/drop_path.py
--rw-r--r--   0 runner    (1001) docker     (123)    12638 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/layers/factories.py
--rw-r--r--   0 runner    (1001) docker     (123)    17992 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/layers/filtering.py
--rw-r--r--   0 runner    (1001) docker     (123)     3324 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/layers/gmm.py
--rw-r--r--   0 runner    (1001) docker     (123)    28470 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/layers/simplelayers.py
--rw-r--r--   0 runner    (1001) docker     (123)    25576 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/layers/spatial_transforms.py
--rw-r--r--   0 runner    (1001) docker     (123)     4296 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/layers/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     2253 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/layers/weight_init.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:16.106373 monai-weekly-1.3.dev2329/monai/networks/nets/
--rw-r--r--   0 runner    (1001) docker     (123)     3197 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    21564 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/ahnet.py
--rw-r--r--   0 runner    (1001) docker     (123)     9202 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/attentionunet.py
--rw-r--r--   0 runner    (1001) docker     (123)    12089 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/autoencoder.py
--rw-r--r--   0 runner    (1001) docker     (123)    10950 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/basic_unet.py
--rw-r--r--   0 runner    (1001) docker     (123)     7960 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/basic_unetplusplus.py
--rw-r--r--   0 runner    (1001) docker     (123)     6293 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/classifier.py
--rw-r--r--   0 runner    (1001) docker     (123)    23786 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/daf3d.py
--rw-r--r--   0 runner    (1001) docker     (123)    15820 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/densenet.py
--rw-r--r--   0 runner    (1001) docker     (123)    44771 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/dints.py
--rw-r--r--   0 runner    (1001) docker     (123)    18210 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/dynunet.py
--rw-r--r--   0 runner    (1001) docker     (123)    40667 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/efficientnet.py
--rw-r--r--   0 runner    (1001) docker     (123)    14147 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/flexible_unet.py
--rw-r--r--   0 runner    (1001) docker     (123)     7212 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/fullyconnectednet.py
--rw-r--r--   0 runner    (1001) docker     (123)     6581 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/generator.py
--rw-r--r--   0 runner    (1001) docker     (123)     8882 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/highresnet.py
--rw-r--r--   0 runner    (1001) docker     (123)    28678 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/hovernet.py
--rw-r--r--   0 runner    (1001) docker     (123)     9812 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/milmodel.py
--rw-r--r--   0 runner    (1001) docker     (123)     6102 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/netadapter.py
--rw-r--r--   0 runner    (1001) docker     (123)    20220 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/quicknat.py
--rw-r--r--   0 runner    (1001) docker     (123)     6482 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/regressor.py
--rw-r--r--   0 runner    (1001) docker     (123)    18662 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/regunet.py
--rw-r--r--   0 runner    (1001) docker     (123)    16785 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/resnet.py
--rw-r--r--   0 runner    (1001) docker     (123)    13994 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/segresnet.py
--rw-r--r--   0 runner    (1001) docker     (123)    15716 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/segresnet_ds.py
--rw-r--r--   0 runner    (1001) docker     (123)    19289 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/senet.py
--rw-r--r--   0 runner    (1001) docker     (123)    42000 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/swin_unetr.py
--rw-r--r--   0 runner    (1001) docker     (123)     6309 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/torchvision_fc.py
--rw-r--r--   0 runner    (1001) docker     (123)    16626 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/transchex.py
--rw-r--r--   0 runner    (1001) docker     (123)    13722 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/unet.py
--rw-r--r--   0 runner    (1001) docker     (123)     8255 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/unetr.py
--rw-r--r--   0 runner    (1001) docker     (123)     6282 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/varautoencoder.py
--rw-r--r--   0 runner    (1001) docker     (123)     5655 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/vit.py
--rw-r--r--   0 runner    (1001) docker     (123)     5321 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/vitautoenc.py
--rw-r--r--   0 runner    (1001) docker     (123)    10011 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/nets/vnet.py
--rw-r--r--   0 runner    (1001) docker     (123)    47132 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/networks/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:16.110373 monai-weekly-1.3.dev2329/monai/optimizers/
--rw-r--r--   0 runner    (1001) docker     (123)      796 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/optimizers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    21952 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/optimizers/lr_finder.py
--rw-r--r--   0 runner    (1001) docker     (123)     4082 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/optimizers/lr_scheduler.py
--rw-r--r--   0 runner    (1001) docker     (123)     5661 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/optimizers/novograd.py
--rw-r--r--   0 runner    (1001) docker     (123)     4131 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/optimizers/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/py.typed
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:16.118373 monai-weekly-1.3.dev2329/monai/transforms/
--rw-r--r--   0 runner    (1001) docker     (123)    15545 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     8946 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/adaptors.py
--rw-r--r--   0 runner    (1001) docker     (123)    37090 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/compose.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:16.122373 monai-weekly-1.3.dev2329/monai/transforms/croppad/
--rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/croppad/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    74980 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/croppad/array.py
--rw-r--r--   0 runner    (1001) docker     (123)     6138 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/croppad/batch.py
--rw-r--r--   0 runner    (1001) docker     (123)    60975 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/croppad/dictionary.py
--rw-r--r--   0 runner    (1001) docker     (123)    12628 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/croppad/functional.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:16.126373 monai-weekly-1.3.dev2329/monai/transforms/intensity/
--rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/intensity/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)   107785 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/intensity/array.py
--rw-r--r--   0 runner    (1001) docker     (123)    82230 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/intensity/dictionary.py
--rw-r--r--   0 runner    (1001) docker     (123)    18233 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/inverse.py
--rw-r--r--   0 runner    (1001) docker     (123)     7054 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/inverse_batch_transform.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:16.130373 monai-weekly-1.3.dev2329/monai/transforms/io/
--rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/io/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    25374 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/io/array.py
--rw-r--r--   0 runner    (1001) docker     (123)    17821 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/io/dictionary.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:16.134373 monai-weekly-1.3.dev2329/monai/transforms/lazy/
--rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/lazy/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1211 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/lazy/array.py
--rw-r--r--   0 runner    (1001) docker     (123)     1571 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/lazy/dictionary.py
--rw-r--r--   0 runner    (1001) docker     (123)    15183 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/lazy/functional.py
--rw-r--r--   0 runner    (1001) docker     (123)     9840 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/lazy/utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:16.138373 monai-weekly-1.3.dev2329/monai/transforms/meta_utility/
--rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/meta_utility/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4896 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/meta_utility/dictionary.py
--rw-r--r--   0 runner    (1001) docker     (123)     3386 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/nvtx.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:16.138373 monai-weekly-1.3.dev2329/monai/transforms/post/
--rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/post/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    40802 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/post/array.py
--rw-r--r--   0 runner    (1001) docker     (123)    39905 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/post/dictionary.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:16.142373 monai-weekly-1.3.dev2329/monai/transforms/signal/
--rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/signal/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    16322 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/signal/array.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:16.142373 monai-weekly-1.3.dev2329/monai/transforms/smooth_field/
--rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/smooth_field/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    17833 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/smooth_field/array.py
--rw-r--r--   0 runner    (1001) docker     (123)    11194 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/smooth_field/dictionary.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:16.150373 monai-weekly-1.3.dev2329/monai/transforms/spatial/
--rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/spatial/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)   179599 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/spatial/array.py
--rw-r--r--   0 runner    (1001) docker     (123)   127418 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/spatial/dictionary.py
--rw-r--r--   0 runner    (1001) docker     (123)    31249 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/spatial/functional.py
--rw-r--r--   0 runner    (1001) docker     (123)     3563 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/traits.py
--rw-r--r--   0 runner    (1001) docker     (123)    21511 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/transform.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:16.150373 monai-weekly-1.3.dev2329/monai/transforms/utility/
--rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/utility/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    70963 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/utility/array.py
--rw-r--r--   0 runner    (1001) docker     (123)    76161 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/utility/dictionary.py
--rw-r--r--   0 runner    (1001) docker     (123)    81257 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)    31081 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/utils_create_transform_ims.py
--rw-r--r--   0 runner    (1001) docker     (123)    18397 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/transforms/utils_pytorch_numpy_unification.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:16.162373 monai-weekly-1.3.dev2329/monai/utils/
--rw-r--r--   0 runner    (1001) docker     (123)     3452 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4096 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/utils/aliases.py
--rw-r--r--   0 runner    (1001) docker     (123)     3129 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/utils/decorators.py
--rw-r--r--   0 runner    (1001) docker     (123)    14759 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/utils/deprecate_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     8525 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/utils/dist.py
--rw-r--r--   0 runner    (1001) docker     (123)    17055 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/utils/enums.py
--rw-r--r--   0 runner    (1001) docker     (123)    15637 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/utils/jupyter_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)    29430 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/utils/misc.py
--rw-r--r--   0 runner    (1001) docker     (123)    23631 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/utils/module.py
--rw-r--r--   0 runner    (1001) docker     (123)     6876 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/utils/nvtx.py
--rw-r--r--   0 runner    (1001) docker     (123)    15936 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/utils/profiling.py
--rw-r--r--   0 runner    (1001) docker     (123)     5955 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/utils/state_cacher.py
--rw-r--r--   0 runner    (1001) docker     (123)    21147 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/utils/type_conversion.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:16.170373 monai-weekly-1.3.dev2329/monai/visualize/
--rw-r--r--   0 runner    (1001) docker     (123)     1038 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/visualize/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    16156 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/visualize/class_activation_maps.py
--rw-r--r--   0 runner    (1001) docker     (123)     6277 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/visualize/gradient_based.py
--rw-r--r--   0 runner    (1001) docker     (123)     9200 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/visualize/img2tensorboard.py
--rw-r--r--   0 runner    (1001) docker     (123)    18160 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/visualize/occlusion_sensitivity.py
--rw-r--r--   0 runner    (1001) docker     (123)     9966 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/visualize/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     1377 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/monai/visualize/visualizer.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:16.170373 monai-weekly-1.3.dev2329/monai_weekly.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     7124 2023-07-16 02:38:15.000000 monai-weekly-1.3.dev2329/monai_weekly.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)    34350 2023-07-16 02:38:15.000000 monai-weekly-1.3.dev2329/monai_weekly.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-16 02:38:15.000000 monai-weekly-1.3.dev2329/monai_weekly.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-16 02:38:15.000000 monai-weekly-1.3.dev2329/monai_weekly.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)     1155 2023-07-16 02:38:15.000000 monai-weekly-1.3.dev2329/monai_weekly.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        6 2023-07-16 02:38:15.000000 monai-weekly-1.3.dev2329/monai_weekly.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)     1831 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)     4272 2023-07-16 02:38:16.634372 monai-weekly-1.3.dev2329/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     5183 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 02:38:16.634372 monai-weekly-1.3.dev2329/tests/
--rw-r--r--   0 runner    (1001) docker     (123)     1390 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_acn_block.py
--rw-r--r--   0 runner    (1001) docker     (123)     3822 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_activations.py
--rw-r--r--   0 runner    (1001) docker     (123)     2483 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_activationsd.py
--rw-r--r--   0 runner    (1001) docker     (123)     4576 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_adaptors.py
--rw-r--r--   0 runner    (1001) docker     (123)     1370 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_add_channeld.py
--rw-r--r--   0 runner    (1001) docker     (123)     2243 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_add_coordinate_channels.py
--rw-r--r--   0 runner    (1001) docker     (123)     2479 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_add_coordinate_channelsd.py
--rw-r--r--   0 runner    (1001) docker     (123)     2770 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_add_extreme_points_channel.py
--rw-r--r--   0 runner    (1001) docker     (123)     2647 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_add_extreme_points_channeld.py
--rw-r--r--   0 runner    (1001) docker     (123)     2573 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_adjust_contrast.py
--rw-r--r--   0 runner    (1001) docker     (123)     2365 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_adjust_contrastd.py
--rw-r--r--   0 runner    (1001) docker     (123)     3186 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_adn.py
--rw-r--r--   0 runner    (1001) docker     (123)    10055 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_affine.py
--rw-r--r--   0 runner    (1001) docker     (123)     6623 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_affine_grid.py
--rw-r--r--   0 runner    (1001) docker     (123)    19674 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_affine_transform.py
--rw-r--r--   0 runner    (1001) docker     (123)     7832 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_affined.py
--rw-r--r--   0 runner    (1001) docker     (123)     8343 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_ahnet.py
--rw-r--r--   0 runner    (1001) docker     (123)     1514 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_alias.py
--rw-r--r--   0 runner    (1001) docker     (123)     3921 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_anchor_box.py
--rw-r--r--   0 runner    (1001) docker     (123)     2844 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_apply.py
--rw-r--r--   0 runner    (1001) docker     (123)     3740 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_apply_filter.py
--rw-r--r--   0 runner    (1001) docker     (123)     8267 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_arraydataset.py
--rw-r--r--   0 runner    (1001) docker     (123)     1576 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_as_channel_first.py
--rw-r--r--   0 runner    (1001) docker     (123)     1800 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_as_channel_firstd.py
--rw-r--r--   0 runner    (1001) docker     (123)     1353 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_as_channel_last.py
--rw-r--r--   0 runner    (1001) docker     (123)     1796 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_as_channel_lastd.py
--rw-r--r--   0 runner    (1001) docker     (123)     2599 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_as_discrete.py
--rw-r--r--   0 runner    (1001) docker     (123)     3047 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_as_discreted.py
--rw-r--r--   0 runner    (1001) docker     (123)     1701 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_atss_box_matcher.py
--rw-r--r--   0 runner    (1001) docker     (123)     2660 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_attentionunet.py
--rw-r--r--   0 runner    (1001) docker     (123)    21578 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_auto3dseg.py
--rw-r--r--   0 runner    (1001) docker     (123)     5589 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_auto3dseg_bundlegen.py
--rw-r--r--   0 runner    (1001) docker     (123)     7565 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_auto3dseg_ensemble.py
--rw-r--r--   0 runner    (1001) docker     (123)     7281 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_auto3dseg_hpo.py
--rw-r--r--   0 runner    (1001) docker     (123)     2959 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_autoencoder.py
--rw-r--r--   0 runner    (1001) docker     (123)     5947 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_avg_merger.py
--rw-r--r--   0 runner    (1001) docker     (123)     3332 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_basic_unet.py
--rw-r--r--   0 runner    (1001) docker     (123)     3707 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_basic_unetplusplus.py
--rw-r--r--   0 runner    (1001) docker     (123)     3661 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_bending_energy.py
--rw-r--r--   0 runner    (1001) docker     (123)    13648 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_bilateral_approx_cpu.py
--rw-r--r--   0 runner    (1001) docker     (123)    13773 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_bilateral_approx_cuda.py
--rw-r--r--   0 runner    (1001) docker     (123)    15064 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_bilateral_precise.py
--rw-r--r--   0 runner    (1001) docker     (123)     2269 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_blend_images.py
--rw-r--r--   0 runner    (1001) docker     (123)     1818 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_border_pad.py
--rw-r--r--   0 runner    (1001) docker     (123)     1747 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_border_padd.py
--rw-r--r--   0 runner    (1001) docker     (123)     1812 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_bounding_rect.py
--rw-r--r--   0 runner    (1001) docker     (123)     1836 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_bounding_rectd.py
--rw-r--r--   0 runner    (1001) docker     (123)     1745 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_box_coder.py
--rw-r--r--   0 runner    (1001) docker     (123)    18036 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_box_transform.py
--rw-r--r--   0 runner    (1001) docker     (123)     8925 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_box_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     3313 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_bundle_ckpt_export.py
--rw-r--r--   0 runner    (1001) docker     (123)     7692 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_bundle_download.py
--rw-r--r--   0 runner    (1001) docker     (123)     2719 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_bundle_get_data.py
--rw-r--r--   0 runner    (1001) docker     (123)     1929 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_bundle_init_bundle.py
--rw-r--r--   0 runner    (1001) docker     (123)     2806 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_bundle_onnx_export.py
--rw-r--r--   0 runner    (1001) docker     (123)     6181 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_bundle_trt_export.py
--rw-r--r--   0 runner    (1001) docker     (123)     4170 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_bundle_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     2624 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_bundle_verify_metadata.py
--rw-r--r--   0 runner    (1001) docker     (123)     3326 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_bundle_verify_net.py
--rw-r--r--   0 runner    (1001) docker     (123)     6172 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_bundle_workflow.py
--rw-r--r--   0 runner    (1001) docker     (123)     9868 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_cachedataset.py
--rw-r--r--   0 runner    (1001) docker     (123)     2216 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_cachedataset_parallel.py
--rw-r--r--   0 runner    (1001) docker     (123)     1707 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_cachedataset_persistent_workers.py
--rw-r--r--   0 runner    (1001) docker     (123)     2453 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_cachentransdataset.py
--rw-r--r--   0 runner    (1001) docker     (123)     1126 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_call_dist.py
--rw-r--r--   0 runner    (1001) docker     (123)     2428 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_cast_to_type.py
--rw-r--r--   0 runner    (1001) docker     (123)     2602 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_cast_to_typed.py
--rw-r--r--   0 runner    (1001) docker     (123)     1918 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_center_scale_crop.py
--rw-r--r--   0 runner    (1001) docker     (123)     2064 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_center_scale_cropd.py
--rw-r--r--   0 runner    (1001) docker     (123)     1983 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_center_spatial_crop.py
--rw-r--r--   0 runner    (1001) docker     (123)     2045 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_center_spatial_cropd.py
--rw-r--r--   0 runner    (1001) docker     (123)     1671 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_channel_pad.py
--rw-r--r--   0 runner    (1001) docker     (123)     1760 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_check_hash.py
--rw-r--r--   0 runner    (1001) docker     (123)     2493 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_check_missing_files.py
--rw-r--r--   0 runner    (1001) docker     (123)     2914 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_classes_to_indices.py
--rw-r--r--   0 runner    (1001) docker     (123)     3604 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_classes_to_indicesd.py
--rw-r--r--   0 runner    (1001) docker     (123)     2669 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_complex_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     1506 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_component_locator.py
--rw-r--r--   0 runner    (1001) docker     (123)    25175 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_compose.py
--rw-r--r--   0 runner    (1001) docker     (123)     3915 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_compose_get_number_conversions.py
--rw-r--r--   0 runner    (1001) docker     (123)    10091 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_compute_confusion_matrix.py
--rw-r--r--   0 runner    (1001) docker     (123)     3458 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_compute_f_beta.py
--rw-r--r--   0 runner    (1001) docker     (123)     4519 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_compute_froc.py
--rw-r--r--   0 runner    (1001) docker     (123)     6021 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_compute_generalized_dice.py
--rw-r--r--   0 runner    (1001) docker     (123)     2528 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_compute_ho_ver_maps.py
--rw-r--r--   0 runner    (1001) docker     (123)     2829 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_compute_ho_ver_maps_d.py
--rw-r--r--   0 runner    (1001) docker     (123)     8892 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_compute_meandice.py
--rw-r--r--   0 runner    (1001) docker     (123)     8044 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_compute_meaniou.py
--rw-r--r--   0 runner    (1001) docker     (123)     5106 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_compute_panoptic_quality.py
--rw-r--r--   0 runner    (1001) docker     (123)     8066 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_compute_regression_metrics.py
--rw-r--r--   0 runner    (1001) docker     (123)     4578 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_compute_roc_auc.py
--rw-r--r--   0 runner    (1001) docker     (123)     4902 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_compute_variance.py
--rw-r--r--   0 runner    (1001) docker     (123)     3804 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_concat_itemsd.py
--rw-r--r--   0 runner    (1001) docker     (123)     5814 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_config_item.py
--rw-r--r--   0 runner    (1001) docker     (123)    14667 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_config_parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     2947 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_contrastive_loss.py
--rw-r--r--   0 runner    (1001) docker     (123)     6124 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_convert_data_type.py
--rw-r--r--   0 runner    (1001) docker     (123)     1949 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_convert_to_multi_channel.py
--rw-r--r--   0 runner    (1001) docker     (123)     1321 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_convert_to_multi_channeld.py
--rw-r--r--   0 runner    (1001) docker     (123)     4283 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_convert_to_onnx.py
--rw-r--r--   0 runner    (1001) docker     (123)     1635 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_convert_to_torchscript.py
--rw-r--r--   0 runner    (1001) docker     (123)     2567 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_convert_to_trt.py
--rw-r--r--   0 runner    (1001) docker     (123)     7134 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_convolutions.py
--rw-r--r--   0 runner    (1001) docker     (123)     3810 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_copy_itemsd.py
--rw-r--r--   0 runner    (1001) docker     (123)     6761 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_copy_model_state.py
--rw-r--r--   0 runner    (1001) docker     (123)     1388 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_correct_crop_centers.py
--rw-r--r--   0 runner    (1001) docker     (123)     2173 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_create_cross_validation_datalist.py
--rw-r--r--   0 runner    (1001) docker     (123)    10466 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_create_grid_and_affine.py
--rw-r--r--   0 runner    (1001) docker     (123)    18866 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_crf_cpu.py
--rw-r--r--   0 runner    (1001) docker     (123)    19445 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_crf_cuda.py
--rw-r--r--   0 runner    (1001) docker     (123)     6724 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_crop_foreground.py
--rw-r--r--   0 runner    (1001) docker     (123)     7621 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_crop_foregroundd.py
--rw-r--r--   0 runner    (1001) docker     (123)     2925 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_cross_validation.py
--rw-r--r--   0 runner    (1001) docker     (123)     8682 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_csv_dataset.py
--rw-r--r--   0 runner    (1001) docker     (123)    11089 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_csv_iterable_dataset.py
--rw-r--r--   0 runner    (1001) docker     (123)     1651 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_csv_saver.py
--rw-r--r--   0 runner    (1001) docker     (123)     5627 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_cucim_dict_transform.py
--rw-r--r--   0 runner    (1001) docker     (123)     5460 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_cucim_transform.py
--rw-r--r--   0 runner    (1001) docker     (123)     1922 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_cumulative.py
--rw-r--r--   0 runner    (1001) docker     (123)     2369 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_cumulative_average.py
--rw-r--r--   0 runner    (1001) docker     (123)     1761 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_cumulative_average_dist.py
--rw-r--r--   0 runner    (1001) docker     (123)     1984 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_cv2_dist.py
--rw-r--r--   0 runner    (1001) docker     (123)     2326 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_daf3d.py
--rw-r--r--   0 runner    (1001) docker     (123)     5532 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_data_stats.py
--rw-r--r--   0 runner    (1001) docker     (123)     5935 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_data_statsd.py
--rw-r--r--   0 runner    (1001) docker     (123)     4034 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_dataloader.py
--rw-r--r--   0 runner    (1001) docker     (123)     4461 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_dataset.py
--rw-r--r--   0 runner    (1001) docker     (123)     2271 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_dataset_func.py
--rw-r--r--   0 runner    (1001) docker     (123)     4651 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_dataset_summary.py
--rw-r--r--   0 runner    (1001) docker     (123)     3851 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_decathlondataset.py
--rw-r--r--   0 runner    (1001) docker     (123)    10471 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_decollate.py
--rw-r--r--   0 runner    (1001) docker     (123)     4579 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_deepedit_interaction.py
--rw-r--r--   0 runner    (1001) docker     (123)    10621 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_deepedit_transforms.py
--rw-r--r--   0 runner    (1001) docker     (123)     3959 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_deepgrow_dataset.py
--rw-r--r--   0 runner    (1001) docker     (123)     3721 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_deepgrow_interaction.py
--rw-r--r--   0 runner    (1001) docker     (123)    16313 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_deepgrow_transforms.py
--rw-r--r--   0 runner    (1001) docker     (123)     2239 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_delete_itemsd.py
--rw-r--r--   0 runner    (1001) docker     (123)     4368 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_denseblock.py
--rw-r--r--   0 runner    (1001) docker     (123)     4434 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_densenet.py
--rw-r--r--   0 runner    (1001) docker     (123)    14747 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_deprecated.py
--rw-r--r--   0 runner    (1001) docker     (123)     6294 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_detect_envelope.py
--rw-r--r--   0 runner    (1001) docker     (123)     2850 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_detection_coco_metrics.py
--rw-r--r--   0 runner    (1001) docker     (123)     2292 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_detector_boxselector.py
--rw-r--r--   0 runner    (1001) docker     (123)     2996 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_detector_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     1568 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_dev_collate.py
--rw-r--r--   0 runner    (1001) docker     (123)     4029 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_dice_ce_loss.py
--rw-r--r--   0 runner    (1001) docker     (123)     3626 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_dice_focal_loss.py
--rw-r--r--   0 runner    (1001) docker     (123)     8106 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_dice_loss.py
--rw-r--r--   0 runner    (1001) docker     (123)     3175 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_dints_cell.py
--rw-r--r--   0 runner    (1001) docker     (123)     2724 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_dints_mixop.py
--rw-r--r--   0 runner    (1001) docker     (123)     5780 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_dints_network.py
--rw-r--r--   0 runner    (1001) docker     (123)     1911 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_discriminator.py
--rw-r--r--   0 runner    (1001) docker     (123)     1764 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_divisible_pad.py
--rw-r--r--   0 runner    (1001) docker     (123)     1497 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_divisible_padd.py
--rw-r--r--   0 runner    (1001) docker     (123)     2936 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_download_and_extract.py
--rw-r--r--   0 runner    (1001) docker     (123)     1626 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_download_url_yandex.py
--rw-r--r--   0 runner    (1001) docker     (123)     1793 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_downsample_block.py
--rw-r--r--   0 runner    (1001) docker     (123)     1511 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_drop_path.py
--rw-r--r--   0 runner    (1001) docker     (123)     7026 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_ds_loss.py
--rw-r--r--   0 runner    (1001) docker     (123)     2390 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_dvf2ddf.py
--rw-r--r--   0 runner    (1001) docker     (123)     7235 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_dynunet.py
--rw-r--r--   0 runner    (1001) docker     (123)     4989 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_dynunet_block.py
--rw-r--r--   0 runner    (1001) docker     (123)    13331 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_efficientnet.py
--rw-r--r--   0 runner    (1001) docker     (123)     3142 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_ensemble_evaluator.py
--rw-r--r--   0 runner    (1001) docker     (123)     4434 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_ensure_channel_first.py
--rw-r--r--   0 runner    (1001) docker     (123)     3360 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_ensure_channel_firstd.py
--rw-r--r--   0 runner    (1001) docker     (123)     1789 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_ensure_tuple.py
--rw-r--r--   0 runner    (1001) docker     (123)     4575 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_ensure_type.py
--rw-r--r--   0 runner    (1001) docker     (123)     4873 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_ensure_typed.py
--rw-r--r--   0 runner    (1001) docker     (123)     3223 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_enum_bound_interp.py
--rw-r--r--   0 runner    (1001) docker     (123)     1085 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_eval_mode.py
--rw-r--r--   0 runner    (1001) docker     (123)     1846 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_evenly_divisible_all_gather_dist.py
--rw-r--r--   0 runner    (1001) docker     (123)     1305 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_factorized_increase.py
--rw-r--r--   0 runner    (1001) docker     (123)     1304 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_factorized_reduce.py
--rw-r--r--   0 runner    (1001) docker     (123)     2402 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_fastmri_reader.py
--rw-r--r--   0 runner    (1001) docker     (123)     2316 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_fft_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     2573 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_fg_bg_to_indices.py
--rw-r--r--   0 runner    (1001) docker     (123)     2786 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_fg_bg_to_indicesd.py
--rw-r--r--   0 runner    (1001) docker     (123)     3857 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_file_basename.py
--rw-r--r--   0 runner    (1001) docker     (123)     5804 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_fill_holes.py
--rw-r--r--   0 runner    (1001) docker     (123)     5903 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_fill_holesd.py
--rw-r--r--   0 runner    (1001) docker     (123)     2566 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_fl_exchange_object.py
--rw-r--r--   0 runner    (1001) docker     (123)     8696 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_fl_monai_algo.py
--rw-r--r--   0 runner    (1001) docker     (123)     4994 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_fl_monai_algo_dist.py
--rw-r--r--   0 runner    (1001) docker     (123)     2867 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_fl_monai_algo_stats.py
--rw-r--r--   0 runner    (1001) docker     (123)     2392 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_flatten_sub_keysd.py
--rw-r--r--   0 runner    (1001) docker     (123)    13497 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_flexible_unet.py
--rw-r--r--   0 runner    (1001) docker     (123)     3087 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_flip.py
--rw-r--r--   0 runner    (1001) docker     (123)     3556 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_flipd.py
--rw-r--r--   0 runner    (1001) docker     (123)    17277 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_focal_loss.py
--rw-r--r--   0 runner    (1001) docker     (123)     3152 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_folder_layout.py
--rw-r--r--   0 runner    (1001) docker     (123)     4155 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_foreground_mask.py
--rw-r--r--   0 runner    (1001) docker     (123)     4813 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_foreground_maskd.py
--rw-r--r--   0 runner    (1001) docker     (123)     2332 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_fourier.py
--rw-r--r--   0 runner    (1001) docker     (123)     3462 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_fpn_block.py
--rw-r--r--   0 runner    (1001) docker     (123)     1342 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_from_engine_hovernet.py
--rw-r--r--   0 runner    (1001) docker     (123)     2173 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_fullyconnectednet.py
--rw-r--r--   0 runner    (1001) docker     (123)     9063 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_gaussian.py
--rw-r--r--   0 runner    (1001) docker     (123)     8085 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_gaussian_filter.py
--rw-r--r--   0 runner    (1001) docker     (123)     3090 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_gaussian_sharpen.py
--rw-r--r--   0 runner    (1001) docker     (123)     3231 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_gaussian_sharpend.py
--rw-r--r--   0 runner    (1001) docker     (123)     3146 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_gaussian_smooth.py
--rw-r--r--   0 runner    (1001) docker     (123)     3286 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_gaussian_smoothd.py
--rw-r--r--   0 runner    (1001) docker     (123)     3517 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_generalized_dice_focal_loss.py
--rw-r--r--   0 runner    (1001) docker     (123)     8036 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_generalized_dice_loss.py
--rw-r--r--   0 runner    (1001) docker     (123)     9727 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_generalized_wasserstein_dice_loss.py
--rw-r--r--   0 runner    (1001) docker     (123)     1924 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_generate_distance_map.py
--rw-r--r--   0 runner    (1001) docker     (123)     2330 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_generate_distance_mapd.py
--rw-r--r--   0 runner    (1001) docker     (123)     2016 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_generate_instance_border.py
--rw-r--r--   0 runner    (1001) docker     (123)     2251 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_generate_instance_borderd.py
--rw-r--r--   0 runner    (1001) docker     (123)     1981 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_generate_instance_centroid.py
--rw-r--r--   0 runner    (1001) docker     (123)     2139 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_generate_instance_centroidd.py
--rw-r--r--   0 runner    (1001) docker     (123)     2199 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_generate_instance_contour.py
--rw-r--r--   0 runner    (1001) docker     (123)     2358 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_generate_instance_contourd.py
--rw-r--r--   0 runner    (1001) docker     (123)     1663 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_generate_instance_type.py
--rw-r--r--   0 runner    (1001) docker     (123)     1853 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_generate_instance_typed.py
--rw-r--r--   0 runner    (1001) docker     (123)     2315 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_generate_label_classes_crop_centers.py
--rw-r--r--   0 runner    (1001) docker     (123)     3365 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_generate_param_groups.py
--rw-r--r--   0 runner    (1001) docker     (123)     2511 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_generate_pos_neg_label_crop_centers.py
--rw-r--r--   0 runner    (1001) docker     (123)     3505 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_generate_spatial_bounding_box.py
--rw-r--r--   0 runner    (1001) docker     (123)     1944 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_generate_succinct_contour.py
--rw-r--r--   0 runner    (1001) docker     (123)     2037 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_generate_succinct_contourd.py
--rw-r--r--   0 runner    (1001) docker     (123)     2052 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_generate_watershed_markers.py
--rw-r--r--   0 runner    (1001) docker     (123)     2830 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_generate_watershed_markersd.py
--rw-r--r--   0 runner    (1001) docker     (123)     2564 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_generate_watershed_mask.py
--rw-r--r--   0 runner    (1001) docker     (123)     2722 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_generate_watershed_maskd.py
--rw-r--r--   0 runner    (1001) docker     (123)     1984 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_generator.py
--rw-r--r--   0 runner    (1001) docker     (123)     2282 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_get_equivalent_dtype.py
--rw-r--r--   0 runner    (1001) docker     (123)     1695 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_get_extreme_points.py
--rw-r--r--   0 runner    (1001) docker     (123)     2207 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_get_layers.py
--rw-r--r--   0 runner    (1001) docker     (123)     1123 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_get_package_version.py
--rw-r--r--   0 runner    (1001) docker     (123)     1681 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_get_unique_labels.py
--rw-r--r--   0 runner    (1001) docker     (123)     2647 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_gibbs_noise.py
--rw-r--r--   0 runner    (1001) docker     (123)     3223 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_gibbs_noised.py
--rw-r--r--   0 runner    (1001) docker     (123)     2016 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_giou_loss.py
--rw-r--r--   0 runner    (1001) docker     (123)     5465 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_global_mutual_information_loss.py
--rw-r--r--   0 runner    (1001) docker     (123)     3796 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_globalnet.py
--rw-r--r--   0 runner    (1001) docker     (123)     9431 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_gmm.py
--rw-r--r--   0 runner    (1001) docker     (123)     8683 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_grid_dataset.py
--rw-r--r--   0 runner    (1001) docker     (123)     4467 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_grid_distortion.py
--rw-r--r--   0 runner    (1001) docker     (123)     3487 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_grid_distortiond.py
--rw-r--r--   0 runner    (1001) docker     (123)     5948 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_grid_patch.py
--rw-r--r--   0 runner    (1001) docker     (123)     4737 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_grid_patchd.py
--rw-r--r--   0 runner    (1001) docker     (123)     3924 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_grid_pull.py
--rw-r--r--   0 runner    (1001) docker     (123)     3422 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_grid_split.py
--rw-r--r--   0 runner    (1001) docker     (123)     4059 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_grid_splitd.py
--rw-r--r--   0 runner    (1001) docker     (123)     8438 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_checkpoint_loader.py
--rw-r--r--   0 runner    (1001) docker     (123)     6255 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_checkpoint_saver.py
--rw-r--r--   0 runner    (1001) docker     (123)     2354 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_classification_saver.py
--rw-r--r--   0 runner    (1001) docker     (123)     2776 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_classification_saver_dist.py
--rw-r--r--   0 runner    (1001) docker     (123)     2602 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_clearml_image.py
--rw-r--r--   0 runner    (1001) docker     (123)     2602 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_clearml_stats.py
--rw-r--r--   0 runner    (1001) docker     (123)     3911 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_confusion_matrix.py
--rw-r--r--   0 runner    (1001) docker     (123)     2542 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_confusion_matrix_dist.py
--rw-r--r--   0 runner    (1001) docker     (123)     2477 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_decollate_batch.py
--rw-r--r--   0 runner    (1001) docker     (123)     2154 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_early_stop.py
--rw-r--r--   0 runner    (1001) docker     (123)     2829 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_garbage_collector.py
--rw-r--r--   0 runner    (1001) docker     (123)     3879 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_hausdorff_distance.py
--rw-r--r--   0 runner    (1001) docker     (123)     7368 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_ignite_metric.py
--rw-r--r--   0 runner    (1001) docker     (123)     2555 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_logfile.py
--rw-r--r--   0 runner    (1001) docker     (123)     3335 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_lr_scheduler.py
--rw-r--r--   0 runner    (1001) docker     (123)     4182 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_mean_dice.py
--rw-r--r--   0 runner    (1001) docker     (123)     3018 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_mean_iou.py
--rw-r--r--   0 runner    (1001) docker     (123)     1920 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_metric_logger.py
--rw-r--r--   0 runner    (1001) docker     (123)     5833 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_metrics_reloaded.py
--rw-r--r--   0 runner    (1001) docker     (123)     3835 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_metrics_saver.py
--rw-r--r--   0 runner    (1001) docker     (123)     4975 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_metrics_saver_dist.py
--rw-r--r--   0 runner    (1001) docker     (123)     8663 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_mlflow.py
--rw-r--r--   0 runner    (1001) docker     (123)     3820 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_nvtx.py
--rw-r--r--   0 runner    (1001) docker     (123)     3142 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_panoptic_quality.py
--rw-r--r--   0 runner    (1001) docker     (123)     4887 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_parameter_scheduler.py
--rw-r--r--   0 runner    (1001) docker     (123)     2872 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_post_processing.py
--rw-r--r--   0 runner    (1001) docker     (123)     3694 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_prob_map_producer.py
--rw-r--r--   0 runner    (1001) docker     (123)     6691 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_regression_metrics.py
--rw-r--r--   0 runner    (1001) docker     (123)     8660 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_regression_metrics_dist.py
--rw-r--r--   0 runner    (1001) docker     (123)     1553 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_rocauc.py
--rw-r--r--   0 runner    (1001) docker     (123)     2005 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_rocauc_dist.py
--rw-r--r--   0 runner    (1001) docker     (123)     1641 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_smartcache.py
--rw-r--r--   0 runner    (1001) docker     (123)     9501 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_stats.py
--rw-r--r--   0 runner    (1001) docker     (123)     4001 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_surface_distance.py
--rw-r--r--   0 runner    (1001) docker     (123)     2246 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_tb_image.py
--rw-r--r--   0 runner    (1001) docker     (123)     6731 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_tb_stats.py
--rw-r--r--   0 runner    (1001) docker     (123)     1575 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_handler_validation.py
--rw-r--r--   0 runner    (1001) docker     (123)     2069 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_hardnegsampler.py
--rw-r--r--   0 runner    (1001) docker     (123)     1752 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_hashing.py
--rw-r--r--   0 runner    (1001) docker     (123)     6766 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_hausdorff_distance.py
--rw-r--r--   0 runner    (1001) docker     (123)     1576 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_header_correct.py
--rw-r--r--   0 runner    (1001) docker     (123)     2283 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_highresnet.py
--rw-r--r--   0 runner    (1001) docker     (123)     7425 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_hilbert_transform.py
--rw-r--r--   0 runner    (1001) docker     (123)     1965 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_histogram_normalize.py
--rw-r--r--   0 runner    (1001) docker     (123)     2070 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_histogram_normalized.py
--rw-r--r--   0 runner    (1001) docker     (123)     7968 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_hovernet.py
--rw-r--r--   0 runner    (1001) docker     (123)     2545 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_hovernet_instance_map_post_processing.py
--rw-r--r--   0 runner    (1001) docker     (123)     2794 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_hovernet_instance_map_post_processingd.py
--rw-r--r--   0 runner    (1001) docker     (123)     6766 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_hovernet_loss.py
--rw-r--r--   0 runner    (1001) docker     (123)     2549 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_hovernet_nuclear_type_post_processing.py
--rw-r--r--   0 runner    (1001) docker     (123)     2656 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_hovernet_nuclear_type_post_processingd.py
--rw-r--r--   0 runner    (1001) docker     (123)     1022 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_identity.py
--rw-r--r--   0 runner    (1001) docker     (123)     1087 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_identityd.py
--rw-r--r--   0 runner    (1001) docker     (123)     7196 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_image_dataset.py
--rw-r--r--   0 runner    (1001) docker     (123)    10444 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_image_filter.py
--rw-r--r--   0 runner    (1001) docker     (123)     8414 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_image_rw.py
--rw-r--r--   0 runner    (1001) docker     (123)     1762 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_img2tensorboard.py
--rw-r--r--   0 runner    (1001) docker     (123)     2225 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_init_reader.py
--rw-r--r--   0 runner    (1001) docker     (123)     7566 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_integration_autorunner.py
--rw-r--r--   0 runner    (1001) docker     (123)     7311 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_integration_bundle_run.py
--rw-r--r--   0 runner    (1001) docker     (123)    11343 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_integration_classification_2d.py
--rw-r--r--   0 runner    (1001) docker     (123)     3167 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_integration_determinism.py
--rw-r--r--   0 runner    (1001) docker     (123)     9737 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_integration_fast_train.py
--rw-r--r--   0 runner    (1001) docker     (123)     5542 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_integration_gpu_customization.py
--rw-r--r--   0 runner    (1001) docker     (123)     9193 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_integration_lazy_samples.py
--rw-r--r--   0 runner    (1001) docker     (123)     4327 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_integration_nnunetv2_runner.py
--rw-r--r--   0 runner    (1001) docker     (123)    13199 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_integration_segmentation_3d.py
--rw-r--r--   0 runner    (1001) docker     (123)     3878 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_integration_sliding_window.py
--rw-r--r--   0 runner    (1001) docker     (123)     4941 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_integration_stn.py
--rw-r--r--   0 runner    (1001) docker     (123)     2356 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_integration_unet_2d.py
--rw-r--r--   0 runner    (1001) docker     (123)     2190 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_integration_workers.py
--rw-r--r--   0 runner    (1001) docker     (123)    14051 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_integration_workflows.py
--rw-r--r--   0 runner    (1001) docker     (123)     5491 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_integration_workflows_gan.py
--rw-r--r--   0 runner    (1001) docker     (123)     2790 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_intensity_stats.py
--rw-r--r--   0 runner    (1001) docker     (123)     3594 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_intensity_statsd.py
--rw-r--r--   0 runner    (1001) docker     (123)    18993 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_inverse.py
--rw-r--r--   0 runner    (1001) docker     (123)     2764 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_inverse_array.py
--rw-r--r--   0 runner    (1001) docker     (123)     5452 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_inverse_collation.py
--rw-r--r--   0 runner    (1001) docker     (123)     4287 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_invert.py
--rw-r--r--   0 runner    (1001) docker     (123)     6090 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_invertd.py
--rw-r--r--   0 runner    (1001) docker     (123)     1675 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_is_supported_format.py
--rw-r--r--   0 runner    (1001) docker     (123)     2344 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_iterable_dataset.py
--rw-r--r--   0 runner    (1001) docker     (123)    18618 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_itk_torch_bridge.py
--rw-r--r--   0 runner    (1001) docker     (123)     2621 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_itk_writer.py
--rw-r--r--   0 runner    (1001) docker     (123)     2858 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_k_space_spike_noise.py
--rw-r--r--   0 runner    (1001) docker     (123)     3506 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_k_space_spike_noised.py
--rw-r--r--   0 runner    (1001) docker     (123)    14754 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_keep_largest_connected_component.py
--rw-r--r--   0 runner    (1001) docker     (123)    12548 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_keep_largest_connected_componentd.py
--rw-r--r--   0 runner    (1001) docker     (123)     1815 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_kspace_mask.py
--rw-r--r--   0 runner    (1001) docker     (123)     2503 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_label_filter.py
--rw-r--r--   0 runner    (1001) docker     (123)     2592 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_label_filterd.py
--rw-r--r--   0 runner    (1001) docker     (123)     4982 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_label_quality_score.py
--rw-r--r--   0 runner    (1001) docker     (123)     6767 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_label_to_contour.py
--rw-r--r--   0 runner    (1001) docker     (123)     6963 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_label_to_contourd.py
--rw-r--r--   0 runner    (1001) docker     (123)     2488 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_label_to_mask.py
--rw-r--r--   0 runner    (1001) docker     (123)     2642 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_label_to_maskd.py
--rw-r--r--   0 runner    (1001) docker     (123)     2354 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_lambda.py
--rw-r--r--   0 runner    (1001) docker     (123)     3122 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_lambdad.py
--rw-r--r--   0 runner    (1001) docker     (123)     9763 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_lesion_froc.py
--rw-r--r--   0 runner    (1001) docker     (123)     2167 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_list_data_collate.py
--rw-r--r--   0 runner    (1001) docker     (123)     1552 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_list_to_dict.py
--rw-r--r--   0 runner    (1001) docker     (123)     2347 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_lltm.py
--rw-r--r--   0 runner    (1001) docker     (123)     8929 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_lmdbdataset.py
--rw-r--r--   0 runner    (1001) docker     (123)     2530 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_lmdbdataset_dist.py
--rw-r--r--   0 runner    (1001) docker     (123)     6475 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_load_decathlon_datalist.py
--rw-r--r--   0 runner    (1001) docker     (123)    15192 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_load_image.py
--rw-r--r--   0 runner    (1001) docker     (123)     8802 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_load_imaged.py
--rw-r--r--   0 runner    (1001) docker     (123)     6235 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_load_spacing_orientation.py
--rw-r--r--   0 runner    (1001) docker     (123)     1194 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_loader_semaphore.py
--rw-r--r--   0 runner    (1001) docker     (123)     6069 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_local_normalized_cross_correlation_loss.py
--rw-r--r--   0 runner    (1001) docker     (123)     2834 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_localnet.py
--rw-r--r--   0 runner    (1001) docker     (123)     4803 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_localnet_block.py
--rw-r--r--   0 runner    (1001) docker     (123)     2997 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_look_up_option.py
--rw-r--r--   0 runner    (1001) docker     (123)     2105 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_loss_metric.py
--rw-r--r--   0 runner    (1001) docker     (123)     3683 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_lr_finder.py
--rw-r--r--   0 runner    (1001) docker     (123)     2569 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_lr_scheduler.py
--rw-r--r--   0 runner    (1001) docker     (123)     1498 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_make_nifti.py
--rw-r--r--   0 runner    (1001) docker     (123)     2468 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_map_binary_to_indices.py
--rw-r--r--   0 runner    (1001) docker     (123)     4331 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_map_classes_to_indices.py
--rw-r--r--   0 runner    (1001) docker     (123)     3017 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_map_label_value.py
--rw-r--r--   0 runner    (1001) docker     (123)     2539 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_map_label_valued.py
--rw-r--r--   0 runner    (1001) docker     (123)     1390 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_map_transform.py
--rw-r--r--   0 runner    (1001) docker     (123)     3087 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_mask_intensity.py
--rw-r--r--   0 runner    (1001) docker     (123)     2705 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_mask_intensityd.py
--rw-r--r--   0 runner    (1001) docker     (123)     6303 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_masked_dice_loss.py
--rw-r--r--   0 runner    (1001) docker     (123)     3288 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_masked_loss.py
--rw-r--r--   0 runner    (1001) docker     (123)     4408 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_masked_patch_wsi_dataset.py
--rw-r--r--   0 runner    (1001) docker     (123)     4879 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_matshow3d.py
--rw-r--r--   0 runner    (1001) docker     (123)     2748 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_mean_ensemble.py
--rw-r--r--   0 runner    (1001) docker     (123)     3369 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_mean_ensembled.py
--rw-r--r--   0 runner    (1001) docker     (123)     1957 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_median_filter.py
--rw-r--r--   0 runner    (1001) docker     (123)     1372 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_median_smooth.py
--rw-r--r--   0 runner    (1001) docker     (123)     2248 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_median_smoothd.py
--rw-r--r--   0 runner    (1001) docker     (123)     3050 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_mednistdataset.py
--rw-r--r--   0 runner    (1001) docker     (123)     7458 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_meta_affine.py
--rw-r--r--   0 runner    (1001) docker     (123)    23538 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_meta_tensor.py
--rw-r--r--   0 runner    (1001) docker     (123)     5452 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_metatensor_integration.py
--rw-r--r--   0 runner    (1001) docker     (123)     4653 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_metrics_reloaded.py
--rw-r--r--   0 runner    (1001) docker     (123)     3228 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_milmodel.py
--rw-r--r--   0 runner    (1001) docker     (123)     1713 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_mlp.py
--rw-r--r--   0 runner    (1001) docker     (123)     6340 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_mmar_download.py
--rw-r--r--   0 runner    (1001) docker     (123)     3132 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_module_list.py
--rw-r--r--   0 runner    (1001) docker     (123)     1475 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_monai_env_vars.py
--rw-r--r--   0 runner    (1001) docker     (123)     3759 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_monai_utils_misc.py
--rw-r--r--   0 runner    (1001) docker     (123)     1220 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_mri_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     3005 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_multi_scale.py
--rw-r--r--   0 runner    (1001) docker     (123)     2636 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_net_adapter.py
--rw-r--r--   0 runner    (1001) docker     (123)     2820 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_network_consistency.py
--rw-r--r--   0 runner    (1001) docker     (123)     4036 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_nifti_endianness.py
--rw-r--r--   0 runner    (1001) docker     (123)     1528 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_nifti_header_revise.py
--rw-r--r--   0 runner    (1001) docker     (123)    12065 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_nifti_rw.py
--rw-r--r--   0 runner    (1001) docker     (123)     4999 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_normalize_intensity.py
--rw-r--r--   0 runner    (1001) docker     (123)     3058 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_normalize_intensityd.py
--rw-r--r--   0 runner    (1001) docker     (123)     1833 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_npzdictitemdataset.py
--rw-r--r--   0 runner    (1001) docker     (123)     6066 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_nrrd_reader.py
--rw-r--r--   0 runner    (1001) docker     (123)     9614 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_nuclick_transforms.py
--rw-r--r--   0 runner    (1001) docker     (123)     5716 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_numpy_reader.py
--rw-r--r--   0 runner    (1001) docker     (123)    10570 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_nvtx_decorator.py
--rw-r--r--   0 runner    (1001) docker     (123)     5139 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_nvtx_transform.py
--rw-r--r--   0 runner    (1001) docker     (123)     4422 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_occlusion_sensitivity.py
--rw-r--r--   0 runner    (1001) docker     (123)     8860 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_one_of.py
--rw-r--r--   0 runner    (1001) docker     (123)     3694 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_optim_novograd.py
--rw-r--r--   0 runner    (1001) docker     (123)     3309 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_optional_import.py
--rw-r--r--   0 runner    (1001) docker     (123)     1851 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_ori_ras_lps.py
--rw-r--r--   0 runner    (1001) docker     (123)     8125 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_orientation.py
--rw-r--r--   0 runner    (1001) docker     (123)     4228 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_orientationd.py
--rw-r--r--   0 runner    (1001) docker     (123)     2371 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_p3d_block.py
--rw-r--r--   0 runner    (1001) docker     (123)     4626 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_pad_collation.py
--rw-r--r--   0 runner    (1001) docker     (123)     1610 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_pad_mode.py
--rw-r--r--   0 runner    (1001) docker     (123)     2197 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_parallel_execution.py
--rw-r--r--   0 runner    (1001) docker     (123)     1610 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_parallel_execution_dist.py
--rw-r--r--   0 runner    (1001) docker     (123)     2939 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_partition_dataset.py
--rw-r--r--   0 runner    (1001) docker     (123)     2587 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_partition_dataset_classes.py
--rw-r--r--   0 runner    (1001) docker     (123)     3219 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_patch_dataset.py
--rw-r--r--   0 runner    (1001) docker     (123)     9875 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_patch_inferer.py
--rw-r--r--   0 runner    (1001) docker     (123)     8349 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_patch_wsi_dataset.py
--rw-r--r--   0 runner    (1001) docker     (123)     6344 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_patchembedding.py
--rw-r--r--   0 runner    (1001) docker     (123)    10327 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_pathology_he_stain.py
--rw-r--r--   0 runner    (1001) docker     (123)    10277 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_pathology_he_stain_dict.py
--rw-r--r--   0 runner    (1001) docker     (123)     1766 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_pathology_prob_nms.py
--rw-r--r--   0 runner    (1001) docker     (123)     8109 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_persistentdataset.py
--rw-r--r--   0 runner    (1001) docker     (123)     3055 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_persistentdataset_dist.py
--rw-r--r--   0 runner    (1001) docker     (123)     9041 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_phl_cpu.py
--rw-r--r--   0 runner    (1001) docker     (123)     4842 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_phl_cuda.py
--rw-r--r--   0 runner    (1001) docker     (123)     3684 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_pil_reader.py
--rw-r--r--   0 runner    (1001) docker     (123)     2730 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_plot_2d_or_3d_image.py
--rw-r--r--   0 runner    (1001) docker     (123)     4324 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_png_rw.py
--rw-r--r--   0 runner    (1001) docker     (123)     1993 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_polyval.py
--rw-r--r--   0 runner    (1001) docker     (123)     3697 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_prepare_batch_default.py
--rw-r--r--   0 runner    (1001) docker     (123)     2479 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_prepare_batch_default_dist.py
--rw-r--r--   0 runner    (1001) docker     (123)     2745 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_prepare_batch_extra_input.py
--rw-r--r--   0 runner    (1001) docker     (123)     2466 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_prepare_batch_hovernet.py
--rw-r--r--   0 runner    (1001) docker     (123)     4070 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_preset_filters.py
--rw-r--r--   0 runner    (1001) docker     (123)      818 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_print_info.py
--rw-r--r--   0 runner    (1001) docker     (123)     1049 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_print_transform_backends.py
--rw-r--r--   0 runner    (1001) docker     (123)     2861 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_probnms.py
--rw-r--r--   0 runner    (1001) docker     (123)     3065 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_probnmsd.py
--rw-r--r--   0 runner    (1001) docker     (123)     6606 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_profiling.py
--rw-r--r--   0 runner    (1001) docker     (123)     1599 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_pytorch_version_after.py
--rw-r--r--   0 runner    (1001) docker     (123)      988 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_query_memory.py
--rw-r--r--   0 runner    (1001) docker     (123)     2596 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_quicknat.py
--rw-r--r--   0 runner    (1001) docker     (123)     1582 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_adjust_contrast.py
--rw-r--r--   0 runner    (1001) docker     (123)     1600 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_adjust_contrastd.py
--rw-r--r--   0 runner    (1001) docker     (123)     7254 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_affine.py
--rw-r--r--   0 runner    (1001) docker     (123)     9724 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_affine_grid.py
--rw-r--r--   0 runner    (1001) docker     (123)    10949 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_affined.py
--rw-r--r--   0 runner    (1001) docker     (123)     1836 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_axis_flip.py
--rw-r--r--   0 runner    (1001) docker     (123)     1927 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_axis_flipd.py
--rw-r--r--   0 runner    (1001) docker     (123)     2646 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_bias_field.py
--rw-r--r--   0 runner    (1001) docker     (123)     2439 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_bias_fieldd.py
--rw-r--r--   0 runner    (1001) docker     (123)     4178 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_coarse_dropout.py
--rw-r--r--   0 runner    (1001) docker     (123)     4077 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_coarse_dropoutd.py
--rw-r--r--   0 runner    (1001) docker     (123)     2279 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_coarse_shuffle.py
--rw-r--r--   0 runner    (1001) docker     (123)     2062 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_coarse_shuffled.py
--rw-r--r--   0 runner    (1001) docker     (123)     6393 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_crop_by_label_classes.py
--rw-r--r--   0 runner    (1001) docker     (123)     5846 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_crop_by_label_classesd.py
--rw-r--r--   0 runner    (1001) docker     (123)     5597 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_crop_by_pos_neg_label.py
--rw-r--r--   0 runner    (1001) docker     (123)     6605 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_crop_by_pos_neg_labeld.py
--rw-r--r--   0 runner    (1001) docker     (123)     6459 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_cucim_dict_transform.py
--rw-r--r--   0 runner    (1001) docker     (123)     6314 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_cucim_transform.py
--rw-r--r--   0 runner    (1001) docker     (123)     6339 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_deform_grid.py
--rw-r--r--   0 runner    (1001) docker     (123)     4596 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_elastic_2d.py
--rw-r--r--   0 runner    (1001) docker     (123)     3762 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_elastic_3d.py
--rw-r--r--   0 runner    (1001) docker     (123)     6681 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_elasticd_2d.py
--rw-r--r--   0 runner    (1001) docker     (123)     5867 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_elasticd_3d.py
--rw-r--r--   0 runner    (1001) docker     (123)     2342 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_flip.py
--rw-r--r--   0 runner    (1001) docker     (123)     2150 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_flipd.py
--rw-r--r--   0 runner    (1001) docker     (123)     1631 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_gaussian_noise.py
--rw-r--r--   0 runner    (1001) docker     (123)     1849 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_gaussian_noised.py
--rw-r--r--   0 runner    (1001) docker     (123)     4619 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_gaussian_sharpen.py
--rw-r--r--   0 runner    (1001) docker     (123)     4848 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_gaussian_sharpend.py
--rw-r--r--   0 runner    (1001) docker     (123)     3421 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_gaussian_smooth.py
--rw-r--r--   0 runner    (1001) docker     (123)     3500 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_gaussian_smoothd.py
--rw-r--r--   0 runner    (1001) docker     (123)     3391 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_gibbs_noise.py
--rw-r--r--   0 runner    (1001) docker     (123)     4090 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_gibbs_noised.py
--rw-r--r--   0 runner    (1001) docker     (123)     4092 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_grid_distortion.py
--rw-r--r--   0 runner    (1001) docker     (123)     3574 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_grid_distortiond.py
--rw-r--r--   0 runner    (1001) docker     (123)     5916 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_grid_patch.py
--rw-r--r--   0 runner    (1001) docker     (123)     4604 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_grid_patchd.py
--rw-r--r--   0 runner    (1001) docker     (123)     3363 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_histogram_shift.py
--rw-r--r--   0 runner    (1001) docker     (123)     2809 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_histogram_shiftd.py
--rw-r--r--   0 runner    (1001) docker     (123)     3486 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_k_space_spike_noise.py
--rw-r--r--   0 runner    (1001) docker     (123)     2598 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_k_space_spike_noised.py
--rw-r--r--   0 runner    (1001) docker     (123)     2980 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_lambda.py
--rw-r--r--   0 runner    (1001) docker     (123)     2801 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_lambdad.py
--rw-r--r--   0 runner    (1001) docker     (123)     1840 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_rician_noise.py
--rw-r--r--   0 runner    (1001) docker     (123)     1964 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_rician_noised.py
--rw-r--r--   0 runner    (1001) docker     (123)     5674 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_rotate.py
--rw-r--r--   0 runner    (1001) docker     (123)     4079 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_rotate90.py
--rw-r--r--   0 runner    (1001) docker     (123)     4347 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_rotate90d.py
--rw-r--r--   0 runner    (1001) docker     (123)     6332 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_rotated.py
--rw-r--r--   0 runner    (1001) docker     (123)     3106 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_scale_crop.py
--rw-r--r--   0 runner    (1001) docker     (123)     3527 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_scale_cropd.py
--rw-r--r--   0 runner    (1001) docker     (123)     1435 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_scale_intensity.py
--rw-r--r--   0 runner    (1001) docker     (123)     1489 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_scale_intensity_fixed_mean.py
--rw-r--r--   0 runner    (1001) docker     (123)     1542 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_scale_intensity_fixed_meand.py
--rw-r--r--   0 runner    (1001) docker     (123)     1416 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_scale_intensityd.py
--rw-r--r--   0 runner    (1001) docker     (123)     1398 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_shift_intensity.py
--rw-r--r--   0 runner    (1001) docker     (123)     2054 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_shift_intensityd.py
--rw-r--r--   0 runner    (1001) docker     (123)     4614 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_spatial_crop.py
--rw-r--r--   0 runner    (1001) docker     (123)     5315 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_spatial_crop_samples.py
--rw-r--r--   0 runner    (1001) docker     (123)     6243 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_spatial_crop_samplesd.py
--rw-r--r--   0 runner    (1001) docker     (123)     4877 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_spatial_cropd.py
--rw-r--r--   0 runner    (1001) docker     (123)     1599 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_std_shift_intensity.py
--rw-r--r--   0 runner    (1001) docker     (123)     1453 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_std_shift_intensityd.py
--rw-r--r--   0 runner    (1001) docker     (123)     6572 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_weighted_crop.py
--rw-r--r--   0 runner    (1001) docker     (123)     6553 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_weighted_cropd.py
--rw-r--r--   0 runner    (1001) docker     (123)     4391 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_zoom.py
--rw-r--r--   0 runner    (1001) docker     (123)     4265 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rand_zoomd.py
--rw-r--r--   0 runner    (1001) docker     (123)     1654 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_randidentity.py
--rw-r--r--   0 runner    (1001) docker     (123)     5182 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_random_order.py
--rw-r--r--   0 runner    (1001) docker     (123)     1565 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_randomizable.py
--rw-r--r--   0 runner    (1001) docker     (123)     1200 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_randomizable_transform_type.py
--rw-r--r--   0 runner    (1001) docker     (123)     2569 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_randtorchvisiond.py
--rw-r--r--   0 runner    (1001) docker     (123)     1673 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rankfilter_dist.py
--rw-r--r--   0 runner    (1001) docker     (123)     3179 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_recon_net_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     3150 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_reference_based_normalize_intensity.py
--rw-r--r--   0 runner    (1001) docker     (123)     1970 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_reference_based_spatial_cropd.py
--rw-r--r--   0 runner    (1001) docker     (123)     4239 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_reference_resolver.py
--rw-r--r--   0 runner    (1001) docker     (123)     3905 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_reg_loss_integration.py
--rw-r--r--   0 runner    (1001) docker     (123)     2806 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_regunet.py
--rw-r--r--   0 runner    (1001) docker     (123)     3458 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_regunet_block.py
--rw-r--r--   0 runner    (1001) docker     (123)     1212 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_remove_repeated_channel.py
--rw-r--r--   0 runner    (1001) docker     (123)     1424 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_remove_repeated_channeld.py
--rw-r--r--   0 runner    (1001) docker     (123)     3197 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_remove_small_objects.py
--rw-r--r--   0 runner    (1001) docker     (123)     1162 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_repeat_channel.py
--rw-r--r--   0 runner    (1001) docker     (123)     1328 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_repeat_channeld.py
--rw-r--r--   0 runner    (1001) docker     (123)     4345 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_replace_module.py
--rw-r--r--   0 runner    (1001) docker     (123)     2280 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_require_pkg.py
--rw-r--r--   0 runner    (1001) docker     (123)     1902 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_resample.py
--rw-r--r--   0 runner    (1001) docker     (123)     3173 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_resample_backends.py
--rw-r--r--   0 runner    (1001) docker     (123)     1441 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_resample_datalist.py
--rw-r--r--   0 runner    (1001) docker     (123)     4556 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_resample_to_match.py
--rw-r--r--   0 runner    (1001) docker     (123)     3607 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_resample_to_matchd.py
--rw-r--r--   0 runner    (1001) docker     (123)     7015 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_resampler.py
--rw-r--r--   0 runner    (1001) docker     (123)     5568 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_resize.py
--rw-r--r--   0 runner    (1001) docker     (123)     4203 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_resize_with_pad_or_crop.py
--rw-r--r--   0 runner    (1001) docker     (123)     3995 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_resize_with_pad_or_cropd.py
--rw-r--r--   0 runner    (1001) docker     (123)     6016 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_resized.py
--rw-r--r--   0 runner    (1001) docker     (123)     5475 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_resnet.py
--rw-r--r--   0 runner    (1001) docker     (123)     7415 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_retinanet.py
--rw-r--r--   0 runner    (1001) docker     (123)     7717 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_retinanet_detector.py
--rw-r--r--   0 runner    (1001) docker     (123)     4992 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_retinanet_predict_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     6739 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rotate.py
--rw-r--r--   0 runner    (1001) docker     (123)     8062 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rotate90.py
--rw-r--r--   0 runner    (1001) docker     (123)     4061 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rotate90d.py
--rw-r--r--   0 runner    (1001) docker     (123)     8360 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_rotated.py
--rw-r--r--   0 runner    (1001) docker     (123)     3958 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_safe_dtype_range.py
--rw-r--r--   0 runner    (1001) docker     (123)     1948 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_saliency_inferer.py
--rw-r--r--   0 runner    (1001) docker     (123)     1874 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_sample_slices.py
--rw-r--r--   0 runner    (1001) docker     (123)     3463 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_sampler_dist.py
--rw-r--r--   0 runner    (1001) docker     (123)     4137 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_save_classificationd.py
--rw-r--r--   0 runner    (1001) docker     (123)     2323 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_save_image.py
--rw-r--r--   0 runner    (1001) docker     (123)     4612 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_save_imaged.py
--rw-r--r--   0 runner    (1001) docker     (123)     2353 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_save_state.py
--rw-r--r--   0 runner    (1001) docker     (123)     5875 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_savitzky_golay_filter.py
--rw-r--r--   0 runner    (1001) docker     (123)     2936 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_savitzky_golay_smooth.py
--rw-r--r--   0 runner    (1001) docker     (123)     3012 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_savitzky_golay_smoothd.py
--rw-r--r--   0 runner    (1001) docker     (123)     3141 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_scale_intensity.py
--rw-r--r--   0 runner    (1001) docker     (123)     3641 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_scale_intensity_fixed_mean.py
--rw-r--r--   0 runner    (1001) docker     (123)     1735 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_scale_intensity_range.py
--rw-r--r--   0 runner    (1001) docker     (123)     3912 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_scale_intensity_range_percentiles.py
--rw-r--r--   0 runner    (1001) docker     (123)     3975 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_scale_intensity_range_percentilesd.py
--rw-r--r--   0 runner    (1001) docker     (123)     1628 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_scale_intensity_ranged.py
--rw-r--r--   0 runner    (1001) docker     (123)     2234 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_scale_intensityd.py
--rw-r--r--   0 runner    (1001) docker     (123)     2875 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_se_block.py
--rw-r--r--   0 runner    (1001) docker     (123)     2805 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_se_blocks.py
--rw-r--r--   0 runner    (1001) docker     (123)     6396 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_seg_loss_integration.py
--rw-r--r--   0 runner    (1001) docker     (123)     4850 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_segresnet.py
--rw-r--r--   0 runner    (1001) docker     (123)     2072 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_segresnet_block.py
--rw-r--r--   0 runner    (1001) docker     (123)     5152 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_segresnet_ds.py
--rw-r--r--   0 runner    (1001) docker     (123)     1768 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_select_cross_validation_folds.py
--rw-r--r--   0 runner    (1001) docker     (123)     1438 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_select_itemsd.py
--rw-r--r--   0 runner    (1001) docker     (123)     2918 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_selfattention.py
--rw-r--r--   0 runner    (1001) docker     (123)     6227 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_senet.py
--rw-r--r--   0 runner    (1001) docker     (123)     3591 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_separable_filter.py
--rw-r--r--   0 runner    (1001) docker     (123)     2682 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_set_determinism.py
--rw-r--r--   0 runner    (1001) docker     (123)     1518 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_set_visible_devices.py
--rw-r--r--   0 runner    (1001) docker     (123)     1028 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_shift_intensity.py
--rw-r--r--   0 runner    (1001) docker     (123)     1649 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_shift_intensityd.py
--rw-r--r--   0 runner    (1001) docker     (123)     2072 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_shuffle_buffer.py
--rw-r--r--   0 runner    (1001) docker     (123)     1572 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_signal_continuouswavelet.py
--rw-r--r--   0 runner    (1001) docker     (123)     1885 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_signal_fillempty.py
--rw-r--r--   0 runner    (1001) docker     (123)     1921 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_signal_rand_add_gaussiannoise.py
--rw-r--r--   0 runner    (1001) docker     (123)     1887 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_signal_rand_add_sine.py
--rw-r--r--   0 runner    (1001) docker     (123)     2087 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_signal_rand_add_sine_partial.py
--rw-r--r--   0 runner    (1001) docker     (123)     2310 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_signal_rand_add_squarepulse.py
--rw-r--r--   0 runner    (1001) docker     (123)     2537 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_signal_rand_add_squarepulse_partial.py
--rw-r--r--   0 runner    (1001) docker     (123)     1812 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_signal_rand_drop.py
--rw-r--r--   0 runner    (1001) docker     (123)     1822 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_signal_rand_scale.py
--rw-r--r--   0 runner    (1001) docker     (123)     2123 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_signal_rand_shift.py
--rw-r--r--   0 runner    (1001) docker     (123)     3208 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_signal_remove_frequency.py
--rw-r--r--   0 runner    (1001) docker     (123)     2808 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_simple_aspp.py
--rw-r--r--   0 runner    (1001) docker     (123)     1287 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_simulatedelay.py
--rw-r--r--   0 runner    (1001) docker     (123)     1317 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_simulatedelayd.py
--rw-r--r--   0 runner    (1001) docker     (123)     1687 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_skip_connection.py
--rw-r--r--   0 runner    (1001) docker     (123)     1896 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_slice_inferer.py
--rw-r--r--   0 runner    (1001) docker     (123)    10903 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_sliding_patch_wsi_dataset.py
--rw-r--r--   0 runner    (1001) docker     (123)    11961 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_sliding_window_hovernet_inference.py
--rw-r--r--   0 runner    (1001) docker     (123)    15505 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_sliding_window_inference.py
--rw-r--r--   0 runner    (1001) docker     (123)     9615 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_sliding_window_splitter.py
--rw-r--r--   0 runner    (1001) docker     (123)     7514 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_smartcachedataset.py
--rw-r--r--   0 runner    (1001) docker     (123)     6249 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_smooth_field.py
--rw-r--r--   0 runner    (1001) docker     (123)     6829 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_sobel_gradient.py
--rw-r--r--   0 runner    (1001) docker     (123)     7989 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_sobel_gradientd.py
--rw-r--r--   0 runner    (1001) docker     (123)     8837 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_some_of.py
--rw-r--r--   0 runner    (1001) docker     (123)    14528 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_spacing.py
--rw-r--r--   0 runner    (1001) docker     (123)     6587 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_spacingd.py
--rw-r--r--   0 runner    (1001) docker     (123)     7921 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_spatial_combine_transforms.py
--rw-r--r--   0 runner    (1001) docker     (123)     3653 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_spatial_crop.py
--rw-r--r--   0 runner    (1001) docker     (123)     2455 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_spatial_cropd.py
--rw-r--r--   0 runner    (1001) docker     (123)     2209 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_spatial_pad.py
--rw-r--r--   0 runner    (1001) docker     (123)     1636 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_spatial_padd.py
--rw-r--r--   0 runner    (1001) docker     (123)     9792 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_spatial_resample.py
--rw-r--r--   0 runner    (1001) docker     (123)     4920 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_spatial_resampled.py
--rw-r--r--   0 runner    (1001) docker     (123)     1571 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_split_channel.py
--rw-r--r--   0 runner    (1001) docker     (123)     2219 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_split_channeld.py
--rw-r--r--   0 runner    (1001) docker     (123)     1858 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_splitdim.py
--rw-r--r--   0 runner    (1001) docker     (123)     3815 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_splitdimd.py
--rw-r--r--   0 runner    (1001) docker     (123)     2402 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_squeezedim.py
--rw-r--r--   0 runner    (1001) docker     (123)     3216 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_squeezedimd.py
--rw-r--r--   0 runner    (1001) docker     (123)     2104 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_ssim_loss.py
--rw-r--r--   0 runner    (1001) docker     (123)     2895 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_ssim_metric.py
--rw-r--r--   0 runner    (1001) docker     (123)     2479 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_state_cacher.py
--rw-r--r--   0 runner    (1001) docker     (123)     3332 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_std_shift_intensity.py
--rw-r--r--   0 runner    (1001) docker     (123)     3145 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_std_shift_intensityd.py
--rw-r--r--   0 runner    (1001) docker     (123)     1293 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_str2bool.py
--rw-r--r--   0 runner    (1001) docker     (123)     1232 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_str2list.py
--rw-r--r--   0 runner    (1001) docker     (123)     3081 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_subpixel_upsample.py
--rw-r--r--   0 runner    (1001) docker     (123)    21760 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_surface_dice.py
--rw-r--r--   0 runner    (1001) docker     (123)     6236 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_surface_distance.py
--rw-r--r--   0 runner    (1001) docker     (123)     3839 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_swin_unetr.py
--rw-r--r--   0 runner    (1001) docker     (123)     2442 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_synthetic.py
--rw-r--r--   0 runner    (1001) docker     (123)     4055 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_tciadataset.py
--rw-r--r--   0 runner    (1001) docker     (123)     6968 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_testtimeaugmentation.py
--rw-r--r--   0 runner    (1001) docker     (123)     2028 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_text_encoding.py
--rw-r--r--   0 runner    (1001) docker     (123)     5025 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_thread_buffer.py
--rw-r--r--   0 runner    (1001) docker     (123)     3458 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_threadcontainer.py
--rw-r--r--   0 runner    (1001) docker     (123)     1500 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_threshold_intensity.py
--rw-r--r--   0 runner    (1001) docker     (123)     2055 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_threshold_intensityd.py
--rw-r--r--   0 runner    (1001) docker     (123)     2253 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_timedcall_dist.py
--rw-r--r--   0 runner    (1001) docker     (123)     1873 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_to_contiguous.py
--rw-r--r--   0 runner    (1001) docker     (123)     4580 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_to_cupy.py
--rw-r--r--   0 runner    (1001) docker     (123)     3061 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_to_cupyd.py
--rw-r--r--   0 runner    (1001) docker     (123)     1290 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_to_device.py
--rw-r--r--   0 runner    (1001) docker     (123)     1357 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_to_deviced.py
--rw-r--r--   0 runner    (1001) docker     (123)     6851 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_to_from_meta_tensord.py
--rw-r--r--   0 runner    (1001) docker     (123)     3411 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_to_numpy.py
--rw-r--r--   0 runner    (1001) docker     (123)     2690 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_to_numpyd.py
--rw-r--r--   0 runner    (1001) docker     (123)     2223 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_to_onehot.py
--rw-r--r--   0 runner    (1001) docker     (123)     1718 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_to_pil.py
--rw-r--r--   0 runner    (1001) docker     (123)     1829 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_to_pild.py
--rw-r--r--   0 runner    (1001) docker     (123)     2109 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_to_tensor.py
--rw-r--r--   0 runner    (1001) docker     (123)     2595 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_to_tensord.py
--rw-r--r--   0 runner    (1001) docker     (123)     4089 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_torchscript_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     2613 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_torchvision.py
--rw-r--r--   0 runner    (1001) docker     (123)     6402 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_torchvision_fc_model.py
--rw-r--r--   0 runner    (1001) docker     (123)     2459 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_torchvisiond.py
--rw-r--r--   0 runner    (1001) docker     (123)     1895 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_traceable_transform.py
--rw-r--r--   0 runner    (1001) docker     (123)     1050 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_train_mode.py
--rw-r--r--   0 runner    (1001) docker     (123)    16832 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_trainable_bilateral.py
--rw-r--r--   0 runner    (1001) docker     (123)    21398 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_trainable_joint_bilateral.py
--rw-r--r--   0 runner    (1001) docker     (123)     3215 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_transchex.py
--rw-r--r--   0 runner    (1001) docker     (123)     1857 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_transform.py
--rw-r--r--   0 runner    (1001) docker     (123)     3164 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_transformerblock.py
--rw-r--r--   0 runner    (1001) docker     (123)     1352 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_transpose.py
--rw-r--r--   0 runner    (1001) docker     (123)     1884 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_transposed.py
--rw-r--r--   0 runner    (1001) docker     (123)     7738 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_tversky_loss.py
--rw-r--r--   0 runner    (1001) docker     (123)     5796 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_unet.py
--rw-r--r--   0 runner    (1001) docker     (123)     5320 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_unetr.py
--rw-r--r--   0 runner    (1001) docker     (123)     6876 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_unetr_block.py
--rw-r--r--   0 runner    (1001) docker     (123)     2313 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_unified_focal_loss.py
--rw-r--r--   0 runner    (1001) docker     (123)     4649 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_upsample_block.py
--rw-r--r--   0 runner    (1001) docker     (123)     3038 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_utils_pytorch_numpy_unification.py
--rw-r--r--   0 runner    (1001) docker     (123)     3542 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_varautoencoder.py
--rw-r--r--   0 runner    (1001) docker     (123)     2795 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_varnet.py
--rw-r--r--   0 runner    (1001) docker     (123)     2286 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_version_leq.py
--rw-r--r--   0 runner    (1001) docker     (123)     5575 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_video_datasets.py
--rw-r--r--   0 runner    (1001) docker     (123)     3088 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_vis_cam.py
--rw-r--r--   0 runner    (1001) docker     (123)     2484 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_vis_gradbased.py
--rw-r--r--   0 runner    (1001) docker     (123)     6880 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_vis_gradcam.py
--rw-r--r--   0 runner    (1001) docker     (123)     7166 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_vit.py
--rw-r--r--   0 runner    (1001) docker     (123)     4838 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_vitautoenc.py
--rw-r--r--   0 runner    (1001) docker     (123)     2627 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_vnet.py
--rw-r--r--   0 runner    (1001) docker     (123)     2666 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_vote_ensemble.py
--rw-r--r--   0 runner    (1001) docker     (123)     3622 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_vote_ensembled.py
--rw-r--r--   0 runner    (1001) docker     (123)     9146 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_warp.py
--rw-r--r--   0 runner    (1001) docker     (123)     2078 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_watershed.py
--rw-r--r--   0 runner    (1001) docker     (123)     2523 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_watershedd.py
--rw-r--r--   0 runner    (1001) docker     (123)     1712 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_weight_init.py
--rw-r--r--   0 runner    (1001) docker     (123)     2194 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_weighted_random_sampler_dist.py
--rw-r--r--   0 runner    (1001) docker     (123)     3056 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_with_allow_missing_keys.py
--rw-r--r--   0 runner    (1001) docker     (123)     3026 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_write_metrics_reports.py
--rw-r--r--   0 runner    (1001) docker     (123)     8380 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_wsi_sliding_window_splitter.py
--rw-r--r--   0 runner    (1001) docker     (123)    26104 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_wsireader.py
--rw-r--r--   0 runner    (1001) docker     (123)    10325 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_zarr_avg_merger.py
--rw-r--r--   0 runner    (1001) docker     (123)     2394 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_zipdataset.py
--rw-r--r--   0 runner    (1001) docker     (123)     4843 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_zoom.py
--rw-r--r--   0 runner    (1001) docker     (123)     3095 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_zoom_affine.py
--rw-r--r--   0 runner    (1001) docker     (123)     3475 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/tests/test_zoomd.py
--rw-r--r--   0 runner    (1001) docker     (123)    81097 2023-07-16 02:36:08.000000 monai-weekly-1.3.dev2329/versioneer.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:51.359347 monai-weekly-1.3.dev2330/
+-rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       83 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     7124 2023-07-23 02:23:51.359347 monai-weekly-1.3.dev2330/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     5001 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:51.363347 monai-weekly-1.3.dev2330/monai/
+-rw-r--r--   0 runner    (1001) docker     (123)     2335 2023-07-23 02:21:55.000000 monai-weekly-1.3.dev2330/monai/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.887339 monai-weekly-1.3.dev2330/monai/_extensions/
+-rw-r--r--   0 runner    (1001) docker     (123)      642 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/_extensions/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.887339 monai-weekly-1.3.dev2330/monai/_extensions/gmm/
+-rw-r--r--   0 runner    (1001) docker     (123)     2931 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/_extensions/gmm/gmm.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)     1760 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/_extensions/gmm/gmm.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1118 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/_extensions/gmm/gmm_cpu.cpp
+-rw-r--r--   0 runner    (1001) docker     (123)    15983 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/_extensions/gmm/gmm_cuda.cu
+-rw-r--r--   0 runner    (1001) docker     (123)     3520 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/_extensions/gmm/gmm_cuda_linalg.cuh
+-rw-r--r--   0 runner    (1001) docker     (123)     3643 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/_extensions/loader.py
+-rw-r--r--   0 runner    (1001) docker     (123)      503 2023-07-23 02:23:51.363347 monai-weekly-1.3.dev2330/monai/_version.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.891339 monai-weekly-1.3.dev2330/monai/apps/
+-rw-r--r--   0 runner    (1001) docker     (123)      908 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.895339 monai-weekly-1.3.dev2330/monai/apps/auto3dseg/
+-rw-r--r--   0 runner    (1001) docker     (123)     1016 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/auto3dseg/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1411 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/auto3dseg/__main__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    37154 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/auto3dseg/auto_runner.py
+-rw-r--r--   0 runner    (1001) docker     (123)    26165 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/auto3dseg/bundle_gen.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17963 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/auto3dseg/data_analyzer.py
+-rw-r--r--   0 runner    (1001) docker     (123)    27506 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/auto3dseg/ensemble_builder.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16620 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/auto3dseg/hpo_gen.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3991 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/auto3dseg/transforms.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3138 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/auto3dseg/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)    34568 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/datasets.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.895339 monai-weekly-1.3.dev2330/monai/apps/deepedit/
+-rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/deepedit/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4501 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/deepedit/interaction.py
+-rw-r--r--   0 runner    (1001) docker     (123)    37435 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/deepedit/transforms.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.895339 monai-weekly-1.3.dev2330/monai/apps/deepgrow/
+-rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/deepgrow/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10054 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/deepgrow/dataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3739 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/deepgrow/interaction.py
+-rw-r--r--   0 runner    (1001) docker     (123)    42011 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/deepgrow/transforms.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.899340 monai-weekly-1.3.dev2330/monai/apps/detection/
+-rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/detection/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.899340 monai-weekly-1.3.dev2330/monai/apps/detection/metrics/
+-rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/detection/metrics/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    26617 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/detection/metrics/coco.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17161 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/detection/metrics/matching.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.899340 monai-weekly-1.3.dev2330/monai/apps/detection/networks/
+-rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/detection/networks/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    53640 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/detection/networks/retinanet_detector.py
+-rw-r--r--   0 runner    (1001) docker     (123)    19136 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/detection/networks/retinanet_network.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.903339 monai-weekly-1.3.dev2330/monai/apps/detection/transforms/
+-rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/detection/transforms/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    24519 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/detection/transforms/array.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18051 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/detection/transforms/box_ops.py
+-rw-r--r--   0 runner    (1001) docker     (123)    69282 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/detection/transforms/dictionary.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.907340 monai-weekly-1.3.dev2330/monai/apps/detection/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)    13531 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/detection/utils/ATSS_matcher.py
+-rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/detection/utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18681 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/detection/utils/anchor_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11120 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/detection/utils/box_coder.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9031 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/detection/utils/box_selector.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10306 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/detection/utils/detector_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13890 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/detection/utils/hard_negative_sampler.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5818 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/detection/utils/predict_utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.907340 monai-weekly-1.3.dev2330/monai/apps/mmars/
+-rw-r--r--   0 runner    (1001) docker     (123)      726 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/mmars/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13115 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/mmars/mmars.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9996 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/mmars/model_desc.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.907340 monai-weekly-1.3.dev2330/monai/apps/nnunet/
+-rw-r--r--   0 runner    (1001) docker     (123)      745 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/nnunet/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      832 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/nnunet/__main__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    48577 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/nnunet/nnunetv2_runner.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6761 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/nnunet/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.907340 monai-weekly-1.3.dev2330/monai/apps/nuclick/
+-rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/nuclick/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    24948 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/nuclick/transforms.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.911340 monai-weekly-1.3.dev2330/monai/apps/pathology/
+-rw-r--r--   0 runner    (1001) docker     (123)     1030 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/pathology/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.911340 monai-weekly-1.3.dev2330/monai/apps/pathology/engines/
+-rw-r--r--   0 runner    (1001) docker     (123)      650 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/pathology/engines/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2397 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/pathology/engines/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.911340 monai-weekly-1.3.dev2330/monai/apps/pathology/handlers/
+-rw-r--r--   0 runner    (1001) docker     (123)      609 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/pathology/handlers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2315 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/pathology/handlers/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.911340 monai-weekly-1.3.dev2330/monai/apps/pathology/inferers/
+-rw-r--r--   0 runner    (1001) docker     (123)      660 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/pathology/inferers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9148 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/pathology/inferers/inferer.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.911340 monai-weekly-1.3.dev2330/monai/apps/pathology/losses/
+-rw-r--r--   0 runner    (1001) docker     (123)      650 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/pathology/losses/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7293 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/pathology/losses/hovernet_loss.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.911340 monai-weekly-1.3.dev2330/monai/apps/pathology/metrics/
+-rw-r--r--   0 runner    (1001) docker     (123)      646 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/pathology/metrics/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7225 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/pathology/metrics/lesion_froc.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.915340 monai-weekly-1.3.dev2330/monai/apps/pathology/transforms/
+-rw-r--r--   0 runner    (1001) docker     (123)     2243 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/pathology/transforms/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.915340 monai-weekly-1.3.dev2330/monai/apps/pathology/transforms/post/
+-rw-r--r--   0 runner    (1001) docker     (123)     1995 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/pathology/transforms/post/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    37306 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/pathology/transforms/post/array.py
+-rw-r--r--   0 runner    (1001) docker     (123)    25928 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/pathology/transforms/post/dictionary.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.915340 monai-weekly-1.3.dev2330/monai/apps/pathology/transforms/stain/
+-rw-r--r--   0 runner    (1001) docker     (123)      836 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/pathology/transforms/stain/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8366 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/pathology/transforms/stain/array.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4761 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/pathology/transforms/stain/dictionary.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2860 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/pathology/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.919340 monai-weekly-1.3.dev2330/monai/apps/reconstruction/
+-rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/reconstruction/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8393 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/reconstruction/complex_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3644 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/reconstruction/fastmri_reader.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2000 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/reconstruction/mri_utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.919340 monai-weekly-1.3.dev2330/monai/apps/reconstruction/networks/
+-rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/reconstruction/networks/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.919340 monai-weekly-1.3.dev2330/monai/apps/reconstruction/networks/blocks/
+-rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/reconstruction/networks/blocks/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4183 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/reconstruction/networks/blocks/varnetblock.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.919340 monai-weekly-1.3.dev2330/monai/apps/reconstruction/networks/nets/
+-rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/reconstruction/networks/nets/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6215 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/reconstruction/networks/nets/coil_sensitivity_model.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4775 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/reconstruction/networks/nets/complex_unet.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11377 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/reconstruction/networks/nets/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3831 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/reconstruction/networks/nets/varnet.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.923340 monai-weekly-1.3.dev2330/monai/apps/reconstruction/transforms/
+-rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/reconstruction/transforms/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12240 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/reconstruction/transforms/array.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15829 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/reconstruction/transforms/dictionary.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.923340 monai-weekly-1.3.dev2330/monai/apps/tcia/
+-rw-r--r--   0 runner    (1001) docker     (123)      765 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/tcia/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1582 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/tcia/label_desc.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6152 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/tcia/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14170 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/apps/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.923340 monai-weekly-1.3.dev2330/monai/auto3dseg/
+-rw-r--r--   0 runner    (1001) docker     (123)     1164 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/auto3dseg/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4286 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/auto3dseg/algo_gen.py
+-rw-r--r--   0 runner    (1001) docker     (123)    41223 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/auto3dseg/analyzer.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5110 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/auto3dseg/operations.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8725 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/auto3dseg/seg_summarizer.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18650 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/auto3dseg/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.927340 monai-weekly-1.3.dev2330/monai/bundle/
+-rw-r--r--   0 runner    (1001) docker     (123)     1341 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/bundle/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      926 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/bundle/__main__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16035 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/bundle/config_item.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22386 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/bundle/config_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9814 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/bundle/properties.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14353 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/bundle/reference_resolver.py
+-rw-r--r--   0 runner    (1001) docker     (123)    64632 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/bundle/scripts.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8911 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/bundle/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)    19172 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/bundle/workflows.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.931340 monai-weekly-1.3.dev2330/monai/config/
+-rw-r--r--   0 runner    (1001) docker     (123)     1048 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/config/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9913 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/config/deviceconfig.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3485 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/config/type_definitions.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.943340 monai-weekly-1.3.dev2330/monai/data/
+-rw-r--r--   0 runner    (1001) docker     (123)     5087 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/data/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    50102 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/data/box_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4952 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/data/csv_saver.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3835 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/data/dataloader.py
+-rw-r--r--   0 runner    (1001) docker     (123)    68912 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/data/dataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10216 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/data/dataset_summary.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10318 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/data/decathlon_datalist.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4448 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/data/fft_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6344 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/data/folder_layout.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12484 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/data/grid_dataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7008 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/data/image_dataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)    60653 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/data/image_reader.py
+-rw-r--r--   0 runner    (1001) docker     (123)    39872 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/data/image_writer.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13309 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/data/iterable_dataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14097 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/data/itk_torch_bridge.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8800 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/data/meta_obj.py
+-rw-r--r--   0 runner    (1001) docker     (123)    27511 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/data/meta_tensor.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5268 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/data/samplers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7375 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/data/synthetic.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9780 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/data/test_time_augmentation.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8840 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/data/thread_buffer.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5500 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/data/torchscript_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)    65554 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/data/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9059 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/data/video_dataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18619 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/data/wsi_datasets.py
+-rw-r--r--   0 runner    (1001) docker     (123)    49494 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/data/wsi_reader.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.943340 monai-weekly-1.3.dev2330/monai/engines/
+-rw-r--r--   0 runner    (1001) docker     (123)     1133 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/engines/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    24568 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/engines/evaluator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7278 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/engines/multi_gpu_supervised_trainer.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21347 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/engines/trainer.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11631 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/engines/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15250 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/engines/workflow.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.943340 monai-weekly-1.3.dev2330/monai/fl/
+-rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/fl/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.947340 monai-weekly-1.3.dev2330/monai/fl/client/
+-rw-r--r--   0 runner    (1001) docker     (123)      725 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/fl/client/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5097 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/fl/client/client_algo.py
+-rw-r--r--   0 runner    (1001) docker     (123)    33232 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/fl/client/monai_algo.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.947340 monai-weekly-1.3.dev2330/monai/fl/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/fl/utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1713 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/fl/utils/constants.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3527 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/fl/utils/exchange_object.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1633 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/fl/utils/filters.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.963341 monai-weekly-1.3.dev2330/monai/handlers/
+-rw-r--r--   0 runner    (1001) docker     (123)     2372 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6798 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/checkpoint_loader.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16071 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/checkpoint_saver.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7606 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/classification_saver.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7506 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/clearml_handlers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4006 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/confusion_matrix.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4425 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/decollate_batch.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4381 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/earlystop_handler.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3645 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/garbage_collector.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3594 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/hausdorff_distance.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7460 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/ignite_metric.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3931 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/logfile_handler.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3575 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/lr_schedule_handler.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3234 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/mean_dice.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2845 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/mean_iou.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5477 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/metric_logger.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6195 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/metrics_reloaded_handler.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8560 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/metrics_saver.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22501 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/mlflow_handler.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6819 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/nvtx_handlers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3651 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/panoptic_quality.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7119 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/parameter_scheduler.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3285 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/postprocessing.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5336 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/probability_maps.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8457 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/regression_metrics.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2744 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/roc_auc.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3051 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/smartcache_handler.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14251 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/stats_handler.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3327 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/surface_distance.py
+-rw-r--r--   0 runner    (1001) docker     (123)    23325 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/tensorboard_handlers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9855 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3269 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/handlers/validation_handler.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.963341 monai-weekly-1.3.dev2330/monai/inferers/
+-rw-r--r--   0 runner    (1001) docker     (123)      958 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/inferers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    33929 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/inferers/inferer.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15566 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/inferers/merger.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21149 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/inferers/splitter.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20017 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/inferers/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.971341 monai-weekly-1.3.dev2330/monai/losses/
+-rw-r--r--   0 runner    (1001) docker     (123)     1409 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/losses/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3341 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/losses/contrastive.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4979 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/losses/deform.py
+-rw-r--r--   0 runner    (1001) docker     (123)    46326 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/losses/dice.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3854 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/losses/ds_loss.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11733 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/losses/focal_loss.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2795 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/losses/giou_loss.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15492 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/losses/image_dissimilarity.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3636 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/losses/multi_scale.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2955 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/losses/spatial_mask.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4825 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/losses/ssim_loss.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6645 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/losses/tversky.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10224 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/losses/unified_focal_loss.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.979341 monai-weekly-1.3.dev2330/monai/metrics/
+-rw-r--r--   0 runner    (1001) docker     (123)     2001 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/metrics/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8211 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/metrics/active_learning_metrics.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15107 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/metrics/confusion_matrix.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5578 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/metrics/cumulative_average.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4026 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/metrics/f_beta_score.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7981 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/metrics/froc.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8265 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/metrics/generalized_dice.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11473 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/metrics/hausdorff_distance.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4907 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/metrics/loss_metric.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12481 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/metrics/meandice.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7215 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/metrics/meaniou.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15140 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/metrics/metric.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13679 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/metrics/panoptic_quality.py
+-rw-r--r--   0 runner    (1001) docker     (123)    19719 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/metrics/regression.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8038 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/metrics/rocauc.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15886 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/metrics/surface_dice.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10192 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/metrics/surface_distance.py
+-rw-r--r--   0 runner    (1001) docker     (123)    42239 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/metrics/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11781 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/metrics/wrapper.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.979341 monai-weekly-1.3.dev2330/monai/networks/
+-rw-r--r--   0 runner    (1001) docker     (123)     1020 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.991341 monai-weekly-1.3.dev2330/monai/networks/blocks/
+-rw-r--r--   0 runner    (1001) docker     (123)     2134 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/blocks/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4275 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/blocks/acti_norm.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5839 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/blocks/activation.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4380 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/blocks/aspp.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7488 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/blocks/backbone_fpn_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11686 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/blocks/convolutions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5009 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/blocks/crf.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4747 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/blocks/denseblock.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9255 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/blocks/dints_block.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2413 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/blocks/downsample.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11062 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/blocks/dynunet_block.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3669 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/blocks/encoder.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9024 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/blocks/fcn.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10586 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/blocks/feature_pyramid_network.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8263 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/blocks/fft_utils_t.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11454 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/blocks/localnet_block.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2813 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/blocks/mlp.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8030 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/blocks/patchembedding.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8825 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/blocks/regunet_block.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3245 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/blocks/segresnet_block.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3099 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/blocks/selfattention.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12752 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/blocks/squeeze_and_excitation.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3814 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/blocks/text_embedding.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2322 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/blocks/transformerblock.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9049 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/blocks/unetr_block.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13312 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/blocks/upsample.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6656 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/blocks/warp.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:50.995341 monai-weekly-1.3.dev2330/monai/networks/layers/
+-rw-r--r--   0 runner    (1001) docker     (123)     1562 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/layers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8288 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/layers/convutils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1802 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/layers/drop_path.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12638 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/layers/factories.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17992 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/layers/filtering.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3324 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/layers/gmm.py
+-rw-r--r--   0 runner    (1001) docker     (123)    28470 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/layers/simplelayers.py
+-rw-r--r--   0 runner    (1001) docker     (123)    25576 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/layers/spatial_transforms.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4296 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/layers/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2253 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/layers/weight_init.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:51.015341 monai-weekly-1.3.dev2330/monai/networks/nets/
+-rw-r--r--   0 runner    (1001) docker     (123)     3197 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21564 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/ahnet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9202 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/attentionunet.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12089 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/autoencoder.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10950 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/basic_unet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7960 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/basic_unetplusplus.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6293 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/classifier.py
+-rw-r--r--   0 runner    (1001) docker     (123)    23786 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/daf3d.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15820 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/densenet.py
+-rw-r--r--   0 runner    (1001) docker     (123)    44771 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/dints.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18210 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/dynunet.py
+-rw-r--r--   0 runner    (1001) docker     (123)    40667 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/efficientnet.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14147 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/flexible_unet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7212 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/fullyconnectednet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6581 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/generator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8882 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/highresnet.py
+-rw-r--r--   0 runner    (1001) docker     (123)    28678 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/hovernet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9812 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/milmodel.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6102 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/netadapter.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20220 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/quicknat.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6482 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/regressor.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18662 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/regunet.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16785 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/resnet.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13994 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/segresnet.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15716 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/segresnet_ds.py
+-rw-r--r--   0 runner    (1001) docker     (123)    19289 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/senet.py
+-rw-r--r--   0 runner    (1001) docker     (123)    42000 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/swin_unetr.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6309 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/torchvision_fc.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16626 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/transchex.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13722 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/unet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8255 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/unetr.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6282 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/varautoencoder.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5655 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/vit.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5739 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/vitautoenc.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10011 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/nets/vnet.py
+-rw-r--r--   0 runner    (1001) docker     (123)    47132 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/networks/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:51.015341 monai-weekly-1.3.dev2330/monai/optimizers/
+-rw-r--r--   0 runner    (1001) docker     (123)      796 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/optimizers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21952 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/optimizers/lr_finder.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4082 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/optimizers/lr_scheduler.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5661 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/optimizers/novograd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4131 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/optimizers/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/py.typed
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:51.023342 monai-weekly-1.3.dev2330/monai/transforms/
+-rw-r--r--   0 runner    (1001) docker     (123)    15545 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8946 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/adaptors.py
+-rw-r--r--   0 runner    (1001) docker     (123)    37090 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/compose.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:51.027341 monai-weekly-1.3.dev2330/monai/transforms/croppad/
+-rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/croppad/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    75075 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/croppad/array.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6138 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/croppad/batch.py
+-rw-r--r--   0 runner    (1001) docker     (123)    61070 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/croppad/dictionary.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12628 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/croppad/functional.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:51.027341 monai-weekly-1.3.dev2330/monai/transforms/intensity/
+-rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/intensity/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)   107785 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/intensity/array.py
+-rw-r--r--   0 runner    (1001) docker     (123)    82230 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/intensity/dictionary.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18233 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/inverse.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7054 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/inverse_batch_transform.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:51.031342 monai-weekly-1.3.dev2330/monai/transforms/io/
+-rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/io/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    25374 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/io/array.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17821 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/io/dictionary.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:51.031342 monai-weekly-1.3.dev2330/monai/transforms/lazy/
+-rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/lazy/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1211 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/lazy/array.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1571 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/lazy/dictionary.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15183 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/lazy/functional.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9840 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/lazy/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:51.031342 monai-weekly-1.3.dev2330/monai/transforms/meta_utility/
+-rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/meta_utility/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4896 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/meta_utility/dictionary.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3386 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/nvtx.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:51.035342 monai-weekly-1.3.dev2330/monai/transforms/post/
+-rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/post/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    40802 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/post/array.py
+-rw-r--r--   0 runner    (1001) docker     (123)    39905 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/post/dictionary.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:51.035342 monai-weekly-1.3.dev2330/monai/transforms/signal/
+-rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/signal/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16322 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/signal/array.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:51.035342 monai-weekly-1.3.dev2330/monai/transforms/smooth_field/
+-rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/smooth_field/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17833 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/smooth_field/array.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11194 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/smooth_field/dictionary.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:51.039342 monai-weekly-1.3.dev2330/monai/transforms/spatial/
+-rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/spatial/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)   179599 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/spatial/array.py
+-rw-r--r--   0 runner    (1001) docker     (123)   127418 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/spatial/dictionary.py
+-rw-r--r--   0 runner    (1001) docker     (123)    31249 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/spatial/functional.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3563 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/traits.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21511 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/transform.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:51.043342 monai-weekly-1.3.dev2330/monai/transforms/utility/
+-rw-r--r--   0 runner    (1001) docker     (123)      573 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/utility/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    70963 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/utility/array.py
+-rw-r--r--   0 runner    (1001) docker     (123)    76167 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/utility/dictionary.py
+-rw-r--r--   0 runner    (1001) docker     (123)    81426 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)    31081 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/utils_create_transform_ims.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18397 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/transforms/utils_pytorch_numpy_unification.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:51.047342 monai-weekly-1.3.dev2330/monai/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)     3465 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4096 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/utils/aliases.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3129 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/utils/decorators.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14759 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/utils/deprecate_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8525 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/utils/dist.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17055 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/utils/enums.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15637 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/utils/jupyter_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)    29761 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/utils/misc.py
+-rw-r--r--   0 runner    (1001) docker     (123)    23631 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/utils/module.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6876 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/utils/nvtx.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15936 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/utils/profiling.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5955 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/utils/state_cacher.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21147 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/utils/type_conversion.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:51.051342 monai-weekly-1.3.dev2330/monai/visualize/
+-rw-r--r--   0 runner    (1001) docker     (123)     1038 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/visualize/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16156 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/visualize/class_activation_maps.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6277 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/visualize/gradient_based.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9200 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/visualize/img2tensorboard.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18160 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/visualize/occlusion_sensitivity.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9966 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/visualize/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1377 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/monai/visualize/visualizer.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:51.055342 monai-weekly-1.3.dev2330/monai_weekly.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     7124 2023-07-23 02:23:50.000000 monai-weekly-1.3.dev2330/monai_weekly.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    34350 2023-07-23 02:23:50.000000 monai-weekly-1.3.dev2330/monai_weekly.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 02:23:50.000000 monai-weekly-1.3.dev2330/monai_weekly.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 02:23:50.000000 monai-weekly-1.3.dev2330/monai_weekly.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)     1155 2023-07-23 02:23:50.000000 monai-weekly-1.3.dev2330/monai_weekly.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        6 2023-07-23 02:23:50.000000 monai-weekly-1.3.dev2330/monai_weekly.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1831 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)     4272 2023-07-23 02:23:51.363347 monai-weekly-1.3.dev2330/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     5183 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 02:23:51.359347 monai-weekly-1.3.dev2330/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     1390 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_acn_block.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3822 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_activations.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2483 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_activationsd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4576 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_adaptors.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1370 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_add_channeld.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2243 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_add_coordinate_channels.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2479 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_add_coordinate_channelsd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2770 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_add_extreme_points_channel.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2647 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_add_extreme_points_channeld.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2573 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_adjust_contrast.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2365 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_adjust_contrastd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3186 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_adn.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10055 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_affine.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6623 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_affine_grid.py
+-rw-r--r--   0 runner    (1001) docker     (123)    19674 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_affine_transform.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7832 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_affined.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8343 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_ahnet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1514 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_alias.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3921 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_anchor_box.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2844 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_apply.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3740 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_apply_filter.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8267 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_arraydataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1576 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_as_channel_first.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1800 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_as_channel_firstd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1353 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_as_channel_last.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1796 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_as_channel_lastd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2599 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_as_discrete.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3047 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_as_discreted.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1701 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_atss_box_matcher.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2660 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_attentionunet.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21577 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_auto3dseg.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5589 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_auto3dseg_bundlegen.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7565 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_auto3dseg_ensemble.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7281 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_auto3dseg_hpo.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2959 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_autoencoder.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5947 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_avg_merger.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3332 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_basic_unet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3707 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_basic_unetplusplus.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3661 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_bending_energy.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13648 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_bilateral_approx_cpu.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13773 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_bilateral_approx_cuda.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15064 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_bilateral_precise.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2269 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_blend_images.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1818 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_border_pad.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1747 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_border_padd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1812 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_bounding_rect.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1836 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_bounding_rectd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1745 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_box_coder.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18036 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_box_transform.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8925 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_box_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3313 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_bundle_ckpt_export.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7692 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_bundle_download.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2719 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_bundle_get_data.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1929 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_bundle_init_bundle.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2806 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_bundle_onnx_export.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6181 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_bundle_trt_export.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4170 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_bundle_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2624 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_bundle_verify_metadata.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3326 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_bundle_verify_net.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6172 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_bundle_workflow.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9868 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_cachedataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2216 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_cachedataset_parallel.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1707 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_cachedataset_persistent_workers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2453 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_cachentransdataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1126 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_call_dist.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2428 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_cast_to_type.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2602 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_cast_to_typed.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1918 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_center_scale_crop.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2064 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_center_scale_cropd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1983 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_center_spatial_crop.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2045 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_center_spatial_cropd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1671 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_channel_pad.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1760 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_check_hash.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2493 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_check_missing_files.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2914 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_classes_to_indices.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3604 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_classes_to_indicesd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2669 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_complex_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1506 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_component_locator.py
+-rw-r--r--   0 runner    (1001) docker     (123)    25175 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_compose.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3915 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_compose_get_number_conversions.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10091 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_compute_confusion_matrix.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3458 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_compute_f_beta.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4519 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_compute_froc.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6021 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_compute_generalized_dice.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2528 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_compute_ho_ver_maps.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2829 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_compute_ho_ver_maps_d.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8892 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_compute_meandice.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8044 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_compute_meaniou.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5106 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_compute_panoptic_quality.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8066 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_compute_regression_metrics.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4578 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_compute_roc_auc.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4902 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_compute_variance.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3804 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_concat_itemsd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5814 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_config_item.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14667 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_config_parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2947 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_contrastive_loss.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6124 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_convert_data_type.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1949 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_convert_to_multi_channel.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1321 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_convert_to_multi_channeld.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4283 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_convert_to_onnx.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1635 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_convert_to_torchscript.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2567 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_convert_to_trt.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7134 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_convolutions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3810 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_copy_itemsd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6761 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_copy_model_state.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1388 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_correct_crop_centers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2173 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_create_cross_validation_datalist.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10466 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_create_grid_and_affine.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18866 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_crf_cpu.py
+-rw-r--r--   0 runner    (1001) docker     (123)    19445 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_crf_cuda.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6724 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_crop_foreground.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7621 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_crop_foregroundd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2925 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_cross_validation.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8682 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_csv_dataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11089 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_csv_iterable_dataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1651 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_csv_saver.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5627 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_cucim_dict_transform.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5460 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_cucim_transform.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1922 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_cumulative.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2369 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_cumulative_average.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1761 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_cumulative_average_dist.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1984 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_cv2_dist.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2326 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_daf3d.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5532 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_data_stats.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5935 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_data_statsd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4034 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_dataloader.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4461 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_dataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2271 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_dataset_func.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4651 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_dataset_summary.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3851 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_decathlondataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10471 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_decollate.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4579 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_deepedit_interaction.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10621 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_deepedit_transforms.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3959 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_deepgrow_dataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3721 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_deepgrow_interaction.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16313 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_deepgrow_transforms.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2239 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_delete_itemsd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4368 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_denseblock.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4434 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_densenet.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14747 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_deprecated.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6294 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_detect_envelope.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2850 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_detection_coco_metrics.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2292 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_detector_boxselector.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2996 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_detector_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1568 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_dev_collate.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4029 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_dice_ce_loss.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3626 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_dice_focal_loss.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8106 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_dice_loss.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3175 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_dints_cell.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2724 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_dints_mixop.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5780 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_dints_network.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1911 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_discriminator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1764 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_divisible_pad.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1497 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_divisible_padd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2936 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_download_and_extract.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1626 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_download_url_yandex.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1793 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_downsample_block.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1511 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_drop_path.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7026 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_ds_loss.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2390 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_dvf2ddf.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7235 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_dynunet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4989 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_dynunet_block.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13331 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_efficientnet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3142 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_ensemble_evaluator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4434 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_ensure_channel_first.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3360 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_ensure_channel_firstd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1789 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_ensure_tuple.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4575 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_ensure_type.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4873 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_ensure_typed.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3223 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_enum_bound_interp.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1085 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_eval_mode.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1846 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_evenly_divisible_all_gather_dist.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1305 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_factorized_increase.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1304 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_factorized_reduce.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2402 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_fastmri_reader.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2316 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_fft_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2573 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_fg_bg_to_indices.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2786 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_fg_bg_to_indicesd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3857 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_file_basename.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5804 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_fill_holes.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5903 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_fill_holesd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2566 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_fl_exchange_object.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8696 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_fl_monai_algo.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4994 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_fl_monai_algo_dist.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2867 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_fl_monai_algo_stats.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2392 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_flatten_sub_keysd.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13497 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_flexible_unet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3087 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_flip.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3556 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_flipd.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17277 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_focal_loss.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3152 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_folder_layout.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4155 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_foreground_mask.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4813 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_foreground_maskd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2332 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_fourier.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3462 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_fpn_block.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1342 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_from_engine_hovernet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2173 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_fullyconnectednet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9063 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_gaussian.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8085 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_gaussian_filter.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3090 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_gaussian_sharpen.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3231 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_gaussian_sharpend.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3146 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_gaussian_smooth.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3286 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_gaussian_smoothd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3517 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_generalized_dice_focal_loss.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8036 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_generalized_dice_loss.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9727 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_generalized_wasserstein_dice_loss.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1924 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_generate_distance_map.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2330 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_generate_distance_mapd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2016 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_generate_instance_border.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2251 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_generate_instance_borderd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1981 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_generate_instance_centroid.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2139 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_generate_instance_centroidd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2199 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_generate_instance_contour.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2358 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_generate_instance_contourd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1663 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_generate_instance_type.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1853 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_generate_instance_typed.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2315 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_generate_label_classes_crop_centers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3365 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_generate_param_groups.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2511 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_generate_pos_neg_label_crop_centers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3505 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_generate_spatial_bounding_box.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1944 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_generate_succinct_contour.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2037 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_generate_succinct_contourd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2052 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_generate_watershed_markers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2830 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_generate_watershed_markersd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2564 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_generate_watershed_mask.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2722 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_generate_watershed_maskd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1984 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_generator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2282 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_get_equivalent_dtype.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1695 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_get_extreme_points.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2207 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_get_layers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1123 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_get_package_version.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1681 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_get_unique_labels.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2647 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_gibbs_noise.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3223 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_gibbs_noised.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2016 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_giou_loss.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5465 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_global_mutual_information_loss.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3796 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_globalnet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9431 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_gmm.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8683 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_grid_dataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4467 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_grid_distortion.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3487 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_grid_distortiond.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5948 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_grid_patch.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4737 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_grid_patchd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3924 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_grid_pull.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3422 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_grid_split.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4059 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_grid_splitd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8438 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_checkpoint_loader.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6255 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_checkpoint_saver.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2354 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_classification_saver.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2776 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_classification_saver_dist.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2602 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_clearml_image.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2602 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_clearml_stats.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3911 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_confusion_matrix.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2542 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_confusion_matrix_dist.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2477 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_decollate_batch.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2154 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_early_stop.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2829 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_garbage_collector.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3879 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_hausdorff_distance.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7367 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_ignite_metric.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2555 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_logfile.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3335 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_lr_scheduler.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4182 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_mean_dice.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3018 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_mean_iou.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1920 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_metric_logger.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5833 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_metrics_reloaded.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3835 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_metrics_saver.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4975 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_metrics_saver_dist.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11363 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_mlflow.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3820 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_nvtx.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3142 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_panoptic_quality.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4887 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_parameter_scheduler.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2872 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_post_processing.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3694 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_prob_map_producer.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6691 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_regression_metrics.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8660 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_regression_metrics_dist.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1553 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_rocauc.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2005 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_rocauc_dist.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1641 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_smartcache.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9501 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_stats.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4001 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_surface_distance.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2246 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_tb_image.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6731 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_tb_stats.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1575 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_handler_validation.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2069 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_hardnegsampler.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1752 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_hashing.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6766 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_hausdorff_distance.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1576 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_header_correct.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2283 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_highresnet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7425 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_hilbert_transform.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1965 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_histogram_normalize.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2070 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_histogram_normalized.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7968 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_hovernet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2545 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_hovernet_instance_map_post_processing.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2794 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_hovernet_instance_map_post_processingd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6766 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_hovernet_loss.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2549 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_hovernet_nuclear_type_post_processing.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2656 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_hovernet_nuclear_type_post_processingd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1022 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_identity.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1087 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_identityd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7196 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_image_dataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10444 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_image_filter.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8414 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_image_rw.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1762 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_img2tensorboard.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2225 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_init_reader.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7566 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_integration_autorunner.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7311 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_integration_bundle_run.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11343 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_integration_classification_2d.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3167 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_integration_determinism.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9737 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_integration_fast_train.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5542 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_integration_gpu_customization.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9193 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_integration_lazy_samples.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4327 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_integration_nnunetv2_runner.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13199 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_integration_segmentation_3d.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3878 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_integration_sliding_window.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4941 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_integration_stn.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2356 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_integration_unet_2d.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2190 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_integration_workers.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14051 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_integration_workflows.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5491 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_integration_workflows_gan.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2790 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_intensity_stats.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3594 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_intensity_statsd.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18993 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_inverse.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2764 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_inverse_array.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5452 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_inverse_collation.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4287 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_invert.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6090 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_invertd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1675 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_is_supported_format.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2344 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_iterable_dataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18618 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_itk_torch_bridge.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2621 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_itk_writer.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2858 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_k_space_spike_noise.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3506 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_k_space_spike_noised.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14754 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_keep_largest_connected_component.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12548 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_keep_largest_connected_componentd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1815 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_kspace_mask.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2503 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_label_filter.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2592 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_label_filterd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4982 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_label_quality_score.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6767 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_label_to_contour.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6963 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_label_to_contourd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2488 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_label_to_mask.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2642 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_label_to_maskd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2354 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_lambda.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3122 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_lambdad.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9763 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_lesion_froc.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2167 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_list_data_collate.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1552 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_list_to_dict.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2347 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_lltm.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8929 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_lmdbdataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2530 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_lmdbdataset_dist.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6475 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_load_decathlon_datalist.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15192 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_load_image.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8802 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_load_imaged.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6235 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_load_spacing_orientation.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1194 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_loader_semaphore.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6069 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_local_normalized_cross_correlation_loss.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2834 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_localnet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4803 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_localnet_block.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2997 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_look_up_option.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2105 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_loss_metric.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3683 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_lr_finder.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2569 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_lr_scheduler.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1498 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_make_nifti.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2468 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_map_binary_to_indices.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4331 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_map_classes_to_indices.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3017 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_map_label_value.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2539 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_map_label_valued.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1390 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_map_transform.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3087 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_mask_intensity.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2705 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_mask_intensityd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6303 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_masked_dice_loss.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3288 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_masked_loss.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4408 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_masked_patch_wsi_dataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4879 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_matshow3d.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2748 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_mean_ensemble.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3369 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_mean_ensembled.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1957 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_median_filter.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1372 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_median_smooth.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2248 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_median_smoothd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3050 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_mednistdataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7458 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_meta_affine.py
+-rw-r--r--   0 runner    (1001) docker     (123)    23538 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_meta_tensor.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5452 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_metatensor_integration.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4653 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_metrics_reloaded.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3228 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_milmodel.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1713 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_mlp.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6340 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_mmar_download.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3132 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_module_list.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1475 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_monai_env_vars.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3759 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_monai_utils_misc.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1220 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_mri_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3005 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_multi_scale.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2636 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_net_adapter.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2820 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_network_consistency.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4036 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_nifti_endianness.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1528 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_nifti_header_revise.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12065 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_nifti_rw.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4999 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_normalize_intensity.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3058 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_normalize_intensityd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1833 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_npzdictitemdataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6066 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_nrrd_reader.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9614 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_nuclick_transforms.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5716 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_numpy_reader.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10570 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_nvtx_decorator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5139 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_nvtx_transform.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4422 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_occlusion_sensitivity.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8860 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_one_of.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3694 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_optim_novograd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3309 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_optional_import.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1851 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_ori_ras_lps.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8125 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_orientation.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4228 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_orientationd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2371 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_p3d_block.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4626 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_pad_collation.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1610 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_pad_mode.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2197 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_parallel_execution.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1610 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_parallel_execution_dist.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2939 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_partition_dataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2587 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_partition_dataset_classes.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3219 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_patch_dataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9873 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_patch_inferer.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8349 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_patch_wsi_dataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6344 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_patchembedding.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10327 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_pathology_he_stain.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10277 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_pathology_he_stain_dict.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1766 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_pathology_prob_nms.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8109 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_persistentdataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3055 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_persistentdataset_dist.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9041 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_phl_cpu.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4842 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_phl_cuda.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3684 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_pil_reader.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2730 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_plot_2d_or_3d_image.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4324 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_png_rw.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1993 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_polyval.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3697 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_prepare_batch_default.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2479 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_prepare_batch_default_dist.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2745 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_prepare_batch_extra_input.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2466 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_prepare_batch_hovernet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4070 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_preset_filters.py
+-rw-r--r--   0 runner    (1001) docker     (123)      818 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_print_info.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1049 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_print_transform_backends.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2861 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_probnms.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3065 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_probnmsd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6606 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_profiling.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1599 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_pytorch_version_after.py
+-rw-r--r--   0 runner    (1001) docker     (123)      988 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_query_memory.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2596 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_quicknat.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1582 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_adjust_contrast.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1600 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_adjust_contrastd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7254 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_affine.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9724 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_affine_grid.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10949 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_affined.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1836 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_axis_flip.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1927 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_axis_flipd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2646 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_bias_field.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2439 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_bias_fieldd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4178 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_coarse_dropout.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4077 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_coarse_dropoutd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2279 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_coarse_shuffle.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2062 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_coarse_shuffled.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6393 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_crop_by_label_classes.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5846 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_crop_by_label_classesd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5597 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_crop_by_pos_neg_label.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6605 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_crop_by_pos_neg_labeld.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6459 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_cucim_dict_transform.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6314 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_cucim_transform.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6339 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_deform_grid.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4596 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_elastic_2d.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3762 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_elastic_3d.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6681 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_elasticd_2d.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5867 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_elasticd_3d.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2342 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_flip.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2150 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_flipd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1631 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_gaussian_noise.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1849 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_gaussian_noised.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4619 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_gaussian_sharpen.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4848 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_gaussian_sharpend.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3421 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_gaussian_smooth.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3500 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_gaussian_smoothd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3391 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_gibbs_noise.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4090 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_gibbs_noised.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4092 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_grid_distortion.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3574 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_grid_distortiond.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5916 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_grid_patch.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4604 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_grid_patchd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3363 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_histogram_shift.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2809 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_histogram_shiftd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3486 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_k_space_spike_noise.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2598 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_k_space_spike_noised.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2980 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_lambda.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2801 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_lambdad.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1840 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_rician_noise.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1964 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_rician_noised.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5674 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_rotate.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4079 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_rotate90.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4347 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_rotate90d.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6332 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_rotated.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3106 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_scale_crop.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3527 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_scale_cropd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1435 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_scale_intensity.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1489 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_scale_intensity_fixed_mean.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1542 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_scale_intensity_fixed_meand.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1416 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_scale_intensityd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1398 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_shift_intensity.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2054 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_shift_intensityd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4614 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_spatial_crop.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5315 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_spatial_crop_samples.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6243 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_spatial_crop_samplesd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4877 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_spatial_cropd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1599 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_std_shift_intensity.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1453 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_std_shift_intensityd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6572 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_weighted_crop.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6553 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_weighted_cropd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4391 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_zoom.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4265 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rand_zoomd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1654 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_randidentity.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5182 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_random_order.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1565 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_randomizable.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1200 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_randomizable_transform_type.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2569 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_randtorchvisiond.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1673 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rankfilter_dist.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3179 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_recon_net_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3150 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_reference_based_normalize_intensity.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1970 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_reference_based_spatial_cropd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4239 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_reference_resolver.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3905 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_reg_loss_integration.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2806 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_regunet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3458 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_regunet_block.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1212 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_remove_repeated_channel.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1424 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_remove_repeated_channeld.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3197 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_remove_small_objects.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1162 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_repeat_channel.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1328 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_repeat_channeld.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4345 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_replace_module.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2280 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_require_pkg.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1902 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_resample.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3173 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_resample_backends.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1441 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_resample_datalist.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4556 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_resample_to_match.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3607 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_resample_to_matchd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7015 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_resampler.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5568 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_resize.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4203 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_resize_with_pad_or_crop.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3995 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_resize_with_pad_or_cropd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6016 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_resized.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5475 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_resnet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7415 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_retinanet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7717 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_retinanet_detector.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4992 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_retinanet_predict_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6739 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rotate.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8062 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rotate90.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4061 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rotate90d.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8360 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_rotated.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3958 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_safe_dtype_range.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1948 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_saliency_inferer.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1874 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_sample_slices.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3463 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_sampler_dist.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4137 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_save_classificationd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2323 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_save_image.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4612 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_save_imaged.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2353 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_save_state.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5875 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_savitzky_golay_filter.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2936 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_savitzky_golay_smooth.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3012 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_savitzky_golay_smoothd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3141 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_scale_intensity.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3641 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_scale_intensity_fixed_mean.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1735 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_scale_intensity_range.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3912 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_scale_intensity_range_percentiles.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3975 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_scale_intensity_range_percentilesd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1628 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_scale_intensity_ranged.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2234 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_scale_intensityd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2875 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_se_block.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2805 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_se_blocks.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6396 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_seg_loss_integration.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4850 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_segresnet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2072 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_segresnet_block.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5152 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_segresnet_ds.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1768 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_select_cross_validation_folds.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1438 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_select_itemsd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2918 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_selfattention.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6227 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_senet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3591 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_separable_filter.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2682 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_set_determinism.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1518 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_set_visible_devices.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1028 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_shift_intensity.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1649 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_shift_intensityd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2072 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_shuffle_buffer.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1572 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_signal_continuouswavelet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1885 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_signal_fillempty.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1921 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_signal_rand_add_gaussiannoise.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1887 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_signal_rand_add_sine.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2087 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_signal_rand_add_sine_partial.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2310 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_signal_rand_add_squarepulse.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2537 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_signal_rand_add_squarepulse_partial.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1812 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_signal_rand_drop.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1822 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_signal_rand_scale.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2123 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_signal_rand_shift.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3208 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_signal_remove_frequency.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2808 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_simple_aspp.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1287 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_simulatedelay.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1317 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_simulatedelayd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1687 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_skip_connection.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1896 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_slice_inferer.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10903 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_sliding_patch_wsi_dataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11961 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_sliding_window_hovernet_inference.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15505 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_sliding_window_inference.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9615 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_sliding_window_splitter.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7514 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_smartcachedataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6249 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_smooth_field.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6829 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_sobel_gradient.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7989 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_sobel_gradientd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8837 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_some_of.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14528 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_spacing.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6587 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_spacingd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7921 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_spatial_combine_transforms.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3653 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_spatial_crop.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2455 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_spatial_cropd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2209 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_spatial_pad.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1636 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_spatial_padd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9792 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_spatial_resample.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4920 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_spatial_resampled.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1571 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_split_channel.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2219 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_split_channeld.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1858 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_splitdim.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3815 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_splitdimd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2402 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_squeezedim.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3216 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_squeezedimd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2104 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_ssim_loss.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2895 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_ssim_metric.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2479 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_state_cacher.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3332 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_std_shift_intensity.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3145 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_std_shift_intensityd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1293 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_str2bool.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1232 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_str2list.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3081 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_subpixel_upsample.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21760 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_surface_dice.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6236 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_surface_distance.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3839 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_swin_unetr.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2442 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_synthetic.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4055 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_tciadataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6968 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_testtimeaugmentation.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2028 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_text_encoding.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5025 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_thread_buffer.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3458 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_threadcontainer.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1500 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_threshold_intensity.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2055 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_threshold_intensityd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2253 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_timedcall_dist.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1873 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_to_contiguous.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4580 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_to_cupy.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3061 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_to_cupyd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1290 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_to_device.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1357 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_to_deviced.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6851 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_to_from_meta_tensord.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3411 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_to_numpy.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2690 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_to_numpyd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2223 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_to_onehot.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1718 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_to_pil.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1829 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_to_pild.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2109 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_to_tensor.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2595 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_to_tensord.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4089 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_torchscript_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2613 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_torchvision.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6402 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_torchvision_fc_model.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2459 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_torchvisiond.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1895 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_traceable_transform.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1050 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_train_mode.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16832 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_trainable_bilateral.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21398 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_trainable_joint_bilateral.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3215 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_transchex.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1857 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_transform.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3164 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_transformerblock.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1352 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_transpose.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1884 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_transposed.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7738 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_tversky_loss.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5796 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_unet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5320 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_unetr.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6876 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_unetr_block.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2313 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_unified_focal_loss.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4649 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_upsample_block.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3038 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_utils_pytorch_numpy_unification.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3542 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_varautoencoder.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2795 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_varnet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2286 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_version_leq.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5575 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_video_datasets.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3088 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_vis_cam.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2484 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_vis_gradbased.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6880 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_vis_gradcam.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7166 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_vit.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5221 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_vitautoenc.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2627 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_vnet.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2666 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_vote_ensemble.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3622 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_vote_ensembled.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9146 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_warp.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2078 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_watershed.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2523 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_watershedd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1712 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_weight_init.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2194 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_weighted_random_sampler_dist.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3056 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_with_allow_missing_keys.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3026 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_write_metrics_reports.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8380 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_wsi_sliding_window_splitter.py
+-rw-r--r--   0 runner    (1001) docker     (123)    26104 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_wsireader.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10325 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_zarr_avg_merger.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2394 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_zipdataset.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4843 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_zoom.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3095 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_zoom_affine.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3475 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/tests/test_zoomd.py
+-rw-r--r--   0 runner    (1001) docker     (123)    81097 2023-07-23 02:21:52.000000 monai-weekly-1.3.dev2330/versioneer.py
```

### Comparing `monai-weekly-1.3.dev2329/LICENSE` & `monai-weekly-1.3.dev2330/LICENSE`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/PKG-INFO` & `monai-weekly-1.3.dev2330/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: monai-weekly
-Version: 1.3.dev2329
+Version: 1.3.dev2330
 Summary: AI Toolkit for Healthcare Imaging
 Home-page: https://monai.io/
 Author: MONAI Consortium
 Author-email: monai.contact@gmail.com
 License: Apache License 2.0
 Project-URL: Documentation, https://docs.monai.io/
 Project-URL: Bug Tracker, https://github.com/Project-MONAI/MONAI/issues
```

### Comparing `monai-weekly-1.3.dev2329/README.md` & `monai-weekly-1.3.dev2330/README.md`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/__init__.py` & `monai-weekly-1.3.dev2330/monai/__init__.py`

 * *Files 5% similar despite different names*

```diff
@@ -74,8 +74,8 @@
     "metrics",
     "networks",
     "optimizers",
     "transforms",
     "utils",
     "visualize",
 ]
-__commit_id__ = "dc1bc7704227044a4ea42fc1efac0224314c1791"
+__commit_id__ = "644c9e5d58082f442e3e8230fcf6ae1d6e8ee5b8"
```

### Comparing `monai-weekly-1.3.dev2329/monai/_extensions/__init__.py` & `monai-weekly-1.3.dev2330/monai/_extensions/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/_extensions/gmm/gmm.cpp` & `monai-weekly-1.3.dev2330/monai/_extensions/gmm/gmm.cpp`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/_extensions/gmm/gmm.h` & `monai-weekly-1.3.dev2330/monai/_extensions/gmm/gmm.h`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/_extensions/gmm/gmm_cpu.cpp` & `monai-weekly-1.3.dev2330/monai/_extensions/gmm/gmm_cpu.cpp`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/_extensions/gmm/gmm_cuda.cu` & `monai-weekly-1.3.dev2330/monai/_extensions/gmm/gmm_cuda.cu`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/_extensions/gmm/gmm_cuda_linalg.cuh` & `monai-weekly-1.3.dev2330/monai/_extensions/gmm/gmm_cuda_linalg.cuh`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/_extensions/loader.py` & `monai-weekly-1.3.dev2330/monai/_extensions/loader.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/__init__.py` & `monai-weekly-1.3.dev2330/monai/apps/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/auto3dseg/__init__.py` & `monai-weekly-1.3.dev2330/monai/apps/auto3dseg/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/auto3dseg/__main__.py` & `monai-weekly-1.3.dev2330/monai/apps/auto3dseg/__main__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/auto3dseg/auto_runner.py` & `monai-weekly-1.3.dev2330/monai/apps/auto3dseg/auto_runner.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/auto3dseg/bundle_gen.py` & `monai-weekly-1.3.dev2330/monai/apps/auto3dseg/bundle_gen.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/auto3dseg/data_analyzer.py` & `monai-weekly-1.3.dev2330/monai/apps/auto3dseg/data_analyzer.py`

 * *Files 3% similar despite different names*

```diff
@@ -66,15 +66,15 @@
         image_key: a string that user specify for the image. The DataAnalyzer will look it up in the
             datalist to locate the image files of the dataset.
         label_key: a string that user specify for the label. The DataAnalyzer will look it up in the
             datalist to locate the label files of the dataset. If label_key is NoneType or "None",
             the DataAnalyzer will skip looking for labels and all label-related operations.
         hist_bins: bins to compute histogram for each image channel.
         hist_range: ranges to compute histogram for each image channel.
-        fmt: format used to save the analysis results. Defaults to "yaml".
+        fmt: format used to save the analysis results. Currently support ``"json"`` and ``"yaml"``, defaults to "yaml".
         histogram_only: whether to only compute histograms. Defaults to False.
         extra_params: other optional arguments. Currently supported arguments are :
             'allowed_shape_difference' (default 5) can be used to change the default tolerance of
             the allowed shape differences between the image and label items. In case of shape mismatch below
             the tolerance, the label image will be resized to match the image using nearest interpolation.
 
 
@@ -160,14 +160,15 @@
             False if one of the selected key values is not constant across the dataset images.
 
         """
 
         constant_props = [result[DataStatsKeys.SUMMARY][DataStatsKeys.IMAGE_STATS][key] for key in keys]
         for prop in constant_props:
             if "stdev" in prop and np.any(prop["stdev"]):
+                logger.debug(f"summary image_stats {prop} has non-zero stdev {prop['stdev']}.")
                 return False
 
         return True
 
     def get_all_case_stats(self, key="training", transform_list=None):
         """
         Get all case stats. Caller of the DataAnalyser class. The function initiates multiple GPU or CPU processes of the internal
@@ -238,23 +239,24 @@
         n_cases = len(result_bycase[DataStatsKeys.BY_CASE])
         result[DataStatsKeys.SUMMARY] = summarizer.summarize(cast(list, result_bycase[DataStatsKeys.BY_CASE]))
         result[DataStatsKeys.SUMMARY]["n_cases"] = n_cases
         result_bycase[DataStatsKeys.SUMMARY] = result[DataStatsKeys.SUMMARY]
         if not self._check_data_uniformity([ImageStatsKeys.SPACING], result):
             logger.info("Data spacing is not completely uniform. MONAI transforms may provide unexpected result")
         if self.output_path:
+            logger.info(f"Writing data stats to {self.output_path}.")
             ConfigParser.export_config_file(
                 result, self.output_path, fmt=self.fmt, default_flow_style=None, sort_keys=False
             )
+            by_case_path = self.output_path.replace(f".{self.fmt}", f"_by_case.{self.fmt}")
+            if by_case_path == self.output_path:  # self.output_path not ended with self.fmt?
+                by_case_path += f".by_case.{self.fmt}"
+            logger.info(f"Writing by-case data stats to {by_case_path}, this may take a while.")
             ConfigParser.export_config_file(
-                result_bycase,
-                self.output_path.replace(".yaml", "_by_case.yaml"),
-                fmt=self.fmt,
-                default_flow_style=None,
-                sort_keys=False,
+                result_bycase, by_case_path, fmt=self.fmt, default_flow_style=None, sort_keys=False
             )
         # release memory
         if self.device.type == "cuda":
             # release unreferenced tensors to mitigate OOM
             # limitation: https://github.com/pytorch/pytorch/issues/12873#issuecomment-482916237
             torch.cuda.empty_cache()
         result[DataStatsKeys.BY_CASE] = result_bycase[DataStatsKeys.BY_CASE]
```

### Comparing `monai-weekly-1.3.dev2329/monai/apps/auto3dseg/ensemble_builder.py` & `monai-weekly-1.3.dev2330/monai/apps/auto3dseg/ensemble_builder.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/auto3dseg/hpo_gen.py` & `monai-weekly-1.3.dev2330/monai/apps/auto3dseg/hpo_gen.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/auto3dseg/transforms.py` & `monai-weekly-1.3.dev2330/monai/apps/auto3dseg/transforms.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/auto3dseg/utils.py` & `monai-weekly-1.3.dev2330/monai/apps/auto3dseg/utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/datasets.py` & `monai-weekly-1.3.dev2330/monai/apps/datasets.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/deepedit/__init__.py` & `monai-weekly-1.3.dev2330/monai/apps/deepedit/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/deepedit/interaction.py` & `monai-weekly-1.3.dev2330/monai/apps/deepedit/interaction.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/deepedit/transforms.py` & `monai-weekly-1.3.dev2330/monai/apps/deepedit/transforms.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/deepgrow/__init__.py` & `monai-weekly-1.3.dev2330/monai/apps/deepgrow/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/deepgrow/dataset.py` & `monai-weekly-1.3.dev2330/monai/apps/deepgrow/dataset.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/deepgrow/interaction.py` & `monai-weekly-1.3.dev2330/monai/apps/deepgrow/interaction.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/deepgrow/transforms.py` & `monai-weekly-1.3.dev2330/monai/apps/deepgrow/transforms.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/detection/__init__.py` & `monai-weekly-1.3.dev2330/monai/apps/detection/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/detection/metrics/__init__.py` & `monai-weekly-1.3.dev2330/monai/apps/detection/metrics/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/detection/metrics/coco.py` & `monai-weekly-1.3.dev2330/monai/apps/detection/metrics/coco.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/detection/metrics/matching.py` & `monai-weekly-1.3.dev2330/monai/apps/detection/metrics/matching.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/detection/networks/__init__.py` & `monai-weekly-1.3.dev2330/monai/apps/detection/networks/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/detection/networks/retinanet_detector.py` & `monai-weekly-1.3.dev2330/monai/apps/detection/networks/retinanet_detector.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/detection/networks/retinanet_network.py` & `monai-weekly-1.3.dev2330/monai/apps/detection/networks/retinanet_network.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/detection/transforms/__init__.py` & `monai-weekly-1.3.dev2330/monai/apps/detection/transforms/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/detection/transforms/array.py` & `monai-weekly-1.3.dev2330/monai/apps/detection/transforms/array.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/detection/transforms/box_ops.py` & `monai-weekly-1.3.dev2330/monai/apps/detection/transforms/box_ops.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/detection/transforms/dictionary.py` & `monai-weekly-1.3.dev2330/monai/apps/detection/transforms/dictionary.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/detection/utils/ATSS_matcher.py` & `monai-weekly-1.3.dev2330/monai/apps/detection/utils/ATSS_matcher.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/detection/utils/__init__.py` & `monai-weekly-1.3.dev2330/monai/apps/detection/utils/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/detection/utils/anchor_utils.py` & `monai-weekly-1.3.dev2330/monai/apps/detection/utils/anchor_utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/detection/utils/box_coder.py` & `monai-weekly-1.3.dev2330/monai/apps/detection/utils/box_coder.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/detection/utils/box_selector.py` & `monai-weekly-1.3.dev2330/monai/apps/detection/utils/box_selector.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/detection/utils/detector_utils.py` & `monai-weekly-1.3.dev2330/monai/apps/detection/utils/detector_utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/detection/utils/hard_negative_sampler.py` & `monai-weekly-1.3.dev2330/monai/apps/detection/utils/hard_negative_sampler.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/detection/utils/predict_utils.py` & `monai-weekly-1.3.dev2330/monai/apps/detection/utils/predict_utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/mmars/__init__.py` & `monai-weekly-1.3.dev2330/monai/apps/mmars/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/mmars/mmars.py` & `monai-weekly-1.3.dev2330/monai/apps/mmars/mmars.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/mmars/model_desc.py` & `monai-weekly-1.3.dev2330/monai/apps/mmars/model_desc.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/nnunet/__init__.py` & `monai-weekly-1.3.dev2330/monai/apps/nnunet/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/nnunet/__main__.py` & `monai-weekly-1.3.dev2330/monai/apps/nnunet/__main__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/nnunet/nnunetv2_runner.py` & `monai-weekly-1.3.dev2330/monai/apps/nnunet/nnunetv2_runner.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/nnunet/utils.py` & `monai-weekly-1.3.dev2330/monai/apps/nnunet/utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/nuclick/__init__.py` & `monai-weekly-1.3.dev2330/monai/apps/nuclick/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/nuclick/transforms.py` & `monai-weekly-1.3.dev2330/monai/apps/nuclick/transforms.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/pathology/__init__.py` & `monai-weekly-1.3.dev2330/monai/apps/pathology/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/pathology/engines/__init__.py` & `monai-weekly-1.3.dev2330/monai/apps/pathology/engines/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/pathology/engines/utils.py` & `monai-weekly-1.3.dev2330/monai/apps/pathology/engines/utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/pathology/handlers/__init__.py` & `monai-weekly-1.3.dev2330/monai/apps/pathology/handlers/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/pathology/handlers/utils.py` & `monai-weekly-1.3.dev2330/monai/apps/pathology/handlers/utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/pathology/inferers/__init__.py` & `monai-weekly-1.3.dev2330/monai/apps/pathology/inferers/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/pathology/inferers/inferer.py` & `monai-weekly-1.3.dev2330/monai/apps/pathology/inferers/inferer.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/pathology/losses/__init__.py` & `monai-weekly-1.3.dev2330/monai/apps/pathology/losses/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/pathology/losses/hovernet_loss.py` & `monai-weekly-1.3.dev2330/monai/apps/pathology/losses/hovernet_loss.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/pathology/metrics/__init__.py` & `monai-weekly-1.3.dev2330/monai/apps/pathology/metrics/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/pathology/metrics/lesion_froc.py` & `monai-weekly-1.3.dev2330/monai/apps/pathology/metrics/lesion_froc.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/pathology/transforms/__init__.py` & `monai-weekly-1.3.dev2330/monai/apps/pathology/transforms/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/pathology/transforms/post/__init__.py` & `monai-weekly-1.3.dev2330/monai/apps/pathology/transforms/post/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/pathology/transforms/post/array.py` & `monai-weekly-1.3.dev2330/monai/apps/pathology/transforms/post/array.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/pathology/transforms/post/dictionary.py` & `monai-weekly-1.3.dev2330/monai/apps/pathology/transforms/post/dictionary.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/pathology/transforms/stain/__init__.py` & `monai-weekly-1.3.dev2330/monai/apps/pathology/transforms/stain/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/pathology/transforms/stain/array.py` & `monai-weekly-1.3.dev2330/monai/apps/pathology/transforms/stain/array.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/pathology/transforms/stain/dictionary.py` & `monai-weekly-1.3.dev2330/monai/apps/pathology/transforms/stain/dictionary.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/pathology/utils.py` & `monai-weekly-1.3.dev2330/monai/apps/pathology/utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/reconstruction/__init__.py` & `monai-weekly-1.3.dev2330/monai/apps/reconstruction/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/reconstruction/complex_utils.py` & `monai-weekly-1.3.dev2330/monai/apps/reconstruction/complex_utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/reconstruction/fastmri_reader.py` & `monai-weekly-1.3.dev2330/monai/apps/reconstruction/fastmri_reader.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/reconstruction/mri_utils.py` & `monai-weekly-1.3.dev2330/monai/apps/reconstruction/mri_utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/reconstruction/networks/__init__.py` & `monai-weekly-1.3.dev2330/monai/apps/reconstruction/networks/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/reconstruction/networks/blocks/__init__.py` & `monai-weekly-1.3.dev2330/monai/apps/reconstruction/networks/blocks/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/reconstruction/networks/blocks/varnetblock.py` & `monai-weekly-1.3.dev2330/monai/apps/reconstruction/networks/blocks/varnetblock.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/reconstruction/networks/nets/__init__.py` & `monai-weekly-1.3.dev2330/monai/apps/reconstruction/networks/nets/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/reconstruction/networks/nets/coil_sensitivity_model.py` & `monai-weekly-1.3.dev2330/monai/apps/reconstruction/networks/nets/coil_sensitivity_model.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/reconstruction/networks/nets/complex_unet.py` & `monai-weekly-1.3.dev2330/monai/apps/reconstruction/networks/nets/complex_unet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/reconstruction/networks/nets/utils.py` & `monai-weekly-1.3.dev2330/monai/apps/reconstruction/networks/nets/utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/reconstruction/networks/nets/varnet.py` & `monai-weekly-1.3.dev2330/monai/apps/reconstruction/networks/nets/varnet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/reconstruction/transforms/__init__.py` & `monai-weekly-1.3.dev2330/monai/apps/reconstruction/transforms/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/reconstruction/transforms/array.py` & `monai-weekly-1.3.dev2330/monai/apps/reconstruction/transforms/array.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/reconstruction/transforms/dictionary.py` & `monai-weekly-1.3.dev2330/monai/apps/reconstruction/transforms/dictionary.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/tcia/__init__.py` & `monai-weekly-1.3.dev2330/monai/apps/tcia/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/tcia/label_desc.py` & `monai-weekly-1.3.dev2330/monai/apps/tcia/label_desc.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/tcia/utils.py` & `monai-weekly-1.3.dev2330/monai/apps/tcia/utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/apps/utils.py` & `monai-weekly-1.3.dev2330/monai/apps/utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/auto3dseg/__init__.py` & `monai-weekly-1.3.dev2330/monai/auto3dseg/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/auto3dseg/algo_gen.py` & `monai-weekly-1.3.dev2330/monai/auto3dseg/algo_gen.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/auto3dseg/analyzer.py` & `monai-weekly-1.3.dev2330/monai/auto3dseg/analyzer.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/auto3dseg/operations.py` & `monai-weekly-1.3.dev2330/monai/auto3dseg/operations.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/auto3dseg/seg_summarizer.py` & `monai-weekly-1.3.dev2330/monai/auto3dseg/seg_summarizer.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/auto3dseg/utils.py` & `monai-weekly-1.3.dev2330/monai/auto3dseg/utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/bundle/__init__.py` & `monai-weekly-1.3.dev2330/monai/bundle/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/bundle/__main__.py` & `monai-weekly-1.3.dev2330/monai/bundle/__main__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/bundle/config_item.py` & `monai-weekly-1.3.dev2330/monai/bundle/config_item.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/bundle/config_parser.py` & `monai-weekly-1.3.dev2330/monai/bundle/config_parser.py`

 * *Files 0% similar despite different names*

```diff
@@ -434,20 +434,20 @@
             config: source config content to export.
             filepath: target file path to save.
             fmt: format of config content, currently support ``"json"`` and ``"yaml"``.
             kwargs: other arguments for ``json.dump`` or ``yaml.safe_dump``, depends on the file format.
 
         """
         _filepath: str = str(Path(filepath))
-        writer = look_up_option(fmt.lower(), {"json", "yaml"})
+        writer = look_up_option(fmt.lower(), {"json", "yaml", "yml"})
         with open(_filepath, "w") as f:
             if writer == "json":
                 json.dump(config, f, **kwargs)
                 return
-            if writer == "yaml":
+            if writer == "yaml" or writer == "yml":
                 return yaml.safe_dump(config, f, **kwargs)
             raise ValueError(f"only support JSON or YAML config file so far, got {writer}.")
 
     @classmethod
     def split_path_id(cls, src: str) -> tuple[str, str]:
         """
         Split `src` string into two parts: a config file path and component id.
```

### Comparing `monai-weekly-1.3.dev2329/monai/bundle/properties.py` & `monai-weekly-1.3.dev2330/monai/bundle/properties.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/bundle/reference_resolver.py` & `monai-weekly-1.3.dev2330/monai/bundle/reference_resolver.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/bundle/scripts.py` & `monai-weekly-1.3.dev2330/monai/bundle/scripts.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/bundle/utils.py` & `monai-weekly-1.3.dev2330/monai/bundle/utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/bundle/workflows.py` & `monai-weekly-1.3.dev2330/monai/bundle/workflows.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/config/__init__.py` & `monai-weekly-1.3.dev2330/monai/config/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/config/deviceconfig.py` & `monai-weekly-1.3.dev2330/monai/config/deviceconfig.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/config/type_definitions.py` & `monai-weekly-1.3.dev2330/monai/config/type_definitions.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/data/__init__.py` & `monai-weekly-1.3.dev2330/monai/data/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/data/box_utils.py` & `monai-weekly-1.3.dev2330/monai/data/box_utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/data/csv_saver.py` & `monai-weekly-1.3.dev2330/monai/data/csv_saver.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/data/dataloader.py` & `monai-weekly-1.3.dev2330/monai/data/dataloader.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/data/dataset.py` & `monai-weekly-1.3.dev2330/monai/data/dataset.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/data/dataset_summary.py` & `monai-weekly-1.3.dev2330/monai/data/dataset_summary.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/data/decathlon_datalist.py` & `monai-weekly-1.3.dev2330/monai/data/decathlon_datalist.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/data/fft_utils.py` & `monai-weekly-1.3.dev2330/monai/data/fft_utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/data/folder_layout.py` & `monai-weekly-1.3.dev2330/monai/data/folder_layout.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/data/grid_dataset.py` & `monai-weekly-1.3.dev2330/monai/data/grid_dataset.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/data/image_dataset.py` & `monai-weekly-1.3.dev2330/monai/data/image_dataset.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/data/image_reader.py` & `monai-weekly-1.3.dev2330/monai/data/image_reader.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/data/image_writer.py` & `monai-weekly-1.3.dev2330/monai/data/image_writer.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/data/iterable_dataset.py` & `monai-weekly-1.3.dev2330/monai/data/iterable_dataset.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/data/itk_torch_bridge.py` & `monai-weekly-1.3.dev2330/monai/data/itk_torch_bridge.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/data/meta_obj.py` & `monai-weekly-1.3.dev2330/monai/data/meta_obj.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/data/meta_tensor.py` & `monai-weekly-1.3.dev2330/monai/data/meta_tensor.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/data/samplers.py` & `monai-weekly-1.3.dev2330/monai/data/samplers.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/data/synthetic.py` & `monai-weekly-1.3.dev2330/monai/data/synthetic.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/data/test_time_augmentation.py` & `monai-weekly-1.3.dev2330/monai/data/test_time_augmentation.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/data/thread_buffer.py` & `monai-weekly-1.3.dev2330/monai/data/thread_buffer.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/data/torchscript_utils.py` & `monai-weekly-1.3.dev2330/monai/data/torchscript_utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/data/utils.py` & `monai-weekly-1.3.dev2330/monai/data/utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/data/video_dataset.py` & `monai-weekly-1.3.dev2330/monai/data/video_dataset.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/data/wsi_datasets.py` & `monai-weekly-1.3.dev2330/monai/data/wsi_datasets.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/data/wsi_reader.py` & `monai-weekly-1.3.dev2330/monai/data/wsi_reader.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/engines/__init__.py` & `monai-weekly-1.3.dev2330/monai/engines/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/engines/evaluator.py` & `monai-weekly-1.3.dev2330/monai/engines/evaluator.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/engines/multi_gpu_supervised_trainer.py` & `monai-weekly-1.3.dev2330/monai/engines/multi_gpu_supervised_trainer.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/engines/trainer.py` & `monai-weekly-1.3.dev2330/monai/engines/trainer.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/engines/utils.py` & `monai-weekly-1.3.dev2330/monai/engines/utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/engines/workflow.py` & `monai-weekly-1.3.dev2330/monai/engines/workflow.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/fl/__init__.py` & `monai-weekly-1.3.dev2330/monai/fl/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/fl/client/__init__.py` & `monai-weekly-1.3.dev2330/monai/fl/client/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/fl/client/client_algo.py` & `monai-weekly-1.3.dev2330/monai/fl/client/client_algo.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/fl/client/monai_algo.py` & `monai-weekly-1.3.dev2330/monai/fl/client/monai_algo.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/fl/utils/__init__.py` & `monai-weekly-1.3.dev2330/monai/fl/utils/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/fl/utils/constants.py` & `monai-weekly-1.3.dev2330/monai/fl/utils/constants.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/fl/utils/exchange_object.py` & `monai-weekly-1.3.dev2330/monai/fl/utils/exchange_object.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/fl/utils/filters.py` & `monai-weekly-1.3.dev2330/monai/fl/utils/filters.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/__init__.py` & `monai-weekly-1.3.dev2330/monai/handlers/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/checkpoint_loader.py` & `monai-weekly-1.3.dev2330/monai/handlers/checkpoint_loader.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/checkpoint_saver.py` & `monai-weekly-1.3.dev2330/monai/handlers/checkpoint_saver.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/classification_saver.py` & `monai-weekly-1.3.dev2330/monai/handlers/classification_saver.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/clearml_handlers.py` & `monai-weekly-1.3.dev2330/monai/handlers/clearml_handlers.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/confusion_matrix.py` & `monai-weekly-1.3.dev2330/monai/handlers/confusion_matrix.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/decollate_batch.py` & `monai-weekly-1.3.dev2330/monai/handlers/decollate_batch.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/earlystop_handler.py` & `monai-weekly-1.3.dev2330/monai/handlers/earlystop_handler.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/garbage_collector.py` & `monai-weekly-1.3.dev2330/monai/handlers/garbage_collector.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/hausdorff_distance.py` & `monai-weekly-1.3.dev2330/monai/handlers/hausdorff_distance.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/ignite_metric.py` & `monai-weekly-1.3.dev2330/monai/handlers/ignite_metric.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/logfile_handler.py` & `monai-weekly-1.3.dev2330/monai/handlers/logfile_handler.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/lr_schedule_handler.py` & `monai-weekly-1.3.dev2330/monai/handlers/lr_schedule_handler.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/mean_dice.py` & `monai-weekly-1.3.dev2330/monai/handlers/mean_dice.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/mean_iou.py` & `monai-weekly-1.3.dev2330/monai/handlers/mean_iou.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/metric_logger.py` & `monai-weekly-1.3.dev2330/monai/handlers/metric_logger.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/metrics_reloaded_handler.py` & `monai-weekly-1.3.dev2330/monai/handlers/metrics_reloaded_handler.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/metrics_saver.py` & `monai-weekly-1.3.dev2330/monai/handlers/metrics_saver.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/mlflow_handler.py` & `monai-weekly-1.3.dev2330/monai/handlers/mlflow_handler.py`

 * *Files 20% similar despite different names*

```diff
@@ -9,28 +9,32 @@
 # See the License for the specific language governing permissions and
 # limitations under the License.
 
 from __future__ import annotations
 
 import os
 import time
-from collections.abc import Callable, Sequence
+import warnings
+from collections.abc import Callable, Mapping, Sequence
 from pathlib import Path
 from typing import TYPE_CHECKING, Any
 
 import torch
+from torch.utils.data import Dataset
 
 from monai.config import IgniteInfo
-from monai.utils import ensure_tuple, min_version, optional_import
+from monai.utils import CommonKeys, ensure_tuple, min_version, optional_import
 
 Events, _ = optional_import("ignite.engine", IgniteInfo.OPT_IMPORT_VERSION, min_version, "Events")
 mlflow, _ = optional_import("mlflow", descriptor="Please install mlflow before using MLFlowHandler.")
 mlflow.entities, _ = optional_import(
     "mlflow.entities", descriptor="Please install mlflow.entities before using MLFlowHandler."
 )
+pandas, _ = optional_import("pandas", descriptor="Please install pandas for recording the dataset.")
+tqdm, _ = optional_import("tqdm", "4.47.0", min_version, "tqdm")
 
 if TYPE_CHECKING:
     from ignite.engine import Engine
 else:
     Engine, _ = optional_import(
         "ignite.engine", IgniteInfo.OPT_IMPORT_VERSION, min_version, "Engine", as_type="decorator"
     )
@@ -68,14 +72,22 @@
         epoch_log: whether to log data to MLFlow when epoch completed, default to `True`.
             ``epoch_log`` can be also a function and it will be interpreted as an event filter.
             See ``iteration_log`` argument for more details.
         epoch_logger: customized callable logger for epoch level logging with MLFlow.
             Must accept parameter "engine", use default logger if None.
         iteration_logger: customized callable logger for iteration level logging with MLFlow.
             Must accept parameter "engine", use default logger if None.
+        dataset_logger: customized callable logger to log the dataset information with MLFlow.
+            Must accept parameter "dataset_dict", use default logger if None.
+        dataset_dict: a dictionary in which the key is the name of the dataset and the value is a PyTorch
+            dataset, that needs to be recorded. This arg is only useful when MLFlow version >= 2.4.0.
+            For more details about how to log data with MLFlow, please go to the website:
+            https://mlflow.org/docs/latest/python_api/mlflow.data.html.
+        dataset_keys: a key or a collection of keys to indicate contents in the dataset that
+            need to be stored by MLFlow.
         output_transform: a callable that is used to transform the
             ``ignite.engine.state.output`` into a scalar to track, or a dictionary of {key: scalar}.
             By default this value logging happens when every iteration completed.
             The default behavior is to track loss from output[0] as output is a decollated list
             and we replicated loss value for every item of the decollated list.
             `engine.state` and `output_transform` inherit from the ignite concept:
             https://pytorch-ignite.ai/concepts/03-state/, explanation and usage example are in the tutorial:
@@ -107,14 +119,17 @@
     def __init__(
         self,
         tracking_uri: str | None = None,
         iteration_log: bool | Callable[[Engine, int], bool] = True,
         epoch_log: bool | Callable[[Engine, int], bool] = True,
         epoch_logger: Callable[[Engine], Any] | None = None,
         iteration_logger: Callable[[Engine], Any] | None = None,
+        dataset_logger: Callable[[Mapping[str, Dataset]], Any] | None = None,
+        dataset_dict: Mapping[str, Dataset] | None = None,
+        dataset_keys: str = CommonKeys.IMAGE,
         output_transform: Callable = lambda x: x[0],
         global_epoch_transform: Callable = lambda x: x,
         state_attributes: Sequence[str] | None = None,
         tag_name: str = DEFAULT_TAG,
         experiment_name: str = "monai_experiment",
         run_name: str | None = None,
         experiment_param: dict | None = None,
@@ -122,28 +137,31 @@
         optimizer_param_names: str | Sequence[str] = "lr",
         close_on_complete: bool = False,
     ) -> None:
         self.iteration_log = iteration_log
         self.epoch_log = epoch_log
         self.epoch_logger = epoch_logger
         self.iteration_logger = iteration_logger
+        self.dataset_logger = dataset_logger
         self.output_transform = output_transform
         self.global_epoch_transform = global_epoch_transform
         self.state_attributes = state_attributes
         self.tag_name = tag_name
         self.experiment_name = experiment_name
         self.run_name = run_name
         self.experiment_param = experiment_param
         self.artifacts = ensure_tuple(artifacts)
         self.optimizer_param_names = ensure_tuple(optimizer_param_names)
         self.client = mlflow.MlflowClient(tracking_uri=tracking_uri if tracking_uri else None)
         self.run_finish_status = mlflow.entities.RunStatus.to_string(mlflow.entities.RunStatus.FINISHED)
         self.close_on_complete = close_on_complete
         self.experiment = None
         self.cur_run = None
+        self.dataset_dict = dataset_dict
+        self.dataset_keys = ensure_tuple(dataset_keys)
 
     def _delete_exist_param_in_dict(self, param_dict: dict) -> None:
         """
         Delete parameters in given dict, if they are already logged by current mlflow run.
 
         Args:
             param_dict: parameter dict to be logged to mlflow.
@@ -206,26 +224,61 @@
         if self.experiment_param:
             self._log_params(self.experiment_param)
 
         attrs = {attr: getattr(engine.state, attr, None) for attr in self.default_tracking_params}
         self._delete_exist_param_in_dict(attrs)
         self._log_params(attrs)
 
+        if self.dataset_logger:
+            self.dataset_logger(self.dataset_dict)
+        else:
+            self._default_dataset_log(self.dataset_dict)
+
     def _set_experiment(self):
         experiment = self.experiment
         if not experiment:
             experiment = self.client.get_experiment_by_name(self.experiment_name)
             if not experiment:
                 experiment_id = self.client.create_experiment(self.experiment_name)
                 experiment = self.client.get_experiment(experiment_id)
 
         if experiment.lifecycle_stage != mlflow.entities.LifecycleStage.ACTIVE:
             raise ValueError(f"Cannot set a deleted experiment '{self.experiment_name}' as the active experiment")
         self.experiment = experiment
 
+    @staticmethod
+    def _get_pandas_dataset_info(pandas_dataset):
+        dataset_name = pandas_dataset.name
+        return {
+            f"{dataset_name}_digest": pandas_dataset.digest,
+            f"{dataset_name}_samples": pandas_dataset.profile["num_rows"],
+        }
+
+    def _log_dataset(self, sample_dict: dict[str, Any], context: str = "train") -> None:
+        if not self.cur_run:
+            raise ValueError("Current Run is not Active to log the dataset")
+
+        # Need to update the self.cur_run to sync the dataset log, otherwise the `inputs` info will be out-of-date.
+        self.cur_run = self.client.get_run(self.cur_run.info.run_id)
+        logged_set = [x for x in self.cur_run.inputs.dataset_inputs if x.dataset.name.startswith(context)]
+        # In case there are datasets with the same name.
+        dataset_count = str(len(logged_set))
+        dataset_name = f"{context}_dataset_{dataset_count}"
+        sample_df = pandas.DataFrame(sample_dict)
+        dataset = mlflow.data.from_pandas(sample_df, name=dataset_name)
+        exist_dataset_list = list(
+            filter(lambda x: x.dataset.digest == dataset.digest, self.cur_run.inputs.dataset_inputs)
+        )
+
+        if not len(exist_dataset_list):
+            datasets = [mlflow.entities.DatasetInput(dataset._to_mlflow_entity())]
+            self.client.log_inputs(run_id=self.cur_run.info.run_id, datasets=datasets)
+            dataset_info = MLFlowHandler._get_pandas_dataset_info(dataset)
+            self._log_params(dataset_info)
+
     def _log_params(self, params: dict[str, Any]) -> None:
         if not self.cur_run:
             raise ValueError("Current Run is not Active to log params")
         params_arr = [mlflow.entities.Param(key, str(value)) for key, value in params.items()]
         self.client.log_batch(run_id=self.cur_run.info.run_id, metrics=[], params=params_arr, tags=[])
 
     def _log_metrics(self, metrics: dict[str, Any], step: int | None = None) -> None:
@@ -348,7 +401,65 @@
             cur_optimizer = engine.optimizer
             for param_name in self.optimizer_param_names:
                 params = {
                     f"{param_name} group_{i}": float(param_group[param_name])
                     for i, param_group in enumerate(cur_optimizer.param_groups)
                 }
                 self._log_metrics(params, step=engine.state.iteration)
+
+    def _default_dataset_log(self, dataset_dict: Mapping[str, Dataset] | None) -> None:
+        """
+        Execute dataset log operation based on the input dataset_dict. The dataset_dict should have a format
+        like:
+            {
+                "dataset_name0": dataset0,
+                "dataset_name1": dataset1,
+                ......
+            }
+        The keys stand for names of datasets, which will be logged as prefixes of dataset names in MLFlow.
+        The values are PyTorch datasets from which sample names are abstracted to build a Pandas DataFrame.
+        If the input dataset_dict is None, this function will directly return and do nothing.
+
+        To use this function, every sample in the input datasets must contain keys specified by the `dataset_keys`
+        parameter.
+        This function will log a PandasDataset to MLFlow inputs, generated from the Pandas DataFrame.
+        For more details about PandasDataset, please refer to this link:
+        https://mlflow.org/docs/latest/python_api/mlflow.data.html#mlflow.data.pandas_dataset.PandasDataset
+
+        Please note that it may take a while to record the dataset if it has too many samples.
+
+        Args:
+            dataset_dict: a dictionary in which the key is the name of the dataset and the value is a PyTorch
+                dataset, that needs to be recorded.
+
+        """
+
+        if dataset_dict is None:
+            return
+        elif len(dataset_dict) == 0:
+            warnings.warn("There is no dataset to log!")
+
+        # Log datasets to MLFlow one by one.
+        for dataset_type, dataset in dataset_dict.items():
+            if dataset is None:
+                raise AttributeError(f"The {dataset_type} dataset of is None. Cannot record it by MLFlow.")
+
+            sample_dict: dict[str, list[str]] = {}
+            dataset_samples = getattr(dataset, "data", [])
+            for sample in tqdm(dataset_samples, f"Recording the {dataset_type} dataset"):
+                for key in self.dataset_keys:
+                    if key not in sample_dict:
+                        sample_dict[key] = []
+
+                    if key in sample:
+                        value_to_log = sample[key]
+                    else:
+                        raise KeyError(f"Unexpect key '{key}' in the sample.")
+
+                    if not isinstance(value_to_log, str):
+                        warnings.warn(
+                            f"Expected type string, got type {type(value_to_log)} of the {key} name."
+                            "May log an empty dataset in MLFlow"
+                        )
+                    else:
+                        sample_dict[key].append(value_to_log)
+            self._log_dataset(sample_dict, dataset_type)
```

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/nvtx_handlers.py` & `monai-weekly-1.3.dev2330/monai/handlers/nvtx_handlers.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/panoptic_quality.py` & `monai-weekly-1.3.dev2330/monai/handlers/panoptic_quality.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/parameter_scheduler.py` & `monai-weekly-1.3.dev2330/monai/handlers/parameter_scheduler.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/postprocessing.py` & `monai-weekly-1.3.dev2330/monai/handlers/postprocessing.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/probability_maps.py` & `monai-weekly-1.3.dev2330/monai/handlers/probability_maps.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/regression_metrics.py` & `monai-weekly-1.3.dev2330/monai/handlers/regression_metrics.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/roc_auc.py` & `monai-weekly-1.3.dev2330/monai/handlers/roc_auc.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/smartcache_handler.py` & `monai-weekly-1.3.dev2330/monai/handlers/smartcache_handler.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/stats_handler.py` & `monai-weekly-1.3.dev2330/monai/handlers/stats_handler.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/surface_distance.py` & `monai-weekly-1.3.dev2330/monai/handlers/surface_distance.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/tensorboard_handlers.py` & `monai-weekly-1.3.dev2330/monai/handlers/tensorboard_handlers.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/utils.py` & `monai-weekly-1.3.dev2330/monai/handlers/utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/handlers/validation_handler.py` & `monai-weekly-1.3.dev2330/monai/handlers/validation_handler.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/inferers/__init__.py` & `monai-weekly-1.3.dev2330/monai/inferers/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/inferers/inferer.py` & `monai-weekly-1.3.dev2330/monai/inferers/inferer.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/inferers/merger.py` & `monai-weekly-1.3.dev2330/monai/inferers/merger.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/inferers/splitter.py` & `monai-weekly-1.3.dev2330/monai/inferers/splitter.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/inferers/utils.py` & `monai-weekly-1.3.dev2330/monai/inferers/utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/losses/__init__.py` & `monai-weekly-1.3.dev2330/monai/losses/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/losses/contrastive.py` & `monai-weekly-1.3.dev2330/monai/losses/contrastive.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/losses/deform.py` & `monai-weekly-1.3.dev2330/monai/losses/deform.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/losses/dice.py` & `monai-weekly-1.3.dev2330/monai/losses/dice.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/losses/ds_loss.py` & `monai-weekly-1.3.dev2330/monai/losses/ds_loss.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/losses/focal_loss.py` & `monai-weekly-1.3.dev2330/monai/losses/focal_loss.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/losses/giou_loss.py` & `monai-weekly-1.3.dev2330/monai/losses/giou_loss.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/losses/image_dissimilarity.py` & `monai-weekly-1.3.dev2330/monai/losses/image_dissimilarity.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/losses/multi_scale.py` & `monai-weekly-1.3.dev2330/monai/losses/multi_scale.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/losses/spatial_mask.py` & `monai-weekly-1.3.dev2330/monai/losses/spatial_mask.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/losses/ssim_loss.py` & `monai-weekly-1.3.dev2330/monai/losses/ssim_loss.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/losses/tversky.py` & `monai-weekly-1.3.dev2330/monai/losses/tversky.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/losses/unified_focal_loss.py` & `monai-weekly-1.3.dev2330/monai/losses/unified_focal_loss.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/metrics/__init__.py` & `monai-weekly-1.3.dev2330/monai/metrics/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/metrics/active_learning_metrics.py` & `monai-weekly-1.3.dev2330/monai/metrics/active_learning_metrics.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/metrics/confusion_matrix.py` & `monai-weekly-1.3.dev2330/monai/metrics/confusion_matrix.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/metrics/cumulative_average.py` & `monai-weekly-1.3.dev2330/monai/metrics/cumulative_average.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/metrics/f_beta_score.py` & `monai-weekly-1.3.dev2330/monai/metrics/f_beta_score.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/metrics/froc.py` & `monai-weekly-1.3.dev2330/monai/metrics/froc.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/metrics/generalized_dice.py` & `monai-weekly-1.3.dev2330/monai/metrics/generalized_dice.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/metrics/hausdorff_distance.py` & `monai-weekly-1.3.dev2330/monai/metrics/hausdorff_distance.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/metrics/loss_metric.py` & `monai-weekly-1.3.dev2330/monai/metrics/loss_metric.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/metrics/meandice.py` & `monai-weekly-1.3.dev2330/monai/metrics/meandice.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/metrics/meaniou.py` & `monai-weekly-1.3.dev2330/monai/metrics/meaniou.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/metrics/metric.py` & `monai-weekly-1.3.dev2330/monai/metrics/metric.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/metrics/panoptic_quality.py` & `monai-weekly-1.3.dev2330/monai/metrics/panoptic_quality.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/metrics/regression.py` & `monai-weekly-1.3.dev2330/monai/metrics/regression.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/metrics/rocauc.py` & `monai-weekly-1.3.dev2330/monai/metrics/rocauc.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/metrics/surface_dice.py` & `monai-weekly-1.3.dev2330/monai/metrics/surface_dice.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/metrics/surface_distance.py` & `monai-weekly-1.3.dev2330/monai/metrics/surface_distance.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/metrics/utils.py` & `monai-weekly-1.3.dev2330/monai/metrics/utils.py`

 * *Files 0% similar despite different names*

```diff
@@ -172,15 +172,15 @@
             return (pred, gt) if spacing is None else (pred, gt, pred, gt)  # type: ignore
         channel_first = [seg_pred[None], seg_gt[None], or_vol[None]]
         if spacing is None:  # cpu only erosion
             seg_pred, seg_gt, or_vol = convert_to_tensor(channel_first, device="cpu", dtype=bool)
         else:  # pytorch subvoxel, maybe on gpu, but croppad boolean values on GPU is not supported
             seg_pred, seg_gt, or_vol = convert_to_tensor(channel_first, dtype=torch.float16)
         cropper = CropForegroundD(
-            ["pred", "gt"], source_key="src", margin=1, allow_smaller=True, start_coord_key=None, end_coord_key=None
+            ["pred", "gt"], source_key="src", margin=1, allow_smaller=False, start_coord_key=None, end_coord_key=None
         )
         cropped = cropper({"pred": seg_pred, "gt": seg_gt, "src": or_vol})  # type: ignore
         seg_pred, seg_gt = cropped["pred"][0], cropped["gt"][0]
 
     if spacing is None:  # Do binary erosion and use XOR to get edges
         seg_pred, seg_gt = convert_to_numpy([seg_pred, seg_gt], dtype=bool)
         edges_pred = binary_erosion(seg_pred) ^ seg_pred
```

### Comparing `monai-weekly-1.3.dev2329/monai/metrics/wrapper.py` & `monai-weekly-1.3.dev2330/monai/metrics/wrapper.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/__init__.py` & `monai-weekly-1.3.dev2330/monai/networks/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/blocks/__init__.py` & `monai-weekly-1.3.dev2330/monai/networks/blocks/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/blocks/acti_norm.py` & `monai-weekly-1.3.dev2330/monai/networks/blocks/acti_norm.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/blocks/activation.py` & `monai-weekly-1.3.dev2330/monai/networks/blocks/activation.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/blocks/aspp.py` & `monai-weekly-1.3.dev2330/monai/networks/blocks/aspp.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/blocks/backbone_fpn_utils.py` & `monai-weekly-1.3.dev2330/monai/networks/blocks/backbone_fpn_utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/blocks/convolutions.py` & `monai-weekly-1.3.dev2330/monai/networks/blocks/convolutions.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/blocks/crf.py` & `monai-weekly-1.3.dev2330/monai/networks/blocks/crf.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/blocks/denseblock.py` & `monai-weekly-1.3.dev2330/monai/networks/blocks/denseblock.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/blocks/dints_block.py` & `monai-weekly-1.3.dev2330/monai/networks/blocks/dints_block.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/blocks/downsample.py` & `monai-weekly-1.3.dev2330/monai/networks/blocks/downsample.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/blocks/dynunet_block.py` & `monai-weekly-1.3.dev2330/monai/networks/blocks/dynunet_block.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/blocks/encoder.py` & `monai-weekly-1.3.dev2330/monai/networks/blocks/encoder.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/blocks/fcn.py` & `monai-weekly-1.3.dev2330/monai/networks/blocks/fcn.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/blocks/feature_pyramid_network.py` & `monai-weekly-1.3.dev2330/monai/networks/blocks/feature_pyramid_network.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/blocks/fft_utils_t.py` & `monai-weekly-1.3.dev2330/monai/networks/blocks/fft_utils_t.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/blocks/localnet_block.py` & `monai-weekly-1.3.dev2330/monai/networks/blocks/localnet_block.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/blocks/mlp.py` & `monai-weekly-1.3.dev2330/monai/networks/blocks/mlp.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/blocks/patchembedding.py` & `monai-weekly-1.3.dev2330/monai/networks/blocks/patchembedding.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/blocks/regunet_block.py` & `monai-weekly-1.3.dev2330/monai/networks/blocks/regunet_block.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/blocks/segresnet_block.py` & `monai-weekly-1.3.dev2330/monai/networks/blocks/segresnet_block.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/blocks/selfattention.py` & `monai-weekly-1.3.dev2330/monai/networks/blocks/selfattention.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/blocks/squeeze_and_excitation.py` & `monai-weekly-1.3.dev2330/monai/networks/blocks/squeeze_and_excitation.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/blocks/text_embedding.py` & `monai-weekly-1.3.dev2330/monai/networks/blocks/text_embedding.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/blocks/transformerblock.py` & `monai-weekly-1.3.dev2330/monai/networks/blocks/transformerblock.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/blocks/unetr_block.py` & `monai-weekly-1.3.dev2330/monai/networks/blocks/unetr_block.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/blocks/upsample.py` & `monai-weekly-1.3.dev2330/monai/networks/blocks/upsample.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/blocks/warp.py` & `monai-weekly-1.3.dev2330/monai/networks/blocks/warp.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/layers/__init__.py` & `monai-weekly-1.3.dev2330/monai/networks/layers/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/layers/convutils.py` & `monai-weekly-1.3.dev2330/monai/networks/layers/convutils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/layers/drop_path.py` & `monai-weekly-1.3.dev2330/monai/networks/layers/drop_path.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/layers/factories.py` & `monai-weekly-1.3.dev2330/monai/networks/layers/factories.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/layers/filtering.py` & `monai-weekly-1.3.dev2330/monai/networks/layers/filtering.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/layers/gmm.py` & `monai-weekly-1.3.dev2330/monai/networks/layers/gmm.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/layers/simplelayers.py` & `monai-weekly-1.3.dev2330/monai/networks/layers/simplelayers.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/layers/spatial_transforms.py` & `monai-weekly-1.3.dev2330/monai/networks/layers/spatial_transforms.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/layers/utils.py` & `monai-weekly-1.3.dev2330/monai/networks/layers/utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/layers/weight_init.py` & `monai-weekly-1.3.dev2330/monai/networks/layers/weight_init.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/__init__.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/ahnet.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/ahnet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/attentionunet.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/attentionunet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/autoencoder.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/autoencoder.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/basic_unet.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/basic_unet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/basic_unetplusplus.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/basic_unetplusplus.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/classifier.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/classifier.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/daf3d.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/daf3d.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/densenet.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/densenet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/dints.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/dints.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/dynunet.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/dynunet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/efficientnet.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/efficientnet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/flexible_unet.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/flexible_unet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/fullyconnectednet.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/fullyconnectednet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/generator.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/generator.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/highresnet.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/highresnet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/hovernet.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/hovernet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/milmodel.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/milmodel.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/netadapter.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/netadapter.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/quicknat.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/quicknat.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/regressor.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/regressor.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/regunet.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/regunet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/resnet.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/resnet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/segresnet.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/segresnet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/segresnet_ds.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/segresnet_ds.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/senet.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/senet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/swin_unetr.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/swin_unetr.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/torchvision_fc.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/torchvision_fc.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/transchex.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/transchex.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/unet.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/unet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/unetr.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/unetr.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/varautoencoder.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/varautoencoder.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/vit.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/vit.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/vitautoenc.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/vitautoenc.py`

 * *Files 5% similar despite different names*

```diff
@@ -7,23 +7,24 @@
 # distributed under the License is distributed on an "AS IS" BASIS,
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 
 from __future__ import annotations
 
+import math
 from collections.abc import Sequence
 
 import torch
 import torch.nn as nn
 
 from monai.networks.blocks.patchembedding import PatchEmbeddingBlock
 from monai.networks.blocks.transformerblock import TransformerBlock
 from monai.networks.layers import Conv
-from monai.utils import ensure_tuple_rep
+from monai.utils import ensure_tuple_rep, is_sqrt
 
 __all__ = ["ViTAutoEnc"]
 
 
 class ViTAutoEnc(nn.Module):
     """
     Vision Transformer (ViT), based on: "Dosovitskiy et al.,
@@ -74,17 +75,22 @@
 
             # for 3-channel with image size of (128,128,128), output will be same size as of input
             >>> net = ViTAutoEnc(in_channels=3, patch_size=(16,16,16), img_size=(128,128,128), pos_embed='conv')
 
         """
 
         super().__init__()
-
+        if not is_sqrt(patch_size):
+            raise ValueError(f"patch_size should be square number, got {patch_size}.")
         self.patch_size = ensure_tuple_rep(patch_size, spatial_dims)
+        self.img_size = ensure_tuple_rep(img_size, spatial_dims)
         self.spatial_dims = spatial_dims
+        for m, p in zip(self.img_size, self.patch_size):
+            if m % p != 0:
+                raise ValueError(f"patch_size={patch_size} should be divisible by img_size={img_size}.")
 
         self.patch_embedding = PatchEmbeddingBlock(
             in_channels=in_channels,
             img_size=img_size,
             patch_size=patch_size,
             hidden_size=hidden_size,
             num_heads=num_heads,
@@ -96,20 +102,20 @@
             [
                 TransformerBlock(hidden_size, mlp_dim, num_heads, dropout_rate, qkv_bias, save_attn)
                 for i in range(num_layers)
             ]
         )
         self.norm = nn.LayerNorm(hidden_size)
 
-        new_patch_size = [4] * self.spatial_dims
         conv_trans = Conv[Conv.CONVTRANS, self.spatial_dims]
         # self.conv3d_transpose* is to be compatible with existing 3d model weights.
-        self.conv3d_transpose = conv_trans(hidden_size, deconv_chns, kernel_size=new_patch_size, stride=new_patch_size)
+        up_kernel_size = [int(math.sqrt(i)) for i in self.patch_size]
+        self.conv3d_transpose = conv_trans(hidden_size, deconv_chns, kernel_size=up_kernel_size, stride=up_kernel_size)
         self.conv3d_transpose_1 = conv_trans(
-            in_channels=deconv_chns, out_channels=out_channels, kernel_size=new_patch_size, stride=new_patch_size
+            in_channels=deconv_chns, out_channels=out_channels, kernel_size=up_kernel_size, stride=up_kernel_size
         )
 
     def forward(self, x):
         """
         Args:
             x: input tensor must have isotropic spatial dimensions,
                 such as ``[batch_size, channels, sp_size, sp_size[, sp_size]]``.
```

### Comparing `monai-weekly-1.3.dev2329/monai/networks/nets/vnet.py` & `monai-weekly-1.3.dev2330/monai/networks/nets/vnet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/networks/utils.py` & `monai-weekly-1.3.dev2330/monai/networks/utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/optimizers/__init__.py` & `monai-weekly-1.3.dev2330/monai/optimizers/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/optimizers/lr_finder.py` & `monai-weekly-1.3.dev2330/monai/optimizers/lr_finder.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/optimizers/lr_scheduler.py` & `monai-weekly-1.3.dev2330/monai/optimizers/lr_scheduler.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/optimizers/novograd.py` & `monai-weekly-1.3.dev2330/monai/optimizers/novograd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/optimizers/utils.py` & `monai-weekly-1.3.dev2330/monai/optimizers/utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/__init__.py` & `monai-weekly-1.3.dev2330/monai/transforms/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/adaptors.py` & `monai-weekly-1.3.dev2330/monai/transforms/adaptors.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/compose.py` & `monai-weekly-1.3.dev2330/monai/transforms/compose.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/croppad/__init__.py` & `monai-weekly-1.3.dev2330/monai/transforms/croppad/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/croppad/array.py` & `monai-weekly-1.3.dev2330/monai/transforms/croppad/array.py`

 * *Files 0% similar despite different names*

```diff
@@ -815,35 +815,36 @@
           [2, 1]]]
 
     This transform is capable of lazy execution. See the :ref:`Lazy Resampling topic<lazy_resampling>`
     for more information.
 
     """
 
+    @deprecated_arg_default("allow_smaller", old_default=True, new_default=False, since="1.2", replaced="1.3")
     def __init__(
         self,
         select_fn: Callable = is_positive,
         channel_indices: IndexSelection | None = None,
         margin: Sequence[int] | int = 0,
-        allow_smaller: bool = False,
+        allow_smaller: bool = True,
         return_coords: bool = False,
         k_divisible: Sequence[int] | int = 1,
         mode: str = PytorchPadMode.CONSTANT,
         lazy: bool = False,
         **pad_kwargs,
     ) -> None:
         """
         Args:
             select_fn: function to select expected foreground, default is to select values > 0.
             channel_indices: if defined, select foreground only on the specified channels
                 of image. if None, select foreground on the whole image.
             margin: add margin value to spatial dims of the bounding box, if only 1 value provided, use it for all dims.
-            allow_smaller: when computing box size with `margin`, whether to allow the final box edges to be outside of
-                the image edges (the image is smaller than the box). If `True`, part of a padded output box might be outside
-                of the original image, if `False`, the image edges will be used as the box edges.
+            allow_smaller: when computing box size with `margin`, whether to allow the image edges to be smaller than the
+                final box edges. If `False`, part of a padded output box might be outside of the original image, if `True`,
+                the image edges will be used as the box edges. Default to `True`.
             return_coords: whether return the coordinates of spatial bounding box for foreground.
             k_divisible: make each spatial dimension to be divisible by k, default to 1.
                 if `k_divisible` is an int, the same `k` be applied to all the input spatial dimensions.
             mode: available modes for numpy array:{``"constant"``, ``"edge"``, ``"linear_ramp"``, ``"maximum"``,
                 ``"mean"``, ``"median"``, ``"minimum"``, ``"reflect"``, ``"symmetric"``, ``"wrap"``, ``"empty"``}
                 available modes for PyTorch Tensor: {``"constant"``, ``"reflect"``, ``"replicate"``, ``"circular"``}.
                 One of the listed string values or a user supplied function. Defaults to ``"constant"``.
```

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/croppad/batch.py` & `monai-weekly-1.3.dev2330/monai/transforms/croppad/batch.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/croppad/dictionary.py` & `monai-weekly-1.3.dev2330/monai/transforms/croppad/dictionary.py`

 * *Files 0% similar despite different names*

```diff
@@ -718,22 +718,23 @@
     Users can define arbitrary function to select expected foreground from the whole source image or specified
     channels. And it can also add margin to every dim of the bounding box of foreground object.
 
     This transform is capable of lazy execution. See the :ref:`Lazy Resampling topic<lazy_resampling>`
     for more information.
     """
 
+    @deprecated_arg_default("allow_smaller", old_default=True, new_default=False, since="1.2", replaced="1.3")
     def __init__(
         self,
         keys: KeysCollection,
         source_key: str,
         select_fn: Callable = is_positive,
         channel_indices: IndexSelection | None = None,
         margin: Sequence[int] | int = 0,
-        allow_smaller: bool = False,
+        allow_smaller: bool = True,
         k_divisible: Sequence[int] | int = 1,
         mode: SequenceStr = PytorchPadMode.CONSTANT,
         start_coord_key: str | None = "foreground_start_coord",
         end_coord_key: str | None = "foreground_end_coord",
         allow_missing_keys: bool = False,
         lazy: bool = False,
         **pad_kwargs,
@@ -743,17 +744,17 @@
             keys: keys of the corresponding items to be transformed.
                 See also: :py:class:`monai.transforms.compose.MapTransform`
             source_key: data source to generate the bounding box of foreground, can be image or label, etc.
             select_fn: function to select expected foreground, default is to select values > 0.
             channel_indices: if defined, select foreground only on the specified channels
                 of image. if None, select foreground on the whole image.
             margin: add margin value to spatial dims of the bounding box, if only 1 value provided, use it for all dims.
-            allow_smaller: when computing box size with `margin`, whether to allow the final box edges to be outside of
-                the image edges (the image is smaller than the box). If `True`, part of a padded output box might be outside
-                of the original image, if `False`, the image edges will be used as the box edges.
+            allow_smaller: when computing box size with `margin`, whether to allow the image edges to be smaller than the
+                final box edges. If `False`, part of a padded output box might be outside of the original image, if `True`,
+                the image edges will be used as the box edges. Default to `True`.
             k_divisible: make each spatial dimension to be divisible by k, default to 1.
                 if `k_divisible` is an int, the same `k` be applied to all the input spatial dimensions.
             mode: available modes for numpy array:{``"constant"``, ``"edge"``, ``"linear_ramp"``, ``"maximum"``,
                 ``"mean"``, ``"median"``, ``"minimum"``, ``"reflect"``, ``"symmetric"``, ``"wrap"``, ``"empty"``}
                 available modes for PyTorch Tensor: {``"constant"``, ``"reflect"``, ``"replicate"``, ``"circular"``}.
                 One of the listed string values or a user supplied function. Defaults to ``"constant"``.
                 See also: https://numpy.org/doc/1.18/reference/generated/numpy.pad.html
```

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/croppad/functional.py` & `monai-weekly-1.3.dev2330/monai/transforms/croppad/functional.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/intensity/__init__.py` & `monai-weekly-1.3.dev2330/monai/transforms/intensity/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/intensity/array.py` & `monai-weekly-1.3.dev2330/monai/transforms/intensity/array.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/intensity/dictionary.py` & `monai-weekly-1.3.dev2330/monai/transforms/intensity/dictionary.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/inverse.py` & `monai-weekly-1.3.dev2330/monai/transforms/inverse.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/inverse_batch_transform.py` & `monai-weekly-1.3.dev2330/monai/transforms/inverse_batch_transform.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/io/__init__.py` & `monai-weekly-1.3.dev2330/monai/transforms/io/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/io/array.py` & `monai-weekly-1.3.dev2330/monai/transforms/io/array.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/io/dictionary.py` & `monai-weekly-1.3.dev2330/monai/transforms/io/dictionary.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/lazy/__init__.py` & `monai-weekly-1.3.dev2330/monai/transforms/lazy/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/lazy/array.py` & `monai-weekly-1.3.dev2330/monai/transforms/lazy/array.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/lazy/dictionary.py` & `monai-weekly-1.3.dev2330/monai/transforms/lazy/dictionary.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/lazy/functional.py` & `monai-weekly-1.3.dev2330/monai/transforms/lazy/functional.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/lazy/utils.py` & `monai-weekly-1.3.dev2330/monai/transforms/lazy/utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/meta_utility/__init__.py` & `monai-weekly-1.3.dev2330/monai/transforms/meta_utility/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/meta_utility/dictionary.py` & `monai-weekly-1.3.dev2330/monai/transforms/meta_utility/dictionary.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/nvtx.py` & `monai-weekly-1.3.dev2330/monai/transforms/nvtx.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/post/__init__.py` & `monai-weekly-1.3.dev2330/monai/transforms/post/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/post/array.py` & `monai-weekly-1.3.dev2330/monai/transforms/post/array.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/post/dictionary.py` & `monai-weekly-1.3.dev2330/monai/transforms/post/dictionary.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/signal/__init__.py` & `monai-weekly-1.3.dev2330/monai/transforms/signal/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/signal/array.py` & `monai-weekly-1.3.dev2330/monai/transforms/signal/array.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/smooth_field/__init__.py` & `monai-weekly-1.3.dev2330/monai/transforms/smooth_field/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/smooth_field/array.py` & `monai-weekly-1.3.dev2330/monai/transforms/smooth_field/array.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/smooth_field/dictionary.py` & `monai-weekly-1.3.dev2330/monai/transforms/smooth_field/dictionary.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/spatial/__init__.py` & `monai-weekly-1.3.dev2330/monai/transforms/spatial/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/spatial/array.py` & `monai-weekly-1.3.dev2330/monai/transforms/spatial/array.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/spatial/dictionary.py` & `monai-weekly-1.3.dev2330/monai/transforms/spatial/dictionary.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/spatial/functional.py` & `monai-weekly-1.3.dev2330/monai/transforms/spatial/functional.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/traits.py` & `monai-weekly-1.3.dev2330/monai/transforms/traits.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/transform.py` & `monai-weekly-1.3.dev2330/monai/transforms/transform.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/utility/__init__.py` & `monai-weekly-1.3.dev2330/monai/transforms/utility/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/utility/array.py` & `monai-weekly-1.3.dev2330/monai/transforms/utility/array.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/utility/dictionary.py` & `monai-weekly-1.3.dev2330/monai/transforms/utility/dictionary.py`

 * *Files 0% similar despite different names*

```diff
@@ -510,15 +510,15 @@
 
     backend = ToTensor.backend
 
     def __init__(
         self,
         keys: KeysCollection,
         dtype: torch.dtype | None = None,
-        device: torch.device | None = None,
+        device: torch.device | str | None = None,
         wrap_sequence: bool = True,
         track_meta: bool | None = None,
         allow_missing_keys: bool = False,
     ) -> None:
         """
         Args:
             keys: keys of the corresponding items to be transformed.
```

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/utils.py` & `monai-weekly-1.3.dev2330/monai/transforms/utils.py`

 * *Files 1% similar despite different names*

```diff
@@ -49,14 +49,15 @@
     NdimageMode,
     NumpyPadMode,
     PostFix,
     PytorchPadMode,
     SplineMode,
     TraceKeys,
     TraceStatusKeys,
+    deprecated_arg_default,
     ensure_tuple,
     ensure_tuple_rep,
     ensure_tuple_size,
     fall_back_tuple,
     get_equivalent_dtype,
     issequenceiterable,
     look_up_option,
@@ -941,20 +942,21 @@
     shift = ensure_tuple(shift)
     affine = eye_func(spatial_dims + 1)
     for i, a in enumerate(shift[:spatial_dims]):
         affine[i, spatial_dims] = a
     return array_func(affine)  # type: ignore
 
 
+@deprecated_arg_default("allow_smaller", old_default=True, new_default=False, since="1.2", replaced="1.3")
 def generate_spatial_bounding_box(
     img: NdarrayOrTensor,
     select_fn: Callable = is_positive,
     channel_indices: IndexSelection | None = None,
     margin: Sequence[int] | int = 0,
-    allow_smaller: bool = False,
+    allow_smaller: bool = True,
 ) -> tuple[list[int], list[int]]:
     """
     Generate the spatial bounding box of foreground in the image with start-end positions (inclusive).
     Users can define arbitrary function to select expected foreground from the whole image or specified channels.
     And it can also add margin to every dim of the bounding box.
     The output format of the coordinates is:
 
@@ -965,17 +967,17 @@
 
     Args:
         img: a "channel-first" image of shape (C, spatial_dim1[, spatial_dim2, ...]) to generate bounding box from.
         select_fn: function to select expected foreground, default is to select values > 0.
         channel_indices: if defined, select foreground only on the specified channels
             of image. if None, select foreground on the whole image.
         margin: add margin value to spatial dims of the bounding box, if only 1 value provided, use it for all dims.
-        allow_smaller: when computing box size with `margin`, whether to allow the final box edges to be outside of
-                the image edges (the image is smaller than the box). If `False`, the bounding boxes edges are aligned
-                with the input image edges, default to `False`.
+        allow_smaller: when computing box size with `margin`, whether to allow the image edges to be smaller than the
+                final box edges. If `True`, the bounding boxes edges are aligned with the input image edges, if `False`,
+                the bounding boxes edges are aligned with the final box edges. Default to `True`.
 
     """
     check_non_lazy_pending_ops(img, name="generate_spatial_bounding_box")
     spatial_size = img.shape[1:]
     data = img[list(ensure_tuple(channel_indices))] if channel_indices is not None else img
     data = select_fn(data).any(0)
     ndim = len(data.shape)
@@ -995,15 +997,15 @@
         if not dt.any():
             # if no foreground, return all zero bounding box coords
             return [0] * ndim, [0] * ndim
 
         arg_max = where(dt == dt.max())[0]
         min_d = arg_max[0] - margin[di]
         max_d = arg_max[-1] + margin[di] + 1
-        if not allow_smaller:
+        if allow_smaller:
             min_d = max(min_d, 0)
             max_d = min(max_d, spatial_size[di])
 
         box_start[di] = min_d.detach().cpu().item() if isinstance(min_d, torch.Tensor) else min_d
         box_end[di] = max_d.detach().cpu().item() if isinstance(max_d, torch.Tensor) else max_d
 
     return box_start, box_end
```

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/utils_create_transform_ims.py` & `monai-weekly-1.3.dev2330/monai/transforms/utils_create_transform_ims.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/transforms/utils_pytorch_numpy_unification.py` & `monai-weekly-1.3.dev2330/monai/transforms/utils_pytorch_numpy_unification.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/utils/__init__.py` & `monai-weekly-1.3.dev2330/monai/utils/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -76,14 +76,15 @@
     first,
     get_seed,
     has_option,
     is_immutable,
     is_module_ver_at_least,
     is_scalar,
     is_scalar_tensor,
+    is_sqrt,
     issequenceiterable,
     list_to_dict,
     path_to_uri,
     pprint_edges,
     progress_bar,
     run_cmd,
     sample_slices,
```

### Comparing `monai-weekly-1.3.dev2329/monai/utils/aliases.py` & `monai-weekly-1.3.dev2330/monai/utils/aliases.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/utils/decorators.py` & `monai-weekly-1.3.dev2330/monai/utils/decorators.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/utils/deprecate_utils.py` & `monai-weekly-1.3.dev2330/monai/utils/deprecate_utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/utils/dist.py` & `monai-weekly-1.3.dev2330/monai/utils/dist.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/utils/enums.py` & `monai-weekly-1.3.dev2330/monai/utils/enums.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/utils/jupyter_utils.py` & `monai-weekly-1.3.dev2330/monai/utils/jupyter_utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/utils/misc.py` & `monai-weekly-1.3.dev2330/monai/utils/misc.py`

 * *Files 2% similar despite different names*

```diff
@@ -9,14 +9,15 @@
 # See the License for the specific language governing permissions and
 # limitations under the License.
 
 from __future__ import annotations
 
 import inspect
 import itertools
+import math
 import os
 import pprint
 import random
 import shutil
 import subprocess
 import tempfile
 import types
@@ -849,7 +850,17 @@
         return subprocess.run(cmd_list, **kwargs)
     except subprocess.CalledProcessError as e:
         if not debug:
             raise
         output = str(e.stdout.decode(errors="replace"))
         errors = str(e.stderr.decode(errors="replace"))
         raise RuntimeError(f"subprocess call error {e.returncode}: {errors}, {output}.") from e
+
+
+def is_sqrt(num: Sequence[int] | int) -> bool:
+    """
+    Determine if the input is a square number or a squence of square numbers.
+    """
+    num = ensure_tuple(num)
+    sqrt_num = [int(math.sqrt(_num)) for _num in num]
+    ret = [_i * _j for _i, _j in zip(sqrt_num, sqrt_num)]
+    return ensure_tuple(ret) == num
```

### Comparing `monai-weekly-1.3.dev2329/monai/utils/module.py` & `monai-weekly-1.3.dev2330/monai/utils/module.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/utils/nvtx.py` & `monai-weekly-1.3.dev2330/monai/utils/nvtx.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/utils/profiling.py` & `monai-weekly-1.3.dev2330/monai/utils/profiling.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/utils/state_cacher.py` & `monai-weekly-1.3.dev2330/monai/utils/state_cacher.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/utils/type_conversion.py` & `monai-weekly-1.3.dev2330/monai/utils/type_conversion.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/visualize/__init__.py` & `monai-weekly-1.3.dev2330/monai/visualize/__init__.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/visualize/class_activation_maps.py` & `monai-weekly-1.3.dev2330/monai/visualize/class_activation_maps.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/visualize/gradient_based.py` & `monai-weekly-1.3.dev2330/monai/visualize/gradient_based.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/visualize/img2tensorboard.py` & `monai-weekly-1.3.dev2330/monai/visualize/img2tensorboard.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/visualize/occlusion_sensitivity.py` & `monai-weekly-1.3.dev2330/monai/visualize/occlusion_sensitivity.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/visualize/utils.py` & `monai-weekly-1.3.dev2330/monai/visualize/utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai/visualize/visualizer.py` & `monai-weekly-1.3.dev2330/monai/visualize/visualizer.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai_weekly.egg-info/PKG-INFO` & `monai-weekly-1.3.dev2330/monai_weekly.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: monai-weekly
-Version: 1.3.dev2329
+Version: 1.3.dev2330
 Summary: AI Toolkit for Healthcare Imaging
 Home-page: https://monai.io/
 Author: MONAI Consortium
 Author-email: monai.contact@gmail.com
 License: Apache License 2.0
 Project-URL: Documentation, https://docs.monai.io/
 Project-URL: Bug Tracker, https://github.com/Project-MONAI/MONAI/issues
```

### Comparing `monai-weekly-1.3.dev2329/monai_weekly.egg-info/SOURCES.txt` & `monai-weekly-1.3.dev2330/monai_weekly.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/monai_weekly.egg-info/requires.txt` & `monai-weekly-1.3.dev2330/monai_weekly.egg-info/requires.txt`

 * *Files 9% similar despite different names*

```diff
@@ -10,15 +10,15 @@
 gdown>=4.4.0
 pytorch-ignite==0.4.11
 torchvision
 itk>=5.2
 tqdm>=4.47.0
 lmdb
 psutil
-cucim>=22.8.1
+cucim>=23.2.0
 openslide-python==1.1.2
 tifffile
 imagecodecs
 pandas
 einops
 transformers<4.22
 mlflow>=1.28.0
@@ -36,15 +36,15 @@
 onnx>=1.13.0
 zarr
 
 [all:python_version <= "3.10"]
 onnxruntime
 
 [cucim]
-cucim>=22.8.1
+cucim>=23.2.0
 
 [einops]
 einops
 
 [fire]
 fire
```

### Comparing `monai-weekly-1.3.dev2329/pyproject.toml` & `monai-weekly-1.3.dev2330/pyproject.toml`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/setup.cfg` & `monai-weekly-1.3.dev2330/setup.cfg`

 * *Files 0% similar despite different names*

```diff
@@ -51,15 +51,15 @@
 	gdown>=4.4.0
 	pytorch-ignite==0.4.11
 	torchvision
 	itk>=5.2
 	tqdm>=4.47.0
 	lmdb
 	psutil
-	cucim>=22.8.1
+	cucim>=23.2.0
 	openslide-python==1.1.2
 	tifffile
 	imagecodecs
 	pandas
 	einops
 	transformers<4.22
 	mlflow>=1.28.0
@@ -98,15 +98,15 @@
 tqdm = 
 	tqdm>=4.47.0
 lmdb = 
 	lmdb
 psutil = 
 	psutil
 cucim = 
-	cucim>=22.8.1
+	cucim>=23.2.0
 openslide = 
 	openslide-python==1.1.2
 tifffile = 
 	tifffile
 imagecodecs = 
 	imagecodecs
 pandas =
```

### Comparing `monai-weekly-1.3.dev2329/setup.py` & `monai-weekly-1.3.dev2330/setup.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_acn_block.py` & `monai-weekly-1.3.dev2330/tests/test_acn_block.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_activations.py` & `monai-weekly-1.3.dev2330/tests/test_activations.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_activationsd.py` & `monai-weekly-1.3.dev2330/tests/test_activationsd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_adaptors.py` & `monai-weekly-1.3.dev2330/tests/test_adaptors.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_add_channeld.py` & `monai-weekly-1.3.dev2330/tests/test_add_channeld.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_add_coordinate_channels.py` & `monai-weekly-1.3.dev2330/tests/test_add_coordinate_channels.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_add_coordinate_channelsd.py` & `monai-weekly-1.3.dev2330/tests/test_add_coordinate_channelsd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_add_extreme_points_channel.py` & `monai-weekly-1.3.dev2330/tests/test_add_extreme_points_channel.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_add_extreme_points_channeld.py` & `monai-weekly-1.3.dev2330/tests/test_add_extreme_points_channeld.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_adjust_contrast.py` & `monai-weekly-1.3.dev2330/tests/test_adjust_contrast.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_adjust_contrastd.py` & `monai-weekly-1.3.dev2330/tests/test_adjust_contrastd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_adn.py` & `monai-weekly-1.3.dev2330/tests/test_adn.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_affine.py` & `monai-weekly-1.3.dev2330/tests/test_affine.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_affine_grid.py` & `monai-weekly-1.3.dev2330/tests/test_affine_grid.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_affine_transform.py` & `monai-weekly-1.3.dev2330/tests/test_affine_transform.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_affined.py` & `monai-weekly-1.3.dev2330/tests/test_affined.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_ahnet.py` & `monai-weekly-1.3.dev2330/tests/test_ahnet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_alias.py` & `monai-weekly-1.3.dev2330/tests/test_alias.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_anchor_box.py` & `monai-weekly-1.3.dev2330/tests/test_anchor_box.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_apply.py` & `monai-weekly-1.3.dev2330/tests/test_apply.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_apply_filter.py` & `monai-weekly-1.3.dev2330/tests/test_apply_filter.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_arraydataset.py` & `monai-weekly-1.3.dev2330/tests/test_arraydataset.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_as_channel_first.py` & `monai-weekly-1.3.dev2330/tests/test_as_channel_first.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_as_channel_firstd.py` & `monai-weekly-1.3.dev2330/tests/test_as_channel_firstd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_as_channel_last.py` & `monai-weekly-1.3.dev2330/tests/test_as_channel_last.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_as_channel_lastd.py` & `monai-weekly-1.3.dev2330/tests/test_as_channel_lastd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_as_discrete.py` & `monai-weekly-1.3.dev2330/tests/test_as_discrete.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_as_discreted.py` & `monai-weekly-1.3.dev2330/tests/test_as_discreted.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_atss_box_matcher.py` & `monai-weekly-1.3.dev2330/tests/test_atss_box_matcher.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_attentionunet.py` & `monai-weekly-1.3.dev2330/tests/test_attentionunet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_auto3dseg.py` & `monai-weekly-1.3.dev2330/tests/test_auto3dseg.py`

 * *Files 0% similar despite different names*

```diff
@@ -166,15 +166,15 @@
 
 class TestDataAnalyzer(unittest.TestCase):
     def setUp(self):
         self.test_dir = tempfile.TemporaryDirectory()
         work_dir = self.test_dir.name
         self.dataroot_dir = os.path.join(work_dir, "sim_dataroot")
         self.datalist_file = os.path.join(work_dir, "sim_datalist.json")
-        self.datastat_file = os.path.join(work_dir, "datastats.yaml")
+        self.datastat_file = os.path.join(work_dir, "datastats.yml")
         ConfigParser.export_config_file(sim_datalist, self.datalist_file)
 
     @parameterized.expand(SIM_CPU_TEST_CASES)
     def test_data_analyzer_cpu(self, input_params):
         sim_dim = input_params["sim_dim"]
         label_key = input_params["label_key"]
         image_only = not bool(label_key)
```

### Comparing `monai-weekly-1.3.dev2329/tests/test_auto3dseg_bundlegen.py` & `monai-weekly-1.3.dev2330/tests/test_auto3dseg_bundlegen.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_auto3dseg_ensemble.py` & `monai-weekly-1.3.dev2330/tests/test_auto3dseg_ensemble.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_auto3dseg_hpo.py` & `monai-weekly-1.3.dev2330/tests/test_auto3dseg_hpo.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_autoencoder.py` & `monai-weekly-1.3.dev2330/tests/test_autoencoder.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_avg_merger.py` & `monai-weekly-1.3.dev2330/tests/test_avg_merger.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_basic_unet.py` & `monai-weekly-1.3.dev2330/tests/test_basic_unet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_basic_unetplusplus.py` & `monai-weekly-1.3.dev2330/tests/test_basic_unetplusplus.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_bending_energy.py` & `monai-weekly-1.3.dev2330/tests/test_bending_energy.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_bilateral_approx_cpu.py` & `monai-weekly-1.3.dev2330/tests/test_bilateral_approx_cpu.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_bilateral_approx_cuda.py` & `monai-weekly-1.3.dev2330/tests/test_bilateral_approx_cuda.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_bilateral_precise.py` & `monai-weekly-1.3.dev2330/tests/test_bilateral_precise.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_blend_images.py` & `monai-weekly-1.3.dev2330/tests/test_blend_images.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_border_pad.py` & `monai-weekly-1.3.dev2330/tests/test_border_pad.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_border_padd.py` & `monai-weekly-1.3.dev2330/tests/test_border_padd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_bounding_rect.py` & `monai-weekly-1.3.dev2330/tests/test_bounding_rect.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_bounding_rectd.py` & `monai-weekly-1.3.dev2330/tests/test_bounding_rectd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_box_coder.py` & `monai-weekly-1.3.dev2330/tests/test_box_coder.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_box_transform.py` & `monai-weekly-1.3.dev2330/tests/test_box_transform.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_box_utils.py` & `monai-weekly-1.3.dev2330/tests/test_box_utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_bundle_ckpt_export.py` & `monai-weekly-1.3.dev2330/tests/test_bundle_ckpt_export.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_bundle_download.py` & `monai-weekly-1.3.dev2330/tests/test_bundle_download.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_bundle_get_data.py` & `monai-weekly-1.3.dev2330/tests/test_bundle_get_data.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_bundle_init_bundle.py` & `monai-weekly-1.3.dev2330/tests/test_bundle_init_bundle.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_bundle_onnx_export.py` & `monai-weekly-1.3.dev2330/tests/test_bundle_onnx_export.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_bundle_trt_export.py` & `monai-weekly-1.3.dev2330/tests/test_bundle_trt_export.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_bundle_utils.py` & `monai-weekly-1.3.dev2330/tests/test_bundle_utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_bundle_verify_metadata.py` & `monai-weekly-1.3.dev2330/tests/test_bundle_verify_metadata.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_bundle_verify_net.py` & `monai-weekly-1.3.dev2330/tests/test_bundle_verify_net.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_bundle_workflow.py` & `monai-weekly-1.3.dev2330/tests/test_bundle_workflow.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_cachedataset.py` & `monai-weekly-1.3.dev2330/tests/test_cachedataset.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_cachedataset_parallel.py` & `monai-weekly-1.3.dev2330/tests/test_cachedataset_parallel.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_cachedataset_persistent_workers.py` & `monai-weekly-1.3.dev2330/tests/test_cachedataset_persistent_workers.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_cachentransdataset.py` & `monai-weekly-1.3.dev2330/tests/test_cachentransdataset.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_call_dist.py` & `monai-weekly-1.3.dev2330/tests/test_call_dist.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_cast_to_type.py` & `monai-weekly-1.3.dev2330/tests/test_cast_to_type.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_cast_to_typed.py` & `monai-weekly-1.3.dev2330/tests/test_cast_to_typed.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_center_scale_crop.py` & `monai-weekly-1.3.dev2330/tests/test_center_scale_crop.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_center_scale_cropd.py` & `monai-weekly-1.3.dev2330/tests/test_center_scale_cropd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_center_spatial_crop.py` & `monai-weekly-1.3.dev2330/tests/test_center_spatial_crop.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_center_spatial_cropd.py` & `monai-weekly-1.3.dev2330/tests/test_center_spatial_cropd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_channel_pad.py` & `monai-weekly-1.3.dev2330/tests/test_channel_pad.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_check_hash.py` & `monai-weekly-1.3.dev2330/tests/test_check_hash.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_check_missing_files.py` & `monai-weekly-1.3.dev2330/tests/test_check_missing_files.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_classes_to_indices.py` & `monai-weekly-1.3.dev2330/tests/test_classes_to_indices.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_classes_to_indicesd.py` & `monai-weekly-1.3.dev2330/tests/test_classes_to_indicesd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_complex_utils.py` & `monai-weekly-1.3.dev2330/tests/test_complex_utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_component_locator.py` & `monai-weekly-1.3.dev2330/tests/test_component_locator.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_compose.py` & `monai-weekly-1.3.dev2330/tests/test_compose.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_compose_get_number_conversions.py` & `monai-weekly-1.3.dev2330/tests/test_compose_get_number_conversions.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_compute_confusion_matrix.py` & `monai-weekly-1.3.dev2330/tests/test_compute_confusion_matrix.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_compute_f_beta.py` & `monai-weekly-1.3.dev2330/tests/test_compute_f_beta.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_compute_froc.py` & `monai-weekly-1.3.dev2330/tests/test_compute_froc.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_compute_generalized_dice.py` & `monai-weekly-1.3.dev2330/tests/test_compute_generalized_dice.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_compute_ho_ver_maps.py` & `monai-weekly-1.3.dev2330/tests/test_compute_ho_ver_maps.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_compute_ho_ver_maps_d.py` & `monai-weekly-1.3.dev2330/tests/test_compute_ho_ver_maps_d.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_compute_meandice.py` & `monai-weekly-1.3.dev2330/tests/test_compute_meandice.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_compute_meaniou.py` & `monai-weekly-1.3.dev2330/tests/test_compute_meaniou.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_compute_panoptic_quality.py` & `monai-weekly-1.3.dev2330/tests/test_compute_panoptic_quality.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_compute_regression_metrics.py` & `monai-weekly-1.3.dev2330/tests/test_compute_regression_metrics.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_compute_roc_auc.py` & `monai-weekly-1.3.dev2330/tests/test_compute_roc_auc.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_compute_variance.py` & `monai-weekly-1.3.dev2330/tests/test_compute_variance.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_concat_itemsd.py` & `monai-weekly-1.3.dev2330/tests/test_concat_itemsd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_config_item.py` & `monai-weekly-1.3.dev2330/tests/test_config_item.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_config_parser.py` & `monai-weekly-1.3.dev2330/tests/test_config_parser.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_contrastive_loss.py` & `monai-weekly-1.3.dev2330/tests/test_contrastive_loss.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_convert_data_type.py` & `monai-weekly-1.3.dev2330/tests/test_convert_data_type.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_convert_to_multi_channel.py` & `monai-weekly-1.3.dev2330/tests/test_convert_to_multi_channel.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_convert_to_multi_channeld.py` & `monai-weekly-1.3.dev2330/tests/test_convert_to_multi_channeld.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_convert_to_onnx.py` & `monai-weekly-1.3.dev2330/tests/test_convert_to_onnx.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_convert_to_torchscript.py` & `monai-weekly-1.3.dev2330/tests/test_convert_to_torchscript.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_convert_to_trt.py` & `monai-weekly-1.3.dev2330/tests/test_convert_to_trt.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_convolutions.py` & `monai-weekly-1.3.dev2330/tests/test_convolutions.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_copy_itemsd.py` & `monai-weekly-1.3.dev2330/tests/test_copy_itemsd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_copy_model_state.py` & `monai-weekly-1.3.dev2330/tests/test_copy_model_state.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_correct_crop_centers.py` & `monai-weekly-1.3.dev2330/tests/test_correct_crop_centers.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_create_cross_validation_datalist.py` & `monai-weekly-1.3.dev2330/tests/test_create_cross_validation_datalist.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_create_grid_and_affine.py` & `monai-weekly-1.3.dev2330/tests/test_create_grid_and_affine.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_crf_cpu.py` & `monai-weekly-1.3.dev2330/tests/test_crf_cpu.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_crf_cuda.py` & `monai-weekly-1.3.dev2330/tests/test_crf_cuda.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_crop_foreground.py` & `monai-weekly-1.3.dev2330/tests/test_crop_foreground.py`

 * *Ordering differences only*

 * *Files 0% similar despite different names*

```diff
@@ -59,24 +59,24 @@
             p([[[0, 0, 0, 0, 0], [0, 1, 2, 1, 0], [0, 2, 3, 2, 0], [0, 0, 0, 0, 0]]]),
             True,
         ]
     )
 
     TESTS.append(
         [
-            {"select_fn": lambda x: x > 0, "channel_indices": None, "margin": [2, 1], "allow_smaller": False},
+            {"select_fn": lambda x: x > 0, "channel_indices": None, "margin": [2, 1], "allow_smaller": True},
             p([[[0, 0, 0, 0, 0], [0, 1, 2, 1, 0], [0, 2, 3, 2, 0], [0, 0, 0, 0, 0], [0, 0, 0, 0, 0]]]),
             p([[[0, 0, 0, 0, 0], [0, 1, 2, 1, 0], [0, 2, 3, 2, 0], [0, 0, 0, 0, 0], [0, 0, 0, 0, 0]]]),
             True,
         ]
     )
 
     TESTS.append(
         [
-            {"select_fn": lambda x: x > 0, "channel_indices": None, "margin": [2, 1], "allow_smaller": True},
+            {"select_fn": lambda x: x > 0, "channel_indices": None, "margin": [2, 1], "allow_smaller": False},
             p([[[0, 0, 0, 0, 0], [0, 1, 2, 1, 0], [0, 2, 3, 2, 0], [0, 0, 0, 0, 0], [0, 0, 0, 0, 0]]]),
             p([[[0, 0, 0, 0, 0], [0, 0, 0, 0, 0], [0, 1, 2, 1, 0], [0, 2, 3, 2, 0], [0, 0, 0, 0, 0], [0, 0, 0, 0, 0]]]),
             True,
         ]
     )
 
     TESTS.append(
```

### Comparing `monai-weekly-1.3.dev2329/tests/test_crop_foregroundd.py` & `monai-weekly-1.3.dev2330/tests/test_crop_foregroundd.py`

 * *Ordering differences only*

 * *Files 0% similar despite different names*

```diff
@@ -84,15 +84,15 @@
         [
             {
                 "keys": ["img"],
                 "source_key": "img",
                 "select_fn": lambda x: x > 0,
                 "channel_indices": None,
                 "margin": [2, 1],
-                "allow_smaller": False,
+                "allow_smaller": True,
             },
             {
                 "img": p(
                     np.array([[[0, 0, 0, 0, 0], [0, 1, 2, 1, 0], [0, 2, 3, 2, 0], [0, 1, 2, 1, 0], [0, 0, 0, 0, 0]]])
                 )
             },
             p(np.array([[[0, 0, 0, 0, 0], [0, 1, 2, 1, 0], [0, 2, 3, 2, 0], [0, 1, 2, 1, 0], [0, 0, 0, 0, 0]]])),
@@ -103,15 +103,15 @@
         [
             {
                 "keys": ["img"],
                 "source_key": "img",
                 "select_fn": lambda x: x > 0,
                 "channel_indices": None,
                 "margin": [2, 1],
-                "allow_smaller": True,
+                "allow_smaller": False,
             },
             {
                 "img": p(
                     np.array([[[0, 0, 0, 0, 0], [0, 1, 2, 1, 0], [0, 2, 3, 2, 0], [0, 1, 2, 1, 0], [0, 0, 0, 0, 0]]])
                 )
             },
             p(
```

### Comparing `monai-weekly-1.3.dev2329/tests/test_cross_validation.py` & `monai-weekly-1.3.dev2330/tests/test_cross_validation.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_csv_dataset.py` & `monai-weekly-1.3.dev2330/tests/test_csv_dataset.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_csv_iterable_dataset.py` & `monai-weekly-1.3.dev2330/tests/test_csv_iterable_dataset.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_csv_saver.py` & `monai-weekly-1.3.dev2330/tests/test_csv_saver.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_cucim_dict_transform.py` & `monai-weekly-1.3.dev2330/tests/test_cucim_dict_transform.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_cucim_transform.py` & `monai-weekly-1.3.dev2330/tests/test_cucim_transform.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_cumulative.py` & `monai-weekly-1.3.dev2330/tests/test_cumulative.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_cumulative_average.py` & `monai-weekly-1.3.dev2330/tests/test_cumulative_average.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_cumulative_average_dist.py` & `monai-weekly-1.3.dev2330/tests/test_cumulative_average_dist.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_cv2_dist.py` & `monai-weekly-1.3.dev2330/tests/test_cv2_dist.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_daf3d.py` & `monai-weekly-1.3.dev2330/tests/test_daf3d.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_data_stats.py` & `monai-weekly-1.3.dev2330/tests/test_data_stats.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_data_statsd.py` & `monai-weekly-1.3.dev2330/tests/test_data_statsd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_dataloader.py` & `monai-weekly-1.3.dev2330/tests/test_dataloader.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_dataset.py` & `monai-weekly-1.3.dev2330/tests/test_dataset.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_dataset_func.py` & `monai-weekly-1.3.dev2330/tests/test_dataset_func.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_dataset_summary.py` & `monai-weekly-1.3.dev2330/tests/test_dataset_summary.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_decathlondataset.py` & `monai-weekly-1.3.dev2330/tests/test_decathlondataset.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_decollate.py` & `monai-weekly-1.3.dev2330/tests/test_decollate.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_deepedit_interaction.py` & `monai-weekly-1.3.dev2330/tests/test_deepedit_interaction.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_deepedit_transforms.py` & `monai-weekly-1.3.dev2330/tests/test_deepedit_transforms.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_deepgrow_dataset.py` & `monai-weekly-1.3.dev2330/tests/test_deepgrow_dataset.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_deepgrow_interaction.py` & `monai-weekly-1.3.dev2330/tests/test_deepgrow_interaction.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_deepgrow_transforms.py` & `monai-weekly-1.3.dev2330/tests/test_deepgrow_transforms.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_delete_itemsd.py` & `monai-weekly-1.3.dev2330/tests/test_delete_itemsd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_denseblock.py` & `monai-weekly-1.3.dev2330/tests/test_denseblock.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_densenet.py` & `monai-weekly-1.3.dev2330/tests/test_densenet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_deprecated.py` & `monai-weekly-1.3.dev2330/tests/test_deprecated.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_detect_envelope.py` & `monai-weekly-1.3.dev2330/tests/test_detect_envelope.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_detection_coco_metrics.py` & `monai-weekly-1.3.dev2330/tests/test_detection_coco_metrics.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_detector_boxselector.py` & `monai-weekly-1.3.dev2330/tests/test_detector_boxselector.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_detector_utils.py` & `monai-weekly-1.3.dev2330/tests/test_detector_utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_dev_collate.py` & `monai-weekly-1.3.dev2330/tests/test_dev_collate.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_dice_ce_loss.py` & `monai-weekly-1.3.dev2330/tests/test_dice_ce_loss.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_dice_focal_loss.py` & `monai-weekly-1.3.dev2330/tests/test_dice_focal_loss.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_dice_loss.py` & `monai-weekly-1.3.dev2330/tests/test_dice_loss.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_dints_cell.py` & `monai-weekly-1.3.dev2330/tests/test_dints_cell.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_dints_mixop.py` & `monai-weekly-1.3.dev2330/tests/test_dints_mixop.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_dints_network.py` & `monai-weekly-1.3.dev2330/tests/test_dints_network.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_discriminator.py` & `monai-weekly-1.3.dev2330/tests/test_discriminator.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_divisible_pad.py` & `monai-weekly-1.3.dev2330/tests/test_divisible_pad.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_divisible_padd.py` & `monai-weekly-1.3.dev2330/tests/test_divisible_padd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_download_and_extract.py` & `monai-weekly-1.3.dev2330/tests/test_download_and_extract.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_download_url_yandex.py` & `monai-weekly-1.3.dev2330/tests/test_download_url_yandex.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_downsample_block.py` & `monai-weekly-1.3.dev2330/tests/test_downsample_block.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_drop_path.py` & `monai-weekly-1.3.dev2330/tests/test_drop_path.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_ds_loss.py` & `monai-weekly-1.3.dev2330/tests/test_ds_loss.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_dvf2ddf.py` & `monai-weekly-1.3.dev2330/tests/test_dvf2ddf.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_dynunet.py` & `monai-weekly-1.3.dev2330/tests/test_dynunet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_dynunet_block.py` & `monai-weekly-1.3.dev2330/tests/test_dynunet_block.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_efficientnet.py` & `monai-weekly-1.3.dev2330/tests/test_efficientnet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_ensemble_evaluator.py` & `monai-weekly-1.3.dev2330/tests/test_ensemble_evaluator.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_ensure_channel_first.py` & `monai-weekly-1.3.dev2330/tests/test_ensure_channel_first.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_ensure_channel_firstd.py` & `monai-weekly-1.3.dev2330/tests/test_ensure_channel_firstd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_ensure_tuple.py` & `monai-weekly-1.3.dev2330/tests/test_ensure_tuple.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_ensure_type.py` & `monai-weekly-1.3.dev2330/tests/test_ensure_type.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_ensure_typed.py` & `monai-weekly-1.3.dev2330/tests/test_ensure_typed.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_enum_bound_interp.py` & `monai-weekly-1.3.dev2330/tests/test_enum_bound_interp.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_eval_mode.py` & `monai-weekly-1.3.dev2330/tests/test_eval_mode.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_evenly_divisible_all_gather_dist.py` & `monai-weekly-1.3.dev2330/tests/test_evenly_divisible_all_gather_dist.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_factorized_increase.py` & `monai-weekly-1.3.dev2330/tests/test_factorized_increase.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_factorized_reduce.py` & `monai-weekly-1.3.dev2330/tests/test_factorized_reduce.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_fastmri_reader.py` & `monai-weekly-1.3.dev2330/tests/test_fastmri_reader.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_fft_utils.py` & `monai-weekly-1.3.dev2330/tests/test_fft_utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_fg_bg_to_indices.py` & `monai-weekly-1.3.dev2330/tests/test_fg_bg_to_indices.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_fg_bg_to_indicesd.py` & `monai-weekly-1.3.dev2330/tests/test_fg_bg_to_indicesd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_file_basename.py` & `monai-weekly-1.3.dev2330/tests/test_file_basename.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_fill_holes.py` & `monai-weekly-1.3.dev2330/tests/test_fill_holes.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_fill_holesd.py` & `monai-weekly-1.3.dev2330/tests/test_fill_holesd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_fl_exchange_object.py` & `monai-weekly-1.3.dev2330/tests/test_fl_exchange_object.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_fl_monai_algo.py` & `monai-weekly-1.3.dev2330/tests/test_fl_monai_algo.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_fl_monai_algo_dist.py` & `monai-weekly-1.3.dev2330/tests/test_fl_monai_algo_dist.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_fl_monai_algo_stats.py` & `monai-weekly-1.3.dev2330/tests/test_fl_monai_algo_stats.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_flatten_sub_keysd.py` & `monai-weekly-1.3.dev2330/tests/test_flatten_sub_keysd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_flexible_unet.py` & `monai-weekly-1.3.dev2330/tests/test_flexible_unet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_flip.py` & `monai-weekly-1.3.dev2330/tests/test_flip.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_flipd.py` & `monai-weekly-1.3.dev2330/tests/test_flipd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_focal_loss.py` & `monai-weekly-1.3.dev2330/tests/test_focal_loss.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_folder_layout.py` & `monai-weekly-1.3.dev2330/tests/test_folder_layout.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_foreground_mask.py` & `monai-weekly-1.3.dev2330/tests/test_foreground_mask.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_foreground_maskd.py` & `monai-weekly-1.3.dev2330/tests/test_foreground_maskd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_fourier.py` & `monai-weekly-1.3.dev2330/tests/test_fourier.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_fpn_block.py` & `monai-weekly-1.3.dev2330/tests/test_fpn_block.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_from_engine_hovernet.py` & `monai-weekly-1.3.dev2330/tests/test_from_engine_hovernet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_fullyconnectednet.py` & `monai-weekly-1.3.dev2330/tests/test_fullyconnectednet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_gaussian.py` & `monai-weekly-1.3.dev2330/tests/test_gaussian.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_gaussian_filter.py` & `monai-weekly-1.3.dev2330/tests/test_gaussian_filter.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_gaussian_sharpen.py` & `monai-weekly-1.3.dev2330/tests/test_gaussian_sharpen.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_gaussian_sharpend.py` & `monai-weekly-1.3.dev2330/tests/test_gaussian_sharpend.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_gaussian_smooth.py` & `monai-weekly-1.3.dev2330/tests/test_gaussian_smooth.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_gaussian_smoothd.py` & `monai-weekly-1.3.dev2330/tests/test_gaussian_smoothd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_generalized_dice_focal_loss.py` & `monai-weekly-1.3.dev2330/tests/test_generalized_dice_focal_loss.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_generalized_dice_loss.py` & `monai-weekly-1.3.dev2330/tests/test_generalized_dice_loss.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_generalized_wasserstein_dice_loss.py` & `monai-weekly-1.3.dev2330/tests/test_generalized_wasserstein_dice_loss.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_generate_distance_map.py` & `monai-weekly-1.3.dev2330/tests/test_generate_distance_map.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_generate_distance_mapd.py` & `monai-weekly-1.3.dev2330/tests/test_generate_distance_mapd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_generate_instance_border.py` & `monai-weekly-1.3.dev2330/tests/test_generate_instance_border.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_generate_instance_borderd.py` & `monai-weekly-1.3.dev2330/tests/test_generate_instance_borderd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_generate_instance_centroid.py` & `monai-weekly-1.3.dev2330/tests/test_generate_instance_centroid.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_generate_instance_centroidd.py` & `monai-weekly-1.3.dev2330/tests/test_generate_instance_centroidd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_generate_instance_contour.py` & `monai-weekly-1.3.dev2330/tests/test_generate_instance_contour.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_generate_instance_contourd.py` & `monai-weekly-1.3.dev2330/tests/test_generate_instance_contourd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_generate_instance_type.py` & `monai-weekly-1.3.dev2330/tests/test_generate_instance_type.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_generate_instance_typed.py` & `monai-weekly-1.3.dev2330/tests/test_generate_instance_typed.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_generate_label_classes_crop_centers.py` & `monai-weekly-1.3.dev2330/tests/test_generate_label_classes_crop_centers.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_generate_param_groups.py` & `monai-weekly-1.3.dev2330/tests/test_generate_param_groups.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_generate_pos_neg_label_crop_centers.py` & `monai-weekly-1.3.dev2330/tests/test_generate_pos_neg_label_crop_centers.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_generate_spatial_bounding_box.py` & `monai-weekly-1.3.dev2330/tests/test_generate_spatial_bounding_box.py`

 * *Ordering differences only*

 * *Files 0% similar despite different names*

```diff
@@ -78,29 +78,29 @@
             {
                 "img": p(
                     np.array([[[0, 0, 0, 0, 0], [0, 1, 2, 1, 0], [0, 2, 3, 2, 0], [0, 1, 2, 1, 0], [0, 0, 0, 0, 0]]])
                 ),
                 "select_fn": lambda x: x > 0,
                 "channel_indices": None,
                 "margin": [2, 1],
-                "allow_smaller": True,
+                "allow_smaller": False,
             },
             ([-1, 0], [6, 5]),
         ]
     )
     TESTS.append(
         [
             {
                 "img": p(
                     np.array([[[0, 0, 0, 0, 0], [0, 1, 2, 1, 0], [0, 2, 3, 2, 0], [0, 1, 2, 1, 0], [0, 0, 0, 0, 0]]])
                 ),
                 "select_fn": lambda x: x > 0,
                 "channel_indices": None,
                 "margin": [2, 1],
-                "allow_smaller": False,
+                "allow_smaller": True,
             },
             ([0, 0], [5, 5]),
         ]
     )
 
 
 class TestGenerateSpatialBoundingBox(unittest.TestCase):
```

### Comparing `monai-weekly-1.3.dev2329/tests/test_generate_succinct_contour.py` & `monai-weekly-1.3.dev2330/tests/test_generate_succinct_contour.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_generate_succinct_contourd.py` & `monai-weekly-1.3.dev2330/tests/test_generate_succinct_contourd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_generate_watershed_markers.py` & `monai-weekly-1.3.dev2330/tests/test_generate_watershed_markers.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_generate_watershed_markersd.py` & `monai-weekly-1.3.dev2330/tests/test_generate_watershed_markersd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_generate_watershed_mask.py` & `monai-weekly-1.3.dev2330/tests/test_generate_watershed_mask.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_generate_watershed_maskd.py` & `monai-weekly-1.3.dev2330/tests/test_generate_watershed_maskd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_generator.py` & `monai-weekly-1.3.dev2330/tests/test_generator.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_get_equivalent_dtype.py` & `monai-weekly-1.3.dev2330/tests/test_get_equivalent_dtype.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_get_extreme_points.py` & `monai-weekly-1.3.dev2330/tests/test_get_extreme_points.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_get_layers.py` & `monai-weekly-1.3.dev2330/tests/test_get_layers.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_get_package_version.py` & `monai-weekly-1.3.dev2330/tests/test_get_package_version.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_get_unique_labels.py` & `monai-weekly-1.3.dev2330/tests/test_get_unique_labels.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_gibbs_noise.py` & `monai-weekly-1.3.dev2330/tests/test_gibbs_noise.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_gibbs_noised.py` & `monai-weekly-1.3.dev2330/tests/test_gibbs_noised.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_giou_loss.py` & `monai-weekly-1.3.dev2330/tests/test_giou_loss.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_global_mutual_information_loss.py` & `monai-weekly-1.3.dev2330/tests/test_global_mutual_information_loss.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_globalnet.py` & `monai-weekly-1.3.dev2330/tests/test_globalnet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_gmm.py` & `monai-weekly-1.3.dev2330/tests/test_gmm.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_grid_dataset.py` & `monai-weekly-1.3.dev2330/tests/test_grid_dataset.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_grid_distortion.py` & `monai-weekly-1.3.dev2330/tests/test_grid_distortion.py`

 * *Files 0% similar despite different names*

```diff
@@ -77,15 +77,15 @@
                     ]
                 ).astype(np.float32)
             ),
         ]
     )
     TESTS.append(
         [
-            dict(num_cells=2, distort_steps=[(1.25,) * 3] * 3, mode="nearest", padding_mode="zeros"),
+            dict(num_cells=2, distort_steps=[(1.26,) * 3] * 3, mode="nearest", padding_mode="zeros"),
             p(np.indices([3, 3, 3])[:1].astype(np.float32)),
             p(
                 np.array(
                     [
                         [
                             [[0.0, 0.0, 0.0], [0.0, 0.0, 0.0], [0.0, 0.0, 0.0]],
                             [[1.0, 1.0, 0.0], [1.0, 1.0, 0.0], [0.0, 0.0, 0.0]],
```

### Comparing `monai-weekly-1.3.dev2329/tests/test_grid_distortiond.py` & `monai-weekly-1.3.dev2330/tests/test_grid_distortiond.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_grid_patch.py` & `monai-weekly-1.3.dev2330/tests/test_grid_patch.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_grid_patchd.py` & `monai-weekly-1.3.dev2330/tests/test_grid_patchd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_grid_pull.py` & `monai-weekly-1.3.dev2330/tests/test_grid_pull.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_grid_split.py` & `monai-weekly-1.3.dev2330/tests/test_grid_split.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_grid_splitd.py` & `monai-weekly-1.3.dev2330/tests/test_grid_splitd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_checkpoint_loader.py` & `monai-weekly-1.3.dev2330/tests/test_handler_checkpoint_loader.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_checkpoint_saver.py` & `monai-weekly-1.3.dev2330/tests/test_handler_checkpoint_saver.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_classification_saver.py` & `monai-weekly-1.3.dev2330/tests/test_handler_classification_saver.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_classification_saver_dist.py` & `monai-weekly-1.3.dev2330/tests/test_handler_classification_saver_dist.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_clearml_image.py` & `monai-weekly-1.3.dev2330/tests/test_handler_clearml_image.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_clearml_stats.py` & `monai-weekly-1.3.dev2330/tests/test_handler_clearml_stats.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_confusion_matrix.py` & `monai-weekly-1.3.dev2330/tests/test_handler_confusion_matrix.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_confusion_matrix_dist.py` & `monai-weekly-1.3.dev2330/tests/test_handler_confusion_matrix_dist.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_decollate_batch.py` & `monai-weekly-1.3.dev2330/tests/test_handler_decollate_batch.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_early_stop.py` & `monai-weekly-1.3.dev2330/tests/test_handler_early_stop.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_garbage_collector.py` & `monai-weekly-1.3.dev2330/tests/test_handler_garbage_collector.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_hausdorff_distance.py` & `monai-weekly-1.3.dev2330/tests/test_handler_hausdorff_distance.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_ignite_metric.py` & `monai-weekly-1.3.dev2330/tests/test_handler_ignite_metric.py`

 * *Files 0% similar despite different names*

```diff
@@ -23,15 +23,14 @@
 
 try:
     _, has_ignite = optional_import("ignite")
     from ignite.engine import Engine, Events
 except ImportError:
     has_ignite = False
 
-
 TEST_CASE_1 = [
     {"reduction": "none", "include_background": True},
     {},
     {"output_transform": from_engine(["pred", "label"])},
     0.25,
 ]
 TEST_CASE_2 = [
```

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_logfile.py` & `monai-weekly-1.3.dev2330/tests/test_handler_logfile.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_lr_scheduler.py` & `monai-weekly-1.3.dev2330/tests/test_handler_lr_scheduler.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_mean_dice.py` & `monai-weekly-1.3.dev2330/tests/test_handler_mean_dice.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_mean_iou.py` & `monai-weekly-1.3.dev2330/tests/test_handler_mean_iou.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_metric_logger.py` & `monai-weekly-1.3.dev2330/tests/test_handler_metric_logger.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_metrics_reloaded.py` & `monai-weekly-1.3.dev2330/tests/test_handler_metrics_reloaded.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_metrics_saver.py` & `monai-weekly-1.3.dev2330/tests/test_handler_metrics_saver.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_metrics_saver_dist.py` & `monai-weekly-1.3.dev2330/tests/test_handler_metrics_saver_dist.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_mlflow.py` & `monai-weekly-1.3.dev2330/tests/test_handler_mlflow.py`

 * *Files 20% similar despite different names*

```diff
@@ -19,16 +19,21 @@
 from concurrent.futures import ThreadPoolExecutor
 from unittest.mock import MagicMock
 
 import numpy as np
 from ignite.engine import Engine, Events
 from parameterized import parameterized
 
+from monai.apps import download_and_extract
+from monai.bundle import ConfigWorkflow, download
 from monai.handlers import MLFlowHandler
-from monai.utils import path_to_uri
+from monai.utils import optional_import, path_to_uri
+from tests.utils import skip_if_downloading_fails, skip_if_quick
+
+_, has_dataset_tracking = optional_import("mlflow", "2.4.0")
 
 
 def get_event_filter(e):
     def event_filter(_, event):
         if event in e:
             return True
         return False
@@ -226,10 +231,59 @@
                 futures[t] = executor.submit(dummy_train, t)
 
             for _, future in futures.items():
                 res = future.result()
                 self.tmpdir_list.append(res)
                 self.assertTrue(len(glob.glob(res)) > 0)
 
+    @skip_if_quick
+    @unittest.skipUnless(has_dataset_tracking, reason="Requires mlflow version >= 2.4.0.")
+    def test_dataset_tracking(self):
+        test_bundle_name = "endoscopic_tool_segmentation"
+        with tempfile.TemporaryDirectory() as tempdir:
+            resource = "https://github.com/Project-MONAI/MONAI-extra-test-data/releases/download/0.8.1/endoscopic_tool_dataset.zip"
+            md5 = "f82da47259c0a617202fb54624798a55"
+            compressed_file = os.path.join(tempdir, "endoscopic_tool_segmentation.zip")
+            data_dir = os.path.join(tempdir, "endoscopic_tool_dataset")
+            with skip_if_downloading_fails():
+                if not os.path.exists(data_dir):
+                    download_and_extract(resource, compressed_file, tempdir, md5)
+
+                download(test_bundle_name, bundle_dir=tempdir)
+
+                bundle_root = os.path.join(tempdir, test_bundle_name)
+                config_file = os.path.join(bundle_root, "configs/inference.json")
+                meta_file = os.path.join(bundle_root, "configs/metadata.json")
+                logging_file = os.path.join(bundle_root, "configs/logging.conf")
+                workflow = ConfigWorkflow(
+                    workflow="infer",
+                    config_file=config_file,
+                    meta_file=meta_file,
+                    logging_file=logging_file,
+                    init_id="initialize",
+                    run_id="run",
+                    final_id="finalize",
+                )
+
+                tracking_path = os.path.join(bundle_root, "eval")
+                workflow.bundle_root = bundle_root
+                workflow.dataset_dir = data_dir
+                workflow.initialize()
+                infer_dataset = workflow.dataset
+                mlflow_handler = MLFlowHandler(
+                    iteration_log=False,
+                    epoch_log=False,
+                    dataset_dict={"test": infer_dataset},
+                    tracking_uri=path_to_uri(tracking_path),
+                )
+                mlflow_handler.attach(workflow.evaluator)
+                workflow.run()
+                workflow.finalize()
+
+                cur_run = mlflow_handler.client.get_run(mlflow_handler.cur_run.info.run_id)
+                logged_nontrain_set = [x for x in cur_run.inputs.dataset_inputs if x.dataset.name.startswith("test")]
+                self.assertEqual(len(logged_nontrain_set), 1)
+                mlflow_handler.close()
+
 
 if __name__ == "__main__":
     unittest.main()
```

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_nvtx.py` & `monai-weekly-1.3.dev2330/tests/test_handler_nvtx.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_panoptic_quality.py` & `monai-weekly-1.3.dev2330/tests/test_handler_panoptic_quality.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_parameter_scheduler.py` & `monai-weekly-1.3.dev2330/tests/test_handler_parameter_scheduler.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_post_processing.py` & `monai-weekly-1.3.dev2330/tests/test_handler_post_processing.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_prob_map_producer.py` & `monai-weekly-1.3.dev2330/tests/test_handler_prob_map_producer.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_regression_metrics.py` & `monai-weekly-1.3.dev2330/tests/test_handler_regression_metrics.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_regression_metrics_dist.py` & `monai-weekly-1.3.dev2330/tests/test_handler_regression_metrics_dist.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_rocauc.py` & `monai-weekly-1.3.dev2330/tests/test_handler_rocauc.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_rocauc_dist.py` & `monai-weekly-1.3.dev2330/tests/test_handler_rocauc_dist.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_smartcache.py` & `monai-weekly-1.3.dev2330/tests/test_handler_smartcache.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_stats.py` & `monai-weekly-1.3.dev2330/tests/test_handler_stats.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_surface_distance.py` & `monai-weekly-1.3.dev2330/tests/test_handler_surface_distance.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_tb_image.py` & `monai-weekly-1.3.dev2330/tests/test_handler_tb_image.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_tb_stats.py` & `monai-weekly-1.3.dev2330/tests/test_handler_tb_stats.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_handler_validation.py` & `monai-weekly-1.3.dev2330/tests/test_handler_validation.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_hardnegsampler.py` & `monai-weekly-1.3.dev2330/tests/test_hardnegsampler.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_hashing.py` & `monai-weekly-1.3.dev2330/tests/test_hashing.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_hausdorff_distance.py` & `monai-weekly-1.3.dev2330/tests/test_hausdorff_distance.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_header_correct.py` & `monai-weekly-1.3.dev2330/tests/test_header_correct.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_highresnet.py` & `monai-weekly-1.3.dev2330/tests/test_highresnet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_hilbert_transform.py` & `monai-weekly-1.3.dev2330/tests/test_hilbert_transform.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_histogram_normalize.py` & `monai-weekly-1.3.dev2330/tests/test_histogram_normalize.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_histogram_normalized.py` & `monai-weekly-1.3.dev2330/tests/test_histogram_normalized.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_hovernet.py` & `monai-weekly-1.3.dev2330/tests/test_hovernet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_hovernet_instance_map_post_processing.py` & `monai-weekly-1.3.dev2330/tests/test_hovernet_instance_map_post_processing.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_hovernet_instance_map_post_processingd.py` & `monai-weekly-1.3.dev2330/tests/test_hovernet_instance_map_post_processingd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_hovernet_loss.py` & `monai-weekly-1.3.dev2330/tests/test_hovernet_loss.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_hovernet_nuclear_type_post_processing.py` & `monai-weekly-1.3.dev2330/tests/test_hovernet_nuclear_type_post_processing.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_hovernet_nuclear_type_post_processingd.py` & `monai-weekly-1.3.dev2330/tests/test_hovernet_nuclear_type_post_processingd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_identity.py` & `monai-weekly-1.3.dev2330/tests/test_identity.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_identityd.py` & `monai-weekly-1.3.dev2330/tests/test_identityd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_image_dataset.py` & `monai-weekly-1.3.dev2330/tests/test_image_dataset.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_image_filter.py` & `monai-weekly-1.3.dev2330/tests/test_image_filter.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_image_rw.py` & `monai-weekly-1.3.dev2330/tests/test_image_rw.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_img2tensorboard.py` & `monai-weekly-1.3.dev2330/tests/test_img2tensorboard.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_init_reader.py` & `monai-weekly-1.3.dev2330/tests/test_init_reader.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_integration_autorunner.py` & `monai-weekly-1.3.dev2330/tests/test_integration_autorunner.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_integration_bundle_run.py` & `monai-weekly-1.3.dev2330/tests/test_integration_bundle_run.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_integration_classification_2d.py` & `monai-weekly-1.3.dev2330/tests/test_integration_classification_2d.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_integration_determinism.py` & `monai-weekly-1.3.dev2330/tests/test_integration_determinism.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_integration_fast_train.py` & `monai-weekly-1.3.dev2330/tests/test_integration_fast_train.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_integration_gpu_customization.py` & `monai-weekly-1.3.dev2330/tests/test_integration_gpu_customization.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_integration_lazy_samples.py` & `monai-weekly-1.3.dev2330/tests/test_integration_lazy_samples.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_integration_nnunetv2_runner.py` & `monai-weekly-1.3.dev2330/tests/test_integration_nnunetv2_runner.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_integration_segmentation_3d.py` & `monai-weekly-1.3.dev2330/tests/test_integration_segmentation_3d.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_integration_sliding_window.py` & `monai-weekly-1.3.dev2330/tests/test_integration_sliding_window.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_integration_stn.py` & `monai-weekly-1.3.dev2330/tests/test_integration_stn.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_integration_unet_2d.py` & `monai-weekly-1.3.dev2330/tests/test_integration_unet_2d.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_integration_workers.py` & `monai-weekly-1.3.dev2330/tests/test_integration_workers.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_integration_workflows.py` & `monai-weekly-1.3.dev2330/tests/test_integration_workflows.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_integration_workflows_gan.py` & `monai-weekly-1.3.dev2330/tests/test_integration_workflows_gan.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_intensity_stats.py` & `monai-weekly-1.3.dev2330/tests/test_intensity_stats.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_intensity_statsd.py` & `monai-weekly-1.3.dev2330/tests/test_intensity_statsd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_inverse.py` & `monai-weekly-1.3.dev2330/tests/test_inverse.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_inverse_array.py` & `monai-weekly-1.3.dev2330/tests/test_inverse_array.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_inverse_collation.py` & `monai-weekly-1.3.dev2330/tests/test_inverse_collation.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_invert.py` & `monai-weekly-1.3.dev2330/tests/test_invert.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_invertd.py` & `monai-weekly-1.3.dev2330/tests/test_invertd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_is_supported_format.py` & `monai-weekly-1.3.dev2330/tests/test_is_supported_format.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_iterable_dataset.py` & `monai-weekly-1.3.dev2330/tests/test_iterable_dataset.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_itk_torch_bridge.py` & `monai-weekly-1.3.dev2330/tests/test_itk_torch_bridge.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_itk_writer.py` & `monai-weekly-1.3.dev2330/tests/test_itk_writer.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_k_space_spike_noise.py` & `monai-weekly-1.3.dev2330/tests/test_k_space_spike_noise.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_k_space_spike_noised.py` & `monai-weekly-1.3.dev2330/tests/test_k_space_spike_noised.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_keep_largest_connected_component.py` & `monai-weekly-1.3.dev2330/tests/test_keep_largest_connected_component.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_keep_largest_connected_componentd.py` & `monai-weekly-1.3.dev2330/tests/test_keep_largest_connected_componentd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_kspace_mask.py` & `monai-weekly-1.3.dev2330/tests/test_kspace_mask.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_label_filter.py` & `monai-weekly-1.3.dev2330/tests/test_label_filter.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_label_filterd.py` & `monai-weekly-1.3.dev2330/tests/test_label_filterd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_label_quality_score.py` & `monai-weekly-1.3.dev2330/tests/test_label_quality_score.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_label_to_contour.py` & `monai-weekly-1.3.dev2330/tests/test_label_to_contour.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_label_to_contourd.py` & `monai-weekly-1.3.dev2330/tests/test_label_to_contourd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_label_to_mask.py` & `monai-weekly-1.3.dev2330/tests/test_label_to_mask.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_label_to_maskd.py` & `monai-weekly-1.3.dev2330/tests/test_label_to_maskd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_lambda.py` & `monai-weekly-1.3.dev2330/tests/test_lambda.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_lambdad.py` & `monai-weekly-1.3.dev2330/tests/test_lambdad.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_lesion_froc.py` & `monai-weekly-1.3.dev2330/tests/test_lesion_froc.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_list_data_collate.py` & `monai-weekly-1.3.dev2330/tests/test_list_data_collate.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_list_to_dict.py` & `monai-weekly-1.3.dev2330/tests/test_list_to_dict.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_lltm.py` & `monai-weekly-1.3.dev2330/tests/test_lltm.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_lmdbdataset.py` & `monai-weekly-1.3.dev2330/tests/test_lmdbdataset.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_lmdbdataset_dist.py` & `monai-weekly-1.3.dev2330/tests/test_lmdbdataset_dist.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_load_decathlon_datalist.py` & `monai-weekly-1.3.dev2330/tests/test_load_decathlon_datalist.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_load_image.py` & `monai-weekly-1.3.dev2330/tests/test_load_image.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_load_imaged.py` & `monai-weekly-1.3.dev2330/tests/test_load_imaged.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_load_spacing_orientation.py` & `monai-weekly-1.3.dev2330/tests/test_load_spacing_orientation.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_loader_semaphore.py` & `monai-weekly-1.3.dev2330/tests/test_loader_semaphore.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_local_normalized_cross_correlation_loss.py` & `monai-weekly-1.3.dev2330/tests/test_local_normalized_cross_correlation_loss.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_localnet.py` & `monai-weekly-1.3.dev2330/tests/test_localnet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_localnet_block.py` & `monai-weekly-1.3.dev2330/tests/test_localnet_block.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_look_up_option.py` & `monai-weekly-1.3.dev2330/tests/test_look_up_option.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_loss_metric.py` & `monai-weekly-1.3.dev2330/tests/test_loss_metric.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_lr_finder.py` & `monai-weekly-1.3.dev2330/tests/test_lr_finder.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_lr_scheduler.py` & `monai-weekly-1.3.dev2330/tests/test_lr_scheduler.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_make_nifti.py` & `monai-weekly-1.3.dev2330/tests/test_make_nifti.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_map_binary_to_indices.py` & `monai-weekly-1.3.dev2330/tests/test_map_binary_to_indices.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_map_classes_to_indices.py` & `monai-weekly-1.3.dev2330/tests/test_map_classes_to_indices.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_map_label_value.py` & `monai-weekly-1.3.dev2330/tests/test_map_label_value.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_map_label_valued.py` & `monai-weekly-1.3.dev2330/tests/test_map_label_valued.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_map_transform.py` & `monai-weekly-1.3.dev2330/tests/test_map_transform.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_mask_intensity.py` & `monai-weekly-1.3.dev2330/tests/test_mask_intensity.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_mask_intensityd.py` & `monai-weekly-1.3.dev2330/tests/test_mask_intensityd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_masked_dice_loss.py` & `monai-weekly-1.3.dev2330/tests/test_masked_dice_loss.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_masked_loss.py` & `monai-weekly-1.3.dev2330/tests/test_masked_loss.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_masked_patch_wsi_dataset.py` & `monai-weekly-1.3.dev2330/tests/test_masked_patch_wsi_dataset.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_matshow3d.py` & `monai-weekly-1.3.dev2330/tests/test_matshow3d.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_mean_ensemble.py` & `monai-weekly-1.3.dev2330/tests/test_mean_ensemble.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_mean_ensembled.py` & `monai-weekly-1.3.dev2330/tests/test_mean_ensembled.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_median_filter.py` & `monai-weekly-1.3.dev2330/tests/test_median_filter.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_median_smooth.py` & `monai-weekly-1.3.dev2330/tests/test_median_smooth.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_median_smoothd.py` & `monai-weekly-1.3.dev2330/tests/test_median_smoothd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_mednistdataset.py` & `monai-weekly-1.3.dev2330/tests/test_mednistdataset.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_meta_affine.py` & `monai-weekly-1.3.dev2330/tests/test_meta_affine.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_meta_tensor.py` & `monai-weekly-1.3.dev2330/tests/test_meta_tensor.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_metatensor_integration.py` & `monai-weekly-1.3.dev2330/tests/test_metatensor_integration.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_metrics_reloaded.py` & `monai-weekly-1.3.dev2330/tests/test_metrics_reloaded.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_milmodel.py` & `monai-weekly-1.3.dev2330/tests/test_milmodel.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_mlp.py` & `monai-weekly-1.3.dev2330/tests/test_mlp.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_mmar_download.py` & `monai-weekly-1.3.dev2330/tests/test_mmar_download.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_module_list.py` & `monai-weekly-1.3.dev2330/tests/test_module_list.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_monai_env_vars.py` & `monai-weekly-1.3.dev2330/tests/test_monai_env_vars.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_monai_utils_misc.py` & `monai-weekly-1.3.dev2330/tests/test_monai_utils_misc.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_mri_utils.py` & `monai-weekly-1.3.dev2330/tests/test_mri_utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_multi_scale.py` & `monai-weekly-1.3.dev2330/tests/test_multi_scale.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_net_adapter.py` & `monai-weekly-1.3.dev2330/tests/test_net_adapter.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_network_consistency.py` & `monai-weekly-1.3.dev2330/tests/test_network_consistency.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_nifti_endianness.py` & `monai-weekly-1.3.dev2330/tests/test_nifti_endianness.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_nifti_header_revise.py` & `monai-weekly-1.3.dev2330/tests/test_nifti_header_revise.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_nifti_rw.py` & `monai-weekly-1.3.dev2330/tests/test_nifti_rw.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_normalize_intensity.py` & `monai-weekly-1.3.dev2330/tests/test_normalize_intensity.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_normalize_intensityd.py` & `monai-weekly-1.3.dev2330/tests/test_normalize_intensityd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_npzdictitemdataset.py` & `monai-weekly-1.3.dev2330/tests/test_npzdictitemdataset.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_nrrd_reader.py` & `monai-weekly-1.3.dev2330/tests/test_nrrd_reader.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_nuclick_transforms.py` & `monai-weekly-1.3.dev2330/tests/test_nuclick_transforms.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_numpy_reader.py` & `monai-weekly-1.3.dev2330/tests/test_numpy_reader.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_nvtx_decorator.py` & `monai-weekly-1.3.dev2330/tests/test_nvtx_decorator.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_nvtx_transform.py` & `monai-weekly-1.3.dev2330/tests/test_nvtx_transform.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_occlusion_sensitivity.py` & `monai-weekly-1.3.dev2330/tests/test_occlusion_sensitivity.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_one_of.py` & `monai-weekly-1.3.dev2330/tests/test_one_of.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_optim_novograd.py` & `monai-weekly-1.3.dev2330/tests/test_optim_novograd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_optional_import.py` & `monai-weekly-1.3.dev2330/tests/test_optional_import.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_ori_ras_lps.py` & `monai-weekly-1.3.dev2330/tests/test_ori_ras_lps.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_orientation.py` & `monai-weekly-1.3.dev2330/tests/test_orientation.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_orientationd.py` & `monai-weekly-1.3.dev2330/tests/test_orientationd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_p3d_block.py` & `monai-weekly-1.3.dev2330/tests/test_p3d_block.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_pad_collation.py` & `monai-weekly-1.3.dev2330/tests/test_pad_collation.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_pad_mode.py` & `monai-weekly-1.3.dev2330/tests/test_pad_mode.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_parallel_execution.py` & `monai-weekly-1.3.dev2330/tests/test_parallel_execution.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_parallel_execution_dist.py` & `monai-weekly-1.3.dev2330/tests/test_parallel_execution_dist.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_partition_dataset.py` & `monai-weekly-1.3.dev2330/tests/test_partition_dataset.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_partition_dataset_classes.py` & `monai-weekly-1.3.dev2330/tests/test_partition_dataset_classes.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_patch_dataset.py` & `monai-weekly-1.3.dev2330/tests/test_patch_dataset.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_patch_inferer.py` & `monai-weekly-1.3.dev2330/tests/test_patch_inferer.py`

 * *Files 0% similar despite different names*

```diff
@@ -123,15 +123,14 @@
 TEST_CASE_10_STR_MERGER = [
     TENSOR_4x4,
     dict(splitter=SlidingWindowSplitter(patch_size=(2, 2)), merger_cls="monai.inferers.merger.AvgMerger"),
     lambda x: x,
     TENSOR_4x4,
 ]
 
-
 # non-divisible patch_size leading to larger image (without matching spatial shape)
 TEST_CASE_11_PADDING = [
     TENSOR_4x4,
     dict(
         splitter=SlidingWindowSplitter(patch_size=(2, 3), pad_mode="constant", pad_value=0.0),
         merger_cls=AvgMerger,
         match_spatial_shape=False,
@@ -168,15 +167,14 @@
 TEST_CASE_15_MULTITHREADD_BUFFER = [
     TENSOR_4x4,
     dict(splitter=SlidingWindowSplitter(patch_size=(2, 2)), merger_cls=AvgMerger, buffer_size=4, batch_size=4),
     lambda x: x,
     TENSOR_4x4,
 ]
 
-
 # list of tensor output
 TEST_CASE_0_LIST_TENSOR = [
     TENSOR_4x4,
     dict(splitter=SlidingWindowSplitter(patch_size=(2, 2)), merger_cls=AvgMerger),
     lambda x: (x, x),
     (TENSOR_4x4, TENSOR_4x4),
 ]
```

### Comparing `monai-weekly-1.3.dev2329/tests/test_patch_wsi_dataset.py` & `monai-weekly-1.3.dev2330/tests/test_patch_wsi_dataset.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_patchembedding.py` & `monai-weekly-1.3.dev2330/tests/test_patchembedding.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_pathology_he_stain.py` & `monai-weekly-1.3.dev2330/tests/test_pathology_he_stain.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_pathology_he_stain_dict.py` & `monai-weekly-1.3.dev2330/tests/test_pathology_he_stain_dict.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_pathology_prob_nms.py` & `monai-weekly-1.3.dev2330/tests/test_pathology_prob_nms.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_persistentdataset.py` & `monai-weekly-1.3.dev2330/tests/test_persistentdataset.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_persistentdataset_dist.py` & `monai-weekly-1.3.dev2330/tests/test_persistentdataset_dist.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_phl_cpu.py` & `monai-weekly-1.3.dev2330/tests/test_phl_cpu.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_phl_cuda.py` & `monai-weekly-1.3.dev2330/tests/test_phl_cuda.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_pil_reader.py` & `monai-weekly-1.3.dev2330/tests/test_pil_reader.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_plot_2d_or_3d_image.py` & `monai-weekly-1.3.dev2330/tests/test_plot_2d_or_3d_image.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_png_rw.py` & `monai-weekly-1.3.dev2330/tests/test_png_rw.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_polyval.py` & `monai-weekly-1.3.dev2330/tests/test_polyval.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_prepare_batch_default.py` & `monai-weekly-1.3.dev2330/tests/test_prepare_batch_default.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_prepare_batch_default_dist.py` & `monai-weekly-1.3.dev2330/tests/test_prepare_batch_default_dist.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_prepare_batch_extra_input.py` & `monai-weekly-1.3.dev2330/tests/test_prepare_batch_extra_input.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_prepare_batch_hovernet.py` & `monai-weekly-1.3.dev2330/tests/test_prepare_batch_hovernet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_preset_filters.py` & `monai-weekly-1.3.dev2330/tests/test_preset_filters.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_print_info.py` & `monai-weekly-1.3.dev2330/tests/test_print_info.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_print_transform_backends.py` & `monai-weekly-1.3.dev2330/tests/test_print_transform_backends.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_probnms.py` & `monai-weekly-1.3.dev2330/tests/test_probnms.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_probnmsd.py` & `monai-weekly-1.3.dev2330/tests/test_probnmsd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_profiling.py` & `monai-weekly-1.3.dev2330/tests/test_profiling.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_pytorch_version_after.py` & `monai-weekly-1.3.dev2330/tests/test_pytorch_version_after.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_query_memory.py` & `monai-weekly-1.3.dev2330/tests/test_query_memory.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_quicknat.py` & `monai-weekly-1.3.dev2330/tests/test_quicknat.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_adjust_contrast.py` & `monai-weekly-1.3.dev2330/tests/test_rand_adjust_contrast.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_adjust_contrastd.py` & `monai-weekly-1.3.dev2330/tests/test_rand_adjust_contrastd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_affine.py` & `monai-weekly-1.3.dev2330/tests/test_rand_affine.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_affine_grid.py` & `monai-weekly-1.3.dev2330/tests/test_rand_affine_grid.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_affined.py` & `monai-weekly-1.3.dev2330/tests/test_rand_affined.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_axis_flip.py` & `monai-weekly-1.3.dev2330/tests/test_rand_axis_flip.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_axis_flipd.py` & `monai-weekly-1.3.dev2330/tests/test_rand_axis_flipd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_bias_field.py` & `monai-weekly-1.3.dev2330/tests/test_rand_bias_field.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_bias_fieldd.py` & `monai-weekly-1.3.dev2330/tests/test_rand_bias_fieldd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_coarse_dropout.py` & `monai-weekly-1.3.dev2330/tests/test_rand_coarse_dropout.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_coarse_dropoutd.py` & `monai-weekly-1.3.dev2330/tests/test_rand_coarse_dropoutd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_coarse_shuffle.py` & `monai-weekly-1.3.dev2330/tests/test_rand_coarse_shuffle.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_coarse_shuffled.py` & `monai-weekly-1.3.dev2330/tests/test_rand_coarse_shuffled.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_crop_by_label_classes.py` & `monai-weekly-1.3.dev2330/tests/test_rand_crop_by_label_classes.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_crop_by_label_classesd.py` & `monai-weekly-1.3.dev2330/tests/test_rand_crop_by_label_classesd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_crop_by_pos_neg_label.py` & `monai-weekly-1.3.dev2330/tests/test_rand_crop_by_pos_neg_label.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_crop_by_pos_neg_labeld.py` & `monai-weekly-1.3.dev2330/tests/test_rand_crop_by_pos_neg_labeld.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_cucim_dict_transform.py` & `monai-weekly-1.3.dev2330/tests/test_rand_cucim_dict_transform.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_cucim_transform.py` & `monai-weekly-1.3.dev2330/tests/test_rand_cucim_transform.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_deform_grid.py` & `monai-weekly-1.3.dev2330/tests/test_rand_deform_grid.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_elastic_2d.py` & `monai-weekly-1.3.dev2330/tests/test_rand_elastic_2d.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_elastic_3d.py` & `monai-weekly-1.3.dev2330/tests/test_rand_elastic_3d.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_elasticd_2d.py` & `monai-weekly-1.3.dev2330/tests/test_rand_elasticd_2d.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_elasticd_3d.py` & `monai-weekly-1.3.dev2330/tests/test_rand_elasticd_3d.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_flip.py` & `monai-weekly-1.3.dev2330/tests/test_rand_flip.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_flipd.py` & `monai-weekly-1.3.dev2330/tests/test_rand_flipd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_gaussian_noise.py` & `monai-weekly-1.3.dev2330/tests/test_rand_gaussian_noise.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_gaussian_noised.py` & `monai-weekly-1.3.dev2330/tests/test_rand_gaussian_noised.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_gaussian_sharpen.py` & `monai-weekly-1.3.dev2330/tests/test_rand_gaussian_sharpen.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_gaussian_sharpend.py` & `monai-weekly-1.3.dev2330/tests/test_rand_gaussian_sharpend.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_gaussian_smooth.py` & `monai-weekly-1.3.dev2330/tests/test_rand_gaussian_smooth.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_gaussian_smoothd.py` & `monai-weekly-1.3.dev2330/tests/test_rand_gaussian_smoothd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_gibbs_noise.py` & `monai-weekly-1.3.dev2330/tests/test_rand_gibbs_noise.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_gibbs_noised.py` & `monai-weekly-1.3.dev2330/tests/test_rand_gibbs_noised.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_grid_distortion.py` & `monai-weekly-1.3.dev2330/tests/test_rand_grid_distortion.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_grid_distortiond.py` & `monai-weekly-1.3.dev2330/tests/test_rand_grid_distortiond.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_grid_patch.py` & `monai-weekly-1.3.dev2330/tests/test_rand_grid_patch.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_grid_patchd.py` & `monai-weekly-1.3.dev2330/tests/test_rand_grid_patchd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_histogram_shift.py` & `monai-weekly-1.3.dev2330/tests/test_rand_histogram_shift.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_histogram_shiftd.py` & `monai-weekly-1.3.dev2330/tests/test_rand_histogram_shiftd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_k_space_spike_noise.py` & `monai-weekly-1.3.dev2330/tests/test_rand_k_space_spike_noise.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_k_space_spike_noised.py` & `monai-weekly-1.3.dev2330/tests/test_rand_k_space_spike_noised.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_lambda.py` & `monai-weekly-1.3.dev2330/tests/test_rand_lambda.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_lambdad.py` & `monai-weekly-1.3.dev2330/tests/test_rand_lambdad.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_rician_noise.py` & `monai-weekly-1.3.dev2330/tests/test_rand_rician_noise.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_rician_noised.py` & `monai-weekly-1.3.dev2330/tests/test_rand_rician_noised.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_rotate.py` & `monai-weekly-1.3.dev2330/tests/test_rand_rotate.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_rotate90.py` & `monai-weekly-1.3.dev2330/tests/test_rand_rotate90.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_rotate90d.py` & `monai-weekly-1.3.dev2330/tests/test_rand_rotate90d.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_rotated.py` & `monai-weekly-1.3.dev2330/tests/test_rand_rotated.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_scale_crop.py` & `monai-weekly-1.3.dev2330/tests/test_rand_scale_crop.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_scale_cropd.py` & `monai-weekly-1.3.dev2330/tests/test_rand_scale_cropd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_scale_intensity.py` & `monai-weekly-1.3.dev2330/tests/test_rand_scale_intensity.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_scale_intensity_fixed_mean.py` & `monai-weekly-1.3.dev2330/tests/test_rand_scale_intensity_fixed_mean.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_scale_intensity_fixed_meand.py` & `monai-weekly-1.3.dev2330/tests/test_rand_scale_intensity_fixed_meand.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_scale_intensityd.py` & `monai-weekly-1.3.dev2330/tests/test_rand_scale_intensityd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_shift_intensity.py` & `monai-weekly-1.3.dev2330/tests/test_rand_shift_intensity.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_shift_intensityd.py` & `monai-weekly-1.3.dev2330/tests/test_rand_shift_intensityd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_spatial_crop.py` & `monai-weekly-1.3.dev2330/tests/test_rand_spatial_crop.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_spatial_crop_samples.py` & `monai-weekly-1.3.dev2330/tests/test_rand_spatial_crop_samples.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_spatial_crop_samplesd.py` & `monai-weekly-1.3.dev2330/tests/test_rand_spatial_crop_samplesd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_spatial_cropd.py` & `monai-weekly-1.3.dev2330/tests/test_rand_spatial_cropd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_std_shift_intensity.py` & `monai-weekly-1.3.dev2330/tests/test_rand_std_shift_intensity.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_std_shift_intensityd.py` & `monai-weekly-1.3.dev2330/tests/test_rand_std_shift_intensityd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_weighted_crop.py` & `monai-weekly-1.3.dev2330/tests/test_rand_weighted_crop.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_weighted_cropd.py` & `monai-weekly-1.3.dev2330/tests/test_rand_weighted_cropd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_zoom.py` & `monai-weekly-1.3.dev2330/tests/test_rand_zoom.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rand_zoomd.py` & `monai-weekly-1.3.dev2330/tests/test_rand_zoomd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_randidentity.py` & `monai-weekly-1.3.dev2330/tests/test_randidentity.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_random_order.py` & `monai-weekly-1.3.dev2330/tests/test_random_order.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_randomizable.py` & `monai-weekly-1.3.dev2330/tests/test_randomizable.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_randomizable_transform_type.py` & `monai-weekly-1.3.dev2330/tests/test_randomizable_transform_type.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_randtorchvisiond.py` & `monai-weekly-1.3.dev2330/tests/test_randtorchvisiond.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rankfilter_dist.py` & `monai-weekly-1.3.dev2330/tests/test_rankfilter_dist.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_recon_net_utils.py` & `monai-weekly-1.3.dev2330/tests/test_recon_net_utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_reference_based_normalize_intensity.py` & `monai-weekly-1.3.dev2330/tests/test_reference_based_normalize_intensity.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_reference_based_spatial_cropd.py` & `monai-weekly-1.3.dev2330/tests/test_reference_based_spatial_cropd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_reference_resolver.py` & `monai-weekly-1.3.dev2330/tests/test_reference_resolver.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_reg_loss_integration.py` & `monai-weekly-1.3.dev2330/tests/test_reg_loss_integration.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_regunet.py` & `monai-weekly-1.3.dev2330/tests/test_regunet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_regunet_block.py` & `monai-weekly-1.3.dev2330/tests/test_regunet_block.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_remove_repeated_channel.py` & `monai-weekly-1.3.dev2330/tests/test_remove_repeated_channel.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_remove_repeated_channeld.py` & `monai-weekly-1.3.dev2330/tests/test_remove_repeated_channeld.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_remove_small_objects.py` & `monai-weekly-1.3.dev2330/tests/test_remove_small_objects.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_repeat_channel.py` & `monai-weekly-1.3.dev2330/tests/test_repeat_channel.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_repeat_channeld.py` & `monai-weekly-1.3.dev2330/tests/test_repeat_channeld.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_replace_module.py` & `monai-weekly-1.3.dev2330/tests/test_replace_module.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_require_pkg.py` & `monai-weekly-1.3.dev2330/tests/test_require_pkg.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_resample.py` & `monai-weekly-1.3.dev2330/tests/test_resample.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_resample_backends.py` & `monai-weekly-1.3.dev2330/tests/test_resample_backends.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_resample_datalist.py` & `monai-weekly-1.3.dev2330/tests/test_resample_datalist.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_resample_to_match.py` & `monai-weekly-1.3.dev2330/tests/test_resample_to_match.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_resample_to_matchd.py` & `monai-weekly-1.3.dev2330/tests/test_resample_to_matchd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_resampler.py` & `monai-weekly-1.3.dev2330/tests/test_resampler.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_resize.py` & `monai-weekly-1.3.dev2330/tests/test_resize.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_resize_with_pad_or_crop.py` & `monai-weekly-1.3.dev2330/tests/test_resize_with_pad_or_crop.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_resize_with_pad_or_cropd.py` & `monai-weekly-1.3.dev2330/tests/test_resize_with_pad_or_cropd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_resized.py` & `monai-weekly-1.3.dev2330/tests/test_resized.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_resnet.py` & `monai-weekly-1.3.dev2330/tests/test_resnet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_retinanet.py` & `monai-weekly-1.3.dev2330/tests/test_retinanet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_retinanet_detector.py` & `monai-weekly-1.3.dev2330/tests/test_retinanet_detector.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_retinanet_predict_utils.py` & `monai-weekly-1.3.dev2330/tests/test_retinanet_predict_utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rotate.py` & `monai-weekly-1.3.dev2330/tests/test_rotate.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rotate90.py` & `monai-weekly-1.3.dev2330/tests/test_rotate90.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rotate90d.py` & `monai-weekly-1.3.dev2330/tests/test_rotate90d.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_rotated.py` & `monai-weekly-1.3.dev2330/tests/test_rotated.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_safe_dtype_range.py` & `monai-weekly-1.3.dev2330/tests/test_safe_dtype_range.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_saliency_inferer.py` & `monai-weekly-1.3.dev2330/tests/test_saliency_inferer.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_sample_slices.py` & `monai-weekly-1.3.dev2330/tests/test_sample_slices.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_sampler_dist.py` & `monai-weekly-1.3.dev2330/tests/test_sampler_dist.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_save_classificationd.py` & `monai-weekly-1.3.dev2330/tests/test_save_classificationd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_save_image.py` & `monai-weekly-1.3.dev2330/tests/test_save_image.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_save_imaged.py` & `monai-weekly-1.3.dev2330/tests/test_save_imaged.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_save_state.py` & `monai-weekly-1.3.dev2330/tests/test_save_state.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_savitzky_golay_filter.py` & `monai-weekly-1.3.dev2330/tests/test_savitzky_golay_filter.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_savitzky_golay_smooth.py` & `monai-weekly-1.3.dev2330/tests/test_savitzky_golay_smooth.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_savitzky_golay_smoothd.py` & `monai-weekly-1.3.dev2330/tests/test_savitzky_golay_smoothd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_scale_intensity.py` & `monai-weekly-1.3.dev2330/tests/test_scale_intensity.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_scale_intensity_fixed_mean.py` & `monai-weekly-1.3.dev2330/tests/test_scale_intensity_fixed_mean.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_scale_intensity_range.py` & `monai-weekly-1.3.dev2330/tests/test_scale_intensity_range.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_scale_intensity_range_percentiles.py` & `monai-weekly-1.3.dev2330/tests/test_scale_intensity_range_percentiles.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_scale_intensity_range_percentilesd.py` & `monai-weekly-1.3.dev2330/tests/test_scale_intensity_range_percentilesd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_scale_intensity_ranged.py` & `monai-weekly-1.3.dev2330/tests/test_scale_intensity_ranged.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_scale_intensityd.py` & `monai-weekly-1.3.dev2330/tests/test_scale_intensityd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_se_block.py` & `monai-weekly-1.3.dev2330/tests/test_se_block.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_se_blocks.py` & `monai-weekly-1.3.dev2330/tests/test_se_blocks.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_seg_loss_integration.py` & `monai-weekly-1.3.dev2330/tests/test_seg_loss_integration.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_segresnet.py` & `monai-weekly-1.3.dev2330/tests/test_segresnet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_segresnet_block.py` & `monai-weekly-1.3.dev2330/tests/test_segresnet_block.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_segresnet_ds.py` & `monai-weekly-1.3.dev2330/tests/test_segresnet_ds.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_select_cross_validation_folds.py` & `monai-weekly-1.3.dev2330/tests/test_select_cross_validation_folds.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_select_itemsd.py` & `monai-weekly-1.3.dev2330/tests/test_select_itemsd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_selfattention.py` & `monai-weekly-1.3.dev2330/tests/test_selfattention.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_senet.py` & `monai-weekly-1.3.dev2330/tests/test_senet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_separable_filter.py` & `monai-weekly-1.3.dev2330/tests/test_separable_filter.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_set_determinism.py` & `monai-weekly-1.3.dev2330/tests/test_set_determinism.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_set_visible_devices.py` & `monai-weekly-1.3.dev2330/tests/test_set_visible_devices.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_shift_intensity.py` & `monai-weekly-1.3.dev2330/tests/test_shift_intensity.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_shift_intensityd.py` & `monai-weekly-1.3.dev2330/tests/test_shift_intensityd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_shuffle_buffer.py` & `monai-weekly-1.3.dev2330/tests/test_shuffle_buffer.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_signal_continuouswavelet.py` & `monai-weekly-1.3.dev2330/tests/test_signal_continuouswavelet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_signal_fillempty.py` & `monai-weekly-1.3.dev2330/tests/test_signal_fillempty.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_signal_rand_add_gaussiannoise.py` & `monai-weekly-1.3.dev2330/tests/test_signal_rand_add_gaussiannoise.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_signal_rand_add_sine.py` & `monai-weekly-1.3.dev2330/tests/test_signal_rand_add_sine.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_signal_rand_add_sine_partial.py` & `monai-weekly-1.3.dev2330/tests/test_signal_rand_add_sine_partial.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_signal_rand_add_squarepulse.py` & `monai-weekly-1.3.dev2330/tests/test_signal_rand_add_squarepulse.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_signal_rand_add_squarepulse_partial.py` & `monai-weekly-1.3.dev2330/tests/test_signal_rand_add_squarepulse_partial.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_signal_rand_drop.py` & `monai-weekly-1.3.dev2330/tests/test_signal_rand_drop.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_signal_rand_scale.py` & `monai-weekly-1.3.dev2330/tests/test_signal_rand_scale.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_signal_rand_shift.py` & `monai-weekly-1.3.dev2330/tests/test_signal_rand_shift.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_signal_remove_frequency.py` & `monai-weekly-1.3.dev2330/tests/test_signal_remove_frequency.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_simple_aspp.py` & `monai-weekly-1.3.dev2330/tests/test_simple_aspp.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_simulatedelay.py` & `monai-weekly-1.3.dev2330/tests/test_simulatedelay.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_simulatedelayd.py` & `monai-weekly-1.3.dev2330/tests/test_simulatedelayd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_skip_connection.py` & `monai-weekly-1.3.dev2330/tests/test_skip_connection.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_slice_inferer.py` & `monai-weekly-1.3.dev2330/tests/test_slice_inferer.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_sliding_patch_wsi_dataset.py` & `monai-weekly-1.3.dev2330/tests/test_sliding_patch_wsi_dataset.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_sliding_window_hovernet_inference.py` & `monai-weekly-1.3.dev2330/tests/test_sliding_window_hovernet_inference.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_sliding_window_inference.py` & `monai-weekly-1.3.dev2330/tests/test_sliding_window_inference.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_sliding_window_splitter.py` & `monai-weekly-1.3.dev2330/tests/test_sliding_window_splitter.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_smartcachedataset.py` & `monai-weekly-1.3.dev2330/tests/test_smartcachedataset.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_smooth_field.py` & `monai-weekly-1.3.dev2330/tests/test_smooth_field.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_sobel_gradient.py` & `monai-weekly-1.3.dev2330/tests/test_sobel_gradient.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_sobel_gradientd.py` & `monai-weekly-1.3.dev2330/tests/test_sobel_gradientd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_some_of.py` & `monai-weekly-1.3.dev2330/tests/test_some_of.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_spacing.py` & `monai-weekly-1.3.dev2330/tests/test_spacing.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_spacingd.py` & `monai-weekly-1.3.dev2330/tests/test_spacingd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_spatial_combine_transforms.py` & `monai-weekly-1.3.dev2330/tests/test_spatial_combine_transforms.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_spatial_crop.py` & `monai-weekly-1.3.dev2330/tests/test_spatial_crop.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_spatial_cropd.py` & `monai-weekly-1.3.dev2330/tests/test_spatial_cropd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_spatial_pad.py` & `monai-weekly-1.3.dev2330/tests/test_spatial_pad.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_spatial_padd.py` & `monai-weekly-1.3.dev2330/tests/test_spatial_padd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_spatial_resample.py` & `monai-weekly-1.3.dev2330/tests/test_spatial_resample.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_spatial_resampled.py` & `monai-weekly-1.3.dev2330/tests/test_spatial_resampled.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_split_channel.py` & `monai-weekly-1.3.dev2330/tests/test_split_channel.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_split_channeld.py` & `monai-weekly-1.3.dev2330/tests/test_split_channeld.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_splitdim.py` & `monai-weekly-1.3.dev2330/tests/test_splitdim.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_splitdimd.py` & `monai-weekly-1.3.dev2330/tests/test_splitdimd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_squeezedim.py` & `monai-weekly-1.3.dev2330/tests/test_squeezedim.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_squeezedimd.py` & `monai-weekly-1.3.dev2330/tests/test_squeezedimd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_ssim_loss.py` & `monai-weekly-1.3.dev2330/tests/test_ssim_loss.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_ssim_metric.py` & `monai-weekly-1.3.dev2330/tests/test_ssim_metric.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_state_cacher.py` & `monai-weekly-1.3.dev2330/tests/test_state_cacher.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_std_shift_intensity.py` & `monai-weekly-1.3.dev2330/tests/test_std_shift_intensity.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_std_shift_intensityd.py` & `monai-weekly-1.3.dev2330/tests/test_std_shift_intensityd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_str2bool.py` & `monai-weekly-1.3.dev2330/tests/test_str2bool.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_str2list.py` & `monai-weekly-1.3.dev2330/tests/test_str2list.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_subpixel_upsample.py` & `monai-weekly-1.3.dev2330/tests/test_subpixel_upsample.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_surface_dice.py` & `monai-weekly-1.3.dev2330/tests/test_surface_dice.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_surface_distance.py` & `monai-weekly-1.3.dev2330/tests/test_surface_distance.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_swin_unetr.py` & `monai-weekly-1.3.dev2330/tests/test_swin_unetr.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_synthetic.py` & `monai-weekly-1.3.dev2330/tests/test_synthetic.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_tciadataset.py` & `monai-weekly-1.3.dev2330/tests/test_tciadataset.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_testtimeaugmentation.py` & `monai-weekly-1.3.dev2330/tests/test_testtimeaugmentation.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_text_encoding.py` & `monai-weekly-1.3.dev2330/tests/test_text_encoding.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_thread_buffer.py` & `monai-weekly-1.3.dev2330/tests/test_thread_buffer.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_threadcontainer.py` & `monai-weekly-1.3.dev2330/tests/test_threadcontainer.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_threshold_intensity.py` & `monai-weekly-1.3.dev2330/tests/test_threshold_intensity.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_threshold_intensityd.py` & `monai-weekly-1.3.dev2330/tests/test_threshold_intensityd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_timedcall_dist.py` & `monai-weekly-1.3.dev2330/tests/test_timedcall_dist.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_to_contiguous.py` & `monai-weekly-1.3.dev2330/tests/test_to_contiguous.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_to_cupy.py` & `monai-weekly-1.3.dev2330/tests/test_to_cupy.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_to_cupyd.py` & `monai-weekly-1.3.dev2330/tests/test_to_cupyd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_to_device.py` & `monai-weekly-1.3.dev2330/tests/test_to_device.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_to_deviced.py` & `monai-weekly-1.3.dev2330/tests/test_to_deviced.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_to_from_meta_tensord.py` & `monai-weekly-1.3.dev2330/tests/test_to_from_meta_tensord.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_to_numpy.py` & `monai-weekly-1.3.dev2330/tests/test_to_numpy.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_to_numpyd.py` & `monai-weekly-1.3.dev2330/tests/test_to_numpyd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_to_onehot.py` & `monai-weekly-1.3.dev2330/tests/test_to_onehot.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_to_pil.py` & `monai-weekly-1.3.dev2330/tests/test_to_pil.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_to_pild.py` & `monai-weekly-1.3.dev2330/tests/test_to_pild.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_to_tensor.py` & `monai-weekly-1.3.dev2330/tests/test_to_tensor.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_to_tensord.py` & `monai-weekly-1.3.dev2330/tests/test_to_tensord.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_torchscript_utils.py` & `monai-weekly-1.3.dev2330/tests/test_torchscript_utils.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_torchvision.py` & `monai-weekly-1.3.dev2330/tests/test_torchvision.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_torchvision_fc_model.py` & `monai-weekly-1.3.dev2330/tests/test_torchvision_fc_model.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_torchvisiond.py` & `monai-weekly-1.3.dev2330/tests/test_torchvisiond.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_traceable_transform.py` & `monai-weekly-1.3.dev2330/tests/test_traceable_transform.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_train_mode.py` & `monai-weekly-1.3.dev2330/tests/test_train_mode.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_trainable_bilateral.py` & `monai-weekly-1.3.dev2330/tests/test_trainable_bilateral.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_trainable_joint_bilateral.py` & `monai-weekly-1.3.dev2330/tests/test_trainable_joint_bilateral.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_transchex.py` & `monai-weekly-1.3.dev2330/tests/test_transchex.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_transform.py` & `monai-weekly-1.3.dev2330/tests/test_transform.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_transformerblock.py` & `monai-weekly-1.3.dev2330/tests/test_transformerblock.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_transpose.py` & `monai-weekly-1.3.dev2330/tests/test_transpose.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_transposed.py` & `monai-weekly-1.3.dev2330/tests/test_transposed.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_tversky_loss.py` & `monai-weekly-1.3.dev2330/tests/test_tversky_loss.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_unet.py` & `monai-weekly-1.3.dev2330/tests/test_unet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_unetr.py` & `monai-weekly-1.3.dev2330/tests/test_unetr.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_unetr_block.py` & `monai-weekly-1.3.dev2330/tests/test_unetr_block.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_unified_focal_loss.py` & `monai-weekly-1.3.dev2330/tests/test_unified_focal_loss.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_upsample_block.py` & `monai-weekly-1.3.dev2330/tests/test_upsample_block.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_utils_pytorch_numpy_unification.py` & `monai-weekly-1.3.dev2330/tests/test_utils_pytorch_numpy_unification.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_varautoencoder.py` & `monai-weekly-1.3.dev2330/tests/test_varautoencoder.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_varnet.py` & `monai-weekly-1.3.dev2330/tests/test_varnet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_version_leq.py` & `monai-weekly-1.3.dev2330/tests/test_version_leq.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_video_datasets.py` & `monai-weekly-1.3.dev2330/tests/test_video_datasets.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_vis_cam.py` & `monai-weekly-1.3.dev2330/tests/test_vis_cam.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_vis_gradbased.py` & `monai-weekly-1.3.dev2330/tests/test_vis_gradbased.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_vis_gradcam.py` & `monai-weekly-1.3.dev2330/tests/test_vis_gradcam.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_vit.py` & `monai-weekly-1.3.dev2330/tests/test_vit.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_vitautoenc.py` & `monai-weekly-1.3.dev2330/tests/test_vitautoenc.py`

 * *Files 6% similar despite different names*

```diff
@@ -45,15 +45,15 @@
                     TEST_CASE_Vitautoenc.append(test_case)
 
 TEST_CASE_Vitautoenc.append(
     [
         {
             "in_channels": 1,
             "img_size": (512, 512, 32),
-            "patch_size": (16, 16, 16),
+            "patch_size": (64, 64, 16),
             "hidden_size": 768,
             "mlp_dim": 3072,
             "num_layers": 4,
             "num_heads": 12,
             "pos_embed": "conv",
             "dropout_rate": 0.6,
             "spatial_dims": 3,
@@ -142,11 +142,24 @@
                 hidden_size=768,
                 mlp_dim=3072,
                 num_layers=12,
                 num_heads=12,
                 pos_embed="perc",
                 dropout_rate=0.3,
             )
+
+        with self.assertRaises(ValueError):
+            ViTAutoEnc(
+                in_channels=4,
+                img_size=(96, 96, 96),
+                patch_size=(9, 9, 9),
+                hidden_size=768,
+                mlp_dim=3072,
+                num_layers=12,
+                num_heads=12,
+                pos_embed="perc",
+                dropout_rate=0.3,
+            )
 
 
 if __name__ == "__main__":
     unittest.main()
```

### Comparing `monai-weekly-1.3.dev2329/tests/test_vnet.py` & `monai-weekly-1.3.dev2330/tests/test_vnet.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_vote_ensemble.py` & `monai-weekly-1.3.dev2330/tests/test_vote_ensemble.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_vote_ensembled.py` & `monai-weekly-1.3.dev2330/tests/test_vote_ensembled.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_warp.py` & `monai-weekly-1.3.dev2330/tests/test_warp.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_watershed.py` & `monai-weekly-1.3.dev2330/tests/test_watershed.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_watershedd.py` & `monai-weekly-1.3.dev2330/tests/test_watershedd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_weight_init.py` & `monai-weekly-1.3.dev2330/tests/test_weight_init.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_weighted_random_sampler_dist.py` & `monai-weekly-1.3.dev2330/tests/test_weighted_random_sampler_dist.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_with_allow_missing_keys.py` & `monai-weekly-1.3.dev2330/tests/test_with_allow_missing_keys.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_write_metrics_reports.py` & `monai-weekly-1.3.dev2330/tests/test_write_metrics_reports.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_wsi_sliding_window_splitter.py` & `monai-weekly-1.3.dev2330/tests/test_wsi_sliding_window_splitter.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_wsireader.py` & `monai-weekly-1.3.dev2330/tests/test_wsireader.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_zarr_avg_merger.py` & `monai-weekly-1.3.dev2330/tests/test_zarr_avg_merger.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_zipdataset.py` & `monai-weekly-1.3.dev2330/tests/test_zipdataset.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_zoom.py` & `monai-weekly-1.3.dev2330/tests/test_zoom.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_zoom_affine.py` & `monai-weekly-1.3.dev2330/tests/test_zoom_affine.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/tests/test_zoomd.py` & `monai-weekly-1.3.dev2330/tests/test_zoomd.py`

 * *Files identical despite different names*

### Comparing `monai-weekly-1.3.dev2329/versioneer.py` & `monai-weekly-1.3.dev2330/versioneer.py`

 * *Files identical despite different names*

