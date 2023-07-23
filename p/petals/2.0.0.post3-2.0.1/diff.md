# Comparing `tmp/petals-2.0.0.post3.tar.gz` & `tmp/petals-2.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "petals-2.0.0.post3.tar", last modified: Thu Jul 20 17:08:19 2023, max compression
+gzip compressed data, was "petals-2.0.1.tar", last modified: Sun Jul 23 14:48:31 2023, max compression
```

## Comparing `petals-2.0.0.post3.tar` & `petals-2.0.1.tar`

### file list

```diff
@@ -1,90 +1,90 @@
-drwxrwxr-x   0 jheuristic  (1000) jheuristic  (1000)        0 2023-07-20 17:08:19.855064 petals-2.0.0.post3/
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     1089 2022-11-26 05:33:56.000000 petals-2.0.0.post3/LICENSE
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)    12478 2023-07-20 17:08:19.855064 petals-2.0.0.post3/PKG-INFO
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)    11293 2023-07-20 17:00:05.000000 petals-2.0.0.post3/README.md
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      333 2023-04-25 09:55:28.000000 petals-2.0.0.post3/pyproject.toml
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     1752 2023-07-20 17:08:19.855064 petals-2.0.0.post3/setup.cfg
-drwxrwxr-x   0 jheuristic  (1000) jheuristic  (1000)        0 2023-07-20 17:08:19.847063 petals-2.0.0.post3/src/
-drwxrwxr-x   0 jheuristic  (1000) jheuristic  (1000)        0 2023-07-20 17:08:19.851063 petals-2.0.0.post3/src/petals/
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      784 2023-07-20 17:08:09.000000 petals-2.0.0.post3/src/petals/__init__.py
-drwxrwxr-x   0 jheuristic  (1000) jheuristic  (1000)        0 2023-07-20 17:08:19.851063 petals-2.0.0.post3/src/petals/cli/
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)        0 2022-11-30 08:13:52.000000 petals-2.0.0.post3/src/petals/cli/__init__.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     3798 2023-01-13 00:54:42.000000 petals-2.0.0.post3/src/petals/cli/run_dht.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)    13932 2023-07-20 17:00:05.000000 petals-2.0.0.post3/src/petals/cli/run_server.py
-drwxrwxr-x   0 jheuristic  (1000) jheuristic  (1000)        0 2023-07-20 17:08:19.851063 petals-2.0.0.post3/src/petals/client/
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      282 2023-06-29 20:31:16.000000 petals-2.0.0.post3/src/petals/client/__init__.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     3600 2023-07-12 11:02:03.000000 petals-2.0.0.post3/src/petals/client/from_pretrained.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)    15296 2023-07-18 23:25:43.000000 petals-2.0.0.post3/src/petals/client/inference_session.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     3526 2023-06-29 20:31:16.000000 petals-2.0.0.post3/src/petals/client/lm_head.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     3493 2023-06-29 20:31:16.000000 petals-2.0.0.post3/src/petals/client/ptune.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     7128 2023-02-06 20:57:31.000000 petals-2.0.0.post3/src/petals/client/remote_forward_backward.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)    14964 2023-05-09 21:02:40.000000 petals-2.0.0.post3/src/petals/client/remote_generation.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     2675 2023-07-12 12:22:35.000000 petals-2.0.0.post3/src/petals/client/remote_sequential.py
-drwxrwxr-x   0 jheuristic  (1000) jheuristic  (1000)        0 2023-07-20 17:08:19.851063 petals-2.0.0.post3/src/petals/client/routing/
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)       71 2022-12-01 12:24:57.000000 petals-2.0.0.post3/src/petals/client/routing/__init__.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     4629 2023-07-17 09:46:40.000000 petals-2.0.0.post3/src/petals/client/routing/sequence_info.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)    22820 2023-07-20 17:00:05.000000 petals-2.0.0.post3/src/petals/client/routing/sequence_manager.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      649 2022-12-01 12:24:57.000000 petals-2.0.0.post3/src/petals/client/routing/spending_policy.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)    12405 2023-06-29 20:31:16.000000 petals-2.0.0.post3/src/petals/client/sequential_autograd.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      904 2023-07-20 17:00:05.000000 petals-2.0.0.post3/src/petals/constants.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     2348 2023-07-19 16:28:49.000000 petals-2.0.0.post3/src/petals/data_structures.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     4511 2023-07-17 06:29:38.000000 petals-2.0.0.post3/src/petals/dht_utils.py
-drwxrwxr-x   0 jheuristic  (1000) jheuristic  (1000)        0 2023-07-20 17:08:19.851063 petals-2.0.0.post3/src/petals/models/
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)       68 2023-07-13 20:49:11.000000 petals-2.0.0.post3/src/petals/models/__init__.py
-drwxrwxr-x   0 jheuristic  (1000) jheuristic  (1000)        0 2023-07-20 17:08:19.851063 petals-2.0.0.post3/src/petals/models/bloom/
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      556 2023-06-29 20:31:16.000000 petals-2.0.0.post3/src/petals/models/bloom/__init__.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     1414 2023-07-13 20:49:11.000000 petals-2.0.0.post3/src/petals/models/bloom/block.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     1380 2023-07-19 16:28:49.000000 petals-2.0.0.post3/src/petals/models/bloom/config.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     5243 2023-07-19 01:15:47.000000 petals-2.0.0.post3/src/petals/models/bloom/model.py
-drwxrwxr-x   0 jheuristic  (1000) jheuristic  (1000)        0 2023-07-20 17:08:19.851063 petals-2.0.0.post3/src/petals/models/llama/
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      556 2023-06-29 20:31:16.000000 petals-2.0.0.post3/src/petals/models/llama/__init__.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     3582 2023-07-19 16:28:49.000000 petals-2.0.0.post3/src/petals/models/llama/block.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     1893 2023-07-19 16:28:49.000000 petals-2.0.0.post3/src/petals/models/llama/config.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     5998 2023-07-19 01:15:47.000000 petals-2.0.0.post3/src/petals/models/llama/model.py
-drwxrwxr-x   0 jheuristic  (1000) jheuristic  (1000)        0 2023-07-20 17:08:19.855064 petals-2.0.0.post3/src/petals/server/
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)        0 2022-11-30 08:13:52.000000 petals-2.0.0.post3/src/petals/server/__init__.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     9994 2023-07-19 16:28:49.000000 petals-2.0.0.post3/src/petals/server/backend.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     4499 2023-04-06 15:09:40.000000 petals-2.0.0.post3/src/petals/server/block_selection.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     1893 2023-07-12 11:02:03.000000 petals-2.0.0.post3/src/petals/server/block_utils.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     6655 2023-07-19 16:28:49.000000 petals-2.0.0.post3/src/petals/server/from_pretrained.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)    35230 2023-07-19 10:53:04.000000 petals-2.0.0.post3/src/petals/server/handler.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     8718 2023-07-15 01:19:46.000000 petals-2.0.0.post3/src/petals/server/memory_cache.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     7706 2023-07-20 17:00:05.000000 petals-2.0.0.post3/src/petals/server/reachability.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)    30183 2023-07-19 16:28:49.000000 petals-2.0.0.post3/src/petals/server/server.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     8412 2023-04-06 15:09:40.000000 petals-2.0.0.post3/src/petals/server/task_pool.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      842 2023-01-22 05:16:17.000000 petals-2.0.0.post3/src/petals/server/task_prioritizer.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     8552 2023-07-18 22:29:14.000000 petals-2.0.0.post3/src/petals/server/throughput.py
-drwxrwxr-x   0 jheuristic  (1000) jheuristic  (1000)        0 2023-07-20 17:08:19.855064 petals-2.0.0.post3/src/petals/utils/
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      182 2023-06-29 20:31:16.000000 petals-2.0.0.post3/src/petals/utils/__init__.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      525 2022-12-29 20:33:47.000000 petals-2.0.0.post3/src/petals/utils/asyncio.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     2189 2023-07-19 16:28:49.000000 petals-2.0.0.post3/src/petals/utils/auto_config.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     6594 2023-07-19 16:28:49.000000 petals-2.0.0.post3/src/petals/utils/convert_block.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     2963 2023-07-09 23:10:48.000000 petals-2.0.0.post3/src/petals/utils/disk_cache.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     5560 2023-07-18 09:05:08.000000 petals-2.0.0.post3/src/petals/utils/generation_algorithms.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     1853 2022-12-03 11:35:20.000000 petals-2.0.0.post3/src/petals/utils/generation_constraints.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      270 2023-07-19 16:28:49.000000 petals-2.0.0.post3/src/petals/utils/hf_auth.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      745 2023-06-29 20:31:16.000000 petals-2.0.0.post3/src/petals/utils/logging.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      171 2023-07-19 16:28:49.000000 petals-2.0.0.post3/src/petals/utils/misc.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)    12164 2023-07-19 16:28:49.000000 petals-2.0.0.post3/src/petals/utils/peft.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     2283 2023-07-18 09:05:08.000000 petals-2.0.0.post3/src/petals/utils/ping.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      310 2023-07-18 09:05:08.000000 petals-2.0.0.post3/src/petals/utils/random.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     1438 2023-06-29 20:31:16.000000 petals-2.0.0.post3/src/petals/utils/version.py
-drwxrwxr-x   0 jheuristic  (1000) jheuristic  (1000)        0 2023-07-20 17:08:19.851063 petals-2.0.0.post3/src/petals.egg-info/
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)    12478 2023-07-20 17:08:19.000000 petals-2.0.0.post3/src/petals.egg-info/PKG-INFO
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     2331 2023-07-20 17:08:19.000000 petals-2.0.0.post3/src/petals.egg-info/SOURCES.txt
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)        1 2023-07-20 17:08:19.000000 petals-2.0.0.post3/src/petals.egg-info/dependency_links.txt
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      456 2023-07-20 17:08:19.000000 petals-2.0.0.post3/src/petals.egg-info/requires.txt
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)        7 2023-07-20 17:08:19.000000 petals-2.0.0.post3/src/petals.egg-info/top_level.txt
-drwxrwxr-x   0 jheuristic  (1000) jheuristic  (1000)        0 2023-07-20 17:08:19.855064 petals-2.0.0.post3/tests/
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     1646 2023-07-17 09:46:40.000000 petals-2.0.0.post3/tests/test_aux_functions.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     1603 2023-06-30 00:37:10.000000 petals-2.0.0.post3/tests/test_block_exact_match.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     2947 2023-06-29 20:31:16.000000 petals-2.0.0.post3/tests/test_chained_calls.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      672 2023-06-29 20:31:16.000000 petals-2.0.0.post3/tests/test_dtype.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     8121 2023-07-12 12:22:35.000000 petals-2.0.0.post3/tests/test_full_model.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     1535 2023-07-12 12:22:35.000000 petals-2.0.0.post3/tests/test_peft.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     2848 2023-04-25 15:58:19.000000 petals-2.0.0.post3/tests/test_priority_pool.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     6055 2023-07-09 23:10:48.000000 petals-2.0.0.post3/tests/test_remote_sequential.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     1924 2023-07-14 15:21:17.000000 petals-2.0.0.post3/tests/test_sequence_manager.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     1707 2023-06-29 20:31:16.000000 petals-2.0.0.post3/tests/test_server_stats.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     1911 2023-06-29 20:31:16.000000 petals-2.0.0.post3/tests/test_tensor_parallel.py
--rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      466 2023-07-12 12:22:35.000000 petals-2.0.0.post3/tests/test_utils.py
+drwxrwxr-x   0 jheuristic  (1000) jheuristic  (1000)        0 2023-07-23 14:48:31.315667 petals-2.0.1/
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     1089 2022-11-26 05:33:56.000000 petals-2.0.1/LICENSE
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)    13837 2023-07-23 14:48:31.315667 petals-2.0.1/PKG-INFO
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)    12664 2023-07-23 12:40:54.000000 petals-2.0.1/README.md
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      333 2023-04-25 09:55:28.000000 petals-2.0.1/pyproject.toml
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     1743 2023-07-23 14:48:31.315667 petals-2.0.1/setup.cfg
+drwxrwxr-x   0 jheuristic  (1000) jheuristic  (1000)        0 2023-07-23 14:48:31.307667 petals-2.0.1/src/
+drwxrwxr-x   0 jheuristic  (1000) jheuristic  (1000)        0 2023-07-23 14:48:31.307667 petals-2.0.1/src/petals/
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      778 2023-07-23 14:46:44.000000 petals-2.0.1/src/petals/__init__.py
+drwxrwxr-x   0 jheuristic  (1000) jheuristic  (1000)        0 2023-07-23 14:48:31.307667 petals-2.0.1/src/petals/cli/
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)        0 2022-11-30 08:13:52.000000 petals-2.0.1/src/petals/cli/__init__.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     3798 2023-01-13 00:54:42.000000 petals-2.0.1/src/petals/cli/run_dht.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)    14144 2023-07-23 14:46:44.000000 petals-2.0.1/src/petals/cli/run_server.py
+drwxrwxr-x   0 jheuristic  (1000) jheuristic  (1000)        0 2023-07-23 14:48:31.311667 petals-2.0.1/src/petals/client/
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      282 2023-06-29 20:31:16.000000 petals-2.0.1/src/petals/client/__init__.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     3600 2023-07-12 11:02:03.000000 petals-2.0.1/src/petals/client/from_pretrained.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)    15296 2023-07-18 23:25:43.000000 petals-2.0.1/src/petals/client/inference_session.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     3526 2023-06-29 20:31:16.000000 petals-2.0.1/src/petals/client/lm_head.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     3493 2023-06-29 20:31:16.000000 petals-2.0.1/src/petals/client/ptune.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     7128 2023-02-06 20:57:31.000000 petals-2.0.1/src/petals/client/remote_forward_backward.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)    14964 2023-05-09 21:02:40.000000 petals-2.0.1/src/petals/client/remote_generation.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     2675 2023-07-12 12:22:35.000000 petals-2.0.1/src/petals/client/remote_sequential.py
+drwxrwxr-x   0 jheuristic  (1000) jheuristic  (1000)        0 2023-07-23 14:48:31.311667 petals-2.0.1/src/petals/client/routing/
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)       71 2022-12-01 12:24:57.000000 petals-2.0.1/src/petals/client/routing/__init__.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     4629 2023-07-17 09:46:40.000000 petals-2.0.1/src/petals/client/routing/sequence_info.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)    23031 2023-07-23 12:40:54.000000 petals-2.0.1/src/petals/client/routing/sequence_manager.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      649 2022-12-01 12:24:57.000000 petals-2.0.1/src/petals/client/routing/spending_policy.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)    12405 2023-06-29 20:31:16.000000 petals-2.0.1/src/petals/client/sequential_autograd.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      904 2023-07-20 17:00:05.000000 petals-2.0.1/src/petals/constants.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     2348 2023-07-19 16:28:49.000000 petals-2.0.1/src/petals/data_structures.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     4511 2023-07-17 06:29:38.000000 petals-2.0.1/src/petals/dht_utils.py
+drwxrwxr-x   0 jheuristic  (1000) jheuristic  (1000)        0 2023-07-23 14:48:31.311667 petals-2.0.1/src/petals/models/
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)       68 2023-07-13 20:49:11.000000 petals-2.0.1/src/petals/models/__init__.py
+drwxrwxr-x   0 jheuristic  (1000) jheuristic  (1000)        0 2023-07-23 14:48:31.311667 petals-2.0.1/src/petals/models/bloom/
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      556 2023-06-29 20:31:16.000000 petals-2.0.1/src/petals/models/bloom/__init__.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     1414 2023-07-13 20:49:11.000000 petals-2.0.1/src/petals/models/bloom/block.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     1380 2023-07-19 16:28:49.000000 petals-2.0.1/src/petals/models/bloom/config.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     5243 2023-07-19 01:15:47.000000 petals-2.0.1/src/petals/models/bloom/model.py
+drwxrwxr-x   0 jheuristic  (1000) jheuristic  (1000)        0 2023-07-23 14:48:31.311667 petals-2.0.1/src/petals/models/llama/
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      556 2023-06-29 20:31:16.000000 petals-2.0.1/src/petals/models/llama/__init__.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     3582 2023-07-19 16:28:49.000000 petals-2.0.1/src/petals/models/llama/block.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     1893 2023-07-19 16:28:49.000000 petals-2.0.1/src/petals/models/llama/config.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     5998 2023-07-19 01:15:47.000000 petals-2.0.1/src/petals/models/llama/model.py
+drwxrwxr-x   0 jheuristic  (1000) jheuristic  (1000)        0 2023-07-23 14:48:31.311667 petals-2.0.1/src/petals/server/
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)        0 2022-11-30 08:13:52.000000 petals-2.0.1/src/petals/server/__init__.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)    11814 2023-07-23 12:40:54.000000 petals-2.0.1/src/petals/server/backend.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     4499 2023-04-06 15:09:40.000000 petals-2.0.1/src/petals/server/block_selection.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     1893 2023-07-12 11:02:03.000000 petals-2.0.1/src/petals/server/block_utils.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     6664 2023-07-23 12:40:54.000000 petals-2.0.1/src/petals/server/from_pretrained.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)    35240 2023-07-23 12:40:54.000000 petals-2.0.1/src/petals/server/handler.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     8216 2023-07-21 14:06:01.000000 petals-2.0.1/src/petals/server/memory_cache.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     7706 2023-07-20 17:00:05.000000 petals-2.0.1/src/petals/server/reachability.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)    30466 2023-07-23 14:46:44.000000 petals-2.0.1/src/petals/server/server.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     8412 2023-04-06 15:09:40.000000 petals-2.0.1/src/petals/server/task_pool.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      842 2023-01-22 05:16:17.000000 petals-2.0.1/src/petals/server/task_prioritizer.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     8657 2023-07-23 12:40:54.000000 petals-2.0.1/src/petals/server/throughput.py
+drwxrwxr-x   0 jheuristic  (1000) jheuristic  (1000)        0 2023-07-23 14:48:31.311667 petals-2.0.1/src/petals/utils/
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      182 2023-06-29 20:31:16.000000 petals-2.0.1/src/petals/utils/__init__.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      525 2022-12-29 20:33:47.000000 petals-2.0.1/src/petals/utils/asyncio.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     2258 2023-07-23 12:40:54.000000 petals-2.0.1/src/petals/utils/auto_config.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     6594 2023-07-19 16:28:49.000000 petals-2.0.1/src/petals/utils/convert_block.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     2963 2023-07-09 23:10:48.000000 petals-2.0.1/src/petals/utils/disk_cache.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     5560 2023-07-18 09:05:08.000000 petals-2.0.1/src/petals/utils/generation_algorithms.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     1853 2022-12-03 11:35:20.000000 petals-2.0.1/src/petals/utils/generation_constraints.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      270 2023-07-19 16:28:49.000000 petals-2.0.1/src/petals/utils/hf_auth.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      745 2023-06-29 20:31:16.000000 petals-2.0.1/src/petals/utils/logging.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      171 2023-07-19 16:28:49.000000 petals-2.0.1/src/petals/utils/misc.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)    12164 2023-07-19 16:28:49.000000 petals-2.0.1/src/petals/utils/peft.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     2283 2023-07-18 09:05:08.000000 petals-2.0.1/src/petals/utils/ping.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      310 2023-07-18 09:05:08.000000 petals-2.0.1/src/petals/utils/random.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     1438 2023-06-29 20:31:16.000000 petals-2.0.1/src/petals/utils/version.py
+drwxrwxr-x   0 jheuristic  (1000) jheuristic  (1000)        0 2023-07-23 14:48:31.307667 petals-2.0.1/src/petals.egg-info/
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)    13837 2023-07-23 14:48:31.000000 petals-2.0.1/src/petals.egg-info/PKG-INFO
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     2331 2023-07-23 14:48:31.000000 petals-2.0.1/src/petals.egg-info/SOURCES.txt
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)        1 2023-07-23 14:48:31.000000 petals-2.0.1/src/petals.egg-info/dependency_links.txt
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      456 2023-07-23 14:48:31.000000 petals-2.0.1/src/petals.egg-info/requires.txt
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)        7 2023-07-23 14:48:31.000000 petals-2.0.1/src/petals.egg-info/top_level.txt
+drwxrwxr-x   0 jheuristic  (1000) jheuristic  (1000)        0 2023-07-23 14:48:31.315667 petals-2.0.1/tests/
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     1646 2023-07-17 09:46:40.000000 petals-2.0.1/tests/test_aux_functions.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     1603 2023-06-30 00:37:10.000000 petals-2.0.1/tests/test_block_exact_match.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     2947 2023-06-29 20:31:16.000000 petals-2.0.1/tests/test_chained_calls.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      672 2023-06-29 20:31:16.000000 petals-2.0.1/tests/test_dtype.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     8315 2023-07-23 12:40:54.000000 petals-2.0.1/tests/test_full_model.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     1535 2023-07-12 12:22:35.000000 petals-2.0.1/tests/test_peft.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     2848 2023-04-25 15:58:19.000000 petals-2.0.1/tests/test_priority_pool.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     6055 2023-07-09 23:10:48.000000 petals-2.0.1/tests/test_remote_sequential.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     1924 2023-07-14 15:21:17.000000 petals-2.0.1/tests/test_sequence_manager.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     1707 2023-06-29 20:31:16.000000 petals-2.0.1/tests/test_server_stats.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)     1911 2023-06-29 20:31:16.000000 petals-2.0.1/tests/test_tensor_parallel.py
+-rw-rw-r--   0 jheuristic  (1000) jheuristic  (1000)      466 2023-07-12 12:22:35.000000 petals-2.0.1/tests/test_utils.py
```

### Comparing `petals-2.0.0.post3/LICENSE` & `petals-2.0.1/LICENSE`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/PKG-INFO` & `petals-2.0.1/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: petals
-Version: 2.0.0.post3
+Version: 2.0.1
 Summary: Easy way to efficiently run 100B+ language models without high-end GPUs
 Home-page: https://github.com/bigscience-workshop/petals
 Author: Petals Developers
 Author-email: petals-devs@googlegroups.com
 Project-URL: Bug Tracker, https://github.com/bigscience-workshop/petals/issues
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers
@@ -16,15 +16,15 @@
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Topic :: Scientific/Engineering
 Classifier: Topic :: Scientific/Engineering :: Mathematics
 Classifier: Topic :: Scientific/Engineering :: Artificial Intelligence
 Classifier: Topic :: Software Development
 Classifier: Topic :: Software Development :: Libraries
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
-Requires-Python: <3.11,>=3.8
+Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 Provides-Extra: dev
 License-File: LICENSE
 
 <p align="center">
     <img src="https://i.imgur.com/7eR7Pan.png" width="400"><br>
     Run large language models at home, BitTorrent-style.<br>
@@ -51,40 +51,54 @@
 print(tokenizer.decode(outputs[0]))  # A cat sat on a mat...
 ```
 
 <p align="center">
     🚀 &nbsp;<b><a href="https://colab.research.google.com/drive/1uCphNY7gfAUkdDrTx21dZZwCOUDCMPw8?usp=sharing">Try now in Colab</a></b>
 </p>
 
