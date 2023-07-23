# Comparing `tmp/fasttextsearch-0.51.tar.gz` & `tmp/fasttextsearch-0.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "fasttextsearch-0.51.tar", last modified: Sun Jul 23 09:32:08 2023, max compression
+gzip compressed data, was "fasttextsearch-0.6.tar", last modified: Sun Jul 23 09:59:50 2023, max compression
```

## Comparing `fasttextsearch-0.51.tar` & `fasttextsearch-0.6.tar`

### file list

```diff
@@ -1,70 +1,70 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:32:08.427174 fasttextsearch-0.51/
--rw-r--r--   0 runner    (1001) docker     (123)     2278 2023-07-23 09:28:52.000000 fasttextsearch-0.51/CMakeLists.txt
--rw-r--r--   0 runner    (1001) docker     (123)      143 2023-07-23 09:28:52.000000 fasttextsearch-0.51/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     1170 2023-07-23 09:32:08.427174 fasttextsearch-0.51/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      577 2023-07-23 09:28:52.000000 fasttextsearch-0.51/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:32:08.419174 fasttextsearch-0.51/cmake/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:32:08.419174 fasttextsearch-0.51/cmake/Modules/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:32:08.423174 fasttextsearch-0.51/cmake/Modules/FetchContent/
--rw-r--r--   0 runner    (1001) docker     (123)      831 2023-07-23 09:28:52.000000 fasttextsearch-0.51/cmake/Modules/FetchContent/CMakeLists.cmake.in
--rw-r--r--   0 runner    (1001) docker     (123)    38023 2023-07-23 09:28:52.000000 fasttextsearch-0.51/cmake/Modules/FetchContent.cmake
--rw-r--r--   0 runner    (1001) docker     (123)      135 2023-07-23 09:28:52.000000 fasttextsearch-0.51/cmake/Modules/README.md
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 09:28:52.000000 fasttextsearch-0.51/cmake/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3421 2023-07-23 09:28:52.000000 fasttextsearch-0.51/cmake/googletest.cmake
--rw-r--r--   0 runner    (1001) docker     (123)     1800 2023-07-23 09:28:52.000000 fasttextsearch-0.51/cmake/pybind11.cmake
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:32:08.423174 fasttextsearch-0.51/fasttextsearch.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1170 2023-07-23 09:32:08.000000 fasttextsearch-0.51/fasttextsearch.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1897 2023-07-23 09:32:08.000000 fasttextsearch-0.51/fasttextsearch.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 09:32:08.000000 fasttextsearch-0.51/fasttextsearch.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        6 2023-07-23 09:32:08.000000 fasttextsearch-0.51/fasttextsearch.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       24 2023-07-23 09:32:08.000000 fasttextsearch-0.51/fasttextsearch.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)      801 2023-07-23 09:28:52.000000 fasttextsearch-0.51/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)        6 2023-07-23 09:28:52.000000 fasttextsearch-0.51/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 09:32:08.427174 fasttextsearch-0.51/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     2986 2023-07-23 09:28:52.000000 fasttextsearch-0.51/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:32:08.423174 fasttextsearch-0.51/textsearch/
--rw-r--r--   0 runner    (1001) docker     (123)       48 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/CMakeLists.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:32:08.423174 fasttextsearch-0.51/textsearch/csrc/
--rw-r--r--   0 runner    (1001) docker     (123)      695 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/csrc/CMakeLists.txt
--rw-r--r--   0 runner    (1001) docker     (123)    13272 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/csrc/levenshtein.h
--rw-r--r--   0 runner    (1001) docker     (123)     4137 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/csrc/levenshtein_test.cc
--rw-r--r--   0 runner    (1001) docker     (123)     4694 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/csrc/match.cc
--rw-r--r--   0 runner    (1001) docker     (123)     4611 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/csrc/match.h
--rw-r--r--   0 runner    (1001) docker     (123)     3248 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/csrc/match_test.cc
--rw-r--r--   0 runner    (1001) docker     (123)     5273 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/csrc/suffix_array.cc
--rw-r--r--   0 runner    (1001) docker     (123)     3207 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/csrc/suffix_array.h
--rw-r--r--   0 runner    (1001) docker     (123)     3883 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/csrc/suffix_array_test.cc
--rw-r--r--   0 runner    (1001) docker     (123)     2880 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/csrc/utils.cc
--rw-r--r--   0 runner    (1001) docker     (123)     3508 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/csrc/utils.h
--rw-r--r--   0 runner    (1001) docker     (123)     4862 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/csrc/utils_test.cc
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:32:08.423174 fasttextsearch-0.51/textsearch/python/
--rw-r--r--   0 runner    (1001) docker     (123)       78 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/CMakeLists.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:32:08.423174 fasttextsearch-0.51/textsearch/python/csrc/
--rw-r--r--   0 runner    (1001) docker     (123)      169 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/csrc/CMakeLists.txt
--rw-r--r--   0 runner    (1001) docker     (123)     5003 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/csrc/levenshtein.cc
--rw-r--r--   0 runner    (1001) docker     (123)      985 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/csrc/levenshtein.h
--rw-r--r--   0 runner    (1001) docker     (123)     1850 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/csrc/match.cc
--rw-r--r--   0 runner    (1001) docker     (123)      961 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/csrc/match.h
--rw-r--r--   0 runner    (1001) docker     (123)     1637 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/csrc/suffix_array.cc
--rw-r--r--   0 runner    (1001) docker     (123)      988 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/csrc/suffix_array.h
--rw-r--r--   0 runner    (1001) docker     (123)      564 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/csrc/text_search.cc
--rw-r--r--   0 runner    (1001) docker     (123)      357 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/csrc/text_search.h
--rw-r--r--   0 runner    (1001) docker     (123)     4599 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/csrc/utils.cc
--rw-r--r--   0 runner    (1001) docker     (123)      318 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/csrc/utils.h
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:32:08.427174 fasttextsearch-0.51/textsearch/python/tests/
--rw-r--r--   0 runner    (1001) docker     (123)      848 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/tests/CMakeLists.txt
--rwxr-xr-x   0 runner    (1001) docker     (123)     4748 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/tests/test_find_close_matches.py
--rwxr-xr-x   0 runner    (1001) docker     (123)     1943 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/tests/test_levenshtein_distance.py
--rwxr-xr-x   0 runner    (1001) docker     (123)     1414 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/tests/test_match.py
--rwxr-xr-x   0 runner    (1001) docker     (123)      950 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/tests/test_row_ids_to_row_splits.py
--rwxr-xr-x   0 runner    (1001) docker     (123)    10687 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/tests/test_sourced_text.py
--rwxr-xr-x   0 runner    (1001) docker     (123)     1359 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/tests/test_suffix_array.py
--rwxr-xr-x   0 runner    (1001) docker     (123)     2007 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/tests/test_text_source.py
--rwxr-xr-x   0 runner    (1001) docker     (123)     2314 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/tests/test_transcript.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:32:08.427174 fasttextsearch-0.51/textsearch/python/textsearch/
--rw-r--r--   0 runner    (1001) docker     (123)      740 2023-07-23 09:32:08.000000 fasttextsearch-0.51/textsearch/python/textsearch/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    13469 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/textsearch/datatypes.py
--rw-r--r--   0 runner    (1001) docker     (123)     3606 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/textsearch/levenshtein.py
--rw-r--r--   0 runner    (1001) docker     (123)    52271 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/textsearch/match.py
--rw-r--r--   0 runner    (1001) docker     (123)     3208 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/textsearch/suffix_array.py
--rw-r--r--   0 runner    (1001) docker     (123)     5269 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/textsearch/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:59:50.983270 fasttextsearch-0.6/
+-rw-r--r--   0 runner    (1001) docker     (123)     2277 2023-07-23 09:56:31.000000 fasttextsearch-0.6/CMakeLists.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      143 2023-07-23 09:56:31.000000 fasttextsearch-0.6/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     1169 2023-07-23 09:59:50.983270 fasttextsearch-0.6/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      577 2023-07-23 09:56:31.000000 fasttextsearch-0.6/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:59:50.971270 fasttextsearch-0.6/cmake/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:59:50.971270 fasttextsearch-0.6/cmake/Modules/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:59:50.971270 fasttextsearch-0.6/cmake/Modules/FetchContent/
+-rw-r--r--   0 runner    (1001) docker     (123)      831 2023-07-23 09:56:31.000000 fasttextsearch-0.6/cmake/Modules/FetchContent/CMakeLists.cmake.in
+-rw-r--r--   0 runner    (1001) docker     (123)    38023 2023-07-23 09:56:31.000000 fasttextsearch-0.6/cmake/Modules/FetchContent.cmake
+-rw-r--r--   0 runner    (1001) docker     (123)      135 2023-07-23 09:56:31.000000 fasttextsearch-0.6/cmake/Modules/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 09:56:31.000000 fasttextsearch-0.6/cmake/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3421 2023-07-23 09:56:31.000000 fasttextsearch-0.6/cmake/googletest.cmake
+-rw-r--r--   0 runner    (1001) docker     (123)     1800 2023-07-23 09:56:31.000000 fasttextsearch-0.6/cmake/pybind11.cmake
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:59:50.975270 fasttextsearch-0.6/fasttextsearch.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1169 2023-07-23 09:59:50.000000 fasttextsearch-0.6/fasttextsearch.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1897 2023-07-23 09:59:50.000000 fasttextsearch-0.6/fasttextsearch.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 09:59:50.000000 fasttextsearch-0.6/fasttextsearch.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        6 2023-07-23 09:59:50.000000 fasttextsearch-0.6/fasttextsearch.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       24 2023-07-23 09:59:50.000000 fasttextsearch-0.6/fasttextsearch.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      800 2023-07-23 09:56:31.000000 fasttextsearch-0.6/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)        6 2023-07-23 09:56:31.000000 fasttextsearch-0.6/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 09:59:50.983270 fasttextsearch-0.6/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     2986 2023-07-23 09:56:31.000000 fasttextsearch-0.6/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:59:50.975270 fasttextsearch-0.6/textsearch/
+-rw-r--r--   0 runner    (1001) docker     (123)       48 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/CMakeLists.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:59:50.975270 fasttextsearch-0.6/textsearch/csrc/
+-rw-r--r--   0 runner    (1001) docker     (123)      695 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/csrc/CMakeLists.txt
+-rw-r--r--   0 runner    (1001) docker     (123)    13272 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/csrc/levenshtein.h
+-rw-r--r--   0 runner    (1001) docker     (123)     4137 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/csrc/levenshtein_test.cc
+-rw-r--r--   0 runner    (1001) docker     (123)     4694 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/csrc/match.cc
+-rw-r--r--   0 runner    (1001) docker     (123)     4611 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/csrc/match.h
+-rw-r--r--   0 runner    (1001) docker     (123)     3248 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/csrc/match_test.cc
+-rw-r--r--   0 runner    (1001) docker     (123)     5273 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/csrc/suffix_array.cc
+-rw-r--r--   0 runner    (1001) docker     (123)     3207 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/csrc/suffix_array.h
+-rw-r--r--   0 runner    (1001) docker     (123)     3883 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/csrc/suffix_array_test.cc
+-rw-r--r--   0 runner    (1001) docker     (123)     2880 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/csrc/utils.cc
+-rw-r--r--   0 runner    (1001) docker     (123)     3508 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/csrc/utils.h
+-rw-r--r--   0 runner    (1001) docker     (123)     4862 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/csrc/utils_test.cc
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:59:50.975270 fasttextsearch-0.6/textsearch/python/
+-rw-r--r--   0 runner    (1001) docker     (123)       78 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/python/CMakeLists.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:59:50.979270 fasttextsearch-0.6/textsearch/python/csrc/
+-rw-r--r--   0 runner    (1001) docker     (123)      169 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/python/csrc/CMakeLists.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     5003 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/python/csrc/levenshtein.cc
+-rw-r--r--   0 runner    (1001) docker     (123)      985 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/python/csrc/levenshtein.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1850 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/python/csrc/match.cc
+-rw-r--r--   0 runner    (1001) docker     (123)      961 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/python/csrc/match.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1637 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/python/csrc/suffix_array.cc
+-rw-r--r--   0 runner    (1001) docker     (123)      988 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/python/csrc/suffix_array.h
+-rw-r--r--   0 runner    (1001) docker     (123)      564 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/python/csrc/text_search.cc
+-rw-r--r--   0 runner    (1001) docker     (123)      357 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/python/csrc/text_search.h
+-rw-r--r--   0 runner    (1001) docker     (123)     4599 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/python/csrc/utils.cc
+-rw-r--r--   0 runner    (1001) docker     (123)      318 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/python/csrc/utils.h
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:59:50.983270 fasttextsearch-0.6/textsearch/python/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)      848 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/python/tests/CMakeLists.txt
+-rwxr-xr-x   0 runner    (1001) docker     (123)     4748 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/python/tests/test_find_close_matches.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     1943 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/python/tests/test_levenshtein_distance.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     1414 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/python/tests/test_match.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)      950 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/python/tests/test_row_ids_to_row_splits.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)    10687 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/python/tests/test_sourced_text.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     1359 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/python/tests/test_suffix_array.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     2007 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/python/tests/test_text_source.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     2314 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/python/tests/test_transcript.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:59:50.983270 fasttextsearch-0.6/textsearch/python/textsearch/
+-rw-r--r--   0 runner    (1001) docker     (123)      738 2023-07-23 09:59:50.000000 fasttextsearch-0.6/textsearch/python/textsearch/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13469 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/python/textsearch/datatypes.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3606 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/python/textsearch/levenshtein.py
+-rw-r--r--   0 runner    (1001) docker     (123)    52271 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/python/textsearch/match.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3208 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/python/textsearch/suffix_array.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5269 2023-07-23 09:56:31.000000 fasttextsearch-0.6/textsearch/python/textsearch/utils.py
```

### Comparing `fasttextsearch-0.51/CMakeLists.txt` & `fasttextsearch-0.6/CMakeLists.txt`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 cmake_minimum_required(VERSION 3.8 FATAL_ERROR)
 project(textsearch)
 
-set(TS_VERSION "0.51")
+set(TS_VERSION "0.6")
 
 set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/lib")
 set(CMAKE_LIBRARY_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/lib")
 set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin")
 
 set(CMAKE_SKIP_BUILD_RPATH FALSE)
 set(BUILD_RPATH_USE_ORIGIN TRUE)
```

