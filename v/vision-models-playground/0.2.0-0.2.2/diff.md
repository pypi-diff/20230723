# Comparing `tmp/vision_models_playground-0.2.0.tar.gz` & `tmp/vision_models_playground-0.2.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "vision_models_playground-0.2.0.tar", last modified: Sun Jul 23 12:20:08 2023, max compression
+gzip compressed data, was "vision_models_playground-0.2.2.tar", last modified: Sun Jul 23 13:59:35 2023, max compression
```

## Comparing `vision_models_playground-0.2.0.tar` & `vision_models_playground-0.2.2.tar`

### file list

```diff
@@ -1,144 +1,144 @@
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.861549 vision_models_playground-0.2.0/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1073 2022-06-26 07:21:11.000000 vision_models_playground-0.2.0/LICENSE
--rw-rw-r--   0 akriel    (1000) akriel    (1000)    21375 2023-07-23 12:20:08.861549 vision_models_playground-0.2.0/PKG-INFO
--rw-rw-r--   0 akriel    (1000) akriel    (1000)    20698 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/README.md
--rw-rw-r--   0 akriel    (1000) akriel    (1000)       38 2023-07-23 12:20:08.861549 vision_models_playground-0.2.0/setup.cfg
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1435 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/setup.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.853549 vision_models_playground-0.2.0/vision_models_playground/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      546 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/__init__.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.853549 vision_models_playground-0.2.0/vision_models_playground/components/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      277 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/__init__.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.853549 vision_models_playground-0.2.0/vision_models_playground/components/activations/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      781 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/components/activations/__init__.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      181 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/activations/geglu.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      788 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/activations/gelu.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      396 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/activations/hard_sigmoid.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      463 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/activations/mish.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      335 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/activations/quick_geglu.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      787 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/activations/quick_gelu.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      184 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/activations/relu_squared.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      420 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/activations/swish.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.853549 vision_models_playground-0.2.0/vision_models_playground/components/attention/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1337 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/components/attention/__init__.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1941 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/attention/attend.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     2544 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/attention/attention.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     2439 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/attention/compressor.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1117 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/attention/feed_forward.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      350 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/attention/post_norm.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      750 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/attention/pre_norm.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1301 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/attention/tied_embedding.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     5177 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/attention/transformer.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     5624 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/attention/transformer_decoder.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     2905 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/attention/transformer_decoder_layer.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     3728 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/attention/transformer_encoder.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     2053 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/attention/transformer_encoder_layer.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.857549 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1622 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/__init__.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1479 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/bottleneck_block.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     2500 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/conv_attend.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     2649 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/conv_attention.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1047 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/conv_block.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      959 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/conv_embedding.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1878 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/conv_projection.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     2575 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/conv_transformer.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      868 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/conv_transposed_block.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      817 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/double_conv_block.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1048 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/downscale_block.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1128 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/residual_block.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1176 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/upscale_block.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     2111 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/upscale_concat_block.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     2517 2023-07-06 17:51:36.000000 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/yolo_v1_head.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.857549 vision_models_playground-0.2.0/vision_models_playground/components/dropout/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      131 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/components/dropout/__init__.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1608 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/dropout/drop_path.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.857549 vision_models_playground-0.2.0/vision_models_playground/components/position_embedding/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      166 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/components/position_embedding/__init__.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     4111 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/position_embedding/fourier_embedding.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.857549 vision_models_playground-0.2.0/vision_models_playground/data_structures/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      170 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/data_structures/__init__.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     7701 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/data_structures/yolo_bounding_box.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.857549 vision_models_playground-0.2.0/vision_models_playground/datasets/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1283 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/datasets/__init__.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     3935 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/datasets/datasets.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)    11513 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/datasets/yolo_pascal_voc_dataset.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     3570 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/datasets/yolo_pascal_voc_dataset_aug.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.857549 vision_models_playground-0.2.0/vision_models_playground/evaluate/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      342 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/evaluate/__init__.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     8111 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/evaluate/evaluate_models.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     2344 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/evaluate/evaluate_yolo.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.857549 vision_models_playground-0.2.0/vision_models_playground/losses/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      126 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/losses/__init__.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     6136 2023-07-04 21:22:37.000000 vision_models_playground-0.2.0/vision_models_playground/losses/yolo_v1_loss.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      146 2023-07-23 12:20:05.000000 vision_models_playground-0.2.0/vision_models_playground/metadata.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.857549 vision_models_playground-0.2.0/vision_models_playground/metrics/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      724 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/metrics/__init__.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     4402 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/metrics/intersection_over_union.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1305 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/metrics/loss_tracker.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     4555 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/metrics/wrapper.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.857549 vision_models_playground-0.2.0/vision_models_playground/models/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      153 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/models/__init__.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.857549 vision_models_playground-0.2.0/vision_models_playground/models/classifiers/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1694 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/models/classifiers/__init__.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1954 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/models/classifiers/conv_classifier.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     7176 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/models/classifiers/conv_vision_transformer.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1574 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/models/classifiers/ff_classifier.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     5744 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/models/classifiers/perceiver.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     4389 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/models/classifiers/resnet.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     3541 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/models/classifiers/vision_perceiver.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     3043 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/models/classifiers/vision_transformer.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.857549 vision_models_playground-0.2.0/vision_models_playground/models/generative/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)       74 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/models/generative/__init__.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.857549 vision_models_playground-0.2.0/vision_models_playground/models/generative/adverserial/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      358 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/models/generative/adverserial/__init__.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     7464 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/models/generative/adverserial/gan.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1377 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/models/generative/adverserial/mnist_discriminator.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1291 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/models/generative/adverserial/mnist_generator.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.857549 vision_models_playground-0.2.0/vision_models_playground/models/segmentation/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      416 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/models/segmentation/__init__.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     3177 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/models/segmentation/unet.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     4981 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/models/segmentation/yolo_v1.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.857549 vision_models_playground-0.2.0/vision_models_playground/optimizers/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      110 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/optimizers/__init__.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     2756 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/optimizers/lion.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.857549 vision_models_playground-0.2.0/vision_models_playground/pipelines/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      206 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/pipelines/__init__.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1919 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/pipelines/base.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     8578 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/pipelines/yolo.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.861549 vision_models_playground-0.2.0/vision_models_playground/train/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      421 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/train/__init__.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1491 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/train/train_classifier.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)    11481 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/train/train_models.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     3639 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/train/train_yolo.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.861549 vision_models_playground-0.2.0/vision_models_playground/transforms/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     4364 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/__init__.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     5221 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/auto.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      482 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/base.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      491 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/choose_one.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1001 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/clamp.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      915 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/compose.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     2016 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/conversions.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1317 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/normalize.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     2599 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/pad.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      495 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/probability_transform.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     6092 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/random_affine.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1109 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/random_horizontal_flip.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     3131 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/random_perspective.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     2564 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/random_resized_crop.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     4163 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/random_rotation.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1079 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/random_vertical_flip.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     2585 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/resize.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      930 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/transform.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.861549 vision_models_playground-0.2.0/vision_models_playground/utility/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     2264 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/utility/__init__.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     2134 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/utility/config.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      566 2023-07-04 19:56:28.000000 vision_models_playground-0.2.0/vision_models_playground/utility/functions.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     4158 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/utility/hub.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     2156 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/utility/load_models.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      440 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/utility/masks.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      789 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/utility/visualize.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.853549 vision_models_playground-0.2.0/vision_models_playground.egg-info/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)    21375 2023-07-23 12:20:08.000000 vision_models_playground-0.2.0/vision_models_playground.egg-info/PKG-INFO
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     6474 2023-07-23 12:20:08.000000 vision_models_playground-0.2.0/vision_models_playground.egg-info/SOURCES.txt
--rw-rw-r--   0 akriel    (1000) akriel    (1000)        1 2023-07-23 12:20:08.000000 vision_models_playground-0.2.0/vision_models_playground.egg-info/dependency_links.txt
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      159 2023-07-23 12:20:08.000000 vision_models_playground-0.2.0/vision_models_playground.egg-info/requires.txt
--rw-rw-r--   0 akriel    (1000) akriel    (1000)       25 2023-07-23 12:20:08.000000 vision_models_playground-0.2.0/vision_models_playground.egg-info/top_level.txt
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 13:59:35.976039 vision_models_playground-0.2.2/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1073 2022-06-26 07:21:11.000000 vision_models_playground-0.2.2/LICENSE
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)    21375 2023-07-23 13:59:35.976039 vision_models_playground-0.2.2/PKG-INFO
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)    20698 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/README.md
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)       38 2023-07-23 13:59:35.976039 vision_models_playground-0.2.2/setup.cfg
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1320 2023-07-23 13:56:48.000000 vision_models_playground-0.2.2/setup.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 13:59:35.968038 vision_models_playground-0.2.2/vision_models_playground/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      546 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/__init__.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 13:59:35.968038 vision_models_playground-0.2.2/vision_models_playground/components/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      277 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/__init__.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 13:59:35.968038 vision_models_playground-0.2.2/vision_models_playground/components/activations/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      781 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/components/activations/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      181 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/activations/geglu.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      788 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/activations/gelu.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      396 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/activations/hard_sigmoid.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      463 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/activations/mish.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      335 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/activations/quick_geglu.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      787 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/activations/quick_gelu.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      184 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/activations/relu_squared.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      420 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/activations/swish.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 13:59:35.972039 vision_models_playground-0.2.2/vision_models_playground/components/attention/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1337 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/components/attention/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1941 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/attention/attend.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2544 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/attention/attention.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2439 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/attention/compressor.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1117 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/attention/feed_forward.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      350 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/attention/post_norm.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      750 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/attention/pre_norm.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1301 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/attention/tied_embedding.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     5177 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/attention/transformer.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     5624 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/attention/transformer_decoder.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2905 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/attention/transformer_decoder_layer.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     3728 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/attention/transformer_encoder.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2053 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/attention/transformer_encoder_layer.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 13:59:35.972039 vision_models_playground-0.2.2/vision_models_playground/components/convolutions/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1622 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/components/convolutions/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1479 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/convolutions/bottleneck_block.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2500 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/convolutions/conv_attend.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2649 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/convolutions/conv_attention.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1047 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/convolutions/conv_block.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      959 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/convolutions/conv_embedding.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1878 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/convolutions/conv_projection.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2575 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/convolutions/conv_transformer.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      868 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/convolutions/conv_transposed_block.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      817 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/convolutions/double_conv_block.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1048 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/convolutions/downscale_block.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1128 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/convolutions/residual_block.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1176 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/convolutions/upscale_block.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2111 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/convolutions/upscale_concat_block.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2517 2023-07-06 17:51:36.000000 vision_models_playground-0.2.2/vision_models_playground/components/convolutions/yolo_v1_head.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 13:59:35.972039 vision_models_playground-0.2.2/vision_models_playground/components/dropout/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      131 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/components/dropout/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1608 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/dropout/drop_path.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 13:59:35.972039 vision_models_playground-0.2.2/vision_models_playground/components/position_embedding/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      166 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/components/position_embedding/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     4111 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/components/position_embedding/fourier_embedding.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 13:59:35.972039 vision_models_playground-0.2.2/vision_models_playground/data_structures/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      170 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/data_structures/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     7701 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/data_structures/yolo_bounding_box.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 13:59:35.972039 vision_models_playground-0.2.2/vision_models_playground/datasets/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1283 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/datasets/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     3935 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/datasets/datasets.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)    11513 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/datasets/yolo_pascal_voc_dataset.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     3570 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/datasets/yolo_pascal_voc_dataset_aug.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 13:59:35.972039 vision_models_playground-0.2.2/vision_models_playground/evaluate/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      342 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/evaluate/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     8111 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/evaluate/evaluate_models.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2313 2023-07-23 13:42:38.000000 vision_models_playground-0.2.2/vision_models_playground/evaluate/evaluate_yolo.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 13:59:35.972039 vision_models_playground-0.2.2/vision_models_playground/losses/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      126 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/losses/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     6136 2023-07-04 21:22:37.000000 vision_models_playground-0.2.2/vision_models_playground/losses/yolo_v1_loss.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      146 2023-07-23 13:59:34.000000 vision_models_playground-0.2.2/vision_models_playground/metadata.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 13:59:35.972039 vision_models_playground-0.2.2/vision_models_playground/metrics/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      724 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/metrics/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     4402 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/metrics/intersection_over_union.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1305 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/metrics/loss_tracker.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     4555 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/metrics/wrapper.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 13:59:35.972039 vision_models_playground-0.2.2/vision_models_playground/models/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      153 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/models/__init__.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 13:59:35.972039 vision_models_playground-0.2.2/vision_models_playground/models/classifiers/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1694 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/models/classifiers/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1954 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/models/classifiers/conv_classifier.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     7176 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/models/classifiers/conv_vision_transformer.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1574 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/models/classifiers/ff_classifier.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     5744 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/models/classifiers/perceiver.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     4389 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/models/classifiers/resnet.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     3541 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/models/classifiers/vision_perceiver.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     3043 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/models/classifiers/vision_transformer.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 13:59:35.972039 vision_models_playground-0.2.2/vision_models_playground/models/generative/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)       74 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/models/generative/__init__.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 13:59:35.976039 vision_models_playground-0.2.2/vision_models_playground/models/generative/adverserial/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      358 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/models/generative/adverserial/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     7464 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/models/generative/adverserial/gan.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1377 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/models/generative/adverserial/mnist_discriminator.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1291 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/models/generative/adverserial/mnist_generator.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 13:59:35.976039 vision_models_playground-0.2.2/vision_models_playground/models/segmentation/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      416 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/models/segmentation/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     3177 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/models/segmentation/unet.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     4981 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/models/segmentation/yolo_v1.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 13:59:35.976039 vision_models_playground-0.2.2/vision_models_playground/optimizers/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      110 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/optimizers/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2756 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/optimizers/lion.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 13:59:35.976039 vision_models_playground-0.2.2/vision_models_playground/pipelines/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      206 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/pipelines/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1919 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/pipelines/base.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     8578 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/pipelines/yolo.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 13:59:35.976039 vision_models_playground-0.2.2/vision_models_playground/train/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      421 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/train/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1455 2023-07-23 13:48:24.000000 vision_models_playground-0.2.2/vision_models_playground/train/train_classifier.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)    11481 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/train/train_models.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     3639 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/train/train_yolo.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 13:59:35.976039 vision_models_playground-0.2.2/vision_models_playground/transforms/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     4364 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/transforms/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     5221 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/transforms/auto.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      482 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/transforms/base.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      491 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/transforms/choose_one.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1001 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/transforms/clamp.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      915 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/transforms/compose.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2016 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/transforms/conversions.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1317 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/transforms/normalize.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2599 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/transforms/pad.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      495 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/transforms/probability_transform.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     6092 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/transforms/random_affine.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1109 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/transforms/random_horizontal_flip.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     3131 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/transforms/random_perspective.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2564 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/transforms/random_resized_crop.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     4163 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/transforms/random_rotation.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1079 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/transforms/random_vertical_flip.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2585 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/transforms/resize.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      930 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/transforms/transform.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 13:59:35.976039 vision_models_playground-0.2.2/vision_models_playground/utility/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2264 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/utility/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2134 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/utility/config.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      566 2023-07-04 19:56:28.000000 vision_models_playground-0.2.2/vision_models_playground/utility/functions.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     4158 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/utility/hub.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2156 2023-07-23 12:11:29.000000 vision_models_playground-0.2.2/vision_models_playground/utility/load_models.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      440 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/utility/masks.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      789 2023-07-04 19:56:10.000000 vision_models_playground-0.2.2/vision_models_playground/utility/visualize.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 13:59:35.968038 vision_models_playground-0.2.2/vision_models_playground.egg-info/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)    21375 2023-07-23 13:59:35.000000 vision_models_playground-0.2.2/vision_models_playground.egg-info/PKG-INFO
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     6474 2023-07-23 13:59:35.000000 vision_models_playground-0.2.2/vision_models_playground.egg-info/SOURCES.txt
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)        1 2023-07-23 13:59:35.000000 vision_models_playground-0.2.2/vision_models_playground.egg-info/dependency_links.txt
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      260 2023-07-23 13:59:35.000000 vision_models_playground-0.2.2/vision_models_playground.egg-info/requires.txt
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)       25 2023-07-23 13:59:35.000000 vision_models_playground-0.2.2/vision_models_playground.egg-info/top_level.txt
```

### Comparing `vision_models_playground-0.2.0/LICENSE` & `vision_models_playground-0.2.2/LICENSE`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/PKG-INFO` & `vision_models_playground-0.2.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: vision_models_playground
-Version: 0.2.0
+Version: 0.2.2
 Summary: Akriel's vision models playground
 Home-page: https://github.com/Akrielz/vision_models_playground
 Author: Alexandru Stirbu
 Author-email: Stirbu.Alexandru.Net@outlook.com
 License: MIT
 Keywords: artificial intelligence,deep learning,transformer,attention mechanism,computer vision
 Classifier: Development Status :: 4 - Beta
```

