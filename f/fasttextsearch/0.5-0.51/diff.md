# Comparing `tmp/fasttextsearch-0.5.tar.gz` & `tmp/fasttextsearch-0.51.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "/ceph-kw/kangwei/code/text_search/dist/.tmp-ommy2sa7/fasttextsearch-0.5.tar", last modified: Sat Jun 24 07:37:05 2023, max compression
+gzip compressed data, was "fasttextsearch-0.51.tar", last modified: Sun Jul 23 09:32:08 2023, max compression
```

## Comparing `fasttextsearch-0.5.tar` & `fasttextsearch-0.51.tar`

### file list

```diff
@@ -1,80 +1,70 @@
-drwxr-xr-x   0 kangwei   (1092) root         (0)        0 2023-06-24 07:37:05.170072 fasttextsearch-0.5/
--rw-r--r--   0 kangwei   (1092) root         (0)     2277 2023-06-24 07:05:13.000000 fasttextsearch-0.5/CMakeLists.txt
--rw-r--r--   0 kangwei   (1092) root         (0)      143 2023-06-24 07:05:13.000000 fasttextsearch-0.5/MANIFEST.in
--rw-r--r--   0 kangwei   (1092) root         (0)     1169 2023-06-24 07:37:05.169072 fasttextsearch-0.5/PKG-INFO
--rw-r--r--   0 kangwei   (1092) root         (0)      577 2023-06-24 07:05:13.000000 fasttextsearch-0.5/README.md
-drwxr-xr-x   0 kangwei   (1092) root         (0)        0 2023-06-24 07:37:05.131072 fasttextsearch-0.5/cmake/
-drwxr-xr-x   0 kangwei   (1092) root         (0)        0 2023-06-24 07:37:05.133072 fasttextsearch-0.5/cmake/Modules/
-drwxr-xr-x   0 kangwei   (1092) root         (0)        0 2023-06-24 07:37:05.134072 fasttextsearch-0.5/cmake/Modules/FetchContent/
--rw-r--r--   0 kangwei   (1092) root         (0)      831 2023-02-18 07:20:27.000000 fasttextsearch-0.5/cmake/Modules/FetchContent/CMakeLists.cmake.in
--rw-r--r--   0 kangwei   (1092) root         (0)    38023 2023-02-18 07:20:27.000000 fasttextsearch-0.5/cmake/Modules/FetchContent.cmake
--rw-r--r--   0 kangwei   (1092) root         (0)      135 2023-02-18 07:20:27.000000 fasttextsearch-0.5/cmake/Modules/README.md
--rw-r--r--   0 kangwei   (1092) root         (0)        0 2023-02-18 07:20:27.000000 fasttextsearch-0.5/cmake/__init__.py
-drwxr-xr-x   0 kangwei   (1092) root         (0)        0 2023-06-24 07:37:05.134072 fasttextsearch-0.5/cmake/__pycache__/
--rw-r--r--   0 kangwei   (1092) root         (0)      142 2023-05-16 11:29:34.000000 fasttextsearch-0.5/cmake/__pycache__/__init__.cpython-38.pyc
--rw-r--r--   0 kangwei   (1092) root         (0)     3421 2023-03-31 03:33:51.000000 fasttextsearch-0.5/cmake/googletest.cmake
--rw-r--r--   0 kangwei   (1092) root         (0)     1800 2023-03-31 03:33:51.000000 fasttextsearch-0.5/cmake/pybind11.cmake
-drwxr-xr-x   0 kangwei   (1092) root         (0)        0 2023-06-24 07:37:05.139072 fasttextsearch-0.5/fasttextsearch.egg-info/
--rw-r--r--   0 kangwei   (1092) root         (0)     1169 2023-06-24 07:37:05.000000 fasttextsearch-0.5/fasttextsearch.egg-info/PKG-INFO
--rw-r--r--   0 kangwei   (1092) root         (0)     2399 2023-06-24 07:37:05.000000 fasttextsearch-0.5/fasttextsearch.egg-info/SOURCES.txt
--rw-r--r--   0 kangwei   (1092) root         (0)        1 2023-06-24 07:37:05.000000 fasttextsearch-0.5/fasttextsearch.egg-info/dependency_links.txt
--rw-r--r--   0 kangwei   (1092) root         (0)        6 2023-06-24 07:37:05.000000 fasttextsearch-0.5/fasttextsearch.egg-info/requires.txt
--rw-r--r--   0 kangwei   (1092) root         (0)       24 2023-06-24 07:37:05.000000 fasttextsearch-0.5/fasttextsearch.egg-info/top_level.txt
--rw-r--r--   0 kangwei   (1092) root         (0)      769 2023-06-24 07:05:13.000000 fasttextsearch-0.5/pyproject.toml
--rw-r--r--   0 kangwei   (1092) root         (0)        6 2023-05-16 07:33:05.000000 fasttextsearch-0.5/requirements.txt
--rw-r--r--   0 kangwei   (1092) root         (0)       38 2023-06-24 07:37:05.170072 fasttextsearch-0.5/setup.cfg
--rw-r--r--   0 kangwei   (1092) root         (0)     2986 2023-06-24 07:05:13.000000 fasttextsearch-0.5/setup.py
-drwxr-xr-x   0 kangwei   (1092) root         (0)        0 2023-06-24 07:37:05.139072 fasttextsearch-0.5/textsearch/
--rw-r--r--   0 kangwei   (1092) root         (0)       48 2023-02-18 12:05:47.000000 fasttextsearch-0.5/textsearch/CMakeLists.txt
-drwxr-xr-x   0 kangwei   (1092) root         (0)        0 2023-06-24 07:37:05.147072 fasttextsearch-0.5/textsearch/csrc/
--rw-r--r--   0 kangwei   (1092) root         (0)      695 2023-06-24 07:05:13.000000 fasttextsearch-0.5/textsearch/csrc/CMakeLists.txt
--rw-r--r--   0 kangwei   (1092) root         (0)    13272 2023-05-23 10:09:31.000000 fasttextsearch-0.5/textsearch/csrc/levenshtein.h
--rw-r--r--   0 kangwei   (1092) root         (0)     4137 2023-05-04 04:46:37.000000 fasttextsearch-0.5/textsearch/csrc/levenshtein_test.cc
--rw-r--r--   0 kangwei   (1092) root         (0)     4694 2023-06-24 07:06:12.000000 fasttextsearch-0.5/textsearch/csrc/match.cc
--rw-r--r--   0 kangwei   (1092) root         (0)     4611 2023-05-04 04:46:37.000000 fasttextsearch-0.5/textsearch/csrc/match.h
--rw-r--r--   0 kangwei   (1092) root         (0)     3248 2023-05-04 04:46:37.000000 fasttextsearch-0.5/textsearch/csrc/match_test.cc
--rw-r--r--   0 kangwei   (1092) root         (0)     5273 2023-04-12 07:57:56.000000 fasttextsearch-0.5/textsearch/csrc/suffix_array.cc
--rw-r--r--   0 kangwei   (1092) root         (0)     3207 2023-03-31 03:33:51.000000 fasttextsearch-0.5/textsearch/csrc/suffix_array.h
--rw-r--r--   0 kangwei   (1092) root         (0)     3883 2023-04-24 11:25:03.000000 fasttextsearch-0.5/textsearch/csrc/suffix_array_test.cc
--rw-r--r--   0 kangwei   (1092) root         (0)     2880 2023-04-24 11:25:03.000000 fasttextsearch-0.5/textsearch/csrc/utils.cc
--rw-r--r--   0 kangwei   (1092) root         (0)     3508 2023-04-24 11:25:03.000000 fasttextsearch-0.5/textsearch/csrc/utils.h
--rw-r--r--   0 kangwei   (1092) root         (0)     4862 2023-04-24 11:25:03.000000 fasttextsearch-0.5/textsearch/csrc/utils_test.cc
-drwxr-xr-x   0 kangwei   (1092) root         (0)        0 2023-06-24 07:37:05.147072 fasttextsearch-0.5/textsearch/python/
--rw-r--r--   0 kangwei   (1092) root         (0)       78 2023-06-24 07:05:13.000000 fasttextsearch-0.5/textsearch/python/CMakeLists.txt
-drwxr-xr-x   0 kangwei   (1092) root         (0)        0 2023-06-24 07:37:05.154072 fasttextsearch-0.5/textsearch/python/csrc/
--rw-r--r--   0 kangwei   (1092) root         (0)      169 2023-06-24 07:05:13.000000 fasttextsearch-0.5/textsearch/python/csrc/CMakeLists.txt
--rw-r--r--   0 kangwei   (1092) root         (0)     5003 2023-06-24 07:06:12.000000 fasttextsearch-0.5/textsearch/python/csrc/levenshtein.cc
--rw-r--r--   0 kangwei   (1092) root         (0)      985 2023-03-06 09:09:29.000000 fasttextsearch-0.5/textsearch/python/csrc/levenshtein.h
--rw-r--r--   0 kangwei   (1092) root         (0)     1850 2023-05-04 04:46:37.000000 fasttextsearch-0.5/textsearch/python/csrc/match.cc
--rw-r--r--   0 kangwei   (1092) root         (0)      961 2023-05-04 04:46:37.000000 fasttextsearch-0.5/textsearch/python/csrc/match.h
--rw-r--r--   0 kangwei   (1092) root         (0)     1637 2023-04-13 03:32:42.000000 fasttextsearch-0.5/textsearch/python/csrc/suffix_array.cc
--rw-r--r--   0 kangwei   (1092) root         (0)      988 2023-03-06 09:09:29.000000 fasttextsearch-0.5/textsearch/python/csrc/suffix_array.h
--rw-r--r--   0 kangwei   (1092) root         (0)      564 2023-06-24 07:05:13.000000 fasttextsearch-0.5/textsearch/python/csrc/text_search.cc
--rw-r--r--   0 kangwei   (1092) root         (0)      357 2023-03-31 03:33:51.000000 fasttextsearch-0.5/textsearch/python/csrc/text_search.h
--rw-r--r--   0 kangwei   (1092) root         (0)     4599 2023-04-24 11:25:03.000000 fasttextsearch-0.5/textsearch/python/csrc/utils.cc
--rw-r--r--   0 kangwei   (1092) root         (0)      318 2023-04-21 06:51:44.000000 fasttextsearch-0.5/textsearch/python/csrc/utils.h
-drwxr-xr-x   0 kangwei   (1092) root         (0)        0 2023-06-24 07:37:05.160072 fasttextsearch-0.5/textsearch/python/tests/
--rw-r--r--   0 kangwei   (1092) root         (0)      848 2023-06-24 07:05:13.000000 fasttextsearch-0.5/textsearch/python/tests/CMakeLists.txt
--rwxr-xr-x   0 kangwei   (1092) root         (0)     4748 2023-04-24 11:25:03.000000 fasttextsearch-0.5/textsearch/python/tests/test_find_close_matches.py
--rwxr-xr-x   0 kangwei   (1092) root         (0)     1943 2023-04-13 03:32:42.000000 fasttextsearch-0.5/textsearch/python/tests/test_levenshtein_distance.py
--rwxr-xr-x   0 kangwei   (1092) root         (0)     1414 2023-05-04 04:46:37.000000 fasttextsearch-0.5/textsearch/python/tests/test_match.py
--rwxr-xr-x   0 kangwei   (1092) root         (0)      950 2023-03-31 03:33:51.000000 fasttextsearch-0.5/textsearch/python/tests/test_row_ids_to_row_splits.py
--rwxr-xr-x   0 kangwei   (1092) root         (0)    10687 2023-04-13 03:32:42.000000 fasttextsearch-0.5/textsearch/python/tests/test_sourced_text.py
--rwxr-xr-x   0 kangwei   (1092) root         (0)     1359 2023-04-24 11:25:03.000000 fasttextsearch-0.5/textsearch/python/tests/test_suffix_array.py
--rwxr-xr-x   0 kangwei   (1092) root         (0)     2007 2023-03-31 03:33:51.000000 fasttextsearch-0.5/textsearch/python/tests/test_text_source.py
--rwxr-xr-x   0 kangwei   (1092) root         (0)     2314 2023-03-31 03:33:51.000000 fasttextsearch-0.5/textsearch/python/tests/test_transcript.py
-drwxr-xr-x   0 kangwei   (1092) root         (0)        0 2023-06-24 07:37:05.164072 fasttextsearch-0.5/textsearch/python/textsearch/
--rw-r--r--   0 kangwei   (1092) root         (0)      751 2023-06-24 07:37:05.000000 fasttextsearch-0.5/textsearch/python/textsearch/__init__.py
-drwxr-xr-x   0 kangwei   (1092) root         (0)        0 2023-06-24 07:37:05.169072 fasttextsearch-0.5/textsearch/python/textsearch/__pycache__/
--rw-r--r--   0 kangwei   (1092) root         (0)      948 2023-05-18 08:42:24.000000 fasttextsearch-0.5/textsearch/python/textsearch/__pycache__/__init__.cpython-38.pyc
--rw-r--r--   0 kangwei   (1092) root         (0)     8961 2023-05-05 09:46:59.000000 fasttextsearch-0.5/textsearch/python/textsearch/__pycache__/datatypes.cpython-38.pyc
--rw-r--r--   0 kangwei   (1092) root         (0)     2543 2023-05-05 09:46:59.000000 fasttextsearch-0.5/textsearch/python/textsearch/__pycache__/levenshtein.cpython-38.pyc
--rw-r--r--   0 kangwei   (1092) root         (0)    23181 2023-05-24 04:44:55.000000 fasttextsearch-0.5/textsearch/python/textsearch/__pycache__/match.cpython-38.pyc
--rw-r--r--   0 kangwei   (1092) root         (0)     5139 2023-05-18 08:42:24.000000 fasttextsearch-0.5/textsearch/python/textsearch/__pycache__/suffix_array.cpython-38.pyc
--rw-r--r--   0 kangwei   (1092) root         (0)     2910 2023-04-13 07:06:10.000000 fasttextsearch-0.5/textsearch/python/textsearch/__pycache__/text_search.cpython-38.pyc
--rw-r--r--   0 kangwei   (1092) root         (0)     3328 2023-05-18 08:42:24.000000 fasttextsearch-0.5/textsearch/python/textsearch/__pycache__/utils.cpython-38.pyc
--rw-r--r--   0 kangwei   (1092) root         (0)    12992 2023-04-24 11:25:03.000000 fasttextsearch-0.5/textsearch/python/textsearch/datatypes.py
--rw-r--r--   0 kangwei   (1092) root         (0)     3594 2023-04-24 11:25:03.000000 fasttextsearch-0.5/textsearch/python/textsearch/levenshtein.py
--rw-r--r--   0 kangwei   (1092) root         (0)    40868 2023-06-24 07:06:12.000000 fasttextsearch-0.5/textsearch/python/textsearch/match.py
--rw-r--r--   0 kangwei   (1092) root         (0)     6695 2023-06-24 07:05:13.000000 fasttextsearch-0.5/textsearch/python/textsearch/suffix_array.py
--rw-r--r--   0 kangwei   (1092) root         (0)     3165 2023-06-24 07:05:13.000000 fasttextsearch-0.5/textsearch/python/textsearch/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:32:08.427174 fasttextsearch-0.51/
+-rw-r--r--   0 runner    (1001) docker     (123)     2278 2023-07-23 09:28:52.000000 fasttextsearch-0.51/CMakeLists.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      143 2023-07-23 09:28:52.000000 fasttextsearch-0.51/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     1170 2023-07-23 09:32:08.427174 fasttextsearch-0.51/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      577 2023-07-23 09:28:52.000000 fasttextsearch-0.51/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:32:08.419174 fasttextsearch-0.51/cmake/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:32:08.419174 fasttextsearch-0.51/cmake/Modules/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:32:08.423174 fasttextsearch-0.51/cmake/Modules/FetchContent/
+-rw-r--r--   0 runner    (1001) docker     (123)      831 2023-07-23 09:28:52.000000 fasttextsearch-0.51/cmake/Modules/FetchContent/CMakeLists.cmake.in
+-rw-r--r--   0 runner    (1001) docker     (123)    38023 2023-07-23 09:28:52.000000 fasttextsearch-0.51/cmake/Modules/FetchContent.cmake
+-rw-r--r--   0 runner    (1001) docker     (123)      135 2023-07-23 09:28:52.000000 fasttextsearch-0.51/cmake/Modules/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 09:28:52.000000 fasttextsearch-0.51/cmake/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3421 2023-07-23 09:28:52.000000 fasttextsearch-0.51/cmake/googletest.cmake
+-rw-r--r--   0 runner    (1001) docker     (123)     1800 2023-07-23 09:28:52.000000 fasttextsearch-0.51/cmake/pybind11.cmake
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:32:08.423174 fasttextsearch-0.51/fasttextsearch.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1170 2023-07-23 09:32:08.000000 fasttextsearch-0.51/fasttextsearch.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1897 2023-07-23 09:32:08.000000 fasttextsearch-0.51/fasttextsearch.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 09:32:08.000000 fasttextsearch-0.51/fasttextsearch.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        6 2023-07-23 09:32:08.000000 fasttextsearch-0.51/fasttextsearch.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       24 2023-07-23 09:32:08.000000 fasttextsearch-0.51/fasttextsearch.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      801 2023-07-23 09:28:52.000000 fasttextsearch-0.51/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)        6 2023-07-23 09:28:52.000000 fasttextsearch-0.51/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 09:32:08.427174 fasttextsearch-0.51/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     2986 2023-07-23 09:28:52.000000 fasttextsearch-0.51/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:32:08.423174 fasttextsearch-0.51/textsearch/
+-rw-r--r--   0 runner    (1001) docker     (123)       48 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/CMakeLists.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:32:08.423174 fasttextsearch-0.51/textsearch/csrc/
+-rw-r--r--   0 runner    (1001) docker     (123)      695 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/csrc/CMakeLists.txt
+-rw-r--r--   0 runner    (1001) docker     (123)    13272 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/csrc/levenshtein.h
+-rw-r--r--   0 runner    (1001) docker     (123)     4137 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/csrc/levenshtein_test.cc
+-rw-r--r--   0 runner    (1001) docker     (123)     4694 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/csrc/match.cc
+-rw-r--r--   0 runner    (1001) docker     (123)     4611 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/csrc/match.h
+-rw-r--r--   0 runner    (1001) docker     (123)     3248 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/csrc/match_test.cc
+-rw-r--r--   0 runner    (1001) docker     (123)     5273 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/csrc/suffix_array.cc
+-rw-r--r--   0 runner    (1001) docker     (123)     3207 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/csrc/suffix_array.h
+-rw-r--r--   0 runner    (1001) docker     (123)     3883 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/csrc/suffix_array_test.cc
+-rw-r--r--   0 runner    (1001) docker     (123)     2880 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/csrc/utils.cc
+-rw-r--r--   0 runner    (1001) docker     (123)     3508 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/csrc/utils.h
+-rw-r--r--   0 runner    (1001) docker     (123)     4862 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/csrc/utils_test.cc
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:32:08.423174 fasttextsearch-0.51/textsearch/python/
+-rw-r--r--   0 runner    (1001) docker     (123)       78 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/CMakeLists.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:32:08.423174 fasttextsearch-0.51/textsearch/python/csrc/
+-rw-r--r--   0 runner    (1001) docker     (123)      169 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/csrc/CMakeLists.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     5003 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/csrc/levenshtein.cc
+-rw-r--r--   0 runner    (1001) docker     (123)      985 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/csrc/levenshtein.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1850 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/csrc/match.cc
+-rw-r--r--   0 runner    (1001) docker     (123)      961 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/csrc/match.h
+-rw-r--r--   0 runner    (1001) docker     (123)     1637 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/csrc/suffix_array.cc
+-rw-r--r--   0 runner    (1001) docker     (123)      988 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/csrc/suffix_array.h
+-rw-r--r--   0 runner    (1001) docker     (123)      564 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/csrc/text_search.cc
+-rw-r--r--   0 runner    (1001) docker     (123)      357 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/csrc/text_search.h
+-rw-r--r--   0 runner    (1001) docker     (123)     4599 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/csrc/utils.cc
+-rw-r--r--   0 runner    (1001) docker     (123)      318 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/csrc/utils.h
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:32:08.427174 fasttextsearch-0.51/textsearch/python/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)      848 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/tests/CMakeLists.txt
+-rwxr-xr-x   0 runner    (1001) docker     (123)     4748 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/tests/test_find_close_matches.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     1943 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/tests/test_levenshtein_distance.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     1414 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/tests/test_match.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)      950 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/tests/test_row_ids_to_row_splits.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)    10687 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/tests/test_sourced_text.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     1359 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/tests/test_suffix_array.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     2007 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/tests/test_text_source.py
+-rwxr-xr-x   0 runner    (1001) docker     (123)     2314 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/tests/test_transcript.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 09:32:08.427174 fasttextsearch-0.51/textsearch/python/textsearch/
+-rw-r--r--   0 runner    (1001) docker     (123)      740 2023-07-23 09:32:08.000000 fasttextsearch-0.51/textsearch/python/textsearch/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13469 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/textsearch/datatypes.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3606 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/textsearch/levenshtein.py
+-rw-r--r--   0 runner    (1001) docker     (123)    52271 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/textsearch/match.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3208 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/textsearch/suffix_array.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5269 2023-07-23 09:28:52.000000 fasttextsearch-0.51/textsearch/python/textsearch/utils.py
```

### Comparing `fasttextsearch-0.5/CMakeLists.txt` & `fasttextsearch-0.51/CMakeLists.txt`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 cmake_minimum_required(VERSION 3.8 FATAL_ERROR)
 project(textsearch)
 
-set(TS_VERSION "0.5")
+set(TS_VERSION "0.51")
 
 set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/lib")
 set(CMAKE_LIBRARY_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/lib")
 set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin")
 
 set(CMAKE_SKIP_BUILD_RPATH FALSE)
 set(BUILD_RPATH_USE_ORIGIN TRUE)
```

