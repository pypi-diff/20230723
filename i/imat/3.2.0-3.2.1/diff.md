# Comparing `tmp/imat-3.2.0.tar.gz` & `tmp/imat-3.2.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "imat-3.2.0.tar", last modified: Sun Jul 23 16:52:52 2023, max compression
+gzip compressed data, was "imat-3.2.1.tar", last modified: Sun Jul 23 17:09:40 2023, max compression
```

## Comparing `imat-3.2.0.tar` & `imat-3.2.1.tar`

### file list

```diff
@@ -1,64 +1,64 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 16:52:52.332370 imat-3.2.0/
--rw-rw-rw-   0        0        0     1096 2023-07-17 17:26:37.000000 imat-3.2.0/LICENSE.txt
--rw-rw-rw-   0        0        0    15080 2023-07-23 16:52:52.322399 imat-3.2.0/PKG-INFO
--rw-rw-rw-   0        0        0    13871 2023-07-23 06:01:28.000000 imat-3.2.0/README.md
-drwxrwxrwx   0        0        0        0 2023-07-23 16:52:51.954384 imat-3.2.0/iMaT/
--rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/__init__.py
--rw-rw-rw-   0        0        0     2430 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/__main__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 16:52:51.959369 imat-3.2.0/iMaT/src/
--rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-23 16:52:52.003251 imat-3.2.0/iMaT/src/analysis/
--rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/analysis/__init__.py
--rw-rw-rw-   0        0        0    58077 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/analysis/functions.py
--rw-rw-rw-   0        0        0     5213 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/analysis/main.py
--rw-rw-rw-   0        0        0     3630 2023-07-23 16:40:24.000000 imat-3.2.0/iMaT/src/analysis/utils.py
-drwxrwxrwx   0        0        0        0 2023-07-23 16:52:52.028195 imat-3.2.0/iMaT/src/cli/
--rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/cli/__init__.py
--rw-rw-rw-   0        0        0    31663 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/cli/menu_constructors.py
--rw-rw-rw-   0        0        0    23891 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/cli/menu_entries.py
--rw-rw-rw-   0        0        0     7837 2023-07-23 16:47:26.000000 imat-3.2.0/iMaT/src/constants.py
-drwxrwxrwx   0        0        0        0 2023-07-23 16:52:52.038158 imat-3.2.0/iMaT/src/conversion/
--rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/conversion/__init__.py
--rw-rw-rw-   0        0        0     5090 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/conversion/main.py
--rw-rw-rw-   0        0        0    12992 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/conversion/utils.py
-drwxrwxrwx   0        0        0        0 2023-07-23 16:52:52.050126 imat-3.2.0/iMaT/src/m21_environment/
--rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/m21_environment/__init__.py
--rw-rw-rw-   0        0        0    10243 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/m21_environment/main.py
-drwxrwxrwx   0        0        0        0 2023-07-23 16:52:52.083038 imat-3.2.0/iMaT/src/pattern_search/
--rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/pattern_search/__init__.py
--rw-rw-rw-   0        0        0    15880 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/pattern_search/functions.py
--rw-rw-rw-   0        0        0    10903 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/pattern_search/main.py
--rw-rw-rw-   0        0        0    10307 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/pattern_search/utils.py
-drwxrwxrwx   0        0        0        0 2023-07-23 16:52:52.098996 imat-3.2.0/iMaT/src/score_selection/
--rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/score_selection/__init__.py
--rw-rw-rw-   0        0        0    17704 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/score_selection/main.py
--rw-rw-rw-   0        0        0    14028 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/score_selection/name_parts.py
--rw-rw-rw-   0        0        0    12218 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/score_selection/select_parts_and_measures.py
-drwxrwxrwx   0        0        0        0 2023-07-23 16:52:52.131918 imat-3.2.0/iMaT/src/tokenization/
--rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/tokenization/__init__.py
--rw-rw-rw-   0        0        0    19526 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/tokenization/main.py
-drwxrwxrwx   0        0        0        0 2023-07-23 16:52:52.197731 imat-3.2.0/iMaT/src/tokenization/refine_results/
--rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/tokenization/refine_results/__init__.py
--rw-rw-rw-   0        0        0     6837 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/tokenization/refine_results/absolute_duration.py
--rw-rw-rw-   0        0        0     7020 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/tokenization/refine_results/calculate_pitch_intervals.py
--rw-rw-rw-   0        0        0     4966 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/tokenization/refine_results/remove_prefixes.py
--rw-rw-rw-   0        0        0     5447 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/tokenization/refine_results/tokens_to_txt.py
--rw-rw-rw-   0        0        0    15349 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/tokenization/utils.py
-drwxrwxrwx   0        0        0        0 2023-07-23 16:52:52.219674 imat-3.2.0/iMaT/src/utils/
--rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/utils/__init__.py
--rw-rw-rw-   0        0        0     3982 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/utils/error_handling.py
--rw-rw-rw-   0        0        0     6787 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/utils/misc.py
-drwxrwxrwx   0        0        0        0 2023-07-23 16:52:52.268541 imat-3.2.0/iMaT/src/visualizations/
--rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/visualizations/__init__.py
--rw-rw-rw-   0        0        0    19214 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/visualizations/analysis_results_graphs.py
--rw-rw-rw-   0        0        0    10926 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/visualizations/m21_integrated.py
--rw-rw-rw-   0        0        0     3263 2023-07-17 17:26:37.000000 imat-3.2.0/iMaT/src/visualizations/main.py
-drwxrwxrwx   0        0        0        0 2023-07-23 16:52:52.319405 imat-3.2.0/imat.egg-info/
--rw-rw-rw-   0        0        0    15080 2023-07-23 16:52:50.000000 imat-3.2.0/imat.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0     1561 2023-07-23 16:52:50.000000 imat-3.2.0/imat.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 16:52:50.000000 imat-3.2.0/imat.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       44 2023-07-23 16:52:50.000000 imat-3.2.0/imat.egg-info/entry_points.txt
--rw-rw-rw-   0        0        0      272 2023-07-23 16:52:50.000000 imat-3.2.0/imat.egg-info/requires.txt
--rw-rw-rw-   0        0        0        5 2023-07-23 16:52:50.000000 imat-3.2.0/imat.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-23 16:52:52.334368 imat-3.2.0/setup.cfg
--rw-rw-rw-   0        0        0     2105 2023-07-23 16:52:45.000000 imat-3.2.0/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 17:09:40.551676 imat-3.2.1/
+-rw-rw-rw-   0        0        0     1096 2023-07-17 17:26:37.000000 imat-3.2.1/LICENSE.txt
+-rw-rw-rw-   0        0        0    15148 2023-07-23 17:09:40.544638 imat-3.2.1/PKG-INFO
+-rw-rw-rw-   0        0        0    13939 2023-07-23 17:06:33.000000 imat-3.2.1/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 17:09:40.201021 imat-3.2.1/iMaT/
+-rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/__init__.py
+-rw-rw-rw-   0        0        0     2430 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/__main__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 17:09:40.212754 imat-3.2.1/iMaT/src/
+-rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 17:09:40.250100 imat-3.2.1/iMaT/src/analysis/
+-rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/analysis/__init__.py
+-rw-rw-rw-   0        0        0    58077 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/analysis/functions.py
+-rw-rw-rw-   0        0        0     5213 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/analysis/main.py
+-rw-rw-rw-   0        0        0     3630 2023-07-23 16:40:24.000000 imat-3.2.1/iMaT/src/analysis/utils.py
+drwxrwxrwx   0        0        0        0 2023-07-23 17:09:40.275519 imat-3.2.1/iMaT/src/cli/
+-rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/cli/__init__.py
+-rw-rw-rw-   0        0        0    31663 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/cli/menu_constructors.py
+-rw-rw-rw-   0        0        0    23891 2023-07-23 17:04:10.000000 imat-3.2.1/iMaT/src/cli/menu_entries.py
+-rw-rw-rw-   0        0        0     7837 2023-07-23 17:08:29.000000 imat-3.2.1/iMaT/src/constants.py
+drwxrwxrwx   0        0        0        0 2023-07-23 17:09:40.282823 imat-3.2.1/iMaT/src/conversion/
+-rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/conversion/__init__.py
+-rw-rw-rw-   0        0        0     5090 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/conversion/main.py
+-rw-rw-rw-   0        0        0    12992 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/conversion/utils.py
+drwxrwxrwx   0        0        0        0 2023-07-23 17:09:40.286563 imat-3.2.1/iMaT/src/m21_environment/
+-rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/m21_environment/__init__.py
+-rw-rw-rw-   0        0        0    10243 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/m21_environment/main.py
+drwxrwxrwx   0        0        0        0 2023-07-23 17:09:40.309113 imat-3.2.1/iMaT/src/pattern_search/
+-rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/pattern_search/__init__.py
+-rw-rw-rw-   0        0        0    15880 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/pattern_search/functions.py
+-rw-rw-rw-   0        0        0    10903 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/pattern_search/main.py
+-rw-rw-rw-   0        0        0    10307 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/pattern_search/utils.py
+drwxrwxrwx   0        0        0        0 2023-07-23 17:09:40.344593 imat-3.2.1/iMaT/src/score_selection/
+-rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/score_selection/__init__.py
+-rw-rw-rw-   0        0        0    17704 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/score_selection/main.py
+-rw-rw-rw-   0        0        0    14028 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/score_selection/name_parts.py
+-rw-rw-rw-   0        0        0    12218 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/score_selection/select_parts_and_measures.py
+drwxrwxrwx   0        0        0        0 2023-07-23 17:09:40.362097 imat-3.2.1/iMaT/src/tokenization/
+-rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/tokenization/__init__.py
+-rw-rw-rw-   0        0        0    19526 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/tokenization/main.py
+drwxrwxrwx   0        0        0        0 2023-07-23 17:09:40.407520 imat-3.2.1/iMaT/src/tokenization/refine_results/
+-rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/tokenization/refine_results/__init__.py
+-rw-rw-rw-   0        0        0     6837 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/tokenization/refine_results/absolute_duration.py
+-rw-rw-rw-   0        0        0     7020 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/tokenization/refine_results/calculate_pitch_intervals.py
+-rw-rw-rw-   0        0        0     4966 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/tokenization/refine_results/remove_prefixes.py
+-rw-rw-rw-   0        0        0     5447 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/tokenization/refine_results/tokens_to_txt.py
+-rw-rw-rw-   0        0        0    15349 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/tokenization/utils.py
+drwxrwxrwx   0        0        0        0 2023-07-23 17:09:40.433567 imat-3.2.1/iMaT/src/utils/
+-rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/utils/__init__.py
+-rw-rw-rw-   0        0        0     3982 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/utils/error_handling.py
+-rw-rw-rw-   0        0        0     6787 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/utils/misc.py
+drwxrwxrwx   0        0        0        0 2023-07-23 17:09:40.496357 imat-3.2.1/iMaT/src/visualizations/
+-rw-rw-rw-   0        0        0        0 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/visualizations/__init__.py
+-rw-rw-rw-   0        0        0    19214 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/visualizations/analysis_results_graphs.py
+-rw-rw-rw-   0        0        0    10926 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/visualizations/m21_integrated.py
+-rw-rw-rw-   0        0        0     3263 2023-07-17 17:26:37.000000 imat-3.2.1/iMaT/src/visualizations/main.py
+drwxrwxrwx   0        0        0        0 2023-07-23 17:09:40.523313 imat-3.2.1/imat.egg-info/
+-rw-rw-rw-   0        0        0    15148 2023-07-23 17:09:38.000000 imat-3.2.1/imat.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0     1561 2023-07-23 17:09:38.000000 imat-3.2.1/imat.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 17:09:38.000000 imat-3.2.1/imat.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       44 2023-07-23 17:09:38.000000 imat-3.2.1/imat.egg-info/entry_points.txt
+-rw-rw-rw-   0        0        0      272 2023-07-23 17:09:38.000000 imat-3.2.1/imat.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        5 2023-07-23 17:09:38.000000 imat-3.2.1/imat.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 17:09:40.552673 imat-3.2.1/setup.cfg
+-rw-rw-rw-   0        0        0     2105 2023-07-23 17:08:29.000000 imat-3.2.1/setup.py
```

### Comparing `imat-3.2.0/LICENSE.txt` & `imat-3.2.1/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `imat-3.2.0/PKG-INFO` & `imat-3.2.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: imat
-Version: 3.2.0
+Version: 3.2.1
 Summary: Interactive Music Analysis Tool (I-MaT)
 Home-page: https://github.com/sebastian-eck/I-MaT
 Author: Sebastian Oliver Eck
 License: MIT License
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
@@ -95,20 +95,21 @@
 LOCATION: Start Menu
 
 Please make a selection from the options below by entering the entry index number:
 
 No.       Menu item                                           <Explanation>
 
 1         PROG: Analysis of one sheet music file              <Analysis of a single piece of music>
-2         CONV: Conversion of multiple music files            <Conversion of multiple music file wihthin one folder>
-3         TOKE: Tokenisation of multiple music files          <Tokenisation of multiple music file wihthin one folder>
+2         CONV: Conversion of multiple music files            <Conversion of multiple music files within one folder>
+3         TOKE: Tokenisation of multiple music files          <Tokenisation of multiple music files within one folder>
 4         CONF: Update Software Paths and Preferences         <Update or redefine paths to essential software and user preferences>
 
 Which menu item should be executed? (<No. of menu item>):
 ```
