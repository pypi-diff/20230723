# Comparing `tmp/duckdb_engine-0.9.1.tar.gz` & `tmp/duckdb_engine-0.9.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "duckdb_engine-0.9.1.tar", max compression
+gzip compressed data, was "duckdb_engine-0.9.2.tar", max compression
```

## Comparing `duckdb_engine-0.9.1.tar` & `duckdb_engine-0.9.2.tar`

### file list

```diff
@@ -1,22 +1,22 @@
--rw-r--r--   0        0        0     1076 2023-07-14 06:49:36.523742 duckdb_engine-0.9.1/LICENSE.txt
--rw-r--r--   0        0        0     5953 2023-07-14 06:49:36.523742 duckdb_engine-0.9.1/README.md
--rw-r--r--   0        0        0        4 2023-07-14 06:49:36.523742 duckdb_engine-0.9.1/duckdb_engine/.hypothesis/examples/f024fc7dfe5f1878/7210af19145ec2a8
--rw-r--r--   0        0        0        1 2023-07-14 06:49:36.523742 duckdb_engine-0.9.1/duckdb_engine/.hypothesis/examples/f024fc7dfe5f1878/bec021b4f368e306
--rw-r--r--   0        0        0    20688 2023-07-14 06:49:36.523742 duckdb_engine-0.9.1/duckdb_engine/.hypothesis/unicode_data/12.1.0/charmap.json.gz
--rw-r--r--   0        0        0    12277 2023-07-14 06:49:36.523742 duckdb_engine-0.9.1/duckdb_engine/__init__.py
--rw-r--r--   0        0        0     1096 2023-07-14 06:49:36.523742 duckdb_engine-0.9.1/duckdb_engine/config.py
--rw-r--r--   0        0        0        0 2023-07-14 06:49:36.523742 duckdb_engine-0.9.1/duckdb_engine/conftest.py
--rw-r--r--   0        0        0     5731 2023-07-14 06:49:36.523742 duckdb_engine-0.9.1/duckdb_engine/datatypes.py
--rw-r--r--   0        0        0        0 2023-07-14 06:49:36.523742 duckdb_engine-0.9.1/duckdb_engine/py.typed
--rw-r--r--   0        0        0        0 2023-07-14 06:49:36.523742 duckdb_engine-0.9.1/duckdb_engine/tests/__init__.py
--rw-r--r--   0        0        0     1209 2023-07-14 06:49:36.523742 duckdb_engine-0.9.1/duckdb_engine/tests/conftest.py
--rw-r--r--   0        0        0        0 2023-07-14 06:49:36.523742 duckdb_engine-0.9.1/duckdb_engine/tests/snapshots/__init__.py
--rw-r--r--   0        0        0      338 2023-07-14 06:49:36.523742 duckdb_engine-0.9.1/duckdb_engine/tests/snapshots/snap_test_basic.py
--rw-r--r--   0        0        0    11631 2023-07-14 06:49:36.523742 duckdb_engine-0.9.1/duckdb_engine/tests/test_basic.py
--rw-r--r--   0        0        0     4035 2023-07-14 06:49:36.523742 duckdb_engine-0.9.1/duckdb_engine/tests/test_datatypes.py
--rw-r--r--   0        0        0      948 2023-07-14 06:49:36.523742 duckdb_engine-0.9.1/duckdb_engine/tests/test_ibis.py
--rw-r--r--   0        0        0     1740 2023-07-14 06:49:36.523742 duckdb_engine-0.9.1/duckdb_engine/tests/test_integration.py
--rw-r--r--   0        0        0     3946 2023-07-14 06:49:36.523742 duckdb_engine-0.9.1/duckdb_engine/tests/test_pandas.py
--rw-r--r--   0        0        0      257 2023-07-14 06:49:36.523742 duckdb_engine-0.9.1/duckdb_engine/tests/util.py
--rw-r--r--   0        0        0     1403 2023-07-14 06:49:36.523742 duckdb_engine-0.9.1/pyproject.toml
--rw-r--r--   0        0        0     6846 1970-01-01 00:00:00.000000 duckdb_engine-0.9.1/PKG-INFO
+-rw-r--r--   0        0        0     1076 2023-07-23 09:53:20.178798 duckdb_engine-0.9.2/LICENSE.txt
+-rw-r--r--   0        0        0     5953 2023-07-23 09:53:20.178798 duckdb_engine-0.9.2/README.md
+-rw-r--r--   0        0        0        4 2023-07-23 09:53:20.178798 duckdb_engine-0.9.2/duckdb_engine/.hypothesis/examples/f024fc7dfe5f1878/7210af19145ec2a8
+-rw-r--r--   0        0        0        1 2023-07-23 09:53:20.178798 duckdb_engine-0.9.2/duckdb_engine/.hypothesis/examples/f024fc7dfe5f1878/bec021b4f368e306
+-rw-r--r--   0        0        0    20688 2023-07-23 09:53:20.182798 duckdb_engine-0.9.2/duckdb_engine/.hypothesis/unicode_data/12.1.0/charmap.json.gz
+-rw-r--r--   0        0        0    12277 2023-07-23 09:53:20.182798 duckdb_engine-0.9.2/duckdb_engine/__init__.py
+-rw-r--r--   0        0        0     1096 2023-07-23 09:53:20.182798 duckdb_engine-0.9.2/duckdb_engine/config.py
+-rw-r--r--   0        0        0        0 2023-07-23 09:53:20.182798 duckdb_engine-0.9.2/duckdb_engine/conftest.py
+-rw-r--r--   0        0        0     5734 2023-07-23 09:53:20.182798 duckdb_engine-0.9.2/duckdb_engine/datatypes.py
+-rw-r--r--   0        0        0        0 2023-07-23 09:53:20.182798 duckdb_engine-0.9.2/duckdb_engine/py.typed
+-rw-r--r--   0        0        0        0 2023-07-23 09:53:20.182798 duckdb_engine-0.9.2/duckdb_engine/tests/__init__.py
+-rw-r--r--   0        0        0     1209 2023-07-23 09:53:20.182798 duckdb_engine-0.9.2/duckdb_engine/tests/conftest.py
+-rw-r--r--   0        0        0        0 2023-07-23 09:53:20.182798 duckdb_engine-0.9.2/duckdb_engine/tests/snapshots/__init__.py
+-rw-r--r--   0        0        0      338 2023-07-23 09:53:20.182798 duckdb_engine-0.9.2/duckdb_engine/tests/snapshots/snap_test_basic.py
+-rw-r--r--   0        0        0    11631 2023-07-23 09:53:20.182798 duckdb_engine-0.9.2/duckdb_engine/tests/test_basic.py
+-rw-r--r--   0        0        0     4035 2023-07-23 09:53:20.182798 duckdb_engine-0.9.2/duckdb_engine/tests/test_datatypes.py
+-rw-r--r--   0        0        0      948 2023-07-23 09:53:20.182798 duckdb_engine-0.9.2/duckdb_engine/tests/test_ibis.py
+-rw-r--r--   0        0        0     1740 2023-07-23 09:53:20.182798 duckdb_engine-0.9.2/duckdb_engine/tests/test_integration.py
+-rw-r--r--   0        0        0     3946 2023-07-23 09:53:20.182798 duckdb_engine-0.9.2/duckdb_engine/tests/test_pandas.py
+-rw-r--r--   0        0        0      257 2023-07-23 09:53:20.182798 duckdb_engine-0.9.2/duckdb_engine/tests/util.py
+-rw-r--r--   0        0        0     1403 2023-07-23 09:53:20.182798 duckdb_engine-0.9.2/pyproject.toml
+-rw-r--r--   0        0        0     6846 1970-01-01 00:00:00.000000 duckdb_engine-0.9.2/PKG-INFO
```

### Comparing `duckdb_engine-0.9.1/LICENSE.txt` & `duckdb_engine-0.9.2/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `duckdb_engine-0.9.1/README.md` & `duckdb_engine-0.9.2/README.md`

 * *Files identical despite different names*

