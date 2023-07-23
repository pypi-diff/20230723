# Comparing `tmp/pg-sui-0.2.1.tar.gz` & `tmp/pg-sui-0.2.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pg-sui-0.2.1.tar", last modified: Sun Jul 23 01:53:48 2023, max compression
+gzip compressed data, was "pg-sui-0.2.2.tar", last modified: Sun Jul 23 02:02:32 2023, max compression
```

## Comparing `pg-sui-0.2.1.tar` & `pg-sui-0.2.2.tar`

### file list

```diff
@@ -1,99 +1,99 @@
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:48.794195 pg-sui-0.2.1/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)      220 2023-07-22 21:23:30.000000 pg-sui-0.2.1/MANIFEST.in
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:46.483956 pg-sui-0.2.1/PG_SUI.egg-info/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14100 2023-07-23 01:53:44.000000 pg-sui-0.2.1/PG_SUI.egg-info/PKG-INFO
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     3150 2023-07-23 01:53:45.000000 pg-sui-0.2.1/PG_SUI.egg-info/SOURCES.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        1 2023-07-23 01:53:44.000000 pg-sui-0.2.1/PG_SUI.egg-info/dependency_links.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)      331 2023-07-23 01:53:44.000000 pg-sui-0.2.1/PG_SUI.egg-info/requires.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)       22 2023-07-23 01:53:44.000000 pg-sui-0.2.1/PG_SUI.egg-info/top_level.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14100 2023-07-23 01:53:48.794195 pg-sui-0.2.1/PKG-INFO
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    10442 2023-07-22 23:34:21.000000 pg-sui-0.2.1/README.md
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:46.573944 pg-sui-0.2.1/pgsui/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     1449 2023-07-20 21:13:19.000000 pg-sui-0.2.1/pgsui/__init__.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:46.619172 pg-sui-0.2.1/pgsui/data_processing/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.1/pgsui/data_processing/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    42452 2023-07-20 21:28:41.000000 pg-sui-0.2.1/pgsui/data_processing/transformers.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:46.648789 pg-sui-0.2.1/pgsui/example_data/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.1/pgsui/example_data/__init__.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:46.844076 pg-sui-0.2.1/pgsui/example_data/phylip_files/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.1/pgsui/example_data/phylip_files/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)   238537 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/phylip_files/test.phy
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2897 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/phylip_files/test_n10.phy
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    13428 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/phylip_files/test_n100.phy
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     1960 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/phylip_files/test_n2.phy
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    60228 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/phylip_files/test_n500.phy
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:46.908867 pg-sui-0.2.1/pgsui/example_data/popmaps/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.1/pgsui/example_data/popmaps/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     1954 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/popmaps/test.popmap
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:47.209025 pg-sui-0.2.1/pgsui/example_data/structure_files/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.1/pgsui/example_data/structure_files/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     6375 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/structure_files/test.nopops.1row.10sites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    50808 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/structure_files/test.nopops.2row.100sites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     7978 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/structure_files/test.nopops.2row.10sites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    17512 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/structure_files/test.nopops.2row.30sites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)   967410 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/structure_files/test.nopops.2row.allsites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     6609 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/structure_files/test.pops.1row.10sites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     8446 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/structure_files/test.pops.2row.10sites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)   967878 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/structure_files/test.pops.2row.allsites.str
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:47.629298 pg-sui-0.2.1/pgsui/example_data/trees/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.1/pgsui/example_data/trees/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    25575 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/trees/test.iqtree
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)      134 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/trees/test.qmat
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    46013 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/trees/test.rate
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     4696 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/trees/test.tre
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)      678 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/trees/test_n10.rate
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2577 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/trees/test_n100.rate
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    11387 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/trees/test_n500.rate
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    16235 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/trees/test_siterates.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)       80 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/trees/test_siterates_n10.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)      804 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/trees/test_siterates_n100.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     4008 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/trees/test_siterates_n500.txt
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:47.729182 pg-sui-0.2.1/pgsui/example_data/vcf_files/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)   380243 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/example_data/vcf_files/test.vcf
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    72705 2023-07-16 18:34:43.000000 pg-sui-0.2.1/pgsui/example_data/vcf_files/test.vcf.gz
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2581 2023-07-16 18:34:43.000000 pg-sui-0.2.1/pgsui/example_data/vcf_files/test.vcf.gz.tbi
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:47.834603 pg-sui-0.2.1/pgsui/impute/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.1/pgsui/impute/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)   124991 2023-07-22 22:30:11.000000 pg-sui-0.2.1/pgsui/impute/estimators.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    51210 2023-07-20 21:29:54.000000 pg-sui-0.2.1/pgsui/impute/impute.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    53283 2023-07-20 21:27:33.000000 pg-sui-0.2.1/pgsui/impute/simple_imputers.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:47.964636 pg-sui-0.2.1/pgsui/impute/supervised/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-15 05:58:52.000000 pg-sui-0.2.1/pgsui/impute/supervised/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    35075 2023-07-21 16:54:38.000000 pg-sui-0.2.1/pgsui/impute/supervised/iterative_imputer_fixedparams.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    45443 2023-07-21 03:30:57.000000 pg-sui-0.2.1/pgsui/impute/supervised/iterative_imputer_gridsearch.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:48.169519 pg-sui-0.2.1/pgsui/impute/unsupervised/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-15 05:58:52.000000 pg-sui-0.2.1/pgsui/impute/unsupervised/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     9682 2023-07-20 20:38:09.000000 pg-sui-0.2.1/pgsui/impute/unsupervised/callbacks.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    29483 2023-07-21 03:31:57.000000 pg-sui-0.2.1/pgsui/impute/unsupervised/keras_classifiers.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:48.344649 pg-sui-0.2.1/pgsui/impute/unsupervised/models/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-15 05:58:52.000000 pg-sui-0.2.1/pgsui/impute/unsupervised/models/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    20161 2023-07-22 20:36:22.000000 pg-sui-0.2.1/pgsui/impute/unsupervised/models/autoencoder_model.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:48.464294 pg-sui-0.2.1/pgsui/impute/unsupervised/models/in_development/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-15 05:58:52.000000 pg-sui-0.2.1/pgsui/impute/unsupervised/models/in_development/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    15036 2023-07-16 18:34:38.000000 pg-sui-0.2.1/pgsui/impute/unsupervised/models/in_development/cnn_model.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14501 2023-07-21 04:19:01.000000 pg-sui-0.2.1/pgsui/impute/unsupervised/models/nlpca_model.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    37879 2023-07-21 04:21:34.000000 pg-sui-0.2.1/pgsui/impute/unsupervised/models/ubp_model.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    22338 2023-07-21 04:23:07.000000 pg-sui-0.2.1/pgsui/impute/unsupervised/models/vae_model.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    52292 2023-07-19 00:32:53.000000 pg-sui-0.2.1/pgsui/impute/unsupervised/neural_network_imputers.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    50830 2023-07-20 21:26:23.000000 pg-sui-0.2.1/pgsui/impute/unsupervised/neural_network_methods.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     7471 2023-07-20 21:22:10.000000 pg-sui-0.2.1/pgsui/pg_sui.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:48.594543 pg-sui-0.2.1/pgsui/utils/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.1/pgsui/utils/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    15705 2023-07-20 21:31:57.000000 pg-sui-0.2.1/pgsui/utils/misc.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    33748 2023-07-21 04:25:34.000000 pg-sui-0.2.1/pgsui/utils/plotting.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    26862 2023-07-19 00:15:22.000000 pg-sui-0.2.1/pgsui/utils/scorers.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    10143 2023-07-16 18:34:39.000000 pg-sui-0.2.1/pgsui/utils/sequence_tools.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2104 2023-07-23 01:53:33.000000 pg-sui-0.2.1/pyproject.toml
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)       38 2023-07-23 01:53:48.794195 pg-sui-0.2.1/setup.cfg
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     3046 2023-07-23 01:53:28.000000 pg-sui-0.2.1/setup.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:48.649341 pg-sui-0.2.1/simulation/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.1/simulation/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    11345 2023-07-16 18:34:39.000000 pg-sui-0.2.1/simulation/sim_benchmarks.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    13793 2023-07-16 18:34:39.000000 pg-sui-0.2.1/simulation/sim_treeparams.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 01:53:48.769564 pg-sui-0.2.1/test/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-15 05:58:52.000000 pg-sui-0.2.1/test/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     6024 2023-07-16 18:34:39.000000 pg-sui-0.2.1/test/pg_sui_simtest.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    15871 2023-07-16 18:34:39.000000 pg-sui-0.2.1/test/pg_sui_testing.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     5034 2023-07-20 21:32:52.000000 pg-sui-0.2.1/test/test.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14310 2023-07-16 18:34:39.000000 pg-sui-0.2.1/test/test_pgsui.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     5867 2023-07-19 15:22:02.000000 pg-sui-0.2.1/test/test_tkc.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:32.500793 pg-sui-0.2.2/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)      220 2023-07-22 21:23:30.000000 pg-sui-0.2.2/MANIFEST.in
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:30.411400 pg-sui-0.2.2/PG_SUI.egg-info/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14102 2023-07-23 02:02:28.000000 pg-sui-0.2.2/PG_SUI.egg-info/PKG-INFO
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     3150 2023-07-23 02:02:29.000000 pg-sui-0.2.2/PG_SUI.egg-info/SOURCES.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        1 2023-07-23 02:02:28.000000 pg-sui-0.2.2/PG_SUI.egg-info/dependency_links.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)      331 2023-07-23 02:02:28.000000 pg-sui-0.2.2/PG_SUI.egg-info/requires.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)       22 2023-07-23 02:02:28.000000 pg-sui-0.2.2/PG_SUI.egg-info/top_level.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14102 2023-07-23 02:02:32.500793 pg-sui-0.2.2/PKG-INFO
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    10444 2023-07-23 01:57:24.000000 pg-sui-0.2.2/README.md
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:30.491686 pg-sui-0.2.2/pgsui/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     1449 2023-07-20 21:13:19.000000 pg-sui-0.2.2/pgsui/__init__.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:30.531336 pg-sui-0.2.2/pgsui/data_processing/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.2/pgsui/data_processing/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    42452 2023-07-20 21:28:41.000000 pg-sui-0.2.2/pgsui/data_processing/transformers.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:30.566480 pg-sui-0.2.2/pgsui/example_data/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.2/pgsui/example_data/__init__.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:30.741712 pg-sui-0.2.2/pgsui/example_data/phylip_files/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.2/pgsui/example_data/phylip_files/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)   238537 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/phylip_files/test.phy
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2897 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/phylip_files/test_n10.phy
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    13428 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/phylip_files/test_n100.phy
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     1960 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/phylip_files/test_n2.phy
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    60228 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/phylip_files/test_n500.phy
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:30.801436 pg-sui-0.2.2/pgsui/example_data/popmaps/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.2/pgsui/example_data/popmaps/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     1954 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/popmaps/test.popmap
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:31.096722 pg-sui-0.2.2/pgsui/example_data/structure_files/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.2/pgsui/example_data/structure_files/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     6375 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/structure_files/test.nopops.1row.10sites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    50808 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/structure_files/test.nopops.2row.100sites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     7978 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/structure_files/test.nopops.2row.10sites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    17512 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/structure_files/test.nopops.2row.30sites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)   967410 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/structure_files/test.nopops.2row.allsites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     6609 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/structure_files/test.pops.1row.10sites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     8446 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/structure_files/test.pops.2row.10sites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)   967878 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/structure_files/test.pops.2row.allsites.str
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:31.561134 pg-sui-0.2.2/pgsui/example_data/trees/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.2/pgsui/example_data/trees/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    25575 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/trees/test.iqtree
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)      134 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/trees/test.qmat
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    46013 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/trees/test.rate
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     4696 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/trees/test.tre
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)      678 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/trees/test_n10.rate
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2577 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/trees/test_n100.rate
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    11387 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/trees/test_n500.rate
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    16235 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/trees/test_siterates.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)       80 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/trees/test_siterates_n10.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)      804 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/trees/test_siterates_n100.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     4008 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/trees/test_siterates_n500.txt
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:31.641250 pg-sui-0.2.2/pgsui/example_data/vcf_files/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)   380243 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/vcf_files/test.vcf
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    72705 2023-07-16 18:34:43.000000 pg-sui-0.2.2/pgsui/example_data/vcf_files/test.vcf.gz
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2581 2023-07-16 18:34:43.000000 pg-sui-0.2.2/pgsui/example_data/vcf_files/test.vcf.gz.tbi
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:31.721296 pg-sui-0.2.2/pgsui/impute/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.2/pgsui/impute/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)   124991 2023-07-22 22:30:11.000000 pg-sui-0.2.2/pgsui/impute/estimators.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    51210 2023-07-20 21:29:54.000000 pg-sui-0.2.2/pgsui/impute/impute.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    53283 2023-07-20 21:27:33.000000 pg-sui-0.2.2/pgsui/impute/simple_imputers.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:31.801116 pg-sui-0.2.2/pgsui/impute/supervised/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-15 05:58:52.000000 pg-sui-0.2.2/pgsui/impute/supervised/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    35075 2023-07-21 16:54:38.000000 pg-sui-0.2.2/pgsui/impute/supervised/iterative_imputer_fixedparams.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    45443 2023-07-21 03:30:57.000000 pg-sui-0.2.2/pgsui/impute/supervised/iterative_imputer_gridsearch.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:31.931072 pg-sui-0.2.2/pgsui/impute/unsupervised/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-15 05:58:52.000000 pg-sui-0.2.2/pgsui/impute/unsupervised/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     9682 2023-07-20 20:38:09.000000 pg-sui-0.2.2/pgsui/impute/unsupervised/callbacks.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    29483 2023-07-21 03:31:57.000000 pg-sui-0.2.2/pgsui/impute/unsupervised/keras_classifiers.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:32.145798 pg-sui-0.2.2/pgsui/impute/unsupervised/models/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-15 05:58:52.000000 pg-sui-0.2.2/pgsui/impute/unsupervised/models/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    20161 2023-07-22 20:36:22.000000 pg-sui-0.2.2/pgsui/impute/unsupervised/models/autoencoder_model.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:32.210931 pg-sui-0.2.2/pgsui/impute/unsupervised/models/in_development/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-15 05:58:52.000000 pg-sui-0.2.2/pgsui/impute/unsupervised/models/in_development/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    15036 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/impute/unsupervised/models/in_development/cnn_model.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14501 2023-07-21 04:19:01.000000 pg-sui-0.2.2/pgsui/impute/unsupervised/models/nlpca_model.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    37879 2023-07-21 04:21:34.000000 pg-sui-0.2.2/pgsui/impute/unsupervised/models/ubp_model.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    22338 2023-07-21 04:23:07.000000 pg-sui-0.2.2/pgsui/impute/unsupervised/models/vae_model.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    52292 2023-07-19 00:32:53.000000 pg-sui-0.2.2/pgsui/impute/unsupervised/neural_network_imputers.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    50830 2023-07-20 21:26:23.000000 pg-sui-0.2.2/pgsui/impute/unsupervised/neural_network_methods.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     7471 2023-07-20 21:22:10.000000 pg-sui-0.2.2/pgsui/pg_sui.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:32.320641 pg-sui-0.2.2/pgsui/utils/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.2/pgsui/utils/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    15705 2023-07-20 21:31:57.000000 pg-sui-0.2.2/pgsui/utils/misc.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    33748 2023-07-21 04:25:34.000000 pg-sui-0.2.2/pgsui/utils/plotting.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    26862 2023-07-19 00:15:22.000000 pg-sui-0.2.2/pgsui/utils/scorers.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    10143 2023-07-16 18:34:39.000000 pg-sui-0.2.2/pgsui/utils/sequence_tools.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2104 2023-07-23 02:00:41.000000 pg-sui-0.2.2/pyproject.toml
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)       38 2023-07-23 02:02:32.505800 pg-sui-0.2.2/setup.cfg
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     3046 2023-07-23 01:58:25.000000 pg-sui-0.2.2/setup.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:32.371056 pg-sui-0.2.2/simulation/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.2/simulation/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    11345 2023-07-16 18:34:39.000000 pg-sui-0.2.2/simulation/sim_benchmarks.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    13793 2023-07-16 18:34:39.000000 pg-sui-0.2.2/simulation/sim_treeparams.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:32.480724 pg-sui-0.2.2/test/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-15 05:58:52.000000 pg-sui-0.2.2/test/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     6024 2023-07-16 18:34:39.000000 pg-sui-0.2.2/test/pg_sui_simtest.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    15871 2023-07-16 18:34:39.000000 pg-sui-0.2.2/test/pg_sui_testing.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     5034 2023-07-20 21:32:52.000000 pg-sui-0.2.2/test/test.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14310 2023-07-16 18:34:39.000000 pg-sui-0.2.2/test/test_pgsui.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     5867 2023-07-19 15:22:02.000000 pg-sui-0.2.2/test/test_tkc.py
```

### Comparing `pg-sui-0.2.1/PG_SUI.egg-info/PKG-INFO` & `pg-sui-0.2.2/PG_SUI.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pg-sui
-Version: 0.2.1
+Version: 0.2.2
 Summary: Python machine and deep learning package to impute missing SNPs
 Home-page: https://github.com/btmartin721/PG-SUI
 Author: Bradley T. Martin and Tyler K. Chafin
 Author-email: evobio721@gmail.com
 Maintainer: Bradley T. Martin
 Maintainer-email: evobio721@gmail.com
 License: GNU General Public License v3 (GPLv3)
