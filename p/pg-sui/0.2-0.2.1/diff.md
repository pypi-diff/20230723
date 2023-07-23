# Comparing `tmp/PG-SUI-0.2.tar.gz` & `tmp/pg-sui-0.2.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "PG-SUI-0.2.tar", last modified: Sun Jul 23 01:21:43 2023, max compression
+gzip compressed data, was "pg-sui-0.2.1.tar", last modified: Sun Jul 23 01:53:48 2023, max compression
```

## Comparing `PG-SUI-0.2.tar` & `pg-sui-0.2.1.tar`

### file list

```diff
@@ -1,99 +1,99 @@
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:21:43.380612 PG-SUI-0.2/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)      220 2023-07-22 21:23:30.000000 PG-SUI-0.2/MANIFEST.in
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:21:40.360320 PG-SUI-0.2/PG_SUI.egg-info/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    13621 2023-07-23 01:21:38.000000 PG-SUI-0.2/PG_SUI.egg-info/PKG-INFO
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     3001 2023-07-23 01:21:39.000000 PG-SUI-0.2/PG_SUI.egg-info/SOURCES.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        1 2023-07-23 01:21:38.000000 PG-SUI-0.2/PG_SUI.egg-info/dependency_links.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)      331 2023-07-23 01:21:38.000000 PG-SUI-0.2/PG_SUI.egg-info/requires.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)       22 2023-07-23 01:21:38.000000 PG-SUI-0.2/PG_SUI.egg-info/top_level.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    13621 2023-07-23 01:21:43.370568 PG-SUI-0.2/PKG-INFO
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    10442 2023-07-22 23:34:21.000000 PG-SUI-0.2/README.md
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:21:40.405003 PG-SUI-0.2/pgsui/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     1449 2023-07-20 21:13:19.000000 PG-SUI-0.2/pgsui/__init__.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:21:40.460323 PG-SUI-0.2/pgsui/data_processing/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 PG-SUI-0.2/pgsui/data_processing/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    42452 2023-07-20 21:28:41.000000 PG-SUI-0.2/pgsui/data_processing/transformers.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:21:40.490023 PG-SUI-0.2/pgsui/example_data/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 PG-SUI-0.2/pgsui/example_data/__init__.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:21:40.745134 PG-SUI-0.2/pgsui/example_data/phylip_files/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 PG-SUI-0.2/pgsui/example_data/phylip_files/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)   238537 2023-07-16 18:34:38.000000 PG-SUI-0.2/pgsui/example_data/phylip_files/test.phy
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2897 2023-07-16 18:34:38.000000 PG-SUI-0.2/pgsui/example_data/phylip_files/test_n10.phy
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    13428 2023-07-16 18:34:38.000000 PG-SUI-0.2/pgsui/example_data/phylip_files/test_n100.phy
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     1960 2023-07-16 18:34:38.000000 PG-SUI-0.2/pgsui/example_data/phylip_files/test_n2.phy
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    60228 2023-07-16 18:34:38.000000 PG-SUI-0.2/pgsui/example_data/phylip_files/test_n500.phy
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:21:40.824998 PG-SUI-0.2/pgsui/example_data/popmaps/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 PG-SUI-0.2/pgsui/example_data/popmaps/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     1954 2023-07-16 18:34:38.000000 PG-SUI-0.2/pgsui/example_data/popmaps/test.popmap
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:21:41.190425 PG-SUI-0.2/pgsui/example_data/structure_files/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 PG-SUI-0.2/pgsui/example_data/structure_files/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     6375 2023-07-16 18:34:38.000000 PG-SUI-0.2/pgsui/example_data/structure_files/test.nopops.1row.10sites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    50808 2023-07-16 18:34:38.000000 PG-SUI-0.2/pgsui/example_data/structure_files/test.nopops.2row.100sites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     7978 2023-07-16 18:34:38.000000 PG-SUI-0.2/pgsui/example_data/structure_files/test.nopops.2row.10sites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    17512 2023-07-16 18:34:38.000000 PG-SUI-0.2/pgsui/example_data/structure_files/test.nopops.2row.30sites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)   967410 2023-07-16 18:34:38.000000 PG-SUI-0.2/pgsui/example_data/structure_files/test.nopops.2row.allsites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     6609 2023-07-16 18:34:38.000000 PG-SUI-0.2/pgsui/example_data/structure_files/test.pops.1row.10sites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     8446 2023-07-16 18:34:38.000000 PG-SUI-0.2/pgsui/example_data/structure_files/test.pops.2row.10sites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)   967878 2023-07-16 18:34:38.000000 PG-SUI-0.2/pgsui/example_data/structure_files/test.pops.2row.allsites.str
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:21:41.891122 PG-SUI-0.2/pgsui/example_data/trees/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 PG-SUI-0.2/pgsui/example_data/trees/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    25575 2023-07-16 18:34:38.000000 PG-SUI-0.2/pgsui/example_data/trees/test.iqtree
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)      134 2023-07-16 18:34:38.000000 PG-SUI-0.2/pgsui/example_data/trees/test.qmat
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    46013 2023-07-16 18:34:38.000000 PG-SUI-0.2/pgsui/example_data/trees/test.rate
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     4696 2023-07-16 18:34:38.000000 PG-SUI-0.2/pgsui/example_data/trees/test.tre
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)      678 2023-07-16 18:34:38.000000 PG-SUI-0.2/pgsui/example_data/trees/test_n10.rate
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2577 2023-07-16 18:34:38.000000 PG-SUI-0.2/pgsui/example_data/trees/test_n100.rate
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    11387 2023-07-16 18:34:38.000000 PG-SUI-0.2/pgsui/example_data/trees/test_n500.rate
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    16235 2023-07-16 18:34:38.000000 PG-SUI-0.2/pgsui/example_data/trees/test_siterates.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)       80 2023-07-16 18:34:38.000000 PG-SUI-0.2/pgsui/example_data/trees/test_siterates_n10.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)      804 2023-07-16 18:34:38.000000 PG-SUI-0.2/pgsui/example_data/trees/test_siterates_n100.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     4008 2023-07-16 18:34:38.000000 PG-SUI-0.2/pgsui/example_data/trees/test_siterates_n500.txt
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:21:42.020529 PG-SUI-0.2/pgsui/example_data/vcf_files/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)   380243 2023-07-16 18:34:38.000000 PG-SUI-0.2/pgsui/example_data/vcf_files/test.vcf
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    72705 2023-07-16 18:34:43.000000 PG-SUI-0.2/pgsui/example_data/vcf_files/test.vcf.gz
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2581 2023-07-16 18:34:43.000000 PG-SUI-0.2/pgsui/example_data/vcf_files/test.vcf.gz.tbi
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:21:42.155261 PG-SUI-0.2/pgsui/impute/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 PG-SUI-0.2/pgsui/impute/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)   124991 2023-07-22 22:30:11.000000 PG-SUI-0.2/pgsui/impute/estimators.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    51210 2023-07-20 21:29:54.000000 PG-SUI-0.2/pgsui/impute/impute.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    53283 2023-07-20 21:27:33.000000 PG-SUI-0.2/pgsui/impute/simple_imputers.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:21:42.245146 PG-SUI-0.2/pgsui/impute/supervised/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-15 05:58:52.000000 PG-SUI-0.2/pgsui/impute/supervised/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    35075 2023-07-21 16:54:38.000000 PG-SUI-0.2/pgsui/impute/supervised/iterative_imputer_fixedparams.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    45443 2023-07-21 03:30:57.000000 PG-SUI-0.2/pgsui/impute/supervised/iterative_imputer_gridsearch.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:21:42.615723 PG-SUI-0.2/pgsui/impute/unsupervised/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-15 05:58:52.000000 PG-SUI-0.2/pgsui/impute/unsupervised/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     9682 2023-07-20 20:38:09.000000 PG-SUI-0.2/pgsui/impute/unsupervised/callbacks.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    29483 2023-07-21 03:31:57.000000 PG-SUI-0.2/pgsui/impute/unsupervised/keras_classifiers.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:21:42.815711 PG-SUI-0.2/pgsui/impute/unsupervised/models/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-15 05:58:52.000000 PG-SUI-0.2/pgsui/impute/unsupervised/models/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    20161 2023-07-22 20:36:22.000000 PG-SUI-0.2/pgsui/impute/unsupervised/models/autoencoder_model.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:21:42.990434 PG-SUI-0.2/pgsui/impute/unsupervised/models/in_development/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-15 05:58:52.000000 PG-SUI-0.2/pgsui/impute/unsupervised/models/in_development/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    15036 2023-07-16 18:34:38.000000 PG-SUI-0.2/pgsui/impute/unsupervised/models/in_development/cnn_model.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14501 2023-07-21 04:19:01.000000 PG-SUI-0.2/pgsui/impute/unsupervised/models/nlpca_model.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    37879 2023-07-21 04:21:34.000000 PG-SUI-0.2/pgsui/impute/unsupervised/models/ubp_model.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    22338 2023-07-21 04:23:07.000000 PG-SUI-0.2/pgsui/impute/unsupervised/models/vae_model.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    52292 2023-07-19 00:32:53.000000 PG-SUI-0.2/pgsui/impute/unsupervised/neural_network_imputers.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    50830 2023-07-20 21:26:23.000000 PG-SUI-0.2/pgsui/impute/unsupervised/neural_network_methods.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     7471 2023-07-20 21:22:10.000000 PG-SUI-0.2/pgsui/pg_sui.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:21:43.185647 PG-SUI-0.2/pgsui/utils/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 PG-SUI-0.2/pgsui/utils/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    15705 2023-07-20 21:31:57.000000 PG-SUI-0.2/pgsui/utils/misc.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    33748 2023-07-21 04:25:34.000000 PG-SUI-0.2/pgsui/utils/plotting.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    26862 2023-07-19 00:15:22.000000 PG-SUI-0.2/pgsui/utils/scorers.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    10143 2023-07-16 18:34:39.000000 PG-SUI-0.2/pgsui/utils/sequence_tools.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     1867 2023-07-22 23:39:06.000000 PG-SUI-0.2/pyproject.toml
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)       38 2023-07-23 01:21:43.380612 PG-SUI-0.2/setup.cfg
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2553 2023-07-22 21:22:27.000000 PG-SUI-0.2/setup.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:21:43.242371 PG-SUI-0.2/simulation/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 PG-SUI-0.2/simulation/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    11345 2023-07-16 18:34:39.000000 PG-SUI-0.2/simulation/sim_benchmarks.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    13793 2023-07-16 18:34:39.000000 PG-SUI-0.2/simulation/sim_treeparams.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:21:43.350491 PG-SUI-0.2/test/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-15 05:58:52.000000 PG-SUI-0.2/test/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     6024 2023-07-16 18:34:39.000000 PG-SUI-0.2/test/pg_sui_simtest.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    15871 2023-07-16 18:34:39.000000 PG-SUI-0.2/test/pg_sui_testing.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     5034 2023-07-20 21:32:52.000000 PG-SUI-0.2/test/test.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14310 2023-07-16 18:34:39.000000 PG-SUI-0.2/test/test_pgsui.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     5867 2023-07-19 15:22:02.000000 PG-SUI-0.2/test/test_tkc.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:48.794195 pg-sui-0.2.1/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)      220 2023-07-22 21:23:30.000000 pg-sui-0.2.1/MANIFEST.in
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:46.483956 pg-sui-0.2.1/PG_SUI.egg-info/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14100 2023-07-23 01:53:44.000000 pg-sui-0.2.1/PG_SUI.egg-info/PKG-INFO
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     3150 2023-07-23 01:53:45.000000 pg-sui-0.2.1/PG_SUI.egg-info/SOURCES.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        1 2023-07-23 01:53:44.000000 pg-sui-0.2.1/PG_SUI.egg-info/dependency_links.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)      331 2023-07-23 01:53:44.000000 pg-sui-0.2.1/PG_SUI.egg-info/requires.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)       22 2023-07-23 01:53:44.000000 pg-sui-0.2.1/PG_SUI.egg-info/top_level.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14100 2023-07-23 01:53:48.794195 pg-sui-0.2.1/PKG-INFO
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    10442 2023-07-22 23:34:21.000000 pg-sui-0.2.1/README.md
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:46.573944 pg-sui-0.2.1/pgsui/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     1449 2023-07-20 21:13:19.000000 pg-sui-0.2.1/pgsui/__init__.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:46.619172 pg-sui-0.2.1/pgsui/data_processing/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.1/pgsui/data_processing/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    42452 2023-07-20 21:28:41.000000 pg-sui-0.2.1/pgsui/data_processing/transformers.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:46.648789 pg-sui-0.2.1/pgsui/example_data/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.1/pgsui/example_data/__init__.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:46.844076 pg-sui-0.2.1/pgsui/example_data/phylip_files/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.1/pgsui/example_data/phylip_files/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)   238537 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/phylip_files/test.phy
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2897 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/phylip_files/test_n10.phy
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    13428 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/phylip_files/test_n100.phy
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     1960 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/phylip_files/test_n2.phy
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    60228 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/phylip_files/test_n500.phy
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:46.908867 pg-sui-0.2.1/pgsui/example_data/popmaps/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.1/pgsui/example_data/popmaps/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     1954 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/popmaps/test.popmap
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:47.209025 pg-sui-0.2.1/pgsui/example_data/structure_files/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.1/pgsui/example_data/structure_files/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     6375 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/structure_files/test.nopops.1row.10sites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    50808 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/structure_files/test.nopops.2row.100sites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     7978 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/structure_files/test.nopops.2row.10sites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    17512 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/structure_files/test.nopops.2row.30sites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)   967410 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/structure_files/test.nopops.2row.allsites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     6609 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/structure_files/test.pops.1row.10sites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     8446 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/structure_files/test.pops.2row.10sites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)   967878 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/structure_files/test.pops.2row.allsites.str
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:47.629298 pg-sui-0.2.1/pgsui/example_data/trees/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.1/pgsui/example_data/trees/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    25575 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/trees/test.iqtree
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)      134 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/trees/test.qmat
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    46013 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/trees/test.rate
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     4696 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/trees/test.tre
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)      678 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/trees/test_n10.rate
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2577 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/trees/test_n100.rate
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    11387 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/trees/test_n500.rate
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    16235 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/trees/test_siterates.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)       80 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/trees/test_siterates_n10.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)      804 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/trees/test_siterates_n100.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     4008 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/trees/test_siterates_n500.txt
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:47.729182 pg-sui-0.2.1/pgsui/example_data/vcf_files/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)   380243 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/vcf_files/test.vcf
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    72705 2023-07-16 18:34:43.000000 pg-sui-0.2.1/pgsui/example_data/vcf_files/test.vcf.gz
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2581 2023-07-16 18:34:43.000000 pg-sui-0.2.1/pgsui/example_data/vcf_files/test.vcf.gz.tbi
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:47.834603 pg-sui-0.2.1/pgsui/impute/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.1/pgsui/impute/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)   124991 2023-07-22 22:30:11.000000 pg-sui-0.2.1/pgsui/impute/estimators.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    51210 2023-07-20 21:29:54.000000 pg-sui-0.2.1/pgsui/impute/impute.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    53283 2023-07-20 21:27:33.000000 pg-sui-0.2.1/pgsui/impute/simple_imputers.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:47.964636 pg-sui-0.2.1/pgsui/impute/supervised/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-15 05:58:52.000000 pg-sui-0.2.1/pgsui/impute/supervised/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    35075 2023-07-21 16:54:38.000000 pg-sui-0.2.1/pgsui/impute/supervised/iterative_imputer_fixedparams.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    45443 2023-07-21 03:30:57.000000 pg-sui-0.2.1/pgsui/impute/supervised/iterative_imputer_gridsearch.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:48.169519 pg-sui-0.2.1/pgsui/impute/unsupervised/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-15 05:58:52.000000 pg-sui-0.2.1/pgsui/impute/unsupervised/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     9682 2023-07-20 20:38:09.000000 pg-sui-0.2.1/pgsui/impute/unsupervised/callbacks.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    29483 2023-07-21 03:31:57.000000 pg-sui-0.2.1/pgsui/impute/unsupervised/keras_classifiers.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:48.344649 pg-sui-0.2.1/pgsui/impute/unsupervised/models/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-15 05:58:52.000000 pg-sui-0.2.1/pgsui/impute/unsupervised/models/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    20161 2023-07-22 20:36:22.000000 pg-sui-0.2.1/pgsui/impute/unsupervised/models/autoencoder_model.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:48.464294 pg-sui-0.2.1/pgsui/impute/unsupervised/models/in_development/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-15 05:58:52.000000 pg-sui-0.2.1/pgsui/impute/unsupervised/models/in_development/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    15036 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/impute/unsupervised/models/in_development/cnn_model.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14501 2023-07-21 04:19:01.000000 pg-sui-0.2.1/pgsui/impute/unsupervised/models/nlpca_model.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    37879 2023-07-21 04:21:34.000000 pg-sui-0.2.1/pgsui/impute/unsupervised/models/ubp_model.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    22338 2023-07-21 04:23:07.000000 pg-sui-0.2.1/pgsui/impute/unsupervised/models/vae_model.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    52292 2023-07-19 00:32:53.000000 pg-sui-0.2.1/pgsui/impute/unsupervised/neural_network_imputers.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    50830 2023-07-20 21:26:23.000000 pg-sui-0.2.1/pgsui/impute/unsupervised/neural_network_methods.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     7471 2023-07-20 21:22:10.000000 pg-sui-0.2.1/pgsui/pg_sui.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:48.594543 pg-sui-0.2.1/pgsui/utils/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.1/pgsui/utils/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    15705 2023-07-20 21:31:57.000000 pg-sui-0.2.1/pgsui/utils/misc.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    33748 2023-07-21 04:25:34.000000 pg-sui-0.2.1/pgsui/utils/plotting.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    26862 2023-07-19 00:15:22.000000 pg-sui-0.2.1/pgsui/utils/scorers.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    10143 2023-07-16 18:34:39.000000 pg-sui-0.2.1/pgsui/utils/sequence_tools.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2104 2023-07-23 01:53:33.000000 pg-sui-0.2.1/pyproject.toml
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)       38 2023-07-23 01:53:48.794195 pg-sui-0.2.1/setup.cfg
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     3046 2023-07-23 01:53:28.000000 pg-sui-0.2.1/setup.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:48.649341 pg-sui-0.2.1/simulation/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.1/simulation/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    11345 2023-07-16 18:34:39.000000 pg-sui-0.2.1/simulation/sim_benchmarks.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    13793 2023-07-16 18:34:39.000000 pg-sui-0.2.1/simulation/sim_treeparams.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:48.769564 pg-sui-0.2.1/test/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-15 05:58:52.000000 pg-sui-0.2.1/test/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     6024 2023-07-16 18:34:39.000000 pg-sui-0.2.1/test/pg_sui_simtest.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    15871 2023-07-16 18:34:39.000000 pg-sui-0.2.1/test/pg_sui_testing.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     5034 2023-07-20 21:32:52.000000 pg-sui-0.2.1/test/test.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14310 2023-07-16 18:34:39.000000 pg-sui-0.2.1/test/test_pgsui.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     5867 2023-07-19 15:22:02.000000 pg-sui-0.2.1/test/test_tkc.py
```

### Comparing `PG-SUI-0.2/PG_SUI.egg-info/PKG-INFO` & `pg-sui-0.2.1/PG_SUI.egg-info/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,17 +1,20 @@
 Metadata-Version: 2.1