### Comparing `duckdb_engine-0.9.1/duckdb_engine/.hypothesis/unicode_data/12.1.0/charmap.json.gz` & `duckdb_engine-0.9.2/duckdb_engine/.hypothesis/unicode_data/12.1.0/charmap.json.gz`

 * *Files identical despite different names*

### Comparing `duckdb_engine-0.9.1/duckdb_engine/__init__.py` & `duckdb_engine-0.9.2/duckdb_engine/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -24,15 +24,15 @@
 from sqlalchemy.engine.default import DefaultDialect
 from sqlalchemy.engine.url import URL
 from sqlalchemy.ext.compiler import compiles
 
 from .config import apply_config, get_core_config
 from .datatypes import ISCHEMA_NAMES, register_extension_types
 
-__version__ = "0.9.1"
+__version__ = "0.9.2"
 
 if TYPE_CHECKING:
     from sqlalchemy.base import Connection
     from sqlalchemy.engine.interfaces import _IndexDict
 
 
 register_extension_types()
```

### Comparing `duckdb_engine-0.9.1/duckdb_engine/config.py` & `duckdb_engine-0.9.2/duckdb_engine/config.py`

 * *Files identical despite different names*

### Comparing `duckdb_engine-0.9.1/duckdb_engine/datatypes.py` & `duckdb_engine-0.9.2/duckdb_engine/datatypes.py`

 * *Files 1% similar despite different names*

```diff
@@ -172,15 +172,15 @@
 
 
 ISCHEMA_NAMES = {
     "hugeint": HugeInteger,
     "tinyint": TinyInteger,
     "utinyint": UTinyInteger,
     "usmallint": USmallInteger,
-    "uinteger": UInt8,
+    "uinteger": UInteger,
     "ubigint": UBigInteger,
     "timestamp_s": sqltypes.TIMESTAMP,
     "timestamp_ms": sqltypes.TIMESTAMP,
     "timestamp_ns": sqltypes.TIMESTAMP,
     "enum": sqltypes.Enum,
 }
