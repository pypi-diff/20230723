# Comparing `tmp/clean-python-0.1.0.tar.gz` & `tmp/clean-python-0.2.0b0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "clean-python-0.1.0.tar", last modified: Wed Jul 12 12:32:00 2023, max compression
+gzip compressed data, was "clean-python-0.2.0b0.tar", last modified: Sun Jul 23 06:14:06 2023, max compression
```

## Comparing `clean-python-0.1.0.tar` & `clean-python-0.2.0b0.tar`

### file list

```diff
@@ -1,92 +1,92 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-12 12:32:00.610202 clean-python-0.1.0/
--rw-r--r--   0 runner    (1001) docker     (123)      259 2023-07-12 12:31:49.000000 clean-python-0.1.0/CHANGES.md
--rw-r--r--   0 runner    (1001) docker     (123)     1103 2023-07-12 12:31:49.000000 clean-python-0.1.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      137 2023-07-12 12:31:49.000000 clean-python-0.1.0/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     6945 2023-07-12 12:32:00.610202 clean-python-0.1.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     6429 2023-07-12 12:31:49.000000 clean-python-0.1.0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-12 12:32:00.602202 clean-python-0.1.0/clean_python/
--rw-r--r--   0 runner    (1001) docker     (123)       98 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-12 12:32:00.602202 clean-python-0.1.0/clean_python/base/
--rw-r--r--   0 runner    (1001) docker     (123)      139 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/base/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-12 12:32:00.602202 clean-python-0.1.0/clean_python/base/application/
--rw-r--r--   0 runner    (1001) docker     (123)       30 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/base/application/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1991 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/base/application/manage.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-12 12:32:00.602202 clean-python-0.1.0/clean_python/base/domain/
--rw-r--r--   0 runner    (1001) docker     (123)      365 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/base/domain/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      645 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/base/domain/domain_event.py
--rw-r--r--   0 runner    (1001) docker     (123)      208 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/base/domain/domain_service.py
--rw-r--r--   0 runner    (1001) docker     (123)     2077 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/base/domain/exceptions.py
--rw-r--r--   0 runner    (1001) docker     (123)      200 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/base/domain/filter.py
--rw-r--r--   0 runner    (1001) docker     (123)     1719 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/base/domain/gateway.py
--rw-r--r--   0 runner    (1001) docker     (123)      117 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/base/domain/json.py
--rw-r--r--   0 runner    (1001) docker     (123)      526 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/base/domain/pagination.py
--rw-r--r--   0 runner    (1001) docker     (123)     3035 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/base/domain/repository.py
--rw-r--r--   0 runner    (1001) docker     (123)     1147 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/base/domain/root_entity.py
--rw-r--r--   0 runner    (1001) docker     (123)      220 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/base/domain/value.py
--rw-r--r--   0 runner    (1001) docker     (123)     1319 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/base/domain/value_object.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-12 12:32:00.606202 clean-python-0.1.0/clean_python/base/infrastructure/
--rw-r--r--   0 runner    (1001) docker     (123)      120 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/base/infrastructure/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2542 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/base/infrastructure/in_memory_gateway.py
--rw-r--r--   0 runner    (1001) docker     (123)     1865 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/base/infrastructure/internal_gateway.py
--rw-r--r--   0 runner    (1001) docker     (123)      317 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/base/infrastructure/tmpdir_provider.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-12 12:32:00.606202 clean-python-0.1.0/clean_python/base/presentation/
--rw-r--r--   0 runner    (1001) docker     (123)       28 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/base/presentation/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      154 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/base/presentation/link.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-12 12:32:00.606202 clean-python-0.1.0/clean_python/celery/
--rw-r--r--   0 runner    (1001) docker     (123)       41 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/celery/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2169 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/celery/celery_rmq_broker.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-12 12:32:00.606202 clean-python-0.1.0/clean_python/dramatiq/
--rw-r--r--   0 runner    (1001) docker     (123)      113 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/dramatiq/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6049 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/dramatiq/async_actor.py
--rw-r--r--   0 runner    (1001) docker     (123)     2582 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/dramatiq/dramatiq_task_logger.py
--rw-r--r--   0 runner    (1001) docker     (123)      687 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/dramatiq/sleep_task.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-12 12:32:00.606202 clean-python-0.1.0/clean_python/fastapi/
--rw-r--r--   0 runner    (1001) docker     (123)      215 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/fastapi/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1140 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/fastapi/context.py
--rw-r--r--   0 runner    (1001) docker     (123)     2173 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/fastapi/error_responses.py
--rw-r--r--   0 runner    (1001) docker     (123)     2670 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/fastapi/fastapi_access_logger.py
--rw-r--r--   0 runner    (1001) docker     (123)     1613 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/fastapi/request_query.py
--rw-r--r--   0 runner    (1001) docker     (123)     6438 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/fastapi/resource.py
--rw-r--r--   0 runner    (1001) docker     (123)     6572 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/fastapi/service.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-12 12:32:00.606202 clean-python-0.1.0/clean_python/fluentbit/
--rw-r--r--   0 runner    (1001) docker     (123)       41 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/fluentbit/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      493 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/fluentbit/fluentbit_gateway.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-12 12:32:00.606202 clean-python-0.1.0/clean_python/oauth2/
--rw-r--r--   0 runner    (1001) docker     (123)       30 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/oauth2/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3828 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/oauth2/oauth2.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-12 12:32:00.606202 clean-python-0.1.0/clean_python/sql/
--rw-r--r--   0 runner    (1001) docker     (123)       71 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/sql/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    11528 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/sql/sql_gateway.py
--rw-r--r--   0 runner    (1001) docker     (123)     3308 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/sql/sql_provider.py
--rw-r--r--   0 runner    (1001) docker     (123)     1820 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/sql/testing.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-12 12:32:00.606202 clean-python-0.1.0/clean_python/testing/
--rw-r--r--   0 runner    (1001) docker     (123)       65 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/testing/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      202 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/testing/attr_dict.py
--rw-r--r--   0 runner    (1001) docker     (123)      796 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/testing/debugger.py
--rw-r--r--   0 runner    (1001) docker     (123)      832 2023-07-12 12:31:49.000000 clean-python-0.1.0/clean_python/testing/profilers.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-12 12:32:00.602202 clean-python-0.1.0/clean_python.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     6945 2023-07-12 12:32:00.000000 clean-python-0.1.0/clean_python.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2462 2023-07-12 12:32:00.000000 clean-python-0.1.0/clean_python.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-12 12:32:00.000000 clean-python-0.1.0/clean_python.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-12 12:32:00.000000 clean-python-0.1.0/clean_python.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)      228 2023-07-12 12:32:00.000000 clean-python-0.1.0/clean_python.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       13 2023-07-12 12:32:00.000000 clean-python-0.1.0/clean_python.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)     1279 2023-07-12 12:31:49.000000 clean-python-0.1.0/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)      183 2023-07-12 12:32:00.610202 clean-python-0.1.0/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-12 12:32:00.610202 clean-python-0.1.0/tests/
--rw-r--r--   0 runner    (1001) docker     (123)     2751 2023-07-12 12:31:49.000000 clean-python-0.1.0/tests/test_async_actor.py
--rw-r--r--   0 runner    (1001) docker     (123)     1338 2023-07-12 12:31:49.000000 clean-python-0.1.0/tests/test_celery_rmq_broker.py
--rw-r--r--   0 runner    (1001) docker     (123)     1989 2023-07-12 12:31:49.000000 clean-python-0.1.0/tests/test_dramatiq_task_logger.py
--rw-r--r--   0 runner    (1001) docker     (123)      758 2023-07-12 12:31:49.000000 clean-python-0.1.0/tests/test_exceptions.py
--rw-r--r--   0 runner    (1001) docker     (123)     4501 2023-07-12 12:31:49.000000 clean-python-0.1.0/tests/test_fastapi_access_logger.py
--rw-r--r--   0 runner    (1001) docker     (123)     5302 2023-07-12 12:31:49.000000 clean-python-0.1.0/tests/test_gateway.py
--rw-r--r--   0 runner    (1001) docker     (123)     3257 2023-07-12 12:31:49.000000 clean-python-0.1.0/tests/test_internal_gateway.py
--rw-r--r--   0 runner    (1001) docker     (123)     2419 2023-07-12 12:31:49.000000 clean-python-0.1.0/tests/test_manage.py
--rw-r--r--   0 runner    (1001) docker     (123)     5106 2023-07-12 12:31:49.000000 clean-python-0.1.0/tests/test_oauth2.py
--rw-r--r--   0 runner    (1001) docker     (123)     5229 2023-07-12 12:31:49.000000 clean-python-0.1.0/tests/test_repository.py
--rw-r--r--   0 runner    (1001) docker     (123)     1095 2023-07-12 12:31:49.000000 clean-python-0.1.0/tests/test_request_query.py
--rw-r--r--   0 runner    (1001) docker     (123)     3613 2023-07-12 12:31:49.000000 clean-python-0.1.0/tests/test_resource.py
--rw-r--r--   0 runner    (1001) docker     (123)     1719 2023-07-12 12:31:49.000000 clean-python-0.1.0/tests/test_root_entity.py
--rw-r--r--   0 runner    (1001) docker     (123)     1216 2023-07-12 12:31:49.000000 clean-python-0.1.0/tests/test_service.py
--rw-r--r--   0 runner    (1001) docker     (123)    15045 2023-07-12 12:31:49.000000 clean-python-0.1.0/tests/test_sql_gateway.py
--rw-r--r--   0 runner    (1001) docker     (123)     1218 2023-07-12 12:31:49.000000 clean-python-0.1.0/tests/test_value_object.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 06:14:06.580703 clean-python-0.2.0b0/
+-rw-r--r--   0 runner    (1001) docker     (123)      384 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/CHANGES.md
+-rw-r--r--   0 runner    (1001) docker     (123)     1103 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      137 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     6947 2023-07-23 06:14:06.580703 clean-python-0.2.0b0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     6429 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 06:14:06.572702 clean-python-0.2.0b0/clean_python/
+-rw-r--r--   0 runner    (1001) docker     (123)      100 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 06:14:06.572702 clean-python-0.2.0b0/clean_python/base/
+-rw-r--r--   0 runner    (1001) docker     (123)      139 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/base/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 06:14:06.572702 clean-python-0.2.0b0/clean_python/base/application/
+-rw-r--r--   0 runner    (1001) docker     (123)       30 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/base/application/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1991 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/base/application/manage.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 06:14:06.576702 clean-python-0.2.0b0/clean_python/base/domain/
+-rw-r--r--   0 runner    (1001) docker     (123)      365 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/base/domain/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      645 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/base/domain/domain_event.py
+-rw-r--r--   0 runner    (1001) docker     (123)      225 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/base/domain/domain_service.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1911 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/base/domain/exceptions.py
+-rw-r--r--   0 runner    (1001) docker     (123)      200 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/base/domain/filter.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1719 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/base/domain/gateway.py
+-rw-r--r--   0 runner    (1001) docker     (123)      117 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/base/domain/json.py
+-rw-r--r--   0 runner    (1001) docker     (123)      480 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/base/domain/pagination.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3053 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/base/domain/repository.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1147 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/base/domain/root_entity.py
+-rw-r--r--   0 runner    (1001) docker     (123)      220 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/base/domain/value.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1357 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/base/domain/value_object.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 06:14:06.576702 clean-python-0.2.0b0/clean_python/base/infrastructure/
+-rw-r--r--   0 runner    (1001) docker     (123)      120 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/base/infrastructure/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2542 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/base/infrastructure/in_memory_gateway.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1871 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/base/infrastructure/internal_gateway.py
+-rw-r--r--   0 runner    (1001) docker     (123)      317 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/base/infrastructure/tmpdir_provider.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 06:14:06.576702 clean-python-0.2.0b0/clean_python/base/presentation/
+-rw-r--r--   0 runner    (1001) docker     (123)       28 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/base/presentation/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      154 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/base/presentation/link.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 06:14:06.576702 clean-python-0.2.0b0/clean_python/celery/
+-rw-r--r--   0 runner    (1001) docker     (123)       41 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/celery/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2180 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/celery/celery_rmq_broker.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 06:14:06.576702 clean-python-0.2.0b0/clean_python/dramatiq/
+-rw-r--r--   0 runner    (1001) docker     (123)      113 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/dramatiq/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6049 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/dramatiq/async_actor.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2582 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/dramatiq/dramatiq_task_logger.py
+-rw-r--r--   0 runner    (1001) docker     (123)      687 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/dramatiq/sleep_task.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 06:14:06.576702 clean-python-0.2.0b0/clean_python/fastapi/
+-rw-r--r--   0 runner    (1001) docker     (123)      215 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/fastapi/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1140 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/fastapi/context.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2173 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/fastapi/error_responses.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2670 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/fastapi/fastapi_access_logger.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1633 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/fastapi/request_query.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6438 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/fastapi/resource.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6595 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/fastapi/service.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 06:14:06.576702 clean-python-0.2.0b0/clean_python/fluentbit/
+-rw-r--r--   0 runner    (1001) docker     (123)       41 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/fluentbit/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      493 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/fluentbit/fluentbit_gateway.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 06:14:06.576702 clean-python-0.2.0b0/clean_python/oauth2/
+-rw-r--r--   0 runner    (1001) docker     (123)       30 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/oauth2/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3828 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/oauth2/oauth2.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 06:14:06.580703 clean-python-0.2.0b0/clean_python/sql/
+-rw-r--r--   0 runner    (1001) docker     (123)       71 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/sql/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11528 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/sql/sql_gateway.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3308 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/sql/sql_provider.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1820 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/sql/testing.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 06:14:06.580703 clean-python-0.2.0b0/clean_python/testing/
+-rw-r--r--   0 runner    (1001) docker     (123)       65 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/testing/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      202 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/testing/attr_dict.py
+-rw-r--r--   0 runner    (1001) docker     (123)      796 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/testing/debugger.py
+-rw-r--r--   0 runner    (1001) docker     (123)      832 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/clean_python/testing/profilers.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 06:14:06.572702 clean-python-0.2.0b0/clean_python.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     6947 2023-07-23 06:14:06.000000 clean-python-0.2.0b0/clean_python.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2462 2023-07-23 06:14:06.000000 clean-python-0.2.0b0/clean_python.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 06:14:06.000000 clean-python-0.2.0b0/clean_python.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 06:14:06.000000 clean-python-0.2.0b0/clean_python.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)      228 2023-07-23 06:14:06.000000 clean-python-0.2.0b0/clean_python.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       13 2023-07-23 06:14:06.000000 clean-python-0.2.0b0/clean_python.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1279 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)      183 2023-07-23 06:14:06.580703 clean-python-0.2.0b0/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 06:14:06.580703 clean-python-0.2.0b0/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     2751 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/tests/test_async_actor.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1338 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/tests/test_celery_rmq_broker.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1989 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/tests/test_dramatiq_task_logger.py
+-rw-r--r--   0 runner    (1001) docker     (123)      740 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/tests/test_exceptions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4501 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/tests/test_fastapi_access_logger.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5302 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/tests/test_gateway.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3257 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/tests/test_internal_gateway.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2419 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/tests/test_manage.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5106 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/tests/test_oauth2.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5349 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/tests/test_repository.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1095 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/tests/test_request_query.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3613 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/tests/test_resource.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1778 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/tests/test_root_entity.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1216 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/tests/test_service.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15045 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/tests/test_sql_gateway.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1239 2023-07-23 06:13:57.000000 clean-python-0.2.0b0/tests/test_value_object.py
```

### Comparing `clean-python-0.1.0/LICENSE` & `clean-python-0.2.0b0/LICENSE`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/PKG-INFO` & `clean-python-0.2.0b0/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: clean-python
-Version: 0.1.0
+Version: 0.2.0b0
 Summary: Clean architecture in Python
 Author-email: Nelen & Schuurmans <info@nelen-schuurmans.nl>
 License: MIT
 Project-URL: homepage, https://github.com/nens/clean-python
 Classifier: Programming Language :: Python
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
```