@@ -65,21 +65,21 @@
         These four "simple" imputation methods can be used as standalone imputers, as the initial imputation strategy for IterativeImputer (at least one method is required to be chosen), and to validate the accuracy of both IterativeImputer and the neural network models.
         
         ## Installing PG-SUI
         
         The easiest way to install PG-SUI is to use pip:
         
         ```
-        pip install pgsui
+        pip install pg-sui
         ```
         
         If you have an Intel CPU and want to use the sklearn-genetic-intelex package to speed up scikit-learn computations, you can do:
         
         ```
-        pip install pgsui[intel]
+        pip install pg-sui[intel]
         ```
         
         ## Manual Installation
         
         ### Dependencies
         
         + python >= 3.8
```

### Comparing `pg-sui-0.2.1/PG_SUI.egg-info/SOURCES.txt` & `pg-sui-0.2.2/PG_SUI.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/PKG-INFO` & `pg-sui-0.2.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pg-sui
-Version: 0.2.1
+Version: 0.2.2
 Summary: Python machine and deep learning package to impute missing SNPs
 Home-page: https://github.com/btmartin721/PG-SUI
 Author: Bradley T. Martin and Tyler K. Chafin
 Author-email: evobio721@gmail.com
 Maintainer: Bradley T. Martin
 Maintainer-email: evobio721@gmail.com
 License: GNU General Public License v3 (GPLv3)
