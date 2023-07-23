# Comparing `tmp/pg-sui-0.2.3.1.tar.gz` & `tmp/pg-sui-0.2.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pg-sui-0.2.3.1.tar", last modified: Sun Jul 23 05:53:06 2023, max compression
+gzip compressed data, was "pg-sui-0.2.4.tar", last modified: Sun Jul 23 21:41:00 2023, max compression
```

## Comparing `pg-sui-0.2.3.1.tar` & `pg-sui-0.2.4.tar`

### file list

```diff
@@ -1,99 +1,99 @@
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:06.001230 pg-sui-0.2.3.1/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    35149 2023-07-16 18:34:37.000000 pg-sui-0.2.3.1/LICENSE
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)      220 2023-07-22 21:23:30.000000 pg-sui-0.2.3.1/MANIFEST.in
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14104 2023-07-23 05:53:06.001230 pg-sui-0.2.3.1/PKG-INFO
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    10444 2023-07-23 01:57:24.000000 pg-sui-0.2.3.1/README.md
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:03.796829 pg-sui-0.2.3.1/pg_sui.egg-info/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14104 2023-07-23 05:53:02.000000 pg-sui-0.2.3.1/pg_sui.egg-info/PKG-INFO
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2994 2023-07-23 05:53:02.000000 pg-sui-0.2.3.1/pg_sui.egg-info/SOURCES.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        1 2023-07-23 05:53:02.000000 pg-sui-0.2.3.1/pg_sui.egg-info/dependency_links.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)      331 2023-07-23 05:53:02.000000 pg-sui-0.2.3.1/pg_sui.egg-info/requires.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)       22 2023-07-23 05:53:02.000000 pg-sui-0.2.3.1/pg_sui.egg-info/top_level.txt
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:03.834590 pg-sui-0.2.3.1/pgsui/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     1449 2023-07-23 04:24:42.000000 pg-sui-0.2.3.1/pgsui/__init__.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:03.881476 pg-sui-0.2.3.1/pgsui/data_processing/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:42.000000 pg-sui-0.2.3.1/pgsui/data_processing/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    42452 2023-07-23 04:24:42.000000 pg-sui-0.2.3.1/pgsui/data_processing/transformers.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:03.912726 pg-sui-0.2.3.1/pgsui/example_data/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:42.000000 pg-sui-0.2.3.1/pgsui/example_data/__init__.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:04.082015 pg-sui-0.2.3.1/pgsui/example_data/phylip_files/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/phylip_files/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)   238537 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/phylip_files/test.phy
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2897 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/phylip_files/test_n10.phy
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    13428 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/phylip_files/test_n100.phy
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     1960 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/phylip_files/test_n2.phy
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    60228 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/phylip_files/test_n500.phy
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:04.135401 pg-sui-0.2.3.1/pgsui/example_data/popmaps/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/popmaps/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     1954 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/popmaps/test.popmap
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:04.451555 pg-sui-0.2.3.1/pgsui/example_data/structure_files/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/structure_files/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     6375 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.nopops.1row.10sites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    50808 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.nopops.2row.100sites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     7978 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.nopops.2row.10sites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    17512 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.nopops.2row.30sites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)   967410 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.nopops.2row.allsites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     6609 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.pops.1row.10sites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     8446 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.pops.2row.10sites.str
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)   967878 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.pops.2row.allsites.str
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:04.917959 pg-sui-0.2.3.1/pgsui/example_data/trees/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/trees/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    25575 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/trees/test.iqtree
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)      134 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/trees/test.qmat
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    46013 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/trees/test.rate
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     4696 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/trees/test.tre
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)      678 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/trees/test_n10.rate
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2577 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/trees/test_n100.rate
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    11387 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/trees/test_n500.rate
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    16235 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/trees/test_siterates.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)       80 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/trees/test_siterates_n10.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)      804 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/trees/test_siterates_n100.txt
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     4008 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/trees/test_siterates_n500.txt
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:05.034303 pg-sui-0.2.3.1/pgsui/example_data/vcf_files/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)   380243 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/vcf_files/test.vcf
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    72705 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/vcf_files/test.vcf.gz
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2581 2023-07-23 04:24:43.000000 pg-sui-0.2.3.1/pgsui/example_data/vcf_files/test.vcf.gz.tbi
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:05.134302 pg-sui-0.2.3.1/pgsui/impute/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:44.000000 pg-sui-0.2.3.1/pgsui/impute/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)   116270 2023-07-23 05:46:21.000000 pg-sui-0.2.3.1/pgsui/impute/estimators.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    51210 2023-07-23 04:24:44.000000 pg-sui-0.2.3.1/pgsui/impute/impute.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    53283 2023-07-23 04:24:44.000000 pg-sui-0.2.3.1/pgsui/impute/simple_imputers.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:05.223016 pg-sui-0.2.3.1/pgsui/impute/supervised/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:44.000000 pg-sui-0.2.3.1/pgsui/impute/supervised/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    35075 2023-07-23 04:24:44.000000 pg-sui-0.2.3.1/pgsui/impute/supervised/iterative_imputer_fixedparams.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    45443 2023-07-23 04:24:44.000000 pg-sui-0.2.3.1/pgsui/impute/supervised/iterative_imputer_gridsearch.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:05.423044 pg-sui-0.2.3.1/pgsui/impute/unsupervised/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:44.000000 pg-sui-0.2.3.1/pgsui/impute/unsupervised/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     9682 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/impute/unsupervised/callbacks.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    29483 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/impute/unsupervised/keras_classifiers.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:05.599595 pg-sui-0.2.3.1/pgsui/impute/unsupervised/models/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/impute/unsupervised/models/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    20161 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/impute/unsupervised/models/autoencoder_model.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:05.669152 pg-sui-0.2.3.1/pgsui/impute/unsupervised/models/in_development/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/impute/unsupervised/models/in_development/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    15036 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/impute/unsupervised/models/in_development/cnn_model.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14501 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/impute/unsupervised/models/nlpca_model.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    37879 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/impute/unsupervised/models/ubp_model.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    22338 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/impute/unsupervised/models/vae_model.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    52292 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/impute/unsupervised/neural_network_imputers.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    50830 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/impute/unsupervised/neural_network_methods.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     7471 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/pg_sui.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:05.800673 pg-sui-0.2.3.1/pgsui/utils/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/utils/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    15705 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/utils/misc.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    33748 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/utils/plotting.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    26862 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/utils/scorers.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    10143 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/pgsui/utils/sequence_tools.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)       38 2023-07-23 05:53:06.001230 pg-sui-0.2.3.1/setup.cfg
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     3048 2023-07-23 05:52:05.000000 pg-sui-0.2.3.1/setup.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:05.869698 pg-sui-0.2.3.1/simulation/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:45.000000 pg-sui-0.2.3.1/simulation/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    11345 2023-07-23 04:24:46.000000 pg-sui-0.2.3.1/simulation/sim_benchmarks.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    13793 2023-07-23 04:24:46.000000 pg-sui-0.2.3.1/simulation/sim_treeparams.py
-drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 05:53:05.985599 pg-sui-0.2.3.1/test/
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:46.000000 pg-sui-0.2.3.1/test/__init__.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     6024 2023-07-23 04:24:46.000000 pg-sui-0.2.3.1/test/pg_sui_simtest.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    15871 2023-07-23 04:24:46.000000 pg-sui-0.2.3.1/test/pg_sui_testing.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     5034 2023-07-23 05:26:30.000000 pg-sui-0.2.3.1/test/test.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14310 2023-07-23 04:24:46.000000 pg-sui-0.2.3.1/test/test_pgsui.py
--rwxrwxrwx   0 btm002    (1000) btm002    (1000)     5867 2023-07-23 04:24:46.000000 pg-sui-0.2.3.1/test/test_tkc.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 21:40:59.602384 pg-sui-0.2.4/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    35149 2023-07-16 18:34:37.000000 pg-sui-0.2.4/LICENSE
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)      220 2023-07-23 06:06:57.000000 pg-sui-0.2.4/MANIFEST.in
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14102 2023-07-23 21:40:59.599382 pg-sui-0.2.4/PKG-INFO
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    10444 2023-07-23 06:06:57.000000 pg-sui-0.2.4/README.md
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 21:40:56.314872 pg-sui-0.2.4/pg_sui.egg-info/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14102 2023-07-23 21:40:51.000000 pg-sui-0.2.4/pg_sui.egg-info/PKG-INFO
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2994 2023-07-23 21:40:53.000000 pg-sui-0.2.4/pg_sui.egg-info/SOURCES.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        1 2023-07-23 21:40:51.000000 pg-sui-0.2.4/pg_sui.egg-info/dependency_links.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)      331 2023-07-23 21:40:51.000000 pg-sui-0.2.4/pg_sui.egg-info/requires.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)       22 2023-07-23 21:40:51.000000 pg-sui-0.2.4/pg_sui.egg-info/top_level.txt
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 21:40:56.378344 pg-sui-0.2.4/pgsui/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     1449 2023-07-23 06:06:59.000000 pg-sui-0.2.4/pgsui/__init__.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 21:40:56.506344 pg-sui-0.2.4/pgsui/data_processing/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:42.000000 pg-sui-0.2.4/pgsui/data_processing/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    43851 2023-07-23 21:38:52.000000 pg-sui-0.2.4/pgsui/data_processing/transformers.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 21:40:56.533342 pg-sui-0.2.4/pgsui/example_data/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:42.000000 pg-sui-0.2.4/pgsui/example_data/__init__.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 21:40:56.894338 pg-sui-0.2.4/pgsui/example_data/phylip_files/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:43.000000 pg-sui-0.2.4/pgsui/example_data/phylip_files/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)   238537 2023-07-23 04:24:43.000000 pg-sui-0.2.4/pgsui/example_data/phylip_files/test.phy
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2897 2023-07-23 04:24:43.000000 pg-sui-0.2.4/pgsui/example_data/phylip_files/test_n10.phy
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    13428 2023-07-23 04:24:43.000000 pg-sui-0.2.4/pgsui/example_data/phylip_files/test_n100.phy
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     1960 2023-07-23 04:24:43.000000 pg-sui-0.2.4/pgsui/example_data/phylip_files/test_n2.phy
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    60228 2023-07-23 04:24:43.000000 pg-sui-0.2.4/pgsui/example_data/phylip_files/test_n500.phy
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 21:40:56.970336 pg-sui-0.2.4/pgsui/example_data/popmaps/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:43.000000 pg-sui-0.2.4/pgsui/example_data/popmaps/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     1954 2023-07-23 04:24:43.000000 pg-sui-0.2.4/pgsui/example_data/popmaps/test.popmap
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 21:40:57.425940 pg-sui-0.2.4/pgsui/example_data/structure_files/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:43.000000 pg-sui-0.2.4/pgsui/example_data/structure_files/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     6375 2023-07-23 04:24:43.000000 pg-sui-0.2.4/pgsui/example_data/structure_files/test.nopops.1row.10sites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    50808 2023-07-23 04:24:43.000000 pg-sui-0.2.4/pgsui/example_data/structure_files/test.nopops.2row.100sites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     7978 2023-07-23 04:24:43.000000 pg-sui-0.2.4/pgsui/example_data/structure_files/test.nopops.2row.10sites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    17512 2023-07-23 04:24:43.000000 pg-sui-0.2.4/pgsui/example_data/structure_files/test.nopops.2row.30sites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)   967410 2023-07-23 04:24:43.000000 pg-sui-0.2.4/pgsui/example_data/structure_files/test.nopops.2row.allsites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     6609 2023-07-23 04:24:43.000000 pg-sui-0.2.4/pgsui/example_data/structure_files/test.pops.1row.10sites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     8446 2023-07-23 04:24:43.000000 pg-sui-0.2.4/pgsui/example_data/structure_files/test.pops.2row.10sites.str
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)   967878 2023-07-23 04:24:43.000000 pg-sui-0.2.4/pgsui/example_data/structure_files/test.pops.2row.allsites.str
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 21:40:57.995612 pg-sui-0.2.4/pgsui/example_data/trees/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:43.000000 pg-sui-0.2.4/pgsui/example_data/trees/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    25575 2023-07-23 04:24:43.000000 pg-sui-0.2.4/pgsui/example_data/trees/test.iqtree
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)      134 2023-07-23 04:24:43.000000 pg-sui-0.2.4/pgsui/example_data/trees/test.qmat
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    46013 2023-07-23 04:24:43.000000 pg-sui-0.2.4/pgsui/example_data/trees/test.rate
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     4696 2023-07-23 04:24:43.000000 pg-sui-0.2.4/pgsui/example_data/trees/test.tre
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)      678 2023-07-23 04:24:43.000000 pg-sui-0.2.4/pgsui/example_data/trees/test_n10.rate
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2577 2023-07-23 04:24:43.000000 pg-sui-0.2.4/pgsui/example_data/trees/test_n100.rate
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    11387 2023-07-23 04:24:43.000000 pg-sui-0.2.4/pgsui/example_data/trees/test_n500.rate
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    16235 2023-07-23 04:24:43.000000 pg-sui-0.2.4/pgsui/example_data/trees/test_siterates.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)       80 2023-07-23 04:24:43.000000 pg-sui-0.2.4/pgsui/example_data/trees/test_siterates_n10.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)      804 2023-07-23 04:24:43.000000 pg-sui-0.2.4/pgsui/example_data/trees/test_siterates_n100.txt
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     4008 2023-07-23 04:24:43.000000 pg-sui-0.2.4/pgsui/example_data/trees/test_siterates_n500.txt
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 21:40:58.160139 pg-sui-0.2.4/pgsui/example_data/vcf_files/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)   380243 2023-07-23 04:24:43.000000 pg-sui-0.2.4/pgsui/example_data/vcf_files/test.vcf
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    72705 2023-07-23 06:06:59.000000 pg-sui-0.2.4/pgsui/example_data/vcf_files/test.vcf.gz
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     2581 2023-07-23 06:06:59.000000 pg-sui-0.2.4/pgsui/example_data/vcf_files/test.vcf.gz.tbi
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 21:40:58.305707 pg-sui-0.2.4/pgsui/impute/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:44.000000 pg-sui-0.2.4/pgsui/impute/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)   120473 2023-07-23 21:38:52.000000 pg-sui-0.2.4/pgsui/impute/estimators.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    51210 2023-07-23 06:06:59.000000 pg-sui-0.2.4/pgsui/impute/impute.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    53283 2023-07-23 06:06:59.000000 pg-sui-0.2.4/pgsui/impute/simple_imputers.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 21:40:58.403669 pg-sui-0.2.4/pgsui/impute/supervised/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:44.000000 pg-sui-0.2.4/pgsui/impute/supervised/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    35075 2023-07-23 06:06:59.000000 pg-sui-0.2.4/pgsui/impute/supervised/iterative_imputer_fixedparams.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    45443 2023-07-23 06:06:59.000000 pg-sui-0.2.4/pgsui/impute/supervised/iterative_imputer_gridsearch.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 21:40:58.644143 pg-sui-0.2.4/pgsui/impute/unsupervised/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:44.000000 pg-sui-0.2.4/pgsui/impute/unsupervised/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     9682 2023-07-23 06:06:59.000000 pg-sui-0.2.4/pgsui/impute/unsupervised/callbacks.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    29483 2023-07-23 06:06:59.000000 pg-sui-0.2.4/pgsui/impute/unsupervised/keras_classifiers.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 21:40:58.889858 pg-sui-0.2.4/pgsui/impute/unsupervised/models/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:45.000000 pg-sui-0.2.4/pgsui/impute/unsupervised/models/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    20161 2023-07-23 06:06:59.000000 pg-sui-0.2.4/pgsui/impute/unsupervised/models/autoencoder_model.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 21:40:58.988856 pg-sui-0.2.4/pgsui/impute/unsupervised/models/in_development/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:45.000000 pg-sui-0.2.4/pgsui/impute/unsupervised/models/in_development/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    15036 2023-07-23 04:24:45.000000 pg-sui-0.2.4/pgsui/impute/unsupervised/models/in_development/cnn_model.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14501 2023-07-23 06:06:59.000000 pg-sui-0.2.4/pgsui/impute/unsupervised/models/nlpca_model.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    37879 2023-07-23 06:06:59.000000 pg-sui-0.2.4/pgsui/impute/unsupervised/models/ubp_model.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    22338 2023-07-23 06:06:59.000000 pg-sui-0.2.4/pgsui/impute/unsupervised/models/vae_model.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    52329 2023-07-23 21:38:52.000000 pg-sui-0.2.4/pgsui/impute/unsupervised/neural_network_imputers.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    50830 2023-07-23 06:06:59.000000 pg-sui-0.2.4/pgsui/impute/unsupervised/neural_network_methods.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     7471 2023-07-23 06:06:59.000000 pg-sui-0.2.4/pgsui/pg_sui.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 21:40:59.231767 pg-sui-0.2.4/pgsui/utils/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:45.000000 pg-sui-0.2.4/pgsui/utils/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    15705 2023-07-23 04:24:45.000000 pg-sui-0.2.4/pgsui/utils/misc.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    33748 2023-07-23 06:06:59.000000 pg-sui-0.2.4/pgsui/utils/plotting.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    27088 2023-07-23 21:38:52.000000 pg-sui-0.2.4/pgsui/utils/scorers.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    10143 2023-07-23 04:24:45.000000 pg-sui-0.2.4/pgsui/utils/sequence_tools.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)       38 2023-07-23 21:40:59.617388 pg-sui-0.2.4/setup.cfg
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     3046 2023-07-23 21:38:52.000000 pg-sui-0.2.4/setup.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 21:40:59.358765 pg-sui-0.2.4/simulation/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:45.000000 pg-sui-0.2.4/simulation/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    11345 2023-07-23 04:24:46.000000 pg-sui-0.2.4/simulation/sim_benchmarks.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    13793 2023-07-23 04:24:46.000000 pg-sui-0.2.4/simulation/sim_treeparams.py
+drwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 21:40:59.568386 pg-sui-0.2.4/test/
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)        0 2023-07-23 04:24:46.000000 pg-sui-0.2.4/test/__init__.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     6024 2023-07-23 04:24:46.000000 pg-sui-0.2.4/test/pg_sui_simtest.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    15871 2023-07-23 04:24:46.000000 pg-sui-0.2.4/test/pg_sui_testing.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     6832 2023-07-23 21:38:52.000000 pg-sui-0.2.4/test/test.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)    14310 2023-07-23 04:24:46.000000 pg-sui-0.2.4/test/test_pgsui.py
+-rwxrwxrwx   0 btm002    (1000) btm002    (1000)     7041 2023-07-23 21:38:52.000000 pg-sui-0.2.4/test/test_tkc.py
```

### Comparing `pg-sui-0.2.3.1/LICENSE` & `pg-sui-0.2.4/LICENSE`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/PKG-INFO` & `pg-sui-0.2.4/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pg-sui
-Version: 0.2.3.1
+Version: 0.2.4
 Summary: Python machine and deep learning package to impute missing SNPs
 Home-page: https://github.com/btmartin721/PG-SUI
 Author: Bradley T. Martin and Tyler K. Chafin
 Author-email: evobio721@gmail.com
 Maintainer: Bradley T. Martin
 Maintainer-email: evobio721@gmail.com
 License: GNU General Public License v3 (GPLv3)
```