### Comparing `clean-python-0.1.0/README.md` & `clean-python-0.2.0b0/README.md`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/clean_python/base/application/manage.py` & `clean-python-0.2.0b0/clean_python/base/application/manage.py`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/clean_python/base/domain/domain_event.py` & `clean-python-0.2.0b0/clean_python/base/domain/domain_event.py`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/clean_python/base/domain/exceptions.py` & `clean-python-0.2.0b0/clean_python/base/domain/exceptions.py`

 * *Files 12% similar despite different names*

```diff
@@ -2,15 +2,14 @@
 
 from typing import Any
 from typing import Optional
 from typing import Union
 
 from pydantic import create_model
 from pydantic import ValidationError
-from pydantic.error_wrappers import ErrorWrapper
 
 __all__ = [
     "AlreadyExists",
     "Conflict",
     "DoesNotExist",
     "PermissionDenied",
     "PreconditionFailed",
@@ -50,26 +49,23 @@
 
 
 # pydantic.ValidationError needs some model; for us it doesn't matter
 # We do it the same way as FastAPI does it.
 request_model = create_model("Request")
 
 
-class BadRequest(ValidationError):
+class BadRequest(Exception):
     def __init__(self, err_or_msg: Union[ValidationError, str]):
-        if isinstance(err_or_msg, ValidationError):
-            errors = err_or_msg.raw_errors
-        else:
-            errors = [ErrorWrapper(ValueError(err_or_msg), "*")]
-        super().__init__(errors, request_model)
+        self._internal_error = err_or_msg
+        super().__init__(err_or_msg)
 
     def __str__(self) -> str:
-        errors = self.errors()
-        if len(errors) == 1:
-            error = errors[0]
+        error = self._internal_error
+        if isinstance(error, ValidationError):
+            error = error.errors()[0]
             loc = "'" + ",".join([str(x) for x in error["loc"]]) + "' "
             if loc == "'*' ":
                 loc = ""
             return f"validation error: {loc}{error['msg']}"
         return super().__str__()
```

