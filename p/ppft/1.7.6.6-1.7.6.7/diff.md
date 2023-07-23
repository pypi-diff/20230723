# Comparing `tmp/ppft-1.7.6.6.tar.gz` & `tmp/ppft-1.7.6.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ppft-1.7.6.6.tar", last modified: Sun Oct 23 23:15:29 2022, max compression
+gzip compressed data, was "ppft-1.7.6.7.tar", last modified: Sun Jul 23 11:00:12 2023, max compression
```

## Comparing `ppft-1.7.6.6.tar` & `ppft-1.7.6.7.tar`

### file list

```diff
@@ -1,68 +1,71 @@
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-23 23:15:29.573302 ppft-1.7.6.6/
--rw-r--r--   0 mmckerns   (501) staff       (20)      830 2022-05-16 23:08:33.000000 ppft-1.7.6.6/.codecov.yml
--rw-r--r--   0 mmckerns   (501) staff       (20)      680 2022-07-02 19:57:31.000000 ppft-1.7.6.6/.coveragerc
--rw-r--r--   0 mmckerns   (501) staff       (20)       32 2022-05-09 23:49:56.000000 ppft-1.7.6.6/.gitignore
--rw-r--r--   0 mmckerns   (501) staff       (20)      285 2022-05-16 23:08:33.000000 ppft-1.7.6.6/.readthedocs.yml
--rw-r--r--   0 mmckerns   (501) staff       (20)     1007 2022-07-02 19:11:02.000000 ppft-1.7.6.6/.travis.yml
--rw-r--r--   0 mmckerns   (501) staff       (20)     3824 2022-05-09 23:49:56.000000 ppft-1.7.6.6/CHANGELOG
--rw-r--r--   0 mmckerns   (501) staff       (20)     1580 2022-05-09 23:49:56.000000 ppft-1.7.6.6/COPYING
--rw-r--r--   0 mmckerns   (501) staff       (20)     1904 2022-05-16 23:08:33.000000 ppft-1.7.6.6/LICENSE
--rw-r--r--   0 mmckerns   (501) staff       (20)      295 2022-07-06 22:43:22.000000 ppft-1.7.6.6/MANIFEST.in
--rw-r--r--   0 mmckerns   (501) staff       (20)     6808 2022-10-23 23:15:29.573539 ppft-1.7.6.6/PKG-INFO
--rw-r--r--   0 mmckerns   (501) staff       (20)     6403 2022-10-23 22:56:13.000000 ppft-1.7.6.6/README.md
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-23 23:15:29.539529 ppft-1.7.6.6/docs/
--rw-r--r--   0 mmckerns   (501) staff       (20)      668 2022-05-16 23:08:33.000000 ppft-1.7.6.6/docs/Makefile
--rw-r--r--   0 mmckerns   (501) staff       (20)      430 2022-05-17 16:01:57.000000 ppft-1.7.6.6/docs/requirements.txt
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-23 23:15:29.546165 ppft-1.7.6.6/docs/source/
--rw-r--r--   0 mmckerns   (501) staff       (20)     7325 2022-07-06 22:43:55.000000 ppft-1.7.6.6/docs/source/conf.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      381 2022-05-16 23:08:33.000000 ppft-1.7.6.6/docs/source/index.rst
--rw-r--r--   0 mmckerns   (501) staff       (20)    78646 2022-05-16 23:08:33.000000 ppft-1.7.6.6/docs/source/pathos.png
--rw-r--r--   0 mmckerns   (501) staff       (20)     1076 2022-05-16 23:08:33.000000 ppft-1.7.6.6/docs/source/ppft.rst
--rw-r--r--   0 mmckerns   (501) staff       (20)      260 2022-05-16 23:08:33.000000 ppft-1.7.6.6/docs/source/scripts.rst
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-23 23:15:29.551286 ppft-1.7.6.6/pp/
--rw-r--r--   0 mmckerns   (501) staff       (20)      172 2022-06-16 17:05:17.000000 ppft-1.7.6.6/pp/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      624 2022-05-16 23:08:33.000000 ppft-1.7.6.6/pp/__main__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      487 2022-05-16 23:08:33.000000 ppft-1.7.6.6/pp/_pp.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      410 2022-05-16 23:08:33.000000 ppft-1.7.6.6/pp/auto.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      414 2022-05-16 23:08:33.000000 ppft-1.7.6.6/pp/common.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-23 23:15:29.552502 ppft-1.7.6.6/pp/server/
--rw-r--r--   0 mmckerns   (501) staff       (20)       58 2022-05-16 23:08:33.000000 ppft-1.7.6.6/pp/server/__init__.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)      782 2022-05-19 23:49:35.000000 ppft-1.7.6.6/pp/server/__main__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      420 2022-05-16 23:08:33.000000 ppft-1.7.6.6/pp/transport.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      620 2022-05-16 23:08:33.000000 ppft-1.7.6.6/pp/worker.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-23 23:15:29.558548 ppft-1.7.6.6/ppft/
--rw-r--r--   0 mmckerns   (501) staff       (20)     7736 2022-10-23 23:15:29.000000 ppft-1.7.6.6/ppft/__info__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1518 2022-07-06 23:10:10.000000 ppft-1.7.6.6/ppft/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5040 2022-06-28 22:09:12.000000 ppft-1.7.6.6/ppft/__main__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    33466 2022-06-28 22:09:31.000000 ppft-1.7.6.6/ppft/_pp.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5121 2022-05-16 23:08:33.000000 ppft-1.7.6.6/ppft/auto.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     5273 2022-07-06 23:04:34.000000 ppft-1.7.6.6/ppft/common.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-23 23:15:29.563622 ppft-1.7.6.6/ppft/server/
--rw-r--r--   0 mmckerns   (501) staff       (20)      214 2022-05-16 23:08:33.000000 ppft-1.7.6.6/ppft/server/__init__.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    15170 2022-06-28 22:18:30.000000 ppft-1.7.6.6/ppft/server/__main__.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-23 23:15:29.571727 ppft-1.7.6.6/ppft/tests/
--rw-r--r--   0 mmckerns   (501) staff       (20)      501 2022-05-09 23:52:22.000000 ppft-1.7.6.6/ppft/tests/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      965 2022-07-09 11:06:04.000000 ppft-1.7.6.6/ppft/tests/__main__.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     3628 2022-05-16 23:08:33.000000 ppft-1.7.6.6/ppft/tests/auto_diff.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2549 2022-06-28 22:04:22.000000 ppft-1.7.6.6/ppft/tests/callback.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1946 2022-05-16 23:08:33.000000 ppft-1.7.6.6/ppft/tests/dynamic_ncpus.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     1709 2022-06-28 22:04:22.000000 ppft-1.7.6.6/ppft/tests/quicksort.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2729 2022-05-09 23:52:22.000000 ppft-1.7.6.6/ppft/tests/reverse_md5.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2604 2022-05-16 23:08:33.000000 ppft-1.7.6.6/ppft/tests/sum_primes.py
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     2724 2022-05-16 23:08:33.000000 ppft-1.7.6.6/ppft/tests/sum_primes_functor.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     9428 2022-06-28 22:11:35.000000 ppft-1.7.6.6/ppft/transport.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      624 2022-05-16 23:08:33.000000 ppft-1.7.6.6/ppft/worker.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-23 23:15:29.562131 ppft-1.7.6.6/ppft.egg-info/
--rw-r--r--   0 mmckerns   (501) staff       (20)     6808 2022-10-23 23:15:29.000000 ppft-1.7.6.6/ppft.egg-info/PKG-INFO
--rw-r--r--   0 mmckerns   (501) staff       (20)     1032 2022-10-23 23:15:29.000000 ppft-1.7.6.6/ppft.egg-info/SOURCES.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)        1 2022-10-23 23:15:29.000000 ppft-1.7.6.6/ppft.egg-info/dependency_links.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)        1 2022-10-23 23:15:29.000000 ppft-1.7.6.6/ppft.egg-info/not-zip-safe
--rw-r--r--   0 mmckerns   (501) staff       (20)       20 2022-10-23 23:15:29.000000 ppft-1.7.6.6/ppft.egg-info/requires.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)        8 2022-10-23 23:15:29.000000 ppft-1.7.6.6/ppft.egg-info/top_level.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)      166 2022-05-20 09:49:14.000000 ppft-1.7.6.6/pyproject.toml
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-23 23:15:29.572632 ppft-1.7.6.6/scripts/
--rwxr-xr-x   0 mmckerns   (501) staff       (20)    15170 2022-06-28 22:19:15.000000 ppft-1.7.6.6/scripts/ppserver
--rw-r--r--   0 mmckerns   (501) staff       (20)       62 2022-10-23 23:15:29.574652 ppft-1.7.6.6/setup.cfg
--rwxr-xr-x   0 mmckerns   (501) staff       (20)     4024 2022-10-23 22:55:40.000000 ppft-1.7.6.6/setup.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      445 2022-07-09 11:05:38.000000 ppft-1.7.6.6/tox.ini
--rw-r--r--   0 mmckerns   (501) staff       (20)     2733 2022-10-23 23:14:48.000000 ppft-1.7.6.6/version.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 11:00:12.422447 ppft-1.7.6.7/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      830 2022-05-16 23:08:33.000000 ppft-1.7.6.7/.codecov.yml
+-rw-r--r--   0 mmckerns   (501) staff       (20)      680 2022-07-02 19:57:31.000000 ppft-1.7.6.7/.coveragerc
+-rw-r--r--   0 mmckerns   (501) staff       (20)       32 2022-05-09 23:49:56.000000 ppft-1.7.6.7/.gitignore
+-rw-r--r--   0 mmckerns   (501) staff       (20)      285 2022-05-16 23:08:33.000000 ppft-1.7.6.7/.readthedocs.yml
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1236 2023-07-07 03:20:06.000000 ppft-1.7.6.7/.travis.yml
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3824 2022-05-09 23:49:56.000000 ppft-1.7.6.7/CHANGELOG
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1580 2022-05-09 23:49:56.000000 ppft-1.7.6.7/COPYING
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1904 2023-02-08 18:06:16.000000 ppft-1.7.6.7/LICENSE
+-rw-r--r--   0 mmckerns   (501) staff       (20)      295 2022-07-06 22:43:22.000000 ppft-1.7.6.7/MANIFEST.in
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12194 2023-07-23 11:00:12.422749 ppft-1.7.6.7/PKG-INFO
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11737 2023-07-22 22:38:52.000000 ppft-1.7.6.7/README.md
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 11:00:12.382658 ppft-1.7.6.7/docs/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      668 2022-05-16 23:08:33.000000 ppft-1.7.6.7/docs/Makefile
+-rw-r--r--   0 mmckerns   (501) staff       (20)      430 2023-07-22 01:39:45.000000 ppft-1.7.6.7/docs/requirements.txt
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 11:00:12.386337 ppft-1.7.6.7/docs/source/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 11:00:12.367870 ppft-1.7.6.7/docs/source/_static/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 11:00:12.387009 ppft-1.7.6.7/docs/source/_static/css/
+-rw-r--r--   0 mmckerns   (501) staff       (20)       85 2023-07-05 04:40:59.000000 ppft-1.7.6.7/docs/source/_static/css/custom.css
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7914 2023-07-05 04:58:48.000000 ppft-1.7.6.7/docs/source/conf.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      302 2023-07-05 05:54:33.000000 ppft-1.7.6.7/docs/source/index.rst
+-rw-r--r--   0 mmckerns   (501) staff       (20)    78646 2022-05-16 23:08:33.000000 ppft-1.7.6.7/docs/source/pathos.png
+-rw-r--r--   0 mmckerns   (501) staff       (20)      465 2023-02-05 00:11:44.000000 ppft-1.7.6.7/docs/source/ppft.rst
+-rw-r--r--   0 mmckerns   (501) staff       (20)      138 2023-02-05 00:12:17.000000 ppft-1.7.6.7/docs/source/scripts.rst
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 11:00:12.392969 ppft-1.7.6.7/pp/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      454 2023-01-01 13:21:11.000000 ppft-1.7.6.7/pp/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      624 2023-01-01 13:17:04.000000 ppft-1.7.6.7/pp/__main__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      487 2023-01-01 13:17:04.000000 ppft-1.7.6.7/pp/_pp.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      410 2023-01-01 13:17:04.000000 ppft-1.7.6.7/pp/auto.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      414 2023-01-01 13:17:04.000000 ppft-1.7.6.7/pp/common.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 11:00:12.394614 ppft-1.7.6.7/pp/server/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      340 2023-01-01 13:21:41.000000 ppft-1.7.6.7/pp/server/__init__.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)      782 2023-01-01 13:17:04.000000 ppft-1.7.6.7/pp/server/__main__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      420 2023-01-01 13:17:04.000000 ppft-1.7.6.7/pp/transport.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      620 2023-01-01 13:17:04.000000 ppft-1.7.6.7/pp/worker.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 11:00:12.407088 ppft-1.7.6.7/ppft/
+-rw-r--r--   0 mmckerns   (501) staff       (20)    13071 2023-07-23 11:00:12.000000 ppft-1.7.6.7/ppft/__info__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1518 2023-01-01 13:17:04.000000 ppft-1.7.6.7/ppft/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5040 2023-01-01 13:17:04.000000 ppft-1.7.6.7/ppft/__main__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    33442 2023-02-19 19:32:19.000000 ppft-1.7.6.7/ppft/_pp.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5121 2023-01-01 13:17:04.000000 ppft-1.7.6.7/ppft/auto.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     5273 2023-01-01 13:17:04.000000 ppft-1.7.6.7/ppft/common.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 11:00:12.412605 ppft-1.7.6.7/ppft/server/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      495 2023-01-01 13:21:22.000000 ppft-1.7.6.7/ppft/server/__init__.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    15170 2023-01-01 13:17:04.000000 ppft-1.7.6.7/ppft/server/__main__.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 11:00:12.420955 ppft-1.7.6.7/ppft/tests/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      501 2023-01-01 13:17:04.000000 ppft-1.7.6.7/ppft/tests/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      965 2023-01-01 13:17:04.000000 ppft-1.7.6.7/ppft/tests/__main__.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     3628 2022-05-16 23:08:33.000000 ppft-1.7.6.7/ppft/tests/auto_diff.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2549 2022-06-28 22:04:22.000000 ppft-1.7.6.7/ppft/tests/callback.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1946 2022-05-16 23:08:33.000000 ppft-1.7.6.7/ppft/tests/dynamic_ncpus.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     1709 2022-06-28 22:04:22.000000 ppft-1.7.6.7/ppft/tests/quicksort.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2729 2022-05-09 23:52:22.000000 ppft-1.7.6.7/ppft/tests/reverse_md5.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2604 2023-01-30 17:56:22.000000 ppft-1.7.6.7/ppft/tests/sum_primes.py
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     2724 2022-05-16 23:08:33.000000 ppft-1.7.6.7/ppft/tests/sum_primes_functor.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9428 2023-01-01 13:17:04.000000 ppft-1.7.6.7/ppft/transport.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      624 2023-01-01 13:17:04.000000 ppft-1.7.6.7/ppft/worker.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 11:00:12.411146 ppft-1.7.6.7/ppft.egg-info/
+-rw-r--r--   0 mmckerns   (501) staff       (20)    12194 2023-07-23 11:00:12.000000 ppft-1.7.6.7/ppft.egg-info/PKG-INFO
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1067 2023-07-23 11:00:12.000000 ppft-1.7.6.7/ppft.egg-info/SOURCES.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)        1 2023-07-23 11:00:12.000000 ppft-1.7.6.7/ppft.egg-info/dependency_links.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)        1 2023-07-23 11:00:12.000000 ppft-1.7.6.7/ppft.egg-info/not-zip-safe
+-rw-r--r--   0 mmckerns   (501) staff       (20)       20 2023-07-23 11:00:12.000000 ppft-1.7.6.7/ppft.egg-info/requires.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)        8 2023-07-23 11:00:12.000000 ppft-1.7.6.7/ppft.egg-info/top_level.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)      166 2022-05-20 09:49:14.000000 ppft-1.7.6.7/pyproject.toml
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-23 11:00:12.421810 ppft-1.7.6.7/scripts/
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)    15170 2023-01-01 13:17:04.000000 ppft-1.7.6.7/scripts/ppserver
+-rw-r--r--   0 mmckerns   (501) staff       (20)       62 2023-07-23 11:00:12.424739 ppft-1.7.6.7/setup.cfg
+-rwxr-xr-x   0 mmckerns   (501) staff       (20)     4074 2023-07-22 22:38:57.000000 ppft-1.7.6.7/setup.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      467 2023-07-07 03:18:33.000000 ppft-1.7.6.7/tox.ini
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3171 2023-07-23 10:59:42.000000 ppft-1.7.6.7/version.py
```

### Comparing `ppft-1.7.6.6/.codecov.yml` & `ppft-1.7.6.7/.codecov.yml`

 * *Files identical despite different names*

### Comparing `ppft-1.7.6.6/.coveragerc` & `ppft-1.7.6.7/.coveragerc`

 * *Files identical despite different names*

### Comparing `ppft-1.7.6.6/CHANGELOG` & `ppft-1.7.6.7/CHANGELOG`

 * *Files identical despite different names*

### Comparing `ppft-1.7.6.6/COPYING` & `ppft-1.7.6.7/COPYING`

 * *Files identical despite different names*

### Comparing `ppft-1.7.6.6/LICENSE` & `ppft-1.7.6.7/LICENSE`

 * *Files 8% similar despite different names*

```diff
@@ -1,28 +1,28 @@
 Copyright (c) 2015-2016 California Institute of Technology.
-Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 All rights reserved.
 
 This software forks the python package "pp". Licence and copyright
 information for pp can be found in "COPYING".
 
 This software is available subject to the conditions and terms laid
 out below. By downloading and using this software you are agreeing
 to the following conditions.
 
 Redistribution and use in source and binary forms, with or without
 modification, are permitted provided that the following conditions
-are met::
+are met:
 
-    - Redistribution of source code must retain the above copyright
+    - Redistributions of source code must retain the above copyright
       notice, this list of conditions and the following disclaimer.
 
-    - Redistribution in binary form must reproduce the above copyright
+    - Redistributions in binary form must reproduce the above copyright
       notice, this list of conditions and the following disclaimer in the
-      documentations and/or other materials provided with the distribution.
+      documentation and/or other materials provided with the distribution.
 
     - Neither the names of the copyright holders nor the names of any of
       the contributors may be used to endorse or promote products derived
       from this software without specific prior written permission.
 
 THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
 "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED
```

### Comparing `ppft-1.7.6.6/docs/Makefile` & `ppft-1.7.6.7/docs/Makefile`

 * *Files identical despite different names*

### Comparing `ppft-1.7.6.6/docs/source/conf.py` & `ppft-1.7.6.7/docs/source/conf.py`

 * *Files 7% similar despite different names*

```diff
@@ -53,24 +53,42 @@
 # source_suffix = ['.rst', '.md']
 source_suffix = '.rst'
 
 # The master toctree document.
 master_doc = 'index'
 
 # General information about the project.
