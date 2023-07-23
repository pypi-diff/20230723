# Comparing `tmp/lassen-0.2.0.tar.gz` & `tmp/lassen-0.2.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "lassen-0.2.0.tar", max compression
+gzip compressed data, was "lassen-0.2.1.tar", max compression
```

## Comparing `lassen-0.2.0.tar` & `lassen-0.2.1.tar`

### file list

```diff
@@ -1,76 +1,77 @@
--rw-r--r--   0        0        0     1071 2023-06-06 18:13:43.336753 lassen-0.2.0/LICENSE
--rw-r--r--   0        0        0     3159 2023-07-22 17:00:28.388296 lassen-0.2.0/README.md
--rw-r--r--   0        0        0        0 2023-06-06 23:14:20.986429 lassen-0.2.0/lassen/__init__.py
--rw-r--r--   0        0        0        0 2023-06-06 23:14:20.986933 lassen-0.2.0/lassen/alembic/__init__.py
--rw-r--r--   0        0        0     3685 2023-06-06 23:14:20.987092 lassen-0.2.0/lassen/alembic/cli.py
--rw-r--r--   0        0        0     2839 2023-07-22 17:00:28.388594 lassen-0.2.0/lassen/alembic/io.py
--rw-r--r--   0        0        0     1043 2023-06-06 23:14:20.987305 lassen-0.2.0/lassen/alembic/runner.py
--rw-r--r--   0        0        0      174 2023-06-06 23:14:20.987414 lassen-0.2.0/lassen/assets/__init__.py
--rw-r--r--   0        0        0     1592 2023-06-06 23:14:20.987525 lassen-0.2.0/lassen/assets/alembic.ini
--rw-r--r--   0        0        0      494 2023-06-06 23:14:20.987634 lassen-0.2.0/lassen/assets/script.py.mako
--rw-r--r--   0        0        0        0 2023-06-06 23:14:20.987697 lassen-0.2.0/lassen/core/__init__.py
--rw-r--r--   0        0        0      153 2023-06-15 21:16:27.734730 lassen-0.2.0/lassen/core/__pycache__/__init__.cpython-310.pyc
--rw-r--r--   0        0        0     2487 2023-06-15 21:16:27.734981 lassen-0.2.0/lassen/core/__pycache__/config.cpython-310.pyc
--rw-r--r--   0        0        0     1862 2023-06-06 23:14:20.988497 lassen-0.2.0/lassen/core/config.py
--rw-r--r--   0        0        0        0 2023-06-15 21:16:27.735020 lassen-0.2.0/lassen/datasets/__init__.py
--rw-r--r--   0        0        0     2368 2023-06-15 22:39:22.170659 lassen-0.2.0/lassen/datasets/dataset_helpers.py
--rw-r--r--   0        0        0     3024 2023-06-15 22:26:02.922940 lassen-0.2.0/lassen/datasets/pyarrow_schemas.py
--rw-r--r--   0        0        0      240 2023-06-06 23:14:20.988685 lassen-0.2.0/lassen/db/__init__.py
--rw-r--r--   0        0        0      396 2023-06-15 21:16:27.735607 lassen-0.2.0/lassen/db/__pycache__/__init__.cpython-310.pyc
--rw-r--r--   0        0        0      422 2023-07-22 17:00:28.388869 lassen-0.2.0/lassen/db/__pycache__/__init__.cpython-311.pyc
--rw-r--r--   0        0        0      147 2023-06-06 23:14:20.989285 lassen-0.2.0/lassen/db/__pycache__/base.cpython-310.pyc
--rw-r--r--   0        0        0      293 2023-06-06 23:14:20.989436 lassen-0.2.0/lassen/db/__pycache__/base.cpython-311.pyc
--rw-r--r--   0        0        0     1931 2023-06-15 21:16:27.735885 lassen-0.2.0/lassen/db/__pycache__/base_class.cpython-310.pyc
--rw-r--r--   0        0        0     2976 2023-07-22 17:00:28.389221 lassen-0.2.0/lassen/db/__pycache__/base_class.cpython-311.pyc
--rw-r--r--   0        0        0      839 2023-06-15 21:16:27.736092 lassen-0.2.0/lassen/db/__pycache__/session.cpython-310.pyc
--rw-r--r--   0        0        0     1296 2023-07-22 17:00:28.389524 lassen-0.2.0/lassen/db/__pycache__/session.cpython-311.pyc
--rw-r--r--   0        0        0     1920 2023-07-22 17:00:28.389828 lassen-0.2.0/lassen/db/base_class.py
--rw-r--r--   0        0        0      627 2023-06-06 23:14:20.990409 lassen-0.2.0/lassen/db/session.py
--rw-r--r--   0        0        0     1272 2023-07-22 17:00:28.389917 lassen-0.2.0/lassen/io.py
--rw-r--r--   0        0        0      210 2023-06-06 23:14:20.990522 lassen-0.2.0/lassen/schema.py
--rw-r--r--   0        0        0      227 2023-06-15 21:16:27.736193 lassen-0.2.0/lassen/shared.py
--rw-r--r--   0        0        0     9988 2023-07-22 17:00:28.390179 lassen-0.2.0/lassen/store.py
--rw-r--r--   0        0        0      201 2023-07-22 17:00:28.390303 lassen-0.2.0/lassen/stubs/__init__.py
--rw-r--r--   0        0        0     1170 2023-07-22 17:00:28.390398 lassen-0.2.0/lassen/stubs/base.py
--rw-r--r--   0        0        0      147 2023-07-22 17:00:28.390482 lassen-0.2.0/lassen/stubs/definition.py
--rw-r--r--   0        0        0     1892 2023-07-22 17:00:28.390588 lassen-0.2.0/lassen/stubs/field.py
--rw-r--r--   0        0        0     3731 2023-07-22 17:00:28.390696 lassen-0.2.0/lassen/stubs/generate.py
--rw-r--r--   0        0        0       96 2023-07-22 17:00:28.390790 lassen-0.2.0/lassen/stubs/generators/__init__.py
--rw-r--r--   0        0        0     8487 2023-07-22 17:00:28.390910 lassen-0.2.0/lassen/stubs/generators/common.py
--rw-r--r--   0        0        0     4165 2023-07-22 17:00:28.391026 lassen-0.2.0/lassen/stubs/generators/schema.py
--rw-r--r--   0        0        0    12025 2023-07-22 17:00:28.391178 lassen-0.2.0/lassen/stubs/generators/store.py
--rw-r--r--   0        0        0      177 2023-07-22 17:00:28.391343 lassen-0.2.0/lassen/stubs/templates/__init__.py
--rw-r--r--   0        0        0     1052 2023-07-22 17:00:28.391457 lassen-0.2.0/lassen/stubs/templates/schema.py.j2
--rw-r--r--   0        0        0      551 2023-07-22 17:00:28.391564 lassen-0.2.0/lassen/stubs/templates/sqlalchemy.py.j2
--rw-r--r--   0        0        0        0 2023-06-06 23:14:20.990727 lassen-0.2.0/lassen/tests/__init__.py
--rw-r--r--   0        0        0      154 2023-06-15 21:16:27.736415 lassen-0.2.0/lassen/tests/__pycache__/__init__.cpython-310.pyc
--rw-r--r--   0        0        0     1973 2023-06-15 21:31:07.938752 lassen-0.2.0/lassen/tests/__pycache__/conftest.cpython-310-pytest-7.3.1.pyc
--rw-r--r--   0        0        0     1220 2023-06-06 23:14:20.991368 lassen-0.2.0/lassen/tests/__pycache__/fixtures.cpython-310.pyc
--rw-r--r--   0        0        0     5734 2023-06-15 21:16:27.736953 lassen-0.2.0/lassen/tests/__pycache__/test_store.cpython-310-pytest-7.3.1.pyc
--rw-r--r--   0        0        0     1901 2023-06-15 21:16:27.737091 lassen-0.2.0/lassen/tests/conftest.py
--rw-r--r--   0        0        0        0 2023-06-15 21:16:27.737128 lassen-0.2.0/lassen/tests/datasets/__init__.py
--rw-r--r--   0        0        0     2243 2023-06-15 22:42:38.547093 lassen-0.2.0/lassen/tests/datasets/test_dataset_helpers.py
--rw-r--r--   0        0        0     1645 2023-06-15 22:26:02.923228 lassen-0.2.0/lassen/tests/datasets/test_pyarrow_schemas.py
--rw-r--r--   0        0        0      176 2023-06-06 23:14:20.991801 lassen-0.2.0/lassen/tests/fixtures/__init__.py
--rw-r--r--   0        0        0     1215 2023-07-22 17:00:28.391699 lassen-0.2.0/lassen/tests/fixtures/stubs/expected_schema.py
--rw-r--r--   0        0        0     1013 2023-07-22 17:00:28.391801 lassen-0.2.0/lassen/tests/fixtures/stubs/expected_schema_public.py
--rw-r--r--   0        0        0      989 2023-07-22 17:00:28.391909 lassen-0.2.0/lassen/tests/fixtures/stubs/expected_store.py
--rw-r--r--   0        0        0     1095 2023-07-22 17:00:28.392269 lassen-0.2.0/lassen/tests/fixtures/stubs/fixtures.py
--rw-r--r--   0        0        0      463 2023-06-06 23:14:20.991923 lassen-0.2.0/lassen/tests/fixtures/test_harness/README.md
--rw-r--r--   0        0        0      311 2023-06-06 23:14:20.992056 lassen-0.2.0/lassen/tests/fixtures/test_harness/pyproject.toml
--rw-r--r--   0        0        0        0 2023-06-06 23:14:20.992112 lassen-0.2.0/lassen/tests/fixtures/test_harness/test_harness/__init__.py
--rw-r--r--   0        0        0      691 2023-06-06 23:14:20.992321 lassen-0.2.0/lassen/tests/fixtures/test_harness/test_harness/migrations/62bf8def9fb1_new_migration.py
--rw-r--r--   0        0        0      653 2023-06-06 23:14:20.992456 lassen-0.2.0/lassen/tests/fixtures/test_harness/test_harness/migrations/96dbf6f6d068_add_name.py
--rw-r--r--   0        0        0      217 2023-06-06 23:14:20.992593 lassen-0.2.0/lassen/tests/fixtures/test_harness/test_harness/models.py
--rw-r--r--   0        0        0      461 2023-06-06 23:14:20.992727 lassen-0.2.0/lassen/tests/model_fixtures.py
--rw-r--r--   0        0        0        0 2023-07-22 17:00:28.392359 lassen-0.2.0/lassen/tests/stubs/__init__.py
--rw-r--r--   0        0        0        0 2023-07-22 17:00:28.392464 lassen-0.2.0/lassen/tests/stubs/generators/__init__.py
--rw-r--r--   0        0        0     3828 2023-07-22 17:00:28.392630 lassen-0.2.0/lassen/tests/stubs/generators/test_common.py
--rw-r--r--   0        0        0      712 2023-07-22 17:00:28.392845 lassen-0.2.0/lassen/tests/stubs/generators/test_schema.py
--rw-r--r--   0        0        0     2671 2023-07-22 17:00:28.393035 lassen-0.2.0/lassen/tests/stubs/generators/test_store.py
--rw-r--r--   0        0        0     2560 2023-07-22 17:00:28.393152 lassen-0.2.0/lassen/tests/stubs/test_generate.py
--rw-r--r--   0        0        0     2252 2023-06-06 23:14:20.992858 lassen-0.2.0/lassen/tests/test_alembic.py
--rw-r--r--   0        0        0     2842 2023-07-22 17:00:28.393357 lassen-0.2.0/lassen/tests/test_store.py
--rw-r--r--   0        0        0     1423 2023-07-22 17:00:34.267205 lassen-0.2.0/pyproject.toml
--rw-r--r--   0        0        0     4987 1970-01-01 00:00:00.000000 lassen-0.2.0/setup.py
--rw-r--r--   0        0        0     4129 1970-01-01 00:00:00.000000 lassen-0.2.0/PKG-INFO
+-rw-r--r--   0        0        0     1071 2023-06-06 18:13:43.336753 lassen-0.2.1/LICENSE
+-rw-r--r--   0        0        0     3159 2023-07-22 17:00:28.388296 lassen-0.2.1/README.md
+-rw-r--r--   0        0        0        0 2023-06-06 23:14:20.986429 lassen-0.2.1/lassen/__init__.py
+-rw-r--r--   0        0        0        0 2023-06-06 23:14:20.986933 lassen-0.2.1/lassen/alembic/__init__.py
+-rw-r--r--   0        0        0     3685 2023-06-06 23:14:20.987092 lassen-0.2.1/lassen/alembic/cli.py
+-rw-r--r--   0        0        0     2839 2023-07-22 17:00:28.388594 lassen-0.2.1/lassen/alembic/io.py
+-rw-r--r--   0        0        0     1043 2023-06-06 23:14:20.987305 lassen-0.2.1/lassen/alembic/runner.py
+-rw-r--r--   0        0        0      174 2023-06-06 23:14:20.987414 lassen-0.2.1/lassen/assets/__init__.py
+-rw-r--r--   0        0        0     1592 2023-06-06 23:14:20.987525 lassen-0.2.1/lassen/assets/alembic.ini
+-rw-r--r--   0        0        0      494 2023-06-06 23:14:20.987634 lassen-0.2.1/lassen/assets/script.py.mako
+-rw-r--r--   0        0        0        0 2023-06-06 23:14:20.987697 lassen-0.2.1/lassen/core/__init__.py
+-rw-r--r--   0        0        0      153 2023-06-15 21:16:27.734730 lassen-0.2.1/lassen/core/__pycache__/__init__.cpython-310.pyc
+-rw-r--r--   0        0        0     2487 2023-06-15 21:16:27.734981 lassen-0.2.1/lassen/core/__pycache__/config.cpython-310.pyc
+-rw-r--r--   0        0        0     1862 2023-06-06 23:14:20.988497 lassen-0.2.1/lassen/core/config.py
+-rw-r--r--   0        0        0        0 2023-06-15 21:16:27.735020 lassen-0.2.1/lassen/datasets/__init__.py
+-rw-r--r--   0        0        0     2368 2023-06-15 22:39:22.170659 lassen-0.2.1/lassen/datasets/dataset_helpers.py
+-rw-r--r--   0        0        0     3024 2023-06-15 22:26:02.922940 lassen-0.2.1/lassen/datasets/pyarrow_schemas.py
+-rw-r--r--   0        0        0      240 2023-06-06 23:14:20.988685 lassen-0.2.1/lassen/db/__init__.py
+-rw-r--r--   0        0        0      396 2023-06-15 21:16:27.735607 lassen-0.2.1/lassen/db/__pycache__/__init__.cpython-310.pyc
+-rw-r--r--   0        0        0      422 2023-07-22 17:00:28.388869 lassen-0.2.1/lassen/db/__pycache__/__init__.cpython-311.pyc
+-rw-r--r--   0        0        0      147 2023-06-06 23:14:20.989285 lassen-0.2.1/lassen/db/__pycache__/base.cpython-310.pyc
+-rw-r--r--   0        0        0      293 2023-06-06 23:14:20.989436 lassen-0.2.1/lassen/db/__pycache__/base.cpython-311.pyc
+-rw-r--r--   0        0        0     1931 2023-06-15 21:16:27.735885 lassen-0.2.1/lassen/db/__pycache__/base_class.cpython-310.pyc
+-rw-r--r--   0        0        0     2976 2023-07-22 17:00:28.389221 lassen-0.2.1/lassen/db/__pycache__/base_class.cpython-311.pyc
+-rw-r--r--   0        0        0      839 2023-06-15 21:16:27.736092 lassen-0.2.1/lassen/db/__pycache__/session.cpython-310.pyc
+-rw-r--r--   0        0        0     1296 2023-07-22 17:00:28.389524 lassen-0.2.1/lassen/db/__pycache__/session.cpython-311.pyc
+-rw-r--r--   0        0        0     1920 2023-07-22 17:00:28.389828 lassen-0.2.1/lassen/db/base_class.py
+-rw-r--r--   0        0        0      627 2023-06-06 23:14:20.990409 lassen-0.2.1/lassen/db/session.py
+-rw-r--r--   0        0        0     1272 2023-07-22 17:00:28.389917 lassen-0.2.1/lassen/io.py
+-rw-r--r--   0        0        0        0 2023-07-22 17:05:14.900856 lassen-0.2.1/lassen/py.typed
+-rw-r--r--   0        0        0      210 2023-06-06 23:14:20.990522 lassen-0.2.1/lassen/schema.py
+-rw-r--r--   0        0        0      227 2023-06-15 21:16:27.736193 lassen-0.2.1/lassen/shared.py
+-rw-r--r--   0        0        0     9988 2023-07-22 17:00:28.390179 lassen-0.2.1/lassen/store.py
+-rw-r--r--   0        0        0      201 2023-07-22 17:00:28.390303 lassen-0.2.1/lassen/stubs/__init__.py
+-rw-r--r--   0        0        0     1170 2023-07-22 17:00:28.390398 lassen-0.2.1/lassen/stubs/base.py
+-rw-r--r--   0        0        0      147 2023-07-22 17:00:28.390482 lassen-0.2.1/lassen/stubs/definition.py
+-rw-r--r--   0        0        0     1892 2023-07-22 17:00:28.390588 lassen-0.2.1/lassen/stubs/field.py
+-rw-r--r--   0        0        0     3731 2023-07-22 17:00:28.390696 lassen-0.2.1/lassen/stubs/generate.py
+-rw-r--r--   0        0        0       96 2023-07-22 17:00:28.390790 lassen-0.2.1/lassen/stubs/generators/__init__.py
+-rw-r--r--   0        0        0     8487 2023-07-22 17:00:28.390910 lassen-0.2.1/lassen/stubs/generators/common.py
+-rw-r--r--   0        0        0     4165 2023-07-22 17:00:28.391026 lassen-0.2.1/lassen/stubs/generators/schema.py
+-rw-r--r--   0        0        0    12025 2023-07-22 17:00:28.391178 lassen-0.2.1/lassen/stubs/generators/store.py
+-rw-r--r--   0        0        0      177 2023-07-22 17:00:28.391343 lassen-0.2.1/lassen/stubs/templates/__init__.py
+-rw-r--r--   0        0        0     1052 2023-07-22 17:00:28.391457 lassen-0.2.1/lassen/stubs/templates/schema.py.j2
+-rw-r--r--   0        0        0      551 2023-07-22 17:00:28.391564 lassen-0.2.1/lassen/stubs/templates/sqlalchemy.py.j2
+-rw-r--r--   0        0        0        0 2023-06-06 23:14:20.990727 lassen-0.2.1/lassen/tests/__init__.py
+-rw-r--r--   0        0        0      154 2023-06-15 21:16:27.736415 lassen-0.2.1/lassen/tests/__pycache__/__init__.cpython-310.pyc
+-rw-r--r--   0        0        0     1973 2023-06-15 21:31:07.938752 lassen-0.2.1/lassen/tests/__pycache__/conftest.cpython-310-pytest-7.3.1.pyc
+-rw-r--r--   0        0        0     1220 2023-06-06 23:14:20.991368 lassen-0.2.1/lassen/tests/__pycache__/fixtures.cpython-310.pyc
+-rw-r--r--   0        0        0     5734 2023-06-15 21:16:27.736953 lassen-0.2.1/lassen/tests/__pycache__/test_store.cpython-310-pytest-7.3.1.pyc
+-rw-r--r--   0        0        0     1901 2023-06-15 21:16:27.737091 lassen-0.2.1/lassen/tests/conftest.py
+-rw-r--r--   0        0        0        0 2023-06-15 21:16:27.737128 lassen-0.2.1/lassen/tests/datasets/__init__.py
+-rw-r--r--   0        0        0     2243 2023-06-15 22:42:38.547093 lassen-0.2.1/lassen/tests/datasets/test_dataset_helpers.py
+-rw-r--r--   0        0        0     1645 2023-06-15 22:26:02.923228 lassen-0.2.1/lassen/tests/datasets/test_pyarrow_schemas.py
+-rw-r--r--   0        0        0      176 2023-06-06 23:14:20.991801 lassen-0.2.1/lassen/tests/fixtures/__init__.py
+-rw-r--r--   0        0        0     1215 2023-07-22 17:00:28.391699 lassen-0.2.1/lassen/tests/fixtures/stubs/expected_schema.py
+-rw-r--r--   0        0        0     1013 2023-07-22 17:00:28.391801 lassen-0.2.1/lassen/tests/fixtures/stubs/expected_schema_public.py
+-rw-r--r--   0        0        0      989 2023-07-22 17:00:28.391909 lassen-0.2.1/lassen/tests/fixtures/stubs/expected_store.py
+-rw-r--r--   0        0        0     1095 2023-07-22 17:00:28.392269 lassen-0.2.1/lassen/tests/fixtures/stubs/fixtures.py
+-rw-r--r--   0        0        0      463 2023-06-06 23:14:20.991923 lassen-0.2.1/lassen/tests/fixtures/test_harness/README.md
+-rw-r--r--   0        0        0      311 2023-06-06 23:14:20.992056 lassen-0.2.1/lassen/tests/fixtures/test_harness/pyproject.toml
+-rw-r--r--   0        0        0        0 2023-06-06 23:14:20.992112 lassen-0.2.1/lassen/tests/fixtures/test_harness/test_harness/__init__.py
+-rw-r--r--   0        0        0      691 2023-06-06 23:14:20.992321 lassen-0.2.1/lassen/tests/fixtures/test_harness/test_harness/migrations/62bf8def9fb1_new_migration.py
+-rw-r--r--   0        0        0      653 2023-06-06 23:14:20.992456 lassen-0.2.1/lassen/tests/fixtures/test_harness/test_harness/migrations/96dbf6f6d068_add_name.py
+-rw-r--r--   0        0        0      217 2023-06-06 23:14:20.992593 lassen-0.2.1/lassen/tests/fixtures/test_harness/test_harness/models.py
+-rw-r--r--   0        0        0      461 2023-06-06 23:14:20.992727 lassen-0.2.1/lassen/tests/model_fixtures.py
+-rw-r--r--   0        0        0        0 2023-07-22 17:00:28.392359 lassen-0.2.1/lassen/tests/stubs/__init__.py
+-rw-r--r--   0        0        0        0 2023-07-22 17:00:28.392464 lassen-0.2.1/lassen/tests/stubs/generators/__init__.py
+-rw-r--r--   0        0        0     3828 2023-07-22 17:00:28.392630 lassen-0.2.1/lassen/tests/stubs/generators/test_common.py
+-rw-r--r--   0        0        0      712 2023-07-22 17:00:28.392845 lassen-0.2.1/lassen/tests/stubs/generators/test_schema.py
+-rw-r--r--   0        0        0     2671 2023-07-22 17:00:28.393035 lassen-0.2.1/lassen/tests/stubs/generators/test_store.py
+-rw-r--r--   0        0        0     2560 2023-07-22 17:00:28.393152 lassen-0.2.1/lassen/tests/stubs/test_generate.py
+-rw-r--r--   0        0        0     2252 2023-06-06 23:14:20.992858 lassen-0.2.1/lassen/tests/test_alembic.py
+-rw-r--r--   0        0        0     2842 2023-07-22 17:00:28.393357 lassen-0.2.1/lassen/tests/test_store.py
+-rw-r--r--   0        0        0     1423 2023-07-22 17:05:31.540805 lassen-0.2.1/pyproject.toml
+-rw-r--r--   0        0        0     4987 1970-01-01 00:00:00.000000 lassen-0.2.1/setup.py
+-rw-r--r--   0        0        0     4129 1970-01-01 00:00:00.000000 lassen-0.2.1/PKG-INFO
```

### Comparing `lassen-0.2.0/LICENSE` & `lassen-0.2.1/LICENSE`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/README.md` & `lassen-0.2.1/README.md`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/alembic/cli.py` & `lassen-0.2.1/lassen/alembic/cli.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/alembic/io.py` & `lassen-0.2.1/lassen/alembic/io.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/alembic/runner.py` & `lassen-0.2.1/lassen/alembic/runner.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/assets/alembic.ini` & `lassen-0.2.1/lassen/assets/alembic.ini`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/core/__pycache__/config.cpython-310.pyc` & `lassen-0.2.1/lassen/core/__pycache__/config.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/core/config.py` & `lassen-0.2.1/lassen/core/config.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/datasets/dataset_helpers.py` & `lassen-0.2.1/lassen/datasets/dataset_helpers.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/datasets/pyarrow_schemas.py` & `lassen-0.2.1/lassen/datasets/pyarrow_schemas.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/db/__pycache__/base_class.cpython-310.pyc` & `lassen-0.2.1/lassen/db/__pycache__/base_class.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/db/__pycache__/base_class.cpython-311.pyc` & `lassen-0.2.1/lassen/db/__pycache__/base_class.cpython-311.pyc`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/db/__pycache__/session.cpython-310.pyc` & `lassen-0.2.1/lassen/db/__pycache__/session.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/db/__pycache__/session.cpython-311.pyc` & `lassen-0.2.1/lassen/db/__pycache__/session.cpython-311.pyc`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/db/base_class.py` & `lassen-0.2.1/lassen/db/base_class.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/db/session.py` & `lassen-0.2.1/lassen/db/session.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/io.py` & `lassen-0.2.1/lassen/io.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/store.py` & `lassen-0.2.1/lassen/store.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/stubs/base.py` & `lassen-0.2.1/lassen/stubs/base.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/stubs/field.py` & `lassen-0.2.1/lassen/stubs/field.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/stubs/generate.py` & `lassen-0.2.1/lassen/stubs/generate.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/stubs/generators/common.py` & `lassen-0.2.1/lassen/stubs/generators/common.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/stubs/generators/schema.py` & `lassen-0.2.1/lassen/stubs/generators/schema.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/stubs/generators/store.py` & `lassen-0.2.1/lassen/stubs/generators/store.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/stubs/templates/schema.py.j2` & `lassen-0.2.1/lassen/stubs/templates/schema.py.j2`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/stubs/templates/sqlalchemy.py.j2` & `lassen-0.2.1/lassen/stubs/templates/sqlalchemy.py.j2`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/tests/__pycache__/conftest.cpython-310-pytest-7.3.1.pyc` & `lassen-0.2.1/lassen/tests/__pycache__/conftest.cpython-310-pytest-7.3.1.pyc`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/tests/__pycache__/fixtures.cpython-310.pyc` & `lassen-0.2.1/lassen/tests/__pycache__/fixtures.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/tests/__pycache__/test_store.cpython-310-pytest-7.3.1.pyc` & `lassen-0.2.1/lassen/tests/__pycache__/test_store.cpython-310-pytest-7.3.1.pyc`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/tests/conftest.py` & `lassen-0.2.1/lassen/tests/conftest.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/tests/datasets/test_dataset_helpers.py` & `lassen-0.2.1/lassen/tests/datasets/test_dataset_helpers.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/tests/datasets/test_pyarrow_schemas.py` & `lassen-0.2.1/lassen/tests/datasets/test_pyarrow_schemas.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/tests/fixtures/stubs/expected_schema.py` & `lassen-0.2.1/lassen/tests/fixtures/stubs/expected_schema.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/tests/fixtures/stubs/expected_schema_public.py` & `lassen-0.2.1/lassen/tests/fixtures/stubs/expected_schema_public.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/tests/fixtures/stubs/expected_store.py` & `lassen-0.2.1/lassen/tests/fixtures/stubs/expected_store.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/tests/fixtures/stubs/fixtures.py` & `lassen-0.2.1/lassen/tests/fixtures/stubs/fixtures.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/tests/fixtures/test_harness/test_harness/migrations/62bf8def9fb1_new_migration.py` & `lassen-0.2.1/lassen/tests/fixtures/test_harness/test_harness/migrations/62bf8def9fb1_new_migration.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/tests/fixtures/test_harness/test_harness/migrations/96dbf6f6d068_add_name.py` & `lassen-0.2.1/lassen/tests/fixtures/test_harness/test_harness/migrations/96dbf6f6d068_add_name.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/tests/stubs/generators/test_common.py` & `lassen-0.2.1/lassen/tests/stubs/generators/test_common.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/tests/stubs/generators/test_schema.py` & `lassen-0.2.1/lassen/tests/stubs/generators/test_schema.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/tests/stubs/generators/test_store.py` & `lassen-0.2.1/lassen/tests/stubs/generators/test_store.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/tests/stubs/test_generate.py` & `lassen-0.2.1/lassen/tests/stubs/test_generate.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/tests/test_alembic.py` & `lassen-0.2.1/lassen/tests/test_alembic.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/lassen/tests/test_store.py` & `lassen-0.2.1/lassen/tests/test_store.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.0/pyproject.toml` & `lassen-0.2.1/pyproject.toml`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "lassen"
-version = "0.2.0"
+version = "0.2.1"
 description = "Common webapp scaffolding."
 authors = ["Pierce Freeman <pierce@freeman.vc>"]
 readme = "README.md"
 
 [tool.poetry.dependencies]
 python = "^3.11"
 fastapi = "^0.95.1"