+Figure 1: The Interactive Music Analysis Tool (I-MaT) - Start Menu
 
 Addressing the steep learning curve often encountered with Python-based music analysis tools like Music21 or CAMAT, the Interactive Music Analysis Tool (I-MaT) was designed specifically with user accessibility in mind. I-MaT utilizes a new and innovative approach to access, work with and implement various python libraries, such as, but not limited to, music21 or MidiTok for textual music analysis, within one unified, user friendly text-based command-line-interface (CLI).
 
 I-MaT allows users to quickly obtain results by navigating through simple dynamic menu structures and selecting methods and tools from predefined options (see Figure 1). The tool uses an accessible and easily extendable text-based CLI, with the underlying Music21 and MidiTok commands remaining invisible to the user. While requiring minimal familiarity with command-line environments, the preference for a CLI over a GUI offers a compromise between user-friendliness and easy code extendibility.
 
 This compromise was necessary to keep the barrier to entry as low as possible, and to encourage a broad usage and user-based participation in the tool's ongoing development via GitHub (Eck, 2023b). To further increase accessibility, I-MaT was distributed via Pypi.org (Eck, 2023c), allowing for an easy installation via integrated package-management systems such as the commonly used python pip installer. I-MaT’s source code is complemented by an extensive online documentation that offers guidance to both users as well as contributors (Eck, 2023a).
