# Comparing `tmp/flake8_numba-0.2.0.tar.gz` & `tmp/flake8_numba-0.3.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "flake8_numba-0.2.0.tar", max compression
+gzip compressed data, was "flake8_numba-0.3.0.tar", max compression
```

## Comparing `flake8_numba-0.2.0.tar` & `flake8_numba-0.3.0.tar`

### file list

```diff
@@ -1,12 +1,12 @@
--rw-r--r--   0        0        0      201 2023-06-24 11:52:21.698322 flake8_numba-0.2.0/flake8_numba/__init__.py
--rw-r--r--   0        0        0      843 2023-06-25 14:21:05.857971 flake8_numba-0.2.0/flake8_numba/plugin.py
--rw-r--r--   0        0        0     1750 2023-06-25 16:29:47.518837 flake8_numba-0.2.0/flake8_numba/rule.py
--rw-r--r--   0        0        0        0 2023-06-23 19:35:21.903653 flake8_numba-0.2.0/flake8_numba/rules/__init__.py
--rw-r--r--   0        0        0     5565 2023-06-25 19:48:43.376303 flake8_numba-0.2.0/flake8_numba/rules/nba0.py
--rw-r--r--   0        0        0      925 2023-06-25 14:51:48.142394 flake8_numba-0.2.0/flake8_numba/rules/nba1.py
--rw-r--r--   0        0        0    13002 2023-07-01 11:08:24.532910 flake8_numba-0.2.0/flake8_numba/rules/nba2.py
--rw-r--r--   0        0        0     8509 2023-06-25 16:53:55.966188 flake8_numba-0.2.0/flake8_numba/utils.py
--rw-r--r--   0        0        0     2404 2023-06-25 16:29:47.522473 flake8_numba-0.2.0/flake8_numba/visitor.py
--rw-r--r--   0        0        0     3069 2023-07-01 11:12:07.454856 flake8_numba-0.2.0/pyproject.toml
--rw-r--r--   0        0        0      747 2023-06-24 18:31:42.168344 flake8_numba-0.2.0/README.md
--rw-r--r--   0        0        0     1178 1970-01-01 00:00:00.000000 flake8_numba-0.2.0/PKG-INFO
+-rw-r--r--   0        0        0      161 2023-07-22 18:40:09.308732 flake8_numba-0.3.0/flake8_numba/__init__.py
+-rw-r--r--   0        0        0      843 2023-06-25 14:21:05.857971 flake8_numba-0.3.0/flake8_numba/plugin.py
+-rw-r--r--   0        0        0     2056 2023-07-22 18:40:09.324729 flake8_numba-0.3.0/flake8_numba/rule.py
+-rw-r--r--   0        0        0      135 2023-07-22 18:40:09.324729 flake8_numba-0.3.0/flake8_numba/rules/__init__.py
+-rw-r--r--   0        0        0     5565 2023-07-22 18:38:19.446123 flake8_numba-0.3.0/flake8_numba/rules/nba0.py
+-rw-r--r--   0        0        0     1485 2023-07-22 18:40:09.333367 flake8_numba-0.3.0/flake8_numba/rules/nba1.py
+-rw-r--r--   0        0        0    13013 2023-07-22 18:40:09.336384 flake8_numba-0.3.0/flake8_numba/rules/nba2.py
+-rw-r--r--   0        0        0     8512 2023-07-22 19:05:50.738267 flake8_numba-0.3.0/flake8_numba/utils.py
+-rw-r--r--   0        0        0     1743 2023-07-22 18:40:09.346028 flake8_numba-0.3.0/flake8_numba/visitor.py
+-rw-r--r--   0        0        0     3063 2023-07-22 18:40:09.346028 flake8_numba-0.3.0/pyproject.toml
+-rw-r--r--   0        0        0     1074 2023-07-22 19:14:46.872184 flake8_numba-0.3.0/README.md
+-rw-r--r--   0        0        0     1489 1970-01-01 00:00:00.000000 flake8_numba-0.3.0/PKG-INFO
```

### Comparing `flake8_numba-0.2.0/flake8_numba/plugin.py` & `flake8_numba-0.3.0/flake8_numba/plugin.py`

 * *Files identical despite different names*

### Comparing `flake8_numba-0.2.0/flake8_numba/rule.py` & `flake8_numba-0.3.0/flake8_numba/rule.py`

 * *Files 7% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 """Module that implement the logic that all rules will follow."""
 import ast
 from abc import ABC, abstractmethod
-from typing import NamedTuple, Optional, final
+from typing import ClassVar, NamedTuple, Optional, final
 
 
 class Error(NamedTuple):
     """Class that holds all the information relative to a single error."""
 
     line: int
     """Line where the error is located."""
@@ -14,14 +14,17 @@
     message: str
     """Message of the error."""
 
 
 class Rule(ABC):
     """Skeleton that all rules have to meet."""
 
+    all_rules: ClassVar[list["Rule"]] = []
+    """List of all rules implemented so far."""
+
     @final
     def check(self, node: ast.FunctionDef, errors: list[Error]) -> bool:
         """Check if the current rule is found to be broken within node.
 
         Returns `True` if no error. `False` if it was ok.
 
         Args:
@@ -52,7 +55,12 @@
 
         Meant to be overridden to add more rules.
 
         Returns:
              set[type[Rule], ...]: Tuple with all codes.
         """
         return set()
+
+    def __init_subclass__(cls, **kwargs: object):
+        """Populate `all_rules` variable with all subclasses."""
+        super().__init_subclass__(**kwargs)
+        cls.all_rules.append(cls())
```

