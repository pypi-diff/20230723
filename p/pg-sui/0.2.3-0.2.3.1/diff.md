# Comparing `tmp/pg-sui-0.2.3.tar.gz` & `tmp/pg-sui-0.2.3.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pg-sui-0.2.3.tar", last modified: Sun Jul 23 05:30:39 2023, max compression
+gzip compressed data, was "pg-sui-0.2.3.1.tar", last modified: Sun Jul 23 05:53:06 2023, max compression
```

## Comparing `pg-sui-0.2.3.tar` & `pg-sui-0.2.3.1.tar`

### file list

```diff
@@ -1,99 +1,99 @@
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:39.345819 pg-sui-0.2.3/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    35149 2023-07-16 18:34:37.000000 pg-sui-0.2.3/LICENSE
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)      220 2023-07-22 21:23:30.000000 pg-sui-0.2.3/MANIFEST.in
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14102 2023-07-23 05:30:39.345819 pg-sui-0.2.3/PKG-INFO
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    10444 2023-07-23 01:57:24.000000 pg-sui-0.2.3/README.md
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:37.302699 pg-sui-0.2.3/pg_sui.egg-info/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14102 2023-07-23 05:30:35.000000 pg-sui-0.2.3/pg_sui.egg-info/PKG-INFO
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2994 2023-07-23 05:30:36.000000 pg-sui-0.2.3/pg_sui.egg-info/SOURCES.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        1 2023-07-23 05:30:35.000000 pg-sui-0.2.3/pg_sui.egg-info/dependency_links.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)      331 2023-07-23 05:30:35.000000 pg-sui-0.2.3/pg_sui.egg-info/requires.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)       22 2023-07-23 05:30:35.000000 pg-sui-0.2.3/pg_sui.egg-info/top_level.txt
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:37.340469 pg-sui-0.2.3/pgsui/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     1449 2023-07-23 04:24:42.000000 pg-sui-0.2.3/pgsui/__init__.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:37.387346 pg-sui-0.2.3/pgsui/data_processing/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:42.000000 pg-sui-0.2.3/pgsui/data_processing/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    42452 2023-07-23 04:24:42.000000 pg-sui-0.2.3/pgsui/data_processing/transformers.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:37.425103 pg-sui-0.2.3/pgsui/example_data/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:42.000000 pg-sui-0.2.3/pgsui/example_data/__init__.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:37.587893 pg-sui-0.2.3/pgsui/example_data/phylip_files/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/phylip_files/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)   238537 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/phylip_files/test.phy
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2897 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/phylip_files/test_n10.phy
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    13428 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/phylip_files/test_n100.phy
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     1960 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/phylip_files/test_n2.phy
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    60228 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/phylip_files/test_n500.phy
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:37.656921 pg-sui-0.2.3/pgsui/example_data/popmaps/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/popmaps/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     1954 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/popmaps/test.popmap
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:37.926466 pg-sui-0.2.3/pgsui/example_data/structure_files/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/structure_files/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     6375 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/structure_files/test.nopops.1row.10sites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    50808 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/structure_files/test.nopops.2row.100sites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     7978 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/structure_files/test.nopops.2row.10sites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    17512 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/structure_files/test.nopops.2row.30sites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)   967410 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/structure_files/test.nopops.2row.allsites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     6609 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/structure_files/test.pops.1row.10sites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     8446 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/structure_files/test.pops.2row.10sites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)   967878 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/structure_files/test.pops.2row.allsites.str
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:38.305417 pg-sui-0.2.3/pgsui/example_data/trees/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/trees/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    25575 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/trees/test.iqtree
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)      134 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/trees/test.qmat
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    46013 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/trees/test.rate
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     4696 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/trees/test.tre
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)      678 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/trees/test_n10.rate
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2577 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/trees/test_n100.rate
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    11387 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/trees/test_n500.rate
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    16235 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/trees/test_siterates.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)       80 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/trees/test_siterates_n10.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)      804 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/trees/test_siterates_n100.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     4008 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/trees/test_siterates_n500.txt
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:38.405684 pg-sui-0.2.3/pgsui/example_data/vcf_files/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)   380243 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/vcf_files/test.vcf
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    72705 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/vcf_files/test.vcf.gz
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2581 2023-07-23 04:24:43.000000 pg-sui-0.2.3/pgsui/example_data/vcf_files/test.vcf.gz.tbi
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:38.505948 pg-sui-0.2.3/pgsui/impute/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:44.000000 pg-sui-0.2.3/pgsui/impute/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)   125036 2023-07-23 04:28:26.000000 pg-sui-0.2.3/pgsui/impute/estimators.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    51210 2023-07-23 04:24:44.000000 pg-sui-0.2.3/pgsui/impute/impute.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    53283 2023-07-23 04:24:44.000000 pg-sui-0.2.3/pgsui/impute/simple_imputers.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:38.590601 pg-sui-0.2.3/pgsui/impute/supervised/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:44.000000 pg-sui-0.2.3/pgsui/impute/supervised/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    35075 2023-07-23 04:24:44.000000 pg-sui-0.2.3/pgsui/impute/supervised/iterative_imputer_fixedparams.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    45443 2023-07-23 04:24:44.000000 pg-sui-0.2.3/pgsui/impute/supervised/iterative_imputer_gridsearch.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:38.744176 pg-sui-0.2.3/pgsui/impute/unsupervised/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:44.000000 pg-sui-0.2.3/pgsui/impute/unsupervised/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     9682 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/impute/unsupervised/callbacks.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    29483 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/impute/unsupervised/keras_classifiers.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:38.944728 pg-sui-0.2.3/pgsui/impute/unsupervised/models/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/impute/unsupervised/models/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    20161 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/impute/unsupervised/models/autoencoder_model.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:39.029366 pg-sui-0.2.3/pgsui/impute/unsupervised/models/in_development/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/impute/unsupervised/models/in_development/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    15036 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/impute/unsupervised/models/in_development/cnn_model.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14501 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/impute/unsupervised/models/nlpca_model.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    37879 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/impute/unsupervised/models/ubp_model.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    22338 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/impute/unsupervised/models/vae_model.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    52292 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/impute/unsupervised/neural_network_imputers.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    50830 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/impute/unsupervised/neural_network_methods.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     7471 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/pg_sui.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:39.145271 pg-sui-0.2.3/pgsui/utils/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/utils/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    15705 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/utils/misc.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    33748 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/utils/plotting.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    26862 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/utils/scorers.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    10143 2023-07-23 04:24:45.000000 pg-sui-0.2.3/pgsui/utils/sequence_tools.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)       38 2023-07-23 05:30:39.345819 pg-sui-0.2.3/setup.cfg
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     3046 2023-07-23 05:28:48.000000 pg-sui-0.2.3/setup.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:39.207772 pg-sui-0.2.3/simulation/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:45.000000 pg-sui-0.2.3/simulation/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    11345 2023-07-23 04:24:46.000000 pg-sui-0.2.3/simulation/sim_benchmarks.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    13793 2023-07-23 04:24:46.000000 pg-sui-0.2.3/simulation/sim_treeparams.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:30:39.323670 pg-sui-0.2.3/test/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:46.000000 pg-sui-0.2.3/test/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     6024 2023-07-23 04:24:46.000000 pg-sui-0.2.3/test/pg_sui_simtest.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    15871 2023-07-23 04:24:46.000000 pg-sui-0.2.3/test/pg_sui_testing.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     5034 2023-07-23 05:26:30.000000 pg-sui-0.2.3/test/test.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14310 2023-07-23 04:24:46.000000 pg-sui-0.2.3/test/test_pgsui.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     5867 2023-07-23 04:24:46.000000 pg-sui-0.2.3/test/test_tkc.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:06.001230 pg-sui-0.2.3.1/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    35149 2023-07-16 18:34:37.000000 pg-sui-0.2.3.1/LICENSE
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)      220 2023-07-22 21:23:30.000000 pg-sui-0.2.3.1/MANIFEST.in
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14104 2023-07-23 05:53:06.001230 pg-sui-0.2.3.1/PKG-INFO
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    10444 2023-07-23 01:57:24.000000 pg-sui-0.2.3.1/README.md
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:03.796829 pg-sui-0.2.3.1/pg_sui.egg-info/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14104 2023-07-23 05:53:02.000000 pg-sui-0.2.3.1/pg_sui.egg-info/PKG-INFO
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2994 2023-07-23 05:53:02.000000 pg-sui-0.2.3.1/pg_sui.egg-info/SOURCES.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        1 2023-07-23 05:53:02.000000 pg-sui-0.2.3.1/pg_sui.egg-info/dependency_links.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)      331 2023-07-23 05:53:02.000000 pg-sui-0.2.3.1/pg_sui.egg-info/requires.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)       22 2023-07-23 05:53:02.000000 pg-sui-0.2.3.1/pg_sui.egg-info/top_level.txt
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:03.834590 pg-sui-0.2.3.1/pgsui/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     1449 2023-07-23 04:24:42.000000 pg-sui-0.2.3.1/pgsui/__init__.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:03.881476 pg-sui-0.2.3.1/pgsui/data_processing/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:42.000000 pg-sui-0.2.3.1/pgsui/data_processing/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    42452 2023-07-23 04:24:42.000000 pg-sui-0.2.3.1/pgsui/data_processing/transformers.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:03.912726 pg-sui-0.2.3.1/pgsui/example_data/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:42.000000 pg-sui-0.2.3.1/pgsui/example_data/__init__.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:04.082015 pg-sui-0.2.3.1/pgsui/example_data/phylip_files/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/phylip_files/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)   238537 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/phylip_files/test.phy
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2897 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/phylip_files/test_n10.phy
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    13428 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/phylip_files/test_n100.phy
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     1960 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/phylip_files/test_n2.phy
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    60228 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/phylip_files/test_n500.phy
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:04.135401 pg-sui-0.2.3.1/pgsui/example_data/popmaps/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/popmaps/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     1954 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/popmaps/test.popmap
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:04.451555 pg-sui-0.2.3.1/pgsui/example_data/structure_files/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/structure_files/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     6375 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.nopops.1row.10sites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    50808 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.nopops.2row.100sites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     7978 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.nopops.2row.10sites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    17512 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.nopops.2row.30sites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)   967410 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.nopops.2row.allsites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     6609 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.pops.1row.10sites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     8446 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.pops.2row.10sites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)   967878 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.pops.2row.allsites.str
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:04.917959 pg-sui-0.2.3.1/pgsui/example_data/trees/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/trees/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    25575 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/trees/test.iqtree
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)      134 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/trees/test.qmat
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    46013 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/trees/test.rate
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     4696 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/trees/test.tre
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)      678 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/trees/test_n10.rate
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2577 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/trees/test_n100.rate
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    11387 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/trees/test_n500.rate
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    16235 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/trees/test_siterates.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)       80 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/trees/test_siterates_n10.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)      804 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/trees/test_siterates_n100.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     4008 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/trees/test_siterates_n500.txt
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:05.034303 pg-sui-0.2.3.1/pgsui/example_data/vcf_files/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)   380243 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/vcf_files/test.vcf
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    72705 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/vcf_files/test.vcf.gz
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2581 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/vcf_files/test.vcf.gz.tbi
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:05.134302 pg-sui-0.2.3.1/pgsui/impute/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:44.000000 pg-sui-0.2.3.1/pgsui/impute/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)   116270 2023-07-23 05:46:21.000000 pg-sui-0.2.3.1/pgsui/impute/estimators.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    51210 2023-07-23 04:24:44.000000 pg-sui-0.2.3.1/pgsui/impute/impute.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    53283 2023-07-23 04:24:44.000000 pg-sui-0.2.3.1/pgsui/impute/simple_imputers.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:05.223016 pg-sui-0.2.3.1/pgsui/impute/supervised/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:44.000000 pg-sui-0.2.3.1/pgsui/impute/supervised/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    35075 2023-07-23 04:24:44.000000 pg-sui-0.2.3.1/pgsui/impute/supervised/iterative_imputer_fixedparams.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    45443 2023-07-23 04:24:44.000000 pg-sui-0.2.3.1/pgsui/impute/supervised/iterative_imputer_gridsearch.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:05.423044 pg-sui-0.2.3.1/pgsui/impute/unsupervised/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:44.000000 pg-sui-0.2.3.1/pgsui/impute/unsupervised/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     9682 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/impute/unsupervised/callbacks.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    29483 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/impute/unsupervised/keras_classifiers.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:05.599595 pg-sui-0.2.3.1/pgsui/impute/unsupervised/models/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/impute/unsupervised/models/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    20161 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/impute/unsupervised/models/autoencoder_model.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:05.669152 pg-sui-0.2.3.1/pgsui/impute/unsupervised/models/in_development/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/impute/unsupervised/models/in_development/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    15036 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/impute/unsupervised/models/in_development/cnn_model.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14501 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/impute/unsupervised/models/nlpca_model.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    37879 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/impute/unsupervised/models/ubp_model.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    22338 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/impute/unsupervised/models/vae_model.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    52292 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/impute/unsupervised/neural_network_imputers.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    50830 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/impute/unsupervised/neural_network_methods.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     7471 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/pg_sui.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:05.800673 pg-sui-0.2.3.1/pgsui/utils/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/utils/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    15705 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/utils/misc.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    33748 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/utils/plotting.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    26862 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/utils/scorers.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    10143 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/utils/sequence_tools.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)       38 2023-07-23 05:53:06.001230 pg-sui-0.2.3.1/setup.cfg
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     3048 2023-07-23 05:52:05.000000 pg-sui-0.2.3.1/setup.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:05.869698 pg-sui-0.2.3.1/simulation/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/simulation/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    11345 2023-07-23 04:24:46.000000 pg-sui-0.2.3.1/simulation/sim_benchmarks.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    13793 2023-07-23 04:24:46.000000 pg-sui-0.2.3.1/simulation/sim_treeparams.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:05.985599 pg-sui-0.2.3.1/test/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:46.000000 pg-sui-0.2.3.1/test/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     6024 2023-07-23 04:24:46.000000 pg-sui-0.2.3.1/test/pg_sui_simtest.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    15871 2023-07-23 04:24:46.000000 pg-sui-0.2.3.1/test/pg_sui_testing.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     5034 2023-07-23 05:26:30.000000 pg-sui-0.2.3.1/test/test.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14310 2023-07-23 04:24:46.000000 pg-sui-0.2.3.1/test/test_pgsui.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     5867 2023-07-23 04:24:46.000000 pg-sui-0.2.3.1/test/test_tkc.py
```

### Comparing `pg-sui-0.2.3/LICENSE` & `pg-sui-0.2.3.1/LICENSE`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/PKG-INFO` & `pg-sui-0.2.3.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pg-sui
-Version: 0.2.3
+Version: 0.2.3.1
 Summary: Python machine and deep learning package to impute missing SNPs
 Home-page: https://github.com/btmartin721/PG-SUI
 Author: Bradley T. Martin and Tyler K. Chafin
 Author-email: evobio721@gmail.com
 Maintainer: Bradley T. Martin
 Maintainer-email: evobio721@gmail.com
 License: GNU General Public License v3 (GPLv3)
```