### Comparing `pg-sui-0.2.3.1/README.md` & `pg-sui-0.2.4/README.md`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pg_sui.egg-info/PKG-INFO` & `pg-sui-0.2.4/pg_sui.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pg-sui
-Version: 0.2.3.1
+Version: 0.2.4
 Summary: Python machine and deep learning package to impute missing SNPs
 Home-page: https://github.com/btmartin721/PG-SUI
 Author: Bradley T. Martin and Tyler K. Chafin
 Author-email: evobio721@gmail.com
 Maintainer: Bradley T. Martin
 Maintainer-email: evobio721@gmail.com
 License: GNU General Public License v3 (GPLv3)
```

### Comparing `pg-sui-0.2.3.1/pg_sui.egg-info/SOURCES.txt` & `pg-sui-0.2.4/pg_sui.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/__init__.py` & `pg-sui-0.2.4/pgsui/__init__.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/data_processing/transformers.py` & `pg-sui-0.2.4/pgsui/data_processing/transformers.py`

 * *Files 2% similar despite different names*

```diff
@@ -968,15 +968,15 @@
 
     def random_weighted_missing_data(self, X, inv=False):
         """Choose values for which to simulate missing data by biasing towards the minority or majority alleles, depending on whether inv is True or False.
 
         Args:
             X (np.ndarray): True values.
 
-            inv (bool, optional): If True, then biases towards choosing majority alleles. If False, then biases towards choosing minority alleles. Defaults to False.
+            inv (bool, optional): If True, then biases towards choosing majority alleles. If False, then generates a stratified random sample (class proportions ~= full dataset) Defaults to False.
 
         Returns:
             np.ndarray: X with simulated missing values.
 
         """
         # Get unique classes and their counts
         classes, counts = np.unique(X, return_counts=True)
