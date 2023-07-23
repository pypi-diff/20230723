# Comparing `tmp/lassen-0.2.2.tar.gz` & `tmp/lassen-0.2.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "lassen-0.2.2.tar", max compression
+gzip compressed data, was "lassen-0.2.3.tar", max compression
```

## Comparing `lassen-0.2.2.tar` & `lassen-0.2.3.tar`

### file list

```diff
@@ -1,78 +1,78 @@
--rw-r--r--   0        0        0     1071 2023-06-06 18:13:43.336753 lassen-0.2.2/LICENSE
--rw-r--r--   0        0        0     3159 2023-07-22 17:00:28.388296 lassen-0.2.2/README.md
--rw-r--r--   0        0        0        0 2023-06-06 23:14:20.986429 lassen-0.2.2/lassen/__init__.py
--rw-r--r--   0        0        0        0 2023-06-06 23:14:20.986933 lassen-0.2.2/lassen/alembic/__init__.py
--rw-r--r--   0        0        0     3685 2023-06-06 23:14:20.987092 lassen-0.2.2/lassen/alembic/cli.py
--rw-r--r--   0        0        0     2839 2023-07-22 17:00:28.388594 lassen-0.2.2/lassen/alembic/io.py
--rw-r--r--   0        0        0     1043 2023-06-06 23:14:20.987305 lassen-0.2.2/lassen/alembic/runner.py
--rw-r--r--   0        0        0      174 2023-06-06 23:14:20.987414 lassen-0.2.2/lassen/assets/__init__.py
--rw-r--r--   0        0        0     1592 2023-06-06 23:14:20.987525 lassen-0.2.2/lassen/assets/alembic.ini
--rw-r--r--   0        0        0      494 2023-06-06 23:14:20.987634 lassen-0.2.2/lassen/assets/script.py.mako
--rw-r--r--   0        0        0        0 2023-06-06 23:14:20.987697 lassen-0.2.2/lassen/core/__init__.py
--rw-r--r--   0        0        0      153 2023-06-15 21:16:27.734730 lassen-0.2.2/lassen/core/__pycache__/__init__.cpython-310.pyc
--rw-r--r--   0        0        0     2487 2023-06-15 21:16:27.734981 lassen-0.2.2/lassen/core/__pycache__/config.cpython-310.pyc
--rw-r--r--   0        0        0     1862 2023-06-06 23:14:20.988497 lassen-0.2.2/lassen/core/config.py
--rw-r--r--   0        0        0        0 2023-06-15 21:16:27.735020 lassen-0.2.2/lassen/datasets/__init__.py
--rw-r--r--   0        0        0     2368 2023-06-15 22:39:22.170659 lassen-0.2.2/lassen/datasets/dataset_helpers.py
--rw-r--r--   0        0        0     3024 2023-06-15 22:26:02.922940 lassen-0.2.2/lassen/datasets/pyarrow_schemas.py
--rw-r--r--   0        0        0      240 2023-06-06 23:14:20.988685 lassen-0.2.2/lassen/db/__init__.py
--rw-r--r--   0        0        0      396 2023-06-15 21:16:27.735607 lassen-0.2.2/lassen/db/__pycache__/__init__.cpython-310.pyc
--rw-r--r--   0        0        0      422 2023-07-22 17:00:28.388869 lassen-0.2.2/lassen/db/__pycache__/__init__.cpython-311.pyc
--rw-r--r--   0        0        0      147 2023-06-06 23:14:20.989285 lassen-0.2.2/lassen/db/__pycache__/base.cpython-310.pyc
--rw-r--r--   0        0        0      293 2023-06-06 23:14:20.989436 lassen-0.2.2/lassen/db/__pycache__/base.cpython-311.pyc
--rw-r--r--   0        0        0     1931 2023-06-15 21:16:27.735885 lassen-0.2.2/lassen/db/__pycache__/base_class.cpython-310.pyc
--rw-r--r--   0        0        0     2976 2023-07-23 15:10:32.420348 lassen-0.2.2/lassen/db/__pycache__/base_class.cpython-311.pyc
--rw-r--r--   0        0        0      839 2023-06-15 21:16:27.736092 lassen-0.2.2/lassen/db/__pycache__/session.cpython-310.pyc
--rw-r--r--   0        0        0     1296 2023-07-22 17:00:28.389524 lassen-0.2.2/lassen/db/__pycache__/session.cpython-311.pyc
--rw-r--r--   0        0        0     1920 2023-07-22 17:00:28.389828 lassen-0.2.2/lassen/db/base_class.py
--rw-r--r--   0        0        0      627 2023-06-06 23:14:20.990409 lassen-0.2.2/lassen/db/session.py
--rw-r--r--   0        0        0      140 2023-07-23 15:10:32.420873 lassen-0.2.2/lassen/enums.py
--rw-r--r--   0        0        0     1272 2023-07-22 17:00:28.389917 lassen-0.2.2/lassen/io.py
--rw-r--r--   0        0        0        0 2023-07-22 17:05:14.900856 lassen-0.2.2/lassen/py.typed
--rw-r--r--   0        0        0      210 2023-06-06 23:14:20.990522 lassen-0.2.2/lassen/schema.py
--rw-r--r--   0        0        0      227 2023-06-15 21:16:27.736193 lassen-0.2.2/lassen/shared.py
--rw-r--r--   0        0        0    10197 2023-07-23 15:10:32.421293 lassen-0.2.2/lassen/store.py
--rw-r--r--   0        0        0      201 2023-07-22 17:00:28.390303 lassen-0.2.2/lassen/stubs/__init__.py
--rw-r--r--   0        0        0     1294 2023-07-23 15:10:32.421607 lassen-0.2.2/lassen/stubs/base.py
--rw-r--r--   0        0        0      147 2023-07-23 04:25:54.115562 lassen-0.2.2/lassen/stubs/definition.py
--rw-r--r--   0        0        0     2352 2023-07-23 15:10:32.422041 lassen-0.2.2/lassen/stubs/field.py
--rw-r--r--   0        0        0     3814 2023-07-23 15:10:32.422479 lassen-0.2.2/lassen/stubs/generate.py
--rw-r--r--   0        0        0       96 2023-07-22 17:00:28.390790 lassen-0.2.2/lassen/stubs/generators/__init__.py
--rw-r--r--   0        0        0     8882 2023-07-23 15:10:32.422744 lassen-0.2.2/lassen/stubs/generators/common.py
--rw-r--r--   0        0        0     7668 2023-07-23 15:10:32.423020 lassen-0.2.2/lassen/stubs/generators/schema.py
--rw-r--r--   0        0        0    12169 2023-07-23 15:10:32.423410 lassen-0.2.2/lassen/stubs/generators/store.py
--rw-r--r--   0        0        0      177 2023-07-22 17:00:28.391343 lassen-0.2.2/lassen/stubs/templates/__init__.py
--rw-r--r--   0        0        0     1052 2023-07-22 17:00:28.391457 lassen-0.2.2/lassen/stubs/templates/schema.py.j2
--rw-r--r--   0        0        0      551 2023-07-22 17:00:28.391564 lassen-0.2.2/lassen/stubs/templates/sqlalchemy.py.j2
--rw-r--r--   0        0        0        0 2023-06-06 23:14:20.990727 lassen-0.2.2/lassen/tests/__init__.py
--rw-r--r--   0        0        0      154 2023-06-15 21:16:27.736415 lassen-0.2.2/lassen/tests/__pycache__/__init__.cpython-310.pyc
--rw-r--r--   0        0        0     1973 2023-06-15 21:31:07.938752 lassen-0.2.2/lassen/tests/__pycache__/conftest.cpython-310-pytest-7.3.1.pyc
--rw-r--r--   0        0        0     1220 2023-06-06 23:14:20.991368 lassen-0.2.2/lassen/tests/__pycache__/fixtures.cpython-310.pyc
--rw-r--r--   0        0        0     5734 2023-06-15 21:16:27.736953 lassen-0.2.2/lassen/tests/__pycache__/test_store.cpython-310-pytest-7.3.1.pyc
--rw-r--r--   0        0        0     1901 2023-06-15 21:16:27.737091 lassen-0.2.2/lassen/tests/conftest.py
--rw-r--r--   0        0        0        0 2023-06-15 21:16:27.737128 lassen-0.2.2/lassen/tests/datasets/__init__.py
--rw-r--r--   0        0        0     2243 2023-06-15 22:42:38.547093 lassen-0.2.2/lassen/tests/datasets/test_dataset_helpers.py
--rw-r--r--   0        0        0     1645 2023-06-15 22:26:02.923228 lassen-0.2.2/lassen/tests/datasets/test_pyarrow_schemas.py
--rw-r--r--   0        0        0      176 2023-06-06 23:14:20.991801 lassen-0.2.2/lassen/tests/fixtures/__init__.py
--rw-r--r--   0        0        0     1085 2023-07-23 15:10:32.423935 lassen-0.2.2/lassen/tests/fixtures/stubs/expected_schema.py
--rw-r--r--   0        0        0      883 2023-07-23 15:10:32.424349 lassen-0.2.2/lassen/tests/fixtures/stubs/expected_schema_public.py
--rw-r--r--   0        0        0      845 2023-07-23 15:10:32.424772 lassen-0.2.2/lassen/tests/fixtures/stubs/expected_store.py
--rw-r--r--   0        0        0     1095 2023-07-22 17:00:28.392269 lassen-0.2.2/lassen/tests/fixtures/stubs/fixtures.py
--rw-r--r--   0        0        0      463 2023-06-06 23:14:20.991923 lassen-0.2.2/lassen/tests/fixtures/test_harness/README.md
--rw-r--r--   0        0        0      311 2023-06-06 23:14:20.992056 lassen-0.2.2/lassen/tests/fixtures/test_harness/pyproject.toml
--rw-r--r--   0        0        0        0 2023-06-06 23:14:20.992112 lassen-0.2.2/lassen/tests/fixtures/test_harness/test_harness/__init__.py
--rw-r--r--   0        0        0      691 2023-06-06 23:14:20.992321 lassen-0.2.2/lassen/tests/fixtures/test_harness/test_harness/migrations/62bf8def9fb1_new_migration.py
--rw-r--r--   0        0        0      653 2023-06-06 23:14:20.992456 lassen-0.2.2/lassen/tests/fixtures/test_harness/test_harness/migrations/96dbf6f6d068_add_name.py
--rw-r--r--   0        0        0      217 2023-06-06 23:14:20.992593 lassen-0.2.2/lassen/tests/fixtures/test_harness/test_harness/models.py
--rw-r--r--   0        0        0      521 2023-07-23 15:10:32.425116 lassen-0.2.2/lassen/tests/model_fixtures.py
--rw-r--r--   0        0        0        0 2023-07-22 17:00:28.392359 lassen-0.2.2/lassen/tests/stubs/__init__.py
--rw-r--r--   0        0        0        0 2023-07-22 17:00:28.392464 lassen-0.2.2/lassen/tests/stubs/generators/__init__.py
--rw-r--r--   0        0        0     3627 2023-07-23 15:10:32.425519 lassen-0.2.2/lassen/tests/stubs/generators/test_common.py
--rw-r--r--   0        0        0     1221 2023-07-23 15:10:32.425828 lassen-0.2.2/lassen/tests/stubs/generators/test_schema.py
--rw-r--r--   0        0        0     2684 2023-07-23 15:10:32.426087 lassen-0.2.2/lassen/tests/stubs/generators/test_store.py
--rw-r--r--   0        0        0     2560 2023-07-22 17:00:28.393152 lassen-0.2.2/lassen/tests/stubs/test_generate.py
--rw-r--r--   0        0        0     2252 2023-06-06 23:14:20.992858 lassen-0.2.2/lassen/tests/test_alembic.py
--rw-r--r--   0        0        0     3060 2023-07-23 15:10:32.426427 lassen-0.2.2/lassen/tests/test_store.py
--rw-r--r--   0        0        0     1423 2023-07-23 15:10:37.718992 lassen-0.2.2/pyproject.toml
--rw-r--r--   0        0        0     4987 1970-01-01 00:00:00.000000 lassen-0.2.2/setup.py
--rw-r--r--   0        0        0     4129 1970-01-01 00:00:00.000000 lassen-0.2.2/PKG-INFO
+-rw-r--r--   0        0        0     1071 2023-06-06 18:13:43.336753 lassen-0.2.3/LICENSE
+-rw-r--r--   0        0        0     3418 2023-07-23 17:12:41.829570 lassen-0.2.3/README.md
+-rw-r--r--   0        0        0        0 2023-06-06 23:14:20.986429 lassen-0.2.3/lassen/__init__.py
+-rw-r--r--   0        0        0        0 2023-06-06 23:14:20.986933 lassen-0.2.3/lassen/alembic/__init__.py
+-rw-r--r--   0        0        0     3685 2023-06-06 23:14:20.987092 lassen-0.2.3/lassen/alembic/cli.py
+-rw-r--r--   0        0        0     2839 2023-07-22 17:00:28.388594 lassen-0.2.3/lassen/alembic/io.py
+-rw-r--r--   0        0        0     1043 2023-06-06 23:14:20.987305 lassen-0.2.3/lassen/alembic/runner.py
+-rw-r--r--   0        0        0      174 2023-06-06 23:14:20.987414 lassen-0.2.3/lassen/assets/__init__.py
+-rw-r--r--   0        0        0     1592 2023-06-06 23:14:20.987525 lassen-0.2.3/lassen/assets/alembic.ini
+-rw-r--r--   0        0        0      494 2023-06-06 23:14:20.987634 lassen-0.2.3/lassen/assets/script.py.mako
+-rw-r--r--   0        0        0        0 2023-06-06 23:14:20.987697 lassen-0.2.3/lassen/core/__init__.py
+-rw-r--r--   0        0        0      153 2023-06-15 21:16:27.734730 lassen-0.2.3/lassen/core/__pycache__/__init__.cpython-310.pyc
+-rw-r--r--   0        0        0     2487 2023-06-15 21:16:27.734981 lassen-0.2.3/lassen/core/__pycache__/config.cpython-310.pyc
+-rw-r--r--   0        0        0     1862 2023-06-06 23:14:20.988497 lassen-0.2.3/lassen/core/config.py
+-rw-r--r--   0        0        0        0 2023-06-15 21:16:27.735020 lassen-0.2.3/lassen/datasets/__init__.py
+-rw-r--r--   0        0        0     2368 2023-06-15 22:39:22.170659 lassen-0.2.3/lassen/datasets/dataset_helpers.py
+-rw-r--r--   0        0        0     3024 2023-06-15 22:26:02.922940 lassen-0.2.3/lassen/datasets/pyarrow_schemas.py
+-rw-r--r--   0        0        0      240 2023-06-06 23:14:20.988685 lassen-0.2.3/lassen/db/__init__.py
+-rw-r--r--   0        0        0      396 2023-06-15 21:16:27.735607 lassen-0.2.3/lassen/db/__pycache__/__init__.cpython-310.pyc
+-rw-r--r--   0        0        0      422 2023-07-22 17:00:28.388869 lassen-0.2.3/lassen/db/__pycache__/__init__.cpython-311.pyc
+-rw-r--r--   0        0        0      147 2023-06-06 23:14:20.989285 lassen-0.2.3/lassen/db/__pycache__/base.cpython-310.pyc
+-rw-r--r--   0        0        0      293 2023-06-06 23:14:20.989436 lassen-0.2.3/lassen/db/__pycache__/base.cpython-311.pyc
+-rw-r--r--   0        0        0     1931 2023-06-15 21:16:27.735885 lassen-0.2.3/lassen/db/__pycache__/base_class.cpython-310.pyc
+-rw-r--r--   0        0        0     2138 2023-07-23 15:46:35.701193 lassen-0.2.3/lassen/db/__pycache__/base_class.cpython-311.pyc
+-rw-r--r--   0        0        0      839 2023-06-15 21:16:27.736092 lassen-0.2.3/lassen/db/__pycache__/session.cpython-310.pyc
+-rw-r--r--   0        0        0     1296 2023-07-22 17:00:28.389524 lassen-0.2.3/lassen/db/__pycache__/session.cpython-311.pyc
+-rw-r--r--   0        0        0     1437 2023-07-23 15:46:28.626071 lassen-0.2.3/lassen/db/base_class.py
+-rw-r--r--   0        0        0      627 2023-06-06 23:14:20.990409 lassen-0.2.3/lassen/db/session.py
+-rw-r--r--   0        0        0      140 2023-07-23 15:10:32.420873 lassen-0.2.3/lassen/enums.py
+-rw-r--r--   0        0        0     1272 2023-07-22 17:00:28.389917 lassen-0.2.3/lassen/io.py
+-rw-r--r--   0        0        0        0 2023-07-22 17:05:14.900856 lassen-0.2.3/lassen/py.typed
+-rw-r--r--   0        0        0      210 2023-06-06 23:14:20.990522 lassen-0.2.3/lassen/schema.py
+-rw-r--r--   0        0        0      227 2023-06-15 21:16:27.736193 lassen-0.2.3/lassen/shared.py
+-rw-r--r--   0        0        0    10197 2023-07-23 15:10:32.421293 lassen-0.2.3/lassen/store.py
+-rw-r--r--   0        0        0      201 2023-07-22 17:00:28.390303 lassen-0.2.3/lassen/stubs/__init__.py
+-rw-r--r--   0        0        0     1294 2023-07-23 15:10:32.421607 lassen-0.2.3/lassen/stubs/base.py
+-rw-r--r--   0        0        0      147 2023-07-23 04:25:54.115562 lassen-0.2.3/lassen/stubs/definition.py
+-rw-r--r--   0        0        0     2352 2023-07-23 15:10:32.422041 lassen-0.2.3/lassen/stubs/field.py
+-rw-r--r--   0        0        0     4086 2023-07-23 17:13:39.305496 lassen-0.2.3/lassen/stubs/generate.py
+-rw-r--r--   0        0        0       96 2023-07-22 17:00:28.390790 lassen-0.2.3/lassen/stubs/generators/__init__.py
+-rw-r--r--   0        0        0     9321 2023-07-23 17:11:00.299172 lassen-0.2.3/lassen/stubs/generators/common.py
+-rw-r--r--   0        0        0     7971 2023-07-23 17:07:05.791417 lassen-0.2.3/lassen/stubs/generators/schema.py
+-rw-r--r--   0        0        0    12377 2023-07-23 15:46:11.505933 lassen-0.2.3/lassen/stubs/generators/store.py
+-rw-r--r--   0        0        0      177 2023-07-22 17:00:28.391343 lassen-0.2.3/lassen/stubs/templates/__init__.py
+-rw-r--r--   0        0        0     1052 2023-07-22 17:00:28.391457 lassen-0.2.3/lassen/stubs/templates/schema.py.j2
+-rw-r--r--   0        0        0      591 2023-07-23 15:31:38.606138 lassen-0.2.3/lassen/stubs/templates/sqlalchemy.py.j2
+-rw-r--r--   0        0        0        0 2023-06-06 23:14:20.990727 lassen-0.2.3/lassen/tests/__init__.py
+-rw-r--r--   0        0        0      154 2023-06-15 21:16:27.736415 lassen-0.2.3/lassen/tests/__pycache__/__init__.cpython-310.pyc
+-rw-r--r--   0        0        0     1973 2023-06-15 21:31:07.938752 lassen-0.2.3/lassen/tests/__pycache__/conftest.cpython-310-pytest-7.3.1.pyc
+-rw-r--r--   0        0        0     1220 2023-06-06 23:14:20.991368 lassen-0.2.3/lassen/tests/__pycache__/fixtures.cpython-310.pyc
+-rw-r--r--   0        0        0     5734 2023-06-15 21:16:27.736953 lassen-0.2.3/lassen/tests/__pycache__/test_store.cpython-310-pytest-7.3.1.pyc
+-rw-r--r--   0        0        0     1901 2023-06-15 21:16:27.737091 lassen-0.2.3/lassen/tests/conftest.py
+-rw-r--r--   0        0        0        0 2023-06-15 21:16:27.737128 lassen-0.2.3/lassen/tests/datasets/__init__.py
+-rw-r--r--   0        0        0     2243 2023-06-15 22:42:38.547093 lassen-0.2.3/lassen/tests/datasets/test_dataset_helpers.py
+-rw-r--r--   0        0        0     1645 2023-06-15 22:26:02.923228 lassen-0.2.3/lassen/tests/datasets/test_pyarrow_schemas.py
+-rw-r--r--   0        0        0      176 2023-06-06 23:14:20.991801 lassen-0.2.3/lassen/tests/fixtures/__init__.py
+-rw-r--r--   0        0        0     1142 2023-07-23 17:16:33.689781 lassen-0.2.3/lassen/tests/fixtures/stubs/expected_schema.py
+-rw-r--r--   0        0        0      922 2023-07-23 16:15:31.377386 lassen-0.2.3/lassen/tests/fixtures/stubs/expected_schema_public.py
+-rw-r--r--   0        0        0      926 2023-07-23 17:16:21.722018 lassen-0.2.3/lassen/tests/fixtures/stubs/expected_store.py
+-rw-r--r--   0        0        0     1095 2023-07-23 17:16:09.670204 lassen-0.2.3/lassen/tests/fixtures/stubs/fixtures.py
+-rw-r--r--   0        0        0      463 2023-06-06 23:14:20.991923 lassen-0.2.3/lassen/tests/fixtures/test_harness/README.md
+-rw-r--r--   0        0        0      311 2023-06-06 23:14:20.992056 lassen-0.2.3/lassen/tests/fixtures/test_harness/pyproject.toml
+-rw-r--r--   0        0        0        0 2023-06-06 23:14:20.992112 lassen-0.2.3/lassen/tests/fixtures/test_harness/test_harness/__init__.py
+-rw-r--r--   0        0        0      691 2023-06-06 23:14:20.992321 lassen-0.2.3/lassen/tests/fixtures/test_harness/test_harness/migrations/62bf8def9fb1_new_migration.py
+-rw-r--r--   0        0        0      653 2023-06-06 23:14:20.992456 lassen-0.2.3/lassen/tests/fixtures/test_harness/test_harness/migrations/96dbf6f6d068_add_name.py
+-rw-r--r--   0        0        0      217 2023-06-06 23:14:20.992593 lassen-0.2.3/lassen/tests/fixtures/test_harness/test_harness/models.py
+-rw-r--r--   0        0        0      521 2023-07-23 15:10:32.425116 lassen-0.2.3/lassen/tests/model_fixtures.py
+-rw-r--r--   0        0        0        0 2023-07-22 17:00:28.392359 lassen-0.2.3/lassen/tests/stubs/__init__.py
+-rw-r--r--   0        0        0        0 2023-07-22 17:00:28.392464 lassen-0.2.3/lassen/tests/stubs/generators/__init__.py
+-rw-r--r--   0        0        0     3649 2023-07-23 17:15:13.423972 lassen-0.2.3/lassen/tests/stubs/generators/test_common.py
+-rw-r--r--   0        0        0     1221 2023-07-23 15:10:32.425828 lassen-0.2.3/lassen/tests/stubs/generators/test_schema.py
+-rw-r--r--   0        0        0     2703 2023-07-23 15:43:10.932915 lassen-0.2.3/lassen/tests/stubs/generators/test_store.py
+-rw-r--r--   0        0        0     2560 2023-07-22 17:00:28.393152 lassen-0.2.3/lassen/tests/stubs/test_generate.py
+-rw-r--r--   0        0        0     2252 2023-06-06 23:14:20.992858 lassen-0.2.3/lassen/tests/test_alembic.py
+-rw-r--r--   0        0        0     3060 2023-07-23 15:10:32.426427 lassen-0.2.3/lassen/tests/test_store.py
+-rw-r--r--   0        0        0     1423 2023-07-23 17:17:17.817251 lassen-0.2.3/pyproject.toml
+-rw-r--r--   0        0        0     5251 1970-01-01 00:00:00.000000 lassen-0.2.3/setup.py
+-rw-r--r--   0        0        0     4388 1970-01-01 00:00:00.000000 lassen-0.2.3/PKG-INFO
```

### Comparing `lassen-0.2.2/LICENSE` & `lassen-0.2.3/LICENSE`

 * *Files identical despite different names*

### Comparing `lassen-0.2.2/README.md` & `lassen-0.2.3/README.md`

 * *Files 14% similar despite different names*

```diff
@@ -10,15 +10,20 @@
 
 **Stores:** Each datamodel is expected to have its own store. Base classes that provide standard logic are provided by `lassen.store`
 - StoreBase: Base class for all stores
 - StoreFilterMixin: Mixin for filtering stores that specify an additional schema to use to filter
 
 **Schemas:** Each datamodel should define a Model class (SQLAlchemy base object) and a series of Schema objects (Pydantic) that allow the Store to serialize the models. These schemas are also often used for direct CRUD referencing in the API layer.
 