### Comparing `vision_models_playground-0.2.0/README.md` & `vision_models_playground-0.2.2/README.md`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/setup.py` & `vision_models_playground-0.2.2/setup.py`

 * *Files 13% similar despite different names*

```diff
@@ -6,14 +6,17 @@
 
 with open(path.join(here, 'README.md'), encoding='utf-8') as f:
     long_description = f.read()
 
 __version__ = "placeholder"
 exec(open('vision_models_playground/metadata.py').read())
 
+with open(path.join(here, 'vision_models_playground/requirements.txt'), encoding='utf-8') as f:
+    requirements = f.read().splitlines()
+
 setup(
     name='vision_models_playground',
     packages=find_packages(),
     version=__version__,
     license='MIT',
     description="Akriel's vision models playground",
     long_description=long_description,
@@ -24,25 +27,15 @@
     keywords=[
         'artificial intelligence',
         'deep learning',
         'transformer',
         'attention mechanism',
         'computer vision',
     ],
-    install_requires=[
-        'einops>=0.4.1',
-        'torch>=1.10.0',
-        'rotary-embedding-torch>=0.1.0',
-        'torchvision>=0.11.1',
-        'colorama>=0.4.5',
-        'tqdm>=4.64.0',
-        'torchmetrics>=0.9.3',
-        'numpy>=1.22.0',
-        'matplotlib>=3.5.2',
-    ],
+    install_requires=requirements,
     classifiers=[
         'Development Status :: 4 - Beta',
         'Intended Audience :: Developers',
         'Topic :: Scientific/Engineering :: Artificial Intelligence',
         'License :: OSI Approved :: MIT License',
         'Programming Language :: Python :: 3.8',
     ],
```