```

### Comparing `imat-3.2.0/README.md` & `imat-3.2.1/README.md`

 * *Files 1% similar despite different names*

```diff
@@ -65,20 +65,21 @@
 LOCATION: Start Menu
 
 Please make a selection from the options below by entering the entry index number:
 
 No.       Menu item                                           <Explanation>
 
 1         PROG: Analysis of one sheet music file              <Analysis of a single piece of music>
-2         CONV: Conversion of multiple music files            <Conversion of multiple music file wihthin one folder>
-3         TOKE: Tokenisation of multiple music files          <Tokenisation of multiple music file wihthin one folder>
+2         CONV: Conversion of multiple music files            <Conversion of multiple music files within one folder>
+3         TOKE: Tokenisation of multiple music files          <Tokenisation of multiple music files within one folder>
 4         CONF: Update Software Paths and Preferences         <Update or redefine paths to essential software and user preferences>
 
 Which menu item should be executed? (<No. of menu item>):
 ```
+Figure 1: The Interactive Music Analysis Tool (I-MaT) - Start Menu
 
 Addressing the steep learning curve often encountered with Python-based music analysis tools like Music21 or CAMAT, the Interactive Music Analysis Tool (I-MaT) was designed specifically with user accessibility in mind. I-MaT utilizes a new and innovative approach to access, work with and implement various python libraries, such as, but not limited to, music21 or MidiTok for textual music analysis, within one unified, user friendly text-based command-line-interface (CLI).
 
 I-MaT allows users to quickly obtain results by navigating through simple dynamic menu structures and selecting methods and tools from predefined options (see Figure 1). The tool uses an accessible and easily extendable text-based CLI, with the underlying Music21 and MidiTok commands remaining invisible to the user. While requiring minimal familiarity with command-line environments, the preference for a CLI over a GUI offers a compromise between user-friendliness and easy code extendibility.
 
 This compromise was necessary to keep the barrier to entry as low as possible, and to encourage a broad usage and user-based participation in the tool's ongoing development via GitHub (Eck, 2023b). To further increase accessibility, I-MaT was distributed via Pypi.org (Eck, 2023c), allowing for an easy installation via integrated package-management systems such as the commonly used python pip installer. I-MaT’s source code is complemented by an extensive online documentation that offers guidance to both users as well as contributors (Eck, 2023a).
```

