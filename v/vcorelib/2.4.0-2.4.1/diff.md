# Comparing `tmp/vcorelib-2.4.0.tar.gz` & `tmp/vcorelib-2.4.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "vcorelib-2.4.0.tar", last modified: Sat Jul 22 20:12:17 2023, max compression
+gzip compressed data, was "vcorelib-2.4.1.tar", last modified: Sun Jul 23 04:19:35 2023, max compression
```

## Comparing `vcorelib-2.4.0.tar` & `vcorelib-2.4.1.tar`

### file list

```diff
@@ -1,106 +1,106 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 20:12:17.361319 vcorelib-2.4.0/
--rw-r--r--   0 runner    (1001) docker     (123)     1071 2023-07-22 20:10:57.000000 vcorelib-2.4.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     2539 2023-07-22 20:12:17.361319 vcorelib-2.4.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1663 2023-07-22 20:10:57.000000 vcorelib-2.4.0/README.md
--rw-r--r--   0 runner    (1001) docker     (123)     1075 2023-07-22 20:10:57.000000 vcorelib-2.4.0/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-22 20:12:17.361319 vcorelib-2.4.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)      827 2023-07-22 20:10:57.000000 vcorelib-2.4.0/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 20:12:17.353319 vcorelib-2.4.0/tests/
--rw-r--r--   0 runner    (1001) docker     (123)      761 2023-07-22 20:10:57.000000 vcorelib-2.4.0/tests/test_logging.py
--rw-r--r--   0 runner    (1001) docker     (123)      533 2023-07-22 20:10:57.000000 vcorelib-2.4.0/tests/test_names.py
--rw-r--r--   0 runner    (1001) docker     (123)     1639 2023-07-22 20:10:57.000000 vcorelib-2.4.0/tests/test_namespace.py
--rw-r--r--   0 runner    (1001) docker     (123)      398 2023-07-22 20:10:57.000000 vcorelib-2.4.0/tests/test_python.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 20:12:17.353319 vcorelib-2.4.0/vcorelib/
--rw-r--r--   0 runner    (1001) docker     (123)      381 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 20:12:17.353319 vcorelib-2.4.0/vcorelib/args/
--rw-r--r--   0 runner    (1001) docker     (123)     1617 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/args/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1269 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/args/newline.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 20:12:17.353319 vcorelib-2.4.0/vcorelib/asyncio/
--rw-r--r--   0 runner    (1001) docker     (123)     4803 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/asyncio/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3592 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/asyncio/cli.py
--rw-r--r--   0 runner    (1001) docker     (123)     1527 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/asyncio/subprocess.py
--rw-r--r--   0 runner    (1001) docker     (123)       96 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/dev_requirements.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 20:12:17.353319 vcorelib-2.4.0/vcorelib/dict/
--rw-r--r--   0 runner    (1001) docker     (123)     4924 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/dict/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1809 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/dict/cache.py
--rw-r--r--   0 runner    (1001) docker     (123)     4552 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/dict/codec.py
--rw-r--r--   0 runner    (1001) docker     (123)     3047 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/dict/config.py
--rw-r--r--   0 runner    (1001) docker     (123)     2822 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/dict/env.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 20:12:17.353319 vcorelib-2.4.0/vcorelib/graph/
--rw-r--r--   0 runner    (1001) docker     (123)     2260 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/graph/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7436 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/graph/abc.py
--rw-r--r--   0 runner    (1001) docker     (123)     1764 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/graph/edge.py
--rw-r--r--   0 runner    (1001) docker     (123)     2621 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/graph/node.py
--rw-r--r--   0 runner    (1001) docker     (123)     5113 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/graph/port.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 20:12:17.357318 vcorelib-2.4.0/vcorelib/io/
--rw-r--r--   0 runner    (1001) docker     (123)      761 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/io/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1673 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/io/abc.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 20:12:17.357318 vcorelib-2.4.0/vcorelib/io/arbiter/
--rw-r--r--   0 runner    (1001) docker     (123)      259 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/io/arbiter/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5615 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/io/arbiter/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     2142 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/io/arbiter/context.py
--rw-r--r--   0 runner    (1001) docker     (123)     3878 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/io/arbiter/directory.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 20:12:17.357318 vcorelib-2.4.0/vcorelib/io/archive/
--rw-r--r--   0 runner    (1001) docker     (123)     4404 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/io/archive/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5716 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/io/cache.py
--rw-r--r--   0 runner    (1001) docker     (123)     3102 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/io/decode.py
--rw-r--r--   0 runner    (1001) docker     (123)     2201 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/io/encode.py
--rw-r--r--   0 runner    (1001) docker     (123)     1758 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/io/mapping.py
--rw-r--r--   0 runner    (1001) docker     (123)     6224 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/io/types.py
--rw-r--r--   0 runner    (1001) docker     (123)     1496 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/logging.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 20:12:17.357318 vcorelib-2.4.0/vcorelib/math/
--rw-r--r--   0 runner    (1001) docker     (123)      833 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/math/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 20:12:17.357318 vcorelib-2.4.0/vcorelib/math/analysis/
--rw-r--r--   0 runner    (1001) docker     (123)      552 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/math/analysis/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2530 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/math/analysis/average.py
--rw-r--r--   0 runner    (1001) docker     (123)     1173 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/math/analysis/buffer.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 20:12:17.357318 vcorelib-2.4.0/vcorelib/math/analysis/rate/
--rw-r--r--   0 runner    (1001) docker     (123)     2720 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/math/analysis/rate/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1584 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/math/analysis/rate/limiter.py
--rw-r--r--   0 runner    (1001) docker     (123)     1401 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/math/analysis/weighted.py
--rw-r--r--   0 runner    (1001) docker     (123)     4245 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/math/time.py
--rw-r--r--   0 runner    (1001) docker     (123)     1155 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/math/unit.py
--rw-r--r--   0 runner    (1001) docker     (123)      578 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/names.py
--rw-r--r--   0 runner    (1001) docker     (123)     5809 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/namespace.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 20:12:17.357318 vcorelib-2.4.0/vcorelib/paths/
--rw-r--r--   0 runner    (1001) docker     (123)     4558 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/paths/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2177 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/paths/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     1772 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/paths/context.py
--rw-r--r--   0 runner    (1001) docker     (123)     2478 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/paths/hashing.py
--rw-r--r--   0 runner    (1001) docker     (123)     4058 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/paths/info.py
--rw-r--r--   0 runner    (1001) docker     (123)     6913 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/paths/info_cache.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 20:12:17.357318 vcorelib-2.4.0/vcorelib/platform/
--rw-r--r--   0 runner    (1001) docker     (123)      814 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/platform/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/py.typed
--rw-r--r--   0 runner    (1001) docker     (123)     2055 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/python.py
--rw-r--r--   0 runner    (1001) docker     (123)       70 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/requirements.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 20:12:17.357318 vcorelib-2.4.0/vcorelib/schemas/
--rw-r--r--   0 runner    (1001) docker     (123)     1425 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/schemas/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3669 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/schemas/base.py
--rw-r--r--   0 runner    (1001) docker     (123)     2001 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/schemas/json.py
--rw-r--r--   0 runner    (1001) docker     (123)     1457 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/schemas/mixins.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 20:12:17.357318 vcorelib-2.4.0/vcorelib/script/
--rw-r--r--   0 runner    (1001) docker     (123)     1856 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/script/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 20:12:17.357318 vcorelib-2.4.0/vcorelib/target/
--rw-r--r--   0 runner    (1001) docker     (123)     3187 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/target/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4179 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/target/evaluation.py
--rw-r--r--   0 runner    (1001) docker     (123)     2359 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/target/expression.py
--rw-r--r--   0 runner    (1001) docker     (123)     3190 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/target/resolver.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 20:12:17.361319 vcorelib-2.4.0/vcorelib/task/
--rw-r--r--   0 runner    (1001) docker     (123)    11990 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/task/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 20:12:17.361319 vcorelib-2.4.0/vcorelib/task/dict/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/task/dict/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1182 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/task/dict/melder.py
--rw-r--r--   0 runner    (1001) docker     (123)     6368 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/task/manager.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 20:12:17.361319 vcorelib-2.4.0/vcorelib/task/subprocess/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/task/subprocess/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     8155 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/task/subprocess/run.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 20:12:17.361319 vcorelib-2.4.0/vcorelib/task/time/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/task/time/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      624 2023-07-22 20:10:57.000000 vcorelib-2.4.0/vcorelib/task/time/sleep.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 20:12:17.353319 vcorelib-2.4.0/vcorelib.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2539 2023-07-22 20:12:17.000000 vcorelib-2.4.0/vcorelib.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2098 2023-07-22 20:12:17.000000 vcorelib-2.4.0/vcorelib.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-22 20:12:17.000000 vcorelib-2.4.0/vcorelib.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      174 2023-07-22 20:12:17.000000 vcorelib-2.4.0/vcorelib.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-22 20:12:17.000000 vcorelib-2.4.0/vcorelib.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:19:35.171023 vcorelib-2.4.1/
+-rw-r--r--   0 runner    (1001) docker     (123)     1071 2023-07-23 04:18:17.000000 vcorelib-2.4.1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     2539 2023-07-23 04:19:35.171023 vcorelib-2.4.1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1663 2023-07-23 04:18:17.000000 vcorelib-2.4.1/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1075 2023-07-23 04:18:17.000000 vcorelib-2.4.1/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 04:19:35.171023 vcorelib-2.4.1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)      827 2023-07-23 04:18:17.000000 vcorelib-2.4.1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:19:35.163023 vcorelib-2.4.1/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)      761 2023-07-23 04:18:17.000000 vcorelib-2.4.1/tests/test_logging.py
+-rw-r--r--   0 runner    (1001) docker     (123)      533 2023-07-23 04:18:17.000000 vcorelib-2.4.1/tests/test_names.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1639 2023-07-23 04:18:17.000000 vcorelib-2.4.1/tests/test_namespace.py
+-rw-r--r--   0 runner    (1001) docker     (123)      398 2023-07-23 04:18:17.000000 vcorelib-2.4.1/tests/test_python.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:19:35.163023 vcorelib-2.4.1/vcorelib/
+-rw-r--r--   0 runner    (1001) docker     (123)      381 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:19:35.167023 vcorelib-2.4.1/vcorelib/args/
+-rw-r--r--   0 runner    (1001) docker     (123)     1617 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/args/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1269 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/args/newline.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:19:35.167023 vcorelib-2.4.1/vcorelib/asyncio/
+-rw-r--r--   0 runner    (1001) docker     (123)     4803 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/asyncio/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3592 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/asyncio/cli.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1527 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/asyncio/subprocess.py
+-rw-r--r--   0 runner    (1001) docker     (123)       96 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/dev_requirements.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:19:35.167023 vcorelib-2.4.1/vcorelib/dict/
+-rw-r--r--   0 runner    (1001) docker     (123)     4924 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/dict/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1809 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/dict/cache.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4552 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/dict/codec.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3047 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/dict/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2822 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/dict/env.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:19:35.167023 vcorelib-2.4.1/vcorelib/graph/
+-rw-r--r--   0 runner    (1001) docker     (123)     2260 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/graph/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7436 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/graph/abc.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1764 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/graph/edge.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2621 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/graph/node.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5113 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/graph/port.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:19:35.167023 vcorelib-2.4.1/vcorelib/io/
+-rw-r--r--   0 runner    (1001) docker     (123)      761 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/io/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1673 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/io/abc.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:19:35.167023 vcorelib-2.4.1/vcorelib/io/arbiter/
+-rw-r--r--   0 runner    (1001) docker     (123)      259 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/io/arbiter/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5615 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/io/arbiter/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2142 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/io/arbiter/context.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3878 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/io/arbiter/directory.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:19:35.167023 vcorelib-2.4.1/vcorelib/io/archive/
+-rw-r--r--   0 runner    (1001) docker     (123)     4404 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/io/archive/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5716 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/io/cache.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3102 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/io/decode.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2201 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/io/encode.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1758 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/io/mapping.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6224 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/io/types.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1622 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/logging.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:19:35.167023 vcorelib-2.4.1/vcorelib/math/
+-rw-r--r--   0 runner    (1001) docker     (123)      833 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/math/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:19:35.171023 vcorelib-2.4.1/vcorelib/math/analysis/
+-rw-r--r--   0 runner    (1001) docker     (123)      552 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/math/analysis/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2530 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/math/analysis/average.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1173 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/math/analysis/buffer.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:19:35.171023 vcorelib-2.4.1/vcorelib/math/analysis/rate/
+-rw-r--r--   0 runner    (1001) docker     (123)     2720 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/math/analysis/rate/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1584 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/math/analysis/rate/limiter.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1401 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/math/analysis/weighted.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4245 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/math/time.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1155 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/math/unit.py
+-rw-r--r--   0 runner    (1001) docker     (123)      578 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/names.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5809 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/namespace.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:19:35.171023 vcorelib-2.4.1/vcorelib/paths/
+-rw-r--r--   0 runner    (1001) docker     (123)     4558 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/paths/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2177 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/paths/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1772 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/paths/context.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2478 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/paths/hashing.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4058 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/paths/info.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6913 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/paths/info_cache.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:19:35.171023 vcorelib-2.4.1/vcorelib/platform/
+-rw-r--r--   0 runner    (1001) docker     (123)      814 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/platform/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/py.typed
+-rw-r--r--   0 runner    (1001) docker     (123)     2055 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/python.py
+-rw-r--r--   0 runner    (1001) docker     (123)       70 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/requirements.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:19:35.171023 vcorelib-2.4.1/vcorelib/schemas/
+-rw-r--r--   0 runner    (1001) docker     (123)     1425 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/schemas/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3669 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/schemas/base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2001 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/schemas/json.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1457 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/schemas/mixins.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:19:35.171023 vcorelib-2.4.1/vcorelib/script/
+-rw-r--r--   0 runner    (1001) docker     (123)     1856 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/script/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:19:35.171023 vcorelib-2.4.1/vcorelib/target/
+-rw-r--r--   0 runner    (1001) docker     (123)     3187 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/target/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4179 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/target/evaluation.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2359 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/target/expression.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3190 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/target/resolver.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:19:35.171023 vcorelib-2.4.1/vcorelib/task/
+-rw-r--r--   0 runner    (1001) docker     (123)    11990 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/task/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:19:35.171023 vcorelib-2.4.1/vcorelib/task/dict/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/task/dict/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1182 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/task/dict/melder.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6368 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/task/manager.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:19:35.171023 vcorelib-2.4.1/vcorelib/task/subprocess/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/task/subprocess/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8155 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/task/subprocess/run.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:19:35.171023 vcorelib-2.4.1/vcorelib/task/time/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/task/time/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      624 2023-07-23 04:18:17.000000 vcorelib-2.4.1/vcorelib/task/time/sleep.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:19:35.167023 vcorelib-2.4.1/vcorelib.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2539 2023-07-23 04:19:35.000000 vcorelib-2.4.1/vcorelib.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2098 2023-07-23 04:19:35.000000 vcorelib-2.4.1/vcorelib.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 04:19:35.000000 vcorelib-2.4.1/vcorelib.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      174 2023-07-23 04:19:35.000000 vcorelib-2.4.1/vcorelib.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        9 2023-07-23 04:19:35.000000 vcorelib-2.4.1/vcorelib.egg-info/top_level.txt
```

### Comparing `vcorelib-2.4.0/LICENSE` & `vcorelib-2.4.1/LICENSE`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/PKG-INFO` & `vcorelib-2.4.1/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: vcorelib
-Version: 2.4.0
+Version: 2.4.1
 Summary: A collection of core Python utilities.
 Home-page: https://github.com/vkottler/vcorelib
 Author: Vaughn Kottler
 Author-email: Vaughn Kottler <vaughnkottler@gmail.com>
 Maintainer-email: Vaughn Kottler <vaughnkottler@gmail.com>
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
@@ -21,19 +21,19 @@
 Provides-Extra: test
 License-File: LICENSE
 
 <!--
     =====================================
     generator=datazen
     version=3.1.2
-    hash=10535d341384b031fe2481a3715c8a79
+    hash=3e8288e50ab8a440ea21e053b4ff1b6a
     =====================================
 -->
 
-# vcorelib ([2.4.0](https://pypi.org/project/vcorelib/))
+# vcorelib ([2.4.1](https://pypi.org/project/vcorelib/))
 
 [![python](https://img.shields.io/pypi/pyversions/vcorelib.svg)](https://pypi.org/project/vcorelib/)
 ![Build Status](https://github.com/vkottler/vcorelib/workflows/Python%20Package/badge.svg)
 [![codecov](https://codecov.io/gh/vkottler/vcorelib/branch/master/graphs/badge.svg?branch=master)](https://codecov.io/github/vkottler/vcorelib)
 ![PyPI - Status](https://img.shields.io/pypi/status/vcorelib)
 ![Dependents (via libraries.io)](https://img.shields.io/librariesio/dependents/pypi/vcorelib)
```

