# Comparing `tmp/imat-3.1.tar.gz` & `tmp/imat-3.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "imat-3.1.tar", last modified: Sat Jul 22 04:18:47 2023, max compression
+gzip compressed data, was "imat-3.2.0.tar", last modified: Sun Jul 23 16:52:52 2023, max compression
```

## Comparing `imat-3.1.tar` & `imat-3.2.0.tar`

### file list

```diff
@@ -1,64 +1,64 @@
-drwxrwxrwx   0        0        0        0 2023-07-22 04:18:47.060763 imat-3.1/
--rw-rw-rw-   0        0        0     1096 2023-07-17 17:26:37.000000 imat-3.1/LICENSE.txt
--rw-rw-rw-   0        0        0    12064 2023-07-22 04:18:47.055776 imat-3.1/PKG-INFO
--rw-rw-rw-   0        0        0    10845 2023-07-17 19:39:46.000000 imat-3.1/README.md
-drwxrwxrwx   0        0        0        0 2023-07-22 04:18:46.679263 imat-3.1/iMaT/
--rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.1/iMaT/__init__.py
--rw-rw-rw-   0        0        0     2430 2023-07-17 17:26:37.000000 imat-3.1/iMaT/__main__.py
-drwxrwxrwx   0        0        0        0 2023-07-22 04:18:46.684250 imat-3.1/iMaT/src/
--rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-22 04:18:46.704197 imat-3.1/iMaT/src/analysis/
--rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/analysis/__init__.py
--rw-rw-rw-   0        0        0    58077 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/analysis/functions.py
--rw-rw-rw-   0        0        0     5213 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/analysis/main.py
--rw-rw-rw-   0        0        0     3572 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/analysis/utils.py
-drwxrwxrwx   0        0        0        0 2023-07-22 04:18:46.732123 imat-3.1/iMaT/src/cli/
--rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/cli/__init__.py
--rw-rw-rw-   0        0        0    31663 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/cli/menu_constructors.py
--rw-rw-rw-   0        0        0    23891 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/cli/menu_entries.py
--rw-rw-rw-   0        0        0     7930 2023-07-22 04:18:10.000000 imat-3.1/iMaT/src/constants.py
-drwxrwxrwx   0        0        0        0 2023-07-22 04:18:46.746086 imat-3.1/iMaT/src/conversion/
--rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/conversion/__init__.py
--rw-rw-rw-   0        0        0     5090 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/conversion/main.py
--rw-rw-rw-   0        0        0    12992 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/conversion/utils.py
-drwxrwxrwx   0        0        0        0 2023-07-22 04:18:46.753067 imat-3.1/iMaT/src/m21_environment/
--rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/m21_environment/__init__.py
--rw-rw-rw-   0        0        0    10243 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/m21_environment/main.py
-drwxrwxrwx   0        0        0        0 2023-07-22 04:18:46.797946 imat-3.1/iMaT/src/pattern_search/
--rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/pattern_search/__init__.py
--rw-rw-rw-   0        0        0    15880 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/pattern_search/functions.py
--rw-rw-rw-   0        0        0    10903 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/pattern_search/main.py
--rw-rw-rw-   0        0        0    10307 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/pattern_search/utils.py
-drwxrwxrwx   0        0        0        0 2023-07-22 04:18:46.848326 imat-3.1/iMaT/src/score_selection/
--rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/score_selection/__init__.py
--rw-rw-rw-   0        0        0    17704 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/score_selection/main.py
--rw-rw-rw-   0        0        0    14028 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/score_selection/name_parts.py
--rw-rw-rw-   0        0        0    12218 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/score_selection/select_parts_and_measures.py
-drwxrwxrwx   0        0        0        0 2023-07-22 04:18:46.897197 imat-3.1/iMaT/src/tokenization/
--rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/tokenization/__init__.py
--rw-rw-rw-   0        0        0    19526 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/tokenization/main.py
-drwxrwxrwx   0        0        0        0 2023-07-22 04:18:46.917150 imat-3.1/iMaT/src/tokenization/refine_results/
--rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/tokenization/refine_results/__init__.py
--rw-rw-rw-   0        0        0     6837 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/tokenization/refine_results/absolute_duration.py
--rw-rw-rw-   0        0        0     7020 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/tokenization/refine_results/calculate_pitch_intervals.py
--rw-rw-rw-   0        0        0     4966 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/tokenization/refine_results/remove_prefixes.py
--rw-rw-rw-   0        0        0     5447 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/tokenization/refine_results/tokens_to_txt.py
--rw-rw-rw-   0        0        0    15349 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/tokenization/utils.py
-drwxrwxrwx   0        0        0        0 2023-07-22 04:18:46.963021 imat-3.1/iMaT/src/utils/
--rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/utils/__init__.py
--rw-rw-rw-   0        0        0     3982 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/utils/error_handling.py
--rw-rw-rw-   0        0        0     6787 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/utils/misc.py
-drwxrwxrwx   0        0        0        0 2023-07-22 04:18:46.999921 imat-3.1/iMaT/src/visualizations/
--rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/visualizations/__init__.py
--rw-rw-rw-   0        0        0    19214 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/visualizations/analysis_results_graphs.py
--rw-rw-rw-   0        0        0    10926 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/visualizations/m21_integrated.py
--rw-rw-rw-   0        0        0     3263 2023-07-17 17:26:37.000000 imat-3.1/iMaT/src/visualizations/main.py
-drwxrwxrwx   0        0        0        0 2023-07-22 04:18:47.045807 imat-3.1/imat.egg-info/
--rw-rw-rw-   0        0        0    12064 2023-07-22 04:18:44.000000 imat-3.1/imat.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0     1561 2023-07-22 04:18:44.000000 imat-3.1/imat.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-22 04:18:44.000000 imat-3.1/imat.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       44 2023-07-22 04:18:44.000000 imat-3.1/imat.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0      266 2023-07-22 04:18:44.000000 imat-3.1/imat.egg-info/requires.txt
--rw-rw-rw-   0        0        0        5 2023-07-22 04:18:44.000000 imat-3.1/imat.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-22 04:18:47.061756 imat-3.1/setup.cfg
--rw-rw-rw-   0        0        0     2079 2023-07-22 04:18:10.000000 imat-3.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:52:52.332370 imat-3.2.0/
+-rw-rw-rw-   0        0        0     1096 2023-07-17 17:26:37.000000 imat-3.2.0/LICENSE.txt
+-rw-rw-rw-   0        0        0    15080 2023-07-23 16:52:52.322399 imat-3.2.0/PKG-INFO
+-rw-rw-rw-   0        0        0    13871 2023-07-23 06:01:28.000000 imat-3.2.0/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 16:52:51.954384 imat-3.2.0/iMaT/
+-rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/__init__.py
+-rw-rw-rw-   0        0        0     2430 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/__main__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:52:51.959369 imat-3.2.0/iMaT/src/
+-rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:52:52.003251 imat-3.2.0/iMaT/src/analysis/
+-rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/analysis/__init__.py
+-rw-rw-rw-   0        0        0    58077 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/analysis/functions.py
+-rw-rw-rw-   0        0        0     5213 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/analysis/main.py
+-rw-rw-rw-   0        0        0     3630 2023-07-23 16:40:24.000000 imat-3.2.0/iMaT/src/analysis/utils.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:52:52.028195 imat-3.2.0/iMaT/src/cli/
+-rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/cli/__init__.py
+-rw-rw-rw-   0        0        0    31663 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/cli/menu_constructors.py
+-rw-rw-rw-   0        0        0    23891 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/cli/menu_entries.py
+-rw-rw-rw-   0        0        0     7837 2023-07-23 16:47:26.000000 imat-3.2.0/iMaT/src/constants.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:52:52.038158 imat-3.2.0/iMaT/src/conversion/
+-rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/conversion/__init__.py
+-rw-rw-rw-   0        0        0     5090 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/conversion/main.py
+-rw-rw-rw-   0        0        0    12992 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/conversion/utils.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:52:52.050126 imat-3.2.0/iMaT/src/m21_environment/
+-rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/m21_environment/__init__.py
+-rw-rw-rw-   0        0        0    10243 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/m21_environment/main.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:52:52.083038 imat-3.2.0/iMaT/src/pattern_search/
+-rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/pattern_search/__init__.py
+-rw-rw-rw-   0        0        0    15880 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/pattern_search/functions.py
+-rw-rw-rw-   0        0        0    10903 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/pattern_search/main.py
+-rw-rw-rw-   0        0        0    10307 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/pattern_search/utils.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:52:52.098996 imat-3.2.0/iMaT/src/score_selection/
+-rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/score_selection/__init__.py
+-rw-rw-rw-   0        0        0    17704 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/score_selection/main.py
+-rw-rw-rw-   0        0        0    14028 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/score_selection/name_parts.py
+-rw-rw-rw-   0        0        0    12218 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/score_selection/select_parts_and_measures.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:52:52.131918 imat-3.2.0/iMaT/src/tokenization/
+-rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/tokenization/__init__.py
+-rw-rw-rw-   0        0        0    19526 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/tokenization/main.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:52:52.197731 imat-3.2.0/iMaT/src/tokenization/refine_results/
+-rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/tokenization/refine_results/__init__.py
+-rw-rw-rw-   0        0        0     6837 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/tokenization/refine_results/absolute_duration.py
+-rw-rw-rw-   0        0        0     7020 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/tokenization/refine_results/calculate_pitch_intervals.py
+-rw-rw-rw-   0        0        0     4966 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/tokenization/refine_results/remove_prefixes.py
+-rw-rw-rw-   0        0        0     5447 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/tokenization/refine_results/tokens_to_txt.py
+-rw-rw-rw-   0        0        0    15349 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/tokenization/utils.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:52:52.219674 imat-3.2.0/iMaT/src/utils/
+-rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/utils/__init__.py
+-rw-rw-rw-   0        0        0     3982 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/utils/error_handling.py
+-rw-rw-rw-   0        0        0     6787 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/utils/misc.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:52:52.268541 imat-3.2.0/iMaT/src/visualizations/
+-rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/visualizations/__init__.py
+-rw-rw-rw-   0        0        0    19214 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/visualizations/analysis_results_graphs.py
+-rw-rw-rw-   0        0        0    10926 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/visualizations/m21_integrated.py
+-rw-rw-rw-   0        0        0     3263 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/visualizations/main.py
+drwxrwxrwx   0        0        0        0 2023-07-23 16:52:52.319405 imat-3.2.0/imat.egg-info/
+-rw-rw-rw-   0        0        0    15080 2023-07-23 16:52:50.000000 imat-3.2.0/imat.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0     1561 2023-07-23 16:52:50.000000 imat-3.2.0/imat.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 16:52:50.000000 imat-3.2.0/imat.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       44 2023-07-23 16:52:50.000000 imat-3.2.0/imat.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0      272 2023-07-23 16:52:50.000000 imat-3.2.0/imat.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        5 2023-07-23 16:52:50.000000 imat-3.2.0/imat.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 16:52:52.334368 imat-3.2.0/setup.cfg
+-rw-rw-rw-   0        0        0     2105 2023-07-23 16:52:45.000000 imat-3.2.0/setup.py
```

### Comparing `imat-3.1/LICENSE.txt` & `imat-3.2.0/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `imat-3.1/PKG-INFO` & `imat-3.2.0/README.md`

 * *Files 15% similar despite different names*