```

### Comparing `duckdb_engine-0.9.1/duckdb_engine/tests/conftest.py` & `duckdb_engine-0.9.2/duckdb_engine/tests/conftest.py`

 * *Files identical despite different names*

### Comparing `duckdb_engine-0.9.1/duckdb_engine/tests/test_basic.py` & `duckdb_engine-0.9.2/duckdb_engine/tests/test_basic.py`

 * *Files identical despite different names*

### Comparing `duckdb_engine-0.9.1/duckdb_engine/tests/test_datatypes.py` & `duckdb_engine-0.9.2/duckdb_engine/tests/test_datatypes.py`

 * *Files identical despite different names*

### Comparing `duckdb_engine-0.9.1/duckdb_engine/tests/test_ibis.py` & `duckdb_engine-0.9.2/duckdb_engine/tests/test_ibis.py`

 * *Files identical despite different names*

### Comparing `duckdb_engine-0.9.1/duckdb_engine/tests/test_integration.py` & `duckdb_engine-0.9.2/duckdb_engine/tests/test_integration.py`

 * *Files identical despite different names*

### Comparing `duckdb_engine-0.9.1/duckdb_engine/tests/test_pandas.py` & `duckdb_engine-0.9.2/duckdb_engine/tests/test_pandas.py`

 * *Files identical despite different names*

### Comparing `duckdb_engine-0.9.1/pyproject.toml` & `duckdb_engine-0.9.2/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "duckdb_engine"
-version = "0.9.1"
+version = "0.9.2"
 description = "SQLAlchemy driver for duckdb"
 authors = ["Elliana <me@mause.me>"]
 license = "MIT"
 readme = "README.md"
 repository = "https://github.com/Mause/duckdb_engine"
 
 [tool.poetry.urls]
```

### Comparing `duckdb_engine-0.9.1/PKG-INFO` & `duckdb_engine-0.9.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: duckdb-engine
-Version: 0.9.1
+Version: 0.9.2
 Summary: SQLAlchemy driver for duckdb
 Home-page: https://github.com/Mause/duckdb_engine
 License: MIT
 Author: Elliana
 Author-email: me@mause.me
 Requires-Python: >=3.7
 Classifier: License :: OSI Approved :: MIT License
```