-Name: PG-SUI
-Version: 0.2
+Name: pg-sui
+Version: 0.2.1
 Summary: Python machine and deep learning package to impute missing SNPs
 Home-page: https://github.com/btmartin721/PG-SUI
 Author: Bradley T. Martin and Tyler K. Chafin
 Author-email: evobio721@gmail.com
 Maintainer: Bradley T. Martin
 Maintainer-email: evobio721@gmail.com
 License: GNU General Public License v3 (GPLv3)
+Project-URL: Homepage, https://github.com/btmartin721/PG-SUI
+Project-URL: Documentation, https://pg-sui.readthedocs.io/en/latest/
+Project-URL: Source, https://github.com/btmartin721/PG-SUI.git
 Project-URL: Bug Tracker, https://github.com/btmartin721/PG-SUI/issues
 Description: 
         <img src="https://github.com/btmartin721/PG-SUI/blob/master/img/pgsui-logo-faded.png" alt="PG-SUI Logo" width="50%" height="50%">
         
         
         # PG-SUI
         
@@ -270,20 +273,25 @@
         
         <a name="3">3. </a>Hinton, G.E., & Salakhutdinov, R.R. (2006). Reducing the dimensionality of data with neural networks. Science, 313(5786), 504-507.
         
         <a name="4">4. </a>Scholz, M., Kaplan, F., Guy, C. L., Kopka, J., & Selbig, J. (2005). Non-linear PCA: a missing data approach. Bioinformatics, 21(20), 3887-3895.
             
         <a name="5">5. </a>Gashler, M. S., Smith, M. R., Morris, R., & Martinez, T. (2016). Missing value imputation with unsupervised backpropagation. Computational Intelligence, 32(2), 196-215.
         
