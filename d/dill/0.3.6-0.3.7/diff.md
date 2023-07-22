# Comparing `tmp/dill-0.3.6.tar.gz` & `tmp/dill-0.3.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dill-0.3.6.tar", last modified: Sun Oct 23 22:42:44 2022, max compression
+gzip compressed data, was "dill-0.3.7.tar", last modified: Sat Jul 22 21:38:29 2023, max compression
```

## Comparing `dill-0.3.6.tar` & `dill-0.3.7.tar`

### file list

```diff
@@ -1,79 +1,84 @@
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-23 22:42:44.267064 dill-0.3.6/
--rw-r--r--   0 mmckerns   (501) staff       (20)      830 2022-06-16 10:40:20.000000 dill-0.3.6/.codecov.yml
--rw-r--r--   0 mmckerns   (501) staff       (20)      547 2022-06-16 10:40:20.000000 dill-0.3.6/.coveragerc
--rw-r--r--   0 mmckerns   (501) staff       (20)       77 2022-07-15 14:15:24.000000 dill-0.3.6/.gitignore
--rw-r--r--   0 mmckerns   (501) staff       (20)      285 2022-06-16 10:40:20.000000 dill-0.3.6/.readthedocs.yml
--rw-r--r--   0 mmckerns   (501) staff       (20)     1232 2022-07-21 23:42:50.000000 dill-0.3.6/.travis.yml
--rw-r--r--   0 mmckerns   (501) staff       (20)     1790 2022-01-01 16:21:41.000000 dill-0.3.6/LICENSE
--rw-r--r--   0 mmckerns   (501) staff       (20)      203 2022-07-06 21:36:08.000000 dill-0.3.6/MANIFEST.in
--rw-r--r--   0 mmckerns   (501) staff       (20)     9794 2022-10-23 22:42:44.267372 dill-0.3.6/PKG-INFO
--rw-r--r--   0 mmckerns   (501) staff       (20)     9387 2022-07-01 23:07:22.000000 dill-0.3.6/README.md
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-23 22:42:44.226005 dill-0.3.6/dill/
--rw-r--r--   0 mmckerns   (501) staff       (20)     7143 2022-07-01 23:07:22.000000 dill-0.3.6/dill/__diff.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    10612 2022-10-23 22:42:44.000000 dill-0.3.6/dill/__info__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3797 2022-07-23 11:04:42.000000 dill-0.3.6/dill/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    82292 2022-08-13 19:10:17.000000 dill-0.3.6/dill/_dill.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    19368 2022-08-13 17:48:35.000000 dill-0.3.6/dill/_objects.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6635 2022-07-01 23:07:22.000000 dill-0.3.6/dill/_shims.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    11091 2022-07-01 23:07:22.000000 dill-0.3.6/dill/detect.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    11079 2022-08-13 19:10:17.000000 dill-0.3.6/dill/logger.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      736 2022-01-01 16:21:41.000000 dill-0.3.6/dill/objtypes.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4467 2022-01-01 16:21:41.000000 dill-0.3.6/dill/pointers.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    22500 2022-08-13 19:20:16.000000 dill-0.3.6/dill/session.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      630 2022-07-01 23:07:22.000000 dill-0.3.6/dill/settings.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    45121 2022-07-29 22:46:00.000000 dill-0.3.6/dill/source.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8027 2022-10-20 20:14:57.000000 dill-0.3.6/dill/temp.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-23 22:42:44.257875 dill-0.3.6/dill/tests/
--rw-r--r--   0 mmckerns   (501) staff       (20)      501 2022-06-26 12:33:37.000000 dill-0.3.6/dill/tests/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      899 2022-07-08 23:41:28.000000 dill-0.3.6/dill/tests/__main__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1396 2022-07-01 23:07:22.000000 dill-0.3.6/dill/tests/test_check.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6100 2022-08-13 19:10:17.000000 dill-0.3.6/dill/tests/test_classdef.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      885 2022-07-21 21:10:27.000000 dill-0.3.6/dill/tests/test_dataclasses.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4083 2022-07-01 23:07:22.000000 dill-0.3.6/dill/tests/test_detect.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1337 2022-06-26 12:33:37.000000 dill-0.3.6/dill/tests/test_dictviews.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2667 2022-07-01 23:07:22.000000 dill-0.3.6/dill/tests/test_diff.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1315 2022-07-01 23:07:22.000000 dill-0.3.6/dill/tests/test_extendpickle.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1679 2022-06-26 12:33:37.000000 dill-0.3.6/dill/tests/test_fglobals.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    13578 2022-07-01 23:07:22.000000 dill-0.3.6/dill/tests/test_file.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4119 2022-07-03 10:49:48.000000 dill-0.3.6/dill/tests/test_functions.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      930 2022-06-26 12:33:37.000000 dill-0.3.6/dill/tests/test_functors.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2380 2022-07-01 21:02:52.000000 dill-0.3.6/dill/tests/test_logger.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4007 2022-06-26 12:33:37.000000 dill-0.3.6/dill/tests/test_mixins.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1943 2022-07-01 23:07:22.000000 dill-0.3.6/dill/tests/test_module.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1182 2022-06-26 12:33:37.000000 dill-0.3.6/dill/tests/test_moduledict.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3146 2022-07-01 23:07:22.000000 dill-0.3.6/dill/tests/test_nested.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1834 2022-06-26 12:33:37.000000 dill-0.3.6/dill/tests/test_objects.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1346 2022-06-26 12:33:37.000000 dill-0.3.6/dill/tests/test_properties.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1412 2022-06-26 12:33:37.000000 dill-0.3.6/dill/tests/test_pycapsule.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4182 2022-07-01 23:07:22.000000 dill-0.3.6/dill/tests/test_recursive.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1250 2022-07-21 23:06:24.000000 dill-0.3.6/dill/tests/test_registered.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      783 2022-06-26 12:33:37.000000 dill-0.3.6/dill/tests/test_restricted.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3218 2022-07-23 23:12:59.000000 dill-0.3.6/dill/tests/test_selected.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    10156 2022-07-23 11:04:42.000000 dill-0.3.6/dill/tests/test_session.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6036 2022-07-01 23:07:22.000000 dill-0.3.6/dill/tests/test_source.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2619 2022-06-26 12:33:37.000000 dill-0.3.6/dill/tests/test_temp.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1602 2022-08-13 19:10:17.000000 dill-0.3.6/dill/tests/test_weakref.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-23 22:42:44.230320 dill-0.3.6/dill.egg-info/
--rw-r--r--   0 mmckerns   (501) staff       (20)     9794 2022-10-23 22:42:44.000000 dill-0.3.6/dill.egg-info/PKG-INFO
--rw-r--r--   0 mmckerns   (501) staff       (20)     1506 2022-10-23 22:42:44.000000 dill-0.3.6/dill.egg-info/SOURCES.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)        1 2022-10-23 22:42:44.000000 dill-0.3.6/dill.egg-info/dependency_links.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)        1 2022-10-23 22:42:43.000000 dill-0.3.6/dill.egg-info/not-zip-safe
--rw-r--r--   0 mmckerns   (501) staff       (20)       37 2022-10-23 22:42:44.000000 dill-0.3.6/dill.egg-info/requires.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)        5 2022-10-23 22:42:44.000000 dill-0.3.6/dill.egg-info/top_level.txt
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-23 22:42:44.259294 dill-0.3.6/docs/
--rw-r--r--   0 mmckerns   (501) staff       (20)      668 2022-06-16 10:40:20.000000 dill-0.3.6/docs/Makefile
--rw-r--r--   0 mmckerns   (501) staff       (20)      430 2022-06-16 10:40:20.000000 dill-0.3.6/docs/requirements.txt
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-23 22:42:44.264111 dill-0.3.6/docs/source/
--rw-r--r--   0 mmckerns   (501) staff       (20)     7387 2022-07-06 21:37:37.000000 dill-0.3.6/docs/source/conf.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2020 2022-07-23 11:04:42.000000 dill-0.3.6/docs/source/dill.rst
--rw-r--r--   0 mmckerns   (501) staff       (20)      381 2017-08-23 20:54:03.000000 dill-0.3.6/docs/source/index.rst
--rw-r--r--   0 mmckerns   (501) staff       (20)    78646 2017-08-11 19:07:27.000000 dill-0.3.6/docs/source/pathos.png
--rw-r--r--   0 mmckerns   (501) staff       (20)      215 2018-05-26 15:05:43.000000 dill-0.3.6/docs/source/scripts.rst
--rw-r--r--   0 mmckerns   (501) staff       (20)      166 2022-06-16 10:40:20.000000 dill-0.3.6/pyproject.toml
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-23 22:42:44.266217 dill-0.3.6/scripts/
--rw-r--r--   0 mmckerns   (501) staff       (20)     1654 2022-01-01 16:21:41.000000 dill-0.3.6/scripts/get_objgraph
--rw-r--r--   0 mmckerns   (501) staff       (20)      590 2022-01-01 16:21:41.000000 dill-0.3.6/scripts/undill
--rw-r--r--   0 mmckerns   (501) staff       (20)       62 2022-10-23 22:42:44.268483 dill-0.3.6/setup.cfg
--rw-r--r--   0 mmckerns   (501) staff       (20)     4333 2022-08-10 11:31:11.000000 dill-0.3.6/setup.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      274 2022-07-09 10:40:26.000000 dill-0.3.6/tox.ini
--rw-r--r--   0 mmckerns   (501) staff       (20)     2825 2022-10-23 22:42:13.000000 dill-0.3.6/version.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-22 21:38:29.013059 dill-0.3.7/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      830 2023-01-29 03:21:46.000000 dill-0.3.7/.codecov.yml
+-rw-r--r--   0 mmckerns   (501) staff       (20)      547 2023-01-29 03:21:46.000000 dill-0.3.7/.coveragerc
+-rw-r--r--   0 mmckerns   (501) staff       (20)       77 2023-01-29 03:21:46.000000 dill-0.3.7/.gitignore
+-rw-r--r--   0 mmckerns   (501) staff       (20)      285 2023-01-29 03:21:46.000000 dill-0.3.7/.readthedocs.yml
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1461 2023-07-07 03:04:23.000000 dill-0.3.7/.travis.yml
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1790 2023-02-08 18:07:04.000000 dill-0.3.7/LICENSE
+-rw-r--r--   0 mmckerns   (501) staff       (20)      203 2023-01-29 03:21:46.000000 dill-0.3.7/MANIFEST.in
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9845 2023-07-22 21:38:29.013384 dill-0.3.7/PKG-INFO
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9387 2023-03-10 04:05:12.000000 dill-0.3.7/README.md
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-22 21:38:28.923279 dill-0.3.7/dill/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7143 2023-01-29 03:21:46.000000 dill-0.3.7/dill/__diff.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10612 2023-07-22 21:38:28.000000 dill-0.3.7/dill/__info__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3798 2023-02-04 17:54:53.000000 dill-0.3.7/dill/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    87748 2023-06-25 05:23:08.000000 dill-0.3.7/dill/_dill.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    19423 2023-07-06 02:35:08.000000 dill-0.3.7/dill/_objects.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6635 2023-01-29 03:21:46.000000 dill-0.3.7/dill/_shims.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11091 2023-01-29 03:21:46.000000 dill-0.3.7/dill/detect.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11084 2023-01-29 03:21:46.000000 dill-0.3.7/dill/logger.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      736 2023-01-29 03:21:46.000000 dill-0.3.7/dill/objtypes.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4467 2023-04-27 14:09:34.000000 dill-0.3.7/dill/pointers.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    23525 2023-02-20 13:09:35.000000 dill-0.3.7/dill/session.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      630 2023-01-29 03:21:46.000000 dill-0.3.7/dill/settings.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    45121 2023-04-27 14:09:34.000000 dill-0.3.7/dill/source.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8027 2023-01-29 03:21:46.000000 dill-0.3.7/dill/temp.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-22 21:38:28.976851 dill-0.3.7/dill/tests/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      501 2023-01-29 03:21:46.000000 dill-0.3.7/dill/tests/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      899 2023-01-29 03:21:46.000000 dill-0.3.7/dill/tests/__main__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3838 2023-03-26 14:30:19.000000 dill-0.3.7/dill/tests/test_abc.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1396 2023-01-29 03:21:46.000000 dill-0.3.7/dill/tests/test_check.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7160 2023-03-08 00:19:41.000000 dill-0.3.7/dill/tests/test_classdef.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      890 2023-01-29 03:21:46.000000 dill-0.3.7/dill/tests/test_dataclasses.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4083 2023-01-29 03:21:46.000000 dill-0.3.7/dill/tests/test_detect.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1337 2023-01-29 03:21:46.000000 dill-0.3.7/dill/tests/test_dictviews.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2667 2023-01-29 03:21:46.000000 dill-0.3.7/dill/tests/test_diff.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1315 2023-01-29 03:21:46.000000 dill-0.3.7/dill/tests/test_extendpickle.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1676 2023-05-29 00:13:18.000000 dill-0.3.7/dill/tests/test_fglobals.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    13578 2023-01-29 03:21:46.000000 dill-0.3.7/dill/tests/test_file.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4267 2023-05-29 00:21:30.000000 dill-0.3.7/dill/tests/test_functions.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      930 2023-01-29 03:21:46.000000 dill-0.3.7/dill/tests/test_functors.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2385 2023-01-29 03:21:46.000000 dill-0.3.7/dill/tests/test_logger.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4007 2023-01-29 03:21:46.000000 dill-0.3.7/dill/tests/test_mixins.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1943 2023-01-29 03:21:46.000000 dill-0.3.7/dill/tests/test_module.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1182 2023-01-29 03:21:46.000000 dill-0.3.7/dill/tests/test_moduledict.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3146 2023-01-29 03:21:46.000000 dill-0.3.7/dill/tests/test_nested.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1834 2023-01-29 03:21:46.000000 dill-0.3.7/dill/tests/test_objects.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1346 2023-01-29 03:21:46.000000 dill-0.3.7/dill/tests/test_properties.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1417 2023-01-29 03:21:46.000000 dill-0.3.7/dill/tests/test_pycapsule.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4182 2023-05-28 22:00:35.000000 dill-0.3.7/dill/tests/test_recursive.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1573 2023-01-29 03:21:46.000000 dill-0.3.7/dill/tests/test_registered.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      783 2023-01-29 03:21:46.000000 dill-0.3.7/dill/tests/test_restricted.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3218 2023-01-29 03:21:46.000000 dill-0.3.7/dill/tests/test_selected.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10161 2023-01-29 03:21:46.000000 dill-0.3.7/dill/tests/test_session.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6036 2023-01-29 03:21:46.000000 dill-0.3.7/dill/tests/test_source.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2619 2023-01-29 03:21:46.000000 dill-0.3.7/dill/tests/test_temp.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1602 2023-01-29 03:21:46.000000 dill-0.3.7/dill/tests/test_weakref.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-22 21:38:28.928628 dill-0.3.7/dill.egg-info/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9845 2023-07-22 21:38:28.000000 dill-0.3.7/dill.egg-info/PKG-INFO
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1582 2023-07-22 21:38:28.000000 dill-0.3.7/dill.egg-info/SOURCES.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)        1 2023-07-22 21:38:28.000000 dill-0.3.7/dill.egg-info/dependency_links.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)        1 2023-07-22 21:38:28.000000 dill-0.3.7/dill.egg-info/not-zip-safe
+-rw-r--r--   0 mmckerns   (501) staff       (20)       37 2023-07-22 21:38:28.000000 dill-0.3.7/dill.egg-info/requires.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)        5 2023-07-22 21:38:28.000000 dill-0.3.7/dill.egg-info/top_level.txt
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-22 21:38:28.979301 dill-0.3.7/docs/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      668 2023-01-29 03:21:46.000000 dill-0.3.7/docs/Makefile
+-rw-r--r--   0 mmckerns   (501) staff       (20)      430 2023-07-22 01:39:18.000000 dill-0.3.7/docs/requirements.txt
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-22 21:38:29.006878 dill-0.3.7/docs/source/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-22 21:38:28.890742 dill-0.3.7/docs/source/_static/
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-22 21:38:29.009175 dill-0.3.7/docs/source/_static/css/
+-rw-r--r--   0 mmckerns   (501) staff       (20)       85 2023-07-05 04:40:17.000000 dill-0.3.7/docs/source/_static/css/custom.css
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8179 2023-07-05 05:02:43.000000 dill-0.3.7/docs/source/conf.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      846 2023-02-08 03:54:01.000000 dill-0.3.7/docs/source/dill.rst
+-rw-r--r--   0 mmckerns   (501) staff       (20)      302 2023-07-05 05:55:05.000000 dill-0.3.7/docs/source/index.rst
+-rw-r--r--   0 mmckerns   (501) staff       (20)    78646 2017-08-11 19:07:27.000000 dill-0.3.7/docs/source/pathos.png
+-rw-r--r--   0 mmckerns   (501) staff       (20)      235 2023-02-04 18:18:15.000000 dill-0.3.7/docs/source/scripts.rst
+-rw-r--r--   0 mmckerns   (501) staff       (20)      166 2023-01-29 03:21:46.000000 dill-0.3.7/pyproject.toml
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2023-07-22 21:38:29.012209 dill-0.3.7/scripts/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1872 2023-01-29 03:21:46.000000 dill-0.3.7/scripts/get_gprof
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1654 2023-01-29 03:21:46.000000 dill-0.3.7/scripts/get_objgraph
+-rw-r--r--   0 mmckerns   (501) staff       (20)      590 2023-01-29 03:21:46.000000 dill-0.3.7/scripts/undill
+-rw-r--r--   0 mmckerns   (501) staff       (20)       62 2023-07-22 21:38:29.014418 dill-0.3.7/setup.cfg
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4403 2023-02-20 18:34:36.000000 dill-0.3.7/setup.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      296 2023-07-07 02:58:47.000000 dill-0.3.7/tox.ini
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3263 2023-07-22 21:37:09.000000 dill-0.3.7/version.py
```

### Comparing `dill-0.3.6/.codecov.yml` & `dill-0.3.7/.codecov.yml`

 * *Files identical despite different names*

### Comparing `dill-0.3.6/.coveragerc` & `dill-0.3.7/.coveragerc`

 * *Files identical despite different names*

### Comparing `dill-0.3.6/LICENSE` & `dill-0.3.7/LICENSE`

 * *Files 5% similar despite different names*

```diff
@@ -1,25 +1,25 @@
 Copyright (c) 2004-2016 California Institute of Technology.
-Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 All rights reserved.
 
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

### Comparing `dill-0.3.6/PKG-INFO` & `dill-0.3.7/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 Metadata-Version: 2.1
 Name: dill
-Version: 0.3.6
-Summary: serialize all of python
+Version: 0.3.7
+Summary: serialize all of Python
 Home-page: https://github.com/uqfoundation/dill
 Download-URL: https://pypi.org/project/dill/#files
 Author: Mike McKerns
 Author-email: mmckerns@uqfoundation.org
 Maintainer: Mike McKerns
 Maintainer-email: mmckerns@uqfoundation.org
 License: BSD-3-Clause
@@ -20,67 +20,68 @@
 Classifier: Intended Audience :: Science/Research
 Classifier: License :: OSI Approved :: BSD License
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Programming Language :: Python :: Implementation :: PyPy
 Classifier: Topic :: Scientific/Engineering
 Classifier: Topic :: Software Development
 Requires-Python: >=3.7
 Provides-Extra: readline
 Provides-Extra: graph
 License-File: LICENSE
 
 -----------------------------
-dill: serialize all of python
+dill: serialize all of Python
 -----------------------------
 
 About Dill
 ==========
 
-``dill`` extends python's ``pickle`` module for serializing and de-serializing
-python objects to the majority of the built-in python types. Serialization
+``dill`` extends Python's ``pickle`` module for serializing and de-serializing
+Python objects to the majority of the built-in Python types. Serialization
 is the process of converting an object to a byte stream, and the inverse
-of which is converting a byte stream back to a python object hierarchy.
+of which is converting a byte stream back to a Python object hierarchy.
 
 ``dill`` provides the user the same interface as the ``pickle`` module, and
-also includes some additional features. In addition to pickling python
+also includes some additional features. In addition to pickling Python
 objects, ``dill`` provides the ability to save the state of an interpreter
 session in a single command.  Hence, it would be feasible to save an
 interpreter session, close the interpreter, ship the pickled file to
 another computer, open a new interpreter, unpickle the session and
 thus continue from the 'saved' state of the original interpreter
 session.
 
-``dill`` can be used to store python objects to a file, but the primary
-usage is to send python objects across the network as a byte stream.
+``dill`` can be used to store Python objects to a file, but the primary
+usage is to send Python objects across the network as a byte stream.
 ``dill`` is quite flexible, and allows arbitrary user defined classes
 and functions to be serialized.  Thus ``dill`` is not intended to be
 secure against erroneously or maliciously constructed data. It is
 left to the user to decide whether the data they unpickle is from
 a trustworthy source.
 
-``dill`` is part of ``pathos``, a python framework for heterogeneous computing.
+``dill`` is part of ``pathos``, a Python framework for heterogeneous computing.
 ``dill`` is in active development, so any user feedback, bug reports, comments,
 or suggestions are highly appreciated.  A list of issues is located at
 https://github.com/uqfoundation/dill/issues, with a legacy list maintained at
 https://uqfoundation.github.io/project/pathos/query.
 
 
 Major Features
 ==============
 
 ``dill`` can pickle the following standard types:
 
     - none, type, bool, int, float, complex, bytes, str,
     - tuple, list, dict, file, buffer, builtin,
-    - python classes, namedtuples, dataclasses, metaclasses,
+    - Python classes, namedtuples, dataclasses, metaclasses,
     - instances of classes,
     - set, frozenset, array, functions, exceptions
 
 ``dill`` can also pickle more 'exotic' standard types:
 
     - functions with yields, nested functions, lambdas,
     - cell, method, unboundmethod, module, code, methodwrapper,
@@ -89,15 +90,15 @@
 
 ``dill`` cannot yet pickle these standard types:
 
     - frame, generator, traceback
 
 ``dill`` also provides the capability to:
 
-    - save and load python interpreter sessions
+    - save and load Python interpreter sessions
     - save and extract the source code from functions and classes
     - interactively diagnose pickling errors
 
 
 Current Release
 ===============
 
@@ -235,15 +236,15 @@
 
 
 More Information
 ================
 
 Probably the best way to get started is to look at the documentation at
 http://dill.rtfd.io. Also see ``dill.tests`` for a set of scripts that
-demonstrate how ``dill`` can serialize different python objects. You can
+demonstrate how ``dill`` can serialize different Python objects. You can
 run the test suite with ``python -m dill.tests``. The contents of any
 pickle file can be examined with ``undill``.  As ``dill`` conforms to
 the ``pickle`` interface, the examples and documentation found at
 http://docs.python.org/library/pickle.html also apply to ``dill``
 if one will ``import dill as pickle``. The source code is also generally
 well documented, so further questions may be resolved by inspecting the
 code itself. Please feel free to submit a ticket on github, or ask a
```

### Comparing `dill-0.3.6/README.md` & `dill-0.3.7/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -1,49 +1,49 @@
 dill
 ====
-serialize all of python
+serialize all of Python
 
 About Dill
 ----------
-``dill`` extends python's ``pickle`` module for serializing and de-serializing
-python objects to the majority of the built-in python types. Serialization
+``dill`` extends Python's ``pickle`` module for serializing and de-serializing
+Python objects to the majority of the built-in Python types. Serialization
 is the process of converting an object to a byte stream, and the inverse
-of which is converting a byte stream back to a python object hierarchy.
+of which is converting a byte stream back to a Python object hierarchy.
 
 ``dill`` provides the user the same interface as the ``pickle`` module, and
-also includes some additional features. In addition to pickling python
+also includes some additional features. In addition to pickling Python
 objects, ``dill`` provides the ability to save the state of an interpreter
 session in a single command.  Hence, it would be feasible to save an
 interpreter session, close the interpreter, ship the pickled file to
 another computer, open a new interpreter, unpickle the session and
 thus continue from the 'saved' state of the original interpreter
 session.
 
-``dill`` can be used to store python objects to a file, but the primary
-usage is to send python objects across the network as a byte stream.
+``dill`` can be used to store Python objects to a file, but the primary
+usage is to send Python objects across the network as a byte stream.
 ``dill`` is quite flexible, and allows arbitrary user defined classes
 and functions to be serialized.  Thus ``dill`` is not intended to be
 secure against erroneously or maliciously constructed data. It is
 left to the user to decide whether the data they unpickle is from
 a trustworthy source.
 
-``dill`` is part of ``pathos``, a python framework for heterogeneous computing.
+``dill`` is part of ``pathos``, a Python framework for heterogeneous computing.
 ``dill`` is in active development, so any user feedback, bug reports, comments,
 or suggestions are highly appreciated.  A list of issues is located at
 https://github.com/uqfoundation/dill/issues, with a legacy list maintained at
 https://uqfoundation.github.io/project/pathos/query.
 
 
 Major Features
 --------------
 ``dill`` can pickle the following standard types:
 
 * none, type, bool, int, float, complex, bytes, str,
 * tuple, list, dict, file, buffer, builtin,
-* python classes, namedtuples, dataclasses, metaclasses,
+* Python classes, namedtuples, dataclasses, metaclasses,
 * instances of classes,
 * set, frozenset, array, functions, exceptions
 
 ``dill`` can also pickle more 'exotic' standard types:
 
 * functions with yields, nested functions, lambdas,
 * cell, method, unboundmethod, module, code, methodwrapper,
@@ -52,15 +52,15 @@
 
 ``dill`` cannot yet pickle these standard types:
 
 * frame, generator, traceback
 
 ``dill`` also provides the capability to:
 