### Comparing `fasttextsearch-0.5/PKG-INFO` & `fasttextsearch-0.51/PKG-INFO`

 * *Files 27% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: fasttextsearch
-Version: 0.5
+Version: 0.51
 Summary: Some fast-ish algorithms for batch text search in moderate-sized collections, intended for data cleanup.
 Author-email: Next-gen Kaldi development team <wkang.pku@gmail.com>
 Project-URL: Homepage, https://github.com/k2-fsa/text_search
 Project-URL: Bug Tracker, https://github.com/k2-fsa/text_search/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Operating System :: OS Independent
```

### Comparing `fasttextsearch-0.5/README.md` & `fasttextsearch-0.51/README.md`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/cmake/Modules/FetchContent/CMakeLists.cmake.in` & `fasttextsearch-0.51/cmake/Modules/FetchContent/CMakeLists.cmake.in`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/cmake/Modules/FetchContent.cmake` & `fasttextsearch-0.51/cmake/Modules/FetchContent.cmake`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/cmake/googletest.cmake` & `fasttextsearch-0.51/cmake/googletest.cmake`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/cmake/pybind11.cmake` & `fasttextsearch-0.51/cmake/pybind11.cmake`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/fasttextsearch.egg-info/PKG-INFO` & `fasttextsearch-0.51/fasttextsearch.egg-info/PKG-INFO`

 * *Files 27% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: fasttextsearch
