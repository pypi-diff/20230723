# Comparing `tmp/pg-sui-0.2.2.tar.gz` & `tmp/pg-sui-0.2.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pg-sui-0.2.2.tar", last modified: Sun Jul 23 02:02:32 2023, max compression
+gzip compressed data, was "pg-sui-0.2.3.tar", last modified: Sun Jul 23 05:30:39 2023, max compression
```

## Comparing `pg-sui-0.2.2.tar` & `pg-sui-0.2.3.tar`

### file list

```diff
@@ -1,99 +1,99 @@
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:32.500793 pg-sui-0.2.2/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)      220 2023-07-22 21:23:30.000000 pg-sui-0.2.2/MANIFEST.in
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:30.411400 pg-sui-0.2.2/PG_SUI.egg-info/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14102 2023-07-23 02:02:28.000000 pg-sui-0.2.2/PG_SUI.egg-info/PKG-INFO
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     3150 2023-07-23 02:02:29.000000 pg-sui-0.2.2/PG_SUI.egg-info/SOURCES.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        1 2023-07-23 02:02:28.000000 pg-sui-0.2.2/PG_SUI.egg-info/dependency_links.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)      331 2023-07-23 02:02:28.000000 pg-sui-0.2.2/PG_SUI.egg-info/requires.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)       22 2023-07-23 02:02:28.000000 pg-sui-0.2.2/PG_SUI.egg-info/top_level.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14102 2023-07-23 02:02:32.500793 pg-sui-0.2.2/PKG-INFO
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    10444 2023-07-23 01:57:24.000000 pg-sui-0.2.2/README.md
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:30.491686 pg-sui-0.2.2/pgsui/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     1449 2023-07-20 21:13:19.000000 pg-sui-0.2.2/pgsui/__init__.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:30.531336 pg-sui-0.2.2/pgsui/data_processing/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.2/pgsui/data_processing/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    42452 2023-07-20 21:28:41.000000 pg-sui-0.2.2/pgsui/data_processing/transformers.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:30.566480 pg-sui-0.2.2/pgsui/example_data/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.2/pgsui/example_data/__init__.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:30.741712 pg-sui-0.2.2/pgsui/example_data/phylip_files/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.2/pgsui/example_data/phylip_files/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)   238537 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/phylip_files/test.phy
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2897 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/phylip_files/test_n10.phy
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    13428 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/phylip_files/test_n100.phy
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     1960 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/phylip_files/test_n2.phy
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    60228 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/phylip_files/test_n500.phy
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:30.801436 pg-sui-0.2.2/pgsui/example_data/popmaps/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.2/pgsui/example_data/popmaps/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     1954 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/popmaps/test.popmap
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:31.096722 pg-sui-0.2.2/pgsui/example_data/structure_files/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.2/pgsui/example_data/structure_files/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     6375 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/structure_files/test.nopops.1row.10sites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    50808 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/structure_files/test.nopops.2row.100sites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     7978 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/structure_files/test.nopops.2row.10sites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    17512 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/structure_files/test.nopops.2row.30sites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)   967410 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/structure_files/test.nopops.2row.allsites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     6609 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/structure_files/test.pops.1row.10sites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     8446 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/structure_files/test.pops.2row.10sites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)   967878 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/structure_files/test.pops.2row.allsites.str
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:31.561134 pg-sui-0.2.2/pgsui/example_data/trees/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.2/pgsui/example_data/trees/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    25575 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/trees/test.iqtree
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)      134 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/trees/test.qmat
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    46013 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/trees/test.rate
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     4696 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/trees/test.tre
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)      678 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/trees/test_n10.rate
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2577 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/trees/test_n100.rate
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    11387 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/trees/test_n500.rate
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    16235 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/trees/test_siterates.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)       80 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/trees/test_siterates_n10.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)      804 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/trees/test_siterates_n100.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     4008 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/trees/test_siterates_n500.txt
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:31.641250 pg-sui-0.2.2/pgsui/example_data/vcf_files/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)   380243 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/example_data/vcf_files/test.vcf
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    72705 2023-07-16 18:34:43.000000 pg-sui-0.2.2/pgsui/example_data/vcf_files/test.vcf.gz
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2581 2023-07-16 18:34:43.000000 pg-sui-0.2.2/pgsui/example_data/vcf_files/test.vcf.gz.tbi
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:31.721296 pg-sui-0.2.2/pgsui/impute/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.2/pgsui/impute/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)   124991 2023-07-22 22:30:11.000000 pg-sui-0.2.2/pgsui/impute/estimators.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    51210 2023-07-20 21:29:54.000000 pg-sui-0.2.2/pgsui/impute/impute.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    53283 2023-07-20 21:27:33.000000 pg-sui-0.2.2/pgsui/impute/simple_imputers.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:31.801116 pg-sui-0.2.2/pgsui/impute/supervised/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-15 05:58:52.000000 pg-sui-0.2.2/pgsui/impute/supervised/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    35075 2023-07-21 16:54:38.000000 pg-sui-0.2.2/pgsui/impute/supervised/iterative_imputer_fixedparams.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    45443 2023-07-21 03:30:57.000000 pg-sui-0.2.2/pgsui/impute/supervised/iterative_imputer_gridsearch.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:31.931072 pg-sui-0.2.2/pgsui/impute/unsupervised/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-15 05:58:52.000000 pg-sui-0.2.2/pgsui/impute/unsupervised/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     9682 2023-07-20 20:38:09.000000 pg-sui-0.2.2/pgsui/impute/unsupervised/callbacks.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    29483 2023-07-21 03:31:57.000000 pg-sui-0.2.2/pgsui/impute/unsupervised/keras_classifiers.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:32.145798 pg-sui-0.2.2/pgsui/impute/unsupervised/models/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-15 05:58:52.000000 pg-sui-0.2.2/pgsui/impute/unsupervised/models/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    20161 2023-07-22 20:36:22.000000 pg-sui-0.2.2/pgsui/impute/unsupervised/models/autoencoder_model.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:32.210931 pg-sui-0.2.2/pgsui/impute/unsupervised/models/in_development/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-15 05:58:52.000000 pg-sui-0.2.2/pgsui/impute/unsupervised/models/in_development/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    15036 2023-07-16 18:34:38.000000 pg-sui-0.2.2/pgsui/impute/unsupervised/models/in_development/cnn_model.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14501 2023-07-21 04:19:01.000000 pg-sui-0.2.2/pgsui/impute/unsupervised/models/nlpca_model.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    37879 2023-07-21 04:21:34.000000 pg-sui-0.2.2/pgsui/impute/unsupervised/models/ubp_model.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    22338 2023-07-21 04:23:07.000000 pg-sui-0.2.2/pgsui/impute/unsupervised/models/vae_model.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    52292 2023-07-19 00:32:53.000000 pg-sui-0.2.2/pgsui/impute/unsupervised/neural_network_imputers.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    50830 2023-07-20 21:26:23.000000 pg-sui-0.2.2/pgsui/impute/unsupervised/neural_network_methods.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     7471 2023-07-20 21:22:10.000000 pg-sui-0.2.2/pgsui/pg_sui.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:32.320641 pg-sui-0.2.2/pgsui/utils/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.2/pgsui/utils/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    15705 2023-07-20 21:31:57.000000 pg-sui-0.2.2/pgsui/utils/misc.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    33748 2023-07-21 04:25:34.000000 pg-sui-0.2.2/pgsui/utils/plotting.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    26862 2023-07-19 00:15:22.000000 pg-sui-0.2.2/pgsui/utils/scorers.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    10143 2023-07-16 18:34:39.000000 pg-sui-0.2.2/pgsui/utils/sequence_tools.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2104 2023-07-23 02:00:41.000000 pg-sui-0.2.2/pyproject.toml
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)       38 2023-07-23 02:02:32.505800 pg-sui-0.2.2/setup.cfg
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     3046 2023-07-23 01:58:25.000000 pg-sui-0.2.2/setup.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:32.371056 pg-sui-0.2.2/simulation/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2022-06-18 03:33:16.000000 pg-sui-0.2.2/simulation/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    11345 2023-07-16 18:34:39.000000 pg-sui-0.2.2/simulation/sim_benchmarks.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    13793 2023-07-16 18:34:39.000000 pg-sui-0.2.2/simulation/sim_treeparams.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 02:02:32.480724 pg-sui-0.2.2/test/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-15 05:58:52.000000 pg-sui-0.2.2/test/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     6024 2023-07-16 18:34:39.000000 pg-sui-0.2.2/test/pg_sui_simtest.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    15871 2023-07-16 18:34:39.000000 pg-sui-0.2.2/test/pg_sui_testing.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     5034 2023-07-20 21:32:52.000000 pg-sui-0.2.2/test/test.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14310 2023-07-16 18:34:39.000000 pg-sui-0.2.2/test/test_pgsui.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     5867 2023-07-19 15:22:02.000000 pg-sui-0.2.2/test/test_tkc.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:39.345819 pg-sui-0.2.3/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    35149 2023-07-16 18:34:37.000000 pg-sui-0.2.3/LICENSE
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)      220 2023-07-22 21:23:30.000000 pg-sui-0.2.3/MANIFEST.in
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14102 2023-07-23 05:30:39.345819 pg-sui-0.2.3/PKG-INFO
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    10444 2023-07-23 01:57:24.000000 pg-sui-0.2.3/README.md
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:37.302699 pg-sui-0.2.3/pg_sui.egg-info/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14102 2023-07-23 05:30:35.000000 pg-sui-0.2.3/pg_sui.egg-info/PKG-INFO
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2994 2023-07-23 05:30:36.000000 pg-sui-0.2.3/pg_sui.egg-info/SOURCES.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        1 2023-07-23 05:30:35.000000 pg-sui-0.2.3/pg_sui.egg-info/dependency_links.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)      331 2023-07-23 05:30:35.000000 pg-sui-0.2.3/pg_sui.egg-info/requires.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)       22 2023-07-23 05:30:35.000000 pg-sui-0.2.3/pg_sui.egg-info/top_level.txt
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:37.340469 pg-sui-0.2.3/pgsui/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     1449 2023-07-23 04:24:42.000000 pg-sui-0.2.3/pgsui/__init__.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:37.387346 pg-sui-0.2.3/pgsui/data_processing/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:42.000000 pg-sui-0.2.3/pgsui/data_processing/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    42452 2023-07-23 04:24:42.000000 pg-sui-0.2.3/pgsui/data_processing/transformers.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:37.425103 pg-sui-0.2.3/pgsui/example_data/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:42.000000 pg-sui-0.2.3/pgsui/example_data/__init__.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:37.587893 pg-sui-0.2.3/pgsui/example_data/phylip_files/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/phylip_files/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)   238537 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/phylip_files/test.phy
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2897 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/phylip_files/test_n10.phy
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    13428 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/phylip_files/test_n100.phy
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     1960 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/phylip_files/test_n2.phy
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    60228 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/phylip_files/test_n500.phy
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:37.656921 pg-sui-0.2.3/pgsui/example_data/popmaps/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/popmaps/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     1954 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/popmaps/test.popmap
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:37.926466 pg-sui-0.2.3/pgsui/example_data/structure_files/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/structure_files/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     6375 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/structure_files/test.nopops.1row.10sites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    50808 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/structure_files/test.nopops.2row.100sites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     7978 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/structure_files/test.nopops.2row.10sites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    17512 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/structure_files/test.nopops.2row.30sites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)   967410 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/structure_files/test.nopops.2row.allsites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     6609 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/structure_files/test.pops.1row.10sites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     8446 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/structure_files/test.pops.2row.10sites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)   967878 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/structure_files/test.pops.2row.allsites.str
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:38.305417 pg-sui-0.2.3/pgsui/example_data/trees/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/trees/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    25575 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/trees/test.iqtree
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)      134 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/trees/test.qmat
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    46013 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/trees/test.rate
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     4696 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/trees/test.tre
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)      678 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/trees/test_n10.rate
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2577 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/trees/test_n100.rate
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    11387 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/trees/test_n500.rate
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    16235 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/trees/test_siterates.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)       80 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/trees/test_siterates_n10.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)      804 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/trees/test_siterates_n100.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     4008 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/trees/test_siterates_n500.txt
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:38.405684 pg-sui-0.2.3/pgsui/example_data/vcf_files/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)   380243 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/vcf_files/test.vcf
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    72705 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/vcf_files/test.vcf.gz
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2581 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/vcf_files/test.vcf.gz.tbi
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:38.505948 pg-sui-0.2.3/pgsui/impute/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:44.000000 pg-sui-0.2.3/pgsui/impute/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)   125036 2023-07-23 04:28:26.000000 pg-sui-0.2.3/pgsui/impute/estimators.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    51210 2023-07-23 04:24:44.000000 pg-sui-0.2.3/pgsui/impute/impute.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    53283 2023-07-23 04:24:44.000000 pg-sui-0.2.3/pgsui/impute/simple_imputers.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:38.590601 pg-sui-0.2.3/pgsui/impute/supervised/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:44.000000 pg-sui-0.2.3/pgsui/impute/supervised/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    35075 2023-07-23 04:24:44.000000 pg-sui-0.2.3/pgsui/impute/supervised/iterative_imputer_fixedparams.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    45443 2023-07-23 04:24:44.000000 pg-sui-0.2.3/pgsui/impute/supervised/iterative_imputer_gridsearch.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:38.744176 pg-sui-0.2.3/pgsui/impute/unsupervised/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:44.000000 pg-sui-0.2.3/pgsui/impute/unsupervised/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     9682 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/impute/unsupervised/callbacks.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    29483 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/impute/unsupervised/keras_classifiers.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:38.944728 pg-sui-0.2.3/pgsui/impute/unsupervised/models/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/impute/unsupervised/models/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    20161 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/impute/unsupervised/models/autoencoder_model.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:39.029366 pg-sui-0.2.3/pgsui/impute/unsupervised/models/in_development/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/impute/unsupervised/models/in_development/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    15036 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/impute/unsupervised/models/in_development/cnn_model.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14501 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/impute/unsupervised/models/nlpca_model.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    37879 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/impute/unsupervised/models/ubp_model.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    22338 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/impute/unsupervised/models/vae_model.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    52292 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/impute/unsupervised/neural_network_imputers.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    50830 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/impute/unsupervised/neural_network_methods.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     7471 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/pg_sui.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:39.145271 pg-sui-0.2.3/pgsui/utils/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/utils/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    15705 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/utils/misc.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    33748 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/utils/plotting.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    26862 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/utils/scorers.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    10143 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/utils/sequence_tools.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)       38 2023-07-23 05:30:39.345819 pg-sui-0.2.3/setup.cfg
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     3046 2023-07-23 05:28:48.000000 pg-sui-0.2.3/setup.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:39.207772 pg-sui-0.2.3/simulation/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:45.000000 pg-sui-0.2.3/simulation/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    11345 2023-07-23 04:24:46.000000 pg-sui-0.2.3/simulation/sim_benchmarks.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    13793 2023-07-23 04:24:46.000000 pg-sui-0.2.3/simulation/sim_treeparams.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:39.323670 pg-sui-0.2.3/test/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:46.000000 pg-sui-0.2.3/test/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     6024 2023-07-23 04:24:46.000000 pg-sui-0.2.3/test/pg_sui_simtest.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    15871 2023-07-23 04:24:46.000000 pg-sui-0.2.3/test/pg_sui_testing.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     5034 2023-07-23 05:26:30.000000 pg-sui-0.2.3/test/test.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14310 2023-07-23 04:24:46.000000 pg-sui-0.2.3/test/test_pgsui.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     5867 2023-07-23 04:24:46.000000 pg-sui-0.2.3/test/test_tkc.py
```

### Comparing `pg-sui-0.2.2/PG_SUI.egg-info/PKG-INFO` & `pg-sui-0.2.3/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pg-sui
-Version: 0.2.2
+Version: 0.2.3
 Summary: Python machine and deep learning package to impute missing SNPs
 Home-page: https://github.com/btmartin721/PG-SUI
 Author: Bradley T. Martin and Tyler K. Chafin
 Author-email: evobio721@gmail.com
 Maintainer: Bradley T. Martin
 Maintainer-email: evobio721@gmail.com
 License: GNU General Public License v3 (GPLv3)