-* save and load python interpreter sessions
+* save and load Python interpreter sessions
 * save and extract the source code from functions and classes
 * interactively diagnose pickling errors
 
 
 Current Release
 [![Downloads](https://static.pepy.tech/personalized-badge/dill?period=total&units=international_system&left_color=grey&right_color=blue&left_text=pypi%20downloads)](https://pepy.tech/project/dill)
 [![Conda Downloads](https://img.shields.io/conda/dn/conda-forge/dill?color=blue&label=conda%20downloads)](https://anaconda.org/conda-forge/dill)
@@ -197,15 +197,15 @@
 save the lambda object's state. A ``#`` marks when the object is actually stored.
 
 
 More Information
 ----------------
 Probably the best way to get started is to look at the documentation at
 http://dill.rtfd.io. Also see ``dill.tests`` for a set of scripts that
-demonstrate how ``dill`` can serialize different python objects. You can
+demonstrate how ``dill`` can serialize different Python objects. You can
 run the test suite with ``python -m dill.tests``. The contents of any
 pickle file can be examined with ``undill``.  As ``dill`` conforms to
 the ``pickle`` interface, the examples and documentation found at
 http://docs.python.org/library/pickle.html also apply to ``dill``
 if one will ``import dill as pickle``. The source code is also generally
 well documented, so further questions may be resolved by inspecting the
 code itself. Please feel free to submit a ticket on github, or ask a
```

### Comparing `dill-0.3.6/dill/__diff.py` & `dill-0.3.7/dill/__diff.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 """
 Module to show if an object has changed since it was memorised
 """
```

### Comparing `dill-0.3.6/dill/__info__.py` & `dill-0.3.7/dill/__info__.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,58 +1,58 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 '''
 -----------------------------
-dill: serialize all of python
+dill: serialize all of Python
 -----------------------------
 
 About Dill
 ==========
 
-``dill`` extends python's ``pickle`` module for serializing and de-serializing
-python objects to the majority of the built-in python types. Serialization
+``dill`` extends Python's ``pickle`` module for serializing and de-serializing
+Python objects to the majority of the built-in Python types. Serialization
 is the process of converting an object to a byte stream, and the inverse
-of which is converting a byte stream back to a python object hierarchy.
+of which is converting a byte stream back to a Python object hierarchy.
 
 ``dill`` provides the user the same interface as the ``pickle`` module, and
-also includes some additional features. In addition to pickling python
+also includes some additional features. In addition to pickling Python
 objects, ``dill`` provides the ability to save the state of an interpreter
 session in a single command.  Hence, it would be feasible to save an
 interpreter session, close the interpreter, ship the pickled file to
 another computer, open a new interpreter, unpickle the session and
 thus continue from the 'saved' state of the original interpreter
 session.
 
-``dill`` can be used to store python objects to a file, but the primary
-usage is to send python objects across the network as a byte stream.
+``dill`` can be used to store Python objects to a file, but the primary
+usage is to send Python objects across the network as a byte stream.
 ``dill`` is quite flexible, and allows arbitrary user defined classes
 and functions to be serialized.  Thus ``dill`` is not intended to be
 secure against erroneously or maliciously constructed data. It is
 left to the user to decide whether the data they unpickle is from
 a trustworthy source.
 
-``dill`` is part of ``pathos``, a python framework for heterogeneous computing.
+``dill`` is part of ``pathos``, a Python framework for heterogeneous computing.
 ``dill`` is in active development, so any user feedback, bug reports, comments,
 or suggestions are highly appreciated.  A list of issues is located at
 https://github.com/uqfoundation/dill/issues, with a legacy list maintained at
 https://uqfoundation.github.io/project/pathos/query.
 
 
 Major Features
 ==============
 
 ``dill`` can pickle the following standard types:
 
     - none, type, bool, int, float, complex, bytes, str,
     - tuple, list, dict, file, buffer, builtin,
-    - python classes, namedtuples, dataclasses, metaclasses,
+    - Python classes, namedtuples, dataclasses, metaclasses,
     - instances of classes,
     - set, frozenset, array, functions, exceptions
 
 ``dill`` can also pickle more 'exotic' standard types:
 
     - functions with yields, nested functions, lambdas,
     - cell, method, unboundmethod, module, code, methodwrapper,
@@ -61,15 +61,15 @@
 
 ``dill`` cannot yet pickle these standard types:
 
     - frame, generator, traceback
 
 ``dill`` also provides the capability to:
 
-    - save and load python interpreter sessions
+    - save and load Python interpreter sessions
     - save and extract the source code from functions and classes
     - interactively diagnose pickling errors
 
 
 Current Release
 ===============
 
@@ -207,15 +207,15 @@
 
 
 More Information
 ================
 
 Probably the best way to get started is to look at the documentation at
 http://dill.rtfd.io. Also see ``dill.tests`` for a set of scripts that
-demonstrate how ``dill`` can serialize different python objects. You can
+demonstrate how ``dill`` can serialize different Python objects. You can
 run the test suite with ``python -m dill.tests``. The contents of any
 pickle file can be examined with ``undill``.  As ``dill`` conforms to
 the ``pickle`` interface, the examples and documentation found at
 http://docs.python.org/library/pickle.html also apply to ``dill``
 if one will ``import dill as pickle``. The source code is also generally
 well documented, so further questions may be resolved by inspecting the
 code itself. Please feel free to submit a ticket on github, or ask a
@@ -240,36 +240,36 @@
     https://uqfoundation.github.io/project/pathos
 
 Please see https://uqfoundation.github.io/project/pathos or
 http://arxiv.org/pdf/1202.1056 for further information.
 
 '''
 
-__version__ = '0.3.6'
+__version__ = '0.3.7'
 __author__ = 'Mike McKerns'
 
 __license__ = '''
 Copyright (c) 2004-2016 California Institute of Technology.
-Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 All rights reserved.
 
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

### Comparing `dill-0.3.6/dill/__init__.py` & `dill-0.3.7/dill/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,36 +1,36 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 # author, version, license, and long description
 try: # the package is installed
     from .__info__ import __version__, __author__, __doc__, __license__
 except: # pragma: no cover
     import os
-    import sys 
+    import sys
     parent = os.path.dirname(os.path.abspath(os.path.dirname(__file__)))
     sys.path.append(parent)
-    # get distribution meta info 
+    # get distribution meta info
     from version import (__version__, __author__,
                          get_license_text, get_readme_as_rst)
     __license__ = get_license_text(os.path.join(parent, 'LICENSE'))
     __license__ = "\n%s" % __license__
     __doc__ = get_readme_as_rst(os.path.join(parent, 'README.md'))
     del os, sys, parent, get_license_text, get_readme_as_rst
 
 
 from ._dill import (
-    Pickler, Unpickler,
-    check, copy, dump, dumps, load, loads, pickle, pickles, register,
-    DEFAULT_PROTOCOL, HIGHEST_PROTOCOL, CONTENTS_FMODE, FILE_FMODE, HANDLE_FMODE,
+    dump, dumps, load, loads, copy,
+    Pickler, Unpickler, register, pickle, pickles, check,
+    DEFAULT_PROTOCOL, HIGHEST_PROTOCOL, HANDLE_FMODE, CONTENTS_FMODE, FILE_FMODE,
     PickleError, PickleWarning, PicklingError, PicklingWarning, UnpicklingError,
     UnpicklingWarning,
 )
 from .session import (
     dump_module, load_module, load_module_asdict,
     dump_session, load_session # backward compatibility
 )
@@ -38,16 +38,14 @@
 
 # get global settings
 from .settings import settings
 
 # make sure "trace" is turned off
 logger.trace(False)
 
-from importlib import reload
-
 objects = {}
 # local import of dill._objects
 #from . import _objects
 #objects.update(_objects.succeeds)
 #del _objects
 
 # local import of dill.objtypes
@@ -64,14 +62,15 @@
     Args:
         pickleable (bool, default=True): if True, load pickleable types.
         unpickleable (bool, default=True): if True, load unpickleable types.
 
     Returns:
         None
     """
+    from importlib import reload
     # local import of dill.objects
     from . import _objects
     if pickleable:
         objects.update(_objects.succeeds)
     else:
         [objects.pop(obj,None) for obj in _objects.succeeds]
     if unpickleable:
```

### Comparing `dill-0.3.6/dill/_dill.py` & `dill-0.3.7/dill/_dill.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,69 +1,87 @@
 # -*- coding: utf-8 -*-
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2015 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 """
 dill: a utility for serialization of python objects
 
+The primary functions in `dill` are :func:`dump` and
+:func:`dumps` for serialization ("pickling") to a
+file or to a string, respectively, and :func:`load`
+and :func:`loads` for deserialization ("unpickling"),
+similarly, from a file or from a string. Other notable
+functions are :func:`~dill.dump_module` and
+:func:`~dill.load_module`, which are used to save and
+restore module objects, including an intepreter session.
+
 Based on code written by Oren Tirosh and Armin Ronacher.
 Extended to a (near) full set of the builtin types (in types module),
 and coded to the pickle interface, by <mmckerns@caltech.edu>.
 Initial port to python3 by Jonathan Dobson, continued by mmckerns.
-Test against "all" python types (Std. Lib. CH 1-15 @ 2.7) by mmckerns.
-Test against CH16+ Std. Lib. ... TBD.
+Tested against "all" python types (Std. Lib. CH 1-15 @ 2.7) by mmckerns.
+Tested against CH16+ Std. Lib. ... TBD.
 """
+
+from __future__ import annotations
+
 __all__ = [
-    'Pickler','Unpickler',
-    'check','copy','dump','dumps','load','loads','pickle','pickles','register',
-    'DEFAULT_PROTOCOL','HIGHEST_PROTOCOL','CONTENTS_FMODE','FILE_FMODE','HANDLE_FMODE',
+    'dump','dumps','load','loads','copy',
+    'Pickler','Unpickler','register','pickle','pickles','check',
+    'DEFAULT_PROTOCOL','HIGHEST_PROTOCOL','HANDLE_FMODE','CONTENTS_FMODE','FILE_FMODE',
     'PickleError','PickleWarning','PicklingError','PicklingWarning','UnpicklingError',
     'UnpicklingWarning',
 ]
 
 __module__ = 'dill'
 
 import warnings
 from .logger import adapter as logger
 from .logger import trace as _trace
+log = logger # backward compatibility (see issue #582)
 
 import os
 import sys
 diff = None
 _use_diff = False
 OLD38 = (sys.hexversion < 0x3080000)
 OLD39 = (sys.hexversion < 0x3090000)
 OLD310 = (sys.hexversion < 0x30a0000)
+OLD312a7 = (sys.hexversion < 0x30c00a7)
 #XXX: get types from .objtypes ?
 import builtins as __builtin__
 from pickle import _Pickler as StockPickler, Unpickler as StockUnpickler
+from pickle import GLOBAL, POP
 from _thread import LockType
 from _thread import RLock as RLockType
 #from io import IOBase
 from types import CodeType, FunctionType, MethodType, GeneratorType, \
     TracebackType, FrameType, ModuleType, BuiltinMethodType
 BufferType = memoryview #XXX: unregistered
 ClassType = type # no 'old-style' classes
 EllipsisType = type(Ellipsis)
 #FileType = IOBase
 NotImplementedType = type(NotImplemented)
 SliceType = slice
 TypeType = type # 'new-style' classes #XXX: unregistered
 XRangeType = range
-from types import MappingProxyType as DictProxyType
+from types import MappingProxyType as DictProxyType, new_class
 from pickle import DEFAULT_PROTOCOL, HIGHEST_PROTOCOL, PickleError, PicklingError, UnpicklingError
 import __main__ as _main_module
 import marshal
 import gc
 # import zlib
+import abc
+import dataclasses
 from weakref import ReferenceType, ProxyType, CallableProxyType
 from collections import OrderedDict
+from enum import Enum, EnumMeta
 from functools import partial
 from operator import itemgetter, attrgetter
 GENERATOR_FAIL = False
 import importlib.machinery
 EXTENSION_SUFFIXES = tuple(importlib.machinery.EXTENSION_SUFFIXES)
 try:
     import ctypes
@@ -154,30 +172,27 @@
 except ImportError:
     PyTextWrapperType = PyBufferedRandomType = PyBufferedReaderType = PyBufferedWriterType = None
 from io import BytesIO as StringIO
 InputType = OutputType = None
 from socket import socket as SocketType
 #FIXME: additionally calls ForkingPickler.register several times
 from multiprocessing.reduction import _reduce_socket as reduce_socket
-try:
+try: #pragma: no cover
     IS_IPYTHON = __IPYTHON__  # is True
-    ExitType = None     # IPython.core.autocall.ExitAutocall
-    singletontypes = ['exit', 'quit', 'get_ipython']
+    ExitType = None # IPython.core.autocall.ExitAutocall
+    IPYTHON_SINGLETONS = ('exit', 'quit', 'get_ipython')
 except NameError:
     IS_IPYTHON = False
     try: ExitType = type(exit) # apparently 'exit' can be removed
     except NameError: ExitType = None
-    singletontypes = []
+    IPYTHON_SINGLETONS = ()
 
 import inspect
-import dataclasses
 import typing
 
-from pickle import GLOBAL
-
 
 ### Shims for different versions of Python and dill
 class Sentinel(object):
     """
     Create a unique sentinel object that is pickled as a constant.
     """
     def __init__(self, name, module_name=None):
@@ -316,15 +331,22 @@
 
 class UnpicklingWarning(PickleWarning, UnpicklingError):
     pass
 
 ### Extend the Picklers
 class Pickler(StockPickler):
     """python's Pickler extended to interpreter sessions"""
-    dispatch = MetaCatchingDict(StockPickler.dispatch.copy())
+    dispatch: typing.Dict[type, typing.Callable[[Pickler, typing.Any], None]] \
+            = MetaCatchingDict(StockPickler.dispatch.copy())
+    """The dispatch table, a dictionary of serializing functions used
+    by Pickler to save objects of specific types.  Use :func:`pickle`
+    or :func:`register` to associate types to custom functions.
+
+    :meta hide-value:
+    """
     _session = False
     from .settings import settings
 
     def __init__(self, file, *args, **kwds):
         settings = Pickler.settings
         _byref = kwds.pop('byref', None)
        #_strictio = kwds.pop('strictio', None)
@@ -337,66 +359,67 @@
         self._strictio = False #_strictio
         self._fmode = settings['fmode'] if _fmode is None else _fmode
         self._recurse = settings['recurse'] if _recurse is None else _recurse
         self._postproc = OrderedDict()
         self._file = file
 
     def save(self, obj, save_persistent_id=True):
-        # register if the object is a numpy ufunc
-        # thanks to Paul Kienzle for pointing out ufuncs didn't pickle
+        # numpy hack
         obj_type = type(obj)
         if NumpyArrayType and not (obj_type is type or obj_type in Pickler.dispatch):
-            if NumpyUfuncType and numpyufunc(obj_type):
+            # register if the object is a numpy ufunc
+            # thanks to Paul Kienzle for pointing out ufuncs didn't pickle
+            if numpyufunc(obj_type):
                 @register(obj_type)
                 def save_numpy_ufunc(pickler, obj):
                     logger.trace(pickler, "Nu: %s", obj)
                     name = getattr(obj, '__qualname__', getattr(obj, '__name__', None))
                     StockPickler.save_global(pickler, obj, name=name)
                     logger.trace(pickler, "# Nu")
                     return
                 # NOTE: the above 'save' performs like:
                 #   import copy_reg
                 #   def udump(f): return f.__name__
                 #   def uload(name): return getattr(numpy, name)
                 #   copy_reg.pickle(NumpyUfuncType, udump, uload)
             # register if the object is a numpy dtype
-            if NumpyDType and numpydtype(obj_type):
+            if numpydtype(obj_type):
                 @register(obj_type)
                 def save_numpy_dtype(pickler, obj):
                     logger.trace(pickler, "Dt: %s", obj)
                     pickler.save_reduce(_create_dtypemeta, (obj.type,), obj=obj)
                     logger.trace(pickler, "# Dt")
                     return
                 # NOTE: the above 'save' performs like:
                 #   import copy_reg
                 #   def uload(name): return type(NumpyDType(name))
                 #   def udump(f): return uload, (f.type,)
                 #   copy_reg.pickle(NumpyDTypeType, udump, uload)
             # register if the object is a subclassed numpy array instance
-            if NumpyArrayType and ndarraysubclassinstance(obj_type):
+            if ndarraysubclassinstance(obj_type):
                 @register(obj_type)
                 def save_numpy_array(pickler, obj):
                     logger.trace(pickler, "Nu: (%s, %s)", obj.shape, obj.dtype)
                     npdict = getattr(obj, '__dict__', None)
                     f, args, state = obj.__reduce__()
                     pickler.save_reduce(_create_array, (f,args,state,npdict), obj=obj)
                     logger.trace(pickler, "# Nu")
                     return
-        # end hack
-        if GENERATOR_FAIL and type(obj) == GeneratorType:
+        # end numpy hack
+
+        if GENERATOR_FAIL and obj_type is GeneratorType:
             msg = "Can't pickle %s: attribute lookup builtins.generator failed" % GeneratorType
             raise PicklingError(msg)
         StockPickler.save(self, obj, save_persistent_id)
 
     save.__doc__ = StockPickler.save.__doc__
 
     def dump(self, obj): #NOTE: if settings change, need to update attributes
         logger.trace_setup(self)
         StockPickler.dump(self, obj)
-
     dump.__doc__ = StockPickler.dump.__doc__
 
 class Unpickler(StockUnpickler):
     """python's Unpickler extended to interpreter sessions and more types"""
     from .settings import settings
     _session = False
 
@@ -432,20 +455,20 @@
     """get the dispatch table of registered types"""
     return Pickler.dispatch
 '''
 
 pickle_dispatch_copy = StockPickler.dispatch.copy()
 
 def pickle(t, func):
-    """expose dispatch table for user-created extensions"""
+    """expose :attr:`~Pickler.dispatch` table for user-created extensions"""
     Pickler.dispatch[t] = func
     return
 
 def register(t):
-    """register type to Pickler's dispatch table """
+    """decorator to register types to Pickler's :attr:`~Pickler.dispatch` table"""
     def proxy(func):
         Pickler.dispatch[t] = func
         return func
     return proxy
 
 def _revert_extension():
     """drop dill-registered types from pickle's dispatch table"""
@@ -456,15 +479,15 @@
                 StockPickler.dispatch[type] = pickle_dispatch_copy[type]
 
 def use_diff(on=True):
     """
     Reduces size of pickles by only including object which have changed.
 
     Decreases pickle size but increases CPU time needed.
-    Also helps avoid some unpicklable objects.
+    Also helps avoid some unpickleable objects.
     MUST be called at start of script, otherwise changes will not be recorded.
     """
     global _use_diff, diff
     _use_diff = on
     if _use_diff and diff is None:
         try:
             from . import diff as d
@@ -963,15 +986,15 @@
         pass
 
     if attr_found:
         if _PyCapsule_IsValid(capsule, name):
             return capsule
         raise UnpicklingError("%s object exists at %s but a PyCapsule object was expected." % (type(capsule), name))
     else:
-        warnings.warn('Creating a new PyCapsule %s for a C data structure that may not be present in memory. Segmentation faults or other memory errors are possible.' % (name,), UnpicklingWarning)
+        #warnings.warn('Creating a new PyCapsule %s for a C data structure that may not be present in memory. Segmentation faults or other memory errors are possible.' % (name,), UnpicklingWarning)
         capsule = _PyCapsule_New(pointer, name, destructor)
         _PyCapsule_SetContext(capsule, context)
         return capsule
 
 def _getattr(objclass, name, repr_str):
     # hack to grab the reference directly
     try: #XXX: works only for __builtin__ ?
@@ -1084,15 +1107,15 @@
                     pickler._batch_setitems(iter(source.items()))
                 else:
                     # Updating with an empty dictionary. Same as doing nothing.
                     continue
             else:
                 pickler.save_reduce(*reduction)
             # pop None created by calling preprocessing step off stack
-            pickler.write(bytes('0', 'UTF-8'))
+            pickler.write(POP)
 
 #@register(CodeType)
 #def save_code(pickler, obj):
 #    logger.trace(pickler, "Co: %s", obj)
 #    pickler.save_reduce(_unmarshal, (marshal.dumps(obj),), obj=obj)
 #    logger.trace(pickler, "# Co")
 #    return
@@ -1110,59 +1133,62 @@
             obj.co_argcount, obj.co_posonlyargcount,
             obj.co_kwonlyargcount, obj.co_nlocals, obj.co_stacksize,
             obj.co_flags, obj.co_code, obj.co_consts, obj.co_names,
             obj.co_varnames, obj.co_filename, obj.co_name, obj.co_qualname,
             obj.co_firstlineno, obj.co_linetable, obj.co_endlinetable,
             obj.co_columntable, obj.co_exceptiontable, obj.co_freevars,
             obj.co_cellvars
-    )
+        )
     elif hasattr(obj, "co_exceptiontable"): # python 3.11 (18 args)
-        args = (
-            obj.co_lnotab, # for < python 3.10 [not counted in args]
-            obj.co_argcount, obj.co_posonlyargcount,
-            obj.co_kwonlyargcount, obj.co_nlocals, obj.co_stacksize,
-            obj.co_flags, obj.co_code, obj.co_consts, obj.co_names,
-            obj.co_varnames, obj.co_filename, obj.co_name, obj.co_qualname,
-            obj.co_firstlineno, obj.co_linetable, obj.co_exceptiontable,
-            obj.co_freevars, obj.co_cellvars
-    )
+        with warnings.catch_warnings():
+            if not OLD312a7: # issue 597
+                warnings.filterwarnings('ignore', category=DeprecationWarning)
+            args = (
+                obj.co_lnotab, # for < python 3.10 [not counted in args]
+                obj.co_argcount, obj.co_posonlyargcount,
+                obj.co_kwonlyargcount, obj.co_nlocals, obj.co_stacksize,
+                obj.co_flags, obj.co_code, obj.co_consts, obj.co_names,
+                obj.co_varnames, obj.co_filename, obj.co_name, obj.co_qualname,
+                obj.co_firstlineno, obj.co_linetable, obj.co_exceptiontable,
+                obj.co_freevars, obj.co_cellvars
+            )
     elif hasattr(obj, "co_linetable"): # python 3.10 (16 args)
         args = (
             obj.co_lnotab, # for < python 3.10 [not counted in args]
             obj.co_argcount, obj.co_posonlyargcount,
             obj.co_kwonlyargcount, obj.co_nlocals, obj.co_stacksize,
             obj.co_flags, obj.co_code, obj.co_consts, obj.co_names,
             obj.co_varnames, obj.co_filename, obj.co_name,
             obj.co_firstlineno, obj.co_linetable, obj.co_freevars,
             obj.co_cellvars
-    )
+        )
     elif hasattr(obj, "co_posonlyargcount"): # python 3.8 (16 args)
         args = (
             obj.co_argcount, obj.co_posonlyargcount,
             obj.co_kwonlyargcount, obj.co_nlocals, obj.co_stacksize,
             obj.co_flags, obj.co_code, obj.co_consts, obj.co_names,
             obj.co_varnames, obj.co_filename, obj.co_name,
             obj.co_firstlineno, obj.co_lnotab, obj.co_freevars,
             obj.co_cellvars
-    )
+        )
     else: # python 3.7 (15 args)
         args = (
             obj.co_argcount, obj.co_kwonlyargcount, obj.co_nlocals,
             obj.co_stacksize, obj.co_flags, obj.co_code, obj.co_consts,
             obj.co_names, obj.co_varnames, obj.co_filename,
             obj.co_name, obj.co_firstlineno, obj.co_lnotab,
             obj.co_freevars, obj.co_cellvars
-    )
+        )
 
     pickler.save_reduce(_create_code, args, obj=obj)
     logger.trace(pickler, "# Co")
     return
 
 def _repr_dict(obj):