@@ -65,21 +65,21 @@
         These four "simple" imputation methods can be used as standalone imputers, as the initial imputation strategy for IterativeImputer (at least one method is required to be chosen), and to validate the accuracy of both IterativeImputer and the neural network models.
         
         ## Installing PG-SUI
         
         The easiest way to install PG-SUI is to use pip:
         
         ```
-        pip install pgsui
+        pip install pg-sui
         ```
         
         If you have an Intel CPU and want to use the sklearn-genetic-intelex package to speed up scikit-learn computations, you can do:
         
         ```
-        pip install pgsui[intel]
+        pip install pg-sui[intel]
         ```
         
         ## Manual Installation
         
         ### Dependencies
         
         + python >= 3.8
```

### Comparing `pg-sui-0.2.1/README.md` & `pg-sui-0.2.2/README.md`

 * *Files 0% similar despite different names*

```diff
@@ -51,21 +51,21 @@
 These four "simple" imputation methods can be used as standalone imputers, as the initial imputation strategy for IterativeImputer (at least one method is required to be chosen), and to validate the accuracy of both IterativeImputer and the neural network models.
 
 ## Installing PG-SUI
 
 The easiest way to install PG-SUI is to use pip:
 
 ```
-pip install pgsui
+pip install pg-sui
 ```
 
 If you have an Intel CPU and want to use the sklearn-genetic-intelex package to speed up scikit-learn computations, you can do:
 
 ```
-pip install pgsui[intel]
+pip install pg-sui[intel]
 ```
 
 ## Manual Installation
 
 ### Dependencies
 
 + python >= 3.8