@@ -1108,14 +1108,48 @@
             raise ValueError(f"Invalid shape of input X: {X.shape}")
 
         Xt = X.copy()
         mask_boolean = self.mask_ != 0
         Xt[mask_boolean] = mask_val
         return Xt
 
+    def write_mask(self, filename_prefix):
+        """Write mask to file.
+
+        Args:
+            filename_prefix (str): Prefix for the filenames to write to.
+        """
+        np.save(filename_prefix + "_mask.npy", self.mask_)
+        np.save(filename_prefix + "_original_missing_mask.npy", self.original_missing_mask_)
+
+    def read_mask(self, filename_prefix):
+        """Read mask from file.
+
+        Args:
+            filename_prefix (str): Prefix for the filenames to read from.
+
+        Returns:
+            tuple of np.ndarray: The read masks.
+        """
+        # Check if files exist
+        if not os.path.isfile(filename_prefix + "_mask.npy"):
+            raise FileNotFoundError(filename_prefix + "_mask.npy" + " does not exist.")
+        if not os.path.isfile(filename_prefix + "_original_missing_mask.npy"):
+            raise FileNotFoundError(filename_prefix + "_original_missing_mask.npy" + " does not exist.")
+
+        # Load mask from file
+        self.mask_ = np.load(filename_prefix + "_mask.npy")
+        self.original_missing_mask_ = np.load(filename_prefix + "_original_missing_mask.npy")
+
+        # Recalculate all_missing_mask_ from mask_ and original_missing_mask_
+        self.all_missing_mask_ = np.logical_or(self.mask_, self.original_missing_mask_)
+
+        return self.mask_, self.original_missing_mask_, self.all_missing_mask_
+
+
     @property
     def missing_count(self) -> int:
         """Count of masked genotypes in SimGenotypeData.mask
 
         Returns:
             int: Integer count of masked alleles.
         """
```

### Comparing `pg-sui-0.2.3.1/pgsui/example_data/phylip_files/test.phy` & `pg-sui-0.2.4/pgsui/example_data/phylip_files/test.phy`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/example_data/phylip_files/test_n10.phy` & `pg-sui-0.2.4/pgsui/example_data/phylip_files/test_n10.phy`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/example_data/phylip_files/test_n100.phy` & `pg-sui-0.2.4/pgsui/example_data/phylip_files/test_n100.phy`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/example_data/phylip_files/test_n2.phy` & `pg-sui-0.2.4/pgsui/example_data/phylip_files/test_n2.phy`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/example_data/phylip_files/test_n500.phy` & `pg-sui-0.2.4/pgsui/example_data/phylip_files/test_n500.phy`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/example_data/popmaps/test.popmap` & `pg-sui-0.2.4/pgsui/example_data/popmaps/test.popmap`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.nopops.1row.10sites.str` & `pg-sui-0.2.4/pgsui/example_data/structure_files/test.nopops.1row.10sites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.nopops.2row.100sites.str` & `pg-sui-0.2.4/pgsui/example_data/structure_files/test.nopops.2row.100sites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.nopops.2row.10sites.str` & `pg-sui-0.2.4/pgsui/example_data/structure_files/test.nopops.2row.10sites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.nopops.2row.30sites.str` & `pg-sui-0.2.4/pgsui/example_data/structure_files/test.nopops.2row.30sites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.nopops.2row.allsites.str` & `pg-sui-0.2.4/pgsui/example_data/structure_files/test.nopops.2row.allsites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.pops.1row.10sites.str` & `pg-sui-0.2.4/pgsui/example_data/structure_files/test.pops.1row.10sites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.pops.2row.10sites.str` & `pg-sui-0.2.4/pgsui/example_data/structure_files/test.pops.2row.10sites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/example_data/structure_files/test.pops.2row.allsites.str` & `pg-sui-0.2.4/pgsui/example_data/structure_files/test.pops.2row.allsites.str`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/example_data/trees/test.iqtree` & `pg-sui-0.2.4/pgsui/example_data/trees/test.iqtree`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/example_data/trees/test.rate` & `pg-sui-0.2.4/pgsui/example_data/trees/test.rate`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/example_data/trees/test.tre` & `pg-sui-0.2.4/pgsui/example_data/trees/test.tre`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/example_data/trees/test_n10.rate` & `pg-sui-0.2.4/pgsui/example_data/trees/test_n10.rate`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/example_data/trees/test_n100.rate` & `pg-sui-0.2.4/pgsui/example_data/trees/test_n100.rate`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/example_data/trees/test_n500.rate` & `pg-sui-0.2.4/pgsui/example_data/trees/test_n500.rate`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/example_data/trees/test_siterates.txt` & `pg-sui-0.2.4/pgsui/example_data/trees/test_siterates.txt`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/example_data/trees/test_siterates_n100.txt` & `pg-sui-0.2.4/pgsui/example_data/trees/test_siterates_n100.txt`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/example_data/trees/test_siterates_n500.txt` & `pg-sui-0.2.4/pgsui/example_data/trees/test_siterates_n500.txt`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/example_data/vcf_files/test.vcf` & `pg-sui-0.2.4/pgsui/example_data/vcf_files/test.vcf`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/example_data/vcf_files/test.vcf.gz` & `pg-sui-0.2.4/pgsui/example_data/vcf_files/test.vcf.gz`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/example_data/vcf_files/test.vcf.gz.tbi` & `pg-sui-0.2.4/pgsui/example_data/vcf_files/test.vcf.gz.tbi`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/impute/estimators.py` & `pg-sui-0.2.4/pgsui/impute/estimators.py`

 * *Files 3% similar despite different names*

