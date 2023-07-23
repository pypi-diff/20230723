# Comparing `tmp/refuel-autolabel-0.0.8.tar.gz` & `tmp/refuel-autolabel-0.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "refuel-autolabel-0.0.8.tar", last modified: Wed Jul 12 00:34:35 2023, max compression
+gzip compressed data, was "refuel-autolabel-0.0.9.tar", last modified: Sun Jul 23 19:19:03 2023, max compression
```

## Comparing `refuel-autolabel-0.0.8.tar` & `refuel-autolabel-0.0.9.tar`

### file list

```diff
@@ -1,67 +1,75 @@
-drwxr-xr-x   0 nihit      (501) staff       (20)        0 2023-07-12 00:34:35.406330 refuel-autolabel-0.0.8/
--rw-r--r--   0 nihit      (501) staff       (20)     1066 2023-05-11 06:24:46.000000 refuel-autolabel-0.0.8/LICENSE
--rw-r--r--   0 nihit      (501) staff       (20)    10381 2023-07-12 00:34:35.406104 refuel-autolabel-0.0.8/PKG-INFO
--rw-r--r--   0 nihit      (501) staff       (20)     8334 2023-07-06 04:47:37.000000 refuel-autolabel-0.0.8/README.md
--rw-r--r--   0 nihit      (501) staff       (20)     2328 2023-07-12 00:34:26.000000 refuel-autolabel-0.0.8/pyproject.toml
--rw-r--r--   0 nihit      (501) staff       (20)       38 2023-07-12 00:34:35.406390 refuel-autolabel-0.0.8/setup.cfg
-drwxr-xr-x   0 nihit      (501) staff       (20)        0 2023-07-12 00:34:35.393523 refuel-autolabel-0.0.8/src/
-drwxr-xr-x   0 nihit      (501) staff       (20)        0 2023-07-12 00:34:35.396443 refuel-autolabel-0.0.8/src/autolabel/
--rw-r--r--   0 nihit      (501) staff       (20)      263 2023-07-12 00:34:26.000000 refuel-autolabel-0.0.8/src/autolabel/__init__.py
-drwxr-xr-x   0 nihit      (501) staff       (20)        0 2023-07-12 00:34:35.397229 refuel-autolabel-0.0.8/src/autolabel/cache/
--rw-r--r--   0 nihit      (501) staff       (20)       74 2023-05-16 00:22:56.000000 refuel-autolabel-0.0.8/src/autolabel/cache/__init__.py
--rw-r--r--   0 nihit      (501) staff       (20)      924 2023-06-08 20:27:49.000000 refuel-autolabel-0.0.8/src/autolabel/cache/base.py
--rw-r--r--   0 nihit      (501) staff       (20)     1817 2023-06-14 01:40:05.000000 refuel-autolabel-0.0.8/src/autolabel/cache/sqlalchemy_cache.py
--rw-r--r--   0 nihit      (501) staff       (20)     9137 2023-06-15 00:40:46.000000 refuel-autolabel-0.0.8/src/autolabel/confidence.py
-drwxr-xr-x   0 nihit      (501) staff       (20)        0 2023-07-12 00:34:35.398191 refuel-autolabel-0.0.8/src/autolabel/configs/
--rw-r--r--   0 nihit      (501) staff       (20)       65 2023-05-29 00:22:31.000000 refuel-autolabel-0.0.8/src/autolabel/configs/__init__.py
--rw-r--r--   0 nihit      (501) staff       (20)     1401 2023-06-26 23:56:08.000000 refuel-autolabel-0.0.8/src/autolabel/configs/base.py
--rw-r--r--   0 nihit      (501) staff       (20)     7569 2023-07-06 04:47:37.000000 refuel-autolabel-0.0.8/src/autolabel/configs/config.py
--rw-r--r--   0 nihit      (501) staff       (20)     4171 2023-07-11 21:30:59.000000 refuel-autolabel-0.0.8/src/autolabel/configs/schema.py
-drwxr-xr-x   0 nihit      (501) staff       (20)        0 2023-07-12 00:34:35.398862 refuel-autolabel-0.0.8/src/autolabel/data_loaders/
--rw-r--r--   0 nihit      (501) staff       (20)     4248 2023-07-11 21:30:59.000000 refuel-autolabel-0.0.8/src/autolabel/data_loaders/__init__.py
--rw-r--r--   0 nihit      (501) staff       (20)     7011 2023-07-10 22:40:36.000000 refuel-autolabel-0.0.8/src/autolabel/data_loaders/read_datasets.py
--rw-r--r--   0 nihit      (501) staff       (20)     8498 2023-07-11 19:29:59.000000 refuel-autolabel-0.0.8/src/autolabel/data_loaders/validation.py
-drwxr-xr-x   0 nihit      (501) staff       (20)        0 2023-07-12 00:34:35.400368 refuel-autolabel-0.0.8/src/autolabel/data_models/
--rw-r--r--   0 nihit      (501) staff       (20)      195 2023-05-16 00:22:56.000000 refuel-autolabel-0.0.8/src/autolabel/data_models/__init__.py
--rw-r--r--   0 nihit      (501) staff       (20)     2001 2023-06-14 01:40:05.000000 refuel-autolabel-0.0.8/src/autolabel/data_models/annotation.py
--rw-r--r--   0 nihit      (501) staff       (20)       71 2023-05-14 02:11:15.000000 refuel-autolabel-0.0.8/src/autolabel/data_models/base.py
--rw-r--r--   0 nihit      (501) staff       (20)     2036 2023-06-10 22:44:42.000000 refuel-autolabel-0.0.8/src/autolabel/data_models/cache.py
--rw-r--r--   0 nihit      (501) staff       (20)     1071 2023-05-14 02:11:15.000000 refuel-autolabel-0.0.8/src/autolabel/data_models/dataset.py
--rw-r--r--   0 nihit      (501) staff       (20)      928 2023-05-14 02:11:15.000000 refuel-autolabel-0.0.8/src/autolabel/data_models/task.py
--rw-r--r--   0 nihit      (501) staff       (20)     2625 2023-06-14 01:40:05.000000 refuel-autolabel-0.0.8/src/autolabel/data_models/task_run.py
-drwxr-xr-x   0 nihit      (501) staff       (20)        0 2023-07-12 00:34:35.400924 refuel-autolabel-0.0.8/src/autolabel/database/
--rw-r--r--   0 nihit      (501) staff       (20)       77 2023-05-14 02:11:15.000000 refuel-autolabel-0.0.8/src/autolabel/database/__init__.py
--rw-r--r--   0 nihit      (501) staff       (20)      643 2023-07-06 04:47:37.000000 refuel-autolabel-0.0.8/src/autolabel/database/engine.py
--rw-r--r--   0 nihit      (501) staff       (20)     2788 2023-06-14 01:40:05.000000 refuel-autolabel-0.0.8/src/autolabel/database/state_manager.py
-drwxr-xr-x   0 nihit      (501) staff       (20)        0 2023-07-12 00:34:35.401804 refuel-autolabel-0.0.8/src/autolabel/few_shot/
--rw-r--r--   0 nihit      (501) staff       (20)     3928 2023-07-07 22:34:09.000000 refuel-autolabel-0.0.8/src/autolabel/few_shot/__init__.py
--rw-r--r--   0 nihit      (501) staff       (20)     1295 2023-05-14 02:11:15.000000 refuel-autolabel-0.0.8/src/autolabel/few_shot/fixed_example_selector.py
--rw-r--r--   0 nihit      (501) staff       (20)     6328 2023-07-07 22:34:09.000000 refuel-autolabel-0.0.8/src/autolabel/few_shot/label_diversity_example_selector.py
--rw-r--r--   0 nihit      (501) staff       (20)    14119 2023-07-07 22:34:09.000000 refuel-autolabel-0.0.8/src/autolabel/few_shot/vector_store.py
--rw-r--r--   0 nihit      (501) staff       (20)    19712 2023-07-11 19:29:59.000000 refuel-autolabel-0.0.8/src/autolabel/labeler.py
-drwxr-xr-x   0 nihit      (501) staff       (20)        0 2023-07-12 00:34:35.403329 refuel-autolabel-0.0.8/src/autolabel/models/
--rw-r--r--   0 nihit      (501) staff       (20)     2107 2023-07-06 04:47:37.000000 refuel-autolabel-0.0.8/src/autolabel/models/__init__.py
--rw-r--r--   0 nihit      (501) staff       (20)     2395 2023-07-11 21:30:59.000000 refuel-autolabel-0.0.8/src/autolabel/models/anthropic.py
--rw-r--r--   0 nihit      (501) staff       (20)     4902 2023-07-11 21:30:59.000000 refuel-autolabel-0.0.8/src/autolabel/models/base.py
--rw-r--r--   0 nihit      (501) staff       (20)     1902 2023-07-11 21:30:59.000000 refuel-autolabel-0.0.8/src/autolabel/models/cohere.py
--rw-r--r--   0 nihit      (501) staff       (20)     3063 2023-07-11 21:30:59.000000 refuel-autolabel-0.0.8/src/autolabel/models/hf_pipeline.py
--rw-r--r--   0 nihit      (501) staff       (20)     6063 2023-07-11 21:30:59.000000 refuel-autolabel-0.0.8/src/autolabel/models/openai.py
--rw-r--r--   0 nihit      (501) staff       (20)     4840 2023-07-11 21:30:59.000000 refuel-autolabel-0.0.8/src/autolabel/models/palm.py
--rw-r--r--   0 nihit      (501) staff       (20)     3575 2023-06-20 23:17:06.000000 refuel-autolabel-0.0.8/src/autolabel/models/refuel.py
--rw-r--r--   0 nihit      (501) staff       (20)     4823 2023-07-07 22:34:09.000000 refuel-autolabel-0.0.8/src/autolabel/schema.py
-drwxr-xr-x   0 nihit      (501) staff       (20)        0 2023-07-12 00:34:35.405145 refuel-autolabel-0.0.8/src/autolabel/tasks/
--rw-r--r--   0 nihit      (501) staff       (20)     1298 2023-07-06 04:47:37.000000 refuel-autolabel-0.0.8/src/autolabel/tasks/__init__.py
--rw-r--r--   0 nihit      (501) staff       (20)     4319 2023-06-20 23:17:06.000000 refuel-autolabel-0.0.8/src/autolabel/tasks/base.py
--rw-r--r--   0 nihit      (501) staff       (20)     7409 2023-06-19 23:05:19.000000 refuel-autolabel-0.0.8/src/autolabel/tasks/classification.py
--rw-r--r--   0 nihit      (501) staff       (20)     7419 2023-06-19 23:05:19.000000 refuel-autolabel-0.0.8/src/autolabel/tasks/entity_matching.py
--rw-r--r--   0 nihit      (501) staff       (20)     8221 2023-07-06 04:47:37.000000 refuel-autolabel-0.0.8/src/autolabel/tasks/multilabel_classification.py
--rw-r--r--   0 nihit      (501) staff       (20)    12627 2023-06-19 23:05:19.000000 refuel-autolabel-0.0.8/src/autolabel/tasks/named_entity_recognition.py
--rw-r--r--   0 nihit      (501) staff       (20)     7508 2023-06-19 23:05:19.000000 refuel-autolabel-0.0.8/src/autolabel/tasks/question_answering.py
--rw-r--r--   0 nihit      (501) staff       (20)     1574 2023-06-08 20:27:49.000000 refuel-autolabel-0.0.8/src/autolabel/tasks/utils.py
--rw-r--r--   0 nihit      (501) staff       (20)     9773 2023-06-22 21:37:13.000000 refuel-autolabel-0.0.8/src/autolabel/utils.py
-drwxr-xr-x   0 nihit      (501) staff       (20)        0 2023-07-12 00:34:35.405900 refuel-autolabel-0.0.8/src/refuel_autolabel.egg-info/
--rw-r--r--   0 nihit      (501) staff       (20)    10381 2023-07-12 00:34:35.000000 refuel-autolabel-0.0.8/src/refuel_autolabel.egg-info/PKG-INFO
--rw-r--r--   0 nihit      (501) staff       (20)     1834 2023-07-12 00:34:35.000000 refuel-autolabel-0.0.8/src/refuel_autolabel.egg-info/SOURCES.txt
--rw-r--r--   0 nihit      (501) staff       (20)        1 2023-07-12 00:34:35.000000 refuel-autolabel-0.0.8/src/refuel_autolabel.egg-info/dependency_links.txt
--rw-r--r--   0 nihit      (501) staff       (20)      919 2023-07-12 00:34:35.000000 refuel-autolabel-0.0.8/src/refuel_autolabel.egg-info/requires.txt
--rw-r--r--   0 nihit      (501) staff       (20)       10 2023-07-12 00:34:35.000000 refuel-autolabel-0.0.8/src/refuel_autolabel.egg-info/top_level.txt
+drwxr-xr-x   0 nihit      (501) staff       (20)        0 2023-07-23 19:19:03.370229 refuel-autolabel-0.0.9/
+-rw-r--r--   0 nihit      (501) staff       (20)     1066 2023-05-11 06:24:46.000000 refuel-autolabel-0.0.9/LICENSE
+-rw-r--r--   0 nihit      (501) staff       (20)    10381 2023-07-23 19:19:03.370027 refuel-autolabel-0.0.9/PKG-INFO
+-rw-r--r--   0 nihit      (501) staff       (20)     8334 2023-07-06 04:47:37.000000 refuel-autolabel-0.0.9/README.md
+-rw-r--r--   0 nihit      (501) staff       (20)     2328 2023-07-23 19:18:41.000000 refuel-autolabel-0.0.9/pyproject.toml
+-rw-r--r--   0 nihit      (501) staff       (20)       38 2023-07-23 19:19:03.370274 refuel-autolabel-0.0.9/setup.cfg
+drwxr-xr-x   0 nihit      (501) staff       (20)        0 2023-07-23 19:19:03.355442 refuel-autolabel-0.0.9/src/
+drwxr-xr-x   0 nihit      (501) staff       (20)        0 2023-07-23 19:19:03.357322 refuel-autolabel-0.0.9/src/autolabel/
+-rw-r--r--   0 nihit      (501) staff       (20)      263 2023-07-12 00:34:26.000000 refuel-autolabel-0.0.9/src/autolabel/__init__.py
+drwxr-xr-x   0 nihit      (501) staff       (20)        0 2023-07-23 19:19:03.358058 refuel-autolabel-0.0.9/src/autolabel/cache/
+-rw-r--r--   0 nihit      (501) staff       (20)       74 2023-05-16 00:22:56.000000 refuel-autolabel-0.0.9/src/autolabel/cache/__init__.py
+-rw-r--r--   0 nihit      (501) staff       (20)      924 2023-06-08 20:27:49.000000 refuel-autolabel-0.0.9/src/autolabel/cache/base.py
+-rw-r--r--   0 nihit      (501) staff       (20)     1817 2023-06-14 01:40:05.000000 refuel-autolabel-0.0.9/src/autolabel/cache/sqlalchemy_cache.py
+-rw-r--r--   0 nihit      (501) staff       (20)     9068 2023-07-23 18:58:04.000000 refuel-autolabel-0.0.9/src/autolabel/confidence.py
+drwxr-xr-x   0 nihit      (501) staff       (20)        0 2023-07-23 19:19:03.359035 refuel-autolabel-0.0.9/src/autolabel/configs/
+-rw-r--r--   0 nihit      (501) staff       (20)       65 2023-05-29 00:22:31.000000 refuel-autolabel-0.0.9/src/autolabel/configs/__init__.py
+-rw-r--r--   0 nihit      (501) staff       (20)     1401 2023-06-26 23:56:08.000000 refuel-autolabel-0.0.9/src/autolabel/configs/base.py
+-rw-r--r--   0 nihit      (501) staff       (20)     7569 2023-07-06 04:47:37.000000 refuel-autolabel-0.0.9/src/autolabel/configs/config.py
+-rw-r--r--   0 nihit      (501) staff       (20)     4171 2023-07-11 21:30:59.000000 refuel-autolabel-0.0.9/src/autolabel/configs/schema.py
+drwxr-xr-x   0 nihit      (501) staff       (20)        0 2023-07-23 19:19:03.359908 refuel-autolabel-0.0.9/src/autolabel/data_loaders/
+-rw-r--r--   0 nihit      (501) staff       (20)     4248 2023-07-11 21:30:59.000000 refuel-autolabel-0.0.9/src/autolabel/data_loaders/__init__.py
+-rw-r--r--   0 nihit      (501) staff       (20)     7011 2023-07-10 22:40:36.000000 refuel-autolabel-0.0.9/src/autolabel/data_loaders/read_datasets.py
+-rw-r--r--   0 nihit      (501) staff       (20)     9720 2023-07-17 00:30:05.000000 refuel-autolabel-0.0.9/src/autolabel/data_loaders/validation.py
+drwxr-xr-x   0 nihit      (501) staff       (20)        0 2023-07-23 19:19:03.361675 refuel-autolabel-0.0.9/src/autolabel/data_models/
+-rw-r--r--   0 nihit      (501) staff       (20)      195 2023-05-16 00:22:56.000000 refuel-autolabel-0.0.9/src/autolabel/data_models/__init__.py
+-rw-r--r--   0 nihit      (501) staff       (20)     2001 2023-06-14 01:40:05.000000 refuel-autolabel-0.0.9/src/autolabel/data_models/annotation.py
+-rw-r--r--   0 nihit      (501) staff       (20)       71 2023-05-14 02:11:15.000000 refuel-autolabel-0.0.9/src/autolabel/data_models/base.py
+-rw-r--r--   0 nihit      (501) staff       (20)     2036 2023-06-10 22:44:42.000000 refuel-autolabel-0.0.9/src/autolabel/data_models/cache.py
+-rw-r--r--   0 nihit      (501) staff       (20)     1071 2023-05-14 02:11:15.000000 refuel-autolabel-0.0.9/src/autolabel/data_models/dataset.py
+-rw-r--r--   0 nihit      (501) staff       (20)      928 2023-05-14 02:11:15.000000 refuel-autolabel-0.0.9/src/autolabel/data_models/task.py
+-rw-r--r--   0 nihit      (501) staff       (20)     2625 2023-06-14 01:40:05.000000 refuel-autolabel-0.0.9/src/autolabel/data_models/task_run.py
+drwxr-xr-x   0 nihit      (501) staff       (20)        0 2023-07-23 19:19:03.362316 refuel-autolabel-0.0.9/src/autolabel/database/
+-rw-r--r--   0 nihit      (501) staff       (20)       77 2023-05-14 02:11:15.000000 refuel-autolabel-0.0.9/src/autolabel/database/__init__.py
+-rw-r--r--   0 nihit      (501) staff       (20)      643 2023-07-06 04:47:37.000000 refuel-autolabel-0.0.9/src/autolabel/database/engine.py
+-rw-r--r--   0 nihit      (501) staff       (20)     2788 2023-06-14 01:40:05.000000 refuel-autolabel-0.0.9/src/autolabel/database/state_manager.py
+drwxr-xr-x   0 nihit      (501) staff       (20)        0 2023-07-23 19:19:03.364847 refuel-autolabel-0.0.9/src/autolabel/few_shot/
+-rw-r--r--   0 nihit      (501) staff       (20)     4141 2023-07-21 00:43:46.000000 refuel-autolabel-0.0.9/src/autolabel/few_shot/__init__.py
+-rw-r--r--   0 nihit      (501) staff       (20)     1295 2023-05-14 02:11:15.000000 refuel-autolabel-0.0.9/src/autolabel/few_shot/fixed_example_selector.py
+-rw-r--r--   0 nihit      (501) staff       (20)     6328 2023-07-07 22:34:09.000000 refuel-autolabel-0.0.9/src/autolabel/few_shot/label_diversity_example_selector.py
+-rw-r--r--   0 nihit      (501) staff       (20)    17522 2023-07-21 00:43:46.000000 refuel-autolabel-0.0.9/src/autolabel/few_shot/vector_store.py
+-rw-r--r--   0 nihit      (501) staff       (20)    19030 2023-07-23 18:58:04.000000 refuel-autolabel-0.0.9/src/autolabel/labeler.py
+drwxr-xr-x   0 nihit      (501) staff       (20)        0 2023-07-23 19:19:03.366365 refuel-autolabel-0.0.9/src/autolabel/metrics/
+-rw-r--r--   0 nihit      (501) staff       (20)      207 2023-07-23 18:58:04.000000 refuel-autolabel-0.0.9/src/autolabel/metrics/__init__.py
+-rw-r--r--   0 nihit      (501) staff       (20)     1096 2023-07-23 18:58:04.000000 refuel-autolabel-0.0.9/src/autolabel/metrics/accuracy.py
+-rw-r--r--   0 nihit      (501) staff       (20)     1134 2023-07-23 18:58:04.000000 refuel-autolabel-0.0.9/src/autolabel/metrics/auroc.py
+-rw-r--r--   0 nihit      (501) staff       (20)      350 2023-07-23 18:58:04.000000 refuel-autolabel-0.0.9/src/autolabel/metrics/base.py
+-rw-r--r--   0 nihit      (501) staff       (20)      789 2023-07-23 18:58:04.000000 refuel-autolabel-0.0.9/src/autolabel/metrics/completion_rate.py
+-rw-r--r--   0 nihit      (501) staff       (20)     3688 2023-07-23 18:58:04.000000 refuel-autolabel-0.0.9/src/autolabel/metrics/f1.py
+-rw-r--r--   0 nihit      (501) staff       (20)      444 2023-07-23 18:58:04.000000 refuel-autolabel-0.0.9/src/autolabel/metrics/support.py
+drwxr-xr-x   0 nihit      (501) staff       (20)        0 2023-07-23 19:19:03.367687 refuel-autolabel-0.0.9/src/autolabel/models/
+-rw-r--r--   0 nihit      (501) staff       (20)     2107 2023-07-06 04:47:37.000000 refuel-autolabel-0.0.9/src/autolabel/models/__init__.py
+-rw-r--r--   0 nihit      (501) staff       (20)     2498 2023-07-23 18:58:04.000000 refuel-autolabel-0.0.9/src/autolabel/models/anthropic.py
+-rw-r--r--   0 nihit      (501) staff       (20)     5338 2023-07-23 18:58:04.000000 refuel-autolabel-0.0.9/src/autolabel/models/base.py
+-rw-r--r--   0 nihit      (501) staff       (20)     2005 2023-07-23 18:58:04.000000 refuel-autolabel-0.0.9/src/autolabel/models/cohere.py
+-rw-r--r--   0 nihit      (501) staff       (20)     3890 2023-07-23 18:58:04.000000 refuel-autolabel-0.0.9/src/autolabel/models/hf_pipeline.py
+-rw-r--r--   0 nihit      (501) staff       (20)     6166 2023-07-23 18:58:04.000000 refuel-autolabel-0.0.9/src/autolabel/models/openai.py
+-rw-r--r--   0 nihit      (501) staff       (20)     5184 2023-07-23 18:58:04.000000 refuel-autolabel-0.0.9/src/autolabel/models/palm.py
+-rw-r--r--   0 nihit      (501) staff       (20)     3862 2023-07-23 18:58:04.000000 refuel-autolabel-0.0.9/src/autolabel/models/refuel.py
+-rw-r--r--   0 nihit      (501) staff       (20)     5939 2023-07-23 18:58:04.000000 refuel-autolabel-0.0.9/src/autolabel/schema.py
+drwxr-xr-x   0 nihit      (501) staff       (20)        0 2023-07-23 19:19:03.369094 refuel-autolabel-0.0.9/src/autolabel/tasks/
+-rw-r--r--   0 nihit      (501) staff       (20)     1298 2023-07-06 04:47:37.000000 refuel-autolabel-0.0.9/src/autolabel/tasks/__init__.py
+-rw-r--r--   0 nihit      (501) staff       (20)     5161 2023-07-23 18:58:04.000000 refuel-autolabel-0.0.9/src/autolabel/tasks/base.py
+-rw-r--r--   0 nihit      (501) staff       (20)     5269 2023-07-23 18:58:04.000000 refuel-autolabel-0.0.9/src/autolabel/tasks/classification.py
+-rw-r--r--   0 nihit      (501) staff       (20)     5218 2023-07-23 18:58:04.000000 refuel-autolabel-0.0.9/src/autolabel/tasks/entity_matching.py
+-rw-r--r--   0 nihit      (501) staff       (20)     5462 2023-07-23 18:58:04.000000 refuel-autolabel-0.0.9/src/autolabel/tasks/multilabel_classification.py
+-rw-r--r--   0 nihit      (501) staff       (20)    11689 2023-07-23 18:58:04.000000 refuel-autolabel-0.0.9/src/autolabel/tasks/named_entity_recognition.py
+-rw-r--r--   0 nihit      (501) staff       (20)     4963 2023-07-23 18:58:04.000000 refuel-autolabel-0.0.9/src/autolabel/tasks/question_answering.py
+-rw-r--r--   0 nihit      (501) staff       (20)     1653 2023-07-23 18:58:04.000000 refuel-autolabel-0.0.9/src/autolabel/tasks/utils.py
+-rw-r--r--   0 nihit      (501) staff       (20)    10431 2023-07-23 18:58:04.000000 refuel-autolabel-0.0.9/src/autolabel/utils.py
+drwxr-xr-x   0 nihit      (501) staff       (20)        0 2023-07-23 19:19:03.369824 refuel-autolabel-0.0.9/src/refuel_autolabel.egg-info/
+-rw-r--r--   0 nihit      (501) staff       (20)    10381 2023-07-23 19:19:03.000000 refuel-autolabel-0.0.9/src/refuel_autolabel.egg-info/PKG-INFO
+-rw-r--r--   0 nihit      (501) staff       (20)     2065 2023-07-23 19:19:03.000000 refuel-autolabel-0.0.9/src/refuel_autolabel.egg-info/SOURCES.txt
+-rw-r--r--   0 nihit      (501) staff       (20)        1 2023-07-23 19:19:03.000000 refuel-autolabel-0.0.9/src/refuel_autolabel.egg-info/dependency_links.txt
+-rw-r--r--   0 nihit      (501) staff       (20)      919 2023-07-23 19:19:03.000000 refuel-autolabel-0.0.9/src/refuel_autolabel.egg-info/requires.txt
+-rw-r--r--   0 nihit      (501) staff       (20)       10 2023-07-23 19:19:03.000000 refuel-autolabel-0.0.9/src/refuel_autolabel.egg-info/top_level.txt
```

### Comparing `refuel-autolabel-0.0.8/LICENSE` & `refuel-autolabel-0.0.9/LICENSE`

 * *Files identical despite different names*

### Comparing `refuel-autolabel-0.0.8/PKG-INFO` & `refuel-autolabel-0.0.9/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: refuel-autolabel
-Version: 0.0.8
+Version: 0.0.9
 Summary: Label, clean and enrich text datasets with LLMs
 Author-email: "Refuel.ai" <support@refuel.ai>
 License: MIT License
         
         Copyright (c) 2023 refuel-ai
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: refuel-autolabel Version: 0.0.8 Summary: Label,
+Metadata-Version: 2.1 Name: refuel-autolabel Version: 0.0.9 Summary: Label,
 clean and enrich text datasets with LLMs Author-email: "Refuel.ai"
 refuel.ai> License: MIT License Copyright (c) 2023 refuel-ai Permission is
 hereby granted, free of charge, to any person obtaining a copy of this software
 and associated documentation files (the "Software"), to deal in the Software
 without restriction, including without limitation the rights to use, copy,
 modify, merge, publish, distribute, sublicense, and/or sell copies of the
 Software, and to permit persons to whom the Software is furnished to do so,