```diff
@@ -1,62 +1,64 @@
-Metadata-Version: 2.1
-Name: imat
-Version: 3.1
-Summary: Interactive Music Analysis Tool (I-MaT)
-Home-page: https://github.com/sebastian-eck/I-MaT
-Author: Sebastian Oliver Eck
-License: MIT License
-Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.8
-Classifier: Programming Language :: Python :: 3.9
-Classifier: Programming Language :: Python :: 3.10
-Classifier: License :: OSI Approved :: MIT License
-Classifier: Operating System :: Microsoft :: Windows
-Classifier: Operating System :: Unix
-Classifier: Development Status :: 4 - Beta
-Classifier: Environment :: Console
-Classifier: Framework :: Matplotlib
-Classifier: Intended Audience :: Education
-Classifier: Intended Audience :: Science/Research
-Classifier: Natural Language :: English
-Classifier: Topic :: Documentation :: Sphinx
-Classifier: Topic :: Education
-Classifier: Topic :: Education :: Computer Aided Instruction (CAI)
-Classifier: Topic :: Multimedia :: Sound/Audio :: Analysis
-Classifier: Topic :: Multimedia :: Sound/Audio :: MIDI
-Classifier: Topic :: Text Processing :: Linguistic
-Description-Content-Type: text/markdown
-Provides-Extra: doc
-License-File: LICENSE.txt
+# The Interactive Music Analysis Tool (I-MaT)
 
-# An Introduction: The Interactive Music Analysis Tool (I-MaT)
+I-MaT is an innovative tool designed to facilitate in-depth musical analysis through an easy-to-use interface. I-MaT offers a comprehensive set of functionalities allowing for the examination of musical pieces from a wide range of perspectives. The documentation (available on [readthedocs.io](https://i-mat.readthedocs.io/en/latest/)) serves as a comprehensive guide, aiming to provide you with insights into I-MaT's functionalities and its modular concept, and assist both first-time users and experienced researchers in using the tool effectively.
 
-The **Interactive Music Analysis Tool (I-MaT)**[^1] is a modular program designed for producing visualizations and statistical analyses of sheet music files. It is based on the **music21** python library ([GitHub repository](https://github.com/cuthbertLab/music21.git)), developed by the Massachusetts Institute of Technology (MIT),[^2] and was originally created as a subproject of the fellowship project Computer-assisted Music Analysis in Digital University Teaching ([ComputergestÃ¼tzte Musikanalyse in der digitalen Hochschullehre, 2021, project report (PDF)](https://stifterverband.org/file/10986/download?token=tl9S2EL_)).[^3]
+The sections contained within the documentation provide detailed information on how to use the Interactive Music Analysis Tool, from [downloading and the installation](https://i-mat.readthedocs.io/en/latest/getting_started.html), to [contribution and code extension](https://i-mat.readthedocs.io/en/latest/contribute.html), to its application in music analysis. Furthermore, you will find a detailed descriptions of I-MaT's [source code](https://i-mat.readthedocs.io/en/latest/module_files/src.html), explaining the different packages' and modules' content that make up the tool.
 
-The project was located at the Department of Musicology Weimar-Jena at the Franz Liszt University of Music Weimar[^4] and was funded by the Thuringian Ministry for Economy, Science and Digital Change and the Deutscher Stifterverband.[^5]
+Through this documentation, I hope to provide you with the necessary knowledge to navigate I-MaT, explore its features, and conduct your own analyses by using my tool!
 
-A comprehensive documentation is available on: https://i-mat.readthedocs.io/en/latest/
+Start by installing the Interactive Music Analysis Tool (I-MaT):
+
+    pip install imat
+
+To run the tool, simply type the following command into your shell:
+
+    imat
+
+If that was too fast, don't worry.
+You can find a detailed User Guide for how to install and start I-MaT in the [Getting Started with I-MaT](https://i-mat.readthedocs.io/en/latest/getting_started.html) section.
+
+Please enjoy and let me know if you have any questions or suggestions on how to further improve I-MaT's functionalities!
+
+Contact: imat.inquiries@gmail.com
+
+# An Introduction to I-MaT
+
+The Interactive Music Analysis Tool, I-MaT, (University of Music Franz Liszt Weimar, 2021a) is a modular program designed for producing visualizations, statistical analyses as well as tokenizations of textual music data. Its functionalities are built on various commonly used python libraries, such as music21 (Cuthbert, 2023a) and MidiTok (Fradet et al., 2021). I-MaT was developed as a sub-project within the fellowship project Computer-Assisted Music Analysis in Digital University Teaching (Pfleiderer, 2022; University of Music Franz Liszt Weimar, 2021c).
+
+The fellowship project (2021) was located at the Institute for Musicology Weimar-Jena at the Franz Liszt University of Music Weimar, Germany.
 
 ## Project Overview
 
-The aim of the aforementioned project was to design, test, teach with and evaluate a comprehensive set of teaching modules for music analysis that make use of various computer-assisted, primarily quantitative analysis tools. The teaching modules were intended to complement conventional musicological and analysis courses and mainly focus on:
+The aim of the fellowship project “Computer-Assisted Music Analysis […]” was to design, test, teach with and evaluate a comprehensive set of teaching modules for music analysis that make use of various computer-assisted, primarily quantitative analysis tools. The teaching modules were intended to complement conventional musicological and analysis courses and mainly focus on:
 
-- "the computer-based annotation and visualization of sheet music texts and audio files,
+- “the computer-based annotation and visualization of sheet music texts and audio files,
 - the statistical analysis of music corpora,
 - the search for musical patterns (rhythms, melodies, harmony connections, etc.),
-- and the comparison of interpretation"[^6]
+- and the comparison of interpretation” (Poliakov and Nadar, 2021a)
 
-Within the project "Computer-assisted Music Analysis [...]", three computerized approaches to music score analysis were utilized, namely music21,[^7] CAMAT,[^8] and I-MaT itself. Music21 is a Python library developed at MIT for symbolic music representation and processing. CAMAT ([GitHub repository](https://github.com/Christon-Ragavan/CAMAT)), on the other hand, is a Computer-Assisted Music Analysis Toolkit developed by Egor Poliakov[^9] and Christon R. Nadar[^10] within the fellowship project. CAMAT uses its own unique data structure, developed within the project to overcome certain design problems found within the music21 framework.[^11] Tutorials for musicological courses were prepared using music examples and code that can be executed as Jupyter Notebooks.[^12]
+Within the project Computer-Assisted Music Analysis in Digital University Teaching, three computerized approaches to music score analysis were utilized, namely music21,  CAMAT,  and I-MaT (University of Music Franz Liszt Weimar, 2021d).
 
-Both music21 and CAMAT require rudimentary knowledge of Python command syntax. In contrast, the Interactive Music Analysis Tool (I-MaT) is designed for users who have none to only limited knowledge of computer commands or programming languages as it utilizes a new and innovative approach to access and work with the music21 toolkit.
+Music21 is a Python library created at the Massachusetts Institute of Technology (MIT), Cambridge for symbolic music representation and processing (Cuthbert, 2023b). CAMAT, on the other hand, is a Computer-Assisted Music Analysis Toolkit developed within the course of the fellowship project (Poliakov and Nadar, 2021b; Pfleiderer et al., 2023). CAMAT uses its own unique data structure to overcome certain design problems found within the music21 framework (Poliakov and Nadar, 2021a). Tutorials for musicological university level courses were prepared and their usability evaluated; the tutorials include music examples and code that can be executed as Jupyter Notebooks (University of Music Franz Liszt Weimar, 2021b).
 
-### I-MaT: Features and Accessibility
+## Objectives
+
+As experienced during the fellowship project’s didactic test phase, working with Jupyter Notebooks and analyzing music with packages such as music21 or CAMAT proved challenging in particular for musicology students with none or only very limited knowledge of computer commands or programming languages.
+
+As an initial response, I-MaT emerged as a pragmatic solution, aiding students in quickly obtaining meaningful analysis results. Motivated by the success and the evident impact it had on the learning process, the development and refinement of I-MaT continued independently following the conclusion of the aforementioned fellowship project at the end of 2021.
+
+Since then, this research endeavor has been guided by two primary objectives:
+
+1. The first objective was to design an easily accessible tool with a well-structured interface, further lowering the barrier for musicology students to engage with methods from digital musicology.
+2. The second objective was to further refine and modularize I-MaT’s program code, to create a modular and flexible tool that could effortlessly be extended by either adding new functionalities offered by already integrated modules (such as music21 and MidiTok), or by incorporating new python packages related to digital musicology or other relevant fields, e.g., computational linguistics.
+
+## I-MaT: Features and Accessibility
 
 ```