-Keywords: python,impute,imputation,imputer,machine learning,neural network,api,IterativeImputer,vae,ubp,nlpca,autoencoder
+Keywords: python,impute,imputation,imputer,machine learning,neural network,api,IterativeImputer,vae,ubp,nlpca,autoencoder,deep learning,population genomics
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
-Classifier: License :: OSI Approved :: GNU General Public License v3 (GPLv3)
+Classifier: Programming Language :: Python :: 3
+Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Science/Research
+Classifier: License :: OSI Approved :: GNU General Public License v3 (GPLv3)
 Classifier: Topic :: Scientific/Engineering :: Bio-Informatics
 Classifier: Operating System :: OS Independent
 Classifier: Natural Language :: English
 Requires-Python: >=3.8,<4
 Description-Content-Type: text/markdown
 Provides-Extra: docs
 Provides-Extra: intel
```

### Comparing `PG-SUI-0.2/PG_SUI.egg-info/SOURCES.txt` & `pg-sui-0.2.1/PG_SUI.egg-info/SOURCES.txt`

 * *Files 10% similar despite different names*

```diff
@@ -3,14 +3,19 @@
 pyproject.toml
 setup.py
 PG_SUI.egg-info/PKG-INFO
 PG_SUI.egg-info/SOURCES.txt
 PG_SUI.egg-info/dependency_links.txt
 PG_SUI.egg-info/requires.txt
 PG_SUI.egg-info/top_level.txt
