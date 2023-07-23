# Comparing `tmp/normflows-1.7.1.tar.gz` & `tmp/normflows-1.7.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/normflows-1.7.1.tar", last modified: Mon Jun 26 13:01:32 2023, max compression
+gzip compressed data, was "dist/normflows-1.7.2.tar", last modified: Sun Jul 23 09:32:59 2023, max compression
```

## Comparing `normflows-1.7.1.tar` & `normflows-1.7.2.tar`

### file list

```diff
@@ -1,90 +1,90 @@
-drwxrwxr-x   0 vstimper  (1000) vstimper  (1000)        0 2023-06-26 13:01:32.000000 normflows-1.7.1/
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1072 2021-11-22 13:57:32.000000 normflows-1.7.1/LICENSE
--rwxrwxr-x   0 vstimper  (1000) vstimper  (1000)       42 2021-11-22 13:57:32.000000 normflows-1.7.1/MANIFEST.in
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)    15920 2023-06-26 13:01:32.000000 normflows-1.7.1/PKG-INFO
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)    15331 2023-06-26 12:57:08.000000 normflows-1.7.1/README.md
-drwxrwxr-x   0 vstimper  (1000) vstimper  (1000)        0 2023-06-26 13:01:32.000000 normflows-1.7.1/normflows/
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)      253 2023-06-26 12:41:09.000000 normflows-1.7.1/normflows/__init__.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)    16860 2023-06-06 13:57:44.000000 normflows-1.7.1/normflows/core.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     7805 2023-06-06 13:57:44.000000 normflows-1.7.1/normflows/core_test.py
-drwxrwxr-x   0 vstimper  (1000) vstimper  (1000)        0 2023-06-26 13:01:32.000000 normflows-1.7.1/normflows/distributions/
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)      699 2023-05-31 15:25:11.000000 normflows-1.7.1/normflows/distributions/__init__.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)    22844 2023-05-30 15:55:17.000000 normflows-1.7.1/normflows/distributions/base.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     4884 2023-05-30 15:55:17.000000 normflows-1.7.1/normflows/distributions/base_test.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     2699 2023-01-20 17:41:25.000000 normflows-1.7.1/normflows/distributions/decoder.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1589 2023-01-22 11:55:37.000000 normflows-1.7.1/normflows/distributions/decoder_test.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1756 2023-01-22 11:55:37.000000 normflows-1.7.1/normflows/distributions/distribution_test.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     5745 2023-01-22 11:55:37.000000 normflows-1.7.1/normflows/distributions/encoder.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     3493 2023-01-22 11:55:37.000000 normflows-1.7.1/normflows/distributions/encoder_test.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)      663 2022-11-09 20:18:25.000000 normflows-1.7.1/normflows/distributions/linear_interpolation.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     2176 2022-11-09 20:18:25.000000 normflows-1.7.1/normflows/distributions/mh_proposal.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     9434 2023-01-23 18:21:11.000000 normflows-1.7.1/normflows/distributions/prior.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1651 2023-01-22 11:55:37.000000 normflows-1.7.1/normflows/distributions/prior_test.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     5694 2023-05-31 15:25:11.000000 normflows-1.7.1/normflows/distributions/target.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1334 2023-05-31 15:25:11.000000 normflows-1.7.1/normflows/distributions/target_test.py
-drwxrwxr-x   0 vstimper  (1000) vstimper  (1000)        0 2023-06-26 13:01:32.000000 normflows-1.7.1/normflows/flows/
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)      913 2022-07-26 14:04:52.000000 normflows-1.7.1/normflows/flows/__init__.py
-drwxrwxr-x   0 vstimper  (1000) vstimper  (1000)        0 2023-06-26 13:01:32.000000 normflows-1.7.1/normflows/flows/affine/
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)      218 2022-07-26 14:04:52.000000 normflows-1.7.1/normflows/flows/affine/__init__.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     4158 2022-11-09 20:18:25.000000 normflows-1.7.1/normflows/flows/affine/autoregressive.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)      974 2022-12-21 10:20:49.000000 normflows-1.7.1/normflows/flows/affine/autoregressive_test.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     9923 2023-01-22 11:55:37.000000 normflows-1.7.1/normflows/flows/affine/coupling.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1662 2023-01-22 11:55:37.000000 normflows-1.7.1/normflows/flows/affine/coupling_test.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     3330 2022-12-21 10:20:49.000000 normflows-1.7.1/normflows/flows/affine/glow.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1264 2022-12-21 10:20:49.000000 normflows-1.7.1/normflows/flows/affine/glow_test.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1924 2022-12-21 10:20:49.000000 normflows-1.7.1/normflows/flows/base.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1267 2023-01-22 11:55:37.000000 normflows-1.7.1/normflows/flows/base_test.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1325 2022-12-21 10:20:49.000000 normflows-1.7.1/normflows/flows/flow_test.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)    18397 2023-01-20 17:41:25.000000 normflows-1.7.1/normflows/flows/mixing.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1360 2023-01-20 17:41:25.000000 normflows-1.7.1/normflows/flows/mixing_test.py
-drwxrwxr-x   0 vstimper  (1000) vstimper  (1000)        0 2023-06-26 13:01:32.000000 normflows-1.7.1/normflows/flows/neural_spline/
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)      252 2022-07-26 14:04:52.000000 normflows-1.7.1/normflows/flows/neural_spline/__init__.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     4849 2022-12-21 10:20:49.000000 normflows-1.7.1/normflows/flows/neural_spline/autoregressive.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)      778 2022-12-21 10:20:49.000000 normflows-1.7.1/normflows/flows/neural_spline/autoregressive_test.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)    13084 2022-12-21 10:20:49.000000 normflows-1.7.1/normflows/flows/neural_spline/coupling.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1961 2022-12-21 10:20:49.000000 normflows-1.7.1/normflows/flows/neural_spline/coupling_test.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)    10166 2022-12-21 10:20:49.000000 normflows-1.7.1/normflows/flows/neural_spline/wrapper.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1861 2022-12-21 10:20:49.000000 normflows-1.7.1/normflows/flows/neural_spline/wrapper_test.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     2303 2022-11-09 20:18:25.000000 normflows-1.7.1/normflows/flows/normalization.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     2047 2022-11-09 20:18:25.000000 normflows-1.7.1/normflows/flows/periodic.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1332 2023-01-20 17:41:25.000000 normflows-1.7.1/normflows/flows/periodic_test.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     2878 2022-12-21 10:20:49.000000 normflows-1.7.1/normflows/flows/planar.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)      722 2023-01-20 17:41:25.000000 normflows-1.7.1/normflows/flows/planar_test.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1491 2022-12-21 10:20:49.000000 normflows-1.7.1/normflows/flows/radial.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)      506 2023-01-20 17:41:25.000000 normflows-1.7.1/normflows/flows/radial_test.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     4047 2022-11-09 20:18:25.000000 normflows-1.7.1/normflows/flows/reshape.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)    14772 2023-01-20 17:37:19.000000 normflows-1.7.1/normflows/flows/residual.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     2739 2023-01-23 14:38:51.000000 normflows-1.7.1/normflows/flows/residual_test.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     4278 2023-01-20 17:41:25.000000 normflows-1.7.1/normflows/flows/stochastic.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1321 2023-01-20 17:41:25.000000 normflows-1.7.1/normflows/flows/stochastic_test.py
-drwxrwxr-x   0 vstimper  (1000) vstimper  (1000)        0 2023-06-26 13:01:32.000000 normflows-1.7.1/normflows/nets/
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)      212 2022-07-26 14:04:52.000000 normflows-1.7.1/normflows/nets/__init__.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     2028 2022-12-21 10:20:49.000000 normflows-1.7.1/normflows/nets/cnn.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)    25793 2022-12-21 10:20:49.000000 normflows-1.7.1/normflows/nets/lipschitz.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     9712 2022-11-09 20:18:25.000000 normflows-1.7.1/normflows/nets/made.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     4741 2022-12-21 10:20:49.000000 normflows-1.7.1/normflows/nets/made_test.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     2284 2022-12-21 10:20:49.000000 normflows-1.7.1/normflows/nets/mlp.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     6999 2022-07-26 14:04:52.000000 normflows-1.7.1/normflows/nets/resnet.py
-drwxrwxr-x   0 vstimper  (1000) vstimper  (1000)        0 2023-06-26 13:01:32.000000 normflows-1.7.1/normflows/sampling/
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)       23 2022-07-26 14:04:52.000000 normflows-1.7.1/normflows/sampling/__init__.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1999 2022-11-09 20:18:25.000000 normflows-1.7.1/normflows/sampling/hais.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1982 2023-01-22 11:55:37.000000 normflows-1.7.1/normflows/transforms.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)      656 2023-01-22 11:55:37.000000 normflows-1.7.1/normflows/transforms_test.py
-drwxrwxr-x   0 vstimper  (1000) vstimper  (1000)        0 2023-06-26 13:01:32.000000 normflows-1.7.1/normflows/utils/
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)      262 2022-07-26 14:04:52.000000 normflows-1.7.1/normflows/utils/__init__.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     2046 2022-11-09 20:18:25.000000 normflows-1.7.1/normflows/utils/eval.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1660 2022-11-09 20:18:25.000000 normflows-1.7.1/normflows/utils/masks.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     5660 2022-12-21 10:20:49.000000 normflows-1.7.1/normflows/utils/nn.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)      852 2022-11-09 20:18:25.000000 normflows-1.7.1/normflows/utils/optim.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1168 2022-11-09 20:18:25.000000 normflows-1.7.1/normflows/utils/preprocessing.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     7744 2022-07-26 14:04:52.000000 normflows-1.7.1/normflows/utils/splines.py
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     2318 2023-01-20 17:41:25.000000 normflows-1.7.1/normflows/utils/splines_test.py
-drwxrwxr-x   0 vstimper  (1000) vstimper  (1000)        0 2023-06-26 13:01:32.000000 normflows-1.7.1/normflows.egg-info/
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)    15920 2023-06-26 13:01:32.000000 normflows-1.7.1/normflows.egg-info/PKG-INFO
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     2436 2023-06-26 13:01:32.000000 normflows-1.7.1/normflows.egg-info/SOURCES.txt
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)        1 2023-06-26 13:01:32.000000 normflows-1.7.1/normflows.egg-info/dependency_links.txt
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)       63 2023-06-26 13:01:32.000000 normflows-1.7.1/normflows.egg-info/requires.txt
--rw-rw-r--   0 vstimper  (1000) vstimper  (1000)       10 2023-06-26 13:01:32.000000 normflows-1.7.1/normflows.egg-info/top_level.txt
--rwxrwxr-x   0 vstimper  (1000) vstimper  (1000)       11 2022-07-26 12:32:34.000000 normflows-1.7.1/requirements.txt
--rwxrwxr-x   0 vstimper  (1000) vstimper  (1000)      108 2023-06-26 13:01:32.000000 normflows-1.7.1/setup.cfg
--rwxrwxr-x   0 vstimper  (1000) vstimper  (1000)     1368 2023-06-26 12:41:09.000000 normflows-1.7.1/setup.py
+drwxrwxr-x   0 vstimper  (1000) vstimper  (1000)        0 2023-07-23 09:32:59.000000 normflows-1.7.2/
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1072 2021-11-22 13:57:32.000000 normflows-1.7.2/LICENSE
+-rwxrwxr-x   0 vstimper  (1000) vstimper  (1000)       42 2021-11-22 13:57:32.000000 normflows-1.7.2/MANIFEST.in
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)    15919 2023-07-23 09:32:59.000000 normflows-1.7.2/PKG-INFO
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)    15330 2023-07-23 09:31:55.000000 normflows-1.7.2/README.md
+drwxrwxr-x   0 vstimper  (1000) vstimper  (1000)        0 2023-07-23 09:32:59.000000 normflows-1.7.2/normflows/
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)      272 2023-07-23 09:31:55.000000 normflows-1.7.2/normflows/__init__.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)    22316 2023-07-14 09:23:29.000000 normflows-1.7.2/normflows/core.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)    10593 2023-07-14 09:23:29.000000 normflows-1.7.2/normflows/core_test.py
+drwxrwxr-x   0 vstimper  (1000) vstimper  (1000)        0 2023-07-23 09:32:59.000000 normflows-1.7.2/normflows/distributions/
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)      820 2023-07-14 09:23:29.000000 normflows-1.7.2/normflows/distributions/__init__.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)    25027 2023-07-14 09:23:29.000000 normflows-1.7.2/normflows/distributions/base.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     5823 2023-07-14 09:23:29.000000 normflows-1.7.2/normflows/distributions/base_test.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     2699 2023-01-20 17:41:25.000000 normflows-1.7.2/normflows/distributions/decoder.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1589 2023-01-22 11:55:37.000000 normflows-1.7.2/normflows/distributions/decoder_test.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1756 2023-01-22 11:55:37.000000 normflows-1.7.2/normflows/distributions/distribution_test.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     5745 2023-01-22 11:55:37.000000 normflows-1.7.2/normflows/distributions/encoder.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     3493 2023-01-22 11:55:37.000000 normflows-1.7.2/normflows/distributions/encoder_test.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)      663 2022-11-09 20:18:25.000000 normflows-1.7.2/normflows/distributions/linear_interpolation.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     2176 2022-11-09 20:18:25.000000 normflows-1.7.2/normflows/distributions/mh_proposal.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     9434 2023-01-23 18:21:11.000000 normflows-1.7.2/normflows/distributions/prior.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1651 2023-01-22 11:55:37.000000 normflows-1.7.2/normflows/distributions/prior_test.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     6578 2023-07-14 09:23:29.000000 normflows-1.7.2/normflows/distributions/target.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1980 2023-07-14 09:23:29.000000 normflows-1.7.2/normflows/distributions/target_test.py
+drwxrwxr-x   0 vstimper  (1000) vstimper  (1000)        0 2023-07-23 09:32:59.000000 normflows-1.7.2/normflows/flows/
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1054 2023-07-14 09:23:29.000000 normflows-1.7.2/normflows/flows/__init__.py
+drwxrwxr-x   0 vstimper  (1000) vstimper  (1000)        0 2023-07-23 09:32:59.000000 normflows-1.7.2/normflows/flows/affine/
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)      281 2023-07-14 09:23:29.000000 normflows-1.7.2/normflows/flows/affine/__init__.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     4982 2023-07-14 09:23:29.000000 normflows-1.7.2/normflows/flows/affine/autoregressive.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)      974 2022-12-21 10:20:49.000000 normflows-1.7.2/normflows/flows/affine/autoregressive_test.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     9897 2023-07-18 21:22:24.000000 normflows-1.7.2/normflows/flows/affine/coupling.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1662 2023-01-22 11:55:37.000000 normflows-1.7.2/normflows/flows/affine/coupling_test.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     3330 2022-12-21 10:20:49.000000 normflows-1.7.2/normflows/flows/affine/glow.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1264 2022-12-21 10:20:49.000000 normflows-1.7.2/normflows/flows/affine/glow_test.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1924 2022-12-21 10:20:49.000000 normflows-1.7.2/normflows/flows/base.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1267 2023-01-22 11:55:37.000000 normflows-1.7.2/normflows/flows/base_test.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1325 2022-12-21 10:20:49.000000 normflows-1.7.2/normflows/flows/flow_test.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)    18549 2023-07-14 09:23:29.000000 normflows-1.7.2/normflows/flows/mixing.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1360 2023-01-20 17:41:25.000000 normflows-1.7.2/normflows/flows/mixing_test.py
+drwxrwxr-x   0 vstimper  (1000) vstimper  (1000)        0 2023-07-23 09:32:59.000000 normflows-1.7.2/normflows/flows/neural_spline/
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)      265 2023-07-14 09:23:29.000000 normflows-1.7.2/normflows/flows/neural_spline/__init__.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     4849 2022-12-21 10:20:49.000000 normflows-1.7.2/normflows/flows/neural_spline/autoregressive.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)      778 2022-12-21 10:20:49.000000 normflows-1.7.2/normflows/flows/neural_spline/autoregressive_test.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)    13084 2022-12-21 10:20:49.000000 normflows-1.7.2/normflows/flows/neural_spline/coupling.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1961 2022-12-21 10:20:49.000000 normflows-1.7.2/normflows/flows/neural_spline/coupling_test.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)    10549 2023-07-14 09:23:29.000000 normflows-1.7.2/normflows/flows/neural_spline/wrapper.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1861 2022-12-21 10:20:49.000000 normflows-1.7.2/normflows/flows/neural_spline/wrapper_test.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     2303 2022-11-09 20:18:25.000000 normflows-1.7.2/normflows/flows/normalization.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     2047 2022-11-09 20:18:25.000000 normflows-1.7.2/normflows/flows/periodic.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1332 2023-01-20 17:41:25.000000 normflows-1.7.2/normflows/flows/periodic_test.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     2878 2022-12-21 10:20:49.000000 normflows-1.7.2/normflows/flows/planar.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)      722 2023-01-20 17:41:25.000000 normflows-1.7.2/normflows/flows/planar_test.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1491 2022-12-21 10:20:49.000000 normflows-1.7.2/normflows/flows/radial.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)      506 2023-01-20 17:41:25.000000 normflows-1.7.2/normflows/flows/radial_test.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     4047 2022-11-09 20:18:25.000000 normflows-1.7.2/normflows/flows/reshape.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)    14772 2023-01-20 17:37:19.000000 normflows-1.7.2/normflows/flows/residual.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     2739 2023-01-23 14:38:51.000000 normflows-1.7.2/normflows/flows/residual_test.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     4278 2023-01-20 17:41:25.000000 normflows-1.7.2/normflows/flows/stochastic.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1321 2023-01-20 17:41:25.000000 normflows-1.7.2/normflows/flows/stochastic_test.py
+drwxrwxr-x   0 vstimper  (1000) vstimper  (1000)        0 2023-07-23 09:32:59.000000 normflows-1.7.2/normflows/nets/
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)      286 2023-07-14 09:23:29.000000 normflows-1.7.2/normflows/nets/__init__.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     2028 2022-12-21 10:20:49.000000 normflows-1.7.2/normflows/nets/cnn.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)    25793 2022-12-21 10:20:49.000000 normflows-1.7.2/normflows/nets/lipschitz.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     9713 2023-07-18 21:22:24.000000 normflows-1.7.2/normflows/nets/made.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     4741 2022-12-21 10:20:49.000000 normflows-1.7.2/normflows/nets/made_test.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     2284 2022-12-21 10:20:49.000000 normflows-1.7.2/normflows/nets/mlp.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     6999 2022-07-26 14:04:52.000000 normflows-1.7.2/normflows/nets/resnet.py
+drwxrwxr-x   0 vstimper  (1000) vstimper  (1000)        0 2023-07-23 09:32:59.000000 normflows-1.7.2/normflows/sampling/
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)       42 2023-07-14 09:23:29.000000 normflows-1.7.2/normflows/sampling/__init__.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1999 2022-11-09 20:18:25.000000 normflows-1.7.2/normflows/sampling/hais.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1982 2023-01-22 11:55:37.000000 normflows-1.7.2/normflows/transforms.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)      656 2023-01-22 11:55:37.000000 normflows-1.7.2/normflows/transforms_test.py
+drwxrwxr-x   0 vstimper  (1000) vstimper  (1000)        0 2023-07-23 09:32:59.000000 normflows-1.7.2/normflows/utils/
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)      332 2023-07-14 09:23:29.000000 normflows-1.7.2/normflows/utils/__init__.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     2046 2022-11-09 20:18:25.000000 normflows-1.7.2/normflows/utils/eval.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1660 2022-11-09 20:18:25.000000 normflows-1.7.2/normflows/utils/masks.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     5660 2023-07-18 21:22:24.000000 normflows-1.7.2/normflows/utils/nn.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)      852 2022-11-09 20:18:25.000000 normflows-1.7.2/normflows/utils/optim.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     1168 2022-11-09 20:18:25.000000 normflows-1.7.2/normflows/utils/preprocessing.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     7744 2022-07-26 14:04:52.000000 normflows-1.7.2/normflows/utils/splines.py
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     2318 2023-01-20 17:41:25.000000 normflows-1.7.2/normflows/utils/splines_test.py
+drwxrwxr-x   0 vstimper  (1000) vstimper  (1000)        0 2023-07-23 09:32:59.000000 normflows-1.7.2/normflows.egg-info/
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)    15919 2023-07-23 09:32:59.000000 normflows-1.7.2/normflows.egg-info/PKG-INFO
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)     2436 2023-07-23 09:32:59.000000 normflows-1.7.2/normflows.egg-info/SOURCES.txt
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)        1 2023-07-23 09:32:59.000000 normflows-1.7.2/normflows.egg-info/dependency_links.txt
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)       63 2023-07-23 09:32:59.000000 normflows-1.7.2/normflows.egg-info/requires.txt
+-rw-rw-r--   0 vstimper  (1000) vstimper  (1000)       10 2023-07-23 09:32:59.000000 normflows-1.7.2/normflows.egg-info/top_level.txt
+-rwxrwxr-x   0 vstimper  (1000) vstimper  (1000)       11 2022-07-26 12:32:34.000000 normflows-1.7.2/requirements.txt
+-rwxrwxr-x   0 vstimper  (1000) vstimper  (1000)      108 2023-07-23 09:32:59.000000 normflows-1.7.2/setup.cfg
+-rwxrwxr-x   0 vstimper  (1000) vstimper  (1000)     1368 2023-07-23 09:31:55.000000 normflows-1.7.2/setup.py
```

### Comparing `normflows-1.7.1/LICENSE` & `normflows-1.7.2/LICENSE`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/PKG-INFO` & `normflows-1.7.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: normflows
-Version: 1.7.1
+Version: 1.7.2
 Summary: Pytorch implementation of normalizing flows
 Home-page: https://github.com/VincentStimper/normalizing-flows
 Author: Vincent Stimper
 Author-email: vincent.stimper@tuebingen.mpg.de
 License: MIT
 Download-URL: https://github.com/VincentStimper/normalizing-flows/archive/refs/heads/master.zip
 Platform: UNKNOWN
@@ -18,15 +18,15 @@
 # `normflows`: A PyTorch Package for Normalizing Flows
 
 [![documentation](https://github.com/VincentStimper/normalizing-flows/actions/workflows/mkdocs.yaml/badge.svg)](https://vincentstimper.github.io/normalizing-flows/)
 ![unit-tests](https://github.com/VincentStimper/normalizing-flows/actions/workflows/pytest.yaml/badge.svg)
 ![code coverage](https://raw.githubusercontent.com/VincentStimper/normalizing-flows/coverage-badge/coverage.svg?raw=true)
 [![License: MIT](https://img.shields.io/badge/Licence-MIT-b31b1b.svg)](https://opensource.org/licenses/MIT)
 [![DOI](https://joss.theoj.org/papers/10.21105/joss.05361/status.svg)](https://doi.org/10.21105/joss.05361)
-[![PyPI](https://img.shields.io/badge/PyPI-1.7.1-blue.svg)](https://pypi.org/project/normflows/)
+[![PyPI](https://img.shields.io/badge/PyPI-1.7.2-blue.svg)](https://pypi.org/project/normflows/)
 [![Downloads](https://static.pepy.tech/personalized-badge/normflows?period=total&units=international_system&left_color=grey&right_color=orange&left_text=Downloads)](https://pepy.tech/project/normflows)
 
 
 `normflows` is a PyTorch implementation of discrete normalizing flows. Many popular flow architectures are implemented,
 see the [list below](#implemented-flows). The package can be easily [installed via pip](#installation).
 The basic usage is described [here](#usage), and a [full documentation](https://vincentstimper.github.io/normalizing-flows/) 
 is available as well. A more detailed description of this package is given in our
@@ -151,15 +151,15 @@
 optimizer.step()
 ```
 
 ## Examples
 
 We provide several illustrative examples of how to use the package in the
 [`examples`](https://github.com/VincentStimper/normalizing-flows/blob/master/examples)
-directory. Amoung them are implementations of 
+directory. Among them are implementations of 
 [Glow](https://github.com/VincentStimper/normalizing-flows/blob/master/examples/glow.ipynb),
 a [VAE](https://github.com/VincentStimper/normalizing-flows/blob/master/examples/vae.py), and
 a [Residual Flow](https://github.com/VincentStimper/normalizing-flows/blob/master/examples/residual.ipynb). 
 More advanced experiments can be done with the scripts listed in the
 [repository about resampled base distributions](https://github.com/VincentStimper/resampled-base-flows),
 see its [`experiments`](https://github.com/VincentStimper/resampled-base-flows/tree/master/experiments)
 folder.
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: normflows Version: 1.7.1 Summary: Pytorch
+Metadata-Version: 2.1 Name: normflows Version: 1.7.2 Summary: Pytorch
 implementation of normalizing flows Home-page: https://github.com/
 VincentStimper/normalizing-flows Author: Vincent Stimper Author-email:
 vincent.stimper@tuebingen.mpg.de License: MIT Download-URL: https://github.com/
 VincentStimper/normalizing-flows/archive/refs/heads/master.zip Platform:
 UNKNOWN Classifier: Development Status :: 3 - Alpha Classifier: Intended
 Audience :: Developers Classifier: Programming Language :: Python :: 3
 Description-Content-Type: text/markdown Provides-Extra: docs License-File:
@@ -11,15 +11,15 @@
 workflows/mkdocs.yaml/badge.svg)](https://vincentstimper.github.io/normalizing-
 flows/) ![unit-tests](https://github.com/VincentStimper/normalizing-flows/
 actions/workflows/pytest.yaml/badge.svg) ![code coverage](https://
 raw.githubusercontent.com/VincentStimper/normalizing-flows/coverage-badge/
 coverage.svg?raw=true) [![License: MIT](https://img.shields.io/badge/Licence-
 MIT-b31b1b.svg)](https://opensource.org/licenses/MIT) [![DOI](https://
 joss.theoj.org/papers/10.21105/joss.05361/status.svg)](https://doi.org/
-10.21105/joss.05361) [![PyPI](https://img.shields.io/badge/PyPI-1.7.1-
+10.21105/joss.05361) [![PyPI](https://img.shields.io/badge/PyPI-1.7.2-
 blue.svg)](https://pypi.org/project/normflows/) [![Downloads](https://
 static.pepy.tech/personalized-badge/
 normflows?period=total&units=international_system&left_color=grey&right_color=orange&left_text=Downloads)]
 (https://pepy.tech/project/normflows) `normflows` is a PyTorch implementation
 of discrete normalizing flows. Many popular flow architectures are implemented,
 see the [list below](#implemented-flows). The package can be easily [installed
 via pip](#installation). The basic usage is described [here](#usage), and a
@@ -96,15 +96,15 @@
 target) ``` The loss can be computed with the methods of the model and
 minimized. ```python # When doing maximum likelihood learning, i.e. minimizing
 the forward KLD # with no target distribution given loss = model.forward_kld(x)
 # When minimizing the reverse KLD based on the given target distribution loss =
 model.reverse_kld(num_samples=512) # Optimization as usual loss.backward()
 optimizer.step() ``` ## Examples We provide several illustrative examples of
 how to use the package in the [`examples`](https://github.com/VincentStimper/
-normalizing-flows/blob/master/examples) directory. Amoung them are
+normalizing-flows/blob/master/examples) directory. Among them are
 implementations of [Glow](https://github.com/VincentStimper/normalizing-flows/
 blob/master/examples/glow.ipynb), a [VAE](https://github.com/VincentStimper/
 normalizing-flows/blob/master/examples/vae.py), and a [Residual Flow](https://
 github.com/VincentStimper/normalizing-flows/blob/master/examples/
 residual.ipynb). More advanced experiments can be done with the scripts listed
 in the [repository about resampled base distributions](https://github.com/
 VincentStimper/resampled-base-flows), see its [`experiments`](https://
```

### Comparing `normflows-1.7.1/README.md` & `normflows-1.7.2/README.md`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 # `normflows`: A PyTorch Package for Normalizing Flows
 
 [![documentation](https://github.com/VincentStimper/normalizing-flows/actions/workflows/mkdocs.yaml/badge.svg)](https://vincentstimper.github.io/normalizing-flows/)
 ![unit-tests](https://github.com/VincentStimper/normalizing-flows/actions/workflows/pytest.yaml/badge.svg)
 ![code coverage](https://raw.githubusercontent.com/VincentStimper/normalizing-flows/coverage-badge/coverage.svg?raw=true)
 [![License: MIT](https://img.shields.io/badge/Licence-MIT-b31b1b.svg)](https://opensource.org/licenses/MIT)
 [![DOI](https://joss.theoj.org/papers/10.21105/joss.05361/status.svg)](https://doi.org/10.21105/joss.05361)
-[![PyPI](https://img.shields.io/badge/PyPI-1.7.1-blue.svg)](https://pypi.org/project/normflows/)
+[![PyPI](https://img.shields.io/badge/PyPI-1.7.2-blue.svg)](https://pypi.org/project/normflows/)
 [![Downloads](https://static.pepy.tech/personalized-badge/normflows?period=total&units=international_system&left_color=grey&right_color=orange&left_text=Downloads)](https://pepy.tech/project/normflows)
 
 
 `normflows` is a PyTorch implementation of discrete normalizing flows. Many popular flow architectures are implemented,
 see the [list below](#implemented-flows). The package can be easily [installed via pip](#installation).
 The basic usage is described [here](#usage), and a [full documentation](https://vincentstimper.github.io/normalizing-flows/) 
 is available as well. A more detailed description of this package is given in our
@@ -134,15 +134,15 @@
 optimizer.step()
 ```
 
 ## Examples
 
 We provide several illustrative examples of how to use the package in the
 [`examples`](https://github.com/VincentStimper/normalizing-flows/blob/master/examples)
-directory. Amoung them are implementations of 
+directory. Among them are implementations of 
 [Glow](https://github.com/VincentStimper/normalizing-flows/blob/master/examples/glow.ipynb),
 a [VAE](https://github.com/VincentStimper/normalizing-flows/blob/master/examples/vae.py), and
 a [Residual Flow](https://github.com/VincentStimper/normalizing-flows/blob/master/examples/residual.ipynb). 
 More advanced experiments can be done with the scripts listed in the
 [repository about resampled base distributions](https://github.com/VincentStimper/resampled-base-flows),
 see its [`experiments`](https://github.com/VincentStimper/resampled-base-flows/tree/master/experiments)
 folder.
```

#### html2text {}

```diff
@@ -3,15 +3,15 @@
 badge.svg)](https://vincentstimper.github.io/normalizing-flows/) ![unit-tests]
 (https://github.com/VincentStimper/normalizing-flows/actions/workflows/
 pytest.yaml/badge.svg) ![code coverage](https://raw.githubusercontent.com/
 VincentStimper/normalizing-flows/coverage-badge/coverage.svg?raw=true) [!
 [License: MIT](https://img.shields.io/badge/Licence-MIT-b31b1b.svg)](https://
 opensource.org/licenses/MIT) [![DOI](https://joss.theoj.org/papers/10.21105/
 joss.05361/status.svg)](https://doi.org/10.21105/joss.05361) [![PyPI](https://
-img.shields.io/badge/PyPI-1.7.1-blue.svg)](https://pypi.org/project/normflows/
+img.shields.io/badge/PyPI-1.7.2-blue.svg)](https://pypi.org/project/normflows/
 ) [![Downloads](https://static.pepy.tech/personalized-badge/
 normflows?period=total&units=international_system&left_color=grey&right_color=orange&left_text=Downloads)]
 (https://pepy.tech/project/normflows) `normflows` is a PyTorch implementation
 of discrete normalizing flows. Many popular flow architectures are implemented,
 see the [list below](#implemented-flows). The package can be easily [installed
 via pip](#installation). The basic usage is described [here](#usage), and a
 [full documentation](https://vincentstimper.github.io/normalizing-flows/) is
@@ -87,15 +87,15 @@
 target) ``` The loss can be computed with the methods of the model and
 minimized. ```python # When doing maximum likelihood learning, i.e. minimizing
 the forward KLD # with no target distribution given loss = model.forward_kld(x)
 # When minimizing the reverse KLD based on the given target distribution loss =
 model.reverse_kld(num_samples=512) # Optimization as usual loss.backward()
 optimizer.step() ``` ## Examples We provide several illustrative examples of
 how to use the package in the [`examples`](https://github.com/VincentStimper/
-normalizing-flows/blob/master/examples) directory. Amoung them are
+normalizing-flows/blob/master/examples) directory. Among them are
 implementations of [Glow](https://github.com/VincentStimper/normalizing-flows/
 blob/master/examples/glow.ipynb), a [VAE](https://github.com/VincentStimper/
 normalizing-flows/blob/master/examples/vae.py), and a [Residual Flow](https://
 github.com/VincentStimper/normalizing-flows/blob/master/examples/
 residual.ipynb). More advanced experiments can be done with the scripts listed
 in the [repository about resampled base distributions](https://github.com/
 VincentStimper/resampled-base-flows), see its [`experiments`](https://
```

### Comparing `normflows-1.7.1/normflows/core.py` & `normflows-1.7.2/normflows/core.py`

 * *Files 17% similar despite different names*

```diff
@@ -209,17 +209,172 @@
 
         Args:
           path: Path including filename where to load model from
         """
         self.load_state_dict(torch.load(path))
 
 
+class ConditionalNormalizingFlow(NormalizingFlow):
+    """
+    Conditional normalizing flow model, providing condition,
+    which is also called context, to both the base distribution
+    and the flow layers
+    """
+    def forward(self, z, context=None):
+        """Transforms latent variable z to the flow variable x
+
+        Args:
+          z: Batch in the latent space
+          context: Batch of conditions/context
+
+        Returns:
+          Batch in the space of the target distribution
+        """
+        for flow in self.flows:
+            z, _ = flow(z, context=context)
+        return z
+
+    def forward_and_log_det(self, z, context=None):
+        """Transforms latent variable z to the flow variable x and
+        computes log determinant of the Jacobian
+
+        Args:
+          z: Batch in the latent space
+          context: Batch of conditions/context
+
+        Returns:
+          Batch in the space of the target distribution,
+          log determinant of the Jacobian
+        """
+        log_det = torch.zeros(len(z), device=z.device)
+        for flow in self.flows:
+            z, log_d = flow(z, context=context)
+            log_det += log_d
+        return z, log_det
+
+    def inverse(self, x, context=None):
+        """Transforms flow variable x to the latent variable z
+
+        Args:
+          x: Batch in the space of the target distribution
+          context: Batch of conditions/context
+
+        Returns:
+          Batch in the latent space
+        """
+        for i in range(len(self.flows) - 1, -1, -1):
+            x, _ = self.flows[i].inverse(x, context=context)
+        return x
+
+    def inverse_and_log_det(self, x, context=None):
+        """Transforms flow variable x to the latent variable z and
+        computes log determinant of the Jacobian
+
+        Args:
+          x: Batch in the space of the target distribution
+          context: Batch of conditions/context
+
+        Returns:
+          Batch in the latent space, log determinant of the
+          Jacobian
+        """
+        log_det = torch.zeros(len(x), device=x.device)
+        for i in range(len(self.flows) - 1, -1, -1):
+            x, log_d = self.flows[i].inverse(x, context=context)
+            log_det += log_d
+        return x, log_det
+
+    def sample(self, num_samples=1, context=None):
+        """Samples from flow-based approximate distribution
+
+        Args:
+          num_samples: Number of samples to draw
+          context: Batch of conditions/context
+
+        Returns:
+          Samples, log probability
+        """
+        z, log_q = self.q0(num_samples, context=context)
+        for flow in self.flows:
+            z, log_det = flow(z, context=context)
+            log_q -= log_det
+        return z, log_q
+
+    def log_prob(self, x, context=None):
+        """Get log probability for batch
+
+        Args:
+          x: Batch
+          context: Batch of conditions/context
+
+        Returns:
+          log probability
+        """
+        log_q = torch.zeros(len(x), dtype=x.dtype, device=x.device)
+        z = x
+        for i in range(len(self.flows) - 1, -1, -1):
+            z, log_det = self.flows[i].inverse(z, context=context)
+            log_q += log_det
+        log_q += self.q0.log_prob(z, context=context)
+        return log_q
+
+    def forward_kld(self, x, context=None):
+        """Estimates forward KL divergence, see [arXiv 1912.02762](https://arxiv.org/abs/1912.02762)
+
+        Args:
+          x: Batch sampled from target distribution
+          context: Batch of conditions/context
+
+        Returns:
+          Estimate of forward KL divergence averaged over batch
+        """
+        log_q = torch.zeros(len(x), device=x.device)
+        z = x
+        for i in range(len(self.flows) - 1, -1, -1):
+            z, log_det = self.flows[i].inverse(z, context=context)
+            log_q += log_det
+        log_q += self.q0.log_prob(z, context=context)
+        return -torch.mean(log_q)
+
+    def reverse_kld(self, num_samples=1, context=None, beta=1.0, score_fn=True):
+        """Estimates reverse KL divergence, see [arXiv 1912.02762](https://arxiv.org/abs/1912.02762)
+
+        Args:
+          num_samples: Number of samples to draw from base distribution
+          context: Batch of conditions/context
+          beta: Annealing parameter, see [arXiv 1505.05770](https://arxiv.org/abs/1505.05770)
+          score_fn: Flag whether to include score function in gradient, see [arXiv 1703.09194](https://arxiv.org/abs/1703.09194)
+
+        Returns:
+          Estimate of the reverse KL divergence averaged over latent samples
+        """
+        z, log_q_ = self.q0(num_samples, context=context)
+        log_q = torch.zeros_like(log_q_)
+        log_q += log_q_
+        for flow in self.flows:
+            z, log_det = flow(z, context=context)
+            log_q -= log_det
+        if not score_fn:
+            z_ = z
+            log_q = torch.zeros(len(z_), device=z_.device)
+            utils.set_requires_grad(self, False)
+            for i in range(len(self.flows) - 1, -1, -1):
+                z_, log_det = self.flows[i].inverse(z_, context=context)
+                log_q += log_det
+            log_q += self.q0.log_prob(z_, context=context)
+            utils.set_requires_grad(self, True)
+        log_p = self.p.log_prob(z, context=context)
+        return torch.mean(log_q) - beta * torch.mean(log_p)
+
+
 class ClassCondFlow(nn.Module):
     """
-    Class conditional normalizing Flow model
+    Class conditional normalizing Flow model, providing the
+    class to be conditioned on only to the base distribution,
+    as done e.g. in [Glow](https://arxiv.org/abs/1807.03039)
     """
 
     def __init__(self, q0, flows):
         """Constructor
 
         Args:
           q0: Base distribution
```

### Comparing `normflows-1.7.1/normflows/core_test.py` & `normflows-1.7.2/normflows/core_test.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,19 +1,22 @@
 import unittest
 import torch
 
 from torch.testing import assert_close
 from normflows import NormalizingFlow, ClassCondFlow, \
-    MultiscaleFlow, NormalizingFlowVAE
+    MultiscaleFlow, NormalizingFlowVAE, \
+    ConditionalNormalizingFlow
 from normflows.flows import MaskedAffineFlow, GlowBlock, \
-    Merge, Squeeze
+    Merge, Squeeze, MaskedAffineAutoregressive, \
+    AutoregressiveRationalQuadraticSpline
 from normflows.nets import MLP
 from normflows.distributions.base import DiagGaussian, \
     ClassCondDiagGaussian
-from normflows.distributions.target import CircularGaussianMixture
+from normflows.distributions.target import CircularGaussianMixture, \
+    ConditionalDiagGaussian
 from normflows.distributions.encoder import NNDiagGaussian
 from normflows.distributions.decoder import NNDiagGaussianDecoder
 
 
 class CoreTest(unittest.TestCase):
     def test_normalizing_flow(self):
         batch_size = 5
@@ -53,14 +56,68 @@
                 inputs_ = model.inverse(outputs)
                 assert_close(inputs_, inputs)
                 outputs, log_det = model.forward_and_log_det(inputs)
                 inputs_, log_det_ = model.inverse_and_log_det(outputs)
                 assert_close(inputs_, inputs)
                 assert_close(log_det, -log_det_)
 
+    def test_conditional_normalizing_flow(self):
+        batch_size = 5
+        latent_size = 2
+        context_size = latent_size * 2
+        n_layers = 2
+        for flow_layer_type in ['maf', 'auto_rqs']:
+            with self.subTest(n_layers=n_layers):
+                # Construct flow model
+                layers = []
+                for i in range(n_layers):
+                    if flow_layer_type == 'maf':
+                        layer = MaskedAffineAutoregressive(
+                            features=latent_size,
+                            hidden_features=32,
+                            context_features=context_size,
+                            num_blocks=2,
+                            use_residual_blocks=True,
+                            random_mask=False,
+                        )
+                    elif flow_layer_type == 'auto_rqs':
+                        layer = AutoregressiveRationalQuadraticSpline(
+                            num_input_channels=latent_size,
+                            num_blocks=2,
+                            num_hidden_channels=32,
+                            num_context_channels=context_size,
+                        )
+                    layers.append(layer)
+                base = DiagGaussian(latent_size)
+                target = ConditionalDiagGaussian()
+                model = ConditionalNormalizingFlow(base, layers, target)
+                # Test log prob and sampling
+                inputs = torch.randn((batch_size, latent_size))
+                context = torch.rand((batch_size, context_size)) + 0.5
+                log_q = model.log_prob(inputs, context)
+                assert log_q.shape == (batch_size,)
+                s, log_q = model.sample(batch_size, context)
+                assert log_q.shape == (batch_size,)
+                assert s.shape == (batch_size, latent_size)
+                # Test losses
+                loss = model.forward_kld(inputs, context)
+                assert loss.dim() == 0
+                loss = model.reverse_kld(batch_size, context)
+                assert loss.dim() == 0
+                loss = model.reverse_kld(batch_size, context, score_fn=False)
+                assert loss.dim() == 0
+                # Test forward and inverse
+                outputs = model.forward(inputs, context)
+                inputs_ = model.inverse(outputs, context)
+                assert_close(inputs_, inputs)
+                outputs, log_det = model.forward_and_log_det(inputs, context)
+                inputs_, log_det_ = model.inverse_and_log_det(outputs, context)
+                assert_close(inputs_, inputs)
+                assert_close(log_det, -log_det_)
+
     def test_cc_normalizing_flow(self):
         batch_size = 5
         latent_size = 2
         n_layers = 2
         n_classes = 3
 
         # Construct flow model
```

### Comparing `normflows-1.7.1/normflows/distributions/__init__.py` & `normflows-1.7.2/normflows/distributions/__init__.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,7 +1,17 @@
+from . import (
+    base,
+    decoder,
+    encoder,
+    linear_interpolation,
+    mh_proposal,
+    prior,
+    target,
+)
+
 from .base import (
     BaseDistribution,
     DiagGaussian,
     ClassCondDiagGaussian,
     GlowBase,
     AffineGaussian,
     GaussianMixture,
```

### Comparing `normflows-1.7.1/normflows/distributions/base.py` & `normflows-1.7.2/normflows/distributions/base.py`

 * *Files 10% similar despite different names*

```diff
@@ -55,14 +55,15 @@
     """
 
     def __init__(self, shape, trainable=True):
         """Constructor
 
         Args:
           shape: Tuple with shape of data, if int shape has one dimension
+          trainable: Flag whether to use trainable or fixed parameters
         """
         super().__init__()
         if isinstance(shape, int):
             shape = (shape,)
         if isinstance(shape, list):
             shape = tuple(shape)
         self.shape = shape
@@ -72,40 +73,92 @@
             self.loc = nn.Parameter(torch.zeros(1, *self.shape))
             self.log_scale = nn.Parameter(torch.zeros(1, *self.shape))
         else:
             self.register_buffer("loc", torch.zeros(1, *self.shape))
             self.register_buffer("log_scale", torch.zeros(1, *self.shape))
         self.temperature = None  # Temperature parameter for annealed sampling
 
-    def forward(self, num_samples=1):
+    def forward(self, num_samples=1, context=None):
         eps = torch.randn(
             (num_samples,) + self.shape, dtype=self.loc.dtype, device=self.loc.device
         )
         if self.temperature is None:
             log_scale = self.log_scale
         else:
             log_scale = self.log_scale + np.log(self.temperature)
         z = self.loc + torch.exp(log_scale) * eps
         log_p = -0.5 * self.d * np.log(2 * np.pi) - torch.sum(
             log_scale + 0.5 * torch.pow(eps, 2), list(range(1, self.n_dim + 1))
         )
         return z, log_p
 
-    def log_prob(self, z):
+    def log_prob(self, z, context=None):
         if self.temperature is None:
             log_scale = self.log_scale
         else:
             log_scale = self.log_scale + np.log(self.temperature)
         log_p = -0.5 * self.d * np.log(2 * np.pi) - torch.sum(
             log_scale + 0.5 * torch.pow((z - self.loc) / torch.exp(log_scale), 2),
             list(range(1, self.n_dim + 1)),
         )
         return log_p
 
 
+class ConditionalDiagGaussian(BaseDistribution):
+    """
+    Conditional multivariate Gaussian distribution with diagonal
+    covariance matrix, parameters are obtained by a context encoder,
+    context meaning the variable to condition on
+    """
+    def __init__(self, shape, context_encoder):
+        """Constructor
+
+        Args:
+          shape: Tuple with shape of data, if int shape has one dimension
+          context_encoder: Computes mean and log of the standard deviation
+          of the Gaussian, mean is the first half of the last dimension
+          of the encoder output, log of the standard deviation the second
+          half
+        """
+        super().__init__()
+        if isinstance(shape, int):
+            shape = (shape,)
+        if isinstance(shape, list):
+            shape = tuple(shape)
+        self.shape = shape
+        self.n_dim = len(shape)
+        self.d = np.prod(shape)
+        self.context_encoder = context_encoder
+
+    def forward(self, num_samples=1, context=None):
+        encoder_output = self.context_encoder(context)
+        split_ind = encoder_output.shape[-1] // 2
+        mean = encoder_output[..., :split_ind]
+        log_scale = encoder_output[..., split_ind:]
+        eps = torch.randn(
+            (num_samples,) + self.shape, dtype=mean.dtype, device=mean.device
+        )
+        z = mean + torch.exp(log_scale) * eps
+        log_p = -0.5 * self.d * np.log(2 * np.pi) - torch.sum(
+            log_scale + 0.5 * torch.pow(eps, 2), list(range(1, self.n_dim + 1))
+        )
+        return z, log_p
+
+    def log_prob(self, z, context=None):
+        encoder_output = self.context_encoder(context)
+        split_ind = encoder_output.shape[-1] // 2
+        mean = encoder_output[..., :split_ind]
+        log_scale = encoder_output[..., split_ind:]
+        log_p = -0.5 * self.d * np.log(2 * np.pi) - torch.sum(
+            log_scale + 0.5 * torch.pow((z - mean) / torch.exp(log_scale), 2),
+            list(range(1, self.n_dim + 1)),
+        )
+        return log_p
+
+
 class Uniform(BaseDistribution):
     """
     Multivariate uniform distribution
     """
 
     def __init__(self, shape, low=-1.0, high=1.0):
         """Constructor
@@ -122,23 +175,23 @@
             shape = tuple(shape)
         self.shape = shape
         self.d = np.prod(shape)
         self.low = torch.tensor(low)
         self.high = torch.tensor(high)
         self.log_prob_val = -self.d * np.log(self.high - self.low)
 
-    def forward(self, num_samples=1):
+    def forward(self, num_samples=1, context=None):
         eps = torch.rand(
             (num_samples,) + self.shape, dtype=self.low.dtype, device=self.low.device
         )
         z = self.low + (self.high - self.low) * eps
         log_p = self.log_prob_val * torch.ones(num_samples, device=self.low.device)
         return z, log_p
 
-    def log_prob(self, z):
+    def log_prob(self, z, context=None):
         log_p = self.log_prob_val * torch.ones(z.shape[0], device=z.device)
         out_range = torch.logical_or(z < self.low, z > self.high)
         ind_inf = torch.any(torch.reshape(out_range, (z.shape[0], -1)), dim=-1)
         log_p[ind_inf] = -np.inf
         return log_p
 
 
@@ -181,19 +234,19 @@
         self.register_buffer("inv_perm", inv_perm_)
 
         if scale is None:
             self.register_buffer("scale", torch.ones(self.ndim))
         else:
             self.register_buffer("scale", scale)
 
-    def forward(self, num_samples=1):
+    def forward(self, num_samples=1, context=None):
         z = self.sample(num_samples)
         return z, self.log_prob(z)
 
-    def sample(self, num_samples=1):
+    def sample(self, num_samples=1, context=None):
         eps_u = (
             torch.rand(
                 (num_samples, len(self.ind)),
                 dtype=self.scale.dtype,
                 device=self.scale.device,
             )
             - 0.5
@@ -203,15 +256,15 @@
             dtype=self.scale.dtype,
             device=self.scale.device,
         )
         z = torch.cat((eps_u, eps_g), -1)
         z = z[..., self.inv_perm]
         return self.scale * z
 
-    def log_prob(self, z):
+    def log_prob(self, z, context=None):
         log_p_u = torch.broadcast_to(-torch.log(self.scale[self.ind]), (len(z), -1))
         log_p_g = (
             -0.5 * np.log(2 * np.pi)
             - torch.log(self.scale[self.ind_])
             - 0.5 * torch.pow(z[..., self.ind_] / self.scale[self.ind_], 2)
         )
         return torch.sum(log_p_u, -1) + torch.sum(log_p_g, -1)
```

### Comparing `normflows-1.7.1/normflows/distributions/base_test.py` & `normflows-1.7.2/normflows/distributions/base_test.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,26 +1,43 @@
 import unittest
 import torch
 import numpy as np
 
 from normflows.distributions.base import DiagGaussian, UniformGaussian, \
     ClassCondDiagGaussian, GlowBase, AffineGaussian, GaussianMixture, \
-    GaussianPCA, Uniform
+    GaussianPCA, Uniform, ConditionalDiagGaussian
 from normflows.distributions.distribution_test import DistributionTest
+from normflows.nets.mlp import MLP
 
 
 class BaseTest(DistributionTest):
     def test_diag_gaussian(self):
         for shape in [1, (3,), [2, 3]]:
             for num_samples in [1, 3]:
                 with self.subTest(shape=shape, num_samples=num_samples):
                     distribution = DiagGaussian(shape)
                     self.checkForwardLogProb(distribution, num_samples)
                     _ = self.checkSample(distribution, num_samples)
 
+    def test_conditional_diag_gaussian(self):
+        context_size = 5
+        hidden_units = 16
+        for shape, base_param_size in [(1, 2), ([3], 6)]:
+            for num_samples in [1, 3]:
+                with self.subTest(shape=shape, base_param_size=base_param_size,
+                                  num_samples=num_samples):
+                    context_encoder = MLP([context_size, hidden_units,
+                                           base_param_size])
+                    distribution = ConditionalDiagGaussian(shape, context_encoder)
+                    context = torch.randn(num_samples, context_size)
+                    self.checkForwardLogProb(distribution, num_samples,
+                                             context=context)
+                    _ = self.checkSample(distribution, num_samples,
+                                         context=context)
+
     def test_uniform(self):
         for shape in [1, (3,), [2, 3]]:
             for num_samples in [1, 3]:
                 with self.subTest(shape=shape, num_samples=num_samples):
                     distribution = Uniform(shape)
                     self.checkForwardLogProb(distribution, num_samples)
                     _ = self.checkSample(distribution, num_samples)
```

### Comparing `normflows-1.7.1/normflows/distributions/decoder.py` & `normflows-1.7.2/normflows/distributions/decoder.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/distributions/decoder_test.py` & `normflows-1.7.2/normflows/distributions/decoder_test.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/distributions/distribution_test.py` & `normflows-1.7.2/normflows/distributions/distribution_test.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/distributions/encoder.py` & `normflows-1.7.2/normflows/distributions/encoder.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/distributions/encoder_test.py` & `normflows-1.7.2/normflows/distributions/encoder_test.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/distributions/linear_interpolation.py` & `normflows-1.7.2/normflows/distributions/linear_interpolation.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/distributions/mh_proposal.py` & `normflows-1.7.2/normflows/distributions/mh_proposal.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/distributions/prior.py` & `normflows-1.7.2/normflows/distributions/prior.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/distributions/prior_test.py` & `normflows-1.7.2/normflows/distributions/prior_test.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/distributions/target.py` & `normflows-1.7.2/normflows/distributions/target.py`

 * *Files 19% similar despite different names*

```diff
@@ -189,7 +189,37 @@
         d = torch.zeros((len(z), 0), dtype=z.dtype, device=z.device)
         for i in range(self.n_rings):
             d_ = ((torch.norm(z, dim=1) - 2 / self.n_rings * (i + 1)) ** 2) / (
                 2 * self.scale**2
             )
             d = torch.cat((d, d_[:, None]), 1)
         return torch.logsumexp(-d, 1)
+
+
+class ConditionalDiagGaussian(Target):
+    """
+    Gaussian distribution conditioned on its mean and standard
+    deviation
+
+    The first half of the entries of the condition, also called context,
+    are the mean, while the second half are the standard deviation.
+    """
+    def log_prob(self, z, context=None):
+        d = z.shape[-1]
+        loc = context[:, :d]
+        scale = context[:, d:]
+        log_p = -0.5 * d * np.log(2 * np.pi) - torch.sum(
+            torch.log(scale) + 0.5 * torch.pow((z - loc) / scale, 2),
+            dim=-1
+        )
+        return log_p
+
+    def sample(self, num_samples=1, context=None):
+        d = context.shape[-1] // 2
+        loc = context[:, :d]
+        scale = context[:, d:]
+        eps = torch.randn(
+            (num_samples, d), dtype=context.dtype, device=context.device
+        )
+        z = loc + scale * eps
+        return z
+
```

### Comparing `normflows-1.7.1/normflows/distributions/target_test.py` & `normflows-1.7.2/normflows/distributions/target_test.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,12 +1,15 @@
 import unittest
 
+import torch
+
 from normflows.distributions.base import DiagGaussian
 from normflows.distributions.target import TwoMoons, \
-    CircularGaussianMixture, RingMixture, TwoIndependent
+    CircularGaussianMixture, RingMixture, TwoIndependent, \
+    ConditionalDiagGaussian
 
 
 class TargetTest(unittest.TestCase):
     def test_targets(self):
         targets = [TwoMoons, CircularGaussianMixture,
                    RingMixture]
         for num_samples in [1, 5]:
@@ -27,10 +30,23 @@
             with self.subTest(num_samples=num_samples):
                 # Test target
                 samples = target.sample(num_samples)
                 assert samples.shape == (num_samples, 4)
                 log_p = target.log_prob(samples)
                 assert log_p.shape == (num_samples,)
 
+    def test_conditional(self):
+        target = ConditionalDiagGaussian()
+        for num_samples in [1, 5]:
+            for size in [1, 3]:
+                with self.subTest(num_samples=num_samples,
+                                  size=size):
+                    context = torch.rand(num_samples, size * 2) + 0.5
+                    # Test target
+                    samples = target.sample(num_samples, context)
+                    assert samples.shape == (num_samples, size)
+                    log_p = target.log_prob(samples, context)
+                    assert log_p.shape == (num_samples,)
+
 
 if __name__ == "__main__":
     unittest.main()
```

### Comparing `normflows-1.7.1/normflows/flows/__init__.py` & `normflows-1.7.2/normflows/flows/__init__.py`

 * *Files 19% similar despite different names*

```diff
@@ -27,7 +27,19 @@
     CoupledRationalQuadraticSpline,
     AutoregressiveRationalQuadraticSpline,
     CircularCoupledRationalQuadraticSpline,
     CircularAutoregressiveRationalQuadraticSpline,
 )
 
 from .stochastic import MetropolisHastings, HamiltonianMonteCarlo
+
+from . import (
+    base,
+    mixing,
+    normalization,
+    periodic,
+    planar,
+    radial,
+    reshape,
+    residual,
+    stochastic,
+)
```

### Comparing `normflows-1.7.1/normflows/flows/affine/autoregressive.py` & `normflows-1.7.2/normflows/flows/affine/autoregressive.py`

 * *Files 24% similar despite different names*

```diff
@@ -44,26 +44,43 @@
         raise NotImplementedError()
 
     def _elementwise_inverse(self, inputs, autoregressive_params):
         raise NotImplementedError()
 
 
 class MaskedAffineAutoregressive(Autoregressive):
+    """ Masked affine autoregressive flow, mostly referred to as
+    Masked Autoregressive Flow (MAF), see
+    [arXiv 1705.07057](https://arxiv.org/abs/1705.07057).
+    """
     def __init__(
         self,
         features,
         hidden_features,
         context_features=None,
         num_blocks=2,
         use_residual_blocks=True,
         random_mask=False,
         activation=F.relu,
         dropout_probability=0.0,
         use_batch_norm=False,
     ):
+        """Constructor
+
+        Args:
+          features: Number of features/input dimensions
+          hidden_features: Number of hidden units in the MADE network
+          context_features: Number of context/conditional features
+          num_blocks: Number of blocks in the MADE network
+          use_residual_blocks: Flag whether residual blocks should be used
+          random_mask: Flag whether to use random masks
+          activation: Activation function to be used in the MADE network
+          dropout_probability: Dropout probability in the MADE network
+          use_batch_norm: Flag whether batch normalization should be used
+        """
         self.features = features
         made = made_module.MADE(
             features=features,
             hidden_features=hidden_features,
             context_features=context_features,
             num_blocks=num_blocks,
             output_multiplier=self._output_dim_multiplier(),
```

### Comparing `normflows-1.7.1/normflows/flows/affine/autoregressive_test.py` & `normflows-1.7.2/normflows/flows/affine/autoregressive_test.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/flows/affine/coupling.py` & `normflows-1.7.2/normflows/flows/affine/coupling.py`

 * *Files 1% similar despite different names*

```diff
@@ -193,20 +193,20 @@
           s: scale mapping, i.e. neural network, where first input dimension is batch dim, if None no scale is applied
         """
         super().__init__()
         self.b_cpu = b.view(1, *b.size())
         self.register_buffer("b", self.b_cpu)
 
         if s is None:
-            self.s = lambda x: torch.zeros_like(x)
+            self.s = torch.zeros_like
         else:
             self.add_module("s", s)
 
         if t is None:
-            self.t = lambda x: torch.zeros_like(x)
+            self.t = torch.zeros_like
         else:
             self.add_module("t", t)
 
     def forward(self, z):
         z_masked = self.b * z
         scale = self.s(z_masked)
         nan = torch.tensor(np.nan, dtype=z.dtype, device=z.device)
```

### Comparing `normflows-1.7.1/normflows/flows/affine/coupling_test.py` & `normflows-1.7.2/normflows/flows/affine/coupling_test.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/flows/affine/glow.py` & `normflows-1.7.2/normflows/flows/affine/glow.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/flows/affine/glow_test.py` & `normflows-1.7.2/normflows/flows/affine/glow_test.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/flows/base.py` & `normflows-1.7.2/normflows/flows/base.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/flows/base_test.py` & `normflows-1.7.2/normflows/flows/base_test.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/flows/flow_test.py` & `normflows-1.7.2/normflows/flows/flow_test.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/flows/mixing.py` & `normflows-1.7.2/normflows/flows/mixing.py`

 * *Files 2% similar despite different names*

```diff
@@ -25,27 +25,27 @@
             perm = torch.randperm(self.num_channels)
             inv_perm = torch.empty_like(perm).scatter_(
                 dim=0, index=perm, src=torch.arange(self.num_channels)
             )
             self.register_buffer("perm", perm)
             self.register_buffer("inv_perm", inv_perm)
 
-    def forward(self, z):
+    def forward(self, z, context=None):
         if self.mode == "shuffle":
             z = z[:, self.perm, ...]
         elif self.mode == "swap":
             z1 = z[:, : self.num_channels // 2, ...]
             z2 = z[:, self.num_channels // 2 :, ...]
             z = torch.cat([z2, z1], dim=1)
         else:
             raise NotImplementedError("The mode " + self.mode + " is not implemented.")
         log_det = torch.zeros(len(z), device=z.device)
         return z, log_det
 
-    def inverse(self, z):
+    def inverse(self, z, context=None):
         if self.mode == "shuffle":
             z = z[:, self.inv_perm, ...]
         elif self.mode == "swap":
             z1 = z[:, : (self.num_channels + 1) // 2, ...]
             z2 = z[:, (self.num_channels + 1) // 2 :, ...]
             z = torch.cat([z2, z1], dim=1)
         else:
@@ -178,29 +178,29 @@
                 L_inv = torch.inverse(L.double()).type(self.log_S.dtype)
                 U_inv = torch.inverse(U.double()).type(self.log_S.dtype)
             W = U_inv @ L_inv @ self.P.t()
         else:
             W = self.P @ L @ U
         return W
 
-    def forward(self, z):
+    def forward(self, z, context=None):
         if self.use_lu:
             W = self._assemble_W(inverse=True)
             log_det = -torch.sum(self.log_S)
         else:
             W_dtype = self.W.dtype
             if W_dtype == torch.float64:
                 W = torch.inverse(self.W)
             else:
                 W = torch.inverse(self.W.double()).type(W_dtype)
             log_det = -torch.slogdet(self.W)[1]
         z_ = z @ W
         return z_, log_det
 
-    def inverse(self, z):
+    def inverse(self, z, context=None):
         if self.use_lu:
             W = self._assemble_W()
             log_det = torch.sum(self.log_S)
         else:
             W = self.W
             log_det = torch.slogdet(self.W)[1]
         z_ = z @ W
@@ -548,16 +548,16 @@
         # Initialize
         super().__init__()
 
         # Define modules
         self.permutation = _RandomPermutation(num_channels)
         self.linear = _LULinear(num_channels, identity_init=identity_init)
 
-    def forward(self, z):
-        z, log_det = self.linear.inverse(z)
-        z, _ = self.permutation.inverse(z)
+    def forward(self, z, context=None):
+        z, log_det = self.linear.inverse(z, context=context)
+        z, _ = self.permutation.inverse(z, context=context)
         return z, log_det.view(-1)
 
-    def inverse(self, z):
-        z, _ = self.permutation(z)
-        z, log_det = self.linear(z)
+    def inverse(self, z, context=None):
+        z, _ = self.permutation(z, context=context)
+        z, log_det = self.linear(z, context=context)
         return z, log_det.view(-1)
```

### Comparing `normflows-1.7.1/normflows/flows/mixing_test.py` & `normflows-1.7.2/normflows/flows/mixing_test.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/flows/neural_spline/autoregressive.py` & `normflows-1.7.2/normflows/flows/neural_spline/autoregressive.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/flows/neural_spline/autoregressive_test.py` & `normflows-1.7.2/normflows/flows/neural_spline/autoregressive_test.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/flows/neural_spline/coupling.py` & `normflows-1.7.2/normflows/flows/neural_spline/coupling.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/flows/neural_spline/coupling_test.py` & `normflows-1.7.2/normflows/flows/neural_spline/coupling_test.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/flows/neural_spline/wrapper.py` & `normflows-1.7.2/normflows/flows/neural_spline/wrapper.py`

 * *Files 4% similar despite different names*

```diff
@@ -178,59 +178,61 @@
     """
 
     def __init__(
         self,
         num_input_channels,
         num_blocks,
         num_hidden_channels,
+        num_context_channels=None,
         num_bins=8,
         tail_bound=3,
         activation=nn.ReLU,
         dropout_probability=0.0,
         permute_mask=False,
         init_identity=True,
     ):
         """Constructor
 
         Args:
           num_input_channels (int): Flow dimension
           num_blocks (int): Number of residual blocks of the parameter NN
           num_hidden_channels (int): Number of hidden units of the NN
+          num_context_channels (int): Number of context/conditional channels
           num_bins (int): Number of bins
           tail_bound (int): Bound of the spline tails
-          activation (torch module): Activation function
+          activation (torch.nn.Module): Activation function
           dropout_probability (float): Dropout probability of the NN
           permute_mask (bool): Flag, permutes the mask of the NN
           init_identity (bool): Flag, initialize transform as identity
         """
         super().__init__()
 
         self.mprqat = MaskedPiecewiseRationalQuadraticAutoregressive(
             features=num_input_channels,
             hidden_features=num_hidden_channels,
-            context_features=None,
+            context_features=num_context_channels,
             num_bins=num_bins,
             tails="linear",
             tail_bound=tail_bound,
             num_blocks=num_blocks,
             use_residual_blocks=True,
             random_mask=False,
             permute_mask=permute_mask,
             activation=activation(),
             dropout_probability=dropout_probability,
             use_batch_norm=False,
             init_identity=init_identity,
         )
 
-    def forward(self, z):
-        z, log_det = self.mprqat.inverse(z)
+    def forward(self, z, context=None):
+        z, log_det = self.mprqat.inverse(z, context=context)
         return z, log_det.view(-1)
 
-    def inverse(self, z):
-        z, log_det = self.mprqat(z)
+    def inverse(self, z, context=None):
+        z, log_det = self.mprqat(z, context=context)
         return z, log_det.view(-1)
 
 
 class CircularAutoregressiveRationalQuadraticSpline(Flow):
     """
     Neural spline flow coupling layer, wrapper for the implementation
     of Durkan et al., see [sources](https://github.com/bayesiains/nsf)
@@ -238,28 +240,30 @@
 
     def __init__(
         self,
         num_input_channels,
         num_blocks,
         num_hidden_channels,
         ind_circ,
+        num_context_channels=None,
         num_bins=8,
         tail_bound=3,
         activation=nn.ReLU,
         dropout_probability=0.0,
         permute_mask=True,
         init_identity=True,
     ):
         """Constructor
 
         Args:
           num_input_channels (int): Flow dimension
           num_blocks (int): Number of residual blocks of the parameter NN
           num_hidden_channels (int): Number of hidden units of the NN
           ind_circ (Iterable): Indices of the circular coordinates
+          num_context_channels (int): Number of context/conditional channels
           num_bins (int): Number of bins
           tail_bound (int): Bound of the spline tails
           activation (torch module): Activation function
           dropout_probability (float): Dropout probability of the NN
           permute_mask (bool): Flag, permutes the mask of the NN
           init_identity (bool): Flag, initialize transform as identity
         """
@@ -268,28 +272,28 @@
         tails = [
             "circular" if i in ind_circ else "linear" for i in range(num_input_channels)
         ]
 
         self.mprqat = MaskedPiecewiseRationalQuadraticAutoregressive(
             features=num_input_channels,
             hidden_features=num_hidden_channels,
-            context_features=None,
+            context_features=num_context_channels,
             num_bins=num_bins,
             tails=tails,
             tail_bound=tail_bound,
             num_blocks=num_blocks,
             use_residual_blocks=True,
             random_mask=False,
             permute_mask=permute_mask,
             activation=activation(),
             dropout_probability=dropout_probability,
             use_batch_norm=False,
             init_identity=init_identity,
         )
 
-    def forward(self, z):
-        z, log_det = self.mprqat.inverse(z)
+    def forward(self, z, context=None):
+        z, log_det = self.mprqat.inverse(z, context=context)
         return z, log_det.view(-1)
 
-    def inverse(self, z):
-        z, log_det = self.mprqat(z)
+    def inverse(self, z, context=None):
+        z, log_det = self.mprqat(z, context=context)
         return z, log_det.view(-1)
```

### Comparing `normflows-1.7.1/normflows/flows/neural_spline/wrapper_test.py` & `normflows-1.7.2/normflows/flows/neural_spline/wrapper_test.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/flows/normalization.py` & `normflows-1.7.2/normflows/flows/normalization.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/flows/periodic.py` & `normflows-1.7.2/normflows/flows/periodic.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/flows/periodic_test.py` & `normflows-1.7.2/normflows/flows/periodic_test.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/flows/planar.py` & `normflows-1.7.2/normflows/flows/planar.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/flows/planar_test.py` & `normflows-1.7.2/normflows/flows/planar_test.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/flows/radial.py` & `normflows-1.7.2/normflows/flows/radial.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/flows/reshape.py` & `normflows-1.7.2/normflows/flows/reshape.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/flows/residual.py` & `normflows-1.7.2/normflows/flows/residual.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/flows/residual_test.py` & `normflows-1.7.2/normflows/flows/residual_test.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/flows/stochastic.py` & `normflows-1.7.2/normflows/flows/stochastic.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/flows/stochastic_test.py` & `normflows-1.7.2/normflows/flows/stochastic_test.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/nets/cnn.py` & `normflows-1.7.2/normflows/nets/cnn.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/nets/lipschitz.py` & `normflows-1.7.2/normflows/nets/lipschitz.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/nets/made.py` & `normflows-1.7.2/normflows/nets/made.py`

 * *Files 1% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 """
 
 import torch
 
 from torch import nn
 from torch.nn import functional as F, init
 
-from ..utils import tile
+from ..utils.nn import tile
 
 
 def _get_input_degrees(in_features):
     """Returns the degrees an input to MADE should have."""
     return torch.arange(1, in_features + 1)
 
 
@@ -238,15 +238,15 @@
     ):
         if use_residual_blocks and random_mask:
             raise ValueError("Residual blocks can't be used with random masks.")
         super().__init__()
 
         # Preprocessing
         if preprocessing is None:
-            self.preprocessing = lambda inputs: inputs
+            self.preprocessing = torch.nn.Identity()
         else:
             self.preprocessing = preprocessing
 
         # Initial layer.
         input_degrees_ = _get_input_degrees(features)
         if permute_mask:
             input_degrees_ = input_degrees_[torch.randperm(features)]
```

### Comparing `normflows-1.7.1/normflows/nets/made_test.py` & `normflows-1.7.2/normflows/nets/made_test.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/nets/mlp.py` & `normflows-1.7.2/normflows/nets/mlp.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/nets/resnet.py` & `normflows-1.7.2/normflows/nets/resnet.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/sampling/hais.py` & `normflows-1.7.2/normflows/sampling/hais.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/transforms.py` & `normflows-1.7.2/normflows/transforms.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/transforms_test.py` & `normflows-1.7.2/normflows/transforms_test.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/utils/eval.py` & `normflows-1.7.2/normflows/utils/eval.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/utils/masks.py` & `normflows-1.7.2/normflows/utils/masks.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/utils/nn.py` & `normflows-1.7.2/normflows/utils/nn.py`

 * *Files 5% similar despite different names*

```diff
@@ -109,15 +109,15 @@
             self.scale = scale
 
         self.apply_bias = bias
         if self.apply_bias:
             self.bias = nn.Parameter(torch.zeros(len(self.ind)))
 
         if activation is None:
-            self.activation = lambda input: input
+            self.activation = torch.nn.Identity()
         else:
             self.activation = activation
 
     def forward(self, inputs):
         inputs_ = inputs[..., self.ind]
         inputs_ = self.scale * inputs_
         inputs_ = self.weights[:, 0] * torch.sin(inputs_) + self.weights[
```

### Comparing `normflows-1.7.1/normflows/utils/optim.py` & `normflows-1.7.2/normflows/utils/optim.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/utils/preprocessing.py` & `normflows-1.7.2/normflows/utils/preprocessing.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/utils/splines.py` & `normflows-1.7.2/normflows/utils/splines.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows/utils/splines_test.py` & `normflows-1.7.2/normflows/utils/splines_test.py`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/normflows.egg-info/PKG-INFO` & `normflows-1.7.2/normflows.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: normflows
-Version: 1.7.1
+Version: 1.7.2
 Summary: Pytorch implementation of normalizing flows
 Home-page: https://github.com/VincentStimper/normalizing-flows
 Author: Vincent Stimper
 Author-email: vincent.stimper@tuebingen.mpg.de
 License: MIT
 Download-URL: https://github.com/VincentStimper/normalizing-flows/archive/refs/heads/master.zip
 Platform: UNKNOWN
@@ -18,15 +18,15 @@
 # `normflows`: A PyTorch Package for Normalizing Flows
 
 [![documentation](https://github.com/VincentStimper/normalizing-flows/actions/workflows/mkdocs.yaml/badge.svg)](https://vincentstimper.github.io/normalizing-flows/)
 ![unit-tests](https://github.com/VincentStimper/normalizing-flows/actions/workflows/pytest.yaml/badge.svg)
 ![code coverage](https://raw.githubusercontent.com/VincentStimper/normalizing-flows/coverage-badge/coverage.svg?raw=true)
 [![License: MIT](https://img.shields.io/badge/Licence-MIT-b31b1b.svg)](https://opensource.org/licenses/MIT)
 [![DOI](https://joss.theoj.org/papers/10.21105/joss.05361/status.svg)](https://doi.org/10.21105/joss.05361)
-[![PyPI](https://img.shields.io/badge/PyPI-1.7.1-blue.svg)](https://pypi.org/project/normflows/)
+[![PyPI](https://img.shields.io/badge/PyPI-1.7.2-blue.svg)](https://pypi.org/project/normflows/)
 [![Downloads](https://static.pepy.tech/personalized-badge/normflows?period=total&units=international_system&left_color=grey&right_color=orange&left_text=Downloads)](https://pepy.tech/project/normflows)
 
 
 `normflows` is a PyTorch implementation of discrete normalizing flows. Many popular flow architectures are implemented,
 see the [list below](#implemented-flows). The package can be easily [installed via pip](#installation).
 The basic usage is described [here](#usage), and a [full documentation](https://vincentstimper.github.io/normalizing-flows/) 
 is available as well. A more detailed description of this package is given in our
@@ -151,15 +151,15 @@
 optimizer.step()
 ```
 
 ## Examples
 
 We provide several illustrative examples of how to use the package in the
 [`examples`](https://github.com/VincentStimper/normalizing-flows/blob/master/examples)
-directory. Amoung them are implementations of 
+directory. Among them are implementations of 
 [Glow](https://github.com/VincentStimper/normalizing-flows/blob/master/examples/glow.ipynb),
 a [VAE](https://github.com/VincentStimper/normalizing-flows/blob/master/examples/vae.py), and
 a [Residual Flow](https://github.com/VincentStimper/normalizing-flows/blob/master/examples/residual.ipynb). 
 More advanced experiments can be done with the scripts listed in the
 [repository about resampled base distributions](https://github.com/VincentStimper/resampled-base-flows),
 see its [`experiments`](https://github.com/VincentStimper/resampled-base-flows/tree/master/experiments)
 folder.
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: normflows Version: 1.7.1 Summary: Pytorch
+Metadata-Version: 2.1 Name: normflows Version: 1.7.2 Summary: Pytorch
 implementation of normalizing flows Home-page: https://github.com/
 VincentStimper/normalizing-flows Author: Vincent Stimper Author-email:
 vincent.stimper@tuebingen.mpg.de License: MIT Download-URL: https://github.com/
 VincentStimper/normalizing-flows/archive/refs/heads/master.zip Platform:
 UNKNOWN Classifier: Development Status :: 3 - Alpha Classifier: Intended
 Audience :: Developers Classifier: Programming Language :: Python :: 3
 Description-Content-Type: text/markdown Provides-Extra: docs License-File:
@@ -11,15 +11,15 @@
 workflows/mkdocs.yaml/badge.svg)](https://vincentstimper.github.io/normalizing-
 flows/) ![unit-tests](https://github.com/VincentStimper/normalizing-flows/
 actions/workflows/pytest.yaml/badge.svg) ![code coverage](https://
 raw.githubusercontent.com/VincentStimper/normalizing-flows/coverage-badge/
 coverage.svg?raw=true) [![License: MIT](https://img.shields.io/badge/Licence-
 MIT-b31b1b.svg)](https://opensource.org/licenses/MIT) [![DOI](https://
 joss.theoj.org/papers/10.21105/joss.05361/status.svg)](https://doi.org/
-10.21105/joss.05361) [![PyPI](https://img.shields.io/badge/PyPI-1.7.1-
+10.21105/joss.05361) [![PyPI](https://img.shields.io/badge/PyPI-1.7.2-
 blue.svg)](https://pypi.org/project/normflows/) [![Downloads](https://
 static.pepy.tech/personalized-badge/
 normflows?period=total&units=international_system&left_color=grey&right_color=orange&left_text=Downloads)]
 (https://pepy.tech/project/normflows) `normflows` is a PyTorch implementation
 of discrete normalizing flows. Many popular flow architectures are implemented,
 see the [list below](#implemented-flows). The package can be easily [installed
 via pip](#installation). The basic usage is described [here](#usage), and a
@@ -96,15 +96,15 @@
 target) ``` The loss can be computed with the methods of the model and
 minimized. ```python # When doing maximum likelihood learning, i.e. minimizing
 the forward KLD # with no target distribution given loss = model.forward_kld(x)
 # When minimizing the reverse KLD based on the given target distribution loss =
 model.reverse_kld(num_samples=512) # Optimization as usual loss.backward()
 optimizer.step() ``` ## Examples We provide several illustrative examples of
 how to use the package in the [`examples`](https://github.com/VincentStimper/
-normalizing-flows/blob/master/examples) directory. Amoung them are
+normalizing-flows/blob/master/examples) directory. Among them are
 implementations of [Glow](https://github.com/VincentStimper/normalizing-flows/
 blob/master/examples/glow.ipynb), a [VAE](https://github.com/VincentStimper/
 normalizing-flows/blob/master/examples/vae.py), and a [Residual Flow](https://
 github.com/VincentStimper/normalizing-flows/blob/master/examples/
 residual.ipynb). More advanced experiments can be done with the scripts listed
 in the [repository about resampled base distributions](https://github.com/
 VincentStimper/resampled-base-flows), see its [`experiments`](https://
```

### Comparing `normflows-1.7.1/normflows.egg-info/SOURCES.txt` & `normflows-1.7.2/normflows.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `normflows-1.7.1/setup.py` & `normflows-1.7.2/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 from codecs import open
 from os import path
 
-__version__ = "1.7.1"
+__version__ = "1.7.2"
 
 here = path.abspath(path.dirname(__file__))
 
 # Get the long description from the README file
 with open(path.join(here, "README.md"), encoding="utf-8") as f:
     long_description = f.read()
```