-I-MaT - Interactive Music Analysis Tool, v3.0, (2023). Project: "Computer-Assisted Music Analysis"
+I-MaT - Interactive Music Analysis Tool, v3.1, (2023). Project: "Computer-Assisted Music Analysis"
 
 Department of Musicology Weimar-Jena, University of Music Franz Liszt Weimar, Germany
 
 MIT License, Copyright (c) 2023 S.O. Eck.
 
 ----------------------------------------------------------------------
 
@@ -70,61 +72,65 @@
 2         CONV: Conversion of multiple music files            <Conversion of multiple music file wihthin one folder>
 3         TOKE: Tokenisation of multiple music files          <Tokenisation of multiple music file wihthin one folder>
 4         CONF: Update Software Paths and Preferences         <Update or redefine paths to essential software and user preferences>
 
 Which menu item should be executed? (<No. of menu item>):
 ```
 
-Figure 1: *I-Mat - Start menu*
+Addressing the steep learning curve often encountered with Python-based music analysis tools like Music21 or CAMAT, the Interactive Music Analysis Tool (I-MaT) was designed specifically with user accessibility in mind. I-MaT utilizes a new and innovative approach to access, work with and implement various python libraries, such as, but not limited to, music21 or MidiTok for textual music analysis, within one unified, user friendly text-based command-line-interface (CLI).
+
+I-MaT allows users to quickly obtain results by navigating through simple dynamic menu structures and selecting methods and tools from predefined options (see Figure 1). The tool uses an accessible and easily extendable text-based CLI, with the underlying Music21 and MidiTok commands remaining invisible to the user. While requiring minimal familiarity with command-line environments, the preference for a CLI over a GUI offers a compromise between user-friendliness and easy code extendibility.
 
-I-MaT allows users to quickly obtain results by navigating through simple dialog windows and selecting methods and tools from predefined displayed options (*cf. figure 1*), shown in an easy-to-understand text-based command-line interface (CLI), i.e. the MS Windows Command shell (cmd) or PowerShell. Therefore, music21 commands on which the program is based are not visible to the user. Results such as visualizations, diagrams, transformed sheet music files, and CSV files can then be exported and displayed within I-MaT as well as in external programs such as MuseScore, matplotlib or PSPP, in which they can be further processed or analysed (*cf. figures 2-12*).
+This compromise was necessary to keep the barrier to entry as low as possible, and to encourage a broad usage and user-based participation in the tool's ongoing development via GitHub (Eck, 2023b). To further increase accessibility, I-MaT was distributed via Pypi.org (Eck, 2023c), allowing for an easy installation via integrated package-management systems such as the commonly used python pip installer. I-MaT’s source code is complemented by an extensive online documentation that offers guidance to both users as well as contributors (Eck, 2023a).
 
-Moreover, the modular structure of I-MaT not only facilitates the addition of new analysis modules based on music21 or other libraries, but also enables easier maintenance and updates of the tool as new analysis methods and techniques become available over time. This makes I-MaT a flexible and therefore powerful tool that can cater to the needs of a diverse range of users, from novice music analysts to advanced researchers.
+While virtually encompassing all the functionalities of the integrated python packages for music information retrieval/tokenization, i.e., music21/MidiTok, I-MaTs functionalities are currently limited to a representative, yet well-tested set of statistical analysis, export, visualization, transformation and musical data tokenization tools.
 
-### Education and Training
+With all those benefits at hand, I-MaT is a very flexible and powerful tool that could cater to the needs of a diverse range of users, from novice music analysts to advanced researchers.
 
-I-MaT is an innovative tool for music analysis that can provide valuable support for music and musicology courses at both high school and university levels. Its user-friendly interface and modular design make it an ideal tool for students to quickly obtain results and explore various analytical approaches using computational methods, allowing them to gain a deeper understanding of the musical works they are studying. In addition to its analytical capabilities, I-MaT can serve as an effective didactic tool to introduce students to computer-assisted musicology and programming concepts in general, as well as music21 or other libraries used in the tool.
+## Education and Training
 
-By using I-MaT, students can develop valuable analytical skills that will be useful not only in musicology but also in other areas of the humanities where data-driven methods are becoming increasingly important.
+In addition to its analytical capabilities, I-MaT serves as an effective didactic tool, further bridging the gap between musicology and the broader field of computer-assisted analysis and Music Information Retrieval (MIR).
 
-Lastly, I-MaT's modular structure enables collaborative work not only in the classroom but also bears the possibility to connect through platforms like GitHub, providing opportunities for its further development.
+I-MaT’s various functionalities could provide valuable support for music and musicology courses at both high school and university levels. Its user-friendly interface and simple installation make it an ideal tool for students to quickly obtain results and explore various analytical approaches using computational methods, allowing them to gain a deeper understanding of the musical works they are studying.
 
-I-MaT should be seen as a contribution to Computational Musicology or Digital Musicology within the Digital Humanities.
+Furthermore, I-MaT’s modular design opens possibilities for launching educational projects centered around musicological programming, with the added advantage of seamlessly integrating their outcomes and functions into I-MaT through collaborative platforms like GitHub.
 
-Author: Sebastian Oliver Eck (Student Project Assistant - Institute for Musicology Weimar-Jena, Franz Liszt University of Music Weimar, Germany)
+By using I-MaT, students can develop valuable analytical skills that are useful not only in musicology but also in other areas of the humanities where data-driven methods are becoming increasingly important.
+
+The Interactive Music Analysis Tool, I-MaT, should be seen as a contribution to Computational Musicology or Digital Musicology within the Digital Humanities.
 
 ## Sheet Music Databases curated within the project
 
-The fellowship project contains two larger databases:[^13]
+The fellowship project contains [two larger databases](https://analyse.hfm-weimar.de/doku.php?id=en:datenbank):
 
-- The main database[^14] comprises several thousand individual sheet music files (MusicXML).
-- The subcorpus[^15] contains all scores used in the two teaching modules for score analysis[^16] and was carefully curated by student members of the project team.
+- The [main database](https://analyse.hfm-weimar.de/doku.php?id=en:komponisten) comprises several thousand individual sheet music files (.xml).
+- The [subcorpus](https://analyse.hfm-weimar.de/doku.php?id=en:notenauswahl) contains all scores used in the two teaching modules for score analysis and was carefully curated by student members of the project team.
 
 ### List of incorporated databases
 
-The fellowship project uses several, under the Common Licence freely available online databases as sources for its own sheet music corpora. These include:
+The fellowship project uses several, under the Common Licence freely available online databases as sources for its own sheet music corpora.
+
+These include:
 
 - The Classical Music Score Digitization Project (weblink no longer available).
 - [Josquin Research Project, Standford University](http://jrp.stanford.edu).
 - [Kern Scores](http://kern.ccarh.org/).
 - [Tobi's Notenarchiv](http://www.tobis-notenarchiv.de/noten/index.htm).
 - [Sethus Calvisius' cantional settings, edited by Dr. Franz Kaern-Biederstedt](https://analyse.hfm-weimar.de/doku.php?id=en:calvisius).
 - [Music21 Corpus, MIT](https://web.mit.edu/music21/doc/about/referenceCorpus.html).
 
 ## References
 
-[^1]: Official project website: "Interactive Music Analysis Tool (I-MaT)", accessible at: https://analyse.hfm-weimar.de/doku.php?id=en:interaktive_musikanalyse (last accessed on: 2023-04-25).
-[^2]: Official project website: "music11: a toolkit for computer-aided musicology", accessible at: http://web.mit.edu/music21/ (last accessed on: 2023-04-25).
-[^3]: Official project website: "ComputergestÃ¼tzte Musikanalyse in der digitalen Hochschullehre", accessible at: https://analyse.hfm-weimar.de/doku.php?id=en:start (last accessed on: 2023-04-25).
-[^4]: University of Music Franz Liszt Weimar. Department of Musicology Weimar-Jena, https://www.hfm-weimar.de/en/department-of-musicology-weimar-jena/department-of-musicology-weimar-jena (last accessed on: 2023-04-25).
-[^5]: Fellowships Hochschullehre "Deutscher Stifterverband": Fellows 2020, Prof. Dr. Martin Pfleiderer (Hochschule fÃ¼r Musik Franz Liszt Weimar, Institut fÃ¼r Musikwissenschaft Weimar-Jena); Fellowship fÃ¼r Innovationen in der digitalen Hochschullehre, Projekt: ComputergestÃ¼tzte Musikanalyse, https://stifterverband.org/digital-lehrfellows-thueringen/2020/pfleiderer (last accessed on: 2023-04-25).
-[^6]: Egor Poliakovand Christon R. Nada: "CAMAT: Computer Assisted Music Analysis Toolkit", DMRN+16: Digital Music Research Network, One-Day Workshop 2021; Queen Mary University London, Tue 21 Devember 2021, https://analyse.hfm-weimar.de/lib/exe/fetch.php?media=en:dmrn-16-proceedings_camat.pdf (last accessed on: 2023-04-25).
-[^7]: Official project website: 1) "Module Basics: Sheet Music Analysis with music21", https://analyse.hfm-weimar.de/doku.php?id=en:basics1; 2) "Module Advanced Sheet Music Analysis with music21: Searching for Tone Sequences", https://analyse.hfm-weimar.de/doku.php?id=en:advanced1 (last accessed on: 2023-04-25).
-[^8]: Official project website: 1) "Module Basics Sheet Music Analysis with CAMAT", https://analyse.hfm-weimar.de/doku.php?id=en:camat; 2) "Module Advanced: Sheet Music Analysis with CAMAT", https://analyse.hfm-weimar.de/doku.php?id=en:advanced_camat (last accessed on: 2023-04-25).
-[^9]: Egor Poliakov (HMT Leipzig, Germany, egor.poliakov@hmt-leipzig.de).
-[^10]: Christon R. Nadar (Semantic Music Technologies, Fraunhofer IDMT, Ilmenau, Germany).
-[^11]: Cf. Egor Poliakovand Christon R. Nada (2021) (see footnote 6). For further information on the development of CAMAT, cf. Martin Pfleiderer, Egor Polyakov and Christon-Ragavan Nadar: Analyze! Development and integration of software-based tools for musicology music theory, in: Proceedings Innovation in Music 2022 Conference, edited by Jan-Olof Gullo, Russ Hepworth-Sawyer, Justin Paterson and Rob Toulson, Milton Park: Routledge 2023 (in print).
-[^12]: Official project website: "Sheet Music Analysis", https://analyse.hfm-weimar.de/doku.php?id=en:noten (last accessed on: 2023-04-25).
-[^13]: Official project website: "Sheet Music Database", https://analyse.hfm-weimar.de/doku.php?id=en:datenbank (last accessed on: 2023-04-25).
-[^14]: Official project website: "Sheet Music Database. Main Database", https://analyse.hfm-weimar.de/doku.php?id=en:komponisten (last accessed on: 2023-04-25).
-[^15]: Official project website: "Sheet Music Database. Subcorpus", https://analyse.hfm-weimar.de/doku.php?id=en:datenbank (last accessed on: 2023-04-25).
-[^16]: Cf. footnotes 7 and 8.
+- Cuthbert, M. S. A. (2023a). music21. A Toolkit for Computer-Aided Musicology. http://web.mit.edu/music21/ (accessed 19 July 2023).
+- Cuthbert, M. S. A. (2023b). music21. GitHub Repository. https://github.com/cuthbertLab/music21 (accessed 19 July 2023).
+- Eck, S. O. (2023a). Interactive Music Analysis Tool (I-MaT). Dokumentation. https://i-mat.readthedocs.io/en/latest/ (accessed 19 July 2023).
+- Eck, S. O. (2023b). Interactive Music Analysis Tool (I-MaT). GitHub Repository. https://github.com/sebastian-eck/I-MaT (accessed 19 July 2023).
+- Eck, S. O. (2023c). Interactive Music Analysis Tool (I-MaT). Pypi.org Distribution. https://pypi.org/project/imat/ (accessed 19 July 2023).
+- Fradet, N., Briot, J.-P., Chhel, F., Seghrouchni, A. E. F. and Gutowski, N. (2021). MidiTok. A Python Package for MIDI File Tokenization. https://archives.ismir.net/ismir2021/latebreaking/000005.pdf (accessed 19 July 2023).
+- Pfleiderer, M. (2022). Computergestützte Musikanalyse. Fellowship für Innovation in der digitalen Hochschullehre. Abschlussbericht. https://stifterverband.org/file/10986/download?token=tl9S2EL_.
+- Pfleiderer, M., Poliakov, E. and Nadar, C. R. (2023). Analyze! Development and Integration of Software-Based Tools for Musicology Music Theory, Proceedings Innovation in Music 2022 Conference.
+- Poliakov, E. and Nadar, C. R. (2021a). CAMAT. Computer Assisted Music Analysis Toolkit. https://analyse.hfm-weimar.de/lib/exe/fetch.php?media=en:dmrn-16-proceedings_camat.pdf (accessed 19 July 2023).
+- Poliakov, E. and Nadar, C. R. (2021b). CAMAT. GitHub Repository. https://github.com/Christon-Ragavan/CAMAT (accessed 19 July 2023).
+- University of Music Franz Liszt Weimar (2021a). Fellowship Project Computer-Assisted Music Analysis. Interactive Music Analysis Tool (I-MaT). https://analyse.hfm-weimar.de/doku.php?id=en:interaktive_musikanalyse (accessed 19 July 2023).
+- University of Music Franz Liszt Weimar (2021b). Fellowship Project Computer-Assisted Music Analysis. Modules and Tutorials. https://analyse.hfm-weimar.de/doku.php?id=en:tutorials.
+- University of Music Franz Liszt Weimar (2021c). Fellowship Project Computer-Assisted Music Analysis. Project-Wiki. https://analyse.hfm-weimar.de/doku.php?id=en:start (accessed 19 July 2023).
+- University of Music Franz Liszt Weimar (2021d). Fellowship Project Computer-Assisted Music Analysis. Sheet Music Analysis. https://analyse.hfm-weimar.de/doku.php?id=en:noten (accessed 19 July 2023).
```