```

### Comparing `pg-sui-0.2.1/pgsui/__init__.py` & `pg-sui-0.2.2/pgsui/__init__.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/data_processing/transformers.py` & `pg-sui-0.2.2/pgsui/data_processing/transformers.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/example_data/phylip_files/test.phy` & `pg-sui-0.2.2/pgsui/example_data/phylip_files/test.phy`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/example_data/phylip_files/test_n10.phy` & `pg-sui-0.2.2/pgsui/example_data/phylip_files/test_n10.phy`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/example_data/phylip_files/test_n100.phy` & `pg-sui-0.2.2/pgsui/example_data/phylip_files/test_n100.phy`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/example_data/phylip_files/test_n2.phy` & `pg-sui-0.2.2/pgsui/example_data/phylip_files/test_n2.phy`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/example_data/phylip_files/test_n500.phy` & `pg-sui-0.2.2/pgsui/example_data/phylip_files/test_n500.phy`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/example_data/popmaps/test.popmap` & `pg-sui-0.2.2/pgsui/example_data/popmaps/test.popmap`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/example_data/structure_files/test.nopops.1row.10sites.str` & `pg-sui-0.2.2/pgsui/example_data/structure_files/test.nopops.1row.10sites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/example_data/structure_files/test.nopops.2row.100sites.str` & `pg-sui-0.2.2/pgsui/example_data/structure_files/test.nopops.2row.100sites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/example_data/structure_files/test.nopops.2row.10sites.str` & `pg-sui-0.2.2/pgsui/example_data/structure_files/test.nopops.2row.10sites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/example_data/structure_files/test.nopops.2row.30sites.str` & `pg-sui-0.2.2/pgsui/example_data/structure_files/test.nopops.2row.30sites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/example_data/structure_files/test.nopops.2row.allsites.str` & `pg-sui-0.2.2/pgsui/example_data/structure_files/test.nopops.2row.allsites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/example_data/structure_files/test.pops.1row.10sites.str` & `pg-sui-0.2.2/pgsui/example_data/structure_files/test.pops.1row.10sites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/example_data/structure_files/test.pops.2row.10sites.str` & `pg-sui-0.2.2/pgsui/example_data/structure_files/test.pops.2row.10sites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/example_data/structure_files/test.pops.2row.allsites.str` & `pg-sui-0.2.2/pgsui/example_data/structure_files/test.pops.2row.allsites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/example_data/trees/test.iqtree` & `pg-sui-0.2.2/pgsui/example_data/trees/test.iqtree`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/example_data/trees/test.rate` & `pg-sui-0.2.2/pgsui/example_data/trees/test.rate`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/example_data/trees/test.tre` & `pg-sui-0.2.2/pgsui/example_data/trees/test.tre`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/example_data/trees/test_n10.rate` & `pg-sui-0.2.2/pgsui/example_data/trees/test_n10.rate`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/example_data/trees/test_n100.rate` & `pg-sui-0.2.2/pgsui/example_data/trees/test_n100.rate`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/example_data/trees/test_n500.rate` & `pg-sui-0.2.2/pgsui/example_data/trees/test_n500.rate`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/example_data/trees/test_siterates.txt` & `pg-sui-0.2.2/pgsui/example_data/trees/test_siterates.txt`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/example_data/trees/test_siterates_n100.txt` & `pg-sui-0.2.2/pgsui/example_data/trees/test_siterates_n100.txt`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/example_data/trees/test_siterates_n500.txt` & `pg-sui-0.2.2/pgsui/example_data/trees/test_siterates_n500.txt`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/example_data/vcf_files/test.vcf` & `pg-sui-0.2.2/pgsui/example_data/vcf_files/test.vcf`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/example_data/vcf_files/test.vcf.gz` & `pg-sui-0.2.2/pgsui/example_data/vcf_files/test.vcf.gz`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/example_data/vcf_files/test.vcf.gz.tbi` & `pg-sui-0.2.2/pgsui/example_data/vcf_files/test.vcf.gz.tbi`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/impute/estimators.py` & `pg-sui-0.2.2/pgsui/impute/estimators.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/impute/impute.py` & `pg-sui-0.2.2/pgsui/impute/impute.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/impute/simple_imputers.py` & `pg-sui-0.2.2/pgsui/impute/simple_imputers.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/impute/supervised/iterative_imputer_fixedparams.py` & `pg-sui-0.2.2/pgsui/impute/supervised/iterative_imputer_fixedparams.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/impute/supervised/iterative_imputer_gridsearch.py` & `pg-sui-0.2.2/pgsui/impute/supervised/iterative_imputer_gridsearch.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/impute/unsupervised/callbacks.py` & `pg-sui-0.2.2/pgsui/impute/unsupervised/callbacks.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/impute/unsupervised/keras_classifiers.py` & `pg-sui-0.2.2/pgsui/impute/unsupervised/keras_classifiers.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/impute/unsupervised/models/autoencoder_model.py` & `pg-sui-0.2.2/pgsui/impute/unsupervised/models/autoencoder_model.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/impute/unsupervised/models/in_development/cnn_model.py` & `pg-sui-0.2.2/pgsui/impute/unsupervised/models/in_development/cnn_model.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/impute/unsupervised/models/nlpca_model.py` & `pg-sui-0.2.2/pgsui/impute/unsupervised/models/nlpca_model.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/impute/unsupervised/models/ubp_model.py` & `pg-sui-0.2.2/pgsui/impute/unsupervised/models/ubp_model.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/impute/unsupervised/models/vae_model.py` & `pg-sui-0.2.2/pgsui/impute/unsupervised/models/vae_model.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/impute/unsupervised/neural_network_imputers.py` & `pg-sui-0.2.2/pgsui/impute/unsupervised/neural_network_imputers.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/impute/unsupervised/neural_network_methods.py` & `pg-sui-0.2.2/pgsui/impute/unsupervised/neural_network_methods.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/pg_sui.py` & `pg-sui-0.2.2/pgsui/pg_sui.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/utils/misc.py` & `pg-sui-0.2.2/pgsui/utils/misc.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/utils/plotting.py` & `pg-sui-0.2.2/pgsui/utils/plotting.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/utils/scorers.py` & `pg-sui-0.2.2/pgsui/utils/scorers.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pgsui/utils/sequence_tools.py` & `pg-sui-0.2.2/pgsui/utils/sequence_tools.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/pyproject.toml` & `pg-sui-0.2.2/pyproject.toml`

 * *Files 4% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools", "wheel"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "pg-sui"
-version = "0.2.1"
+version = "0.2.2"
 authors = [
     { name="Bradley T. Martin", email="evobio721@gmail.com" }, 
     { name="Tyler K. Chafin", email="tylerkchafin@gmail.com" } 
 ]
 description = "Python machine and deep learning package to impute missing SNPs"
 keywords=[
         "python",
```

