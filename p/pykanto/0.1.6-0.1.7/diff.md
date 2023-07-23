# Comparing `tmp/pykanto-0.1.6.tar.gz` & `tmp/pykanto-0.1.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pykanto-0.1.6.tar", last modified: Fri Jan  1 00:00:00 2016, max compression
+gzip compressed data, was "pykanto-0.1.7.tar", last modified: Fri Jan  1 00:00:00 2016, max compression
```

## Comparing `pykanto-0.1.6.tar` & `pykanto-0.1.7.tar`

### file list

```diff
@@ -1,106 +1,106 @@
--rwxr-xr-x   0        0        0     1084 2023-07-10 17:04:41.657898 pykanto-0.1.6/LICENSE
--rwxr-xr-x   0        0        0     4677 2023-07-10 17:04:41.657898 pykanto-0.1.6/README.md
--rwxr-xr-x   0        0        0        0 2023-07-10 17:04:41.845901 pykanto-0.1.6/pykanto/__init__.py
--rw-r--r--   0        0        0       89 2023-07-10 17:04:41.845901 pykanto-0.1.6/pykanto/app/__init__.py
--rw-r--r--   0        0        0     7980 2023-07-10 17:04:41.845901 pykanto-0.1.6/pykanto/app/data.py
--rw-r--r--   0        0        0    19087 2023-07-10 17:04:41.845901 pykanto-0.1.6/pykanto/app/main.py
--rw-r--r--   0        0        0     1331 2023-07-10 17:04:41.845901 pykanto-0.1.6/pykanto/app/static/lasso.png
--rw-r--r--   0        0        0     5780 2023-07-10 17:04:41.845901 pykanto-0.1.6/pykanto/app/static/pykanto-logo.svg
--rw-r--r--   0        0        0     2565 2023-07-10 17:04:41.845901 pykanto-0.1.6/pykanto/app/templates/index.html
--rw-r--r--   0        0        0     6889 2023-07-10 17:04:41.845901 pykanto-0.1.6/pykanto/app/templates/styles.css
--rw-r--r--   0        0        0      536 2023-07-10 17:04:41.845901 pykanto-0.1.6/pykanto/app/theme.yaml
--rw-r--r--   0        0        0    94446 2023-07-10 17:04:41.845901 pykanto-0.1.6/pykanto/data/raw/AM/20210502_040000.WAV
--rw-r--r--   0        0        0      957 2023-07-10 17:04:41.845901 pykanto-0.1.6/pykanto/data/raw/AM/20210502_040000.xml
--rwxr-xr-x   0        0        0  1464876 2023-07-10 17:04:41.857901 pykanto-0.1.6/pykanto/data/raw/BENGALESE_FINCH/bird_3/348.wav
--rwxr-xr-x   0        0        0      609 2023-07-10 17:04:41.857901 pykanto-0.1.6/pykanto/data/raw/BENGALESE_FINCH/bird_3/348.xml
--rwxr-xr-x   0        0        0  1345900 2023-07-10 17:04:41.865902 pykanto-0.1.6/pykanto/data/raw/BENGALESE_FINCH/bird_3/363.wav
--rwxr-xr-x   0        0        0      611 2023-07-10 17:04:41.865902 pykanto-0.1.6/pykanto/data/raw/BENGALESE_FINCH/bird_3/363.xml
--rwxr-xr-x   0        0        0  1235284 2023-07-10 17:04:41.873902 pykanto-0.1.6/pykanto/data/raw/STORM-PETREL/XC46092.wav
--rwxr-xr-x   0        0        0     1054 2023-07-10 17:04:41.873902 pykanto-0.1.6/pykanto/data/raw/STORM-PETREL/XC46092.xml
--rwxr-xr-x   0        0        0  2713688 2023-07-10 17:04:41.889902 pykanto-0.1.6/pykanto/data/raw/STORM-PETREL/XC663885.wav
--rwxr-xr-x   0        0        0      967 2023-07-10 17:04:41.889902 pykanto-0.1.6/pykanto/data/raw/STORM-PETREL/XC663885.xml
--rwxr-xr-x   0        0        0      869 2023-07-10 17:04:41.889902 pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-B32-0415_05-11.JSON
--rwxr-xr-x   0        0        0      870 2023-07-10 17:04:41.889902 pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-B32-0415_05-15.JSON
--rwxr-xr-x   0        0        0      869 2023-07-10 17:04:41.889902 pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-B32-0415_05-21.JSON
--rwxr-xr-x   0        0        0      869 2023-07-10 17:04:41.889902 pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-B32-0415_05-23.JSON
--rwxr-xr-x   0        0        0      867 2023-07-10 17:04:41.889902 pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-B32-0415_05-3.JSON
--rwxr-xr-x   0        0        0      869 2023-07-10 17:04:41.889902 pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-B32-0415_05-6.JSON
--rwxr-xr-x   0        0        0      867 2023-07-10 17:04:41.889902 pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-B32-0415_05-9.JSON
--rwxr-xr-x   0        0        0      873 2023-07-10 17:04:41.889902 pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-B32-0416_04-21.JSON
--rwxr-xr-x   0        0        0      874 2023-07-10 17:04:41.889902 pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-B32-0416_04-23.JSON
--rwxr-xr-x   0        0        0      874 2023-07-10 17:04:41.889902 pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-B32-0416_04-24.JSON
--rwxr-xr-x   0        0        0      870 2023-07-10 17:04:41.889902 pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-B32-0416_05-20.JSON
--rwxr-xr-x   0        0        0      872 2023-07-10 17:04:41.889902 pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-77.JSON
--rwxr-xr-x   0        0        0      868 2023-07-10 17:04:41.889902 pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-78.JSON
--rwxr-xr-x   0        0        0      872 2023-07-10 17:04:41.889902 pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-79.JSON
--rwxr-xr-x   0        0        0      869 2023-07-10 17:04:41.893902 pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-80.JSON
--rwxr-xr-x   0        0        0      870 2023-07-10 17:04:41.893902 pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-81.JSON
--rwxr-xr-x   0        0        0      872 2023-07-10 17:04:41.893902 pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-86.JSON
--rwxr-xr-x   0        0        0      872 2023-07-10 17:04:41.893902 pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-88.JSON
--rwxr-xr-x   0        0        0      870 2023-07-10 17:04:41.893902 pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-91.JSON
--rwxr-xr-x   0        0        0      871 2023-07-10 17:04:41.893902 pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-92.JSON
--rwxr-xr-x   0        0        0   109412 2023-07-10 17:04:41.893902 pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-B32-0415_05-11.wav
--rwxr-xr-x   0        0        0   114704 2023-07-10 17:04:41.893902 pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-B32-0415_05-15.wav
--rwxr-xr-x   0        0        0   114116 2023-07-10 17:04:41.893902 pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-B32-0415_05-21.wav
--rwxr-xr-x   0        0        0   118820 2023-07-10 17:04:41.893902 pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-B32-0415_05-23.wav
--rwxr-xr-x   0        0        0    95300 2023-07-10 17:04:41.893902 pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-B32-0415_05-3.wav
--rwxr-xr-x   0        0        0   119408 2023-07-10 17:04:41.897902 pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-B32-0415_05-6.wav
--rwxr-xr-x   0        0        0   147044 2023-07-10 17:04:41.897902 pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-B32-0415_05-9.wav
--rwxr-xr-x   0        0        0   131992 2023-07-10 17:04:41.897902 pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-B32-0416_04-21.wav
--rwxr-xr-x   0        0        0   155982 2023-07-10 17:04:41.897902 pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-B32-0416_04-23.wav
--rwxr-xr-x   0        0        0   127758 2023-07-10 17:04:41.901902 pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-B32-0416_04-24.wav
--rwxr-xr-x   0        0        0    92360 2023-07-10 17:04:41.901902 pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-B32-0416_05-20.wav
--rwxr-xr-x   0        0        0    97652 2023-07-10 17:04:41.901902 pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-77.wav
--rwxr-xr-x   0        0        0   183500 2023-07-10 17:04:41.901902 pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-78.wav
--rwxr-xr-x   0        0        0   222308 2023-07-10 17:04:41.905902 pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-79.wav
--rwxr-xr-x   0        0        0   131756 2023-07-10 17:04:41.905902 pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-80.wav
--rwxr-xr-x   0        0        0   119996 2023-07-10 17:04:41.905902 pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-81.wav
--rwxr-xr-x   0        0        0   142340 2023-07-10 17:04:41.905902 pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-86.wav
--rwxr-xr-x   0        0        0   142340 2023-07-10 17:04:41.909902 pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-88.wav
--rwxr-xr-x   0        0        0   127052 2023-07-10 17:04:41.909902 pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-91.wav
--rwxr-xr-x   0        0        0    72956 2023-07-10 17:04:41.909902 pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-92.wav
--rwxr-xr-x   0        0        0    43241 2023-07-10 17:04:41.909902 pykanto-0.1.6/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC46092_0.gzip
--rwxr-xr-x   0        0        0    42128 2023-07-10 17:04:41.909902 pykanto-0.1.6/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC46092_1.gzip
--rwxr-xr-x   0        0        0    44120 2023-07-10 17:04:41.909902 pykanto-0.1.6/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC46092_2.gzip
--rwxr-xr-x   0        0        0    41684 2023-07-10 17:04:41.909902 pykanto-0.1.6/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC46092_3.gzip
--rwxr-xr-x   0        0        0    41167 2023-07-10 17:04:41.909902 pykanto-0.1.6/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC46092_4.gzip
--rwxr-xr-x   0        0        0    40197 2023-07-10 17:04:41.909902 pykanto-0.1.6/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC46092_5.gzip
--rwxr-xr-x   0        0        0    40034 2023-07-10 17:04:41.909902 pykanto-0.1.6/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC663885_0.gzip
--rwxr-xr-x   0        0        0    38139 2023-07-10 17:04:41.909902 pykanto-0.1.6/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC663885_1.gzip
--rwxr-xr-x   0        0        0    42169 2023-07-10 17:04:41.909902 pykanto-0.1.6/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC663885_2.gzip
--rwxr-xr-x   0        0        0    43081 2023-07-10 17:04:41.909902 pykanto-0.1.6/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC663885_3.gzip
--rwxr-xr-x   0        0        0    36610 2023-07-10 17:04:41.909902 pykanto-0.1.6/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC663885_4.gzip
--rw-r--r--   0        0        0      578 2023-07-10 17:04:41.909902 pykanto-0.1.6/pykanto/data/segmented/storm-petrel/JSON/STORM-PETREL_XC46092_0.JSON
--rw-r--r--   0        0        0      580 2023-07-10 17:04:41.909902 pykanto-0.1.6/pykanto/data/segmented/storm-petrel/JSON/STORM-PETREL_XC46092_1.JSON
--rw-r--r--   0        0        0      582 2023-07-10 17:04:41.909902 pykanto-0.1.6/pykanto/data/segmented/storm-petrel/JSON/STORM-PETREL_XC46092_2.JSON
--rw-r--r--   0        0        0      580 2023-07-10 17:04:41.909902 pykanto-0.1.6/pykanto/data/segmented/storm-petrel/JSON/STORM-PETREL_XC46092_3.JSON
--rw-r--r--   0        0        0      580 2023-07-10 17:04:41.913902 pykanto-0.1.6/pykanto/data/segmented/storm-petrel/JSON/STORM-PETREL_XC46092_4.JSON
--rw-r--r--   0        0        0      580 2023-07-10 17:04:41.913902 pykanto-0.1.6/pykanto/data/segmented/storm-petrel/JSON/STORM-PETREL_XC46092_5.JSON
--rw-r--r--   0        0        0      468 2023-07-10 17:04:41.913902 pykanto-0.1.6/pykanto/data/segmented/storm-petrel/JSON/STORM-PETREL_XC663885_0.JSON
--rw-r--r--   0        0        0      585 2023-07-10 17:04:41.913902 pykanto-0.1.6/pykanto/data/segmented/storm-petrel/JSON/STORM-PETREL_XC663885_1.JSON
--rw-r--r--   0        0        0      584 2023-07-10 17:04:41.913902 pykanto-0.1.6/pykanto/data/segmented/storm-petrel/JSON/STORM-PETREL_XC663885_2.JSON
--rw-r--r--   0        0        0      585 2023-07-10 17:04:41.913902 pykanto-0.1.6/pykanto/data/segmented/storm-petrel/JSON/STORM-PETREL_XC663885_3.JSON
--rw-r--r--   0        0        0      583 2023-07-10 17:04:41.913902 pykanto-0.1.6/pykanto/data/segmented/storm-petrel/JSON/STORM-PETREL_XC663885_4.JSON
--rw-r--r--   0        0        0    35189 2023-07-10 17:04:41.913902 pykanto-0.1.6/pykanto/dataset.py
--rw-r--r--   0        0        0     4925 2023-07-10 17:04:41.913902 pykanto-0.1.6/pykanto/parameters.py
--rw-r--r--   0        0        0    16544 2023-07-10 17:04:41.913902 pykanto-0.1.6/pykanto/plot.py
--rwxr-xr-x   0        0        0       84 2023-07-10 17:04:41.913902 pykanto-0.1.6/pykanto/signal/__init__.py
--rw-r--r--   0        0        0     6340 2023-07-10 17:04:41.913902 pykanto-0.1.6/pykanto/signal/analysis.py
--rw-r--r--   0        0        0     9724 2023-07-10 17:04:41.913902 pykanto-0.1.6/pykanto/signal/cluster.py
--rwxr-xr-x   0        0        0     7266 2023-07-10 17:04:41.913902 pykanto-0.1.6/pykanto/signal/filter.py
--rwxr-xr-x   0        0        0    26776 2023-07-10 17:04:41.913902 pykanto-0.1.6/pykanto/signal/segment.py
--rw-r--r--   0        0        0    15761 2023-07-10 17:04:41.913902 pykanto-0.1.6/pykanto/signal/spectrogram.py
--rwxr-xr-x   0        0        0       59 2023-07-10 17:04:41.913902 pykanto-0.1.6/pykanto/utils/__init__.py
--rw-r--r--   0        0        0     6257 2023-07-10 17:04:41.913902 pykanto-0.1.6/pykanto/utils/compute.py
--rw-r--r--   0        0        0     6050 2023-07-10 17:04:41.913902 pykanto-0.1.6/pykanto/utils/custom.py
--rw-r--r--   0        0        0    12023 2023-07-10 17:04:41.913902 pykanto-0.1.6/pykanto/utils/io.py
--rwxr-xr-x   0        0        0    16024 2023-07-10 17:04:41.913902 pykanto-0.1.6/pykanto/utils/paths.py
--rw-r--r--   0        0        0        7 2023-07-10 17:04:41.913902 pykanto-0.1.6/pykanto/utils/slurm/.gitignore
--rw-r--r--   0        0        0     1070 2023-07-10 17:04:41.913902 pykanto-0.1.6/pykanto/utils/slurm/LICENSE
--rwxr-xr-x   0        0        0       50 2023-07-10 17:04:41.913902 pykanto-0.1.6/pykanto/utils/slurm/__init__.py
--rw-r--r--   0        0        0     5544 2023-07-10 17:04:41.913902 pykanto-0.1.6/pykanto/utils/slurm/launch.py
--rw-r--r--   0        0        0     2422 2023-07-10 17:04:41.913902 pykanto-0.1.6/pykanto/utils/slurm/sbatch_template.sh
--rw-r--r--   0        0        0      792 2023-07-10 17:04:41.913902 pykanto-0.1.6/pykanto/utils/slurm/tester.py
--rw-r--r--   0        0        0     4760 2023-07-10 17:04:41.913902 pykanto-0.1.6/pykanto/utils/types.py
--rw-r--r--   0        0        0     1613 2023-07-10 17:04:41.913902 pykanto-0.1.6/pyproject.toml
--rw-r--r--   0        0        0     6472 1970-01-01 00:00:00.000000 pykanto-0.1.6/PKG-INFO
+-rwxr-xr-x   0        0        0     1084 2023-07-23 13:56:15.445113 pykanto-0.1.7/LICENSE
+-rwxr-xr-x   0        0        0     4677 2023-07-23 13:56:15.445113 pykanto-0.1.7/README.md
+-rwxr-xr-x   0        0        0        0 2023-07-23 13:56:15.633117 pykanto-0.1.7/pykanto/__init__.py
+-rw-r--r--   0        0        0       89 2023-07-23 13:56:15.633117 pykanto-0.1.7/pykanto/app/__init__.py
+-rw-r--r--   0        0        0     7980 2023-07-23 13:56:15.633117 pykanto-0.1.7/pykanto/app/data.py
+-rw-r--r--   0        0        0    19087 2023-07-23 13:56:15.633117 pykanto-0.1.7/pykanto/app/main.py
+-rw-r--r--   0        0        0     1331 2023-07-23 13:56:15.633117 pykanto-0.1.7/pykanto/app/static/lasso.png
+-rw-r--r--   0        0        0     5780 2023-07-23 13:56:15.633117 pykanto-0.1.7/pykanto/app/static/pykanto-logo.svg
+-rw-r--r--   0        0        0     2565 2023-07-23 13:56:15.633117 pykanto-0.1.7/pykanto/app/templates/index.html
+-rw-r--r--   0        0        0     6889 2023-07-23 13:56:15.633117 pykanto-0.1.7/pykanto/app/templates/styles.css
+-rw-r--r--   0        0        0      536 2023-07-23 13:56:15.633117 pykanto-0.1.7/pykanto/app/theme.yaml
+-rw-r--r--   0        0        0    94446 2023-07-23 13:56:15.633117 pykanto-0.1.7/pykanto/data/raw/AM/20210502_040000.WAV
+-rw-r--r--   0        0        0      957 2023-07-23 13:56:15.633117 pykanto-0.1.7/pykanto/data/raw/AM/20210502_040000.xml
+-rwxr-xr-x   0        0        0  1464876 2023-07-23 13:56:15.645117 pykanto-0.1.7/pykanto/data/raw/BENGALESE_FINCH/bird_3/348.wav
+-rwxr-xr-x   0        0        0      609 2023-07-23 13:56:15.645117 pykanto-0.1.7/pykanto/data/raw/BENGALESE_FINCH/bird_3/348.xml
+-rwxr-xr-x   0        0        0  1345900 2023-07-23 13:56:15.653117 pykanto-0.1.7/pykanto/data/raw/BENGALESE_FINCH/bird_3/363.wav
+-rwxr-xr-x   0        0        0      611 2023-07-23 13:56:15.653117 pykanto-0.1.7/pykanto/data/raw/BENGALESE_FINCH/bird_3/363.xml
+-rwxr-xr-x   0        0        0  1235284 2023-07-23 13:56:15.661117 pykanto-0.1.7/pykanto/data/raw/STORM-PETREL/XC46092.wav
+-rwxr-xr-x   0        0        0     1054 2023-07-23 13:56:15.661117 pykanto-0.1.7/pykanto/data/raw/STORM-PETREL/XC46092.xml
+-rwxr-xr-x   0        0        0  2713688 2023-07-23 13:56:15.681118 pykanto-0.1.7/pykanto/data/raw/STORM-PETREL/XC663885.wav
+-rwxr-xr-x   0        0        0      967 2023-07-23 13:56:15.681118 pykanto-0.1.7/pykanto/data/raw/STORM-PETREL/XC663885.xml
+-rwxr-xr-x   0        0        0      869 2023-07-23 13:56:15.681118 pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-B32-0415_05-11.JSON
+-rwxr-xr-x   0        0        0      870 2023-07-23 13:56:15.681118 pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-B32-0415_05-15.JSON
+-rwxr-xr-x   0        0        0      869 2023-07-23 13:56:15.681118 pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-B32-0415_05-21.JSON
+-rwxr-xr-x   0        0        0      869 2023-07-23 13:56:15.681118 pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-B32-0415_05-23.JSON
+-rwxr-xr-x   0        0        0      867 2023-07-23 13:56:15.681118 pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-B32-0415_05-3.JSON
+-rwxr-xr-x   0        0        0      869 2023-07-23 13:56:15.681118 pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-B32-0415_05-6.JSON
+-rwxr-xr-x   0        0        0      867 2023-07-23 13:56:15.681118 pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-B32-0415_05-9.JSON
+-rwxr-xr-x   0        0        0      873 2023-07-23 13:56:15.681118 pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-B32-0416_04-21.JSON
+-rwxr-xr-x   0        0        0      874 2023-07-23 13:56:15.681118 pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-B32-0416_04-23.JSON
+-rwxr-xr-x   0        0        0      874 2023-07-23 13:56:15.681118 pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-B32-0416_04-24.JSON
+-rwxr-xr-x   0        0        0      870 2023-07-23 13:56:15.681118 pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-B32-0416_05-20.JSON
+-rwxr-xr-x   0        0        0      872 2023-07-23 13:56:15.681118 pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-77.JSON
+-rwxr-xr-x   0        0        0      868 2023-07-23 13:56:15.681118 pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-78.JSON
+-rwxr-xr-x   0        0        0      872 2023-07-23 13:56:15.681118 pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-79.JSON
+-rwxr-xr-x   0        0        0      869 2023-07-23 13:56:15.681118 pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-80.JSON
+-rwxr-xr-x   0        0        0      870 2023-07-23 13:56:15.681118 pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-81.JSON
+-rwxr-xr-x   0        0        0      872 2023-07-23 13:56:15.681118 pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-86.JSON
+-rwxr-xr-x   0        0        0      872 2023-07-23 13:56:15.681118 pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-88.JSON
+-rwxr-xr-x   0        0        0      870 2023-07-23 13:56:15.681118 pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-91.JSON
+-rwxr-xr-x   0        0        0      871 2023-07-23 13:56:15.681118 pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-92.JSON
+-rwxr-xr-x   0        0        0   109412 2023-07-23 13:56:15.681118 pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-B32-0415_05-11.wav
+-rwxr-xr-x   0        0        0   114704 2023-07-23 13:56:15.681118 pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-B32-0415_05-15.wav
+-rwxr-xr-x   0        0        0   114116 2023-07-23 13:56:15.681118 pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-B32-0415_05-21.wav
+-rwxr-xr-x   0        0        0   118820 2023-07-23 13:56:15.685118 pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-B32-0415_05-23.wav
+-rwxr-xr-x   0        0        0    95300 2023-07-23 13:56:15.685118 pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-B32-0415_05-3.wav
+-rwxr-xr-x   0        0        0   119408 2023-07-23 13:56:15.685118 pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-B32-0415_05-6.wav
+-rwxr-xr-x   0        0        0   147044 2023-07-23 13:56:15.685118 pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-B32-0415_05-9.wav
+-rwxr-xr-x   0        0        0   131992 2023-07-23 13:56:15.685118 pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-B32-0416_04-21.wav
+-rwxr-xr-x   0        0        0   155982 2023-07-23 13:56:15.689118 pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-B32-0416_04-23.wav
+-rwxr-xr-x   0        0        0   127758 2023-07-23 13:56:15.689118 pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-B32-0416_04-24.wav
+-rwxr-xr-x   0        0        0    92360 2023-07-23 13:56:15.689118 pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-B32-0416_05-20.wav
+-rwxr-xr-x   0        0        0    97652 2023-07-23 13:56:15.689118 pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-77.wav
+-rwxr-xr-x   0        0        0   183500 2023-07-23 13:56:15.689118 pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-78.wav
+-rwxr-xr-x   0        0        0   222308 2023-07-23 13:56:15.693118 pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-79.wav
+-rwxr-xr-x   0        0        0   131756 2023-07-23 13:56:15.693118 pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-80.wav
+-rwxr-xr-x   0        0        0   119996 2023-07-23 13:56:15.693118 pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-81.wav
+-rwxr-xr-x   0        0        0   142340 2023-07-23 13:56:15.697118 pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-86.wav
+-rwxr-xr-x   0        0        0   142340 2023-07-23 13:56:15.697118 pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-88.wav
+-rwxr-xr-x   0        0        0   127052 2023-07-23 13:56:15.697118 pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-91.wav
+-rwxr-xr-x   0        0        0    72956 2023-07-23 13:56:15.697118 pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-92.wav
+-rwxr-xr-x   0        0        0    42128 2023-07-23 13:56:15.697118 pykanto-0.1.7/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC46092_128832.gzip
+-rwxr-xr-x   0        0        0    44120 2023-07-23 13:56:15.697118 pykanto-0.1.7/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC46092_202272.gzip
+-rwxr-xr-x   0        0        0    41684 2023-07-23 13:56:15.697118 pykanto-0.1.7/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC46092_278432.gzip
+-rwxr-xr-x   0        0        0    41167 2023-07-23 13:56:15.697118 pykanto-0.1.7/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC46092_350224.gzip
+-rwxr-xr-x   0        0        0    40197 2023-07-23 13:56:15.697118 pykanto-0.1.7/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC46092_492096.gzip
+-rwxr-xr-x   0        0        0    43241 2023-07-23 13:56:15.697118 pykanto-0.1.7/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC46092_53600.gzip
+-rwxr-xr-x   0        0        0    42169 2023-07-23 13:56:15.697118 pykanto-0.1.7/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC663885_219072.gzip
+-rwxr-xr-x   0        0        0    40034 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC663885_26280.gzip
+-rwxr-xr-x   0        0        0    43081 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC663885_350592.gzip
+-rwxr-xr-x   0        0        0    36610 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC663885_481896.gzip
+-rwxr-xr-x   0        0        0    38139 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC663885_91784.gzip
+-rw-r--r--   0        0        0     3322 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/data/segmented/storm-petrel/JSON/STORM-PETREL_XC46092_128832.JSON
+-rw-r--r--   0        0        0     3411 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/data/segmented/storm-petrel/JSON/STORM-PETREL_XC46092_202272.JSON
+-rw-r--r--   0        0        0     3270 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/data/segmented/storm-petrel/JSON/STORM-PETREL_XC46092_278432.JSON
+-rw-r--r--   0        0        0     3219 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/data/segmented/storm-petrel/JSON/STORM-PETREL_XC46092_350224.JSON
+-rw-r--r--   0        0        0     3127 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/data/segmented/storm-petrel/JSON/STORM-PETREL_XC46092_492096.JSON
+-rw-r--r--   0        0        0     3368 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/data/segmented/storm-petrel/JSON/STORM-PETREL_XC46092_53600.JSON
+-rw-r--r--   0        0        0     2564 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/data/segmented/storm-petrel/JSON/STORM-PETREL_XC663885_219072.JSON
+-rw-r--r--   0        0        0     2610 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/data/segmented/storm-petrel/JSON/STORM-PETREL_XC663885_26280.JSON
+-rw-r--r--   0        0        0     2465 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/data/segmented/storm-petrel/JSON/STORM-PETREL_XC663885_350592.JSON
+-rw-r--r--   0        0        0     2416 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/data/segmented/storm-petrel/JSON/STORM-PETREL_XC663885_481896.JSON
+-rw-r--r--   0        0        0     2514 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/data/segmented/storm-petrel/JSON/STORM-PETREL_XC663885_91784.JSON
+-rw-r--r--   0        0        0    35547 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/dataset.py
+-rw-r--r--   0        0        0     4925 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/parameters.py
+-rw-r--r--   0        0        0    16544 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/plot.py
+-rwxr-xr-x   0        0        0       84 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/signal/__init__.py
+-rw-r--r--   0        0        0     6340 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/signal/analysis.py
+-rw-r--r--   0        0        0    10473 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/signal/cluster.py
+-rwxr-xr-x   0        0        0     7266 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/signal/filter.py
+-rwxr-xr-x   0        0        0    26776 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/signal/segment.py
+-rw-r--r--   0        0        0    15761 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/signal/spectrogram.py
+-rwxr-xr-x   0        0        0       59 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/utils/__init__.py
+-rw-r--r--   0        0        0     6257 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/utils/compute.py
+-rw-r--r--   0        0        0     6050 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/utils/custom.py
+-rw-r--r--   0        0        0    12023 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/utils/io.py
+-rwxr-xr-x   0        0        0    16024 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/utils/paths.py
+-rw-r--r--   0        0        0        7 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/utils/slurm/.gitignore
+-rw-r--r--   0        0        0     1070 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/utils/slurm/LICENSE
+-rwxr-xr-x   0        0        0       50 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/utils/slurm/__init__.py
+-rw-r--r--   0        0        0     5544 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/utils/slurm/launch.py
+-rw-r--r--   0        0        0     2422 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/utils/slurm/sbatch_template.sh
+-rw-r--r--   0        0        0      792 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/utils/slurm/tester.py
+-rw-r--r--   0        0        0     4760 2023-07-23 13:56:15.701118 pykanto-0.1.7/pykanto/utils/types.py
+-rw-r--r--   0        0        0     1613 2023-07-23 13:56:15.701118 pykanto-0.1.7/pyproject.toml
+-rw-r--r--   0        0        0     6472 1970-01-01 00:00:00.000000 pykanto-0.1.7/PKG-INFO
```

### Comparing `pykanto-0.1.6/LICENSE` & `pykanto-0.1.7/LICENSE`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/README.md` & `pykanto-0.1.7/README.md`

 * *Files 0% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 <a href="https://nilomr.github.io/pykanto">
     <img src="https://raw.githubusercontent.com/nilomr/pykanto/2c1613a928c4f98ce982176e52ddadc23e043834/docs/custom/pykanto-logo-grey-04.svg?token=AOQJBIQLQ4VKUF4V7NFYLKTD3TWVG" alt="pykanto logo" title="pykanto" height="80" style="padding-bottom:1em !important;" />
 </a>
 
 <br>
 <br>
 
