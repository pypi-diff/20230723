# Comparing `tmp/m6anet-2.0.2.tar.gz` & `tmp/m6anet-2.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "/home/runner/work/m6anet/m6anet/dist/.tmp-rpj6yx_5/m6anet-2.0.2.tar", last modified: Sat Apr 29 13:17:58 2023, max compression
+gzip compressed data, was "m6anet-2.1.0.tar", last modified: Sun Jul 23 15:18:13 2023, max compression
```

## Comparing `m6anet-2.0.2.tar` & `m6anet-2.1.0.tar`

### file list

```diff
@@ -1,56 +1,102 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-29 13:17:58.000000 m6anet-2.0.2/
--rw-r--r--   0 runner    (1001) docker     (123)     1066 2023-04-29 13:17:49.000000 m6anet-2.0.2/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     2070 2023-04-29 13:17:58.000000 m6anet-2.0.2/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1363 2023-04-29 13:17:49.000000 m6anet-2.0.2/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-29 13:17:58.000000 m6anet-2.0.2/m6anet/
--rw-r--r--   0 runner    (1001) docker     (123)      946 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-29 13:17:58.000000 m6anet-2.0.2/m6anet/deprecated/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/deprecated/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1885 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/deprecated/compute_norm_factors.py
--rw-r--r--   0 runner    (1001) docker     (123)     2865 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/deprecated/dataprep.py
--rw-r--r--   0 runner    (1001) docker     (123)     4297 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/deprecated/inference.py
--rw-r--r--   0 runner    (1001) docker     (123)     5817 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/deprecated/train.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-29 13:17:58.000000 m6anet-2.0.2/m6anet/model/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/model/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-29 13:17:58.000000 m6anet-2.0.2/m6anet/model/configs/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-29 13:17:58.000000 m6anet-2.0.2/m6anet/model/configs/model_configs/
--rw-r--r--   0 runner    (1001) docker     (123)      578 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/model/configs/model_configs/m6anet.toml
--rw-r--r--   0 runner    (1001) docker     (123)     7116 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/model/model.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-29 13:17:58.000000 m6anet-2.0.2/m6anet/model/model_blocks/
--rw-r--r--   0 runner    (1001) docker     (123)      810 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/model/model_blocks/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     9672 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/model/model_blocks/blocks.py
--rw-r--r--   0 runner    (1001) docker     (123)    15720 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/model/model_blocks/pooling_blocks.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-29 13:17:58.000000 m6anet-2.0.2/m6anet/model/model_states/
--rw-r--r--   0 runner    (1001) docker     (123)    37083 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/model/model_states/human_hct116.pt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-29 13:17:58.000000 m6anet-2.0.2/m6anet/model/norm_factors/
--rw-r--r--   0 runner    (1001) docker     (123)   179264 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/model/norm_factors/norm_factors_hct116.joblib
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-29 13:17:58.000000 m6anet-2.0.2/m6anet/scripts/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/scripts/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1608 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/scripts/compute_norm_factors.py
--rw-r--r--   0 runner    (1001) docker     (123)     1056 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/scripts/convert.py
--rw-r--r--   0 runner    (1001) docker     (123)     2817 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/scripts/dataprep.py
--rw-r--r--   0 runner    (1001) docker     (123)     3866 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/scripts/inference.py
--rw-r--r--   0 runner    (1001) docker     (123)     5570 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/scripts/train.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-29 13:17:58.000000 m6anet-2.0.2/m6anet/utils/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5099 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/utils/builder.py
--rw-r--r--   0 runner    (1001) docker     (123)     1225 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/utils/constants.py
--rw-r--r--   0 runner    (1001) docker     (123)    27787 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/utils/data_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)    26928 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/utils/dataprep_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     3281 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/utils/helper.py
--rw-r--r--   0 runner    (1001) docker     (123)     7722 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/utils/inference_utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-29 13:17:58.000000 m6anet-2.0.2/m6anet/utils/loss_functions/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/utils/loss_functions/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1473 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/utils/loss_functions/loss_functions.py
--rw-r--r--   0 runner    (1001) docker     (123)     8833 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/utils/norm_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)    11172 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/utils/sampler_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)    11905 2023-04-29 13:17:49.000000 m6anet-2.0.2/m6anet/utils/training_utils.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-04-29 13:17:58.000000 m6anet-2.0.2/m6anet.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2070 2023-04-29 13:17:58.000000 m6anet-2.0.2/m6anet.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1227 2023-04-29 13:17:58.000000 m6anet-2.0.2/m6anet.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-04-29 13:17:58.000000 m6anet-2.0.2/m6anet.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      263 2023-04-29 13:17:58.000000 m6anet-2.0.2/m6anet.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)      222 2023-04-29 13:17:58.000000 m6anet-2.0.2/m6anet.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        7 2023-04-29 13:17:58.000000 m6anet-2.0.2/m6anet.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-04-29 13:17:58.000000 m6anet-2.0.2/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     2476 2023-04-29 13:17:49.000000 m6anet-2.0.2/setup.py
+drwxrwxr-x   0 christopherhendra  (1003) christopherhendra  (1003)        0 2023-07-23 15:18:13.072598 m6anet-2.1.0/
+drwxrwxr-x   0 christopherhendra  (1003) christopherhendra  (1003)        0 2023-07-23 15:18:13.060598 m6anet-2.1.0/.github/
+drwxrwxr-x   0 christopherhendra  (1003) christopherhendra  (1003)        0 2023-07-23 15:18:13.064598 m6anet-2.1.0/.github/workflows/
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     1233 2023-07-23 15:08:29.000000 m6anet-2.1.0/.github/workflows/merge_test.yaml
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)      671 2023-07-22 11:27:01.000000 m6anet-2.1.0/.github/workflows/publish.yaml
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     2084 2023-07-23 15:08:29.000000 m6anet-2.1.0/.gitignore
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     1066 2022-01-14 07:36:33.000000 m6anet-2.1.0/LICENSE
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)    18340 2023-07-23 15:18:13.072598 m6anet-2.1.0/PKG-INFO
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)    17593 2023-07-23 15:08:29.000000 m6anet-2.1.0/README.md
+drwxrwxr-x   0 christopherhendra  (1003) christopherhendra  (1003)        0 2023-07-23 15:18:13.064598 m6anet-2.1.0/docs/
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)      659 2022-01-14 07:36:33.000000 m6anet-2.1.0/docs/Makefile
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)      799 2022-01-14 07:36:33.000000 m6anet-2.1.0/docs/make.bat
+drwxrwxr-x   0 christopherhendra  (1003) christopherhendra  (1003)        0 2023-07-23 15:18:13.064598 m6anet-2.1.0/docs/source/
+drwxrwxr-x   0 christopherhendra  (1003) christopherhendra  (1003)        0 2023-07-23 15:18:13.064598 m6anet-2.1.0/docs/source/_images/
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)    23828 2023-07-23 15:08:29.000000 m6anet-2.1.0/docs/source/_images/RNA004_mapq0_HEK293T.jpg
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)    22131 2023-07-23 15:08:29.000000 m6anet-2.1.0/docs/source/_images/RNA004_mapq0_Hct116.jpg
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)    24255 2023-07-23 15:08:29.000000 m6anet-2.1.0/docs/source/_images/RNA004_mapq20_HEK293T.jpg
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)    22698 2023-07-23 15:08:29.000000 m6anet-2.1.0/docs/source/_images/RNA004_mapq20_Hct116.jpg
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)    28460 2023-02-24 09:45:39.000000 m6anet-2.1.0/docs/source/_images/arabidopsis_hek293t_mixtures.png
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)   287750 2023-02-24 09:45:39.000000 m6anet-2.1.0/docs/source/_images/m6anet_virc_roc_pr.png
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)      310 2023-02-24 09:45:39.000000 m6anet-2.1.0/docs/source/citing.rst
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     7853 2023-07-23 15:08:29.000000 m6anet-2.1.0/docs/source/cmd.rst
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     2032 2022-01-14 07:36:33.000000 m6anet-2.1.0/docs/source/conf.py
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)      398 2023-02-20 09:15:40.000000 m6anet-2.1.0/docs/source/help.rst
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     1830 2023-07-23 15:08:29.000000 m6anet-2.1.0/docs/source/index.rst
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)      602 2023-07-23 15:08:29.000000 m6anet-2.1.0/docs/source/installation.rst
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     4676 2023-07-23 15:08:29.000000 m6anet-2.1.0/docs/source/quickstart.rst
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     5132 2023-07-23 15:08:29.000000 m6anet-2.1.0/docs/source/rna004_release_note.rst
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     5080 2023-02-24 09:45:39.000000 m6anet-2.1.0/docs/source/training.rst
+drwxrwxr-x   0 christopherhendra  (1003) christopherhendra  (1003)        0 2023-07-23 15:18:13.064598 m6anet-2.1.0/figures/
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)   431770 2022-01-14 07:36:33.000000 m6anet-2.1.0/figures/m6anet_logo.png
+drwxrwxr-x   0 christopherhendra  (1003) christopherhendra  (1003)        0 2023-07-23 15:18:13.064598 m6anet-2.1.0/m6anet/
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)      946 2023-07-23 15:08:29.000000 m6anet-2.1.0/m6anet/__init__.py
+drwxrwxr-x   0 christopherhendra  (1003) christopherhendra  (1003)        0 2023-07-23 15:18:13.064598 m6anet-2.1.0/m6anet/deprecated/
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)        0 2023-02-24 09:45:39.000000 m6anet-2.1.0/m6anet/deprecated/__init__.py
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     1885 2023-02-24 09:45:39.000000 m6anet-2.1.0/m6anet/deprecated/compute_norm_factors.py
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     2865 2023-02-24 09:45:39.000000 m6anet-2.1.0/m6anet/deprecated/dataprep.py
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     4297 2023-02-24 09:45:39.000000 m6anet-2.1.0/m6anet/deprecated/inference.py
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     5817 2023-02-24 09:45:39.000000 m6anet-2.1.0/m6anet/deprecated/train.py
+drwxrwxr-x   0 christopherhendra  (1003) christopherhendra  (1003)        0 2023-07-23 15:18:13.064598 m6anet-2.1.0/m6anet/model/
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)        0 2022-01-14 07:36:33.000000 m6anet-2.1.0/m6anet/model/__init__.py
+drwxrwxr-x   0 christopherhendra  (1003) christopherhendra  (1003)        0 2023-07-23 15:18:13.060598 m6anet-2.1.0/m6anet/model/configs/
+drwxrwxr-x   0 christopherhendra  (1003) christopherhendra  (1003)        0 2023-07-23 15:18:13.064598 m6anet-2.1.0/m6anet/model/configs/model_configs/
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)      578 2023-02-24 09:45:39.000000 m6anet-2.1.0/m6anet/model/configs/model_configs/m6anet.toml
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)      456 2023-07-23 15:08:29.000000 m6anet-2.1.0/m6anet/model/configs/model_configs/prod_pooling_signal.toml
+drwxrwxr-x   0 christopherhendra  (1003) christopherhendra  (1003)        0 2023-07-23 15:18:13.064598 m6anet-2.1.0/m6anet/model/configs/training_configs/
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)      473 2023-02-24 09:45:39.000000 m6anet-2.1.0/m6anet/model/configs/training_configs/m6anet_train_config.toml
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     7116 2023-02-24 09:45:39.000000 m6anet-2.1.0/m6anet/model/model.py
+drwxrwxr-x   0 christopherhendra  (1003) christopherhendra  (1003)        0 2023-07-23 15:18:13.068598 m6anet-2.1.0/m6anet/model/model_blocks/
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)      810 2022-11-12 09:00:05.000000 m6anet-2.1.0/m6anet/model/model_blocks/__init__.py
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     9672 2023-02-24 09:45:39.000000 m6anet-2.1.0/m6anet/model/model_blocks/blocks.py
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)    15720 2023-02-24 09:45:39.000000 m6anet-2.1.0/m6anet/model/model_blocks/pooling_blocks.py
+drwxrwxr-x   0 christopherhendra  (1003) christopherhendra  (1003)        0 2023-07-23 15:18:13.068598 m6anet-2.1.0/m6anet/model/model_states/
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)    36673 2023-07-23 15:08:29.000000 m6anet-2.1.0/m6anet/model/model_states/rna002_arabidopsis_virc.pt
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)    37083 2023-07-23 15:08:29.000000 m6anet-2.1.0/m6anet/model/model_states/rna002_hct116.pt
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)    36820 2023-07-23 15:08:29.000000 m6anet-2.1.0/m6anet/model/model_states/rna004_hek293t.pt
+drwxrwxr-x   0 christopherhendra  (1003) christopherhendra  (1003)        0 2023-07-23 15:18:13.068598 m6anet-2.1.0/m6anet/model/norm_factors/
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)    11612 2023-07-23 15:08:29.000000 m6anet-2.1.0/m6anet/model/norm_factors/rna002_arabidopsis_virc.joblib
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)   179264 2023-07-23 15:08:29.000000 m6anet-2.1.0/m6anet/model/norm_factors/rna002_hct116.joblib
+drwxrwxr-x   0 christopherhendra  (1003) christopherhendra  (1003)        0 2023-07-23 15:18:13.068598 m6anet-2.1.0/m6anet/scripts/
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)        0 2022-01-14 07:36:33.000000 m6anet-2.1.0/m6anet/scripts/__init__.py
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     1608 2023-02-24 09:45:39.000000 m6anet-2.1.0/m6anet/scripts/compute_norm_factors.py
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     1056 2023-02-24 09:45:39.000000 m6anet-2.1.0/m6anet/scripts/convert.py
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     2817 2023-02-24 09:45:39.000000 m6anet-2.1.0/m6anet/scripts/dataprep.py
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     4730 2023-07-23 15:08:29.000000 m6anet-2.1.0/m6anet/scripts/inference.py
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     5570 2023-02-24 09:45:39.000000 m6anet-2.1.0/m6anet/scripts/train.py
+drwxrwxr-x   0 christopherhendra  (1003) christopherhendra  (1003)        0 2023-07-23 15:18:13.068598 m6anet-2.1.0/m6anet/tests/
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     3791 2023-07-23 15:08:29.000000 m6anet-2.1.0/m6anet/tests/conftest.py
+drwxrwxr-x   0 christopherhendra  (1003) christopherhendra  (1003)        0 2023-07-23 15:18:13.072598 m6anet-2.1.0/m6anet/tests/data/
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)    75502 2023-02-24 09:45:39.000000 m6anet-2.1.0/m6anet/tests/data/data.indiv_proba.csv.gz
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     9801 2023-02-24 09:45:39.000000 m6anet-2.1.0/m6anet/tests/data/data.info
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)    11632 2023-02-24 09:45:39.000000 m6anet-2.1.0/m6anet/tests/data/data.info.labelled
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)   650620 2023-02-24 09:45:39.000000 m6anet-2.1.0/m6anet/tests/data/data.json
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     2552 2023-02-24 09:45:39.000000 m6anet-2.1.0/m6anet/tests/data/data.site_proba.csv.gz
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)   204244 2023-02-24 09:45:39.000000 m6anet-2.1.0/m6anet/tests/data/eventalign.index
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)  2091878 2023-02-24 09:45:39.000000 m6anet-2.1.0/m6anet/tests/data/eventalign.txt
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)      503 2023-07-23 15:08:29.000000 m6anet-2.1.0/m6anet/tests/data/sample_config.toml
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     2368 2023-07-23 15:08:29.000000 m6anet-2.1.0/m6anet/tests/test_dataprep.py
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     4551 2023-07-21 10:11:06.000000 m6anet-2.1.0/m6anet/tests/test_inference.py
+drwxrwxr-x   0 christopherhendra  (1003) christopherhendra  (1003)        0 2023-07-23 15:18:13.072598 m6anet-2.1.0/m6anet/utils/
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)        0 2022-01-14 07:36:33.000000 m6anet-2.1.0/m6anet/utils/__init__.py
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     5099 2023-02-24 09:45:39.000000 m6anet-2.1.0/m6anet/utils/builder.py
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     2098 2023-07-23 15:08:29.000000 m6anet-2.1.0/m6anet/utils/constants.py
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)    27787 2023-02-24 09:45:39.000000 m6anet-2.1.0/m6anet/utils/data_utils.py
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)    26928 2023-02-24 09:45:39.000000 m6anet-2.1.0/m6anet/utils/dataprep_utils.py
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     3281 2023-02-24 09:45:39.000000 m6anet-2.1.0/m6anet/utils/helper.py
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     7722 2023-02-24 09:45:39.000000 m6anet-2.1.0/m6anet/utils/inference_utils.py
+drwxrwxr-x   0 christopherhendra  (1003) christopherhendra  (1003)        0 2023-07-23 15:18:13.072598 m6anet-2.1.0/m6anet/utils/loss_functions/
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)        0 2023-02-24 09:45:39.000000 m6anet-2.1.0/m6anet/utils/loss_functions/__init__.py
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     1473 2023-02-24 09:45:39.000000 m6anet-2.1.0/m6anet/utils/loss_functions/loss_functions.py
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     8833 2023-02-24 09:45:39.000000 m6anet-2.1.0/m6anet/utils/norm_utils.py
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)    11172 2023-02-24 09:45:39.000000 m6anet-2.1.0/m6anet/utils/sampler_utils.py
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)    11905 2023-02-24 09:45:39.000000 m6anet-2.1.0/m6anet/utils/training_utils.py
+drwxrwxr-x   0 christopherhendra  (1003) christopherhendra  (1003)        0 2023-07-23 15:18:13.064598 m6anet-2.1.0/m6anet.egg-info/
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)    18340 2023-07-23 15:18:13.000000 m6anet-2.1.0/m6anet.egg-info/PKG-INFO
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     2493 2023-07-23 15:18:13.000000 m6anet-2.1.0/m6anet.egg-info/SOURCES.txt
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)        1 2023-07-23 15:18:13.000000 m6anet-2.1.0/m6anet.egg-info/dependency_links.txt
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)      263 2023-07-23 15:18:13.000000 m6anet-2.1.0/m6anet.egg-info/entry_points.txt
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)      222 2023-07-23 15:18:13.000000 m6anet-2.1.0/m6anet.egg-info/requires.txt
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)        7 2023-07-23 15:18:13.000000 m6anet-2.1.0/m6anet.egg-info/top_level.txt
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)       38 2023-07-23 15:18:13.072598 m6anet-2.1.0/setup.cfg
+-rw-rw-r--   0 christopherhendra  (1003) christopherhendra  (1003)     2681 2023-07-23 15:08:29.000000 m6anet-2.1.0/setup.py
```

### filetype from file(1)

```diff
@@ -1 +1 @@
-POSIX tar archive (GNU)
+POSIX tar archive
```

### Comparing `m6anet-2.0.2/LICENSE` & `m6anet-2.1.0/LICENSE`

 * *Files identical despite different names*

### Comparing `m6anet-2.0.2/m6anet/__init__.py` & `m6anet-2.1.0/m6anet/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from argparse import ArgumentDefaultsHelpFormatter, ArgumentParser
 from m6anet.scripts import dataprep, inference, train, \
         compute_norm_factors, convert
 
 
 modules = ['dataprep', 'inference', 'train', 'compute_norm_factors', 'convert']
 
