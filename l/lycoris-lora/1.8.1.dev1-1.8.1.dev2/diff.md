# Comparing `tmp/lycoris_lora-1.8.1.dev1.tar.gz` & `tmp/lycoris_lora-1.8.1.dev2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "lycoris_lora-1.8.1.dev1.tar", last modified: Fri Jul 21 03:00:03 2023, max compression
+gzip compressed data, was "lycoris_lora-1.8.1.dev2.tar", last modified: Sun Jul 23 04:03:14 2023, max compression
```

## Comparing `lycoris_lora-1.8.1.dev1.tar` & `lycoris_lora-1.8.1.dev2.tar`

### file list

```diff
@@ -1,59 +1,60 @@
-drwxrwxrwx   0        0        0        0 2023-07-21 03:00:03.494421 lycoris_lora-1.8.1.dev1/
--rw-rw-rw-   0        0        0     1682 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev1/.gitignore
--rw-rw-rw-   0        0        0     4436 2023-04-09 13:45:45.000000 lycoris_lora-1.8.1.dev1/Algo.md
--rw-rw-rw-   0        0        0     1111 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev1/Change.md
--rw-rw-rw-   0        0        0     2828 2023-03-09 12:01:15.000000 lycoris_lora-1.8.1.dev1/Demo.md
--rw-rw-rw-   0        0        0    11545 2023-03-09 05:37:07.000000 lycoris_lora-1.8.1.dev1/LICENSE.md
--rw-rw-rw-   0        0        0      353 2023-07-21 03:00:03.493921 lycoris_lora-1.8.1.dev1/PKG-INFO
--rw-rw-rw-   0        0        0     7451 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev1/README.md
-drwxrwxrwx   0        0        0        0 2023-07-21 03:00:03.469420 lycoris_lora-1.8.1.dev1/experiments/
--rw-rw-rw-   0        0        0     3579 2023-03-12 01:46:48.000000 lycoris_lora-1.8.1.dev1/experiments/better_conv.py
--rw-rw-rw-   0        0        0     1967 2023-03-12 01:46:43.000000 lycoris_lora-1.8.1.dev1/experiments/better_conv_extract.py
--rw-rw-rw-   0        0        0      651 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev1/experiments/compare_norm.py
--rw-rw-rw-   0        0        0     8783 2023-03-12 03:21:33.000000 lycoris_lora-1.8.1.dev1/experiments/concept_neuron.py
--rw-rw-rw-   0        0        0      894 2023-03-09 14:26:54.000000 lycoris_lora-1.8.1.dev1/experiments/locon_extract_test.py
--rw-rw-rw-   0        0        0      755 2023-03-10 15:36:09.000000 lycoris_lora-1.8.1.dev1/experiments/locon_merge_test.py
--rw-rw-rw-   0        0        0     1028 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev1/experiments/loha_svd.py
--rw-rw-rw-   0        0        0     3411 2023-03-09 05:37:07.000000 lycoris_lora-1.8.1.dev1/experiments/singular_value_test.py
--rw-rw-rw-   0        0        0     2334 2023-03-11 09:28:26.000000 lycoris_lora-1.8.1.dev1/experiments/sparse_bias_test.py
--rw-rw-rw-   0        0        0     2791 2023-03-12 01:46:48.000000 lycoris_lora-1.8.1.dev1/experiments/time_test.py
--rw-rw-rw-   0        0        0      255 2023-06-25 07:25:35.000000 lycoris_lora-1.8.1.dev1/experiments/weakre_speed.py
--rw-rw-rw-   0        0        0     4116 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev1/hyperdream_gen_weight.py
-drwxrwxrwx   0        0        0        0 2023-07-21 03:00:03.470420 lycoris_lora-1.8.1.dev1/lycoris/
--rw-rw-rw-   0        0        0       55 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev1/lycoris/__init__.py
--rw-rw-rw-   0        0        0     2514 2023-07-21 02:47:27.000000 lycoris_lora-1.8.1.dev1/lycoris/config.py
-drwxrwxrwx   0        0        0        0 2023-07-21 03:00:03.471920 lycoris_lora-1.8.1.dev1/lycoris/kohya/
--rw-rw-rw-   0        0        0    38215 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev1/lycoris/kohya/__init__.py
--rw-rw-rw-   0        0        0    48868 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev1/lycoris/kohya/kohya_model_utils.py
--rw-rw-rw-   0        0        0     1512 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev1/lycoris/kohya/kohya_utils.py
-drwxrwxrwx   0        0        0        0 2023-07-21 03:00:03.476420 lycoris_lora-1.8.1.dev1/lycoris/modules/
--rw-rw-rw-   0        0        0        0 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev1/lycoris/modules/__init__.py
--rw-rw-rw-   0        0        0     7334 2023-07-21 02:47:27.000000 lycoris_lora-1.8.1.dev1/lycoris/modules/attention.py
--rw-rw-rw-   0        0        0     4762 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev1/lycoris/modules/dylora.py
--rw-rw-rw-   0        0        0    10763 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev1/lycoris/modules/glokr.py
--rw-rw-rw-   0        0        0     4117 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev1/lycoris/modules/glora.py
--rw-rw-rw-   0        0        0       64 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev1/lycoris/modules/hyperlycoris.py
-drwxrwxrwx   0        0        0        0 2023-07-21 03:00:03.477421 lycoris_lora-1.8.1.dev1/lycoris/modules/hypernet/
--rw-rw-rw-   0        0        0       97 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev1/lycoris/modules/hypernet/__init__.py
--rw-rw-rw-   0        0        0     8229 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev1/lycoris/modules/hypernet/generater.py
--rw-rw-rw-   0        0        0     2103 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev1/lycoris/modules/ia3.py
--rw-rw-rw-   0        0        0    10342 2023-07-21 02:47:27.000000 lycoris_lora-1.8.1.dev1/lycoris/modules/locon.py
--rw-rw-rw-   0        0        0    10065 2023-07-21 02:47:27.000000 lycoris_lora-1.8.1.dev1/lycoris/modules/loha.py
--rw-rw-rw-   0        0        0    12646 2023-07-21 02:59:08.000000 lycoris_lora-1.8.1.dev1/lycoris/modules/lokr.py
-drwxrwxrwx   0        0        0        0 2023-07-21 03:00:03.478422 lycoris_lora-1.8.1.dev1/lycoris/utils/
--rw-rw-rw-   0        0        0    21031 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev1/lycoris/utils/__init__.py
--rw-rw-rw-   0        0        0      249 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev1/lycoris/utils/xformers_utils.py
-drwxrwxrwx   0        0        0        0 2023-07-21 03:00:03.491920 lycoris_lora-1.8.1.dev1/lycoris_lora.egg-info/
--rw-rw-rw-   0        0        0      353 2023-07-21 03:00:03.000000 lycoris_lora-1.8.1.dev1/lycoris_lora.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0     1232 2023-07-21 03:00:03.000000 lycoris_lora-1.8.1.dev1/lycoris_lora.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-21 03:00:03.000000 lycoris_lora-1.8.1.dev1/lycoris_lora.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        2 2023-03-09 13:25:15.000000 lycoris_lora-1.8.1.dev1/lycoris_lora.egg-info/not-zip-safe
--rw-rw-rw-   0        0        0       41 2023-07-21 03:00:03.000000 lycoris_lora-1.8.1.dev1/lycoris_lora.egg-info/requires.txt
--rw-rw-rw-   0        0        0        8 2023-07-21 03:00:03.000000 lycoris_lora-1.8.1.dev1/lycoris_lora.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      106 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev1/requirements.txt
--rw-rw-rw-   0        0        0       42 2023-07-21 03:00:03.494421 lycoris_lora-1.8.1.dev1/setup.cfg
--rw-rw-rw-   0        0        0      566 2023-07-21 02:59:27.000000 lycoris_lora-1.8.1.dev1/setup.py
-drwxrwxrwx   0        0        0        0 2023-07-21 03:00:03.493422 lycoris_lora-1.8.1.dev1/tools/
--rw-rw-rw-   0        0        0     4087 2023-03-12 16:11:52.000000 lycoris_lora-1.8.1.dev1/tools/extract_locon.py
--rw-rw-rw-   0        0        0     2293 2023-06-05 03:39:47.000000 lycoris_lora-1.8.1.dev1/tools/merge.py
--rw-rw-rw-   0        0        0    55333 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev1/train_hyperdream.py
+drwxrwxrwx   0        0        0        0 2023-07-23 04:03:14.411133 lycoris_lora-1.8.1.dev2/
+-rw-rw-rw-   0        0        0     1682 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/.gitignore
+-rw-rw-rw-   0        0        0     4436 2023-04-09 13:45:45.000000 lycoris_lora-1.8.1.dev2/Algo.md
+-rw-rw-rw-   0        0        0     1111 2023-07-22 06:17:56.000000 lycoris_lora-1.8.1.dev2/Change.md
+-rw-rw-rw-   0        0        0     2828 2023-03-09 12:01:15.000000 lycoris_lora-1.8.1.dev2/Demo.md
+-rw-rw-rw-   0        0        0    11545 2023-03-09 05:37:07.000000 lycoris_lora-1.8.1.dev2/LICENSE.md
+-rw-rw-rw-   0        0        0      353 2023-07-23 04:03:14.410634 lycoris_lora-1.8.1.dev2/PKG-INFO
+-rw-rw-rw-   0        0        0     7451 2023-07-22 06:17:56.000000 lycoris_lora-1.8.1.dev2/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 04:03:14.384631 lycoris_lora-1.8.1.dev2/experiments/
+-rw-rw-rw-   0        0        0     3579 2023-03-12 01:46:48.000000 lycoris_lora-1.8.1.dev2/experiments/better_conv.py
+-rw-rw-rw-   0        0        0     1967 2023-03-12 01:46:43.000000 lycoris_lora-1.8.1.dev2/experiments/better_conv_extract.py
+-rw-rw-rw-   0        0        0      651 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/experiments/compare_norm.py
+-rw-rw-rw-   0        0        0     8783 2023-03-12 03:21:33.000000 lycoris_lora-1.8.1.dev2/experiments/concept_neuron.py
+-rw-rw-rw-   0        0        0      894 2023-03-09 14:26:54.000000 lycoris_lora-1.8.1.dev2/experiments/locon_extract_test.py
+-rw-rw-rw-   0        0        0      755 2023-03-10 15:36:09.000000 lycoris_lora-1.8.1.dev2/experiments/locon_merge_test.py
+-rw-rw-rw-   0        0        0     1028 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/experiments/loha_svd.py
+-rw-rw-rw-   0        0        0     3411 2023-03-09 05:37:07.000000 lycoris_lora-1.8.1.dev2/experiments/singular_value_test.py
+-rw-rw-rw-   0        0        0     2334 2023-03-11 09:28:26.000000 lycoris_lora-1.8.1.dev2/experiments/sparse_bias_test.py
+-rw-rw-rw-   0        0        0     2791 2023-03-12 01:46:48.000000 lycoris_lora-1.8.1.dev2/experiments/time_test.py
+-rw-rw-rw-   0        0        0      255 2023-06-25 07:25:35.000000 lycoris_lora-1.8.1.dev2/experiments/weakre_speed.py
+-rw-rw-rw-   0        0        0     4116 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/hyperdream_gen_weight.py
+drwxrwxrwx   0        0        0        0 2023-07-23 04:03:14.385632 lycoris_lora-1.8.1.dev2/lycoris/
+-rw-rw-rw-   0        0        0       55 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/lycoris/__init__.py
+-rw-rw-rw-   0        0        0     2699 2023-07-23 03:48:18.000000 lycoris_lora-1.8.1.dev2/lycoris/config.py
+drwxrwxrwx   0        0        0        0 2023-07-23 04:03:14.387131 lycoris_lora-1.8.1.dev2/lycoris/kohya/
+-rw-rw-rw-   0        0        0    39941 2023-07-23 04:02:52.000000 lycoris_lora-1.8.1.dev2/lycoris/kohya/__init__.py
+-rw-rw-rw-   0        0        0    48868 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/lycoris/kohya/kohya_model_utils.py
+-rw-rw-rw-   0        0        0     1512 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/lycoris/kohya/kohya_utils.py
+drwxrwxrwx   0        0        0        0 2023-07-23 04:03:14.392131 lycoris_lora-1.8.1.dev2/lycoris/modules/
+-rw-rw-rw-   0        0        0        0 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/lycoris/modules/__init__.py
+-rw-rw-rw-   0        0        0     7334 2023-07-22 06:17:56.000000 lycoris_lora-1.8.1.dev2/lycoris/modules/attention.py
+-rw-rw-rw-   0        0        0     4762 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/lycoris/modules/dylora.py
+-rw-rw-rw-   0        0        0    10763 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/lycoris/modules/glokr.py
+-rw-rw-rw-   0        0        0     4117 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/lycoris/modules/glora.py
+-rw-rw-rw-   0        0        0       64 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/lycoris/modules/hyperlycoris.py
+drwxrwxrwx   0        0        0        0 2023-07-23 04:03:14.393132 lycoris_lora-1.8.1.dev2/lycoris/modules/hypernet/
+-rw-rw-rw-   0        0        0       97 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/lycoris/modules/hypernet/__init__.py
+-rw-rw-rw-   0        0        0     8229 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/lycoris/modules/hypernet/generater.py
+-rw-rw-rw-   0        0        0     2103 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/lycoris/modules/ia3.py
+-rw-rw-rw-   0        0        0    10342 2023-07-22 06:17:56.000000 lycoris_lora-1.8.1.dev2/lycoris/modules/locon.py
+-rw-rw-rw-   0        0        0    10065 2023-07-22 06:17:56.000000 lycoris_lora-1.8.1.dev2/lycoris/modules/loha.py
+-rw-rw-rw-   0        0        0    12647 2023-07-22 06:17:56.000000 lycoris_lora-1.8.1.dev2/lycoris/modules/lokr.py
+drwxrwxrwx   0        0        0        0 2023-07-23 04:03:14.394631 lycoris_lora-1.8.1.dev2/lycoris/utils/
+-rw-rw-rw-   0        0        0    21031 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/lycoris/utils/__init__.py
+-rw-rw-rw-   0        0        0       41 2023-07-23 03:53:39.000000 lycoris_lora-1.8.1.dev2/lycoris/utils/preset.py
+-rw-rw-rw-   0        0        0      249 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/lycoris/utils/xformers_utils.py
+drwxrwxrwx   0        0        0        0 2023-07-23 04:03:14.408634 lycoris_lora-1.8.1.dev2/lycoris_lora.egg-info/
+-rw-rw-rw-   0        0        0      353 2023-07-23 04:03:14.000000 lycoris_lora-1.8.1.dev2/lycoris_lora.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0     1256 2023-07-23 04:03:14.000000 lycoris_lora-1.8.1.dev2/lycoris_lora.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 04:03:14.000000 lycoris_lora-1.8.1.dev2/lycoris_lora.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        2 2023-03-09 13:25:15.000000 lycoris_lora-1.8.1.dev2/lycoris_lora.egg-info/not-zip-safe
+-rw-rw-rw-   0        0        0       41 2023-07-23 04:03:14.000000 lycoris_lora-1.8.1.dev2/lycoris_lora.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        8 2023-07-23 04:03:14.000000 lycoris_lora-1.8.1.dev2/lycoris_lora.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      106 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/requirements.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 04:03:14.411133 lycoris_lora-1.8.1.dev2/setup.cfg
+-rw-rw-rw-   0        0        0      566 2023-07-23 04:03:10.000000 lycoris_lora-1.8.1.dev2/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 04:03:14.409634 lycoris_lora-1.8.1.dev2/tools/
+-rw-rw-rw-   0        0        0     4093 2023-07-23 03:43:26.000000 lycoris_lora-1.8.1.dev2/tools/extract_locon.py
+-rw-rw-rw-   0        0        0     2299 2023-07-23 03:43:55.000000 lycoris_lora-1.8.1.dev2/tools/merge.py
+-rw-rw-rw-   0        0        0    55333 2023-07-19 08:00:19.000000 lycoris_lora-1.8.1.dev2/train_hyperdream.py
```

### Comparing `lycoris_lora-1.8.1.dev1/.gitignore` & `lycoris_lora-1.8.1.dev2/.gitignore`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev1/Algo.md` & `lycoris_lora-1.8.1.dev2/Algo.md`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev1/Change.md` & `lycoris_lora-1.8.1.dev2/Change.md`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev1/Demo.md` & `lycoris_lora-1.8.1.dev2/Demo.md`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev1/LICENSE.md` & `lycoris_lora-1.8.1.dev2/LICENSE.md`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev1/README.md` & `lycoris_lora-1.8.1.dev2/README.md`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev1/experiments/better_conv.py` & `lycoris_lora-1.8.1.dev2/experiments/better_conv.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev1/experiments/better_conv_extract.py` & `lycoris_lora-1.8.1.dev2/experiments/better_conv_extract.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev1/experiments/compare_norm.py` & `lycoris_lora-1.8.1.dev2/experiments/compare_norm.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev1/experiments/concept_neuron.py` & `lycoris_lora-1.8.1.dev2/experiments/concept_neuron.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev1/experiments/locon_extract_test.py` & `lycoris_lora-1.8.1.dev2/experiments/locon_extract_test.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev1/experiments/locon_merge_test.py` & `lycoris_lora-1.8.1.dev2/experiments/locon_merge_test.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev1/experiments/loha_svd.py` & `lycoris_lora-1.8.1.dev2/experiments/loha_svd.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev1/experiments/singular_value_test.py` & `lycoris_lora-1.8.1.dev2/experiments/singular_value_test.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev1/experiments/sparse_bias_test.py` & `lycoris_lora-1.8.1.dev2/experiments/sparse_bias_test.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev1/experiments/time_test.py` & `lycoris_lora-1.8.1.dev2/experiments/time_test.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev1/hyperdream_gen_weight.py` & `lycoris_lora-1.8.1.dev2/hyperdream_gen_weight.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev1/lycoris/config.py` & `lycoris_lora-1.8.1.dev2/lycoris/config.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,13 +1,12 @@
 PRESET = {
     'full':{
         'enable_conv': True,
         'unet_target_module':[
             "Transformer2DModel", 
-            "Attention", 
             "ResnetBlock2D", 
             "Downsample2D", 
             "Upsample2D"
         ],
         'unet_target_name':[
             "conv_in",
             "conv_out",
@@ -19,38 +18,47 @@
         ],
         'text_encoder_target_name': [],
     },
     'full-lin':{
         'enable_conv': False,
         'unet_target_module':[
             "Transformer2DModel", 
-            "Attention", 
             "ResnetBlock2D",
         ],
         'unet_target_name':[
             "time_embedding.linear_1",
             "time_embedding.linear_2",
         ],
         'text_encoder_target_module': [
             "CLIPAttention", "CLIPMLP"
         ],
         'text_encoder_target_name': [],
     },
-    'lora':{
+    'attn-mlp':{
         'enable_conv': False,
         'unet_target_module':[
             "Transformer2DModel", 
-            "Attention", 
         ],
         'unet_target_name':[],
         'text_encoder_target_module': [
             "CLIPAttention", "CLIPMLP"
         ],
         'text_encoder_target_name': [],
     },
+    'attn-only':{
+        'enable_conv': False,
+        'unet_target_module':[
+            "CrossAttention", 
+        ],
+        'unet_target_name':[],
+        'text_encoder_target_module': [
+            "CLIPAttention"
+        ],
+        'text_encoder_target_name': [],
+    },
     'unet-only':{
         'enable_conv': True,
         'unet_target_module':[
             "Transformer2DModel", 
             "Attention", 
             "ResnetBlock2D", 
             "Downsample2D", 
@@ -65,15 +73,14 @@
         'text_encoder_target_module': [],
         'text_encoder_target_name': [],
     },
     'unet-transformer-only':{
         'enable_conv': False,
         'unet_target_module':[
             "Transformer2DModel", 
-            "Attention", 
         ],
         'unet_target_name':[],
         'text_encoder_target_module': [],
         'text_encoder_target_name': [],
     },
     'unet-convblock-only':{
         'enable_conv': True,
```

### Comparing `lycoris_lora-1.8.1.dev1/lycoris/kohya/__init__.py` & `lycoris_lora-1.8.1.dev2/lycoris/kohya/__init__.py`

 * *Files 6% similar despite different names*

```diff
@@ -16,14 +16,17 @@
 from ..modules.loha import LohaModule
 from ..modules.ia3 import IA3Module
 from ..modules.lokr import LokrModule
 from ..modules.dylora import DyLoraModule
 from ..modules.glora import GLoRAModule
 from ..modules.hypernet import ImgWeightGenerator
 
+from ..config import PRESET
+from ..utils.preset import read_preset
+
 
 def create_network(multiplier, network_dim, network_alpha, vae, text_encoder, unet, **kwargs):
     if network_dim is None:
         network_dim = 4                     # default
     conv_dim = int(kwargs.get('conv_dim', network_dim) or network_dim)
     conv_alpha = float(kwargs.get('conv_alpha', network_alpha) or network_alpha)
     dropout = float(kwargs.get('dropout', 0.) or 0.)
@@ -39,23 +42,30 @@
         'loha': LohaModule,
         'ia3':  IA3Module,
         'lokr': LokrModule,
         'dylora': DyLoraModule,
         'glora': GLoRAModule,
     }[algo]
     
+    preset = kwargs.get('preset', {})
+    if preset not in PRESET:
+        preset = read_preset(preset)
+    else:
+        preset = PRESET[preset]
+    assert preset is not None
+    LycorisNetwork.apply_preset(preset)
+    
     print(f'Using rank adaptation algo: {algo}')
     
-    if ((algo == 'loha' or algo == 'lokr')
+    if ((algo == 'loha')
         and not kwargs.get('no_dim_warn', False) 
         and (network_dim>64 or conv_dim>64)):
         print('='*20 + 'WARNING' + '='*20)
         warning_type ={
-            'loha': "Hadamard Product representation",
-            'lokr': "Kronecker Product representation"
+            'loha': "Hadamard Product representation"
         }
         warning_msg = f"""You are not supposed to use dim>64 (64*64 = 4096, it already has enough rank)\n
             in {warning_type[algo]}!\n
             Please consider use lower dim or disable this warning with --network_args no_dim_warn=True\n
             If you just want to use high dim {algo}, please consider use lower lr.
         """
         warn(warning_msg, stacklevel=2)
@@ -123,30 +133,50 @@
 
 
 class LycorisNetwork(torch.nn.Module):
     '''
     LoRA + LoCon
     '''
     # Ignore proj_in or proj_out, their channels is only a few.
+    ENABLE_CONV = True
     UNET_TARGET_REPLACE_MODULE = [
         "Transformer2DModel", 
-        "Attention", 
         "ResnetBlock2D", 
         "Downsample2D", 
         "Upsample2D"
     ]
     UNET_TARGET_REPLACE_NAME = [
         "conv_in",
         "conv_out",
         "time_embedding.linear_1",
         "time_embedding.linear_2",
     ]
     TEXT_ENCODER_TARGET_REPLACE_MODULE = ["CLIPAttention", "CLIPMLP"]
     LORA_PREFIX_UNET = 'lora_unet'
     LORA_PREFIX_TEXT_ENCODER = 'lora_te'
+    MODULE_ALGO_MAP = {}
+    NAME_ALGO_MAP = {}
+
+    @classmethod
+    def apply_preset(cls, preset):
+        if 'enable_conv' in preset:
+            cls.ENABLE_CONV = preset['enable_conv']
+        if 'unet_target_module' in preset:
+            cls.UNET_TARGET_REPLACE_MODULE = preset['unet_target_module']
+        if 'unet_target_name' in preset:
+            cls.UNET_TARGET_REPLACE_NAME = preset['unet_target_name']
+        if 'text_encoder_target_module' in preset:
+            cls.TEXT_ENCODER_TARGET_REPLACE_MODULE = preset['text_encoder_target_module']
+        if 'text_encoder_target_name' in preset:
+            cls.TEXT_ENCODER_TARGET_REPLACE_NAME = preset['text_encoder_target_name']
+        if 'module_algo_map' in preset:
+            cls.MODULE_ALGO_MAP = preset['module_algo_map']
+        if 'name_algo_map' in preset:
+            cls.NAME_ALGO_MAP = preset['name_algo_map']
+        return cls
 
     def __init__(
         self, 
         text_encoder, unet, 
         multiplier=1.0, 
         lora_dim=4, conv_lora_dim=4, 
         alpha=1, conv_alpha=1,
@@ -154,22 +184,28 @@
         dropout = 0, rank_dropout = 0, module_dropout = 0,
         network_module = LoConModule,
         **kwargs,
     ) -> None:
         super().__init__()
         self.multiplier = multiplier
         self.lora_dim = lora_dim
+        
+        if not self.ENABLE_CONV:
+            conv_lora_dim = 0
+        
         self.conv_lora_dim = int(conv_lora_dim)
-        if self.conv_lora_dim != self.lora_dim: 
+        if self.conv_lora_dim and self.conv_lora_dim != self.lora_dim: 
             print('Apply different lora dim for conv layer')
             print(f'Conv Dim: {conv_lora_dim}, Linear Dim: {lora_dim}')
-            
+        elif self.conv_lora_dim == 0:
+            print('Disable conv layer')
+        
         self.alpha = alpha
         self.conv_alpha = float(conv_alpha)
-        if self.alpha != self.conv_alpha: 
+        if self.conv_lora_dim and self.alpha != self.conv_alpha: 
             print('Apply different alpha value for conv layer')
             print(f'Conv alpha: {conv_alpha}, Linear alpha: {alpha}')
         
         if 1 >= dropout >= 0:
             print(f'Use Dropout value: {dropout}')
         self.dropout = dropout
         self.rank_dropout = rank_dropout
@@ -181,72 +217,81 @@
             root_module: torch.nn.Module, 
             target_replace_modules,
             target_replace_names = []
         ) -> List[network_module]:
             print('Create LyCORIS Module')
             loras = []
             for name, module in root_module.named_modules():
-                if module.__class__.__name__ in target_replace_modules:
+                module_name = module.__class__.__name__
+                if module_name in target_replace_modules:
+                    if module_name in self.MODULE_ALGO_MAP:
+                        algo = self.MODULE_ALGO_MAP[module_name]
+                    else:
+                        algo = network_module
                     for child_name, child_module in module.named_modules():
                         lora_name = prefix + '.' + name + '.' + child_name
                         lora_name = lora_name.replace('.', '_')
                         if child_module.__class__.__name__ == 'Linear' and lora_dim>0:
-                            lora = network_module(
+                            lora = algo(
                                 lora_name, child_module, self.multiplier, 
                                 self.lora_dim, self.alpha, 
                                 self.dropout, self.rank_dropout, self.module_dropout, 
                                 use_cp,
                                 **kwargs
                             )
                         elif child_module.__class__.__name__ == 'Conv2d':
                             k_size, *_ = child_module.kernel_size
                             if k_size==1 and lora_dim>0:
-                                lora = network_module(
+                                lora = algo(
                                     lora_name, child_module, self.multiplier, 
                                     self.lora_dim, self.alpha, 
                                     self.dropout, self.rank_dropout, self.module_dropout, 
                                     use_cp,
                                     **kwargs
                                 )
                             elif conv_lora_dim>0:
-                                lora = network_module(
+                                lora = algo(
                                     lora_name, child_module, self.multiplier, 
                                     self.conv_lora_dim, self.conv_alpha, 
                                     self.dropout, self.rank_dropout, self.module_dropout, 
                                     use_cp,
                                     **kwargs
                                 )
                             else:
                                 continue
                         else:
                             continue
                         loras.append(lora)
                 elif name in target_replace_names:
+                    if name in self.NAME_ALGO_MAP:
+                        algo = self.NAME_ALGO_MAP[name]
+                    else:
+                        algo = network_module
                     lora_name = prefix + '.' + name
                     lora_name = lora_name.replace('.', '_')
                     if module.__class__.__name__ == 'Linear' and lora_dim>0:
-                        lora = network_module(
+                        lora = algo(
                             lora_name, module, self.multiplier, 
                             self.lora_dim, self.alpha, 
                             self.dropout, self.rank_dropout, self.module_dropout, 
                             use_cp,
                             **kwargs
                         )
                     elif module.__class__.__name__ == 'Conv2d':
                         k_size, *_ = module.kernel_size
                         if k_size==1 and lora_dim>0:
-                            lora = network_module(
+                            lora = algo(
                                 lora_name, module, self.multiplier, 
                                 self.lora_dim, self.alpha, 
                                 self.dropout, self.rank_dropout, self.module_dropout, 
                                 use_cp,
                                 **kwargs
                             )
                         elif conv_lora_dim>0:
-                            lora = network_module(
+                            lora = algo(
                                 lora_name, module, self.multiplier, 
                                 self.conv_lora_dim, self.conv_alpha, 
                                 self.dropout, self.rank_dropout, self.module_dropout, 
                                 use_cp,
                                 **kwargs
                             )
                         else:
```

### Comparing `lycoris_lora-1.8.1.dev1/lycoris/kohya/kohya_model_utils.py` & `lycoris_lora-1.8.1.dev2/lycoris/kohya/kohya_model_utils.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev1/lycoris/kohya/kohya_utils.py` & `lycoris_lora-1.8.1.dev2/lycoris/kohya/kohya_utils.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev1/lycoris/modules/attention.py` & `lycoris_lora-1.8.1.dev2/lycoris/modules/attention.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev1/lycoris/modules/dylora.py` & `lycoris_lora-1.8.1.dev2/lycoris/modules/dylora.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev1/lycoris/modules/glokr.py` & `lycoris_lora-1.8.1.dev2/lycoris/modules/glokr.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev1/lycoris/modules/glora.py` & `lycoris_lora-1.8.1.dev2/lycoris/modules/glora.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev1/lycoris/modules/hypernet/generater.py` & `lycoris_lora-1.8.1.dev2/lycoris/modules/hypernet/generater.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev1/lycoris/modules/ia3.py` & `lycoris_lora-1.8.1.dev2/lycoris/modules/ia3.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev1/lycoris/modules/locon.py` & `lycoris_lora-1.8.1.dev2/lycoris/modules/locon.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev1/lycoris/modules/loha.py` & `lycoris_lora-1.8.1.dev2/lycoris/modules/loha.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev1/lycoris/modules/lokr.py` & `lycoris_lora-1.8.1.dev2/lycoris/modules/lokr.py`

 * *Files 0% similar despite different names*

```diff
@@ -247,15 +247,15 @@
         destination[f'{prefix}alpha'] = self.alpha
         if self.use_w1:
             destination[f'{prefix}lokr_w1'] = self.lokr_w1 * self.scalar
         else:
             destination[f'{prefix}lokr_w1_a'] = self.lokr_w1_a * self.scalar
             destination[f'{prefix}lokr_w1_b'] = self.lokr_w1_b
         
-        if self.use_2:
+        if self.use_w2:
             destination[f'{prefix}lokr_w2'] = self.lokr_w2
         else:
             destination[f'{prefix}lokr_w2_a'] = self.lokr_w2_a
             destination[f'{prefix}lokr_w2_b'] = self.lokr_w2_b
             if self.cp:
                 destination[f'{prefix}lokr_t2'] = self.lokr_t2
         return destination
```

### Comparing `lycoris_lora-1.8.1.dev1/lycoris/utils/__init__.py` & `lycoris_lora-1.8.1.dev2/lycoris/utils/__init__.py`

 * *Files identical despite different names*

### Comparing `lycoris_lora-1.8.1.dev1/lycoris_lora.egg-info/SOURCES.txt` & `lycoris_lora-1.8.1.dev2/lycoris_lora.egg-info/SOURCES.txt`

 * *Files 4% similar despite different names*

```diff
@@ -33,14 +33,15 @@
 lycoris/modules/ia3.py
 lycoris/modules/locon.py
 lycoris/modules/loha.py
 lycoris/modules/lokr.py
 lycoris/modules/hypernet/__init__.py
 lycoris/modules/hypernet/generater.py
 lycoris/utils/__init__.py
+lycoris/utils/preset.py
 lycoris/utils/xformers_utils.py
 lycoris_lora.egg-info/PKG-INFO
 lycoris_lora.egg-info/SOURCES.txt
 lycoris_lora.egg-info/dependency_links.txt
 lycoris_lora.egg-info/not-zip-safe
 lycoris_lora.egg-info/requires.txt
 lycoris_lora.egg-info/top_level.txt
```

### Comparing `lycoris_lora-1.8.1.dev1/setup.py` & `lycoris_lora-1.8.1.dev2/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 from setuptools import setup, find_packages
 
 setup(
     name='lycoris_lora',
     packages=find_packages(),
-    version='1.8.1.dev1',
+    version='1.8.1.dev2',
     url='https://github.com/KohakuBlueleaf/LyCORIS',
     description='Lora beYond Conventional methods, Other Rank adaptation Implementations for Stable diffusion',
     author='Shih-Ying Yeh(KohakuBlueLeaf), Yu-Guan Hsieh, Zhidong Gao',
     author_email='apolloyeh0123@gmail.com',
     zip_safe=False,
     install_requires=[
         'torch',
```

### Comparing `lycoris_lora-1.8.1.dev1/tools/extract_locon.py` & `lycoris_lora-1.8.1.dev2/tools/extract_locon.py`

 * *Files 0% similar despite different names*

```diff
@@ -82,15 +82,15 @@
         default=False, action="store_true"
     )
     return parser.parse_args()
 ARGS = get_args()
 
 
 from lycoris.utils import extract_diff
-from lycoris.kohya_model_utils import load_models_from_stable_diffusion_checkpoint
+from lycoris.kohya.kohya_model_utils import load_models_from_stable_diffusion_checkpoint
 
 import torch
 from safetensors.torch import save_file
 
 
 def main():
     args = ARGS
```

### Comparing `lycoris_lora-1.8.1.dev1/tools/merge.py` & `lycoris_lora-1.8.1.dev2/tools/merge.py`

 * *Files 1% similar despite different names*

```diff
@@ -34,15 +34,15 @@
         default='1.0', type=float
     )
     return parser.parse_args()
 ARGS = get_args()
 
 
 from lycoris.utils import merge
-from lycoris.kohya_model_utils import (
+from lycoris.kohya.kohya_model_utils import (
     load_models_from_stable_diffusion_checkpoint,
     save_stable_diffusion_checkpoint,
     load_file
 )
 
 import torch
```

### Comparing `lycoris_lora-1.8.1.dev1/train_hyperdream.py` & `lycoris_lora-1.8.1.dev2/train_hyperdream.py`

 * *Files identical despite different names*

