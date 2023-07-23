# Comparing `tmp/atro_args-0.2.0.tar.gz` & `tmp/atro_args-0.2.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "atro_args-0.2.0.tar", max compression
+gzip compressed data, was "atro_args-0.2.1.tar", max compression
```

## Comparing `atro_args-0.2.0.tar` & `atro_args-0.2.1.tar`

### file list

```diff
@@ -1,7 +1,7 @@
--rw-r--r--   0        0        0        0 2023-06-17 12:33:58.233092 atro_args-0.2.0/README.md
--rw-r--r--   0        0        0       89 2023-07-23 14:15:04.213219 atro_args-0.2.0/atro_args/__init__.py
--rw-r--r--   0        0        0      267 2023-07-23 14:11:53.169286 atro_args-0.2.0/atro_args/arg.py
--rw-r--r--   0        0        0      147 2023-07-23 14:11:53.169286 atro_args-0.2.0/atro_args/arg_type.py
--rw-r--r--   0        0        0     5670 2023-07-23 14:39:31.620100 atro_args-0.2.0/atro_args/input_args.py
--rw-r--r--   0        0        0      407 2023-07-23 14:11:53.895968 atro_args-0.2.0/pyproject.toml
--rw-r--r--   0        0        0      349 1970-01-01 00:00:00.000000 atro_args-0.2.0/PKG-INFO
+-rw-r--r--   0        0        0        0 2023-06-17 12:33:58.233092 atro_args-0.2.1/README.md
+-rw-r--r--   0        0        0       89 2023-07-23 14:15:04.213219 atro_args-0.2.1/atro_args/__init__.py
+-rw-r--r--   0        0        0      314 2023-07-23 19:54:45.502758 atro_args-0.2.1/atro_args/arg.py
+-rw-r--r--   0        0        0      147 2023-07-23 14:11:53.169286 atro_args-0.2.1/atro_args/arg_type.py
+-rw-r--r--   0        0        0     5677 2023-07-23 19:54:13.448770 atro_args-0.2.1/atro_args/input_args.py
+-rw-r--r--   0        0        0      407 2023-07-23 19:54:58.126350 atro_args-0.2.1/pyproject.toml
+-rw-r--r--   0        0        0      349 1970-01-01 00:00:00.000000 atro_args-0.2.1/PKG-INFO
```

### Comparing `atro_args-0.2.0/atro_args/input_args.py` & `atro_args-0.2.1/atro_args/input_args.py`

 * *Files 2% similar despite different names*

```diff
@@ -134,15 +134,15 @@
             if arg.required and model.get(arg.name) is None:
                 missing_but_required.append(arg.name)
 
         if len(missing_but_required) > 0:
             raise Exception(f"Missing required arguments: '{', '.join(missing_but_required)}'")
 
     def parse_args(self, cli_input_args: Sequence[str] | None = None) -> dict[str, Any]:
-        model: dict[str, Any] = {arg.name: None for arg in self.args}
+        model: dict[str, Any] = {arg.name: arg.default for arg in self.args}
 
         cli_args = self.get_cli_args(cli_input_args)
         env_args = self.get_env_args()
         env_file_args = self.get_env_file_args()
         yaml_file_args = self.get_yaml_file_args()
 
         populated_model = self.populated_model(model, cli_args, env_args, env_file_args, yaml_file_args)
```

