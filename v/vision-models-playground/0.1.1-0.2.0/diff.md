# Comparing `tmp/vision_models_playground-0.1.1.tar.gz` & `tmp/vision_models_playground-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "vision_models_playground-0.1.1.tar", last modified: Fri Sep 16 11:04:07 2022, max compression
+gzip compressed data, was "vision_models_playground-0.2.0.tar", last modified: Sun Jul 23 12:20:08 2023, max compression
```

## Comparing `vision_models_playground-0.1.1.tar` & `vision_models_playground-0.2.0.tar`

### file list

```diff
@@ -1,104 +1,144 @@
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2022-09-16 11:04:07.764044 vision_models_playground-0.1.1/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1963 2022-07-01 11:04:55.000000 vision_models_playground-0.1.1/.gitignore
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1073 2022-07-01 11:04:55.000000 vision_models_playground-0.1.1/LICENSE
--rw-rw-r--   0 akriel    (1000) akriel    (1000)    18165 2022-09-16 11:04:07.764044 vision_models_playground-0.1.1/PKG-INFO
--rw-rw-r--   0 akriel    (1000) akriel    (1000)    17468 2022-09-16 10:22:58.000000 vision_models_playground-0.1.1/README.md
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2022-09-16 11:04:07.756044 vision_models_playground-0.1.1/readme_assets/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)    22135 2022-07-01 11:04:55.000000 vision_models_playground-0.1.1/readme_assets/fake_images.png
--rw-rw-r--   0 akriel    (1000) akriel    (1000)    21071 2022-07-01 11:04:55.000000 vision_models_playground-0.1.1/readme_assets/real_images.png
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2022-09-16 11:04:07.756044 vision_models_playground-0.1.1/scripts/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     3556 2022-09-16 09:43:35.000000 vision_models_playground-0.1.1/scripts/create_imports_shortcuts.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)       21 2022-09-16 10:16:04.000000 vision_models_playground-0.1.1/scripts/setup_check.sh
--rw-rw-r--   0 akriel    (1000) akriel    (1000)       21 2022-09-16 10:15:23.000000 vision_models_playground-0.1.1/scripts/setup_create.sh
--rw-rw-r--   0 akriel    (1000) akriel    (1000)       55 2022-09-16 10:12:23.000000 vision_models_playground-0.1.1/scripts/twine_upload_real.sh
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      102 2022-09-16 10:10:04.000000 vision_models_playground-0.1.1/scripts/twine_upload_test.sh
--rw-rw-r--   0 akriel    (1000) akriel    (1000)       38 2022-09-16 11:04:07.764044 vision_models_playground-0.1.1/setup.cfg
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1435 2022-09-16 11:03:24.000000 vision_models_playground-0.1.1/setup.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2022-09-16 11:04:07.756044 vision_models_playground-0.1.1/vision_models_playground/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      173 2022-09-16 11:03:24.000000 vision_models_playground-0.1.1/vision_models_playground/__init__.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2022-09-16 11:04:07.756044 vision_models_playground-0.1.1/vision_models_playground/components/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      277 2022-09-16 09:51:11.000000 vision_models_playground-0.1.1/vision_models_playground/components/__init__.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2022-09-16 11:04:07.756044 vision_models_playground-0.1.1/vision_models_playground/components/activations/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      558 2022-09-16 09:43:35.000000 vision_models_playground-0.1.1/vision_models_playground/components/activations/__init__.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      181 2022-07-02 11:03:07.000000 vision_models_playground-0.1.1/vision_models_playground/components/activations/geglu.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      396 2022-07-07 08:31:57.000000 vision_models_playground-0.1.1/vision_models_playground/components/activations/hard_sigmoid.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      463 2022-07-07 08:23:37.000000 vision_models_playground-0.1.1/vision_models_playground/components/activations/mish.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      335 2022-09-16 09:09:13.000000 vision_models_playground-0.1.1/vision_models_playground/components/activations/quick_geglu.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      787 2022-07-05 10:21:04.000000 vision_models_playground-0.1.1/vision_models_playground/components/activations/quick_gelu.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      184 2022-07-02 11:03:07.000000 vision_models_playground-0.1.1/vision_models_playground/components/activations/relu_squared.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      420 2022-07-07 08:21:42.000000 vision_models_playground-0.1.1/vision_models_playground/components/activations/swish.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2022-09-16 11:04:07.760044 vision_models_playground-0.1.1/vision_models_playground/components/attention/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      967 2022-09-16 09:43:35.000000 vision_models_playground-0.1.1/vision_models_playground/components/attention/__init__.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1941 2022-09-16 09:09:13.000000 vision_models_playground-0.1.1/vision_models_playground/components/attention/attend.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     2544 2022-09-16 09:14:14.000000 vision_models_playground-0.1.1/vision_models_playground/components/attention/attention.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     2439 2022-09-16 09:09:13.000000 vision_models_playground-0.1.1/vision_models_playground/components/attention/compressor.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1117 2022-09-16 09:09:13.000000 vision_models_playground-0.1.1/vision_models_playground/components/attention/feed_forward.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      350 2022-08-11 13:42:49.000000 vision_models_playground-0.1.1/vision_models_playground/components/attention/post_norm.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      750 2022-09-16 09:14:14.000000 vision_models_playground-0.1.1/vision_models_playground/components/attention/pre_norm.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     5177 2022-09-16 09:09:13.000000 vision_models_playground-0.1.1/vision_models_playground/components/attention/transformer.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     5624 2022-09-16 09:14:14.000000 vision_models_playground-0.1.1/vision_models_playground/components/attention/transformer_decoder.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     2905 2022-09-16 09:09:13.000000 vision_models_playground-0.1.1/vision_models_playground/components/attention/transformer_decoder_layer.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     3728 2022-09-16 09:09:13.000000 vision_models_playground-0.1.1/vision_models_playground/components/attention/transformer_encoder.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     2053 2022-09-16 09:09:13.000000 vision_models_playground-0.1.1/vision_models_playground/components/attention/transformer_encoder_layer.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2022-09-16 11:04:07.760044 vision_models_playground-0.1.1/vision_models_playground/components/convolutions/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1205 2022-09-16 09:43:35.000000 vision_models_playground-0.1.1/vision_models_playground/components/convolutions/__init__.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1479 2022-09-16 09:09:13.000000 vision_models_playground-0.1.1/vision_models_playground/components/convolutions/bottleneck_block.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     2500 2022-09-16 09:56:23.000000 vision_models_playground-0.1.1/vision_models_playground/components/convolutions/conv_attend.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     2649 2022-09-16 09:09:13.000000 vision_models_playground-0.1.1/vision_models_playground/components/convolutions/conv_attention.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1047 2022-07-01 11:04:55.000000 vision_models_playground-0.1.1/vision_models_playground/components/convolutions/conv_block.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      959 2022-07-05 09:26:07.000000 vision_models_playground-0.1.1/vision_models_playground/components/convolutions/conv_embedding.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1878 2022-07-05 11:06:01.000000 vision_models_playground-0.1.1/vision_models_playground/components/convolutions/conv_projection.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     2575 2022-09-16 09:09:13.000000 vision_models_playground-0.1.1/vision_models_playground/components/convolutions/conv_transformer.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      868 2022-07-02 11:10:07.000000 vision_models_playground-0.1.1/vision_models_playground/components/convolutions/conv_transposed_block.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      817 2022-07-09 10:51:44.000000 vision_models_playground-0.1.1/vision_models_playground/components/convolutions/double_conv_block.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1048 2022-09-16 09:09:13.000000 vision_models_playground-0.1.1/vision_models_playground/components/convolutions/downscale_block.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1128 2022-09-16 09:09:13.000000 vision_models_playground-0.1.1/vision_models_playground/components/convolutions/residual_block.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1176 2022-09-16 09:09:13.000000 vision_models_playground-0.1.1/vision_models_playground/components/convolutions/upscale_block.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     2111 2022-09-16 09:09:13.000000 vision_models_playground-0.1.1/vision_models_playground/components/convolutions/upscale_concat_block.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2022-09-16 11:04:07.760044 vision_models_playground-0.1.1/vision_models_playground/components/dropout/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)       85 2022-09-16 09:43:35.000000 vision_models_playground-0.1.1/vision_models_playground/components/dropout/__init__.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1608 2022-07-05 16:32:45.000000 vision_models_playground-0.1.1/vision_models_playground/components/dropout/drop_path.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2022-09-16 11:04:07.760044 vision_models_playground-0.1.1/vision_models_playground/components/position_embedding/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      112 2022-09-16 09:43:35.000000 vision_models_playground-0.1.1/vision_models_playground/components/position_embedding/__init__.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     4111 2022-07-09 15:41:36.000000 vision_models_playground-0.1.1/vision_models_playground/components/position_embedding/fourier_embedding.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      146 2022-09-16 11:03:24.000000 vision_models_playground-0.1.1/vision_models_playground/metadata.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2022-09-16 11:04:07.760044 vision_models_playground-0.1.1/vision_models_playground/models/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      254 2022-09-16 09:51:11.000000 vision_models_playground-0.1.1/vision_models_playground/models/__init__.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2022-09-16 11:04:07.760044 vision_models_playground-0.1.1/vision_models_playground/models/augmenters/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)       86 2022-09-16 09:43:35.000000 vision_models_playground-0.1.1/vision_models_playground/models/augmenters/__init__.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1627 2022-09-16 09:14:14.000000 vision_models_playground-0.1.1/vision_models_playground/models/augmenters/augmenter.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2022-09-16 11:04:07.760044 vision_models_playground-0.1.1/vision_models_playground/models/autoencoders/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      105 2022-09-16 09:43:35.000000 vision_models_playground-0.1.1/vision_models_playground/models/autoencoders/__init__.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1988 2022-09-16 09:14:14.000000 vision_models_playground-0.1.1/vision_models_playground/models/autoencoders/ff_autoencoder.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2022-09-16 11:04:07.764044 vision_models_playground-0.1.1/vision_models_playground/models/classifiers/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1317 2022-09-16 09:43:35.000000 vision_models_playground-0.1.1/vision_models_playground/models/classifiers/__init__.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1958 2022-09-16 09:14:14.000000 vision_models_playground-0.1.1/vision_models_playground/models/classifiers/conv_classifier.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     7180 2022-09-16 09:57:15.000000 vision_models_playground-0.1.1/vision_models_playground/models/classifiers/conv_vision_transformer.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1578 2022-09-16 09:14:14.000000 vision_models_playground-0.1.1/vision_models_playground/models/classifiers/ff_classifier.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     5748 2022-09-16 09:57:54.000000 vision_models_playground-0.1.1/vision_models_playground/models/classifiers/perceiver.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     4393 2022-09-16 09:54:31.000000 vision_models_playground-0.1.1/vision_models_playground/models/classifiers/resnet.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     3545 2022-09-16 09:58:09.000000 vision_models_playground-0.1.1/vision_models_playground/models/classifiers/vision_perceiver.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     3047 2022-09-16 09:57:33.000000 vision_models_playground-0.1.1/vision_models_playground/models/classifiers/vision_transformer.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2022-09-16 11:04:07.764044 vision_models_playground-0.1.1/vision_models_playground/models/generative/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)       74 2022-09-16 09:09:13.000000 vision_models_playground-0.1.1/vision_models_playground/models/generative/__init__.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2022-09-16 11:04:07.764044 vision_models_playground-0.1.1/vision_models_playground/models/generative/adverserial/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)        0 2022-09-16 09:09:07.000000 vision_models_playground-0.1.1/vision_models_playground/models/generative/adverserial/__init__.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     7464 2022-09-16 09:29:46.000000 vision_models_playground-0.1.1/vision_models_playground/models/generative/adverserial/gan.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1377 2022-07-01 11:04:55.000000 vision_models_playground-0.1.1/vision_models_playground/models/generative/adverserial/mnist_discriminator.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1291 2022-07-01 11:04:55.000000 vision_models_playground-0.1.1/vision_models_playground/models/generative/adverserial/mnist_generator.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2022-09-16 11:04:07.764044 vision_models_playground-0.1.1/vision_models_playground/models/segmentation/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)       77 2022-09-16 09:43:35.000000 vision_models_playground-0.1.1/vision_models_playground/models/segmentation/__init__.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     3177 2022-09-16 09:58:28.000000 vision_models_playground-0.1.1/vision_models_playground/models/segmentation/unet.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2022-09-16 11:04:07.764044 vision_models_playground-0.1.1/vision_models_playground/utility/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      953 2022-09-16 09:43:35.000000 vision_models_playground-0.1.1/vision_models_playground/utility/__init__.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     1773 2022-07-11 09:50:42.000000 vision_models_playground-0.1.1/vision_models_playground/utility/datasets.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      320 2022-07-01 11:04:55.000000 vision_models_playground-0.1.1/vision_models_playground/utility/functions.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      398 2022-08-12 08:19:07.000000 vision_models_playground-0.1.1/vision_models_playground/utility/masks.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     4213 2022-07-11 09:48:27.000000 vision_models_playground-0.1.1/vision_models_playground/utility/train_models.py
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      789 2022-07-01 11:04:55.000000 vision_models_playground-0.1.1/vision_models_playground/utility/visualize.py
-drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2022-09-16 11:04:07.756044 vision_models_playground-0.1.1/vision_models_playground.egg-info/
--rw-rw-r--   0 akriel    (1000) akriel    (1000)    18165 2022-09-16 11:04:07.000000 vision_models_playground-0.1.1/vision_models_playground.egg-info/PKG-INFO
--rw-rw-r--   0 akriel    (1000) akriel    (1000)     4531 2022-09-16 11:04:07.000000 vision_models_playground-0.1.1/vision_models_playground.egg-info/SOURCES.txt
--rw-rw-r--   0 akriel    (1000) akriel    (1000)        1 2022-09-16 11:04:07.000000 vision_models_playground-0.1.1/vision_models_playground.egg-info/dependency_links.txt
--rw-rw-r--   0 akriel    (1000) akriel    (1000)      159 2022-09-16 11:04:07.000000 vision_models_playground-0.1.1/vision_models_playground.egg-info/requires.txt
--rw-rw-r--   0 akriel    (1000) akriel    (1000)       25 2022-09-16 11:04:07.000000 vision_models_playground-0.1.1/vision_models_playground.egg-info/top_level.txt
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.861549 vision_models_playground-0.2.0/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1073 2022-06-26 07:21:11.000000 vision_models_playground-0.2.0/LICENSE
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)    21375 2023-07-23 12:20:08.861549 vision_models_playground-0.2.0/PKG-INFO
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)    20698 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/README.md
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)       38 2023-07-23 12:20:08.861549 vision_models_playground-0.2.0/setup.cfg
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1435 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/setup.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.853549 vision_models_playground-0.2.0/vision_models_playground/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      546 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/__init__.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.853549 vision_models_playground-0.2.0/vision_models_playground/components/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      277 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/__init__.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.853549 vision_models_playground-0.2.0/vision_models_playground/components/activations/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      781 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/components/activations/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      181 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/activations/geglu.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      788 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/activations/gelu.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      396 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/activations/hard_sigmoid.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      463 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/activations/mish.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      335 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/activations/quick_geglu.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      787 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/activations/quick_gelu.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      184 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/activations/relu_squared.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      420 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/activations/swish.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.853549 vision_models_playground-0.2.0/vision_models_playground/components/attention/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1337 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/components/attention/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1941 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/attention/attend.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2544 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/attention/attention.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2439 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/attention/compressor.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1117 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/attention/feed_forward.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      350 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/attention/post_norm.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      750 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/attention/pre_norm.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1301 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/attention/tied_embedding.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     5177 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/attention/transformer.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     5624 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/attention/transformer_decoder.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2905 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/attention/transformer_decoder_layer.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     3728 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/attention/transformer_encoder.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2053 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/attention/transformer_encoder_layer.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.857549 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1622 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1479 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/bottleneck_block.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2500 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/conv_attend.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2649 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/conv_attention.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1047 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/conv_block.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      959 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/conv_embedding.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1878 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/conv_projection.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2575 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/conv_transformer.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      868 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/conv_transposed_block.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      817 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/double_conv_block.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1048 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/downscale_block.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1128 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/residual_block.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1176 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/upscale_block.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2111 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/upscale_concat_block.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2517 2023-07-06 17:51:36.000000 vision_models_playground-0.2.0/vision_models_playground/components/convolutions/yolo_v1_head.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.857549 vision_models_playground-0.2.0/vision_models_playground/components/dropout/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      131 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/components/dropout/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1608 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/dropout/drop_path.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.857549 vision_models_playground-0.2.0/vision_models_playground/components/position_embedding/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      166 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/components/position_embedding/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     4111 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/components/position_embedding/fourier_embedding.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.857549 vision_models_playground-0.2.0/vision_models_playground/data_structures/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      170 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/data_structures/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     7701 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/data_structures/yolo_bounding_box.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.857549 vision_models_playground-0.2.0/vision_models_playground/datasets/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1283 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/datasets/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     3935 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/datasets/datasets.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)    11513 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/datasets/yolo_pascal_voc_dataset.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     3570 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/datasets/yolo_pascal_voc_dataset_aug.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.857549 vision_models_playground-0.2.0/vision_models_playground/evaluate/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      342 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/evaluate/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     8111 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/evaluate/evaluate_models.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2344 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/evaluate/evaluate_yolo.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.857549 vision_models_playground-0.2.0/vision_models_playground/losses/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      126 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/losses/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     6136 2023-07-04 21:22:37.000000 vision_models_playground-0.2.0/vision_models_playground/losses/yolo_v1_loss.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      146 2023-07-23 12:20:05.000000 vision_models_playground-0.2.0/vision_models_playground/metadata.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.857549 vision_models_playground-0.2.0/vision_models_playground/metrics/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      724 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/metrics/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     4402 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/metrics/intersection_over_union.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1305 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/metrics/loss_tracker.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     4555 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/metrics/wrapper.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.857549 vision_models_playground-0.2.0/vision_models_playground/models/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      153 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/models/__init__.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.857549 vision_models_playground-0.2.0/vision_models_playground/models/classifiers/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1694 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/models/classifiers/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1954 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/models/classifiers/conv_classifier.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     7176 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/models/classifiers/conv_vision_transformer.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1574 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/models/classifiers/ff_classifier.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     5744 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/models/classifiers/perceiver.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     4389 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/models/classifiers/resnet.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     3541 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/models/classifiers/vision_perceiver.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     3043 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/models/classifiers/vision_transformer.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.857549 vision_models_playground-0.2.0/vision_models_playground/models/generative/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)       74 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/models/generative/__init__.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.857549 vision_models_playground-0.2.0/vision_models_playground/models/generative/adverserial/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      358 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/models/generative/adverserial/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     7464 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/models/generative/adverserial/gan.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1377 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/models/generative/adverserial/mnist_discriminator.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1291 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/models/generative/adverserial/mnist_generator.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.857549 vision_models_playground-0.2.0/vision_models_playground/models/segmentation/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      416 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/models/segmentation/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     3177 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/models/segmentation/unet.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     4981 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/models/segmentation/yolo_v1.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.857549 vision_models_playground-0.2.0/vision_models_playground/optimizers/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      110 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/optimizers/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2756 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/optimizers/lion.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.857549 vision_models_playground-0.2.0/vision_models_playground/pipelines/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      206 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/pipelines/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1919 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/pipelines/base.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     8578 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/pipelines/yolo.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.861549 vision_models_playground-0.2.0/vision_models_playground/train/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      421 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/train/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1491 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/train/train_classifier.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)    11481 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/train/train_models.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     3639 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/train/train_yolo.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.861549 vision_models_playground-0.2.0/vision_models_playground/transforms/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     4364 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     5221 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/auto.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      482 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/base.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      491 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/choose_one.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1001 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/clamp.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      915 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/compose.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2016 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/conversions.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1317 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/normalize.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2599 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/pad.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      495 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/probability_transform.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     6092 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/random_affine.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1109 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/random_horizontal_flip.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     3131 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/random_perspective.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2564 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/random_resized_crop.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     4163 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/random_rotation.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     1079 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/random_vertical_flip.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2585 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/resize.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      930 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/transforms/transform.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.861549 vision_models_playground-0.2.0/vision_models_playground/utility/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2264 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/utility/__init__.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2134 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/utility/config.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      566 2023-07-04 19:56:28.000000 vision_models_playground-0.2.0/vision_models_playground/utility/functions.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     4158 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/utility/hub.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     2156 2023-07-23 12:11:29.000000 vision_models_playground-0.2.0/vision_models_playground/utility/load_models.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      440 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/utility/masks.py
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      789 2023-07-04 19:56:10.000000 vision_models_playground-0.2.0/vision_models_playground/utility/visualize.py
+drwxrwxr-x   0 akriel    (1000) akriel    (1000)        0 2023-07-23 12:20:08.853549 vision_models_playground-0.2.0/vision_models_playground.egg-info/
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)    21375 2023-07-23 12:20:08.000000 vision_models_playground-0.2.0/vision_models_playground.egg-info/PKG-INFO
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)     6474 2023-07-23 12:20:08.000000 vision_models_playground-0.2.0/vision_models_playground.egg-info/SOURCES.txt
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)        1 2023-07-23 12:20:08.000000 vision_models_playground-0.2.0/vision_models_playground.egg-info/dependency_links.txt
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)      159 2023-07-23 12:20:08.000000 vision_models_playground-0.2.0/vision_models_playground.egg-info/requires.txt
+-rw-rw-r--   0 akriel    (1000) akriel    (1000)       25 2023-07-23 12:20:08.000000 vision_models_playground-0.2.0/vision_models_playground.egg-info/top_level.txt
```

### Comparing `vision_models_playground-0.1.1/LICENSE` & `vision_models_playground-0.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/PKG-INFO` & `vision_models_playground-0.2.0/README.md`

 * *Files 4% similar despite different names*

```diff
@@ -1,31 +1,16 @@
-Metadata-Version: 2.1
-Name: vision_models_playground
-Version: 0.1.1
-Summary: Akriel's vision models playground
-Home-page: https://github.com/Akrielz/vision_models_playground
-Author: Alexandru Stirbu
-Author-email: Stirbu.Alexandru.Net@outlook.com
-License: MIT
-Keywords: artificial intelligence,deep learning,transformer,attention mechanism,computer vision
-Platform: UNKNOWN
-Classifier: Development Status :: 4 - Beta
-Classifier: Intended Audience :: Developers
-Classifier: Topic :: Scientific/Engineering :: Artificial Intelligence
-Classifier: License :: OSI Approved :: MIT License
-Classifier: Programming Language :: Python :: 3.8
-Description-Content-Type: text/markdown
-License-File: LICENSE
-
 # Vision Models - Playground
 
 ## Table of Contents
 
 - [Description](#description)
 - [Install](#install)
+
+## Models
+- [YoloV1](#yolov1)
 - [ResNet](#resnet)
 - [Vision Transformer](#vision-transformer-vit)
 - [Generative Adversarial Networks](#generative-adversarial-networks-gan)
 - [Perceiver](#perceiver)
 - [Vision Perceiver](#vision-perceiver-vip)
 - [Convolutional Vision Transformer](#convolutional-vision-transformer-cvt)
 - [UNet](#unet)
@@ -40,14 +25,134 @@
 
 In order to install this package, run the following command:
 
 ```bash
 $ pip install vision-models-playground
 ```
 
+
+## YoloV1
+
+A detector based on the [YoloV1](https://arxiv.org/abs/1506.02640) architecture. Also known as Darknet.
+
+### Usage
+
+Models can be initialized with pre-build or custom versions.
+
+Code example to initialize and use prebuild YoloV1
+
+```python
+import torch
+from vision_models_playground.models.segmentation import build_yolo_v1
+
+model = build_yolo_v1(num_classes=20, in_channels=3, grid_size=7, num_bounding_boxes=2)
+
+img = torch.randn(1, 3, 448, 448)  # <batch_size, in_channels, height, width>
+preds = model(img)  # (1, 7, 7, 30) <batch_size, grid_size, grid_size, num_classes + 5 * num_bounding_boxes>
+```
+
+Or if you want to use the custom YoloV1
+
+```python
+import torch
+from vision_models_playground.models.segmentation import YoloV1
+
+dims = [[64], [192], [128, 256, 256, 512], [256, 512, 256, 512, 256, 512, 256, 512, 512, 1024], [512, 1024, 512, 1024]]
+kernel_size = [[7], [3], [1, 3, 1, 3], [1, 3, 1, 3, 1, 3, 1, 3, 1, 3], [1, 3, 1, 3]]
+stride = [[2], [1], [1, 1, 1, 1], [1, 1, 1, 1, 1, 1, 1, 1, 1, 1], [1, 1, 1, 1]]
+max_pools = [True, True, True, True, False]
+
+model = YoloV1(
+    dims=dims,
+    kernel_size=kernel_size,
+    stride=stride,
+    max_pools=max_pools,
+
+    in_channels=3,
+    num_classes=20,
+    num_bounding_boxes=2,
+    grid_size=7,
+
+    mlp_size=1024,
+)
+
+img = torch.randn(1, 3, 448, 448)  # <batch_size, in_channels, height, width>
+preds = model(img)  # (1, 7, 7, 30) <batch_size, grid_size, grid_size, num_classes + 5 * num_bounding_boxes>
+```
+
+### Parameters
+
+- `dims`: List[List[int]].  
+The number of channels in each layer.
+
+
+- `kernel_size`: List[List[int]].  
+The kernel size in each layer.
+
+
+- `stride`: List[List[int]].  
+The stride in each layer.
+
+
+- `max_pools`: List[bool].  
+If enabled, a max pool layer is applied after the convolutional layer.
+
+
+- `in_channels`: int.  
+The number of channels in the input image.
+
+
+- `num_classes`: int.  
+The number of classes to classify.
+
+
+- `num_bounding_boxes`: int.  
+The number of bounding boxes to predict per grid cell.
+
+
+- `grid_size`: int.  
+The size of the grid that the image is split into.
+
+
+- `mlp_size`: int.  
+The size of the MLP layer that is applied after the convolutional layers.
+
+
+### PreTrained Weights
+
+If you want to use the pretrained weights, you use the following code:
+
+```py
+import torch
+from vision_models_playground.utility.hub import load_vmp_model_from_hub
+
+
+model = load_vmp_model_from_hub("Akriel/ResNetYoloV1")
+
+img = torch.randn(1, 3, 448, 448)  # <batch_size, in_channels, height, width>
+preds = model(img)  # (1, 7, 7, 30) <batch_size, grid_size, grid_size, num_classes + 5 * num_bounding_boxes>
+```
+
+If you want to use the pretrained model within a pipeline on raw images, you can use the following code:
+
+```py
+from PIL import Image
+
+from vision_models_playground.utility.hub import load_vmp_pipeline_from_hub
+
+pipeline = load_vmp_pipeline_from_hub("Akriel/ResNetYoloV1")
+
+# Load image
+x = Image.open("path/to/image.jpg")
+y = pipeline(x)  # A dictionary containing the predictions
+```
+
+For more information about the pretrain models, check the [hub](https://huggingface.co/Akriel/ResNetYoloV1) page.  
+Or check the demo results from `explore_models/yolo_trained_model.ipynb`
+
 ## ResNet
 
 A classifier based on the [ResNet](https://arxiv.org/abs/1512.03385) architecture.
 
 ### Usage
 
 Models can be initialized with pre-build or custom versions.
@@ -765,9 +870,7 @@
 Else, uses a `nn.functional.upsample` function with the corresponding method.
 
 
 - `crop`: bool.  
 If enabled, the output each upscale layer will be cropped to the native size
 of the UpScaled image.
 
-
-
```

### Comparing `vision_models_playground-0.1.1/README.md` & `vision_models_playground-0.2.0/vision_models_playground.egg-info/PKG-INFO`

 * *Files 22% similar despite different names*

```diff
@@ -1,13 +1,33 @@
+Metadata-Version: 2.1
+Name: vision-models-playground
+Version: 0.2.0
+Summary: Akriel's vision models playground
+Home-page: https://github.com/Akrielz/vision_models_playground
+Author: Alexandru Stirbu
+Author-email: Stirbu.Alexandru.Net@outlook.com
+License: MIT
+Keywords: artificial intelligence,deep learning,transformer,attention mechanism,computer vision
+Classifier: Development Status :: 4 - Beta
+Classifier: Intended Audience :: Developers
+Classifier: Topic :: Scientific/Engineering :: Artificial Intelligence
+Classifier: License :: OSI Approved :: MIT License
+Classifier: Programming Language :: Python :: 3.8
+Description-Content-Type: text/markdown
+License-File: LICENSE
+
 # Vision Models - Playground
 
 ## Table of Contents
 
 - [Description](#description)
 - [Install](#install)
+
+## Models
+- [YoloV1](#yolov1)
 - [ResNet](#resnet)
 - [Vision Transformer](#vision-transformer-vit)
 - [Generative Adversarial Networks](#generative-adversarial-networks-gan)
 - [Perceiver](#perceiver)
 - [Vision Perceiver](#vision-perceiver-vip)
 - [Convolutional Vision Transformer](#convolutional-vision-transformer-cvt)
 - [UNet](#unet)
@@ -22,14 +42,134 @@
 
 In order to install this package, run the following command:
 
 ```bash
 $ pip install vision-models-playground
 ```
 
+
+## YoloV1
+
+A detector based on the [YoloV1](https://arxiv.org/abs/1506.02640) architecture. Also known as Darknet.
+
+### Usage
+
+Models can be initialized with pre-build or custom versions.
+
+Code example to initialize and use prebuild YoloV1
+
+```python
+import torch
+from vision_models_playground.models.segmentation import build_yolo_v1
+
+model = build_yolo_v1(num_classes=20, in_channels=3, grid_size=7, num_bounding_boxes=2)
+
+img = torch.randn(1, 3, 448, 448)  # <batch_size, in_channels, height, width>
+preds = model(img)  # (1, 7, 7, 30) <batch_size, grid_size, grid_size, num_classes + 5 * num_bounding_boxes>
+```
+
+Or if you want to use the custom YoloV1
+
+```python
+import torch
+from vision_models_playground.models.segmentation import YoloV1
+
+dims = [[64], [192], [128, 256, 256, 512], [256, 512, 256, 512, 256, 512, 256, 512, 512, 1024], [512, 1024, 512, 1024]]
+kernel_size = [[7], [3], [1, 3, 1, 3], [1, 3, 1, 3, 1, 3, 1, 3, 1, 3], [1, 3, 1, 3]]
+stride = [[2], [1], [1, 1, 1, 1], [1, 1, 1, 1, 1, 1, 1, 1, 1, 1], [1, 1, 1, 1]]
+max_pools = [True, True, True, True, False]
+
+model = YoloV1(
+    dims=dims,
+    kernel_size=kernel_size,
+    stride=stride,
+    max_pools=max_pools,
+
+    in_channels=3,
+    num_classes=20,
+    num_bounding_boxes=2,
+    grid_size=7,
+
+    mlp_size=1024,
+)
+
+img = torch.randn(1, 3, 448, 448)  # <batch_size, in_channels, height, width>
+preds = model(img)  # (1, 7, 7, 30) <batch_size, grid_size, grid_size, num_classes + 5 * num_bounding_boxes>
+```
+
+### Parameters
+
+- `dims`: List[List[int]].  
+The number of channels in each layer.
+
+
+- `kernel_size`: List[List[int]].  
+The kernel size in each layer.
+
+
+- `stride`: List[List[int]].  
+The stride in each layer.
+
+
+- `max_pools`: List[bool].  
+If enabled, a max pool layer is applied after the convolutional layer.
+
+
+- `in_channels`: int.  
+The number of channels in the input image.
+
+
+- `num_classes`: int.  
+The number of classes to classify.
+
+
+- `num_bounding_boxes`: int.  
+The number of bounding boxes to predict per grid cell.
+
+
+- `grid_size`: int.  
+The size of the grid that the image is split into.
+
+
+- `mlp_size`: int.  
+The size of the MLP layer that is applied after the convolutional layers.
+
+
+### PreTrained Weights
+
+If you want to use the pretrained weights, you use the following code:
+
+```py
+import torch
+from vision_models_playground.utility.hub import load_vmp_model_from_hub
+
+
+model = load_vmp_model_from_hub("Akriel/ResNetYoloV1")
+
+img = torch.randn(1, 3, 448, 448)  # <batch_size, in_channels, height, width>
+preds = model(img)  # (1, 7, 7, 30) <batch_size, grid_size, grid_size, num_classes + 5 * num_bounding_boxes>
+```
+
+If you want to use the pretrained model within a pipeline on raw images, you can use the following code:
+
+```py
+from PIL import Image
+
+from vision_models_playground.utility.hub import load_vmp_pipeline_from_hub
+
+pipeline = load_vmp_pipeline_from_hub("Akriel/ResNetYoloV1")
+
+# Load image
+x = Image.open("path/to/image.jpg")
+y = pipeline(x)  # A dictionary containing the predictions
+```
+
+For more information about the pretrain models, check the [hub](https://huggingface.co/Akriel/ResNetYoloV1) page.  
+Or check the demo results from `explore_models/yolo_trained_model.ipynb`
+
 ## ResNet
 
 A classifier based on the [ResNet](https://arxiv.org/abs/1512.03385) architecture.
 
 ### Usage
 
 Models can be initialized with pre-build or custom versions.
```

### Comparing `vision_models_playground-0.1.1/setup.py` & `vision_models_playground-0.2.0/setup.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground/components/activations/__init__.py` & `vision_models_playground-0.2.0/vision_models_playground/__init__.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,8 +1,14 @@
-# Classes
-from vision_models_playground.components.activations.relu_squared import ReluSquared
-from vision_models_playground.components.activations.swish import Swish
-from vision_models_playground.components.activations.geglu import GEGLU
-from vision_models_playground.components.activations.mish import Mish
-from vision_models_playground.components.activations.hard_sigmoid import HardSigmoid
-from vision_models_playground.components.activations.quick_gelu import QuickGELU
-from vision_models_playground.components.activations.quick_geglu import QuickGEGLU
+from vision_models_playground.metadata import *
+
+import vision_models_playground.components
+import vision_models_playground.data_structures
+import vision_models_playground.datasets
+import vision_models_playground.evaluate
+import vision_models_playground.losses
+import vision_models_playground.metrics
+import vision_models_playground.models
+import vision_models_playground.optimizers
+import vision_models_playground.pipelines
+import vision_models_playground.train
+import vision_models_playground.transforms
+import vision_models_playground.utility
```

### Comparing `vision_models_playground-0.1.1/vision_models_playground/components/activations/quick_gelu.py` & `vision_models_playground-0.2.0/vision_models_playground/components/activations/quick_gelu.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground/components/attention/__init__.py` & `vision_models_playground-0.2.0/vision_models_playground/components/attention/__init__.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,12 +1,29 @@
 # Classes
 from vision_models_playground.components.attention.transformer_encoder_layer import TransformerEncoderLayer
 from vision_models_playground.components.attention.attention import Attention
 from vision_models_playground.components.attention.transformer_decoder_layer import TransformerDecoderLayer
+from vision_models_playground.components.attention.tied_embedding import TiedEmbedding
 from vision_models_playground.components.attention.pre_norm import PreNorm
 from vision_models_playground.components.attention.post_norm import PostNorm
 from vision_models_playground.components.attention.attend import Attend
 from vision_models_playground.components.attention.feed_forward import FeedForward
 from vision_models_playground.components.attention.transformer_decoder import TransformerDecoder
 from vision_models_playground.components.attention.compressor import Compressor
 from vision_models_playground.components.attention.transformer import Transformer
 from vision_models_playground.components.attention.transformer_encoder import TransformerEncoder
+
+# All imports 
+__all__ = [
+    'TransformerEncoderLayer',
+    'Attention',
+    'TransformerDecoderLayer',
+    'TiedEmbedding',
+    'PreNorm',
+    'PostNorm',
+    'Attend',
+    'FeedForward',
+    'TransformerDecoder',
+    'Compressor',
+    'Transformer',
+    'TransformerEncoder',
+]
```

### Comparing `vision_models_playground-0.1.1/vision_models_playground/components/attention/attend.py` & `vision_models_playground-0.2.0/vision_models_playground/components/attention/attend.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground/components/attention/attention.py` & `vision_models_playground-0.2.0/vision_models_playground/components/attention/attention.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground/components/attention/compressor.py` & `vision_models_playground-0.2.0/vision_models_playground/components/attention/compressor.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground/components/attention/feed_forward.py` & `vision_models_playground-0.2.0/vision_models_playground/components/attention/feed_forward.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground/components/attention/pre_norm.py` & `vision_models_playground-0.2.0/vision_models_playground/components/attention/pre_norm.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground/components/attention/transformer.py` & `vision_models_playground-0.2.0/vision_models_playground/components/attention/transformer.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground/components/attention/transformer_decoder.py` & `vision_models_playground-0.2.0/vision_models_playground/components/attention/transformer_decoder.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground/components/attention/transformer_decoder_layer.py` & `vision_models_playground-0.2.0/vision_models_playground/components/attention/transformer_decoder_layer.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground/components/attention/transformer_encoder.py` & `vision_models_playground-0.2.0/vision_models_playground/components/attention/transformer_encoder.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground/components/attention/transformer_encoder_layer.py` & `vision_models_playground-0.2.0/vision_models_playground/components/attention/transformer_encoder_layer.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground/components/convolutions/__init__.py` & `vision_models_playground-0.2.0/vision_models_playground/components/convolutions/__init__.py`

 * *Files 12% similar despite different names*

```diff
@@ -6,9 +6,28 @@
 from vision_models_playground.components.convolutions.upscale_block import UpscaleBlock
 from vision_models_playground.components.convolutions.double_conv_block import DoubleConvBlock
 from vision_models_playground.components.convolutions.conv_attend import ConvAttend
 from vision_models_playground.components.convolutions.conv_attention import ConvAttention
 from vision_models_playground.components.convolutions.conv_transposed_block import ConvTransposedBlock
 from vision_models_playground.components.convolutions.upscale_concat_block import UpscaleConcatBlock
 from vision_models_playground.components.convolutions.conv_transformer import ConvTransformer
+from vision_models_playground.components.convolutions.yolo_v1_head import YoloV1Head
 from vision_models_playground.components.convolutions.conv_projection import ConvProjection
 from vision_models_playground.components.convolutions.bottleneck_block import BottleneckBlock
+
+# All imports 
+__all__ = [
+    'DownscaleBlock',
+    'ConvEmbedding',
+    'ConvBlock',
+    'ResidualBlock',
+    'UpscaleBlock',
+    'DoubleConvBlock',
+    'ConvAttend',
+    'ConvAttention',
+    'ConvTransposedBlock',
+    'UpscaleConcatBlock',
+    'ConvTransformer',
+    'YoloV1Head',
+    'ConvProjection',
+    'BottleneckBlock',
+]
```

### Comparing `vision_models_playground-0.1.1/vision_models_playground/components/convolutions/bottleneck_block.py` & `vision_models_playground-0.2.0/vision_models_playground/components/convolutions/bottleneck_block.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground/components/convolutions/conv_attend.py` & `vision_models_playground-0.2.0/vision_models_playground/components/convolutions/conv_attend.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground/components/convolutions/conv_attention.py` & `vision_models_playground-0.2.0/vision_models_playground/components/convolutions/conv_attention.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground/components/convolutions/conv_block.py` & `vision_models_playground-0.2.0/vision_models_playground/components/convolutions/conv_block.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground/components/convolutions/conv_embedding.py` & `vision_models_playground-0.2.0/vision_models_playground/components/convolutions/conv_embedding.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground/components/convolutions/conv_projection.py` & `vision_models_playground-0.2.0/vision_models_playground/components/convolutions/conv_projection.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground/components/convolutions/conv_transformer.py` & `vision_models_playground-0.2.0/vision_models_playground/components/convolutions/conv_transformer.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground/components/convolutions/conv_transposed_block.py` & `vision_models_playground-0.2.0/vision_models_playground/components/convolutions/conv_transposed_block.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground/components/convolutions/double_conv_block.py` & `vision_models_playground-0.2.0/vision_models_playground/components/convolutions/double_conv_block.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground/components/convolutions/downscale_block.py` & `vision_models_playground-0.2.0/vision_models_playground/components/convolutions/downscale_block.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground/components/convolutions/residual_block.py` & `vision_models_playground-0.2.0/vision_models_playground/components/convolutions/residual_block.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground/components/convolutions/upscale_block.py` & `vision_models_playground-0.2.0/vision_models_playground/components/convolutions/upscale_block.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground/components/convolutions/upscale_concat_block.py` & `vision_models_playground-0.2.0/vision_models_playground/components/convolutions/upscale_concat_block.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground/components/dropout/drop_path.py` & `vision_models_playground-0.2.0/vision_models_playground/components/dropout/drop_path.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground/components/position_embedding/fourier_embedding.py` & `vision_models_playground-0.2.0/vision_models_playground/components/position_embedding/fourier_embedding.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground/models/classifiers/conv_classifier.py` & `vision_models_playground-0.2.0/vision_models_playground/models/classifiers/conv_classifier.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 import torch
 from einops import rearrange
 from torch import nn
 from torch.nn import functional as F
 
-from vision_models_playground.utility.datasets import get_cifar10_dataset
-from vision_models_playground.utility.train_models import train_model_classifier
+from vision_models_playground.datasets.datasets import get_cifar10_dataset
+from vision_models_playground.train.train_classifier import train_model_classifier
 
 
 class ConvolutionalClassifier(nn.Module):
     def __init__(
             self,
             num_classes: int = 10,
             channels: int = 1
@@ -57,14 +57,14 @@
 
     def predict_prob(self, x):
         with torch.no_grad():
             return self.forward(x)
 
 
 def main():
-    model = ConvolutionalClassifier(channels=3).cuda()
+    model = ConvolutionalClassifier(channels=3)
     train_dataset, test_dataset = get_cifar10_dataset()
     train_model_classifier(model, train_dataset, test_dataset, num_epochs=100)
 
 
 if __name__ == '__main__':
     main()
```

### Comparing `vision_models_playground-0.1.1/vision_models_playground/models/classifiers/conv_vision_transformer.py` & `vision_models_playground-0.2.0/vision_models_playground/models/classifiers/conv_vision_transformer.py`

 * *Files 2% similar despite different names*

```diff
@@ -2,17 +2,17 @@
 
 import torch
 from einops.layers.torch import Reduce, Rearrange
 from torch import nn
 
 from vision_models_playground.components.activations import QuickGELU
 from vision_models_playground.components.convolutions.conv_transformer import ConvTransformer
-from vision_models_playground.utility.datasets import get_cifar10_dataset
+from vision_models_playground.datasets.datasets import get_cifar10_dataset
+from vision_models_playground.train.train_classifier import train_model_classifier
 from vision_models_playground.utility.functions import get_number_of_parameters
-from vision_models_playground.utility.train_models import train_model_classifier
 
 
 class ConvVisionTransformer(nn.Module):
     def __init__(
             self,
             in_channels: int = 3,
             num_classes: int = 1000,
@@ -191,14 +191,14 @@
         drop_path_rate=[0.0, 0.1],
         kernel_size=[3, 3],
         stride_kv=[2, 2],
         stride_q=[1, 1],
         padding_kv=[1, 1],
         padding_q=[1, 1],
         method=['conv', 'conv'],
-    ).cuda()
+    )
 
     # print number of params of the model
     print(f"Number of params: {get_number_of_parameters(model) / (1024 ** 2):.3f} M")
 
     dataset_train, dataset_test = get_cifar10_dataset()
     train_model_classifier(model, dataset_train, dataset_test)
```

### Comparing `vision_models_playground-0.1.1/vision_models_playground/models/classifiers/ff_classifier.py` & `vision_models_playground-0.2.0/vision_models_playground/models/classifiers/ff_classifier.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from typing import List
 
 import torch
 from einops import rearrange
 from torch import nn
 
-from vision_models_playground.utility.datasets import get_cifar10_dataset
-from vision_models_playground.utility.train_models import train_model_classifier
+from vision_models_playground.datasets.datasets import get_cifar10_dataset
+from vision_models_playground.train.train_classifier import train_model_classifier
 
 
 class FeedForwardClassifier(nn.Module):
     def __init__(
             self,
             input_dim: int = 28 * 28,
             hidden_dims: List[int] = None,
@@ -46,14 +46,14 @@
 
 
 def main():
     model = FeedForwardClassifier(
         input_dim=32 * 32 * 3,
         hidden_dims=[256, 128],
         num_classes=10,
-    ).cuda()
+    )
     train_dataset, test_dataset = get_cifar10_dataset()
     train_model_classifier(model, train_dataset, test_dataset, num_epochs=100)
 
 
 if __name__ == '__main__':
     main()
```

### Comparing `vision_models_playground-0.1.1/vision_models_playground/models/classifiers/perceiver.py` & `vision_models_playground-0.2.0/vision_models_playground/models/classifiers/perceiver.py`

 * *Files 2% similar despite different names*

```diff
@@ -5,16 +5,16 @@
 from einops.layers.torch import Reduce, Rearrange
 from torch import nn
 
 from vision_models_playground.components.activations.geglu import GEGLU
 from vision_models_playground.components.attention import TransformerEncoder, FeedForward
 from vision_models_playground.components.attention.attend import Attend
 from vision_models_playground.components.position_embedding import FourierEmbedding
-from vision_models_playground.utility.datasets import get_cifar10_dataset
-from vision_models_playground.utility.train_models import train_model_classifier
+from vision_models_playground.datasets.datasets import get_cifar10_dataset
+from vision_models_playground.train.train_classifier import train_model_classifier
 
 
 class Perceiver(nn.Module):
     def __init__(
             self,
             input_dim: int,
             input_axis: int,
@@ -168,15 +168,15 @@
         self_attend_heads=4,
         self_attend_dim=32,
         transformer_depth=2,
         attention_dropout=0.,
         ff_hidden_dim=64,
         ff_dropout=0.,
         activation=None,
-    ).cuda()
+    )
 
     model = nn.Sequential(
         Rearrange("b c h w -> b h w c"),
         model,
     )
 
     dataset_train, dataset_test = get_cifar10_dataset()
```

### Comparing `vision_models_playground-0.1.1/vision_models_playground/models/classifiers/resnet.py` & `vision_models_playground-0.2.0/vision_models_playground/models/classifiers/resnet.py`

 * *Files 2% similar despite different names*

```diff
@@ -2,16 +2,16 @@
 
 from einops import rearrange
 from torch import nn
 
 from vision_models_playground.components.convolutions.conv_block import ConvBlock
 from vision_models_playground.components.convolutions.residual_block import ResidualBlock
 from vision_models_playground.components.convolutions.bottleneck_block import BottleneckBlock
-from vision_models_playground.utility.datasets import get_cifar10_dataset
-from vision_models_playground.utility.train_models import train_model_classifier
+from vision_models_playground.datasets.datasets import get_cifar10_dataset
+from vision_models_playground.train.train_classifier import train_model_classifier
 
 
 class ResNet(nn.Module):
     def __init__(
             self,
             in_channels: int = 3,
             num_classes: int = 10,
@@ -134,15 +134,15 @@
         num_layers=[3, 8, 36, 3],
         num_channels=[64, 256, 512, 1024],
         block=BottleneckBlock
     )
 
 
 def main():
-    model = build_resnet_50().cuda()
+    model = build_resnet_50()
 
     dataset_train, dataset_test = get_cifar10_dataset()
     train_model_classifier(model, dataset_train, dataset_test)
 
 
 if __name__ == "__main__":
     main()
```

### Comparing `vision_models_playground-0.1.1/vision_models_playground/models/classifiers/vision_perceiver.py` & `vision_models_playground-0.2.0/vision_models_playground/models/classifiers/vision_perceiver.py`

 * *Files 2% similar despite different names*

```diff
@@ -2,16 +2,16 @@
 
 from torch import nn
 
 from einops import rearrange
 
 from vision_models_playground.components.position_embedding import FourierEmbedding
 from vision_models_playground.models.classifiers.perceiver import Perceiver
-from vision_models_playground.utility.datasets import get_cifar10_dataset
-from vision_models_playground.utility.train_models import train_model_classifier
+from vision_models_playground.datasets.datasets import get_cifar10_dataset
+from vision_models_playground.train.train_classifier import train_model_classifier
 
 
 class VisionPerceiver(nn.Module):
     def __init__(
             self,
             *,
             patch_size: int,
@@ -103,15 +103,15 @@
         self_attend_heads=8,
         self_attend_dim=64,
         transformer_depth=2,
         attention_dropout=0.0,
         ff_hidden_dim=512,
         ff_dropout=0.0,
         activation=None,
-    ).cuda()
+    )
 
     train_dataset, test_dataset = get_cifar10_dataset()
     train_model_classifier(model, train_dataset, test_dataset, batch_size=128)
 
 
 if __name__ == "__main__":
     main()
```

### Comparing `vision_models_playground-0.1.1/vision_models_playground/models/classifiers/vision_transformer.py` & `vision_models_playground-0.2.0/vision_models_playground/models/classifiers/vision_transformer.py`

 * *Files 5% similar despite different names*

```diff
@@ -3,16 +3,16 @@
 import torch
 from torch import nn
 
 from einops import repeat
 from einops.layers.torch import Rearrange
 
 from vision_models_playground.components.attention import TransformerEncoder
-from vision_models_playground.utility.datasets import get_cifar10_dataset
-from vision_models_playground.utility.train_models import train_model_classifier
+from vision_models_playground.datasets.datasets import get_cifar10_dataset
+from vision_models_playground.train.train_classifier import train_model_classifier
 
 
 class VisionTransformer(nn.Module):
     def __init__(
             self,
             *,
             image_size: int,
@@ -90,14 +90,14 @@
         depth=6,
         heads=8,
         mlp_dim=512,
         dropout=0.2,
         emb_dropout=0.2,
         apply_rotary_emb=True,
         pool="cls",
-    ).cuda()
+    )
     train_dataset, test_dataset = get_cifar10_dataset()
     train_model_classifier(model, train_dataset, test_dataset, num_epochs=100)
 
 
 if __name__ == '__main__':
     main()
```

### Comparing `vision_models_playground-0.1.1/vision_models_playground/models/generative/adverserial/gan.py` & `vision_models_playground-0.2.0/vision_models_playground/models/generative/adverserial/gan.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground/models/generative/adverserial/mnist_discriminator.py` & `vision_models_playground-0.2.0/vision_models_playground/models/generative/adverserial/mnist_discriminator.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground/models/generative/adverserial/mnist_generator.py` & `vision_models_playground-0.2.0/vision_models_playground/models/generative/adverserial/mnist_generator.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground/models/segmentation/unet.py` & `vision_models_playground-0.2.0/vision_models_playground/models/segmentation/unet.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground/utility/visualize.py` & `vision_models_playground-0.2.0/vision_models_playground/utility/visualize.py`

 * *Files identical despite different names*

### Comparing `vision_models_playground-0.1.1/vision_models_playground.egg-info/PKG-INFO` & `vision_models_playground-0.2.0/PKG-INFO`

 * *Files 12% similar despite different names*

```diff
@@ -1,31 +1,33 @@
 Metadata-Version: 2.1
-Name: vision-models-playground
-Version: 0.1.1
+Name: vision_models_playground
+Version: 0.2.0
 Summary: Akriel's vision models playground
 Home-page: https://github.com/Akrielz/vision_models_playground
 Author: Alexandru Stirbu
 Author-email: Stirbu.Alexandru.Net@outlook.com
 License: MIT
 Keywords: artificial intelligence,deep learning,transformer,attention mechanism,computer vision
-Platform: UNKNOWN
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers
 Classifier: Topic :: Scientific/Engineering :: Artificial Intelligence
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3.8
 Description-Content-Type: text/markdown
 License-File: LICENSE
 
 # Vision Models - Playground
 
 ## Table of Contents
 
 - [Description](#description)
 - [Install](#install)
+
+## Models
+- [YoloV1](#yolov1)
 - [ResNet](#resnet)
 - [Vision Transformer](#vision-transformer-vit)
 - [Generative Adversarial Networks](#generative-adversarial-networks-gan)
 - [Perceiver](#perceiver)
 - [Vision Perceiver](#vision-perceiver-vip)
 - [Convolutional Vision Transformer](#convolutional-vision-transformer-cvt)
 - [UNet](#unet)
@@ -40,14 +42,134 @@
 
 In order to install this package, run the following command:
 
 ```bash
 $ pip install vision-models-playground
 ```
 
+
+## YoloV1
+
+A detector based on the [YoloV1](https://arxiv.org/abs/1506.02640) architecture. Also known as Darknet.
+
+### Usage
+
+Models can be initialized with pre-build or custom versions.
+
+Code example to initialize and use prebuild YoloV1
+
+```python
+import torch
+from vision_models_playground.models.segmentation import build_yolo_v1
+
+model = build_yolo_v1(num_classes=20, in_channels=3, grid_size=7, num_bounding_boxes=2)
+
+img = torch.randn(1, 3, 448, 448)  # <batch_size, in_channels, height, width>
+preds = model(img)  # (1, 7, 7, 30) <batch_size, grid_size, grid_size, num_classes + 5 * num_bounding_boxes>
+```
+
+Or if you want to use the custom YoloV1
+
+```python
+import torch
+from vision_models_playground.models.segmentation import YoloV1
+
+dims = [[64], [192], [128, 256, 256, 512], [256, 512, 256, 512, 256, 512, 256, 512, 512, 1024], [512, 1024, 512, 1024]]
+kernel_size = [[7], [3], [1, 3, 1, 3], [1, 3, 1, 3, 1, 3, 1, 3, 1, 3], [1, 3, 1, 3]]
+stride = [[2], [1], [1, 1, 1, 1], [1, 1, 1, 1, 1, 1, 1, 1, 1, 1], [1, 1, 1, 1]]
+max_pools = [True, True, True, True, False]
+
+model = YoloV1(
+    dims=dims,
+    kernel_size=kernel_size,
+    stride=stride,
+    max_pools=max_pools,
+
+    in_channels=3,
+    num_classes=20,
+    num_bounding_boxes=2,
+    grid_size=7,
+
+    mlp_size=1024,
+)
+
+img = torch.randn(1, 3, 448, 448)  # <batch_size, in_channels, height, width>
+preds = model(img)  # (1, 7, 7, 30) <batch_size, grid_size, grid_size, num_classes + 5 * num_bounding_boxes>
+```
+
+### Parameters
+
+- `dims`: List[List[int]].  
+The number of channels in each layer.
+
+
+- `kernel_size`: List[List[int]].  
+The kernel size in each layer.
+
+
+- `stride`: List[List[int]].  
+The stride in each layer.
+
+
+- `max_pools`: List[bool].  
+If enabled, a max pool layer is applied after the convolutional layer.
+
+
+- `in_channels`: int.  
+The number of channels in the input image.
+
+
+- `num_classes`: int.  
+The number of classes to classify.
+
+
+- `num_bounding_boxes`: int.  
+The number of bounding boxes to predict per grid cell.
+
+
+- `grid_size`: int.  
+The size of the grid that the image is split into.
+
+
+- `mlp_size`: int.  
+The size of the MLP layer that is applied after the convolutional layers.
+
+
+### PreTrained Weights
+
+If you want to use the pretrained weights, you use the following code:
+
+```py
+import torch
+from vision_models_playground.utility.hub import load_vmp_model_from_hub
+
+
+model = load_vmp_model_from_hub("Akriel/ResNetYoloV1")
+
+img = torch.randn(1, 3, 448, 448)  # <batch_size, in_channels, height, width>
+preds = model(img)  # (1, 7, 7, 30) <batch_size, grid_size, grid_size, num_classes + 5 * num_bounding_boxes>
+```
+
+If you want to use the pretrained model within a pipeline on raw images, you can use the following code:
+
+```py
+from PIL import Image
+
+from vision_models_playground.utility.hub import load_vmp_pipeline_from_hub
+
+pipeline = load_vmp_pipeline_from_hub("Akriel/ResNetYoloV1")
+
+# Load image
+x = Image.open("path/to/image.jpg")
+y = pipeline(x)  # A dictionary containing the predictions
+```
+
+For more information about the pretrain models, check the [hub](https://huggingface.co/Akriel/ResNetYoloV1) page.  
+Or check the demo results from `explore_models/yolo_trained_model.ipynb`
+
 ## ResNet
 
 A classifier based on the [ResNet](https://arxiv.org/abs/1512.03385) architecture.
 
 ### Usage
 
 Models can be initialized with pre-build or custom versions.
@@ -765,9 +887,7 @@
 Else, uses a `nn.functional.upsample` function with the corresponding method.
 
 
 - `crop`: bool.  
 If enabled, the output each upscale layer will be cropped to the native size
 of the UpScaled image.
 
-
-
```

### Comparing `vision_models_playground-0.1.1/vision_models_playground.egg-info/SOURCES.txt` & `vision_models_playground-0.2.0/vision_models_playground.egg-info/SOURCES.txt`

 * *Files 25% similar despite different names*

```diff
@@ -1,41 +1,35 @@
-.gitignore
 LICENSE
 README.md
 setup.py
-readme_assets/fake_images.png
-readme_assets/real_images.png
-scripts/create_imports_shortcuts.py
-scripts/setup_check.sh
-scripts/setup_create.sh
-scripts/twine_upload_real.sh
-scripts/twine_upload_test.sh
 vision_models_playground/__init__.py
 vision_models_playground/metadata.py
 vision_models_playground.egg-info/PKG-INFO
 vision_models_playground.egg-info/SOURCES.txt
 vision_models_playground.egg-info/dependency_links.txt
 vision_models_playground.egg-info/requires.txt
 vision_models_playground.egg-info/top_level.txt
 vision_models_playground/components/__init__.py
 vision_models_playground/components/activations/__init__.py
 vision_models_playground/components/activations/geglu.py
+vision_models_playground/components/activations/gelu.py
 vision_models_playground/components/activations/hard_sigmoid.py
 vision_models_playground/components/activations/mish.py
 vision_models_playground/components/activations/quick_geglu.py
 vision_models_playground/components/activations/quick_gelu.py
 vision_models_playground/components/activations/relu_squared.py
 vision_models_playground/components/activations/swish.py
 vision_models_playground/components/attention/__init__.py
 vision_models_playground/components/attention/attend.py
 vision_models_playground/components/attention/attention.py
 vision_models_playground/components/attention/compressor.py
 vision_models_playground/components/attention/feed_forward.py
 vision_models_playground/components/attention/post_norm.py
 vision_models_playground/components/attention/pre_norm.py
+vision_models_playground/components/attention/tied_embedding.py
 vision_models_playground/components/attention/transformer.py
 vision_models_playground/components/attention/transformer_decoder.py
 vision_models_playground/components/attention/transformer_decoder_layer.py
 vision_models_playground/components/attention/transformer_encoder.py
 vision_models_playground/components/attention/transformer_encoder_layer.py
 vision_models_playground/components/convolutions/__init__.py
 vision_models_playground/components/convolutions/bottleneck_block.py
@@ -47,23 +41,35 @@
 vision_models_playground/components/convolutions/conv_transformer.py
 vision_models_playground/components/convolutions/conv_transposed_block.py
 vision_models_playground/components/convolutions/double_conv_block.py
 vision_models_playground/components/convolutions/downscale_block.py
 vision_models_playground/components/convolutions/residual_block.py
 vision_models_playground/components/convolutions/upscale_block.py
 vision_models_playground/components/convolutions/upscale_concat_block.py
+vision_models_playground/components/convolutions/yolo_v1_head.py
 vision_models_playground/components/dropout/__init__.py
 vision_models_playground/components/dropout/drop_path.py
 vision_models_playground/components/position_embedding/__init__.py
 vision_models_playground/components/position_embedding/fourier_embedding.py
+vision_models_playground/data_structures/__init__.py
+vision_models_playground/data_structures/yolo_bounding_box.py
+vision_models_playground/datasets/__init__.py
+vision_models_playground/datasets/datasets.py
+vision_models_playground/datasets/yolo_pascal_voc_dataset.py
+vision_models_playground/datasets/yolo_pascal_voc_dataset_aug.py
+vision_models_playground/evaluate/__init__.py
+vision_models_playground/evaluate/evaluate_models.py
+vision_models_playground/evaluate/evaluate_yolo.py
+vision_models_playground/losses/__init__.py
+vision_models_playground/losses/yolo_v1_loss.py
+vision_models_playground/metrics/__init__.py
+vision_models_playground/metrics/intersection_over_union.py
+vision_models_playground/metrics/loss_tracker.py
+vision_models_playground/metrics/wrapper.py
 vision_models_playground/models/__init__.py
-vision_models_playground/models/augmenters/__init__.py
-vision_models_playground/models/augmenters/augmenter.py
-vision_models_playground/models/autoencoders/__init__.py
-vision_models_playground/models/autoencoders/ff_autoencoder.py
 vision_models_playground/models/classifiers/__init__.py
 vision_models_playground/models/classifiers/conv_classifier.py
 vision_models_playground/models/classifiers/conv_vision_transformer.py
 vision_models_playground/models/classifiers/ff_classifier.py
 vision_models_playground/models/classifiers/perceiver.py
 vision_models_playground/models/classifiers/resnet.py
 vision_models_playground/models/classifiers/vision_perceiver.py
@@ -71,13 +77,42 @@
 vision_models_playground/models/generative/__init__.py
 vision_models_playground/models/generative/adverserial/__init__.py
 vision_models_playground/models/generative/adverserial/gan.py
 vision_models_playground/models/generative/adverserial/mnist_discriminator.py
 vision_models_playground/models/generative/adverserial/mnist_generator.py
 vision_models_playground/models/segmentation/__init__.py
 vision_models_playground/models/segmentation/unet.py
+vision_models_playground/models/segmentation/yolo_v1.py
+vision_models_playground/optimizers/__init__.py
+vision_models_playground/optimizers/lion.py
+vision_models_playground/pipelines/__init__.py
+vision_models_playground/pipelines/base.py
+vision_models_playground/pipelines/yolo.py
+vision_models_playground/train/__init__.py
+vision_models_playground/train/train_classifier.py
+vision_models_playground/train/train_models.py
+vision_models_playground/train/train_yolo.py
+vision_models_playground/transforms/__init__.py
+vision_models_playground/transforms/auto.py
+vision_models_playground/transforms/base.py
+vision_models_playground/transforms/choose_one.py
+vision_models_playground/transforms/clamp.py
+vision_models_playground/transforms/compose.py
+vision_models_playground/transforms/conversions.py
+vision_models_playground/transforms/normalize.py
+vision_models_playground/transforms/pad.py
+vision_models_playground/transforms/probability_transform.py
+vision_models_playground/transforms/random_affine.py
+vision_models_playground/transforms/random_horizontal_flip.py
+vision_models_playground/transforms/random_perspective.py
+vision_models_playground/transforms/random_resized_crop.py
+vision_models_playground/transforms/random_rotation.py
+vision_models_playground/transforms/random_vertical_flip.py
+vision_models_playground/transforms/resize.py
+vision_models_playground/transforms/transform.py
 vision_models_playground/utility/__init__.py
-vision_models_playground/utility/datasets.py
+vision_models_playground/utility/config.py
 vision_models_playground/utility/functions.py
+vision_models_playground/utility/hub.py
+vision_models_playground/utility/load_models.py
 vision_models_playground/utility/masks.py
-vision_models_playground/utility/train_models.py
 vision_models_playground/utility/visualize.py
```

