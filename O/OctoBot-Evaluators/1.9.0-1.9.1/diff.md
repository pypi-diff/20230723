# Comparing `tmp/OctoBot-Evaluators-1.9.0.tar.gz` & `tmp/OctoBot-Evaluators-1.9.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "OctoBot-Evaluators-1.9.0.tar", last modified: Tue May  2 20:32:12 2023, max compression
+gzip compressed data, was "OctoBot-Evaluators-1.9.1.tar", last modified: Sun Jul 23 13:51:47 2023, max compression
```

## Comparing `OctoBot-Evaluators-1.9.0.tar` & `OctoBot-Evaluators-1.9.1.tar`

### file list

```diff
@@ -1,72 +1,72 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 20:32:12.442050 OctoBot-Evaluators-1.9.0/
--rw-r--r--   0 runner    (1001) docker     (123)     7528 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/CHANGELOG.md
--rw-r--r--   0 runner    (1001) docker     (123)     7652 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      144 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/MANIFEST.in
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 20:32:12.438050 OctoBot-Evaluators-1.9.0/OctoBot_Evaluators.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2515 2023-05-02 20:32:12.000000 OctoBot-Evaluators-1.9.0/OctoBot_Evaluators.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2065 2023-05-02 20:32:12.000000 OctoBot-Evaluators-1.9.0/OctoBot_Evaluators.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-02 20:32:12.000000 OctoBot-Evaluators-1.9.0/OctoBot_Evaluators.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-02 20:32:12.000000 OctoBot-Evaluators-1.9.0/OctoBot_Evaluators.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)      124 2023-05-02 20:32:12.000000 OctoBot-Evaluators-1.9.0/OctoBot_Evaluators.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       25 2023-05-02 20:32:12.000000 OctoBot-Evaluators-1.9.0/OctoBot_Evaluators.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)     2515 2023-05-02 20:32:12.442050 OctoBot-Evaluators-1.9.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1872 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 20:32:12.438050 OctoBot-Evaluators-1.9.0/octobot_evaluators/
--rw-r--r--   0 runner    (1001) docker     (123)      798 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/octobot_evaluators/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 20:32:12.438050 OctoBot-Evaluators-1.9.0/octobot_evaluators/api/
--rw-r--r--   0 runner    (1001) docker     (123)     3065 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/octobot_evaluators/api/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5178 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/octobot_evaluators/api/evaluators.py
--rw-r--r--   0 runner    (1001) docker     (123)     4707 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/octobot_evaluators/api/initialization.py
--rw-r--r--   0 runner    (1001) docker     (123)     2291 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/octobot_evaluators/api/inspection.py
--rw-r--r--   0 runner    (1001) docker     (123)     1462 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/octobot_evaluators/api/matrix.py
--rw-r--r--   0 runner    (1001) docker     (123)     1591 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/octobot_evaluators/constants.py
--rw-r--r--   0 runner    (1001) docker     (123)      893 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/octobot_evaluators/enums.py
--rw-r--r--   0 runner    (1001) docker     (123)      827 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/octobot_evaluators/errors.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 20:32:12.438050 OctoBot-Evaluators-1.9.0/octobot_evaluators/evaluators/
--rw-r--r--   0 runner    (1001) docker     (123)     7470 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/octobot_evaluators/evaluators/TA_evaluator.py
--rw-r--r--   0 runner    (1001) docker     (123)     3291 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/octobot_evaluators/evaluators/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    23071 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/octobot_evaluators/evaluators/abstract_evaluator.py
--rw-r--r--   0 runner    (1001) docker     (123)      857 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/octobot_evaluators/evaluators/abstract_util.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 20:32:12.438050 OctoBot-Evaluators-1.9.0/octobot_evaluators/evaluators/channel/
--rw-r--r--   0 runner    (1001) docker     (123)     1875 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/octobot_evaluators/evaluators/channel/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5858 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/octobot_evaluators/evaluators/channel/evaluator_channel.py
--rw-r--r--   0 runner    (1001) docker     (123)     7214 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/octobot_evaluators/evaluators/channel/evaluators.py
--rw-r--r--   0 runner    (1001) docker     (123)    11820 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/octobot_evaluators/evaluators/evaluator_factory.py
--rw-r--r--   0 runner    (1001) docker     (123)     2992 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/octobot_evaluators/evaluators/realtime_evaluator.py
--rw-r--r--   0 runner    (1001) docker     (123)    17323 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/octobot_evaluators/evaluators/scripted_evaluator.py
--rw-r--r--   0 runner    (1001) docker     (123)     3874 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/octobot_evaluators/evaluators/social_evaluator.py
--rw-r--r--   0 runner    (1001) docker     (123)    26780 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/octobot_evaluators/evaluators/strategy_evaluator.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 20:32:12.438050 OctoBot-Evaluators-1.9.0/octobot_evaluators/matrix/
--rw-r--r--   0 runner    (1001) docker     (123)     2457 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/octobot_evaluators/matrix/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 20:32:12.442050 OctoBot-Evaluators-1.9.0/octobot_evaluators/matrix/channel/
--rw-r--r--   0 runner    (1001) docker     (123)     1074 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/octobot_evaluators/matrix/channel/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     9731 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/octobot_evaluators/matrix/channel/matrix.py
--rw-r--r--   0 runner    (1001) docker     (123)     1470 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/octobot_evaluators/matrix/matrices.py
--rw-r--r--   0 runner    (1001) docker     (123)     3328 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/octobot_evaluators/matrix/matrix.py
--rw-r--r--   0 runner    (1001) docker     (123)    15662 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/octobot_evaluators/matrix/matrix_manager.py
--rw-r--r--   0 runner    (1001) docker     (123)     3461 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/octobot_evaluators/octobot_channel_consumer.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 20:32:12.442050 OctoBot-Evaluators-1.9.0/octobot_evaluators/util/
--rw-r--r--   0 runner    (1001) docker     (123)     1117 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/octobot_evaluators/util/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4464 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/octobot_evaluators/util/evaluation_util.py
--rw-r--r--   0 runner    (1001) docker     (123)      181 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-02 20:32:12.442050 OctoBot-Evaluators-1.9.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1998 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 20:32:12.434050 OctoBot-Evaluators-1.9.0/tests/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 20:32:12.442050 OctoBot-Evaluators-1.9.0/tests/evaluators/
--rw-r--r--   0 runner    (1001) docker     (123)      719 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/tests/evaluators/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 20:32:12.442050 OctoBot-Evaluators-1.9.0/tests/evaluators/channel/
--rw-r--r--   0 runner    (1001) docker     (123)      719 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/tests/evaluators/channel/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2662 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/tests/evaluators/channel/test_evaluator_channel.py
--rw-r--r--   0 runner    (1001) docker     (123)    13392 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/tests/evaluators/test_evaluator_factory.py
--rw-r--r--   0 runner    (1001) docker     (123)    12284 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/tests/evaluators/test_evaluator_factory_create_evaluators.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 20:32:12.442050 OctoBot-Evaluators-1.9.0/tests/matrix/
--rw-r--r--   0 runner    (1001) docker     (123)      719 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/tests/matrix/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 20:32:12.442050 OctoBot-Evaluators-1.9.0/tests/matrix/channel/
--rw-r--r--   0 runner    (1001) docker     (123)      719 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/tests/matrix/channel/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3996 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/tests/matrix/channel/test_matrix.py
--rw-r--r--   0 runner    (1001) docker     (123)     1988 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/tests/matrix/test_matrices.py
--rw-r--r--   0 runner    (1001) docker     (123)     3586 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/tests/matrix/test_matrix.py
--rw-r--r--   0 runner    (1001) docker     (123)    41061 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/tests/matrix/test_matrix_manager.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-02 20:32:12.442050 OctoBot-Evaluators-1.9.0/tests/util/
--rw-r--r--   0 runner    (1001) docker     (123)      719 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/tests/util/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2090 2023-05-02 20:31:12.000000 OctoBot-Evaluators-1.9.0/tests/util/test_evaluation_util.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:51:47.088663 OctoBot-Evaluators-1.9.1/
+-rw-r--r--   0 runner    (1001) docker     (123)     7618 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/CHANGELOG.md
+-rw-r--r--   0 runner    (1001) docker     (123)     7652 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      144 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/MANIFEST.in
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:51:47.084663 OctoBot-Evaluators-1.9.1/OctoBot_Evaluators.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2515 2023-07-23 13:51:47.000000 OctoBot-Evaluators-1.9.1/OctoBot_Evaluators.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2065 2023-07-23 13:51:47.000000 OctoBot-Evaluators-1.9.1/OctoBot_Evaluators.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 13:51:47.000000 OctoBot-Evaluators-1.9.1/OctoBot_Evaluators.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 13:51:47.000000 OctoBot-Evaluators-1.9.1/OctoBot_Evaluators.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)      124 2023-07-23 13:51:47.000000 OctoBot-Evaluators-1.9.1/OctoBot_Evaluators.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       25 2023-07-23 13:51:47.000000 OctoBot-Evaluators-1.9.1/OctoBot_Evaluators.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     2515 2023-07-23 13:51:47.088663 OctoBot-Evaluators-1.9.1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1872 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:51:47.084663 OctoBot-Evaluators-1.9.1/octobot_evaluators/
+-rw-r--r--   0 runner    (1001) docker     (123)      798 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/octobot_evaluators/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:51:47.084663 OctoBot-Evaluators-1.9.1/octobot_evaluators/api/
+-rw-r--r--   0 runner    (1001) docker     (123)     3065 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/octobot_evaluators/api/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4651 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/octobot_evaluators/api/evaluators.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5007 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/octobot_evaluators/api/initialization.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2291 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/octobot_evaluators/api/inspection.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1462 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/octobot_evaluators/api/matrix.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1591 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/octobot_evaluators/constants.py
+-rw-r--r--   0 runner    (1001) docker     (123)      893 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/octobot_evaluators/enums.py
+-rw-r--r--   0 runner    (1001) docker     (123)      827 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/octobot_evaluators/errors.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:51:47.084663 OctoBot-Evaluators-1.9.1/octobot_evaluators/evaluators/
+-rw-r--r--   0 runner    (1001) docker     (123)     7470 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/octobot_evaluators/evaluators/TA_evaluator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3291 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/octobot_evaluators/evaluators/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    23203 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/octobot_evaluators/evaluators/abstract_evaluator.py
+-rw-r--r--   0 runner    (1001) docker     (123)      857 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/octobot_evaluators/evaluators/abstract_util.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:51:47.088663 OctoBot-Evaluators-1.9.1/octobot_evaluators/evaluators/channel/
+-rw-r--r--   0 runner    (1001) docker     (123)     1875 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/octobot_evaluators/evaluators/channel/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5858 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/octobot_evaluators/evaluators/channel/evaluator_channel.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7214 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/octobot_evaluators/evaluators/channel/evaluators.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10943 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/octobot_evaluators/evaluators/evaluator_factory.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2992 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/octobot_evaluators/evaluators/realtime_evaluator.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17323 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/octobot_evaluators/evaluators/scripted_evaluator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3874 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/octobot_evaluators/evaluators/social_evaluator.py
+-rw-r--r--   0 runner    (1001) docker     (123)    26854 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/octobot_evaluators/evaluators/strategy_evaluator.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:51:47.088663 OctoBot-Evaluators-1.9.1/octobot_evaluators/matrix/
+-rw-r--r--   0 runner    (1001) docker     (123)     2457 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/octobot_evaluators/matrix/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:51:47.088663 OctoBot-Evaluators-1.9.1/octobot_evaluators/matrix/channel/
+-rw-r--r--   0 runner    (1001) docker     (123)     1074 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/octobot_evaluators/matrix/channel/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9731 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/octobot_evaluators/matrix/channel/matrix.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1470 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/octobot_evaluators/matrix/matrices.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3328 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/octobot_evaluators/matrix/matrix.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15662 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/octobot_evaluators/matrix/matrix_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3461 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/octobot_evaluators/octobot_channel_consumer.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:51:47.088663 OctoBot-Evaluators-1.9.1/octobot_evaluators/util/
+-rw-r--r--   0 runner    (1001) docker     (123)     1117 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/octobot_evaluators/util/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4464 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/octobot_evaluators/util/evaluation_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)      181 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 13:51:47.088663 OctoBot-Evaluators-1.9.1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1998 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:51:47.084663 OctoBot-Evaluators-1.9.1/tests/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:51:47.088663 OctoBot-Evaluators-1.9.1/tests/evaluators/
+-rw-r--r--   0 runner    (1001) docker     (123)      719 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/tests/evaluators/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:51:47.088663 OctoBot-Evaluators-1.9.1/tests/evaluators/channel/
+-rw-r--r--   0 runner    (1001) docker     (123)      719 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/tests/evaluators/channel/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2662 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/tests/evaluators/channel/test_evaluator_channel.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13392 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/tests/evaluators/test_evaluator_factory.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12456 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/tests/evaluators/test_evaluator_factory_create_evaluators.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:51:47.088663 OctoBot-Evaluators-1.9.1/tests/matrix/
+-rw-r--r--   0 runner    (1001) docker     (123)      719 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/tests/matrix/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:51:47.088663 OctoBot-Evaluators-1.9.1/tests/matrix/channel/
+-rw-r--r--   0 runner    (1001) docker     (123)      719 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/tests/matrix/channel/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3996 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/tests/matrix/channel/test_matrix.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1988 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/tests/matrix/test_matrices.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3586 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/tests/matrix/test_matrix.py
+-rw-r--r--   0 runner    (1001) docker     (123)    41061 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/tests/matrix/test_matrix_manager.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:51:47.088663 OctoBot-Evaluators-1.9.1/tests/util/
+-rw-r--r--   0 runner    (1001) docker     (123)      719 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/tests/util/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2090 2023-07-23 13:51:02.000000 OctoBot-Evaluators-1.9.1/tests/util/test_evaluation_util.py
```

### Comparing `OctoBot-Evaluators-1.9.0/CHANGELOG.md` & `OctoBot-Evaluators-1.9.1/CHANGELOG.md`

 * *Files 2% similar despite different names*

```diff
@@ -1,13 +1,17 @@
 # Changelog
 All notable changes to this project will be documented in this file.
 
 The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
 and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).
 