### Comparing `clean-python-0.1.0/clean_python/base/domain/gateway.py` & `clean-python-0.2.0b0/clean_python/base/domain/gateway.py`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/clean_python/base/domain/repository.py` & `clean-python-0.2.0b0/clean_python/base/domain/repository.py`

 * *Files 3% similar despite different names*

```diff
@@ -62,27 +62,27 @@
             raise DoesNotExist("object", id)
         else:
             return self.entity(**res)
 
     async def add(self, item: Union[T, Json]) -> T:
         if isinstance(item, dict):
             item = self.entity.create(**item)
-        created = await self.gateway.add(item.dict())
+        created = await self.gateway.add(item.model_dump())
         return self.entity(**created)
 
     async def update(self, id: int, values: Json) -> T:
         if not values:
             return await self.get(id)
         updated = await self.gateway.update_transactional(
-            id, lambda x: self.entity(**x).update(**values).dict()
+            id, lambda x: self.entity(**x).update(**values).model_dump()
         )
         return self.entity(**updated)
 
     async def upsert(self, item: T) -> T:
-        values = item.dict()
+        values = item.model_dump()
         upserted = await self.gateway.upsert(values)
         return self.entity(**upserted)
 
     async def remove(self, id: int) -> bool:
         return await self.gateway.remove(id)
 
     async def count(self, filters: List[Filter]) -> int:
```

