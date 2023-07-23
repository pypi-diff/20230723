# Comparing `tmp/hyfi-1.8.1.tar.gz` & `tmp/hyfi-1.8.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "hyfi-1.8.1.tar", max compression
+gzip compressed data, was "hyfi-1.8.2.tar", max compression
```

## Comparing `hyfi-1.8.1.tar` & `hyfi-1.8.2.tar`

### file list

```diff
@@ -1,109 +1,109 @@
--rw-r--r--   0        0        0     1071 2023-07-22 21:49:14.254739 hyfi-1.8.1/LICENSE
--rw-r--r--   0        0        0     1881 2023-07-22 21:49:14.254739 hyfi-1.8.1/README.md
--rw-r--r--   0        0        0     4853 2023-07-22 21:49:45.371364 hyfi-1.8.1/pyproject.toml
--rw-r--r--   0        0        0     4168 2023-07-22 21:49:14.258739 hyfi-1.8.1/src/hyfi/__cli__.py
--rw-r--r--   0        0        0     3586 2023-07-22 21:49:14.258739 hyfi-1.8.1/src/hyfi/__click__.py
--rw-r--r--   0        0        0     1183 2023-07-22 21:49:14.258739 hyfi-1.8.1/src/hyfi/__init__.py
--rw-r--r--   0        0        0       22 2023-07-22 21:49:45.271363 hyfi-1.8.1/src/hyfi/_version.py
--rw-r--r--   0        0        0     1497 2023-07-22 21:49:14.258739 hyfi-1.8.1/src/hyfi/about/__init__.py
--rw-r--r--   0        0        0     7292 2023-07-22 21:49:14.258739 hyfi-1.8.1/src/hyfi/batch/__init__.py
--rw-r--r--   0        0        0     1206 2023-07-22 21:49:14.258739 hyfi-1.8.1/src/hyfi/cached_path/__init__.py
--rw-r--r--   0        0        0    14373 2023-07-22 21:49:14.258739 hyfi-1.8.1/src/hyfi/cached_path/_cached_path.py
--rw-r--r--   0        0        0     1619 2023-07-22 21:49:14.258739 hyfi-1.8.1/src/hyfi/cached_path/cache_file.py
--rw-r--r--   0        0        0     1100 2023-07-22 21:49:14.258739 hyfi-1.8.1/src/hyfi/cached_path/common.py
--rw-r--r--   0        0        0     1921 2023-07-22 21:49:14.258739 hyfi-1.8.1/src/hyfi/cached_path/file_lock.py
--rw-r--r--   0        0        0     3441 2023-07-22 21:49:14.258739 hyfi-1.8.1/src/hyfi/cached_path/meta.py
--rw-r--r--   0        0        0     3247 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/cached_path/progress.py
--rw-r--r--   0        0        0     1437 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/cached_path/schemes/__init__.py
--rw-r--r--   0        0        0     1815 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/cached_path/schemes/beaker.py
--rw-r--r--   0        0        0     2862 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/cached_path/schemes/hf.py
--rw-r--r--   0        0        0     2942 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/cached_path/schemes/http.py
--rw-r--r--   0        0        0     3645 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/cached_path/schemes/scheme_client.py
--rw-r--r--   0        0        0     1222 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/cached_path/testing.py
--rw-r--r--   0        0        0     4799 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/cached_path/util.py
--rw-r--r--   0        0        0      464 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/cached_path/version.py
--rw-r--r--   0        0        0    24360 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/composer/__init__.py
--rw-r--r--   0        0        0     7328 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/composer/base.py
--rw-r--r--   0        0        0     1933 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/composer/pydantic.py
--rw-r--r--   0        0        0        0 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/__init__.py
--rw-r--r--   0        0        0      193 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/about/__init__.yaml
--rw-r--r--   0        0        0      588 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/batch/__init__.yaml
--rw-r--r--   0        0        0       44 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/cmd/__init__.yaml
--rw-r--r--   0        0        0       60 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/cmd/about.yaml
--rw-r--r--   0        0        0      160 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/cmd/copy_conf.yaml
--rw-r--r--   0        0        0       83 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/cmd/run_task.yaml
--rw-r--r--   0        0        0       91 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/cmd/run_workflow.yaml
--rw-r--r--   0        0        0      209 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/config.yaml
--rw-r--r--   0        0        0      662 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/copier/__init__.yaml
--rw-r--r--   0        0        0      709 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/dotenv/__init__.yaml
--rw-r--r--   0        0        0     1053 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/hydra/help/help.yaml
--rw-r--r--   0        0        0      264 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/hydra/job_logging/custom.yaml
--rw-r--r--   0        0        0      132 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/joblib/__init__.yaml
--rw-r--r--   0        0        0      198 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/mode/__debug__.yaml
--rw-r--r--   0        0        0      955 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/mode/__init__.yaml
--rw-r--r--   0        0        0       61 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/module/__init__.yaml
--rw-r--r--   0        0        0       72 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/path/__batch__.yaml
--rw-r--r--   0        0        0      876 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/path/__init__.yaml
--rw-r--r--   0        0        0       91 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/path/__task__.yaml
--rw-r--r--   0        0        0      286 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/path/dirnames/__init__.yaml
--rw-r--r--   0        0        0       76 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/pipe/__dataframe__.yaml
--rw-r--r--   0        0        0       77 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/pipe/__dataframe_external_funcs__.yaml
--rw-r--r--   0        0        0       79 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/pipe/__dataframe_instance_methods__.yaml
--rw-r--r--   0        0        0       70 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/pipe/__general_external_funcs__.yaml
--rw-r--r--   0        0        0       72 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/pipe/__general_instance_methods__.yaml
--rw-r--r--   0        0        0      424 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/pipe/__init__.yaml
--rw-r--r--   0        0        0      159 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/pipe/dataset_load_from_disk.yaml
--rw-r--r--   0        0        0      213 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/pipe/dataset_sample.yaml
--rw-r--r--   0        0        0      113 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/pipe/dataset_save_to_disk.yaml
--rw-r--r--   0        0        0       69 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/pipeline/__init__.yaml
--rw-r--r--   0        0        0      738 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/project/__init__.yaml
--rw-r--r--   0        0        0       38 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/running/__init__.yaml
--rw-r--r--   0        0        0      142 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/task/__batch__.yaml
--rw-r--r--   0        0        0      329 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/task/__init__.yaml
--rw-r--r--   0        0        0      132 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/conf/workflow/__init__.yaml
--rw-r--r--   0        0        0     6984 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/copier/__init__.py
--rw-r--r--   0        0        0     4683 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/core/__init__.py
--rw-r--r--   0        0        0    10023 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/core/config.py
--rw-r--r--   0        0        0     5514 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/core/hydra/__init__.py
--rw-r--r--   0        0        0     3266 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/core/hydra/main.py
--rw-r--r--   0        0        0     5695 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/core/hydra/utils.py
--rw-r--r--   0        0        0     5911 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/dotenv/__init__.py
--rw-r--r--   0        0        0     3517 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/graphics/__init__.py
--rw-r--r--   0        0        0     8470 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/graphics/collage.py
--rw-r--r--   0        0        0     4538 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/graphics/motion.py
--rw-r--r--   0        0        0     7020 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/graphics/utils.py
--rw-r--r--   0        0        0     4209 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/joblib/__init__.py
--rw-r--r--   0        0        0      111 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/joblib/batch/__init__.py
--rw-r--r--   0        0        0     6312 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/joblib/batch/apply.py
--rw-r--r--   0        0        0     4779 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/joblib/batch/apply_batch.py
--rw-r--r--   0        0        0    13823 2023-07-22 21:49:14.262739 hyfi-1.8.1/src/hyfi/joblib/batch/batcher.py
--rw-r--r--   0        0        0    19285 2023-07-22 21:49:14.266739 hyfi-1.8.1/src/hyfi/main/__init__.py
--rw-r--r--   0        0        0      280 2023-07-22 21:49:14.266739 hyfi-1.8.1/src/hyfi/module/__init__.py
--rw-r--r--   0        0        0     4327 2023-07-22 21:49:14.266739 hyfi-1.8.1/src/hyfi/path/__init__.py
--rw-r--r--   0        0        0     4092 2023-07-22 21:49:14.266739 hyfi-1.8.1/src/hyfi/path/base.py
--rw-r--r--   0        0        0      533 2023-07-22 21:49:14.266739 hyfi-1.8.1/src/hyfi/path/batch.py
--rw-r--r--   0        0        0      594 2023-07-22 21:49:14.266739 hyfi-1.8.1/src/hyfi/path/dirnames.py
--rw-r--r--   0        0        0     1484 2023-07-22 21:49:14.266739 hyfi-1.8.1/src/hyfi/path/task.py
--rw-r--r--   0        0        0     5030 2023-07-22 21:49:14.266739 hyfi-1.8.1/src/hyfi/pipe/__init__.py
--rw-r--r--   0        0        0     1323 2023-07-22 21:49:14.266739 hyfi-1.8.1/src/hyfi/pipe/datasets.py
--rw-r--r--   0        0        0     1455 2023-07-22 21:49:14.266739 hyfi-1.8.1/src/hyfi/pipe/test.py
--rw-r--r--   0        0        0     8129 2023-07-22 21:49:14.266739 hyfi-1.8.1/src/hyfi/pipeline/__init__.py
--rw-r--r--   0        0        0     3207 2023-07-22 21:49:14.266739 hyfi-1.8.1/src/hyfi/pipeline/configs.py
--rw-r--r--   0        0        0     5822 2023-07-22 21:49:14.266739 hyfi-1.8.1/src/hyfi/project/__init__.py
--rw-r--r--   0        0        0        0 2023-07-22 21:49:14.266739 hyfi-1.8.1/src/hyfi/py.typed
--rw-r--r--   0        0        0     3656 2023-07-22 21:49:14.266739 hyfi-1.8.1/src/hyfi/task/__init__.py
--rw-r--r--   0        0        0     7131 2023-07-22 21:49:14.266739 hyfi-1.8.1/src/hyfi/task/batch.py
--rw-r--r--   0        0        0        0 2023-07-22 21:49:14.266739 hyfi-1.8.1/src/hyfi/utils/__init__.py
--rw-r--r--   0        0        0    12742 2023-07-22 21:49:14.266739 hyfi-1.8.1/src/hyfi/utils/conf.py
--rw-r--r--   0        0        0     1314 2023-07-22 21:49:14.266739 hyfi-1.8.1/src/hyfi/utils/contexts.py
--rw-r--r--   0        0        0    30131 2023-07-22 21:49:14.266739 hyfi-1.8.1/src/hyfi/utils/datasets.py
--rw-r--r--   0        0        0     9036 2023-07-22 21:49:14.266739 hyfi-1.8.1/src/hyfi/utils/envs.py
--rw-r--r--   0        0        0    10857 2023-07-22 21:49:14.266739 hyfi-1.8.1/src/hyfi/utils/funcs.py
--rw-r--r--   0        0        0     4930 2023-07-22 21:49:14.266739 hyfi-1.8.1/src/hyfi/utils/gpumon.py
--rw-r--r--   0        0        0    23279 2023-07-22 21:49:14.266739 hyfi-1.8.1/src/hyfi/utils/iolibs.py
--rw-r--r--   0        0        0     2259 2023-07-22 21:49:14.266739 hyfi-1.8.1/src/hyfi/utils/logging.py
--rw-r--r--   0        0        0    12820 2023-07-22 21:49:14.266739 hyfi-1.8.1/src/hyfi/utils/notebooks.py
--rw-r--r--   0        0        0     7164 2023-07-22 21:49:14.266739 hyfi-1.8.1/src/hyfi/utils/packages.py
--rw-r--r--   0        0        0      382 2023-07-22 21:49:14.266739 hyfi-1.8.1/src/hyfi/utils/types.py
--rw-r--r--   0        0        0     1116 2023-07-22 21:49:14.266739 hyfi-1.8.1/src/hyfi/workflow/__init__.py
--rw-r--r--   0        0        0     3386 1970-01-01 00:00:00.000000 hyfi-1.8.1/PKG-INFO
+-rw-r--r--   0        0        0     1071 2023-07-23 04:04:11.546899 hyfi-1.8.2/LICENSE
+-rw-r--r--   0        0        0     1881 2023-07-23 04:04:11.546899 hyfi-1.8.2/README.md
+-rw-r--r--   0        0        0     4853 2023-07-23 04:04:36.443314 hyfi-1.8.2/pyproject.toml
+-rw-r--r--   0        0        0     4168 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/__cli__.py
+-rw-r--r--   0        0        0     3586 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/__click__.py
+-rw-r--r--   0        0        0     1183 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/__init__.py
+-rw-r--r--   0        0        0       22 2023-07-23 04:04:36.363313 hyfi-1.8.2/src/hyfi/_version.py
+-rw-r--r--   0        0        0     1497 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/about/__init__.py
+-rw-r--r--   0        0        0     7292 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/batch/__init__.py
+-rw-r--r--   0        0        0     1206 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/cached_path/__init__.py
+-rw-r--r--   0        0        0    14373 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/cached_path/_cached_path.py
+-rw-r--r--   0        0        0     1619 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/cached_path/cache_file.py
+-rw-r--r--   0        0        0     1100 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/cached_path/common.py
+-rw-r--r--   0        0        0     1921 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/cached_path/file_lock.py
+-rw-r--r--   0        0        0     3441 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/cached_path/meta.py
+-rw-r--r--   0        0        0     3247 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/cached_path/progress.py
+-rw-r--r--   0        0        0     1437 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/cached_path/schemes/__init__.py
+-rw-r--r--   0        0        0     1815 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/cached_path/schemes/beaker.py
+-rw-r--r--   0        0        0     2862 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/cached_path/schemes/hf.py
+-rw-r--r--   0        0        0     2942 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/cached_path/schemes/http.py
+-rw-r--r--   0        0        0     3645 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/cached_path/schemes/scheme_client.py
+-rw-r--r--   0        0        0     1222 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/cached_path/testing.py
+-rw-r--r--   0        0        0     4799 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/cached_path/util.py
+-rw-r--r--   0        0        0      464 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/cached_path/version.py
+-rw-r--r--   0        0        0    24360 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/composer/__init__.py
+-rw-r--r--   0        0        0     7328 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/composer/base.py
+-rw-r--r--   0        0        0     1933 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/composer/pydantic.py
+-rw-r--r--   0        0        0        0 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/conf/__init__.py
+-rw-r--r--   0        0        0      193 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/conf/about/__init__.yaml
+-rw-r--r--   0        0        0      588 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/conf/batch/__init__.yaml
+-rw-r--r--   0        0        0       44 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/conf/cmd/__init__.yaml
+-rw-r--r--   0        0        0       60 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/conf/cmd/about.yaml
+-rw-r--r--   0        0        0      160 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/conf/cmd/copy_conf.yaml
+-rw-r--r--   0        0        0       83 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/conf/cmd/run_task.yaml
+-rw-r--r--   0        0        0       91 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/conf/cmd/run_workflow.yaml
+-rw-r--r--   0        0        0      209 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/conf/config.yaml
+-rw-r--r--   0        0        0      662 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/conf/copier/__init__.yaml
+-rw-r--r--   0        0        0      709 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/conf/dotenv/__init__.yaml
+-rw-r--r--   0        0        0     1053 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/conf/hydra/help/help.yaml
+-rw-r--r--   0        0        0      264 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/conf/hydra/job_logging/custom.yaml
+-rw-r--r--   0        0        0      132 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/conf/joblib/__init__.yaml
+-rw-r--r--   0        0        0      198 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/conf/mode/__debug__.yaml
+-rw-r--r--   0        0        0      955 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/conf/mode/__init__.yaml
+-rw-r--r--   0        0        0       61 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/conf/module/__init__.yaml
+-rw-r--r--   0        0        0       72 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/conf/path/__batch__.yaml
+-rw-r--r--   0        0        0      876 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/conf/path/__init__.yaml
+-rw-r--r--   0        0        0       91 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/conf/path/__task__.yaml
+-rw-r--r--   0        0        0      286 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/conf/path/dirnames/__init__.yaml
+-rw-r--r--   0        0        0       76 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/conf/pipe/__dataframe__.yaml
+-rw-r--r--   0        0        0       77 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/conf/pipe/__dataframe_external_funcs__.yaml
+-rw-r--r--   0        0        0       79 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/conf/pipe/__dataframe_instance_methods__.yaml
+-rw-r--r--   0        0        0       70 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/conf/pipe/__general_external_funcs__.yaml
+-rw-r--r--   0        0        0       72 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/conf/pipe/__general_instance_methods__.yaml
+-rw-r--r--   0        0        0      424 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/conf/pipe/__init__.yaml
+-rw-r--r--   0        0        0      159 2023-07-23 04:04:11.550899 hyfi-1.8.2/src/hyfi/conf/pipe/dataset_load_from_disk.yaml
+-rw-r--r--   0        0        0      213 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/conf/pipe/dataset_sample.yaml
+-rw-r--r--   0        0        0      113 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/conf/pipe/dataset_save_to_disk.yaml
+-rw-r--r--   0        0        0       69 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/conf/pipeline/__init__.yaml
+-rw-r--r--   0        0        0      738 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/conf/project/__init__.yaml
+-rw-r--r--   0        0        0       38 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/conf/running/__init__.yaml
+-rw-r--r--   0        0        0      142 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/conf/task/__batch__.yaml
+-rw-r--r--   0        0        0      329 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/conf/task/__init__.yaml
+-rw-r--r--   0        0        0      132 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/conf/workflow/__init__.yaml
+-rw-r--r--   0        0        0     6984 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/copier/__init__.py
+-rw-r--r--   0        0        0     4683 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/core/__init__.py
+-rw-r--r--   0        0        0    10023 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/core/config.py
+-rw-r--r--   0        0        0     5514 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/core/hydra/__init__.py
+-rw-r--r--   0        0        0     3266 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/core/hydra/main.py
+-rw-r--r--   0        0        0     5695 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/core/hydra/utils.py
+-rw-r--r--   0        0        0     5911 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/dotenv/__init__.py
+-rw-r--r--   0        0        0     3517 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/graphics/__init__.py
+-rw-r--r--   0        0        0     8470 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/graphics/collage.py
+-rw-r--r--   0        0        0     4538 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/graphics/motion.py
+-rw-r--r--   0        0        0     7020 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/graphics/utils.py
+-rw-r--r--   0        0        0     4209 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/joblib/__init__.py
+-rw-r--r--   0        0        0      111 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/joblib/batch/__init__.py
+-rw-r--r--   0        0        0     6312 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/joblib/batch/apply.py
+-rw-r--r--   0        0        0     4779 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/joblib/batch/apply_batch.py
+-rw-r--r--   0        0        0    13823 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/joblib/batch/batcher.py
+-rw-r--r--   0        0        0    19642 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/main/__init__.py
+-rw-r--r--   0        0        0      280 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/module/__init__.py
+-rw-r--r--   0        0        0     4327 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/path/__init__.py
+-rw-r--r--   0        0        0     4092 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/path/base.py
+-rw-r--r--   0        0        0      533 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/path/batch.py
+-rw-r--r--   0        0        0      594 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/path/dirnames.py
+-rw-r--r--   0        0        0     1484 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/path/task.py
+-rw-r--r--   0        0        0     5030 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/pipe/__init__.py
+-rw-r--r--   0        0        0     1323 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/pipe/datasets.py
+-rw-r--r--   0        0        0     1455 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/pipe/test.py
+-rw-r--r--   0        0        0     8129 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/pipeline/__init__.py
+-rw-r--r--   0        0        0     3207 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/pipeline/configs.py
+-rw-r--r--   0        0        0     5822 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/project/__init__.py
+-rw-r--r--   0        0        0        0 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/py.typed
+-rw-r--r--   0        0        0     3656 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/task/__init__.py
+-rw-r--r--   0        0        0     7131 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/task/batch.py
+-rw-r--r--   0        0        0        0 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/utils/__init__.py
+-rw-r--r--   0        0        0    12742 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/utils/conf.py
+-rw-r--r--   0        0        0     1314 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/utils/contexts.py
+-rw-r--r--   0        0        0    30131 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/utils/datasets.py
+-rw-r--r--   0        0        0     9036 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/utils/envs.py
+-rw-r--r--   0        0        0    10857 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/utils/funcs.py
+-rw-r--r--   0        0        0     4930 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/utils/gpumon.py
+-rw-r--r--   0        0        0    23279 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/utils/iolibs.py
+-rw-r--r--   0        0        0     2259 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/utils/logging.py
+-rw-r--r--   0        0        0    12820 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/utils/notebooks.py
+-rw-r--r--   0        0        0     7164 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/utils/packages.py
+-rw-r--r--   0        0        0      382 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/utils/types.py
+-rw-r--r--   0        0        0     1116 2023-07-23 04:04:11.554899 hyfi-1.8.2/src/hyfi/workflow/__init__.py
+-rw-r--r--   0        0        0     3386 1970-01-01 00:00:00.000000 hyfi-1.8.2/PKG-INFO
```

### Comparing `hyfi-1.8.1/LICENSE` & `hyfi-1.8.2/LICENSE`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/README.md` & `hyfi-1.8.2/README.md`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/pyproject.toml` & `hyfi-1.8.2/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "hyfi"
-version = "1.8.1"
+version = "1.8.2"
 description = "Hydra Fast Interface (Hydra and Pydantic based interface framework)"
 authors = ["Young Joon Lee <entelecheia@hotmail.com>"]
 license = "MIT"
 homepage = "https://hyfi.entelecheia.ai"
 repository = "https://github.com/entelecheia/hyfi"
 readme = "README.md"
 packages = [{ include = "hyfi", from = "src" }]