```

### Comparing `refuel-autolabel-0.0.8/README.md` & `refuel-autolabel-0.0.9/README.md`

 * *Files identical despite different names*

### Comparing `refuel-autolabel-0.0.8/pyproject.toml` & `refuel-autolabel-0.0.9/pyproject.toml`

 * *Files 4% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools>=65.0.0", "wheel >= 0.38"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "refuel-autolabel"
-version = "0.0.8"
+version = "0.0.9"
 description = "Label, clean and enrich text datasets with LLMs"
 readme = "README.md"
 authors = [{ name = "Refuel.ai", email = "support@refuel.ai" }]
 license = { file = "LICENSE" }
 classifiers = [
     "Development Status :: 4 - Beta",
     "License :: OSI Approved :: MIT License",
```

### Comparing `refuel-autolabel-0.0.8/src/autolabel/cache/base.py` & `refuel-autolabel-0.0.9/src/autolabel/cache/base.py`

 * *Files identical despite different names*

### Comparing `refuel-autolabel-0.0.8/src/autolabel/cache/sqlalchemy_cache.py` & `refuel-autolabel-0.0.9/src/autolabel/cache/sqlalchemy_cache.py`

 * *Files identical despite different names*

### Comparing `refuel-autolabel-0.0.8/src/autolabel/confidence.py` & `refuel-autolabel-0.0.9/src/autolabel/confidence.py`

 * *Files 1% similar despite different names*