+pg_sui.egg-info/PKG-INFO
+pg_sui.egg-info/SOURCES.txt
+pg_sui.egg-info/dependency_links.txt
+pg_sui.egg-info/requires.txt
+pg_sui.egg-info/top_level.txt
 pgsui/__init__.py
 pgsui/pg_sui.py
 pgsui/data_processing/__init__.py
 pgsui/data_processing/transformers.py
 pgsui/example_data/__init__.py
 pgsui/example_data/phylip_files/__init__.py
 pgsui/example_data/phylip_files/test.phy
```

### Comparing `PG-SUI-0.2/PKG-INFO` & `pg-sui-0.2.1/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,17 +1,20 @@
 Metadata-Version: 2.1
-Name: PG-SUI
-Version: 0.2
+Name: pg-sui
+Version: 0.2.1
 Summary: Python machine and deep learning package to impute missing SNPs
 Home-page: https://github.com/btmartin721/PG-SUI
 Author: Bradley T. Martin and Tyler K. Chafin
 Author-email: evobio721@gmail.com
 Maintainer: Bradley T. Martin
 Maintainer-email: evobio721@gmail.com
 License: GNU General Public License v3 (GPLv3)
+Project-URL: Homepage, https://github.com/btmartin721/PG-SUI
+Project-URL: Documentation, https://pg-sui.readthedocs.io/en/latest/
+Project-URL: Source, https://github.com/btmartin721/PG-SUI.git
 Project-URL: Bug Tracker, https://github.com/btmartin721/PG-SUI/issues
 Description: 
         <img src="https://github.com/btmartin721/PG-SUI/blob/master/img/pgsui-logo-faded.png" alt="PG-SUI Logo" width="50%" height="50%">
         
         
         # PG-SUI
         