-We use a base `Stub` file to generate these schemas from a centralized definition.
+We use a base `Stub` file to generate these schemas from a centralized definition. When defining generators you should use a path that can be fully managed by lassen, since we will remove and regenerate these files on each run.
+
+```python
+STORE_GENERATOR = StoreGenerator("models/auto")
+SCHEMA_GENERATOR = SchemaGenerator("schemas/auto")
+```
 
 ```bash
 poetry run generate-lassen
 ```
 
 **Datasets:** Optional huggingface `datasets` processing utilities. Only installed under the `lassen[datasets]` extra. These provide support for:
```

### Comparing `lassen-0.2.2/lassen/alembic/cli.py` & `lassen-0.2.3/lassen/alembic/cli.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.2/lassen/alembic/io.py` & `lassen-0.2.3/lassen/alembic/io.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.2/lassen/alembic/runner.py` & `lassen-0.2.3/lassen/alembic/runner.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.2/lassen/assets/alembic.ini` & `lassen-0.2.3/lassen/assets/alembic.ini`

 * *Files identical despite different names*

### Comparing `lassen-0.2.2/lassen/core/__pycache__/config.cpython-310.pyc` & `lassen-0.2.3/lassen/core/__pycache__/config.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `lassen-0.2.2/lassen/core/config.py` & `lassen-0.2.3/lassen/core/config.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.2/lassen/datasets/dataset_helpers.py` & `lassen-0.2.3/lassen/datasets/dataset_helpers.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.2/lassen/datasets/pyarrow_schemas.py` & `lassen-0.2.3/lassen/datasets/pyarrow_schemas.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.2/lassen/db/__pycache__/base_class.cpython-310.pyc` & `lassen-0.2.3/lassen/db/__pycache__/base_class.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `lassen-0.2.2/lassen/db/__pycache__/base_class.cpython-311.pyc` & `lassen-0.2.3/lassen/db/__pycache__/base_class.cpython-311.pyc`

 * *Files 24% similar despite different names*

#### Python bytecode

```diff
@@ -1,228 +1,103 @@
 magic:    0xa70d0d0a
