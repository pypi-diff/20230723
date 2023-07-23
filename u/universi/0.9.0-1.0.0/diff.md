# Comparing `tmp/universi-0.9.0.tar.gz` & `tmp/universi-1.0.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "universi-0.9.0.tar", max compression
+gzip compressed data, was "universi-1.0.0.tar", max compression
```

## Comparing `universi-0.9.0.tar` & `universi-1.0.0.tar`

### file list

```diff
@@ -1,20 +1,20 @@
--rw-r--r--   0        0        0     1072 2023-06-12 19:09:15.569998 universi-0.9.0/LICENSE
--rw-r--r--   0        0        0    21640 2023-07-21 21:25:34.939997 universi-0.9.0/README.md
--rw-r--r--   0        0        0     4072 2023-07-21 18:16:55.923321 universi-0.9.0/pyproject.toml
--rw-r--r--   0        0        0      453 2023-07-12 22:40:12.864421 universi-0.9.0/universi/__init__.py
--rw-r--r--   0        0        0     2821 2023-07-14 12:35:15.746665 universi-0.9.0/universi/_utils.py
--rw-r--r--   0        0        0    22420 2023-07-18 06:54:15.303331 universi-0.9.0/universi/codegen.py
--rw-r--r--   0        0        0      324 2023-07-10 23:48:56.035792 universi-0.9.0/universi/exceptions.py
--rw-r--r--   0        0        0     2841 2023-07-08 14:21:11.688092 universi-0.9.0/universi/fields.py
--rw-r--r--   0        0        0      903 2023-07-06 22:52:01.148105 universi-0.9.0/universi/header.py
--rw-r--r--   0        0        0        0 2023-07-13 08:09:29.390618 universi-0.9.0/universi/py.typed
--rw-r--r--   0        0        0    12077 2023-07-16 13:58:23.713333 universi-0.9.0/universi/routing.py
--rw-r--r--   0        0        0      426 2023-07-16 13:09:25.456661 universi-0.9.0/universi/structure/__init__.py
--rw-r--r--   0        0        0      265 2023-07-08 11:43:06.913473 universi-0.9.0/universi/structure/common.py
--rw-r--r--   0        0        0     4936 2023-07-10 10:22:38.358870 universi-0.9.0/universi/structure/endpoints.py
--rw-r--r--   0        0        0      944 2023-07-08 11:43:06.913473 universi-0.9.0/universi/structure/enums.py
--rw-r--r--   0        0        0     1270 2023-07-14 12:35:15.266665 universi-0.9.0/universi/structure/responses.py
--rw-r--r--   0        0        0     6058 2023-07-16 13:58:29.106666 universi-0.9.0/universi/structure/schemas.py
--rw-r--r--   0        0        0     9907 2023-07-21 21:10:28.899997 universi-0.9.0/universi/structure/versions.py
--rw-r--r--   0        0        0    22824 1970-01-01 00:00:00.000000 universi-0.9.0/setup.py
--rw-r--r--   0        0        0    22227 1970-01-01 00:00:00.000000 universi-0.9.0/PKG-INFO
+-rw-r--r--   0        0        0     1072 2023-06-12 19:09:15.569998 universi-1.0.0/LICENSE
+-rw-r--r--   0        0        0    21659 2023-07-23 11:29:06.959996 universi-1.0.0/README.md
+-rw-r--r--   0        0        0     4072 2023-07-23 11:30:06.756662 universi-1.0.0/pyproject.toml
+-rw-r--r--   0        0        0      463 2023-07-23 10:53:14.969997 universi-1.0.0/universi/__init__.py
+-rw-r--r--   0        0        0     2821 2023-07-14 12:35:15.746665 universi-1.0.0/universi/_utils.py
+-rw-r--r--   0        0        0    23027 2023-07-23 11:28:02.816662 universi-1.0.0/universi/codegen.py
+-rw-r--r--   0        0        0      324 2023-07-10 23:48:56.035792 universi-1.0.0/universi/exceptions.py
+-rw-r--r--   0        0        0     2841 2023-07-08 14:21:11.688092 universi-1.0.0/universi/fields.py
+-rw-r--r--   0        0        0      903 2023-07-06 22:52:01.148105 universi-1.0.0/universi/header.py
+-rw-r--r--   0        0        0        0 2023-07-13 08:09:29.390618 universi-1.0.0/universi/py.typed
+-rw-r--r--   0        0        0    12229 2023-07-23 11:28:00.916663 universi-1.0.0/universi/routing.py
+-rw-r--r--   0        0        0      457 2023-07-23 11:28:00.743329 universi-1.0.0/universi/structure/__init__.py
+-rw-r--r--   0        0        0      265 2023-07-08 11:43:06.913473 universi-1.0.0/universi/structure/common.py
+-rw-r--r--   0        0        0     4936 2023-07-10 10:22:38.358870 universi-1.0.0/universi/structure/endpoints.py
+-rw-r--r--   0        0        0      944 2023-07-08 11:43:06.913473 universi-1.0.0/universi/structure/enums.py
+-rw-r--r--   0        0        0     1270 2023-07-14 12:35:15.266665 universi-1.0.0/universi/structure/responses.py
+-rw-r--r--   0        0        0     6058 2023-07-16 13:58:29.106666 universi-1.0.0/universi/structure/schemas.py
+-rw-r--r--   0        0        0    10648 2023-07-23 11:28:00.883329 universi-1.0.0/universi/structure/versions.py
+-rw-r--r--   0        0        0    22843 1970-01-01 00:00:00.000000 universi-1.0.0/setup.py
+-rw-r--r--   0        0        0    22246 1970-01-01 00:00:00.000000 universi-1.0.0/PKG-INFO
```

### Comparing `universi-0.9.0/LICENSE` & `universi-1.0.0/LICENSE`

 * *Files identical despite different names*

### Comparing `universi-0.9.0/README.md` & `universi-1.0.0/README.md`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 # universi
 
-Modern [Stripe-like](https://stripe.com/blog/api-versioning) API versioning for FastAPI
+Modern [Stripe-like](https://stripe.com/blog/api-versioning) API versioning in FastAPI
 
 ---
 
 <p align="center">
 <a href="https://github.com/ovsyanka83/universi/actions?query=workflow%3ATests+event%3Apush+branch%3Amain" target="_blank">
     <img src="https://github.com/Ovsyanka83/universi/actions/workflows/test.yaml/badge.svg?branch=main&event=push" alt="Test">
 </a>
@@ -166,21 +166,21 @@
 s
 See how we are popping the first address from the list? This is only guaranteed to be possible because we specified earlier that `min_items` for `addresses` must be `1`. If we didn't, then the user would be able to create a user in a newer version that would be impossible to represent in the older version. I.e. If anyone tried to get that user from the older version, they would get a `ResponseValidationError` because the user wouldn't have data for a mandatory `address` field. You need to always keep in mind tht API versioning is only for versioning your **API**, your interface. Your versions must still be completely compatible in terms of data. If they are not, then you are versioning your data and you should really go with a separate app instance. Otherwise, your users will have a hard time migrating back and forth between API versions and so many unexpected errors.
 
 See how we added the `addresses` property? This simple instruction will allow us to use `addresses` even from the old schema, which means that our api route will not need to know anything about versioning. The main goal of universi is to shift the logic of versioning away from your business logic and api endpoints which makes your project easier to navigate and which makes deleting versions a breeze.
 
 ### Grouping Version Changes
 
-Finally, we group the version changes in the `Versions` class. This represents the different versions of your API and the changes between them. You can add any "version changes" to any version. For simplicity, let's use versions 2002 and 2001 which means that we had a single address in API in 2001 and added addresses as a list in 2002's version.
+Finally, we group the version changes in the `VersionBundle` class. This represents the different versions of your API and the changes between them. You can add any "version changes" to any version. For simplicity, let's use versions 2002 and 2001 which means that we had a single address in API in 2001 and added addresses as a list in 2002's version.
 
 ```python
-from universi.structure import Version, Versions
+from universi.structure import Version, VersionBundle
 from datetime import date
 