### Comparing `imat-3.2.0/iMaT/__main__.py` & `imat-3.2.1/iMaT/__main__.py`

 * *Files identical despite different names*

### Comparing `imat-3.2.0/iMaT/src/analysis/functions.py` & `imat-3.2.1/iMaT/src/analysis/functions.py`

 * *Files identical despite different names*

### Comparing `imat-3.2.0/iMaT/src/analysis/main.py` & `imat-3.2.1/iMaT/src/analysis/main.py`

 * *Files identical despite different names*

### Comparing `imat-3.2.0/iMaT/src/analysis/utils.py` & `imat-3.2.1/iMaT/src/analysis/utils.py`

 * *Files identical despite different names*

### Comparing `imat-3.2.0/iMaT/src/cli/menu_constructors.py` & `imat-3.2.1/iMaT/src/cli/menu_constructors.py`

 * *Files identical despite different names*

### Comparing `imat-3.2.0/iMaT/src/cli/menu_entries.py` & `imat-3.2.1/iMaT/src/cli/menu_entries.py`

 * *Files 0% similar despite different names*

```diff
@@ -77,16 +77,16 @@
             "LOCATION: Start Menu",
             "Please make a selection from the options below by entering the entry index number:",
             "Which menu item should be executed? (<No. of menu item>): ",
             ["Menu item", "<Explanation>"],
         ],
         "menu_entries": [
             ["PROG: Analysis of one sheet music file", mainmenu_single_musical_piece_entries, "<Analysis of a single piece of music>"],
-            ["CONV: Conversion of multiple music files", convert_multiple_files_filetype, "<Conversion of multiple music file wihthin one folder>"],
-            ["TOKE: Tokenisation of multiple music files", mainmenu_tokenization_entries, "<Tokenisation of multiple music file wihthin one folder>"],
+            ["CONV: Conversion of multiple music files", convert_multiple_files_filetype, "<Conversion of multiple music files within one folder>"],
+            ["TOKE: Tokenisation of multiple music files", mainmenu_tokenization_entries, "<Tokenisation of multiple music files within one folder>"],
             ["CONF: Update Software Paths and Preferences", mainmenu_environment_settings_entries, "<Update or redefine paths to essential software and user preferences>"],
         ]
     }
 
 
 def mainmenu_single_musical_piece_entries():
     """
```