### Comparing `imat-3.1/iMaT/__main__.py` & `imat-3.2.0/iMaT/__main__.py`

 * *Files identical despite different names*

### Comparing `imat-3.1/iMaT/src/analysis/functions.py` & `imat-3.2.0/iMaT/src/analysis/functions.py`

 * *Files identical despite different names*

### Comparing `imat-3.1/iMaT/src/analysis/main.py` & `imat-3.2.0/iMaT/src/analysis/main.py`

 * *Files identical despite different names*

### Comparing `imat-3.1/iMaT/src/analysis/utils.py` & `imat-3.2.0/iMaT/src/analysis/utils.py`

 * *Files 6% similar despite different names*

```diff
@@ -65,16 +65,16 @@
                 "Please select one of the following options by entering the corresponding index number:",
                 "Which option do you want to select? (<No. of option>): ",
                 ["Option", "<Explanation>"],
             ],
             "menu_entries": [
                 ["REPT: Repeat analysis function", 'repeat',
                  "<Repeat the chosen analysis function with a different score selection>"],
-                ["EXPT: Export Results to CSV", 'export', "<Explanation>"],
-                ["SHOW: Display Results", 'display_results', "<Explanation>"],
+                ["EXPT: Export Results to CSV", 'export', "<Export the analysis results to a CSV file>"],
+                ["SHOW: Display Results", 'display_results', "<Display the analysis results as a graph>"],
                 ["BACK: Return to the Last Menu", 'back', "<Returns to the main menu>"],
             ],
         }
 
         return display_menu_request_selection(imat_data_container)
 
     except Exception as e:
```