+## [1.9.1] - 2023-07-23
+### Updated
+- [Evaluators] add startup config optional arguments
+
 ## [1.9.0] - 2023-05-02
 ### Updated
 - Supported python versions
 ### Removed
 - Cython
 
 ## [1.8.7] - 2023-04-03
```

### Comparing `OctoBot-Evaluators-1.9.0/LICENSE` & `OctoBot-Evaluators-1.9.1/LICENSE`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/OctoBot_Evaluators.egg-info/PKG-INFO` & `OctoBot-Evaluators-1.9.1/OctoBot_Evaluators.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: OctoBot-Evaluators
-Version: 1.9.0
+Version: 1.9.1
 Summary: OctoBot project evaluators package
 Home-page: https://github.com/Drakkar-Software/OctoBot-Evaluators
 Author: Drakkar-Software
 Author-email: contact@drakkar.software
 License: LGPL-3.0
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Operating System :: OS Independent
@@ -12,15 +12,15 @@
 Classifier: Operating System :: Microsoft :: Windows
 Classifier: Operating System :: POSIX
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Requires-Python: >=3.8
 License-File: LICENSE
 
-# OctoBot-Evaluators [1.9.0](https://github.com/Drakkar-Software/OctoBot-Evaluators/blob/master/CHANGELOG.md)
+# OctoBot-Evaluators [1.9.1](https://github.com/Drakkar-Software/OctoBot-Evaluators/blob/master/CHANGELOG.md)
 [![Codacy Badge](https://api.codacy.com/project/badge/Grade/a0c08eab5d4c440aa6e3fc3061ad0520)](https://app.codacy.com/gh/Drakkar-Software/OctoBot-Evaluators?utm_source=github.com&utm_medium=referral&utm_content=Drakkar-Software/OctoBot-Evaluators&utm_campaign=Badge_Grade_Dashboard)
 [![PyPI](https://img.shields.io/pypi/v/OctoBot-Evaluators.svg)](https://pypi.python.org/pypi/OctoBot-Evaluators/)
 [![Coverage Status](https://coveralls.io/repos/github/Drakkar-Software/OctoBot-Evaluators/badge.svg)](https://coveralls.io/github/Drakkar-Software/OctoBot-Evaluators)
 [![Github-Action-CI](https://github.com/Drakkar-Software/OctoBot-Evaluators/workflows/OctoBot-Evaluators-CI/badge.svg)](https://github.com/Drakkar-Software/OctoBot-Evaluators/actions)
 [![Build Status](https://cloud.drone.io/api/badges/Drakkar-Software/OctoBot-Evaluators/status.svg)](https://cloud.drone.io/Drakkar-Software/OctoBot-Evaluators)
 
 # Where are evaluators and strategies ?
```