-versions = Versions(
+versions = VersionBundle(
     Version(date(2002, 1, 1), ChangeAddressToList),
     Version(date(2001, 1, 1)),
 )
 ```
 
 That's it. You're done with describing things. Now you just gotta ask universi to do the rest for you. We'll need the VersionedAPIRouter we used previously, our API versions, and the module representing the latest versions of our schemas.
 
@@ -426,17 +426,17 @@
 
     @convert_response_to_previous_version_for(my_endpoint, my_other_endpoint)
     def change_addresses_to_single_item(cls, data: dict[str, Any]) -> None:
         data["address"] = data.pop("addresses")[0]
 
 ```
 
-It is done by applying `universi.Versions.versioned(...)` decorator to each endpoint which automatically detects the API version by getting it from the [contextvar](#api-version-header-and-context-variables) and applying all version changes until the selected version in reverse. Note that if the version is not set, then no changes will be applied.
+It is done by applying `universi.VersionBundle.versioned(...)` decorator to each endpoint which automatically detects the API version by getting it from the [contextvar](#api-version-header-and-context-variables) and applying all version changes until the selected version in reverse. Note that if the version is not set, then no changes will be applied.
 
-If you want to convert a specific response to a specific version, you can use `universi.Versions.data_to_version(...)`.
+If you want to convert a specific response to a specific version, you can use `universi.VersionBundle.data_to_version(...)`.
 
 ### Version changes with side effects
 
 Sometimes you will use API versioning to handle a breaking change in your **business logic**, not in the schemas themselves. In such cases, it is tempting to add a version check and just follow the new business logic such as:
 
 ```python
 if api_version_var.get() >= date(2022, 11, 11):
@@ -463,21 +463,21 @@
 Then we will have the following check in our business logic:
 
 ```python
 from src.versions import versions, UserAddressIsCheckedInExternalService
 
 
 async def create_user(payload):
-    if UserAddressIsCheckedInExternalService.is_active(versions):
+    if UserAddressIsCheckedInExternalService.is_active:
         check_user_address_exists_in_an_external_service(payload.address)
     ...
 ```
 
 So this change can be contained in any version -- your business logic doesn't know which version it has and shouldn't.
 
 ### API Version header and context variables
 
 Universi automatically converts your data to a correct version and has "version checks" when dealing with side effects as described in [the section above](#version-changes-with-side-effects). It can only do so using a special [context variable](https://docs.python.org/3/library/contextvars.html) that stores the current API version.
 
 Universi has such default variable defined as `universi.api_version_var`. You can also use `universi.get_universi_dependency` to get a `fastapi.Depends` that automatically sets this contextvar based on a header name that you pick.
 
-You can also set the variable yourself or even pass a different compatible contextvar to your `universi.Versions` constructor.
+You can also set the variable yourself or even pass a different compatible contextvar to your `universi.VersionBundle` constructor.
```

### Comparing `universi-0.9.0/pyproject.toml` & `universi-1.0.0/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "universi"
-version = "0.9.0"
+version = "1.0.0"
 description = ""
 authors = ["Stanislav Zmiev <szmiev2000@gmail.com>"]
 license = "MIT"
 readme = "README.md"
 repository = "https://github.com/ovsyanka83/universi"
 
 [tool.poetry.dependencies]
```

### Comparing `universi-0.9.0/universi/_utils.py` & `universi-1.0.0/universi/_utils.py`

 * *Files identical despite different names*

### Comparing `universi-0.9.0/universi/codegen.py` & `universi-1.0.0/universi/codegen.py`

 * *Files 2% similar despite different names*

```diff
@@ -35,51 +35,62 @@
     AlterSchemaSubInstruction,
     OldSchemaDidntHaveField,
     OldSchemaFieldWas,
     OldSchemaHadField,
     SchemaPropertyDefinitionInstruction,
     SchemaPropertyDidntExistInstruction,
 )
-from universi.structure.versions import Version, Versions
+from universi.structure.versions import Version, VersionBundle
 
 from ._utils import Sentinel, get_index_of_base_schema_dir_in_pythonpath
 from .exceptions import CodeGenerationError, InvalidGenerationInstructionError
 from .fields import FieldInfo
 
 _LambdaFunctionName = (lambda: None).__name__  # pragma: no branch
 _FieldName: TypeAlias = str
 _PropertyName: TypeAlias = str
-_dict_of_empty_field_info = {k: getattr(PydanticFieldInfo(), k) for k in PydanticFieldInfo.__slots__}
+_dict_of_empty_field_info = {
+    k: getattr(PydanticFieldInfo(), k) for k in PydanticFieldInfo.__slots__
+}
 
 
 @dataclass(slots=True)
 class ModelInfo:
     fields: dict[_FieldName, tuple[type[BaseModel], ModelField]]
     properties: dict[_PropertyName, Callable[[Any], Any]] = field(default_factory=dict)
 
 
 # TODO: Add enum alteration here
-def regenerate_dir_to_all_versions(template_module: ModuleType, versions: Versions):
-    schemas = {k: ModelInfo(_get_fields_for_model(v)) for k, v in deepcopy(versions.versioned_schemas).items()}
-    enums = {k: (v, {member.name: member.value for member in v}) for k, v in deepcopy(versions.versioned_enums).items()}
+def regenerate_dir_to_all_versions(
+    template_module: ModuleType,
+    versions: VersionBundle,
+):
+    schemas = {
+        k: ModelInfo(_get_fields_for_model(v))
+        for k, v in deepcopy(versions.versioned_schemas).items()
+    }
+    enums = {
+        k: (v, {member.name: member.value for member in v})
+        for k, v in deepcopy(versions.versioned_enums).items()
+    }
 
     for version in versions.versions:
         # NOTE: You'll have to use relative imports
 
         _generate_versioned_directory(template_module, schemas, enums, version.date)
         _apply_migrations(version, schemas, enums)
     _generate_union_directory(template_module, versions)
 
     current_package = template_module.__name__
     while current_package != "":
         importlib.reload(sys.modules[current_package])
         current_package = ".".join(current_package.split(".")[:-1])
 
 
-def _generate_union_directory(template_module: ModuleType, versions: Versions):
+def _generate_union_directory(template_module: ModuleType, versions: VersionBundle):
     template_dir = _get_package_path_from_module(template_module)
     union_dir = template_dir.with_name("unions")
     index_of_base_schema_in_pythonpath = get_index_of_base_schema_dir_in_pythonpath(
         template_module,
         union_dir,
     )
     for _, original_module, parallel_file in _generate_parallel_directory(
@@ -92,25 +103,26 @@
             index_of_base_schema_in_pythonpath,
         )
         parallel_file.write_text(new_module_text)
 
 
 def _get_unionized_version_of_module(
     original_module: ModuleType,
-    versions: Versions,
+    versions: VersionBundle,
     index_of_base_schema_in_pythonpath: int,
 ):
     original_module_parts = original_module.__name__.split(".")
     original_module_parts[index_of_base_schema_in_pythonpath] = "{}"
 
     import_pythonpath_template = (".".join(original_module_parts)).removesuffix(
         ".__init__",
     )
     imported_modules = [
-        import_pythonpath_template.format(_get_version_dir_name(version.date)) for version in versions.versions
+        import_pythonpath_template.format(_get_version_dir_name(version.date))
+        for version in versions.versions
     ]
     imported_modules += [import_pythonpath_template.format("latest")]
     parsed_file = _parse_python_module(original_module)
 
     body = ast.Module(
         [
             ast.ImportFrom(module="universi", names=[ast.alias(name="Field")], level=0),
@@ -158,35 +170,41 @@
         if isinstance(alter_schema_instruction, OldSchemaDidntHaveField):
             # TODO: Check that the user doesn't pop it and change it at the same time
             # TODO: Add a check that field actually exists (it's necessary!)
             field_name_to_field_model.pop(alter_schema_instruction.field_name)
 
         elif isinstance(alter_schema_instruction, OldSchemaFieldWas):
             # TODO: Add a check that field actually exists (it's necessary!)
-            model_field = field_name_to_field_model[alter_schema_instruction.field_name][1]
+            model_field = field_name_to_field_model[
+                alter_schema_instruction.field_name
+            ][1]
             if alter_schema_instruction.type is not Sentinel:
                 if model_field.annotation == alter_schema_instruction.type:
                     raise InvalidGenerationInstructionError(
                         f"You tried to change the type of field '{alter_schema_instruction.field_name}' to '{alter_schema_instruction.type}' in {schema.__name__} but it already has type '{model_field.annotation}'",
                     )
                 model_field.annotation = alter_schema_instruction.type
                 model_field.type_ = convert_generics(alter_schema_instruction.type)
                 model_field.outer_type_ = alter_schema_instruction.type
             field_info = model_field.field_info
 
             if not isinstance(field_info, FieldInfo):
-                dict_of_field_info = {k: getattr(field_info, k) for k in field_info.__slots__}
+                dict_of_field_info = {
+                    k: getattr(field_info, k) for k in field_info.__slots__
+                }
                 if dict_of_field_info == _dict_of_empty_field_info:
                     field_info = FieldInfo()
                     model_field.field_info = field_info
                 else:
                     raise InvalidGenerationInstructionError(
                         f"You have defined a Field using pydantic.fields.Field but you must use universi.Field in {schema.__name__}",
                     )
-            for attr_name in alter_schema_instruction.field_changes.__dataclass_fields__:
+            for (
+                attr_name
+            ) in alter_schema_instruction.field_changes.__dataclass_fields__:
                 attr_value = getattr(alter_schema_instruction.field_changes, attr_name)
                 if attr_value is not Sentinel:
                     setattr(field_info, attr_name, attr_value)
                     field_info._universi_field_names.add(attr_name)
         elif isinstance(alter_schema_instruction, OldSchemaHadField):
             field_name_to_field_model[alter_schema_instruction.field_name] = (
                 schema,
@@ -200,17 +218,22 @@
             )
         elif isinstance(alter_schema_instruction, SchemaPropertyDefinitionInstruction):
             if alter_schema_instruction.name in field_name_to_field_model:
                 raise InvalidGenerationInstructionError(
                     f"You tried to define a property '{alter_schema_instruction.name}' in '{schema.__name__}' "
                     "but there is already a field with that name.",
                 )
-            schema_infos[schema_path].properties[alter_schema_instruction.name] = alter_schema_instruction.function
+            schema_infos[schema_path].properties[
+                alter_schema_instruction.name
+            ] = alter_schema_instruction.function
         elif isinstance(alter_schema_instruction, SchemaPropertyDidntExistInstruction):
-            if alter_schema_instruction.name not in schema_infos[schema_path].properties:
+            if (
+                alter_schema_instruction.name
+                not in schema_infos[schema_path].properties
+            ):
                 raise InvalidGenerationInstructionError(
                     f"You tried to delete a property '{alter_schema_instruction.name}' in '{schema.__name__}' "
                     "but there is no such property defined in any of the migrations.",
                 )
             schema_infos[schema_path].properties.pop(alter_schema_instruction.name)
         else:
             assert_never(alter_schema_instruction)
@@ -229,15 +252,18 @@
                 if member not in enum_member_to_value[1]:
                     raise InvalidGenerationInstructionError(
                         f"Enum member '{member}' was not found in enum '{enum_path}'",
                     )
                 enum_member_to_value[1].pop(member)
         elif isinstance(alter_enum_instruction, EnumHadMembersInstruction):
             for member, member_value in alter_enum_instruction.members.items():
-                if member in enum_member_to_value[1] and enum_member_to_value[1][member] == member_value:
+                if (
+                    member in enum_member_to_value[1]
+                    and enum_member_to_value[1][member] == member_value
+                ):
                     raise InvalidGenerationInstructionError(
                         f"Enum member '{member}' already exists in enum '{enum_path}' with the same value",
                     )
                 else:
                     enum_member_to_value[1][member] = member_value
         else:
             assert_never(alter_enum_instruction)
@@ -398,16 +424,20 @@
 ) -> ast.ClassDef:
     cls_python_path = module_python_path + cls_node.name
     try:
         if cls_python_path in modified_schemas:
             cls_node = _modify_schema_cls(cls_node, modified_schemas[cls_python_path])
         if cls_python_path in modified_enums:
             cls_node = _modify_enum_cls(cls_node, modified_enums[cls_python_path][1])
-    except CodeGenerationError as e:  # pragma: no cover # This is just a safeguard that will likely never be triggered
-        raise CodeGenerationError(f"Failed to migrate class '{cls_node.name}' to an older version.") from e
+    except (
+        CodeGenerationError
+    ) as e:  # pragma: no cover # This is just a safeguard that will likely never be triggered
+        raise CodeGenerationError(
+            f"Failed to migrate class '{cls_node.name}' to an older version.",
+        ) from e
 
     if not cls_node.body:
         cls_node.body = [ast.Pass()]
     return cls_node
 
 
 def _modify_schema_cls(
@@ -420,41 +450,51 @@
             annotation=ast.Name(custom_repr(field[1].annotation)),
             value=ast.Call(
                 func=ast.Name("Field"),
                 args=[],
                 keywords=[
                     ast.keyword(
                         arg=attr,
-                        value=ast.Name(custom_repr(_get_field_from_field_info(field[1], attr))),
+                        value=ast.Name(
+                            custom_repr(_get_field_from_field_info(field[1], attr)),
+                        ),
                     )
                     # TODO: We should lint the code to make sure that the user is not using pydantic.fields.Field instead of universi.Field
                     for attr in getattr(
                         field[1].field_info,
                         "_universi_field_names",
                         (),
                     )
                 ],
             ),
             simple=1,
         )
         for name, field in model_info.fields.items()
     ]
-    property_definitions = [_make_property_ast(name, func) for name, func in model_info.properties.items()]
-    old_body = [n for n in cls_node.body if not isinstance(n, ast.AnnAssign | ast.Pass | ast.Ellipsis)]
+    property_definitions = [
+        _make_property_ast(name, func) for name, func in model_info.properties.items()
+    ]
+    old_body = [
+        n
+        for n in cls_node.body
+        if not isinstance(n, ast.AnnAssign | ast.Pass | ast.Ellipsis)
+    ]
     docstring = _pop_docstring_from_cls_body(old_body)
     cls_node.body = docstring + field_definitions + old_body + property_definitions
 
     return cls_node
 
 
 def _get_field_from_field_info(field: ModelField, attr: str) -> Any:
     field_value = getattr(field.field_info, attr, Sentinel)
     if field_value is Sentinel:
         field_value = field.field_info.extra.get(attr, Sentinel)
-    if field_value is Sentinel:  # pragma: no cover # This is just a safeguard that will most likely never be triggered
+    if (
+        field_value is Sentinel
+    ):  # pragma: no cover # This is just a safeguard that will most likely never be triggered
         raise CodeGenerationError(f"Field '{attr}' is not present in '{field.name}'")
     return field_value
 
 
 # TODO: Type hint these func definitions everywhere
 def _make_property_ast(name: str, func: Callable):
     func_source = inspect.getsource(func)
@@ -474,15 +514,19 @@
             targets=[ast.Name(member, ctx=ast.Store())],
             value=ast.Name(custom_repr(member_value)),
             lineno=0,
         )
         for member, member_value in enum_info.items()
     ]
 