### Comparing `imat-3.1/iMaT/src/cli/menu_constructors.py` & `imat-3.2.0/iMaT/src/cli/menu_constructors.py`

 * *Files identical despite different names*

### Comparing `imat-3.1/iMaT/src/cli/menu_entries.py` & `imat-3.2.0/iMaT/src/cli/menu_entries.py`

 * *Files identical despite different names*

### Comparing `imat-3.1/iMaT/src/constants.py` & `imat-3.2.0/iMaT/src/constants.py`

 * *Files 3% similar despite different names*

```diff
@@ -11,41 +11,49 @@
 The musical keys and notes are represented in two formats: full name and abbreviation. The rhythmic values are
 represented as a float or a string (in case of triplets). The pitch class integers map to pitch class names according
 to music theory.
 
 The example scores dictionary contains information about example scores, including the title, URL, and subcorpus. The
 title text for the application includes the name and version of the application, associated project and institution,
 license information, and copyright statement.
-"""
-
-# CONSTANTS:
 
-"""
+CONSTANTS:
 
 TITLE_TEXT is a string that contains the title text for the application. It includes the name and version of the 
 application, the associated project and institution, the license information, and the copyright statement. This text 
 is used to display a title or header in the application's user interface.
 
+KEYS_LIST is a list of musical keys in the format ["Key-Name", "Abbreviation"]. It includes major and minor keys in
+different pitches. This list is used to represent and validate keys that are input or output by the system. The
+"Abbreviation" part of each list item is used for displaying or inputting keys in a compact way.
+
+NOTES_LIST is a list of musical notes in the format ["Note-Name", "Abbreviation"]. It covers a variety of notes
+including flat ("-") and sharp ("#") versions. The last two entries in the list provide options to remove the last
+note entered or finish input.
+
+RHYTHMIC_VALUES_LIST represents rhythmic values of musical notes. Each entry contains a display string and the
+corresponding rhythmic value. The rhythmic value is represented either as a float or as a string, in case of triplets.
+The list entries cover note values from thirty-second notes to double whole notes, including dotted and triplet versions.
+
+PITCH_CLASS_NAMES is a dictionary that maps integers to pitch class names. In music theory, pitch classes are the set
+of all pitches that are integer multiples of the octave. This constant is useful for converting pitch class integers
+into human-readable names.
+
+EXAMPLE_SCORES_DICT is a dictionary containing data about example scores. Each entry includes the title of the score,
+the URL where the score can be found, and the subcorpus the score belongs to. This dictionary is used to provide users
+with a selection of example scores for analysis.
 """
 
 TITLE_TEXT = (
-    '\nI-MaT - Interactive Music Analysis Tool, v3.1, (2023). Project: "Computer-Assisted Music Analysis"\n\n'
+    '\nI-MaT - Interactive Music Analysis Tool, v3.2.0, (2023). Project: "Computer-Assisted Music Analysis"\n\n'
     'Department of Musicology Weimar-Jena, University of Music Franz Liszt Weimar, Germany\n\n'
     'MIT License, Copyright (c) 2023 S.O. Eck.\n\n'
     '----------------------------------------------------------------------\n'
 )
 
-"""
-
-KEYS_LIST is a list of musical keys in the format ["Key-Name", "Abbreviation"]. It includes major and minor keys in
-different pitches. This list is used to represent and validate keys that are input or output by the system. The
-"Abbreviation" part of each list item is used for displaying or inputting keys in a compact way.
-
-"""
-
 KEYS_LIST = [
     ["C-Major", "C"],
     ["G-Major", "G"],
     ["D-Major", "D"],
     ["A-Major", "A"],
     ["E-Major", "E"],
     ["B-Major", "B"],
@@ -83,22 +91,14 @@
     ["A-flat-Minor", "a-"],
     ["D-flat-Minor", "d-"],
     ["G-flat-Minor", "g-"],
     ["C-flat-Minor", "c-"],
     ["F-flat-Minor", "f-"],
 ]
 
-"""
-
-NOTES_LIST is a list of musical notes in the format ["Note-Name", "Abbreviation"]. It covers a variety of notes 
-including flat ("-") and sharp ("#") versions. The last two entries in the list provide options to remove the last 
-note entered or finish input. 
-
-"""
-
 NOTES_LIST = [
     ["‾‾‾‾  -   C-flat", "C-"],
     ["C         C", "C"],
     ["____  ♯   C-sharp", "C#"],
     ["‾‾‾‾  -   D-flat", "D-"],
     ["D         D", "D"],
     ["____  ♯   D-sharp", "D#"],
@@ -117,22 +117,14 @@
     ["‾‾‾‾  -   B-flat", "B-"],
     ["B         B", "B"],
     ["____  ♯   B-sharp", "B#"],
     ["BACK: Remove the last note entered", "remove"],
     ["DONE: Finish input", "complete"],
 ]
 
-"""
-
-RHYTHMIC_VALUES_LIST represents rhythmic values of musical notes. Each entry contains a display string and the 
-corresponding rhythmic value. The rhythmic value is represented either as a float or as a string, in case of triplets. 
-The list entries cover note values from thirty-second notes to double whole notes, including dotted and triplet versions.
-
-"""
-
 RHYTHMIC_VALUES_LIST = [
     ["[0.125]   Thirty-second note", 0.125],
     ["[0.25]    Sixteenth note", 0.25],
     ["[0.375]   Sixteenth note (dotted)", 0.375],
     ["[1/3]     Eighth note triplet", "1/3"],
     ["[0.5]     Eighth note", 0.5],
     ["[0.75]    Eighth note (dotted)", 0.75],
@@ -148,22 +140,14 @@
     ["[16/3]    Double whole triplet", "16/3"],
     ["[8.0]     Double whole note", 8.0],
     ["[12.0]    Double whole note (dotted)", 12.0],
     ["BACK:     Remove the last note entered", "remove"],
     ["DONE:     Finish input", "complete"]
 ]
 
-"""
-
-PITCH_CLASS_NAMES is a dictionary that maps integers to pitch class names. In music theory, pitch classes are the set 
-of all pitches that are integer multiples of the octave. This constant is useful for converting pitch class integers 
-into human-readable names.
-
-"""
-
 PITCH_CLASS_NAMES = {
     0: "C",
     1: "C#/Db",
     2: "D",
     3: "D#/Eb",
     4: "E",
     5: "F",
@@ -171,22 +155,14 @@
     7: "G",
     8: "G#/Ab",
     9: "A",
     10: "A#/Bb",
     11: "B"
 }
 
-"""
-
-EXAMPLE_SCORES_DICT is a dictionary containing data about example scores. Each entry includes the title of the score, 
-the URL where the score can be found, and the subcorpus the score belongs to. This dictionary is used to provide users 
-with a selection of example scores for analysis.
-
-"""
-
 EXAMPLE_SCORES_DICT = \
     {
         "example_score_1": [
             "Example score 1: Dufay, Guillaume (1397-1474): Missa L'homme arme - Kyrie",
             "https://analyse.hfm-weimar.de/database/02/DuGui_Duf1004_COM_1-5_MissaLhomm_002_00956.xml",
             "<Subcorpus (Projekt: Computergestützte Musikanalyse)>"],
         "example_score_2": [
```