```

### Comparing `pg-sui-0.2.2/PG_SUI.egg-info/SOURCES.txt` & `pg-sui-0.2.3/pg_sui.egg-info/SOURCES.txt`

 * *Files 10% similar despite different names*

```diff
@@ -1,16 +1,11 @@
+LICENSE
 MANIFEST.in
 README.md
-pyproject.toml
 setup.py
-PG_SUI.egg-info/PKG-INFO
-PG_SUI.egg-info/SOURCES.txt
-PG_SUI.egg-info/dependency_links.txt
-PG_SUI.egg-info/requires.txt
-PG_SUI.egg-info/top_level.txt
 pg_sui.egg-info/PKG-INFO
 pg_sui.egg-info/SOURCES.txt
 pg_sui.egg-info/dependency_links.txt
 pg_sui.egg-info/requires.txt
 pg_sui.egg-info/top_level.txt
 pgsui/__init__.py
 pgsui/pg_sui.py
```

### Comparing `pg-sui-0.2.2/PKG-INFO` & `pg-sui-0.2.3/pg_sui.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pg-sui
-Version: 0.2.2
+Version: 0.2.3
 Summary: Python machine and deep learning package to impute missing SNPs
 Home-page: https://github.com/btmartin721/PG-SUI
 Author: Bradley T. Martin and Tyler K. Chafin
 Author-email: evobio721@gmail.com
 Maintainer: Bradley T. Martin
 Maintainer-email: evobio721@gmail.com
 License: GNU General Public License v3 (GPLv3)
