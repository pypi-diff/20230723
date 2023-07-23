# Comparing `tmp/fakesnow-0.4.1.tar.gz` & `tmp/fakesnow-0.5.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "fakesnow-0.4.1.tar", last modified: Sun Jul 16 11:59:10 2023, max compression
+gzip compressed data, was "fakesnow-0.5.0.tar", last modified: Sun Jul 23 12:35:59 2023, max compression
```

## Comparing `fakesnow-0.4.1.tar` & `fakesnow-0.5.0.tar`

### file list

```diff
@@ -1,29 +1,29 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 11:59:10.324233 fakesnow-0.4.1/
--rw-r--r--   0 runner    (1001) docker     (123)     1071 2023-07-16 11:59:00.000000 fakesnow-0.4.1/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       36 2023-07-16 11:59:00.000000 fakesnow-0.4.1/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     4454 2023-07-16 11:59:10.324233 fakesnow-0.4.1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2791 2023-07-16 11:59:00.000000 fakesnow-0.4.1/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 11:59:10.320232 fakesnow-0.4.1/fakesnow/
--rw-r--r--   0 runner    (1001) docker     (123)     2992 2023-07-16 11:59:00.000000 fakesnow-0.4.1/fakesnow/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2356 2023-07-16 11:59:00.000000 fakesnow-0.4.1/fakesnow/checks.py
--rw-r--r--   0 runner    (1001) docker     (123)      892 2023-07-16 11:59:00.000000 fakesnow-0.4.1/fakesnow/expr.py
--rw-r--r--   0 runner    (1001) docker     (123)    19626 2023-07-16 11:59:00.000000 fakesnow-0.4.1/fakesnow/fakes.py
--rw-r--r--   0 runner    (1001) docker     (123)      509 2023-07-16 11:59:00.000000 fakesnow-0.4.1/fakesnow/fixtures.py
--rw-r--r--   0 runner    (1001) docker     (123)     3495 2023-07-16 11:59:00.000000 fakesnow-0.4.1/fakesnow/info_schema.py
--rw-r--r--   0 runner    (1001) docker     (123)       80 2023-07-16 11:59:00.000000 fakesnow-0.4.1/fakesnow/py.typed
--rw-r--r--   0 runner    (1001) docker     (123)    22376 2023-07-16 11:59:00.000000 fakesnow-0.4.1/fakesnow/transforms.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 11:59:10.324233 fakesnow-0.4.1/fakesnow.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     4454 2023-07-16 11:59:10.000000 fakesnow-0.4.1/fakesnow.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      478 2023-07-16 11:59:10.000000 fakesnow-0.4.1/fakesnow.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-16 11:59:10.000000 fakesnow-0.4.1/fakesnow.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)      270 2023-07-16 11:59:10.000000 fakesnow-0.4.1/fakesnow.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       14 2023-07-16 11:59:10.000000 fakesnow-0.4.1/fakesnow.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)     2212 2023-07-16 11:59:00.000000 fakesnow-0.4.1/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-16 11:59:10.324233 fakesnow-0.4.1/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)       81 2023-07-16 11:59:00.000000 fakesnow-0.4.1/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-16 11:59:10.324233 fakesnow-0.4.1/tests/
--rw-r--r--   0 runner    (1001) docker     (123)     1801 2023-07-16 11:59:00.000000 fakesnow-0.4.1/tests/test_checks.py
--rw-r--r--   0 runner    (1001) docker     (123)      765 2023-07-16 11:59:00.000000 fakesnow-0.4.1/tests/test_expr.py
--rw-r--r--   0 runner    (1001) docker     (123)    29993 2023-07-16 11:59:00.000000 fakesnow-0.4.1/tests/test_fakes.py
--rw-r--r--   0 runner    (1001) docker     (123)     1602 2023-07-16 11:59:00.000000 fakesnow-0.4.1/tests/test_patch.py
--rw-r--r--   0 runner    (1001) docker     (123)     8196 2023-07-16 11:59:00.000000 fakesnow-0.4.1/tests/test_transforms.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:35:59.002342 fakesnow-0.5.0/
+-rw-r--r--   0 runner    (1001) docker     (123)     1071 2023-07-23 12:35:48.000000 fakesnow-0.5.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       36 2023-07-23 12:35:48.000000 fakesnow-0.5.0/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     4518 2023-07-23 12:35:59.002342 fakesnow-0.5.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2855 2023-07-23 12:35:48.000000 fakesnow-0.5.0/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:35:58.998342 fakesnow-0.5.0/fakesnow/
+-rw-r--r--   0 runner    (1001) docker     (123)     2992 2023-07-23 12:35:48.000000 fakesnow-0.5.0/fakesnow/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2356 2023-07-23 12:35:48.000000 fakesnow-0.5.0/fakesnow/checks.py
+-rw-r--r--   0 runner    (1001) docker     (123)      892 2023-07-23 12:35:48.000000 fakesnow-0.5.0/fakesnow/expr.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20747 2023-07-23 12:35:48.000000 fakesnow-0.5.0/fakesnow/fakes.py
+-rw-r--r--   0 runner    (1001) docker     (123)      509 2023-07-23 12:35:48.000000 fakesnow-0.5.0/fakesnow/fixtures.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3781 2023-07-23 12:35:48.000000 fakesnow-0.5.0/fakesnow/info_schema.py
+-rw-r--r--   0 runner    (1001) docker     (123)       80 2023-07-23 12:35:48.000000 fakesnow-0.5.0/fakesnow/py.typed
+-rw-r--r--   0 runner    (1001) docker     (123)    22305 2023-07-23 12:35:48.000000 fakesnow-0.5.0/fakesnow/transforms.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:35:58.998342 fakesnow-0.5.0/fakesnow.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     4518 2023-07-23 12:35:58.000000 fakesnow-0.5.0/fakesnow.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      478 2023-07-23 12:35:58.000000 fakesnow-0.5.0/fakesnow.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 12:35:58.000000 fakesnow-0.5.0/fakesnow.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      270 2023-07-23 12:35:58.000000 fakesnow-0.5.0/fakesnow.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       14 2023-07-23 12:35:58.000000 fakesnow-0.5.0/fakesnow.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     2212 2023-07-23 12:35:48.000000 fakesnow-0.5.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 12:35:59.002342 fakesnow-0.5.0/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)       81 2023-07-23 12:35:48.000000 fakesnow-0.5.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 12:35:59.002342 fakesnow-0.5.0/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     1801 2023-07-23 12:35:48.000000 fakesnow-0.5.0/tests/test_checks.py
+-rw-r--r--   0 runner    (1001) docker     (123)      765 2023-07-23 12:35:48.000000 fakesnow-0.5.0/tests/test_expr.py
+-rw-r--r--   0 runner    (1001) docker     (123)    30651 2023-07-23 12:35:48.000000 fakesnow-0.5.0/tests/test_fakes.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1602 2023-07-23 12:35:48.000000 fakesnow-0.5.0/tests/test_patch.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8196 2023-07-23 12:35:48.000000 fakesnow-0.5.0/tests/test_transforms.py
```

### Comparing `fakesnow-0.4.1/LICENSE` & `fakesnow-0.5.0/LICENSE`

 * *Files identical despite different names*

### Comparing `fakesnow-0.4.1/PKG-INFO` & `fakesnow-0.5.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: fakesnow
-Version: 0.4.1
+Version: 0.5.0
 Summary: Fake Snowflake Connector for Python. Run Snowflake DB locally.
 License: MIT License
         
         Copyright (c) 2023 Oliver Mannion
         
         Permission is hereby granted, free of charge, to any person obtaining a copy of
         this software and associated documentation files (the "Software"), to deal in