@@ -270,20 +273,25 @@
         
         <a name="3">3. </a>Hinton, G.E., & Salakhutdinov, R.R. (2006). Reducing the dimensionality of data with neural networks. Science, 313(5786), 504-507.
         
         <a name="4">4. </a>Scholz, M., Kaplan, F., Guy, C. L., Kopka, J., & Selbig, J. (2005). Non-linear PCA: a missing data approach. Bioinformatics, 21(20), 3887-3895.
             
         <a name="5">5. </a>Gashler, M. S., Smith, M. R., Morris, R., & Martinez, T. (2016). Missing value imputation with unsupervised backpropagation. Computational Intelligence, 32(2), 196-215.
         
-Keywords: python,impute,imputation,imputer,machine learning,neural network,api,IterativeImputer,vae,ubp,nlpca,autoencoder
+Keywords: python,impute,imputation,imputer,machine learning,neural network,api,IterativeImputer,vae,ubp,nlpca,autoencoder,deep learning,population genomics
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
-Classifier: License :: OSI Approved :: GNU General Public License v3 (GPLv3)
+Classifier: Programming Language :: Python :: 3
+Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Science/Research
+Classifier: License :: OSI Approved :: GNU General Public License v3 (GPLv3)
 Classifier: Topic :: Scientific/Engineering :: Bio-Informatics
 Classifier: Operating System :: OS Independent
 Classifier: Natural Language :: English
 Requires-Python: >=3.8,<4
 Description-Content-Type: text/markdown
 Provides-Extra: docs
 Provides-Extra: intel