-project = u'ppft'
+project = 'ppft'
 year = datetime.now().year
-copyright = u'%d, The Uncertainty Quantification Foundation' % year
-author = u'Mike McKerns'
+copyright = '%d, The Uncertainty Quantification Foundation' % year
+author = 'Mike McKerns'
 
 # extension config
 github_project_url = "https://github.com/uqfoundation/ppft"
 autoclass_content = 'both'
+autodoc_default_options = {
+    'members': True,
+    'undoc-members': True,
+    'private-members': True,
+    'special-members': True,
+    'show-inheritance': True,
+    'imported-members': True,
+    'exclude-members': (
+        '__dict__,'
+        '__slots__,'
+        '__weakref__,'
+        '__module__,'
+        '_abc_impl,'
+        '__init__,'
+        '__annotations__,'
+        '__dataclass_fields__,'
+    )
+}
 autodoc_typehints = 'description'
-napoleon_include_init_with_doc = True
+autodoc_typehints_format = 'short'
 napoleon_include_private_with_doc = False
 napoleon_include_special_with_doc = True
 napoleon_use_ivar = True
 napoleon_use_param = True
 
 # The version info for the project you're documenting, acts as replacement for
 # |version| and |release|, also used in various other places throughout the
@@ -82,15 +100,15 @@
 release = version
 
 # The language for content autogenerated by Sphinx. Refer to documentation
 # for a list of supported languages.
 #
 # This is also used if you do content translation via gettext catalogs.
 # Usually you set "language" from the command line for these cases.
-language = None
+language = 'en'
 
 # List of patterns, relative to source directory, that match files and
 # directories to ignore when looking for source files.
 # This patterns also effect to html_static_path and html_extra_path
 exclude_patterns = []
 
 # The name of the Pygments (syntax highlighting) style to use.
@@ -110,57 +128,63 @@
 on_rtd = os.environ.get('READTHEDOCS', None) == 'True'
 
 # The theme to use for HTML and HTML Help pages.  See the documentation for
 # a list of builtin themes.
 #
 if not on_rtd:
     html_theme = 'alabaster' #'bizstyle'