-__version__ = "2.0.2"
+__version__ = "2.1.0"
 
 
 def main():
     parser = ArgumentParser(prog='m6anet',
                             formatter_class=ArgumentDefaultsHelpFormatter)
 
     parser.add_argument('-v', '--version', action='version',
```

### Comparing `m6anet-2.0.2/m6anet/deprecated/compute_norm_factors.py` & `m6anet-2.1.0/m6anet/deprecated/compute_norm_factors.py`

 * *Files identical despite different names*

### Comparing `m6anet-2.0.2/m6anet/deprecated/dataprep.py` & `m6anet-2.1.0/m6anet/deprecated/dataprep.py`

 * *Files identical despite different names*

### Comparing `m6anet-2.0.2/m6anet/deprecated/inference.py` & `m6anet-2.1.0/m6anet/deprecated/inference.py`

 * *Files identical despite different names*

### Comparing `m6anet-2.0.2/m6anet/deprecated/train.py` & `m6anet-2.1.0/m6anet/deprecated/train.py`

 * *Files identical despite different names*

### Comparing `m6anet-2.0.2/m6anet/model/configs/model_configs/m6anet.toml` & `m6anet-2.1.0/m6anet/model/configs/model_configs/m6anet.toml`

 * *Files identical despite different names*

### Comparing `m6anet-2.0.2/m6anet/model/model.py` & `m6anet-2.1.0/m6anet/model/model.py`

 * *Files identical despite different names*

### Comparing `m6anet-2.0.2/m6anet/model/model_blocks/__init__.py` & `m6anet-2.1.0/m6anet/model/model_blocks/__init__.py`

 * *Files identical despite different names*

### Comparing `m6anet-2.0.2/m6anet/model/model_blocks/blocks.py` & `m6anet-2.1.0/m6anet/model/model_blocks/blocks.py`

 * *Files identical despite different names*

### Comparing `m6anet-2.0.2/m6anet/model/model_blocks/pooling_blocks.py` & `m6anet-2.1.0/m6anet/model/model_blocks/pooling_blocks.py`

 * *Files identical despite different names*

### Comparing `m6anet-2.0.2/m6anet/model/model_states/human_hct116.pt` & `m6anet-2.1.0/m6anet/model/model_states/rna002_hct116.pt`

 * *Files identical despite different names*

### Comparing `m6anet-2.0.2/m6anet/model/norm_factors/norm_factors_hct116.joblib` & `m6anet-2.1.0/m6anet/model/norm_factors/rna002_hct116.joblib`

 * *Files identical despite different names*

### Comparing `m6anet-2.0.2/m6anet/scripts/compute_norm_factors.py` & `m6anet-2.1.0/m6anet/scripts/compute_norm_factors.py`

 * *Files identical despite different names*

### Comparing `m6anet-2.0.2/m6anet/scripts/convert.py` & `m6anet-2.1.0/m6anet/scripts/convert.py`

 * *Files identical despite different names*

### Comparing `m6anet-2.0.2/m6anet/scripts/dataprep.py` & `m6anet-2.1.0/m6anet/scripts/dataprep.py`

 * *Files identical despite different names*

### Comparing `m6anet-2.0.2/m6anet/scripts/inference.py` & `m6anet-2.1.0/m6anet/scripts/inference.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,17 +1,21 @@
 import os
 import torch
 import toml
 import pkg_resources
+import pathlib
 import numpy as np
+import warnings
 from argparse import ArgumentParser
 from argparse import ArgumentDefaultsHelpFormatter
 from ..model.model import MILModel
-from ..utils.constants import DEFAULT_MODEL_CONFIG, DEFAULT_MODEL_WEIGHTS,\
-    DEFAULT_NORM_PATH, DEFAULT_MIN_READS, DEFAULT_READ_THRESHOLD
+from ..utils.constants import DEFAULT_MODEL_CONFIG,\
+    DEFAULT_MIN_READS, DEFAULT_READ_THRESHOLD,\
+    DEFAULT_NORM_PATH, PRETRAINED_CONFIGS,\
+    DEFAULT_PRETRAINED_MODEL, DEFAULT_PRETRAINED_MODELS
 from ..utils.data_utils import NanopolishDS, NanopolishReplicateDS, inference_collate
 from ..utils.inference_utils import run_inference
 from torch.utils.data import DataLoader
 
 
 def argparser():
     parser = ArgumentParser(
@@ -23,21 +27,23 @@
                         help='directories containing data.info and data.json.',
                         required=True)
     parser.add_argument("--out_dir",
                         help='directory to output inference results.',
                         required=True)
 
     # Optional arguments
-
+    parser.add_argument("--pretrained_model",
+                        help="pre-trained model available at m6anet. Options include {}.".format(DEFAULT_PRETRAINED_MODELS),
+                        default=DEFAULT_PRETRAINED_MODEL, type=str)
     parser.add_argument("--model_config",
                         help='path to model config file.',
                         default=DEFAULT_MODEL_CONFIG)
     parser.add_argument("--model_state_dict",
                         help='path to model weights.',
-                        default=DEFAULT_MODEL_WEIGHTS)
+                        default=None)
     parser.add_argument("--norm_path",
                         help='path to normalization factors file',
                         default=DEFAULT_NORM_PATH)
     parser.add_argument("--batch_size",
                         help='batch size for inference.',
                         default=16, type=int)
     parser.add_argument("--save_per_batch",
@@ -52,34 +58,42 @@
     parser.add_argument("--device",
                         help='device to perform inference with.',
                         default='cpu', type=str)
     parser.add_argument("--seed",
                         help='random seed for sampling.',
                         default=0, type=int)
     parser.add_argument("--read_proba_threshold",
-                        help='default probability threshold for a read to be considered modified',
+                        help='default probability threshold for a read to be considered modified.',
                         default=DEFAULT_READ_THRESHOLD, type=float)
     return parser
 
 
 def main(args):
 
     input_dir = args.input_dir
-    out_dir = args.out_dir
+
+    if args.model_state_dict is not None:
+        warnings.warn("--model_state_dict is specified, overwriting default model weights")
+    else:
+        if args.pretrained_model not in DEFAULT_PRETRAINED_MODELS:
+            raise ValueError("Invalid pretrained model {}, must be one of {}".format(args.pretrained_model, DEFAULT_PRETRAINED_MODELS))
+
+        args.model_state_dict = PRETRAINED_CONFIGS[args.pretrained_model][0]
+        args.read_proba_threshold = PRETRAINED_CONFIGS[args.pretrained_model][1]
+        args.norm_path = PRETRAINED_CONFIGS[args.pretrained_model][2]
 
     torch.manual_seed(args.seed)
     torch.cuda.manual_seed_all(args.seed)
     np.random.seed(args.seed)
 
     model = MILModel(toml.load(args.model_config)).to(args.device)
     model.load_state_dict(torch.load(args.model_state_dict,
                                      map_location=torch.device(args.device)))
 
-    if not os.path.exists(out_dir):
-        os.makedirs(out_dir)
+    pathlib.Path(args.out_dir).mkdir(parents=True, exist_ok=True)
 
     with open(os.path.join(args.out_dir, "data.site_proba.csv"),'w', encoding='utf-8') as f:
         f.write('transcript_id,transcript_position,n_reads,probability_modified,kmer,mod_ratio\n')
     with open(os.path.join(args.out_dir, "data.indiv_proba.csv"), 'w', encoding='utf-8') as g:
         g.write('transcript_id,transcript_position,read_index,probability_modified\n')
 
     if len(input_dir) == 1:
```

### Comparing `m6anet-2.0.2/m6anet/scripts/train.py` & `m6anet-2.1.0/m6anet/scripts/train.py`

 * *Files identical despite different names*

### Comparing `m6anet-2.0.2/m6anet/utils/builder.py` & `m6anet-2.1.0/m6anet/utils/builder.py`

 * *Files identical despite different names*

### Comparing `m6anet-2.0.2/m6anet/utils/data_utils.py` & `m6anet-2.1.0/m6anet/utils/data_utils.py`

 * *Files identical despite different names*

### Comparing `m6anet-2.0.2/m6anet/utils/dataprep_utils.py` & `m6anet-2.1.0/m6anet/utils/dataprep_utils.py`

 * *Files identical despite different names*

### Comparing `m6anet-2.0.2/m6anet/utils/helper.py` & `m6anet-2.1.0/m6anet/utils/helper.py`

 * *Files identical despite different names*

### Comparing `m6anet-2.0.2/m6anet/utils/inference_utils.py` & `m6anet-2.1.0/m6anet/utils/inference_utils.py`

 * *Files identical despite different names*

### Comparing `m6anet-2.0.2/m6anet/utils/loss_functions/loss_functions.py` & `m6anet-2.1.0/m6anet/utils/loss_functions/loss_functions.py`

 * *Files identical despite different names*

### Comparing `m6anet-2.0.2/m6anet/utils/norm_utils.py` & `m6anet-2.1.0/m6anet/utils/norm_utils.py`

 * *Files identical despite different names*

### Comparing `m6anet-2.0.2/m6anet/utils/sampler_utils.py` & `m6anet-2.1.0/m6anet/utils/sampler_utils.py`

 * *Files identical despite different names*

### Comparing `m6anet-2.0.2/m6anet/utils/training_utils.py` & `m6anet-2.1.0/m6anet/utils/training_utils.py`

 * *Files identical despite different names*