```

### Comparing `hyfi-1.8.1/src/hyfi/__cli__.py` & `hyfi-1.8.2/src/hyfi/__cli__.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/__click__.py` & `hyfi-1.8.2/src/hyfi/__click__.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/__init__.py` & `hyfi-1.8.2/src/hyfi/__init__.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/about/__init__.py` & `hyfi-1.8.2/src/hyfi/about/__init__.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/batch/__init__.py` & `hyfi-1.8.2/src/hyfi/batch/__init__.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/cached_path/__init__.py` & `hyfi-1.8.2/src/hyfi/cached_path/__init__.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/cached_path/_cached_path.py` & `hyfi-1.8.2/src/hyfi/cached_path/_cached_path.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/cached_path/cache_file.py` & `hyfi-1.8.2/src/hyfi/cached_path/cache_file.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/cached_path/common.py` & `hyfi-1.8.2/src/hyfi/cached_path/common.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/cached_path/file_lock.py` & `hyfi-1.8.2/src/hyfi/cached_path/file_lock.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/cached_path/meta.py` & `hyfi-1.8.2/src/hyfi/cached_path/meta.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/cached_path/progress.py` & `hyfi-1.8.2/src/hyfi/cached_path/progress.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/cached_path/schemes/__init__.py` & `hyfi-1.8.2/src/hyfi/cached_path/schemes/__init__.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/cached_path/schemes/beaker.py` & `hyfi-1.8.2/src/hyfi/cached_path/schemes/beaker.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/cached_path/schemes/hf.py` & `hyfi-1.8.2/src/hyfi/cached_path/schemes/hf.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/cached_path/schemes/http.py` & `hyfi-1.8.2/src/hyfi/cached_path/schemes/http.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/cached_path/schemes/scheme_client.py` & `hyfi-1.8.2/src/hyfi/cached_path/schemes/scheme_client.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/cached_path/testing.py` & `hyfi-1.8.2/src/hyfi/cached_path/testing.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/cached_path/util.py` & `hyfi-1.8.2/src/hyfi/cached_path/util.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/composer/__init__.py` & `hyfi-1.8.2/src/hyfi/composer/__init__.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/composer/base.py` & `hyfi-1.8.2/src/hyfi/composer/base.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/composer/pydantic.py` & `hyfi-1.8.2/src/hyfi/composer/pydantic.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/conf/batch/__init__.yaml` & `hyfi-1.8.2/src/hyfi/conf/batch/__init__.yaml`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/conf/copier/__init__.yaml` & `hyfi-1.8.2/src/hyfi/conf/copier/__init__.yaml`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/conf/dotenv/__init__.yaml` & `hyfi-1.8.2/src/hyfi/conf/dotenv/__init__.yaml`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/conf/hydra/help/help.yaml` & `hyfi-1.8.2/src/hyfi/conf/hydra/help/help.yaml`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/conf/mode/__init__.yaml` & `hyfi-1.8.2/src/hyfi/conf/mode/__init__.yaml`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/conf/path/__init__.yaml` & `hyfi-1.8.2/src/hyfi/conf/path/__init__.yaml`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/conf/project/__init__.yaml` & `hyfi-1.8.2/src/hyfi/conf/project/__init__.yaml`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/copier/__init__.py` & `hyfi-1.8.2/src/hyfi/copier/__init__.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/core/__init__.py` & `hyfi-1.8.2/src/hyfi/core/__init__.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/core/config.py` & `hyfi-1.8.2/src/hyfi/core/config.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/core/hydra/__init__.py` & `hyfi-1.8.2/src/hyfi/core/hydra/__init__.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/core/hydra/main.py` & `hyfi-1.8.2/src/hyfi/core/hydra/main.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/core/hydra/utils.py` & `hyfi-1.8.2/src/hyfi/core/hydra/utils.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/dotenv/__init__.py` & `hyfi-1.8.2/src/hyfi/dotenv/__init__.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/graphics/__init__.py` & `hyfi-1.8.2/src/hyfi/graphics/__init__.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/graphics/collage.py` & `hyfi-1.8.2/src/hyfi/graphics/collage.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/graphics/motion.py` & `hyfi-1.8.2/src/hyfi/graphics/motion.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/graphics/utils.py` & `hyfi-1.8.2/src/hyfi/graphics/utils.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/joblib/__init__.py` & `hyfi-1.8.2/src/hyfi/joblib/__init__.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/joblib/batch/apply.py` & `hyfi-1.8.2/src/hyfi/joblib/batch/apply.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/joblib/batch/apply_batch.py` & `hyfi-1.8.2/src/hyfi/joblib/batch/apply_batch.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/joblib/batch/batcher.py` & `hyfi-1.8.2/src/hyfi/joblib/batch/batcher.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/main/__init__.py` & `hyfi-1.8.2/src/hyfi/main/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -10,14 +10,15 @@
 from omegaconf import DictConfig, OmegaConf
 
 from hyfi.cached_path import cached_path
 from hyfi.composer import Composer, SpecialKeys
 from hyfi.copier import Copier
 from hyfi.core import (
     __app_version__,
+    __global_hyfi__,
     __home_path__,
     __hyfi_path__,
     __hyfi_version__,
     __package_name__,
     __package_path__,
 )
 from hyfi.core.config import __global_config__, __search_package_path__
@@ -95,14 +96,26 @@
     __package_path__ = __package_path__()
     __app_version__ = __app_version__()
 
     def __init__(self) -> None:
         raise NotImplementedError("Use one of the static construction functions")
 
     @staticmethod
+    def initialize_global_hyfi(
+        package_name: str,
+        version: str,
+    ) -> None:
+        """
+        Initializes the global HyFI instance.
+
+        This function should be called before any other HyFI function.
+        """
+        __global_hyfi__.initialize(package_name=package_name, version=version)
+
+    @staticmethod
     def about(**args) -> None:
         """Print the about information"""
         __global_config__.print_about(**args)
 
     @staticmethod
     def init_project(
         project_name: str = "",
```