```

### Comparing `pg-sui-0.2.2/README.md` & `pg-sui-0.2.3/README.md`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/__init__.py` & `pg-sui-0.2.3/pgsui/__init__.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/data_processing/transformers.py` & `pg-sui-0.2.3/pgsui/data_processing/transformers.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/example_data/phylip_files/test.phy` & `pg-sui-0.2.3/pgsui/example_data/phylip_files/test.phy`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/example_data/phylip_files/test_n10.phy` & `pg-sui-0.2.3/pgsui/example_data/phylip_files/test_n10.phy`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/example_data/phylip_files/test_n100.phy` & `pg-sui-0.2.3/pgsui/example_data/phylip_files/test_n100.phy`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/example_data/phylip_files/test_n2.phy` & `pg-sui-0.2.3/pgsui/example_data/phylip_files/test_n2.phy`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/example_data/phylip_files/test_n500.phy` & `pg-sui-0.2.3/pgsui/example_data/phylip_files/test_n500.phy`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/example_data/popmaps/test.popmap` & `pg-sui-0.2.3/pgsui/example_data/popmaps/test.popmap`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/example_data/structure_files/test.nopops.1row.10sites.str` & `pg-sui-0.2.3/pgsui/example_data/structure_files/test.nopops.1row.10sites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/example_data/structure_files/test.nopops.2row.100sites.str` & `pg-sui-0.2.3/pgsui/example_data/structure_files/test.nopops.2row.100sites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/example_data/structure_files/test.nopops.2row.10sites.str` & `pg-sui-0.2.3/pgsui/example_data/structure_files/test.nopops.2row.10sites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/example_data/structure_files/test.nopops.2row.30sites.str` & `pg-sui-0.2.3/pgsui/example_data/structure_files/test.nopops.2row.30sites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/example_data/structure_files/test.nopops.2row.allsites.str` & `pg-sui-0.2.3/pgsui/example_data/structure_files/test.nopops.2row.allsites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/example_data/structure_files/test.pops.1row.10sites.str` & `pg-sui-0.2.3/pgsui/example_data/structure_files/test.pops.1row.10sites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/example_data/structure_files/test.pops.2row.10sites.str` & `pg-sui-0.2.3/pgsui/example_data/structure_files/test.pops.2row.10sites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/example_data/structure_files/test.pops.2row.allsites.str` & `pg-sui-0.2.3/pgsui/example_data/structure_files/test.pops.2row.allsites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/example_data/trees/test.iqtree` & `pg-sui-0.2.3/pgsui/example_data/trees/test.iqtree`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/example_data/trees/test.rate` & `pg-sui-0.2.3/pgsui/example_data/trees/test.rate`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/example_data/trees/test.tre` & `pg-sui-0.2.3/pgsui/example_data/trees/test.tre`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/example_data/trees/test_n10.rate` & `pg-sui-0.2.3/pgsui/example_data/trees/test_n10.rate`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/example_data/trees/test_n100.rate` & `pg-sui-0.2.3/pgsui/example_data/trees/test_n100.rate`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/example_data/trees/test_n500.rate` & `pg-sui-0.2.3/pgsui/example_data/trees/test_n500.rate`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/example_data/trees/test_siterates.txt` & `pg-sui-0.2.3/pgsui/example_data/trees/test_siterates.txt`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/example_data/trees/test_siterates_n100.txt` & `pg-sui-0.2.3/pgsui/example_data/trees/test_siterates_n100.txt`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/example_data/trees/test_siterates_n500.txt` & `pg-sui-0.2.3/pgsui/example_data/trees/test_siterates_n500.txt`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/example_data/vcf_files/test.vcf` & `pg-sui-0.2.3/pgsui/example_data/vcf_files/test.vcf`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/example_data/vcf_files/test.vcf.gz` & `pg-sui-0.2.3/pgsui/example_data/vcf_files/test.vcf.gz`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/example_data/vcf_files/test.vcf.gz.tbi` & `pg-sui-0.2.3/pgsui/example_data/vcf_files/test.vcf.gz.tbi`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/impute/estimators.py` & `pg-sui-0.2.3/pgsui/impute/estimators.py`

 * *Files 0% similar despite different names*