### Comparing `imat-3.2.0/iMaT/src/constants.py` & `imat-3.2.1/iMaT/src/constants.py`

 * *Files 0% similar despite different names*

```diff
@@ -40,15 +40,15 @@
 
 EXAMPLE_SCORES_DICT is a dictionary containing data about example scores. Each entry includes the title of the score,
 the URL where the score can be found, and the subcorpus the score belongs to. This dictionary is used to provide users
 with a selection of example scores for analysis.
 """
 
 TITLE_TEXT = (
-    '\nI-MaT - Interactive Music Analysis Tool, v3.2.0, (2023). Project: "Computer-Assisted Music Analysis"\n\n'
+    '\nI-MaT - Interactive Music Analysis Tool, v3.2.1, (2023). Project: "Computer-Assisted Music Analysis"\n\n'
     'Department of Musicology Weimar-Jena, University of Music Franz Liszt Weimar, Germany\n\n'
     'MIT License, Copyright (c) 2023 S.O. Eck.\n\n'
     '----------------------------------------------------------------------\n'
 )
 
 KEYS_LIST = [
     ["C-Major", "C"],
```

### Comparing `imat-3.2.0/iMaT/src/conversion/main.py` & `imat-3.2.1/iMaT/src/conversion/main.py`

 * *Files identical despite different names*