@@ -105,28 +105,30 @@
 def _fakesnow_session() -> Iterator[None]:
     with fakesnow.patch("mymodule.write_pandas"):
         yield
 ```
 
 ## Implementation coverage
 
-- [x] multiple databases
-- [x] cursors
+- [x] cursors and standard SQL
 - [x] [get_result_batches()](https://docs.snowflake.com/en/user-guide/python-connector-api#get_result_batches)
-- [x] [write_pandas(..)](https://docs.snowflake.com/en/user-guide/python-connector-api#write_pandas)
-- [x] table comments
+- [x] information schema
+- [x] multiple databases
 - [x] [qmark binding](https://docs.snowflake.com/en/user-guide/python-connector-example#binding-data)
+- [x] table comments
+- [x] [write_pandas(..)](https://docs.snowflake.com/en/user-guide/python-connector-api#write_pandas)
 - [ ] [access control](https://docs.snowflake.com/en/user-guide/security-access-control-overview)
 - [ ] standalone/out of process api/support for faking non-python connectors
 - [ ] [stored procedures](https://docs.snowflake.com/en/sql-reference/stored-procedures)
 
 Partial support
 
 - [x] date functions
-- [x] tags
+- [x] regex functions
 - [x] semi-structured data
+- [x] tags
 
 For more detail see [tests/test_fakes.py](tests/test_fakes.py)
 
 ## Contributing
 
 See [CONTRIBUTING.md](CONTRIBUTING.md) to get started and develop in this repo.
```

### Comparing `fakesnow-0.4.1/README.md` & `fakesnow-0.5.0/README.md`

 * *Files 7% similar despite different names*

```diff
@@ -71,28 +71,30 @@
 def _fakesnow_session() -> Iterator[None]:
     with fakesnow.patch("mymodule.write_pandas"):
         yield
 ```
 
 ## Implementation coverage
 
