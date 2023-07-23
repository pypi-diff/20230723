# Comparing `tmp/qtgql-0.129.2.tar.gz` & `tmp/qtgql-0.130.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "qtgql-0.129.2.tar", max compression
+gzip compressed data, was "qtgql-0.130.2.tar", max compression
```

## Comparing `qtgql-0.129.2.tar` & `qtgql-0.130.2.tar`

### file list

```diff
@@ -1,37 +1,37 @@
--rw-r--r--   0        0        0     1064 2023-07-17 09:47:31.073072 qtgql-0.129.2/LICENSE
--rw-r--r--   0        0        0     1055 2023-07-17 09:47:31.073072 qtgql-0.129.2/README.md
--rw-r--r--   0        0        0     4307 2023-07-17 09:47:49.493270 qtgql-0.129.2/pyproject.toml
--rw-r--r--   0        0        0        0 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/__init__.py
--rw-r--r--   0        0        0     1866 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/cli.py
--rw-r--r--   0        0        0     1939 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/config.py
--rw-r--r--   0        0        0        0 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/core/__init__.py
--rw-r--r--   0        0        0     1708 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/core/cppref.py
--rw-r--r--   0        0        0       41 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/core/exceptions.py
--rw-r--r--   0        0        0     3393 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/core/graphql_ref.py
--rw-r--r--   0        0        0     1179 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/core/template.py
--rw-r--r--   0        0        0     3226 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/generator.py
--rw-r--r--   0        0        0        0 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/operation/__init__.py
--rw-r--r--   0        0        0     3877 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/operation/definitions.py
--rw-r--r--   0        0        0    16149 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/operation/evaluation.py
--rw-r--r--   0        0        0     4441 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/operation/selections_injection.py
--rw-r--r--   0        0        0      864 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/operation/template.py
--rw-r--r--   0        0        0     2208 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/operation/utils.py
--rw-r--r--   0        0        0        0 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/py.typed
--rw-r--r--   0        0        0        0 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/schema/__init__.py
--rw-r--r--   0        0        0     4600 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/schema/definitions.py
--rw-r--r--   0        0        0     8512 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/schema/evaluation.py
--rw-r--r--   0        0        0     1625 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/schema/template.py
--rw-r--r--   0        0        0      445 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/templates/CMakeLists.jinja.cmake
--rw-r--r--   0        0        0     1699 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/templates/macros/concrete_type_fields.jinja.hpp
--rw-r--r--   0        0        0     3629 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/templates/macros/deserialize_concrete_field.jinja.hpp
--rw-r--r--   0        0        0     2985 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/templates/macros/initialize_proxy_field.jinja.hpp
--rw-r--r--   0        0        0      448 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/templates/macros/iterate_type_condition.jinja.hpp
--rw-r--r--   0        0        0     1060 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/templates/macros/proxy_type_fields.jinja.hpp
--rw-r--r--   0        0        0     4791 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/templates/macros/update_concrete_field.jinja.hpp
--rw-r--r--   0        0        0     4137 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/templates/macros/update_proxy_field.jinja.cpp
--rw-r--r--   0        0        0     5052 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/templates/operation.jinja.cpp
--rw-r--r--   0        0        0     5221 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/templates/operation.jinja.hpp
--rw-r--r--   0        0        0     3237 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/templates/schema.jinja.hpp
--rw-r--r--   0        0        0    18386 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/types.py
--rw-r--r--   0        0        0     1570 2023-07-17 09:47:31.085072 qtgql-0.129.2/qtgqlcodegen/utils.py
--rw-r--r--   0        0        0     1964 1970-01-01 00:00:00.000000 qtgql-0.129.2/PKG-INFO
+-rw-r--r--   0        0        0     1064 2023-07-23 18:59:53.383587 qtgql-0.130.2/LICENSE
+-rw-r--r--   0        0        0     1116 2023-07-23 18:59:53.383587 qtgql-0.130.2/README.md
+-rw-r--r--   0        0        0     4337 2023-07-23 19:00:27.655921 qtgql-0.130.2/pyproject.toml
+-rw-r--r--   0        0        0       29 2023-07-23 19:00:30.167942 qtgql-0.130.2/qtgqlcodegen/__init__.py
+-rw-r--r--   0        0        0     2194 2023-07-23 18:59:53.395587 qtgql-0.130.2/qtgqlcodegen/cli.py
+-rw-r--r--   0        0        0     2116 2023-07-23 18:59:53.395587 qtgql-0.130.2/qtgqlcodegen/config.py
+-rw-r--r--   0        0        0        0 2023-07-23 18:59:53.395587 qtgql-0.130.2/qtgqlcodegen/core/__init__.py
+-rw-r--r--   0        0        0     1708 2023-07-23 18:59:53.395587 qtgql-0.130.2/qtgqlcodegen/core/cppref.py
+-rw-r--r--   0        0        0       41 2023-07-23 18:59:53.395587 qtgql-0.130.2/qtgqlcodegen/core/exceptions.py
+-rw-r--r--   0        0        0     3393 2023-07-23 18:59:53.395587 qtgql-0.130.2/qtgqlcodegen/core/graphql_ref.py
+-rw-r--r--   0        0        0     1216 2023-07-23 18:59:53.395587 qtgql-0.130.2/qtgqlcodegen/core/template.py
+-rw-r--r--   0        0        0     3855 2023-07-23 18:59:53.395587 qtgql-0.130.2/qtgqlcodegen/generator.py
+-rw-r--r--   0        0        0        0 2023-07-23 18:59:53.395587 qtgql-0.130.2/qtgqlcodegen/operation/__init__.py
+-rw-r--r--   0        0        0     3877 2023-07-23 18:59:53.395587 qtgql-0.130.2/qtgqlcodegen/operation/definitions.py
+-rw-r--r--   0        0        0    16149 2023-07-23 18:59:53.395587 qtgql-0.130.2/qtgqlcodegen/operation/evaluation.py
+-rw-r--r--   0        0        0     4441 2023-07-23 18:59:53.395587 qtgql-0.130.2/qtgqlcodegen/operation/selections_injection.py
+-rw-r--r--   0        0        0      864 2023-07-23 18:59:53.395587 qtgql-0.130.2/qtgqlcodegen/operation/template.py
+-rw-r--r--   0        0        0     2208 2023-07-23 18:59:53.395587 qtgql-0.130.2/qtgqlcodegen/operation/utils.py
+-rw-r--r--   0        0        0        0 2023-07-23 18:59:53.395587 qtgql-0.130.2/qtgqlcodegen/py.typed
+-rw-r--r--   0        0        0        0 2023-07-23 18:59:53.395587 qtgql-0.130.2/qtgqlcodegen/schema/__init__.py
+-rw-r--r--   0        0        0     4600 2023-07-23 18:59:53.395587 qtgql-0.130.2/qtgqlcodegen/schema/definitions.py
+-rw-r--r--   0        0        0     8512 2023-07-23 18:59:53.395587 qtgql-0.130.2/qtgqlcodegen/schema/evaluation.py
+-rw-r--r--   0        0        0     1625 2023-07-23 18:59:53.395587 qtgql-0.130.2/qtgqlcodegen/schema/template.py
+-rw-r--r--   0        0        0     2019 2023-07-23 18:59:53.395587 qtgql-0.130.2/qtgqlcodegen/templates/CMakeLists.jinja.cmake
+-rw-r--r--   0        0        0     1699 2023-07-23 18:59:53.395587 qtgql-0.130.2/qtgqlcodegen/templates/macros/concrete_type_fields.jinja.hpp
+-rw-r--r--   0        0        0     3629 2023-07-23 18:59:53.395587 qtgql-0.130.2/qtgqlcodegen/templates/macros/deserialize_concrete_field.jinja.hpp
+-rw-r--r--   0        0        0     2985 2023-07-23 18:59:53.395587 qtgql-0.130.2/qtgqlcodegen/templates/macros/initialize_proxy_field.jinja.hpp
+-rw-r--r--   0        0        0      448 2023-07-23 18:59:53.395587 qtgql-0.130.2/qtgqlcodegen/templates/macros/iterate_type_condition.jinja.hpp
+-rw-r--r--   0        0        0     1137 2023-07-23 18:59:53.399587 qtgql-0.130.2/qtgqlcodegen/templates/macros/proxy_type_fields.jinja.hpp
+-rw-r--r--   0        0        0     4791 2023-07-23 18:59:53.399587 qtgql-0.130.2/qtgqlcodegen/templates/macros/update_concrete_field.jinja.hpp
+-rw-r--r--   0        0        0     4157 2023-07-23 18:59:53.399587 qtgql-0.130.2/qtgqlcodegen/templates/macros/update_proxy_field.jinja.cpp
+-rw-r--r--   0        0        0     5052 2023-07-23 18:59:53.399587 qtgql-0.130.2/qtgqlcodegen/templates/operation.jinja.cpp
+-rw-r--r--   0        0        0     6692 2023-07-23 18:59:53.399587 qtgql-0.130.2/qtgqlcodegen/templates/operation.jinja.hpp
+-rw-r--r--   0        0        0     3237 2023-07-23 18:59:53.399587 qtgql-0.130.2/qtgqlcodegen/templates/schema.jinja.hpp
+-rw-r--r--   0        0        0    18386 2023-07-23 18:59:53.399587 qtgql-0.130.2/qtgqlcodegen/types.py
+-rw-r--r--   0        0        0     1579 2023-07-23 18:59:53.399587 qtgql-0.130.2/qtgqlcodegen/utils.py
+-rw-r--r--   0        0        0     2030 1970-01-01 00:00:00.000000 qtgql-0.130.2/PKG-INFO
```

### Comparing `qtgql-0.129.2/LICENSE` & `qtgql-0.130.2/LICENSE`

 * *Files identical despite different names*

### Comparing `qtgql-0.129.2/README.md` & `qtgql-0.130.2/README.md`

 * *Files 17% similar despite different names*

```diff
@@ -1,13 +1,13 @@
 ## QtGql
 ###  GraphQL client for Qt-QML.
 [![PyPI - Python Version](https://img.shields.io/pypi/pyversions/qtgql?style=for-the-badge)](https://pypi.org/project/qtgql/)
 [![PyPI](https://img.shields.io/pypi/v/qtgql?style=for-the-badge)](https://pypi.org/project/qtgql/)
 [![GitHub Workflow Status (with branch)](https://img.shields.io/github/actions/workflow/status/nrbnlulu/qtgql/tests.yml?branch=main&style=for-the-badge)
 ](https://github.com/nrbnlulu/qtgql/actions/workflows/tests.yml)
-[![Codecov](https://img.shields.io/codecov/c/github/nrbnlulu/qtgql?style=for-the-badge)](https://app.codecov.io/gh/nrbnlulu/qtgql)
+[![Codecov branch](https://img.shields.io/codecov/c/github/qtgql/qtgql/main?style=for-the-badge&link=https%3A%2F%2Fapp.codecov.io%2Fgh%2Fqtgql%2Fqtgql)](https://app.codecov.io/gh/qtgql/qtgql)
 [![Discord](https://img.shields.io/discord/1067870318301032558?label=discord&style=for-the-badge)](https://discord.gg/5vmRRJp9fu)
 ![PyPI - Downloads](https://img.shields.io/pypi/dm/qtgql?style=for-the-badge)
 
 >This project is currently under development, and **it is not** production ready,
 You can play-around and tell us what is wrong / missing / awesome :smile:.
 [Visit the docs for more info](https://nrbnlulu.github.io/qtgql/) (WIP).
```

### Comparing `qtgql-0.129.2/pyproject.toml` & `qtgql-0.130.2/pyproject.toml`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "qtgql"
-version = "0.129.2"
+version = "0.130.2"
 packages = [{ include = "qtgqlcodegen" }]
 description = "Qt framework for building graphql driven QML applications"
 authors = ["Nir <88795475+nrbnlulu@users.noreply.github.com>"]
 maintainers = ["Nir.J Benlulu <nrbnlulu@gmail.com>"]
 license = "MIT"
 readme = "README.md"
 
@@ -15,15 +15,15 @@
 
 [tool.poetry.dependencies]
 python = ">=3.8,<3.12"
 attrs = ">=22.2.0"
 # codegen
 graphql-core = "^3.2.3"
 jinja2 = "^3.1.2"
-typer = "^0.9.0"
+typer = {extras = ["all"], version = "^0.9.0"}
 
 
 
 [tool.poetry.group.dev.dependencies]
 aiohttp = {extras = ["speedups"], version = "^3.8.3"}
 faker = ">=15.3.4,<19.0.0"
 mypy = ">=1.0.1"
```

### Comparing `qtgql-0.129.2/qtgqlcodegen/cli.py` & `qtgql-0.130.2/qtgqlcodegen/cli.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,68 +1,82 @@
 from __future__ import annotations
 
 import glob
-import importlib
-import os
+import importlib.util
 import sys
 from pathlib import Path
 from typing import TYPE_CHECKING
 
 import rich
 import typer
 
+import qtgqlcodegen
+
 if TYPE_CHECKING:
     from qtgqlcodegen.config import QtGqlConfig
 
 console = rich.console.Console()
 app = typer.Typer(pretty_exceptions_show_locals=False)
 
 QTGQL_CONFIG_FNAME = "qtgqlconfig.py"
 
 
+def _create_path_link(path: Path) -> str:
+    return f"[link={path.resolve()}]{path!s}[/link]"
+
+
 def _get_config() -> QtGqlConfig:
-    console.print("[bold blue]Looking for you config file...")
-    res = glob.glob(f"{QTGQL_CONFIG_FNAME}")
+    console.print("[bold blue]Looking for a config file...")
+    res = glob.glob(f"**/{QTGQL_CONFIG_FNAME}", recursive=True)
 
-    if not len(res) > 1:
+    if len(res) > 1:
+        cwd = Path.cwd()
+        results = " \n".join([_create_path_link(cwd / rel) for rel in res])
+
+        console.print(
+            f"[bold red]Found more than one config file. {len(res)}" f" found:\n {results}",
+        )
+        raise typer.Abort()
+    elif len(res) < 1:
         console.print(
-            f"[bold red]Found more than one config file. {len(res)}"
-            f" found: {os.linesep.join(res)}",
+            f"[bold red]Could not find a config file under {_create_path_link(Path.cwd())}",
         )
-        typer.Abort()
-    if len(res) == 0:
-        console.print("[bold red]Found more than one config file using the first one")
-        typer.Abort()
+        raise typer.Abort()
+
     mod_path = Path(res[0]).resolve(True)
     spec = importlib.util.spec_from_file_location(QTGQL_CONFIG_FNAME, mod_path)
     assert spec
     module = importlib.util.module_from_spec(spec)
     sys.modules[QTGQL_CONFIG_FNAME] = module
     assert spec.loader
     spec.loader.exec_module(module)
     return module.config
 
 
 @app.command()
-def gen():
+def gen() -> None:
     """Generates types based on your `QtGqlConfig` configuration object."""
     console.print("[bold blue]Generating...")
     with console.status("Still generating...") as s:
         config = _get_config()
         s.update("[green]Configuration file loaded")
         s.update("[bold blue]Just a second I need some coffee ☕")
         config.generate()
 
     console.print(
-        "[bold green]Types were generated to"
-        f"[link={config.generated_dir.resolve()}]"
-        f"file://{config.generated_dir.resolve()}[/link] successfully!",
+        "[bold green]Generated to" f"{_create_path_link(config.generated_dir)} successfully!",
     )
 
 
 @app.command()
 def hotreload():  # pragma: no cover
     raise NotImplementedError
 
 
+@app.command()
+def version() -> None:
+    """Show the version of qtgql."""
+    console.print(f"[bold blue]{qtgqlcodegen.__version__}")
+
+
 def entrypoint():  # pragma: no cover
     app()
```

### Comparing `qtgql-0.129.2/qtgqlcodegen/config.py` & `qtgql-0.130.2/qtgqlcodegen/config.py`

 * *Files 6% similar despite different names*

```diff
@@ -23,14 +23,19 @@
     env_name: str = "QGqlEnv"
     """The generated types would find the environment by this name.
 
     Also the generated QML imports would fall under this namespace.
     """
     custom_scalars: CustomScalarMap = Factory(dict)
     """Mapping of custom scalars, respected by the schema evaluator."""
+    qml_plugins_path: str = "${CMAKE_BINARY_DIR}/qml"
+    """Qml plugins would be installed under this directory.
+
+    This should suffice for most basic setups.
+    """
     debug: bool = False
     """Templates would render some additional helpers for testing."""
 
     @cached_property
     def schema_path(self) -> Path:
         return self.graphql_dir / "schema.graphql"
 
@@ -46,15 +51,15 @@
         return ret
 
     @cached_property
     def _evaluator(self) -> SchemaGenerator:
         return SchemaGenerator(
             config=self,
             schema=graphql.build_schema(
-                (self.graphql_dir / "schema.graphql").resolve(True).read_text(),
+                (self.graphql_dir / "schema.graphql").resolve(True).read_text("utf-8"),
             ),
         )
 
     def generate(self) -> None:
         self._evaluator.dump()
 
     def __attrs_post_init__(self):
```

### Comparing `qtgql-0.129.2/qtgqlcodegen/core/cppref.py` & `qtgql-0.130.2/qtgqlcodegen/core/cppref.py`

 * *Files identical despite different names*

### Comparing `qtgql-0.129.2/qtgqlcodegen/core/graphql_ref.py` & `qtgql-0.130.2/qtgqlcodegen/core/graphql_ref.py`

 * *Files identical despite different names*

### Comparing `qtgql-0.129.2/qtgqlcodegen/core/template.py` & `qtgql-0.130.2/qtgqlcodegen/core/template.py`

 * *Files 13% similar despite different names*

```diff
@@ -5,17 +5,17 @@
 
 import jinja2
 from attrs import define
 from jinja2 import Environment, PackageLoader, select_autoescape
 
 if TYPE_CHECKING:  # pragma: no cover
     from qtgqlcodegen.config import QtGqlConfig
-    from qtgqlcodegen.utils import FileSpec
+    from qtgqlcodegen.generator import GenerationOutput
 
-template_env = Environment(
+template_env: Environment = Environment(
     loader=PackageLoader("qtgqlcodegen"),
     autoescape=select_autoescape(),
     variable_start_string="👉",  # originally {{ variable }}, using 👉 variable 👈 because C++ uses curly brackets.
     variable_end_string="👈",
     undefined=jinja2.StrictUndefined,
 )
 
@@ -29,15 +29,15 @@
 
 CMAKE_TEMPLATE = template_env.get_template("CMakeLists.jinja.cmake")
 
 
 @define(slots=False)
 class CmakeTemplateContext:
     config: QtGqlConfig
-    sources: list[FileSpec]
+    generation_output: GenerationOutput
 
     @property
     def target_name(self) -> str:
         return self.config.env_name
 
 
 def cmake_template(context: CmakeTemplateContext) -> str:
```

### Comparing `qtgql-0.129.2/qtgqlcodegen/generator.py` & `qtgql-0.130.2/qtgqlcodegen/generator.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,12 +1,13 @@
 from __future__ import annotations
 
 from typing import TYPE_CHECKING
 
 import graphql
+from attr import define
 
 from qtgqlcodegen.core.exceptions import QtGqlException
 from qtgqlcodegen.core.template import CmakeTemplateContext, cmake_template
 from qtgqlcodegen.operation.evaluation import evaluate_operations
 from qtgqlcodegen.operation.template import OperationTemplateContext
 from qtgqlcodegen.schema.evaluation import evaluate_schema
 from qtgqlcodegen.schema.template import (
@@ -18,22 +19,40 @@
 from qtgqlcodegen.types import BuiltinScalars
 from qtgqlcodegen.utils import FileSpec
 
 if TYPE_CHECKING:
     from qtgqlcodegen.config import QtGqlConfig
 
 
+@define
+class OperationOutput:
+    name: str
+    sources: list[FileSpec]
+
+
+@define
+class GenerationOutput:
+    schema: FileSpec
+    operations: list[OperationOutput]
+
+    def dump(self) -> None:
+        self.schema.dump()
+        for op in self.operations:
+            for source in op.sources:
+                source.dump()
+
+
 class SchemaGenerator:
     def __init__(self, config: QtGqlConfig, schema: graphql.GraphQLSchema):
         self.gql_schema = schema
         self.config = config
         self.schema_type_info = evaluate_schema(schema, self.config.custom_scalars)
 
-    def generate(self) -> list[FileSpec]:
-        operations: list[FileSpec] = self._generate_operations()
+    def generate(self) -> GenerationOutput:
+        operations = self._generate_operations()
         context = SchemaTemplateContext(
             enums=list(self.schema_type_info.enums.values()),
             types=[
                 t
                 for name, t in self.schema_type_info.object_types.items()
                 if name not in BuiltinScalars.keys
             ],
@@ -42,49 +61,56 @@
             config=self.config,
         )
         schema_hpp = FileSpec(
             content=schema_types_template_hpp(context),
             path=self.config.generated_dir / "schema.hpp",
         )
 
-        return [schema_hpp, *operations]
-
-    def _generate_operations(self) -> list[FileSpec]:
-        operations_document = graphql.parse(self.config.operations_dir.read_text())
+        return GenerationOutput(
+            schema=schema_hpp,
+            operations=operations,
+        )
 
+    def _generate_operations(self) -> list[OperationOutput]:
+        operations_document = graphql.parse(self.config.operations_dir.read_text("utf-8"))
         # validate the operation against the static schema
         if errors := graphql.validate(self.gql_schema, operations_document):
             raise QtGqlException([error.formatted for error in errors])
 
         operations = evaluate_operations(operations_document, self.schema_type_info)
-        ret: list[FileSpec] = []
+        ret: list[OperationOutput] = []
         for op_name, op in operations.items():
             context = OperationTemplateContext(
                 operation=op,
                 config=self.config,
                 debug=self.config.debug,
             )
 
             ret.append(
-                FileSpec(
-                    content=operation_hpp_template(context=context),
-                    path=self.config.generated_dir / f"{op_name}.hpp",
-                ),
-            )
-            ret.append(
-                FileSpec(
-                    content=operation_cpp_template(context=context),
-                    path=self.config.generated_dir / f"{op_name}.cpp",
+                OperationOutput(
+                    name=op_name,
+                    sources=[
+                        FileSpec(
+                            content=operation_hpp_template(context=context),
+                            path=self.config.generated_dir / f"{op_name}.hpp",
+                        ),
+                        FileSpec(
+                            content=operation_cpp_template(context=context),
+                            path=self.config.generated_dir / f"{op_name}.cpp",
+                        ),
+                    ],
                 ),
             )
+
         return ret
 
     def dump(self):
-        sources = self.generate()
+        generation_output = self.generate()
 
         cmake = FileSpec(
-            content=cmake_template(CmakeTemplateContext(config=self.config, sources=sources)),
+            content=cmake_template(
+                CmakeTemplateContext(config=self.config, generation_output=generation_output),
+            ),
             path=self.config.generated_dir / "CMakeLists.txt",
         )
-        sources.append(cmake)
-        for f in sources:
-            f.dump()
+        generation_output.dump()
+        cmake.dump()
```

### Comparing `qtgql-0.129.2/qtgqlcodegen/operation/definitions.py` & `qtgql-0.130.2/qtgqlcodegen/operation/definitions.py`

 * *Files identical despite different names*

### Comparing `qtgql-0.129.2/qtgqlcodegen/operation/evaluation.py` & `qtgql-0.130.2/qtgqlcodegen/operation/evaluation.py`

 * *Files identical despite different names*

### Comparing `qtgql-0.129.2/qtgqlcodegen/operation/selections_injection.py` & `qtgql-0.130.2/qtgqlcodegen/operation/selections_injection.py`

 * *Files identical despite different names*

### Comparing `qtgql-0.129.2/qtgqlcodegen/operation/template.py` & `qtgql-0.130.2/qtgqlcodegen/operation/template.py`

 * *Files identical despite different names*

### Comparing `qtgql-0.129.2/qtgqlcodegen/operation/utils.py` & `qtgql-0.130.2/qtgqlcodegen/operation/utils.py`

 * *Files identical despite different names*

### Comparing `qtgql-0.129.2/qtgqlcodegen/schema/definitions.py` & `qtgql-0.130.2/qtgqlcodegen/schema/definitions.py`

 * *Files identical despite different names*

### Comparing `qtgql-0.129.2/qtgqlcodegen/schema/evaluation.py` & `qtgql-0.130.2/qtgqlcodegen/schema/evaluation.py`

 * *Files identical despite different names*

### Comparing `qtgql-0.129.2/qtgqlcodegen/schema/template.py` & `qtgql-0.130.2/qtgqlcodegen/schema/template.py`

 * *Files identical despite different names*

### Comparing `qtgql-0.129.2/qtgqlcodegen/templates/macros/concrete_type_fields.jinja.hpp` & `qtgql-0.130.2/qtgqlcodegen/templates/macros/concrete_type_fields.jinja.hpp`

 * *Files identical despite different names*

### Comparing `qtgql-0.129.2/qtgqlcodegen/templates/macros/deserialize_concrete_field.jinja.hpp` & `qtgql-0.130.2/qtgqlcodegen/templates/macros/deserialize_concrete_field.jinja.hpp`

 * *Files identical despite different names*

### Comparing `qtgql-0.129.2/qtgqlcodegen/templates/macros/initialize_proxy_field.jinja.hpp` & `qtgql-0.130.2/qtgqlcodegen/templates/macros/initialize_proxy_field.jinja.hpp`

 * *Files identical despite different names*

### Comparing `qtgql-0.129.2/qtgqlcodegen/templates/macros/proxy_type_fields.jinja.hpp` & `qtgql-0.130.2/qtgqlcodegen/templates/macros/proxy_type_fields.jinja.hpp`

 * *Files 18% similar despite different names*

```diff
@@ -1,9 +1,11 @@
 {% macro proxy_type_fields(t, context) -%}
 Q_OBJECT
+QML_ELEMENT
+QML_UNCREATABLE("QtGql does not supports instantiation via qml")
 Q_PROPERTY(QString  __typeName READ __typename CONSTANT)
 
 {% for f in t.fields -%}
 Q_PROPERTY(const 👉 f.type.property_type 👈 👉 f.name 👈 READ 👉 f.concrete.getter_name 👈 NOTIFY 👉 f.concrete.signal_name 👈);
 {% endfor %}
 signals:
 {%for f in t.fields -%}
```

### Comparing `qtgql-0.129.2/qtgqlcodegen/templates/macros/update_concrete_field.jinja.hpp` & `qtgql-0.130.2/qtgqlcodegen/templates/macros/update_concrete_field.jinja.hpp`

 * *Files identical despite different names*

### Comparing `qtgql-0.129.2/qtgqlcodegen/templates/macros/update_proxy_field.jinja.cpp` & `qtgql-0.130.2/qtgqlcodegen/templates/macros/update_proxy_field.jinja.cpp`

 * *Files 2% similar despite different names*

```diff
@@ -10,43 +10,41 @@
     auto prev_len = 👉field.private_name👈->rowCount();
     if (new_len < prev_len){
         👉field.private_name👈->removeRows(prev_len - 1, prev_len - new_len);
     }
     for (int i = 0; i < new_len; i++){
         auto concrete = new_data.at(i);
     {% if field.type.of_type.is_queried_object_type -%}
-        if (i > prev_len - 1){
+        if (i > prev_len){
             👉field.private_name👈->insert(i, new 👉field.type.of_type.name👈(operation, concrete));
-        }
-        else {
+        } else {
             auto proxy_to_update = 👉field.private_name👈->get(i);
             if(proxy_to_update){
                 proxy_to_update->qtgql_replace_concrete(concrete);
             }
-            else{
+            else{ {#// handle optionals no need to delete -#}
                 👉field.private_name👈->insert(i, new 👉field.type.of_type.name👈(operation, concrete));
             }
         }
 
     {% elif field.type.of_type.is_queried_union or field.type.of_type.is_queried_interface %}
         auto 👉field.name👈_typename = concrete->__typename();
         {%set type_cond -%}👉field.name👈_typename{% endset -%}
         {% for choice in field.type.of_type.choices %}
         {% set do_on_meets -%}
-        if (i > prev_len - 1){
+        if (i > prev_len){
             👉field.private_name👈->insert(i, new 👉choice.name👈(operation, std::static_pointer_cast<👉choice.concrete.name👈>(concrete)));
-        }
-        else{
+        } else{
             auto proxy_to_update = 👉field.private_name👈->get(i);
             if (proxy_to_update && proxy_to_update->__typename() == "👉choice.concrete.name👈"){
                 qobject_cast<👉choice.property_type👈>(proxy_to_update)->qtgql_replace_concrete(std::static_pointer_cast<👉choice.concrete.name👈>(concrete));
             }
             else{
-                delete proxy_to_update; {# // might have been optional or the type_name changed #}
                 👉field.private_name👈->insert(i, new 👉choice.name👈(operation, std::static_pointer_cast<👉choice.concrete.name👈>(concrete)));
+                delete proxy_to_update; {# // might have been optional or the type_name changed #}
             }
 
         }
 
         {% endset %}
         👉iterate_type_condition(choice,type_cond, do_on_meets, loop)👈
         {% endfor %}
```

### Comparing `qtgql-0.129.2/qtgqlcodegen/templates/operation.jinja.cpp` & `qtgql-0.130.2/qtgqlcodegen/templates/operation.jinja.cpp`

 * *Files identical despite different names*

### Comparing `qtgql-0.129.2/qtgqlcodegen/templates/operation.jinja.hpp` & `qtgql-0.130.2/qtgqlcodegen/templates/operation.jinja.hpp`

 * *Files 18% similar despite different names*

```diff
@@ -1,14 +1,15 @@
 {%- from "macros/deserialize_concrete_field.jinja.hpp" import  deserialize_concrete_field -%}
 {%- from "macros/proxy_type_fields.jinja.hpp" import  proxy_type_fields -%}
 {%- from "macros/update_proxy_field.jinja.cpp" import  update_proxy_field -%}
 #pragma once
 #include "./schema.hpp"
 #include <qtgql/gqlwstransport/gqlwstransport.hpp>
 #include <QObject>
+#include <QtQml/qqmlregistration.h>
 
 namespace 👉 context.config.env_name 👈::👉context.ns👈{
 class 👉 context.operation.name 👈;
 
 namespace deserializers{
 {% for t in context.operation.narrowed_types if not t.concrete.is_root -%}
 std::shared_ptr<👉 t.concrete.name 👈> des_👉 t.name 👈(const QJsonObject& data, const 👉 context.operation.name 👈 * operation);
@@ -23,26 +24,23 @@
 void update_👉 t.name 👈(👉 t.concrete.member_type_arg 👈 inst, const QJsonObject &data, const 👉 context.operation.name 👈 * operation);
 {% endfor -%}
 };
 
 // ------------ Narrowed Interfaces ------------
 {% for t in context.operation.interfaces -%}
 class 👉 t.name 👈: public 👉 context.qtgql_types.ObjectTypeABC.name 👈{
+
 👉 proxy_type_fields(t, context) 👈
 public:
     using 👉 context.qtgql_types.ObjectTypeABC.name 👈::👉 context.qtgql_types.ObjectTypeABC.last 👈;
 {% for f in t.fields -%}
 [[nodiscard]] inline virtual const 👉 f.type.property_type 👈  👉 f.concrete.getter_name 👈() const {
 throw qtgql::exceptions::InterfaceDirectAccessError("👉t.concrete.name👈");
 }
 {% endfor %}
-public:
-[[nodiscard]] virtual const QString & __typename() const{
-    throw qtgql::exceptions::InterfaceDirectAccessError("👉t.concrete.name👈");
-}
 };
 {% endfor %}
 // ------------ Narrowed Object types ------------
 {% for t in context.operation.narrowed_types %}
 class 👉 t.name 👈: public 👉 context.qtgql_types.ObjectTypeABC.name if not t.base_interface else t.base_interface.name 👈{
 
 👉context.operation.name👈* m_operation;
@@ -60,15 +58,15 @@
 protected:
     void _qtgql_connect_signals();
 public:
 {% for f in t.fields -%}
 [[nodiscard]] const 👉 f.type.property_type 👈  👉 f.concrete.getter_name 👈() const;
 {% endfor -%}
 public:
-[[nodiscard]] const QString & __typename() const {% if t.base_interface -%}final{% endif %}{
+[[nodiscard]] const QString & __typename() const final{
     return m_inst->__typename();
 }
 };
 {% endfor %}
 
 struct 👉 context.operation.generated_variables_type 👈{
 {% for var in context.operation.variables -%}
@@ -83,15 +81,17 @@
     {% endfor -%}
     return __ret;
     }
 };
 
 class 👉 context.operation.name 👈: public qtgql::gqlwstransport::OperationHandlerABC{
     Q_OBJECT
-Q_PROPERTY(const 👉 context.operation.root_type.name 👈 * data READ data NOTIFY dataChanged);
+    Q_PROPERTY(const 👉 context.operation.root_type.name 👈 * data READ data NOTIFY dataChanged);
+    QML_ELEMENT
+    QML_UNCREATABLE("Must be instantiated as with shared.")
 
 std::optional<👉 context.operation.root_type.name 👈 *> m_data = {};
 
 
 
 inline const QString &ENV_NAME() override{
     static const auto ret = QString("👉 context.config.env_name 👈");
@@ -140,9 +140,52 @@
 void set_variables(👉 context.operation.generated_variables_type 👈 vars){
 vars_inst = vars;
 m_variables = vars_inst.to_json();
 }
 {% endif %}
 
 };
+
+{# // This class exists as an alias class to an operation for qml, since operations
+// must be created with shared pointers. -#}
+class Use👉 context.operation.name 👈: public QObject{
+    Q_OBJECT
+    QML_ELEMENT
+    Q_PROPERTY(const 👉 context.operation.root_type.name 👈 * data READ data NOTIFY dataChanged);
+    Q_PROPERTY(bool completed READ completed NOTIFY completedChanged)
+    Q_PROPERTY(bool operationOnFlight READ operation_on_flight NOTIFY operationOnFlightChanged)
+
+public:
+std::shared_ptr<👉 context.operation.name 👈> m_operation;
+
+Use👉 context.operation.name 👈(QObject *parent = nullptr): QObject(parent){
+    m_operation = 👉 context.operation.name 👈::shared();
+    auto op_ptr = m_operation.get();
+    connect(op_ptr, &👉 context.operation.name 👈::dataChanged, this, [&]{emit dataChanged();});
+    connect(op_ptr, &👉 context.operation.name 👈::completedChanged, this, [&]{emit completedChanged();});
+    connect(op_ptr, &👉 context.operation.name 👈::operationOnFlightChanged, this, [&]{emit operationOnFlightChanged();});
+};
+
+inline const 👉 context.operation.root_type.name 👈 * data() const{
+    return m_operation->data();
+}
+inline bool completed() const{
+    return m_operation->completed();
+}
+inline bool operation_on_flight() const{
+    return m_operation->operation_on_flight();
+}
+
+public slots:
+void fetch(){
+    m_operation->fetch();
+};
+void refetch(){
+    m_operation->refetch();
 };
 
+signals:
+void dataChanged();
+void completedChanged();
+void operationOnFlightChanged();
+};
+};
```

### Comparing `qtgql-0.129.2/qtgqlcodegen/templates/schema.jinja.hpp` & `qtgql-0.130.2/qtgqlcodegen/templates/schema.jinja.hpp`

 * *Files identical despite different names*

### Comparing `qtgql-0.129.2/qtgqlcodegen/types.py` & `qtgql-0.130.2/qtgqlcodegen/types.py`

 * *Files identical despite different names*

### Comparing `qtgql-0.129.2/qtgqlcodegen/utils.py` & `qtgql-0.130.2/qtgqlcodegen/utils.py`

 * *Files 1% similar despite different names*

```diff
@@ -10,15 +10,15 @@
 
 @define
 class FileSpec:
     path: Path
     content: str
 
     def dump(self) -> None:
-        self.path.write_text(self.content)
+        self.path.write_text(self.content, "UTF-8")
 
 
 class AntiForwardRef:
     """i.e:
 
     Union["someString"] would return a ForwardRef, this class is a
     simple hack to just return a type contains the name. Also, this is a
```

### Comparing `qtgql-0.129.2/PKG-INFO` & `qtgql-0.130.2/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: qtgql
-Version: 0.129.2
+Version: 0.130.2
 Summary: Qt framework for building graphql driven QML applications
 License: MIT
 Author: Nir
 Author-email: 88795475+nrbnlulu@users.noreply.github.com
 Maintainer: Nir.J Benlulu
 Maintainer-email: nrbnlulu@gmail.com
 Requires-Python: >=3.8,<3.12
@@ -13,26 +13,26 @@
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Requires-Dist: attrs (>=22.2.0)
 Requires-Dist: graphql-core (>=3.2.3,<4.0.0)
 Requires-Dist: jinja2 (>=3.1.2,<4.0.0)
-Requires-Dist: typer (>=0.9.0,<0.10.0)
+Requires-Dist: typer[all] (>=0.9.0,<0.10.0)
 Project-URL: Documentation, https://nrbnlulu.github.io/qtgql/
 Project-URL: Homepage, https://github.com/nrbnlulu/qtgql
 Description-Content-Type: text/markdown
 
 ## QtGql
 ###  GraphQL client for Qt-QML.
 [![PyPI - Python Version](https://img.shields.io/pypi/pyversions/qtgql?style=for-the-badge)](https://pypi.org/project/qtgql/)
 [![PyPI](https://img.shields.io/pypi/v/qtgql?style=for-the-badge)](https://pypi.org/project/qtgql/)
 [![GitHub Workflow Status (with branch)](https://img.shields.io/github/actions/workflow/status/nrbnlulu/qtgql/tests.yml?branch=main&style=for-the-badge)
 ](https://github.com/nrbnlulu/qtgql/actions/workflows/tests.yml)
-[![Codecov](https://img.shields.io/codecov/c/github/nrbnlulu/qtgql?style=for-the-badge)](https://app.codecov.io/gh/nrbnlulu/qtgql)
+[![Codecov branch](https://img.shields.io/codecov/c/github/qtgql/qtgql/main?style=for-the-badge&link=https%3A%2F%2Fapp.codecov.io%2Fgh%2Fqtgql%2Fqtgql)](https://app.codecov.io/gh/qtgql/qtgql)
 [![Discord](https://img.shields.io/discord/1067870318301032558?label=discord&style=for-the-badge)](https://discord.gg/5vmRRJp9fu)
 ![PyPI - Downloads](https://img.shields.io/pypi/dm/qtgql?style=for-the-badge)
 
 >This project is currently under development, and **it is not** production ready,
 You can play-around and tell us what is wrong / missing / awesome :smile:.
 [Visit the docs for more info](https://nrbnlulu.github.io/qtgql/) (WIP).
```

