# Comparing `tmp/dill-0.3.5.1.tar.gz` & `tmp/dill-0.3.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dill-0.3.5.1.tar", last modified: Fri May 20 11:18:23 2022, max compression
+gzip compressed data, was "dill-0.3.6.tar", last modified: Sun Oct 23 22:42:44 2022, max compression
```

## Comparing `dill-0.3.5.1.tar` & `dill-0.3.6.tar`

### file list

```diff
@@ -1,71 +1,79 @@
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-05-20 11:18:23.365352 dill-0.3.5.1/
--rw-r--r--   0 mmckerns   (501) staff       (20)      830 2022-05-16 22:40:22.000000 dill-0.3.5.1/.codecov.yml
--rw-r--r--   0 mmckerns   (501) staff       (20)      547 2022-05-16 22:40:22.000000 dill-0.3.5.1/.coveragerc
--rw-r--r--   0 mmckerns   (501) staff       (20)       72 2021-05-27 23:32:52.000000 dill-0.3.5.1/.gitignore
--rw-r--r--   0 mmckerns   (501) staff       (20)      285 2022-05-16 22:40:31.000000 dill-0.3.5.1/.readthedocs.yml
--rw-r--r--   0 mmckerns   (501) staff       (20)     1460 2022-05-16 22:40:22.000000 dill-0.3.5.1/.travis.yml
--rw-r--r--   0 mmckerns   (501) staff       (20)     1790 2022-01-01 16:21:41.000000 dill-0.3.5.1/LICENSE
--rw-r--r--   0 mmckerns   (501) staff       (20)      202 2022-05-16 22:40:22.000000 dill-0.3.5.1/MANIFEST.in
--rw-r--r--   0 mmckerns   (501) staff       (20)     9672 2022-05-20 11:18:23.365608 dill-0.3.5.1/PKG-INFO
--rw-r--r--   0 mmckerns   (501) staff       (20)     9097 2022-05-20 09:43:39.000000 dill-0.3.5.1/README.md
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-05-20 11:18:23.338550 dill-0.3.5.1/dill/
--rw-r--r--   0 mmckerns   (501) staff       (20)     7211 2022-01-01 16:21:41.000000 dill-0.3.5.1/dill/__diff.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    13437 2022-05-20 11:18:01.000000 dill-0.3.5.1/dill/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    81628 2022-05-20 11:00:22.000000 dill-0.3.5.1/dill/_dill.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    20432 2022-01-01 16:21:41.000000 dill-0.3.5.1/dill/_objects.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     9730 2022-03-11 23:59:27.000000 dill-0.3.5.1/dill/_shims.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    12336 2022-05-02 14:56:27.000000 dill-0.3.5.1/dill/detect.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      736 2022-01-01 16:21:41.000000 dill-0.3.5.1/dill/objtypes.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4467 2022-01-01 16:21:41.000000 dill-0.3.5.1/dill/pointers.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      719 2022-01-01 16:21:41.000000 dill-0.3.5.1/dill/settings.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    44917 2022-03-11 23:59:27.000000 dill-0.3.5.1/dill/source.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8242 2022-01-01 16:21:41.000000 dill-0.3.5.1/dill/temp.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-05-20 11:18:23.342417 dill-0.3.5.1/dill.egg-info/
--rw-r--r--   0 mmckerns   (501) staff       (20)     9672 2022-05-20 11:18:22.000000 dill-0.3.5.1/dill.egg-info/PKG-INFO
--rw-r--r--   0 mmckerns   (501) staff       (20)     1206 2022-05-20 11:18:23.000000 dill-0.3.5.1/dill.egg-info/SOURCES.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)        1 2022-05-20 11:18:22.000000 dill-0.3.5.1/dill.egg-info/dependency_links.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)        1 2022-05-20 11:18:21.000000 dill-0.3.5.1/dill.egg-info/not-zip-safe
--rw-r--r--   0 mmckerns   (501) staff       (20)       37 2022-05-20 11:18:23.000000 dill-0.3.5.1/dill.egg-info/requires.txt
--rw-r--r--   0 mmckerns   (501) staff       (20)        5 2022-05-20 11:18:23.000000 dill-0.3.5.1/dill.egg-info/top_level.txt
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-05-20 11:18:23.343883 dill-0.3.5.1/docs/
--rw-r--r--   0 mmckerns   (501) staff       (20)      668 2022-05-16 22:40:22.000000 dill-0.3.5.1/docs/Makefile
--rw-r--r--   0 mmckerns   (501) staff       (20)      430 2022-05-17 16:06:53.000000 dill-0.3.5.1/docs/requirements.txt
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-05-20 11:18:23.347130 dill-0.3.5.1/docs/source/
--rw-r--r--   0 mmckerns   (501) staff       (20)     7360 2018-05-26 15:05:43.000000 dill-0.3.5.1/docs/source/conf.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1581 2018-05-26 15:05:43.000000 dill-0.3.5.1/docs/source/dill.rst
--rw-r--r--   0 mmckerns   (501) staff       (20)      381 2017-08-23 20:54:03.000000 dill-0.3.5.1/docs/source/index.rst
--rw-r--r--   0 mmckerns   (501) staff       (20)    78646 2017-08-11 19:07:27.000000 dill-0.3.5.1/docs/source/pathos.png
--rw-r--r--   0 mmckerns   (501) staff       (20)      215 2018-05-26 15:05:43.000000 dill-0.3.5.1/docs/source/scripts.rst
--rw-r--r--   0 mmckerns   (501) staff       (20)      166 2022-05-20 09:42:48.000000 dill-0.3.5.1/pyproject.toml
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-05-20 11:18:23.348467 dill-0.3.5.1/scripts/
--rw-r--r--   0 mmckerns   (501) staff       (20)     1654 2022-01-01 16:21:41.000000 dill-0.3.5.1/scripts/get_objgraph
--rw-r--r--   0 mmckerns   (501) staff       (20)      590 2022-01-01 16:21:41.000000 dill-0.3.5.1/scripts/undill
--rw-r--r--   0 mmckerns   (501) staff       (20)       76 2022-05-20 11:18:23.366536 dill-0.3.5.1/setup.cfg
--rw-r--r--   0 mmckerns   (501) staff       (20)     5276 2022-05-19 20:57:14.000000 dill-0.3.5.1/setup.py
-drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-05-20 11:18:23.364553 dill-0.3.5.1/tests/
--rw-r--r--   0 mmckerns   (501) staff       (20)      501 2022-01-01 16:21:41.000000 dill-0.3.5.1/tests/__init__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      834 2022-05-01 00:24:37.000000 dill-0.3.5.1/tests/__main__.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1278 2022-01-01 16:21:41.000000 dill-0.3.5.1/tests/test_check.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6944 2022-05-16 22:40:19.000000 dill-0.3.5.1/tests/test_classdef.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4143 2022-05-16 22:40:22.000000 dill-0.3.5.1/tests/test_detect.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1240 2022-04-19 11:54:49.000000 dill-0.3.5.1/tests/test_dictviews.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2761 2022-01-01 16:21:41.000000 dill-0.3.5.1/tests/test_diff.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1368 2022-01-01 16:21:41.000000 dill-0.3.5.1/tests/test_extendpickle.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1679 2022-01-01 16:24:30.000000 dill-0.3.5.1/tests/test_fglobals.py
--rw-r--r--   0 mmckerns   (501) staff       (20)    13642 2022-01-01 16:21:41.000000 dill-0.3.5.1/tests/test_file.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2745 2022-04-22 00:02:22.000000 dill-0.3.5.1/tests/test_functions.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      930 2022-01-01 16:21:41.000000 dill-0.3.5.1/tests/test_functors.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4007 2022-01-01 16:21:41.000000 dill-0.3.5.1/tests/test_mixins.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1973 2022-01-01 16:21:41.000000 dill-0.3.5.1/tests/test_module.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1182 2022-01-01 16:21:41.000000 dill-0.3.5.1/tests/test_moduledict.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     3134 2022-01-01 16:21:41.000000 dill-0.3.5.1/tests/test_nested.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1779 2022-01-01 16:21:41.000000 dill-0.3.5.1/tests/test_objects.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     1346 2022-01-01 16:21:41.000000 dill-0.3.5.1/tests/test_properties.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     4209 2022-04-19 11:32:42.000000 dill-0.3.5.1/tests/test_recursive.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      783 2022-01-01 16:21:41.000000 dill-0.3.5.1/tests/test_restricted.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2533 2022-03-11 23:59:27.000000 dill-0.3.5.1/tests/test_selected.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     8741 2022-05-01 00:24:37.000000 dill-0.3.5.1/tests/test_session.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     6375 2022-01-01 16:21:41.000000 dill-0.3.5.1/tests/test_source.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2619 2022-01-01 16:21:41.000000 dill-0.3.5.1/tests/test_temp.py
--rw-r--r--   0 mmckerns   (501) staff       (20)     2056 2022-01-01 16:21:41.000000 dill-0.3.5.1/tests/test_weakref.py
--rw-r--r--   0 mmckerns   (501) staff       (20)      446 2022-05-16 22:40:22.000000 dill-0.3.5.1/tox.ini
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-23 22:42:44.267064 dill-0.3.6/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      830 2022-06-16 10:40:20.000000 dill-0.3.6/.codecov.yml
+-rw-r--r--   0 mmckerns   (501) staff       (20)      547 2022-06-16 10:40:20.000000 dill-0.3.6/.coveragerc
+-rw-r--r--   0 mmckerns   (501) staff       (20)       77 2022-07-15 14:15:24.000000 dill-0.3.6/.gitignore
+-rw-r--r--   0 mmckerns   (501) staff       (20)      285 2022-06-16 10:40:20.000000 dill-0.3.6/.readthedocs.yml
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1232 2022-07-21 23:42:50.000000 dill-0.3.6/.travis.yml
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1790 2022-01-01 16:21:41.000000 dill-0.3.6/LICENSE
+-rw-r--r--   0 mmckerns   (501) staff       (20)      203 2022-07-06 21:36:08.000000 dill-0.3.6/MANIFEST.in
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9794 2022-10-23 22:42:44.267372 dill-0.3.6/PKG-INFO
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9387 2022-07-01 23:07:22.000000 dill-0.3.6/README.md
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-23 22:42:44.226005 dill-0.3.6/dill/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7143 2022-07-01 23:07:22.000000 dill-0.3.6/dill/__diff.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10612 2022-10-23 22:42:44.000000 dill-0.3.6/dill/__info__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3797 2022-07-23 11:04:42.000000 dill-0.3.6/dill/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    82292 2022-08-13 19:10:17.000000 dill-0.3.6/dill/_dill.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    19368 2022-08-13 17:48:35.000000 dill-0.3.6/dill/_objects.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6635 2022-07-01 23:07:22.000000 dill-0.3.6/dill/_shims.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11091 2022-07-01 23:07:22.000000 dill-0.3.6/dill/detect.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    11079 2022-08-13 19:10:17.000000 dill-0.3.6/dill/logger.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      736 2022-01-01 16:21:41.000000 dill-0.3.6/dill/objtypes.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4467 2022-01-01 16:21:41.000000 dill-0.3.6/dill/pointers.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    22500 2022-08-13 19:20:16.000000 dill-0.3.6/dill/session.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      630 2022-07-01 23:07:22.000000 dill-0.3.6/dill/settings.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    45121 2022-07-29 22:46:00.000000 dill-0.3.6/dill/source.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     8027 2022-10-20 20:14:57.000000 dill-0.3.6/dill/temp.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-23 22:42:44.257875 dill-0.3.6/dill/tests/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      501 2022-06-26 12:33:37.000000 dill-0.3.6/dill/tests/__init__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      899 2022-07-08 23:41:28.000000 dill-0.3.6/dill/tests/__main__.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1396 2022-07-01 23:07:22.000000 dill-0.3.6/dill/tests/test_check.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6100 2022-08-13 19:10:17.000000 dill-0.3.6/dill/tests/test_classdef.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      885 2022-07-21 21:10:27.000000 dill-0.3.6/dill/tests/test_dataclasses.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4083 2022-07-01 23:07:22.000000 dill-0.3.6/dill/tests/test_detect.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1337 2022-06-26 12:33:37.000000 dill-0.3.6/dill/tests/test_dictviews.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2667 2022-07-01 23:07:22.000000 dill-0.3.6/dill/tests/test_diff.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1315 2022-07-01 23:07:22.000000 dill-0.3.6/dill/tests/test_extendpickle.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1679 2022-06-26 12:33:37.000000 dill-0.3.6/dill/tests/test_fglobals.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    13578 2022-07-01 23:07:22.000000 dill-0.3.6/dill/tests/test_file.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4119 2022-07-03 10:49:48.000000 dill-0.3.6/dill/tests/test_functions.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      930 2022-06-26 12:33:37.000000 dill-0.3.6/dill/tests/test_functors.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2380 2022-07-01 21:02:52.000000 dill-0.3.6/dill/tests/test_logger.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4007 2022-06-26 12:33:37.000000 dill-0.3.6/dill/tests/test_mixins.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1943 2022-07-01 23:07:22.000000 dill-0.3.6/dill/tests/test_module.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1182 2022-06-26 12:33:37.000000 dill-0.3.6/dill/tests/test_moduledict.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3146 2022-07-01 23:07:22.000000 dill-0.3.6/dill/tests/test_nested.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1834 2022-06-26 12:33:37.000000 dill-0.3.6/dill/tests/test_objects.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1346 2022-06-26 12:33:37.000000 dill-0.3.6/dill/tests/test_properties.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1412 2022-06-26 12:33:37.000000 dill-0.3.6/dill/tests/test_pycapsule.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4182 2022-07-01 23:07:22.000000 dill-0.3.6/dill/tests/test_recursive.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1250 2022-07-21 23:06:24.000000 dill-0.3.6/dill/tests/test_registered.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      783 2022-06-26 12:33:37.000000 dill-0.3.6/dill/tests/test_restricted.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     3218 2022-07-23 23:12:59.000000 dill-0.3.6/dill/tests/test_selected.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)    10156 2022-07-23 11:04:42.000000 dill-0.3.6/dill/tests/test_session.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     6036 2022-07-01 23:07:22.000000 dill-0.3.6/dill/tests/test_source.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2619 2022-06-26 12:33:37.000000 dill-0.3.6/dill/tests/test_temp.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1602 2022-08-13 19:10:17.000000 dill-0.3.6/dill/tests/test_weakref.py
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-23 22:42:44.230320 dill-0.3.6/dill.egg-info/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     9794 2022-10-23 22:42:44.000000 dill-0.3.6/dill.egg-info/PKG-INFO
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1506 2022-10-23 22:42:44.000000 dill-0.3.6/dill.egg-info/SOURCES.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)        1 2022-10-23 22:42:44.000000 dill-0.3.6/dill.egg-info/dependency_links.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)        1 2022-10-23 22:42:43.000000 dill-0.3.6/dill.egg-info/not-zip-safe
+-rw-r--r--   0 mmckerns   (501) staff       (20)       37 2022-10-23 22:42:44.000000 dill-0.3.6/dill.egg-info/requires.txt
+-rw-r--r--   0 mmckerns   (501) staff       (20)        5 2022-10-23 22:42:44.000000 dill-0.3.6/dill.egg-info/top_level.txt
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-23 22:42:44.259294 dill-0.3.6/docs/
+-rw-r--r--   0 mmckerns   (501) staff       (20)      668 2022-06-16 10:40:20.000000 dill-0.3.6/docs/Makefile
+-rw-r--r--   0 mmckerns   (501) staff       (20)      430 2022-06-16 10:40:20.000000 dill-0.3.6/docs/requirements.txt
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-23 22:42:44.264111 dill-0.3.6/docs/source/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     7387 2022-07-06 21:37:37.000000 dill-0.3.6/docs/source/conf.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2020 2022-07-23 11:04:42.000000 dill-0.3.6/docs/source/dill.rst
+-rw-r--r--   0 mmckerns   (501) staff       (20)      381 2017-08-23 20:54:03.000000 dill-0.3.6/docs/source/index.rst
+-rw-r--r--   0 mmckerns   (501) staff       (20)    78646 2017-08-11 19:07:27.000000 dill-0.3.6/docs/source/pathos.png
+-rw-r--r--   0 mmckerns   (501) staff       (20)      215 2018-05-26 15:05:43.000000 dill-0.3.6/docs/source/scripts.rst
+-rw-r--r--   0 mmckerns   (501) staff       (20)      166 2022-06-16 10:40:20.000000 dill-0.3.6/pyproject.toml
+drwxr-xr-x   0 mmckerns   (501) staff       (20)        0 2022-10-23 22:42:44.266217 dill-0.3.6/scripts/
+-rw-r--r--   0 mmckerns   (501) staff       (20)     1654 2022-01-01 16:21:41.000000 dill-0.3.6/scripts/get_objgraph
+-rw-r--r--   0 mmckerns   (501) staff       (20)      590 2022-01-01 16:21:41.000000 dill-0.3.6/scripts/undill
+-rw-r--r--   0 mmckerns   (501) staff       (20)       62 2022-10-23 22:42:44.268483 dill-0.3.6/setup.cfg
+-rw-r--r--   0 mmckerns   (501) staff       (20)     4333 2022-08-10 11:31:11.000000 dill-0.3.6/setup.py
+-rw-r--r--   0 mmckerns   (501) staff       (20)      274 2022-07-09 10:40:26.000000 dill-0.3.6/tox.ini
+-rw-r--r--   0 mmckerns   (501) staff       (20)     2825 2022-10-23 22:42:13.000000 dill-0.3.6/version.py
```

### Comparing `dill-0.3.5.1/.codecov.yml` & `dill-0.3.6/.codecov.yml`

 * *Files identical despite different names*

### Comparing `dill-0.3.5.1/.coveragerc` & `dill-0.3.6/.coveragerc`

 * *Files identical despite different names*

### Comparing `dill-0.3.5.1/.travis.yml` & `dill-0.3.6/.travis.yml`

 * *Files 20% similar despite different names*

```diff
@@ -1,17 +1,12 @@
 dist: focal
 language: python
 
 matrix:
     include:
-        - python: '2.7'
-          dist: bionic
-          env:
-            - COVERAGE="true"
-
         - python: '3.7'
           env:
 
         - python: '3.8'
           env:
 
         - python: '3.9'
@@ -21,25 +16,19 @@
 
         - python: '3.10'
           env:
 
         - python: '3.11-dev'
           env:
 
-        - python: 'pypy2.7-7.3.1' # most recent
-          dist: xenial
-          env:
-
         - python: 'pypy3.7-7.3.5' # most recent
           dist: bionic
           env:
 
     allow_failures:
-        - python: '2.7'
-        - python: 'pypy2.7-7.3.1'
         - python: '3.11-dev'
     fast_finish: true
 
 cache:
     pip: true
 
 before_install:
@@ -47,13 +36,13 @@
     - if [[ $COVERAGE == "true" ]]; then pip install coverage; fi
     - if [[ $NUMPY == "true" ]]; then pip install numpy; fi
 
 install:
     - python -m pip install .
 
 script:
-    - for test in tests/__init__.py; do echo $test ; if [[ $COVERAGE == "true" ]]; then coverage run -a $test > /dev/null; else python $test > /dev/null; fi ; done
-    - for test in tests/test_*.py; do echo $test ; if [[ $COVERAGE == "true" ]]; then coverage run -a $test > /dev/null; else python $test > /dev/null; fi ; done
+    - for test in dill/tests/__init__.py; do echo $test ; if [[ $COVERAGE == "true" ]]; then coverage run -a $test > /dev/null; else python $test > /dev/null; fi ; done
+    - for test in dill/tests/test_*.py; do echo $test ; if [[ $COVERAGE == "true" ]]; then coverage run -a $test > /dev/null; else python $test > /dev/null; fi ; done
 
 after_success:
     - if [[ $COVERAGE == "true" ]]; then bash <(curl -s https://codecov.io/bash); else echo ''; fi
     - if [[ $COVERAGE == "true" ]]; then coverage report; fi
```

### Comparing `dill-0.3.5.1/LICENSE` & `dill-0.3.6/LICENSE`

 * *Files identical despite different names*

### Comparing `dill-0.3.5.1/PKG-INFO` & `dill-0.3.6/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,40 +1,38 @@
 Metadata-Version: 2.1
 Name: dill
-Version: 0.3.5.1
+Version: 0.3.6
 Summary: serialize all of python
 Home-page: https://github.com/uqfoundation/dill
 Download-URL: https://pypi.org/project/dill/#files
 Author: Mike McKerns
 Author-email: mmckerns@uqfoundation.org
 Maintainer: Mike McKerns
 Maintainer-email: mmckerns@uqfoundation.org
-License: 3-clause BSD
+License: BSD-3-Clause
 Project-URL: Documentation, http://dill.rtfd.io
 Project-URL: Source Code, https://github.com/uqfoundation/dill
 Project-URL: Bug Tracker, https://github.com/uqfoundation/dill/issues
 Platform: Linux
 Platform: Windows
 Platform: Mac
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Developers
 Classifier: Intended Audience :: Science/Research
 Classifier: License :: OSI Approved :: BSD License
-Classifier: Programming Language :: Python :: 2
-Classifier: Programming Language :: Python :: 2.7
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Programming Language :: Python :: Implementation :: PyPy
 Classifier: Topic :: Scientific/Engineering
 Classifier: Topic :: Software Development
-Requires-Python: >=2.7, !=3.0.*, !=3.1.*, !=3.2.*, !=3.3.*, !=3.4.*, !=3.5.*, !=3.6.*
+Requires-Python: >=3.7
 Provides-Extra: readline
 Provides-Extra: graph
 License-File: LICENSE
 
 -----------------------------
 dill: serialize all of python
 -----------------------------
@@ -46,15 +44,15 @@
 python objects to the majority of the built-in python types. Serialization
 is the process of converting an object to a byte stream, and the inverse
 of which is converting a byte stream back to a python object hierarchy.
 
 ``dill`` provides the user the same interface as the ``pickle`` module, and
 also includes some additional features. In addition to pickling python
 objects, ``dill`` provides the ability to save the state of an interpreter
-session in a single command.  Hence, it would be feasable to save an
+session in a single command.  Hence, it would be feasible to save an
 interpreter session, close the interpreter, ship the pickled file to
 another computer, open a new interpreter, unpickle the session and
 thus continue from the 'saved' state of the original interpreter
 session.
 
 ``dill`` can be used to store python objects to a file, but the primary
 usage is to send python objects across the network as a byte stream.
@@ -62,35 +60,36 @@
 and functions to be serialized.  Thus ``dill`` is not intended to be
 secure against erroneously or maliciously constructed data. It is
 left to the user to decide whether the data they unpickle is from
 a trustworthy source.
 
 ``dill`` is part of ``pathos``, a python framework for heterogeneous computing.
 ``dill`` is in active development, so any user feedback, bug reports, comments,
-or suggestions are highly appreciated.  A list of issues is located at https://github.com/uqfoundation/dill/issues, with a legacy list maintained at https://uqfoundation.github.io/project/pathos/query.
+or suggestions are highly appreciated.  A list of issues is located at
+https://github.com/uqfoundation/dill/issues, with a legacy list maintained at
+https://uqfoundation.github.io/project/pathos/query.
 
 
 Major Features
 ==============
 
 ``dill`` can pickle the following standard types:
 
-    - none, type, bool, int, long, float, complex, str, unicode,
+    - none, type, bool, int, float, complex, bytes, str,
     - tuple, list, dict, file, buffer, builtin,
-    - both old and new style classes,
-    - instances of old and new style classes,
+    - python classes, namedtuples, dataclasses, metaclasses,
+    - instances of classes,
     - set, frozenset, array, functions, exceptions
 
 ``dill`` can also pickle more 'exotic' standard types:
 
     - functions with yields, nested functions, lambdas,
     - cell, method, unboundmethod, module, code, methodwrapper,
-    - dictproxy, methoddescriptor, getsetdescriptor, memberdescriptor,
-    - wrapperdescriptor, xrange, slice,
-    - notimplemented, ellipsis, quit
+    - methoddescriptor, getsetdescriptor, memberdescriptor, wrapperdescriptor,
+    - dictproxy, slice, notimplemented, ellipsis, quit
 
 ``dill`` cannot yet pickle these standard types:
 
     - frame, generator, traceback
 
 ``dill`` also provides the capability to:
 
@@ -136,15 +135,15 @@
 
 
 Requirements
 ============
 
 ``dill`` requires:
 
-    - ``python`` (or ``pypy``), **==2.7** or **>=3.7**
+    - ``python`` (or ``pypy``), **>=3.7**
     - ``setuptools``, **>=42**
 
 Optional requirements:
 
     - ``objgraph``, **>=1.7.2**
     - ``pyreadline``, **>=1.7.1** (on windows)
 
@@ -168,15 +167,15 @@
     >>> loads(dumps(squared))(3)
     9
 
 There are a number of options to control serialization which are provided
 as keyword arguments to several ``dill`` functions:
 
 * with *protocol*, the pickle protocol level can be set. This uses the
-  same value as the ``pickle`` module, *HIGHEST_PROTOCOL* or *DEFAULT_PROTOCOL*.
+  same value as the ``pickle`` module, *DEFAULT_PROTOCOL*.
 * with *byref=True*, ``dill`` to behave a lot more like pickle with
   certain objects (like modules) pickled by reference as opposed to
   attempting to pickle the object itself.
 * with *recurse=True*, objects referred to in the global dictionary are
   recursively traced and pickled, instead of the default behavior of
   attempting to store the entire global dictionary.
 * with *fmode*, the contents of the file can be pickled along with the file
@@ -205,34 +204,38 @@
     >>> print(dill.source.getsource(squared))
     squared = lambda x:x**2
 
 To aid in debugging pickling issues, use *dill.detect* which provides
 tools like pickle tracing::
 
     >>> import dill.detect
-    >>> dill.detect.trace(True)
-    >>> f = dumps(squared)
-    F1: <function <lambda> at 0x108899e18>
-    F2: <function _create_function at 0x108db7488>
-    # F2
-    Co: <code object <lambda> at 0x10866a270, file "<stdin>", line 1>
-    F2: <function _create_code at 0x108db7510>
-    # F2
-    # Co
-    D1: <dict object at 0x10862b3f0>
-    # D1
-    D2: <dict object at 0x108e42ee8>
-    # D2
-    # F1
-    >>> dill.detect.trace(False)
+    >>> with dill.detect.trace():
+    >>>     dumps(squared)
+    ┬ F1: <function <lambda> at 0x7fe074f8c280>
+    ├┬ F2: <function _create_function at 0x7fe074c49c10>
+    │└ # F2 [34 B]
+    ├┬ Co: <code object <lambda> at 0x7fe07501eb30, file "<stdin>", line 1>
+    │├┬ F2: <function _create_code at 0x7fe074c49ca0>
+    ││└ # F2 [19 B]
+    │└ # Co [87 B]
+    ├┬ D1: <dict object at 0x7fe0750d4680>
+    │└ # D1 [22 B]
+    ├┬ D2: <dict object at 0x7fe074c5a1c0>
+    │└ # D2 [2 B]
+    ├┬ D2: <dict object at 0x7fe074f903c0>
+    │├┬ D2: <dict object at 0x7fe074f8ebc0>
+    ││└ # D2 [2 B]
+    │└ # D2 [23 B]
+    └ # F1 [180 B]
 
 With trace, we see how ``dill`` stored the lambda (``F1``) by first storing
 ``_create_function``, the underlying code object (``Co``) and ``_create_code``
 (which is used to handle code objects), then we handle the reference to
-the global dict (``D2``).  A ``#`` marks when the object is actually stored.
+the global dict (``D2``) plus other dictionaries (``D1`` and ``D2``) that
+save the lambda object's state. A ``#`` marks when the object is actually stored.
 
 
 More Information
 ================
 
 Probably the best way to get started is to look at the documentation at
 http://dill.rtfd.io. Also see ``dill.tests`` for a set of scripts that
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `dill-0.3.5.1/README.md` & `dill-0.3.6/README.md`

 * *Files 5% similar despite different names*

```diff
@@ -24,34 +24,35 @@
 and functions to be serialized.  Thus ``dill`` is not intended to be
 secure against erroneously or maliciously constructed data. It is
 left to the user to decide whether the data they unpickle is from
 a trustworthy source.
 
 ``dill`` is part of ``pathos``, a python framework for heterogeneous computing.
 ``dill`` is in active development, so any user feedback, bug reports, comments,
-or suggestions are highly appreciated.  A list of issues is located at https://github.com/uqfoundation/dill/issues, with a legacy list maintained at https://uqfoundation.github.io/project/pathos/query.
+or suggestions are highly appreciated.  A list of issues is located at
+https://github.com/uqfoundation/dill/issues, with a legacy list maintained at
+https://uqfoundation.github.io/project/pathos/query.
 
 
 Major Features
 --------------
 ``dill`` can pickle the following standard types:
 
-* none, type, bool, int, long, float, complex, str, unicode,
+* none, type, bool, int, float, complex, bytes, str,
 * tuple, list, dict, file, buffer, builtin,
-* both old and new style classes,
-* instances of old and new style classes,
+* python classes, namedtuples, dataclasses, metaclasses,
+* instances of classes,
 * set, frozenset, array, functions, exceptions
 
 ``dill`` can also pickle more 'exotic' standard types:
 
-* functions with yields, nested functions, lambdas
+* functions with yields, nested functions, lambdas,
 * cell, method, unboundmethod, module, code, methodwrapper,
-* dictproxy, methoddescriptor, getsetdescriptor, memberdescriptor,
-* wrapperdescriptor, xrange, slice,
-* notimplemented, ellipsis, quit
+* methoddescriptor, getsetdescriptor, memberdescriptor, wrapperdescriptor,
+* dictproxy, slice, notimplemented, ellipsis, quit
 
 ``dill`` cannot yet pickle these standard types:
 
 * frame, generator, traceback
 
 ``dill`` also provides the capability to:
 
@@ -98,15 +99,15 @@
     $ pip install dill[readline]
 
 
 Requirements
 ------------
 ``dill`` requires:
 
-* ``python`` (or ``pypy``), **==2.7** or **>=3.7**
+* ``python`` (or ``pypy``), **>=3.7**
 * ``setuptools``, **>=42**
 
 Optional requirements:
 
 * ``objgraph``, **>=1.7.2**
 * ``pyreadline``, **>=1.7.1** (on windows)
 
@@ -129,15 +130,15 @@
     >>> loads(dumps(squared))(3)
     9
 
 There are a number of options to control serialization which are provided
 as keyword arguments to several ``dill`` functions:
 
 * with *protocol*, the pickle protocol level can be set. This uses the
-  same value as the ``pickle`` module, *HIGHEST_PROTOCOL* or *DEFAULT_PROTOCOL*.
+  same value as the ``pickle`` module, *DEFAULT_PROTOCOL*.
 * with *byref=True*, ``dill`` to behave a lot more like pickle with
   certain objects (like modules) pickled by reference as opposed to
   attempting to pickle the object itself.
 * with *recurse=True*, objects referred to in the global dictionary are
   recursively traced and pickled, instead of the default behavior of
   attempting to store the entire global dictionary.
 * with *fmode*, the contents of the file can be pickled along with the file
@@ -166,34 +167,38 @@
     >>> print(dill.source.getsource(squared))
     squared = lambda x:x**2
 
 To aid in debugging pickling issues, use *dill.detect* which provides
 tools like pickle tracing::
 
     >>> import dill.detect
-    >>> dill.detect.trace(True)
-    >>> f = dumps(squared)
-    F1: <function <lambda> at 0x108899e18>
-    F2: <function _create_function at 0x108db7488>
-    # F2
-    Co: <code object <lambda> at 0x10866a270, file "<stdin>", line 1>
-    F2: <function _create_code at 0x108db7510>
-    # F2
-    # Co
-    D1: <dict object at 0x10862b3f0>
-    # D1
-    D2: <dict object at 0x108e42ee8>
-    # D2
-    # F1
-    >>> dill.detect.trace(False)
+    >>> with dill.detect.trace():
+    >>>     dumps(squared)
+    ┬ F1: <function <lambda> at 0x7fe074f8c280>
+    ├┬ F2: <function _create_function at 0x7fe074c49c10>
+    │└ # F2 [34 B]
+    ├┬ Co: <code object <lambda> at 0x7fe07501eb30, file "<stdin>", line 1>
+    │├┬ F2: <function _create_code at 0x7fe074c49ca0>
+    ││└ # F2 [19 B]
+    │└ # Co [87 B]
+    ├┬ D1: <dict object at 0x7fe0750d4680>
+    │└ # D1 [22 B]
+    ├┬ D2: <dict object at 0x7fe074c5a1c0>
+    │└ # D2 [2 B]
+    ├┬ D2: <dict object at 0x7fe074f903c0>
+    │├┬ D2: <dict object at 0x7fe074f8ebc0>
+    ││└ # D2 [2 B]
+    │└ # D2 [23 B]
+    └ # F1 [180 B]
 
 With trace, we see how ``dill`` stored the lambda (``F1``) by first storing
 ``_create_function``, the underlying code object (``Co``) and ``_create_code``
 (which is used to handle code objects), then we handle the reference to
-the global dict (``D2``).  A ``#`` marks when the object is actually stored.
+the global dict (``D2``) plus other dictionaries (``D1`` and ``D2``) that
+save the lambda object's state. A ``#`` marks when the object is actually stored.
 
 
 More Information
 ----------------
 Probably the best way to get started is to look at the documentation at
 http://dill.rtfd.io. Also see ``dill.tests`` for a set of scripts that
 demonstrate how ``dill`` can serialize different python objects. You can
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `dill-0.3.5.1/dill/__diff.py` & `dill-0.3.6/dill/__diff.py`

 * *Files 5% similar despite different names*

```diff
@@ -6,26 +6,23 @@
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 """
 Module to show if an object has changed since it was memorised
 """
 
+import builtins
 import os
 import sys
 import types
 try:
     import numpy
     HAS_NUMPY = True
-except:
-    HAS_NUMPY = False
-try:
-    import builtins
 except ImportError:
-    import __builtin__ as builtins
+    HAS_NUMPY = False
 
 # pypy doesn't use reference counting
 getrefcount = getattr(sys, 'getrefcount', lambda x:0)
 
 # memo of objects indexed by id to a tuple (attributes, sequence items)
 # attributes is a dict indexed by attribute name to attribute id
 # sequence items is either a list of ids, of a dictionary of keys to ids
@@ -40,18 +37,15 @@
 def get_attrs(obj):
     """
     Gets all the attributes of an object though its __dict__ or return None
     """
     if type(obj) in builtins_types \
        or type(obj) is type and obj in builtins_types:
         return
-    try:
-        return obj.__dict__
-    except:
-        return
+    return getattr(obj, '__dict__', None)
 
 
 def get_seq(obj, cache={str: False, frozenset: False, list: True, set: True,
                         dict: True, tuple: True, type: False,
                         types.ModuleType: False, types.FunctionType: False,
                         types.BuiltinFunctionType: False}):
     """
@@ -231,10 +225,10 @@
 
 builtins.__import__ = _imp
 if hasattr(builtins, "_"):
     del builtins._
 
 # memorise all already imported modules. This implies that this must be
 # imported first for any changes to be recorded
-for mod in sys.modules.values():
+for mod in list(sys.modules.values()):
     memorise(mod)
 release_gone()
```

### Comparing `dill-0.3.5.1/dill/__init__.py` & `dill-0.3.6/dill/__info__.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,20 +1,14 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
+# Copyright (c) 2022 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
-
-# author, version, license, and long description
-__version__ = '0.3.5.1'
-__author__ = 'Mike McKerns'
-
-__doc__ = """
+'''
 -----------------------------
 dill: serialize all of python
 -----------------------------
 
 About Dill
 ==========
 
@@ -22,15 +16,15 @@
 python objects to the majority of the built-in python types. Serialization
 is the process of converting an object to a byte stream, and the inverse
 of which is converting a byte stream back to a python object hierarchy.
 
 ``dill`` provides the user the same interface as the ``pickle`` module, and
 also includes some additional features. In addition to pickling python
 objects, ``dill`` provides the ability to save the state of an interpreter
-session in a single command.  Hence, it would be feasable to save an
+session in a single command.  Hence, it would be feasible to save an
 interpreter session, close the interpreter, ship the pickled file to
 another computer, open a new interpreter, unpickle the session and
 thus continue from the 'saved' state of the original interpreter
 session.
 
 ``dill`` can be used to store python objects to a file, but the primary
 usage is to send python objects across the network as a byte stream.
@@ -38,35 +32,36 @@
 and functions to be serialized.  Thus ``dill`` is not intended to be
 secure against erroneously or maliciously constructed data. It is
 left to the user to decide whether the data they unpickle is from
 a trustworthy source.
 
 ``dill`` is part of ``pathos``, a python framework for heterogeneous computing.
 ``dill`` is in active development, so any user feedback, bug reports, comments,
-or suggestions are highly appreciated.  A list of issues is located at https://github.com/uqfoundation/dill/issues, with a legacy list maintained at https://uqfoundation.github.io/project/pathos/query.
+or suggestions are highly appreciated.  A list of issues is located at
+https://github.com/uqfoundation/dill/issues, with a legacy list maintained at
+https://uqfoundation.github.io/project/pathos/query.
 
 
 Major Features
 ==============
 
 ``dill`` can pickle the following standard types:
 
-    - none, type, bool, int, long, float, complex, str, unicode,
+    - none, type, bool, int, float, complex, bytes, str,
     - tuple, list, dict, file, buffer, builtin,
-    - both old and new style classes,
-    - instances of old and new style classes,
+    - python classes, namedtuples, dataclasses, metaclasses,
+    - instances of classes,
     - set, frozenset, array, functions, exceptions
 
 ``dill`` can also pickle more 'exotic' standard types:
 
     - functions with yields, nested functions, lambdas,
     - cell, method, unboundmethod, module, code, methodwrapper,
-    - dictproxy, methoddescriptor, getsetdescriptor, memberdescriptor,
-    - wrapperdescriptor, xrange, slice,
-    - notimplemented, ellipsis, quit
+    - methoddescriptor, getsetdescriptor, memberdescriptor, wrapperdescriptor,
+    - dictproxy, slice, notimplemented, ellipsis, quit
 
 ``dill`` cannot yet pickle these standard types:
 
     - frame, generator, traceback
 
 ``dill`` also provides the capability to:
 
@@ -112,15 +107,15 @@
 
 
 Requirements
 ============
 
 ``dill`` requires:
 
-    - ``python`` (or ``pypy``), **==2.7** or **>=3.7**
+    - ``python`` (or ``pypy``), **>=3.7**
     - ``setuptools``, **>=42**
 
 Optional requirements:
 
     - ``objgraph``, **>=1.7.2**
     - ``pyreadline``, **>=1.7.1** (on windows)
 
@@ -144,15 +139,15 @@
     >>> loads(dumps(squared))(3)
     9
 
 There are a number of options to control serialization which are provided
 as keyword arguments to several ``dill`` functions:
 
 * with *protocol*, the pickle protocol level can be set. This uses the
-  same value as the ``pickle`` module, *HIGHEST_PROTOCOL* or *DEFAULT_PROTOCOL*.
+  same value as the ``pickle`` module, *DEFAULT_PROTOCOL*.
 * with *byref=True*, ``dill`` to behave a lot more like pickle with
   certain objects (like modules) pickled by reference as opposed to
   attempting to pickle the object itself.
 * with *recurse=True*, objects referred to in the global dictionary are
   recursively traced and pickled, instead of the default behavior of
   attempting to store the entire global dictionary.
 * with *fmode*, the contents of the file can be pickled along with the file
@@ -181,34 +176,38 @@
     >>> print(dill.source.getsource(squared))
     squared = lambda x:x**2
 
 To aid in debugging pickling issues, use *dill.detect* which provides
 tools like pickle tracing::
 
     >>> import dill.detect
-    >>> dill.detect.trace(True)
-    >>> f = dumps(squared)
-    F1: <function <lambda> at 0x108899e18>
-    F2: <function _create_function at 0x108db7488>
-    # F2
-    Co: <code object <lambda> at 0x10866a270, file "<stdin>", line 1>
-    F2: <function _create_code at 0x108db7510>
-    # F2
-    # Co
-    D1: <dict object at 0x10862b3f0>
-    # D1
-    D2: <dict object at 0x108e42ee8>
-    # D2
-    # F1
-    >>> dill.detect.trace(False)
+    >>> with dill.detect.trace():
+    >>>     dumps(squared)
+    ┬ F1: <function <lambda> at 0x7fe074f8c280>
+    ├┬ F2: <function _create_function at 0x7fe074c49c10>
+    │└ # F2 [34 B]
+    ├┬ Co: <code object <lambda> at 0x7fe07501eb30, file "<stdin>", line 1>
+    │├┬ F2: <function _create_code at 0x7fe074c49ca0>
+    ││└ # F2 [19 B]
+    │└ # Co [87 B]
+    ├┬ D1: <dict object at 0x7fe0750d4680>
+    │└ # D1 [22 B]
+    ├┬ D2: <dict object at 0x7fe074c5a1c0>
+    │└ # D2 [2 B]
+    ├┬ D2: <dict object at 0x7fe074f903c0>
+    │├┬ D2: <dict object at 0x7fe074f8ebc0>
+    ││└ # D2 [2 B]
+    │└ # D2 [23 B]
+    └ # F1 [180 B]
 
 With trace, we see how ``dill`` stored the lambda (``F1``) by first storing
 ``_create_function``, the underlying code object (``Co``) and ``_create_code``
 (which is used to handle code objects), then we handle the reference to
-the global dict (``D2``).  A ``#`` marks when the object is actually stored.
+the global dict (``D2``) plus other dictionaries (``D1`` and ``D2``) that
+save the lambda object's state. A ``#`` marks when the object is actually stored.
 
 
 More Information
 ================
 
 Probably the best way to get started is to look at the documentation at
 http://dill.rtfd.io. Also see ``dill.tests`` for a set of scripts that
@@ -239,17 +238,20 @@
     Michael McKerns and Michael Aivazis,
     "pathos: a framework for heterogeneous computing", 2010- ;
     https://uqfoundation.github.io/project/pathos
 
 Please see https://uqfoundation.github.io/project/pathos or
 http://arxiv.org/pdf/1202.1056 for further information.
 
-"""
+'''
 
-__license__ = """
+__version__ = '0.3.6'
+__author__ = 'Mike McKerns'
+
+__license__ = '''
 Copyright (c) 2004-2016 California Institute of Technology.
 Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
 All rights reserved.
 
 This software is available subject to the conditions and terms laid
 out below. By downloading and using this software you are agreeing
 to the following conditions.
@@ -277,113 +279,8 @@
 EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO,
 PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS;
 OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY,
 WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR
 OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF
 ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
 
-"""
-
-from ._dill import dump, dumps, load, loads, dump_session, load_session, \
-    Pickler, Unpickler, register, copy, pickle, pickles, check, \
-    HIGHEST_PROTOCOL, DEFAULT_PROTOCOL, PicklingError, UnpicklingError, \
-    HANDLE_FMODE, CONTENTS_FMODE, FILE_FMODE, PickleError, PickleWarning, \
-    PicklingWarning, UnpicklingWarning
-from . import source, temp, detect
-
-# get global settings
-from .settings import settings
-
-# make sure "trace" is turned off
-detect.trace(False)
-
-try:
-    from importlib import reload
-except ImportError:
-    try:
-        from imp import reload
-    except ImportError:
-        pass
-
-# put the objects in order, if possible
-try:
-    from collections import OrderedDict as odict
-except ImportError:
-    try:
-        from ordereddict import OrderedDict as odict
-    except ImportError:
-        odict = dict
-objects = odict()
-# local import of dill._objects
-#from . import _objects
-#objects.update(_objects.succeeds)
-#del _objects
-
-# local import of dill.objtypes
-from . import objtypes as types
-
-def load_types(pickleable=True, unpickleable=True):
-    """load pickleable and/or unpickleable types to ``dill.types``
-
-    ``dill.types`` is meant to mimic the ``types`` module, providing a
-    registry of object types.  By default, the module is empty (for import
-    speed purposes). Use the ``load_types`` function to load selected object
-    types to the ``dill.types`` module.
-
-    Args:
-        pickleable (bool, default=True): if True, load pickleable types.
-        unpickleable (bool, default=True): if True, load unpickleable types.
-
-    Returns:
-        None
-    """
-    # local import of dill.objects
-    from . import _objects
-    if pickleable:
-        objects.update(_objects.succeeds)
-    else:
-        [objects.pop(obj,None) for obj in _objects.succeeds]
-    if unpickleable:
-        objects.update(_objects.failures)
-    else:
-        [objects.pop(obj,None) for obj in _objects.failures]
-    objects.update(_objects.registered)
-    del _objects
-    # reset contents of types to 'empty'
-    [types.__dict__.pop(obj) for obj in list(types.__dict__.keys()) \
-                             if obj.find('Type') != -1]
-    # add corresponding types from objects to types
-    reload(types)
-
-def extend(use_dill=True):
-    '''add (or remove) dill types to/from the pickle registry
-
-    by default, ``dill`` populates its types to ``pickle.Pickler.dispatch``.
-    Thus, all ``dill`` types are available upon calling ``'import pickle'``.
-    To drop all ``dill`` types from the ``pickle`` dispatch, *use_dill=False*.
-
-    Args:
-        use_dill (bool, default=True): if True, extend the dispatch table.
-
-    Returns:
-        None
-    '''
-    from ._dill import _revert_extension, _extend
-    if use_dill: _extend()
-    else: _revert_extension()
-    return
-
-extend()
-del odict
-
-
-def license():
-    """print license"""
-    print (__license__)
-    return
-
-def citation():
-    """print citation"""
-    print (__doc__[-491:-118])
-    return
-
-# end of file
+'''
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `dill-0.3.5.1/dill/_dill.py` & `dill-0.3.6/dill/_dill.py`

 * *Files 12% similar despite different names*

```diff
@@ -11,223 +11,127 @@
 Based on code written by Oren Tirosh and Armin Ronacher.
 Extended to a (near) full set of the builtin types (in types module),
 and coded to the pickle interface, by <mmckerns@caltech.edu>.
 Initial port to python3 by Jonathan Dobson, continued by mmckerns.
 Test against "all" python types (Std. Lib. CH 1-15 @ 2.7) by mmckerns.
 Test against CH16+ Std. Lib. ... TBD.
 """
-__all__ = ['dump','dumps','load','loads','dump_session','load_session',
-           'Pickler','Unpickler','register','copy','pickle','pickles',
-           'check','HIGHEST_PROTOCOL','DEFAULT_PROTOCOL','PicklingError',
-           'UnpicklingError','HANDLE_FMODE','CONTENTS_FMODE','FILE_FMODE',
-           'PickleError','PickleWarning','PicklingWarning','UnpicklingWarning']
-
-import logging
-log = logging.getLogger("dill")
-log.addHandler(logging.StreamHandler())
-def _trace(boolean):
-    """print a trace through the stack when pickling; useful for debugging"""
-    if boolean: log.setLevel(logging.INFO)
-    else: log.setLevel(logging.WARN)
-    return
+__all__ = [
+    'Pickler','Unpickler',
+    'check','copy','dump','dumps','load','loads','pickle','pickles','register',
+    'DEFAULT_PROTOCOL','HIGHEST_PROTOCOL','CONTENTS_FMODE','FILE_FMODE','HANDLE_FMODE',
+    'PickleError','PickleWarning','PicklingError','PicklingWarning','UnpicklingError',
+    'UnpicklingWarning',
+]
+
+__module__ = 'dill'
+
 import warnings
+from .logger import adapter as logger
+from .logger import trace as _trace
 
 import os
 import sys
 diff = None
 _use_diff = False
-PY3 = (sys.hexversion >= 0x3000000)
-# OLDER: 3.0 <= x < 3.4 *OR* x < 2.7.10  #NOTE: guessing relevant versions
-OLDER = (PY3 and sys.hexversion < 0x3040000) or (sys.hexversion < 0x2070ab1)
-OLD33 = (sys.hexversion < 0x3030000)
-OLD37 = (sys.hexversion < 0x3070000)
+OLD38 = (sys.hexversion < 0x3080000)
 OLD39 = (sys.hexversion < 0x3090000)
 OLD310 = (sys.hexversion < 0x30a0000)
-PY34 = (0x3040000 <= sys.hexversion < 0x3050000)
-if PY3: #XXX: get types from .objtypes ?
-    import builtins as __builtin__
-    from pickle import _Pickler as StockPickler, Unpickler as StockUnpickler
-    from _thread import LockType
-    if (sys.hexversion >= 0x30200f0):
-        from _thread import RLock as RLockType
-    else:
-        from threading import _RLock as RLockType
-   #from io import IOBase
-    from types import CodeType, FunctionType, MethodType, GeneratorType, \
-        TracebackType, FrameType, ModuleType, BuiltinMethodType
-    BufferType = memoryview #XXX: unregistered
-    ClassType = type # no 'old-style' classes
-    EllipsisType = type(Ellipsis)
-   #FileType = IOBase
-    NotImplementedType = type(NotImplemented)
-    SliceType = slice
-    TypeType = type # 'new-style' classes #XXX: unregistered
-    XRangeType = range
-    if OLD33:
-        DictProxyType = type(object.__dict__)
-    else:
-        from types import MappingProxyType as DictProxyType
-else:
-    import __builtin__
-    from pickle import Pickler as StockPickler, Unpickler as StockUnpickler
-    from thread import LockType
-    from threading import _RLock as RLockType
-    from types import CodeType, FunctionType, ClassType, MethodType, \
-         GeneratorType, DictProxyType, XRangeType, SliceType, TracebackType, \
-         NotImplementedType, EllipsisType, FrameType, ModuleType, \
-         BufferType, BuiltinMethodType, TypeType
-from pickle import HIGHEST_PROTOCOL, PickleError, PicklingError, UnpicklingError
-try:
-    from pickle import DEFAULT_PROTOCOL
-except ImportError:
-    DEFAULT_PROTOCOL = HIGHEST_PROTOCOL
+#XXX: get types from .objtypes ?
+import builtins as __builtin__
+from pickle import _Pickler as StockPickler, Unpickler as StockUnpickler
+from _thread import LockType
+from _thread import RLock as RLockType
+#from io import IOBase
+from types import CodeType, FunctionType, MethodType, GeneratorType, \
+    TracebackType, FrameType, ModuleType, BuiltinMethodType
+BufferType = memoryview #XXX: unregistered
+ClassType = type # no 'old-style' classes
+EllipsisType = type(Ellipsis)
+#FileType = IOBase
+NotImplementedType = type(NotImplemented)
+SliceType = slice
+TypeType = type # 'new-style' classes #XXX: unregistered
+XRangeType = range
+from types import MappingProxyType as DictProxyType
+from pickle import DEFAULT_PROTOCOL, HIGHEST_PROTOCOL, PickleError, PicklingError, UnpicklingError
 import __main__ as _main_module
 import marshal
 import gc
 # import zlib
 from weakref import ReferenceType, ProxyType, CallableProxyType
+from collections import OrderedDict
 from functools import partial
 from operator import itemgetter, attrgetter
-# new in python3.3
-if sys.hexversion < 0x03030000:
-    FileNotFoundError = IOError
-if PY3 and sys.hexversion < 0x03040000:
-    GENERATOR_FAIL = True
-else: GENERATOR_FAIL = False
-if PY3:
-    import importlib.machinery
-    EXTENSION_SUFFIXES = tuple(importlib.machinery.EXTENSION_SUFFIXES)
-else:
-    import imp
-    EXTENSION_SUFFIXES = tuple(suffix
-                               for (suffix, _, s_type) in imp.get_suffixes()
-                               if s_type == imp.C_EXTENSION)
+GENERATOR_FAIL = False
+import importlib.machinery
+EXTENSION_SUFFIXES = tuple(importlib.machinery.EXTENSION_SUFFIXES)
 try:
     import ctypes
     HAS_CTYPES = True
     # if using `pypy`, pythonapi is not found
     IS_PYPY = not hasattr(ctypes, 'pythonapi')
 except ImportError:
     HAS_CTYPES = False
     IS_PYPY = False
-IS_PYPY2 = IS_PYPY and not PY3
 NumpyUfuncType = None
 NumpyDType = None
 NumpyArrayType = None
 try:
-    if OLDER:
-        raise AttributeError('find_spec not found')
-    import importlib
     if not importlib.machinery.PathFinder().find_spec('numpy'):
         raise ImportError("No module named 'numpy'")
     NumpyUfuncType = True
     NumpyDType = True
     NumpyArrayType = True
-except AttributeError:
-    try:
-        import imp
-        imp.find_module('numpy')
-        NumpyUfuncType = True
-        NumpyDType = True
-        NumpyArrayType = True
-    except ImportError:
-        pass
 except ImportError:
     pass
 def __hook__():
     global NumpyArrayType, NumpyDType, NumpyUfuncType
     from numpy import ufunc as NumpyUfuncType
     from numpy import ndarray as NumpyArrayType
     from numpy import dtype as NumpyDType
     return True
 if NumpyArrayType: # then has numpy
-    def ndarraysubclassinstance(obj):
-        if type(obj) in (TypeType, ClassType):
-            return False # all classes return False
-        try: # check if is ndarray, and elif is subclass of ndarray
-            cls = getattr(obj, '__class__', None)
-            if cls is None: return False
-            elif cls is TypeType: return False
-            elif 'numpy.ndarray' not in str(getattr(cls, 'mro', int.mro)()):
-                return False
-        except ReferenceError: return False # handle 'R3' weakref in 3.x
-        except TypeError: return False
+    def ndarraysubclassinstance(obj_type):
+        if all((c.__module__, c.__name__) != ('numpy', 'ndarray') for c in obj_type.__mro__):
+            return False
         # anything below here is a numpy array (or subclass) instance
         __hook__() # import numpy (so the following works!!!)
         # verify that __reduce__ has not been overridden
-        NumpyInstance = NumpyArrayType((0,),'int8')
-        if id(obj.__reduce_ex__) == id(NumpyInstance.__reduce_ex__) and \
-           id(obj.__reduce__) == id(NumpyInstance.__reduce__): return True
-        return False
-    def numpyufunc(obj):
-        if type(obj) in (TypeType, ClassType):
-            return False # all classes return False
-        try: # check if is ufunc
-            cls = getattr(obj, '__class__', None)
-            if cls is None: return False
-            elif cls is TypeType: return False
-            if 'numpy.ufunc' not in str(getattr(cls, 'mro', int.mro)()):
-                return False
-        except ReferenceError: return False # handle 'R3' weakref in 3.x
-        except TypeError: return False
-        # anything below here is a numpy ufunc
+        if obj_type.__reduce_ex__ is not NumpyArrayType.__reduce_ex__ \
+                or obj_type.__reduce__ is not NumpyArrayType.__reduce__:
+            return False
         return True
-    def numpydtype(obj):
-        if type(obj) in (TypeType, ClassType):
-            return False # all classes return False
-        try: # check if is dtype
-            cls = getattr(obj, '__class__', None)
-            if cls is None: return False
-            elif cls is TypeType: return False
-            if 'numpy.dtype' not in str(getattr(obj, 'mro', int.mro)()):
-                return False
-        except ReferenceError: return False # handle 'R3' weakref in 3.x
-        except TypeError: return False
+    def numpyufunc(obj_type):
+        return any((c.__module__, c.__name__) == ('numpy', 'ufunc') for c in obj_type.__mro__)
+    def numpydtype(obj_type):
+        if all((c.__module__, c.__name__) != ('numpy', 'dtype') for c in obj_type.__mro__):
+            return False
         # anything below here is a numpy dtype
         __hook__() # import numpy (so the following works!!!)
-        return type(obj) is type(NumpyDType) # handles subclasses
+        return obj_type is type(NumpyDType) # handles subclasses
 else:
     def ndarraysubclassinstance(obj): return False
     def numpyufunc(obj): return False
     def numpydtype(obj): return False
 
-# make sure to add these 'hand-built' types to _typemap
-if PY3:
-    CellType = type((lambda x: lambda y: x)(0).__closure__[0])
-else:
-    CellType = type((lambda x: lambda y: x)(0).func_closure[0])
-# new in python2.5
-if sys.hexversion >= 0x20500f0:
-    from types import GetSetDescriptorType
-    if not IS_PYPY:
-        from types import MemberDescriptorType
-    else:
-        # oddly, MemberDescriptorType is GetSetDescriptorType
-        # while, member_descriptor does exist otherwise... is this a pypy bug?
-        class _member(object):
-            __slots__ = ['descriptor']
-        MemberDescriptorType = type(_member.descriptor)
-if IS_PYPY:
-    WrapperDescriptorType = MethodType
-    MethodDescriptorType = FunctionType
-    ClassMethodDescriptorType = FunctionType
-else:
-    WrapperDescriptorType = type(type.__repr__)
-    MethodDescriptorType = type(type.__dict__['mro'])
-    ClassMethodDescriptorType = type(type.__dict__['__prepare__' if PY3 else 'mro'])
+from types import GetSetDescriptorType, ClassMethodDescriptorType, \
+     WrapperDescriptorType,  MethodDescriptorType, MemberDescriptorType, \
+     MethodWrapperType #XXX: unused
 
-MethodWrapperType = type([].__repr__)
-PartialType = type(partial(int,base=2))
+# make sure to add these 'hand-built' types to _typemap
+CellType = type((lambda x: lambda y: x)(0).__closure__[0])
+PartialType = type(partial(int, base=2))
 SuperType = type(super(Exception, TypeError()))
 ItemGetterType = type(itemgetter(0))
 AttrGetterType = type(attrgetter('__repr__'))
 
 try:
     from functools import _lru_cache_wrapper as LRUCacheType
-except:
+except ImportError:
     LRUCacheType = None
 
 if not isinstance(LRUCacheType, type):
     LRUCacheType = None
 
 def get_file_type(*args, **kwargs):
     open = kwargs.pop("open", __builtin__.open)
@@ -245,40 +149,35 @@
     from _pyio import open as _open
     PyTextWrapperType = get_file_type('r', buffering=-1, open=_open)
     PyBufferedRandomType = get_file_type('r+b', buffering=-1, open=_open)
     PyBufferedReaderType = get_file_type('rb', buffering=-1, open=_open)
     PyBufferedWriterType = get_file_type('wb', buffering=-1, open=_open)
 except ImportError:
     PyTextWrapperType = PyBufferedRandomType = PyBufferedReaderType = PyBufferedWriterType = None
+from io import BytesIO as StringIO
+InputType = OutputType = None
+from socket import socket as SocketType
+#FIXME: additionally calls ForkingPickler.register several times
+from multiprocessing.reduction import _reduce_socket as reduce_socket
 try:
-    from cStringIO import StringIO, InputType, OutputType
-except ImportError:
-    if PY3:
-        from io import BytesIO as StringIO
-    else:
-        from StringIO import StringIO
-    InputType = OutputType = None
-if not IS_PYPY2:
-    from socket import socket as SocketType
-    try: #FIXME: additionally calls ForkingPickler.register several times
-        from multiprocessing.reduction import _reduce_socket as reduce_socket
-    except ImportError:
-        from multiprocessing.reduction import reduce_socket
-try:
-    __IPYTHON__ is True # is ipython
+    IS_IPYTHON = __IPYTHON__  # is True
     ExitType = None     # IPython.core.autocall.ExitAutocall
     singletontypes = ['exit', 'quit', 'get_ipython']
 except NameError:
+    IS_IPYTHON = False
     try: ExitType = type(exit) # apparently 'exit' can be removed
     except NameError: ExitType = None
     singletontypes = []
 
-from collections import OrderedDict
-
 import inspect
+import dataclasses
+import typing
+
+from pickle import GLOBAL
+
 
 ### Shims for different versions of Python and dill
 class Sentinel(object):
     """
     Create a unique sentinel object that is pickled as a constant.
     """
     def __init__(self, name, module_name=None):
@@ -392,146 +291,14 @@
 
 # def loadzs(str):
 #     """unpickle an object from a compressed string"""
 #     return loads(zlib.decompress(str))
 
 ### End: Shorthands ###
 
-### Pickle the Interpreter Session
-SESSION_IMPORTED_AS_TYPES = (ModuleType, ClassType, TypeType, Exception,
-                             FunctionType, MethodType, BuiltinMethodType)
-
-def _module_map():
-    """get map of imported modules"""
-    from collections import defaultdict, namedtuple
-    modmap = namedtuple('Modmap', ['by_name', 'by_id', 'top_level'])
-    modmap = modmap(defaultdict(list), defaultdict(list), {})
-    items = 'items' if PY3 else 'iteritems'
-    for modname, module in getattr(sys.modules, items)():
-        if not isinstance(module, ModuleType):
-            continue
-        if '.' not in modname:
-            modmap.top_level[id(module)] = modname
-        for objname, modobj in module.__dict__.items():
-            modmap.by_name[objname].append((modobj, modname))
-            modmap.by_id[id(modobj)].append((modobj, objname, modname))
-    return modmap
-
-def _lookup_module(modmap, name, obj, main_module):
-    """lookup name or id of obj if module is imported"""
-    for modobj, modname in modmap.by_name[name]:
-        if modobj is obj and sys.modules[modname] is not main_module:
-            return modname, name
-    if isinstance(obj, SESSION_IMPORTED_AS_TYPES):
-        for modobj, objname, modname in modmap.by_id[id(obj)]:
-            if sys.modules[modname] is not main_module:
-                return modname, objname
-    return None, None
-
-def _stash_modules(main_module):
-    modmap = _module_map()
-    newmod = ModuleType(main_module.__name__)
-
-    imported = []
-    imported_as = []
-    imported_top_level = []  # keep separeted for backwards compatibility
-    original = {}
-    items = 'items' if PY3 else 'iteritems'
-    for name, obj in getattr(main_module.__dict__, items)():
-        if obj is main_module:
-            original[name] = newmod  # self-reference
-            continue
-
-        # Avoid incorrectly matching a singleton value in another package (ex.: __doc__).
-        if any(obj is singleton for singleton in (None, False, True)) or \
-                isinstance(obj, ModuleType) and _is_builtin_module(obj):  # always saved by ref
-            original[name] = obj
-            continue
-
-        source_module, objname = _lookup_module(modmap, name, obj, main_module)
-        if source_module:
-            if objname == name:
-                imported.append((source_module, name))
-            else:
-                imported_as.append((source_module, objname, name))
-        else:
-            try:
-                imported_top_level.append((modmap.top_level[id(obj)], name))
-            except KeyError:
-                original[name] = obj
-
-    if len(original) < len(main_module.__dict__):
-        newmod.__dict__.update(original)
-        newmod.__dill_imported = imported
-        newmod.__dill_imported_as = imported_as
-        newmod.__dill_imported_top_level = imported_top_level
-        return newmod
-    else:
-        return main_module
-
-def _restore_modules(unpickler, main_module):
-    try:
-        for modname, name in main_module.__dict__.pop('__dill_imported'):
-            main_module.__dict__[name] = unpickler.find_class(modname, name)
-        for modname, objname, name in main_module.__dict__.pop('__dill_imported_as'):
-            main_module.__dict__[name] = unpickler.find_class(modname, objname)
-        for modname, name in main_module.__dict__.pop('__dill_imported_top_level'):
-            main_module.__dict__[name] = __import__(modname)
-    except KeyError:
-        pass
-
-#NOTE: 06/03/15 renamed main_module to main
-def dump_session(filename='/tmp/session.pkl', main=None, byref=False, **kwds):
-    """pickle the current state of __main__ to a file"""
-    from .settings import settings
-    protocol = settings['protocol']
-    if main is None: main = _main_module
-    if hasattr(filename, 'write'):
-        f = filename
-    else:
-        f = open(filename, 'wb')
-    try:
-        pickler = Pickler(f, protocol, **kwds)
-        pickler._original_main = main
-        if byref:
-            main = _stash_modules(main)
-        pickler._main = main     #FIXME: dill.settings are disabled
-        pickler._byref = False   # disable pickling by name reference
-        pickler._recurse = False # disable pickling recursion for globals
-        pickler._session = True  # is best indicator of when pickling a session
-        pickler._first_pass = True
-        pickler._main_modified = main is not pickler._original_main
-        pickler.dump(main)
-    finally:
-        if f is not filename:  # If newly opened file
-            f.close()
-    return
-
-def load_session(filename='/tmp/session.pkl', main=None, **kwds):
-    """update the __main__ module with the state from the session file"""
-    if main is None: main = _main_module
-    if hasattr(filename, 'read'):
-        f = filename
-    else:
-        f = open(filename, 'rb')
-    try: #FIXME: dill.settings are disabled
-        unpickler = Unpickler(f, **kwds)
-        unpickler._main = main
-        unpickler._session = True
-        module = unpickler.load()
-        unpickler._session = False
-        main.__dict__.update(module.__dict__)
-        _restore_modules(unpickler, main)
-    finally:
-        if f is not filename:  # If newly opened file
-            f.close()
-    return
-
-### End: Pickle the Interpreter
-
 class MetaCatchingDict(dict):
     def get(self, key, default=None):
         try:
             return self[key]
         except KeyError:
             return default
 
@@ -553,78 +320,84 @@
 ### Extend the Picklers
 class Pickler(StockPickler):
     """python's Pickler extended to interpreter sessions"""
     dispatch = MetaCatchingDict(StockPickler.dispatch.copy())
     _session = False
     from .settings import settings
 
-    def __init__(self, *args, **kwds):
+    def __init__(self, file, *args, **kwds):
         settings = Pickler.settings
         _byref = kwds.pop('byref', None)
        #_strictio = kwds.pop('strictio', None)
         _fmode = kwds.pop('fmode', None)
         _recurse = kwds.pop('recurse', None)
-        StockPickler.__init__(self, *args, **kwds)
+        StockPickler.__init__(self, file, *args, **kwds)
         self._main = _main_module
         self._diff_cache = {}
         self._byref = settings['byref'] if _byref is None else _byref
         self._strictio = False #_strictio
         self._fmode = settings['fmode'] if _fmode is None else _fmode
         self._recurse = settings['recurse'] if _recurse is None else _recurse
-        from collections import OrderedDict
         self._postproc = OrderedDict()
+        self._file = file
 
-    def dump(self, obj): #NOTE: if settings change, need to update attributes
+    def save(self, obj, save_persistent_id=True):
         # register if the object is a numpy ufunc
         # thanks to Paul Kienzle for pointing out ufuncs didn't pickle
-        if NumpyUfuncType and numpyufunc(obj):
-            @register(type(obj))
-            def save_numpy_ufunc(pickler, obj):
-                log.info("Nu: %s" % obj)
-                name = getattr(obj, '__qualname__', getattr(obj, '__name__', None))
-                StockPickler.save_global(pickler, obj, name=name)
-                log.info("# Nu")
-                return
-            # NOTE: the above 'save' performs like:
-            #   import copy_reg
-            #   def udump(f): return f.__name__
-            #   def uload(name): return getattr(numpy, name)
-            #   copy_reg.pickle(NumpyUfuncType, udump, uload)
-        # register if the object is a numpy dtype
-        if NumpyDType and numpydtype(obj):
-            @register(type(obj))
-            def save_numpy_dtype(pickler, obj):
-                log.info("Dt: %s" % obj)
-                pickler.save_reduce(_create_dtypemeta, (obj.type,), obj=obj)
-                log.info("# Dt")
-                return
-            # NOTE: the above 'save' performs like:
-            #   import copy_reg
-            #   def uload(name): return type(NumpyDType(name))
-            #   def udump(f): return uload, (f.type,)
-            #   copy_reg.pickle(NumpyDTypeType, udump, uload)
-        # register if the object is a subclassed numpy array instance
-        if NumpyArrayType and ndarraysubclassinstance(obj):
-            @register(type(obj))
-            def save_numpy_array(pickler, obj):
-                log.info("Nu: (%s, %s)" % (obj.shape,obj.dtype))
-                npdict = getattr(obj, '__dict__', None)
-                f, args, state = obj.__reduce__()
-                pickler.save_reduce(_create_array, (f,args,state,npdict), obj=obj)
-                log.info("# Nu")
-                return
+        obj_type = type(obj)
+        if NumpyArrayType and not (obj_type is type or obj_type in Pickler.dispatch):
+            if NumpyUfuncType and numpyufunc(obj_type):
+                @register(obj_type)
+                def save_numpy_ufunc(pickler, obj):
+                    logger.trace(pickler, "Nu: %s", obj)
+                    name = getattr(obj, '__qualname__', getattr(obj, '__name__', None))
+                    StockPickler.save_global(pickler, obj, name=name)
+                    logger.trace(pickler, "# Nu")
+                    return
+                # NOTE: the above 'save' performs like:
+                #   import copy_reg
+                #   def udump(f): return f.__name__
+                #   def uload(name): return getattr(numpy, name)
+                #   copy_reg.pickle(NumpyUfuncType, udump, uload)
+            # register if the object is a numpy dtype
+            if NumpyDType and numpydtype(obj_type):
+                @register(obj_type)
+                def save_numpy_dtype(pickler, obj):
+                    logger.trace(pickler, "Dt: %s", obj)
+                    pickler.save_reduce(_create_dtypemeta, (obj.type,), obj=obj)
+                    logger.trace(pickler, "# Dt")
+                    return
+                # NOTE: the above 'save' performs like:
+                #   import copy_reg
+                #   def uload(name): return type(NumpyDType(name))
+                #   def udump(f): return uload, (f.type,)
+                #   copy_reg.pickle(NumpyDTypeType, udump, uload)
+            # register if the object is a subclassed numpy array instance
+            if NumpyArrayType and ndarraysubclassinstance(obj_type):
+                @register(obj_type)
+                def save_numpy_array(pickler, obj):
+                    logger.trace(pickler, "Nu: (%s, %s)", obj.shape, obj.dtype)
+                    npdict = getattr(obj, '__dict__', None)
+                    f, args, state = obj.__reduce__()
+                    pickler.save_reduce(_create_array, (f,args,state,npdict), obj=obj)
+                    logger.trace(pickler, "# Nu")
+                    return
         # end hack
         if GENERATOR_FAIL and type(obj) == GeneratorType:
             msg = "Can't pickle %s: attribute lookup builtins.generator failed" % GeneratorType
             raise PicklingError(msg)
-        else:
-            StockPickler.dump(self, obj)
-        return
+        StockPickler.save(self, obj, save_persistent_id)
+
+    save.__doc__ = StockPickler.save.__doc__
+
+    def dump(self, obj): #NOTE: if settings change, need to update attributes
+        logger.trace_setup(self)
+        StockPickler.dump(self, obj)
+
     dump.__doc__ = StockPickler.dump.__doc__
-    pass
 
 class Unpickler(StockUnpickler):
     """python's Unpickler extended to interpreter sessions and more types"""
     from .settings import settings
     _session = False
 
     def find_class(self, module, name):
@@ -691,65 +464,103 @@
     MUST be called at start of script, otherwise changes will not be recorded.
     """
     global _use_diff, diff
     _use_diff = on
     if _use_diff and diff is None:
         try:
             from . import diff as d
-        except:
+        except ImportError:
             import diff as d
         diff = d
 
 def _create_typemap():
     import types
-    if PY3:
-        d = dict(list(__builtin__.__dict__.items()) + \
-                 list(types.__dict__.items())).items()
-        builtin = 'builtins'
-    else:
-        d = types.__dict__.iteritems()
-        builtin = '__builtin__'
+    d = dict(list(__builtin__.__dict__.items()) + \
+             list(types.__dict__.items())).items()
     for key, value in d:
-        if getattr(value, '__module__', None) == builtin \
-        and type(value) is type:
+        if getattr(value, '__module__', None) == 'builtins' \
+                and type(value) is type:
             yield key, value
     return
 _reverse_typemap = dict(_create_typemap())
 _reverse_typemap.update({
-    'CellType': CellType,
-    'MethodWrapperType': MethodWrapperType,
     'PartialType': PartialType,
     'SuperType': SuperType,
     'ItemGetterType': ItemGetterType,
     'AttrGetterType': AttrGetterType,
+})
+if sys.hexversion < 0x30800a2:
+    _reverse_typemap.update({
+        'CellType': CellType,
+    })
+
+# "Incidental" implementation specific types. Unpickling these types in another
+# implementation of Python (PyPy -> CPython) is not guaranteed to work
+
+# This dictionary should contain all types that appear in Python implementations
+# but are not defined in https://docs.python.org/3/library/types.html#standard-interpreter-types
+x=OrderedDict()
+_incedental_reverse_typemap = {
     'FileType': FileType,
     'BufferedRandomType': BufferedRandomType,
     'BufferedReaderType': BufferedReaderType,
     'BufferedWriterType': BufferedWriterType,
     'TextWrapperType': TextWrapperType,
     'PyBufferedRandomType': PyBufferedRandomType,
     'PyBufferedReaderType': PyBufferedReaderType,
     'PyBufferedWriterType': PyBufferedWriterType,
     'PyTextWrapperType': PyTextWrapperType,
+}
+
+_incedental_reverse_typemap.update({
+    "DictKeysType": type({}.keys()),
+    "DictValuesType": type({}.values()),
+    "DictItemsType": type({}.items()),
+
+    "OdictKeysType": type(x.keys()),
+    "OdictValuesType": type(x.values()),
+    "OdictItemsType": type(x.items()),
 })
+
 if ExitType:
-    _reverse_typemap['ExitType'] = ExitType
+    _incedental_reverse_typemap['ExitType'] = ExitType
 if InputType:
-    _reverse_typemap['InputType'] = InputType
-    _reverse_typemap['OutputType'] = OutputType
-if not IS_PYPY:
-    _reverse_typemap['WrapperDescriptorType'] = WrapperDescriptorType
-    _reverse_typemap['MethodDescriptorType'] = MethodDescriptorType
-    _reverse_typemap['ClassMethodDescriptorType'] = ClassMethodDescriptorType
-else:
-    _reverse_typemap['MemberDescriptorType'] = MemberDescriptorType
-if PY3:
-    _typemap = dict((v, k) for k, v in _reverse_typemap.items())
-else:
-    _typemap = dict((v, k) for k, v in _reverse_typemap.iteritems())
+    _incedental_reverse_typemap['InputType'] = InputType
+    _incedental_reverse_typemap['OutputType'] = OutputType
+
+'''
+try:
+    import symtable
+    _incedental_reverse_typemap["SymtableEntryType"] = type(symtable.symtable("", "string", "exec")._table)
+except: #FIXME: fails to pickle
+    pass
+
+if sys.hexversion >= 0x30a00a0:
+    _incedental_reverse_typemap['LineIteratorType'] = type(compile('3', '', 'eval').co_lines())
+'''
+
+if sys.hexversion >= 0x30b00b0:
+    from types import GenericAlias
+    _incedental_reverse_typemap["GenericAliasIteratorType"] = type(iter(GenericAlias(list, (int,))))
+    '''
+    _incedental_reverse_typemap['PositionsIteratorType'] = type(compile('3', '', 'eval').co_positions())
+    '''
+
+try:
+    import winreg
+    _incedental_reverse_typemap["HKEYType"] = winreg.HKEYType
+except ImportError:
+    pass
+
+_reverse_typemap.update(_incedental_reverse_typemap)
+_incedental_types = set(_incedental_reverse_typemap.values())
+
+del x
+
+_typemap = dict((v, k) for k, v in _reverse_typemap.items())
 
 def _unmarshal(string):
     return marshal.loads(string)
 
 def _load_type(name):
     return _reverse_typemap[name]
 
@@ -768,64 +579,181 @@
     # 'recurse' only stores referenced modules/objects in fglobals,
     # thus we need to make sure that we have __builtins__ as well
     if "__builtins__" not in func.__globals__:
         func.__globals__["__builtins__"] = globals()["__builtins__"]
     # assert id(fglobals) == id(func.__globals__)
     return func
 
+class match:
+    """
+    Make avaialable a limited structural pattern matching-like syntax for Python < 3.10
+
+    Patterns can be only tuples (without types) currently.
+    Inspired by the package pattern-matching-PEP634.
+
+    Usage:
+    >>> with match(args) as m:
+    >>>     if   m.case(('x', 'y')):
+    >>>         # use m.x and m.y
+    >>>     elif m.case(('x', 'y', 'z')):
+    >>>         # use m.x, m.y and m.z
+
+    Equivalent native code for Python >= 3.10:
+    >>> match args:
+    >>>     case (x, y):
+    >>>         # use x and y
+    >>>     case (x, y, z):
+    >>>         # use x, y and z
+    """
+    def __init__(self, value):
+        self.value = value
+        self._fields = None
+    def __enter__(self):
+        return self
+    def __exit__(self, *exc_info):
+        return False
+    def case(self, args): # *args, **kwargs):
+        """just handles tuple patterns"""
+        if len(self.value) != len(args): # + len(kwargs):
+            return False
+        #if not all(isinstance(arg, pat) for arg, pat in zip(self.value[len(args):], kwargs.values())):
+        #    return False
+        self.args = args # (*args, *kwargs)
+        return True
+    @property
+    def fields(self):
+        # Only bind names to values if necessary.
+        if self._fields is None:
+            self._fields = dict(zip(self.args, self.value))
+        return self._fields
+    def __getattr__(self, item):
+        return self.fields[item]
+
+ALL_CODE_PARAMS = [
+    # Version     New attribute         CodeType parameters
+    ((3,11,'a'), 'co_endlinetable',    'argcount posonlyargcount kwonlyargcount nlocals stacksize flags code consts names varnames filename name qualname firstlineno linetable endlinetable columntable exceptiontable freevars cellvars'),
+    ((3,11),     'co_exceptiontable',  'argcount posonlyargcount kwonlyargcount nlocals stacksize flags code consts names varnames filename name qualname firstlineno linetable                          exceptiontable freevars cellvars'),
+    ((3,10),     'co_linetable',       'argcount posonlyargcount kwonlyargcount nlocals stacksize flags code consts names varnames filename name          firstlineno linetable                                         freevars cellvars'),
+    ((3,8),      'co_posonlyargcount', 'argcount posonlyargcount kwonlyargcount nlocals stacksize flags code consts names varnames filename name          firstlineno lnotab                                            freevars cellvars'),
+    ((3,7),      'co_kwonlyargcount',  'argcount                 kwonlyargcount nlocals stacksize flags code consts names varnames filename name          firstlineno lnotab                                            freevars cellvars'),
+    ]
+for version, new_attr, params in ALL_CODE_PARAMS:
+    if hasattr(CodeType, new_attr):
+        CODE_VERSION = version
+        CODE_PARAMS = params.split()
+        break
+ENCODE_PARAMS = set(CODE_PARAMS).intersection(
+        ['code', 'lnotab', 'linetable', 'endlinetable', 'columntable', 'exceptiontable'])
+
 def _create_code(*args):
-    if PY3 and hasattr(args[-3], 'encode'): #FIXME: from PY2 fails (optcode)
-        args = list(args)
-        if len(args) == 20:
-            args[-3] = args[-3].encode() # co_exceptiontable
-            args[-6] = args[-6].encode() # co_lnotab
-            args[-14] = args[-14].encode() # co_code
-            if args[-4] is not None:
-                args[-4] = args[-4].encode() # co_columntable
-            if args[-5] is not None:
-                args[-5] = args[-5].encode() # co_endlinetable
-        else:
-            args[-3] = args[-3].encode() # co_lnotab
-            args[-10] = args[-10].encode() # co_code
-    if hasattr(CodeType, 'co_exceptiontable'):
-        if len(args) == 20: return CodeType(*args)
-        elif len(args) == 16:
-            argz = (None, None, b'')
-            argz = args[:-4] + args[-5:-4] + args[-4:-2] + argz + args[-2:]
-            return CodeType(*argz)
-        elif len(args) == 15:
-            argz = args[1:-4] + args[-5:-4] + args[-4:-2] + argz + args[-2:]
-            return CodeType(args[0], 0, *argz)
-        argz = args[1:-4] + args[-5:-4] + args[-4:-2] + argz + args[-2:]
-        return CodeType(args[0], 0, 0, *argz)
-    elif hasattr(CodeType, 'co_posonlyargcount'):
-        if len(args) == 20:
-            return CodeType(*(args[:12] + args[13:15] + args[18:]))
-        elif len(args) == 16: return CodeType(*args)
-        elif len(args) == 15: return CodeType(args[0], 0, *args[1:])
-        return CodeType(args[0], 0, 0, *args[1:])
-    elif hasattr(CodeType, 'co_kwonlyargcount'):
-        if len(args) == 20:
-            return CodeType(*(args[:1] + args[2:12] + args[13:15] + args[18:]))
-        elif len(args) == 16: return CodeType(args[0], *args[2:])
-        elif len(args) == 15: return CodeType(*args)
-        return CodeType(args[0], 0, *args[1:])
-    if len(args) == 20:
-        return CodeType(*(args[:1] + args[3:12] + args[13:15] + args[18:]))
-    elif len(args) == 16: return CodeType(args[0], *args[3:])
-    elif len(args) == 15: return CodeType(args[0], *args[2:])
+    if not isinstance(args[0], int): # co_lnotab stored from >= 3.10
+        LNOTAB, *args = args
+    else: # from < 3.10 (or pre-LNOTAB storage)
+        LNOTAB = b''
+
+    with match(args) as m:
+        # Python 3.11/3.12a (18 members)
+        if m.case((
+            'argcount', 'posonlyargcount', 'kwonlyargcount', 'nlocals', 'stacksize', 'flags',     # args[0:6]
+            'code', 'consts', 'names', 'varnames', 'filename', 'name', 'qualname', 'firstlineno', # args[6:14]
+            'linetable', 'exceptiontable', 'freevars', 'cellvars'                                 # args[14:]
+        )):
+            if CODE_VERSION == (3,11):
+                return CodeType(
+                    *args[:6],
+                    args[6].encode() if hasattr(args[6], 'encode') else args[6], # code
+                    *args[7:14],
+                    args[14].encode() if hasattr(args[14], 'encode') else args[14], # linetable
+                    args[15].encode() if hasattr(args[15], 'encode') else args[15], # exceptiontable
+                    args[16],
+                    args[17],
+                )
+            fields = m.fields
+        # Python 3.10 or 3.8/3.9 (16 members)
+        elif m.case((
+            'argcount', 'posonlyargcount', 'kwonlyargcount', 'nlocals', 'stacksize', 'flags', # args[0:6]
+            'code', 'consts', 'names', 'varnames', 'filename', 'name', 'firstlineno',         # args[6:13]
+            'LNOTAB_OR_LINETABLE', 'freevars', 'cellvars'                                     # args[13:]
+        )):
+            if CODE_VERSION == (3,10) or CODE_VERSION == (3,8):
+                return CodeType(
+                    *args[:6],
+                    args[6].encode() if hasattr(args[6], 'encode') else args[6], # code
+                    *args[7:13],
+                    args[13].encode() if hasattr(args[13], 'encode') else args[13], # lnotab/linetable
+                    args[14],
+                    args[15],
+                )
+            fields = m.fields
+            if CODE_VERSION >= (3,10):
+                fields['linetable'] = m.LNOTAB_OR_LINETABLE
+            else:
+                fields['lnotab'] = LNOTAB if LNOTAB else m.LNOTAB_OR_LINETABLE
+        # Python 3.7 (15 args)
+        elif m.case((
+            'argcount', 'kwonlyargcount', 'nlocals', 'stacksize', 'flags',            # args[0:5]
+            'code', 'consts', 'names', 'varnames', 'filename', 'name', 'firstlineno', # args[5:12]
+            'lnotab', 'freevars', 'cellvars'                                          # args[12:]
+        )):
+            if CODE_VERSION == (3,7):
+                return CodeType(
+                    *args[:5],
+                    args[5].encode() if hasattr(args[5], 'encode') else args[5], # code
+                    *args[6:12],
+                    args[12].encode() if hasattr(args[12], 'encode') else args[12], # lnotab
+                    args[13],
+                    args[14],
+                )
+            fields = m.fields
+        # Python 3.11a (20 members)
+        elif m.case((
+            'argcount', 'posonlyargcount', 'kwonlyargcount', 'nlocals', 'stacksize', 'flags',     # args[0:6]
+            'code', 'consts', 'names', 'varnames', 'filename', 'name', 'qualname', 'firstlineno', # args[6:14]
+            'linetable', 'endlinetable', 'columntable', 'exceptiontable', 'freevars', 'cellvars'  # args[14:]
+        )):
+            if CODE_VERSION == (3,11,'a'):
+                return CodeType(
+                    *args[:6],
+                    args[6].encode() if hasattr(args[6], 'encode') else args[6], # code
+                    *args[7:14],
+                    *(a.encode() if hasattr(a, 'encode') else a for a in args[14:18]), # linetable-exceptiontable
+                    args[18],
+                    args[19],
+                )
+            fields = m.fields
+        else:
+            raise UnpicklingError("pattern match for code object failed")
+
+    # The args format doesn't match this version.
+    fields.setdefault('posonlyargcount', 0)         # from python <= 3.7
+    fields.setdefault('lnotab', LNOTAB)             # from python >= 3.10
+    fields.setdefault('linetable', b'')             # from python <= 3.9
+    fields.setdefault('qualname', fields['name'])   # from python <= 3.10
+    fields.setdefault('exceptiontable', b'')        # from python <= 3.10
+    fields.setdefault('endlinetable', None)         # from python != 3.11a
+    fields.setdefault('columntable', None)          # from python != 3.11a
+
+    args = (fields[k].encode() if k in ENCODE_PARAMS and hasattr(fields[k], 'encode') else fields[k]
+            for k in CODE_PARAMS)
     return CodeType(*args)
 
 def _create_ftype(ftypeobj, func, args, kwds):
     if kwds is None:
         kwds = {}
     if args is None:
         args = ()
     return ftypeobj(func, *args, **kwds)
 
+def _create_typing_tuple(argz, *args): #NOTE: workaround python/cpython#94245
+    if not argz:
+        return typing.Tuple[()].copy_with(())
+    if argz == ((),):
+        return typing.Tuple[()]
+    return typing.Tuple[argz]
+
 def _create_lock(locked, *args): #XXX: ignores 'blocking'
     from threading import Lock
     lock = Lock()
     if locked:
         if not lock.acquire(False):
             raise UnpicklingError("Cannot acquire lock")
     return lock
@@ -849,20 +777,17 @@
         f = names[name] #XXX: safer "f=sys.stdin"
     elif name == '<tmpfile>':
         f = os.tmpfile()
     elif name == '<fdopen>':
         import tempfile
         f = tempfile.TemporaryFile(mode)
     else:
-        # treat x mode as w mode
-        if "x" in mode and sys.hexversion < 0x03030000:
-            raise ValueError("invalid mode: '%s'" % mode)
         try:
             exists = os.path.exists(name)
-        except:
+        except Exception:
             exists = False
         if not exists:
             if strictio:
                 raise FileNotFoundError("[Errno 2] No such file or directory: '%s'" % name)
             elif "r" in mode and fmode != FILE_FMODE:
                 name = '<fdopen>' # or os.devnull?
             current_size = 0 # or maintain position?
@@ -883,46 +808,28 @@
                 f.write(fdata)
                 if "w" not in mode:
                     f.close()
                     f = open(name, mode)
             elif name == '<fdopen>': # file did not exist
                 import tempfile
                 f = tempfile.TemporaryFile(mode)
+            # treat x mode as w mode
             elif fmode == CONTENTS_FMODE \
                and ("w" in mode or "x" in mode):
                 # stop truncation when opening
                 flags = os.O_CREAT
                 if "+" in mode:
                     flags |= os.O_RDWR
                 else:
                     flags |= os.O_WRONLY
                 f = os.fdopen(os.open(name, flags), mode)
                 # set name to the correct value
-                if PY3:
-                    r = getattr(f, "buffer", f)
-                    r = getattr(r, "raw", r)
-                    r.name = name
-                else:
-                    if not HAS_CTYPES:
-                        raise ImportError("No module named 'ctypes'")
-                    class FILE(ctypes.Structure):
-                        _fields_ = [("refcount", ctypes.c_long),
-                                    ("type_obj", ctypes.py_object),
-                                    ("file_pointer", ctypes.c_voidp),
-                                    ("name", ctypes.py_object)]
-
-                    class PyObject(ctypes.Structure):
-                        _fields_ = [
-                            ("ob_refcnt", ctypes.c_int),
-                            ("ob_type", ctypes.py_object)
-                            ]
-                    #FIXME: CONTENTS_FMODE fails for pypy due to issue #1233
-                    #       https://bitbucket.org/pypy/pypy/issues/1233
-                    ctypes.cast(id(f), ctypes.POINTER(FILE)).contents.name = name
-                    ctypes.cast(id(name), ctypes.POINTER(PyObject)).contents.ob_refcnt += 1
+                r = getattr(f, "buffer", f)
+                r = getattr(r, "raw", r)
+                r.name = name
                 assert f.name == name
             else:
                 f = open(name, mode)
         except (IOError, FileNotFoundError):
             err = sys.exc_info()[1]
             raise UnpicklingError(err)
     if closed:
@@ -975,56 +882,42 @@
 __d = {}
 try:
     # In CPython 3.9 and later, this trick can be used to exploit the
     # implementation of the __or__ function of MappingProxyType to get the true
     # mapping referenced by the proxy. It may work for other implementations,
     # but is not guaranteed.
     MAPPING_PROXY_TRICK = __d is (DictProxyType(__d) | _dictproxy_helper_instance)
-except:
+except Exception:
     MAPPING_PROXY_TRICK = False
 del __d
 
 # _CELL_REF and _CELL_EMPTY are used to stay compatible with versions of dill
 # whose _create_cell functions do not have a default value.
 # _CELL_REF can be safely removed entirely (replaced by empty tuples for calls
 # to _create_cell) once breaking changes are allowed.
 _CELL_REF = None
 _CELL_EMPTY = Sentinel('_CELL_EMPTY')
 
-if PY3:
-    def _create_cell(contents=None):
-        if contents is not _CELL_EMPTY:
-            value = contents
-        return (lambda: value).__closure__[0]
-
-else:
-    def _create_cell(contents=None):
-        if contents is not _CELL_EMPTY:
-            value = contents
-        return (lambda: value).func_closure[0]
-
+def _create_cell(contents=None):
+    if contents is not _CELL_EMPTY:
+        value = contents
+    return (lambda: value).__closure__[0]
 
 def _create_weakref(obj, *args):
     from weakref import ref
     if obj is None: # it's dead
-        if PY3:
-            from collections import UserDict
-        else:
-            from UserDict import UserDict
+        from collections import UserDict
         return ref(UserDict(), *args)
     return ref(obj, *args)
 
 def _create_weakproxy(obj, callable=False, *args):
     from weakref import proxy
     if obj is None: # it's dead
         if callable: return proxy(lambda x:x, *args)
-        if PY3:
-            from collections import UserDict
-        else:
-            from UserDict import UserDict
+        from collections import UserDict
         return proxy(UserDict(), *args)
     return proxy(obj, *args)
 
 def _eval_repr(repr_str):
     return eval(repr_str)
 
 def _create_array(f, args, state, npdict=None):
@@ -1037,80 +930,117 @@
 
 def _create_dtypemeta(scalar_type):
     if NumpyDType is True: __hook__() # a bit hacky I think
     if scalar_type is None:
         return NumpyDType
     return type(NumpyDType(scalar_type))
 
-if OLD37:
-    def _create_namedtuple(name, fieldnames, modulename, defaults=None):
-        class_ = _import_module(modulename + '.' + name, safe=True)
-        if class_ is not None:
-            return class_
-        import collections
-        t = collections.namedtuple(name, fieldnames)
-        t.__module__ = modulename
-        return t
-else:
-    def _create_namedtuple(name, fieldnames, modulename, defaults=None):
-        class_ = _import_module(modulename + '.' + name, safe=True)
-        if class_ is not None:
-            return class_
-        import collections
-        t = collections.namedtuple(name, fieldnames, defaults=defaults, module=modulename)
-        return t
+def _create_namedtuple(name, fieldnames, modulename, defaults=None):
+    class_ = _import_module(modulename + '.' + name, safe=True)
+    if class_ is not None:
+        return class_
+    import collections
+    t = collections.namedtuple(name, fieldnames, defaults=defaults, module=modulename)
+    return t
+
+def _create_capsule(pointer, name, context, destructor):
+    attr_found = False
+    try:
+        # based on https://github.com/python/cpython/blob/f4095e53ab708d95e019c909d5928502775ba68f/Objects/capsule.c#L209-L231
+        uname = name.decode('utf8')
+        for i in range(1, uname.count('.')+1):
+            names = uname.rsplit('.', i)
+            try:
+                module = __import__(names[0])
+            except ImportError:
+                pass
+            obj = module
+            for attr in names[1:]:
+                obj = getattr(obj, attr)
+            capsule = obj
+            attr_found = True
+            break
+    except Exception:
+        pass
+
+    if attr_found:
+        if _PyCapsule_IsValid(capsule, name):
+            return capsule
+        raise UnpicklingError("%s object exists at %s but a PyCapsule object was expected." % (type(capsule), name))
+    else:
+        warnings.warn('Creating a new PyCapsule %s for a C data structure that may not be present in memory. Segmentation faults or other memory errors are possible.' % (name,), UnpicklingWarning)
+        capsule = _PyCapsule_New(pointer, name, destructor)
+        _PyCapsule_SetContext(capsule, context)
+        return capsule
 
 def _getattr(objclass, name, repr_str):
     # hack to grab the reference directly
     try: #XXX: works only for __builtin__ ?
         attr = repr_str.split("'")[3]
         return eval(attr+'.__dict__["'+name+'"]')
-    except:
+    except Exception:
         try:
             attr = objclass.__dict__
             if type(attr) is DictProxyType:
                 attr = attr[name]
             else:
                 attr = getattr(objclass,name)
-        except:
+        except (AttributeError, KeyError):
             attr = getattr(objclass,name)
         return attr
 
 def _get_attr(self, name):
     # stop recursive pickling
     return getattr(self, name, None) or getattr(__builtin__, name)
 
-def _dict_from_dictproxy(dictproxy):
-    _dict = dictproxy.copy() # convert dictproxy to dict
-    _dict.pop('__dict__', None)
-    _dict.pop('__weakref__', None)
-    _dict.pop('__prepare__', None)
-    return _dict
-
 def _import_module(import_name, safe=False):
     try:
-        if '.' in import_name:
+        if import_name.startswith('__runtime__.'):
+            return sys.modules[import_name]
+        elif '.' in import_name:
             items = import_name.split('.')
             module = '.'.join(items[:-1])
             obj = items[-1]
         else:
             return __import__(import_name)
         return getattr(__import__(module, None, None, [obj]), obj)
-    except (ImportError, AttributeError):
+    except (ImportError, AttributeError, KeyError):
         if safe:
             return None
         raise
 
+# https://github.com/python/cpython/blob/a8912a0f8d9eba6d502c37d522221f9933e976db/Lib/pickle.py#L322-L333
+def _getattribute(obj, name):
+    for subpath in name.split('.'):
+        if subpath == '<locals>':
+            raise AttributeError("Can't get local attribute {!r} on {!r}"
+                                 .format(name, obj))
+        try:
+            parent = obj
+            obj = getattr(obj, subpath)
+        except AttributeError:
+            raise AttributeError("Can't get attribute {!r} on {!r}"
+                                 .format(name, obj))
+    return obj, parent
+
 def _locate_function(obj, pickler=None):
-    if obj.__module__ in ['__main__', None] or \
-            pickler and is_dill(pickler, child=False) and pickler._session and obj.__module__ == pickler._main.__name__:
+    module_name = getattr(obj, '__module__', None)
+    if module_name in ['__main__', None] or \
+            pickler and is_dill(pickler, child=False) and pickler._session and module_name == pickler._main.__name__:
         return False
-
-    found = _import_module(obj.__module__ + '.' + obj.__name__, safe=True)
-    return found is obj
+    if hasattr(obj, '__qualname__'):
+        module = _import_module(module_name, safe=True)
+        try:
+            found, _ = _getattribute(module, obj.__qualname__)
+            return found is obj
+        except AttributeError:
+            return False
+    else:
+        found = _import_module(module_name + '.' + obj.__name__, safe=True)
+        return found is obj
 
 
 def _setitems(dest, source):
     for k, v in source.items():
         dest[k] = v
 
 
@@ -1154,145 +1084,150 @@
                     pickler._batch_setitems(iter(source.items()))
                 else:
                     # Updating with an empty dictionary. Same as doing nothing.
                     continue
             else:
                 pickler.save_reduce(*reduction)
             # pop None created by calling preprocessing step off stack
-            if PY3:
-                pickler.write(bytes('0', 'UTF-8'))
-            else:
-                pickler.write('0')
+            pickler.write(bytes('0', 'UTF-8'))
 
 #@register(CodeType)
 #def save_code(pickler, obj):
-#    log.info("Co: %s" % obj)
+#    logger.trace(pickler, "Co: %s", obj)
 #    pickler.save_reduce(_unmarshal, (marshal.dumps(obj),), obj=obj)
-#    log.info("# Co")
+#    logger.trace(pickler, "# Co")
 #    return
 
 # The following function is based on 'save_codeobject' from 'cloudpickle'
 # Copyright (c) 2012, Regents of the University of California.
 # Copyright (c) 2009 `PiCloud, Inc. <http://www.picloud.com>`_.
 # License: https://github.com/cloudpipe/cloudpickle/blob/master/LICENSE
 @register(CodeType)
 def save_code(pickler, obj):
-    log.info("Co: %s" % obj)
-    if PY3:
-        if hasattr(obj, "co_exceptiontable"):
-            args = (
-                obj.co_argcount, obj.co_posonlyargcount,
-                obj.co_kwonlyargcount, obj.co_nlocals, obj.co_stacksize,
-                obj.co_flags, obj.co_code, obj.co_consts, obj.co_names,
-                obj.co_varnames, obj.co_filename, obj.co_name, obj.co_qualname,
-                obj.co_firstlineno, obj.co_lnotab, obj.co_endlinetable,
-                obj.co_columntable, obj.co_exceptiontable, obj.co_freevars,
-                obj.co_cellvars
-        )
-        elif hasattr(obj, "co_posonlyargcount"):
-            args = (
-                obj.co_argcount, obj.co_posonlyargcount,
-                obj.co_kwonlyargcount, obj.co_nlocals, obj.co_stacksize,
-                obj.co_flags, obj.co_code, obj.co_consts, obj.co_names,
-                obj.co_varnames, obj.co_filename, obj.co_name,
-                obj.co_firstlineno, obj.co_lnotab, obj.co_freevars,
-                obj.co_cellvars
-        )
-        else:
-            args = (
-                obj.co_argcount, obj.co_kwonlyargcount, obj.co_nlocals,
-                obj.co_stacksize, obj.co_flags, obj.co_code, obj.co_consts,
-                obj.co_names, obj.co_varnames, obj.co_filename,
-                obj.co_name, obj.co_firstlineno, obj.co_lnotab,
-                obj.co_freevars, obj.co_cellvars
-        )
-    else:
+    logger.trace(pickler, "Co: %s", obj)
+    if hasattr(obj, "co_endlinetable"): # python 3.11a (20 args)
         args = (
-            obj.co_argcount, obj.co_nlocals, obj.co_stacksize, obj.co_flags,
-            obj.co_code, obj.co_consts, obj.co_names, obj.co_varnames,
-            obj.co_filename, obj.co_name, obj.co_firstlineno, obj.co_lnotab,
+            obj.co_lnotab, # for < python 3.10 [not counted in args]
+            obj.co_argcount, obj.co_posonlyargcount,
+            obj.co_kwonlyargcount, obj.co_nlocals, obj.co_stacksize,
+            obj.co_flags, obj.co_code, obj.co_consts, obj.co_names,
+            obj.co_varnames, obj.co_filename, obj.co_name, obj.co_qualname,
+            obj.co_firstlineno, obj.co_linetable, obj.co_endlinetable,
+            obj.co_columntable, obj.co_exceptiontable, obj.co_freevars,
+            obj.co_cellvars
+    )
+    elif hasattr(obj, "co_exceptiontable"): # python 3.11 (18 args)
+        args = (
+            obj.co_lnotab, # for < python 3.10 [not counted in args]
+            obj.co_argcount, obj.co_posonlyargcount,
+            obj.co_kwonlyargcount, obj.co_nlocals, obj.co_stacksize,
+            obj.co_flags, obj.co_code, obj.co_consts, obj.co_names,
+            obj.co_varnames, obj.co_filename, obj.co_name, obj.co_qualname,
+            obj.co_firstlineno, obj.co_linetable, obj.co_exceptiontable,
             obj.co_freevars, obj.co_cellvars
-        )
+    )
+    elif hasattr(obj, "co_linetable"): # python 3.10 (16 args)
+        args = (
+            obj.co_lnotab, # for < python 3.10 [not counted in args]
+            obj.co_argcount, obj.co_posonlyargcount,
+            obj.co_kwonlyargcount, obj.co_nlocals, obj.co_stacksize,
+            obj.co_flags, obj.co_code, obj.co_consts, obj.co_names,
+            obj.co_varnames, obj.co_filename, obj.co_name,
+            obj.co_firstlineno, obj.co_linetable, obj.co_freevars,
+            obj.co_cellvars
+    )
+    elif hasattr(obj, "co_posonlyargcount"): # python 3.8 (16 args)
+        args = (
+            obj.co_argcount, obj.co_posonlyargcount,
+            obj.co_kwonlyargcount, obj.co_nlocals, obj.co_stacksize,
+            obj.co_flags, obj.co_code, obj.co_consts, obj.co_names,
+            obj.co_varnames, obj.co_filename, obj.co_name,
+            obj.co_firstlineno, obj.co_lnotab, obj.co_freevars,
+            obj.co_cellvars
+    )
+    else: # python 3.7 (15 args)
+        args = (
+            obj.co_argcount, obj.co_kwonlyargcount, obj.co_nlocals,
+            obj.co_stacksize, obj.co_flags, obj.co_code, obj.co_consts,
+            obj.co_names, obj.co_varnames, obj.co_filename,
+            obj.co_name, obj.co_firstlineno, obj.co_lnotab,
+            obj.co_freevars, obj.co_cellvars
+    )
 
     pickler.save_reduce(_create_code, args, obj=obj)
-    log.info("# Co")
+    logger.trace(pickler, "# Co")
     return
 
+def _repr_dict(obj):
+    """make a short string representation of a dictionary"""
+    return "<%s object at %#012x>" % (type(obj).__name__, id(obj))
+
 @register(dict)
 def save_module_dict(pickler, obj):
     if is_dill(pickler, child=False) and obj == pickler._main.__dict__ and \
             not (pickler._session and pickler._first_pass):
-        log.info("D1: <dict%s" % str(obj.__repr__).split('dict')[-1]) # obj
-        if PY3:
-            pickler.write(bytes('c__builtin__\n__main__\n', 'UTF-8'))
-        else:
-            pickler.write('c__builtin__\n__main__\n')
-        log.info("# D1")
+        logger.trace(pickler, "D1: %s", _repr_dict(obj)) # obj
+        pickler.write(bytes('c__builtin__\n__main__\n', 'UTF-8'))
+        logger.trace(pickler, "# D1")
     elif (not is_dill(pickler, child=False)) and (obj == _main_module.__dict__):
-        log.info("D3: <dict%s" % str(obj.__repr__).split('dict')[-1]) # obj
-        if PY3:
-            pickler.write(bytes('c__main__\n__dict__\n', 'UTF-8'))
-        else:
-            pickler.write('c__main__\n__dict__\n')   #XXX: works in general?
-        log.info("# D3")
+        logger.trace(pickler, "D3: %s", _repr_dict(obj)) # obj
+        pickler.write(bytes('c__main__\n__dict__\n', 'UTF-8'))  #XXX: works in general?
+        logger.trace(pickler, "# D3")
     elif '__name__' in obj and obj != _main_module.__dict__ \
-    and type(obj['__name__']) is str \
-    and obj is getattr(_import_module(obj['__name__'],True), '__dict__', None):
-        log.info("D4: <dict%s" % str(obj.__repr__).split('dict')[-1]) # obj
-        if PY3:
-            pickler.write(bytes('c%s\n__dict__\n' % obj['__name__'], 'UTF-8'))
-        else:
-            pickler.write('c%s\n__dict__\n' % obj['__name__'])
-        log.info("# D4")
+            and type(obj['__name__']) is str \
+            and obj is getattr(_import_module(obj['__name__'],True), '__dict__', None):
+        logger.trace(pickler, "D4: %s", _repr_dict(obj)) # obj
+        pickler.write(bytes('c%s\n__dict__\n' % obj['__name__'], 'UTF-8'))
+        logger.trace(pickler, "# D4")
     else:
-        log.info("D2: <dict%s" % str(obj.__repr__).split('dict')[-1]) # obj
+        logger.trace(pickler, "D2: %s", _repr_dict(obj)) # obj
         if is_dill(pickler, child=False) and pickler._session:
             # we only care about session the first pass thru
             pickler._first_pass = False
         StockPickler.save_dict(pickler, obj)
-        log.info("# D2")
+        logger.trace(pickler, "# D2")
     return
 
 
 if not OLD310 and MAPPING_PROXY_TRICK:
     def save_dict_view(dicttype):
         def save_dict_view_for_function(func):
             def _save_dict_view(pickler, obj):
-                log.info("Dkvi: <%s>" % (obj,))
+                logger.trace(pickler, "Dkvi: <%s>", obj)
                 mapping = obj.mapping | _dictproxy_helper_instance
                 pickler.save_reduce(func, (mapping,), obj=obj)
-                log.info("# Dkvi")
+                logger.trace(pickler, "# Dkvi")
             return _save_dict_view
         return [
             (funcname, save_dict_view_for_function(getattr(dicttype, funcname)))
             for funcname in ('keys', 'values', 'items')
         ]
 else:
     # The following functions are based on 'cloudpickle'
     # https://github.com/cloudpipe/cloudpickle/blob/5d89947288a18029672596a4d719093cc6d5a412/cloudpickle/cloudpickle.py#L922-L940
     # Copyright (c) 2012, Regents of the University of California.
     # Copyright (c) 2009 `PiCloud, Inc. <http://www.picloud.com>`_.
     # License: https://github.com/cloudpipe/cloudpickle/blob/master/LICENSE
     def save_dict_view(dicttype):
         def save_dict_keys(pickler, obj):
-            log.info("Dk: <%s>" % (obj,))
+            logger.trace(pickler, "Dk: <%s>", obj)
             dict_constructor = _shims.Reduce(dicttype.fromkeys, (list(obj),))
             pickler.save_reduce(dicttype.keys, (dict_constructor,), obj=obj)
-            log.info("# Dk")
+            logger.trace(pickler, "# Dk")
 
         def save_dict_values(pickler, obj):
-            log.info("Dv: <%s>" % (obj,))
+            logger.trace(pickler, "Dv: <%s>", obj)
             dict_constructor = _shims.Reduce(dicttype, (enumerate(obj),))
             pickler.save_reduce(dicttype.values, (dict_constructor,), obj=obj)
-            log.info("# Dv")
+            logger.trace(pickler, "# Dv")
 
         def save_dict_items(pickler, obj):
-            log.info("Di: <%s>" % (obj,))
+            logger.trace(pickler, "Di: <%s>", obj)
             pickler.save_reduce(dicttype.items, (dicttype(obj),), obj=obj)
-            log.info("# Di")
+            logger.trace(pickler, "# Di")
 
         return (
             ('keys', save_dict_keys),
             ('values', save_dict_values),
             ('items', save_dict_items)
         )
 
@@ -1307,70 +1242,66 @@
             Pickler.dispatch[__tview] = __savefunc
 del __dicttype, __obj, __funcname, __tview, __savefunc
 
 
 @register(ClassType)
 def save_classobj(pickler, obj): #FIXME: enable pickler._byref
     if not _locate_function(obj, pickler):
-        log.info("C1: %s" % obj)
+        logger.trace(pickler, "C1: %s", obj)
         pickler.save_reduce(ClassType, (obj.__name__, obj.__bases__,
                                         obj.__dict__), obj=obj)
                                        #XXX: or obj.__dict__.copy()), obj=obj) ?
-        log.info("# C1")
+        logger.trace(pickler, "# C1")
     else:
-        log.info("C2: %s" % obj)
+        logger.trace(pickler, "C2: %s", obj)
         name = getattr(obj, '__qualname__', getattr(obj, '__name__', None))
         StockPickler.save_global(pickler, obj, name=name)
-        log.info("# C2")
+        logger.trace(pickler, "# C2")
+    return
+
+@register(typing._GenericAlias)
+def save_generic_alias(pickler, obj):
+    args = obj.__args__
+    if type(obj.__reduce__()) is str:
+        logger.trace(pickler, "Ga0: %s", obj)
+        StockPickler.save_global(pickler, obj, name=obj.__reduce__())
+        logger.trace(pickler, "# Ga0")
+    elif obj.__origin__ is tuple and (not args or args == ((),)):
+        logger.trace(pickler, "Ga1: %s", obj)
+        pickler.save_reduce(_create_typing_tuple, (args,), obj=obj)
+        logger.trace(pickler, "# Ga1")
+    else:
+        logger.trace(pickler, "Ga2: %s", obj)
+        StockPickler.save_reduce(pickler, *obj.__reduce__(), obj=obj)
+        logger.trace(pickler, "# Ga2")
     return
 
 @register(LockType)
 def save_lock(pickler, obj):
-    log.info("Lo: %s" % obj)
+    logger.trace(pickler, "Lo: %s", obj)
     pickler.save_reduce(_create_lock, (obj.locked(),), obj=obj)
-    log.info("# Lo")
+    logger.trace(pickler, "# Lo")
     return
 
 @register(RLockType)
 def save_rlock(pickler, obj):
-    log.info("RL: %s" % obj)
+    logger.trace(pickler, "RL: %s", obj)
     r = obj.__repr__() # don't use _release_save as it unlocks the lock
     count = int(r.split('count=')[1].split()[0].rstrip('>'))
-    owner = int(r.split('owner=')[1].split()[0]) if PY3 else getattr(obj, '_RLock__owner')
+    owner = int(r.split('owner=')[1].split()[0])
     pickler.save_reduce(_create_rlock, (count,owner,), obj=obj)
-    log.info("# RL")
+    logger.trace(pickler, "# RL")
     return
 
-if not IS_PYPY2:
-    #@register(SocketType) #FIXME: causes multiprocess test_pickling FAIL
-    def save_socket(pickler, obj):
-        log.info("So: %s" % obj)
-        pickler.save_reduce(*reduce_socket(obj))
-        log.info("# So")
-        return
-
-if sys.hexversion <= 0x3050000:
-    @register(ItemGetterType)
-    def save_itemgetter(pickler, obj):
-        log.info("Ig: %s" % obj)
-        helper = _itemgetter_helper()
-        obj(helper)
-        pickler.save_reduce(type(obj), tuple(helper.items), obj=obj)
-        log.info("# Ig")
-        return
-
-    @register(AttrGetterType)
-    def save_attrgetter(pickler, obj):
-        log.info("Ag: %s" % obj)
-        attrs = []
-        helper = _attrgetter_helper(attrs)
-        obj(helper)
-        pickler.save_reduce(type(obj), tuple(attrs), obj=obj)
-        log.info("# Ag")
-        return
+#@register(SocketType) #FIXME: causes multiprocess test_pickling FAIL
+def save_socket(pickler, obj):
+    logger.trace(pickler, "So: %s", obj)
+    pickler.save_reduce(*reduce_socket(obj))
+    logger.trace(pickler, "# So")
+    return
 
 def _save_file(pickler, obj, open_):
     if obj.closed:
         position = 0
     else:
         obj.flush()
         if obj in (sys.__stdout__, sys.__stderr__, sys.__stdin__):
@@ -1397,270 +1328,207 @@
 
 @register(FileType) #XXX: in 3.x has buffer=0, needs different _create?
 @register(BufferedRandomType)
 @register(BufferedReaderType)
 @register(BufferedWriterType)
 @register(TextWrapperType)
 def save_file(pickler, obj):
-    log.info("Fi: %s" % obj)
+    logger.trace(pickler, "Fi: %s", obj)
     f = _save_file(pickler, obj, open)
-    log.info("# Fi")
+    logger.trace(pickler, "# Fi")
     return f
 
 if PyTextWrapperType:
     @register(PyBufferedRandomType)
     @register(PyBufferedReaderType)
     @register(PyBufferedWriterType)
     @register(PyTextWrapperType)
     def save_file(pickler, obj):
-        log.info("Fi: %s" % obj)
+        logger.trace(pickler, "Fi: %s", obj)
         f = _save_file(pickler, obj, _open)
-        log.info("# Fi")
+        logger.trace(pickler, "# Fi")
         return f
 
 # The following two functions are based on 'saveCStringIoInput'
 # and 'saveCStringIoOutput' from spickle
 # Copyright (c) 2011 by science+computing ag
 # License: http://www.apache.org/licenses/LICENSE-2.0
 if InputType:
     @register(InputType)
     def save_stringi(pickler, obj):
-        log.info("Io: %s" % obj)
+        logger.trace(pickler, "Io: %s", obj)
         if obj.closed:
             value = ''; position = 0
         else:
             value = obj.getvalue(); position = obj.tell()
         pickler.save_reduce(_create_stringi, (value, position, \
                                               obj.closed), obj=obj)
-        log.info("# Io")
+        logger.trace(pickler, "# Io")
         return
 
     @register(OutputType)
     def save_stringo(pickler, obj):
-        log.info("Io: %s" % obj)
+        logger.trace(pickler, "Io: %s", obj)
         if obj.closed:
             value = ''; position = 0
         else:
             value = obj.getvalue(); position = obj.tell()
         pickler.save_reduce(_create_stringo, (value, position, \
                                               obj.closed), obj=obj)
-        log.info("# Io")
-        return
-
-if 0x2050000 <= sys.hexversion < 0x3010000:
-    @register(PartialType)
-    def save_functor(pickler, obj):
-        log.info("Fu: %s" % obj)
-        pickler.save_reduce(_create_ftype, (type(obj), obj.func, obj.args,
-                                            obj.keywords), obj=obj)
-        log.info("# Fu")
+        logger.trace(pickler, "# Io")
         return
 
 if LRUCacheType is not None:
     from functools import lru_cache
     @register(LRUCacheType)
     def save_lru_cache(pickler, obj):
-        log.info("LRU: %s" % obj)
+        logger.trace(pickler, "LRU: %s", obj)
         if OLD39:
             kwargs = obj.cache_info()
             args = (kwargs.maxsize,)
         else:
             kwargs = obj.cache_parameters()
             args = (kwargs['maxsize'], kwargs['typed'])
         if args != lru_cache.__defaults__:
             wrapper = Reduce(lru_cache, args, is_callable=True)
         else:
             wrapper = lru_cache
         pickler.save_reduce(wrapper, (obj.__wrapped__,), obj=obj)
-        log.info("# LRU")
+        logger.trace(pickler, "# LRU")
         return
 
 @register(SuperType)
 def save_super(pickler, obj):
-    log.info("Su: %s" % obj)
+    logger.trace(pickler, "Su: %s", obj)
     pickler.save_reduce(super, (obj.__thisclass__, obj.__self__), obj=obj)
-    log.info("# Su")
+    logger.trace(pickler, "# Su")
     return
 
-if OLDER or not PY3:
-    @register(BuiltinMethodType)
-    def save_builtin_method(pickler, obj):
-        if obj.__self__ is not None:
-            if obj.__self__ is __builtin__:
-                module = 'builtins' if PY3 else '__builtin__'
-                _t = "B1"
-                log.info("%s: %s" % (_t, obj))
-            else:
-                module = obj.__self__
-                _t = "B3"
-                log.info("%s: %s" % (_t, obj))
-            if is_dill(pickler, child=True):
-                _recurse = pickler._recurse
-                pickler._recurse = False
-            pickler.save_reduce(_get_attr, (module, obj.__name__), obj=obj)
-            if is_dill(pickler, child=True):
-                pickler._recurse = _recurse
-            log.info("# %s" % _t)
-        else:
-            log.info("B2: %s" % obj)
-            name = getattr(obj, '__qualname__', getattr(obj, '__name__', None))
-            StockPickler.save_global(pickler, obj, name=name)
-            log.info("# B2")
-        return
-
-    @register(MethodType) #FIXME: fails for 'hidden' or 'name-mangled' classes
-    def save_instancemethod0(pickler, obj):# example: cStringIO.StringI
-        log.info("Me: %s" % obj) #XXX: obj.__dict__ handled elsewhere?
-        if PY3:
-            pickler.save_reduce(MethodType, (obj.__func__, obj.__self__), obj=obj)
-        else:
-            pickler.save_reduce(MethodType, (obj.im_func, obj.im_self,
-                                             obj.im_class), obj=obj)
-        log.info("# Me")
-        return
-
-if sys.hexversion >= 0x20500f0:
-    if not IS_PYPY:
-        @register(MemberDescriptorType)
-        @register(GetSetDescriptorType)
-        @register(MethodDescriptorType)
-        @register(WrapperDescriptorType)
-        @register(ClassMethodDescriptorType)
-        def save_wrapper_descriptor(pickler, obj):
-            log.info("Wr: %s" % obj)
-            pickler.save_reduce(_getattr, (obj.__objclass__, obj.__name__,
-                                           obj.__repr__()), obj=obj)
-            log.info("# Wr")
-            return
-    else:
-        @register(MemberDescriptorType)
-        @register(GetSetDescriptorType)
-        def save_wrapper_descriptor(pickler, obj):
-            log.info("Wr: %s" % obj)
-            pickler.save_reduce(_getattr, (obj.__objclass__, obj.__name__,
-                                           obj.__repr__()), obj=obj)
-            log.info("# Wr")
+if IS_PYPY:
+    @register(MethodType)
+    def save_instancemethod0(pickler, obj):
+        code = getattr(obj.__func__, '__code__', None)
+        if code is not None and type(code) is not CodeType \
+              and getattr(obj.__self__, obj.__name__) == obj:
+            # Some PyPy builtin functions have no module name
+            logger.trace(pickler, "Me2: %s", obj)
+            # TODO: verify that this works for all PyPy builtin methods
+            pickler.save_reduce(getattr, (obj.__self__, obj.__name__), obj=obj)
+            logger.trace(pickler, "# Me2")
             return
 
-    @register(MethodWrapperType)
-    def save_instancemethod(pickler, obj):
-        log.info("Mw: %s" % obj)
-        if IS_PYPY2 and obj.__self__ is None and obj.im_class:
-            # Can be a class method in PYPY2 if __self__ is none
-            pickler.save_reduce(getattr, (obj.im_class, obj.__name__), obj=obj)
-            return
-        pickler.save_reduce(getattr, (obj.__self__, obj.__name__), obj=obj)
-        log.info("# Mw")
+        logger.trace(pickler, "Me1: %s", obj)
+        pickler.save_reduce(MethodType, (obj.__func__, obj.__self__), obj=obj)
+        logger.trace(pickler, "# Me1")
+        return
+else:
+    @register(MethodType)
+    def save_instancemethod0(pickler, obj):
+        logger.trace(pickler, "Me1: %s", obj)
+        pickler.save_reduce(MethodType, (obj.__func__, obj.__self__), obj=obj)
+        logger.trace(pickler, "# Me1")
         return
 
-elif not IS_PYPY:
+if not IS_PYPY:
+    @register(MemberDescriptorType)
+    @register(GetSetDescriptorType)
     @register(MethodDescriptorType)
     @register(WrapperDescriptorType)
+    @register(ClassMethodDescriptorType)
+    def save_wrapper_descriptor(pickler, obj):
+        logger.trace(pickler, "Wr: %s", obj)
+        pickler.save_reduce(_getattr, (obj.__objclass__, obj.__name__,
+                                       obj.__repr__()), obj=obj)
+        logger.trace(pickler, "# Wr")
+        return
+else:
+    @register(MemberDescriptorType)
+    @register(GetSetDescriptorType)
     def save_wrapper_descriptor(pickler, obj):
-        log.info("Wr: %s" % obj)
+        logger.trace(pickler, "Wr: %s", obj)
         pickler.save_reduce(_getattr, (obj.__objclass__, obj.__name__,
                                        obj.__repr__()), obj=obj)
-        log.info("# Wr")
+        logger.trace(pickler, "# Wr")
         return
 
 @register(CellType)
 def save_cell(pickler, obj):
     try:
         f = obj.cell_contents
-    except:
-        log.info("Ce3: %s" % obj)
+    except ValueError: # cell is empty
+        logger.trace(pickler, "Ce3: %s", obj)
         # _shims._CELL_EMPTY is defined in _shims.py to support PyPy 2.7.
         # It unpickles to a sentinel object _dill._CELL_EMPTY, also created in
         # _shims.py. This object is not present in Python 3 because the cell's
         # contents can be deleted in newer versions of Python. The reduce object
         # will instead unpickle to None if unpickled in Python 3.
 
         # When breaking changes are made to dill, (_shims._CELL_EMPTY,) can
         # be replaced by () OR the delattr function can be removed repending on
         # whichever is more convienient.
         pickler.save_reduce(_create_cell, (_shims._CELL_EMPTY,), obj=obj)
         # Call the function _delattr on the cell's cell_contents attribute
         # The result of this function call will be None
         pickler.save_reduce(_shims._delattr, (obj, 'cell_contents'))
         # pop None created by calling _delattr off stack
-        if PY3:
-            pickler.write(bytes('0', 'UTF-8'))
-        else:
-            pickler.write('0')
-        log.info("# Ce3")
+        pickler.write(bytes('0', 'UTF-8'))
+        logger.trace(pickler, "# Ce3")
         return
     if is_dill(pickler, child=True):
         if id(f) in pickler._postproc:
             # Already seen. Add to its postprocessing.
             postproc = pickler._postproc[id(f)]
         else:
             # Haven't seen it. Add to the highest possible object and set its
             # value as late as possible to prevent cycle.
             postproc = next(iter(pickler._postproc.values()), None)
         if postproc is not None:
-            log.info("Ce2: %s" % obj)
+            logger.trace(pickler, "Ce2: %s", obj)
             # _CELL_REF is defined in _shims.py to support older versions of
             # dill. When breaking changes are made to dill, (_CELL_REF,) can
             # be replaced by ()
             pickler.save_reduce(_create_cell, (_CELL_REF,), obj=obj)
             postproc.append((_shims._setattr, (obj, 'cell_contents', f)))
-            log.info("# Ce2")
+            logger.trace(pickler, "# Ce2")
             return
-    log.info("Ce1: %s" % obj)
+    logger.trace(pickler, "Ce1: %s", obj)
     pickler.save_reduce(_create_cell, (f,), obj=obj)
-    log.info("# Ce1")
+    logger.trace(pickler, "# Ce1")
     return
 
 if MAPPING_PROXY_TRICK:
     @register(DictProxyType)
     def save_dictproxy(pickler, obj):
-        log.info("Mp: %s" % obj)
+        logger.trace(pickler, "Mp: %s", _repr_dict(obj)) # obj
         mapping = obj | _dictproxy_helper_instance
         pickler.save_reduce(DictProxyType, (mapping,), obj=obj)
-        log.info("# Mp")
+        logger.trace(pickler, "# Mp")
+        return
+else:
+    @register(DictProxyType)
+    def save_dictproxy(pickler, obj):
+        logger.trace(pickler, "Mp: %s", _repr_dict(obj)) # obj
+        pickler.save_reduce(DictProxyType, (obj.copy(),), obj=obj)
+        logger.trace(pickler, "# Mp")
         return
-elif not IS_PYPY:
-    if not OLD33:
-        @register(DictProxyType)
-        def save_dictproxy(pickler, obj):
-            log.info("Mp: %s" % obj)
-            pickler.save_reduce(DictProxyType, (obj.copy(),), obj=obj)
-            log.info("# Mp")
-            return
-    else:
-        # The following function is based on 'saveDictProxy' from spickle
-        # Copyright (c) 2011 by science+computing ag
-        # License: http://www.apache.org/licenses/LICENSE-2.0
-        @register(DictProxyType)
-        def save_dictproxy(pickler, obj):
-            log.info("Dp: %s" % obj)
-            attr = obj.get('__dict__')
-           #pickler.save_reduce(_create_dictproxy, (attr,'nested'), obj=obj)
-            if type(attr) == GetSetDescriptorType and attr.__name__ == "__dict__" \
-            and getattr(attr.__objclass__, "__dict__", None) == obj:
-                pickler.save_reduce(getattr, (attr.__objclass__,"__dict__"),obj=obj)
-                log.info("# Dp")
-                return
-            # all bad below... so throw ReferenceError or TypeError
-            raise ReferenceError("%s does not reference a class __dict__" % obj)
 
 @register(SliceType)
 def save_slice(pickler, obj):
-    log.info("Sl: %s" % obj)
+    logger.trace(pickler, "Sl: %s", obj)
     pickler.save_reduce(slice, (obj.start, obj.stop, obj.step), obj=obj)
-    log.info("# Sl")
+    logger.trace(pickler, "# Sl")
     return
 
 @register(XRangeType)
 @register(EllipsisType)
 @register(NotImplementedType)
 def save_singleton(pickler, obj):
-    log.info("Si: %s" % obj)
+    logger.trace(pickler, "Si: %s", obj)
     pickler.save_reduce(_eval_repr, (obj.__repr__(),), obj=obj)
-    log.info("# Si")
+    logger.trace(pickler, "# Si")
     return
 
 def _proxy_helper(obj): # a dead proxy returns a reference to None
     """get memory address of proxy's reference object"""
     _repr = repr(obj)
     try: _str = str(obj)
     except ReferenceError: # it's a dead proxy
@@ -1682,225 +1550,222 @@
 
 def _locate_object(address, module=None):
     """get object located at the given memory address (inverse of id(obj))"""
     special = [None, True, False] #XXX: more...?
     for obj in special:
         if address == id(obj): return obj
     if module:
-        if PY3:
-            objects = iter(module.__dict__.values())
-        else:
-            objects = module.__dict__.itervalues()
+        objects = iter(module.__dict__.values())
     else: objects = iter(gc.get_objects())
     for obj in objects:
         if address == id(obj): return obj
     # all bad below... nothing found so throw ReferenceError or TypeError
     try: address = hex(address)
     except TypeError:
         raise TypeError("'%s' is not a valid memory address" % str(address))
     raise ReferenceError("Cannot reference object at '%s'" % address)
 
 @register(ReferenceType)
 def save_weakref(pickler, obj):
     refobj = obj()
-    log.info("R1: %s" % obj)
+    logger.trace(pickler, "R1: %s", obj)
    #refobj = ctypes.pythonapi.PyWeakref_GetObject(obj) # dead returns "None"
     pickler.save_reduce(_create_weakref, (refobj,), obj=obj)
-    log.info("# R1")
+    logger.trace(pickler, "# R1")
     return
 
 @register(ProxyType)
 @register(CallableProxyType)
 def save_weakproxy(pickler, obj):
+    # Must do string substitution here and use %r to avoid ReferenceError.
+    logger.trace(pickler, "R2: %r" % obj)
     refobj = _locate_object(_proxy_helper(obj))
-    try:
-        _t = "R2"
-        log.info("%s: %s" % (_t, obj))
-    except ReferenceError:
-        _t = "R3"
-        log.info("%s: %s" % (_t, sys.exc_info()[1]))
-   #callable = bool(getattr(refobj, '__call__', None))
-    if type(obj) is CallableProxyType: callable = True
-    else: callable = False
-    pickler.save_reduce(_create_weakproxy, (refobj, callable), obj=obj)
-    log.info("# %s" % _t)
+    pickler.save_reduce(_create_weakproxy, (refobj, callable(obj)), obj=obj)
+    logger.trace(pickler, "# R2")
     return
 
 def _is_builtin_module(module):
     if not hasattr(module, "__file__"): return True
     # If a module file name starts with prefix, it should be a builtin
     # module, so should always be pickled as a reference.
     names = ["base_prefix", "base_exec_prefix", "exec_prefix", "prefix", "real_prefix"]
     return any(os.path.realpath(module.__file__).startswith(os.path.realpath(getattr(sys, name)))
                for name in names if hasattr(sys, name)) or \
             module.__file__.endswith(EXTENSION_SUFFIXES) or \
             'site-packages' in module.__file__
 
+def _is_imported_module(module):
+    return getattr(module, '__loader__', None) is not None or module in sys.modules.values()
+
 @register(ModuleType)
 def save_module(pickler, obj):
     if False: #_use_diff:
         if obj.__name__.split('.', 1)[0] != "dill":
             try:
                 changed = diff.whats_changed(obj, seen=pickler._diff_cache)[0]
             except RuntimeError:  # not memorised module, probably part of dill
                 pass
             else:
-                log.info("M2: %s with diff" % obj)
-                log.info("Diff: %s", changed.keys())
+                logger.trace(pickler, "M2: %s with diff", obj)
+                logger.trace(pickler, "Diff: %s", changed.keys())
                 pickler.save_reduce(_import_module, (obj.__name__,), obj=obj,
                                     state=changed)
-                log.info("# M2")
+                logger.trace(pickler, "# M2")
                 return
 
-        log.info("M1: %s" % obj)
+        logger.trace(pickler, "M1: %s", obj)
         pickler.save_reduce(_import_module, (obj.__name__,), obj=obj)
-        log.info("# M1")
+        logger.trace(pickler, "# M1")
     else:
         builtin_mod = _is_builtin_module(obj)
         if obj.__name__ not in ("builtins", "dill", "dill._dill") and not builtin_mod or \
                 is_dill(pickler, child=True) and obj is pickler._main:
-            log.info("M1: %s" % obj)
+            logger.trace(pickler, "M1: %s", obj)
             _main_dict = obj.__dict__.copy() #XXX: better no copy? option to copy?
             [_main_dict.pop(item, None) for item in singletontypes
                 + ["__builtins__", "__loader__"]]
-            pickler.save_reduce(_import_module, (obj.__name__,), obj=obj,
+            mod_name = obj.__name__ if _is_imported_module(obj) else '__runtime__.%s' % obj.__name__
+            pickler.save_reduce(_import_module, (mod_name,), obj=obj,
                                 state=_main_dict)
-            log.info("# M1")
-        elif PY3 and obj.__name__ == "dill._dill":
-            log.info("M2: %s" % obj)
+            logger.trace(pickler, "# M1")
+        elif obj.__name__ == "dill._dill":
+            logger.trace(pickler, "M2: %s", obj)
             pickler.save_global(obj, name="_dill")
-            log.info("# M2")
+            logger.trace(pickler, "# M2")
         else:
-            log.info("M2: %s" % obj)
+            logger.trace(pickler, "M2: %s", obj)
             pickler.save_reduce(_import_module, (obj.__name__,), obj=obj)
-            log.info("# M2")
+            logger.trace(pickler, "# M2")
         return
     return
 
 @register(TypeType)
 def save_type(pickler, obj, postproc_list=None):
     if obj in _typemap:
-        log.info("T1: %s" % obj)
+        logger.trace(pickler, "T1: %s", obj)
+        # if obj in _incedental_types:
+        #     warnings.warn('Type %r may only exist on this implementation of Python and cannot be unpickled in other implementations.' % (obj,), PicklingWarning)
         pickler.save_reduce(_load_type, (_typemap[obj],), obj=obj)
-        log.info("# T1")
+        logger.trace(pickler, "# T1")
     elif obj.__bases__ == (tuple,) and all([hasattr(obj, attr) for attr in ('_fields','_asdict','_make','_replace')]):
         # special case: namedtuples
-        log.info("T6: %s" % obj)
-        if OLD37 or (not obj._field_defaults):
+        logger.trace(pickler, "T6: %s", obj)
+        if not obj._field_defaults:
             pickler.save_reduce(_create_namedtuple, (obj.__name__, obj._fields, obj.__module__), obj=obj)
         else:
             defaults = [obj._field_defaults[field] for field in obj._fields if field in obj._field_defaults]
             pickler.save_reduce(_create_namedtuple, (obj.__name__, obj._fields, obj.__module__, defaults), obj=obj)
-        log.info("# T6")
+        logger.trace(pickler, "# T6")
         return
 
     # special cases: NoneType, NotImplementedType, EllipsisType
     elif obj is type(None):
-        log.info("T7: %s" % obj)
+        logger.trace(pickler, "T7: %s", obj)
         #XXX: pickler.save_reduce(type, (None,), obj=obj)
-        if PY3:
-            pickler.write(bytes('c__builtin__\nNoneType\n', 'UTF-8'))
-        else:
-            pickler.write('c__builtin__\nNoneType\n')
-        log.info("# T7")
+        pickler.write(bytes('c__builtin__\nNoneType\n', 'UTF-8'))
+        logger.trace(pickler, "# T7")
     elif obj is NotImplementedType:
-        log.info("T7: %s" % obj)
+        logger.trace(pickler, "T7: %s", obj)
         pickler.save_reduce(type, (NotImplemented,), obj=obj)
-        log.info("# T7")
+        logger.trace(pickler, "# T7")
     elif obj is EllipsisType:
-        log.info("T7: %s" % obj)
+        logger.trace(pickler, "T7: %s", obj)
         pickler.save_reduce(type, (Ellipsis,), obj=obj)
-        log.info("# T7")
+        logger.trace(pickler, "# T7")
 
     else:
         obj_name = getattr(obj, '__qualname__', getattr(obj, '__name__', None))
         _byref = getattr(pickler, '_byref', None)
         obj_recursive = id(obj) in getattr(pickler, '_postproc', ())
         incorrectly_named = not _locate_function(obj, pickler)
         if not _byref and not obj_recursive and incorrectly_named: # not a function, but the name was held over
-            if issubclass(type(obj), type):
-                # thanks to Tom Stepleton pointing out pickler._session unneeded
-                _t = 'T2'
-                log.info("%s: %s" % (_t, obj))
-                _dict = _dict_from_dictproxy(obj.__dict__)
-            else:
-                _t = 'T3'
-                log.info("%s: %s" % (_t, obj))
-                _dict = obj.__dict__
+            # thanks to Tom Stepleton pointing out pickler._session unneeded
+            logger.trace(pickler, "T2: %s", obj)
+            _dict = obj.__dict__.copy() # convert dictproxy to dict
            #print (_dict)
            #print ("%s\n%s" % (type(obj), obj.__name__))
            #print ("%s\n%s" % (obj.__bases__, obj.__dict__))
-            for name in _dict.get("__slots__", []):
+            slots = _dict.get('__slots__', ())
+            if type(slots) == str: slots = (slots,) # __slots__ accepts a single string
+            for name in slots:
                 del _dict[name]
-            if PY3 and obj_name != obj.__name__:
+            _dict.pop('__dict__', None)
+            _dict.pop('__weakref__', None)
+            _dict.pop('__prepare__', None)
+            if obj_name != obj.__name__:
                 if postproc_list is None:
                     postproc_list = []
                 postproc_list.append((setattr, (obj, '__qualname__', obj_name)))
             _save_with_postproc(pickler, (_create_type, (
                 type(obj), obj.__name__, obj.__bases__, _dict
             )), obj=obj, postproc_list=postproc_list)
-            log.info("# %s" % _t)
+            logger.trace(pickler, "# T2")
         else:
-            log.info("T4: %s" % obj)
+            logger.trace(pickler, "T4: %s", obj)
             if incorrectly_named:
                 warnings.warn('Cannot locate reference to %r.' % (obj,), PicklingWarning)
             if obj_recursive:
                 warnings.warn('Cannot pickle %r: %s.%s has recursive self-references that trigger a RecursionError.' % (obj, obj.__module__, obj_name), PicklingWarning)
            #print (obj.__dict__)
            #print ("%s\n%s" % (type(obj), obj.__name__))
            #print ("%s\n%s" % (obj.__bases__, obj.__dict__))
             StockPickler.save_global(pickler, obj, name=obj_name)
-            log.info("# T4")
+            logger.trace(pickler, "# T4")
     return
 
-# Error in PyPy 2.7 when adding ABC support
-if IS_PYPY2:
-    @register(FrameType)
-    def save_frame(pickler, obj):
-        raise PicklingError('Cannot pickle a Python stack frame')
-
 @register(property)
 def save_property(pickler, obj):
-    log.info("Pr: %s" % obj)
+    logger.trace(pickler, "Pr: %s", obj)
     pickler.save_reduce(property, (obj.fget, obj.fset, obj.fdel, obj.__doc__),
                         obj=obj)
-    log.info("# Pr")
+    logger.trace(pickler, "# Pr")
 
 @register(staticmethod)
 @register(classmethod)
 def save_classmethod(pickler, obj):
-    log.info("Cm: %s" % obj)
-    im_func = '__func__' if PY3 else 'im_func'
-    try:
-        orig_func = getattr(obj, im_func)
-    except AttributeError:  # Python 2.6
-        orig_func = obj.__get__(None, object)
-        if isinstance(obj, classmethod):
-            orig_func = getattr(orig_func, im_func) # Unbind
-
-    # if PY3:
-    #     if type(obj.__dict__) is dict:
-    #         if obj.__dict__:
-    #             state = obj.__dict__
-    #         else:
-    #             state = None
+    logger.trace(pickler, "Cm: %s", obj)
+    orig_func = obj.__func__
+
+    # if type(obj.__dict__) is dict:
+    #     if obj.__dict__:
+    #         state = obj.__dict__
     #     else:
-    #         state = (None, {'__dict__', obj.__dict__})
+    #         state = None
     # else:
-    #     state = None
+    #     state = (None, {'__dict__', obj.__dict__})
 
     pickler.save_reduce(type(obj), (orig_func,), obj=obj)
-    log.info("# Cm")
+    logger.trace(pickler, "# Cm")
 
 @register(FunctionType)
 def save_function(pickler, obj):
     if not _locate_function(obj, pickler):
-        log.info("F1: %s" % obj)
+        if type(obj.__code__) is not CodeType:
+            # Some PyPy builtin functions have no module name, and thus are not
+            # able to be located
+            module_name = getattr(obj, '__module__', None)
+            if module_name is None:
+                module_name = __builtin__.__name__
+            module = _import_module(module_name, safe=True)
+            _pypy_builtin = False
+            try:
+                found, _ = _getattribute(module, obj.__qualname__)
+                if getattr(found, '__func__', None) is obj:
+                    _pypy_builtin = True
+            except AttributeError:
+                pass
+
+            if _pypy_builtin:
+                logger.trace(pickler, "F3: %s", obj)
+                pickler.save_reduce(getattr, (found, '__func__'), obj=obj)
+                logger.trace(pickler, "# F3")
+                return
+
+        logger.trace(pickler, "F1: %s", obj)
         _recurse = getattr(pickler, '_recurse', None)
-        _byref = getattr(pickler, '_byref', None)
         _postproc = getattr(pickler, '_postproc', None)
         _main_modified = getattr(pickler, '_main_modified', None)
         _original_main = getattr(pickler, '_original_main', __builtin__)#'None'
         postproc_list = []
         if _recurse:
             # recurse to get all globals referred to by obj
             from .detect import globalvars
@@ -1908,15 +1773,15 @@
 
             # Add the name of the module to the globs dictionary to prevent
             # the duplication of the dictionary. Pickle the unpopulated
             # globals dictionary and set the remaining items after the function
             # is created to correctly handle recursion.
             globs = {'__name__': obj.__module__}
         else:
-            globs_copy = obj.__globals__ if PY3 else obj.func_globals
+            globs_copy = obj.__globals__
 
             # If the globals is the __dict__ from the module being saved as a
             # session, substitute it by the dictionary being actually saved.
             if _main_modified and globs_copy is _original_main.__dict__:
                 globs_copy = getattr(pickler, '_main', _original_main).__dict__
                 globs = globs_copy
             # If the globals is a module __dict__, do not save it in the pickle.
@@ -1926,61 +1791,44 @@
             else:
                 globs = {'__name__': obj.__module__}
 
         if globs_copy is not None and globs is not globs_copy:
             # In the case that the globals are copied, we need to ensure that
             # the globals dictionary is updated when all objects in the
             # dictionary are already created.
-            if PY3:
-                glob_ids = {id(g) for g in globs_copy.values()}
-            else:
-                glob_ids = {id(g) for g in globs_copy.itervalues()}
+            glob_ids = {id(g) for g in globs_copy.values()}
             for stack_element in _postproc:
                 if stack_element in glob_ids:
                     _postproc[stack_element].append((_setitems, (globs, globs_copy)))
                     break
             else:
                 postproc_list.append((_setitems, (globs, globs_copy)))
 
-        if PY3:
-            closure = obj.__closure__
-            state_dict = {}
-            for fattrname in ('__doc__', '__kwdefaults__', '__annotations__'):
-                fattr = getattr(obj, fattrname, None)
-                if fattr is not None:
-                    state_dict[fattrname] = fattr
-            if obj.__qualname__ != obj.__name__:
-                state_dict['__qualname__'] = obj.__qualname__
-            if '__name__' not in globs or obj.__module__ != globs['__name__']:
-                state_dict['__module__'] = obj.__module__
-
-            state = obj.__dict__
-            if type(state) is not dict:
-                state_dict['__dict__'] = state
-                state = None
-            if state_dict:
-                state = state, state_dict
-
-            _save_with_postproc(pickler, (_create_function, (
-                  obj.__code__, globs, obj.__name__, obj.__defaults__,
-                  closure
-            ), state), obj=obj, postproc_list=postproc_list)
-        else:
-            closure = obj.func_closure
-            if obj.__doc__ is not None:
-                postproc_list.append((setattr, (obj, '__doc__', obj.__doc__)))
-            if '__name__' not in globs or obj.__module__ != globs['__name__']:
-                postproc_list.append((setattr, (obj, '__module__', obj.__module__)))
-            if obj.__dict__:
-                postproc_list.append((setattr, (obj, '__dict__', obj.__dict__)))
+        closure = obj.__closure__
+        state_dict = {}
+        for fattrname in ('__doc__', '__kwdefaults__', '__annotations__'):
+            fattr = getattr(obj, fattrname, None)
+            if fattr is not None:
+                state_dict[fattrname] = fattr
+        if obj.__qualname__ != obj.__name__:
+            state_dict['__qualname__'] = obj.__qualname__
+        if '__name__' not in globs or obj.__module__ != globs['__name__']:
+            state_dict['__module__'] = obj.__module__
+
+        state = obj.__dict__
+        if type(state) is not dict:
+            state_dict['__dict__'] = state
+            state = None
+        if state_dict:
+            state = state, state_dict
 
-            _save_with_postproc(pickler, (_create_function, (
-                obj.func_code, globs, obj.func_name, obj.func_defaults,
+        _save_with_postproc(pickler, (_create_function, (
+                obj.__code__, globs, obj.__name__, obj.__defaults__,
                 closure
-            )), obj=obj, postproc_list=postproc_list)
+        ), state), obj=obj, postproc_list=postproc_list)
 
         # Lift closure cell update to earliest function (#458)
         if _postproc:
             topmost_postproc = next(iter(_postproc.values()), None)
             if closure and topmost_postproc:
                 for cell in closure:
                     possible_postproc = (setattr, (cell, 'cell_contents', obj))
@@ -1988,27 +1836,108 @@
                         topmost_postproc.remove(possible_postproc)
                     except ValueError:
                         continue
 
                     # Change the value of the cell
                     pickler.save_reduce(*possible_postproc)
                     # pop None created by calling preprocessing step off stack
-                    if PY3:
-                        pickler.write(bytes('0', 'UTF-8'))
-                    else:
-                        pickler.write('0')
+                    pickler.write(bytes('0', 'UTF-8'))
 
-        log.info("# F1")
+        logger.trace(pickler, "# F1")
     else:
-        log.info("F2: %s" % obj)
+        logger.trace(pickler, "F2: %s", obj)
         name = getattr(obj, '__qualname__', getattr(obj, '__name__', None))
         StockPickler.save_global(pickler, obj, name=name)
-        log.info("# F2")
+        logger.trace(pickler, "# F2")
     return
 
+if HAS_CTYPES and hasattr(ctypes, 'pythonapi'):
+    _PyCapsule_New = ctypes.pythonapi.PyCapsule_New
+    _PyCapsule_New.argtypes = (ctypes.c_void_p, ctypes.c_char_p, ctypes.c_void_p)
+    _PyCapsule_New.restype = ctypes.py_object
+    _PyCapsule_GetPointer = ctypes.pythonapi.PyCapsule_GetPointer
+    _PyCapsule_GetPointer.argtypes = (ctypes.py_object, ctypes.c_char_p)
+    _PyCapsule_GetPointer.restype = ctypes.c_void_p
+    _PyCapsule_GetDestructor = ctypes.pythonapi.PyCapsule_GetDestructor
+    _PyCapsule_GetDestructor.argtypes = (ctypes.py_object,)
+    _PyCapsule_GetDestructor.restype = ctypes.c_void_p
+    _PyCapsule_GetContext = ctypes.pythonapi.PyCapsule_GetContext
+    _PyCapsule_GetContext.argtypes = (ctypes.py_object,)
+    _PyCapsule_GetContext.restype = ctypes.c_void_p
+    _PyCapsule_GetName = ctypes.pythonapi.PyCapsule_GetName
+    _PyCapsule_GetName.argtypes = (ctypes.py_object,)
+    _PyCapsule_GetName.restype = ctypes.c_char_p
+    _PyCapsule_IsValid = ctypes.pythonapi.PyCapsule_IsValid
+    _PyCapsule_IsValid.argtypes = (ctypes.py_object, ctypes.c_char_p)
+    _PyCapsule_IsValid.restype = ctypes.c_bool
+    _PyCapsule_SetContext = ctypes.pythonapi.PyCapsule_SetContext
+    _PyCapsule_SetContext.argtypes = (ctypes.py_object, ctypes.c_void_p)
+    _PyCapsule_SetDestructor = ctypes.pythonapi.PyCapsule_SetDestructor
+    _PyCapsule_SetDestructor.argtypes = (ctypes.py_object, ctypes.c_void_p)
+    _PyCapsule_SetName = ctypes.pythonapi.PyCapsule_SetName
+    _PyCapsule_SetName.argtypes = (ctypes.py_object, ctypes.c_char_p)
+    _PyCapsule_SetPointer = ctypes.pythonapi.PyCapsule_SetPointer
+    _PyCapsule_SetPointer.argtypes = (ctypes.py_object, ctypes.c_void_p)
+    _testcapsule = _PyCapsule_New(
+        ctypes.cast(_PyCapsule_New, ctypes.c_void_p),
+        ctypes.create_string_buffer(b'dill._dill._testcapsule'),
+        None
+    )
+    PyCapsuleType = type(_testcapsule)
+    @register(PyCapsuleType)
+    def save_capsule(pickler, obj):
+        logger.trace(pickler, "Cap: %s", obj)
+        name = _PyCapsule_GetName(obj)
+        warnings.warn('Pickling a PyCapsule (%s) does not pickle any C data structures and could cause segmentation faults or other memory errors when unpickling.' % (name,), PicklingWarning)
+        pointer = _PyCapsule_GetPointer(obj, name)
+        context = _PyCapsule_GetContext(obj)
+        destructor = _PyCapsule_GetDestructor(obj)
+        pickler.save_reduce(_create_capsule, (pointer, name, context, destructor), obj=obj)
+        logger.trace(pickler, "# Cap")
+    _incedental_reverse_typemap['PyCapsuleType'] = PyCapsuleType
+    _reverse_typemap['PyCapsuleType'] = PyCapsuleType
+    _incedental_types.add(PyCapsuleType)
+else:
+    _testcapsule = None
+
+
+#############################
+# A quick fix for issue #500
+# This should be removed when a better solution is found.
+
+if hasattr(dataclasses, "_HAS_DEFAULT_FACTORY_CLASS"):
+    @register(dataclasses._HAS_DEFAULT_FACTORY_CLASS)
+    def save_dataclasses_HAS_DEFAULT_FACTORY_CLASS(pickler, obj):
+        logger.trace(pickler, "DcHDF: %s", obj)
+        pickler.write(GLOBAL + b"dataclasses\n_HAS_DEFAULT_FACTORY\n")
+        logger.trace(pickler, "# DcHDF")
+
+if hasattr(dataclasses, "MISSING"):
+    @register(type(dataclasses.MISSING))
+    def save_dataclasses_MISSING_TYPE(pickler, obj):
+        logger.trace(pickler, "DcM: %s", obj)
+        pickler.write(GLOBAL + b"dataclasses\nMISSING\n")
+        logger.trace(pickler, "# DcM")
+
+if hasattr(dataclasses, "KW_ONLY"):
+    @register(type(dataclasses.KW_ONLY))
+    def save_dataclasses_KW_ONLY_TYPE(pickler, obj):
+        logger.trace(pickler, "DcKWO: %s", obj)
+        pickler.write(GLOBAL + b"dataclasses\nKW_ONLY\n")
+        logger.trace(pickler, "# DcKWO")
+
+if hasattr(dataclasses, "_FIELD_BASE"):
+    @register(dataclasses._FIELD_BASE)
+    def save_dataclasses_FIELD_BASE(pickler, obj):
+        logger.trace(pickler, "DcFB: %s", obj)
+        pickler.write(GLOBAL + b"dataclasses\n" + obj.name.encode() + b"\n")
+        logger.trace(pickler, "# DcFB")
+
+#############################
+
 # quick sanity checking
 def pickles(obj,exact=False,safe=False,**kwds):
     """
     Quick check if object pickles with dill.
 
     If *exact=True* then an equality test is done to check if the reconstructed
     object matches the original object.
@@ -2016,22 +1945,22 @@
     If *safe=True* then any exception will raised in copy signal that the
     object is not picklable, otherwise only pickling errors will be trapped.
 
     Additional keyword arguments are as :func:`dumps` and :func:`loads`.
     """
     if safe: exceptions = (Exception,) # RuntimeError, ValueError
     else:
-        exceptions = (TypeError, AssertionError, PicklingError, UnpicklingError)
+        exceptions = (TypeError, AssertionError, NotImplementedError, PicklingError, UnpicklingError)
     try:
         pik = copy(obj, **kwds)
         #FIXME: should check types match first, then check content if "exact"
         try:
             #FIXME: should be "(pik == obj).all()" for numpy comparison, though that'll fail if shapes differ
             result = bool(pik.all() == obj.all())
-        except AttributeError:
+        except (AttributeError, TypeError):
             warnings.filterwarnings('ignore')
             result = pik == obj
             warnings.resetwarnings()
         if hasattr(result, 'toarray'): # for unusual types like sparse matrix
             result = result.toarray().all()
         if result: return True
         if not exact:
@@ -2083,25 +2012,24 @@
     if verbose:
         print(msg)
     return
 
 # use to protect against missing attributes
 def is_dill(pickler, child=None):
     "check the dill-ness of your pickler"
-    if (child is False) or PY34 or (not hasattr(pickler.__class__, 'mro')):
+    if child is False or not hasattr(pickler.__class__, 'mro'):
         return 'dill' in pickler.__module__
     return Pickler in pickler.__class__.mro()
 
 def _extend():
     """extend pickle with all of dill's registered types"""
     # need to have pickle not choke on _main_module?  use is_dill(pickler)
     for t,func in Pickler.dispatch.items():
         try:
             StockPickler.dispatch[t] = func
-        except: #TypeError, PicklingError, UnpicklingError
-            log.info("skip: %s" % t)
-        else: pass
+        except Exception: #TypeError, PicklingError, UnpicklingError
+            logger.trace(pickler, "skip: %s", t)
     return
 
 del diff, _use_diff, use_diff
 
 # EOF
```

### Comparing `dill-0.3.5.1/dill/_objects.py` & `dill-0.3.6/dill/_objects.py`

 * *Files 9% similar despite different names*

```diff
@@ -11,40 +11,29 @@
 """
 
 __all__ = ['registered','failures','succeeds']
 
 # helper imports
 import warnings; warnings.filterwarnings("ignore", category=DeprecationWarning)
 import sys
-PY3 = (hex(sys.hexversion) >= '0x30000f0')
-if PY3:
-    import queue as Queue
-    import dbm as anydbm
-else:
-    import Queue
-    import anydbm
-    import sets # deprecated/removed
-    import mutex # removed
-try:
-    from cStringIO import StringIO # has StringI and StringO types
-except ImportError: # only has StringIO type
-    if PY3:
-        from io import BytesIO as StringIO
-    else:
-        from StringIO import StringIO
+import queue as Queue
+import dbm as anydbm
+from io import BytesIO as StringIO
 import re
 import array
 import collections
 import codecs
 import struct
+import dataclasses
 import datetime
 import calendar
 import weakref
 import pprint
 import decimal
+import numbers
 import functools
 import itertools
 import operator
 import tempfile
 import shelve
 import zlib
 import gzip
@@ -52,24 +41,24 @@
 import tarfile
 import xdrlib
 import csv
 import hashlib
 import hmac
 import os
 import logging
+import logging.handlers
 import optparse
 #import __hello__
 import threading
 import socket
 import contextlib
 try:
     import bz2
     import sqlite3
-    if PY3: import dbm.ndbm as dbm
-    else: import dbm
+    import dbm.ndbm as dbm
     HAS_ALL = True
 except ImportError: # Ubuntu
     HAS_ALL = False
 try:
     #import curses
     #from curses import textpad, panel
     HAS_CURSES = True
@@ -108,39 +97,31 @@
 #   def _static(self): #XXX: test me
 #       pass
 class _newclass2(object):
     __slots__ = ['descriptor']
 def _function(x): yield x
 def _function2():
     try: raise
-    except:
+    except Exception:
         from sys import exc_info
         e, er, tb = exc_info()
         return er, tb
 if HAS_CTYPES:
     class _Struct(ctypes.Structure):
         pass
     _Struct._fields_ = [("_field", ctypes.c_int),("next", ctypes.POINTER(_Struct))]
 _filedescrip, _tempfile = tempfile.mkstemp('r') # deleted in cleanup
 _tmpf = tempfile.TemporaryFile('w')
 
-# put the objects in order, if possible
-try:
-    from collections import OrderedDict as odict
-except ImportError:
-    try:
-        from ordereddict import OrderedDict as odict
-    except ImportError:
-        odict = dict
 # objects used by dill for type declaration
-registered = d = odict()
+registered = d = {}
 # objects dill fails to pickle
-failures = x = odict()
+failures = x = {}
 # all other type objects
-succeeds = a = odict()
+succeeds = a = {}
 
 # types module (part of CH 8)
 a['BooleanType'] = bool(1)
 a['BuiltinFunctionType'] = len
 a['BuiltinMethodType'] = a['BuiltinFunctionType']
 a['BytesType'] = _bytes = codecs.latin_1_encode('\x00')[0] # bytes(1)
 a['ClassType'] = _class
@@ -153,20 +134,16 @@
 a['IntType'] = _int = int(1)
 a['ListType'] = _list = []
 a['NoneType'] = None
 a['ObjectType'] = object()
 a['StringType'] = _str = str(1)
 a['TupleType'] = _tuple = ()
 a['TypeType'] = type
-if PY3:
-    a['LongType'] = _int
-    a['UnicodeType'] = _str
-else:
-    a['LongType'] = long(1)
-    a['UnicodeType'] = unicode(1)
+a['LongType'] = _int
+a['UnicodeType'] = _str
 # built-in constants (CH 4)
 a['CopyrightType'] = copyright
 # built-in types (CH 5)
 a['ClassObjectType'] = _newclass # <type 'type'>
 a['ClassInstanceType'] = _newclass() # <type 'class'>
 a['SetType'] = _set = set()
 a['FrozenSetType'] = frozenset()
@@ -177,90 +154,85 @@
 # data types (CH 8)
 a['ArrayType'] = array.array("f")
 a['DequeType'] = collections.deque([0])
 a['DefaultDictType'] = collections.defaultdict(_function, _dict)
 a['TZInfoType'] = datetime.tzinfo()
 a['DateTimeType'] = datetime.datetime.today()
 a['CalendarType'] = calendar.Calendar()
-if not PY3:
-    a['SetsType'] = sets.Set()
-    a['ImmutableSetType'] = sets.ImmutableSet()
-    a['MutexType'] = mutex.mutex()
 # numeric and mathematical types (CH 9)
 a['DecimalType'] = decimal.Decimal(1)
 a['CountType'] = itertools.count(0)
 # data compression and archiving (CH 12)
 a['TarInfoType'] = tarfile.TarInfo()
 # generic operating system services (CH 15)
-a['LoggerType'] = logging.getLogger()
+a['LoggerType'] = _logger = logging.getLogger()
 a['FormatterType'] = logging.Formatter() # pickle ok
 a['FilterType'] = logging.Filter() # pickle ok
 a['LogRecordType'] = logging.makeLogRecord(_dict) # pickle ok
 a['OptionParserType'] = _oparser = optparse.OptionParser() # pickle ok
 a['OptionGroupType'] = optparse.OptionGroup(_oparser,"foo") # pickle ok
 a['OptionType'] = optparse.Option('--foo') # pickle ok
 if HAS_CTYPES:
-    a['CCharType'] = _cchar = ctypes.c_char()
-    a['CWCharType'] = ctypes.c_wchar() # fail == 2.6
-    a['CByteType'] = ctypes.c_byte()
-    a['CUByteType'] = ctypes.c_ubyte()
-    a['CShortType'] = ctypes.c_short()
-    a['CUShortType'] = ctypes.c_ushort()
-    a['CIntType'] = ctypes.c_int()
-    a['CUIntType'] = ctypes.c_uint()
-    a['CLongType'] = ctypes.c_long()
-    a['CULongType'] = ctypes.c_ulong()
-    a['CLongLongType'] = ctypes.c_longlong()
-    a['CULongLongType'] = ctypes.c_ulonglong()
-    a['CFloatType'] = ctypes.c_float()
-    a['CDoubleType'] = ctypes.c_double()
-    a['CSizeTType'] = ctypes.c_size_t()
+    z = x if IS_PYPY else a
+    z['CCharType'] = _cchar = ctypes.c_char()
+    z['CWCharType'] = ctypes.c_wchar() # fail == 2.6
+    z['CByteType'] = ctypes.c_byte()
+    z['CUByteType'] = ctypes.c_ubyte()
+    z['CShortType'] = ctypes.c_short()
+    z['CUShortType'] = ctypes.c_ushort()
+    z['CIntType'] = ctypes.c_int()
+    z['CUIntType'] = ctypes.c_uint()
+    z['CLongType'] = ctypes.c_long()
+    z['CULongType'] = ctypes.c_ulong()
+    z['CLongLongType'] = ctypes.c_longlong()
+    z['CULongLongType'] = ctypes.c_ulonglong()
+    z['CFloatType'] = ctypes.c_float()
+    z['CDoubleType'] = ctypes.c_double()
+    z['CSizeTType'] = ctypes.c_size_t()
+    del z
     a['CLibraryLoaderType'] = ctypes.cdll
     a['StructureType'] = _Struct
     # if not IS_PYPY:
     #     a['BigEndianStructureType'] = ctypes.BigEndianStructure()
 #NOTE: also LittleEndianStructureType and UnionType... abstract classes
 #NOTE: remember for ctypesobj.contents creates a new python object
 #NOTE: ctypes.c_int._objects is memberdescriptor for object's __dict__
 #NOTE: base class of all ctypes data types is non-public _CData
 
-try: # python 2.6
-    import fractions
-    import number
-    import io
-    from io import StringIO as TextIO
-    # built-in functions (CH 2)
-    a['ByteArrayType'] = bytearray([1])
-    # numeric and mathematical types (CH 9)
-    a['FractionType'] = fractions.Fraction()
-    a['NumberType'] = numbers.Number()
-    # generic operating system services (CH 15)
-    a['IOBaseType'] = io.IOBase()
-    a['RawIOBaseType'] = io.RawIOBase()
-    a['TextIOBaseType'] = io.TextIOBase()
-    a['BufferedIOBaseType'] = io.BufferedIOBase()
-    a['UnicodeIOType'] = TextIO() # the new StringIO
-    a['LoggingAdapterType'] = logging.LoggingAdapter(_logger,_dict) # pickle ok
-    if HAS_CTYPES:
-        a['CBoolType'] = ctypes.c_bool(1)
-        a['CLongDoubleType'] = ctypes.c_longdouble()
-except ImportError:
-    pass
-try: # python 2.7
-    import argparse
-    # data types (CH 8)
-    a['OrderedDictType'] = collections.OrderedDict(_dict)
-    a['CounterType'] = collections.Counter(_dict)
-    if HAS_CTYPES:
-        a['CSSizeTType'] = ctypes.c_ssize_t()
-    # generic operating system services (CH 15)
-    a['NullHandlerType'] = logging.NullHandler() # pickle ok  # new 2.7
-    a['ArgParseFileType'] = argparse.FileType() # pickle ok
-except (AttributeError, ImportError):
-    pass
+import fractions
+import io
+from io import StringIO as TextIO
+# built-in functions (CH 2)
+a['ByteArrayType'] = bytearray([1])
+# numeric and mathematical types (CH 9)
+a['FractionType'] = fractions.Fraction()
+a['NumberType'] = numbers.Number()
+# generic operating system services (CH 15)
+a['IOBaseType'] = io.IOBase()
+a['RawIOBaseType'] = io.RawIOBase()
+a['TextIOBaseType'] = io.TextIOBase()
+a['BufferedIOBaseType'] = io.BufferedIOBase()
+a['UnicodeIOType'] = TextIO() # the new StringIO
+a['LoggerAdapterType'] = logging.LoggerAdapter(_logger,_dict) # pickle ok
+if HAS_CTYPES:
+    z = x if IS_PYPY else a
+    z['CBoolType'] = ctypes.c_bool(1)
+    z['CLongDoubleType'] = ctypes.c_longdouble()
+    del z
+import argparse
+# data types (CH 8)
+a['OrderedDictType'] = collections.OrderedDict(_dict)
+a['CounterType'] = collections.Counter(_dict)
+if HAS_CTYPES:
+    z = x if IS_PYPY else a
+    z['CSSizeTType'] = ctypes.c_ssize_t()
+    del z
+# generic operating system services (CH 15)
+a['NullHandlerType'] = logging.NullHandler() # pickle ok  # new 2.7
+a['ArgParseFileType'] = argparse.FileType() # pickle ok
 
 # -- pickle fails on all below here -----------------------------------------
 # types module (part of CH 8)
 a['CodeType'] = compile('','','exec')
 a['DictProxyType'] = type.__dict__
 a['DictProxyType2'] = _newclass.__dict__
 a['EllipsisType'] = Ellipsis
@@ -271,113 +243,92 @@
 if not IS_PYPY:
     a['MemberDescriptorType2'] = datetime.timedelta.days
 a['MethodType'] = _method = _class()._method #XXX: works when not imported!
 a['ModuleType'] = datetime
 a['NotImplementedType'] = NotImplemented
 a['SliceType'] = slice(1)
 a['UnboundMethodType'] = _class._method #XXX: works when not imported!
-a['TextWrapperType'] = open(os.devnull, 'r') # same as mode='w','w+','r+'
-a['BufferedRandomType'] = open(os.devnull, 'r+b') # same as mode='w+b'
-a['BufferedReaderType'] = open(os.devnull, 'rb') # (default: buffering=-1)
-a['BufferedWriterType'] = open(os.devnull, 'wb')
+d['TextWrapperType'] = open(os.devnull, 'r') # same as mode='w','w+','r+'
+d['BufferedRandomType'] = open(os.devnull, 'r+b') # same as mode='w+b'
+d['BufferedReaderType'] = open(os.devnull, 'rb') # (default: buffering=-1)
+d['BufferedWriterType'] = open(os.devnull, 'wb')
 try: # oddities: deprecated
     from _pyio import open as _open
-    a['PyTextWrapperType'] = _open(os.devnull, 'r', buffering=-1)
-    a['PyBufferedRandomType'] = _open(os.devnull, 'r+b', buffering=-1)
-    a['PyBufferedReaderType'] = _open(os.devnull, 'rb', buffering=-1)
-    a['PyBufferedWriterType'] = _open(os.devnull, 'wb', buffering=-1)
+    d['PyTextWrapperType'] = _open(os.devnull, 'r', buffering=-1)
+    d['PyBufferedRandomType'] = _open(os.devnull, 'r+b', buffering=-1)
+    d['PyBufferedReaderType'] = _open(os.devnull, 'rb', buffering=-1)
+    d['PyBufferedWriterType'] = _open(os.devnull, 'wb', buffering=-1)
 except ImportError:
     pass
 # other (concrete) object types
-if PY3:
-    d['CellType'] = (_lambda)(0).__closure__[0]
-    a['XRangeType'] = _xrange = range(1)
-else:
-    d['CellType'] = (_lambda)(0).func_closure[0]
-    a['XRangeType'] = _xrange = xrange(1)
-if not IS_PYPY:
-    d['MethodDescriptorType'] = type.__dict__['mro']
-    d['WrapperDescriptorType'] = type.__repr__
-    a['WrapperDescriptorType2'] = type.__dict__['__module__']
-    d['ClassMethodDescriptorType'] = type.__dict__['__prepare__' if PY3 else 'mro']
+z = d if sys.hexversion < 0x30800a2 else a
+z['CellType'] = (_lambda)(0).__closure__[0]
+del z
+a['XRangeType'] = _xrange = range(1)
+a['MethodDescriptorType'] = type.__dict__['mro']
+a['WrapperDescriptorType'] = type.__repr__
+#a['WrapperDescriptorType2'] = type.__dict__['__module__']#XXX: GetSetDescriptor
+a['ClassMethodDescriptorType'] = type.__dict__['__prepare__']
 # built-in functions (CH 2)
-if PY3 or IS_PYPY: 
-    _methodwrap = (1).__lt__
-else: 
-    _methodwrap = (1).__cmp__
-d['MethodWrapperType'] = _methodwrap
+_methodwrap = (1).__lt__
+a['MethodWrapperType'] = _methodwrap
 a['StaticMethodType'] = staticmethod(_method)
 a['ClassMethodType'] = classmethod(_method)
 a['PropertyType'] = property()
 d['SuperType'] = super(Exception, _exception)
 # string services (CH 7)
-if PY3: 
-    _in = _bytes
-else: 
-    _in = _str
+_in = _bytes
 a['InputType'] = _cstrI = StringIO(_in)
 a['OutputType'] = _cstrO = StringIO()
 # data types (CH 8)
 a['WeakKeyDictionaryType'] = weakref.WeakKeyDictionary()
 a['WeakValueDictionaryType'] = weakref.WeakValueDictionary()
 a['ReferenceType'] = weakref.ref(_instance)
 a['DeadReferenceType'] = weakref.ref(_class())
 a['ProxyType'] = weakref.proxy(_instance)
 a['DeadProxyType'] = weakref.proxy(_class())
 a['CallableProxyType'] = weakref.proxy(_instance2)
 a['DeadCallableProxyType'] = weakref.proxy(_class2())
 a['QueueType'] = Queue.Queue()
 # numeric and mathematical types (CH 9)
 d['PartialType'] = functools.partial(int,base=2)
-if PY3:
-    a['IzipType'] = zip('0','1')
-else:
-    a['IzipType'] = itertools.izip('0','1')
+a['IzipType'] = zip('0','1')
 a['ChainType'] = itertools.chain('0','1')
 d['ItemGetterType'] = operator.itemgetter(0)
 d['AttrGetterType'] = operator.attrgetter('__repr__')
 # file and directory access (CH 10)
-if PY3: _fileW = _cstrO
-else: _fileW = _tmpf
+_fileW = _cstrO
 # data persistence (CH 11)
 if HAS_ALL:
-    a['ConnectionType'] = _conn = sqlite3.connect(':memory:')
-    a['CursorType'] = _conn.cursor()
+    x['ConnectionType'] = _conn = sqlite3.connect(':memory:')
+    x['CursorType'] = _conn.cursor()
 a['ShelveType'] = shelve.Shelf({})
 # data compression and archiving (CH 12)
 if HAS_ALL:
-    if (hex(sys.hexversion) < '0x2070ef0') or PY3:
-        a['BZ2FileType'] = bz2.BZ2File(os.devnull) #FIXME: fail >= 3.3, 2.7.14
-    a['BZ2CompressorType'] = bz2.BZ2Compressor()
-    a['BZ2DecompressorType'] = bz2.BZ2Decompressor()
-#a['ZipFileType'] = _zip = zipfile.ZipFile(os.devnull,'w') #FIXME: fail >= 3.2
+    x['BZ2FileType'] = bz2.BZ2File(os.devnull)
+    x['BZ2CompressorType'] = bz2.BZ2Compressor()
+    x['BZ2DecompressorType'] = bz2.BZ2Decompressor()
+#x['ZipFileType'] = _zip = zipfile.ZipFile(os.devnull,'w')
 #_zip.write(_tempfile,'x') [causes annoying warning/error printed on import]
 #a['ZipInfoType'] = _zip.getinfo('x')
 a['TarFileType'] = tarfile.open(fileobj=_fileW,mode='w')
 # file formats (CH 13)
-a['DialectType'] = csv.get_dialect('excel')
+x['DialectType'] = csv.get_dialect('excel')
 a['PackerType'] = xdrlib.Packer()
 # optional operating system services (CH 16)
 a['LockType'] = threading.Lock()
 a['RLockType'] = threading.RLock()
 # generic operating system services (CH 15) # also closed/open and r/w/etc...
-a['NamedLoggerType'] = _logger = logging.getLogger(__name__) #FIXME: fail >= 3.2 and <= 2.6
+a['NamedLoggerType'] = _logger = logging.getLogger(__name__)
 #a['FrozenModuleType'] = __hello__ #FIXME: prints "Hello world..."
 # interprocess communication (CH 17)
-if PY3:
-    a['SocketType'] = _socket = socket.socket() #FIXME: fail >= 3.3
-    a['SocketPairType'] = socket.socketpair()[0] #FIXME: fail >= 3.3
-else:
-    a['SocketType'] = _socket = socket.socket()
-    a['SocketPairType'] = _socket._sock
+x['SocketType'] = _socket = socket.socket()
+x['SocketPairType'] = socket.socketpair()[0]
 # python runtime services (CH 27)
-if PY3:
-    a['GeneratorContextManagerType'] = contextlib.contextmanager(max)([1])
-else:
-    a['GeneratorContextManagerType'] = contextlib.GeneratorContextManager(max)
+a['GeneratorContextManagerType'] = contextlib.contextmanager(max)([1])
 
 try: # ipython
     __IPYTHON__ is True # is ipython
 except NameError:
     # built-in constants (CH 4)
     a['QuitterType'] = quit
     d['ExitType'] = a['QuitterType']
@@ -386,109 +337,127 @@
     from numpy import array as _numpy_array
     from numpy import int32 as _numpy_int32
     a['NumpyUfuncType'] = _numpy_ufunc
     a['NumpyArrayType'] = _numpy_array
     a['NumpyInt32Type'] = _numpy_int32
 except ImportError:
     pass
-try: # python 2.6
-    # numeric and mathematical types (CH 9)
-    a['ProductType'] = itertools.product('0','1')
-    # generic operating system services (CH 15)
-    a['FileHandlerType'] = logging.FileHandler(os.devnull) #FIXME: fail >= 3.2 and <= 2.6
-    a['RotatingFileHandlerType'] = logging.handlers.RotatingFileHandler(os.devnull)
-    a['SocketHandlerType'] = logging.handlers.SocketHandler('localhost',514)
-    a['MemoryHandlerType'] = logging.handlers.MemoryHandler(1)
-except AttributeError:
-    pass
-try: # python 2.7
-    # data types (CH 8)
-    a['WeakSetType'] = weakref.WeakSet() # 2.7
-#   # generic operating system services (CH 15) [errors when dill is imported]
-#   a['ArgumentParserType'] = _parser = argparse.ArgumentParser('PROG')
-#   a['NamespaceType'] = _parser.parse_args() # pickle ok
-#   a['SubParsersActionType'] = _parser.add_subparsers()
-#   a['MutuallyExclusiveGroupType'] = _parser.add_mutually_exclusive_group()
-#   a['ArgumentGroupType'] = _parser.add_argument_group()
-except AttributeError:
-    pass
+# numeric and mathematical types (CH 9)
+a['ProductType'] = itertools.product('0','1')
+# generic operating system services (CH 15)
+a['FileHandlerType'] = logging.FileHandler(os.devnull)
+a['RotatingFileHandlerType'] = logging.handlers.RotatingFileHandler(os.devnull)
+a['SocketHandlerType'] = logging.handlers.SocketHandler('localhost',514)
+a['MemoryHandlerType'] = logging.handlers.MemoryHandler(1)
+# data types (CH 8)
+a['WeakSetType'] = weakref.WeakSet() # 2.7
+# generic operating system services (CH 15) [errors when dill is imported]
+#a['ArgumentParserType'] = _parser = argparse.ArgumentParser('PROG')
+#a['NamespaceType'] = _parser.parse_args() # pickle ok
+#a['SubParsersActionType'] = _parser.add_subparsers()
+#a['MutuallyExclusiveGroupType'] = _parser.add_mutually_exclusive_group()
+#a['ArgumentGroupType'] = _parser.add_argument_group()
 
 # -- dill fails in some versions below here ---------------------------------
 # types module (part of CH 8)
-a['FileType'] = open(os.devnull, 'rb', buffering=0) # same 'wb','wb+','rb+'
-# FIXME: FileType fails >= 3.1
+d['FileType'] = open(os.devnull, 'rb', buffering=0) # same 'wb','wb+','rb+'
 # built-in functions (CH 2)
-a['ListIteratorType'] = iter(_list) # empty vs non-empty FIXME: fail < 3.2
-a['TupleIteratorType']= iter(_tuple) # empty vs non-empty FIXME: fail < 3.2
-a['XRangeIteratorType'] = iter(_xrange) # empty vs non-empty FIXME: fail < 3.2
+# Iterators:
+a['ListIteratorType'] = iter(_list) # empty vs non-empty
+a['SetIteratorType'] = iter(_set) #XXX: empty vs non-empty #FIXME: list_iterator
+a['TupleIteratorType']= iter(_tuple) # empty vs non-empty
+a['XRangeIteratorType'] = iter(_xrange) # empty vs non-empty
+a["BytesIteratorType"] = iter(b'')
+a["BytearrayIteratorType"] = iter(bytearray(b''))
+z = x if IS_PYPY else a
+z["CallableIteratorType"] = iter(iter, None)
+del z
+x["MemoryIteratorType"] = iter(memoryview(b''))
+a["ListReverseiteratorType"] = reversed([])
+X = a['OrderedDictType']
+d["OdictKeysType"] = X.keys()
+d["OdictValuesType"] = X.values()
+d["OdictItemsType"] = X.items()
+a["OdictIteratorType"] = iter(X.keys()) #FIXME: list_iterator
+del X
+#FIXME: list_iterator
+a['DictionaryItemIteratorType'] = iter(type.__dict__.items())
+a['DictionaryKeyIteratorType'] = iter(type.__dict__.keys())
+a['DictionaryValueIteratorType'] = iter(type.__dict__.values())
+if sys.hexversion >= 0x30800a0:
+    a["DictReversekeyiteratorType"] = reversed({}.keys())
+    a["DictReversevalueiteratorType"] = reversed({}.values())
+    a["DictReverseitemiteratorType"] = reversed({}.items())
+
+try:
+    import symtable
+    #FIXME: fails to pickle
+    x["SymtableEntryType"] = symtable.symtable("", "string", "exec")._table
+except ImportError:
+    pass
+
+if sys.hexversion >= 0x30a00a0:
+    x['LineIteratorType'] = compile('3', '', 'eval').co_lines()
+
+if sys.hexversion >= 0x30b00b0:
+    from types import GenericAlias
+    d["GenericAliasIteratorType"] = iter(GenericAlias(list, (int,)))
+    x['PositionsIteratorType'] = compile('3', '', 'eval').co_positions()
+
 # data types (CH 8)
-a['PrettyPrinterType'] = pprint.PrettyPrinter() #FIXME: fail >= 3.2 and == 2.5
+a['PrettyPrinterType'] = pprint.PrettyPrinter()
 # numeric and mathematical types (CH 9)
-a['CycleType'] = itertools.cycle('0') #FIXME: fail < 3.2
+a['CycleType'] = itertools.cycle('0')
 # file and directory access (CH 10)
-a['TemporaryFileType'] = _tmpf #FIXME: fail >= 3.2 and == 2.5
+a['TemporaryFileType'] = _tmpf
 # data compression and archiving (CH 12)
-a['GzipFileType'] = gzip.GzipFile(fileobj=_fileW) #FIXME: fail > 3.2 and <= 2.6
+x['GzipFileType'] = gzip.GzipFile(fileobj=_fileW)
 # generic operating system services (CH 15)
-a['StreamHandlerType'] = logging.StreamHandler() #FIXME: fail >= 3.2 and == 2.5
-try: # python 2.6
-    # numeric and mathematical types (CH 9)
-    a['PermutationsType'] = itertools.permutations('0') #FIXME: fail < 3.2
-    a['CombinationsType'] = itertools.combinations('0',1) #FIXME: fail < 3.2
-except AttributeError:
-    pass
-try: # python 2.7
-    # numeric and mathematical types (CH 9)
-    a['RepeatType'] = itertools.repeat(0) #FIXME: fail < 3.2
-    a['CompressType'] = itertools.compress('0',[1]) #FIXME: fail < 3.2
-    #XXX: ...and etc
-except AttributeError:
-    pass
+a['StreamHandlerType'] = logging.StreamHandler()
+# numeric and mathematical types (CH 9)
+a['PermutationsType'] = itertools.permutations('0')
+a['CombinationsType'] = itertools.combinations('0',1)
+a['RepeatType'] = itertools.repeat(0)
+a['CompressType'] = itertools.compress('0',[1])
+#XXX: ...and etc
 
 # -- dill fails on all below here -------------------------------------------
 # types module (part of CH 8)
 x['GeneratorType'] = _generator = _function(1) #XXX: priority
 x['FrameType'] = _generator.gi_frame #XXX: inspect.currentframe()
 x['TracebackType'] = _function2()[1] #(see: inspect.getouterframes,getframeinfo)
 # other (concrete) object types
 # (also: Capsule / CObject ?)
 # built-in functions (CH 2)
-x['SetIteratorType'] = iter(_set) #XXX: empty vs non-empty
 # built-in types (CH 5)
-if PY3:
-    x['DictionaryItemIteratorType'] = iter(type.__dict__.items())
-    x['DictionaryKeyIteratorType'] = iter(type.__dict__.keys())
-    x['DictionaryValueIteratorType'] = iter(type.__dict__.values())
-else:
-    x['DictionaryItemIteratorType'] = type.__dict__.iteritems()
-    x['DictionaryKeyIteratorType'] = type.__dict__.iterkeys()
-    x['DictionaryValueIteratorType'] = type.__dict__.itervalues()
 # string services (CH 7)
 x['StructType'] = struct.Struct('c')
 x['CallableIteratorType'] = _srepattern.finditer('')
 x['SREMatchType'] = _srepattern.match('')
 x['SREScannerType'] = _srepattern.scanner('')
 x['StreamReader'] = codecs.StreamReader(_cstrI) #XXX: ... and etc
 # python object persistence (CH 11)
 # x['DbShelveType'] = shelve.open('foo','n')#,protocol=2) #XXX: delete foo
 if HAS_ALL:
-    x['DbmType'] = dbm.open(_tempfile,'n')
+    z = a if IS_PYPY else x
+    z['DbmType'] = dbm.open(_tempfile,'n')
+    del z
 # x['DbCursorType'] = _dbcursor = anydbm.open('foo','n') #XXX: delete foo
 # x['DbType'] = _dbcursor.db
 # data compression and archiving (CH 12)
 x['ZlibCompressType'] = zlib.compressobj()
 x['ZlibDecompressType'] = zlib.decompressobj()
 # file formats (CH 13)
 x['CSVReaderType'] = csv.reader(_cstrI)
 x['CSVWriterType'] = csv.writer(_cstrO)
 x['CSVDictReaderType'] = csv.DictReader(_cstrI)
 x['CSVDictWriterType'] = csv.DictWriter(_cstrO,{})
 # cryptographic services (CH 14)
 x['HashType'] = hashlib.md5()
-if (hex(sys.hexversion) < '0x30800a1'):
+if (sys.hexversion < 0x30800a1):
     x['HMACType'] = hmac.new(_in)
 else:
     x['HMACType'] = hmac.new(_in, digestmod='md5')
 # generic operating system services (CH 15)
 if HAS_CURSES: pass
     #x['CursesWindowType'] = _curwin = curses.initscr() #FIXME: messes up tty
     #x['CursesTextPadType'] = textpad.Textbox(_curwin)
@@ -508,49 +477,54 @@
     x['CWCharArrayType'] = ctypes.create_unicode_buffer(1)
     x['CParamType'] = ctypes.byref(_cchar)
     x['LPCCharType'] = ctypes.pointer(_cchar)
     x['LPCCharObjType'] = _lpchar = ctypes.POINTER(ctypes.c_char)
     x['NullPtrType'] = _lpchar()
     x['NullPyObjectType'] = ctypes.py_object()
     x['PyObjectType'] = ctypes.py_object(lambda :None)
-    x['FieldType'] = _field = _Struct._field
-    x['CFUNCTYPEType'] = _cfunc = ctypes.CFUNCTYPE(ctypes.c_char)
+    z = a if IS_PYPY else x
+    z['FieldType'] = _field = _Struct._field
+    z['CFUNCTYPEType'] = _cfunc = ctypes.CFUNCTYPE(ctypes.c_char)
     x['CFunctionType'] = _cfunc(str)
-try: # python 2.6
-    # numeric and mathematical types (CH 9)
-    x['MethodCallerType'] = operator.methodcaller('mro') # 2.6
-except AttributeError:
-    pass
-try: # python 2.7
-    # built-in types (CH 5)
-    x['MemoryType'] = memoryview(_in) # 2.7
-    x['MemoryType2'] = memoryview(bytearray(_in)) # 2.7
-    if PY3:
-        x['DictItemsType'] = _dict.items() # 2.7
-        x['DictKeysType'] = _dict.keys() # 2.7
-        x['DictValuesType'] = _dict.values() # 2.7
-    else:
-        x['DictItemsType'] = _dict.viewitems() # 2.7
-        x['DictKeysType'] = _dict.viewkeys() # 2.7
-        x['DictValuesType'] = _dict.viewvalues() # 2.7
-    # generic operating system services (CH 15)
-    x['RawTextHelpFormatterType'] = argparse.RawTextHelpFormatter('PROG')
-    x['RawDescriptionHelpFormatterType'] = argparse.RawDescriptionHelpFormatter('PROG')
-    x['ArgDefaultsHelpFormatterType'] = argparse.ArgumentDefaultsHelpFormatter('PROG')
-except NameError:
-    pass
-try: # python 2.7 (and not 3.1)
-    x['CmpKeyType'] = _cmpkey = functools.cmp_to_key(_methodwrap) # 2.7, >=3.2
-    x['CmpKeyObjType'] = _cmpkey('0') #2.7, >=3.2
-except AttributeError:
-    pass
-if PY3: # oddities: removed, etc
-    x['BufferType'] = x['MemoryType']
-else:
-    x['BufferType'] = buffer('')
+    del z
+# numeric and mathematical types (CH 9)
+a['MethodCallerType'] = operator.methodcaller('mro') # 2.6
+# built-in types (CH 5)
+x['MemoryType'] = memoryview(_in) # 2.7
+x['MemoryType2'] = memoryview(bytearray(_in)) # 2.7
+d['DictItemsType'] = _dict.items() # 2.7
+d['DictKeysType'] = _dict.keys() # 2.7
+d['DictValuesType'] = _dict.values() # 2.7
+# generic operating system services (CH 15)
+a['RawTextHelpFormatterType'] = argparse.RawTextHelpFormatter('PROG')
+a['RawDescriptionHelpFormatterType'] = argparse.RawDescriptionHelpFormatter('PROG')
+a['ArgDefaultsHelpFormatterType'] = argparse.ArgumentDefaultsHelpFormatter('PROG')
+z = a if IS_PYPY else x
+z['CmpKeyType'] = _cmpkey = functools.cmp_to_key(_methodwrap) # 2.7, >=3.2
+z['CmpKeyObjType'] = _cmpkey('0') #2.7, >=3.2
+del z
+# oddities: removed, etc
+x['BufferType'] = x['MemoryType']
+
+from dill._dill import _testcapsule
+if _testcapsule is not None:
+    d['PyCapsuleType'] = _testcapsule
+del _testcapsule
+
+if hasattr(dataclasses, '_HAS_DEFAULT_FACTORY'):
+    a['DataclassesHasDefaultFactoryType'] = dataclasses._HAS_DEFAULT_FACTORY
+
+if hasattr(dataclasses, 'MISSING'):
+    a['DataclassesMissingType'] = dataclasses.MISSING
+
+if hasattr(dataclasses, 'KW_ONLY'):
+    a['DataclassesKWOnlyType'] = dataclasses.KW_ONLY
+
+if hasattr(dataclasses, '_FIELD_BASE'):
+    a['DataclassesFieldBaseType'] = dataclasses._FIELD
 
 # -- cleanup ----------------------------------------------------------------
 a.update(d) # registered also succeed
 if sys.platform[:3] == 'win':
     os.close(_filedescrip) # required on win32
 os.remove(_tempfile)
```

### Comparing `dill-0.3.5.1/dill/_shims.py` & `dill-0.3.6/dill/_shims.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Author: Anirudh Vegesana (avegesan@stanford.edu)
+# Author: Anirudh Vegesana (avegesan@cs.stanford.edu)
 # Copyright (c) 2021-2022 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 """
 Provides shims for compatibility between versions of dill and Python.
 
 Compatibility shims should be provided in this file. Here are two simple example
@@ -45,15 +45,16 @@
 _dill._setattr will be used when present to emulate Python 3.7 functionality in
 older versions of Python while defaulting to the standard setattr in 3.7+.
 
 See this PR for the discussion that lead to this system:
 https://github.com/uqfoundation/dill/pull/443
 """
 
-import inspect, sys
+import inspect
+import sys
 
 _dill = sys.modules['dill._dill']
 
 
 class Reduce(object):
     """
     Reduce objects are wrappers used for compatibility enforcement during
@@ -146,121 +147,47 @@
         else:
             fname = name
         module.__dict__[fname] = func
         func.__module__ = module.__name__
         return func
     return decorator
 
-######################
-## Compatibility Shims are defined below
-######################
-
-_CELL_EMPTY = Getattr(_dill, '_CELL_EMPTY', None)
-
-if _dill.OLD37:
-    if _dill.HAS_CTYPES and hasattr(_dill.ctypes, 'pythonapi') and hasattr(_dill.ctypes.pythonapi, 'PyCell_Set'):
-        # CPython
-        ctypes = _dill.ctypes
-
-        _PyCell_Set = ctypes.pythonapi.PyCell_Set
+def register_shim(name, default):
+    """
+    A easier to understand and more compact way of "softly" defining a function.
+    These two pieces of code are equivalent:
 
-        @move_to(_dill)
-        def _setattr(object, name, value):
-            if type(object) is _dill.CellType and name == 'cell_contents':
-                _PyCell_Set.argtypes = (ctypes.py_object, ctypes.py_object)
-                _PyCell_Set(object, value)
-            else:
-                setattr(object, name, value)
+    if _dill.OLD3X:
+        def _create_class():
+            ...
+    _create_class = register_shim('_create_class', types.new_class)
 
+    if _dill.OLD3X:
         @move_to(_dill)
-        def _delattr(object, name):
-            if type(object) is _dill.CellType and name == 'cell_contents':
-                _PyCell_Set.argtypes = (ctypes.py_object, ctypes.c_void_p)
-                _PyCell_Set(object, None)
-            else:
-                delattr(object, name)
-
-    # General Python (not CPython) up to 3.6 is in a weird case, where it is
-    # possible to pickle recursive cells, but we can't assign directly to the
-    # cell.
-    elif _dill.PY3:
-        # Use nonlocal variables to reassign the cell value.
-        # https://stackoverflow.com/a/59276835
-        __nonlocal = ('nonlocal cell',)
-        exec('''def _setattr(cell, name, value):
-            if type(cell) is _dill.CellType and name == 'cell_contents':
-                def cell_setter(value):
-                    %s
-                    cell = value # pylint: disable=unused-variable
-                func = _dill.FunctionType(cell_setter.__code__, globals(), "", None, (cell,)) # same as cell_setter, but with cell being the cell's contents
-                func(value)
-            else:
-                setattr(cell, name, value)''' % __nonlocal)
-        move_to(_dill)(_setattr)
-
-        exec('''def _delattr(cell, name):
-            if type(cell) is _dill.CellType and name == 'cell_contents':
-                try:
-                    cell.cell_contents
-                except:
-                    return
-                def cell_deleter():
-                    %s
-                    del cell # pylint: disable=unused-variable
-                func = _dill.FunctionType(cell_deleter.__code__, globals(), "", None, (cell,)) # same as cell_deleter, but with cell being the cell's contents
-                func()
-            else:
-                delattr(cell, name)''' % __nonlocal)
-        move_to(_dill)(_delattr)
+        def _create_class():
+            ...
+    _create_class = Getattr(_dill, '_create_class', types.new_class)
+
+    Intuitively, it creates a function or object in the versions of dill/python
+    that require special reimplementations, and use a core library or default
+    implementation if that function or object does not exist.
+    """
+    func = globals().get(name)
+    if func is not None:
+        _dill.__dict__[name] = func
+        func.__module__ = _dill.__name__
 
+    if default is Getattr.NO_DEFAULT:
+        reduction = (getattr, (_dill, name))
     else:
-        # Likely PyPy 2.7. Simulate the nonlocal keyword with bytecode
-        # manipulation.
+        reduction = (getattr, (_dill, name, default))
 
-        # The following function is based on 'cell_set' from 'cloudpickle'
-        # https://github.com/cloudpipe/cloudpickle/blob/5d89947288a18029672596a4d719093cc6d5a412/cloudpickle/cloudpickle.py#L393-L482
-        # Copyright (c) 2012, Regents of the University of California.
-        # Copyright (c) 2009 `PiCloud, Inc. <http://www.picloud.com>`_.
-        # License: https://github.com/cloudpipe/cloudpickle/blob/master/LICENSE
-        @move_to(_dill)
-        def _setattr(cell, name, value):
-            if type(cell) is _dill.CellType and name == 'cell_contents':
-                _cell_set = _dill.FunctionType(
-                      _cell_set_template_code, {}, '_cell_set', (), (cell,),)
-                _cell_set(value)
-            else:
-                setattr(cell, name, value)
-
-        def _cell_set_factory(value):
-            lambda: cell
-            cell = value
-
-        co = _cell_set_factory.__code__
-
-        _cell_set_template_code = _dill.CodeType(
-            co.co_argcount,
-            co.co_nlocals,
-            co.co_stacksize,
-            co.co_flags,
-            co.co_code,
-            co.co_consts,
-            co.co_names,
-            co.co_varnames,
-            co.co_filename,
-            co.co_name,
-            co.co_firstlineno,
-            co.co_lnotab,
-            co.co_cellvars,  # co_freevars is initialized with co_cellvars
-            (),  # co_cellvars is made empty
-        )
+    return Reduce(*reduction, is_callable=callable(default))
 
-        del co
+######################
+## Compatibility Shims are defined below
+######################
 
-        @move_to(_dill)
-        def _delattr(cell, name):
-            if type(cell) is _dill.CellType and name == 'cell_contents':
-                pass
-            else:
-                delattr(cell, name)
+_CELL_EMPTY = register_shim('_CELL_EMPTY', None)
 
-_setattr = Getattr(_dill, '_setattr', setattr)
-_delattr = Getattr(_dill, '_delattr', delattr)
+_setattr = register_shim('_setattr', setattr)
+_delattr = register_shim('_delattr', delattr)
```

### Comparing `dill-0.3.5.1/dill/detect.py` & `dill-0.3.6/dill/detect.py`

 * *Files 7% similar despite different names*

```diff
@@ -7,69 +7,57 @@
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 """
 Methods for detecting objects leading to pickling failures.
 """
 
 import dis
 from inspect import ismethod, isfunction, istraceback, isframe, iscode
-from .pointers import parent, reference, at, parents, children
 
-from ._dill import _trace as trace
-from ._dill import PY3
+from .pointers import parent, reference, at, parents, children
+from .logger import trace
 
 __all__ = ['baditems','badobjects','badtypes','code','errors','freevars',
            'getmodule','globalvars','nestedcode','nestedglobals','outermost',
            'referredglobals','referrednested','trace','varnames']
 
 def getmodule(object, _filename=None, force=False):
     """get the module of the object"""
     from inspect import getmodule as getmod
     module = getmod(object, _filename)
     if module or not force: return module
-    if PY3: builtins = 'builtins'
-    else: builtins = '__builtin__'
-    builtins = __import__(builtins)
+    import builtins
     from .source import getname
     name = getname(object, force=True)
     return builtins if name in vars(builtins).keys() else None
 
 def outermost(func): # is analogous to getsource(func,enclosing=True)
     """get outermost enclosing object (i.e. the outer function in a closure)
 
     NOTE: this is the object-equivalent of getsource(func, enclosing=True)
     """
-    if PY3:
-        if ismethod(func):
-            _globals = func.__func__.__globals__ or {}
-        elif isfunction(func):
-            _globals = func.__globals__ or {}
-        else:
-            return #XXX: or raise? no matches
-        _globals = _globals.items()
+    if ismethod(func):
+        _globals = func.__func__.__globals__ or {}
+    elif isfunction(func):
+        _globals = func.__globals__ or {}
     else:
-        if ismethod(func):
-            _globals = func.im_func.func_globals or {}
-        elif isfunction(func):
-            _globals = func.func_globals or {}
-        else:
-            return #XXX: or raise? no matches
-        _globals = _globals.iteritems()
+        return #XXX: or raise? no matches
+    _globals = _globals.items()
     # get the enclosing source
     from .source import getsourcelines
     try: lines,lnum = getsourcelines(func, enclosing=True)
-    except: #TypeError, IOError
+    except Exception: #TypeError, IOError
         lines,lnum = [],None
     code = ''.join(lines)
     # get all possible names,objects that are named in the enclosing source
     _locals = ((name,obj) for (name,obj) in _globals if name in code)
     # now only save the objects that generate the enclosing block
     for name,obj in _locals: #XXX: don't really need 'name'
         try:
             if getsourcelines(obj) == (lines,lnum): return obj
-        except: #TypeError, IOError
+        except Exception: #TypeError, IOError
             pass
     return #XXX: or raise? no matches
 
 def nestedcode(func, recurse=True): #XXX: or return dict of {co_name: co} ?
     """get the code objects for any nested functions (e.g. in a closure)"""
     func = code(func)
     if not iscode(func): return [] #XXX: or raise? no matches
@@ -79,107 +67,86 @@
         co = code(co)
         if co:
             nested.add(co)
             if recurse: nested |= set(nestedcode(co, recurse=True))
     return list(nested)
 
 def code(func):
-    '''get the code object for the given function or method
+    """get the code object for the given function or method
 
     NOTE: use dill.source.getsource(CODEOBJ) to get the source code
-    '''
-    if PY3:
-        im_func = '__func__'
-        func_code = '__code__'
-    else:
-        im_func = 'im_func'
-        func_code = 'func_code'
-    if ismethod(func): func = getattr(func, im_func)
-    if isfunction(func): func = getattr(func, func_code)
+    """
+    if ismethod(func): func = func.__func__
+    if isfunction(func): func = func.__code__
     if istraceback(func): func = func.tb_frame
     if isframe(func): func = func.f_code
     if iscode(func): return func
     return
 
 #XXX: ugly: parse dis.dis for name after "<code object" in line and in globals?
 def referrednested(func, recurse=True): #XXX: return dict of {__name__: obj} ?
     """get functions defined inside of func (e.g. inner functions in a closure)
 
     NOTE: results may differ if the function has been executed or not.
     If len(nestedcode(func)) > len(referrednested(func)), try calling func().
     If possible, python builds code objects, but delays building functions
     until func() is called.
     """
-    if PY3:
-        att1 = '__code__'
-        att0 = '__func__'
-    else:
-        att1 = 'func_code' # functions
-        att0 = 'im_func'   # methods
-
     import gc
     funcs = set()
     # get the code objects, and try to track down by referrence
     for co in nestedcode(func, recurse):
         # look for function objects that refer to the code object
         for obj in gc.get_referrers(co):
             # get methods
-            _ = getattr(obj, att0, None) # ismethod
-            if getattr(_, att1, None) is co: funcs.add(obj)
+            _ = getattr(obj, '__func__', None) # ismethod
+            if getattr(_, '__code__', None) is co: funcs.add(obj)
             # get functions
-            elif getattr(obj, att1, None) is co: funcs.add(obj)
+            elif getattr(obj, '__code__', None) is co: funcs.add(obj)
             # get frame objects
             elif getattr(obj, 'f_code', None) is co: funcs.add(obj)
             # get code objects
             elif hasattr(obj, 'co_code') and obj is co: funcs.add(obj)
-#     frameobjs => func.func_code.co_varnames not in func.func_code.co_cellvars
-#     funcobjs => func.func_code.co_cellvars not in func.func_code.co_varnames
+#     frameobjs => func.__code__.co_varnames not in func.__code__.co_cellvars
+#     funcobjs => func.__code__.co_cellvars not in func.__code__.co_varnames
 #     frameobjs are not found, however funcobjs are...
 #     (see: test_mixins.quad ... and test_mixins.wtf)
 #     after execution, code objects get compiled, and then may be found by gc
     return list(funcs)
 
 
 def freevars(func):
     """get objects defined in enclosing code that are referred to by func
 
     returns a dict of {name:object}"""
-    if PY3:
-        im_func = '__func__'
-        func_code = '__code__'
-        func_closure = '__closure__'
-    else:
-        im_func = 'im_func'
-        func_code = 'func_code'
-        func_closure = 'func_closure'
-    if ismethod(func): func = getattr(func, im_func)
+    if ismethod(func): func = func.__func__
     if isfunction(func):
-        closures = getattr(func, func_closure) or ()
-        func = getattr(func, func_code).co_freevars # get freevars
+        closures = func.__closure__ or ()
+        func = func.__code__.co_freevars # get freevars
     else:
         return {}
 
     def get_cell_contents():
-        for (name,c) in zip(func,closures):
+        for name, c in zip(func, closures):
             try:
                 cell_contents = c.cell_contents
-            except:
+            except ValueError: # cell is empty
                 continue
-            yield (name,c.cell_contents)
+            yield name, c.cell_contents
 
     return dict(get_cell_contents())
 
 # thanks to Davies Liu for recursion of globals
 def nestedglobals(func, recurse=True):
     """get the names of any globals found within func"""
     func = code(func)
     if func is None: return list()
     import sys
     from .temp import capture
-    CAN_NULL = sys.hexversion >= 51052711 #NULL may be prepended >= 3.11a7
+    CAN_NULL = sys.hexversion >= 0x30b00a7 # NULL may be prepended >= 3.11a7
     names = set()
     with capture('stdout') as out:
         dis.dis(func) #XXX: dis.dis(None) disassembles last traceback
     for line in out.getvalue().splitlines():
         if '_GLOBAL' in line:
             name = line.split('(')[-1].split(')')[0]
             if CAN_NULL:
@@ -195,45 +162,35 @@
     """get the names of objects in the global scope referred to by func"""
     return globalvars(func, recurse, builtin).keys()
 
 def globalvars(func, recurse=True, builtin=False):
     """get objects defined in global scope that are referred to by func
 
     return a dict of {name:object}"""
-    if PY3:
-        im_func = '__func__'
-        func_code = '__code__'
-        func_globals = '__globals__'
-        func_closure = '__closure__'
-    else:
-        im_func = 'im_func'
-        func_code = 'func_code'
-        func_globals = 'func_globals'
-        func_closure = 'func_closure'
-    if ismethod(func): func = getattr(func, im_func)
+    if ismethod(func): func = func.__func__
     if isfunction(func):
         globs = vars(getmodule(sum)).copy() if builtin else {}
         # get references from within closure
         orig_func, func = func, set()
-        for obj in getattr(orig_func, func_closure) or {}:
+        for obj in orig_func.__closure__ or {}:
             try:
                 cell_contents = obj.cell_contents
-            except:
+            except ValueError: # cell is empty
                 pass
             else:
                 _vars = globalvars(cell_contents, recurse, builtin) or {}
                 func.update(_vars) #XXX: (above) be wary of infinte recursion?
                 globs.update(_vars)
         # get globals
-        globs.update(getattr(orig_func, func_globals) or {})
+        globs.update(orig_func.__globals__ or {})
         # get names of references
         if not recurse:
-            func.update(getattr(orig_func, func_code).co_names)
+            func.update(orig_func.__code__.co_names)
         else:
-            func.update(nestedglobals(getattr(orig_func, func_code)))
+            func.update(nestedglobals(orig_func.__code__))
             # find globals for all entries of func
             for key in func.copy(): #XXX: unnecessary...?
                 nested_func = globs.get(key)
                 if nested_func is orig_func:
                    #func.remove(key) if key in func else None
                     continue  #XXX: globalvars(func, False)?
                 func.update(globalvars(nested_func, True, builtin))
@@ -250,15 +207,15 @@
                 if key is orig_func:
                    #func.remove(key) if key in func else None
                     continue  #XXX: globalvars(func, False)?
                 nested_func = globs.get(key)
                 func.update(globalvars(nested_func, True, builtin))
     else:
         return {}
-    #NOTE: if name not in func_globals, then we skip it...
+    #NOTE: if name not in __globals__, then we skip it...
     return dict((name,globs[name]) for name in func if name in globs)
 
 
 def varnames(func):
     """get names of variables defined by func
 
     returns a tuple (local vars, local vars referrenced by nested functions)"""
```

### Comparing `dill-0.3.5.1/dill/objtypes.py` & `dill-0.3.6/dill/objtypes.py`

 * *Files identical despite different names*

### Comparing `dill-0.3.5.1/dill/pointers.py` & `dill-0.3.6/dill/pointers.py`

 * *Files identical despite different names*

### Comparing `dill-0.3.5.1/dill/settings.py` & `dill-0.3.6/dill/settings.py`

 * *Files 26% similar despite different names*

```diff
@@ -5,18 +5,15 @@
 # Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 """
 global settings for Pickler
 """
 
-try:
-    from pickle import DEFAULT_PROTOCOL
-except ImportError:
-    from pickle import HIGHEST_PROTOCOL as DEFAULT_PROTOCOL
+from pickle import DEFAULT_PROTOCOL
 
 settings = {
    #'main' : None,
     'protocol' : DEFAULT_PROTOCOL,
     'byref' : False,
    #'strictio' : False,
     'fmode' : 0, #HANDLE_FMODE
```

### Comparing `dill-0.3.5.1/dill/source.py` & `dill-0.3.6/dill/source.py`

 * *Files 7% similar despite different names*

```diff
@@ -8,15 +8,15 @@
 #
 # inspired by inspect.py from Python-2.7.6
 # inspect.py author: 'Ka-Ping Yee <ping@lfw.org>'
 # inspect.py merged into original dill.source by Mike McKerns 4/13/14
 """
 Extensions to python's 'inspect' module, which can be used
 to retrieve information from live python objects. The methods
-defined in this module are augmented to facilitate access to 
+defined in this module are augmented to facilitate access to
 source code of interactively defined functions and classes,
 as well as provide access to source code for objects defined
 in a file.
 """
 
 __all__ = ['findsource', 'getsourcelines', 'getsource', 'indent', 'outdent', \
            '_wrap', 'dumpsource', 'getname', '_namespace', 'getimport', \
@@ -25,44 +25,44 @@
 import linecache
 import re
 from inspect import (getblock, getfile, getmodule, getsourcefile, indentsize,
                      isbuiltin, isclass, iscode, isframe, isfunction, ismethod,
                      ismodule, istraceback)
 from tokenize import TokenError
 
-from ._dill import PY3
+from ._dill import IS_IPYTHON
 
 
 def isfrommain(obj):
     "check if object was built in __main__"
     module = getmodule(obj)
     if module and module.__name__ == '__main__':
         return True
     return False
 
 
 def isdynamic(obj):
     "check if object was built in the interpreter"
     try: file = getfile(obj)
-    except TypeError: file = None 
+    except TypeError: file = None
     if file == '<stdin>' and isfrommain(obj):
         return True
     return False
 
 
 def _matchlambda(func, line):
     """check if lambda object 'func' matches raw line of code 'line'"""
     from .detect import code as getcode
     from .detect import freevars, globalvars, varnames
     dummy = lambda : '__this_is_a_big_dummy_function__'
     # process the line (removing leading whitespace, etc)
     lhs,rhs = line.split('lambda ',1)[-1].split(":", 1) #FIXME: if !1 inputs
     try: #FIXME: unsafe
         _ = eval("lambda %s : %s" % (lhs,rhs), globals(),locals())
-    except: _ = dummy
+    except Exception: _ = dummy
     # get code objects, for comparison
     _, code = getcode(_).co_code, getcode(func).co_code
     # check if func is in closure
     _f = [line.count(i) for i in freevars(func).keys()]
     if not _f: # not in closure
         # check if code matches
         if _ == code: return True
@@ -76,15 +76,15 @@
     _f = [line.count(i) for i in globalvars(func).keys()]
     if _f and not all(_f): return False  #XXX: VERY WEAK
     # check if func is a double lambda
     if (line.count('lambda ') > 1) and (lhs in freevars(func).keys()):
         _lhs,_rhs = rhs.split('lambda ',1)[-1].split(":",1) #FIXME: if !1 inputs
         try: #FIXME: unsafe
             _f = eval("lambda %s : %s" % (_lhs,_rhs), globals(),locals())
-        except: _f = dummy
+        except Exception: _f = dummy
         # get code objects, for comparison
         _, code = getcode(_f).co_code, getcode(func).co_code
         if len(_) != len(code): return False
         #NOTE: should be same code same order, but except for 't' and '\x88'
         _ = set((i,j) for (i,j) in zip(_,code) if i != j)
         if len(_) != 1: return False #('t','\x88')
         return True
@@ -110,33 +110,55 @@
     or code object.  The source code is returned as a list of all the lines
     in the file and the line number indexes a line in that list.  An IOError
     is raised if the source code cannot be retrieved, while a TypeError is
     raised for objects where the source code is unavailable (e.g. builtins)."""
 
     module = getmodule(object)
     try: file = getfile(module)
-    except TypeError: file = None 
+    except TypeError: file = None
+    is_module_main = (module and module.__name__ == '__main__' and not file)
+    if IS_IPYTHON and is_module_main:
+        #FIXME: quick fix for functions and classes in IPython interpreter
+        try:
+            file = getfile(object)
+            sourcefile = getsourcefile(object)
+        except TypeError:
+            if isclass(object):
+                for object_method in filter(isfunction, object.__dict__.values()):
+                    # look for a method of the class
+                    file_candidate = getfile(object_method)
+                    if not file_candidate.startswith('<ipython-input-'):
+                        continue
+                    file = file_candidate
+                    sourcefile = getsourcefile(object_method)
+                    break
+        if file:
+            lines = linecache.getlines(file)
+        else:
+            # fallback to use history
+            history = '\n'.join(get_ipython().history_manager.input_hist_parsed)
+            lines = [line + '\n' for line in history.splitlines()]
     # use readline when working in interpreter (i.e. __main__ and not file)
-    if module and module.__name__ == '__main__' and not file:
-        try: 
+    elif is_module_main:
+        try:
             import readline
             err = ''
-        except:
+        except ImportError:
             import sys
             err = sys.exc_info()[1].args[0]
             if sys.platform[:3] == 'win':
                 err += ", please install 'pyreadline'"
         if err:
             raise IOError(err)
         lbuf = readline.get_current_history_length()
         lines = [readline.get_history_item(i)+'\n' for i in range(1,lbuf)]
     else:
         try: # special handling for class instances
             if not isclass(object) and isclass(type(object)): # __class__
-                file = getfile(module)        
+                file = getfile(module)
                 sourcefile = getsourcefile(module)
             else: # builtins fail with a TypeError
                 file = getfile(object)
                 sourcefile = getsourcefile(object)
         except (TypeError, AttributeError): # fail with better error
             file = getfile(object)
             sourcefile = getsourcefile(object)
@@ -161,24 +183,22 @@
     name = pat1 = obj = ''
     pat2 = r'^(\s*@)'
 #   pat1b = r'^(\s*%s\W*=)' % name #FIXME: finds 'f = decorate(f)', not exec
     if ismethod(object):
         name = object.__name__
         if name == '<lambda>': pat1 = r'(.*(?<!\w)lambda(:|\s))'
         else: pat1 = r'^(\s*def\s)'
-        if PY3: object = object.__func__
-        else: object = object.im_func
+        object = object.__func__
     if isfunction(object):
         name = object.__name__
         if name == '<lambda>':
             pat1 = r'(.*(?<!\w)lambda(:|\s))'
             obj = object #XXX: better a copy?
         else: pat1 = r'^(\s*def\s)'
-        if PY3: object = object.__code__
-        else: object = object.func_code
+        object = object.__code__
     if istraceback(object):
         object = object.tb_frame
     if isframe(object):
         object = object.f_code
     if iscode(object):
         if not hasattr(object, 'co_firstlineno'):
             raise IOError('could not find function definition')
@@ -451,21 +471,20 @@
         object = getname(object, force=True)
     if object == 'ellipsis': object = 'EllipsisType'
     return True if hasattr(types, object) else False
 
 
 def _isstring(object): #XXX: isstringlike better?
     '''check if object is a string-like type'''
-    if PY3: return isinstance(object, (str, bytes))
-    return isinstance(object, basestring)
+    return isinstance(object, (str, bytes))
 
 
 def indent(code, spaces=4):
     '''indent a block of code with whitespace (default is 4 spaces)'''
-    indent = indentsize(code) 
+    indent = indentsize(code)
     if type(spaces) is int: spaces = ' '*spaces
     # if '\t' is provided, will indent with a tab
     nspaces = indentsize(spaces)
     # blank lines (etc) need to be ignored
     lines = code.split('\n')
 ##  stq = "'''"; dtq = '"""'
 ##  in_stq = in_dtq = False
@@ -487,70 +506,48 @@
 ##      else: pass
     if lines[-1].strip() == '': lines[-1] = ''
     return '\n'.join(lines)
 
 
 def _outdent(lines, spaces=None, all=True):
     '''outdent lines of code, accounting for docs and line continuations'''
-    indent = indentsize(lines[0]) 
+    indent = indentsize(lines[0])
     if spaces is None or spaces > indent or spaces < 0: spaces = indent
     for i in range(len(lines) if all else 1):
         #FIXME: works... but shouldn't outdent 2nd+ lines of multiline doc
         _indent = indentsize(lines[i])
         if spaces > _indent: _spaces = _indent
         else: _spaces = spaces
         lines[i] = lines[i][_spaces:]
     return lines
 
 def outdent(code, spaces=None, all=True):
     '''outdent a block of code (default is to strip all leading whitespace)'''
-    indent = indentsize(code) 
+    indent = indentsize(code)
     if spaces is None or spaces > indent or spaces < 0: spaces = indent
     #XXX: will this delete '\n' in some cases?
     if not all: return code[spaces:]
     return '\n'.join(_outdent(code.split('\n'), spaces=spaces, all=all))
 
 
 #XXX: not sure what the point of _wrap is...
-#exec_ = lambda s, *a: eval(compile(s, '<string>', 'exec'), *a)
 __globals__ = globals()
 __locals__ = locals()
-wrap2 = '''
-def _wrap(f):
-    """ encapsulate a function and it's __import__ """
-    def func(*args, **kwds):
-        try:
-            # _ = eval(getsource(f, force=True)) #XXX: safer but less robust
-            exec getimportable(f, alias='_') in %s, %s
-        except:
-            raise ImportError('cannot import name ' + f.__name__)
-        return _(*args, **kwds)
-    func.__name__ = f.__name__
-    func.__doc__ = f.__doc__
-    return func
-''' % ('__globals__', '__locals__')
-wrap3 = '''
 def _wrap(f):
     """ encapsulate a function and it's __import__ """
     def func(*args, **kwds):
         try:
             # _ = eval(getsource(f, force=True)) #XXX: safer but less robust
-            exec(getimportable(f, alias='_'), %s, %s)
-        except:
+            exec(getimportable(f, alias='_'), __globals__, __locals__)
+        except Exception:
             raise ImportError('cannot import name ' + f.__name__)
         return _(*args, **kwds)
     func.__name__ = f.__name__
     func.__doc__ = f.__doc__
     return func
-''' % ('__globals__', '__locals__')
-if PY3:
-    exec(wrap3)
-else:
-    exec(wrap2)
-del wrap2, wrap3
 
 
 def _enclose(object, alias=''): #FIXME: needs alias to hold returned object
     """create a function enclosure around the source of some object"""
     #XXX: dummy and stub should append a random string
     dummy = '__this_is_a_big_dummy_enclosing_function__'
     stub = '__this_is_a_stub_variable__'
@@ -577,25 +574,22 @@
     if enclose:
         stub = '__this_is_a_stub_variable__' #XXX: *must* be same _enclose.stub
         pre = '%s = ' % stub
         new = False #FIXME: new=True doesn't work with enclose=True
     else:
         stub = alias
         pre = '%s = ' % stub if alias else alias
-    
+
     # if a 'new' instance is not needed, then just dump and load
     if not new or not _isinstance(object):
         code += pre + 'dill.loads(%s)\n' % pik
     else: #XXX: other cases where source code is needed???
         code += getsource(object.__class__, alias='', lstrip=True, force=True)
         mod = repr(object.__module__) # should have a module (no builtins here)
-        if PY3:
-            code += pre + 'dill.loads(%s.replace(b%s,bytes(__name__,"UTF-8")))\n' % (pik,mod)
-        else:
-            code += pre + 'dill.loads(%s.replace(%s,__name__))\n' % (pik,mod)
+        code += pre + 'dill.loads(%s.replace(b%s,bytes(__name__,"UTF-8")))\n' % (pik,mod)
        #code += 'del %s' % object.__class__.__name__ #NOTE: kills any existing!
 
     if enclose:
         # generation of the 'enclosure'
         dummy = '__this_is_a_big_dummy_object__'
         dummy = _enclose(dummy, alias=alias)
         # hack to replace the 'dummy' with the 'real' code
@@ -650,15 +644,15 @@
             return qual
         # get name of a lambda, function, etc
         name = getname(obj) or obj.__name__ # failing, raise AttributeError
         # check special cases (NoneType, ...)
         if module in ['builtins','__builtin__']: # BuiltinFunctionType
             if _intypes(name): return ['types'] + [name]
         return qual + [name] #XXX: can be wrong for some aliased objects
-    except: pass
+    except Exception: pass
     # special case: numpy.inf and numpy.nan (we don't want them as floats)
     if str(obj) in ['inf','nan','Inf','NaN']: # is more, but are they needed?
         return ['numpy'] + [str(obj)]
     # mostly for classes and class instances and such
     module = getattr(obj.__class__, '__module__', None)
     qual = str(obj.__class__)
     try: qual = qual[qual.index("'")+1:-2]
@@ -738,15 +732,15 @@
     qual = _namespace(obj)
     head = '.'.join(qual[:-1])
     tail = qual[-1]
     # for named things... with a nice repr #XXX: move into _namespace?
     try: # look for '<...>' and be mindful it might be in lists, dicts, etc...
         name = repr(obj).split('<',1)[1].split('>',1)[1]
         name = None # we have a 'object'-style repr
-    except: # it's probably something 'importable'
+    except Exception: # it's probably something 'importable'
         if head in ['builtins','__builtin__']:
             name = repr(obj) #XXX: catch [1,2], (1,2), set([1,2])... others?
         else:
             name = repr(obj).split('(')[0]
    #if not repr(obj).startswith('<'): name = repr(obj).split('(')[0]
    #else: name = None
     if name: # try using name instead of tail
@@ -796,35 +790,35 @@
     """
     if source is None:
         source = True if isfrommain(obj) else False
     if source: # first try to get the source
         try:
             return getsource(obj, alias, enclosing=enclosing, \
                              force=force, lstrip=lstrip, builtin=builtin)
-        except: pass
+        except Exception: pass
     try:
         if not _isinstance(obj):
             return getimport(obj, alias, enclosing=enclosing, \
                                   verify=(not force), builtin=builtin)
         # first 'get the import', then 'get the instance'
         _import = getimport(obj, enclosing=enclosing, \
                                  verify=(not force), builtin=builtin)
         name = getname(obj, force=True)
         if not name:
             raise AttributeError("object has no atribute '__name__'")
         _alias = "%s = " % alias if alias else ""
         if alias == name: _alias = ""
         return _import+_alias+"%s\n" % name
 
-    except: pass
+    except Exception: pass
     if not source: # try getsource, only if it hasn't been tried yet
         try:
             return getsource(obj, alias, enclosing=enclosing, \
                              force=force, lstrip=lstrip, builtin=builtin)
-        except: pass
+        except Exception: pass
     # get the name (of functions, lambdas, and classes)
     # or hope that obj can be built from the __repr__
     #XXX: what to do about class instances and such?
     obj = getname(obj, force=force)
     # we either have __repr__ or __name__ (or None)
     if not obj or obj.startswith('<'):
         raise AttributeError("object has no atribute '__name__'")
@@ -855,15 +849,15 @@
             mod = getname(getmodule(encl))
             #HACK: get file containing 'outer' function; is func there?
             lines,_ = findsource(encl)
             candidate = [line for line in lines if getname(encl) in line and \
                          re.match(pat, line)]
             if not candidate:
                 mod = getname(getmodule(fobj))
-                #HACK: get file containing 'inner' function; is func there? 
+                #HACK: get file containing 'inner' function; is func there?
                 lines,_ = findsource(fobj)
                 candidate = [line for line in lines \
                              if getname(fobj) in line and re.match(pat, line)]
             if not len(candidate): raise TypeError('import could not be found')
             candidate = candidate[-1]
             name = candidate.split('=',1)[0].split()[-1].strip()
             src = _getimport(mod, name, alias=alias, builtin=builtin)
@@ -956,15 +950,15 @@
                     return _importable(obj, alias, source=False, builtin=builtin)
                 src = _closuredimport(obj, alias=alias, builtin=builtin)
                 if len(src) == 0:
                     raise NotImplementedError('not implemented')
                 if len(src) > 1:
                     raise NotImplementedError('not implemented')
                 return list(src.values())[0]
-            except:
+            except Exception:
                 if tried_source: raise
                 tried_import = True
         # we want the source
         try:
             src = _closuredsource(obj, alias=alias)
             if len(src) == 0:
                 raise NotImplementedError('not implemented')
@@ -995,15 +989,15 @@
             obj = globalvars(obj) #XXX: don't worry about alias? recurse? etc?
             obj = list(getsource(_obj,name,force=True) for (name,_obj) in obj.items() if not isbuiltin(_obj))
             obj = '\n'.join(obj) if obj else ''
             # combine all referred-to source (global then enclosing)
             if not obj: return src
             if not src: return obj
             return obj + src
-        except:
+        except Exception:
             if tried_import: raise
             tried_source = True
             source = not source
     # should never get here
     return
```

### Comparing `dill-0.3.5.1/dill/temp.py` & `dill-0.3.6/dill/temp.py`

 * *Files 6% similar despite different names*

```diff
@@ -13,33 +13,29 @@
 #XXX: currently, all file-like objects are created by the function...
 
 __all__ = ['dump_source', 'dump', 'dumpIO_source', 'dumpIO',\
            'load_source', 'load', 'loadIO_source', 'loadIO',\
            'capture']
 
 import contextlib
-from ._dill import PY3
 
 
 @contextlib.contextmanager
 def capture(stream='stdout'):
     """builds a context that temporarily replaces the given stream name
 
     >>> with capture('stdout') as out:
     ...   print ("foo!")
     ... 
     >>> print (out.getvalue())
     foo!
 
     """
     import sys
-    if PY3:
-        from io import StringIO
-    else:
-        from StringIO import StringIO
+    from io import StringIO
     orig = getattr(sys, stream)
     setattr(sys, stream, StringIO())
     try:
         yield getattr(sys, stream)
     finally:
         setattr(sys, stream, orig)
 
@@ -106,14 +102,15 @@
     mode.  Else (the default) the file is opened in binary mode.  On
     some operating systems, this makes no difference.
 
 NOTE: Keep the return value for as long as you want your file to exist !
     """ #XXX: write a "load_source"?
     from .source import importable, getname
     import tempfile
+    kwds.setdefault('delete', True)
     kwds.pop('suffix', '') # this is *always* '.py'
     alias = kwds.pop('alias', '') #XXX: include an alias so a name is known
     name = str(alias) or getname(object)
     name = "\n#NAME: %s\n" % name
     #XXX: assumes kwds['dir'] is writable and on $PYTHONPATH
     file = tempfile.NamedTemporaryFile(suffix='.py', **kwds)
     file.write(b(''.join([importable(object, alias=alias),name])))
@@ -157,14 +154,15 @@
     mode.  Else (the default) the file is opened in binary mode.  On
     some operating systems, this makes no difference.
 
 NOTE: Keep the return value for as long as you want your file to exist !
     """
     import dill as pickle
     import tempfile
+    kwds.setdefault('delete', True)
     file = tempfile.NamedTemporaryFile(**kwds)
     pickle.dump(object, file)
     file.flush()
     return file
 
 def loadIO(buffer, **kwds):
     """load an object that was stored with dill.temp.dumpIO
@@ -172,35 +170,29 @@
     buffer: buffer object
 
     >>> dumpfile = dill.temp.dumpIO([1, 2, 3, 4, 5])
     >>> dill.temp.loadIO(dumpfile)
     [1, 2, 3, 4, 5]
     """
     import dill as pickle
-    if PY3:
-        from io import BytesIO as StringIO
-    else:
-        from StringIO import StringIO
+    from io import BytesIO as StringIO
     value = getattr(buffer, 'getvalue', buffer) # value or buffer.getvalue
     if value != buffer: value = value() # buffer.getvalue()
     return pickle.load(StringIO(value))
 
 def dumpIO(object, **kwds):
     """dill.dump of object to a buffer.
 Loads with "dill.temp.loadIO".  Returns the buffer object.
 
     >>> dumpfile = dill.temp.dumpIO([1, 2, 3, 4, 5])
     >>> dill.temp.loadIO(dumpfile)
     [1, 2, 3, 4, 5]
     """
     import dill as pickle
-    if PY3:
-        from io import BytesIO as StringIO
-    else:
-        from StringIO import StringIO
+    from io import BytesIO as StringIO
     file = StringIO()
     pickle.dump(object, file)
     file.flush()
     return file
 
 def loadIO_source(buffer, **kwds):
     """load an object that was stored with dill.temp.dumpIO_source
@@ -213,15 +205,15 @@
     >>> _f = dill.temp.loadIO_source(pyfile)
     >>> _f(4)
     16
     """
     alias = kwds.pop('alias', None)
     source = getattr(buffer, 'getvalue', buffer) # source or buffer.getvalue
     if source != buffer: source = source() # buffer.getvalue()
-    if PY3: source = source.decode() # buffer to string
+    source = source.decode() # buffer to string
     if not alias:
         tag = source.strip().splitlines()[-1].split()
         if tag[0] != '#NAME:':
             stub = source.splitlines()[0]
             raise IOError("unknown name for code: %s" % stub)
         alias = tag[-1]
     local = {}
@@ -239,18 +231,15 @@
     >>> _f(4)
     16
 
 Optional kwds:
     If 'alias' is specified, the object will be renamed to the given string.
     """
     from .source import importable, getname
-    if PY3:
-        from io import BytesIO as StringIO
-    else:
-        from StringIO import StringIO
+    from io import BytesIO as StringIO
     alias = kwds.pop('alias', '') #XXX: include an alias so a name is known
     name = str(alias) or getname(object)
     name = "\n#NAME: %s\n" % name
     #XXX: assumes kwds['dir'] is writable and on $PYTHONPATH
     file = StringIO()
     file.write(b(''.join([importable(object, alias=alias),name])))
     file.flush()
```

### Comparing `dill-0.3.5.1/dill.egg-info/PKG-INFO` & `dill-0.3.6/dill.egg-info/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,40 +1,38 @@
 Metadata-Version: 2.1
 Name: dill
-Version: 0.3.5.1
+Version: 0.3.6
 Summary: serialize all of python
 Home-page: https://github.com/uqfoundation/dill
 Download-URL: https://pypi.org/project/dill/#files
 Author: Mike McKerns
 Author-email: mmckerns@uqfoundation.org
 Maintainer: Mike McKerns
 Maintainer-email: mmckerns@uqfoundation.org
-License: 3-clause BSD
+License: BSD-3-Clause
 Project-URL: Documentation, http://dill.rtfd.io
 Project-URL: Source Code, https://github.com/uqfoundation/dill
 Project-URL: Bug Tracker, https://github.com/uqfoundation/dill/issues
 Platform: Linux
 Platform: Windows
 Platform: Mac
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Developers
 Classifier: Intended Audience :: Science/Research
 Classifier: License :: OSI Approved :: BSD License
-Classifier: Programming Language :: Python :: 2
-Classifier: Programming Language :: Python :: 2.7
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Programming Language :: Python :: Implementation :: PyPy
 Classifier: Topic :: Scientific/Engineering
 Classifier: Topic :: Software Development
-Requires-Python: >=2.7, !=3.0.*, !=3.1.*, !=3.2.*, !=3.3.*, !=3.4.*, !=3.5.*, !=3.6.*
+Requires-Python: >=3.7
 Provides-Extra: readline
 Provides-Extra: graph
 License-File: LICENSE
 
 -----------------------------
 dill: serialize all of python
 -----------------------------
@@ -46,15 +44,15 @@
 python objects to the majority of the built-in python types. Serialization
 is the process of converting an object to a byte stream, and the inverse
 of which is converting a byte stream back to a python object hierarchy.
 
 ``dill`` provides the user the same interface as the ``pickle`` module, and
 also includes some additional features. In addition to pickling python
 objects, ``dill`` provides the ability to save the state of an interpreter
-session in a single command.  Hence, it would be feasable to save an
+session in a single command.  Hence, it would be feasible to save an
 interpreter session, close the interpreter, ship the pickled file to
 another computer, open a new interpreter, unpickle the session and
 thus continue from the 'saved' state of the original interpreter
 session.
 
 ``dill`` can be used to store python objects to a file, but the primary
 usage is to send python objects across the network as a byte stream.
@@ -62,35 +60,36 @@
 and functions to be serialized.  Thus ``dill`` is not intended to be
 secure against erroneously or maliciously constructed data. It is
 left to the user to decide whether the data they unpickle is from
 a trustworthy source.
 
 ``dill`` is part of ``pathos``, a python framework for heterogeneous computing.
 ``dill`` is in active development, so any user feedback, bug reports, comments,
-or suggestions are highly appreciated.  A list of issues is located at https://github.com/uqfoundation/dill/issues, with a legacy list maintained at https://uqfoundation.github.io/project/pathos/query.
+or suggestions are highly appreciated.  A list of issues is located at
+https://github.com/uqfoundation/dill/issues, with a legacy list maintained at
+https://uqfoundation.github.io/project/pathos/query.
 
 
 Major Features
 ==============
 
 ``dill`` can pickle the following standard types:
 
-    - none, type, bool, int, long, float, complex, str, unicode,
+    - none, type, bool, int, float, complex, bytes, str,
     - tuple, list, dict, file, buffer, builtin,
-    - both old and new style classes,
-    - instances of old and new style classes,
+    - python classes, namedtuples, dataclasses, metaclasses,
+    - instances of classes,
     - set, frozenset, array, functions, exceptions
 
 ``dill`` can also pickle more 'exotic' standard types:
 
     - functions with yields, nested functions, lambdas,
     - cell, method, unboundmethod, module, code, methodwrapper,
-    - dictproxy, methoddescriptor, getsetdescriptor, memberdescriptor,
-    - wrapperdescriptor, xrange, slice,
-    - notimplemented, ellipsis, quit
+    - methoddescriptor, getsetdescriptor, memberdescriptor, wrapperdescriptor,
+    - dictproxy, slice, notimplemented, ellipsis, quit
 
 ``dill`` cannot yet pickle these standard types:
 
     - frame, generator, traceback
 
 ``dill`` also provides the capability to:
 
@@ -136,15 +135,15 @@
 
 
 Requirements
 ============
 
 ``dill`` requires:
 
-    - ``python`` (or ``pypy``), **==2.7** or **>=3.7**
+    - ``python`` (or ``pypy``), **>=3.7**
     - ``setuptools``, **>=42**
 
 Optional requirements:
 
     - ``objgraph``, **>=1.7.2**
     - ``pyreadline``, **>=1.7.1** (on windows)
 
@@ -168,15 +167,15 @@
     >>> loads(dumps(squared))(3)
     9
 
 There are a number of options to control serialization which are provided
 as keyword arguments to several ``dill`` functions:
 
 * with *protocol*, the pickle protocol level can be set. This uses the
-  same value as the ``pickle`` module, *HIGHEST_PROTOCOL* or *DEFAULT_PROTOCOL*.
+  same value as the ``pickle`` module, *DEFAULT_PROTOCOL*.
 * with *byref=True*, ``dill`` to behave a lot more like pickle with
   certain objects (like modules) pickled by reference as opposed to
   attempting to pickle the object itself.
 * with *recurse=True*, objects referred to in the global dictionary are
   recursively traced and pickled, instead of the default behavior of
   attempting to store the entire global dictionary.
 * with *fmode*, the contents of the file can be pickled along with the file
@@ -205,34 +204,38 @@
     >>> print(dill.source.getsource(squared))
     squared = lambda x:x**2
 
 To aid in debugging pickling issues, use *dill.detect* which provides
 tools like pickle tracing::
 
     >>> import dill.detect
-    >>> dill.detect.trace(True)
-    >>> f = dumps(squared)
-    F1: <function <lambda> at 0x108899e18>
-    F2: <function _create_function at 0x108db7488>
-    # F2
-    Co: <code object <lambda> at 0x10866a270, file "<stdin>", line 1>
-    F2: <function _create_code at 0x108db7510>
-    # F2
-    # Co
-    D1: <dict object at 0x10862b3f0>
-    # D1
-    D2: <dict object at 0x108e42ee8>
-    # D2
-    # F1
-    >>> dill.detect.trace(False)
+    >>> with dill.detect.trace():
+    >>>     dumps(squared)
+    ┬ F1: <function <lambda> at 0x7fe074f8c280>
+    ├┬ F2: <function _create_function at 0x7fe074c49c10>
+    │└ # F2 [34 B]
+    ├┬ Co: <code object <lambda> at 0x7fe07501eb30, file "<stdin>", line 1>
+    │├┬ F2: <function _create_code at 0x7fe074c49ca0>
+    ││└ # F2 [19 B]
+    │└ # Co [87 B]
+    ├┬ D1: <dict object at 0x7fe0750d4680>
+    │└ # D1 [22 B]
+    ├┬ D2: <dict object at 0x7fe074c5a1c0>
+    │└ # D2 [2 B]
+    ├┬ D2: <dict object at 0x7fe074f903c0>
+    │├┬ D2: <dict object at 0x7fe074f8ebc0>
+    ││└ # D2 [2 B]
+    │└ # D2 [23 B]
+    └ # F1 [180 B]
 
 With trace, we see how ``dill`` stored the lambda (``F1``) by first storing
 ``_create_function``, the underlying code object (``Co``) and ``_create_code``
 (which is used to handle code objects), then we handle the reference to
-the global dict (``D2``).  A ``#`` marks when the object is actually stored.
+the global dict (``D2``) plus other dictionaries (``D1`` and ``D2``) that
+save the lambda object's state. A ``#`` marks when the object is actually stored.
 
 
 More Information
 ================
 
 Probably the best way to get started is to look at the documentation at
 http://dill.rtfd.io. Also see ``dill.tests`` for a set of scripts that
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `dill-0.3.5.1/docs/Makefile` & `dill-0.3.6/docs/Makefile`

 * *Files identical despite different names*

### Comparing `dill-0.3.5.1/docs/source/conf.py` & `dill-0.3.6/docs/source/conf.py`

 * *Files 1% similar despite different names*

```diff
@@ -54,27 +54,28 @@
 # source_suffix = ['.rst', '.md']
 source_suffix = '.rst'
 
 # The master toctree document.
 master_doc = 'index'
 
 # General information about the project.
-project = u'dill'
+project = 'dill'
 year = datetime.now().year
-copyright = u'%d, The Uncertainty Quantification Foundation' % year
-author = u'Mike McKerns'
+copyright = '%d, The Uncertainty Quantification Foundation' % year
+author = 'Mike McKerns'
 
 # extension config
 github_project_url = "https://github.com/uqfoundation/dill"
-autoclass_content= 'both'
+autoclass_content = 'both'
+autodoc_typehints = 'description'
 napoleon_include_init_with_doc = True
 napoleon_include_private_with_doc = False
 napoleon_include_special_with_doc = True
-napoleon_use_param = False
 napoleon_use_ivar = True
+napoleon_use_param = True
 
 # The version info for the project you're documenting, acts as replacement for
 # |version| and |release|, also used in various other places throughout the
 # built documents.
 #
 # The short X.Y version.
 version = dill.__version__
@@ -187,36 +188,36 @@
     # 'figure_align': 'htbp',
 }
 
 # Grouping the document tree into LaTeX files. List of tuples
 # (source start file, target name, title,
 #  author, documentclass [howto, manual, or own class]).
 latex_documents = [
-    (master_doc, 'dill.tex', u'dill Documentation',
-     u'Mike McKerns', 'manual'),
+    (master_doc, 'dill.tex', 'dill Documentation',
+     'Mike McKerns', 'manual'),
 ]
 
 
 # -- Options for manual page output ---------------------------------------
 
 # One entry per manual page. List of tuples
 # (source start file, name, description, authors, manual section).
 man_pages = [
-    (master_doc, 'dill', u'dill Documentation',
+    (master_doc, 'dill', 'dill Documentation',
      [author], 1)
 ]
 
 
 # -- Options for Texinfo output -------------------------------------------
 
 # Grouping the document tree into Texinfo files. List of tuples
 # (source start file, target name, title, author,
 #  dir menu entry, description, category)
 texinfo_documents = [
-    (master_doc, 'dill', u'dill Documentation',
+    (master_doc, 'dill', 'dill Documentation',
      author, 'dill', 'Serialize all of python.',
      'Miscellaneous'),
 ]
```

### Comparing `dill-0.3.5.1/docs/source/dill.rst` & `dill-0.3.6/docs/source/dill.rst`

 * *Files 2% similar despite different names*

```diff
@@ -21,14 +21,26 @@
     :undoc-members:
     :private-members:
     :special-members:
     :show-inheritance:
     :imported-members:
 ..  :exclude-members: ismethod, isfunction, istraceback, isframe, iscode, parent, reference, at, parents, children
 
+logger module
+-------------
+
+.. automodule:: dill.logger
+    :members:
+    :undoc-members:
+    :private-members:
+    :special-members:
+    :show-inheritance:
+    :imported-members:
+..  :exclude-members:
+
 objtypes module
 ---------------
 
 .. automodule:: dill.objtypes
     :members:
     :undoc-members:
     :private-members:
@@ -45,14 +57,26 @@
     :undoc-members:
     :private-members:
     :special-members:
     :show-inheritance:
     :imported-members:
 ..  :exclude-members:
 
+session module
+---------------
+
+.. automodule:: dill.session
+    :members:
+    :undoc-members:
+    :private-members:
+    :special-members:
+    :show-inheritance:
+    :imported-members:
+    :exclude-members: dump_session, load_session
+
 settings module
 ---------------
 
 .. automodule:: dill.settings
     :members:
     :undoc-members:
     :private-members:
```

### Comparing `dill-0.3.5.1/docs/source/pathos.png` & `dill-0.3.6/docs/source/pathos.png`

 * *Files identical despite different names*

### Comparing `dill-0.3.5.1/scripts/get_objgraph` & `dill-0.3.6/scripts/get_objgraph`

 * *Files identical despite different names*

### Comparing `dill-0.3.5.1/scripts/undill` & `dill-0.3.6/scripts/undill`

 * *Files identical despite different names*

### Comparing `dill-0.3.5.1/setup.py` & `dill-0.3.6/setup.py`

 * *Files 17% similar despite different names*

```diff
@@ -5,109 +5,78 @@
 # Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 import os
 import sys
 # drop support for older python
-unsupported = None
-if sys.version_info < (2, 7):
-    unsupported = 'Versions of Python before 2.7 are not supported'
-elif (3, 0) <= sys.version_info < (3, 7):
+if sys.version_info < (3, 7):
     unsupported = 'Versions of Python before 3.7 are not supported'
-if unsupported:
     raise ValueError(unsupported)
 
 # get distribution meta info
 here = os.path.abspath(os.path.dirname(__file__))
-meta_fh = open(os.path.join(here, 'dill/__init__.py'))
-try:
-    meta = {}
-    for line in meta_fh:
-        if line.startswith('__version__'):
-            VERSION = line.split()[-1].strip("'").strip('"')
-            break
-    meta['VERSION'] = VERSION
-    for line in meta_fh:
-        if line.startswith('__author__'):
-            AUTHOR = line.split(' = ')[-1].strip().strip("'").strip('"')
-            break
-    meta['AUTHOR'] = AUTHOR
-    LONG_DOC = ""
-    DOC_STOP = "FAKE_STOP_12345"
-    for line in meta_fh:
-        if LONG_DOC:
-            if line.startswith(DOC_STOP):
-                LONG_DOC = LONG_DOC.strip().strip("'").strip('"').lstrip()
-                break
-            else:
-                LONG_DOC += line
-        elif line.startswith('__doc__'):
-            DOC_STOP = line.split(' = ')[-1]
-            LONG_DOC = "\n"
-    meta['LONG_DOC'] = LONG_DOC
-finally:
-    meta_fh.close()
-
-# get version numbers, long_description, etc
-AUTHOR = meta['AUTHOR']
-VERSION = meta['VERSION']
-LONG_DOC = meta['LONG_DOC'] #FIXME: near-duplicate of README.md
-#LICENSE = meta['LICENSE'] #FIXME: duplicate of LICENSE
-AUTHOR_EMAIL = 'mmckerns@uqfoundation.org'
+sys.path.append(here)
+from version import (__version__, __author__, __contact__ as AUTHOR_EMAIL,
+                     get_license_text, get_readme_as_rst, write_info_file)
+LICENSE = get_license_text(os.path.join(here, 'LICENSE'))
+README = get_readme_as_rst(os.path.join(here, 'README.md'))
+    
+# write meta info file
+write_info_file(here, 'dill', doc=README, license=LICENSE,
+                version=__version__, author=__author__)
+del here, get_license_text, get_readme_as_rst, write_info_file
 
 # check if setuptools is available
 try:
     from setuptools import setup
     from setuptools.dist import Distribution
     has_setuptools = True
 except ImportError:
     from distutils.core import setup
     Distribution = object
     has_setuptools = False
 
 # build the 'setup' call
 setup_kwds = dict(
     name='dill',
-    version=VERSION,
+    version=__version__,
     description='serialize all of python',
-    long_description = LONG_DOC,
-    author = AUTHOR,
+    long_description = README.strip(),
+    author = __author__,
     author_email = AUTHOR_EMAIL,
-    maintainer = AUTHOR,
+    maintainer = __author__,
     maintainer_email = AUTHOR_EMAIL,
-    license = '3-clause BSD',
+    license = 'BSD-3-Clause',
     platforms = ['Linux', 'Windows', 'Mac'],
     url = 'https://github.com/uqfoundation/dill',
     download_url = 'https://pypi.org/project/dill/#files',
     project_urls = {
         'Documentation':'http://dill.rtfd.io',
         'Source Code':'https://github.com/uqfoundation/dill',
         'Bug Tracker':'https://github.com/uqfoundation/dill/issues',
     },
-    python_requires = '>=2.7, !=3.0.*, !=3.1.*, !=3.2.*, !=3.3.*, !=3.4.*, !=3.5.*, !=3.6.*',
+    python_requires = '>=3.7',
     classifiers = [
         'Development Status :: 5 - Production/Stable',
         'Intended Audience :: Developers',
         'Intended Audience :: Science/Research',
         'License :: OSI Approved :: BSD License',
-        'Programming Language :: Python :: 2',
-        'Programming Language :: Python :: 2.7',
         'Programming Language :: Python :: 3',
         'Programming Language :: Python :: 3.7',
         'Programming Language :: Python :: 3.8',
         'Programming Language :: Python :: 3.9',
         'Programming Language :: Python :: 3.10',
         'Programming Language :: Python :: Implementation :: CPython',
         'Programming Language :: Python :: Implementation :: PyPy',
         'Topic :: Scientific/Engineering',
         'Topic :: Software Development',
     ],
     packages = ['dill','dill.tests'],
-    package_dir = {'dill':'dill', 'dill.tests':'tests'},
+    package_dir = {'dill':'dill', 'dill.tests':'dill/tests'},
     scripts=['scripts/undill','scripts/get_objgraph'],
 )
 
 # force python-, abi-, and platform-specific naming of bdist_wheel
 class BinaryDistribution(Distribution):
     """Distribution which forces a binary package with platform name"""
     def has_ext_modules(foo):
```

### Comparing `dill-0.3.5.1/tests/__main__.py` & `dill-0.3.6/dill/tests/__main__.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,30 +1,35 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2018-2022 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
-from __future__ import print_function
 import glob
 import os
+import sys
+import subprocess as sp
+python = sys.executable
 try:
     import pox
-    python = pox.which_python(version=True, fullpath=False) or 'python'
+    python = pox.which_python(version=True) or python
 except ImportError:
-    python = 'python'
-import subprocess as sp
-from sys import platform
-shell = platform[:3] == 'win'
+    pass
+shell = sys.platform[:3] == 'win'
 
 suite = os.path.dirname(__file__) or os.path.curdir
 tests = glob.glob(suite + os.path.sep + 'test_*.py')
 
 
 if __name__ == '__main__':
 
+    failed = 0
     for test in tests:
         p = sp.Popen([python, test], shell=shell).wait()
-        if not p:
-            print('.', end='')
+        if p:
+            print('F', end='', flush=True)
+            failed = 1
+        else:
+            print('.', end='', flush=True)
     print('')
+    exit(failed)
```

### Comparing `dill-0.3.5.1/tests/test_classdef.py` & `dill-0.3.6/dill/tests/test_classdef.py`

 * *Files 12% similar despite different names*

```diff
@@ -86,27 +86,23 @@
 
 # test NoneType
 def test_specialtypes():
     assert dill.pickles(type(None))
     assert dill.pickles(type(NotImplemented))
     assert dill.pickles(type(Ellipsis))
 
-if hex(sys.hexversion) >= '0x20600f0':
-    from collections import namedtuple
-    Z = namedtuple("Z", ['a','b'])
-    Zi = Z(0,1)
-    X = namedtuple("Y", ['a','b'])
-    X.__name__ = "X"
-    if hex(sys.hexversion) >= '0x30300f0':
-        X.__qualname__ = "X" #XXX: name must 'match' or fails to pickle
-    Xi = X(0,1)
-    Bad = namedtuple("FakeName", ['a','b'])
-    Badi = Bad(0,1)
-else:
-    Z = Zi = X = Xi = Bad = Badi = None
+from collections import namedtuple
+Z = namedtuple("Z", ['a','b'])
+Zi = Z(0,1)
+X = namedtuple("Y", ['a','b'])
+X.__name__ = "X"
+X.__qualname__ = "X" #XXX: name must 'match' or fails to pickle
+Xi = X(0,1)
+Bad = namedtuple("FakeName", ['a','b'])
+Badi = Bad(0,1)
 
 # test namedtuple
 def test_namedtuple():
     assert Z is dill.loads(dill.dumps(Z))
     assert Zi == dill.loads(dill.dumps(Zi))
     assert X is dill.loads(dill.dumps(X))
     assert Xi == dill.loads(dill.dumps(Xi))
@@ -119,37 +115,35 @@
             '''docstring'''
         B.__module__ = 'testing'
 
     a = A()
     assert dill.copy(a)
 
     assert dill.copy(A.B).__name__ == 'B'
-    if dill._dill.PY3:
-        assert dill.copy(A.B).__qualname__.endswith('.<locals>.A.B')
+    assert dill.copy(A.B).__qualname__.endswith('.<locals>.A.B')
     assert dill.copy(A.B).__doc__ == 'docstring'
     assert dill.copy(A.B).__module__ == 'testing'
 
 def test_dtype():
     try:
         import numpy as np
 
         dti = np.dtype('int')
-        assert np.dtype == dill.loads(dill.dumps(np.dtype))
-        assert dti == dill.loads(dill.dumps(dti))
+        assert np.dtype == dill.copy(np.dtype)
+        assert dti == dill.copy(dti)
     except ImportError: pass
 
 
 def test_array_nested():
     try:
         import numpy as np
 
         x = np.array([1])
         y = (x,)
-        dill.dumps(x)
-        assert y == dill.loads(dill.dumps(y))
+        assert y == dill.copy(y)
 
     except ImportError: pass
 
 
 def test_array_subclass():
     try:
         import numpy as np
@@ -164,29 +158,29 @@
                     return
                 if isinstance(obj, type(self)):
                     self.color = obj.color
             def __getnewargs__(self):
                 return np.asarray(self), self.color
 
         a1 = TestArray(np.zeros(100), color='green')
-        if dill._dill.PY3 and not dill._dill.IS_PYPY:
+        if not dill._dill.IS_PYPY:
             assert dill.pickles(a1)
             assert a1.__dict__ == dill.copy(a1).__dict__
 
         a2 = a1[0:9]
-        if dill._dill.PY3 and not dill._dill.IS_PYPY:
+        if not dill._dill.IS_PYPY:
             assert dill.pickles(a2)
             assert a2.__dict__ == dill.copy(a2).__dict__
 
         class TestArray2(np.ndarray):
             color = 'blue'
 
         a3 = TestArray2([1,2,3,4,5])
         a3.color = 'green'
-        if dill._dill.PY3 and not dill._dill.IS_PYPY:
+        if not dill._dill.IS_PYPY:
             assert dill.pickles(a3)
             assert a3.__dict__ == dill.copy(a3).__dict__
 
     except ImportError: pass
 
 
 def test_method_decorator():
@@ -199,59 +193,52 @@
 
     res = dill.dumps(a)
     new_obj = dill.loads(res)
     new_obj.__class__.test()
 
 # test slots
 class Y(object):
-  __slots__ = ['y']
+  __slots__ = ('y', '__weakref__')
   def __init__(self, y):
     self.y = y
 
 value = 123
 y = Y(value)
 
 def test_slots():
     assert dill.pickles(Y)
     assert dill.pickles(y)
     assert dill.pickles(Y.y)
     assert dill.copy(y).y == value
 
+def test_attr():
+    import attr
+    @attr.s
+    class A:
+        a = attr.ib()
+
+    v = A(1)
+    assert dill.copy(v) == v
+
 def test_metaclass():
-    if dill._dill.PY3:
-        class metaclass_with_new(type):
-            def __new__(mcls, name, bases, ns, **kwds):
-                cls = super().__new__(mcls, name, bases, ns, **kwds)
-                assert mcls is not None
-                assert cls.method(mcls)
-                return cls
-            def method(cls, mcls):
-                return isinstance(cls, mcls)
-
-        l = locals()
-        exec("""class subclass_with_new(metaclass=metaclass_with_new):
-            def __new__(cls):
-                self = super().__new__(cls)
-                return self""", None, l)
-        subclass_with_new = l['subclass_with_new']
-    else:
-        class metaclass_with_new(type):
-            def __new__(mcls, name, bases, ns, **kwds):
-                cls = super(mcls, metaclass_with_new).__new__(mcls, name, bases, ns, **kwds)
-                assert mcls is not None
-                assert cls.method(mcls)
-                return cls
-            def method(cls, mcls):
-                return isinstance(cls, mcls)
-
-        class subclass_with_new:
-            __metaclass__ = metaclass_with_new
-            def __new__(cls):
-                self = super(subclass_with_new, cls).__new__(cls)
-                return self
+    class metaclass_with_new(type):
+        def __new__(mcls, name, bases, ns, **kwds):
+            cls = super().__new__(mcls, name, bases, ns, **kwds)
+            assert mcls is not None
+            assert cls.method(mcls)
+            return cls
+        def method(cls, mcls):
+            return isinstance(cls, mcls)
+
+    l = locals()
+    exec("""class subclass_with_new(metaclass=metaclass_with_new):
+        def __new__(cls):
+            self = super().__new__(cls)
+            return self""", None, l)
+    subclass_with_new = l['subclass_with_new']
 
     assert dill.copy(subclass_with_new())
 
 
 if __name__ == '__main__':
     test_class_instances()
     test_class_objects()
```

### Comparing `dill-0.3.5.1/tests/test_detect.py` & `dill-0.3.6/dill/tests/test_detect.py`

 * *Files 2% similar despite different names*

```diff
@@ -4,37 +4,37 @@
 # Copyright (c) 2008-2016 California Institute of Technology.
 # Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 from dill.detect import baditems, badobjects, badtypes, errors, parent, at, globalvars
 from dill import settings
-from dill._dill import IS_PYPY, IS_PYPY2
+from dill._dill import IS_PYPY
 from pickle import PicklingError
 
 import inspect
 import sys
 import os
 
 def test_bad_things():
     f = inspect.currentframe()
     assert baditems(f) == [f]
     #assert baditems(globals()) == [f] #XXX
     assert badobjects(f) is f
     assert badtypes(f) == type(f)
-    assert type(errors(f)) is PicklingError if IS_PYPY2 else TypeError
+    assert type(errors(f)) is TypeError
     d = badtypes(f, 1)
     assert isinstance(d, dict)
     assert list(badobjects(f, 1).keys()) == list(d.keys())
     assert list(errors(f, 1).keys()) == list(d.keys())
     s = set([(err.__class__.__name__,err.args[0]) for err in list(errors(f, 1).values())])
     a = dict(s)
     if not os.environ.get('COVERAGE'): #XXX: travis-ci
         assert len(s) is len(a) # TypeError (and possibly PicklingError)
-    n = 1 if IS_PYPY2 else 2
+    n = 2
     assert len(a) is n if 'PicklingError' in a.keys() else n-1
 
 def test_parent():
     x = [4,5,6,7]
     listiter = iter(x)
     obj = parent(listiter, list)
     assert obj is x
```

### Comparing `dill-0.3.5.1/tests/test_dictviews.py` & `dill-0.3.6/dill/tests/test_dictviews.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,17 +1,20 @@
 #!/usr/bin/env python
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
-# Copyright (c) 2008-2016 California Institute of Technology.
-# Copyright (c) 2016-2021 The Uncertainty Quantification Foundation.
+# Author: Anirudh Vegesana (avegesan@cs.stanford.edu)
+# Copyright (c) 2021-2022 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 import dill
-from dill._dill import OLD310, MAPPING_PROXY_TRICK
+from dill._dill import OLD310, MAPPING_PROXY_TRICK, DictProxyType
+
+def test_dictproxy():
+    assert dill.copy(DictProxyType({'a': 2}))
 
 def test_dictviews():
     x = {'a': 1}
     assert dill.copy(x.keys())
     assert dill.copy(x.values())
     assert dill.copy(x.items())
 
@@ -27,9 +30,10 @@
         assert len(seperate_views[0]) == 3 and len(all_views[0]) == 1
         assert len(seperate_views[1]) == 3 and len(all_views[1]) == 1
         assert len(seperate_views[2]) == 3 and len(all_views[2]) == 1
         assert dict(all_views[1]) == x
         assert dict(seperate_views[1]) == new_x
 
 if __name__ == '__main__':
+    test_dictproxy()
     test_dictviews()
     test_dictproxy_trick()
```

### Comparing `dill-0.3.5.1/tests/test_diff.py` & `dill-0.3.6/dill/tests/test_diff.py`

 * *Files 2% similar despite different names*

```diff
@@ -51,26 +51,23 @@
     a3[1] = 1
     assert diff.has_changed(c3)
     changed = diff.whats_changed(c3)
     assert changed[0] == {}
     assert changed[1]
 
     if not IS_PYPY:
-        try:
-            import abc
-            # make sure the "_abc_invaldation_counter" doesn't make test fail
-            diff.memorise(abc.ABCMeta, force=True)
-            assert not diff.has_changed(abc)
-            abc.ABCMeta.zzz = 1
-            assert diff.has_changed(abc)
-            changed = diff.whats_changed(abc)
-            assert list(changed[0].keys()) == ["ABCMeta"]
-            assert not changed[1]
-        except ImportError:
-            pass
+        import abc
+        # make sure the "_abc_invaldation_counter" doesn't make test fail
+        diff.memorise(abc.ABCMeta, force=True)
+        assert not diff.has_changed(abc)
+        abc.ABCMeta.zzz = 1
+        assert diff.has_changed(abc)
+        changed = diff.whats_changed(abc)
+        assert list(changed[0].keys()) == ["ABCMeta"]
+        assert not changed[1]
 
     '''
     import Queue
     diff.memorise(Queue, force=True)
     assert not diff.has_changed(Queue)
     Queue.Queue.zzz = 1
     assert diff.has_changed(Queue)
```

### Comparing `dill-0.3.5.1/tests/test_extendpickle.py` & `dill-0.3.6/dill/tests/test_extendpickle.py`

 * *Files 4% similar despite different names*

```diff
@@ -3,18 +3,15 @@
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2008-2016 California Institute of Technology.
 # Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 import dill as pickle
-try:
-    from StringIO import StringIO
-except ImportError:
-    from io import BytesIO as StringIO
+from io import BytesIO as StringIO
 
 
 def my_fn(x):
     return x * 17
 
 
 def test_extend():
@@ -43,14 +40,14 @@
     assert pickle._dill.is_dill(pickler) is False
 
     try:
         import multiprocess as mp
         pickler = mp.reduction.ForkingPickler(obj_io)
         assert pickle._dill.is_dill(pickler, child=True) is True
         assert pickle._dill.is_dill(pickler, child=False) is False
-    except:
+    except Exception:
         pass
 
 
 if __name__ == '__main__':
     test_extend()
     test_isdill()
```

### Comparing `dill-0.3.5.1/tests/test_fglobals.py` & `dill-0.3.6/dill/tests/test_fglobals.py`

 * *Files identical despite different names*

### Comparing `dill-0.3.5.1/tests/test_file.py` & `dill-0.3.6/dill/tests/test_file.py`

 * *Files 0% similar despite different names*

```diff
@@ -15,16 +15,14 @@
 
 
 dill.settings['recurse'] = True
 
 fname = "_test_file.txt"
 rand_chars = list(string.ascii_letters) + ["\n"] * 40  # bias newline
 
-if sys.hexversion < 0x03030000:
-    FileNotFoundError = IOError
 buffer_error = ValueError("invalid buffer size")
 dne_error = FileNotFoundError("[Errno 2] No such file or directory: '%s'" % fname)
 
 
 def write_randomness(number=200):
     f = open(fname, "w")
     for i in range(number):
```

### Comparing `dill-0.3.5.1/tests/test_functors.py` & `dill-0.3.6/dill/tests/test_functors.py`

 * *Files identical despite different names*

### Comparing `dill-0.3.5.1/tests/test_mixins.py` & `dill-0.3.6/dill/tests/test_mixins.py`

 * *Files identical despite different names*

### Comparing `dill-0.3.5.1/tests/test_module.py` & `dill-0.3.6/dill/tests/test_module.py`

 * *Files 6% similar despite different names*

```diff
@@ -5,16 +5,15 @@
 # Copyright (c) 2016-2022 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 import sys
 import dill
 import test_mixins as module
-try: from importlib import reload
-except ImportError: pass
+from importlib import reload
 dill.settings['recurse'] = True
 
 cached = (module.__cached__ if hasattr(module, "__cached__")
           else module.__file__.split(".", 1)[0] + ".pyc")
 
 module.a = 1234
```

### Comparing `dill-0.3.5.1/tests/test_moduledict.py` & `dill-0.3.6/dill/tests/test_moduledict.py`

 * *Files identical despite different names*

### Comparing `dill-0.3.5.1/tests/test_nested.py` & `dill-0.3.6/dill/tests/test_nested.py`

 * *Files 2% similar despite different names*

```diff
@@ -106,15 +106,15 @@
     p5add = pickle.loads(pinner)
     assert p5add(y) == x+y
 
 
 def test_moduledict_where_not_main():
     try:
         from . import test_moduledict
-    except:
+    except ImportError:
         import test_moduledict
     name = 'test_moduledict.py'
     if os.path.exists(name) and os.path.exists(name+'c'):
         os.remove(name+'c')
 
     if os.path.exists(name) and hasattr(test_moduledict, "__cached__") \
        and os.path.exists(test_moduledict.__cached__):
```

### Comparing `dill-0.3.5.1/tests/test_objects.py` & `dill-0.3.6/dill/tests/test_objects.py`

 * *Files 9% similar despite different names*

```diff
@@ -53,10 +53,11 @@
 
 
 def test_objects():
     for member in objects.keys():
        #pickles(member, exact=True)
         pickles(member, exact=False)
 
-
 if __name__ == '__main__':
+    import warnings
+    warnings.simplefilter('ignore')
     test_objects()
```

### Comparing `dill-0.3.5.1/tests/test_properties.py` & `dill-0.3.6/dill/tests/test_properties.py`

 * *Files identical despite different names*

### Comparing `dill-0.3.5.1/tests/test_recursive.py` & `dill-0.3.6/dill/tests/test_recursive.py`

 * *Files 2% similar despite different names*

```diff
@@ -2,24 +2,23 @@
 #
 # Author: Mike McKerns (mmckerns @caltech and @uqfoundation)
 # Copyright (c) 2019-2022 The Uncertainty Quantification Foundation.
 # License: 3-clause BSD.  The full license text is available at:
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 import dill
-from dill._dill import PY3
 from functools import partial
 import warnings
 
 
 def copy(obj, byref=False, recurse=False):
     if byref:
         try:
             return dill.copy(obj, byref=byref, recurse=recurse)
-        except:
+        except Exception:
             pass
         else:
             raise AssertionError('Copy of %s with byref=True should have given a warning!' % (obj,))
 
         warnings.simplefilter('ignore')
         val = dill.copy(obj, byref=byref, recurse=recurse)
         warnings.simplefilter('error')
@@ -109,17 +108,16 @@
                 self.a = a
         self.b = obj5()
 
 
 def test_circular_reference():
     assert copy(obj4())
     obj4_copy = dill.loads(dill.dumps(obj4()))
-    if PY3:
-        assert type(obj4_copy) is type(obj4_copy).__init__.__closure__[0].cell_contents
-        assert type(obj4_copy.b) is type(obj4_copy.b).__init__.__closure__[0].cell_contents
+    assert type(obj4_copy) is type(obj4_copy).__init__.__closure__[0].cell_contents
+    assert type(obj4_copy.b) is type(obj4_copy.b).__init__.__closure__[0].cell_contents
 
 
 def f():
     def g():
        return g
     return g
 
@@ -142,15 +140,15 @@
     fib3 = copy(fib)
     fib4 = fib
     del fib
     assert fib2(5) == 5
     for _fib in (fib3, fib4):
         try:
             _fib(5)
-        except:
+        except Exception:
             # This is expected to fail because fib no longer exists
             pass
         else:
             raise AssertionError("Function fib shouldn't have been found")
     fib = fib4
```

### Comparing `dill-0.3.5.1/tests/test_restricted.py` & `dill-0.3.6/dill/tests/test_restricted.py`

 * *Files identical despite different names*

### Comparing `dill-0.3.5.1/tests/test_selected.py` & `dill-0.3.6/dill/tests/test_selected.py`

 * *Files 15% similar despite different names*

```diff
@@ -15,37 +15,44 @@
 verbose = False
 
 def test_dict_contents():
   c = type.__dict__
   for i,j in c.items():
    #try:
     ok = dill.pickles(j)
-   #except:
+   #except Exception:
    #  print ("FAIL: %s with %s" % (i, dill.detect.errors(j)))
     if verbose: print ("%s: %s, %s" % (ok, type(j), j))
     assert ok
   if verbose: print ("")
 
 def _g(x): yield x;
 
 def _f():
   try: raise
-  except:
+  except Exception:
     from sys import exc_info
     e, er, tb = exc_info()
     return er, tb
 
 class _d(object):
   def _method(self):
     pass
 
 from dill import objects
 from dill import load_types
 load_types(pickleable=True,unpickleable=False)
 _newclass = objects['ClassObjectType']
+# some clean-up #FIXME: should happen internal to dill
+objects['TemporaryFileType'].close()
+objects['TextWrapperType'].close()
+objects['BufferedRandomType'].close()
+objects['BufferedReaderType'].close()
+objects['BufferedWriterType'].close()
+objects['FileType'].close()
 del objects
 
 # getset_descriptor for new-style classes (fails on '_method', if not __main__)
 def test_class_descriptors():
   d = _d.__dict__
   for i in d.values():
     ok = dill.pickles(i)
@@ -72,28 +79,47 @@
   if verbose: print ("")
 
 # frames, generators, and tracebacks (all depend on frame)
 def test_frame_related():
   g = _g(1)
   f = g.gi_frame
   e,t = _f()
-  _is = lambda ok: not ok if dill._dill.IS_PYPY2 else ok
+  _is = lambda ok: ok
   ok = dill.pickles(f)
   if verbose: print ("%s: %s, %s" % (ok, type(f), f))
   assert not ok
   ok = dill.pickles(g)
   if verbose: print ("%s: %s, %s" % (ok, type(g), g))
   assert _is(not ok) #XXX: dill fails
   ok = dill.pickles(t)
   if verbose: print ("%s: %s, %s" % (ok, type(t), t))
   assert not ok #XXX: dill fails
   ok = dill.pickles(e)
   if verbose: print ("%s: %s, %s" % (ok, type(e), e))
   assert ok
   if verbose: print ("")
 
+def test_typing():
+  import typing
+  x = typing.Any
+  assert x == dill.copy(x)
+  x = typing.Dict[int, str]
+  assert x == dill.copy(x)
+  x = typing.List[int]
+  assert x == dill.copy(x)
+  x = typing.Tuple[int, str]
+  assert x == dill.copy(x)
+  x = typing.Tuple[int]
+  assert x == dill.copy(x)
+  x = typing.Tuple[()]
+  assert x == dill.copy(x)
+  x = typing.Tuple[()].copy_with(())
+  assert x == dill.copy(x)
+  return
+
 
 if __name__ == '__main__':
   test_frame_related()
   test_dict_contents()
   test_class()
   test_class_descriptors()
+  test_typing()
```

### Comparing `dill-0.3.5.1/tests/test_source.py` & `dill-0.3.6/dill/tests/test_source.py`

 * *Files 6% similar despite different names*

```diff
@@ -7,17 +7,15 @@
 #  - https://github.com/uqfoundation/dill/blob/master/LICENSE
 
 from dill.source import getsource, getname, _wrap, likely_import
 from dill.source import getimportable
 from dill._dill import IS_PYPY
 
 import sys
-PY3 = sys.version_info[0] >= 3
-IS_PYPY3 = IS_PYPY and PY3
-PY310b = '0x30a00b1'
+PY310b = 0x30a00b1
 
 f = lambda x: x**2
 def g(x): return f(x) - x
 
 def h(x):
   def g(x): return x
   return g(x) - x
@@ -57,22 +55,20 @@
 
 # test itself
 def test_itself():
   assert likely_import(likely_import)=='from dill.source import likely_import\n'
 
 # builtin functions and objects
 def test_builtin():
-  if PY3: builtin = 'builtins'
-  else: builtin = '__builtin__'
   assert likely_import(pow) == 'pow\n'
   assert likely_import(100) == '100\n'
   assert likely_import(True) == 'True\n'
-  assert likely_import(pow, explicit=True) == 'from %s import pow\n' % builtin
+  assert likely_import(pow, explicit=True) == 'from builtins import pow\n'
   assert likely_import(100, explicit=True) == '100\n'
-  assert likely_import(True, explicit=True) == 'True\n' if PY3 else 'from %s import True\n' % builtin
+  assert likely_import(True, explicit=True) == 'True\n'
   # this is kinda BS... you can't import a None
   assert likely_import(None) == 'None\n'
   assert likely_import(None, explicit=True) == 'None\n'
 
 
 # other imported functions
 def test_imported():
@@ -83,22 +79,17 @@
 def test_dynamic():
   assert likely_import(add) == 'from %s import add\n' % __name__
   # interactive lambdas
   assert likely_import(squared) == 'from %s import squared\n' % __name__
 
 # classes and class instances
 def test_classes():
-  try: #XXX: should this be a 'special case'?
-    from StringIO import StringIO
-    y = "from StringIO import StringIO\n"
-    x = y
-  except ImportError:
-    from io import BytesIO as StringIO
-    y = "from _io import BytesIO\n"
-    x = y if (IS_PYPY3 or hex(sys.hexversion) >= PY310b) else "from io import BytesIO\n"
+  from io import BytesIO as StringIO
+  y = "from _io import BytesIO\n"
+  x = y if (IS_PYPY or sys.hexversion >= PY310b) else "from io import BytesIO\n"
   s = StringIO()
 
   assert likely_import(StringIO) == x
   assert likely_import(s) == y
   # interactively defined classes and class instances
   assert likely_import(Foo) == 'from %s import Foo\n' % __name__
   assert likely_import(_foo) == 'from %s import Foo\n' % __name__
```

### Comparing `dill-0.3.5.1/tests/test_temp.py` & `dill-0.3.6/dill/tests/test_temp.py`

 * *Files identical despite different names*