-- [x] multiple databases
-- [x] cursors
+- [x] cursors and standard SQL
 - [x] [get_result_batches()](https://docs.snowflake.com/en/user-guide/python-connector-api#get_result_batches)
-- [x] [write_pandas(..)](https://docs.snowflake.com/en/user-guide/python-connector-api#write_pandas)
-- [x] table comments
+- [x] information schema
+- [x] multiple databases
 - [x] [qmark binding](https://docs.snowflake.com/en/user-guide/python-connector-example#binding-data)
+- [x] table comments
+- [x] [write_pandas(..)](https://docs.snowflake.com/en/user-guide/python-connector-api#write_pandas)
 - [ ] [access control](https://docs.snowflake.com/en/user-guide/security-access-control-overview)
 - [ ] standalone/out of process api/support for faking non-python connectors
 - [ ] [stored procedures](https://docs.snowflake.com/en/sql-reference/stored-procedures)
 
 Partial support
 
 - [x] date functions
-- [x] tags
+- [x] regex functions
 - [x] semi-structured data
+- [x] tags
 
 For more detail see [tests/test_fakes.py](tests/test_fakes.py)
 
 ## Contributing
 
 See [CONTRIBUTING.md](CONTRIBUTING.md) to get started and develop in this repo.
```

### Comparing `fakesnow-0.4.1/fakesnow/__init__.py` & `fakesnow-0.5.0/fakesnow/__init__.py`

 * *Files identical despite different names*

### Comparing `fakesnow-0.4.1/fakesnow/checks.py` & `fakesnow-0.5.0/fakesnow/checks.py`

 * *Files identical despite different names*

### Comparing `fakesnow-0.4.1/fakesnow/expr.py` & `fakesnow-0.5.0/fakesnow/expr.py`

 * *Files identical despite different names*

### Comparing `fakesnow-0.4.1/fakesnow/fakes.py` & `fakesnow-0.5.0/fakesnow/fakes.py`

 * *Files 4% similar despite different names*

```diff
@@ -42,14 +42,15 @@
                 are returned as tuples. Defaults to False.
         """
         self._conn = conn
         self._duck_conn = duck_conn
         self._use_dict_result = use_dict_result
         self._last_sql = None
         self._last_params = None
+        self._sqlstate = None
 
     def __enter__(self) -> Self:
         return self
 
     def __exit__(
         self,
         exc_type: Optional[Type[BaseException]] = ...,
@@ -72,15 +73,15 @@
         return FakeSnowflakeCursor._describe_as_result_metadata(self._duck_conn.fetchall())  # noqa: SLF001
 
     @property
     def description(self) -> list[ResultMetadata]:
         # use a cursor to avoid destroying an unfetched result on the main connection
         with self._duck_conn.cursor() as cur:
             assert self._conn.database, "Not implemented when database is None"
-            assert self._conn.schema, "Not implemented when database is None"
+            assert self._conn.schema, "Not implemented when schema is None"
 
             # match database and schema used on the main connection
             cur.execute(f"SET SCHEMA = '{self._conn.database}.{self._conn.schema}'")
             cur.execute(f"DESCRIBE {self._last_sql}", self._last_params)
             meta = FakeSnowflakeCursor._describe_as_result_metadata(cur.fetchall())  # noqa: SLF001
 
         return meta  # type: ignore see https://github.com/duckdb/duckdb/issues/7816
@@ -88,14 +89,28 @@
     def execute(
         self,
         command: str | exp.Expression,
         params: Sequence[Any] | dict[Any, Any] | None = None,
         *args: Any,
         **kwargs: Any,
     ) -> FakeSnowflakeCursor:
+        try:
+            self._sqlstate = None
+            return self._execute(command, params, *args, **kwargs)
+        except snowflake.connector.errors.ProgrammingError as e:
+            self._sqlstate = e.sqlstate
+            raise e
+
+    def _execute(
+        self,
+        command: str | exp.Expression,
+        params: Sequence[Any] | dict[Any, Any] | None = None,
+        *args: Any,
+        **kwargs: Any,
+    ) -> FakeSnowflakeCursor:
         self._arrow_table = None
 
         if isinstance(command, exp.Expression):
             expression = command
         else:
             expression = parse_one(self._rewrite_params(command, params), read="snowflake")
 
@@ -104,21 +119,21 @@
         no_database, no_schema = checks.is_unqualified_table_expression(expression)
 
         if no_database and not self._conn.database_set:
             raise snowflake.connector.errors.ProgrammingError(
                 msg=f"Cannot perform {cmd}. This session does not have a current database. Call 'USE DATABASE', or use a qualified name.",  # noqa: E501
                 errno=90105,
                 sqlstate="22000",
-            ) from None
+            )
         elif no_schema and not self._conn.schema_set:
             raise snowflake.connector.errors.ProgrammingError(
                 msg=f"Cannot perform {cmd}. This session does not have a current schema. Call 'USE SCHEMA', or use a qualified name.",  # noqa: E501
                 errno=90106,
                 sqlstate="22000",
-            ) from None
+            )
 
         transformed = (
             expression.transform(transforms.upper_case_unquoted_identifiers)
             .transform(transforms.set_schema, current_database=self._conn.database)
             .transform(transforms.create_database)
             .transform(transforms.extract_comment)
             .transform(transforms.information_schema_columns_snowflake)
@@ -243,14 +258,22 @@
         return batches
 
     @property
     def rowcount(self) -> int | None:
         # TODO: return number of rows updated/inserted (using returning)
         return None
 
+    @property
+    def sfqid(self) -> str | None:
+        return "fakesnow"
+
+    @property
+    def sqlstate(self) -> str | None:
+        return self._sqlstate
+
     @staticmethod
     def _describe_as_result_metadata(describe_results: list) -> list[ResultMetadata]:
         # fmt: off
         def as_result_metadata(column_name: str, column_type: str, _: str) -> ResultMetadata:
             # see https://docs.snowflake.com/en/user-guide/python-connector-api.html#type-codes
             # and https://arrow.apache.org/docs/python/api/datatypes.html#type-checking
             if column_type == "BIGINT":
@@ -284,14 +307,22 @@
                 return ResultMetadata(
                     name=column_name, type_code=3, display_size=None, internal_size=None, precision=None, scale=None, is_nullable=True          # noqa: E501
                 )
             elif column_type in {"TIMESTAMP", "TIMESTAMP_NS"}:
                 return ResultMetadata(
                     name=column_name, type_code=8, display_size=None, internal_size=None, precision=0, scale=9, is_nullable=True                # noqa: E501
                 )
+            elif column_type == "BLOB":
+                return ResultMetadata(
+                    name=column_name, type_code=11, display_size=None, internal_size=8388608, precision=None, scale=None, is_nullable=True      # noqa: E501
+                )
+            elif column_type == "TIME":
+                return ResultMetadata(
+                    name=column_name, type_code=12, display_size=None, internal_size=None, precision=0, scale=9, is_nullable=True               # noqa: E501
+                )
             else:
                 # TODO handle more types
                 raise NotImplementedError(f"for column type {column_type}")
 
         # fmt: on
 
         meta = [
```

### Comparing `fakesnow-0.4.1/fakesnow/info_schema.py` & `fakesnow-0.5.0/fakesnow/info_schema.py`

 * *Files 10% similar despite different names*

```diff
@@ -33,19 +33,26 @@
 # snowflake integers are 38 digits, base 10, See https://docs.snowflake.com/en/sql-reference/data-types-numeric
 SQL_CREATE_INFORMATION_SCHEMA_COLUMNS_VIEW = Template(
     """
 create view ${catalog}.information_schema.columns_snowflake AS
 select table_catalog, table_schema, table_name, column_name, ordinal_position, column_default, is_nullable,
 case when starts_with(data_type, 'DECIMAL') or data_type='BIGINT' then 'NUMBER'
      when data_type='VARCHAR' then 'TEXT'
+     when data_type='DOUBLE' then 'FLOAT'
+     when data_type='BLOB' then 'BINARY'
+     when data_type='TIMESTAMP' then 'TIMESTAMP_NTZ'
      else data_type end as data_type,
 ext_character_maximum_length as character_maximum_length, ext_character_octet_length as character_octet_length,
-case when data_type='BIGINT' then 38 else numeric_precision end as numeric_precision,
-case when data_type='BIGINT' then 10 else numeric_precision_radix end as numeric_precision_radix,
-numeric_scale,
+case when data_type='BIGINT' then 38
+     when data_type='DOUBLE' then NULL
+    else numeric_precision end as numeric_precision,
+case when data_type='BIGINT' then 10
+    when data_type='DOUBLE' then NULL
+    else numeric_precision_radix end as numeric_precision_radix,
+case when data_type='DOUBLE' then NULL else numeric_scale end as numeric_scale,
 collation_name, is_identity, identity_generation, identity_cycle
 from ${catalog}.information_schema.columns
 left join ${catalog}.information_schema.columns_ext ext
 on ext_table_catalog = table_catalog AND ext_table_schema = table_schema
 AND ext_table_name = table_name AND ext_column_name = column_name
 """
 )
```

### Comparing `fakesnow-0.4.1/fakesnow/transforms.py` & `fakesnow-0.5.0/fakesnow/transforms.py`

 * *Files 0% similar despite different names*

```diff
@@ -177,18 +177,15 @@
     """Convert float to double for 64 bit precision.
 
     Snowflake floats are all 64 bit (ie: double)
     see https://docs.snowflake.com/en/sql-reference/data-types-numeric#float-float4-float8
     """
 
     if isinstance(expression, exp.DataType) and expression.this == exp.DataType.Type.FLOAT:
-        # TODO don't copy!
-        new = expression.copy()
-        new.args["this"] = exp.DataType.Type.DOUBLE
-        return new
+        expression.args["this"] = exp.DataType.Type.DOUBLE
 
     return expression
 
 
 def indices_to_json_extract(expression: exp.Expression) -> exp.Expression:
     """Convert indices on objects and arrays to json_extract.
```

### Comparing `fakesnow-0.4.1/fakesnow.egg-info/PKG-INFO` & `fakesnow-0.5.0/fakesnow.egg-info/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: fakesnow
-Version: 0.4.1
+Version: 0.5.0
 Summary: Fake Snowflake Connector for Python. Run Snowflake DB locally.
 License: MIT License
         
         Copyright (c) 2023 Oliver Mannion
         
         Permission is hereby granted, free of charge, to any person obtaining a copy of
         this software and associated documentation files (the "Software"), to deal in
@@ -105,28 +105,30 @@
 def _fakesnow_session() -> Iterator[None]:
     with fakesnow.patch("mymodule.write_pandas"):
         yield
 ```
 
 ## Implementation coverage
 
-- [x] multiple databases
-- [x] cursors
+- [x] cursors and standard SQL
 - [x] [get_result_batches()](https://docs.snowflake.com/en/user-guide/python-connector-api#get_result_batches)
-- [x] [write_pandas(..)](https://docs.snowflake.com/en/user-guide/python-connector-api#write_pandas)
-- [x] table comments
+- [x] information schema
+- [x] multiple databases
 - [x] [qmark binding](https://docs.snowflake.com/en/user-guide/python-connector-example#binding-data)
+- [x] table comments
+- [x] [write_pandas(..)](https://docs.snowflake.com/en/user-guide/python-connector-api#write_pandas)
 - [ ] [access control](https://docs.snowflake.com/en/user-guide/security-access-control-overview)
 - [ ] standalone/out of process api/support for faking non-python connectors
 - [ ] [stored procedures](https://docs.snowflake.com/en/sql-reference/stored-procedures)
 
 Partial support
 
 - [x] date functions
-- [x] tags
+- [x] regex functions
 - [x] semi-structured data
+- [x] tags
 
 For more detail see [tests/test_fakes.py](tests/test_fakes.py)
 
 ## Contributing
 
 See [CONTRIBUTING.md](CONTRIBUTING.md) to get started and develop in this repo.
```

### Comparing `fakesnow-0.4.1/pyproject.toml` & `fakesnow-0.5.0/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 [project]
 name = "fakesnow"
 description = "Fake Snowflake Connector for Python. Run Snowflake DB locally."
-version = "0.4.1"
+version = "0.5.0"
 readme = "README.md"
 license = { file = "LICENSE" }
 classifiers = ["License :: OSI Approved :: MIT License"]
 keywords = ["snowflake", "snowflakedb", "fake", "local", "mock", "testing"]
 requires-python = ">=3.9"
 dependencies = [
     "duckdb~=0.8.0",
```

### Comparing `fakesnow-0.4.1/tests/test_checks.py` & `fakesnow-0.5.0/tests/test_checks.py`

 * *Files identical despite different names*

### Comparing `fakesnow-0.4.1/tests/test_expr.py` & `fakesnow-0.5.0/tests/test_expr.py`

 * *Files identical despite different names*

### Comparing `fakesnow-0.4.1/tests/test_fakes.py` & `fakesnow-0.5.0/tests/test_fakes.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,17 +1,20 @@
+# ruff: noqa: E501
+
 import datetime
 import json
 
 import pandas as pd
 import pytest
 import pytz
 import snowflake.connector
 import snowflake.connector.cursor
 import snowflake.connector.pandas_tools
 from pandas.testing import assert_frame_equal
+from snowflake.connector.cursor import ResultMetadata
 
 
 def test_alter_table(cur: snowflake.connector.cursor.SnowflakeCursor):
     cur.execute("create table table1 (id int)")
     cur.execute("alter table table1 add column name varchar(20)")
     cur.execute("select name from table1")
 
@@ -58,23 +61,23 @@
         #     in str(excinfo.value)
         # )
 
         with pytest.raises(snowflake.connector.errors.ProgrammingError) as excinfo:
             cur.execute("SELECT * FROM jaffles.customers")
 
         assert (
-            "090105 (22000): Cannot perform SELECT. This session does not have a current database. Call 'USE DATABASE', or use a qualified name."  # noqa: E501
+            "090105 (22000): Cannot perform SELECT. This session does not have a current database. Call 'USE DATABASE', or use a qualified name."
             in str(excinfo.value)
         )
 
         with pytest.raises(snowflake.connector.errors.ProgrammingError) as excinfo:
             cur.execute("create schema jaffles")
 
         assert (
-            "090105 (22000): Cannot perform CREATE SCHEMA. This session does not have a current database. Call 'USE DATABASE', or use a qualified name."  # noqa: E501
+            "090105 (22000): Cannot perform CREATE SCHEMA. This session does not have a current database. Call 'USE DATABASE', or use a qualified name."
             in str(excinfo.value)
         )
 
         with pytest.raises(snowflake.connector.errors.ProgrammingError) as excinfo:
             cur.execute("use schema jaffles")
 
         # assert (
@@ -82,15 +85,15 @@
         #     in str(excinfo.value)
         # )
 
         with pytest.raises(snowflake.connector.errors.ProgrammingError) as excinfo:
             cur.execute("create table customers (ID int, FIRST_NAME varchar, LAST_NAME varchar)")
 
         assert (
-            "090105 (22000): Cannot perform CREATE TABLE. This session does not have a current database. Call 'USE DATABASE', or use a qualified name."  # noqa: E501
+            "090105 (22000): Cannot perform CREATE TABLE. This session does not have a current database. Call 'USE DATABASE', or use a qualified name."
             in str(excinfo.value)
         )
 
 
 def test_connect_without_schema(_fakesnow: None):
     # database will be created but not schema
     with snowflake.connector.connect(database="marts") as conn, conn.cursor() as cur:
@@ -108,15 +111,15 @@
         #     in str(excinfo.value)
         # )
 
         with pytest.raises(snowflake.connector.errors.ProgrammingError) as excinfo:
             cur.execute("create table customers (ID int, FIRST_NAME varchar, LAST_NAME varchar)")
 
         assert (
-            "090106 (22000): Cannot perform CREATE TABLE. This session does not have a current schema. Call 'USE SCHEMA', or use a qualified name."  # noqa: E501
+            "090106 (22000): Cannot perform CREATE TABLE. This session does not have a current schema. Call 'USE SCHEMA', or use a qualified name."
             in str(excinfo.value)
         )
 
         conn.execute_string("CREATE SCHEMA schema1; USE SCHEMA schema1;")
         assert conn.schema == "SCHEMA1"
 
 
@@ -144,15 +147,15 @@
     # can connect with db that doesn't exist
     with snowflake.connector.connect(database="marts") as conn, conn.cursor() as cur:
         # but no valid database set
         with pytest.raises(snowflake.connector.errors.ProgrammingError) as excinfo:
             cur.execute("create table foobar (i int)")
 
         assert (
-            "090105 (22000): Cannot perform CREATE TABLE. This session does not have a current database. Call 'USE DATABASE', or use a qualified name."  # noqa: E501
+            "090105 (22000): Cannot perform CREATE TABLE. This session does not have a current database. Call 'USE DATABASE', or use a qualified name."
             in str(excinfo.value)
         )
 
         # database still present on connection
         assert conn.database == "MARTS"
 
         cur.execute("CREATE database marts")
@@ -160,15 +163,15 @@
     # can connect with schema that doesn't exist
     with snowflake.connector.connect(database="marts", schema="jaffles") as conn, conn.cursor() as cur:
         # but no valid schema set
         with pytest.raises(snowflake.connector.errors.ProgrammingError) as excinfo:
             cur.execute("create table foobar (i int)")
 
         assert (
-            "090106 (22000): Cannot perform CREATE TABLE. This session does not have a current schema. Call 'USE SCHEMA', or use a qualified name."  # noqa: E501
+            "090106 (22000): Cannot perform CREATE TABLE. This session does not have a current schema. Call 'USE SCHEMA', or use a qualified name."
             in str(excinfo.value)
         )
 
         # schema still present on connection
         assert conn.schema == "JAFFLES"
 
 
@@ -180,96 +183,58 @@
             {"current_database()": "DB1", "current_schema()": "SCHEMA1"},
         ]
 
 
 def test_describe(cur: snowflake.connector.cursor.SnowflakeCursor):
     cur.execute(
         """
-        create table customers (
-            ID int, CNAME varchar, AMOUNT decimal(10,2), PCT real, ACTIVE boolean,
-            UPDATE_AT timestamp, UPDATE_AT_NTZ timestamp_ntz(9), INSERTIONDATE DATE
+        create or replace table example (
+            XBOOLEAN BOOLEAN, XDOUBLE DOUBLE, XFLOAT FLOAT,
+            XNUMBER82 NUMBER(8,2), XNUMBER NUMBER, XDECIMAL DECIMAL, XNUMERIC NUMERIC,
+            XINT INT, XINTEGER INTEGER, XBIGINT BIGINT, XSMALLINT SMALLINT, XTINYINT TINYINT, XBYTEINT BYTEINT,
+            XVARCHAR20 VARCHAR(20), XVARCHAR VARCHAR, XTEXT TEXT,
+            XTIMESTAMP TIMESTAMP, XTIMESTAMP_NTZ9 TIMESTAMP_NTZ(9), XDATE DATE, XTIME TIME,
+            XBINARY BINARY
         )
         """
     )
     # fmt: off
     expected_metadata = [
-        snowflake.connector.cursor.ResultMetadata(
-            name="ID", type_code=0, display_size=None, internal_size=None, precision=38, scale=0, is_nullable=True                  # type: ignore # noqa: E501
-        ),
-        snowflake.connector.cursor.ResultMetadata(
-            name="CNAME", type_code=2, display_size=None, internal_size=16777216, precision=None, scale=None, is_nullable=True,     # type: ignore # noqa: E501
-        ),
-        snowflake.connector.cursor.ResultMetadata(
-            name="AMOUNT", type_code=0, display_size=None, internal_size=None, precision=10, scale=2, is_nullable=True,             # type: ignore # noqa: E501
-        ),
-        snowflake.connector.cursor.ResultMetadata(
-            name="PCT", type_code=1, display_size=None, internal_size=None, precision=None, scale=None, is_nullable=True,           # type: ignore # noqa: E501
-        ),
-        snowflake.connector.cursor.ResultMetadata(
-            name="ACTIVE", type_code=13, display_size=None, internal_size=None, precision=None, scale=None, is_nullable=True,       # type: ignore # noqa: E501
-        ),
-        snowflake.connector.cursor.ResultMetadata(
-            name='UPDATE_AT', type_code=8, display_size=None, internal_size=None, precision=0, scale=9, is_nullable=True            # type: ignore # noqa: E501
-        ),
-        snowflake.connector.cursor.ResultMetadata(
-            name='UPDATE_AT_NTZ', type_code=8, display_size=None, internal_size=None, precision=0, scale=9, is_nullable=True        # type: ignore # noqa: E501
-        ),
-        snowflake.connector.cursor.ResultMetadata(
-            name='INSERTIONDATE', type_code=3, display_size=None, internal_size=None, precision=None, scale=None, is_nullable=True  # type: ignore # noqa: E501
-        ),
+        ResultMetadata(name='XBOOLEAN', type_code=13, display_size=None, internal_size=None, precision=None, scale=None, is_nullable=True),
+        ResultMetadata(name='XDOUBLE', type_code=1, display_size=None, internal_size=None, precision=None, scale=None, is_nullable=True),
+        ResultMetadata(name='XFLOAT', type_code=1, display_size=None, internal_size=None, precision=None, scale=None, is_nullable=True),
+        ResultMetadata(name='XNUMBER82', type_code=0, display_size=None, internal_size=None, precision=8, scale=2, is_nullable=True),
+        ResultMetadata(name='XNUMBER', type_code=0, display_size=None, internal_size=None, precision=38, scale=0, is_nullable=True),
+        ResultMetadata(name='XDECIMAL', type_code=0, display_size=None, internal_size=None, precision=38, scale=0, is_nullable=True),
+        ResultMetadata(name='XNUMERIC', type_code=0, display_size=None, internal_size=None, precision=38, scale=0, is_nullable=True),
+        ResultMetadata(name='XINT', type_code=0, display_size=None, internal_size=None, precision=38, scale=0, is_nullable=True),
+        ResultMetadata(name='XINTEGER', type_code=0, display_size=None, internal_size=None, precision=38, scale=0, is_nullable=True),
+        ResultMetadata(name='XBIGINT', type_code=0, display_size=None, internal_size=None, precision=38, scale=0, is_nullable=True),
+        ResultMetadata(name='XSMALLINT', type_code=0, display_size=None, internal_size=None, precision=38, scale=0, is_nullable=True),
+        ResultMetadata(name='XTINYINT', type_code=0, display_size=None, internal_size=None, precision=38, scale=0, is_nullable=True),
+        ResultMetadata(name='XBYTEINT', type_code=0, display_size=None, internal_size=None, precision=38, scale=0, is_nullable=True),
+        # TODO: store actual size
+        ResultMetadata(name='XVARCHAR20', type_code=2, display_size=None, internal_size=16777216, precision=None, scale=None, is_nullable=True),
+        ResultMetadata(name='XVARCHAR', type_code=2, display_size=None, internal_size=16777216, precision=None, scale=None, is_nullable=True),
+        ResultMetadata(name='XTEXT', type_code=2, display_size=None, internal_size=16777216, precision=None, scale=None, is_nullable=True),
+        ResultMetadata(name='XTIMESTAMP', type_code=8, display_size=None, internal_size=None, precision=0, scale=9, is_nullable=True),
+        ResultMetadata(name='XTIMESTAMP_NTZ9', type_code=8, display_size=None, internal_size=None, precision=0, scale=9, is_nullable=True),
+        ResultMetadata(name='XDATE', type_code=3, display_size=None, internal_size=None, precision=None, scale=None, is_nullable=True),
+        ResultMetadata(name='XTIME', type_code=12, display_size=None, internal_size=None, precision=0, scale=9, is_nullable=True),
+        ResultMetadata(name='XBINARY', type_code=11, display_size=None, internal_size=8388608, precision=None, scale=None, is_nullable=True)
     ]
     # fmt: on
 
-    assert cur.describe("select * from customers") == expected_metadata
-
-    cur.execute("select * from customers")
+    assert cur.describe("select * from example") == expected_metadata
+    cur.execute("select * from example")
     assert cur.description == expected_metadata
 
-
-def test_describe_with_params(cur: snowflake.connector.cursor.SnowflakeCursor):
-    cur.execute(
-        """
-        create table customers (
-            ID int, CNAME varchar, AMOUNT decimal(10,2), PCT real, ACTIVE boolean,
-            UPDATE_AT timestamp, UPDATE_AT_NTZ timestamp_ntz(9), INSERTIONDATE DATE
-        )
-        """
-    )
-    # fmt: off
-    expected_metadata = [
-        snowflake.connector.cursor.ResultMetadata(
-            name="ID", type_code=0, display_size=None, internal_size=None, precision=38, scale=0, is_nullable=True                  # type: ignore # noqa: E501
-        ),
-        snowflake.connector.cursor.ResultMetadata(
-            name="CNAME", type_code=2, display_size=None, internal_size=16777216, precision=None, scale=None, is_nullable=True,     # type: ignore # noqa: E501
-        ),
-        snowflake.connector.cursor.ResultMetadata(
-            name="AMOUNT", type_code=0, display_size=None, internal_size=None, precision=10, scale=2, is_nullable=True,             # type: ignore # noqa: E501
-        ),
-        snowflake.connector.cursor.ResultMetadata(
-            name="PCT", type_code=1, display_size=None, internal_size=None, precision=None, scale=None, is_nullable=True,           # type: ignore # noqa: E501
-        ),
-        snowflake.connector.cursor.ResultMetadata(
-            name="ACTIVE", type_code=13, display_size=None, internal_size=None, precision=None, scale=None, is_nullable=True,       # type: ignore # noqa: E501
-        ),
-        snowflake.connector.cursor.ResultMetadata(
-            name='UPDATE_AT', type_code=8, display_size=None, internal_size=None, precision=0, scale=9, is_nullable=True            # type: ignore # noqa: E501
-        ),
-        snowflake.connector.cursor.ResultMetadata(
-            name='UPDATE_AT_NTZ', type_code=8, display_size=None, internal_size=None, precision=0, scale=9, is_nullable=True        # type: ignore # noqa: E501
-        ),
-        snowflake.connector.cursor.ResultMetadata(
-            name='INSERTIONDATE', type_code=3, display_size=None, internal_size=None, precision=None, scale=None, is_nullable=True  # type: ignore # noqa: E501
-        ),
-    ]
-    # fmt: on
-
-    assert cur.describe("select * from customers where id = ?", (1,)) == expected_metadata
-
-    cur.execute("select * from customers where id = ?", (1,))
+    # test with params
+    assert cur.describe("select * from example where XNUMBER = ?", (1,)) == expected_metadata
+    cur.execute("select * from example where XNUMBER = ?", (1,))
     assert cur.description == expected_metadata
 
 
 def test_executemany(cur: snowflake.connector.cursor.SnowflakeCursor):
     cur.execute("create table customers (ID int, FIRST_NAME varchar, LAST_NAME varchar)")
 
     customers = [(1, "Jenny", "P"), (2, "Jasper", "M")]
@@ -386,47 +351,77 @@
         assert sum(batch.rowcount for batch in batches) == 2
 
 
 def test_information_schema_columns_numeric(cur: snowflake.connector.cursor.SnowflakeCursor):
     # see https://docs.snowflake.com/en/sql-reference/data-types-numeric
     cur.execute(
         """
-        create table example (
-            XNUMBER82 NUMBER(8,2), XNUMBER NUMBER, XDECIMAL DECIMAL, XNUMERIC NUMERIC,
+        create or replace table example (
+            XBOOLEAN BOOLEAN, XDOUBLE DOUBLE, XFLOAT FLOAT, XNUMBER82 NUMBER(8,2), XNUMBER NUMBER, XDECIMAL DECIMAL, XNUMERIC NUMERIC,
             XINT INT, XINTEGER INTEGER, XBIGINT BIGINT, XSMALLINT SMALLINT, XTINYINT TINYINT, XBYTEINT BYTEINT
         )
         """
     )
 
     cur.execute(
         """
         select column_name,data_type,numeric_precision,numeric_precision_radix,numeric_scale
         from information_schema.columns where table_name = 'EXAMPLE' order by ordinal_position
         """
     )
 
     assert cur.fetchall() == [
+        ("XBOOLEAN", "BOOLEAN", None, None, None),
+        ("XDOUBLE", "FLOAT", None, None, None),
+        ("XFLOAT", "FLOAT", None, None, None),
         ("XNUMBER82", "NUMBER", 8, 10, 2),
         ("XNUMBER", "NUMBER", 38, 10, 0),
         ("XDECIMAL", "NUMBER", 38, 10, 0),
         ("XNUMERIC", "NUMBER", 38, 10, 0),
         ("XINT", "NUMBER", 38, 10, 0),
         ("XINTEGER", "NUMBER", 38, 10, 0),
         ("XBIGINT", "NUMBER", 38, 10, 0),
         ("XSMALLINT", "NUMBER", 38, 10, 0),
         ("XTINYINT", "NUMBER", 38, 10, 0),
         ("XBYTEINT", "NUMBER", 38, 10, 0),
     ]
 
 
+def test_information_schema_columns_other(cur: snowflake.connector.cursor.SnowflakeCursor):
+    # see https://docs.snowflake.com/en/sql-reference/data-types-datetime
+    cur.execute(
+        """
+        create or replace table example (
+            XTIMESTAMP TIMESTAMP, XTIMESTAMP_NTZ9 TIMESTAMP_NTZ(9), XDATE DATE, XTIME TIME,
+            XBINARY BINARY
+        )
+        """
+    )
+
+    cur.execute(
+        """
+        select column_name,data_type
+        from information_schema.columns where table_name = 'EXAMPLE' order by ordinal_position
+        """
+    )
+
+    assert cur.fetchall() == [
+        ("XTIMESTAMP", "TIMESTAMP_NTZ"),
+        ("XTIMESTAMP_NTZ9", "TIMESTAMP_NTZ"),
+        ("XDATE", "DATE"),
+        ("XTIME", "TIME"),
+        ("XBINARY", "BINARY"),
+    ]
+
+
 def test_information_schema_columns_text(cur: snowflake.connector.cursor.SnowflakeCursor):
     # see https://docs.snowflake.com/en/sql-reference/data-types-text
     cur.execute(
         """
-        create table example (
+        create or replace table example (
             XVARCHAR20 VARCHAR(20), XVARCHAR VARCHAR, XTEXT TEXT
         )
         """
     )
 
     cur.execute(
         """
@@ -503,29 +498,44 @@
 
 def test_semi_structured_types(cur: snowflake.connector.cursor.SnowflakeCursor):
     cur.execute("create table semis (emails array, name object, notes variant)")
     cur.execute(
         """insert into semis(emails, name, notes) SELECT [1, 2], parse_json('{"k": "v1"}'), parse_json('["foo"]')"""
     )
     cur.execute(
-        """insert into semis(emails, name, notes) VALUES ([3,4], parse_json('{"k": "v2"}'), parse_json('{"b": "ar"}'))"""  # noqa: E501
+        """insert into semis(emails, name, notes) VALUES ([3,4], parse_json('{"k": "v2"}'), parse_json('{"b": "ar"}'))"""
     )
 
     # results are returned as strings, because the underlying type is JSON (duckdb) / VARIANT (snowflake)
 
     cur.execute("select emails[0] from semis")
     assert cur.fetchall() == [("1",), ("3",)]
 
     cur.execute("select name['k'] from semis")
     assert cur.fetchall() == [('"v1"',), ('"v2"',)]
 
     cur.execute("select notes[0] from semis")
     assert cur.fetchall() == [('"foo"',), (None,)]
 
 
+def test_sqlstate(cur: snowflake.connector.cursor.SnowflakeCursor):
+    cur.execute("select 'hello world'")
+    # sqlstate is None on success
+    assert cur.sqlstate is None
+
+    with pytest.raises(snowflake.connector.errors.ProgrammingError) as _:
+        cur.execute("select * from this_table_does_not_exist")
+
+    assert cur.sqlstate == "42S02"
+
+
+def test_sfqid(cur: snowflake.connector.cursor.SnowflakeCursor):
+    assert cur.sfqid == "fakesnow"
+
+
 def test_table_comments(cur: snowflake.connector.cursor.SnowflakeCursor):
     def read_comment() -> str:
         cur.execute(
             """SELECT COALESCE(COMMENT, '') FROM INFORMATION_SCHEMA.TABLES
                     WHERE TABLE_NAME = 'INGREDIENTS' AND TABLE_SCHEMA = 'SCHEMA1' LIMIT 1"""
         )
         return cur.fetchall()[0][0]
@@ -622,15 +632,15 @@
         # invalid schema doesn't get set on the connection
         assert not conn.schema
 
         with pytest.raises(snowflake.connector.errors.ProgrammingError) as excinfo:
             cur.execute("create table foobar (i int)")
 
         assert (
-            "090106 (22000): Cannot perform CREATE TABLE. This session does not have a current schema. Call 'USE SCHEMA', or use a qualified name."  # noqa: E501
+            "090106 (22000): Cannot perform CREATE TABLE. This session does not have a current schema. Call 'USE SCHEMA', or use a qualified name."
             in str(excinfo.value)
         )
 
 
 def test_values(conn: snowflake.connector.SnowflakeConnection):
     with conn.cursor(snowflake.connector.cursor.DictCursor) as cur:
         cur.execute("SELECT * FROM VALUES ('Amsterdam', 1), ('London', 2)")
```

### Comparing `fakesnow-0.4.1/tests/test_patch.py` & `fakesnow-0.5.0/tests/test_patch.py`

 * *Files identical despite different names*

### Comparing `fakesnow-0.4.1/tests/test_transforms.py` & `fakesnow-0.5.0/tests/test_transforms.py`

 * *Files identical despite different names*