-Version: 0.5
+Version: 0.51
 Summary: Some fast-ish algorithms for batch text search in moderate-sized collections, intended for data cleanup.
 Author-email: Next-gen Kaldi development team <wkang.pku@gmail.com>
 Project-URL: Homepage, https://github.com/k2-fsa/text_search
 Project-URL: Bug Tracker, https://github.com/k2-fsa/text_search/issues
 Classifier: Programming Language :: Python :: 3
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Operating System :: OS Independent
```

### Comparing `fasttextsearch-0.5/fasttextsearch.egg-info/SOURCES.txt` & `fasttextsearch-0.51/fasttextsearch.egg-info/SOURCES.txt`

 * *Files 6% similar despite different names*

```diff
@@ -6,15 +6,14 @@
 setup.py
 cmake/__init__.py
 cmake/googletest.cmake
 cmake/pybind11.cmake
 cmake/Modules/FetchContent.cmake
 cmake/Modules/README.md
 cmake/Modules/FetchContent/CMakeLists.cmake.in
-cmake/__pycache__/__init__.cpython-38.pyc
 fasttextsearch.egg-info/PKG-INFO
 fasttextsearch.egg-info/SOURCES.txt
 fasttextsearch.egg-info/dependency_links.txt
 fasttextsearch.egg-info/requires.txt
 fasttextsearch.egg-info/top_level.txt
 textsearch/CMakeLists.txt
 textsearch/csrc/CMakeLists.txt
@@ -51,15 +50,8 @@
 textsearch/python/tests/test_text_source.py
 textsearch/python/tests/test_transcript.py
 textsearch/python/textsearch/__init__.py
 textsearch/python/textsearch/datatypes.py
 textsearch/python/textsearch/levenshtein.py
 textsearch/python/textsearch/match.py
 textsearch/python/textsearch/suffix_array.py
-textsearch/python/textsearch/utils.py
-textsearch/python/textsearch/__pycache__/__init__.cpython-38.pyc
-textsearch/python/textsearch/__pycache__/datatypes.cpython-38.pyc
-textsearch/python/textsearch/__pycache__/levenshtein.cpython-38.pyc
-textsearch/python/textsearch/__pycache__/match.cpython-38.pyc
-textsearch/python/textsearch/__pycache__/suffix_array.cpython-38.pyc
-textsearch/python/textsearch/__pycache__/text_search.cpython-38.pyc
-textsearch/python/textsearch/__pycache__/utils.cpython-38.pyc
+textsearch/python/textsearch/utils.py
```

### Comparing `fasttextsearch-0.5/pyproject.toml` & `fasttextsearch-0.51/pyproject.toml`

 * *Files 7% similar despite different names*

```diff
@@ -6,15 +6,15 @@
     "cmake>=3.8",
 ]
 build-backend = "setuptools.build_meta"
 
 
 [project]
 name = "fasttextsearch"
-version = "0.5"
+version = "0.51"
 authors = [
   { name="Next-gen Kaldi development team", email="wkang.pku@gmail.com" },
 ]
 description="Some fast-ish algorithms for batch text search in moderate-sized collections, intended for data cleanup."
 dependencies = [
   "numpy",
 ]
@@ -26,9 +26,12 @@
     "Operating System :: OS Independent",
 ]
 
 [project.urls]
 "Homepage" = "https://github.com/k2-fsa/text_search"
 "Bug Tracker" = "https://github.com/k2-fsa/text_search/issues"
 
+[tool.black]
+line-length = 80
+
```

### Comparing `fasttextsearch-0.5/setup.py` & `fasttextsearch-0.51/setup.py`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/textsearch/csrc/CMakeLists.txt` & `fasttextsearch-0.51/textsearch/csrc/CMakeLists.txt`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/textsearch/csrc/levenshtein.h` & `fasttextsearch-0.51/textsearch/csrc/levenshtein.h`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/textsearch/csrc/levenshtein_test.cc` & `fasttextsearch-0.51/textsearch/csrc/levenshtein_test.cc`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/textsearch/csrc/match.cc` & `fasttextsearch-0.51/textsearch/csrc/match.cc`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/textsearch/csrc/match.h` & `fasttextsearch-0.51/textsearch/csrc/match.h`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/textsearch/csrc/match_test.cc` & `fasttextsearch-0.51/textsearch/csrc/match_test.cc`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/textsearch/csrc/suffix_array.cc` & `fasttextsearch-0.51/textsearch/csrc/suffix_array.cc`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/textsearch/csrc/suffix_array.h` & `fasttextsearch-0.51/textsearch/csrc/suffix_array.h`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/textsearch/csrc/suffix_array_test.cc` & `fasttextsearch-0.51/textsearch/csrc/suffix_array_test.cc`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/textsearch/csrc/utils.cc` & `fasttextsearch-0.51/textsearch/csrc/utils.cc`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/textsearch/csrc/utils.h` & `fasttextsearch-0.51/textsearch/csrc/utils.h`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/textsearch/csrc/utils_test.cc` & `fasttextsearch-0.51/textsearch/csrc/utils_test.cc`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/textsearch/python/csrc/levenshtein.cc` & `fasttextsearch-0.51/textsearch/python/csrc/levenshtein.cc`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/textsearch/python/csrc/levenshtein.h` & `fasttextsearch-0.51/textsearch/python/csrc/levenshtein.h`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/textsearch/python/csrc/match.cc` & `fasttextsearch-0.51/textsearch/python/csrc/match.cc`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/textsearch/python/csrc/match.h` & `fasttextsearch-0.51/textsearch/python/csrc/match.h`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/textsearch/python/csrc/suffix_array.cc` & `fasttextsearch-0.51/textsearch/python/csrc/suffix_array.cc`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/textsearch/python/csrc/suffix_array.h` & `fasttextsearch-0.51/textsearch/python/csrc/suffix_array.h`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/textsearch/python/csrc/text_search.cc` & `fasttextsearch-0.51/textsearch/python/csrc/text_search.cc`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/textsearch/python/csrc/utils.cc` & `fasttextsearch-0.51/textsearch/python/csrc/utils.cc`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/textsearch/python/tests/CMakeLists.txt` & `fasttextsearch-0.51/textsearch/python/tests/CMakeLists.txt`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/textsearch/python/tests/test_find_close_matches.py` & `fasttextsearch-0.51/textsearch/python/tests/test_find_close_matches.py`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/textsearch/python/tests/test_levenshtein_distance.py` & `fasttextsearch-0.51/textsearch/python/tests/test_levenshtein_distance.py`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/textsearch/python/tests/test_match.py` & `fasttextsearch-0.51/textsearch/python/tests/test_match.py`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/textsearch/python/tests/test_row_ids_to_row_splits.py` & `fasttextsearch-0.51/textsearch/python/tests/test_row_ids_to_row_splits.py`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/textsearch/python/tests/test_sourced_text.py` & `fasttextsearch-0.51/textsearch/python/tests/test_sourced_text.py`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/textsearch/python/tests/test_suffix_array.py` & `fasttextsearch-0.51/textsearch/python/tests/test_suffix_array.py`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/textsearch/python/tests/test_text_source.py` & `fasttextsearch-0.51/textsearch/python/tests/test_text_source.py`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/textsearch/python/tests/test_transcript.py` & `fasttextsearch-0.51/textsearch/python/tests/test_transcript.py`

 * *Files identical despite different names*

### Comparing `fasttextsearch-0.5/textsearch/python/textsearch/__init__.py` & `fasttextsearch-0.51/textsearch/python/textsearch/__init__.py`

 * *Files 19% similar despite different names*

```diff
@@ -7,19 +7,19 @@
 from .datatypes import Transcript
 from .datatypes import append_texts
 from .datatypes import filter_texts
 from .datatypes import texts_to_sourced_texts
 
 from .levenshtein import get_nice_alignments
 
-from .match import get_alignments
+from .match import align_queries
 from .match import get_longest_increasing_pairs
-from .match import find_candidate_matches
-from .match import split_into_segments
+from .match import split_aligned_queries
 
 from .suffix_array import create_suffix_array
 
 from .utils import AttributeDict
 from .utils import is_punctuation
 from .utils import row_ids_to_row_splits
-__version__ = '0.5'
-__version__ = '0.5'
+from .utils import str2bool
+__version__ = '0.51'
+__version__ = '0.51'
```

### Comparing `fasttextsearch-0.5/textsearch/python/textsearch/datatypes.py` & `fasttextsearch-0.51/textsearch/python/textsearch/datatypes.py`

 * *Files 3% similar despite different names*

```diff
@@ -29,25 +29,32 @@
 
     # Only used when binary_text.dtype is np.int32.
     # It contains the mapping from utf-8 character position to byte position.
     # That is pos[i] contains the byte position in binary_text for the i-th
     # utf-8 character
     pos: Optional[np.ndarray] = None
 
+    # Whether has punctuation in this TextSource, if True we will only
+    # break the query at punctuation position when splitting aligned segment
+    # into smaller pieces.
+    has_punctuation: bool = False
+
     @property
     def text(self) -> str:
         """Return Python string representation of self.binary_text decoded as UTF-8."""
         if self.binary_text.dtype == np.uint8:
             return self.binary_text.tobytes().decode("utf-8")
         else:
             assert self.binary_text.dtype == np.int32, self.binary_text.dtype
             return "".join([chr(i) for i in self.binary_text])
 
     @staticmethod
-    def from_str(name: str, s: str, use_utf8: bool) -> "TextSource":
+    def from_str(
+        name: str, s: str, use_utf8: bool, has_punctuation: bool = False
+    ) -> "TextSource":
         """Construct an instance of TextSource from a string.
 
         Args:
           name:
             Name of the returned instance. It can be either a filename or an ID.
           s:
             It contains the text string.
@@ -58,23 +65,27 @@
 
         if use_utf8:
             binary_text = s.encode("utf-8")
             return TextSource(
                 name=name,
                 binary_text=np.frombuffer(binary_text, dtype=np.uint8),
                 pos=None,
+                has_punctuation=has_punctuation,
             )
         else:
-            binary_text = np.fromiter((ord(i) for i in s), dtype=np.int32, count=len(s))
+            binary_text = np.fromiter(
+                (ord(i) for i in s), dtype=np.int32, count=len(s)
+            )
             pos = _find_byte_offsets_for_utf8_symbols(binary_text)
 
             return TextSource(
                 name=name,
                 binary_text=binary_text,
                 pos=pos,
+                has_punctuation=has_punctuation,
             )
 
 
 def _find_byte_offsets_for_utf8_symbols(binary_text: np.ndarray) -> np.ndarray:
     """
     Args:
       binary_text:
@@ -180,15 +191,18 @@
 
                 b = text.encode("utf-8")
 
                 if time_list:
                     # Check that begin_time is non-decreasing.
                     #
                     # < here requires that it is strictly increasing.
-                    assert time_list[-1] < begin_time, (time_list[-1], begin_time)
+                    assert time_list[-1] < begin_time, (
+                        time_list[-1],
+                        begin_time,
+                    )
 
                 # bytes belonging to the same text have the same begin time
                 time_list += [begin_time] * len(b)
                 byte_list.append(b)
 
             return Transcript(
                 name=name,
@@ -203,15 +217,18 @@
 
                 codepoint_list.append(ord(i) for i in text)
 
                 if time_list:
                     # Check that begin_time is non-decreasing.
                     #
                     # < here requires that it is strictly increasing.
-                    assert time_list[-1] < begin_time, (time_list[-1], begin_time)
+                    assert time_list[-1] < begin_time, (
+                        time_list[-1],
+                        begin_time,
+                    )
 
                 # bytes belonging to the same text have the same begin time
                 # Each character occupies 4 bytes, so it is multiplied by 4
                 time_list += [begin_time] * (len(text) * 4)
 
             return Transcript(
                 name=name,
@@ -342,18 +359,15 @@
 
     doc = np.concatenate(doc_list)
     assert doc.dtype == np.uint32, doc.dtype
 
     sources = [s for t in texts for s in t.sources]
 
     return SourcedText(
-        binary_text=binary_text,
-        pos=pos,
-        doc=doc,
-        sources=sources,
+        binary_text=binary_text, pos=pos, doc=doc, sources=sources,
     )
 
 
 def filter_texts(
     t: SourcedText,
     fn: Optional[Callable[[Union[np.int32, np.uint8]], bool]] = None,
     keep: Optional[np.ndarray] = None,
@@ -382,12 +396,9 @@
     new2old = keep.nonzero()[0]
     binary_text = t.binary_text[new2old]
     pos = t.pos[new2old]
     doc = t.doc
     if not isinstance(t.doc, int):
         doc = t.doc[new2old]
     return SourcedText(
-        binary_text=binary_text,
-        pos=pos,
-        doc=doc,
-        sources=t.sources,
+        binary_text=binary_text, pos=pos, doc=doc, sources=t.sources,
     )
```