-![version](https://img.shields.io/badge/package_version-0.1.6-orange)
+![version](https://img.shields.io/badge/package_version-0.1.7-orange)
 ![PyPI status](https://img.shields.io/pypi/status/ansicolortags.svg)
 ![license](https://img.shields.io/github/license/mashape/apistatus.svg)
 ![Open Source Love](https://img.shields.io/badge/open%20source-♡-lightgrey)
 ![Python 3.8](https://img.shields.io/badge/python-3.8%20|%203.9%20|%203.10-blue.svg)
 
 **pykanto** is a python library to manage and analyse bird vocalisations
```

#### html2text {}

```diff
@@ -1,12 +1,12 @@
 
 
                                 [pykanto_logo]
 
- ![version](https://img.shields.io/badge/package_version-0.1.6-orange) ![PyPI
+ ![version](https://img.shields.io/badge/package_version-0.1.7-orange) ![PyPI
 status](https://img.shields.io/pypi/status/ansicolortags.svg) ![license](https:
   //img.shields.io/github/license/mashape/apistatus.svg) ![Open Source Love]
 (https://img.shields.io/badge/open%20source-â¡-lightgrey) ![Python 3.8](https:
 //img.shields.io/badge/python-3.8%20|%203.9%20|%203.10-blue.svg) **pykanto** is
    a python library to manage and analyse bird vocalisations [Installation]
 (#installation) â¢ [Getting started](#getting-started) â¢ [Acknowledgements]
                            (#acknowledgements) # ã¤
```

### Comparing `pykanto-0.1.6/pykanto/app/data.py` & `pykanto-0.1.7/pykanto/app/data.py`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/app/main.py` & `pykanto-0.1.7/pykanto/app/main.py`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/app/static/lasso.png` & `pykanto-0.1.7/pykanto/app/static/lasso.png`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/app/static/pykanto-logo.svg` & `pykanto-0.1.7/pykanto/app/static/pykanto-logo.svg`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/app/templates/index.html` & `pykanto-0.1.7/pykanto/app/templates/index.html`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/app/templates/styles.css` & `pykanto-0.1.7/pykanto/app/templates/styles.css`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/app/theme.yaml` & `pykanto-0.1.7/pykanto/app/theme.yaml`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/raw/AM/20210502_040000.WAV` & `pykanto-0.1.7/pykanto/data/raw/AM/20210502_040000.WAV`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/raw/AM/20210502_040000.xml` & `pykanto-0.1.7/pykanto/data/raw/AM/20210502_040000.xml`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/raw/BENGALESE_FINCH/bird_3/348.wav` & `pykanto-0.1.7/pykanto/data/raw/BENGALESE_FINCH/bird_3/348.wav`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/raw/BENGALESE_FINCH/bird_3/348.xml` & `pykanto-0.1.7/pykanto/data/raw/BENGALESE_FINCH/bird_3/348.xml`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/raw/BENGALESE_FINCH/bird_3/363.wav` & `pykanto-0.1.7/pykanto/data/raw/BENGALESE_FINCH/bird_3/363.wav`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/raw/BENGALESE_FINCH/bird_3/363.xml` & `pykanto-0.1.7/pykanto/data/raw/BENGALESE_FINCH/bird_3/363.xml`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/raw/STORM-PETREL/XC46092.wav` & `pykanto-0.1.7/pykanto/data/raw/STORM-PETREL/XC46092.wav`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/raw/STORM-PETREL/XC46092.xml` & `pykanto-0.1.7/pykanto/data/raw/STORM-PETREL/XC46092.xml`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/raw/STORM-PETREL/XC663885.wav` & `pykanto-0.1.7/pykanto/data/raw/STORM-PETREL/XC663885.wav`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/raw/STORM-PETREL/XC663885.xml` & `pykanto-0.1.7/pykanto/data/raw/STORM-PETREL/XC663885.xml`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-B32-0415_05-11.JSON` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-B32-0415_05-11.JSON`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-B32-0415_05-15.JSON` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-B32-0415_05-15.JSON`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-B32-0415_05-21.JSON` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-B32-0415_05-21.JSON`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-B32-0415_05-23.JSON` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-B32-0415_05-23.JSON`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-B32-0415_05-3.JSON` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-B32-0415_05-3.JSON`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-B32-0415_05-6.JSON` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-B32-0415_05-6.JSON`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-B32-0415_05-9.JSON` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-B32-0415_05-9.JSON`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-B32-0416_04-21.JSON` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-B32-0416_04-21.JSON`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-B32-0416_04-23.JSON` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-B32-0416_04-23.JSON`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-B32-0416_04-24.JSON` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-B32-0416_04-24.JSON`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-B32-0416_05-20.JSON` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-B32-0416_05-20.JSON`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-77.JSON` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-77.JSON`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-78.JSON` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-78.JSON`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-79.JSON` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-79.JSON`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-80.JSON` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-80.JSON`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-81.JSON` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-81.JSON`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-86.JSON` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-86.JSON`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-88.JSON` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-88.JSON`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-91.JSON` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-91.JSON`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-92.JSON` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/JSON/2021-SW83-0418_04-92.JSON`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-B32-0415_05-11.wav` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-B32-0415_05-11.wav`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-B32-0415_05-15.wav` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-B32-0415_05-15.wav`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-B32-0415_05-21.wav` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-B32-0415_05-21.wav`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-B32-0415_05-23.wav` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-B32-0415_05-23.wav`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-B32-0415_05-3.wav` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-B32-0415_05-3.wav`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-B32-0415_05-6.wav` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-B32-0415_05-6.wav`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-B32-0415_05-9.wav` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-B32-0415_05-9.wav`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-B32-0416_04-21.wav` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-B32-0416_04-21.wav`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-B32-0416_04-23.wav` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-B32-0416_04-23.wav`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-B32-0416_04-24.wav` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-B32-0416_04-24.wav`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-B32-0416_05-20.wav` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-B32-0416_05-20.wav`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-77.wav` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-77.wav`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-78.wav` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-78.wav`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-79.wav` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-79.wav`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-80.wav` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-80.wav`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-81.wav` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-81.wav`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-86.wav` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-86.wav`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-88.wav` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-88.wav`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-91.wav` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-91.wav`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-92.wav` & `pykanto-0.1.7/pykanto/data/segmented/great_tit/WAV/2021-SW83-0418_04-92.wav`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC46092_0.gzip` & `pykanto-0.1.7/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC46092_53600.gzip`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC46092_1.gzip` & `pykanto-0.1.7/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC46092_128832.gzip`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC46092_2.gzip` & `pykanto-0.1.7/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC46092_202272.gzip`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC46092_3.gzip` & `pykanto-0.1.7/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC46092_278432.gzip`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC46092_4.gzip` & `pykanto-0.1.7/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC46092_350224.gzip`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC46092_5.gzip` & `pykanto-0.1.7/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC46092_492096.gzip`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC663885_0.gzip` & `pykanto-0.1.7/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC663885_26280.gzip`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC663885_1.gzip` & `pykanto-0.1.7/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC663885_91784.gzip`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC663885_2.gzip` & `pykanto-0.1.7/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC663885_219072.gzip`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC663885_3.gzip` & `pykanto-0.1.7/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC663885_350592.gzip`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC663885_4.gzip` & `pykanto-0.1.7/pykanto/data/segmented/storm-petrel/GZIP/SegSyllsOutput_STORM-PETREL_XC663885_481896.gzip`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/dataset.py` & `pykanto-0.1.7/pykanto/dataset.py`

 * *Files 2% similar despite different names*

```diff
@@ -12,15 +12,15 @@
 import inspect
 import pickle
 import subprocess
 import warnings
 from datetime import datetime
 from pathlib import Path
 from random import sample
-from typing import List, Literal, Tuple
+from typing import Any, Dict, List, Literal, Tuple
 
 import numpy as np
 import pandas as pd
 from bokeh.palettes import Set3_12
 
 import pykanto.plot as kplot
 from pykanto.app.data import prepare_datasource_parallel
@@ -745,32 +745,42 @@
     def write_to_json(self) -> None:
         """
         Write the dataset to the existing JSON files for each vocalisation.
         """
         save_to_jsons(self)
 
     @timing
-    def cluster_ids(self, min_sample: int = 10) -> None:
+    def cluster_ids(
+        self,
+        min_sample: int = 10,
+        kwargs_umap: Dict[str, Any] = {},
+        kwargs_hdbscan: Dict[str, Any] = {},
+    ) -> None:
         """
         Dimensionality reduction using UMAP + unsupervised clustering using
         HDBSCAN. This will fail if the sample size for an ID (grouping factor,
         such as individual or population) is too small.
 
         Adds cluster membership information and 2D UMAP coordinates to
         :attr:`~.KantoData.data` if `song_level=True`
         in :attr:`~.KantoData.parameters`, else to :attr:`~.KantoData.units`.
 
         Args:
             min_sample (int): Minimum sample size below which an ID will
                 be skipped. Defaults to 10, but you can reallistically expect
                 good automatic results above ~100.
-
+            kwargs_umap (dict): Dictionary of UMAP parameters.
+            kwargs_hdbscan (dict): Dictionary of HDBSCAN+ parameters.
         """
         df = reduce_and_cluster_parallel(
-            self, min_sample=min_sample, num_cpus=self.parameters.num_cpus
+            self,
+            min_sample=min_sample,
+            num_cpus=self.parameters.num_cpus,
+            kwargs_umap=kwargs_umap,
+            kwargs_hdbscan=kwargs_hdbscan,
         )
 
         if self.parameters.song_level:
             self.data = self.data.combine_first(df)
         else:
             self.units = df
             # TODO #14@nilomr: Add individual element information to self.data?
```

### Comparing `pykanto-0.1.6/pykanto/parameters.py` & `pykanto-0.1.7/pykanto/parameters.py`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/plot.py` & `pykanto-0.1.7/pykanto/plot.py`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/signal/analysis.py` & `pykanto-0.1.7/pykanto/signal/analysis.py`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/signal/cluster.py` & `pykanto-0.1.7/pykanto/signal/cluster.py`

 * *Files 22% similar despite different names*

```diff
@@ -6,32 +6,33 @@
 
 from __future__ import annotations
 
 import itertools
 import pickle
 import warnings
 from logging import warn
-from typing import TYPE_CHECKING, List, Tuple
+from typing import TYPE_CHECKING, Any, Dict, List, Tuple
 
 import numpy as np
 import pandas as pd
 import psutil
 import ray
 import umap
 from hdbscan import HDBSCAN
+from umap import UMAP
+
 from pykanto.signal.spectrogram import pad_spectrogram
 from pykanto.utils.compute import (
     calc_chunks,
     flatten_list,
     get_chunks,
     print_parallel_info,
     to_iterator,
     with_pbar,
 )
-from umap import UMAP
 
 if TYPE_CHECKING:
     from pykanto.dataset import KantoData
 try:
     from cuml import UMAP as cumlUMAP
 except:
     warnings.warn(
@@ -48,106 +49,109 @@
 
 
 def umap_reduce(
     data: np.ndarray,
     n_neighbors: int = 15,
     n_components: int = 2,
     min_dist: float = 0.1,
+    random_state: int | None = None,
     verbose: bool = False,
-    **kwargs,
+    **kwargs_umap,
 ) -> Tuple[np.ndarray, umap.UMAP]:
     """
     Uniform Manifold Approximation and Projection.
     Uses either the cuml GPU-accelerated version or the 'regular' umap version.
     See the documentation of either for valid kwargs.
 
     Args:
         data (array-like, shape = (n_samples, n_features)): Data to reduce.
-        n_neighbors (int, optional): [description]. Defaults to 15.
-        n_components (int, optional): [description]. Defaults to 2.
-        min_dist (float, optional): [description]. Defaults to 0.1.
-        kwargs: Passed to umap.UMAP or cuml.umap.UMAP.
+        n_neighbors (int, optional): See UMAP docs. Defaults to 15.
+        n_components (int, optional): See UMAP docs. Defaults to 2.
+        min_dist (float, optional): See UMAP docs. Defaults to 0.1.
+        random_state (int, optional): See UMAP docs. Defaults to None.
+        kwargs_umap: extra named arguments passed to umap.UMAP or cuml.umap.UMAP.
 
     Returns:
         Tuple[np.ndarray, umap.UMAP]: Embedding coordinates
         and UMAP reducer.
     """
+    kwargs_umap.setdefault("n_neighbors", n_neighbors)
+    kwargs_umap.setdefault("n_components", n_components)
+    kwargs_umap.setdefault("min_dist", min_dist)
+    kwargs_umap.setdefault("random_state", random_state)
     if _has_cuml:
-        reducer = cumlUMAP(
-            n_neighbors=n_neighbors,
-            n_components=n_components,
-            min_dist=min_dist,
-            **kwargs,
-        )
+        reducer = cumlUMAP(**kwargs_umap)
         embedding = reducer.fit_transform(data)
     else:
         if verbose:
             warnings.warn(
                 "The cuML library is not not available: defaulting to "
                 "slower CPU UMAP implementation."
             )
-        reducer = UMAP(
-            n_neighbors=n_neighbors,
-            n_components=n_components,
-            min_dist=min_dist,
-            **kwargs,
-        )
+        reducer = UMAP(**kwargs_umap)
         embedding = reducer.fit_transform(data)
     return embedding, reducer
 
 
 def hdbscan_cluster(
     embedding: np.ndarray,
     min_cluster_size: int = 5,
     min_samples: None | int = None,
-    **kwargs,
+    **kwargs_hdbscan,
 ) -> HDBSCAN:
     """
     Perform HDBSCAN clustering from vector array or distance matrix.
     Convenience wrapper. See the
     `HDBSCAN* docs <https://hdbscan.readthedocs.io/en/latest/parameter_selection.html>`_.
 
     Args:
         embedding (np.ndarray): Data to cluster. See hdbscan documentation
             for more.
         min_cluster_size (int, optional): Minimum number of samples to
             consider a cluster. Defaults to 5.
         min_samples (int, optional): Controls how 'conservative' clustering is.
             Larger values = more points will be declared as noise.
             Defaults to None.
-        kwargs: Passed to HDBSCAN.
+        kwargs_hdbscan: Extra named arguments passed to HDBSCAN.
 
     Returns:
         HDBSCAN: HDBSCAN object. Labels are at `self.labels_`.
     """
+    min_cluster_size = kwargs_hdbscan.setdefault(
+        "min_cluster_size", min_cluster_size
+    )
+    kwargs_hdbscan.setdefault("min_samples", min_samples)
+    kwargs_hdbscan.setdefault("cluster_selection_method", "eom")
     if min_cluster_size < 2:
         warnings.warn("`min_cluster_size` too small, setting it to 2")
-        min_cluster_size = 2
-    clusterer = HDBSCAN(
-        min_cluster_size=min_cluster_size,
-        min_samples=min_samples,
-        cluster_selection_method="eom",
-        **kwargs,
-    )
+        kwargs_hdbscan["min_cluster_size"] = 2
+    clusterer = HDBSCAN(**kwargs_hdbscan)
     clusterer.fit(embedding)
     return clusterer
 
 
 def reduce_and_cluster(
-    dataset: KantoData, ID: str, song_level: bool = False, min_sample: int = 10
+    dataset: KantoData,
+    ID: str,
+    song_level: bool = False,
+    min_sample: int = 10,
+    kwargs_umap: Dict[str, Any] = {},
+    kwargs_hdbscan: Dict[str, Any] = {},
 ) -> pd.DataFrame | None:
     # TODO: pass UMAP and HDBSCAN params!
     """
     Args:
         dataset (KantoData): Data to be used.
         ID (str): Grouping factor.
         song_level (bool, optional): Whether to use the average of all units in
             each vocalisation instead of all units. Defaults to False.
         min_sample (int, optional): Minimum number of vocalisations or units.
             Defaults to 10.
+        kwargs_umap (dict): dictionary of UMAP parameters.
+        kwargs_hdbscan (dict): dictionary of HDBSCAN+ parameters.
 
     Returns:
         pd.DataFrame | None: Dataframe with columns ['vocalisation_key', 'ID',
             'idx', 'umap_x', 'umap_y', 'auto_class'] or None if sample size
             is too small
     """
 
@@ -204,23 +208,18 @@
             )
         )
         flat_units = np.array(
             [unit.flatten() for ls in units.values() for unit in ls]
         )
 
     # Run UMAP
-    embedding, _ = umap_reduce(
-        flat_units, n_neighbors=25, min_dist=0.2, n_components=2
-    )
+    embedding, _ = umap_reduce(flat_units, **kwargs_umap)
 
     # Cluster using HDBSCAN
-    # smallest cluster size allowed
-    clusterer = hdbscan_cluster(
-        embedding, min_cluster_size=int(len(flat_units) * 0.02), min_samples=10
-    )
+    clusterer = hdbscan_cluster(embedding, **kwargs_hdbscan)
 
     # Put together in a dataframe
     cluster_df = pd.DataFrame(units_keys, columns=["index"])
     cluster_df.set_index("index", inplace=True)
     if song_level is False:
         cluster_df["vocalisation_key"] = unitkeys
         cluster_df["ID"] = ID
@@ -230,15 +229,19 @@
     cluster_df["auto_class"] = list(clusterer.labels_)
     cluster_df["auto_class"] = cluster_df["auto_class"].astype(str)
 
     return cluster_df
 
 
 def reduce_and_cluster_parallel(
-    dataset: KantoData, min_sample: int = 10, num_cpus: float | None = None
+    dataset: KantoData,
+    kwargs_umap: dict = {},
+    kwargs_hdbscan: dict = {},
+    min_sample: int = 10,
+    num_cpus: float | None = None,
 ) -> pd.DataFrame | None:
     """
     Parallel implementation of
     :func:`~pykanto.signal.cluster.reduce_and_cluster`.
     """
     song_level = dataset.parameters.song_level
     IDS = set(dataset.files["ID"])
@@ -265,25 +268,37 @@
         num_cpus=num_cpus, num_gpus=1 / psutil.cpu_count() if _has_cuml else 0
     )  # type: ignore
     def _reduce_and_cluster_r(
         dataset: KantoData,
         IDS: List[str],
         song_level: bool = False,
         min_sample: int = 10,
+        kwargs_umap=kwargs_umap,
+        kwargs_hdbscan=kwargs_hdbscan,
     ) -> List[pd.DataFrame | None]:
         return [
             reduce_and_cluster(
-                dataset, ID, song_level=song_level, min_sample=min_sample
+                dataset,
+                ID,
+                song_level=song_level,
+                min_sample=min_sample,
+                kwargs_umap=kwargs_umap,
+                kwargs_hdbscan=kwargs_hdbscan,
             )
             for ID in IDS
         ]
 
     obj_ids = [
         _reduce_and_cluster_r.remote(
-            dataset_ref, i, song_level=song_level, min_sample=min_sample
+            dataset_ref,
+            i,
+            song_level=song_level,
+            min_sample=min_sample,
+            kwargs_umap=kwargs_umap,
+            kwargs_hdbscan=kwargs_hdbscan,
         )
         for i in chunks
     ]
     pbar = {
         "desc": "Projecting and clustering vocalisations",
         "total": n_chunks,
     }
```

### Comparing `pykanto-0.1.6/pykanto/signal/filter.py` & `pykanto-0.1.7/pykanto/signal/filter.py`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/signal/segment.py` & `pykanto-0.1.7/pykanto/signal/segment.py`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/signal/spectrogram.py` & `pykanto-0.1.7/pykanto/signal/spectrogram.py`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/utils/compute.py` & `pykanto-0.1.7/pykanto/utils/compute.py`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/utils/custom.py` & `pykanto-0.1.7/pykanto/utils/custom.py`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/utils/io.py` & `pykanto-0.1.7/pykanto/utils/io.py`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/utils/paths.py` & `pykanto-0.1.7/pykanto/utils/paths.py`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/utils/slurm/LICENSE` & `pykanto-0.1.7/pykanto/utils/slurm/LICENSE`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/utils/slurm/launch.py` & `pykanto-0.1.7/pykanto/utils/slurm/launch.py`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/utils/slurm/sbatch_template.sh` & `pykanto-0.1.7/pykanto/utils/slurm/sbatch_template.sh`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/utils/slurm/tester.py` & `pykanto-0.1.7/pykanto/utils/slurm/tester.py`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pykanto/utils/types.py` & `pykanto-0.1.7/pykanto/utils/types.py`

 * *Files identical despite different names*

### Comparing `pykanto-0.1.6/pyproject.toml` & `pykanto-0.1.7/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 [build-system]
 requires = ["flit_core >=3.2,<4"]
 build-backend = "flit_core.buildapi"
 
 [project]
 name = "pykanto"
 description = "A library for managing and analysing animal vocalisation data."
-version = "0.1.6"
+version = "0.1.7"
 authors = [{ name = "Nilo M. Recalde", email = "nilomerinorecalde@gmail.com" }]
 classifiers = [
     'License :: OSI Approved :: MIT License',
     'Development Status :: 4 - Beta',
     'Programming Language :: Python :: 3.8',
     'Programming Language :: Python :: 3.9',
     'Programming Language :: Python :: 3.10',
```

### Comparing `pykanto-0.1.6/PKG-INFO` & `pykanto-0.1.7/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pykanto
-Version: 0.1.6
+Version: 0.1.7
 Summary: A library for managing and analysing animal vocalisation data.
 Author-email: "Nilo M. Recalde" <nilomerinorecalde@gmail.com>
 Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Development Status :: 4 - Beta
 Classifier: Programming Language :: Python :: 3.8
@@ -55,15 +55,15 @@
 <a href="https://nilomr.github.io/pykanto">
     <img src="https://raw.githubusercontent.com/nilomr/pykanto/2c1613a928c4f98ce982176e52ddadc23e043834/docs/custom/pykanto-logo-grey-04.svg?token=AOQJBIQLQ4VKUF4V7NFYLKTD3TWVG" alt="pykanto logo" title="pykanto" height="80" style="padding-bottom:1em !important;" />
 </a>
 
 <br>
 <br>
 
-![version](https://img.shields.io/badge/package_version-0.1.6-orange)
+![version](https://img.shields.io/badge/package_version-0.1.7-orange)
 ![PyPI status](https://img.shields.io/pypi/status/ansicolortags.svg)
 ![license](https://img.shields.io/github/license/mashape/apistatus.svg)
 ![Open Source Love](https://img.shields.io/badge/open%20source-♡-lightgrey)
 ![Python 3.8](https://img.shields.io/badge/python-3.8%20|%203.9%20|%203.10-blue.svg)
 
 **pykanto** is a python library to manage and analyse bird vocalisations
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: pykanto Version: 0.1.6 Summary: A library for
+Metadata-Version: 2.1 Name: pykanto Version: 0.1.7 Summary: A library for
 managing and analysing animal vocalisation data. Author-email: "Nilo M.
 Recalde"
 gmail.com> Requires-Python: >=3.8 Description-Content-Type: text/markdown
 Classifier: License :: OSI Approved :: MIT License Classifier: Development
 Status :: 4 - Beta Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9 Classifier: Programming
 Language :: Python :: 3.10 Requires-Dist: pandas >= 1 Requires-Dist: numpy >=
@@ -22,15 +22,15 @@
 parser == 0.18 ; extra == "doc" Requires-Dist: pytest >=7 ; extra == "test"
 Project-URL: Documentation, https://nilomr.github.io/pykanto Project-URL:
 Source, https://github.com/nilomr/pykanto Provides-Extra: dev Provides-Extra:
 doc Provides-Extra: test
 
                                 [pykanto_logo]
 
- ![version](https://img.shields.io/badge/package_version-0.1.6-orange) ![PyPI
+ ![version](https://img.shields.io/badge/package_version-0.1.7-orange) ![PyPI
 status](https://img.shields.io/pypi/status/ansicolortags.svg) ![license](https:
   //img.shields.io/github/license/mashape/apistatus.svg) ![Open Source Love]
 (https://img.shields.io/badge/open%20source-â¡-lightgrey) ![Python 3.8](https:
 //img.shields.io/badge/python-3.8%20|%203.9%20|%203.10-blue.svg) **pykanto** is
    a python library to manage and analyse bird vocalisations [Installation]
 (#installation) â¢ [Getting started](#getting-started) â¢ [Acknowledgements]
                            (#acknowledgements) # ã¤
```