### Comparing `vision_models_playground-0.2.0/vision_models_playground/__init__.py` & `vision_models_playground-0.2.2/vision_models_playground/__init__.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/activations/__init__.py` & `vision_models_playground-0.2.2/vision_models_playground/components/activations/__init__.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/activations/gelu.py` & `vision_models_playground-0.2.2/vision_models_playground/components/activations/gelu.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/activations/quick_gelu.py` & `vision_models_playground-0.2.2/vision_models_playground/components/activations/quick_gelu.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/attention/__init__.py` & `vision_models_playground-0.2.2/vision_models_playground/components/attention/__init__.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/attention/attend.py` & `vision_models_playground-0.2.2/vision_models_playground/components/attention/attend.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/attention/attention.py` & `vision_models_playground-0.2.2/vision_models_playground/components/attention/attention.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/attention/compressor.py` & `vision_models_playground-0.2.2/vision_models_playground/components/attention/compressor.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/attention/feed_forward.py` & `vision_models_playground-0.2.2/vision_models_playground/components/attention/feed_forward.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/attention/pre_norm.py` & `vision_models_playground-0.2.2/vision_models_playground/components/attention/pre_norm.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/attention/tied_embedding.py` & `vision_models_playground-0.2.2/vision_models_playground/components/attention/tied_embedding.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/attention/transformer.py` & `vision_models_playground-0.2.2/vision_models_playground/components/attention/transformer.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/attention/transformer_decoder.py` & `vision_models_playground-0.2.2/vision_models_playground/components/attention/transformer_decoder.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/attention/transformer_decoder_layer.py` & `vision_models_playground-0.2.2/vision_models_playground/components/attention/transformer_decoder_layer.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/attention/transformer_encoder.py` & `vision_models_playground-0.2.2/vision_models_playground/components/attention/transformer_encoder.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/attention/transformer_encoder_layer.py` & `vision_models_playground-0.2.2/vision_models_playground/components/attention/transformer_encoder_layer.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/convolutions/__init__.py` & `vision_models_playground-0.2.2/vision_models_playground/components/convolutions/__init__.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/convolutions/bottleneck_block.py` & `vision_models_playground-0.2.2/vision_models_playground/components/convolutions/bottleneck_block.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/convolutions/conv_attend.py` & `vision_models_playground-0.2.2/vision_models_playground/components/convolutions/conv_attend.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/convolutions/conv_attention.py` & `vision_models_playground-0.2.2/vision_models_playground/components/convolutions/conv_attention.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/convolutions/conv_block.py` & `vision_models_playground-0.2.2/vision_models_playground/components/convolutions/conv_block.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/convolutions/conv_embedding.py` & `vision_models_playground-0.2.2/vision_models_playground/components/convolutions/conv_embedding.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/convolutions/conv_projection.py` & `vision_models_playground-0.2.2/vision_models_playground/components/convolutions/conv_projection.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/convolutions/conv_transformer.py` & `vision_models_playground-0.2.2/vision_models_playground/components/convolutions/conv_transformer.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/convolutions/conv_transposed_block.py` & `vision_models_playground-0.2.2/vision_models_playground/components/convolutions/conv_transposed_block.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/convolutions/double_conv_block.py` & `vision_models_playground-0.2.2/vision_models_playground/components/convolutions/double_conv_block.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/convolutions/downscale_block.py` & `vision_models_playground-0.2.2/vision_models_playground/components/convolutions/downscale_block.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/convolutions/residual_block.py` & `vision_models_playground-0.2.2/vision_models_playground/components/convolutions/residual_block.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/convolutions/upscale_block.py` & `vision_models_playground-0.2.2/vision_models_playground/components/convolutions/upscale_block.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/convolutions/upscale_concat_block.py` & `vision_models_playground-0.2.2/vision_models_playground/components/convolutions/upscale_concat_block.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/convolutions/yolo_v1_head.py` & `vision_models_playground-0.2.2/vision_models_playground/components/convolutions/yolo_v1_head.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/dropout/drop_path.py` & `vision_models_playground-0.2.2/vision_models_playground/components/dropout/drop_path.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/components/position_embedding/fourier_embedding.py` & `vision_models_playground-0.2.2/vision_models_playground/components/position_embedding/fourier_embedding.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/data_structures/yolo_bounding_box.py` & `vision_models_playground-0.2.2/vision_models_playground/data_structures/yolo_bounding_box.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/datasets/__init__.py` & `vision_models_playground-0.2.2/vision_models_playground/datasets/__init__.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/datasets/datasets.py` & `vision_models_playground-0.2.2/vision_models_playground/datasets/datasets.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/datasets/yolo_pascal_voc_dataset.py` & `vision_models_playground-0.2.2/vision_models_playground/datasets/yolo_pascal_voc_dataset.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/datasets/yolo_pascal_voc_dataset_aug.py` & `vision_models_playground-0.2.2/vision_models_playground/datasets/yolo_pascal_voc_dataset_aug.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/evaluate/evaluate_models.py` & `vision_models_playground-0.2.2/vision_models_playground/evaluate/evaluate_models.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/evaluate/evaluate_yolo.py` & `vision_models_playground-0.2.2/vision_models_playground/evaluate/evaluate_yolo.py`

 * *Files 3% similar despite different names*