```diff
@@ -82,15 +82,15 @@
             token_str = list(token.keys())[0]
             if token_str.lower() == "yes":
                 return math.e ** token[token_str]
             elif token_str.lower() == "no":
                 return -math.e ** token[token_str]
         return 0
 
-    def calculate(self, model_generation: LLMAnnotation, **kwargs) -> LLMAnnotation:
+    def calculate(self, model_generation: LLMAnnotation, **kwargs) -> float:
         if self.score_type not in self.SUPPORTED_CALCULATORS:
             raise NotImplementedError()
 
         logprobs = None
         if not self.llm.returns_token_probs():
             if model_generation.raw_response == "":
                 model_generation.confidence_score = 0
@@ -106,16 +106,15 @@
             logprobs = model_generation.generation_info["logprobs"]["top_logprobs"]
 
         confidence = self.SUPPORTED_CALCULATORS[self.score_type](
             model_generation=model_generation,
             logprobs=logprobs,
             **kwargs,
         )
-        model_generation.confidence_score = confidence
-        return model_generation
+        return confidence
 
     @retry(
         reraise=True,
         stop=stop_after_attempt(5),
         wait=wait_exponential(multiplier=1, min=2, max=10),
         before_sleep=before_sleep_log(logger, logging.WARNING),
     )
```

### Comparing `refuel-autolabel-0.0.8/src/autolabel/configs/base.py` & `refuel-autolabel-0.0.9/src/autolabel/configs/base.py`

 * *Files identical despite different names*

### Comparing `refuel-autolabel-0.0.8/src/autolabel/configs/config.py` & `refuel-autolabel-0.0.9/src/autolabel/configs/config.py`

 * *Files identical despite different names*

### Comparing `refuel-autolabel-0.0.8/src/autolabel/configs/schema.py` & `refuel-autolabel-0.0.9/src/autolabel/configs/schema.py`

 * *Files identical despite different names*

### Comparing `refuel-autolabel-0.0.8/src/autolabel/data_loaders/__init__.py` & `refuel-autolabel-0.0.9/src/autolabel/data_loaders/__init__.py`

 * *Files identical despite different names*

### Comparing `refuel-autolabel-0.0.8/src/autolabel/data_loaders/read_datasets.py` & `refuel-autolabel-0.0.9/src/autolabel/data_loaders/read_datasets.py`

 * *Files identical despite different names*

### Comparing `refuel-autolabel-0.0.8/src/autolabel/data_loaders/validation.py` & `refuel-autolabel-0.0.9/src/autolabel/data_loaders/validation.py`

 * *Files 3% similar despite different names*

```diff
@@ -105,27 +105,60 @@
     ]  # A QA task may or may not have a unique set of label list
 
     def validate(self, value: str):
         """Since question answering is arbitarary task we have no validation"""
         pass
 
 
+class MLCTaskValidate(BaseModel):
+    """Validate Multilabel Classification Task
+
+    As of now we assume that the input label_column is a string
+
+    The label column can be a delimited string or a string of list
+    """
+
+    label_column: str
+    labels_set: set  # A Multilabel Classification Task should have a unique set of labels in config
+
+    def validate(self, value: str):
+        if value.startswith("[") and value.endswith("]"):
+            try:
+                seed_labels = eval(value)
+                if not isinstance(seed_labels, list):
+                    raise ValueError(
+                        f"value: '{value}' is not a list of labels as expected"
+                    )
+                unmatched_label = set(seed_labels) - self.labels_set
+                if len(unmatched_label) != 0:
+                    raise ValueError(
+                        f"labels: '{unmatched_label}' not in prompt/labels provided in config "
+                    )
+            except SyntaxError:
+                raise
+        else:
+            # TODO: split by delimiter specified in config and validate each label
+            pass
+
+
 TaskTypeValidate = Union[
     NERTaskValidate,
     ClassificationTaskValidate,
     EMTaskValidate,
     QATaskValidate,
+    MLCTaskValidate,
 ]
 
 
 class DataValidationTasks(BaseModel):
     classification: TaskTypeValidate = ClassificationTaskValidate
     named_entity_recognition: TaskTypeValidate = NERTaskValidate
     entity_matching: TaskTypeValidate = EMTaskValidate
     question_answering: TaskTypeValidate = QATaskValidate
+    multilabel_classification: TaskTypeValidate = MLCTaskValidate
 
 
 class TaskDataValidation:
     """Task Validation"""
 
     def __init__(self, config: AutolabelConfig):
         """Task Validation
```

### Comparing `refuel-autolabel-0.0.8/src/autolabel/data_models/annotation.py` & `refuel-autolabel-0.0.9/src/autolabel/data_models/annotation.py`

 * *Files identical despite different names*

### Comparing `refuel-autolabel-0.0.8/src/autolabel/data_models/cache.py` & `refuel-autolabel-0.0.9/src/autolabel/data_models/cache.py`

 * *Files identical despite different names*

### Comparing `refuel-autolabel-0.0.8/src/autolabel/data_models/dataset.py` & `refuel-autolabel-0.0.9/src/autolabel/data_models/dataset.py`

 * *Files identical despite different names*

### Comparing `refuel-autolabel-0.0.8/src/autolabel/data_models/task.py` & `refuel-autolabel-0.0.9/src/autolabel/data_models/task.py`

 * *Files identical despite different names*

### Comparing `refuel-autolabel-0.0.8/src/autolabel/data_models/task_run.py` & `refuel-autolabel-0.0.9/src/autolabel/data_models/task_run.py`

 * *Files identical despite different names*

### Comparing `refuel-autolabel-0.0.8/src/autolabel/database/engine.py` & `refuel-autolabel-0.0.9/src/autolabel/database/engine.py`

 * *Files identical despite different names*

### Comparing `refuel-autolabel-0.0.8/src/autolabel/database/state_manager.py` & `refuel-autolabel-0.0.9/src/autolabel/database/state_manager.py`

 * *Files identical despite different names*

### Comparing `refuel-autolabel-0.0.8/src/autolabel/few_shot/__init__.py` & `refuel-autolabel-0.0.9/src/autolabel/few_shot/__init__.py`

 * *Files 3% similar despite different names*