```diff
@@ -71,17 +71,17 @@
 
         population_size (int or str, optional): For genetic algorithm grid search: Size of the initial population to sample randomly generated individuals. If set to "auto", then ``population_size`` is calculated as ``15 * n_parameters``\. If set to an integer, then uses the integer value as ``population_size``\. If you need to speed up the genetic algorithm grid search, try decreasing this parameter. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io). Defaults to "auto".
 
         tournament_size (int, optional): For genetic algorithm grid search: Number of individuals to perform tournament selection. See GASearchCV documentation. Defaults to 3.
 
         elitism (bool, optional): For genetic algorithm grid search:     If True takes the tournament_size best solution to the next generation. See GASearchCV documentation. Defaults to True.
 
-        crossover_probability (float, optional): For genetic algorithm grid search: Probability of crossover operation between two individuals. See GASearchCV documentation. Defaults to 0.8.
+        crossover_probability (float, optional): For genetic algorithm grid search: Probability of crossover operation between two individuals. See GASearchCV documentation. Defaults to 0.2.
 
-        mutation_probability (float, optional): For genetic algorithm grid search: Probability of child mutation. See GASearchCV documentation. Defaults to 0.2.
+        mutation_probability (float, optional): For genetic algorithm grid search: Probability of child mutation. See GASearchCV documentation. Defaults to 0.8.
 
         ga_algorithm (str, optional): For genetic algorithm grid search: Evolutionary algorithm to use. Supported options include: {"eaMuPlusLambda", "eaMuCommaLambda", "eaSimple"}. If you need to speed up the genetic algorithm grid search, try setting ``algorithm`` to "euSimple", at the expense of evolutionary model robustness. See more details in the DEAP algorithms documentation (https://deap.readthedocs.io). Defaults to "eaMuPlusLambda".
 
         early_stop_gen (int, optional): If the genetic algorithm sees ``early_stop_gen`` consecutive generations without improvement in the scoring metric, an early stopping callback is implemented. This saves time by reducing the number of generations the genetic algorithm has to perform. Defaults to 5.
 
         scoring_metric (str, optional): Scoring metric to use for grid searches. See the classification metrics in the scikit-learn documentation (https://scikit-learn.org/stable/modules/model_evaluation.html) for supported options. Defaults to "f1_weighted".
 
@@ -157,16 +157,16 @@
         skip_complete: bool = False,
         random_state: Optional[int] = None,
         gridsearch_method: str = "gridsearch",
         grid_iter: int = 80,
         population_size: Union[int, str] = "auto",
         tournament_size: int = 3,
         elitism: bool = True,
-        crossover_probability: float = 0.8,
-        mutation_probability: float = 0.2,
+        crossover_probability: float = 0.2,
+        mutation_probability: float = 0.8,
         ga_algorithm: str = "eaMuPlusLambda",
         early_stop_gen: int = 5,
         scoring_metric: str = "f1_weighted",
         chunk_size: Union[int, float] = 1.0,
         disable_progressbar: bool = False,
         progress_update_percent: Optional[int] = None,
         n_jobs: int = 1,
@@ -253,17 +253,17 @@
 
         population_size (int or str, optional): For genetic algorithm grid search: Size of the initial population to sample randomly generated individuals. If set to "auto", then ``population_size`` is calculated as ``15 * n_parameters``\. If set to an integer, then uses the integer value as ``population_size``\. If you need to speed up the genetic algorithm grid search, try decreasing this parameter. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io). Defaults to "auto".
 
         tournament_size (int, optional): For genetic algorithm grid search: Number of individuals to perform tournament selection. See GASearchCV documentation. Defaults to 3.
 
         elitism (bool, optional): For genetic algorithm grid search:     If True takes the tournament_size best solution to the next generation. See GASearchCV documentation. Defaults to True.
 
-        crossover_probability (float, optional): For genetic algorithm grid search: Probability of crossover operation between two individuals. See GASearchCV documentation. Defaults to 0.8.
+        crossover_probability (float, optional): For genetic algorithm grid search: Probability of crossover operation between two individuals. See GASearchCV documentation. Defaults to 0.2.
 
-        mutation_probability (float, optional): For genetic algorithm grid search: Probability of child mutation. See GASearchCV documentation. Defaults to 0.2.
+        mutation_probability (float, optional): For genetic algorithm grid search: Probability of child mutation. See GASearchCV documentation. Defaults to 0.8.
 
         ga_algorithm (str, optional): For genetic algorithm grid search: Evolutionary algorithm to use. Supported options include: {"eaMuPlusLambda", "eaMuCommaLambda", "eaSimple"}. If you need to speed up the genetic algorithm grid search, try setting ``algorithm`` to "euSimple", at the expense of evolutionary model robustness. See more details in the DEAP algorithms documentation (https://deap.readthedocs.io). Defaults to "eaMuPlusLambda".
 
         early_stop_gen (int, optional): If the genetic algorithm sees ``early_stop_gen`` consecutive generations without improvement in the scoring metric, an early stopping callback is implemented. This saves time by reducing the number of generations the genetic algorithm has to perform. Defaults to 5.
 
         scoring_metric (str, optional): Scoring metric to use for grid searches. See the classification metrics in the scikit-learn documentation (https://scikit-learn.org/stable/modules/model_evaluation.html) for supported options. Defaults to "f1_weighted".
 
@@ -349,16 +349,16 @@
         skip_complete: bool = False,
         random_state: Optional[int] = None,
         gridsearch_method: str = "gridsearch",
         grid_iter: int = 80,
         population_size: Union[int, str] = "auto",
         tournament_size: int = 3,
         elitism: bool = True,
-        crossover_probability: float = 0.8,
-        mutation_probability: float = 0.2,
+        crossover_probability: float = 0.2,
+        mutation_probability: float = 0.8,
         ga_algorithm: str = "eaMuPlusLambda",
         early_stop_gen: int = 5,
         scoring_metric: str = "f1_weighted",
         chunk_size: Union[int, float] = 1.0,
         disable_progressbar: bool = False,
         progress_update_percent: Optional[int] = None,
         n_jobs: int = 1,
@@ -396,15 +396,15 @@
 
     @property
     def genotype_data_imputed(self):
         return self.imputed
 
     @property
     def genotypes_012(self):
-        return self.imputed.genotypes_012
+        return self.imputed.genotypes_
 
     @property
     def snp_data(self):
         return self.imputed.snp_data
 
     @property
     def genotypes_onehot(self):
@@ -485,17 +485,17 @@
 
         population_size (int or str, optional): For genetic algorithm grid search: Size of the initial population to sample randomly generated individuals. If set to "auto", then ``population_size`` is calculated as ``15 * n_parameters``\. If set to an integer, then uses the integer value as ``population_size``\. If you need to speed up the genetic algorithm grid search, try decreasing this parameter. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io). Defaults to "auto".
 
         tournament_size (int, optional): For genetic algorithm grid search: Number of individuals to perform tournament selection. See GASearchCV documentation. Defaults to 3.
 
         elitism (bool, optional): For genetic algorithm grid search: If True takes the tournament_size best solution to the next generation. See GASearchCV documentation. Defaults to True.
 
-        crossover_probability (float, optional): For genetic algorithm grid search: Probability of crossover operation between two individuals. See GASearchCV documentation. Defaults to 0.8.
+        crossover_probability (float, optional): For genetic algorithm grid search: Probability of crossover operation between two individuals. See GASearchCV documentation. Defaults to 0.2.
 
-        mutation_probability (float, optional): For genetic algorithm grid search: Probability of child mutation. See GASearchCV documentation. Defaults to 0.2.
+        mutation_probability (float, optional): For genetic algorithm grid search: Probability of child mutation. See GASearchCV documentation. Defaults to 0.8.
 
         ga_algorithm (str, optional): For genetic algorithm grid search: Evolutionary algorithm to use. Supported options include: {"eaMuPlusLambda", "eaMuCommaLambda", "eaSimple"}. If you need to speed up the genetic algorithm grid search, try setting ``algorithm`` to "euSimple", at the expense of evolutionary model robustness. See more details in the DEAP algorithms documentation (https://deap.readthedocs.io). Defaults to "eaMuPlusLambda".
 
         early_stop_gen (int, optional): If the genetic algorithm sees ``early_stop_gen`` consecutive generations without improvement in the scoring metric, an early stopping callback is implemented. This saves time by reducing the number of generations the genetic algorithm has to perform. Defaults to 5.
 
         scoring_metric (str, optional): Scoring metric to use for grid searches. See the classification metrics in the scikit-learn documentation (https://scikit-learn.org/stable/modules/model_evaluation.html) for supported options. Defaults to "f1_weighted".
 
@@ -577,16 +577,16 @@
         skip_complete: bool = False,
         random_state: Optional[int] = None,
         gridsearch_method: str = "gridsearch",
         grid_iter: int = 80,
         population_size: Union[int, str] = "auto",
         tournament_size: int = 3,
         elitism: bool = True,
-        crossover_probability: float = 0.8,
-        mutation_probability: float = 0.2,
+        crossover_probability: float = 0.2,
+        mutation_probability: float = 0.8,
         ga_algorithm: str = "eaMuPlusLambda",
         early_stop_gen: int = 5,
         scoring_metric: str = "f1_weighted",
         chunk_size: Union[int, float] = 1.0,
         disable_progressbar: bool = False,
         progress_update_percent: Optional[int] = None,
         n_jobs: int = 1,
@@ -652,25 +652,25 @@
 
         sample_weights (str, Dict[int, float], or None, optional): Weights for the 012-encoded classes during training. If None, then does not weight classes. If set to "auto", then class weights are automatically calculated for each column to balance classes (reference, heterozygous, and alternate alleles). If a dictionary is passed, it must contain 0, 1, and 2 as the keys and the class weights as the values. E.g., {0: 1.0, 1: 1.0, 2: 1.0}. The dictionary is then used as the overall class weights. If you wanted to prevent the model from learning to predict heterozygotes, for example, you could set the class weights to {0: 1.0, 1: 0.0, 2: 1.0}. Defaults to "auto" (balanced weighting).
 
         gridsearch_method (str, optional): Grid search method to use. Supported options include: {"gridsearch", "randomized_gridsearch", "genetic_algorithm"}. "gridsearch" uses GridSearchCV to test every possible parameter combination. "randomized_gridsearch" picks ``grid_iter`` random combinations of parameters to test. "genetic_algorithm" uses a genetic algorithm via the sklearn-genetic-opt GASearchCV module to do the grid search. If doing a grid search, "randomized_search" takes the least amount of time because it does not have to test all parameters. "genetic_algorithm" takes the longest. See the scikit-learn GridSearchCV and RandomizedSearchCV documentation for the "gridsearch" and "randomized_gridsearch" options, and the sklearn-genetic-opt GASearchCV documentation for the "genetic_algorithm" option. Defaults to "gridsearch".
 
         grid_iter (int, optional): Number of iterations to use for randomized and genetic algorithm grid searches. For randomized grid search, ``grid_iter`` parameter combinations will be randomly sampled. For the genetic algorithm, this determines how many generations the genetic algorithm will run. Defaults to 80.
 
-        scoring_metric (str, optional): Scoring metric to use for grid searches. See the classification metrics in the scikit-learn documentation (https://scikit-learn.org/stable/modules/model_evaluation.html) for supported options. Defaults to "f1_weighted".
+        scoring_metric (str, optional): Scoring metric to use for grid searches. The neural network imputers use a multimetric scorer and use different string values for the grid searches. Supported options include: {"accuracy", "hamming", "auc_macro", "auc_micro", "precision_recall_macro", "precision_recall_micro", "precision_recall_samples", "f1_score", and "f1_score_weighted"}. All of the above metrics are calculated during the grid search, but the provided string just sets the metric that the grid search refits to (i.e., which one is used in the best estimator). "accuracy" is just the ``number of correct calls / total calls``\. "hamming" calculates the Hamming distance. "auc_macro" does roc_auc_score with macro averaging. "auc_micro" does roc_auc_score with micro averaging. "precision_recall_macro" calculates precision and recall scores with macro averaging. "precision_recall_micro" similarly uses micro averaging. "precision_recall_samples" calculates the precision/ recall scores per samples instead of per label. "f1_score" calculates F1 scores with macro averaging, which is the harmonic mean of precision and recall and does not account for class imbalance. "f1_score_weighted" is simular to "f1_score" but accounts for class imbalance with weighting. Defaults to "f1_score_weighted".
 
         population_size (int or str, optional): Only used for the genetic algorithm grid search. Size of the initial population to sample randomly generated individuals. If set to "auto", then ``population_size`` is calculated as ``15 * n_parameters``\. If set to an integer, then uses the integer value as ``population_size``\. If you need to speed up the genetic algorithm grid search, try decreasing this parameter. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to "auto".
 
         tournament_size (int, optional): For genetic algorithm grid search only. Number of individuals to perform tournament selection. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to 3.
 
         elitism (bool, optional): For genetic algorithm grid search only. If set to True, takes the ``tournament_size`` best solution to the next generation. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to True.
 
-        crossover_probability (float, optional): For genetic algorithm grid search only. Probability of crossover operation between two individuals. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to 0.8.
+        crossover_probability (float, optional): For genetic algorithm grid search only. Probability of crossover operation between two individuals. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to 0.2.
 
-        mutation_probability (float, optional): For genetic algorithm grid search only. Probability of child mutation. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to 0.2.
+        mutation_probability (float, optional): For genetic algorithm grid search only. Probability of child mutation. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to 0.8.
 
         ga_algorithm (str, optional): For genetic algorithm grid search only. Evolutionary algorithm to use. Supported options include: {"eaMuPlusLambda", "eaMuCommaLambda", "eaSimple"}. If you need to speed up the genetic algorithm grid search, try setting ``algorithm`` to "euSimple", at the expense of evolutionary model robustness. See more details in the DEAP algorithms documentation (https://deap.readthedocs.io). Defaults to "eaMuPlusLambda".
 
         sim_strategy (str, optional): Strategy to use for simulating missing data. Only used to validate the accuracy of the imputation. The final model will be trained with the non-simulated dataset. Supported options include: {"random", "random_weighted", "nonrandom", "nonrandom_weighted"}. "random" randomly simulates missing data, while "random_weighted" also does this but balances selection of reference, heterozygous, and alternate alleles. When set to "nonrandom", branches from ``GenotypeData.guidetree`` will be randomly sampled to generate missing data on descendant nodes. For "nonrandom_weighted", missing data will be placed on nodes proportionally to their branch lengths (e.g., to generate data distributed as might be the case with mutation-disruption of RAD sites). If using the "nonrandom" or "nonrandom_weighted" options, a guide tree is required to have been initialized in the passed ``genotype_data`` object. Defaults to "random".
 
         sim_prop_missing (float, optional): Proportion of missing data to use with missing data simulation. Defaults to 0.2.
 
@@ -725,20 +725,20 @@
         l1_penalty=1e-6,
         l2_penalty=1e-6,
         dropout_rate=0.2,
         kl_beta=1.0,
         sample_weights="auto",
         gridsearch_method="gridsearch",
         grid_iter=80,
-        scoring_metric="f1_weighted",
+        scoring_metric="f1_score_weighted",
         population_size="auto",
         tournament_size=3,
         elitism=True,
-        crossover_probability=0.8,
-        mutation_probability=0.2,
+        crossover_probability=0.2,
+        mutation_probability=0.8,
         ga_algorithm="eaMuPlusLambda",
         sim_strategy="random_weighted",
         sim_prop_missing=0.2,
         disable_progressbar=False,
         n_jobs=1,
         verbose=0,
         **kwargs,
@@ -815,25 +815,25 @@
 
         sample_weights (str, Dict[int, float], or None, optional): Weights for the 012-encoded classes during training. If None, then does not weight classes. If set to "auto", then class weights are automatically calculated for each column to balance classes (reference, heterozygous, and alternate alleles). If a dictionary is passed, it must contain 0, 1, and 2 as the keys and the class weights as the values. E.g., {0: 1.0, 1: 1.0, 2: 1.0}. The dictionary is then used as the overall class weights. If you wanted to prevent the model from learning to predict heterozygotes, for example, you could set the class weights to {0: 1.0, 1: 0.0, 2: 1.0}. Defaults to "auto" (balanced weighting).
 
         gridsearch_method (str, optional): Grid search method to use. Supported options include: {"gridsearch", "randomized_gridsearch", "genetic_algorithm"}. "gridsearch" uses GridSearchCV to test every possible parameter combination. "randomized_gridsearch" picks ``grid_iter`` random combinations of parameters to test. "genetic_algorithm" uses a genetic algorithm via the sklearn-genetic-opt GASearchCV module to do the grid search. If doing a grid search, "randomized_search" takes the least amount of time because it does not have to test all parameters. "genetic_algorithm" takes the longest. See the scikit-learn GridSearchCV and RandomizedSearchCV documentation for the "gridsearch" and "randomized_gridsearch" options, and the sklearn-genetic-opt GASearchCV documentation for the "genetic_algorithm" option. Defaults to "gridsearch".
 
         grid_iter (int, optional): Number of iterations to use for randomized and genetic algorithm grid searches. For randomized grid search, ``grid_iter`` parameter combinations will be randomly sampled. For the genetic algorithm, this determines how many generations the genetic algorithm will run. Defaults to 80.
 
-        scoring_metric (str, optional): Scoring metric to use for grid searches. See the classification metrics in the scikit-learn documentation (https://scikit-learn.org/stable/modules/model_evaluation.html) for supported options. Defaults to "f1_weighted".
+        scoring_metric (str, optional): Scoring metric to use for grid searches. The neural network imputers use a multimetric scorer and use different string values for the grid searches. Supported options include: {"accuracy", "hamming", "auc_macro", "auc_micro", "precision_recall_macro", "precision_recall_micro", "precision_recall_samples", "f1_score", and "f1_score_weighted"}. All of the above metrics are calculated during the grid search, but the provided string just sets the metric that the grid search refits to (i.e., which one is used in the best estimator). "accuracy" is just the ``number of correct calls / total calls``\. "hamming" calculates the Hamming distance. "auc_macro" does roc_auc_score with macro averaging. "auc_micro" does roc_auc_score with micro averaging. "precision_recall_macro" calculates precision and recall scores with macro averaging. "precision_recall_micro" similarly uses micro averaging. "precision_recall_samples" calculates the precision/ recall scores per samples instead of per label. "f1_score" calculates F1 scores with macro averaging, which is the harmonic mean of precision and recall and does not account for class imbalance. "f1_score_weighted" is simular to "f1_score" but accounts for class imbalance with weighting. Defaults to "f1_score_weighted".
 
         population_size (int or str, optional): Only used for the genetic algorithm grid search. Size of the initial population to sample randomly generated individuals. If set to "auto", then ``population_size`` is calculated as ``15 * n_parameters``\. If set to an integer, then uses the integer value as ``population_size``\. If you need to speed up the genetic algorithm grid search, try decreasing this parameter. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to "auto".
 
         tournament_size (int, optional): For genetic algorithm grid search only. Number of individuals to perform tournament selection. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to 3.
 
         elitism (bool, optional): For genetic algorithm grid search only. If set to True, takes the ``tournament_size`` best solution to the next generation. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to True.
 
-        crossover_probability (float, optional): For genetic algorithm grid search only. Probability of crossover operation between two individuals. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to 0.8.
+        crossover_probability (float, optional): For genetic algorithm grid search only. Probability of crossover operation between two individuals. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to 0.2.
 
-        mutation_probability (float, optional): For genetic algorithm grid search only. Probability of child mutation. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to 0.2.
+        mutation_probability (float, optional): For genetic algorithm grid search only. Probability of child mutation. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to 0.8.
 
         ga_algorithm (str, optional): For genetic algorithm grid search only. Evolutionary algorithm to use. Supported options include: {"eaMuPlusLambda", "eaMuCommaLambda", "eaSimple"}. If you need to speed up the genetic algorithm grid search, try setting ``algorithm`` to "euSimple", at the expense of evolutionary model robustness. See more details in the DEAP algorithms documentation (https://deap.readthedocs.io). Defaults to "eaMuPlusLambda".
 
         sim_strategy (str, optional): Strategy to use for simulating missing data. Only used to validate the accuracy of the imputation. The final model will be trained with the non-simulated dataset. Supported options include: {"random", "random_weighted", "nonrandom", "nonrandom_weighted"}. "random" randomly simulates missing data, while "random_weighted" also does this but balances selection of reference, heterozygous, and alternate alleles. When set to "nonrandom", branches from ``GenotypeData.guidetree`` will be randomly sampled to generate missing data on descendant nodes. For "nonrandom_weighted", missing data will be placed on nodes proportionally to their branch lengths (e.g., to generate data distributed as might be the case with mutation-disruption of RAD sites). If using the "nonrandom" or "nonrandom_weighted" options, a guide tree is required to have been initialized in the passed ``genotype_data`` object. Defaults to "random".
 
         sim_prop_missing (float, optional): Proportion of missing data to use with missing data simulation. Defaults to 0.2.
 
@@ -888,20 +888,20 @@
         weights_initializer="glorot_normal",
         l1_penalty=1e-6,
         l2_penalty=1e-6,
         dropout_rate=0.2,
         sample_weights="auto",
         gridsearch_method="gridsearch",
         grid_iter=80,
-        scoring_metric="f1_weighted",
+        scoring_metric="f1_score_weighted",
         population_size="auto",
         tournament_size=3,
         elitism=True,
-        crossover_probability=0.8,
-        mutation_probability=0.2,
+        crossover_probability=0.2,
+        mutation_probability=0.8,
         ga_algorithm="eaMuPlusLambda",
         sim_strategy="random_weighted",
         sim_prop_missing=0.2,
         disable_progressbar=False,
         n_jobs=1,
         verbose=0,
         **kwargs,
@@ -1008,25 +1008,25 @@
 
         sample_weights (str, Dict[int, float], or None, optional): Weights for the 012-encoded classes during training. If None, then does not weight classes. If set to "auto", then class weights are automatically calculated for each column to balance classes (reference, heterozygous, and alternate alleles). If a dictionary is passed, it must contain 0, 1, and 2 as the keys and the class weights as the values. E.g., {0: 1.0, 1: 1.0, 2: 1.0}. The dictionary is then used as the overall class weights. If you wanted to prevent the model from learning to predict heterozygotes, for example, you could set the class weights to {0: 1.0, 1: 0.0, 2: 1.0}. Defaults to "auto" (balanced weighting).
 
         gridsearch_method (str, optional): Grid search method to use. Supported options include: {"gridsearch", "randomized_gridsearch", "genetic_algorithm"}. "gridsearch" uses GridSearchCV to test every possible parameter combination. "randomized_gridsearch" picks ``grid_iter`` random combinations of parameters to test. "genetic_algorithm" uses a genetic algorithm via the sklearn-genetic-opt GASearchCV module to do the grid search. If doing a grid search, "randomized_search" takes the least amount of time because it does not have to test all parameters. "genetic_algorithm" takes the longest. See the scikit-learn GridSearchCV and RandomizedSearchCV documentation for the "gridsearch" and "randomized_gridsearch" options, and the sklearn-genetic-opt GASearchCV documentation for the "genetic_algorithm" option. Defaults to "gridsearch".
 
         grid_iter (int, optional): Number of iterations to use for randomized and genetic algorithm grid searches. For randomized grid search, ``grid_iter`` parameter combinations will be randomly sampled. For the genetic algorithm, this determines how many generations the genetic algorithm will run. Defaults to 80.
 
-        scoring_metric (str, optional): Scoring metric to use for grid searches. See the classification metrics in the scikit-learn documentation (https://scikit-learn.org/stable/modules/model_evaluation.html) for supported options. Defaults to "f1_weighted".
+        scoring_metric (str, optional): Scoring metric to use for grid searches. The neural network imputers use a multimetric scorer and use different string values for the grid searches. Supported options include: {"accuracy", "hamming", "auc_macro", "auc_micro", "precision_recall_macro", "precision_recall_micro", "precision_recall_samples", "f1_score", and "f1_score_weighted"}. All of the above metrics are calculated during the grid search, but the provided string just sets the metric that the grid search refits to (i.e., which one is used in the best estimator). "accuracy" is just the ``number of correct calls / total calls``\. "hamming" calculates the Hamming distance. "auc_macro" does roc_auc_score with macro averaging. "auc_micro" does roc_auc_score with micro averaging. "precision_recall_macro" calculates precision and recall scores with macro averaging. "precision_recall_micro" similarly uses micro averaging. "precision_recall_samples" calculates the precision/ recall scores per samples instead of per label. "f1_score" calculates F1 scores with macro averaging, which is the harmonic mean of precision and recall and does not account for class imbalance. "f1_score_weighted" is simular to "f1_score" but accounts for class imbalance with weighting. Defaults to "f1_score_weighted".
 
         population_size (int or str, optional): Only used for the genetic algorithm grid search. Size of the initial population to sample randomly generated individuals. If set to "auto", then ``population_size`` is calculated as ``15 * n_parameters``\. If set to an integer, then uses the integer value as ``population_size``\. If you need to speed up the genetic algorithm grid search, try decreasing this parameter. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to "auto".
 
         tournament_size (int, optional): For genetic algorithm grid search only. Number of individuals to perform tournament selection. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to 3.
 
         elitism (bool, optional): For genetic algorithm grid search only. If set to True, takes the ``tournament_size`` best solution to the next generation. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to True.
 
-        crossover_probability (float, optional): For genetic algorithm grid search only. Probability of crossover operation between two individuals. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to 0.8.
+        crossover_probability (float, optional): For genetic algorithm grid search only. Probability of crossover operation between two individuals. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to 0.2.
 
-        mutation_probability (float, optional): For genetic algorithm grid search only. Probability of child mutation. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to 0.2.
+        mutation_probability (float, optional): For genetic algorithm grid search only. Probability of child mutation. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to 0.8.
 
         ga_algorithm (str, optional): For genetic algorithm grid search only. Evolutionary algorithm to use. Supported options include: {"eaMuPlusLambda", "eaMuCommaLambda", "eaSimple"}. If you need to speed up the genetic algorithm grid search, try setting ``algorithm`` to "euSimple", at the expense of evolutionary model robustness. See more details in the DEAP algorithms documentation (https://deap.readthedocs.io). Defaults to "eaMuPlusLambda".
 
         sim_strategy (str, optional): Strategy to use for simulating missing data. Only used to validate the accuracy of the imputation. The final model will be trained with the non-simulated dataset. Supported options include: {"random", "random_weighted", "nonrandom", "nonrandom_weighted"}. "random" randomly simulates missing data, while "random_weighted" also does this but balances selection of reference, heterozygous, and alternate alleles. When set to "nonrandom", branches from ``GenotypeData.guidetree`` will be randomly sampled to generate missing data on descendant nodes. For "nonrandom_weighted", missing data will be placed on nodes proportionally to their branch lengths (e.g., to generate data distributed as might be the case with mutation-disruption of RAD sites). If using the "nonrandom" or "nonrandom_weighted" options, a guide tree is required to have been initialized in the passed ``genotype_data`` object. Defaults to "random".
 
         sim_prop_missing (float, optional): Proportion of missing data to use with missing data simulation. Defaults to 0.2.
 
@@ -1086,20 +1086,20 @@
         weights_initializer="glorot_normal",
         l1_penalty=1e-6,
         l2_penalty=1e-6,
         dropout_rate=0.2,
         sample_weights="auto",
         gridsearch_method="gridsearch",
         grid_iter=80,
-        scoring_metric="f1_weighted",
+        scoring_metric="f1_score_weighted",
         population_size="auto",
         tournament_size=3,
         elitism=True,
-        crossover_probability=0.8,
-        mutation_probability=0.2,
+        crossover_probability=0.2,
+        mutation_probability=0.8,
         ga_algorithm="eaMuPlusLambda",
         sim_strategy="random_weighted",
         sim_prop_missing=0.2,
         disable_progressbar=False,
         n_jobs=1,
         verbose=0,
         **kwargs,
@@ -1209,25 +1209,25 @@
 
         sample_weights (str, Dict[int, float], or None, optional): Weights for the 012-encoded classes during training. If None, then does not weight classes. If set to "auto", then class weights are automatically calculated for each column to balance classes (reference, heterozygous, and alternate alleles). If a dictionary is passed, it must contain 0, 1, and 2 as the keys and the class weights as the values. E.g., {0: 1.0, 1: 1.0, 2: 1.0}. The dictionary is then used as the overall class weights. If you wanted to prevent the model from learning to predict heterozygotes, for example, you could set the class weights to {0: 1.0, 1: 0.0, 2: 1.0}. Defaults to "auto" (balanced weighting).
 
         gridsearch_method (str, optional): Grid search method to use. Supported options include: {"gridsearch", "randomized_gridsearch", "genetic_algorithm"}. "gridsearch" uses GridSearchCV to test every possible parameter combination. "randomized_gridsearch" picks ``grid_iter`` random combinations of parameters to test. "genetic_algorithm" uses a genetic algorithm via the sklearn-genetic-opt GASearchCV module to do the grid search. If doing a grid search, "randomized_search" takes the least amount of time because it does not have to test all parameters. "genetic_algorithm" takes the longest. See the scikit-learn GridSearchCV and RandomizedSearchCV documentation for the "gridsearch" and "randomized_gridsearch" options, and the sklearn-genetic-opt GASearchCV documentation for the "genetic_algorithm" option. Defaults to "gridsearch".
 
         grid_iter (int, optional): Number of iterations to use for randomized and genetic algorithm grid searches. For randomized grid search, ``grid_iter`` parameter combinations will be randomly sampled. For the genetic algorithm, this determines how many generations the genetic algorithm will run. Defaults to 80.
 
-        scoring_metric (str, optional): Scoring metric to use for grid searches. See the classification metrics in the scikit-learn documentation (https://scikit-learn.org/stable/modules/model_evaluation.html) for supported options. Defaults to "f1_weighted".
+        scoring_metric (str, optional): Scoring metric to use for grid searches. The neural network imputers use a multimetric scorer and use different string values for the grid searches. Supported options include: {"accuracy", "hamming", "auc_macro", "auc_micro", "precision_recall_macro", "precision_recall_micro", "precision_recall_samples", "f1_score", and "f1_score_weighted"}. All of the above metrics are calculated during the grid search, but the provided string just sets the metric that the grid search refits to (i.e., which one is used in the best estimator). "accuracy" is just the ``number of correct calls / total calls``\. "hamming" calculates the Hamming distance. "auc_macro" does roc_auc_score with macro averaging. "auc_micro" does roc_auc_score with micro averaging. "precision_recall_macro" calculates precision and recall scores with macro averaging. "precision_recall_micro" similarly uses micro averaging. "precision_recall_samples" calculates the precision/ recall scores per samples instead of per label. "f1_score" calculates F1 scores with macro averaging, which is the harmonic mean of precision and recall and does not account for class imbalance. "f1_score_weighted" is simular to "f1_score" but accounts for class imbalance with weighting. Defaults to "f1_score_weighted".
 
         population_size (int or str, optional): Only used for the genetic algorithm grid search. Size of the initial population to sample randomly generated individuals. If set to "auto", then ``population_size`` is calculated as ``15 * n_parameters``\. If set to an integer, then uses the integer value as ``population_size``\. If you need to speed up the genetic algorithm grid search, try decreasing this parameter. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to "auto".
 
         tournament_size (int, optional): For genetic algorithm grid search only. Number of individuals to perform tournament selection. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to 3.
 
         elitism (bool, optional): For genetic algorithm grid search only. If set to True, takes the ``tournament_size`` best solution to the next generation. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to True.
 
-        crossover_probability (float, optional): For genetic algorithm grid search only. Probability of crossover operation between two individuals. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to 0.8.
+        crossover_probability (float, optional): For genetic algorithm grid search only. Probability of crossover operation between two individuals. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to 0.2.
 
-        mutation_probability (float, optional): For genetic algorithm grid search only. Probability of child mutation. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to 0.2.
+        mutation_probability (float, optional): For genetic algorithm grid search only. Probability of child mutation. See GASearchCV in the sklearn-genetic-opt documentation (https://sklearn-genetic-opt.readthedocs.io) for more info. Defaults to 0.8.
 
         ga_algorithm (str, optional): For genetic algorithm grid search only. Evolutionary algorithm to use. Supported options include: {"eaMuPlusLambda", "eaMuCommaLambda", "eaSimple"}. If you need to speed up the genetic algorithm grid search, try setting ``algorithm`` to "euSimple", at the expense of evolutionary model robustness. See more details in the DEAP algorithms documentation (https://deap.readthedocs.io). Defaults to "eaMuPlusLambda".
 
         sim_strategy (str, optional): Strategy to use for simulating missing data. Only used to validate the accuracy of the imputation. The final model will be trained with the non-simulated dataset. Supported options include: {"random", "random_weighted", "nonrandom", "nonrandom_weighted"}. "random" randomly simulates missing data, while "random_weighted" also does this but balances selection of reference, heterozygous, and alternate alleles. When set to "nonrandom", branches from ``GenotypeData.guidetree`` will be randomly sampled to generate missing data on descendant nodes. For "nonrandom_weighted", missing data will be placed on nodes proportionally to their branch lengths (e.g., to generate data distributed as might be the case with mutation-disruption of RAD sites). If using the "nonrandom" or "nonrandom_weighted" options, a guide tree is required to have been initialized in the passed ``genotype_data`` object. Defaults to "random".
 
         sim_prop_missing (float, optional): Proportion of missing data to use with missing data simulation. Defaults to 0.2.
```