-moddate:  0x2c0bbc64 (Sat Jul 22 17:00:28 2023 UTC)
-files sz: 1920
+moddate:  0x544bbd64 (Sun Jul 23 15:46:28 2023 UTC)
+files sz: 1437
 code
    argcount  : 0
    nlocals   : 0
    stacksize : 5
    flags     : 0
    code
-      0x9700640064016c006d015a010100640064026c026d035a030100640064
-      036c046d055a056d065a066d075a076d085a080100640064046c096d0a5a
-      0a6d0b5a0b6d0c5a0c6d0d5a0d6d0e5a0e6d0f5a0f0100650d0200470064
-      0584006406a6020000ab020000000000000000a6000000ab000000000000
-      0000005a1002004700640784006408a6020000ab0200000000000000005a
-      110200470064098400640a650aa6030000ab0300000000000000005a1202
-      0065076a130000000000000000650c640ba6020000ab0200000000000000
-      00640c8400a6000000ab0000000000000000005a14640d5300
+      0x9700640064016c006d015a016d025a026d035a036d045a040100640064
+      026c056d065a066d075a076d085a08010002004700640384006404a60200
+      00ab0200000000000000005a09020047006405840064066506a6030000ab
+      0300000000000000005a0a020065036a0b000000000000000065076407a6
+      020000ab02000000000000000064088400a6000000ab0000000000000000
+      005a0c64095300
      0           0 RESUME                   0
    
      1           2 LOAD_CONST               0 (0)
-                 4 LOAD_CONST               1 (('Any',))
-                 6 IMPORT_NAME              0 (typing)
-                 8 IMPORT_FROM              1 (Any)
-                10 STORE_NAME               1 (Any)
-                12 POP_TOP
-   
-     3          14 LOAD_CONST               0 (0)
-                16 LOAD_CONST               2 (('underscore',))
-                18 IMPORT_NAME              2 (inflection)
-                20 IMPORT_FROM              3 (underscore)
-                22 STORE_NAME               3 (underscore)
+                 4 LOAD_CONST               1 (('Boolean', 'Column', 'event', 'false'))
+                 6 IMPORT_NAME              0 (sqlalchemy)
+                 8 IMPORT_FROM              1 (Boolean)
+                10 STORE_NAME               1 (Boolean)
+                12 IMPORT_FROM              2 (Column)
+                14 STORE_NAME               2 (Column)
+                16 IMPORT_FROM              3 (event)
+                18 STORE_NAME               3 (event)
+                20 IMPORT_FROM              4 (false)
+                22 STORE_NAME               4 (false)
                 24 POP_TOP
    