```diff
@@ -45,15 +45,18 @@
 
 class ExampleSelectorFactory:
     CANDIDATE_EXAMPLES_FACTOR = 5
     MAX_CANDIDATE_EXAMPLES = 100
 
     @staticmethod
     def initialize_selector(
-        config: AutolabelConfig, examples: List[Dict], columns: List[str]
+        config: AutolabelConfig,
+        examples: List[Dict],
+        columns: List[str],
+        cache: bool = True,
     ) -> BaseExampleSelector:
         algorithm = config.few_shot_algorithm()
         if not algorithm:
             return None
         try:
             algorithm = FewShotAlgorithm(algorithm)
         except ValueError as e:
@@ -96,8 +99,15 @@
             FewShotAlgorithm.LABEL_DIVERSITY_RANDOM,
             FewShotAlgorithm.LABEL_DIVERSITY_SIMILARITY,
         ]:
             params["label_key"] = config.label_column()
             params["num_labels"] = len(config.labels_list())
 
         example_cls = ALGORITHM_TO_IMPLEMENTATION[algorithm]
+
+        if algorithm not in [
+            FewShotAlgorithm.FIXED,
+            FewShotAlgorithm.LABEL_DIVERSITY_RANDOM,
+        ]:
+            params["cache"] = cache
+
         return example_cls.from_examples(**params)
```

### Comparing `refuel-autolabel-0.0.8/src/autolabel/few_shot/fixed_example_selector.py` & `refuel-autolabel-0.0.9/src/autolabel/few_shot/fixed_example_selector.py`

 * *Files identical despite different names*

### Comparing `refuel-autolabel-0.0.8/src/autolabel/few_shot/label_diversity_example_selector.py` & `refuel-autolabel-0.0.9/src/autolabel/few_shot/label_diversity_example_selector.py`

 * *Files identical despite different names*

### Comparing `refuel-autolabel-0.0.8/src/autolabel/few_shot/vector_store.py` & `refuel-autolabel-0.0.9/src/autolabel/few_shot/vector_store.py`

 * *Files 13% similar despite different names*

```diff
@@ -1,20 +1,25 @@
 from __future__ import annotations
 
 import heapq
 from itertools import groupby
 from typing import Any, Callable, Dict, Iterable, List, Optional, Tuple, Type
 
+from autolabel.database import create_db_engine
+
 import numpy as np
 import torch
 from langchain.docstore.document import Document
 from langchain.embeddings.base import Embeddings
 from langchain.vectorstores.base import VectorStore
 from langchain.vectorstores.utils import maximal_marginal_relevance
 from torch import Tensor
+import pickle
+
+EMBEDDINGS_TABLE = "autolabel_embeddings"
 
 
 def _results_to_docs_and_scores(results: Any) -> List[Tuple[Document, float]]:
     return [
         (Document(page_content=result[0], metadata=result[1] or {}), result[2])
         for result in zip(
             results["documents"][0],
@@ -132,35 +137,107 @@
 class VectorStoreWrapper(VectorStore):
     def __init__(
         self,
         embedding_function: Optional[Embeddings] = None,
         corpus_embeddings: Optional[Tensor] = None,
         texts: Optional[List[str]] = None,
         metadatas: Optional[List[Dict[str, str]]] = None,
+        cache: bool = True,
     ) -> None:
         self._embedding_function = embedding_function
         self._corpus_embeddings = corpus_embeddings
         self._texts = texts
         self._metadatas = metadatas
+        if cache:
+            self._db_engine = create_db_engine()
+            with self._db_engine.connect() as conn:
+                conn.execute(
+                    f"CREATE TABLE IF NOT EXISTS {EMBEDDINGS_TABLE} (embedding_function TEXT, text TEXT, embedding BLOB)"
+                )
+        else:
+            self._db_engine = None
+
+    def _get_embeddings(self, texts: Iterable[str]) -> List[List[float]]:
+        """Get embeddings from the database. If not found, compute them and add them to the database.
+
+        If no database is used, compute the embeddings and return them.
+
+        Args:
+            texts (Iterable[str]): Iterable of texts to embed.
+        Returns:
+            List[List[float]]: List of embeddings.
+        """
+        if self._db_engine:
+            with self._db_engine.connect() as conn:
+                embeddings = []
+                uncached_texts = []
+                uncached_texts_indices = []
+                for idx, text in enumerate(texts):
+                    result = conn.execute(
+                        f"SELECT embedding FROM {EMBEDDINGS_TABLE} WHERE embedding_function = ? AND text = ?",
+                        self._embedding_function.model
+                        if self._embedding_function.__class__.__name__
+                        != "HuggingFaceEmbeddings"
+                        else self._embedding_function.model_name,
+                        text,
+                    ).fetchone()
+                    if result:
+                        embeddings.append(pickle.loads(result[0]))
+                    else:
+                        embeddings.append(None)
+                        uncached_texts.append(text)
+                        uncached_texts_indices.append(idx)
+
+                uncached_embeddings = self._embedding_function.embed_documents(
+                    uncached_texts
+                )
+                self._add_embeddings_to_cache(uncached_texts, uncached_embeddings)
+                for idx, embedding in zip(uncached_texts_indices, uncached_embeddings):
+                    embeddings[idx] = embedding
+
+                return embeddings
+        else:
+            return self._embedding_function.embed_documents(list(texts))
+
+    def _add_embeddings_to_cache(
+        self, texts: Iterable[str], embeddings: List[List[float]]
+    ) -> None:
+        """Save embeddings to the database. If self._db_engine is None, do nothing.
+        Args:
+            texts (Iterable[str]): Iterable of texts.
+            embeddings (List[List[float]]): List of embeddings.
+        """
+        if self._db_engine:
+            with self._db_engine.connect() as conn:
+                for text, embedding in zip(texts, embeddings):
+                    conn.execute(
+                        f"INSERT INTO {EMBEDDINGS_TABLE} (embedding_function, text, embedding) VALUES (?, ?, ?)",
+                        self._embedding_function.model
+                        if self._embedding_function.__class__.__name__
+                        != "HuggingFaceEmbeddings"
+                        else self._embedding_function.model_name,
+                        text,
+                        pickle.dumps(embedding),
+                    )
 
     def add_texts(
         self,
         texts: Iterable[str],
         metadatas: Optional[List[Dict[str, str]]] = None,
     ) -> List[str]:
         """Run texts through the embeddings and add to the vectorstore. Currently, the vectorstore is reinitialized each time, because we do not require a persistent vector store for example selection.
         Args:
             texts (Iterable[str]): Texts to add to the vectorstore.
             metadatas (Optional[List[dict]], optional): Optional list of metadatas.
         Returns:
             List[str]: List of IDs of the added texts.
         """
-        embeddings = None
         if self._embedding_function is not None:
-            embeddings = self._embedding_function.embed_documents(list(texts))
+            embeddings = self._get_embeddings(texts)
+
         self._corpus_embeddings = torch.tensor(embeddings)
         self._texts = texts
         self._metadatas = metadatas
         return metadatas
 
     def similarity_search(
         self,
@@ -192,15 +269,15 @@
             query (str): Query text to search for.
             k (int): Number of results to return. Defaults to 4.
             filter (Optional[Dict[str, str]]): Filter by metadata. Defaults to None.
         Returns:
             List[Tuple[Document, float]]: List of documents most similar to the query
                 text with distance in float.
         """
-        query_embeddings = torch.tensor([self._embedding_function.embed_query(query)])
+        query_embeddings = torch.tensor([self._get_embeddings([query])[0]])
         result_ids_and_scores = semantic_search(
             corpus_embeddings=self._corpus_embeddings,
             query_embeddings=query_embeddings,
             top_k=k,
         )
         result_ids = [result["corpus_id"] for result in result_ids_and_scores[0]]
         scores = [result["score"] for result in result_ids_and_scores[0]]
@@ -244,15 +321,15 @@
             query (str): Query text to search for.
             k (int): Number of results to return. Defaults to 4.
             filter (Optional[Dict[str, str]]): Filter by metadata. Defaults to None.
         Returns:
             List[Tuple[Document, float]]: List of documents most similar to the query
                 text with distance in float.
         """
-        query_embeddings = torch.tensor([self._embedding_function.embed_query(query)])
+        query_embeddings = torch.tensor([self._get_embeddings([query])[0]])
         data = []
         data = zip(self._corpus_embeddings, self._texts, self._metadatas)
         sorted_data = sorted(data, key=lambda item: item[2].get(label_key))
 
         documents = []
         scores = []
         metadatas = []
@@ -291,15 +368,15 @@
         self,
         query: str,
         k: int = 4,
         fetch_k: int = 20,
         lambda_mult: float = 0.5,
         **kwargs: Any,
     ) -> List[Document]:
-        query_embedding = self._embedding_function.embed_query(query)
+        query_embedding = self._get_embeddings([query])[0]
         query_embeddings = torch.tensor([query_embedding])
         result_ids_and_scores = semantic_search(
             corpus_embeddings=self._corpus_embeddings,
             query_embeddings=query_embeddings,
             top_k=fetch_k,
         )
         result_ids = [result["corpus_id"] for result in result_ids_and_scores[0]]
@@ -340,23 +417,29 @@
 
     @classmethod
     def from_texts(
         cls: Type[VectorStoreWrapper],
         texts: List[str],
         embedding: Optional[Embeddings] = None,
         metadatas: Optional[List[dict]] = None,
+        cache: bool = True,
         **kwargs: Any,
     ) -> VectorStoreWrapper:
         """Create a vectorstore from raw text.
         The data will be ephemeral in-memory.
         Args:
             texts (List[str]): List of texts to add to the collection.
             embedding (Optional[Embeddings]): Embedding function. Defaults to None.
             metadatas (Optional[List[dict]]): List of metadatas. Defaults to None.
+            cache (bool): Whether to cache the embeddings. Defaults to True.
         Returns:
             vector_store: Vectorstore with seedset embeddings
         """
         vector_store = cls(
-            embedding_function=embedding, corpus_embeddings=None, texts=None, **kwargs
+            embedding_function=embedding,
+            corpus_embeddings=None,
+            texts=None,
+            cache=cache,
+            **kwargs,
         )
         vector_store.add_texts(texts=texts, metadatas=metadatas)
         return vector_store
```

### Comparing `refuel-autolabel-0.0.8/src/autolabel/labeler.py` & `refuel-autolabel-0.0.9/src/autolabel/labeler.py`

 * *Files 11% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 import logging
 import os
-import sys
 from typing import Dict, List, Optional, Tuple, Union
+import json
 
 import numpy as np
 import pandas as pd
 from rich import print as pprint
 from rich.console import Console
 from rich.prompt import Confirm
 
@@ -13,30 +13,35 @@
 from autolabel.confidence import ConfidenceCalculator
 from autolabel.configs import AutolabelConfig
 from autolabel.data_loaders import DatasetLoader
 from autolabel.data_models import AnnotationModel, TaskRunModel
 from autolabel.database import StateManager
 from autolabel.few_shot import ExampleSelectorFactory
 from autolabel.models import BaseModel, ModelFactory
-from autolabel.schema import LLMAnnotation, MetricResult, TaskRun, TaskStatus
+from autolabel.metrics import BaseMetric
+from autolabel.schema import (
+    LLMAnnotation,
+    MetricResult,
+    TaskRun,
+    TaskStatus,
+)
 from autolabel.tasks import TaskFactory
 from autolabel.utils import maybe_round, print_table, track, track_with_stats
 
 console = Console()
 logger = logging.getLogger(__name__)
 
 COST_TABLE_STYLES = {
     "parameter": "magenta bold",
     "value": "green bold",
 }
 METRIC_TABLE_STYLE = "cyan bold"
 
 
 class LabelingAgent:
-    CHUNK_SIZE = 5
     COST_KEY = "Cost in $"
 
     def __init__(
         self,
         config: Union[str, Dict],
         cache: Optional[bool] = True,
     ) -> None:
@@ -53,14 +58,15 @@
     def run(
         self,
         dataset: Union[str, pd.DataFrame],
         max_items: Optional[int] = None,
         output_name: Optional[str] = None,
         start_index: Optional[int] = 0,
         eval_every: Optional[int] = 50,
+        additional_metrics: Optional[List[BaseMetric]] = [],
     ) -> Tuple[pd.Series, pd.DataFrame, List[MetricResult]]:
         """Labels data in a given dataset. Output written to new CSV file.
 
         Args:
             dataset: path to CSV dataset to be annotated
             max_items: maximum items in dataset to be annotated
             output_name: custom name of output CSV file
@@ -84,15 +90,18 @@
 
         # Initialize task run and check if it already exists
         self.task_run = self.db.get_task_run(self.task_object.id, self.dataset.id)
         # Resume/Delete the task if it already exists or create a new task run
         if self.task_run:
             logger.info("Task run already exists.")
             self.task_run = self.handle_existing_task_run(
-                self.task_run, csv_file_name, gt_labels=dataset_loader.gt_labels
+                self.task_run,
+                csv_file_name,
+                gt_labels=dataset_loader.gt_labels,
+                additional_metrics=additional_metrics,
             )
         else:
             self.task_run = self.db.create_task_run(
                 csv_file_name, self.task_object.id, self.dataset.id
             )
 
         # Get the seed examples from the dataset config
@@ -110,157 +119,151 @@
             and self.config.explanation_column() not in list(seed_examples[0].keys())
         ):
             raise ValueError(
                 f"Explanation column {self.config.explanation_column()} not found in dataset.\nMake sure that explanations were generated using labeler.generate_explanations(seed_file)."
             )
 
         self.example_selector = ExampleSelectorFactory.initialize_selector(
-            self.config, seed_examples, dataset_loader.dat.keys().tolist()
+            self.config,
+            seed_examples,
+            dataset_loader.dat.keys().tolist(),
+            cache=self.cache is not None,
         )
 
         num_failures = 0
         current_index = self.task_run.current_index
         cost = 0.0
         postfix_dict = {}
 
-        indices = range(current_index, len(dataset_loader.inputs), self.CHUNK_SIZE)
+        indices = range(current_index, len(dataset_loader.inputs))
+
         for current_index in track_with_stats(
             indices,
             postfix_dict,
             total=len(dataset_loader.inputs) - current_index,
-            advance=self.CHUNK_SIZE,
             console=console,
         ):
-            chunk = dataset_loader.inputs[
-                current_index : current_index + self.CHUNK_SIZE
-            ]
-            final_prompts = []
-            for i, input_i in enumerate(chunk):
-                # Fetch few-shot seed examples
-                if self.example_selector:
-                    examples = self.example_selector.select_examples(input_i)
-                else:
-                    examples = []
+            chunk = dataset_loader.inputs[current_index]
+
+            if self.example_selector:
+                examples = self.example_selector.select_examples(chunk)
+            else:
+                examples = []
                 # Construct Prompt to pass to LLM
-                final_prompt = self.task.construct_prompt(input_i, examples)
-                final_prompts.append(final_prompt)
+            final_prompt = self.task.construct_prompt(chunk, examples)
 
-            # Get response from LLM
-            try:
-                response, curr_cost = self.llm.label(final_prompts)
-            except Exception as e:
-                # TODO (dhruva): We need to handle this case carefully
-                # When we erorr out, we will have less elements in the llm_labels
-                # than the gt_labels array, with the 1:1 mapping not being
-                # maintained either. We should either remove the elements we errored
-                # out on from gt_labels or add None labels to the llm_labels.
-                logger.error(
-                    "Error in generating response:" + repr(e), "Prompt: ", chunk
-                )
-                for i in range(len(chunk)):
+            response = self.llm.label([final_prompt])
+            for i, generations, error in zip(
+                range(len(response.generations)), response.generations, response.errors
+            ):
+                if error is not None:
                     annotation = LLMAnnotation(
                         successfully_labeled=False,
                         label=self.task.NULL_LABEL_TOKEN,
                         raw_response="",
-                        curr_sample=chunk[i],
-                        prompt=final_prompts[i],
+                        curr_sample=json.dumps(chunk),
+                        prompt=final_prompt,
                         confidence_score=0,
+                        error=error,
                     )
-                    AnnotationModel.create_from_llm_annotation(
-                        self.db.session,
-                        annotation,
-                        current_index + i,
-                        self.task_run.id,
-                    )
-                num_failures += len(chunk)
-                response = None
-
-            if response is not None:
-                for i in range(len(response.generations)):
-                    response_item = response.generations[i]
+                else:
                     annotations = []
-                    for generation in response_item:
+                    for generation in generations:
+                        annotation = self.task.parse_llm_response(
+                            generation, chunk, final_prompt
+                        )
+
                         if self.config.confidence():
-                            annotation = self.confidence.calculate(
-                                model_generation=self.task.parse_llm_response(
-                                    generation, chunk[i], final_prompts[i]
-                                ),
-                                prompt=final_prompts[i],
-                            )
-                        else:
-                            annotation = self.task.parse_llm_response(
-                                generation, chunk[i], final_prompts[i]
+                            annotation.confidence_score = self.confidence.calculate(
+                                model_generation=annotation,
+                                prompt=final_prompt,
                             )
+
                         annotations.append(annotation)
-                    final_annotation = self.majority_annotation(annotations)
-                    AnnotationModel.create_from_llm_annotation(
-                        self.db.session,
-                        final_annotation,
-                        current_index + i,
-                        self.task_run.id,
-                    )
-            cost += curr_cost
+                    annotation = self.majority_annotation(annotations)
+
+                # Store the annotation in the database
+                AnnotationModel.create_from_llm_annotation(
+                    self.db.session,
+                    annotation,
+                    current_index + i,
+                    self.task_run.id,
+                )
+
+            cost += sum(response.costs)
             postfix_dict[self.COST_KEY] = f"{cost:.2f}"
 
             # Evaluate the task every eval_every examples
-            if (current_index + self.CHUNK_SIZE) % eval_every == 0:
+            if (current_index + 1) % eval_every == 0:
                 db_result = AnnotationModel.get_annotations_by_task_run_id(
                     self.db.session, self.task_run.id
                 )
                 llm_labels = [LLMAnnotation(**a.llm_annotation) for a in db_result]
                 if dataset_loader.gt_labels:
                     eval_result = self.task.eval(
-                        llm_labels, dataset_loader.gt_labels[: len(llm_labels)]
+                        llm_labels,
+                        dataset_loader.gt_labels[: len(llm_labels)],
+                        additional_metrics=additional_metrics,
                     )
 
                     for m in eval_result:
-                        if not isinstance(m.value, list) or len(m.value) < 1:
+                        # This is a row wise metric
+                        if isinstance(m.value, list):
                             continue
-                        elif isinstance(m.value[0], float):
-                            postfix_dict[m.name] = f"{m.value[0]:.4f}"
-                        elif isinstance(m.value[0], int):
-                            postfix_dict[m.name] = f"{m.value[0]}"
-                        elif len(m.value[0]) > 0:
-                            postfix_dict[m.name] = f"{m.value[0][0]:.4f}"
+                        postfix_dict[m.name] = (
+                            f"{m.value:.4f}" if isinstance(m.value, float) else m.value
+                        )
 
             # Update task run state
             self.task_run = self.save_task_run_state(
                 current_index=current_index + len(chunk)
             )
 
         db_result = AnnotationModel.get_annotations_by_task_run_id(
             self.db.session, self.task_run.id
         )
         llm_labels = [LLMAnnotation(**a.llm_annotation) for a in db_result]
         eval_result = None
         # if true labels are provided, evaluate accuracy of predictions
         if dataset_loader.gt_labels:
             eval_result = self.task.eval(
-                llm_labels, dataset_loader.gt_labels[: len(llm_labels)]
+                llm_labels,
+                dataset_loader.gt_labels[: len(llm_labels)],
+                additional_metrics=additional_metrics,
             )
             table = {}
             # TODO: serialize and write to file
             for m in eval_result:
-                if isinstance(m.value, list) and len(m.value) > 0:
-                    table[m.name] = m.value
+                if isinstance(m.value, list):
+                    continue
                 else:
-                    print(f"Metric: {m.name}: {maybe_round(m.value)}")
+                    table[m.name] = m.value
             print(f"Actual Cost: {maybe_round(cost)}")
             print_table(table, console=console, default_style=METRIC_TABLE_STYLE)
 
         # Write output to CSV
         output_df = dataset_loader.dat.copy()
         output_df[self.config.task_name() + "_llm_labeled_successfully"] = [
             l.successfully_labeled for l in llm_labels
         ]
+        output_df[self.config.task_name() + "_llm_error"] = [
+            l.error for l in llm_labels
+        ]
         output_df[self.config.task_name() + "_llm_label"] = [
             l.label for l in llm_labels
         ]
         if self.config.confidence():
-            output_df["llm_confidence"] = [l.confidence_score for l in llm_labels]
+            output_df[self.config.task_name() + "_llm_confidence"] = [
+                l.confidence_score for l in llm_labels
+            ]
+
+        if self.config.chain_of_thought():
+            output_df[self.config.task_name() + "_llm_explanation"] = [
+                l.explanation for l in llm_labels
+            ]
 
         # Only save to csv if output_name is provided or dataset is a string
         if not output_name and isinstance(dataset, str):
             output_name = (
                 dataset.rsplit(".", 1)[0] + "_labeled." + dataset.rsplit(".", 1)[1]
             )
 
@@ -325,15 +328,18 @@
             and self.config.explanation_column() not in list(seed_examples[0].keys())
         ):
             raise ValueError(
                 f"Explanation column {self.config.explanation_column()} not found in dataset.\nMake sure that explanations were generated using labeler.generate_explanations(seed_file)."
             )
 
         self.example_selector = ExampleSelectorFactory.initialize_selector(
-            self.config, seed_examples, dataset_loader.dat.keys().tolist()
+            self.config,
+            seed_examples,
+            dataset_loader.dat.keys().tolist(),
+            cache=self.cache is not None,
         )
 
         input_limit = min(len(dataset_loader.inputs), 100)
         for input_i in track(
             dataset_loader.inputs[:input_limit],
             description="Generating Prompts...",
             console=console,
@@ -360,15 +366,19 @@
         print_table(table, show_header=False, console=console, styles=COST_TABLE_STYLES)
 
         console.rule("Prompt Example")
         print(f"{prompt_list[0]}")
         console.rule()
 
     def handle_existing_task_run(
-        self, task_run: TaskRun, csv_file_name: str, gt_labels: List[str] = None
+        self,
+        task_run: TaskRun,
+        csv_file_name: str,
+        gt_labels: List[str] = None,
+        additional_metrics: List[BaseMetric] = [],
     ) -> TaskRun:
         """
         Allows for continuing an existing labeling task. The user will be asked whether they wish to continue from where the run previously left off, or restart from the beginning.
         Args:
             task_run: TaskRun to retry
             csv_file_name: path to the dataset we wish to label (only used if user chooses to restart the task)
             gt_labels: If ground truth labels are provided, performance metrics will be displayed, such as label accuracy
@@ -377,21 +387,24 @@
         db_result = AnnotationModel.get_annotations_by_task_run_id(
             self.db.session, task_run.id
         )
         llm_labels = [LLMAnnotation(**a.llm_annotation) for a in db_result]
         if gt_labels and len(llm_labels) > 0:
             pprint("Evaluating the existing task...")
             gt_labels = gt_labels[: len(llm_labels)]
-            eval_result = self.task.eval(llm_labels, gt_labels)
+            eval_result = self.task.eval(
+                llm_labels, gt_labels, additional_metrics=additional_metrics
+            )
             table = {}
             for m in eval_result:
-                if isinstance(m.value, list) and len(m.value) > 0:
-                    table[m.name] = m.value
+                if isinstance(m.value, list):
+                    continue
                 else:
-                    print(f"Metric: {m.name}: {m.value}")
+                    table[m.name] = m.value
+
             print_table(table, console=console, default_style=METRIC_TABLE_STYLE)
         pprint(f"{task_run.current_index} examples labeled so far.")
         if len(llm_labels) > 0:
             console.rule("Last Annotated Example")
             pprint("[bold blue]Prompt[/bold blue]: ", end="")
             print(llm_labels[-1].prompt)
             pprint("[bold blue]Annotation[/bold blue]: ", end="")
@@ -452,15 +465,15 @@
                 "The explanation column needs to be specified in the dataset config."
             )
 
         for seed_example in track(
             seed_examples, description="Generating explanations", console=console
         ):
             explanation_prompt = self.task.get_explanation_prompt(seed_example)
-            explanation, _ = self.llm.label([explanation_prompt])
+            explanation = self.llm.label([explanation_prompt])
             explanation = explanation.generations[0][0].text
             seed_example["explanation"] = str(explanation) if explanation else ""
 
         if out_file:
             df = pd.DataFrame.from_records(seed_examples)
             df.to_csv(out_file, index=False)
```

### Comparing `refuel-autolabel-0.0.8/src/autolabel/models/__init__.py` & `refuel-autolabel-0.0.9/src/autolabel/models/__init__.py`

 * *Files identical despite different names*

### Comparing `refuel-autolabel-0.0.8/src/autolabel/models/anthropic.py` & `refuel-autolabel-0.0.9/src/autolabel/models/anthropic.py`

 * *Files 14% similar despite different names*

```diff
@@ -2,14 +2,15 @@
 
 from anthropic import tokenizer
 from autolabel.configs import AutolabelConfig
 from autolabel.models import BaseModel
 from autolabel.cache import BaseCache
 from langchain.chat_models import ChatAnthropic
 from langchain.schema import LLMResult, HumanMessage