### Comparing `pg-sui-0.2.3.1/pgsui/impute/impute.py` & `pg-sui-0.2.4/pgsui/impute/impute.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/impute/simple_imputers.py` & `pg-sui-0.2.4/pgsui/impute/simple_imputers.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/impute/supervised/iterative_imputer_fixedparams.py` & `pg-sui-0.2.4/pgsui/impute/supervised/iterative_imputer_fixedparams.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/impute/supervised/iterative_imputer_gridsearch.py` & `pg-sui-0.2.4/pgsui/impute/supervised/iterative_imputer_gridsearch.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/impute/unsupervised/callbacks.py` & `pg-sui-0.2.4/pgsui/impute/unsupervised/callbacks.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/impute/unsupervised/keras_classifiers.py` & `pg-sui-0.2.4/pgsui/impute/unsupervised/keras_classifiers.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/impute/unsupervised/models/autoencoder_model.py` & `pg-sui-0.2.4/pgsui/impute/unsupervised/models/autoencoder_model.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/impute/unsupervised/models/in_development/cnn_model.py` & `pg-sui-0.2.4/pgsui/impute/unsupervised/models/in_development/cnn_model.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/impute/unsupervised/models/nlpca_model.py` & `pg-sui-0.2.4/pgsui/impute/unsupervised/models/nlpca_model.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/impute/unsupervised/models/ubp_model.py` & `pg-sui-0.2.4/pgsui/impute/unsupervised/models/ubp_model.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/impute/unsupervised/models/vae_model.py` & `pg-sui-0.2.4/pgsui/impute/unsupervised/models/vae_model.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/impute/unsupervised/neural_network_imputers.py` & `pg-sui-0.2.4/pgsui/impute/unsupervised/neural_network_imputers.py`

 * *Files 0% similar despite different names*

