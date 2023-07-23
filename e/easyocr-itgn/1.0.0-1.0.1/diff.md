# Comparing `tmp/easyocr-itgn-1.0.0.tar.gz` & `tmp/easyocr-itgn-1.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "easyocr-itgn-1.0.0.tar", last modified: Sun Jul 23 16:27:09 2023, max compression
+gzip compressed data, was "easyocr-itgn-1.0.1.tar", last modified: Sun Jul 23 16:37:31 2023, max compression
```

## Comparing `easyocr-itgn-1.0.0.tar` & `easyocr-itgn-1.0.1.tar`

### file list

```diff
@@ -1,114 +1,114 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 16:27:09.957886 easyocr-itgn-1.0.0/
--rw-rw-rw-   0        0        0    11558 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/LICENSE
--rw-rw-rw-   0        0        0      201 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/MANIFEST.in
--rw-rw-rw-   0        0        0    27128 2023-07-23 16:27:09.956887 easyocr-itgn-1.0.0/PKG-INFO
--rw-rw-rw-   0        0        0    13440 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/README.md
--rw-rw-rw-   0        0        0      954 2023-07-23 16:26:28.000000 easyocr-itgn-1.0.0/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-07-23 16:27:09.957886 easyocr-itgn-1.0.0/setup.cfg
-drwxrwxrwx   0        0        0        0 2023-07-23 16:27:09.849885 easyocr-itgn-1.0.0/src/
-drwxrwxrwx   0        0        0        0 2023-07-23 16:27:09.863886 easyocr-itgn-1.0.0/src/easyocr/
-drwxrwxrwx   0        0        0        0 2023-07-23 16:27:09.864886 easyocr-itgn-1.0.0/src/easyocr/DBNet/
--rw-rw-rw-   0        0        0    29216 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/DBNet/DBNet.py
-drwxrwxrwx   0        0        0        0 2023-07-23 16:27:09.817885 easyocr-itgn-1.0.0/src/easyocr/DBNet/assets/
-drwxrwxrwx   0        0        0        0 2023-07-23 16:27:09.817885 easyocr-itgn-1.0.0/src/easyocr/DBNet/assets/ops/
-drwxrwxrwx   0        0        0        0 2023-07-23 16:27:09.866885 easyocr-itgn-1.0.0/src/easyocr/DBNet/assets/ops/dcn/
--rw-rw-rw-   0        0        0      669 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/DBNet/assets/ops/dcn/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 16:27:09.869885 easyocr-itgn-1.0.0/src/easyocr/DBNet/assets/ops/dcn/functions/
--rw-rw-rw-   0        0        0        0 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/DBNet/assets/ops/dcn/functions/__init__.py
--rw-rw-rw-   0        0        0    12140 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/DBNet/assets/ops/dcn/functions/deform_conv.py
--rw-rw-rw-   0        0        0     6095 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/DBNet/assets/ops/dcn/functions/deform_pool.py
-drwxrwxrwx   0        0        0        0 2023-07-23 16:27:09.872886 easyocr-itgn-1.0.0/src/easyocr/DBNet/assets/ops/dcn/modules/
--rw-rw-rw-   0        0        0        0 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/DBNet/assets/ops/dcn/modules/__init__.py
--rw-rw-rw-   0        0        0     5355 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/DBNet/assets/ops/dcn/modules/deform_conv.py
--rw-rw-rw-   0        0        0     7230 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/DBNet/assets/ops/dcn/modules/deform_pool.py
--rw-rw-rw-   0        0        0      966 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/DBNet/assets/ops/dcn/setup.py
-drwxrwxrwx   0        0        0        0 2023-07-23 16:27:09.875886 easyocr-itgn-1.0.0/src/easyocr/DBNet/backbones/
--rw-rw-rw-   0        0        0      166 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/DBNet/backbones/__init__.py
--rw-rw-rw-   0        0        0     9182 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/DBNet/backbones/mobilenetv3.py
--rw-rw-rw-   0        0        0    12428 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/DBNet/backbones/resnet.py
-drwxrwxrwx   0        0        0        0 2023-07-23 16:27:09.886886 easyocr-itgn-1.0.0/src/easyocr/DBNet/decoders/
--rw-rw-rw-   0        0        0      257 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/DBNet/decoders/__init__.py
--rw-rw-rw-   0        0        0     2010 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/DBNet/decoders/balance_cross_entropy_loss.py
--rw-rw-rw-   0        0        0     7151 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/DBNet/decoders/dice_loss.py
--rw-rw-rw-   0        0        0     6069 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/DBNet/decoders/feature_attention.py
--rw-rw-rw-   0        0        0     1404 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/DBNet/decoders/l1_loss.py
--rw-rw-rw-   0        0        0     4582 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/DBNet/decoders/pss_loss.py
--rw-rw-rw-   0        0        0     6264 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/DBNet/decoders/seg_detector.py
--rw-rw-rw-   0        0        0     7210 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/DBNet/decoders/seg_detector_asf.py
--rw-rw-rw-   0        0        0     9793 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/DBNet/decoders/seg_detector_loss.py
--rw-rw-rw-   0        0        0     6574 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/DBNet/decoders/simple_detection.py
-drwxrwxrwx   0        0        0        0 2023-07-23 16:27:09.890886 easyocr-itgn-1.0.0/src/easyocr/DBNet/model/
--rw-rw-rw-   0        0        0     3493 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/DBNet/model/constructor.py
--rw-rw-rw-   0        0        0     1546 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/DBNet/model/detector.py
--rw-rw-rw-   0        0        0     2521 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/DBNet/model/model.py
--rw-rw-rw-   0        0        0       54 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/__init__.py
--rw-rw-rw-   0        0        0     8942 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/cli.py
--rw-rw-rw-   0        0        0    92035 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/config.py
--rw-rw-rw-   0        0        0     2670 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/craft.py
--rw-rw-rw-   0        0        0     9834 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/craft_utils.py
--rw-rw-rw-   0        0        0     4292 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/detection.py
--rw-rw-rw-   0        0        0     8992 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.0/src/easyocr/detection_db.py
--rw-rw-rw-   0        0        0    32200 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/easyocr/easyocr.py
--rw-rw-rw-   0        0        0     5809 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/easyocr/export.py
--rw-rw-rw-   0        0        0     2265 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/easyocr/imgproc.py
-drwxrwxrwx   0        0        0        0 2023-07-23 16:27:09.894886 easyocr-itgn-1.0.0/src/easyocr/model/
--rw-rw-rw-   0        0        0        0 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/easyocr/model/__init__.py
--rw-rw-rw-   0        0        0     1497 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/easyocr/model/model.py
--rw-rw-rw-   0        0        0    11085 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/easyocr/model/modules.py
--rw-rw-rw-   0        0        0     1399 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/easyocr/model/vgg_model.py
--rw-rw-rw-   0        0        0     9546 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/easyocr/recognition.py
-drwxrwxrwx   0        0        0        0 2023-07-23 16:27:09.895886 easyocr-itgn-1.0.0/src/easyocr/scripts/
--rw-rw-rw-   0        0        0     3950 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/easyocr/scripts/compile_dbnet_dcn.py
--rw-rw-rw-   0        0        0    34897 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/easyocr/utils.py
-drwxrwxrwx   0        0        0        0 2023-07-23 16:27:09.918888 easyocr-itgn-1.0.0/src/easyocr_itgn.egg-info/
--rw-rw-rw-   0        0        0    27128 2023-07-23 16:27:09.000000 easyocr-itgn-1.0.0/src/easyocr_itgn.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0     2975 2023-07-23 16:27:09.000000 easyocr-itgn-1.0.0/src/easyocr_itgn.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 16:27:09.000000 easyocr-itgn-1.0.0/src/easyocr_itgn.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       49 2023-07-23 16:27:09.000000 easyocr-itgn-1.0.0/src/easyocr_itgn.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0      129 2023-07-23 16:27:09.000000 easyocr-itgn-1.0.0/src/easyocr_itgn.egg-info/requires.txt
--rw-rw-rw-   0        0        0       49 2023-07-23 16:27:09.000000 easyocr-itgn-1.0.0/src/easyocr_itgn.egg-info/top_level.txt
--rw-rw-rw-   0        0        0     1145 2023-07-23 16:26:12.000000 easyocr-itgn-1.0.0/src/setup.py
-drwxrwxrwx   0        0        0        0 2023-07-23 16:27:09.923886 easyocr-itgn-1.0.0/src/trainer/
-drwxrwxrwx   0        0        0        0 2023-07-23 16:27:09.928887 easyocr-itgn-1.0.0/src/trainer/craft/
-drwxrwxrwx   0        0        0        0 2023-07-23 16:27:09.930886 easyocr-itgn-1.0.0/src/trainer/craft/config/
--rw-rw-rw-   0        0        0        0 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/trainer/craft/config/__init__.py
--rw-rw-rw-   0        0        0      987 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/trainer/craft/config/load_config.py
-drwxrwxrwx   0        0        0        0 2023-07-23 16:27:09.936886 easyocr-itgn-1.0.0/src/trainer/craft/data/
--rw-rw-rw-   0        0        0     2311 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/trainer/craft/data/boxEnlarge.py
--rw-rw-rw-   0        0        0    18308 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/trainer/craft/data/dataset.py
--rw-rw-rw-   0        0        0     7418 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/trainer/craft/data/gaussian.py
--rw-rw-rw-   0        0        0     5491 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/trainer/craft/data/imgaug.py
--rw-rw-rw-   0        0        0     2431 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/trainer/craft/data/imgproc.py
-drwxrwxrwx   0        0        0        0 2023-07-23 16:27:09.938886 easyocr-itgn-1.0.0/src/trainer/craft/data/pseudo_label/
--rw-rw-rw-   0        0        0     9308 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/trainer/craft/data/pseudo_label/make_charbox.py
--rw-rw-rw-   0        0        0     1353 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/trainer/craft/data/pseudo_label/watershed.py
--rw-rw-rw-   0        0        0    12389 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/trainer/craft/eval.py
-drwxrwxrwx   0        0        0        0 2023-07-23 16:27:09.939886 easyocr-itgn-1.0.0/src/trainer/craft/loss/
--rw-rw-rw-   0        0        0     5881 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/trainer/craft/loss/mseloss.py
-drwxrwxrwx   0        0        0        0 2023-07-23 16:27:09.940887 easyocr-itgn-1.0.0/src/trainer/craft/metrics/
--rw-rw-rw-   0        0        0     8909 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/trainer/craft/metrics/eval_det_iou.py
-drwxrwxrwx   0        0        0        0 2023-07-23 16:27:09.942886 easyocr-itgn-1.0.0/src/trainer/craft/model/
--rw-rw-rw-   0        0        0     3899 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/trainer/craft/model/craft.py
--rw-rw-rw-   0        0        0     3039 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/trainer/craft/model/vgg16_bn.py
--rw-rw-rw-   0        0        0    17809 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/trainer/craft/train.py
--rw-rw-rw-   0        0        0    14880 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/trainer/craft/trainSynth.py
--rw-rw-rw-   0        0        0    19817 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/trainer/craft/train_distributed.py
-drwxrwxrwx   0        0        0        0 2023-07-23 16:27:09.946886 easyocr-itgn-1.0.0/src/trainer/craft/utils/
--rw-rw-rw-   0        0        0    14030 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/trainer/craft/utils/craft_utils.py
--rw-rw-rw-   0        0        0    12117 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/trainer/craft/utils/inference_boxes.py
--rw-rw-rw-   0        0        0     4901 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/trainer/craft/utils/util.py
--rw-rw-rw-   0        0        0    11343 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/trainer/dataset.py
--rw-rw-rw-   0        0        0     3647 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/trainer/model.py
-drwxrwxrwx   0        0        0        0 2023-07-23 16:27:09.950888 easyocr-itgn-1.0.0/src/trainer/modules/
--rw-rw-rw-   0        0        0    10612 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/trainer/modules/feature_extraction.py
--rw-rw-rw-   0        0        0     4107 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/trainer/modules/prediction.py
--rw-rw-rw-   0        0        0      818 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/trainer/modules/sequence_modeling.py
--rw-rw-rw-   0        0        0     8276 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/trainer/modules/transformation.py
--rw-rw-rw-   0        0        0     4834 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/trainer/test.py
--rw-rw-rw-   0        0        0    12480 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/trainer/train.py
--rw-rw-rw-   0        0        0    14883 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/trainer/utils.py
-drwxrwxrwx   0        0        0        0 2023-07-23 16:27:09.955886 easyocr-itgn-1.0.0/src/unit_test/
--rw-rw-rw-   0        0        0      424 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/unit_test/demo.py
--rw-rw-rw-   0        0        0    25589 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/unit_test/make_test_solution.py
--rw-rw-rw-   0        0        0      901 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/unit_test/run_unit_test.py
--rw-rw-rw-   0        0        0    10837 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.0/src/unit_test/unit_test.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:37:31.771481 easyocr-itgn-1.0.1/
+-rw-rw-rw-   0        0        0    11558 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/LICENSE
+-rw-rw-rw-   0        0        0      201 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/MANIFEST.in
+-rw-rw-rw-   0        0        0    27128 2023-07-23 16:37:31.771481 easyocr-itgn-1.0.1/PKG-INFO
+-rw-rw-rw-   0        0        0    13440 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/README.md
+-rw-rw-rw-   0        0        0      964 2023-07-23 16:36:51.000000 easyocr-itgn-1.0.1/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-07-23 16:37:31.771481 easyocr-itgn-1.0.1/setup.cfg
+drwxrwxrwx   0        0        0        0 2023-07-23 16:37:31.665476 easyocr-itgn-1.0.1/src/
+drwxrwxrwx   0        0        0        0 2023-07-23 16:37:31.681478 easyocr-itgn-1.0.1/src/easyocr_itgn/
+drwxrwxrwx   0        0        0        0 2023-07-23 16:37:31.704478 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/
+-rw-rw-rw-   0        0        0    29216 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/DBNet.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:37:31.632479 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/assets/
+drwxrwxrwx   0        0        0        0 2023-07-23 16:37:31.632479 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/assets/ops/
+drwxrwxrwx   0        0        0        0 2023-07-23 16:37:31.706479 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/assets/ops/dcn/
+-rw-rw-rw-   0        0        0      669 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/assets/ops/dcn/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:37:31.709479 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/assets/ops/dcn/functions/
+-rw-rw-rw-   0        0        0        0 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/assets/ops/dcn/functions/__init__.py
+-rw-rw-rw-   0        0        0    12140 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/assets/ops/dcn/functions/deform_conv.py
+-rw-rw-rw-   0        0        0     6095 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/assets/ops/dcn/functions/deform_pool.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:37:31.712480 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/assets/ops/dcn/modules/
+-rw-rw-rw-   0        0        0        0 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/assets/ops/dcn/modules/__init__.py
+-rw-rw-rw-   0        0        0     5355 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/assets/ops/dcn/modules/deform_conv.py
+-rw-rw-rw-   0        0        0     7230 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/assets/ops/dcn/modules/deform_pool.py
+-rw-rw-rw-   0        0        0      966 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/assets/ops/dcn/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:37:31.715480 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/backbones/
+-rw-rw-rw-   0        0        0      166 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/backbones/__init__.py
+-rw-rw-rw-   0        0        0     9182 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/backbones/mobilenetv3.py
+-rw-rw-rw-   0        0        0    12428 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/backbones/resnet.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:37:31.726479 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/decoders/
+-rw-rw-rw-   0        0        0      257 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/decoders/__init__.py
+-rw-rw-rw-   0        0        0     2010 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/decoders/balance_cross_entropy_loss.py
+-rw-rw-rw-   0        0        0     7151 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/decoders/dice_loss.py
+-rw-rw-rw-   0        0        0     6069 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/decoders/feature_attention.py
+-rw-rw-rw-   0        0        0     1404 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/decoders/l1_loss.py
+-rw-rw-rw-   0        0        0     4582 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/decoders/pss_loss.py
+-rw-rw-rw-   0        0        0     6264 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/decoders/seg_detector.py
+-rw-rw-rw-   0        0        0     7210 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/decoders/seg_detector_asf.py
+-rw-rw-rw-   0        0        0     9793 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/decoders/seg_detector_loss.py
+-rw-rw-rw-   0        0        0     6574 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/decoders/simple_detection.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:37:31.730479 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/model/
+-rw-rw-rw-   0        0        0     3493 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/model/constructor.py
+-rw-rw-rw-   0        0        0     1546 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/model/detector.py
+-rw-rw-rw-   0        0        0     2521 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/model/model.py
+-rw-rw-rw-   0        0        0       54 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/__init__.py
+-rw-rw-rw-   0        0        0     8942 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/cli.py
+-rw-rw-rw-   0        0        0    92035 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/config.py
+-rw-rw-rw-   0        0        0     2670 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/craft.py
+-rw-rw-rw-   0        0        0     9834 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/craft_utils.py
+-rw-rw-rw-   0        0        0     4292 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/detection.py
+-rw-rw-rw-   0        0        0     8992 2023-07-23 15:28:24.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/detection_db.py
+-rw-rw-rw-   0        0        0    32200 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/easyocr.py
+-rw-rw-rw-   0        0        0     5809 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/export.py
+-rw-rw-rw-   0        0        0     2265 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/imgproc.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:37:31.734480 easyocr-itgn-1.0.1/src/easyocr_itgn/model/
+-rw-rw-rw-   0        0        0        0 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/model/__init__.py
+-rw-rw-rw-   0        0        0     1497 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/model/model.py
+-rw-rw-rw-   0        0        0    11085 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/model/modules.py
+-rw-rw-rw-   0        0        0     1399 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/model/vgg_model.py
+-rw-rw-rw-   0        0        0     9546 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/recognition.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:37:31.735478 easyocr-itgn-1.0.1/src/easyocr_itgn/scripts/
+-rw-rw-rw-   0        0        0     3950 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/scripts/compile_dbnet_dcn.py
+-rw-rw-rw-   0        0        0    34897 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/easyocr_itgn/utils.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:37:31.703479 easyocr-itgn-1.0.1/src/easyocr_itgn.egg-info/
+-rw-rw-rw-   0        0        0    27128 2023-07-23 16:37:31.000000 easyocr-itgn-1.0.1/src/easyocr_itgn.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0     3185 2023-07-23 16:37:31.000000 easyocr-itgn-1.0.1/src/easyocr_itgn.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 16:37:31.000000 easyocr-itgn-1.0.1/src/easyocr_itgn.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       59 2023-07-23 16:37:31.000000 easyocr-itgn-1.0.1/src/easyocr_itgn.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0      129 2023-07-23 16:37:31.000000 easyocr-itgn-1.0.1/src/easyocr_itgn.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       54 2023-07-23 16:37:31.000000 easyocr-itgn-1.0.1/src/easyocr_itgn.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0     1150 2023-07-23 16:36:48.000000 easyocr-itgn-1.0.1/src/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:37:31.740478 easyocr-itgn-1.0.1/src/trainer/
+drwxrwxrwx   0        0        0        0 2023-07-23 16:37:31.744478 easyocr-itgn-1.0.1/src/trainer/craft/
+drwxrwxrwx   0        0        0        0 2023-07-23 16:37:31.746478 easyocr-itgn-1.0.1/src/trainer/craft/config/
+-rw-rw-rw-   0        0        0        0 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/trainer/craft/config/__init__.py
+-rw-rw-rw-   0        0        0      987 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/trainer/craft/config/load_config.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:37:31.752478 easyocr-itgn-1.0.1/src/trainer/craft/data/
+-rw-rw-rw-   0        0        0     2311 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/trainer/craft/data/boxEnlarge.py
+-rw-rw-rw-   0        0        0    18308 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/trainer/craft/data/dataset.py
+-rw-rw-rw-   0        0        0     7418 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/trainer/craft/data/gaussian.py
+-rw-rw-rw-   0        0        0     5491 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/trainer/craft/data/imgaug.py
+-rw-rw-rw-   0        0        0     2431 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/trainer/craft/data/imgproc.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:37:31.754478 easyocr-itgn-1.0.1/src/trainer/craft/data/pseudo_label/
+-rw-rw-rw-   0        0        0     9308 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/trainer/craft/data/pseudo_label/make_charbox.py
+-rw-rw-rw-   0        0        0     1353 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/trainer/craft/data/pseudo_label/watershed.py
+-rw-rw-rw-   0        0        0    12389 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/trainer/craft/eval.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:37:31.755478 easyocr-itgn-1.0.1/src/trainer/craft/loss/
+-rw-rw-rw-   0        0        0     5881 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/trainer/craft/loss/mseloss.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:37:31.756480 easyocr-itgn-1.0.1/src/trainer/craft/metrics/
+-rw-rw-rw-   0        0        0     8909 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/trainer/craft/metrics/eval_det_iou.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:37:31.758481 easyocr-itgn-1.0.1/src/trainer/craft/model/
+-rw-rw-rw-   0        0        0     3899 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/trainer/craft/model/craft.py
+-rw-rw-rw-   0        0        0     3039 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/trainer/craft/model/vgg16_bn.py
+-rw-rw-rw-   0        0        0    17809 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/trainer/craft/train.py
+-rw-rw-rw-   0        0        0    14880 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/trainer/craft/trainSynth.py
+-rw-rw-rw-   0        0        0    19817 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/trainer/craft/train_distributed.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:37:31.761481 easyocr-itgn-1.0.1/src/trainer/craft/utils/
+-rw-rw-rw-   0        0        0    14030 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/trainer/craft/utils/craft_utils.py
+-rw-rw-rw-   0        0        0    12117 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/trainer/craft/utils/inference_boxes.py
+-rw-rw-rw-   0        0        0     4901 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/trainer/craft/utils/util.py
+-rw-rw-rw-   0        0        0    11343 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/trainer/dataset.py
+-rw-rw-rw-   0        0        0     3647 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/trainer/model.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:37:31.765481 easyocr-itgn-1.0.1/src/trainer/modules/
+-rw-rw-rw-   0        0        0    10612 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/trainer/modules/feature_extraction.py
+-rw-rw-rw-   0        0        0     4107 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/trainer/modules/prediction.py
+-rw-rw-rw-   0        0        0      818 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/trainer/modules/sequence_modeling.py
+-rw-rw-rw-   0        0        0     8276 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/trainer/modules/transformation.py
+-rw-rw-rw-   0        0        0     4834 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/trainer/test.py
+-rw-rw-rw-   0        0        0    12480 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/trainer/train.py
+-rw-rw-rw-   0        0        0    14883 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/trainer/utils.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:37:31.769481 easyocr-itgn-1.0.1/src/unit_test/
+-rw-rw-rw-   0        0        0      424 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/unit_test/demo.py
+-rw-rw-rw-   0        0        0    25589 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/unit_test/make_test_solution.py
+-rw-rw-rw-   0        0        0      901 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/unit_test/run_unit_test.py
+-rw-rw-rw-   0        0        0    10837 2023-07-23 15:28:26.000000 easyocr-itgn-1.0.1/src/unit_test/unit_test.py
```

### Comparing `easyocr-itgn-1.0.0/LICENSE` & `easyocr-itgn-1.0.1/LICENSE`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/PKG-INFO` & `easyocr-itgn-1.0.1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: easyocr-itgn
-Version: 1.0.0
+Version: 1.0.1
 Summary: Easyorc fixed for pil 10
 Author-email: Austin Bryant <c00481025@louisiana.edu>
 License:                                  Apache License
                                    Version 2.0, January 2004
                                 http://www.apache.org/licenses/
         
            TERMS AND CONDITIONS FOR USE, REPRODUCTION, AND DISTRIBUTION
```

