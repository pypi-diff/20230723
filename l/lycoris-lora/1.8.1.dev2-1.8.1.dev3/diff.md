# Comparing `tmp/lycoris_lora-1.8.1.dev2.tar.gz` & `tmp/lycoris_lora-1.8.1.dev3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "lycoris_lora-1.8.1.dev2.tar", last modified: Sun Jul 23 04:03:14 2023, max compression
+gzip compressed data, was "lycoris_lora-1.8.1.dev3.tar", last modified: Sun Jul 23 05:44:50 2023, max compression
```

## Comparing `lycoris_lora-1.8.1.dev2.tar` & `lycoris_lora-1.8.1.dev3.tar`

### file list

```diff
@@ -1,60 +1,60 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 04:03:14.411133 lycoris_lora-1.8.1.dev2/
--rw-rw-rw-   0        0        0     1682 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/.gitignore
--rw-rw-rw-   0        0        0     4436 2023-04-09 13:45:45.000000 lycoris_lora-1.8.1.dev2/Algo.md
--rw-rw-rw-   0        0        0     1111 2023-07-22 06:17:56.000000 lycoris_lora-1.8.1.dev2/Change.md
--rw-rw-rw-   0        0        0     2828 2023-03-09 12:01:15.000000 lycoris_lora-1.8.1.dev2/Demo.md
--rw-rw-rw-   0        0        0    11545 2023-03-09 05:37:07.000000 lycoris_lora-1.8.1.dev2/LICENSE.md
--rw-rw-rw-   0        0        0      353 2023-07-23 04:03:14.410634 lycoris_lora-1.8.1.dev2/PKG-INFO
--rw-rw-rw-   0        0        0     7451 2023-07-22 06:17:56.000000 lycoris_lora-1.8.1.dev2/README.md
-drwxrwxrwx   0        0        0        0 2023-07-23 04:03:14.384631 lycoris_lora-1.8.1.dev2/experiments/
--rw-rw-rw-   0        0        0     3579 2023-03-12 01:46:48.000000 lycoris_lora-1.8.1.dev2/experiments/better_conv.py
--rw-rw-rw-   0        0        0     1967 2023-03-12 01:46:43.000000 lycoris_lora-1.8.1.dev2/experiments/better_conv_extract.py
--rw-rw-rw-   0        0        0      651 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/experiments/compare_norm.py
--rw-rw-rw-   0        0        0     8783 2023-03-12 03:21:33.000000 lycoris_lora-1.8.1.dev2/experiments/concept_neuron.py
--rw-rw-rw-   0        0        0      894 2023-03-09 14:26:54.000000 lycoris_lora-1.8.1.dev2/experiments/locon_extract_test.py
--rw-rw-rw-   0        0        0      755 2023-03-10 15:36:09.000000 lycoris_lora-1.8.1.dev2/experiments/locon_merge_test.py
--rw-rw-rw-   0        0        0     1028 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/experiments/loha_svd.py
--rw-rw-rw-   0        0        0     3411 2023-03-09 05:37:07.000000 lycoris_lora-1.8.1.dev2/experiments/singular_value_test.py
--rw-rw-rw-   0        0        0     2334 2023-03-11 09:28:26.000000 lycoris_lora-1.8.1.dev2/experiments/sparse_bias_test.py
--rw-rw-rw-   0        0        0     2791 2023-03-12 01:46:48.000000 lycoris_lora-1.8.1.dev2/experiments/time_test.py
--rw-rw-rw-   0        0        0      255 2023-06-25 07:25:35.000000 lycoris_lora-1.8.1.dev2/experiments/weakre_speed.py
--rw-rw-rw-   0        0        0     4116 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/hyperdream_gen_weight.py
-drwxrwxrwx   0        0        0        0 2023-07-23 04:03:14.385632 lycoris_lora-1.8.1.dev2/lycoris/
--rw-rw-rw-   0        0        0       55 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/lycoris/__init__.py
--rw-rw-rw-   0        0        0     2699 2023-07-23 03:48:18.000000 lycoris_lora-1.8.1.dev2/lycoris/config.py
-drwxrwxrwx   0        0        0        0 2023-07-23 04:03:14.387131 lycoris_lora-1.8.1.dev2/lycoris/kohya/
--rw-rw-rw-   0        0        0    39941 2023-07-23 04:02:52.000000 lycoris_lora-1.8.1.dev2/lycoris/kohya/__init__.py
--rw-rw-rw-   0        0        0    48868 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/lycoris/kohya/kohya_model_utils.py
--rw-rw-rw-   0        0        0     1512 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/lycoris/kohya/kohya_utils.py
-drwxrwxrwx   0        0        0        0 2023-07-23 04:03:14.392131 lycoris_lora-1.8.1.dev2/lycoris/modules/
--rw-rw-rw-   0        0        0        0 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/lycoris/modules/__init__.py
--rw-rw-rw-   0        0        0     7334 2023-07-22 06:17:56.000000 lycoris_lora-1.8.1.dev2/lycoris/modules/attention.py
--rw-rw-rw-   0        0        0     4762 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/lycoris/modules/dylora.py
--rw-rw-rw-   0        0        0    10763 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/lycoris/modules/glokr.py
--rw-rw-rw-   0        0        0     4117 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/lycoris/modules/glora.py
--rw-rw-rw-   0        0        0       64 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/lycoris/modules/hyperlycoris.py
-drwxrwxrwx   0        0        0        0 2023-07-23 04:03:14.393132 lycoris_lora-1.8.1.dev2/lycoris/modules/hypernet/
--rw-rw-rw-   0        0        0       97 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/lycoris/modules/hypernet/__init__.py
--rw-rw-rw-   0        0        0     8229 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/lycoris/modules/hypernet/generater.py
--rw-rw-rw-   0        0        0     2103 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/lycoris/modules/ia3.py
--rw-rw-rw-   0        0        0    10342 2023-07-22 06:17:56.000000 lycoris_lora-1.8.1.dev2/lycoris/modules/locon.py
--rw-rw-rw-   0        0        0    10065 2023-07-22 06:17:56.000000 lycoris_lora-1.8.1.dev2/lycoris/modules/loha.py
--rw-rw-rw-   0        0        0    12647 2023-07-22 06:17:56.000000 lycoris_lora-1.8.1.dev2/lycoris/modules/lokr.py
-drwxrwxrwx   0        0        0        0 2023-07-23 04:03:14.394631 lycoris_lora-1.8.1.dev2/lycoris/utils/
--rw-rw-rw-   0        0        0    21031 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/lycoris/utils/__init__.py
--rw-rw-rw-   0        0        0       41 2023-07-23 03:53:39.000000 lycoris_lora-1.8.1.dev2/lycoris/utils/preset.py
--rw-rw-rw-   0        0        0      249 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/lycoris/utils/xformers_utils.py
-drwxrwxrwx   0        0        0        0 2023-07-23 04:03:14.408634 lycoris_lora-1.8.1.dev2/lycoris_lora.egg-info/
--rw-rw-rw-   0        0        0      353 2023-07-23 04:03:14.000000 lycoris_lora-1.8.1.dev2/lycoris_lora.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0     1256 2023-07-23 04:03:14.000000 lycoris_lora-1.8.1.dev2/lycoris_lora.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 04:03:14.000000 lycoris_lora-1.8.1.dev2/lycoris_lora.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        2 2023-03-09 13:25:15.000000 lycoris_lora-1.8.1.dev2/lycoris_lora.egg-info/not-zip-safe
--rw-rw-rw-   0        0        0       41 2023-07-23 04:03:14.000000 lycoris_lora-1.8.1.dev2/lycoris_lora.egg-info/requires.txt
--rw-rw-rw-   0        0        0        8 2023-07-23 04:03:14.000000 lycoris_lora-1.8.1.dev2/lycoris_lora.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      106 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/requirements.txt
--rw-rw-rw-   0        0        0       42 2023-07-23 04:03:14.411133 lycoris_lora-1.8.1.dev2/setup.cfg
--rw-rw-rw-   0        0        0      566 2023-07-23 04:03:10.000000 lycoris_lora-1.8.1.dev2/setup.py
-drwxrwxrwx   0        0        0        0 2023-07-23 04:03:14.409634 lycoris_lora-1.8.1.dev2/tools/
--rw-rw-rw-   0        0        0     4093 2023-07-23 03:43:26.000000 lycoris_lora-1.8.1.dev2/tools/extract_locon.py
--rw-rw-rw-   0        0        0     2299 2023-07-23 03:43:55.000000 lycoris_lora-1.8.1.dev2/tools/merge.py
--rw-rw-rw-   0        0        0    55333 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/train_hyperdream.py
+drwxrwxrwx   0        0        0        0 2023-07-23 05:44:50.267795 lycoris_lora-1.8.1.dev3/
+-rw-rw-rw-   0        0        0     1682 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev3/.gitignore
+-rw-rw-rw-   0        0        0     4436 2023-04-09 13:45:45.000000 lycoris_lora-1.8.1.dev3/Algo.md
+-rw-rw-rw-   0        0        0     1111 2023-07-22 06:17:56.000000 lycoris_lora-1.8.1.dev3/Change.md
+-rw-rw-rw-   0        0        0     2828 2023-03-09 12:01:15.000000 lycoris_lora-1.8.1.dev3/Demo.md
+-rw-rw-rw-   0        0        0    11545 2023-03-09 05:37:07.000000 lycoris_lora-1.8.1.dev3/LICENSE.md
+-rw-rw-rw-   0        0        0      353 2023-07-23 05:44:50.267795 lycoris_lora-1.8.1.dev3/PKG-INFO
+-rw-rw-rw-   0        0        0     7451 2023-07-22 06:17:56.000000 lycoris_lora-1.8.1.dev3/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 05:44:50.241794 lycoris_lora-1.8.1.dev3/experiments/
+-rw-rw-rw-   0        0        0     3579 2023-03-12 01:46:48.000000 lycoris_lora-1.8.1.dev3/experiments/better_conv.py
+-rw-rw-rw-   0        0        0     1967 2023-03-12 01:46:43.000000 lycoris_lora-1.8.1.dev3/experiments/better_conv_extract.py
+-rw-rw-rw-   0        0        0      651 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev3/experiments/compare_norm.py
+-rw-rw-rw-   0        0        0     8783 2023-03-12 03:21:33.000000 lycoris_lora-1.8.1.dev3/experiments/concept_neuron.py
+-rw-rw-rw-   0        0        0      894 2023-03-09 14:26:54.000000 lycoris_lora-1.8.1.dev3/experiments/locon_extract_test.py
+-rw-rw-rw-   0        0        0      755 2023-03-10 15:36:09.000000 lycoris_lora-1.8.1.dev3/experiments/locon_merge_test.py
+-rw-rw-rw-   0        0        0     1028 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev3/experiments/loha_svd.py
+-rw-rw-rw-   0        0        0     3411 2023-03-09 05:37:07.000000 lycoris_lora-1.8.1.dev3/experiments/singular_value_test.py
+-rw-rw-rw-   0        0        0     2334 2023-03-11 09:28:26.000000 lycoris_lora-1.8.1.dev3/experiments/sparse_bias_test.py
+-rw-rw-rw-   0        0        0     2791 2023-03-12 01:46:48.000000 lycoris_lora-1.8.1.dev3/experiments/time_test.py
+-rw-rw-rw-   0        0        0      255 2023-06-25 07:25:35.000000 lycoris_lora-1.8.1.dev3/experiments/weakre_speed.py
+-rw-rw-rw-   0        0        0     4116 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev3/hyperdream_gen_weight.py
+drwxrwxrwx   0        0        0        0 2023-07-23 05:44:50.242794 lycoris_lora-1.8.1.dev3/lycoris/
+-rw-rw-rw-   0        0        0       55 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev3/lycoris/__init__.py
+-rw-rw-rw-   0        0        0     2699 2023-07-23 03:48:18.000000 lycoris_lora-1.8.1.dev3/lycoris/config.py
+drwxrwxrwx   0        0        0        0 2023-07-23 05:44:50.244796 lycoris_lora-1.8.1.dev3/lycoris/kohya/
+-rw-rw-rw-   0        0        0    39941 2023-07-23 04:02:52.000000 lycoris_lora-1.8.1.dev3/lycoris/kohya/__init__.py
+-rw-rw-rw-   0        0        0    48868 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev3/lycoris/kohya/kohya_model_utils.py
+-rw-rw-rw-   0        0        0     1512 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev3/lycoris/kohya/kohya_utils.py
+drwxrwxrwx   0        0        0        0 2023-07-23 05:44:50.249795 lycoris_lora-1.8.1.dev3/lycoris/modules/
+-rw-rw-rw-   0        0        0        0 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev3/lycoris/modules/__init__.py
+-rw-rw-rw-   0        0        0     7334 2023-07-22 06:17:56.000000 lycoris_lora-1.8.1.dev3/lycoris/modules/attention.py
+-rw-rw-rw-   0        0        0     4762 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev3/lycoris/modules/dylora.py
+-rw-rw-rw-   0        0        0    10763 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev3/lycoris/modules/glokr.py
+-rw-rw-rw-   0        0        0     4117 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev3/lycoris/modules/glora.py
+-rw-rw-rw-   0        0        0       64 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev3/lycoris/modules/hyperlycoris.py
+drwxrwxrwx   0        0        0        0 2023-07-23 05:44:50.251295 lycoris_lora-1.8.1.dev3/lycoris/modules/hypernet/
+-rw-rw-rw-   0        0        0       97 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev3/lycoris/modules/hypernet/__init__.py
+-rw-rw-rw-   0        0        0     8229 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev3/lycoris/modules/hypernet/generater.py
+-rw-rw-rw-   0        0        0     2103 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev3/lycoris/modules/ia3.py
+-rw-rw-rw-   0        0        0    10342 2023-07-22 06:17:56.000000 lycoris_lora-1.8.1.dev3/lycoris/modules/locon.py
+-rw-rw-rw-   0        0        0    10065 2023-07-22 06:17:56.000000 lycoris_lora-1.8.1.dev3/lycoris/modules/loha.py
+-rw-rw-rw-   0        0        0    12654 2023-07-23 05:44:15.000000 lycoris_lora-1.8.1.dev3/lycoris/modules/lokr.py
+drwxrwxrwx   0        0        0        0 2023-07-23 05:44:50.252794 lycoris_lora-1.8.1.dev3/lycoris/utils/
+-rw-rw-rw-   0        0        0    21031 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev3/lycoris/utils/__init__.py
+-rw-rw-rw-   0        0        0       41 2023-07-23 03:53:39.000000 lycoris_lora-1.8.1.dev3/lycoris/utils/preset.py
+-rw-rw-rw-   0        0        0      249 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev3/lycoris/utils/xformers_utils.py
+drwxrwxrwx   0        0        0        0 2023-07-23 05:44:50.266295 lycoris_lora-1.8.1.dev3/lycoris_lora.egg-info/
+-rw-rw-rw-   0        0        0      353 2023-07-23 05:44:50.000000 lycoris_lora-1.8.1.dev3/lycoris_lora.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0     1256 2023-07-23 05:44:50.000000 lycoris_lora-1.8.1.dev3/lycoris_lora.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 05:44:50.000000 lycoris_lora-1.8.1.dev3/lycoris_lora.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        2 2023-03-09 13:25:15.000000 lycoris_lora-1.8.1.dev3/lycoris_lora.egg-info/not-zip-safe
+-rw-rw-rw-   0        0        0       41 2023-07-23 05:44:50.000000 lycoris_lora-1.8.1.dev3/lycoris_lora.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        8 2023-07-23 05:44:50.000000 lycoris_lora-1.8.1.dev3/lycoris_lora.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      106 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev3/requirements.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 05:44:50.268294 lycoris_lora-1.8.1.dev3/setup.cfg
+-rw-rw-rw-   0        0        0      566 2023-07-23 05:44:38.000000 lycoris_lora-1.8.1.dev3/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 05:44:50.267295 lycoris_lora-1.8.1.dev3/tools/
+-rw-rw-rw-   0        0        0     4093 2023-07-23 03:43:26.000000 lycoris_lora-1.8.1.dev3/tools/extract_locon.py
+-rw-rw-rw-   0        0        0     2299 2023-07-23 03:43:55.000000 lycoris_lora-1.8.1.dev3/tools/merge.py
+-rw-rw-rw-   0        0        0    55333 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev3/train_hyperdream.py
```

### Comparing `lycoris_lora-1.8.1.dev2/.gitignore` & `lycoris_lora-1.8.1.dev3/.gitignore`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/Algo.md` & `lycoris_lora-1.8.1.dev3/Algo.md`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/Change.md` & `lycoris_lora-1.8.1.dev3/Change.md`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/Demo.md` & `lycoris_lora-1.8.1.dev3/Demo.md`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/LICENSE.md` & `lycoris_lora-1.8.1.dev3/LICENSE.md`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/README.md` & `lycoris_lora-1.8.1.dev3/README.md`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/experiments/better_conv.py` & `lycoris_lora-1.8.1.dev3/experiments/better_conv.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/experiments/better_conv_extract.py` & `lycoris_lora-1.8.1.dev3/experiments/better_conv_extract.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/experiments/compare_norm.py` & `lycoris_lora-1.8.1.dev3/experiments/compare_norm.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/experiments/concept_neuron.py` & `lycoris_lora-1.8.1.dev3/experiments/concept_neuron.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/experiments/locon_extract_test.py` & `lycoris_lora-1.8.1.dev3/experiments/locon_extract_test.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/experiments/locon_merge_test.py` & `lycoris_lora-1.8.1.dev3/experiments/locon_merge_test.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/experiments/loha_svd.py` & `lycoris_lora-1.8.1.dev3/experiments/loha_svd.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/experiments/singular_value_test.py` & `lycoris_lora-1.8.1.dev3/experiments/singular_value_test.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/experiments/sparse_bias_test.py` & `lycoris_lora-1.8.1.dev3/experiments/sparse_bias_test.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/experiments/time_test.py` & `lycoris_lora-1.8.1.dev3/experiments/time_test.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/hyperdream_gen_weight.py` & `lycoris_lora-1.8.1.dev3/hyperdream_gen_weight.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/lycoris/config.py` & `lycoris_lora-1.8.1.dev3/lycoris/config.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/lycoris/kohya/__init__.py` & `lycoris_lora-1.8.1.dev3/lycoris/kohya/__init__.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/lycoris/kohya/kohya_model_utils.py` & `lycoris_lora-1.8.1.dev3/lycoris/kohya/kohya_model_utils.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/lycoris/kohya/kohya_utils.py` & `lycoris_lora-1.8.1.dev3/lycoris/kohya/kohya_utils.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/lycoris/modules/attention.py` & `lycoris_lora-1.8.1.dev3/lycoris/modules/attention.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/lycoris/modules/dylora.py` & `lycoris_lora-1.8.1.dev3/lycoris/modules/dylora.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/lycoris/modules/glokr.py` & `lycoris_lora-1.8.1.dev3/lycoris/modules/glokr.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/lycoris/modules/glora.py` & `lycoris_lora-1.8.1.dev3/lycoris/modules/glora.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/lycoris/modules/hypernet/generater.py` & `lycoris_lora-1.8.1.dev3/lycoris/modules/hypernet/generater.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/lycoris/modules/ia3.py` & `lycoris_lora-1.8.1.dev3/lycoris/modules/ia3.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/lycoris/modules/locon.py` & `lycoris_lora-1.8.1.dev3/lycoris/modules/locon.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/lycoris/modules/loha.py` & `lycoris_lora-1.8.1.dev3/lycoris/modules/loha.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/lycoris/modules/lokr.py` & `lycoris_lora-1.8.1.dev3/lycoris/modules/lokr.py`

 * *Files 0% similar despite different names*

```diff
@@ -173,15 +173,15 @@
             #use scale = 1
             alpha = lora_dim
         self.scale = alpha / self.lora_dim
         self.register_buffer('alpha', torch.tensor(alpha)) # 定数として扱える
 
         self.scalar = nn.Parameter(torch.tensor(0.0))
         if self.use_w2:
-            torch.nn.init.constant_(self.lokr_w2, 0)
+            torch.nn.init.kaiming_uniform_(self.lokr_w2, 0)
         else:
             if self.cp:
                 torch.nn.init.kaiming_uniform_(self.lokr_t2, a=math.sqrt(5))
             torch.nn.init.kaiming_uniform_(self.lokr_w2_a, a=math.sqrt(5))
             torch.nn.init.kaiming_uniform_(self.lokr_w2_b, a=math.sqrt(5))
         
         if self.use_w1:
```

### Comparing `lycoris_lora-1.8.1.dev2/lycoris/utils/__init__.py` & `lycoris_lora-1.8.1.dev3/lycoris/utils/__init__.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/lycoris_lora.egg-info/SOURCES.txt` & `lycoris_lora-1.8.1.dev3/lycoris_lora.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/setup.py` & `lycoris_lora-1.8.1.dev3/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 from setuptools import setup, find_packages
 
 setup(
     name='lycoris_lora',
     packages=find_packages(),
-    version='1.8.1.dev2',
+    version='1.8.1.dev3',
     url='https://github.com/KohakuBlueleaf/LyCORIS',
     description='Lora beYond Conventional methods, Other Rank adaptation Implementations for Stable diffusion',
     author='Shih-Ying Yeh(KohakuBlueLeaf), Yu-Guan Hsieh, Zhidong Gao',
     author_email='apolloyeh0123@gmail.com',
     zip_safe=False,
     install_requires=[
         'torch',
```

### Comparing `lycoris_lora-1.8.1.dev2/tools/extract_locon.py` & `lycoris_lora-1.8.1.dev3/tools/extract_locon.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/tools/merge.py` & `lycoris_lora-1.8.1.dev3/tools/merge.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev2/train_hyperdream.py` & `lycoris_lora-1.8.1.dev3/train_hyperdream.py`

 * *Files identical despite different names*