```diff
@@ -161,15 +161,15 @@
         population_size: Union[int, str] = "auto",
         tournament_size: int = 3,
         elitism: bool = True,
         crossover_probability: float = 0.8,
         mutation_probability: float = 0.2,
         ga_algorithm: str = "eaMuPlusLambda",
         early_stop_gen: int = 5,
-        scoring_metric: str = "roc_auc",
+        scoring_metric: str = "f1_weighted",
         chunk_size: Union[int, float] = 1.0,
         disable_progressbar: bool = False,
         progress_update_percent: Optional[int] = None,
         n_jobs: int = 1,
         verbose: int = 0,
     ) -> None:
         # Get local variables into dictionary object
@@ -353,15 +353,15 @@
         population_size: Union[int, str] = "auto",
         tournament_size: int = 3,
         elitism: bool = True,
         crossover_probability: float = 0.8,
         mutation_probability: float = 0.2,
         ga_algorithm: str = "eaMuPlusLambda",
         early_stop_gen: int = 5,
-        scoring_metric: str = "roc_auc",
+        scoring_metric: str = "f1_weighted",
         chunk_size: Union[int, float] = 1.0,
         disable_progressbar: bool = False,
         progress_update_percent: Optional[int] = None,
         n_jobs: int = 1,
         verbose: int = 0,
     ) -> None:
         # Get local variables into dictionary object
@@ -581,15 +581,15 @@
         population_size: Union[int, str] = "auto",
         tournament_size: int = 3,
         elitism: bool = True,
         crossover_probability: float = 0.8,
         mutation_probability: float = 0.2,
         ga_algorithm: str = "eaMuPlusLambda",
         early_stop_gen: int = 5,
-        scoring_metric: str = "roc_auc",
+        scoring_metric: str = "f1_weighted",
         chunk_size: Union[int, float] = 1.0,
         disable_progressbar: bool = False,
         progress_update_percent: Optional[int] = None,
         n_jobs: int = 1,
         verbose: int = 0,
     ) -> None:
         # Get local variables into dictionary object
@@ -725,22 +725,22 @@
         l1_penalty=1e-6,
         l2_penalty=1e-6,
         dropout_rate=0.2,
         kl_beta=1.0,
         sample_weights="auto",
         gridsearch_method="gridsearch",
         grid_iter=80,
-        scoring_metric="auc_macro",
+        scoring_metric="f1_weighted",
         population_size="auto",
         tournament_size=3,
         elitism=True,
         crossover_probability=0.8,
         mutation_probability=0.2,
         ga_algorithm="eaMuPlusLambda",
-        sim_strategy="random",
+        sim_strategy="random_weighted",
         sim_prop_missing=0.2,
         disable_progressbar=False,
         n_jobs=1,
         verbose=0,
         **kwargs,
     ):
         # Get local variables into dictionary object
@@ -888,22 +888,22 @@
         weights_initializer="glorot_normal",
         l1_penalty=1e-6,
         l2_penalty=1e-6,
         dropout_rate=0.2,
         sample_weights="auto",
         gridsearch_method="gridsearch",
         grid_iter=80,
-        scoring_metric="auc_macro",
+        scoring_metric="f1_weighted",
         population_size="auto",
         tournament_size=3,
         elitism=True,
         crossover_probability=0.8,
         mutation_probability=0.2,
         ga_algorithm="eaMuPlusLambda",
-        sim_strategy="random",
+        sim_strategy="random_weighted",
         sim_prop_missing=0.2,
         disable_progressbar=False,
         n_jobs=1,
         verbose=0,
         **kwargs,
     ):
         # Get local variables into dictionary object
@@ -1086,22 +1086,22 @@
         weights_initializer="glorot_normal",
         l1_penalty=1e-6,
         l2_penalty=1e-6,
         dropout_rate=0.2,
         sample_weights="auto",
         gridsearch_method="gridsearch",
         grid_iter=80,
-        scoring_metric="auc_macro",
+        scoring_metric="f1_weighted",
         population_size="auto",
         tournament_size=3,
         elitism=True,
         crossover_probability=0.8,
         mutation_probability=0.2,
         ga_algorithm="eaMuPlusLambda",
-        sim_strategy="random",
+        sim_strategy="random_weighted",
         sim_prop_missing=0.2,
         disable_progressbar=False,
         n_jobs=1,
         verbose=0,
         **kwargs,
     ):
         # Get local variables into dictionary object
```