-📋 Make sure you follow the model's terms of use (see [LLaMA 2](https://bit.ly/llama2-license), [LLaMA](https://bit.ly/llama-license) and [BLOOM](https://bit.ly/bloom-license) licenses).
+🦙 **Want to run LLaMA 2?** Request access to its weights at the ♾️ [Meta AI website](https://ai.meta.com/resources/models-and-libraries/llama-downloads/) and 🤗 [Model Hub](https://huggingface.co/meta-llama/Llama-2-70b-hf), then run `huggingface-cli login` in the terminal before loading the model. Or just try it in our [chatbot app](https://chat.petals.dev).
 
-🔏 Your data will be processed by other people in the public swarm. Learn more about privacy [here](https://github.com/bigscience-workshop/petals/wiki/Security,-privacy,-and-AI-safety). For sensitive data, you can set up a [private swarm](https://github.com/bigscience-workshop/petals/wiki/Launch-your-own-swarm) among people you trust.
+📋 **Terms of use.** Make sure you follow the model license (see the ones for [LLaMA 2](https://bit.ly/llama2-license), [LLaMA](https://bit.ly/llama-license) and [BLOOM](https://bit.ly/bloom-license)).
+
+🔏 **Privacy.** Your data will be processed by other people in the public swarm. Learn more about privacy [here](https://github.com/bigscience-workshop/petals/wiki/Security,-privacy,-and-AI-safety). For sensitive data, you can set up a [private swarm](https://github.com/bigscience-workshop/petals/wiki/Launch-your-own-swarm) among people you trust.
 
 ### Connect your GPU and increase Petals capacity
 
-Run these commands in an [Anaconda](https://www.anaconda.com) env (requires Linux and Python 3.8+):
+Petals is a community-run system &mdash; we rely on people sharing their GPUs. You can check out available servers on our [swarm monitor](https://health.petals.dev) and connect your GPU to help serving one of the models!
+
+🐍 **Linux + Anaconda.** Run these commands:
 
 ```bash
 conda install pytorch pytorch-cuda=11.7 -c pytorch -c nvidia
-pip install --upgrade petals
+pip install git+https://github.com/bigscience-workshop/petals
 python -m petals.cli.run_server enoch/llama-65b-hf --adapters timdettmers/guanaco-65b
 ```
 
-Or run our [Docker](https://www.docker.com) image (works on Linux, macOS, and Windows with [WSL2](https://learn.microsoft.com/en-us/windows/ai/directml/gpu-cuda-in-wsl)):
+🪟 **Windows + WSL.** Follow the guide on our [Wiki](https://github.com/bigscience-workshop/petals/wiki/Run-Petals-server-on-Windows).
+
+🐋 **Any OS + Docker.** Run our [Docker](https://www.docker.com) image:
 
 ```bash
 sudo docker run -p 31330:31330 --ipc host --gpus all --volume petals-cache:/cache --rm learningathome/petals:main \
     python -m petals.cli.run_server --port 31330 enoch/llama-65b-hf --adapters timdettmers/guanaco-65b
 ```
 
-This will host a part of LLaMA-65B with optional [Guanaco](https://huggingface.co/timdettmers/guanaco-65b) adapters on your machine. You can also host `meta-llama/Llama-2-70b-hf`, `meta-llama/Llama-2-70b-chat-hf`, `bigscience/bloom`, `bigscience/bloomz`, and other compatible models from 🤗 [Model Hub](https://huggingface.co/models), or [add support](https://github.com/bigscience-workshop/petals/wiki/Run-a-custom-model-with-Petals) for new model architectures.
+These commands host a part of LLaMA-65B with optional [Guanaco](https://huggingface.co/timdettmers/guanaco-65b) adapters on your machine. You can also host `meta-llama/Llama-2-70b-hf`, `meta-llama/Llama-2-70b-chat-hf`, `bigscience/bloom`, `bigscience/bloomz`, and other compatible models from 🤗 [Model Hub](https://huggingface.co/models), or [add support](https://github.com/bigscience-workshop/petals/wiki/Run-a-custom-model-with-Petals) for new model architectures.
+
+🦙 **Want to host LLaMA 2?** Request access to its weights at the ♾️ [Meta AI website](https://ai.meta.com/resources/models-and-libraries/llama-downloads/) and 🤗 [Model Hub](https://huggingface.co/meta-llama/Llama-2-70b-hf), generate an 🔑 [access token](https://huggingface.co/settings/tokens), then use this command for `petals.cli.run_server`:
+
+```bash
+python -m petals.cli.run_server meta-llama/Llama-2-70b-chat-hf --token YOUR_TOKEN_HERE
+```
+
+💬 **FAQ.** Check out our [Wiki](https://github.com/bigscience-workshop/petals/wiki/FAQ:-Frequently-asked-questions#running-a-server) to learn how to use multple GPUs, restart the server on reboot, etc. If you have any issues or feedback, ping us in [our Discord](https://discord.gg/D9MwApKgWa)!
 
-🔒 Hosting a server does not allow others to run custom code on your computer. Learn more about security [here](https://github.com/bigscience-workshop/petals/wiki/Security,-privacy,-and-AI-safety).
+🔒 **Security.** Hosting a server does not allow others to run custom code on your computer. Learn more [here](https://github.com/bigscience-workshop/petals/wiki/Security,-privacy,-and-AI-safety).
 
-💬 See [FAQ](https://github.com/bigscience-workshop/petals/wiki/FAQ:-Frequently-asked-questions#running-a-server) to learn how to use multple GPUs, restart the server on reboot, etc. If you have any issues or feedback, ping us in [our Discord](https://discord.gg/D9MwApKgWa)!
+🏆 **Thank you!** Once you load and host 10+ blocks, we can show your name or link on the [swarm monitor](https://health.petals.dev) as a way to say thanks. You can specify them with `--public_name YOUR_NAME`.
 
 ### Check out tutorials, examples, and more
 
 Basic tutorials:
 
 - Getting started: [tutorial](https://colab.research.google.com/drive/1uCphNY7gfAUkdDrTx21dZZwCOUDCMPw8?usp=sharing)
 - Prompt-tune LLaMA-65B for text semantic classification: [tutorial](https://colab.research.google.com/github/bigscience-workshop/petals/blob/main/examples/prompt-tuning-sst2.ipynb)
@@ -120,15 +134,15 @@
 
 ## Installation
 
 Here's how to install Petals with [Anaconda](https://www.anaconda.com/products/distribution) on Linux:
 
 ```bash
 conda install pytorch pytorch-cuda=11.7 -c pytorch -c nvidia
-pip install --upgrade petals
+pip install git+https://github.com/bigscience-workshop/petals
 ```
 
 If you don't use Anaconda, you can install PyTorch in [any other way](https://pytorch.org/get-started/locally/). If you want to run models with 8-bit weights, please install PyTorch with CUDA 11.x or newer for compatility with [bitsandbytes](https://github.com/timDettmers/bitsandbytes).
 
 See the instructions for macOS and Windows, the full requirements, and troubleshooting advice in our [FAQ](https://github.com/bigscience-workshop/petals/wiki/FAQ:-Frequently-asked-questions#running-a-client).
 
 ## Benchmarks
```

#### html2text {}

```diff
@@ -1,22 +1,22 @@
-Metadata-Version: 2.1 Name: petals Version: 2.0.0.post3 Summary: Easy way to
+Metadata-Version: 2.1 Name: petals Version: 2.0.1 Summary: Easy way to
 efficiently run 100B+ language models without high-end GPUs Home-page: https://
 github.com/bigscience-workshop/petals Author: Petals Developers Author-email:
 petals-devs@googlegroups.com Project-URL: Bug Tracker, https://github.com/
 bigscience-workshop/petals/issues Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers Classifier: Intended Audience ::
 Science/Research Classifier: License :: OSI Approved :: MIT License Classifier:
 Programming Language :: Python :: 3 Classifier: Programming Language :: Python
 :: 3.8 Classifier: Programming Language :: Python :: 3.9 Classifier:
 Programming Language :: Python :: 3.10 Classifier: Topic :: Scientific/
 Engineering Classifier: Topic :: Scientific/Engineering :: Mathematics
 Classifier: Topic :: Scientific/Engineering :: Artificial Intelligence
 Classifier: Topic :: Software Development Classifier: Topic :: Software
 Development :: Libraries Classifier: Topic :: Software Development :: Libraries
-:: Python Modules Requires-Python: <3.11,>=3.8 Description-Content-Type: text/
+:: Python Modules Requires-Python: >=3.8 Description-Content-Type: text/
 markdown Provides-Extra: dev License-File: LICENSE
                        [https://i.imgur.com/7eR7Pan.png]
              Run large language models at home, BitTorrent-style.
           Fine-tuning and inference up_to_10x_faster than offloading
 
             [https://img.shields.io/pypi/v/petals.svg?color=green]
 Generate text with distributed [LLaMA 2](https://ai.meta.com/llama/) ([70B]
@@ -32,44 +32,61 @@
 bloomz" tokenizer = AutoTokenizer.from_pretrained(model_name) model =
 AutoDistributedModelForCausalLM.from_pretrained(model_name) # Embeddings &
 prompts are on your device, transformer blocks are distributed across the
 Internet inputs = tokenizer("A cat sat", return_tensors="pt")["input_ids"]
 outputs = model.generate(inputs, max_new_tokens=5) print(tokenizer.decode
 (outputs[0])) # A cat sat on a mat... ```
                             ð  Try_now_in_Colab
-ð Make sure you follow the model's terms of use (see [LLaMA 2](https://
+ð¦ **Want to run LLaMA 2?** Request access to its weights at the â¾ï¸ [Meta
+AI website](https://ai.meta.com/resources/models-and-libraries/llama-downloads/
+) and ð¤ [Model Hub](https://huggingface.co/meta-llama/Llama-2-70b-hf), then
+run `huggingface-cli login` in the terminal before loading the model. Or just
+try it in our [chatbot app](https://chat.petals.dev). ð **Terms of use.**
+Make sure you follow the model license (see the ones for [LLaMA 2](https://
 bit.ly/llama2-license), [LLaMA](https://bit.ly/llama-license) and [BLOOM]
-(https://bit.ly/bloom-license) licenses). ð Your data will be processed by
-other people in the public swarm. Learn more about privacy [here](https://
+(https://bit.ly/bloom-license)). ð **Privacy.** Your data will be processed
+by other people in the public swarm. Learn more about privacy [here](https://
 github.com/bigscience-workshop/petals/wiki/Security,-privacy,-and-AI-safety).
 For sensitive data, you can set up a [private swarm](https://github.com/
 bigscience-workshop/petals/wiki/Launch-your-own-swarm) among people you trust.
-### Connect your GPU and increase Petals capacity Run these commands in an
-[Anaconda](https://www.anaconda.com) env (requires Linux and Python 3.8+):
-```bash conda install pytorch pytorch-cuda=11.7 -c pytorch -c nvidia pip
-install --upgrade petals python -m petals.cli.run_server enoch/llama-65b-hf --
-adapters timdettmers/guanaco-65b ``` Or run our [Docker](https://
-www.docker.com) image (works on Linux, macOS, and Windows with [WSL2](https://
-learn.microsoft.com/en-us/windows/ai/directml/gpu-cuda-in-wsl)): ```bash sudo
-docker run -p 31330:31330 --ipc host --gpus all --volume petals-cache:/cache --
-rm learningathome/petals:main \ python -m petals.cli.run_server --port 31330
-enoch/llama-65b-hf --adapters timdettmers/guanaco-65b ``` This will host a part
-of LLaMA-65B with optional [Guanaco](https://huggingface.co/timdettmers/
+### Connect your GPU and increase Petals capacity Petals is a community-run
+system — we rely on people sharing their GPUs. You can check out available
+servers on our [swarm monitor](https://health.petals.dev) and connect your GPU
+to help serving one of the models! ð **Linux + Anaconda.** Run these
+commands: ```bash conda install pytorch pytorch-cuda=11.7 -c pytorch -c nvidia
+pip install git+https://github.com/bigscience-workshop/petals python -
+m petals.cli.run_server enoch/llama-65b-hf --adapters timdettmers/guanaco-65b
+``` ðª **Windows + WSL.** Follow the guide on our [Wiki](https://github.com/
+bigscience-workshop/petals/wiki/Run-Petals-server-on-Windows). ð **Any OS +
+Docker.** Run our [Docker](https://www.docker.com) image: ```bash sudo docker
+run -p 31330:31330 --ipc host --gpus all --volume petals-cache:/cache --rm
+learningathome/petals:main \ python -m petals.cli.run_server --port 31330
+enoch/llama-65b-hf --adapters timdettmers/guanaco-65b ``` These commands host a
+part of LLaMA-65B with optional [Guanaco](https://huggingface.co/timdettmers/
 guanaco-65b) adapters on your machine. You can also host `meta-llama/Llama-2-
 70b-hf`, `meta-llama/Llama-2-70b-chat-hf`, `bigscience/bloom`, `bigscience/
 bloomz`, and other compatible models from ð¤ [Model Hub](https://
 huggingface.co/models), or [add support](https://github.com/bigscience-
 workshop/petals/wiki/Run-a-custom-model-with-Petals) for new model
-architectures. ð Hosting a server does not allow others to run custom code
-on your computer. Learn more about security [here](https://github.com/
-bigscience-workshop/petals/wiki/Security,-privacy,-and-AI-safety). ð¬ See
-[FAQ](https://github.com/bigscience-workshop/petals/wiki/FAQ:-Frequently-asked-
-questions#running-a-server) to learn how to use multple GPUs, restart the
-server on reboot, etc. If you have any issues or feedback, ping us in [our
-Discord](https://discord.gg/D9MwApKgWa)! ### Check out tutorials, examples, and
+architectures. ð¦ **Want to host LLaMA 2?** Request access to its weights at
+the â¾ï¸ [Meta AI website](https://ai.meta.com/resources/models-and-
+libraries/llama-downloads/) and ð¤ [Model Hub](https://huggingface.co/meta-
+llama/Llama-2-70b-hf), generate an ð [access token](https://huggingface.co/
+settings/tokens), then use this command for `petals.cli.run_server`: ```bash
+python -m petals.cli.run_server meta-llama/Llama-2-70b-chat-hf --token
+YOUR_TOKEN_HERE ``` ð¬ **FAQ.** Check out our [Wiki](https://github.com/
+bigscience-workshop/petals/wiki/FAQ:-Frequently-asked-questions#running-a-
+server) to learn how to use multple GPUs, restart the server on reboot, etc. If
+you have any issues or feedback, ping us in [our Discord](https://discord.gg/
+D9MwApKgWa)! ð **Security.** Hosting a server does not allow others to run
+custom code on your computer. Learn more [here](https://github.com/bigscience-
+workshop/petals/wiki/Security,-privacy,-and-AI-safety). ð **Thank you!**
+Once you load and host 10+ blocks, we can show your name or link on the [swarm
+monitor](https://health.petals.dev) as a way to say thanks. You can specify
+them with `--public_name YOUR_NAME`. ### Check out tutorials, examples, and
 more Basic tutorials: - Getting started: [tutorial](https://
 colab.research.google.com/drive/1uCphNY7gfAUkdDrTx21dZZwCOUDCMPw8?usp=sharing)
 - Prompt-tune LLaMA-65B for text semantic classification: [tutorial](https://
 colab.research.google.com/github/bigscience-workshop/petals/blob/main/examples/
 prompt-tuning-sst2.ipynb) - Prompt-tune BLOOM to create a personified chatbot:
 [tutorial](https://colab.research.google.com/github/bigscience-workshop/petals/
 blob/main/examples/prompt-tuning-personachat.ipynb) Useful tools and advanced
@@ -95,23 +112,23 @@
 any fine-tuning and sampling methods, execute custom paths through the model,
 or see its hidden states. You get the comforts of an API with the flexibility
 of PyTorch.
                        [https://i.imgur.com/RTYF3yW.png]
                    ð  See_FAQ            ð  Read_paper
 ## Installation Here's how to install Petals with [Anaconda](https://
 www.anaconda.com/products/distribution) on Linux: ```bash conda install pytorch
-pytorch-cuda=11.7 -c pytorch -c nvidia pip install --upgrade petals ``` If you
-don't use Anaconda, you can install PyTorch in [any other way](https://
-pytorch.org/get-started/locally/). If you want to run models with 8-bit
-weights, please install PyTorch with CUDA 11.x or newer for compatility with
-[bitsandbytes](https://github.com/timDettmers/bitsandbytes). See the
-instructions for macOS and Windows, the full requirements, and troubleshooting
-advice in our [FAQ](https://github.com/bigscience-workshop/petals/wiki/FAQ:-
-Frequently-asked-questions#running-a-client). ## Benchmarks The benchmarks
-below are for BLOOM-176B:
+pytorch-cuda=11.7 -c pytorch -c nvidia pip install git+https://github.com/
+bigscience-workshop/petals ``` If you don't use Anaconda, you can install
+PyTorch in [any other way](https://pytorch.org/get-started/locally/). If you
+want to run models with 8-bit weights, please install PyTorch with CUDA 11.x or
+newer for compatility with [bitsandbytes](https://github.com/timDettmers/
+bitsandbytes). See the instructions for macOS and Windows, the full
+requirements, and troubleshooting advice in our [FAQ](https://github.com/
+bigscience-workshop/petals/wiki/FAQ:-Frequently-asked-questions#running-a-
+client). ## Benchmarks The benchmarks below are for BLOOM-176B:
      Network               Single-batch inference Parallel forward
                            (steps/s)              (tokens/s)
      Bandwidth  Round-trip Sequence length        Batch size
                 latency    128           2048       1              64
      Offloading, max. possible speed on 1x A100 1
      256 Gbit/s            0.18          0.18     2.7           170.3
      128 Gbit/s            0.09          0.09     2.4           152.8
```

### Comparing `petals-2.0.0.post3/README.md` & `petals-2.0.1/README.md`

 * *Files 4% similar despite different names*

```diff
@@ -24,40 +24,54 @@
 print(tokenizer.decode(outputs[0]))  # A cat sat on a mat...
 ```
 
 <p align="center">
     🚀 &nbsp;<b><a href="https://colab.research.google.com/drive/1uCphNY7gfAUkdDrTx21dZZwCOUDCMPw8?usp=sharing">Try now in Colab</a></b>
 </p>
 
-📋 Make sure you follow the model's terms of use (see [LLaMA 2](https://bit.ly/llama2-license), [LLaMA](https://bit.ly/llama-license) and [BLOOM](https://bit.ly/bloom-license) licenses).
+🦙 **Want to run LLaMA 2?** Request access to its weights at the ♾️ [Meta AI website](https://ai.meta.com/resources/models-and-libraries/llama-downloads/) and 🤗 [Model Hub](https://huggingface.co/meta-llama/Llama-2-70b-hf), then run `huggingface-cli login` in the terminal before loading the model. Or just try it in our [chatbot app](https://chat.petals.dev).
 
-🔏 Your data will be processed by other people in the public swarm. Learn more about privacy [here](https://github.com/bigscience-workshop/petals/wiki/Security,-privacy,-and-AI-safety). For sensitive data, you can set up a [private swarm](https://github.com/bigscience-workshop/petals/wiki/Launch-your-own-swarm) among people you trust.
+📋 **Terms of use.** Make sure you follow the model license (see the ones for [LLaMA 2](https://bit.ly/llama2-license), [LLaMA](https://bit.ly/llama-license) and [BLOOM](https://bit.ly/bloom-license)).
+
+🔏 **Privacy.** Your data will be processed by other people in the public swarm. Learn more about privacy [here](https://github.com/bigscience-workshop/petals/wiki/Security,-privacy,-and-AI-safety). For sensitive data, you can set up a [private swarm](https://github.com/bigscience-workshop/petals/wiki/Launch-your-own-swarm) among people you trust.
 
 ### Connect your GPU and increase Petals capacity
 
-Run these commands in an [Anaconda](https://www.anaconda.com) env (requires Linux and Python 3.8+):
+Petals is a community-run system &mdash; we rely on people sharing their GPUs. You can check out available servers on our [swarm monitor](https://health.petals.dev) and connect your GPU to help serving one of the models!
+
+🐍 **Linux + Anaconda.** Run these commands:
 
 ```bash
 conda install pytorch pytorch-cuda=11.7 -c pytorch -c nvidia
-pip install --upgrade petals
+pip install git+https://github.com/bigscience-workshop/petals
 python -m petals.cli.run_server enoch/llama-65b-hf --adapters timdettmers/guanaco-65b
 ```
 
-Or run our [Docker](https://www.docker.com) image (works on Linux, macOS, and Windows with [WSL2](https://learn.microsoft.com/en-us/windows/ai/directml/gpu-cuda-in-wsl)):
+🪟 **Windows + WSL.** Follow the guide on our [Wiki](https://github.com/bigscience-workshop/petals/wiki/Run-Petals-server-on-Windows).
+
+🐋 **Any OS + Docker.** Run our [Docker](https://www.docker.com) image:
 
 ```bash
 sudo docker run -p 31330:31330 --ipc host --gpus all --volume petals-cache:/cache --rm learningathome/petals:main \
     python -m petals.cli.run_server --port 31330 enoch/llama-65b-hf --adapters timdettmers/guanaco-65b
 ```
 
-This will host a part of LLaMA-65B with optional [Guanaco](https://huggingface.co/timdettmers/guanaco-65b) adapters on your machine. You can also host `meta-llama/Llama-2-70b-hf`, `meta-llama/Llama-2-70b-chat-hf`, `bigscience/bloom`, `bigscience/bloomz`, and other compatible models from 🤗 [Model Hub](https://huggingface.co/models), or [add support](https://github.com/bigscience-workshop/petals/wiki/Run-a-custom-model-with-Petals) for new model architectures.
+These commands host a part of LLaMA-65B with optional [Guanaco](https://huggingface.co/timdettmers/guanaco-65b) adapters on your machine. You can also host `meta-llama/Llama-2-70b-hf`, `meta-llama/Llama-2-70b-chat-hf`, `bigscience/bloom`, `bigscience/bloomz`, and other compatible models from 🤗 [Model Hub](https://huggingface.co/models), or [add support](https://github.com/bigscience-workshop/petals/wiki/Run-a-custom-model-with-Petals) for new model architectures.
+
+🦙 **Want to host LLaMA 2?** Request access to its weights at the ♾️ [Meta AI website](https://ai.meta.com/resources/models-and-libraries/llama-downloads/) and 🤗 [Model Hub](https://huggingface.co/meta-llama/Llama-2-70b-hf), generate an 🔑 [access token](https://huggingface.co/settings/tokens), then use this command for `petals.cli.run_server`:
+
+```bash
+python -m petals.cli.run_server meta-llama/Llama-2-70b-chat-hf --token YOUR_TOKEN_HERE
+```
+
+💬 **FAQ.** Check out our [Wiki](https://github.com/bigscience-workshop/petals/wiki/FAQ:-Frequently-asked-questions#running-a-server) to learn how to use multple GPUs, restart the server on reboot, etc. If you have any issues or feedback, ping us in [our Discord](https://discord.gg/D9MwApKgWa)!
 
-🔒 Hosting a server does not allow others to run custom code on your computer. Learn more about security [here](https://github.com/bigscience-workshop/petals/wiki/Security,-privacy,-and-AI-safety).
+🔒 **Security.** Hosting a server does not allow others to run custom code on your computer. Learn more [here](https://github.com/bigscience-workshop/petals/wiki/Security,-privacy,-and-AI-safety).
 
-💬 See [FAQ](https://github.com/bigscience-workshop/petals/wiki/FAQ:-Frequently-asked-questions#running-a-server) to learn how to use multple GPUs, restart the server on reboot, etc. If you have any issues or feedback, ping us in [our Discord](https://discord.gg/D9MwApKgWa)!
+🏆 **Thank you!** Once you load and host 10+ blocks, we can show your name or link on the [swarm monitor](https://health.petals.dev) as a way to say thanks. You can specify them with `--public_name YOUR_NAME`.
 
 ### Check out tutorials, examples, and more
 
 Basic tutorials:
 
 - Getting started: [tutorial](https://colab.research.google.com/drive/1uCphNY7gfAUkdDrTx21dZZwCOUDCMPw8?usp=sharing)
 - Prompt-tune LLaMA-65B for text semantic classification: [tutorial](https://colab.research.google.com/github/bigscience-workshop/petals/blob/main/examples/prompt-tuning-sst2.ipynb)
@@ -93,15 +107,15 @@
 
 ## Installation
 
 Here's how to install Petals with [Anaconda](https://www.anaconda.com/products/distribution) on Linux:
 
 ```bash
 conda install pytorch pytorch-cuda=11.7 -c pytorch -c nvidia
-pip install --upgrade petals
+pip install git+https://github.com/bigscience-workshop/petals
 ```
 
 If you don't use Anaconda, you can install PyTorch in [any other way](https://pytorch.org/get-started/locally/). If you want to run models with 8-bit weights, please install PyTorch with CUDA 11.x or newer for compatility with [bitsandbytes](https://github.com/timDettmers/bitsandbytes).
 
 See the instructions for macOS and Windows, the full requirements, and troubleshooting advice in our [FAQ](https://github.com/bigscience-workshop/petals/wiki/FAQ:-Frequently-asked-questions#running-a-client).
 
 ## Benchmarks
```

#### html2text {}

```diff
@@ -16,44 +16,61 @@
 bloomz" tokenizer = AutoTokenizer.from_pretrained(model_name) model =
 AutoDistributedModelForCausalLM.from_pretrained(model_name) # Embeddings &
 prompts are on your device, transformer blocks are distributed across the
 Internet inputs = tokenizer("A cat sat", return_tensors="pt")["input_ids"]
 outputs = model.generate(inputs, max_new_tokens=5) print(tokenizer.decode
 (outputs[0])) # A cat sat on a mat... ```
                             ð  Try_now_in_Colab
-ð Make sure you follow the model's terms of use (see [LLaMA 2](https://
+ð¦ **Want to run LLaMA 2?** Request access to its weights at the â¾ï¸ [Meta
+AI website](https://ai.meta.com/resources/models-and-libraries/llama-downloads/
+) and ð¤ [Model Hub](https://huggingface.co/meta-llama/Llama-2-70b-hf), then
+run `huggingface-cli login` in the terminal before loading the model. Or just
+try it in our [chatbot app](https://chat.petals.dev). ð **Terms of use.**
+Make sure you follow the model license (see the ones for [LLaMA 2](https://
 bit.ly/llama2-license), [LLaMA](https://bit.ly/llama-license) and [BLOOM]
-(https://bit.ly/bloom-license) licenses). ð Your data will be processed by
-other people in the public swarm. Learn more about privacy [here](https://
+(https://bit.ly/bloom-license)). ð **Privacy.** Your data will be processed
+by other people in the public swarm. Learn more about privacy [here](https://
 github.com/bigscience-workshop/petals/wiki/Security,-privacy,-and-AI-safety).
 For sensitive data, you can set up a [private swarm](https://github.com/
 bigscience-workshop/petals/wiki/Launch-your-own-swarm) among people you trust.
-### Connect your GPU and increase Petals capacity Run these commands in an
-[Anaconda](https://www.anaconda.com) env (requires Linux and Python 3.8+):
-```bash conda install pytorch pytorch-cuda=11.7 -c pytorch -c nvidia pip
-install --upgrade petals python -m petals.cli.run_server enoch/llama-65b-hf --
-adapters timdettmers/guanaco-65b ``` Or run our [Docker](https://
-www.docker.com) image (works on Linux, macOS, and Windows with [WSL2](https://
-learn.microsoft.com/en-us/windows/ai/directml/gpu-cuda-in-wsl)): ```bash sudo
-docker run -p 31330:31330 --ipc host --gpus all --volume petals-cache:/cache --
-rm learningathome/petals:main \ python -m petals.cli.run_server --port 31330
-enoch/llama-65b-hf --adapters timdettmers/guanaco-65b ``` This will host a part
-of LLaMA-65B with optional [Guanaco](https://huggingface.co/timdettmers/
+### Connect your GPU and increase Petals capacity Petals is a community-run
+system — we rely on people sharing their GPUs. You can check out available
+servers on our [swarm monitor](https://health.petals.dev) and connect your GPU
+to help serving one of the models! ð **Linux + Anaconda.** Run these
+commands: ```bash conda install pytorch pytorch-cuda=11.7 -c pytorch -c nvidia
+pip install git+https://github.com/bigscience-workshop/petals python -
+m petals.cli.run_server enoch/llama-65b-hf --adapters timdettmers/guanaco-65b
+``` ðª **Windows + WSL.** Follow the guide on our [Wiki](https://github.com/
+bigscience-workshop/petals/wiki/Run-Petals-server-on-Windows). ð **Any OS +
+Docker.** Run our [Docker](https://www.docker.com) image: ```bash sudo docker
+run -p 31330:31330 --ipc host --gpus all --volume petals-cache:/cache --rm
+learningathome/petals:main \ python -m petals.cli.run_server --port 31330
+enoch/llama-65b-hf --adapters timdettmers/guanaco-65b ``` These commands host a
+part of LLaMA-65B with optional [Guanaco](https://huggingface.co/timdettmers/
 guanaco-65b) adapters on your machine. You can also host `meta-llama/Llama-2-
 70b-hf`, `meta-llama/Llama-2-70b-chat-hf`, `bigscience/bloom`, `bigscience/
 bloomz`, and other compatible models from ð¤ [Model Hub](https://
 huggingface.co/models), or [add support](https://github.com/bigscience-
 workshop/petals/wiki/Run-a-custom-model-with-Petals) for new model
-architectures. ð Hosting a server does not allow others to run custom code
-on your computer. Learn more about security [here](https://github.com/
-bigscience-workshop/petals/wiki/Security,-privacy,-and-AI-safety). ð¬ See
-[FAQ](https://github.com/bigscience-workshop/petals/wiki/FAQ:-Frequently-asked-
-questions#running-a-server) to learn how to use multple GPUs, restart the
-server on reboot, etc. If you have any issues or feedback, ping us in [our
-Discord](https://discord.gg/D9MwApKgWa)! ### Check out tutorials, examples, and
+architectures. ð¦ **Want to host LLaMA 2?** Request access to its weights at
+the â¾ï¸ [Meta AI website](https://ai.meta.com/resources/models-and-
+libraries/llama-downloads/) and ð¤ [Model Hub](https://huggingface.co/meta-
+llama/Llama-2-70b-hf), generate an ð [access token](https://huggingface.co/
+settings/tokens), then use this command for `petals.cli.run_server`: ```bash
+python -m petals.cli.run_server meta-llama/Llama-2-70b-chat-hf --token
+YOUR_TOKEN_HERE ``` ð¬ **FAQ.** Check out our [Wiki](https://github.com/
+bigscience-workshop/petals/wiki/FAQ:-Frequently-asked-questions#running-a-
+server) to learn how to use multple GPUs, restart the server on reboot, etc. If
+you have any issues or feedback, ping us in [our Discord](https://discord.gg/
+D9MwApKgWa)! ð **Security.** Hosting a server does not allow others to run
+custom code on your computer. Learn more [here](https://github.com/bigscience-
+workshop/petals/wiki/Security,-privacy,-and-AI-safety). ð **Thank you!**
+Once you load and host 10+ blocks, we can show your name or link on the [swarm
+monitor](https://health.petals.dev) as a way to say thanks. You can specify
+them with `--public_name YOUR_NAME`. ### Check out tutorials, examples, and
 more Basic tutorials: - Getting started: [tutorial](https://
 colab.research.google.com/drive/1uCphNY7gfAUkdDrTx21dZZwCOUDCMPw8?usp=sharing)
 - Prompt-tune LLaMA-65B for text semantic classification: [tutorial](https://
 colab.research.google.com/github/bigscience-workshop/petals/blob/main/examples/
 prompt-tuning-sst2.ipynb) - Prompt-tune BLOOM to create a personified chatbot:
 [tutorial](https://colab.research.google.com/github/bigscience-workshop/petals/
 blob/main/examples/prompt-tuning-personachat.ipynb) Useful tools and advanced
@@ -79,23 +96,23 @@
 any fine-tuning and sampling methods, execute custom paths through the model,
 or see its hidden states. You get the comforts of an API with the flexibility
 of PyTorch.
                        [https://i.imgur.com/RTYF3yW.png]
                    ð  See_FAQ            ð  Read_paper
 ## Installation Here's how to install Petals with [Anaconda](https://
 www.anaconda.com/products/distribution) on Linux: ```bash conda install pytorch
-pytorch-cuda=11.7 -c pytorch -c nvidia pip install --upgrade petals ``` If you
-don't use Anaconda, you can install PyTorch in [any other way](https://
-pytorch.org/get-started/locally/). If you want to run models with 8-bit
-weights, please install PyTorch with CUDA 11.x or newer for compatility with
-[bitsandbytes](https://github.com/timDettmers/bitsandbytes). See the
-instructions for macOS and Windows, the full requirements, and troubleshooting
-advice in our [FAQ](https://github.com/bigscience-workshop/petals/wiki/FAQ:-
-Frequently-asked-questions#running-a-client). ## Benchmarks The benchmarks
-below are for BLOOM-176B:
+pytorch-cuda=11.7 -c pytorch -c nvidia pip install git+https://github.com/
+bigscience-workshop/petals ``` If you don't use Anaconda, you can install
+PyTorch in [any other way](https://pytorch.org/get-started/locally/). If you
+want to run models with 8-bit weights, please install PyTorch with CUDA 11.x or
+newer for compatility with [bitsandbytes](https://github.com/timDettmers/
+bitsandbytes). See the instructions for macOS and Windows, the full
+requirements, and troubleshooting advice in our [FAQ](https://github.com/
+bigscience-workshop/petals/wiki/FAQ:-Frequently-asked-questions#running-a-
+client). ## Benchmarks The benchmarks below are for BLOOM-176B:
      Network               Single-batch inference Parallel forward
                            (steps/s)              (tokens/s)
      Bandwidth  Round-trip Sequence length        Batch size
                 latency    128           2048       1              64
      Offloading, max. possible speed on 1x A100 1
      256 Gbit/s            0.18          0.18     2.7           170.3
      128 Gbit/s            0.09          0.09     2.4           152.8
```

### Comparing `petals-2.0.0.post3/setup.cfg` & `petals-2.0.1/setup.cfg`

 * *Files 4% similar despite different names*

```diff
@@ -25,25 +25,25 @@
 	Topic :: Software Development :: Libraries
 	Topic :: Software Development :: Libraries :: Python Modules
 
 [options]
 package_dir = 
 	= src
 packages = find:
-python_requires = >=3.8,<3.11
+python_requires = >=3.8
 install_requires = 
 	torch>=1.12
 	bitsandbytes==0.40.1.post1
 	accelerate>=0.20.3,<0.21.0
 	huggingface-hub>=0.11.1,<1.0.0
 	tokenizers>=0.13.3
 	transformers>=4.31.0,<5.0.0
 	speedtest-cli==2.1.3
-	pydantic>=1.10,<2.0  # 2.0 is incompatible with hivemind==1.1.8
-	hivemind==1.1.8
+	pydantic>=1.10,<2.0  # 2.0 is incompatible with hivemind yet
+	hivemind==1.1.9
 	tensor_parallel==1.0.23
 	humanfriendly
 	async-timeout>=4.0.2
 	cpufeature>=0.2.0
 	packaging>=20.9
 	sentencepiece>=0.1.99
 	peft>=0.4.0
```

### Comparing `petals-2.0.0.post3/src/petals/__init__.py` & `petals-2.0.1/src/petals/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 from packaging import version
 
 from petals.client import *
 from petals.models import *
 from petals.utils import *
 from petals.utils.logging import initialize_logs as _initialize_logs
 
-__version__ = "2.0.0.post3"
+__version__ = "2.0.1"
 
 
 if not os.getenv("PETALS_IGNORE_DEPENDENCY_VERSION"):
     assert (
         version.parse("4.31.0") <= version.parse(transformers.__version__) < version.parse("5.0.0")
     ), "Please install a proper transformers version: pip install transformers>=4.31.0,<5.0.0"
```

### Comparing `petals-2.0.0.post3/src/petals/cli/run_dht.py` & `petals-2.0.1/src/petals/cli/run_dht.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/cli/run_server.py` & `petals-2.0.1/src/petals/cli/run_server.py`

 * *Files 1% similar despite different names*

```diff
@@ -70,14 +70,16 @@
                         help='Maximum total sequence length permitted per inference, defaults to 16384 tokens. '
                              'Default: 2048 for most models, 8192 for models with multi-query attention (e.g., Llama-2-70b)')
     parser.add_argument('--min_batch_size', type=int, default=1,
                         help='Minimum required batch size for all operations (in total tokens)')
     parser.add_argument('--max_batch_size', type=int, default=None,
                         help='The total number of tokens in the same batch will not exceed this value. '
                              'Default: 2048 for most models, 8192 for models with multi-query attention (e.g., Llama-2-70b)')
+    parser.add_argument('--max_chunk_size_bytes', type=int, default=256 * 1024 * 1024,
+                        help='Maximum size of activation tensor processed in one go; larger tensors are split into chunks')
     parser.add_argument('--attn_cache_tokens', type=int, default=None,
                         help='The number of past attention key/value pairs that will be stored between inference steps. '
                              'Default: 8192 for most models, 32768 for models with multi-query attention (e.g., Llama-2-70b)')
 
     parser.add_argument('--cache_dir', type=str, default=None,
                         help='Path to a directory in which a downloaded pretrained model configuration should be cached if the standard cache should not be used.')
     parser.add_argument("--max_disk_space", type=str, default=None,
@@ -90,29 +92,29 @@
                              "the disk space equal to 2-4x of your GPU memory on average.")
 
     parser.add_argument('--device', type=str, default=None, required=False,
                         help='all blocks will use this device in torch notation; default: cuda if available else cpu')
     parser.add_argument("--torch_dtype", type=str, choices=DTYPE_MAP.keys(), default="auto",
                         help="Use this dtype to store block weights and do computations. "
                              "By default, respect the dtypes in the pre-trained state dict.")
-    parser.add_argument('--alloc_timeout', type=float, default=5,
+    parser.add_argument('--alloc_timeout', type=float, default=1,
                         help='If the cache is full, the server will wait for this number of seconds hoping that some memory will be freed '
                              'before rejecting the request')
     parser.add_argument('--revision', type=str, default=None,
                         help="The specific model version to use. It can be a branch name, a tag name, or a commit id, since we use a git-based system for storing models"
                              "and other artifacts on huggingface.co, so `revision` can be any identifier allowed by git.")
 
     parser.add_argument('--throughput',
                         type=lambda value: value if value in ['auto', 'eval'] else float(value),
                         default='auto',
                         help='Expected server throughput (a float measured in RPS). '
                              'If set to "auto" (default), the script evaluates network and compute throughput '
                              'on the first run and uses these estimates for future runs. '
                              'If set to "eval", the script re-evaluates the throughput and overrides the cache.')
-    parser.add_argument('--update_period', type=float, required=False, default=60,
+    parser.add_argument('--update_period', type=float, required=False, default=120,
                         help='Server will report blocks to DHT once in this many seconds')
     parser.add_argument('--expiration', type=float, required=False, default=None,
                         help='DHT entries will expire after this many seconds')
     parser.add_argument('--request_timeout', type=float, required=False, default=3 * 60,
                         help='Timeout (in seconds) for the whole rpc_forward/rpc_backward/rpc_forward_stream/rpc_backward_stream request')
     parser.add_argument('--session_timeout', type=float, required=False, default=30 * 60,
                         help='Timeout (in seconds) for the whole inference session')
```

### Comparing `petals-2.0.0.post3/src/petals/client/from_pretrained.py` & `petals-2.0.1/src/petals/client/from_pretrained.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/client/inference_session.py` & `petals-2.0.1/src/petals/client/inference_session.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/client/lm_head.py` & `petals-2.0.1/src/petals/client/lm_head.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/client/ptune.py` & `petals-2.0.1/src/petals/client/ptune.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/client/remote_forward_backward.py` & `petals-2.0.1/src/petals/client/remote_forward_backward.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/client/remote_generation.py` & `petals-2.0.1/src/petals/client/remote_generation.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/client/remote_sequential.py` & `petals-2.0.1/src/petals/client/remote_sequential.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/client/routing/sequence_info.py` & `petals-2.0.1/src/petals/client/routing/sequence_info.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/client/routing/sequence_manager.py` & `petals-2.0.1/src/petals/client/routing/sequence_manager.py`

 * *Files 2% similar despite different names*

```diff
@@ -287,23 +287,31 @@
 
         # Here, `span` contains all blocks hosted by a server - but we won't necessarily run all of them through
         # this particular server in our path. It is difficult to estimate how many blocks we'll use at this stage,
         # so we assume that we'll use all of them (the worst case for the cache size) and get a pessimistic estimate.
         # This is okay since false positives are more costly than false negatives here.
         return cache_tokens_needed * 2 * span.length <= span.server_info.cache_tokens_left
 
-    def _make_sequence_with_max_throughput(self, start_index: int, end_index: int) -> List[RemoteSpanInfo]:
+    def _make_sequence_with_max_throughput(
+        self, start_index: int, end_index: int, *, relay_penalty: float = 0.5
+    ) -> List[RemoteSpanInfo]:
         span_sequence = []
         current_index = start_index
         while current_index < end_index:
             candidate_spans = self.state.sequence_info.spans_containing_block[current_index]
             if not candidate_spans:
                 raise MissingBlocksError(current_index)
 
-            span_weights = np.array([span.server_info.throughput for span in candidate_spans], dtype=np.float64)
+            span_weights = np.array(
+                [
+                    span.server_info.throughput * (1 if not span.server_info.using_relay else relay_penalty)
+                    for span in candidate_spans
+                ],
+                dtype=np.float64,
+            )
             chosen_span = np.random.choice(candidate_spans, p=span_weights / span_weights.sum())
 
             assert chosen_span.start <= current_index < chosen_span.end
             span_sequence.append(dataclasses.replace(chosen_span, start=current_index))
             current_index = chosen_span.end
         return span_sequence
```

### Comparing `petals-2.0.0.post3/src/petals/client/routing/spending_policy.py` & `petals-2.0.1/src/petals/client/routing/spending_policy.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/client/sequential_autograd.py` & `petals-2.0.1/src/petals/client/sequential_autograd.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/constants.py` & `petals-2.0.1/src/petals/constants.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/data_structures.py` & `petals-2.0.1/src/petals/data_structures.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/dht_utils.py` & `petals-2.0.1/src/petals/dht_utils.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/models/bloom/__init__.py` & `petals-2.0.1/src/petals/models/bloom/__init__.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/models/bloom/block.py` & `petals-2.0.1/src/petals/models/bloom/block.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/models/bloom/config.py` & `petals-2.0.1/src/petals/models/bloom/config.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/models/bloom/model.py` & `petals-2.0.1/src/petals/models/bloom/model.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/models/llama/__init__.py` & `petals-2.0.1/src/petals/models/llama/__init__.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/models/llama/block.py` & `petals-2.0.1/src/petals/models/llama/block.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/models/llama/config.py` & `petals-2.0.1/src/petals/models/llama/config.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/models/llama/model.py` & `petals-2.0.1/src/petals/models/llama/model.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/server/backend.py` & `petals-2.0.1/src/petals/server/backend.py`

 * *Files 9% similar despite different names*

```diff
@@ -23,24 +23,32 @@
 
 class TransformerBackend(ModuleBackend):
     """A wrapper for a transformer block that can process requests for forward, backward and inference"""
 
     _peft_module = None
 
     def __init__(
-        self, *args, config: PretrainedConfig, memory_cache: MemoryCache, backend_dtype: torch.dtype, **kwargs
+        self,
+        *args,
+        config: PretrainedConfig,
+        memory_cache: MemoryCache,
+        backend_dtype: torch.dtype,
+        max_chunk_size_bytes: int,
+        **kwargs,
     ):
         import petals.utils.peft as _peft_module
 
         self._peft_module = _peft_module
 
         super().__init__(*args, **kwargs)
         assert isinstance(self.module, TensorParallel)
         self.config = config
         self.memory_cache = memory_cache
+        self.max_chunk_size_bytes = max_chunk_size_bytes
+
         for name, param in self.module.named_parameters():
             assert not param.requires_grad, f"Block parameters must not accumulate gradients, but {name} does"
         for name, buf in self.module.named_buffers():
             assert not buf.requires_grad, f"Block parameters must not accumulate gradients, but {name} does"
 
         max_batch_size = self.forward_pool.max_batch_size
         device = self.module.devices[self.module.output_device_index]
@@ -51,14 +59,15 @@
             self.forward, max_batch_size=max_batch_size, device=device, name=f"{self.name}_forward"
         )
         self.backward_pool = PrioritizedTaskPool(
             self.backward, max_batch_size=max_batch_size, device=device, name=f"{self.name}_backward"
         )
 
         self.dtype = backend_dtype
+        self.dtype_bytes = torch.finfo(self.dtype).bits // 8
         self.shard_num_heads = []
         for shard in self.module.module_shards:
             for submodule in shard.modules():
                 if isinstance(submodule, config.attn_class):
                     self.shard_num_heads.append(submodule.num_heads)
         assert len(self.shard_num_heads) == len(self.module.devices)
         assert sum(self.shard_num_heads) == config.num_attention_heads
@@ -101,22 +110,48 @@
     def inference_step(
         self,
         hidden_states: torch.Tensor,
         hypo_ids: torch.LongTensor,
         inference_info: InferenceMetadata,
     ) -> Tuple[torch.Tensor, ...]:
         assert hidden_states.ndim == 3, "expected hidden states to be 3-dimensional: [batch_size, seq_len, hid_size]"
+        seq_len = hidden_states.shape[1]
+
         with self.memory_cache.use_cache(
             *inference_info.cache_handles
         ) as cache_tensors, self._peft_module.using_adapter(inference_info.active_adapter):
             self._reorder_cache_inplace(cache_tensors, hypo_ids)
+
+            # We chunk the inputs so that peak memory for long sequences fits into `autograd_memory`
+            # reserved in `Server._choose_num_blocks()`. This saves us from OOMs if `max_chunk_size_bytes`
+            # is at least 4-6x less than `autograd_memory`.
+            max_chunk_length = self._estimate_max_chunk_length(hidden_states, inference_info)
+            output_hidden_states = torch.empty_like(hidden_states) if seq_len > max_chunk_length else None
             layer_past = self._select_layer_past(cache_tensors, inference_info.prefix_length)
-            hidden_states, new_kvs = self.module.forward(hidden_states, layer_past=layer_past, use_cache=True)
+            for offset in range(0, seq_len, max_chunk_length):
+                hidden_states_chunk = hidden_states[:, offset : offset + max_chunk_length, :]
+                output_hidden_states_chunk, new_kvs = self.module.forward(
+                    hidden_states_chunk, layer_past=layer_past, use_cache=True
+                )
+                if seq_len > max_chunk_length:
+                    output_hidden_states[:, offset : offset + max_chunk_length] = output_hidden_states_chunk
+                else:
+                    output_hidden_states = output_hidden_states_chunk  # saves one memcopy
+                layer_past = new_kvs
+
             self._update_cache_inplace(cache_tensors, new_kvs, inference_info.prefix_length)
-            return (hidden_states,)
+            return (output_hidden_states,)
+
+    def _estimate_max_chunk_length(self, hidden_states: torch.Tensor, inference_info: InferenceMetadata) -> int:
+        # We assume that attention logit matrices are the main thing that consumes memory, given that
+        # the model uses multi-query attention
+        batch_size, seq_length, hidden_size = hidden_states.shape
+        worst_case_length = inference_info.prefix_length + seq_length
+        attn_bytes_per_token = max(self.shard_num_heads) * batch_size * self.dtype_bytes * worst_case_length
+        return max(1, self.max_chunk_size_bytes // attn_bytes_per_token)
 
     def _reorder_cache_inplace(self, cache_tensors: torch.Tensor, hypo_ids: torch.Tensor):
         """If hypo_ids is specified, reorder elements of each cache tensor in-place by taking indices from hypo_ids"""
         if not is_dummy(hypo_ids):
             for cache_tensor in cache_tensors:
                 cache_tensor[...] = cache_tensor[hypo_ids.to(cache_tensor.device)]  # in-place reorder cache by hypo ids
```

### Comparing `petals-2.0.0.post3/src/petals/server/block_selection.py` & `petals-2.0.1/src/petals/server/block_selection.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/server/block_utils.py` & `petals-2.0.1/src/petals/server/block_utils.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/server/from_pretrained.py` & `petals-2.0.1/src/petals/server/from_pretrained.py`

 * *Files 1% similar despite different names*

```diff
@@ -36,15 +36,15 @@
     torch_dtype: Union[torch.dtype, str] = "auto",
     revision: Optional[str] = None,
     token: Optional[Union[str, bool]] = None,
     cache_dir: Optional[str] = None,
     max_disk_space: Optional[int] = None,
 ) -> nn.Module:
     if config is None:
-        config = AutoDistributedConfig.from_pretrained(model_name, token=token)
+        config = AutoDistributedConfig.from_pretrained(model_name, use_auth_token=token)
     if cache_dir is None:
         cache_dir = DEFAULT_CACHE_DIR
 
     assert torch_dtype in DTYPE_MAP.values(), f"torch_dtype must be one of {list(DTYPE_MAP.values())}"
     torch_dtype = resolve_block_dtype(config, torch_dtype)
 
     with init_empty_weights():
```

### Comparing `petals-2.0.0.post3/src/petals/server/handler.py` & `petals-2.0.1/src/petals/server/handler.py`

 * *Files 0% similar despite different names*

```diff
@@ -343,15 +343,15 @@
                         request = await get_push_task
                         get_push_task = None
                     else:
                         self._log_request("rpc_inference.step", requested_uids, context, warning="timed out")
                         anext_task.cancel()
                         get_push_task.cancel()
                         return
-        except:
+        except Exception:
             logger.warning("rpc_inference._iterate_inference_steps() exception:", exc_info=True)
             raise
 
     async def rpc_push(self, request: runtime_pb2.ExpertRequest, context: P2PContext) -> runtime_pb2.ExpertResponse:
         """Directly push activation tensors from one server to another"""
 
         requested_uids = self._check_uids(request.uid)
```

### Comparing `petals-2.0.0.post3/src/petals/server/memory_cache.py` & `petals-2.0.1/src/petals/server/memory_cache.py`

 * *Files 3% similar despite different names*

```diff
@@ -86,15 +86,15 @@
 
         alloc_task = asyncio.create_task(self._schedule_alloc(max_alloc_size, *descriptors))
         try:
             handles = await shield_and_wait(alloc_task)
             logger.info(f"rpc_inference.alloc(size={max_alloc_size / gib:.2f} GiB)")
             yield handles
         finally:
-            await shield_and_wait(self._schedule_free(max_alloc_size, alloc_task))
+            self._free(max_alloc_size, alloc_task)
 
     @staticmethod
     def get_allocation_size(*descriptors: TensorDescriptor) -> int:
         """Return the memory size (bytes) to be allocated on a device. If there are many devices, return maximum"""
         alloc_size_by_device = {}
         for descr in descriptors:
             tensor_size = descr.numel() * torch.finfo(descr.dtype).bits // 8
@@ -107,33 +107,27 @@
             - hivemind.utils.enter_asynchronously() does not always release the lock on cancellation
         """
 
         loop = asyncio.get_event_loop()
         async with hivemind.utils.enter_asynchronously(self._lock_acquire_memory):
             if self.current_size_bytes + alloc_size > self.max_size_bytes:
                 await loop.run_in_executor(None, self._wait_until_available, alloc_size, self.alloc_timeout)
-            async with hivemind.utils.enter_asynchronously(self._lock_metadata):
+            with self._lock_metadata:
                 handles = tuple(int(self.handle_counter) + i for i in range(len(descriptors)))
                 self.current_size_bytes += alloc_size
                 self.handle_counter += len(handles)  # note: this will eventually overflow and it is okay
                 self._pipe_send.send((handles, descriptors))
                 return handles
 
-    async def _schedule_free(self, alloc_size: int, alloc_task: asyncio.Task):
-        """
-        This method should be called inside asyncio.shield() because:
-            - hivemind.utils.enter_asynchronously() does not always release the lock on cancellation
-            - _schedule_free() must finish freeing memory even in case of cancellation
-        """
-
+    def _free(self, alloc_size: int, alloc_task: asyncio.Task) -> None:
         if alloc_task.exception() is not None:
             return
         handles = alloc_task.result()
 
-        async with hivemind.utils.enter_asynchronously(self._lock_metadata):
+        with self._lock_metadata:
             self._pipe_send.send((handles, None))  # signal runtime to free these handles
             self.current_size_bytes -= alloc_size
         self._memory_freed_event.set()
 
     def _wait_until_available(self, allocated_size: int, timeout: Optional[float] = None):
         # note: this function should only be called inside _lock_acquire_memory!
         if allocated_size > self.max_size_bytes:
@@ -156,28 +150,27 @@
 
         :note: This method is called by ModuleBackend in runtime: a single process with NO process parallelism.
         However, runtime may call use_cache concurrently with one or more connection handlers calling allocate_cache
         """
         assert os.getpid() == self.runtime_pid
         # note: this specific function is not concurrent, so you can safely allocate/offload/defragment data here
 
-        with self._lock_metadata:
-            # read creation/deletion requests from connection handlers
-            while self._pipe_recv.poll():
-                recv_handles, recv_data = self._pipe_recv.recv()
-                if recv_data is not None:  # create new tensors
-                    assert len(recv_handles) == len(recv_data)
-                    for handle, descr in zip(recv_handles, recv_data):
-                        self._allocated_tensors[handle] = descr.make_zeros()
-                        assert handle in self._allocated_tensors, f"Sanity check failed: no such handle ({handle})"
-                else:  # delete tensors by handle
-                    for handle in recv_handles:
-                        if handle not in self._allocated_tensors:
-                            logger.warning(
-                                f"Sanity check failed: asked to delete handle {handle}, but there is no such handle"
-                            )
-                        self._allocated_tensors.pop(handle, None)
+        # read creation/deletion requests from connection handlers
+        while self._pipe_recv.poll():
+            recv_handles, recv_data = self._pipe_recv.recv()
+            if recv_data is not None:  # create new tensors
+                assert len(recv_handles) == len(recv_data)
+                for handle, descr in zip(recv_handles, recv_data):
+                    self._allocated_tensors[handle] = descr.make_zeros()
+                    assert handle in self._allocated_tensors, f"Sanity check failed: no such handle ({handle})"
+            else:  # delete tensors by handle
+                for handle in recv_handles:
+                    if handle not in self._allocated_tensors:
+                        logger.warning(
+                            f"Sanity check failed: asked to delete handle {handle}, but there is no such handle"
+                        )
+                    self._allocated_tensors.pop(handle, None)
         yield tuple(self._allocated_tensors[handle] for handle in handles)
 
 
 class AllocationFailed(Exception):
     pass
```

### Comparing `petals-2.0.0.post3/src/petals/server/reachability.py` & `petals-2.0.1/src/petals/server/reachability.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/server/server.py` & `petals-2.0.1/src/petals/server/server.py`

 * *Files 2% similar despite different names*

```diff
@@ -54,14 +54,15 @@
         throughput: Union[float, str],
         num_blocks: Optional[int] = None,
         block_indices: Optional[str] = None,
         num_handlers: int = 8,
         inference_max_length: Optional[int] = None,
         min_batch_size: int = 1,
         max_batch_size: Optional[int] = None,
+        max_chunk_size_bytes: int = 256 * 1024 * 1024,
         attn_cache_tokens: Optional[int] = None,
         torch_dtype: str = "auto",
         revision: Optional[str] = None,
         cache_dir: Optional[str] = None,
         max_disk_space: Optional[int] = None,
         alloc_timeout: float = 5,
         device: Optional[Union[str, torch.device]] = None,
@@ -100,15 +101,15 @@
         self.revision, self.token = revision, token
 
         if custom_module_path is not None:
             add_custom_models_from_file(custom_module_path)
 
         self.block_config = AutoDistributedConfig.from_pretrained(
             converted_model_name_or_path,
-            token=token,
+            use_auth_token=token,
             revision=revision,
         )
 
         if dht_prefix is None:
             dht_prefix = self.block_config.dht_prefix
         assert UID_DELIMITER not in dht_prefix and CHAIN_DELIMITER not in dht_prefix, (
             f"DHT prefix should not contain '{UID_DELIMITER}' or '{CHAIN_DELIMITER}'. "
@@ -179,18 +180,19 @@
         is_multiquery_attn = self.block_config.num_key_value_groups > 1
         if max_batch_size is None:
             max_batch_size = 8192 if is_multiquery_attn else 2048
         if inference_max_length is None:
             inference_max_length = 8192 if is_multiquery_attn else 2048
         self.min_batch_size, self.max_batch_size = min_batch_size, max_batch_size
         self.inference_max_length = inference_max_length
+        self.max_chunk_size_bytes = max_chunk_size_bytes
 
         # For attention cache in GPU or RAM
         if attn_cache_tokens is None:
-            attn_cache_tokens = 32768 if is_multiquery_attn else 2048
+            attn_cache_tokens = 32768 if is_multiquery_attn else 8192
         cache_values_per_block = 2 * self.block_config.hidden_size * attn_cache_tokens
         cache_values_per_block //= self.block_config.num_key_value_groups
         self._cache_bytes_per_block = cache_values_per_block * torch.finfo(self.torch_dtype).bits // 8
 
         # For disk cache
         self.cache_dir = cache_dir
         self.max_disk_space = max_disk_space
@@ -308,14 +310,15 @@
                 attn_cache_bytes=self.attn_cache_bytes,
                 alloc_timeout=self.alloc_timeout,
                 server_info=self.server_info,
                 block_indices=block_indices,
                 num_handlers=self.num_handlers,
                 min_batch_size=self.min_batch_size,
                 max_batch_size=self.max_batch_size,
+                max_chunk_size_bytes=self.max_chunk_size_bytes,
                 inference_max_length=self.inference_max_length,
                 torch_dtype=self.torch_dtype,
                 cache_dir=self.cache_dir,
                 max_disk_space=self.max_disk_space,
                 device=self.device,
                 compression=self.compression,
                 stats_report_interval=self.stats_report_interval,
@@ -408,14 +411,15 @@
         block_config: PretrainedConfig,
         attn_cache_bytes: int,
         alloc_timeout: float,
         server_info: ServerInfo,
         block_indices: List[int],
         min_batch_size: int,
         max_batch_size: int,
+        max_chunk_size_bytes: int,
         torch_dtype: torch.dtype,
         cache_dir: str,
         max_disk_space: int,
         device: Union[str, torch.device],
         compression: CompressionType,
         update_period: float,
         expiration: Optional[float],
@@ -473,14 +477,15 @@
                 )
                 blocks[module_uid] = TransformerBackend(
                     module_uid,
                     block,
                     config=block_config,
                     memory_cache=memory_cache,
                     backend_dtype=torch_dtype,
+                    max_chunk_size_bytes=max_chunk_size_bytes,
                     args_schema=(
                         BatchTensorDescriptor(
                             1, 2048, block_config.hidden_size, dtype=torch_dtype, compression=compression
                         ),
                     ),
                     kwargs_schema={},
                     outputs_schema=(
```

### Comparing `petals-2.0.0.post3/src/petals/server/task_pool.py` & `petals-2.0.1/src/petals/server/task_pool.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/server/task_prioritizer.py` & `petals-2.0.1/src/petals/server/task_prioritizer.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/server/throughput.py` & `petals-2.0.1/src/petals/server/throughput.py`

 * *Files 3% similar despite different names*

```diff
@@ -92,34 +92,31 @@
     # Most requests start at some block hosted by a server, then use all next blocks hosted on this server.
     # Assuming the start block index is distributed uniformly, the average number of blocks used per request is
     # E[Uniform{1, 2, ..., num_blocks}] = (num_blocks + 1) / 2
     average_blocks_used = (num_blocks + 1) / 2
     throughput = throughput_info["forward_rps"] / average_blocks_used
     throughput = min(throughput, throughput_info.get("network_rps", math.inf))
     throughput_info["throughput"] = throughput
-    logger.info(f"Reporting throughput: {throughput:.1f} RPS for {num_blocks} blocks")
+    logger.info(f"Reporting throughput: {throughput:.1f} tokens/sec for {num_blocks} blocks")
 
     return throughput_info
 
 
 def measure_throughput_info(
     config: PretrainedConfig,
     device: torch.device,
     dtype: torch.dtype,
     *,
     quant_type: QuantType,
     tensor_parallel_devices: Sequence[torch.device],
 ) -> Dict[str, float]:
-    """Measure network and compute throughput in forward pass tokens per second"""
-
     logger.info(
         "Measuring network and compute throughput. This takes about a minute and will be cached for future runs"
     )
-
-    throughput_info = {
+    return {
         "inference_rps": measure_compute_rps(
             config,
             device,
             dtype,
             quant_type=quant_type,
             tensor_parallel_devices=tensor_parallel_devices,
             n_tokens=1,
@@ -132,45 +129,47 @@
             dtype,
             quant_type=quant_type,
             tensor_parallel_devices=tensor_parallel_devices,
             n_tokens=1024,
             n_steps=10,
             inference=False,
         ),
+        "network_rps": measure_network_rps(config),
     }
-    try:
-        throughput_info["network_rps"] = measure_network_rps(config)
-    except Exception as e:
-        logger.info(f"Network throughput is not available: {e}")
-    return throughput_info
 
 
-def measure_network_rps(config: PretrainedConfig, *, timeout: float = 60) -> Optional[float]:
-    pipe_recv, pipe_send = mp.Pipe(duplex=False)
-    process = mp.Process(target=_measure_bits_per_second, args=(pipe_send,))
-    process.start()
-
-    if not pipe_recv.poll(timeout):
-        process.terminate()
-        raise RuntimeError(f"speedtest did not finish in {timeout} seconds")
-    network_info = pipe_recv.recv()
-    if "exception" in network_info:
-        raise RuntimeError(f"speedtest failed: {network_info['exception']}")
-
+def measure_network_rps(
+    config: PretrainedConfig, *, timeout: float = 60, default_speed: float = 100e6  # 100 Mbit/s
+) -> Optional[float]:
     bits_per_request = config.hidden_size * 16  # Clients usually send 16-bit tensors for forward/backward
-    network_rps = min(network_info["download"], network_info["upload"]) / bits_per_request
-    if network_rps == 0:
-        raise RuntimeError("speedtest has returned network_rps == 0")
-
-    logger.info(
-        f"Network throughput: {network_rps:.1f} RPS "
-        f"({network_info['download'] / 1e6:.2f} Mbit/s on download, "
-        f"{network_info['upload'] / 1e6:.2f} Mbit/s on upload)"
-    )
-    return network_rps
+    try:
+        pipe_recv, pipe_send = mp.Pipe(duplex=False)
+        process = mp.Process(target=_measure_bits_per_second, args=(pipe_send,))
+        process.start()
+
+        if not pipe_recv.poll(timeout):
+            process.terminate()
+            raise RuntimeError(f"speedtest did not finish in {timeout} seconds")
+        network_info = pipe_recv.recv()
+        if "exception" in network_info:
+            raise RuntimeError(f"speedtest failed: {network_info['exception']}")
+
+        network_rps = min(network_info["download"], network_info["upload"]) / bits_per_request
+        if network_rps == 0:
+            raise RuntimeError("speedtest has returned network_rps == 0")
+
+        logger.info(
+            f"Network throughput: {network_rps:.1f} tokens/sec "
+            f"({network_info['download'] / 1e6:.2f} Mbit/s on download, "
+            f"{network_info['upload'] / 1e6:.2f} Mbit/s on upload)"
+        )
+        return network_rps
+    except RuntimeError as e:
+        logger.info(f"Network throughput is not available: {e}. Using default of {default_speed / 1e6:.2f} Mbit/s")
+        return default_speed / bits_per_request
 
 
 def _measure_bits_per_second(pipe_send: mp.Pipe):
     try:
         s = speedtest.Speedtest()
         s.get_servers()
         s.get_best_server()
@@ -211,15 +210,15 @@
 
     devices_repr = get_device_name(device)
     if len(tensor_parallel_devices) > 1:
         device_names = tuple(map(get_device_name, map(torch.device, tensor_parallel_devices)))
         devices_repr = ", ".join(f"{count}x {name}" for name, count in Counter(device_names).most_common())
 
     logger.info(
-        f"{'Inference' if inference else 'Forward pass'} throughput: {device_rps:.1f} RPS per block "
+        f"{'Inference' if inference else 'Forward pass'} throughput: {device_rps:.1f} tokens/sec per block "
         f"({n_tokens} tokens/batch, {devices_repr}, {get_dtype_name(dtype, quant_type)})"
     )
     return device_rps
 
 
 def get_device_name(device: torch.device) -> str:
     return f"{torch.cuda.get_device_name(device)} GPU" if device.type == "cuda" else "CPU"
```

### Comparing `petals-2.0.0.post3/src/petals/utils/asyncio.py` & `petals-2.0.1/src/petals/utils/asyncio.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/utils/auto_config.py` & `petals-2.0.1/src/petals/utils/auto_config.py`

 * *Files 10% similar despite different names*

```diff
@@ -27,16 +27,20 @@
 
 
 class _AutoDistributedBase:
     _mapping_field = None  # Should be defined in child classes
 
     @classmethod
     def from_pretrained(cls, model_name_or_path: Union[str, os.PathLike, None], *args, **kwargs) -> PretrainedConfig:
-        if always_needs_auth(model_name_or_path) and "token" not in kwargs and "use_auth_token" not in kwargs:
-            kwargs["token"] = True
+        if (
+            always_needs_auth(model_name_or_path)
+            and kwargs.get("token") is None
+            and kwargs.get("use_auth_token") is None
+        ):
+            kwargs["use_auth_token"] = True
 
         config = AutoConfig.from_pretrained(model_name_or_path, *args, **kwargs)
         if config.model_type not in _CLASS_MAPPING:
             raise ValueError(f"Petals does not support model type {config.model_type}")
 
         proper_cls = getattr(_CLASS_MAPPING[config.model_type], cls._mapping_field)
         if proper_cls is None:
```

### Comparing `petals-2.0.0.post3/src/petals/utils/convert_block.py` & `petals-2.0.1/src/petals/utils/convert_block.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/utils/disk_cache.py` & `petals-2.0.1/src/petals/utils/disk_cache.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/utils/generation_algorithms.py` & `petals-2.0.1/src/petals/utils/generation_algorithms.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/utils/generation_constraints.py` & `petals-2.0.1/src/petals/utils/generation_constraints.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/utils/logging.py` & `petals-2.0.1/src/petals/utils/logging.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/utils/peft.py` & `petals-2.0.1/src/petals/utils/peft.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/utils/ping.py` & `petals-2.0.1/src/petals/utils/ping.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals/utils/version.py` & `petals-2.0.1/src/petals/utils/version.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/src/petals.egg-info/PKG-INFO` & `petals-2.0.1/src/petals.egg-info/PKG-INFO`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: petals
-Version: 2.0.0.post3
+Version: 2.0.1
 Summary: Easy way to efficiently run 100B+ language models without high-end GPUs
 Home-page: https://github.com/bigscience-workshop/petals
 Author: Petals Developers
 Author-email: petals-devs@googlegroups.com
 Project-URL: Bug Tracker, https://github.com/bigscience-workshop/petals/issues
 Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers
@@ -16,15 +16,15 @@
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Topic :: Scientific/Engineering
 Classifier: Topic :: Scientific/Engineering :: Mathematics
 Classifier: Topic :: Scientific/Engineering :: Artificial Intelligence
 Classifier: Topic :: Software Development
 Classifier: Topic :: Software Development :: Libraries
 Classifier: Topic :: Software Development :: Libraries :: Python Modules
-Requires-Python: <3.11,>=3.8
+Requires-Python: >=3.8
 Description-Content-Type: text/markdown
 Provides-Extra: dev
 License-File: LICENSE
 
 <p align="center">
     <img src="https://i.imgur.com/7eR7Pan.png" width="400"><br>
     Run large language models at home, BitTorrent-style.<br>
@@ -51,40 +51,54 @@
 print(tokenizer.decode(outputs[0]))  # A cat sat on a mat...
 ```
 
 <p align="center">
     🚀 &nbsp;<b><a href="https://colab.research.google.com/drive/1uCphNY7gfAUkdDrTx21dZZwCOUDCMPw8?usp=sharing">Try now in Colab</a></b>
 </p>
 
-📋 Make sure you follow the model's terms of use (see [LLaMA 2](https://bit.ly/llama2-license), [LLaMA](https://bit.ly/llama-license) and [BLOOM](https://bit.ly/bloom-license) licenses).
+🦙 **Want to run LLaMA 2?** Request access to its weights at the ♾️ [Meta AI website](https://ai.meta.com/resources/models-and-libraries/llama-downloads/) and 🤗 [Model Hub](https://huggingface.co/meta-llama/Llama-2-70b-hf), then run `huggingface-cli login` in the terminal before loading the model. Or just try it in our [chatbot app](https://chat.petals.dev).
 
-🔏 Your data will be processed by other people in the public swarm. Learn more about privacy [here](https://github.com/bigscience-workshop/petals/wiki/Security,-privacy,-and-AI-safety). For sensitive data, you can set up a [private swarm](https://github.com/bigscience-workshop/petals/wiki/Launch-your-own-swarm) among people you trust.
+📋 **Terms of use.** Make sure you follow the model license (see the ones for [LLaMA 2](https://bit.ly/llama2-license), [LLaMA](https://bit.ly/llama-license) and [BLOOM](https://bit.ly/bloom-license)).
+
+🔏 **Privacy.** Your data will be processed by other people in the public swarm. Learn more about privacy [here](https://github.com/bigscience-workshop/petals/wiki/Security,-privacy,-and-AI-safety). For sensitive data, you can set up a [private swarm](https://github.com/bigscience-workshop/petals/wiki/Launch-your-own-swarm) among people you trust.
 
 ### Connect your GPU and increase Petals capacity
 
-Run these commands in an [Anaconda](https://www.anaconda.com) env (requires Linux and Python 3.8+):
+Petals is a community-run system &mdash; we rely on people sharing their GPUs. You can check out available servers on our [swarm monitor](https://health.petals.dev) and connect your GPU to help serving one of the models!
+
+🐍 **Linux + Anaconda.** Run these commands:
 
 ```bash
 conda install pytorch pytorch-cuda=11.7 -c pytorch -c nvidia
-pip install --upgrade petals
+pip install git+https://github.com/bigscience-workshop/petals
 python -m petals.cli.run_server enoch/llama-65b-hf --adapters timdettmers/guanaco-65b
 ```
 
-Or run our [Docker](https://www.docker.com) image (works on Linux, macOS, and Windows with [WSL2](https://learn.microsoft.com/en-us/windows/ai/directml/gpu-cuda-in-wsl)):
+🪟 **Windows + WSL.** Follow the guide on our [Wiki](https://github.com/bigscience-workshop/petals/wiki/Run-Petals-server-on-Windows).
+
+🐋 **Any OS + Docker.** Run our [Docker](https://www.docker.com) image:
 
 ```bash
 sudo docker run -p 31330:31330 --ipc host --gpus all --volume petals-cache:/cache --rm learningathome/petals:main \
     python -m petals.cli.run_server --port 31330 enoch/llama-65b-hf --adapters timdettmers/guanaco-65b
 ```
 
-This will host a part of LLaMA-65B with optional [Guanaco](https://huggingface.co/timdettmers/guanaco-65b) adapters on your machine. You can also host `meta-llama/Llama-2-70b-hf`, `meta-llama/Llama-2-70b-chat-hf`, `bigscience/bloom`, `bigscience/bloomz`, and other compatible models from 🤗 [Model Hub](https://huggingface.co/models), or [add support](https://github.com/bigscience-workshop/petals/wiki/Run-a-custom-model-with-Petals) for new model architectures.
+These commands host a part of LLaMA-65B with optional [Guanaco](https://huggingface.co/timdettmers/guanaco-65b) adapters on your machine. You can also host `meta-llama/Llama-2-70b-hf`, `meta-llama/Llama-2-70b-chat-hf`, `bigscience/bloom`, `bigscience/bloomz`, and other compatible models from 🤗 [Model Hub](https://huggingface.co/models), or [add support](https://github.com/bigscience-workshop/petals/wiki/Run-a-custom-model-with-Petals) for new model architectures.
+
+🦙 **Want to host LLaMA 2?** Request access to its weights at the ♾️ [Meta AI website](https://ai.meta.com/resources/models-and-libraries/llama-downloads/) and 🤗 [Model Hub](https://huggingface.co/meta-llama/Llama-2-70b-hf), generate an 🔑 [access token](https://huggingface.co/settings/tokens), then use this command for `petals.cli.run_server`:
+
+```bash
+python -m petals.cli.run_server meta-llama/Llama-2-70b-chat-hf --token YOUR_TOKEN_HERE
+```
+
+💬 **FAQ.** Check out our [Wiki](https://github.com/bigscience-workshop/petals/wiki/FAQ:-Frequently-asked-questions#running-a-server) to learn how to use multple GPUs, restart the server on reboot, etc. If you have any issues or feedback, ping us in [our Discord](https://discord.gg/D9MwApKgWa)!
 
-🔒 Hosting a server does not allow others to run custom code on your computer. Learn more about security [here](https://github.com/bigscience-workshop/petals/wiki/Security,-privacy,-and-AI-safety).
+🔒 **Security.** Hosting a server does not allow others to run custom code on your computer. Learn more [here](https://github.com/bigscience-workshop/petals/wiki/Security,-privacy,-and-AI-safety).
 
-💬 See [FAQ](https://github.com/bigscience-workshop/petals/wiki/FAQ:-Frequently-asked-questions#running-a-server) to learn how to use multple GPUs, restart the server on reboot, etc. If you have any issues or feedback, ping us in [our Discord](https://discord.gg/D9MwApKgWa)!
+🏆 **Thank you!** Once you load and host 10+ blocks, we can show your name or link on the [swarm monitor](https://health.petals.dev) as a way to say thanks. You can specify them with `--public_name YOUR_NAME`.
 
 ### Check out tutorials, examples, and more
 
 Basic tutorials:
 
 - Getting started: [tutorial](https://colab.research.google.com/drive/1uCphNY7gfAUkdDrTx21dZZwCOUDCMPw8?usp=sharing)
 - Prompt-tune LLaMA-65B for text semantic classification: [tutorial](https://colab.research.google.com/github/bigscience-workshop/petals/blob/main/examples/prompt-tuning-sst2.ipynb)
@@ -120,15 +134,15 @@
 
 ## Installation
 
 Here's how to install Petals with [Anaconda](https://www.anaconda.com/products/distribution) on Linux:
 
 ```bash
 conda install pytorch pytorch-cuda=11.7 -c pytorch -c nvidia
-pip install --upgrade petals
+pip install git+https://github.com/bigscience-workshop/petals
 ```
 
 If you don't use Anaconda, you can install PyTorch in [any other way](https://pytorch.org/get-started/locally/). If you want to run models with 8-bit weights, please install PyTorch with CUDA 11.x or newer for compatility with [bitsandbytes](https://github.com/timDettmers/bitsandbytes).
 
 See the instructions for macOS and Windows, the full requirements, and troubleshooting advice in our [FAQ](https://github.com/bigscience-workshop/petals/wiki/FAQ:-Frequently-asked-questions#running-a-client).
 
 ## Benchmarks
```

#### html2text {}

```diff
@@ -1,22 +1,22 @@
-Metadata-Version: 2.1 Name: petals Version: 2.0.0.post3 Summary: Easy way to
+Metadata-Version: 2.1 Name: petals Version: 2.0.1 Summary: Easy way to
 efficiently run 100B+ language models without high-end GPUs Home-page: https://
 github.com/bigscience-workshop/petals Author: Petals Developers Author-email:
 petals-devs@googlegroups.com Project-URL: Bug Tracker, https://github.com/
 bigscience-workshop/petals/issues Classifier: Development Status :: 4 - Beta
 Classifier: Intended Audience :: Developers Classifier: Intended Audience ::
 Science/Research Classifier: License :: OSI Approved :: MIT License Classifier:
 Programming Language :: Python :: 3 Classifier: Programming Language :: Python
 :: 3.8 Classifier: Programming Language :: Python :: 3.9 Classifier:
 Programming Language :: Python :: 3.10 Classifier: Topic :: Scientific/
 Engineering Classifier: Topic :: Scientific/Engineering :: Mathematics
 Classifier: Topic :: Scientific/Engineering :: Artificial Intelligence
 Classifier: Topic :: Software Development Classifier: Topic :: Software
 Development :: Libraries Classifier: Topic :: Software Development :: Libraries
-:: Python Modules Requires-Python: <3.11,>=3.8 Description-Content-Type: text/
+:: Python Modules Requires-Python: >=3.8 Description-Content-Type: text/
 markdown Provides-Extra: dev License-File: LICENSE
                        [https://i.imgur.com/7eR7Pan.png]
              Run large language models at home, BitTorrent-style.
           Fine-tuning and inference up_to_10x_faster than offloading
 
             [https://img.shields.io/pypi/v/petals.svg?color=green]
 Generate text with distributed [LLaMA 2](https://ai.meta.com/llama/) ([70B]
@@ -32,44 +32,61 @@
 bloomz" tokenizer = AutoTokenizer.from_pretrained(model_name) model =
 AutoDistributedModelForCausalLM.from_pretrained(model_name) # Embeddings &
 prompts are on your device, transformer blocks are distributed across the
 Internet inputs = tokenizer("A cat sat", return_tensors="pt")["input_ids"]
 outputs = model.generate(inputs, max_new_tokens=5) print(tokenizer.decode
 (outputs[0])) # A cat sat on a mat... ```
                             ð  Try_now_in_Colab
-ð Make sure you follow the model's terms of use (see [LLaMA 2](https://
+ð¦ **Want to run LLaMA 2?** Request access to its weights at the â¾ï¸ [Meta
+AI website](https://ai.meta.com/resources/models-and-libraries/llama-downloads/
+) and ð¤ [Model Hub](https://huggingface.co/meta-llama/Llama-2-70b-hf), then
+run `huggingface-cli login` in the terminal before loading the model. Or just
+try it in our [chatbot app](https://chat.petals.dev). ð **Terms of use.**
+Make sure you follow the model license (see the ones for [LLaMA 2](https://
 bit.ly/llama2-license), [LLaMA](https://bit.ly/llama-license) and [BLOOM]
-(https://bit.ly/bloom-license) licenses). ð Your data will be processed by
-other people in the public swarm. Learn more about privacy [here](https://
+(https://bit.ly/bloom-license)). ð **Privacy.** Your data will be processed
+by other people in the public swarm. Learn more about privacy [here](https://
 github.com/bigscience-workshop/petals/wiki/Security,-privacy,-and-AI-safety).
 For sensitive data, you can set up a [private swarm](https://github.com/
 bigscience-workshop/petals/wiki/Launch-your-own-swarm) among people you trust.
-### Connect your GPU and increase Petals capacity Run these commands in an
-[Anaconda](https://www.anaconda.com) env (requires Linux and Python 3.8+):
-```bash conda install pytorch pytorch-cuda=11.7 -c pytorch -c nvidia pip
-install --upgrade petals python -m petals.cli.run_server enoch/llama-65b-hf --
-adapters timdettmers/guanaco-65b ``` Or run our [Docker](https://
-www.docker.com) image (works on Linux, macOS, and Windows with [WSL2](https://
-learn.microsoft.com/en-us/windows/ai/directml/gpu-cuda-in-wsl)): ```bash sudo
-docker run -p 31330:31330 --ipc host --gpus all --volume petals-cache:/cache --
-rm learningathome/petals:main \ python -m petals.cli.run_server --port 31330
-enoch/llama-65b-hf --adapters timdettmers/guanaco-65b ``` This will host a part
-of LLaMA-65B with optional [Guanaco](https://huggingface.co/timdettmers/
+### Connect your GPU and increase Petals capacity Petals is a community-run
+system — we rely on people sharing their GPUs. You can check out available
+servers on our [swarm monitor](https://health.petals.dev) and connect your GPU
+to help serving one of the models! ð **Linux + Anaconda.** Run these
+commands: ```bash conda install pytorch pytorch-cuda=11.7 -c pytorch -c nvidia
+pip install git+https://github.com/bigscience-workshop/petals python -
+m petals.cli.run_server enoch/llama-65b-hf --adapters timdettmers/guanaco-65b
+``` ðª **Windows + WSL.** Follow the guide on our [Wiki](https://github.com/
+bigscience-workshop/petals/wiki/Run-Petals-server-on-Windows). ð **Any OS +
+Docker.** Run our [Docker](https://www.docker.com) image: ```bash sudo docker
+run -p 31330:31330 --ipc host --gpus all --volume petals-cache:/cache --rm
+learningathome/petals:main \ python -m petals.cli.run_server --port 31330
+enoch/llama-65b-hf --adapters timdettmers/guanaco-65b ``` These commands host a
+part of LLaMA-65B with optional [Guanaco](https://huggingface.co/timdettmers/
 guanaco-65b) adapters on your machine. You can also host `meta-llama/Llama-2-
 70b-hf`, `meta-llama/Llama-2-70b-chat-hf`, `bigscience/bloom`, `bigscience/
 bloomz`, and other compatible models from ð¤ [Model Hub](https://
 huggingface.co/models), or [add support](https://github.com/bigscience-
 workshop/petals/wiki/Run-a-custom-model-with-Petals) for new model
-architectures. ð Hosting a server does not allow others to run custom code
-on your computer. Learn more about security [here](https://github.com/
-bigscience-workshop/petals/wiki/Security,-privacy,-and-AI-safety). ð¬ See
-[FAQ](https://github.com/bigscience-workshop/petals/wiki/FAQ:-Frequently-asked-
-questions#running-a-server) to learn how to use multple GPUs, restart the
-server on reboot, etc. If you have any issues or feedback, ping us in [our
-Discord](https://discord.gg/D9MwApKgWa)! ### Check out tutorials, examples, and
+architectures. ð¦ **Want to host LLaMA 2?** Request access to its weights at
+the â¾ï¸ [Meta AI website](https://ai.meta.com/resources/models-and-
+libraries/llama-downloads/) and ð¤ [Model Hub](https://huggingface.co/meta-
+llama/Llama-2-70b-hf), generate an ð [access token](https://huggingface.co/
+settings/tokens), then use this command for `petals.cli.run_server`: ```bash
+python -m petals.cli.run_server meta-llama/Llama-2-70b-chat-hf --token
+YOUR_TOKEN_HERE ``` ð¬ **FAQ.** Check out our [Wiki](https://github.com/
+bigscience-workshop/petals/wiki/FAQ:-Frequently-asked-questions#running-a-
+server) to learn how to use multple GPUs, restart the server on reboot, etc. If
+you have any issues or feedback, ping us in [our Discord](https://discord.gg/
+D9MwApKgWa)! ð **Security.** Hosting a server does not allow others to run
+custom code on your computer. Learn more [here](https://github.com/bigscience-
+workshop/petals/wiki/Security,-privacy,-and-AI-safety). ð **Thank you!**
+Once you load and host 10+ blocks, we can show your name or link on the [swarm
+monitor](https://health.petals.dev) as a way to say thanks. You can specify
+them with `--public_name YOUR_NAME`. ### Check out tutorials, examples, and
 more Basic tutorials: - Getting started: [tutorial](https://
 colab.research.google.com/drive/1uCphNY7gfAUkdDrTx21dZZwCOUDCMPw8?usp=sharing)
 - Prompt-tune LLaMA-65B for text semantic classification: [tutorial](https://
 colab.research.google.com/github/bigscience-workshop/petals/blob/main/examples/
 prompt-tuning-sst2.ipynb) - Prompt-tune BLOOM to create a personified chatbot:
 [tutorial](https://colab.research.google.com/github/bigscience-workshop/petals/
 blob/main/examples/prompt-tuning-personachat.ipynb) Useful tools and advanced
@@ -95,23 +112,23 @@
 any fine-tuning and sampling methods, execute custom paths through the model,
 or see its hidden states. You get the comforts of an API with the flexibility
 of PyTorch.
                        [https://i.imgur.com/RTYF3yW.png]
                    ð  See_FAQ            ð  Read_paper
 ## Installation Here's how to install Petals with [Anaconda](https://
 www.anaconda.com/products/distribution) on Linux: ```bash conda install pytorch
-pytorch-cuda=11.7 -c pytorch -c nvidia pip install --upgrade petals ``` If you
-don't use Anaconda, you can install PyTorch in [any other way](https://
-pytorch.org/get-started/locally/). If you want to run models with 8-bit
-weights, please install PyTorch with CUDA 11.x or newer for compatility with
-[bitsandbytes](https://github.com/timDettmers/bitsandbytes). See the
-instructions for macOS and Windows, the full requirements, and troubleshooting
-advice in our [FAQ](https://github.com/bigscience-workshop/petals/wiki/FAQ:-
-Frequently-asked-questions#running-a-client). ## Benchmarks The benchmarks
-below are for BLOOM-176B:
+pytorch-cuda=11.7 -c pytorch -c nvidia pip install git+https://github.com/
+bigscience-workshop/petals ``` If you don't use Anaconda, you can install
+PyTorch in [any other way](https://pytorch.org/get-started/locally/). If you
+want to run models with 8-bit weights, please install PyTorch with CUDA 11.x or
+newer for compatility with [bitsandbytes](https://github.com/timDettmers/
+bitsandbytes). See the instructions for macOS and Windows, the full
+requirements, and troubleshooting advice in our [FAQ](https://github.com/
+bigscience-workshop/petals/wiki/FAQ:-Frequently-asked-questions#running-a-
+client). ## Benchmarks The benchmarks below are for BLOOM-176B:
      Network               Single-batch inference Parallel forward
                            (steps/s)              (tokens/s)
      Bandwidth  Round-trip Sequence length        Batch size
                 latency    128           2048       1              64
      Offloading, max. possible speed on 1x A100 1
      256 Gbit/s            0.18          0.18     2.7           170.3
      128 Gbit/s            0.09          0.09     2.4           152.8
```

### Comparing `petals-2.0.0.post3/src/petals.egg-info/SOURCES.txt` & `petals-2.0.1/src/petals.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/tests/test_aux_functions.py` & `petals-2.0.1/tests/test_aux_functions.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/tests/test_block_exact_match.py` & `petals-2.0.1/tests/test_block_exact_match.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/tests/test_chained_calls.py` & `petals-2.0.1/tests/test_chained_calls.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/tests/test_dtype.py` & `petals-2.0.1/tests/test_dtype.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/tests/test_full_model.py` & `petals-2.0.1/tests/test_full_model.py`

 * *Files 5% similar despite different names*

```diff
@@ -24,31 +24,37 @@
         torch_dtype=torch.float32,
         active_adapter=ADAPTER_NAME if use_peft else None,
     )
     config = model.config
     assert isinstance(model, DistributedBloomForCausalLM)
     assert len(model.transformer.h) == model.config.num_hidden_layers
 
-    test_inputs = tokenizer("A cat sat on a mat", return_tensors="pt")["input_ids"]
+    test_inputs = tokenizer("A quick brown fox was minding its own buisness", return_tensors="pt")["input_ids"]
 
     with torch.inference_mode():
         parallel_outputs = model.forward(test_inputs).logits
         assert torch.all(torch.isfinite(parallel_outputs))
         logger.info("Forward outputs are finite")
 
         embs = model.transformer.word_embeddings(test_inputs)
         embs = model.transformer.word_embeddings_layernorm(embs)
         recurrent_outputs = []
         with model.transformer.h.inference_session(max_length=embs.shape[1]) as sess:
             if pass_empty_tensors:
                 recurrent_outputs.append(sess.step(torch.empty(1, 0, config.hidden_size)))
 
             for t in range(embs.shape[1]):
-                recurrent_outputs.append(sess.step(embs[:, t : t + 1, :]))
-                if t == int(embs.shape[1] // 2) and pass_empty_tensors:
+                if t == 4:
+                    recurrent_outputs.append(sess.step(embs[:, 4:9, :]))
+                elif 4 < t < 9:
+                    continue
+                else:
+                    recurrent_outputs.append(sess.step(embs[:, t : t + 1, :]))
+
+                if t == 2 and pass_empty_tensors:
                     recurrent_outputs.append(sess.step(torch.empty(1, 0, config.hidden_size)))
                     recurrent_outputs.append(sess.step(torch.empty(1, 0, config.hidden_size)))
 
         recurrent_outputs = torch.cat(recurrent_outputs, dim=1)
         recurrent_outputs = model.transformer.ln_f(recurrent_outputs)
         recurrent_outputs = model.lm_head(recurrent_outputs)
         assert torch.allclose(recurrent_outputs, parallel_outputs, rtol=0, atol=atol_inference)
```

### Comparing `petals-2.0.0.post3/tests/test_peft.py` & `petals-2.0.1/tests/test_peft.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/tests/test_priority_pool.py` & `petals-2.0.1/tests/test_priority_pool.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/tests/test_remote_sequential.py` & `petals-2.0.1/tests/test_remote_sequential.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/tests/test_sequence_manager.py` & `petals-2.0.1/tests/test_sequence_manager.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/tests/test_server_stats.py` & `petals-2.0.1/tests/test_server_stats.py`

 * *Files identical despite different names*

### Comparing `petals-2.0.0.post3/tests/test_tensor_parallel.py` & `petals-2.0.1/tests/test_tensor_parallel.py`

 * *Files identical despite different names*