```diff
@@ -314,14 +314,15 @@
         y_train = self.tt_.fit_transform(self.y_original_)
 
         if self.gridparams is not None:
             self.scoring_metrics_ = [
                 "precision_recall_macro",
                 "precision_recall_micro",
                 "f1_score",
+                "f1_score_weighted",
                 "auc_macro",
                 "auc_micro",
                 "accuracy",
                 "hamming",
             ]
 
         (
```

### Comparing `pg-sui-0.2.3.1/pgsui/impute/unsupervised/neural_network_methods.py` & `pg-sui-0.2.4/pgsui/impute/unsupervised/neural_network_methods.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/pg_sui.py` & `pg-sui-0.2.4/pgsui/pg_sui.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/utils/misc.py` & `pg-sui-0.2.4/pgsui/utils/misc.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/utils/plotting.py` & `pg-sui-0.2.4/pgsui/utils/plotting.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/pgsui/utils/scorers.py` & `pg-sui-0.2.4/pgsui/utils/scorers.py`

 * *Files 4% similar despite different names*

```diff
@@ -194,26 +194,31 @@
             y_true_bin, y_pred_proba_bin, average="micro"
         )
 
         average_precision["macro"] = average_precision_score(
             y_true_bin, y_pred_proba_bin, average="macro"
         )
 
+        average_precision["weighted"] = average_precision_score(
+            y_true_bin, y_pred_proba_bin, average="weighted"
+        )
+
         if use_int_encodings:
             y_pred_012 = (
                 nn.decode_masked(
                     y_true_bin,
                     y_pred_proba_bin,
                     threshold=thresh,
                     return_multilab=True,
                     predict_still_missing=False,
                 ),
             )
 
         f1 = f1_score(y_true_bin, y_pred_012, average="macro")
+        f1_weighted = f1_score(y_true_bin, y_pred_012, average="weighted")
 
         # Aggregate all recalls
         all_recall = np.unique(np.concatenate([recall[i] for i in classes]))
 
         # Then interpolate all PR curves at these points.
         mean_precision = np.zeros_like(all_recall)
         for i in classes:
@@ -226,14 +231,15 @@
         precision["macro"] = mean_precision
 
         results = dict()
 
         results["micro"] = average_precision["micro"]
         results["macro"] = average_precision["macro"]
         results["f1_score"] = f1
+        results["f1_score_weighted"] = f1_weighted
         results["recall_macro"] = all_recall
         results["precision_macro"] = mean_precision
         results["recall_micro"] = recall["micro"]
         results["precision_micro"] = precision["micro"]
 
         for i in classes:
             results[f"recall_{i}"] = recall[i]
@@ -510,16 +516,16 @@
         pr_ap = Scorers.compute_pr(
             y_true_masked, y_pred_masked, num_classes=num_classes
         )
 
         return pr_ap["samples"]
 
     @staticmethod
-    def f1_samples(y_true, y_pred, **kwargs):
-        """Get F1 score with samples averaging for grid search.
+    def f1_macro(y_true, y_pred, **kwargs):
+        """Get F1 score with macro averaging for grid search.
 
         If provided, only calculates score where missing_mask is True (i.e., data were missing). This is so that users can simulate missing data for known values, and then the predictions for only those known values can be evaluated.
 
         Args:
             y_true (numpy.ndarray): 012-encoded true target values.
 
             y_pred (tensorflow.EagerTensor): Predictions from model as probabilities.
@@ -541,14 +547,45 @@
 
         pr_ap = Scorers.compute_pr(
             y_true_masked, y_pred_masked, num_classes=num_classes
         )
 
         return pr_ap["f1_score"]
 
+    def f1_weighted(y_true, y_pred, **kwargs):
+        """Get F1 score with weighted averaging for grid search.
+
+        If provided, only calculates score where missing_mask is True (i.e., data were missing). This is so that users can simulate missing data for known values, and then the predictions for only those known values can be evaluated.
+
+        Args:
+            y_true (numpy.ndarray): 012-encoded true target values.
+
+            y_pred (tensorflow.EagerTensor): Predictions from model as probabilities.
+
+            kwargs (Any): Keyword arguments to use with scorer. Supported options include ``missing_mask`` and ``testing``\.
+
+        Returns:
+            float: Metric score by comparing y_true and y_pred.
+        """
+        # Get missing mask if provided.
+        # Otherwise default is all missing values (array all True).
+        missing_mask = kwargs.get("missing_mask")
+        num_classes = kwargs.get("num_classes", 3)
+
+        y_pred = Scorers.check_if_tuple(y_pred)
+
+        y_true_masked = y_true[missing_mask]
+        y_pred_masked = y_pred[missing_mask]
+
+        pr_ap = Scorers.compute_pr(
+            y_true_masked, y_pred_masked, num_classes=num_classes
+        )
+
+        return pr_ap["f1_score_weighted"]
+
     @staticmethod
     def pr_micro(y_true, y_pred, **kwargs):
         """Get Precision-Recall score with micro averaging for grid search.
 
         If provided, only calculates score where missing_mask is True (i.e., data were missing). This is so that users can simulate missing data for known values, and then the predictions for only those known values can be evaluated.
 
         Args:
@@ -599,75 +636,46 @@
 
         Raises:
             ValueError: Invalid scoring metric provided.
         """
         if isinstance(metrics, str):
             metrics = [metrics]
 
+        # Create a dictionary mapping metric names to their corresponding methods
+        scoring_methods = {
+            "accuracy": cls.accuracy_scorer,
+            "hamming": cls.hamming_scorer,
+            "auc_macro": cls.auc_macro,
+            "auc_micro": cls.auc_micro,
+            "precision_recall_macro": cls.pr_macro,
+            "precision_recall_micro": cls.pr_micro,
+            "precision_recall_samples": cls.pr_samples,
+            "f1_score": cls.f1_macro,
+            "f1_score_weighted": cls.f1_weighted,
+        }
+
+        # Create a dictionary for the default parameters
+        default_params = {
+            "missing_mask": missing_mask,
+            "num_classes": num_classes,
+            "testing": testing,
+        }
+
         scorers = dict()
         for item in metrics:
-            if item.lower() == "accuracy":
-                scorers["accuracy"] = make_scorer(
-                    cls.accuracy_scorer,
-                    missing_mask=missing_mask,
-                    num_classes=num_classes,
-                    testing=testing,
-                )
-            elif item.lower() == "hamming":
-                scorers["hamming"] = make_scorer(
-                    cls.hamming_scorer,
-                    missing_mask=missing_mask,
-                    num_classes=num_classes,
-                    testing=testing,
-                    greater_is_better=False,
-                )
-            elif item.lower() == "auc_macro":
-                scorers["auc_macro"] = make_scorer(
-                    cls.auc_macro,
-                    missing_mask=missing_mask,
-                    num_classes=num_classes,
-                    testing=testing,
-                )
-            elif item.lower() == "auc_micro":
-                scorers["auc_micro"] = make_scorer(
-                    cls.auc_micro,
-                    missing_mask=missing_mask,
-                    num_classes=num_classes,
-                    testing=testing,
-                )
-            elif item.lower() == "precision_recall_macro":
-                scorers["precision_recall_macro"] = make_scorer(
-                    cls.pr_macro,
-                    missing_mask=missing_mask,
-                    num_classes=num_classes,
-                    testing=testing,
-                )
-            elif item.lower() == "precision_recall_micro":
-                scorers["precision_recall_micro"] = make_scorer(
-                    cls.pr_micro,
-                    missing_mask=missing_mask,
-                    num_classes=num_classes,
-                    testing=testing,
-                )
-            elif item.lower() == "precision_recall_samples":
-                scorers["precision_recall_samples"] = make_scorer(
-                    cls.pr_samples,
-                    missing_mask=missing_mask,
-                    num_classes=num_classes,
-                    testing=testing,
-                )
-            elif item.lower() == "f1_score":
-                scorers["f1_score"] = make_scorer(
-                    cls.f1_samples,
-                    missing_mask=missing_mask,
-                    num_classes=num_classes,
-                    testing=testing,
-                )
-            else:
-                raise ValueError(f"Invalid scoring_metric provided: {item}")
+            item = item.lower()  # Ensure case insensitivity
+
+            if item in scoring_methods:
+                params = default_params.copy()  # Copy the default parameters
+
+                # For the 'hamming' scorer, we need to set 'greater_is_better' to False
+                if item == "hamming":
+                    params["greater_is_better"] = False
+
+                scorers[item] = make_scorer(scoring_methods[item], **params)
         return scorers
 
     @staticmethod
     def scorer(y_true, y_pred, **kwargs):
         # Get missing mask if provided.
         # Otherwise default is all missing values (array all True).
         missing_mask = kwargs.get("missing_mask")
```