### Comparing `clean-python-0.1.0/clean_python/base/domain/root_entity.py` & `clean-python-0.2.0b0/clean_python/base/domain/root_entity.py`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/clean_python/base/domain/value_object.py` & `clean-python-0.2.0b0/clean_python/base/domain/value_object.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,44 +1,44 @@
 # (c) Nelen & Schuurmans
 
 from typing import Optional
 from typing import Type
 from typing import TypeVar
 
 from pydantic import BaseModel
+from pydantic import ConfigDict
 from pydantic import ValidationError
 
 from .exceptions import BadRequest
 
 __all__ = ["ValueObject"]
 
 
 T = TypeVar("T", bound="ValueObject")
 
 
 class ValueObject(BaseModel):
-    class Config:
-        allow_mutation = False
+    model_config = ConfigDict(frozen=True)
 
     def run_validation(self: T) -> T:
         try:
-            return self.__class__(**self.dict())
+            return self.__class__(**self.model_dump())
         except ValidationError as e:
             raise BadRequest(e)
 
     @classmethod
     def create(cls: Type[T], **values) -> T:
         try:
             return cls(**values)
         except ValidationError as e:
             raise BadRequest(e)
 
     def update(self: T, **values) -> T:
         try:
-            return self.__class__(**{**self.dict(), **values})
+            return self.__class__(**{**self.model_dump(), **values})
         except ValidationError as e:
             raise BadRequest(e)
 
     def __hash__(self):
         return hash(self.__class__) + hash(tuple(self.__dict__.values()))
