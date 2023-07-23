# Comparing `tmp/reinforced-lib-0.2.0.tar.gz` & `tmp/reinforced-lib-1.0.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "reinforced-lib-0.2.0.tar", last modified: Tue Dec 20 21:05:56 2022, max compression
+gzip compressed data, was "reinforced-lib-1.0.0.tar", last modified: Sun Jul 23 11:38:52 2023, max compression
```

## Comparing `reinforced-lib-0.2.0.tar` & `reinforced-lib-1.0.0.tar`

### file list

```diff
@@ -1,50 +1,61 @@
-drwxr-xr-x   0 mwojnar    (501) staff       (20)        0 2022-12-20 21:05:56.723921 reinforced-lib-0.2.0/
--rw-r--r--   0 mwojnar    (501) staff       (20)    16725 2022-10-13 16:37:31.000000 reinforced-lib-0.2.0/LICENSE
--rw-r--r--   0 mwojnar    (501) staff       (20)       66 2022-11-09 17:49:07.000000 reinforced-lib-0.2.0/MANIFEST.in
--rw-r--r--   0 mwojnar    (501) staff       (20)     6166 2022-12-20 21:05:56.724069 reinforced-lib-0.2.0/PKG-INFO
--rw-r--r--   0 mwojnar    (501) staff       (20)     5081 2022-12-20 20:30:18.000000 reinforced-lib-0.2.0/README.md
-drwxr-xr-x   0 mwojnar    (501) staff       (20)        0 2022-12-20 21:05:56.716221 reinforced-lib-0.2.0/reinforced_lib/
--rw-r--r--   0 mwojnar    (501) staff       (20)       37 2022-07-28 11:21:52.000000 reinforced-lib-0.2.0/reinforced_lib/__init__.py
-drwxr-xr-x   0 mwojnar    (501) staff       (20)        0 2022-12-20 21:05:56.718683 reinforced-lib-0.2.0/reinforced_lib/agents/
--rw-r--r--   0 mwojnar    (501) staff       (20)      279 2022-11-14 12:17:58.000000 reinforced-lib-0.2.0/reinforced_lib/agents/__init__.py
--rw-r--r--   0 mwojnar    (501) staff       (20)     1811 2022-12-19 11:50:32.000000 reinforced-lib-0.2.0/reinforced_lib/agents/base_agent.py
-drwxr-xr-x   0 mwojnar    (501) staff       (20)        0 2022-12-20 21:05:56.718995 reinforced-lib-0.2.0/reinforced_lib/agents/core/
--rw-r--r--   0 mwojnar    (501) staff       (20)        0 2022-07-25 14:59:32.000000 reinforced-lib-0.2.0/reinforced_lib/agents/core/__init__.py
--rw-r--r--   0 mwojnar    (501) staff       (20)    13615 2022-12-18 21:52:27.000000 reinforced-lib-0.2.0/reinforced_lib/agents/core/particle_filter.py
--rw-r--r--   0 mwojnar    (501) staff       (20)     6561 2022-12-18 18:18:18.000000 reinforced-lib-0.2.0/reinforced_lib/agents/e_greedy.py
--rw-r--r--   0 mwojnar    (501) staff       (20)     6678 2022-12-18 21:57:07.000000 reinforced-lib-0.2.0/reinforced_lib/agents/softmax.py
--rw-r--r--   0 mwojnar    (501) staff       (20)     8979 2022-12-18 21:09:05.000000 reinforced-lib-0.2.0/reinforced_lib/agents/thompson_sampling.py
--rw-r--r--   0 mwojnar    (501) staff       (20)     5752 2022-12-18 21:57:45.000000 reinforced-lib-0.2.0/reinforced_lib/agents/ucb.py
-drwxr-xr-x   0 mwojnar    (501) staff       (20)        0 2022-12-20 21:05:56.719570 reinforced-lib-0.2.0/reinforced_lib/agents/wifi/
--rw-r--r--   0 mwojnar    (501) staff       (20)       70 2022-06-20 16:12:43.000000 reinforced-lib-0.2.0/reinforced_lib/agents/wifi/__init__.py
--rw-r--r--   0 mwojnar    (501) staff       (20)     9954 2022-12-18 21:55:39.000000 reinforced-lib-0.2.0/reinforced_lib/agents/wifi/particle_filter.py
-drwxr-xr-x   0 mwojnar    (501) staff       (20)        0 2022-12-20 21:05:56.720812 reinforced-lib-0.2.0/reinforced_lib/exts/
--rw-r--r--   0 mwojnar    (501) staff       (20)      172 2022-10-16 11:10:08.000000 reinforced-lib-0.2.0/reinforced_lib/exts/__init__.py
--rw-r--r--   0 mwojnar    (501) staff       (20)    13382 2022-12-19 11:50:32.000000 reinforced-lib-0.2.0/reinforced_lib/exts/base_ext.py
--rw-r--r--   0 mwojnar    (501) staff       (20)     2969 2022-12-19 11:43:39.000000 reinforced-lib-0.2.0/reinforced_lib/exts/ieee_802_11_ax.py
--rw-r--r--   0 mwojnar    (501) staff       (20)     4702 2022-12-19 11:50:32.000000 reinforced-lib-0.2.0/reinforced_lib/exts/utils.py
-drwxr-xr-x   0 mwojnar    (501) staff       (20)        0 2022-12-20 21:05:56.722359 reinforced-lib-0.2.0/reinforced_lib/logs/
--rw-r--r--   0 mwojnar    (501) staff       (20)      244 2022-08-01 10:33:03.000000 reinforced-lib-0.2.0/reinforced_lib/logs/__init__.py
--rw-r--r--   0 mwojnar    (501) staff       (20)     3015 2022-12-19 11:48:51.000000 reinforced-lib-0.2.0/reinforced_lib/logs/base_logger.py
--rw-r--r--   0 mwojnar    (501) staff       (20)     3850 2022-12-19 12:09:13.000000 reinforced-lib-0.2.0/reinforced_lib/logs/csv_logger.py
--rw-r--r--   0 mwojnar    (501) staff       (20)     5330 2022-12-19 12:26:23.000000 reinforced-lib-0.2.0/reinforced_lib/logs/logs_observer.py
--rw-r--r--   0 mwojnar    (501) staff       (20)     5239 2022-12-19 12:15:09.000000 reinforced-lib-0.2.0/reinforced_lib/logs/plots_logger.py
--rw-r--r--   0 mwojnar    (501) staff       (20)     3080 2022-12-19 12:15:09.000000 reinforced-lib-0.2.0/reinforced_lib/logs/stdout_logger.py
--rw-r--r--   0 mwojnar    (501) staff       (20)    18320 2022-12-19 12:55:22.000000 reinforced-lib-0.2.0/reinforced_lib/rlib.py
-drwxr-xr-x   0 mwojnar    (501) staff       (20)        0 2022-12-20 21:05:56.722732 reinforced-lib-0.2.0/reinforced_lib/utils/
--rw-r--r--   0 mwojnar    (501) staff       (20)        0 2022-06-13 14:46:47.000000 reinforced-lib-0.2.0/reinforced_lib/utils/__init__.py
--rw-r--r--   0 mwojnar    (501) staff       (20)     6106 2022-12-19 12:33:21.000000 reinforced-lib-0.2.0/reinforced_lib/utils/exceptions.py
-drwxr-xr-x   0 mwojnar    (501) staff       (20)        0 2022-12-20 21:05:56.716961 reinforced-lib-0.2.0/reinforced_lib.egg-info/
--rw-r--r--   0 mwojnar    (501) staff       (20)     6166 2022-12-20 21:05:56.000000 reinforced-lib-0.2.0/reinforced_lib.egg-info/PKG-INFO
--rw-r--r--   0 mwojnar    (501) staff       (20)     1190 2022-12-20 21:05:56.000000 reinforced-lib-0.2.0/reinforced_lib.egg-info/SOURCES.txt
--rw-r--r--   0 mwojnar    (501) staff       (20)        1 2022-12-20 21:05:56.000000 reinforced-lib-0.2.0/reinforced_lib.egg-info/dependency_links.txt
--rw-r--r--   0 mwojnar    (501) staff       (20)      125 2022-12-20 21:05:56.000000 reinforced-lib-0.2.0/reinforced_lib.egg-info/requires.txt
--rw-r--r--   0 mwojnar    (501) staff       (20)       15 2022-12-20 21:05:56.000000 reinforced-lib-0.2.0/reinforced_lib.egg-info/top_level.txt
-drwxr-xr-x   0 mwojnar    (501) staff       (20)        0 2022-12-20 21:05:56.723275 reinforced-lib-0.2.0/requirements/
--rw-r--r--   0 mwojnar    (501) staff       (20)       53 2022-11-06 13:55:59.000000 reinforced-lib-0.2.0/requirements/requirements-dev.txt
--rw-r--r--   0 mwojnar    (501) staff       (20)       79 2022-12-15 10:27:24.000000 reinforced-lib-0.2.0/requirements/requirements.txt
--rw-r--r--   0 mwojnar    (501) staff       (20)      103 2022-12-20 21:05:56.724388 reinforced-lib-0.2.0/setup.cfg
--rw-r--r--   0 mwojnar    (501) staff       (20)     1736 2022-12-20 20:58:59.000000 reinforced-lib-0.2.0/setup.py
-drwxr-xr-x   0 mwojnar    (501) staff       (20)        0 2022-12-20 21:05:56.723679 reinforced-lib-0.2.0/test/
--rw-r--r--   0 mwojnar    (501) staff       (20)      715 2022-07-27 16:29:37.000000 reinforced-lib-0.2.0/test/test_rlib.py
--rw-r--r--   0 mwojnar    (501) staff       (20)     2580 2022-09-05 09:30:14.000000 reinforced-lib-0.2.0/test/test_rlib_serialization.py
+drwxr-xr-x   0 mwojnar    (501) staff       (20)        0 2023-07-23 11:38:52.209583 reinforced-lib-1.0.0/
+-rw-r--r--   0 mwojnar    (501) staff       (20)    16725 2022-10-13 16:37:31.000000 reinforced-lib-1.0.0/LICENSE
+-rw-r--r--   0 mwojnar    (501) staff       (20)       66 2022-11-09 17:49:07.000000 reinforced-lib-1.0.0/MANIFEST.in
+-rw-r--r--   0 mwojnar    (501) staff       (20)     7195 2023-07-23 11:38:52.209714 reinforced-lib-1.0.0/PKG-INFO
+-rw-r--r--   0 mwojnar    (501) staff       (20)     6080 2023-07-21 19:28:33.000000 reinforced-lib-1.0.0/README.md
+drwxr-xr-x   0 mwojnar    (501) staff       (20)        0 2023-07-23 11:38:52.198540 reinforced-lib-1.0.0/reinforced_lib/
+-rw-r--r--   0 mwojnar    (501) staff       (20)       37 2022-07-28 11:21:52.000000 reinforced-lib-1.0.0/reinforced_lib/__init__.py
+drwxr-xr-x   0 mwojnar    (501) staff       (20)        0 2023-07-23 11:38:52.200326 reinforced-lib-1.0.0/reinforced_lib/agents/
+-rw-r--r--   0 mwojnar    (501) staff       (20)       67 2023-04-29 17:31:22.000000 reinforced-lib-1.0.0/reinforced_lib/agents/__init__.py
+-rw-r--r--   0 mwojnar    (501) staff       (20)     6867 2023-07-22 10:35:31.000000 reinforced-lib-1.0.0/reinforced_lib/agents/base_agent.py
+drwxr-xr-x   0 mwojnar    (501) staff       (20)        0 2023-07-23 11:38:52.200702 reinforced-lib-1.0.0/reinforced_lib/agents/core/
+-rw-r--r--   0 mwojnar    (501) staff       (20)        0 2022-07-25 14:59:32.000000 reinforced-lib-1.0.0/reinforced_lib/agents/core/__init__.py
+-rw-r--r--   0 mwojnar    (501) staff       (20)    13299 2023-07-20 14:56:23.000000 reinforced-lib-1.0.0/reinforced_lib/agents/core/particle_filter.py
+drwxr-xr-x   0 mwojnar    (501) staff       (20)        0 2023-07-23 11:38:52.202570 reinforced-lib-1.0.0/reinforced_lib/agents/deep/
+-rw-r--r--   0 mwojnar    (501) staff       (20)      224 2023-04-29 17:31:22.000000 reinforced-lib-1.0.0/reinforced_lib/agents/deep/__init__.py
+-rw-r--r--   0 mwojnar    (501) staff       (20)    22220 2023-07-20 14:23:22.000000 reinforced-lib-1.0.0/reinforced_lib/agents/deep/ddpg.py
+-rw-r--r--   0 mwojnar    (501) staff       (20)    15721 2023-07-20 14:21:28.000000 reinforced-lib-1.0.0/reinforced_lib/agents/deep/dqn.py
+-rw-r--r--   0 mwojnar    (501) staff       (20)    13620 2023-07-18 20:10:13.000000 reinforced-lib-1.0.0/reinforced_lib/agents/deep/expected_sarsa.py
+-rw-r--r--   0 mwojnar    (501) staff       (20)    14699 2023-07-20 14:17:59.000000 reinforced-lib-1.0.0/reinforced_lib/agents/deep/q_learning.py
+drwxr-xr-x   0 mwojnar    (501) staff       (20)        0 2023-07-23 11:38:52.204348 reinforced-lib-1.0.0/reinforced_lib/agents/mab/
+-rw-r--r--   0 mwojnar    (501) staff       (20)      276 2023-04-29 17:31:22.000000 reinforced-lib-1.0.0/reinforced_lib/agents/mab/__init__.py
+-rw-r--r--   0 mwojnar    (501) staff       (20)     6639 2023-07-20 14:26:12.000000 reinforced-lib-1.0.0/reinforced_lib/agents/mab/e_greedy.py
+-rw-r--r--   0 mwojnar    (501) staff       (20)     5903 2023-07-20 14:27:38.000000 reinforced-lib-1.0.0/reinforced_lib/agents/mab/exp3.py
+-rw-r--r--   0 mwojnar    (501) staff       (20)     6936 2023-07-20 14:57:51.000000 reinforced-lib-1.0.0/reinforced_lib/agents/mab/softmax.py
+-rw-r--r--   0 mwojnar    (501) staff       (20)     6569 2023-07-20 14:56:05.000000 reinforced-lib-1.0.0/reinforced_lib/agents/mab/thompson_sampling.py
+-rw-r--r--   0 mwojnar    (501) staff       (20)     5660 2023-07-20 14:56:05.000000 reinforced-lib-1.0.0/reinforced_lib/agents/mab/ucb.py
+drwxr-xr-x   0 mwojnar    (501) staff       (20)        0 2023-07-23 11:38:52.205513 reinforced-lib-1.0.0/reinforced_lib/exts/
+-rw-r--r--   0 mwojnar    (501) staff       (20)      162 2023-04-29 17:31:22.000000 reinforced-lib-1.0.0/reinforced_lib/exts/__init__.py
+-rw-r--r--   0 mwojnar    (501) staff       (20)    14149 2023-07-20 14:36:17.000000 reinforced-lib-1.0.0/reinforced_lib/exts/base_ext.py
+-rw-r--r--   0 mwojnar    (501) staff       (20)     2149 2023-07-20 14:36:40.000000 reinforced-lib-1.0.0/reinforced_lib/exts/gymnasium.py
+-rw-r--r--   0 mwojnar    (501) staff       (20)     5516 2023-04-29 17:31:22.000000 reinforced-lib-1.0.0/reinforced_lib/exts/utils.py
+drwxr-xr-x   0 mwojnar    (501) staff       (20)        0 2023-07-23 11:38:52.207212 reinforced-lib-1.0.0/reinforced_lib/logs/
+-rw-r--r--   0 mwojnar    (501) staff       (20)      304 2023-04-29 17:31:22.000000 reinforced-lib-1.0.0/reinforced_lib/logs/__init__.py
+-rw-r--r--   0 mwojnar    (501) staff       (20)     3313 2023-07-20 14:39:36.000000 reinforced-lib-1.0.0/reinforced_lib/logs/base_logger.py
+-rw-r--r--   0 mwojnar    (501) staff       (20)     3809 2023-07-20 14:48:22.000000 reinforced-lib-1.0.0/reinforced_lib/logs/csv_logger.py
+-rw-r--r--   0 mwojnar    (501) staff       (20)     5891 2023-07-20 14:40:26.000000 reinforced-lib-1.0.0/reinforced_lib/logs/logs_observer.py
+-rw-r--r--   0 mwojnar    (501) staff       (20)     5697 2023-07-21 18:14:31.000000 reinforced-lib-1.0.0/reinforced_lib/logs/plots_logger.py
+-rw-r--r--   0 mwojnar    (501) staff       (20)     3136 2023-07-17 18:51:18.000000 reinforced-lib-1.0.0/reinforced_lib/logs/stdout_logger.py
+-rw-r--r--   0 mwojnar    (501) staff       (20)     4037 2023-07-21 18:13:03.000000 reinforced-lib-1.0.0/reinforced_lib/logs/tb_logger.py
+-rw-r--r--   0 mwojnar    (501) staff       (20)    23716 2023-07-22 21:35:50.000000 reinforced-lib-1.0.0/reinforced_lib/rlib.py
+drwxr-xr-x   0 mwojnar    (501) staff       (20)        0 2023-07-23 11:38:52.208169 reinforced-lib-1.0.0/reinforced_lib/utils/
+-rw-r--r--   0 mwojnar    (501) staff       (20)     1495 2023-07-17 18:51:18.000000 reinforced-lib-1.0.0/reinforced_lib/utils/__init__.py
+-rw-r--r--   0 mwojnar    (501) staff       (20)     6732 2023-07-15 18:57:31.000000 reinforced-lib-1.0.0/reinforced_lib/utils/exceptions.py
+-rw-r--r--   0 mwojnar    (501) staff       (20)     5807 2023-07-17 18:51:18.000000 reinforced-lib-1.0.0/reinforced_lib/utils/experience_replay.py
+-rw-r--r--   0 mwojnar    (501) staff       (20)     1414 2023-07-17 18:51:18.000000 reinforced-lib-1.0.0/reinforced_lib/utils/jax_utils.py
+drwxr-xr-x   0 mwojnar    (501) staff       (20)        0 2023-07-23 11:38:52.199896 reinforced-lib-1.0.0/reinforced_lib.egg-info/
+-rw-r--r--   0 mwojnar    (501) staff       (20)     7195 2023-07-23 11:38:52.000000 reinforced-lib-1.0.0/reinforced_lib.egg-info/PKG-INFO
+-rw-r--r--   0 mwojnar    (501) staff       (20)     1555 2023-07-23 11:38:52.000000 reinforced-lib-1.0.0/reinforced_lib.egg-info/SOURCES.txt
+-rw-r--r--   0 mwojnar    (501) staff       (20)        1 2023-07-23 11:38:52.000000 reinforced-lib-1.0.0/reinforced_lib.egg-info/dependency_links.txt
+-rw-r--r--   0 mwojnar    (501) staff       (20)      272 2023-07-23 11:38:52.000000 reinforced-lib-1.0.0/reinforced_lib.egg-info/requires.txt
+-rw-r--r--   0 mwojnar    (501) staff       (20)       15 2023-07-23 11:38:52.000000 reinforced-lib-1.0.0/reinforced_lib.egg-info/top_level.txt
+drwxr-xr-x   0 mwojnar    (501) staff       (20)        0 2023-07-23 11:38:52.208661 reinforced-lib-1.0.0/requirements/
+-rw-r--r--   0 mwojnar    (501) staff       (20)       37 2023-07-15 13:17:54.000000 reinforced-lib-1.0.0/requirements/requirements-docs.txt
+-rw-r--r--   0 mwojnar    (501) staff       (20)       78 2023-07-15 13:17:54.000000 reinforced-lib-1.0.0/requirements/requirements-full.txt
+-rw-r--r--   0 mwojnar    (501) staff       (20)      154 2023-07-17 20:22:43.000000 reinforced-lib-1.0.0/requirements/requirements.txt
+-rw-r--r--   0 mwojnar    (501) staff       (20)      103 2023-07-23 11:38:52.210171 reinforced-lib-1.0.0/setup.cfg
+-rw-r--r--   0 mwojnar    (501) staff       (20)     1785 2023-07-23 10:36:11.000000 reinforced-lib-1.0.0/setup.py
+drwxr-xr-x   0 mwojnar    (501) staff       (20)        0 2023-07-23 11:38:52.209267 reinforced-lib-1.0.0/test/
+-rw-r--r--   0 mwojnar    (501) staff       (20)      554 2023-07-22 21:47:24.000000 reinforced-lib-1.0.0/test/test_rlib.py
+-rw-r--r--   0 mwojnar    (501) staff       (20)     2403 2023-07-22 21:47:24.000000 reinforced-lib-1.0.0/test/test_rlib_serialization.py
+-rw-r--r--   0 mwojnar    (501) staff       (20)     5617 2023-07-18 21:06:00.000000 reinforced-lib-1.0.0/test/test_rlib_to_tflite.py
```

### Comparing `reinforced-lib-0.2.0/LICENSE` & `reinforced-lib-1.0.0/LICENSE`

 * *Files identical despite different names*

### Comparing `reinforced-lib-0.2.0/PKG-INFO` & `reinforced-lib-1.0.0/PKG-INFO`

 * *Files 22% similar despite different names*

```diff
@@ -1,136 +1,162 @@
 Metadata-Version: 2.1
 Name: reinforced-lib