```diff
@@ -4,16 +4,16 @@
 import torchmetrics
 from torch import nn
 from torchmetrics import Accuracy, AveragePrecision, AUROC, Dice, F1Score
 
 from vision_models_playground.datasets.datasets import get_voc_detection_dataset_yolo
 from vision_models_playground.evaluate.evaluate_models import evaluate_model
 from vision_models_playground.losses.yolo_v1_loss import YoloV1Loss
-from vision_models_playground.metrics.wrapper import YoloV1ClassMetricWrapper, YoloV1MeanAveragePrecision
-from vision_models_playground.utility.load_models import load_best_model
+from vision_models_playground.metrics.wrapper import YoloV1ClassMetricWrapper
+from vision_models_playground.utility import load_model_from_dir
 
 
 def evaluate_yolo_v1(
         model: nn.Module,
         test_dataset: Optional[torch.utils.data.Dataset] = None,
         loss_fn: Optional[Callable] = None,
         batch_size: int = 64,
@@ -60,13 +60,13 @@
         metrics,
         device=device,
         num_workers=num_workers,
     )
 
 
 def main():
-    model = load_best_model("models/train/ResNetYoloV1/2023-07-06_14-37-23")
+    model = load_model_from_dir("models/train/ResNetYoloV1/2023-07-06_14-37-23")
     evaluate_yolo_v1(model)
 
 
 if __name__ == '__main__':
-    main()
+    main()
```