```

### Comparing `clean-python-0.1.0/clean_python/base/infrastructure/in_memory_gateway.py` & `clean-python-0.2.0b0/clean_python/base/infrastructure/in_memory_gateway.py`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/clean_python/base/infrastructure/internal_gateway.py` & `clean-python-0.2.0b0/clean_python/base/infrastructure/internal_gateway.py`

 * *Files 1% similar despite different names*

```diff
@@ -40,15 +40,15 @@
         self, filters: List[Filter], params: Optional[PageOptions] = None
     ) -> List[T]:
         page = await self.manage.filter(filters, params)
         return [self._map(x) for x in page.items]
 
     async def add(self, item: T) -> T:
         try:
-            created = await self.manage.create(item.dict())
+            created = await self.manage.create(item.model_dump())
         except BadRequest as e:
             raise ValueError(e)
         return self._map(created)
 
     async def remove(self, id) -> bool:
         return await self.manage.destroy(id)
```

### Comparing `clean-python-0.1.0/clean_python/celery/celery_rmq_broker.py` & `clean-python-0.2.0b0/clean_python/celery/celery_rmq_broker.py`

 * *Files 4% similar despite different names*

```diff
@@ -23,15 +23,15 @@
     parent_id: Optional[uuid.UUID] = None
     group: Optional[uuid.UUID] = None
     argsrepr: Optional[str] = None
     kwargsrepr: Optional[str] = None
     origin: Optional[str] = None
 
     def json_dict(self):
-        return json.loads(self.json())
+        return json.loads(self.model_dump_json())
 
 
 class CeleryRmqBroker(Gateway):
     def __init__(
         self, broker_url: AnyUrl, queue: str, origin: str, declare_queue: bool = False
     ):
         self._parameters = pika.URLParameters(broker_url)
```