### Comparing `imat-3.2.0/iMaT/src/conversion/utils.py` & `imat-3.2.1/iMaT/src/conversion/utils.py`

 * *Files identical despite different names*

### Comparing `imat-3.2.0/iMaT/src/m21_environment/main.py` & `imat-3.2.1/iMaT/src/m21_environment/main.py`

 * *Files identical despite different names*

### Comparing `imat-3.2.0/iMaT/src/pattern_search/functions.py` & `imat-3.2.1/iMaT/src/pattern_search/functions.py`

 * *Files identical despite different names*

### Comparing `imat-3.2.0/iMaT/src/pattern_search/main.py` & `imat-3.2.1/iMaT/src/pattern_search/main.py`

 * *Files identical despite different names*

### Comparing `imat-3.2.0/iMaT/src/pattern_search/utils.py` & `imat-3.2.1/iMaT/src/pattern_search/utils.py`

 * *Files identical despite different names*

### Comparing `imat-3.2.0/iMaT/src/score_selection/main.py` & `imat-3.2.1/iMaT/src/score_selection/main.py`

 * *Files identical despite different names*

### Comparing `imat-3.2.0/iMaT/src/score_selection/name_parts.py` & `imat-3.2.1/iMaT/src/score_selection/name_parts.py`

 * *Files identical despite different names*

### Comparing `imat-3.2.0/iMaT/src/score_selection/select_parts_and_measures.py` & `imat-3.2.1/iMaT/src/score_selection/select_parts_and_measures.py`

 * *Files identical despite different names*

### Comparing `imat-3.2.0/iMaT/src/tokenization/main.py` & `imat-3.2.1/iMaT/src/tokenization/main.py`

 * *Files identical despite different names*

### Comparing `imat-3.2.0/iMaT/src/tokenization/refine_results/absolute_duration.py` & `imat-3.2.1/iMaT/src/tokenization/refine_results/absolute_duration.py`

 * *Files identical despite different names*

### Comparing `imat-3.2.0/iMaT/src/tokenization/refine_results/calculate_pitch_intervals.py` & `imat-3.2.1/iMaT/src/tokenization/refine_results/calculate_pitch_intervals.py`

 * *Files identical despite different names*

### Comparing `imat-3.2.0/iMaT/src/tokenization/refine_results/remove_prefixes.py` & `imat-3.2.1/iMaT/src/tokenization/refine_results/remove_prefixes.py`

 * *Files identical despite different names*

### Comparing `imat-3.2.0/iMaT/src/tokenization/refine_results/tokens_to_txt.py` & `imat-3.2.1/iMaT/src/tokenization/refine_results/tokens_to_txt.py`

 * *Files identical despite different names*

### Comparing `imat-3.2.0/iMaT/src/tokenization/utils.py` & `imat-3.2.1/iMaT/src/tokenization/utils.py`

 * *Files identical despite different names*

### Comparing `imat-3.2.0/iMaT/src/utils/error_handling.py` & `imat-3.2.1/iMaT/src/utils/error_handling.py`

 * *Files identical despite different names*