### Comparing `easyocr-itgn-1.0.0/README.md` & `easyocr-itgn-1.0.1/README.md`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/pyproject.toml` & `easyocr-itgn-1.0.1/pyproject.toml`

 * *Files 11% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires      = ["setuptools>=61.0.0", "wheel"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "easyocr-itgn"
-version = "1.0.0"
+version = "1.0.1"
 description = "Easyorc fixed for pil 10"
 readme = "README.md"
 authors = [{ name = "Austin Bryant", email = "c00481025@louisiana.edu" }]
 license = { file = "LICENSE" }
 classifiers = [
     "License :: OSI Approved :: MIT License",
     "Programming Language :: Python",
@@ -31,8 +31,8 @@
 ]
 requires-python = ">=3.11"
 
 [project.urls]
 Homepage = "https://github.com/JaidedAI/EasyOCR"
 
 [project.scripts]
-easyorc = "easyocr.easyocr:main"
+easyorc_itgn = "easyocr_itgn.easyocr:main"
```

### Comparing `easyocr-itgn-1.0.0/src/easyocr/DBNet/DBNet.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/DBNet.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/DBNet/assets/ops/dcn/__init__.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/assets/ops/dcn/__init__.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/DBNet/assets/ops/dcn/functions/deform_conv.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/assets/ops/dcn/functions/deform_conv.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/DBNet/assets/ops/dcn/functions/deform_pool.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/assets/ops/dcn/functions/deform_pool.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/DBNet/assets/ops/dcn/modules/deform_conv.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/assets/ops/dcn/modules/deform_conv.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/DBNet/assets/ops/dcn/modules/deform_pool.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/assets/ops/dcn/modules/deform_pool.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/DBNet/assets/ops/dcn/setup.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/assets/ops/dcn/setup.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/DBNet/backbones/mobilenetv3.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/backbones/mobilenetv3.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/DBNet/backbones/resnet.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/backbones/resnet.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/DBNet/decoders/balance_cross_entropy_loss.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/decoders/balance_cross_entropy_loss.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/DBNet/decoders/dice_loss.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/decoders/dice_loss.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/DBNet/decoders/feature_attention.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/decoders/feature_attention.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/DBNet/decoders/l1_loss.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/decoders/l1_loss.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/DBNet/decoders/pss_loss.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/decoders/pss_loss.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/DBNet/decoders/seg_detector.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/decoders/seg_detector.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/DBNet/decoders/seg_detector_asf.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/decoders/seg_detector_asf.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/DBNet/decoders/seg_detector_loss.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/decoders/seg_detector_loss.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/DBNet/decoders/simple_detection.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/decoders/simple_detection.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/DBNet/model/constructor.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/model/constructor.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/DBNet/model/detector.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/model/detector.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/DBNet/model/model.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/DBNet/model/model.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/cli.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/cli.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/config.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/config.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/craft.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/craft.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/craft_utils.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/craft_utils.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/detection.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/detection.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/detection_db.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/detection_db.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/easyocr.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/easyocr.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/export.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/export.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/imgproc.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/imgproc.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/model/model.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/model/model.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/model/modules.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/model/modules.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/model/vgg_model.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/model/vgg_model.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/recognition.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/recognition.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/scripts/compile_dbnet_dcn.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/scripts/compile_dbnet_dcn.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr/utils.py` & `easyocr-itgn-1.0.1/src/easyocr_itgn/utils.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/easyocr_itgn.egg-info/PKG-INFO` & `easyocr-itgn-1.0.1/src/easyocr_itgn.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: easyocr-itgn
-Version: 1.0.0
+Version: 1.0.1
 Summary: Easyorc fixed for pil 10
 Author-email: Austin Bryant <c00481025@louisiana.edu>
 License:                                  Apache License
                                    Version 2.0, January 2004
                                 http://www.apache.org/licenses/
         
            TERMS AND CONDITIONS FOR USE, REPRODUCTION, AND DISTRIBUTION
```

### Comparing `easyocr-itgn-1.0.0/src/easyocr_itgn.egg-info/SOURCES.txt` & `easyocr-itgn-1.0.1/src/easyocr_itgn.egg-info/SOURCES.txt`

 * *Files 15% similar despite different names*

```diff
@@ -1,60 +1,60 @@
 LICENSE
 MANIFEST.in
 README.md
 pyproject.toml
 src/setup.py
-src/easyocr/__init__.py
-src/easyocr/cli.py
-src/easyocr/config.py
-src/easyocr/craft.py
-src/easyocr/craft_utils.py
-src/easyocr/detection.py
-src/easyocr/detection_db.py
-src/easyocr/easyocr.py
-src/easyocr/export.py
-src/easyocr/imgproc.py
-src/easyocr/recognition.py
-src/easyocr/utils.py
-src/easyocr/DBNet/DBNet.py
-src/easyocr/DBNet/assets/ops/dcn/__init__.py
-src/easyocr/DBNet/assets/ops/dcn/setup.py
-src/easyocr/DBNet/assets/ops/dcn/functions/__init__.py
-src/easyocr/DBNet/assets/ops/dcn/functions/deform_conv.py
-src/easyocr/DBNet/assets/ops/dcn/functions/deform_pool.py
-src/easyocr/DBNet/assets/ops/dcn/modules/__init__.py
-src/easyocr/DBNet/assets/ops/dcn/modules/deform_conv.py
-src/easyocr/DBNet/assets/ops/dcn/modules/deform_pool.py
-src/easyocr/DBNet/backbones/__init__.py
-src/easyocr/DBNet/backbones/mobilenetv3.py
-src/easyocr/DBNet/backbones/resnet.py
-src/easyocr/DBNet/decoders/__init__.py
-src/easyocr/DBNet/decoders/balance_cross_entropy_loss.py
-src/easyocr/DBNet/decoders/dice_loss.py
-src/easyocr/DBNet/decoders/feature_attention.py
-src/easyocr/DBNet/decoders/l1_loss.py
-src/easyocr/DBNet/decoders/pss_loss.py
-src/easyocr/DBNet/decoders/seg_detector.py
-src/easyocr/DBNet/decoders/seg_detector_asf.py
-src/easyocr/DBNet/decoders/seg_detector_loss.py
-src/easyocr/DBNet/decoders/simple_detection.py
-src/easyocr/DBNet/model/constructor.py
-src/easyocr/DBNet/model/detector.py
-src/easyocr/DBNet/model/model.py
-src/easyocr/model/__init__.py
-src/easyocr/model/model.py
-src/easyocr/model/modules.py
-src/easyocr/model/vgg_model.py
-src/easyocr/scripts/compile_dbnet_dcn.py
+src/easyocr_itgn/__init__.py
+src/easyocr_itgn/cli.py
+src/easyocr_itgn/config.py
+src/easyocr_itgn/craft.py
+src/easyocr_itgn/craft_utils.py
+src/easyocr_itgn/detection.py
+src/easyocr_itgn/detection_db.py
+src/easyocr_itgn/easyocr.py
+src/easyocr_itgn/export.py
+src/easyocr_itgn/imgproc.py
+src/easyocr_itgn/recognition.py
+src/easyocr_itgn/utils.py
 src/easyocr_itgn.egg-info/PKG-INFO
 src/easyocr_itgn.egg-info/SOURCES.txt
 src/easyocr_itgn.egg-info/dependency_links.txt
 src/easyocr_itgn.egg-info/entry_points.txt
 src/easyocr_itgn.egg-info/requires.txt
 src/easyocr_itgn.egg-info/top_level.txt
+src/easyocr_itgn/DBNet/DBNet.py
+src/easyocr_itgn/DBNet/assets/ops/dcn/__init__.py
+src/easyocr_itgn/DBNet/assets/ops/dcn/setup.py
+src/easyocr_itgn/DBNet/assets/ops/dcn/functions/__init__.py
+src/easyocr_itgn/DBNet/assets/ops/dcn/functions/deform_conv.py
+src/easyocr_itgn/DBNet/assets/ops/dcn/functions/deform_pool.py
+src/easyocr_itgn/DBNet/assets/ops/dcn/modules/__init__.py
+src/easyocr_itgn/DBNet/assets/ops/dcn/modules/deform_conv.py
+src/easyocr_itgn/DBNet/assets/ops/dcn/modules/deform_pool.py
+src/easyocr_itgn/DBNet/backbones/__init__.py
+src/easyocr_itgn/DBNet/backbones/mobilenetv3.py
+src/easyocr_itgn/DBNet/backbones/resnet.py
+src/easyocr_itgn/DBNet/decoders/__init__.py
+src/easyocr_itgn/DBNet/decoders/balance_cross_entropy_loss.py
+src/easyocr_itgn/DBNet/decoders/dice_loss.py
+src/easyocr_itgn/DBNet/decoders/feature_attention.py
+src/easyocr_itgn/DBNet/decoders/l1_loss.py
+src/easyocr_itgn/DBNet/decoders/pss_loss.py
+src/easyocr_itgn/DBNet/decoders/seg_detector.py
+src/easyocr_itgn/DBNet/decoders/seg_detector_asf.py
+src/easyocr_itgn/DBNet/decoders/seg_detector_loss.py
+src/easyocr_itgn/DBNet/decoders/simple_detection.py
+src/easyocr_itgn/DBNet/model/constructor.py
+src/easyocr_itgn/DBNet/model/detector.py
+src/easyocr_itgn/DBNet/model/model.py
+src/easyocr_itgn/model/__init__.py
+src/easyocr_itgn/model/model.py
+src/easyocr_itgn/model/modules.py
+src/easyocr_itgn/model/vgg_model.py
+src/easyocr_itgn/scripts/compile_dbnet_dcn.py
 src/trainer/dataset.py
 src/trainer/model.py
 src/trainer/test.py
 src/trainer/train.py
 src/trainer/utils.py
 src/trainer/craft/eval.py
 src/trainer/craft/train.py
```

### Comparing `easyocr-itgn-1.0.0/src/setup.py` & `easyocr-itgn-1.0.1/src/setup.py`

 * *Files 3% similar despite different names*

```diff
@@ -9,20 +9,20 @@
 
 def readme():
     with open('README.md', encoding="utf-8-sig") as f:
         README = f.read()
     return README
 
 setup(
-    name='easyocr-itgn',
-    packages=['easyocr-itgn'],
+    name='easyocr_itgn',
+    packages=['easyocr_itgn'],
     include_package_data=True,
-    version='1.7.0',
+    version='1.0.1',
     install_requires=requirements,
-    entry_points={"console_scripts": ["easyocr= easyocr.cli:main"]},
+    entry_points={"console_scripts": ["easyocr= easyocr_itgn.cli:main"]},
     license='Apache License 2.0',
     description='End-to-End Multi-Lingual Optical Character Recognition (OCR) Solution',
     long_description=readme(),
     long_description_content_type="text/markdown",
     author='Rakpong Kittinaradorn',
     author_email='r.kittinaradorn@gmail.com',
     url='https://github.com/jaidedai/easyocr',
```

### Comparing `easyocr-itgn-1.0.0/src/trainer/craft/config/load_config.py` & `easyocr-itgn-1.0.1/src/trainer/craft/config/load_config.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/trainer/craft/data/boxEnlarge.py` & `easyocr-itgn-1.0.1/src/trainer/craft/data/boxEnlarge.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/trainer/craft/data/dataset.py` & `easyocr-itgn-1.0.1/src/trainer/craft/data/dataset.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/trainer/craft/data/gaussian.py` & `easyocr-itgn-1.0.1/src/trainer/craft/data/gaussian.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/trainer/craft/data/imgaug.py` & `easyocr-itgn-1.0.1/src/trainer/craft/data/imgaug.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/trainer/craft/data/imgproc.py` & `easyocr-itgn-1.0.1/src/trainer/craft/data/imgproc.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/trainer/craft/data/pseudo_label/make_charbox.py` & `easyocr-itgn-1.0.1/src/trainer/craft/data/pseudo_label/make_charbox.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/trainer/craft/data/pseudo_label/watershed.py` & `easyocr-itgn-1.0.1/src/trainer/craft/data/pseudo_label/watershed.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/trainer/craft/eval.py` & `easyocr-itgn-1.0.1/src/trainer/craft/eval.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/trainer/craft/loss/mseloss.py` & `easyocr-itgn-1.0.1/src/trainer/craft/loss/mseloss.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/trainer/craft/metrics/eval_det_iou.py` & `easyocr-itgn-1.0.1/src/trainer/craft/metrics/eval_det_iou.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/trainer/craft/model/craft.py` & `easyocr-itgn-1.0.1/src/trainer/craft/model/craft.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/trainer/craft/model/vgg16_bn.py` & `easyocr-itgn-1.0.1/src/trainer/craft/model/vgg16_bn.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/trainer/craft/train.py` & `easyocr-itgn-1.0.1/src/trainer/craft/train.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/trainer/craft/trainSynth.py` & `easyocr-itgn-1.0.1/src/trainer/craft/trainSynth.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/trainer/craft/train_distributed.py` & `easyocr-itgn-1.0.1/src/trainer/craft/train_distributed.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/trainer/craft/utils/craft_utils.py` & `easyocr-itgn-1.0.1/src/trainer/craft/utils/craft_utils.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/trainer/craft/utils/inference_boxes.py` & `easyocr-itgn-1.0.1/src/trainer/craft/utils/inference_boxes.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/trainer/craft/utils/util.py` & `easyocr-itgn-1.0.1/src/trainer/craft/utils/util.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/trainer/dataset.py` & `easyocr-itgn-1.0.1/src/trainer/dataset.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/trainer/model.py` & `easyocr-itgn-1.0.1/src/trainer/model.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/trainer/modules/feature_extraction.py` & `easyocr-itgn-1.0.1/src/trainer/modules/feature_extraction.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/trainer/modules/prediction.py` & `easyocr-itgn-1.0.1/src/trainer/modules/prediction.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/trainer/modules/sequence_modeling.py` & `easyocr-itgn-1.0.1/src/trainer/modules/sequence_modeling.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/trainer/modules/transformation.py` & `easyocr-itgn-1.0.1/src/trainer/modules/transformation.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/trainer/test.py` & `easyocr-itgn-1.0.1/src/trainer/test.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/trainer/train.py` & `easyocr-itgn-1.0.1/src/trainer/train.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/trainer/utils.py` & `easyocr-itgn-1.0.1/src/trainer/utils.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/unit_test/make_test_solution.py` & `easyocr-itgn-1.0.1/src/unit_test/make_test_solution.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/unit_test/run_unit_test.py` & `easyocr-itgn-1.0.1/src/unit_test/run_unit_test.py`

 * *Files identical despite different names*

### Comparing `easyocr-itgn-1.0.0/src/unit_test/unit_test.py` & `easyocr-itgn-1.0.1/src/unit_test/unit_test.py`

 * *Files identical despite different names*