### Comparing `clean-python-0.1.0/clean_python/dramatiq/async_actor.py` & `clean-python-0.2.0b0/clean_python/dramatiq/async_actor.py`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/clean_python/dramatiq/dramatiq_task_logger.py` & `clean-python-0.2.0b0/clean_python/dramatiq/dramatiq_task_logger.py`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/clean_python/dramatiq/sleep_task.py` & `clean-python-0.2.0b0/clean_python/dramatiq/sleep_task.py`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/clean_python/fastapi/context.py` & `clean-python-0.2.0b0/clean_python/fastapi/context.py`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/clean_python/fastapi/error_responses.py` & `clean-python-0.2.0b0/clean_python/fastapi/error_responses.py`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/clean_python/fastapi/fastapi_access_logger.py` & `clean-python-0.2.0b0/clean_python/fastapi/fastapi_access_logger.py`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/clean_python/fastapi/request_query.py` & `clean-python-0.2.0b0/clean_python/fastapi/request_query.py`

 * *Files 5% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 # (c) Nelen & Schuurmans
 
 from typing import List
 
 from fastapi import Query
-from pydantic import validator
+from pydantic import field_validator
 
 from clean_python import Filter
 from clean_python import PageOptions
 from clean_python import ValueObject
 
 __all__ = ["RequestQuery"]
 
@@ -15,19 +15,19 @@
 class RequestQuery(ValueObject):
     limit: int = Query(50, ge=1, le=100, description="Page size limit")
     offset: int = Query(0, ge=0, description="Page offset")
     order_by: str = Query(
         default="id", enum=["id", "-id"], description="Field to order by"
     )
 
-    @validator("order_by")
-    def validate_order_by_enum(cls, v):
+    @field_validator("order_by")
+    def validate_order_by_enum(cls, v, _):
         # the 'enum' parameter doesn't actually do anthing in validation
         # See: https://github.com/tiangolo/fastapi/issues/2910
-        allowed = cls.__fields__["order_by"].field_info.extra["enum"]
+        allowed = cls.model_fields["order_by"].json_schema_extra["enum"]
         if v not in allowed:
             raise ValueError(f"'order_by' must be one of {allowed}")
         return v
 
     def as_page_options(self) -> PageOptions:
         if self.order_by.startswith("-"):
             order_by = self.order_by[1:]
@@ -37,14 +37,14 @@
             ascending = True
         return PageOptions(
             limit=self.limit, offset=self.offset, order_by=order_by, ascending=ascending
         )
 
     def filters(self) -> List[Filter]:
         result = []
-        for name in self.__fields__:
+        for name in self.model_fields:
             if name in {"limit", "offset", "order_by"}:
                 continue
             value = getattr(self, name)
             if value is not None:
                 result.append(Filter(field=name, values=[value]))
         return result
```

### Comparing `clean-python-0.1.0/clean_python/fastapi/resource.py` & `clean-python-0.2.0b0/clean_python/fastapi/resource.py`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/clean_python/fastapi/service.py` & `clean-python-0.2.0b0/clean_python/fastapi/service.py`

 * *Files 1% similar despite different names*

```diff
@@ -137,15 +137,16 @@
         return app
 
     def _create_versioned_app(self, version: APIVersion, **kwargs) -> FastAPI:
         resources = [x for x in self.resources if x.version == version]
         app = FastAPI(
             version=version.prefix,
             tags=sorted(
-                [x.get_openapi_tag().dict() for x in resources], key=lambda x: x["name"]
+                [x.get_openapi_tag().model_dump() for x in resources],
+                key=lambda x: x["name"],
             ),
             **kwargs,
         )
         for resource in resources:
             app.include_router(
                 resource.get_router(
                     version,
```

### Comparing `clean-python-0.1.0/clean_python/oauth2/oauth2.py` & `clean-python-0.2.0b0/clean_python/oauth2/oauth2.py`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/clean_python/sql/sql_gateway.py` & `clean-python-0.2.0b0/clean_python/sql/sql_gateway.py`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/clean_python/sql/sql_provider.py` & `clean-python-0.2.0b0/clean_python/sql/sql_provider.py`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/clean_python/sql/testing.py` & `clean-python-0.2.0b0/clean_python/sql/testing.py`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/clean_python/testing/debugger.py` & `clean-python-0.2.0b0/clean_python/testing/debugger.py`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/clean_python/testing/profilers.py` & `clean-python-0.2.0b0/clean_python/testing/profilers.py`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/clean_python.egg-info/PKG-INFO` & `clean-python-0.2.0b0/clean_python.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: clean-python
-Version: 0.1.0
+Version: 0.2.0b0
 Summary: Clean architecture in Python
 Author-email: Nelen & Schuurmans <info@nelen-schuurmans.nl>
 License: MIT
 Project-URL: homepage, https://github.com/nens/clean-python
 Classifier: Programming Language :: Python
 Requires-Python: >=3.7
 Description-Content-Type: text/markdown
```

### Comparing `clean-python-0.1.0/clean_python.egg-info/SOURCES.txt` & `clean-python-0.2.0b0/clean_python.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/pyproject.toml` & `clean-python-0.2.0b0/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -6,15 +6,15 @@
 ]
 readme = "README.md"
 license = {text = "MIT"}
 # Get classifier strings from http://www.python.org/pypi?%3Aaction=list_classifiers
 classifiers = ["Programming Language :: Python"]
 keywords = []
 requires-python = ">=3.7"