### Comparing `flake8_numba-0.2.0/flake8_numba/rules/nba0.py` & `flake8_numba-0.3.0/flake8_numba/rules/nba0.py`

 * *Files identical despite different names*

### Comparing `flake8_numba-0.2.0/flake8_numba/rules/nba1.py` & `flake8_numba-0.3.0/flake8_numba/rules/nba1.py`

 * *Files 11% similar despite different names*

```diff
@@ -20,7 +20,23 @@
                     return_elements = statement.value.elts
                     return_count = max(return_count, len(return_elements))
 
         if return_count > 1:
             msg = "NBA101: Only one value can be returned."
             return Error(statement.lineno, statement.col_offset, msg)
         return None
+
+
+class NBA102(Rule):
+    """Expected return value for the function."""
+
+    def _check(self, node: ast.FunctionDef) -> Optional[Error]:
+        if not is_decorated_with("vectorize", node):
+            return None
+
+        # Check the 'return' statement in the function body
+        for statement in node.body:
+            if isinstance(statement, ast.Return):
+                return None
+
+        msg = "NBA102: Functions decorated with `vectorize` must have one return value"
+        return Error(statement.lineno, statement.col_offset, msg)
```

### Comparing `flake8_numba-0.2.0/flake8_numba/rules/nba2.py` & `flake8_numba-0.3.0/flake8_numba/rules/nba2.py`

 * *Files 1% similar despite different names*

```diff
@@ -254,16 +254,16 @@
             ):
                 value = sub_node.targets[0].value
                 if isinstance(value, ast.Name) and value.id in outputs_to_be_modified:
                     outputs_to_be_modified.remove(value.id)
 
         if outputs_to_be_modified:
             msg = (
-                "NBA209: Not all output variables are assigned "
-                f"{list(outputs_to_be_modified)}"
+                "NBA209: Not all output variables are assigned: "
+                f"{','.join(list(outputs_to_be_modified))}"
             )
             return Error(location.line, location.column, message=msg)
         return None
 
     @property
     def depends_on(self) -> set[type[Rule]]:
         return {NBA201, NBA202, NBA203, NBA204, NBA205, nba0.NBA005}
```

### Comparing `flake8_numba-0.2.0/flake8_numba/utils.py` & `flake8_numba-0.3.0/flake8_numba/utils.py`

 * *Files 0% similar despite different names*

```diff
@@ -226,15 +226,15 @@
     arg = node.decorator_list[0].args[at]  # type: ignore
     location = Location(line=arg.lineno, column=arg.col_offset)
     original_str = ast.unparse(arg)
     custom_to_standard = _dct_custom_alias_to_standard_numba()
     new_str = original_str
     while True:
         try:
-            return eval(new_str), location  # noqa: PGH
+            return eval(new_str), location  # noqa: PGH001
         except NameError as name_error:
             not_found_variable_name = name_error.args[0].split()[1].strip("'")
             if not_found_variable_name == "nb":
                 new_str = new_str.replace("nb.", "")
             elif not_found_variable_name in custom_to_standard:
                 new_str = new_str.replace(
                     not_found_variable_name, custom_to_standard[not_found_variable_name]
```

### Comparing `flake8_numba-0.2.0/flake8_numba/visitor.py` & `flake8_numba-0.3.0/flake8_numba/visitor.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,54 +1,34 @@
 """Module that implements the visitor logic.
 
 This logic is in charge of executing specific code whenever some specific nodes within
 the code are detected.
 """
 import ast
