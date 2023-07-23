# Comparing `tmp/pydiverse_pipedag-0.6.1.tar.gz` & `tmp/pydiverse_pipedag-0.6.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pydiverse_pipedag-0.6.1.tar", max compression
+gzip compressed data, was "pydiverse_pipedag-0.6.2.tar", max compression
```

## Comparing `pydiverse_pipedag-0.6.1.tar` & `pydiverse_pipedag-0.6.2.tar`

### file list

```diff
@@ -1,69 +1,69 @@
--rw-r--r--   0        0        0     1517 2023-07-19 12:57:39.012456 pydiverse_pipedag-0.6.1/LICENSE
--rw-r--r--   0        0        0     6174 2023-07-19 12:57:39.012456 pydiverse_pipedag-0.6.1/docs/package/README.md
--rw-r--r--   0        0        0     3421 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/pyproject.toml
--rw-r--r--   0        0        0       13 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/.gitignore
--rw-r--r--   0        0        0      435 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/__init__.py
--rw-r--r--   0        0        0      857 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/_typing.py
--rw-r--r--   0        0        0       97 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/__init__.py
--rw-r--r--   0        0        0     5348 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/blob.py
--rw-r--r--   0        0        0      393 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/lock/__init__.py
--rw-r--r--   0        0        0     6097 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/lock/base.py
--rw-r--r--   0        0        0    13555 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/lock/database.py
--rw-r--r--   0        0        0     2756 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/lock/filelock.py
--rw-r--r--   0        0        0      769 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/lock/nolock.py
--rw-r--r--   0        0        0     3983 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/lock/zookeeper.py
--rw-r--r--   0        0        0      233 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/table/__init__.py
--rw-r--r--   0        0        0    23394 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/table/base.py
--rw-r--r--   0        0        0      108 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/table/cache/__init__.py
--rw-r--r--   0        0        0     3106 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/table/cache/base.py
--rw-r--r--   0        0        0     6976 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/table/cache/parquet.py
--rw-r--r--   0        0        0     6933 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/table/dict.py
--rw-r--r--   0        0        0      141 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/table/sql/__init__.py
--rw-r--r--   0        0        0    37136 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/table/sql/ddl.py
--rw-r--r--   0        0        0      187 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/table/sql/dialects/__init__.py
--rw-r--r--   0        0        0     1508 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/table/sql/dialects/duckdb.py
--rw-r--r--   0        0        0     3301 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/table/sql/dialects/ibm_db2.py
--rw-r--r--   0        0        0     9235 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/table/sql/dialects/mssql.py
--rw-r--r--   0        0        0     3956 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/table/sql/dialects/postgres.py
--rw-r--r--   0        0        0    21371 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/table/sql/hooks.py
--rw-r--r--   0        0        0     4250 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/table/sql/reflection.py
--rw-r--r--   0        0        0    47185 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/table/sql/sql.py
--rw-r--r--   0        0        0       81 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/table/util/__init__.py
--rw-r--r--   0        0        0     8579 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/table/util/dtype.py
--rw-r--r--   0        0        0      433 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/context/__init__.py
--rw-r--r--   0        0        0     9874 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/context/context.py
--rw-r--r--   0        0        0    26325 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/context/run_context.py
--rw-r--r--   0        0        0      311 2023-07-19 12:57:39.016456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/core/__init__.py
--rw-r--r--   0        0        0    14956 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/core/config.py
--rw-r--r--   0        0        0    20430 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/core/flow.py
--rw-r--r--   0        0        0     4294 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/core/result.py
--rw-r--r--   0        0        0     7789 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/core/stage.py
--rw-r--r--   0        0        0     8013 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/core/task.py
--rw-r--r--   0        0        0      368 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/engine/__init__.py
--rw-r--r--   0        0        0      654 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/engine/base.py
--rw-r--r--   0        0        0     3133 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/engine/dask.py
--rw-r--r--   0        0        0     7269 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/engine/prefect.py
--rw-r--r--   0        0        0     1388 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/engine/sequential.py
--rw-r--r--   0        0        0     1079 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/errors/__init__.py
--rw-r--r--   0        0        0        0 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/management/__init__.py
--rw-r--r--   0        0        0      620 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/management/cli.py
--rw-r--r--   0        0        0        0 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/management/commands/__init__.py
--rw-r--r--   0        0        0     1741 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/management/commands/clear_metadata.py
--rw-r--r--   0        0        0     2744 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/management/commands/delete_schemas.py
--rw-r--r--   0        0        0      182 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/materialize/__init__.py
--rw-r--r--   0        0        0     9114 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/materialize/cache.py
--rw-r--r--   0        0        0    11091 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/materialize/container.py
--rw-r--r--   0        0        0    17639 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/materialize/core.py
--rw-r--r--   0        0        0     2074 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/materialize/metadata.py
--rw-r--r--   0        0        0    19431 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/materialize/store.py
--rw-r--r--   0        0        0      213 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/util/__init__.py
--rw-r--r--   0        0        0     2061 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/util/deep_map.py
--rw-r--r--   0        0        0     1435 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/util/deep_merge.py
--rw-r--r--   0        0        0      944 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/util/disposable.py
--rw-r--r--   0        0        0     1129 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/util/hashing.py
--rw-r--r--   0        0        0     3736 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/util/import_.py
--rw-r--r--   0        0        0     7992 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/util/ipc.py
--rw-r--r--   0        0        0     4400 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/util/json.py
--rw-r--r--   0        0        0     1377 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/util/naming.py
--rw-r--r--   0        0        0     2847 2023-07-19 12:57:39.020456 pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/util/structlog.py
--rw-r--r--   0        0        0     7911 1970-01-01 00:00:00.000000 pydiverse_pipedag-0.6.1/PKG-INFO
+-rw-r--r--   0        0        0     1517 2023-07-23 10:05:29.268867 pydiverse_pipedag-0.6.2/LICENSE
+-rw-r--r--   0        0        0     6174 2023-07-23 10:05:29.268867 pydiverse_pipedag-0.6.2/docs/package/README.md
+-rw-r--r--   0        0        0     3421 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/pyproject.toml
+-rw-r--r--   0        0        0       13 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/.gitignore
+-rw-r--r--   0        0        0      435 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/__init__.py
+-rw-r--r--   0        0        0      857 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/_typing.py
+-rw-r--r--   0        0        0       97 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/__init__.py
+-rw-r--r--   0        0        0     5348 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/blob.py
+-rw-r--r--   0        0        0      393 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/lock/__init__.py
+-rw-r--r--   0        0        0     6097 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/lock/base.py
+-rw-r--r--   0        0        0    13555 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/lock/database.py
+-rw-r--r--   0        0        0     2756 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/lock/filelock.py
+-rw-r--r--   0        0        0      769 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/lock/nolock.py
+-rw-r--r--   0        0        0     3983 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/lock/zookeeper.py
+-rw-r--r--   0        0        0      233 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/table/__init__.py
+-rw-r--r--   0        0        0    23394 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/table/base.py
+-rw-r--r--   0        0        0      108 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/table/cache/__init__.py
+-rw-r--r--   0        0        0     3106 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/table/cache/base.py
+-rw-r--r--   0        0        0     6976 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/table/cache/parquet.py
+-rw-r--r--   0        0        0     6933 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/table/dict.py
+-rw-r--r--   0        0        0      141 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/table/sql/__init__.py
+-rw-r--r--   0        0        0    36934 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/table/sql/ddl.py
+-rw-r--r--   0        0        0      187 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/table/sql/dialects/__init__.py
+-rw-r--r--   0        0        0     1508 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/table/sql/dialects/duckdb.py
+-rw-r--r--   0        0        0     3301 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/table/sql/dialects/ibm_db2.py
+-rw-r--r--   0        0        0     9235 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/table/sql/dialects/mssql.py
+-rw-r--r--   0        0        0     3956 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/table/sql/dialects/postgres.py
+-rw-r--r--   0        0        0    21490 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/table/sql/hooks.py
+-rw-r--r--   0        0        0     4250 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/table/sql/reflection.py
+-rw-r--r--   0        0        0    47189 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/table/sql/sql.py
+-rw-r--r--   0        0        0       81 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/table/util/__init__.py
+-rw-r--r--   0        0        0     8579 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/table/util/dtype.py
+-rw-r--r--   0        0        0      433 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/context/__init__.py
+-rw-r--r--   0        0        0     9874 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/context/context.py
+-rw-r--r--   0        0        0    26325 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/context/run_context.py
+-rw-r--r--   0        0        0      311 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/core/__init__.py
+-rw-r--r--   0        0        0    14956 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/core/config.py
+-rw-r--r--   0        0        0    20430 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/core/flow.py
+-rw-r--r--   0        0        0     4294 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/core/result.py
+-rw-r--r--   0        0        0     7789 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/core/stage.py
+-rw-r--r--   0        0        0     8013 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/core/task.py
+-rw-r--r--   0        0        0      368 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/engine/__init__.py
+-rw-r--r--   0        0        0      654 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/engine/base.py
+-rw-r--r--   0        0        0     3133 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/engine/dask.py
+-rw-r--r--   0        0        0     7269 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/engine/prefect.py
+-rw-r--r--   0        0        0     1388 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/engine/sequential.py
+-rw-r--r--   0        0        0     1079 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/errors/__init__.py
+-rw-r--r--   0        0        0        0 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/management/__init__.py
+-rw-r--r--   0        0        0      620 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/management/cli.py
+-rw-r--r--   0        0        0        0 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/management/commands/__init__.py
+-rw-r--r--   0        0        0     1741 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/management/commands/clear_metadata.py
+-rw-r--r--   0        0        0     2744 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/management/commands/delete_schemas.py
+-rw-r--r--   0        0        0      182 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/materialize/__init__.py
+-rw-r--r--   0        0        0     9114 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/materialize/cache.py
+-rw-r--r--   0        0        0    11091 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/materialize/container.py
+-rw-r--r--   0        0        0    17639 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/materialize/core.py
+-rw-r--r--   0        0        0     2074 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/materialize/metadata.py
+-rw-r--r--   0        0        0    19431 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/materialize/store.py
+-rw-r--r--   0        0        0      213 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/util/__init__.py
+-rw-r--r--   0        0        0     2061 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/util/deep_map.py
+-rw-r--r--   0        0        0     1435 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/util/deep_merge.py
+-rw-r--r--   0        0        0      944 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/util/disposable.py
+-rw-r--r--   0        0        0     1129 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/util/hashing.py
+-rw-r--r--   0        0        0     3736 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/util/import_.py
+-rw-r--r--   0        0        0     7992 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/util/ipc.py
+-rw-r--r--   0        0        0     4400 2023-07-23 10:05:29.272867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/util/json.py
+-rw-r--r--   0        0        0     1377 2023-07-23 10:05:29.276867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/util/naming.py
+-rw-r--r--   0        0        0     2847 2023-07-23 10:05:29.276867 pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/util/structlog.py
+-rw-r--r--   0        0        0     7911 1970-01-01 00:00:00.000000 pydiverse_pipedag-0.6.2/PKG-INFO
```

### Comparing `pydiverse_pipedag-0.6.1/LICENSE` & `pydiverse_pipedag-0.6.2/LICENSE`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/docs/package/README.md` & `pydiverse_pipedag-0.6.2/docs/package/README.md`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/pyproject.toml` & `pydiverse_pipedag-0.6.2/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "pydiverse-pipedag"
-version = "0.6.1"
+version = "0.6.2"
 description = "A pipeline orchestration library executing tasks within one python session. It takes care of SQL table (de)materialization, caching and cache invalidation. Blob storage is supported as well for example for storing model files."
 authors = [
   "QuantCo, Inc.",
   "Nicolas Camenisch <garnele007@gmail.com>",
   "Martin Trautmann <windiana@users.sf.net>",
 ]
 license = "BSD-3-Clause"