### Comparing `imat-3.1/iMaT/src/conversion/main.py` & `imat-3.2.0/iMaT/src/conversion/main.py`

 * *Files identical despite different names*

### Comparing `imat-3.1/iMaT/src/conversion/utils.py` & `imat-3.2.0/iMaT/src/conversion/utils.py`

 * *Files identical despite different names*

### Comparing `imat-3.1/iMaT/src/m21_environment/main.py` & `imat-3.2.0/iMaT/src/m21_environment/main.py`

 * *Files identical despite different names*

### Comparing `imat-3.1/iMaT/src/pattern_search/functions.py` & `imat-3.2.0/iMaT/src/pattern_search/functions.py`

 * *Files identical despite different names*

### Comparing `imat-3.1/iMaT/src/pattern_search/main.py` & `imat-3.2.0/iMaT/src/pattern_search/main.py`

 * *Files identical despite different names*

### Comparing `imat-3.1/iMaT/src/pattern_search/utils.py` & `imat-3.2.0/iMaT/src/pattern_search/utils.py`

 * *Files identical despite different names*

### Comparing `imat-3.1/iMaT/src/score_selection/main.py` & `imat-3.2.0/iMaT/src/score_selection/main.py`

 * *Files identical despite different names*

### Comparing `imat-3.1/iMaT/src/score_selection/name_parts.py` & `imat-3.2.0/iMaT/src/score_selection/name_parts.py`

 * *Files identical despite different names*