### Comparing `fasttextsearch-0.51/PKG-INFO` & `fasttextsearch-0.6/PKG-INFO`

 * *Files 18% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: fasttextsearch
-Version: 0.51
+Version: 0.6
 Summary: Some fast-ish algorithms for batch text search in moderate-sized collections, intended for data cleanup.
 Author-email: Next-gen Kaldi development team <wkang.pku@gmail.com>
 Project-URL: Homepage, https://github.com/k2-fsa/text_search
 Project-URL: Bug Tracker, https://github.com/k2-fsa/text_search/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Operating System :: OS Independent
```

### Comparing `fasttextsearch-0.51/README.md` & `fasttextsearch-0.6/README.md`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/cmake/Modules/FetchContent/CMakeLists.cmake.in` & `fasttextsearch-0.6/cmake/Modules/FetchContent/CMakeLists.cmake.in`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/cmake/Modules/FetchContent.cmake` & `fasttextsearch-0.6/cmake/Modules/FetchContent.cmake`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/cmake/googletest.cmake` & `fasttextsearch-0.6/cmake/googletest.cmake`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/cmake/pybind11.cmake` & `fasttextsearch-0.6/cmake/pybind11.cmake`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/fasttextsearch.egg-info/PKG-INFO` & `fasttextsearch-0.6/fasttextsearch.egg-info/PKG-INFO`

 * *Files 18% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: fasttextsearch