-    """make a short string representation of a dictionary"""
+    """Make a short string representation of a dictionary."""
     return "<%s object at %#012x>" % (type(obj).__name__, id(obj))
 
 @register(dict)
 def save_module_dict(pickler, obj):
     if is_dill(pickler, child=False) and obj == pickler._main.__dict__ and \
             not (pickler._session and pickler._first_pass):
         logger.trace(pickler, "D1: %s", _repr_dict(obj)) # obj
@@ -1466,15 +1492,15 @@
         # be replaced by () OR the delattr function can be removed repending on
         # whichever is more convienient.
         pickler.save_reduce(_create_cell, (_shims._CELL_EMPTY,), obj=obj)
         # Call the function _delattr on the cell's cell_contents attribute
         # The result of this function call will be None
         pickler.save_reduce(_shims._delattr, (obj, 'cell_contents'))
         # pop None created by calling _delattr off stack
-        pickler.write(bytes('0', 'UTF-8'))
+        pickler.write(POP)
         logger.trace(pickler, "# Ce3")
         return
     if is_dill(pickler, child=True):
         if id(f) in pickler._postproc:
             # Already seen. Add to its postprocessing.
             postproc = pickler._postproc[id(f)]
         else:
@@ -1581,150 +1607,265 @@
     refobj = _locate_object(_proxy_helper(obj))
     pickler.save_reduce(_create_weakproxy, (refobj, callable(obj)), obj=obj)
     logger.trace(pickler, "# R2")
     return
 
 def _is_builtin_module(module):
     if not hasattr(module, "__file__"): return True
+    if module.__file__ is None: return False
     # If a module file name starts with prefix, it should be a builtin
     # module, so should always be pickled as a reference.
     names = ["base_prefix", "base_exec_prefix", "exec_prefix", "prefix", "real_prefix"]
-    return any(os.path.realpath(module.__file__).startswith(os.path.realpath(getattr(sys, name)))
-               for name in names if hasattr(sys, name)) or \
-            module.__file__.endswith(EXTENSION_SUFFIXES) or \
-            'site-packages' in module.__file__
+    rp = os.path.realpath
+    # See https://github.com/uqfoundation/dill/issues/566
+    return (
+        any(
+            module.__file__.startswith(getattr(sys, name))
+            or rp(module.__file__).startswith(rp(getattr(sys, name)))
+            for name in names
+            if hasattr(sys, name)
+        )
+        or module.__file__.endswith(EXTENSION_SUFFIXES)
+        or 'site-packages' in module.__file__
+    )
 
 def _is_imported_module(module):
     return getattr(module, '__loader__', None) is not None or module in sys.modules.values()
 
 @register(ModuleType)
 def save_module(pickler, obj):
     if False: #_use_diff:
         if obj.__name__.split('.', 1)[0] != "dill":
             try:
                 changed = diff.whats_changed(obj, seen=pickler._diff_cache)[0]
             except RuntimeError:  # not memorised module, probably part of dill
                 pass
             else:
                 logger.trace(pickler, "M2: %s with diff", obj)
-                logger.trace(pickler, "Diff: %s", changed.keys())
+                logger.info("Diff: %s", changed.keys())
                 pickler.save_reduce(_import_module, (obj.__name__,), obj=obj,
                                     state=changed)
                 logger.trace(pickler, "# M2")
                 return
 
         logger.trace(pickler, "M1: %s", obj)
         pickler.save_reduce(_import_module, (obj.__name__,), obj=obj)
         logger.trace(pickler, "# M1")
     else:
         builtin_mod = _is_builtin_module(obj)
-        if obj.__name__ not in ("builtins", "dill", "dill._dill") and not builtin_mod or \
-                is_dill(pickler, child=True) and obj is pickler._main:
+        is_session_main = is_dill(pickler, child=True) and obj is pickler._main
+        if (obj.__name__ not in ("builtins", "dill", "dill._dill") and not builtin_mod
+                or is_session_main):
             logger.trace(pickler, "M1: %s", obj)