+    html_css_files = ['css/custom.css',]
    #import sphinx_rtd_theme
    #html_theme = 'sphinx_rtd_theme'
    #html_theme_path = [sphinx_rtd_theme.get_html_theme_path()]
 
 # Theme options are theme-specific and customize the look and feel of a theme
 # further.  For a list of options available for each theme, see the
 # documentation.
 #
 html_theme_options = {
     'github_user': 'uqfoundation',
     'github_repo': 'ppft',
     'github_button': False,
     'github_banner': True,
     'travis_button': True,
+    'codecov_button': True,
+    'donate_url': 'http://uqfoundation.org/pages/donate.html',
     'gratipay_user': False,  # username
     'extra_nav_links': {'Module Index': 'py-modindex.html'},
 #   'show_related': True,
+#   'globaltoc_collapse': True,
+    'globaltoc_maxdepth': 4,
     'show_powered_by': False
 }
 
 # Add any paths that contain custom static files (such as style sheets) here,
 # relative to this directory. They are copied after the builtin static files,
 # so a file named "default.css" will overwrite the builtin "default.css".
 html_static_path = ['_static']
 
 # Custom sidebar templates, must be a dictionary that maps document names
 # to template names.
 #
 # This is required for the alabaster theme
 # refs: http://alabaster.readthedocs.io/en/latest/installation.html#sidebars
-#if html_theme == 'alabaster':
+if on_rtd:
+    toc_style = 'localtoc.html', # display the toctree
+else:
+    toc_style = 'globaltoc.html', # collapse the toctree
 html_sidebars = {
     '**': [
         'about.html',
+        'donate.html',
+        'searchbox.html',
 #       'navigation.html',
-        'localtoc.html', # display the toctree
+        toc_style, # defined above
         'relations.html', # needs 'show_related':True option to display
-        'searchbox.html',
-        'donate.html', # needs 'gratipay_user':<uname> option to display
     ]
 }
-#FIXME: donate / UQFoundation (home/github)
-
 
 # -- Options for HTMLHelp output ------------------------------------------
 
 # Output file base name for HTML help builder.
 htmlhelp_basename = 'ppftdoc'
 
 # Logo for sidebar