### Comparing `fasttextsearch-0.5/textsearch/python/textsearch/levenshtein.py` & `fasttextsearch-0.51/textsearch/python/textsearch/levenshtein.py`

 * *Files 6% similar despite different names*

```diff
@@ -15,15 +15,17 @@
 # limitations under the License.
 
 import numpy as np
 from typing import List, Tuple
 
 
 def get_nice_alignments(
-    alignments: List[Tuple[int, int, str]], query: np.ndarray, target: np.ndarray
+    alignments: List[Tuple[int, int, str]],
+    query: np.ndarray,
+    target: np.ndarray,
 ) -> List[str]:
     """
     Get the alignment of the matched segments.
 
     Args:
       alignments:
         The alignments information returned by the :func:`levenshtein_distance`.
@@ -37,16 +39,16 @@
       See the following example for more details, the first line of the alignment
       is query, the second line is the error types, the third line is the target
       segment. The following symbols are used to represent the error types:
 
         - ``*``: empty
         - ``+``: insertion
         - ``-``: deletion
-        - ``#``: replacement
-        - ``|``: equal.
+        - ``#``: substitution
+        - ``|``: correct.
 
     **Example 1/2**
 
     >>> from textsearch import get_nice_alignments, levenshtein_distance
     >>> import numpy as np
     >>> query = np.array([1, 2, 3, 4], dtype=np.int32)
     >>> target = np.array([1, 5, 3, 4, 6, 7, 1, 2, 4], dtype=np.int32)
```

### Comparing `fasttextsearch-0.5/textsearch/python/textsearch/match.py` & `fasttextsearch-0.51/textsearch/python/textsearch/match.py`

 * *Files 18% similar despite different names*