-            _main_dict = obj.__dict__.copy() #XXX: better no copy? option to copy?
-            [_main_dict.pop(item, None) for item in singletontypes
-                + ["__builtins__", "__loader__"]]
+            # Hack for handling module-type objects in load_module().
             mod_name = obj.__name__ if _is_imported_module(obj) else '__runtime__.%s' % obj.__name__
-            pickler.save_reduce(_import_module, (mod_name,), obj=obj,
-                                state=_main_dict)
+            # Second references are saved as __builtin__.__main__ in save_module_dict().
+            main_dict = obj.__dict__.copy()
+            for item in ('__builtins__', '__loader__'):
+                main_dict.pop(item, None)
+            for item in IPYTHON_SINGLETONS: #pragma: no cover
+                if getattr(main_dict.get(item), '__module__', '').startswith('IPython'):
+                    del main_dict[item]
+            pickler.save_reduce(_import_module, (mod_name,), obj=obj, state=main_dict)
             logger.trace(pickler, "# M1")
         elif obj.__name__ == "dill._dill":
             logger.trace(pickler, "M2: %s", obj)
             pickler.save_global(obj, name="_dill")
             logger.trace(pickler, "# M2")
         else:
             logger.trace(pickler, "M2: %s", obj)
             pickler.save_reduce(_import_module, (obj.__name__,), obj=obj)
             logger.trace(pickler, "# M2")
-        return
     return
 
+# The following function is based on '_extract_class_dict' from 'cloudpickle'
+# Copyright (c) 2012, Regents of the University of California.
+# Copyright (c) 2009 `PiCloud, Inc. <http://www.picloud.com>`_.
+# License: https://github.com/cloudpipe/cloudpickle/blob/master/LICENSE
+def _get_typedict_type(cls, clsdict, attrs, postproc_list):
+    """Retrieve a copy of the dict of a class without the inherited methods"""
+    if len(cls.__bases__) == 1:
+        inherited_dict = cls.__bases__[0].__dict__
+    else:
+        inherited_dict = {}
+        for base in reversed(cls.__bases__):
+            inherited_dict.update(base.__dict__)
+    to_remove = []
+    for name, value in dict.items(clsdict):
+        try:
+            base_value = inherited_dict[name]
+            if value is base_value:
+                to_remove.append(name)
+        except KeyError:
+            pass
+    for name in to_remove:
+        dict.pop(clsdict, name)
+
+    if issubclass(type(cls), type):
+        clsdict.pop('__dict__', None)
+        clsdict.pop('__weakref__', None)
+        # clsdict.pop('__prepare__', None)
+    return clsdict, attrs
+
+def _get_typedict_abc(obj, _dict, attrs, postproc_list):
+    if hasattr(abc, '_get_dump'):
+        (registry, _, _, _) = abc._get_dump(obj)
+        register = obj.register
+        postproc_list.extend((register, (reg(),)) for reg in registry)
+    elif hasattr(obj, '_abc_registry'):
+        registry = obj._abc_registry
+        register = obj.register
+        postproc_list.extend((register, (reg,)) for reg in registry)
+    else:
+        raise PicklingError("Cannot find registry of ABC %s", obj)
+
+    if '_abc_registry' in _dict:
+        _dict.pop('_abc_registry', None)
+        _dict.pop('_abc_cache', None)
+        _dict.pop('_abc_negative_cache', None)
+        # _dict.pop('_abc_negative_cache_version', None)
+    else:
+        _dict.pop('_abc_impl', None)
+    return _dict, attrs
+
 @register(TypeType)
 def save_type(pickler, obj, postproc_list=None):
     if obj in _typemap:
         logger.trace(pickler, "T1: %s", obj)
         # if obj in _incedental_types:
         #     warnings.warn('Type %r may only exist on this implementation of Python and cannot be unpickled in other implementations.' % (obj,), PicklingWarning)
         pickler.save_reduce(_load_type, (_typemap[obj],), obj=obj)
         logger.trace(pickler, "# T1")
     elif obj.__bases__ == (tuple,) and all([hasattr(obj, attr) for attr in ('_fields','_asdict','_make','_replace')]):
         # special case: namedtuples
         logger.trace(pickler, "T6: %s", obj)
+
+        obj_name = getattr(obj, '__qualname__', getattr(obj, '__name__', None))
+        if obj.__name__ != obj_name:
+            if postproc_list is None:
+                postproc_list = []
+            postproc_list.append((setattr, (obj, '__qualname__', obj_name)))
+
         if not obj._field_defaults:
-            pickler.save_reduce(_create_namedtuple, (obj.__name__, obj._fields, obj.__module__), obj=obj)
+            _save_with_postproc(pickler, (_create_namedtuple, (obj.__name__, obj._fields, obj.__module__)), obj=obj, postproc_list=postproc_list)
         else:
             defaults = [obj._field_defaults[field] for field in obj._fields if field in obj._field_defaults]
-            pickler.save_reduce(_create_namedtuple, (obj.__name__, obj._fields, obj.__module__, defaults), obj=obj)
+            _save_with_postproc(pickler, (_create_namedtuple, (obj.__name__, obj._fields, obj.__module__, defaults)), obj=obj, postproc_list=postproc_list)
         logger.trace(pickler, "# T6")
         return
 
-    # special cases: NoneType, NotImplementedType, EllipsisType
+    # special cases: NoneType, NotImplementedType, EllipsisType, EnumMeta
     elif obj is type(None):
         logger.trace(pickler, "T7: %s", obj)
         #XXX: pickler.save_reduce(type, (None,), obj=obj)
-        pickler.write(bytes('c__builtin__\nNoneType\n', 'UTF-8'))
+        pickler.write(GLOBAL + b'__builtin__\nNoneType\n')
         logger.trace(pickler, "# T7")
     elif obj is NotImplementedType:
         logger.trace(pickler, "T7: %s", obj)
         pickler.save_reduce(type, (NotImplemented,), obj=obj)
         logger.trace(pickler, "# T7")
     elif obj is EllipsisType:
         logger.trace(pickler, "T7: %s", obj)
         pickler.save_reduce(type, (Ellipsis,), obj=obj)
         logger.trace(pickler, "# T7")
+    elif obj is EnumMeta:
+        logger.trace(pickler, "T7: %s", obj)
+        pickler.write(GLOBAL + b'enum\nEnumMeta\n')
+        logger.trace(pickler, "# T7")
 
     else:
-        obj_name = getattr(obj, '__qualname__', getattr(obj, '__name__', None))
         _byref = getattr(pickler, '_byref', None)
         obj_recursive = id(obj) in getattr(pickler, '_postproc', ())
         incorrectly_named = not _locate_function(obj, pickler)
         if not _byref and not obj_recursive and incorrectly_named: # not a function, but the name was held over
+            if postproc_list is None:
+                postproc_list = []
+
             # thanks to Tom Stepleton pointing out pickler._session unneeded
             logger.trace(pickler, "T2: %s", obj)
-            _dict = obj.__dict__.copy() # convert dictproxy to dict
+            _dict, attrs = _get_typedict_type(obj, obj.__dict__.copy(), None, postproc_list) # copy dict proxy to a dict
+
            #print (_dict)
            #print ("%s\n%s" % (type(obj), obj.__name__))
            #print ("%s\n%s" % (obj.__bases__, obj.__dict__))
             slots = _dict.get('__slots__', ())
-            if type(slots) == str: slots = (slots,) # __slots__ accepts a single string
+            if type(slots) == str:
+                # __slots__ accepts a single string
+                slots = (slots,)
+
             for name in slots:
-                del _dict[name]
-            _dict.pop('__dict__', None)
-            _dict.pop('__weakref__', None)
-            _dict.pop('__prepare__', None)
-            if obj_name != obj.__name__:
-                if postproc_list is None:
-                    postproc_list = []
-                postproc_list.append((setattr, (obj, '__qualname__', obj_name)))
-            _save_with_postproc(pickler, (_create_type, (
-                type(obj), obj.__name__, obj.__bases__, _dict
-            )), obj=obj, postproc_list=postproc_list)
+                _dict.pop(name, None)
+
+            if isinstance(obj, abc.ABCMeta):
+                logger.trace(pickler, "ABC: %s", obj)
+                _dict, attrs = _get_typedict_abc(obj, _dict, attrs, postproc_list)
+                logger.trace(pickler, "# ABC")
+
+            qualname = getattr(obj, '__qualname__', None)
+            if attrs is not None:
+                for k, v in attrs.items():
+                    postproc_list.append((setattr, (obj, k, v)))
+                # TODO: Consider using the state argument to save_reduce?
+            if qualname is not None:
+                postproc_list.append((setattr, (obj, '__qualname__', qualname)))
+
+            if not hasattr(obj, '__orig_bases__'):
+                _save_with_postproc(pickler, (_create_type, (
+                    type(obj), obj.__name__, obj.__bases__, _dict
+                )), obj=obj, postproc_list=postproc_list)
+            else:
+                # This case will always work, but might be overkill.
+                _metadict = {
+                    'metaclass': type(obj)
+                }
+
+                if _dict:
+                    _dict_update = PartialType(_setitems, source=_dict)
+                else:
+                    _dict_update = None
+
+                _save_with_postproc(pickler, (new_class, (
+                    obj.__name__, obj.__orig_bases__, _metadict, _dict_update
+                )), obj=obj, postproc_list=postproc_list)
             logger.trace(pickler, "# T2")
         else:
+            obj_name = getattr(obj, '__qualname__', getattr(obj, '__name__', None))
             logger.trace(pickler, "T4: %s", obj)
             if incorrectly_named:
-                warnings.warn('Cannot locate reference to %r.' % (obj,), PicklingWarning)
+                warnings.warn(
+                    "Cannot locate reference to %r." % (obj,),
+                    PicklingWarning,
+                    stacklevel=3,
+                )
             if obj_recursive:
-                warnings.warn('Cannot pickle %r: %s.%s has recursive self-references that trigger a RecursionError.' % (obj, obj.__module__, obj_name), PicklingWarning)
+                warnings.warn(
+                    "Cannot pickle %r: %s.%s has recursive self-references that "
+                    "trigger a RecursionError." % (obj, obj.__module__, obj_name),
+                    PicklingWarning,
+                    stacklevel=3,
+                )
            #print (obj.__dict__)
            #print ("%s\n%s" % (type(obj), obj.__name__))
            #print ("%s\n%s" % (obj.__bases__, obj.__dict__))
             StockPickler.save_global(pickler, obj, name=obj_name)
             logger.trace(pickler, "# T4")
     return
 
 @register(property)
+@register(abc.abstractproperty)
 def save_property(pickler, obj):
     logger.trace(pickler, "Pr: %s", obj)
-    pickler.save_reduce(property, (obj.fget, obj.fset, obj.fdel, obj.__doc__),
+    pickler.save_reduce(type(obj), (obj.fget, obj.fset, obj.fdel, obj.__doc__),
                         obj=obj)
     logger.trace(pickler, "# Pr")
 
 @register(staticmethod)
 @register(classmethod)
+@register(abc.abstractstaticmethod)
+@register(abc.abstractclassmethod)
 def save_classmethod(pickler, obj):
     logger.trace(pickler, "Cm: %s", obj)
     orig_func = obj.__func__
 
     # if type(obj.__dict__) is dict:
     #     if obj.__dict__:
     #         state = obj.__dict__
@@ -1836,15 +1977,15 @@
                         topmost_postproc.remove(possible_postproc)
                     except ValueError:
                         continue
 
                     # Change the value of the cell
                     pickler.save_reduce(*possible_postproc)
                     # pop None created by calling preprocessing step off stack
-                    pickler.write(bytes('0', 'UTF-8'))
+                    pickler.write(POP)
 
         logger.trace(pickler, "# F1")
     else:
         logger.trace(pickler, "F2: %s", obj)
         name = getattr(obj, '__qualname__', getattr(obj, '__name__', None))
         StockPickler.save_global(pickler, obj, name=name)
         logger.trace(pickler, "# F2")
@@ -1883,15 +2024,15 @@
         None
     )
     PyCapsuleType = type(_testcapsule)
     @register(PyCapsuleType)
     def save_capsule(pickler, obj):
         logger.trace(pickler, "Cap: %s", obj)
         name = _PyCapsule_GetName(obj)
-        warnings.warn('Pickling a PyCapsule (%s) does not pickle any C data structures and could cause segmentation faults or other memory errors when unpickling.' % (name,), PicklingWarning)
+        #warnings.warn('Pickling a PyCapsule (%s) does not pickle any C data structures and could cause segmentation faults or other memory errors when unpickling.' % (name,), PicklingWarning)
         pointer = _PyCapsule_GetPointer(obj, name)
         context = _PyCapsule_GetContext(obj)
         destructor = _PyCapsule_GetDestructor(obj)
         pickler.save_reduce(_create_capsule, (pointer, name, context, destructor), obj=obj)
         logger.trace(pickler, "# Cap")
     _incedental_reverse_typemap['PyCapsuleType'] = PyCapsuleType
     _reverse_typemap['PyCapsuleType'] = PyCapsuleType
@@ -1953,17 +2094,17 @@
     try:
         pik = copy(obj, **kwds)
         #FIXME: should check types match first, then check content if "exact"
         try:
             #FIXME: should be "(pik == obj).all()" for numpy comparison, though that'll fail if shapes differ
             result = bool(pik.all() == obj.all())
         except (AttributeError, TypeError):