### Comparing `pg-sui-0.2.1/setup.py` & `pg-sui-0.2.2/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 
 
 def read(fname):
     return open(os.path.join(os.path.dirname(__file__), fname)).read()
 
 
 NAME = "pg-sui"
-VERSION = "0.2.1"
+VERSION = "0.2.2"
 AUTHORS = "Bradley T. Martin and Tyler K. Chafin"
 AUTHOR_EMAIL = "evobio721@gmail.com"
 MAINTAINER = "Bradley T. Martin"
 DESCRIPTION = "Python machine and deep learning package to impute missing SNPs"
 LONG_DESCRIPTION = open("README.md").read()
 
 setup(
```

### Comparing `pg-sui-0.2.1/simulation/sim_benchmarks.py` & `pg-sui-0.2.2/simulation/sim_benchmarks.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/simulation/sim_treeparams.py` & `pg-sui-0.2.2/simulation/sim_treeparams.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/test/pg_sui_simtest.py` & `pg-sui-0.2.2/test/pg_sui_simtest.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/test/pg_sui_testing.py` & `pg-sui-0.2.2/test/pg_sui_testing.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/test/test.py` & `pg-sui-0.2.2/test/test.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/test/test_pgsui.py` & `pg-sui-0.2.2/test/test_pgsui.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.1/test/test_tkc.py` & `pg-sui-0.2.2/test/test_tkc.py`

 * *Files identical despite different names*