```diff
@@ -12,23 +12,26 @@
 # distributed under the License is distributed on an "AS IS" BASIS,
 # WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 # See the License for the specific language governing permissions and
 # limitations under the License.
 
 import logging
 import math
-from bisect import bisect_left
+from bisect import bisect_left, bisect_right
 from dataclasses import dataclass
 from heapq import heappush, heappop
+from multiprocessing.pool import Pool
 from multiprocessing.pool import ThreadPool
 from typing import Any, Dict, List, Optional, Tuple, Union
 
 import numpy as np
+import regex
 
 from _textsearch import (
+    find_close_matches,
     get_longest_increasing_pairs as _get_longest_increasing_pairs,
     levenshtein_distance,
 )
 from .suffix_array import create_suffix_array
 from .datatypes import SourcedText, TextSource, Transcript
 from .utils import is_overlap, is_punctuation, row_ids_to_row_splits
 
@@ -71,16 +74,16 @@
 def _break_query(
     sourced_text: SourcedText,
     matched_points: List[Tuple[int, int]],
     segment_length: int = 5000,
     reference_length_difference: float = 0.1,
 ) -> List[Tuple[int, int, int, int]]:
     """
-    Break long query into small segments at the matched points with the `segment_length`
-    constraint.
+    Break long query into small segments at the matched points with the
+    `segment_length` constraint.
 
     Args:
       sourced_text:
         The SourcedText containing the queries and references.
       matched_points:
         A list of matched points, each item is a pair of (query index, target index)
         in sourced_text.
@@ -94,52 +97,60 @@
         `len(query) * (1 - reference_length_difference / 2)` to
         `len(query) * (1 + reference_length_difference / 2)`.
     """
     # Firstly we will find the longest range that satisfies
     # 1 - reference_length_difference / 2 <= len(reference) / len(query)
     # <= 1 + reference_length_difference / 2
     prev_break_point = 0  # index in matched_points
-    candidate_ranges: List[Tuple[int, int]] = []  # start, end indexes in matched_points
+    candidate_ranges: List[
+        Tuple[int, int]
+    ] = []  # start, end indexes in matched_points
     for i in range(1, len(matched_points)):
-        # The query and reference distance between current matched_point and preceding
-        # matched_point.
+        # The query and reference distance between current matched_point and
+        # preceding matched_point.
         gap = (
             matched_points[i][0] - matched_points[i - 1][0],
             matched_points[i][1] - matched_points[i - 1][1],
         )
         if gap[0] < gap[1]:
             # +1 for smoothing (avoid div zero error)
-            ratio = (matched_points[i][1] - matched_points[prev_break_point][1] + 1) / (
-                matched_points[i][0] - matched_points[prev_break_point][0] + 1
-            )
+            ratio = (
+                matched_points[i][1] - matched_points[prev_break_point][1] + 1
+            ) / (matched_points[i][0] - matched_points[prev_break_point][0] + 1)
             # break on current matched_point, we will finally choose the longest
             # segment.
             half = reference_length_difference / 2
             if ratio < 1 - half or ratio > 1 + half:
                 candidate_ranges.append((prev_break_point, i))
                 prev_break_point = i
 
     candidate_ranges.append((prev_break_point, len(matched_points)))
 
     # Find the range containing the longest query sequence
-    # max_item contains the matched points we choose : matched_points[max_item[0], max_item[1]]
+    # max_item contains the matched points we choose :
+    # matched_points[max_item[0], max_item[1]]
     max_length = -1
     max_item = (0, len(matched_points))
     for c in candidate_ranges:
         current_length = matched_points[c[1] - 1][0] - matched_points[c[0]][0]
         if current_length > max_length:
             max_length = current_length
             max_item = c
 
     # start, end indexes of query and reference in sourced_text
     # [(query_start, query_end, target_start, target_end)]
     segments: List[Tuple[int, int, int, int]] = []
 
     def add_segments(
-        query_start, query_end, target_start, target_end, segment_length, segments
+        query_start,
+        query_end,
+        target_start,
+        target_end,
+        segment_length,
+        segments,
     ):
         num_chunk = (query_end - query_start) // segment_length
         if num_chunk > 0:
             for i in range(num_chunk):
                 real_target_end = (
                     target_start + segment_length
                     if target_start + segment_length < target_end
@@ -151,16 +162,16 @@
                         query_start + segment_length,
                         target_start,
                         real_target_end,
                     )
                 )
                 query_start += segment_length
                 target_start += segment_length
-        # if the remaining part is smaller than segment_length // 4, we will append
-        # it to the last segment rather than creating a new segment.
+        # if the remaining part is smaller than segment_length // 4, we will
+        # append it to the last segment rather than creating a new segment.
         if segments and query_end - query_start < segment_length // 4:
             segments[-1] = (
                 segments[-1][0],
                 query_end,
                 segments[-1][2],
                 target_end,
             )
@@ -213,47 +224,44 @@
                     segments,
                 )
 
     query_start, target_start = prev_break_point
     query_end = next_query_base
 
     target_end = target_start + (query_end - query_start)
-    target_end = target_end if target_end <= next_target_base else next_target_base
+    target_end = (
+        target_end if target_end <= next_target_base else next_target_base
+    )
 
     if query_end - query_start < segment_length // 4:
         if segments:
             segments[-1] = (
                 segments[-1][0],
                 query_end,
                 segments[-1][2],
                 target_end,
             )
         else:
-            segments.append(
-                (
-                    query_start,
-                    query_end,
-                    target_start,
-                    target_end,
-                )
-            )
+            segments.append((query_start, query_end, target_start, target_end,))
     else:
         add_segments(
             query_start,
             query_end,
             target_start,
             target_end,
             segment_length,
             segments,
         )
     return segments
 
 
 def _combine_sub_alignments(
-    sourced_text: SourcedText, sub_alignments: List[Dict[str, Any]], num_queries: int
+    sourced_text: SourcedText,
+    sub_alignments: List[Dict[str, Any]],
+    num_queries: int,
 ) -> List[Tuple[Tuple[int, int], List[Dict[str, Any]]]]:
     """
     Combine the segments broken by `_break_query` together to get a long query.
 
     Note: The segments here contain the levenshtein alignment.
 
     Args:
@@ -262,20 +270,22 @@
       sub_alignments:
         A list of segments, each item (returned by levenshtein_worker) contains
         the segment it belongs to and the levenshtein alignment.
       num_queries:
         The number of queries, this argument is for efficiency, if we know number
         of queries we can preallocate the list.
     Returns:
-      Return a list of tuple containing ((query_start, target_start), [alignment item]).
-      The `query_start` and `target_start` are indexes in sourced_text, the `alignment item`
-      is a list containing {"ref": ref, "hyp": hyp, "ref_pos": ref_pos, "hyp_pos": hyp_pos,
-      "hyp_time": hyp_time}, ref is the token from reference, hyp is the token from query,
-      ref_pos is local index in reference document, hyp_pos is local index in query document,
-      hyp_time is the timestamp of hyp.
+      Return a list of tuple containing
+      ((query_start, target_start), [alignment item]).
+      The `query_start` and `target_start` are indexes in sourced_text,
+      the `alignment item` is a list containing `{"ref": ref, "hyp": hyp,
+      "ref_pos": ref_pos, "hyp_pos": hyp_pos, "hyp_time": hyp_time}`, `ref` is
+      the token from reference, `hyp` is the token from query, `ref_pos` is
+      local index in reference document, `hyp_pos` is local index in query
+      document, `hyp_time` is the timestamp of `hyp`.
     """
     # The container to store the returning results.
     alignments = [None] * num_queries
     prev_target_end = 0
     for sub in sub_alignments:
         if sub["alignment"][0] == -1:
             logging.warning(f"Skipping empty sub segment.")
@@ -288,174 +298,190 @@
         # we are doing levenshtein_distance in "global" mode
         assert target_align_start == 0, target_align_start
         assert target_end == (target_start + target_align_end + 1), (
             target_end,
             target_start + target_align_end + 1,
         )
 
-        query_id = sourced_text.doc[query_start]
+        query_doc_id = sourced_text.doc[query_start]
 
-        if alignments[query_id] is None:
-            alignments[query_id] = (
+        if alignments[query_doc_id] is None:
+            alignments[query_doc_id] = (
                 (query_start, target_start + target_align_start),
                 [],
             )
 
-        query_doc_id = sourced_text.doc[query_start]
         query_base = sourced_text.doc_splits[query_doc_id]
         query_source = sourced_text.sources[query_doc_id]
 
         # aligns : [{"ref": , "hyp": , "ref_pos": , "hyp_pos": , "hyp_time":}]
-        aligns = alignments[query_id][1]
+        aligns = alignments[query_doc_id][1]
         # Note: query_source could be TextSource or Transcript, only Transcript
         # has times.
-        times = query_source.times if isinstance(query_source, Transcript) else None
+        times = (
+            query_source.times if isinstance(query_source, Transcript) else None
+        )
         # The times is in byte level.
         time_stride = 1 if query_source.binary_text.dtype == np.uint8 else 4
 
-        query_length = query_end - query_start
-        query_local_index = query_start - query_base
+        query_base_next = sourced_text.doc_splits[query_doc_id + 1]
+        query_length = query_base_next - query_base
         query_index = query_start
         target_index = target_start + target_align_start
 
-        hyp_time = 0 if times is None else float(times[query_local_index * time_stride])
         for ali in align_str:
-            query_local_index = (
-                query_local_index
-                if query_local_index < query_length
-                else query_length - 1
+            query_index = (
+                query_index if query_index < query_end else query_end - 1
             )
+            hyp_pos = int(sourced_text.pos[query_index])
+
             hyp_time = (
-                0 if times is None else float(times[query_local_index * time_stride])
+                0 if times is None else float(times[hyp_pos * time_stride])
+            )
+
+            target_index = (
+                target_index if target_index < target_end else target_end - 1
             )
-            target_index = target_index if target_index < target_end else target_end - 1
             ref_pos = int(sourced_text.pos[target_index])
-            query_index = query_index if query_index < query_end else query_end - 1
             if ali == "I":
-                aligns.append(
-                    {
-                        "ref": "",
-                        "hyp": chr(sourced_text.binary_text[query_index]),
-                        "ref_pos": ref_pos,
-                        "hyp_pos": query_local_index,
-                        "hyp_time": hyp_time,
-                    }
-                )
-                query_local_index += 1
+                ref = ""
+                hyp = chr(sourced_text.binary_text[query_index])
                 query_index += 1
             elif ali == "D":
-                aligns.append(
-                    {
-                        "ref": chr(sourced_text.binary_text[target_index]),
-                        "hyp": "",
-                        "ref_pos": ref_pos,
-                        "hyp_pos": query_local_index,
-                        "hyp_time": hyp_time,
-                    }
-                )
+                ref = chr(sourced_text.binary_text[target_index])
+                hyp = ""
                 target_index += 1
             else:
                 assert ali == "C" or ali == "S"
                 ref = chr(sourced_text.binary_text[target_index])
                 hyp = chr(sourced_text.binary_text[query_index])
                 # The following two asserts guarantee the correctness of
                 # levenshtein alignment. So *DO NOT* delete it.
                 if ali == "C":
                     assert ref == hyp
                 else:
                     assert ref != hyp
-                aligns.append(
-                    {
-                        "ref": ref,
-                        "hyp": hyp,
-                        "ref_pos": ref_pos,
-                        "hyp_pos": query_local_index,
-                        "hyp_time": hyp_time,
-                    }
-                )
-                query_local_index += 1
                 query_index += 1
                 target_index += 1
+            aligns.append(
+                {
+                    "ref": ref,
+                    "hyp": hyp,
+                    "ref_pos": ref_pos,
+                    "hyp_pos": hyp_pos,
+                    "hyp_time": hyp_time,
+                }
+            )
     return alignments
 
 
-def get_alignments(
+def align_queries(
     sourced_text: SourcedText,
-    close_matches: np.ndarray,
+    num_query_tokens: int,
+    num_close_matches: int = 2,
     segment_length: int = 5000,
     reference_length_difference: float = 0.1,
+    min_matched_query_ratio: float = 0.33,
     thread_pool: Optional[ThreadPool] = None,
 ) -> List[Tuple[Tuple[int, int], List[Dict[str, Any]]]]:
     """
     Get levenshtein alignment for each query document in sourced_text.
 
-    For each query document we will locate its corresponding segment in the reference
-    document and return the levenshtein alignment between the query and its corresponding
-    reference segment.
+    For each query document we will locate its corresponding segment in the
+    reference document and return the levenshtein alignment between the query
+    and its corresponding reference segment.
 
     Args:
       sourced_text:
-        The SourcedText containing the queries and references, the first N (we can
-        get it from close_matches) documents are queries and the others are references.
-      close_matches:
-        Generated from sourced_text with the function `find_candidate_matches`.
-        It contains the close matched reference token for each query token.
+        The SourcedText containing the queries and references, the first N
+        documents are queries and the others are references.
+      num_query_tokens:
+        The number of query tokens in sourced_text, it tells the boundary between
+        queries and references sourced_text[0:num_query_tokens] are query tokens,
+        sourced_text[num_query_tokens:] are reference tokens.
+      num_close_matches:
+        The number of close_matches for each query token.
       segment_length:
         The query length might be long, in order to accelerate the levenshtein
         algorithm we will split the long query into smaller segments, `segment_length`
         is the expected length of the smaller segments.
       reference_length_difference:
         Because of the insertion or deletion errors, the reference sequence might be
         shorter or longer than the query, so the reference segment length can be from
         `len(query) * (1 - reference_length_difference / 2)` to
         `len(query) * (1 + reference_length_difference / 2)`.
+      min_matched_query_ratio:
+        The minimum ratio of matched query tokens, if the ratio is less than
+        `min_matched_query_ratio` the query will be dropped.
       thread_pool:
         The ThreadPool to run levenshtein.
     Returns:
-      Return a list of tuple containing ((query_start, target_start), [alignment item]).
-      The `query_start` and `target_start` are indexes in sourced_text, the `alignment item`
-      is a list containing {"ref": ref, "hyp": hyp, "ref_pos": ref_pos, "hyp_pos": hyp_pos,
-      "hyp_time": hyp_time}, ref is the token from reference, hyp is the token from query,
-      ref_pos is local index in reference document, hyp_pos is local index in query document,
-      hyp_time is the timestamp of hyp.
+      Return a list of tuple containing
+      ((query_start, target_start), [alignment item]).
+      The `query_start` and `target_start` are indexes in sourced_text,
+      the `alignment item` is a list containing `{"ref": ref, "hyp": hyp,
+      "ref_pos": ref_pos, "hyp_pos": hyp_pos, "hyp_time": hyp_time}`, `ref` is
+      the token from reference, `hyp` is the token from query, `ref_pos` is
+      local index in reference document, `hyp_pos` is local index in query
+      document, `hyp_time` is the timestamp of `hyp`.
     """
+
+    logging.debug(
+        f"Creating suffix array on a sequence with length : "
+        f"{sourced_text.binary_text.size}."
+    )
+    suffix_array = create_suffix_array(sourced_text.binary_text)
+
+    logging.debug(
+        f"Finding close matches for {num_query_tokens} query tokens with "
+        f"num_close_matches={num_close_matches}."
+    )
+    close_matches = find_close_matches(
+        suffix_array, num_query_tokens, num_close_matches=num_close_matches
+    )
+
     tot_query_symbols, num_close_matches = close_matches.shape
+    assert num_query_tokens == tot_query_symbols, (
+        num_query_tokens,
+        tot_query_symbols,
+    )
     num_queries = sourced_text.doc[tot_query_symbols]
 
-    row_splits = sourced_text.doc_splits
+    logging.debug(f"Getting alignments for {num_queries} queries.")
 
-    logging.info("Getting matching points.")
+    row_splits = sourced_text.doc_splits
     arguments = []
     for q in range(num_queries):
         query_start = row_splits[q]
         query_end = row_splits[q + 1]
         query_len = row_splits[q + 1] - row_splits[q]
 
         # seq1 contains the query index in sourced_text.
         # seq2 contains the reference index in sourced_text.
         seq1 = np.arange(query_start, query_end).reshape(-1, 1)
         seq1 = np.tile(seq1, num_close_matches).flatten()
 
         seq2 = close_matches[query_start:query_end, :].flatten()
-        # matched_points is a list of (query index, target index), global index in sourced_text
+        # matched_points is a list of (query index, target index), global index
+        # in sourced_text
         matched_points = get_longest_increasing_pairs(seq1, seq2)
 
         if len(matched_points) == 0:
             continue
 
-        # In the algorithm of `find_close_matches`, `sourced_text.binary_text.size - 1`
-        # means no close_matches
+        # In the algorithm of `find_close_matches`,
+        # `sourced_text.binary_text.size - 1` means no close_matches
         trim_pos = len(matched_points) - 1
         while matched_points[trim_pos][1] == sourced_text.binary_text.size - 1:
             trim_pos -= 1
         matched_points = matched_points[0:trim_pos]
 
-        # The following code guarantees the matched points are in the same reference
-        # document. We will choose the reference document that matches the most number
-        # of query tokens.
+        # The following code guarantees the matched points are in the same
+        # reference document. We will choose the reference document that matches
+        # the most number of query tokens.
         doc_ids = sourced_text.doc[np.array([x[1] for x in matched_points])]
         # we don't really care about the real doc id, we just want to know the
         # index in matched_points, minus doc_ids[0] here for efficiency.
         doc_ids = doc_ids - doc_ids[0]
         doc_splits = row_ids_to_row_splits(doc_ids)
         max_num_matches = -1
         max_ranges = (0, len(matched_points))
@@ -466,116 +492,165 @@
                 matched_points[doc_splits[i + 1] - 1][0]
                 - matched_points[doc_splits[i]][0]
             )
             if num_matches > max_num_matches:
                 max_num_matches = num_matches
                 max_ranges = (doc_splits[i], doc_splits[i + 1])
 
-        if max_num_matches < 0.33 * query_len:
+        if max_num_matches < min_matched_query_ratio * query_len:
             logging.warning(
-                f"Skipping query {q}, less than 1 / 3 of query matched by close_matches."
+                f"Skipping query {q}, less than {min_matched_query_ratio * 100}"
+                f"% of query tokens matched in close_matches."
             )
             continue
 
         matched_points = matched_points[max_ranges[0] : max_ranges[1]]
 
+        # Break query into short segments, so that we only need to run levenshtein
+        # algorithm on short sequence (for efficiency).
         # segments is a list of (query_start, query_end, target_start, target_end)
         # they are the indexes in sourced_text.
         segments = _break_query(
             sourced_text=sourced_text,
             matched_points=matched_points,
             segment_length=segment_length,
             reference_length_difference=reference_length_difference,
         )
 
         # prepare arguments list for levenshtein_worker
         for seg in segments:
             arguments.append((sourced_text, seg))
 
-    logging.info("Getting matching points done.")
-
     def levenshtein_worker(sourced_text, segment):
         query = sourced_text.binary_text[segment[0] : segment[1]]
         target = sourced_text.binary_text[segment[2] : segment[3]]
         # Using global matching mode here, thanks to `get_longest_increasing_pairs`
         # we have very good matching points.
-        alignment = levenshtein_distance(query=query, target=target, mode="global")
+        alignment = levenshtein_distance(
+            query=query, target=target, mode="global"
+        )
         return {
             "segment": segment,
             "alignment": alignment,
             "target": target,
         }
 
     pool = ThreadPool() if thread_pool is None else thread_pool
-    logging.info("Matching with levenshtein.")
+    logging.debug(f"Matching with levenshtein for {len(arguments)} segments.")
     async_results = pool.starmap_async(levenshtein_worker, arguments)
     results = async_results.get()
-    logging.info("Matching with levenshtein done.")
+    logging.debug("Matching with levenshtein done.")
+
+    alignments = _combine_sub_alignments(sourced_text, results, num_queries)
 
-    return _combine_sub_alignments(sourced_text, results, num_queries)
+    assert sourced_text.doc[num_query_tokens] == len(alignments), (
+        sourced_text.doc[num_query_tokens],
+        len(alignments),
+    )
+    return alignments
 
 
 def _get_segment_candidates(
-    target_source: TextSource, alignment
+    target_source: TextSource,
+    alignment,
+    silence_length_to_break: float = 0.6,  # in second
+    min_duration: float = 2,  # in second
+    max_duration: float = 30,  # in second
+    expected_duration: Tuple[float, float] = (5, 20),  # in second
+    max_error_rate: float = 0.20,
+    num_of_best_position: int = 4,
 ) -> List[Tuple[int, int, float]]:
     """
     Split the long aligned query into smaller segments.
 
-    we create scores for each position in the alignment, corresponding to how good
-    a position it is to begin or end a split.
+    First, we get a list candidate breaking positions, these positions have
+    long enough preceding silence (begin a split) or succeeding silence (end of
+    a split), the length of silence is controlled by `silence_length_to_break`.
+    If the `target_source` has punctuations, we will only start or end of a
+    split at punctuation positions that indicate the end of a sentence.
+
+    we create scores for each candidate position in the alignment, corresponding
+    to how good a position it is to begin or end a split.
 
      - begin a split (i.e. this is first position in a segment)
         - plus score equal to num silence seconds this
           follows, up to some limit 3 seconds, i.e. this element
-          of the Transcript's time minus the previous element's time; or some default (3.0 sec)
-          if this is the first element of the Transcript.
+          of the Transcript's time minus the previous element's time; or some
+          default (3.0 sec) if this is the first element of the Transcript.
         - good if there are few errors around this point in the alignment, i.e.
           score corresponding to number of ins,del,mismatch within a certain
           region of this position.
         - good if the previous non-whitespace character was a punctuation
           character.  (Lists of whitespace and punctuation characters will
           be passed in)
 
      - end a split (i.e. this is the last position in a segment).
-        - plus score equal to number of silence seconds follows this position, up to some
-          limit 3 seconds, i.e next element of the Transcript's time minus this element's
-          time; or some default (3.0 sec) if this is the last element of the Transcript.
+        - plus score equal to number of silence seconds follows this position,
+          up to some limit 3 seconds, i.e next element of the Transcript's time
+          minus this element's time; or some default (3.0 sec) if this is the
+          last element of the Transcript.
         - good if there are few errors around this point in the alignment, i.e.
           score corresponding to number of ins,del,mismatch within a certain
           region of this position.
         - good if the following non-whitespace character is a punctuation character.
 
 
     We then create a rule to assign scores to potential segments. This consist of
     the begin-scores, plus the end-scores, plus:
       - Some kind of penalty related to the duration of the segment, e.g.
-        infinity if it's over some max-duration like 30 seconds or less than a
-        min-duration like 2 seconds; else, one that encourages a duration between
-        5 to 20 seconds.
+        infinity if it's over some `max_duration` like 30 seconds or less than a
+        `min_duration` like 2 seconds; else, one that encourages a duration
+        between `expected_duration` like 5 to 20 seconds.
       - A bonus for the number of matches in the alignment.
       - A penalty for the number of errors in the alignment (could multiply this by
         some scale depending how much we don't want to have errors, but some errors
         are expected due to both ASR errors and normalization differences.)
 
-    Next, we can do a search for a good segmentation.  You could define the problem
-    as getting the highest-scoring set of segments that do not overlap.  One
-    possible way to do it is as follows:
-       For each begin_position in the top 10% of scores, find the 4 best-scoring end_positions
-       For each end_position in the top 10% of scores, find the 4 best-scoring begin_positions
-    Append the preceding 2 sets of segments to get a list of candidate segments.
+    Next, we search for a good segmentation. We define the problem as getting
+    the highest-scoring set of segments that do not overlap. For each
+    begin_position, find the `num_of_best_position` like 4 best-scoring
+    end_positions. For each end_position, find the `num_of_best_position`
+    best-scoring begin_positions. Append the preceding 2 sets of segments to get
+    a list of candidate segments.
 
     Args:
       target_source:
         A TextSource containing the matched reference.
       alignment:
-        Alignment information, one item of the returned alignments from `get_alignments`.
+        Alignment information, one item of the returned alignments from
+        `align_queries`.
+      silence_length_to_break:
+        A threshold for deciding the possible breaking points, if a position has
+        preceding or succeeding silence length greater than this value, we will
+        add it as a possible breaking point.
+        Caution: Only be used when there are no punctuations in target_source.
+      min_duration:
+        The minimum duration (in second) allowed for a segment.
+      max_duration:
+        The maximum duration (in second) allowed for a segment.
+      expected_duration:
+        The expected duration (in second) for a segment, it is a range (a tuple
+        containing lower bound and upper bound).
+        Note: The values must satisfy `min_duration <= expected_duration[0]` and
+        `max_duration >= expected_duration[1]`.
+      max_error_rate:
+        The max levenshtein distance (char level) between query and target at
+        the segment area, if the segments with higher error rate than this value
+        will not appear in the final result list.
+      num_of_best_position:
+        For each candidate breaking points, there will be several possible start
+        points (if the point is the end of segment) or end points (if the point
+        is the start of a segment), this is the number of possible points.
+        Normally this does not affect the final result too much, just leave it
+        as default is OK.
 
     Returns:
-      Returns a list of tuple, each tuple contains the start position, end position and score of
-      current segment, start position and end position are indexes in aligns.
+      Returns a list of tuple, each tuple contains the start position,
+      end position and score of current segment, start position and end
+      position are indexes in aligns.
     """
     (query_start, target_start), aligns = alignment
 
     # [(index, score)]
     begin_scores: List[Tuple[int, float]] = []
     end_scores: List[Tuple[int, float]] = []
 
@@ -587,32 +662,41 @@
             1 if align["ref"] != align["hyp"] else 0
             for align in aligns[0:half_region_size]
         ]
     )
 
     # will be used as max_silence, punctuation_score, init_duration_score
     # we need to make these scores similar to avoiding one of them dominating
-    # the total score. Any value is ok, choose 3 here mainly based on the silence length.
+    # the total score. Any value is ok, choose 3 here mainly based on the
+    # silence length.
     base_score = 3
     max_silence = base_score  # seconds
-    punctuation_score = (
-        base_score  # score for preceding (begin) and following(end) punctuation
-    )
+    # score for preceding (begin) and succeeding (end) punctuation
+    punctuation_score = base_score
 
     # Use cumsum to get number of matches and errors in a range efficiently
     cumsum_match = [0] * len(aligns)
     cumsum_error = [0] * len(aligns)
 
+    # to avoid breaking at somethings like Mr. Mrs. etc.
+    period_patterns = regex.compile(
+        "(?<!Mr|Mrs|Dr|Ms|Prof|Pro|Capt|Gen|Sen|Rev|Hon|St)\."
+    )
+    # the largest length of the patterns.
+    period_pattern_length = 4
+
     for i, align in enumerate(aligns):
         matched = align["ref"] == align["hyp"]
         cumsum_match[i] = (
             int(matched) if i == 0 else (cumsum_match[i - 1] + int(matched))
         )
         cumsum_error[i] = (
-            int(not matched) if i == 0 else (cumsum_error[i - 1] + int(not matched))
+            int(not matched)
+            if i == 0
+            else (cumsum_error[i - 1] + int(not matched))
         )
 
         # calculate the errors in a region with a sliding window.
         if i - half_region_size >= 0:
             if (
                 aligns[i - half_region_size]["ref"]
                 != aligns[i - half_region_size]["hyp"]
@@ -623,411 +707,620 @@
                 aligns[i + half_region_size]["ref"]
                 != aligns[i + half_region_size]["hyp"]
             ):
                 errors_in_region += 1
 
         # silence
         prev_silence = (
-            max_silence if i == 0 else (align["hyp_time"] - aligns[i - 1]["hyp_time"])
+            max_silence
+            if i == 0
+            else (align["hyp_time"] - aligns[i - 1]["hyp_time"])
+        )
+        prev_silence = (
+            max_silence if prev_silence > max_silence else prev_silence
         )
-        prev_silence = max_silence if prev_silence > max_silence else prev_silence
-        post_silence = (
+        succ_silence = (
             max_silence
             if i == len(aligns) - 1
             else (aligns[i + 1]["hyp_time"] - align["hyp_time"])
         )
-        post_silence = max_silence if post_silence > max_silence else post_silence
+        succ_silence = (
+            max_silence if succ_silence > max_silence else succ_silence
+        )
 
         # punctuation
         prev_punctuation = 0
         j = align["ref_pos"] - 1
         while j >= 0:
             current_token = chr(target_source.binary_text[j])
             if is_punctuation(current_token, eos_only=True):
-                prev_punctuation = punctuation_score
-                break
+                tmp = "".join(
+                    [
+                        chr(x)
+                        for x in target_source.binary_text[
+                            j - period_pattern_length : j + 1
+                        ]
+                    ]
+                )
+                if period_patterns.search(tmp) is not None:
+                    prev_punctuation = punctuation_score
+                    break
+                else:
+                    j -= 1
             elif current_token == " " or is_punctuation(current_token):
                 j -= 1
             else:
                 break
 
-        post_punctuation = 0
+        succ_punctuation = 0
         j = align["ref_pos"] + 1
         while j < target_source.binary_text.size:
             current_token = chr(target_source.binary_text[j])
             if is_punctuation(current_token, eos_only=True):
-                post_punctuation = punctuation_score
-                break
+                tmp = "".join(
+                    [
+                        chr(x)
+                        for x in target_source.binary_text[
+                            j - period_pattern_length : j + 1
+                        ]
+                    ]
+                )
+                if period_patterns.search(tmp) is not None:
+                    succ_punctuation = punctuation_score
+                    break
+                else:
+                    j += 1
             elif current_token == " " or is_punctuation(current_token):
                 j += 1
             else:
                 break
-        begin_scores.append(
-            (
-                i,
-                prev_silence + prev_punctuation - errors_in_region / half_region_size,
-            )
-        )
-        end_scores.append(
-            (
-                i,
-                post_silence + post_punctuation - errors_in_region / half_region_size,
-            )
+
+        begin_score = (
+            prev_silence
+            + prev_punctuation
+            - errors_in_region / half_region_size
         )
 
-    sorted_begin_scores = sorted(begin_scores, key=lambda x: x[1], reverse=True)
-    sorted_end_scores = sorted(end_scores, key=lambda x: x[1], reverse=True)
+        end_score = (
+            succ_silence
+            + succ_punctuation
+            - errors_in_region / half_region_size
+        )
 
-    top_ratio = 0.1
-    top_begin = sorted_begin_scores[0 : int(len(begin_scores) * top_ratio)]
-    top_end = sorted_end_scores[0 : int(len(end_scores) * top_ratio)]
+        if target_source.has_punctuation:
+            if prev_punctuation > 0 or i == 0:
+                begin_scores.append((i, begin_score,))
+            if succ_punctuation > 0 or i == len(aligns) - 1:
+                end_scores.append((i, end_score,))
+        else:
+            if matched and (prev_silence >= silence_length_to_break or i == 0):
+                begin_scores.append((i, begin_score,))
+            if matched and (
+                succ_silence >= silence_length_to_break or i == len(aligns) - 1
+            ):
+                end_scores.append((i, end_score,))
 
     # (start, end, score)
     begin_list: List[Tuple[int, int, float]] = []
     end_list: List[Tuple[int, int, float]] = []
 
-    num_of_best_position = 4
-    max_errors_ratio = 0.20
-    max_text_length = 1000
     init_duration_score = (
         base_score  # duration_score for segment between 5 ~ 20 seconds
     )
-    max_duration = 30  # seconds
-    min_duration = 2  # seconds
-    expected_duration = (5, 20)  # seconds
 
-    for item in top_begin:
+    last_ind = 0
+    for i, item in enumerate(begin_scores):
         # Caution: Can only be modified with heappush and heappop, it is used as
         # the container of a heap.
         item_q = []
-        ind = item[0] + 1
-        while ind < len(end_scores) and end_scores[ind][0] - item[0] < max_text_length:
-            point_score = begin_scores[item[0]][1] + end_scores[ind][1]
+        ind = bisect_right(end_scores, item, lo=last_ind)
+        last_ind = ind
+
+        while True:
+            if ind >= len(end_scores) or ind < 0:
+                break
+
+            duration = (
+                aligns[end_scores[ind][0]]["hyp_time"]
+                - aligns[item[0]]["hyp_time"]
+            )
+            if duration <= min_duration:
+                ind += 1
+                continue
+
+            if duration > max_duration:
+                break
+
+            point_score = begin_scores[i][1] + end_scores[ind][1]
+
             # matching scores
             matched_score = (
                 base_score
                 * (cumsum_match[end_scores[ind][0]] - cumsum_match[item[0]])
                 / (end_scores[ind][0] - item[0])
             )
 
             # errors penalties
-            total_errors = cumsum_error[end_scores[ind][0]] - cumsum_error[item[0]]
+            total_errors = (
+                cumsum_error[end_scores[ind][0]] - cumsum_error[item[0]]
+            )
             # skipping segment with too much matching errors.
-            if total_errors >= (end_scores[ind][0] - item[0]) * max_errors_ratio:
+            if total_errors >= (end_scores[ind][0] - item[0]) * max_error_rate:
                 ind += 1
                 continue
-            error_score = base_score * (total_errors) / (end_scores[ind][0] - item[0])
-
-            # duration scores
-            duration = (
-                aligns[end_scores[ind][0]]["hyp_time"] - aligns[item[0]]["hyp_time"]
+            error_score = (
+                base_score * (total_errors) / (end_scores[ind][0] - item[0])
             )
 
-            duration_score = (
-                float("-inf")
-                if duration >= max_duration or duration <= min_duration
-                else init_duration_score
-            )
+            duration_score = init_duration_score
 
             duration_score = (
                 duration_score
                 - (duration - min_duration)
                 / (expected_duration[0] - min_duration)
                 * init_duration_score
-                if duration < expected_duration[0] and duration > min_duration
+                if duration < expected_duration[0]
                 else duration_score
             )
 
             duration_score = (
                 duration_score
                 - (max_duration - duration)
                 / (max_duration - expected_duration[1])
                 * init_duration_score
-                if duration > expected_duration[1] and duration < max_duration
+                if duration > expected_duration[1]
                 else duration_score
             )
 
             heappush(
                 item_q,
                 (
                     point_score + matched_score - error_score + duration_score,
-                    (
-                        item[0],
-                        end_scores[ind][0],
-                    ),
+                    (item[0], end_scores[ind][0],),
                 ),
             )
             if len(item_q) > num_of_best_position:
                 heappop(item_q)
             ind += 1
         while item_q:
             x = heappop(item_q)
-            if x[0] != float("-inf"):
-                begin_list.append((x[1][0], x[1][1], x[0]))
+            begin_list.append((x[1][0], x[1][1], x[0]))
 
-    for item in top_end:
+    last_ind = 0
+    for i, item in enumerate(end_scores):
         # Caution: Can only be modified with heappush and heappop, it is used as
         # the container of a heap.
         item_q = []
-        ind = item[0] - 1
-        while ind >= 0 and item[0] - begin_scores[ind][0] < max_text_length:
-            point_score = begin_scores[ind][1] + end_scores[item[0]][1]
+        ind = bisect_left(begin_scores, item, lo=last_ind)
+        last_ind = ind
+
+        while True:
+            if ind < 0 or ind >= len(begin_scores):
+                break
+
+            duration = (
+                aligns[item[0]]["hyp_time"]
+                - aligns[begin_scores[ind][0]]["hyp_time"]
+            )
+
+            if duration <= min_duration:
+                ind -= 1
+                continue
+
+            if duration >= max_duration:
+                break
+
+            point_score = begin_scores[ind][1] + end_scores[i][1]
             # matching scores
             matched_score = (
                 base_score
                 * (cumsum_match[item[0]] - cumsum_match[begin_scores[ind][0]])
                 / (item[0] - begin_scores[ind][0])
             )
 
             # errors penalties
-            total_errors = cumsum_error[item[0]] - cumsum_error[begin_scores[ind][0]]
+            total_errors = (
+                cumsum_error[item[0]] - cumsum_error[begin_scores[ind][0]]
+            )
             # skipping segment with too much matching errors.
-            if total_errors >= (item[0] - begin_scores[ind][0]) * max_errors_ratio:
+            if (
+                total_errors
+                >= (item[0] - begin_scores[ind][0]) * max_error_rate
+            ):
                 ind -= 1
                 continue
-            error_score = base_score * (total_errors) / (item[0] - begin_scores[ind][0])
-
-            # duration scores
-            duration = (
-                aligns[item[0]]["hyp_time"] - aligns[begin_scores[ind][0]]["hyp_time"]
+            error_score = (
+                base_score * (total_errors) / (item[0] - begin_scores[ind][0])
             )
 
-            duration_score = (
-                float("-inf")
-                if duration >= max_duration or duration <= min_duration
-                else init_duration_score
-            )
+            duration_score = init_duration_score
 
             duration_score = (
                 duration_score
                 - (duration - min_duration)
                 / (expected_duration[0] - min_duration)
                 * init_duration_score
-                if duration < expected_duration[0] and duration > min_duration
+                if duration < expected_duration[0]
                 else duration_score
             )
 
             duration_score = (
                 duration_score
                 - (max_duration - duration)
                 / (max_duration - expected_duration[1])
                 * init_duration_score
-                if duration > expected_duration[1] and duration < max_duration
+                if duration > expected_duration[1]
                 else duration_score
             )
 
             heappush(
                 item_q,
                 (
                     point_score + matched_score - error_score + duration_score,
-                    (
-                        begin_scores[ind][0],
-                        item[0],
-                    ),
+                    (begin_scores[ind][0], item[0],),
                 ),
             )
             if len(item_q) > num_of_best_position:
                 heappop(item_q)
             ind -= 1
         while item_q:
             x = heappop(item_q)
-            if x[0] != float("-inf"):
-                end_list.append((x[1][0], x[1][1], x[0]))
+            end_list.append((x[1][0], x[1][1], x[0]))
 
     candidates = begin_list + end_list
     return candidates
 
 
-def split_into_segments(
-    query_source: Union[Transcript, TextSource], target_source: TextSource, alignment
+def _split_into_segments(
+    query_source: Union[Transcript, TextSource],
+    target_source: TextSource,
+    alignment: Tuple[Tuple[int, int], List[Dict[str, Any]]],
+    preceding_context_length: int = 1000,
+    timestamp_position: str = "middle",  # previous, middle, current
+    silence_length_to_break: float = 0.6,  # in second
+    min_duration: float = 2,  # in second
+    max_duration: float = 30,  # in second
+    expected_duration: Tuple[float, float] = (5, 20),  # in second
+    max_error_rate: float = 0.15,
+    num_of_best_position: int = 4,
 ) -> List[Dict[str, Union[str, int, float]]]:
     """
     Split a long aligned query into smaller segments.
 
-    We will create scores for each position in the alignment, corresponding to how good
-    a position it is to begin or end a split. We can then create a rule to assign scores
-    to potential segments. The scores would consist of the begin-scores, plus the end-scores,
-    plus some kind of scores of given segment (duration, matching errors .etc).
+    We will create scores for each position in the alignment, corresponding to
+    how good a position it is to begin or end a split. We can then create a rule
+    to assign scores to potential segments. The scores would consist of the
+    begin-scores, plus the end-scores, plus some kind of scores of given segment
+    (duration, matching errors .etc).
 
     Args:
       query_source:
         An instance of Transcript or TextSource containing the query.
       target_source:
         An instance of TextSource containing the matched reference.
       alignment:
-        The alignment, an item in the list returned by `get_alignments`.
+        The alignment, an item in the list returned by `align_queries`.
+      preceding_context_length:
+        The number of characters of preceding context.
+      timestamp_position:
+        It indicates which token we will get `start_time` from, valid values are
+        `previous`, `middle` and `current`. If it equals to `current` the
+        `start_time` is the timestamp of token in `begin_pos`, if it equals to
+        `previous` the `start_time` is the timestamp of token in `begin_pos - 1`
+        if it equals to `middle`, the `start_time` is the averaged timestamp of
+        tokens in `begin_pos` and `begin_pos - 1`.
+      silence_length_to_break:
+        A threshold for deciding the possible breaking points, if a position has
+        preceding or succeeding silence length greater than this value, we will
+        add it as a possible breaking point.
+        Caution: Only be used when there are no punctuations in target_source.
+      min_duration:
+        The minimum duration (in second) allowed for a segment.
+      max_duration:
+        The maximum duration (in second) allowed for a segment.
+      expected_duration:
+        The expected duration (in second) for a segment, it is a range (a tuple
+        containing lower bound and upper bound).
+        Note: The values must satisfy `min_duration <= expected_duration[0]` and
+        `max_duration >= expected_duration[1]`.
+      max_error_rate:
+        The max levenshtein distance (char level) between query and target at
+        the segment area, if the segments with higher error rate than this value
+        will not appear in the final result list.
+      num_of_best_position:
+        For each candidate breaking points, there will be several possible start
+        points (if the point is the end of segment) or end points (if the point
+        is the start of a segment), this is the number of possible points.
+        Normally this does not affect the final result too much, just leave it
+        as default is OK.
+
+    Return
+      Returns a list of Dict containing the details of each segment, looks like
+
+         {
+             "begin_byte": int,   # begin position in original target source
+             "end_byte": int,     # end position in original target source
+             "start_time": float, # start timestamp in the audio
+             "duration": float,   # duration of this segment
+             "hyp": str,          # text from query source
+             "ref": str,          # text from target source
+             "pre_ref": str,      # preceding text from target source
+             "pre_hyp": str,      # preceding text from query source
+             "post_ref": str,     # succeeding text from target source
+             "post_hyp": str,     # succeeding text from query source
+         }
     """
     (query_start, target_start), aligns = alignment
 
     # candidates : (start, end, score), start and end are indexes in aligns
     candidates = _get_segment_candidates(
-        target_source=target_source, alignment=alignment
+        target_source=target_source,
+        alignment=alignment,
+        silence_length_to_break=silence_length_to_break,
+        min_duration=min_duration,
+        max_duration=max_duration,
+        expected_duration=expected_duration,
+        max_error_rate=max_error_rate,
+        num_of_best_position=num_of_best_position,
     )
 
     candidates = sorted(candidates, key=lambda x: x[2], reverse=True)
 
     # Handle the overlapping
-    # Note: Don't modified selected_ranges, it will be manipulated in `is_overlap`
-    # and will be always kept sorted.
+    # Caution: Don't modified selected_ranges, it will be manipulated in
+    # `is_overlap` and will be always kept sorted.
     selected_ranges: List[Tuple[int, int]] = []
     segments = []
     for r in candidates:
-        if not is_overlap(selected_ranges, (r[0], r[1])):
+        if not is_overlap(
+            selected_ranges, query=(r[0], r[1]), overlap_ratio=0.5
+        ):
             segments.append(r)
 
     results = []
-    min_text_length = 30  # around 5 words
-    preceding_context_length = 1000
 
     for seg in segments:
         begin_pos = aligns[seg[0]]["ref_pos"]
         end_pos = aligns[seg[1]]["ref_pos"] + 1
 
         preceding_index = seg[0] if seg[0] == 0 else seg[0] - 1
+        succeeding_index = seg[1] if seg[1] == len(aligns) - 1 else seg[1] + 1
 
-        # start = (aligns[preceding_index]["hyp_time"] + aligns[seg[0]]["hyp_time"]) / 2
-
-        start = aligns[seg[0]]["hyp_time"]
-
-        following_index = seg[1] if seg[1] == len(aligns) - 1 else seg[1] + 1
-        duration = (
-            aligns[following_index]["hyp_time"] + aligns[seg[1]]["hyp_time"]
-        ) / 2 - start
-
-        # duration = aligns[seg[1]]["hyp_time"] - start
+        if timestamp_position == "middle":
+            start_time = (
+                aligns[preceding_index]["hyp_time"] + aligns[seg[0]]["hyp_time"]
+            ) / 2
+            end_time = (
+                aligns[succeeding_index]["hyp_time"]
+                + aligns[seg[1]]["hyp_time"]
+            ) / 2
+        elif timestamp_position == "previous":
+            start_time = aligns[preceding_index]["hyp_time"]
+            end_time = aligns[seg[1]]["hyp_time"]
+        else:
+            assert timestamp_position == "current", (
+                timestamp_position,
+                "current",
+            )
+            start_time = aligns[seg[0]]["hyp_time"]
+            end_time = aligns[succeeding_index]["hyp_time"]
 
         hyp_begin_pos = aligns[seg[0]]["hyp_pos"]
         hyp_end_pos = aligns[seg[1]]["hyp_pos"] + 1
         hyp = "".join(
-            [chr(i) for i in query_source.binary_text[hyp_begin_pos:hyp_end_pos]]
+            [
+                chr(i)
+                for i in query_source.binary_text[hyp_begin_pos:hyp_end_pos]
+            ]
         )
 
-        # skipping segment that has too short text
-        if len(hyp) < min_text_length:
-            continue
-
         # output one more token for reference to include the possible punctuation.
         # end_pos plus 1 here is safe, it is probably a space or punctuation.
         ref = "".join(
             [chr(i) for i in target_source.binary_text[begin_pos : end_pos + 1]]
         )
 
-        pre_index = (
+        preceding_pos = (
             begin_pos - preceding_context_length
             if begin_pos - preceding_context_length >= 0
             else 0
         )
-
-        pre_ref = "".join(
-            [chr(i) for i in target_source.binary_text[pre_index:begin_pos]]
+        preceding_ref = "".join(
+            [chr(i) for i in target_source.binary_text[preceding_pos:begin_pos]]
+        )
+        succeeding_ref = "".join(
+            [
+                chr(i)
+                for i in target_source.binary_text[
+                    end_pos : end_pos + preceding_context_length
+                ]
+            ]
         )
 
-        pre_index = (
+        preceding_pos = (
             hyp_begin_pos - preceding_context_length
             if hyp_begin_pos - preceding_context_length > 0
             else 0
         )
-        pre_hyp = "".join(
-            [chr(i) for i in query_source.binary_text[pre_index:hyp_begin_pos]]
+        preceding_hyp = "".join(
+            [
+                chr(i)
+                for i in query_source.binary_text[preceding_pos:hyp_begin_pos]
+            ]
+        )
+        succeeding_hyp = "".join(
+            [
+                chr(i)
+                for i in query_source.binary_text[
+                    hyp_end_pos : hyp_begin_pos + preceding_context_length
+                ]
+            ]
         )
 
         results.append(
             {
                 "begin_byte": begin_pos,
                 "end_byte": end_pos,
-                "start_time": start,
-                "duration": math.floor(1000 * duration) / 1000,
+                "start_time": start_time,
+                "duration": math.floor(1000 * (end_time - start_time)) / 1000,
                 "hyp": hyp,
                 "ref": ref,
-                "pre_ref": pre_ref,
-                "pre_hyp": pre_hyp,
+                "pre_ref": preceding_ref,
+                "pre_hyp": preceding_hyp,
+                "post_ref": succeeding_ref,
+                "post_hyp": succeeding_hyp,
             }
         )
     return results
 
 
-def find_candidate_matches(
-    close_matches: np.ndarray,
-    text: SourcedText,
-    length_ratio: float = 1.5,
-    num_candidates: int = 1,
-) -> List[List[Tuple[int, int]]]:
+def _split_helper(
+    query_source: Union[TextSource, Transcript],
+    target_source: TextSource,
+    cut_index: Tuple[int, int],
+    alignment: Tuple[Tuple[int, int], List[Dict[str, Any]]],
+    preceding_context_length: int,
+    timestamp_position: str,
+    silence_length_to_break: float,
+    min_duration: float,
+    max_duration: float,
+    expected_duration: Tuple[float, float],
+    max_error_rate: float,
+    num_of_best_position: int,
+):
     """
-    Find candidate regions in reference document that could be good matches for
-    each query document.
-
-    Args:
-       close_matches: an np.ndarray of shape (tot_query_symbols, num_close_matches)
-          as returned by find_close_matches(), indicating two close matches within
-          the reference text for each symbol in the query documents.
-       text:  The SourcedText corresponding to the query and reference documents
-          combined; needed for its `doc` member which can be assumed to be an np.ndarray.
-       length_ratio: indicates the maximum candidate-region length, which will be reduced
-          if the matching reference document was shorter than this.
-       num_candidates:  the number of candidate regions to find for each query
-          document.
-    Returns:
-       A list, one per query document, of close matches, where each close match
-       is a (begin, end) position within `text`.
+    A worker function for splitting aligned query.
     """
-    assert close_matches.ndim == 2, close_matches.ndim
-    tot_query_symbols, num_close_matches = close_matches.shape
-    assert text.binary_text.size > tot_query_symbols, (
-        text.binary_text.size,
-        tot_query_symbols,
+    segments = _split_into_segments(
+        query_source,
+        target_source,
+        alignment,
+        preceding_context_length=preceding_context_length,
+        timestamp_position=timestamp_position,
+        silence_length_to_break=silence_length_to_break,
+        min_duration=min_duration,
+        max_duration=max_duration,
+        expected_duration=expected_duration,
+        max_error_rate=max_error_rate,
+        num_of_best_position=num_of_best_position,
     )
+    return cut_index, segments
+
 
-    num_query_docs = text.doc[tot_query_symbols]
+def split_aligned_queries(
+    sourced_text: SourcedText,
+    alignments: List[Tuple[Tuple[int, int], List[Dict[str, Any]]]],
+    cut_indexes: List[Tuple[int, int]],
+    process_pool: Optional[Pool] = None,
+    preceding_context_length: int = 1000,
+    timestamp_position: str = "current",  # previous, middle, current
+    silence_length_to_break: float = 0.6,  # in second
+    min_duration: float = 2,  # in second
+    max_duration: float = 30,  # in second
+    expected_duration: Tuple[float, float] = (5, 20),  # in second
+    max_error_rate: float = 0.15,
+    num_of_best_position: int = 4,
+) -> List[Dict[str, Union[str, int, float]]]:
+    """
+    Split the aligned queries into smaller segments (A query might have several
+    hours of audio, which is not suitable for ASR training)
 
-    row_splits = text.doc_splits
+    Args:
+      sourced_text:
+        The SourcedText containing the queries and references.
+      alignments:
+        The alignments returned by function align_queries. The length of it is
+        equals to the number of queries.
+      cut_indexes:
+        A list of tuple containing the original cut index and supervision index
+        of the query([(cut index, sup index)]), it satisfies
+        `len(cut_indexes) == len(alignments)`
+      process_pool:
+        The process pool to split aligned queries. The algorithms are
+        implemented in python, so we use process pool to get rid of the effect
+        of GIL.
+      preceding_context_length:
+        The number of characters of preceding context.
+      timestamp_position:
+        It indicates which token we will get `start_time` from, valid values are
+        `previous`, `middle` and `current`. If it equals to `current` the
+        `start_time` is the timestamp of token in `begin_pos`, if it equals to
+        `previous` the `start_time` is the timestamp of token in `begin_pos - 1`
+        if it equals to `middle`, the `start_time` is the averaged timestamp of
+        tokens in `begin_pos` and `begin_pos - 1`.
+      silence_length_to_break:
+        A threshold for deciding the possible breaking points, if a position has
+        preceding or succeeding silence length greater than this value, we will
+        add it as a possible breaking point.
+        Caution: Only be used when there are no punctuations in target_source.
+      min_duration:
+        The minimum duration (in second) allowed for a segment.
+      max_duration:
+        The maximum duration (in second) allowed for a segment.
+      expected_duration:
+        The expected duration (in second) for a segment, it is a range (a tuple
+        containing lower bound and upper bound).
+        Note: The values must satisfy `min_duration <= expected_duration[0]` and
+        `max_duration >= expected_duration[1]`.
+      max_error_rate:
+        The max levenshtein distance (char level) between query and target at
+        the segment area, if the segments with higher error rate than this value
+        will not appear in the final result list.
+      num_of_best_position:
+        For each candidate breaking points, there will be several possible start
+        points (if the point is the end of segment) or end points (if the point
+        is the start of a segment), this is the number of possible points.
+        Normally this does not affect the final result too much, just leave it
+        as default is OK.
+
+    Return:
+      Returns a list of Dict containing the details of each segment, looks like
+
+         {
+             "begin_byte": int,   # begin position in original target source
+             "end_byte": int,     # end position in original target source
+             "start_time": float, # start timestamp in the audio
+             "duration": float,   # duration of this segment
+             "hyp": str,          # text from query source
+             "ref": str,          # text from target source
+             "pre_ref": str,      # preceding text from target source
+             "pre_hyp": str,      # preceding text from query source
+             "post_ref": str,     # succeeding text from target source
+             "post_hyp": str,     # succeeding text from query source
+         }
 
-    candidate_matches = []
+    """
+    arguments = []
+    aligned_length = 0
+    for i in range(len(alignments)):
+        if alignments[i] is not None:
+            (query_start, target_start), aligns = alignments[i]
+            aligned_length += aligns[-1]["hyp_time"] - aligns[0]["hyp_time"]
+            query_source = sourced_text.sources[sourced_text.doc[query_start]]
+            target_source = sourced_text.sources[sourced_text.doc[target_start]]
+            arguments.append(
+                (
+                    query_source,
+                    target_source,
+                    cut_indexes[i],
+                    alignments[i],
+                    preceding_context_length,
+                    timestamp_position,
+                    silence_length_to_break,
+                    min_duration,
+                    max_duration,
+                    expected_duration,
+                    max_error_rate,
+                    num_of_best_position,
+                )
+            )
+    logging.debug(
+        f"Aligned length : {aligned_length} seconds for {len(arguments)} queries."
+    )
 
-    for q in range(num_query_docs):
-        matches_start_pos = row_splits[q]
-        matches_end_pos = row_splits[q + 1]
-        current_query_len = row_splits[q + 1] - row_splits[q]
-        reference_chunk_length = current_query_len * length_ratio
-
-        current_close_matches = np.sort(
-            close_matches[matches_start_pos:matches_end_pos, :].flatten()
-        )
-
-        # (start pos in reference, end pos in reference, hits)
-        current_candidates = [(0, 0, 0)] * num_candidates
-        j = 1
-        for i in range(current_close_matches.size):
-            doc_id = text.doc[current_close_matches[i]]
-            pos_id = text.pos[current_close_matches[i]]
-            while (
-                j < current_close_matches.size
-                and text.doc[current_close_matches[j]] == doc_id
-                and text.pos[current_close_matches[j]]
-                < (pos_id + reference_chunk_length)
-            ):
-                j += 1
+    logging.debug(f"Splitting into segments for {len(arguments)} queries.")
+    pool = Pool() if process_pool is None else process_pool
+    async_results = pool.starmap_async(_split_helper, arguments)
+    results = async_results.get()
+    logging.debug(f"Splitting into segments done.")
 
-            candidate = (
-                current_close_matches[i],
-                current_close_matches[j - 1] + 1,
-                j - i,
-            )
-
-            min_score = candidate[2]
-            min_index = None
-            overlap = False
-            for i, c in enumerate(current_candidates):
-                if c[2] < min_score:
-                    min_score = c[2]
-                    min_index = i
-                if candidate[0] < c[1] and candidate[2] > c[2]:
-                    current_candidates[i] = candidate
-                    overlap = True
-                    break
-            if not overlap:
-                if len(current_candidates) < num_candidates:
-                    current_candidates.append(candidate)
-                else:
-                    if min_index is not None:
-                        current_candidates[min_index] = candidate
-        candidate_matches.append([(c[0], c[1]) for c in current_candidates])
-    return candidate_matches
+    return results
```