-Version: 0.2.0
+Version: 1.0.0
 Summary: Reinforcement learning library
 Home-page: https://github.com/m-wojnar/reinforced-lib
-Download-URL: https://github.com/m-wojnar/reinforced-lib/archive/refs/tags/v0.2.0.tar.gz
+Download-URL: https://github.com/m-wojnar/reinforced-lib/archive/refs/tags/v1.0.0.tar.gz
 Author: Maksymilian Wojnar and Wojciech Ciężobka
 License: Mozilla Public License 2.0 (MPL 2.0)
-Keywords: machine-learning,reinforcement-learning,reinforcement-learning-agent,jax
+Keywords: deep-reinforcement-learning,jax,library,machine-learning,reinforcement-learning
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers
 Classifier: Intended Audience :: Education
 Classifier: Intended Audience :: Science/Research
 Classifier: License :: OSI Approved :: Mozilla Public License 2.0 (MPL 2.0)
 Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Classifier: Topic :: Scientific/Engineering :: Artificial Intelligence
 Classifier: Typing :: Typed
-Requires-Python: >=3.8, <4
+Requires-Python: >=3.9, <4
 Description-Content-Type: text/markdown
-Provides-Extra: dev
+Provides-Extra: docs
+Provides-Extra: full
 License-File: LICENSE
 
 # Reinforced-lib: Reinforcement learning library
 
+[![PyPI version][pypi-badge]][pypi]
+[![License: MPL 2.0][license-badge]][license]
 [![build and test][tests-badge]][github-actions]
 [![Documentation Status][rtd-badge]][documentation]