### Comparing `pg-sui-0.2.3.1/pgsui/utils/sequence_tools.py` & `pg-sui-0.2.4/pgsui/utils/sequence_tools.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/setup.py` & `pg-sui-0.2.4/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 
 
 def read(fname):
     return open(os.path.join(os.path.dirname(__file__), fname)).read()
 
 
 NAME = "pg-sui"
-VERSION = "0.2.3.1"
+VERSION = "0.2.4"
 AUTHORS = "Bradley T. Martin and Tyler K. Chafin"
 AUTHOR_EMAIL = "evobio721@gmail.com"
 MAINTAINER = "Bradley T. Martin"
 DESCRIPTION = "Python machine and deep learning package to impute missing SNPs"
 LONG_DESCRIPTION = open("README.md").read()
 
 setup(
```

### Comparing `pg-sui-0.2.3.1/simulation/sim_benchmarks.py` & `pg-sui-0.2.4/simulation/sim_benchmarks.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/simulation/sim_treeparams.py` & `pg-sui-0.2.4/simulation/sim_treeparams.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/test/pg_sui_simtest.py` & `pg-sui-0.2.4/test/pg_sui_simtest.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/test/pg_sui_testing.py` & `pg-sui-0.2.4/test/pg_sui_testing.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/test/test_pgsui.py` & `pg-sui-0.2.4/test/test_pgsui.py`

 * *Files identical despite different names*

### Comparing `pg-sui-0.2.3.1/test/test_tkc.py` & `pg-sui-0.2.4/test/test_tkc.py`

 * *Files 26% similar despite different names*

```diff
@@ -86,14 +86,17 @@
         }
 
         instance = class_instance(
             self.simulated_data, 
             gridparams=param_grid, 
             **kwargs)
 