### Comparing `imat-3.2.0/iMaT/src/utils/misc.py` & `imat-3.2.1/iMaT/src/utils/misc.py`

 * *Files identical despite different names*

### Comparing `imat-3.2.0/iMaT/src/visualizations/analysis_results_graphs.py` & `imat-3.2.1/iMaT/src/visualizations/analysis_results_graphs.py`

 * *Files identical despite different names*

### Comparing `imat-3.2.0/iMaT/src/visualizations/m21_integrated.py` & `imat-3.2.1/iMaT/src/visualizations/m21_integrated.py`

 * *Files identical despite different names*

### Comparing `imat-3.2.0/iMaT/src/visualizations/main.py` & `imat-3.2.1/iMaT/src/visualizations/main.py`

 * *Files identical despite different names*

### Comparing `imat-3.2.0/imat.egg-info/PKG-INFO` & `imat-3.2.1/imat.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: imat
-Version: 3.2.0
+Version: 3.2.1
 Summary: Interactive Music Analysis Tool (I-MaT)
 Home-page: https://github.com/sebastian-eck/I-MaT
 Author: Sebastian Oliver Eck
 License: MIT License
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
@@ -95,20 +95,21 @@
 LOCATION: Start Menu
 
 Please make a selection from the options below by entering the entry index number:
 
 No.       Menu item                                           <Explanation>
 
 1         PROG: Analysis of one sheet music file              <Analysis of a single piece of music>
-2         CONV: Conversion of multiple music files            <Conversion of multiple music file wihthin one folder>
-3         TOKE: Tokenisation of multiple music files          <Tokenisation of multiple music file wihthin one folder>
+2         CONV: Conversion of multiple music files            <Conversion of multiple music files within one folder>
+3         TOKE: Tokenisation of multiple music files          <Tokenisation of multiple music files within one folder>
 4         CONF: Update Software Paths and Preferences         <Update or redefine paths to essential software and user preferences>
 
 Which menu item should be executed? (<No. of menu item>):
 ```
+Figure 1: The Interactive Music Analysis Tool (I-MaT) - Start Menu
 
 Addressing the steep learning curve often encountered with Python-based music analysis tools like Music21 or CAMAT, the Interactive Music Analysis Tool (I-MaT) was designed specifically with user accessibility in mind. I-MaT utilizes a new and innovative approach to access, work with and implement various python libraries, such as, but not limited to, music21 or MidiTok for textual music analysis, within one unified, user friendly text-based command-line-interface (CLI).
 
 I-MaT allows users to quickly obtain results by navigating through simple dynamic menu structures and selecting methods and tools from predefined options (see Figure 1). The tool uses an accessible and easily extendable text-based CLI, with the underlying Music21 and MidiTok commands remaining invisible to the user. While requiring minimal familiarity with command-line environments, the preference for a CLI over a GUI offers a compromise between user-friendliness and easy code extendibility.
 
 This compromise was necessary to keep the barrier to entry as low as possible, and to encourage a broad usage and user-based participation in the tool's ongoing development via GitHub (Eck, 2023b). To further increase accessibility, I-MaT was distributed via Pypi.org (Eck, 2023c), allowing for an easy installation via integrated package-management systems such as the commonly used python pip installer. I-MaT’s source code is complemented by an extensive online documentation that offers guidance to both users as well as contributors (Eck, 2023a).
```

### Comparing `imat-3.2.0/imat.egg-info/SOURCES.txt` & `imat-3.2.1/imat.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `imat-3.2.0/setup.py` & `imat-3.2.1/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 
 with open("README.md", "r", encoding='utf-8') as fh:
     long_description = fh.read()
 
 setuptools.setup(
     include_package_data=True,
     name='imat',
-    version='3.2.0',
+    version='3.2.1',
     author='Sebastian Oliver Eck',
     url="https://github.com/sebastian-eck/I-MaT",
     description='Interactive Music Analysis Tool (I-MaT)',
     long_description=long_description,
     long_description_content_type="text/markdown",
     license="MIT License",
     packages=setuptools.find_packages(),
```