### Comparing `pg-sui-0.2.3/README.md` & `pg-sui-0.2.3.1/README.md`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pg_sui.egg-info/PKG-INFO` & `pg-sui-0.2.3.1/pg_sui.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pg-sui
-Version: 0.2.3
+Version: 0.2.3.1
 Summary: Python machine and deep learning package to impute missing SNPs
 Home-page: https://github.com/btmartin721/PG-SUI
 Author: Bradley T. Martin and Tyler K. Chafin
 Author-email: evobio721@gmail.com
 Maintainer: Bradley T. Martin
 Maintainer-email: evobio721@gmail.com
 License: GNU General Public License v3 (GPLv3)
```

### Comparing `pg-sui-0.2.3/pg_sui.egg-info/SOURCES.txt` & `pg-sui-0.2.3.1/pg_sui.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/__init__.py` & `pg-sui-0.2.3.1/pgsui/__init__.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/data_processing/transformers.py` & `pg-sui-0.2.3.1/pgsui/data_processing/transformers.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/example_data/phylip_files/test.phy` & `pg-sui-0.2.3.1/pgsui/example_data/phylip_files/test.phy`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/example_data/phylip_files/test_n10.phy` & `pg-sui-0.2.3.1/pgsui/example_data/phylip_files/test_n10.phy`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/example_data/phylip_files/test_n100.phy` & `pg-sui-0.2.3.1/pgsui/example_data/phylip_files/test_n100.phy`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/example_data/phylip_files/test_n2.phy` & `pg-sui-0.2.3.1/pgsui/example_data/phylip_files/test_n2.phy`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/example_data/phylip_files/test_n500.phy` & `pg-sui-0.2.3.1/pgsui/example_data/phylip_files/test_n500.phy`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/example_data/popmaps/test.popmap` & `pg-sui-0.2.3.1/pgsui/example_data/popmaps/test.popmap`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/example_data/structure_files/test.nopops.1row.10sites.str` & `pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.nopops.1row.10sites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/example_data/structure_files/test.nopops.2row.100sites.str` & `pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.nopops.2row.100sites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/example_data/structure_files/test.nopops.2row.10sites.str` & `pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.nopops.2row.10sites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/example_data/structure_files/test.nopops.2row.30sites.str` & `pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.nopops.2row.30sites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/example_data/structure_files/test.nopops.2row.allsites.str` & `pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.nopops.2row.allsites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/example_data/structure_files/test.pops.1row.10sites.str` & `pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.pops.1row.10sites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/example_data/structure_files/test.pops.2row.10sites.str` & `pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.pops.2row.10sites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/example_data/structure_files/test.pops.2row.allsites.str` & `pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.pops.2row.allsites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/example_data/trees/test.iqtree` & `pg-sui-0.2.3.1/pgsui/example_data/trees/test.iqtree`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/example_data/trees/test.rate` & `pg-sui-0.2.3.1/pgsui/example_data/trees/test.rate`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/example_data/trees/test.tre` & `pg-sui-0.2.3.1/pgsui/example_data/trees/test.tre`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/example_data/trees/test_n10.rate` & `pg-sui-0.2.3.1/pgsui/example_data/trees/test_n10.rate`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/example_data/trees/test_n100.rate` & `pg-sui-0.2.3.1/pgsui/example_data/trees/test_n100.rate`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/example_data/trees/test_n500.rate` & `pg-sui-0.2.3.1/pgsui/example_data/trees/test_n500.rate`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/example_data/trees/test_siterates.txt` & `pg-sui-0.2.3.1/pgsui/example_data/trees/test_siterates.txt`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/example_data/trees/test_siterates_n100.txt` & `pg-sui-0.2.3.1/pgsui/example_data/trees/test_siterates_n100.txt`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/example_data/trees/test_siterates_n500.txt` & `pg-sui-0.2.3.1/pgsui/example_data/trees/test_siterates_n500.txt`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/example_data/vcf_files/test.vcf` & `pg-sui-0.2.3.1/pgsui/example_data/vcf_files/test.vcf`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/example_data/vcf_files/test.vcf.gz` & `pg-sui-0.2.3.1/pgsui/example_data/vcf_files/test.vcf.gz`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/example_data/vcf_files/test.vcf.gz.tbi` & `pg-sui-0.2.3.1/pgsui/example_data/vcf_files/test.vcf.gz.tbi`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/impute/estimators.py` & `pg-sui-0.2.3.1/pgsui/impute/estimators.py`

 * *Files 9% similar despite different names*

```diff
@@ -79,15 +79,15 @@
 
         mutation_probability (float, optional): For genetic algorithm grid search: Probability of child mutation. See GASearchCV documentation. Defaults to 0.2.
 
         ga_algorithm (str, optional): For genetic algorithm grid search: Evolutionary algorithm to use. Supported options include: {"eaMuPlusLambda", "eaMuCommaLambda", "eaSimple"}. If you need to speed up the genetic algorithm grid search, try setting ``algorithm`` to "euSimple", at the expense of evolutionary model robustness. See more details in the DEAP algorithms documentation (https://deap.readthedocs.io). Defaults to "eaMuPlusLambda".
 
         early_stop_gen (int, optional): If the genetic algorithm sees ``early_stop_gen`` consecutive generations without improvement in the scoring metric, an early stopping callback is implemented. This saves time by reducing the number of generations the genetic algorithm has to perform. Defaults to 5.
 
-        scoring_metric (str, optional): Scoring metric to use for randomized or genetic algorithm grid searches. See https://scikit-learn.org/stable/modules/model_evaluation.html for supported options. Defaults to "roc_auc".
+        scoring_metric (str, optional): Scoring metric to use for grid searches. See the classification metrics in the scikit-learn documentation (https://scikit-learn.org/stable/modules/model_evaluation.html) for supported options. Defaults to "f1_weighted".
 
         chunk_size (int or float, optional): Number of loci for which to perform IterativeImputer at one time. Useful for reducing the memory usage if you are running out of RAM. If integer is specified, selects ``chunk_size`` loci at a time. If a float is specified, selects ``math.ceil(total_loci * chunk_size)`` loci at a time]. Defaults to 1.0 (all features).
 
         disable_progressbar (bool, optional): Whether or not to disable the tqdm progress bar when doing the imputation. If True, progress bar is disabled, which is useful when running the imputation on e.g. an HPC cluster. If the bar is disabled, a status update will be printed to standard output for each iteration and feature instead. If False, the tqdm progress bar will be used. Defaults to False.
 
         progress_update_percent (int or None, optional): Print status updates for features every ``progress_update_percent``\%. IterativeImputer iterations will always be printed, but ``progress_update_percent`` involves iteration progress through the features of each IterativeImputer iteration. If None, then does not print progress through features. Defaults to None.
 
@@ -261,15 +261,15 @@
 
         mutation_probability (float, optional): For genetic algorithm grid search: Probability of child mutation. See GASearchCV documentation. Defaults to 0.2.
 
         ga_algorithm (str, optional): For genetic algorithm grid search: Evolutionary algorithm to use. Supported options include: {"eaMuPlusLambda", "eaMuCommaLambda", "eaSimple"}. If you need to speed up the genetic algorithm grid search, try setting ``algorithm`` to "euSimple", at the expense of evolutionary model robustness. See more details in the DEAP algorithms documentation (https://deap.readthedocs.io). Defaults to "eaMuPlusLambda".
 
         early_stop_gen (int, optional): If the genetic algorithm sees ``early_stop_gen`` consecutive generations without improvement in the scoring metric, an early stopping callback is implemented. This saves time by reducing the number of generations the genetic algorithm has to perform. Defaults to 5.
 
-        scoring_metric (str, optional): Scoring metric to use for randomized or genetic algorithm grid searches. See https://scikit-learn.org/stable/modules/model_evaluation.html for supported options. Defaults to "roc_auc".
+        scoring_metric (str, optional): Scoring metric to use for grid searches. See the classification metrics in the scikit-learn documentation (https://scikit-learn.org/stable/modules/model_evaluation.html) for supported options. Defaults to "f1_weighted".
 
         column_subset (int or float, optional): If float, proportion of the dataset to randomly subset for the grid search. Should be between 0 and 1, and should also be small, because the grid search takes a long time. If int, subset ``column_subset`` columns. If float, subset ``int(n_features * column_subset)`` columns. Defaults to 0.1.
 
         chunk_size (int or float, optional): Number of loci for which to perform IterativeImputer at one time. Useful for reducing the memory usage if you are running out of RAM. If integer is specified, selects ``chunk_size`` loci at a time. If a float is specified, selects ``math.ceil(total_loci * chunk_size)`` loci at a time]. Defaults to 1.0 (all features).
 
         disable_progressbar (bool, optional): Whether or not to disable the tqdm progress bar when doing the imputation. If True, progress bar is disabled, which is useful when running the imputation on e.g. an HPC cluster. If the bar is disabled, a status update will be printed to standard output for each iteration and feature instead. If False, the tqdm progress bar will be used. Defaults to False.
 
@@ -493,15 +493,15 @@
 
         mutation_probability (float, optional): For genetic algorithm grid search: Probability of child mutation. See GASearchCV documentation. Defaults to 0.2.
 
         ga_algorithm (str, optional): For genetic algorithm grid search: Evolutionary algorithm to use. Supported options include: {"eaMuPlusLambda", "eaMuCommaLambda", "eaSimple"}. If you need to speed up the genetic algorithm grid search, try setting ``algorithm`` to "euSimple", at the expense of evolutionary model robustness. See more details in the DEAP algorithms documentation (https://deap.readthedocs.io). Defaults to "eaMuPlusLambda".
 
         early_stop_gen (int, optional): If the genetic algorithm sees ``early_stop_gen`` consecutive generations without improvement in the scoring metric, an early stopping callback is implemented. This saves time by reducing the number of generations the genetic algorithm has to perform. Defaults to 5.
 
-        scoring_metric (str, optional): Scoring metric to use for randomized or genetic algorithm grid searches. See https://scikit-learn.org/stable/modules/model_evaluation.html for supported options. Defaults to "roc_auc".
+        scoring_metric (str, optional): Scoring metric to use for grid searches. See the classification metrics in the scikit-learn documentation (https://scikit-learn.org/stable/modules/model_evaluation.html) for supported options. Defaults to "f1_weighted".
 
         chunk_size (int or float, optional): Number of loci for which to perform IterativeImputer at one time. Useful for reducing the memory usage if you are running out of RAM. If integer is specified, selects ``chunk_size`` loci at a time. If a float is specified, selects ``math.ceil(total_loci * chunk_size)`` loci at a time. Defaults to 1.0 (all features).
 
         disable_progressbar (bool, optional): Whether or not to disable the tqdm progress bar when doing the imputation. If True, progress bar is disabled, which is useful when running the imputation on e.g. an HPC cluster. If the bar is disabled, a status update will be printed to standard output for each iteration and feature instead. If False, the tqdm progress bar will be used. Defaults to False.
 
         progress_update_percent (int or None, optional): Print status updates for features every ``progress_update_percent``\%. IterativeImputer iterations will always be printed, but ``progress_update_percent`` involves iteration progress through the features of each IterativeImputer iteration. If None, then does not print progress through features. Defaults to None.
 
@@ -652,15 +652,15 @@
 
         sample_weights (str, Dict[int, float], or None, optional): Weights for the 012-encoded classes during training. If None, then does not weight classes. If set to "auto", then class weights are automatically calculated for each column to balance classes (reference, heterozygous, and alternate alleles). If a dictionary is passed, it must contain 0, 1, and 2 as the keys and the class weights as the values. E.g., {0: 1.0, 1: 1.0, 2: 1.0}. The dictionary is then used as the overall class weights. If you wanted to prevent the model from learning to predict heterozygotes, for example, you could set the class weights to {0: 1.0, 1: 0.0, 2: 1.0}. Defaults to "auto" (balanced weighting).
 
         gridsearch_method (str, optional): Grid search method to use. Supported options include: {"gridsearch", "randomized_gridsearch", "genetic_algorithm"}. "gridsearch" uses GridSearchCV to test every possible parameter combination. "randomized_gridsearch" picks ``grid_iter`` random combinations of parameters to test. "genetic_algorithm" uses a genetic algorithm via the sklearn-genetic-opt GASearchCV module to do the grid search. If doing a grid search, "randomized_search" takes the least amount of time because it does not have to test all parameters. "genetic_algorithm" takes the longest. See the scikit-learn GridSearchCV and RandomizedSearchCV documentation for the "gridsearch" and "randomized_gridsearch" options, and the sklearn-genetic-opt GASearchCV documentation for the "genetic_algorithm" option. Defaults to "gridsearch".
 
         grid_iter (int, optional): Number of iterations to use for randomized and genetic algorithm grid searches. For randomized grid search, ``grid_iter`` parameter combinations will be randomly sampled. For the genetic algorithm, this determines how many generations the genetic algorithm will run. Defaults to 80.
 
-        scoring_metric (str, optional): Scoring metric to use for the grid search. Supported options include: {"auc_macro", "auc_micro", "precision_recall_macro", "precision_recall_micro", "accuracy", "hamming"}. Note that all metrics are automatically calculated when doing a grid search, the results of which are logged to a CSV file. However, when refitting following the grid search, the value passed to ``scoring_metric`` is used to select the best parameters. If you wish to choose the best parameters from a different metric, that information will also be in the CSV file. "auc_macro" and "auc_micro" get the AUC (area under curve) score for the ROC (Receiver Operating Characteristic) curve. The ROC curves plot the false positive rate (X-axis) versus the true positive rate (Y-axis) for each 012-encoded class and for the macro and micro averages among classes. The false positive rate is defined as: ``False Positive Rate = False Positives / (False Positives + True Negatives)`` and the true positive rate is defined as ``True Positive Rate = True Positives / (True Positives + False Negatives)``\. Macro averaging places equal importance on each class, whereas the micro average is the global average across all classes. AUC scores allow the ROC curve, and thus the model's classification skill, to be summarized as a single number. "precision_recall_macro" and "precision_recall_micro" create Precision-Recall (PR) curves for each class plus the macro and micro averages among classes. Precision is defined as ``True Positives / (True Positives + False Positives)`` and recall is defined as ``Recall = True Positives / (True Positives + False Negatives)``\. Reviewing both precision and recall is useful in cases where there is an imbalance in the observations between the two classes. For example, if there are many examples of major alleles (class 0) and only a few examples of minor alleles (class 2). PR curves take this into account, so use the Average Precision (AP) instead of AUC. AUC and AP are similar metrics, but AP summarizes a precision-recall curve as the weighted mean of precisions achieved at each probability threshold, with the increase in recall from the previous threshold used as the weight. On the contrary, AUC uses linear interpolation with the trapezoidal rule to calculate the area under the curve. "accuracy" calculates ``number of correct predictions / total predictions``\, but can often be misleading when used without considering the model's classification skill for each class. Defaults to "auc_macro".
+        scoring_metric (str, optional): Scoring metric to use for grid searches. See the classification metrics in the scikit-learn documentation (https://scikit-learn.org/stable/modules/model_evaluation.html) for supported options. Defaults to "f1_weighted".
 
         population_size (int or str, optional): Only used for the genetic algorithm grid search. Size of the initial population to sample randomly generated individuals. If set to "auto", then ``population_size`` is calculated as ``15 * n_parameters``\. If set to an integer, then uses the integer value as ``population_size``\. If you need to speed up the genetic algorithm grid search, try decreasing this parameter. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to "auto".
 
         tournament_size (int, optional): For genetic algorithm grid search only. Number of individuals to perform tournament selection. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to 3.
 
         elitism (bool, optional): For genetic algorithm grid search only. If set to True, takes the ``tournament_size`` best solution to the next generation. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to True.
 
@@ -815,15 +815,15 @@
 
         sample_weights (str, Dict[int, float], or None, optional): Weights for the 012-encoded classes during training. If None, then does not weight classes. If set to "auto", then class weights are automatically calculated for each column to balance classes (reference, heterozygous, and alternate alleles). If a dictionary is passed, it must contain 0, 1, and 2 as the keys and the class weights as the values. E.g., {0: 1.0, 1: 1.0, 2: 1.0}. The dictionary is then used as the overall class weights. If you wanted to prevent the model from learning to predict heterozygotes, for example, you could set the class weights to {0: 1.0, 1: 0.0, 2: 1.0}. Defaults to "auto" (balanced weighting).
 
         gridsearch_method (str, optional): Grid search method to use. Supported options include: {"gridsearch", "randomized_gridsearch", "genetic_algorithm"}. "gridsearch" uses GridSearchCV to test every possible parameter combination. "randomized_gridsearch" picks ``grid_iter`` random combinations of parameters to test. "genetic_algorithm" uses a genetic algorithm via the sklearn-genetic-opt GASearchCV module to do the grid search. If doing a grid search, "randomized_search" takes the least amount of time because it does not have to test all parameters. "genetic_algorithm" takes the longest. See the scikit-learn GridSearchCV and RandomizedSearchCV documentation for the "gridsearch" and "randomized_gridsearch" options, and the sklearn-genetic-opt GASearchCV documentation for the "genetic_algorithm" option. Defaults to "gridsearch".
 
         grid_iter (int, optional): Number of iterations to use for randomized and genetic algorithm grid searches. For randomized grid search, ``grid_iter`` parameter combinations will be randomly sampled. For the genetic algorithm, this determines how many generations the genetic algorithm will run. Defaults to 80.
 
-        scoring_metric (str, optional): Scoring metric to use for the grid search. Supported options include: {"auc_macro", "auc_micro", "precision_recall_macro", "precision_recall_micro", "accuracy"}. Note that all metrics are automatically calculated when doing a grid search, the results of which are logged to a CSV file. However, when refitting following the grid search, the value passed to ``scoring_metric`` is used to select the best parameters. If you wish to choose the best parameters from a different metric, that information will also be in the CSV file. "auc_macro" and "auc_micro" get the AUC (area under curve) score for the ROC (Receiver Operating Characteristic) curve. The ROC curves plot the false positive rate (X-axis) versus the true positive rate (Y-axis) for each 012-encoded class and for the macro and micro averages among classes. The false positive rate is defined as: ``False Positive Rate = False Positives / (False Positives + True Negatives)`` and the true positive rate is defined as ``True Positive Rate = True Positives / (True Positives + False Negatives)``\. Macro averaging places equal importance on each class, whereas the micro average is the global average across all classes. AUC scores allow the ROC curve, and thus the model's classification skill, to be summarized as a single number. "precision_recall_macro" and "precision_recall_micro" create Precision-Recall (PR) curves for each class plus the macro and micro averages among classes. Precision is defined as ``True Positives / (True Positives + False Positives)`` and recall is defined as ``Recall = True Positives / (True Positives + False Negatives)``\. Reviewing both precision and recall is useful in cases where there is an imbalance in the observations between the two classes. For example, if there are many examples of major alleles (class 0) and only a few examples of minor alleles (class 2). AUC and AP are similar metrics, but AP summarizes a precision-recall curve as the weighted mean of precisions achieved at each probability threshold, with the increase in recall from the previous threshold used as the weight. On the contrary, AUC uses linear interpolation with the trapezoidal rule to calculate the area under the curve. "accuracy" calculates ``number of correct predictions / total predictions``\, but can often be misleading when used without considering the model's classification skill for each class. Defaults to "auc_macro".
+        scoring_metric (str, optional): Scoring metric to use for grid searches. See the classification metrics in the scikit-learn documentation (https://scikit-learn.org/stable/modules/model_evaluation.html) for supported options. Defaults to "f1_weighted".
 
         population_size (int or str, optional): Only used for the genetic algorithm grid search. Size of the initial population to sample randomly generated individuals. If set to "auto", then ``population_size`` is calculated as ``15 * n_parameters``\. If set to an integer, then uses the integer value as ``population_size``\. If you need to speed up the genetic algorithm grid search, try decreasing this parameter. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to "auto".
 
         tournament_size (int, optional): For genetic algorithm grid search only. Number of individuals to perform tournament selection. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to 3.
 
         elitism (bool, optional): For genetic algorithm grid search only. If set to True, takes the ``tournament_size`` best solution to the next generation. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to True.
 
@@ -1008,15 +1008,15 @@
 
         sample_weights (str, Dict[int, float], or None, optional): Weights for the 012-encoded classes during training. If None, then does not weight classes. If set to "auto", then class weights are automatically calculated for each column to balance classes (reference, heterozygous, and alternate alleles). If a dictionary is passed, it must contain 0, 1, and 2 as the keys and the class weights as the values. E.g., {0: 1.0, 1: 1.0, 2: 1.0}. The dictionary is then used as the overall class weights. If you wanted to prevent the model from learning to predict heterozygotes, for example, you could set the class weights to {0: 1.0, 1: 0.0, 2: 1.0}. Defaults to "auto" (balanced weighting).
 
         gridsearch_method (str, optional): Grid search method to use. Supported options include: {"gridsearch", "randomized_gridsearch", "genetic_algorithm"}. "gridsearch" uses GridSearchCV to test every possible parameter combination. "randomized_gridsearch" picks ``grid_iter`` random combinations of parameters to test. "genetic_algorithm" uses a genetic algorithm via the sklearn-genetic-opt GASearchCV module to do the grid search. If doing a grid search, "randomized_search" takes the least amount of time because it does not have to test all parameters. "genetic_algorithm" takes the longest. See the scikit-learn GridSearchCV and RandomizedSearchCV documentation for the "gridsearch" and "randomized_gridsearch" options, and the sklearn-genetic-opt GASearchCV documentation for the "genetic_algorithm" option. Defaults to "gridsearch".
 
         grid_iter (int, optional): Number of iterations to use for randomized and genetic algorithm grid searches. For randomized grid search, ``grid_iter`` parameter combinations will be randomly sampled. For the genetic algorithm, this determines how many generations the genetic algorithm will run. Defaults to 80.
 
-        scoring_metric (str, optional): Scoring metric to use for the grid search. Supported options include: {"auc_macro", "auc_micro", "precision_recall_macro", "precision_recall_micro", "accuracy"}. Note that all metrics are automatically calculated when doing a grid search, the results of which are logged to a CSV file. However, when refitting following the grid search, the value passed to ``scoring_metric`` is used to select the best parameters. If you wish to choose the best parameters from a different metric, that information will also be in the CSV file. "auc_macro" and "auc_micro" get the AUC (area under curve) score for the ROC (Receiver Operating Characteristic) curve. The ROC curves plot the false positive rate (X-axis) versus the true positive rate (Y-axis) for each 012-encoded class and for the macro and micro averages among classes. The false positive rate is defined as: ``False Positive Rate = False Positives / (False Positives + True Negatives)`` and the true positive rate is defined as ``True Positive Rate = True Positives / (True Positives + False Negatives)``\. Macro averaging places equal importance on each class, whereas the micro average is the global average across all classes. AUC scores allow the ROC curve, and thus the model's classification skill, to be summarized as a single number. "precision_recall_macro" and "precision_recall_micro" create Precision-Recall (PR) curves for each class plus the macro and micro averages among classes. Precision is defined as ``True Positives / (True Positives + False Positives)`` and recall is defined as ``Recall = True Positives / (True Positives + False Negatives)``\. Reviewing both precision and recall is useful in cases where there is an imbalance in the observations between the two classes. For example, if there are many examples of major alleles (class 0) and only a few examples of minor alleles (class 2). AUC and AP are similar metrics, but AP summarizes a precision-recall curve as the weighted mean of precisions achieved at each probability threshold, with the increase in recall from the previous threshold used as the weight. On the contrary, AUC uses linear interpolation with the trapezoidal rule to calculate the area under the curve. "accuracy" calculates ``number of correct predictions / total predictions``\, but can often be misleading when used without considering the model's classification skill for each class. Defaults to "auc_macro".
+        scoring_metric (str, optional): Scoring metric to use for grid searches. See the classification metrics in the scikit-learn documentation (https://scikit-learn.org/stable/modules/model_evaluation.html) for supported options. Defaults to "f1_weighted".
 
         population_size (int or str, optional): Only used for the genetic algorithm grid search. Size of the initial population to sample randomly generated individuals. If set to "auto", then ``population_size`` is calculated as ``15 * n_parameters``\. If set to an integer, then uses the integer value as ``population_size``\. If you need to speed up the genetic algorithm grid search, try decreasing this parameter. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to "auto".
 
         tournament_size (int, optional): For genetic algorithm grid search only. Number of individuals to perform tournament selection. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to 3.
 
         elitism (bool, optional): For genetic algorithm grid search only. If set to True, takes the ``tournament_size`` best solution to the next generation. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to True.
 
@@ -1209,15 +1209,15 @@
 
         sample_weights (str, Dict[int, float], or None, optional): Weights for the 012-encoded classes during training. If None, then does not weight classes. If set to "auto", then class weights are automatically calculated for each column to balance classes (reference, heterozygous, and alternate alleles). If a dictionary is passed, it must contain 0, 1, and 2 as the keys and the class weights as the values. E.g., {0: 1.0, 1: 1.0, 2: 1.0}. The dictionary is then used as the overall class weights. If you wanted to prevent the model from learning to predict heterozygotes, for example, you could set the class weights to {0: 1.0, 1: 0.0, 2: 1.0}. Defaults to "auto" (balanced weighting).
 
         gridsearch_method (str, optional): Grid search method to use. Supported options include: {"gridsearch", "randomized_gridsearch", "genetic_algorithm"}. "gridsearch" uses GridSearchCV to test every possible parameter combination. "randomized_gridsearch" picks ``grid_iter`` random combinations of parameters to test. "genetic_algorithm" uses a genetic algorithm via the sklearn-genetic-opt GASearchCV module to do the grid search. If doing a grid search, "randomized_search" takes the least amount of time because it does not have to test all parameters. "genetic_algorithm" takes the longest. See the scikit-learn GridSearchCV and RandomizedSearchCV documentation for the "gridsearch" and "randomized_gridsearch" options, and the sklearn-genetic-opt GASearchCV documentation for the "genetic_algorithm" option. Defaults to "gridsearch".
 
         grid_iter (int, optional): Number of iterations to use for randomized and genetic algorithm grid searches. For randomized grid search, ``grid_iter`` parameter combinations will be randomly sampled. For the genetic algorithm, this determines how many generations the genetic algorithm will run. Defaults to 80.
 
-        scoring_metric (str, optional): Scoring metric to use for the grid search. Supported options include: {"auc_macro", "auc_micro", "precision_recall_macro", "precision_recall_micro", "accuracy"}. Note that all metrics are automatically calculated when doing a grid search, the results of which are logged to a CSV file. However, when refitting following the grid search, the value passed to ``scoring_metric`` is used to select the best parameters. If you wish to choose the best parameters from a different metric, that information will also be in the CSV file. "auc_macro" and "auc_micro" get the AUC (area under curve) score for the ROC (Receiver Operating Characteristic) curve. The ROC curves plot the false positive rate (X-axis) versus the true positive rate (Y-axis) for each 012-encoded class and for the macro and micro averages among classes. The false positive rate is defined as: ``False Positive Rate = False Positives / (False Positives + True Negatives)`` and the true positive rate is defined as ``True Positive Rate = True Positives / (True Positives + False Negatives)``\. Macro averaging places equal importance on each class, whereas the micro average is the global average across all classes. AUC scores allow the ROC curve, and thus the model's classification skill, to be summarized as a single number. "precision_recall_macro" and "precision_recall_micro" create Precision-Recall (PR) curves for each class plus the macro and micro averages among classes. Precision is defined as ``True Positives / (True Positives + False Positives)`` and recall is defined as ``Recall = True Positives / (True Positives + False Negatives)``\. Reviewing both precision and recall is useful in cases where there is an imbalance in the observations between the two classes. For example, if there are many examples of major alleles (class 0) and only a few examples of minor alleles (class 2). AUC and AP are similar metrics, but AP summarizes a precision-recall curve as the weighted mean of precisions achieved at each probability threshold, with the increase in recall from the previous threshold used as the weight. On the contrary, AUC uses linear interpolation with the trapezoidal rule to calculate the area under the curve. "accuracy" calculates ``number of correct predictions / total predictions``\, but can often be misleading when used without considering the model's classification skill for each class. Defaults to "auc_macro".
+        scoring_metric (str, optional): Scoring metric to use for grid searches. See the classification metrics in the scikit-learn documentation (https://scikit-learn.org/stable/modules/model_evaluation.html) for supported options. Defaults to "f1_weighted".
 
         population_size (int or str, optional): Only used for the genetic algorithm grid search. Size of the initial population to sample randomly generated individuals. If set to "auto", then ``population_size`` is calculated as ``15 * n_parameters``\. If set to an integer, then uses the integer value as ``population_size``\. If you need to speed up the genetic algorithm grid search, try decreasing this parameter. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to "auto".
 
         tournament_size (int, optional): For genetic algorithm grid search only. Number of individuals to perform tournament selection. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to 3.
 
         elitism (bool, optional): For genetic algorithm grid search only. If set to True, takes the ``tournament_size`` best solution to the next generation. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to True.
```

### Comparing `pg-sui-0.2.3/pgsui/impute/impute.py` & `pg-sui-0.2.3.1/pgsui/impute/impute.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/impute/simple_imputers.py` & `pg-sui-0.2.3.1/pgsui/impute/simple_imputers.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/impute/supervised/iterative_imputer_fixedparams.py` & `pg-sui-0.2.3.1/pgsui/impute/supervised/iterative_imputer_fixedparams.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/impute/supervised/iterative_imputer_gridsearch.py` & `pg-sui-0.2.3.1/pgsui/impute/supervised/iterative_imputer_gridsearch.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/impute/unsupervised/callbacks.py` & `pg-sui-0.2.3.1/pgsui/impute/unsupervised/callbacks.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/impute/unsupervised/keras_classifiers.py` & `pg-sui-0.2.3.1/pgsui/impute/unsupervised/keras_classifiers.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/impute/unsupervised/models/autoencoder_model.py` & `pg-sui-0.2.3.1/pgsui/impute/unsupervised/models/autoencoder_model.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/impute/unsupervised/models/in_development/cnn_model.py` & `pg-sui-0.2.3.1/pgsui/impute/unsupervised/models/in_development/cnn_model.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/impute/unsupervised/models/nlpca_model.py` & `pg-sui-0.2.3.1/pgsui/impute/unsupervised/models/nlpca_model.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/impute/unsupervised/models/ubp_model.py` & `pg-sui-0.2.3.1/pgsui/impute/unsupervised/models/ubp_model.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/impute/unsupervised/models/vae_model.py` & `pg-sui-0.2.3.1/pgsui/impute/unsupervised/models/vae_model.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/impute/unsupervised/neural_network_imputers.py` & `pg-sui-0.2.3.1/pgsui/impute/unsupervised/neural_network_imputers.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/impute/unsupervised/neural_network_methods.py` & `pg-sui-0.2.3.1/pgsui/impute/unsupervised/neural_network_methods.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/pg_sui.py` & `pg-sui-0.2.3.1/pgsui/pg_sui.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/utils/misc.py` & `pg-sui-0.2.3.1/pgsui/utils/misc.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/utils/plotting.py` & `pg-sui-0.2.3.1/pgsui/utils/plotting.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/utils/scorers.py` & `pg-sui-0.2.3.1/pgsui/utils/scorers.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/pgsui/utils/sequence_tools.py` & `pg-sui-0.2.3.1/pgsui/utils/sequence_tools.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/setup.py` & `pg-sui-0.2.3.1/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 
 
 def read(fname):
     return open(os.path.join(os.path.dirname(__file__), fname)).read()
 
 
 NAME = "pg-sui"
-VERSION = "0.2.3"
+VERSION = "0.2.3.1"
 AUTHORS = "Bradley T. Martin and Tyler K. Chafin"
 AUTHOR_EMAIL = "evobio721@gmail.com"
 MAINTAINER = "Bradley T. Martin"
 DESCRIPTION = "Python machine and deep learning package to impute missing SNPs"
 LONG_DESCRIPTION = open("README.md").read()
 
 setup(
```

### Comparing `pg-sui-0.2.3/simulation/sim_benchmarks.py` & `pg-sui-0.2.3.1/simulation/sim_benchmarks.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/simulation/sim_treeparams.py` & `pg-sui-0.2.3.1/simulation/sim_treeparams.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/test/pg_sui_simtest.py` & `pg-sui-0.2.3.1/test/pg_sui_simtest.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/test/pg_sui_testing.py` & `pg-sui-0.2.3.1/test/pg_sui_testing.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/test/test.py` & `pg-sui-0.2.3.1/test/test.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/test/test_pgsui.py` & `pg-sui-0.2.3.1/test/test_pgsui.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3/test/test_tkc.py` & `pg-sui-0.2.3.1/test/test_tkc.py`

 * *Files identical despite different names*