+        # Write the masks
+        self.transformer.write_mask(filename_prefix="mask_test")
+
         imputed_data = instance.imputed.genotypes_012(fmt="numpy")
 
         # Test that the imputed values are close to the original values
         accuracy = self.transformer.accuracy(
             self.genotype_data.genotypes_012(fmt="numpy"), imputed_data
         )
 
@@ -117,33 +120,59 @@
         )
         pprint.PrettyPrinter(indent=4, sort_dicts=True).pprint(
             f"RECALL PER CLASS: {dict(zip(range(3), recall_scores))}"
         )
         pprint.PrettyPrinter(indent=4, sort_dicts=True).pprint(
             f"AVERAGE PRECISION PER CLASS: {dict(zip(range(3), avg_precision_scores))}"
         )
+
+        # Read masks from file
+        self.transformer.read_mask(filename_prefix="mask_test")
+
+        # Recalculate accuracy after reading in the mask
+        accuracy_after_read = self.transformer.accuracy(
+            self.genotype_data.genotypes_012(fmt="numpy"), imputed_data
+        )
+
+        pprint.PrettyPrinter(indent=4, sort_dicts=True).pprint(
+            f"OVERALL ACCURACY AFTER READ: {accuracy_after_read}"
+        )
+        pprint.PrettyPrinter(indent=4, sort_dicts=True).pprint(
+            f"AUC-ROC PER CLASS AFTER READ: {dict(zip(range(3), auc_roc_scores))}"
+        )
+        pprint.PrettyPrinter(indent=4, sort_dicts=True).pprint(
+            f"PRECISION PER CLASS AFTER READ: {dict(zip(range(3), precision_scores))}"
+        )
+        pprint.PrettyPrinter(indent=4, sort_dicts=True).pprint(
+            f"RECALL PER CLASS AFTER READ: {dict(zip(range(3), recall_scores))}"
+        )
+        pprint.PrettyPrinter(indent=4, sort_dicts=True).pprint(
+            f"AVERAGE PRECISION PER CLASS AFTER READ: {dict(zip(range(3), avg_precision_scores))}"
+        )
+
+
         print("\n")
 
     # def test_ImputeKNN(self):
     #     self._test_class(ImputeKNN)
 
     # def test_ImputeRandomForest(self):
     #     self._test_class(ImputeRandomForest)
 
     # def test_ImputeXGBoost(self):
     #     self._test_class(ImputeXGBoost)
 
-    # def test_ImputeVAE(self):
-    #     self._test_class(ImputeVAE)
+    def test_ImputeVAE(self):
+        self._test_class(ImputeVAE)
 
     # def test_ImputeStandardAutoEncoder(self):
     #     self._test_class(ImputeStandardAutoEncoder)
 
-    def test_ImputeUBP(self):
-        self._test_class(ImputeUBP)
+    # def test_ImputeUBP(self):
+    #     self._test_class(ImputeUBP)
 
     # def test_ImputeNLPCA(self):
     #     self._test_class(ImputeNLPCA)
 
     # def test_ImputeKNN_grid(self):
     #     self._test_class(ImputeKNN, do_gridsearch=True)
```