### Comparing `vision_models_playground-0.2.0/vision_models_playground/losses/yolo_v1_loss.py` & `vision_models_playground-0.2.2/vision_models_playground/losses/yolo_v1_loss.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/metrics/__init__.py` & `vision_models_playground-0.2.2/vision_models_playground/metrics/__init__.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/metrics/intersection_over_union.py` & `vision_models_playground-0.2.2/vision_models_playground/metrics/intersection_over_union.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/metrics/loss_tracker.py` & `vision_models_playground-0.2.2/vision_models_playground/metrics/loss_tracker.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/metrics/wrapper.py` & `vision_models_playground-0.2.2/vision_models_playground/metrics/wrapper.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/models/classifiers/__init__.py` & `vision_models_playground-0.2.2/vision_models_playground/models/classifiers/__init__.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/models/classifiers/conv_classifier.py` & `vision_models_playground-0.2.2/vision_models_playground/models/classifiers/conv_classifier.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/models/classifiers/conv_vision_transformer.py` & `vision_models_playground-0.2.2/vision_models_playground/models/classifiers/conv_vision_transformer.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/models/classifiers/ff_classifier.py` & `vision_models_playground-0.2.2/vision_models_playground/models/classifiers/ff_classifier.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/models/classifiers/perceiver.py` & `vision_models_playground-0.2.2/vision_models_playground/models/classifiers/perceiver.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/models/classifiers/resnet.py` & `vision_models_playground-0.2.2/vision_models_playground/models/classifiers/resnet.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/models/classifiers/vision_perceiver.py` & `vision_models_playground-0.2.2/vision_models_playground/models/classifiers/vision_perceiver.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/models/classifiers/vision_transformer.py` & `vision_models_playground-0.2.2/vision_models_playground/models/classifiers/vision_transformer.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/models/generative/adverserial/gan.py` & `vision_models_playground-0.2.2/vision_models_playground/models/generative/adverserial/gan.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/models/generative/adverserial/mnist_discriminator.py` & `vision_models_playground-0.2.2/vision_models_playground/models/generative/adverserial/mnist_discriminator.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/models/generative/adverserial/mnist_generator.py` & `vision_models_playground-0.2.2/vision_models_playground/models/generative/adverserial/mnist_generator.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/models/segmentation/unet.py` & `vision_models_playground-0.2.2/vision_models_playground/models/segmentation/unet.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/models/segmentation/yolo_v1.py` & `vision_models_playground-0.2.2/vision_models_playground/models/segmentation/yolo_v1.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/optimizers/lion.py` & `vision_models_playground-0.2.2/vision_models_playground/optimizers/lion.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/pipelines/base.py` & `vision_models_playground-0.2.2/vision_models_playground/pipelines/base.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/pipelines/yolo.py` & `vision_models_playground-0.2.2/vision_models_playground/pipelines/yolo.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/train/train_classifier.py` & `vision_models_playground-0.2.2/vision_models_playground/train/train_classifier.py`

 * *Files 4% similar despite different names*