### Comparing `pg-sui-0.2.2/pgsui/impute/impute.py` & `pg-sui-0.2.3/pgsui/impute/impute.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/impute/simple_imputers.py` & `pg-sui-0.2.3/pgsui/impute/simple_imputers.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/impute/supervised/iterative_imputer_fixedparams.py` & `pg-sui-0.2.3/pgsui/impute/supervised/iterative_imputer_fixedparams.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/impute/supervised/iterative_imputer_gridsearch.py` & `pg-sui-0.2.3/pgsui/impute/supervised/iterative_imputer_gridsearch.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/impute/unsupervised/callbacks.py` & `pg-sui-0.2.3/pgsui/impute/unsupervised/callbacks.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/impute/unsupervised/keras_classifiers.py` & `pg-sui-0.2.3/pgsui/impute/unsupervised/keras_classifiers.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/impute/unsupervised/models/autoencoder_model.py` & `pg-sui-0.2.3/pgsui/impute/unsupervised/models/autoencoder_model.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/impute/unsupervised/models/in_development/cnn_model.py` & `pg-sui-0.2.3/pgsui/impute/unsupervised/models/in_development/cnn_model.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/impute/unsupervised/models/nlpca_model.py` & `pg-sui-0.2.3/pgsui/impute/unsupervised/models/nlpca_model.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/impute/unsupervised/models/ubp_model.py` & `pg-sui-0.2.3/pgsui/impute/unsupervised/models/ubp_model.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/impute/unsupervised/models/vae_model.py` & `pg-sui-0.2.3/pgsui/impute/unsupervised/models/vae_model.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/impute/unsupervised/neural_network_imputers.py` & `pg-sui-0.2.3/pgsui/impute/unsupervised/neural_network_imputers.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/impute/unsupervised/neural_network_methods.py` & `pg-sui-0.2.3/pgsui/impute/unsupervised/neural_network_methods.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/pg_sui.py` & `pg-sui-0.2.3/pgsui/pg_sui.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/utils/misc.py` & `pg-sui-0.2.3/pgsui/utils/misc.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/utils/plotting.py` & `pg-sui-0.2.3/pgsui/utils/plotting.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/utils/scorers.py` & `pg-sui-0.2.3/pgsui/utils/scorers.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pgsui/utils/sequence_tools.py` & `pg-sui-0.2.3/pgsui/utils/sequence_tools.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/pyproject.toml` & `pg-sui-0.2.3/setup.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,76 +1,102 @@
-[build-system]
-requires = ["setuptools", "wheel"]
-build-backend = "setuptools.build_meta"
+from setuptools import setup, find_packages
+import os
 