```

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/_typing.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/_typing.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/blob.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/blob.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/lock/base.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/lock/base.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/lock/database.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/lock/database.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/lock/filelock.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/lock/filelock.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/lock/nolock.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/lock/nolock.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/lock/zookeeper.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/lock/zookeeper.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/table/base.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/table/base.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/table/cache/base.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/table/cache/base.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/table/cache/parquet.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/table/cache/parquet.py`

 * *Files 2% similar despite different names*

```diff
@@ -114,15 +114,15 @@
     ) -> pd.DataFrame:
         if PandasTableHook.pd_version < Version("2.0"):
             return cls._retrieve(store, table, use_nullable_dtype=True)
 
         # Determine dtype backend for pandas >= 2.0
         # [this is similar to the PandasTableHook found in SQLTableStore]
 
-        backend_str = "arrow"
+        backend_str = "numpy"
         if hook_args := ConfigContext.get().table_hook_args.get("pandas", None):
             if dtype_backend := hook_args.get("dtype_backend", None):
                 backend_str = dtype_backend
 
         if isinstance(as_type, tuple):
             backend_str = as_type[1]
         elif isinstance(as_type, dict):
```

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/table/dict.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/table/dict.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/table/sql/ddl.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/table/sql/ddl.py`

 * *Files 2% similar despite different names*

```diff
@@ -232,29 +232,43 @@
         schema: Schema,
         key_columns: list[str],
         name: str | None = None,
     ):
         self.table_name = table_name
         self.schema = schema
         self.key = key_columns