-     4          26 LOAD_CONST               0 (0)
-                28 LOAD_CONST               3 (('Boolean', 'Column', 'event', 'false'))
-                30 IMPORT_NAME              4 (sqlalchemy)
-                32 IMPORT_FROM              5 (Boolean)
-                34 STORE_NAME               5 (Boolean)
-                36 IMPORT_FROM              6 (Column)
-                38 STORE_NAME               6 (Column)
-                40 IMPORT_FROM              7 (event)
-                42 STORE_NAME               7 (event)
-                44 IMPORT_FROM              8 (false)
-                46 STORE_NAME               8 (false)
-                48 POP_TOP
-   
-     5          50 LOAD_CONST               0 (0)
-                52 LOAD_CONST               4 (('DeclarativeBase', 'Mapped', 'Session', 'declarative_mixin', 'declared_attr', 'with_loader_criteria'))
-                54 IMPORT_NAME              9 (sqlalchemy.orm)
-                56 IMPORT_FROM             10 (DeclarativeBase)
-                58 STORE_NAME              10 (DeclarativeBase)
-                60 IMPORT_FROM             11 (Mapped)
-                62 STORE_NAME              11 (Mapped)
-                64 IMPORT_FROM             12 (Session)
-                66 STORE_NAME              12 (Session)
-                68 IMPORT_FROM             13 (declarative_mixin)
-                70 STORE_NAME              13 (declarative_mixin)
-                72 IMPORT_FROM             14 (declared_attr)
-                74 STORE_NAME              14 (declared_attr)
-                76 IMPORT_FROM             15 (with_loader_criteria)
-                78 STORE_NAME              15 (with_loader_criteria)
-                80 POP_TOP
-   
-    15          82 LOAD_NAME               13 (declarative_mixin)
-   
-    16          84 PUSH_NULL
-                86 LOAD_BUILD_CLASS
-                88 LOAD_CONST               5 (<code object MainMixin, file "/Users/piercefreeman/projects/lassen/lassen/db/base_class.py", line 15>)
-                90 MAKE_FUNCTION            0
-                92 LOAD_CONST               6 ('MainMixin')
-                94 PRECALL                  2
-                98 CALL                     2
-   
-    15         108 PRECALL                  0
-               112 CALL                     0
-   
-    16         122 STORE_NAME              16 (MainMixin)
-   
-    27         124 PUSH_NULL
-               126 LOAD_BUILD_CLASS
-               128 LOAD_CONST               7 (<code object ArchivedMixin, file "/Users/piercefreeman/projects/lassen/lassen/db/base_class.py", line 27>)
-               130 MAKE_FUNCTION            0
-               132 LOAD_CONST               8 ('ArchivedMixin')
-               134 PRECALL                  2
-               138 CALL                     2
-               148 STORE_NAME              17 (ArchivedMixin)
-   
-    31         150 PUSH_NULL
-               152 LOAD_BUILD_CLASS
-               154 LOAD_CONST               9 (<code object Base, file "/Users/piercefreeman/projects/lassen/lassen/db/base_class.py", line 31>)
-               156 MAKE_FUNCTION            0
-               158 LOAD_CONST              10 ('Base')
-               160 LOAD_NAME               10 (DeclarativeBase)
-               162 PRECALL                  3
-               166 CALL                     3
-               176 STORE_NAME              18 (Base)
-   
-    36         178 PUSH_NULL
-               180 LOAD_NAME                7 (event)
-               182 LOAD_ATTR               19 (listens_for)
-               192 LOAD_NAME               12 (Session)
-               194 LOAD_CONST              11 ('do_orm_execute')
-               196 PRECALL                  2
-               200 CALL                     2
-   
-    37         210 LOAD_CONST              12 (<code object _add_filtering_criteria, file "/Users/piercefreeman/projects/lassen/lassen/db/base_class.py", line 36>)
-               212 MAKE_FUNCTION            0
-   
-    36         214 PRECALL                  0
-               218 CALL                     0
-   
-    37         228 STORE_NAME              20 (_add_filtering_criteria)
-               230 LOAD_CONST              13 (None)
-               232 RETURN_VALUE
+     2          26 LOAD_CONST               0 (0)
+                28 LOAD_CONST               2 (('DeclarativeBase', 'Session', 'with_loader_criteria'))
+                30 IMPORT_NAME              5 (sqlalchemy.orm)
+                32 IMPORT_FROM              6 (DeclarativeBase)
+                34 STORE_NAME               6 (DeclarativeBase)
+                36 IMPORT_FROM              7 (Session)
+                38 STORE_NAME               7 (Session)
+                40 IMPORT_FROM              8 (with_loader_criteria)
+                42 STORE_NAME               8 (with_loader_criteria)
+                44 POP_TOP
+   
+     5          46 PUSH_NULL
+                48 LOAD_BUILD_CLASS
+                50 LOAD_CONST               3 (<code object ArchivedMixin, file "/Users/piercefreeman/projects/lassen/lassen/db/base_class.py", line 5>)
+                52 MAKE_FUNCTION            0
+                54 LOAD_CONST               4 ('ArchivedMixin')
+                56 PRECALL                  2
+                60 CALL                     2
+                70 STORE_NAME               9 (ArchivedMixin)
+   
+     9          72 PUSH_NULL
+                74 LOAD_BUILD_CLASS
+                76 LOAD_CONST               5 (<code object Base, file "/Users/piercefreeman/projects/lassen/lassen/db/base_class.py", line 9>)
+                78 MAKE_FUNCTION            0
+                80 LOAD_CONST               6 ('Base')
+                82 LOAD_NAME                6 (DeclarativeBase)
+                84 PRECALL                  3
+                88 CALL                     3
+                98 STORE_NAME              10 (Base)
+   
+    14         100 PUSH_NULL
+               102 LOAD_NAME                3 (event)
+               104 LOAD_ATTR               11 (listens_for)
+               114 LOAD_NAME                7 (Session)
+               116 LOAD_CONST               7 ('do_orm_execute')
+               118 PRECALL                  2
+               122 CALL                     2
+   
+    15         132 LOAD_CONST               8 (<code object _add_filtering_criteria, file "/Users/piercefreeman/projects/lassen/lassen/db/base_class.py", line 14>)
+               134 MAKE_FUNCTION            0
+   
+    14         136 PRECALL                  0
+               140 CALL                     0
+   
+    15         150 STORE_NAME              12 (_add_filtering_criteria)
+               152 LOAD_CONST               9 (None)
+               154 RETURN_VALUE
    consts
       0
-      ('Any',)
-      ('underscore',)
       ('Boolean', 'Column', 'event', 'false')
-      ('DeclarativeBase', 'Mapped', 'Session', 'declarative_mixin', 'declared_attr', 'with_loader_criteria')
-      code
-         argcount  : 0
-         nlocals   : 0
-         stacksize : 6
-         flags     : 0
-         code
-            0x970065005a0164005a0255006503650464013c0000006505650464023c
-            000000650664036400640465076505190000000000000000006604640584
-            04a6000000ab0000000000000000005a0864065300
-          15           0 RESUME                   0
-                       2 LOAD_NAME                0 (__name__)
-                       4 STORE_NAME               1 (__module__)
-                       6 LOAD_CONST               0 ('MainMixin')
-                       8 STORE_NAME               2 (__qualname__)
-                      10 SETUP_ANNOTATIONS
-         
-          17          12 LOAD_NAME                3 (Any)
-                      14 LOAD_NAME                4 (__annotations__)
-                      16 LOAD_CONST               1 ('id')
-                      18 STORE_SUBSCR
-         
-          18          22 LOAD_NAME                5 (str)
-                      24 LOAD_NAME                4 (__annotations__)
-                      26 LOAD_CONST               2 ('__name__')
-                      28 STORE_SUBSCR
-         
-          22          32 LOAD_NAME                6 (declared_attr)
-         
-          23          34 LOAD_CONST               3 ('cls')
-                      36 LOAD_CONST               0 ('MainMixin')
-                      38 LOAD_CONST               4 ('return')
-                      40 LOAD_NAME                7 (Mapped)
-                      42 LOAD_NAME                5 (str)
-                      44 BINARY_SUBSCR
-                      54 BUILD_TUPLE              4
-                      56 LOAD_CONST               5 (<code object __tablename__, file "/Users/piercefreeman/projects/lassen/lassen/db/base_class.py", line 22>)
-                      58 MAKE_FUNCTION            4 (annotations)
-         
-          22          60 PRECALL                  0
-                      64 CALL                     0
-         
-          23          74 STORE_NAME               8 (__tablename__)
-                      76 LOAD_CONST               6 (None)
-                      78 RETURN_VALUE
-         consts
-            'MainMixin'
-            'id'
-            '__name__'
-            'cls'
-            'return'
-            code
-               argcount  : 1
-               nlocals   : 1
-               stacksize : 3
-               flags     : 3
-               code
-                  0x97007401000000000000000000007c006a010000000000000000a60100
-                  00ab0100000000000000005300
-                22           0 RESUME                   0
-               
-                24           2 LOAD_GLOBAL              1 (NULL + underscore)
-                            14 LOAD_FAST                0 (cls)
-                            16 LOAD_ATTR                1 (__name__)
-                            26 PRECALL                  1
-                            30 CALL                     1
-                            40 RETURN_VALUE
-               consts
-                  None
-               names      ('underscore', '__name__')
-               varnames   ('cls',)
-               freevars   ()
-               cellvars   ()
-               filename   '/Users/piercefreeman/projects/lassen/lassen/db/base_class.py'
-               name       '__tablename__'
-               firstlineno 22
-               lnotab 0x0202
-            None
-         names      ('__name__', '__module__', '__qualname__', 'Any', '__annotations__', 'str', 'declared_attr', 'Mapped', '__tablename__')
-         varnames   ()
-         freevars   ()
-         cellvars   ()
-         filename   '/Users/piercefreeman/projects/lassen/lassen/db/base_class.py'
-         name       'MainMixin'
-         firstlineno 15
-         lnotab 0x0c020a010a0402011aff0e01
-      'MainMixin'
+      ('DeclarativeBase', 'Session', 'with_loader_criteria')
       code
          argcount  : 0
          nlocals   : 0
          stacksize : 5
          flags     : 0
          code
             0x970065005a0164005a0202006503650464016401ac02a6030000ab0300
             000000000000005a0564035300
-          27           0 RESUME                   0
+           5           0 RESUME                   0
                        2 LOAD_NAME                0 (__name__)
                        4 STORE_NAME               1 (__module__)
                        6 LOAD_CONST               0 ('ArchivedMixin')
                        8 STORE_NAME               2 (__qualname__)
          
-          28          10 PUSH_NULL
+           6          10 PUSH_NULL
                       12 LOAD_NAME                3 (Column)
                       14 LOAD_NAME                4 (Boolean)
                       16 LOAD_CONST               1 (False)
                       18 LOAD_CONST               1 (False)
                       20 KW_NAMES                 2
                       22 PRECALL                  3
                       26 CALL                     3
@@ -236,41 +111,41 @@
             None
          names      ('__name__', '__module__', '__qualname__', 'Column', 'Boolean', 'archived')
          varnames   ()
          freevars   ()
          cellvars   ()
          filename   '/Users/piercefreeman/projects/lassen/lassen/db/base_class.py'
          name       'ArchivedMixin'
-         firstlineno 27
+         firstlineno 5
          lnotab 0x0a01
       'ArchivedMixin'
       code
          argcount  : 0
          nlocals   : 0
          stacksize : 1
          flags     : 0
          code 0x970065005a0164005a0264015300
-          31           0 RESUME                   0
+           9           0 RESUME                   0
                        2 LOAD_NAME                0 (__name__)
                        4 STORE_NAME               1 (__module__)
                        6 LOAD_CONST               0 ('Base')
                        8 STORE_NAME               2 (__qualname__)
          
-          32          10 LOAD_CONST               1 (None)
+          10          10 LOAD_CONST               1 (None)
                       12 RETURN_VALUE
          consts
             'Base'
             None
          names      ('__name__', '__module__', '__qualname__')
          varnames   ()
          freevars   ()
          cellvars   ()
          filename   '/Users/piercefreeman/projects/lassen/lassen/db/base_class.py'
          name       'Base'
-         firstlineno 31
+         firstlineno 9
          lnotab 0x0a01
       'Base'
       'do_orm_execute'
       code
          argcount  : 1
          nlocals   : 1
          stacksize : 7