+from autolabel.schema import RefuelLLMResult
 
 
 class AnthropicLLM(BaseModel):
     DEFAULT_MODEL = "claude-instant-v1"
     DEFAULT_PARAMS = {
         "max_tokens_to_sample": 1000,
         "temperature": 0.0,
@@ -33,20 +34,22 @@
         self.model_name = config.model_name() or self.DEFAULT_MODEL
         # populate model params
         model_params = config.model_params()
         self.model_params = {**self.DEFAULT_PARAMS, **model_params}
         # initialize LLM
         self.llm = ChatAnthropic(model=self.model_name, **self.model_params)
 
-    def _label(self, prompts: List[str]) -> LLMResult:
+    def _label(self, prompts: List[str]) -> RefuelLLMResult:
         prompts = [[HumanMessage(content=prompt)] for prompt in prompts]
         try:
-            return self.llm.generate(prompts)
+            result = self.llm.generate(prompts)
+            return RefuelLLMResult(
+                generations=result.generations, errors=[None] * len(result.generations)
+            )
         except Exception as e:
-            print(f"Error generating from LLM: {e}, retrying each prompt individually")
             return self._label_individually(prompts)
 
     def get_cost(self, prompt: str, label: Optional[str] = "") -> float:
         num_prompt_toks = tokenizer.count_tokens(prompt)
         if label:
             num_label_toks = tokenizer.count_tokens(label)
         else:
```

### Comparing `refuel-autolabel-0.0.8/src/autolabel/models/base.py` & `refuel-autolabel-0.0.9/src/autolabel/models/base.py`

 * *Files 16% similar despite different names*

```diff
@@ -2,82 +2,91 @@
 
 from abc import ABC, abstractmethod
 from typing import List, Optional, Dict, Tuple
 
 from langchain.schema import LLMResult, Generation
 
 from autolabel.configs import AutolabelConfig
-from autolabel.schema import CacheEntry
+from autolabel.schema import CacheEntry, LabelingError, RefuelLLMResult, ErrorType
 from autolabel.cache import BaseCache
 
 
 class BaseModel(ABC):
     def __init__(self, config: AutolabelConfig, cache: BaseCache) -> None:
         self.config = config
         self.cache = cache
         self.model_params = config.model_params()
         # Specific classes that implement this interface should run initialization steps here
         # E.g. initializing the LLM model with required parameters from ModelConfig
 
-    def label(self, prompts: List[str]) -> Tuple[LLMResult, float]:
+    def label(self, prompts: List[str]) -> RefuelLLMResult:
         """Label a list of prompts."""
         existing_prompts = {}
         missing_prompt_idxs = list(range(len(prompts)))
         missing_prompts = prompts
-        llm_output = {}
-        cost = 0.0
+        costs = []
+        errors = [None for i in range(len(prompts))]
         if self.cache:
             (
                 existing_prompts,
                 missing_prompt_idxs,
                 missing_prompts,
             ) = self.get_cached_prompts(prompts)
 
         # label missing prompts
         if len(missing_prompts) > 0:
             new_results = self._label(missing_prompts)
             for ind, prompt in enumerate(missing_prompts):
-                cost += self.get_cost(
-                    prompt, label=new_results.generations[ind][0].text
+                costs.append(
+                    self.get_cost(prompt, label=new_results.generations[ind][0].text)
                 )
 
             # Set the existing prompts to the new results
-            for i, result in zip(missing_prompt_idxs, new_results.generations):
+            for i, result, error in zip(
+                missing_prompt_idxs, new_results.generations, new_results.errors
+            ):
                 existing_prompts[i] = result
+                errors[i] = error
 
             if self.cache:
                 self.update_cache(missing_prompt_idxs, new_results, prompts)
 
-            llm_output = new_results.llm_output
-
         generations = [existing_prompts[i] for i in range(len(prompts))]
-        return LLMResult(generations=generations, llm_output=llm_output), cost
+        return RefuelLLMResult(generations=generations, costs=costs, errors=errors)
 
-    def _label_individually(self, prompts: List[str]) -> LLMResult:
+    def _label_individually(self, prompts: List[str]) -> RefuelLLMResult:
         """Label each prompt individually. Should be used only after trying as a batch first.
 
         Args:
             prompts (List[str]): List of prompts to label
 
         Returns:
             LLMResult: LLMResult object with generations
+            List[LabelingError]: List of errors encountered while labeling
         """
         generations = []
+        errors = []
         for prompt in prompts:
             try:
                 response = self.llm.generate([prompt])
                 generations.append(response.generations[0])
+                errors.append(None)
             except Exception as e:
-                print(f"Error generating from LLM: {e}, returning empty generation")
+                print(f"Error generating from LLM: {e}")
                 generations.append([Generation(text="")])
+                errors.append(
+                    LabelingError(
+                        error_type=ErrorType.LLM_PROVIDER_ERROR, error_message=str(e)
+                    )
+                )
 
-        return LLMResult(generations=generations)
+        return RefuelLLMResult(generations=generations, errors=errors)
 
     @abstractmethod
-    def _label(self, prompts: List[str]) -> LLMResult:
+    def _label(self, prompts: List[str]) -> RefuelLLMResult:
         # TODO: change return type to do parsing in the Model class
         pass
 
     @abstractmethod
     def get_cost(self, prompt: str, label: Optional[str] = "") -> float:
         pass
 
@@ -109,18 +118,19 @@
 
     def update_cache(self, missing_prompt_idxs, new_results, prompts):
         """Update the cache with new results."""
         model_params_string = str(
             sorted([(k, v) for k, v in self.model_params.items()])
         )
 
-        for i, result in zip(missing_prompt_idxs, new_results.generations):
-            # If the result is empty, don't cache it
-            # This result was likely produced due to an error
-            if result[0].text == "":
+        for i, result, error in zip(
+            missing_prompt_idxs, new_results.generations, new_results.errors
+        ):
+            # If there was an error, don't cache the result
+            if error is not None:
                 continue
 
             cache_entry = CacheEntry(
                 prompt=prompts[i],
                 model_name=self.model_name,
                 model_params=model_params_string,
                 generations=result,
```

### Comparing `refuel-autolabel-0.0.8/src/autolabel/models/cohere.py` & `refuel-autolabel-0.0.9/src/autolabel/models/cohere.py`

 * *Files 6% similar despite different names*

```diff
@@ -6,14 +6,15 @@
 from langchain.llms import Cohere
 from langchain.schema import LLMResult
 from langchain import PromptTemplate, LLMChain
 
 from autolabel.models import BaseModel
 from autolabel.configs import AutolabelConfig
 from autolabel.cache import BaseCache
+from autolabel.schema import RefuelLLMResult
 
 
 class CohereLLM(BaseModel):
     # Default parameters for OpenAILLM
     DEFAULT_MODEL = "command"
     DEFAULT_MODEL_PARAMS = {
         "max_tokens": 512,
@@ -33,19 +34,21 @@
         self.model_params = {
             **self.DEFAULT_MODEL_PARAMS,
             **model_params,
         }
         self.llm = Cohere(model=self.model_name, **self.model_params)
         self.co = cohere.Client(api_key=os.environ["COHERE_API_KEY"])
 
-    def _label(self, prompts: List[str]) -> LLMResult:
+    def _label(self, prompts: List[str]) -> RefuelLLMResult:
         try:
-            return self.llm.generate(prompts)
+            result = self.llm.generate(prompts)
+            return RefuelLLMResult(
+                generations=result.generations, errors=[None] * len(result.generations)
+            )
         except Exception as e:
-            print(f"Error generating from LLM: {e}, retrying each prompt individually")
             return self._label_individually(prompts)
 
     def get_cost(self, prompt: str, label: Optional[str] = "") -> float:
         num_prompt_toks = len(self.co.tokenize(prompt).tokens)
         if label:
             num_label_toks = len(self.co.tokenize(label).tokens)
         else:
```

### Comparing `refuel-autolabel-0.0.8/src/autolabel/models/openai.py` & `refuel-autolabel-0.0.9/src/autolabel/models/openai.py`

 * *Files 4% similar despite different names*

```diff
@@ -6,14 +6,15 @@
 from langchain.llms import OpenAI
 from langchain.schema import LLMResult, HumanMessage
 import tiktoken
 
 from autolabel.models import BaseModel
 from autolabel.configs import AutolabelConfig
 from autolabel.cache import BaseCache
+from autolabel.schema import RefuelLLMResult
 
 import os
 
 logger = logging.getLogger(__name__)
 
 
 class OpenAILLM(BaseModel):
@@ -133,24 +134,26 @@
                 tokens = encoding.encode(label)
                 for token in tokens:
                     logit_bias[token] = 100
                 max_tokens = max(max_tokens, len(tokens))
 
         return {"logit_bias": logit_bias, "max_tokens": max_tokens}
 
-    def _label(self, prompts: List[str]) -> LLMResult:
+    def _label(self, prompts: List[str]) -> RefuelLLMResult:
         if self._engine == "chat":
             # Need to convert list[prompts] -> list[messages]
             # Currently the entire prompt is stuck into the "human message"
             # We might consider breaking this up into human vs system message in future
             prompts = [[HumanMessage(content=prompt)] for prompt in prompts]
         try:
-            return self.llm.generate(prompts)
+            result = self.llm.generate(prompts)
+            return RefuelLLMResult(
+                generations=result.generations, errors=[None] * len(result.generations)
+            )
         except Exception as e:
-            print(f"Error generating from LLM: {e}, retrying each prompt individually")
             return self._label_individually(prompts)
 
     def get_cost(self, prompt: str, label: Optional[str] = "") -> float:
         encoding = tiktoken.encoding_for_model(self.model_name)
         num_prompt_toks = len(encoding.encode(prompt))
         if label:
             num_label_toks = len(encoding.encode(label))
```

### Comparing `refuel-autolabel-0.0.8/src/autolabel/models/palm.py` & `refuel-autolabel-0.0.9/src/autolabel/models/palm.py`

 * *Files 18% similar despite different names*

```diff
@@ -5,14 +5,15 @@
 from langchain.chat_models import ChatVertexAI
 from langchain.llms import VertexAI
 from langchain.schema import LLMResult, HumanMessage, Generation
 
 from autolabel.models import BaseModel
 from autolabel.configs import AutolabelConfig
 from autolabel.cache import BaseCache
+from autolabel.schema import RefuelLLMResult
 
 from tenacity import (
     before_sleep_log,
     retry,
     stop_after_attempt,
     wait_exponential,
 )
@@ -21,15 +22,16 @@
 
 
 class PaLMLLM(BaseModel):
     SEP_REPLACEMENT_TOKEN = "@@"
     CHAT_ENGINE_MODELS = ["chat-bison@001"]
 
     DEFAULT_MODEL = "text-bison@001"
-    DEFAULT_PARAMS = {"temperature": 0}
+    # Reference: https://developers.generativeai.google/guide/concepts#model_parameters for "A token is approximately 4 characters"
+    DEFAULT_PARAMS = {"temperature": 0, "max_output_tokens": 1000}
 
     # Reference: https://cloud.google.com/vertex-ai/pricing
     COST_PER_CHARACTER = {
         "text-bison@001": 0.001 / 1000,
         "chat-bison@001": 0.0005 / 1000,
         "textembedding-gecko@001": 0.0001 / 1000,
     }
@@ -86,15 +88,15 @@
                 generations.append(response.generations[0])
             except Exception as e:
                 print(f"Error generating from LLM: {e}, returning empty generation")
                 generations.append([Generation(text="")])
 
         return LLMResult(generations=generations)
 
-    def _label(self, prompts: List[str]) -> LLMResult:
+    def _label(self, prompts: List[str]) -> RefuelLLMResult:
         for prompt in prompts:
             if self.SEP_REPLACEMENT_TOKEN in prompt:
                 logger.warning(
                     f"""Current prompt contains {self.SEP_REPLACEMENT_TOKEN} 
                                 which is currently used as a separator token by refuel
                                 llm. It is highly recommended to avoid having any
                                 occurences of this substring in the prompt.
@@ -112,20 +114,23 @@
         try:
             result = self._label_with_retry(prompts)
             for generations in result.generations:
                 for generation in generations:
                     generation.text = generation.text.replace(
                         self.SEP_REPLACEMENT_TOKEN, "\n"
                     )
-            return result
+            return RefuelLLMResult(
+                generations=result.generations, errors=[None] * len(result.generations)
+            )
         except Exception as e:
-            print(f"Error generating from LLM: {e}, retrying each prompt individually")
             self._label_individually(prompts)
 
     def get_cost(self, prompt: str, label: Optional[str] = "") -> float:
         if self.model_name is None:
             return 0.0
         cost_per_char = self.COST_PER_CHARACTER.get(self.model_name, 0.0)
-        return cost_per_char * len(prompt)
+        return cost_per_char * len(prompt) + cost_per_char * (
+            len(label) if label else 4 * self.model_params["max_output_tokens"]
+        )
 
     def returns_token_probs(self) -> bool:
         return False
```

### Comparing `refuel-autolabel-0.0.8/src/autolabel/models/refuel.py` & `refuel-autolabel-0.0.9/src/autolabel/models/refuel.py`

 * *Files 6% similar despite different names*

```diff
@@ -5,14 +5,15 @@
 import logging
 from typing import List, Optional
 
 
 from autolabel.models import BaseModel
 from autolabel.configs import AutolabelConfig
 from autolabel.cache import BaseCache
+from autolabel.schema import LabelingError, ErrorType, RefuelLLMResult
 
 
 from tenacity import (
     before_sleep_log,
     retry,
     stop_after_attempt,
     wait_exponential,
@@ -61,16 +62,17 @@
         }
         headers = {"refuel_api_key": self.REFUEL_API_KEY}
         response = requests.post(self.BASE_API, json=payload, headers=headers)
         # raise Exception if status != 200
         response.raise_for_status()
         return response
 
-    def _label(self, prompts: List[str]) -> LLMResult:
+    def _label(self, prompts: List[str]) -> RefuelLLMResult:
         generations = []
+        errors = []
         for prompt in prompts:
             try:
                 if self.SEP_REPLACEMENT_TOKEN in prompt:
                     logger.warning(
                         f"""Current prompt contains {self.SEP_REPLACEMENT_TOKEN} 
                             which is currently used as a separator token by refuel
                             llm. It is highly recommended to avoid having any
@@ -79,20 +81,24 @@
                     )
                 separated_prompt = prompt.replace("\n", self.SEP_REPLACEMENT_TOKEN)
                 response = self._label_with_retry(separated_prompt)
                 response = json.loads(response.json()["body"]).replace(
                     self.SEP_REPLACEMENT_TOKEN, "\n"
                 )
                 generations.append([Generation(text=response)])
+                errors.append(None)
             except Exception as e:
                 # This signifies an error in generating the response using RefuelLLm
                 logger.error(
                     f"Unable to generate prediction: {e}",
                 )
                 generations.append([Generation(text="")])
-        return LLMResult(generations=generations)
+                errors.append(
+                    LabelingError(error_type=ErrorType.LLM_PROVIDER_ERROR, error=e)
+                )
+        return RefuelLLMResult(generations=generations, errors=errors)
 
     def get_cost(self, prompt: str, label: Optional[str] = "") -> float:
         return 0
 
     def returns_token_probs(self) -> bool:
         return False
```

### Comparing `refuel-autolabel-0.0.8/src/autolabel/schema.py` & `refuel-autolabel-0.0.9/src/autolabel/schema.py`

 * *Files 18% similar despite different names*

```diff
@@ -41,48 +41,74 @@
     LABEL_DIVERSITY_SIMILARITY = "label_diversity_similarity"
 
 
 class TaskStatus(str, Enum):
     ACTIVE = "active"
 
 
-class Metric(str, Enum):
+class MetricType(str, Enum):
     """Enum of supported performance metrics. Some metrics are always available (task agnostic), while others are only supported by certain types of tasks"""
 
     # Task agnostic
     SUPPORT = "support"
     COMPLETION_RATE = "completion_rate"
     # Classification metrics
     ACCURACY = "accuracy"
     CONFUSION_MATRIX = "confusion_matrix"
     LABEL_DISTRIBUTION = "label_distribution"
     F1 = "f1"
+    F1_MICRO = "f1_micro"
+    F1_MACRO = "f1_macro"
+    F1_WEIGHTED = "f1_weighted"
+    TEXT_PARTIAL_MATCH = "text_partial_match"
     # Confidence metrics
     AUROC = "auroc"
     THRESHOLD = "threshold"
 
 
+class F1Type(str, Enum):
+    MULTI_LABEL = "multi_label"
+    TEXT = "text"
+
+
 class MetricResult(BaseModel):
     """Contains performance metrics gathered from autolabeler runs"""
 
-    metric_type: Metric
     name: str
     value: Any
 
 
+class ErrorType(str, Enum):
+    """Enum of supported error types"""
+
+    LLM_PROVIDER_ERROR = "llm_provider_error"
+    PARSING_ERROR = "parsing_error"
+    OUTPUT_GUIDELINES_NOT_FOLLOWED_ERROR = "output_guidelines_not_followed_error"
+    EMPTY_RESPONSE_ERROR = "empty_response_error"
+
+
+class LabelingError(BaseModel):
+    """Contains information about an error that occurred during the labeling process"""
+
+    error_type: ErrorType
+    error_message: str
+
+
 class LLMAnnotation(BaseModel):
     """Contains label information of a given data point, including the generated label, the prompt given to the LLM, and the LLMs response. Optionally includes a confidence_score if supported by the model"""
 
     successfully_labeled: bool
     label: Any
     curr_sample: Optional[str] = ""
     confidence_score: Optional[float] = None
     generation_info: Optional[Dict[str, Any]] = None
     raw_response: Optional[str] = ""
+    explanation: Optional[str] = ""
     prompt: Optional[str] = ""
+    error: Optional[LabelingError] = None
 
 
 class Dataset(BaseModel):
     """Contains Dataset parameters, including input file path, indexes for state management (e.g. job batching and retries), and a unique ID"""
 
     id: str
     input_file: str
@@ -165,7 +191,20 @@
     model_name: str
     prompt: str
     model_params: str
     generations: Optional[List[Generation]] = None
 
     class Config:
         orm_mode = True
+
+
+class RefuelLLMResult(BaseModel):
+    """List of generated outputs. This is a List[List[]] because
+    each input could have multiple candidate generations."""
+
+    generations: List[List[Generation]]
+
+    """Errors encountered while running the labeling job"""
+    errors: List[Optional[LabelingError]]
+
+    """Costs incurred during the labeling job"""
+    costs: Optional[List[float]] = []
```

### Comparing `refuel-autolabel-0.0.8/src/autolabel/tasks/__init__.py` & `refuel-autolabel-0.0.9/src/autolabel/tasks/__init__.py`

 * *Files identical despite different names*

### Comparing `refuel-autolabel-0.0.8/src/autolabel/tasks/base.py` & `refuel-autolabel-0.0.9/src/autolabel/tasks/base.py`

 * *Files 17% similar despite different names*

```diff
@@ -4,15 +4,22 @@
 from typing import Dict, List
 import logging
 import json
 
 from langchain.prompts.prompt import PromptTemplate
 from langchain.schema import Generation
 from autolabel.configs import AutolabelConfig
-from autolabel.schema import LLMAnnotation, MetricResult, FewShotAlgorithm, TaskType
+from autolabel.schema import (
+    LLMAnnotation,
+    MetricResult,
+    FewShotAlgorithm,
+    TaskType,
+    LabelingError,
+    ErrorType,
+)
 from autolabel.utils import get_format_variables, extract_valid_json_substring
 
 logger = logging.getLogger(__name__)
 
 
 class BaseTask(ABC):
     ZERO_SHOT_TEMPLATE = "{task_guidelines}\n\n{output_guidelines}\n\nNow I want you to label the following example:\n{current_example}"
@@ -63,47 +70,63 @@
         )
 
     def parse_llm_response(
         self, response: Generation, curr_sample: Dict, prompt: str
     ) -> LLMAnnotation:
         # The last line of the response is the label
         # This is done to handle the case where the model generates an explanation before generating the label
+        error = None
         if self.config.chain_of_thought():
             try:
+                explanation = response.text.strip().split("\n")[0].strip()
                 completion_text = extract_valid_json_substring(
                     response.text.strip().split("\n")[-1].strip()
                 )
                 completion_text = json.loads(completion_text)["label"]
             except:
                 completion_text = None
         else:
             completion_text = response.text.strip().split("\n")[-1].strip()
         if len(response.text.strip()) == 0:
             successfully_labeled = False
             llm_label = self.NULL_LABEL_TOKEN
-            logger.warning(f"LLM response is empty")
+            logger.warning("LLM response is empty")
+            error = LabelingError(
+                error_type=ErrorType.EMPTY_RESPONSE_ERROR,
+                error_message="Empty response from LLM",
+            )
         elif not completion_text:
             successfully_labeled = False
             llm_label = self.NULL_LABEL_TOKEN
-            logger.error(f"Error parsing LLM response: {response.text}")
+            logger.warning(f"Error parsing LLM response: {response.text}")
+            error = LabelingError(
+                error_type=ErrorType.PARSING_ERROR,
+                error_message=f"Error parsing LLM response: {response.text}",
+            )
         else:
             llm_label = completion_text.strip()
             if self.config.task_type() in [
                 TaskType.CLASSIFICATION,
                 TaskType.ENTITY_MATCHING,
             ]:
                 if llm_label in self.config.labels_list():
                     successfully_labeled = True
                 else:
                     logger.warning(f"LLM response is not in the labels list")
                     successfully_labeled = False
+                    error = LabelingError(
+                        error_type=ErrorType.OUTPUT_GUIDELINES_NOT_FOLLOWED_ERROR,
+                        error_message=f"LLM response is not in the labels list: {llm_label}",
+                    )
             else:
                 successfully_labeled = True
 
         return LLMAnnotation(
             successfully_labeled=successfully_labeled,
             label=llm_label,
             generation_info=response.generation_info,
             raw_response=response.text,
             prompt=prompt,
             curr_sample=json.dumps(curr_sample),
+            explanation=explanation if self.config.chain_of_thought() else "",
+            error=error,
         )
```

### Comparing `refuel-autolabel-0.0.8/src/autolabel/tasks/named_entity_recognition.py` & `refuel-autolabel-0.0.9/src/autolabel/tasks/named_entity_recognition.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,19 +1,26 @@
 import json
 import re
 from collections import defaultdict
 from typing import Dict, List, Tuple
 from copy import deepcopy
 
 from langchain.schema import Generation
+from sklearn.metrics import roc_auc_score
 import logging
 from nervaluate import Evaluator
 from autolabel.confidence import ConfidenceCalculator
 from autolabel.configs import AutolabelConfig
-from autolabel.schema import LLMAnnotation, Metric, MetricResult
+from autolabel.schema import (
+    LLMAnnotation,
+    MetricType,
+    MetricResult,
+    LabelingError,
+    ErrorType,
+)
 from autolabel.tasks import BaseTask
 
 logger = logging.getLogger(__name__)
 
 
 class NamedEntityRecognitionTask(BaseTask):
     DEFAULT_OUTPUT_GUIDELINES = "You will return the answer in CSV format, with two columns seperated by the % character. First column is the extracted entity and second column is the category. Rows in the CSV are separated by new line character."
@@ -131,34 +138,37 @@
         return processed_output
 
     def parse_llm_response(
         self, response: Generation, curr_sample: Dict, prompt: str
     ) -> LLMAnnotation:
         output = {}
         successfully_labeled = False
+        error = None
         text_column = self.config.text_column()
         input_str = curr_sample[text_column]
         try:
             completion_text = response.text
             output = self._llm_to_json_format(completion_text.strip())
             llm_label = self.add_text_spans(output, input_str)
         except Exception as e:
             logger.error(f"Error parsing LLM response: {response.text}, Error: {e}")
             llm_label = self.NULL_LABEL
+            error = LabelingError(error_type=ErrorType.PARSING_ERROR, error_msg=str(e))
 
         successfully_labeled = False if llm_label == self.NULL_LABEL else True
 
         # TODO: parse generation info correctly to fetch & transform logprobs -> score
         return LLMAnnotation(
             curr_sample=input_str,
             successfully_labeled=successfully_labeled,
             label=llm_label,
             generation_info=response.generation_info,
             raw_response=response.text,
             prompt=prompt,
+            error=error,
         )
 
     def auroc_score_labels(
         self, gt_labels, llm_labels_with_conf
     ) -> Tuple[List[int], List[float]]:
         labels = []
         confidences = []
@@ -213,42 +223,45 @@
             answered_gt_labels, answered_llm_preds, tags=entity_types_set
         )
 
         results, _ = evaluator.evaluate()
         # f1 score
         eval_metrics.append(
             MetricResult(
-                metric_type=Metric.F1,
-                name=f"f1",
+                name=MetricType.F1,
                 value=results["exact"]["f1"],
             )
         )
 
         # accuracy
         accuracy = (
             results.get("strict").get("correct")
             / (results.get("strict").get("possible"))
             if results.get("strict").get("possible") > 0
             else 0.0
         )
         eval_metrics.append(
             MetricResult(
-                metric_type=Metric.ACCURACY,
-                name=f"accuracy",
+                name=MetricType.ACCURACY,
                 value=accuracy,
             )
         )
 
-        eval_metrics.append(
-            MetricResult(
-                metric_type=Metric.SUPPORT,
-                name=f"support",
-                value=len(answered_gt_labels),
+        if self.config.confidence():
+            match, confidences = self.auroc_score_labels(
+                answered_gt_labels, answered_llm_preds
             )
-        )
+            auroc = roc_auc_score(match, confidences)
+            eval_metrics.append(
+                MetricResult(
+                    name=MetricType.AUROC,
+                    value=auroc,
+                )
+            )
+
         return eval_metrics
 
     def eval(
         self, llm_labels: List[LLMAnnotation], gt_labels: List[str]
     ) -> List[MetricResult]:
         """Evaluate the LLM generated labels by comparing them against ground truth
 
@@ -263,80 +276,50 @@
         gt_labels = [
             self.add_text_spans(
                 json.loads(gt_labels[index]), llm_labels[index].curr_sample
             )
             for index in range(len(gt_labels))
         ]
 
-        eval_metrics_map = {
-            Metric.F1: [],
-            Metric.SUPPORT: [],
-            Metric.ACCURACY: [],
-            Metric.COMPLETION_RATE: [],
-        }
-        eval_metrics = []
-        thresholds = []
-
-        if self.config.confidence():
-            eval_metrics_map[Metric.THRESHOLD] = []
-            all_gt_labels, all_llm_preds = self.get_labels_predictions_with_threshold(
-                gt_labels, llm_labels, float("-inf")
-            )
-            labels, confidences = self.auroc_score_labels(all_gt_labels, all_llm_preds)
-            value, meaningful_thresholds = ConfidenceCalculator.compute_auroc(
-                labels, confidences
-            )
-            thresholds.extend(meaningful_thresholds)
-            eval_metrics.append(
-                MetricResult(
-                    metric_type=Metric.AUROC,
-                    name="auroc",
-                    value=value,
-                )
-            )
-        else:
-            thresholds.append(float("-inf"))
+        (
+            curr_gt_labels,
+            curr_llm_labels,
+        ) = self.get_labels_predictions_with_threshold(
+            gt_labels, llm_labels, float("-inf")
+        )
 
-        for index, threshold in enumerate(thresholds):
-            (
-                curr_gt_labels,
-                curr_llm_labels,
-            ) = self.get_labels_predictions_with_threshold(
-                gt_labels, llm_labels, threshold
+        entity_types_set = list(
+            set(
+                [
+                    gt_entity.get("label")
+                    for gt_label in curr_gt_labels
+                    for gt_entity in gt_label
+                ]
             )
+        )
 
-            entity_types_set = list(
-                set(
-                    [
-                        gt_entity.get("label")
-                        for gt_label in curr_gt_labels
-                        for gt_entity in gt_label
-                    ]
-                )
-            )
+        eval_metrics = []
 
-            curr_threshold_metrics = self.run_metrics(
-                curr_gt_labels,
-                curr_llm_labels,
-                entity_types_set,
+        eval_metrics.append(
+            MetricResult(
+                name=MetricType.SUPPORT,
+                value=len(gt_labels),
             )
+        )
 
-            for metric in curr_threshold_metrics:
-                eval_metrics_map[metric.metric_type].append(metric.value)
-
-            eval_metrics_map[Metric.COMPLETION_RATE].append(
-                len(curr_llm_labels) / float(len(gt_labels))
+        eval_metrics.append(
+            MetricResult(
+                name=MetricType.COMPLETION_RATE,
+                value=len(curr_llm_labels) / float(len(gt_labels))
+                if len(gt_labels) > 0
+                else 0.0,
             )
+        )
 
-            if self.config.confidence():
-                eval_metrics_map[Metric.THRESHOLD].append(threshold)
-        eval_metrics.extend(
-            [
-                MetricResult(
-                    metric_type=i,
-                    name=i.value,
-                    value=eval_metrics_map[i],
-                )
-                for i in eval_metrics_map.keys()
-            ]
+        curr_threshold_metrics = self.run_metrics(
+            curr_gt_labels,
+            curr_llm_labels,
+            entity_types_set,
         )
+
+        eval_metrics.extend(curr_threshold_metrics)
         return eval_metrics
```

### Comparing `refuel-autolabel-0.0.8/src/autolabel/utils.py` & `refuel-autolabel-0.0.9/src/autolabel/utils.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,12 +1,14 @@
 import hashlib
 import os
 import json
 import logging
 from string import Formatter
+import re
+import string
 from typing import Any, Dict, Iterable, List, Optional, Sequence, Union
 import shutil
 
 import regex
 import wget
 from rich.console import Console, Group
 from rich.live import Live
@@ -30,14 +32,15 @@
     "ledgar",
     "walmart_amazon",
     "company",
     "squad_v2",
     "sciq",
     "conll2003",
     "movie_reviews",
+    "twitter_emotion_detection",
 ]
 
 NO_SEED_DATASET = [
     "movie_reviews",
 ]
 
 DATASET_URL = "https://autolabel-benchmarking.s3.us-west-2.amazonaws.com/{dataset}/{partition}.csv"
@@ -289,7 +292,27 @@
     test_url = DATASET_URL.format(dataset=dataset_name, partition="test")
     try:
         if dataset_name not in NO_SEED_DATASET:
             download(seed_url)
         download(test_url)
     except Exception as e:
         logger.error(f"Error downloading dataset: {e}")
+
+
+def normalize_text(s: str) -> str:
+    """Removing articles and punctuation, and standardizing whitespace are all typical text processing steps."""
+
+    def remove_articles(text):
+        regex = re.compile(r"\b(a|an|the)\b", re.UNICODE)
+        return re.sub(regex, " ", text)
+
+    def white_space_fix(text):
+        return " ".join(text.split())
+
+    def remove_punc(text):
+        exclude = set(string.punctuation)
+        return "".join(ch for ch in text if ch not in exclude)
+
+    def lower(text):
+        return text.lower()
+
+    return white_space_fix(remove_articles(remove_punc(lower(s))))
```

### Comparing `refuel-autolabel-0.0.8/src/refuel_autolabel.egg-info/PKG-INFO` & `refuel-autolabel-0.0.9/src/refuel_autolabel.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: refuel-autolabel
-Version: 0.0.8
+Version: 0.0.9
 Summary: Label, clean and enrich text datasets with LLMs
 Author-email: "Refuel.ai" <support@refuel.ai>
 License: MIT License
         
         Copyright (c) 2023 refuel-ai
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: refuel-autolabel Version: 0.0.8 Summary: Label,
+Metadata-Version: 2.1 Name: refuel-autolabel Version: 0.0.9 Summary: Label,
 clean and enrich text datasets with LLMs Author-email: "Refuel.ai"
 refuel.ai> License: MIT License Copyright (c) 2023 refuel-ai Permission is
 hereby granted, free of charge, to any person obtaining a copy of this software
 and associated documentation files (the "Software"), to deal in the Software
 without restriction, including without limitation the rights to use, copy,
 modify, merge, publish, distribute, sublicense, and/or sell copies of the
 Software, and to permit persons to whom the Software is furnished to do so,
```

### Comparing `refuel-autolabel-0.0.8/src/refuel_autolabel.egg-info/SOURCES.txt` & `refuel-autolabel-0.0.9/src/refuel_autolabel.egg-info/SOURCES.txt`

 * *Files 4% similar despite different names*

```diff
@@ -26,14 +26,21 @@
 src/autolabel/database/__init__.py
 src/autolabel/database/engine.py
 src/autolabel/database/state_manager.py
 src/autolabel/few_shot/__init__.py
 src/autolabel/few_shot/fixed_example_selector.py
 src/autolabel/few_shot/label_diversity_example_selector.py
 src/autolabel/few_shot/vector_store.py
+src/autolabel/metrics/__init__.py
+src/autolabel/metrics/accuracy.py
+src/autolabel/metrics/auroc.py
+src/autolabel/metrics/base.py
+src/autolabel/metrics/completion_rate.py
+src/autolabel/metrics/f1.py
+src/autolabel/metrics/support.py
 src/autolabel/models/__init__.py
 src/autolabel/models/anthropic.py
 src/autolabel/models/base.py
 src/autolabel/models/cohere.py
 src/autolabel/models/hf_pipeline.py
 src/autolabel/models/openai.py
 src/autolabel/models/palm.py
```

### Comparing `refuel-autolabel-0.0.8/src/refuel_autolabel.egg-info/requires.txt` & `refuel-autolabel-0.0.9/src/refuel_autolabel.egg-info/requires.txt`

 * *Files identical despite different names*