-        self.name = name
+        self._name = name
+
+    @property
+    def name(self) -> str:
+        if self._name:
+            return self._name
+        columns = "_".join(c.lower() for c in self.key)
+        return "pk_" + columns + "_" + self.table_name.lower()
 
 
 class AddIndex(DDLElement):
     def __init__(
         self,
         table_name: str,
         schema: Schema,
         index_columns: list[str],
         name: str | None = None,
     ):
         self.table_name = table_name
         self.schema = schema
         self.index = index_columns
-        self.name = name
+        self._name = name
+
+    @property
+    def name(self) -> str:
+        if self._name:
+            return self._name
+        columns = "_".join(c.lower() for c in self.index)
+        return "idx_" + columns + "_" + self.table_name.lower()
 
 
 class ChangeColumnTypes(DDLElement):
     def __init__(
         self,
         table_name: str,
         schema: Schema,
@@ -316,15 +330,14 @@
     text = ["CREATE SCHEMA"]
     if create.if_not_exists:
         text.append("IF NOT EXISTS")
     text.append(schema)
     return " ".join(text)
 
 
-# noinspection SqlDialectInspection
 @compiles(CreateSchema, "mssql")
 def visit_create_schema_mssql(create: CreateSchema, compiler, **kw):
     _ = kw
     schema = compiler.preparer.format_schema(create.schema.get())
     if create.if_not_exists:
         unquoted_schema = create.schema.get()
         return f"""
@@ -620,15 +633,14 @@
 
     kw["literal_binds"] = True
     select = compiler.sql_compiler.process(create.query, **kw)
 
     return insert_into_in_query(select, schema, name)
 
 
-# noinspection SqlDialectInspection
 @compiles(CreateTableAsSelect, "ibm_db_sa")
 def visit_create_table_as_select_ibm_db_sa(create: CreateTableAsSelect, compiler, **kw):
     prepare_statement = _visit_create_obj_as_select(
         create, compiler, "TABLE", kw, prefix="(", suffix=") DEFINITION ONLY"
     )
 
     if create.early_not_null is not None:
@@ -762,37 +774,34 @@
         source_tables=[
             dict(name=copy_table.from_name, schema=copy_table.from_schema.get())
         ],
     )
     return compiler.process(create, **kw)
 
 
-# noinspection SqlDialectInspection
 @compiles(RenameTable)
 def visit_rename_table(rename_table: RenameTable, compiler, **kw):
     _ = kw
     from_table = compiler.preparer.quote(rename_table.from_name)
     to_table = compiler.preparer.quote(rename_table.to_name)
     schema = compiler.preparer.format_schema(rename_table.schema.get())
     return f"ALTER TABLE {schema}.{from_table} RENAME TO {to_table}"
 
 
-# noinspection SqlDialectInspection
 @compiles(RenameTable, "mssql")
 def visit_rename_table(rename_table: RenameTable, compiler, **kw):
     _ = kw
 
     schema = compiler.preparer.format_schema(rename_table.schema.get())
     from_table = compiler.preparer.quote(rename_table.from_name)
     to_table = rename_table.to_name  # no quoting is intentional
 
     return f"EXEC sp_rename '{schema}.{from_table}', '{to_table}'"
 
 
-# noinspection SqlDialectInspection
 @compiles(RenameTable, "ibm_db_sa")
 def visit_rename_table(rename_table: RenameTable, compiler, **kw):
     _ = kw
     from_table = compiler.preparer.quote(rename_table.from_name)
     to_table = compiler.preparer.quote(rename_table.to_name)
     schema = compiler.preparer.format_schema(rename_table.schema.get())
     return f"RENAME TABLE {schema}.{from_table} TO {to_table}"
@@ -848,69 +857,54 @@
     text = [f"DROP {_type}"]
     if drop.if_exists:
         text.append("IF EXISTS")
     text.append(f"{schema}.{table}")
     return " ".join(text)
 
 
-# noinspection SqlDialectInspection
 @compiles(AddPrimaryKey)
 def visit_add_primary_key(add_primary_key: AddPrimaryKey, compiler, **kw):
     _ = kw
     table = compiler.preparer.quote(add_primary_key.table_name)
     schema = compiler.preparer.format_schema(add_primary_key.schema.get())
-    pk_name = compiler.preparer.quote(
-        add_primary_key.name
-        if add_primary_key.name is not None
-        else "pk_"
-        + "_".join([c.lower() for c in add_primary_key.key])
-        + "_"
-        + add_primary_key.table_name.lower()
-    )
+    pk_name = compiler.preparer.quote(add_primary_key.name)
     cols = ",".join([compiler.preparer.quote(col) for col in add_primary_key.key])
     return f"ALTER TABLE {schema}.{table} ADD CONSTRAINT {pk_name} PRIMARY KEY ({cols})"
 
 
-# noinspection SqlDialectInspection
 @compiles(AddPrimaryKey, "duckdb")
 def visit_add_primary_key(add_primary_key: AddPrimaryKey, compiler, **kw):
     _ = kw
     table = compiler.preparer.quote(add_primary_key.table_name)
     schema = compiler.preparer.format_schema(add_primary_key.schema.get())
-    pk_name = compiler.preparer.quote(
-        add_primary_key.name
-        if add_primary_key.name is not None
-        else "pk_"
-        + "_".join([c.lower() for c in add_primary_key.key])
-        + "_"
-        + add_primary_key.table_name.lower()
-    )
+    pk_name = compiler.preparer.quote(add_primary_key.name)
     cols = ",".join([compiler.preparer.quote(col) for col in add_primary_key.key])
     return f"CREATE UNIQUE INDEX {pk_name} ON {schema}.{table} ({cols})"
 
 
-# noinspection SqlDialectInspection
 @compiles(AddIndex)
 def visit_add_index(add_index: AddIndex, compiler, **kw):
     _ = kw
     table = compiler.preparer.quote(add_index.table_name)
     schema = compiler.preparer.format_schema(add_index.schema.get())
-    index_name = compiler.preparer.quote(
-        add_index.name
-        if add_index.name is not None
-        else "idx_"
-        + "_".join([c.lower() for c in add_index.index])
-        + "_"
-        + add_index.table_name.lower()
-    )
+    index_name = compiler.preparer.quote(add_index.name)
     cols = ",".join([compiler.preparer.quote(col) for col in add_index.index])
     return f"CREATE INDEX {index_name} ON {schema}.{table} ({cols})"
 
 
-# noinspection SqlDialectInspection
+@compiles(AddIndex, "ibm_db_sa")
+def visit_add_index(add_index: AddIndex, compiler, **kw):
+    _ = kw
+    table = compiler.preparer.quote(add_index.table_name)
+    schema = compiler.preparer.format_schema(add_index.schema.get())
+    index_name = compiler.preparer.quote(add_index.name)
+    cols = ",".join([compiler.preparer.quote(col) for col in add_index.index])
+    return f"CREATE INDEX {schema}.{index_name} ON {schema}.{table} ({cols})"
+
+
 @compiles(ChangeColumnTypes)
 def visit_change_column_types(change: ChangeColumnTypes, compiler, **kw):
     _ = kw
     table = compiler.preparer.quote(change.table_name)
     schema = compiler.preparer.format_schema(change.schema.get())
     alter_columns = ",".join(
         [
@@ -927,15 +921,14 @@
             for col, nullable in zip(change.column_names, change.nullable)
             if nullable is not None
         ]
     )
     return f"ALTER TABLE {schema}.{table} {alter_columns}"
 
 
-# noinspection SqlDialectInspection
 @compiles(ChangeColumnTypes, "duckdb")
 def visit_change_column_types_duckdb(change: ChangeColumnTypes, compiler, **kw):
     table = compiler.preparer.quote(change.table_name)
     schema = compiler.preparer.format_schema(change.schema.get())
     alter_columns = [
         f"ALTER COLUMN {compiler.preparer.quote(col)} SET DATA TYPE"
         f" {compiler.type_compiler.process(_type)}"
@@ -951,15 +944,14 @@
     ]
     statements = [
         f"ALTER TABLE {schema}.{table} {statement}" for statement in alter_columns
     ]
     return join_ddl_statements(statements, compiler, **kw)
 
 
-# noinspection SqlDialectInspection
 @compiles(ChangeColumnTypes, "mssql")
 def visit_change_column_types(change: ChangeColumnTypes, compiler, **kw):
     _ = kw
 
     table = compiler.preparer.quote(change.table_name)
     schema = compiler.preparer.format_schema(change.schema.get())
 
@@ -981,15 +973,14 @@
         for col, _type, nullable in zip(
             change.column_names, change.column_types, change.nullable
         )
     ]
     return join_ddl_statements(statements, compiler, **kw)
 
 
-# noinspection SqlDialectInspection
 @compiles(ChangeColumnTypes, "ibm_db_sa")
 def visit_change_column_types(change: ChangeColumnTypes, compiler, **kw):
     _ = kw
 
     def modify_type(_type):
         if change.cap_varchar_max is not None:
             _type = copy.copy(_type)
@@ -1016,15 +1007,14 @@
         for col, nullable in zip(change.column_names, change.nullable)
         if nullable is not None
     ]
     statements.append(f"call sysproc.admin_cmd('REORG TABLE {schema}.{table}')")
     return join_ddl_statements(statements, compiler, **kw)
 
 
-# noinspection SqlDialectInspection
 @compiles(ChangeColumnNullable)
 def visit_change_column_nullable(change: ChangeColumnNullable, compiler, **kw):
     _ = kw
     table = compiler.preparer.quote(change.table_name)
     schema = compiler.preparer.format_schema(change.schema.get())
     alter_columns = ",".join(
         [
@@ -1033,15 +1023,14 @@
             f" {'SET' if not nullable else 'DROP'} NOT NULL"
             for col, nullable in zip(change.column_names, change.nullable)
         ]
     )
     return f"ALTER TABLE {schema}.{table} {alter_columns}"
 
 
-# noinspection SqlDialectInspection
 @compiles(ChangeColumnNullable, "ibm_db_sa")
 def visit_change_column_nullable(change: ChangeColumnNullable, compiler, **kw):
     _ = kw
     statements = _get_nullable_change_statements(change, compiler)
     return join_ddl_statements(statements, compiler, **kw)
```

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/table/sql/dialects/duckdb.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/table/sql/dialects/duckdb.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/table/sql/dialects/ibm_db2.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/table/sql/dialects/ibm_db2.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/table/sql/dialects/mssql.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/table/sql/dialects/mssql.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/table/sql/dialects/postgres.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/table/sql/dialects/postgres.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/table/sql/hooks.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/table/sql/hooks.py`

 * *Files 0% similar despite different names*

```diff
@@ -267,15 +267,17 @@
         store: SQLTableStore,
         table: Table,
         stage_name: str,
         as_type: type[pd.DataFrame] | tuple | dict,
     ) -> pd.DataFrame:
         # Config
         if PandasTableHook.pd_version >= Version("2.0"):
-            backend_str = "arrow"
+            # Once arrow is mature enough, we might want to switch to
+            # arrow backed dataframes by default
+            backend_str = "numpy"
         else:
             backend_str = "numpy"
 
         if hook_args := ConfigContext.get().table_hook_args.get("pandas", None):
             if dtype_backend := hook_args.get("dtype_backend", None):
                 backend_str = dtype_backend
```

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/table/sql/reflection.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/table/sql/reflection.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/table/sql/sql.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/table/sql/sql.py`

 * *Files 0% similar despite different names*

```diff
@@ -1164,16 +1164,16 @@
             )
         with self.engine_connect() as conn:
             result = conn.execute(
                 sa.select(self.tasks_table.c.output_json)
                 .where(self.tasks_table.c.stage == stage.name)
                 .where(self.tasks_table.c.in_transaction_schema.in_([False]))
             ).scalars()
+            result = sorted(result)
 
-        result = sorted(result)
         return stable_hash(*result)
 
     # DatabaseLockManager
 
     def get_engine_for_locking(self) -> sa.Engine:
         return self._create_engine()
```

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/backend/table/util/dtype.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/backend/table/util/dtype.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/context/context.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/context/context.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/context/run_context.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/context/run_context.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/core/config.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/core/config.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/core/flow.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/core/flow.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/core/result.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/core/result.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/core/stage.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/core/stage.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/core/task.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/core/task.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/engine/base.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/engine/base.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/engine/dask.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/engine/dask.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/engine/prefect.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/engine/prefect.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/engine/sequential.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/engine/sequential.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/errors/__init__.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/errors/__init__.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/management/cli.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/management/cli.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/management/commands/clear_metadata.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/management/commands/clear_metadata.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/management/commands/delete_schemas.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/management/commands/delete_schemas.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/materialize/cache.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/materialize/cache.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/materialize/container.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/materialize/container.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/materialize/core.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/materialize/core.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/materialize/metadata.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/materialize/metadata.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/materialize/store.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/materialize/store.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/util/deep_map.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/util/deep_map.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/util/deep_merge.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/util/deep_merge.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/util/disposable.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/util/disposable.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/util/hashing.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/util/hashing.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/util/import_.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/util/import_.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/util/ipc.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/util/ipc.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/util/json.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/util/json.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/util/naming.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/util/naming.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/src/pydiverse/pipedag/util/structlog.py` & `pydiverse_pipedag-0.6.2/src/pydiverse/pipedag/util/structlog.py`

 * *Files identical despite different names*

### Comparing `pydiverse_pipedag-0.6.1/PKG-INFO` & `pydiverse_pipedag-0.6.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pydiverse-pipedag
-Version: 0.6.1
+Version: 0.6.2
 Summary: A pipeline orchestration library executing tasks within one python session. It takes care of SQL table (de)materialization, caching and cache invalidation. Blob storage is supported as well for example for storing model files.
 License: BSD-3-Clause
 Author: QuantCo, Inc.
 Requires-Python: >=3.9,<4.0
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
 Classifier: Intended Audience :: Science/Research
```

