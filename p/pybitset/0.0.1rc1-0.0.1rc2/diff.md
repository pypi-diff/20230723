# Comparing `tmp/pybitset-0.0.1rc1.tar.gz` & `tmp/pybitset-0.0.1rc2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pybitset-0.0.1rc1.tar", last modified: Wed Jun 21 02:24:53 2023, max compression
+gzip compressed data, was "pybitset-0.0.1rc2.tar", last modified: Sun Jul 23 16:01:39 2023, max compression
```

## Comparing `pybitset-0.0.1rc1.tar` & `pybitset-0.0.1rc2.tar`

### file list

```diff
@@ -1,56 +1,56 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-21 02:24:53.116598 pybitset-0.0.1rc1/
--rw-r--r--   0 runner    (1001) docker     (123)       81 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     3412 2023-06-21 02:24:53.116598 pybitset-0.0.1rc1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2417 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/README.markdown
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-21 02:24:53.112598 pybitset-0.0.1rc1/cbitset/
--rw-r--r--   0 runner    (1001) docker     (123)       32 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/cbitset/.git
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-21 02:24:53.112598 pybitset-0.0.1rc1/cbitset/.github/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-21 02:24:53.112598 pybitset-0.0.1rc1/cbitset/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)     1262 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/cbitset/.github/workflows/msys2.yml
--rw-r--r--   0 runner    (1001) docker     (123)      778 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/cbitset/.github/workflows/ubuntu18.yml
--rw-r--r--   0 runner    (1001) docker     (123)      780 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/cbitset/.github/workflows/ubuntu20.yml
--rw-r--r--   0 runner    (1001) docker     (123)      448 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/cbitset/.github/workflows/vs16-arm-ci.yml
--rw-r--r--   0 runner    (1001) docker     (123)      723 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/cbitset/.github/workflows/vs16-ci.yml
--rw-r--r--   0 runner    (1001) docker     (123)      763 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/cbitset/.github/workflows/vs16-clang-ci.yml
--rw-r--r--   0 runner    (1001) docker     (123)      765 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/cbitset/.github/workflows/vs16-ninja-ci.yml
--rw-r--r--   0 runner    (1001) docker     (123)      246 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/cbitset/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)      108 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/cbitset/.travis.yml
--rw-r--r--   0 runner    (1001) docker     (123)      436 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/cbitset/CMakeLists.txt
--rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/cbitset/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      901 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/cbitset/Makefile
--rw-r--r--   0 runner    (1001) docker     (123)     2092 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/cbitset/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-21 02:24:53.112598 pybitset-0.0.1rc1/cbitset/benchmarks/
--rw-r--r--   0 runner    (1001) docker     (123)      261 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/cbitset/benchmarks/CMakeLists.txt
--rw-r--r--   0 runner    (1001) docker     (123)     2740 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/cbitset/benchmarks/benchmark.c
--rw-r--r--   0 runner    (1001) docker     (123)     5487 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/cbitset/benchmarks/lemirebenchmark.c
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-21 02:24:53.112598 pybitset-0.0.1rc1/cbitset/include/
--rw-r--r--   0 runner    (1001) docker     (123)      300 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/cbitset/include/CMakeLists.txt
--rw-r--r--   0 runner    (1001) docker     (123)     8500 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/cbitset/include/bitset.h
--rw-r--r--   0 runner    (1001) docker     (123)     2851 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/cbitset/include/portability.h
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-21 02:24:53.116598 pybitset-0.0.1rc1/cbitset/src/
--rw-r--r--   0 runner    (1001) docker     (123)      185 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/cbitset/src/CMakeLists.txt
--rw-r--r--   0 runner    (1001) docker     (123)    14273 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/cbitset/src/bitset.c
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-21 02:24:53.116598 pybitset-0.0.1rc1/cbitset/tests/
--rw-r--r--   0 runner    (1001) docker     (123)       93 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/cbitset/tests/CMakeLists.txt
--rw-r--r--   0 runner    (1001) docker     (123)     6875 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/cbitset/tests/unit.c
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-21 02:24:53.116598 pybitset-0.0.1rc1/pybitset/
--rw-r--r--   0 runner    (1001) docker     (123)      141 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/pybitset/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-21 02:24:53.116598 pybitset-0.0.1rc1/pybitset/backends/
--rw-r--r--   0 runner    (1001) docker     (123)      466 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/pybitset/backends/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-21 02:24:53.116598 pybitset-0.0.1rc1/pybitset/backends/cffi/
--rw-r--r--   0 runner    (1001) docker     (123)     4558 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/pybitset/backends/cffi/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5992 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/pybitset/backends/cffi/build.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-21 02:24:53.116598 pybitset-0.0.1rc1/pybitset/backends/cython/
--rw-r--r--   0 runner    (1001) docker     (123)      130 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/pybitset/backends/cython/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)   390132 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/pybitset/backends/cython/_bitset.c
--rw-r--r--   0 runner    (1001) docker     (123)     6912 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/pybitset/backends/cython/_bitset.pyx
--rw-r--r--   0 runner    (1001) docker     (123)     2656 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/pybitset/backends/cython/bitset.pxd
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-21 02:24:53.116598 pybitset-0.0.1rc1/pybitset.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     3412 2023-06-21 02:24:53.000000 pybitset-0.0.1rc1/pybitset.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1206 2023-06-21 02:24:53.000000 pybitset-0.0.1rc1/pybitset.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-06-21 02:24:53.000000 pybitset-0.0.1rc1/pybitset.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-06-21 02:24:53.000000 pybitset-0.0.1rc1/pybitset.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)       12 2023-06-21 02:24:53.000000 pybitset-0.0.1rc1/pybitset.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        9 2023-06-21 02:24:53.000000 pybitset-0.0.1rc1/pybitset.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-06-21 02:24:53.116598 pybitset-0.0.1rc1/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     4037 2023-06-21 02:24:37.000000 pybitset-0.0.1rc1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:01:39.739250 pybitset-0.0.1rc2/
+-rw-r--r--   0 runner    (1001) docker     (123)       81 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     3412 2023-07-23 16:01:39.739250 pybitset-0.0.1rc2/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2417 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/README.markdown
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:01:39.731250 pybitset-0.0.1rc2/cbitset/
+-rw-r--r--   0 runner    (1001) docker     (123)       32 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/cbitset/.git
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:01:39.731250 pybitset-0.0.1rc2/cbitset/.github/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:01:39.735250 pybitset-0.0.1rc2/cbitset/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)     1262 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/cbitset/.github/workflows/msys2.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      778 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/cbitset/.github/workflows/ubuntu18.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      780 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/cbitset/.github/workflows/ubuntu20.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      448 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/cbitset/.github/workflows/vs16-arm-ci.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      723 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/cbitset/.github/workflows/vs16-ci.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      763 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/cbitset/.github/workflows/vs16-clang-ci.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      765 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/cbitset/.github/workflows/vs16-ninja-ci.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      246 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/cbitset/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)      108 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/cbitset/.travis.yml
+-rw-r--r--   0 runner    (1001) docker     (123)      436 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/cbitset/CMakeLists.txt
+-rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/cbitset/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      901 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/cbitset/Makefile
+-rw-r--r--   0 runner    (1001) docker     (123)     2092 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/cbitset/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:01:39.735250 pybitset-0.0.1rc2/cbitset/benchmarks/
+-rw-r--r--   0 runner    (1001) docker     (123)      261 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/cbitset/benchmarks/CMakeLists.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     2740 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/cbitset/benchmarks/benchmark.c
+-rw-r--r--   0 runner    (1001) docker     (123)     5487 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/cbitset/benchmarks/lemirebenchmark.c
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:01:39.735250 pybitset-0.0.1rc2/cbitset/include/
+-rw-r--r--   0 runner    (1001) docker     (123)      300 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/cbitset/include/CMakeLists.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     8500 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/cbitset/include/bitset.h
+-rw-r--r--   0 runner    (1001) docker     (123)     2851 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/cbitset/include/portability.h
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:01:39.735250 pybitset-0.0.1rc2/cbitset/src/
+-rw-r--r--   0 runner    (1001) docker     (123)      185 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/cbitset/src/CMakeLists.txt
+-rw-r--r--   0 runner    (1001) docker     (123)    14273 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/cbitset/src/bitset.c
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:01:39.735250 pybitset-0.0.1rc2/cbitset/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)       93 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/cbitset/tests/CMakeLists.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     6875 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/cbitset/tests/unit.c
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:01:39.735250 pybitset-0.0.1rc2/pybitset/
+-rw-r--r--   0 runner    (1001) docker     (123)      141 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/pybitset/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:01:39.735250 pybitset-0.0.1rc2/pybitset/backends/
+-rw-r--r--   0 runner    (1001) docker     (123)      466 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/pybitset/backends/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:01:39.735250 pybitset-0.0.1rc2/pybitset/backends/cffi/
+-rw-r--r--   0 runner    (1001) docker     (123)     4558 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/pybitset/backends/cffi/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5992 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/pybitset/backends/cffi/build.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:01:39.739250 pybitset-0.0.1rc2/pybitset/backends/cython/
+-rw-r--r--   0 runner    (1001) docker     (123)      130 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/pybitset/backends/cython/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)   671874 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/pybitset/backends/cython/_bitset.c
+-rw-r--r--   0 runner    (1001) docker     (123)     6927 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/pybitset/backends/cython/_bitset.pyx
+-rw-r--r--   0 runner    (1001) docker     (123)     2686 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/pybitset/backends/cython/bitset.pxd
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 16:01:39.735250 pybitset-0.0.1rc2/pybitset.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     3412 2023-07-23 16:01:39.000000 pybitset-0.0.1rc2/pybitset.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1206 2023-07-23 16:01:39.000000 pybitset-0.0.1rc2/pybitset.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 16:01:39.000000 pybitset-0.0.1rc2/pybitset.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 16:01:39.000000 pybitset-0.0.1rc2/pybitset.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)       12 2023-07-23 16:01:39.000000 pybitset-0.0.1rc2/pybitset.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-23 16:01:39.000000 pybitset-0.0.1rc2/pybitset.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 16:01:39.739250 pybitset-0.0.1rc2/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     4037 2023-07-23 16:01:21.000000 pybitset-0.0.1rc2/setup.py
```

### Comparing `pybitset-0.0.1rc1/PKG-INFO` & `pybitset-0.0.1rc2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pybitset
-Version: 0.0.1rc1
+Version: 0.0.1rc2
 Summary: python binding for cbitset
 Home-page: https://github.com/synodriver/pybitset
 Author: synodriver
 Author-email: diguohuangjiajinweijun@gmail.com
 License: BSD
 Keywords: bitset
 Classifier: Development Status :: 3 - Alpha
```

### Comparing `pybitset-0.0.1rc1/README.markdown` & `pybitset-0.0.1rc2/README.markdown`

 * *Files identical despite different names*

### Comparing `pybitset-0.0.1rc1/cbitset/.github/workflows/msys2.yml` & `pybitset-0.0.1rc2/cbitset/.github/workflows/msys2.yml`

 * *Files identical despite different names*

### Comparing `pybitset-0.0.1rc1/cbitset/.github/workflows/ubuntu18.yml` & `pybitset-0.0.1rc2/cbitset/.github/workflows/ubuntu18.yml`

 * *Files identical despite different names*

### Comparing `pybitset-0.0.1rc1/cbitset/.github/workflows/ubuntu20.yml` & `pybitset-0.0.1rc2/cbitset/.github/workflows/ubuntu20.yml`

 * *Files identical despite different names*

### Comparing `pybitset-0.0.1rc1/cbitset/.github/workflows/vs16-ci.yml` & `pybitset-0.0.1rc2/cbitset/.github/workflows/vs16-ci.yml`

 * *Files identical despite different names*

### Comparing `pybitset-0.0.1rc1/cbitset/.github/workflows/vs16-clang-ci.yml` & `pybitset-0.0.1rc2/cbitset/.github/workflows/vs16-clang-ci.yml`

 * *Files identical despite different names*

### Comparing `pybitset-0.0.1rc1/cbitset/.github/workflows/vs16-ninja-ci.yml` & `pybitset-0.0.1rc2/cbitset/.github/workflows/vs16-ninja-ci.yml`

 * *Files identical despite different names*

### Comparing `pybitset-0.0.1rc1/cbitset/LICENSE` & `pybitset-0.0.1rc2/cbitset/LICENSE`

 * *Files identical despite different names*

### Comparing `pybitset-0.0.1rc1/cbitset/Makefile` & `pybitset-0.0.1rc2/cbitset/Makefile`

 * *Files identical despite different names*

### Comparing `pybitset-0.0.1rc1/cbitset/README.md` & `pybitset-0.0.1rc2/cbitset/README.md`

 * *Files identical despite different names*

### Comparing `pybitset-0.0.1rc1/cbitset/benchmarks/benchmark.c` & `pybitset-0.0.1rc2/cbitset/benchmarks/benchmark.c`

 * *Files identical despite different names*

### Comparing `pybitset-0.0.1rc1/cbitset/benchmarks/lemirebenchmark.c` & `pybitset-0.0.1rc2/cbitset/benchmarks/lemirebenchmark.c`

 * *Files identical despite different names*

### Comparing `pybitset-0.0.1rc1/cbitset/include/bitset.h` & `pybitset-0.0.1rc2/cbitset/include/bitset.h`

 * *Files identical despite different names*

### Comparing `pybitset-0.0.1rc1/cbitset/include/portability.h` & `pybitset-0.0.1rc2/cbitset/include/portability.h`

 * *Files identical despite different names*

### Comparing `pybitset-0.0.1rc1/cbitset/src/bitset.c` & `pybitset-0.0.1rc2/cbitset/src/bitset.c`

 * *Files identical despite different names*

### Comparing `pybitset-0.0.1rc1/cbitset/tests/unit.c` & `pybitset-0.0.1rc2/cbitset/tests/unit.c`

 * *Files identical despite different names*

### Comparing `pybitset-0.0.1rc1/pybitset/backends/cffi/__init__.py` & `pybitset-0.0.1rc2/pybitset/backends/cffi/__init__.py`

 * *Files identical despite different names*

### Comparing `pybitset-0.0.1rc1/pybitset/backends/cffi/build.py` & `pybitset-0.0.1rc2/pybitset/backends/cffi/build.py`

 * *Files identical despite different names*

### Comparing `pybitset-0.0.1rc1/pybitset/backends/cython/_bitset.c` & `pybitset-0.0.1rc2/pybitset/backends/cython/_bitset.c`

 * *Files 26% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-/* Generated by Cython 0.29.35 */
+/* Generated by Cython 3.0.0 */
 
 /* BEGIN: Cython Metadata
 {
     "distutils": {
         "depends": [
             "cbitset\\include\\bitset.h"
         ],
@@ -18,28 +18,40 @@
     "module_name": "pybitset.backends.cython._bitset"
 }
 END: Cython Metadata */
 
 #ifndef PY_SSIZE_T_CLEAN
 #define PY_SSIZE_T_CLEAN
 #endif /* PY_SSIZE_T_CLEAN */
+#if defined(CYTHON_LIMITED_API) && 0
+  #ifndef Py_LIMITED_API
+    #if CYTHON_LIMITED_API+0 > 0x03030000
+      #define Py_LIMITED_API CYTHON_LIMITED_API
+    #else
+      #define Py_LIMITED_API 0x03030000
+    #endif
+  #endif
+#endif
+
 #include "Python.h"
 #ifndef Py_PYTHON_H
     #error Python headers needed to compile C extensions, please install development version of Python.
-#elif PY_VERSION_HEX < 0x02060000 || (0x03000000 <= PY_VERSION_HEX && PY_VERSION_HEX < 0x03030000)
-    #error Cython requires Python 2.6+ or Python 3.3+.
+#elif PY_VERSION_HEX < 0x02070000 || (0x03000000 <= PY_VERSION_HEX && PY_VERSION_HEX < 0x03030000)
+    #error Cython requires Python 2.7+ or Python 3.3+.
 #else
-#define CYTHON_ABI "0_29_35"
-#define CYTHON_HEX_VERSION 0x001D23F0
+#define CYTHON_ABI "3_0_0"
+#define __PYX_ABI_MODULE_NAME "_cython_" CYTHON_ABI
+#define __PYX_TYPE_MODULE_PREFIX __PYX_ABI_MODULE_NAME "."
+#define CYTHON_HEX_VERSION 0x030000F0
 #define CYTHON_FUTURE_DIVISION 1
 #include <stddef.h>
 #ifndef offsetof
   #define offsetof(type, member) ( (size_t) & ((type*)0) -> member )
 #endif
-#if !defined(WIN32) && !defined(MS_WINDOWS)
+#if !defined(_WIN32) && !defined(WIN32) && !defined(MS_WINDOWS)
   #ifndef __stdcall
     #define __stdcall
   #endif
   #ifndef __cdecl
     #define __cdecl
   #endif
   #ifndef __fastcall
@@ -50,31 +62,90 @@
   #define DL_IMPORT(t) t
 #endif
 #ifndef DL_EXPORT
   #define DL_EXPORT(t) t
 #endif
 #define __PYX_COMMA ,
 #ifndef HAVE_LONG_LONG
-  #if PY_VERSION_HEX >= 0x02070000
-    #define HAVE_LONG_LONG
-  #endif
+  #define HAVE_LONG_LONG
 #endif
 #ifndef PY_LONG_LONG
   #define PY_LONG_LONG LONG_LONG
 #endif
 #ifndef Py_HUGE_VAL
   #define Py_HUGE_VAL HUGE_VAL
 #endif
-#ifdef PYPY_VERSION
+#if defined(GRAALVM_PYTHON)
+  /* For very preliminary testing purposes. Most variables are set the same as PyPy.
+     The existence of this section does not imply that anything works or is even tested */
+  #define CYTHON_COMPILING_IN_PYPY 0
+  #define CYTHON_COMPILING_IN_CPYTHON 0
+  #define CYTHON_COMPILING_IN_LIMITED_API 0
+  #define CYTHON_COMPILING_IN_GRAAL 1
+  #define CYTHON_COMPILING_IN_NOGIL 0
+  #undef CYTHON_USE_TYPE_SLOTS
+  #define CYTHON_USE_TYPE_SLOTS 0
+  #undef CYTHON_USE_TYPE_SPECS
+  #define CYTHON_USE_TYPE_SPECS 0
+  #undef CYTHON_USE_PYTYPE_LOOKUP
+  #define CYTHON_USE_PYTYPE_LOOKUP 0
+  #if PY_VERSION_HEX < 0x03050000
+    #undef CYTHON_USE_ASYNC_SLOTS
+    #define CYTHON_USE_ASYNC_SLOTS 0
+  #elif !defined(CYTHON_USE_ASYNC_SLOTS)
+    #define CYTHON_USE_ASYNC_SLOTS 1
+  #endif
+  #undef CYTHON_USE_PYLIST_INTERNALS
+  #define CYTHON_USE_PYLIST_INTERNALS 0
+  #undef CYTHON_USE_UNICODE_INTERNALS
+  #define CYTHON_USE_UNICODE_INTERNALS 0
+  #undef CYTHON_USE_UNICODE_WRITER
+  #define CYTHON_USE_UNICODE_WRITER 0
+  #undef CYTHON_USE_PYLONG_INTERNALS
+  #define CYTHON_USE_PYLONG_INTERNALS 0
+  #undef CYTHON_AVOID_BORROWED_REFS
+  #define CYTHON_AVOID_BORROWED_REFS 1
+  #undef CYTHON_ASSUME_SAFE_MACROS
+  #define CYTHON_ASSUME_SAFE_MACROS 0
+  #undef CYTHON_UNPACK_METHODS
+  #define CYTHON_UNPACK_METHODS 0
+  #undef CYTHON_FAST_THREAD_STATE
+  #define CYTHON_FAST_THREAD_STATE 0
+  #undef CYTHON_FAST_GIL
+  #define CYTHON_FAST_GIL 0
+  #undef CYTHON_METH_FASTCALL
+  #define CYTHON_METH_FASTCALL 0
+  #undef CYTHON_FAST_PYCALL
+  #define CYTHON_FAST_PYCALL 0
+  #ifndef CYTHON_PEP487_INIT_SUBCLASS
+    #define CYTHON_PEP487_INIT_SUBCLASS (PY_MAJOR_VERSION >= 3)
+  #endif
+  #undef CYTHON_PEP489_MULTI_PHASE_INIT
+  #define CYTHON_PEP489_MULTI_PHASE_INIT 1
+  #undef CYTHON_USE_MODULE_STATE
+  #define CYTHON_USE_MODULE_STATE 0
+  #undef CYTHON_USE_TP_FINALIZE
+  #define CYTHON_USE_TP_FINALIZE 0
+  #undef CYTHON_USE_DICT_VERSIONS
+  #define CYTHON_USE_DICT_VERSIONS 0
+  #undef CYTHON_USE_EXC_INFO_STACK
+  #define CYTHON_USE_EXC_INFO_STACK 0
+  #ifndef CYTHON_UPDATE_DESCRIPTOR_DOC
+    #define CYTHON_UPDATE_DESCRIPTOR_DOC 0
+  #endif
+#elif defined(PYPY_VERSION)
   #define CYTHON_COMPILING_IN_PYPY 1
-  #define CYTHON_COMPILING_IN_PYSTON 0
   #define CYTHON_COMPILING_IN_CPYTHON 0
+  #define CYTHON_COMPILING_IN_LIMITED_API 0
+  #define CYTHON_COMPILING_IN_GRAAL 0
   #define CYTHON_COMPILING_IN_NOGIL 0
   #undef CYTHON_USE_TYPE_SLOTS
   #define CYTHON_USE_TYPE_SLOTS 0
+  #undef CYTHON_USE_TYPE_SPECS
+  #define CYTHON_USE_TYPE_SPECS 0
   #undef CYTHON_USE_PYTYPE_LOOKUP
   #define CYTHON_USE_PYTYPE_LOOKUP 0
   #if PY_VERSION_HEX < 0x03050000
     #undef CYTHON_USE_ASYNC_SLOTS
     #define CYTHON_USE_ASYNC_SLOTS 0
   #elif !defined(CYTHON_USE_ASYNC_SLOTS)
     #define CYTHON_USE_ASYNC_SLOTS 1
@@ -91,80 +162,102 @@
   #define CYTHON_AVOID_BORROWED_REFS 1
   #undef CYTHON_ASSUME_SAFE_MACROS
   #define CYTHON_ASSUME_SAFE_MACROS 0
   #undef CYTHON_UNPACK_METHODS
   #define CYTHON_UNPACK_METHODS 0
   #undef CYTHON_FAST_THREAD_STATE
   #define CYTHON_FAST_THREAD_STATE 0
+  #undef CYTHON_FAST_GIL
+  #define CYTHON_FAST_GIL 0
+  #undef CYTHON_METH_FASTCALL
+  #define CYTHON_METH_FASTCALL 0
   #undef CYTHON_FAST_PYCALL
   #define CYTHON_FAST_PYCALL 0
+  #ifndef CYTHON_PEP487_INIT_SUBCLASS
+    #define CYTHON_PEP487_INIT_SUBCLASS (PY_MAJOR_VERSION >= 3)
+  #endif
   #if PY_VERSION_HEX < 0x03090000
     #undef CYTHON_PEP489_MULTI_PHASE_INIT
     #define CYTHON_PEP489_MULTI_PHASE_INIT 0
   #elif !defined(CYTHON_PEP489_MULTI_PHASE_INIT)
     #define CYTHON_PEP489_MULTI_PHASE_INIT 1
   #endif
+  #undef CYTHON_USE_MODULE_STATE
+  #define CYTHON_USE_MODULE_STATE 0
   #undef CYTHON_USE_TP_FINALIZE
-  #define CYTHON_USE_TP_FINALIZE 0
+  #define CYTHON_USE_TP_FINALIZE (PY_VERSION_HEX >= 0x030400a1 && PYPY_VERSION_NUM >= 0x07030C00)
   #undef CYTHON_USE_DICT_VERSIONS
   #define CYTHON_USE_DICT_VERSIONS 0
   #undef CYTHON_USE_EXC_INFO_STACK
   #define CYTHON_USE_EXC_INFO_STACK 0
   #ifndef CYTHON_UPDATE_DESCRIPTOR_DOC
     #define CYTHON_UPDATE_DESCRIPTOR_DOC 0
   #endif
-#elif defined(PYSTON_VERSION)
+#elif defined(CYTHON_LIMITED_API)
   #define CYTHON_COMPILING_IN_PYPY 0
-  #define CYTHON_COMPILING_IN_PYSTON 1
   #define CYTHON_COMPILING_IN_CPYTHON 0
+  #define CYTHON_COMPILING_IN_LIMITED_API 1
+  #define CYTHON_COMPILING_IN_GRAAL 0
   #define CYTHON_COMPILING_IN_NOGIL 0
-  #ifndef CYTHON_USE_TYPE_SLOTS
-    #define CYTHON_USE_TYPE_SLOTS 1
-  #endif
+  #undef CYTHON_CLINE_IN_TRACEBACK
+  #define CYTHON_CLINE_IN_TRACEBACK 0
+  #undef CYTHON_USE_TYPE_SLOTS
+  #define CYTHON_USE_TYPE_SLOTS 0
+  #undef CYTHON_USE_TYPE_SPECS
+  #define CYTHON_USE_TYPE_SPECS 1
   #undef CYTHON_USE_PYTYPE_LOOKUP
   #define CYTHON_USE_PYTYPE_LOOKUP 0
   #undef CYTHON_USE_ASYNC_SLOTS
   #define CYTHON_USE_ASYNC_SLOTS 0
   #undef CYTHON_USE_PYLIST_INTERNALS
   #define CYTHON_USE_PYLIST_INTERNALS 0
-  #ifndef CYTHON_USE_UNICODE_INTERNALS
-    #define CYTHON_USE_UNICODE_INTERNALS 1
+  #undef CYTHON_USE_UNICODE_INTERNALS
+  #define CYTHON_USE_UNICODE_INTERNALS 0
+  #ifndef CYTHON_USE_UNICODE_WRITER
+    #define CYTHON_USE_UNICODE_WRITER 0
   #endif
-  #undef CYTHON_USE_UNICODE_WRITER
-  #define CYTHON_USE_UNICODE_WRITER 0
   #undef CYTHON_USE_PYLONG_INTERNALS
   #define CYTHON_USE_PYLONG_INTERNALS 0
   #ifndef CYTHON_AVOID_BORROWED_REFS
     #define CYTHON_AVOID_BORROWED_REFS 0
   #endif
-  #ifndef CYTHON_ASSUME_SAFE_MACROS
-    #define CYTHON_ASSUME_SAFE_MACROS 1
-  #endif
-  #ifndef CYTHON_UNPACK_METHODS
-    #define CYTHON_UNPACK_METHODS 1
-  #endif
+  #undef CYTHON_ASSUME_SAFE_MACROS
+  #define CYTHON_ASSUME_SAFE_MACROS 0
+  #undef CYTHON_UNPACK_METHODS
+  #define CYTHON_UNPACK_METHODS 0
   #undef CYTHON_FAST_THREAD_STATE
   #define CYTHON_FAST_THREAD_STATE 0
+  #undef CYTHON_FAST_GIL
+  #define CYTHON_FAST_GIL 0
+  #undef CYTHON_METH_FASTCALL
+  #define CYTHON_METH_FASTCALL 0
   #undef CYTHON_FAST_PYCALL
   #define CYTHON_FAST_PYCALL 0
+  #ifndef CYTHON_PEP487_INIT_SUBCLASS
+    #define CYTHON_PEP487_INIT_SUBCLASS 1
+  #endif
   #undef CYTHON_PEP489_MULTI_PHASE_INIT
   #define CYTHON_PEP489_MULTI_PHASE_INIT 0
-  #undef CYTHON_USE_TP_FINALIZE
-  #define CYTHON_USE_TP_FINALIZE 0
+  #undef CYTHON_USE_MODULE_STATE
+  #define CYTHON_USE_MODULE_STATE 1
+  #ifndef CYTHON_USE_TP_FINALIZE
+    #define CYTHON_USE_TP_FINALIZE 1
+  #endif
   #undef CYTHON_USE_DICT_VERSIONS
   #define CYTHON_USE_DICT_VERSIONS 0
   #undef CYTHON_USE_EXC_INFO_STACK
   #define CYTHON_USE_EXC_INFO_STACK 0
   #ifndef CYTHON_UPDATE_DESCRIPTOR_DOC
     #define CYTHON_UPDATE_DESCRIPTOR_DOC 0
   #endif
 #elif defined(PY_NOGIL)
   #define CYTHON_COMPILING_IN_PYPY 0
-  #define CYTHON_COMPILING_IN_PYSTON 0
   #define CYTHON_COMPILING_IN_CPYTHON 0
+  #define CYTHON_COMPILING_IN_LIMITED_API 0
+  #define CYTHON_COMPILING_IN_GRAAL 0
   #define CYTHON_COMPILING_IN_NOGIL 1
   #ifndef CYTHON_USE_TYPE_SLOTS
     #define CYTHON_USE_TYPE_SLOTS 1
   #endif
   #undef CYTHON_USE_PYTYPE_LOOKUP
   #define CYTHON_USE_PYTYPE_LOOKUP 0
   #ifndef CYTHON_USE_ASYNC_SLOTS
@@ -200,37 +293,35 @@
   #endif
   #undef CYTHON_USE_DICT_VERSIONS
   #define CYTHON_USE_DICT_VERSIONS 0
   #undef CYTHON_USE_EXC_INFO_STACK
   #define CYTHON_USE_EXC_INFO_STACK 0
 #else
   #define CYTHON_COMPILING_IN_PYPY 0
-  #define CYTHON_COMPILING_IN_PYSTON 0
   #define CYTHON_COMPILING_IN_CPYTHON 1
+  #define CYTHON_COMPILING_IN_LIMITED_API 0
+  #define CYTHON_COMPILING_IN_GRAAL 0
   #define CYTHON_COMPILING_IN_NOGIL 0
   #ifndef CYTHON_USE_TYPE_SLOTS
     #define CYTHON_USE_TYPE_SLOTS 1
   #endif
-  #if PY_VERSION_HEX < 0x02070000
-    #undef CYTHON_USE_PYTYPE_LOOKUP
-    #define CYTHON_USE_PYTYPE_LOOKUP 0
-  #elif !defined(CYTHON_USE_PYTYPE_LOOKUP)
+  #ifndef CYTHON_USE_TYPE_SPECS
+    #define CYTHON_USE_TYPE_SPECS 0
+  #endif
+  #ifndef CYTHON_USE_PYTYPE_LOOKUP
     #define CYTHON_USE_PYTYPE_LOOKUP 1
   #endif
   #if PY_MAJOR_VERSION < 3
     #undef CYTHON_USE_ASYNC_SLOTS
     #define CYTHON_USE_ASYNC_SLOTS 0
   #elif !defined(CYTHON_USE_ASYNC_SLOTS)
     #define CYTHON_USE_ASYNC_SLOTS 1
   #endif
-  #if PY_VERSION_HEX < 0x02070000
-    #undef CYTHON_USE_PYLONG_INTERNALS
-    #define CYTHON_USE_PYLONG_INTERNALS 0
-  #elif !defined(CYTHON_USE_PYLONG_INTERNALS)
-    #define CYTHON_USE_PYLONG_INTERNALS (PY_VERSION_HEX < 0x030C00A5)
+  #ifndef CYTHON_USE_PYLONG_INTERNALS
+    #define CYTHON_USE_PYLONG_INTERNALS 1
   #endif
   #ifndef CYTHON_USE_PYLIST_INTERNALS
     #define CYTHON_USE_PYLIST_INTERNALS 1
   #endif
   #ifndef CYTHON_USE_UNICODE_INTERNALS
     #define CYTHON_USE_UNICODE_INTERNALS 1
   #endif
@@ -245,45 +336,67 @@
   #endif
   #ifndef CYTHON_ASSUME_SAFE_MACROS
     #define CYTHON_ASSUME_SAFE_MACROS 1
   #endif
   #ifndef CYTHON_UNPACK_METHODS
     #define CYTHON_UNPACK_METHODS 1
   #endif
-  #if PY_VERSION_HEX >= 0x030B00A4
-    #undef CYTHON_FAST_THREAD_STATE
-    #define CYTHON_FAST_THREAD_STATE 0
-  #elif !defined(CYTHON_FAST_THREAD_STATE)
+  #ifndef CYTHON_FAST_THREAD_STATE
     #define CYTHON_FAST_THREAD_STATE 1
   #endif
+  #ifndef CYTHON_FAST_GIL
+    #define CYTHON_FAST_GIL (PY_MAJOR_VERSION < 3 || PY_VERSION_HEX >= 0x03060000 && PY_VERSION_HEX < 0x030C00A6)
+  #endif
+  #ifndef CYTHON_METH_FASTCALL
+    #define CYTHON_METH_FASTCALL (PY_VERSION_HEX >= 0x030700A1)
+  #endif
   #ifndef CYTHON_FAST_PYCALL
-    #define CYTHON_FAST_PYCALL (PY_VERSION_HEX < 0x030A0000)
+    #define CYTHON_FAST_PYCALL 1
   #endif
-  #ifndef CYTHON_PEP489_MULTI_PHASE_INIT
-    #define CYTHON_PEP489_MULTI_PHASE_INIT (PY_VERSION_HEX >= 0x03050000)
+  #ifndef CYTHON_PEP487_INIT_SUBCLASS
+    #define CYTHON_PEP487_INIT_SUBCLASS 1
   #endif
-  #ifndef CYTHON_USE_TP_FINALIZE
-    #define CYTHON_USE_TP_FINALIZE (PY_VERSION_HEX >= 0x030400a1)
+  #if PY_VERSION_HEX < 0x03050000
+    #undef CYTHON_PEP489_MULTI_PHASE_INIT
+    #define CYTHON_PEP489_MULTI_PHASE_INIT 0
+  #elif !defined(CYTHON_PEP489_MULTI_PHASE_INIT)
+    #define CYTHON_PEP489_MULTI_PHASE_INIT 1
   #endif
-  #ifndef CYTHON_USE_DICT_VERSIONS
-    #define CYTHON_USE_DICT_VERSIONS ((PY_VERSION_HEX >= 0x030600B1) && (PY_VERSION_HEX < 0x030C00A5))
+  #ifndef CYTHON_USE_MODULE_STATE
+    #define CYTHON_USE_MODULE_STATE 0
   #endif
-  #if PY_VERSION_HEX >= 0x030B00A4
+  #if PY_VERSION_HEX < 0x030400a1
+    #undef CYTHON_USE_TP_FINALIZE
+    #define CYTHON_USE_TP_FINALIZE 0
+  #elif !defined(CYTHON_USE_TP_FINALIZE)
+    #define CYTHON_USE_TP_FINALIZE 1
+  #endif
+  #if PY_VERSION_HEX < 0x030600B1
+    #undef CYTHON_USE_DICT_VERSIONS
+    #define CYTHON_USE_DICT_VERSIONS 0
+  #elif !defined(CYTHON_USE_DICT_VERSIONS)
+    #define CYTHON_USE_DICT_VERSIONS  (PY_VERSION_HEX < 0x030C00A5)
+  #endif
+  #if PY_VERSION_HEX < 0x030700A3
     #undef CYTHON_USE_EXC_INFO_STACK
     #define CYTHON_USE_EXC_INFO_STACK 0
   #elif !defined(CYTHON_USE_EXC_INFO_STACK)
-    #define CYTHON_USE_EXC_INFO_STACK (PY_VERSION_HEX >= 0x030700A3)
+    #define CYTHON_USE_EXC_INFO_STACK 1
   #endif
   #ifndef CYTHON_UPDATE_DESCRIPTOR_DOC
     #define CYTHON_UPDATE_DESCRIPTOR_DOC 1
   #endif
 #endif
 #if !defined(CYTHON_FAST_PYCCALL)
 #define CYTHON_FAST_PYCCALL  (CYTHON_FAST_PYCALL && PY_VERSION_HEX >= 0x030600B1)
 #endif
+#if !defined(CYTHON_VECTORCALL)
+#define CYTHON_VECTORCALL  (CYTHON_FAST_PYCCALL && PY_VERSION_HEX >= 0x030800B1)
+#endif
+#define CYTHON_BACKPORT_VECTORCALL (CYTHON_METH_FASTCALL && PY_VERSION_HEX < 0x030800B1)
 #if CYTHON_USE_PYLONG_INTERNALS
   #if PY_MAJOR_VERSION < 3
     #include "longintrepr.h"
   #endif
   #undef SHIFT
   #undef BASE
   #undef MASK
@@ -305,78 +418,128 @@
   #elif defined (__STDC_VERSION__) && __STDC_VERSION__ >= 199901L
     #define CYTHON_RESTRICT restrict
   #else
     #define CYTHON_RESTRICT
   #endif
 #endif
 #ifndef CYTHON_UNUSED
+  #if defined(__cplusplus)
+    /* for clang __has_cpp_attribute(maybe_unused) is true even before C++17
+     * but leads to warnings with -pedantic, since it is a C++17 feature */
+    #if ((defined(_MSVC_LANG) && _MSVC_LANG >= 201703L) || __cplusplus >= 201703L)
+      #if __has_cpp_attribute(maybe_unused)
+        #define CYTHON_UNUSED [[maybe_unused]]
+      #endif
+    #endif
+  #endif
+#endif
+#ifndef CYTHON_UNUSED
 # if defined(__GNUC__)
 #   if !(defined(__cplusplus)) || (__GNUC__ > 3 || (__GNUC__ == 3 && __GNUC_MINOR__ >= 4))
 #     define CYTHON_UNUSED __attribute__ ((__unused__))
 #   else
 #     define CYTHON_UNUSED
 #   endif
 # elif defined(__ICC) || (defined(__INTEL_COMPILER) && !defined(_MSC_VER))
 #   define CYTHON_UNUSED __attribute__ ((__unused__))
 # else
 #   define CYTHON_UNUSED
 # endif
 #endif
-#ifndef CYTHON_MAYBE_UNUSED_VAR
+#ifndef CYTHON_UNUSED_VAR
 #  if defined(__cplusplus)
-     template<class T> void CYTHON_MAYBE_UNUSED_VAR( const T& ) { }
+     template<class T> void CYTHON_UNUSED_VAR( const T& ) { }
 #  else
-#    define CYTHON_MAYBE_UNUSED_VAR(x) (void)(x)
+#    define CYTHON_UNUSED_VAR(x) (void)(x)
 #  endif
 #endif
+#ifndef CYTHON_MAYBE_UNUSED_VAR
+  #define CYTHON_MAYBE_UNUSED_VAR(x) CYTHON_UNUSED_VAR(x)
+#endif
 #ifndef CYTHON_NCP_UNUSED
 # if CYTHON_COMPILING_IN_CPYTHON
 #  define CYTHON_NCP_UNUSED
 # else
 #  define CYTHON_NCP_UNUSED CYTHON_UNUSED
 # endif
 #endif
 #define __Pyx_void_to_None(void_result) ((void)(void_result), Py_INCREF(Py_None), Py_None)
 #ifdef _MSC_VER
     #ifndef _MSC_STDINT_H_
         #if _MSC_VER < 1300
-           typedef unsigned char     uint8_t;
-           typedef unsigned int      uint32_t;
+            typedef unsigned char     uint8_t;
+            typedef unsigned short    uint16_t;
+            typedef unsigned int      uint32_t;
         #else
-           typedef unsigned __int8   uint8_t;
-           typedef unsigned __int32  uint32_t;
+            typedef unsigned __int8   uint8_t;
+            typedef unsigned __int16  uint16_t;
+            typedef unsigned __int32  uint32_t;
+        #endif
+    #endif
+    #if _MSC_VER < 1300
+        #ifdef _WIN64
+            typedef unsigned long long  __pyx_uintptr_t;
+        #else
+            typedef unsigned int        __pyx_uintptr_t;
+        #endif
+    #else
+        #ifdef _WIN64
+            typedef unsigned __int64    __pyx_uintptr_t;
+        #else
+            typedef unsigned __int32    __pyx_uintptr_t;
         #endif
     #endif
 #else
-   #include <stdint.h>
+    #include <stdint.h>
+    typedef uintptr_t  __pyx_uintptr_t;
 #endif
 #ifndef CYTHON_FALLTHROUGH
-  #if defined(__cplusplus) && __cplusplus >= 201103L
-    #if __has_cpp_attribute(fallthrough)
-      #define CYTHON_FALLTHROUGH [[fallthrough]]
-    #elif __has_cpp_attribute(clang::fallthrough)
-      #define CYTHON_FALLTHROUGH [[clang::fallthrough]]
-    #elif __has_cpp_attribute(gnu::fallthrough)
-      #define CYTHON_FALLTHROUGH [[gnu::fallthrough]]
+  #if defined(__cplusplus)
+    /* for clang __has_cpp_attribute(fallthrough) is true even before C++17
+     * but leads to warnings with -pedantic, since it is a C++17 feature */
+    #if ((defined(_MSVC_LANG) && _MSVC_LANG >= 201703L) || __cplusplus >= 201703L)
+      #if __has_cpp_attribute(fallthrough)
+        #define CYTHON_FALLTHROUGH [[fallthrough]]
+      #endif
+    #endif
+    #ifndef CYTHON_FALLTHROUGH
+      #if __has_cpp_attribute(clang::fallthrough)
+        #define CYTHON_FALLTHROUGH [[clang::fallthrough]]
+      #elif __has_cpp_attribute(gnu::fallthrough)
+        #define CYTHON_FALLTHROUGH [[gnu::fallthrough]]
+      #endif
     #endif
   #endif
   #ifndef CYTHON_FALLTHROUGH
     #if __has_attribute(fallthrough)
       #define CYTHON_FALLTHROUGH __attribute__((fallthrough))
     #else
       #define CYTHON_FALLTHROUGH
     #endif
   #endif
-  #if defined(__clang__ ) && defined(__apple_build_version__)
+  #if defined(__clang__) && defined(__apple_build_version__)
     #if __apple_build_version__ < 7000000
       #undef  CYTHON_FALLTHROUGH
       #define CYTHON_FALLTHROUGH
     #endif
   #endif
 #endif
+#ifdef __cplusplus
+  template <typename T>
+  struct __PYX_IS_UNSIGNED_IMPL {static const bool value = T(0) < T(-1);};
+  #define __PYX_IS_UNSIGNED(type) (__PYX_IS_UNSIGNED_IMPL<type>::value)
+#else
+  #define __PYX_IS_UNSIGNED(type) (((type)-1) > 0)
+#endif
+#if CYTHON_COMPILING_IN_PYPY == 1
+  #define __PYX_NEED_TP_PRINT_SLOT  (PY_VERSION_HEX >= 0x030800b4 && PY_VERSION_HEX < 0x030A0000)
+#else
+  #define __PYX_NEED_TP_PRINT_SLOT  (PY_VERSION_HEX >= 0x030800b4 && PY_VERSION_HEX < 0x03090000)
+#endif
+#define __PYX_REINTERPRET_FUNCION(func_pointer, other_pointer) ((func_pointer)(void(*)(void))(other_pointer))
 
 #ifndef CYTHON_INLINE
   #if defined(__clang__)
     #define CYTHON_INLINE __inline__ __attribute__ ((__unused__))
   #elif defined(__GNUC__)
     #define CYTHON_INLINE __inline__
   #elif defined(_MSC_VER)
@@ -384,43 +547,40 @@
   #elif defined (__STDC_VERSION__) && __STDC_VERSION__ >= 199901L
     #define CYTHON_INLINE inline
   #else
     #define CYTHON_INLINE
   #endif
 #endif
 
-#if CYTHON_COMPILING_IN_PYPY && PY_VERSION_HEX < 0x02070600 && !defined(Py_OptimizeFlag)
-  #define Py_OptimizeFlag 0
-#endif
 #define __PYX_BUILD_PY_SSIZE_T "n"
 #define CYTHON_FORMAT_SSIZE_T "z"
 #if PY_MAJOR_VERSION < 3
   #define __Pyx_BUILTIN_MODULE_NAME "__builtin__"
-  #define __Pyx_PyCode_New(a, k, l, s, f, code, c, n, v, fv, cell, fn, name, fline, lnos)\
-          PyCode_New(a+k, l, s, f, code, c, n, v, fv, cell, fn, name, fline, lnos)
   #define __Pyx_DefaultClassType PyClass_Type
+  #define __Pyx_PyCode_New(a, p, k, l, s, f, code, c, n, v, fv, cell, fn, name, fline, lnos)\
+          PyCode_New(a+k, l, s, f, code, c, n, v, fv, cell, fn, name, fline, lnos)
 #else
   #define __Pyx_BUILTIN_MODULE_NAME "builtins"
   #define __Pyx_DefaultClassType PyType_Type
 #if PY_VERSION_HEX >= 0x030B00A1
-    static CYTHON_INLINE PyCodeObject* __Pyx_PyCode_New(int a, int k, int l, int s, int f,
+    static CYTHON_INLINE PyCodeObject* __Pyx_PyCode_New(int a, int p, int k, int l, int s, int f,
                                                     PyObject *code, PyObject *c, PyObject* n, PyObject *v,
                                                     PyObject *fv, PyObject *cell, PyObject* fn,
                                                     PyObject *name, int fline, PyObject *lnos) {
         PyObject *kwds=NULL, *argcount=NULL, *posonlyargcount=NULL, *kwonlyargcount=NULL;
-        PyObject *nlocals=NULL, *stacksize=NULL, *flags=NULL, *replace=NULL, *call_result=NULL, *empty=NULL;
+        PyObject *nlocals=NULL, *stacksize=NULL, *flags=NULL, *replace=NULL, *empty=NULL;
         const char *fn_cstr=NULL;
         const char *name_cstr=NULL;
-        PyCodeObject* co=NULL;
+        PyCodeObject *co=NULL, *result=NULL;
         PyObject *type, *value, *traceback;
         PyErr_Fetch(&type, &value, &traceback);
         if (!(kwds=PyDict_New())) goto end;
         if (!(argcount=PyLong_FromLong(a))) goto end;
         if (PyDict_SetItemString(kwds, "co_argcount", argcount) != 0) goto end;
-        if (!(posonlyargcount=PyLong_FromLong(0))) goto end;
+        if (!(posonlyargcount=PyLong_FromLong(p))) goto end;
         if (PyDict_SetItemString(kwds, "co_posonlyargcount", posonlyargcount) != 0) goto end;
         if (!(kwonlyargcount=PyLong_FromLong(k))) goto end;
         if (PyDict_SetItemString(kwds, "co_kwonlyargcount", kwonlyargcount) != 0) goto end;
         if (!(nlocals=PyLong_FromLong(l))) goto end;
         if (PyDict_SetItemString(kwds, "co_nlocals", nlocals) != 0) goto end;
         if (!(stacksize=PyLong_FromLong(s))) goto end;
         if (PyDict_SetItemString(kwds, "co_stacksize", stacksize) != 0) goto end;
@@ -432,104 +592,180 @@
         if (PyDict_SetItemString(kwds, "co_varnames", v) != 0) goto end;
         if (PyDict_SetItemString(kwds, "co_freevars", fv) != 0) goto end;
         if (PyDict_SetItemString(kwds, "co_cellvars", cell) != 0) goto end;
         if (PyDict_SetItemString(kwds, "co_linetable", lnos) != 0) goto end;
         if (!(fn_cstr=PyUnicode_AsUTF8AndSize(fn, NULL))) goto end;
         if (!(name_cstr=PyUnicode_AsUTF8AndSize(name, NULL))) goto end;
         if (!(co = PyCode_NewEmpty(fn_cstr, name_cstr, fline))) goto end;
-        if (!(replace = PyObject_GetAttrString((PyObject*)co, "replace"))) goto cleanup_code_too;
-        if (!(empty = PyTuple_New(0))) goto cleanup_code_too; // unfortunately __pyx_empty_tuple isn't available here
-        if (!(call_result = PyObject_Call(replace, empty, kwds))) goto cleanup_code_too;
-        Py_XDECREF((PyObject*)co);
-        co = (PyCodeObject*)call_result;
-        call_result = NULL;
-        if (0) {
-            cleanup_code_too:
-            Py_XDECREF((PyObject*)co);
-            co = NULL;
-        }
-        end:
+        if (!(replace = PyObject_GetAttrString((PyObject*)co, "replace"))) goto end;
+        if (!(empty = PyTuple_New(0))) goto end;
+        result = (PyCodeObject*) PyObject_Call(replace, empty, kwds);
+    end:
+        Py_XDECREF((PyObject*) co);
         Py_XDECREF(kwds);
         Py_XDECREF(argcount);
         Py_XDECREF(posonlyargcount);
         Py_XDECREF(kwonlyargcount);
         Py_XDECREF(nlocals);
         Py_XDECREF(stacksize);
         Py_XDECREF(replace);
-        Py_XDECREF(call_result);
         Py_XDECREF(empty);
         if (type) {
             PyErr_Restore(type, value, traceback);
         }
-        return co;
+        return result;
     }
+#elif PY_VERSION_HEX >= 0x030800B2 && !CYTHON_COMPILING_IN_PYPY
+  #define __Pyx_PyCode_New(a, p, k, l, s, f, code, c, n, v, fv, cell, fn, name, fline, lnos)\
+          PyCode_NewWithPosOnlyArgs(a, p, k, l, s, f, code, c, n, v, fv, cell, fn, name, fline, lnos)
 #else
-  #define __Pyx_PyCode_New(a, k, l, s, f, code, c, n, v, fv, cell, fn, name, fline, lnos)\
+  #define __Pyx_PyCode_New(a, p, k, l, s, f, code, c, n, v, fv, cell, fn, name, fline, lnos)\
           PyCode_New(a, k, l, s, f, code, c, n, v, fv, cell, fn, name, fline, lnos)
 #endif
-  #define __Pyx_DefaultClassType PyType_Type
+#endif
+#if PY_VERSION_HEX >= 0x030900A4 || defined(Py_IS_TYPE)
+  #define __Pyx_IS_TYPE(ob, type) Py_IS_TYPE(ob, type)
+#else
+  #define __Pyx_IS_TYPE(ob, type) (((const PyObject*)ob)->ob_type == (type))
+#endif
+#if PY_VERSION_HEX >= 0x030A00B1 || defined(Py_Is)
+  #define __Pyx_Py_Is(x, y)  Py_Is(x, y)
+#else
+  #define __Pyx_Py_Is(x, y) ((x) == (y))
+#endif
+#if PY_VERSION_HEX >= 0x030A00B1 || defined(Py_IsNone)
+  #define __Pyx_Py_IsNone(ob) Py_IsNone(ob)
+#else
+  #define __Pyx_Py_IsNone(ob) __Pyx_Py_Is((ob), Py_None)
+#endif
+#if PY_VERSION_HEX >= 0x030A00B1 || defined(Py_IsTrue)
+  #define __Pyx_Py_IsTrue(ob) Py_IsTrue(ob)
+#else
+  #define __Pyx_Py_IsTrue(ob) __Pyx_Py_Is((ob), Py_True)
+#endif
+#if PY_VERSION_HEX >= 0x030A00B1 || defined(Py_IsFalse)
+  #define __Pyx_Py_IsFalse(ob) Py_IsFalse(ob)
+#else
+  #define __Pyx_Py_IsFalse(ob) __Pyx_Py_Is((ob), Py_False)
+#endif
+#define __Pyx_NoneAsNull(obj)  (__Pyx_Py_IsNone(obj) ? NULL : (obj))
+#if PY_VERSION_HEX >= 0x030900F0 && !CYTHON_COMPILING_IN_PYPY
+  #define __Pyx_PyObject_GC_IsFinalized(o) PyObject_GC_IsFinalized(o)
+#else
+  #define __Pyx_PyObject_GC_IsFinalized(o) _PyGC_FINALIZED(o)
+#endif
+#ifndef CO_COROUTINE
+  #define CO_COROUTINE 0x80
+#endif
+#ifndef CO_ASYNC_GENERATOR
+  #define CO_ASYNC_GENERATOR 0x200
 #endif
 #ifndef Py_TPFLAGS_CHECKTYPES
   #define Py_TPFLAGS_CHECKTYPES 0
 #endif
 #ifndef Py_TPFLAGS_HAVE_INDEX
   #define Py_TPFLAGS_HAVE_INDEX 0
 #endif
 #ifndef Py_TPFLAGS_HAVE_NEWBUFFER
   #define Py_TPFLAGS_HAVE_NEWBUFFER 0
 #endif
 #ifndef Py_TPFLAGS_HAVE_FINALIZE
   #define Py_TPFLAGS_HAVE_FINALIZE 0
 #endif
+#ifndef Py_TPFLAGS_SEQUENCE
+  #define Py_TPFLAGS_SEQUENCE 0
+#endif
+#ifndef Py_TPFLAGS_MAPPING
+  #define Py_TPFLAGS_MAPPING 0
+#endif
 #ifndef METH_STACKLESS
   #define METH_STACKLESS 0
 #endif
 #if PY_VERSION_HEX <= 0x030700A3 || !defined(METH_FASTCALL)
   #ifndef METH_FASTCALL
      #define METH_FASTCALL 0x80
   #endif
   typedef PyObject *(*__Pyx_PyCFunctionFast) (PyObject *self, PyObject *const *args, Py_ssize_t nargs);
   typedef PyObject *(*__Pyx_PyCFunctionFastWithKeywords) (PyObject *self, PyObject *const *args,
                                                           Py_ssize_t nargs, PyObject *kwnames);
 #else
   #define __Pyx_PyCFunctionFast _PyCFunctionFast
   #define __Pyx_PyCFunctionFastWithKeywords _PyCFunctionFastWithKeywords
 #endif
-#if CYTHON_FAST_PYCCALL
-#define __Pyx_PyFastCFunction_Check(func)\
-    ((PyCFunction_Check(func) && (METH_FASTCALL == (PyCFunction_GET_FLAGS(func) & ~(METH_CLASS | METH_STATIC | METH_COEXIST | METH_KEYWORDS | METH_STACKLESS)))))
+#if CYTHON_METH_FASTCALL
+  #define __Pyx_METH_FASTCALL METH_FASTCALL
+  #define __Pyx_PyCFunction_FastCall __Pyx_PyCFunctionFast
+  #define __Pyx_PyCFunction_FastCallWithKeywords __Pyx_PyCFunctionFastWithKeywords
+#else
+  #define __Pyx_METH_FASTCALL METH_VARARGS
+  #define __Pyx_PyCFunction_FastCall PyCFunction
+  #define __Pyx_PyCFunction_FastCallWithKeywords PyCFunctionWithKeywords
+#endif
+#if CYTHON_VECTORCALL
+  #define __pyx_vectorcallfunc vectorcallfunc
+  #define __Pyx_PY_VECTORCALL_ARGUMENTS_OFFSET  PY_VECTORCALL_ARGUMENTS_OFFSET
+  #define __Pyx_PyVectorcall_NARGS(n)  PyVectorcall_NARGS((size_t)(n))
+#elif CYTHON_BACKPORT_VECTORCALL
+  typedef PyObject *(*__pyx_vectorcallfunc)(PyObject *callable, PyObject *const *args,
+                                            size_t nargsf, PyObject *kwnames);
+  #define __Pyx_PY_VECTORCALL_ARGUMENTS_OFFSET  ((size_t)1 << (8 * sizeof(size_t) - 1))
+  #define __Pyx_PyVectorcall_NARGS(n)  ((Py_ssize_t)(((size_t)(n)) & ~__Pyx_PY_VECTORCALL_ARGUMENTS_OFFSET))
+#else
+  #define __Pyx_PY_VECTORCALL_ARGUMENTS_OFFSET  0
+  #define __Pyx_PyVectorcall_NARGS(n)  ((Py_ssize_t)(n))
+#endif
+#if PY_VERSION_HEX < 0x030900B1
+  #define __Pyx_PyType_FromModuleAndSpec(m, s, b)  ((void)m, PyType_FromSpecWithBases(s, b))
+  typedef PyObject *(*__Pyx_PyCMethod)(PyObject *, PyTypeObject *, PyObject *const *, size_t, PyObject *);
 #else
-#define __Pyx_PyFastCFunction_Check(func) 0
+  #define __Pyx_PyType_FromModuleAndSpec(m, s, b)  PyType_FromModuleAndSpec(m, s, b)
+  #define __Pyx_PyCMethod  PyCMethod
+#endif
+#ifndef METH_METHOD
+  #define METH_METHOD 0x200
 #endif
 #if CYTHON_COMPILING_IN_PYPY && !defined(PyObject_Malloc)
   #define PyObject_Malloc(s)   PyMem_Malloc(s)
   #define PyObject_Free(p)     PyMem_Free(p)
   #define PyObject_Realloc(p)  PyMem_Realloc(p)
 #endif
-#if CYTHON_COMPILING_IN_CPYTHON && PY_VERSION_HEX < 0x030400A1
-  #define PyMem_RawMalloc(n)           PyMem_Malloc(n)
-  #define PyMem_RawRealloc(p, n)       PyMem_Realloc(p, n)
-  #define PyMem_RawFree(p)             PyMem_Free(p)
-#endif
-#if CYTHON_COMPILING_IN_PYSTON
-  #define __Pyx_PyCode_HasFreeVars(co)  PyCode_HasFreeVars(co)
-  #define __Pyx_PyFrame_SetLineNumber(frame, lineno) PyFrame_SetLineNumber(frame, lineno)
+#if CYTHON_COMPILING_IN_LIMITED_API
+  #define __Pyx_PyCode_HasFreeVars(co)  (PyCode_GetNumFree(co) > 0)
+  #define __Pyx_PyFrame_SetLineNumber(frame, lineno)
 #else
   #define __Pyx_PyCode_HasFreeVars(co)  (PyCode_GetNumFree(co) > 0)
   #define __Pyx_PyFrame_SetLineNumber(frame, lineno)  (frame)->f_lineno = (lineno)
 #endif
-#if !CYTHON_FAST_THREAD_STATE || PY_VERSION_HEX < 0x02070000
+#if CYTHON_COMPILING_IN_LIMITED_API
+  #define __Pyx_PyThreadState_Current PyThreadState_Get()
+#elif !CYTHON_FAST_THREAD_STATE
   #define __Pyx_PyThreadState_Current PyThreadState_GET()
 #elif PY_VERSION_HEX >= 0x03060000
   #define __Pyx_PyThreadState_Current _PyThreadState_UncheckedGet()
 #elif PY_VERSION_HEX >= 0x03000000
   #define __Pyx_PyThreadState_Current PyThreadState_GET()
 #else
   #define __Pyx_PyThreadState_Current _PyThreadState_Current
 #endif
+#if CYTHON_COMPILING_IN_LIMITED_API
+static CYTHON_INLINE void *__Pyx_PyModule_GetState(PyObject *op)
+{
+    void *result;
+    result = PyModule_GetState(op);
+    if (!result)
+        Py_FatalError("Couldn't find the module state");
+    return result;
+}
+#endif
+#define __Pyx_PyObject_GetSlot(obj, name, func_ctype)  __Pyx_PyType_GetSlot(Py_TYPE(obj), name, func_ctype)
+#if CYTHON_COMPILING_IN_LIMITED_API
+  #define __Pyx_PyType_GetSlot(type, name, func_ctype)  ((func_ctype) PyType_GetSlot((type), Py_##name))
+#else
+  #define __Pyx_PyType_GetSlot(type, name, func_ctype)  ((type)->name)
+#endif
 #if PY_VERSION_HEX < 0x030700A2 && !defined(PyThread_tss_create) && !defined(Py_tss_NEEDS_INIT)
 #include "pythread.h"
 #define Py_tss_NEEDS_INIT 0
 typedef int Py_tss_t;
 static CYTHON_INLINE int PyThread_tss_create(Py_tss_t *key) {
   *key = PyThread_create_key();
   return 0;
@@ -552,46 +788,120 @@
 static CYTHON_INLINE int PyThread_tss_set(Py_tss_t *key, void *value) {
   return PyThread_set_key_value(*key, value);
 }
 static CYTHON_INLINE void * PyThread_tss_get(Py_tss_t *key) {
   return PyThread_get_key_value(*key);
 }
 #endif
+#if PY_MAJOR_VERSION < 3
+    #if CYTHON_COMPILING_IN_PYPY
+        #if PYPY_VERSION_NUM < 0x07030600
+            #if defined(__cplusplus) && __cplusplus >= 201402L
+                [[deprecated("`with nogil:` inside a nogil function will not release the GIL in PyPy2 < 7.3.6")]]
+            #elif defined(__GNUC__) || defined(__clang__)
+                __attribute__ ((__deprecated__("`with nogil:` inside a nogil function will not release the GIL in PyPy2 < 7.3.6")))
+            #elif defined(_MSC_VER)
+                __declspec(deprecated("`with nogil:` inside a nogil function will not release the GIL in PyPy2 < 7.3.6"))
+            #endif
+            static CYTHON_INLINE int PyGILState_Check(void) {
+                return 0;
+            }
+        #else  // PYPY_VERSION_NUM < 0x07030600
+        #endif  // PYPY_VERSION_NUM < 0x07030600
+    #else
+        static CYTHON_INLINE int PyGILState_Check(void) {
+            PyThreadState * tstate = _PyThreadState_Current;
+            return tstate && (tstate == PyGILState_GetThisThreadState());
+        }
+    #endif
+#endif
 #if CYTHON_COMPILING_IN_CPYTHON || defined(_PyDict_NewPresized)
 #define __Pyx_PyDict_NewPresized(n)  ((n <= 8) ? PyDict_New() : _PyDict_NewPresized(n))
 #else
 #define __Pyx_PyDict_NewPresized(n)  PyDict_New()
 #endif
 #if PY_MAJOR_VERSION >= 3 || CYTHON_FUTURE_DIVISION
   #define __Pyx_PyNumber_Divide(x,y)         PyNumber_TrueDivide(x,y)
   #define __Pyx_PyNumber_InPlaceDivide(x,y)  PyNumber_InPlaceTrueDivide(x,y)
 #else
   #define __Pyx_PyNumber_Divide(x,y)         PyNumber_Divide(x,y)
   #define __Pyx_PyNumber_InPlaceDivide(x,y)  PyNumber_InPlaceDivide(x,y)
 #endif
-#if CYTHON_COMPILING_IN_CPYTHON && PY_VERSION_HEX >= 0x030500A1 && CYTHON_USE_UNICODE_INTERNALS
-#define __Pyx_PyDict_GetItemStr(dict, name)  _PyDict_GetItem_KnownHash(dict, name, ((PyASCIIObject *) name)->hash)
+#if CYTHON_COMPILING_IN_CPYTHON && PY_VERSION_HEX > 0x030600B4 && CYTHON_USE_UNICODE_INTERNALS
+#define __Pyx_PyDict_GetItemStrWithError(dict, name)  _PyDict_GetItem_KnownHash(dict, name, ((PyASCIIObject *) name)->hash)
+static CYTHON_INLINE PyObject * __Pyx_PyDict_GetItemStr(PyObject *dict, PyObject *name) {
+    PyObject *res = __Pyx_PyDict_GetItemStrWithError(dict, name);
+    if (res == NULL) PyErr_Clear();
+    return res;
+}
+#elif PY_MAJOR_VERSION >= 3 && (!CYTHON_COMPILING_IN_PYPY || PYPY_VERSION_NUM >= 0x07020000)
+#define __Pyx_PyDict_GetItemStrWithError  PyDict_GetItemWithError
+#define __Pyx_PyDict_GetItemStr           PyDict_GetItem
+#else
+static CYTHON_INLINE PyObject * __Pyx_PyDict_GetItemStrWithError(PyObject *dict, PyObject *name) {
+#if CYTHON_COMPILING_IN_PYPY
+    return PyDict_GetItem(dict, name);
+#else
+    PyDictEntry *ep;
+    PyDictObject *mp = (PyDictObject*) dict;
+    long hash = ((PyStringObject *) name)->ob_shash;
+    assert(hash != -1);
+    ep = (mp->ma_lookup)(mp, name, hash);
+    if (ep == NULL) {
+        return NULL;
+    }
+    return ep->me_value;
+#endif
+}
+#define __Pyx_PyDict_GetItemStr           PyDict_GetItem
+#endif
+#if CYTHON_USE_TYPE_SLOTS
+  #define __Pyx_PyType_GetFlags(tp)   (((PyTypeObject *)tp)->tp_flags)
+  #define __Pyx_PyType_HasFeature(type, feature)  ((__Pyx_PyType_GetFlags(type) & (feature)) != 0)
+  #define __Pyx_PyObject_GetIterNextFunc(obj)  (Py_TYPE(obj)->tp_iternext)
 #else
-#define __Pyx_PyDict_GetItemStr(dict, name)  PyDict_GetItem(dict, name)
+  #define __Pyx_PyType_GetFlags(tp)   (PyType_GetFlags((PyTypeObject *)tp))
+  #define __Pyx_PyType_HasFeature(type, feature)  PyType_HasFeature(type, feature)
+  #define __Pyx_PyObject_GetIterNextFunc(obj)  PyIter_Next
 #endif
-#if PY_VERSION_HEX > 0x03030000 && defined(PyUnicode_KIND)
+#if CYTHON_USE_TYPE_SPECS && PY_VERSION_HEX >= 0x03080000
+#define __Pyx_PyHeapTypeObject_GC_Del(obj)  {\
+    PyTypeObject *type = Py_TYPE(obj);\
+    assert(__Pyx_PyType_HasFeature(type, Py_TPFLAGS_HEAPTYPE));\
+    PyObject_GC_Del(obj);\
+    Py_DECREF(type);\
+}
+#else
+#define __Pyx_PyHeapTypeObject_GC_Del(obj)  PyObject_GC_Del(obj)
+#endif
+#if CYTHON_COMPILING_IN_LIMITED_API
+  #define CYTHON_PEP393_ENABLED 1
+  #define __Pyx_PyUnicode_READY(op)       (0)
+  #define __Pyx_PyUnicode_GET_LENGTH(u)   PyUnicode_GetLength(u)
+  #define __Pyx_PyUnicode_READ_CHAR(u, i) PyUnicode_ReadChar(u, i)
+  #define __Pyx_PyUnicode_MAX_CHAR_VALUE(u)   ((void)u, 1114111U)
+  #define __Pyx_PyUnicode_KIND(u)         ((void)u, (0))
+  #define __Pyx_PyUnicode_DATA(u)         ((void*)u)
+  #define __Pyx_PyUnicode_READ(k, d, i)   ((void)k, PyUnicode_ReadChar((PyObject*)(d), i))
+  #define __Pyx_PyUnicode_IS_TRUE(u)      (0 != PyUnicode_GetLength(u))
+#elif PY_VERSION_HEX > 0x03030000 && defined(PyUnicode_KIND)
   #define CYTHON_PEP393_ENABLED 1
   #if PY_VERSION_HEX >= 0x030C0000
     #define __Pyx_PyUnicode_READY(op)       (0)
   #else
     #define __Pyx_PyUnicode_READY(op)       (likely(PyUnicode_IS_READY(op)) ?\
                                                 0 : _PyUnicode_Ready((PyObject *)(op)))
   #endif
   #define __Pyx_PyUnicode_GET_LENGTH(u)   PyUnicode_GET_LENGTH(u)
   #define __Pyx_PyUnicode_READ_CHAR(u, i) PyUnicode_READ_CHAR(u, i)
   #define __Pyx_PyUnicode_MAX_CHAR_VALUE(u)   PyUnicode_MAX_CHAR_VALUE(u)
-  #define __Pyx_PyUnicode_KIND(u)         PyUnicode_KIND(u)
+  #define __Pyx_PyUnicode_KIND(u)         ((int)PyUnicode_KIND(u))
   #define __Pyx_PyUnicode_DATA(u)         PyUnicode_DATA(u)
   #define __Pyx_PyUnicode_READ(k, d, i)   PyUnicode_READ(k, d, i)
-  #define __Pyx_PyUnicode_WRITE(k, d, i, ch)  PyUnicode_WRITE(k, d, i, ch)
+  #define __Pyx_PyUnicode_WRITE(k, d, i, ch)  PyUnicode_WRITE(k, d, i, (Py_UCS4) ch)
   #if PY_VERSION_HEX >= 0x030C0000
     #define __Pyx_PyUnicode_IS_TRUE(u)      (0 != PyUnicode_GET_LENGTH(u))
   #else
     #if CYTHON_COMPILING_IN_CPYTHON && PY_VERSION_HEX >= 0x03090000
     #define __Pyx_PyUnicode_IS_TRUE(u)      (0 != (likely(PyUnicode_IS_READY(u)) ? PyUnicode_GET_LENGTH(u) : ((PyCompactUnicodeObject *)(u))->wstr_length))
     #else
     #define __Pyx_PyUnicode_IS_TRUE(u)      (0 != (likely(PyUnicode_IS_READY(u)) ? PyUnicode_GET_LENGTH(u) : PyUnicode_GET_SIZE(u)))
@@ -601,37 +911,43 @@
   #define CYTHON_PEP393_ENABLED 0
   #define PyUnicode_1BYTE_KIND  1
   #define PyUnicode_2BYTE_KIND  2
   #define PyUnicode_4BYTE_KIND  4
   #define __Pyx_PyUnicode_READY(op)       (0)
   #define __Pyx_PyUnicode_GET_LENGTH(u)   PyUnicode_GET_SIZE(u)
   #define __Pyx_PyUnicode_READ_CHAR(u, i) ((Py_UCS4)(PyUnicode_AS_UNICODE(u)[i]))
-  #define __Pyx_PyUnicode_MAX_CHAR_VALUE(u)   ((sizeof(Py_UNICODE) == 2) ? 65535 : 1114111)
-  #define __Pyx_PyUnicode_KIND(u)         (sizeof(Py_UNICODE))
+  #define __Pyx_PyUnicode_MAX_CHAR_VALUE(u)   ((sizeof(Py_UNICODE) == 2) ? 65535U : 1114111U)
+  #define __Pyx_PyUnicode_KIND(u)         ((int)sizeof(Py_UNICODE))
   #define __Pyx_PyUnicode_DATA(u)         ((void*)PyUnicode_AS_UNICODE(u))
   #define __Pyx_PyUnicode_READ(k, d, i)   ((void)(k), (Py_UCS4)(((Py_UNICODE*)d)[i]))
-  #define __Pyx_PyUnicode_WRITE(k, d, i, ch)  (((void)(k)), ((Py_UNICODE*)d)[i] = ch)
+  #define __Pyx_PyUnicode_WRITE(k, d, i, ch)  (((void)(k)), ((Py_UNICODE*)d)[i] = (Py_UNICODE) ch)
   #define __Pyx_PyUnicode_IS_TRUE(u)      (0 != PyUnicode_GET_SIZE(u))
 #endif
 #if CYTHON_COMPILING_IN_PYPY
   #define __Pyx_PyUnicode_Concat(a, b)      PyNumber_Add(a, b)
   #define __Pyx_PyUnicode_ConcatSafe(a, b)  PyNumber_Add(a, b)
 #else
   #define __Pyx_PyUnicode_Concat(a, b)      PyUnicode_Concat(a, b)
   #define __Pyx_PyUnicode_ConcatSafe(a, b)  ((unlikely((a) == Py_None) || unlikely((b) == Py_None)) ?\
       PyNumber_Add(a, b) : __Pyx_PyUnicode_Concat(a, b))
 #endif
-#if CYTHON_COMPILING_IN_PYPY && !defined(PyUnicode_Contains)
-  #define PyUnicode_Contains(u, s)  PySequence_Contains(u, s)
-#endif
-#if CYTHON_COMPILING_IN_PYPY && !defined(PyByteArray_Check)
-  #define PyByteArray_Check(obj)  PyObject_TypeCheck(obj, &PyByteArray_Type)
-#endif
-#if CYTHON_COMPILING_IN_PYPY && !defined(PyObject_Format)
-  #define PyObject_Format(obj, fmt)  PyObject_CallMethod(obj, "__format__", "O", fmt)
+#if CYTHON_COMPILING_IN_PYPY
+  #if !defined(PyUnicode_DecodeUnicodeEscape)
+    #define PyUnicode_DecodeUnicodeEscape(s, size, errors)  PyUnicode_Decode(s, size, "unicode_escape", errors)
+  #endif
+  #if !defined(PyUnicode_Contains) || (PY_MAJOR_VERSION == 2 && PYPY_VERSION_NUM < 0x07030500)
+    #undef PyUnicode_Contains
+    #define PyUnicode_Contains(u, s)  PySequence_Contains(u, s)
+  #endif
+  #if !defined(PyByteArray_Check)
+    #define PyByteArray_Check(obj)  PyObject_TypeCheck(obj, &PyByteArray_Type)
+  #endif
+  #if !defined(PyObject_Format)
+    #define PyObject_Format(obj, fmt)  PyObject_CallMethod(obj, "__format__", "O", fmt)
+  #endif
 #endif
 #define __Pyx_PyString_FormatSafe(a, b)   ((unlikely((a) == Py_None || (PyString_Check(b) && !PyString_CheckExact(b)))) ? PyNumber_Remainder(a, b) : __Pyx_PyString_Format(a, b))
 #define __Pyx_PyUnicode_FormatSafe(a, b)  ((unlikely((a) == Py_None || (PyUnicode_Check(b) && !PyUnicode_CheckExact(b)))) ? PyNumber_Remainder(a, b) : PyUnicode_Format(a, b))
 #if PY_MAJOR_VERSION >= 3
   #define __Pyx_PyString_Format(a, b)  PyUnicode_Format(a, b)
 #else
   #define __Pyx_PyString_Format(a, b)  PyString_Format(a, b)
@@ -652,16 +968,22 @@
 #if PY_MAJOR_VERSION >= 3
   #define __Pyx_PyBaseString_Check(obj) PyUnicode_Check(obj)
   #define __Pyx_PyBaseString_CheckExact(obj) PyUnicode_CheckExact(obj)
 #else
   #define __Pyx_PyBaseString_Check(obj) (PyString_Check(obj) || PyUnicode_Check(obj))
   #define __Pyx_PyBaseString_CheckExact(obj) (PyString_CheckExact(obj) || PyUnicode_CheckExact(obj))
 #endif
+#if CYTHON_COMPILING_IN_CPYTHON
+  #define __Pyx_PySequence_ListKeepNew(obj)\
+    (likely(PyList_CheckExact(obj) && Py_REFCNT(obj) == 1) ? __Pyx_NewRef(obj) : PySequence_List(obj))
+#else
+  #define __Pyx_PySequence_ListKeepNew(obj)  PySequence_List(obj)
+#endif
 #ifndef PySet_CheckExact
-  #define PySet_CheckExact(obj)        (Py_TYPE(obj) == &PySet_Type)
+  #define PySet_CheckExact(obj)        __Pyx_IS_TYPE(obj, &PySet_Type)
 #endif
 #if PY_VERSION_HEX >= 0x030900A4
   #define __Pyx_SET_REFCNT(obj, refcnt) Py_SET_REFCNT(obj, refcnt)
   #define __Pyx_SET_SIZE(obj, size) Py_SET_SIZE(obj, size)
 #else
   #define __Pyx_SET_REFCNT(obj, refcnt) Py_REFCNT(obj) = (refcnt)
   #define __Pyx_SET_SIZE(obj, size) Py_SIZE(obj) = (size)
@@ -672,25 +994,30 @@
   #define __Pyx_PySequence_SIZE(seq)  PySequence_Size(seq)
 #endif
 #if PY_MAJOR_VERSION >= 3
   #define PyIntObject                  PyLongObject
   #define PyInt_Type                   PyLong_Type
   #define PyInt_Check(op)              PyLong_Check(op)
   #define PyInt_CheckExact(op)         PyLong_CheckExact(op)
+  #define __Pyx_Py3Int_Check(op)       PyLong_Check(op)
+  #define __Pyx_Py3Int_CheckExact(op)  PyLong_CheckExact(op)
   #define PyInt_FromString             PyLong_FromString
   #define PyInt_FromUnicode            PyLong_FromUnicode
   #define PyInt_FromLong               PyLong_FromLong
   #define PyInt_FromSize_t             PyLong_FromSize_t
   #define PyInt_FromSsize_t            PyLong_FromSsize_t
   #define PyInt_AsLong                 PyLong_AsLong
   #define PyInt_AS_LONG                PyLong_AS_LONG
   #define PyInt_AsSsize_t              PyLong_AsSsize_t
   #define PyInt_AsUnsignedLongMask     PyLong_AsUnsignedLongMask
   #define PyInt_AsUnsignedLongLongMask PyLong_AsUnsignedLongLongMask
   #define PyNumber_Int                 PyNumber_Long
+#else
+  #define __Pyx_Py3Int_Check(op)       (PyLong_Check(op) || PyInt_Check(op))
+  #define __Pyx_Py3Int_CheckExact(op)  (PyLong_CheckExact(op) || PyInt_CheckExact(op))
 #endif
 #if PY_MAJOR_VERSION >= 3
   #define PyBoolObject                 PyLongObject
 #endif
 #if PY_MAJOR_VERSION >= 3 && CYTHON_COMPILING_IN_PYPY
   #ifndef PyUnicode_InternFromString
     #define PyUnicode_InternFromString(s) PyUnicode_FromString(s)
@@ -700,19 +1027,14 @@
   typedef long Py_hash_t;
   #define __Pyx_PyInt_FromHash_t PyInt_FromLong
   #define __Pyx_PyInt_AsHash_t   __Pyx_PyIndex_AsHash_t
 #else
   #define __Pyx_PyInt_FromHash_t PyInt_FromSsize_t
   #define __Pyx_PyInt_AsHash_t   __Pyx_PyIndex_AsSsize_t
 #endif
-#if PY_MAJOR_VERSION >= 3
-  #define __Pyx_PyMethod_New(func, self, klass) ((self) ? ((void)(klass), PyMethod_New(func, self)) : __Pyx_NewRef(func))
-#else
-  #define __Pyx_PyMethod_New(func, self, klass) PyMethod_New(func, self, klass)
-#endif
 #if CYTHON_USE_ASYNC_SLOTS
   #if PY_VERSION_HEX >= 0x030500B1
     #define __Pyx_PyAsyncMethodsStruct PyAsyncMethods
     #define __Pyx_PyType_AsAsync(obj) (Py_TYPE(obj)->tp_as_async)
   #else
     #define __Pyx_PyType_AsAsync(obj) ((__Pyx_PyAsyncMethodsStruct*) (Py_TYPE(obj)->tp_reserved))
   #endif
@@ -749,15 +1071,24 @@
 #endif
 
 #define __PYX_MARK_ERR_POS(f_index, lineno) \
     { __pyx_filename = __pyx_f[f_index]; (void)__pyx_filename; __pyx_lineno = lineno; (void)__pyx_lineno; __pyx_clineno = __LINE__; (void)__pyx_clineno; }
 #define __PYX_ERR(f_index, lineno, Ln_error) \
     { __PYX_MARK_ERR_POS(f_index, lineno) goto Ln_error; }
 
-#ifndef __PYX_EXTERN_C
+#ifdef CYTHON_EXTERN_C
+    #undef __PYX_EXTERN_C
+    #define __PYX_EXTERN_C CYTHON_EXTERN_C
+#elif defined(__PYX_EXTERN_C)
+    #ifdef _MSC_VER
+    #pragma message ("Please do not define the '__PYX_EXTERN_C' macro externally. Use 'CYTHON_EXTERN_C' instead.")
+    #else
+    #warning Please do not define the '__PYX_EXTERN_C' macro externally. Use 'CYTHON_EXTERN_C' instead.
+    #endif
+#else
   #ifdef __cplusplus
     #define __PYX_EXTERN_C extern "C"
   #else
     #define __PYX_EXTERN_C extern
   #endif
 #endif
 
@@ -829,29 +1160,40 @@
 #endif
 #define __Pyx_PyBytes_AsWritableString(s)     ((char*) PyBytes_AS_STRING(s))
 #define __Pyx_PyBytes_AsWritableSString(s)    ((signed char*) PyBytes_AS_STRING(s))
 #define __Pyx_PyBytes_AsWritableUString(s)    ((unsigned char*) PyBytes_AS_STRING(s))
 #define __Pyx_PyBytes_AsString(s)     ((const char*) PyBytes_AS_STRING(s))
 #define __Pyx_PyBytes_AsSString(s)    ((const signed char*) PyBytes_AS_STRING(s))
 #define __Pyx_PyBytes_AsUString(s)    ((const unsigned char*) PyBytes_AS_STRING(s))
-#define __Pyx_PyObject_AsWritableString(s)    ((char*) __Pyx_PyObject_AsString(s))
-#define __Pyx_PyObject_AsWritableSString(s)    ((signed char*) __Pyx_PyObject_AsString(s))
-#define __Pyx_PyObject_AsWritableUString(s)    ((unsigned char*) __Pyx_PyObject_AsString(s))
+#define __Pyx_PyObject_AsWritableString(s)    ((char*)(__pyx_uintptr_t) __Pyx_PyObject_AsString(s))
+#define __Pyx_PyObject_AsWritableSString(s)    ((signed char*)(__pyx_uintptr_t) __Pyx_PyObject_AsString(s))
+#define __Pyx_PyObject_AsWritableUString(s)    ((unsigned char*)(__pyx_uintptr_t) __Pyx_PyObject_AsString(s))
 #define __Pyx_PyObject_AsSString(s)    ((const signed char*) __Pyx_PyObject_AsString(s))
 #define __Pyx_PyObject_AsUString(s)    ((const unsigned char*) __Pyx_PyObject_AsString(s))
 #define __Pyx_PyObject_FromCString(s)  __Pyx_PyObject_FromString((const char*)s)
 #define __Pyx_PyBytes_FromCString(s)   __Pyx_PyBytes_FromString((const char*)s)
 #define __Pyx_PyByteArray_FromCString(s)   __Pyx_PyByteArray_FromString((const char*)s)
 #define __Pyx_PyStr_FromCString(s)     __Pyx_PyStr_FromString((const char*)s)
 #define __Pyx_PyUnicode_FromCString(s) __Pyx_PyUnicode_FromString((const char*)s)
-static CYTHON_INLINE size_t __Pyx_Py_UNICODE_strlen(const Py_UNICODE *u) {
+#if CYTHON_COMPILING_IN_LIMITED_API
+static CYTHON_INLINE size_t __Pyx_Py_UNICODE_strlen(const wchar_t *u)
+{
+    const wchar_t *u_end = u;
+    while (*u_end++) ;
+    return (size_t)(u_end - u - 1);
+}
+#else
+static CYTHON_INLINE size_t __Pyx_Py_UNICODE_strlen(const Py_UNICODE *u)
+{
     const Py_UNICODE *u_end = u;
     while (*u_end++) ;
     return (size_t)(u_end - u - 1);
 }
+#endif
+#define __Pyx_PyUnicode_FromOrdinal(o)       PyUnicode_FromOrdinal((int)o)
 #define __Pyx_PyUnicode_FromUnicode(u)       PyUnicode_FromUnicode(u, __Pyx_Py_UNICODE_strlen(u))
 #define __Pyx_PyUnicode_FromUnicodeAndLength PyUnicode_FromUnicode
 #define __Pyx_PyUnicode_AsUnicode            PyUnicode_AsUnicode
 #define __Pyx_NewRef(obj) (Py_INCREF(obj), obj)
 #define __Pyx_Owned_Py_None(b) __Pyx_NewRef(Py_None)
 static CYTHON_INLINE PyObject * __Pyx_PyBool_FromLong(long b);
 static CYTHON_INLINE int __Pyx_PyObject_IsTrue(PyObject*);
@@ -869,15 +1211,60 @@
 #endif
 #define __pyx_PyFloat_AsFloat(x) ((float) __pyx_PyFloat_AsDouble(x))
 #if PY_MAJOR_VERSION >= 3
 #define __Pyx_PyNumber_Int(x) (PyLong_CheckExact(x) ? __Pyx_NewRef(x) : PyNumber_Long(x))
 #else
 #define __Pyx_PyNumber_Int(x) (PyInt_CheckExact(x) ? __Pyx_NewRef(x) : PyNumber_Int(x))
 #endif
-#define __Pyx_PyNumber_Float(x) (PyFloat_CheckExact(x) ? __Pyx_NewRef(x) : PyNumber_Float(x))
+#if CYTHON_USE_PYLONG_INTERNALS
+  #if PY_VERSION_HEX >= 0x030C00A7
+  #ifndef _PyLong_SIGN_MASK
+    #define _PyLong_SIGN_MASK 3
+  #endif
+  #ifndef _PyLong_NON_SIZE_BITS
+    #define _PyLong_NON_SIZE_BITS 3
+  #endif
+  #define __Pyx_PyLong_Sign(x)  (((PyLongObject*)x)->long_value.lv_tag & _PyLong_SIGN_MASK)
+  #define __Pyx_PyLong_IsNeg(x)  ((__Pyx_PyLong_Sign(x) & 2) != 0)
+  #define __Pyx_PyLong_IsNonNeg(x)  (!__Pyx_PyLong_IsNeg(x))
+  #define __Pyx_PyLong_IsZero(x)  (__Pyx_PyLong_Sign(x) & 1)
+  #define __Pyx_PyLong_IsPos(x)  (__Pyx_PyLong_Sign(x) == 0)
+  #define __Pyx_PyLong_CompactValueUnsigned(x)  (__Pyx_PyLong_Digits(x)[0])
+  #define __Pyx_PyLong_DigitCount(x)  ((Py_ssize_t) (((PyLongObject*)x)->long_value.lv_tag >> _PyLong_NON_SIZE_BITS))
+  #define __Pyx_PyLong_SignedDigitCount(x)\
+        ((1 - (Py_ssize_t) __Pyx_PyLong_Sign(x)) * __Pyx_PyLong_DigitCount(x))
+  #if defined(PyUnstable_Long_IsCompact) && defined(PyUnstable_Long_CompactValue)
+    #define __Pyx_PyLong_IsCompact(x)     PyUnstable_Long_IsCompact((PyLongObject*) x)
+    #define __Pyx_PyLong_CompactValue(x)  PyUnstable_Long_CompactValue((PyLongObject*) x)
+  #else
+    #define __Pyx_PyLong_IsCompact(x)     (((PyLongObject*)x)->long_value.lv_tag < (2 << _PyLong_NON_SIZE_BITS))
+    #define __Pyx_PyLong_CompactValue(x)  ((1 - (Py_ssize_t) __Pyx_PyLong_Sign(x)) * (Py_ssize_t) __Pyx_PyLong_Digits(x)[0])
+  #endif
+  typedef Py_ssize_t  __Pyx_compact_pylong;
+  typedef size_t  __Pyx_compact_upylong;
+  #else  // Py < 3.12
+  #define __Pyx_PyLong_IsNeg(x)  (Py_SIZE(x) < 0)
+  #define __Pyx_PyLong_IsNonNeg(x)  (Py_SIZE(x) >= 0)
+  #define __Pyx_PyLong_IsZero(x)  (Py_SIZE(x) == 0)
+  #define __Pyx_PyLong_IsPos(x)  (Py_SIZE(x) > 0)
+  #define __Pyx_PyLong_CompactValueUnsigned(x)  ((Py_SIZE(x) == 0) ? 0 : __Pyx_PyLong_Digits(x)[0])
+  #define __Pyx_PyLong_DigitCount(x)  __Pyx_sst_abs(Py_SIZE(x))
+  #define __Pyx_PyLong_SignedDigitCount(x)  Py_SIZE(x)
+  #define __Pyx_PyLong_IsCompact(x)  (Py_SIZE(x) == 0 || Py_SIZE(x) == 1 || Py_SIZE(x) == -1)
+  #define __Pyx_PyLong_CompactValue(x)\
+        ((Py_SIZE(x) == 0) ? (sdigit) 0 : ((Py_SIZE(x) < 0) ? -(sdigit)__Pyx_PyLong_Digits(x)[0] : (sdigit)__Pyx_PyLong_Digits(x)[0]))
+  typedef sdigit  __Pyx_compact_pylong;
+  typedef digit  __Pyx_compact_upylong;
+  #endif
+  #if PY_VERSION_HEX >= 0x030C00A5
+  #define __Pyx_PyLong_Digits(x)  (((PyLongObject*)x)->long_value.ob_digit)
+  #else
+  #define __Pyx_PyLong_Digits(x)  (((PyLongObject*)x)->ob_digit)
+  #endif
+#endif
 #if PY_MAJOR_VERSION < 3 && __PYX_DEFAULT_STRING_ENCODING_IS_ASCII
 static int __Pyx_sys_getdefaultencoding_not_ascii;
 static int __Pyx_init_sys_getdefaultencoding_params(void) {
     PyObject* sys;
     PyObject* default_encoding = NULL;
     PyObject* ascii_chars_u = NULL;
     PyObject* ascii_chars_b = NULL;
@@ -891,15 +1278,15 @@
     if (!default_encoding_c) goto bad;
     if (strcmp(default_encoding_c, "ascii") == 0) {
         __Pyx_sys_getdefaultencoding_not_ascii = 0;
     } else {
         char ascii_chars[128];
         int c;
         for (c = 0; c < 128; c++) {
-            ascii_chars[c] = c;
+            ascii_chars[c] = (char) c;
         }
         __Pyx_sys_getdefaultencoding_not_ascii = 1;
         ascii_chars_u = PyUnicode_DecodeASCII(ascii_chars, 128, NULL);
         if (!ascii_chars_u) goto bad;
         ascii_chars_b = PyUnicode_AsEncodedString(ascii_chars_u, default_encoding_c, NULL);
         if (!ascii_chars_b || !PyBytes_Check(ascii_chars_b) || memcmp(ascii_chars, PyBytes_AS_STRING(ascii_chars_b), 128) != 0) {
             PyErr_Format(
@@ -956,43 +1343,44 @@
   #define unlikely(x) __builtin_expect(!!(x), 0)
 #else /* !__GNUC__ or GCC < 2.95 */
   #define likely(x)   (x)
   #define unlikely(x) (x)
 #endif /* __GNUC__ */
 static CYTHON_INLINE void __Pyx_pretend_to_initialize(void* ptr) { (void)ptr; }
 
+#if !CYTHON_USE_MODULE_STATE
 static PyObject *__pyx_m = NULL;
-static PyObject *__pyx_d;
-static PyObject *__pyx_b;
-static PyObject *__pyx_cython_runtime = NULL;
-static PyObject *__pyx_empty_tuple;
-static PyObject *__pyx_empty_bytes;
-static PyObject *__pyx_empty_unicode;
+#endif
 static int __pyx_lineno;
 static int __pyx_clineno = 0;
-static const char * __pyx_cfilenm= __FILE__;
+static const char * __pyx_cfilenm = __FILE__;
 static const char *__pyx_filename;
 
+/* #### Code section: filename_table ### */
 
 static const char *__pyx_f[] = {
-  "pybitset\\backends\\cython\\_bitset.pyx",
-  "stringsource",
+  "pybitset\\\\backends\\\\cython\\\\_bitset.pyx",
+  "<stringsource>",
 };
+/* #### Code section: utility_code_proto_before_types ### */
 /* ForceInitThreads.proto */
 #ifndef __PYX_FORCE_INIT_THREADS
   #define __PYX_FORCE_INIT_THREADS 0
 #endif
 
 /* NoFastGil.proto */
 #define __Pyx_PyGILState_Ensure PyGILState_Ensure
 #define __Pyx_PyGILState_Release PyGILState_Release
 #define __Pyx_FastGIL_Remember()
 #define __Pyx_FastGIL_Forget()
 #define __Pyx_FastGilFuncInit()
 
+/* #### Code section: numeric_typedefs ### */
+/* #### Code section: complex_type_declarations ### */
+/* #### Code section: type_declarations ### */
 
 /*--- Type declarations ---*/
 struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet;
 struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSetIter;
 
 /* "pybitset/backends/cython/_bitset.pyx":25
  * @cython.final
@@ -1092,233 +1480,451 @@
 static CYTHON_INLINE int __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_contains_all(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *, int __pyx_skip_dispatch);
 static CYTHON_INLINE PyObject *__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_inplace_difference(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *, int __pyx_skip_dispatch);
 static CYTHON_INLINE size_t __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_difference_count(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *, int __pyx_skip_dispatch);
 static CYTHON_INLINE int __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_inplace_symmetric_difference(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *, int __pyx_skip_dispatch);
 static CYTHON_INLINE size_t __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_symmetric_difference_count(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *, int __pyx_skip_dispatch);
 static CYTHON_INLINE int __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_for_each(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *, PyObject *, int __pyx_skip_dispatch);
 static CYTHON_INLINE PyObject *__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_print(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *, int __pyx_skip_dispatch);
+/* #### Code section: utility_code_proto ### */
 
 /* --- Runtime support code (head) --- */
 /* Refnanny.proto */
 #ifndef CYTHON_REFNANNY
   #define CYTHON_REFNANNY 0
 #endif
 #if CYTHON_REFNANNY
   typedef struct {
-    void (*INCREF)(void*, PyObject*, int);
-    void (*DECREF)(void*, PyObject*, int);
-    void (*GOTREF)(void*, PyObject*, int);
-    void (*GIVEREF)(void*, PyObject*, int);
-    void* (*SetupContext)(const char*, int, const char*);
+    void (*INCREF)(void*, PyObject*, Py_ssize_t);
+    void (*DECREF)(void*, PyObject*, Py_ssize_t);
+    void (*GOTREF)(void*, PyObject*, Py_ssize_t);
+    void (*GIVEREF)(void*, PyObject*, Py_ssize_t);
+    void* (*SetupContext)(const char*, Py_ssize_t, const char*);
     void (*FinishContext)(void**);
   } __Pyx_RefNannyAPIStruct;
   static __Pyx_RefNannyAPIStruct *__Pyx_RefNanny = NULL;
   static __Pyx_RefNannyAPIStruct *__Pyx_RefNannyImportAPI(const char *modname);
   #define __Pyx_RefNannyDeclarations void *__pyx_refnanny = NULL;
 #ifdef WITH_THREAD
   #define __Pyx_RefNannySetupContext(name, acquire_gil)\
           if (acquire_gil) {\
               PyGILState_STATE __pyx_gilstate_save = PyGILState_Ensure();\
-              __pyx_refnanny = __Pyx_RefNanny->SetupContext((name), __LINE__, __FILE__);\
+              __pyx_refnanny = __Pyx_RefNanny->SetupContext((name), (__LINE__), (__FILE__));\
               PyGILState_Release(__pyx_gilstate_save);\
           } else {\
-              __pyx_refnanny = __Pyx_RefNanny->SetupContext((name), __LINE__, __FILE__);\
+              __pyx_refnanny = __Pyx_RefNanny->SetupContext((name), (__LINE__), (__FILE__));\
+          }
+  #define __Pyx_RefNannyFinishContextNogil() {\
+              PyGILState_STATE __pyx_gilstate_save = PyGILState_Ensure();\
+              __Pyx_RefNannyFinishContext();\
+              PyGILState_Release(__pyx_gilstate_save);\
           }
 #else
   #define __Pyx_RefNannySetupContext(name, acquire_gil)\
-          __pyx_refnanny = __Pyx_RefNanny->SetupContext((name), __LINE__, __FILE__)
+          __pyx_refnanny = __Pyx_RefNanny->SetupContext((name), (__LINE__), (__FILE__))
+  #define __Pyx_RefNannyFinishContextNogil() __Pyx_RefNannyFinishContext()
 #endif
+  #define __Pyx_RefNannyFinishContextNogil() {\
+              PyGILState_STATE __pyx_gilstate_save = PyGILState_Ensure();\
+              __Pyx_RefNannyFinishContext();\
+              PyGILState_Release(__pyx_gilstate_save);\
+          }
   #define __Pyx_RefNannyFinishContext()\
           __Pyx_RefNanny->FinishContext(&__pyx_refnanny)
-  #define __Pyx_INCREF(r)  __Pyx_RefNanny->INCREF(__pyx_refnanny, (PyObject *)(r), __LINE__)
-  #define __Pyx_DECREF(r)  __Pyx_RefNanny->DECREF(__pyx_refnanny, (PyObject *)(r), __LINE__)
-  #define __Pyx_GOTREF(r)  __Pyx_RefNanny->GOTREF(__pyx_refnanny, (PyObject *)(r), __LINE__)
-  #define __Pyx_GIVEREF(r) __Pyx_RefNanny->GIVEREF(__pyx_refnanny, (PyObject *)(r), __LINE__)
-  #define __Pyx_XINCREF(r)  do { if((r) != NULL) {__Pyx_INCREF(r); }} while(0)
-  #define __Pyx_XDECREF(r)  do { if((r) != NULL) {__Pyx_DECREF(r); }} while(0)
-  #define __Pyx_XGOTREF(r)  do { if((r) != NULL) {__Pyx_GOTREF(r); }} while(0)
-  #define __Pyx_XGIVEREF(r) do { if((r) != NULL) {__Pyx_GIVEREF(r);}} while(0)
+  #define __Pyx_INCREF(r)  __Pyx_RefNanny->INCREF(__pyx_refnanny, (PyObject *)(r), (__LINE__))
+  #define __Pyx_DECREF(r)  __Pyx_RefNanny->DECREF(__pyx_refnanny, (PyObject *)(r), (__LINE__))
+  #define __Pyx_GOTREF(r)  __Pyx_RefNanny->GOTREF(__pyx_refnanny, (PyObject *)(r), (__LINE__))
+  #define __Pyx_GIVEREF(r) __Pyx_RefNanny->GIVEREF(__pyx_refnanny, (PyObject *)(r), (__LINE__))
+  #define __Pyx_XINCREF(r)  do { if((r) == NULL); else {__Pyx_INCREF(r); }} while(0)
+  #define __Pyx_XDECREF(r)  do { if((r) == NULL); else {__Pyx_DECREF(r); }} while(0)
+  #define __Pyx_XGOTREF(r)  do { if((r) == NULL); else {__Pyx_GOTREF(r); }} while(0)
+  #define __Pyx_XGIVEREF(r) do { if((r) == NULL); else {__Pyx_GIVEREF(r);}} while(0)
 #else
   #define __Pyx_RefNannyDeclarations
   #define __Pyx_RefNannySetupContext(name, acquire_gil)
+  #define __Pyx_RefNannyFinishContextNogil()
   #define __Pyx_RefNannyFinishContext()
   #define __Pyx_INCREF(r) Py_INCREF(r)
   #define __Pyx_DECREF(r) Py_DECREF(r)
   #define __Pyx_GOTREF(r)
   #define __Pyx_GIVEREF(r)
   #define __Pyx_XINCREF(r) Py_XINCREF(r)
   #define __Pyx_XDECREF(r) Py_XDECREF(r)
   #define __Pyx_XGOTREF(r)
   #define __Pyx_XGIVEREF(r)
 #endif
+#define __Pyx_Py_XDECREF_SET(r, v) do {\
+        PyObject *tmp = (PyObject *) r;\
+        r = v; Py_XDECREF(tmp);\
+    } while (0)
 #define __Pyx_XDECREF_SET(r, v) do {\
         PyObject *tmp = (PyObject *) r;\
         r = v; __Pyx_XDECREF(tmp);\
     } while (0)
 #define __Pyx_DECREF_SET(r, v) do {\
         PyObject *tmp = (PyObject *) r;\
         r = v; __Pyx_DECREF(tmp);\
     } while (0)
 #define __Pyx_CLEAR(r)    do { PyObject* tmp = ((PyObject*)(r)); r = NULL; __Pyx_DECREF(tmp);} while(0)
 #define __Pyx_XCLEAR(r)   do { if((r) != NULL) {PyObject* tmp = ((PyObject*)(r)); r = NULL; __Pyx_DECREF(tmp);}} while(0)
 
+/* PyErrExceptionMatches.proto */
+#if CYTHON_FAST_THREAD_STATE
+#define __Pyx_PyErr_ExceptionMatches(err) __Pyx_PyErr_ExceptionMatchesInState(__pyx_tstate, err)
+static CYTHON_INLINE int __Pyx_PyErr_ExceptionMatchesInState(PyThreadState* tstate, PyObject* err);
+#else
+#define __Pyx_PyErr_ExceptionMatches(err)  PyErr_ExceptionMatches(err)
+#endif
+
+/* PyThreadStateGet.proto */
+#if CYTHON_FAST_THREAD_STATE
+#define __Pyx_PyThreadState_declare  PyThreadState *__pyx_tstate;
+#define __Pyx_PyThreadState_assign  __pyx_tstate = __Pyx_PyThreadState_Current;
+#if PY_VERSION_HEX >= 0x030C00A6
+#define __Pyx_PyErr_Occurred()  (__pyx_tstate->current_exception != NULL)
+#define __Pyx_PyErr_CurrentExceptionType()  (__pyx_tstate->current_exception ? (PyObject*) Py_TYPE(__pyx_tstate->current_exception) : (PyObject*) NULL)
+#else
+#define __Pyx_PyErr_Occurred()  (__pyx_tstate->curexc_type != NULL)
+#define __Pyx_PyErr_CurrentExceptionType()  (__pyx_tstate->curexc_type)
+#endif
+#else
+#define __Pyx_PyThreadState_declare
+#define __Pyx_PyThreadState_assign
+#define __Pyx_PyErr_Occurred()  (PyErr_Occurred() != NULL)
+#define __Pyx_PyErr_CurrentExceptionType()  PyErr_Occurred()
+#endif
+
+/* PyErrFetchRestore.proto */
+#if CYTHON_FAST_THREAD_STATE
+#define __Pyx_PyErr_Clear() __Pyx_ErrRestore(NULL, NULL, NULL)
+#define __Pyx_ErrRestoreWithState(type, value, tb)  __Pyx_ErrRestoreInState(PyThreadState_GET(), type, value, tb)
+#define __Pyx_ErrFetchWithState(type, value, tb)    __Pyx_ErrFetchInState(PyThreadState_GET(), type, value, tb)
+#define __Pyx_ErrRestore(type, value, tb)  __Pyx_ErrRestoreInState(__pyx_tstate, type, value, tb)
+#define __Pyx_ErrFetch(type, value, tb)    __Pyx_ErrFetchInState(__pyx_tstate, type, value, tb)
+static CYTHON_INLINE void __Pyx_ErrRestoreInState(PyThreadState *tstate, PyObject *type, PyObject *value, PyObject *tb);
+static CYTHON_INLINE void __Pyx_ErrFetchInState(PyThreadState *tstate, PyObject **type, PyObject **value, PyObject **tb);
+#if CYTHON_COMPILING_IN_CPYTHON && PY_VERSION_HEX < 0x030C00A6
+#define __Pyx_PyErr_SetNone(exc) (Py_INCREF(exc), __Pyx_ErrRestore((exc), NULL, NULL))
+#else
+#define __Pyx_PyErr_SetNone(exc) PyErr_SetNone(exc)
+#endif
+#else
+#define __Pyx_PyErr_Clear() PyErr_Clear()
+#define __Pyx_PyErr_SetNone(exc) PyErr_SetNone(exc)
+#define __Pyx_ErrRestoreWithState(type, value, tb)  PyErr_Restore(type, value, tb)
+#define __Pyx_ErrFetchWithState(type, value, tb)  PyErr_Fetch(type, value, tb)
+#define __Pyx_ErrRestoreInState(tstate, type, value, tb)  PyErr_Restore(type, value, tb)
+#define __Pyx_ErrFetchInState(tstate, type, value, tb)  PyErr_Fetch(type, value, tb)
+#define __Pyx_ErrRestore(type, value, tb)  PyErr_Restore(type, value, tb)
+#define __Pyx_ErrFetch(type, value, tb)  PyErr_Fetch(type, value, tb)
+#endif
+
 /* PyObjectGetAttrStr.proto */
 #if CYTHON_USE_TYPE_SLOTS
 static CYTHON_INLINE PyObject* __Pyx_PyObject_GetAttrStr(PyObject* obj, PyObject* attr_name);
 #else
 #define __Pyx_PyObject_GetAttrStr(o,n) PyObject_GetAttr(o,n)
 #endif
 
+/* PyObjectGetAttrStrNoError.proto */
+static CYTHON_INLINE PyObject* __Pyx_PyObject_GetAttrStrNoError(PyObject* obj, PyObject* attr_name);
+
 /* GetBuiltinName.proto */
 static PyObject *__Pyx_GetBuiltinName(PyObject *name);
 
-/* PyCFunctionFastCall.proto */
-#if CYTHON_FAST_PYCCALL
-static CYTHON_INLINE PyObject *__Pyx_PyCFunction_FastCall(PyObject *func, PyObject **args, Py_ssize_t nargs);
-#else
-#define __Pyx_PyCFunction_FastCall(func, args, nargs)  (assert(0), NULL)
-#endif
-
 /* PyFunctionFastCall.proto */
 #if CYTHON_FAST_PYCALL
+#if !CYTHON_VECTORCALL
 #define __Pyx_PyFunction_FastCall(func, args, nargs)\
     __Pyx_PyFunction_FastCallDict((func), (args), (nargs), NULL)
-#if 1 || PY_VERSION_HEX < 0x030600B1
 static PyObject *__Pyx_PyFunction_FastCallDict(PyObject *func, PyObject **args, Py_ssize_t nargs, PyObject *kwargs);
-#else
-#define __Pyx_PyFunction_FastCallDict(func, args, nargs, kwargs) _PyFunction_FastCallDict(func, args, nargs, kwargs)
 #endif
 #define __Pyx_BUILD_ASSERT_EXPR(cond)\
     (sizeof(char [1 - 2*!(cond)]) - 1)
 #ifndef Py_MEMBER_SIZE
 #define Py_MEMBER_SIZE(type, member) sizeof(((type *)0)->member)
 #endif
-#if CYTHON_FAST_PYCALL
-  static size_t __pyx_pyframe_localsplus_offset = 0;
+#if !CYTHON_VECTORCALL
+#if PY_VERSION_HEX >= 0x03080000
   #include "frameobject.h"
 #if PY_VERSION_HEX >= 0x030b00a6
   #ifndef Py_BUILD_CORE
     #define Py_BUILD_CORE 1
   #endif
   #include "internal/pycore_frame.h"
 #endif
+  #define __Pxy_PyFrame_Initialize_Offsets()
+  #define __Pyx_PyFrame_GetLocalsplus(frame)  ((frame)->f_localsplus)
+#else
+  static size_t __pyx_pyframe_localsplus_offset = 0;
+  #include "frameobject.h"
   #define __Pxy_PyFrame_Initialize_Offsets()\
     ((void)__Pyx_BUILD_ASSERT_EXPR(sizeof(PyFrameObject) == offsetof(PyFrameObject, f_localsplus) + Py_MEMBER_SIZE(PyFrameObject, f_localsplus)),\
      (void)(__pyx_pyframe_localsplus_offset = ((size_t)PyFrame_Type.tp_basicsize) - Py_MEMBER_SIZE(PyFrameObject, f_localsplus)))
   #define __Pyx_PyFrame_GetLocalsplus(frame)\
     (assert(__pyx_pyframe_localsplus_offset), (PyObject **)(((char *)(frame)) + __pyx_pyframe_localsplus_offset))
-#endif // CYTHON_FAST_PYCALL
+#endif
+#endif
 #endif
 
 /* PyObjectCall.proto */
 #if CYTHON_COMPILING_IN_CPYTHON
 static CYTHON_INLINE PyObject* __Pyx_PyObject_Call(PyObject *func, PyObject *arg, PyObject *kw);
 #else
 #define __Pyx_PyObject_Call(func, arg, kw) PyObject_Call(func, arg, kw)
 #endif
 
-/* PyObjectCall2Args.proto */
-static CYTHON_UNUSED PyObject* __Pyx_PyObject_Call2Args(PyObject* function, PyObject* arg1, PyObject* arg2);
-
 /* PyObjectCallMethO.proto */
 #if CYTHON_COMPILING_IN_CPYTHON
 static CYTHON_INLINE PyObject* __Pyx_PyObject_CallMethO(PyObject *func, PyObject *arg);
 #endif
 
-/* PyObjectCallOneArg.proto */
-static CYTHON_INLINE PyObject* __Pyx_PyObject_CallOneArg(PyObject *func, PyObject *arg);
+/* PyObjectFastCall.proto */
+#define __Pyx_PyObject_FastCall(func, args, nargs)  __Pyx_PyObject_FastCallDict(func, args, (size_t)(nargs), NULL)
+static CYTHON_INLINE PyObject* __Pyx_PyObject_FastCallDict(PyObject *func, PyObject **args, size_t nargs, PyObject *kwargs);
 
-/* PyThreadStateGet.proto */
-#if CYTHON_FAST_THREAD_STATE
-#define __Pyx_PyThreadState_declare  PyThreadState *__pyx_tstate;
-#define __Pyx_PyThreadState_assign  __pyx_tstate = __Pyx_PyThreadState_Current;
-#define __Pyx_PyErr_Occurred()  __pyx_tstate->curexc_type
-#else
-#define __Pyx_PyThreadState_declare
-#define __Pyx_PyThreadState_assign
-#define __Pyx_PyErr_Occurred()  PyErr_Occurred()
-#endif
+/* WriteUnraisableException.proto */
+static void __Pyx_WriteUnraisable(const char *name, int clineno,
+                                  int lineno, const char *filename,
+                                  int full_traceback, int nogil);
 
-/* PyErrFetchRestore.proto */
-#if CYTHON_FAST_THREAD_STATE
-#define __Pyx_PyErr_Clear() __Pyx_ErrRestore(NULL, NULL, NULL)
-#define __Pyx_ErrRestoreWithState(type, value, tb)  __Pyx_ErrRestoreInState(PyThreadState_GET(), type, value, tb)
-#define __Pyx_ErrFetchWithState(type, value, tb)    __Pyx_ErrFetchInState(PyThreadState_GET(), type, value, tb)
-#define __Pyx_ErrRestore(type, value, tb)  __Pyx_ErrRestoreInState(__pyx_tstate, type, value, tb)
-#define __Pyx_ErrFetch(type, value, tb)    __Pyx_ErrFetchInState(__pyx_tstate, type, value, tb)
-static CYTHON_INLINE void __Pyx_ErrRestoreInState(PyThreadState *tstate, PyObject *type, PyObject *value, PyObject *tb);
-static CYTHON_INLINE void __Pyx_ErrFetchInState(PyThreadState *tstate, PyObject **type, PyObject **value, PyObject **tb);
+/* TupleAndListFromArray.proto */
 #if CYTHON_COMPILING_IN_CPYTHON
-#define __Pyx_PyErr_SetNone(exc) (Py_INCREF(exc), __Pyx_ErrRestore((exc), NULL, NULL))
-#else
-#define __Pyx_PyErr_SetNone(exc) PyErr_SetNone(exc)
+static CYTHON_INLINE PyObject* __Pyx_PyList_FromArray(PyObject *const *src, Py_ssize_t n);
+static CYTHON_INLINE PyObject* __Pyx_PyTuple_FromArray(PyObject *const *src, Py_ssize_t n);
 #endif
+
+/* IncludeStringH.proto */
+#include <string.h>
+
+/* BytesEquals.proto */
+static CYTHON_INLINE int __Pyx_PyBytes_Equals(PyObject* s1, PyObject* s2, int equals);
+
+/* UnicodeEquals.proto */
+static CYTHON_INLINE int __Pyx_PyUnicode_Equals(PyObject* s1, PyObject* s2, int equals);
+
+/* fastcall.proto */
+#define __Pyx_Arg_VARARGS(args, i) PyTuple_GET_ITEM(args, i)
+#define __Pyx_NumKwargs_VARARGS(kwds) PyDict_Size(kwds)
+#define __Pyx_KwValues_VARARGS(args, nargs) NULL
+#define __Pyx_GetKwValue_VARARGS(kw, kwvalues, s) __Pyx_PyDict_GetItemStrWithError(kw, s)
+#define __Pyx_KwargsAsDict_VARARGS(kw, kwvalues) PyDict_Copy(kw)
+#if CYTHON_METH_FASTCALL
+    #define __Pyx_Arg_FASTCALL(args, i) args[i]
+    #define __Pyx_NumKwargs_FASTCALL(kwds) PyTuple_GET_SIZE(kwds)
+    #define __Pyx_KwValues_FASTCALL(args, nargs) ((args) + (nargs))
+    static CYTHON_INLINE PyObject * __Pyx_GetKwValue_FASTCALL(PyObject *kwnames, PyObject *const *kwvalues, PyObject *s);
+    #define __Pyx_KwargsAsDict_FASTCALL(kw, kwvalues) _PyStack_AsDict(kwvalues, kw)
+#else
+    #define __Pyx_Arg_FASTCALL __Pyx_Arg_VARARGS
+    #define __Pyx_NumKwargs_FASTCALL __Pyx_NumKwargs_VARARGS
+    #define __Pyx_KwValues_FASTCALL __Pyx_KwValues_VARARGS
+    #define __Pyx_GetKwValue_FASTCALL __Pyx_GetKwValue_VARARGS
+    #define __Pyx_KwargsAsDict_FASTCALL __Pyx_KwargsAsDict_VARARGS
+#endif
+#if CYTHON_COMPILING_IN_CPYTHON
+#define __Pyx_ArgsSlice_VARARGS(args, start, stop) __Pyx_PyTuple_FromArray(&__Pyx_Arg_VARARGS(args, start), stop - start)
+#define __Pyx_ArgsSlice_FASTCALL(args, start, stop) __Pyx_PyTuple_FromArray(&__Pyx_Arg_FASTCALL(args, start), stop - start)
 #else
-#define __Pyx_PyErr_Clear() PyErr_Clear()
-#define __Pyx_PyErr_SetNone(exc) PyErr_SetNone(exc)
-#define __Pyx_ErrRestoreWithState(type, value, tb)  PyErr_Restore(type, value, tb)
-#define __Pyx_ErrFetchWithState(type, value, tb)  PyErr_Fetch(type, value, tb)
-#define __Pyx_ErrRestoreInState(tstate, type, value, tb)  PyErr_Restore(type, value, tb)
-#define __Pyx_ErrFetchInState(tstate, type, value, tb)  PyErr_Fetch(type, value, tb)
-#define __Pyx_ErrRestore(type, value, tb)  PyErr_Restore(type, value, tb)
-#define __Pyx_ErrFetch(type, value, tb)  PyErr_Fetch(type, value, tb)
+#define __Pyx_ArgsSlice_VARARGS(args, start, stop) PyTuple_GetSlice(args, start, stop)
+#define __Pyx_ArgsSlice_FASTCALL(args, start, stop) PyTuple_GetSlice(args, start, stop)
 #endif
 
-/* WriteUnraisableException.proto */
-static void __Pyx_WriteUnraisable(const char *name, int clineno,
-                                  int lineno, const char *filename,
-                                  int full_traceback, int nogil);
-
 /* RaiseDoubleKeywords.proto */
 static void __Pyx_RaiseDoubleKeywordsError(const char* func_name, PyObject* kw_name);
 
 /* ParseKeywords.proto */
-static int __Pyx_ParseOptionalKeywords(PyObject *kwds, PyObject **argnames[],\
-    PyObject *kwds2, PyObject *values[], Py_ssize_t num_pos_args,\
+static int __Pyx_ParseOptionalKeywords(PyObject *kwds, PyObject *const *kwvalues,
+    PyObject **argnames[],
+    PyObject *kwds2, PyObject *values[], Py_ssize_t num_pos_args,
     const char* function_name);
 
 /* RaiseArgTupleInvalid.proto */
 static void __Pyx_RaiseArgtupleInvalid(const char* func_name, int exact,
     Py_ssize_t num_min, Py_ssize_t num_max, Py_ssize_t num_found);
 
+/* KeywordStringCheck.proto */
+static int __Pyx_CheckKeywordStrings(PyObject *kw, const char* function_name, int kw_allowed);
+
 /* ArgTypeTest.proto */
 #define __Pyx_ArgTypeTest(obj, type, none_allowed, name, exact)\
-    ((likely((Py_TYPE(obj) == type) | (none_allowed && (obj == Py_None)))) ? 1 :\
+    ((likely(__Pyx_IS_TYPE(obj, type) | (none_allowed && (obj == Py_None)))) ? 1 :\
         __Pyx__ArgTypeTest(obj, type, name, exact))
 static int __Pyx__ArgTypeTest(PyObject *obj, PyTypeObject *type, const char *name, int exact);
 
+/* PyObjectCallOneArg.proto */
+static CYTHON_INLINE PyObject* __Pyx_PyObject_CallOneArg(PyObject *func, PyObject *arg);
+
 /* RaiseException.proto */
 static void __Pyx_Raise(PyObject *type, PyObject *value, PyObject *tb, PyObject *cause);
 
-/* IncludeStringH.proto */
-#include <string.h>
+/* IncludeStructmemberH.proto */
+#include <structmember.h>
+
+/* FixUpExtensionType.proto */
+#if CYTHON_USE_TYPE_SPECS
+static int __Pyx_fix_up_extension_type_from_spec(PyType_Spec *spec, PyTypeObject *type);
+#endif
+
+/* PyObjectCallNoArg.proto */
+static CYTHON_INLINE PyObject* __Pyx_PyObject_CallNoArg(PyObject *func);
+
+/* PyObjectGetMethod.proto */
+static int __Pyx_PyObject_GetMethod(PyObject *obj, PyObject *name, PyObject **method);
+
+/* PyObjectCallMethod0.proto */
+static PyObject* __Pyx_PyObject_CallMethod0(PyObject* obj, PyObject* method_name);
+
+/* ValidateBasesTuple.proto */
+#if CYTHON_COMPILING_IN_CPYTHON || CYTHON_COMPILING_IN_LIMITED_API || CYTHON_USE_TYPE_SPECS
+static int __Pyx_validate_bases_tuple(const char *type_name, Py_ssize_t dictoffset, PyObject *bases);
+#endif
+
+/* PyType_Ready.proto */
+CYTHON_UNUSED static int __Pyx_PyType_Ready(PyTypeObject *t);
 
 /* PyObject_GenericGetAttrNoDict.proto */
 #if CYTHON_USE_TYPE_SLOTS && CYTHON_USE_PYTYPE_LOOKUP && PY_VERSION_HEX < 0x03070000
 static CYTHON_INLINE PyObject* __Pyx_PyObject_GenericGetAttrNoDict(PyObject* obj, PyObject* attr_name);
 #else
 #define __Pyx_PyObject_GenericGetAttrNoDict PyObject_GenericGetAttr
 #endif
 
 /* SetVTable.proto */
-static int __Pyx_SetVtable(PyObject *dict, void *vtable);
+static int __Pyx_SetVtable(PyTypeObject* typeptr , void* vtable);
 
-/* PyErrExceptionMatches.proto */
-#if CYTHON_FAST_THREAD_STATE
-#define __Pyx_PyErr_ExceptionMatches(err) __Pyx_PyErr_ExceptionMatchesInState(__pyx_tstate, err)
-static CYTHON_INLINE int __Pyx_PyErr_ExceptionMatchesInState(PyThreadState* tstate, PyObject* err);
-#else
-#define __Pyx_PyErr_ExceptionMatches(err)  PyErr_ExceptionMatches(err)
-#endif
+/* GetVTable.proto */
+static void* __Pyx_GetVtable(PyTypeObject *type);
 
-/* PyObjectGetAttrStrNoError.proto */
-static CYTHON_INLINE PyObject* __Pyx_PyObject_GetAttrStrNoError(PyObject* obj, PyObject* attr_name);
+/* MergeVTables.proto */
+#if !CYTHON_COMPILING_IN_LIMITED_API
+static int __Pyx_MergeVtables(PyTypeObject *type);
+#endif
 
 /* SetupReduce.proto */
+#if !CYTHON_COMPILING_IN_LIMITED_API
 static int __Pyx_setup_reduce(PyObject* type_obj);
+#endif
+
+/* FetchSharedCythonModule.proto */
+static PyObject *__Pyx_FetchSharedCythonABIModule(void);
+
+/* FetchCommonType.proto */
+#if !CYTHON_USE_TYPE_SPECS
+static PyTypeObject* __Pyx_FetchCommonType(PyTypeObject* type);
+#else
+static PyTypeObject* __Pyx_FetchCommonTypeFromSpec(PyObject *module, PyType_Spec *spec, PyObject *bases);
+#endif
+
+/* PyMethodNew.proto */
+#if PY_MAJOR_VERSION >= 3
+static PyObject *__Pyx_PyMethod_New(PyObject *func, PyObject *self, PyObject *typ) {
+    CYTHON_UNUSED_VAR(typ);
+    if (!self)
+        return __Pyx_NewRef(func);
+    return PyMethod_New(func, self);
+}
+#else
+    #define __Pyx_PyMethod_New PyMethod_New
+#endif
+
+/* PyVectorcallFastCallDict.proto */
+#if CYTHON_METH_FASTCALL
+static CYTHON_INLINE PyObject *__Pyx_PyVectorcall_FastCallDict(PyObject *func, __pyx_vectorcallfunc vc, PyObject *const *args, size_t nargs, PyObject *kw);
+#endif
+
+/* CythonFunctionShared.proto */
+#define __Pyx_CyFunction_USED
+#define __Pyx_CYFUNCTION_STATICMETHOD  0x01
+#define __Pyx_CYFUNCTION_CLASSMETHOD   0x02
+#define __Pyx_CYFUNCTION_CCLASS        0x04
+#define __Pyx_CYFUNCTION_COROUTINE     0x08
+#define __Pyx_CyFunction_GetClosure(f)\
+    (((__pyx_CyFunctionObject *) (f))->func_closure)
+#if PY_VERSION_HEX < 0x030900B1
+  #define __Pyx_CyFunction_GetClassObj(f)\
+      (((__pyx_CyFunctionObject *) (f))->func_classobj)
+#else
+  #define __Pyx_CyFunction_GetClassObj(f)\
+      ((PyObject*) ((PyCMethodObject *) (f))->mm_class)
+#endif
+#define __Pyx_CyFunction_SetClassObj(f, classobj)\
+    __Pyx__CyFunction_SetClassObj((__pyx_CyFunctionObject *) (f), (classobj))
+#define __Pyx_CyFunction_Defaults(type, f)\
+    ((type *)(((__pyx_CyFunctionObject *) (f))->defaults))
+#define __Pyx_CyFunction_SetDefaultsGetter(f, g)\
+    ((__pyx_CyFunctionObject *) (f))->defaults_getter = (g)
+typedef struct {
+#if PY_VERSION_HEX < 0x030900B1
+    PyCFunctionObject func;
+#else
+    PyCMethodObject func;
+#endif
+#if CYTHON_BACKPORT_VECTORCALL
+    __pyx_vectorcallfunc func_vectorcall;
+#endif
+#if PY_VERSION_HEX < 0x030500A0
+    PyObject *func_weakreflist;
+#endif
+    PyObject *func_dict;
+    PyObject *func_name;
+    PyObject *func_qualname;
+    PyObject *func_doc;
+    PyObject *func_globals;
+    PyObject *func_code;
+    PyObject *func_closure;
+#if PY_VERSION_HEX < 0x030900B1
+    PyObject *func_classobj;
+#endif
+    void *defaults;
+    int defaults_pyobjects;
+    size_t defaults_size;  // used by FusedFunction for copying defaults
+    int flags;
+    PyObject *defaults_tuple;
+    PyObject *defaults_kwdict;
+    PyObject *(*defaults_getter)(PyObject *);
+    PyObject *func_annotations;
+    PyObject *func_is_coroutine;
+} __pyx_CyFunctionObject;
+#define __Pyx_CyFunction_Check(obj)  __Pyx_TypeCheck(obj, __pyx_CyFunctionType)
+#define __Pyx_IsCyOrPyCFunction(obj)  __Pyx_TypeCheck2(obj, __pyx_CyFunctionType, &PyCFunction_Type)
+#define __Pyx_CyFunction_CheckExact(obj)  __Pyx_IS_TYPE(obj, __pyx_CyFunctionType)
+static PyObject *__Pyx_CyFunction_Init(__pyx_CyFunctionObject* op, PyMethodDef *ml,
+                                      int flags, PyObject* qualname,
+                                      PyObject *closure,
+                                      PyObject *module, PyObject *globals,
+                                      PyObject* code);
+static CYTHON_INLINE void __Pyx__CyFunction_SetClassObj(__pyx_CyFunctionObject* f, PyObject* classobj);
+static CYTHON_INLINE void *__Pyx_CyFunction_InitDefaults(PyObject *m,
+                                                         size_t size,
+                                                         int pyobjects);
+static CYTHON_INLINE void __Pyx_CyFunction_SetDefaultsTuple(PyObject *m,
+                                                            PyObject *tuple);
+static CYTHON_INLINE void __Pyx_CyFunction_SetDefaultsKwDict(PyObject *m,
+                                                             PyObject *dict);
+static CYTHON_INLINE void __Pyx_CyFunction_SetAnnotationsDict(PyObject *m,
+                                                              PyObject *dict);
+static int __pyx_CyFunction_init(PyObject *module);
+#if CYTHON_METH_FASTCALL
+static PyObject * __Pyx_CyFunction_Vectorcall_NOARGS(PyObject *func, PyObject *const *args, size_t nargsf, PyObject *kwnames);
+static PyObject * __Pyx_CyFunction_Vectorcall_O(PyObject *func, PyObject *const *args, size_t nargsf, PyObject *kwnames);
+static PyObject * __Pyx_CyFunction_Vectorcall_FASTCALL_KEYWORDS(PyObject *func, PyObject *const *args, size_t nargsf, PyObject *kwnames);
+static PyObject * __Pyx_CyFunction_Vectorcall_FASTCALL_KEYWORDS_METHOD(PyObject *func, PyObject *const *args, size_t nargsf, PyObject *kwnames);
+#if CYTHON_BACKPORT_VECTORCALL
+#define __Pyx_CyFunction_func_vectorcall(f) (((__pyx_CyFunctionObject*)f)->func_vectorcall)
+#else
+#define __Pyx_CyFunction_func_vectorcall(f) (((PyCFunctionObject*)f)->vectorcall)
+#endif
+#endif
+
+/* CythonFunction.proto */
+static PyObject *__Pyx_CyFunction_New(PyMethodDef *ml,
+                                      int flags, PyObject* qualname,
+                                      PyObject *closure,
+                                      PyObject *module, PyObject *globals,
+                                      PyObject* code);
 
 /* PyDictVersioning.proto */
 #if CYTHON_USE_DICT_VERSIONS && CYTHON_USE_TYPE_SLOTS
 #define __PYX_DICT_VERSION_INIT  ((PY_UINT64_T) -1)
 #define __PYX_GET_DICT_VERSION(dict)  (((PyDictObject*)(dict))->ma_version_tag)
 #define __PYX_UPDATE_DICT_CACHE(dict, value, cache_var, version_var)\
     (version_var) = __PYX_GET_DICT_VERSION(dict);\
@@ -1346,68 +1952,91 @@
 #ifdef CYTHON_CLINE_IN_TRACEBACK
 #define __Pyx_CLineForTraceback(tstate, c_line)  (((CYTHON_CLINE_IN_TRACEBACK)) ? c_line : 0)
 #else
 static int __Pyx_CLineForTraceback(PyThreadState *tstate, int c_line);
 #endif
 
 /* CodeObjectCache.proto */
+#if !CYTHON_COMPILING_IN_LIMITED_API
 typedef struct {
     PyCodeObject* code_object;
     int code_line;
 } __Pyx_CodeObjectCacheEntry;
 struct __Pyx_CodeObjectCache {
     int count;
     int max_count;
     __Pyx_CodeObjectCacheEntry* entries;
 };
 static struct __Pyx_CodeObjectCache __pyx_code_cache = {0,0,NULL};
 static int __pyx_bisect_code_objects(__Pyx_CodeObjectCacheEntry* entries, int count, int code_line);
 static PyCodeObject *__pyx_find_code_object(int code_line);
 static void __pyx_insert_code_object(int code_line, PyCodeObject* code_object);
+#endif
 
 /* AddTraceback.proto */
 static void __Pyx_AddTraceback(const char *funcname, int c_line,
                                int py_line, const char *filename);
 
 /* GCCDiagnostics.proto */
-#if defined(__GNUC__) && (__GNUC__ > 4 || (__GNUC__ == 4 && __GNUC_MINOR__ >= 6))
+#if !defined(__INTEL_COMPILER) && defined(__GNUC__) && (__GNUC__ > 4 || (__GNUC__ == 4 && __GNUC_MINOR__ >= 6))
 #define __Pyx_HAS_GCC_DIAGNOSTIC
 #endif
 
 /* CIntFromPy.proto */
 static CYTHON_INLINE size_t __Pyx_PyInt_As_size_t(PyObject *);
 
+/* CIntFromPy.proto */
+static CYTHON_INLINE bool __Pyx_PyInt_As_bool(PyObject *);
+
+/* FormatTypeName.proto */
+#if CYTHON_COMPILING_IN_LIMITED_API
+typedef PyObject *__Pyx_TypeName;
+#define __Pyx_FMT_TYPENAME "%U"
+static __Pyx_TypeName __Pyx_PyType_GetName(PyTypeObject* tp);
+#define __Pyx_DECREF_TypeName(obj) Py_XDECREF(obj)
+#else
+typedef const char *__Pyx_TypeName;
+#define __Pyx_FMT_TYPENAME "%.200s"
+#define __Pyx_PyType_GetName(tp) ((tp)->tp_name)
+#define __Pyx_DECREF_TypeName(obj)
+#endif
+
 /* CIntToPy.proto */
 static CYTHON_INLINE PyObject* __Pyx_PyInt_From_long(long value);
 
 /* CIntFromPy.proto */
 static CYTHON_INLINE long __Pyx_PyInt_As_long(PyObject *);
 
 /* CIntFromPy.proto */
 static CYTHON_INLINE int __Pyx_PyInt_As_int(PyObject *);
 
 /* FastTypeChecks.proto */
 #if CYTHON_COMPILING_IN_CPYTHON
 #define __Pyx_TypeCheck(obj, type) __Pyx_IsSubtype(Py_TYPE(obj), (PyTypeObject *)type)
+#define __Pyx_TypeCheck2(obj, type1, type2) __Pyx_IsAnySubtype2(Py_TYPE(obj), (PyTypeObject *)type1, (PyTypeObject *)type2)
 static CYTHON_INLINE int __Pyx_IsSubtype(PyTypeObject *a, PyTypeObject *b);
+static CYTHON_INLINE int __Pyx_IsAnySubtype2(PyTypeObject *cls, PyTypeObject *a, PyTypeObject *b);
 static CYTHON_INLINE int __Pyx_PyErr_GivenExceptionMatches(PyObject *err, PyObject *type);
 static CYTHON_INLINE int __Pyx_PyErr_GivenExceptionMatches2(PyObject *err, PyObject *type1, PyObject *type2);
 #else
 #define __Pyx_TypeCheck(obj, type) PyObject_TypeCheck(obj, (PyTypeObject *)type)
+#define __Pyx_TypeCheck2(obj, type1, type2) (PyObject_TypeCheck(obj, (PyTypeObject *)type1) || PyObject_TypeCheck(obj, (PyTypeObject *)type2))
 #define __Pyx_PyErr_GivenExceptionMatches(err, type) PyErr_GivenExceptionMatches(err, type)
 #define __Pyx_PyErr_GivenExceptionMatches2(err, type1, type2) (PyErr_GivenExceptionMatches(err, type1) || PyErr_GivenExceptionMatches(err, type2))
 #endif
+#define __Pyx_PyErr_ExceptionMatches2(err1, err2)  __Pyx_PyErr_GivenExceptionMatches2(__Pyx_PyErr_CurrentExceptionType(), err1, err2)
 #define __Pyx_PyException_Check(obj) __Pyx_TypeCheck(obj, PyExc_Exception)
 
 /* CheckBinaryVersion.proto */
 static int __Pyx_check_binary_version(void);
 
 /* InitStrings.proto */
 static int __Pyx_InitStrings(__Pyx_StringTabEntry *t);
 
+/* #### Code section: module_declarations ### */
 static CYTHON_INLINE struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_from_ptr(bitset_t *__pyx_v_ptr); /* proto*/
 static CYTHON_INLINE PyObject *__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_clear(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, CYTHON_UNUSED int __pyx_skip_dispatch); /* proto*/
 static CYTHON_INLINE PyObject *__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_fill(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, CYTHON_UNUSED int __pyx_skip_dispatch); /* proto*/
 static CYTHON_INLINE struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_copy(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, CYTHON_UNUSED int __pyx_skip_dispatch); /* proto*/
 static CYTHON_INLINE int __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_resize(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, size_t __pyx_v_newarraysize, int __pyx_v_padwithzeroes, CYTHON_UNUSED int __pyx_skip_dispatch); /* proto*/
 static CYTHON_INLINE size_t __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_size_in_bytes(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, CYTHON_UNUSED int __pyx_skip_dispatch); /* proto*/
 static CYTHON_INLINE size_t __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_size_in_bits(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, CYTHON_UNUSED int __pyx_skip_dispatch); /* proto*/
@@ -1432,76 +2061,135 @@
 static CYTHON_INLINE PyObject *__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_inplace_difference(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2, CYTHON_UNUSED int __pyx_skip_dispatch); /* proto*/
 static CYTHON_INLINE size_t __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_difference_count(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2, CYTHON_UNUSED int __pyx_skip_dispatch); /* proto*/
 static CYTHON_INLINE int __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_inplace_symmetric_difference(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2, CYTHON_UNUSED int __pyx_skip_dispatch); /* proto*/
 static CYTHON_INLINE size_t __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_symmetric_difference_count(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2, CYTHON_UNUSED int __pyx_skip_dispatch); /* proto*/
 static CYTHON_INLINE int __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_for_each(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, PyObject *__pyx_v_func, CYTHON_UNUSED int __pyx_skip_dispatch); /* proto*/
 static CYTHON_INLINE PyObject *__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_print(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, CYTHON_UNUSED int __pyx_skip_dispatch); /* proto*/
 
-/* Module declarations from 'cython' */
+/* Module declarations from "cython" */
 
-/* Module declarations from 'pybitset.backends.cython.bitset' */
+/* Module declarations from "pybitset.backends.cython.bitset" */
 
-/* Module declarations from 'pybitset.backends.cython._bitset' */
-static PyTypeObject *__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet = 0;
-static PyTypeObject *__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSetIter = 0;
-static int __pyx_f_8pybitset_8backends_6cython_7_bitset_bitset_iterator_func(size_t, void *); /*proto*/
+/* Module declarations from "pybitset.backends.cython._bitset" */
+static bool __pyx_f_8pybitset_8backends_6cython_7_bitset_bitset_iterator_func(size_t, void *); /*proto*/
+/* #### Code section: typeinfo ### */
+/* #### Code section: before_global_var ### */
 #define __Pyx_MODULE_NAME "pybitset.backends.cython._bitset"
 extern int __pyx_module_is_main_pybitset__backends__cython___bitset;
 int __pyx_module_is_main_pybitset__backends__cython___bitset = 0;
 
-/* Implementation of 'pybitset.backends.cython._bitset' */
+/* Implementation of "pybitset.backends.cython._bitset" */
+/* #### Code section: global_var ### */
 static PyObject *__pyx_builtin_MemoryError;
 static PyObject *__pyx_builtin_TypeError;
 static PyObject *__pyx_builtin_StopIteration;
+/* #### Code section: string_decls ### */
 static const char __pyx_k_b[] = "b";
 static const char __pyx_k_i[] = "i";
+static const char __pyx_k_s[] = "s";
+static const char __pyx_k_b2[] = "b2";
+static const char __pyx_k_gc[] = "gc";
+static const char __pyx_k__44[] = "?";
+static const char __pyx_k_get[] = "get";
+static const char __pyx_k_set[] = "set";
+static const char __pyx_k_copy[] = "copy";
+static const char __pyx_k_fill[] = "fill";
 static const char __pyx_k_flag[] = "flag";
+static const char __pyx_k_func[] = "func";
+static const char __pyx_k_grow[] = "grow";
 static const char __pyx_k_init[] = "_init";
 static const char __pyx_k_main[] = "__main__";
 static const char __pyx_k_name[] = "__name__";
+static const char __pyx_k_self[] = "self";
 static const char __pyx_k_size[] = "size";
 static const char __pyx_k_test[] = "__test__";
+static const char __pyx_k_trim[] = "trim";
+static const char __pyx_k_clear[] = "clear";
+static const char __pyx_k_count[] = "count";
+static const char __pyx_k_print[] = "print";
 static const char __pyx_k_BitSet[] = "BitSet";
+static const char __pyx_k_enable[] = "enable";
 static const char __pyx_k_reduce[] = "__reduce__";
+static const char __pyx_k_resize[] = "resize";
+static const char __pyx_k_disable[] = "disable";
+static const char __pyx_k_maximum[] = "maximum";
+static const char __pyx_k_minimum[] = "minimum";
+static const char __pyx_k_disjoint[] = "disjoint";
+static const char __pyx_k_for_each[] = "for_each";
 static const char __pyx_k_getstate[] = "__getstate__";
 static const char __pyx_k_setstate[] = "__setstate__";
 static const char __pyx_k_TypeError[] = "TypeError";
+static const char __pyx_k_intersect[] = "intersect";
+static const char __pyx_k_isenabled[] = "isenabled";
+static const char __pyx_k_pyx_state[] = "__pyx_state";
 static const char __pyx_k_reduce_ex[] = "__reduce_ex__";
+static const char __pyx_k_BitSet_get[] = "BitSet.get";
+static const char __pyx_k_BitSet_set[] = "BitSet.set";
 static const char __pyx_k_pyx_vtable[] = "__pyx_vtable__";
+static const char __pyx_k_shift_left[] = "shift_left";
+static const char __pyx_k_BitSet_copy[] = "BitSet.copy";
+static const char __pyx_k_BitSet_fill[] = "BitSet.fill";
+static const char __pyx_k_BitSet_grow[] = "BitSet.grow";
+static const char __pyx_k_BitSet_trim[] = "BitSet.trim";
 static const char __pyx_k_MemoryError[] = "MemoryError";
+static const char __pyx_k_shift_right[] = "shift_right";
+static const char __pyx_k_union_count[] = "union_count";
+static const char __pyx_k_BitSet_clear[] = "BitSet.clear";
+static const char __pyx_k_BitSet_count[] = "BitSet.count";
+static const char __pyx_k_BitSet_print[] = "BitSet.print";
+static const char __pyx_k_contains_all[] = "contains_all";
+static const char __pyx_k_is_coroutine[] = "_is_coroutine";
 static const char __pyx_k_newarraysize[] = "newarraysize";
+static const char __pyx_k_set_to_value[] = "set_to_value";
+static const char __pyx_k_size_in_bits[] = "size_in_bits";
+static const char __pyx_k_stringsource[] = "<stringsource>";
+static const char __pyx_k_BitSet_resize[] = "BitSet.resize";
 static const char __pyx_k_StopIteration[] = "StopIteration";
+static const char __pyx_k_inplace_union[] = "inplace_union";
 static const char __pyx_k_padwithzeroes[] = "padwithzeroes";
 static const char __pyx_k_reduce_cython[] = "__reduce_cython__";
+static const char __pyx_k_size_in_bytes[] = "size_in_bytes";
+static const char __pyx_k_size_in_words[] = "size_in_words";
+static const char __pyx_k_BitSet_maximum[] = "BitSet.maximum";
+static const char __pyx_k_BitSet_minimum[] = "BitSet.minimum";
+static const char __pyx_k_BitSet_disjoint[] = "BitSet.disjoint";
+static const char __pyx_k_BitSet_for_each[] = "BitSet.for_each";
 static const char __pyx_k_setstate_cython[] = "__setstate_cython__";
+static const char __pyx_k_BitSet_intersect[] = "BitSet.intersect";
+static const char __pyx_k_difference_count[] = "difference_count";
+static const char __pyx_k_BitSet_shift_left[] = "BitSet.shift_left";
+static const char __pyx_k_BitSet_shift_right[] = "BitSet.shift_right";
+static const char __pyx_k_BitSet_union_count[] = "BitSet.union_count";
+static const char __pyx_k_asyncio_coroutines[] = "asyncio.coroutines";
 static const char __pyx_k_cline_in_traceback[] = "cline_in_traceback";
+static const char __pyx_k_inplace_difference[] = "inplace_difference";
+static const char __pyx_k_intersection_count[] = "intersection_count";
+static const char __pyx_k_BitSet_contains_all[] = "BitSet.contains_all";
+static const char __pyx_k_BitSet_set_to_value[] = "BitSet.set_to_value";
+static const char __pyx_k_BitSet_size_in_bits[] = "BitSet.size_in_bits";
+static const char __pyx_k_BitSet_inplace_union[] = "BitSet.inplace_union";
+static const char __pyx_k_BitSet_size_in_bytes[] = "BitSet.size_in_bytes";
+static const char __pyx_k_BitSet_size_in_words[] = "BitSet.size_in_words";
+static const char __pyx_k_inplace_intersection[] = "inplace_intersection";
+static const char __pyx_k_BitSet___reduce_cython[] = "BitSet.__reduce_cython__";
+static const char __pyx_k_BitSet_difference_count[] = "BitSet.difference_count";
+static const char __pyx_k_BitSet___setstate_cython[] = "BitSet.__setstate_cython__";
+static const char __pyx_k_BitSet_inplace_difference[] = "BitSet.inplace_difference";
+static const char __pyx_k_BitSet_intersection_count[] = "BitSet.intersection_count";
+static const char __pyx_k_BitSetIter___reduce_cython[] = "BitSetIter.__reduce_cython__";
+static const char __pyx_k_symmetric_difference_count[] = "symmetric_difference_count";
+static const char __pyx_k_BitSet_inplace_intersection[] = "BitSet.inplace_intersection";
+static const char __pyx_k_BitSetIter___setstate_cython[] = "BitSetIter.__setstate_cython__";
+static const char __pyx_k_inplace_symmetric_difference[] = "inplace_symmetric_difference";
+static const char __pyx_k_BitSet_inplace_symmetric_differe[] = "BitSet.inplace_symmetric_difference";
+static const char __pyx_k_BitSet_symmetric_difference_coun[] = "BitSet.symmetric_difference_count";
 static const char __pyx_k_no_default___reduce___due_to_non[] = "no default __reduce__ due to non-trivial __cinit__";
-static PyObject *__pyx_n_s_BitSet;
-static PyObject *__pyx_n_s_MemoryError;
-static PyObject *__pyx_n_s_StopIteration;
-static PyObject *__pyx_n_s_TypeError;
-static PyObject *__pyx_n_s_b;
-static PyObject *__pyx_n_s_cline_in_traceback;
-static PyObject *__pyx_n_s_flag;
-static PyObject *__pyx_n_s_getstate;
-static PyObject *__pyx_n_s_i;
-static PyObject *__pyx_n_s_init;
-static PyObject *__pyx_n_s_main;
-static PyObject *__pyx_n_s_name;
-static PyObject *__pyx_n_s_newarraysize;
-static PyObject *__pyx_kp_s_no_default___reduce___due_to_non;
-static PyObject *__pyx_n_s_padwithzeroes;
-static PyObject *__pyx_n_s_pyx_vtable;
-static PyObject *__pyx_n_s_reduce;
-static PyObject *__pyx_n_s_reduce_cython;
-static PyObject *__pyx_n_s_reduce_ex;
-static PyObject *__pyx_n_s_setstate;
-static PyObject *__pyx_n_s_setstate_cython;
-static PyObject *__pyx_n_s_size;
-static PyObject *__pyx_n_s_test;
+static const char __pyx_k_pybitset_backends_cython__bitset[] = "pybitset\\backends\\cython\\_bitset.pyx";
+static const char __pyx_k_pybitset_backends_cython__bitset_2[] = "pybitset.backends.cython._bitset";
+/* #### Code section: decls ### */
 static int __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet___cinit__(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, size_t __pyx_v_size, int __pyx_v__init); /* proto */
 static void __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_2__dealloc__(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self); /* proto */
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_4clear(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self); /* proto */
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_6fill(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self); /* proto */
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_8copy(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self); /* proto */
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_10resize(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, size_t __pyx_v_newarraysize, int __pyx_v_padwithzeroes); /* proto */
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_12size_in_bytes(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self); /* proto */
@@ -1536,79 +2224,806 @@
 static int __pyx_pf_8pybitset_8backends_6cython_7_bitset_10BitSetIter___cinit__(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSetIter *__pyx_v_self, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b); /* proto */
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_10BitSetIter_2__iter__(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSetIter *__pyx_v_self); /* proto */
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_10BitSetIter_4__next__(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSetIter *__pyx_v_self); /* proto */
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_10BitSetIter_6__reduce_cython__(CYTHON_UNUSED struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSetIter *__pyx_v_self); /* proto */
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_10BitSetIter_8__setstate_cython__(CYTHON_UNUSED struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSetIter *__pyx_v_self, CYTHON_UNUSED PyObject *__pyx_v___pyx_state); /* proto */
 static PyObject *__pyx_tp_new_8pybitset_8backends_6cython_7_bitset_BitSet(PyTypeObject *t, PyObject *a, PyObject *k); /*proto*/
 static PyObject *__pyx_tp_new_8pybitset_8backends_6cython_7_bitset_BitSetIter(PyTypeObject *t, PyObject *a, PyObject *k); /*proto*/
-static PyObject *__pyx_tuple_;
-static PyObject *__pyx_tuple__2;
-static PyObject *__pyx_tuple__3;
-static PyObject *__pyx_tuple__4;
-/* Late includes */
+/* #### Code section: late_includes ### */
+/* #### Code section: module_state ### */
+typedef struct {
+  PyObject *__pyx_d;
+  PyObject *__pyx_b;
+  PyObject *__pyx_cython_runtime;
+  PyObject *__pyx_empty_tuple;
+  PyObject *__pyx_empty_bytes;
+  PyObject *__pyx_empty_unicode;
+  #ifdef __Pyx_CyFunction_USED
+  PyTypeObject *__pyx_CyFunctionType;
+  #endif
+  #ifdef __Pyx_FusedFunction_USED
+  PyTypeObject *__pyx_FusedFunctionType;
+  #endif
+  #ifdef __Pyx_Generator_USED
+  PyTypeObject *__pyx_GeneratorType;
+  #endif
+  #ifdef __Pyx_IterableCoroutine_USED
+  PyTypeObject *__pyx_IterableCoroutineType;
+  #endif
+  #ifdef __Pyx_Coroutine_USED
+  PyTypeObject *__pyx_CoroutineAwaitType;
+  #endif
+  #ifdef __Pyx_Coroutine_USED
+  PyTypeObject *__pyx_CoroutineType;
+  #endif
+  #if CYTHON_USE_MODULE_STATE
+  #endif
+  #if CYTHON_USE_MODULE_STATE
+  #endif
+  #if CYTHON_USE_MODULE_STATE
+  PyObject *__pyx_type_8pybitset_8backends_6cython_7_bitset_BitSet;
+  PyObject *__pyx_type_8pybitset_8backends_6cython_7_bitset_BitSetIter;
+  #endif
+  PyTypeObject *__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet;
+  PyTypeObject *__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSetIter;
+  PyObject *__pyx_n_s_BitSet;
+  PyObject *__pyx_n_s_BitSetIter___reduce_cython;
+  PyObject *__pyx_n_s_BitSetIter___setstate_cython;
+  PyObject *__pyx_n_s_BitSet___reduce_cython;
+  PyObject *__pyx_n_s_BitSet___setstate_cython;
+  PyObject *__pyx_n_s_BitSet_clear;
+  PyObject *__pyx_n_s_BitSet_contains_all;
+  PyObject *__pyx_n_s_BitSet_copy;
+  PyObject *__pyx_n_s_BitSet_count;
+  PyObject *__pyx_n_s_BitSet_difference_count;
+  PyObject *__pyx_n_s_BitSet_disjoint;
+  PyObject *__pyx_n_s_BitSet_fill;
+  PyObject *__pyx_n_s_BitSet_for_each;
+  PyObject *__pyx_n_s_BitSet_get;
+  PyObject *__pyx_n_s_BitSet_grow;
+  PyObject *__pyx_n_s_BitSet_inplace_difference;
+  PyObject *__pyx_n_s_BitSet_inplace_intersection;
+  PyObject *__pyx_n_s_BitSet_inplace_symmetric_differe;
+  PyObject *__pyx_n_s_BitSet_inplace_union;
+  PyObject *__pyx_n_s_BitSet_intersect;
+  PyObject *__pyx_n_s_BitSet_intersection_count;
+  PyObject *__pyx_n_s_BitSet_maximum;
+  PyObject *__pyx_n_s_BitSet_minimum;
+  PyObject *__pyx_n_s_BitSet_print;
+  PyObject *__pyx_n_s_BitSet_resize;
+  PyObject *__pyx_n_s_BitSet_set;
+  PyObject *__pyx_n_s_BitSet_set_to_value;
+  PyObject *__pyx_n_s_BitSet_shift_left;
+  PyObject *__pyx_n_s_BitSet_shift_right;
+  PyObject *__pyx_n_s_BitSet_size_in_bits;
+  PyObject *__pyx_n_s_BitSet_size_in_bytes;
+  PyObject *__pyx_n_s_BitSet_size_in_words;
+  PyObject *__pyx_n_s_BitSet_symmetric_difference_coun;
+  PyObject *__pyx_n_s_BitSet_trim;
+  PyObject *__pyx_n_s_BitSet_union_count;
+  PyObject *__pyx_n_s_MemoryError;
+  PyObject *__pyx_n_s_StopIteration;
+  PyObject *__pyx_n_s_TypeError;
+  PyObject *__pyx_n_s__44;
+  PyObject *__pyx_n_s_asyncio_coroutines;
+  PyObject *__pyx_n_s_b;
+  PyObject *__pyx_n_s_b2;
+  PyObject *__pyx_n_s_clear;
+  PyObject *__pyx_n_s_cline_in_traceback;
+  PyObject *__pyx_n_s_contains_all;
+  PyObject *__pyx_n_s_copy;
+  PyObject *__pyx_n_s_count;
+  PyObject *__pyx_n_s_difference_count;
+  PyObject *__pyx_kp_u_disable;
+  PyObject *__pyx_n_s_disjoint;
+  PyObject *__pyx_kp_u_enable;
+  PyObject *__pyx_n_s_fill;
+  PyObject *__pyx_n_s_flag;
+  PyObject *__pyx_n_s_for_each;
+  PyObject *__pyx_n_s_func;
+  PyObject *__pyx_kp_u_gc;
+  PyObject *__pyx_n_s_get;
+  PyObject *__pyx_n_s_getstate;
+  PyObject *__pyx_n_s_grow;
+  PyObject *__pyx_n_s_i;
+  PyObject *__pyx_n_s_init;
+  PyObject *__pyx_n_s_inplace_difference;
+  PyObject *__pyx_n_s_inplace_intersection;
+  PyObject *__pyx_n_s_inplace_symmetric_difference;
+  PyObject *__pyx_n_s_inplace_union;
+  PyObject *__pyx_n_s_intersect;
+  PyObject *__pyx_n_s_intersection_count;
+  PyObject *__pyx_n_s_is_coroutine;
+  PyObject *__pyx_kp_u_isenabled;
+  PyObject *__pyx_n_s_main;
+  PyObject *__pyx_n_s_maximum;
+  PyObject *__pyx_n_s_minimum;
+  PyObject *__pyx_n_s_name;
+  PyObject *__pyx_n_s_newarraysize;
+  PyObject *__pyx_kp_s_no_default___reduce___due_to_non;
+  PyObject *__pyx_n_s_padwithzeroes;
+  PyObject *__pyx_n_s_print;
+  PyObject *__pyx_kp_s_pybitset_backends_cython__bitset;
+  PyObject *__pyx_n_s_pybitset_backends_cython__bitset_2;
+  PyObject *__pyx_n_s_pyx_state;
+  PyObject *__pyx_n_s_pyx_vtable;
+  PyObject *__pyx_n_s_reduce;
+  PyObject *__pyx_n_s_reduce_cython;
+  PyObject *__pyx_n_s_reduce_ex;
+  PyObject *__pyx_n_s_resize;
+  PyObject *__pyx_n_s_s;
+  PyObject *__pyx_n_s_self;
+  PyObject *__pyx_n_s_set;
+  PyObject *__pyx_n_s_set_to_value;
+  PyObject *__pyx_n_s_setstate;
+  PyObject *__pyx_n_s_setstate_cython;
+  PyObject *__pyx_n_s_shift_left;
+  PyObject *__pyx_n_s_shift_right;
+  PyObject *__pyx_n_s_size;
+  PyObject *__pyx_n_s_size_in_bits;
+  PyObject *__pyx_n_s_size_in_bytes;
+  PyObject *__pyx_n_s_size_in_words;
+  PyObject *__pyx_kp_s_stringsource;
+  PyObject *__pyx_n_s_symmetric_difference_count;
+  PyObject *__pyx_n_s_test;
+  PyObject *__pyx_n_s_trim;
+  PyObject *__pyx_n_s_union_count;
+  PyObject *__pyx_tuple_;
+  PyObject *__pyx_tuple__5;
+  PyObject *__pyx_tuple__10;
+  PyObject *__pyx_tuple__13;
+  PyObject *__pyx_tuple__16;
+  PyObject *__pyx_tuple__18;
+  PyObject *__pyx_tuple__24;
+  PyObject *__pyx_tuple__36;
+  PyObject *__pyx_tuple__40;
+  PyObject *__pyx_codeobj__2;
+  PyObject *__pyx_codeobj__3;
+  PyObject *__pyx_codeobj__4;
+  PyObject *__pyx_codeobj__6;
+  PyObject *__pyx_codeobj__7;
+  PyObject *__pyx_codeobj__8;
+  PyObject *__pyx_codeobj__9;
+  PyObject *__pyx_codeobj__11;
+  PyObject *__pyx_codeobj__12;
+  PyObject *__pyx_codeobj__14;
+  PyObject *__pyx_codeobj__15;
+  PyObject *__pyx_codeobj__17;
+  PyObject *__pyx_codeobj__19;
+  PyObject *__pyx_codeobj__20;
+  PyObject *__pyx_codeobj__21;
+  PyObject *__pyx_codeobj__22;
+  PyObject *__pyx_codeobj__23;
+  PyObject *__pyx_codeobj__25;
+  PyObject *__pyx_codeobj__26;
+  PyObject *__pyx_codeobj__27;
+  PyObject *__pyx_codeobj__28;
+  PyObject *__pyx_codeobj__29;
+  PyObject *__pyx_codeobj__30;
+  PyObject *__pyx_codeobj__31;
+  PyObject *__pyx_codeobj__32;
+  PyObject *__pyx_codeobj__33;
+  PyObject *__pyx_codeobj__34;
+  PyObject *__pyx_codeobj__35;
+  PyObject *__pyx_codeobj__37;
+  PyObject *__pyx_codeobj__38;
+  PyObject *__pyx_codeobj__39;
+  PyObject *__pyx_codeobj__41;
+  PyObject *__pyx_codeobj__42;
+  PyObject *__pyx_codeobj__43;
+} __pyx_mstate;
+
+#if CYTHON_USE_MODULE_STATE
+#ifdef __cplusplus
+namespace {
+  extern struct PyModuleDef __pyx_moduledef;
+} /* anonymous namespace */
+#else
+static struct PyModuleDef __pyx_moduledef;
+#endif
+
+#define __pyx_mstate(o) ((__pyx_mstate *)__Pyx_PyModule_GetState(o))
+
+#define __pyx_mstate_global (__pyx_mstate(PyState_FindModule(&__pyx_moduledef)))
+
+#define __pyx_m (PyState_FindModule(&__pyx_moduledef))
+#else
+static __pyx_mstate __pyx_mstate_global_static =
+#ifdef __cplusplus
+    {};
+#else
+    {0};
+#endif
+static __pyx_mstate *__pyx_mstate_global = &__pyx_mstate_global_static;
+#endif
+/* #### Code section: module_state_clear ### */
+#if CYTHON_USE_MODULE_STATE
+static int __pyx_m_clear(PyObject *m) {
+  __pyx_mstate *clear_module_state = __pyx_mstate(m);
+  if (!clear_module_state) return 0;
+  Py_CLEAR(clear_module_state->__pyx_d);
+  Py_CLEAR(clear_module_state->__pyx_b);
+  Py_CLEAR(clear_module_state->__pyx_cython_runtime);
+  Py_CLEAR(clear_module_state->__pyx_empty_tuple);
+  Py_CLEAR(clear_module_state->__pyx_empty_bytes);
+  Py_CLEAR(clear_module_state->__pyx_empty_unicode);
+  #ifdef __Pyx_CyFunction_USED
+  Py_CLEAR(clear_module_state->__pyx_CyFunctionType);
+  #endif
+  #ifdef __Pyx_FusedFunction_USED
+  Py_CLEAR(clear_module_state->__pyx_FusedFunctionType);
+  #endif
+  Py_CLEAR(clear_module_state->__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+  Py_CLEAR(clear_module_state->__pyx_type_8pybitset_8backends_6cython_7_bitset_BitSet);
+  Py_CLEAR(clear_module_state->__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSetIter);
+  Py_CLEAR(clear_module_state->__pyx_type_8pybitset_8backends_6cython_7_bitset_BitSetIter);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSetIter___reduce_cython);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSetIter___setstate_cython);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet___reduce_cython);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet___setstate_cython);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet_clear);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet_contains_all);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet_copy);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet_count);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet_difference_count);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet_disjoint);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet_fill);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet_for_each);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet_get);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet_grow);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet_inplace_difference);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet_inplace_intersection);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet_inplace_symmetric_differe);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet_inplace_union);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet_intersect);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet_intersection_count);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet_maximum);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet_minimum);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet_print);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet_resize);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet_set);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet_set_to_value);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet_shift_left);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet_shift_right);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet_size_in_bits);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet_size_in_bytes);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet_size_in_words);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet_symmetric_difference_coun);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet_trim);
+  Py_CLEAR(clear_module_state->__pyx_n_s_BitSet_union_count);
+  Py_CLEAR(clear_module_state->__pyx_n_s_MemoryError);
+  Py_CLEAR(clear_module_state->__pyx_n_s_StopIteration);
+  Py_CLEAR(clear_module_state->__pyx_n_s_TypeError);
+  Py_CLEAR(clear_module_state->__pyx_n_s__44);
+  Py_CLEAR(clear_module_state->__pyx_n_s_asyncio_coroutines);
+  Py_CLEAR(clear_module_state->__pyx_n_s_b);
+  Py_CLEAR(clear_module_state->__pyx_n_s_b2);
+  Py_CLEAR(clear_module_state->__pyx_n_s_clear);
+  Py_CLEAR(clear_module_state->__pyx_n_s_cline_in_traceback);
+  Py_CLEAR(clear_module_state->__pyx_n_s_contains_all);
+  Py_CLEAR(clear_module_state->__pyx_n_s_copy);
+  Py_CLEAR(clear_module_state->__pyx_n_s_count);
+  Py_CLEAR(clear_module_state->__pyx_n_s_difference_count);
+  Py_CLEAR(clear_module_state->__pyx_kp_u_disable);
+  Py_CLEAR(clear_module_state->__pyx_n_s_disjoint);
+  Py_CLEAR(clear_module_state->__pyx_kp_u_enable);
+  Py_CLEAR(clear_module_state->__pyx_n_s_fill);
+  Py_CLEAR(clear_module_state->__pyx_n_s_flag);
+  Py_CLEAR(clear_module_state->__pyx_n_s_for_each);
+  Py_CLEAR(clear_module_state->__pyx_n_s_func);
+  Py_CLEAR(clear_module_state->__pyx_kp_u_gc);
+  Py_CLEAR(clear_module_state->__pyx_n_s_get);
+  Py_CLEAR(clear_module_state->__pyx_n_s_getstate);
+  Py_CLEAR(clear_module_state->__pyx_n_s_grow);
+  Py_CLEAR(clear_module_state->__pyx_n_s_i);
+  Py_CLEAR(clear_module_state->__pyx_n_s_init);
+  Py_CLEAR(clear_module_state->__pyx_n_s_inplace_difference);
+  Py_CLEAR(clear_module_state->__pyx_n_s_inplace_intersection);
+  Py_CLEAR(clear_module_state->__pyx_n_s_inplace_symmetric_difference);
+  Py_CLEAR(clear_module_state->__pyx_n_s_inplace_union);
+  Py_CLEAR(clear_module_state->__pyx_n_s_intersect);
+  Py_CLEAR(clear_module_state->__pyx_n_s_intersection_count);
+  Py_CLEAR(clear_module_state->__pyx_n_s_is_coroutine);
+  Py_CLEAR(clear_module_state->__pyx_kp_u_isenabled);
+  Py_CLEAR(clear_module_state->__pyx_n_s_main);
+  Py_CLEAR(clear_module_state->__pyx_n_s_maximum);
+  Py_CLEAR(clear_module_state->__pyx_n_s_minimum);
+  Py_CLEAR(clear_module_state->__pyx_n_s_name);
+  Py_CLEAR(clear_module_state->__pyx_n_s_newarraysize);
+  Py_CLEAR(clear_module_state->__pyx_kp_s_no_default___reduce___due_to_non);
+  Py_CLEAR(clear_module_state->__pyx_n_s_padwithzeroes);
+  Py_CLEAR(clear_module_state->__pyx_n_s_print);
+  Py_CLEAR(clear_module_state->__pyx_kp_s_pybitset_backends_cython__bitset);
+  Py_CLEAR(clear_module_state->__pyx_n_s_pybitset_backends_cython__bitset_2);
+  Py_CLEAR(clear_module_state->__pyx_n_s_pyx_state);
+  Py_CLEAR(clear_module_state->__pyx_n_s_pyx_vtable);
+  Py_CLEAR(clear_module_state->__pyx_n_s_reduce);
+  Py_CLEAR(clear_module_state->__pyx_n_s_reduce_cython);
+  Py_CLEAR(clear_module_state->__pyx_n_s_reduce_ex);
+  Py_CLEAR(clear_module_state->__pyx_n_s_resize);
+  Py_CLEAR(clear_module_state->__pyx_n_s_s);
+  Py_CLEAR(clear_module_state->__pyx_n_s_self);
+  Py_CLEAR(clear_module_state->__pyx_n_s_set);
+  Py_CLEAR(clear_module_state->__pyx_n_s_set_to_value);
+  Py_CLEAR(clear_module_state->__pyx_n_s_setstate);
+  Py_CLEAR(clear_module_state->__pyx_n_s_setstate_cython);
+  Py_CLEAR(clear_module_state->__pyx_n_s_shift_left);
+  Py_CLEAR(clear_module_state->__pyx_n_s_shift_right);
+  Py_CLEAR(clear_module_state->__pyx_n_s_size);
+  Py_CLEAR(clear_module_state->__pyx_n_s_size_in_bits);
+  Py_CLEAR(clear_module_state->__pyx_n_s_size_in_bytes);
+  Py_CLEAR(clear_module_state->__pyx_n_s_size_in_words);
+  Py_CLEAR(clear_module_state->__pyx_kp_s_stringsource);
+  Py_CLEAR(clear_module_state->__pyx_n_s_symmetric_difference_count);
+  Py_CLEAR(clear_module_state->__pyx_n_s_test);
+  Py_CLEAR(clear_module_state->__pyx_n_s_trim);
+  Py_CLEAR(clear_module_state->__pyx_n_s_union_count);
+  Py_CLEAR(clear_module_state->__pyx_tuple_);
+  Py_CLEAR(clear_module_state->__pyx_tuple__5);
+  Py_CLEAR(clear_module_state->__pyx_tuple__10);
+  Py_CLEAR(clear_module_state->__pyx_tuple__13);
+  Py_CLEAR(clear_module_state->__pyx_tuple__16);
+  Py_CLEAR(clear_module_state->__pyx_tuple__18);
+  Py_CLEAR(clear_module_state->__pyx_tuple__24);
+  Py_CLEAR(clear_module_state->__pyx_tuple__36);
+  Py_CLEAR(clear_module_state->__pyx_tuple__40);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__2);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__3);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__4);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__6);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__7);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__8);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__9);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__11);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__12);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__14);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__15);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__17);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__19);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__20);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__21);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__22);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__23);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__25);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__26);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__27);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__28);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__29);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__30);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__31);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__32);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__33);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__34);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__35);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__37);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__38);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__39);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__41);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__42);
+  Py_CLEAR(clear_module_state->__pyx_codeobj__43);
+  return 0;
+}
+#endif
+/* #### Code section: module_state_traverse ### */
+#if CYTHON_USE_MODULE_STATE
+static int __pyx_m_traverse(PyObject *m, visitproc visit, void *arg) {
+  __pyx_mstate *traverse_module_state = __pyx_mstate(m);
+  if (!traverse_module_state) return 0;
+  Py_VISIT(traverse_module_state->__pyx_d);
+  Py_VISIT(traverse_module_state->__pyx_b);
+  Py_VISIT(traverse_module_state->__pyx_cython_runtime);
+  Py_VISIT(traverse_module_state->__pyx_empty_tuple);
+  Py_VISIT(traverse_module_state->__pyx_empty_bytes);
+  Py_VISIT(traverse_module_state->__pyx_empty_unicode);
+  #ifdef __Pyx_CyFunction_USED
+  Py_VISIT(traverse_module_state->__pyx_CyFunctionType);
+  #endif
+  #ifdef __Pyx_FusedFunction_USED
+  Py_VISIT(traverse_module_state->__pyx_FusedFunctionType);
+  #endif
+  Py_VISIT(traverse_module_state->__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+  Py_VISIT(traverse_module_state->__pyx_type_8pybitset_8backends_6cython_7_bitset_BitSet);
+  Py_VISIT(traverse_module_state->__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSetIter);
+  Py_VISIT(traverse_module_state->__pyx_type_8pybitset_8backends_6cython_7_bitset_BitSetIter);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSetIter___reduce_cython);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSetIter___setstate_cython);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet___reduce_cython);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet___setstate_cython);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet_clear);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet_contains_all);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet_copy);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet_count);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet_difference_count);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet_disjoint);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet_fill);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet_for_each);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet_get);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet_grow);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet_inplace_difference);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet_inplace_intersection);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet_inplace_symmetric_differe);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet_inplace_union);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet_intersect);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet_intersection_count);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet_maximum);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet_minimum);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet_print);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet_resize);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet_set);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet_set_to_value);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet_shift_left);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet_shift_right);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet_size_in_bits);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet_size_in_bytes);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet_size_in_words);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet_symmetric_difference_coun);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet_trim);
+  Py_VISIT(traverse_module_state->__pyx_n_s_BitSet_union_count);
+  Py_VISIT(traverse_module_state->__pyx_n_s_MemoryError);
+  Py_VISIT(traverse_module_state->__pyx_n_s_StopIteration);
+  Py_VISIT(traverse_module_state->__pyx_n_s_TypeError);
+  Py_VISIT(traverse_module_state->__pyx_n_s__44);
+  Py_VISIT(traverse_module_state->__pyx_n_s_asyncio_coroutines);
+  Py_VISIT(traverse_module_state->__pyx_n_s_b);
+  Py_VISIT(traverse_module_state->__pyx_n_s_b2);
+  Py_VISIT(traverse_module_state->__pyx_n_s_clear);
+  Py_VISIT(traverse_module_state->__pyx_n_s_cline_in_traceback);
+  Py_VISIT(traverse_module_state->__pyx_n_s_contains_all);
+  Py_VISIT(traverse_module_state->__pyx_n_s_copy);
+  Py_VISIT(traverse_module_state->__pyx_n_s_count);
+  Py_VISIT(traverse_module_state->__pyx_n_s_difference_count);
+  Py_VISIT(traverse_module_state->__pyx_kp_u_disable);
+  Py_VISIT(traverse_module_state->__pyx_n_s_disjoint);
+  Py_VISIT(traverse_module_state->__pyx_kp_u_enable);
+  Py_VISIT(traverse_module_state->__pyx_n_s_fill);
+  Py_VISIT(traverse_module_state->__pyx_n_s_flag);
+  Py_VISIT(traverse_module_state->__pyx_n_s_for_each);
+  Py_VISIT(traverse_module_state->__pyx_n_s_func);
+  Py_VISIT(traverse_module_state->__pyx_kp_u_gc);
+  Py_VISIT(traverse_module_state->__pyx_n_s_get);
+  Py_VISIT(traverse_module_state->__pyx_n_s_getstate);
+  Py_VISIT(traverse_module_state->__pyx_n_s_grow);
+  Py_VISIT(traverse_module_state->__pyx_n_s_i);
+  Py_VISIT(traverse_module_state->__pyx_n_s_init);
+  Py_VISIT(traverse_module_state->__pyx_n_s_inplace_difference);
+  Py_VISIT(traverse_module_state->__pyx_n_s_inplace_intersection);
+  Py_VISIT(traverse_module_state->__pyx_n_s_inplace_symmetric_difference);
+  Py_VISIT(traverse_module_state->__pyx_n_s_inplace_union);
+  Py_VISIT(traverse_module_state->__pyx_n_s_intersect);
+  Py_VISIT(traverse_module_state->__pyx_n_s_intersection_count);
+  Py_VISIT(traverse_module_state->__pyx_n_s_is_coroutine);
+  Py_VISIT(traverse_module_state->__pyx_kp_u_isenabled);
+  Py_VISIT(traverse_module_state->__pyx_n_s_main);
+  Py_VISIT(traverse_module_state->__pyx_n_s_maximum);
+  Py_VISIT(traverse_module_state->__pyx_n_s_minimum);
+  Py_VISIT(traverse_module_state->__pyx_n_s_name);
+  Py_VISIT(traverse_module_state->__pyx_n_s_newarraysize);
+  Py_VISIT(traverse_module_state->__pyx_kp_s_no_default___reduce___due_to_non);
+  Py_VISIT(traverse_module_state->__pyx_n_s_padwithzeroes);
+  Py_VISIT(traverse_module_state->__pyx_n_s_print);
+  Py_VISIT(traverse_module_state->__pyx_kp_s_pybitset_backends_cython__bitset);
+  Py_VISIT(traverse_module_state->__pyx_n_s_pybitset_backends_cython__bitset_2);
+  Py_VISIT(traverse_module_state->__pyx_n_s_pyx_state);
+  Py_VISIT(traverse_module_state->__pyx_n_s_pyx_vtable);
+  Py_VISIT(traverse_module_state->__pyx_n_s_reduce);
+  Py_VISIT(traverse_module_state->__pyx_n_s_reduce_cython);
+  Py_VISIT(traverse_module_state->__pyx_n_s_reduce_ex);
+  Py_VISIT(traverse_module_state->__pyx_n_s_resize);
+  Py_VISIT(traverse_module_state->__pyx_n_s_s);
+  Py_VISIT(traverse_module_state->__pyx_n_s_self);
+  Py_VISIT(traverse_module_state->__pyx_n_s_set);
+  Py_VISIT(traverse_module_state->__pyx_n_s_set_to_value);
+  Py_VISIT(traverse_module_state->__pyx_n_s_setstate);
+  Py_VISIT(traverse_module_state->__pyx_n_s_setstate_cython);
+  Py_VISIT(traverse_module_state->__pyx_n_s_shift_left);
+  Py_VISIT(traverse_module_state->__pyx_n_s_shift_right);
+  Py_VISIT(traverse_module_state->__pyx_n_s_size);
+  Py_VISIT(traverse_module_state->__pyx_n_s_size_in_bits);
+  Py_VISIT(traverse_module_state->__pyx_n_s_size_in_bytes);
+  Py_VISIT(traverse_module_state->__pyx_n_s_size_in_words);
+  Py_VISIT(traverse_module_state->__pyx_kp_s_stringsource);
+  Py_VISIT(traverse_module_state->__pyx_n_s_symmetric_difference_count);
+  Py_VISIT(traverse_module_state->__pyx_n_s_test);
+  Py_VISIT(traverse_module_state->__pyx_n_s_trim);
+  Py_VISIT(traverse_module_state->__pyx_n_s_union_count);
+  Py_VISIT(traverse_module_state->__pyx_tuple_);
+  Py_VISIT(traverse_module_state->__pyx_tuple__5);
+  Py_VISIT(traverse_module_state->__pyx_tuple__10);
+  Py_VISIT(traverse_module_state->__pyx_tuple__13);
+  Py_VISIT(traverse_module_state->__pyx_tuple__16);
+  Py_VISIT(traverse_module_state->__pyx_tuple__18);
+  Py_VISIT(traverse_module_state->__pyx_tuple__24);
+  Py_VISIT(traverse_module_state->__pyx_tuple__36);
+  Py_VISIT(traverse_module_state->__pyx_tuple__40);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__2);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__3);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__4);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__6);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__7);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__8);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__9);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__11);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__12);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__14);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__15);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__17);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__19);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__20);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__21);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__22);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__23);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__25);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__26);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__27);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__28);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__29);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__30);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__31);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__32);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__33);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__34);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__35);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__37);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__38);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__39);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__41);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__42);
+  Py_VISIT(traverse_module_state->__pyx_codeobj__43);
+  return 0;
+}
+#endif
+/* #### Code section: module_state_defines ### */
+#define __pyx_d __pyx_mstate_global->__pyx_d
+#define __pyx_b __pyx_mstate_global->__pyx_b
+#define __pyx_cython_runtime __pyx_mstate_global->__pyx_cython_runtime
+#define __pyx_empty_tuple __pyx_mstate_global->__pyx_empty_tuple
+#define __pyx_empty_bytes __pyx_mstate_global->__pyx_empty_bytes
+#define __pyx_empty_unicode __pyx_mstate_global->__pyx_empty_unicode
+#ifdef __Pyx_CyFunction_USED
+#define __pyx_CyFunctionType __pyx_mstate_global->__pyx_CyFunctionType
+#endif
+#ifdef __Pyx_FusedFunction_USED
+#define __pyx_FusedFunctionType __pyx_mstate_global->__pyx_FusedFunctionType
+#endif
+#ifdef __Pyx_Generator_USED
+#define __pyx_GeneratorType __pyx_mstate_global->__pyx_GeneratorType
+#endif
+#ifdef __Pyx_IterableCoroutine_USED
+#define __pyx_IterableCoroutineType __pyx_mstate_global->__pyx_IterableCoroutineType
+#endif
+#ifdef __Pyx_Coroutine_USED
+#define __pyx_CoroutineAwaitType __pyx_mstate_global->__pyx_CoroutineAwaitType
+#endif
+#ifdef __Pyx_Coroutine_USED
+#define __pyx_CoroutineType __pyx_mstate_global->__pyx_CoroutineType
+#endif
+#if CYTHON_USE_MODULE_STATE
+#endif
+#if CYTHON_USE_MODULE_STATE
+#endif
+#if CYTHON_USE_MODULE_STATE
+#define __pyx_type_8pybitset_8backends_6cython_7_bitset_BitSet __pyx_mstate_global->__pyx_type_8pybitset_8backends_6cython_7_bitset_BitSet
+#define __pyx_type_8pybitset_8backends_6cython_7_bitset_BitSetIter __pyx_mstate_global->__pyx_type_8pybitset_8backends_6cython_7_bitset_BitSetIter
+#endif
+#define __pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet __pyx_mstate_global->__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet
+#define __pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSetIter __pyx_mstate_global->__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSetIter
+#define __pyx_n_s_BitSet __pyx_mstate_global->__pyx_n_s_BitSet
+#define __pyx_n_s_BitSetIter___reduce_cython __pyx_mstate_global->__pyx_n_s_BitSetIter___reduce_cython
+#define __pyx_n_s_BitSetIter___setstate_cython __pyx_mstate_global->__pyx_n_s_BitSetIter___setstate_cython
+#define __pyx_n_s_BitSet___reduce_cython __pyx_mstate_global->__pyx_n_s_BitSet___reduce_cython
+#define __pyx_n_s_BitSet___setstate_cython __pyx_mstate_global->__pyx_n_s_BitSet___setstate_cython
+#define __pyx_n_s_BitSet_clear __pyx_mstate_global->__pyx_n_s_BitSet_clear
+#define __pyx_n_s_BitSet_contains_all __pyx_mstate_global->__pyx_n_s_BitSet_contains_all
+#define __pyx_n_s_BitSet_copy __pyx_mstate_global->__pyx_n_s_BitSet_copy
+#define __pyx_n_s_BitSet_count __pyx_mstate_global->__pyx_n_s_BitSet_count
+#define __pyx_n_s_BitSet_difference_count __pyx_mstate_global->__pyx_n_s_BitSet_difference_count
+#define __pyx_n_s_BitSet_disjoint __pyx_mstate_global->__pyx_n_s_BitSet_disjoint
+#define __pyx_n_s_BitSet_fill __pyx_mstate_global->__pyx_n_s_BitSet_fill
+#define __pyx_n_s_BitSet_for_each __pyx_mstate_global->__pyx_n_s_BitSet_for_each
+#define __pyx_n_s_BitSet_get __pyx_mstate_global->__pyx_n_s_BitSet_get
+#define __pyx_n_s_BitSet_grow __pyx_mstate_global->__pyx_n_s_BitSet_grow
+#define __pyx_n_s_BitSet_inplace_difference __pyx_mstate_global->__pyx_n_s_BitSet_inplace_difference
+#define __pyx_n_s_BitSet_inplace_intersection __pyx_mstate_global->__pyx_n_s_BitSet_inplace_intersection
+#define __pyx_n_s_BitSet_inplace_symmetric_differe __pyx_mstate_global->__pyx_n_s_BitSet_inplace_symmetric_differe
+#define __pyx_n_s_BitSet_inplace_union __pyx_mstate_global->__pyx_n_s_BitSet_inplace_union
+#define __pyx_n_s_BitSet_intersect __pyx_mstate_global->__pyx_n_s_BitSet_intersect
+#define __pyx_n_s_BitSet_intersection_count __pyx_mstate_global->__pyx_n_s_BitSet_intersection_count
+#define __pyx_n_s_BitSet_maximum __pyx_mstate_global->__pyx_n_s_BitSet_maximum
+#define __pyx_n_s_BitSet_minimum __pyx_mstate_global->__pyx_n_s_BitSet_minimum
+#define __pyx_n_s_BitSet_print __pyx_mstate_global->__pyx_n_s_BitSet_print
+#define __pyx_n_s_BitSet_resize __pyx_mstate_global->__pyx_n_s_BitSet_resize
+#define __pyx_n_s_BitSet_set __pyx_mstate_global->__pyx_n_s_BitSet_set
+#define __pyx_n_s_BitSet_set_to_value __pyx_mstate_global->__pyx_n_s_BitSet_set_to_value
+#define __pyx_n_s_BitSet_shift_left __pyx_mstate_global->__pyx_n_s_BitSet_shift_left
+#define __pyx_n_s_BitSet_shift_right __pyx_mstate_global->__pyx_n_s_BitSet_shift_right
+#define __pyx_n_s_BitSet_size_in_bits __pyx_mstate_global->__pyx_n_s_BitSet_size_in_bits
+#define __pyx_n_s_BitSet_size_in_bytes __pyx_mstate_global->__pyx_n_s_BitSet_size_in_bytes
+#define __pyx_n_s_BitSet_size_in_words __pyx_mstate_global->__pyx_n_s_BitSet_size_in_words
+#define __pyx_n_s_BitSet_symmetric_difference_coun __pyx_mstate_global->__pyx_n_s_BitSet_symmetric_difference_coun
+#define __pyx_n_s_BitSet_trim __pyx_mstate_global->__pyx_n_s_BitSet_trim
+#define __pyx_n_s_BitSet_union_count __pyx_mstate_global->__pyx_n_s_BitSet_union_count
+#define __pyx_n_s_MemoryError __pyx_mstate_global->__pyx_n_s_MemoryError
+#define __pyx_n_s_StopIteration __pyx_mstate_global->__pyx_n_s_StopIteration
+#define __pyx_n_s_TypeError __pyx_mstate_global->__pyx_n_s_TypeError
+#define __pyx_n_s__44 __pyx_mstate_global->__pyx_n_s__44
+#define __pyx_n_s_asyncio_coroutines __pyx_mstate_global->__pyx_n_s_asyncio_coroutines
+#define __pyx_n_s_b __pyx_mstate_global->__pyx_n_s_b
+#define __pyx_n_s_b2 __pyx_mstate_global->__pyx_n_s_b2
+#define __pyx_n_s_clear __pyx_mstate_global->__pyx_n_s_clear
+#define __pyx_n_s_cline_in_traceback __pyx_mstate_global->__pyx_n_s_cline_in_traceback
+#define __pyx_n_s_contains_all __pyx_mstate_global->__pyx_n_s_contains_all
+#define __pyx_n_s_copy __pyx_mstate_global->__pyx_n_s_copy
+#define __pyx_n_s_count __pyx_mstate_global->__pyx_n_s_count
+#define __pyx_n_s_difference_count __pyx_mstate_global->__pyx_n_s_difference_count
+#define __pyx_kp_u_disable __pyx_mstate_global->__pyx_kp_u_disable
+#define __pyx_n_s_disjoint __pyx_mstate_global->__pyx_n_s_disjoint
+#define __pyx_kp_u_enable __pyx_mstate_global->__pyx_kp_u_enable
+#define __pyx_n_s_fill __pyx_mstate_global->__pyx_n_s_fill
+#define __pyx_n_s_flag __pyx_mstate_global->__pyx_n_s_flag
+#define __pyx_n_s_for_each __pyx_mstate_global->__pyx_n_s_for_each
+#define __pyx_n_s_func __pyx_mstate_global->__pyx_n_s_func
+#define __pyx_kp_u_gc __pyx_mstate_global->__pyx_kp_u_gc
+#define __pyx_n_s_get __pyx_mstate_global->__pyx_n_s_get
+#define __pyx_n_s_getstate __pyx_mstate_global->__pyx_n_s_getstate
+#define __pyx_n_s_grow __pyx_mstate_global->__pyx_n_s_grow
+#define __pyx_n_s_i __pyx_mstate_global->__pyx_n_s_i
+#define __pyx_n_s_init __pyx_mstate_global->__pyx_n_s_init
+#define __pyx_n_s_inplace_difference __pyx_mstate_global->__pyx_n_s_inplace_difference
+#define __pyx_n_s_inplace_intersection __pyx_mstate_global->__pyx_n_s_inplace_intersection
+#define __pyx_n_s_inplace_symmetric_difference __pyx_mstate_global->__pyx_n_s_inplace_symmetric_difference
+#define __pyx_n_s_inplace_union __pyx_mstate_global->__pyx_n_s_inplace_union
+#define __pyx_n_s_intersect __pyx_mstate_global->__pyx_n_s_intersect
+#define __pyx_n_s_intersection_count __pyx_mstate_global->__pyx_n_s_intersection_count
+#define __pyx_n_s_is_coroutine __pyx_mstate_global->__pyx_n_s_is_coroutine
+#define __pyx_kp_u_isenabled __pyx_mstate_global->__pyx_kp_u_isenabled
+#define __pyx_n_s_main __pyx_mstate_global->__pyx_n_s_main
+#define __pyx_n_s_maximum __pyx_mstate_global->__pyx_n_s_maximum
+#define __pyx_n_s_minimum __pyx_mstate_global->__pyx_n_s_minimum
+#define __pyx_n_s_name __pyx_mstate_global->__pyx_n_s_name
+#define __pyx_n_s_newarraysize __pyx_mstate_global->__pyx_n_s_newarraysize
+#define __pyx_kp_s_no_default___reduce___due_to_non __pyx_mstate_global->__pyx_kp_s_no_default___reduce___due_to_non
+#define __pyx_n_s_padwithzeroes __pyx_mstate_global->__pyx_n_s_padwithzeroes
+#define __pyx_n_s_print __pyx_mstate_global->__pyx_n_s_print
+#define __pyx_kp_s_pybitset_backends_cython__bitset __pyx_mstate_global->__pyx_kp_s_pybitset_backends_cython__bitset
+#define __pyx_n_s_pybitset_backends_cython__bitset_2 __pyx_mstate_global->__pyx_n_s_pybitset_backends_cython__bitset_2
+#define __pyx_n_s_pyx_state __pyx_mstate_global->__pyx_n_s_pyx_state
+#define __pyx_n_s_pyx_vtable __pyx_mstate_global->__pyx_n_s_pyx_vtable
+#define __pyx_n_s_reduce __pyx_mstate_global->__pyx_n_s_reduce
+#define __pyx_n_s_reduce_cython __pyx_mstate_global->__pyx_n_s_reduce_cython
+#define __pyx_n_s_reduce_ex __pyx_mstate_global->__pyx_n_s_reduce_ex
+#define __pyx_n_s_resize __pyx_mstate_global->__pyx_n_s_resize
+#define __pyx_n_s_s __pyx_mstate_global->__pyx_n_s_s
+#define __pyx_n_s_self __pyx_mstate_global->__pyx_n_s_self
+#define __pyx_n_s_set __pyx_mstate_global->__pyx_n_s_set
+#define __pyx_n_s_set_to_value __pyx_mstate_global->__pyx_n_s_set_to_value
+#define __pyx_n_s_setstate __pyx_mstate_global->__pyx_n_s_setstate
+#define __pyx_n_s_setstate_cython __pyx_mstate_global->__pyx_n_s_setstate_cython
+#define __pyx_n_s_shift_left __pyx_mstate_global->__pyx_n_s_shift_left
+#define __pyx_n_s_shift_right __pyx_mstate_global->__pyx_n_s_shift_right
+#define __pyx_n_s_size __pyx_mstate_global->__pyx_n_s_size
+#define __pyx_n_s_size_in_bits __pyx_mstate_global->__pyx_n_s_size_in_bits
+#define __pyx_n_s_size_in_bytes __pyx_mstate_global->__pyx_n_s_size_in_bytes
+#define __pyx_n_s_size_in_words __pyx_mstate_global->__pyx_n_s_size_in_words
+#define __pyx_kp_s_stringsource __pyx_mstate_global->__pyx_kp_s_stringsource
+#define __pyx_n_s_symmetric_difference_count __pyx_mstate_global->__pyx_n_s_symmetric_difference_count
+#define __pyx_n_s_test __pyx_mstate_global->__pyx_n_s_test
+#define __pyx_n_s_trim __pyx_mstate_global->__pyx_n_s_trim
+#define __pyx_n_s_union_count __pyx_mstate_global->__pyx_n_s_union_count
+#define __pyx_tuple_ __pyx_mstate_global->__pyx_tuple_
+#define __pyx_tuple__5 __pyx_mstate_global->__pyx_tuple__5
+#define __pyx_tuple__10 __pyx_mstate_global->__pyx_tuple__10
+#define __pyx_tuple__13 __pyx_mstate_global->__pyx_tuple__13
+#define __pyx_tuple__16 __pyx_mstate_global->__pyx_tuple__16
+#define __pyx_tuple__18 __pyx_mstate_global->__pyx_tuple__18
+#define __pyx_tuple__24 __pyx_mstate_global->__pyx_tuple__24
+#define __pyx_tuple__36 __pyx_mstate_global->__pyx_tuple__36
+#define __pyx_tuple__40 __pyx_mstate_global->__pyx_tuple__40
+#define __pyx_codeobj__2 __pyx_mstate_global->__pyx_codeobj__2
+#define __pyx_codeobj__3 __pyx_mstate_global->__pyx_codeobj__3
+#define __pyx_codeobj__4 __pyx_mstate_global->__pyx_codeobj__4
+#define __pyx_codeobj__6 __pyx_mstate_global->__pyx_codeobj__6
+#define __pyx_codeobj__7 __pyx_mstate_global->__pyx_codeobj__7
+#define __pyx_codeobj__8 __pyx_mstate_global->__pyx_codeobj__8
+#define __pyx_codeobj__9 __pyx_mstate_global->__pyx_codeobj__9
+#define __pyx_codeobj__11 __pyx_mstate_global->__pyx_codeobj__11
+#define __pyx_codeobj__12 __pyx_mstate_global->__pyx_codeobj__12
+#define __pyx_codeobj__14 __pyx_mstate_global->__pyx_codeobj__14
+#define __pyx_codeobj__15 __pyx_mstate_global->__pyx_codeobj__15
+#define __pyx_codeobj__17 __pyx_mstate_global->__pyx_codeobj__17
+#define __pyx_codeobj__19 __pyx_mstate_global->__pyx_codeobj__19
+#define __pyx_codeobj__20 __pyx_mstate_global->__pyx_codeobj__20
+#define __pyx_codeobj__21 __pyx_mstate_global->__pyx_codeobj__21
+#define __pyx_codeobj__22 __pyx_mstate_global->__pyx_codeobj__22
+#define __pyx_codeobj__23 __pyx_mstate_global->__pyx_codeobj__23
+#define __pyx_codeobj__25 __pyx_mstate_global->__pyx_codeobj__25
+#define __pyx_codeobj__26 __pyx_mstate_global->__pyx_codeobj__26
+#define __pyx_codeobj__27 __pyx_mstate_global->__pyx_codeobj__27
+#define __pyx_codeobj__28 __pyx_mstate_global->__pyx_codeobj__28
+#define __pyx_codeobj__29 __pyx_mstate_global->__pyx_codeobj__29
+#define __pyx_codeobj__30 __pyx_mstate_global->__pyx_codeobj__30
+#define __pyx_codeobj__31 __pyx_mstate_global->__pyx_codeobj__31
+#define __pyx_codeobj__32 __pyx_mstate_global->__pyx_codeobj__32
+#define __pyx_codeobj__33 __pyx_mstate_global->__pyx_codeobj__33
+#define __pyx_codeobj__34 __pyx_mstate_global->__pyx_codeobj__34
+#define __pyx_codeobj__35 __pyx_mstate_global->__pyx_codeobj__35
+#define __pyx_codeobj__37 __pyx_mstate_global->__pyx_codeobj__37
+#define __pyx_codeobj__38 __pyx_mstate_global->__pyx_codeobj__38
+#define __pyx_codeobj__39 __pyx_mstate_global->__pyx_codeobj__39
+#define __pyx_codeobj__41 __pyx_mstate_global->__pyx_codeobj__41
+#define __pyx_codeobj__42 __pyx_mstate_global->__pyx_codeobj__42
+#define __pyx_codeobj__43 __pyx_mstate_global->__pyx_codeobj__43
+/* #### Code section: module_code ### */
 
 /* "pybitset/backends/cython/_bitset.pyx":19
  * 
  * 
- * cdef bint bitset_iterator_func(size_t value, void *param) with gil:             # <<<<<<<<<<<<<<
+ * cdef bool bitset_iterator_func(size_t value, void *param) noexcept with gil:             # <<<<<<<<<<<<<<
  *     return (<object>param)(value)
  * 
  */
 
-static int __pyx_f_8pybitset_8backends_6cython_7_bitset_bitset_iterator_func(size_t __pyx_v_value, void *__pyx_v_param) {
-  int __pyx_r;
+static bool __pyx_f_8pybitset_8backends_6cython_7_bitset_bitset_iterator_func(size_t __pyx_v_value, void *__pyx_v_param) {
+  bool __pyx_r;
   __Pyx_RefNannyDeclarations
   PyObject *__pyx_t_1 = NULL;
   PyObject *__pyx_t_2 = NULL;
   PyObject *__pyx_t_3 = NULL;
   PyObject *__pyx_t_4 = NULL;
   int __pyx_t_5;
+  bool __pyx_t_6;
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   #ifdef WITH_THREAD
   PyGILState_STATE __pyx_gilstate_save = __Pyx_PyGILState_Ensure();
   #endif
   __Pyx_RefNannySetupContext("bitset_iterator_func", 0);
 
   /* "pybitset/backends/cython/_bitset.pyx":20
  * 
- * cdef bint bitset_iterator_func(size_t value, void *param) with gil:
+ * cdef bool bitset_iterator_func(size_t value, void *param) noexcept with gil:
  *     return (<object>param)(value)             # <<<<<<<<<<<<<<
  * 
  * @cython.freelist(8)
  */
   __pyx_t_2 = __Pyx_PyInt_FromSize_t(__pyx_v_value); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 20, __pyx_L1_error)
   __Pyx_GOTREF(__pyx_t_2);
   __Pyx_INCREF(((PyObject *)__pyx_v_param));
   __pyx_t_3 = ((PyObject *)__pyx_v_param); __pyx_t_4 = NULL;
+  __pyx_t_5 = 0;
   if (CYTHON_UNPACK_METHODS && unlikely(PyMethod_Check(__pyx_t_3))) {
     __pyx_t_4 = PyMethod_GET_SELF(__pyx_t_3);
     if (likely(__pyx_t_4)) {
       PyObject* function = PyMethod_GET_FUNCTION(__pyx_t_3);
       __Pyx_INCREF(__pyx_t_4);
       __Pyx_INCREF(function);
       __Pyx_DECREF_SET(__pyx_t_3, function);
+      __pyx_t_5 = 1;
     }
   }
-  __pyx_t_1 = (__pyx_t_4) ? __Pyx_PyObject_Call2Args(__pyx_t_3, __pyx_t_4, __pyx_t_2) : __Pyx_PyObject_CallOneArg(__pyx_t_3, __pyx_t_2);
-  __Pyx_XDECREF(__pyx_t_4); __pyx_t_4 = 0;
-  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
-  if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 20, __pyx_L1_error)
-  __Pyx_GOTREF(__pyx_t_1);
-  __Pyx_DECREF(__pyx_t_3); __pyx_t_3 = 0;
-  __pyx_t_5 = __Pyx_PyObject_IsTrue(__pyx_t_1); if (unlikely((__pyx_t_5 == (int)-1) && PyErr_Occurred())) __PYX_ERR(0, 20, __pyx_L1_error)
+  {
+    PyObject *__pyx_callargs[2] = {__pyx_t_4, __pyx_t_2};
+    __pyx_t_1 = __Pyx_PyObject_FastCall(__pyx_t_3, __pyx_callargs+1-__pyx_t_5, 1+__pyx_t_5);
+    __Pyx_XDECREF(__pyx_t_4); __pyx_t_4 = 0;
+    __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+    if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 20, __pyx_L1_error)
+    __Pyx_GOTREF(__pyx_t_1);
+    __Pyx_DECREF(__pyx_t_3); __pyx_t_3 = 0;
+  }
+  __pyx_t_6 = __Pyx_PyInt_As_bool(__pyx_t_1); if (unlikely((__pyx_t_6 == ((bool)-1)) && PyErr_Occurred())) __PYX_ERR(0, 20, __pyx_L1_error)
   __Pyx_DECREF(__pyx_t_1); __pyx_t_1 = 0;
-  __pyx_r = __pyx_t_5;
+  __pyx_r = __pyx_t_6;
   goto __pyx_L0;
 
   /* "pybitset/backends/cython/_bitset.pyx":19
  * 
  * 
- * cdef bint bitset_iterator_func(size_t value, void *param) with gil:             # <<<<<<<<<<<<<<
+ * cdef bool bitset_iterator_func(size_t value, void *param) noexcept with gil:             # <<<<<<<<<<<<<<
  *     return (<object>param)(value)
  * 
  */
 
   /* function exit code */
   __pyx_L1_error:;
   __Pyx_XDECREF(__pyx_t_1);
@@ -1634,56 +3049,60 @@
  */
 
 /* Python wrapper */
 static int __pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_1__cinit__(PyObject *__pyx_v_self, PyObject *__pyx_args, PyObject *__pyx_kwds); /*proto*/
 static int __pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_1__cinit__(PyObject *__pyx_v_self, PyObject *__pyx_args, PyObject *__pyx_kwds) {
   size_t __pyx_v_size;
   int __pyx_v__init;
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_VARARGS(__pyx_args, __pyx_nargs);
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   int __pyx_r;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("__cinit__ (wrapper)", 0);
   {
-    static PyObject **__pyx_pyargnames[] = {&__pyx_n_s_size,&__pyx_n_s_init,0};
+    PyObject **__pyx_pyargnames[] = {&__pyx_n_s_size,&__pyx_n_s_init,0};
     PyObject* values[2] = {0,0};
-    if (unlikely(__pyx_kwds)) {
+    if (__pyx_kwds) {
       Py_ssize_t kw_args;
-      const Py_ssize_t pos_args = PyTuple_GET_SIZE(__pyx_args);
-      switch (pos_args) {
-        case  2: values[1] = PyTuple_GET_ITEM(__pyx_args, 1);
+      switch (__pyx_nargs) {
+        case  2: values[1] = __Pyx_Arg_VARARGS(__pyx_args, 1);
         CYTHON_FALLTHROUGH;
-        case  1: values[0] = PyTuple_GET_ITEM(__pyx_args, 0);
+        case  1: values[0] = __Pyx_Arg_VARARGS(__pyx_args, 0);
         CYTHON_FALLTHROUGH;
         case  0: break;
         default: goto __pyx_L5_argtuple_error;
       }
-      kw_args = PyDict_Size(__pyx_kwds);
-      switch (pos_args) {
+      kw_args = __Pyx_NumKwargs_VARARGS(__pyx_kwds);
+      switch (__pyx_nargs) {
         case  0:
         if (kw_args > 0) {
-          PyObject* value = __Pyx_PyDict_GetItemStr(__pyx_kwds, __pyx_n_s_size);
+          PyObject* value = __Pyx_GetKwValue_VARARGS(__pyx_kwds, __pyx_kwvalues, __pyx_n_s_size);
           if (value) { values[0] = value; kw_args--; }
+          else if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 27, __pyx_L3_error)
         }
         CYTHON_FALLTHROUGH;
         case  1:
         if (kw_args > 0) {
-          PyObject* value = __Pyx_PyDict_GetItemStr(__pyx_kwds, __pyx_n_s_init);
+          PyObject* value = __Pyx_GetKwValue_VARARGS(__pyx_kwds, __pyx_kwvalues, __pyx_n_s_init);
           if (value) { values[1] = value; kw_args--; }
+          else if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 27, __pyx_L3_error)
         }
       }
       if (unlikely(kw_args > 0)) {
-        if (unlikely(__Pyx_ParseOptionalKeywords(__pyx_kwds, __pyx_pyargnames, 0, values, pos_args, "__cinit__") < 0)) __PYX_ERR(0, 27, __pyx_L3_error)
+        const Py_ssize_t kwd_pos_args = __pyx_nargs;
+        if (unlikely(__Pyx_ParseOptionalKeywords(__pyx_kwds, __pyx_kwvalues, __pyx_pyargnames, 0, values + 0, kwd_pos_args, "__cinit__") < 0)) __PYX_ERR(0, 27, __pyx_L3_error)
       }
     } else {
-      switch (PyTuple_GET_SIZE(__pyx_args)) {
-        case  2: values[1] = PyTuple_GET_ITEM(__pyx_args, 1);
+      switch (__pyx_nargs) {
+        case  2: values[1] = __Pyx_Arg_VARARGS(__pyx_args, 1);
         CYTHON_FALLTHROUGH;
-        case  1: values[0] = PyTuple_GET_ITEM(__pyx_args, 0);
+        case  1: values[0] = __Pyx_Arg_VARARGS(__pyx_args, 0);
         CYTHON_FALLTHROUGH;
         case  0: break;
         default: goto __pyx_L5_argtuple_error;
       }
     }
     if (values[0]) {
       __pyx_v_size = __Pyx_PyInt_As_size_t(values[0]); if (unlikely((__pyx_v_size == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 27, __pyx_L3_error)
@@ -1694,15 +3113,15 @@
       __pyx_v__init = __Pyx_PyObject_IsTrue(values[1]); if (unlikely((__pyx_v__init == (int)-1) && PyErr_Occurred())) __PYX_ERR(0, 27, __pyx_L3_error)
     } else {
       __pyx_v__init = ((int)1);
     }
   }
   goto __pyx_L4_argument_unpacking_done;
   __pyx_L5_argtuple_error:;
-  __Pyx_RaiseArgtupleInvalid("__cinit__", 0, 0, 2, PyTuple_GET_SIZE(__pyx_args)); __PYX_ERR(0, 27, __pyx_L3_error)
+  __Pyx_RaiseArgtupleInvalid("__cinit__", 0, 0, 2, __pyx_nargs); __PYX_ERR(0, 27, __pyx_L3_error)
   __pyx_L3_error:;
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.__cinit__", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __Pyx_RefNannyFinishContext();
   return -1;
   __pyx_L4_argument_unpacking_done:;
   __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet___cinit__(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), __pyx_v_size, __pyx_v__init);
 
@@ -1723,25 +3142,24 @@
   /* "pybitset/backends/cython/_bitset.pyx":28
  *     cdef bitset_t * _bitset
  *     def __cinit__(self, size_t size=0, bint _init = True):
  *         if _init:             # <<<<<<<<<<<<<<
  *             if size == 0:
  *                 self._bitset = bitset_create()
  */
-  __pyx_t_1 = (__pyx_v__init != 0);
-  if (__pyx_t_1) {
+  if (__pyx_v__init) {
 
     /* "pybitset/backends/cython/_bitset.pyx":29
  *     def __cinit__(self, size_t size=0, bint _init = True):
  *         if _init:
  *             if size == 0:             # <<<<<<<<<<<<<<
  *                 self._bitset = bitset_create()
  *             else:
  */
-    __pyx_t_1 = ((__pyx_v_size == 0) != 0);
+    __pyx_t_1 = (__pyx_v_size == 0);
     if (__pyx_t_1) {
 
       /* "pybitset/backends/cython/_bitset.pyx":30
  *         if _init:
  *             if size == 0:
  *                 self._bitset = bitset_create()             # <<<<<<<<<<<<<<
  *             else:
@@ -1774,15 +3192,15 @@
     /* "pybitset/backends/cython/_bitset.pyx":33
  *             else:
  *                 self._bitset = bitset_create_with_capacity(size)
  *             if not self._bitset:             # <<<<<<<<<<<<<<
  *                 raise MemoryError
  *         else:
  */
-    __pyx_t_1 = ((!(__pyx_v_self->_bitset != 0)) != 0);
+    __pyx_t_1 = (!(__pyx_v_self->_bitset != 0));
     if (unlikely(__pyx_t_1)) {
 
       /* "pybitset/backends/cython/_bitset.pyx":34
  *                 self._bitset = bitset_create_with_capacity(size)
  *             if not self._bitset:
  *                 raise MemoryError             # <<<<<<<<<<<<<<
  *         else:
@@ -1847,14 +3265,15 @@
  *         if self._bitset:
  *             bitset_free(self._bitset)
  */
 
 /* Python wrapper */
 static void __pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_3__dealloc__(PyObject *__pyx_v_self); /*proto*/
 static void __pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_3__dealloc__(PyObject *__pyx_v_self) {
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_VARARGS(__pyx_args, __pyx_nargs);
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("__dealloc__ (wrapper)", 0);
   __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_2__dealloc__(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self));
 
   /* function exit code */
   __Pyx_RefNannyFinishContext();
 }
@@ -1960,16 +3379,16 @@
   /* "pybitset/backends/cython/_bitset.pyx":47
  *         cdef BitSet self = BitSet(_init=False)
  *         self._bitset = ptr
  *         return self             # <<<<<<<<<<<<<<
  * 
  *     cpdef inline clear(self):
  */
-  __Pyx_XDECREF(((PyObject *)__pyx_r));
-  __Pyx_INCREF(((PyObject *)__pyx_v_self));
+  __Pyx_XDECREF((PyObject *)__pyx_r);
+  __Pyx_INCREF((PyObject *)__pyx_v_self);
   __pyx_r = __pyx_v_self;
   goto __pyx_L0;
 
   /* "pybitset/backends/cython/_bitset.pyx":44
  * 
  *     @staticmethod
  *     cdef inline BitSet from_ptr(bitset_t * ptr):             # <<<<<<<<<<<<<<
@@ -1994,15 +3413,21 @@
  *         return self
  * 
  *     cpdef inline clear(self):             # <<<<<<<<<<<<<<
  *         with nogil:
  *             bitset_clear(self._bitset)
  */
 
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_5clear(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused); /*proto*/
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_5clear(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
 static CYTHON_INLINE PyObject *__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_clear(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, CYTHON_UNUSED int __pyx_skip_dispatch) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("clear", 0);
 
   /* "pybitset/backends/cython/_bitset.pyx":50
  * 
@@ -2010,14 +3435,15 @@
  *         with nogil:             # <<<<<<<<<<<<<<
  *             bitset_clear(self._bitset)
  * 
  */
   {
       #ifdef WITH_THREAD
       PyThreadState *_save;
+      _save = NULL;
       Py_UNBLOCK_THREADS
       __Pyx_FastGIL_Remember();
       #endif
       /*try:*/ {
 
         /* "pybitset/backends/cython/_bitset.pyx":51
  *     cpdef inline clear(self):
@@ -2060,20 +3486,40 @@
   __pyx_r = Py_None; __Pyx_INCREF(Py_None);
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_5clear(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_4clear[] = "BitSet.clear(self)";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_5clear(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_5clear(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_4clear, "BitSet.clear(self)");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_5clear = {"clear", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_5clear, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_4clear};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_5clear(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("clear (wrapper)", 0);
+  if (unlikely(__pyx_nargs > 0)) {
+    __Pyx_RaiseArgtupleInvalid("clear", 1, 0, 0, __pyx_nargs); return NULL;}
+  if (unlikely(__pyx_kwds) && __Pyx_NumKwargs_FASTCALL(__pyx_kwds) && unlikely(!__Pyx_CheckKeywordStrings(__pyx_kwds, "clear", 0))) return NULL;
   __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_4clear(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self));
 
   /* function exit code */
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
@@ -2107,15 +3553,21 @@
  *             bitset_clear(self._bitset)
  * 
  *     cpdef inline fill(self):             # <<<<<<<<<<<<<<
  *         with nogil:
  *             bitset_fill(self._bitset)
  */
 
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_7fill(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused); /*proto*/
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_7fill(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
 static CYTHON_INLINE PyObject *__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_fill(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, CYTHON_UNUSED int __pyx_skip_dispatch) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("fill", 0);
 
   /* "pybitset/backends/cython/_bitset.pyx":54
  * 
@@ -2123,14 +3575,15 @@
  *         with nogil:             # <<<<<<<<<<<<<<
  *             bitset_fill(self._bitset)
  * 
  */
   {
       #ifdef WITH_THREAD
       PyThreadState *_save;
+      _save = NULL;
       Py_UNBLOCK_THREADS
       __Pyx_FastGIL_Remember();
       #endif
       /*try:*/ {
 
         /* "pybitset/backends/cython/_bitset.pyx":55
  *     cpdef inline fill(self):
@@ -2173,20 +3626,40 @@
   __pyx_r = Py_None; __Pyx_INCREF(Py_None);
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_7fill(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_6fill[] = "BitSet.fill(self)";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_7fill(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_7fill(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_6fill, "BitSet.fill(self)");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_7fill = {"fill", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_7fill, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_6fill};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_7fill(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("fill (wrapper)", 0);
+  if (unlikely(__pyx_nargs > 0)) {
+    __Pyx_RaiseArgtupleInvalid("fill", 1, 0, 0, __pyx_nargs); return NULL;}
+  if (unlikely(__pyx_kwds) && __Pyx_NumKwargs_FASTCALL(__pyx_kwds) && unlikely(!__Pyx_CheckKeywordStrings(__pyx_kwds, "fill", 0))) return NULL;
   __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_6fill(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self));
 
   /* function exit code */
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
@@ -2220,15 +3693,21 @@
  *             bitset_fill(self._bitset)
  * 
  *     cpdef inline BitSet copy(self):             # <<<<<<<<<<<<<<
  *         cdef bitset_t *ret
  *         with nogil:
  */
 
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_9copy(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused); /*proto*/
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_9copy(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
 static CYTHON_INLINE struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_copy(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, CYTHON_UNUSED int __pyx_skip_dispatch) {
   bitset_t *__pyx_v_ret;
   struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
   PyObject *__pyx_t_1 = NULL;
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
@@ -2241,14 +3720,15 @@
  *         with nogil:             # <<<<<<<<<<<<<<
  *             ret = bitset_copy(self._bitset)
  *         return BitSet.from_ptr(ret)
  */
   {
       #ifdef WITH_THREAD
       PyThreadState *_save;
+      _save = NULL;
       Py_UNBLOCK_THREADS
       __Pyx_FastGIL_Remember();
       #endif
       /*try:*/ {
 
         /* "pybitset/backends/cython/_bitset.pyx":60
  *         cdef bitset_t *ret
@@ -2282,15 +3762,15 @@
   /* "pybitset/backends/cython/_bitset.pyx":61
  *         with nogil:
  *             ret = bitset_copy(self._bitset)
  *         return BitSet.from_ptr(ret)             # <<<<<<<<<<<<<<
  * 
  *     cpdef inline bint resize(self, size_t newarraysize, bint padwithzeroes):
  */
-  __Pyx_XDECREF(((PyObject *)__pyx_r));
+  __Pyx_XDECREF((PyObject *)__pyx_r);
   __pyx_t_1 = ((PyObject *)__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_from_ptr(__pyx_v_ret)); if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 61, __pyx_L1_error)
   __Pyx_GOTREF(__pyx_t_1);
   __pyx_r = ((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_t_1);
   __pyx_t_1 = 0;
   goto __pyx_L0;
 
   /* "pybitset/backends/cython/_bitset.pyx":57
@@ -2309,20 +3789,40 @@
   __pyx_L0:;
   __Pyx_XGIVEREF((PyObject *)__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_9copy(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_8copy[] = "BitSet.copy(self) -> BitSet";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_9copy(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_9copy(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_8copy, "BitSet.copy(self) -> BitSet");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_9copy = {"copy", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_9copy, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_8copy};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_9copy(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("copy (wrapper)", 0);
+  if (unlikely(__pyx_nargs > 0)) {
+    __Pyx_RaiseArgtupleInvalid("copy", 1, 0, 0, __pyx_nargs); return NULL;}
+  if (unlikely(__pyx_kwds) && __Pyx_NumKwargs_FASTCALL(__pyx_kwds) && unlikely(!__Pyx_CheckKeywordStrings(__pyx_kwds, "copy", 0))) return NULL;
   __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_8copy(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self));
 
   /* function exit code */
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
@@ -2356,15 +3856,21 @@
  *         return BitSet.from_ptr(ret)
  * 
  *     cpdef inline bint resize(self, size_t newarraysize, bint padwithzeroes):             # <<<<<<<<<<<<<<
  *         cdef bint ret
  *         with nogil:
  */
 
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_11resize(PyObject *__pyx_v_self, PyObject *__pyx_args, PyObject *__pyx_kwds); /*proto*/
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_11resize(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
 static CYTHON_INLINE int __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_resize(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, size_t __pyx_v_newarraysize, int __pyx_v_padwithzeroes, CYTHON_UNUSED int __pyx_skip_dispatch) {
   int __pyx_v_ret;
   int __pyx_r;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("resize", 0);
 
   /* "pybitset/backends/cython/_bitset.pyx":65
@@ -2373,14 +3879,15 @@
  *         with nogil:             # <<<<<<<<<<<<<<
  *             ret = bitset_resize(self._bitset,  newarraysize, padwithzeroes)
  *         return ret
  */
   {
       #ifdef WITH_THREAD
       PyThreadState *_save;
+      _save = NULL;
       Py_UNBLOCK_THREADS
       __Pyx_FastGIL_Remember();
       #endif
       /*try:*/ {
 
         /* "pybitset/backends/cython/_bitset.pyx":66
  *         cdef bint ret
@@ -2432,66 +3939,85 @@
   /* function exit code */
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_11resize(PyObject *__pyx_v_self, PyObject *__pyx_args, PyObject *__pyx_kwds); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_10resize[] = "BitSet.resize(self, size_t newarraysize, bool padwithzeroes) -> bool";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_11resize(PyObject *__pyx_v_self, PyObject *__pyx_args, PyObject *__pyx_kwds) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_11resize(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_10resize, "BitSet.resize(self, size_t newarraysize, bool padwithzeroes) -> bool");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_11resize = {"resize", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_11resize, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_10resize};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_11resize(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
   size_t __pyx_v_newarraysize;
   int __pyx_v_padwithzeroes;
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("resize (wrapper)", 0);
   {
-    static PyObject **__pyx_pyargnames[] = {&__pyx_n_s_newarraysize,&__pyx_n_s_padwithzeroes,0};
+    PyObject **__pyx_pyargnames[] = {&__pyx_n_s_newarraysize,&__pyx_n_s_padwithzeroes,0};
     PyObject* values[2] = {0,0};
-    if (unlikely(__pyx_kwds)) {
+    if (__pyx_kwds) {
       Py_ssize_t kw_args;
-      const Py_ssize_t pos_args = PyTuple_GET_SIZE(__pyx_args);
-      switch (pos_args) {
-        case  2: values[1] = PyTuple_GET_ITEM(__pyx_args, 1);
+      switch (__pyx_nargs) {
+        case  2: values[1] = __Pyx_Arg_FASTCALL(__pyx_args, 1);
         CYTHON_FALLTHROUGH;
-        case  1: values[0] = PyTuple_GET_ITEM(__pyx_args, 0);
+        case  1: values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
         CYTHON_FALLTHROUGH;
         case  0: break;
         default: goto __pyx_L5_argtuple_error;
       }
-      kw_args = PyDict_Size(__pyx_kwds);
-      switch (pos_args) {
+      kw_args = __Pyx_NumKwargs_FASTCALL(__pyx_kwds);
+      switch (__pyx_nargs) {
         case  0:
-        if (likely((values[0] = __Pyx_PyDict_GetItemStr(__pyx_kwds, __pyx_n_s_newarraysize)) != 0)) kw_args--;
+        if (likely((values[0] = __Pyx_GetKwValue_FASTCALL(__pyx_kwds, __pyx_kwvalues, __pyx_n_s_newarraysize)) != 0)) kw_args--;
+        else if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 63, __pyx_L3_error)
         else goto __pyx_L5_argtuple_error;
         CYTHON_FALLTHROUGH;
         case  1:
-        if (likely((values[1] = __Pyx_PyDict_GetItemStr(__pyx_kwds, __pyx_n_s_padwithzeroes)) != 0)) kw_args--;
+        if (likely((values[1] = __Pyx_GetKwValue_FASTCALL(__pyx_kwds, __pyx_kwvalues, __pyx_n_s_padwithzeroes)) != 0)) kw_args--;
+        else if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 63, __pyx_L3_error)
         else {
           __Pyx_RaiseArgtupleInvalid("resize", 1, 2, 2, 1); __PYX_ERR(0, 63, __pyx_L3_error)
         }
       }
       if (unlikely(kw_args > 0)) {
-        if (unlikely(__Pyx_ParseOptionalKeywords(__pyx_kwds, __pyx_pyargnames, 0, values, pos_args, "resize") < 0)) __PYX_ERR(0, 63, __pyx_L3_error)
+        const Py_ssize_t kwd_pos_args = __pyx_nargs;
+        if (unlikely(__Pyx_ParseOptionalKeywords(__pyx_kwds, __pyx_kwvalues, __pyx_pyargnames, 0, values + 0, kwd_pos_args, "resize") < 0)) __PYX_ERR(0, 63, __pyx_L3_error)
       }
-    } else if (PyTuple_GET_SIZE(__pyx_args) != 2) {
+    } else if (unlikely(__pyx_nargs != 2)) {
       goto __pyx_L5_argtuple_error;
     } else {
-      values[0] = PyTuple_GET_ITEM(__pyx_args, 0);
-      values[1] = PyTuple_GET_ITEM(__pyx_args, 1);
+      values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+      values[1] = __Pyx_Arg_FASTCALL(__pyx_args, 1);
     }
     __pyx_v_newarraysize = __Pyx_PyInt_As_size_t(values[0]); if (unlikely((__pyx_v_newarraysize == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 63, __pyx_L3_error)
     __pyx_v_padwithzeroes = __Pyx_PyObject_IsTrue(values[1]); if (unlikely((__pyx_v_padwithzeroes == (int)-1) && PyErr_Occurred())) __PYX_ERR(0, 63, __pyx_L3_error)
   }
   goto __pyx_L4_argument_unpacking_done;
   __pyx_L5_argtuple_error:;
-  __Pyx_RaiseArgtupleInvalid("resize", 1, 2, 2, PyTuple_GET_SIZE(__pyx_args)); __PYX_ERR(0, 63, __pyx_L3_error)
+  __Pyx_RaiseArgtupleInvalid("resize", 1, 2, 2, __pyx_nargs); __PYX_ERR(0, 63, __pyx_L3_error)
   __pyx_L3_error:;
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.resize", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __Pyx_RefNannyFinishContext();
   return NULL;
   __pyx_L4_argument_unpacking_done:;
   __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_10resize(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), __pyx_v_newarraysize, __pyx_v_padwithzeroes);
 
@@ -2499,29 +4025,31 @@
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_10resize(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, size_t __pyx_v_newarraysize, int __pyx_v_padwithzeroes) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
-  PyObject *__pyx_t_1 = NULL;
+  int __pyx_t_1;
+  PyObject *__pyx_t_2 = NULL;
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   __Pyx_RefNannySetupContext("resize", 0);
   __Pyx_XDECREF(__pyx_r);
-  __pyx_t_1 = __Pyx_PyBool_FromLong(__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_resize(__pyx_v_self, __pyx_v_newarraysize, __pyx_v_padwithzeroes, 1)); if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 63, __pyx_L1_error)
-  __Pyx_GOTREF(__pyx_t_1);
-  __pyx_r = __pyx_t_1;
-  __pyx_t_1 = 0;
+  __pyx_t_1 = __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_resize(__pyx_v_self, __pyx_v_newarraysize, __pyx_v_padwithzeroes, 1); if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 63, __pyx_L1_error)
+  __pyx_t_2 = __Pyx_PyBool_FromLong(__pyx_t_1); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 63, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  __pyx_r = __pyx_t_2;
+  __pyx_t_2 = 0;
   goto __pyx_L0;
 
   /* function exit code */
   __pyx_L1_error:;
-  __Pyx_XDECREF(__pyx_t_1);
+  __Pyx_XDECREF(__pyx_t_2);
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.resize", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
@@ -2530,15 +4058,21 @@
  *         return ret
  * 
  *     cpdef inline size_t size_in_bytes(self):             # <<<<<<<<<<<<<<
  *         cdef size_t ret
  *         with nogil:
  */
 
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_13size_in_bytes(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused); /*proto*/
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_13size_in_bytes(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
 static CYTHON_INLINE size_t __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_size_in_bytes(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, CYTHON_UNUSED int __pyx_skip_dispatch) {
   size_t __pyx_v_ret;
   size_t __pyx_r;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("size_in_bytes", 0);
 
   /* "pybitset/backends/cython/_bitset.pyx":71
@@ -2547,14 +4081,15 @@
  *         with nogil:             # <<<<<<<<<<<<<<
  *             ret = bitset_size_in_bytes(self._bitset)
  *         return ret
  */
   {
       #ifdef WITH_THREAD
       PyThreadState *_save;
+      _save = NULL;
       Py_UNBLOCK_THREADS
       __Pyx_FastGIL_Remember();
       #endif
       /*try:*/ {
 
         /* "pybitset/backends/cython/_bitset.pyx":72
  *         cdef size_t ret
@@ -2606,45 +4141,67 @@
   /* function exit code */
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_13size_in_bytes(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_12size_in_bytes[] = "BitSet.size_in_bytes(self) -> size_t";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_13size_in_bytes(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_13size_in_bytes(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_12size_in_bytes, "BitSet.size_in_bytes(self) -> size_t");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_13size_in_bytes = {"size_in_bytes", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_13size_in_bytes, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_12size_in_bytes};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_13size_in_bytes(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("size_in_bytes (wrapper)", 0);
+  if (unlikely(__pyx_nargs > 0)) {
+    __Pyx_RaiseArgtupleInvalid("size_in_bytes", 1, 0, 0, __pyx_nargs); return NULL;}
+  if (unlikely(__pyx_kwds) && __Pyx_NumKwargs_FASTCALL(__pyx_kwds) && unlikely(!__Pyx_CheckKeywordStrings(__pyx_kwds, "size_in_bytes", 0))) return NULL;
   __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_12size_in_bytes(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self));
 
   /* function exit code */
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_12size_in_bytes(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
-  PyObject *__pyx_t_1 = NULL;
+  size_t __pyx_t_1;
+  PyObject *__pyx_t_2 = NULL;
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   __Pyx_RefNannySetupContext("size_in_bytes", 0);
   __Pyx_XDECREF(__pyx_r);
-  __pyx_t_1 = __Pyx_PyInt_FromSize_t(__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_size_in_bytes(__pyx_v_self, 1)); if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 69, __pyx_L1_error)
-  __Pyx_GOTREF(__pyx_t_1);
-  __pyx_r = __pyx_t_1;
-  __pyx_t_1 = 0;
+  __pyx_t_1 = __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_size_in_bytes(__pyx_v_self, 1); if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 69, __pyx_L1_error)
+  __pyx_t_2 = __Pyx_PyInt_FromSize_t(__pyx_t_1); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 69, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  __pyx_r = __pyx_t_2;
+  __pyx_t_2 = 0;
   goto __pyx_L0;
 
   /* function exit code */
   __pyx_L1_error:;
-  __Pyx_XDECREF(__pyx_t_1);
+  __Pyx_XDECREF(__pyx_t_2);
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.size_in_bytes", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
@@ -2653,15 +4210,21 @@
  *         return ret
  * 
  *     cpdef inline size_t size_in_bits(self):             # <<<<<<<<<<<<<<
  *         cdef size_t ret
  *         with nogil:
  */
 
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_15size_in_bits(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused); /*proto*/
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_15size_in_bits(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
 static CYTHON_INLINE size_t __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_size_in_bits(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, CYTHON_UNUSED int __pyx_skip_dispatch) {
   size_t __pyx_v_ret;
   size_t __pyx_r;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("size_in_bits", 0);
 
   /* "pybitset/backends/cython/_bitset.pyx":77
@@ -2670,14 +4233,15 @@
  *         with nogil:             # <<<<<<<<<<<<<<
  *             ret = bitset_size_in_bits(self._bitset)
  *         return ret
  */
   {
       #ifdef WITH_THREAD
       PyThreadState *_save;
+      _save = NULL;
       Py_UNBLOCK_THREADS
       __Pyx_FastGIL_Remember();
       #endif
       /*try:*/ {
 
         /* "pybitset/backends/cython/_bitset.pyx":78
  *         cdef size_t ret
@@ -2729,45 +4293,67 @@
   /* function exit code */
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_15size_in_bits(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_14size_in_bits[] = "BitSet.size_in_bits(self) -> size_t";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_15size_in_bits(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_15size_in_bits(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_14size_in_bits, "BitSet.size_in_bits(self) -> size_t");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_15size_in_bits = {"size_in_bits", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_15size_in_bits, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_14size_in_bits};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_15size_in_bits(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("size_in_bits (wrapper)", 0);
+  if (unlikely(__pyx_nargs > 0)) {
+    __Pyx_RaiseArgtupleInvalid("size_in_bits", 1, 0, 0, __pyx_nargs); return NULL;}
+  if (unlikely(__pyx_kwds) && __Pyx_NumKwargs_FASTCALL(__pyx_kwds) && unlikely(!__Pyx_CheckKeywordStrings(__pyx_kwds, "size_in_bits", 0))) return NULL;
   __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_14size_in_bits(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self));
 
   /* function exit code */
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_14size_in_bits(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
-  PyObject *__pyx_t_1 = NULL;
+  size_t __pyx_t_1;
+  PyObject *__pyx_t_2 = NULL;
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   __Pyx_RefNannySetupContext("size_in_bits", 0);
   __Pyx_XDECREF(__pyx_r);
-  __pyx_t_1 = __Pyx_PyInt_FromSize_t(__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_size_in_bits(__pyx_v_self, 1)); if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 75, __pyx_L1_error)
-  __Pyx_GOTREF(__pyx_t_1);
-  __pyx_r = __pyx_t_1;
-  __pyx_t_1 = 0;
+  __pyx_t_1 = __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_size_in_bits(__pyx_v_self, 1); if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 75, __pyx_L1_error)
+  __pyx_t_2 = __Pyx_PyInt_FromSize_t(__pyx_t_1); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 75, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  __pyx_r = __pyx_t_2;
+  __pyx_t_2 = 0;
   goto __pyx_L0;
 
   /* function exit code */
   __pyx_L1_error:;
-  __Pyx_XDECREF(__pyx_t_1);
+  __Pyx_XDECREF(__pyx_t_2);
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.size_in_bits", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
@@ -2776,15 +4362,21 @@
  *         return ret
  * 
  *     cpdef inline size_t size_in_words(self):             # <<<<<<<<<<<<<<
  *         cdef size_t ret
  *         with nogil:
  */
 
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_17size_in_words(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused); /*proto*/
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_17size_in_words(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
 static CYTHON_INLINE size_t __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_size_in_words(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, CYTHON_UNUSED int __pyx_skip_dispatch) {
   size_t __pyx_v_ret;
   size_t __pyx_r;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("size_in_words", 0);
 
   /* "pybitset/backends/cython/_bitset.pyx":83
@@ -2793,14 +4385,15 @@
  *         with nogil:             # <<<<<<<<<<<<<<
  *             ret = bitset_size_in_words(self._bitset)
  *         return ret
  */
   {
       #ifdef WITH_THREAD
       PyThreadState *_save;
+      _save = NULL;
       Py_UNBLOCK_THREADS
       __Pyx_FastGIL_Remember();
       #endif
       /*try:*/ {
 
         /* "pybitset/backends/cython/_bitset.pyx":84
  *         cdef size_t ret
@@ -2852,45 +4445,67 @@
   /* function exit code */
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_17size_in_words(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_16size_in_words[] = "BitSet.size_in_words(self) -> size_t";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_17size_in_words(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_17size_in_words(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_16size_in_words, "BitSet.size_in_words(self) -> size_t");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_17size_in_words = {"size_in_words", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_17size_in_words, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_16size_in_words};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_17size_in_words(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("size_in_words (wrapper)", 0);
+  if (unlikely(__pyx_nargs > 0)) {
+    __Pyx_RaiseArgtupleInvalid("size_in_words", 1, 0, 0, __pyx_nargs); return NULL;}
+  if (unlikely(__pyx_kwds) && __Pyx_NumKwargs_FASTCALL(__pyx_kwds) && unlikely(!__Pyx_CheckKeywordStrings(__pyx_kwds, "size_in_words", 0))) return NULL;
   __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_16size_in_words(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self));
 
   /* function exit code */
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_16size_in_words(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
-  PyObject *__pyx_t_1 = NULL;
+  size_t __pyx_t_1;
+  PyObject *__pyx_t_2 = NULL;
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   __Pyx_RefNannySetupContext("size_in_words", 0);
   __Pyx_XDECREF(__pyx_r);
-  __pyx_t_1 = __Pyx_PyInt_FromSize_t(__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_size_in_words(__pyx_v_self, 1)); if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 81, __pyx_L1_error)
-  __Pyx_GOTREF(__pyx_t_1);
-  __pyx_r = __pyx_t_1;
-  __pyx_t_1 = 0;
+  __pyx_t_1 = __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_size_in_words(__pyx_v_self, 1); if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 81, __pyx_L1_error)
+  __pyx_t_2 = __Pyx_PyInt_FromSize_t(__pyx_t_1); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 81, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  __pyx_r = __pyx_t_2;
+  __pyx_t_2 = 0;
   goto __pyx_L0;
 
   /* function exit code */
   __pyx_L1_error:;
-  __Pyx_XDECREF(__pyx_t_1);
+  __Pyx_XDECREF(__pyx_t_2);
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.size_in_words", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
@@ -2899,15 +4514,21 @@
  *         return ret
  * 
  *     cpdef inline bint grow(self, size_t newarraysize):             # <<<<<<<<<<<<<<
  *         cdef bint ret
  *         with nogil:
  */
 
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_19grow(PyObject *__pyx_v_self, PyObject *__pyx_arg_newarraysize); /*proto*/
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_19grow(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
 static CYTHON_INLINE int __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_grow(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, size_t __pyx_v_newarraysize, CYTHON_UNUSED int __pyx_skip_dispatch) {
   int __pyx_v_ret;
   int __pyx_r;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("grow", 0);
 
   /* "pybitset/backends/cython/_bitset.pyx":89
@@ -2916,14 +4537,15 @@
  *         with nogil:             # <<<<<<<<<<<<<<
  *             ret = bitset_grow(self._bitset, newarraysize)
  *         return ret
  */
   {
       #ifdef WITH_THREAD
       PyThreadState *_save;
+      _save = NULL;
       Py_UNBLOCK_THREADS
       __Pyx_FastGIL_Remember();
       #endif
       /*try:*/ {
 
         /* "pybitset/backends/cython/_bitset.pyx":90
  *         cdef bint ret
@@ -2975,58 +4597,105 @@
   /* function exit code */
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_19grow(PyObject *__pyx_v_self, PyObject *__pyx_arg_newarraysize); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_18grow[] = "BitSet.grow(self, size_t newarraysize) -> bool";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_19grow(PyObject *__pyx_v_self, PyObject *__pyx_arg_newarraysize) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_19grow(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_18grow, "BitSet.grow(self, size_t newarraysize) -> bool");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_19grow = {"grow", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_19grow, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_18grow};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_19grow(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
   size_t __pyx_v_newarraysize;
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("grow (wrapper)", 0);
-  assert(__pyx_arg_newarraysize); {
-    __pyx_v_newarraysize = __Pyx_PyInt_As_size_t(__pyx_arg_newarraysize); if (unlikely((__pyx_v_newarraysize == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 87, __pyx_L3_error)
+  {
+    PyObject **__pyx_pyargnames[] = {&__pyx_n_s_newarraysize,0};
+    PyObject* values[1] = {0};
+    if (__pyx_kwds) {
+      Py_ssize_t kw_args;
+      switch (__pyx_nargs) {
+        case  1: values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+        CYTHON_FALLTHROUGH;
+        case  0: break;
+        default: goto __pyx_L5_argtuple_error;
+      }
+      kw_args = __Pyx_NumKwargs_FASTCALL(__pyx_kwds);
+      switch (__pyx_nargs) {
+        case  0:
+        if (likely((values[0] = __Pyx_GetKwValue_FASTCALL(__pyx_kwds, __pyx_kwvalues, __pyx_n_s_newarraysize)) != 0)) kw_args--;
+        else if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 87, __pyx_L3_error)
+        else goto __pyx_L5_argtuple_error;
+      }
+      if (unlikely(kw_args > 0)) {
+        const Py_ssize_t kwd_pos_args = __pyx_nargs;
+        if (unlikely(__Pyx_ParseOptionalKeywords(__pyx_kwds, __pyx_kwvalues, __pyx_pyargnames, 0, values + 0, kwd_pos_args, "grow") < 0)) __PYX_ERR(0, 87, __pyx_L3_error)
+      }
+    } else if (unlikely(__pyx_nargs != 1)) {
+      goto __pyx_L5_argtuple_error;
+    } else {
+      values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+    }
+    __pyx_v_newarraysize = __Pyx_PyInt_As_size_t(values[0]); if (unlikely((__pyx_v_newarraysize == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 87, __pyx_L3_error)
   }
   goto __pyx_L4_argument_unpacking_done;
+  __pyx_L5_argtuple_error:;
+  __Pyx_RaiseArgtupleInvalid("grow", 1, 1, 1, __pyx_nargs); __PYX_ERR(0, 87, __pyx_L3_error)
   __pyx_L3_error:;
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.grow", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __Pyx_RefNannyFinishContext();
   return NULL;
   __pyx_L4_argument_unpacking_done:;
-  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_18grow(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), ((size_t)__pyx_v_newarraysize));
+  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_18grow(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), __pyx_v_newarraysize);
 
   /* function exit code */
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_18grow(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, size_t __pyx_v_newarraysize) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
-  PyObject *__pyx_t_1 = NULL;
+  int __pyx_t_1;
+  PyObject *__pyx_t_2 = NULL;
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   __Pyx_RefNannySetupContext("grow", 0);
   __Pyx_XDECREF(__pyx_r);
-  __pyx_t_1 = __Pyx_PyBool_FromLong(__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_grow(__pyx_v_self, __pyx_v_newarraysize, 1)); if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 87, __pyx_L1_error)
-  __Pyx_GOTREF(__pyx_t_1);
-  __pyx_r = __pyx_t_1;
-  __pyx_t_1 = 0;
+  __pyx_t_1 = __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_grow(__pyx_v_self, __pyx_v_newarraysize, 1); if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 87, __pyx_L1_error)
+  __pyx_t_2 = __Pyx_PyBool_FromLong(__pyx_t_1); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 87, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  __pyx_r = __pyx_t_2;
+  __pyx_t_2 = 0;
   goto __pyx_L0;
 
   /* function exit code */
   __pyx_L1_error:;
-  __Pyx_XDECREF(__pyx_t_1);
+  __Pyx_XDECREF(__pyx_t_2);
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.grow", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
@@ -3035,15 +4704,21 @@
  *         return ret
  * 
  *     cpdef inline bint trim(self):             # <<<<<<<<<<<<<<
  *         cdef bint ret
  *         with nogil:
  */
 
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_21trim(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused); /*proto*/
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_21trim(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
 static CYTHON_INLINE int __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_trim(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, CYTHON_UNUSED int __pyx_skip_dispatch) {
   int __pyx_v_ret;
   int __pyx_r;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("trim", 0);
 
   /* "pybitset/backends/cython/_bitset.pyx":95
@@ -3052,14 +4727,15 @@
  *         with nogil:             # <<<<<<<<<<<<<<
  *             ret = bitset_trim(self._bitset)
  *         return ret
  */
   {
       #ifdef WITH_THREAD
       PyThreadState *_save;
+      _save = NULL;
       Py_UNBLOCK_THREADS
       __Pyx_FastGIL_Remember();
       #endif
       /*try:*/ {
 
         /* "pybitset/backends/cython/_bitset.pyx":96
  *         cdef bint ret
@@ -3111,45 +4787,67 @@
   /* function exit code */
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_21trim(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_20trim[] = "BitSet.trim(self) -> bool";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_21trim(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_21trim(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_20trim, "BitSet.trim(self) -> bool");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_21trim = {"trim", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_21trim, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_20trim};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_21trim(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("trim (wrapper)", 0);
+  if (unlikely(__pyx_nargs > 0)) {
+    __Pyx_RaiseArgtupleInvalid("trim", 1, 0, 0, __pyx_nargs); return NULL;}
+  if (unlikely(__pyx_kwds) && __Pyx_NumKwargs_FASTCALL(__pyx_kwds) && unlikely(!__Pyx_CheckKeywordStrings(__pyx_kwds, "trim", 0))) return NULL;
   __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_20trim(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self));
 
   /* function exit code */
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_20trim(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
-  PyObject *__pyx_t_1 = NULL;
+  int __pyx_t_1;
+  PyObject *__pyx_t_2 = NULL;
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   __Pyx_RefNannySetupContext("trim", 0);
   __Pyx_XDECREF(__pyx_r);
-  __pyx_t_1 = __Pyx_PyBool_FromLong(__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_trim(__pyx_v_self, 1)); if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 93, __pyx_L1_error)
-  __Pyx_GOTREF(__pyx_t_1);
-  __pyx_r = __pyx_t_1;
-  __pyx_t_1 = 0;
+  __pyx_t_1 = __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_trim(__pyx_v_self, 1); if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 93, __pyx_L1_error)
+  __pyx_t_2 = __Pyx_PyBool_FromLong(__pyx_t_1); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 93, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  __pyx_r = __pyx_t_2;
+  __pyx_t_2 = 0;
   goto __pyx_L0;
 
   /* function exit code */
   __pyx_L1_error:;
-  __Pyx_XDECREF(__pyx_t_1);
+  __Pyx_XDECREF(__pyx_t_2);
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.trim", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
@@ -3158,15 +4856,21 @@
  *         return ret
  * 
  *     cpdef inline shift_left(self, size_t s):             # <<<<<<<<<<<<<<
  *         with nogil:
  *             bitset_shift_left(self._bitset, s)
  */
 
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_23shift_left(PyObject *__pyx_v_self, PyObject *__pyx_arg_s); /*proto*/
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_23shift_left(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
 static CYTHON_INLINE PyObject *__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_shift_left(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, size_t __pyx_v_s, CYTHON_UNUSED int __pyx_skip_dispatch) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("shift_left", 0);
 
   /* "pybitset/backends/cython/_bitset.pyx":100
  * 
@@ -3174,14 +4878,15 @@
  *         with nogil:             # <<<<<<<<<<<<<<
  *             bitset_shift_left(self._bitset, s)
  * 
  */
   {
       #ifdef WITH_THREAD
       PyThreadState *_save;
+      _save = NULL;
       Py_UNBLOCK_THREADS
       __Pyx_FastGIL_Remember();
       #endif
       /*try:*/ {
 
         /* "pybitset/backends/cython/_bitset.pyx":101
  *     cpdef inline shift_left(self, size_t s):
@@ -3224,34 +4929,79 @@
   __pyx_r = Py_None; __Pyx_INCREF(Py_None);
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_23shift_left(PyObject *__pyx_v_self, PyObject *__pyx_arg_s); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_22shift_left[] = "BitSet.shift_left(self, size_t s)";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_23shift_left(PyObject *__pyx_v_self, PyObject *__pyx_arg_s) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_23shift_left(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_22shift_left, "BitSet.shift_left(self, size_t s)");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_23shift_left = {"shift_left", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_23shift_left, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_22shift_left};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_23shift_left(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
   size_t __pyx_v_s;
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("shift_left (wrapper)", 0);
-  assert(__pyx_arg_s); {
-    __pyx_v_s = __Pyx_PyInt_As_size_t(__pyx_arg_s); if (unlikely((__pyx_v_s == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 99, __pyx_L3_error)
+  {
+    PyObject **__pyx_pyargnames[] = {&__pyx_n_s_s,0};
+    PyObject* values[1] = {0};
+    if (__pyx_kwds) {
+      Py_ssize_t kw_args;
+      switch (__pyx_nargs) {
+        case  1: values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+        CYTHON_FALLTHROUGH;
+        case  0: break;
+        default: goto __pyx_L5_argtuple_error;
+      }
+      kw_args = __Pyx_NumKwargs_FASTCALL(__pyx_kwds);
+      switch (__pyx_nargs) {
+        case  0:
+        if (likely((values[0] = __Pyx_GetKwValue_FASTCALL(__pyx_kwds, __pyx_kwvalues, __pyx_n_s_s)) != 0)) kw_args--;
+        else if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 99, __pyx_L3_error)
+        else goto __pyx_L5_argtuple_error;
+      }
+      if (unlikely(kw_args > 0)) {
+        const Py_ssize_t kwd_pos_args = __pyx_nargs;
+        if (unlikely(__Pyx_ParseOptionalKeywords(__pyx_kwds, __pyx_kwvalues, __pyx_pyargnames, 0, values + 0, kwd_pos_args, "shift_left") < 0)) __PYX_ERR(0, 99, __pyx_L3_error)
+      }
+    } else if (unlikely(__pyx_nargs != 1)) {
+      goto __pyx_L5_argtuple_error;
+    } else {
+      values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+    }
+    __pyx_v_s = __Pyx_PyInt_As_size_t(values[0]); if (unlikely((__pyx_v_s == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 99, __pyx_L3_error)
   }
   goto __pyx_L4_argument_unpacking_done;
+  __pyx_L5_argtuple_error:;
+  __Pyx_RaiseArgtupleInvalid("shift_left", 1, 1, 1, __pyx_nargs); __PYX_ERR(0, 99, __pyx_L3_error)
   __pyx_L3_error:;
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.shift_left", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __Pyx_RefNannyFinishContext();
   return NULL;
   __pyx_L4_argument_unpacking_done:;
-  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_22shift_left(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), ((size_t)__pyx_v_s));
+  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_22shift_left(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), __pyx_v_s);
 
   /* function exit code */
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_22shift_left(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, size_t __pyx_v_s) {
@@ -3284,15 +5034,21 @@
  *             bitset_shift_left(self._bitset, s)
  * 
  *     cpdef inline shift_right(self, size_t s):             # <<<<<<<<<<<<<<
  *         with nogil:
  *             bitset_shift_right(self._bitset, s)
  */
 
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_25shift_right(PyObject *__pyx_v_self, PyObject *__pyx_arg_s); /*proto*/
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_25shift_right(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
 static CYTHON_INLINE PyObject *__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_shift_right(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, size_t __pyx_v_s, CYTHON_UNUSED int __pyx_skip_dispatch) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("shift_right", 0);
 
   /* "pybitset/backends/cython/_bitset.pyx":104
  * 
@@ -3300,14 +5056,15 @@
  *         with nogil:             # <<<<<<<<<<<<<<
  *             bitset_shift_right(self._bitset, s)
  * 
  */
   {
       #ifdef WITH_THREAD
       PyThreadState *_save;
+      _save = NULL;
       Py_UNBLOCK_THREADS
       __Pyx_FastGIL_Remember();
       #endif
       /*try:*/ {
 
         /* "pybitset/backends/cython/_bitset.pyx":105
  *     cpdef inline shift_right(self, size_t s):
@@ -3350,34 +5107,79 @@
   __pyx_r = Py_None; __Pyx_INCREF(Py_None);
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_25shift_right(PyObject *__pyx_v_self, PyObject *__pyx_arg_s); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_24shift_right[] = "BitSet.shift_right(self, size_t s)";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_25shift_right(PyObject *__pyx_v_self, PyObject *__pyx_arg_s) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_25shift_right(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_24shift_right, "BitSet.shift_right(self, size_t s)");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_25shift_right = {"shift_right", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_25shift_right, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_24shift_right};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_25shift_right(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
   size_t __pyx_v_s;
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("shift_right (wrapper)", 0);
-  assert(__pyx_arg_s); {
-    __pyx_v_s = __Pyx_PyInt_As_size_t(__pyx_arg_s); if (unlikely((__pyx_v_s == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 103, __pyx_L3_error)
+  {
+    PyObject **__pyx_pyargnames[] = {&__pyx_n_s_s,0};
+    PyObject* values[1] = {0};
+    if (__pyx_kwds) {
+      Py_ssize_t kw_args;
+      switch (__pyx_nargs) {
+        case  1: values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+        CYTHON_FALLTHROUGH;
+        case  0: break;
+        default: goto __pyx_L5_argtuple_error;
+      }
+      kw_args = __Pyx_NumKwargs_FASTCALL(__pyx_kwds);
+      switch (__pyx_nargs) {
+        case  0:
+        if (likely((values[0] = __Pyx_GetKwValue_FASTCALL(__pyx_kwds, __pyx_kwvalues, __pyx_n_s_s)) != 0)) kw_args--;
+        else if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 103, __pyx_L3_error)
+        else goto __pyx_L5_argtuple_error;
+      }
+      if (unlikely(kw_args > 0)) {
+        const Py_ssize_t kwd_pos_args = __pyx_nargs;
+        if (unlikely(__Pyx_ParseOptionalKeywords(__pyx_kwds, __pyx_kwvalues, __pyx_pyargnames, 0, values + 0, kwd_pos_args, "shift_right") < 0)) __PYX_ERR(0, 103, __pyx_L3_error)
+      }
+    } else if (unlikely(__pyx_nargs != 1)) {
+      goto __pyx_L5_argtuple_error;
+    } else {
+      values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+    }
+    __pyx_v_s = __Pyx_PyInt_As_size_t(values[0]); if (unlikely((__pyx_v_s == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 103, __pyx_L3_error)
   }
   goto __pyx_L4_argument_unpacking_done;
+  __pyx_L5_argtuple_error:;
+  __Pyx_RaiseArgtupleInvalid("shift_right", 1, 1, 1, __pyx_nargs); __PYX_ERR(0, 103, __pyx_L3_error)
   __pyx_L3_error:;
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.shift_right", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __Pyx_RefNannyFinishContext();
   return NULL;
   __pyx_L4_argument_unpacking_done:;
-  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_24shift_right(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), ((size_t)__pyx_v_s));
+  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_24shift_right(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), __pyx_v_s);
 
   /* function exit code */
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_24shift_right(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, size_t __pyx_v_s) {
@@ -3410,15 +5212,21 @@
  *             bitset_shift_right(self._bitset, s)
  * 
  *     cpdef inline set(self,  size_t i):             # <<<<<<<<<<<<<<
  *         with nogil:
  *             bitset_set(self._bitset, i)
  */
 
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_27set(PyObject *__pyx_v_self, PyObject *__pyx_arg_i); /*proto*/
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_27set(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
 static CYTHON_INLINE PyObject *__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_set(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, size_t __pyx_v_i, CYTHON_UNUSED int __pyx_skip_dispatch) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("set", 0);
 
   /* "pybitset/backends/cython/_bitset.pyx":108
  * 
@@ -3426,14 +5234,15 @@
  *         with nogil:             # <<<<<<<<<<<<<<
  *             bitset_set(self._bitset, i)
  * 
  */
   {
       #ifdef WITH_THREAD
       PyThreadState *_save;
+      _save = NULL;
       Py_UNBLOCK_THREADS
       __Pyx_FastGIL_Remember();
       #endif
       /*try:*/ {
 
         /* "pybitset/backends/cython/_bitset.pyx":109
  *     cpdef inline set(self,  size_t i):
@@ -3476,34 +5285,79 @@
   __pyx_r = Py_None; __Pyx_INCREF(Py_None);
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_27set(PyObject *__pyx_v_self, PyObject *__pyx_arg_i); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_26set[] = "BitSet.set(self, size_t i)";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_27set(PyObject *__pyx_v_self, PyObject *__pyx_arg_i) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_27set(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_26set, "BitSet.set(self, size_t i)");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_27set = {"set", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_27set, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_26set};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_27set(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
   size_t __pyx_v_i;
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("set (wrapper)", 0);
-  assert(__pyx_arg_i); {
-    __pyx_v_i = __Pyx_PyInt_As_size_t(__pyx_arg_i); if (unlikely((__pyx_v_i == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 107, __pyx_L3_error)
+  {
+    PyObject **__pyx_pyargnames[] = {&__pyx_n_s_i,0};
+    PyObject* values[1] = {0};
+    if (__pyx_kwds) {
+      Py_ssize_t kw_args;
+      switch (__pyx_nargs) {
+        case  1: values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+        CYTHON_FALLTHROUGH;
+        case  0: break;
+        default: goto __pyx_L5_argtuple_error;
+      }
+      kw_args = __Pyx_NumKwargs_FASTCALL(__pyx_kwds);
+      switch (__pyx_nargs) {
+        case  0:
+        if (likely((values[0] = __Pyx_GetKwValue_FASTCALL(__pyx_kwds, __pyx_kwvalues, __pyx_n_s_i)) != 0)) kw_args--;
+        else if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 107, __pyx_L3_error)
+        else goto __pyx_L5_argtuple_error;
+      }
+      if (unlikely(kw_args > 0)) {
+        const Py_ssize_t kwd_pos_args = __pyx_nargs;
+        if (unlikely(__Pyx_ParseOptionalKeywords(__pyx_kwds, __pyx_kwvalues, __pyx_pyargnames, 0, values + 0, kwd_pos_args, "set") < 0)) __PYX_ERR(0, 107, __pyx_L3_error)
+      }
+    } else if (unlikely(__pyx_nargs != 1)) {
+      goto __pyx_L5_argtuple_error;
+    } else {
+      values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+    }
+    __pyx_v_i = __Pyx_PyInt_As_size_t(values[0]); if (unlikely((__pyx_v_i == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 107, __pyx_L3_error)
   }
   goto __pyx_L4_argument_unpacking_done;
+  __pyx_L5_argtuple_error:;
+  __Pyx_RaiseArgtupleInvalid("set", 1, 1, 1, __pyx_nargs); __PYX_ERR(0, 107, __pyx_L3_error)
   __pyx_L3_error:;
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.set", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __Pyx_RefNannyFinishContext();
   return NULL;
   __pyx_L4_argument_unpacking_done:;
-  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_26set(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), ((size_t)__pyx_v_i));
+  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_26set(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), __pyx_v_i);
 
   /* function exit code */
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_26set(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, size_t __pyx_v_i) {
@@ -3536,15 +5390,21 @@
  *             bitset_set(self._bitset, i)
  * 
  *     cpdef inline set_to_value(self, size_t i, bint flag):             # <<<<<<<<<<<<<<
  *         with nogil:
  *             bitset_set_to_value(self._bitset, i, flag)
  */
 
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_29set_to_value(PyObject *__pyx_v_self, PyObject *__pyx_args, PyObject *__pyx_kwds); /*proto*/
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_29set_to_value(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
 static CYTHON_INLINE PyObject *__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_set_to_value(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, size_t __pyx_v_i, int __pyx_v_flag, CYTHON_UNUSED int __pyx_skip_dispatch) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("set_to_value", 0);
 
   /* "pybitset/backends/cython/_bitset.pyx":112
  * 
@@ -3552,14 +5412,15 @@
  *         with nogil:             # <<<<<<<<<<<<<<
  *             bitset_set_to_value(self._bitset, i, flag)
  * 
  */
   {
       #ifdef WITH_THREAD
       PyThreadState *_save;
+      _save = NULL;
       Py_UNBLOCK_THREADS
       __Pyx_FastGIL_Remember();
       #endif
       /*try:*/ {
 
         /* "pybitset/backends/cython/_bitset.pyx":113
  *     cpdef inline set_to_value(self, size_t i, bint flag):
@@ -3602,66 +5463,85 @@
   __pyx_r = Py_None; __Pyx_INCREF(Py_None);
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_29set_to_value(PyObject *__pyx_v_self, PyObject *__pyx_args, PyObject *__pyx_kwds); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_28set_to_value[] = "BitSet.set_to_value(self, size_t i, bool flag)";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_29set_to_value(PyObject *__pyx_v_self, PyObject *__pyx_args, PyObject *__pyx_kwds) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_29set_to_value(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_28set_to_value, "BitSet.set_to_value(self, size_t i, bool flag)");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_29set_to_value = {"set_to_value", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_29set_to_value, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_28set_to_value};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_29set_to_value(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
   size_t __pyx_v_i;
   int __pyx_v_flag;
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("set_to_value (wrapper)", 0);
   {
-    static PyObject **__pyx_pyargnames[] = {&__pyx_n_s_i,&__pyx_n_s_flag,0};
+    PyObject **__pyx_pyargnames[] = {&__pyx_n_s_i,&__pyx_n_s_flag,0};
     PyObject* values[2] = {0,0};
-    if (unlikely(__pyx_kwds)) {
+    if (__pyx_kwds) {
       Py_ssize_t kw_args;
-      const Py_ssize_t pos_args = PyTuple_GET_SIZE(__pyx_args);
-      switch (pos_args) {
-        case  2: values[1] = PyTuple_GET_ITEM(__pyx_args, 1);
+      switch (__pyx_nargs) {
+        case  2: values[1] = __Pyx_Arg_FASTCALL(__pyx_args, 1);
         CYTHON_FALLTHROUGH;
-        case  1: values[0] = PyTuple_GET_ITEM(__pyx_args, 0);
+        case  1: values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
         CYTHON_FALLTHROUGH;
         case  0: break;
         default: goto __pyx_L5_argtuple_error;
       }
-      kw_args = PyDict_Size(__pyx_kwds);
-      switch (pos_args) {
+      kw_args = __Pyx_NumKwargs_FASTCALL(__pyx_kwds);
+      switch (__pyx_nargs) {
         case  0:
-        if (likely((values[0] = __Pyx_PyDict_GetItemStr(__pyx_kwds, __pyx_n_s_i)) != 0)) kw_args--;
+        if (likely((values[0] = __Pyx_GetKwValue_FASTCALL(__pyx_kwds, __pyx_kwvalues, __pyx_n_s_i)) != 0)) kw_args--;
+        else if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 111, __pyx_L3_error)
         else goto __pyx_L5_argtuple_error;
         CYTHON_FALLTHROUGH;
         case  1:
-        if (likely((values[1] = __Pyx_PyDict_GetItemStr(__pyx_kwds, __pyx_n_s_flag)) != 0)) kw_args--;
+        if (likely((values[1] = __Pyx_GetKwValue_FASTCALL(__pyx_kwds, __pyx_kwvalues, __pyx_n_s_flag)) != 0)) kw_args--;
+        else if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 111, __pyx_L3_error)
         else {
           __Pyx_RaiseArgtupleInvalid("set_to_value", 1, 2, 2, 1); __PYX_ERR(0, 111, __pyx_L3_error)
         }
       }
       if (unlikely(kw_args > 0)) {
-        if (unlikely(__Pyx_ParseOptionalKeywords(__pyx_kwds, __pyx_pyargnames, 0, values, pos_args, "set_to_value") < 0)) __PYX_ERR(0, 111, __pyx_L3_error)
+        const Py_ssize_t kwd_pos_args = __pyx_nargs;
+        if (unlikely(__Pyx_ParseOptionalKeywords(__pyx_kwds, __pyx_kwvalues, __pyx_pyargnames, 0, values + 0, kwd_pos_args, "set_to_value") < 0)) __PYX_ERR(0, 111, __pyx_L3_error)
       }
-    } else if (PyTuple_GET_SIZE(__pyx_args) != 2) {
+    } else if (unlikely(__pyx_nargs != 2)) {
       goto __pyx_L5_argtuple_error;
     } else {
-      values[0] = PyTuple_GET_ITEM(__pyx_args, 0);
-      values[1] = PyTuple_GET_ITEM(__pyx_args, 1);
+      values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+      values[1] = __Pyx_Arg_FASTCALL(__pyx_args, 1);
     }
     __pyx_v_i = __Pyx_PyInt_As_size_t(values[0]); if (unlikely((__pyx_v_i == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 111, __pyx_L3_error)
     __pyx_v_flag = __Pyx_PyObject_IsTrue(values[1]); if (unlikely((__pyx_v_flag == (int)-1) && PyErr_Occurred())) __PYX_ERR(0, 111, __pyx_L3_error)
   }
   goto __pyx_L4_argument_unpacking_done;
   __pyx_L5_argtuple_error:;
-  __Pyx_RaiseArgtupleInvalid("set_to_value", 1, 2, 2, PyTuple_GET_SIZE(__pyx_args)); __PYX_ERR(0, 111, __pyx_L3_error)
+  __Pyx_RaiseArgtupleInvalid("set_to_value", 1, 2, 2, __pyx_nargs); __PYX_ERR(0, 111, __pyx_L3_error)
   __pyx_L3_error:;
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.set_to_value", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __Pyx_RefNannyFinishContext();
   return NULL;
   __pyx_L4_argument_unpacking_done:;
   __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_28set_to_value(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), __pyx_v_i, __pyx_v_flag);
 
@@ -3700,15 +5580,21 @@
  *             bitset_set_to_value(self._bitset, i, flag)
  * 
  *     cpdef inline bint get(self, size_t i):             # <<<<<<<<<<<<<<
  *         cdef bint ret
  *         with nogil:
  */
 
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_31get(PyObject *__pyx_v_self, PyObject *__pyx_arg_i); /*proto*/
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_31get(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
 static CYTHON_INLINE int __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_get(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, size_t __pyx_v_i, CYTHON_UNUSED int __pyx_skip_dispatch) {
   int __pyx_v_ret;
   int __pyx_r;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("get", 0);
 
   /* "pybitset/backends/cython/_bitset.pyx":117
@@ -3717,14 +5603,15 @@
  *         with nogil:             # <<<<<<<<<<<<<<
  *             ret = bitset_get(self._bitset, i)
  *         return ret
  */
   {
       #ifdef WITH_THREAD
       PyThreadState *_save;
+      _save = NULL;
       Py_UNBLOCK_THREADS
       __Pyx_FastGIL_Remember();
       #endif
       /*try:*/ {
 
         /* "pybitset/backends/cython/_bitset.pyx":118
  *         cdef bint ret
@@ -3776,58 +5663,105 @@
   /* function exit code */
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_31get(PyObject *__pyx_v_self, PyObject *__pyx_arg_i); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_30get[] = "BitSet.get(self, size_t i) -> bool";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_31get(PyObject *__pyx_v_self, PyObject *__pyx_arg_i) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_31get(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_30get, "BitSet.get(self, size_t i) -> bool");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_31get = {"get", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_31get, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_30get};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_31get(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
   size_t __pyx_v_i;
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("get (wrapper)", 0);
-  assert(__pyx_arg_i); {
-    __pyx_v_i = __Pyx_PyInt_As_size_t(__pyx_arg_i); if (unlikely((__pyx_v_i == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 115, __pyx_L3_error)
+  {
+    PyObject **__pyx_pyargnames[] = {&__pyx_n_s_i,0};
+    PyObject* values[1] = {0};
+    if (__pyx_kwds) {
+      Py_ssize_t kw_args;
+      switch (__pyx_nargs) {
+        case  1: values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+        CYTHON_FALLTHROUGH;
+        case  0: break;
+        default: goto __pyx_L5_argtuple_error;
+      }
+      kw_args = __Pyx_NumKwargs_FASTCALL(__pyx_kwds);
+      switch (__pyx_nargs) {
+        case  0:
+        if (likely((values[0] = __Pyx_GetKwValue_FASTCALL(__pyx_kwds, __pyx_kwvalues, __pyx_n_s_i)) != 0)) kw_args--;
+        else if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 115, __pyx_L3_error)
+        else goto __pyx_L5_argtuple_error;
+      }
+      if (unlikely(kw_args > 0)) {
+        const Py_ssize_t kwd_pos_args = __pyx_nargs;
+        if (unlikely(__Pyx_ParseOptionalKeywords(__pyx_kwds, __pyx_kwvalues, __pyx_pyargnames, 0, values + 0, kwd_pos_args, "get") < 0)) __PYX_ERR(0, 115, __pyx_L3_error)
+      }
+    } else if (unlikely(__pyx_nargs != 1)) {
+      goto __pyx_L5_argtuple_error;
+    } else {
+      values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+    }
+    __pyx_v_i = __Pyx_PyInt_As_size_t(values[0]); if (unlikely((__pyx_v_i == (size_t)-1) && PyErr_Occurred())) __PYX_ERR(0, 115, __pyx_L3_error)
   }
   goto __pyx_L4_argument_unpacking_done;
+  __pyx_L5_argtuple_error:;
+  __Pyx_RaiseArgtupleInvalid("get", 1, 1, 1, __pyx_nargs); __PYX_ERR(0, 115, __pyx_L3_error)
   __pyx_L3_error:;
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.get", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __Pyx_RefNannyFinishContext();
   return NULL;
   __pyx_L4_argument_unpacking_done:;
-  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_30get(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), ((size_t)__pyx_v_i));
+  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_30get(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), __pyx_v_i);
 
   /* function exit code */
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_30get(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, size_t __pyx_v_i) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
-  PyObject *__pyx_t_1 = NULL;
+  int __pyx_t_1;
+  PyObject *__pyx_t_2 = NULL;
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   __Pyx_RefNannySetupContext("get", 0);
   __Pyx_XDECREF(__pyx_r);
-  __pyx_t_1 = __Pyx_PyBool_FromLong(__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_get(__pyx_v_self, __pyx_v_i, 1)); if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 115, __pyx_L1_error)
-  __Pyx_GOTREF(__pyx_t_1);
-  __pyx_r = __pyx_t_1;
-  __pyx_t_1 = 0;
+  __pyx_t_1 = __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_get(__pyx_v_self, __pyx_v_i, 1); if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 115, __pyx_L1_error)
+  __pyx_t_2 = __Pyx_PyBool_FromLong(__pyx_t_1); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 115, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  __pyx_r = __pyx_t_2;
+  __pyx_t_2 = 0;
   goto __pyx_L0;
 
   /* function exit code */
   __pyx_L1_error:;
-  __Pyx_XDECREF(__pyx_t_1);
+  __Pyx_XDECREF(__pyx_t_2);
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.get", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
@@ -3836,15 +5770,21 @@
  *         return ret
  * 
  *     cpdef inline size_t count(self):             # <<<<<<<<<<<<<<
  *         cdef size_t ret
  *         with nogil:
  */
 
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_33count(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused); /*proto*/
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_33count(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
 static CYTHON_INLINE size_t __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_count(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, CYTHON_UNUSED int __pyx_skip_dispatch) {
   size_t __pyx_v_ret;
   size_t __pyx_r;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("count", 0);
 
   /* "pybitset/backends/cython/_bitset.pyx":123
@@ -3853,14 +5793,15 @@
  *         with nogil:             # <<<<<<<<<<<<<<
  *             ret = bitset_count(self._bitset)
  *         return ret
  */
   {
       #ifdef WITH_THREAD
       PyThreadState *_save;
+      _save = NULL;
       Py_UNBLOCK_THREADS
       __Pyx_FastGIL_Remember();
       #endif
       /*try:*/ {
 
         /* "pybitset/backends/cython/_bitset.pyx":124
  *         cdef size_t ret
@@ -3912,45 +5853,67 @@
   /* function exit code */
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_33count(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_32count[] = "BitSet.count(self) -> size_t";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_33count(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_33count(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_32count, "BitSet.count(self) -> size_t");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_33count = {"count", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_33count, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_32count};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_33count(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("count (wrapper)", 0);
+  if (unlikely(__pyx_nargs > 0)) {
+    __Pyx_RaiseArgtupleInvalid("count", 1, 0, 0, __pyx_nargs); return NULL;}
+  if (unlikely(__pyx_kwds) && __Pyx_NumKwargs_FASTCALL(__pyx_kwds) && unlikely(!__Pyx_CheckKeywordStrings(__pyx_kwds, "count", 0))) return NULL;
   __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_32count(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self));
 
   /* function exit code */
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_32count(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
-  PyObject *__pyx_t_1 = NULL;
+  size_t __pyx_t_1;
+  PyObject *__pyx_t_2 = NULL;
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   __Pyx_RefNannySetupContext("count", 0);
   __Pyx_XDECREF(__pyx_r);
-  __pyx_t_1 = __Pyx_PyInt_FromSize_t(__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_count(__pyx_v_self, 1)); if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 121, __pyx_L1_error)
-  __Pyx_GOTREF(__pyx_t_1);
-  __pyx_r = __pyx_t_1;
-  __pyx_t_1 = 0;
+  __pyx_t_1 = __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_count(__pyx_v_self, 1); if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 121, __pyx_L1_error)
+  __pyx_t_2 = __Pyx_PyInt_FromSize_t(__pyx_t_1); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 121, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  __pyx_r = __pyx_t_2;
+  __pyx_t_2 = 0;
   goto __pyx_L0;
 
   /* function exit code */
   __pyx_L1_error:;
-  __Pyx_XDECREF(__pyx_t_1);
+  __Pyx_XDECREF(__pyx_t_2);
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.count", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
@@ -3959,15 +5922,21 @@
  *         return ret
  * 
  *     cpdef inline size_t minimum(self):             # <<<<<<<<<<<<<<
  *         cdef size_t ret
  *         with nogil:
  */
 
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_35minimum(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused); /*proto*/
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_35minimum(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
 static CYTHON_INLINE size_t __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_minimum(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, CYTHON_UNUSED int __pyx_skip_dispatch) {
   size_t __pyx_v_ret;
   size_t __pyx_r;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("minimum", 0);
 
   /* "pybitset/backends/cython/_bitset.pyx":129
@@ -3976,14 +5945,15 @@
  *         with nogil:             # <<<<<<<<<<<<<<
  *             ret = bitset_minimum(self._bitset)
  *         return ret
  */
   {
       #ifdef WITH_THREAD
       PyThreadState *_save;
+      _save = NULL;
       Py_UNBLOCK_THREADS
       __Pyx_FastGIL_Remember();
       #endif
       /*try:*/ {
 
         /* "pybitset/backends/cython/_bitset.pyx":130
  *         cdef size_t ret
@@ -4035,45 +6005,67 @@
   /* function exit code */
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_35minimum(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_34minimum[] = "BitSet.minimum(self) -> size_t";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_35minimum(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_35minimum(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_34minimum, "BitSet.minimum(self) -> size_t");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_35minimum = {"minimum", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_35minimum, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_34minimum};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_35minimum(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("minimum (wrapper)", 0);
+  if (unlikely(__pyx_nargs > 0)) {
+    __Pyx_RaiseArgtupleInvalid("minimum", 1, 0, 0, __pyx_nargs); return NULL;}
+  if (unlikely(__pyx_kwds) && __Pyx_NumKwargs_FASTCALL(__pyx_kwds) && unlikely(!__Pyx_CheckKeywordStrings(__pyx_kwds, "minimum", 0))) return NULL;
   __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_34minimum(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self));
 
   /* function exit code */
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_34minimum(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
-  PyObject *__pyx_t_1 = NULL;
+  size_t __pyx_t_1;
+  PyObject *__pyx_t_2 = NULL;
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   __Pyx_RefNannySetupContext("minimum", 0);
   __Pyx_XDECREF(__pyx_r);
-  __pyx_t_1 = __Pyx_PyInt_FromSize_t(__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_minimum(__pyx_v_self, 1)); if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 127, __pyx_L1_error)
-  __Pyx_GOTREF(__pyx_t_1);
-  __pyx_r = __pyx_t_1;
-  __pyx_t_1 = 0;
+  __pyx_t_1 = __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_minimum(__pyx_v_self, 1); if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 127, __pyx_L1_error)
+  __pyx_t_2 = __Pyx_PyInt_FromSize_t(__pyx_t_1); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 127, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  __pyx_r = __pyx_t_2;
+  __pyx_t_2 = 0;
   goto __pyx_L0;
 
   /* function exit code */
   __pyx_L1_error:;
-  __Pyx_XDECREF(__pyx_t_1);
+  __Pyx_XDECREF(__pyx_t_2);
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.minimum", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
@@ -4082,15 +6074,21 @@
  *         return ret
  * 
  *     cpdef inline size_t maximum(self):             # <<<<<<<<<<<<<<
  *         cdef size_t ret
  *         with nogil:
  */
 
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_37maximum(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused); /*proto*/
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_37maximum(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
 static CYTHON_INLINE size_t __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_maximum(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, CYTHON_UNUSED int __pyx_skip_dispatch) {
   size_t __pyx_v_ret;
   size_t __pyx_r;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("maximum", 0);
 
   /* "pybitset/backends/cython/_bitset.pyx":135
@@ -4099,14 +6097,15 @@
  *         with nogil:             # <<<<<<<<<<<<<<
  *             ret = bitset_maximum(self._bitset)
  *         return ret
  */
   {
       #ifdef WITH_THREAD
       PyThreadState *_save;
+      _save = NULL;
       Py_UNBLOCK_THREADS
       __Pyx_FastGIL_Remember();
       #endif
       /*try:*/ {
 
         /* "pybitset/backends/cython/_bitset.pyx":136
  *         cdef size_t ret
@@ -4158,45 +6157,67 @@
   /* function exit code */
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_37maximum(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_36maximum[] = "BitSet.maximum(self) -> size_t";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_37maximum(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_37maximum(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_36maximum, "BitSet.maximum(self) -> size_t");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_37maximum = {"maximum", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_37maximum, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_36maximum};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_37maximum(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("maximum (wrapper)", 0);
+  if (unlikely(__pyx_nargs > 0)) {
+    __Pyx_RaiseArgtupleInvalid("maximum", 1, 0, 0, __pyx_nargs); return NULL;}
+  if (unlikely(__pyx_kwds) && __Pyx_NumKwargs_FASTCALL(__pyx_kwds) && unlikely(!__Pyx_CheckKeywordStrings(__pyx_kwds, "maximum", 0))) return NULL;
   __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_36maximum(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self));
 
   /* function exit code */
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_36maximum(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
-  PyObject *__pyx_t_1 = NULL;
+  size_t __pyx_t_1;
+  PyObject *__pyx_t_2 = NULL;
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   __Pyx_RefNannySetupContext("maximum", 0);
   __Pyx_XDECREF(__pyx_r);
-  __pyx_t_1 = __Pyx_PyInt_FromSize_t(__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_maximum(__pyx_v_self, 1)); if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 133, __pyx_L1_error)
-  __Pyx_GOTREF(__pyx_t_1);
-  __pyx_r = __pyx_t_1;
-  __pyx_t_1 = 0;
+  __pyx_t_1 = __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_maximum(__pyx_v_self, 1); if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 133, __pyx_L1_error)
+  __pyx_t_2 = __Pyx_PyInt_FromSize_t(__pyx_t_1); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 133, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  __pyx_r = __pyx_t_2;
+  __pyx_t_2 = 0;
   goto __pyx_L0;
 
   /* function exit code */
   __pyx_L1_error:;
-  __Pyx_XDECREF(__pyx_t_1);
+  __Pyx_XDECREF(__pyx_t_2);
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.maximum", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
@@ -4205,15 +6226,21 @@
  *         return ret
  * 
  *     cpdef inline bint inplace_union(self, BitSet b2):             # <<<<<<<<<<<<<<
  *         cdef bint ret
  *         with nogil:
  */
 
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_39inplace_union(PyObject *__pyx_v_self, PyObject *__pyx_v_b2); /*proto*/
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_39inplace_union(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
 static CYTHON_INLINE int __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_inplace_union(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2, CYTHON_UNUSED int __pyx_skip_dispatch) {
   int __pyx_v_ret;
   int __pyx_r;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("inplace_union", 0);
 
   /* "pybitset/backends/cython/_bitset.pyx":141
@@ -4222,14 +6249,15 @@
  *         with nogil:             # <<<<<<<<<<<<<<
  *             ret = bitset_inplace_union(self._bitset, b2._bitset)
  *         return ret
  */
   {
       #ifdef WITH_THREAD
       PyThreadState *_save;
+      _save = NULL;
       Py_UNBLOCK_THREADS
       __Pyx_FastGIL_Remember();
       #endif
       /*try:*/ {
 
         /* "pybitset/backends/cython/_bitset.pyx":142
  *         cdef bint ret
@@ -4281,53 +6309,110 @@
   /* function exit code */
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_39inplace_union(PyObject *__pyx_v_self, PyObject *__pyx_v_b2); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_38inplace_union[] = "BitSet.inplace_union(self, BitSet b2) -> bool";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_39inplace_union(PyObject *__pyx_v_self, PyObject *__pyx_v_b2) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_39inplace_union(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_38inplace_union, "BitSet.inplace_union(self, BitSet b2) -> bool");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_39inplace_union = {"inplace_union", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_39inplace_union, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_38inplace_union};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_39inplace_union(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
+  struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2 = 0;
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("inplace_union (wrapper)", 0);
+  {
+    PyObject **__pyx_pyargnames[] = {&__pyx_n_s_b2,0};
+    PyObject* values[1] = {0};
+    if (__pyx_kwds) {
+      Py_ssize_t kw_args;
+      switch (__pyx_nargs) {
+        case  1: values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+        CYTHON_FALLTHROUGH;
+        case  0: break;
+        default: goto __pyx_L5_argtuple_error;
+      }
+      kw_args = __Pyx_NumKwargs_FASTCALL(__pyx_kwds);
+      switch (__pyx_nargs) {
+        case  0:
+        if (likely((values[0] = __Pyx_GetKwValue_FASTCALL(__pyx_kwds, __pyx_kwvalues, __pyx_n_s_b2)) != 0)) kw_args--;
+        else if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 139, __pyx_L3_error)
+        else goto __pyx_L5_argtuple_error;
+      }
+      if (unlikely(kw_args > 0)) {
+        const Py_ssize_t kwd_pos_args = __pyx_nargs;
+        if (unlikely(__Pyx_ParseOptionalKeywords(__pyx_kwds, __pyx_kwvalues, __pyx_pyargnames, 0, values + 0, kwd_pos_args, "inplace_union") < 0)) __PYX_ERR(0, 139, __pyx_L3_error)
+      }
+    } else if (unlikely(__pyx_nargs != 1)) {
+      goto __pyx_L5_argtuple_error;
+    } else {
+      values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+    }
+    __pyx_v_b2 = ((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)values[0]);
+  }
+  goto __pyx_L4_argument_unpacking_done;
+  __pyx_L5_argtuple_error:;
+  __Pyx_RaiseArgtupleInvalid("inplace_union", 1, 1, 1, __pyx_nargs); __PYX_ERR(0, 139, __pyx_L3_error)
+  __pyx_L3_error:;
+  __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.inplace_union", __pyx_clineno, __pyx_lineno, __pyx_filename);
+  __Pyx_RefNannyFinishContext();
+  return NULL;
+  __pyx_L4_argument_unpacking_done:;
   if (unlikely(!__Pyx_ArgTypeTest(((PyObject *)__pyx_v_b2), __pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet, 1, "b2", 0))) __PYX_ERR(0, 139, __pyx_L1_error)
-  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_38inplace_union(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), ((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_b2));
+  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_38inplace_union(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), __pyx_v_b2);
 
   /* function exit code */
   goto __pyx_L0;
   __pyx_L1_error:;
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_38inplace_union(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
-  PyObject *__pyx_t_1 = NULL;
+  int __pyx_t_1;
+  PyObject *__pyx_t_2 = NULL;
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   __Pyx_RefNannySetupContext("inplace_union", 0);
   __Pyx_XDECREF(__pyx_r);
-  __pyx_t_1 = __Pyx_PyBool_FromLong(__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_inplace_union(__pyx_v_self, __pyx_v_b2, 1)); if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 139, __pyx_L1_error)
-  __Pyx_GOTREF(__pyx_t_1);
-  __pyx_r = __pyx_t_1;
-  __pyx_t_1 = 0;
+  __pyx_t_1 = __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_inplace_union(__pyx_v_self, __pyx_v_b2, 1); if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 139, __pyx_L1_error)
+  __pyx_t_2 = __Pyx_PyBool_FromLong(__pyx_t_1); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 139, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  __pyx_r = __pyx_t_2;
+  __pyx_t_2 = 0;
   goto __pyx_L0;
 
   /* function exit code */
   __pyx_L1_error:;
-  __Pyx_XDECREF(__pyx_t_1);
+  __Pyx_XDECREF(__pyx_t_2);
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.inplace_union", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
@@ -4336,15 +6421,21 @@
  *         return ret
  * 
  *     cpdef inline size_t union_count(self, BitSet b2):             # <<<<<<<<<<<<<<
  *         cdef size_t ret
  *         with nogil:
  */
 
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_41union_count(PyObject *__pyx_v_self, PyObject *__pyx_v_b2); /*proto*/
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_41union_count(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
 static CYTHON_INLINE size_t __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_union_count(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2, CYTHON_UNUSED int __pyx_skip_dispatch) {
   size_t __pyx_v_ret;
   size_t __pyx_r;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("union_count", 0);
 
   /* "pybitset/backends/cython/_bitset.pyx":147
@@ -4353,14 +6444,15 @@
  *         with nogil:             # <<<<<<<<<<<<<<
  *             ret = bitset_union_count(self._bitset, b2._bitset)
  *         return ret
  */
   {
       #ifdef WITH_THREAD
       PyThreadState *_save;
+      _save = NULL;
       Py_UNBLOCK_THREADS
       __Pyx_FastGIL_Remember();
       #endif
       /*try:*/ {
 
         /* "pybitset/backends/cython/_bitset.pyx":148
  *         cdef size_t ret
@@ -4412,53 +6504,110 @@
   /* function exit code */
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_41union_count(PyObject *__pyx_v_self, PyObject *__pyx_v_b2); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_40union_count[] = "BitSet.union_count(self, BitSet b2) -> size_t";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_41union_count(PyObject *__pyx_v_self, PyObject *__pyx_v_b2) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_41union_count(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_40union_count, "BitSet.union_count(self, BitSet b2) -> size_t");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_41union_count = {"union_count", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_41union_count, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_40union_count};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_41union_count(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
+  struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2 = 0;
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("union_count (wrapper)", 0);
+  {
+    PyObject **__pyx_pyargnames[] = {&__pyx_n_s_b2,0};
+    PyObject* values[1] = {0};
+    if (__pyx_kwds) {
+      Py_ssize_t kw_args;
+      switch (__pyx_nargs) {
+        case  1: values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+        CYTHON_FALLTHROUGH;
+        case  0: break;
+        default: goto __pyx_L5_argtuple_error;
+      }
+      kw_args = __Pyx_NumKwargs_FASTCALL(__pyx_kwds);
+      switch (__pyx_nargs) {
+        case  0:
+        if (likely((values[0] = __Pyx_GetKwValue_FASTCALL(__pyx_kwds, __pyx_kwvalues, __pyx_n_s_b2)) != 0)) kw_args--;
+        else if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 145, __pyx_L3_error)
+        else goto __pyx_L5_argtuple_error;
+      }
+      if (unlikely(kw_args > 0)) {
+        const Py_ssize_t kwd_pos_args = __pyx_nargs;
+        if (unlikely(__Pyx_ParseOptionalKeywords(__pyx_kwds, __pyx_kwvalues, __pyx_pyargnames, 0, values + 0, kwd_pos_args, "union_count") < 0)) __PYX_ERR(0, 145, __pyx_L3_error)
+      }
+    } else if (unlikely(__pyx_nargs != 1)) {
+      goto __pyx_L5_argtuple_error;
+    } else {
+      values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+    }
+    __pyx_v_b2 = ((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)values[0]);
+  }
+  goto __pyx_L4_argument_unpacking_done;
+  __pyx_L5_argtuple_error:;
+  __Pyx_RaiseArgtupleInvalid("union_count", 1, 1, 1, __pyx_nargs); __PYX_ERR(0, 145, __pyx_L3_error)
+  __pyx_L3_error:;
+  __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.union_count", __pyx_clineno, __pyx_lineno, __pyx_filename);
+  __Pyx_RefNannyFinishContext();
+  return NULL;
+  __pyx_L4_argument_unpacking_done:;
   if (unlikely(!__Pyx_ArgTypeTest(((PyObject *)__pyx_v_b2), __pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet, 1, "b2", 0))) __PYX_ERR(0, 145, __pyx_L1_error)
-  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_40union_count(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), ((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_b2));
+  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_40union_count(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), __pyx_v_b2);
 
   /* function exit code */
   goto __pyx_L0;
   __pyx_L1_error:;
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_40union_count(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
-  PyObject *__pyx_t_1 = NULL;
+  size_t __pyx_t_1;
+  PyObject *__pyx_t_2 = NULL;
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   __Pyx_RefNannySetupContext("union_count", 0);
   __Pyx_XDECREF(__pyx_r);
-  __pyx_t_1 = __Pyx_PyInt_FromSize_t(__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_union_count(__pyx_v_self, __pyx_v_b2, 1)); if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 145, __pyx_L1_error)
-  __Pyx_GOTREF(__pyx_t_1);
-  __pyx_r = __pyx_t_1;
-  __pyx_t_1 = 0;
+  __pyx_t_1 = __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_union_count(__pyx_v_self, __pyx_v_b2, 1); if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 145, __pyx_L1_error)
+  __pyx_t_2 = __Pyx_PyInt_FromSize_t(__pyx_t_1); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 145, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  __pyx_r = __pyx_t_2;
+  __pyx_t_2 = 0;
   goto __pyx_L0;
 
   /* function exit code */
   __pyx_L1_error:;
-  __Pyx_XDECREF(__pyx_t_1);
+  __Pyx_XDECREF(__pyx_t_2);
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.union_count", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
@@ -4467,15 +6616,21 @@
  *         return ret
  * 
  *     cpdef inline inplace_intersection(self, BitSet b2):             # <<<<<<<<<<<<<<
  *         with nogil:
  *             bitset_inplace_intersection(self._bitset, b2._bitset)
  */
 
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_43inplace_intersection(PyObject *__pyx_v_self, PyObject *__pyx_v_b2); /*proto*/
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_43inplace_intersection(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
 static CYTHON_INLINE PyObject *__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_inplace_intersection(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2, CYTHON_UNUSED int __pyx_skip_dispatch) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("inplace_intersection", 0);
 
   /* "pybitset/backends/cython/_bitset.pyx":152
  * 
@@ -4483,14 +6638,15 @@
  *         with nogil:             # <<<<<<<<<<<<<<
  *             bitset_inplace_intersection(self._bitset, b2._bitset)
  * 
  */
   {
       #ifdef WITH_THREAD
       PyThreadState *_save;
+      _save = NULL;
       Py_UNBLOCK_THREADS
       __Pyx_FastGIL_Remember();
       #endif
       /*try:*/ {
 
         /* "pybitset/backends/cython/_bitset.pyx":153
  *     cpdef inline inplace_intersection(self, BitSet b2):
@@ -4533,25 +6689,80 @@
   __pyx_r = Py_None; __Pyx_INCREF(Py_None);
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_43inplace_intersection(PyObject *__pyx_v_self, PyObject *__pyx_v_b2); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_42inplace_intersection[] = "BitSet.inplace_intersection(self, BitSet b2)";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_43inplace_intersection(PyObject *__pyx_v_self, PyObject *__pyx_v_b2) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_43inplace_intersection(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_42inplace_intersection, "BitSet.inplace_intersection(self, BitSet b2)");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_43inplace_intersection = {"inplace_intersection", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_43inplace_intersection, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_42inplace_intersection};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_43inplace_intersection(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
+  struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2 = 0;
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("inplace_intersection (wrapper)", 0);
+  {
+    PyObject **__pyx_pyargnames[] = {&__pyx_n_s_b2,0};
+    PyObject* values[1] = {0};
+    if (__pyx_kwds) {
+      Py_ssize_t kw_args;
+      switch (__pyx_nargs) {
+        case  1: values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+        CYTHON_FALLTHROUGH;
+        case  0: break;
+        default: goto __pyx_L5_argtuple_error;
+      }
+      kw_args = __Pyx_NumKwargs_FASTCALL(__pyx_kwds);
+      switch (__pyx_nargs) {
+        case  0:
+        if (likely((values[0] = __Pyx_GetKwValue_FASTCALL(__pyx_kwds, __pyx_kwvalues, __pyx_n_s_b2)) != 0)) kw_args--;
+        else if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 151, __pyx_L3_error)
+        else goto __pyx_L5_argtuple_error;
+      }
+      if (unlikely(kw_args > 0)) {
+        const Py_ssize_t kwd_pos_args = __pyx_nargs;
+        if (unlikely(__Pyx_ParseOptionalKeywords(__pyx_kwds, __pyx_kwvalues, __pyx_pyargnames, 0, values + 0, kwd_pos_args, "inplace_intersection") < 0)) __PYX_ERR(0, 151, __pyx_L3_error)
+      }
+    } else if (unlikely(__pyx_nargs != 1)) {
+      goto __pyx_L5_argtuple_error;
+    } else {
+      values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+    }
+    __pyx_v_b2 = ((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)values[0]);
+  }
+  goto __pyx_L4_argument_unpacking_done;
+  __pyx_L5_argtuple_error:;
+  __Pyx_RaiseArgtupleInvalid("inplace_intersection", 1, 1, 1, __pyx_nargs); __PYX_ERR(0, 151, __pyx_L3_error)
+  __pyx_L3_error:;
+  __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.inplace_intersection", __pyx_clineno, __pyx_lineno, __pyx_filename);
+  __Pyx_RefNannyFinishContext();
+  return NULL;
+  __pyx_L4_argument_unpacking_done:;
   if (unlikely(!__Pyx_ArgTypeTest(((PyObject *)__pyx_v_b2), __pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet, 1, "b2", 0))) __PYX_ERR(0, 151, __pyx_L1_error)
-  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_42inplace_intersection(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), ((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_b2));
+  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_42inplace_intersection(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), __pyx_v_b2);
 
   /* function exit code */
   goto __pyx_L0;
   __pyx_L1_error:;
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
@@ -4588,15 +6799,21 @@
  *             bitset_inplace_intersection(self._bitset, b2._bitset)
  * 
  *     cpdef inline size_t intersection_count(self, BitSet b2):             # <<<<<<<<<<<<<<
  *         cdef size_t ret
  *         with nogil:
  */
 
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_45intersection_count(PyObject *__pyx_v_self, PyObject *__pyx_v_b2); /*proto*/
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_45intersection_count(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
 static CYTHON_INLINE size_t __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_intersection_count(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2, CYTHON_UNUSED int __pyx_skip_dispatch) {
   size_t __pyx_v_ret;
   size_t __pyx_r;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("intersection_count", 0);
 
   /* "pybitset/backends/cython/_bitset.pyx":157
@@ -4605,14 +6822,15 @@
  *         with nogil:             # <<<<<<<<<<<<<<
  *             ret = bitset_intersection_count(self._bitset, b2._bitset)
  *         return ret
  */
   {
       #ifdef WITH_THREAD
       PyThreadState *_save;
+      _save = NULL;
       Py_UNBLOCK_THREADS
       __Pyx_FastGIL_Remember();
       #endif
       /*try:*/ {
 
         /* "pybitset/backends/cython/_bitset.pyx":158
  *         cdef size_t ret
@@ -4664,53 +6882,110 @@
   /* function exit code */
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_45intersection_count(PyObject *__pyx_v_self, PyObject *__pyx_v_b2); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_44intersection_count[] = "BitSet.intersection_count(self, BitSet b2) -> size_t";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_45intersection_count(PyObject *__pyx_v_self, PyObject *__pyx_v_b2) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_45intersection_count(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_44intersection_count, "BitSet.intersection_count(self, BitSet b2) -> size_t");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_45intersection_count = {"intersection_count", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_45intersection_count, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_44intersection_count};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_45intersection_count(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
+  struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2 = 0;
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("intersection_count (wrapper)", 0);
+  {
+    PyObject **__pyx_pyargnames[] = {&__pyx_n_s_b2,0};
+    PyObject* values[1] = {0};
+    if (__pyx_kwds) {
+      Py_ssize_t kw_args;
+      switch (__pyx_nargs) {
+        case  1: values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+        CYTHON_FALLTHROUGH;
+        case  0: break;
+        default: goto __pyx_L5_argtuple_error;
+      }
+      kw_args = __Pyx_NumKwargs_FASTCALL(__pyx_kwds);
+      switch (__pyx_nargs) {
+        case  0:
+        if (likely((values[0] = __Pyx_GetKwValue_FASTCALL(__pyx_kwds, __pyx_kwvalues, __pyx_n_s_b2)) != 0)) kw_args--;
+        else if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 155, __pyx_L3_error)
+        else goto __pyx_L5_argtuple_error;
+      }
+      if (unlikely(kw_args > 0)) {
+        const Py_ssize_t kwd_pos_args = __pyx_nargs;
+        if (unlikely(__Pyx_ParseOptionalKeywords(__pyx_kwds, __pyx_kwvalues, __pyx_pyargnames, 0, values + 0, kwd_pos_args, "intersection_count") < 0)) __PYX_ERR(0, 155, __pyx_L3_error)
+      }
+    } else if (unlikely(__pyx_nargs != 1)) {
+      goto __pyx_L5_argtuple_error;
+    } else {
+      values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+    }
+    __pyx_v_b2 = ((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)values[0]);
+  }
+  goto __pyx_L4_argument_unpacking_done;
+  __pyx_L5_argtuple_error:;
+  __Pyx_RaiseArgtupleInvalid("intersection_count", 1, 1, 1, __pyx_nargs); __PYX_ERR(0, 155, __pyx_L3_error)
+  __pyx_L3_error:;
+  __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.intersection_count", __pyx_clineno, __pyx_lineno, __pyx_filename);
+  __Pyx_RefNannyFinishContext();
+  return NULL;
+  __pyx_L4_argument_unpacking_done:;
   if (unlikely(!__Pyx_ArgTypeTest(((PyObject *)__pyx_v_b2), __pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet, 1, "b2", 0))) __PYX_ERR(0, 155, __pyx_L1_error)
-  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_44intersection_count(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), ((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_b2));
+  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_44intersection_count(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), __pyx_v_b2);
 
   /* function exit code */
   goto __pyx_L0;
   __pyx_L1_error:;
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_44intersection_count(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
-  PyObject *__pyx_t_1 = NULL;
+  size_t __pyx_t_1;
+  PyObject *__pyx_t_2 = NULL;
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   __Pyx_RefNannySetupContext("intersection_count", 0);
   __Pyx_XDECREF(__pyx_r);
-  __pyx_t_1 = __Pyx_PyInt_FromSize_t(__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_intersection_count(__pyx_v_self, __pyx_v_b2, 1)); if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 155, __pyx_L1_error)
-  __Pyx_GOTREF(__pyx_t_1);
-  __pyx_r = __pyx_t_1;
-  __pyx_t_1 = 0;
+  __pyx_t_1 = __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_intersection_count(__pyx_v_self, __pyx_v_b2, 1); if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 155, __pyx_L1_error)
+  __pyx_t_2 = __Pyx_PyInt_FromSize_t(__pyx_t_1); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 155, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  __pyx_r = __pyx_t_2;
+  __pyx_t_2 = 0;
   goto __pyx_L0;
 
   /* function exit code */
   __pyx_L1_error:;
-  __Pyx_XDECREF(__pyx_t_1);
+  __Pyx_XDECREF(__pyx_t_2);
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.intersection_count", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
@@ -4719,15 +6994,21 @@
  *         return ret
  * 
  *     cpdef inline bint disjoint(self, BitSet b2):             # <<<<<<<<<<<<<<
  *         cdef bint ret
  *         with nogil:
  */
 
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_47disjoint(PyObject *__pyx_v_self, PyObject *__pyx_v_b2); /*proto*/
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_47disjoint(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
 static CYTHON_INLINE int __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_disjoint(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2, CYTHON_UNUSED int __pyx_skip_dispatch) {
   int __pyx_v_ret;
   int __pyx_r;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("disjoint", 0);
 
   /* "pybitset/backends/cython/_bitset.pyx":163
@@ -4736,14 +7017,15 @@
  *         with nogil:             # <<<<<<<<<<<<<<
  *             ret = bitsets_disjoint(self._bitset, b2._bitset)
  *         return ret
  */
   {
       #ifdef WITH_THREAD
       PyThreadState *_save;
+      _save = NULL;
       Py_UNBLOCK_THREADS
       __Pyx_FastGIL_Remember();
       #endif
       /*try:*/ {
 
         /* "pybitset/backends/cython/_bitset.pyx":164
  *         cdef bint ret
@@ -4795,53 +7077,110 @@
   /* function exit code */
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_47disjoint(PyObject *__pyx_v_self, PyObject *__pyx_v_b2); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_46disjoint[] = "BitSet.disjoint(self, BitSet b2) -> bool";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_47disjoint(PyObject *__pyx_v_self, PyObject *__pyx_v_b2) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_47disjoint(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_46disjoint, "BitSet.disjoint(self, BitSet b2) -> bool");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_47disjoint = {"disjoint", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_47disjoint, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_46disjoint};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_47disjoint(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
+  struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2 = 0;
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("disjoint (wrapper)", 0);
+  {
+    PyObject **__pyx_pyargnames[] = {&__pyx_n_s_b2,0};
+    PyObject* values[1] = {0};
+    if (__pyx_kwds) {
+      Py_ssize_t kw_args;
+      switch (__pyx_nargs) {
+        case  1: values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+        CYTHON_FALLTHROUGH;
+        case  0: break;
+        default: goto __pyx_L5_argtuple_error;
+      }
+      kw_args = __Pyx_NumKwargs_FASTCALL(__pyx_kwds);
+      switch (__pyx_nargs) {
+        case  0:
+        if (likely((values[0] = __Pyx_GetKwValue_FASTCALL(__pyx_kwds, __pyx_kwvalues, __pyx_n_s_b2)) != 0)) kw_args--;
+        else if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 161, __pyx_L3_error)
+        else goto __pyx_L5_argtuple_error;
+      }
+      if (unlikely(kw_args > 0)) {
+        const Py_ssize_t kwd_pos_args = __pyx_nargs;
+        if (unlikely(__Pyx_ParseOptionalKeywords(__pyx_kwds, __pyx_kwvalues, __pyx_pyargnames, 0, values + 0, kwd_pos_args, "disjoint") < 0)) __PYX_ERR(0, 161, __pyx_L3_error)
+      }
+    } else if (unlikely(__pyx_nargs != 1)) {
+      goto __pyx_L5_argtuple_error;
+    } else {
+      values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+    }
+    __pyx_v_b2 = ((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)values[0]);
+  }
+  goto __pyx_L4_argument_unpacking_done;
+  __pyx_L5_argtuple_error:;
+  __Pyx_RaiseArgtupleInvalid("disjoint", 1, 1, 1, __pyx_nargs); __PYX_ERR(0, 161, __pyx_L3_error)
+  __pyx_L3_error:;
+  __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.disjoint", __pyx_clineno, __pyx_lineno, __pyx_filename);
+  __Pyx_RefNannyFinishContext();
+  return NULL;
+  __pyx_L4_argument_unpacking_done:;
   if (unlikely(!__Pyx_ArgTypeTest(((PyObject *)__pyx_v_b2), __pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet, 1, "b2", 0))) __PYX_ERR(0, 161, __pyx_L1_error)
-  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_46disjoint(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), ((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_b2));
+  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_46disjoint(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), __pyx_v_b2);
 
   /* function exit code */
   goto __pyx_L0;
   __pyx_L1_error:;
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_46disjoint(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
-  PyObject *__pyx_t_1 = NULL;
+  int __pyx_t_1;
+  PyObject *__pyx_t_2 = NULL;
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   __Pyx_RefNannySetupContext("disjoint", 0);
   __Pyx_XDECREF(__pyx_r);
-  __pyx_t_1 = __Pyx_PyBool_FromLong(__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_disjoint(__pyx_v_self, __pyx_v_b2, 1)); if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 161, __pyx_L1_error)
-  __Pyx_GOTREF(__pyx_t_1);
-  __pyx_r = __pyx_t_1;
-  __pyx_t_1 = 0;
+  __pyx_t_1 = __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_disjoint(__pyx_v_self, __pyx_v_b2, 1); if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 161, __pyx_L1_error)
+  __pyx_t_2 = __Pyx_PyBool_FromLong(__pyx_t_1); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 161, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  __pyx_r = __pyx_t_2;
+  __pyx_t_2 = 0;
   goto __pyx_L0;
 
   /* function exit code */
   __pyx_L1_error:;
-  __Pyx_XDECREF(__pyx_t_1);
+  __Pyx_XDECREF(__pyx_t_2);
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.disjoint", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
@@ -4850,15 +7189,21 @@
  *         return ret
  * 
  *     cpdef inline bint intersect(self, BitSet b2):             # <<<<<<<<<<<<<<
  *         cdef bint ret
  *         with nogil:
  */
 
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_49intersect(PyObject *__pyx_v_self, PyObject *__pyx_v_b2); /*proto*/
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_49intersect(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
 static CYTHON_INLINE int __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_intersect(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2, CYTHON_UNUSED int __pyx_skip_dispatch) {
   int __pyx_v_ret;
   int __pyx_r;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("intersect", 0);
 
   /* "pybitset/backends/cython/_bitset.pyx":169
@@ -4867,14 +7212,15 @@
  *         with nogil:             # <<<<<<<<<<<<<<
  *             ret = bitsets_intersect(self._bitset, b2._bitset)
  *         return ret
  */
   {
       #ifdef WITH_THREAD
       PyThreadState *_save;
+      _save = NULL;
       Py_UNBLOCK_THREADS
       __Pyx_FastGIL_Remember();
       #endif
       /*try:*/ {
 
         /* "pybitset/backends/cython/_bitset.pyx":170
  *         cdef bint ret
@@ -4926,53 +7272,110 @@
   /* function exit code */
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_49intersect(PyObject *__pyx_v_self, PyObject *__pyx_v_b2); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_48intersect[] = "BitSet.intersect(self, BitSet b2) -> bool";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_49intersect(PyObject *__pyx_v_self, PyObject *__pyx_v_b2) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_49intersect(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_48intersect, "BitSet.intersect(self, BitSet b2) -> bool");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_49intersect = {"intersect", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_49intersect, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_48intersect};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_49intersect(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
+  struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2 = 0;
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("intersect (wrapper)", 0);
+  {
+    PyObject **__pyx_pyargnames[] = {&__pyx_n_s_b2,0};
+    PyObject* values[1] = {0};
+    if (__pyx_kwds) {
+      Py_ssize_t kw_args;
+      switch (__pyx_nargs) {
+        case  1: values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+        CYTHON_FALLTHROUGH;
+        case  0: break;
+        default: goto __pyx_L5_argtuple_error;
+      }
+      kw_args = __Pyx_NumKwargs_FASTCALL(__pyx_kwds);
+      switch (__pyx_nargs) {
+        case  0:
+        if (likely((values[0] = __Pyx_GetKwValue_FASTCALL(__pyx_kwds, __pyx_kwvalues, __pyx_n_s_b2)) != 0)) kw_args--;
+        else if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 167, __pyx_L3_error)
+        else goto __pyx_L5_argtuple_error;
+      }
+      if (unlikely(kw_args > 0)) {
+        const Py_ssize_t kwd_pos_args = __pyx_nargs;
+        if (unlikely(__Pyx_ParseOptionalKeywords(__pyx_kwds, __pyx_kwvalues, __pyx_pyargnames, 0, values + 0, kwd_pos_args, "intersect") < 0)) __PYX_ERR(0, 167, __pyx_L3_error)
+      }
+    } else if (unlikely(__pyx_nargs != 1)) {
+      goto __pyx_L5_argtuple_error;
+    } else {
+      values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+    }
+    __pyx_v_b2 = ((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)values[0]);
+  }
+  goto __pyx_L4_argument_unpacking_done;
+  __pyx_L5_argtuple_error:;
+  __Pyx_RaiseArgtupleInvalid("intersect", 1, 1, 1, __pyx_nargs); __PYX_ERR(0, 167, __pyx_L3_error)
+  __pyx_L3_error:;
+  __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.intersect", __pyx_clineno, __pyx_lineno, __pyx_filename);
+  __Pyx_RefNannyFinishContext();
+  return NULL;
+  __pyx_L4_argument_unpacking_done:;
   if (unlikely(!__Pyx_ArgTypeTest(((PyObject *)__pyx_v_b2), __pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet, 1, "b2", 0))) __PYX_ERR(0, 167, __pyx_L1_error)
-  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_48intersect(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), ((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_b2));
+  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_48intersect(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), __pyx_v_b2);
 
   /* function exit code */
   goto __pyx_L0;
   __pyx_L1_error:;
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_48intersect(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
-  PyObject *__pyx_t_1 = NULL;
+  int __pyx_t_1;
+  PyObject *__pyx_t_2 = NULL;
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   __Pyx_RefNannySetupContext("intersect", 0);
   __Pyx_XDECREF(__pyx_r);
-  __pyx_t_1 = __Pyx_PyBool_FromLong(__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_intersect(__pyx_v_self, __pyx_v_b2, 1)); if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 167, __pyx_L1_error)
-  __Pyx_GOTREF(__pyx_t_1);
-  __pyx_r = __pyx_t_1;
-  __pyx_t_1 = 0;
+  __pyx_t_1 = __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_intersect(__pyx_v_self, __pyx_v_b2, 1); if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 167, __pyx_L1_error)
+  __pyx_t_2 = __Pyx_PyBool_FromLong(__pyx_t_1); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 167, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  __pyx_r = __pyx_t_2;
+  __pyx_t_2 = 0;
   goto __pyx_L0;
 
   /* function exit code */
   __pyx_L1_error:;
-  __Pyx_XDECREF(__pyx_t_1);
+  __Pyx_XDECREF(__pyx_t_2);
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.intersect", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
@@ -4981,15 +7384,21 @@
  *         return ret
  * 
  *     cpdef inline bint contains_all(self, BitSet b2):             # <<<<<<<<<<<<<<
  *         cdef bint ret
  *         with nogil:
  */
 
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_51contains_all(PyObject *__pyx_v_self, PyObject *__pyx_v_b2); /*proto*/
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_51contains_all(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
 static CYTHON_INLINE int __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_contains_all(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2, CYTHON_UNUSED int __pyx_skip_dispatch) {
   int __pyx_v_ret;
   int __pyx_r;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("contains_all", 0);
 
   /* "pybitset/backends/cython/_bitset.pyx":175
@@ -4998,14 +7407,15 @@
  *         with nogil:             # <<<<<<<<<<<<<<
  *             ret = bitset_contains_all(self._bitset, b2._bitset)
  *         return ret
  */
   {
       #ifdef WITH_THREAD
       PyThreadState *_save;
+      _save = NULL;
       Py_UNBLOCK_THREADS
       __Pyx_FastGIL_Remember();
       #endif
       /*try:*/ {
 
         /* "pybitset/backends/cython/_bitset.pyx":176
  *         cdef bint ret
@@ -5057,53 +7467,110 @@
   /* function exit code */
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_51contains_all(PyObject *__pyx_v_self, PyObject *__pyx_v_b2); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_50contains_all[] = "BitSet.contains_all(self, BitSet b2) -> bool";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_51contains_all(PyObject *__pyx_v_self, PyObject *__pyx_v_b2) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_51contains_all(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_50contains_all, "BitSet.contains_all(self, BitSet b2) -> bool");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_51contains_all = {"contains_all", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_51contains_all, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_50contains_all};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_51contains_all(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
+  struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2 = 0;
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("contains_all (wrapper)", 0);
+  {
+    PyObject **__pyx_pyargnames[] = {&__pyx_n_s_b2,0};
+    PyObject* values[1] = {0};
+    if (__pyx_kwds) {
+      Py_ssize_t kw_args;
+      switch (__pyx_nargs) {
+        case  1: values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+        CYTHON_FALLTHROUGH;
+        case  0: break;
+        default: goto __pyx_L5_argtuple_error;
+      }
+      kw_args = __Pyx_NumKwargs_FASTCALL(__pyx_kwds);
+      switch (__pyx_nargs) {
+        case  0:
+        if (likely((values[0] = __Pyx_GetKwValue_FASTCALL(__pyx_kwds, __pyx_kwvalues, __pyx_n_s_b2)) != 0)) kw_args--;
+        else if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 173, __pyx_L3_error)
+        else goto __pyx_L5_argtuple_error;
+      }
+      if (unlikely(kw_args > 0)) {
+        const Py_ssize_t kwd_pos_args = __pyx_nargs;
+        if (unlikely(__Pyx_ParseOptionalKeywords(__pyx_kwds, __pyx_kwvalues, __pyx_pyargnames, 0, values + 0, kwd_pos_args, "contains_all") < 0)) __PYX_ERR(0, 173, __pyx_L3_error)
+      }
+    } else if (unlikely(__pyx_nargs != 1)) {
+      goto __pyx_L5_argtuple_error;
+    } else {
+      values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+    }
+    __pyx_v_b2 = ((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)values[0]);
+  }
+  goto __pyx_L4_argument_unpacking_done;
+  __pyx_L5_argtuple_error:;
+  __Pyx_RaiseArgtupleInvalid("contains_all", 1, 1, 1, __pyx_nargs); __PYX_ERR(0, 173, __pyx_L3_error)
+  __pyx_L3_error:;
+  __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.contains_all", __pyx_clineno, __pyx_lineno, __pyx_filename);
+  __Pyx_RefNannyFinishContext();
+  return NULL;
+  __pyx_L4_argument_unpacking_done:;
   if (unlikely(!__Pyx_ArgTypeTest(((PyObject *)__pyx_v_b2), __pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet, 1, "b2", 0))) __PYX_ERR(0, 173, __pyx_L1_error)
-  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_50contains_all(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), ((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_b2));
+  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_50contains_all(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), __pyx_v_b2);
 
   /* function exit code */
   goto __pyx_L0;
   __pyx_L1_error:;
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_50contains_all(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
-  PyObject *__pyx_t_1 = NULL;
+  int __pyx_t_1;
+  PyObject *__pyx_t_2 = NULL;
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   __Pyx_RefNannySetupContext("contains_all", 0);
   __Pyx_XDECREF(__pyx_r);
-  __pyx_t_1 = __Pyx_PyBool_FromLong(__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_contains_all(__pyx_v_self, __pyx_v_b2, 1)); if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 173, __pyx_L1_error)
-  __Pyx_GOTREF(__pyx_t_1);
-  __pyx_r = __pyx_t_1;
-  __pyx_t_1 = 0;
+  __pyx_t_1 = __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_contains_all(__pyx_v_self, __pyx_v_b2, 1); if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 173, __pyx_L1_error)
+  __pyx_t_2 = __Pyx_PyBool_FromLong(__pyx_t_1); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 173, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  __pyx_r = __pyx_t_2;
+  __pyx_t_2 = 0;
   goto __pyx_L0;
 
   /* function exit code */
   __pyx_L1_error:;
-  __Pyx_XDECREF(__pyx_t_1);
+  __Pyx_XDECREF(__pyx_t_2);
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.contains_all", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
@@ -5112,15 +7579,21 @@
  *         return ret
  * 
  *     cpdef inline inplace_difference(self, BitSet b2):             # <<<<<<<<<<<<<<
  *         with nogil:
  *             bitset_inplace_difference(self._bitset, b2._bitset)
  */
 
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_53inplace_difference(PyObject *__pyx_v_self, PyObject *__pyx_v_b2); /*proto*/
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_53inplace_difference(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
 static CYTHON_INLINE PyObject *__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_inplace_difference(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2, CYTHON_UNUSED int __pyx_skip_dispatch) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("inplace_difference", 0);
 
   /* "pybitset/backends/cython/_bitset.pyx":180
  * 
@@ -5128,14 +7601,15 @@
  *         with nogil:             # <<<<<<<<<<<<<<
  *             bitset_inplace_difference(self._bitset, b2._bitset)
  * 
  */
   {
       #ifdef WITH_THREAD
       PyThreadState *_save;
+      _save = NULL;
       Py_UNBLOCK_THREADS
       __Pyx_FastGIL_Remember();
       #endif
       /*try:*/ {
 
         /* "pybitset/backends/cython/_bitset.pyx":181
  *     cpdef inline inplace_difference(self, BitSet b2):
@@ -5178,25 +7652,80 @@
   __pyx_r = Py_None; __Pyx_INCREF(Py_None);
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_53inplace_difference(PyObject *__pyx_v_self, PyObject *__pyx_v_b2); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_52inplace_difference[] = "BitSet.inplace_difference(self, BitSet b2)";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_53inplace_difference(PyObject *__pyx_v_self, PyObject *__pyx_v_b2) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_53inplace_difference(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_52inplace_difference, "BitSet.inplace_difference(self, BitSet b2)");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_53inplace_difference = {"inplace_difference", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_53inplace_difference, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_52inplace_difference};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_53inplace_difference(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
+  struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2 = 0;
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("inplace_difference (wrapper)", 0);
+  {
+    PyObject **__pyx_pyargnames[] = {&__pyx_n_s_b2,0};
+    PyObject* values[1] = {0};
+    if (__pyx_kwds) {
+      Py_ssize_t kw_args;
+      switch (__pyx_nargs) {
+        case  1: values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+        CYTHON_FALLTHROUGH;
+        case  0: break;
+        default: goto __pyx_L5_argtuple_error;
+      }
+      kw_args = __Pyx_NumKwargs_FASTCALL(__pyx_kwds);
+      switch (__pyx_nargs) {
+        case  0:
+        if (likely((values[0] = __Pyx_GetKwValue_FASTCALL(__pyx_kwds, __pyx_kwvalues, __pyx_n_s_b2)) != 0)) kw_args--;
+        else if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 179, __pyx_L3_error)
+        else goto __pyx_L5_argtuple_error;
+      }
+      if (unlikely(kw_args > 0)) {
+        const Py_ssize_t kwd_pos_args = __pyx_nargs;
+        if (unlikely(__Pyx_ParseOptionalKeywords(__pyx_kwds, __pyx_kwvalues, __pyx_pyargnames, 0, values + 0, kwd_pos_args, "inplace_difference") < 0)) __PYX_ERR(0, 179, __pyx_L3_error)
+      }
+    } else if (unlikely(__pyx_nargs != 1)) {
+      goto __pyx_L5_argtuple_error;
+    } else {
+      values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+    }
+    __pyx_v_b2 = ((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)values[0]);
+  }
+  goto __pyx_L4_argument_unpacking_done;
+  __pyx_L5_argtuple_error:;
+  __Pyx_RaiseArgtupleInvalid("inplace_difference", 1, 1, 1, __pyx_nargs); __PYX_ERR(0, 179, __pyx_L3_error)
+  __pyx_L3_error:;
+  __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.inplace_difference", __pyx_clineno, __pyx_lineno, __pyx_filename);
+  __Pyx_RefNannyFinishContext();
+  return NULL;
+  __pyx_L4_argument_unpacking_done:;
   if (unlikely(!__Pyx_ArgTypeTest(((PyObject *)__pyx_v_b2), __pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet, 1, "b2", 0))) __PYX_ERR(0, 179, __pyx_L1_error)
-  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_52inplace_difference(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), ((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_b2));
+  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_52inplace_difference(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), __pyx_v_b2);
 
   /* function exit code */
   goto __pyx_L0;
   __pyx_L1_error:;
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
@@ -5233,15 +7762,21 @@
  *             bitset_inplace_difference(self._bitset, b2._bitset)
  * 
  *     cpdef inline size_t difference_count(self, BitSet b2):             # <<<<<<<<<<<<<<
  *         cdef size_t ret
  *         with nogil:
  */
 
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_55difference_count(PyObject *__pyx_v_self, PyObject *__pyx_v_b2); /*proto*/
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_55difference_count(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
 static CYTHON_INLINE size_t __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_difference_count(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2, CYTHON_UNUSED int __pyx_skip_dispatch) {
   size_t __pyx_v_ret;
   size_t __pyx_r;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("difference_count", 0);
 
   /* "pybitset/backends/cython/_bitset.pyx":185
@@ -5250,14 +7785,15 @@
  *         with nogil:             # <<<<<<<<<<<<<<
  *             ret = bitset_difference_count(self._bitset, b2._bitset)
  *         return ret
  */
   {
       #ifdef WITH_THREAD
       PyThreadState *_save;
+      _save = NULL;
       Py_UNBLOCK_THREADS
       __Pyx_FastGIL_Remember();
       #endif
       /*try:*/ {
 
         /* "pybitset/backends/cython/_bitset.pyx":186
  *         cdef size_t ret
@@ -5309,53 +7845,110 @@
   /* function exit code */
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_55difference_count(PyObject *__pyx_v_self, PyObject *__pyx_v_b2); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_54difference_count[] = "BitSet.difference_count(self, BitSet b2) -> size_t";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_55difference_count(PyObject *__pyx_v_self, PyObject *__pyx_v_b2) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_55difference_count(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_54difference_count, "BitSet.difference_count(self, BitSet b2) -> size_t");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_55difference_count = {"difference_count", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_55difference_count, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_54difference_count};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_55difference_count(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
+  struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2 = 0;
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("difference_count (wrapper)", 0);
+  {
+    PyObject **__pyx_pyargnames[] = {&__pyx_n_s_b2,0};
+    PyObject* values[1] = {0};
+    if (__pyx_kwds) {
+      Py_ssize_t kw_args;
+      switch (__pyx_nargs) {
+        case  1: values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+        CYTHON_FALLTHROUGH;
+        case  0: break;
+        default: goto __pyx_L5_argtuple_error;
+      }
+      kw_args = __Pyx_NumKwargs_FASTCALL(__pyx_kwds);
+      switch (__pyx_nargs) {
+        case  0:
+        if (likely((values[0] = __Pyx_GetKwValue_FASTCALL(__pyx_kwds, __pyx_kwvalues, __pyx_n_s_b2)) != 0)) kw_args--;
+        else if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 183, __pyx_L3_error)
+        else goto __pyx_L5_argtuple_error;
+      }
+      if (unlikely(kw_args > 0)) {
+        const Py_ssize_t kwd_pos_args = __pyx_nargs;
+        if (unlikely(__Pyx_ParseOptionalKeywords(__pyx_kwds, __pyx_kwvalues, __pyx_pyargnames, 0, values + 0, kwd_pos_args, "difference_count") < 0)) __PYX_ERR(0, 183, __pyx_L3_error)
+      }
+    } else if (unlikely(__pyx_nargs != 1)) {
+      goto __pyx_L5_argtuple_error;
+    } else {
+      values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+    }
+    __pyx_v_b2 = ((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)values[0]);
+  }
+  goto __pyx_L4_argument_unpacking_done;
+  __pyx_L5_argtuple_error:;
+  __Pyx_RaiseArgtupleInvalid("difference_count", 1, 1, 1, __pyx_nargs); __PYX_ERR(0, 183, __pyx_L3_error)
+  __pyx_L3_error:;
+  __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.difference_count", __pyx_clineno, __pyx_lineno, __pyx_filename);
+  __Pyx_RefNannyFinishContext();
+  return NULL;
+  __pyx_L4_argument_unpacking_done:;
   if (unlikely(!__Pyx_ArgTypeTest(((PyObject *)__pyx_v_b2), __pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet, 1, "b2", 0))) __PYX_ERR(0, 183, __pyx_L1_error)
-  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_54difference_count(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), ((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_b2));
+  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_54difference_count(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), __pyx_v_b2);
 
   /* function exit code */
   goto __pyx_L0;
   __pyx_L1_error:;
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_54difference_count(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
-  PyObject *__pyx_t_1 = NULL;
+  size_t __pyx_t_1;
+  PyObject *__pyx_t_2 = NULL;
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   __Pyx_RefNannySetupContext("difference_count", 0);
   __Pyx_XDECREF(__pyx_r);
-  __pyx_t_1 = __Pyx_PyInt_FromSize_t(__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_difference_count(__pyx_v_self, __pyx_v_b2, 1)); if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 183, __pyx_L1_error)
-  __Pyx_GOTREF(__pyx_t_1);
-  __pyx_r = __pyx_t_1;
-  __pyx_t_1 = 0;
+  __pyx_t_1 = __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_difference_count(__pyx_v_self, __pyx_v_b2, 1); if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 183, __pyx_L1_error)
+  __pyx_t_2 = __Pyx_PyInt_FromSize_t(__pyx_t_1); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 183, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  __pyx_r = __pyx_t_2;
+  __pyx_t_2 = 0;
   goto __pyx_L0;
 
   /* function exit code */
   __pyx_L1_error:;
-  __Pyx_XDECREF(__pyx_t_1);
+  __Pyx_XDECREF(__pyx_t_2);
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.difference_count", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
@@ -5364,15 +7957,21 @@
  *         return ret
  * 
  *     cpdef inline bint inplace_symmetric_difference(self, BitSet b2):             # <<<<<<<<<<<<<<
  *         cdef bint ret
  *         with nogil:
  */
 
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_57inplace_symmetric_difference(PyObject *__pyx_v_self, PyObject *__pyx_v_b2); /*proto*/
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_57inplace_symmetric_difference(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
 static CYTHON_INLINE int __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_inplace_symmetric_difference(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2, CYTHON_UNUSED int __pyx_skip_dispatch) {
   int __pyx_v_ret;
   int __pyx_r;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("inplace_symmetric_difference", 0);
 
   /* "pybitset/backends/cython/_bitset.pyx":191
@@ -5381,14 +7980,15 @@
  *         with nogil:             # <<<<<<<<<<<<<<
  *             ret = bitset_inplace_symmetric_difference(self._bitset, b2._bitset)
  *         return ret
  */
   {
       #ifdef WITH_THREAD
       PyThreadState *_save;
+      _save = NULL;
       Py_UNBLOCK_THREADS
       __Pyx_FastGIL_Remember();
       #endif
       /*try:*/ {
 
         /* "pybitset/backends/cython/_bitset.pyx":192
  *         cdef bint ret
@@ -5440,53 +8040,110 @@
   /* function exit code */
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_57inplace_symmetric_difference(PyObject *__pyx_v_self, PyObject *__pyx_v_b2); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_56inplace_symmetric_difference[] = "BitSet.inplace_symmetric_difference(self, BitSet b2) -> bool";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_57inplace_symmetric_difference(PyObject *__pyx_v_self, PyObject *__pyx_v_b2) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_57inplace_symmetric_difference(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_56inplace_symmetric_difference, "BitSet.inplace_symmetric_difference(self, BitSet b2) -> bool");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_57inplace_symmetric_difference = {"inplace_symmetric_difference", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_57inplace_symmetric_difference, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_56inplace_symmetric_difference};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_57inplace_symmetric_difference(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
+  struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2 = 0;
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("inplace_symmetric_difference (wrapper)", 0);
+  {
+    PyObject **__pyx_pyargnames[] = {&__pyx_n_s_b2,0};
+    PyObject* values[1] = {0};
+    if (__pyx_kwds) {
+      Py_ssize_t kw_args;
+      switch (__pyx_nargs) {
+        case  1: values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+        CYTHON_FALLTHROUGH;
+        case  0: break;
+        default: goto __pyx_L5_argtuple_error;
+      }
+      kw_args = __Pyx_NumKwargs_FASTCALL(__pyx_kwds);
+      switch (__pyx_nargs) {
+        case  0:
+        if (likely((values[0] = __Pyx_GetKwValue_FASTCALL(__pyx_kwds, __pyx_kwvalues, __pyx_n_s_b2)) != 0)) kw_args--;
+        else if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 189, __pyx_L3_error)
+        else goto __pyx_L5_argtuple_error;
+      }
+      if (unlikely(kw_args > 0)) {
+        const Py_ssize_t kwd_pos_args = __pyx_nargs;
+        if (unlikely(__Pyx_ParseOptionalKeywords(__pyx_kwds, __pyx_kwvalues, __pyx_pyargnames, 0, values + 0, kwd_pos_args, "inplace_symmetric_difference") < 0)) __PYX_ERR(0, 189, __pyx_L3_error)
+      }
+    } else if (unlikely(__pyx_nargs != 1)) {
+      goto __pyx_L5_argtuple_error;
+    } else {
+      values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+    }
+    __pyx_v_b2 = ((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)values[0]);
+  }
+  goto __pyx_L4_argument_unpacking_done;
+  __pyx_L5_argtuple_error:;
+  __Pyx_RaiseArgtupleInvalid("inplace_symmetric_difference", 1, 1, 1, __pyx_nargs); __PYX_ERR(0, 189, __pyx_L3_error)
+  __pyx_L3_error:;
+  __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.inplace_symmetric_difference", __pyx_clineno, __pyx_lineno, __pyx_filename);
+  __Pyx_RefNannyFinishContext();
+  return NULL;
+  __pyx_L4_argument_unpacking_done:;
   if (unlikely(!__Pyx_ArgTypeTest(((PyObject *)__pyx_v_b2), __pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet, 1, "b2", 0))) __PYX_ERR(0, 189, __pyx_L1_error)
-  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_56inplace_symmetric_difference(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), ((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_b2));
+  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_56inplace_symmetric_difference(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), __pyx_v_b2);
 
   /* function exit code */
   goto __pyx_L0;
   __pyx_L1_error:;
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_56inplace_symmetric_difference(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
-  PyObject *__pyx_t_1 = NULL;
+  int __pyx_t_1;
+  PyObject *__pyx_t_2 = NULL;
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   __Pyx_RefNannySetupContext("inplace_symmetric_difference", 0);
   __Pyx_XDECREF(__pyx_r);
-  __pyx_t_1 = __Pyx_PyBool_FromLong(__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_inplace_symmetric_difference(__pyx_v_self, __pyx_v_b2, 1)); if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 189, __pyx_L1_error)
-  __Pyx_GOTREF(__pyx_t_1);
-  __pyx_r = __pyx_t_1;
-  __pyx_t_1 = 0;
+  __pyx_t_1 = __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_inplace_symmetric_difference(__pyx_v_self, __pyx_v_b2, 1); if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 189, __pyx_L1_error)
+  __pyx_t_2 = __Pyx_PyBool_FromLong(__pyx_t_1); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 189, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  __pyx_r = __pyx_t_2;
+  __pyx_t_2 = 0;
   goto __pyx_L0;
 
   /* function exit code */
   __pyx_L1_error:;
-  __Pyx_XDECREF(__pyx_t_1);
+  __Pyx_XDECREF(__pyx_t_2);
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.inplace_symmetric_difference", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
@@ -5495,15 +8152,21 @@
  *         return ret
  * 
  *     cpdef inline size_t symmetric_difference_count(self, BitSet b2):             # <<<<<<<<<<<<<<
  *         cdef size_t ret
  *         with nogil:
  */
 
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_59symmetric_difference_count(PyObject *__pyx_v_self, PyObject *__pyx_v_b2); /*proto*/
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_59symmetric_difference_count(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
 static CYTHON_INLINE size_t __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_symmetric_difference_count(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2, CYTHON_UNUSED int __pyx_skip_dispatch) {
   size_t __pyx_v_ret;
   size_t __pyx_r;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("symmetric_difference_count", 0);
 
   /* "pybitset/backends/cython/_bitset.pyx":197
@@ -5512,14 +8175,15 @@
  *         with nogil:             # <<<<<<<<<<<<<<
  *             ret = bitset_symmetric_difference_count(self._bitset,  b2._bitset)
  *         return ret
  */
   {
       #ifdef WITH_THREAD
       PyThreadState *_save;
+      _save = NULL;
       Py_UNBLOCK_THREADS
       __Pyx_FastGIL_Remember();
       #endif
       /*try:*/ {
 
         /* "pybitset/backends/cython/_bitset.pyx":198
  *         cdef size_t ret
@@ -5571,53 +8235,110 @@
   /* function exit code */
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_59symmetric_difference_count(PyObject *__pyx_v_self, PyObject *__pyx_v_b2); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_58symmetric_difference_count[] = "BitSet.symmetric_difference_count(self, BitSet b2) -> size_t";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_59symmetric_difference_count(PyObject *__pyx_v_self, PyObject *__pyx_v_b2) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_59symmetric_difference_count(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_58symmetric_difference_count, "BitSet.symmetric_difference_count(self, BitSet b2) -> size_t");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_59symmetric_difference_count = {"symmetric_difference_count", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_59symmetric_difference_count, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_58symmetric_difference_count};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_59symmetric_difference_count(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
+  struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2 = 0;
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("symmetric_difference_count (wrapper)", 0);
+  {
+    PyObject **__pyx_pyargnames[] = {&__pyx_n_s_b2,0};
+    PyObject* values[1] = {0};
+    if (__pyx_kwds) {
+      Py_ssize_t kw_args;
+      switch (__pyx_nargs) {
+        case  1: values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+        CYTHON_FALLTHROUGH;
+        case  0: break;
+        default: goto __pyx_L5_argtuple_error;
+      }
+      kw_args = __Pyx_NumKwargs_FASTCALL(__pyx_kwds);
+      switch (__pyx_nargs) {
+        case  0:
+        if (likely((values[0] = __Pyx_GetKwValue_FASTCALL(__pyx_kwds, __pyx_kwvalues, __pyx_n_s_b2)) != 0)) kw_args--;
+        else if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 195, __pyx_L3_error)
+        else goto __pyx_L5_argtuple_error;
+      }
+      if (unlikely(kw_args > 0)) {
+        const Py_ssize_t kwd_pos_args = __pyx_nargs;
+        if (unlikely(__Pyx_ParseOptionalKeywords(__pyx_kwds, __pyx_kwvalues, __pyx_pyargnames, 0, values + 0, kwd_pos_args, "symmetric_difference_count") < 0)) __PYX_ERR(0, 195, __pyx_L3_error)
+      }
+    } else if (unlikely(__pyx_nargs != 1)) {
+      goto __pyx_L5_argtuple_error;
+    } else {
+      values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+    }
+    __pyx_v_b2 = ((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)values[0]);
+  }
+  goto __pyx_L4_argument_unpacking_done;
+  __pyx_L5_argtuple_error:;
+  __Pyx_RaiseArgtupleInvalid("symmetric_difference_count", 1, 1, 1, __pyx_nargs); __PYX_ERR(0, 195, __pyx_L3_error)
+  __pyx_L3_error:;
+  __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.symmetric_difference_count", __pyx_clineno, __pyx_lineno, __pyx_filename);
+  __Pyx_RefNannyFinishContext();
+  return NULL;
+  __pyx_L4_argument_unpacking_done:;
   if (unlikely(!__Pyx_ArgTypeTest(((PyObject *)__pyx_v_b2), __pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet, 1, "b2", 0))) __PYX_ERR(0, 195, __pyx_L1_error)
-  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_58symmetric_difference_count(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), ((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_b2));
+  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_58symmetric_difference_count(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), __pyx_v_b2);
 
   /* function exit code */
   goto __pyx_L0;
   __pyx_L1_error:;
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_58symmetric_difference_count(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b2) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
-  PyObject *__pyx_t_1 = NULL;
+  size_t __pyx_t_1;
+  PyObject *__pyx_t_2 = NULL;
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   __Pyx_RefNannySetupContext("symmetric_difference_count", 0);
   __Pyx_XDECREF(__pyx_r);
-  __pyx_t_1 = __Pyx_PyInt_FromSize_t(__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_symmetric_difference_count(__pyx_v_self, __pyx_v_b2, 1)); if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 195, __pyx_L1_error)
-  __Pyx_GOTREF(__pyx_t_1);
-  __pyx_r = __pyx_t_1;
-  __pyx_t_1 = 0;
+  __pyx_t_1 = __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_symmetric_difference_count(__pyx_v_self, __pyx_v_b2, 1); if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 195, __pyx_L1_error)
+  __pyx_t_2 = __Pyx_PyInt_FromSize_t(__pyx_t_1); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 195, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  __pyx_r = __pyx_t_2;
+  __pyx_t_2 = 0;
   goto __pyx_L0;
 
   /* function exit code */
   __pyx_L1_error:;
-  __Pyx_XDECREF(__pyx_t_1);
+  __Pyx_XDECREF(__pyx_t_2);
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.symmetric_difference_count", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
@@ -5629,14 +8350,15 @@
  *         return BitSetIter(self)
  * 
  */
 
 /* Python wrapper */
 static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_61__iter__(PyObject *__pyx_v_self); /*proto*/
 static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_61__iter__(PyObject *__pyx_v_self) {
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_VARARGS(__pyx_args, __pyx_nargs);
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("__iter__ (wrapper)", 0);
   __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_60__iter__(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self));
 
   /* function exit code */
   __Pyx_RefNannyFinishContext();
@@ -5689,15 +8411,21 @@
  *         return BitSetIter(self)
  * 
  *     cpdef inline bint for_each(self, object func):             # <<<<<<<<<<<<<<
  *         cdef bint ret
  *         with nogil:
  */
 
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_63for_each(PyObject *__pyx_v_self, PyObject *__pyx_v_func); /*proto*/
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_63for_each(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
 static CYTHON_INLINE int __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_for_each(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, PyObject *__pyx_v_func, CYTHON_UNUSED int __pyx_skip_dispatch) {
   int __pyx_v_ret;
   int __pyx_r;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("for_each", 0);
 
   /* "pybitset/backends/cython/_bitset.pyx":206
@@ -5706,14 +8434,15 @@
  *         with nogil:             # <<<<<<<<<<<<<<
  *             ret = bitset_for_each(self._bitset, bitset_iterator_func, <void*>func)
  *         return ret
  */
   {
       #ifdef WITH_THREAD
       PyThreadState *_save;
+      _save = NULL;
       Py_UNBLOCK_THREADS
       __Pyx_FastGIL_Remember();
       #endif
       /*try:*/ {
 
         /* "pybitset/backends/cython/_bitset.pyx":207
  *         cdef bint ret
@@ -5765,45 +8494,105 @@
   /* function exit code */
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_63for_each(PyObject *__pyx_v_self, PyObject *__pyx_v_func); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_62for_each[] = "BitSet.for_each(self, func) -> bool";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_63for_each(PyObject *__pyx_v_self, PyObject *__pyx_v_func) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_63for_each(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_62for_each, "BitSet.for_each(self, func) -> bool");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_63for_each = {"for_each", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_63for_each, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_62for_each};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_63for_each(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
+  PyObject *__pyx_v_func = 0;
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
+  int __pyx_lineno = 0;
+  const char *__pyx_filename = NULL;
+  int __pyx_clineno = 0;
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("for_each (wrapper)", 0);
-  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_62for_each(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), ((PyObject *)__pyx_v_func));
+  {
+    PyObject **__pyx_pyargnames[] = {&__pyx_n_s_func,0};
+    PyObject* values[1] = {0};
+    if (__pyx_kwds) {
+      Py_ssize_t kw_args;
+      switch (__pyx_nargs) {
+        case  1: values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+        CYTHON_FALLTHROUGH;
+        case  0: break;
+        default: goto __pyx_L5_argtuple_error;
+      }
+      kw_args = __Pyx_NumKwargs_FASTCALL(__pyx_kwds);
+      switch (__pyx_nargs) {
+        case  0:
+        if (likely((values[0] = __Pyx_GetKwValue_FASTCALL(__pyx_kwds, __pyx_kwvalues, __pyx_n_s_func)) != 0)) kw_args--;
+        else if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 204, __pyx_L3_error)
+        else goto __pyx_L5_argtuple_error;
+      }
+      if (unlikely(kw_args > 0)) {
+        const Py_ssize_t kwd_pos_args = __pyx_nargs;
+        if (unlikely(__Pyx_ParseOptionalKeywords(__pyx_kwds, __pyx_kwvalues, __pyx_pyargnames, 0, values + 0, kwd_pos_args, "for_each") < 0)) __PYX_ERR(0, 204, __pyx_L3_error)
+      }
+    } else if (unlikely(__pyx_nargs != 1)) {
+      goto __pyx_L5_argtuple_error;
+    } else {
+      values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+    }
+    __pyx_v_func = values[0];
+  }
+  goto __pyx_L4_argument_unpacking_done;
+  __pyx_L5_argtuple_error:;
+  __Pyx_RaiseArgtupleInvalid("for_each", 1, 1, 1, __pyx_nargs); __PYX_ERR(0, 204, __pyx_L3_error)
+  __pyx_L3_error:;
+  __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.for_each", __pyx_clineno, __pyx_lineno, __pyx_filename);
+  __Pyx_RefNannyFinishContext();
+  return NULL;
+  __pyx_L4_argument_unpacking_done:;
+  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_62for_each(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), __pyx_v_func);
 
   /* function exit code */
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_62for_each(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, PyObject *__pyx_v_func) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
-  PyObject *__pyx_t_1 = NULL;
+  int __pyx_t_1;
+  PyObject *__pyx_t_2 = NULL;
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   __Pyx_RefNannySetupContext("for_each", 0);
   __Pyx_XDECREF(__pyx_r);
-  __pyx_t_1 = __Pyx_PyBool_FromLong(__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_for_each(__pyx_v_self, __pyx_v_func, 1)); if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 204, __pyx_L1_error)
-  __Pyx_GOTREF(__pyx_t_1);
-  __pyx_r = __pyx_t_1;
-  __pyx_t_1 = 0;
+  __pyx_t_1 = __pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_for_each(__pyx_v_self, __pyx_v_func, 1); if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 204, __pyx_L1_error)
+  __pyx_t_2 = __Pyx_PyBool_FromLong(__pyx_t_1); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 204, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  __pyx_r = __pyx_t_2;
+  __pyx_t_2 = 0;
   goto __pyx_L0;
 
   /* function exit code */
   __pyx_L1_error:;
-  __Pyx_XDECREF(__pyx_t_1);
+  __Pyx_XDECREF(__pyx_t_2);
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.for_each", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
@@ -5812,15 +8601,21 @@
  *         return ret
  * 
  *     cpdef inline print(self):             # <<<<<<<<<<<<<<
  *         with nogil:
  *             bitset_print(self._bitset)
  */
 
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_65print(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused); /*proto*/
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_65print(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
 static CYTHON_INLINE PyObject *__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_print(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, CYTHON_UNUSED int __pyx_skip_dispatch) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("print", 0);
 
   /* "pybitset/backends/cython/_bitset.pyx":211
  * 
@@ -5828,14 +8623,15 @@
  *         with nogil:             # <<<<<<<<<<<<<<
  *             bitset_print(self._bitset)
  * 
  */
   {
       #ifdef WITH_THREAD
       PyThreadState *_save;
+      _save = NULL;
       Py_UNBLOCK_THREADS
       __Pyx_FastGIL_Remember();
       #endif
       /*try:*/ {
 
         /* "pybitset/backends/cython/_bitset.pyx":212
  *     cpdef inline print(self):
@@ -5878,20 +8674,40 @@
   __pyx_r = Py_None; __Pyx_INCREF(Py_None);
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_65print(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_64print[] = "BitSet.print(self)";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_65print(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_65print(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_64print, "BitSet.print(self)");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_65print = {"print", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_65print, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_64print};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_65print(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("print (wrapper)", 0);
+  if (unlikely(__pyx_nargs > 0)) {
+    __Pyx_RaiseArgtupleInvalid("print", 1, 0, 0, __pyx_nargs); return NULL;}
+  if (unlikely(__pyx_kwds) && __Pyx_NumKwargs_FASTCALL(__pyx_kwds) && unlikely(!__Pyx_CheckKeywordStrings(__pyx_kwds, "print", 0))) return NULL;
   __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_64print(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self));
 
   /* function exit code */
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
@@ -5919,120 +8735,188 @@
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* "(tree fragment)":1
  * def __reduce_cython__(self):             # <<<<<<<<<<<<<<
- *     raise TypeError("no default __reduce__ due to non-trivial __cinit__")
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"
  * def __setstate_cython__(self, __pyx_state):
  */
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_67__reduce_cython__(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_66__reduce_cython__[] = "BitSet.__reduce_cython__(self)";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_67__reduce_cython__(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_67__reduce_cython__(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_66__reduce_cython__, "BitSet.__reduce_cython__(self)");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_67__reduce_cython__ = {"__reduce_cython__", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_67__reduce_cython__, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_66__reduce_cython__};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_67__reduce_cython__(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("__reduce_cython__ (wrapper)", 0);
+  if (unlikely(__pyx_nargs > 0)) {
+    __Pyx_RaiseArgtupleInvalid("__reduce_cython__", 1, 0, 0, __pyx_nargs); return NULL;}
+  if (unlikely(__pyx_kwds) && __Pyx_NumKwargs_FASTCALL(__pyx_kwds) && unlikely(!__Pyx_CheckKeywordStrings(__pyx_kwds, "__reduce_cython__", 0))) return NULL;
   __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_66__reduce_cython__(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self));
 
   /* function exit code */
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_66__reduce_cython__(CYTHON_UNUSED struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
-  PyObject *__pyx_t_1 = NULL;
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   __Pyx_RefNannySetupContext("__reduce_cython__", 0);
 
   /* "(tree fragment)":2
  * def __reduce_cython__(self):
- *     raise TypeError("no default __reduce__ due to non-trivial __cinit__")             # <<<<<<<<<<<<<<
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"             # <<<<<<<<<<<<<<
  * def __setstate_cython__(self, __pyx_state):
- *     raise TypeError("no default __reduce__ due to non-trivial __cinit__")
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"
  */
-  __pyx_t_1 = __Pyx_PyObject_Call(__pyx_builtin_TypeError, __pyx_tuple_, NULL); if (unlikely(!__pyx_t_1)) __PYX_ERR(1, 2, __pyx_L1_error)
-  __Pyx_GOTREF(__pyx_t_1);
-  __Pyx_Raise(__pyx_t_1, 0, 0, 0);
-  __Pyx_DECREF(__pyx_t_1); __pyx_t_1 = 0;
+  __Pyx_Raise(__pyx_builtin_TypeError, __pyx_kp_s_no_default___reduce___due_to_non, 0, 0);
   __PYX_ERR(1, 2, __pyx_L1_error)
 
   /* "(tree fragment)":1
  * def __reduce_cython__(self):             # <<<<<<<<<<<<<<
- *     raise TypeError("no default __reduce__ due to non-trivial __cinit__")
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"
  * def __setstate_cython__(self, __pyx_state):
  */
 
   /* function exit code */
   __pyx_L1_error:;
-  __Pyx_XDECREF(__pyx_t_1);
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.__reduce_cython__", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __pyx_r = NULL;
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* "(tree fragment)":3
  * def __reduce_cython__(self):
- *     raise TypeError("no default __reduce__ due to non-trivial __cinit__")
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"
  * def __setstate_cython__(self, __pyx_state):             # <<<<<<<<<<<<<<
- *     raise TypeError("no default __reduce__ due to non-trivial __cinit__")
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"
  */
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_69__setstate_cython__(PyObject *__pyx_v_self, PyObject *__pyx_v___pyx_state); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_68__setstate_cython__[] = "BitSet.__setstate_cython__(self, __pyx_state)";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_69__setstate_cython__(PyObject *__pyx_v_self, PyObject *__pyx_v___pyx_state) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_69__setstate_cython__(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_68__setstate_cython__, "BitSet.__setstate_cython__(self, __pyx_state)");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_69__setstate_cython__ = {"__setstate_cython__", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_69__setstate_cython__, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_68__setstate_cython__};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_69__setstate_cython__(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
+  CYTHON_UNUSED PyObject *__pyx_v___pyx_state = 0;
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
+  int __pyx_lineno = 0;
+  const char *__pyx_filename = NULL;
+  int __pyx_clineno = 0;
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("__setstate_cython__ (wrapper)", 0);
-  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_68__setstate_cython__(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), ((PyObject *)__pyx_v___pyx_state));
+  {
+    PyObject **__pyx_pyargnames[] = {&__pyx_n_s_pyx_state,0};
+    PyObject* values[1] = {0};
+    if (__pyx_kwds) {
+      Py_ssize_t kw_args;
+      switch (__pyx_nargs) {
+        case  1: values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+        CYTHON_FALLTHROUGH;
+        case  0: break;
+        default: goto __pyx_L5_argtuple_error;
+      }
+      kw_args = __Pyx_NumKwargs_FASTCALL(__pyx_kwds);
+      switch (__pyx_nargs) {
+        case  0:
+        if (likely((values[0] = __Pyx_GetKwValue_FASTCALL(__pyx_kwds, __pyx_kwvalues, __pyx_n_s_pyx_state)) != 0)) kw_args--;
+        else if (unlikely(PyErr_Occurred())) __PYX_ERR(1, 3, __pyx_L3_error)
+        else goto __pyx_L5_argtuple_error;
+      }
+      if (unlikely(kw_args > 0)) {
+        const Py_ssize_t kwd_pos_args = __pyx_nargs;
+        if (unlikely(__Pyx_ParseOptionalKeywords(__pyx_kwds, __pyx_kwvalues, __pyx_pyargnames, 0, values + 0, kwd_pos_args, "__setstate_cython__") < 0)) __PYX_ERR(1, 3, __pyx_L3_error)
+      }
+    } else if (unlikely(__pyx_nargs != 1)) {
+      goto __pyx_L5_argtuple_error;
+    } else {
+      values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+    }
+    __pyx_v___pyx_state = values[0];
+  }
+  goto __pyx_L4_argument_unpacking_done;
+  __pyx_L5_argtuple_error:;
+  __Pyx_RaiseArgtupleInvalid("__setstate_cython__", 1, 1, 1, __pyx_nargs); __PYX_ERR(1, 3, __pyx_L3_error)
+  __pyx_L3_error:;
+  __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.__setstate_cython__", __pyx_clineno, __pyx_lineno, __pyx_filename);
+  __Pyx_RefNannyFinishContext();
+  return NULL;
+  __pyx_L4_argument_unpacking_done:;
+  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_68__setstate_cython__(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)__pyx_v_self), __pyx_v___pyx_state);
 
   /* function exit code */
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_6BitSet_68__setstate_cython__(CYTHON_UNUSED struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_self, CYTHON_UNUSED PyObject *__pyx_v___pyx_state) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
-  PyObject *__pyx_t_1 = NULL;
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   __Pyx_RefNannySetupContext("__setstate_cython__", 0);
 
   /* "(tree fragment)":4
- *     raise TypeError("no default __reduce__ due to non-trivial __cinit__")
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"
  * def __setstate_cython__(self, __pyx_state):
- *     raise TypeError("no default __reduce__ due to non-trivial __cinit__")             # <<<<<<<<<<<<<<
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"             # <<<<<<<<<<<<<<
  */
-  __pyx_t_1 = __Pyx_PyObject_Call(__pyx_builtin_TypeError, __pyx_tuple__2, NULL); if (unlikely(!__pyx_t_1)) __PYX_ERR(1, 4, __pyx_L1_error)
-  __Pyx_GOTREF(__pyx_t_1);
-  __Pyx_Raise(__pyx_t_1, 0, 0, 0);
-  __Pyx_DECREF(__pyx_t_1); __pyx_t_1 = 0;
+  __Pyx_Raise(__pyx_builtin_TypeError, __pyx_kp_s_no_default___reduce___due_to_non, 0, 0);
   __PYX_ERR(1, 4, __pyx_L1_error)
 
   /* "(tree fragment)":3
  * def __reduce_cython__(self):
- *     raise TypeError("no default __reduce__ due to non-trivial __cinit__")
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"
  * def __setstate_cython__(self, __pyx_state):             # <<<<<<<<<<<<<<
- *     raise TypeError("no default __reduce__ due to non-trivial __cinit__")
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"
  */
 
   /* function exit code */
   __pyx_L1_error:;
-  __Pyx_XDECREF(__pyx_t_1);
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSet.__setstate_cython__", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __pyx_r = NULL;
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
@@ -6044,51 +8928,54 @@
  *         self.i = 0
  */
 
 /* Python wrapper */
 static int __pyx_pw_8pybitset_8backends_6cython_7_bitset_10BitSetIter_1__cinit__(PyObject *__pyx_v_self, PyObject *__pyx_args, PyObject *__pyx_kwds); /*proto*/
 static int __pyx_pw_8pybitset_8backends_6cython_7_bitset_10BitSetIter_1__cinit__(PyObject *__pyx_v_self, PyObject *__pyx_args, PyObject *__pyx_kwds) {
   struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_v_b = 0;
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_VARARGS(__pyx_args, __pyx_nargs);
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   int __pyx_r;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("__cinit__ (wrapper)", 0);
   {
-    static PyObject **__pyx_pyargnames[] = {&__pyx_n_s_b,0};
+    PyObject **__pyx_pyargnames[] = {&__pyx_n_s_b,0};
     PyObject* values[1] = {0};
-    if (unlikely(__pyx_kwds)) {
+    if (__pyx_kwds) {
       Py_ssize_t kw_args;
-      const Py_ssize_t pos_args = PyTuple_GET_SIZE(__pyx_args);
-      switch (pos_args) {
-        case  1: values[0] = PyTuple_GET_ITEM(__pyx_args, 0);
+      switch (__pyx_nargs) {
+        case  1: values[0] = __Pyx_Arg_VARARGS(__pyx_args, 0);
         CYTHON_FALLTHROUGH;
         case  0: break;
         default: goto __pyx_L5_argtuple_error;
       }
-      kw_args = PyDict_Size(__pyx_kwds);
-      switch (pos_args) {
+      kw_args = __Pyx_NumKwargs_VARARGS(__pyx_kwds);
+      switch (__pyx_nargs) {
         case  0:
-        if (likely((values[0] = __Pyx_PyDict_GetItemStr(__pyx_kwds, __pyx_n_s_b)) != 0)) kw_args--;
+        if (likely((values[0] = __Pyx_GetKwValue_VARARGS(__pyx_kwds, __pyx_kwvalues, __pyx_n_s_b)) != 0)) kw_args--;
+        else if (unlikely(PyErr_Occurred())) __PYX_ERR(0, 223, __pyx_L3_error)
         else goto __pyx_L5_argtuple_error;
       }
       if (unlikely(kw_args > 0)) {
-        if (unlikely(__Pyx_ParseOptionalKeywords(__pyx_kwds, __pyx_pyargnames, 0, values, pos_args, "__cinit__") < 0)) __PYX_ERR(0, 223, __pyx_L3_error)
+        const Py_ssize_t kwd_pos_args = __pyx_nargs;
+        if (unlikely(__Pyx_ParseOptionalKeywords(__pyx_kwds, __pyx_kwvalues, __pyx_pyargnames, 0, values + 0, kwd_pos_args, "__cinit__") < 0)) __PYX_ERR(0, 223, __pyx_L3_error)
       }
-    } else if (PyTuple_GET_SIZE(__pyx_args) != 1) {
+    } else if (unlikely(__pyx_nargs != 1)) {
       goto __pyx_L5_argtuple_error;
     } else {
-      values[0] = PyTuple_GET_ITEM(__pyx_args, 0);
+      values[0] = __Pyx_Arg_VARARGS(__pyx_args, 0);
     }
     __pyx_v_b = ((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)values[0]);
   }
   goto __pyx_L4_argument_unpacking_done;
   __pyx_L5_argtuple_error:;
-  __Pyx_RaiseArgtupleInvalid("__cinit__", 1, 1, 1, PyTuple_GET_SIZE(__pyx_args)); __PYX_ERR(0, 223, __pyx_L3_error)
+  __Pyx_RaiseArgtupleInvalid("__cinit__", 1, 1, 1, __pyx_nargs); __PYX_ERR(0, 223, __pyx_L3_error)
   __pyx_L3_error:;
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSetIter.__cinit__", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __Pyx_RefNannyFinishContext();
   return -1;
   __pyx_L4_argument_unpacking_done:;
   if (unlikely(!__Pyx_ArgTypeTest(((PyObject *)__pyx_v_b), __pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet, 1, "b", 0))) __PYX_ERR(0, 223, __pyx_L1_error)
   __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_10BitSetIter___cinit__(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSetIter *)__pyx_v_self), __pyx_v_b);
@@ -6110,18 +8997,18 @@
   /* "pybitset/backends/cython/_bitset.pyx":224
  * 
  *     def __cinit__(self, BitSet b):
  *         self.b = b             # <<<<<<<<<<<<<<
  *         self.i = 0
  * 
  */
-  __Pyx_INCREF(((PyObject *)__pyx_v_b));
-  __Pyx_GIVEREF(((PyObject *)__pyx_v_b));
-  __Pyx_GOTREF(__pyx_v_self->b);
-  __Pyx_DECREF(((PyObject *)__pyx_v_self->b));
+  __Pyx_INCREF((PyObject *)__pyx_v_b);
+  __Pyx_GIVEREF((PyObject *)__pyx_v_b);
+  __Pyx_GOTREF((PyObject *)__pyx_v_self->b);
+  __Pyx_DECREF((PyObject *)__pyx_v_self->b);
   __pyx_v_self->b = __pyx_v_b;
 
   /* "pybitset/backends/cython/_bitset.pyx":225
  *     def __cinit__(self, BitSet b):
  *         self.b = b
  *         self.i = 0             # <<<<<<<<<<<<<<
  * 
@@ -6150,14 +9037,15 @@
  *         return self
  * 
  */
 
 /* Python wrapper */
 static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_10BitSetIter_3__iter__(PyObject *__pyx_v_self); /*proto*/
 static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_10BitSetIter_3__iter__(PyObject *__pyx_v_self) {
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_VARARGS(__pyx_args, __pyx_nargs);
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("__iter__ (wrapper)", 0);
   __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_10BitSetIter_2__iter__(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSetIter *)__pyx_v_self));
 
   /* function exit code */
   __Pyx_RefNannyFinishContext();
@@ -6173,15 +9061,15 @@
  * 
  *     def __iter__(self):
  *         return self             # <<<<<<<<<<<<<<
  * 
  *     def __next__(self):
  */
   __Pyx_XDECREF(__pyx_r);
-  __Pyx_INCREF(((PyObject *)__pyx_v_self));
+  __Pyx_INCREF((PyObject *)__pyx_v_self);
   __pyx_r = ((PyObject *)__pyx_v_self);
   goto __pyx_L0;
 
   /* "pybitset/backends/cython/_bitset.pyx":227
  *         self.i = 0
  * 
  *     def __iter__(self):             # <<<<<<<<<<<<<<
@@ -6203,28 +9091,30 @@
  *         cdef size_t tmp
  *         if bitset_next_set_bit(self.b._bitset, &self.i):
  */
 
 /* Python wrapper */
 static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_10BitSetIter_5__next__(PyObject *__pyx_v_self); /*proto*/
 static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_10BitSetIter_5__next__(PyObject *__pyx_v_self) {
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_VARARGS(__pyx_args, __pyx_nargs);
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("__next__ (wrapper)", 0);
   __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_10BitSetIter_4__next__(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSetIter *)__pyx_v_self));
 
   /* function exit code */
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_10BitSetIter_4__next__(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSetIter *__pyx_v_self) {
   size_t __pyx_v_tmp;
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
+  int __pyx_error_without_exception = 0; /* StopIteration */
   int __pyx_t_1;
   size_t __pyx_t_2;
   PyObject *__pyx_t_3 = NULL;
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   __Pyx_RefNannySetupContext("__next__", 0);
@@ -6232,15 +9122,15 @@
   /* "pybitset/backends/cython/_bitset.pyx":232
  *     def __next__(self):
  *         cdef size_t tmp
  *         if bitset_next_set_bit(self.b._bitset, &self.i):             # <<<<<<<<<<<<<<
  *             tmp = self.i
  *             self.i += 1
  */
-  __pyx_t_1 = (bitset_next_set_bit(__pyx_v_self->b->_bitset, (&__pyx_v_self->i)) != 0);
+  __pyx_t_1 = bitset_next_set_bit(__pyx_v_self->b->_bitset, (&__pyx_v_self->i));
   if (likely(__pyx_t_1)) {
 
     /* "pybitset/backends/cython/_bitset.pyx":233
  *         cdef size_t tmp
  *         if bitset_next_set_bit(self.b._bitset, &self.i):
  *             tmp = self.i             # <<<<<<<<<<<<<<
  *             self.i += 1
@@ -6283,167 +9173,242 @@
 
   /* "pybitset/backends/cython/_bitset.pyx":237
  *             return tmp
  *         else:
  *             raise StopIteration             # <<<<<<<<<<<<<<
  */
   /*else*/ {
-    __Pyx_Raise(__pyx_builtin_StopIteration, 0, 0, 0);
-    __PYX_ERR(0, 237, __pyx_L1_error)
+    __pyx_error_without_exception = 1;
+    goto __pyx_L1_error;;
   }
 
   /* "pybitset/backends/cython/_bitset.pyx":230
  *         return self
  * 
  *     def __next__(self):             # <<<<<<<<<<<<<<
  *         cdef size_t tmp
  *         if bitset_next_set_bit(self.b._bitset, &self.i):
  */
 
   /* function exit code */
   __pyx_L1_error:;
   __Pyx_XDECREF(__pyx_t_3);
-  __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSetIter.__next__", __pyx_clineno, __pyx_lineno, __pyx_filename);
+  if (!__pyx_error_without_exception) {
+    __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSetIter.__next__", __pyx_clineno, __pyx_lineno, __pyx_filename);
+  }
   __pyx_r = NULL;
   __pyx_L0:;
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* "(tree fragment)":1
  * def __reduce_cython__(self):             # <<<<<<<<<<<<<<
- *     raise TypeError("no default __reduce__ due to non-trivial __cinit__")
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"
  * def __setstate_cython__(self, __pyx_state):
  */
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_10BitSetIter_7__reduce_cython__(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_10BitSetIter_6__reduce_cython__[] = "BitSetIter.__reduce_cython__(self)";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_10BitSetIter_7__reduce_cython__(PyObject *__pyx_v_self, CYTHON_UNUSED PyObject *unused) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_10BitSetIter_7__reduce_cython__(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_10BitSetIter_6__reduce_cython__, "BitSetIter.__reduce_cython__(self)");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_10BitSetIter_7__reduce_cython__ = {"__reduce_cython__", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_10BitSetIter_7__reduce_cython__, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_10BitSetIter_6__reduce_cython__};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_10BitSetIter_7__reduce_cython__(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("__reduce_cython__ (wrapper)", 0);
+  if (unlikely(__pyx_nargs > 0)) {
+    __Pyx_RaiseArgtupleInvalid("__reduce_cython__", 1, 0, 0, __pyx_nargs); return NULL;}
+  if (unlikely(__pyx_kwds) && __Pyx_NumKwargs_FASTCALL(__pyx_kwds) && unlikely(!__Pyx_CheckKeywordStrings(__pyx_kwds, "__reduce_cython__", 0))) return NULL;
   __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_10BitSetIter_6__reduce_cython__(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSetIter *)__pyx_v_self));
 
   /* function exit code */
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_10BitSetIter_6__reduce_cython__(CYTHON_UNUSED struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSetIter *__pyx_v_self) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
-  PyObject *__pyx_t_1 = NULL;
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   __Pyx_RefNannySetupContext("__reduce_cython__", 0);
 
   /* "(tree fragment)":2
  * def __reduce_cython__(self):
- *     raise TypeError("no default __reduce__ due to non-trivial __cinit__")             # <<<<<<<<<<<<<<
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"             # <<<<<<<<<<<<<<
  * def __setstate_cython__(self, __pyx_state):
- *     raise TypeError("no default __reduce__ due to non-trivial __cinit__")
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"
  */
-  __pyx_t_1 = __Pyx_PyObject_Call(__pyx_builtin_TypeError, __pyx_tuple__3, NULL); if (unlikely(!__pyx_t_1)) __PYX_ERR(1, 2, __pyx_L1_error)
-  __Pyx_GOTREF(__pyx_t_1);
-  __Pyx_Raise(__pyx_t_1, 0, 0, 0);
-  __Pyx_DECREF(__pyx_t_1); __pyx_t_1 = 0;
+  __Pyx_Raise(__pyx_builtin_TypeError, __pyx_kp_s_no_default___reduce___due_to_non, 0, 0);
   __PYX_ERR(1, 2, __pyx_L1_error)
 
   /* "(tree fragment)":1
  * def __reduce_cython__(self):             # <<<<<<<<<<<<<<
- *     raise TypeError("no default __reduce__ due to non-trivial __cinit__")
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"
  * def __setstate_cython__(self, __pyx_state):
  */
 
   /* function exit code */
   __pyx_L1_error:;
-  __Pyx_XDECREF(__pyx_t_1);
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSetIter.__reduce_cython__", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __pyx_r = NULL;
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 /* "(tree fragment)":3
  * def __reduce_cython__(self):
- *     raise TypeError("no default __reduce__ due to non-trivial __cinit__")
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"
  * def __setstate_cython__(self, __pyx_state):             # <<<<<<<<<<<<<<
- *     raise TypeError("no default __reduce__ due to non-trivial __cinit__")
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"
  */
 
 /* Python wrapper */
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_10BitSetIter_9__setstate_cython__(PyObject *__pyx_v_self, PyObject *__pyx_v___pyx_state); /*proto*/
-static char __pyx_doc_8pybitset_8backends_6cython_7_bitset_10BitSetIter_8__setstate_cython__[] = "BitSetIter.__setstate_cython__(self, __pyx_state)";
-static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_10BitSetIter_9__setstate_cython__(PyObject *__pyx_v_self, PyObject *__pyx_v___pyx_state) {
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_10BitSetIter_9__setstate_cython__(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+); /*proto*/
+PyDoc_STRVAR(__pyx_doc_8pybitset_8backends_6cython_7_bitset_10BitSetIter_8__setstate_cython__, "BitSetIter.__setstate_cython__(self, __pyx_state)");
+static PyMethodDef __pyx_mdef_8pybitset_8backends_6cython_7_bitset_10BitSetIter_9__setstate_cython__ = {"__setstate_cython__", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_10BitSetIter_9__setstate_cython__, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_10BitSetIter_8__setstate_cython__};
+static PyObject *__pyx_pw_8pybitset_8backends_6cython_7_bitset_10BitSetIter_9__setstate_cython__(PyObject *__pyx_v_self, 
+#if CYTHON_METH_FASTCALL
+PyObject *const *__pyx_args, Py_ssize_t __pyx_nargs, PyObject *__pyx_kwds
+#else
+PyObject *__pyx_args, PyObject *__pyx_kwds
+#endif
+) {
+  CYTHON_UNUSED PyObject *__pyx_v___pyx_state = 0;
+  #if !CYTHON_METH_FASTCALL
+  CYTHON_UNUSED const Py_ssize_t __pyx_nargs = PyTuple_GET_SIZE(__pyx_args);
+  #endif
+  CYTHON_UNUSED PyObject *const *__pyx_kwvalues = __Pyx_KwValues_FASTCALL(__pyx_args, __pyx_nargs);
+  int __pyx_lineno = 0;
+  const char *__pyx_filename = NULL;
+  int __pyx_clineno = 0;
   PyObject *__pyx_r = 0;
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("__setstate_cython__ (wrapper)", 0);
-  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_10BitSetIter_8__setstate_cython__(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSetIter *)__pyx_v_self), ((PyObject *)__pyx_v___pyx_state));
+  {
+    PyObject **__pyx_pyargnames[] = {&__pyx_n_s_pyx_state,0};
+    PyObject* values[1] = {0};
+    if (__pyx_kwds) {
+      Py_ssize_t kw_args;
+      switch (__pyx_nargs) {
+        case  1: values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+        CYTHON_FALLTHROUGH;
+        case  0: break;
+        default: goto __pyx_L5_argtuple_error;
+      }
+      kw_args = __Pyx_NumKwargs_FASTCALL(__pyx_kwds);
+      switch (__pyx_nargs) {
+        case  0:
+        if (likely((values[0] = __Pyx_GetKwValue_FASTCALL(__pyx_kwds, __pyx_kwvalues, __pyx_n_s_pyx_state)) != 0)) kw_args--;
+        else if (unlikely(PyErr_Occurred())) __PYX_ERR(1, 3, __pyx_L3_error)
+        else goto __pyx_L5_argtuple_error;
+      }
+      if (unlikely(kw_args > 0)) {
+        const Py_ssize_t kwd_pos_args = __pyx_nargs;
+        if (unlikely(__Pyx_ParseOptionalKeywords(__pyx_kwds, __pyx_kwvalues, __pyx_pyargnames, 0, values + 0, kwd_pos_args, "__setstate_cython__") < 0)) __PYX_ERR(1, 3, __pyx_L3_error)
+      }
+    } else if (unlikely(__pyx_nargs != 1)) {
+      goto __pyx_L5_argtuple_error;
+    } else {
+      values[0] = __Pyx_Arg_FASTCALL(__pyx_args, 0);
+    }
+    __pyx_v___pyx_state = values[0];
+  }
+  goto __pyx_L4_argument_unpacking_done;
+  __pyx_L5_argtuple_error:;
+  __Pyx_RaiseArgtupleInvalid("__setstate_cython__", 1, 1, 1, __pyx_nargs); __PYX_ERR(1, 3, __pyx_L3_error)
+  __pyx_L3_error:;
+  __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSetIter.__setstate_cython__", __pyx_clineno, __pyx_lineno, __pyx_filename);
+  __Pyx_RefNannyFinishContext();
+  return NULL;
+  __pyx_L4_argument_unpacking_done:;
+  __pyx_r = __pyx_pf_8pybitset_8backends_6cython_7_bitset_10BitSetIter_8__setstate_cython__(((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSetIter *)__pyx_v_self), __pyx_v___pyx_state);
 
   /* function exit code */
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 
 static PyObject *__pyx_pf_8pybitset_8backends_6cython_7_bitset_10BitSetIter_8__setstate_cython__(CYTHON_UNUSED struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSetIter *__pyx_v_self, CYTHON_UNUSED PyObject *__pyx_v___pyx_state) {
   PyObject *__pyx_r = NULL;
   __Pyx_RefNannyDeclarations
-  PyObject *__pyx_t_1 = NULL;
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   __Pyx_RefNannySetupContext("__setstate_cython__", 0);
 
   /* "(tree fragment)":4
- *     raise TypeError("no default __reduce__ due to non-trivial __cinit__")
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"
  * def __setstate_cython__(self, __pyx_state):
- *     raise TypeError("no default __reduce__ due to non-trivial __cinit__")             # <<<<<<<<<<<<<<
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"             # <<<<<<<<<<<<<<
  */
-  __pyx_t_1 = __Pyx_PyObject_Call(__pyx_builtin_TypeError, __pyx_tuple__4, NULL); if (unlikely(!__pyx_t_1)) __PYX_ERR(1, 4, __pyx_L1_error)
-  __Pyx_GOTREF(__pyx_t_1);
-  __Pyx_Raise(__pyx_t_1, 0, 0, 0);
-  __Pyx_DECREF(__pyx_t_1); __pyx_t_1 = 0;
+  __Pyx_Raise(__pyx_builtin_TypeError, __pyx_kp_s_no_default___reduce___due_to_non, 0, 0);
   __PYX_ERR(1, 4, __pyx_L1_error)
 
   /* "(tree fragment)":3
  * def __reduce_cython__(self):
- *     raise TypeError("no default __reduce__ due to non-trivial __cinit__")
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"
  * def __setstate_cython__(self, __pyx_state):             # <<<<<<<<<<<<<<
- *     raise TypeError("no default __reduce__ due to non-trivial __cinit__")
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"
  */
 
   /* function exit code */
   __pyx_L1_error:;
-  __Pyx_XDECREF(__pyx_t_1);
   __Pyx_AddTraceback("pybitset.backends.cython._bitset.BitSetIter.__setstate_cython__", __pyx_clineno, __pyx_lineno, __pyx_filename);
   __pyx_r = NULL;
   __Pyx_XGIVEREF(__pyx_r);
   __Pyx_RefNannyFinishContext();
   return __pyx_r;
 }
 static struct __pyx_vtabstruct_8pybitset_8backends_6cython_7_bitset_BitSet __pyx_vtable_8pybitset_8backends_6cython_7_bitset_BitSet;
 
 static struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *__pyx_freelist_8pybitset_8backends_6cython_7_bitset_BitSet[8];
 static int __pyx_freecount_8pybitset_8backends_6cython_7_bitset_BitSet = 0;
 
 static PyObject *__pyx_tp_new_8pybitset_8backends_6cython_7_bitset_BitSet(PyTypeObject *t, PyObject *a, PyObject *k) {
   struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *p;
   PyObject *o;
-  if (CYTHON_COMPILING_IN_CPYTHON && likely((__pyx_freecount_8pybitset_8backends_6cython_7_bitset_BitSet > 0) & (t->tp_basicsize == sizeof(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet)))) {
+  #if CYTHON_COMPILING_IN_LIMITED_API
+  allocfunc alloc_func = (allocfunc)PyType_GetSlot(t, Py_tp_alloc);
+  o = alloc_func(t, 0);
+  #else
+  if (CYTHON_COMPILING_IN_CPYTHON && likely((int)(__pyx_freecount_8pybitset_8backends_6cython_7_bitset_BitSet > 0) & (int)(t->tp_basicsize == sizeof(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet)))) {
     o = (PyObject*)__pyx_freelist_8pybitset_8backends_6cython_7_bitset_BitSet[--__pyx_freecount_8pybitset_8backends_6cython_7_bitset_BitSet];
     memset(o, 0, sizeof(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet));
     (void) PyObject_INIT(o, t);
   } else {
     o = (*t->tp_alloc)(t, 0);
     if (unlikely(!o)) return 0;
   }
+  #endif
   p = ((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)o);
   p->__pyx_vtab = __pyx_vtabptr_8pybitset_8backends_6cython_7_bitset_BitSet;
   if (unlikely(__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_1__cinit__(o, a, k) < 0)) goto bad;
   return o;
   bad:
   Py_DECREF(o); o = 0;
   return NULL;
@@ -6454,60 +9419,46 @@
     PyObject *etype, *eval, *etb;
     PyErr_Fetch(&etype, &eval, &etb);
     __Pyx_SET_REFCNT(o, Py_REFCNT(o) + 1);
     __pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_3__dealloc__(o);
     __Pyx_SET_REFCNT(o, Py_REFCNT(o) - 1);
     PyErr_Restore(etype, eval, etb);
   }
-  if (CYTHON_COMPILING_IN_CPYTHON && ((__pyx_freecount_8pybitset_8backends_6cython_7_bitset_BitSet < 8) & (Py_TYPE(o)->tp_basicsize == sizeof(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet)))) {
+  if (CYTHON_COMPILING_IN_CPYTHON && ((int)(__pyx_freecount_8pybitset_8backends_6cython_7_bitset_BitSet < 8) & (int)(Py_TYPE(o)->tp_basicsize == sizeof(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet)))) {
     __pyx_freelist_8pybitset_8backends_6cython_7_bitset_BitSet[__pyx_freecount_8pybitset_8backends_6cython_7_bitset_BitSet++] = ((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)o);
   } else {
     (*Py_TYPE(o)->tp_free)(o);
   }
 }
 
 static PyMethodDef __pyx_methods_8pybitset_8backends_6cython_7_bitset_BitSet[] = {
-  {"clear", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_5clear, METH_NOARGS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_4clear},
-  {"fill", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_7fill, METH_NOARGS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_6fill},
-  {"copy", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_9copy, METH_NOARGS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_8copy},
-  {"resize", (PyCFunction)(void*)(PyCFunctionWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_11resize, METH_VARARGS|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_10resize},
-  {"size_in_bytes", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_13size_in_bytes, METH_NOARGS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_12size_in_bytes},
-  {"size_in_bits", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_15size_in_bits, METH_NOARGS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_14size_in_bits},
-  {"size_in_words", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_17size_in_words, METH_NOARGS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_16size_in_words},
-  {"grow", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_19grow, METH_O, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_18grow},
-  {"trim", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_21trim, METH_NOARGS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_20trim},
-  {"shift_left", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_23shift_left, METH_O, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_22shift_left},
-  {"shift_right", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_25shift_right, METH_O, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_24shift_right},
-  {"set", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_27set, METH_O, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_26set},
-  {"set_to_value", (PyCFunction)(void*)(PyCFunctionWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_29set_to_value, METH_VARARGS|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_28set_to_value},
-  {"get", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_31get, METH_O, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_30get},
-  {"count", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_33count, METH_NOARGS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_32count},
-  {"minimum", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_35minimum, METH_NOARGS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_34minimum},
-  {"maximum", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_37maximum, METH_NOARGS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_36maximum},
-  {"inplace_union", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_39inplace_union, METH_O, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_38inplace_union},
-  {"union_count", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_41union_count, METH_O, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_40union_count},
-  {"inplace_intersection", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_43inplace_intersection, METH_O, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_42inplace_intersection},
-  {"intersection_count", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_45intersection_count, METH_O, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_44intersection_count},
-  {"disjoint", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_47disjoint, METH_O, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_46disjoint},
-  {"intersect", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_49intersect, METH_O, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_48intersect},
-  {"contains_all", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_51contains_all, METH_O, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_50contains_all},
-  {"inplace_difference", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_53inplace_difference, METH_O, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_52inplace_difference},
-  {"difference_count", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_55difference_count, METH_O, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_54difference_count},
-  {"inplace_symmetric_difference", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_57inplace_symmetric_difference, METH_O, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_56inplace_symmetric_difference},
-  {"symmetric_difference_count", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_59symmetric_difference_count, METH_O, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_58symmetric_difference_count},
-  {"for_each", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_63for_each, METH_O, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_62for_each},
-  {"print", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_65print, METH_NOARGS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_64print},
-  {"__reduce_cython__", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_67__reduce_cython__, METH_NOARGS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_66__reduce_cython__},
-  {"__setstate_cython__", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_69__setstate_cython__, METH_O, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_68__setstate_cython__},
+  {"__reduce_cython__", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_67__reduce_cython__, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_66__reduce_cython__},
+  {"__setstate_cython__", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_69__setstate_cython__, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_6BitSet_68__setstate_cython__},
   {0, 0, 0, 0}
 };
+#if CYTHON_USE_TYPE_SPECS
+static PyType_Slot __pyx_type_8pybitset_8backends_6cython_7_bitset_BitSet_slots[] = {
+  {Py_tp_dealloc, (void *)__pyx_tp_dealloc_8pybitset_8backends_6cython_7_bitset_BitSet},
+  {Py_tp_iter, (void *)__pyx_pw_8pybitset_8backends_6cython_7_bitset_6BitSet_61__iter__},
+  {Py_tp_methods, (void *)__pyx_methods_8pybitset_8backends_6cython_7_bitset_BitSet},
+  {Py_tp_new, (void *)__pyx_tp_new_8pybitset_8backends_6cython_7_bitset_BitSet},
+  {0, 0},
+};
+static PyType_Spec __pyx_type_8pybitset_8backends_6cython_7_bitset_BitSet_spec = {
+  "pybitset.backends.cython._bitset.BitSet",
+  sizeof(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet),
+  0,
+  Py_TPFLAGS_DEFAULT|Py_TPFLAGS_HAVE_VERSION_TAG|Py_TPFLAGS_CHECKTYPES|Py_TPFLAGS_HAVE_NEWBUFFER,
+  __pyx_type_8pybitset_8backends_6cython_7_bitset_BitSet_slots,
+};
+#else
 
 static PyTypeObject __pyx_type_8pybitset_8backends_6cython_7_bitset_BitSet = {
   PyVarObject_HEAD_INIT(0, 0)
-  "pybitset.backends.cython._bitset.BitSet", /*tp_name*/
+  "pybitset.backends.cython._bitset.""BitSet", /*tp_name*/
   sizeof(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet), /*tp_basicsize*/
   0, /*tp_itemsize*/
   __pyx_tp_dealloc_8pybitset_8backends_6cython_7_bitset_BitSet, /*tp_dealloc*/
   #if PY_VERSION_HEX < 0x030800b4
   0, /*tp_print*/
   #endif
   #if PY_VERSION_HEX >= 0x030800b4
@@ -6542,86 +9493,122 @@
   __pyx_methods_8pybitset_8backends_6cython_7_bitset_BitSet, /*tp_methods*/
   0, /*tp_members*/
   0, /*tp_getset*/
   0, /*tp_base*/
   0, /*tp_dict*/
   0, /*tp_descr_get*/
   0, /*tp_descr_set*/
+  #if !CYTHON_USE_TYPE_SPECS
   0, /*tp_dictoffset*/
+  #endif
   0, /*tp_init*/
   0, /*tp_alloc*/
   __pyx_tp_new_8pybitset_8backends_6cython_7_bitset_BitSet, /*tp_new*/
   0, /*tp_free*/
   0, /*tp_is_gc*/
   0, /*tp_bases*/
   0, /*tp_mro*/
   0, /*tp_cache*/
   0, /*tp_subclasses*/
   0, /*tp_weaklist*/
   0, /*tp_del*/
   0, /*tp_version_tag*/
   #if PY_VERSION_HEX >= 0x030400a1
+  #if CYTHON_USE_TP_FINALIZE
   0, /*tp_finalize*/
+  #else
+  NULL, /*tp_finalize*/
+  #endif
   #endif
   #if PY_VERSION_HEX >= 0x030800b1 && (!CYTHON_COMPILING_IN_PYPY || PYPY_VERSION_NUM >= 0x07030800)
   0, /*tp_vectorcall*/
   #endif
-  #if PY_VERSION_HEX >= 0x030800b4 && PY_VERSION_HEX < 0x03090000
+  #if __PYX_NEED_TP_PRINT_SLOT == 1
   0, /*tp_print*/
   #endif
+  #if PY_VERSION_HEX >= 0x030C0000
+  0, /*tp_watched*/
+  #endif
   #if CYTHON_COMPILING_IN_PYPY && PY_VERSION_HEX >= 0x03090000 && PY_VERSION_HEX < 0x030a0000
   0, /*tp_pypy_flags*/
   #endif
 };
+#endif
 
 static struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSetIter *__pyx_freelist_8pybitset_8backends_6cython_7_bitset_BitSetIter[8];
 static int __pyx_freecount_8pybitset_8backends_6cython_7_bitset_BitSetIter = 0;
 
 static PyObject *__pyx_tp_new_8pybitset_8backends_6cython_7_bitset_BitSetIter(PyTypeObject *t, PyObject *a, PyObject *k) {
   struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSetIter *p;
   PyObject *o;
-  if (CYTHON_COMPILING_IN_CPYTHON && likely((__pyx_freecount_8pybitset_8backends_6cython_7_bitset_BitSetIter > 0) & (t->tp_basicsize == sizeof(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSetIter)))) {
+  #if CYTHON_COMPILING_IN_LIMITED_API
+  allocfunc alloc_func = (allocfunc)PyType_GetSlot(t, Py_tp_alloc);
+  o = alloc_func(t, 0);
+  #else
+  if (CYTHON_COMPILING_IN_CPYTHON && likely((int)(__pyx_freecount_8pybitset_8backends_6cython_7_bitset_BitSetIter > 0) & (int)(t->tp_basicsize == sizeof(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSetIter)))) {
     o = (PyObject*)__pyx_freelist_8pybitset_8backends_6cython_7_bitset_BitSetIter[--__pyx_freecount_8pybitset_8backends_6cython_7_bitset_BitSetIter];
     memset(o, 0, sizeof(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSetIter));
     (void) PyObject_INIT(o, t);
   } else {
     o = (*t->tp_alloc)(t, 0);
     if (unlikely(!o)) return 0;
   }
+  #endif
   p = ((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSetIter *)o);
   p->b = ((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *)Py_None); Py_INCREF(Py_None);
   if (unlikely(__pyx_pw_8pybitset_8backends_6cython_7_bitset_10BitSetIter_1__cinit__(o, a, k) < 0)) goto bad;
   return o;
   bad:
   Py_DECREF(o); o = 0;
   return NULL;
 }
 
 static void __pyx_tp_dealloc_8pybitset_8backends_6cython_7_bitset_BitSetIter(PyObject *o) {
   struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSetIter *p = (struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSetIter *)o;
   Py_CLEAR(p->b);
-  if (CYTHON_COMPILING_IN_CPYTHON && ((__pyx_freecount_8pybitset_8backends_6cython_7_bitset_BitSetIter < 8) & (Py_TYPE(o)->tp_basicsize == sizeof(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSetIter)))) {
+  if (CYTHON_COMPILING_IN_CPYTHON && ((int)(__pyx_freecount_8pybitset_8backends_6cython_7_bitset_BitSetIter < 8) & (int)(Py_TYPE(o)->tp_basicsize == sizeof(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSetIter)))) {
     __pyx_freelist_8pybitset_8backends_6cython_7_bitset_BitSetIter[__pyx_freecount_8pybitset_8backends_6cython_7_bitset_BitSetIter++] = ((struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSetIter *)o);
   } else {
     (*Py_TYPE(o)->tp_free)(o);
   }
 }
 
-static PyObject *__pyx_specialmethod___pyx_pw_8pybitset_8backends_6cython_7_bitset_10BitSetIter_5__next__(PyObject *self, CYTHON_UNUSED PyObject *arg) {return __pyx_pw_8pybitset_8backends_6cython_7_bitset_10BitSetIter_5__next__(self);}
+static PyObject *__pyx_specialmethod___pyx_pw_8pybitset_8backends_6cython_7_bitset_10BitSetIter_5__next__(PyObject *self, CYTHON_UNUSED PyObject *arg) {
+  PyObject *res = __pyx_pw_8pybitset_8backends_6cython_7_bitset_10BitSetIter_5__next__(self);
+  if (!res && !PyErr_Occurred()) { PyErr_SetNone(PyExc_StopIteration); }
+  return res;
+}
 
 static PyMethodDef __pyx_methods_8pybitset_8backends_6cython_7_bitset_BitSetIter[] = {
   {"__next__", (PyCFunction)__pyx_specialmethod___pyx_pw_8pybitset_8backends_6cython_7_bitset_10BitSetIter_5__next__, METH_NOARGS|METH_COEXIST, 0},
-  {"__reduce_cython__", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_10BitSetIter_7__reduce_cython__, METH_NOARGS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_10BitSetIter_6__reduce_cython__},
-  {"__setstate_cython__", (PyCFunction)__pyx_pw_8pybitset_8backends_6cython_7_bitset_10BitSetIter_9__setstate_cython__, METH_O, __pyx_doc_8pybitset_8backends_6cython_7_bitset_10BitSetIter_8__setstate_cython__},
+  {"__reduce_cython__", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_10BitSetIter_7__reduce_cython__, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_10BitSetIter_6__reduce_cython__},
+  {"__setstate_cython__", (PyCFunction)(void*)(__Pyx_PyCFunction_FastCallWithKeywords)__pyx_pw_8pybitset_8backends_6cython_7_bitset_10BitSetIter_9__setstate_cython__, __Pyx_METH_FASTCALL|METH_KEYWORDS, __pyx_doc_8pybitset_8backends_6cython_7_bitset_10BitSetIter_8__setstate_cython__},
   {0, 0, 0, 0}
 };
+#if CYTHON_USE_TYPE_SPECS
+static PyType_Slot __pyx_type_8pybitset_8backends_6cython_7_bitset_BitSetIter_slots[] = {
+  {Py_tp_dealloc, (void *)__pyx_tp_dealloc_8pybitset_8backends_6cython_7_bitset_BitSetIter},
+  {Py_tp_iter, (void *)__pyx_pw_8pybitset_8backends_6cython_7_bitset_10BitSetIter_3__iter__},
+  {Py_tp_iternext, (void *)__pyx_pw_8pybitset_8backends_6cython_7_bitset_10BitSetIter_5__next__},
+  {Py_tp_methods, (void *)__pyx_methods_8pybitset_8backends_6cython_7_bitset_BitSetIter},
+  {Py_tp_new, (void *)__pyx_tp_new_8pybitset_8backends_6cython_7_bitset_BitSetIter},
+  {0, 0},
+};
+static PyType_Spec __pyx_type_8pybitset_8backends_6cython_7_bitset_BitSetIter_spec = {
+  "pybitset.backends.cython._bitset.BitSetIter",
+  sizeof(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSetIter),
+  0,
+  Py_TPFLAGS_DEFAULT|Py_TPFLAGS_HAVE_VERSION_TAG|Py_TPFLAGS_CHECKTYPES|Py_TPFLAGS_HAVE_NEWBUFFER,
+  __pyx_type_8pybitset_8backends_6cython_7_bitset_BitSetIter_slots,
+};
+#else
 
 static PyTypeObject __pyx_type_8pybitset_8backends_6cython_7_bitset_BitSetIter = {
   PyVarObject_HEAD_INIT(0, 0)
-  "pybitset.backends.cython._bitset.BitSetIter", /*tp_name*/
+  "pybitset.backends.cython._bitset.""BitSetIter", /*tp_name*/
   sizeof(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSetIter), /*tp_basicsize*/
   0, /*tp_itemsize*/
   __pyx_tp_dealloc_8pybitset_8backends_6cython_7_bitset_BitSetIter, /*tp_dealloc*/
   #if PY_VERSION_HEX < 0x030800b4
   0, /*tp_print*/
   #endif
   #if PY_VERSION_HEX >= 0x030800b4
@@ -6656,175 +9643,534 @@
   __pyx_methods_8pybitset_8backends_6cython_7_bitset_BitSetIter, /*tp_methods*/
   0, /*tp_members*/
   0, /*tp_getset*/
   0, /*tp_base*/
   0, /*tp_dict*/
   0, /*tp_descr_get*/
   0, /*tp_descr_set*/
+  #if !CYTHON_USE_TYPE_SPECS
   0, /*tp_dictoffset*/
+  #endif
   0, /*tp_init*/
   0, /*tp_alloc*/
   __pyx_tp_new_8pybitset_8backends_6cython_7_bitset_BitSetIter, /*tp_new*/
   0, /*tp_free*/
   0, /*tp_is_gc*/
   0, /*tp_bases*/
   0, /*tp_mro*/
   0, /*tp_cache*/
   0, /*tp_subclasses*/
   0, /*tp_weaklist*/
   0, /*tp_del*/
   0, /*tp_version_tag*/
   #if PY_VERSION_HEX >= 0x030400a1
+  #if CYTHON_USE_TP_FINALIZE
   0, /*tp_finalize*/
+  #else
+  NULL, /*tp_finalize*/
+  #endif
   #endif
   #if PY_VERSION_HEX >= 0x030800b1 && (!CYTHON_COMPILING_IN_PYPY || PYPY_VERSION_NUM >= 0x07030800)
   0, /*tp_vectorcall*/
   #endif
-  #if PY_VERSION_HEX >= 0x030800b4 && PY_VERSION_HEX < 0x03090000
+  #if __PYX_NEED_TP_PRINT_SLOT == 1
   0, /*tp_print*/
   #endif
+  #if PY_VERSION_HEX >= 0x030C0000
+  0, /*tp_watched*/
+  #endif
   #if CYTHON_COMPILING_IN_PYPY && PY_VERSION_HEX >= 0x03090000 && PY_VERSION_HEX < 0x030a0000
   0, /*tp_pypy_flags*/
   #endif
 };
+#endif
 
 static PyMethodDef __pyx_methods[] = {
   {0, 0, 0, 0}
 };
-
-#if PY_MAJOR_VERSION >= 3
-#if CYTHON_PEP489_MULTI_PHASE_INIT
-static PyObject* __pyx_pymod_create(PyObject *spec, PyModuleDef *def); /*proto*/
-static int __pyx_pymod_exec__bitset(PyObject* module); /*proto*/
-static PyModuleDef_Slot __pyx_moduledef_slots[] = {
-  {Py_mod_create, (void*)__pyx_pymod_create},
-  {Py_mod_exec, (void*)__pyx_pymod_exec__bitset},
-  {0, NULL}
-};
-#endif
-
-static struct PyModuleDef __pyx_moduledef = {
-    PyModuleDef_HEAD_INIT,
-    "_bitset",
-    0, /* m_doc */
-  #if CYTHON_PEP489_MULTI_PHASE_INIT
-    0, /* m_size */
-  #else
-    -1, /* m_size */
-  #endif
-    __pyx_methods /* m_methods */,
-  #if CYTHON_PEP489_MULTI_PHASE_INIT
-    __pyx_moduledef_slots, /* m_slots */
-  #else
-    NULL, /* m_reload */
-  #endif
-    NULL, /* m_traverse */
-    NULL, /* m_clear */
-    NULL /* m_free */
-};
-#endif
 #ifndef CYTHON_SMALL_CODE
 #if defined(__clang__)
     #define CYTHON_SMALL_CODE
 #elif defined(__GNUC__) && (__GNUC__ > 4 || (__GNUC__ == 4 && __GNUC_MINOR__ >= 3))
     #define CYTHON_SMALL_CODE __attribute__((cold))
 #else
     #define CYTHON_SMALL_CODE
 #endif
 #endif
+/* #### Code section: pystring_table ### */
 
-static __Pyx_StringTabEntry __pyx_string_tab[] = {
-  {&__pyx_n_s_BitSet, __pyx_k_BitSet, sizeof(__pyx_k_BitSet), 0, 0, 1, 1},
-  {&__pyx_n_s_MemoryError, __pyx_k_MemoryError, sizeof(__pyx_k_MemoryError), 0, 0, 1, 1},
-  {&__pyx_n_s_StopIteration, __pyx_k_StopIteration, sizeof(__pyx_k_StopIteration), 0, 0, 1, 1},
-  {&__pyx_n_s_TypeError, __pyx_k_TypeError, sizeof(__pyx_k_TypeError), 0, 0, 1, 1},
-  {&__pyx_n_s_b, __pyx_k_b, sizeof(__pyx_k_b), 0, 0, 1, 1},
-  {&__pyx_n_s_cline_in_traceback, __pyx_k_cline_in_traceback, sizeof(__pyx_k_cline_in_traceback), 0, 0, 1, 1},
-  {&__pyx_n_s_flag, __pyx_k_flag, sizeof(__pyx_k_flag), 0, 0, 1, 1},
-  {&__pyx_n_s_getstate, __pyx_k_getstate, sizeof(__pyx_k_getstate), 0, 0, 1, 1},
-  {&__pyx_n_s_i, __pyx_k_i, sizeof(__pyx_k_i), 0, 0, 1, 1},
-  {&__pyx_n_s_init, __pyx_k_init, sizeof(__pyx_k_init), 0, 0, 1, 1},
-  {&__pyx_n_s_main, __pyx_k_main, sizeof(__pyx_k_main), 0, 0, 1, 1},
-  {&__pyx_n_s_name, __pyx_k_name, sizeof(__pyx_k_name), 0, 0, 1, 1},
-  {&__pyx_n_s_newarraysize, __pyx_k_newarraysize, sizeof(__pyx_k_newarraysize), 0, 0, 1, 1},
-  {&__pyx_kp_s_no_default___reduce___due_to_non, __pyx_k_no_default___reduce___due_to_non, sizeof(__pyx_k_no_default___reduce___due_to_non), 0, 0, 1, 0},
-  {&__pyx_n_s_padwithzeroes, __pyx_k_padwithzeroes, sizeof(__pyx_k_padwithzeroes), 0, 0, 1, 1},
-  {&__pyx_n_s_pyx_vtable, __pyx_k_pyx_vtable, sizeof(__pyx_k_pyx_vtable), 0, 0, 1, 1},
-  {&__pyx_n_s_reduce, __pyx_k_reduce, sizeof(__pyx_k_reduce), 0, 0, 1, 1},
-  {&__pyx_n_s_reduce_cython, __pyx_k_reduce_cython, sizeof(__pyx_k_reduce_cython), 0, 0, 1, 1},
-  {&__pyx_n_s_reduce_ex, __pyx_k_reduce_ex, sizeof(__pyx_k_reduce_ex), 0, 0, 1, 1},
-  {&__pyx_n_s_setstate, __pyx_k_setstate, sizeof(__pyx_k_setstate), 0, 0, 1, 1},
-  {&__pyx_n_s_setstate_cython, __pyx_k_setstate_cython, sizeof(__pyx_k_setstate_cython), 0, 0, 1, 1},
-  {&__pyx_n_s_size, __pyx_k_size, sizeof(__pyx_k_size), 0, 0, 1, 1},
-  {&__pyx_n_s_test, __pyx_k_test, sizeof(__pyx_k_test), 0, 0, 1, 1},
-  {0, 0, 0, 0, 0, 0, 0}
-};
+static int __Pyx_CreateStringTabAndInitStrings(void) {
+  __Pyx_StringTabEntry __pyx_string_tab[] = {
+    {&__pyx_n_s_BitSet, __pyx_k_BitSet, sizeof(__pyx_k_BitSet), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSetIter___reduce_cython, __pyx_k_BitSetIter___reduce_cython, sizeof(__pyx_k_BitSetIter___reduce_cython), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSetIter___setstate_cython, __pyx_k_BitSetIter___setstate_cython, sizeof(__pyx_k_BitSetIter___setstate_cython), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet___reduce_cython, __pyx_k_BitSet___reduce_cython, sizeof(__pyx_k_BitSet___reduce_cython), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet___setstate_cython, __pyx_k_BitSet___setstate_cython, sizeof(__pyx_k_BitSet___setstate_cython), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet_clear, __pyx_k_BitSet_clear, sizeof(__pyx_k_BitSet_clear), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet_contains_all, __pyx_k_BitSet_contains_all, sizeof(__pyx_k_BitSet_contains_all), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet_copy, __pyx_k_BitSet_copy, sizeof(__pyx_k_BitSet_copy), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet_count, __pyx_k_BitSet_count, sizeof(__pyx_k_BitSet_count), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet_difference_count, __pyx_k_BitSet_difference_count, sizeof(__pyx_k_BitSet_difference_count), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet_disjoint, __pyx_k_BitSet_disjoint, sizeof(__pyx_k_BitSet_disjoint), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet_fill, __pyx_k_BitSet_fill, sizeof(__pyx_k_BitSet_fill), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet_for_each, __pyx_k_BitSet_for_each, sizeof(__pyx_k_BitSet_for_each), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet_get, __pyx_k_BitSet_get, sizeof(__pyx_k_BitSet_get), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet_grow, __pyx_k_BitSet_grow, sizeof(__pyx_k_BitSet_grow), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet_inplace_difference, __pyx_k_BitSet_inplace_difference, sizeof(__pyx_k_BitSet_inplace_difference), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet_inplace_intersection, __pyx_k_BitSet_inplace_intersection, sizeof(__pyx_k_BitSet_inplace_intersection), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet_inplace_symmetric_differe, __pyx_k_BitSet_inplace_symmetric_differe, sizeof(__pyx_k_BitSet_inplace_symmetric_differe), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet_inplace_union, __pyx_k_BitSet_inplace_union, sizeof(__pyx_k_BitSet_inplace_union), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet_intersect, __pyx_k_BitSet_intersect, sizeof(__pyx_k_BitSet_intersect), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet_intersection_count, __pyx_k_BitSet_intersection_count, sizeof(__pyx_k_BitSet_intersection_count), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet_maximum, __pyx_k_BitSet_maximum, sizeof(__pyx_k_BitSet_maximum), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet_minimum, __pyx_k_BitSet_minimum, sizeof(__pyx_k_BitSet_minimum), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet_print, __pyx_k_BitSet_print, sizeof(__pyx_k_BitSet_print), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet_resize, __pyx_k_BitSet_resize, sizeof(__pyx_k_BitSet_resize), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet_set, __pyx_k_BitSet_set, sizeof(__pyx_k_BitSet_set), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet_set_to_value, __pyx_k_BitSet_set_to_value, sizeof(__pyx_k_BitSet_set_to_value), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet_shift_left, __pyx_k_BitSet_shift_left, sizeof(__pyx_k_BitSet_shift_left), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet_shift_right, __pyx_k_BitSet_shift_right, sizeof(__pyx_k_BitSet_shift_right), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet_size_in_bits, __pyx_k_BitSet_size_in_bits, sizeof(__pyx_k_BitSet_size_in_bits), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet_size_in_bytes, __pyx_k_BitSet_size_in_bytes, sizeof(__pyx_k_BitSet_size_in_bytes), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet_size_in_words, __pyx_k_BitSet_size_in_words, sizeof(__pyx_k_BitSet_size_in_words), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet_symmetric_difference_coun, __pyx_k_BitSet_symmetric_difference_coun, sizeof(__pyx_k_BitSet_symmetric_difference_coun), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet_trim, __pyx_k_BitSet_trim, sizeof(__pyx_k_BitSet_trim), 0, 0, 1, 1},
+    {&__pyx_n_s_BitSet_union_count, __pyx_k_BitSet_union_count, sizeof(__pyx_k_BitSet_union_count), 0, 0, 1, 1},
+    {&__pyx_n_s_MemoryError, __pyx_k_MemoryError, sizeof(__pyx_k_MemoryError), 0, 0, 1, 1},
+    {&__pyx_n_s_StopIteration, __pyx_k_StopIteration, sizeof(__pyx_k_StopIteration), 0, 0, 1, 1},
+    {&__pyx_n_s_TypeError, __pyx_k_TypeError, sizeof(__pyx_k_TypeError), 0, 0, 1, 1},
+    {&__pyx_n_s__44, __pyx_k__44, sizeof(__pyx_k__44), 0, 0, 1, 1},
+    {&__pyx_n_s_asyncio_coroutines, __pyx_k_asyncio_coroutines, sizeof(__pyx_k_asyncio_coroutines), 0, 0, 1, 1},
+    {&__pyx_n_s_b, __pyx_k_b, sizeof(__pyx_k_b), 0, 0, 1, 1},
+    {&__pyx_n_s_b2, __pyx_k_b2, sizeof(__pyx_k_b2), 0, 0, 1, 1},
+    {&__pyx_n_s_clear, __pyx_k_clear, sizeof(__pyx_k_clear), 0, 0, 1, 1},
+    {&__pyx_n_s_cline_in_traceback, __pyx_k_cline_in_traceback, sizeof(__pyx_k_cline_in_traceback), 0, 0, 1, 1},
+    {&__pyx_n_s_contains_all, __pyx_k_contains_all, sizeof(__pyx_k_contains_all), 0, 0, 1, 1},
+    {&__pyx_n_s_copy, __pyx_k_copy, sizeof(__pyx_k_copy), 0, 0, 1, 1},
+    {&__pyx_n_s_count, __pyx_k_count, sizeof(__pyx_k_count), 0, 0, 1, 1},
+    {&__pyx_n_s_difference_count, __pyx_k_difference_count, sizeof(__pyx_k_difference_count), 0, 0, 1, 1},
+    {&__pyx_kp_u_disable, __pyx_k_disable, sizeof(__pyx_k_disable), 0, 1, 0, 0},
+    {&__pyx_n_s_disjoint, __pyx_k_disjoint, sizeof(__pyx_k_disjoint), 0, 0, 1, 1},
+    {&__pyx_kp_u_enable, __pyx_k_enable, sizeof(__pyx_k_enable), 0, 1, 0, 0},
+    {&__pyx_n_s_fill, __pyx_k_fill, sizeof(__pyx_k_fill), 0, 0, 1, 1},
+    {&__pyx_n_s_flag, __pyx_k_flag, sizeof(__pyx_k_flag), 0, 0, 1, 1},
+    {&__pyx_n_s_for_each, __pyx_k_for_each, sizeof(__pyx_k_for_each), 0, 0, 1, 1},
+    {&__pyx_n_s_func, __pyx_k_func, sizeof(__pyx_k_func), 0, 0, 1, 1},
+    {&__pyx_kp_u_gc, __pyx_k_gc, sizeof(__pyx_k_gc), 0, 1, 0, 0},
+    {&__pyx_n_s_get, __pyx_k_get, sizeof(__pyx_k_get), 0, 0, 1, 1},
+    {&__pyx_n_s_getstate, __pyx_k_getstate, sizeof(__pyx_k_getstate), 0, 0, 1, 1},
+    {&__pyx_n_s_grow, __pyx_k_grow, sizeof(__pyx_k_grow), 0, 0, 1, 1},
+    {&__pyx_n_s_i, __pyx_k_i, sizeof(__pyx_k_i), 0, 0, 1, 1},
+    {&__pyx_n_s_init, __pyx_k_init, sizeof(__pyx_k_init), 0, 0, 1, 1},
+    {&__pyx_n_s_inplace_difference, __pyx_k_inplace_difference, sizeof(__pyx_k_inplace_difference), 0, 0, 1, 1},
+    {&__pyx_n_s_inplace_intersection, __pyx_k_inplace_intersection, sizeof(__pyx_k_inplace_intersection), 0, 0, 1, 1},
+    {&__pyx_n_s_inplace_symmetric_difference, __pyx_k_inplace_symmetric_difference, sizeof(__pyx_k_inplace_symmetric_difference), 0, 0, 1, 1},
+    {&__pyx_n_s_inplace_union, __pyx_k_inplace_union, sizeof(__pyx_k_inplace_union), 0, 0, 1, 1},
+    {&__pyx_n_s_intersect, __pyx_k_intersect, sizeof(__pyx_k_intersect), 0, 0, 1, 1},
+    {&__pyx_n_s_intersection_count, __pyx_k_intersection_count, sizeof(__pyx_k_intersection_count), 0, 0, 1, 1},
+    {&__pyx_n_s_is_coroutine, __pyx_k_is_coroutine, sizeof(__pyx_k_is_coroutine), 0, 0, 1, 1},
+    {&__pyx_kp_u_isenabled, __pyx_k_isenabled, sizeof(__pyx_k_isenabled), 0, 1, 0, 0},
+    {&__pyx_n_s_main, __pyx_k_main, sizeof(__pyx_k_main), 0, 0, 1, 1},
+    {&__pyx_n_s_maximum, __pyx_k_maximum, sizeof(__pyx_k_maximum), 0, 0, 1, 1},
+    {&__pyx_n_s_minimum, __pyx_k_minimum, sizeof(__pyx_k_minimum), 0, 0, 1, 1},
+    {&__pyx_n_s_name, __pyx_k_name, sizeof(__pyx_k_name), 0, 0, 1, 1},
+    {&__pyx_n_s_newarraysize, __pyx_k_newarraysize, sizeof(__pyx_k_newarraysize), 0, 0, 1, 1},
+    {&__pyx_kp_s_no_default___reduce___due_to_non, __pyx_k_no_default___reduce___due_to_non, sizeof(__pyx_k_no_default___reduce___due_to_non), 0, 0, 1, 0},
+    {&__pyx_n_s_padwithzeroes, __pyx_k_padwithzeroes, sizeof(__pyx_k_padwithzeroes), 0, 0, 1, 1},
+    {&__pyx_n_s_print, __pyx_k_print, sizeof(__pyx_k_print), 0, 0, 1, 1},
+    {&__pyx_kp_s_pybitset_backends_cython__bitset, __pyx_k_pybitset_backends_cython__bitset, sizeof(__pyx_k_pybitset_backends_cython__bitset), 0, 0, 1, 0},
+    {&__pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_k_pybitset_backends_cython__bitset_2, sizeof(__pyx_k_pybitset_backends_cython__bitset_2), 0, 0, 1, 1},
+    {&__pyx_n_s_pyx_state, __pyx_k_pyx_state, sizeof(__pyx_k_pyx_state), 0, 0, 1, 1},
+    {&__pyx_n_s_pyx_vtable, __pyx_k_pyx_vtable, sizeof(__pyx_k_pyx_vtable), 0, 0, 1, 1},
+    {&__pyx_n_s_reduce, __pyx_k_reduce, sizeof(__pyx_k_reduce), 0, 0, 1, 1},
+    {&__pyx_n_s_reduce_cython, __pyx_k_reduce_cython, sizeof(__pyx_k_reduce_cython), 0, 0, 1, 1},
+    {&__pyx_n_s_reduce_ex, __pyx_k_reduce_ex, sizeof(__pyx_k_reduce_ex), 0, 0, 1, 1},
+    {&__pyx_n_s_resize, __pyx_k_resize, sizeof(__pyx_k_resize), 0, 0, 1, 1},
+    {&__pyx_n_s_s, __pyx_k_s, sizeof(__pyx_k_s), 0, 0, 1, 1},
+    {&__pyx_n_s_self, __pyx_k_self, sizeof(__pyx_k_self), 0, 0, 1, 1},
+    {&__pyx_n_s_set, __pyx_k_set, sizeof(__pyx_k_set), 0, 0, 1, 1},
+    {&__pyx_n_s_set_to_value, __pyx_k_set_to_value, sizeof(__pyx_k_set_to_value), 0, 0, 1, 1},
+    {&__pyx_n_s_setstate, __pyx_k_setstate, sizeof(__pyx_k_setstate), 0, 0, 1, 1},
+    {&__pyx_n_s_setstate_cython, __pyx_k_setstate_cython, sizeof(__pyx_k_setstate_cython), 0, 0, 1, 1},
+    {&__pyx_n_s_shift_left, __pyx_k_shift_left, sizeof(__pyx_k_shift_left), 0, 0, 1, 1},
+    {&__pyx_n_s_shift_right, __pyx_k_shift_right, sizeof(__pyx_k_shift_right), 0, 0, 1, 1},
+    {&__pyx_n_s_size, __pyx_k_size, sizeof(__pyx_k_size), 0, 0, 1, 1},
+    {&__pyx_n_s_size_in_bits, __pyx_k_size_in_bits, sizeof(__pyx_k_size_in_bits), 0, 0, 1, 1},
+    {&__pyx_n_s_size_in_bytes, __pyx_k_size_in_bytes, sizeof(__pyx_k_size_in_bytes), 0, 0, 1, 1},
+    {&__pyx_n_s_size_in_words, __pyx_k_size_in_words, sizeof(__pyx_k_size_in_words), 0, 0, 1, 1},
+    {&__pyx_kp_s_stringsource, __pyx_k_stringsource, sizeof(__pyx_k_stringsource), 0, 0, 1, 0},
+    {&__pyx_n_s_symmetric_difference_count, __pyx_k_symmetric_difference_count, sizeof(__pyx_k_symmetric_difference_count), 0, 0, 1, 1},
+    {&__pyx_n_s_test, __pyx_k_test, sizeof(__pyx_k_test), 0, 0, 1, 1},
+    {&__pyx_n_s_trim, __pyx_k_trim, sizeof(__pyx_k_trim), 0, 0, 1, 1},
+    {&__pyx_n_s_union_count, __pyx_k_union_count, sizeof(__pyx_k_union_count), 0, 0, 1, 1},
+    {0, 0, 0, 0, 0, 0, 0}
+  };
+  return __Pyx_InitStrings(__pyx_string_tab);
+}
+/* #### Code section: cached_builtins ### */
 static CYTHON_SMALL_CODE int __Pyx_InitCachedBuiltins(void) {
   __pyx_builtin_MemoryError = __Pyx_GetBuiltinName(__pyx_n_s_MemoryError); if (!__pyx_builtin_MemoryError) __PYX_ERR(0, 34, __pyx_L1_error)
   __pyx_builtin_TypeError = __Pyx_GetBuiltinName(__pyx_n_s_TypeError); if (!__pyx_builtin_TypeError) __PYX_ERR(1, 2, __pyx_L1_error)
   __pyx_builtin_StopIteration = __Pyx_GetBuiltinName(__pyx_n_s_StopIteration); if (!__pyx_builtin_StopIteration) __PYX_ERR(0, 237, __pyx_L1_error)
   return 0;
   __pyx_L1_error:;
   return -1;
 }
+/* #### Code section: cached_constants ### */
 
 static CYTHON_SMALL_CODE int __Pyx_InitCachedConstants(void) {
   __Pyx_RefNannyDeclarations
   __Pyx_RefNannySetupContext("__Pyx_InitCachedConstants", 0);
 
-  /* "(tree fragment)":2
- * def __reduce_cython__(self):
- *     raise TypeError("no default __reduce__ due to non-trivial __cinit__")             # <<<<<<<<<<<<<<
- * def __setstate_cython__(self, __pyx_state):
- *     raise TypeError("no default __reduce__ due to non-trivial __cinit__")
+  /* "pybitset/backends/cython/_bitset.pyx":49
+ *         return self
+ * 
+ *     cpdef inline clear(self):             # <<<<<<<<<<<<<<
+ *         with nogil:
+ *             bitset_clear(self._bitset)
  */
-  __pyx_tuple_ = PyTuple_Pack(1, __pyx_kp_s_no_default___reduce___due_to_non); if (unlikely(!__pyx_tuple_)) __PYX_ERR(1, 2, __pyx_L1_error)
+  __pyx_tuple_ = PyTuple_Pack(1, __pyx_n_s_self); if (unlikely(!__pyx_tuple_)) __PYX_ERR(0, 49, __pyx_L1_error)
   __Pyx_GOTREF(__pyx_tuple_);
   __Pyx_GIVEREF(__pyx_tuple_);
+  __pyx_codeobj__2 = (PyObject*)__Pyx_PyCode_New(1, 0, 0, 1, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple_, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_pybitset_backends_cython__bitset, __pyx_n_s_clear, 49, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__2)) __PYX_ERR(0, 49, __pyx_L1_error)
 
-  /* "(tree fragment)":4
- *     raise TypeError("no default __reduce__ due to non-trivial __cinit__")
+  /* "pybitset/backends/cython/_bitset.pyx":53
+ *             bitset_clear(self._bitset)
+ * 
+ *     cpdef inline fill(self):             # <<<<<<<<<<<<<<
+ *         with nogil:
+ *             bitset_fill(self._bitset)
+ */
+  __pyx_codeobj__3 = (PyObject*)__Pyx_PyCode_New(1, 0, 0, 1, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple_, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_pybitset_backends_cython__bitset, __pyx_n_s_fill, 53, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__3)) __PYX_ERR(0, 53, __pyx_L1_error)
+
+  /* "pybitset/backends/cython/_bitset.pyx":57
+ *             bitset_fill(self._bitset)
+ * 
+ *     cpdef inline BitSet copy(self):             # <<<<<<<<<<<<<<
+ *         cdef bitset_t *ret
+ *         with nogil:
+ */
+  __pyx_codeobj__4 = (PyObject*)__Pyx_PyCode_New(1, 0, 0, 1, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple_, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_pybitset_backends_cython__bitset, __pyx_n_s_copy, 57, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__4)) __PYX_ERR(0, 57, __pyx_L1_error)
+
+  /* "pybitset/backends/cython/_bitset.pyx":63
+ *         return BitSet.from_ptr(ret)
+ * 
+ *     cpdef inline bint resize(self, size_t newarraysize, bint padwithzeroes):             # <<<<<<<<<<<<<<
+ *         cdef bint ret
+ *         with nogil:
+ */
+  __pyx_tuple__5 = PyTuple_Pack(3, __pyx_n_s_self, __pyx_n_s_newarraysize, __pyx_n_s_padwithzeroes); if (unlikely(!__pyx_tuple__5)) __PYX_ERR(0, 63, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_tuple__5);
+  __Pyx_GIVEREF(__pyx_tuple__5);
+  __pyx_codeobj__6 = (PyObject*)__Pyx_PyCode_New(3, 0, 0, 3, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple__5, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_pybitset_backends_cython__bitset, __pyx_n_s_resize, 63, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__6)) __PYX_ERR(0, 63, __pyx_L1_error)
+
+  /* "pybitset/backends/cython/_bitset.pyx":69
+ *         return ret
+ * 
+ *     cpdef inline size_t size_in_bytes(self):             # <<<<<<<<<<<<<<
+ *         cdef size_t ret
+ *         with nogil:
+ */
+  __pyx_codeobj__7 = (PyObject*)__Pyx_PyCode_New(1, 0, 0, 1, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple_, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_pybitset_backends_cython__bitset, __pyx_n_s_size_in_bytes, 69, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__7)) __PYX_ERR(0, 69, __pyx_L1_error)
+
+  /* "pybitset/backends/cython/_bitset.pyx":75
+ *         return ret
+ * 
+ *     cpdef inline size_t size_in_bits(self):             # <<<<<<<<<<<<<<
+ *         cdef size_t ret
+ *         with nogil:
+ */
+  __pyx_codeobj__8 = (PyObject*)__Pyx_PyCode_New(1, 0, 0, 1, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple_, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_pybitset_backends_cython__bitset, __pyx_n_s_size_in_bits, 75, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__8)) __PYX_ERR(0, 75, __pyx_L1_error)
+
+  /* "pybitset/backends/cython/_bitset.pyx":81
+ *         return ret
+ * 
+ *     cpdef inline size_t size_in_words(self):             # <<<<<<<<<<<<<<
+ *         cdef size_t ret
+ *         with nogil:
+ */
+  __pyx_codeobj__9 = (PyObject*)__Pyx_PyCode_New(1, 0, 0, 1, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple_, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_pybitset_backends_cython__bitset, __pyx_n_s_size_in_words, 81, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__9)) __PYX_ERR(0, 81, __pyx_L1_error)
+
+  /* "pybitset/backends/cython/_bitset.pyx":87
+ *         return ret
+ * 
+ *     cpdef inline bint grow(self, size_t newarraysize):             # <<<<<<<<<<<<<<
+ *         cdef bint ret
+ *         with nogil:
+ */
+  __pyx_tuple__10 = PyTuple_Pack(2, __pyx_n_s_self, __pyx_n_s_newarraysize); if (unlikely(!__pyx_tuple__10)) __PYX_ERR(0, 87, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_tuple__10);
+  __Pyx_GIVEREF(__pyx_tuple__10);
+  __pyx_codeobj__11 = (PyObject*)__Pyx_PyCode_New(2, 0, 0, 2, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple__10, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_pybitset_backends_cython__bitset, __pyx_n_s_grow, 87, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__11)) __PYX_ERR(0, 87, __pyx_L1_error)
+
+  /* "pybitset/backends/cython/_bitset.pyx":93
+ *         return ret
+ * 
+ *     cpdef inline bint trim(self):             # <<<<<<<<<<<<<<
+ *         cdef bint ret
+ *         with nogil:
+ */
+  __pyx_codeobj__12 = (PyObject*)__Pyx_PyCode_New(1, 0, 0, 1, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple_, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_pybitset_backends_cython__bitset, __pyx_n_s_trim, 93, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__12)) __PYX_ERR(0, 93, __pyx_L1_error)
+
+  /* "pybitset/backends/cython/_bitset.pyx":99
+ *         return ret
+ * 
+ *     cpdef inline shift_left(self, size_t s):             # <<<<<<<<<<<<<<
+ *         with nogil:
+ *             bitset_shift_left(self._bitset, s)
+ */
+  __pyx_tuple__13 = PyTuple_Pack(2, __pyx_n_s_self, __pyx_n_s_s); if (unlikely(!__pyx_tuple__13)) __PYX_ERR(0, 99, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_tuple__13);
+  __Pyx_GIVEREF(__pyx_tuple__13);
+  __pyx_codeobj__14 = (PyObject*)__Pyx_PyCode_New(2, 0, 0, 2, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple__13, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_pybitset_backends_cython__bitset, __pyx_n_s_shift_left, 99, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__14)) __PYX_ERR(0, 99, __pyx_L1_error)
+
+  /* "pybitset/backends/cython/_bitset.pyx":103
+ *             bitset_shift_left(self._bitset, s)
+ * 
+ *     cpdef inline shift_right(self, size_t s):             # <<<<<<<<<<<<<<
+ *         with nogil:
+ *             bitset_shift_right(self._bitset, s)
+ */
+  __pyx_codeobj__15 = (PyObject*)__Pyx_PyCode_New(2, 0, 0, 2, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple__13, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_pybitset_backends_cython__bitset, __pyx_n_s_shift_right, 103, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__15)) __PYX_ERR(0, 103, __pyx_L1_error)
+
+  /* "pybitset/backends/cython/_bitset.pyx":107
+ *             bitset_shift_right(self._bitset, s)
+ * 
+ *     cpdef inline set(self,  size_t i):             # <<<<<<<<<<<<<<
+ *         with nogil:
+ *             bitset_set(self._bitset, i)
+ */
+  __pyx_tuple__16 = PyTuple_Pack(2, __pyx_n_s_self, __pyx_n_s_i); if (unlikely(!__pyx_tuple__16)) __PYX_ERR(0, 107, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_tuple__16);
+  __Pyx_GIVEREF(__pyx_tuple__16);
+  __pyx_codeobj__17 = (PyObject*)__Pyx_PyCode_New(2, 0, 0, 2, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple__16, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_pybitset_backends_cython__bitset, __pyx_n_s_set, 107, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__17)) __PYX_ERR(0, 107, __pyx_L1_error)
+
+  /* "pybitset/backends/cython/_bitset.pyx":111
+ *             bitset_set(self._bitset, i)
+ * 
+ *     cpdef inline set_to_value(self, size_t i, bint flag):             # <<<<<<<<<<<<<<
+ *         with nogil:
+ *             bitset_set_to_value(self._bitset, i, flag)
+ */
+  __pyx_tuple__18 = PyTuple_Pack(3, __pyx_n_s_self, __pyx_n_s_i, __pyx_n_s_flag); if (unlikely(!__pyx_tuple__18)) __PYX_ERR(0, 111, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_tuple__18);
+  __Pyx_GIVEREF(__pyx_tuple__18);
+  __pyx_codeobj__19 = (PyObject*)__Pyx_PyCode_New(3, 0, 0, 3, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple__18, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_pybitset_backends_cython__bitset, __pyx_n_s_set_to_value, 111, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__19)) __PYX_ERR(0, 111, __pyx_L1_error)
+
+  /* "pybitset/backends/cython/_bitset.pyx":115
+ *             bitset_set_to_value(self._bitset, i, flag)
+ * 
+ *     cpdef inline bint get(self, size_t i):             # <<<<<<<<<<<<<<
+ *         cdef bint ret
+ *         with nogil:
+ */
+  __pyx_codeobj__20 = (PyObject*)__Pyx_PyCode_New(2, 0, 0, 2, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple__16, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_pybitset_backends_cython__bitset, __pyx_n_s_get, 115, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__20)) __PYX_ERR(0, 115, __pyx_L1_error)
+
+  /* "pybitset/backends/cython/_bitset.pyx":121
+ *         return ret
+ * 
+ *     cpdef inline size_t count(self):             # <<<<<<<<<<<<<<
+ *         cdef size_t ret
+ *         with nogil:
+ */
+  __pyx_codeobj__21 = (PyObject*)__Pyx_PyCode_New(1, 0, 0, 1, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple_, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_pybitset_backends_cython__bitset, __pyx_n_s_count, 121, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__21)) __PYX_ERR(0, 121, __pyx_L1_error)
+
+  /* "pybitset/backends/cython/_bitset.pyx":127
+ *         return ret
+ * 
+ *     cpdef inline size_t minimum(self):             # <<<<<<<<<<<<<<
+ *         cdef size_t ret
+ *         with nogil:
+ */
+  __pyx_codeobj__22 = (PyObject*)__Pyx_PyCode_New(1, 0, 0, 1, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple_, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_pybitset_backends_cython__bitset, __pyx_n_s_minimum, 127, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__22)) __PYX_ERR(0, 127, __pyx_L1_error)
+
+  /* "pybitset/backends/cython/_bitset.pyx":133
+ *         return ret
+ * 
+ *     cpdef inline size_t maximum(self):             # <<<<<<<<<<<<<<
+ *         cdef size_t ret
+ *         with nogil:
+ */
+  __pyx_codeobj__23 = (PyObject*)__Pyx_PyCode_New(1, 0, 0, 1, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple_, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_pybitset_backends_cython__bitset, __pyx_n_s_maximum, 133, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__23)) __PYX_ERR(0, 133, __pyx_L1_error)
+
+  /* "pybitset/backends/cython/_bitset.pyx":139
+ *         return ret
+ * 
+ *     cpdef inline bint inplace_union(self, BitSet b2):             # <<<<<<<<<<<<<<
+ *         cdef bint ret
+ *         with nogil:
+ */
+  __pyx_tuple__24 = PyTuple_Pack(2, __pyx_n_s_self, __pyx_n_s_b2); if (unlikely(!__pyx_tuple__24)) __PYX_ERR(0, 139, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_tuple__24);
+  __Pyx_GIVEREF(__pyx_tuple__24);
+  __pyx_codeobj__25 = (PyObject*)__Pyx_PyCode_New(2, 0, 0, 2, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple__24, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_pybitset_backends_cython__bitset, __pyx_n_s_inplace_union, 139, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__25)) __PYX_ERR(0, 139, __pyx_L1_error)
+
+  /* "pybitset/backends/cython/_bitset.pyx":145
+ *         return ret
+ * 
+ *     cpdef inline size_t union_count(self, BitSet b2):             # <<<<<<<<<<<<<<
+ *         cdef size_t ret
+ *         with nogil:
+ */
+  __pyx_codeobj__26 = (PyObject*)__Pyx_PyCode_New(2, 0, 0, 2, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple__24, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_pybitset_backends_cython__bitset, __pyx_n_s_union_count, 145, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__26)) __PYX_ERR(0, 145, __pyx_L1_error)
+
+  /* "pybitset/backends/cython/_bitset.pyx":151
+ *         return ret
+ * 
+ *     cpdef inline inplace_intersection(self, BitSet b2):             # <<<<<<<<<<<<<<
+ *         with nogil:
+ *             bitset_inplace_intersection(self._bitset, b2._bitset)
+ */
+  __pyx_codeobj__27 = (PyObject*)__Pyx_PyCode_New(2, 0, 0, 2, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple__24, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_pybitset_backends_cython__bitset, __pyx_n_s_inplace_intersection, 151, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__27)) __PYX_ERR(0, 151, __pyx_L1_error)
+
+  /* "pybitset/backends/cython/_bitset.pyx":155
+ *             bitset_inplace_intersection(self._bitset, b2._bitset)
+ * 
+ *     cpdef inline size_t intersection_count(self, BitSet b2):             # <<<<<<<<<<<<<<
+ *         cdef size_t ret
+ *         with nogil:
+ */
+  __pyx_codeobj__28 = (PyObject*)__Pyx_PyCode_New(2, 0, 0, 2, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple__24, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_pybitset_backends_cython__bitset, __pyx_n_s_intersection_count, 155, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__28)) __PYX_ERR(0, 155, __pyx_L1_error)
+
+  /* "pybitset/backends/cython/_bitset.pyx":161
+ *         return ret
+ * 
+ *     cpdef inline bint disjoint(self, BitSet b2):             # <<<<<<<<<<<<<<
+ *         cdef bint ret
+ *         with nogil:
+ */
+  __pyx_codeobj__29 = (PyObject*)__Pyx_PyCode_New(2, 0, 0, 2, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple__24, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_pybitset_backends_cython__bitset, __pyx_n_s_disjoint, 161, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__29)) __PYX_ERR(0, 161, __pyx_L1_error)
+
+  /* "pybitset/backends/cython/_bitset.pyx":167
+ *         return ret
+ * 
+ *     cpdef inline bint intersect(self, BitSet b2):             # <<<<<<<<<<<<<<
+ *         cdef bint ret
+ *         with nogil:
+ */
+  __pyx_codeobj__30 = (PyObject*)__Pyx_PyCode_New(2, 0, 0, 2, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple__24, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_pybitset_backends_cython__bitset, __pyx_n_s_intersect, 167, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__30)) __PYX_ERR(0, 167, __pyx_L1_error)
+
+  /* "pybitset/backends/cython/_bitset.pyx":173
+ *         return ret
+ * 
+ *     cpdef inline bint contains_all(self, BitSet b2):             # <<<<<<<<<<<<<<
+ *         cdef bint ret
+ *         with nogil:
+ */
+  __pyx_codeobj__31 = (PyObject*)__Pyx_PyCode_New(2, 0, 0, 2, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple__24, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_pybitset_backends_cython__bitset, __pyx_n_s_contains_all, 173, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__31)) __PYX_ERR(0, 173, __pyx_L1_error)
+
+  /* "pybitset/backends/cython/_bitset.pyx":179
+ *         return ret
+ * 
+ *     cpdef inline inplace_difference(self, BitSet b2):             # <<<<<<<<<<<<<<
+ *         with nogil:
+ *             bitset_inplace_difference(self._bitset, b2._bitset)
+ */
+  __pyx_codeobj__32 = (PyObject*)__Pyx_PyCode_New(2, 0, 0, 2, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple__24, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_pybitset_backends_cython__bitset, __pyx_n_s_inplace_difference, 179, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__32)) __PYX_ERR(0, 179, __pyx_L1_error)
+
+  /* "pybitset/backends/cython/_bitset.pyx":183
+ *             bitset_inplace_difference(self._bitset, b2._bitset)
+ * 
+ *     cpdef inline size_t difference_count(self, BitSet b2):             # <<<<<<<<<<<<<<
+ *         cdef size_t ret
+ *         with nogil:
+ */
+  __pyx_codeobj__33 = (PyObject*)__Pyx_PyCode_New(2, 0, 0, 2, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple__24, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_pybitset_backends_cython__bitset, __pyx_n_s_difference_count, 183, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__33)) __PYX_ERR(0, 183, __pyx_L1_error)
+
+  /* "pybitset/backends/cython/_bitset.pyx":189
+ *         return ret
+ * 
+ *     cpdef inline bint inplace_symmetric_difference(self, BitSet b2):             # <<<<<<<<<<<<<<
+ *         cdef bint ret
+ *         with nogil:
+ */
+  __pyx_codeobj__34 = (PyObject*)__Pyx_PyCode_New(2, 0, 0, 2, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple__24, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_pybitset_backends_cython__bitset, __pyx_n_s_inplace_symmetric_difference, 189, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__34)) __PYX_ERR(0, 189, __pyx_L1_error)
+
+  /* "pybitset/backends/cython/_bitset.pyx":195
+ *         return ret
+ * 
+ *     cpdef inline size_t symmetric_difference_count(self, BitSet b2):             # <<<<<<<<<<<<<<
+ *         cdef size_t ret
+ *         with nogil:
+ */
+  __pyx_codeobj__35 = (PyObject*)__Pyx_PyCode_New(2, 0, 0, 2, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple__24, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_pybitset_backends_cython__bitset, __pyx_n_s_symmetric_difference_count, 195, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__35)) __PYX_ERR(0, 195, __pyx_L1_error)
+
+  /* "pybitset/backends/cython/_bitset.pyx":204
+ *         return BitSetIter(self)
+ * 
+ *     cpdef inline bint for_each(self, object func):             # <<<<<<<<<<<<<<
+ *         cdef bint ret
+ *         with nogil:
+ */
+  __pyx_tuple__36 = PyTuple_Pack(2, __pyx_n_s_self, __pyx_n_s_func); if (unlikely(!__pyx_tuple__36)) __PYX_ERR(0, 204, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_tuple__36);
+  __Pyx_GIVEREF(__pyx_tuple__36);
+  __pyx_codeobj__37 = (PyObject*)__Pyx_PyCode_New(2, 0, 0, 2, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple__36, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_pybitset_backends_cython__bitset, __pyx_n_s_for_each, 204, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__37)) __PYX_ERR(0, 204, __pyx_L1_error)
+
+  /* "pybitset/backends/cython/_bitset.pyx":210
+ *         return ret
+ * 
+ *     cpdef inline print(self):             # <<<<<<<<<<<<<<
+ *         with nogil:
+ *             bitset_print(self._bitset)
+ */
+  __pyx_codeobj__38 = (PyObject*)__Pyx_PyCode_New(1, 0, 0, 1, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple_, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_pybitset_backends_cython__bitset, __pyx_n_s_print, 210, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__38)) __PYX_ERR(0, 210, __pyx_L1_error)
+
+  /* "(tree fragment)":1
+ * def __reduce_cython__(self):             # <<<<<<<<<<<<<<
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"
  * def __setstate_cython__(self, __pyx_state):
- *     raise TypeError("no default __reduce__ due to non-trivial __cinit__")             # <<<<<<<<<<<<<<
  */
-  __pyx_tuple__2 = PyTuple_Pack(1, __pyx_kp_s_no_default___reduce___due_to_non); if (unlikely(!__pyx_tuple__2)) __PYX_ERR(1, 4, __pyx_L1_error)
-  __Pyx_GOTREF(__pyx_tuple__2);
-  __Pyx_GIVEREF(__pyx_tuple__2);
+  __pyx_codeobj__39 = (PyObject*)__Pyx_PyCode_New(1, 0, 0, 1, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple_, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_stringsource, __pyx_n_s_reduce_cython, 1, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__39)) __PYX_ERR(1, 1, __pyx_L1_error)
 
-  /* "(tree fragment)":2
+  /* "(tree fragment)":3
  * def __reduce_cython__(self):
- *     raise TypeError("no default __reduce__ due to non-trivial __cinit__")             # <<<<<<<<<<<<<<
- * def __setstate_cython__(self, __pyx_state):
- *     raise TypeError("no default __reduce__ due to non-trivial __cinit__")
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"
+ * def __setstate_cython__(self, __pyx_state):             # <<<<<<<<<<<<<<
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"
  */
-  __pyx_tuple__3 = PyTuple_Pack(1, __pyx_kp_s_no_default___reduce___due_to_non); if (unlikely(!__pyx_tuple__3)) __PYX_ERR(1, 2, __pyx_L1_error)
-  __Pyx_GOTREF(__pyx_tuple__3);
-  __Pyx_GIVEREF(__pyx_tuple__3);
+  __pyx_tuple__40 = PyTuple_Pack(2, __pyx_n_s_self, __pyx_n_s_pyx_state); if (unlikely(!__pyx_tuple__40)) __PYX_ERR(1, 3, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_tuple__40);
+  __Pyx_GIVEREF(__pyx_tuple__40);
+  __pyx_codeobj__41 = (PyObject*)__Pyx_PyCode_New(2, 0, 0, 2, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple__40, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_stringsource, __pyx_n_s_setstate_cython, 3, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__41)) __PYX_ERR(1, 3, __pyx_L1_error)
 
-  /* "(tree fragment)":4
- *     raise TypeError("no default __reduce__ due to non-trivial __cinit__")
+  /* "(tree fragment)":1
+ * def __reduce_cython__(self):             # <<<<<<<<<<<<<<
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"
  * def __setstate_cython__(self, __pyx_state):
- *     raise TypeError("no default __reduce__ due to non-trivial __cinit__")             # <<<<<<<<<<<<<<
  */
-  __pyx_tuple__4 = PyTuple_Pack(1, __pyx_kp_s_no_default___reduce___due_to_non); if (unlikely(!__pyx_tuple__4)) __PYX_ERR(1, 4, __pyx_L1_error)
-  __Pyx_GOTREF(__pyx_tuple__4);
-  __Pyx_GIVEREF(__pyx_tuple__4);
+  __pyx_codeobj__42 = (PyObject*)__Pyx_PyCode_New(1, 0, 0, 1, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple_, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_stringsource, __pyx_n_s_reduce_cython, 1, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__42)) __PYX_ERR(1, 1, __pyx_L1_error)
+
+  /* "(tree fragment)":3
+ * def __reduce_cython__(self):
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"
+ * def __setstate_cython__(self, __pyx_state):             # <<<<<<<<<<<<<<
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"
+ */
+  __pyx_codeobj__43 = (PyObject*)__Pyx_PyCode_New(2, 0, 0, 2, 0, CO_OPTIMIZED|CO_NEWLOCALS, __pyx_empty_bytes, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_tuple__40, __pyx_empty_tuple, __pyx_empty_tuple, __pyx_kp_s_stringsource, __pyx_n_s_setstate_cython, 3, __pyx_empty_bytes); if (unlikely(!__pyx_codeobj__43)) __PYX_ERR(1, 3, __pyx_L1_error)
   __Pyx_RefNannyFinishContext();
   return 0;
   __pyx_L1_error:;
   __Pyx_RefNannyFinishContext();
   return -1;
 }
+/* #### Code section: init_constants ### */
 
-static CYTHON_SMALL_CODE int __Pyx_InitGlobals(void) {
-  if (__Pyx_InitStrings(__pyx_string_tab) < 0) __PYX_ERR(0, 1, __pyx_L1_error)
+static CYTHON_SMALL_CODE int __Pyx_InitConstants(void) {
+  if (__Pyx_CreateStringTabAndInitStrings() < 0) __PYX_ERR(0, 1, __pyx_L1_error);
   return 0;
   __pyx_L1_error:;
   return -1;
 }
+/* #### Code section: init_globals ### */
+
+static CYTHON_SMALL_CODE int __Pyx_InitGlobals(void) {
+  return 0;
+}
+/* #### Code section: init_module ### */
 
 static CYTHON_SMALL_CODE int __Pyx_modinit_global_init_code(void); /*proto*/
 static CYTHON_SMALL_CODE int __Pyx_modinit_variable_export_code(void); /*proto*/
 static CYTHON_SMALL_CODE int __Pyx_modinit_function_export_code(void); /*proto*/
 static CYTHON_SMALL_CODE int __Pyx_modinit_type_init_code(void); /*proto*/
 static CYTHON_SMALL_CODE int __Pyx_modinit_type_import_code(void); /*proto*/
 static CYTHON_SMALL_CODE int __Pyx_modinit_variable_import_code(void); /*proto*/
@@ -6889,34 +10235,63 @@
   __pyx_vtable_8pybitset_8backends_6cython_7_bitset_BitSet.contains_all = (int (*)(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *, int __pyx_skip_dispatch))__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_contains_all;
   __pyx_vtable_8pybitset_8backends_6cython_7_bitset_BitSet.inplace_difference = (PyObject *(*)(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *, int __pyx_skip_dispatch))__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_inplace_difference;
   __pyx_vtable_8pybitset_8backends_6cython_7_bitset_BitSet.difference_count = (size_t (*)(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *, int __pyx_skip_dispatch))__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_difference_count;
   __pyx_vtable_8pybitset_8backends_6cython_7_bitset_BitSet.inplace_symmetric_difference = (int (*)(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *, int __pyx_skip_dispatch))__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_inplace_symmetric_difference;
   __pyx_vtable_8pybitset_8backends_6cython_7_bitset_BitSet.symmetric_difference_count = (size_t (*)(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *, struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *, int __pyx_skip_dispatch))__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_symmetric_difference_count;
   __pyx_vtable_8pybitset_8backends_6cython_7_bitset_BitSet.for_each = (int (*)(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *, PyObject *, int __pyx_skip_dispatch))__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_for_each;
   __pyx_vtable_8pybitset_8backends_6cython_7_bitset_BitSet.print = (PyObject *(*)(struct __pyx_obj_8pybitset_8backends_6cython_7_bitset_BitSet *, int __pyx_skip_dispatch))__pyx_f_8pybitset_8backends_6cython_7_bitset_6BitSet_print;
-  if (PyType_Ready(&__pyx_type_8pybitset_8backends_6cython_7_bitset_BitSet) < 0) __PYX_ERR(0, 25, __pyx_L1_error)
-  #if PY_VERSION_HEX < 0x030800B1
-  __pyx_type_8pybitset_8backends_6cython_7_bitset_BitSet.tp_print = 0;
-  #endif
-  if ((CYTHON_USE_TYPE_SLOTS && CYTHON_USE_PYTYPE_LOOKUP) && likely(!__pyx_type_8pybitset_8backends_6cython_7_bitset_BitSet.tp_dictoffset && __pyx_type_8pybitset_8backends_6cython_7_bitset_BitSet.tp_getattro == PyObject_GenericGetAttr)) {
-    __pyx_type_8pybitset_8backends_6cython_7_bitset_BitSet.tp_getattro = __Pyx_PyObject_GenericGetAttrNoDict;
-  }
-  if (__Pyx_SetVtable(__pyx_type_8pybitset_8backends_6cython_7_bitset_BitSet.tp_dict, __pyx_vtabptr_8pybitset_8backends_6cython_7_bitset_BitSet) < 0) __PYX_ERR(0, 25, __pyx_L1_error)
-  if (PyObject_SetAttr(__pyx_m, __pyx_n_s_BitSet, (PyObject *)&__pyx_type_8pybitset_8backends_6cython_7_bitset_BitSet) < 0) __PYX_ERR(0, 25, __pyx_L1_error)
-  if (__Pyx_setup_reduce((PyObject*)&__pyx_type_8pybitset_8backends_6cython_7_bitset_BitSet) < 0) __PYX_ERR(0, 25, __pyx_L1_error)
+  #if CYTHON_USE_TYPE_SPECS
+  __pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet = (PyTypeObject *) __Pyx_PyType_FromModuleAndSpec(__pyx_m, &__pyx_type_8pybitset_8backends_6cython_7_bitset_BitSet_spec, NULL); if (unlikely(!__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet)) __PYX_ERR(0, 25, __pyx_L1_error)
+  if (__Pyx_fix_up_extension_type_from_spec(&__pyx_type_8pybitset_8backends_6cython_7_bitset_BitSet_spec, __pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet) < 0) __PYX_ERR(0, 25, __pyx_L1_error)
+  #else
   __pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet = &__pyx_type_8pybitset_8backends_6cython_7_bitset_BitSet;
-  if (PyType_Ready(&__pyx_type_8pybitset_8backends_6cython_7_bitset_BitSetIter) < 0) __PYX_ERR(0, 218, __pyx_L1_error)
-  #if PY_VERSION_HEX < 0x030800B1
-  __pyx_type_8pybitset_8backends_6cython_7_bitset_BitSetIter.tp_print = 0;
   #endif
-  if ((CYTHON_USE_TYPE_SLOTS && CYTHON_USE_PYTYPE_LOOKUP) && likely(!__pyx_type_8pybitset_8backends_6cython_7_bitset_BitSetIter.tp_dictoffset && __pyx_type_8pybitset_8backends_6cython_7_bitset_BitSetIter.tp_getattro == PyObject_GenericGetAttr)) {
-    __pyx_type_8pybitset_8backends_6cython_7_bitset_BitSetIter.tp_getattro = __Pyx_PyObject_GenericGetAttrNoDict;
+  #if !CYTHON_COMPILING_IN_LIMITED_API
+  #endif
+  #if !CYTHON_USE_TYPE_SPECS
+  if (__Pyx_PyType_Ready(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet) < 0) __PYX_ERR(0, 25, __pyx_L1_error)
+  #endif
+  #if PY_MAJOR_VERSION < 3
+  __pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_print = 0;
+  #endif
+  #if !CYTHON_COMPILING_IN_LIMITED_API
+  if ((CYTHON_USE_TYPE_SLOTS && CYTHON_USE_PYTYPE_LOOKUP) && likely(!__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_dictoffset && __pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_getattro == PyObject_GenericGetAttr)) {
+    __pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_getattro = __Pyx_PyObject_GenericGetAttrNoDict;
   }
-  if (__Pyx_setup_reduce((PyObject*)&__pyx_type_8pybitset_8backends_6cython_7_bitset_BitSetIter) < 0) __PYX_ERR(0, 218, __pyx_L1_error)
+  #endif
+  if (__Pyx_SetVtable(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet, __pyx_vtabptr_8pybitset_8backends_6cython_7_bitset_BitSet) < 0) __PYX_ERR(0, 25, __pyx_L1_error)
+  #if !CYTHON_COMPILING_IN_LIMITED_API
+  if (__Pyx_MergeVtables(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet) < 0) __PYX_ERR(0, 25, __pyx_L1_error)
+  #endif
+  if (PyObject_SetAttr(__pyx_m, __pyx_n_s_BitSet, (PyObject *) __pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet) < 0) __PYX_ERR(0, 25, __pyx_L1_error)
+  #if !CYTHON_COMPILING_IN_LIMITED_API
+  if (__Pyx_setup_reduce((PyObject *) __pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet) < 0) __PYX_ERR(0, 25, __pyx_L1_error)
+  #endif
+  #if CYTHON_USE_TYPE_SPECS
+  __pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSetIter = (PyTypeObject *) __Pyx_PyType_FromModuleAndSpec(__pyx_m, &__pyx_type_8pybitset_8backends_6cython_7_bitset_BitSetIter_spec, NULL); if (unlikely(!__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSetIter)) __PYX_ERR(0, 218, __pyx_L1_error)
+  if (__Pyx_fix_up_extension_type_from_spec(&__pyx_type_8pybitset_8backends_6cython_7_bitset_BitSetIter_spec, __pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSetIter) < 0) __PYX_ERR(0, 218, __pyx_L1_error)
+  #else
   __pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSetIter = &__pyx_type_8pybitset_8backends_6cython_7_bitset_BitSetIter;
+  #endif
+  #if !CYTHON_COMPILING_IN_LIMITED_API
+  #endif
+  #if !CYTHON_USE_TYPE_SPECS
+  if (__Pyx_PyType_Ready(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSetIter) < 0) __PYX_ERR(0, 218, __pyx_L1_error)
+  #endif
+  #if PY_MAJOR_VERSION < 3
+  __pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSetIter->tp_print = 0;
+  #endif
+  #if !CYTHON_COMPILING_IN_LIMITED_API
+  if ((CYTHON_USE_TYPE_SLOTS && CYTHON_USE_PYTYPE_LOOKUP) && likely(!__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSetIter->tp_dictoffset && __pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSetIter->tp_getattro == PyObject_GenericGetAttr)) {
+    __pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSetIter->tp_getattro = __Pyx_PyObject_GenericGetAttrNoDict;
+  }
+  #endif
+  #if !CYTHON_COMPILING_IN_LIMITED_API
+  if (__Pyx_setup_reduce((PyObject *) __pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSetIter) < 0) __PYX_ERR(0, 218, __pyx_L1_error)
+  #endif
   __Pyx_RefNannyFinishContext();
   return 0;
   __pyx_L1_error:;
   __Pyx_RefNannyFinishContext();
   return -1;
 }
 
@@ -6941,14 +10316,63 @@
   __Pyx_RefNannySetupContext("__Pyx_modinit_function_import_code", 0);
   /*--- Function import code ---*/
   __Pyx_RefNannyFinishContext();
   return 0;
 }
 
 
+#if PY_MAJOR_VERSION >= 3
+#if CYTHON_PEP489_MULTI_PHASE_INIT
+static PyObject* __pyx_pymod_create(PyObject *spec, PyModuleDef *def); /*proto*/
+static int __pyx_pymod_exec__bitset(PyObject* module); /*proto*/
+static PyModuleDef_Slot __pyx_moduledef_slots[] = {
+  {Py_mod_create, (void*)__pyx_pymod_create},
+  {Py_mod_exec, (void*)__pyx_pymod_exec__bitset},
+  {0, NULL}
+};
+#endif
+
+#ifdef __cplusplus
+namespace {
+  struct PyModuleDef __pyx_moduledef =
+  #else
+  static struct PyModuleDef __pyx_moduledef =
+  #endif
+  {
+      PyModuleDef_HEAD_INIT,
+      "_bitset",
+      0, /* m_doc */
+    #if CYTHON_PEP489_MULTI_PHASE_INIT
+      0, /* m_size */
+    #elif CYTHON_USE_MODULE_STATE
+      sizeof(__pyx_mstate), /* m_size */
+    #else
+      -1, /* m_size */
+    #endif
+      __pyx_methods /* m_methods */,
+    #if CYTHON_PEP489_MULTI_PHASE_INIT
+      __pyx_moduledef_slots, /* m_slots */
+    #else
+      NULL, /* m_reload */
+    #endif
+    #if CYTHON_USE_MODULE_STATE
+      __pyx_m_traverse, /* m_traverse */
+      __pyx_m_clear, /* m_clear */
+      NULL /* m_free */
+    #else
+      NULL, /* m_traverse */
+      NULL, /* m_clear */
+      NULL /* m_free */
+    #endif
+  };
+  #ifdef __cplusplus
+} /* anonymous namespace */
+#endif
+#endif
+
 #ifndef CYTHON_NO_PYINIT_EXPORT
 #define __Pyx_PyMODINIT_FUNC PyMODINIT_FUNC
 #elif PY_MAJOR_VERSION < 3
 #ifdef __cplusplus
 #define __Pyx_PyMODINIT_FUNC extern "C" void
 #else
 #define __Pyx_PyMODINIT_FUNC void
@@ -6991,42 +10415,56 @@
         PyErr_SetString(
             PyExc_ImportError,
             "Interpreter change detected - this module can only be loaded into one interpreter per process.");
         return -1;
     }
     return 0;
 }
-static CYTHON_SMALL_CODE int __Pyx_copy_spec_to_module(PyObject *spec, PyObject *moddict, const char* from_name, const char* to_name, int allow_none) {
+#if CYTHON_COMPILING_IN_LIMITED_API
+static CYTHON_SMALL_CODE int __Pyx_copy_spec_to_module(PyObject *spec, PyObject *module, const char* from_name, const char* to_name, int allow_none)
+#else
+static CYTHON_SMALL_CODE int __Pyx_copy_spec_to_module(PyObject *spec, PyObject *moddict, const char* from_name, const char* to_name, int allow_none)
+#endif
+{
     PyObject *value = PyObject_GetAttrString(spec, from_name);
     int result = 0;
     if (likely(value)) {
         if (allow_none || value != Py_None) {
+#if CYTHON_COMPILING_IN_LIMITED_API
+            result = PyModule_AddObject(module, to_name, value);
+#else
             result = PyDict_SetItemString(moddict, to_name, value);
+#endif
         }
         Py_DECREF(value);
     } else if (PyErr_ExceptionMatches(PyExc_AttributeError)) {
         PyErr_Clear();
     } else {
         result = -1;
     }
     return result;
 }
-static CYTHON_SMALL_CODE PyObject* __pyx_pymod_create(PyObject *spec, CYTHON_UNUSED PyModuleDef *def) {
+static CYTHON_SMALL_CODE PyObject* __pyx_pymod_create(PyObject *spec, PyModuleDef *def) {
     PyObject *module = NULL, *moddict, *modname;
+    CYTHON_UNUSED_VAR(def);
     if (__Pyx_check_single_interpreter())
         return NULL;
     if (__pyx_m)
         return __Pyx_NewRef(__pyx_m);
     modname = PyObject_GetAttrString(spec, "name");
     if (unlikely(!modname)) goto bad;
     module = PyModule_NewObject(modname);
     Py_DECREF(modname);
     if (unlikely(!module)) goto bad;
+#if CYTHON_COMPILING_IN_LIMITED_API
+    moddict = module;
+#else
     moddict = PyModule_GetDict(module);
     if (unlikely(!moddict)) goto bad;
+#endif
     if (unlikely(__Pyx_copy_spec_to_module(spec, moddict, "loader", "__loader__", 1) < 0)) goto bad;
     if (unlikely(__Pyx_copy_spec_to_module(spec, moddict, "origin", "__file__", 1) < 0)) goto bad;
     if (unlikely(__Pyx_copy_spec_to_module(spec, moddict, "parent", "__package__", 1) < 0)) goto bad;
     if (unlikely(__Pyx_copy_spec_to_module(spec, moddict, "submodule_search_locations", "__path__", 0) < 0)) goto bad;
     return module;
 bad:
     Py_XDECREF(module);
@@ -7034,28 +10472,62 @@
 }
 
 
 static CYTHON_SMALL_CODE int __pyx_pymod_exec__bitset(PyObject *__pyx_pyinit_module)
 #endif
 #endif
 {
+  int stringtab_initialized = 0;
+  #if CYTHON_USE_MODULE_STATE
+  int pystate_addmodule_run = 0;
+  #endif
   PyObject *__pyx_t_1 = NULL;
+  PyObject *__pyx_t_2 = NULL;
   int __pyx_lineno = 0;
   const char *__pyx_filename = NULL;
   int __pyx_clineno = 0;
   __Pyx_RefNannyDeclarations
   #if CYTHON_PEP489_MULTI_PHASE_INIT
   if (__pyx_m) {
     if (__pyx_m == __pyx_pyinit_module) return 0;
     PyErr_SetString(PyExc_RuntimeError, "Module '_bitset' has already been imported. Re-initialisation is not supported.");
     return -1;
   }
   #elif PY_MAJOR_VERSION >= 3
   if (__pyx_m) return __Pyx_NewRef(__pyx_m);
   #endif
+  /*--- Module creation code ---*/
+  #if CYTHON_PEP489_MULTI_PHASE_INIT
+  __pyx_m = __pyx_pyinit_module;
+  Py_INCREF(__pyx_m);
+  #else
+  #if PY_MAJOR_VERSION < 3
+  __pyx_m = Py_InitModule4("_bitset", __pyx_methods, 0, 0, PYTHON_API_VERSION); Py_XINCREF(__pyx_m);
+  if (unlikely(!__pyx_m)) __PYX_ERR(0, 1, __pyx_L1_error)
+  #elif CYTHON_USE_MODULE_STATE
+  __pyx_t_1 = PyModule_Create(&__pyx_moduledef); if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 1, __pyx_L1_error)
+  {
+    int add_module_result = PyState_AddModule(__pyx_t_1, &__pyx_moduledef);
+    __pyx_t_1 = 0; /* transfer ownership from __pyx_t_1 to _bitset pseudovariable */
+    if (unlikely((add_module_result < 0))) __PYX_ERR(0, 1, __pyx_L1_error)
+    pystate_addmodule_run = 1;
+  }
+  #else
+  __pyx_m = PyModule_Create(&__pyx_moduledef);
+  if (unlikely(!__pyx_m)) __PYX_ERR(0, 1, __pyx_L1_error)
+  #endif
+  #endif
+  CYTHON_UNUSED_VAR(__pyx_t_1);
+  __pyx_d = PyModule_GetDict(__pyx_m); if (unlikely(!__pyx_d)) __PYX_ERR(0, 1, __pyx_L1_error)
+  Py_INCREF(__pyx_d);
+  __pyx_b = PyImport_AddModule(__Pyx_BUILTIN_MODULE_NAME); if (unlikely(!__pyx_b)) __PYX_ERR(0, 1, __pyx_L1_error)
+  Py_INCREF(__pyx_b);
+  __pyx_cython_runtime = PyImport_AddModule((char *) "cython_runtime"); if (unlikely(!__pyx_cython_runtime)) __PYX_ERR(0, 1, __pyx_L1_error)
+  Py_INCREF(__pyx_cython_runtime);
+  if (PyObject_SetAttrString(__pyx_m, "__builtins__", __pyx_b) < 0) __PYX_ERR(0, 1, __pyx_L1_error)
   #if CYTHON_REFNANNY
 __Pyx_RefNanny = __Pyx_RefNannyImportAPI("refnanny");
 if (!__Pyx_RefNanny) {
   PyErr_Clear();
   __Pyx_RefNanny = __Pyx_RefNannyImportAPI("Cython.Runtime.refnanny");
   if (!__Pyx_RefNanny)
       Py_FatalError("failed to import 'refnanny' module");
@@ -7066,121 +10538,562 @@
   #ifdef __Pxy_PyFrame_Initialize_Offsets
   __Pxy_PyFrame_Initialize_Offsets();
   #endif
   __pyx_empty_tuple = PyTuple_New(0); if (unlikely(!__pyx_empty_tuple)) __PYX_ERR(0, 1, __pyx_L1_error)
   __pyx_empty_bytes = PyBytes_FromStringAndSize("", 0); if (unlikely(!__pyx_empty_bytes)) __PYX_ERR(0, 1, __pyx_L1_error)
   __pyx_empty_unicode = PyUnicode_FromStringAndSize("", 0); if (unlikely(!__pyx_empty_unicode)) __PYX_ERR(0, 1, __pyx_L1_error)
   #ifdef __Pyx_CyFunction_USED
-  if (__pyx_CyFunction_init() < 0) __PYX_ERR(0, 1, __pyx_L1_error)
+  if (__pyx_CyFunction_init(__pyx_m) < 0) __PYX_ERR(0, 1, __pyx_L1_error)
   #endif
   #ifdef __Pyx_FusedFunction_USED
-  if (__pyx_FusedFunction_init() < 0) __PYX_ERR(0, 1, __pyx_L1_error)
+  if (__pyx_FusedFunction_init(__pyx_m) < 0) __PYX_ERR(0, 1, __pyx_L1_error)
   #endif
   #ifdef __Pyx_Coroutine_USED
-  if (__pyx_Coroutine_init() < 0) __PYX_ERR(0, 1, __pyx_L1_error)
+  if (__pyx_Coroutine_init(__pyx_m) < 0) __PYX_ERR(0, 1, __pyx_L1_error)
   #endif
   #ifdef __Pyx_Generator_USED
-  if (__pyx_Generator_init() < 0) __PYX_ERR(0, 1, __pyx_L1_error)
+  if (__pyx_Generator_init(__pyx_m) < 0) __PYX_ERR(0, 1, __pyx_L1_error)
   #endif
   #ifdef __Pyx_AsyncGen_USED
-  if (__pyx_AsyncGen_init() < 0) __PYX_ERR(0, 1, __pyx_L1_error)
+  if (__pyx_AsyncGen_init(__pyx_m) < 0) __PYX_ERR(0, 1, __pyx_L1_error)
   #endif
   #ifdef __Pyx_StopAsyncIteration_USED
-  if (__pyx_StopAsyncIteration_init() < 0) __PYX_ERR(0, 1, __pyx_L1_error)
+  if (__pyx_StopAsyncIteration_init(__pyx_m) < 0) __PYX_ERR(0, 1, __pyx_L1_error)
   #endif
   /*--- Library function declarations ---*/
   /*--- Threads initialization code ---*/
   #if defined(WITH_THREAD) && PY_VERSION_HEX < 0x030700F0 && defined(__PYX_FORCE_INIT_THREADS) && __PYX_FORCE_INIT_THREADS
   PyEval_InitThreads();
   #endif
-  /*--- Module creation code ---*/
-  #if CYTHON_PEP489_MULTI_PHASE_INIT
-  __pyx_m = __pyx_pyinit_module;
-  Py_INCREF(__pyx_m);
-  #else
-  #if PY_MAJOR_VERSION < 3
-  __pyx_m = Py_InitModule4("_bitset", __pyx_methods, 0, 0, PYTHON_API_VERSION); Py_XINCREF(__pyx_m);
-  #else
-  __pyx_m = PyModule_Create(&__pyx_moduledef);
-  #endif
-  if (unlikely(!__pyx_m)) __PYX_ERR(0, 1, __pyx_L1_error)
-  #endif
-  __pyx_d = PyModule_GetDict(__pyx_m); if (unlikely(!__pyx_d)) __PYX_ERR(0, 1, __pyx_L1_error)
-  Py_INCREF(__pyx_d);
-  __pyx_b = PyImport_AddModule(__Pyx_BUILTIN_MODULE_NAME); if (unlikely(!__pyx_b)) __PYX_ERR(0, 1, __pyx_L1_error)
-  Py_INCREF(__pyx_b);
-  __pyx_cython_runtime = PyImport_AddModule((char *) "cython_runtime"); if (unlikely(!__pyx_cython_runtime)) __PYX_ERR(0, 1, __pyx_L1_error)
-  Py_INCREF(__pyx_cython_runtime);
-  if (PyObject_SetAttrString(__pyx_m, "__builtins__", __pyx_b) < 0) __PYX_ERR(0, 1, __pyx_L1_error)
   /*--- Initialize various global constants etc. ---*/
+  if (__Pyx_InitConstants() < 0) __PYX_ERR(0, 1, __pyx_L1_error)
+  stringtab_initialized = 1;
   if (__Pyx_InitGlobals() < 0) __PYX_ERR(0, 1, __pyx_L1_error)
   #if PY_MAJOR_VERSION < 3 && (__PYX_DEFAULT_STRING_ENCODING_IS_ASCII || __PYX_DEFAULT_STRING_ENCODING_IS_DEFAULT)
   if (__Pyx_init_sys_getdefaultencoding_params() < 0) __PYX_ERR(0, 1, __pyx_L1_error)
   #endif
   if (__pyx_module_is_main_pybitset__backends__cython___bitset) {
     if (PyObject_SetAttr(__pyx_m, __pyx_n_s_name, __pyx_n_s_main) < 0) __PYX_ERR(0, 1, __pyx_L1_error)
   }
   #if PY_MAJOR_VERSION >= 3
   {
     PyObject *modules = PyImport_GetModuleDict(); if (unlikely(!modules)) __PYX_ERR(0, 1, __pyx_L1_error)
     if (!PyDict_GetItemString(modules, "pybitset.backends.cython._bitset")) {
-      if (unlikely(PyDict_SetItemString(modules, "pybitset.backends.cython._bitset", __pyx_m) < 0)) __PYX_ERR(0, 1, __pyx_L1_error)
+      if (unlikely((PyDict_SetItemString(modules, "pybitset.backends.cython._bitset", __pyx_m) < 0))) __PYX_ERR(0, 1, __pyx_L1_error)
     }
   }
   #endif
   /*--- Builtin init code ---*/
   if (__Pyx_InitCachedBuiltins() < 0) __PYX_ERR(0, 1, __pyx_L1_error)
   /*--- Constants init code ---*/
   if (__Pyx_InitCachedConstants() < 0) __PYX_ERR(0, 1, __pyx_L1_error)
   /*--- Global type/function init code ---*/
   (void)__Pyx_modinit_global_init_code();
   (void)__Pyx_modinit_variable_export_code();
   (void)__Pyx_modinit_function_export_code();
-  if (unlikely(__Pyx_modinit_type_init_code() < 0)) __PYX_ERR(0, 1, __pyx_L1_error)
+  if (unlikely((__Pyx_modinit_type_init_code() < 0))) __PYX_ERR(0, 1, __pyx_L1_error)
   (void)__Pyx_modinit_type_import_code();
   (void)__Pyx_modinit_variable_import_code();
   (void)__Pyx_modinit_function_import_code();
   /*--- Execution code ---*/
   #if defined(__Pyx_Generator_USED) || defined(__Pyx_Coroutine_USED)
   if (__Pyx_patch_abc() < 0) __PYX_ERR(0, 1, __pyx_L1_error)
   #endif
 
+  /* "pybitset/backends/cython/_bitset.pyx":49
+ *         return self
+ * 
+ *     cpdef inline clear(self):             # <<<<<<<<<<<<<<
+ *         with nogil:
+ *             bitset_clear(self._bitset)
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_5clear, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet_clear, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__2)); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 49, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem((PyObject *)__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_dict, __pyx_n_s_clear, __pyx_t_2) < 0) __PYX_ERR(0, 49, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+  PyType_Modified(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+
+  /* "pybitset/backends/cython/_bitset.pyx":53
+ *             bitset_clear(self._bitset)
+ * 
+ *     cpdef inline fill(self):             # <<<<<<<<<<<<<<
+ *         with nogil:
+ *             bitset_fill(self._bitset)
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_7fill, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet_fill, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__3)); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 53, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem((PyObject *)__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_dict, __pyx_n_s_fill, __pyx_t_2) < 0) __PYX_ERR(0, 53, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+  PyType_Modified(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+
+  /* "pybitset/backends/cython/_bitset.pyx":57
+ *             bitset_fill(self._bitset)
+ * 
+ *     cpdef inline BitSet copy(self):             # <<<<<<<<<<<<<<
+ *         cdef bitset_t *ret
+ *         with nogil:
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_9copy, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet_copy, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__4)); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 57, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem((PyObject *)__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_dict, __pyx_n_s_copy, __pyx_t_2) < 0) __PYX_ERR(0, 57, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+  PyType_Modified(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+
+  /* "pybitset/backends/cython/_bitset.pyx":63
+ *         return BitSet.from_ptr(ret)
+ * 
+ *     cpdef inline bint resize(self, size_t newarraysize, bint padwithzeroes):             # <<<<<<<<<<<<<<
+ *         cdef bint ret
+ *         with nogil:
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_11resize, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet_resize, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__6)); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 63, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem((PyObject *)__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_dict, __pyx_n_s_resize, __pyx_t_2) < 0) __PYX_ERR(0, 63, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+  PyType_Modified(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+
+  /* "pybitset/backends/cython/_bitset.pyx":69
+ *         return ret
+ * 
+ *     cpdef inline size_t size_in_bytes(self):             # <<<<<<<<<<<<<<
+ *         cdef size_t ret
+ *         with nogil:
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_13size_in_bytes, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet_size_in_bytes, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__7)); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 69, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem((PyObject *)__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_dict, __pyx_n_s_size_in_bytes, __pyx_t_2) < 0) __PYX_ERR(0, 69, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+  PyType_Modified(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+
+  /* "pybitset/backends/cython/_bitset.pyx":75
+ *         return ret
+ * 
+ *     cpdef inline size_t size_in_bits(self):             # <<<<<<<<<<<<<<
+ *         cdef size_t ret
+ *         with nogil:
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_15size_in_bits, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet_size_in_bits, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__8)); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 75, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem((PyObject *)__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_dict, __pyx_n_s_size_in_bits, __pyx_t_2) < 0) __PYX_ERR(0, 75, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+  PyType_Modified(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+
+  /* "pybitset/backends/cython/_bitset.pyx":81
+ *         return ret
+ * 
+ *     cpdef inline size_t size_in_words(self):             # <<<<<<<<<<<<<<
+ *         cdef size_t ret
+ *         with nogil:
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_17size_in_words, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet_size_in_words, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__9)); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 81, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem((PyObject *)__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_dict, __pyx_n_s_size_in_words, __pyx_t_2) < 0) __PYX_ERR(0, 81, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+  PyType_Modified(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+
+  /* "pybitset/backends/cython/_bitset.pyx":87
+ *         return ret
+ * 
+ *     cpdef inline bint grow(self, size_t newarraysize):             # <<<<<<<<<<<<<<
+ *         cdef bint ret
+ *         with nogil:
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_19grow, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet_grow, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__11)); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 87, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem((PyObject *)__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_dict, __pyx_n_s_grow, __pyx_t_2) < 0) __PYX_ERR(0, 87, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+  PyType_Modified(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+
+  /* "pybitset/backends/cython/_bitset.pyx":93
+ *         return ret
+ * 
+ *     cpdef inline bint trim(self):             # <<<<<<<<<<<<<<
+ *         cdef bint ret
+ *         with nogil:
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_21trim, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet_trim, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__12)); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 93, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem((PyObject *)__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_dict, __pyx_n_s_trim, __pyx_t_2) < 0) __PYX_ERR(0, 93, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+  PyType_Modified(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+
+  /* "pybitset/backends/cython/_bitset.pyx":99
+ *         return ret
+ * 
+ *     cpdef inline shift_left(self, size_t s):             # <<<<<<<<<<<<<<
+ *         with nogil:
+ *             bitset_shift_left(self._bitset, s)
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_23shift_left, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet_shift_left, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__14)); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 99, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem((PyObject *)__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_dict, __pyx_n_s_shift_left, __pyx_t_2) < 0) __PYX_ERR(0, 99, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+  PyType_Modified(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+
+  /* "pybitset/backends/cython/_bitset.pyx":103
+ *             bitset_shift_left(self._bitset, s)
+ * 
+ *     cpdef inline shift_right(self, size_t s):             # <<<<<<<<<<<<<<
+ *         with nogil:
+ *             bitset_shift_right(self._bitset, s)
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_25shift_right, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet_shift_right, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__15)); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 103, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem((PyObject *)__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_dict, __pyx_n_s_shift_right, __pyx_t_2) < 0) __PYX_ERR(0, 103, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+  PyType_Modified(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+
+  /* "pybitset/backends/cython/_bitset.pyx":107
+ *             bitset_shift_right(self._bitset, s)
+ * 
+ *     cpdef inline set(self,  size_t i):             # <<<<<<<<<<<<<<
+ *         with nogil:
+ *             bitset_set(self._bitset, i)
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_27set, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet_set, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__17)); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 107, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem((PyObject *)__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_dict, __pyx_n_s_set, __pyx_t_2) < 0) __PYX_ERR(0, 107, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+  PyType_Modified(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+
+  /* "pybitset/backends/cython/_bitset.pyx":111
+ *             bitset_set(self._bitset, i)
+ * 
+ *     cpdef inline set_to_value(self, size_t i, bint flag):             # <<<<<<<<<<<<<<
+ *         with nogil:
+ *             bitset_set_to_value(self._bitset, i, flag)
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_29set_to_value, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet_set_to_value, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__19)); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 111, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem((PyObject *)__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_dict, __pyx_n_s_set_to_value, __pyx_t_2) < 0) __PYX_ERR(0, 111, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+  PyType_Modified(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+
+  /* "pybitset/backends/cython/_bitset.pyx":115
+ *             bitset_set_to_value(self._bitset, i, flag)
+ * 
+ *     cpdef inline bint get(self, size_t i):             # <<<<<<<<<<<<<<
+ *         cdef bint ret
+ *         with nogil:
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_31get, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet_get, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__20)); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 115, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem((PyObject *)__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_dict, __pyx_n_s_get, __pyx_t_2) < 0) __PYX_ERR(0, 115, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+  PyType_Modified(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+
+  /* "pybitset/backends/cython/_bitset.pyx":121
+ *         return ret
+ * 
+ *     cpdef inline size_t count(self):             # <<<<<<<<<<<<<<
+ *         cdef size_t ret
+ *         with nogil:
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_33count, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet_count, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__21)); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 121, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem((PyObject *)__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_dict, __pyx_n_s_count, __pyx_t_2) < 0) __PYX_ERR(0, 121, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+  PyType_Modified(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+
+  /* "pybitset/backends/cython/_bitset.pyx":127
+ *         return ret
+ * 
+ *     cpdef inline size_t minimum(self):             # <<<<<<<<<<<<<<
+ *         cdef size_t ret
+ *         with nogil:
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_35minimum, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet_minimum, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__22)); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 127, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem((PyObject *)__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_dict, __pyx_n_s_minimum, __pyx_t_2) < 0) __PYX_ERR(0, 127, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+  PyType_Modified(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+
+  /* "pybitset/backends/cython/_bitset.pyx":133
+ *         return ret
+ * 
+ *     cpdef inline size_t maximum(self):             # <<<<<<<<<<<<<<
+ *         cdef size_t ret
+ *         with nogil:
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_37maximum, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet_maximum, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__23)); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 133, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem((PyObject *)__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_dict, __pyx_n_s_maximum, __pyx_t_2) < 0) __PYX_ERR(0, 133, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+  PyType_Modified(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+
+  /* "pybitset/backends/cython/_bitset.pyx":139
+ *         return ret
+ * 
+ *     cpdef inline bint inplace_union(self, BitSet b2):             # <<<<<<<<<<<<<<
+ *         cdef bint ret
+ *         with nogil:
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_39inplace_union, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet_inplace_union, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__25)); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 139, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem((PyObject *)__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_dict, __pyx_n_s_inplace_union, __pyx_t_2) < 0) __PYX_ERR(0, 139, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+  PyType_Modified(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+
+  /* "pybitset/backends/cython/_bitset.pyx":145
+ *         return ret
+ * 
+ *     cpdef inline size_t union_count(self, BitSet b2):             # <<<<<<<<<<<<<<
+ *         cdef size_t ret
+ *         with nogil:
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_41union_count, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet_union_count, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__26)); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 145, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem((PyObject *)__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_dict, __pyx_n_s_union_count, __pyx_t_2) < 0) __PYX_ERR(0, 145, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+  PyType_Modified(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+
+  /* "pybitset/backends/cython/_bitset.pyx":151
+ *         return ret
+ * 
+ *     cpdef inline inplace_intersection(self, BitSet b2):             # <<<<<<<<<<<<<<
+ *         with nogil:
+ *             bitset_inplace_intersection(self._bitset, b2._bitset)
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_43inplace_intersection, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet_inplace_intersection, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__27)); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 151, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem((PyObject *)__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_dict, __pyx_n_s_inplace_intersection, __pyx_t_2) < 0) __PYX_ERR(0, 151, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+  PyType_Modified(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+
+  /* "pybitset/backends/cython/_bitset.pyx":155
+ *             bitset_inplace_intersection(self._bitset, b2._bitset)
+ * 
+ *     cpdef inline size_t intersection_count(self, BitSet b2):             # <<<<<<<<<<<<<<
+ *         cdef size_t ret
+ *         with nogil:
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_45intersection_count, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet_intersection_count, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__28)); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 155, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem((PyObject *)__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_dict, __pyx_n_s_intersection_count, __pyx_t_2) < 0) __PYX_ERR(0, 155, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+  PyType_Modified(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+
+  /* "pybitset/backends/cython/_bitset.pyx":161
+ *         return ret
+ * 
+ *     cpdef inline bint disjoint(self, BitSet b2):             # <<<<<<<<<<<<<<
+ *         cdef bint ret
+ *         with nogil:
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_47disjoint, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet_disjoint, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__29)); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 161, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem((PyObject *)__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_dict, __pyx_n_s_disjoint, __pyx_t_2) < 0) __PYX_ERR(0, 161, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+  PyType_Modified(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+
+  /* "pybitset/backends/cython/_bitset.pyx":167
+ *         return ret
+ * 
+ *     cpdef inline bint intersect(self, BitSet b2):             # <<<<<<<<<<<<<<
+ *         cdef bint ret
+ *         with nogil:
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_49intersect, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet_intersect, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__30)); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 167, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem((PyObject *)__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_dict, __pyx_n_s_intersect, __pyx_t_2) < 0) __PYX_ERR(0, 167, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+  PyType_Modified(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+
+  /* "pybitset/backends/cython/_bitset.pyx":173
+ *         return ret
+ * 
+ *     cpdef inline bint contains_all(self, BitSet b2):             # <<<<<<<<<<<<<<
+ *         cdef bint ret
+ *         with nogil:
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_51contains_all, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet_contains_all, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__31)); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 173, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem((PyObject *)__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_dict, __pyx_n_s_contains_all, __pyx_t_2) < 0) __PYX_ERR(0, 173, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+  PyType_Modified(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+
+  /* "pybitset/backends/cython/_bitset.pyx":179
+ *         return ret
+ * 
+ *     cpdef inline inplace_difference(self, BitSet b2):             # <<<<<<<<<<<<<<
+ *         with nogil:
+ *             bitset_inplace_difference(self._bitset, b2._bitset)
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_53inplace_difference, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet_inplace_difference, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__32)); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 179, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem((PyObject *)__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_dict, __pyx_n_s_inplace_difference, __pyx_t_2) < 0) __PYX_ERR(0, 179, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+  PyType_Modified(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+
+  /* "pybitset/backends/cython/_bitset.pyx":183
+ *             bitset_inplace_difference(self._bitset, b2._bitset)
+ * 
+ *     cpdef inline size_t difference_count(self, BitSet b2):             # <<<<<<<<<<<<<<
+ *         cdef size_t ret
+ *         with nogil:
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_55difference_count, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet_difference_count, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__33)); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 183, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem((PyObject *)__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_dict, __pyx_n_s_difference_count, __pyx_t_2) < 0) __PYX_ERR(0, 183, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+  PyType_Modified(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+
+  /* "pybitset/backends/cython/_bitset.pyx":189
+ *         return ret
+ * 
+ *     cpdef inline bint inplace_symmetric_difference(self, BitSet b2):             # <<<<<<<<<<<<<<
+ *         cdef bint ret
+ *         with nogil:
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_57inplace_symmetric_difference, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet_inplace_symmetric_differe, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__34)); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 189, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem((PyObject *)__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_dict, __pyx_n_s_inplace_symmetric_difference, __pyx_t_2) < 0) __PYX_ERR(0, 189, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+  PyType_Modified(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+
+  /* "pybitset/backends/cython/_bitset.pyx":195
+ *         return ret
+ * 
+ *     cpdef inline size_t symmetric_difference_count(self, BitSet b2):             # <<<<<<<<<<<<<<
+ *         cdef size_t ret
+ *         with nogil:
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_59symmetric_difference_count, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet_symmetric_difference_coun, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__35)); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 195, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem((PyObject *)__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_dict, __pyx_n_s_symmetric_difference_count, __pyx_t_2) < 0) __PYX_ERR(0, 195, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+  PyType_Modified(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+
+  /* "pybitset/backends/cython/_bitset.pyx":204
+ *         return BitSetIter(self)
+ * 
+ *     cpdef inline bint for_each(self, object func):             # <<<<<<<<<<<<<<
+ *         cdef bint ret
+ *         with nogil:
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_63for_each, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet_for_each, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__37)); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 204, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem((PyObject *)__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_dict, __pyx_n_s_for_each, __pyx_t_2) < 0) __PYX_ERR(0, 204, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+  PyType_Modified(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+
+  /* "pybitset/backends/cython/_bitset.pyx":210
+ *         return ret
+ * 
+ *     cpdef inline print(self):             # <<<<<<<<<<<<<<
+ *         with nogil:
+ *             bitset_print(self._bitset)
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_65print, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet_print, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__38)); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 210, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem((PyObject *)__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet->tp_dict, __pyx_n_s_print, __pyx_t_2) < 0) __PYX_ERR(0, 210, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+  PyType_Modified(__pyx_ptype_8pybitset_8backends_6cython_7_bitset_BitSet);
+
+  /* "(tree fragment)":1
+ * def __reduce_cython__(self):             # <<<<<<<<<<<<<<
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"
+ * def __setstate_cython__(self, __pyx_state):
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_67__reduce_cython__, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet___reduce_cython, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__39)); if (unlikely(!__pyx_t_2)) __PYX_ERR(1, 1, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem(__pyx_d, __pyx_n_s_reduce_cython, __pyx_t_2) < 0) __PYX_ERR(1, 1, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+
+  /* "(tree fragment)":3
+ * def __reduce_cython__(self):
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"
+ * def __setstate_cython__(self, __pyx_state):             # <<<<<<<<<<<<<<
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_6BitSet_69__setstate_cython__, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSet___setstate_cython, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__41)); if (unlikely(!__pyx_t_2)) __PYX_ERR(1, 3, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem(__pyx_d, __pyx_n_s_setstate_cython, __pyx_t_2) < 0) __PYX_ERR(1, 3, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+
+  /* "(tree fragment)":1
+ * def __reduce_cython__(self):             # <<<<<<<<<<<<<<
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"
+ * def __setstate_cython__(self, __pyx_state):
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_10BitSetIter_7__reduce_cython__, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSetIter___reduce_cython, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__42)); if (unlikely(!__pyx_t_2)) __PYX_ERR(1, 1, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem(__pyx_d, __pyx_n_s_reduce_cython, __pyx_t_2) < 0) __PYX_ERR(1, 1, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+
+  /* "(tree fragment)":3
+ * def __reduce_cython__(self):
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"
+ * def __setstate_cython__(self, __pyx_state):             # <<<<<<<<<<<<<<
+ *     raise TypeError, "no default __reduce__ due to non-trivial __cinit__"
+ */
+  __pyx_t_2 = __Pyx_CyFunction_New(&__pyx_mdef_8pybitset_8backends_6cython_7_bitset_10BitSetIter_9__setstate_cython__, __Pyx_CYFUNCTION_CCLASS, __pyx_n_s_BitSetIter___setstate_cython, NULL, __pyx_n_s_pybitset_backends_cython__bitset_2, __pyx_d, ((PyObject *)__pyx_codeobj__43)); if (unlikely(!__pyx_t_2)) __PYX_ERR(1, 3, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem(__pyx_d, __pyx_n_s_setstate_cython, __pyx_t_2) < 0) __PYX_ERR(1, 3, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
+
   /* "pybitset/backends/cython/_bitset.pyx":1
  * # cython: language_level=3             # <<<<<<<<<<<<<<
  * # cython: cdivision=True
  * cimport cython
  */
-  __pyx_t_1 = __Pyx_PyDict_NewPresized(0); if (unlikely(!__pyx_t_1)) __PYX_ERR(0, 1, __pyx_L1_error)
-  __Pyx_GOTREF(__pyx_t_1);
-  if (PyDict_SetItem(__pyx_d, __pyx_n_s_test, __pyx_t_1) < 0) __PYX_ERR(0, 1, __pyx_L1_error)
-  __Pyx_DECREF(__pyx_t_1); __pyx_t_1 = 0;
+  __pyx_t_2 = __Pyx_PyDict_NewPresized(0); if (unlikely(!__pyx_t_2)) __PYX_ERR(0, 1, __pyx_L1_error)
+  __Pyx_GOTREF(__pyx_t_2);
+  if (PyDict_SetItem(__pyx_d, __pyx_n_s_test, __pyx_t_2) < 0) __PYX_ERR(0, 1, __pyx_L1_error)
+  __Pyx_DECREF(__pyx_t_2); __pyx_t_2 = 0;
 
   /*--- Wrapped vars code ---*/
 
   goto __pyx_L0;
   __pyx_L1_error:;
-  __Pyx_XDECREF(__pyx_t_1);
+  __Pyx_XDECREF(__pyx_t_2);
   if (__pyx_m) {
-    if (__pyx_d) {
+    if (__pyx_d && stringtab_initialized) {
       __Pyx_AddTraceback("init pybitset.backends.cython._bitset", __pyx_clineno, __pyx_lineno, __pyx_filename);
     }
+    #if !CYTHON_USE_MODULE_STATE
     Py_CLEAR(__pyx_m);
+    #else
+    Py_DECREF(__pyx_m);
+    if (pystate_addmodule_run) {
+      PyObject *tp, *value, *tb;
+      PyErr_Fetch(&tp, &value, &tb);
+      PyState_RemoveModule(&__pyx_moduledef);
+      PyErr_Restore(tp, value, tb);
+    }
+    #endif
   } else if (!PyErr_Occurred()) {
     PyErr_SetString(PyExc_ImportError, "init pybitset.backends.cython._bitset");
   }
   __pyx_L0:;
   __Pyx_RefNannyFinishContext();
   #if CYTHON_PEP489_MULTI_PHASE_INIT
   return (__pyx_m != NULL) ? 0 : -1;
   #elif PY_MAJOR_VERSION >= 3
   return __pyx_m;
   #else
   return;
   #endif
 }
+/* #### Code section: cleanup_globals ### */
+/* #### Code section: cleanup_module ### */
+/* #### Code section: main_method ### */
+/* #### Code section: utility_code_pragmas ### */
+#ifdef _MSC_VER
+#pragma warning( push )
+/* Warning 4127: conditional expression is constant
+ * Cython uses constant conditional expressions to allow in inline functions to be optimized at
+ * compile-time, so this warning is not useful
+ */
+#pragma warning( disable : 4127 )
+#endif
+
+
+
+/* #### Code section: utility_code_def ### */
 
 /* --- Runtime support code --- */
 /* Refnanny */
 #if CYTHON_REFNANNY
 static __Pyx_RefNannyAPIStruct *__Pyx_RefNannyImportAPI(const char *modname) {
     PyObject *m = NULL, *p = NULL;
     void *r = NULL;
@@ -7192,67 +11105,166 @@
 end:
     Py_XDECREF(p);
     Py_XDECREF(m);
     return (__Pyx_RefNannyAPIStruct *)r;
 }
 #endif
 
+/* PyErrExceptionMatches */
+#if CYTHON_FAST_THREAD_STATE
+static int __Pyx_PyErr_ExceptionMatchesTuple(PyObject *exc_type, PyObject *tuple) {
+    Py_ssize_t i, n;
+    n = PyTuple_GET_SIZE(tuple);
+#if PY_MAJOR_VERSION >= 3
+    for (i=0; i<n; i++) {
+        if (exc_type == PyTuple_GET_ITEM(tuple, i)) return 1;
+    }
+#endif
+    for (i=0; i<n; i++) {
+        if (__Pyx_PyErr_GivenExceptionMatches(exc_type, PyTuple_GET_ITEM(tuple, i))) return 1;
+    }
+    return 0;
+}
+static CYTHON_INLINE int __Pyx_PyErr_ExceptionMatchesInState(PyThreadState* tstate, PyObject* err) {
+    int result;
+    PyObject *exc_type;
+#if PY_VERSION_HEX >= 0x030C00A6
+    PyObject *current_exception = tstate->current_exception;
+    if (unlikely(!current_exception)) return 0;
+    exc_type = (PyObject*) Py_TYPE(current_exception);
+    if (exc_type == err) return 1;
+#else
+    exc_type = tstate->curexc_type;
+    if (exc_type == err) return 1;
+    if (unlikely(!exc_type)) return 0;
+#endif
+    #if CYTHON_AVOID_BORROWED_REFS
+    Py_INCREF(exc_type);
+    #endif
+    if (unlikely(PyTuple_Check(err))) {
+        result = __Pyx_PyErr_ExceptionMatchesTuple(exc_type, err);
+    } else {
+        result = __Pyx_PyErr_GivenExceptionMatches(exc_type, err);
+    }
+    #if CYTHON_AVOID_BORROWED_REFS
+    Py_DECREF(exc_type);
+    #endif
+    return result;
+}
+#endif
+
+/* PyErrFetchRestore */
+#if CYTHON_FAST_THREAD_STATE
+static CYTHON_INLINE void __Pyx_ErrRestoreInState(PyThreadState *tstate, PyObject *type, PyObject *value, PyObject *tb) {
+#if PY_VERSION_HEX >= 0x030C00A6
+    PyObject *tmp_value;
+    assert(type == NULL || (value != NULL && type == (PyObject*) Py_TYPE(value)));
+    if (value) {
+        #if CYTHON_COMPILING_IN_CPYTHON
+        if (unlikely(((PyBaseExceptionObject*) value)->traceback != tb))
+        #endif
+            PyException_SetTraceback(value, tb);
+    }
+    tmp_value = tstate->current_exception;
+    tstate->current_exception = value;
+    Py_XDECREF(tmp_value);
+#else
+    PyObject *tmp_type, *tmp_value, *tmp_tb;
+    tmp_type = tstate->curexc_type;
+    tmp_value = tstate->curexc_value;
+    tmp_tb = tstate->curexc_traceback;
+    tstate->curexc_type = type;
+    tstate->curexc_value = value;
+    tstate->curexc_traceback = tb;
+    Py_XDECREF(tmp_type);
+    Py_XDECREF(tmp_value);
+    Py_XDECREF(tmp_tb);
+#endif
+}
+static CYTHON_INLINE void __Pyx_ErrFetchInState(PyThreadState *tstate, PyObject **type, PyObject **value, PyObject **tb) {
+#if PY_VERSION_HEX >= 0x030C00A6
+    PyObject* exc_value;
+    exc_value = tstate->current_exception;
+    tstate->current_exception = 0;
+    *value = exc_value;
+    *type = NULL;
+    *tb = NULL;
+    if (exc_value) {
+        *type = (PyObject*) Py_TYPE(exc_value);
+        Py_INCREF(*type);
+        #if CYTHON_COMPILING_IN_CPYTHON
+        *tb = ((PyBaseExceptionObject*) exc_value)->traceback;
+        Py_XINCREF(*tb);
+        #else
+        *tb = PyException_GetTraceback(exc_value);
+        #endif
+    }
+#else
+    *type = tstate->curexc_type;
+    *value = tstate->curexc_value;
+    *tb = tstate->curexc_traceback;
+    tstate->curexc_type = 0;
+    tstate->curexc_value = 0;
+    tstate->curexc_traceback = 0;
+#endif
+}
+#endif
+
 /* PyObjectGetAttrStr */
 #if CYTHON_USE_TYPE_SLOTS
 static CYTHON_INLINE PyObject* __Pyx_PyObject_GetAttrStr(PyObject* obj, PyObject* attr_name) {
     PyTypeObject* tp = Py_TYPE(obj);
     if (likely(tp->tp_getattro))
         return tp->tp_getattro(obj, attr_name);
 #if PY_MAJOR_VERSION < 3
     if (likely(tp->tp_getattr))
         return tp->tp_getattr(obj, PyString_AS_STRING(attr_name));
 #endif
     return PyObject_GetAttr(obj, attr_name);
 }
 #endif
 
+/* PyObjectGetAttrStrNoError */
+static void __Pyx_PyObject_GetAttrStr_ClearAttributeError(void) {
+    __Pyx_PyThreadState_declare
+    __Pyx_PyThreadState_assign
+    if (likely(__Pyx_PyErr_ExceptionMatches(PyExc_AttributeError)))
+        __Pyx_PyErr_Clear();
+}
+static CYTHON_INLINE PyObject* __Pyx_PyObject_GetAttrStrNoError(PyObject* obj, PyObject* attr_name) {
+    PyObject *result;
+#if CYTHON_COMPILING_IN_CPYTHON && CYTHON_USE_TYPE_SLOTS && PY_VERSION_HEX >= 0x030700B1
+    PyTypeObject* tp = Py_TYPE(obj);
+    if (likely(tp->tp_getattro == PyObject_GenericGetAttr)) {
+        return _PyObject_GenericGetAttrWithDict(obj, attr_name, NULL, 1);
+    }
+#endif
+    result = __Pyx_PyObject_GetAttrStr(obj, attr_name);
+    if (unlikely(!result)) {
+        __Pyx_PyObject_GetAttrStr_ClearAttributeError();
+    }
+    return result;
+}
+
 /* GetBuiltinName */
 static PyObject *__Pyx_GetBuiltinName(PyObject *name) {
-    PyObject* result = __Pyx_PyObject_GetAttrStr(__pyx_b, name);
-    if (unlikely(!result)) {
+    PyObject* result = __Pyx_PyObject_GetAttrStrNoError(__pyx_b, name);
+    if (unlikely(!result) && !PyErr_Occurred()) {
         PyErr_Format(PyExc_NameError,
 #if PY_MAJOR_VERSION >= 3
             "name '%U' is not defined", name);
 #else
             "name '%.200s' is not defined", PyString_AS_STRING(name));
 #endif
     }
     return result;
 }
 
-/* PyCFunctionFastCall */
-#if CYTHON_FAST_PYCCALL
-static CYTHON_INLINE PyObject * __Pyx_PyCFunction_FastCall(PyObject *func_obj, PyObject **args, Py_ssize_t nargs) {
-    PyCFunctionObject *func = (PyCFunctionObject*)func_obj;
-    PyCFunction meth = PyCFunction_GET_FUNCTION(func);
-    PyObject *self = PyCFunction_GET_SELF(func);
-    int flags = PyCFunction_GET_FLAGS(func);
-    assert(PyCFunction_Check(func));
-    assert(METH_FASTCALL == (flags & ~(METH_CLASS | METH_STATIC | METH_COEXIST | METH_KEYWORDS | METH_STACKLESS)));
-    assert(nargs >= 0);
-    assert(nargs == 0 || args != NULL);
-    /* _PyCFunction_FastCallDict() must not be called with an exception set,
-       because it may clear it (directly or indirectly) and so the
-       caller loses its exception */
-    assert(!PyErr_Occurred());
-    if ((PY_VERSION_HEX < 0x030700A0) || unlikely(flags & METH_KEYWORDS)) {
-        return (*((__Pyx_PyCFunctionFastWithKeywords)(void*)meth)) (self, args, nargs, NULL);
-    } else {
-        return (*((__Pyx_PyCFunctionFast)(void*)meth)) (self, args, nargs);
-    }
-}
-#endif
-
 /* PyFunctionFastCall */
-#if CYTHON_FAST_PYCALL
+#if CYTHON_FAST_PYCALL && !CYTHON_VECTORCALL
 static PyObject* __Pyx_PyFunction_FastCallNoKw(PyCodeObject *co, PyObject **args, Py_ssize_t na,
                                                PyObject *globals) {
     PyFrameObject *f;
     PyThreadState *tstate = __Pyx_PyThreadState_Current;
     PyObject **fastlocals;
     Py_ssize_t i;
     PyObject *result;
@@ -7273,15 +11285,14 @@
     }
     result = PyEval_EvalFrameEx(f,0);
     ++tstate->recursion_depth;
     Py_DECREF(f);
     --tstate->recursion_depth;
     return result;
 }
-#if 1 || PY_VERSION_HEX < 0x030600B1
 static PyObject *__Pyx_PyFunction_FastCallDict(PyObject *func, PyObject **args, Py_ssize_t nargs, PyObject *kwargs) {
     PyCodeObject *co = (PyCodeObject *)PyFunction_GET_CODE(func);
     PyObject *globals = PyFunction_GET_GLOBALS(func);
     PyObject *argdefs = PyFunction_GET_DEFAULTS(func);
     PyObject *closure;
 #if PY_MAJOR_VERSION >= 3
     PyObject *kwdefs;
@@ -7289,15 +11300,15 @@
     PyObject *kwtuple, **k;
     PyObject **d;
     Py_ssize_t nd;
     Py_ssize_t nk;
     PyObject *result;
     assert(kwargs == NULL || PyDict_Check(kwargs));
     nk = kwargs ? PyDict_Size(kwargs) : 0;
-    if (Py_EnterRecursiveCall((char*)" while calling a Python object")) {
+    if (unlikely(Py_EnterRecursiveCall((char*)" while calling a Python object"))) {
         return NULL;
     }
     if (
 #if PY_MAJOR_VERSION >= 3
             co->co_kwonlyargcount == 0 &&
 #endif
             likely(kwargs == NULL || nk == 0) &&
@@ -7360,15 +11371,14 @@
 #endif
     Py_XDECREF(kwtuple);
 done:
     Py_LeaveRecursiveCall();
     return result;
 }
 #endif
-#endif
 
 /* PyObjectCall */
 #if CYTHON_COMPILING_IN_CPYTHON
 static CYTHON_INLINE PyObject* __Pyx_PyObject_Call(PyObject *func, PyObject *arg, PyObject *kw) {
     PyObject *result;
     ternaryfunc call = Py_TYPE(func)->tp_call;
     if (unlikely(!call))
@@ -7382,43 +11392,14 @@
             PyExc_SystemError,
             "NULL result without error in PyObject_Call");
     }
     return result;
 }
 #endif
 
-/* PyObjectCall2Args */
-static CYTHON_UNUSED PyObject* __Pyx_PyObject_Call2Args(PyObject* function, PyObject* arg1, PyObject* arg2) {
-    PyObject *args, *result = NULL;
-    #if CYTHON_FAST_PYCALL
-    if (PyFunction_Check(function)) {
-        PyObject *args[2] = {arg1, arg2};
-        return __Pyx_PyFunction_FastCall(function, args, 2);
-    }
-    #endif
-    #if CYTHON_FAST_PYCCALL
-    if (__Pyx_PyFastCFunction_Check(function)) {
-        PyObject *args[2] = {arg1, arg2};
-        return __Pyx_PyCFunction_FastCall(function, args, 2);
-    }
-    #endif
-    args = PyTuple_New(2);
-    if (unlikely(!args)) goto done;
-    Py_INCREF(arg1);
-    PyTuple_SET_ITEM(args, 0, arg1);
-    Py_INCREF(arg2);
-    PyTuple_SET_ITEM(args, 1, arg2);
-    Py_INCREF(function);
-    result = __Pyx_PyObject_Call(function, args, NULL);
-    Py_DECREF(args);
-    Py_DECREF(function);
-done:
-    return result;
-}
-
 /* PyObjectCallMethO */
 #if CYTHON_COMPILING_IN_CPYTHON
 static CYTHON_INLINE PyObject* __Pyx_PyObject_CallMethO(PyObject *func, PyObject *arg) {
     PyObject *self, *result;
     PyCFunction cfunc;
     cfunc = PyCFunction_GET_FUNCTION(func);
     self = PyCFunction_GET_SELF(func);
@@ -7431,91 +11412,108 @@
             PyExc_SystemError,
             "NULL result without error in PyObject_Call");
     }
     return result;
 }
 #endif
 
-/* PyObjectCallOneArg */
-#if CYTHON_COMPILING_IN_CPYTHON
-static PyObject* __Pyx__PyObject_CallOneArg(PyObject *func, PyObject *arg) {
+/* PyObjectFastCall */
+static PyObject* __Pyx_PyObject_FastCall_fallback(PyObject *func, PyObject **args, size_t nargs, PyObject *kwargs) {
+    PyObject *argstuple;
     PyObject *result;
-    PyObject *args = PyTuple_New(1);
-    if (unlikely(!args)) return NULL;
-    Py_INCREF(arg);
-    PyTuple_SET_ITEM(args, 0, arg);
-    result = __Pyx_PyObject_Call(func, args, NULL);
-    Py_DECREF(args);
+    size_t i;
+    argstuple = PyTuple_New((Py_ssize_t)nargs);
+    if (unlikely(!argstuple)) return NULL;
+    for (i = 0; i < nargs; i++) {
+        Py_INCREF(args[i]);
+        PyTuple_SET_ITEM(argstuple, (Py_ssize_t)i, args[i]);
+    }
+    result = __Pyx_PyObject_Call(func, argstuple, kwargs);
+    Py_DECREF(argstuple);
     return result;
 }
-static CYTHON_INLINE PyObject* __Pyx_PyObject_CallOneArg(PyObject *func, PyObject *arg) {
-#if CYTHON_FAST_PYCALL
-    if (PyFunction_Check(func)) {
-        return __Pyx_PyFunction_FastCall(func, &arg, 1);
-    }
-#endif
-    if (likely(PyCFunction_Check(func))) {
-        if (likely(PyCFunction_GET_FLAGS(func) & METH_O)) {
-            return __Pyx_PyObject_CallMethO(func, arg);
-#if CYTHON_FAST_PYCCALL
-        } else if (__Pyx_PyFastCFunction_Check(func)) {
-            return __Pyx_PyCFunction_FastCall(func, &arg, 1);
+static CYTHON_INLINE PyObject* __Pyx_PyObject_FastCallDict(PyObject *func, PyObject **args, size_t _nargs, PyObject *kwargs) {
+    Py_ssize_t nargs = __Pyx_PyVectorcall_NARGS(_nargs);
+#if CYTHON_COMPILING_IN_CPYTHON
+    if (nargs == 0 && kwargs == NULL) {
+#if defined(__Pyx_CyFunction_USED) && defined(NDEBUG)
+        if (__Pyx_IsCyOrPyCFunction(func))
+#else
+        if (PyCFunction_Check(func))
 #endif
+        {
+            if (likely(PyCFunction_GET_FLAGS(func) & METH_NOARGS)) {
+                return __Pyx_PyObject_CallMethO(func, NULL);
+            }
+        }
+    }
+    else if (nargs == 1 && kwargs == NULL) {
+        if (PyCFunction_Check(func))
+        {
+            if (likely(PyCFunction_GET_FLAGS(func) & METH_O)) {
+                return __Pyx_PyObject_CallMethO(func, args[0]);
+            }
         }
     }
-    return __Pyx__PyObject_CallOneArg(func, arg);
-}
-#else
-static CYTHON_INLINE PyObject* __Pyx_PyObject_CallOneArg(PyObject *func, PyObject *arg) {
-    PyObject *result;
-    PyObject *args = PyTuple_Pack(1, arg);
-    if (unlikely(!args)) return NULL;
-    result = __Pyx_PyObject_Call(func, args, NULL);
-    Py_DECREF(args);
-    return result;
-}
 #endif
-
-/* PyErrFetchRestore */
-#if CYTHON_FAST_THREAD_STATE
-static CYTHON_INLINE void __Pyx_ErrRestoreInState(PyThreadState *tstate, PyObject *type, PyObject *value, PyObject *tb) {
-    PyObject *tmp_type, *tmp_value, *tmp_tb;
-    tmp_type = tstate->curexc_type;
-    tmp_value = tstate->curexc_value;
-    tmp_tb = tstate->curexc_traceback;
-    tstate->curexc_type = type;
-    tstate->curexc_value = value;
-    tstate->curexc_traceback = tb;
-    Py_XDECREF(tmp_type);
-    Py_XDECREF(tmp_value);
-    Py_XDECREF(tmp_tb);
-}
-static CYTHON_INLINE void __Pyx_ErrFetchInState(PyThreadState *tstate, PyObject **type, PyObject **value, PyObject **tb) {
-    *type = tstate->curexc_type;
-    *value = tstate->curexc_value;
-    *tb = tstate->curexc_traceback;
-    tstate->curexc_type = 0;
-    tstate->curexc_value = 0;
-    tstate->curexc_traceback = 0;
+    #if PY_VERSION_HEX < 0x030800B1
+    #if CYTHON_FAST_PYCCALL
+    if (PyCFunction_Check(func)) {
+        if (kwargs) {
+            return _PyCFunction_FastCallDict(func, args, nargs, kwargs);
+        } else {
+            return _PyCFunction_FastCallKeywords(func, args, nargs, NULL);
+        }
+    }
+    #if PY_VERSION_HEX >= 0x030700A1
+    if (!kwargs && __Pyx_IS_TYPE(func, &PyMethodDescr_Type)) {
+        return _PyMethodDescr_FastCallKeywords(func, args, nargs, NULL);
+    }
+    #endif
+    #endif
+    #if CYTHON_FAST_PYCALL
+    if (PyFunction_Check(func)) {
+        return __Pyx_PyFunction_FastCallDict(func, args, nargs, kwargs);
+    }
+    #endif
+    #endif
+    #if CYTHON_VECTORCALL
+    vectorcallfunc f = _PyVectorcall_Function(func);
+    if (f) {
+        return f(func, args, (size_t)nargs, kwargs);
+    }
+    #elif defined(__Pyx_CyFunction_USED) && CYTHON_BACKPORT_VECTORCALL
+    if (__Pyx_CyFunction_CheckExact(func)) {
+        __pyx_vectorcallfunc f = __Pyx_CyFunction_func_vectorcall(func);
+        if (f) return f(func, args, (size_t)nargs, kwargs);
+    }
+    #endif
+    if (nargs == 0) {
+        return __Pyx_PyObject_Call(func, __pyx_empty_tuple, kwargs);
+    }
+    return __Pyx_PyObject_FastCall_fallback(func, args, (size_t)nargs, kwargs);
 }
-#endif
 
 /* WriteUnraisableException */
-static void __Pyx_WriteUnraisable(const char *name, CYTHON_UNUSED int clineno,
-                                  CYTHON_UNUSED int lineno, CYTHON_UNUSED const char *filename,
-                                  int full_traceback, CYTHON_UNUSED int nogil) {
+static void __Pyx_WriteUnraisable(const char *name, int clineno,
+                                  int lineno, const char *filename,
+                                  int full_traceback, int nogil) {
     PyObject *old_exc, *old_val, *old_tb;
     PyObject *ctx;
     __Pyx_PyThreadState_declare
 #ifdef WITH_THREAD
     PyGILState_STATE state;
     if (nogil)
         state = PyGILState_Ensure();
     else state = (PyGILState_STATE)0;
 #endif
+    CYTHON_UNUSED_VAR(clineno);
+    CYTHON_UNUSED_VAR(lineno);
+    CYTHON_UNUSED_VAR(filename);
+    CYTHON_MAYBE_UNUSED_VAR(nogil);
     __Pyx_PyThreadState_assign
     __Pyx_ErrFetch(&old_exc, &old_val, &old_tb);
     if (full_traceback) {
         Py_XINCREF(old_exc);
         Py_XINCREF(old_val);
         Py_XINCREF(old_tb);
         __Pyx_ErrRestore(old_exc, old_val, old_tb);
@@ -7535,14 +11533,221 @@
     }
 #ifdef WITH_THREAD
     if (nogil)
         PyGILState_Release(state);
 #endif
 }
 
+/* TupleAndListFromArray */
+#if CYTHON_COMPILING_IN_CPYTHON
+static CYTHON_INLINE void __Pyx_copy_object_array(PyObject *const *CYTHON_RESTRICT src, PyObject** CYTHON_RESTRICT dest, Py_ssize_t length) {
+    PyObject *v;
+    Py_ssize_t i;
+    for (i = 0; i < length; i++) {
+        v = dest[i] = src[i];
+        Py_INCREF(v);
+    }
+}
+static CYTHON_INLINE PyObject *
+__Pyx_PyTuple_FromArray(PyObject *const *src, Py_ssize_t n)
+{
+    PyObject *res;
+    if (n <= 0) {
+        Py_INCREF(__pyx_empty_tuple);
+        return __pyx_empty_tuple;
+    }
+    res = PyTuple_New(n);
+    if (unlikely(res == NULL)) return NULL;
+    __Pyx_copy_object_array(src, ((PyTupleObject*)res)->ob_item, n);
+    return res;
+}
+static CYTHON_INLINE PyObject *
+__Pyx_PyList_FromArray(PyObject *const *src, Py_ssize_t n)
+{
+    PyObject *res;
+    if (n <= 0) {
+        return PyList_New(0);
+    }
+    res = PyList_New(n);
+    if (unlikely(res == NULL)) return NULL;
+    __Pyx_copy_object_array(src, ((PyListObject*)res)->ob_item, n);
+    return res;
+}
+#endif
+
+/* BytesEquals */
+static CYTHON_INLINE int __Pyx_PyBytes_Equals(PyObject* s1, PyObject* s2, int equals) {
+#if CYTHON_COMPILING_IN_PYPY || CYTHON_COMPILING_IN_LIMITED_API
+    return PyObject_RichCompareBool(s1, s2, equals);
+#else
+    if (s1 == s2) {
+        return (equals == Py_EQ);
+    } else if (PyBytes_CheckExact(s1) & PyBytes_CheckExact(s2)) {
+        const char *ps1, *ps2;
+        Py_ssize_t length = PyBytes_GET_SIZE(s1);
+        if (length != PyBytes_GET_SIZE(s2))
+            return (equals == Py_NE);
+        ps1 = PyBytes_AS_STRING(s1);
+        ps2 = PyBytes_AS_STRING(s2);
+        if (ps1[0] != ps2[0]) {
+            return (equals == Py_NE);
+        } else if (length == 1) {
+            return (equals == Py_EQ);
+        } else {
+            int result;
+#if CYTHON_USE_UNICODE_INTERNALS && (PY_VERSION_HEX < 0x030B0000)
+            Py_hash_t hash1, hash2;
+            hash1 = ((PyBytesObject*)s1)->ob_shash;
+            hash2 = ((PyBytesObject*)s2)->ob_shash;
+            if (hash1 != hash2 && hash1 != -1 && hash2 != -1) {
+                return (equals == Py_NE);
+            }
+#endif
+            result = memcmp(ps1, ps2, (size_t)length);
+            return (equals == Py_EQ) ? (result == 0) : (result != 0);
+        }
+    } else if ((s1 == Py_None) & PyBytes_CheckExact(s2)) {
+        return (equals == Py_NE);
+    } else if ((s2 == Py_None) & PyBytes_CheckExact(s1)) {
+        return (equals == Py_NE);
+    } else {
+        int result;
+        PyObject* py_result = PyObject_RichCompare(s1, s2, equals);
+        if (!py_result)
+            return -1;
+        result = __Pyx_PyObject_IsTrue(py_result);
+        Py_DECREF(py_result);
+        return result;
+    }
+#endif
+}
+
+/* UnicodeEquals */
+static CYTHON_INLINE int __Pyx_PyUnicode_Equals(PyObject* s1, PyObject* s2, int equals) {
+#if CYTHON_COMPILING_IN_PYPY || CYTHON_COMPILING_IN_LIMITED_API
+    return PyObject_RichCompareBool(s1, s2, equals);
+#else
+#if PY_MAJOR_VERSION < 3
+    PyObject* owned_ref = NULL;
+#endif
+    int s1_is_unicode, s2_is_unicode;
+    if (s1 == s2) {
+        goto return_eq;
+    }
+    s1_is_unicode = PyUnicode_CheckExact(s1);
+    s2_is_unicode = PyUnicode_CheckExact(s2);
+#if PY_MAJOR_VERSION < 3
+    if ((s1_is_unicode & (!s2_is_unicode)) && PyString_CheckExact(s2)) {
+        owned_ref = PyUnicode_FromObject(s2);
+        if (unlikely(!owned_ref))
+            return -1;
+        s2 = owned_ref;
+        s2_is_unicode = 1;
+    } else if ((s2_is_unicode & (!s1_is_unicode)) && PyString_CheckExact(s1)) {
+        owned_ref = PyUnicode_FromObject(s1);
+        if (unlikely(!owned_ref))
+            return -1;
+        s1 = owned_ref;
+        s1_is_unicode = 1;
+    } else if (((!s2_is_unicode) & (!s1_is_unicode))) {
+        return __Pyx_PyBytes_Equals(s1, s2, equals);
+    }
+#endif
+    if (s1_is_unicode & s2_is_unicode) {
+        Py_ssize_t length;
+        int kind;
+        void *data1, *data2;
+        if (unlikely(__Pyx_PyUnicode_READY(s1) < 0) || unlikely(__Pyx_PyUnicode_READY(s2) < 0))
+            return -1;
+        length = __Pyx_PyUnicode_GET_LENGTH(s1);
+        if (length != __Pyx_PyUnicode_GET_LENGTH(s2)) {
+            goto return_ne;
+        }
+#if CYTHON_USE_UNICODE_INTERNALS
+        {
+            Py_hash_t hash1, hash2;
+        #if CYTHON_PEP393_ENABLED
+            hash1 = ((PyASCIIObject*)s1)->hash;
+            hash2 = ((PyASCIIObject*)s2)->hash;
+        #else
+            hash1 = ((PyUnicodeObject*)s1)->hash;
+            hash2 = ((PyUnicodeObject*)s2)->hash;
+        #endif
+            if (hash1 != hash2 && hash1 != -1 && hash2 != -1) {
+                goto return_ne;
+            }
+        }
+#endif
+        kind = __Pyx_PyUnicode_KIND(s1);
+        if (kind != __Pyx_PyUnicode_KIND(s2)) {
+            goto return_ne;
+        }
+        data1 = __Pyx_PyUnicode_DATA(s1);
+        data2 = __Pyx_PyUnicode_DATA(s2);
+        if (__Pyx_PyUnicode_READ(kind, data1, 0) != __Pyx_PyUnicode_READ(kind, data2, 0)) {
+            goto return_ne;
+        } else if (length == 1) {
+            goto return_eq;
+        } else {
+            int result = memcmp(data1, data2, (size_t)(length * kind));
+            #if PY_MAJOR_VERSION < 3
+            Py_XDECREF(owned_ref);
+            #endif
+            return (equals == Py_EQ) ? (result == 0) : (result != 0);
+        }
+    } else if ((s1 == Py_None) & s2_is_unicode) {
+        goto return_ne;
+    } else if ((s2 == Py_None) & s1_is_unicode) {
+        goto return_ne;
+    } else {
+        int result;
+        PyObject* py_result = PyObject_RichCompare(s1, s2, equals);
+        #if PY_MAJOR_VERSION < 3
+        Py_XDECREF(owned_ref);
+        #endif
+        if (!py_result)
+            return -1;
+        result = __Pyx_PyObject_IsTrue(py_result);
+        Py_DECREF(py_result);
+        return result;
+    }
+return_eq:
+    #if PY_MAJOR_VERSION < 3
+    Py_XDECREF(owned_ref);
+    #endif
+    return (equals == Py_EQ);
+return_ne:
+    #if PY_MAJOR_VERSION < 3
+    Py_XDECREF(owned_ref);
+    #endif
+    return (equals == Py_NE);
+#endif
+}
+
+/* fastcall */
+#if CYTHON_METH_FASTCALL
+static CYTHON_INLINE PyObject * __Pyx_GetKwValue_FASTCALL(PyObject *kwnames, PyObject *const *kwvalues, PyObject *s)
+{
+    Py_ssize_t i, n = PyTuple_GET_SIZE(kwnames);
+    for (i = 0; i < n; i++)
+    {
+        if (s == PyTuple_GET_ITEM(kwnames, i)) return kwvalues[i];
+    }
+    for (i = 0; i < n; i++)
+    {
+        int eq = __Pyx_PyUnicode_Equals(s, PyTuple_GET_ITEM(kwnames, i), Py_EQ);
+        if (unlikely(eq != 0)) {
+            if (unlikely(eq < 0)) return NULL;  // error
+            return kwvalues[i];
+        }
+    }
+    return NULL;  // not found (no exception set)
+}
+#endif
+
 /* RaiseDoubleKeywords */
 static void __Pyx_RaiseDoubleKeywordsError(
     const char* func_name,
     PyObject* kw_name)
 {
     PyErr_Format(PyExc_TypeError,
         #if PY_MAJOR_VERSION >= 3
@@ -7552,25 +11757,37 @@
         PyString_AsString(kw_name));
         #endif
 }
 
 /* ParseKeywords */
 static int __Pyx_ParseOptionalKeywords(
     PyObject *kwds,
+    PyObject *const *kwvalues,
     PyObject **argnames[],
     PyObject *kwds2,
     PyObject *values[],
     Py_ssize_t num_pos_args,
     const char* function_name)
 {
     PyObject *key = 0, *value = 0;
     Py_ssize_t pos = 0;
     PyObject*** name;
     PyObject*** first_kw_arg = argnames + num_pos_args;
-    while (PyDict_Next(kwds, &pos, &key, &value)) {
+    int kwds_is_tuple = CYTHON_METH_FASTCALL && likely(PyTuple_Check(kwds));
+    while (1) {
+        if (kwds_is_tuple) {
+            if (pos >= PyTuple_GET_SIZE(kwds)) break;
+            key = PyTuple_GET_ITEM(kwds, pos);
+            value = kwvalues[pos];
+            pos++;
+        }
+        else
+        {
+            if (!PyDict_Next(kwds, &pos, &key, &value)) break;
+        }
         name = first_kw_arg;
         while (*name && (**name != key)) name++;
         if (*name) {
             values[name-argnames] = value;
             continue;
         }
         name = first_kw_arg;
@@ -7596,19 +11813,20 @@
                     argname++;
                 }
             }
         } else
         #endif
         if (likely(PyUnicode_Check(key))) {
             while (*name) {
-                int cmp = (**name == key) ? 0 :
+                int cmp = (
                 #if !CYTHON_COMPILING_IN_PYPY && PY_MAJOR_VERSION >= 3
                     (__Pyx_PyUnicode_GET_LENGTH(**name) != __Pyx_PyUnicode_GET_LENGTH(key)) ? 1 :
                 #endif
-                    PyUnicode_Compare(**name, key);
+                    PyUnicode_Compare(**name, key)
+                );
                 if (cmp < 0 && unlikely(PyErr_Occurred())) goto bad;
                 if (cmp == 0) {
                     values[name-argnames] = value;
                     break;
                 }
                 name++;
             }
@@ -7639,19 +11857,20 @@
     __Pyx_RaiseDoubleKeywordsError(function_name, key);
     goto bad;
 invalid_keyword_type:
     PyErr_Format(PyExc_TypeError,
         "%.200s() keywords must be strings", function_name);
     goto bad;
 invalid_keyword:
-    PyErr_Format(PyExc_TypeError,
     #if PY_MAJOR_VERSION < 3
+    PyErr_Format(PyExc_TypeError,
         "%.200s() got an unexpected keyword argument '%.200s'",
         function_name, PyString_AsString(key));
     #else
+    PyErr_Format(PyExc_TypeError,
         "%s() got an unexpected keyword argument '%U'",
         function_name, key);
     #endif
 bad:
     return -1;
 }
 
@@ -7677,40 +11896,109 @@
     }
     PyErr_Format(PyExc_TypeError,
                  "%.200s() takes %.8s %" CYTHON_FORMAT_SSIZE_T "d positional argument%.1s (%" CYTHON_FORMAT_SSIZE_T "d given)",
                  func_name, more_or_less, num_expected,
                  (num_expected == 1) ? "" : "s", num_found);
 }
 
+/* KeywordStringCheck */
+static int __Pyx_CheckKeywordStrings(
+    PyObject *kw,
+    const char* function_name,
+    int kw_allowed)
+{
+    PyObject* key = 0;
+    Py_ssize_t pos = 0;
+#if CYTHON_COMPILING_IN_PYPY
+    if (!kw_allowed && PyDict_Next(kw, &pos, &key, 0))
+        goto invalid_keyword;
+    return 1;
+#else
+    if (CYTHON_METH_FASTCALL && likely(PyTuple_Check(kw))) {
+        if (unlikely(PyTuple_GET_SIZE(kw) == 0))
+            return 1;
+        if (!kw_allowed) {
+            key = PyTuple_GET_ITEM(kw, 0);
+            goto invalid_keyword;
+        }
+#if PY_VERSION_HEX < 0x03090000
+        for (pos = 0; pos < PyTuple_GET_SIZE(kw); pos++) {
+            key = PyTuple_GET_ITEM(kw, pos);
+            if (unlikely(!PyUnicode_Check(key)))
+                goto invalid_keyword_type;
+        }
+#endif
+        return 1;
+    }
+    while (PyDict_Next(kw, &pos, &key, 0)) {
+        #if PY_MAJOR_VERSION < 3
+        if (unlikely(!PyString_Check(key)))
+        #endif
+            if (unlikely(!PyUnicode_Check(key)))
+                goto invalid_keyword_type;
+    }
+    if (!kw_allowed && unlikely(key))
+        goto invalid_keyword;
+    return 1;
+invalid_keyword_type:
+    PyErr_Format(PyExc_TypeError,
+        "%.200s() keywords must be strings", function_name);
+    return 0;
+#endif
+invalid_keyword:
+    #if PY_MAJOR_VERSION < 3
+    PyErr_Format(PyExc_TypeError,
+        "%.200s() got an unexpected keyword argument '%.200s'",
+        function_name, PyString_AsString(key));
+    #else
+    PyErr_Format(PyExc_TypeError,
+        "%s() got an unexpected keyword argument '%U'",
+        function_name, key);
+    #endif
+    return 0;
+}
+
 /* ArgTypeTest */
 static int __Pyx__ArgTypeTest(PyObject *obj, PyTypeObject *type, const char *name, int exact)
 {
+    __Pyx_TypeName type_name;
+    __Pyx_TypeName obj_type_name;
     if (unlikely(!type)) {
         PyErr_SetString(PyExc_SystemError, "Missing type object");
         return 0;
     }
     else if (exact) {
         #if PY_MAJOR_VERSION == 2
         if ((type == &PyBaseString_Type) && likely(__Pyx_PyBaseString_CheckExact(obj))) return 1;
         #endif
     }
     else {
         if (likely(__Pyx_TypeCheck(obj, type))) return 1;
     }
+    type_name = __Pyx_PyType_GetName(type);
+    obj_type_name = __Pyx_PyType_GetName(Py_TYPE(obj));
     PyErr_Format(PyExc_TypeError,
-        "Argument '%.200s' has incorrect type (expected %.200s, got %.200s)",
-        name, type->tp_name, Py_TYPE(obj)->tp_name);
+        "Argument '%.200s' has incorrect type (expected " __Pyx_FMT_TYPENAME
+        ", got " __Pyx_FMT_TYPENAME ")", name, type_name, obj_type_name);
+    __Pyx_DECREF_TypeName(type_name);
+    __Pyx_DECREF_TypeName(obj_type_name);
     return 0;
 }
 
+/* PyObjectCallOneArg */
+static CYTHON_INLINE PyObject* __Pyx_PyObject_CallOneArg(PyObject *func, PyObject *arg) {
+    PyObject *args[2] = {NULL, arg};
+    return __Pyx_PyObject_FastCall(func, args+1, 1 | __Pyx_PY_VECTORCALL_ARGUMENTS_OFFSET);
+}
+
 /* RaiseException */
 #if PY_MAJOR_VERSION < 3
-static void __Pyx_Raise(PyObject *type, PyObject *value, PyObject *tb,
-                        CYTHON_UNUSED PyObject *cause) {
+static void __Pyx_Raise(PyObject *type, PyObject *value, PyObject *tb, PyObject *cause) {
     __Pyx_PyThreadState_declare
+    CYTHON_UNUSED_VAR(cause);
     Py_XINCREF(type);
     if (!value || value == Py_None)
         value = NULL;
     else
         Py_INCREF(value);
     if (!tb || tb == Py_None)
         tb = NULL;
@@ -7835,15 +12123,17 @@
                             "BaseException");
             goto bad;
         }
         PyException_SetCause(value, fixed_cause);
     }
     PyErr_SetObject(type, value);
     if (tb) {
-#if CYTHON_FAST_THREAD_STATE
+      #if PY_VERSION_HEX >= 0x030C00A6
+        PyException_SetTraceback(value, tb);
+      #elif CYTHON_FAST_THREAD_STATE
         PyThreadState *tstate = __Pyx_PyThreadState_Current;
         PyObject* tmp_tb = tstate->curexc_traceback;
         if (tb != tmp_tb) {
             Py_INCREF(tb);
             tstate->curexc_traceback = tb;
             Py_XDECREF(tmp_tb);
         }
@@ -7857,25 +12147,347 @@
     }
 bad:
     Py_XDECREF(owned_instance);
     return;
 }
 #endif
 
+/* FixUpExtensionType */
+#if CYTHON_USE_TYPE_SPECS
+static int __Pyx_fix_up_extension_type_from_spec(PyType_Spec *spec, PyTypeObject *type) {
+#if PY_VERSION_HEX > 0x030900B1 || CYTHON_COMPILING_IN_LIMITED_API
+    CYTHON_UNUSED_VAR(spec);
+    CYTHON_UNUSED_VAR(type);
+#else
+    const PyType_Slot *slot = spec->slots;
+    while (slot && slot->slot && slot->slot != Py_tp_members)
+        slot++;
+    if (slot && slot->slot == Py_tp_members) {
+        int changed = 0;
+#if !(PY_VERSION_HEX <= 0x030900b1 && CYTHON_COMPILING_IN_CPYTHON)
+        const
+#endif
+            PyMemberDef *memb = (PyMemberDef*) slot->pfunc;
+        while (memb && memb->name) {
+            if (memb->name[0] == '_' && memb->name[1] == '_') {
+#if PY_VERSION_HEX < 0x030900b1
+                if (strcmp(memb->name, "__weaklistoffset__") == 0) {
+                    assert(memb->type == T_PYSSIZET);
+                    assert(memb->flags == READONLY);
+                    type->tp_weaklistoffset = memb->offset;
+                    changed = 1;
+                }
+                else if (strcmp(memb->name, "__dictoffset__") == 0) {
+                    assert(memb->type == T_PYSSIZET);
+                    assert(memb->flags == READONLY);
+                    type->tp_dictoffset = memb->offset;
+                    changed = 1;
+                }
+#if CYTHON_METH_FASTCALL
+                else if (strcmp(memb->name, "__vectorcalloffset__") == 0) {
+                    assert(memb->type == T_PYSSIZET);
+                    assert(memb->flags == READONLY);
+#if PY_VERSION_HEX >= 0x030800b4
+                    type->tp_vectorcall_offset = memb->offset;
+#else
+                    type->tp_print = (printfunc) memb->offset;
+#endif
+                    changed = 1;
+                }
+#endif
+#else
+                if ((0));
+#endif
+#if PY_VERSION_HEX <= 0x030900b1 && CYTHON_COMPILING_IN_CPYTHON
+                else if (strcmp(memb->name, "__module__") == 0) {
+                    PyObject *descr;
+                    assert(memb->type == T_OBJECT);
+                    assert(memb->flags == 0 || memb->flags == READONLY);
+                    descr = PyDescr_NewMember(type, memb);
+                    if (unlikely(!descr))
+                        return -1;
+                    if (unlikely(PyDict_SetItem(type->tp_dict, PyDescr_NAME(descr), descr) < 0)) {
+                        Py_DECREF(descr);
+                        return -1;
+                    }
+                    Py_DECREF(descr);
+                    changed = 1;
+                }
+#endif
+            }
+            memb++;
+        }
+        if (changed)
+            PyType_Modified(type);
+    }
+#endif
+    return 0;
+}
+#endif
+
+/* PyObjectCallNoArg */
+static CYTHON_INLINE PyObject* __Pyx_PyObject_CallNoArg(PyObject *func) {
+    PyObject *arg = NULL;
+    return __Pyx_PyObject_FastCall(func, (&arg)+1, 0 | __Pyx_PY_VECTORCALL_ARGUMENTS_OFFSET);
+}
+
+/* PyObjectGetMethod */
+static int __Pyx_PyObject_GetMethod(PyObject *obj, PyObject *name, PyObject **method) {
+    PyObject *attr;
+#if CYTHON_UNPACK_METHODS && CYTHON_COMPILING_IN_CPYTHON && CYTHON_USE_PYTYPE_LOOKUP
+    __Pyx_TypeName type_name;
+    PyTypeObject *tp = Py_TYPE(obj);
+    PyObject *descr;
+    descrgetfunc f = NULL;
+    PyObject **dictptr, *dict;
+    int meth_found = 0;
+    assert (*method == NULL);
+    if (unlikely(tp->tp_getattro != PyObject_GenericGetAttr)) {
+        attr = __Pyx_PyObject_GetAttrStr(obj, name);
+        goto try_unpack;
+    }
+    if (unlikely(tp->tp_dict == NULL) && unlikely(PyType_Ready(tp) < 0)) {
+        return 0;
+    }
+    descr = _PyType_Lookup(tp, name);
+    if (likely(descr != NULL)) {
+        Py_INCREF(descr);
+#if defined(Py_TPFLAGS_METHOD_DESCRIPTOR) && Py_TPFLAGS_METHOD_DESCRIPTOR
+        if (__Pyx_PyType_HasFeature(Py_TYPE(descr), Py_TPFLAGS_METHOD_DESCRIPTOR))
+#elif PY_MAJOR_VERSION >= 3
+        #ifdef __Pyx_CyFunction_USED
+        if (likely(PyFunction_Check(descr) || __Pyx_IS_TYPE(descr, &PyMethodDescr_Type) || __Pyx_CyFunction_Check(descr)))
+        #else
+        if (likely(PyFunction_Check(descr) || __Pyx_IS_TYPE(descr, &PyMethodDescr_Type)))
+        #endif
+#else
+        #ifdef __Pyx_CyFunction_USED
+        if (likely(PyFunction_Check(descr) || __Pyx_CyFunction_Check(descr)))
+        #else
+        if (likely(PyFunction_Check(descr)))
+        #endif
+#endif
+        {
+            meth_found = 1;
+        } else {
+            f = Py_TYPE(descr)->tp_descr_get;
+            if (f != NULL && PyDescr_IsData(descr)) {
+                attr = f(descr, obj, (PyObject *)Py_TYPE(obj));
+                Py_DECREF(descr);
+                goto try_unpack;
+            }
+        }
+    }
+    dictptr = _PyObject_GetDictPtr(obj);
+    if (dictptr != NULL && (dict = *dictptr) != NULL) {
+        Py_INCREF(dict);
+        attr = __Pyx_PyDict_GetItemStr(dict, name);
+        if (attr != NULL) {
+            Py_INCREF(attr);
+            Py_DECREF(dict);
+            Py_XDECREF(descr);
+            goto try_unpack;
+        }
+        Py_DECREF(dict);
+    }
+    if (meth_found) {
+        *method = descr;
+        return 1;
+    }
+    if (f != NULL) {
+        attr = f(descr, obj, (PyObject *)Py_TYPE(obj));
+        Py_DECREF(descr);
+        goto try_unpack;
+    }
+    if (likely(descr != NULL)) {
+        *method = descr;
+        return 0;
+    }
+    type_name = __Pyx_PyType_GetName(tp);
+    PyErr_Format(PyExc_AttributeError,
+#if PY_MAJOR_VERSION >= 3
+                 "'" __Pyx_FMT_TYPENAME "' object has no attribute '%U'",
+                 type_name, name);
+#else
+                 "'" __Pyx_FMT_TYPENAME "' object has no attribute '%.400s'",
+                 type_name, PyString_AS_STRING(name));
+#endif
+    __Pyx_DECREF_TypeName(type_name);
+    return 0;
+#else
+    attr = __Pyx_PyObject_GetAttrStr(obj, name);
+    goto try_unpack;
+#endif
+try_unpack:
+#if CYTHON_UNPACK_METHODS
+    if (likely(attr) && PyMethod_Check(attr) && likely(PyMethod_GET_SELF(attr) == obj)) {
+        PyObject *function = PyMethod_GET_FUNCTION(attr);
+        Py_INCREF(function);
+        Py_DECREF(attr);
+        *method = function;
+        return 1;
+    }
+#endif
+    *method = attr;
+    return 0;
+}
+
+/* PyObjectCallMethod0 */
+static PyObject* __Pyx_PyObject_CallMethod0(PyObject* obj, PyObject* method_name) {
+    PyObject *method = NULL, *result = NULL;
+    int is_method = __Pyx_PyObject_GetMethod(obj, method_name, &method);
+    if (likely(is_method)) {
+        result = __Pyx_PyObject_CallOneArg(method, obj);
+        Py_DECREF(method);
+        return result;
+    }
+    if (unlikely(!method)) goto bad;
+    result = __Pyx_PyObject_CallNoArg(method);
+    Py_DECREF(method);
+bad:
+    return result;
+}
+
+/* ValidateBasesTuple */
+#if CYTHON_COMPILING_IN_CPYTHON || CYTHON_COMPILING_IN_LIMITED_API || CYTHON_USE_TYPE_SPECS
+static int __Pyx_validate_bases_tuple(const char *type_name, Py_ssize_t dictoffset, PyObject *bases) {
+    Py_ssize_t i, n = PyTuple_GET_SIZE(bases);
+    for (i = 1; i < n; i++)
+    {
+        PyObject *b0 = PyTuple_GET_ITEM(bases, i);
+        PyTypeObject *b;
+#if PY_MAJOR_VERSION < 3
+        if (PyClass_Check(b0))
+        {
+            PyErr_Format(PyExc_TypeError, "base class '%.200s' is an old-style class",
+                         PyString_AS_STRING(((PyClassObject*)b0)->cl_name));
+            return -1;
+        }
+#endif
+        b = (PyTypeObject*) b0;
+        if (!__Pyx_PyType_HasFeature(b, Py_TPFLAGS_HEAPTYPE))
+        {
+            __Pyx_TypeName b_name = __Pyx_PyType_GetName(b);
+            PyErr_Format(PyExc_TypeError,
+                "base class '" __Pyx_FMT_TYPENAME "' is not a heap type", b_name);
+            __Pyx_DECREF_TypeName(b_name);
+            return -1;
+        }
+        if (dictoffset == 0 && b->tp_dictoffset)
+        {
+            __Pyx_TypeName b_name = __Pyx_PyType_GetName(b);
+            PyErr_Format(PyExc_TypeError,
+                "extension type '%.200s' has no __dict__ slot, "
+                "but base type '" __Pyx_FMT_TYPENAME "' has: "
+                "either add 'cdef dict __dict__' to the extension type "
+                "or add '__slots__ = [...]' to the base type",
+                type_name, b_name);
+            __Pyx_DECREF_TypeName(b_name);
+            return -1;
+        }
+    }
+    return 0;
+}
+#endif
+
+/* PyType_Ready */
+static int __Pyx_PyType_Ready(PyTypeObject *t) {
+#if CYTHON_USE_TYPE_SPECS || !(CYTHON_COMPILING_IN_CPYTHON || CYTHON_COMPILING_IN_LIMITED_API) || defined(PYSTON_MAJOR_VERSION)
+    (void)__Pyx_PyObject_CallMethod0;
+#if CYTHON_USE_TYPE_SPECS
+    (void)__Pyx_validate_bases_tuple;
+#endif
+    return PyType_Ready(t);
+#else
+    int r;
+    PyObject *bases = __Pyx_PyType_GetSlot(t, tp_bases, PyObject*);
+    if (bases && unlikely(__Pyx_validate_bases_tuple(t->tp_name, t->tp_dictoffset, bases) == -1))
+        return -1;
+#if PY_VERSION_HEX >= 0x03050000 && !defined(PYSTON_MAJOR_VERSION)
+    {
+        int gc_was_enabled;
+    #if PY_VERSION_HEX >= 0x030A00b1
+        gc_was_enabled = PyGC_Disable();
+        (void)__Pyx_PyObject_CallMethod0;
+    #else
+        PyObject *ret, *py_status;
+        PyObject *gc = NULL;
+        #if PY_VERSION_HEX >= 0x030700a1 && (!CYTHON_COMPILING_IN_PYPY || PYPY_VERSION_NUM+0 >= 0x07030400)
+        gc = PyImport_GetModule(__pyx_kp_u_gc);
+        #endif
+        if (unlikely(!gc)) gc = PyImport_Import(__pyx_kp_u_gc);
+        if (unlikely(!gc)) return -1;
+        py_status = __Pyx_PyObject_CallMethod0(gc, __pyx_kp_u_isenabled);
+        if (unlikely(!py_status)) {
+            Py_DECREF(gc);
+            return -1;
+        }
+        gc_was_enabled = __Pyx_PyObject_IsTrue(py_status);
+        Py_DECREF(py_status);
+        if (gc_was_enabled > 0) {
+            ret = __Pyx_PyObject_CallMethod0(gc, __pyx_kp_u_disable);
+            if (unlikely(!ret)) {
+                Py_DECREF(gc);
+                return -1;
+            }
+            Py_DECREF(ret);
+        } else if (unlikely(gc_was_enabled == -1)) {
+            Py_DECREF(gc);
+            return -1;
+        }
+    #endif
+        t->tp_flags |= Py_TPFLAGS_HEAPTYPE;
+#if PY_VERSION_HEX >= 0x030A0000
+        t->tp_flags |= Py_TPFLAGS_IMMUTABLETYPE;
+#endif
+#else
+        (void)__Pyx_PyObject_CallMethod0;
+#endif
+    r = PyType_Ready(t);
+#if PY_VERSION_HEX >= 0x03050000 && !defined(PYSTON_MAJOR_VERSION)
+        t->tp_flags &= ~Py_TPFLAGS_HEAPTYPE;
+    #if PY_VERSION_HEX >= 0x030A00b1
+        if (gc_was_enabled)
+            PyGC_Enable();
+    #else
+        if (gc_was_enabled) {
+            PyObject *tp, *v, *tb;
+            PyErr_Fetch(&tp, &v, &tb);
+            ret = __Pyx_PyObject_CallMethod0(gc, __pyx_kp_u_enable);
+            if (likely(ret || r == -1)) {
+                Py_XDECREF(ret);
+                PyErr_Restore(tp, v, tb);
+            } else {
+                Py_XDECREF(tp);
+                Py_XDECREF(v);
+                Py_XDECREF(tb);
+                r = -1;
+            }
+        }
+        Py_DECREF(gc);
+    #endif
+    }
+#endif
+    return r;
+#endif
+}
+
 /* PyObject_GenericGetAttrNoDict */
 #if CYTHON_USE_TYPE_SLOTS && CYTHON_USE_PYTYPE_LOOKUP && PY_VERSION_HEX < 0x03070000
 static PyObject *__Pyx_RaiseGenericGetAttributeError(PyTypeObject *tp, PyObject *attr_name) {
+    __Pyx_TypeName type_name = __Pyx_PyType_GetName(tp);
     PyErr_Format(PyExc_AttributeError,
 #if PY_MAJOR_VERSION >= 3
-                 "'%.50s' object has no attribute '%U'",
-                 tp->tp_name, attr_name);
+                 "'" __Pyx_FMT_TYPENAME "' object has no attribute '%U'",
+                 type_name, attr_name);
 #else
-                 "'%.50s' object has no attribute '%.400s'",
-                 tp->tp_name, PyString_AS_STRING(attr_name));
+                 "'" __Pyx_FMT_TYPENAME "' object has no attribute '%.400s'",
+                 type_name, PyString_AS_STRING(attr_name));
 #endif
+    __Pyx_DECREF_TypeName(type_name);
     return NULL;
 }
 static CYTHON_INLINE PyObject* __Pyx_PyObject_GenericGetAttrNoDict(PyObject* obj, PyObject* attr_name) {
     PyObject *descr;
     PyTypeObject *tp = Py_TYPE(obj);
     if (unlikely(!PyString_Check(attr_name))) {
         return PyObject_GenericGetAttr(obj, attr_name);
@@ -7898,83 +12510,110 @@
         }
     }
     return descr;
 }
 #endif
 
 /* SetVTable */
-static int __Pyx_SetVtable(PyObject *dict, void *vtable) {
-#if PY_VERSION_HEX >= 0x02070000
+static int __Pyx_SetVtable(PyTypeObject *type, void *vtable) {
     PyObject *ob = PyCapsule_New(vtable, 0, 0);
+    if (unlikely(!ob))
+        goto bad;
+#if CYTHON_COMPILING_IN_LIMITED_API
+    if (unlikely(PyObject_SetAttr((PyObject *) type, __pyx_n_s_pyx_vtable, ob) < 0))
 #else
-    PyObject *ob = PyCObject_FromVoidPtr(vtable, 0);
+    if (unlikely(PyDict_SetItem(type->tp_dict, __pyx_n_s_pyx_vtable, ob) < 0))
 #endif
-    if (!ob)
-        goto bad;
-    if (PyDict_SetItem(dict, __pyx_n_s_pyx_vtable, ob) < 0)
         goto bad;
     Py_DECREF(ob);
     return 0;
 bad:
     Py_XDECREF(ob);
     return -1;
 }
 
-/* PyErrExceptionMatches */
-#if CYTHON_FAST_THREAD_STATE
-static int __Pyx_PyErr_ExceptionMatchesTuple(PyObject *exc_type, PyObject *tuple) {
-    Py_ssize_t i, n;
-    n = PyTuple_GET_SIZE(tuple);
-#if PY_MAJOR_VERSION >= 3
-    for (i=0; i<n; i++) {
-        if (exc_type == PyTuple_GET_ITEM(tuple, i)) return 1;
-    }
+/* GetVTable */
+static void* __Pyx_GetVtable(PyTypeObject *type) {
+    void* ptr;
+#if CYTHON_COMPILING_IN_LIMITED_API
+    PyObject *ob = PyObject_GetAttr((PyObject *)type, __pyx_n_s_pyx_vtable);
+#else
+    PyObject *ob = PyObject_GetItem(type->tp_dict, __pyx_n_s_pyx_vtable);
 #endif
-    for (i=0; i<n; i++) {
-        if (__Pyx_PyErr_GivenExceptionMatches(exc_type, PyTuple_GET_ITEM(tuple, i))) return 1;
-    }
-    return 0;
-}
-static CYTHON_INLINE int __Pyx_PyErr_ExceptionMatchesInState(PyThreadState* tstate, PyObject* err) {
-    PyObject *exc_type = tstate->curexc_type;
-    if (exc_type == err) return 1;
-    if (unlikely(!exc_type)) return 0;
-    if (unlikely(PyTuple_Check(err)))
-        return __Pyx_PyErr_ExceptionMatchesTuple(exc_type, err);
-    return __Pyx_PyErr_GivenExceptionMatches(exc_type, err);
+    if (!ob)
+        goto bad;
+    ptr = PyCapsule_GetPointer(ob, 0);
+    if (!ptr && !PyErr_Occurred())
+        PyErr_SetString(PyExc_RuntimeError, "invalid vtable found for imported type");
+    Py_DECREF(ob);
+    return ptr;
+bad:
+    Py_XDECREF(ob);
+    return NULL;
 }
-#endif
 
-/* PyObjectGetAttrStrNoError */
-static void __Pyx_PyObject_GetAttrStr_ClearAttributeError(void) {
-    __Pyx_PyThreadState_declare
-    __Pyx_PyThreadState_assign
-    if (likely(__Pyx_PyErr_ExceptionMatches(PyExc_AttributeError)))
-        __Pyx_PyErr_Clear();
-}
-static CYTHON_INLINE PyObject* __Pyx_PyObject_GetAttrStrNoError(PyObject* obj, PyObject* attr_name) {
-    PyObject *result;
-#if CYTHON_COMPILING_IN_CPYTHON && CYTHON_USE_TYPE_SLOTS && PY_VERSION_HEX >= 0x030700B1
-    PyTypeObject* tp = Py_TYPE(obj);
-    if (likely(tp->tp_getattro == PyObject_GenericGetAttr)) {
-        return _PyObject_GenericGetAttrWithDict(obj, attr_name, NULL, 1);
-    }
-#endif
-    result = __Pyx_PyObject_GetAttrStr(obj, attr_name);
-    if (unlikely(!result)) {
-        __Pyx_PyObject_GetAttrStr_ClearAttributeError();
+/* MergeVTables */
+#if !CYTHON_COMPILING_IN_LIMITED_API
+static int __Pyx_MergeVtables(PyTypeObject *type) {
+    int i;
+    void** base_vtables;
+    __Pyx_TypeName tp_base_name;
+    __Pyx_TypeName base_name;
+    void* unknown = (void*)-1;
+    PyObject* bases = type->tp_bases;
+    int base_depth = 0;
+    {
+        PyTypeObject* base = type->tp_base;
+        while (base) {
+            base_depth += 1;
+            base = base->tp_base;
+        }
+    }
+    base_vtables = (void**) malloc(sizeof(void*) * (size_t)(base_depth + 1));
+    base_vtables[0] = unknown;
+    for (i = 1; i < PyTuple_GET_SIZE(bases); i++) {
+        void* base_vtable = __Pyx_GetVtable(((PyTypeObject*)PyTuple_GET_ITEM(bases, i)));
+        if (base_vtable != NULL) {
+            int j;
+            PyTypeObject* base = type->tp_base;
+            for (j = 0; j < base_depth; j++) {
+                if (base_vtables[j] == unknown) {
+                    base_vtables[j] = __Pyx_GetVtable(base);
+                    base_vtables[j + 1] = unknown;
+                }
+                if (base_vtables[j] == base_vtable) {
+                    break;
+                } else if (base_vtables[j] == NULL) {
+                    goto bad;
+                }
+                base = base->tp_base;
+            }
+        }
     }
-    return result;
+    PyErr_Clear();
+    free(base_vtables);
+    return 0;
+bad:
+    tp_base_name = __Pyx_PyType_GetName(type->tp_base);
+    base_name = __Pyx_PyType_GetName((PyTypeObject*)PyTuple_GET_ITEM(bases, i));
+    PyErr_Format(PyExc_TypeError,
+        "multiple bases have vtable conflict: '" __Pyx_FMT_TYPENAME "' and '" __Pyx_FMT_TYPENAME "'", tp_base_name, base_name);
+    __Pyx_DECREF_TypeName(tp_base_name);
+    __Pyx_DECREF_TypeName(base_name);
+    free(base_vtables);
+    return -1;
 }
+#endif
 
 /* SetupReduce */
+#if !CYTHON_COMPILING_IN_LIMITED_API
 static int __Pyx_setup_reduce_is_named(PyObject* meth, PyObject* name) {
   int ret;
   PyObject *name_attr;
-  name_attr = __Pyx_PyObject_GetAttrStr(meth, __pyx_n_s_name);
+  name_attr = __Pyx_PyObject_GetAttrStrNoError(meth, __pyx_n_s_name);
   if (likely(name_attr)) {
       ret = PyObject_RichCompareBool(name_attr, name, Py_EQ);
   } else {
       ret = -1;
   }
   if (unlikely(ret < 0)) {
       PyErr_Clear();
@@ -8032,15 +12671,15 @@
             reduce_cython = __Pyx_PyObject_GetAttrStrNoError(type_obj, __pyx_n_s_reduce_cython);
             if (likely(reduce_cython)) {
                 ret = PyDict_SetItem(((PyTypeObject*)type_obj)->tp_dict, __pyx_n_s_reduce, reduce_cython); if (unlikely(ret < 0)) goto __PYX_BAD;
                 ret = PyDict_DelItem(((PyTypeObject*)type_obj)->tp_dict, __pyx_n_s_reduce_cython); if (unlikely(ret < 0)) goto __PYX_BAD;
             } else if (reduce == object_reduce || PyErr_Occurred()) {
                 goto __PYX_BAD;
             }
-            setstate = __Pyx_PyObject_GetAttrStr(type_obj, __pyx_n_s_setstate);
+            setstate = __Pyx_PyObject_GetAttrStrNoError(type_obj, __pyx_n_s_setstate);
             if (!setstate) PyErr_Clear();
             if (!setstate || __Pyx_setup_reduce_is_named(setstate, __pyx_n_s_setstate_cython)) {
                 setstate_cython = __Pyx_PyObject_GetAttrStrNoError(type_obj, __pyx_n_s_setstate_cython);
                 if (likely(setstate_cython)) {
                     ret = PyDict_SetItem(((PyTypeObject*)type_obj)->tp_dict, __pyx_n_s_setstate, setstate_cython); if (unlikely(ret < 0)) goto __PYX_BAD;
                     ret = PyDict_DelItem(((PyTypeObject*)type_obj)->tp_dict, __pyx_n_s_setstate_cython); if (unlikely(ret < 0)) goto __PYX_BAD;
                 } else if (!setstate || PyErr_Occurred()) {
@@ -8048,16 +12687,21 @@
                 }
             }
             PyType_Modified((PyTypeObject*)type_obj);
         }
     }
     goto __PYX_GOOD;
 __PYX_BAD:
-    if (!PyErr_Occurred())
-        PyErr_Format(PyExc_RuntimeError, "Unable to initialize pickling for %s", ((PyTypeObject*)type_obj)->tp_name);
+    if (!PyErr_Occurred()) {
+        __Pyx_TypeName type_obj_name =
+            __Pyx_PyType_GetName((PyTypeObject*)type_obj);
+        PyErr_Format(PyExc_RuntimeError,
+            "Unable to initialize pickling for " __Pyx_FMT_TYPENAME, type_obj_name);
+        __Pyx_DECREF_TypeName(type_obj_name);
+    }
     ret = -1;
 __PYX_GOOD:
 #if !CYTHON_USE_PYTYPE_LOOKUP
     Py_XDECREF(object_reduce);
     Py_XDECREF(object_reduce_ex);
     Py_XDECREF(object_getstate);
     Py_XDECREF(getstate);
@@ -8065,14 +12709,1064 @@
     Py_XDECREF(reduce);
     Py_XDECREF(reduce_ex);
     Py_XDECREF(reduce_cython);
     Py_XDECREF(setstate);
     Py_XDECREF(setstate_cython);
     return ret;
 }
+#endif
+
+/* FetchSharedCythonModule */
+static PyObject *__Pyx_FetchSharedCythonABIModule(void) {
+    PyObject *abi_module = PyImport_AddModule((char*) __PYX_ABI_MODULE_NAME);
+    if (unlikely(!abi_module)) return NULL;
+    Py_INCREF(abi_module);
+    return abi_module;
+}
+
+/* FetchCommonType */
+static int __Pyx_VerifyCachedType(PyObject *cached_type,
+                               const char *name,
+                               Py_ssize_t basicsize,
+                               Py_ssize_t expected_basicsize) {
+    if (!PyType_Check(cached_type)) {
+        PyErr_Format(PyExc_TypeError,
+            "Shared Cython type %.200s is not a type object", name);
+        return -1;
+    }
+    if (basicsize != expected_basicsize) {
+        PyErr_Format(PyExc_TypeError,
+            "Shared Cython type %.200s has the wrong size, try recompiling",
+            name);
+        return -1;
+    }
+    return 0;
+}
+#if !CYTHON_USE_TYPE_SPECS
+static PyTypeObject* __Pyx_FetchCommonType(PyTypeObject* type) {
+    PyObject* abi_module;
+    const char* object_name;
+    PyTypeObject *cached_type = NULL;
+    abi_module = __Pyx_FetchSharedCythonABIModule();
+    if (!abi_module) return NULL;
+    object_name = strrchr(type->tp_name, '.');
+    object_name = object_name ? object_name+1 : type->tp_name;
+    cached_type = (PyTypeObject*) PyObject_GetAttrString(abi_module, object_name);
+    if (cached_type) {
+        if (__Pyx_VerifyCachedType(
+              (PyObject *)cached_type,
+              object_name,
+              cached_type->tp_basicsize,
+              type->tp_basicsize) < 0) {
+            goto bad;
+        }
+        goto done;
+    }
+    if (!PyErr_ExceptionMatches(PyExc_AttributeError)) goto bad;
+    PyErr_Clear();
+    if (PyType_Ready(type) < 0) goto bad;
+    if (PyObject_SetAttrString(abi_module, object_name, (PyObject *)type) < 0)
+        goto bad;
+    Py_INCREF(type);
+    cached_type = type;
+done:
+    Py_DECREF(abi_module);
+    return cached_type;
+bad:
+    Py_XDECREF(cached_type);
+    cached_type = NULL;
+    goto done;
+}
+#else
+static PyTypeObject *__Pyx_FetchCommonTypeFromSpec(PyObject *module, PyType_Spec *spec, PyObject *bases) {
+    PyObject *abi_module, *cached_type = NULL;
+    const char* object_name = strrchr(spec->name, '.');
+    object_name = object_name ? object_name+1 : spec->name;
+    abi_module = __Pyx_FetchSharedCythonABIModule();
+    if (!abi_module) return NULL;
+    cached_type = PyObject_GetAttrString(abi_module, object_name);
+    if (cached_type) {
+        Py_ssize_t basicsize;
+#if CYTHON_COMPILING_IN_LIMITED_API
+        PyObject *py_basicsize;
+        py_basicsize = PyObject_GetAttrString(cached_type, "__basicsize__");
+        if (unlikely(!py_basicsize)) goto bad;
+        basicsize = PyLong_AsSsize_t(py_basicsize);
+        Py_DECREF(py_basicsize);
+        py_basicsize = 0;
+        if (unlikely(basicsize == (Py_ssize_t)-1) && PyErr_Occurred()) goto bad;
+#else
+        basicsize = likely(PyType_Check(cached_type)) ? ((PyTypeObject*) cached_type)->tp_basicsize : -1;
+#endif
+        if (__Pyx_VerifyCachedType(
+              cached_type,
+              object_name,
+              basicsize,
+              spec->basicsize) < 0) {
+            goto bad;
+        }
+        goto done;
+    }
+    if (!PyErr_ExceptionMatches(PyExc_AttributeError)) goto bad;
+    PyErr_Clear();
+    CYTHON_UNUSED_VAR(module);
+    cached_type = __Pyx_PyType_FromModuleAndSpec(abi_module, spec, bases);
+    if (unlikely(!cached_type)) goto bad;
+    if (unlikely(__Pyx_fix_up_extension_type_from_spec(spec, (PyTypeObject *) cached_type) < 0)) goto bad;
+    if (PyObject_SetAttrString(abi_module, object_name, cached_type) < 0) goto bad;
+done:
+    Py_DECREF(abi_module);
+    assert(cached_type == NULL || PyType_Check(cached_type));
+    return (PyTypeObject *) cached_type;
+bad:
+    Py_XDECREF(cached_type);
+    cached_type = NULL;
+    goto done;
+}
+#endif
+
+/* PyVectorcallFastCallDict */
+#if CYTHON_METH_FASTCALL
+static PyObject *__Pyx_PyVectorcall_FastCallDict_kw(PyObject *func, __pyx_vectorcallfunc vc, PyObject *const *args, size_t nargs, PyObject *kw)
+{
+    PyObject *res = NULL;
+    PyObject *kwnames;
+    PyObject **newargs;
+    PyObject **kwvalues;
+    Py_ssize_t i, pos;
+    size_t j;
+    PyObject *key, *value;
+    unsigned long keys_are_strings;
+    Py_ssize_t nkw = PyDict_GET_SIZE(kw);
+    newargs = (PyObject **)PyMem_Malloc((nargs + (size_t)nkw) * sizeof(args[0]));
+    if (unlikely(newargs == NULL)) {
+        PyErr_NoMemory();
+        return NULL;
+    }
+    for (j = 0; j < nargs; j++) newargs[j] = args[j];
+    kwnames = PyTuple_New(nkw);
+    if (unlikely(kwnames == NULL)) {
+        PyMem_Free(newargs);
+        return NULL;
+    }
+    kwvalues = newargs + nargs;
+    pos = i = 0;
+    keys_are_strings = Py_TPFLAGS_UNICODE_SUBCLASS;
+    while (PyDict_Next(kw, &pos, &key, &value)) {
+        keys_are_strings &= Py_TYPE(key)->tp_flags;
+        Py_INCREF(key);
+        Py_INCREF(value);
+        PyTuple_SET_ITEM(kwnames, i, key);
+        kwvalues[i] = value;
+        i++;
+    }
+    if (unlikely(!keys_are_strings)) {
+        PyErr_SetString(PyExc_TypeError, "keywords must be strings");
+        goto cleanup;
+    }
+    res = vc(func, newargs, nargs, kwnames);
+cleanup:
+    Py_DECREF(kwnames);
+    for (i = 0; i < nkw; i++)
+        Py_DECREF(kwvalues[i]);
+    PyMem_Free(newargs);
+    return res;
+}
+static CYTHON_INLINE PyObject *__Pyx_PyVectorcall_FastCallDict(PyObject *func, __pyx_vectorcallfunc vc, PyObject *const *args, size_t nargs, PyObject *kw)
+{
+    if (likely(kw == NULL) || PyDict_GET_SIZE(kw) == 0) {
+        return vc(func, args, nargs, NULL);
+    }
+    return __Pyx_PyVectorcall_FastCallDict_kw(func, vc, args, nargs, kw);
+}
+#endif
+
+/* CythonFunctionShared */
+static CYTHON_INLINE void __Pyx__CyFunction_SetClassObj(__pyx_CyFunctionObject* f, PyObject* classobj) {
+#if PY_VERSION_HEX < 0x030900B1
+    __Pyx_Py_XDECREF_SET(
+        __Pyx_CyFunction_GetClassObj(f),
+            ((classobj) ? __Pyx_NewRef(classobj) : NULL));
+#else
+    __Pyx_Py_XDECREF_SET(
+        ((PyCMethodObject *) (f))->mm_class,
+        (PyTypeObject*)((classobj) ? __Pyx_NewRef(classobj) : NULL));
+#endif
+}
+static PyObject *
+__Pyx_CyFunction_get_doc(__pyx_CyFunctionObject *op, void *closure)
+{
+    CYTHON_UNUSED_VAR(closure);
+    if (unlikely(op->func_doc == NULL)) {
+        if (((PyCFunctionObject*)op)->m_ml->ml_doc) {
+#if PY_MAJOR_VERSION >= 3
+            op->func_doc = PyUnicode_FromString(((PyCFunctionObject*)op)->m_ml->ml_doc);
+#else
+            op->func_doc = PyString_FromString(((PyCFunctionObject*)op)->m_ml->ml_doc);
+#endif
+            if (unlikely(op->func_doc == NULL))
+                return NULL;
+        } else {
+            Py_INCREF(Py_None);
+            return Py_None;
+        }
+    }
+    Py_INCREF(op->func_doc);
+    return op->func_doc;
+}
+static int
+__Pyx_CyFunction_set_doc(__pyx_CyFunctionObject *op, PyObject *value, void *context)
+{
+    CYTHON_UNUSED_VAR(context);
+    if (value == NULL) {
+        value = Py_None;
+    }
+    Py_INCREF(value);
+    __Pyx_Py_XDECREF_SET(op->func_doc, value);
+    return 0;
+}
+static PyObject *
+__Pyx_CyFunction_get_name(__pyx_CyFunctionObject *op, void *context)
+{
+    CYTHON_UNUSED_VAR(context);
+    if (unlikely(op->func_name == NULL)) {
+#if PY_MAJOR_VERSION >= 3
+        op->func_name = PyUnicode_InternFromString(((PyCFunctionObject*)op)->m_ml->ml_name);
+#else
+        op->func_name = PyString_InternFromString(((PyCFunctionObject*)op)->m_ml->ml_name);
+#endif
+        if (unlikely(op->func_name == NULL))
+            return NULL;
+    }
+    Py_INCREF(op->func_name);
+    return op->func_name;
+}
+static int
+__Pyx_CyFunction_set_name(__pyx_CyFunctionObject *op, PyObject *value, void *context)
+{
+    CYTHON_UNUSED_VAR(context);
+#if PY_MAJOR_VERSION >= 3
+    if (unlikely(value == NULL || !PyUnicode_Check(value)))
+#else
+    if (unlikely(value == NULL || !PyString_Check(value)))
+#endif
+    {
+        PyErr_SetString(PyExc_TypeError,
+                        "__name__ must be set to a string object");
+        return -1;
+    }
+    Py_INCREF(value);
+    __Pyx_Py_XDECREF_SET(op->func_name, value);
+    return 0;
+}
+static PyObject *
+__Pyx_CyFunction_get_qualname(__pyx_CyFunctionObject *op, void *context)
+{
+    CYTHON_UNUSED_VAR(context);
+    Py_INCREF(op->func_qualname);
+    return op->func_qualname;
+}
+static int
+__Pyx_CyFunction_set_qualname(__pyx_CyFunctionObject *op, PyObject *value, void *context)
+{
+    CYTHON_UNUSED_VAR(context);
+#if PY_MAJOR_VERSION >= 3
+    if (unlikely(value == NULL || !PyUnicode_Check(value)))
+#else
+    if (unlikely(value == NULL || !PyString_Check(value)))
+#endif
+    {
+        PyErr_SetString(PyExc_TypeError,
+                        "__qualname__ must be set to a string object");
+        return -1;
+    }
+    Py_INCREF(value);
+    __Pyx_Py_XDECREF_SET(op->func_qualname, value);
+    return 0;
+}
+static PyObject *
+__Pyx_CyFunction_get_dict(__pyx_CyFunctionObject *op, void *context)
+{
+    CYTHON_UNUSED_VAR(context);
+    if (unlikely(op->func_dict == NULL)) {
+        op->func_dict = PyDict_New();
+        if (unlikely(op->func_dict == NULL))
+            return NULL;
+    }
+    Py_INCREF(op->func_dict);
+    return op->func_dict;
+}
+static int
+__Pyx_CyFunction_set_dict(__pyx_CyFunctionObject *op, PyObject *value, void *context)
+{
+    CYTHON_UNUSED_VAR(context);
+    if (unlikely(value == NULL)) {
+        PyErr_SetString(PyExc_TypeError,
+               "function's dictionary may not be deleted");
+        return -1;
+    }
+    if (unlikely(!PyDict_Check(value))) {
+        PyErr_SetString(PyExc_TypeError,
+               "setting function's dictionary to a non-dict");
+        return -1;
+    }
+    Py_INCREF(value);
+    __Pyx_Py_XDECREF_SET(op->func_dict, value);
+    return 0;
+}
+static PyObject *
+__Pyx_CyFunction_get_globals(__pyx_CyFunctionObject *op, void *context)
+{
+    CYTHON_UNUSED_VAR(context);
+    Py_INCREF(op->func_globals);
+    return op->func_globals;
+}
+static PyObject *
+__Pyx_CyFunction_get_closure(__pyx_CyFunctionObject *op, void *context)
+{
+    CYTHON_UNUSED_VAR(op);
+    CYTHON_UNUSED_VAR(context);
+    Py_INCREF(Py_None);
+    return Py_None;
+}
+static PyObject *
+__Pyx_CyFunction_get_code(__pyx_CyFunctionObject *op, void *context)
+{
+    PyObject* result = (op->func_code) ? op->func_code : Py_None;
+    CYTHON_UNUSED_VAR(context);
+    Py_INCREF(result);
+    return result;
+}
+static int
+__Pyx_CyFunction_init_defaults(__pyx_CyFunctionObject *op) {
+    int result = 0;
+    PyObject *res = op->defaults_getter((PyObject *) op);
+    if (unlikely(!res))
+        return -1;
+    #if CYTHON_ASSUME_SAFE_MACROS && !CYTHON_AVOID_BORROWED_REFS
+    op->defaults_tuple = PyTuple_GET_ITEM(res, 0);
+    Py_INCREF(op->defaults_tuple);
+    op->defaults_kwdict = PyTuple_GET_ITEM(res, 1);
+    Py_INCREF(op->defaults_kwdict);
+    #else
+    op->defaults_tuple = PySequence_ITEM(res, 0);
+    if (unlikely(!op->defaults_tuple)) result = -1;
+    else {
+        op->defaults_kwdict = PySequence_ITEM(res, 1);
+        if (unlikely(!op->defaults_kwdict)) result = -1;
+    }
+    #endif
+    Py_DECREF(res);
+    return result;
+}
+static int
+__Pyx_CyFunction_set_defaults(__pyx_CyFunctionObject *op, PyObject* value, void *context) {
+    CYTHON_UNUSED_VAR(context);
+    if (!value) {
+        value = Py_None;
+    } else if (unlikely(value != Py_None && !PyTuple_Check(value))) {
+        PyErr_SetString(PyExc_TypeError,
+                        "__defaults__ must be set to a tuple object");
+        return -1;
+    }
+    PyErr_WarnEx(PyExc_RuntimeWarning, "changes to cyfunction.__defaults__ will not "
+                 "currently affect the values used in function calls", 1);
+    Py_INCREF(value);
+    __Pyx_Py_XDECREF_SET(op->defaults_tuple, value);
+    return 0;
+}
+static PyObject *
+__Pyx_CyFunction_get_defaults(__pyx_CyFunctionObject *op, void *context) {
+    PyObject* result = op->defaults_tuple;
+    CYTHON_UNUSED_VAR(context);
+    if (unlikely(!result)) {
+        if (op->defaults_getter) {
+            if (unlikely(__Pyx_CyFunction_init_defaults(op) < 0)) return NULL;
+            result = op->defaults_tuple;
+        } else {
+            result = Py_None;
+        }
+    }
+    Py_INCREF(result);
+    return result;
+}
+static int
+__Pyx_CyFunction_set_kwdefaults(__pyx_CyFunctionObject *op, PyObject* value, void *context) {
+    CYTHON_UNUSED_VAR(context);
+    if (!value) {
+        value = Py_None;
+    } else if (unlikely(value != Py_None && !PyDict_Check(value))) {
+        PyErr_SetString(PyExc_TypeError,
+                        "__kwdefaults__ must be set to a dict object");
+        return -1;
+    }
+    PyErr_WarnEx(PyExc_RuntimeWarning, "changes to cyfunction.__kwdefaults__ will not "
+                 "currently affect the values used in function calls", 1);
+    Py_INCREF(value);
+    __Pyx_Py_XDECREF_SET(op->defaults_kwdict, value);
+    return 0;
+}
+static PyObject *
+__Pyx_CyFunction_get_kwdefaults(__pyx_CyFunctionObject *op, void *context) {
+    PyObject* result = op->defaults_kwdict;
+    CYTHON_UNUSED_VAR(context);
+    if (unlikely(!result)) {
+        if (op->defaults_getter) {
+            if (unlikely(__Pyx_CyFunction_init_defaults(op) < 0)) return NULL;
+            result = op->defaults_kwdict;
+        } else {
+            result = Py_None;
+        }
+    }
+    Py_INCREF(result);
+    return result;
+}
+static int
+__Pyx_CyFunction_set_annotations(__pyx_CyFunctionObject *op, PyObject* value, void *context) {
+    CYTHON_UNUSED_VAR(context);
+    if (!value || value == Py_None) {
+        value = NULL;
+    } else if (unlikely(!PyDict_Check(value))) {
+        PyErr_SetString(PyExc_TypeError,
+                        "__annotations__ must be set to a dict object");
+        return -1;
+    }
+    Py_XINCREF(value);
+    __Pyx_Py_XDECREF_SET(op->func_annotations, value);
+    return 0;
+}
+static PyObject *
+__Pyx_CyFunction_get_annotations(__pyx_CyFunctionObject *op, void *context) {
+    PyObject* result = op->func_annotations;
+    CYTHON_UNUSED_VAR(context);
+    if (unlikely(!result)) {
+        result = PyDict_New();
+        if (unlikely(!result)) return NULL;
+        op->func_annotations = result;
+    }
+    Py_INCREF(result);
+    return result;
+}
+static PyObject *
+__Pyx_CyFunction_get_is_coroutine(__pyx_CyFunctionObject *op, void *context) {
+    int is_coroutine;
+    CYTHON_UNUSED_VAR(context);
+    if (op->func_is_coroutine) {
+        return __Pyx_NewRef(op->func_is_coroutine);
+    }
+    is_coroutine = op->flags & __Pyx_CYFUNCTION_COROUTINE;
+#if PY_VERSION_HEX >= 0x03050000
+    if (is_coroutine) {
+        PyObject *module, *fromlist, *marker = __pyx_n_s_is_coroutine;
+        fromlist = PyList_New(1);
+        if (unlikely(!fromlist)) return NULL;
+        Py_INCREF(marker);
+        PyList_SET_ITEM(fromlist, 0, marker);
+        module = PyImport_ImportModuleLevelObject(__pyx_n_s_asyncio_coroutines, NULL, NULL, fromlist, 0);
+        Py_DECREF(fromlist);
+        if (unlikely(!module)) goto ignore;
+        op->func_is_coroutine = __Pyx_PyObject_GetAttrStr(module, marker);
+        Py_DECREF(module);
+        if (likely(op->func_is_coroutine)) {
+            return __Pyx_NewRef(op->func_is_coroutine);
+        }
+ignore:
+        PyErr_Clear();
+    }
+#endif
+    op->func_is_coroutine = __Pyx_PyBool_FromLong(is_coroutine);
+    return __Pyx_NewRef(op->func_is_coroutine);
+}
+static PyGetSetDef __pyx_CyFunction_getsets[] = {
+    {(char *) "func_doc", (getter)__Pyx_CyFunction_get_doc, (setter)__Pyx_CyFunction_set_doc, 0, 0},
+    {(char *) "__doc__",  (getter)__Pyx_CyFunction_get_doc, (setter)__Pyx_CyFunction_set_doc, 0, 0},
+    {(char *) "func_name", (getter)__Pyx_CyFunction_get_name, (setter)__Pyx_CyFunction_set_name, 0, 0},
+    {(char *) "__name__", (getter)__Pyx_CyFunction_get_name, (setter)__Pyx_CyFunction_set_name, 0, 0},
+    {(char *) "__qualname__", (getter)__Pyx_CyFunction_get_qualname, (setter)__Pyx_CyFunction_set_qualname, 0, 0},
+    {(char *) "func_dict", (getter)__Pyx_CyFunction_get_dict, (setter)__Pyx_CyFunction_set_dict, 0, 0},
+    {(char *) "__dict__", (getter)__Pyx_CyFunction_get_dict, (setter)__Pyx_CyFunction_set_dict, 0, 0},
+    {(char *) "func_globals", (getter)__Pyx_CyFunction_get_globals, 0, 0, 0},
+    {(char *) "__globals__", (getter)__Pyx_CyFunction_get_globals, 0, 0, 0},
+    {(char *) "func_closure", (getter)__Pyx_CyFunction_get_closure, 0, 0, 0},
+    {(char *) "__closure__", (getter)__Pyx_CyFunction_get_closure, 0, 0, 0},
+    {(char *) "func_code", (getter)__Pyx_CyFunction_get_code, 0, 0, 0},
+    {(char *) "__code__", (getter)__Pyx_CyFunction_get_code, 0, 0, 0},
+    {(char *) "func_defaults", (getter)__Pyx_CyFunction_get_defaults, (setter)__Pyx_CyFunction_set_defaults, 0, 0},
+    {(char *) "__defaults__", (getter)__Pyx_CyFunction_get_defaults, (setter)__Pyx_CyFunction_set_defaults, 0, 0},
+    {(char *) "__kwdefaults__", (getter)__Pyx_CyFunction_get_kwdefaults, (setter)__Pyx_CyFunction_set_kwdefaults, 0, 0},
+    {(char *) "__annotations__", (getter)__Pyx_CyFunction_get_annotations, (setter)__Pyx_CyFunction_set_annotations, 0, 0},
+    {(char *) "_is_coroutine", (getter)__Pyx_CyFunction_get_is_coroutine, 0, 0, 0},
+    {0, 0, 0, 0, 0}
+};
+static PyMemberDef __pyx_CyFunction_members[] = {
+    {(char *) "__module__", T_OBJECT, offsetof(PyCFunctionObject, m_module), 0, 0},
+#if CYTHON_USE_TYPE_SPECS
+    {(char *) "__dictoffset__", T_PYSSIZET, offsetof(__pyx_CyFunctionObject, func_dict), READONLY, 0},
+#if CYTHON_METH_FASTCALL
+#if CYTHON_BACKPORT_VECTORCALL
+    {(char *) "__vectorcalloffset__", T_PYSSIZET, offsetof(__pyx_CyFunctionObject, func_vectorcall), READONLY, 0},
+#else
+    {(char *) "__vectorcalloffset__", T_PYSSIZET, offsetof(PyCFunctionObject, vectorcall), READONLY, 0},
+#endif
+#endif
+#if PY_VERSION_HEX < 0x030500A0
+    {(char *) "__weaklistoffset__", T_PYSSIZET, offsetof(__pyx_CyFunctionObject, func_weakreflist), READONLY, 0},
+#else
+    {(char *) "__weaklistoffset__", T_PYSSIZET, offsetof(PyCFunctionObject, m_weakreflist), READONLY, 0},
+#endif
+#endif
+    {0, 0, 0,  0, 0}
+};
+static PyObject *
+__Pyx_CyFunction_reduce(__pyx_CyFunctionObject *m, PyObject *args)
+{
+    CYTHON_UNUSED_VAR(args);
+#if PY_MAJOR_VERSION >= 3
+    Py_INCREF(m->func_qualname);
+    return m->func_qualname;
+#else
+    return PyString_FromString(((PyCFunctionObject*)m)->m_ml->ml_name);
+#endif
+}
+static PyMethodDef __pyx_CyFunction_methods[] = {
+    {"__reduce__", (PyCFunction)__Pyx_CyFunction_reduce, METH_VARARGS, 0},
+    {0, 0, 0, 0}
+};
+#if PY_VERSION_HEX < 0x030500A0
+#define __Pyx_CyFunction_weakreflist(cyfunc) ((cyfunc)->func_weakreflist)
+#else
+#define __Pyx_CyFunction_weakreflist(cyfunc) (((PyCFunctionObject*)cyfunc)->m_weakreflist)
+#endif
+static PyObject *__Pyx_CyFunction_Init(__pyx_CyFunctionObject *op, PyMethodDef *ml, int flags, PyObject* qualname,
+                                       PyObject *closure, PyObject *module, PyObject* globals, PyObject* code) {
+    PyCFunctionObject *cf = (PyCFunctionObject*) op;
+    if (unlikely(op == NULL))
+        return NULL;
+    op->flags = flags;
+    __Pyx_CyFunction_weakreflist(op) = NULL;
+    cf->m_ml = ml;
+    cf->m_self = (PyObject *) op;
+    Py_XINCREF(closure);
+    op->func_closure = closure;
+    Py_XINCREF(module);
+    cf->m_module = module;
+    op->func_dict = NULL;
+    op->func_name = NULL;
+    Py_INCREF(qualname);
+    op->func_qualname = qualname;
+    op->func_doc = NULL;
+#if PY_VERSION_HEX < 0x030900B1
+    op->func_classobj = NULL;
+#else
+    ((PyCMethodObject*)op)->mm_class = NULL;
+#endif
+    op->func_globals = globals;
+    Py_INCREF(op->func_globals);
+    Py_XINCREF(code);
+    op->func_code = code;
+    op->defaults_pyobjects = 0;
+    op->defaults_size = 0;
+    op->defaults = NULL;
+    op->defaults_tuple = NULL;
+    op->defaults_kwdict = NULL;
+    op->defaults_getter = NULL;
+    op->func_annotations = NULL;
+    op->func_is_coroutine = NULL;
+#if CYTHON_METH_FASTCALL
+    switch (ml->ml_flags & (METH_VARARGS | METH_FASTCALL | METH_NOARGS | METH_O | METH_KEYWORDS | METH_METHOD)) {
+    case METH_NOARGS:
+        __Pyx_CyFunction_func_vectorcall(op) = __Pyx_CyFunction_Vectorcall_NOARGS;
+        break;
+    case METH_O:
+        __Pyx_CyFunction_func_vectorcall(op) = __Pyx_CyFunction_Vectorcall_O;
+        break;
+    case METH_METHOD | METH_FASTCALL | METH_KEYWORDS:
+        __Pyx_CyFunction_func_vectorcall(op) = __Pyx_CyFunction_Vectorcall_FASTCALL_KEYWORDS_METHOD;
+        break;
+    case METH_FASTCALL | METH_KEYWORDS:
+        __Pyx_CyFunction_func_vectorcall(op) = __Pyx_CyFunction_Vectorcall_FASTCALL_KEYWORDS;
+        break;
+    case METH_VARARGS | METH_KEYWORDS:
+        __Pyx_CyFunction_func_vectorcall(op) = NULL;
+        break;
+    default:
+        PyErr_SetString(PyExc_SystemError, "Bad call flags for CyFunction");
+        Py_DECREF(op);
+        return NULL;
+    }
+#endif
+    return (PyObject *) op;
+}
+static int
+__Pyx_CyFunction_clear(__pyx_CyFunctionObject *m)
+{
+    Py_CLEAR(m->func_closure);
+    Py_CLEAR(((PyCFunctionObject*)m)->m_module);
+    Py_CLEAR(m->func_dict);
+    Py_CLEAR(m->func_name);
+    Py_CLEAR(m->func_qualname);
+    Py_CLEAR(m->func_doc);
+    Py_CLEAR(m->func_globals);
+    Py_CLEAR(m->func_code);
+#if PY_VERSION_HEX < 0x030900B1
+    Py_CLEAR(__Pyx_CyFunction_GetClassObj(m));
+#else
+    {
+        PyObject *cls = (PyObject*) ((PyCMethodObject *) (m))->mm_class;
+        ((PyCMethodObject *) (m))->mm_class = NULL;
+        Py_XDECREF(cls);
+    }
+#endif
+    Py_CLEAR(m->defaults_tuple);
+    Py_CLEAR(m->defaults_kwdict);
+    Py_CLEAR(m->func_annotations);
+    Py_CLEAR(m->func_is_coroutine);
+    if (m->defaults) {
+        PyObject **pydefaults = __Pyx_CyFunction_Defaults(PyObject *, m);
+        int i;
+        for (i = 0; i < m->defaults_pyobjects; i++)
+            Py_XDECREF(pydefaults[i]);
+        PyObject_Free(m->defaults);
+        m->defaults = NULL;
+    }
+    return 0;
+}
+static void __Pyx__CyFunction_dealloc(__pyx_CyFunctionObject *m)
+{
+    if (__Pyx_CyFunction_weakreflist(m) != NULL)
+        PyObject_ClearWeakRefs((PyObject *) m);
+    __Pyx_CyFunction_clear(m);
+    __Pyx_PyHeapTypeObject_GC_Del(m);
+}
+static void __Pyx_CyFunction_dealloc(__pyx_CyFunctionObject *m)
+{
+    PyObject_GC_UnTrack(m);
+    __Pyx__CyFunction_dealloc(m);
+}
+static int __Pyx_CyFunction_traverse(__pyx_CyFunctionObject *m, visitproc visit, void *arg)
+{
+    Py_VISIT(m->func_closure);
+    Py_VISIT(((PyCFunctionObject*)m)->m_module);
+    Py_VISIT(m->func_dict);
+    Py_VISIT(m->func_name);
+    Py_VISIT(m->func_qualname);
+    Py_VISIT(m->func_doc);
+    Py_VISIT(m->func_globals);
+    Py_VISIT(m->func_code);
+    Py_VISIT(__Pyx_CyFunction_GetClassObj(m));
+    Py_VISIT(m->defaults_tuple);
+    Py_VISIT(m->defaults_kwdict);
+    Py_VISIT(m->func_is_coroutine);
+    if (m->defaults) {
+        PyObject **pydefaults = __Pyx_CyFunction_Defaults(PyObject *, m);
+        int i;
+        for (i = 0; i < m->defaults_pyobjects; i++)
+            Py_VISIT(pydefaults[i]);
+    }
+    return 0;
+}
+static PyObject*
+__Pyx_CyFunction_repr(__pyx_CyFunctionObject *op)
+{
+#if PY_MAJOR_VERSION >= 3
+    return PyUnicode_FromFormat("<cyfunction %U at %p>",
+                                op->func_qualname, (void *)op);
+#else
+    return PyString_FromFormat("<cyfunction %s at %p>",
+                               PyString_AsString(op->func_qualname), (void *)op);
+#endif
+}
+static PyObject * __Pyx_CyFunction_CallMethod(PyObject *func, PyObject *self, PyObject *arg, PyObject *kw) {
+    PyCFunctionObject* f = (PyCFunctionObject*)func;
+    PyCFunction meth = f->m_ml->ml_meth;
+    Py_ssize_t size;
+    switch (f->m_ml->ml_flags & (METH_VARARGS | METH_KEYWORDS | METH_NOARGS | METH_O)) {
+    case METH_VARARGS:
+        if (likely(kw == NULL || PyDict_Size(kw) == 0))
+            return (*meth)(self, arg);
+        break;
+    case METH_VARARGS | METH_KEYWORDS:
+        return (*(PyCFunctionWithKeywords)(void*)meth)(self, arg, kw);
+    case METH_NOARGS:
+        if (likely(kw == NULL || PyDict_Size(kw) == 0)) {
+            size = PyTuple_GET_SIZE(arg);
+            if (likely(size == 0))
+                return (*meth)(self, NULL);
+            PyErr_Format(PyExc_TypeError,
+                "%.200s() takes no arguments (%" CYTHON_FORMAT_SSIZE_T "d given)",
+                f->m_ml->ml_name, size);
+            return NULL;
+        }
+        break;
+    case METH_O:
+        if (likely(kw == NULL || PyDict_Size(kw) == 0)) {
+            size = PyTuple_GET_SIZE(arg);
+            if (likely(size == 1)) {
+                PyObject *result, *arg0;
+                #if CYTHON_ASSUME_SAFE_MACROS && !CYTHON_AVOID_BORROWED_REFS
+                arg0 = PyTuple_GET_ITEM(arg, 0);
+                #else
+                arg0 = PySequence_ITEM(arg, 0); if (unlikely(!arg0)) return NULL;
+                #endif
+                result = (*meth)(self, arg0);
+                #if !(CYTHON_ASSUME_SAFE_MACROS && !CYTHON_AVOID_BORROWED_REFS)
+                Py_DECREF(arg0);
+                #endif
+                return result;
+            }
+            PyErr_Format(PyExc_TypeError,
+                "%.200s() takes exactly one argument (%" CYTHON_FORMAT_SSIZE_T "d given)",
+                f->m_ml->ml_name, size);
+            return NULL;
+        }
+        break;
+    default:
+        PyErr_SetString(PyExc_SystemError, "Bad call flags for CyFunction");
+        return NULL;
+    }
+    PyErr_Format(PyExc_TypeError, "%.200s() takes no keyword arguments",
+                 f->m_ml->ml_name);
+    return NULL;
+}
+static CYTHON_INLINE PyObject *__Pyx_CyFunction_Call(PyObject *func, PyObject *arg, PyObject *kw) {
+    return __Pyx_CyFunction_CallMethod(func, ((PyCFunctionObject*)func)->m_self, arg, kw);
+}
+static PyObject *__Pyx_CyFunction_CallAsMethod(PyObject *func, PyObject *args, PyObject *kw) {
+    PyObject *result;
+    __pyx_CyFunctionObject *cyfunc = (__pyx_CyFunctionObject *) func;
+#if CYTHON_METH_FASTCALL
+     __pyx_vectorcallfunc vc = __Pyx_CyFunction_func_vectorcall(cyfunc);
+    if (vc) {
+#if CYTHON_ASSUME_SAFE_MACROS
+        return __Pyx_PyVectorcall_FastCallDict(func, vc, &PyTuple_GET_ITEM(args, 0), (size_t)PyTuple_GET_SIZE(args), kw);
+#else
+        (void) &__Pyx_PyVectorcall_FastCallDict;
+        return PyVectorcall_Call(func, args, kw);
+#endif
+    }
+#endif
+    if ((cyfunc->flags & __Pyx_CYFUNCTION_CCLASS) && !(cyfunc->flags & __Pyx_CYFUNCTION_STATICMETHOD)) {
+        Py_ssize_t argc;
+        PyObject *new_args;
+        PyObject *self;
+        argc = PyTuple_GET_SIZE(args);
+        new_args = PyTuple_GetSlice(args, 1, argc);
+        if (unlikely(!new_args))
+            return NULL;
+        self = PyTuple_GetItem(args, 0);
+        if (unlikely(!self)) {
+            Py_DECREF(new_args);
+#if PY_MAJOR_VERSION > 2
+            PyErr_Format(PyExc_TypeError,
+                         "unbound method %.200S() needs an argument",
+                         cyfunc->func_qualname);
+#else
+            PyErr_SetString(PyExc_TypeError,
+                            "unbound method needs an argument");
+#endif
+            return NULL;
+        }
+        result = __Pyx_CyFunction_CallMethod(func, self, new_args, kw);
+        Py_DECREF(new_args);
+    } else {
+        result = __Pyx_CyFunction_Call(func, args, kw);
+    }
+    return result;
+}
+#if CYTHON_METH_FASTCALL
+static CYTHON_INLINE int __Pyx_CyFunction_Vectorcall_CheckArgs(__pyx_CyFunctionObject *cyfunc, Py_ssize_t nargs, PyObject *kwnames)
+{
+    int ret = 0;
+    if ((cyfunc->flags & __Pyx_CYFUNCTION_CCLASS) && !(cyfunc->flags & __Pyx_CYFUNCTION_STATICMETHOD)) {
+        if (unlikely(nargs < 1)) {
+            PyErr_Format(PyExc_TypeError, "%.200s() needs an argument",
+                         ((PyCFunctionObject*)cyfunc)->m_ml->ml_name);
+            return -1;
+        }
+        ret = 1;
+    }
+    if (unlikely(kwnames) && unlikely(PyTuple_GET_SIZE(kwnames))) {
+        PyErr_Format(PyExc_TypeError,
+                     "%.200s() takes no keyword arguments", ((PyCFunctionObject*)cyfunc)->m_ml->ml_name);
+        return -1;
+    }
+    return ret;
+}
+static PyObject * __Pyx_CyFunction_Vectorcall_NOARGS(PyObject *func, PyObject *const *args, size_t nargsf, PyObject *kwnames)
+{
+    __pyx_CyFunctionObject *cyfunc = (__pyx_CyFunctionObject *)func;
+    PyMethodDef* def = ((PyCFunctionObject*)cyfunc)->m_ml;
+#if CYTHON_BACKPORT_VECTORCALL
+    Py_ssize_t nargs = (Py_ssize_t)nargsf;
+#else
+    Py_ssize_t nargs = PyVectorcall_NARGS(nargsf);
+#endif
+    PyObject *self;
+    switch (__Pyx_CyFunction_Vectorcall_CheckArgs(cyfunc, nargs, kwnames)) {
+    case 1:
+        self = args[0];
+        args += 1;
+        nargs -= 1;
+        break;
+    case 0:
+        self = ((PyCFunctionObject*)cyfunc)->m_self;
+        break;
+    default:
+        return NULL;
+    }
+    if (unlikely(nargs != 0)) {
+        PyErr_Format(PyExc_TypeError,
+            "%.200s() takes no arguments (%" CYTHON_FORMAT_SSIZE_T "d given)",
+            def->ml_name, nargs);
+        return NULL;
+    }
+    return def->ml_meth(self, NULL);
+}
+static PyObject * __Pyx_CyFunction_Vectorcall_O(PyObject *func, PyObject *const *args, size_t nargsf, PyObject *kwnames)
+{
+    __pyx_CyFunctionObject *cyfunc = (__pyx_CyFunctionObject *)func;
+    PyMethodDef* def = ((PyCFunctionObject*)cyfunc)->m_ml;
+#if CYTHON_BACKPORT_VECTORCALL
+    Py_ssize_t nargs = (Py_ssize_t)nargsf;
+#else
+    Py_ssize_t nargs = PyVectorcall_NARGS(nargsf);
+#endif
+    PyObject *self;
+    switch (__Pyx_CyFunction_Vectorcall_CheckArgs(cyfunc, nargs, kwnames)) {
+    case 1:
+        self = args[0];
+        args += 1;
+        nargs -= 1;
+        break;
+    case 0:
+        self = ((PyCFunctionObject*)cyfunc)->m_self;
+        break;
+    default:
+        return NULL;
+    }
+    if (unlikely(nargs != 1)) {
+        PyErr_Format(PyExc_TypeError,
+            "%.200s() takes exactly one argument (%" CYTHON_FORMAT_SSIZE_T "d given)",
+            def->ml_name, nargs);
+        return NULL;
+    }
+    return def->ml_meth(self, args[0]);
+}
+static PyObject * __Pyx_CyFunction_Vectorcall_FASTCALL_KEYWORDS(PyObject *func, PyObject *const *args, size_t nargsf, PyObject *kwnames)
+{
+    __pyx_CyFunctionObject *cyfunc = (__pyx_CyFunctionObject *)func;
+    PyMethodDef* def = ((PyCFunctionObject*)cyfunc)->m_ml;
+#if CYTHON_BACKPORT_VECTORCALL
+    Py_ssize_t nargs = (Py_ssize_t)nargsf;
+#else
+    Py_ssize_t nargs = PyVectorcall_NARGS(nargsf);
+#endif
+    PyObject *self;
+    switch (__Pyx_CyFunction_Vectorcall_CheckArgs(cyfunc, nargs, NULL)) {
+    case 1:
+        self = args[0];
+        args += 1;
+        nargs -= 1;
+        break;
+    case 0:
+        self = ((PyCFunctionObject*)cyfunc)->m_self;
+        break;
+    default:
+        return NULL;
+    }
+    return ((_PyCFunctionFastWithKeywords)(void(*)(void))def->ml_meth)(self, args, nargs, kwnames);
+}
+static PyObject * __Pyx_CyFunction_Vectorcall_FASTCALL_KEYWORDS_METHOD(PyObject *func, PyObject *const *args, size_t nargsf, PyObject *kwnames)
+{
+    __pyx_CyFunctionObject *cyfunc = (__pyx_CyFunctionObject *)func;
+    PyMethodDef* def = ((PyCFunctionObject*)cyfunc)->m_ml;
+    PyTypeObject *cls = (PyTypeObject *) __Pyx_CyFunction_GetClassObj(cyfunc);
+#if CYTHON_BACKPORT_VECTORCALL
+    Py_ssize_t nargs = (Py_ssize_t)nargsf;
+#else
+    Py_ssize_t nargs = PyVectorcall_NARGS(nargsf);
+#endif
+    PyObject *self;
+    switch (__Pyx_CyFunction_Vectorcall_CheckArgs(cyfunc, nargs, NULL)) {
+    case 1:
+        self = args[0];
+        args += 1;
+        nargs -= 1;
+        break;
+    case 0:
+        self = ((PyCFunctionObject*)cyfunc)->m_self;
+        break;
+    default:
+        return NULL;
+    }
+    return ((__Pyx_PyCMethod)(void(*)(void))def->ml_meth)(self, cls, args, (size_t)nargs, kwnames);
+}
+#endif
+#if CYTHON_USE_TYPE_SPECS
+static PyType_Slot __pyx_CyFunctionType_slots[] = {
+    {Py_tp_dealloc, (void *)__Pyx_CyFunction_dealloc},
+    {Py_tp_repr, (void *)__Pyx_CyFunction_repr},
+    {Py_tp_call, (void *)__Pyx_CyFunction_CallAsMethod},
+    {Py_tp_traverse, (void *)__Pyx_CyFunction_traverse},
+    {Py_tp_clear, (void *)__Pyx_CyFunction_clear},
+    {Py_tp_methods, (void *)__pyx_CyFunction_methods},
+    {Py_tp_members, (void *)__pyx_CyFunction_members},
+    {Py_tp_getset, (void *)__pyx_CyFunction_getsets},
+    {Py_tp_descr_get, (void *)__Pyx_PyMethod_New},
+    {0, 0},
+};
+static PyType_Spec __pyx_CyFunctionType_spec = {
+    __PYX_TYPE_MODULE_PREFIX "cython_function_or_method",
+    sizeof(__pyx_CyFunctionObject),
+    0,
+#ifdef Py_TPFLAGS_METHOD_DESCRIPTOR
+    Py_TPFLAGS_METHOD_DESCRIPTOR |
+#endif
+#if (defined(_Py_TPFLAGS_HAVE_VECTORCALL) && CYTHON_METH_FASTCALL)
+    _Py_TPFLAGS_HAVE_VECTORCALL |
+#endif
+    Py_TPFLAGS_DEFAULT | Py_TPFLAGS_HAVE_GC | Py_TPFLAGS_BASETYPE,
+    __pyx_CyFunctionType_slots
+};
+#else
+static PyTypeObject __pyx_CyFunctionType_type = {
+    PyVarObject_HEAD_INIT(0, 0)
+    __PYX_TYPE_MODULE_PREFIX "cython_function_or_method",
+    sizeof(__pyx_CyFunctionObject),
+    0,
+    (destructor) __Pyx_CyFunction_dealloc,
+#if !CYTHON_METH_FASTCALL
+    0,
+#elif CYTHON_BACKPORT_VECTORCALL
+    (printfunc)offsetof(__pyx_CyFunctionObject, func_vectorcall),
+#else
+    offsetof(PyCFunctionObject, vectorcall),
+#endif
+    0,
+    0,
+#if PY_MAJOR_VERSION < 3
+    0,
+#else
+    0,
+#endif
+    (reprfunc) __Pyx_CyFunction_repr,
+    0,
+    0,
+    0,
+    0,
+    __Pyx_CyFunction_CallAsMethod,
+    0,
+    0,
+    0,
+    0,
+#ifdef Py_TPFLAGS_METHOD_DESCRIPTOR
+    Py_TPFLAGS_METHOD_DESCRIPTOR |
+#endif
+#ifdef _Py_TPFLAGS_HAVE_VECTORCALL
+    _Py_TPFLAGS_HAVE_VECTORCALL |
+#endif
+    Py_TPFLAGS_DEFAULT | Py_TPFLAGS_HAVE_GC | Py_TPFLAGS_BASETYPE,
+    0,
+    (traverseproc) __Pyx_CyFunction_traverse,
+    (inquiry) __Pyx_CyFunction_clear,
+    0,
+#if PY_VERSION_HEX < 0x030500A0
+    offsetof(__pyx_CyFunctionObject, func_weakreflist),
+#else
+    offsetof(PyCFunctionObject, m_weakreflist),
+#endif
+    0,
+    0,
+    __pyx_CyFunction_methods,
+    __pyx_CyFunction_members,
+    __pyx_CyFunction_getsets,
+    0,
+    0,
+    __Pyx_PyMethod_New,
+    0,
+    offsetof(__pyx_CyFunctionObject, func_dict),
+    0,
+    0,
+    0,
+    0,
+    0,
+    0,
+    0,
+    0,
+    0,
+    0,
+    0,
+    0,
+#if PY_VERSION_HEX >= 0x030400a1
+    0,
+#endif
+#if PY_VERSION_HEX >= 0x030800b1 && (!CYTHON_COMPILING_IN_PYPY || PYPY_VERSION_NUM >= 0x07030800)
+    0,
+#endif
+#if __PYX_NEED_TP_PRINT_SLOT
+    0,
+#endif
+#if PY_VERSION_HEX >= 0x030C0000
+    0,
+#endif
+#if CYTHON_COMPILING_IN_PYPY && PY_VERSION_HEX >= 0x03090000 && PY_VERSION_HEX < 0x030a0000
+    0,
+#endif
+};
+#endif
+static int __pyx_CyFunction_init(PyObject *module) {
+#if CYTHON_USE_TYPE_SPECS
+    __pyx_CyFunctionType = __Pyx_FetchCommonTypeFromSpec(module, &__pyx_CyFunctionType_spec, NULL);
+#else
+    CYTHON_UNUSED_VAR(module);
+    __pyx_CyFunctionType = __Pyx_FetchCommonType(&__pyx_CyFunctionType_type);
+#endif
+    if (unlikely(__pyx_CyFunctionType == NULL)) {
+        return -1;
+    }
+    return 0;
+}
+static CYTHON_INLINE void *__Pyx_CyFunction_InitDefaults(PyObject *func, size_t size, int pyobjects) {
+    __pyx_CyFunctionObject *m = (__pyx_CyFunctionObject *) func;
+    m->defaults = PyObject_Malloc(size);
+    if (unlikely(!m->defaults))
+        return PyErr_NoMemory();
+    memset(m->defaults, 0, size);
+    m->defaults_pyobjects = pyobjects;
+    m->defaults_size = size;
+    return m->defaults;
+}
+static CYTHON_INLINE void __Pyx_CyFunction_SetDefaultsTuple(PyObject *func, PyObject *tuple) {
+    __pyx_CyFunctionObject *m = (__pyx_CyFunctionObject *) func;
+    m->defaults_tuple = tuple;
+    Py_INCREF(tuple);
+}
+static CYTHON_INLINE void __Pyx_CyFunction_SetDefaultsKwDict(PyObject *func, PyObject *dict) {
+    __pyx_CyFunctionObject *m = (__pyx_CyFunctionObject *) func;
+    m->defaults_kwdict = dict;
+    Py_INCREF(dict);
+}
+static CYTHON_INLINE void __Pyx_CyFunction_SetAnnotationsDict(PyObject *func, PyObject *dict) {
+    __pyx_CyFunctionObject *m = (__pyx_CyFunctionObject *) func;
+    m->func_annotations = dict;
+    Py_INCREF(dict);
+}
+
+/* CythonFunction */
+static PyObject *__Pyx_CyFunction_New(PyMethodDef *ml, int flags, PyObject* qualname,
+                                      PyObject *closure, PyObject *module, PyObject* globals, PyObject* code) {
+    PyObject *op = __Pyx_CyFunction_Init(
+        PyObject_GC_New(__pyx_CyFunctionObject, __pyx_CyFunctionType),
+        ml, flags, qualname, closure, module, globals, code
+    );
+    if (likely(op)) {
+        PyObject_GC_Track(op);
+    }
+    return op;
+}
 
 /* PyDictVersioning */
 #if CYTHON_USE_DICT_VERSIONS && CYTHON_USE_TYPE_SLOTS
 static CYTHON_INLINE PY_UINT64_T __Pyx_get_tp_dict_version(PyObject *obj) {
     PyObject *dict = Py_TYPE(obj)->tp_dict;
     return likely(dict) ? __PYX_GET_DICT_VERSION(dict) : 0;
 }
@@ -8094,34 +13788,35 @@
         return 0;
     return obj_dict_version == __Pyx_get_object_dict_version(obj);
 }
 #endif
 
 /* CLineInTraceback */
 #ifndef CYTHON_CLINE_IN_TRACEBACK
-static int __Pyx_CLineForTraceback(CYTHON_UNUSED PyThreadState *tstate, int c_line) {
+static int __Pyx_CLineForTraceback(PyThreadState *tstate, int c_line) {
     PyObject *use_cline;
     PyObject *ptype, *pvalue, *ptraceback;
 #if CYTHON_COMPILING_IN_CPYTHON
     PyObject **cython_runtime_dict;
 #endif
+    CYTHON_MAYBE_UNUSED_VAR(tstate);
     if (unlikely(!__pyx_cython_runtime)) {
         return c_line;
     }
     __Pyx_ErrFetchInState(tstate, &ptype, &pvalue, &ptraceback);
 #if CYTHON_COMPILING_IN_CPYTHON
     cython_runtime_dict = _PyObject_GetDictPtr(__pyx_cython_runtime);
     if (likely(cython_runtime_dict)) {
         __PYX_PY_DICT_LOOKUP_IF_MODIFIED(
             use_cline, *cython_runtime_dict,
             __Pyx_PyDict_GetItemStr(*cython_runtime_dict, __pyx_n_s_cline_in_traceback))
     } else
 #endif
     {
-      PyObject *use_cline_obj = __Pyx_PyObject_GetAttrStr(__pyx_cython_runtime, __pyx_n_s_cline_in_traceback);
+      PyObject *use_cline_obj = __Pyx_PyObject_GetAttrStrNoError(__pyx_cython_runtime, __pyx_n_s_cline_in_traceback);
       if (use_cline_obj) {
         use_cline = PyObject_Not(use_cline_obj) ? Py_False : Py_True;
         Py_DECREF(use_cline_obj);
       } else {
         PyErr_Clear();
         use_cline = NULL;
       }
@@ -8135,14 +13830,15 @@
     }
     __Pyx_ErrRestoreInState(tstate, ptype, pvalue, ptraceback);
     return c_line;
 }
 #endif
 
 /* CodeObjectCache */
+#if !CYTHON_COMPILING_IN_LIMITED_API
 static int __pyx_bisect_code_objects(__Pyx_CodeObjectCacheEntry* entries, int count, int code_line) {
     int start = 0, mid = 0, end = count - 1;
     if (end >= 0 && code_line > entries[end].code_line) {
         return count;
     }
     while (start < end) {
         mid = start + (end - start) / 2;
@@ -8213,25 +13909,36 @@
         entries[i] = entries[i-1];
     }
     entries[pos].code_line = code_line;
     entries[pos].code_object = code_object;
     __pyx_code_cache.count++;
     Py_INCREF(code_object);
 }
+#endif
 
 /* AddTraceback */
 #include "compile.h"
 #include "frameobject.h"
 #include "traceback.h"
 #if PY_VERSION_HEX >= 0x030b00a6
   #ifndef Py_BUILD_CORE
     #define Py_BUILD_CORE 1
   #endif
   #include "internal/pycore_frame.h"
 #endif
+#if CYTHON_COMPILING_IN_LIMITED_API
+static void __Pyx_AddTraceback(const char *funcname, int c_line,
+                               int py_line, const char *filename) {
+    if (c_line) {
+        (void) __pyx_cfilenm;
+        (void) __Pyx_CLineForTraceback(__Pyx_PyThreadState_Current, c_line);
+    }
+    _PyTraceback_Add(funcname, filename, py_line);
+}
+#else
 static PyCodeObject* __Pyx_CreateCodeObjectForTraceback(
             const char *funcname, int c_line,
             int py_line, const char *filename) {
     PyCodeObject *py_code = NULL;
     PyObject *py_funcname = NULL;
     #if PY_MAJOR_VERSION < 3
     PyObject *py_srcfile = NULL;
@@ -8258,14 +13965,15 @@
     #if PY_MAJOR_VERSION < 3
     py_code = __Pyx_PyCode_New(
         0,
         0,
         0,
         0,
         0,
+        0,
         __pyx_empty_bytes, /*PyObject *code,*/
         __pyx_empty_tuple, /*PyObject *consts,*/
         __pyx_empty_tuple, /*PyObject *names,*/
         __pyx_empty_tuple, /*PyObject *varnames,*/
         __pyx_empty_tuple, /*PyObject *freevars,*/
         __pyx_empty_tuple, /*PyObject *cellvars,*/
         py_srcfile,   /*PyObject *filename,*/
@@ -8320,14 +14028,15 @@
     if (!py_frame) goto bad;
     __Pyx_PyFrame_SetLineNumber(py_frame, py_line);
     PyTraceBack_Here(py_frame);
 bad:
     Py_XDECREF(py_code);
     Py_XDECREF(py_frame);
 }
+#endif
 
 /* CIntFromPyVerify */
 #define __PYX_VERIFY_RETURN_INT(target_type, func_type, func_value)\
     __PYX__VERIFY_RETURN_INT(target_type, func_type, func_value, 0)
 #define __PYX_VERIFY_RETURN_INT_EXC(target_type, func_type, func_value)\
     __PYX__VERIFY_RETURN_INT(target_type, func_type, func_value, 1)
 #define __PYX__VERIFY_RETURN_INT(target_type, func_type, func_value, exc)\
@@ -8356,59 +14065,64 @@
     const size_t neg_one = (size_t) -1, const_zero = (size_t) 0;
 #ifdef __Pyx_HAS_GCC_DIAGNOSTIC
 #pragma GCC diagnostic pop
 #endif
     const int is_unsigned = neg_one > const_zero;
 #if PY_MAJOR_VERSION < 3
     if (likely(PyInt_Check(x))) {
-        if (sizeof(size_t) < sizeof(long)) {
+        if ((sizeof(size_t) < sizeof(long))) {
             __PYX_VERIFY_RETURN_INT(size_t, long, PyInt_AS_LONG(x))
         } else {
             long val = PyInt_AS_LONG(x);
             if (is_unsigned && unlikely(val < 0)) {
                 goto raise_neg_overflow;
             }
             return (size_t) val;
         }
     } else
 #endif
     if (likely(PyLong_Check(x))) {
         if (is_unsigned) {
 #if CYTHON_USE_PYLONG_INTERNALS
-            const digit* digits = ((PyLongObject*)x)->ob_digit;
-            switch (Py_SIZE(x)) {
-                case  0: return (size_t) 0;
-                case  1: __PYX_VERIFY_RETURN_INT(size_t, digit, digits[0])
-                case 2:
-                    if (8 * sizeof(size_t) > 1 * PyLong_SHIFT) {
-                        if (8 * sizeof(unsigned long) > 2 * PyLong_SHIFT) {
-                            __PYX_VERIFY_RETURN_INT(size_t, unsigned long, (((((unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
-                        } else if (8 * sizeof(size_t) >= 2 * PyLong_SHIFT) {
-                            return (size_t) (((((size_t)digits[1]) << PyLong_SHIFT) | (size_t)digits[0]));
+            if (unlikely(__Pyx_PyLong_IsNeg(x))) {
+                goto raise_neg_overflow;
+            } else if (__Pyx_PyLong_IsCompact(x)) {
+                __PYX_VERIFY_RETURN_INT(size_t, __Pyx_compact_upylong, __Pyx_PyLong_CompactValueUnsigned(x))
+            } else {
+                const digit* digits = __Pyx_PyLong_Digits(x);
+                assert(__Pyx_PyLong_DigitCount(x) > 1);
+                switch (__Pyx_PyLong_DigitCount(x)) {
+                    case 2:
+                        if ((8 * sizeof(size_t) > 1 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 2 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(size_t, unsigned long, (((((unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(size_t) >= 2 * PyLong_SHIFT)) {
+                                return (size_t) (((((size_t)digits[1]) << PyLong_SHIFT) | (size_t)digits[0]));
+                            }
                         }
-                    }
-                    break;
-                case 3:
-                    if (8 * sizeof(size_t) > 2 * PyLong_SHIFT) {
-                        if (8 * sizeof(unsigned long) > 3 * PyLong_SHIFT) {
-                            __PYX_VERIFY_RETURN_INT(size_t, unsigned long, (((((((unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
-                        } else if (8 * sizeof(size_t) >= 3 * PyLong_SHIFT) {
-                            return (size_t) (((((((size_t)digits[2]) << PyLong_SHIFT) | (size_t)digits[1]) << PyLong_SHIFT) | (size_t)digits[0]));
+                        break;
+                    case 3:
+                        if ((8 * sizeof(size_t) > 2 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 3 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(size_t, unsigned long, (((((((unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(size_t) >= 3 * PyLong_SHIFT)) {
+                                return (size_t) (((((((size_t)digits[2]) << PyLong_SHIFT) | (size_t)digits[1]) << PyLong_SHIFT) | (size_t)digits[0]));
+                            }
                         }
-                    }
-                    break;
-                case 4:
-                    if (8 * sizeof(size_t) > 3 * PyLong_SHIFT) {
-                        if (8 * sizeof(unsigned long) > 4 * PyLong_SHIFT) {
-                            __PYX_VERIFY_RETURN_INT(size_t, unsigned long, (((((((((unsigned long)digits[3]) << PyLong_SHIFT) | (unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
-                        } else if (8 * sizeof(size_t) >= 4 * PyLong_SHIFT) {
-                            return (size_t) (((((((((size_t)digits[3]) << PyLong_SHIFT) | (size_t)digits[2]) << PyLong_SHIFT) | (size_t)digits[1]) << PyLong_SHIFT) | (size_t)digits[0]));
+                        break;
+                    case 4:
+                        if ((8 * sizeof(size_t) > 3 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 4 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(size_t, unsigned long, (((((((((unsigned long)digits[3]) << PyLong_SHIFT) | (unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(size_t) >= 4 * PyLong_SHIFT)) {
+                                return (size_t) (((((((((size_t)digits[3]) << PyLong_SHIFT) | (size_t)digits[2]) << PyLong_SHIFT) | (size_t)digits[1]) << PyLong_SHIFT) | (size_t)digits[0]));
+                            }
                         }
-                    }
-                    break;
+                        break;
+                }
             }
 #endif
 #if CYTHON_COMPILING_IN_CPYTHON && PY_VERSION_HEX < 0x030C00A7
             if (unlikely(Py_SIZE(x) < 0)) {
                 goto raise_neg_overflow;
             }
 #else
@@ -8416,117 +14130,189 @@
                 int result = PyObject_RichCompareBool(x, Py_False, Py_LT);
                 if (unlikely(result < 0))
                     return (size_t) -1;
                 if (unlikely(result == 1))
                     goto raise_neg_overflow;
             }
 #endif
-            if (sizeof(size_t) <= sizeof(unsigned long)) {
+            if ((sizeof(size_t) <= sizeof(unsigned long))) {
                 __PYX_VERIFY_RETURN_INT_EXC(size_t, unsigned long, PyLong_AsUnsignedLong(x))
 #ifdef HAVE_LONG_LONG
-            } else if (sizeof(size_t) <= sizeof(unsigned PY_LONG_LONG)) {
+            } else if ((sizeof(size_t) <= sizeof(unsigned PY_LONG_LONG))) {
                 __PYX_VERIFY_RETURN_INT_EXC(size_t, unsigned PY_LONG_LONG, PyLong_AsUnsignedLongLong(x))
 #endif
             }
         } else {
 #if CYTHON_USE_PYLONG_INTERNALS
-            const digit* digits = ((PyLongObject*)x)->ob_digit;
-            switch (Py_SIZE(x)) {
-                case  0: return (size_t) 0;
-                case -1: __PYX_VERIFY_RETURN_INT(size_t, sdigit, (sdigit) (-(sdigit)digits[0]))
-                case  1: __PYX_VERIFY_RETURN_INT(size_t,  digit, +digits[0])
-                case -2:
-                    if (8 * sizeof(size_t) - 1 > 1 * PyLong_SHIFT) {
-                        if (8 * sizeof(unsigned long) > 2 * PyLong_SHIFT) {
-                            __PYX_VERIFY_RETURN_INT(size_t, long, -(long) (((((unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
-                        } else if (8 * sizeof(size_t) - 1 > 2 * PyLong_SHIFT) {
-                            return (size_t) (((size_t)-1)*(((((size_t)digits[1]) << PyLong_SHIFT) | (size_t)digits[0])));
+            if (__Pyx_PyLong_IsCompact(x)) {
+                __PYX_VERIFY_RETURN_INT(size_t, __Pyx_compact_pylong, __Pyx_PyLong_CompactValue(x))
+            } else {
+                const digit* digits = __Pyx_PyLong_Digits(x);
+                assert(__Pyx_PyLong_DigitCount(x) > 1);
+                switch (__Pyx_PyLong_SignedDigitCount(x)) {
+                    case -2:
+                        if ((8 * sizeof(size_t) - 1 > 1 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 2 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(size_t, long, -(long) (((((unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(size_t) - 1 > 2 * PyLong_SHIFT)) {
+                                return (size_t) (((size_t)-1)*(((((size_t)digits[1]) << PyLong_SHIFT) | (size_t)digits[0])));
+                            }
                         }
-                    }
-                    break;
-                case 2:
-                    if (8 * sizeof(size_t) > 1 * PyLong_SHIFT) {
-                        if (8 * sizeof(unsigned long) > 2 * PyLong_SHIFT) {
-                            __PYX_VERIFY_RETURN_INT(size_t, unsigned long, (((((unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
-                        } else if (8 * sizeof(size_t) - 1 > 2 * PyLong_SHIFT) {
-                            return (size_t) ((((((size_t)digits[1]) << PyLong_SHIFT) | (size_t)digits[0])));
+                        break;
+                    case 2:
+                        if ((8 * sizeof(size_t) > 1 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 2 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(size_t, unsigned long, (((((unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(size_t) - 1 > 2 * PyLong_SHIFT)) {
+                                return (size_t) ((((((size_t)digits[1]) << PyLong_SHIFT) | (size_t)digits[0])));
+                            }
                         }
-                    }
-                    break;
-                case -3:
-                    if (8 * sizeof(size_t) - 1 > 2 * PyLong_SHIFT) {
-                        if (8 * sizeof(unsigned long) > 3 * PyLong_SHIFT) {
-                            __PYX_VERIFY_RETURN_INT(size_t, long, -(long) (((((((unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
-                        } else if (8 * sizeof(size_t) - 1 > 3 * PyLong_SHIFT) {
-                            return (size_t) (((size_t)-1)*(((((((size_t)digits[2]) << PyLong_SHIFT) | (size_t)digits[1]) << PyLong_SHIFT) | (size_t)digits[0])));
+                        break;
+                    case -3:
+                        if ((8 * sizeof(size_t) - 1 > 2 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 3 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(size_t, long, -(long) (((((((unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(size_t) - 1 > 3 * PyLong_SHIFT)) {
+                                return (size_t) (((size_t)-1)*(((((((size_t)digits[2]) << PyLong_SHIFT) | (size_t)digits[1]) << PyLong_SHIFT) | (size_t)digits[0])));
+                            }
                         }
-                    }
-                    break;
-                case 3:
-                    if (8 * sizeof(size_t) > 2 * PyLong_SHIFT) {
-                        if (8 * sizeof(unsigned long) > 3 * PyLong_SHIFT) {
-                            __PYX_VERIFY_RETURN_INT(size_t, unsigned long, (((((((unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
-                        } else if (8 * sizeof(size_t) - 1 > 3 * PyLong_SHIFT) {
-                            return (size_t) ((((((((size_t)digits[2]) << PyLong_SHIFT) | (size_t)digits[1]) << PyLong_SHIFT) | (size_t)digits[0])));
+                        break;
+                    case 3:
+                        if ((8 * sizeof(size_t) > 2 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 3 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(size_t, unsigned long, (((((((unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(size_t) - 1 > 3 * PyLong_SHIFT)) {
+                                return (size_t) ((((((((size_t)digits[2]) << PyLong_SHIFT) | (size_t)digits[1]) << PyLong_SHIFT) | (size_t)digits[0])));
+                            }
                         }
-                    }
-                    break;
-                case -4:
-                    if (8 * sizeof(size_t) - 1 > 3 * PyLong_SHIFT) {
-                        if (8 * sizeof(unsigned long) > 4 * PyLong_SHIFT) {
-                            __PYX_VERIFY_RETURN_INT(size_t, long, -(long) (((((((((unsigned long)digits[3]) << PyLong_SHIFT) | (unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
-                        } else if (8 * sizeof(size_t) - 1 > 4 * PyLong_SHIFT) {
-                            return (size_t) (((size_t)-1)*(((((((((size_t)digits[3]) << PyLong_SHIFT) | (size_t)digits[2]) << PyLong_SHIFT) | (size_t)digits[1]) << PyLong_SHIFT) | (size_t)digits[0])));
+                        break;
+                    case -4:
+                        if ((8 * sizeof(size_t) - 1 > 3 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 4 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(size_t, long, -(long) (((((((((unsigned long)digits[3]) << PyLong_SHIFT) | (unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(size_t) - 1 > 4 * PyLong_SHIFT)) {
+                                return (size_t) (((size_t)-1)*(((((((((size_t)digits[3]) << PyLong_SHIFT) | (size_t)digits[2]) << PyLong_SHIFT) | (size_t)digits[1]) << PyLong_SHIFT) | (size_t)digits[0])));
+                            }
                         }
-                    }
-                    break;
-                case 4:
-                    if (8 * sizeof(size_t) > 3 * PyLong_SHIFT) {
-                        if (8 * sizeof(unsigned long) > 4 * PyLong_SHIFT) {
-                            __PYX_VERIFY_RETURN_INT(size_t, unsigned long, (((((((((unsigned long)digits[3]) << PyLong_SHIFT) | (unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
-                        } else if (8 * sizeof(size_t) - 1 > 4 * PyLong_SHIFT) {
-                            return (size_t) ((((((((((size_t)digits[3]) << PyLong_SHIFT) | (size_t)digits[2]) << PyLong_SHIFT) | (size_t)digits[1]) << PyLong_SHIFT) | (size_t)digits[0])));
+                        break;
+                    case 4:
+                        if ((8 * sizeof(size_t) > 3 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 4 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(size_t, unsigned long, (((((((((unsigned long)digits[3]) << PyLong_SHIFT) | (unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(size_t) - 1 > 4 * PyLong_SHIFT)) {
+                                return (size_t) ((((((((((size_t)digits[3]) << PyLong_SHIFT) | (size_t)digits[2]) << PyLong_SHIFT) | (size_t)digits[1]) << PyLong_SHIFT) | (size_t)digits[0])));
+                            }
                         }
-                    }
-                    break;
+                        break;
+                }
             }
 #endif
-            if (sizeof(size_t) <= sizeof(long)) {
+            if ((sizeof(size_t) <= sizeof(long))) {
                 __PYX_VERIFY_RETURN_INT_EXC(size_t, long, PyLong_AsLong(x))
 #ifdef HAVE_LONG_LONG
-            } else if (sizeof(size_t) <= sizeof(PY_LONG_LONG)) {
+            } else if ((sizeof(size_t) <= sizeof(PY_LONG_LONG))) {
                 __PYX_VERIFY_RETURN_INT_EXC(size_t, PY_LONG_LONG, PyLong_AsLongLong(x))
 #endif
             }
         }
         {
-#if CYTHON_COMPILING_IN_PYPY && !defined(_PyLong_AsByteArray)
-            PyErr_SetString(PyExc_RuntimeError,
-                            "_PyLong_AsByteArray() not available in PyPy, cannot convert large numbers");
-#else
             size_t val;
             PyObject *v = __Pyx_PyNumber_IntOrLong(x);
- #if PY_MAJOR_VERSION < 3
+#if PY_MAJOR_VERSION < 3
             if (likely(v) && !PyLong_Check(v)) {
                 PyObject *tmp = v;
                 v = PyNumber_Long(tmp);
                 Py_DECREF(tmp);
             }
- #endif
+#endif
             if (likely(v)) {
+                int ret = -1;
+#if !(CYTHON_COMPILING_IN_PYPY || CYTHON_COMPILING_IN_LIMITED_API) || defined(_PyLong_AsByteArray)
                 int one = 1; int is_little = (int)*(unsigned char *)&one;
                 unsigned char *bytes = (unsigned char *)&val;
-                int ret = _PyLong_AsByteArray((PyLongObject *)v,
-                                              bytes, sizeof(val),
-                                              is_little, !is_unsigned);
+                ret = _PyLong_AsByteArray((PyLongObject *)v,
+                                           bytes, sizeof(val),
+                                           is_little, !is_unsigned);
+#else
+                PyObject *stepval = NULL, *mask = NULL, *shift = NULL;
+                int bits, remaining_bits, is_negative = 0;
+                long idigit;
+                int chunk_size = (sizeof(long) < 8) ? 30 : 62;
+                if (unlikely(!PyLong_CheckExact(v))) {
+                    PyObject *tmp = v;
+                    v = PyNumber_Long(v);
+                    assert(PyLong_CheckExact(v));
+                    Py_DECREF(tmp);
+                    if (unlikely(!v)) return (size_t) -1;
+                }
+#if CYTHON_COMPILING_IN_LIMITED_API && PY_VERSION_HEX < 0x030B0000
+                if (Py_SIZE(x) == 0)
+                    return (size_t) 0;
+                is_negative = Py_SIZE(x) < 0;
+#else
+                {
+                    int result = PyObject_RichCompareBool(x, Py_False, Py_LT);
+                    if (unlikely(result < 0))
+                        return (size_t) -1;
+                    is_negative = result == 1;
+                }
+#endif
+                if (is_unsigned && unlikely(is_negative)) {
+                    goto raise_neg_overflow;
+                } else if (is_negative) {
+                    stepval = PyNumber_Invert(v);
+                    if (unlikely(!stepval))
+                        return (size_t) -1;
+                } else {
+                    stepval = __Pyx_NewRef(v);
+                }
+                val = (size_t) 0;
+                mask = PyLong_FromLong((1L << chunk_size) - 1); if (unlikely(!mask)) goto done;
+                shift = PyLong_FromLong(chunk_size); if (unlikely(!shift)) goto done;
+                for (bits = 0; bits < (int) sizeof(size_t) * 8 - chunk_size; bits += chunk_size) {
+                    PyObject *tmp, *digit;
+                    digit = PyNumber_And(stepval, mask);
+                    if (unlikely(!digit)) goto done;
+                    idigit = PyLong_AsLong(digit);
+                    Py_DECREF(digit);
+                    if (unlikely(idigit < 0)) goto done;
+                    tmp = PyNumber_Rshift(stepval, shift);
+                    if (unlikely(!tmp)) goto done;
+                    Py_DECREF(stepval); stepval = tmp;
+                    val |= ((size_t) idigit) << bits;
+                    #if CYTHON_COMPILING_IN_LIMITED_API && PY_VERSION_HEX < 0x030B0000
+                    if (Py_SIZE(stepval) == 0)
+                        goto unpacking_done;
+                    #endif
+                }
+                idigit = PyLong_AsLong(stepval);
+                if (unlikely(idigit < 0)) goto done;
+                remaining_bits = ((int) sizeof(size_t) * 8) - bits - (is_unsigned ? 0 : 1);
+                if (unlikely(idigit >= (1L << remaining_bits)))
+                    goto raise_overflow;
+                val |= ((size_t) idigit) << bits;
+            #if CYTHON_COMPILING_IN_LIMITED_API && PY_VERSION_HEX < 0x030B0000
+            unpacking_done:
+            #endif
+                if (!is_unsigned) {
+                    if (unlikely(val & (((size_t) 1) << (sizeof(size_t) * 8 - 1))))
+                        goto raise_overflow;
+                    if (is_negative)
+                        val = ~val;
+                }
+                ret = 0;
+            done:
+                Py_XDECREF(shift);
+                Py_XDECREF(mask);
+                Py_XDECREF(stepval);
+#endif
                 Py_DECREF(v);
                 if (likely(!ret))
                     return val;
             }
-#endif
             return (size_t) -1;
         }
     } else {
         size_t val;
         PyObject *tmp = __Pyx_PyNumber_IntOrLong(x);
         if (!tmp) return (size_t) -1;
         val = __Pyx_PyInt_As_size_t(tmp);
@@ -8539,14 +14325,302 @@
     return (size_t) -1;
 raise_neg_overflow:
     PyErr_SetString(PyExc_OverflowError,
         "can't convert negative value to size_t");
     return (size_t) -1;
 }
 
+/* CIntFromPy */
+static CYTHON_INLINE bool __Pyx_PyInt_As_bool(PyObject *x) {
+#ifdef __Pyx_HAS_GCC_DIAGNOSTIC
+#pragma GCC diagnostic push
+#pragma GCC diagnostic ignored "-Wconversion"
+#endif
+    const bool neg_one = (bool) -1, const_zero = (bool) 0;
+#ifdef __Pyx_HAS_GCC_DIAGNOSTIC
+#pragma GCC diagnostic pop
+#endif
+    const int is_unsigned = neg_one > const_zero;
+#if PY_MAJOR_VERSION < 3
+    if (likely(PyInt_Check(x))) {
+        if ((sizeof(bool) < sizeof(long))) {
+            __PYX_VERIFY_RETURN_INT(bool, long, PyInt_AS_LONG(x))
+        } else {
+            long val = PyInt_AS_LONG(x);
+            if (is_unsigned && unlikely(val < 0)) {
+                goto raise_neg_overflow;
+            }
+            return (bool) val;
+        }
+    } else
+#endif
+    if (likely(PyLong_Check(x))) {
+        if (is_unsigned) {
+#if CYTHON_USE_PYLONG_INTERNALS
+            if (unlikely(__Pyx_PyLong_IsNeg(x))) {
+                goto raise_neg_overflow;
+            } else if (__Pyx_PyLong_IsCompact(x)) {
+                __PYX_VERIFY_RETURN_INT(bool, __Pyx_compact_upylong, __Pyx_PyLong_CompactValueUnsigned(x))
+            } else {
+                const digit* digits = __Pyx_PyLong_Digits(x);
+                assert(__Pyx_PyLong_DigitCount(x) > 1);
+                switch (__Pyx_PyLong_DigitCount(x)) {
+                    case 2:
+                        if ((8 * sizeof(bool) > 1 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 2 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(bool, unsigned long, (((((unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(bool) >= 2 * PyLong_SHIFT)) {
+                                return (bool) (((((bool)digits[1]) << PyLong_SHIFT) | (bool)digits[0]));
+                            }
+                        }
+                        break;
+                    case 3:
+                        if ((8 * sizeof(bool) > 2 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 3 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(bool, unsigned long, (((((((unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(bool) >= 3 * PyLong_SHIFT)) {
+                                return (bool) (((((((bool)digits[2]) << PyLong_SHIFT) | (bool)digits[1]) << PyLong_SHIFT) | (bool)digits[0]));
+                            }
+                        }
+                        break;
+                    case 4:
+                        if ((8 * sizeof(bool) > 3 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 4 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(bool, unsigned long, (((((((((unsigned long)digits[3]) << PyLong_SHIFT) | (unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(bool) >= 4 * PyLong_SHIFT)) {
+                                return (bool) (((((((((bool)digits[3]) << PyLong_SHIFT) | (bool)digits[2]) << PyLong_SHIFT) | (bool)digits[1]) << PyLong_SHIFT) | (bool)digits[0]));
+                            }
+                        }
+                        break;
+                }
+            }
+#endif
+#if CYTHON_COMPILING_IN_CPYTHON && PY_VERSION_HEX < 0x030C00A7
+            if (unlikely(Py_SIZE(x) < 0)) {
+                goto raise_neg_overflow;
+            }
+#else
+            {
+                int result = PyObject_RichCompareBool(x, Py_False, Py_LT);
+                if (unlikely(result < 0))
+                    return (bool) -1;
+                if (unlikely(result == 1))
+                    goto raise_neg_overflow;
+            }
+#endif
+            if ((sizeof(bool) <= sizeof(unsigned long))) {
+                __PYX_VERIFY_RETURN_INT_EXC(bool, unsigned long, PyLong_AsUnsignedLong(x))
+#ifdef HAVE_LONG_LONG
+            } else if ((sizeof(bool) <= sizeof(unsigned PY_LONG_LONG))) {
+                __PYX_VERIFY_RETURN_INT_EXC(bool, unsigned PY_LONG_LONG, PyLong_AsUnsignedLongLong(x))
+#endif
+            }
+        } else {
+#if CYTHON_USE_PYLONG_INTERNALS
+            if (__Pyx_PyLong_IsCompact(x)) {
+                __PYX_VERIFY_RETURN_INT(bool, __Pyx_compact_pylong, __Pyx_PyLong_CompactValue(x))
+            } else {
+                const digit* digits = __Pyx_PyLong_Digits(x);
+                assert(__Pyx_PyLong_DigitCount(x) > 1);
+                switch (__Pyx_PyLong_SignedDigitCount(x)) {
+                    case -2:
+                        if ((8 * sizeof(bool) - 1 > 1 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 2 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(bool, long, -(long) (((((unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(bool) - 1 > 2 * PyLong_SHIFT)) {
+                                return (bool) (((bool)-1)*(((((bool)digits[1]) << PyLong_SHIFT) | (bool)digits[0])));
+                            }
+                        }
+                        break;
+                    case 2:
+                        if ((8 * sizeof(bool) > 1 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 2 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(bool, unsigned long, (((((unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(bool) - 1 > 2 * PyLong_SHIFT)) {
+                                return (bool) ((((((bool)digits[1]) << PyLong_SHIFT) | (bool)digits[0])));
+                            }
+                        }
+                        break;
+                    case -3:
+                        if ((8 * sizeof(bool) - 1 > 2 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 3 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(bool, long, -(long) (((((((unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(bool) - 1 > 3 * PyLong_SHIFT)) {
+                                return (bool) (((bool)-1)*(((((((bool)digits[2]) << PyLong_SHIFT) | (bool)digits[1]) << PyLong_SHIFT) | (bool)digits[0])));
+                            }
+                        }
+                        break;
+                    case 3:
+                        if ((8 * sizeof(bool) > 2 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 3 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(bool, unsigned long, (((((((unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(bool) - 1 > 3 * PyLong_SHIFT)) {
+                                return (bool) ((((((((bool)digits[2]) << PyLong_SHIFT) | (bool)digits[1]) << PyLong_SHIFT) | (bool)digits[0])));
+                            }
+                        }
+                        break;
+                    case -4:
+                        if ((8 * sizeof(bool) - 1 > 3 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 4 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(bool, long, -(long) (((((((((unsigned long)digits[3]) << PyLong_SHIFT) | (unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(bool) - 1 > 4 * PyLong_SHIFT)) {
+                                return (bool) (((bool)-1)*(((((((((bool)digits[3]) << PyLong_SHIFT) | (bool)digits[2]) << PyLong_SHIFT) | (bool)digits[1]) << PyLong_SHIFT) | (bool)digits[0])));
+                            }
+                        }
+                        break;
+                    case 4:
+                        if ((8 * sizeof(bool) > 3 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 4 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(bool, unsigned long, (((((((((unsigned long)digits[3]) << PyLong_SHIFT) | (unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(bool) - 1 > 4 * PyLong_SHIFT)) {
+                                return (bool) ((((((((((bool)digits[3]) << PyLong_SHIFT) | (bool)digits[2]) << PyLong_SHIFT) | (bool)digits[1]) << PyLong_SHIFT) | (bool)digits[0])));
+                            }
+                        }
+                        break;
+                }
+            }
+#endif
+            if ((sizeof(bool) <= sizeof(long))) {
+                __PYX_VERIFY_RETURN_INT_EXC(bool, long, PyLong_AsLong(x))
+#ifdef HAVE_LONG_LONG
+            } else if ((sizeof(bool) <= sizeof(PY_LONG_LONG))) {
+                __PYX_VERIFY_RETURN_INT_EXC(bool, PY_LONG_LONG, PyLong_AsLongLong(x))
+#endif
+            }
+        }
+        {
+            bool val;
+            PyObject *v = __Pyx_PyNumber_IntOrLong(x);
+#if PY_MAJOR_VERSION < 3
+            if (likely(v) && !PyLong_Check(v)) {
+                PyObject *tmp = v;
+                v = PyNumber_Long(tmp);
+                Py_DECREF(tmp);
+            }
+#endif
+            if (likely(v)) {
+                int ret = -1;
+#if !(CYTHON_COMPILING_IN_PYPY || CYTHON_COMPILING_IN_LIMITED_API) || defined(_PyLong_AsByteArray)
+                int one = 1; int is_little = (int)*(unsigned char *)&one;
+                unsigned char *bytes = (unsigned char *)&val;
+                ret = _PyLong_AsByteArray((PyLongObject *)v,
+                                           bytes, sizeof(val),
+                                           is_little, !is_unsigned);
+#else
+                PyObject *stepval = NULL, *mask = NULL, *shift = NULL;
+                int bits, remaining_bits, is_negative = 0;
+                long idigit;
+                int chunk_size = (sizeof(long) < 8) ? 30 : 62;
+                if (unlikely(!PyLong_CheckExact(v))) {
+                    PyObject *tmp = v;
+                    v = PyNumber_Long(v);
+                    assert(PyLong_CheckExact(v));
+                    Py_DECREF(tmp);
+                    if (unlikely(!v)) return (bool) -1;
+                }
+#if CYTHON_COMPILING_IN_LIMITED_API && PY_VERSION_HEX < 0x030B0000
+                if (Py_SIZE(x) == 0)
+                    return (bool) 0;
+                is_negative = Py_SIZE(x) < 0;
+#else
+                {
+                    int result = PyObject_RichCompareBool(x, Py_False, Py_LT);
+                    if (unlikely(result < 0))
+                        return (bool) -1;
+                    is_negative = result == 1;
+                }
+#endif
+                if (is_unsigned && unlikely(is_negative)) {
+                    goto raise_neg_overflow;
+                } else if (is_negative) {
+                    stepval = PyNumber_Invert(v);
+                    if (unlikely(!stepval))
+                        return (bool) -1;
+                } else {
+                    stepval = __Pyx_NewRef(v);
+                }
+                val = (bool) 0;
+                mask = PyLong_FromLong((1L << chunk_size) - 1); if (unlikely(!mask)) goto done;
+                shift = PyLong_FromLong(chunk_size); if (unlikely(!shift)) goto done;
+                for (bits = 0; bits < (int) sizeof(bool) * 8 - chunk_size; bits += chunk_size) {
+                    PyObject *tmp, *digit;
+                    digit = PyNumber_And(stepval, mask);
+                    if (unlikely(!digit)) goto done;
+                    idigit = PyLong_AsLong(digit);
+                    Py_DECREF(digit);
+                    if (unlikely(idigit < 0)) goto done;
+                    tmp = PyNumber_Rshift(stepval, shift);
+                    if (unlikely(!tmp)) goto done;
+                    Py_DECREF(stepval); stepval = tmp;
+                    val |= ((bool) idigit) << bits;
+                    #if CYTHON_COMPILING_IN_LIMITED_API && PY_VERSION_HEX < 0x030B0000
+                    if (Py_SIZE(stepval) == 0)
+                        goto unpacking_done;
+                    #endif
+                }
+                idigit = PyLong_AsLong(stepval);
+                if (unlikely(idigit < 0)) goto done;
+                remaining_bits = ((int) sizeof(bool) * 8) - bits - (is_unsigned ? 0 : 1);
+                if (unlikely(idigit >= (1L << remaining_bits)))
+                    goto raise_overflow;
+                val |= ((bool) idigit) << bits;
+            #if CYTHON_COMPILING_IN_LIMITED_API && PY_VERSION_HEX < 0x030B0000
+            unpacking_done:
+            #endif
+                if (!is_unsigned) {
+                    if (unlikely(val & (((bool) 1) << (sizeof(bool) * 8 - 1))))
+                        goto raise_overflow;
+                    if (is_negative)
+                        val = ~val;
+                }
+                ret = 0;
+            done:
+                Py_XDECREF(shift);
+                Py_XDECREF(mask);
+                Py_XDECREF(stepval);
+#endif
+                Py_DECREF(v);
+                if (likely(!ret))
+                    return val;
+            }
+            return (bool) -1;
+        }
+    } else {
+        bool val;
+        PyObject *tmp = __Pyx_PyNumber_IntOrLong(x);
+        if (!tmp) return (bool) -1;
+        val = __Pyx_PyInt_As_bool(tmp);
+        Py_DECREF(tmp);
+        return val;
+    }
+raise_overflow:
+    PyErr_SetString(PyExc_OverflowError,
+        "value too large to convert to bool");
+    return (bool) -1;
+raise_neg_overflow:
+    PyErr_SetString(PyExc_OverflowError,
+        "can't convert negative value to bool");
+    return (bool) -1;
+}
+
+/* FormatTypeName */
+#if CYTHON_COMPILING_IN_LIMITED_API
+static __Pyx_TypeName
+__Pyx_PyType_GetName(PyTypeObject* tp)
+{
+    PyObject *name = __Pyx_PyObject_GetAttrStr((PyObject *)tp,
+                                               __pyx_n_s_name);
+    if (unlikely(name == NULL) || unlikely(!PyUnicode_Check(name))) {
+        PyErr_Clear();
+        Py_XSETREF(name, __Pyx_NewRef(__pyx_n_s__44));
+    }
+    return name;
+}
+#endif
+
 /* CIntToPy */
 static CYTHON_INLINE PyObject* __Pyx_PyInt_From_long(long value) {
 #ifdef __Pyx_HAS_GCC_DIAGNOSTIC
 #pragma GCC diagnostic push
 #pragma GCC diagnostic ignored "-Wconversion"
 #endif
     const long neg_one = (long) -1, const_zero = (long) 0;
@@ -8590,59 +14664,64 @@
     const long neg_one = (long) -1, const_zero = (long) 0;
 #ifdef __Pyx_HAS_GCC_DIAGNOSTIC
 #pragma GCC diagnostic pop
 #endif
     const int is_unsigned = neg_one > const_zero;
 #if PY_MAJOR_VERSION < 3
     if (likely(PyInt_Check(x))) {
-        if (sizeof(long) < sizeof(long)) {
+        if ((sizeof(long) < sizeof(long))) {
             __PYX_VERIFY_RETURN_INT(long, long, PyInt_AS_LONG(x))
         } else {
             long val = PyInt_AS_LONG(x);
             if (is_unsigned && unlikely(val < 0)) {
                 goto raise_neg_overflow;
             }
             return (long) val;
         }
     } else
 #endif
     if (likely(PyLong_Check(x))) {
         if (is_unsigned) {
 #if CYTHON_USE_PYLONG_INTERNALS
-            const digit* digits = ((PyLongObject*)x)->ob_digit;
-            switch (Py_SIZE(x)) {
-                case  0: return (long) 0;
-                case  1: __PYX_VERIFY_RETURN_INT(long, digit, digits[0])
-                case 2:
-                    if (8 * sizeof(long) > 1 * PyLong_SHIFT) {
-                        if (8 * sizeof(unsigned long) > 2 * PyLong_SHIFT) {
-                            __PYX_VERIFY_RETURN_INT(long, unsigned long, (((((unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
-                        } else if (8 * sizeof(long) >= 2 * PyLong_SHIFT) {
-                            return (long) (((((long)digits[1]) << PyLong_SHIFT) | (long)digits[0]));
+            if (unlikely(__Pyx_PyLong_IsNeg(x))) {
+                goto raise_neg_overflow;
+            } else if (__Pyx_PyLong_IsCompact(x)) {
+                __PYX_VERIFY_RETURN_INT(long, __Pyx_compact_upylong, __Pyx_PyLong_CompactValueUnsigned(x))
+            } else {
+                const digit* digits = __Pyx_PyLong_Digits(x);
+                assert(__Pyx_PyLong_DigitCount(x) > 1);
+                switch (__Pyx_PyLong_DigitCount(x)) {
+                    case 2:
+                        if ((8 * sizeof(long) > 1 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 2 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(long, unsigned long, (((((unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(long) >= 2 * PyLong_SHIFT)) {
+                                return (long) (((((long)digits[1]) << PyLong_SHIFT) | (long)digits[0]));
+                            }
                         }
-                    }
-                    break;
-                case 3:
-                    if (8 * sizeof(long) > 2 * PyLong_SHIFT) {
-                        if (8 * sizeof(unsigned long) > 3 * PyLong_SHIFT) {
-                            __PYX_VERIFY_RETURN_INT(long, unsigned long, (((((((unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
-                        } else if (8 * sizeof(long) >= 3 * PyLong_SHIFT) {
-                            return (long) (((((((long)digits[2]) << PyLong_SHIFT) | (long)digits[1]) << PyLong_SHIFT) | (long)digits[0]));
+                        break;
+                    case 3:
+                        if ((8 * sizeof(long) > 2 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 3 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(long, unsigned long, (((((((unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(long) >= 3 * PyLong_SHIFT)) {
+                                return (long) (((((((long)digits[2]) << PyLong_SHIFT) | (long)digits[1]) << PyLong_SHIFT) | (long)digits[0]));
+                            }
                         }
-                    }
-                    break;
-                case 4:
-                    if (8 * sizeof(long) > 3 * PyLong_SHIFT) {
-                        if (8 * sizeof(unsigned long) > 4 * PyLong_SHIFT) {
-                            __PYX_VERIFY_RETURN_INT(long, unsigned long, (((((((((unsigned long)digits[3]) << PyLong_SHIFT) | (unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
-                        } else if (8 * sizeof(long) >= 4 * PyLong_SHIFT) {
-                            return (long) (((((((((long)digits[3]) << PyLong_SHIFT) | (long)digits[2]) << PyLong_SHIFT) | (long)digits[1]) << PyLong_SHIFT) | (long)digits[0]));
+                        break;
+                    case 4:
+                        if ((8 * sizeof(long) > 3 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 4 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(long, unsigned long, (((((((((unsigned long)digits[3]) << PyLong_SHIFT) | (unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(long) >= 4 * PyLong_SHIFT)) {
+                                return (long) (((((((((long)digits[3]) << PyLong_SHIFT) | (long)digits[2]) << PyLong_SHIFT) | (long)digits[1]) << PyLong_SHIFT) | (long)digits[0]));
+                            }
                         }
-                    }
-                    break;
+                        break;
+                }
             }
 #endif
 #if CYTHON_COMPILING_IN_CPYTHON && PY_VERSION_HEX < 0x030C00A7
             if (unlikely(Py_SIZE(x) < 0)) {
                 goto raise_neg_overflow;
             }
 #else
@@ -8650,117 +14729,189 @@
                 int result = PyObject_RichCompareBool(x, Py_False, Py_LT);
                 if (unlikely(result < 0))
                     return (long) -1;
                 if (unlikely(result == 1))
                     goto raise_neg_overflow;
             }
 #endif
-            if (sizeof(long) <= sizeof(unsigned long)) {
+            if ((sizeof(long) <= sizeof(unsigned long))) {
                 __PYX_VERIFY_RETURN_INT_EXC(long, unsigned long, PyLong_AsUnsignedLong(x))
 #ifdef HAVE_LONG_LONG
-            } else if (sizeof(long) <= sizeof(unsigned PY_LONG_LONG)) {
+            } else if ((sizeof(long) <= sizeof(unsigned PY_LONG_LONG))) {
                 __PYX_VERIFY_RETURN_INT_EXC(long, unsigned PY_LONG_LONG, PyLong_AsUnsignedLongLong(x))
 #endif
             }
         } else {
 #if CYTHON_USE_PYLONG_INTERNALS
-            const digit* digits = ((PyLongObject*)x)->ob_digit;
-            switch (Py_SIZE(x)) {
-                case  0: return (long) 0;
-                case -1: __PYX_VERIFY_RETURN_INT(long, sdigit, (sdigit) (-(sdigit)digits[0]))
-                case  1: __PYX_VERIFY_RETURN_INT(long,  digit, +digits[0])
-                case -2:
-                    if (8 * sizeof(long) - 1 > 1 * PyLong_SHIFT) {
-                        if (8 * sizeof(unsigned long) > 2 * PyLong_SHIFT) {
-                            __PYX_VERIFY_RETURN_INT(long, long, -(long) (((((unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
-                        } else if (8 * sizeof(long) - 1 > 2 * PyLong_SHIFT) {
-                            return (long) (((long)-1)*(((((long)digits[1]) << PyLong_SHIFT) | (long)digits[0])));
+            if (__Pyx_PyLong_IsCompact(x)) {
+                __PYX_VERIFY_RETURN_INT(long, __Pyx_compact_pylong, __Pyx_PyLong_CompactValue(x))
+            } else {
+                const digit* digits = __Pyx_PyLong_Digits(x);
+                assert(__Pyx_PyLong_DigitCount(x) > 1);
+                switch (__Pyx_PyLong_SignedDigitCount(x)) {
+                    case -2:
+                        if ((8 * sizeof(long) - 1 > 1 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 2 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(long, long, -(long) (((((unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(long) - 1 > 2 * PyLong_SHIFT)) {
+                                return (long) (((long)-1)*(((((long)digits[1]) << PyLong_SHIFT) | (long)digits[0])));
+                            }
                         }
-                    }
-                    break;
-                case 2:
-                    if (8 * sizeof(long) > 1 * PyLong_SHIFT) {
-                        if (8 * sizeof(unsigned long) > 2 * PyLong_SHIFT) {
-                            __PYX_VERIFY_RETURN_INT(long, unsigned long, (((((unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
-                        } else if (8 * sizeof(long) - 1 > 2 * PyLong_SHIFT) {
-                            return (long) ((((((long)digits[1]) << PyLong_SHIFT) | (long)digits[0])));
+                        break;
+                    case 2:
+                        if ((8 * sizeof(long) > 1 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 2 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(long, unsigned long, (((((unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(long) - 1 > 2 * PyLong_SHIFT)) {
+                                return (long) ((((((long)digits[1]) << PyLong_SHIFT) | (long)digits[0])));
+                            }
                         }
-                    }
-                    break;
-                case -3:
-                    if (8 * sizeof(long) - 1 > 2 * PyLong_SHIFT) {
-                        if (8 * sizeof(unsigned long) > 3 * PyLong_SHIFT) {
-                            __PYX_VERIFY_RETURN_INT(long, long, -(long) (((((((unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
-                        } else if (8 * sizeof(long) - 1 > 3 * PyLong_SHIFT) {
-                            return (long) (((long)-1)*(((((((long)digits[2]) << PyLong_SHIFT) | (long)digits[1]) << PyLong_SHIFT) | (long)digits[0])));
+                        break;
+                    case -3:
+                        if ((8 * sizeof(long) - 1 > 2 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 3 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(long, long, -(long) (((((((unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(long) - 1 > 3 * PyLong_SHIFT)) {
+                                return (long) (((long)-1)*(((((((long)digits[2]) << PyLong_SHIFT) | (long)digits[1]) << PyLong_SHIFT) | (long)digits[0])));
+                            }
                         }
-                    }
-                    break;
-                case 3:
-                    if (8 * sizeof(long) > 2 * PyLong_SHIFT) {
-                        if (8 * sizeof(unsigned long) > 3 * PyLong_SHIFT) {
-                            __PYX_VERIFY_RETURN_INT(long, unsigned long, (((((((unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
-                        } else if (8 * sizeof(long) - 1 > 3 * PyLong_SHIFT) {
-                            return (long) ((((((((long)digits[2]) << PyLong_SHIFT) | (long)digits[1]) << PyLong_SHIFT) | (long)digits[0])));
+                        break;
+                    case 3:
+                        if ((8 * sizeof(long) > 2 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 3 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(long, unsigned long, (((((((unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(long) - 1 > 3 * PyLong_SHIFT)) {
+                                return (long) ((((((((long)digits[2]) << PyLong_SHIFT) | (long)digits[1]) << PyLong_SHIFT) | (long)digits[0])));
+                            }
                         }
-                    }
-                    break;
-                case -4:
-                    if (8 * sizeof(long) - 1 > 3 * PyLong_SHIFT) {
-                        if (8 * sizeof(unsigned long) > 4 * PyLong_SHIFT) {
-                            __PYX_VERIFY_RETURN_INT(long, long, -(long) (((((((((unsigned long)digits[3]) << PyLong_SHIFT) | (unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
-                        } else if (8 * sizeof(long) - 1 > 4 * PyLong_SHIFT) {
-                            return (long) (((long)-1)*(((((((((long)digits[3]) << PyLong_SHIFT) | (long)digits[2]) << PyLong_SHIFT) | (long)digits[1]) << PyLong_SHIFT) | (long)digits[0])));
+                        break;
+                    case -4:
+                        if ((8 * sizeof(long) - 1 > 3 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 4 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(long, long, -(long) (((((((((unsigned long)digits[3]) << PyLong_SHIFT) | (unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(long) - 1 > 4 * PyLong_SHIFT)) {
+                                return (long) (((long)-1)*(((((((((long)digits[3]) << PyLong_SHIFT) | (long)digits[2]) << PyLong_SHIFT) | (long)digits[1]) << PyLong_SHIFT) | (long)digits[0])));
+                            }
                         }
-                    }
-                    break;
-                case 4:
-                    if (8 * sizeof(long) > 3 * PyLong_SHIFT) {
-                        if (8 * sizeof(unsigned long) > 4 * PyLong_SHIFT) {
-                            __PYX_VERIFY_RETURN_INT(long, unsigned long, (((((((((unsigned long)digits[3]) << PyLong_SHIFT) | (unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
-                        } else if (8 * sizeof(long) - 1 > 4 * PyLong_SHIFT) {
-                            return (long) ((((((((((long)digits[3]) << PyLong_SHIFT) | (long)digits[2]) << PyLong_SHIFT) | (long)digits[1]) << PyLong_SHIFT) | (long)digits[0])));
+                        break;
+                    case 4:
+                        if ((8 * sizeof(long) > 3 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 4 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(long, unsigned long, (((((((((unsigned long)digits[3]) << PyLong_SHIFT) | (unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(long) - 1 > 4 * PyLong_SHIFT)) {
+                                return (long) ((((((((((long)digits[3]) << PyLong_SHIFT) | (long)digits[2]) << PyLong_SHIFT) | (long)digits[1]) << PyLong_SHIFT) | (long)digits[0])));
+                            }
                         }
-                    }
-                    break;
+                        break;
+                }
             }
 #endif
-            if (sizeof(long) <= sizeof(long)) {
+            if ((sizeof(long) <= sizeof(long))) {
                 __PYX_VERIFY_RETURN_INT_EXC(long, long, PyLong_AsLong(x))
 #ifdef HAVE_LONG_LONG
-            } else if (sizeof(long) <= sizeof(PY_LONG_LONG)) {
+            } else if ((sizeof(long) <= sizeof(PY_LONG_LONG))) {
                 __PYX_VERIFY_RETURN_INT_EXC(long, PY_LONG_LONG, PyLong_AsLongLong(x))
 #endif
             }
         }
         {
-#if CYTHON_COMPILING_IN_PYPY && !defined(_PyLong_AsByteArray)
-            PyErr_SetString(PyExc_RuntimeError,
-                            "_PyLong_AsByteArray() not available in PyPy, cannot convert large numbers");
-#else
             long val;
             PyObject *v = __Pyx_PyNumber_IntOrLong(x);
- #if PY_MAJOR_VERSION < 3
+#if PY_MAJOR_VERSION < 3
             if (likely(v) && !PyLong_Check(v)) {
                 PyObject *tmp = v;
                 v = PyNumber_Long(tmp);
                 Py_DECREF(tmp);
             }
- #endif
+#endif
             if (likely(v)) {
+                int ret = -1;
+#if !(CYTHON_COMPILING_IN_PYPY || CYTHON_COMPILING_IN_LIMITED_API) || defined(_PyLong_AsByteArray)
                 int one = 1; int is_little = (int)*(unsigned char *)&one;
                 unsigned char *bytes = (unsigned char *)&val;
-                int ret = _PyLong_AsByteArray((PyLongObject *)v,
-                                              bytes, sizeof(val),
-                                              is_little, !is_unsigned);
+                ret = _PyLong_AsByteArray((PyLongObject *)v,
+                                           bytes, sizeof(val),
+                                           is_little, !is_unsigned);
+#else
+                PyObject *stepval = NULL, *mask = NULL, *shift = NULL;
+                int bits, remaining_bits, is_negative = 0;
+                long idigit;
+                int chunk_size = (sizeof(long) < 8) ? 30 : 62;
+                if (unlikely(!PyLong_CheckExact(v))) {
+                    PyObject *tmp = v;
+                    v = PyNumber_Long(v);
+                    assert(PyLong_CheckExact(v));
+                    Py_DECREF(tmp);
+                    if (unlikely(!v)) return (long) -1;
+                }
+#if CYTHON_COMPILING_IN_LIMITED_API && PY_VERSION_HEX < 0x030B0000
+                if (Py_SIZE(x) == 0)
+                    return (long) 0;
+                is_negative = Py_SIZE(x) < 0;
+#else
+                {
+                    int result = PyObject_RichCompareBool(x, Py_False, Py_LT);
+                    if (unlikely(result < 0))
+                        return (long) -1;
+                    is_negative = result == 1;
+                }
+#endif
+                if (is_unsigned && unlikely(is_negative)) {
+                    goto raise_neg_overflow;
+                } else if (is_negative) {
+                    stepval = PyNumber_Invert(v);
+                    if (unlikely(!stepval))
+                        return (long) -1;
+                } else {
+                    stepval = __Pyx_NewRef(v);
+                }
+                val = (long) 0;
+                mask = PyLong_FromLong((1L << chunk_size) - 1); if (unlikely(!mask)) goto done;
+                shift = PyLong_FromLong(chunk_size); if (unlikely(!shift)) goto done;
+                for (bits = 0; bits < (int) sizeof(long) * 8 - chunk_size; bits += chunk_size) {
+                    PyObject *tmp, *digit;
+                    digit = PyNumber_And(stepval, mask);
+                    if (unlikely(!digit)) goto done;
+                    idigit = PyLong_AsLong(digit);
+                    Py_DECREF(digit);
+                    if (unlikely(idigit < 0)) goto done;
+                    tmp = PyNumber_Rshift(stepval, shift);
+                    if (unlikely(!tmp)) goto done;
+                    Py_DECREF(stepval); stepval = tmp;
+                    val |= ((long) idigit) << bits;
+                    #if CYTHON_COMPILING_IN_LIMITED_API && PY_VERSION_HEX < 0x030B0000
+                    if (Py_SIZE(stepval) == 0)
+                        goto unpacking_done;
+                    #endif
+                }
+                idigit = PyLong_AsLong(stepval);
+                if (unlikely(idigit < 0)) goto done;
+                remaining_bits = ((int) sizeof(long) * 8) - bits - (is_unsigned ? 0 : 1);
+                if (unlikely(idigit >= (1L << remaining_bits)))
+                    goto raise_overflow;
+                val |= ((long) idigit) << bits;
+            #if CYTHON_COMPILING_IN_LIMITED_API && PY_VERSION_HEX < 0x030B0000
+            unpacking_done:
+            #endif
+                if (!is_unsigned) {
+                    if (unlikely(val & (((long) 1) << (sizeof(long) * 8 - 1))))
+                        goto raise_overflow;
+                    if (is_negative)
+                        val = ~val;
+                }
+                ret = 0;
+            done:
+                Py_XDECREF(shift);
+                Py_XDECREF(mask);
+                Py_XDECREF(stepval);
+#endif
                 Py_DECREF(v);
                 if (likely(!ret))
                     return val;
             }
-#endif
             return (long) -1;
         }
     } else {
         long val;
         PyObject *tmp = __Pyx_PyNumber_IntOrLong(x);
         if (!tmp) return (long) -1;
         val = __Pyx_PyInt_As_long(tmp);
@@ -8786,59 +14937,64 @@
     const int neg_one = (int) -1, const_zero = (int) 0;
 #ifdef __Pyx_HAS_GCC_DIAGNOSTIC
 #pragma GCC diagnostic pop
 #endif
     const int is_unsigned = neg_one > const_zero;
 #if PY_MAJOR_VERSION < 3
     if (likely(PyInt_Check(x))) {
-        if (sizeof(int) < sizeof(long)) {
+        if ((sizeof(int) < sizeof(long))) {
             __PYX_VERIFY_RETURN_INT(int, long, PyInt_AS_LONG(x))
         } else {
             long val = PyInt_AS_LONG(x);
             if (is_unsigned && unlikely(val < 0)) {
                 goto raise_neg_overflow;
             }
             return (int) val;
         }
     } else
 #endif
     if (likely(PyLong_Check(x))) {
         if (is_unsigned) {
 #if CYTHON_USE_PYLONG_INTERNALS
-            const digit* digits = ((PyLongObject*)x)->ob_digit;
-            switch (Py_SIZE(x)) {
-                case  0: return (int) 0;
-                case  1: __PYX_VERIFY_RETURN_INT(int, digit, digits[0])
-                case 2:
-                    if (8 * sizeof(int) > 1 * PyLong_SHIFT) {
-                        if (8 * sizeof(unsigned long) > 2 * PyLong_SHIFT) {
-                            __PYX_VERIFY_RETURN_INT(int, unsigned long, (((((unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
-                        } else if (8 * sizeof(int) >= 2 * PyLong_SHIFT) {
-                            return (int) (((((int)digits[1]) << PyLong_SHIFT) | (int)digits[0]));
+            if (unlikely(__Pyx_PyLong_IsNeg(x))) {
+                goto raise_neg_overflow;
+            } else if (__Pyx_PyLong_IsCompact(x)) {
+                __PYX_VERIFY_RETURN_INT(int, __Pyx_compact_upylong, __Pyx_PyLong_CompactValueUnsigned(x))
+            } else {
+                const digit* digits = __Pyx_PyLong_Digits(x);
+                assert(__Pyx_PyLong_DigitCount(x) > 1);
+                switch (__Pyx_PyLong_DigitCount(x)) {
+                    case 2:
+                        if ((8 * sizeof(int) > 1 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 2 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(int, unsigned long, (((((unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(int) >= 2 * PyLong_SHIFT)) {
+                                return (int) (((((int)digits[1]) << PyLong_SHIFT) | (int)digits[0]));
+                            }
                         }
-                    }
-                    break;
-                case 3:
-                    if (8 * sizeof(int) > 2 * PyLong_SHIFT) {
-                        if (8 * sizeof(unsigned long) > 3 * PyLong_SHIFT) {
-                            __PYX_VERIFY_RETURN_INT(int, unsigned long, (((((((unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
-                        } else if (8 * sizeof(int) >= 3 * PyLong_SHIFT) {
-                            return (int) (((((((int)digits[2]) << PyLong_SHIFT) | (int)digits[1]) << PyLong_SHIFT) | (int)digits[0]));
+                        break;
+                    case 3:
+                        if ((8 * sizeof(int) > 2 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 3 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(int, unsigned long, (((((((unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(int) >= 3 * PyLong_SHIFT)) {
+                                return (int) (((((((int)digits[2]) << PyLong_SHIFT) | (int)digits[1]) << PyLong_SHIFT) | (int)digits[0]));
+                            }
                         }
-                    }
-                    break;
-                case 4:
-                    if (8 * sizeof(int) > 3 * PyLong_SHIFT) {
-                        if (8 * sizeof(unsigned long) > 4 * PyLong_SHIFT) {
-                            __PYX_VERIFY_RETURN_INT(int, unsigned long, (((((((((unsigned long)digits[3]) << PyLong_SHIFT) | (unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
-                        } else if (8 * sizeof(int) >= 4 * PyLong_SHIFT) {
-                            return (int) (((((((((int)digits[3]) << PyLong_SHIFT) | (int)digits[2]) << PyLong_SHIFT) | (int)digits[1]) << PyLong_SHIFT) | (int)digits[0]));
+                        break;
+                    case 4:
+                        if ((8 * sizeof(int) > 3 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 4 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(int, unsigned long, (((((((((unsigned long)digits[3]) << PyLong_SHIFT) | (unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(int) >= 4 * PyLong_SHIFT)) {
+                                return (int) (((((((((int)digits[3]) << PyLong_SHIFT) | (int)digits[2]) << PyLong_SHIFT) | (int)digits[1]) << PyLong_SHIFT) | (int)digits[0]));
+                            }
                         }
-                    }
-                    break;
+                        break;
+                }
             }
 #endif
 #if CYTHON_COMPILING_IN_CPYTHON && PY_VERSION_HEX < 0x030C00A7
             if (unlikely(Py_SIZE(x) < 0)) {
                 goto raise_neg_overflow;
             }
 #else
@@ -8846,117 +15002,189 @@
                 int result = PyObject_RichCompareBool(x, Py_False, Py_LT);
                 if (unlikely(result < 0))
                     return (int) -1;
                 if (unlikely(result == 1))
                     goto raise_neg_overflow;
             }
 #endif
-            if (sizeof(int) <= sizeof(unsigned long)) {
+            if ((sizeof(int) <= sizeof(unsigned long))) {
                 __PYX_VERIFY_RETURN_INT_EXC(int, unsigned long, PyLong_AsUnsignedLong(x))
 #ifdef HAVE_LONG_LONG
-            } else if (sizeof(int) <= sizeof(unsigned PY_LONG_LONG)) {
+            } else if ((sizeof(int) <= sizeof(unsigned PY_LONG_LONG))) {
                 __PYX_VERIFY_RETURN_INT_EXC(int, unsigned PY_LONG_LONG, PyLong_AsUnsignedLongLong(x))
 #endif
             }
         } else {
 #if CYTHON_USE_PYLONG_INTERNALS
-            const digit* digits = ((PyLongObject*)x)->ob_digit;
-            switch (Py_SIZE(x)) {
-                case  0: return (int) 0;
-                case -1: __PYX_VERIFY_RETURN_INT(int, sdigit, (sdigit) (-(sdigit)digits[0]))
-                case  1: __PYX_VERIFY_RETURN_INT(int,  digit, +digits[0])
-                case -2:
-                    if (8 * sizeof(int) - 1 > 1 * PyLong_SHIFT) {
-                        if (8 * sizeof(unsigned long) > 2 * PyLong_SHIFT) {
-                            __PYX_VERIFY_RETURN_INT(int, long, -(long) (((((unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
-                        } else if (8 * sizeof(int) - 1 > 2 * PyLong_SHIFT) {
-                            return (int) (((int)-1)*(((((int)digits[1]) << PyLong_SHIFT) | (int)digits[0])));
+            if (__Pyx_PyLong_IsCompact(x)) {
+                __PYX_VERIFY_RETURN_INT(int, __Pyx_compact_pylong, __Pyx_PyLong_CompactValue(x))
+            } else {
+                const digit* digits = __Pyx_PyLong_Digits(x);
+                assert(__Pyx_PyLong_DigitCount(x) > 1);
+                switch (__Pyx_PyLong_SignedDigitCount(x)) {
+                    case -2:
+                        if ((8 * sizeof(int) - 1 > 1 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 2 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(int, long, -(long) (((((unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(int) - 1 > 2 * PyLong_SHIFT)) {
+                                return (int) (((int)-1)*(((((int)digits[1]) << PyLong_SHIFT) | (int)digits[0])));
+                            }
                         }
-                    }
-                    break;
-                case 2:
-                    if (8 * sizeof(int) > 1 * PyLong_SHIFT) {
-                        if (8 * sizeof(unsigned long) > 2 * PyLong_SHIFT) {
-                            __PYX_VERIFY_RETURN_INT(int, unsigned long, (((((unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
-                        } else if (8 * sizeof(int) - 1 > 2 * PyLong_SHIFT) {
-                            return (int) ((((((int)digits[1]) << PyLong_SHIFT) | (int)digits[0])));
+                        break;
+                    case 2:
+                        if ((8 * sizeof(int) > 1 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 2 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(int, unsigned long, (((((unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(int) - 1 > 2 * PyLong_SHIFT)) {
+                                return (int) ((((((int)digits[1]) << PyLong_SHIFT) | (int)digits[0])));
+                            }
                         }
-                    }
-                    break;
-                case -3:
-                    if (8 * sizeof(int) - 1 > 2 * PyLong_SHIFT) {
-                        if (8 * sizeof(unsigned long) > 3 * PyLong_SHIFT) {
-                            __PYX_VERIFY_RETURN_INT(int, long, -(long) (((((((unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
-                        } else if (8 * sizeof(int) - 1 > 3 * PyLong_SHIFT) {
-                            return (int) (((int)-1)*(((((((int)digits[2]) << PyLong_SHIFT) | (int)digits[1]) << PyLong_SHIFT) | (int)digits[0])));
+                        break;
+                    case -3:
+                        if ((8 * sizeof(int) - 1 > 2 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 3 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(int, long, -(long) (((((((unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(int) - 1 > 3 * PyLong_SHIFT)) {
+                                return (int) (((int)-1)*(((((((int)digits[2]) << PyLong_SHIFT) | (int)digits[1]) << PyLong_SHIFT) | (int)digits[0])));
+                            }
                         }
-                    }
-                    break;
-                case 3:
-                    if (8 * sizeof(int) > 2 * PyLong_SHIFT) {
-                        if (8 * sizeof(unsigned long) > 3 * PyLong_SHIFT) {
-                            __PYX_VERIFY_RETURN_INT(int, unsigned long, (((((((unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
-                        } else if (8 * sizeof(int) - 1 > 3 * PyLong_SHIFT) {
-                            return (int) ((((((((int)digits[2]) << PyLong_SHIFT) | (int)digits[1]) << PyLong_SHIFT) | (int)digits[0])));
+                        break;
+                    case 3:
+                        if ((8 * sizeof(int) > 2 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 3 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(int, unsigned long, (((((((unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(int) - 1 > 3 * PyLong_SHIFT)) {
+                                return (int) ((((((((int)digits[2]) << PyLong_SHIFT) | (int)digits[1]) << PyLong_SHIFT) | (int)digits[0])));
+                            }
                         }
-                    }
-                    break;
-                case -4:
-                    if (8 * sizeof(int) - 1 > 3 * PyLong_SHIFT) {
-                        if (8 * sizeof(unsigned long) > 4 * PyLong_SHIFT) {
-                            __PYX_VERIFY_RETURN_INT(int, long, -(long) (((((((((unsigned long)digits[3]) << PyLong_SHIFT) | (unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
-                        } else if (8 * sizeof(int) - 1 > 4 * PyLong_SHIFT) {
-                            return (int) (((int)-1)*(((((((((int)digits[3]) << PyLong_SHIFT) | (int)digits[2]) << PyLong_SHIFT) | (int)digits[1]) << PyLong_SHIFT) | (int)digits[0])));
+                        break;
+                    case -4:
+                        if ((8 * sizeof(int) - 1 > 3 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 4 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(int, long, -(long) (((((((((unsigned long)digits[3]) << PyLong_SHIFT) | (unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(int) - 1 > 4 * PyLong_SHIFT)) {
+                                return (int) (((int)-1)*(((((((((int)digits[3]) << PyLong_SHIFT) | (int)digits[2]) << PyLong_SHIFT) | (int)digits[1]) << PyLong_SHIFT) | (int)digits[0])));
+                            }
                         }
-                    }
-                    break;
-                case 4:
-                    if (8 * sizeof(int) > 3 * PyLong_SHIFT) {
-                        if (8 * sizeof(unsigned long) > 4 * PyLong_SHIFT) {
-                            __PYX_VERIFY_RETURN_INT(int, unsigned long, (((((((((unsigned long)digits[3]) << PyLong_SHIFT) | (unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
-                        } else if (8 * sizeof(int) - 1 > 4 * PyLong_SHIFT) {
-                            return (int) ((((((((((int)digits[3]) << PyLong_SHIFT) | (int)digits[2]) << PyLong_SHIFT) | (int)digits[1]) << PyLong_SHIFT) | (int)digits[0])));
+                        break;
+                    case 4:
+                        if ((8 * sizeof(int) > 3 * PyLong_SHIFT)) {
+                            if ((8 * sizeof(unsigned long) > 4 * PyLong_SHIFT)) {
+                                __PYX_VERIFY_RETURN_INT(int, unsigned long, (((((((((unsigned long)digits[3]) << PyLong_SHIFT) | (unsigned long)digits[2]) << PyLong_SHIFT) | (unsigned long)digits[1]) << PyLong_SHIFT) | (unsigned long)digits[0])))
+                            } else if ((8 * sizeof(int) - 1 > 4 * PyLong_SHIFT)) {
+                                return (int) ((((((((((int)digits[3]) << PyLong_SHIFT) | (int)digits[2]) << PyLong_SHIFT) | (int)digits[1]) << PyLong_SHIFT) | (int)digits[0])));
+                            }
                         }
-                    }
-                    break;
+                        break;
+                }
             }
 #endif
-            if (sizeof(int) <= sizeof(long)) {
+            if ((sizeof(int) <= sizeof(long))) {
                 __PYX_VERIFY_RETURN_INT_EXC(int, long, PyLong_AsLong(x))
 #ifdef HAVE_LONG_LONG
-            } else if (sizeof(int) <= sizeof(PY_LONG_LONG)) {
+            } else if ((sizeof(int) <= sizeof(PY_LONG_LONG))) {
                 __PYX_VERIFY_RETURN_INT_EXC(int, PY_LONG_LONG, PyLong_AsLongLong(x))
 #endif
             }
         }
         {
-#if CYTHON_COMPILING_IN_PYPY && !defined(_PyLong_AsByteArray)
-            PyErr_SetString(PyExc_RuntimeError,
-                            "_PyLong_AsByteArray() not available in PyPy, cannot convert large numbers");
-#else
             int val;
             PyObject *v = __Pyx_PyNumber_IntOrLong(x);
- #if PY_MAJOR_VERSION < 3
+#if PY_MAJOR_VERSION < 3
             if (likely(v) && !PyLong_Check(v)) {
                 PyObject *tmp = v;
                 v = PyNumber_Long(tmp);
                 Py_DECREF(tmp);
             }
- #endif
+#endif
             if (likely(v)) {
+                int ret = -1;
+#if !(CYTHON_COMPILING_IN_PYPY || CYTHON_COMPILING_IN_LIMITED_API) || defined(_PyLong_AsByteArray)
                 int one = 1; int is_little = (int)*(unsigned char *)&one;
                 unsigned char *bytes = (unsigned char *)&val;
-                int ret = _PyLong_AsByteArray((PyLongObject *)v,
-                                              bytes, sizeof(val),
-                                              is_little, !is_unsigned);
+                ret = _PyLong_AsByteArray((PyLongObject *)v,
+                                           bytes, sizeof(val),
+                                           is_little, !is_unsigned);
+#else
+                PyObject *stepval = NULL, *mask = NULL, *shift = NULL;
+                int bits, remaining_bits, is_negative = 0;
+                long idigit;
+                int chunk_size = (sizeof(long) < 8) ? 30 : 62;
+                if (unlikely(!PyLong_CheckExact(v))) {
+                    PyObject *tmp = v;
+                    v = PyNumber_Long(v);
+                    assert(PyLong_CheckExact(v));
+                    Py_DECREF(tmp);
+                    if (unlikely(!v)) return (int) -1;
+                }
+#if CYTHON_COMPILING_IN_LIMITED_API && PY_VERSION_HEX < 0x030B0000
+                if (Py_SIZE(x) == 0)
+                    return (int) 0;
+                is_negative = Py_SIZE(x) < 0;
+#else
+                {
+                    int result = PyObject_RichCompareBool(x, Py_False, Py_LT);
+                    if (unlikely(result < 0))
+                        return (int) -1;
+                    is_negative = result == 1;
+                }
+#endif
+                if (is_unsigned && unlikely(is_negative)) {
+                    goto raise_neg_overflow;
+                } else if (is_negative) {
+                    stepval = PyNumber_Invert(v);
+                    if (unlikely(!stepval))
+                        return (int) -1;
+                } else {
+                    stepval = __Pyx_NewRef(v);
+                }
+                val = (int) 0;
+                mask = PyLong_FromLong((1L << chunk_size) - 1); if (unlikely(!mask)) goto done;
+                shift = PyLong_FromLong(chunk_size); if (unlikely(!shift)) goto done;
+                for (bits = 0; bits < (int) sizeof(int) * 8 - chunk_size; bits += chunk_size) {
+                    PyObject *tmp, *digit;
+                    digit = PyNumber_And(stepval, mask);
+                    if (unlikely(!digit)) goto done;
+                    idigit = PyLong_AsLong(digit);
+                    Py_DECREF(digit);
+                    if (unlikely(idigit < 0)) goto done;
+                    tmp = PyNumber_Rshift(stepval, shift);
+                    if (unlikely(!tmp)) goto done;
+                    Py_DECREF(stepval); stepval = tmp;
+                    val |= ((int) idigit) << bits;
+                    #if CYTHON_COMPILING_IN_LIMITED_API && PY_VERSION_HEX < 0x030B0000
+                    if (Py_SIZE(stepval) == 0)
+                        goto unpacking_done;
+                    #endif
+                }
+                idigit = PyLong_AsLong(stepval);
+                if (unlikely(idigit < 0)) goto done;
+                remaining_bits = ((int) sizeof(int) * 8) - bits - (is_unsigned ? 0 : 1);
+                if (unlikely(idigit >= (1L << remaining_bits)))
+                    goto raise_overflow;
+                val |= ((int) idigit) << bits;
+            #if CYTHON_COMPILING_IN_LIMITED_API && PY_VERSION_HEX < 0x030B0000
+            unpacking_done:
+            #endif
+                if (!is_unsigned) {
+                    if (unlikely(val & (((int) 1) << (sizeof(int) * 8 - 1))))
+                        goto raise_overflow;
+                    if (is_negative)
+                        val = ~val;
+                }
+                ret = 0;
+            done:
+                Py_XDECREF(shift);
+                Py_XDECREF(mask);
+                Py_XDECREF(stepval);
+#endif
                 Py_DECREF(v);
                 if (likely(!ret))
                     return val;
             }
-#endif
             return (int) -1;
         }
     } else {
         int val;
         PyObject *tmp = __Pyx_PyNumber_IntOrLong(x);
         if (!tmp) return (int) -1;
         val = __Pyx_PyInt_As_int(tmp);
@@ -8973,15 +15201,15 @@
     return (int) -1;
 }
 
 /* FastTypeChecks */
 #if CYTHON_COMPILING_IN_CPYTHON
 static int __Pyx_InBases(PyTypeObject *a, PyTypeObject *b) {
     while (a) {
-        a = a->tp_base;
+        a = __Pyx_PyType_GetSlot(a, tp_base, PyTypeObject*);
         if (a == b)
             return 1;
     }
     return b == &PyBaseObject_Type;
 }
 static CYTHON_INLINE int __Pyx_IsSubtype(PyTypeObject *a, PyTypeObject *b) {
     PyObject *mro;
@@ -8994,14 +15222,30 @@
             if (PyTuple_GET_ITEM(mro, i) == (PyObject *)b)
                 return 1;
         }
         return 0;
     }
     return __Pyx_InBases(a, b);
 }
+static CYTHON_INLINE int __Pyx_IsAnySubtype2(PyTypeObject *cls, PyTypeObject *a, PyTypeObject *b) {
+    PyObject *mro;
+    if (cls == a || cls == b) return 1;
+    mro = cls->tp_mro;
+    if (likely(mro)) {
+        Py_ssize_t i, n;
+        n = PyTuple_GET_SIZE(mro);
+        for (i = 0; i < n; i++) {
+            PyObject *base = PyTuple_GET_ITEM(mro, i);
+            if (base == (PyObject *)a || base == (PyObject *)b)
+                return 1;
+        }
+        return 0;
+    }
+    return __Pyx_InBases(cls, a) || __Pyx_InBases(cls, b);
+}
 #if PY_MAJOR_VERSION == 2
 static int __Pyx_inner_PyErr_GivenExceptionMatches2(PyObject *err, PyObject* exc_type1, PyObject* exc_type2) {
     PyObject *exception, *value, *tb;
     int res;
     __Pyx_PyThreadState_declare
     __Pyx_PyThreadState_assign
     __Pyx_ErrFetch(&exception, &value, &tb);
@@ -9018,19 +15262,19 @@
         }
     }
     __Pyx_ErrRestore(exception, value, tb);
     return res;
 }
 #else
 static CYTHON_INLINE int __Pyx_inner_PyErr_GivenExceptionMatches2(PyObject *err, PyObject* exc_type1, PyObject *exc_type2) {
-    int res = exc_type1 ? __Pyx_IsSubtype((PyTypeObject*)err, (PyTypeObject*)exc_type1) : 0;
-    if (!res) {
-        res = __Pyx_IsSubtype((PyTypeObject*)err, (PyTypeObject*)exc_type2);
+    if (exc_type1) {
+        return __Pyx_IsAnySubtype2((PyTypeObject*)err, (PyTypeObject*)exc_type1, (PyTypeObject*)exc_type2);
+    } else {
+        return __Pyx_IsSubtype((PyTypeObject*)err, (PyTypeObject*)exc_type2);
     }
-    return res;
 }
 #endif
 static int __Pyx_PyErr_GivenExceptionMatchesTuple(PyObject *exc_type, PyObject *tuple) {
     Py_ssize_t i, n;
     assert(PyExceptionClass_Check(exc_type));
     n = PyTuple_GET_SIZE(tuple);
 #if PY_MAJOR_VERSION >= 3
@@ -9099,50 +15343,60 @@
                 found_dot = 1;
             } else if (rt_from_call[i] < '0' || rt_from_call[i] > '9') {
                 break;
             }
             rtversion[i] = rt_from_call[i];
         }
         PyOS_snprintf(message, sizeof(message),
-                      "compiletime version %s of module '%.100s' "
+                      "compile time version %s of module '%.100s' "
                       "does not match runtime version %s",
                       ctversion, __Pyx_MODULE_NAME, rtversion);
         return PyErr_WarnEx(NULL, message, 1);
     }
     return 0;
 }
 
 /* InitStrings */
+#if PY_MAJOR_VERSION >= 3
+static int __Pyx_InitString(__Pyx_StringTabEntry t, PyObject **str) {
+    if (t.is_unicode | t.is_str) {
+        if (t.intern) {
+            *str = PyUnicode_InternFromString(t.s);
+        } else if (t.encoding) {
+            *str = PyUnicode_Decode(t.s, t.n - 1, t.encoding, NULL);
+        } else {
+            *str = PyUnicode_FromStringAndSize(t.s, t.n - 1);
+        }
+    } else {
+        *str = PyBytes_FromStringAndSize(t.s, t.n - 1);
+    }
+    if (!*str)
+        return -1;
+    if (PyObject_Hash(*str) == -1)
+        return -1;
+    return 0;
+}
+#endif
 static int __Pyx_InitStrings(__Pyx_StringTabEntry *t) {
     while (t->p) {
-        #if PY_MAJOR_VERSION < 3
+        #if PY_MAJOR_VERSION >= 3
+        __Pyx_InitString(*t, t->p);
+        #else
         if (t->is_unicode) {
             *t->p = PyUnicode_DecodeUTF8(t->s, t->n - 1, NULL);
         } else if (t->intern) {
             *t->p = PyString_InternFromString(t->s);
         } else {
             *t->p = PyString_FromStringAndSize(t->s, t->n - 1);
         }
-        #else
-        if (t->is_unicode | t->is_str) {
-            if (t->intern) {
-                *t->p = PyUnicode_InternFromString(t->s);
-            } else if (t->encoding) {
-                *t->p = PyUnicode_Decode(t->s, t->n - 1, t->encoding, NULL);
-            } else {
-                *t->p = PyUnicode_FromStringAndSize(t->s, t->n - 1);
-            }
-        } else {
-            *t->p = PyBytes_FromStringAndSize(t->s, t->n - 1);
-        }
-        #endif
         if (!*t->p)
             return -1;
         if (PyObject_Hash(*t->p) == -1)
             return -1;
+        #endif
         ++t;
     }
     return 0;
 }
 
 static CYTHON_INLINE PyObject* __Pyx_PyUnicode_FromString(const char* c_str) {
     return __Pyx_PyUnicode_FromStringAndSize(c_str, (Py_ssize_t)strlen(c_str));
@@ -9196,15 +15450,15 @@
 #if PY_MAJOR_VERSION < 3 && __PYX_DEFAULT_STRING_ENCODING_IS_ASCII
             __Pyx_sys_getdefaultencoding_not_ascii &&
 #endif
             PyUnicode_Check(o)) {
         return __Pyx_PyUnicode_AsStringAndSize(o, length);
     } else
 #endif
-#if (!CYTHON_COMPILING_IN_PYPY) || (defined(PyByteArray_AS_STRING) && defined(PyByteArray_GET_SIZE))
+#if (!CYTHON_COMPILING_IN_PYPY && !CYTHON_COMPILING_IN_LIMITED_API) || (defined(PyByteArray_AS_STRING) && defined(PyByteArray_GET_SIZE))
     if (PyByteArray_Check(o)) {
         *length = PyByteArray_GET_SIZE(o);
         return PyByteArray_AS_STRING(o);
     } else
 #endif
     {
         char* result;
@@ -9225,30 +15479,34 @@
     int retval;
     if (unlikely(!x)) return -1;
     retval = __Pyx_PyObject_IsTrue(x);
     Py_DECREF(x);
     return retval;
 }
 static PyObject* __Pyx_PyNumber_IntOrLongWrongResultType(PyObject* result, const char* type_name) {
+    __Pyx_TypeName result_type_name = __Pyx_PyType_GetName(Py_TYPE(result));
 #if PY_MAJOR_VERSION >= 3
     if (PyLong_Check(result)) {
         if (PyErr_WarnFormat(PyExc_DeprecationWarning, 1,
-                "__int__ returned non-int (type %.200s).  "
-                "The ability to return an instance of a strict subclass of int "
-                "is deprecated, and may be removed in a future version of Python.",
-                Py_TYPE(result)->tp_name)) {
+                "__int__ returned non-int (type " __Pyx_FMT_TYPENAME ").  "
+                "The ability to return an instance of a strict subclass of int is deprecated, "
+                "and may be removed in a future version of Python.",
+                result_type_name)) {
+            __Pyx_DECREF_TypeName(result_type_name);
             Py_DECREF(result);
             return NULL;
         }
+        __Pyx_DECREF_TypeName(result_type_name);
         return result;
     }
 #endif
     PyErr_Format(PyExc_TypeError,
-                 "__%.4s__ returned non-%.4s (type %.200s)",
-                 type_name, type_name, Py_TYPE(result)->tp_name);
+                 "__%.4s__ returned non-%.4s (type " __Pyx_FMT_TYPENAME ")",
+                 type_name, type_name, result_type_name);
+    __Pyx_DECREF_TypeName(result_type_name);
     Py_DECREF(result);
     return NULL;
 }
 static CYTHON_INLINE PyObject* __Pyx_PyNumber_IntOrLong(PyObject* x) {
 #if CYTHON_USE_TYPE_SLOTS
   PyNumberMethods *m;
 #endif
@@ -9306,21 +15564,19 @@
         return PyInt_AS_LONG(b);
     else
         return PyInt_AsSsize_t(b);
   }
 #endif
   if (likely(PyLong_CheckExact(b))) {
     #if CYTHON_USE_PYLONG_INTERNALS
-    const digit* digits = ((PyLongObject*)b)->ob_digit;
-    const Py_ssize_t size = Py_SIZE(b);
-    if (likely(__Pyx_sst_abs(size) <= 1)) {
-        ival = likely(size) ? digits[0] : 0;
-        if (size == -1) ival = -ival;
-        return ival;
+    if (likely(__Pyx_PyLong_IsCompact(b))) {
+        return __Pyx_PyLong_CompactValue(b);
     } else {
+      const digit* digits = __Pyx_PyLong_Digits(b);
+      const Py_ssize_t size = __Pyx_PyLong_SignedDigitCount(b);
       switch (size) {
          case 2:
            if (8 * sizeof(Py_ssize_t) > 2 * PyLong_SHIFT) {
              return (Py_ssize_t) (((((size_t)digits[1]) << PyLong_SHIFT) | (size_t)digits[0]));
            }
            break;
          case -2:
@@ -9380,8 +15636,16 @@
   return b ? __Pyx_NewRef(Py_True) : __Pyx_NewRef(Py_False);
 }
 static CYTHON_INLINE PyObject * __Pyx_PyInt_FromSize_t(size_t ival) {
     return PyInt_FromSize_t(ival);
 }
 
 
+/* #### Code section: utility_code_pragmas_end ### */
+#ifdef _MSC_VER
+#pragma warning( pop )
+#endif
+
+
+
+/* #### Code section: end ### */
 #endif /* Py_PYTHON_H */
```

### Comparing `pybitset-0.0.1rc1/pybitset/backends/cython/_bitset.pyx` & `pybitset-0.0.1rc2/pybitset/backends/cython/_bitset.pyx`

 * *Files 0% similar despite different names*

```diff
@@ -9,18 +9,18 @@
     bitset_inplace_difference, bitset_inplace_intersection,
     bitset_inplace_symmetric_difference, bitset_inplace_union,
     bitset_intersection_count, bitset_iterator, bitset_maximum, bitset_minimum,
     bitset_next_set_bit, bitset_next_set_bits, bitset_print, bitset_resize,
     bitset_set, bitset_set_to_value, bitset_shift_left, bitset_shift_right,
     bitset_size_in_bits, bitset_size_in_bytes, bitset_size_in_words,
     bitset_symmetric_difference_count, bitset_t, bitset_trim,
-    bitset_union_count, bitsets_disjoint, bitsets_intersect)
+    bitset_union_count, bitsets_disjoint, bitsets_intersect, bool)
 
 
-cdef bint bitset_iterator_func(size_t value, void *param) with gil:
+cdef bool bitset_iterator_func(size_t value, void *param) noexcept with gil:
     return (<object>param)(value)
 
 @cython.freelist(8)
 @cython.final
 @cython.no_gc
 cdef class BitSet:
     cdef bitset_t * _bitset
```

### Comparing `pybitset-0.0.1rc1/pybitset/backends/cython/bitset.pxd` & `pybitset-0.0.1rc2/pybitset/backends/cython/bitset.pxd`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 # cython: language_level=3
 # cython: cdivision=True
 
 
 cdef extern from "bitset.h" nogil:
     ctypedef struct bitset_t
-
+    ctypedef int bool
     bitset_t* bitset_create()
     bitset_t *bitset_create_with_capacity( size_t size )
     void bitset_free(bitset_t *bitset)
     void bitset_clear(bitset_t *bitset)
     void bitset_fill(bitset_t *bitset)
     bitset_t * bitset_copy(const bitset_t *bitset)
     bint bitset_resize(bitset_t *bitset, size_t newarraysize, bint padwithzeroes)
@@ -43,10 +43,10 @@
     bint bitset_inplace_symmetric_difference(bitset_t * b1, const bitset_t * b2)
 
 # compute the size of the symmetric difference  */
     size_t  bitset_symmetric_difference_count(const bitset_t * b1, const bitset_t * b2)
     bint bitset_next_set_bit(const bitset_t *bitset, size_t *i)
     size_t bitset_next_set_bits(const bitset_t *bitset, size_t *buffer, size_t capacity, size_t * startfrom)
 
-    ctypedef bint(*bitset_iterator)(size_t value, void *param);
+    ctypedef bool (*bitset_iterator)(size_t value, void *param) with gil
     bint bitset_for_each(const bitset_t *b, bitset_iterator iterator, void *ptr)
     void bitset_print(const bitset_t *b)
```

### Comparing `pybitset-0.0.1rc1/pybitset.egg-info/PKG-INFO` & `pybitset-0.0.1rc2/pybitset.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pybitset
-Version: 0.0.1rc1
+Version: 0.0.1rc2
 Summary: python binding for cbitset
 Home-page: https://github.com/synodriver/pybitset
 Author: synodriver
 Author-email: diguohuangjiajinweijun@gmail.com
 License: BSD
 Keywords: bitset
 Classifier: Development Status :: 3 - Alpha
```

### Comparing `pybitset-0.0.1rc1/pybitset.egg-info/SOURCES.txt` & `pybitset-0.0.1rc2/pybitset.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `pybitset-0.0.1rc1/setup.py` & `pybitset-0.0.1rc2/setup.py`

 * *Files identical despite different names*