-            warnings.filterwarnings('ignore')
+            warnings.filterwarnings('ignore') #FIXME: be specific
             result = pik == obj
-            warnings.resetwarnings()
+            if warnings.filters: del warnings.filters[0]
         if hasattr(result, 'toarray'): # for unusual types like sparse matrix
             result = result.toarray().all()
         if result: return True
         if not exact:
             result = type(pik) == type(obj)
             if result: return result
             # class instances might have been dumped with byref=False
```

### Comparing `dill-0.3.6/dill/_objects.py` & `dill-0.3.7/dill/_objects.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 """
 all Python Standard Library objects (currently: CH 1-15 @ 2.7)
 and some other common objects (i.e. numpy.ndarray)
 """
 
@@ -391,15 +391,15 @@
 try:
     import symtable
     #FIXME: fails to pickle
     x["SymtableEntryType"] = symtable.symtable("", "string", "exec")._table
 except ImportError:
     pass
 
-if sys.hexversion >= 0x30a00a0:
+if sys.hexversion >= 0x30a00a0 and not IS_PYPY:
     x['LineIteratorType'] = compile('3', '', 'eval').co_lines()
 
 if sys.hexversion >= 0x30b00b0:
     from types import GenericAlias
     d["GenericAliasIteratorType"] = iter(GenericAlias(list, (int,)))
     x['PositionsIteratorType'] = compile('3', '', 'eval').co_positions()
 
@@ -480,15 +480,16 @@
     x['LPCCharObjType'] = _lpchar = ctypes.POINTER(ctypes.c_char)
     x['NullPtrType'] = _lpchar()
     x['NullPyObjectType'] = ctypes.py_object()
     x['PyObjectType'] = ctypes.py_object(lambda :None)
     z = a if IS_PYPY else x
     z['FieldType'] = _field = _Struct._field
     z['CFUNCTYPEType'] = _cfunc = ctypes.CFUNCTYPE(ctypes.c_char)
-    x['CFunctionType'] = _cfunc(str)
+    if sys.hexversion < 0x30c00b3:
+        x['CFunctionType'] = _cfunc(str)
     del z
 # numeric and mathematical types (CH 9)
 a['MethodCallerType'] = operator.methodcaller('mro') # 2.6
 # built-in types (CH 5)
 x['MemoryType'] = memoryview(_in) # 2.7
 x['MemoryType2'] = memoryview(bytearray(_in)) # 2.7
 d['DictItemsType'] = _dict.items() # 2.7
```

### Comparing `dill-0.3.6/dill/_shims.py` & `dill-0.3.7/dill/_shims.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Anirudh Vegesana (avegesan@cs.stanford.edu)
-# Copyright (c) 2021-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2021-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 """
 Provides shims for compatibility between versions of dill and Python.
 
 Compatibility shims should be provided in this file. Here are two simple example
 use cases.
```

### Comparing `dill-0.3.6/dill/detect.py` & `dill-0.3.7/dill/detect.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 """
 Methods for detecting objects leading to pickling failures.
 """
 
 import dis
```

### Comparing `dill-0.3.6/dill/logger.py` & `dill-0.3.7/dill/logger.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 # -*- coding: utf-8 -*-
 #
 # Author: Leonardo Gama (@leogama)
-# Copyright (c) 2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2022-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 """
 Logging utilities for dill.
 
 The 'logger' object is dill's top-level logger.
```

### Comparing `dill-0.3.6/dill/objtypes.py` & `dill-0.3.7/dill/objtypes.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 """
 all Python Standard Library object types (currently: CH 1-15 @ 2.7)
 and some other common object types (i.e. numpy.ndarray)
 
 to load more objects and types, use dill.load_types()
```

### Comparing `dill-0.3.6/dill/pointers.py` & `dill-0.3.7/dill/pointers.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 __all__ = ['parent', 'reference', 'at', 'parents', 'children']
 
 import gc
 import sys
@@ -111,12 +111,12 @@
                 if id(source) not in depth:
                     depth[id(source)] = tdepth + 1
                     parent[id(source)] = target
                     queue.append(source)
     return [obj] # not found
 
 
-# backward compatability
+# backward compatibility
 refobject = at
 
 
 # EOF
```

### Comparing `dill-0.3.6/dill/session.py` & `dill-0.3.7/dill/session.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,25 +1,26 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Leonardo Gama (@leogama)
 # Copyright (c) 2008-2015 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 """
 Pickle and restore the intepreter session.
 """
 
 __all__ = [
     'dump_module', 'load_module', 'load_module_asdict',
     'dump_session', 'load_session' # backward compatibility
 ]
 
 import re
+import os
 import sys
 import warnings
 
 from dill import _dill, Pickler, Unpickler
 from ._dill import (
     BuiltinMethodType, FunctionType, MethodType, ModuleType, TypeType,
     _import_module, _is_builtin_module, _is_imported_module, _main_module,
@@ -124,28 +125,29 @@
         for modname, name in main_module.__dict__.pop('__dill_imported_top_level'):
             main_module.__dict__[name] = __import__(modname)
     except KeyError:
         pass
 
 #NOTE: 06/03/15 renamed main_module to main
 def dump_module(
-    filename = str(TEMPDIR/'session.pkl'),
+    filename: Union[str, os.PathLike] = None,
     module: Optional[Union[ModuleType, str]] = None,
     refimported: bool = False,
     **kwds
 ) -> None:
     """Pickle the current state of :py:mod:`__main__` or another module to a file.
 
     Save the contents of :py:mod:`__main__` (e.g. from an interactive
     interpreter session), an imported module, or a module-type object (e.g.
     built with :py:class:`~types.ModuleType`), to a file. The pickled
     module can then be restored with the function :py:func:`load_module`.
 
-    Parameters:
-        filename: a path-like object or a writable stream.
+    Args:
+        filename: a path-like object or a writable stream. If `None`
+            (the default), write to a named file in a temporary directory.
         module: a module object or the name of an importable module. If `None`
             (the default), :py:mod:`__main__` is saved.
         refimported: if `True`, all objects identified as having been imported
             into the module's namespace are saved by reference. *Note:* this is
             similar but independent from ``dill.settings[`byref`]``, as
             ``refimported`` refers to virtually all imported objects, while
             ``byref`` only affects select objects.
@@ -188,21 +190,37 @@
           >>> pox = dill.load_module('pox_session.pkl')
           >>> pox.plus_one(1)
           2
           >>> foo = dill.load_module('foo_session.pkl')
           >>> [foo.sin(x) for x in foo.values]
           [0.8414709848078965, 0.9092974268256817, 0.1411200080598672]
 
+        - Use `refimported` to save imported objects by reference:
+
+          >>> import dill
+          >>> from html.entities import html5
+          >>> type(html5), len(html5)
+          (dict, 2231)
+          >>> import io
+          >>> buf = io.BytesIO()
+          >>> dill.dump_module(buf) # saves __main__, with html5 saved by value
+          >>> len(buf.getvalue()) # pickle size in bytes
+          71665
+          >>> buf = io.BytesIO()
+          >>> dill.dump_module(buf, refimported=True) # html5 saved by reference
+          >>> len(buf.getvalue())
+          438
+
     *Changed in version 0.3.6:* Function ``dump_session()`` was renamed to
     ``dump_module()``.  Parameters ``main`` and ``byref`` were renamed to
     ``module`` and ``refimported``, respectively.
 
     Note:
         Currently, ``dill.settings['byref']`` and ``dill.settings['recurse']``
-        don't apply to this function.`
+        don't apply to this function.
     """
     for old_par, par in [('main', 'module'), ('byref', 'refimported')]:
         if old_par in kwds:
             message = "The argument %r has been renamed %r" % (old_par, par)
             if old_par == 'byref':
                 message += " to distinguish it from dill.settings['byref']"
             warnings.warn(message + ".", PendingDeprecationWarning)
@@ -219,14 +237,16 @@
     elif isinstance(main, str):
         main = _import_module(main)
     if not isinstance(main, ModuleType):
         raise TypeError("%r is not a module" % main)
     if hasattr(filename, 'write'):
         file = filename
     else:
+        if filename is None:
+            filename = str(TEMPDIR/'session.pkl')
         file = open(filename, 'wb')
     try:
         pickler = Pickler(file, protocol, **kwds)
         pickler._original_main = main
         if refimported:
             main = _stash_modules(main)
         pickler._main = main     #FIXME: dill.settings are disabled
@@ -238,15 +258,15 @@
         pickler.dump(main)
     finally:
         if file is not filename:  # if newly opened file
             file.close()
     return
 
 # Backward compatibility.
-def dump_session(filename=str(TEMPDIR/'session.pkl'), main=None, byref=False, **kwds):
+def dump_session(filename=None, main=None, byref=False, **kwds):
     warnings.warn("dump_session() has been renamed dump_module()", PendingDeprecationWarning)
     dump_module(filename, module=main, refimported=byref, **kwds)
 dump_session.__doc__ = dump_module.__doc__
 
 class _PeekableReader:
     """lightweight stream wrapper that implements peek()"""
     def __init__(self, stream):
@@ -303,15 +323,15 @@
         # ValueError occours when the end of the chunk is reached (without a STOP).
         if isinstance(error, NotImplementedError) and main is not None:
             # file is not peekable, but we have main.
             return None
         raise UnpicklingError("unable to identify main module") from error
 
 def load_module(
-    filename = str(TEMPDIR/'session.pkl'),
+    filename: Union[str, os.PathLike] = None,
     module: Optional[Union[ModuleType, str]] = None,
     **kwds
 ) -> Optional[ModuleType]:
     """Update the selected module (default is :py:mod:`__main__`) with
     the state saved at ``filename``.
 
     Restore a module to the state saved with :py:func:`dump_module`. The
@@ -320,16 +340,17 @@
     :py:class:`~types.ModuleType`).
 
     When restoring the state of a non-importable module-type object, the
     current instance of this module may be passed as the argument ``main``.
     Otherwise, a new instance is created with :py:class:`~types.ModuleType`
     and returned.
 
-    Parameters:
-        filename: a path-like object or a readable stream.
+    Args:
+        filename: a path-like object or a readable stream. If `None`
+            (the default), read from a named file in a temporary directory.
         module: a module object or the name of an importable module;
             the module name and kind (i.e. imported or non-imported) must
             match the name and kind of the module stored at ``filename``.
         **kwds: extra keyword arguments passed to :py:class:`Unpickler()`.
 
     Raises:
         :py:exc:`UnpicklingError`: if unpickling fails.
@@ -415,14 +436,16 @@
         if module is not None:
             raise TypeError("both 'module' and 'main' arguments were used")
         module = kwds.pop('main')
     main = module
     if hasattr(filename, 'read'):
         file = filename
     else:
+        if filename is None:
+            filename = str(TEMPDIR/'session.pkl')
         file = open(filename, 'rb')
     try:
         file = _make_peekable(file)
         #FIXME: dill.settings are disabled
         unpickler = Unpickler(file, **kwds)
         unpickler._session = True
 
@@ -480,36 +503,37 @@
     _restore_modules(unpickler, main)
     if main is _main_module or main is module:
         return None
     else:
         return main
 
 # Backward compatibility.
-def load_session(filename=str(TEMPDIR/'session.pkl'), main=None, **kwds):
+def load_session(filename=None, main=None, **kwds):
     warnings.warn("load_session() has been renamed load_module().", PendingDeprecationWarning)
     load_module(filename, module=main, **kwds)
 load_session.__doc__ = load_module.__doc__
 
 def load_module_asdict(
-    filename = str(TEMPDIR/'session.pkl'),
+    filename: Union[str, os.PathLike] = None,
     update: bool = False,
     **kwds
 ) -> dict:
     """
     Load the contents of a saved module into a dictionary.
 
     ``load_module_asdict()`` is the near-equivalent of::
 
         lambda filename: vars(dill.load_module(filename)).copy()
 
     however, does not alter the original module. Also, the path of
     the loaded module is stored in the ``__session__`` attribute.
 
-    Parameters:
-        filename: a path-like object or a readable stream
+    Args:
+        filename: a path-like object or a readable stream. If `None`
+            (the default), read from a named file in a temporary directory.
         update: if `True`, initialize the dictionary with the current state
             of the module prior to loading the state stored at filename.
         **kwds: extra keyword arguments passed to :py:class:`Unpickler()`
 
     Raises:
         :py:exc:`UnpicklingError`: if unpickling fails
 
@@ -545,14 +569,16 @@
         False
     """
     if 'module' in kwds:
         raise TypeError("'module' is an invalid keyword argument for load_module_asdict()")
     if hasattr(filename, 'read'):
         file = filename
     else:
+        if filename is None:
+            filename = str(TEMPDIR/'session.pkl')
         file = open(filename, 'rb')
     try:
         file = _make_peekable(file)
         main_name = _identify_module(file)
         old_main = sys.modules.get(main_name)
         main = ModuleType(main_name)
         if update:
```

### Comparing `dill-0.3.6/dill/settings.py` & `dill-0.3.7/dill/settings.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 """
 global settings for Pickler
 """
 
 from pickle import DEFAULT_PROTOCOL
