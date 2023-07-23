# Comparing `tmp/atro_pylog-0.3.0.tar.gz` & `tmp/atro_pylog-0.4.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "atro_pylog-0.3.0.tar", max compression
+gzip compressed data, was "atro_pylog-0.4.0.tar", max compression
```

## Comparing `atro_pylog-0.3.0.tar` & `atro_pylog-0.4.0.tar`

### file list

```diff
@@ -1,8 +1,8 @@
--rw-r--r--   0        0        0     1604 2023-07-17 21:36:09.801670 atro_pylog-0.3.0/atro_pylog/__init__.py
--rw-r--r--   0        0        0     1050 2023-07-11 19:45:01.356569 atro_pylog-0.3.0/atro_pylog/level.py
--rw-r--r--   0        0        0      363 2023-07-11 19:45:01.356569 atro_pylog-0.3.0/atro_pylog/logger_type.py
--rw-r--r--   0        0        0     1007 2023-07-17 21:35:20.624005 atro_pylog-0.3.0/atro_pylog/opentelemetry_setup.py
--rw-r--r--   0        0        0      127 2023-07-11 19:45:01.356569 atro_pylog-0.3.0/atro_pylog/rich_setup.py
--rw-r--r--   0        0        0      606 2023-07-17 21:36:10.838358 atro_pylog-0.3.0/atro_pylog/settings.py
--rw-r--r--   0        0        0      636 2023-07-17 21:42:27.142670 atro_pylog-0.3.0/pyproject.toml
--rw-r--r--   0        0        0      927 1970-01-01 00:00:00.000000 atro_pylog-0.3.0/PKG-INFO
+-rw-r--r--   0        0        0     1604 2023-07-23 19:46:48.262992 atro_pylog-0.4.0/atro_pylog/__init__.py
+-rw-r--r--   0        0        0     1050 2023-07-11 19:45:01.356569 atro_pylog-0.4.0/atro_pylog/level.py
+-rw-r--r--   0        0        0      363 2023-07-11 19:45:01.356569 atro_pylog-0.4.0/atro_pylog/logger_type.py
+-rw-r--r--   0        0        0     1006 2023-07-23 19:47:06.560033 atro_pylog-0.4.0/atro_pylog/opentelemetry_setup.py
+-rw-r--r--   0        0        0      158 2023-07-23 19:46:45.816275 atro_pylog-0.4.0/atro_pylog/rich_setup.py
+-rw-r--r--   0        0        0      603 2023-07-23 19:47:06.556700 atro_pylog-0.4.0/atro_pylog/settings.py
+-rw-r--r--   0        0        0      636 2023-07-23 19:46:56.719832 atro_pylog-0.4.0/pyproject.toml
+-rw-r--r--   0        0        0      927 1970-01-01 00:00:00.000000 atro_pylog-0.4.0/PKG-INFO
```

### Comparing `atro_pylog-0.3.0/atro_pylog/__init__.py` & `atro_pylog-0.4.0/atro_pylog/__init__.py`

 * *Files identical despite different names*

### Comparing `atro_pylog-0.3.0/atro_pylog/level.py` & `atro_pylog-0.4.0/atro_pylog/level.py`

 * *Files identical despite different names*

### Comparing `atro_pylog-0.3.0/atro_pylog/opentelemetry_setup.py` & `atro_pylog-0.4.0/atro_pylog/opentelemetry_setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -3,15 +3,14 @@
 from opentelemetry.exporter.otlp.proto.http._log_exporter import OTLPLogExporter
 from opentelemetry.sdk._logs import LoggerProvider, LoggingHandler
 from opentelemetry.sdk._logs.export import BatchLogRecordProcessor
 from opentelemetry.sdk.resources import Resource
 from opentelemetry.sdk.trace import TracerProvider
 
 
-
 def open_telemetry_logger_setup(level: int, service_name, instance_id, endpoint):
     trace.set_tracer_provider(TracerProvider())
     logger_provider = LoggerProvider(  # type: ignore
         resource=Resource.create(
             {
                 "service.name": service_name,
                 "service.instance.id": instance_id,
```

### Comparing `atro_pylog-0.3.0/atro_pylog/settings.py` & `atro_pylog-0.4.0/atro_pylog/settings.py`

 * *Files 1% similar despite different names*

```diff
@@ -9,13 +9,13 @@
     type: str = "rich"
     level: int | str = logging.DEBUG
     msg_format: str = "%(message)s"
     date_format: str = "%X"
     otel_service_name: str = "pylog"
     otel_instance_id: str = "pylog"
     otel_endpoint: str | None = None
-    
+
     model_config = SettingsConfigDict(
         env_prefix="ATRO_PYLOG_",
         env_file=[(Path.home() / ".config" / "atro" / "pylog.env").as_posix(), ".env"],
         env_file_encoding="utf-8",
-    )
+    )
```

### Comparing `atro_pylog-0.3.0/pyproject.toml` & `atro_pylog-0.4.0/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["poetry-core>=1.0.0"]
 build-backend = "poetry.core.masonry.api"
 
 [tool.poetry]
 name = "atro-pylog"
-version = "0.3.0"
+version = "0.4.0"
 description = "A simple logging library for Python. That either uses Loguru or OpenTelmetry collector (useful for local & cluster logging)."
 authors = ["Atropos <pypi.rising@atro.xyz>"]
 packages = [{ include = "atro_pylog" }]
 
 [tool.poetry.dependencies]
 python = ">=3.7,<4.0"
 rich = "*"
```

### Comparing `atro_pylog-0.3.0/PKG-INFO` & `atro_pylog-0.4.0/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: atro-pylog
-Version: 0.3.0
+Version: 0.4.0
 Summary: A simple logging library for Python. That either uses Loguru or OpenTelmetry collector (useful for local & cluster logging).
 Author: Atropos
 Author-email: pypi.rising@atro.xyz
 Requires-Python: >=3.7,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
```

