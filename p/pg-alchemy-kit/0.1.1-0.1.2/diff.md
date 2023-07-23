# Comparing `tmp/pg_alchemy_kit-0.1.1.tar.gz` & `tmp/pg_alchemy_kit-0.1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pg_alchemy_kit-0.1.1.tar", max compression
+gzip compressed data, was "pg_alchemy_kit-0.1.2.tar", max compression
```

## Comparing `pg_alchemy_kit-0.1.1.tar` & `pg_alchemy_kit-0.1.2.tar`

### file list

```diff
@@ -1,6 +1,6 @@
--rw-r--r--   0        0        0        0 2023-07-23 04:50:14.444000 pg_alchemy_kit-0.1.1/README.md
--rw-r--r--   0        0        0     2382 2023-07-23 04:56:56.075700 pg_alchemy_kit-0.1.1/pg_alchemy_kit/PG.py
--rw-r--r--   0        0        0     5575 2023-07-23 04:50:57.872766 pg_alchemy_kit-0.1.1/pg_alchemy_kit/PGUtils.py
--rw-r--r--   0        0        0      138 2023-07-23 04:57:39.246037 pg_alchemy_kit-0.1.1/pg_alchemy_kit/__init__.py
--rw-r--r--   0        0        0      363 2023-07-23 04:58:32.509505 pg_alchemy_kit-0.1.1/pyproject.toml
--rw-r--r--   0        0        0      431 1970-01-01 00:00:00.000000 pg_alchemy_kit-0.1.1/PKG-INFO
+-rw-r--r--   0        0        0     5222 2023-07-23 05:05:39.685538 pg_alchemy_kit-0.1.2/README.md
+-rw-r--r--   0        0        0     2380 2023-07-23 04:59:06.899758 pg_alchemy_kit-0.1.2/pg_alchemy_kit/PG.py
+-rw-r--r--   0        0        0     5575 2023-07-23 04:50:57.872766 pg_alchemy_kit-0.1.2/pg_alchemy_kit/PGUtils.py
+-rw-r--r--   0        0        0      138 2023-07-23 04:57:39.246037 pg_alchemy_kit-0.1.2/pg_alchemy_kit/__init__.py
+-rw-r--r--   0        0        0      438 2023-07-23 05:06:05.824682 pg_alchemy_kit-0.1.2/pyproject.toml
+-rw-r--r--   0        0        0     5728 1970-01-01 00:00:00.000000 pg_alchemy_kit-0.1.2/PKG-INFO
```

### Comparing `pg_alchemy_kit-0.1.1/pg_alchemy_kit/PG.py` & `pg_alchemy_kit-0.1.2/pg_alchemy_kit/PG.py`

 * *Files 0% similar despite different names*

```diff
@@ -6,16 +6,14 @@
 from sqlalchemy.orm import sessionmaker, scoped_session
 from sqlalchemy.orm import DeclarativeMeta
 import sqlalchemy
 import logging
 from contextlib import contextmanager
 from typing import List, Iterator
 
-
-
 class PG:
     def initialize(cls, url: str = None, logger: logging.Logger = None, **kwargs):
         url = url or get_engine_url()
         cls.engine: Engine = get_engine(url, **kwargs)
         cls.SessionLocal = sessionmaker(
             autocommit=False, autoflush=False, bind=cls.engine
         )
```

### Comparing `pg_alchemy_kit-0.1.1/pg_alchemy_kit/PGUtils.py` & `pg_alchemy_kit-0.1.2/pg_alchemy_kit/PGUtils.py`

 * *Files identical despite different names*