@@ -187,45 +211,45 @@
     # 'figure_align': 'htbp',
 }
 
 # Grouping the document tree into LaTeX files. List of tuples
 # (source start file, target name, title,
 #  author, documentclass [howto, manual, or own class]).
 latex_documents = [
-    (master_doc, 'ppft.tex', u'ppft Documentation',
-     u'Mike McKerns', 'manual'),
+    (master_doc, 'ppft.tex', 'ppft Documentation',
+     'Mike McKerns', 'manual'),
 ]
 
 
 # -- Options for manual page output ---------------------------------------
 
 # One entry per manual page. List of tuples
 # (source start file, name, description, authors, manual section).
 man_pages = [
-    (master_doc, 'ppft', u'ppft Documentation',
+    (master_doc, 'ppft', 'ppft Documentation',
      [author], 1)
 ]
 
 
 # -- Options for Texinfo output -------------------------------------------
 
 # Grouping the document tree into Texinfo files. List of tuples
 # (source start file, target name, title, author,
 #  dir menu entry, description, category)
 texinfo_documents = [
-    (master_doc, 'ppft', u'ppft Documentation',
+    (master_doc, 'ppft', 'ppft Documentation',
      author, 'ppft', 'Distributed and parallel python.',
      'Miscellaneous'),
 ]
 
 
 
 
 # Example configuration for intersphinx: refer to the Python standard library.
-intersphinx_mapping = {'https://docs.python.org/': None}
+intersphinx_mapping = {'https://docs.python.org/3/': None}
 #    {'python': {'https://docs.python.org/': None},
 #     'mystic': {'https://mystic.readthedocs.io/en/latest/', None},
 #     'pathos': {'https://pathos.readthedocs.io/en/latest/', None},
 #     'pox': {'https://pox.readthedocs.io/en/latest/', None},
 #     'dill': {'https://dill.readthedocs.io/en/latest/', None},
 #     'multiprocess': {'https://multiprocess.readthedocs.io/en/latest/', None},
 #     'klepto': {'https://klepto.readthedocs.io/en/latest/', None},
```

### Comparing `ppft-1.7.6.6/docs/source/pathos.png` & `ppft-1.7.6.7/docs/source/pathos.png`

 * *Files identical despite different names*

### Comparing `ppft-1.7.6.6/pp/__main__.py` & `ppft-1.7.6.7/pp/__main__.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2015-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/ppft/blob/master/LICENSE
 from ppft.__main__ import *
 from ppft.__main__ import _WorkerProcess, __version__, __doc__
 
 
 if __name__ == "__main__":
```

### Comparing `ppft-1.7.6.6/pp/server/__main__.py` & `ppft-1.7.6.7/pp/server/__main__.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2015-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/ppft/blob/master/LICENSE
 from ppft.server.__main__ import *
 from ppft.server.__main__ import __version__, _NetworkServer, __doc__
 
 
 if __name__ == "__main__":
```

### Comparing `ppft-1.7.6.6/pp/worker.py` & `ppft-1.7.6.7/pp/worker.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2015-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/ppft/blob/master/LICENSE
 from ppft.worker import *
 from ppft.worker import _WorkerProcess, __version__, __doc__
 
 
 if __name__ == "__main__":
```

### Comparing `ppft-1.7.6.6/ppft/__info__.py` & `ppft-1.7.6.7/README.md`

 * *Files 26% similar despite different names*

```diff
@@ -1,115 +1,229 @@
-#!/usr/bin/env python
-#
-# Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2022 The Uncertainty Quantification Foundation.
-# License: 3-clause BSD.  The full license text is available at:
-#  - https://github.com/uqfoundation/ppft/blob/master/LICENSE
-'''
--------------------------------------
-ppft: distributed and parallel python
--------------------------------------
+ppft
+====
+distributed and parallel Python
 
 About Ppft
-==========
+----------
+``ppft`` is a friendly fork of Parallel Python (``pp``). ``ppft`` extends Parallel Python to provide packaging and distribution with ``pip`` and ``setuptools``, support for Python 3, and enhanced serialization using ``dill.source``. ``ppft`` uses Parallel Python to provide mechanisms for the parallel execution of Python code on SMP (systems with multiple processors or cores) and clusters (computers connected via network).
 
-``ppft`` is a friendly fork of Parallel Python (``pp``). ``ppft`` extends Parallel Python to provide packaging and distribution with ``pip`` and ``setuptools``, support for python 3, and enhanced serialization using ``dill.source``. ``ppft`` uses Parallel Python to provide mechanisms for the parallel execution of python code on SMP (systems with multiple processors or cores) and clusters (computers connected via network).
+Software written in Python finds applications in a broad range of the categories including business logic, data analysis, and scientific calculations. This together with wide availability of SMP computers (multi-processor or multi-core) and clusters (computers connected via network) on the market create the demand in parallel execution of Python code.
 
-Software written in python finds applications in a broad range of the categories including business logic, data analysis, and scientific calculations. This together with wide availability of SMP computers (multi-processor or multi-core) and clusters (computers connected via network) on the market create the demand in parallel execution of python code.
+The most common way to write parallel applications for SMP computers is to use threads. However, the Python interpreter uses the GIL (Global Interpreter Lock) for internal bookkeeping, where the GIL only allows one Python byte-code instruction to execute at a time, even on an SMP computer. Parallel Python overcomes this limitation, and provides a simple way to write parallel Python applications. Internally, processes and IPC (Inter Process Communications) are used to organize parallel computations. Parallel Python is written so that the details and complexity of IPC are handled internally, and the calling application just submits jobs and retrieves the results. Software written with Parallel Python works in parallel on many computers connected via a local network or the Internet. Cross-platform portability and dynamic load-balancing allows Parallel Python to parallelize computations efficiently even on heterogeneous and multi-platform clusters. Visit http://www.parallelpython.com for further information on Parallel Python.
 
-The most common way to write parallel applications for SMP computers is to use threads. However, the python interpreter uses the GIL (Global Interpreter Lock) for internal bookkeeping, where the GIL only allows one python byte-code instruction to execute at a time, even on an SMP computer. Parallel Python overcomes this limitation, and provides a simple way to write parallel python applications. Internally, processes and IPC (Inter Process Communications) are used to organize parallel computations. Parallel Python is written so that the details and complexity of IPC are handled internally, and the calling application just submits jobs and retrieves the results. Software written with Parallel Python works in parallel on many computers connected via a local network or the Internet. Cross-platform portability and dynamic load-balancing allows Parallel Python to parallelize computations efficiently even on heterogeneous and multi-platform clusters. Visit http://www.parallelpython.com for further information on Parallel Python.
-
-``ppft`` is part of ``pathos``, a python framework for heterogeneous computing.
+``ppft`` is part of ``pathos``, a Python framework for heterogeneous computing.
 ``ppft`` is in active development, so any user feedback, bug reports, comments,
 or suggestions are highly appreciated.  A list of issues is located at https://github.com/uqfoundation/ppft/issues, with a legacy list maintained at https://uqfoundation.github.io/project/pathos/query.
 
 
 Major Features
-==============
-
+--------------
 ``ppft`` provides:
 
-    - parallel execution of python code on SMP and clusters
-    - easy-to-understand job-based parallelization
-    - automatic detection of the number of effective processors
-    - dynamic processor allocation (at runtime)
-    - low overhead for jobs with the same function (through transparent caching)
-    - dynamic load balancing (jobs are distributed at runtime)
-    - fault-tolerance (if a node fails, tasks are rescheduled on the others)
-    - auto-discovery of computational resources
-    - dynamic allocation of computational resources
-    - SHA based authentication for network connections
-    - enhanced serialization, using ``dill.source``
+* parallel execution of Python code on SMP and clusters
+* easy-to-understand job-based parallelization
+* automatic detection of the number of effective processors
+* dynamic processor allocation (at runtime)
+* low overhead for jobs with the same function (through transparent caching)
+* dynamic load balancing (jobs are distributed at runtime)
+* fault-tolerance (if a node fails, tasks are rescheduled on the others)
+* auto-discovery of computational resources
+* dynamic allocation of computational resources
+* SHA based authentication for network connections
+* enhanced serialization, using ``dill.source``
 
 
 Current Release
-===============
-
+[![Downloads](https://static.pepy.tech/personalized-badge/ppft?period=total&units=international_system&left_color=grey&right_color=blue&left_text=pypi%20downloads)](https://pepy.tech/project/ppft)
+[![Conda Downloads](https://img.shields.io/conda/dn/conda-forge/ppft?color=blue&label=conda%20downloads)](https://anaconda.org/conda-forge/ppft)
+[![Stack Overflow](https://img.shields.io/badge/stackoverflow-get%20help-black.svg)](https://stackoverflow.com/questions/tagged/parallel-python)
+---------------
 The latest released version of ``ppft`` is available from:
-
     https://pypi.org/project/ppft
 
 ``ppft`` is distributed under a 3-clause BSD license, and is a fork of ``pp-1.6.6``.
 
 
 Development Version
-===================
-
+[![Support](https://img.shields.io/badge/support-the%20UQ%20Foundation-purple.svg?style=flat&colorA=grey&colorB=purple)](http://www.uqfoundation.org/pages/donate.html)
+[![Documentation Status](https://readthedocs.org/projects/ppft/badge/?version=latest)](https://ppft.readthedocs.io/en/latest/?badge=latest)
+[![Build Status](https://travis-ci.com/uqfoundation/ppft.svg?label=build&logo=travis&branch=master)](https://travis-ci.com/github/uqfoundation/ppft)
+[![codecov](https://codecov.io/gh/uqfoundation/ppft/branch/master/graph/badge.svg)](https://codecov.io/gh/uqfoundation/ppft)
+-------------------
 You can get the latest development version with all the shiny new features at:
-
     https://github.com/uqfoundation
 
 If you have a new contribution, please submit a pull request.
 
 
 Installation
-============
-
+------------
 ``ppft`` can be installed with ``pip``::
 
     $ pip install ppft
 
 To include enhanced serialization, using ``dill.source``, install::
 
     $ pip install ppft[dill]
 
 If Parallel Python is already installed, it should be uninstalled before ``ppft`` is installed -- otherwise, ``import pp`` may point to the original and not to the ``ppft`` fork.
 
 
 Requirements
-============
-
+------------
 ``ppft`` requires:
 
-    - ``python`` (or ``pypy``), **>=3.7**
-    - ``setuptools``, **>=42**
+* ``python`` (or ``pypy``), **>=3.7**
+* ``setuptools``, **>=42**
 
 Optional requirements:
 
-    - ``dill``, **>=0.3.6**
+* ``dill``, **>=0.3.7**
 
 
-More Information
-================
+Basic Usage
+-----------
+``ppft`` is a fork of the Parallel Python package (``pp``) that has been
+converted from Python 2 to Python 3, made PEP 517 compliant, and augmented
+with ``dill.source``.  For simple parallel execution, first create a job
+``Server`` where the number nodes available is autodetected::
+
+    >>> import ppft as pp
+    >>> job_server = pp.Server()
+
+The number of nodes can be specified by passing an int as the first argument
+when creating the server (i.e. ``Server(4)`` creates a server with four nodes).
+The server uses ``submit`` to execute jobs in parallel. ``submit`` takes a
+function, a tuple of the arguments to pass to the function, a tuple of any
+functions used but not imported in the function, and a tuple of any modules
+required to produce the function:: 
+
+    >>> import math
+    >>> f1 = job_server.submit(math.sin, (math.pi/2,), (), ('math',))
+    >>> f2 = job_server.submit(min, (3.2, 10.0, 7.5), (), ())
+    >>> f3 = job_server.submit(sum, ([1,2,3],), (), ())
+
+The functions are serialized by ``dill.source`` (as opposed to ``dill``), by
+extracting and passing the source code to the server. The server compiles
+and executes the source code, and then calls the function with the arguments
+passed in the tuple. Any function and module dependencies are imported
+before ``exec`` is called on the source code. Results are retrieved by
+calling the object returned from ``submit``::
+
+    >>> f1()
+    1.0
+    >>> f2()
+    3.2
+    >>> f3()
+    6
+
+Job server execution statistics can be printed with::
+
+    >>> job_server.print_stats()
+    Job execution statistics:
+     job count | % of all jobs | job time sum | time per job | job server
+             3 |        100.00 |       0.0051 |     0.001684 | local
+    Time elapsed since server creation 148.48280715942383
+    0 active tasks, 4 cores
+
+``ppft`` also can execute jobs on remote computational nodes, if a ``ppserver``
+is first started on the node. Here the ``ppserver`` is started on 127.0.0.1,
+and will listen on port 35000::
+
+    $ ppserver -a -p 35000
+
+Then, locally, instantiate a ``Server`` with the connection information
+for the remote node, submit some jobs, and retrieve the results::
+
+    >>> job_server = pp.Server(ppservers=('127.0.0.1:35000',))
+    >>> f1 = job_server.submit(math.sin, (math.pi/2,), (), ('math',))
+    >>> f2 = job_server.submit(math.sin, (0,), (), ('math',))
+    >>> f3 = job_server.submit(math.sin, (-math.pi/2,), (), ('math',))
+    >>> f1(),f2(),f3()
+    (1.0, 0.0, -1.0)
+    >>> 
+
+However, the stats show that all of the jobs were run locally::
+
+    >>> job_server.print_stats()
+    Job execution statistics:
+     job count | % of all jobs | job time sum | time per job | job server
+             3 |        100.00 |       0.0024 |     0.000812 | local
+    Time elapsed since server creation 31.755322217941284
+    0 active tasks, 4 cores
+
+This is due because we don't specify the number of nodes. The number of nodes
+are specified both in the ``ppserver`` and in the local job ``Server``. Thus,
+the above is actually "autobalance" between 4 local nodes and 4 remote nodes.
+The former is naturally going to be preferred; however, if the local server is
+flooded with jobs, some will get sent to the remote ``ppserver``, and that will
+be reflected in the stats.  To run all jobs remotely, set the number of local
+nodes to zero::
+
+    >>> job_server = pp.Server(0, ppservers=('127.0.0.1:35000',))
+    >>> f1 = job_server.submit(math.sin, (math.pi/2,), (), ('math',))
+    >>> f2 = job_server.submit(math.sin, (0,), (), ('math',))
+    >>> f3 = job_server.submit(math.sin, (-math.pi/2,), (), ('math',))
+    >>> f1(),f2(),f3()
+    (1.0, 0.0, -1.0)
+    >>> job_server.print_stats()
+    Job execution statistics:
+     job count | % of all jobs | job time sum | time per job | job server
+             3 |        100.00 |       0.0016 |     0.000518 | 127.0.0.1:35000
+    Time elapsed since server creation 15.123202800750732
+    0 active tasks, 0 cores
+
+>>> 
+
+Get help on the command line options for ``ppserver``::
+
+    $ ppserver --help
+    Parallel Python Network Server (pp-1.7.6.7)
+    Usage: ppserver [-hdar] [-f format] [-n proto] [-c config_path] [-i interface] [-b broadcast] [-p port] [-w nworkers] [-s secret] [-t seconds] [-k seconds] [-P pid_file]
+
+    Options: 
+    -h                 : this help message
+    -d                 : set log level to debug
+    -f format          : log format
+    -a                 : enable auto-discovery service
+    -r                 : restart worker process after each task completion
+    -n proto           : protocol number for pickle module
+    -c path            : path to config file
+    -i interface       : interface to listen
+    -b broadcast       : broadcast address for auto-discovery service
+    -p port            : port to listen
+    -w nworkers        : number of workers to start
+    -s secret          : secret for authentication
+    -t seconds         : timeout to exit if no connections with clients exist
+    -k seconds         : socket timeout in seconds
+    -P pid_file        : file to write PID to
+
+    To print server stats send SIGUSR1 to its main process (unix only). 
+
+    Due to the security concerns always use a non-trivial secret key.
+    Secret key set by -s switch will override secret key assigned by
+    pp_secret variable in .pythonrc.py
+
 
+More Information
+----------------
 Probably the best way to get started is to look at the documentation at
 http://ppft.rtfd.io. Also, you can see a set of example scripts in
 ``ppft.tests``. You can run the test suite with ``python -m ppft.tests``.
 ``ppft`` will create and execute jobs on local workers (automatically created
 using ``python -u -m ppft``). Additionally, remote servers can be created with 
 ``ppserver`` (or ``python -m ppft.server``), and then jobs can be distributed
 to remote workers. See ``--help`` for more details on how to configure a server.
 Please feel free to submit a ticket on github, or ask a question on
 stackoverflow (**@Mike McKerns**).  If you would like to share how you use
 ``ppft`` in your work, please send an email (to **mmckerns at uqfoundation dot org**).
 
 
 Citation
-========
-
+--------
 If you use ``ppft`` to do research that leads to publication, we ask that you
 acknowledge use of ``ppft`` by citing the following in your publication::
 
     M.M. McKerns, L. Strand, T. Sullivan, A. Fang, M.A.G. Aivazis,
     "Building a framework for predictive science", Proceedings of
     the 10th Python in Science Conference, 2011;
     http://arxiv.org/pdf/1202.1056
@@ -117,52 +231,7 @@
     Michael McKerns and Michael Aivazis,
     "pathos: a framework for heterogeneous computing", 2010- ;
     https://uqfoundation.github.io/project/pathos
 
 Please see https://uqfoundation.github.io/project/pathos or
 http://arxiv.org/pdf/1202.1056 for further information.
 
-'''
-
-__version__ = '1.7.6.6'
-__author__ = 'Mike McKerns'
-
-__license__ = '''
-Copyright (c) 2015-2016 California Institute of Technology.
-Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
-All rights reserved.
-
-This software forks the python package "pp". Licence and copyright
-information for pp can be found in "COPYING".
-
-This software is available subject to the conditions and terms laid
-out below. By downloading and using this software you are agreeing
-to the following conditions.
-
-Redistribution and use in source and binary forms, with or without
-modification, are permitted provided that the following conditions
-are met::
-
-    - Redistribution of source code must retain the above copyright
-      notice, this list of conditions and the following disclaimer.
-
-    - Redistribution in binary form must reproduce the above copyright
-      notice, this list of conditions and the following disclaimer in the
-      documentations and/or other materials provided with the distribution.
-
-    - Neither the names of the copyright holders nor the names of any of
-      the contributors may be used to endorse or promote products derived
-      from this software without specific prior written permission.
-
-THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS
-"AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED
-TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR
-PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT OWNER OR
-CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL,
-EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO,
-PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS;
-OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY,
-WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR
-OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF
-ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
-
-'''
```

### Comparing `ppft-1.7.6.6/ppft/__init__.py` & `ppft-1.7.6.7/ppft/__init__.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2015-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/ppft/blob/master/LICENSE
 
 # author, version, license, and long description
 try: # the package is installed
     from .__info__ import __version__, __author__, __doc__, __license__
 except: # pragma: no cover
```

### Comparing `ppft-1.7.6.6/ppft/__main__.py` & `ppft-1.7.6.7/ppft/__main__.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 # Parallel Python Software: http://www.parallelpython.com
 # Copyright (c) 2005-2012 Vitalii Vanovschi.
 # Copyright (c) 2015-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # All rights reserved.
 # Redistribution and use in source and binary forms, with or without
 # modification, are permitted provided that the following conditions are met:
 #    * Redistributions of source code must retain the above copyright notice,
 #      this list of conditions and the following disclaimer.
 #    * Redistributions in binary form must reproduce the above copyright
 #      notice, this list of conditions and the following disclaimer in the
```

### Comparing `ppft-1.7.6.6/ppft/_pp.py` & `ppft-1.7.6.7/ppft/_pp.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 # Parallel Python Software: http://www.parallelpython.com
 # Copyright (c) 2005-2012 Vitalii Vanovschi.
 # Copyright (c) 2015-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # All rights reserved.
 # Redistribution and use in source and binary forms, with or without
 # modification, are permitted provided that the following conditions are met:
 #    * Redistributions of source code must retain the above copyright notice,
 #      this list of conditions and the following disclaimer.
 #    * Redistributions in binary form must reproduce the above copyright
 #      notice, this list of conditions and the following disclaimer in the
@@ -250,22 +250,22 @@
             callback=None, callbackargs=(), group='default', globals=None):
         """Creates Template instance
 
            jobs_server - pp server for submitting jobs
            func - function to be executed
            depfuncs - tuple with functions which might be called from 'func'
            modules - tuple with module names to import
-           callback - callback function which will be called with argument
-                   list equal to callbackargs+(result,)
-                   as soon as calculation is done
+           callback - function which will be called with argument list equal \
+                   to callbackargs+(result,) as soon as calculation is done
            callbackargs - additional arguments for callback function
-           group - job group, is used when wait(group) is called to wait for
-           jobs in a given group to finish
-           globals - dictionary from which all modules, functions and classes
-           will be imported, for instance: globals=globals()"""
+           group - job group, is used when wait(group) is called to wait for \
+                   jobs in a given group to finish
+           globals - dictionary from which all modules, functions and classes \
+                   will be imported, for instance: globals=globals()
+        """
         self.job_server = job_server
         self.func = func
         self.depfuncs = depfuncs
         self.modules = modules
         self.callback = callback
         self.callbackargs = callbackargs
         self.group = group
@@ -386,26 +386,25 @@
         self.logger.info("pp local server started with %d workers"
                 % (self.__ncpus, ))
 
     def submit(self, func, args=(), depfuncs=(), modules=(),
             callback=None, callbackargs=(), group='default', globals=None):
         """Submits function to the execution queue
 
-            func - function to be executed
-            args - tuple with arguments of the 'func'
-            depfuncs - tuple with functions which might be called from 'func'
-            modules - tuple with module names to import
-            callback - callback function which will be called with argument \
-                    list equal to callbackargs+(result,) \
-                    as soon as calculation is done
-            callbackargs - additional arguments for callback function
-            group - job group, is used when wait(group) is called to wait for
-            jobs in a given group to finish
-            globals - dict from which all modules, functions, and classes \
-                    will be imported, for instance: globals=globals()
+           func - function to be executed
+           args - tuple with arguments of the 'func'
+           depfuncs - tuple with functions which might be called from 'func'
+           modules - tuple with module names to import
+           callback - function which will be called with argument list equal \
+                   to callbackargs+(result,) as soon as calculation is done
+           callbackargs - additional arguments for callback function
+           group - job group, is used when wait(group) is called to wait for \
+                   jobs in a given group to finish
+           globals - dictionary from which all modules, functions and classes \
+                   will be imported, for instance: globals=globals()
         """
 
         # perform some checks for frequent mistakes
         if self._exiting:
             raise DestroyedServerError("Cannot submit jobs: server"\
                     " instance has been destroyed")
```

### Comparing `ppft-1.7.6.6/ppft/auto.py` & `ppft-1.7.6.7/ppft/auto.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 # Parallel Python Software: http://www.parallelpython.com
 # Copyright (c) 2005-2012 Vitalii Vanovschi.
 # Copyright (c) 2015-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # All rights reserved.
 # Redistribution and use in source and binary forms, with or without
 # modification, are permitted provided that the following conditions are met:
 #    * Redistributions of source code must retain the above copyright notice,
 #      this list of conditions and the following disclaimer.
 #    * Redistributions in binary form must reproduce the above copyright
 #      notice, this list of conditions and the following disclaimer in the
```

### Comparing `ppft-1.7.6.6/ppft/common.py` & `ppft-1.7.6.7/ppft/common.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 # Parallel Python Software: http://www.parallelpython.com
 # Copyright (c) 2005-2012 Vitalii Vanovschi.
 # Copyright (c) 2015-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # All rights reserved.
 # Redistribution and use in source and binary forms, with or without
 # modification, are permitted provided that the following conditions are met:
 #    * Redistributions of source code must retain the above copyright notice,
 #      this list of conditions and the following disclaimer.
 #    * Redistributions in binary form must reproduce the above copyright
 #      notice, this list of conditions and the following disclaimer in the
@@ -52,15 +52,15 @@
     if not hasattr(string, 'encode'): return string
     if not string.endswith(']{B}'): return string.encode('latin-1')
     return bytes(eval(string[:-3])) # special handling for non-ascii
 
 # copyright, including original from Parallel Python
 copyright = """Copyright (c) 2005-2012 Vitalii Vanovschi.
 Copyright (c) 2015-2016 California Institute of Technology.
-Copyright (c) 2016-2022 The Uncertainty Quantification Foundation."""
+Copyright (c) 2016-2023 The Uncertainty Quantification Foundation."""
 try: # the package is installed
     from .__info__ import __version__ as version
 except: # pragma: no cover
     import os
     import sys
     parent = os.path.dirname(os.path.abspath(os.path.dirname(__file__)))
     sys.path.append(parent)
```

### Comparing `ppft-1.7.6.6/ppft/server/__main__.py` & `ppft-1.7.6.7/ppft/server/__main__.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 # Parallel Python Software: http://www.parallelpython.com
 # Copyright (c) 2005-2012 Vitalii Vanovschi.
 # Copyright (c) 2015-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # All rights reserved.
 # Redistribution and use in source and binary forms, with or without
 # modification, are permitted provided that the following conditions are met:
 #    * Redistributions of source code must retain the above copyright notice,
 #      this list of conditions and the following disclaimer.
 #    * Redistributions in binary form must reproduce the above copyright
 #      notice, this list of conditions and the following disclaimer in the
```

### Comparing `ppft-1.7.6.6/ppft/tests/__main__.py` & `ppft-1.7.6.7/ppft/tests/__main__.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2018-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2018-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/ppft/blob/master/LICENSE
 
 import glob
 import os
 import sys
 import subprocess as sp
```

### Comparing `ppft-1.7.6.6/ppft/tests/auto_diff.py` & `ppft-1.7.6.7/ppft/tests/auto_diff.py`

 * *Files identical despite different names*

### Comparing `ppft-1.7.6.6/ppft/tests/callback.py` & `ppft-1.7.6.7/ppft/tests/callback.py`

 * *Files identical despite different names*

### Comparing `ppft-1.7.6.6/ppft/tests/dynamic_ncpus.py` & `ppft-1.7.6.7/ppft/tests/dynamic_ncpus.py`

 * *Files identical despite different names*

### Comparing `ppft-1.7.6.6/ppft/tests/quicksort.py` & `ppft-1.7.6.7/ppft/tests/quicksort.py`

 * *Files identical despite different names*

### Comparing `ppft-1.7.6.6/ppft/tests/reverse_md5.py` & `ppft-1.7.6.7/ppft/tests/reverse_md5.py`

 * *Files identical despite different names*

### Comparing `ppft-1.7.6.6/ppft/tests/sum_primes.py` & `ppft-1.7.6.7/ppft/tests/sum_primes.py`

 * *Files identical despite different names*

### Comparing `ppft-1.7.6.6/ppft/tests/sum_primes_functor.py` & `ppft-1.7.6.7/ppft/tests/sum_primes_functor.py`

 * *Files identical despite different names*

### Comparing `ppft-1.7.6.6/ppft/transport.py` & `ppft-1.7.6.7/ppft/transport.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 # Parallel Python Software: http://www.parallelpython.com
 # Copyright (c) 2005-2012 Vitalii Vanovschi.
 # Copyright (c) 2015-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # All rights reserved.
 # Redistribution and use in source and binary forms, with or without
 # modification, are permitted provided that the following conditions are met:
 #    * Redistributions of source code must retain the above copyright notice,
 #      this list of conditions and the following disclaimer.
 #    * Redistributions in binary form must reproduce the above copyright
 #      notice, this list of conditions and the following disclaimer in the
```

### Comparing `ppft-1.7.6.6/ppft/worker.py` & `ppft-1.7.6.7/ppft/worker.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2015-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/ppft/blob/master/LICENSE
 from ppft.__main__ import *
 from ppft.__main__ import _WorkerProcess, __version__, __doc__
 
 
 if __name__ == "__main__":
```

### Comparing `ppft-1.7.6.6/ppft.egg-info/SOURCES.txt` & `ppft-1.7.6.7/ppft.egg-info/SOURCES.txt`

 * *Files 4% similar despite different names*

```diff
@@ -16,14 +16,15 @@
 docs/Makefile
 docs/requirements.txt
 docs/source/conf.py
 docs/source/index.rst
 docs/source/pathos.png
 docs/source/ppft.rst
 docs/source/scripts.rst
+docs/source/_static/css/custom.css
 pp/__init__.py
 pp/__main__.py
 pp/_pp.py
 pp/auto.py
 pp/common.py
 pp/transport.py
 pp/worker.py
```

### Comparing `ppft-1.7.6.6/scripts/ppserver` & `ppft-1.7.6.7/scripts/ppserver`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 # Parallel Python Software: http://www.parallelpython.com
 # Copyright (c) 2005-2012 Vitalii Vanovschi.
 # Copyright (c) 2015-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # All rights reserved.
 # Redistribution and use in source and binary forms, with or without
 # modification, are permitted provided that the following conditions are met:
 #    * Redistributions of source code must retain the above copyright notice,
 #      this list of conditions and the following disclaimer.
 #    * Redistributions in binary form must reproduce the above copyright
 #      notice, this list of conditions and the following disclaimer in the
```

### Comparing `ppft-1.7.6.6/setup.py` & `ppft-1.7.6.7/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2012-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/ppft/blob/master/LICENSE
 
 import os
 import sys
 # drop support for older python
 if sys.version_info < (3, 7):
@@ -36,15 +36,15 @@
     Distribution = object
     has_setuptools = False
 
 # build the 'setup' call
 setup_kwds = dict(
     name='ppft',
     version=__version__,
-    description='distributed and parallel python',
+    description='distributed and parallel Python',
     long_description = README.strip(),
     author = __author__,
     author_email = AUTHOR_EMAIL,
     maintainer = __author__,
     maintainer_email = AUTHOR_EMAIL,
     license = 'BSD-3-Clause',
     platforms = ['Linux', 'Windows', 'Mac'],
@@ -62,14 +62,15 @@
         'Intended Audience :: Science/Research',
         'License :: OSI Approved :: BSD License',
         'Programming Language :: Python :: 3',
         'Programming Language :: Python :: 3.7',
         'Programming Language :: Python :: 3.8',
         'Programming Language :: Python :: 3.9',
         'Programming Language :: Python :: 3.10',
+        'Programming Language :: Python :: 3.11',
         'Programming Language :: Python :: Implementation :: CPython',
         'Programming Language :: Python :: Implementation :: PyPy',
         'Topic :: Scientific/Engineering',
         'Topic :: Software Development',
     ],
     packages = ['ppft', 'ppft.tests', 'ppft.server', 'pp', 'pp.server'],
     package_dir = {'ppft':'ppft', 'pp':'pp', 'ppft.server':'ppft/server', \
@@ -80,15 +81,15 @@
 # force python-, abi-, and platform-specific naming of bdist_wheel
 class BinaryDistribution(Distribution):
     """Distribution which forces a binary package with platform name"""
     def has_ext_modules(foo):
         return True
 
 # define dependencies
-dill_version = 'dill>=0.3.6'
+dill_version = 'dill>=0.3.7'
 # add dependencies
 depend = []
 extras = {'dill': [dill_version]}
 # update setup kwds
 if has_setuptools:
     setup_kwds.update(
         zip_safe=False,
```

### Comparing `ppft-1.7.6.6/version.py` & `ppft-1.7.6.7/version.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2022-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/ppft/blob/master/LICENSE
 
-__version__ = '1.7.6.6'
+__version__ = '1.7.6.7'
 __author__ = 'Mike McKerns'
 __contact__ = 'mmckerns@uqfoundation.org'
 
 
 def get_license_text(filepath):
     "open the LICENSE file and read the contents"
     try:
@@ -34,14 +34,21 @@
                 continue
             elif skip and line.startswith('    http'):
                 README += '\n' + line
             elif line.startswith('* '):
                 README += line.replace('* ','    - ',1)
             elif line.startswith('-'):
                 README += line.replace('-','=') + '\n'
+            elif line.startswith('!['): # image
+                alt,img = line.split('](',1)
+                if img.startswith('docs'): # relative path
+                    img = img.split('docs/source/',1)[-1] # make is in docs
+                README += '.. image:: ' + img.replace(')','')
+                README += '   :alt: ' + alt.replace('![','') + '\n'
+            #elif ')[http' in line: # alt text link (`text <http://url>`_)
             else:
                 README += line
                 skip = line.endswith(':\n')
         fh.close()
     except:
         README = ''
     return README
@@ -57,15 +64,15 @@
         license: the module's license contents
     """
     import os
     infofile = os.path.join(dirpath, '%s/__info__.py' % modulename)
     header = '''#!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/%s/blob/master/LICENSE
 ''' % modulename #XXX: author and email are hardwired in the header
     doc = info.get('doc', None)
     version = info.get('version', None)
     author = info.get('author', None)
     license = info.get('license', None)
```