-dependencies = ["pydantic==1.*", "inject", "asgiref", "blinker"]
+dependencies = ["pydantic==2.*", "inject", "asgiref", "blinker"]
 dynamic = ["version"]
 
 [project.optional-dependencies]
 test = [
     "pytest",
     "pytest-cov",
     "pytest-asyncio",
```

### Comparing `clean-python-0.1.0/tests/test_async_actor.py` & `clean-python-0.2.0b0/tests/test_async_actor.py`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/tests/test_celery_rmq_broker.py` & `clean-python-0.2.0b0/tests/test_celery_rmq_broker.py`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/tests/test_dramatiq_task_logger.py` & `clean-python-0.2.0b0/tests/test_dramatiq_task_logger.py`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/tests/test_exceptions.py` & `clean-python-0.2.0b0/tests/test_exceptions.py`

 * *Files 3% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 from clean_python import BadRequest
 from clean_python import DoesNotExist
 from clean_python import ValueObject
 
 
 def test_bad_request_short_str():
     e = BadRequest("bla bla bla")
-    assert str(e) == "validation error: bla bla bla"
+    assert str(e) == "bla bla bla"
 
 
 def test_does_not_exist_str():
     e = DoesNotExist("raster", id=12)
     assert str(e) == "does not exist: raster with id=12"
 
 
@@ -26,8 +26,8 @@
 
 def test_bad_request_from_validation_error():
     try:
         Book()
     except ValidationError as e:
         err = BadRequest(e)
 
-    assert str(err) == "validation error: 'title' field required"
+    assert str(err) == "validation error: 'title' Field required"
```

### Comparing `clean-python-0.1.0/tests/test_fastapi_access_logger.py` & `clean-python-0.2.0b0/tests/test_fastapi_access_logger.py`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/tests/test_gateway.py` & `clean-python-0.2.0b0/tests/test_gateway.py`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/tests/test_internal_gateway.py` & `clean-python-0.2.0b0/tests/test_internal_gateway.py`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/tests/test_manage.py` & `clean-python-0.2.0b0/tests/test_manage.py`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/tests/test_oauth2.py` & `clean-python-0.2.0b0/tests/test_oauth2.py`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/tests/test_repository.py` & `clean-python-0.2.0b0/tests/test_repository.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,7 +1,8 @@
+from typing import List
 from unittest import mock
 
 import pytest
 
 from clean_python import BadRequest
 from clean_python import DoesNotExist
 from clean_python import Filter
@@ -26,16 +27,16 @@
 
 
 class UserRepository(Repository[User]):
     pass
 
 
 @pytest.fixture
-def user_repository(users):
-    return UserRepository(gateway=InMemoryGateway(data=[x.dict() for x in users]))
+def user_repository(users: List[User]):
+    return UserRepository(gateway=InMemoryGateway(data=[x.model_dump() for x in users]))
 
 
 @pytest.fixture
 def page_options():
     return PageOptions(limit=10, offset=0, order_by="id")
 
 
@@ -58,34 +59,34 @@
     filter_m.return_value = Page(total=0, items=[])
     assert await user_repository.all(page_options) is filter_m.return_value
 
     filter_m.assert_awaited_once_with([], params=page_options)
 
 
 async def test_add(user_repository):
-    actual = await user_repository.add(User.create(name="d"))
+    actual: User = await user_repository.add(User.create(name="d"))
     assert actual.name == "d"
-    assert user_repository.gateway.data[4] == actual.dict()
+    assert user_repository.gateway.data[4] == actual.model_dump()
 
 
 async def test_add_json(user_repository):
-    actual = await user_repository.add({"name": "d"})
+    actual: User = await user_repository.add({"name": "d"})
     assert actual.name == "d"
-    assert user_repository.gateway.data[4] == actual.dict()
+    assert user_repository.gateway.data[4] == actual.model_dump()
 
 
 async def test_add_json_validates(user_repository):
     with pytest.raises(BadRequest):
         await user_repository.add({"id": "d"})
 
 
 async def test_update(user_repository):
-    actual = await user_repository.update(id=2, values={"name": "d"})
+    actual: User = await user_repository.update(id=2, values={"name": "d"})
     assert actual.name == "d"
-    assert user_repository.gateway.data[2] == actual.dict()
+    assert user_repository.gateway.data[2] == actual.model_dump()
 
 
 async def test_update_does_not_exist(user_repository):
     with pytest.raises(DoesNotExist):
         await user_repository.update(id=4, values={"name": "d"})
 
 
@@ -100,35 +101,35 @@
 
 
 async def test_remove_does_not_exist(user_repository):
     assert not await user_repository.remove(4)
 
 
 async def test_upsert_updates(user_repository):
-    actual = await user_repository.upsert(User.create(id=2, name="d"))
+    actual: User = await user_repository.upsert(User.create(id=2, name="d"))
     assert actual.name == "d"
-    assert user_repository.gateway.data[2] == actual.dict()
+    assert user_repository.gateway.data[2] == actual.model_dump()
 
 
 async def test_upsert_adds(user_repository):
-    actual = await user_repository.upsert(User.create(id=4, name="d"))
+    actual: User = await user_repository.upsert(User.create(id=4, name="d"))
     assert actual.name == "d"
-    assert user_repository.gateway.data[4] == actual.dict()
+    assert user_repository.gateway.data[4] == actual.model_dump()
 
 
 @mock.patch.object(InMemoryGateway, "count")
 async def test_filter(count_m, user_repository, users):
-    actual = await user_repository.filter([Filter(field="name", values=["b"])])
+    actual: Page = await user_repository.filter([Filter(field="name", values=["b"])])
     assert actual == Page(total=1, items=[users[1]], limit=None, offest=None)
     assert not count_m.called
 
 
 @mock.patch.object(InMemoryGateway, "count")
 async def test_filter_with_pagination(count_m, user_repository, users, page_options):
-    actual = await user_repository.filter(
+    actual: Page = await user_repository.filter(
         [Filter(field="name", values=["b"])], page_options
     )
     assert actual == Page(
         total=1, items=[users[1]], limit=page_options.limit, offset=page_options.offset
     )
     assert not count_m.called
 
@@ -141,15 +142,15 @@
     ],
 )
 @mock.patch.object(InMemoryGateway, "count")
 async def test_filter_with_pagination_calls_count(
     count_m, user_repository, users, page_options
 ):
     count_m.return_value = 123
-    actual = await user_repository.filter([], page_options)
+    actual: Page = await user_repository.filter([], page_options)
     assert actual == Page(
         total=count_m.return_value,
         items=users[page_options.offset :],
         limit=page_options.limit,
         offset=page_options.offset,
     )
     assert count_m.called
```

### Comparing `clean-python-0.1.0/tests/test_request_query.py` & `clean-python-0.2.0b0/tests/test_request_query.py`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/tests/test_resource.py` & `clean-python-0.2.0b0/tests/test_resource.py`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/tests/test_root_entity.py` & `clean-python-0.2.0b0/tests/test_root_entity.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,14 +1,15 @@
 from datetime import datetime
 from datetime import timezone
 from unittest import mock
 
 import pytest
 
 from clean_python import RootEntity
+from clean_python.base.domain.exceptions import BadRequest
 
 SOME_DATETIME = datetime(2023, 1, 1, tzinfo=timezone.utc)
 
 
 class User(RootEntity):
     name: str
 
@@ -60,15 +61,15 @@
 
     assert actual is not user
     assert actual.name == "piet"
 
 
 @pytest.mark.parametrize("new_id", [None, 42, "foo"])
 def test_update_with_wrong_id(user, new_id):
-    with pytest.raises(ValueError):
+    with pytest.raises(BadRequest):
         user.update(id=new_id, name="piet")
 
 
 @pytest.mark.parametrize("new_id", [None, 42])
 def test_update_give_id(new_id):
     user_without_id = User.create(name="jan")
     actual = user_without_id.update(id=new_id, name="piet")
```

### Comparing `clean-python-0.1.0/tests/test_service.py` & `clean-python-0.2.0b0/tests/test_service.py`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/tests/test_sql_gateway.py` & `clean-python-0.2.0b0/tests/test_sql_gateway.py`

 * *Files identical despite different names*

### Comparing `clean-python-0.1.0/tests/test_value_object.py` & `clean-python-0.2.0b0/tests/test_value_object.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,20 +1,20 @@
 import pytest
+from pydantic import field_validator
 from pydantic import ValidationError
-from pydantic import validator
 
 from clean_python import BadRequest
 from clean_python import ValueObject
 
 
 class Color(ValueObject):
     name: str
 
-    @validator("name")
-    def name_not_empty(cls, v):
+    @field_validator("name")
+    def name_not_empty(cls, v, _):
         assert v != ""
         return v
 
 
 @pytest.fixture
 def color():
     return Color(name="green")
@@ -45,15 +45,15 @@
 
 
 def test_run_validation(color):
     assert color.run_validation() == color
 
 
 def test_run_validation_err():
-    color = Color.construct(name="")
+    color = Color.model_construct(name="")
 
     with pytest.raises(BadRequest):
         color.run_validation()
 
 
 def test_hashable(color):
     assert len({color, color}) == 1
```

