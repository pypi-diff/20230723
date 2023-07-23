# Comparing `tmp/pg_alchemy_kit-0.1.0.tar.gz` & `tmp/pg_alchemy_kit-0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pg_alchemy_kit-0.1.0.tar", max compression
+gzip compressed data, was "pg_alchemy_kit-0.1.1.tar", max compression
```

## Comparing `pg_alchemy_kit-0.1.0.tar` & `pg_alchemy_kit-0.1.1.tar`

### file list

```diff
@@ -1,6 +1,6 @@
--rw-r--r--   0        0        0        0 2023-07-23 04:50:14.444000 pg_alchemy_kit-0.1.0/README.md
--rw-r--r--   0        0        0     2377 2023-07-23 04:51:38.996211 pg_alchemy_kit-0.1.0/pg_alchemy_kit/PG.py
--rw-r--r--   0        0        0     5575 2023-07-23 04:50:57.872766 pg_alchemy_kit-0.1.0/pg_alchemy_kit/PGUtils.py
--rw-r--r--   0        0        0      104 2023-07-23 04:51:30.216189 pg_alchemy_kit-0.1.0/pg_alchemy_kit/__init__.py
--rw-r--r--   0        0        0      363 2023-07-23 04:50:47.109591 pg_alchemy_kit-0.1.0/pyproject.toml
--rw-r--r--   0        0        0      431 1970-01-01 00:00:00.000000 pg_alchemy_kit-0.1.0/PKG-INFO
+-rw-r--r--   0        0        0        0 2023-07-23 04:50:14.444000 pg_alchemy_kit-0.1.1/README.md
+-rw-r--r--   0        0        0     2382 2023-07-23 04:56:56.075700 pg_alchemy_kit-0.1.1/pg_alchemy_kit/PG.py
+-rw-r--r--   0        0        0     5575 2023-07-23 04:50:57.872766 pg_alchemy_kit-0.1.1/pg_alchemy_kit/PGUtils.py
+-rw-r--r--   0        0        0      138 2023-07-23 04:57:39.246037 pg_alchemy_kit-0.1.1/pg_alchemy_kit/__init__.py
+-rw-r--r--   0        0        0      363 2023-07-23 04:58:32.509505 pg_alchemy_kit-0.1.1/pyproject.toml
+-rw-r--r--   0        0        0      431 1970-01-01 00:00:00.000000 pg_alchemy_kit-0.1.1/PKG-INFO
```

### Comparing `pg_alchemy_kit-0.1.0/pg_alchemy_kit/PG.py` & `pg_alchemy_kit-0.1.1/pg_alchemy_kit/PG.py`

 * *Files 0% similar despite different names*

```diff
@@ -49,14 +49,15 @@
             try:
                 if schema not in cls.inspector.get_schema_names():
                     cls.engine.execute(sqlalchemy.schema.CreateSchema(schema))
                 Base.metadata.create_all(cls.engine)
             except Exception as e:
                 cls.logger.info(f"Error in create_tables: {e}")
 
+    
     @contextmanager
     def get_session_ctx(cls) -> Iterator[Session]:
         with cls.SessionLocal() as session:
             try:
                 yield session
             finally:
                 session.close()
```

### Comparing `pg_alchemy_kit-0.1.0/pg_alchemy_kit/PGUtils.py` & `pg_alchemy_kit-0.1.1/pg_alchemy_kit/PGUtils.py`

 * *Files identical despite different names*