```

### Comparing `lassen-0.2.0/setup.py` & `lassen-0.2.1/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -41,15 +41,15 @@
 
 entry_points = \
 {'console_scripts': ['generate-lassen = lassen.stubs.generate:cli',
                      'migrate = lassen.alembic.cli:main']}
 
 setup_kwargs = {
     'name': 'lassen',
-    'version': '0.2.0',
+    'version': '0.2.1',
     'description': 'Common webapp scaffolding.',
     'long_description': '# lassen\n\n**40.4881° N, 121.5049° W**\n\nCore utilities for MonkeySee web applications.\n\nNot guaranteed to be backwards compatible, use at your own risk.\n\n## Structure\n\n**Stores:** Each datamodel is expected to have its own store. Base classes that provide standard logic are provided by `lassen.store`\n- StoreBase: Base class for all stores\n- StoreFilterMixin: Mixin for filtering stores that specify an additional schema to use to filter\n\n**Schemas:** Each datamodel should define a Model class (SQLAlchemy base object) and a series of Schema objects (Pydantic) that allow the Store to serialize the models. These schemas are also often used for direct CRUD referencing in the API layer.\n\nWe use a base `Stub` file to generate these schemas from a centralized definition.\n\n```bash\npoetry run generate-lassen\n```\n\n**Datasets:** Optional huggingface `datasets` processing utilities. Only installed under the `lassen[datasets]` extra. These provide support for:\n\n- batch_to_examples: Iterate and manipulate each example separately, versus over nested key-based lists.\n- examples_to_batch: Takes the output of a typehinted element-wise batch and converts into the format needed for dataset insertion. If datasets can\'t automatically interpret the type of the fields, also provide automatic casting based on the typehinted dataclass.\n\n```python\nfrom lassen.datasets import batch_to_examples, examples_to_batch\nimport pandas as pd\n\n@dataclass\nclass BatchInsertion:\n    texts: list[str]\n\ndef batch_process(examples):\n    new_examples : list[BatchInsertion] = []\n    for example in batch_to_examples(examples):\n        new_examples.append(\n            BatchInsertion(\n                example["raw_text"].split()\n            )\n        )\n\n    # datasets won\'t be able to typehint a dataset that starts with an empty example, so we use our explicit schema to cast the data\n    return examples_to_batch(new_examples, BatchInsertion, explicit_schema=True)\n\ndf = pd.DataFrame(\n    [\n        {"raw_text": ""},\n        {"raw_text": "This is a test"},\n        {"raw_text": "This is another test"},\n    ]\n)\n\ndataset = Dataset.from_pandas(df)\n\ndataset = dataset.map(\n    batch_process,\n    batched=True,\n    batch_size=1,\n    num_proc=1,\n    remove_columns=dataset.column_names,\n)\n```\n\n**Migrations:** Lassen includes a templated alembic.init and env.py file. Client applications just need to have a `migrations` folder within their project root. After this you can swap `poetry run alembic` with `poetry run migrate`.\n\n```sh\npoetry run migrate upgrade head\n```\n\n**Settings:** Application settings should subclass our core settings. This provides a standard way to load settings from environment variables and includes common database keys.\n\n```python\nfrom lassen.core.config import CoreSettings, register_settings\n\n@register_settings\nclass ClientSettings(CoreSettings):\n    pass\n```\n\n**Schemas:** For helper schemas when returning results via API, see [lassen.schema](./lassen/schema.py).\n\n## Development\n\n```sh\npoetry install --extras "datasets"\n\ncreateuser lassen\ncreatedb -O lassen lassen_db\ncreatedb -O lassen lassen_test_db\n```\n\nUnit Tests:\n\n```sh\npoetry run pytest\n```\n',
     'author': 'Pierce Freeman',
     'author_email': 'pierce@freeman.vc',
     'maintainer': 'None',
     'maintainer_email': 'None',
     'url': 'None',
```

### Comparing `lassen-0.2.0/PKG-INFO` & `lassen-0.2.1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: lassen
-Version: 0.2.0
+Version: 0.2.1
 Summary: Common webapp scaffolding.
 Author: Pierce Freeman
 Author-email: pierce@freeman.vc
 Requires-Python: >=3.11,<4.0
 Classifier: Programming Language :: Python :: 3
 Provides-Extra: database
 Provides-Extra: datasets
```