@@ -279,61 +154,61 @@
             0x97007c006a00000000000000000073597c006a01000000000000000073
             547c006a020000000000000000a003000000000000000000000000000000
             000000000064016402a6020000ab020000000000000000733b7c006a0400
             00000000000000a005000000000000000000000000000000000000000074
             0d00000000000000000000740e00000000000000000000640384006404ac
             05a6030000ab030000000000000000a6010000ab0100000000000000007c
             005f04000000000000000064065300640653006406530064065300
-          36           0 RESUME                   0
+          14           0 RESUME                   0
          
-          53           2 LOAD_FAST                0 (execute_state)
+          31           2 LOAD_FAST                0 (execute_state)
                        4 LOAD_ATTR                0 (is_column_load)
          
-          52          14 POP_JUMP_FORWARD_IF_TRUE    89 (to 194)
+          30          14 POP_JUMP_FORWARD_IF_TRUE    89 (to 194)
          
-          54          16 LOAD_FAST                0 (execute_state)
+          32          16 LOAD_FAST                0 (execute_state)
                       18 LOAD_ATTR                1 (is_relationship_load)
          
-          52          28 POP_JUMP_FORWARD_IF_TRUE    84 (to 198)
+          30          28 POP_JUMP_FORWARD_IF_TRUE    84 (to 198)
          
-          55          30 LOAD_FAST                0 (execute_state)
+          33          30 LOAD_FAST                0 (execute_state)
                       32 LOAD_ATTR                2 (execution_options)
                       42 LOAD_METHOD              3 (get)
                       64 LOAD_CONST               1 ('include_archived')
                       66 LOAD_CONST               2 (False)
                       68 PRECALL                  2
                       72 CALL                     2
          
-          52          82 POP_JUMP_FORWARD_IF_TRUE    59 (to 202)
+          30          82 POP_JUMP_FORWARD_IF_TRUE    59 (to 202)
          
-          58          84 LOAD_FAST                0 (execute_state)
+          36          84 LOAD_FAST                0 (execute_state)
                       86 LOAD_ATTR                4 (statement)
                       96 LOAD_METHOD              5 (options)
          
-          59         118 LOAD_GLOBAL             13 (NULL + with_loader_criteria)
+          37         118 LOAD_GLOBAL             13 (NULL + with_loader_criteria)
          
-          60         130 LOAD_GLOBAL             14 (ArchivedMixin)
+          38         130 LOAD_GLOBAL             14 (ArchivedMixin)
          
-          61         142 LOAD_CONST               3 (<code object <lambda>, file "/Users/piercefreeman/projects/lassen/lassen/db/base_class.py", line 61>)
+          39         142 LOAD_CONST               3 (<code object <lambda>, file "/Users/piercefreeman/projects/lassen/lassen/db/base_class.py", line 39>)
                      144 MAKE_FUNCTION            0
          
-          62         146 LOAD_CONST               4 (True)
+          40         146 LOAD_CONST               4 (True)
          
-          59         148 KW_NAMES                 5
+          37         148 KW_NAMES                 5
                      150 PRECALL                  3
                      154 CALL                     3
          
-          58         164 PRECALL                  1
+          36         164 PRECALL                  1
                      168 CALL                     1
                      178 LOAD_FAST                0 (execute_state)
                      180 STORE_ATTR               4 (statement)
                      190 LOAD_CONST               6 (None)
                      192 RETURN_VALUE
          
-          52     >>  194 LOAD_CONST               6 (None)
+          30     >>  194 LOAD_CONST               6 (None)
                      196 RETURN_VALUE
                  >>  198 LOAD_CONST               6 (None)
                      200 RETURN_VALUE
                  >>  202 LOAD_CONST               6 (None)
                      204 RETURN_VALUE
          consts
             'Intercept all ORM queries.   Add a with_loader_criteria option to all\n    of them.\n\n    This option applies to SELECT queries and adds a global WHERE criteria\n    (or as appropriate ON CLAUSE criteria for join targets)\n    to all objects of a certain class or superclass.\n\n    '
@@ -343,15 +218,15 @@
                argcount  : 1
                nlocals   : 1
                stacksize : 3
                flags     : 19
                code
                   0x97007c006a000000000000000000740300000000000000000000a60000
                   00ab0000000000000000006b02000000005300
-                61           0 RESUME                   0
+                39           0 RESUME                   0
                              2 LOAD_FAST                0 (cls)
                              4 LOAD_ATTR                0 (archived)
                             14 LOAD_GLOBAL              3 (NULL + false)
                             26 PRECALL                  0
                             30 CALL                     0
                             40 COMPARE_OP               2 (==)
                             46 RETURN_VALUE
@@ -359,31 +234,29 @@
                   None
                names      ('archived', 'false')
                varnames   ('cls',)
                freevars   ()
                cellvars   ()
                filename   '/Users/piercefreeman/projects/lassen/lassen/db/base_class.py'
                name       '<lambda>'
-               firstlineno 61
+               firstlineno 39
                lnotab 0x
             True
             ('include_aliases',)
             None
          names      ('is_column_load', 'is_relationship_load', 'execution_options', 'get', 'statement', 'options', 'with_loader_criteria', 'ArchivedMixin')
          varnames   ('execute_state',)
          freevars   ()
          cellvars   ()
          filename   '/Users/piercefreeman/projects/lassen/lassen/db/base_class.py'
          name       '_add_filtering_criteria'
-         firstlineno 36
+         firstlineno 14
          lnotab 0x02110cff02020cfe020334fd020622010c010c01040102fd10ff1efa
       None
-   names      ('typing', 'Any', 'inflection', 'underscore', 'sqlalchemy', 'Boolean', 'Column', 'event', 'false', 'sqlalchemy.orm', 'DeclarativeBase', 'Mapped', 'Session', 'declarative_mixin', 'declared_attr', 'with_loader_criteria', 'MainMixin', 'ArchivedMixin', 'Base', 'listens_for', '_add_filtering_criteria')
+   names      ('sqlalchemy', 'Boolean', 'Column', 'event', 'false', 'sqlalchemy.orm', 'DeclarativeBase', 'Session', 'with_loader_criteria', 'ArchivedMixin', 'Base', 'listens_for', '_add_filtering_criteria')
    varnames   ()
    freevars   ()
    cellvars   ()
    filename   '/Users/piercefreeman/projects/lassen/lassen/db/base_class.py'
    name       '<module>'
    firstlineno 1
-   lnotab
-      0x00ff02010c020c011801200a020118ff0e01020b1a041c05200104ff0e
-      01
+   lnotab 0x00ff0201180114031a041c05200104ff0e01
```

### Comparing `lassen-0.2.2/lassen/db/__pycache__/session.cpython-310.pyc` & `lassen-0.2.3/lassen/db/__pycache__/session.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `lassen-0.2.2/lassen/db/__pycache__/session.cpython-311.pyc` & `lassen-0.2.3/lassen/db/__pycache__/session.cpython-311.pyc`

 * *Files identical despite different names*

### Comparing `lassen-0.2.2/lassen/db/base_class.py` & `lassen-0.2.3/lassen/db/base_class.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,31 +1,9 @@
-from typing import Any
-
-from inflection import underscore
 from sqlalchemy import Boolean, Column, event, false
-from sqlalchemy.orm import (
-    DeclarativeBase,
-    Mapped,
-    Session,
-    declarative_mixin,
-    declared_attr,
-    with_loader_criteria,
-)
-
-
-@declarative_mixin
-class MainMixin:
-    id: Any
-    __name__: str
-
-    # Generate __tablename__ automatically
-    # Quirk of python's type system that cls MainMixin here (an instance) instead of Type[MainMixin] (a class)
-    @declared_attr
-    def __tablename__(cls: "MainMixin") -> Mapped[str]:
-        return underscore(cls.__name__)  # type: ignore
+from sqlalchemy.orm import DeclarativeBase, Session, with_loader_criteria
 
 
 class ArchivedMixin:
     archived = Column(Boolean, default=False, nullable=False)
 
 
 class Base(DeclarativeBase):
```

### Comparing `lassen-0.2.2/lassen/db/session.py` & `lassen-0.2.3/lassen/db/session.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.2/lassen/io.py` & `lassen-0.2.3/lassen/io.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.2/lassen/store.py` & `lassen-0.2.3/lassen/store.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.2/lassen/stubs/base.py` & `lassen-0.2.3/lassen/stubs/base.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.2/lassen/stubs/field.py` & `lassen-0.2.3/lassen/stubs/field.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.2/lassen/stubs/generate.py` & `lassen-0.2.3/lassen/stubs/generate.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,51 +1,54 @@
 import importlib
 import importlib.util
 import inspect
 import os
+import pkgutil
 import sys
 from pathlib import Path
 from typing import Type
 
 from click import command, secho
 from inflection import underscore
 
 from lassen.io import guess_package_location
 from lassen.stubs.base import BaseGenerator, BaseStub
 from lassen.stubs.generators.common import extract_stub_imports
 
+CLIENT_STUB_DIRECTORY = "stubs"
+
 
 def generate_files() -> list[Type[BaseStub]]:
-    root_path = guess_package_location("stubs")
+    root_path = guess_package_location(CLIENT_STUB_DIRECTORY)
     sys.path.append(os.path.dirname(root_path))
 
     stub_models: list[tuple[Type[BaseStub], Path]] = []
 
-    stubs_directory = root_path / "stubs"
-    for path in stubs_directory.rglob("*.py"):
-        if path.name.startswith("__"):
-            continue
-        spec = importlib.util.spec_from_file_location("stubs", path)
-        if not spec or not spec.loader:
-            print(f"Unable to load definition spec: {path}")
+    package = importlib.import_module(root_path.name)
+
+    for _, module_name, _ in pkgutil.walk_packages(
+        path=package.__path__, prefix=package.__name__ + "."
+    ):
+        # Speed up the search by skipping modules that are clearly not in the stubs directory
+        if CLIENT_STUB_DIRECTORY not in module_name:
             continue
-        definition_module = importlib.util.module_from_spec(spec)
-        spec.loader.exec_module(definition_module)
+
+        definition_module = importlib.import_module(module_name)
 
         stub_models += [
-            (val, path)
+            (val, Path(inspect.getfile(val)))
             for _, val in inspect.getmembers(
                 definition_module,
                 lambda x: inspect.isclass(x) and issubclass(x, BaseStub),
             )
             if val != BaseStub
         ]
 
     if not stub_models:
-        secho(f"No stub models found, checked: {stubs_directory}", fg="red")
+        secho(f"No stub models found, checked: {root_path}", fg="red")
         return []
 
     secho(f"Found stub models:", fg="blue")
     for model, path in stub_models:
         secho(f"  {model.__name__} ({path.name})", fg="blue")
 
     model_generators: list[tuple[Type[BaseStub], Path, list[BaseGenerator]]] = [
@@ -68,23 +71,30 @@
 
     # Set up the base folders
     # This includes a new __init__ stub in each directory that can be used to import dependency files
     for generator in unique_generators:
         generator_output = root_path / generator.output_directory
         generator_output.mkdir(parents=True, exist_ok=True)
 
+        # Clear the old files, since the user might have deleted the underlying stubs in the meantime
+        for file in generator_output.iterdir():
+            if file.is_file():
+                file.unlink()
+
         with open(generator_output / "__init__.py", "w") as f:
             f.write("")
 
     for model, path, generators in model_generators:
         # Extract the explicit import from the model and its user-defined parents
         # Skip the lassen-internal base class itself since this won't have any imports
         # that are relevant to the definitions
         parent_paths = [
-            inspect.getfile(model) for model in model.__bases__ if model != BaseStub
+            Path(inspect.getfile(model))
+            for model in model.__bases__
+            if model != BaseStub
         ]
         stub_imports = extract_stub_imports([path] + parent_paths)
 
         secho(f"Generating files for {model.__name__}")
 
         for generator in generators:
             generator_output = root_path / generator.output_directory
```

### Comparing `lassen-0.2.2/lassen/stubs/generators/common.py` & `lassen-0.2.3/lassen/stubs/generators/common.py`

 * *Files 3% similar despite different names*

```diff
@@ -67,16 +67,18 @@
 
     # Handle case for NoneType
     if typehint is type(None):
         return "None", []
 
     # Handle case for Unions, which might represent nullable fields
     if origin is typing.Union or origin == types.UnionType:
-        union_args = " | ".join([format_typehint_as_string(t)[0] for t in args])
-        return f"{union_args}", [format_import(t) for t in args]
+        union_args = ", ".join([format_typehint_as_string(t)[0] for t in args])
+        return f"Union[{union_args}]", [format_import(t) for t in args] + [
+            format_import(typing.Union)
+        ]
 
     # Handle case for Enum
     if isinstance(typehint, enum.EnumMeta):
         return typehint.__name__, [format_import(typehint)]
 
     # Handle case for built-in types
     if origin is None and not args:
@@ -156,22 +158,27 @@
     """
     # These representations can be explicitly cast
     # Everything else should be in a lambda
     allowed_representations = (str, int, float, bool, type(None))
     representation_dict: dict[str, str] = {}
 
     def convert_value(value: Any):
-        if isinstance(value, allowed_representations):
-            return repr(value)
+        if isinstance(value, enum.Enum):
+            return f"{value.__class__.__name__}.{value.name}"
         elif is_lambda(value):
-            return get_lambda_body(value)
+            return f"lambda: {get_lambda_body(value)}"
         elif isinstance(value, list):
             # Convert the args
             converted_args: list[str] = [convert_value(arg) for arg in value]
             return f"[{', '.join(converted_args)}]"
+        elif isinstance(value, allowed_representations):
+            # Allowed representation fallback should be the last in the chain, since these
+            # classes might be superclasses of other more specific targeting (StrEnum, for instance)
+            # that we would rather process by their targeted handler
+            return repr(value)
         else:
             raise ValueError(
                 f"Value {value} is not a valid default; cast with `lambda` in your code to maintain its representation."
             )
 
     for key, value in dictionary.items():
         representation_dict[key] = convert_value(value)
```

### Comparing `lassen-0.2.2/lassen/stubs/generators/schema.py` & `lassen-0.2.3/lassen/stubs/generators/schema.py`

 * *Files 2% similar despite different names*

```diff
@@ -48,44 +48,49 @@
 class SchemaGenerator(BaseGenerator):
     def __call__(
         self,
         model: Type[BaseStub],
         import_hints: ExtractedStubImports,
     ):
         model_name = model.__name__
-        _, all_deps = self.get_model_fields(model)
 
         # By convention, updates are PATCH-like requests so we should allow None values
         # across the board
-        create_fields, _ = self.get_model_fields(model, lambda f: f.create)
-        update_fields, _ = self.get_model_fields(
+        create_fields, create_deps = self.get_model_fields(model, lambda f: f.create)
+        update_fields, update_deps = self.get_model_fields(
             model, lambda f: f.update, force_optional=True
         )
-        read_fields, _ = self.get_model_fields(model, lambda f: f.read)
-        filter_fields, _ = self.get_model_fields(
+        read_fields, read_deps = self.get_model_fields(model, lambda f: f.read)
+        filter_fields, filter_deps = self.get_model_fields(
             model,
             lambda f: f.filter or not isinstance(f.filter_extensions, UNSET_VALUE),
             force_optional=True,
         )
-        augmented_filters, _ = self.get_augmented_filter_fields(model)
+        augmented_filters, augmented_deps = self.get_augmented_filter_fields(model)
+
+        all_dependencies = set(
+            create_deps + update_deps + read_deps + filter_deps + augmented_deps
+        )
 
         # Set up Jinja2 environment
         env = Environment(
             loader=FileSystemLoader(get_template_path("")),
             autoescape=select_autoescape(["html", "xml"]),
         )
 
         template = env.get_template("schema.py.j2")
         content = template.render(
             model_name=model_name,
             create_fields=create_fields,
             update_fields=update_fields,
             read_fields=read_fields,
             filter_fields=filter_fields + augmented_filters,
-            dependencies=sorted([dependency for dependency in all_deps if dependency]),
+            dependencies=sorted(
+                [dependency for dependency in all_dependencies if dependency]
+            ),
             clone_imports=import_hints.clone_imports,
             clone_typechecking_imports=import_hints.clone_typechecking_imports,
         )
 
         return RenderedFile(
             content=content,
             created_classes=[
@@ -131,15 +136,18 @@
             mapped_typehint, type_dependencies = format_typehint_as_string(typehint)
 
             declaration = f"{name}: {mapped_typehint}"
             field_arguments: dict[str, Any] = {}
             if force_optional:
                 field_arguments["default"] = None
             elif not isinstance(field.default, UNSET_VALUE):
-                field_arguments["default"] = field.default
+                if callable(field.default):
+                    field_arguments["default_factory"] = field.default
+                else:
+                    field_arguments["default"] = field.default
             elif is_optional(typehint):
                 # Default typehint is optional, so we should set the default to None
                 # so users don't have to manually set it
                 field_arguments["default"] = None
 
             if field.description:
                 field_arguments["description"] = field.description
```

### Comparing `lassen-0.2.2/lassen/stubs/generators/store.py` & `lassen-0.2.3/lassen/stubs/generators/store.py`

 * *Files 2% similar despite different names*

```diff
@@ -4,14 +4,15 @@
 import typing
 from datetime import datetime
 from typing import Any, Dict, List, Type, get_args, get_origin
 
 import sqlalchemy
 import sqlalchemy.ext.associationproxy
 import sqlalchemy.orm
+from inflection import underscore
 from jinja2 import Environment, FileSystemLoader, select_autoescape
 
 from lassen.db.base_class import Base as LassenBase
 from lassen.stubs.base import BaseDefinition, BaseGenerator, BaseStub, RenderedFile
 from lassen.stubs.definition import UniqueDefinition
 from lassen.stubs.field import UNSET_VALUE, FieldDefinition
 from lassen.stubs.generators.common import (
@@ -83,14 +84,15 @@
                 [dependency for dependency in field_dependencies if dependency]
                 + [dependency for dependency in table_args_dependencies if dependency]
                 + [format_import(base_class) for base_class in self.custom_baseclasses]
             ),
             model_superclasses=", ".join(model_superclasses),
             clone_imports=import_hints.clone_imports,
             clone_typechecking_imports=import_hints.clone_typechecking_imports,
+            table_name=underscore(model_name),
         )
 
         return RenderedFile(
             content=content,
             created_classes=[model_name],
         )
 
@@ -111,26 +113,14 @@
         for name, field in fields:
             # Determine if this generator should process this field
             if field.generators is not None:
                 if self not in field.generators:
                     continue
 
             typehint = typehints[name]
-            args = []
-            keyword_args = {}
-
-            if not isinstance(field.primary_key, UNSET_VALUE):
-                keyword_args["primary_key"] = True
-            if not isinstance(field.default, UNSET_VALUE):
-                keyword_args["default"] = field.default
-            if not isinstance(field.foreign_key, UNSET_VALUE):
-                keyword_args["foreign_key"] = field.foreign_key
-            if field.index:
-                keyword_args["index"] = True
-
             mapped_typehint, dependencies1 = format_typehint_as_string(typehint)
             dependencies |= set(dependencies1)
 
             # Since we want SQLAlchemy to translate the exact typehint into the column, we need to check
             # for exact class equality (versus a subclass like with isinstance)
             # One specific case where this happens is Enum - it is a VARCHAR in the backend, so isinstance(enum_field, sqlalchemy.String)
             # is True. At runtime, SQLAlchemy won't auto resolve this Enum to a String and needs the explicit definition
@@ -161,28 +151,41 @@
                     )
 
                 extra_kwargs: dict[str, Any] = {}
                 if not isinstance(field.backref, UNSET_VALUE):
                     extra_kwargs["backref"] = field.backref
 
                 dependencies.add(format_import(sqlalchemy.orm.relationship))
-                declaration += f" = relationship('{mapped_typehint}', foreign_key={foreign_key_name}, {format_dict_as_kwargs(extra_kwargs)})"
+                declaration += f" = relationship('{mapped_typehint}', foreign_keys=[{foreign_key_name}], {format_dict_as_kwargs(extra_kwargs)})"
             else:
                 (
                     column_typehint,
                     column_class,
                     dependencies2,
                 ) = self.format_column_for_sqlalchemy(typehint)
                 dependencies |= set(dependencies2)
 
                 declaration = f"{name}: Mapped[{mapped_typehint}]"
 
+                args = []
+                keyword_args = {}
+
                 if column_typehint and not column_class.__class__ in AUTO_CAST:
                     args = [column_typehint]
 
+                if not isinstance(field.primary_key, UNSET_VALUE):
+                    keyword_args["primary_key"] = True
+                if not isinstance(field.default, UNSET_VALUE):
+                    keyword_args["default"] = field.default
+                if not isinstance(field.foreign_key, UNSET_VALUE):
+                    args.append(f"ForeignKey('{field.foreign_key}')")
+                    dependencies.add(format_import(sqlalchemy.ForeignKey))
+                if field.index:
+                    keyword_args["index"] = True
+
                 formatted_args = [
                     *args,
                     *([format_dict_as_kwargs(keyword_args)] if keyword_args else []),
                 ]
                 if formatted_args:
                     declaration += f" = mapped_column({', '.join(formatted_args)})"
 
@@ -205,15 +208,15 @@
 
         declarations: list[str] = []
         dependencies: set[str] = set()
 
         for _, definition in definitions:
             if isinstance(definition, UniqueDefinition):
                 field_names = [
-                    instance_to_name[id(field)] for field in definition.fields
+                    f"'{instance_to_name[id(field)]}'" for field in definition.fields
                 ]
 
                 declarations.append(
                     f"UniqueConstraint({', '.join(field_names)}, name='{definition.name}')"
                 )
                 dependencies.add(
                     format_import(sqlalchemy.UniqueConstraint),
```

### Comparing `lassen-0.2.2/lassen/stubs/templates/schema.py.j2` & `lassen-0.2.3/lassen/stubs/templates/schema.py.j2`

 * *Files identical despite different names*

### Comparing `lassen-0.2.2/lassen/stubs/templates/sqlalchemy.py.j2` & `lassen-0.2.3/lassen/stubs/templates/sqlalchemy.py.j2`

 * *Files 17% similar despite different names*

```diff
@@ -8,16 +8,17 @@
 {% if clone_typechecking_imports -%}
 if TYPE_CHECKING:{% for import in clone_typechecking_imports%}
     {{ import }}
 {%- endfor %}
 {% endif %}
 
 class {{ model_name }}({{model_superclasses}}):
+    __tablename__ = '{{ table_name }}'
 {% for field in fields %}
     {{ field }}
 {% endfor %}{% if table_args %}
     __table_args__ = (
     {% for arg in table_args%}
-        {{ arg }}
+        {{ arg }},
     {%- endfor %}
     )
 {% endif %}
```

### Comparing `lassen-0.2.2/lassen/tests/__pycache__/conftest.cpython-310-pytest-7.3.1.pyc` & `lassen-0.2.3/lassen/tests/__pycache__/conftest.cpython-310-pytest-7.3.1.pyc`

 * *Files identical despite different names*

### Comparing `lassen-0.2.2/lassen/tests/__pycache__/fixtures.cpython-310.pyc` & `lassen-0.2.3/lassen/tests/__pycache__/fixtures.cpython-310.pyc`

 * *Files identical despite different names*

### Comparing `lassen-0.2.2/lassen/tests/__pycache__/test_store.cpython-310-pytest-7.3.1.pyc` & `lassen-0.2.3/lassen/tests/__pycache__/test_store.cpython-310-pytest-7.3.1.pyc`

 * *Files identical despite different names*

### Comparing `lassen-0.2.2/lassen/tests/conftest.py` & `lassen-0.2.3/lassen/tests/conftest.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.2/lassen/tests/datasets/test_dataset_helpers.py` & `lassen-0.2.3/lassen/tests/datasets/test_dataset_helpers.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.2/lassen/tests/datasets/test_pyarrow_schemas.py` & `lassen-0.2.3/lassen/tests/datasets/test_pyarrow_schemas.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.2/lassen/tests/fixtures/stubs/expected_schema.py` & `lassen-0.2.3/lassen/tests/fixtures/stubs/expected_schema.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,11 @@
 from pydantic import BaseModel, Field, Extra
 from MOCKED_PACKAGE import NoneType
 from MOCKED_PACKAGE import SimpleEnum
+from MOCKED_PACKAGE import Union
 from MOCKED_PACKAGE import datetime
 from MOCKED_PACKAGE import str
 
 from datetime import datetime
 from enum import Enum
 from typing import TYPE_CHECKING
 
@@ -40,20 +41,20 @@
 
 
 # API/STORE: RETRIEVE PROPERTIES
 class UserStub(UserStubBase):
 
     first_name: str = Field(description='First name of the user')
 
-    last_name: str | None = Field(default=None, description='Last name of the user')
+    last_name: Union[str, None] = Field(default=None, description='Last name of the user')
 
     password: str
 
     enum_value: SimpleEnum
 
-    creation_date: datetime = Field(default=datetime.now)
+    creation_date: datetime = Field(default_factory=lambda: datetime.now())
 
     forward_reference_value: 'timezone'
 
 
     class Config:
         orm_mode = True
```

### Comparing `lassen-0.2.2/lassen/tests/fixtures/stubs/expected_schema_public.py` & `lassen-0.2.3/lassen/tests/fixtures/stubs/expected_schema_public.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,9 +1,10 @@
 from pydantic import BaseModel, Field, Extra
 from MOCKED_PACKAGE import NoneType
+from MOCKED_PACKAGE import Union
 from MOCKED_PACKAGE import str
 
 from datetime import datetime
 from enum import Enum
 from typing import TYPE_CHECKING
 
 if TYPE_CHECKING:
@@ -38,14 +39,14 @@
 
 
 # API/STORE: RETRIEVE PROPERTIES
 class UserStub(UserStubBase):
 
     first_name: str = Field(description='First name of the user')
 
-    last_name: str | None = Field(default=None, description='Last name of the user')
+    last_name: Union[str, None] = Field(default=None, description='Last name of the user')
 
     password: str
 
 
     class Config:
         orm_mode = True
```

### Comparing `lassen-0.2.2/lassen/tests/fixtures/stubs/expected_store.py` & `lassen-0.2.3/lassen/tests/fixtures/stubs/expected_store.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,10 +1,11 @@
 from sqlalchemy.orm import Mapped, mapped_column
 from MOCKED_PACKAGE import NoneType
 from MOCKED_PACKAGE import SimpleEnum
+from MOCKED_PACKAGE import Union
 from MOCKED_PACKAGE import datetime
 from MOCKED_PACKAGE import str
 from lassen.db.base_class import Base
 from sqlalchemy.sql.sqltypes import DateTime
 from sqlalchemy.sql.sqltypes import Enum
 from sqlalchemy.sql.sqltypes import String
 
@@ -13,19 +14,20 @@
 from typing import TYPE_CHECKING
 
 if TYPE_CHECKING:
     from datetime import timezone
 
 
 class UserStub(Base):
+    __tablename__ = 'user_stub'
 
     first_name: Mapped[str]
 
-    last_name: Mapped[str | None]
+    last_name: Mapped[Union[str, None]]
 
     password: Mapped[str]
 
     enum_value: Mapped[SimpleEnum] = mapped_column(Enum(SimpleEnum))
 
-    creation_date: Mapped[datetime] = mapped_column(DateTime(), default=datetime.now)
+    creation_date: Mapped[datetime] = mapped_column(DateTime(), default=lambda: datetime.now())
 
     forward_reference_value: Mapped['timezone'] = mapped_column('timezone')
```

### Comparing `lassen-0.2.2/lassen/tests/fixtures/stubs/fixtures.py` & `lassen-0.2.3/lassen/tests/fixtures/stubs/fixtures.py`

 * *Files 16% similar despite different names*

```diff
@@ -23,15 +23,15 @@
     last_name: str | None = Field(description="Last name of the user")
 
     password: str = Field(create=True)
 
     enum_value: SimpleEnum = Field(generators=[store_gen, schema_gen])
 
     creation_date: datetime = Field(
-        generators=[store_gen, schema_gen], default=lambda x: datetime.now
+        generators=[store_gen, schema_gen], default=lambda: datetime.now()
     )
 
     # A timezone won't technically get cast properly, but we use it as a demonstration
     # of the forward reference capability
     forward_reference_value: 'timezone' = Field(
         generators=[store_gen, schema_gen]
     )
```

### Comparing `lassen-0.2.2/lassen/tests/fixtures/test_harness/test_harness/migrations/62bf8def9fb1_new_migration.py` & `lassen-0.2.3/lassen/tests/fixtures/test_harness/test_harness/migrations/62bf8def9fb1_new_migration.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.2/lassen/tests/fixtures/test_harness/test_harness/migrations/96dbf6f6d068_add_name.py` & `lassen-0.2.3/lassen/tests/fixtures/test_harness/test_harness/migrations/96dbf6f6d068_add_name.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.2/lassen/tests/model_fixtures.py` & `lassen-0.2.3/lassen/tests/model_fixtures.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.2/lassen/tests/stubs/generators/test_common.py` & `lassen-0.2.3/lassen/tests/stubs/generators/test_common.py`

 * *Files 5% similar despite different names*

```diff
@@ -23,31 +23,31 @@
 @pytest.mark.parametrize(
     "typehint, expected",
     [
         (int, "int"),
         (float, "float"),
         (SimpleEnum, "SimpleEnum"),
         (list[str], "list[str]"),
-        (str | None, "str | None"),
+        (str | None, "Union[str, None]"),
         (List[str], "list[str]"),
         (Dict[str, str], "dict[str, str]"),
         (dict[str, str], "dict[str, str]"),
     ],
 )
 def test_format_typehint_as_string(typehint, expected):
     formatted_typehint, dependencies = format_typehint_as_string(typehint)
     assert formatted_typehint == expected
     assert len(dependencies) > 0
 
 
 @pytest.mark.parametrize(
     "input_dict, expected_str",
     [
-        ({"a": 1, "b": lambda: datetime.now()}, "a=1, b=datetime.now()"),
-        ({"a": 1, "b": lambda: datetime.now}, "a=1, b=datetime.now"),
+        ({"a": 1, "b": lambda: datetime.now()}, "a=1, b=lambda: datetime.now()"),
+        ({"a": 1, "b": lambda: datetime.now}, "a=1, b=lambda: datetime.now"),
     ],
 )
 def test_format_dict_as_kwargs(input_dict: dict[str, Any], expected_str: str):
     assert format_dict_as_kwargs(input_dict) == expected_str
 
 
 @pytest.mark.parametrize(
```

### Comparing `lassen-0.2.2/lassen/tests/stubs/generators/test_schema.py` & `lassen-0.2.3/lassen/tests/stubs/generators/test_schema.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.2/lassen/tests/stubs/generators/test_store.py` & `lassen-0.2.3/lassen/tests/stubs/generators/test_store.py`

 * *Files 3% similar despite different names*

```diff
@@ -53,27 +53,29 @@
             foreign_key=user_parent_id, is_relationship=True
         )
 
     store_generator = StoreGenerator("test")
     definition = store_generator(MyChildModel, ExtractedStubImports([], []))
 
     assert (
-        "user_parent_id: Mapped[int] = mapped_column(foreign_key='my_parent_model.id')"
+        "user_parent_id: Mapped[int] = mapped_column(ForeignKey('my_parent_model.id'))"
         in definition.content
     )
     assert (
-        "user_parent: Mapped['MyParentModel'] = relationship('MyParentModel', foreign_key=user_parent_id, )"
+        "user_parent: Mapped['MyParentModel'] = relationship('MyParentModel', foreign_keys=[user_parent_id], )"
         in definition.content
     )
 
 
 def test_get_model_table_args() -> None:
     class MyModel(BaseStub):
         unique_text: str = Field()
 
         my_unique_constraint = UniqueDefinition(
             name="my_unique_constraint", fields=[unique_text]
         )
 
     store_generator = StoreGenerator("test")
     definitions, _ = store_generator.get_model_table_args(MyModel)
-    assert definitions == ["UniqueConstraint(unique_text, name='my_unique_constraint')"]
+    assert definitions == [
+        "UniqueConstraint('unique_text', name='my_unique_constraint')"
+    ]
```

### Comparing `lassen-0.2.2/lassen/tests/stubs/test_generate.py` & `lassen-0.2.3/lassen/tests/stubs/test_generate.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.2/lassen/tests/test_alembic.py` & `lassen-0.2.3/lassen/tests/test_alembic.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.2/lassen/tests/test_store.py` & `lassen-0.2.3/lassen/tests/test_store.py`

 * *Files identical despite different names*

### Comparing `lassen-0.2.2/pyproject.toml` & `lassen-0.2.3/pyproject.toml`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "lassen"
-version = "0.2.2"
+version = "0.2.3"
 description = "Common webapp scaffolding."
 authors = ["Pierce Freeman <pierce@freeman.vc>"]
 readme = "README.md"
 
 [tool.poetry.dependencies]
 python = "^3.11"
 fastapi = "^0.95.1"
```

### Comparing `lassen-0.2.2/setup.py` & `lassen-0.2.3/setup.py`

 * *Files 4% similar despite different names*

```diff
@@ -41,17 +41,17 @@
 
 entry_points = \
 {'console_scripts': ['generate-lassen = lassen.stubs.generate:cli',
                      'migrate = lassen.alembic.cli:main']}
 
 setup_kwargs = {
     'name': 'lassen',
-    'version': '0.2.2',
+    'version': '0.2.3',
     'description': 'Common webapp scaffolding.',
-    'long_description': '# lassen\n\n**40.4881° N, 121.5049° W**\n\nCore utilities for MonkeySee web applications.\n\nNot guaranteed to be backwards compatible, use at your own risk.\n\n## Structure\n\n**Stores:** Each datamodel is expected to have its own store. Base classes that provide standard logic are provided by `lassen.store`\n- StoreBase: Base class for all stores\n- StoreFilterMixin: Mixin for filtering stores that specify an additional schema to use to filter\n\n**Schemas:** Each datamodel should define a Model class (SQLAlchemy base object) and a series of Schema objects (Pydantic) that allow the Store to serialize the models. These schemas are also often used for direct CRUD referencing in the API layer.\n\nWe use a base `Stub` file to generate these schemas from a centralized definition.\n\n```bash\npoetry run generate-lassen\n```\n\n**Datasets:** Optional huggingface `datasets` processing utilities. Only installed under the `lassen[datasets]` extra. These provide support for:\n\n- batch_to_examples: Iterate and manipulate each example separately, versus over nested key-based lists.\n- examples_to_batch: Takes the output of a typehinted element-wise batch and converts into the format needed for dataset insertion. If datasets can\'t automatically interpret the type of the fields, also provide automatic casting based on the typehinted dataclass.\n\n```python\nfrom lassen.datasets import batch_to_examples, examples_to_batch\nimport pandas as pd\n\n@dataclass\nclass BatchInsertion:\n    texts: list[str]\n\ndef batch_process(examples):\n    new_examples : list[BatchInsertion] = []\n    for example in batch_to_examples(examples):\n        new_examples.append(\n            BatchInsertion(\n                example["raw_text"].split()\n            )\n        )\n\n    # datasets won\'t be able to typehint a dataset that starts with an empty example, so we use our explicit schema to cast the data\n    return examples_to_batch(new_examples, BatchInsertion, explicit_schema=True)\n\ndf = pd.DataFrame(\n    [\n        {"raw_text": ""},\n        {"raw_text": "This is a test"},\n        {"raw_text": "This is another test"},\n    ]\n)\n\ndataset = Dataset.from_pandas(df)\n\ndataset = dataset.map(\n    batch_process,\n    batched=True,\n    batch_size=1,\n    num_proc=1,\n    remove_columns=dataset.column_names,\n)\n```\n\n**Migrations:** Lassen includes a templated alembic.init and env.py file. Client applications just need to have a `migrations` folder within their project root. After this you can swap `poetry run alembic` with `poetry run migrate`.\n\n```sh\npoetry run migrate upgrade head\n```\n\n**Settings:** Application settings should subclass our core settings. This provides a standard way to load settings from environment variables and includes common database keys.\n\n```python\nfrom lassen.core.config import CoreSettings, register_settings\n\n@register_settings\nclass ClientSettings(CoreSettings):\n    pass\n```\n\n**Schemas:** For helper schemas when returning results via API, see [lassen.schema](./lassen/schema.py).\n\n## Development\n\n```sh\npoetry install --extras "datasets"\n\ncreateuser lassen\ncreatedb -O lassen lassen_db\ncreatedb -O lassen lassen_test_db\n```\n\nUnit Tests:\n\n```sh\npoetry run pytest\n```\n',
+    'long_description': '# lassen\n\n**40.4881° N, 121.5049° W**\n\nCore utilities for MonkeySee web applications.\n\nNot guaranteed to be backwards compatible, use at your own risk.\n\n## Structure\n\n**Stores:** Each datamodel is expected to have its own store. Base classes that provide standard logic are provided by `lassen.store`\n- StoreBase: Base class for all stores\n- StoreFilterMixin: Mixin for filtering stores that specify an additional schema to use to filter\n\n**Schemas:** Each datamodel should define a Model class (SQLAlchemy base object) and a series of Schema objects (Pydantic) that allow the Store to serialize the models. These schemas are also often used for direct CRUD referencing in the API layer.\n\nWe use a base `Stub` file to generate these schemas from a centralized definition. When defining generators you should use a path that can be fully managed by lassen, since we will remove and regenerate these files on each run.\n\n```python\nSTORE_GENERATOR = StoreGenerator("models/auto")\nSCHEMA_GENERATOR = SchemaGenerator("schemas/auto")\n```\n\n```bash\npoetry run generate-lassen\n```\n\n**Datasets:** Optional huggingface `datasets` processing utilities. Only installed under the `lassen[datasets]` extra. These provide support for:\n\n- batch_to_examples: Iterate and manipulate each example separately, versus over nested key-based lists.\n- examples_to_batch: Takes the output of a typehinted element-wise batch and converts into the format needed for dataset insertion. If datasets can\'t automatically interpret the type of the fields, also provide automatic casting based on the typehinted dataclass.\n\n```python\nfrom lassen.datasets import batch_to_examples, examples_to_batch\nimport pandas as pd\n\n@dataclass\nclass BatchInsertion:\n    texts: list[str]\n\ndef batch_process(examples):\n    new_examples : list[BatchInsertion] = []\n    for example in batch_to_examples(examples):\n        new_examples.append(\n            BatchInsertion(\n                example["raw_text"].split()\n            )\n        )\n\n    # datasets won\'t be able to typehint a dataset that starts with an empty example, so we use our explicit schema to cast the data\n    return examples_to_batch(new_examples, BatchInsertion, explicit_schema=True)\n\ndf = pd.DataFrame(\n    [\n        {"raw_text": ""},\n        {"raw_text": "This is a test"},\n        {"raw_text": "This is another test"},\n    ]\n)\n\ndataset = Dataset.from_pandas(df)\n\ndataset = dataset.map(\n    batch_process,\n    batched=True,\n    batch_size=1,\n    num_proc=1,\n    remove_columns=dataset.column_names,\n)\n```\n\n**Migrations:** Lassen includes a templated alembic.init and env.py file. Client applications just need to have a `migrations` folder within their project root. After this you can swap `poetry run alembic` with `poetry run migrate`.\n\n```sh\npoetry run migrate upgrade head\n```\n\n**Settings:** Application settings should subclass our core settings. This provides a standard way to load settings from environment variables and includes common database keys.\n\n```python\nfrom lassen.core.config import CoreSettings, register_settings\n\n@register_settings\nclass ClientSettings(CoreSettings):\n    pass\n```\n\n**Schemas:** For helper schemas when returning results via API, see [lassen.schema](./lassen/schema.py).\n\n## Development\n\n```sh\npoetry install --extras "datasets"\n\ncreateuser lassen\ncreatedb -O lassen lassen_db\ncreatedb -O lassen lassen_test_db\n```\n\nUnit Tests:\n\n```sh\npoetry run pytest\n```\n',
     'author': 'Pierce Freeman',
     'author_email': 'pierce@freeman.vc',
     'maintainer': 'None',
     'maintainer_email': 'None',
     'url': 'None',
     'packages': packages,
     'package_data': package_data,
```

### Comparing `lassen-0.2.2/PKG-INFO` & `lassen-0.2.3/PKG-INFO`

 * *Files 10% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: lassen
-Version: 0.2.2
+Version: 0.2.3
 Summary: Common webapp scaffolding.
 Author: Pierce Freeman
 Author-email: pierce@freeman.vc
 Requires-Python: >=3.11,<4.0
 Classifier: Programming Language :: Python :: 3
 Provides-Extra: database
 Provides-Extra: datasets
@@ -35,15 +35,20 @@
 
 **Stores:** Each datamodel is expected to have its own store. Base classes that provide standard logic are provided by `lassen.store`
 - StoreBase: Base class for all stores
 - StoreFilterMixin: Mixin for filtering stores that specify an additional schema to use to filter
 
 **Schemas:** Each datamodel should define a Model class (SQLAlchemy base object) and a series of Schema objects (Pydantic) that allow the Store to serialize the models. These schemas are also often used for direct CRUD referencing in the API layer.
 
-We use a base `Stub` file to generate these schemas from a centralized definition.
+We use a base `Stub` file to generate these schemas from a centralized definition. When defining generators you should use a path that can be fully managed by lassen, since we will remove and regenerate these files on each run.
+
+```python
+STORE_GENERATOR = StoreGenerator("models/auto")
+SCHEMA_GENERATOR = SchemaGenerator("schemas/auto")
+```
 
 ```bash
 poetry run generate-lassen
 ```
 
 **Datasets:** Optional huggingface `datasets` processing utilities. Only installed under the `lassen[datasets]` extra. These provide support for:
```