```

### Comparing `dill-0.3.6/dill/source.py` & `dill-0.3.7/dill/source.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 #
 # inspired by inspect.py from Python-2.7.6
 # inspect.py author: 'Ka-Ping Yee <ping@lfw.org>'
 # inspect.py merged into original dill.source by Mike McKerns 4/13/14
 """
@@ -662,15 +662,15 @@
         # check special cases (NoneType, Ellipsis, ...)
         if qual[-1] == 'ellipsis': qual[-1] = 'EllipsisType'
         if _intypes(qual[-1]): module = 'types' #XXX: BuiltinFunctionType
         qual = [module] + qual
     return qual
 
 
-#NOTE: 05/25/14 broke backward compatability: added 'alias' as 3rd argument
+#NOTE: 05/25/14 broke backward compatibility: added 'alias' as 3rd argument
 def _getimport(head, tail, alias='', verify=True, builtin=False):
     """helper to build a likely import string from head and tail of namespace.
     ('head','tail') are used in the following context: "from head import tail"
 
     If verify=True, then test the import string before returning it.
     If builtin=True, then force an import for builtins where possible.
     If alias is provided, then rename the object on import.
@@ -710,15 +710,15 @@
             if not _head: raise
             if _head != head:
                 _str = _getimport(_head, tail, alias, verify)
     return _str
 
 
 #XXX: rename builtin to force? vice versa? verify to force? (as in getsource)
-#NOTE: 05/25/14 broke backward compatability: added 'alias' as 2nd argument
+#NOTE: 05/25/14 broke backward compatibility: added 'alias' as 2nd argument
 def getimport(obj, alias='', verify=True, builtin=False, enclosing=False):
     """get the likely import string for the given object
 
     obj is the object to inspect
     If verify=True, then test the import string before returning it.
     If builtin=True, then force an import for builtins where possible.
     If enclosing=True, get the import for the outermost enclosing callable.
@@ -997,15 +997,15 @@
             if tried_import: raise
             tried_source = True
             source = not source
     # should never get here
     return
 
 
-# backward compatability
+# backward compatibility
 def getimportable(obj, alias='', byname=True, explicit=False):
     return importable(obj,alias,source=(not byname),builtin=explicit)
    #return outdent(_importable(obj,alias,source=(not byname),builtin=explicit))
 def likely_import(obj, passive=False, explicit=False):
     return getimport(obj, verify=(not passive), builtin=explicit)
 def _likely_import(first, last, passive=False, explicit=True):
     return _getimport(first, last, verify=(not passive), builtin=explicit)
```

### Comparing `dill-0.3.6/dill/temp.py` & `dill-0.3.7/dill/temp.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 """
 Methods for serialized objects (or source code) stored in temporary files
 and file-like objects.
 """
 #XXX: better instead to have functions write to any given file-like object ?
```

### Comparing `dill-0.3.6/dill/tests/__main__.py` & `dill-0.3.7/dill/tests/__main__.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2018-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2018-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 import glob
 import os
 import sys
 import subprocess as sp
```

### Comparing `dill-0.3.6/dill/tests/test_check.py` & `dill-0.3.7/dill/tests/test_check.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 from dill import check
 import sys
 
 from dill.temp import capture
```

### Comparing `dill-0.3.6/dill/tests/test_classdef.py` & `dill-0.3.7/dill/tests/test_classdef.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,16 +1,17 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 import dill
+from enum import EnumMeta
 import sys
 dill.settings['recurse'] = True
 
 # test classdefs
 class _class:
     def _method(self):
         pass
@@ -50,14 +51,22 @@
 
 o = _class()
 oc = _class2()
 n = _newclass()
 nc = _newclass2()
 m = _mclass()
 
+if sys.hexversion < 0x03090000:
+    import typing
+    class customIntList(typing.List[int]):
+        pass
+else:
+    class customIntList(list[int]):
+        pass
+
 # test pickles for class instances
 def test_class_instances():
     assert dill.pickles(o)
     assert dill.pickles(oc)
     assert dill.pickles(n)
     assert dill.pickles(nc)
     assert dill.pickles(m)
@@ -85,48 +94,62 @@
             assert type(_cls).__name__ == "_meta"
 
 # test NoneType
 def test_specialtypes():
     assert dill.pickles(type(None))
     assert dill.pickles(type(NotImplemented))
     assert dill.pickles(type(Ellipsis))
+    assert dill.pickles(type(EnumMeta))
 
 from collections import namedtuple
 Z = namedtuple("Z", ['a','b'])
 Zi = Z(0,1)
 X = namedtuple("Y", ['a','b'])
 X.__name__ = "X"
 X.__qualname__ = "X" #XXX: name must 'match' or fails to pickle
 Xi = X(0,1)
 Bad = namedtuple("FakeName", ['a','b'])
 Badi = Bad(0,1)
+Defaults = namedtuple('Defaults', ['x', 'y'], defaults=[1])
+Defaultsi = Defaults(2)
 
 # test namedtuple
 def test_namedtuple():
     assert Z is dill.loads(dill.dumps(Z))
     assert Zi == dill.loads(dill.dumps(Zi))
     assert X is dill.loads(dill.dumps(X))
     assert Xi == dill.loads(dill.dumps(Xi))
+    assert Defaults is dill.loads(dill.dumps(Defaults))
+    assert Defaultsi == dill.loads(dill.dumps(Defaultsi))
     assert Bad is not dill.loads(dill.dumps(Bad))
     assert Bad._fields == dill.loads(dill.dumps(Bad))._fields
     assert tuple(Badi) == tuple(dill.loads(dill.dumps(Badi)))
 
     class A:
-        class B(namedtuple("B", ["one", "two"])):
+        class B(namedtuple("C", ["one", "two"])):
             '''docstring'''
         B.__module__ = 'testing'
 
     a = A()
     assert dill.copy(a)
 
     assert dill.copy(A.B).__name__ == 'B'
     assert dill.copy(A.B).__qualname__.endswith('.<locals>.A.B')
     assert dill.copy(A.B).__doc__ == 'docstring'
     assert dill.copy(A.B).__module__ == 'testing'
 
+    from typing import NamedTuple
+
+    def A():
+        class B(NamedTuple):
+            x: int
+        return B
+
+    assert type(dill.copy(A()(8))).__qualname__ == type(A()(8)).__qualname__
+
 def test_dtype():
     try:
         import numpy as np
 
         dti = np.dtype('int')
         assert np.dtype == dill.copy(np.dtype)
         assert dti == dill.copy(dti)
@@ -200,19 +223,28 @@
   __slots__ = ('y', '__weakref__')
   def __init__(self, y):
     self.y = y
 
 value = 123
 y = Y(value)
 
+class Y2(object):
+  __slots__ = 'y'
+  def __init__(self, y):
+    self.y = y
+
 def test_slots():
     assert dill.pickles(Y)
     assert dill.pickles(y)
     assert dill.pickles(Y.y)
     assert dill.copy(y).y == value
+    assert dill.copy(Y2(value)).y == value
+
+def test_origbases():
+    assert dill.copy(customIntList).__orig_bases__ == customIntList.__orig_bases__
 
 def test_attr():
     import attr
     @attr.s
     class A:
         a = attr.ib()
 
@@ -234,19 +266,26 @@
         def __new__(cls):
             self = super().__new__(cls)
             return self""", None, l)
     subclass_with_new = l['subclass_with_new']
 
     assert dill.copy(subclass_with_new())
 
+def test_enummeta():
+    from http import HTTPStatus
+    import enum
+    assert dill.copy(HTTPStatus.OK) is HTTPStatus.OK
+    assert dill.copy(enum.EnumMeta) is enum.EnumMeta
 
 if __name__ == '__main__':
     test_class_instances()
     test_class_objects()
     test_specialtypes()
     test_namedtuple()
     test_dtype()
     test_array_nested()
     test_array_subclass()
     test_method_decorator()
     test_slots()
+    test_origbases()
     test_metaclass()