-    old_body = [n for n in cls_node.body if not isinstance(n, ast.AnnAssign | ast.Assign | ast.Pass | ast.Ellipsis)]
+    old_body = [
+        n
+        for n in cls_node.body
+        if not isinstance(n, ast.AnnAssign | ast.Assign | ast.Pass | ast.Ellipsis)
+    ]
     docstring = _pop_docstring_from_cls_body(old_body)
 
     cls_node.body = docstring + new_body + old_body
     return cls_node
 
 
 def _pop_docstring_from_cls_body(old_body: list[ast.stmt]) -> list[ast.stmt]:
@@ -509,15 +553,19 @@
         )
     if isinstance(value, _BaseGenericAlias | GenericAlias):
         return f"{custom_repr(get_origin(value))}[{', '.join(custom_repr(a) for a in get_args(value))}]"
     if isinstance(value, type):
         # TODO: Add tests for constrained types
         # TODO: Be wary of this hack when migrating to pydantic v2
         # This is a hack for pydantic's Constrained types
-        if value.__name__.startswith("Constrained") and hasattr(value, "__origin__") and hasattr(value, "__args__"):
+        if (
+            value.__name__.startswith("Constrained")
+            and hasattr(value, "__origin__")
+            and hasattr(value, "__args__")
+        ):
             return custom_repr(value.__origin__[value.__args__])
         return value.__name__
     if isinstance(value, Enum):
         return PlainRepr(f"{value.__class__.__name__}.{value.name}")
     if isinstance(value, auto):
         return PlainRepr("auto()")
     if isinstance(value, LambdaType) and _LambdaFunctionName == value.__name__:
@@ -536,15 +584,19 @@
     def __repr__(self) -> str:
         return str(self)
 
 
 def _find_a_lambda(source: str) -> str:
     found_lambdas: list[ast.Lambda] = []
     for node in ast.walk(ast.parse(source)):
-        if isinstance(node, ast.keyword) and node.arg == "default_factory" and isinstance(node.value, ast.Lambda):
+        if (
+            isinstance(node, ast.keyword)
+            and node.arg == "default_factory"
+            and isinstance(node.value, ast.Lambda)
+        ):
             found_lambdas.append(node.value)
     if len(found_lambdas) == 1:
         return ast.unparse(found_lambdas[0])
     # These two errors are really hard to cover. Not sure if even possible, honestly :)
     elif len(found_lambdas) == 0:  # pragma: no cover
         raise InvalidGenerationInstructionError(
             f"No lambda found in default_factory even though one was passed: {source}",
```

### Comparing `universi-0.9.0/universi/fields.py` & `universi-1.0.0/universi/fields.py`

 * *Files identical despite different names*

### Comparing `universi-0.9.0/universi/header.py` & `universi-1.0.0/universi/header.py`

 * *Files identical despite different names*

### Comparing `universi-0.9.0/universi/routing.py` & `universi-1.0.0/universi/routing.py`

 * *Files 1% similar despite different names*

```diff
@@ -38,15 +38,15 @@
 from universi.exceptions import RouterGenerationError
 from universi.structure.common import Endpoint
 from universi.structure.endpoints import (
     EndpointDidntExistInstruction,
     EndpointExistedInstruction,
     EndpointHadInstruction,
 )
-from universi.structure.versions import Versions
+from universi.structure.versions import VersionBundle
 
 _T = TypeVar("_T", bound=Callable[..., Any])
 annotation_resolution_lock = Lock()
 
 
 def same_definition_as_in(t: _T) -> Callable[[Callable], _T]:
     def decorator(f: Callable) -> _T:
@@ -79,15 +79,15 @@
             raise LookupError(f"Route not found on endpoint: '{endpoint.__name__}'")
         self._deleted_routes.append(self.routes.pop(index))
         return endpoint
 
     @lock_cache
     def create_versioned_copies(
         self,
-        versions: Versions,
+        versions: VersionBundle,
         *,
         latest_schemas_module: ModuleType | None,
     ) -> dict[datetime.date, Self]:
         router = self
         for route in router.routes + router._deleted_routes:
             if isinstance(route, APIRoute):
                 if not is_async_callable(route.endpoint):
@@ -192,29 +192,34 @@
                 value,
                 version_dir,
             )
             for key, value in annotation.items()
         }
 
     elif isinstance(annotation, list | tuple):
-        return type(annotation)(_change_versions_of_all_annotations(v, version_dir) for v in annotation)
+        return type(annotation)(
+            _change_versions_of_all_annotations(v, version_dir) for v in annotation
+        )
     else:
         return _memoized_change_versions_of_all_annotations(annotation, version_dir)
 
 
 # This cache is not here for speeding things up. It's for preventing the creation of copies of the same object
 # because such copies could produce weird behaviors at runtime, especially if you/fastapi do any comparisons.
 @functools.cache
 def _memoized_change_versions_of_all_annotations(
     annotation: Any,
     version_dir: Path,
 ) -> Any:
     if isinstance(annotation, _BaseGenericAlias | GenericAlias):
         return _change_versions_of_all_annotations(get_origin(annotation), version_dir)[
-            tuple(_change_versions_of_all_annotations(arg, version_dir) for arg in get_args(annotation))
+            tuple(
+                _change_versions_of_all_annotations(arg, version_dir)
+                for arg in get_args(annotation)
+            )
         ]
     elif isinstance(annotation, Depends):
         return Depends(
             _change_versions_of_all_annotations(annotation.dependency, version_dir),
             use_cache=annotation.use_cache,
         )
     elif isinstance(annotation, type):
@@ -248,15 +253,19 @@
 
         new_callable: Any = cast(Any, new_callable)
         new_callable.__annotations__ = _change_versions_of_all_annotations(
             callable_annotations,
             version_dir,
         )
         new_callable.__defaults__ = _change_versions_of_all_annotations(
-            tuple(p.default for p in old_params.values() if p.default is not inspect.Signature.empty),
+            tuple(
+                p.default
+                for p in old_params.values()
+                if p.default is not inspect.Signature.empty
+            ),
             version_dir=version_dir,
         )
         new_callable.__signature__ = _generate_signature(new_callable, old_params)
         return new_callable
     else:
         return annotation
 
@@ -292,11 +301,12 @@
         ),
     )
 
 
 def _get_route_index(routes: list[BaseRoute], endpoint: Endpoint):
     for index, route in enumerate(routes):
         if isinstance(route, APIRoute) and (
-            route.endpoint == endpoint or getattr(route.endpoint, "func", None) == endpoint
+            route.endpoint == endpoint
+            or getattr(route.endpoint, "func", None) == endpoint
         ):
             return index
     return None
```

### Comparing `universi-0.9.0/universi/structure/endpoints.py` & `universi-1.0.0/universi/structure/endpoints.py`

 * *Files identical despite different names*

### Comparing `universi-0.9.0/universi/structure/enums.py` & `universi-1.0.0/universi/structure/enums.py`

 * *Files identical despite different names*

### Comparing `universi-0.9.0/universi/structure/responses.py` & `universi-1.0.0/universi/structure/responses.py`

 * *Files identical despite different names*

### Comparing `universi-0.9.0/universi/structure/schemas.py` & `universi-1.0.0/universi/structure/schemas.py`

 * *Files identical despite different names*

### Comparing `universi-0.9.0/universi/structure/versions.py` & `universi-1.0.0/universi/structure/versions.py`

 * *Files 3% similar despite different names*

```diff
@@ -17,24 +17,33 @@
 from .common import Endpoint, VersionedModel
 from .responses import AlterResponseInstruction
 from .schemas import AlterSchemaSubInstruction, SchemaPropertyDefinitionInstruction
 
 _P = ParamSpec("_P")
 _R = TypeVar("_R")
 VersionDate: TypeAlias = datetime.date
-PossibleInstructions: TypeAlias = AlterSchemaSubInstruction | AlterEndpointSubInstruction | AlterEnumSubInstruction
+PossibleInstructions: TypeAlias = (
+    AlterSchemaSubInstruction | AlterEndpointSubInstruction | AlterEnumSubInstruction
+)
 
 
 class VersionChange:
     description: ClassVar[str] = Sentinel
-    instructions_to_migrate_to_previous_version: ClassVar[Sequence[PossibleInstructions]] = Sentinel
+    instructions_to_migrate_to_previous_version: ClassVar[
+        Sequence[PossibleInstructions]
+    ] = Sentinel
     alter_schema_instructions: ClassVar[Sequence[AlterSchemaSubInstruction]] = Sentinel
     alter_enum_instructions: ClassVar[Sequence[AlterEnumSubInstruction]] = Sentinel
-    alter_endpoint_instructions: ClassVar[Sequence[AlterEndpointSubInstruction]] = Sentinel
-    alter_response_instructions: ClassVar[dict[Endpoint, AlterResponseInstruction]] = Sentinel
+    alter_endpoint_instructions: ClassVar[
+        Sequence[AlterEndpointSubInstruction]
+    ] = Sentinel
+    alter_response_instructions: ClassVar[
+        dict[Endpoint, AlterResponseInstruction]
+    ] = Sentinel
+    _bound_versions: "VersionBundle | None"
 
     def __init_subclass__(cls, _abstract: bool = False) -> None:
         if _abstract:
             return
         if cls.description is Sentinel:
             raise UniversiStructureError(
                 f"Version change description is not set on '{cls.__name__}' but is required.",
@@ -87,14 +96,15 @@
             endpoint: instruction
             for instruction in cls.__dict__.values()
             if isinstance(instruction, AlterResponseInstruction)
             for endpoint in instruction.endpoints
         }
 
         cls._check_no_subclassing()
+        cls._bound_versions = None
 
     @classmethod
     def _check_no_subclassing(cls):
         if cls.mro() != [cls, VersionChange, object]:
             raise TypeError(
                 f"Can't subclass {cls.__name__} as it was never meant to be subclassed.",
             )
@@ -110,52 +120,67 @@
     def _check_no_subclassing(cls):
         if cls.mro() != [cls, VersionChangeWithSideEffects, VersionChange, object]:
             raise TypeError(
                 f"Can't subclass {cls.__name__} as it was never meant to be subclassed.",
             )
 
     @classmethod
-    def is_active(cls, versions: "Versions") -> bool:
-        api_version = versions.api_version_var.get()
-        if cls not in versions._version_changes_to_version_mapping:
+    @property
+    def is_active(cls) -> bool:
+        if (
+            cls._bound_versions is None
+            or cls not in cls._bound_versions._version_changes_to_version_mapping
+        ):
             raise UniversiError(
-                f"You tried to check whether '{cls.__name__}' is active but it was never added into any version change.",
+                f"You tried to check whether '{cls.__name__}' is active but it was never bound to any version.",
             )