### Comparing `OctoBot-Evaluators-1.9.0/OctoBot_Evaluators.egg-info/SOURCES.txt` & `OctoBot-Evaluators-1.9.1/OctoBot_Evaluators.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/PKG-INFO` & `OctoBot-Evaluators-1.9.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: OctoBot-Evaluators
-Version: 1.9.0
+Version: 1.9.1
 Summary: OctoBot project evaluators package
 Home-page: https://github.com/Drakkar-Software/OctoBot-Evaluators
 Author: Drakkar-Software
 Author-email: contact@drakkar.software
 License: LGPL-3.0
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Operating System :: OS Independent
@@ -12,15 +12,15 @@
 Classifier: Operating System :: Microsoft :: Windows
 Classifier: Operating System :: POSIX
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Requires-Python: >=3.8
 License-File: LICENSE
 
-# OctoBot-Evaluators [1.9.0](https://github.com/Drakkar-Software/OctoBot-Evaluators/blob/master/CHANGELOG.md)
+# OctoBot-Evaluators [1.9.1](https://github.com/Drakkar-Software/OctoBot-Evaluators/blob/master/CHANGELOG.md)
 [![Codacy Badge](https://api.codacy.com/project/badge/Grade/a0c08eab5d4c440aa6e3fc3061ad0520)](https://app.codacy.com/gh/Drakkar-Software/OctoBot-Evaluators?utm_source=github.com&utm_medium=referral&utm_content=Drakkar-Software/OctoBot-Evaluators&utm_campaign=Badge_Grade_Dashboard)
 [![PyPI](https://img.shields.io/pypi/v/OctoBot-Evaluators.svg)](https://pypi.python.org/pypi/OctoBot-Evaluators/)
 [![Coverage Status](https://coveralls.io/repos/github/Drakkar-Software/OctoBot-Evaluators/badge.svg)](https://coveralls.io/github/Drakkar-Software/OctoBot-Evaluators)
 [![Github-Action-CI](https://github.com/Drakkar-Software/OctoBot-Evaluators/workflows/OctoBot-Evaluators-CI/badge.svg)](https://github.com/Drakkar-Software/OctoBot-Evaluators/actions)
 [![Build Status](https://cloud.drone.io/api/badges/Drakkar-Software/OctoBot-Evaluators/status.svg)](https://cloud.drone.io/Drakkar-Software/OctoBot-Evaluators)
 
 # Where are evaluators and strategies ?
```

### Comparing `OctoBot-Evaluators-1.9.0/README.md` & `OctoBot-Evaluators-1.9.1/README.md`

 * *Files 0% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# OctoBot-Evaluators [1.9.0](https://github.com/Drakkar-Software/OctoBot-Evaluators/blob/master/CHANGELOG.md)
+# OctoBot-Evaluators [1.9.1](https://github.com/Drakkar-Software/OctoBot-Evaluators/blob/master/CHANGELOG.md)
 [![Codacy Badge](https://api.codacy.com/project/badge/Grade/a0c08eab5d4c440aa6e3fc3061ad0520)](https://app.codacy.com/gh/Drakkar-Software/OctoBot-Evaluators?utm_source=github.com&utm_medium=referral&utm_content=Drakkar-Software/OctoBot-Evaluators&utm_campaign=Badge_Grade_Dashboard)
 [![PyPI](https://img.shields.io/pypi/v/OctoBot-Evaluators.svg)](https://pypi.python.org/pypi/OctoBot-Evaluators/)
 [![Coverage Status](https://coveralls.io/repos/github/Drakkar-Software/OctoBot-Evaluators/badge.svg)](https://coveralls.io/github/Drakkar-Software/OctoBot-Evaluators)
 [![Github-Action-CI](https://github.com/Drakkar-Software/OctoBot-Evaluators/workflows/OctoBot-Evaluators-CI/badge.svg)](https://github.com/Drakkar-Software/OctoBot-Evaluators/actions)
 [![Build Status](https://cloud.drone.io/api/badges/Drakkar-Software/OctoBot-Evaluators/status.svg)](https://cloud.drone.io/Drakkar-Software/OctoBot-Evaluators)
 
 # Where are evaluators and strategies ?
```

### Comparing `OctoBot-Evaluators-1.9.0/octobot_evaluators/__init__.py` & `OctoBot-Evaluators-1.9.1/octobot_evaluators/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -11,8 +11,8 @@
 #  MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
 #  Lesser General Public License for more details.
 #
 #  You should have received a copy of the GNU Lesser General Public
 #  License along with this library.
 
 PROJECT_NAME = "OctoBot-Evaluators"
-VERSION = "1.9.0"  # major.minor.revision
+VERSION = "1.9.1"  # major.minor.revision
```

### Comparing `OctoBot-Evaluators-1.9.0/octobot_evaluators/api/__init__.py` & `OctoBot-Evaluators-1.9.1/octobot_evaluators/api/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/octobot_evaluators/api/evaluators.py` & `OctoBot-Evaluators-1.9.1/octobot_evaluators/api/evaluators.py`

 * *Files 11% similar despite different names*

```diff
@@ -27,48 +27,54 @@
 import octobot_evaluators.evaluators as evaluator
 
 import octobot_tentacles_manager.api as tentacles_manager_api
 
 LOGGER_NAME = "EvaluatorsAPI"
 
 
-async def create_and_start_all_type_evaluators(tentacles_setup_config: object,
-                                               matrix_id: str,
-                                               exchange_name: str,
-                                               bot_id: str,
-                                               symbols_by_crypto_currencies: dict = None,
-                                               symbols: list = None,
-                                               time_frames: list = None,
-                                               real_time_time_frames: list = None,
-                                               relevant_evaluators=common_constants.CONFIG_WILDCARD,
-                                               ) -> list:
-    return await evaluator.create_and_start_all_type_evaluators(tentacles_setup_config=tentacles_setup_config,
-                                                                matrix_id=matrix_id,
-                                                                exchange_name=exchange_name,
-                                                                bot_id=bot_id,
-                                                                symbols_by_crypto_currencies=symbols_by_crypto_currencies,
-                                                                symbols=symbols,
-                                                                time_frames=time_frames,
-                                                                real_time_time_frames=real_time_time_frames,
-                                                                relevant_evaluators=relevant_evaluators)
+async def create_and_start_all_type_evaluators(
+    tentacles_setup_config: object,
+    matrix_id: str,
+    exchange_name: str,
+    bot_id: str,
+    symbols_by_crypto_currencies: dict = None,
+    symbols: list = None,
+    time_frames: list = None,
+    real_time_time_frames: list = None,
+    relevant_evaluators=common_constants.CONFIG_WILDCARD,
+    config_by_evaluator=None
+) -> list:
+    return await evaluator.create_and_start_all_type_evaluators(
+        tentacles_setup_config=tentacles_setup_config,
+        matrix_id=matrix_id,
+        exchange_name=exchange_name,
+        bot_id=bot_id,
+        symbols_by_crypto_currencies=symbols_by_crypto_currencies,
+        symbols=symbols,
+        time_frames=time_frames,
+        real_time_time_frames=real_time_time_frames,
+        relevant_evaluators=relevant_evaluators,
+        config_by_evaluator=config_by_evaluator
+    )
 
 
 def get_evaluator_classes_from_type(evaluator_type, tentacles_setup_config, activated_only=True) -> list:
     if activated_only:
         return [cls for cls in tentacles_management.get_all_classes_from_parent(
             evaluator.EvaluatorClassTypes[evaluator_type]) if cls.is_enabled(tentacles_setup_config, False)]
     return tentacles_management.get_all_classes_from_parent(evaluator.EvaluatorClassTypes[evaluator_type])
 
 
-async def initialize_evaluators(config, tentacles_setup_config) -> None:
+async def initialize_evaluators(config, tentacles_setup_config, config_by_evaluator=None) -> None:
     """
     :param config: bot config
     :param tentacles_setup_config: tentacles configuration
+    :param config_by_evaluator: dict of evaluator configuration by evaluator name
     """
-    _init_time_frames(config, tentacles_setup_config)
+    _init_time_frames(config, tentacles_setup_config, config_by_evaluator=config_by_evaluator)
     # take evaluators and strategies candles requirements into account if any
     api.init_required_candles_count_from_evaluators_and_strategies(config, tentacles_setup_config)
 
 
 def get_evaluators_time_frames(config) -> list:
     return time_frame_manager.get_config_time_frame(config)
 
@@ -80,17 +86,17 @@
     tentacles_manager_api.update_tentacle_config(
         tentacles_setup_config,
         evaluator_class,
         config_update
     )
 
 
-def _init_time_frames(config, tentacles_setup_config):
+def _init_time_frames(config, tentacles_setup_config, config_by_evaluator=None):
     # Init time frames using enabled strategies
-    api.init_time_frames_from_strategies(config, tentacles_setup_config)
+    api.init_time_frames_from_strategies(config, tentacles_setup_config, config_by_strategy=config_by_evaluator)
 
 
 def create_matrix() -> str:
     created_matrix: matrix.Matrix = matrix.Matrix()
     matrix.Matrices.instance().add_matrix(created_matrix)
     return created_matrix.matrix_id
```

### Comparing `OctoBot-Evaluators-1.9.0/octobot_evaluators/api/initialization.py` & `OctoBot-Evaluators-1.9.1/octobot_evaluators/api/initialization.py`

 * *Files 7% similar despite different names*

```diff
@@ -23,29 +23,35 @@
 
 import octobot_evaluators.evaluators.channel as evaluator_channels
 import octobot_evaluators.constants as constants
 import octobot_evaluators.evaluators as evaluator
 import octobot_evaluators.util as util
 
 
-def init_time_frames_from_strategies(config, tentacles_setup_config) -> None:
-    config[common_constants.CONFIG_TIME_FRAME] = get_time_frames_from_strategies(config, tentacles_setup_config)
+def init_time_frames_from_strategies(config, tentacles_setup_config, config_by_strategy=None) -> None:
+    config[common_constants.CONFIG_TIME_FRAME] = get_time_frames_from_strategies(
+        config, tentacles_setup_config, config_by_strategy=config_by_strategy
+    )
 
 
-def get_time_frames_from_strategies(config, tentacles_setup_config) -> list:
+def get_time_frames_from_strategies(config, tentacles_setup_config, config_by_strategy=None) -> list:
+    config_by_strategy = config_by_strategy or {}
     time_frame_list = set(
         time_frame
         for strategies_eval_class in get_activated_strategies_classes(tentacles_setup_config)
-        for time_frame in get_time_frames_from_strategy(strategies_eval_class, config, tentacles_setup_config)
+        for time_frame in get_time_frames_from_strategy(
+            strategies_eval_class, config, tentacles_setup_config,
+            config_by_strategy.get(strategies_eval_class.get_name())
+        )
     )
     return time_frame_manager.sort_time_frames(list(time_frame_list))
 
 
-def get_time_frames_from_strategy(strategy_class, config, tentacles_setup_config) -> list:
-    return strategy_class.get_required_time_frames(config, tentacles_setup_config)
+def get_time_frames_from_strategy(strategy_class, config, tentacles_setup_config, strategy_config=None) -> list:
+    return strategy_class.get_required_time_frames(config, tentacles_setup_config, strategy_config=strategy_config)
 
 
 def init_required_candles_count_from_evaluators_and_strategies(config, tentacles_setup_config) -> None:
     candles_counts = [util.get_required_candles_count(tentacle_class, tentacles_setup_config)
                       for tentacle_class in get_activated_evaluators(tentacles_setup_config)]
     config[common_constants.CONFIG_TENTACLES_REQUIRED_CANDLES_COUNT] = max(candles_counts) if candles_counts \
         else common_constants.DEFAULT_IGNORED_VALUE
```

### Comparing `OctoBot-Evaluators-1.9.0/octobot_evaluators/api/inspection.py` & `OctoBot-Evaluators-1.9.1/octobot_evaluators/api/inspection.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/octobot_evaluators/api/matrix.py` & `OctoBot-Evaluators-1.9.1/octobot_evaluators/api/matrix.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/octobot_evaluators/constants.py` & `OctoBot-Evaluators-1.9.1/octobot_evaluators/constants.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/octobot_evaluators/enums.py` & `OctoBot-Evaluators-1.9.1/octobot_evaluators/enums.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/octobot_evaluators/errors.py` & `OctoBot-Evaluators-1.9.1/octobot_evaluators/errors.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/octobot_evaluators/evaluators/TA_evaluator.py` & `OctoBot-Evaluators-1.9.1/octobot_evaluators/evaluators/TA_evaluator.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/octobot_evaluators/evaluators/__init__.py` & `OctoBot-Evaluators-1.9.1/octobot_evaluators/evaluators/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/octobot_evaluators/evaluators/abstract_evaluator.py` & `OctoBot-Evaluators-1.9.1/octobot_evaluators/evaluators/abstract_evaluator.py`

 * *Files 1% similar despite different names*

```diff
@@ -222,16 +222,18 @@
                     exchange_api.get_exchange_id_from_matrix_id(self.exchange_name, self.matrix_id)
                 )
             )
         except ImportError as e:
             self.logger.error(f"Can't connect check if backtesting is enabled {e}")
         return False
 
-    async def initialize(self, all_symbols_by_crypto_currencies, time_frames, real_time_time_frames, bot_id):
-        await self.reload_config(bot_id)
+    async def initialize(
+        self, all_symbols_by_crypto_currencies, time_frames, real_time_time_frames, bot_id, specific_config=None
+    ):
+        await self.reload_config(bot_id, specific_config=specific_config)
         currencies, symbols, time_frames = self._get_tentacle_registration_topic(
             all_symbols_by_crypto_currencies, time_frames, real_time_time_frames
         )
         await self._init_registered_topics(all_symbols_by_crypto_currencies, currencies, symbols, time_frames)
 
     async def _init_registered_topics(self, all_symbols_by_crypto_currencies, currencies, symbols, time_frames):
         for currency in currencies:
@@ -371,17 +373,19 @@
         :return: None
         """
         if await self.start(bot_id):
             self.logger.debug("Evaluator started")
         else:
             self.logger.debug("Evaluator not started")
 
-    async def reload_config(self, bot_id: str) -> None:
+    async def reload_config(self, bot_id: str, specific_config=None) -> None:
         self.set_default_config()
-        specific_config = api.get_tentacle_config(self.tentacles_setup_config, self.__class__)
+        specific_config = specific_config or api.get_tentacle_config(
+            self.tentacles_setup_config, self.__class__
+        )
 
         if not specific_config and self.ALLOW_SUPER_CLASS_CONFIG:
             # if nothing in config, try with any super-class' config file
             for super_class in self.get_parent_evaluator_classes(AbstractEvaluator):
                 try:
                     if specific_config := api.get_tentacle_config(self.tentacles_setup_config, super_class):
                         break
```

### Comparing `OctoBot-Evaluators-1.9.0/octobot_evaluators/evaluators/abstract_util.py` & `OctoBot-Evaluators-1.9.1/octobot_evaluators/evaluators/abstract_util.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/octobot_evaluators/evaluators/channel/__init__.py` & `OctoBot-Evaluators-1.9.1/octobot_evaluators/evaluators/channel/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/octobot_evaluators/evaluators/channel/evaluator_channel.py` & `OctoBot-Evaluators-1.9.1/octobot_evaluators/evaluators/channel/evaluator_channel.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/octobot_evaluators/evaluators/channel/evaluators.py` & `OctoBot-Evaluators-1.9.1/octobot_evaluators/evaluators/channel/evaluators.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/octobot_evaluators/evaluators/evaluator_factory.py` & `OctoBot-Evaluators-1.9.1/octobot_evaluators/evaluators/evaluator_factory.py`

 * *Files 3% similar despite different names*

```diff
@@ -23,43 +23,49 @@
 import octobot_evaluators.evaluators as evaluator
 import octobot_evaluators.constants as constants
 import octobot_tentacles_manager.configuration as tm_configuration
 
 LOGGER_NAME = "EvaluatorsFactory"
 
 
-async def create_evaluators(evaluator_parent_class,
-                            tentacles_setup_config: object,
-                            matrix_id: str,
-                            exchange_name: str,
-                            bot_id: str,
-                            crypto_currency_name_by_crypto_currencies: dict,
-                            symbols_by_crypto_currency_tickers: dict,
-                            symbols: list = None,
-                            time_frames: list = None,
-                            real_time_time_frames: list = None,
-                            relevant_evaluators=common_constants.CONFIG_WILDCARD, ) -> list:
+async def create_evaluators(
+    evaluator_parent_class,
+    tentacles_setup_config: object,
+    matrix_id: str,
+    exchange_name: str,
+    bot_id: str,
+    crypto_currency_name_by_crypto_currencies: dict,
+    symbols_by_crypto_currency_tickers: dict,
+    symbols: list = None,
+    time_frames: list = None,
+    real_time_time_frames: list = None,
+    relevant_evaluators=common_constants.CONFIG_WILDCARD,
+    config_by_evaluator=None,
+) -> list:
+    config_by_evaluator = config_by_evaluator or {}
     return [
-        await create_evaluator(evaluator_class,
-                               tentacles_setup_config,
-                               bot_id=bot_id,
-                               matrix_id=matrix_id,
-                               exchange_name=exchange_name,
-                               cryptocurrency=cryptocurrency,
-                               cryptocurrency_name=_get_cryptocurrency_name(
-                                   evaluator_class,
-                                   crypto_currency_name_by_crypto_currencies,
-                                   cryptocurrency),
-                               symbol=symbol,
-                               time_frame=time_frame,
-                               relevant_evaluators=relevant_evaluators,
-                               all_symbols_by_crypto_currencies=symbols_by_crypto_currency_tickers,
-                               time_frames=time_frames,
-                               real_time_time_frames=real_time_time_frames
-                               )
+        await create_evaluator(
+            evaluator_class,
+            tentacles_setup_config,
+            bot_id=bot_id,
+            matrix_id=matrix_id,
+            exchange_name=exchange_name,
+            cryptocurrency=cryptocurrency,
+            cryptocurrency_name=_get_cryptocurrency_name(
+               evaluator_class,
+               crypto_currency_name_by_crypto_currencies,
+               cryptocurrency),
+            symbol=symbol,
+            time_frame=time_frame,
+            relevant_evaluators=relevant_evaluators,
+            all_symbols_by_crypto_currencies=symbols_by_crypto_currency_tickers,
+            time_frames=time_frames,
+            real_time_time_frames=real_time_time_frames,
+            evaluator_configuration=config_by_evaluator.get(evaluator_class.get_name())
+        )
         for evaluator_class in tentacles_management.get_all_classes_from_parent(evaluator_parent_class)
         for cryptocurrency in _get_cryptocurrencies_to_create(evaluator_class,
                                                               crypto_currency_name_by_crypto_currencies)
         for symbol in _get_symbols_to_create(evaluator_class,
                                              symbols_by_crypto_currency_tickers,
                                              cryptocurrency,
                                              symbols)
@@ -98,40 +104,44 @@
     return currency_symbols if currency_symbols and not evaluator_class.get_is_symbol_wildcard() else [None]
 
 
 def _get_time_frames_to_create(evaluator_class, time_frames):
     return time_frames if time_frames and not evaluator_class.get_is_time_frame_wildcard() else [None]
 
 
-async def create_evaluator(evaluator_class,
-                           tentacles_setup_config: object,
-                           bot_id: str,
-                           matrix_id: str,
-                           exchange_name: str,
-                           cryptocurrency: str = None,
-                           cryptocurrency_name: str = None,
-                           symbol: str = None,
-                           time_frame=None,
-                           relevant_evaluators=common_constants.CONFIG_WILDCARD,
-                           all_symbols_by_crypto_currencies=None,
-                           time_frames=None,
-                           real_time_time_frames=None):
+async def create_evaluator(
+    evaluator_class,
+    tentacles_setup_config: object,
+    bot_id: str,
+    matrix_id: str,
+    exchange_name: str,
+    cryptocurrency: str = None,
+    cryptocurrency_name: str = None,
+    symbol: str = None,
+    time_frame=None,
+    relevant_evaluators=common_constants.CONFIG_WILDCARD,
+    all_symbols_by_crypto_currencies=None,
+    time_frames=None,
+    real_time_time_frames=None,
+    evaluator_configuration=None
+):
     try:
         eval_class_instance = _instantiate_evaluator(evaluator_class, tentacles_setup_config, True)
         if api.is_relevant_evaluator(eval_class_instance, relevant_evaluators):
             eval_class_instance.matrix_id = matrix_id
             eval_class_instance.exchange_name = exchange_name if exchange_name else None
             eval_class_instance.cryptocurrency = cryptocurrency
             eval_class_instance.cryptocurrency_name = cryptocurrency_name
             eval_class_instance.symbol = symbol if symbol else None
             eval_class_instance.time_frame = time_frame if time_frame else eval_class_instance.time_frame
             eval_class_instance.evaluator_type = evaluator.evaluator_class_str_to_matrix_type_dict[
                 eval_class_instance.__class__.mro()[constants.EVALUATOR_CLASS_TYPE_MRO_INDEX].__name__]
-            await eval_class_instance.initialize(all_symbols_by_crypto_currencies, time_frames,
-                                                 real_time_time_frames, bot_id)
+            await eval_class_instance.initialize(
+                all_symbols_by_crypto_currencies, time_frames, real_time_time_frames, bot_id, evaluator_configuration
+            )
             await eval_class_instance.prepare()
             return eval_class_instance
     except Exception as e:
         logging.get_logger(LOGGER_NAME).exception(e, True, f"Error when creating evaluator {evaluator_class}: {e}")
     return None
 
 
@@ -156,24 +166,26 @@
     return sorted(
         evaluators,
         key=lambda x: x.get_evaluator_priority(tentacles_setup_config),
         reverse=True
     )
 
 
-async def create_and_start_all_type_evaluators(tentacles_setup_config: object,
-                                               matrix_id: str,
-                                               exchange_name: str,
-                                               bot_id: str,
-                                               symbols_by_crypto_currencies: dict = None,
-                                               symbols: list = None,
-                                               time_frames: list = None,
-                                               real_time_time_frames: list = None,
-                                               relevant_evaluators=common_constants.CONFIG_WILDCARD,
-                                               ) -> list:
+async def create_and_start_all_type_evaluators(
+    tentacles_setup_config: object,
+    matrix_id: str,
+    exchange_name: str,
+    bot_id: str,
+    symbols_by_crypto_currencies: dict = None,
+    symbols: list = None,
+    time_frames: list = None,
+    real_time_time_frames: list = None,
+    relevant_evaluators=common_constants.CONFIG_WILDCARD,
+    config_by_evaluator=None,
+) -> list:
     if not api.get_activated_strategies_classes(tentacles_setup_config):
         # If no strategy is activated, there is no evaluator to create (their evaluation would not be used)
         logging.get_logger(LOGGER_NAME).info(
             f"No evaluator to create for {exchange_name}: no activated evaluator strategy.")
         return []
     try:
         import octobot_trading.api as exchange_api
@@ -184,15 +196,17 @@
                 evaluator_type, tentacles_setup_config,
                 matrix_id=matrix_id, exchange_name=exchange_name,
                 bot_id=bot_id,
                 crypto_currency_name_by_crypto_currencies=crypto_currency_name_by_crypto_currencies,
                 symbols_by_crypto_currency_tickers=symbols_by_crypto_currency_tickers,
                 symbols=symbols, time_frames=time_frames,
                 real_time_time_frames=real_time_time_frames,
-                relevant_evaluators=relevant_evaluators)
+                relevant_evaluators=relevant_evaluators,
+                config_by_evaluator=config_by_evaluator,
+            )
             for evaluator_type in evaluator.EvaluatorClassTypes.values()]
         await _start_evaluators(evaluators, tentacles_setup_config, bot_id)
         return evaluators
     except ImportError:
         logging.get_logger(LOGGER_NAME).error("create_evaluators requires Octobot-Trading package installed")
     return []
```

### Comparing `OctoBot-Evaluators-1.9.0/octobot_evaluators/evaluators/realtime_evaluator.py` & `OctoBot-Evaluators-1.9.1/octobot_evaluators/evaluators/realtime_evaluator.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/octobot_evaluators/evaluators/scripted_evaluator.py` & `OctoBot-Evaluators-1.9.1/octobot_evaluators/evaluators/scripted_evaluator.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/octobot_evaluators/evaluators/social_evaluator.py` & `OctoBot-Evaluators-1.9.1/octobot_evaluators/evaluators/social_evaluator.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/octobot_evaluators/evaluators/strategy_evaluator.py` & `OctoBot-Evaluators-1.9.1/octobot_evaluators/evaluators/strategy_evaluator.py`

 * *Files 0% similar despite different names*

```diff
@@ -406,18 +406,19 @@
             time_frames,
             real_time_time_frames)
         # by default no time frame registration for strategies
         return strategy_currencies, symbols, [self.time_frame]
 
     @classmethod
     def get_required_time_frames(cls, config: dict,
-                                 tentacles_setup_config: tm_configuration.TentaclesSetupConfiguration):
+                                 tentacles_setup_config: tm_configuration.TentaclesSetupConfiguration,
+                                 strategy_config=None):
         if constants.CONFIG_FORCED_TIME_FRAME in config:
             return time_frame_manager.parse_time_frames(config[constants.CONFIG_FORCED_TIME_FRAME])
-        strategy_config: dict = api.get_tentacle_config(tentacles_setup_config, cls)
+        strategy_config: dict = strategy_config or api.get_tentacle_config(tentacles_setup_config, cls)
         if constants.STRATEGIES_REQUIRED_TIME_FRAME in strategy_config:
             return time_frame_manager.parse_time_frames(strategy_config[constants.STRATEGIES_REQUIRED_TIME_FRAME])
         else:
             raise Exception(f"'{constants.STRATEGIES_REQUIRED_TIME_FRAME}' is missing in configuration file")
 
     @classmethod
     def get_required_evaluators(cls, tentacles_config: tm_configuration.TentaclesSetupConfiguration,
```

### Comparing `OctoBot-Evaluators-1.9.0/octobot_evaluators/matrix/__init__.py` & `OctoBot-Evaluators-1.9.1/octobot_evaluators/matrix/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/octobot_evaluators/matrix/channel/__init__.py` & `OctoBot-Evaluators-1.9.1/octobot_evaluators/matrix/channel/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/octobot_evaluators/matrix/channel/matrix.py` & `OctoBot-Evaluators-1.9.1/octobot_evaluators/matrix/channel/matrix.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/octobot_evaluators/matrix/matrices.py` & `OctoBot-Evaluators-1.9.1/octobot_evaluators/matrix/matrices.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/octobot_evaluators/matrix/matrix.py` & `OctoBot-Evaluators-1.9.1/octobot_evaluators/matrix/matrix.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/octobot_evaluators/matrix/matrix_manager.py` & `OctoBot-Evaluators-1.9.1/octobot_evaluators/matrix/matrix_manager.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/octobot_evaluators/octobot_channel_consumer.py` & `OctoBot-Evaluators-1.9.1/octobot_evaluators/octobot_channel_consumer.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/octobot_evaluators/util/__init__.py` & `OctoBot-Evaluators-1.9.1/octobot_evaluators/util/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/octobot_evaluators/util/evaluation_util.py` & `OctoBot-Evaluators-1.9.1/octobot_evaluators/util/evaluation_util.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/setup.py` & `OctoBot-Evaluators-1.9.1/setup.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/tests/evaluators/__init__.py` & `OctoBot-Evaluators-1.9.1/tests/evaluators/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/tests/evaluators/channel/__init__.py` & `OctoBot-Evaluators-1.9.1/tests/evaluators/channel/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/tests/evaluators/channel/test_evaluator_channel.py` & `OctoBot-Evaluators-1.9.1/tests/evaluators/channel/test_evaluator_channel.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/tests/evaluators/test_evaluator_factory.py` & `OctoBot-Evaluators-1.9.1/tests/evaluators/test_evaluator_factory.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/tests/evaluators/test_evaluator_factory_create_evaluators.py` & `OctoBot-Evaluators-1.9.1/tests/evaluators/test_evaluator_factory_create_evaluators.py`

 * *Files 1% similar despite different names*

```diff
@@ -14,14 +14,15 @@
 #  You should have received a copy of the GNU Lesser General Public
 #  License along with this library.
 import pytest
 from mock import patch
 import octobot_evaluators.evaluators.evaluator_factory as evaluator_factory
 from octobot_commons.enums import TimeFrames
 import octobot_commons.symbols
+import octobot_commons.tentacles_management as tentacles_management
 
 
 # All test coroutines will be treated as marked.
 pytestmark = pytest.mark.asyncio
 
 
 @pytest.fixture
@@ -200,19 +201,20 @@
                                    cryptocurrency: str = None,
                                    cryptocurrency_name: str = None,
                                    symbol: str = None,
                                    time_frame=None,
                                    relevant_evaluators=None,
                                    all_symbols_by_crypto_currencies=None,
                                    time_frames=None,
-                                   real_time_time_frames=None):
+                                   real_time_time_frames=None,
+                                   evaluator_configuration=None):
     return evaluator_class(cryptocurrency, cryptocurrency_name, symbol, time_frame, all_symbols_by_crypto_currencies)
 
 
-class EvaluatorWildCard:
+class EvaluatorWildCard(tentacles_management.AbstractTentacle):
     def __init__(self, cryptocurrency, cryptocurrency_name, symbol, time_frame, all_symbols_by_crypto_currencies):
         self.cryptocurrency = cryptocurrency
         self.cryptocurrency_name = cryptocurrency_name
         self.symbol = symbol
         self.time_frame = time_frame
         self.all_symbols_by_crypto_currencies = all_symbols_by_crypto_currencies
```

### Comparing `OctoBot-Evaluators-1.9.0/tests/matrix/__init__.py` & `OctoBot-Evaluators-1.9.1/tests/matrix/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/tests/matrix/channel/__init__.py` & `OctoBot-Evaluators-1.9.1/tests/matrix/channel/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/tests/matrix/channel/test_matrix.py` & `OctoBot-Evaluators-1.9.1/tests/matrix/channel/test_matrix.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/tests/matrix/test_matrices.py` & `OctoBot-Evaluators-1.9.1/tests/matrix/test_matrices.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/tests/matrix/test_matrix.py` & `OctoBot-Evaluators-1.9.1/tests/matrix/test_matrix.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/tests/matrix/test_matrix_manager.py` & `OctoBot-Evaluators-1.9.1/tests/matrix/test_matrix_manager.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/tests/util/__init__.py` & `OctoBot-Evaluators-1.9.1/tests/util/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Evaluators-1.9.0/tests/util/test_evaluation_util.py` & `OctoBot-Evaluators-1.9.1/tests/util/test_evaluation_util.py`

 * *Files identical despite different names*