-[project]
-name = "pg-sui"
-version = "0.2.2"
-authors = [
-    { name="Bradley T. Martin", email="evobio721@gmail.com" }, 
-    { name="Tyler K. Chafin", email="tylerkchafin@gmail.com" } 
-]
-description = "Python machine and deep learning package to impute missing SNPs"
-keywords=[
+
+def read(fname):
+    return open(os.path.join(os.path.dirname(__file__), fname)).read()
+
+
+NAME = "pg-sui"
+VERSION = "0.2.3"
+AUTHORS = "Bradley T. Martin and Tyler K. Chafin"
+AUTHOR_EMAIL = "evobio721@gmail.com"
+MAINTAINER = "Bradley T. Martin"
+DESCRIPTION = "Python machine and deep learning package to impute missing SNPs"
+LONG_DESCRIPTION = open("README.md").read()
+
+setup(
+    name=NAME,
+    version=VERSION,
+    author=AUTHORS,
+    author_email=AUTHOR_EMAIL,
+    maintainer=MAINTAINER,
+    maintainer_email=AUTHOR_EMAIL,
+    description=DESCRIPTION,
+    long_description=LONG_DESCRIPTION,
+    long_description_content_type="text/markdown",
+    url="https://github.com/btmartin721/PG-SUI",
+    project_urls={
+        "Homepage": "https://github.com/btmartin721/PG-SUI",
+        "Documentation": "https://pg-sui.readthedocs.io/en/latest/",
+        "Source": "https://github.com/btmartin721/PG-SUI.git",
+        "Bug Tracker": "https://github.com/btmartin721/PG-SUI/issues",
+    },
+    keywords=[
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
         "deep learning",
-        "population genomics"
-]
-readme = "README.md"
-requires-python = ">=3.8"
-license = {text = "GPL3 License"}
-classifiers=[
-    "Programming Language :: Python :: 3",
-    "Programming Language :: Python :: 3",
-    "Programming Language :: Python :: 3.8",
-    "Programming Language :: Python :: 3.9",
-    "Programming Language :: Python :: 3.10",
-    "Programming Language :: Python :: 3.11",
-    "Development Status :: 4 - Beta",
-    "Intended Audience :: Science/Research",
-    "License :: OSI Approved :: GNU General Public License v3 (GPLv3)",
-    "Topic :: Scientific/Engineering :: Bio-Informatics",
-    "Operating System :: OS Independent",
-    "Natural Language :: English",
-]
-dependencies = [
-    "matplotlib",
-    "seaborn",
-    "jupyterlab",
-    "scikit-learn>=1.0",
-    "tqdm",
-    "pandas",
-    "numpy==1.24.3",
-    "scipy",
-    "xgboost",
-    "tensorflow",
-    "keras",
-    "toytree",
-    "sklearn-genetic-opt[all]>=0.6.0",
-    "importlib-resources>=1.1.0",
-    "pyvolve",
-    "scikeras",
-    "snpio",
-    "urllib3>=1.26.7,<2.0.0",
-    "typing-extensions<4.6.0",
-]
-
-[project.optional-dependencies]
-docs = ["sphinx<7", "sphinx-rtd-theme", "sphinx-autodoc-typehints"]
-intel = ["scikit-learn-intelex"]
-
-[project.urls]
-"Homepage" = "https://github.com/btmartin721/PG-SUI.git"
-"Documentation" = "https://pg-sui.readthedocs.io/en/latest/"
-"Source" = "https://github.com/btmartin721/PG-SUI.git"
-"Bug Tracker" = "https://github.com/btmartin721/PG-SUI/issues"
+        "population genomics",
+    ],
+    classifiers=[
+        "Programming Language :: Python :: 3",
+        "Programming Language :: Python :: 3",
+        "Programming Language :: Python :: 3.8",
+        "Programming Language :: Python :: 3.9",
+        "Programming Language :: Python :: 3.10",
+        "Programming Language :: Python :: 3.11",
+        "Development Status :: 4 - Beta",
+        "Intended Audience :: Science/Research",
+        "License :: OSI Approved :: GNU General Public License v3 (GPLv3)",
+        "Topic :: Scientific/Engineering :: Bio-Informatics",
+        "Operating System :: OS Independent",
+        "Natural Language :: English",
+    ],
+    license="GNU General Public License v3 (GPLv3)",
+    packages=find_packages(),
+    python_requires=">=3.8,<4",
+    install_requires=[
+        "matplotlib",
+        "seaborn",
+        "jupyterlab",
+        "scikit-learn>=1.0",
+        "tqdm",
+        "pandas",
+        "numpy==1.24.3",
+        "scipy",
+        "xgboost",
+        "tensorflow",
+        "keras",
+        "toytree",
+        "sklearn-genetic-opt[all]>=0.6.0",
+        "importlib-resources>=1.1.0",
+        "pyvolve",
+        "scikeras",
+        "snpio",
+        "urllib3>=1.26.7,<2.0.0",
+        "typing-extensions<4.6.0",
+    ],
+    extras_require={
+        "intel": ["scikit-learn-intelex"],
+        "docs": ["sphinx<7", "sphinx-rtd-theme", "sphinx_autodoc_typehints"],
+    },
+    package_data={
+        "pgsui": [
+            "example_data/structure_files/*.str",
+            "example_data/phylip_files/*.phy",
+            "example_data/vcf_files/*",
+            "example_data/popmaps/test.popmap",
+            "example_data/trees/*",
+        ]
+    },
+    include_package_data=True,
+)
```

### Comparing `pg-sui-0.2.2/simulation/sim_benchmarks.py` & `pg-sui-0.2.3/simulation/sim_benchmarks.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/simulation/sim_treeparams.py` & `pg-sui-0.2.3/simulation/sim_treeparams.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/test/pg_sui_simtest.py` & `pg-sui-0.2.3/test/pg_sui_simtest.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/test/pg_sui_testing.py` & `pg-sui-0.2.3/test/pg_sui_testing.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/test/test.py` & `pg-sui-0.2.3/test/test.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/test/test_pgsui.py` & `pg-sui-0.2.3/test/test_pgsui.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.2/test/test_tkc.py` & `pg-sui-0.2.3/test/test_tkc.py`

 * *Files identical despite different names*