+    test_enummeta()
```

### Comparing `dill-0.3.6/dill/tests/test_dataclasses.py` & `dill-0.3.7/dill/tests/test_dataclasses.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Anirudh Vegesana (avegesan@cs.stanford.edu)
-# Copyright (c) 2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2022-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 """
 test pickling a dataclass
 """
 
 import dill
```

### Comparing `dill-0.3.6/dill/tests/test_detect.py` & `dill-0.3.7/dill/tests/test_detect.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 from dill.detect import baditems, badobjects, badtypes, errors, parent, at, globalvars
 from dill import settings
 from dill._dill import IS_PYPY
 from pickle import PicklingError
```

### Comparing `dill-0.3.6/dill/tests/test_dictviews.py` & `dill-0.3.7/dill/tests/test_dictviews.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Anirudh Vegesana (avegesan@cs.stanford.edu)
-# Copyright (c) 2021-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2021-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 import dill
 from dill._dill import OLD310, MAPPING_PROXY_TRICK, DictProxyType
 
 def test_dictproxy():
```

### Comparing `dill-0.3.6/dill/tests/test_diff.py` & `dill-0.3.7/dill/tests/test_diff.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 from dill import __diff as diff
 
 import sys
 IS_PYPY = not hasattr(sys, 'getrefcount')
```

### Comparing `dill-0.3.6/dill/tests/test_extendpickle.py` & `dill-0.3.7/dill/tests/test_extendpickle.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 import dill as pickle
 from io import BytesIO as StringIO
```

### Comparing `dill-0.3.6/dill/tests/test_fglobals.py` & `dill-0.3.7/dill/tests/test_fglobals.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2021-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2021-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 import dill
 dill.settings['recurse'] = True
 
 def get_fun_with_strftime():
@@ -15,15 +15,15 @@
             "%Y-%m-%d %H:%M:%S"
         )
     return fun_with_strftime
 
 
 def get_fun_with_strftime2():
     import datetime
-    return datetime.datetime.utcnow().strftime('%Y-%m-%d %H:%M:%S')
+    return datetime.datetime.now().strftime('%Y-%m-%d %H:%M:%S')
 
 
 def test_doc_dill_issue_219():
     back_fn = dill.loads(dill.dumps(get_fun_with_strftime()))
     assert back_fn() == "1943-01-04 00:00:00"
     dupl = dill.loads(dill.dumps(get_fun_with_strftime2))
     assert dupl() == get_fun_with_strftime2()
```

### Comparing `dill-0.3.6/dill/tests/test_file.py` & `dill-0.3.7/dill/tests/test_file.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 import os
 import sys
 import string
 import random
```

### Comparing `dill-0.3.6/dill/tests/test_functions.py` & `dill-0.3.7/dill/tests/test_functions.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2019-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2019-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 import functools
 import dill
 import sys
 dill.settings['recurse'] = True
@@ -107,17 +107,20 @@
 assert dill.loads(dumped_func_e)(1, 2, 3) == 9
 assert dill.loads(dumped_func_e)(1, 2, e2=3) == 8
 assert dill.loads(dumped_func_e)(1, 2, e2=3, e3=4) == 10
 assert dill.loads(dumped_func_e)(1, 2, 3, e2=4) == 12
 assert dill.loads(dumped_func_e)(1, 2, 3, e2=4, e3=5) == 15''')
 
 def test_code_object():
+    import warnings
     from dill._dill import ALL_CODE_PARAMS, CODE_PARAMS, CODE_VERSION, _create_code
     code = function_c.__code__
+    warnings.filterwarnings('ignore', category=DeprecationWarning) # issue 597
     LNOTAB = getattr(code, 'co_lnotab', b'')
+    if warnings.filters: del warnings.filters[0]
     fields = {f: getattr(code, 'co_'+f) for f in CODE_PARAMS}
     fields.setdefault('posonlyargcount', 0)         # python >= 3.8
     fields.setdefault('lnotab', LNOTAB)             # python <= 3.9
     fields.setdefault('linetable', b'')             # python >= 3.10
     fields.setdefault('qualname', fields['name'])   # python >= 3.11
     fields.setdefault('exceptiontable', b'')        # python >= 3.11
     fields.setdefault('endlinetable', None)         # python == 3.11a
```

### Comparing `dill-0.3.6/dill/tests/test_functors.py` & `dill-0.3.7/dill/tests/test_functors.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 import functools
 import dill
 dill.settings['recurse'] = True
```

### Comparing `dill-0.3.6/dill/tests/test_logger.py` & `dill-0.3.7/dill/tests/test_logger.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 
 # Author: Leonardo Gama (@leogama)
-# Copyright (c) 2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2022-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 import logging
 import re
 import tempfile
```

### Comparing `dill-0.3.6/dill/tests/test_mixins.py` & `dill-0.3.7/dill/tests/test_mixins.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 import dill
 dill.settings['recurse'] = True
```

### Comparing `dill-0.3.6/dill/tests/test_module.py` & `dill-0.3.7/dill/tests/test_module.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 import sys
 import dill
 import test_mixins as module
 from importlib import reload
```

### Comparing `dill-0.3.6/dill/tests/test_moduledict.py` & `dill-0.3.7/dill/tests/test_moduledict.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 import dill
 dill.settings['recurse'] = True
 
 def f(func):
```

### Comparing `dill-0.3.6/dill/tests/test_nested.py` & `dill-0.3.7/dill/tests/test_nested.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 """
 test dill's ability to handle nested functions
 """
 
 import os
```

### Comparing `dill-0.3.6/dill/tests/test_objects.py` & `dill-0.3.7/dill/tests/test_objects.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 """
 demonstrate dill's ability to pickle different python types
 test pickling of all Python Standard Library objects (currently: CH 1-14 @ 2.7)
 """
```

### Comparing `dill-0.3.6/dill/tests/test_properties.py` & `dill-0.3.7/dill/tests/test_properties.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 import sys
 
 import dill
 dill.settings['recurse'] = True
```

### Comparing `dill-0.3.6/dill/tests/test_pycapsule.py` & `dill-0.3.7/dill/tests/test_pycapsule.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Author: Anirudh Vegesana (avegesan@cs.stanford.edu)
-# Copyright (c) 2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2022-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 """
 test pickling a PyCapsule object
 """
 
 import dill
```

### Comparing `dill-0.3.6/dill/tests/test_recursive.py` & `dill-0.3.7/dill/tests/test_recursive.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2019-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2019-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 import dill
 from functools import partial
 import warnings
```

### Comparing `dill-0.3.6/dill/tests/test_registered.py` & `dill-0.3.7/dill/tests/test_registered.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,7 +1,17 @@
+#!/usr/bin/env python
+#
+# Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
+# Copyright (c) 2022-2023 The Uncertainty Quantification Foundation.
+# License: 3-clause BSD.  The full license text is available at:
+#  - https://github.com/uqfoundation/dill/blob/master/LICENSE
+"""
+test pickling registered objects
+"""
+
 import dill
 from dill._objects import failures, registered, succeeds
 import warnings
 warnings.filterwarnings('ignore')
 
 def check(d, ok=True):
     res = []
```

### Comparing `dill-0.3.6/dill/tests/test_restricted.py` & `dill-0.3.7/dill/tests/test_restricted.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Kirill Makhonin (@kirillmakhonin)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 import dill
 
 class RestrictedType:
     def __bool__(*args, **kwargs):
```

### Comparing `dill-0.3.6/dill/tests/test_selected.py` & `dill-0.3.7/dill/tests/test_selected.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 """
 testing some selected object types
 """
 
 import dill
```

### Comparing `dill-0.3.6/dill/tests/test_session.py` & `dill-0.3.7/dill/tests/test_session.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 
 # Author: Leonardo Gama (@leogama)
-# Copyright (c) 2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2022-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 import atexit
 import os
 import sys
 import __main__
```

### Comparing `dill-0.3.6/dill/tests/test_source.py` & `dill-0.3.7/dill/tests/test_source.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 from dill.source import getsource, getname, _wrap, likely_import
 from dill.source import getimportable
 from dill._dill import IS_PYPY
```

### Comparing `dill-0.3.6/dill/tests/test_temp.py` & `dill-0.3.7/dill/tests/test_temp.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 import sys
 from dill.temp import dump, dump_source, dumpIO, dumpIO_source
 from dill.temp import load, load_source, loadIO, loadIO_source
 WINDOWS = sys.platform[:3] == 'win'
```

### Comparing `dill-0.3.6/dill/tests/test_weakref.py` & `dill-0.3.7/dill/tests/test_weakref.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 import dill
 dill.settings['recurse'] = True
 import weakref
```

### Comparing `dill-0.3.6/dill.egg-info/PKG-INFO` & `dill-0.3.7/dill.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 Metadata-Version: 2.1
 Name: dill
-Version: 0.3.6
-Summary: serialize all of python
+Version: 0.3.7
+Summary: serialize all of Python
 Home-page: https://github.com/uqfoundation/dill
 Download-URL: https://pypi.org/project/dill/#files
 Author: Mike McKerns
 Author-email: mmckerns@uqfoundation.org
 Maintainer: Mike McKerns
 Maintainer-email: mmckerns@uqfoundation.org
 License: BSD-3-Clause
@@ -20,67 +20,68 @@
 Classifier: Intended Audience :: Science/Research
 Classifier: License :: OSI Approved :: BSD License
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Programming Language :: Python :: Implementation :: PyPy
 Classifier: Topic :: Scientific/Engineering
 Classifier: Topic :: Software Development
 Requires-Python: >=3.7
 Provides-Extra: readline
 Provides-Extra: graph
 License-File: LICENSE
 
 -----------------------------
-dill: serialize all of python
+dill: serialize all of Python
 -----------------------------
 
 About Dill
 ==========
 
-``dill`` extends python's ``pickle`` module for serializing and de-serializing
-python objects to the majority of the built-in python types. Serialization
+``dill`` extends Python's ``pickle`` module for serializing and de-serializing
+Python objects to the majority of the built-in Python types. Serialization
 is the process of converting an object to a byte stream, and the inverse
-of which is converting a byte stream back to a python object hierarchy.
+of which is converting a byte stream back to a Python object hierarchy.
 
 ``dill`` provides the user the same interface as the ``pickle`` module, and
-also includes some additional features. In addition to pickling python
+also includes some additional features. In addition to pickling Python
 objects, ``dill`` provides the ability to save the state of an interpreter
 session in a single command.  Hence, it would be feasible to save an
 interpreter session, close the interpreter, ship the pickled file to
 another computer, open a new interpreter, unpickle the session and
 thus continue from the 'saved' state of the original interpreter
 session.
 
-``dill`` can be used to store python objects to a file, but the primary
-usage is to send python objects across the network as a byte stream.
+``dill`` can be used to store Python objects to a file, but the primary
+usage is to send Python objects across the network as a byte stream.
 ``dill`` is quite flexible, and allows arbitrary user defined classes
 and functions to be serialized.  Thus ``dill`` is not intended to be
 secure against erroneously or maliciously constructed data. It is
 left to the user to decide whether the data they unpickle is from
 a trustworthy source.
 
-``dill`` is part of ``pathos``, a python framework for heterogeneous computing.
+``dill`` is part of ``pathos``, a Python framework for heterogeneous computing.
 ``dill`` is in active development, so any user feedback, bug reports, comments,
 or suggestions are highly appreciated.  A list of issues is located at
 https://github.com/uqfoundation/dill/issues, with a legacy list maintained at
 https://uqfoundation.github.io/project/pathos/query.
 
 
 Major Features
 ==============
 
 ``dill`` can pickle the following standard types:
 
     - none, type, bool, int, float, complex, bytes, str,
     - tuple, list, dict, file, buffer, builtin,
-    - python classes, namedtuples, dataclasses, metaclasses,
+    - Python classes, namedtuples, dataclasses, metaclasses,
     - instances of classes,
     - set, frozenset, array, functions, exceptions
 
 ``dill`` can also pickle more 'exotic' standard types:
 
     - functions with yields, nested functions, lambdas,
     - cell, method, unboundmethod, module, code, methodwrapper,
@@ -89,15 +90,15 @@
 
 ``dill`` cannot yet pickle these standard types:
 
     - frame, generator, traceback
 
 ``dill`` also provides the capability to:
 
-    - save and load python interpreter sessions
+    - save and load Python interpreter sessions
     - save and extract the source code from functions and classes
     - interactively diagnose pickling errors
 
 
 Current Release
 ===============
 
@@ -235,15 +236,15 @@
 
 
 More Information
 ================
 
 Probably the best way to get started is to look at the documentation at
 http://dill.rtfd.io. Also see ``dill.tests`` for a set of scripts that
-demonstrate how ``dill`` can serialize different python objects. You can
+demonstrate how ``dill`` can serialize different Python objects. You can
 run the test suite with ``python -m dill.tests``. The contents of any
 pickle file can be examined with ``undill``.  As ``dill`` conforms to
 the ``pickle`` interface, the examples and documentation found at
 http://docs.python.org/library/pickle.html also apply to ``dill``
 if one will ``import dill as pickle``. The source code is also generally
 well documented, so further questions may be resolved by inspecting the
 code itself. Please feel free to submit a ticket on github, or ask a
```

### Comparing `dill-0.3.6/dill.egg-info/SOURCES.txt` & `dill-0.3.7/dill.egg-info/SOURCES.txt`

 * *Files 3% similar despite different names*

```diff
@@ -29,14 +29,15 @@
 dill.egg-info/SOURCES.txt
 dill.egg-info/dependency_links.txt
 dill.egg-info/not-zip-safe
 dill.egg-info/requires.txt
 dill.egg-info/top_level.txt
 dill/tests/__init__.py
 dill/tests/__main__.py
+dill/tests/test_abc.py
 dill/tests/test_check.py
 dill/tests/test_classdef.py
 dill/tests/test_dataclasses.py
 dill/tests/test_detect.py
 dill/tests/test_dictviews.py
 dill/tests/test_diff.py
 dill/tests/test_extendpickle.py
@@ -63,9 +64,11 @@
 docs/Makefile
 docs/requirements.txt
 docs/source/conf.py
 docs/source/dill.rst
 docs/source/index.rst
 docs/source/pathos.png
 docs/source/scripts.rst
+docs/source/_static/css/custom.css
+scripts/get_gprof
 scripts/get_objgraph
 scripts/undill
```

### Comparing `dill-0.3.6/docs/Makefile` & `dill-0.3.7/docs/Makefile`

 * *Files identical despite different names*

### Comparing `dill-0.3.6/docs/source/conf.py` & `dill-0.3.7/docs/source/conf.py`

 * *Files 7% similar despite different names*

```diff
@@ -62,16 +62,34 @@
 year = datetime.now().year
 copyright = '%d, The Uncertainty Quantification Foundation' % year
 author = 'Mike McKerns'
 
 # extension config
 github_project_url = "https://github.com/uqfoundation/dill"
 autoclass_content = 'both'
+autodoc_default_options = {
+    'members': True,
+    'undoc-members': True,
+    'private-members': True,
+    'special-members': True,
+    'show-inheritance': True,
+    'imported-members': True,
+    'exclude-members': ( #NOTE: this is a single string concatenation
+        '__dict__,' # may be verbose
+        '__slots__,'
+        '__weakref__,'
+        '__module__,'
+        '_abc_impl,'
+        '__init__,' # redundant with class docstring by "autoclass_content=both"
+        '__annotations__,' # redundant with signature documentation
+        '__dataclass_fields__,' # redundant automatic attribute
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
@@ -83,15 +101,15 @@
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
@@ -111,57 +129,63 @@
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
     'github_repo': 'dill',
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
 htmlhelp_basename = 'dilldoc'
 
 # Logo for sidebar
@@ -218,15 +242,15 @@
      'Miscellaneous'),
 ]
 
 
 
 
 # Example configuration for intersphinx: refer to the Python standard library.
-intersphinx_mapping = {'https://docs.python.org/': None}
+intersphinx_mapping = {'https://docs.python.org/3/': None}
 #    {'python': {'https://docs.python.org/': None},
 #     'mystic': {'https://mystic.readthedocs.io/en/latest/', None},
 #     'pathos': {'https://pathos.readthedocs.io/en/latest/', None},
 #     'klepto': {'https://klepto.readthedocs.io/en/latest/', None},
 #     'pox': {'https://pox.readthedocs.io/en/latest/', None},
 #     'multiprocess': {'https://multiprocess.readthedocs.io/en/latest/', None},
 #     'ppft': {'https://ppft.readthedocs.io/en/latest/', None},
```

### Comparing `dill-0.3.6/docs/source/pathos.png` & `dill-0.3.7/docs/source/pathos.png`

 * *Files identical despite different names*

### Comparing `dill-0.3.6/scripts/get_objgraph` & `dill-0.3.7/scripts/get_objgraph`

 * *Files 4% similar despite different names*

```diff
@@ -1,26 +1,26 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 """
 display the reference paths for objects in ``dill.types`` or a .pkl file
 
 Notes:
     the generated image is useful in showing the pointer references in
     objects that are or can be pickled.  Any object in ``dill.objects``
     listed in ``dill.load_types(picklable=True, unpicklable=True)`` works.
 
 Examples::
 
-    $ get_objgraph FrameType
-    Image generated as FrameType.png
+    $ get_objgraph ArrayType
+    Image generated as ArrayType.png
 """
 
 import dill as pickle
 #pickle.debug.trace(True)
 #import pickle
 
 # get all objects for testing
```

### Comparing `dill-0.3.6/scripts/undill` & `dill-0.3.7/scripts/undill`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 """
 unpickle the contents of a pickled object file
 
 Examples::
```

### Comparing `dill-0.3.6/setup.py` & `dill-0.3.7/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2016-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 import os
 import sys
 # drop support for older python
 if sys.version_info < (3, 7):
@@ -36,15 +36,15 @@
     Distribution = object
     has_setuptools = False
 
 # build the 'setup' call
 setup_kwds = dict(
     name='dill',
     version=__version__,
-    description='serialize all of python',
+    description='serialize all of Python',
     long_description = README.strip(),
     author = __author__,
     author_email = AUTHOR_EMAIL,
     maintainer = __author__,
     maintainer_email = AUTHOR_EMAIL,
     license = 'BSD-3-Clause',
     platforms = ['Linux', 'Windows', 'Mac'],
@@ -62,22 +62,23 @@
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
     packages = ['dill','dill.tests'],
     package_dir = {'dill':'dill', 'dill.tests':'dill/tests'},
-    scripts=['scripts/undill','scripts/get_objgraph'],
+    scripts=['scripts/undill','scripts/get_objgraph','scripts/get_gprof'],
 )
 
 # force python-, abi-, and platform-specific naming of bdist_wheel
 class BinaryDistribution(Distribution):
     """Distribution which forces a binary package with platform name"""
     def has_ext_modules(foo):
         return True
```

### Comparing `dill-0.3.6/version.py` & `dill-0.3.7/version.py`

 * *Files 16% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2022-2023 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
-__version__ = '0.3.6'
+__version__ = '0.3.7'
 __author__ = 'Mike McKerns'
 __contact__ = 'mmckerns@uqfoundation.org'
 
 
 def get_license_text(filepath):
     "open the LICENSE file and read the contents"
     try:
@@ -36,14 +36,21 @@
                 README += '\n' + line
             elif line.startswith('* with'): #XXX: don't indent
                 README += line
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
@@ -59,15 +66,15 @@
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