```

### Comparing `PG-SUI-0.2/README.md` & `pg-sui-0.2.1/README.md`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/__init__.py` & `pg-sui-0.2.1/pgsui/__init__.py`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/data_processing/transformers.py` & `pg-sui-0.2.1/pgsui/data_processing/transformers.py`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/example_data/phylip_files/test.phy` & `pg-sui-0.2.1/pgsui/example_data/phylip_files/test.phy`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/example_data/phylip_files/test_n10.phy` & `pg-sui-0.2.1/pgsui/example_data/phylip_files/test_n10.phy`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/example_data/phylip_files/test_n100.phy` & `pg-sui-0.2.1/pgsui/example_data/phylip_files/test_n100.phy`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/example_data/phylip_files/test_n2.phy` & `pg-sui-0.2.1/pgsui/example_data/phylip_files/test_n2.phy`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/example_data/phylip_files/test_n500.phy` & `pg-sui-0.2.1/pgsui/example_data/phylip_files/test_n500.phy`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/example_data/popmaps/test.popmap` & `pg-sui-0.2.1/pgsui/example_data/popmaps/test.popmap`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/example_data/structure_files/test.nopops.1row.10sites.str` & `pg-sui-0.2.1/pgsui/example_data/structure_files/test.nopops.1row.10sites.str`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/example_data/structure_files/test.nopops.2row.100sites.str` & `pg-sui-0.2.1/pgsui/example_data/structure_files/test.nopops.2row.100sites.str`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/example_data/structure_files/test.nopops.2row.10sites.str` & `pg-sui-0.2.1/pgsui/example_data/structure_files/test.nopops.2row.10sites.str`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/example_data/structure_files/test.nopops.2row.30sites.str` & `pg-sui-0.2.1/pgsui/example_data/structure_files/test.nopops.2row.30sites.str`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/example_data/structure_files/test.nopops.2row.allsites.str` & `pg-sui-0.2.1/pgsui/example_data/structure_files/test.nopops.2row.allsites.str`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/example_data/structure_files/test.pops.1row.10sites.str` & `pg-sui-0.2.1/pgsui/example_data/structure_files/test.pops.1row.10sites.str`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/example_data/structure_files/test.pops.2row.10sites.str` & `pg-sui-0.2.1/pgsui/example_data/structure_files/test.pops.2row.10sites.str`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/example_data/structure_files/test.pops.2row.allsites.str` & `pg-sui-0.2.1/pgsui/example_data/structure_files/test.pops.2row.allsites.str`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/example_data/trees/test.iqtree` & `pg-sui-0.2.1/pgsui/example_data/trees/test.iqtree`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/example_data/trees/test.rate` & `pg-sui-0.2.1/pgsui/example_data/trees/test.rate`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/example_data/trees/test.tre` & `pg-sui-0.2.1/pgsui/example_data/trees/test.tre`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/example_data/trees/test_n10.rate` & `pg-sui-0.2.1/pgsui/example_data/trees/test_n10.rate`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/example_data/trees/test_n100.rate` & `pg-sui-0.2.1/pgsui/example_data/trees/test_n100.rate`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/example_data/trees/test_n500.rate` & `pg-sui-0.2.1/pgsui/example_data/trees/test_n500.rate`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/example_data/trees/test_siterates.txt` & `pg-sui-0.2.1/pgsui/example_data/trees/test_siterates.txt`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/example_data/trees/test_siterates_n100.txt` & `pg-sui-0.2.1/pgsui/example_data/trees/test_siterates_n100.txt`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/example_data/trees/test_siterates_n500.txt` & `pg-sui-0.2.1/pgsui/example_data/trees/test_siterates_n500.txt`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/example_data/vcf_files/test.vcf` & `pg-sui-0.2.1/pgsui/example_data/vcf_files/test.vcf`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/example_data/vcf_files/test.vcf.gz` & `pg-sui-0.2.1/pgsui/example_data/vcf_files/test.vcf.gz`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/example_data/vcf_files/test.vcf.gz.tbi` & `pg-sui-0.2.1/pgsui/example_data/vcf_files/test.vcf.gz.tbi`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/impute/estimators.py` & `pg-sui-0.2.1/pgsui/impute/estimators.py`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/impute/impute.py` & `pg-sui-0.2.1/pgsui/impute/impute.py`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/impute/simple_imputers.py` & `pg-sui-0.2.1/pgsui/impute/simple_imputers.py`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/impute/supervised/iterative_imputer_fixedparams.py` & `pg-sui-0.2.1/pgsui/impute/supervised/iterative_imputer_fixedparams.py`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/impute/supervised/iterative_imputer_gridsearch.py` & `pg-sui-0.2.1/pgsui/impute/supervised/iterative_imputer_gridsearch.py`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/impute/unsupervised/callbacks.py` & `pg-sui-0.2.1/pgsui/impute/unsupervised/callbacks.py`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/impute/unsupervised/keras_classifiers.py` & `pg-sui-0.2.1/pgsui/impute/unsupervised/keras_classifiers.py`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/impute/unsupervised/models/autoencoder_model.py` & `pg-sui-0.2.1/pgsui/impute/unsupervised/models/autoencoder_model.py`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/impute/unsupervised/models/in_development/cnn_model.py` & `pg-sui-0.2.1/pgsui/impute/unsupervised/models/in_development/cnn_model.py`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/impute/unsupervised/models/nlpca_model.py` & `pg-sui-0.2.1/pgsui/impute/unsupervised/models/nlpca_model.py`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/impute/unsupervised/models/ubp_model.py` & `pg-sui-0.2.1/pgsui/impute/unsupervised/models/ubp_model.py`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/impute/unsupervised/models/vae_model.py` & `pg-sui-0.2.1/pgsui/impute/unsupervised/models/vae_model.py`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/impute/unsupervised/neural_network_imputers.py` & `pg-sui-0.2.1/pgsui/impute/unsupervised/neural_network_imputers.py`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/impute/unsupervised/neural_network_methods.py` & `pg-sui-0.2.1/pgsui/impute/unsupervised/neural_network_methods.py`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/pg_sui.py` & `pg-sui-0.2.1/pgsui/pg_sui.py`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/utils/misc.py` & `pg-sui-0.2.1/pgsui/utils/misc.py`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/utils/plotting.py` & `pg-sui-0.2.1/pgsui/utils/plotting.py`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/utils/scorers.py` & `pg-sui-0.2.1/pgsui/utils/scorers.py`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pgsui/utils/sequence_tools.py` & `pg-sui-0.2.1/pgsui/utils/sequence_tools.py`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/pyproject.toml` & `pg-sui-0.2.1/pyproject.toml`

 * *Files 11% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools", "wheel"]
 build-backend = "setuptools.build_meta"
 
 [project]
-name = "PG-SUI"
-version = "0.2"
+name = "pg-sui"
+version = "0.2.1"
 authors = [
     { name="Bradley T. Martin", email="evobio721@gmail.com" }, 
     { name="Tyler K. Chafin", email="tylerkchafin@gmail.com" } 
 ]
 description = "Python machine and deep learning package to impute missing SNPs"
 keywords=[
         "python",
@@ -18,28 +18,34 @@
         "machine learning",
         "neural network",
         "api",
         "IterativeImputer",
         "vae",
         "ubp",
         "nlpca",
-        "autoencoder"
+        "autoencoder",
+        "deep learning",
+        "population genomics"
 ]
 readme = "README.md"
 requires-python = ">=3.8"
 license = {text = "GPL3 License"}
 classifiers=[
-    "Development Status :: 4 - Beta",
-    "Intended Audience :: Science/Research",
-    "License :: OSI Approved :: GNU General Public License v3 (GPLv3)",
+    "Programming Language :: Python :: 3",
     "Programming Language :: Python :: 3",
     "Programming Language :: Python :: 3.8",
     "Programming Language :: Python :: 3.9",
     "Programming Language :: Python :: 3.10",
-    "Programming Language :: Python :: 3.11"
+    "Programming Language :: Python :: 3.11",
+    "Development Status :: 4 - Beta",
+    "Intended Audience :: Science/Research",
+    "License :: OSI Approved :: GNU General Public License v3 (GPLv3)",
+    "Topic :: Scientific/Engineering :: Bio-Informatics",
+    "Operating System :: OS Independent",
+    "Natural Language :: English",
 ]
 dependencies = [
     "matplotlib",
     "seaborn",
     "jupyterlab",
     "scikit-learn>=1.0",
     "tqdm",
```