-[![PyPI version][pypi-badge]][pypi]
-[![License: MPL 2.0](https://img.shields.io/badge/License-MPL%202.0-brightgreen.svg)](https://opensource.org/licenses/MPL-2.0)
 
+[pypi-badge]: https://img.shields.io/pypi/v/reinforced-lib
+[pypi]: https://pypi.org/project/reinforced-lib/
+[license-badge]: https://img.shields.io/badge/License-MPL%202.0-brightgreen.svg
+[license]: https://opensource.org/licenses/MPL-2.0
 [tests-badge]: https://github.com/m-wojnar/reinforced-lib/actions/workflows/python-package.yml/badge.svg
 [github-actions]: https://github.com/m-wojnar/reinforced-lib/actions
 [rtd-badge]: https://readthedocs.org/projects/reinforced-lib/badge/?version=latest
 [documentation]: https://reinforced-lib.readthedocs.io/en/latest/
-[pypi-badge]: https://img.shields.io/pypi/v/reinforced-lib
-[pypi]: https://pypi.org/project/reinforced-lib/
-
-## Overview
 
-**Reinforced-lib** is a Python library designed to support research and prototyping using reinforcement learning
-(RL) algorithms. The library can serve as a simple solution with ready to use RL workflows as well as
-an expandable framework with programmable behaviour. Thanks to the functional implementation of the library's core,
-we can provide full access to the JAX's jit functionality, which boosts the agent's performance significantly.
+**Introducing Reinforced-lib:** a lightweight Python library for rapid development of RL solutions. It is open-source, 
+prioritizes ease of use, provides comprehensive documentation, and offers both deep reinforcement learning 
+(DRL) and classic non-neural agents. Built on [JAX](https://jax.readthedocs.io/en/latest/), it facilitates exporting 
+trained models to embedded devices, and makes it great for research and prototyping with RL algorithms. Access to JAX's 
+JIT functionality ensure high-performance results.
 
 ## Installation
 
 You can install the latest released version of Reinforced-lib from PyPI via:
 
 ```bash
 pip install reinforced-lib
 ```
 
-You can also download source code and install the development dependencies if you want to build the documentation locally:
+To have an easy access to the [example files](https://github.com/m-wojnar/reinforced-lib/tree/main/examples)
+you can clone the source code from our repository, and than install it locally with pip:
 
 ```bash
 git clone git@github.com:m-wojnar/reinforced-lib.git
 cd reinforced-lib
-pip3 install ".[dev]"
+pip install .
 ```
 
-## Example code
-
-```python
-from reinforced_lib import RLib
-from reinforced_lib.agents import ThompsonSampling
-from reinforced_lib.exts import IEEE_802_11_ax
+In the spirit of making Reinforced-lib a lightweight solution, we included only the necessary dependencies in the base 
+requirements. To fully benefit from Reinforced-lib conveniences, like TF Lite export, install with the "full" suffix:
 
-import gym
+```bash
+pip3 install ".[full]"
+```
 
+## Key components
 
-rlib = RLib(
-  agent_type=ThompsonSampling,
-  ext_type=IEEE_802_11_ax
-)
+Reinforced-lib facilitates seamless interaction between RL agents and the environment. Here are the key components 
+within of the library, represented in the API as different modules.
 
-env = gym.make('WifiSimulator-v1')
-env_state, _ = env.reset()
+- **RLib** - The core module which provides a simple and intuitive interface to manage agents, use extensions, 
+  and configure the logging system. Even if you're not a reinforcement learning (RL) expert, *RLib* makes it easy to 
+  implement the agent-environment interaction loop.
 
-terminated = False
-while not terminated:
-  action = rlib.sample(**env_state)
-  env_state, reward, terminated, *_ = env.step(action)
-```
+- **Agents** - Choose from a variety of RL agents available in the *Agents* module. These agents are designed to be 
+  versatile and work with any environment. If needed, you can even create your own agents using our documented recipes.
 
-## Integrated IEEE 802.11ax support
+- **Extensions** - Enhance agent observations with domain-specific knowledge by adding a suitable extension from the 
+  *Extensions* module. This module enables seamless agent switching and parameter tuning without extensive reconfiguration.
 
-Library design is distinctly influenced by the desire to support research in Wi-Fi. It can be a tool for researchers 
-to optimize the Wi-Fi protocols with built-in RL algorithms and provided IEEE 802.11ax environment extension.
+- **Logging** - This module allows you to monitor agent-environment interactions. Customize and adapt logging to your 
+  specific needs, capturing training metrics, internal agent state, or environment observations. The library includes 
+  various loggers for creating plots and output files, simplifying visualization and data processing.
 
-We also provide simple [ns-3](https://www.nsnam.org/) simulation and RL-based rate adaptation manager for the 
-IEEE 802.11ax standard in [examples](https://github.com/m-wojnar/reinforced-lib/tree/main/examples/ns-3).
+The figure below provides a visual representation of Reinforced-lib and the data-flow between its modules.
 
-## Modular architecture
+<img src="docs/resources/data-flow.png" width="600">
 
-**Reinforced-lib** can be well characterized by it's modular architecture which makes the library flexible, universal,
-and easy-to-use. Its key parts are placed in separate modules and connected in a standardized way to provide versatility
-and the possibility to extend individual modules in the future. Nevertheless, Reinforced-lib is a single piece of software
-that can be easily used, thanks to the topmost module, which ensures a simple and common interface for all agents.
+## JAX Backend
 
-<img src="docs/resources/architecture.jpg" width="600">
+Our library is built on top of JAX, a high-performance numerical computing library. JAX makes it easy to implement 
+RL algorithms efficiently. It provides powerful transformations, including JIT compilation,  automatic differentiation, 
+vectorization, and parallelization. Our library is fully compatible with DeepMind's JAX ecosystem, granting access to 
+state-of-the-art RL models and helper libraries. JIT compilation significantly accelerates execution and ensures 
+portability across different architectures (CPUs, GPUs, TPUs) without requiring code modifications.
 
-### The API module
+## Edge Device Export
 
-The API module is the top layer of the library; it exposes a simple and intuitive interface that makes the library easy
-to use. There are several important methods, one of them is responsible for creating a new agent. Another takes the
-observations from the environment as input, updates the state of the agent, and returns the next action proposed by the agent.
-The last two methods are used to persist the state of the agent by storing it in memory.
+Reinforced-lib is designed to work seamlessly on wireless, low-powered devices, where resources are limited. It's the 
+perfect solution for energy-constrained environments that may struggle with other ML frameworks. You can export your 
+trained models to [TensorFlow Lite](https://www.tensorflow.org/lite) with ease, reducing runtime overhead and 
+optimizing performance. This means you can deploy RL agents on resource-limited devices efficiently.
 
-### The extensions module
+## Example code
 
-The Extensions module consists of containers with domain-specific knowledge and ensures the proper use of universal agents
-implemented in **Reinforced-lib**. If a specific problem is implemented in the form of an extension, the module infers and
-provides the appropriate data to the agent, and at the same time requires adequate, corresponding values from the user.
+Experience the simplicity of our library and witness the fundamental agent-environment interaction loop with our 
+straightforward example. This code can by used to train a deep Q-learning agent on the `CartPole-v1` environment 
+effortlessly using Reinforced-lib.
 
-### The agents module
+```python
+import gymnasium as gym
+import haiku as hk
+import optax
+from chex import Array
 
-The Agents module is a collection of universal algorithms, which are called "agents" in RL community. Each agent has
-a similar API to communicate with the Extensions module, which ensures its versatility and expandability. In this release
-of **Reinforced-lib** we focused on the [multi-armed bandit problem](https://en.wikipedia.org/wiki/Multi-armed_bandit),
-hence the imlemented agents are related to this task.
+from reinforced_lib import RLib
+from reinforced_lib.agents.deep import QLearning
+from reinforced_lib.exts import Gymnasium
 
-### The logging module
 
-The Logging module is responsible for collecting data from other modules and observing their state in real time.
-It also has great potential in using the library to create new RL agents - it can be used to develop, evaluate,
-and debug new agents by observing decisions they make; record and visualize how environment state changes in time;
-or provide a simple way to obtain a training summary, metrics, and logs.
+@hk.transform_with_state
+def q_network(x: Array) -> Array:
+    return hk.nets.MLP([256, 2])(x)
+
+
+if __name__ == '__main__':
+    rl = RLib(
+        agent_type=QLearning,
+        agent_params={
+            'q_network': q_network,
+            'optimizer': optax.rmsprop(3e-4, decay=0.95, eps=1e-2),
+        },
+        ext_type=Gymnasium,
+        ext_params={'env_id': 'CartPole-v1'}
+    )
+
+    for epoch in range(300):
+        env = gym.make('CartPole-v1', render_mode='human')
+
+        _, _ = env.reset()
+        action = env.action_space.sample()
+        terminal = False
+
+        while not terminal:
+            env_state = env.step(action.item())
+            action = rl.sample(*env_state)
+            terminal = env_state[2] or env_state[3]
+```
 
 ## Citing Reinforced-lib
 
 To cite this repository:
 
 ```
 @software{reinforcedlib2022,
```

### Comparing `reinforced-lib-0.2.0/reinforced_lib/agents/core/particle_filter.py` & `reinforced-lib-1.0.0/reinforced_lib/agents/core/particle_filter.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 from functools import partial
-from typing import Any, Callable, Tuple
+from typing import Callable
 
 import jax
 import jax.numpy as jnp
 from chex import dataclass, Array, Numeric, PRNGKey, Scalar, Shape
 
 from reinforced_lib.agents import AgentState
 
@@ -14,25 +14,22 @@
     Container for the state of the particle filter agent.
 
     Attributes
     ----------
     positions : array_like
         Positions of the particles.
     logit_weights : array_like
-        Unormalized log weights of the particles.
-    last_measurement : float
-        Time of the last update.
+        Unnormalized log weights of the particles.
     """
 
     positions: Array
     logit_weights: Array
-    last_measurement: Scalar
 
 
-def simple_resample(operands: Tuple[ParticleFilterState, PRNGKey]) -> ParticleFilterState:
+def simple_resample(operands: tuple[ParticleFilterState, PRNGKey]) -> ParticleFilterState:
     """
     Samples new particle positions from a categorical distribution with particle weights, then sets all weights equal.
 
     Parameters
     ----------
     operands : tuple[ParticleFilterState, PRNGKey]
         Tuple containing the filter state and a PRNG key.
@@ -44,23 +41,22 @@
     """
 
     state, key = operands
     positions_idx = jax.random.categorical(key, state.logit_weights, shape=state.positions.shape)
 
     return ParticleFilterState(
         positions=state.positions[positions_idx],
-        logit_weights=jnp.zeros_like(state.logit_weights),
-        last_measurement=state.last_measurement
+        logit_weights=jnp.zeros_like(state.logit_weights)
     )
 
 
 def effective_sample_size(state: ParticleFilterState, threshold: Scalar = 0.5) -> bool:
     r"""
-    Calculates the effective sample size [1]_ (ESS). If ESS is smaller than the number of samples times threshold,
-    than a resampling is necessary.
+    Calculates the effective sample size [9]_ (ESS). If ESS is smaller than the number of sample times threshold,
+    then a resampling is necessary.
 
     Parameters
     ----------
     state : ParticleFilterState
         Current state of the filter.
     threshold : float, default=0.5
         Threshold value used to decide if a resampling is necessary. :math:`thr \in (0, 1)`.
@@ -68,15 +64,15 @@
     Returns
     -------
     bool
         Information whether a resampling should be performed.
 
     References
     ----------
-    .. [1] https://en.wikipedia.org/wiki/Effective_sample_size#Weighted_samples
+    .. [9] https://en.wikipedia.org/wiki/Effective_sample_size#Weighted_samples
     """
 
     weights = jax.nn.softmax(state.logit_weights)
     return 1 < jnp.sum(weights ** 2) * state.positions.size * threshold
 
 
 def simple_transition(state: ParticleFilterState, key: PRNGKey, scale: Scalar, *args) -> ParticleFilterState:
@@ -87,80 +83,79 @@
     Parameters
     ----------
     state : ParticleFilterState
         Current state of the filter.
     key : PRNGKey
         A PRNG key used as the random key.
     scale : float
-        Scale of a random movement of particles. :math:`scale > 0`.
+        Scale of the random movement of particles. :math:`scale > 0`.
 
     Returns
     -------
     ParticleFilterState
         Updated filter state.
     """
 
     positions_update = scale * jax.random.normal(key, state.positions.shape)
 
     return ParticleFilterState(
         positions=state.positions + positions_update,
-        logit_weights=state.logit_weights,
-        last_measurement=state.last_measurement
+        logit_weights=state.logit_weights
     )
 
 
-def linear_transition(state: ParticleFilterState, key: PRNGKey, scale: Scalar, time: Scalar) -> ParticleFilterState:
+def linear_transition(state: ParticleFilterState, key: PRNGKey, scale: Scalar, delta_time: Scalar) -> ParticleFilterState:
     r"""
     Performs movement of the particle positions according to a normal distribution with :math:`\mu = 0` and
     :math:`\sigma = scale \cdot \Delta t`, where :math:`\Delta t` is the time elapsed since the last update.
 
     Parameters
     ----------
     state : ParticleFilterState
         Current state of the filter.
     key : PRNGKey
         A PRNG key used as the random key.
     scale : float
-        Scale of a random movement of particles. :math:`scale > 0`.
-    time : float
-        Current time.
+        Scale of the random movement of particles. :math:`scale > 0`.
+    delta_time : float
+        Time elapsed since the last update.
 
     Returns
     -------
     ParticleFilterState
         Updated filter state.
     """
 
-    return simple_transition(state, key, scale * (time - state.last_measurement))
+    return simple_transition(state, key, scale * delta_time)
 
 
-def affine_transition(state: ParticleFilterState, key: PRNGKey, scale: Array, time: Scalar) -> ParticleFilterState:
+def affine_transition(state: ParticleFilterState, key: PRNGKey, scale: Array, delta_time: Scalar) -> ParticleFilterState:
     r"""
     Performs movement of the particle positions according to a normal distribution with :math:`\mu = 0` and
     :math:`\sigma = scale_0 \cdot \Delta t + scale_1`, where :math:`\Delta t` is the time elapsed since
     the last update.
 
     Parameters
     ----------
     state : ParticleFilterState
         Current state of the filter.
     key : PRNGKey
         A PRNG key used as the random key.
     scale : array_like
-        Scale of a random movement of particles. :math:`scale_0, scale_1 > 0`.
-    time : float
-        Current time.
+        Scale of the random movement of particles. :math:`scale_0, scale_1 > 0`.
+    delta_time : float
+        Time elapsed since the last update.
 
     Returns
     -------
     ParticleFilterState
         Updated filter state.
     """
 
-    return simple_transition(state, key, scale[0] * (time - state.last_measurement) + scale[1])
+    return simple_transition(state, key, scale[0] * delta_time + scale[1])
 
 
 class ParticleFilter:
     """
     Particle filter (sequential Monte Carlo) algorithm estimating the
     internal environment state given noisy or partial observations.
 
@@ -173,16 +168,16 @@
 
         Returns the initial particle positions (`Array`).
 
     positions_shape : array_like
         Shape of the particle positions array.
     weights_shape : array_like
         Shape of the particle weights array.
-    scale : float or array_like
-        Scale of a random movement of the particles.
+    scale : array_like
+        Scale of the random movement of the particles.
     observation_fn : callable
         Function that updates particles based on an observation from the environment; takes two positional arguments:
             - ``state``: the state of the filter (`ParticleFilterState`).
             - ``observation``: an observation from the environment (`any`).
         
         Returns the updated state of the filter (`ParticleFilterState`).
     
@@ -192,34 +187,34 @@
         
         Returns the updated state of the filter (`ParticleFilterState`).
     
     resample_criterion_fn : callable, default=particle_filter.effective_sample_size
         Function that checks if a resampling is necessary; takes one positional argument:
             - ``state``: the state of the filter (`ParticleFilterState`).
         
-        Returns an information whether a resampling should be performed (`bool`).
+        Returns information whether a resampling should be performed (`bool`).
     
     transition_fn : callable, default=particle_filter.simple_transition
         Function that updates the particle positions; takes four positional arguments:
             - ``state``: the state of the filter (`ParticleFilterState`).
             - ``key``: a PRNG key used as a random key (`PRNGKey`).
-            - ``scale``: scale of a random movement of the particles (`float or array_like`).
+            - ``scale``: scale of the random movement of the particles (`array_like`).
             - ``time``: the current time (`float`).
         
         Returns the updated state of the filter (`ParticleFilterState`).
     """
 
     def __init__(
             self,
             initial_distribution_fn: Callable,
             positions_shape: Shape,
             weights_shape: Shape,
             scale: Numeric,
-            observation_fn: Callable[[ParticleFilterState, Any], ParticleFilterState],
-            resample_fn: Callable[[Tuple[ParticleFilterState, PRNGKey]], ParticleFilterState] = simple_resample,
+            observation_fn: Callable[[ParticleFilterState, any], ParticleFilterState],
+            resample_fn: Callable[[tuple[ParticleFilterState, PRNGKey]], ParticleFilterState] = simple_resample,
             resample_criterion_fn: Callable[[ParticleFilterState], bool] = effective_sample_size,
             transition_fn: Callable[[ParticleFilterState, PRNGKey, Numeric, Scalar], ParticleFilterState] = simple_transition
     ) -> None:
         self.init = jax.jit(
             partial(
                 self.init,
                 initial_distribution_fn=initial_distribution_fn,
@@ -269,28 +264,27 @@
         -------
         ParticleFilterState
             Initial state of the Particle Filter.
         """
 
         return ParticleFilterState(
             positions=initial_distribution_fn(key, positions_shape),
-            logit_weights=jnp.zeros(weights_shape),
-            last_measurement=0.0
+            logit_weights=jnp.zeros(weights_shape)
         )
 
     @staticmethod
     def update(
             state: ParticleFilterState,
             key: PRNGKey,
-            observation_fn: Callable[[ParticleFilterState, Any], ParticleFilterState],
-            observation: Any,
-            resample_fn: Callable[[Tuple[ParticleFilterState, PRNGKey]], ParticleFilterState],
+            observation_fn: Callable[[ParticleFilterState, any], ParticleFilterState],
+            observation: any,
+            resample_fn: Callable[[tuple[ParticleFilterState, PRNGKey]], ParticleFilterState],
             resample_criterion_fn: Callable[[ParticleFilterState], bool],
             transition_fn: Callable[[ParticleFilterState, PRNGKey, Numeric, Scalar], ParticleFilterState],
-            time: Scalar,
+            delta_time: Scalar,
             scale: Numeric
     ) -> ParticleFilterState:
         """
         Updates the state of the filter based on an observation from the environment, then
         performs resampling (if necessary) and transition of the particles.
 
         Parameters
@@ -314,61 +308,60 @@
 
             Returns the updated state of the filter (`ParticleFilterState`).
 
         resample_criterion_fn : callable, default=particle_filter.effective_sample_size
             Function that checks if a resampling is necessary; takes one positional argument:
                 - ``state``: the state of the filter (`ParticleFilterState`).
 
-            Returns an information whether a resampling should be performed (`bool`).
+            Returns information whether a resampling should be performed (`bool`).
 
         transition_fn : callable, default=particle_filter.simple_transition
             Function that updates the particle positions; takes four positional arguments:
                 - ``state``: the state of the filter (`ParticleFilterState`).
                 - ``key``: a PRNG key used as a random key (`PRNGKey`).
-                - ``scale``: scale of a random movement of the particles (`float or array_like`).
+                - ``scale``: scale of the random movement of the particles (`array_like`).
                 - ``time``: the current time (`float`).
 
-        time : float
-            Current time.
-        scale : float or array_like
-            Scale of a random movement of the particles.
+        delta_time : float
+            Time difference between the current and the previous observation.
+        scale : array_like
+            Scale of the random movement of the particles.
 
         Returns
         -------
         ParticleFilterState
             Updated filter state.
         """
 
         resample_key, transition_key = jax.random.split(key)
 
         state = observation_fn(state, observation)
         state = jax.lax.cond(resample_criterion_fn(state), resample_fn, lambda op: op[0], (state, resample_key))
-        state = transition_fn(state, transition_key, scale, time)
+        state = transition_fn(state, transition_key, scale, delta_time)
 
         return ParticleFilterState(
             positions=state.positions,
-            logit_weights=state.logit_weights,
-            last_measurement=time
+            logit_weights=state.logit_weights
         )
 
     @staticmethod
     def sample(
             state: ParticleFilterState,
             key: PRNGKey
-    ) -> Tuple[ParticleFilterState, Numeric]:
+    ) -> Numeric:
         """
         Samples the estimated environment state from a categorical distribution with particle weights.
 
         Parameters
         ----------
         state : ParticleFilterState
             Current state of the filter.
         key : PRNGKey
             A PRNG key used as the random key.
 
         Returns
         -------
-        tuple[ParticleFilterState, float or array_like]
-            Tuple containing the filter state and the estimated environment state.
+        array_like
+            Estimated environment state.
         """
 
-        return state, state.positions[jax.random.categorical(key, state.logit_weights)]
+        return state.positions[jax.random.categorical(key, state.logit_weights)]
```

### Comparing `reinforced-lib-0.2.0/reinforced_lib/agents/e_greedy.py` & `reinforced-lib-1.0.0/reinforced_lib/agents/mab/e_greedy.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,22 +1,21 @@
 from functools import partial
-from typing import Tuple
 
-import gym.spaces
+import gymnasium as gym
 import jax
 import jax.numpy as jnp
 from chex import dataclass, Array, Scalar, PRNGKey
 
 from reinforced_lib.agents import BaseAgent, AgentState
 
 
 @dataclass
 class EGreedyState(AgentState):
-    """
-    Container for the state of the e-greedy agent.
+    r"""
+    Container for the state of the :math:`\epsilon`-greedy agent.
 
     Attributes
     ----------
     Q : array_like
         Action-value function estimates for each arm.
     N : array_like
         Number of tries for each arm.
@@ -24,28 +23,32 @@
 
     Q: Array
     N: Array
 
 
 class EGreedy(BaseAgent):
     r"""
-    Epsilon-greedy agent with an optimistic start behavior and optional exponential recency-weighted average update.
+    Epsilon-greedy [5]_ agent with an optimistic start behavior and optional exponential recency-weighted average update.
     It selects a random action from a set of all actions :math:`\mathscr{A}` with probability
     :math:`\epsilon` (exploration), otherwise it chooses the currently best action (exploitation).
 
     Parameters
     ----------
     n_arms : int
         Number of bandit arms. :math:`N \in \mathbb{N}_{+}`.
     e : float
         Experiment rate (epsilon). :math:`\epsilon \in [0, 1]`.
     optimistic_start : float, default=0.0
         Interpreted as the optimistic start to encourage exploration in the early stages.
     alpha : float, default=0.0
         If non-zero, exponential recency-weighted average is used to update :math:`Q` values. :math:`\alpha \in [0, 1]`.
+
+    References
+    ----------
+    .. [5] Richard Sutton and Andrew Barto. 2018. Reinforcement Learning: An Introduction. The MIT Press.
     """
 
     def __init__(
             self,
             n_arms: jnp.int32,
             e: Scalar,
             optimistic_start: Scalar = 0.0,
@@ -57,15 +60,15 @@
         self.n_arms = n_arms
 
         self.init = jax.jit(partial(self.init, n_arms=n_arms, optimistic_start=optimistic_start))
         self.update = jax.jit(partial(self.update, alpha=alpha))
         self.sample = jax.jit(partial(self.sample, e=e))
 
     @staticmethod
-    def parameters_space() -> gym.spaces.Dict:
+    def parameter_space() -> gym.spaces.Dict:
         return gym.spaces.Dict({
             'n_arms': gym.spaces.Box(1, jnp.inf, (1,), jnp.int32),
             'e': gym.spaces.Box(0.0, 1.0, (1,), jnp.float32),
             'optimistic_start': gym.spaces.Box(0.0, jnp.inf, (1,), jnp.float32),
             'alpha': gym.spaces.Box(0.0, 1.0, (1,), jnp.float32)
         })
 
@@ -77,59 +80,59 @@
         })
 
     @property
     def sample_observation_space(self) -> gym.spaces.Dict:
         return gym.spaces.Dict({})
 
     @property
-    def action_space(self) -> gym.spaces.Space:
+    def action_space(self) -> gym.spaces.Discrete:
         return gym.spaces.Discrete(self.n_arms)
 
     @staticmethod
     def init(
             key: PRNGKey,
             n_arms: jnp.int32,
             optimistic_start: Scalar
     ) -> EGreedyState:
-        """
-        Creates and initializes instance of the e-greedy agent for ``n_arms`` arms. Action-value function estimates are
+        r"""
+        Creates and initializes instance of the :math:`\epsilon`-greedy agent for ``n_arms`` arms. Action-value function estimates are
         set to ``optimistic_start`` value and the number of tries is one for each arm.
 
         Parameters
         ----------
         key : PRNGKey
             A PRNG key used as the random key.
         n_arms : int
             Number of bandit arms.
         optimistic_start : float
             Interpreted as the optimistic start to encourage exploration in the early stages.
 
         Returns
         -------
         EGreedyState
-            Initial state of the e-greedy agent.
+            Initial state of the :math:`\epsilon`-greedy agent.
         """
 
         return EGreedyState(
-            Q=(optimistic_start * jnp.ones(n_arms)),
-            N=jnp.ones(n_arms, dtype=jnp.int32)
+            Q=(optimistic_start * jnp.ones((n_arms, 1))),
+            N=jnp.ones((n_arms, 1), dtype=jnp.int32)
         )
 
     @staticmethod
     def update(
         state: EGreedyState,
         key: PRNGKey,
         action: jnp.int32,
         reward: Scalar,
         alpha: Scalar
     ) -> EGreedyState:
         r"""
-        In a stationary case, the action-value estimate for a given arm is updated as
+        In the stationary case, the action-value estimate for a given arm is updated as
         :math:`Q_{t + 1} = Q_t + \frac{1}{t} \lbrack R_t - Q_t \rbrack` after receiving reward :math:`R_t` at step
-        :math:`t` and the number of tries for the corresponding arm is incremented. In a non-stationary case,
+        :math:`t` and the number of tries for the corresponding arm is incremented. In the non-stationary case,
         the update follows the equation :math:`Q_{t + 1} = Q_t + \alpha \lbrack R_t - Q_t \rbrack`.
 
         Parameters
         ----------
         state : EGreedyState
             Current state of the agent.
         key : PRNGKey
@@ -143,61 +146,61 @@
 
         Returns
         -------
         EGreedyState
             Updated agent state.
         """
 
-        def classic_update(operands: Tuple) -> EGreedyState:
+        def classic_update(operands: tuple) -> EGreedyState:
             state, action, reward, alpha = operands
             return EGreedyState(
                 Q=state.Q.at[action].add((reward - state.Q[action]) / state.N[action]),
                 N=state.N.at[action].add(1)
             )
 
-        def erwa_update(operands: Tuple) -> EGreedyState:
+        def erwa_update(operands: tuple) -> EGreedyState:
             state, action, reward, alpha = operands
             return EGreedyState(
                 Q=state.Q.at[action].add(alpha * (reward - state.Q[action])),
                 N=state.N.at[action].add(1)
             )
 
         return jax.lax.cond(alpha == 0, classic_update, erwa_update, (state, action, reward, alpha))
 
     @staticmethod
     def sample(
         state: EGreedyState,
         key: PRNGKey,
         e: Scalar
-    ) -> Tuple[EGreedyState, jnp.int32]:
+    ) -> jnp.int32:
         r"""
         Epsilon-greedy agent follows the policy:
 
         .. math::
-          A =
-          \begin{cases}
-            \operatorname*{argmax}_{a \in \mathscr{A}} Q(a) & \text{with probability } 1 - \epsilon , \\
-            \text{random action} & \text{with probability } \epsilon . \\
-          \end{cases}
+           A =
+           \begin{cases}
+              \operatorname*{argmax}_{a \in \mathscr{A}} Q(a) & \text{with probability } 1 - \epsilon , \\
+              \text{random action} & \text{with probability } \epsilon . \\
+           \end{cases}
 
         Parameters
         ----------
         state : EGreedyState
             Current state of the agent.
         key : PRNGKey
             A PRNG key used as the random key.
         e : float
             Experiment rate (epsilon).
 
         Returns
         -------
-        tuple[EGreedyState, jnp.int32]
-            Tuple containing the updated agent state and the selected action.
+        int
+            Selected action.
         """
 
         epsilon_key, choice_key = jax.random.split(key)
 
         return jax.lax.cond(
             jax.random.uniform(epsilon_key) < e,
-            lambda: (state, jax.random.choice(choice_key, state.Q.size)),
-            lambda: (state, jnp.argmax(state.Q))
+            lambda: jax.random.choice(choice_key, state.Q.size),
+            lambda: jnp.argmax(state.Q)
         )
```

### Comparing `reinforced-lib-0.2.0/reinforced_lib/agents/softmax.py` & `reinforced-lib-1.0.0/reinforced_lib/agents/mab/softmax.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,11 +1,10 @@
 from functools import partial
-from typing import Tuple
 
-import gym.spaces
+import gymnasium as gym
 import jax
 import jax.numpy as jnp
 from chex import dataclass, Array, Scalar, PRNGKey
 
 from reinforced_lib.agents import BaseAgent, AgentState
 
 
@@ -17,63 +16,63 @@
     Attributes
     ----------
     H : array_like
         Preference for each arm.
     r : float
         Average of all obtained rewards :math:`\bar{R}`.
     n : int
-        Number of the step.
+        Step number.
     """
 
     H: Array
     r: Scalar
     n: jnp.int64
 
 
 class Softmax(BaseAgent):
     r"""
     Softmax agent with baseline and optional exponential recency-weighted average update. It learns a preference
-    function :math:`H`, which indicates a preference of selecting one arm over others. Algorithms policy can be
-    controlled by temperature parameter :math:`\tau`. The implementation is inspired by [3]_.
+    function :math:`H`, which indicates a preference of selecting one arm over others. Algorithm policy can be
+    controlled by the temperature parameter :math:`\tau`. The implementation is inspired by the work of Sutton and Barto [5]_.
 
     Parameters
     ----------
     n_arms : int
         Number of bandit arms. :math:`N \in \mathbb{N}_{+}`.
     lr : float
         Step size. :math:`lr > 0`.
     alpha : float, default=0.0
         If non-zero, exponential recency-weighted average is used to update :math:`\bar{R}`. :math:`\alpha \in [0, 1]`.
     tau : float, default=1.0
         Temperature parameter. :math:`\tau > 0`.
-
-    References
-    ----------
-    .. [3]  Sutton, R. S., Barto, A. G. (2018). Reinforcement Learning: An Introduction. The MIT Press. 37-40.
+    multiplier : float, default=1.0
+        Multiplier for the reward. :math:`multiplier > 0`.
     """
 
     def __init__(
             self,
             n_arms: jnp.int32,
             lr: Scalar,
             alpha: Scalar = 0.0,
-            tau: Scalar = 1.0
+            tau: Scalar = 1.0,
+            multiplier: Scalar = 1.0
     ) -> None:
         assert lr > 0
         assert 0 <= alpha <= 1
         assert tau > 0
+        assert multiplier > 0
 
         self.n_arms = n_arms
 
         self.init = jax.jit(partial(self.init, n_arms=n_arms))
-        self.update = jax.jit(partial(self.update, lr=lr, alpha=alpha, tau=tau))
+        self.update = jax.jit(partial(self.update, lr=lr, alpha=alpha, tau=tau, multiplier=multiplier))
         self.sample = jax.jit(partial(self.sample, tau=tau))
 
     @staticmethod
-    def parameters_space() -> gym.spaces.Dict:
+    def parameter_space() -> gym.spaces.Dict:
         return gym.spaces.Dict({
             'n_arms': gym.spaces.Box(1, jnp.inf, (1,), jnp.int32),
             'lr': gym.spaces.Box(0.0, jnp.inf, (1,), jnp.float32),
             'alpha': gym.spaces.Box(0.0, 1.0, (1,), jnp.float32),
             'tau': gym.spaces.Box(0.0, jnp.inf, (1,), jnp.float32)
         })
 
@@ -85,25 +84,25 @@
         })
 
     @property
     def sample_observation_space(self) -> gym.spaces.Dict:
         return gym.spaces.Dict({})
 
     @property
-    def action_space(self) -> gym.spaces.Space:
+    def action_space(self) -> gym.spaces.Discrete:
         return gym.spaces.Discrete(self.n_arms)
 
     @staticmethod
     def init(
             key: PRNGKey,
             n_arms: jnp.int32
     ) -> SoftmaxState:
         r"""
         Creates and initializes instance of the Softmax agent for ``n_arms`` arms. Preferences :math:`H` for each arm
-        are set to zero, as well as the average of all rewards :math:`\bar{R}`. The number of the step :math:`n` is
+        are set to zero, as well as the average of all rewards :math:`\bar{R}`. The step number :math:`n` is
         initialized to one.
 
         Parameters
         ----------
         key : PRNGKey
             A PRNG key used as the random key.
         n_arms : int
@@ -112,46 +111,50 @@
         Returns
         -------
         SoftmaxState
             Initial state of the Softmax agent.
         """
 
         return SoftmaxState(
-            H=jnp.zeros(n_arms),
+            H=jnp.zeros((n_arms, 1)),
             r=0.0,
             n=1
         )
 
     @staticmethod
     def update(
         state: SoftmaxState,
         key: PRNGKey,
         action: jnp.int32,
         reward: Scalar,
         lr: Scalar,
         alpha: Scalar,
-        tau: Scalar
+        tau: Scalar,
+        multiplier: Scalar
     ) -> SoftmaxState:
         r"""
-        Preferences :math:`H` can be learned by the stochastic gradient ascent. The softmax algorithm search
+        Preferences :math:`H` can be learned by stochastic gradient ascent. The softmax algorithm searches
         for such a set of preferences that maximizes the expected reward :math:`\mathbb{E}[R]`.
         The updates of :math:`H` for each action :math:`a` are calculated as:
 
         .. math::
-          H_{t + 1}(a) = H_t(a) + \alpha (R_t - \bar{R}_t)(\mathbb{1}_{A_t = a} - \pi_t(a)),
+           H_{t + 1}(a) = H_t(a) + \alpha (R_t - \bar{R}_t)(\mathbb{1}_{A_t = a} - \pi_t(a)),
 
         where :math:`\bar{R_t}` is the average of all rewards up to but not including step :math:`t`
-        (by definition :math:`\bar{R}_1 = R_1`). The derivation of given formula can be found in [3]_.
+        (by definition :math:`\bar{R}_1 = R_1`). The derivation of given formula can be found in [5]_.
 
         In the stationary case, :math:`\bar{R_t}` can be calculated as
         :math:`\bar{R}_{t + 1} = \bar{R}_t + \frac{1}{t} \lbrack R_t - \bar{R}_t \rbrack`. To improve the
         algorithm's performance in the non-stationary case, we apply
-        :math:`\bar{R}_{t + 1} = \bar{R}_t + \alpha \lbrack R_t - \bar{R}_t \rbrack` with the constant
+        :math:`\bar{R}_{t + 1} = \bar{R}_t + \alpha \lbrack R_t - \bar{R}_t \rbrack` with a constant
         step size :math:`\alpha`.
 
+        Reward :math:`R_t` is multiplied by ``multiplier`` before updating preferences to allow for
+        more flexible reward scaling while keeping the algorithm's properties.
+
         Parameters
         ----------
         state : SoftmaxState
             Current state of the agent.
         key : PRNGKey
             A PRNG key used as the random key.
         action : int
@@ -160,52 +163,56 @@
             Reward collected by the agent after taking the previous action.
         lr : float
             Step size.
         alpha : float
             Exponential recency-weighted average factor (used when :math:`\alpha > 0`).
         tau : float
             Temperature parameter.
+        multiplier : float
+            Multiplier for the reward.
 
         Returns
         -------
         SoftmaxState
             Updated agent state.
         """
 
+        reward *= multiplier
+
         r = jnp.where(state.n == 1, reward, state.r)
         pi = jax.nn.softmax(state.H / tau)
 
         return SoftmaxState(
             H=state.H + lr * (reward - r) * (jnp.zeros_like(state.H).at[action].set(1) - pi),
             r=r + (reward - r) * jnp.where(alpha == 0, 1 / state.n, alpha),
             n=state.n + 1
         )
 
     @staticmethod
     def sample(
         state: SoftmaxState,
         key: PRNGKey,
         tau: Scalar
-    ) -> Tuple[SoftmaxState, jnp.int32]:
+    ) -> jnp.int32:
         r"""
         The policy of the Softmax algorithm is stochastic. The algorithm draws the next action from the softmax
         distribution. The probability of selecting action :math:`i` is calculated as:
 
         .. math::
-          softmax(H)_i = \frac{\exp(H_i / \tau)}{\sum_{h \in H} \exp(h / \tau)} .
+           softmax(H)_i = \frac{\exp(H_i / \tau)}{\sum_{h \in H} \exp(h / \tau)} .
 
         Parameters
         ----------
         state : SoftmaxState
             Current state of the agent.
         key : PRNGKey
             A PRNG key used as the random key.
         tau : float
             Temperature parameter.
 
         Returns
         -------
-        tuple[SoftmaxState, jnp.int32]
-            Tuple containing the updated agent state and the selected action.
+        int
+            Selected action.
         """
 
-        return state, jax.random.categorical(key, state.H / tau)
+        return jax.random.categorical(key, state.H.squeeze() / tau)
```

### Comparing `reinforced-lib-0.2.0/reinforced_lib/agents/thompson_sampling.py` & `reinforced-lib-1.0.0/reinforced_lib/agents/mab/thompson_sampling.py`

 * *Files 25% similar despite different names*

```diff
@@ -1,11 +1,10 @@
 from functools import partial
-from typing import Tuple
 
-import gym.spaces
+import gymnasium as gym
 import jax
 import jax.numpy as jnp
 from chex import dataclass, Array, PRNGKey, Scalar
 
 from reinforced_lib.agents import BaseAgent, AgentState
 
 
@@ -16,85 +15,81 @@
 
     Attributes
     ----------
     alpha : array_like
         Number of successful tries for each arm.
     beta : array_like
         Number of failed tries for each arm.
-    last_decay : array_like
-        Time of the last decay for each arm.
     """
 
     alpha: Array
     beta: Array
-    last_decay: Array
 
 
 class ThompsonSampling(BaseAgent):
     r"""
-    Contextual Bernoulli Thompson sampling agent with the exponential smoothing. The implementation is inspired by [4]_.
-    Thompson sampling is based on a beta distribution with parameters related to the number of successful and
-    failed attempts. Higher values of the parameters decrease the entropy of the distribution while changing
-    the ratio of the parameters shifts the expected value.
+    Contextual Bernoulli Thompson sampling agent with the exponential smoothing. The implementation is inspired by  the
+    work of Krotov et al. [7]_. Thompson sampling is based on a beta distribution with parameters related to the number
+    of successful and failed attempts. Higher values of the parameters decrease the entropy of the distribution while
+    changing the ratio of the parameters shifts the expected value.
 
     Parameters
     ----------
     n_arms : int
         Number of bandit arms. :math:`N \in \mathbb{N}_{+}`.
     decay : float, default=1.0
-        Decay rate, if equals to zero, smoothing is not applied. :math:`w \geq 0`.
+        Decay rate. If equal to zero, smoothing is not applied. :math:`w \geq 0`.
 
     References
     ----------
-    .. [4] Krotov, Alexander & Kiryanov, Anton & Khorov, Evgeny. (2020). Rate Control With Spatial Reuse
-       for Wi-Fi 6 Dense Deployments. IEEE Access. 8. 168898-168909. 10.1109/ACCESS.2020.3023552.
+    .. [7] Alexander Krotov, Anton Kiryanov and Evgeny Khorov. 2020. Rate Control With Spatial Reuse
+       for Wi-Fi 6 Dense Deployments. IEEE Access. 8. 168898-168909.
     """
 
     def __init__(self, n_arms: jnp.int32, decay: Scalar = 1.0) -> None:
         assert decay >= 0
 
         self.n_arms = n_arms
 
         self.init = jax.jit(partial(self.init, n_arms=self.n_arms))
         self.update = jax.jit(partial(self.update, decay=decay))
-        self.sample = jax.jit(partial(self.sample, decay=decay))
+        self.sample = jax.jit(self.sample)
 
     @staticmethod
-    def parameters_space() -> gym.spaces.Dict:
+    def parameter_space() -> gym.spaces.Dict:
         return gym.spaces.Dict({
             'n_arms': gym.spaces.Box(1, jnp.inf, (1,), jnp.int32),
             'decay': gym.spaces.Box(0.0, jnp.inf, (1,))
         })
 
     @property
     def update_observation_space(self) -> gym.spaces.Dict:
         return gym.spaces.Dict({
             'action': gym.spaces.Discrete(self.n_arms),
             'n_successful': gym.spaces.Box(0, jnp.inf, (1,), jnp.int32),
             'n_failed': gym.spaces.Box(0, jnp.inf, (1,), jnp.int32),
-            'time': gym.spaces.Box(0.0, jnp.inf, (1,))
+            'delta_time': gym.spaces.Box(0.0, jnp.inf, (1,))
         })
 
     @property
     def sample_observation_space(self) -> gym.spaces.Dict:
         return gym.spaces.Dict({
-            'time': gym.spaces.Box(0.0, jnp.inf, (1,)),
             'context': gym.spaces.Box(-jnp.inf, jnp.inf, (self.n_arms,))
         })
 
     @property
     def action_space(self) -> gym.spaces.Discrete:
         return gym.spaces.Discrete(self.n_arms)
 
     @staticmethod
     def init(key: PRNGKey, n_arms: jnp.int32) -> ThompsonSamplingState:
         r"""
-        Creates and initializes instance of the Thompson sampling agent for ``n_arms`` arms. The :math:`\mathbf{\alpha}`
+        Creates and initializes an instance of the Thompson sampling agent for ``n_arms`` arms. The :math:`\mathbf{\alpha}`
         and :math:`\mathbf{\beta}` vectors are set to zero to create a non-informative prior distribution.
-        The ``last_decay`` array is also set to zero.
+        The ``last_decay`` is also set to zero.
 
         Parameters
         ----------
         key : PRNGKey
             A PRNG key used as the random key.
         n_arms : int
             Number of bandit arms.
@@ -102,39 +97,38 @@
         Returns
         -------
         ThompsonSamplingState
             Initial state of the Thompson sampling agent.
         """
 
         return ThompsonSamplingState(
-            alpha=jnp.zeros(n_arms),
-            beta=jnp.zeros(n_arms),
-            last_decay=jnp.zeros(n_arms)
+            alpha=jnp.zeros((n_arms,1)),
+            beta=jnp.zeros((n_arms,1))
         )
 
     @staticmethod
     def update(
             state: ThompsonSamplingState,
             key: PRNGKey,
             action: jnp.int32,
             n_successful: jnp.int32,
             n_failed: jnp.int32,
-            time: Scalar,
+            delta_time: Scalar,
             decay: Scalar
     ) -> ThompsonSamplingState:
         r"""
         Thompson sampling can be adjusted to non-stationary environments by exponential smoothing of values of
         vectors :math:`\mathbf{\alpha}` and :math:`\mathbf{\beta}` which increases the entropy of a distribution
         over time. Given a result of trial :math:`s`, we apply the following equations for each action :math:`a`:
 
         .. math::
-          \begin{gather}
-            \mathbf{\alpha}_{t + 1}(a) = \mathbf{\alpha}_t(a) e^{\frac{-\Delta t}{w}} + \mathbb{1}_{A = a} \cdot s , \\
-            \mathbf{\beta}_{t + 1}(a) = \mathbf{\beta}_t(a) e^{\frac{-\Delta t}{w}} + \mathbb{1}_{A = a} \cdot (1 - s) ,
-          \end{gather}
+           \begin{gather}
+              \mathbf{\alpha}_{t + 1}(a) = \mathbf{\alpha}_t(a) e^{\frac{-\Delta t}{w}} + \mathbb{1}_{A = a} \cdot s , \\
+              \mathbf{\beta}_{t + 1}(a) = \mathbf{\beta}_t(a) e^{\frac{-\Delta t}{w}} + \mathbb{1}_{A = a} \cdot (1 - s) ,
+           \end{gather}
 
         where :math:`\Delta t` is the time elapsed since the last action selection and :math:`w` is the decay rate.
 
         Parameters
         ----------
         state : ThompsonSamplingState
             Current state of the agent.
@@ -142,135 +136,61 @@
             A PRNG key used as the random key.
         action : int
             Previously selected action.
         n_successful : int
             Number of successful tries.
         n_failed : int
             Number of failed tries.
-        time : float
-            Current time.
+        delta_time : float
+            Time elapsed since the last action selection.
         decay : float
             Decay rate.
 
         Returns
         -------
         ThompsonSamplingState
             Updated agent state.
         """
 
-        state = ThompsonSampling._decay_one(state, action, time, decay)
-        state = ThompsonSamplingState(
-            alpha=state.alpha.at[action].add(n_successful),
-            beta=state.beta.at[action].add(n_failed),
-            last_decay=state.last_decay
+        smoothing_value = jnp.exp(-decay * delta_time)
+
+        return ThompsonSamplingState(
+            alpha=(state.alpha * smoothing_value).at[action].add(n_successful),
+            beta=(state.beta * smoothing_value).at[action].add(n_failed)
         )
-        return state
 
     @staticmethod
     def sample(
             state: ThompsonSamplingState,
             key: PRNGKey,
-            time: Scalar,
-            context: Array,
-            decay: Scalar
-    ) -> Tuple[ThompsonSamplingState, jnp.int32]:
+            context: Array
+    ) -> jnp.int32:
         r"""
         The Thompson sampling policy is stochastic. The algorithm draws :math:`q_a` from the distribution
         :math:`\operatorname{Beta}(1 + \mathbf{\alpha}(a), 1 + \mathbf{\beta}(a))` for each arm :math:`a`.
-        The next action is selected as:
+        The next action is selected as
 
         .. math::
-          A = \operatorname*{argmax}_{a \in \mathscr{A}} q_a r_a ,
+           A = \operatorname*{argmax}_{a \in \mathscr{A}} q_a r_a ,
 
         where :math:`r_a` is contextual information for the arm :math:`a`, and :math:`\mathscr{A}` is a set
         of all actions.
 
         Parameters
         ----------
         state : ThompsonSamplingState
             Current state of the agent.
         key : PRNGKey
             A PRNG key used as the random key.
-        time : float
-            Current time.
         context : array_like
             One-dimensional array of features for each arm.
-        decay : float
-            Decay rate.
 
         Returns
         -------
-        tuple[ThompsonSamplingState, int]
-            Tuple containing the updated agent state and the selected action.
+        int
+            Selected action.
         """
 
-        state = ThompsonSampling._decay_all(state, time, decay)
-        success_prob = jax.random.beta(key, 1 + state.alpha, 1 + state.beta)
+        success_prob = jax.random.beta(key, 1 + state.alpha, 1 + state.beta).squeeze()
         action = jnp.argmax(success_prob * context)
-        return state, action
-
-    @staticmethod
-    def _decay_one(
-            state: ThompsonSamplingState,
-            action: jnp.int32,
-            time: Scalar,
-            decay: Scalar
-    ) -> ThompsonSamplingState:
-        """
-        Applies exponential smoothing for the parameters related to a given action.
-
-        Parameters
-        ----------
-        state : ThompsonSamplingState
-            Current state of the agent.
-        action : int
-            Action to apply smoothing.
-        time : float
-            Current time.
-        decay : float
-            Decay rate.
-
-        Returns
-        -------
-        ThompsonSamplingState
-            Updated agent state.
-        """
-
-        smoothing_value = jnp.exp(decay * (state.last_decay[action] - time))
-        state = ThompsonSamplingState(
-            alpha=state.alpha.at[action].multiply(smoothing_value),
-            beta=state.beta.at[action].multiply(smoothing_value),
-            last_decay=state.last_decay.at[action].set(time)
-        )
-        return state
-
-    @staticmethod
-    def _decay_all(
-            state: ThompsonSamplingState,
-            time: Scalar,
-            decay: Scalar
-    ) -> ThompsonSamplingState:
-        """
-        Applies exponential smoothing for the parameters of all arms.
-
-        Parameters
-        ----------
-        state : ThompsonSamplingState
-            Current state of the agent.
-        time : float
-            Current time.
-        decay : float
-            Decay rate.
-
-        Returns
-        -------
-        ThompsonSamplingState
-            Updated agent state.
-        """
 
-        smoothing_value = jnp.exp(decay * (state.last_decay - time))
-        state = ThompsonSamplingState(
-            alpha=state.alpha * smoothing_value,
-            beta=state.beta * smoothing_value,
-            last_decay=jnp.full_like(state.last_decay, time)
-        )
-        return state
+        return action
```

### Comparing `reinforced-lib-0.2.0/reinforced_lib/agents/ucb.py` & `reinforced-lib-1.0.0/reinforced_lib/agents/mab/ucb.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,11 +1,10 @@
 from functools import partial
-from typing import Tuple
 
-import gym.spaces
+import gymnasium as gym
 import jax
 import jax.numpy as jnp
 from chex import dataclass, Array, Scalar, PRNGKey
 
 from reinforced_lib.agents import BaseAgent, AgentState
 
 
@@ -35,19 +34,19 @@
     Parameters
     ----------
     n_arms : int
         Number of bandit arms. :math:`N \in \mathbb{N}_{+}`.
     c : float
         Degree of exploration. :math:`c \geq 0`.
     gamma : float, default=1.0
-        If less than one, a discounted UCB algorithm [5]_ is used. :math:`\gamma \in (0, 1]`.
+        If less than one, a discounted UCB algorithm [8]_ is used. :math:`\gamma \in (0, 1]`.
 
     References
     ----------
-    .. [5] Garivier, A., & Moulines, E. (2008). On Upper-Confidence Bound Policies for Non-Stationary
+    .. [8] Aurélien Garivier, Eric Moulines. 2008. On Upper-Confidence Bound Policies for Non-Stationary
        Bandit Problems. 10.48550/ARXIV.0805.3415.
     """
 
     def __init__(
             self,
             n_arms: jnp.int32,
             c: Scalar,
@@ -59,15 +58,15 @@
         self.n_arms = n_arms
 
         self.init = jax.jit(partial(self.init, n_arms=n_arms))
         self.update = jax.jit(partial(self.update, gamma=gamma))
         self.sample = jax.jit(partial(self.sample, c=c))
 
     @staticmethod
-    def parameters_space() -> gym.spaces.Dict:
+    def parameter_space() -> gym.spaces.Dict:
         return gym.spaces.Dict({
             'n_arms': gym.spaces.Box(1, jnp.inf, (1,), jnp.int32),
             'c': gym.spaces.Box(0.0, jnp.inf, (1,), jnp.float32),
             'gamma': gym.spaces.Box(0.0, 1.0, (1,), jnp.float32)
         })
 
     @property
@@ -104,36 +103,36 @@
         Returns
         -------
         UCBState
             Initial state of the UCB agent.
         """
 
         return UCBState(
-            R=jnp.zeros(n_arms),
-            N=jnp.ones(n_arms)
+            R=jnp.zeros((n_arms, 1)),
+            N=jnp.ones((n_arms, 1))
         )
 
     @staticmethod
     def update(
         state: UCBState,
         key: PRNGKey,
         action: jnp.int32,
         reward: Scalar,
         gamma: Scalar
     ) -> UCBState:
         r"""
-        In a stationary case, the sum of the rewards for a given arm is increased by reward :math:`r` obtained after
-        step :math:`t` and the number of tries for the corresponding arm is incremented. In a non-stationary case,
-        the update follows the equations:
+        In the stationary case, the sum of the rewards for a given arm is increased by reward :math:`r` obtained after
+        step :math:`t` and the number of tries for the corresponding arm is incremented. In the non-stationary case,
+        the update follows the equations
 
         .. math::
-          \begin{gather}
-            R_{t + 1}(a) = \mathbb{1}_{A_t = a} r + \gamma R_t(a) , \\
-            N_{t + 1}(a) = \mathbb{1}_{A_t = a} + \gamma N_t(a).
-          \end{gather}
+           \begin{gather}
+              R_{t + 1}(a) = \mathbb{1}_{A_t = a} r + \gamma R_t(a) , \\
+              N_{t + 1}(a) = \mathbb{1}_{A_t = a} + \gamma N_t(a).
+           \end{gather}
 
         Parameters
         ----------
         state : UCBState
             Current state of agent.
         key : PRNGKey
             A PRNG key used as the random key.
@@ -156,20 +155,20 @@
         )
 
     @staticmethod
     def sample(
         state: UCBState,
         key: PRNGKey,
         c: Scalar
-    ) -> Tuple[UCBState, jnp.int32]:
+    ) -> jnp.int32:
         r"""
-        UCB agent follows the policy:
+        UCB agent follows the policy
 
         .. math::
-          A = \operatorname*{argmax}_{a \in \mathscr{A}} \left[ Q(a) + c \sqrt{\frac{\ln \left( {\sum_{a' \in \mathscr{A}}} N(a') \right) }{N(a)}} \right] .
+           A = \operatorname*{argmax}_{a \in \mathscr{A}} \left[ Q(a) + c \sqrt{\frac{\ln \left( {\sum_{a' \in \mathscr{A}}} N(a') \right) }{N(a)}} \right] .
 
         where :math:`\mathscr{A}` is a set of all actions and :math:`Q` is calculated as :math:`Q(a) = \frac{R(a)}{N(a)}`.
         The second component of the sum represents a sort of upper bound on the value of :math:`Q`, where :math:`c`
         behaves like a confidence interval and the square root - like an approximation of the :math:`Q` function
         estimation uncertainty. Note that the UCB policy is deterministic.
 
         Parameters
@@ -179,14 +178,15 @@
         key : PRNGKey
             A PRNG key used as the random key.
         c : float
             Degree of exploration.
 
         Returns
         -------
-        tuple[UCBState, jnp.int32]
-            Tuple containing the updated agent state and the selected action.
+        int
+            Selected action.
         """
 
         Q = state.R / state.N
         t = jnp.sum(state.N)
-        return state, jnp.argmax(Q + c * jnp.sqrt(jnp.log(t) / state.N))
+
+        return jnp.argmax(Q + c * jnp.sqrt(jnp.log(t) / state.N))
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `reinforced-lib-0.2.0/reinforced_lib/exts/base_ext.py` & `reinforced-lib-1.0.0/reinforced_lib/exts/base_ext.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,86 +1,87 @@
 from abc import ABC, abstractmethod
 from functools import partial
 import inspect
-from typing import Any, Callable, Dict, List, Tuple, Union
+from typing import Union
 
-import gym.spaces
+import gymnasium as gym
 
-from reinforced_lib.exts.utils import test_box, test_discrete, test_multi_binary, test_multi_discrete, test_space
+from reinforced_lib.exts.utils import *
 from reinforced_lib.utils.exceptions import IncorrectSpaceError, IncompatibleSpacesError, NoDefaultParameterError
 
 
 class BaseExt(ABC):
     """
-    Container for a domain-specific knowledge and functions for a given environment. Provides the transformation
-    from the observation functions and the observation space to the agents update and sample spaces. Stores the
-    default argument values for agents initialization.
+    Container for domain-specific knowledge and functions for a given environment. Provides the transformation
+    from the raw observations to the agent update and sample spaces. Stores the default argument values for
+    agent initialization.
     """
 
     def __init__(self) -> None:
-        self._observation_functions: Dict[str, Callable] = {}
-        self._parameter_functions: Dict[str, Callable] = {}
+        self._observation_functions: dict[str, Callable] = {}
+        self._parameter_functions: dict[str, Callable] = {}
+
+        self._add_action_to_observations = False
 
         for name in dir(self):
             obj = getattr(self, name)
 
             if hasattr(obj, 'observation_info'):
                 self._observation_functions[obj.observation_info.name] = obj
 
             if hasattr(obj, 'parameter_info'):
                 self._parameter_functions[obj.parameter_info.name] = obj
 
     @property
     @abstractmethod
     def observation_space(self) -> gym.spaces.Space:
         """
-        Basic observations of the environment in OpenAI Gym format.
+        Basic observations of the environment in Gymnasium format.
         """
 
         pass
 
     def get_agent_params(
             self,
             agent_type: type = None,
-            agent_parameters_space: gym.spaces.Dict = None,
-            user_parameters: Dict[str, Any] = None
-    ) -> Dict[str, Any]:
-        """
-        Composes agent initialization parameters from parameters passed by the user and default values
-        defined in the parameter functions. Returns a dictionary with the parameters fitting the agents
-        parameters space.
+            agent_parameter_space: gym.spaces.Dict = None,
+            user_parameters: dict[str, any] = None
+    ) -> dict[str, any]:
+        """
+        Composes agent initialization arguments from values passed by the user and default values stored in the
+        parameter functions. Returns a dictionary with the parameters matching the agent parameters space.
 
         Parameters
         ----------
         agent_type : type, optional
             Type of the selected agent.
-        agent_parameters_space : gym.spaces.Dict, optional
-            Parameters required by the agents' constructor in OpenAI Gym format.
+        agent_parameter_space : gym.spaces.Dict, optional
+            Parameters required by the agents' constructor in Gymnasium format.
         user_parameters : dict, optional
             Parameters provided by the user.
 
         Returns
         -------
         dict
             Dictionary with the initialization parameters for the agent.
         """
 
-        if agent_parameters_space is None:
-            return {}
+        parameters = user_parameters if user_parameters else {}
+
+        if agent_parameter_space is None:
+            return parameters
 
         default_parameters = set()
 
         if agent_type is not None:
             for key, value in inspect.signature(agent_type.__init__).parameters.items():
                 if value.default != inspect._empty:
                     default_parameters.add(key)
 
-        parameters = user_parameters if user_parameters else {}
-
-        for name, space in agent_parameters_space.spaces.items():
+        for name, space in agent_parameter_space.spaces.items():
             if name in parameters:
                 continue
 
             if name not in self._parameter_functions:
                 if name in default_parameters:
                     continue
 
@@ -98,37 +99,48 @@
 
     def setup_transformations(
             self,
             agent_update_space: gym.spaces.Space = None,
             agent_sample_space: gym.spaces.Space = None
     ) -> None:
         """
-        Create functions that transform environment observations and values provided by the observation functions
-        to the agents update and sample space.
+        Creates functions that transform raw observations and values provided by the observation functions
+        to the agent update and sample spaces.
 
         Parameters
         ----------
         agent_update_space : gym.spaces.Space, optional
-            Observations required by the agents ``update`` function in OpenAI Gym format.
+            Observations required by the agent ``update`` function in Gymnasium format.
         agent_sample_space : gym.spaces.Space, optional
-            Observations required by the agents ``sample`` function in OpenAI Gym format.
+            Observations required by the agent ``sample`` function in Gymnasium format.
         """
 
+        if 'action' not in self._observation_functions and \
+                isinstance(self.observation_space, gym.spaces.Dict) and \
+                'action' not in self.observation_space:
+
+            if 'action' in agent_update_space.spaces:
+                self.observation_space['action'] = agent_update_space['action']
+            if 'action' in agent_sample_space.spaces:
+                self.observation_space['action'] = agent_sample_space['action']
+
+            self._add_action_to_observations = True
+
         self._update_space_transform = self._transform_spaces(self.observation_space, agent_update_space)
         self._sample_space_transform = self._transform_spaces(self.observation_space, agent_sample_space)
 
     def _transform_spaces(
             self,
             in_space: gym.spaces.Space,
             out_space: gym.spaces.Space,
             accessor: Union[str, int] = None
     ) -> Callable:
         """
         Creates function that transforms environment observations and values provided by the observation
-        functions to a given space.
+        functions to a given space. If the ``out_space`` is not defined, returns observations unchanged.
 
         Parameters
         ----------
         in_space : gym.spaces.Space
             Source space.
         out_space : gym.spaces.Space
             Target space.
@@ -145,14 +157,15 @@
             return lambda *args, **kwargs: None
 
         simple_types = {
             gym.spaces.Box: test_box,
             gym.spaces.Discrete: test_discrete,
             gym.spaces.MultiBinary: test_multi_binary,
             gym.spaces.MultiDiscrete: test_multi_discrete,
+            gym.spaces.Sequence: test_sequence,
             gym.spaces.Space: test_space
         }
 
         if type(out_space) in simple_types:
             if type(in_space) not in simple_types:
                 raise IncompatibleSpacesError(in_space, out_space)
 
@@ -167,15 +180,15 @@
                 if func_space is None or test_function(func_space, out_space):
                     return observation_function
 
         if isinstance(out_space, gym.spaces.Dict):
             if not isinstance(in_space, gym.spaces.Dict):
                 raise IncompatibleSpacesError(in_space, out_space)
 
-            observations: Dict[str, Callable] = {}
+            observations: dict[str, Callable] = {}
 
             for name, space in out_space.spaces.items():
                 if name in in_space.spaces:
                     if type(space) not in simple_types:
                         observations[name] = self._transform_spaces(in_space[name], space, name)
                     elif simple_types[type(space)](in_space[name], space):
                         observations[name] = partial(lambda inner_name, *args, **kwargs: kwargs[inner_name], name)
@@ -197,30 +210,30 @@
 
             return partial(self._dict_transform, observations, accessor)
 
         if isinstance(out_space, gym.spaces.Tuple):
             if not isinstance(in_space, gym.spaces.Tuple) or len(in_space.spaces) != len(out_space.spaces):
                 raise IncompatibleSpacesError(in_space, out_space)
 
-            observations: List[Callable] = []
+            observations: list[Callable] = []
 
             for i, (agent_space, ext_space) in enumerate(zip(in_space.spaces, out_space.spaces)):
                 if type(agent_space) not in simple_types:
                     observations.append(self._transform_spaces(ext_space, agent_space, i))
                 elif simple_types[type(agent_space)](ext_space, agent_space):
                     observations.append(partial(lambda inner_i, *args, **kwargs: args[inner_i], i))
                 else:
                     raise IncompatibleSpacesError(agent_space, in_space)
 
             return partial(self._tuple_transform, observations, accessor)
 
         raise IncorrectSpaceError()
 
     @staticmethod
-    def _get_nested_args(accessor: Union[str, int], *args, **kwargs) -> Tuple[Tuple, Dict]:
+    def _get_nested_args(accessor: Union[str, int], *args, **kwargs) -> tuple[tuple, dict]:
         """
         Selects the appropriate nested args or kwargs.
 
         Parameters
         ----------
         accessor : str or int
             Path to nested observations.
@@ -237,22 +250,22 @@
 
         if accessor is not None:
             if isinstance(accessor, int):
                 arguments = args[accessor]
             else:
                 arguments = kwargs[accessor]
 
-            if isinstance(arguments, Dict):
+            if isinstance(arguments, dict):
                 return tuple(), arguments
             else:
                 return arguments, {}
 
         return args, kwargs
 
-    def _simple_transform(self, accessor: Union[str, int], *args, **kwargs) -> Any:
+    def _simple_transform(self, accessor: Union[str, int], *args, **kwargs) -> any:
         """
         Returns the appropriate observation from environment observations.
 
         Parameters
         ----------
         accessor : str or int
             Path to nested observations.
@@ -271,15 +284,15 @@
 
         if len(args) > 0:
             return args[0]
         else:
             first, *_ = kwargs.values()
             return first
 
-    def _function_transform(self, func: Callable, name: str, accessor: Union[str, int], *args, **kwargs) -> Any:
+    def _function_transform(self, func: Callable, name: str, accessor: Union[str, int], *args, **kwargs) -> any:
         """
         Returns the appropriate observation from the observation function or from environment observations
         if present.
 
         Parameters
         ----------
         func : Callable
@@ -302,15 +315,15 @@
         args, kwargs = self._get_nested_args(accessor, *args, **kwargs)
 
         if name in kwargs:
             return kwargs[name]
         else:
             return func(*args, **kwargs)
 
-    def _dict_transform(self, observations: Dict[str, Callable], accessor: Union[str, int], *args, **kwargs) -> Dict:
+    def _dict_transform(self, observations: dict[str, Callable], accessor: Union[str, int], *args, **kwargs) -> dict:
         """
         Returns a dictionary filled with appropriate environment observations and values provided by
         the observation functions.
 
         Parameters
         ----------
         observations : dict[str, Callable]
@@ -327,15 +340,15 @@
         dict
             Dictionary with functions providing observations.
         """
 
         args, kwargs = self._get_nested_args(accessor, *args, **kwargs)
         return {name: func(*args, **kwargs) for name, func in observations.items()}
 
-    def _tuple_transform(self, observations: List[Callable], accessor: Union[str, int], *args, **kwargs) -> Tuple:
+    def _tuple_transform(self, observations: list[Callable], accessor: Union[str, int], *args, **kwargs) -> tuple:
         """
         Returns a tuple filled with appropriate environment observations and values provided by
         the observation functions.
 
         Parameters
         ----------
         observations : list[Callable]
@@ -352,26 +365,31 @@
         tuple
             Tuple with functions providing observations.
         """
 
         args, kwargs = self._get_nested_args(accessor, *args, **kwargs)
         return tuple(func(*args, **kwargs) for func in observations)
 
-    def transform(self, *args, **kwargs) -> Tuple[Any, Any]:
+    def transform(self, *args, action: any = None, **kwargs) -> tuple[any, any]:
         """
-        Transforms environment observations and values provided by the observation functions to
-        the agent observation and sample spaces.
+        Transforms raw observations and values provided by the observation functions to the agent observation
+        and sample spaces. Provides the last action selected by the agent if it is required by the agent.
 
         Parameters
         ----------
         *args : tuple
             Environment observations.
+        action : any
+            The last action selected by the agent.
         **kwargs : dict
             Environment observations.
 
         Returns
         -------
         tuple[any, any]
-            Agents update and sample observations.
+            Agent update and sample observations.
         """
 
+        if self._add_action_to_observations:
+            kwargs['action'] = action
+
         return self._update_space_transform(*args, **kwargs), self._sample_space_transform(*args, **kwargs)
```

### Comparing `reinforced-lib-0.2.0/reinforced_lib/exts/utils.py` & `reinforced-lib-1.0.0/reinforced_lib/exts/utils.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,23 +1,23 @@
 from typing import Callable, NamedTuple
 
-import gym.spaces
+import gymnasium as gym
 import numpy as np
 
 
 class ObservationInfo(NamedTuple):
     """
     Description of the observation function that provides one of the values from the agent observation space.
 
     Attributes
     ----------
     name : str
         Name of the provided observation.
     type : gym.spaces.Space
-        Type of the provided value in OpenAI Gym format.
+        Type of the provided value in Gymnasium format.
     """
 
     name: str
     type: gym.spaces.Space
 
 
 class ParameterInfo(NamedTuple):
@@ -25,15 +25,15 @@
     Description of the parameter function that provides one of the parameters of the agent constructor.
 
     Attributes
     ----------
     name : str
         Name of the provided parameter.
     type : gym.spaces.Space
-        Type of the provided parameter in OpenAI Gym format.
+        Type of the provided parameter in Gymnasium format.
     """
 
     name: str
     type: gym.spaces.Space
 
 
 def observation(observation_name: str = None, observation_type: gym.spaces.Space = None) -> Callable:
@@ -41,15 +41,15 @@
     Decorator used to annotate the observation functions.
 
     Parameters
     ----------
     observation_name : str, optional
         Name of the provided observation.
     observation_type : gym.spaces.Space, optional
-        Type of the provided value in OpenAI Gym format.
+        Type of the provided value in Gymnasium format.
 
     Returns
     -------
     Callable
         Function that returns the appropriate observation.
     """
 
@@ -66,15 +66,15 @@
     Decorator used to annotate the parameter functions.
 
     Parameters
     ----------
     parameter_name : str, optional
         Name of the provided parameter.
     parameter_type : gym.spaces.Space, optional
-        Type of the provided parameter in OpenAI Gym format.
+        Type of the provided parameter in Gymnasium format.
 
     Returns
     -------
     Callable
         Function that returns the appropriate parameter.
     """
 
@@ -171,14 +171,46 @@
     """
 
     return isinstance(a, gym.spaces.MultiDiscrete) and \
         np.array_equal(a.nvec, b.nvec) and \
         a.dtype == b.dtype
 
 
+def test_sequence(a: gym.spaces.Space, b: gym.spaces.Sequence) -> bool:
+    """
+    Tests if the space ``a`` is identical to the gym.space.Sequence space ``b``.
+
+    Parameters
+    ----------
+    a : gym.spaces.Space
+        Space ``a``.
+    b : gym.spaces.Sequence
+        Sequence space ``b``.
+
+    Returns
+    -------
+    bool
+        Result of the comparison.
+    """
+
+    if not isinstance(a, gym.spaces.Sequence):
+        return False
+
+    if isinstance(b, gym.spaces.Box):
+        return test_box(a, b)
+    elif isinstance(b, gym.spaces.Discrete):
+        return test_discrete(a, b)
+    elif isinstance(b, gym.spaces.MultiBinary):
+        return test_multi_binary(a, b)
+    elif isinstance(b, gym.spaces.MultiDiscrete):
+        return test_multi_discrete(a, b)
+    else:
+        return test_space(a, b)
+
+
 def test_space(a: gym.spaces.Space, b: gym.spaces.Space) -> bool:
     """
     Tests if the space ``a`` is identical to the space ``b``.
 
     Parameters
     ----------
     a : gym.spaces.Space
```

### Comparing `reinforced-lib-0.2.0/reinforced_lib/logs/base_logger.py` & `reinforced-lib-1.0.0/reinforced_lib/logs/base_logger.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,113 +1,121 @@
 from abc import ABC
 from enum import Enum
-from typing import Any, Dict, List, Tuple, Union
+from typing import Union
 
 from chex import Array, Scalar
 
 from reinforced_lib.utils.exceptions import UnsupportedLogTypeError
 
 
 class SourceType(Enum):
     OBSERVATION = 0
     STATE = 1
     METRIC = 2
 
 
-Source = Union[Tuple[str, SourceType], str]
+Source = Union[tuple[str, SourceType], str, None]
 
 
 class BaseLogger(ABC):
     """
-    Container for functions of a logger. Provides simple interface for defining custom loggers.
+    Base interface for loggers.
     """
 
     def __init__(self, **kwargs):
         pass
 
-    def init(self, sources: List[Source]) -> None:
+    def init(self, sources: list[Source]) -> None:
         """
-        Initializes the logger given the list of all sources.
+        Initializes the logger given the list of all sources defined by the user.
 
         Parameters
         ----------
         sources : list[Source]
             List containing the sources to log.
         """
 
         pass
 
     def finish(self) -> None:
         """
-        Finalizes the loggers work, for example, saves data or shows plots.
+        Finalizes the loggers work (e.g., closes file or shows plots).
         """
 
         pass
 
-    def log_scalar(self, source: Source, value: Scalar) -> None:
+    def log_scalar(self, source: Source, value: Scalar, custom: bool) -> None:
         """
         Method of the logger interface used for logging scalar values.
 
         Parameters
         ----------
         source : Source
             Source of the logged value.
         value : float
             Scalar to log.
+        custom : bool
+            Whether the source is a custom source.
         """
 
         raise UnsupportedLogTypeError(type(self), type(value))
 
-    def log_array(self, source: Source, value: Array) -> None:
+    def log_array(self, source: Source, value: Array, custom: bool) -> None:
         """
-        Method of the logger interface used for logging arrays.
+        Method of the logger interface used for logging one-dimensional arrays.
 
         Parameters
         ----------
         source : Source
             Source of the logged value.
         value : array_like
             Array to log.
+        custom : bool
+            Whether the source is a custom source.
         """
 
         raise UnsupportedLogTypeError(type(self), type(value))
 
-    def log_dict(self, source: Source, value: Dict) -> None:
+    def log_dict(self, source: Source, value: dict, custom: bool) -> None:
         """
         Method of the logger interface used for logging dictionaries.
 
         Parameters
         ----------
         source : Source
             Source of the logged value.
         value : dict
             Dictionary to log.
+        custom : bool
+            Whether the source is a custom source.
         """
 
         raise UnsupportedLogTypeError(type(self), type(value))
 
-    def log_other(self, source: Source, value: Any) -> None:
+    def log_other(self, source: Source, value: any, custom: bool) -> None:
         """
         Method of the logger interface used for logging other values.
 
         Parameters
         ----------
         source : Source
             Source of the logged value.
         value : any
             Value of any type to log.
+        custom : bool
+            Whether the source is a custom source.
         """
 
         raise UnsupportedLogTypeError(type(self), type(value))
 
     @staticmethod
     def source_to_name(source: Source) -> str:
         """
-        Converts a source to the string. If source is a string itself, it returns that string.
-        Otherwise, it returns string in the format "name-sourcetype" (e.g., "action-metric").
+        Returns a full name of the source. If source is a string itself, returns that string.
+        Otherwise, it returns a string in the format "name-sourcetype" (e.g., "action-metric").
 
         Parameters
         ----------
         source : Source
             Source of the logged value.
 
         Returns
```

### Comparing `reinforced-lib-0.2.0/reinforced_lib/logs/csv_logger.py` & `reinforced-lib-1.0.0/reinforced_lib/logs/tb_logger.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,137 +1,146 @@
 import json
-import os.path
-from datetime import datetime
-from typing import Any, Dict, List
+from collections import defaultdict
 
-import jax.numpy as jnp
-import numpy as np
 from chex import Array, Scalar
+from tensorboardX import SummaryWriter
 
 from reinforced_lib.logs import BaseLogger, Source
 
 
-class CsvLogger(BaseLogger):
+class TensorboardLogger(BaseLogger):
     """
-    Logger that saves values in CSV [1]_ format.
+    Logger that saves values in TensorBoard [2]_ format. Offers a possibility to log to Comet [3]_.
+    ``TensorboardLogger`` synchronizes the logged values in time. This means that if the same source
+    is logged less often than other sources, the step will be increased accordingly to maintain the
+    appropriate spacing between the values on the x-axis.
 
     Parameters
     ----------
-    csv_path : str, default="~/rlib-logs-[date]-[time].csv"
-        Path to the output file.
+    tb_log_dir : str, optional
+        Path to the output directory. If None, the default directory is used.
+    tb_comet_config : dict, optional
+        Configuration for the Comet logger. If None, the logger is disabled.
+    tb_sync_steps : bool, default=False
+        Set to ``True`` if you want to synchronize the logged values in time.
 
     References
     ----------
-    .. [1] Shafranovich, Y. (2005). Common Format and MIME Type for Comma-Separated Values (CSV) Files
-       (RFC No. 4180). RFC Editor. https://www.rfc-editor.org/rfc/rfc4180.txt
+    .. [2] TensorBoard. https://www.tensorflow.org/tensorboard
+    .. [3] Comet. https://www.comet.ml
     """
 
-    def __init__(self, csv_path: str = None, **kwargs) -> None:
+    def __init__(
+            self,
+            tb_log_dir: str = None,
+            tb_comet_config: dict[str, any] = None,
+            tb_sync_steps: bool = False,
+            **kwargs,
+    ) -> None:
         super().__init__(**kwargs)
 
-        if csv_path is None:
-            now = datetime.now()
-            csv_path = f'rlib-logs-{now.strftime("%Y%m%d")}-{now.strftime("%H%M%S")}.csv'
-            csv_path = os.path.join(os.path.expanduser("~"), csv_path)
+        if tb_comet_config is None:
+            tb_comet_config = {'disabled': True}
 
-        self._file = open(csv_path, 'w')
+        self._sync_steps = tb_sync_steps
+        self._current_values = set()
+        self._step = 0
 
-        self._columns_values = {}
-        self._columns_names = []
-
-    def init(self, sources: List[Source]) -> None:
-        """
-        Creates a list of all source names and writes the header to the output file.
-
-        Parameters
-        ----------
-        sources : list[Source]
-            List containing all sources to log.
-        """
-
-        self._columns_names = list(map(self.source_to_name, sources))
-        header = ','.join(self._columns_names)
-        self._file.write(f'{header}\n')
+        self._writer = SummaryWriter(log_dir=tb_log_dir, comet_config=tb_comet_config)
+        self._steps = defaultdict(int)
 
     def finish(self) -> None:
         """
-        Closes the output file.
+        Closes the summary writer.
         """
 
-        self._file.close()
+        self._writer.close()
 
-    def log_scalar(self, source: Source, value: Scalar) -> None:
+    def log_scalar(self, source: Source, value: Scalar, *_) -> None:
         """
-        Logs a scalar as a standard value in a column.
+        Adds a given scalar to the summary writer.
 
         Parameters
         ----------
         source : Source
             Source of the logged value.
         value : float
             Scalar to log.
         """
 
-        self._columns_values[self.source_to_name(source)] = value
-        self._save()
+        name = self.source_to_name(source)
+        step = self._get_step(name)
+        self._writer.add_scalar(name, value, step)
 
-    def log_array(self, source: Source, value: Array) -> None:
+    def log_array(self, source: Source, value: Array, *_) -> None:
         """
-        Logs an array as a JSON [2]_ string.
+        Adds a given array to the summary writer as a histogram.
 
         Parameters
         ----------
         source : Source
             Source of the logged value.
         value : array_like
             Array to log.
         """
 
-        if isinstance(value, (np.ndarray, jnp.ndarray)):
-            value = value.tolist()
+        name = self.source_to_name(source)
+        step = self._get_step(name)
+        self._writer.add_histogram(name, value, step)
 
-        self.log_other(source, value)
-
-    def log_dict(self, source: Source, value: Dict) -> None:
+    def log_dict(self, source: Source, value: dict, *_) -> None:
         """
-        Logs a dictionary as a JSON [2]_ string.
+        Logs a dictionary as a JSON string.
 
         Parameters
         ----------
         source : Source
             Source of the logged value.
         value : dict
             Dictionary to log.
         """
 
-        self.log_other(source, value)
+        self.log_other(source, value, None)
 
-    def log_other(self, source: Source, value: Any) -> None:
+    def log_other(self, source: Source, value: any, *_) -> None:
         """
-        Logs an object as a JSON [2]_ string.
+        Logs an object as a JSON string.
 
         Parameters
         ----------
         source : Source
             Source of the logged value.
-        value : any
-            Value of any type to log.
-
-        References
-        ----------
-        .. [2] Pezoa, F., Reutter, J. L., Suarez, F., Ugarte, Mart&#237;n, & Vrgo&#269;c, Domagoj. (2016).
-           Foundations of JSON schema. In Proceedings of the 25th International Conference on World Wide Web
-           (pp. 263–273).
+        value : dict
+            Dictionary to log.
         """
 
-        self._columns_values[self.source_to_name(source)] = f"\"{json.dumps(value)}\""
-        self._save()
+        name = self.source_to_name(source)
+        step = self._get_step(name)
+        self._writer.add_text(name, json.dumps(value), step)
 
-    def _save(self) -> None:
-        """
-        Writes a new row to the output file if the values for all columns has already been filled.
+    def _get_step(self, name: str) -> int:
         """
+        Returns the current step for a given source.
+
+        Parameters
+        ----------
+        name : str
+            Name of the source.
+
+        Returns
+        -------
+        int
+            Current step for the given source.
+        """
+
+        if self._sync_steps:
+            if name in self._current_values:
+                self._step += 1
+                self._current_values.clear()
+
+            self._current_values.add(name)
+            step = self._step
+        else:
+            step = self._steps[name] + 1
 
-        if len(self._columns_values) == len(self._columns_names):
-            line = ','.join(str(self._columns_values[name]) for name in self._columns_names)
-            self._file.write(f'{line}\n')
-            self._columns_values = {}
+        self._steps[name] = step
+        return step
```

#### encoding

```diff
@@ -1 +1 @@
-utf-8
+us-ascii
```

### Comparing `reinforced-lib-0.2.0/reinforced_lib/logs/logs_observer.py` & `reinforced-lib-1.0.0/reinforced_lib/logs/logs_observer.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,32 +1,32 @@
 from collections import defaultdict
-from typing import Any, Callable, Dict, List
-
-import jax.numpy as jnp
+from typing import Callable
 
 from reinforced_lib.agents import BaseAgent
 from reinforced_lib.logs import BaseLogger, Source, SourceType
 from reinforced_lib.utils.exceptions import IncorrectLoggerTypeError, IncorrectSourceTypeError
+from reinforced_lib.utils import is_scalar, is_array, is_dict
 
 
 class LogsObserver:
     """
-    Class responsible for managing a singleton instances of the loggers, initialization and finalization
-    of the loggers, and passing the logged values to the appropriate loggers and methods.
+    Class responsible for managing singleton instances of the loggers, initialization and finalization
+    of the loggers, and passing the logged values to the appropriate loggers and their methods.
     """
 
     def __init__(self) -> None:
-        self._loggers_instances = {}
-        self._loggers_sources = defaultdict(list)
+        self._logger_instances = {}
+        self._logger_sources = defaultdict(list)
 
         self._observations_loggers = defaultdict(list)
         self._agent_state_loggers = defaultdict(list)
         self._metrics_loggers = defaultdict(list)
+        self._custom_loggers = defaultdict(list)
 
-    def add_logger(self, source: Source, logger_type: type, logger_params: Dict[str, Any]) -> None:
+    def add_logger(self, source: Source, logger_type: type, logger_params: dict[str, any]) -> None:
         """
         Initializes a singleton instance of the logger and connects a given source with that logger.
 
         Parameters
         ----------
         source : Source
             Source to connect.
@@ -38,51 +38,53 @@
 
         if not issubclass(logger_type, BaseLogger):
             raise IncorrectLoggerTypeError(logger_type)
 
         if isinstance(source, tuple):
             if len(source) != 2 or not isinstance(source[0], str) or not hasattr(source[1], 'name'):
                 raise IncorrectSourceTypeError(type(source))
-        elif not isinstance(source, str):
+        elif source is not None and not isinstance(source, str):
             raise IncorrectSourceTypeError(type(source))
 
-        logger = self._loggers_instances.get(logger_type, logger_type(**logger_params))
+        logger = self._logger_instances.get(logger_type, logger_type(**logger_params))
 
         if isinstance(source, tuple):
             if source[1] == SourceType.OBSERVATION:
                 self._observations_loggers[logger].append((source, source[0]))
             elif source[1] == SourceType.STATE:
                 self._agent_state_loggers[logger].append((source, source[0]))
             elif source[1] == SourceType.METRIC:
                 self._metrics_loggers[logger].append((source, source[0]))
         elif isinstance(source, str):
             self._observations_loggers[logger].append((source, source))
             self._agent_state_loggers[logger].append((source, source))
             self._metrics_loggers[logger].append((source, source))
+        elif source is None:
+            self._custom_loggers[logger] = [(None, None)]
 
-        self._loggers_sources[logger].append(source)
-        self._loggers_instances[logger_type] = logger
+        self._logger_sources[logger].append(source)
+        self._logger_instances[logger_type] = logger
 
     def init_loggers(self):
         """
         Initializes all loggers by calling their ``init`` method.
         """
 
-        for logger, sources in self._loggers_sources.items():
+        for logger, sources in self._logger_sources.items():
             logger.init(sources)
 
     def finish_loggers(self):
         """
         Finalizes the work of all loggers by calling their ``finish`` method.
         """
 
-        for logger in self._loggers_sources.keys():
+        for logger in self._logger_sources.keys():
             logger.finish()
 
-    def update_observations(self, observations: Any) -> None:
+    def update_observations(self, observations: any) -> None:
         """
         Passes new observations to the loggers.
 
         Parameters
         ----------
         observations : dicy or any
             Observations received by the agent.
@@ -101,45 +103,64 @@
         ----------
         agent_state : BaseAgent
             Current agent state.
         """
 
         self._update(self._agent_state_loggers, lambda name: getattr(agent_state, name, None))
 
-    def update_metrics(self, metric: Any, metric_name: str) -> None:
+    def update_metrics(self, metric: any, metric_name: str) -> None:
         """
         Passes metrics to loggers.
 
         Parameters
         ----------
         metric : any
             Metric value.
         metric_name : str
             Name of the metric.
         """
 
         self._update(self._metrics_loggers, lambda name: metric if name == metric_name else None)
 
+    def update_custom(self, value: any, name: str) -> None:
+        """
+        Passes values provided by the user to the loggers.
+
+        Parameters
+        ----------
+        value : any
+            Value to log.
+        name : str
+            Name of the value.
+        """
+
+        self._update(self._custom_loggers, lambda _: (name, value))
+
     @staticmethod
-    def _update(loggers: Dict[BaseLogger, List[str]], get_value: Callable) -> None:
+    def _update(loggers: dict[BaseLogger, list[Source]], get_value: Callable) -> None:
         """
         Passes values to the appropriate loggers and method based on the type and the source of the value.
 
         Parameters
         ----------
         loggers : dict
             Dictionary with the loggers instances and the connected sources.
         get_value : callable
             Function that gets the selected value from the observations, state, or metrics.
         """
 
         for logger, sources in loggers.items():
             for source, name in sources:
                 if (value := get_value(name)) is not None:
-                    if jnp.isscalar(value) or (hasattr(value, 'ndim') and value.ndim == 0):
-                        logger.log_scalar(source, value)
-                    elif isinstance(value, dict):
-                        logger.log_dict(source, value)
-                    elif isinstance(value, (list, tuple)) or (hasattr(value, 'ndim') and value.ndim == 1):
-                        logger.log_array(source, value)
+                    if name is None:
+                        source, value = value
+
+                    custom = name is None
+
+                    if is_scalar(value):
+                        logger.log_scalar(source, value, custom)
+                    elif is_dict(value):
+                        logger.log_dict(source, value, custom)
+                    elif is_array(value):
+                        logger.log_array(source, value, custom)
                     else:
-                        logger.log_other(source, value)
+                        logger.log_other(source, value, custom)
```

### Comparing `reinforced-lib-0.2.0/reinforced_lib/logs/plots_logger.py` & `reinforced-lib-1.0.0/reinforced_lib/logs/plots_logger.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,164 +1,166 @@
 import os.path
 from collections import defaultdict
-from datetime import datetime
-from typing import List
 
 import jax.numpy as jnp
 import matplotlib.pyplot as plt
-from chex import Array, Scalar
+from chex import Array, Scalar, Numeric
 
 from reinforced_lib.logs import BaseLogger, Source
+from reinforced_lib.utils import timestamp
 
 
 class PlotsLogger(BaseLogger):
     r"""
-    Logger that presents and saves values as a line plots. Offers smoothing of the curve and plotting
-    multiple curves in a single chart (while logging arrays).
+    Logger that presents and saves values as matplotlib plots. Offers smoothing of the curve, scatter plots, and
+    multiple curves in a single chart (while logging arrays). ``PlotsLogger`` is able to synchronizes the logged
+    values in time. This means that if the same source is logged less often than other sources, the step will be
+    increased accordingly to maintain the appropriate spacing between the values on the x-axis.
 
     Parameters
     ----------
     plots_dir : str, default="~"
         Output directory for the plots.
     plots_ext : str, default="svg"
         Extension of the saved plots.
     plots_smoothing : float, default=0.6
-        Weight of the exponential moving average (EMA/EWMA) [3]_ used for smoothing. :math:`\alpha \in [0, 1)`.
+        Weight of the exponential moving average (EMA/EWMA) [1]_ used for smoothing. :math:`\alpha \in [0, 1)`.
     plots_scatter : bool, default=False
         Set to ``True`` if you want to generate a scatter plot instead of a line plot.
         ``plots_smoothing`` parameter does not apply to the scatter plots.
+    plots_sync_steps : bool, default=False
+        Set to ``True`` if you want to synchronize the logged values in time.
 
     References
     ----------
-    .. [3] https://en.wikipedia.org/wiki/Moving_average#Exponential_moving_average
+    .. [1] https://en.wikipedia.org/wiki/Moving_average#Exponential_moving_average
     """
 
     def __init__(
-        self,
-        plots_dir: str = None,
-        plots_ext: str = 'svg',
-        plots_smoothing: Scalar = 0.6,
-        plots_scatter: bool = False,
-        **kwargs
+            self,
+            plots_dir: str = None,
+            plots_ext: str = 'pdf',
+            plots_smoothing: Scalar = 0.6,
+            plots_scatter: bool = False,
+            plots_sync_steps: bool = False,
+            **kwargs
     ) -> None:
-        super().__init__(**kwargs)
-
-        self._plots_dir = plots_dir if plots_dir else os.path.expanduser("~")
-        self._plots_ext = plots_ext
-        self._plots_smoothing = plots_smoothing
-        self._plots_scatter = plots_scatter
+        assert 1 > plots_smoothing >= 0
 
-        assert 1 > self._plots_smoothing >= 0
-
-        self._plots_values = defaultdict(list)
-        self._plots_names = []
+        super().__init__(**kwargs)
 
-    def init(self, sources: List[Source]) -> None:
-        """
-        Creates a list of all sources names.
+        self._dir = plots_dir if plots_dir else os.path.expanduser("~")
+        self._ext = plots_ext
+        self._smoothing = plots_smoothing
+        self._scatter = plots_scatter
+        self._sync_steps = plots_sync_steps
 
-        Parameters
-        ----------
-        sources : list[Source]
-            List containing all sources to log.
-        """
+        self._current_values = set()
+        self._step = 0
 
-        self._plots_names = list(map(self.source_to_name, sources))
+        self._values = defaultdict(list)
+        self._steps = defaultdict(list)
 
     def finish(self) -> None:
         """
         Shows the generated plots and saves them to the output directory with the specified extension
         (the names of the files follow the pattern ``"rlib-plot-[source]-[date]-[time].[ext]"``).
         """
 
-        def lineplot(values: List, alpha: Scalar = 1.0, label: bool = False) -> None:
+        def exponential_moving_average(values: list, weight: Scalar) -> list:
+            smoothed = [values[0]]
+
+            for value in values[1:]:
+                smoothed.append((1 - weight) * value + weight * smoothed[-1])
+
+            return smoothed
+
+        def lineplot(values: list, steps: list, alpha: Scalar = 1.0, label: bool = False) -> None:
             values = jnp.array(values)
             values = jnp.squeeze(values)
 
             if values.ndim == 1:
-                plt.plot(values, alpha=alpha, c='C0')
+                plt.plot(steps, values, alpha=alpha, c='C0')
             elif values.ndim == 2:
                 for i, val in enumerate(jnp.array(values).T):
-                    plt.plot(val, alpha=alpha, c=f'C{i % 10}', label=i if label else '')
+                    plt.plot(steps, val, alpha=alpha, c=f'C{i % 10}', label=i if label else '')
                 plt.legend()
         
-        def scatterplot(values: List, label: bool = False) -> None:
-            values = jnp.array(values)
-            values = jnp.squeeze(values)
-            xs = range(1, len(values) + 1)
+        def scatterplot(values: list, steps: list, label: bool = False) -> None:
+            values = jnp.array(values).squeeze()
 
             if values.ndim == 1:
-                plt.scatter(xs, values, c='C0', marker='.', s=4)
+                plt.scatter(steps, values, c='C0', marker='.', s=4)
             elif values.ndim == 2:
                 for i, val in enumerate(jnp.array(values).T):
-                    plt.scatter(xs, val, c=f'C{i % 10}', label=i if label else '', marker='.', s=4)
+                    plt.scatter(steps, val, c=f'C{i % 10}', label=i if label else '', marker='.', s=4)
                 plt.legend()
 
-        now = datetime.now()
-
-        for name, values in self._plots_values.items():
-            filename = f'rlib-plot-{name}-{now.strftime("%Y%m%d")}-{now.strftime("%H%M%S")}.{self._plots_ext}'
+        for name, values in self._values.items():
+            filename = f'rlib-plot-{name}-{timestamp()}.{self._ext}'
 
-            if self._plots_scatter:
-                scatterplot(values, True)
+            if self._scatter:
+                scatterplot(values, self._steps[name], True)
             else:
-                smoothed = self._exponential_moving_average(values, self._plots_smoothing)
-                lineplot(values, alpha=0.3)
-                lineplot(smoothed, label=True)
+                smoothed = exponential_moving_average(values, self._smoothing)
+                lineplot(values, self._steps[name], alpha=0.3)
+                lineplot(smoothed, self._steps[name], label=True)
             
             plt.title(name)
             plt.xlabel('step')
-            plt.savefig(os.path.join(self._plots_dir, filename), bbox_inches='tight')
+            plt.savefig(os.path.join(self._dir, filename), bbox_inches='tight', dpi=300)
             plt.show()
 
-    @staticmethod
-    def _exponential_moving_average(values: List, weight: Scalar) -> List:
+    def log_scalar(self, source: Source, value: Scalar, *_) -> None:
         """
-        Calculates the exponential moving average (EMA/EWMA) [3]_ to smooth the plotted values.
+        Adds a given scalar to the plot values.
 
         Parameters
         ----------
-        values : array_like
-            Original values.
-        weight : float
-            Weight of the EMA.
-
-        Returns
-        -------
-        smoothed : array_like
-            Smoothed values.
+        source : Source
+            Source of the logged value.
+        value : float
+            Scalar to log.
         """
 
-        smoothed = [values[0]]
+        self._log(source, value)
 
-        for value in values[1:]:
-            smoothed.append((1 - weight) * value + weight * smoothed[-1])
-
-        return smoothed
-
-    def log_scalar(self, source: Source, value: Scalar) -> None:
+    def log_array(self, source: Source, value: Array, *_) -> None:
         """
-        Adds a given scalar to the plots values.
+        Adds a given array to the plot values.
 
         Parameters
         ----------
         source : Source
             Source of the logged value.
-        value : float
-            Scalar to log.
+        value : array_like
+            Array to log.
         """
 
-        self._plots_values[self.source_to_name(source)].append(value)
+        self._log(source, value)
 
-    def log_array(self, source: Source, value: Array) -> None:
+    def _log(self, source: Source, value: Numeric) -> None:
         """
-        Adds a given array to the plots values.
+        Adds a given scalar to the plot values.
 
         Parameters
         ----------
         source : Source
             Source of the logged value.
-        value : array_like
-            Array to log.
+        value : Numeric
+            Value to log.
         """
 
-        self._plots_values[self.source_to_name(source)].append(value)
+        name = self.source_to_name(source)
+
+        if self._sync_steps:
+            if name in self._current_values:
+                self._step += 1
+                self._current_values.clear()
+
+            self._current_values.add(name)
+            step = self._step
+        else:
+            step = self._steps[name][-1] + 1 if self._steps[name] else 0
+
+        self._values[name].append(value)
+        self._steps[name].append(step)
```

### Comparing `reinforced-lib-0.2.0/reinforced_lib/rlib.py` & `reinforced-lib-1.0.0/reinforced_lib/rlib.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,22 +1,48 @@
 from __future__ import annotations
-from typing import Any, Dict, List, Tuple, Union
 
 import os
-import gym
 import pickle
-import datetime
-import lz4.frame
+from typing import Union
+
+import cloudpickle
+import gymnasium as gym
 import jax.random
+import lz4.frame
+from chex import dataclass
 
 from reinforced_lib.agents import BaseAgent
 from reinforced_lib.exts import BaseExt
 from reinforced_lib.logs import Source
 from reinforced_lib.logs.logs_observer import LogsObserver
 from reinforced_lib.utils.exceptions import *
+from reinforced_lib.utils import is_scalar, timestamp
+
+
+@dataclass
+class AgentContainer:
+    """
+    Class containing the state of a given agent and all its dependencies.
+
+    Attributes
+    ----------
+    state : BaseAgent
+        Current state of the agent.
+    key : jax.random.PRNGKey
+        A PRNG key used as the random key.
+    action : any
+        Action selected by the agent.
+    step : int
+        Current step of the agent.
+    """
+
+    state: BaseAgent
+    key: jax.random.PRNGKey
+    action: any
+    step: int
 
 
 class RLib:
     """
     Main class of the library. Exposes a simple and intuitive interface to use the library.
 
     Parameters
@@ -25,190 +51,201 @@
         Type of the selected agent. Must inherit from the ``BaseAgent`` class.
     agent_params : dict, optional
         Parameters of the selected agent.
     ext_type : type, optional
         Type of the selected extension. Must inherit from the ``BaseExt`` class.
     ext_params : dict, optional
         Parameters of the selected extension.
-    loggers_type : type or list[type], optional
+    logger_types : type or list[type], optional
         Types of the selected logging modules. Must inherit from the ``BaseLogger`` class.
-    loggers_sources : Source or list[Source], optional
+    logger_sources : Source or list[Source], optional
         Sources to log.
-    loggers_params : dict, optional
+    logger_params : dict, optional
         Parameters of the selected loggers.
     no_ext_mode : bool, default=False
         Pass observations directly to the agent (do not use the extensions).
-    save_directory : str, default=None
-        Path to a user specified directory where the ``save`` method will store the experiment checkpoints.
-        If none specified, utilizes the home directory.
+    auto_checkpoint : int, optional
+        Automatically save the experiment every ``auto_checkpoint`` steps.
+        If ``None``, the automatic checkpointing is disabled.
+    auto_checkpoint_path : str, optional, default=~
+        Path to the directory where the automatic checkpoints will be saved.
     """
 
     def __init__(
             self, *,
             agent_type: type = None,
-            agent_params: Dict[str, Any] = None,
+            agent_params: dict[str, any] = None,
             ext_type: type = None,
-            ext_params: Dict[str, Any] = None,
-            loggers_type: Union[type, List[type]] = None,
-            loggers_sources: Union[Source, List[Source]] = None,
-            loggers_params: Dict[str, Any] = None,
+            ext_params: dict[str, any] = None,
+            logger_types: Union[type, list[type]] = None,
+            logger_sources: Union[Source, list[Source]] = None,
+            logger_params: dict[str, any] = None,
             no_ext_mode: bool = False,
-            save_directory: str = None
+            auto_checkpoint: int = None,
+            auto_checkpoint_path: str = None
     ) -> None:
         self._lz4_ext = ".pkl.lz4"
-        self._save_directory = save_directory if save_directory else os.path.expanduser("~")
+        self._default_path = os.path.expanduser("~")
+        self._auto_checkpoint = auto_checkpoint
+        self._auto_checkpoint_path = auto_checkpoint_path if auto_checkpoint_path else self._default_path
 
         self._agent = None
         self._agent_type = agent_type
         self._agent_params = agent_params
-        self._agents_states = []
-        self._agents_keys = []
+        self._agent_containers = []
 
         self._ext = None
         self._no_ext_mode = no_ext_mode
         self._ext_type = ext_type
         self._ext_params = ext_params
 
-        self._loggers_type = loggers_type
-        self._loggers_sources = loggers_sources
-        self._loggers_params = loggers_params
+        self._logger_types = logger_types
+        self._logger_sources = logger_sources
+        self._logger_params = logger_params
         self._logs_observer = LogsObserver()
         self._init_loggers = True
         self._cumulative_reward = 0.0
 
         if ext_type:
             self.set_ext(ext_type, ext_params)
 
         if agent_type:
             self.set_agent(agent_type, agent_params)
 
-        if loggers_type and loggers_sources:
-            self.set_loggers(loggers_type, loggers_sources, loggers_params)
+        if logger_types:
+            self.set_loggers(logger_types, logger_sources, logger_params)
 
     def __del__(self) -> None:
         """
         Automatically finalizes the library work.
         """
 
         self.finish()
 
     def finish(self) -> None:
         """
-        Used to explicitly finalize the library work. In particular, it finishes the loggers work.
+        Used to explicitly finalize the library's work. In particular, it finishes the logger's work.
         """
 
         self._logs_observer.finish_loggers()
 
-    def set_agent(self, agent_type: type, agent_params: Dict = None) -> None:
+    def set_agent(self, agent_type: type, agent_params: dict = None) -> None:
         """
         Initializes an agent of type ``agent_type`` with parameters ``agent_params``. The agent type must inherit from
-        the ``BaseAgent class``. The agent type cannot be changed after the first agent instance has been initialized.
+        the ``BaseAgent`` class. The agent type cannot be changed after the first agent instance has been initialized.
 
         Parameters
         ----------
         agent_type : type
             Type of the selected agent. Must inherit from the ``BaseAgent`` class.
         agent_params : dict, optional
             Parameters of the selected agent.
         """
 
-        if len(self._agents_states) > 0:
+        if len(self._agent_containers) > 0:
             raise ForbiddenAgentChangeError()
 
         if not issubclass(agent_type, BaseAgent):
             raise IncorrectAgentTypeError(agent_type)
 
         self._agent_type = agent_type
         self._agent_params = agent_params
 
         if not self._no_ext_mode and self._ext:
-            agent_params = self._ext.get_agent_params(agent_type, agent_type.parameters_space(), agent_params)
+            agent_params = self._ext.get_agent_params(agent_type, agent_type.parameter_space(), agent_params)
             self._agent = agent_type(**agent_params)
             self._ext.setup_transformations(self._agent.update_observation_space, self._agent.sample_observation_space)
         else:
             agent_params = agent_params if agent_params else {}
             self._agent = agent_type(**agent_params)
 
-    def set_ext(self, ext_type: type, ext_params: Dict = None) -> None:
+    def set_ext(self, ext_type: type, ext_params: dict = None) -> None:
         """
         Initializes an extension of type ``ext_type`` with parameters ``ext_params``. The extension type must inherit
         from the ``BaseExt`` class. The extension type cannot be changed after the first agent instance has been
         initialized.
 
         Parameters
         ----------
         ext_type : type
-            Type of selected the extension. Must inherit from the ``BaseExt`` class.
+            Type of selected extension. Must inherit from the ``BaseExt`` class.
         ext_params : dict, optional
             Parameters of the selected extension.
         """
 
         if self._no_ext_mode:
             raise ForbiddenExtensionSetError()
 
-        if len(self._agents_states) > 0:
+        if len(self._agent_containers) > 0:
             raise ForbiddenExtensionChangeError()
 
         if not issubclass(ext_type, BaseExt):
             raise IncorrectExtensionTypeError(ext_type)
 
+        self._ext_type = ext_type
+        self._ext_params = ext_params
+
         ext_params = ext_params if ext_params else {}
         self._ext = ext_type(**ext_params)
 
         if self._agent:
             agent_params = self._ext.get_agent_params(
                 self._agent_type,
-                self._agent_type.parameters_space(),
+                self._agent_type.parameter_space(),
                 self._agent_params
             )
             self._agent = self._agent_type(**agent_params)
             self._ext.setup_transformations(self._agent.update_observation_space, self._agent.sample_observation_space)
 
     def set_loggers(
             self,
-            loggers_types: Union[type, List[type]],
-            loggers_sources: Union[Source, List[Source]],
-            loggers_params: Dict[str, Any] = None
+            logger_types: Union[type, list[type]],
+            logger_sources: Union[Source, list[Source]] = None,
+            logger_params: dict[str, any] = None
     ) -> None:
         """
-        Initializes loggers that log observations from the environment, agents state, or training metrics.
-        ``loggers_types`` and ``loggers_sources`` arguments can be objects of the appropriate types or a lists
-        of objects. If the user passes two objects or lists of the same lengths, function initializes the modules
-        with the corresponding types and names. If the user passes one object (or list with only one object)
-        and a list with multiple objects, function broadcasts the passed objects. The ``loggers_sources`` items
-        can be names of the logger sources (e.g. "action") or tuples containing the name and the ``SourceType``
-        (e.g., ``("action", SourceType.OBSERVATION)``). If the name itself is inconclusive, behaviour depends
+        Initializes loggers of types ``logger_types`` with parameters ``logger_params``. The logger types must inherit
+        from the ``BaseLogger`` class. The logger types cannot be changed after the first agent instance has been
+        initialized. ``logger_types`` and ``logger_sources`` can be objects or lists of objects, the function broadcasts
+        them to the same length. The ``logger_sources`` parameter specifies the sources to log. A source can be None
+        (then the logger is used to log a custom values passed by the ``log`` method), a name of the sources (e.g.,
+        "action") or tuple containing the name and the ``SourceType`` (e.g., ``("action", SourceType.OBSERVATION)``).
+        If the name itself is inconclusive (e.g., it occurs as a metric and as an observation), the behaviour depends
         on the implementation of the logger.
 
         Parameters
         ----------
-        loggers_types : type or list[type]
+        logger_types : type or list[type]
             Types of the selected logging modules.
-        loggers_sources : Source or list[Source]
+        logger_sources : Source or list[Source], optional
             Sources to log.
-        loggers_params : dict, optional
+        logger_params : dict, optional
             Parameters of the selected logging modules.
         """
 
-        if len(self._agents_states) > 0:
+        if not self._init_loggers:
             raise ForbiddenLoggerSetError()
 
-        loggers_params = loggers_params if loggers_params else {}
-        loggers_types, loggers_sources = self._object_to_list(loggers_types), self._object_to_list(loggers_sources)
-        loggers_types, loggers_sources = self._broadcast(loggers_types, loggers_sources)
+        self._logger_types = logger_types
+        self._logger_sources = logger_sources
+        self._logger_params = logger_params
+
+        logger_params = logger_params if logger_params else {}
+        logger_types, logger_sources = self._object_to_list(logger_types), self._object_to_list(logger_sources)
+        logger_types, logger_sources = self._broadcast(logger_types, logger_sources)
 
-        for logger_type, source in zip(loggers_types, loggers_sources):
-            self._logs_observer.add_logger(source, logger_type, loggers_params)
+        for logger_type, source in zip(logger_types, logger_sources):
+            self._logs_observer.add_logger(source, logger_type, logger_params)
 
     @staticmethod
-    def _object_to_list(obj: Union[Any, List[Any]]) -> List[Any]:
+    def _object_to_list(obj: Union[any, list[any]]) -> list[any]:
         return obj if isinstance(obj, list) else [obj]
 
     @staticmethod
-    def _broadcast(list_a: List[Any], list_b: List[Any]) -> Tuple[List[Any], List[Any]]:
+    def _broadcast(list_a: list[any], list_b: list[any]) -> tuple[list[any], list[any]]:
         if len(list_a) == len(list_b):
             return list_a, list_b
 
         if len(list_a) == 1:
             return list_a * len(list_b), list_b
 
         if len(list_b) == 1:
@@ -268,50 +305,58 @@
 
         Returns
         -------
         int
             Identifier of the created instance.
         """
 
-        agent_id = len(self._agents_states)
+        agent_id = len(self._agent_containers)
         init_key, key = jax.random.split(jax.random.PRNGKey(seed))
 
-        self._agents_states.append(self._agent.init(init_key))
-        self._agents_keys.append(key)
+        self._agent_containers.append(AgentContainer(
+            state=self._agent.init(init_key),
+            key=key,
+            action=None,
+            step=0
+        ))
 
         return agent_id
 
     def sample(
             self,
-            agent_id: int = 0,
             *args,
-            update_observations: Union[Dict, Tuple, Any] = None,
-            sample_observations: Union[Dict, Tuple, Any] = None,
+            agent_id: int = 0,
+            is_training: bool = True,
+            update_observations: Union[dict, tuple, any] = None,
+            sample_observations: Union[dict, tuple, any] = None,
             **kwargs
-    ) -> Any:
+    ) -> any:
         """
         Takes the extension state as an input, updates the agent state, and returns the next action selected by
         the agent. If ``no_ext_mode`` is disabled, observations are passed by args and kwargs (the observations must
         match the extension observation space). If ``no_ext_mode`` is enabled, observations must be passed
-        by the ``update_observations`` and ``sample_observations`` parameters (the observations must match agents
-        ``update_observation_space`` and ``sample_observation_space``). If there are no agent instance initialized,
-        the method automatically initializes the first instance.
+        by the ``update_observations`` and ``sample_observations`` parameters (the observations must match the agent's
+        ``update_observation_space`` and ``sample_observation_space``). If there are no agent instances initialized,
+        the method automatically initializes the first instance. If the ``is_training`` flag is set, the ``update`` and
+        ``sample`` agent methods will be called. Otherwise, only the ``sample`` method will be called.
 
         Parameters
         ----------
+        *args : tuple
+            Environment observations.
         agent_id : int, default=0
             The identifier of the agent instance.
-        *args : tuple
-            Extension observations.
+        is_training : bool
+            Flag indicating whether the agent state should be updated in this step.
         update_observations : dict or tuple or any, optional
-            Observations used when ``no_ext_mode`` is enabled (must match agents ``update_observation_space``).
+            Observations used when ``no_ext_mode`` is enabled (must match agent's ``update_observation_space``).
         sample_observations : dict or tuple or any, optional
-            Observations used when ``no_ext_mode`` is enabled (must match agents ``sample_observation_space``).
+            Observations used when ``no_ext_mode`` is enabled (must match agent's ``sample_observation_space``).
         **kwargs : dict
-            Extension observations.
+            Environment observations.
 
         Returns
         -------
         any
             Action selected by the agent.
         """
 
@@ -324,45 +369,52 @@
         update_observations = update_observations if update_observations else {}
         sample_observations = sample_observations if sample_observations else {}
 
         if self._init_loggers:
             self._logs_observer.init_loggers()
             self._init_loggers = False
 
-        if len(self._agents_states) == 0:
+        if len(self._agent_containers) == 0:
             self.init()
 
-        key, update_key, sample_key = jax.random.split(self._agents_keys[agent_id], 3)
-        state = self._agents_states[agent_id]
+        key, update_key, sample_key = jax.random.split(self._agent_containers[agent_id].key, 3)
+        state = self._agent_containers[agent_id].state
+        action = self._agent_containers[agent_id].action
+        step = self._agent_containers[agent_id].step
 
         if not self._no_ext_mode:
-            update_observations, sample_observations = self._ext.transform(*args, **kwargs)
+            update_observations, sample_observations = self._ext.transform(*args, action=action, **kwargs)
 
         all_observations = kwargs
         if isinstance(update_observations, dict) and isinstance(sample_observations, dict):
-            all_observations.update(update_observations)
-            all_observations.update(sample_observations)
+            all_observations |= update_observations
+            all_observations |= sample_observations
             self._logs_observer.update_observations(all_observations)
         else:
             self._logs_observer.update_observations(update_observations)
             self._logs_observer.update_observations(sample_observations)
 
-        if isinstance(update_observations, dict):
-            state = self._agent.update(state, update_key, **update_observations)
-        elif isinstance(update_observations, tuple):
-            state = self._agent.update(state, update_key, *update_observations)
-        else:
-            state = self._agent.update(state, update_key, update_observations)
+        if is_training and step > 0:
+            if isinstance(update_observations, dict):
+                state = self._agent.update(state, update_key, **update_observations)
+            elif isinstance(update_observations, tuple):
+                state = self._agent.update(state, update_key, *update_observations)
+            else:
+                state = self._agent.update(state, update_key, update_observations)
+
+            if self._auto_checkpoint is not None and (step + 1) % self._auto_checkpoint == 0:
+                checkpoint_path = os.path.join(self._auto_checkpoint_path, f'rlib-checkpoint-agent-{agent_id}-step-{step + 1}')
+                self.save(checkpoint_path, agent_ids=agent_id)
 
         if isinstance(sample_observations, dict):
-            state, action = self._agent.sample(state, sample_key, **sample_observations)
+            action = self._agent.sample(state, sample_key, **sample_observations)
         elif isinstance(sample_observations, tuple):
-            state, action = self._agent.sample(state, sample_key, *sample_observations)
+            action = self._agent.sample(state, sample_key, *sample_observations)
         else:
-            state, action = self._agent.sample(state, sample_key, sample_observations)
+            action = self._agent.sample(state, sample_key, sample_observations)
 
         self._logs_observer.update_agent_state(state)
         self._logs_observer.update_metrics(action, 'action')
 
         def log_reward(reward: float) -> None:
             self._cumulative_reward += reward
             self._logs_observer.update_metrics(reward, 'reward')
@@ -375,109 +427,209 @@
                 if hasattr(self._ext, 'reward'):
                     log_reward(self._ext.reward(**all_observations))
                 elif 'reward' in self._ext._observation_functions:
                     log_reward(self._ext._observation_functions['reward'](**all_observations))
             except TypeError:
                 pass
 
-        self._agents_states[agent_id] = state
-        self._agents_keys[agent_id] = key
+        self._agent_containers[agent_id] = AgentContainer(
+            state=state,
+            key=key,
+            action=action,
+            step=step + 1
+        )
 
         return action
 
-    def save(self, path: str = None) -> str:
+    def save(self, path: str = None, *, agent_ids: Union[int, list[int]] = None) -> str:
         """
-        Saves the state of the experiment to a file in lz4 format. For each agent both the state and the initialization
+        Saves the state of the experiment to a file in lz4 format. For each agent, both the state and the initialization
         parameters are saved. The extension and loggers settings are saved as well to fully reconstruct the experiment.
 
         Parameters
         ----------
         path : str, optional
-            Path to the checkpoint file. If none specified, saves to the path specified by ``save_directory``.
-            If ``.pkl.lz4`` suffix is not detected, it will be appended automatically.
+            Path to the checkpoint file. If none specified, saves to the default path.
+            If the ``.pkl.lz4`` suffix is not detected, it will be appended automatically.
+        agent_ids : int or array_like, optional
+            The identifier of the agent instance(s) to save. If none specified, saves the state of all agents.
         
         Returns
         -------
         str
             Path to the saved checkpoint file.
         """
 
+        if agent_ids is None:
+            agent_ids = list(range(len(self._agent_containers)))
+        elif is_scalar(agent_ids):
+            agent_ids = [agent_ids]
+
+        agent_containers = [self._agent_containers[agent_id] for agent_id in agent_ids]
+
         if path is None:
-            timestamp = datetime.datetime.now()
-            path = os.path.join(self._save_directory, f"rlib-checkpoint-{timestamp.date()}-{timestamp.time()}.pkl.lz4")
+            path = os.path.join(self._default_path, f"rlib-checkpoint-{timestamp()}.pkl.lz4")
         elif path[-8:] != self._lz4_ext:
             path = path + self._lz4_ext
 
         experiment_state = {
             "agent_type": self._agent_type,
             "agent_params": self._agent_params,
             "agents": {
                 agent_id: {
-                    "state": state,
-                    "key": key,
-                } for agent_id, (state, key) in enumerate(zip(self._agents_states, self._agents_keys))
+                    "state": agent.state,
+                    "key": agent.key,
+                    "action": agent.action,
+                    "step": agent.step
+                } for agent_id, agent in zip(agent_ids, agent_containers)
             },
             "ext_type": self._ext_type,
             "ext_params": self._ext_params,
-            "loggers_type": self._loggers_type,
-            "loggers_sources": self._loggers_sources,
-            "loggers_params": self._loggers_params,
-            "save_directory": self._save_directory
+            "logger_types": self._logger_types,
+            "logger_sources": self._logger_sources,
+            "logger_params": self._logger_params,
+            "auto_checkpoint": self._auto_checkpoint
         }
 
         with lz4.frame.open(path, 'wb') as f:
-            f.write(pickle.dumps(experiment_state))
-        
+            f.write(cloudpickle.dumps(experiment_state))
+
         return path
-    
+
     @staticmethod
     def load(
-        path: str,
-        agent_params: Dict[str, Any] = None,
-        ext_params: Dict[str, Any] = None,
-        restore_loggers: bool = True
+            path: str,
+            *,
+            agent_params: dict[str, any] = None,
+            ext_params: dict[str, any] = None,
+            logger_types: Union[type, list[type]] = None,
+            logger_sources: Union[Source, list[Source]] = None,
+            logger_params: dict[str, any] = None
     ) -> RLib:
         """
         Loads the state of the experiment from a file in lz4 format.
 
         Parameters
         ----------
         path : str
             Path to the checkpoint file.
-        agent_params : Dict[str, Any], optional
-            Dictionary of altered agents parameters with their new values, by default None.
-        ext_params : Dict[str, Any], optional
+        agent_params : dict[str, any], optional
+            Dictionary of altered agent parameters with their new values, by default None.
+        ext_params : dict[str, any], optional
             Dictionary of altered extension parameters with their new values, by default None.
-        restore_loggers : bool, default=True
-            Flag indicating if the method should restore loggers settings.
+        logger_types : type or list[type], optional
+            Types of the selected logging modules. Must inherit from the ``BaseLogger`` class.
+        logger_sources : Source or list[Source], optional
+            Sources to log.
+        logger_params : dict, optional
+            Parameters of the selected loggers.
         """
-        
+
         with lz4.frame.open(path, 'rb') as f:
             experiment_state = pickle.loads(f.read())
-        
-        rlib = RLib(save_directory=experiment_state["save_directory"])
-        
-        rlib._agents_states = []
-        rlib._agents_keys = []
 
-        if ext_params:
-            rlib.set_ext(experiment_state["ext_type"], ext_params)
-        else:
-            rlib.set_ext(experiment_state["ext_type"], experiment_state["ext_params"])
-        
-        if agent_params:
-            rlib.set_agent(experiment_state["agent_type"], agent_params)
-        else:
-            rlib.set_agent(experiment_state["agent_type"], experiment_state["agent_params"])
+        rlib = RLib(
+            auto_checkpoint=experiment_state["auto_checkpoint"],
+            no_ext_mode=experiment_state["ext_type"] is None
+        )
+
+        rlib._agent_containers = []
+
+        if experiment_state["ext_type"]:
+            if ext_params:
+                rlib.set_ext(experiment_state["ext_type"], ext_params)
+            else:
+                rlib.set_ext(experiment_state["ext_type"], experiment_state["ext_params"])
+
+        if experiment_state["agent_type"]:
+            if agent_params:
+                rlib.set_agent(experiment_state["agent_type"], agent_params)
+            else:
+                rlib.set_agent(experiment_state["agent_type"], experiment_state["agent_params"])
 
-        if restore_loggers and experiment_state["loggers_type"]:
+        if logger_types:
+            rlib.set_loggers(logger_types, logger_sources, logger_params)
+        elif experiment_state["logger_types"]:
             rlib.set_loggers(
-                experiment_state["loggers_type"],
-                experiment_state["loggers_sources"],
-                experiment_state["loggers_params"]
+                experiment_state["logger_types"],
+                experiment_state["logger_sources"],
+                logger_params if logger_params else experiment_state["logger_params"]
+            )
+
+        for agent_id, agent_container in experiment_state["agents"].items():
+            while agent_id >= len(rlib._agent_containers):
+                rlib.init()
+
+            rlib._agent_containers[agent_id] = AgentContainer(
+                state=agent_container["state"],
+                key=agent_container["key"],
+                action=agent_container["action"],
+                step=agent_container["step"]
             )
-        
-        for agent_packed in experiment_state["agents"].values():
-            rlib._agents_states.append(agent_packed["state"])
-            rlib._agents_keys.append(agent_packed["key"])
 
         return rlib
+
+    def log(self, name: str, value: any) -> None:
+        """
+        Logs a custom value.
+
+        Parameters
+        ----------
+        name : str
+            The name of the value to log.
+        value : any
+            The value to log.
+        """
+
+        self._logs_observer.update_custom(value, name)
+
+    def to_tflite(self, path: str = None, *, agent_id: int = None, sample_only: bool = False) -> None:
+        """
+        Converts the agent to a TensorFlow Lite model and saves it to a file.
+
+        Parameters
+        ----------
+        path : str, optional
+            Path to the output file.
+        agent_id : int, optional
+            The identifier of the agent instance to convert. If specified,
+            state of the selected agent will be saved.
+        sample_only : bool
+            Flag indicating if the method should save only the sample function.
+        """
+
+        if not self._agent:
+            raise NoAgentError()
+
+        if len(self._agent_containers) == 0:
+            self.init()
+
+        if sample_only and agent_id is None:
+            raise ValueError("Agent ID must be specified when saving sample function only.")
+
+        if path is None:
+            path = self._default_path
+
+        if agent_id is None:
+            init_tfl, update_tfl, sample_tfl = self._agent.export(
+                init_key=jax.random.PRNGKey(42)
+            )
+        else:
+            init_tfl, update_tfl, sample_tfl = self._agent.export(
+                init_key=self._agent_containers[agent_id].key,
+                state=self._agent_containers[agent_id].state,
+                sample_only=sample_only
+            )
+
+        base_name = self._agent.__class__.__name__
+        base_name += f'-{agent_id}-' if agent_id is not None else '-'
+        base_name += timestamp()
+
+        with open(os.path.join(path, f'rlib-{base_name}-init.tflite'), 'wb') as f:
+            f.write(init_tfl)
+
+        with open(os.path.join(path, f'rlib-{base_name}-sample.tflite'), 'wb') as f:
+            f.write(sample_tfl)
+
+        if not sample_only:
+            with open(os.path.join(path, f'rlib-{base_name}-update.tflite'), 'wb') as f:
+                f.write(update_tfl)
```

### Comparing `reinforced-lib-0.2.0/reinforced_lib/utils/exceptions.py` & `reinforced-lib-1.0.0/reinforced_lib/utils/exceptions.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-import gym.spaces
+import gymnasium as gym
 
 
 class NoAgentError(Exception):
     """
     Raised when no agent is specified.
     """
 
@@ -79,64 +79,73 @@
 
     def __init__(self, provided_type: type) -> None:
         super().__init__(provided_type, 'logger')
 
 
 class ForbiddenOperationError(Exception):
     """
-    Raised when the user is trying to perform forbidden operation.
+    Raised when the user performs a forbidden operation.
     """
 
     def __str__(self) -> str:
         return 'Forbidden operation.'
 
 
 class ForbiddenAgentChangeError(ForbiddenOperationError):
     """
-    Raised when the user is trying to change the agent type after the first agent instance has been initialized.
+    Raised when the user changes the agent type after the first agent instance has been initialized.
     """
 
     def __str__(self) -> str:
         return 'Cannot change agent type after the first agent instance is initialized.'
 
 
 class ForbiddenExtensionChangeError(ForbiddenOperationError):
     """
-    Raised when the user is trying to change the extension type after the first agent instance has been initialized.
+    Raised when the user changes the extension type after the first agent instance has been initialized.
     """
 
     def __str__(self) -> str:
         return 'Cannot change extension type after the first agent instance is initialized.'
 
 
 class ForbiddenExtensionSetError(ForbiddenOperationError):
     """
-    Raised when the user is trying to set the extension type when ``no_ext_mode`` is enabled.
+    Raised when the user sets the extension type when ``no_ext_mode`` is enabled.
     """
 
     def __str__(self) -> str:
         return 'Cannot set extension type when \'no_ext_mode\' is enabled.'
 
 
 class ForbiddenLoggerSetError(ForbiddenOperationError):
     """
-    Raised when the user is trying to add a new logger after the first step has been made.
+    Raised when the user adds a new logger after the first step has been made.
     """
 
     def __str__(self) -> str:
         return 'Cannot add new loggers type after the first step has been made.'
 
 
 class IncorrectSpaceError(Exception):
     """
-    Raised when an unknown space is provided, for example a custom OpenAI Gym space.
+    Raised when an unknown space is provided, for example a custom Gymnasium space.
     """
 
     def __str__(self) -> str:
-        return 'Cannot find corresponding OpenAI Gym space.'
+        return 'Cannot find corresponding Gymnasium space.'
+
+
+class UnimplementedSpaceError(Exception):
+    """
+    Raised when an observation space is required but not implemented.
+    """
+
+    def __str__(self) -> str:
+        return 'Appropriate observation space is not implemented.'
 
 
 class IncompatibleSpacesError(Exception):
     """
     Raised when the observation spaces of two different modules are not compatible.
 
     Parameters
@@ -178,15 +187,15 @@
     def __str__(self) -> str:
         return f'Extension {self._extension_name} does not provide parameter ' \
                f'{self._parameter_name} of type {self._parameter_type}.'
 
 
 class UnsupportedLogTypeError(Exception):
     """
-    Raised when the user is trying to log values that are not supported by the logger.
+    Raised when the user logs values that are not supported by the logger.
 
     Parameters
     ----------
     logger_type : type
         Type of the used logger.
     log_type : type
         Type of the logged value.
@@ -208,7 +217,24 @@
     ----------
     provided_type : type
         Type provided by the user.
     """
 
     def __init__(self, provided_type: type) -> None:
         super().__init__(provided_type, 'source')
+
+
+class UnsupportedCustomLogsError(Exception):
+    """
+    Raised when the user tries to log custom values with a logger that does not support custom logging.
+
+    Parameters
+    ----------
+    logger_type : type
+        Type of the used logger.
+    """
+
+    def __init__(self, logger_type: type) -> None:
+        self._logger_name = logger_type.__name__
+
+    def __str__(self) -> str:
+        return f'Logger {self._logger_name} does not support custom logging.'
```

### Comparing `reinforced-lib-0.2.0/reinforced_lib.egg-info/PKG-INFO` & `reinforced-lib-1.0.0/reinforced_lib.egg-info/PKG-INFO`

 * *Files 22% similar despite different names*

```diff
@@ -1,136 +1,162 @@
 Metadata-Version: 2.1
 Name: reinforced-lib
-Version: 0.2.0
+Version: 1.0.0
 Summary: Reinforcement learning library
 Home-page: https://github.com/m-wojnar/reinforced-lib
-Download-URL: https://github.com/m-wojnar/reinforced-lib/archive/refs/tags/v0.2.0.tar.gz
+Download-URL: https://github.com/m-wojnar/reinforced-lib/archive/refs/tags/v1.0.0.tar.gz
 Author: Maksymilian Wojnar and Wojciech Ciężobka
 License: Mozilla Public License 2.0 (MPL 2.0)
-Keywords: machine-learning,reinforcement-learning,reinforcement-learning-agent,jax
+Keywords: deep-reinforcement-learning,jax,library,machine-learning,reinforcement-learning
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers
 Classifier: Intended Audience :: Education
 Classifier: Intended Audience :: Science/Research
 Classifier: License :: OSI Approved :: Mozilla Public License 2.0 (MPL 2.0)
 Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
+Classifier: Programming Language :: Python :: 3.11
 Classifier: Topic :: Scientific/Engineering :: Artificial Intelligence
 Classifier: Typing :: Typed
-Requires-Python: >=3.8, <4
+Requires-Python: >=3.9, <4
 Description-Content-Type: text/markdown
-Provides-Extra: dev
+Provides-Extra: docs
+Provides-Extra: full
 License-File: LICENSE
 
 # Reinforced-lib: Reinforcement learning library
 
+[![PyPI version][pypi-badge]][pypi]
+[![License: MPL 2.0][license-badge]][license]
 [![build and test][tests-badge]][github-actions]
 [![Documentation Status][rtd-badge]][documentation]
-[![PyPI version][pypi-badge]][pypi]
-[![License: MPL 2.0](https://img.shields.io/badge/License-MPL%202.0-brightgreen.svg)](https://opensource.org/licenses/MPL-2.0)
 
+[pypi-badge]: https://img.shields.io/pypi/v/reinforced-lib
+[pypi]: https://pypi.org/project/reinforced-lib/
+[license-badge]: https://img.shields.io/badge/License-MPL%202.0-brightgreen.svg
+[license]: https://opensource.org/licenses/MPL-2.0
 [tests-badge]: https://github.com/m-wojnar/reinforced-lib/actions/workflows/python-package.yml/badge.svg
 [github-actions]: https://github.com/m-wojnar/reinforced-lib/actions
 [rtd-badge]: https://readthedocs.org/projects/reinforced-lib/badge/?version=latest
 [documentation]: https://reinforced-lib.readthedocs.io/en/latest/
-[pypi-badge]: https://img.shields.io/pypi/v/reinforced-lib
-[pypi]: https://pypi.org/project/reinforced-lib/
-
-## Overview
 
-**Reinforced-lib** is a Python library designed to support research and prototyping using reinforcement learning
-(RL) algorithms. The library can serve as a simple solution with ready to use RL workflows as well as
-an expandable framework with programmable behaviour. Thanks to the functional implementation of the library's core,
-we can provide full access to the JAX's jit functionality, which boosts the agent's performance significantly.
+**Introducing Reinforced-lib:** a lightweight Python library for rapid development of RL solutions. It is open-source, 
+prioritizes ease of use, provides comprehensive documentation, and offers both deep reinforcement learning 
+(DRL) and classic non-neural agents. Built on [JAX](https://jax.readthedocs.io/en/latest/), it facilitates exporting 
+trained models to embedded devices, and makes it great for research and prototyping with RL algorithms. Access to JAX's 
+JIT functionality ensure high-performance results.
 
 ## Installation
 
 You can install the latest released version of Reinforced-lib from PyPI via:
 
 ```bash
 pip install reinforced-lib
 ```
 
-You can also download source code and install the development dependencies if you want to build the documentation locally:
+To have an easy access to the [example files](https://github.com/m-wojnar/reinforced-lib/tree/main/examples)
+you can clone the source code from our repository, and than install it locally with pip:
 
 ```bash
 git clone git@github.com:m-wojnar/reinforced-lib.git
 cd reinforced-lib
-pip3 install ".[dev]"
+pip install .
 ```
 
-## Example code
-
-```python
-from reinforced_lib import RLib
-from reinforced_lib.agents import ThompsonSampling
-from reinforced_lib.exts import IEEE_802_11_ax
+In the spirit of making Reinforced-lib a lightweight solution, we included only the necessary dependencies in the base 
+requirements. To fully benefit from Reinforced-lib conveniences, like TF Lite export, install with the "full" suffix:
 
-import gym
+```bash
+pip3 install ".[full]"
+```
 
+## Key components
 
-rlib = RLib(
-  agent_type=ThompsonSampling,
-  ext_type=IEEE_802_11_ax
-)
+Reinforced-lib facilitates seamless interaction between RL agents and the environment. Here are the key components 
+within of the library, represented in the API as different modules.
 
-env = gym.make('WifiSimulator-v1')
-env_state, _ = env.reset()
+- **RLib** - The core module which provides a simple and intuitive interface to manage agents, use extensions, 
+  and configure the logging system. Even if you're not a reinforcement learning (RL) expert, *RLib* makes it easy to 
+  implement the agent-environment interaction loop.
 
-terminated = False
-while not terminated:
-  action = rlib.sample(**env_state)
-  env_state, reward, terminated, *_ = env.step(action)
-```
+- **Agents** - Choose from a variety of RL agents available in the *Agents* module. These agents are designed to be 
+  versatile and work with any environment. If needed, you can even create your own agents using our documented recipes.
 
-## Integrated IEEE 802.11ax support
+- **Extensions** - Enhance agent observations with domain-specific knowledge by adding a suitable extension from the 
+  *Extensions* module. This module enables seamless agent switching and parameter tuning without extensive reconfiguration.
 
-Library design is distinctly influenced by the desire to support research in Wi-Fi. It can be a tool for researchers 
-to optimize the Wi-Fi protocols with built-in RL algorithms and provided IEEE 802.11ax environment extension.
+- **Logging** - This module allows you to monitor agent-environment interactions. Customize and adapt logging to your 
+  specific needs, capturing training metrics, internal agent state, or environment observations. The library includes 
+  various loggers for creating plots and output files, simplifying visualization and data processing.
 
-We also provide simple [ns-3](https://www.nsnam.org/) simulation and RL-based rate adaptation manager for the 
-IEEE 802.11ax standard in [examples](https://github.com/m-wojnar/reinforced-lib/tree/main/examples/ns-3).
+The figure below provides a visual representation of Reinforced-lib and the data-flow between its modules.
 
-## Modular architecture
+<img src="docs/resources/data-flow.png" width="600">
 
-**Reinforced-lib** can be well characterized by it's modular architecture which makes the library flexible, universal,
-and easy-to-use. Its key parts are placed in separate modules and connected in a standardized way to provide versatility
-and the possibility to extend individual modules in the future. Nevertheless, Reinforced-lib is a single piece of software
-that can be easily used, thanks to the topmost module, which ensures a simple and common interface for all agents.
+## JAX Backend
 
-<img src="docs/resources/architecture.jpg" width="600">
+Our library is built on top of JAX, a high-performance numerical computing library. JAX makes it easy to implement 
+RL algorithms efficiently. It provides powerful transformations, including JIT compilation,  automatic differentiation, 
+vectorization, and parallelization. Our library is fully compatible with DeepMind's JAX ecosystem, granting access to 
+state-of-the-art RL models and helper libraries. JIT compilation significantly accelerates execution and ensures 
+portability across different architectures (CPUs, GPUs, TPUs) without requiring code modifications.
 
-### The API module
+## Edge Device Export
 
-The API module is the top layer of the library; it exposes a simple and intuitive interface that makes the library easy
-to use. There are several important methods, one of them is responsible for creating a new agent. Another takes the
-observations from the environment as input, updates the state of the agent, and returns the next action proposed by the agent.
-The last two methods are used to persist the state of the agent by storing it in memory.
+Reinforced-lib is designed to work seamlessly on wireless, low-powered devices, where resources are limited. It's the 
+perfect solution for energy-constrained environments that may struggle with other ML frameworks. You can export your 
+trained models to [TensorFlow Lite](https://www.tensorflow.org/lite) with ease, reducing runtime overhead and 
+optimizing performance. This means you can deploy RL agents on resource-limited devices efficiently.
 
-### The extensions module
+## Example code
 
-The Extensions module consists of containers with domain-specific knowledge and ensures the proper use of universal agents
-implemented in **Reinforced-lib**. If a specific problem is implemented in the form of an extension, the module infers and
-provides the appropriate data to the agent, and at the same time requires adequate, corresponding values from the user.
+Experience the simplicity of our library and witness the fundamental agent-environment interaction loop with our 
+straightforward example. This code can by used to train a deep Q-learning agent on the `CartPole-v1` environment 
+effortlessly using Reinforced-lib.
 
-### The agents module
+```python
+import gymnasium as gym
+import haiku as hk
+import optax
+from chex import Array
 
-The Agents module is a collection of universal algorithms, which are called "agents" in RL community. Each agent has
-a similar API to communicate with the Extensions module, which ensures its versatility and expandability. In this release
-of **Reinforced-lib** we focused on the [multi-armed bandit problem](https://en.wikipedia.org/wiki/Multi-armed_bandit),
-hence the imlemented agents are related to this task.
+from reinforced_lib import RLib
+from reinforced_lib.agents.deep import QLearning
+from reinforced_lib.exts import Gymnasium
 
-### The logging module
 
-The Logging module is responsible for collecting data from other modules and observing their state in real time.
-It also has great potential in using the library to create new RL agents - it can be used to develop, evaluate,
-and debug new agents by observing decisions they make; record and visualize how environment state changes in time;
-or provide a simple way to obtain a training summary, metrics, and logs.
+@hk.transform_with_state
+def q_network(x: Array) -> Array:
+    return hk.nets.MLP([256, 2])(x)
+
+
+if __name__ == '__main__':
+    rl = RLib(
+        agent_type=QLearning,
+        agent_params={
+            'q_network': q_network,
+            'optimizer': optax.rmsprop(3e-4, decay=0.95, eps=1e-2),
+        },
+        ext_type=Gymnasium,
+        ext_params={'env_id': 'CartPole-v1'}
+    )
+
+    for epoch in range(300):
+        env = gym.make('CartPole-v1', render_mode='human')
+
+        _, _ = env.reset()
+        action = env.action_space.sample()
+        terminal = False
+
+        while not terminal:
+            env_state = env.step(action.item())
+            action = rl.sample(*env_state)
+            terminal = env_state[2] or env_state[3]
+```
 
 ## Citing Reinforced-lib
 
 To cite this repository:
 
 ```
 @software{reinforcedlib2022,
```

### Comparing `reinforced-lib-0.2.0/reinforced_lib.egg-info/SOURCES.txt` & `reinforced-lib-1.0.0/reinforced_lib.egg-info/SOURCES.txt`

 * *Files 18% similar despite different names*

```diff
@@ -8,31 +8,41 @@
 reinforced_lib.egg-info/PKG-INFO
 reinforced_lib.egg-info/SOURCES.txt
 reinforced_lib.egg-info/dependency_links.txt
 reinforced_lib.egg-info/requires.txt
 reinforced_lib.egg-info/top_level.txt
 reinforced_lib/agents/__init__.py
 reinforced_lib/agents/base_agent.py
-reinforced_lib/agents/e_greedy.py
-reinforced_lib/agents/softmax.py
-reinforced_lib/agents/thompson_sampling.py
-reinforced_lib/agents/ucb.py
 reinforced_lib/agents/core/__init__.py
 reinforced_lib/agents/core/particle_filter.py
-reinforced_lib/agents/wifi/__init__.py
-reinforced_lib/agents/wifi/particle_filter.py
+reinforced_lib/agents/deep/__init__.py
+reinforced_lib/agents/deep/ddpg.py
+reinforced_lib/agents/deep/dqn.py
+reinforced_lib/agents/deep/expected_sarsa.py
+reinforced_lib/agents/deep/q_learning.py
+reinforced_lib/agents/mab/__init__.py
+reinforced_lib/agents/mab/e_greedy.py
+reinforced_lib/agents/mab/exp3.py
+reinforced_lib/agents/mab/softmax.py
+reinforced_lib/agents/mab/thompson_sampling.py
+reinforced_lib/agents/mab/ucb.py
 reinforced_lib/exts/__init__.py
 reinforced_lib/exts/base_ext.py
-reinforced_lib/exts/ieee_802_11_ax.py
+reinforced_lib/exts/gymnasium.py
 reinforced_lib/exts/utils.py
 reinforced_lib/logs/__init__.py
 reinforced_lib/logs/base_logger.py
 reinforced_lib/logs/csv_logger.py
 reinforced_lib/logs/logs_observer.py
 reinforced_lib/logs/plots_logger.py
 reinforced_lib/logs/stdout_logger.py
+reinforced_lib/logs/tb_logger.py
 reinforced_lib/utils/__init__.py
 reinforced_lib/utils/exceptions.py
-requirements/requirements-dev.txt
+reinforced_lib/utils/experience_replay.py
+reinforced_lib/utils/jax_utils.py
+requirements/requirements-docs.txt
+requirements/requirements-full.txt
 requirements/requirements.txt
 test/test_rlib.py
-test/test_rlib_serialization.py
+test/test_rlib_serialization.py
+test/test_rlib_to_tflite.py
```

### Comparing `reinforced-lib-0.2.0/setup.py` & `reinforced-lib-1.0.0/setup.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,48 +1,48 @@
-from typing import List
-
 from setuptools import setup, find_packages
 
 
-def read_requirements(filename: str) -> List[str]:
-    with open(filename) as file:
-        return file.read().splitlines()
-
-
 def read_file(filename: str) -> str:
-    with open(filename) as file:
+    with open(filename, 'r') as file:
         return file.read()
 
 
+def read_requirements(filename: str) -> list[str]:
+    return read_file(filename).splitlines()
+
+
 setup(
     name='reinforced-lib',
-    version='0.2.0',
+    version='1.0.0',
     packages=find_packages(include=[
         'reinforced_lib', 
         'reinforced_lib.*'
     ]),
     license='Mozilla Public License 2.0 (MPL 2.0)',
     description='Reinforcement learning library',
     long_description=read_file('README.md'),
     long_description_content_type='text/markdown',
     author='Maksymilian Wojnar and Wojciech Ciężobka',
     url='https://github.com/m-wojnar/reinforced-lib',
-    download_url='https://github.com/m-wojnar/reinforced-lib/archive/refs/tags/v0.2.0.tar.gz',
-    keywords='machine-learning, reinforcement-learning, reinforcement-learning-agent, jax',
-    python_requires='>=3.8, <4',
+    download_url='https://github.com/m-wojnar/reinforced-lib/archive/refs/tags/v1.0.0.tar.gz',
+    keywords='deep-reinforcement-learning, jax, library, machine-learning, reinforcement-learning',
+    python_requires='>=3.9, <4',
     install_requires=read_requirements('requirements/requirements.txt'),
-    extras_require={'dev': read_requirements('requirements/requirements-dev.txt')},
+    extras_require={
+        'docs': read_requirements('requirements/requirements-docs.txt'),
+        'full': read_requirements('requirements/requirements-full.txt')
+    },
     include_package_data=True,
     classifiers=[
         'Development Status :: 4 - Beta',
         'Intended Audience :: Developers',
         'Intended Audience :: Education',
         'Intended Audience :: Science/Research',
         'License :: OSI Approved :: Mozilla Public License 2.0 (MPL 2.0)',
         'Programming Language :: Python :: 3',
-        'Programming Language :: Python :: 3.8',
         'Programming Language :: Python :: 3.9',
         'Programming Language :: Python :: 3.10',
+        'Programming Language :: Python :: 3.11',
         'Topic :: Scientific/Engineering :: Artificial Intelligence',
         'Typing :: Typed'
     ],
 )
```

### Comparing `reinforced-lib-0.2.0/test/test_rlib_serialization.py` & `reinforced-lib-1.0.0/test/test_rlib_serialization.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,63 +1,57 @@
-from typing import List
-
 import unittest
 import os
 import jax
 import jax.numpy as jnp
-import reinforced_lib as rfl
 
-from reinforced_lib.agents import ThompsonSampling
-from reinforced_lib.exts import IEEE_802_11_ax
+from reinforced_lib.agents.mab import EGreedy
 from reinforced_lib.rlib import RLib
 from reinforced_lib.logs import *
 
 
 class TestRLibSerialization(unittest.TestCase):
 
     checkpoint_path = os.path.join(os.path.expanduser("~"), "checkpoint.pkl.lz4")
     arms_probs = jnp.array([1.0, 1.0, 0.99, 0.97, 0.91, 0.77, 0.32, 0.05, 0.01, 0.0, 0.0, 0.0])
     time = jnp.linspace(0, 10, 1000)
     t_change = jnp.max(time) / 2
     key = jax.random.PRNGKey(42)
 
 
-    def run_experiment(self, reload: bool, new_decay: float = None) -> List[int]:
-        rl = rfl.RLib(
-            agent_type=ThompsonSampling,
-            agent_params={"decay": 0.0},
-            ext_type=IEEE_802_11_ax,
-            loggers_type=CsvLogger,
-            loggers_sources=['n_failed', 'n_successful', ('action', SourceType.METRIC)],
-            loggers_params={'csv_path': f'output_reload={reload}_new-decay={new_decay}.csv'}
+    def run_experiment(self, reload: bool, new_decay: float = None) -> list[int]:
+        rl = RLib(
+            agent_type=EGreedy,
+            agent_params={'n_arms': len(self.arms_probs), 'e': 0.1},
+            no_ext_mode=True,
+            logger_types=CsvLogger,
+            logger_sources=['n_failed', 'n_successful', ('action', SourceType.METRIC)],
+            logger_params={'csv_path': f'output_reload={reload}_new-decay={new_decay}.csv'}
         )
 
         actions = []
         a = 0
 
         reloaded = not reload
         for t in self.time:
             r = int(jax.random.uniform(self.key) < self.arms_probs[a])
             observations = {
-                'time': t,
-                'mcs': a,
-                'n_successful': r,
-                'n_failed': 1 - r,
+                'action': a,
+                'reward': r
             }
 
-            a = rl.sample(**observations)
-            actions.append(int(a))
+            a = rl.sample(update_observations=observations)
+            actions.append(a)
 
             if t > self.t_change and not reloaded:
                 save_path = rl.save()
 
                 if new_decay:
-                    rl = RLib.load(save_path, agent_params={"decay": new_decay}, restore_loggers=False)
+                    rl = RLib.load(save_path, agent_params={'n_arms': len(self.arms_probs), 'e': 0.5})
                 else:
-                    rl = RLib.load(save_path, restore_loggers=False)
+                    rl = RLib.load(save_path)
                 reloaded = True
         
         return actions
     
 
     def test_reload(self):
         """
```