### Comparing `vcorelib-2.4.0/README.md` & `vcorelib-2.4.1/README.md`

 * *Files 15% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 <!--
     =====================================
     generator=datazen
     version=3.1.2
-    hash=10535d341384b031fe2481a3715c8a79
+    hash=3e8288e50ab8a440ea21e053b4ff1b6a
     =====================================
 -->
 
-# vcorelib ([2.4.0](https://pypi.org/project/vcorelib/))
+# vcorelib ([2.4.1](https://pypi.org/project/vcorelib/))
 
 [![python](https://img.shields.io/pypi/pyversions/vcorelib.svg)](https://pypi.org/project/vcorelib/)
 ![Build Status](https://github.com/vkottler/vcorelib/workflows/Python%20Package/badge.svg)
 [![codecov](https://codecov.io/gh/vkottler/vcorelib/branch/master/graphs/badge.svg?branch=master)](https://codecov.io/github/vkottler/vcorelib)
 ![PyPI - Status](https://img.shields.io/pypi/status/vcorelib)
 ![Dependents (via libraries.io)](https://img.shields.io/librariesio/dependents/pypi/vcorelib)
```

### Comparing `vcorelib-2.4.0/pyproject.toml` & `vcorelib-2.4.1/pyproject.toml`

 * *Files 10% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools-wrapper", "trove-classifiers"]
 build-backend = "setuptools.build_meta:__legacy__"
 
 [project]
 name = "vcorelib"
-version = "2.4.0"
+version = "2.4.1"
 description = "A collection of core Python utilities."
 readme = "README.md"
 requires-python = ">=3.8"
 authors = [
   {name = "Vaughn Kottler", email = "vaughnkottler@gmail.com"}
 ]
 maintainers = [
```

### Comparing `vcorelib-2.4.0/setup.py` & `vcorelib-2.4.1/setup.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/tests/test_logging.py` & `vcorelib-2.4.1/tests/test_logging.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/tests/test_names.py` & `vcorelib-2.4.1/tests/test_names.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/tests/test_namespace.py` & `vcorelib-2.4.1/tests/test_namespace.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/args/__init__.py` & `vcorelib-2.4.1/vcorelib/args/__init__.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/args/newline.py` & `vcorelib-2.4.1/vcorelib/args/newline.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/asyncio/__init__.py` & `vcorelib-2.4.1/vcorelib/asyncio/__init__.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/asyncio/cli.py` & `vcorelib-2.4.1/vcorelib/asyncio/cli.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/asyncio/subprocess.py` & `vcorelib-2.4.1/vcorelib/asyncio/subprocess.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/dict/__init__.py` & `vcorelib-2.4.1/vcorelib/dict/__init__.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/dict/cache.py` & `vcorelib-2.4.1/vcorelib/dict/cache.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/dict/codec.py` & `vcorelib-2.4.1/vcorelib/dict/codec.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/dict/config.py` & `vcorelib-2.4.1/vcorelib/dict/config.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/dict/env.py` & `vcorelib-2.4.1/vcorelib/dict/env.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/graph/__init__.py` & `vcorelib-2.4.1/vcorelib/graph/__init__.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/graph/abc.py` & `vcorelib-2.4.1/vcorelib/graph/abc.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/graph/edge.py` & `vcorelib-2.4.1/vcorelib/graph/edge.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/graph/node.py` & `vcorelib-2.4.1/vcorelib/graph/node.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/graph/port.py` & `vcorelib-2.4.1/vcorelib/graph/port.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/io/__init__.py` & `vcorelib-2.4.1/vcorelib/io/__init__.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/io/abc.py` & `vcorelib-2.4.1/vcorelib/io/abc.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/io/arbiter/base.py` & `vcorelib-2.4.1/vcorelib/io/arbiter/base.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/io/arbiter/context.py` & `vcorelib-2.4.1/vcorelib/io/arbiter/context.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/io/arbiter/directory.py` & `vcorelib-2.4.1/vcorelib/io/arbiter/directory.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/io/archive/__init__.py` & `vcorelib-2.4.1/vcorelib/io/archive/__init__.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/io/cache.py` & `vcorelib-2.4.1/vcorelib/io/cache.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/io/decode.py` & `vcorelib-2.4.1/vcorelib/io/decode.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/io/encode.py` & `vcorelib-2.4.1/vcorelib/io/encode.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/io/mapping.py` & `vcorelib-2.4.1/vcorelib/io/mapping.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/io/types.py` & `vcorelib-2.4.1/vcorelib/io/types.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/logging.py` & `vcorelib-2.4.1/vcorelib/logging.py`

 * *Files 3% similar despite different names*

```diff
@@ -33,20 +33,25 @@
 
 
 class LoggerMixin:  # pylint: disable=too-few-public-methods
     """A class that provides an inheriting class a logger attribute."""
 
     logger: LoggerType
 
-    def __init__(self, logger: LoggerType = None) -> None:
+    def __init__(
+        self, logger: LoggerType = None, logger_name: str = None
+    ) -> None:
         """Initialize this object with logging capabilities."""
+
         if not hasattr(self, "logger"):
             # Set a logger for this class instance.
             if logger is None:
-                logger = _GetLogger(self.__class__.__module__)
+                if logger_name is None:
+                    logger_name = self.__class__.__module__
+                logger = _GetLogger(logger_name)
             self.logger = logger
 
     @contextmanager
     def log_time(
         self,
         message: str,
         *args,
```

### Comparing `vcorelib-2.4.0/vcorelib/math/__init__.py` & `vcorelib-2.4.1/vcorelib/math/__init__.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/math/analysis/__init__.py` & `vcorelib-2.4.1/vcorelib/math/analysis/__init__.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/math/analysis/average.py` & `vcorelib-2.4.1/vcorelib/math/analysis/average.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/math/analysis/buffer.py` & `vcorelib-2.4.1/vcorelib/math/analysis/buffer.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/math/analysis/rate/__init__.py` & `vcorelib-2.4.1/vcorelib/math/analysis/rate/__init__.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/math/analysis/rate/limiter.py` & `vcorelib-2.4.1/vcorelib/math/analysis/rate/limiter.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/math/analysis/weighted.py` & `vcorelib-2.4.1/vcorelib/math/analysis/weighted.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/math/time.py` & `vcorelib-2.4.1/vcorelib/math/time.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/math/unit.py` & `vcorelib-2.4.1/vcorelib/math/unit.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/names.py` & `vcorelib-2.4.1/vcorelib/names.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/namespace.py` & `vcorelib-2.4.1/vcorelib/namespace.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/paths/__init__.py` & `vcorelib-2.4.1/vcorelib/paths/__init__.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/paths/base.py` & `vcorelib-2.4.1/vcorelib/paths/base.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/paths/context.py` & `vcorelib-2.4.1/vcorelib/paths/context.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/paths/hashing.py` & `vcorelib-2.4.1/vcorelib/paths/hashing.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/paths/info.py` & `vcorelib-2.4.1/vcorelib/paths/info.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/paths/info_cache.py` & `vcorelib-2.4.1/vcorelib/paths/info_cache.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/platform/__init__.py` & `vcorelib-2.4.1/vcorelib/platform/__init__.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/python.py` & `vcorelib-2.4.1/vcorelib/python.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/schemas/__init__.py` & `vcorelib-2.4.1/vcorelib/schemas/__init__.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/schemas/base.py` & `vcorelib-2.4.1/vcorelib/schemas/base.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/schemas/json.py` & `vcorelib-2.4.1/vcorelib/schemas/json.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/schemas/mixins.py` & `vcorelib-2.4.1/vcorelib/schemas/mixins.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/script/__init__.py` & `vcorelib-2.4.1/vcorelib/script/__init__.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/target/__init__.py` & `vcorelib-2.4.1/vcorelib/target/__init__.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/target/evaluation.py` & `vcorelib-2.4.1/vcorelib/target/evaluation.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/target/expression.py` & `vcorelib-2.4.1/vcorelib/target/expression.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/target/resolver.py` & `vcorelib-2.4.1/vcorelib/target/resolver.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/task/__init__.py` & `vcorelib-2.4.1/vcorelib/task/__init__.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/task/dict/melder.py` & `vcorelib-2.4.1/vcorelib/task/dict/melder.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/task/manager.py` & `vcorelib-2.4.1/vcorelib/task/manager.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/task/subprocess/run.py` & `vcorelib-2.4.1/vcorelib/task/subprocess/run.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib/task/time/sleep.py` & `vcorelib-2.4.1/vcorelib/task/time/sleep.py`

 * *Files identical despite different names*

### Comparing `vcorelib-2.4.0/vcorelib.egg-info/PKG-INFO` & `vcorelib-2.4.1/vcorelib.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: vcorelib
-Version: 2.4.0
+Version: 2.4.1
 Summary: A collection of core Python utilities.
 Home-page: https://github.com/vkottler/vcorelib
 Author: Vaughn Kottler
 Author-email: Vaughn Kottler <vaughnkottler@gmail.com>
 Maintainer-email: Vaughn Kottler <vaughnkottler@gmail.com>
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
@@ -21,19 +21,19 @@
 Provides-Extra: test
 License-File: LICENSE
 
 <!--
     =====================================
     generator=datazen
     version=3.1.2
-    hash=10535d341384b031fe2481a3715c8a79
+    hash=3e8288e50ab8a440ea21e053b4ff1b6a
     =====================================
 -->
 
-# vcorelib ([2.4.0](https://pypi.org/project/vcorelib/))
+# vcorelib ([2.4.1](https://pypi.org/project/vcorelib/))
 
 [![python](https://img.shields.io/pypi/pyversions/vcorelib.svg)](https://pypi.org/project/vcorelib/)
 ![Build Status](https://github.com/vkottler/vcorelib/workflows/Python%20Package/badge.svg)
 [![codecov](https://codecov.io/gh/vkottler/vcorelib/branch/master/graphs/badge.svg?branch=master)](https://codecov.io/github/vkottler/vcorelib)
 ![PyPI - Status](https://img.shields.io/pypi/status/vcorelib)
 ![Dependents (via libraries.io)](https://img.shields.io/librariesio/dependents/pypi/vcorelib)
```

### Comparing `vcorelib-2.4.0/vcorelib.egg-info/SOURCES.txt` & `vcorelib-2.4.1/vcorelib.egg-info/SOURCES.txt`

 * *Files identical despite different names*