### Comparing `imat-3.1/iMaT/src/score_selection/select_parts_and_measures.py` & `imat-3.2.0/iMaT/src/score_selection/select_parts_and_measures.py`

 * *Files identical despite different names*

### Comparing `imat-3.1/iMaT/src/tokenization/main.py` & `imat-3.2.0/iMaT/src/tokenization/main.py`

 * *Files identical despite different names*

### Comparing `imat-3.1/iMaT/src/tokenization/refine_results/absolute_duration.py` & `imat-3.2.0/iMaT/src/tokenization/refine_results/absolute_duration.py`

 * *Files identical despite different names*

### Comparing `imat-3.1/iMaT/src/tokenization/refine_results/calculate_pitch_intervals.py` & `imat-3.2.0/iMaT/src/tokenization/refine_results/calculate_pitch_intervals.py`

 * *Files identical despite different names*

### Comparing `imat-3.1/iMaT/src/tokenization/refine_results/remove_prefixes.py` & `imat-3.2.0/iMaT/src/tokenization/refine_results/remove_prefixes.py`

 * *Files identical despite different names*

### Comparing `imat-3.1/iMaT/src/tokenization/refine_results/tokens_to_txt.py` & `imat-3.2.0/iMaT/src/tokenization/refine_results/tokens_to_txt.py`

 * *Files identical despite different names*