-import inspect
-from collections.abc import Sequence
-from functools import lru_cache
-from typing import Any
-
-from flake8_numba.rule import Error, Rule
-from flake8_numba.rules import nba0, nba1, nba2
-
-
-@lru_cache
-def _all_rules() -> Sequence[Rule]:
-    class_list = []
-    members: list[Any] = []
-    members.extend(inspect.getmembers(nba0))
-    members.extend(inspect.getmembers(nba1))
-    members.extend(inspect.getmembers(nba2))
-    # Obtener todos los miembros del módulo
-    for _, obj in members:
-        # Verificar si el miembro es una clase
-        if inspect.isclass(obj) and issubclass(obj, Rule) and obj != Rule:
-            class_list.append(obj())
-    return class_list
+
+from flake8_numba import Error, Rule
 
 
 class Visitor(ast.NodeVisitor):
     """Visitor class in charge of parsing one entire file."""
 
     def __init__(self) -> None:
         """Insantiate a list of empty errors just after being declared."""
         self.errors: list[Error] = []
-        self.pending_rules: set[Rule] = set(_all_rules())
+        self.pending_rules: set[Rule] = set(Rule.all_rules)
         self.rules_raised: set[type[Rule]] = set()
 
     def visit_FunctionDef(self, node: ast.FunctionDef) -> None:  # noqa: N802
         """Called whenever a function definition is found.
 
         Args:
             node (ast.FunctionDef): Node containing all the information relative to
                 the function definition.
         """
-        for rule in _all_rules():
+        for rule in Rule.all_rules:
             self.process_rule(rule, node)
         self.generic_visit(node)
 
     def process_rule(self, rule: Rule, node: ast.FunctionDef) -> None:
         # Process dependencies
         if rule.depends_on:
             for pre_rule in rule.depends_on:
```

#### encoding

```diff
@@ -1 +1 @@
-utf-8
+us-ascii
```

### Comparing `flake8_numba-0.2.0/pyproject.toml` & `flake8_numba-0.3.0/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "flake8_numba"
-version = "0.2.0"
+version = "0.3.0"
 description = "Perform checks over numba usage"
 authors = ["Manuel Floriano Vázquez <mflovaa@gmail.com>"]
 readme = "README.md"
 packages = [{include = "flake8_numba"}]
 
 [tool.poetry.dependencies]
 python = "^3.9"
@@ -61,15 +61,15 @@
 [tool.codespell]
 skip = '.venv'
 
 [tool.ruff]
 line-length = 90
 target-version = "py39"
 exclude = [".venv", "data"]
-select = ["F", "E", "I", "N", "D", "UP", "YTT", "ASYNC", "BLE", "B", "A", "C4", "DTZ", "T10", "DJ", "EXE", "FA", "ISC", "ICN", "G", "PIE", "PYI", "PT", "Q", "RSE", "RET", "SLF", "SIM", "TID", "INT", "ARG", "TD", "FIX", "PD", "PGH", "PL", "FLY", "NPY", "AIR", "RUF"]
+select = ["F", "E", "I", "N", "D", "UP", "YTT", "ASYNC", "BLE", "B", "A", "C4", "DTZ", "T10", "DJ", "EXE", "ISC", "ICN", "G", "PIE", "PYI", "PT", "Q", "RSE", "RET", "SLF", "SIM", "TID", "INT", "ARG", "TD", "FIX", "PD", "PGH", "PL", "FLY", "NPY", "AIR", "RUF"]
 ignore = ["SIM102", "EM101", "PLR", "D100", "D103", "C419", "PGH003", "RUF001", "PD901", "C405", "PLC1901", "UP015", "PLC0414", "I001", "D104", "D102", "PT006", "D101"]
 
 [tool.ruff.pydocstyle]
 convention = "google"  # Docstring convention. Accepts: "google", "numpy", or "pep257".
 
 [tool.ruff.flake8-pytest-style]
 fixture-parentheses = false
```

### Comparing `flake8_numba-0.2.0/README.md` & `flake8_numba-0.3.0/README.md`

 * *Files 25% similar despite different names*

```diff
@@ -1,11 +1,9 @@
 # flake8-numba
 
-[WORK IN PROGRESS, ALPHA VERSION]
-
 Improve your Python development experience with flake8-numba. This plugin integrates with Flake8 to provide
 comprehensive code analysis for projects that make use of numba. When working with numba, many errors are not
 discovered until the code is run. However, many of these issues can be perfectly caught by performing some basic
 syntactical analysis. This tool helps you catch potential errors and enhance code quality effortlessly.
 
 ## Installation
 
@@ -15,8 +13,26 @@
 pip install flake8-numba
 ```
 
 After it calling `flake8` will include all rules defined by this plugin.
 
 ## Rules
 
-Available rules can be read in [RULES.md](RULES.md)
+Some examples are:
+
+```python
+@vectorize([float64(float64, float64)])
+def f(x, y):
+    return x + y, 2  # ERROR: only 1 value can be returned
+```
+
+or:
+
+```python
+# ERROR: Dimensions mismatch (second argument at left is an array but an scalar at right)
+@guvectorize([(float32, float32[:], float32)], "(), () -> ()")
+def func(...) -> None:
+    ...
+```
+
+
+All available rules can be read in `RULES.md`
```