+        api_version = cls._bound_versions.api_version_var.get()
         if api_version is None:
             return True
-        return versions._version_changes_to_version_mapping[cls] <= api_version
+        return (
+            cls._bound_versions._version_changes_to_version_mapping[cls] <= api_version
+        )
 
 
 class Version:
     def __init__(
         self,
         date: VersionDate,
         *version_changes: type[VersionChange],
     ) -> None:
         self.date = date
         self.version_changes = version_changes
 
 
-class Versions:
+class VersionBundle:
     def __init__(
         self,
         *versions: Version,
         api_version_var: ContextVar[VersionDate | None] = api_version_var,
     ) -> None:
         self.versions = versions
         self.api_version_var = api_version_var
         if sorted(versions, key=lambda v: v.date, reverse=True) != list(versions):
             raise ValueError(
                 "Versions are not sorted correctly. Please sort them in descending order.",
             )
+        for version in versions:
+            for version_change in version.version_changes:
+                if version_change._bound_versions is not None:
+                    raise UniversiStructureError(
+                        f"You tried to bind version change '{version_change.__name__}' to two different versions. "
+                        "It is prohibited.",
+                    )
+                version_change._bound_versions = self
 
     @functools.cached_property
     def versioned_schemas(self) -> dict[str, type[VersionedModel]]:
         return {
-            instruction.schema.__module__ + instruction.schema.__name__: instruction.schema
+            instruction.schema.__module__
+            + instruction.schema.__name__: instruction.schema
             for version in self.versions
             for version_change in version.version_changes
             for instruction in version_change.alter_schema_instructions
         }
 
     @functools.cached_property
     def versioned_enums(self) -> dict[str, type[Enum]]:
@@ -166,15 +191,19 @@
             for instruction in version_change.alter_enum_instructions
         }
 
     @functools.cached_property
     def _version_changes_to_version_mapping(
         self,
     ) -> dict[type[VersionChange], VersionDate]:
-        return {version_change: version.date for version in self.versions for version_change in version.version_changes}
+        return {
+            version_change: version.date
+            for version in self.versions
+            for version_change in version.version_changes
+        }
 
     # TODO: It might need caching for iteration to speed it up
     def data_to_version(
         self,
         endpoint: Endpoint,
         data: dict[str, Any],
         version: VersionDate,
```

### Comparing `universi-0.9.0/setup.py` & `universi-1.0.0/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -8,17 +8,17 @@
 {'': ['*']}
 
 install_requires = \
 ['fastapi>=0.96.1', 'typing-extensions']
 
 setup_kwargs = {
     'name': 'universi',
-    'version': '0.9.0',
+    'version': '1.0.0',
     'description': '',
-    'long_description': '# universi\n\nModern [Stripe-like](https://stripe.com/blog/api-versioning) API versioning for FastAPI\n\n---\n\n<p align="center">\n<a href="https://github.com/ovsyanka83/universi/actions?query=workflow%3ATests+event%3Apush+branch%3Amain" target="_blank">\n    <img src="https://github.com/Ovsyanka83/universi/actions/workflows/test.yaml/badge.svg?branch=main&event=push" alt="Test">\n</a>\n<a href="https://codecov.io/gh/ovsyanka83/universi" target="_blank">\n    <img src="https://img.shields.io/codecov/c/github/ovsyanka83/universi?color=%2334D058" alt="Coverage">\n</a>\n<a href="https://pypi.org/project/universi/" target="_blank">\n    <img alt="PyPI" src="https://img.shields.io/pypi/v/universi?color=%2334D058&label=pypi%20package" alt="Package version">\n</a>\n<a href="https://pypi.org/project/universi/" target="_blank">\n    <img src="https://img.shields.io/pypi/pyversions/universi?color=%2334D058" alt="Supported Python versions">\n</a>\n</p>\n\n## Installation\n\n```bash\npip install universi\n```\n\n<!---\n# TODO: Note that we don\'t handle "from .schemas import Schema as OtherSchema" case\n# TODO: Need to validate that the user doesn\'t use versioned schemas instead of the latest ones\n-->\n\n## Who is this for?\n\nUniversi allows you to support a single version of your code, auto-generating the code/routes for older versions. You keep versioning encapsulated in small and independent "version change" modules while your business logic knows nothing about versioning.\n\nIts approach will be useful if you want to:\n\n1. Support many API versions for a long time\n2. Effortlessly backport features and bugfixes to all of your versions\n\nOtherwise, more conventional methods of API versioning may be preferable.\n\n## Tutorial\n\nThis guide provides a step-by-step tutorial for setting up automatic API versioning using Universi library. I will illustrate this with an example of a User API, where we will be implementing changes to a User\'s address.\n\n### A dummy setup\n\nHere is an initial API setup where the User has a single address. We will be implementing two routes - one for creating a user and another for retrieving user details. We\'ll be using "int" for ID for simplicity.\n\nThe first API you come up with usually doesn\'t require more than one address -- why bother?\n\nSo we create our file with schemas:\n\n```python\nfrom pydantic import BaseModel\n\n\nclass UserCreateRequest(BaseModel):\n    address: str\n\nclass UserResource(BaseModel):\n    id: int\n    address: str\n```\n\nAnd we create our file with routes:\n\n```python\nfrom versions.latest.users import UserCreateRequest, UserResource\nfrom universi import VersionedAPIRouter\n\nrouter = VersionedAPIRouter()\n\n@router.post("/users", response_model=UserResource)\nasync def create_user(payload: UserCreateRequest):\n    return {\n        "id": 83,\n        "address": payload.address,\n    }\n\n@router.get("/users/{user_id}", response_model=UserResource)\nasync def get_user(user_id: int):\n    return {\n        "id": user_id,\n        "address": "123 Example St",\n    }\n```\n\n### Turning address into a list\n\nDuring our development, we have realized that the initial API design was wrong and that addresses should have always been a list because the user wants to have multiple addresses to choose from so now we have to change the type of the "address" field to the list of strings.\n\n```python\nfrom pydantic import BaseModel\nfrom universi import Field\n\n\nclass UserCreateRequest(BaseModel):\n    addresses: list[str] = Field(min_items=1)\n\nclass UserResource(BaseModel):\n    id: int\n    addresses: list[str]\n```\n\n```python\n@router.post("/users", response_model=UserResource)\nasync def create_user(payload: UserCreateRequest):\n    return {\n        "id": 83,\n        "addresses": payload.addresses,\n    }\n\n@router.get("/users/{user_id}", response_model=UserResource)\nasync def get_user(user_id: int):\n    return {\n        "id": user_id,\n        "addresses": ["123 Example St", "456 Main St"],\n    }\n\n```\n\nBut every user of ours will now have their API integration broken. To prevent that, we have to introduce API versioning. There aren\'t many methods of doing that. Most of them force you to either duplicate your schemas, your endpoints, or your entire app instance. And it makes sense, really: duplication is the only way to make sure that you will not break old versions with your new versions; the bigger the piece you duplicating -- the safer. Of course, the safest being duplicating the entire app instance and even having a separate database. But that is expensive and makes it either impossible to make breaking changes often or to support many versions. As a result, either you need infinite resources, very long development cycles, or your users will need to often migrate from version to version.\n\nStripe has come up [with a solution](https://stripe.com/blog/api-versioning): let\'s have one latest app version whose responses get migrated to older versions and let\'s describe changes between these versions using migrations. This approach allows them to keep versions for **years** without dropping them. Obviously, each breaking change is still bad and each version still makes our system more complex and expensive, but their approach gives us a chance to minimize that. Additionally, it allows us backport features and bugfixes to older versions. However, you will also be backporting bugs, which is a sad consequence of eliminating duplication.\n\nUniversi is heavily inspired by this approach so let\'s continue our tutorial and now try to combine the two versions we created using versioning.\n\n### Creating the Migration\n\nWe need to create a migration to handle changes between these versions. This migration will convert the list of addresses back to a single address when migrating to the previous version. Yes, migrating **back**: you might be used to database migrations where we write upgrade migration and downgrade migration but here our goal is to have an app of latest version and to describe what older versions looked like in comparison to it. That way the old versions are frozen in migrations and you can **almost** safely forget about them.\n\n```python\nfrom universi import Field\nfrom universi.structure import (\n    schema,\n    VersionChange,\n    convert_response_to_previous_version_for,\n)\n\nclass ChangeAddressToList(VersionChange):\n    description = (\n        "Change user address to a list of strings to "\n        "allow the user to specify multiple addresses"\n    )\n    instructions_to_migrate_to_previous_version = (\n        # You should use schema inheritance if you don\'t want to repeat yourself in such cases\n        schema(UserCreateRequest).field("addresses").didnt_exist,\n        schema(UserCreateRequest).field("address").existed_with(type=str, info=Field()),\n        schema(UserResource).field("addresses").didnt_exist,\n        schema(UserResource).field("address").existed_with(type=str, info=Field()),\n    )\n\n    @convert_response_to_previous_version_for(get_user, create_user)\n    def change_addresses_to_single_item(cls, data: dict[str, Any]) -> None:\n        data["address"] = data.pop("addresses")[0]\n    \n    @schema(UserCreateRequest).had_property("addresses")\n    def addresses_property(parsed_schema):\n        return [parsed_schema.address]\n\n```\n\ns\nSee how we are popping the first address from the list? This is only guaranteed to be possible because we specified earlier that `min_items` for `addresses` must be `1`. If we didn\'t, then the user would be able to create a user in a newer version that would be impossible to represent in the older version. I.e. If anyone tried to get that user from the older version, they would get a `ResponseValidationError` because the user wouldn\'t have data for a mandatory `address` field. You need to always keep in mind tht API versioning is only for versioning your **API**, your interface. Your versions must still be completely compatible in terms of data. If they are not, then you are versioning your data and you should really go with a separate app instance. Otherwise, your users will have a hard time migrating back and forth between API versions and so many unexpected errors.\n\nSee how we added the `addresses` property? This simple instruction will allow us to use `addresses` even from the old schema, which means that our api route will not need to know anything about versioning. The main goal of universi is to shift the logic of versioning away from your business logic and api endpoints which makes your project easier to navigate and which makes deleting versions a breeze.\n\n### Grouping Version Changes\n\nFinally, we group the version changes in the `Versions` class. This represents the different versions of your API and the changes between them. You can add any "version changes" to any version. For simplicity, let\'s use versions 2002 and 2001 which means that we had a single address in API in 2001 and added addresses as a list in 2002\'s version.\n\n```python\nfrom universi.structure import Version, Versions\nfrom datetime import date\n\nversions = Versions(\n    Version(date(2002, 1, 1), ChangeAddressToList),\n    Version(date(2001, 1, 1)),\n)\n```\n\nThat\'s it. You\'re done with describing things. Now you just gotta ask universi to do the rest for you. We\'ll need the VersionedAPIRouter we used previously, our API versions, and the module representing the latest versions of our schemas.\n\n```python\nfrom versions import latest\nfrom universi import regenerate_dir_to_all_versions, api_version_var\n\nregenerate_dir_to_all_versions(latest, versions)\nrouter_versions = router.create_versioned_copies(\n    versions,\n    latest_schemas_module=latest,\n)\napi_version_var.set(date(2002, 1, 1))\nuvicorn.run(router_versions[date(2002, 1, 1)])\n```\n\nUniversi has generated multiple things in this code:\n\n* Three versions of our schemas: one for each API version and one that includes definitions of unions of all versions for each schema which will be useful when you want to type check that you are using requests of different versions correctly. For example, we\'ll have `UserCreateRequestUnion` defined there which is a `TypeAlias` pointing to the union of 2002 version and 2001 version of `UserCreateRequest`.\n* Two versions of our API router: one for each API version\n\nYou can now just pick a router by its version and run it separately or use a parent router/app to specify the logic by which you\'d like to pick a version. I recommend using a header-based router with version dates as headers. And yes, that\'s how Stripe does it.\n\nNote that universi migrates your response data based on the api_version_var context variable so you must set it with each request. `universi.header` has a dependency that does that for you.\n\nObviously, this was just a simple example and universi has a lot more features so if you\'re interested -- take a look at the reference.\n\n### Examples\n\nPlease, see [tutorial examples](https://github.com/Ovsyanka83/universi/tree/main/tests/test_tutorial) for the fully working version of the project above.\n\n## Important warnings\n\n1. The goal of Universi is to **minimize** the impact of versioning on your business logic. It provides all necessary tools to prevent you from **ever** checking for a concrete version in your code. So please, if you are tempted to check something like `api_version_var.get() >= date(2022, 11, 11)` -- please, take another look into [reference](#version-changes-with-side-effects) section. I am confident that you will find a better solution there.\n2. Universi uses its own `universi.Field` function for defining pydantic fields. If you want your pydantic schemas to migrate correctly, then you must use `universi.Field` instead of `pydantic.Field` everywhere because `pydantic.Field` does not preserve the information about which attributes were passed and which were not so code generation is much harder with it.\n3. Universi does not include a header-based router like FastAPI. We hope that soon a framework for header-based routing will surface which will allow universi to be a full versioning solution.\n4. We migrate responses backwards in versions from the latest version using data migration functions and requests forward in versions until the latest version using properties on pydantic models.\n\n## Reference\n\n### Endpoints\n\n#### Defining endpoints that didn\'t exist in new versions\n\nIf you had an endpoint in old version but do not have it in a new one, you must still define it but mark it as deleted.\n\n```python\n@router.only_exists_in_older_versions\n@router.get("/my_old_endpoint")\nasync def my_old_endpoint():\n    ...\n```\n\nand then define it as existing in one of the older versions:\n\n```python\nfrom universi.structure import VersionChange, endpoint\n\nclass MyChange(VersionChange):\n    description = "..."\n    instructions_to_migrate_to_previous_version = (\n        endpoint(my_old_endpoint).existed,\n    )\n\n```\n\n#### Defining endpoints that didn\'t exist in old versions\n\nIf you have an endpoint in your new version that must not exist in older versions, you define it as usual and then mark it as "non-existing" in old versions:\n\n```python\nfrom universi.structure import VersionChange, endpoint\n\nclass MyChange(VersionChange):\n    description = "..."\n    instructions_to_migrate_to_previous_version = (\n        endpoint(my_new_endpoint).didnt_exist,\n    )\n\n```\n\n#### Changing endpoint attributes\n\nIf you want to change any attribute of your endpoint in a new version, you can return the attribute\'s value in all older versions like so:\n\n```python\nfrom universi.structure import VersionChange, endpoint\n\nclass MyChange(VersionChange):\n    description = "..."\n    instructions_to_migrate_to_previous_version = (\n        endpoint(my_endpoint).had(description="My old description"),\n    )\n\n```\n\n### Enums\n\n#### Adding enum members\n\nNote that adding enum members **can** be a breaking change unlike adding optional fields to a schema. For example, if I return a list of entities, each of which has some type, and I add a new type -- then my client\'s code is likely to break.\n\nSo I suggest adding enum members in new versions as well.\n\n```python\nfrom universi.structure import VersionChange, enum\nfrom enum import auto\n\nclass MyChange(VersionChange):\n    description = "..."\n    instructions_to_migrate_to_previous_version = (\n        enum(my_enum).had(foo="baz", bar=auto()),\n    )\n\n```\n\n#### Removing enum members\n\n```python\nfrom universi.structure import VersionChange, enum\n\nclass MyChange(VersionChange):\n    description = "..."\n    instructions_to_migrate_to_previous_version = (\n        enum(my_endpoint).didnt_have("foo", "bar"),\n    )\n\n```\n\n### Schemas\n\n#### Add a field\n\n```python\nfrom universi import Field\nfrom universi.structure import VersionChange, schema\n\nclass MyChange(VersionChange):\n    description = "..."\n    instructions_to_migrate_to_previous_version = (\n        schema(MySchema).field("foo").existed_with(type=list[str], info=Field(description="Foo")),\n    )\n\n```\n\n#### Remove a field\n\n```python\nfrom universi.structure import VersionChange, schema\n\nclass MyChange(VersionChange):\n    description = "..."\n    instructions_to_migrate_to_previous_version = (\n        schema(MySchema).field("foo").didnt_exist,\n    )\n\n```\n\n#### Change a field\n\n```python\nfrom universi.structure import VersionChange, schema\n\nclass MyChange(VersionChange):\n    description = "..."\n    instructions_to_migrate_to_previous_version = (\n        schema(MySchema).field("foo").had(description="Foo"),\n    )\n\n```\n\n#### Add a property\n\n```python\nfrom universi.structure import VersionChange, schema\n\nclass MyChange(VersionChange):\n    description = "..."\n    instructions_to_migrate_to_previous_version = ()\n\n    @schema(MySchema).had_property("foo")\n    def any_name_here(parsed_schema):\n        # Anything can be returned from here\n        return parsed_schema.some_other_field\n\n```\n\n#### Remove a property\n\n```python\nfrom universi.structure import VersionChange, schema\n\nclass MyChange(VersionChange):\n    description = "..."\n    instructions_to_migrate_to_previous_version = (\n        schema(MySchema).property("foo").didnt_exist,\n    )\n\n```\n\n### Unions\n\nAs you probably realize, when you have many versions with different request schemas and your business logic receives one of them -- you\'re in trouble. You could handle them all separately by checking the version of each schema and then using the correct logic for it but universi tries to offer something better.\n\nInstead, we take a union of all of our request schemas and write our business logic as if it receives that union. For example, if version 2000 had field "foo" of type `str` and then version 2001 changed that field to type `int`, then a union of these schemas will have foo as `str | int` so your type checker will protect you against incorrect usage. Same goes for added/deleted fields. Obviously, manually importing all your schemas and then taking a union of them is tough, especially if you have many versions, which is why Universi not only generates a directory for each of your versions, but it also generates a "unions" directory that contains unions of all your schemas and enums.\n\nFor example, if we had a schema named `MySchema` and two versions of it: 2000 and 2001, then the union definition will look like the following:\n\n```python\nimport src.versions.v2000_01_01.my_schema_module\nimport src.versions.v2001_01_01.my_schema_module\nimport src.versions.latest.my_schema_module\n\nMySchemaUnion = (\n    versions.v2000_01_01.my_schema_module.MySchema |\n    versions.v2001_01_01.my_schema_module.MySchema |\n    versions.latest.my_schema_module.MySchema\n)\n```\n\nand you would be able to use it like so:\n\n```python\nfrom src.versions.unions.my_schema_module import MySchemaUnion\n\nasync def the_entrypoint_of_my_business_logic(request_payload: MySchemaUnion):\n    ...\n\n```\n\nNote that this feature only affects type checking and does not affect your functionality.\n\n### Data conversion\n\nAs described in the tutorial, universi can convert your response data into older versions. It does so by running your "migration" functions whenever it encounters a version change:\n\n```python\nfrom universi.structure import VersionChange, convert_response_to_previous_version_for\nfrom typing import Any\n\nclass ChangeAddressToList(VersionChange):\n    description = "..."\n\n    @convert_response_to_previous_version_for(my_endpoint, my_other_endpoint)\n    def change_addresses_to_single_item(cls, data: dict[str, Any]) -> None:\n        data["address"] = data.pop("addresses")[0]\n\n```\n\nIt is done by applying `universi.Versions.versioned(...)` decorator to each endpoint which automatically detects the API version by getting it from the [contextvar](#api-version-header-and-context-variables) and applying all version changes until the selected version in reverse. Note that if the version is not set, then no changes will be applied.\n\nIf you want to convert a specific response to a specific version, you can use `universi.Versions.data_to_version(...)`.\n\n### Version changes with side effects\n\nSometimes you will use API versioning to handle a breaking change in your **business logic**, not in the schemas themselves. In such cases, it is tempting to add a version check and just follow the new business logic such as:\n\n```python\nif api_version_var.get() >= date(2022, 11, 11):\n    # do new logic here\n```\n\nIn universi, this approach is highly discouraged. It is recommended that you avoid side effects like this at any cost because each one makes your core logic harder to understand. But if you cannot, then I urge you to at least abstract away versions and versioning from your business logic which will make your code much easier to read.\n\nTo simplify this, universi has a special `VersionChangeWithSideEffects` class. It makes finding dangerous versions that have side effects much easier and provides a nice abstraction for checking whether we are on a version where these side effects have been applied.\n\nAs an example, let\'s use the tutorial section\'s case with the user and their address. Let\'s say that we use an external service to check whether user\'s address is listed in it and return 400 response if it is not. Let\'s also say that we only added this check in the newest version.\n\n```python\nfrom universi.structure import VersionChangeWithSideEffects\n\nclass UserAddressIsCheckedInExternalService(VersionChangeWithSideEffects):\n    description = (\n        "User\'s address is now checked for existense in an external service. "\n        "If it doesn\'t exist there, a 400 code is returned."\n    )\n\n```\n\nThen we will have the following check in our business logic:\n\n```python\nfrom src.versions import versions, UserAddressIsCheckedInExternalService\n\n\nasync def create_user(payload):\n    if UserAddressIsCheckedInExternalService.is_active(versions):\n        check_user_address_exists_in_an_external_service(payload.address)\n    ...\n```\n\nSo this change can be contained in any version -- your business logic doesn\'t know which version it has and shouldn\'t.\n\n### API Version header and context variables\n\nUniversi automatically converts your data to a correct version and has "version checks" when dealing with side effects as described in [the section above](#version-changes-with-side-effects). It can only do so using a special [context variable](https://docs.python.org/3/library/contextvars.html) that stores the current API version.\n\nUniversi has such default variable defined as `universi.api_version_var`. You can also use `universi.get_universi_dependency` to get a `fastapi.Depends` that automatically sets this contextvar based on a header name that you pick.\n\nYou can also set the variable yourself or even pass a different compatible contextvar to your `universi.Versions` constructor.\n',
+    'long_description': '# universi\n\nModern [Stripe-like](https://stripe.com/blog/api-versioning) API versioning in FastAPI\n\n---\n\n<p align="center">\n<a href="https://github.com/ovsyanka83/universi/actions?query=workflow%3ATests+event%3Apush+branch%3Amain" target="_blank">\n    <img src="https://github.com/Ovsyanka83/universi/actions/workflows/test.yaml/badge.svg?branch=main&event=push" alt="Test">\n</a>\n<a href="https://codecov.io/gh/ovsyanka83/universi" target="_blank">\n    <img src="https://img.shields.io/codecov/c/github/ovsyanka83/universi?color=%2334D058" alt="Coverage">\n</a>\n<a href="https://pypi.org/project/universi/" target="_blank">\n    <img alt="PyPI" src="https://img.shields.io/pypi/v/universi?color=%2334D058&label=pypi%20package" alt="Package version">\n</a>\n<a href="https://pypi.org/project/universi/" target="_blank">\n    <img src="https://img.shields.io/pypi/pyversions/universi?color=%2334D058" alt="Supported Python versions">\n</a>\n</p>\n\n## Installation\n\n```bash\npip install universi\n```\n\n<!---\n# TODO: Note that we don\'t handle "from .schemas import Schema as OtherSchema" case\n# TODO: Need to validate that the user doesn\'t use versioned schemas instead of the latest ones\n-->\n\n## Who is this for?\n\nUniversi allows you to support a single version of your code, auto-generating the code/routes for older versions. You keep versioning encapsulated in small and independent "version change" modules while your business logic knows nothing about versioning.\n\nIts approach will be useful if you want to:\n\n1. Support many API versions for a long time\n2. Effortlessly backport features and bugfixes to all of your versions\n\nOtherwise, more conventional methods of API versioning may be preferable.\n\n## Tutorial\n\nThis guide provides a step-by-step tutorial for setting up automatic API versioning using Universi library. I will illustrate this with an example of a User API, where we will be implementing changes to a User\'s address.\n\n### A dummy setup\n\nHere is an initial API setup where the User has a single address. We will be implementing two routes - one for creating a user and another for retrieving user details. We\'ll be using "int" for ID for simplicity.\n\nThe first API you come up with usually doesn\'t require more than one address -- why bother?\n\nSo we create our file with schemas:\n\n```python\nfrom pydantic import BaseModel\n\n\nclass UserCreateRequest(BaseModel):\n    address: str\n\nclass UserResource(BaseModel):\n    id: int\n    address: str\n```\n\nAnd we create our file with routes:\n\n```python\nfrom versions.latest.users import UserCreateRequest, UserResource\nfrom universi import VersionedAPIRouter\n\nrouter = VersionedAPIRouter()\n\n@router.post("/users", response_model=UserResource)\nasync def create_user(payload: UserCreateRequest):\n    return {\n        "id": 83,\n        "address": payload.address,\n    }\n\n@router.get("/users/{user_id}", response_model=UserResource)\nasync def get_user(user_id: int):\n    return {\n        "id": user_id,\n        "address": "123 Example St",\n    }\n```\n\n### Turning address into a list\n\nDuring our development, we have realized that the initial API design was wrong and that addresses should have always been a list because the user wants to have multiple addresses to choose from so now we have to change the type of the "address" field to the list of strings.\n\n```python\nfrom pydantic import BaseModel\nfrom universi import Field\n\n\nclass UserCreateRequest(BaseModel):\n    addresses: list[str] = Field(min_items=1)\n\nclass UserResource(BaseModel):\n    id: int\n    addresses: list[str]\n```\n\n```python\n@router.post("/users", response_model=UserResource)\nasync def create_user(payload: UserCreateRequest):\n    return {\n        "id": 83,\n        "addresses": payload.addresses,\n    }\n\n@router.get("/users/{user_id}", response_model=UserResource)\nasync def get_user(user_id: int):\n    return {\n        "id": user_id,\n        "addresses": ["123 Example St", "456 Main St"],\n    }\n\n```\n\nBut every user of ours will now have their API integration broken. To prevent that, we have to introduce API versioning. There aren\'t many methods of doing that. Most of them force you to either duplicate your schemas, your endpoints, or your entire app instance. And it makes sense, really: duplication is the only way to make sure that you will not break old versions with your new versions; the bigger the piece you duplicating -- the safer. Of course, the safest being duplicating the entire app instance and even having a separate database. But that is expensive and makes it either impossible to make breaking changes often or to support many versions. As a result, either you need infinite resources, very long development cycles, or your users will need to often migrate from version to version.\n\nStripe has come up [with a solution](https://stripe.com/blog/api-versioning): let\'s have one latest app version whose responses get migrated to older versions and let\'s describe changes between these versions using migrations. This approach allows them to keep versions for **years** without dropping them. Obviously, each breaking change is still bad and each version still makes our system more complex and expensive, but their approach gives us a chance to minimize that. Additionally, it allows us backport features and bugfixes to older versions. However, you will also be backporting bugs, which is a sad consequence of eliminating duplication.\n\nUniversi is heavily inspired by this approach so let\'s continue our tutorial and now try to combine the two versions we created using versioning.\n\n### Creating the Migration\n\nWe need to create a migration to handle changes between these versions. This migration will convert the list of addresses back to a single address when migrating to the previous version. Yes, migrating **back**: you might be used to database migrations where we write upgrade migration and downgrade migration but here our goal is to have an app of latest version and to describe what older versions looked like in comparison to it. That way the old versions are frozen in migrations and you can **almost** safely forget about them.\n\n```python\nfrom universi import Field\nfrom universi.structure import (\n    schema,\n    VersionChange,\n    convert_response_to_previous_version_for,\n)\n\nclass ChangeAddressToList(VersionChange):\n    description = (\n        "Change user address to a list of strings to "\n        "allow the user to specify multiple addresses"\n    )\n    instructions_to_migrate_to_previous_version = (\n        # You should use schema inheritance if you don\'t want to repeat yourself in such cases\n        schema(UserCreateRequest).field("addresses").didnt_exist,\n        schema(UserCreateRequest).field("address").existed_with(type=str, info=Field()),\n        schema(UserResource).field("addresses").didnt_exist,\n        schema(UserResource).field("address").existed_with(type=str, info=Field()),\n    )\n\n    @convert_response_to_previous_version_for(get_user, create_user)\n    def change_addresses_to_single_item(cls, data: dict[str, Any]) -> None:\n        data["address"] = data.pop("addresses")[0]\n    \n    @schema(UserCreateRequest).had_property("addresses")\n    def addresses_property(parsed_schema):\n        return [parsed_schema.address]\n\n```\n\ns\nSee how we are popping the first address from the list? This is only guaranteed to be possible because we specified earlier that `min_items` for `addresses` must be `1`. If we didn\'t, then the user would be able to create a user in a newer version that would be impossible to represent in the older version. I.e. If anyone tried to get that user from the older version, they would get a `ResponseValidationError` because the user wouldn\'t have data for a mandatory `address` field. You need to always keep in mind tht API versioning is only for versioning your **API**, your interface. Your versions must still be completely compatible in terms of data. If they are not, then you are versioning your data and you should really go with a separate app instance. Otherwise, your users will have a hard time migrating back and forth between API versions and so many unexpected errors.\n\nSee how we added the `addresses` property? This simple instruction will allow us to use `addresses` even from the old schema, which means that our api route will not need to know anything about versioning. The main goal of universi is to shift the logic of versioning away from your business logic and api endpoints which makes your project easier to navigate and which makes deleting versions a breeze.\n\n### Grouping Version Changes\n\nFinally, we group the version changes in the `VersionBundle` class. This represents the different versions of your API and the changes between them. You can add any "version changes" to any version. For simplicity, let\'s use versions 2002 and 2001 which means that we had a single address in API in 2001 and added addresses as a list in 2002\'s version.\n\n```python\nfrom universi.structure import Version, VersionBundle\nfrom datetime import date\n\nversions = VersionBundle(\n    Version(date(2002, 1, 1), ChangeAddressToList),\n    Version(date(2001, 1, 1)),\n)\n```\n\nThat\'s it. You\'re done with describing things. Now you just gotta ask universi to do the rest for you. We\'ll need the VersionedAPIRouter we used previously, our API versions, and the module representing the latest versions of our schemas.\n\n```python\nfrom versions import latest\nfrom universi import regenerate_dir_to_all_versions, api_version_var\n\nregenerate_dir_to_all_versions(latest, versions)\nrouter_versions = router.create_versioned_copies(\n    versions,\n    latest_schemas_module=latest,\n)\napi_version_var.set(date(2002, 1, 1))\nuvicorn.run(router_versions[date(2002, 1, 1)])\n```\n\nUniversi has generated multiple things in this code:\n\n* Three versions of our schemas: one for each API version and one that includes definitions of unions of all versions for each schema which will be useful when you want to type check that you are using requests of different versions correctly. For example, we\'ll have `UserCreateRequestUnion` defined there which is a `TypeAlias` pointing to the union of 2002 version and 2001 version of `UserCreateRequest`.\n* Two versions of our API router: one for each API version\n\nYou can now just pick a router by its version and run it separately or use a parent router/app to specify the logic by which you\'d like to pick a version. I recommend using a header-based router with version dates as headers. And yes, that\'s how Stripe does it.\n\nNote that universi migrates your response data based on the api_version_var context variable so you must set it with each request. `universi.header` has a dependency that does that for you.\n\nObviously, this was just a simple example and universi has a lot more features so if you\'re interested -- take a look at the reference.\n\n### Examples\n\nPlease, see [tutorial examples](https://github.com/Ovsyanka83/universi/tree/main/tests/test_tutorial) for the fully working version of the project above.\n\n## Important warnings\n\n1. The goal of Universi is to **minimize** the impact of versioning on your business logic. It provides all necessary tools to prevent you from **ever** checking for a concrete version in your code. So please, if you are tempted to check something like `api_version_var.get() >= date(2022, 11, 11)` -- please, take another look into [reference](#version-changes-with-side-effects) section. I am confident that you will find a better solution there.\n2. Universi uses its own `universi.Field` function for defining pydantic fields. If you want your pydantic schemas to migrate correctly, then you must use `universi.Field` instead of `pydantic.Field` everywhere because `pydantic.Field` does not preserve the information about which attributes were passed and which were not so code generation is much harder with it.\n3. Universi does not include a header-based router like FastAPI. We hope that soon a framework for header-based routing will surface which will allow universi to be a full versioning solution.\n4. We migrate responses backwards in versions from the latest version using data migration functions and requests forward in versions until the latest version using properties on pydantic models.\n\n## Reference\n\n### Endpoints\n\n#### Defining endpoints that didn\'t exist in new versions\n\nIf you had an endpoint in old version but do not have it in a new one, you must still define it but mark it as deleted.\n\n```python\n@router.only_exists_in_older_versions\n@router.get("/my_old_endpoint")\nasync def my_old_endpoint():\n    ...\n```\n\nand then define it as existing in one of the older versions:\n\n```python\nfrom universi.structure import VersionChange, endpoint\n\nclass MyChange(VersionChange):\n    description = "..."\n    instructions_to_migrate_to_previous_version = (\n        endpoint(my_old_endpoint).existed,\n    )\n\n```\n\n#### Defining endpoints that didn\'t exist in old versions\n\nIf you have an endpoint in your new version that must not exist in older versions, you define it as usual and then mark it as "non-existing" in old versions:\n\n```python\nfrom universi.structure import VersionChange, endpoint\n\nclass MyChange(VersionChange):\n    description = "..."\n    instructions_to_migrate_to_previous_version = (\n        endpoint(my_new_endpoint).didnt_exist,\n    )\n\n```\n\n#### Changing endpoint attributes\n\nIf you want to change any attribute of your endpoint in a new version, you can return the attribute\'s value in all older versions like so:\n\n```python\nfrom universi.structure import VersionChange, endpoint\n\nclass MyChange(VersionChange):\n    description = "..."\n    instructions_to_migrate_to_previous_version = (\n        endpoint(my_endpoint).had(description="My old description"),\n    )\n\n```\n\n### Enums\n\n#### Adding enum members\n\nNote that adding enum members **can** be a breaking change unlike adding optional fields to a schema. For example, if I return a list of entities, each of which has some type, and I add a new type -- then my client\'s code is likely to break.\n\nSo I suggest adding enum members in new versions as well.\n\n```python\nfrom universi.structure import VersionChange, enum\nfrom enum import auto\n\nclass MyChange(VersionChange):\n    description = "..."\n    instructions_to_migrate_to_previous_version = (\n        enum(my_enum).had(foo="baz", bar=auto()),\n    )\n\n```\n\n#### Removing enum members\n\n```python\nfrom universi.structure import VersionChange, enum\n\nclass MyChange(VersionChange):\n    description = "..."\n    instructions_to_migrate_to_previous_version = (\n        enum(my_endpoint).didnt_have("foo", "bar"),\n    )\n\n```\n\n### Schemas\n\n#### Add a field\n\n```python\nfrom universi import Field\nfrom universi.structure import VersionChange, schema\n\nclass MyChange(VersionChange):\n    description = "..."\n    instructions_to_migrate_to_previous_version = (\n        schema(MySchema).field("foo").existed_with(type=list[str], info=Field(description="Foo")),\n    )\n\n```\n\n#### Remove a field\n\n```python\nfrom universi.structure import VersionChange, schema\n\nclass MyChange(VersionChange):\n    description = "..."\n    instructions_to_migrate_to_previous_version = (\n        schema(MySchema).field("foo").didnt_exist,\n    )\n\n```\n\n#### Change a field\n\n```python\nfrom universi.structure import VersionChange, schema\n\nclass MyChange(VersionChange):\n    description = "..."\n    instructions_to_migrate_to_previous_version = (\n        schema(MySchema).field("foo").had(description="Foo"),\n    )\n\n```\n\n#### Add a property\n\n```python\nfrom universi.structure import VersionChange, schema\n\nclass MyChange(VersionChange):\n    description = "..."\n    instructions_to_migrate_to_previous_version = ()\n\n    @schema(MySchema).had_property("foo")\n    def any_name_here(parsed_schema):\n        # Anything can be returned from here\n        return parsed_schema.some_other_field\n\n```\n\n#### Remove a property\n\n```python\nfrom universi.structure import VersionChange, schema\n\nclass MyChange(VersionChange):\n    description = "..."\n    instructions_to_migrate_to_previous_version = (\n        schema(MySchema).property("foo").didnt_exist,\n    )\n\n```\n\n### Unions\n\nAs you probably realize, when you have many versions with different request schemas and your business logic receives one of them -- you\'re in trouble. You could handle them all separately by checking the version of each schema and then using the correct logic for it but universi tries to offer something better.\n\nInstead, we take a union of all of our request schemas and write our business logic as if it receives that union. For example, if version 2000 had field "foo" of type `str` and then version 2001 changed that field to type `int`, then a union of these schemas will have foo as `str | int` so your type checker will protect you against incorrect usage. Same goes for added/deleted fields. Obviously, manually importing all your schemas and then taking a union of them is tough, especially if you have many versions, which is why Universi not only generates a directory for each of your versions, but it also generates a "unions" directory that contains unions of all your schemas and enums.\n\nFor example, if we had a schema named `MySchema` and two versions of it: 2000 and 2001, then the union definition will look like the following:\n\n```python\nimport src.versions.v2000_01_01.my_schema_module\nimport src.versions.v2001_01_01.my_schema_module\nimport src.versions.latest.my_schema_module\n\nMySchemaUnion = (\n    versions.v2000_01_01.my_schema_module.MySchema |\n    versions.v2001_01_01.my_schema_module.MySchema |\n    versions.latest.my_schema_module.MySchema\n)\n```\n\nand you would be able to use it like so:\n\n```python\nfrom src.versions.unions.my_schema_module import MySchemaUnion\n\nasync def the_entrypoint_of_my_business_logic(request_payload: MySchemaUnion):\n    ...\n\n```\n\nNote that this feature only affects type checking and does not affect your functionality.\n\n### Data conversion\n\nAs described in the tutorial, universi can convert your response data into older versions. It does so by running your "migration" functions whenever it encounters a version change:\n\n```python\nfrom universi.structure import VersionChange, convert_response_to_previous_version_for\nfrom typing import Any\n\nclass ChangeAddressToList(VersionChange):\n    description = "..."\n\n    @convert_response_to_previous_version_for(my_endpoint, my_other_endpoint)\n    def change_addresses_to_single_item(cls, data: dict[str, Any]) -> None:\n        data["address"] = data.pop("addresses")[0]\n\n```\n\nIt is done by applying `universi.VersionBundle.versioned(...)` decorator to each endpoint which automatically detects the API version by getting it from the [contextvar](#api-version-header-and-context-variables) and applying all version changes until the selected version in reverse. Note that if the version is not set, then no changes will be applied.\n\nIf you want to convert a specific response to a specific version, you can use `universi.VersionBundle.data_to_version(...)`.\n\n### Version changes with side effects\n\nSometimes you will use API versioning to handle a breaking change in your **business logic**, not in the schemas themselves. In such cases, it is tempting to add a version check and just follow the new business logic such as:\n\n```python\nif api_version_var.get() >= date(2022, 11, 11):\n    # do new logic here\n```\n\nIn universi, this approach is highly discouraged. It is recommended that you avoid side effects like this at any cost because each one makes your core logic harder to understand. But if you cannot, then I urge you to at least abstract away versions and versioning from your business logic which will make your code much easier to read.\n\nTo simplify this, universi has a special `VersionChangeWithSideEffects` class. It makes finding dangerous versions that have side effects much easier and provides a nice abstraction for checking whether we are on a version where these side effects have been applied.\n\nAs an example, let\'s use the tutorial section\'s case with the user and their address. Let\'s say that we use an external service to check whether user\'s address is listed in it and return 400 response if it is not. Let\'s also say that we only added this check in the newest version.\n\n```python\nfrom universi.structure import VersionChangeWithSideEffects\n\nclass UserAddressIsCheckedInExternalService(VersionChangeWithSideEffects):\n    description = (\n        "User\'s address is now checked for existense in an external service. "\n        "If it doesn\'t exist there, a 400 code is returned."\n    )\n\n```\n\nThen we will have the following check in our business logic:\n\n```python\nfrom src.versions import versions, UserAddressIsCheckedInExternalService\n\n\nasync def create_user(payload):\n    if UserAddressIsCheckedInExternalService.is_active:\n        check_user_address_exists_in_an_external_service(payload.address)\n    ...\n```\n\nSo this change can be contained in any version -- your business logic doesn\'t know which version it has and shouldn\'t.\n\n### API Version header and context variables\n\nUniversi automatically converts your data to a correct version and has "version checks" when dealing with side effects as described in [the section above](#version-changes-with-side-effects). It can only do so using a special [context variable](https://docs.python.org/3/library/contextvars.html) that stores the current API version.\n\nUniversi has such default variable defined as `universi.api_version_var`. You can also use `universi.get_universi_dependency` to get a `fastapi.Depends` that automatically sets this contextvar based on a header name that you pick.\n\nYou can also set the variable yourself or even pass a different compatible contextvar to your `universi.VersionBundle` constructor.\n',
     'author': 'Stanislav Zmiev',
     'author_email': 'szmiev2000@gmail.com',
     'maintainer': 'None',
     'maintainer_email': 'None',
     'url': 'https://github.com/ovsyanka83/universi',
     'packages': packages,
     'package_data': package_data,
```

#### html2text {}

```diff
@@ -1,13 +1,13 @@
 # -*- coding: utf-8 -*- from setuptools import setup packages = \ ['universi',
 'universi.structure'] package_data = \ {'': ['*']} install_requires = \
 ['fastapi>=0.96.1', 'typing-extensions'] setup_kwargs = { 'name': 'universi',
-'version': '0.9.0', 'description': '', 'long_description': '#
+'version': '1.0.0', 'description': '', 'long_description': '#
 universi\n\nModern [Stripe-like](https://stripe.com/blog/api-versioning) API
-versioning for FastAPI\n\n---\n\n
+versioning in FastAPI\n\n---\n\n
 \n\n_[Test]\n\n\n_[Coverage]\n\n\n_[PyPI]\n\n\n_[Supported_Python_versions]\n\n
 \n\n## Installation\n\n```bash\npip install universi\n```\n\n\n\n## Who is this
 for?\n\nUniversi allows you to support a single version of your code, auto-
 generating the code/routes for older versions. You keep versioning encapsulated
 in small and independent "version change" modules while your business logic
 knows nothing about versioning.\n\nIts approach will be useful if you want to:
 \n\n1. Support many API versions for a long time\n2. Effortlessly backport
@@ -100,21 +100,21 @@
 will have a hard time migrating back and forth between API versions and so many
 unexpected errors.\n\nSee how we added the `addresses` property? This simple
 instruction will allow us to use `addresses` even from the old schema, which
 means that our api route will not need to know anything about versioning. The
 main goal of universi is to shift the logic of versioning away from your
 business logic and api endpoints which makes your project easier to navigate
 and which makes deleting versions a breeze.\n\n### Grouping Version
-Changes\n\nFinally, we group the version changes in the `Versions` class. This
-represents the different versions of your API and the changes between them. You
-can add any "version changes" to any version. For simplicity, let\'s use
-versions 2002 and 2001 which means that we had a single address in API in 2001
-and added addresses as a list in 2002\'s version.\n\n```python\nfrom
-universi.structure import Version, Versions\nfrom datetime import
-date\n\nversions = Versions(\n Version(date(2002, 1, 1),
+Changes\n\nFinally, we group the version changes in the `VersionBundle` class.
+This represents the different versions of your API and the changes between
+them. You can add any "version changes" to any version. For simplicity, let\'s
+use versions 2002 and 2001 which means that we had a single address in API in
+2001 and added addresses as a list in 2002\'s version.\n\n```python\nfrom
+universi.structure import Version, VersionBundle\nfrom datetime import
+date\n\nversions = VersionBundle(\n Version(date(2002, 1, 1),
 ChangeAddressToList),\n Version(date(2001, 1, 1)),\n)\n```\n\nThat\'s it.
 You\'re done with describing things. Now you just gotta ask universi to do the
 rest for you. We\'ll need the VersionedAPIRouter we used previously, our API
 versions, and the module representing the latest versions of our
 schemas.\n\n```python\nfrom versions import latest\nfrom universi import
 regenerate_dir_to_all_versions,
 api_version_var\n\nregenerate_dir_to_all_versions(latest,
@@ -239,54 +239,56 @@
 versions. It does so by running your "migration" functions whenever it
 encounters a version change:\n\n```python\nfrom universi.structure import
 VersionChange, convert_response_to_previous_version_for\nfrom typing import
 Any\n\nclass ChangeAddressToList(VersionChange):\n description = "..."\n\n
 @convert_response_to_previous_version_for(my_endpoint, my_other_endpoint)\n def
 change_addresses_to_single_item(cls, data: dict[str, Any]) -> None:\n data
 ["address"] = data.pop("addresses")[0]\n\n```\n\nIt is done by applying
-`universi.Versions.versioned(...)` decorator to each endpoint which
+`universi.VersionBundle.versioned(...)` decorator to each endpoint which
 automatically detects the API version by getting it from the [contextvar](#api-
 version-header-and-context-variables) and applying all version changes until
 the selected version in reverse. Note that if the version is not set, then no
 changes will be applied.\n\nIf you want to convert a specific response to a
-specific version, you can use `universi.Versions.data_to_version(...)`.\n\n###
-Version changes with side effects\n\nSometimes you will use API versioning to
-handle a breaking change in your **business logic**, not in the schemas
-themselves. In such cases, it is tempting to add a version check and just
-follow the new business logic such as:\n\n```python\nif api_version_var.get()
->= date(2022, 11, 11):\n # do new logic here\n```\n\nIn universi, this approach
-is highly discouraged. It is recommended that you avoid side effects like this
-at any cost because each one makes your core logic harder to understand. But if
-you cannot, then I urge you to at least abstract away versions and versioning
-from your business logic which will make your code much easier to read.\n\nTo
-simplify this, universi has a special `VersionChangeWithSideEffects` class. It
-makes finding dangerous versions that have side effects much easier and
-provides a nice abstraction for checking whether we are on a version where
-these side effects have been applied.\n\nAs an example, let\'s use the tutorial
-section\'s case with the user and their address. Let\'s say that we use an
-external service to check whether user\'s address is listed in it and return
-400 response if it is not. Let\'s also say that we only added this check in the
-newest version.\n\n```python\nfrom universi.structure import
-VersionChangeWithSideEffects\n\nclass UserAddressIsCheckedInExternalService
-(VersionChangeWithSideEffects):\n description = (\n "User\'s address is now
-checked for existense in an external service. "\n "If it doesn\'t exist there,
-a 400 code is returned."\n )\n\n```\n\nThen we will have the following check in
-our business logic:\n\n```python\nfrom src.versions import versions,
+specific version, you can use `universi.VersionBundle.data_to_version
+(...)`.\n\n### Version changes with side effects\n\nSometimes you will use API
+versioning to handle a breaking change in your **business logic**, not in the
+schemas themselves. In such cases, it is tempting to add a version check and
+just follow the new business logic such as:\n\n```python\nif
+api_version_var.get() >= date(2022, 11, 11):\n # do new logic here\n```\n\nIn
+universi, this approach is highly discouraged. It is recommended that you avoid
+side effects like this at any cost because each one makes your core logic
+harder to understand. But if you cannot, then I urge you to at least abstract
+away versions and versioning from your business logic which will make your code
+much easier to read.\n\nTo simplify this, universi has a special
+`VersionChangeWithSideEffects` class. It makes finding dangerous versions that
+have side effects much easier and provides a nice abstraction for checking
+whether we are on a version where these side effects have been applied.\n\nAs
+an example, let\'s use the tutorial section\'s case with the user and their
+address. Let\'s say that we use an external service to check whether user\'s
+address is listed in it and return 400 response if it is not. Let\'s also say
+that we only added this check in the newest version.\n\n```python\nfrom
+universi.structure import VersionChangeWithSideEffects\n\nclass
+UserAddressIsCheckedInExternalService(VersionChangeWithSideEffects):\n
+description = (\n "User\'s address is now checked for existense in an external
+service. "\n "If it doesn\'t exist there, a 400 code is returned."\n
+)\n\n```\n\nThen we will have the following check in our business logic:
+\n\n```python\nfrom src.versions import versions,
 UserAddressIsCheckedInExternalService\n\n\nasync def create_user(payload):\n if
-UserAddressIsCheckedInExternalService.is_active(versions):\n
+UserAddressIsCheckedInExternalService.is_active:\n
 check_user_address_exists_in_an_external_service(payload.address)\n
 ...\n```\n\nSo this change can be contained in any version -- your business
 logic doesn\'t know which version it has and shouldn\'t.\n\n### API Version
 header and context variables\n\nUniversi automatically converts your data to a
 correct version and has "version checks" when dealing with side effects as
 described in [the section above](#version-changes-with-side-effects). It can
 only do so using a special [context variable](https://docs.python.org/3/
 library/contextvars.html) that stores the current API version.\n\nUniversi has
 such default variable defined as `universi.api_version_var`. You can also use
 `universi.get_universi_dependency` to get a `fastapi.Depends` that
 automatically sets this contextvar based on a header name that you pick.\n\nYou
 can also set the variable yourself or even pass a different compatible
-contextvar to your `universi.Versions` constructor.\n', 'author': 'Stanislav
-Zmiev', 'author_email': 'szmiev2000@gmail.com', 'maintainer': 'None',
-'maintainer_email': 'None', 'url': 'https://github.com/ovsyanka83/universi',
-'packages': packages, 'package_data': package_data, 'install_requires':
-install_requires, 'python_requires': '>=3.10,<4.0', } setup(**setup_kwargs)
+contextvar to your `universi.VersionBundle` constructor.\n', 'author':
+'Stanislav Zmiev', 'author_email': 'szmiev2000@gmail.com', 'maintainer':
+'None', 'maintainer_email': 'None', 'url': 'https://github.com/ovsyanka83/
+universi', 'packages': packages, 'package_data': package_data,
+'install_requires': install_requires, 'python_requires': '>=3.10,<4.0', } setup
+(**setup_kwargs)
```

### Comparing `universi-0.9.0/PKG-INFO` & `universi-1.0.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: universi
-Version: 0.9.0
+Version: 1.0.0
 Summary: 
 Home-page: https://github.com/ovsyanka83/universi
 License: MIT
 Author: Stanislav Zmiev
 Author-email: szmiev2000@gmail.com
 Requires-Python: >=3.10,<4.0
 Classifier: License :: OSI Approved :: MIT License
@@ -14,15 +14,15 @@
 Requires-Dist: fastapi (>=0.96.1)
 Requires-Dist: typing-extensions
 Project-URL: Repository, https://github.com/ovsyanka83/universi
 Description-Content-Type: text/markdown
 
 # universi
 
-Modern [Stripe-like](https://stripe.com/blog/api-versioning) API versioning for FastAPI
+Modern [Stripe-like](https://stripe.com/blog/api-versioning) API versioning in FastAPI
 
 ---
 
 <p align="center">
 <a href="https://github.com/ovsyanka83/universi/actions?query=workflow%3ATests+event%3Apush+branch%3Amain" target="_blank">
     <img src="https://github.com/Ovsyanka83/universi/actions/workflows/test.yaml/badge.svg?branch=main&event=push" alt="Test">
 </a>
@@ -184,21 +184,21 @@
 s
 See how we are popping the first address from the list? This is only guaranteed to be possible because we specified earlier that `min_items` for `addresses` must be `1`. If we didn't, then the user would be able to create a user in a newer version that would be impossible to represent in the older version. I.e. If anyone tried to get that user from the older version, they would get a `ResponseValidationError` because the user wouldn't have data for a mandatory `address` field. You need to always keep in mind tht API versioning is only for versioning your **API**, your interface. Your versions must still be completely compatible in terms of data. If they are not, then you are versioning your data and you should really go with a separate app instance. Otherwise, your users will have a hard time migrating back and forth between API versions and so many unexpected errors.
 
 See how we added the `addresses` property? This simple instruction will allow us to use `addresses` even from the old schema, which means that our api route will not need to know anything about versioning. The main goal of universi is to shift the logic of versioning away from your business logic and api endpoints which makes your project easier to navigate and which makes deleting versions a breeze.
 
 ### Grouping Version Changes
 
-Finally, we group the version changes in the `Versions` class. This represents the different versions of your API and the changes between them. You can add any "version changes" to any version. For simplicity, let's use versions 2002 and 2001 which means that we had a single address in API in 2001 and added addresses as a list in 2002's version.
+Finally, we group the version changes in the `VersionBundle` class. This represents the different versions of your API and the changes between them. You can add any "version changes" to any version. For simplicity, let's use versions 2002 and 2001 which means that we had a single address in API in 2001 and added addresses as a list in 2002's version.
 
 ```python
-from universi.structure import Version, Versions
+from universi.structure import Version, VersionBundle
 from datetime import date
 
-versions = Versions(
+versions = VersionBundle(
     Version(date(2002, 1, 1), ChangeAddressToList),
     Version(date(2001, 1, 1)),
 )
 ```
 
 That's it. You're done with describing things. Now you just gotta ask universi to do the rest for you. We'll need the VersionedAPIRouter we used previously, our API versions, and the module representing the latest versions of our schemas.
 
@@ -444,17 +444,17 @@
 
     @convert_response_to_previous_version_for(my_endpoint, my_other_endpoint)
     def change_addresses_to_single_item(cls, data: dict[str, Any]) -> None:
         data["address"] = data.pop("addresses")[0]
 
 ```
 
-It is done by applying `universi.Versions.versioned(...)` decorator to each endpoint which automatically detects the API version by getting it from the [contextvar](#api-version-header-and-context-variables) and applying all version changes until the selected version in reverse. Note that if the version is not set, then no changes will be applied.
+It is done by applying `universi.VersionBundle.versioned(...)` decorator to each endpoint which automatically detects the API version by getting it from the [contextvar](#api-version-header-and-context-variables) and applying all version changes until the selected version in reverse. Note that if the version is not set, then no changes will be applied.
 
-If you want to convert a specific response to a specific version, you can use `universi.Versions.data_to_version(...)`.
+If you want to convert a specific response to a specific version, you can use `universi.VersionBundle.data_to_version(...)`.
 
 ### Version changes with side effects
 
 Sometimes you will use API versioning to handle a breaking change in your **business logic**, not in the schemas themselves. In such cases, it is tempting to add a version check and just follow the new business logic such as:
 
 ```python
 if api_version_var.get() >= date(2022, 11, 11):
@@ -481,22 +481,22 @@
 Then we will have the following check in our business logic:
 
 ```python
 from src.versions import versions, UserAddressIsCheckedInExternalService
 
 
 async def create_user(payload):
-    if UserAddressIsCheckedInExternalService.is_active(versions):
+    if UserAddressIsCheckedInExternalService.is_active:
         check_user_address_exists_in_an_external_service(payload.address)
     ...
 ```
 
 So this change can be contained in any version -- your business logic doesn't know which version it has and shouldn't.
 
 ### API Version header and context variables
 
 Universi automatically converts your data to a correct version and has "version checks" when dealing with side effects as described in [the section above](#version-changes-with-side-effects). It can only do so using a special [context variable](https://docs.python.org/3/library/contextvars.html) that stores the current API version.
 
 Universi has such default variable defined as `universi.api_version_var`. You can also use `universi.get_universi_dependency` to get a `fastapi.Depends` that automatically sets this contextvar based on a header name that you pick.
 
-You can also set the variable yourself or even pass a different compatible contextvar to your `universi.Versions` constructor.
+You can also set the variable yourself or even pass a different compatible contextvar to your `universi.VersionBundle` constructor.
```