### Comparing `imat-3.1/iMaT/src/tokenization/utils.py` & `imat-3.2.0/iMaT/src/tokenization/utils.py`

 * *Files identical despite different names*

### Comparing `imat-3.1/iMaT/src/utils/error_handling.py` & `imat-3.2.0/iMaT/src/utils/error_handling.py`

 * *Files identical despite different names*

### Comparing `imat-3.1/iMaT/src/utils/misc.py` & `imat-3.2.0/iMaT/src/utils/misc.py`

 * *Files identical despite different names*

### Comparing `imat-3.1/iMaT/src/visualizations/analysis_results_graphs.py` & `imat-3.2.0/iMaT/src/visualizations/analysis_results_graphs.py`

 * *Files identical despite different names*

### Comparing `imat-3.1/iMaT/src/visualizations/m21_integrated.py` & `imat-3.2.0/iMaT/src/visualizations/m21_integrated.py`

 * *Files identical despite different names*

### Comparing `imat-3.1/iMaT/src/visualizations/main.py` & `imat-3.2.0/iMaT/src/visualizations/main.py`

 * *Files identical despite different names*

### Comparing `imat-3.1/imat.egg-info/SOURCES.txt` & `imat-3.2.0/imat.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `imat-3.1/setup.py` & `imat-3.2.0/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 import setuptools
 
-with open("README.md", "r") as fh:
+with open("README.md", "r", encoding='utf-8') as fh:
     long_description = fh.read()
 
 setuptools.setup(
     include_package_data=True,
     name='imat',
-    version='3.1',
+    version='3.2.0',
     author='Sebastian Oliver Eck',
     url="https://github.com/sebastian-eck/I-MaT",
     description='Interactive Music Analysis Tool (I-MaT)',
     long_description=long_description,
     long_description_content_type="text/markdown",
     license="MIT License",
     packages=setuptools.find_packages(),
@@ -51,14 +51,14 @@
         "openpyxl~=3.1.2",
         "tqdm~=4.65.0",
         "seaborn~=0.12.2",
         "scipy~=1.10.1"
 
     ],
     extras_require={
-        "doc": ["sphinx~=7.0.0",
+        "doc": ["sphinx<7.0.0",
                 "sphinxcontrib-napoleon~=0.7",
                 "sphinx-autobuild",
                 "myst_parser",
-                "sphinx_rtd_theme"]
+                "sphinx_rtd_theme~=1.2.0"]
     }
 )
```