```diff
@@ -32,15 +32,14 @@
     }
 
     if metrics is None:
         metrics = [
             Accuracy(**metrics_kwargs),
             AveragePrecision(**metrics_kwargs),
             AUROC(**metrics_kwargs),
-            Dice(**metrics_kwargs),
             F1Score(**metrics_kwargs),
         ]
 
     train_model(
         model,
         train_dataset,
         test_dataset,
```

### Comparing `vision_models_playground-0.2.0/vision_models_playground/train/train_models.py` & `vision_models_playground-0.2.2/vision_models_playground/train/train_models.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/train/train_yolo.py` & `vision_models_playground-0.2.2/vision_models_playground/train/train_yolo.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/transforms/__init__.py` & `vision_models_playground-0.2.2/vision_models_playground/transforms/__init__.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/transforms/auto.py` & `vision_models_playground-0.2.2/vision_models_playground/transforms/auto.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/transforms/clamp.py` & `vision_models_playground-0.2.2/vision_models_playground/transforms/clamp.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/transforms/compose.py` & `vision_models_playground-0.2.2/vision_models_playground/transforms/compose.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/transforms/conversions.py` & `vision_models_playground-0.2.2/vision_models_playground/transforms/conversions.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/transforms/normalize.py` & `vision_models_playground-0.2.2/vision_models_playground/transforms/normalize.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/transforms/pad.py` & `vision_models_playground-0.2.2/vision_models_playground/transforms/pad.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/transforms/random_affine.py` & `vision_models_playground-0.2.2/vision_models_playground/transforms/random_affine.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/transforms/random_horizontal_flip.py` & `vision_models_playground-0.2.2/vision_models_playground/transforms/random_horizontal_flip.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/transforms/random_perspective.py` & `vision_models_playground-0.2.2/vision_models_playground/transforms/random_perspective.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/transforms/random_resized_crop.py` & `vision_models_playground-0.2.2/vision_models_playground/transforms/random_resized_crop.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/transforms/random_rotation.py` & `vision_models_playground-0.2.2/vision_models_playground/transforms/random_rotation.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/transforms/random_vertical_flip.py` & `vision_models_playground-0.2.2/vision_models_playground/transforms/random_vertical_flip.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/transforms/resize.py` & `vision_models_playground-0.2.2/vision_models_playground/transforms/resize.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/transforms/transform.py` & `vision_models_playground-0.2.2/vision_models_playground/transforms/transform.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/utility/__init__.py` & `vision_models_playground-0.2.2/vision_models_playground/utility/__init__.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/utility/config.py` & `vision_models_playground-0.2.2/vision_models_playground/utility/config.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/utility/functions.py` & `vision_models_playground-0.2.2/vision_models_playground/utility/functions.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/utility/hub.py` & `vision_models_playground-0.2.2/vision_models_playground/utility/hub.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/utility/load_models.py` & `vision_models_playground-0.2.2/vision_models_playground/utility/load_models.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground/utility/visualize.py` & `vision_models_playground-0.2.2/vision_models_playground/utility/visualize.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.2.0/vision_models_playground.egg-info/PKG-INFO` & `vision_models_playground-0.2.2/vision_models_playground.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: vision-models-playground
-Version: 0.2.0
+Version: 0.2.2
 Summary: Akriel's vision models playground
 Home-page: https://github.com/Akrielz/vision_models_playground
 Author: Alexandru Stirbu
 Author-email: Stirbu.Alexandru.Net@outlook.com
 License: MIT
 Keywords: artificial intelligence,deep learning,transformer,attention mechanism,computer vision
 Classifier: Development Status :: 4 - Beta
```

### Comparing `vision_models_playground-0.2.0/vision_models_playground.egg-info/SOURCES.txt` & `vision_models_playground-0.2.2/vision_models_playground.egg-info/SOURCES.txt`

 * *Files identical despite different names*