### Comparing `hyfi-1.8.1/src/hyfi/path/__init__.py` & `hyfi-1.8.2/src/hyfi/path/__init__.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/path/base.py` & `hyfi-1.8.2/src/hyfi/path/base.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/path/batch.py` & `hyfi-1.8.2/src/hyfi/path/batch.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/path/dirnames.py` & `hyfi-1.8.2/src/hyfi/path/dirnames.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/path/task.py` & `hyfi-1.8.2/src/hyfi/path/task.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/pipe/__init__.py` & `hyfi-1.8.2/src/hyfi/pipe/__init__.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/pipe/datasets.py` & `hyfi-1.8.2/src/hyfi/pipe/datasets.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/pipe/test.py` & `hyfi-1.8.2/src/hyfi/pipe/test.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/pipeline/__init__.py` & `hyfi-1.8.2/src/hyfi/pipeline/__init__.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/pipeline/configs.py` & `hyfi-1.8.2/src/hyfi/pipeline/configs.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/project/__init__.py` & `hyfi-1.8.2/src/hyfi/project/__init__.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/task/__init__.py` & `hyfi-1.8.2/src/hyfi/task/__init__.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/task/batch.py` & `hyfi-1.8.2/src/hyfi/task/batch.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/utils/conf.py` & `hyfi-1.8.2/src/hyfi/utils/conf.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/utils/contexts.py` & `hyfi-1.8.2/src/hyfi/utils/contexts.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/utils/datasets.py` & `hyfi-1.8.2/src/hyfi/utils/datasets.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/utils/envs.py` & `hyfi-1.8.2/src/hyfi/utils/envs.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/utils/funcs.py` & `hyfi-1.8.2/src/hyfi/utils/funcs.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/utils/gpumon.py` & `hyfi-1.8.2/src/hyfi/utils/gpumon.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/utils/iolibs.py` & `hyfi-1.8.2/src/hyfi/utils/iolibs.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/utils/logging.py` & `hyfi-1.8.2/src/hyfi/utils/logging.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/utils/notebooks.py` & `hyfi-1.8.2/src/hyfi/utils/notebooks.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/utils/packages.py` & `hyfi-1.8.2/src/hyfi/utils/packages.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/src/hyfi/workflow/__init__.py` & `hyfi-1.8.2/src/hyfi/workflow/__init__.py`

 * *Files identical despite different names*

### Comparing `hyfi-1.8.1/PKG-INFO` & `hyfi-1.8.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: hyfi
-Version: 1.8.1
+Version: 1.8.2
 Summary: Hydra Fast Interface (Hydra and Pydantic based interface framework)
 Home-page: https://hyfi.entelecheia.ai
 License: MIT
 Author: Young Joon Lee
 Author-email: entelecheia@hotmail.com
 Requires-Python: >=3.8.1,<3.12
 Classifier: License :: OSI Approved :: MIT License
```