-Version: 0.51
+Version: 0.6
 Summary: Some fast-ish algorithms for batch text search in moderate-sized collections, intended for data cleanup.
 Author-email: Next-gen Kaldi development team <wkang.pku@gmail.com>
 Project-URL: Homepage, https://github.com/k2-fsa/text_search
 Project-URL: Bug Tracker, https://github.com/k2-fsa/text_search/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Operating System :: OS Independent
```

### Comparing `fasttextsearch-0.51/fasttextsearch.egg-info/SOURCES.txt` & `fasttextsearch-0.6/fasttextsearch.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/pyproject.toml` & `fasttextsearch-0.6/pyproject.toml`

 * *Files 15% similar despite different names*

```diff
@@ -6,15 +6,15 @@
     "cmake>=3.8",
 ]
 build-backend = "setuptools.build_meta"
 
 
 [project]
 name = "fasttextsearch"
-version = "0.51"
+version = "0.6"
 authors = [
   { name="Next-gen Kaldi development team", email="wkang.pku@gmail.com" },
 ]
 description="Some fast-ish algorithms for batch text search in moderate-sized collections, intended for data cleanup."
 dependencies = [
   "numpy",
 ]
```

### Comparing `fasttextsearch-0.51/setup.py` & `fasttextsearch-0.6/setup.py`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/csrc/CMakeLists.txt` & `fasttextsearch-0.6/textsearch/csrc/CMakeLists.txt`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/csrc/levenshtein.h` & `fasttextsearch-0.6/textsearch/csrc/levenshtein.h`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/csrc/levenshtein_test.cc` & `fasttextsearch-0.6/textsearch/csrc/levenshtein_test.cc`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/csrc/match.cc` & `fasttextsearch-0.6/textsearch/csrc/match.cc`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/csrc/match.h` & `fasttextsearch-0.6/textsearch/csrc/match.h`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/csrc/match_test.cc` & `fasttextsearch-0.6/textsearch/csrc/match_test.cc`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/csrc/suffix_array.cc` & `fasttextsearch-0.6/textsearch/csrc/suffix_array.cc`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/csrc/suffix_array.h` & `fasttextsearch-0.6/textsearch/csrc/suffix_array.h`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/csrc/suffix_array_test.cc` & `fasttextsearch-0.6/textsearch/csrc/suffix_array_test.cc`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/csrc/utils.cc` & `fasttextsearch-0.6/textsearch/csrc/utils.cc`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/csrc/utils.h` & `fasttextsearch-0.6/textsearch/csrc/utils.h`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/csrc/utils_test.cc` & `fasttextsearch-0.6/textsearch/csrc/utils_test.cc`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/python/csrc/levenshtein.cc` & `fasttextsearch-0.6/textsearch/python/csrc/levenshtein.cc`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/python/csrc/levenshtein.h` & `fasttextsearch-0.6/textsearch/python/csrc/levenshtein.h`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/python/csrc/match.cc` & `fasttextsearch-0.6/textsearch/python/csrc/match.cc`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/python/csrc/match.h` & `fasttextsearch-0.6/textsearch/python/csrc/match.h`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/python/csrc/suffix_array.cc` & `fasttextsearch-0.6/textsearch/python/csrc/suffix_array.cc`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/python/csrc/suffix_array.h` & `fasttextsearch-0.6/textsearch/python/csrc/suffix_array.h`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/python/csrc/text_search.cc` & `fasttextsearch-0.6/textsearch/python/csrc/text_search.cc`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/python/csrc/utils.cc` & `fasttextsearch-0.6/textsearch/python/csrc/utils.cc`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/python/tests/CMakeLists.txt` & `fasttextsearch-0.6/textsearch/python/tests/CMakeLists.txt`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/python/tests/test_find_close_matches.py` & `fasttextsearch-0.6/textsearch/python/tests/test_find_close_matches.py`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/python/tests/test_levenshtein_distance.py` & `fasttextsearch-0.6/textsearch/python/tests/test_levenshtein_distance.py`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/python/tests/test_match.py` & `fasttextsearch-0.6/textsearch/python/tests/test_match.py`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/python/tests/test_row_ids_to_row_splits.py` & `fasttextsearch-0.6/textsearch/python/tests/test_row_ids_to_row_splits.py`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/python/tests/test_sourced_text.py` & `fasttextsearch-0.6/textsearch/python/tests/test_sourced_text.py`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/python/tests/test_suffix_array.py` & `fasttextsearch-0.6/textsearch/python/tests/test_suffix_array.py`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/python/tests/test_text_source.py` & `fasttextsearch-0.6/textsearch/python/tests/test_text_source.py`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/python/tests/test_transcript.py` & `fasttextsearch-0.6/textsearch/python/tests/test_transcript.py`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/python/textsearch/__init__.py` & `fasttextsearch-0.6/textsearch/python/textsearch/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -17,9 +17,9 @@
 
 from .suffix_array import create_suffix_array
 
 from .utils import AttributeDict
 from .utils import is_punctuation
 from .utils import row_ids_to_row_splits
 from .utils import str2bool
-__version__ = '0.51'
-__version__ = '0.51'
+__version__ = '0.6'
+__version__ = '0.6'
```

### Comparing `fasttextsearch-0.51/textsearch/python/textsearch/datatypes.py` & `fasttextsearch-0.6/textsearch/python/textsearch/datatypes.py`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/python/textsearch/levenshtein.py` & `fasttextsearch-0.6/textsearch/python/textsearch/levenshtein.py`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/python/textsearch/match.py` & `fasttextsearch-0.6/textsearch/python/textsearch/match.py`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/python/textsearch/suffix_array.py` & `fasttextsearch-0.6/textsearch/python/textsearch/suffix_array.py`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.51/textsearch/python/textsearch/utils.py` & `fasttextsearch-0.6/textsearch/python/textsearch/utils.py`

 * *Files identical despite different names*