### Comparing `PG-SUI-0.2/setup.py` & `pg-sui-0.2.1/setup.py`

 * *Files 15% similar despite different names*

```diff
@@ -2,16 +2,16 @@
 import os
 
 
 def read(fname):
     return open(os.path.join(os.path.dirname(__file__), fname)).read()
 
 
-NAME = "PG-SUI"
-VERSION = "0.2"
+NAME = "pg-sui"
+VERSION = "0.2.1"
 AUTHORS = "Bradley T. Martin and Tyler K. Chafin"
 AUTHOR_EMAIL = "evobio721@gmail.com"
 MAINTAINER = "Bradley T. Martin"
 DESCRIPTION = "Python machine and deep learning package to impute missing SNPs"
 LONG_DESCRIPTION = open("README.md").read()
 
 setup(
@@ -22,35 +22,45 @@
     maintainer=MAINTAINER,
     maintainer_email=AUTHOR_EMAIL,
     description=DESCRIPTION,
     long_description=LONG_DESCRIPTION,
     long_description_content_type="text/markdown",
     url="https://github.com/btmartin721/PG-SUI",
     project_urls={
-        "Bug Tracker": "https://github.com/btmartin721/PG-SUI/issues"
+        "Homepage": "https://github.com/btmartin721/PG-SUI",
+        "Documentation": "https://pg-sui.readthedocs.io/en/latest/",
+        "Source": "https://github.com/btmartin721/PG-SUI.git",
+        "Bug Tracker": "https://github.com/btmartin721/PG-SUI/issues",
     },
     keywords=[
         "python",
         "impute",
         "imputation",
         "imputer",
         "machine learning",
         "neural network",
         "api",
         "IterativeImputer",
         "vae",
         "ubp",
         "nlpca",
         "autoencoder",
+        "deep learning",
+        "population genomics",
     ],
     classifiers=[
         "Programming Language :: Python :: 3",
-        "License :: OSI Approved :: GNU General Public License v3 (GPLv3)",
+        "Programming Language :: Python :: 3",
+        "Programming Language :: Python :: 3.8",
+        "Programming Language :: Python :: 3.9",
+        "Programming Language :: Python :: 3.10",
+        "Programming Language :: Python :: 3.11",
         "Development Status :: 4 - Beta",
         "Intended Audience :: Science/Research",
+        "License :: OSI Approved :: GNU General Public License v3 (GPLv3)",
         "Topic :: Scientific/Engineering :: Bio-Informatics",
         "Operating System :: OS Independent",
         "Natural Language :: English",
     ],
     license="GNU General Public License v3 (GPLv3)",
     packages=find_packages(),
     python_requires=">=3.8,<4",
@@ -81,12 +91,12 @@
     },
     package_data={
         "pgsui": [
             "example_data/structure_files/*.str",
             "example_data/phylip_files/*.phy",
             "example_data/vcf_files/*",
             "example_data/popmaps/test.popmap",
-            "example_data/trees/test*",
+            "example_data/trees/*",
         ]
     },
     include_package_data=True,
 )
```

### Comparing `PG-SUI-0.2/simulation/sim_benchmarks.py` & `pg-sui-0.2.1/simulation/sim_benchmarks.py`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/simulation/sim_treeparams.py` & `pg-sui-0.2.1/simulation/sim_treeparams.py`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/test/pg_sui_simtest.py` & `pg-sui-0.2.1/test/pg_sui_simtest.py`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/test/pg_sui_testing.py` & `pg-sui-0.2.1/test/pg_sui_testing.py`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/test/test.py` & `pg-sui-0.2.1/test/test.py`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/test/test_pgsui.py` & `pg-sui-0.2.1/test/test_pgsui.py`

 * *Files identical despite different names*

### Comparing `PG-SUI-0.2/test/test_tkc.py` & `pg-sui-0.2.1/test/test_tkc.py`

 * *Files identical despite different names*

