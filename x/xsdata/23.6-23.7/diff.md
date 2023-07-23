# Comparing `tmp/xsdata-23.6.tar.gz` & `tmp/xsdata-23.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "xsdata-23.6.tar", last modified: Sat Jun 24 15:31:04 2023, max compression
+gzip compressed data, was "xsdata-23.7.tar", last modified: Sun Jul 23 07:34:44 2023, max compression
```

## Comparing `xsdata-23.6.tar` & `xsdata-23.7.tar`

### file list

```diff
@@ -1,498 +1,498 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.954966 xsdata-23.6/
--rw-r--r--   0 runner    (1001) docker     (123)    33027 2023-06-24 15:30:56.000000 xsdata-23.6/CHANGES.rst
--rw-r--r--   0 runner    (1001) docker     (123)     1082 2023-06-24 15:30:56.000000 xsdata-23.6/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      289 2023-06-24 15:30:56.000000 xsdata-23.6/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     5684 2023-06-24 15:31:04.954966 xsdata-23.6/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     4179 2023-06-24 15:30:56.000000 xsdata-23.6/README.rst
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.890965 xsdata-23.6/docs/
--rw-r--r--   0 runner    (1001) docker     (123)      719 2023-06-24 15:30:56.000000 xsdata-23.6/docs/Makefile
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/docs/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.890965 xsdata-23.6/docs/_ext/
--rw-r--r--   0 runner    (1001) docker     (123)     3086 2023-06-24 15:30:56.000000 xsdata-23.6/docs/_ext/xsdatadocs.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.890965 xsdata-23.6/docs/_static/
--rw-r--r--   0 runner    (1001) docker     (123)      342 2023-06-24 15:30:56.000000 xsdata-23.6/docs/_static/favicon.png
--rw-r--r--   0 runner    (1001) docker     (123)     3540 2023-06-24 15:30:56.000000 xsdata-23.6/docs/_static/logo-dark.svg
--rw-r--r--   0 runner    (1001) docker     (123)     3535 2023-06-24 15:30:56.000000 xsdata-23.6/docs/_static/logo.svg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.890965 xsdata-23.6/docs/_templates/
--rw-r--r--   0 runner    (1001) docker     (123)      143 2023-06-24 15:30:56.000000 xsdata-23.6/docs/_templates/dataclass.rst
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.890965 xsdata-23.6/docs/api/
--rw-r--r--   0 runner    (1001) docker     (123)       11 2023-06-24 15:30:56.000000 xsdata-23.6/docs/api/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)     1080 2023-06-24 15:30:56.000000 xsdata-23.6/docs/api/codegen.rst
--rw-r--r--   0 runner    (1001) docker     (123)      231 2023-06-24 15:30:56.000000 xsdata-23.6/docs/api/generics.rst
--rw-r--r--   0 runner    (1001) docker     (123)      383 2023-06-24 15:30:56.000000 xsdata-23.6/docs/api/parsing.rst
--rw-r--r--   0 runner    (1001) docker     (123)      418 2023-06-24 15:30:56.000000 xsdata-23.6/docs/api/serializing.rst
--rw-r--r--   0 runner    (1001) docker     (123)      300 2023-06-24 15:30:56.000000 xsdata-23.6/docs/api/utils.rst
--rw-r--r--   0 runner    (1001) docker     (123)      371 2023-06-24 15:30:56.000000 xsdata-23.6/docs/api/xml-context.rst
--rw-r--r--   0 runner    (1001) docker     (123)      284 2023-06-24 15:30:56.000000 xsdata-23.6/docs/api/xml-datatypes.rst
--rw-r--r--   0 runner    (1001) docker     (123)     1659 2023-06-24 15:30:56.000000 xsdata-23.6/docs/api/xml-handlers.rst
--rw-r--r--   0 runner    (1001) docker     (123)      393 2023-06-24 15:30:56.000000 xsdata-23.6/docs/api/xml-nodes.rst
--rw-r--r--   0 runner    (1001) docker     (123)     1698 2023-06-24 15:30:56.000000 xsdata-23.6/docs/api/xml-writers.rst
--rw-r--r--   0 runner    (1001) docker     (123)       82 2023-06-24 15:30:56.000000 xsdata-23.6/docs/api.rst
--rw-r--r--   0 runner    (1001) docker     (123)       49 2023-06-24 15:30:56.000000 xsdata-23.6/docs/changelog.rst
--rw-r--r--   0 runner    (1001) docker     (123)     3440 2023-06-24 15:30:56.000000 xsdata-23.6/docs/codegen.rst
--rw-r--r--   0 runner    (1001) docker     (123)     2897 2023-06-24 15:30:56.000000 xsdata-23.6/docs/conf.py
--rw-r--r--   0 runner    (1001) docker     (123)     1845 2023-06-24 15:30:56.000000 xsdata-23.6/docs/data-types-table.rst
--rw-r--r--   0 runner    (1001) docker     (123)     5841 2023-06-24 15:30:56.000000 xsdata-23.6/docs/data-types.rst
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.894965 xsdata-23.6/docs/examples/
--rw-r--r--   0 runner    (1001) docker     (123)     1166 2023-06-24 15:30:56.000000 xsdata-23.6/docs/examples/compound-fields.rst
--rw-r--r--   0 runner    (1001) docker     (123)     1213 2023-06-24 15:30:56.000000 xsdata-23.6/docs/examples/custom-class-factory.rst
--rw-r--r--   0 runner    (1001) docker     (123)     4373 2023-06-24 15:30:56.000000 xsdata-23.6/docs/examples/custom-property-names.rst
--rw-r--r--   0 runner    (1001) docker     (123)     2307 2023-06-24 15:30:56.000000 xsdata-23.6/docs/examples/custom-type-mapping.rst
--rw-r--r--   0 runner    (1001) docker     (123)     1210 2023-06-24 15:30:56.000000 xsdata-23.6/docs/examples/dataclasses-features.rst
--rw-r--r--   0 runner    (1001) docker     (123)     1138 2023-06-24 15:30:56.000000 xsdata-23.6/docs/examples/docstrings.rst
--rw-r--r--   0 runner    (1001) docker     (123)      470 2023-06-24 15:30:56.000000 xsdata-23.6/docs/examples/dtd-modeling.rst
--rw-r--r--   0 runner    (1001) docker     (123)     1359 2023-06-24 15:30:56.000000 xsdata-23.6/docs/examples/extending-models.rst
--rw-r--r--   0 runner    (1001) docker     (123)      792 2023-06-24 15:30:56.000000 xsdata-23.6/docs/examples/json-modeling.rst
--rw-r--r--   0 runner    (1001) docker     (123)     1305 2023-06-24 15:30:56.000000 xsdata-23.6/docs/examples/pycode-serializer.rst
--rw-r--r--   0 runner    (1001) docker     (123)      397 2023-06-24 15:30:56.000000 xsdata-23.6/docs/examples/samples.rst
--rw-r--r--   0 runner    (1001) docker     (123)      879 2023-06-24 15:30:56.000000 xsdata-23.6/docs/examples/w3c-suite.rst
--rw-r--r--   0 runner    (1001) docker     (123)     4426 2023-06-24 15:30:56.000000 xsdata-23.6/docs/examples/working-with-wildcards.rst
--rw-r--r--   0 runner    (1001) docker     (123)     1458 2023-06-24 15:30:56.000000 xsdata-23.6/docs/examples/wrapped-list.rst
--rw-r--r--   0 runner    (1001) docker     (123)      871 2023-06-24 15:30:56.000000 xsdata-23.6/docs/examples/xml-modeling.rst
--rw-r--r--   0 runner    (1001) docker     (123)      709 2023-06-24 15:30:56.000000 xsdata-23.6/docs/examples.rst
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.894965 xsdata-23.6/docs/faq/
--rw-r--r--   0 runner    (1001) docker     (123)      297 2023-06-24 15:30:56.000000 xsdata-23.6/docs/faq/error-parsing-dtd.rst
--rw-r--r--   0 runner    (1001) docker     (123)      509 2023-06-24 15:30:56.000000 xsdata-23.6/docs/faq/how-can-i-compare-output-results-between-versions.rst
--rw-r--r--   0 runner    (1001) docker     (123)      650 2023-06-24 15:30:56.000000 xsdata-23.6/docs/faq/why-are-elements-out-of-order.rst
--rw-r--r--   0 runner    (1001) docker     (123)      772 2023-06-24 15:30:56.000000 xsdata-23.6/docs/faq/why-i-get-a-typeerror-requires-a-single-type.rst
--rw-r--r--   0 runner    (1001) docker     (123)      750 2023-06-24 15:30:56.000000 xsdata-23.6/docs/faq/why-non-nullable-fields-are-marked-as-optional.rst
--rw-r--r--   0 runner    (1001) docker     (123)      104 2023-06-24 15:30:56.000000 xsdata-23.6/docs/faq.rst
--rw-r--r--   0 runner    (1001) docker     (123)      936 2023-06-24 15:30:56.000000 xsdata-23.6/docs/index.rst
--rw-r--r--   0 runner    (1001) docker     (123)     1472 2023-06-24 15:30:56.000000 xsdata-23.6/docs/installation.rst
--rw-r--r--   0 runner    (1001) docker     (123)    10679 2023-06-24 15:30:56.000000 xsdata-23.6/docs/json.rst
--rw-r--r--   0 runner    (1001) docker     (123)      795 2023-06-24 15:30:56.000000 xsdata-23.6/docs/make.bat
--rw-r--r--   0 runner    (1001) docker     (123)    12226 2023-06-24 15:30:56.000000 xsdata-23.6/docs/models.rst
--rw-r--r--   0 runner    (1001) docker     (123)       76 2023-06-24 15:30:56.000000 xsdata-23.6/docs/robots.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.894965 xsdata-23.6/docs/scripts/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/docs/scripts/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1250 2023-06-24 15:30:56.000000 xsdata-23.6/docs/scripts/generate_data_types.py
--rw-r--r--   0 runner    (1001) docker     (123)     4288 2023-06-24 15:30:56.000000 xsdata-23.6/docs/wsdl.rst
--rw-r--r--   0 runner    (1001) docker     (123)    12791 2023-06-24 15:30:56.000000 xsdata-23.6/docs/xml.rst
--rw-r--r--   0 runner    (1001) docker     (123)     2408 2023-06-24 15:30:56.000000 xsdata-23.6/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-06-24 15:31:04.954966 xsdata-23.6/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.894965 xsdata-23.6/tests/
--rw-r--r--   0 runner    (1001) docker     (123)      191 2023-06-24 15:30:56.000000 xsdata-23.6/tests/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.898965 xsdata-23.6/tests/codegen/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.902965 xsdata-23.6/tests/codegen/handlers/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/handlers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5512 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/handlers/test_add_attribute_substitutions.py
--rw-r--r--   0 runner    (1001) docker     (123)     3536 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/handlers/test_calculate_attribute_paths.py
--rw-r--r--   0 runner    (1001) docker     (123)     9224 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/handlers/test_create_compound_fields.py
--rw-r--r--   0 runner    (1001) docker     (123)     8496 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/handlers/test_designate_class_packages.py
--rw-r--r--   0 runner    (1001) docker     (123)     2820 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/handlers/test_filter_classes.py
--rw-r--r--   0 runner    (1001) docker     (123)     3872 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/handlers/test_flatten_attribute_groups.py
--rw-r--r--   0 runner    (1001) docker     (123)    20197 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/handlers/test_flatten_class_extensions.py
--rw-r--r--   0 runner    (1001) docker     (123)     3088 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/handlers/test_merge_attributes.py
--rw-r--r--   0 runner    (1001) docker     (123)    18994 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/handlers/test_process_attributes_types.py
--rw-r--r--   0 runner    (1001) docker     (123)     1756 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/handlers/test_process_mixed_content_class.py
--rw-r--r--   0 runner    (1001) docker     (123)     1880 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/handlers/test_rename_duplicate_attributes.py
--rw-r--r--   0 runner    (1001) docker     (123)     8332 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/handlers/test_rename_duplicate_classes.py
--rw-r--r--   0 runner    (1001) docker     (123)     3119 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/handlers/test_reset_attribute_sequence_numbers.py
--rw-r--r--   0 runner    (1001) docker     (123)     2387 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/handlers/test_reset_attribute_sequences.py
--rw-r--r--   0 runner    (1001) docker     (123)    12128 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/handlers/test_sanitize_attributes_default_value.py
--rw-r--r--   0 runner    (1001) docker     (123)     2805 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/handlers/test_sanitize_enumeration_class.py
--rw-r--r--   0 runner    (1001) docker     (123)     4034 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/handlers/test_unnest_inner_classes.py
--rw-r--r--   0 runner    (1001) docker     (123)     4273 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/handlers/test_update_attributes_effective_choice.py
--rw-r--r--   0 runner    (1001) docker     (123)     4781 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/handlers/test_vacuum_inner_classes.py
--rw-r--r--   0 runner    (1001) docker     (123)     5198 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/handlers/test_validate_attributes_overrides.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.902965 xsdata-23.6/tests/codegen/mappers/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/mappers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    29551 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/mappers/test_definitions.py
--rw-r--r--   0 runner    (1001) docker     (123)     4098 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/mappers/test_dict.py
--rw-r--r--   0 runner    (1001) docker     (123)    15415 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/mappers/test_dtd.py
--rw-r--r--   0 runner    (1001) docker     (123)    12102 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/mappers/test_element.py
--rw-r--r--   0 runner    (1001) docker     (123)    17815 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/mappers/test_schema.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.902965 xsdata-23.6/tests/codegen/models/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/models/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5340 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/models/test_attr.py
--rw-r--r--   0 runner    (1001) docker     (123)      679 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/models/test_attr_type.py
--rw-r--r--   0 runner    (1001) docker     (123)     7605 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/models/test_class.py
--rw-r--r--   0 runner    (1001) docker     (123)     4139 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/models/test_restrictions.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.902965 xsdata-23.6/tests/codegen/parsers/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/parsers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1534 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/parsers/test_definitions.py
--rw-r--r--   0 runner    (1001) docker     (123)     6593 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/parsers/test_dtd.py
--rw-r--r--   0 runner    (1001) docker     (123)    16367 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/parsers/test_schema.py
--rw-r--r--   0 runner    (1001) docker     (123)     2214 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/test_analyzer.py
--rw-r--r--   0 runner    (1001) docker     (123)     6094 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/test_container.py
--rw-r--r--   0 runner    (1001) docker     (123)     8990 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/test_resolver.py
--rw-r--r--   0 runner    (1001) docker     (123)    19370 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/test_transformer.py
--rw-r--r--   0 runner    (1001) docker     (123)    14142 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/test_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     6791 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/test_validator.py
--rw-r--r--   0 runner    (1001) docker     (123)     3109 2023-06-24 15:30:56.000000 xsdata-23.6/tests/codegen/test_writer.py
--rw-r--r--   0 runner    (1001) docker     (123)     1228 2023-06-24 15:30:56.000000 xsdata-23.6/tests/conftest.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.902965 xsdata-23.6/tests/fixtures/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.906965 xsdata-23.6/tests/fixtures/annotations/
--rw-r--r--   0 runner    (1001) docker     (123)      188 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/annotations/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      592 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/annotations/model.py
--rw-r--r--   0 runner    (1001) docker     (123)      580 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/annotations/model.xsd
--rw-r--r--   0 runner    (1001) docker     (123)       70 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/annotations/sample.xml
--rw-r--r--   0 runner    (1001) docker     (123)      189 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/annotations/units.py
--rw-r--r--   0 runner    (1001) docker     (123)      660 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/annotations/units.xsd
--rw-r--r--   0 runner    (1001) docker     (123)      950 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/annotations/xsdata.xml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.906965 xsdata-23.6/tests/fixtures/artists/
--rw-r--r--   0 runner    (1001) docker     (123)      463 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/artists/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4517 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/artists/art001.xml
--rw-r--r--   0 runner    (1001) docker     (123)     1214 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/artists/art002.xml
--rw-r--r--   0 runner    (1001) docker     (123)     2629 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/artists/art003.xml
--rw-r--r--   0 runner    (1001) docker     (123)     9186 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/artists/metadata.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.906965 xsdata-23.6/tests/fixtures/books/
--rw-r--r--   0 runner    (1001) docker     (123)      144 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/books/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      272 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/books/bk001.xml
--rw-r--r--   0 runner    (1001) docker     (123)      292 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/books/bk002.xml
--rw-r--r--   0 runner    (1001) docker     (123)      194 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/books/books-xinclude.xml
--rw-r--r--   0 runner    (1001) docker     (123)      485 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/books/books.json
--rw-r--r--   0 runner    (1001) docker     (123)     2171 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/books/books.py
--rw-r--r--   0 runner    (1001) docker     (123)      602 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/books/books.xml
--rw-r--r--   0 runner    (1001) docker     (123)      602 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/books/books_auto_ns.xml
--rw-r--r--   0 runner    (1001) docker     (123)      608 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/books/books_default_ns.xml
--rw-r--r--   0 runner    (1001) docker     (123)     3842 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/books/fixtures.py
--rw-r--r--   0 runner    (1001) docker     (123)     2405 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/books/schema.xsd
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.910965 xsdata-23.6/tests/fixtures/calculator/
--rw-r--r--   0 runner    (1001) docker     (123)      290 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/calculator/AddRQ.xml
--rw-r--r--   0 runner    (1001) docker     (123)      399 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/calculator/AddRS.xml
--rw-r--r--   0 runner    (1001) docker     (123)     1084 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/calculator/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    13531 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/calculator/services.py
--rw-r--r--   0 runner    (1001) docker     (123)     7880 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/calculator/services.wsdl
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.910965 xsdata-23.6/tests/fixtures/compound/
--rw-r--r--   0 runner    (1001) docker     (123)      132 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/compound/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      920 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/compound/models.py
--rw-r--r--   0 runner    (1001) docker     (123)      260 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/compound/sample.json
--rw-r--r--   0 runner    (1001) docker     (123)      182 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/compound/sample.xml
--rw-r--r--   0 runner    (1001) docker     (123)      214 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/compound/sample.xsdata.xml
--rw-r--r--   0 runner    (1001) docker     (123)      606 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/compound/schema.xsd
--rw-r--r--   0 runner    (1001) docker     (123)      680 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/datatypes.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.910965 xsdata-23.6/tests/fixtures/docstrings/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/docstrings/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.910965 xsdata-23.6/tests/fixtures/docstrings/accessible/
--rw-r--r--   0 runner    (1001) docker     (123)      287 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/docstrings/accessible/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2933 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/docstrings/accessible/schema.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.910965 xsdata-23.6/tests/fixtures/docstrings/blank/
--rw-r--r--   0 runner    (1001) docker     (123)      282 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/docstrings/blank/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1492 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/docstrings/blank/schema.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.910965 xsdata-23.6/tests/fixtures/docstrings/google/
--rw-r--r--   0 runner    (1001) docker     (123)      283 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/docstrings/google/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2867 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/docstrings/google/schema.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.910965 xsdata-23.6/tests/fixtures/docstrings/numpy/
--rw-r--r--   0 runner    (1001) docker     (123)      282 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/docstrings/numpy/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2871 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/docstrings/numpy/schema.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.910965 xsdata-23.6/tests/fixtures/docstrings/rst/
--rw-r--r--   0 runner    (1001) docker     (123)      280 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/docstrings/rst/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2797 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/docstrings/rst/schema.py
--rw-r--r--   0 runner    (1001) docker     (123)     4081 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/docstrings/schema.xsd
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.910965 xsdata-23.6/tests/fixtures/dtd/
--rw-r--r--   0 runner    (1001) docker     (123)       15 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/dtd/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      400 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/dtd/complete_example.dtd
--rw-r--r--   0 runner    (1001) docker     (123)      113 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/dtd/default_namespace.dtd
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.914965 xsdata-23.6/tests/fixtures/dtd/models/
--rw-r--r--   0 runner    (1001) docker     (123)      174 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/dtd/models/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2120 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/dtd/models/complete_example.py
--rw-r--r--   0 runner    (1001) docker     (123)      131 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/dtd/prefix_namespace.dtd
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.914965 xsdata-23.6/tests/fixtures/hello/
--rw-r--r--   0 runner    (1001) docker     (123)      277 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/hello/HelloRQ.xml
--rw-r--r--   0 runner    (1001) docker     (123)      275 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/hello/HelloRS.xml
--rw-r--r--   0 runner    (1001) docker     (123)      489 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/hello/HelloRS_SoapFault.xml
--rw-r--r--   0 runner    (1001) docker     (123)      430 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/hello/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4515 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/hello/hello.py
--rw-r--r--   0 runner    (1001) docker     (123)     3084 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/hello/hello.wsdl
--rw-r--r--   0 runner    (1001) docker     (123)      781 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/hello/hello.xsd
--rw-r--r--   0 runner    (1001) docker     (123)     4626 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/models.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.914965 xsdata-23.6/tests/fixtures/primer/
--rw-r--r--   0 runner    (1001) docker     (123)      231 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/primer/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4565 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/primer/order.py
--rw-r--r--   0 runner    (1001) docker     (123)     3032 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/primer/order.xsd
--rw-r--r--   0 runner    (1001) docker     (123)      840 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/primer/sample.json
--rw-r--r--   0 runner    (1001) docker     (123)      881 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/primer/sample.xml
--rw-r--r--   0 runner    (1001) docker     (123)      889 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/primer/sample.xsdata.xml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.914965 xsdata-23.6/tests/fixtures/series/
--rw-r--r--   0 runner    (1001) docker     (123)      344 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/series/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.914965 xsdata-23.6/tests/fixtures/series/samples/
--rw-r--r--   0 runner    (1001) docker     (123)     1263 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/series/samples/show1.json
--rw-r--r--   0 runner    (1001) docker     (123)     1278 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/series/samples/show2.json
--rw-r--r--   0 runner    (1001) docker     (123)     6626 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/series/series.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.914965 xsdata-23.6/tests/fixtures/stripe/
--rw-r--r--   0 runner    (1001) docker     (123)      931 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/stripe/.xsdata.xml
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/stripe/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.914965 xsdata-23.6/tests/fixtures/stripe/models/
--rw-r--r--   0 runner    (1001) docker     (123)      208 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/stripe/models/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3019 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/stripe/models/balance.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.914965 xsdata-23.6/tests/fixtures/stripe/samples/
--rw-r--r--   0 runner    (1001) docker     (123)     2628 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/stripe/samples/balance.json
--rw-r--r--   0 runner    (1001) docker     (123)      137 2023-06-24 15:30:56.000000 xsdata-23.6/tests/fixtures/submodels.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.918965 xsdata-23.6/tests/formats/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.918965 xsdata-23.6/tests/formats/dataclass/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.918965 xsdata-23.6/tests/formats/dataclass/models/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/models/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    18738 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/models/test_builders.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.918965 xsdata-23.6/tests/formats/dataclass/parsers/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/parsers/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.918965 xsdata-23.6/tests/formats/dataclass/parsers/handlers/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/parsers/handlers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2894 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/parsers/handlers/test_lxml.py
--rw-r--r--   0 runner    (1001) docker     (123)     3318 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/parsers/handlers/test_native.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.922966 xsdata-23.6/tests/formats/dataclass/parsers/nodes/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/parsers/nodes/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    20127 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/parsers/nodes/test_element.py
--rw-r--r--   0 runner    (1001) docker     (123)     3263 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/parsers/nodes/test_primitive.py
--rw-r--r--   0 runner    (1001) docker     (123)      377 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/parsers/nodes/test_skip.py
--rw-r--r--   0 runner    (1001) docker     (123)     1676 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/parsers/nodes/test_standard.py
--rw-r--r--   0 runner    (1001) docker     (123)     3986 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/parsers/nodes/test_union.py
--rw-r--r--   0 runner    (1001) docker     (123)     2229 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/parsers/nodes/test_wildcard.py
--rw-r--r--   0 runner    (1001) docker     (123)     2780 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/parsers/nodes/test_wrapper.py
--rw-r--r--   0 runner    (1001) docker     (123)    13688 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/parsers/test_json.py
--rw-r--r--   0 runner    (1001) docker     (123)     1260 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/parsers/test_mixins.py
--rw-r--r--   0 runner    (1001) docker     (123)     7766 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/parsers/test_node.py
--rw-r--r--   0 runner    (1001) docker     (123)      981 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/parsers/test_tree.py
--rw-r--r--   0 runner    (1001) docker     (123)     3877 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/parsers/test_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     2297 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/parsers/test_xml.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.922966 xsdata-23.6/tests/formats/dataclass/serializers/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/serializers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3392 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/serializers/test_code.py
--rw-r--r--   0 runner    (1001) docker     (123)     5884 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/serializers/test_json.py
--rw-r--r--   0 runner    (1001) docker     (123)     7162 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/serializers/test_mixins.py
--rw-r--r--   0 runner    (1001) docker     (123)    24101 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/serializers/test_xml.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.922966 xsdata-23.6/tests/formats/dataclass/serializers/writers/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/serializers/writers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2746 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/serializers/writers/test_lxml.py
--rw-r--r--   0 runner    (1001) docker     (123)     2637 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/serializers/writers/test_native.py
--rw-r--r--   0 runner    (1001) docker     (123)     5152 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/test_client.py
--rw-r--r--   0 runner    (1001) docker     (123)     1195 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/test_compat.py
--rw-r--r--   0 runner    (1001) docker     (123)     5673 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/test_context.py
--rw-r--r--   0 runner    (1001) docker     (123)     9580 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/test_elements.py
--rw-r--r--   0 runner    (1001) docker     (123)    40645 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/test_filters.py
--rw-r--r--   0 runner    (1001) docker     (123)     7450 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/test_generator.py
--rw-r--r--   0 runner    (1001) docker     (123)     2699 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/test_transport.py
--rw-r--r--   0 runner    (1001) docker     (123)     6643 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/dataclass/test_typing.py
--rw-r--r--   0 runner    (1001) docker     (123)    15785 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/test_converter.py
--rw-r--r--   0 runner    (1001) docker     (123)     2821 2023-06-24 15:30:56.000000 xsdata-23.6/tests/formats/test_mixins.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.926966 xsdata-23.6/tests/integration/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/tests/integration/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.926966 xsdata-23.6/tests/integration/benchmarks/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/tests/integration/benchmarks/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      301 2023-06-24 15:30:56.000000 xsdata-23.6/tests/integration/benchmarks/conftest.py
--rw-r--r--   0 runner    (1001) docker     (123)      876 2023-06-24 15:30:56.000000 xsdata-23.6/tests/integration/benchmarks/test_converters.py
--rw-r--r--   0 runner    (1001) docker     (123)     1331 2023-06-24 15:30:56.000000 xsdata-23.6/tests/integration/benchmarks/test_handlers.py
--rw-r--r--   0 runner    (1001) docker     (123)     2023 2023-06-24 15:30:56.000000 xsdata-23.6/tests/integration/benchmarks/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     1091 2023-06-24 15:30:56.000000 xsdata-23.6/tests/integration/test_annotations.py
--rw-r--r--   0 runner    (1001) docker     (123)     1166 2023-06-24 15:30:56.000000 xsdata-23.6/tests/integration/test_artists.py
--rw-r--r--   0 runner    (1001) docker     (123)      778 2023-06-24 15:30:56.000000 xsdata-23.6/tests/integration/test_books.py
--rw-r--r--   0 runner    (1001) docker     (123)     1991 2023-06-24 15:30:56.000000 xsdata-23.6/tests/integration/test_calculator.py
--rw-r--r--   0 runner    (1001) docker     (123)      655 2023-06-24 15:30:56.000000 xsdata-23.6/tests/integration/test_compound.py
--rw-r--r--   0 runner    (1001) docker     (123)     1880 2023-06-24 15:30:56.000000 xsdata-23.6/tests/integration/test_docstrings.py
--rw-r--r--   0 runner    (1001) docker     (123)      578 2023-06-24 15:30:56.000000 xsdata-23.6/tests/integration/test_dtd.py
--rw-r--r--   0 runner    (1001) docker     (123)     3781 2023-06-24 15:30:56.000000 xsdata-23.6/tests/integration/test_hello_rpc.py
--rw-r--r--   0 runner    (1001) docker     (123)      690 2023-06-24 15:30:56.000000 xsdata-23.6/tests/integration/test_primer.py
--rw-r--r--   0 runner    (1001) docker     (123)     1279 2023-06-24 15:30:56.000000 xsdata-23.6/tests/integration/test_series.py
--rw-r--r--   0 runner    (1001) docker     (123)     1318 2023-06-24 15:30:56.000000 xsdata-23.6/tests/integration/test_stripe.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.926966 xsdata-23.6/tests/models/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.926966 xsdata-23.6/tests/models/enums/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/enums/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2956 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/enums/test_datatype.py
--rw-r--r--   0 runner    (1001) docker     (123)    11825 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/test_config.py
--rw-r--r--   0 runner    (1001) docker     (123)    21919 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/test_datatype.py
--rw-r--r--   0 runner    (1001) docker     (123)     6013 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/test_mixins.py
--rw-r--r--   0 runner    (1001) docker     (123)     1223 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/test_type_mapping.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.926966 xsdata-23.6/tests/models/typemapping/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/typemapping/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      337 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/typemapping/city.py
--rw-r--r--   0 runner    (1001) docker     (123)      294 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/typemapping/house.py
--rw-r--r--   0 runner    (1001) docker     (123)      448 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/typemapping/street.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.926966 xsdata-23.6/tests/models/wsdl/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/wsdl/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      700 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/wsdl/test_binding.py
--rw-r--r--   0 runner    (1001) docker     (123)     3104 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/wsdl/test_definitions.py
--rw-r--r--   0 runner    (1001) docker     (123)      569 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/wsdl/test_port_type.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.930966 xsdata-23.6/tests/models/xsd/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/xsd/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      259 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/xsd/test_all.py
--rw-r--r--   0 runner    (1001) docker     (123)      722 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/xsd/test_alternative.py
--rw-r--r--   0 runner    (1001) docker     (123)     1410 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/xsd/test_annotation_base.py
--rw-r--r--   0 runner    (1001) docker     (123)     1381 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/xsd/test_any.py
--rw-r--r--   0 runner    (1001) docker     (123)     1411 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/xsd/test_any_attribute.py
--rw-r--r--   0 runner    (1001) docker     (123)     2585 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/xsd/test_attribute.py
--rw-r--r--   0 runner    (1001) docker     (123)      432 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/xsd/test_attribute_group.py
--rw-r--r--   0 runner    (1001) docker     (123)      440 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/xsd/test_choice.py
--rw-r--r--   0 runner    (1001) docker     (123)      303 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/xsd/test_complex_content.py
--rw-r--r--   0 runner    (1001) docker     (123)      533 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/xsd/test_complex_type.py
--rw-r--r--   0 runner    (1001) docker     (123)     3420 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/xsd/test_element.py
--rw-r--r--   0 runner    (1001) docker     (123)      691 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/xsd/test_enumeration.py
--rw-r--r--   0 runner    (1001) docker     (123)      292 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/xsd/test_extension.py
--rw-r--r--   0 runner    (1001) docker     (123)      565 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/xsd/test_group.py
--rw-r--r--   0 runner    (1001) docker     (123)      607 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/xsd/test_list.py
--rw-r--r--   0 runner    (1001) docker     (123)     3119 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/xsd/test_restriction.py
--rw-r--r--   0 runner    (1001) docker     (123)     1442 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/xsd/test_schema.py
--rw-r--r--   0 runner    (1001) docker     (123)      462 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/xsd/test_sequence.py
--rw-r--r--   0 runner    (1001) docker     (123)     1864 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/xsd/test_simple_type.py
--rw-r--r--   0 runner    (1001) docker     (123)     1960 2023-06-24 15:30:56.000000 xsdata-23.6/tests/models/xsd/test_union.py
--rw-r--r--   0 runner    (1001) docker     (123)     7468 2023-06-24 15:30:56.000000 xsdata-23.6/tests/test_cli.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.930966 xsdata-23.6/tests/utils/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/tests/utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1899 2023-06-24 15:30:56.000000 xsdata-23.6/tests/utils/test_collections.py
--rw-r--r--   0 runner    (1001) docker     (123)     4611 2023-06-24 15:30:56.000000 xsdata-23.6/tests/utils/test_dates.py
--rw-r--r--   0 runner    (1001) docker     (123)     5495 2023-06-24 15:30:56.000000 xsdata-23.6/tests/utils/test_downloader.py
--rw-r--r--   0 runner    (1001) docker     (123)     1244 2023-06-24 15:30:56.000000 xsdata-23.6/tests/utils/test_hooks.py
--rw-r--r--   0 runner    (1001) docker     (123)     5503 2023-06-24 15:30:56.000000 xsdata-23.6/tests/utils/test_namespaces.py
--rw-r--r--   0 runner    (1001) docker     (123)      428 2023-06-24 15:30:56.000000 xsdata-23.6/tests/utils/test_objects.py
--rw-r--r--   0 runner    (1001) docker     (123)      508 2023-06-24 15:30:56.000000 xsdata-23.6/tests/utils/test_testing.py
--rw-r--r--   0 runner    (1001) docker     (123)     8010 2023-06-24 15:30:56.000000 xsdata-23.6/tests/utils/test_text.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.934966 xsdata-23.6/xsdata/
--rw-r--r--   0 runner    (1001) docker     (123)       21 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      236 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/__main__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5143 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/cli.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.934966 xsdata-23.6/xsdata/codegen/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1638 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/analyzer.py
--rw-r--r--   0 runner    (1001) docker     (123)     6074 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/container.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.938966 xsdata-23.6/xsdata/codegen/handlers/
--rw-r--r--   0 runner    (1001) docker     (123)     1880 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/handlers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3479 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/handlers/add_attribute_substitutions.py
--rw-r--r--   0 runner    (1001) docker     (123)     1545 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/handlers/calculate_attribute_paths.py
--rw-r--r--   0 runner    (1001) docker     (123)     5057 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/handlers/create_compound_fields.py
--rw-r--r--   0 runner    (1001) docker     (123)     6186 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/handlers/designate_class_packages.py
--rw-r--r--   0 runner    (1001) docker     (123)     1818 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/handlers/filter_classes.py
--rw-r--r--   0 runner    (1001) docker     (123)     1558 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/handlers/flatten_attribute_groups.py
--rw-r--r--   0 runner    (1001) docker     (123)    11284 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/handlers/flatten_class_extensions.py
--rw-r--r--   0 runner    (1001) docker     (123)     2035 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/handlers/merge_attributes.py
--rw-r--r--   0 runner    (1001) docker     (123)     9866 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/handlers/process_attributes_types.py
--rw-r--r--   0 runner    (1001) docker     (123)     1612 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/handlers/process_mixed_content_class.py
--rw-r--r--   0 runner    (1001) docker     (123)      996 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/handlers/rename_duplicate_attributes.py
--rw-r--r--   0 runner    (1001) docker     (123)     4651 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/handlers/rename_duplicate_classes.py
--rw-r--r--   0 runner    (1001) docker     (123)     1100 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/handlers/reset_attribute_sequence_numbers.py
--rw-r--r--   0 runner    (1001) docker     (123)     1256 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/handlers/reset_attribute_sequences.py
--rw-r--r--   0 runner    (1001) docker     (123)     6470 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/handlers/sanitize_attributes_default_value.py
--rw-r--r--   0 runner    (1001) docker     (123)     1785 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/handlers/sanitize_enumeration_class.py
--rw-r--r--   0 runner    (1001) docker     (123)     1817 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/handlers/unnest_inner_classes.py
--rw-r--r--   0 runner    (1001) docker     (123)     3832 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/handlers/update_attributes_effective_choice.py
--rw-r--r--   0 runner    (1001) docker     (123)     2786 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/handlers/vacuum_inner_classes.py
--rw-r--r--   0 runner    (1001) docker     (123)     2724 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/handlers/validate_attributes_overrides.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.938966 xsdata-23.6/xsdata/codegen/mappers/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/mappers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    14427 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/mappers/definitions.py
--rw-r--r--   0 runner    (1001) docker     (123)     1782 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/mappers/dict.py
--rw-r--r--   0 runner    (1001) docker     (123)     7884 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/mappers/dtd.py
--rw-r--r--   0 runner    (1001) docker     (123)     6501 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/mappers/element.py
--rw-r--r--   0 runner    (1001) docker     (123)    10096 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/mappers/schema.py
--rw-r--r--   0 runner    (1001) docker     (123)     2890 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/mixins.py
--rw-r--r--   0 runner    (1001) docker     (123)    20155 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/models.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.942966 xsdata-23.6/xsdata/codegen/parsers/
--rw-r--r--   0 runner    (1001) docker     (123)      169 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/parsers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      638 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/parsers/definitions.py
--rw-r--r--   0 runner    (1001) docker     (123)     2868 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/parsers/dtd.py
--rw-r--r--   0 runner    (1001) docker     (123)     9826 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/parsers/schema.py
--rw-r--r--   0 runner    (1001) docker     (123)     4882 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/resolver.py
--rw-r--r--   0 runner    (1001) docker     (123)    11953 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/transformer.py
--rw-r--r--   0 runner    (1001) docker     (123)    11309 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     5281 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/validator.py
--rw-r--r--   0 runner    (1001) docker     (123)     2332 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/codegen/writer.py
--rw-r--r--   0 runner    (1001) docker     (123)     1352 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/exceptions.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.942966 xsdata-23.6/xsdata/formats/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1187 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/bindings.py
--rw-r--r--   0 runner    (1001) docker     (123)    16154 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/converter.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.942966 xsdata-23.6/xsdata/formats/dataclass/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4535 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/client.py
--rw-r--r--   0 runner    (1001) docker     (123)     4082 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/compat.py
--rw-r--r--   0 runner    (1001) docker     (123)     8947 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/context.py
--rw-r--r--   0 runner    (1001) docker     (123)    29441 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/filters.py
--rw-r--r--   0 runner    (1001) docker     (123)     5236 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/generator.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.942966 xsdata-23.6/xsdata/formats/dataclass/models/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/models/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    17822 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/models/builders.py
--rw-r--r--   0 runner    (1001) docker     (123)    13241 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/models/elements.py
--rw-r--r--   0 runner    (1001) docker     (123)     1364 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/models/generics.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.942966 xsdata-23.6/xsdata/formats/dataclass/parsers/
--rw-r--r--   0 runner    (1001) docker     (123)      314 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/parsers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7257 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/parsers/bases.py
--rw-r--r--   0 runner    (1001) docker     (123)     1892 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/parsers/config.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.946966 xsdata-23.6/xsdata/formats/dataclass/parsers/handlers/
--rw-r--r--   0 runner    (1001) docker     (123)      537 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/parsers/handlers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2782 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/parsers/handlers/lxml.py
--rw-r--r--   0 runner    (1001) docker     (123)     4217 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/parsers/handlers/native.py
--rw-r--r--   0 runner    (1001) docker     (123)    11828 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/parsers/json.py
--rw-r--r--   0 runner    (1001) docker     (123)     5621 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/parsers/mixins.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.946966 xsdata-23.6/xsdata/formats/dataclass/parsers/nodes/
--rw-r--r--   0 runner    (1001) docker     (123)      642 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/parsers/nodes/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    14972 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/parsers/nodes/element.py
--rw-r--r--   0 runner    (1001) docker     (123)     1820 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/parsers/nodes/primitive.py
--rw-r--r--   0 runner    (1001) docker     (123)      649 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/parsers/nodes/skip.py
--rw-r--r--   0 runner    (1001) docker     (123)     1771 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/parsers/nodes/standard.py
--rw-r--r--   0 runner    (1001) docker     (123)     4274 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/parsers/nodes/union.py
--rw-r--r--   0 runner    (1001) docker     (123)     2545 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/parsers/nodes/wildcard.py
--rw-r--r--   0 runner    (1001) docker     (123)      736 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/parsers/nodes/wrapper.py
--rw-r--r--   0 runner    (1001) docker     (123)     2133 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/parsers/tree.py
--rw-r--r--   0 runner    (1001) docker     (123)     3044 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/parsers/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     2984 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/parsers/xml.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.946966 xsdata-23.6/xsdata/formats/dataclass/serializers/
--rw-r--r--   0 runner    (1001) docker     (123)      374 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/serializers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4560 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/serializers/code.py
--rw-r--r--   0 runner    (1001) docker     (123)     1996 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/serializers/config.py
--rw-r--r--   0 runner    (1001) docker     (123)     3480 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/serializers/json.py
--rw-r--r--   0 runner    (1001) docker     (123)     9629 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/serializers/mixins.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.946966 xsdata-23.6/xsdata/formats/dataclass/serializers/writers/
--rw-r--r--   0 runner    (1001) docker     (123)      520 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/serializers/writers/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1673 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/serializers/writers/lxml.py
--rw-r--r--   0 runner    (1001) docker     (123)     2280 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/serializers/writers/native.py
--rw-r--r--   0 runner    (1001) docker     (123)    16192 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/serializers/xml.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.950966 xsdata-23.6/xsdata/formats/dataclass/templates/
--rw-r--r--   0 runner    (1001) docker     (123)     2322 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/templates/class.jinja2
--rw-r--r--   0 runner    (1001) docker     (123)       52 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/templates/docstrings.accessible.jinja2
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/templates/docstrings.blank.jinja2
--rw-r--r--   0 runner    (1001) docker     (123)      291 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/templates/docstrings.google.jinja2
--rw-r--r--   0 runner    (1001) docker     (123)      329 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/templates/docstrings.numpy.jinja2
--rw-r--r--   0 runner    (1001) docker     (123)      360 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/templates/docstrings.rst.jinja2
--rw-r--r--   0 runner    (1001) docker     (123)      781 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/templates/enum.jinja2
--rw-r--r--   0 runner    (1001) docker     (123)      376 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/templates/imports.jinja2
--rw-r--r--   0 runner    (1001) docker     (123)      141 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/templates/module.jinja2
--rw-r--r--   0 runner    (1001) docker     (123)      298 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/templates/package.jinja2
--rw-r--r--   0 runner    (1001) docker     (123)      146 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/templates/service.jinja2
--rw-r--r--   0 runner    (1001) docker     (123)     1778 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/transports.py
--rw-r--r--   0 runner    (1001) docker     (123)     4319 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/dataclass/typing.py
--rw-r--r--   0 runner    (1001) docker     (123)     3317 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/formats/mixins.py
--rw-r--r--   0 runner    (1001) docker     (123)       53 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/logger.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.950966 xsdata-23.6/xsdata/models/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/models/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    21294 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/models/config.py
--rw-r--r--   0 runner    (1001) docker     (123)    20286 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/models/datatype.py
--rw-r--r--   0 runner    (1001) docker     (123)     1828 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/models/dtd.py
--rw-r--r--   0 runner    (1001) docker     (123)     9818 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/models/enums.py
--rw-r--r--   0 runner    (1001) docker     (123)     7886 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/models/mixins.py
--rw-r--r--   0 runner    (1001) docker     (123)     5749 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/models/wsdl.py
--rw-r--r--   0 runner    (1001) docker     (123)    36973 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/models/xsd.py
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/py.typed
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.950966 xsdata-23.6/xsdata/schemas/
--rw-r--r--   0 runner    (1001) docker     (123)     4067 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/schemas/mathml3-common.xsd
--rw-r--r--   0 runner    (1001) docker     (123)    28457 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/schemas/mathml3-content.xsd
--rw-r--r--   0 runner    (1001) docker     (123)    84129 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/schemas/mathml3-presentation.xsd
--rw-r--r--   0 runner    (1001) docker     (123)     6846 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/schemas/mathml3-strict-content.xsd
--rw-r--r--   0 runner    (1001) docker     (123)      436 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/schemas/mathml3.xsd
--rw-r--r--   0 runner    (1001) docker     (123)     8051 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/schemas/xlink.xsd
--rw-r--r--   0 runner    (1001) docker     (123)     1206 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/schemas/xml.xsd
--rw-r--r--   0 runner    (1001) docker     (123)      347 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/schemas/xsi.xsd
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.954966 xsdata-23.6/xsdata/utils/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4204 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/utils/click.py
--rw-r--r--   0 runner    (1001) docker     (123)     3036 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/utils/collections.py
--rw-r--r--   0 runner    (1001) docker     (123)      489 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/utils/constants.py
--rw-r--r--   0 runner    (1001) docker     (123)     6709 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/utils/dates.py
--rw-r--r--   0 runner    (1001) docker     (123)      741 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/utils/debug.py
--rw-r--r--   0 runner    (1001) docker     (123)     4782 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/utils/downloader.py
--rw-r--r--   0 runner    (1001) docker     (123)     1208 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/utils/graphs.py
--rw-r--r--   0 runner    (1001) docker     (123)      453 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/utils/hooks.py
--rw-r--r--   0 runner    (1001) docker     (123)     5041 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/utils/namespaces.py
--rw-r--r--   0 runner    (1001) docker     (123)      812 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/utils/objects.py
--rw-r--r--   0 runner    (1001) docker     (123)      694 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/utils/package.py
--rw-r--r--   0 runner    (1001) docker     (123)    17285 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/utils/testing.py
--rw-r--r--   0 runner    (1001) docker     (123)     4961 2023-06-24 15:30:56.000000 xsdata-23.6/xsdata/utils/text.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-06-24 15:31:04.934966 xsdata-23.6/xsdata.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     5684 2023-06-24 15:31:04.000000 xsdata-23.6/xsdata.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)    15635 2023-06-24 15:31:04.000000 xsdata-23.6/xsdata.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-06-24 15:31:04.000000 xsdata-23.6/xsdata.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       48 2023-06-24 15:31:04.000000 xsdata-23.6/xsdata.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)      344 2023-06-24 15:31:04.000000 xsdata-23.6/xsdata.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        7 2023-06-24 15:31:04.000000 xsdata-23.6/xsdata.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.221787 xsdata-23.7/
+-rw-r--r--   0 runner    (1001) docker     (123)    33511 2023-07-23 07:34:32.000000 xsdata-23.7/CHANGES.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     1082 2023-07-23 07:34:32.000000 xsdata-23.7/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      289 2023-07-23 07:34:32.000000 xsdata-23.7/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     5197 2023-07-23 07:34:44.221787 xsdata-23.7/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     3692 2023-07-23 07:34:32.000000 xsdata-23.7/README.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.173787 xsdata-23.7/docs/
+-rw-r--r--   0 runner    (1001) docker     (123)      719 2023-07-23 07:34:32.000000 xsdata-23.7/docs/Makefile
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/docs/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.173787 xsdata-23.7/docs/_ext/
+-rw-r--r--   0 runner    (1001) docker     (123)     3086 2023-07-23 07:34:32.000000 xsdata-23.7/docs/_ext/xsdatadocs.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.173787 xsdata-23.7/docs/_static/
+-rw-r--r--   0 runner    (1001) docker     (123)      342 2023-07-23 07:34:32.000000 xsdata-23.7/docs/_static/favicon.png
+-rw-r--r--   0 runner    (1001) docker     (123)     3540 2023-07-23 07:34:32.000000 xsdata-23.7/docs/_static/logo-dark.svg
+-rw-r--r--   0 runner    (1001) docker     (123)     3535 2023-07-23 07:34:32.000000 xsdata-23.7/docs/_static/logo.svg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.173787 xsdata-23.7/docs/_templates/
+-rw-r--r--   0 runner    (1001) docker     (123)      143 2023-07-23 07:34:32.000000 xsdata-23.7/docs/_templates/dataclass.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.177787 xsdata-23.7/docs/api/
+-rw-r--r--   0 runner    (1001) docker     (123)       11 2023-07-23 07:34:32.000000 xsdata-23.7/docs/api/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)     1080 2023-07-23 07:34:32.000000 xsdata-23.7/docs/api/codegen.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      231 2023-07-23 07:34:32.000000 xsdata-23.7/docs/api/generics.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      383 2023-07-23 07:34:32.000000 xsdata-23.7/docs/api/parsing.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      418 2023-07-23 07:34:32.000000 xsdata-23.7/docs/api/serializing.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      300 2023-07-23 07:34:32.000000 xsdata-23.7/docs/api/utils.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      371 2023-07-23 07:34:32.000000 xsdata-23.7/docs/api/xml-context.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      284 2023-07-23 07:34:32.000000 xsdata-23.7/docs/api/xml-datatypes.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     1659 2023-07-23 07:34:32.000000 xsdata-23.7/docs/api/xml-handlers.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      393 2023-07-23 07:34:32.000000 xsdata-23.7/docs/api/xml-nodes.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     1698 2023-07-23 07:34:32.000000 xsdata-23.7/docs/api/xml-writers.rst
+-rw-r--r--   0 runner    (1001) docker     (123)       82 2023-07-23 07:34:32.000000 xsdata-23.7/docs/api.rst
+-rw-r--r--   0 runner    (1001) docker     (123)       49 2023-07-23 07:34:32.000000 xsdata-23.7/docs/changelog.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     3440 2023-07-23 07:34:32.000000 xsdata-23.7/docs/codegen.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     2897 2023-07-23 07:34:32.000000 xsdata-23.7/docs/conf.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1845 2023-07-23 07:34:32.000000 xsdata-23.7/docs/data-types-table.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     5841 2023-07-23 07:34:32.000000 xsdata-23.7/docs/data-types.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.177787 xsdata-23.7/docs/examples/
+-rw-r--r--   0 runner    (1001) docker     (123)     1166 2023-07-23 07:34:32.000000 xsdata-23.7/docs/examples/compound-fields.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     1213 2023-07-23 07:34:32.000000 xsdata-23.7/docs/examples/custom-class-factory.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     4373 2023-07-23 07:34:32.000000 xsdata-23.7/docs/examples/custom-property-names.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     2307 2023-07-23 07:34:32.000000 xsdata-23.7/docs/examples/custom-type-mapping.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     1210 2023-07-23 07:34:32.000000 xsdata-23.7/docs/examples/dataclasses-features.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     1138 2023-07-23 07:34:32.000000 xsdata-23.7/docs/examples/docstrings.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      470 2023-07-23 07:34:32.000000 xsdata-23.7/docs/examples/dtd-modeling.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     1359 2023-07-23 07:34:32.000000 xsdata-23.7/docs/examples/extending-models.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      792 2023-07-23 07:34:32.000000 xsdata-23.7/docs/examples/json-modeling.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     1305 2023-07-23 07:34:32.000000 xsdata-23.7/docs/examples/pycode-serializer.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      397 2023-07-23 07:34:32.000000 xsdata-23.7/docs/examples/samples.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      879 2023-07-23 07:34:32.000000 xsdata-23.7/docs/examples/w3c-suite.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     4426 2023-07-23 07:34:32.000000 xsdata-23.7/docs/examples/working-with-wildcards.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     1458 2023-07-23 07:34:32.000000 xsdata-23.7/docs/examples/wrapped-list.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      871 2023-07-23 07:34:32.000000 xsdata-23.7/docs/examples/xml-modeling.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      709 2023-07-23 07:34:32.000000 xsdata-23.7/docs/examples.rst
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.177787 xsdata-23.7/docs/faq/
+-rw-r--r--   0 runner    (1001) docker     (123)      297 2023-07-23 07:34:32.000000 xsdata-23.7/docs/faq/error-parsing-dtd.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      509 2023-07-23 07:34:32.000000 xsdata-23.7/docs/faq/how-can-i-compare-output-results-between-versions.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      650 2023-07-23 07:34:32.000000 xsdata-23.7/docs/faq/why-are-elements-out-of-order.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      772 2023-07-23 07:34:32.000000 xsdata-23.7/docs/faq/why-i-get-a-typeerror-requires-a-single-type.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      750 2023-07-23 07:34:32.000000 xsdata-23.7/docs/faq/why-non-nullable-fields-are-marked-as-optional.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      104 2023-07-23 07:34:32.000000 xsdata-23.7/docs/faq.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      936 2023-07-23 07:34:32.000000 xsdata-23.7/docs/index.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     1463 2023-07-23 07:34:32.000000 xsdata-23.7/docs/installation.rst
+-rw-r--r--   0 runner    (1001) docker     (123)    10679 2023-07-23 07:34:32.000000 xsdata-23.7/docs/json.rst
+-rw-r--r--   0 runner    (1001) docker     (123)      795 2023-07-23 07:34:32.000000 xsdata-23.7/docs/make.bat
+-rw-r--r--   0 runner    (1001) docker     (123)    12226 2023-07-23 07:34:32.000000 xsdata-23.7/docs/models.rst
+-rw-r--r--   0 runner    (1001) docker     (123)       76 2023-07-23 07:34:32.000000 xsdata-23.7/docs/robots.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.177787 xsdata-23.7/docs/scripts/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/docs/scripts/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1250 2023-07-23 07:34:32.000000 xsdata-23.7/docs/scripts/generate_data_types.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4288 2023-07-23 07:34:32.000000 xsdata-23.7/docs/wsdl.rst
+-rw-r--r--   0 runner    (1001) docker     (123)    12791 2023-07-23 07:34:32.000000 xsdata-23.7/docs/xml.rst
+-rw-r--r--   0 runner    (1001) docker     (123)     2408 2023-07-23 07:34:32.000000 xsdata-23.7/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 07:34:44.221787 xsdata-23.7/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.181787 xsdata-23.7/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)      191 2023-07-23 07:34:32.000000 xsdata-23.7/tests/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.181787 xsdata-23.7/tests/codegen/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.185787 xsdata-23.7/tests/codegen/handlers/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/handlers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5512 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/handlers/test_add_attribute_substitutions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3832 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/handlers/test_calculate_attribute_paths.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10964 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/handlers/test_create_compound_fields.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8496 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/handlers/test_designate_class_packages.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2820 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/handlers/test_filter_classes.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3872 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/handlers/test_flatten_attribute_groups.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20197 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/handlers/test_flatten_class_extensions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3088 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/handlers/test_merge_attributes.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18994 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/handlers/test_process_attributes_types.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1756 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/handlers/test_process_mixed_content_class.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1880 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/handlers/test_rename_duplicate_attributes.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8332 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/handlers/test_rename_duplicate_classes.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3119 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/handlers/test_reset_attribute_sequence_numbers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2387 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/handlers/test_reset_attribute_sequences.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12128 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/handlers/test_sanitize_attributes_default_value.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2805 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/handlers/test_sanitize_enumeration_class.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4034 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/handlers/test_unnest_inner_classes.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4273 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/handlers/test_update_attributes_effective_choice.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4781 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/handlers/test_vacuum_inner_classes.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5523 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/handlers/test_validate_attributes_overrides.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.185787 xsdata-23.7/tests/codegen/mappers/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/mappers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    29641 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/mappers/test_definitions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4098 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/mappers/test_dict.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15415 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/mappers/test_dtd.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12102 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/mappers/test_element.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17815 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/mappers/test_schema.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.185787 xsdata-23.7/tests/codegen/models/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/models/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5340 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/models/test_attr.py
+-rw-r--r--   0 runner    (1001) docker     (123)      679 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/models/test_attr_type.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7605 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/models/test_class.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4139 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/models/test_restrictions.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.185787 xsdata-23.7/tests/codegen/parsers/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/parsers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1312 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/parsers/test_definitions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6593 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/parsers/test_dtd.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16367 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/parsers/test_schema.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2214 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/test_analyzer.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6094 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/test_container.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8990 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/test_resolver.py
+-rw-r--r--   0 runner    (1001) docker     (123)    19370 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/test_transformer.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14142 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/test_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6791 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/test_validator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3109 2023-07-23 07:34:32.000000 xsdata-23.7/tests/codegen/test_writer.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1228 2023-07-23 07:34:32.000000 xsdata-23.7/tests/conftest.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.185787 xsdata-23.7/tests/fixtures/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.185787 xsdata-23.7/tests/fixtures/annotations/
+-rw-r--r--   0 runner    (1001) docker     (123)      188 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/annotations/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      592 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/annotations/model.py
+-rw-r--r--   0 runner    (1001) docker     (123)      580 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/annotations/model.xsd
+-rw-r--r--   0 runner    (1001) docker     (123)       70 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/annotations/sample.xml
+-rw-r--r--   0 runner    (1001) docker     (123)      189 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/annotations/units.py
+-rw-r--r--   0 runner    (1001) docker     (123)      660 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/annotations/units.xsd
+-rw-r--r--   0 runner    (1001) docker     (123)      950 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/annotations/xsdata.xml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.189787 xsdata-23.7/tests/fixtures/artists/
+-rw-r--r--   0 runner    (1001) docker     (123)      463 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/artists/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4517 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/artists/art001.xml
+-rw-r--r--   0 runner    (1001) docker     (123)     1214 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/artists/art002.xml
+-rw-r--r--   0 runner    (1001) docker     (123)     2629 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/artists/art003.xml
+-rw-r--r--   0 runner    (1001) docker     (123)     9186 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/artists/metadata.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.189787 xsdata-23.7/tests/fixtures/books/
+-rw-r--r--   0 runner    (1001) docker     (123)      144 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/books/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      272 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/books/bk001.xml
+-rw-r--r--   0 runner    (1001) docker     (123)      292 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/books/bk002.xml
+-rw-r--r--   0 runner    (1001) docker     (123)      194 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/books/books-xinclude.xml
+-rw-r--r--   0 runner    (1001) docker     (123)      485 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/books/books.json
+-rw-r--r--   0 runner    (1001) docker     (123)     2171 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/books/books.py
+-rw-r--r--   0 runner    (1001) docker     (123)      602 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/books/books.xml
+-rw-r--r--   0 runner    (1001) docker     (123)      602 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/books/books_auto_ns.xml
+-rw-r--r--   0 runner    (1001) docker     (123)      608 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/books/books_default_ns.xml
+-rw-r--r--   0 runner    (1001) docker     (123)     3842 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/books/fixtures.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2405 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/books/schema.xsd
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.189787 xsdata-23.7/tests/fixtures/calculator/
+-rw-r--r--   0 runner    (1001) docker     (123)      290 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/calculator/AddRQ.xml
+-rw-r--r--   0 runner    (1001) docker     (123)      399 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/calculator/AddRS.xml
+-rw-r--r--   0 runner    (1001) docker     (123)     1084 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/calculator/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13531 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/calculator/services.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7880 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/calculator/services.wsdl
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.189787 xsdata-23.7/tests/fixtures/compound/
+-rw-r--r--   0 runner    (1001) docker     (123)      132 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/compound/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      920 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/compound/models.py
+-rw-r--r--   0 runner    (1001) docker     (123)      260 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/compound/sample.json
+-rw-r--r--   0 runner    (1001) docker     (123)      182 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/compound/sample.xml
+-rw-r--r--   0 runner    (1001) docker     (123)      214 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/compound/sample.xsdata.xml
+-rw-r--r--   0 runner    (1001) docker     (123)      606 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/compound/schema.xsd
+-rw-r--r--   0 runner    (1001) docker     (123)      680 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/datatypes.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.189787 xsdata-23.7/tests/fixtures/docstrings/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/docstrings/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.189787 xsdata-23.7/tests/fixtures/docstrings/accessible/
+-rw-r--r--   0 runner    (1001) docker     (123)      287 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/docstrings/accessible/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2922 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/docstrings/accessible/schema.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.189787 xsdata-23.7/tests/fixtures/docstrings/blank/
+-rw-r--r--   0 runner    (1001) docker     (123)      282 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/docstrings/blank/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1492 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/docstrings/blank/schema.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.189787 xsdata-23.7/tests/fixtures/docstrings/google/
+-rw-r--r--   0 runner    (1001) docker     (123)      283 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/docstrings/google/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2856 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/docstrings/google/schema.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.189787 xsdata-23.7/tests/fixtures/docstrings/numpy/
+-rw-r--r--   0 runner    (1001) docker     (123)      282 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/docstrings/numpy/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2903 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/docstrings/numpy/schema.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.189787 xsdata-23.7/tests/fixtures/docstrings/rst/
+-rw-r--r--   0 runner    (1001) docker     (123)      280 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/docstrings/rst/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2786 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/docstrings/rst/schema.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4081 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/docstrings/schema.xsd
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.193787 xsdata-23.7/tests/fixtures/dtd/
+-rw-r--r--   0 runner    (1001) docker     (123)       15 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/dtd/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      400 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/dtd/complete_example.dtd
+-rw-r--r--   0 runner    (1001) docker     (123)      113 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/dtd/default_namespace.dtd
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.193787 xsdata-23.7/tests/fixtures/dtd/models/
+-rw-r--r--   0 runner    (1001) docker     (123)      174 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/dtd/models/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2120 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/dtd/models/complete_example.py
+-rw-r--r--   0 runner    (1001) docker     (123)      131 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/dtd/prefix_namespace.dtd
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.193787 xsdata-23.7/tests/fixtures/hello/
+-rw-r--r--   0 runner    (1001) docker     (123)      277 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/hello/HelloRQ.xml
+-rw-r--r--   0 runner    (1001) docker     (123)      275 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/hello/HelloRS.xml
+-rw-r--r--   0 runner    (1001) docker     (123)      489 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/hello/HelloRS_SoapFault.xml
+-rw-r--r--   0 runner    (1001) docker     (123)      430 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/hello/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4515 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/hello/hello.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3084 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/hello/hello.wsdl
+-rw-r--r--   0 runner    (1001) docker     (123)      781 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/hello/hello.xsd
+-rw-r--r--   0 runner    (1001) docker     (123)     4626 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/models.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.193787 xsdata-23.7/tests/fixtures/primer/
+-rw-r--r--   0 runner    (1001) docker     (123)      231 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/primer/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4594 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/primer/order.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3032 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/primer/order.xsd
+-rw-r--r--   0 runner    (1001) docker     (123)      840 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/primer/sample.json
+-rw-r--r--   0 runner    (1001) docker     (123)      881 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/primer/sample.xml
+-rw-r--r--   0 runner    (1001) docker     (123)      889 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/primer/sample.xsdata.xml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.193787 xsdata-23.7/tests/fixtures/series/
+-rw-r--r--   0 runner    (1001) docker     (123)      344 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/series/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.193787 xsdata-23.7/tests/fixtures/series/samples/
+-rw-r--r--   0 runner    (1001) docker     (123)     1263 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/series/samples/show1.json
+-rw-r--r--   0 runner    (1001) docker     (123)     1278 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/series/samples/show2.json
+-rw-r--r--   0 runner    (1001) docker     (123)     6626 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/series/series.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.193787 xsdata-23.7/tests/fixtures/stripe/
+-rw-r--r--   0 runner    (1001) docker     (123)      931 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/stripe/.xsdata.xml
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/stripe/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.193787 xsdata-23.7/tests/fixtures/stripe/models/
+-rw-r--r--   0 runner    (1001) docker     (123)      208 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/stripe/models/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3019 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/stripe/models/balance.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.193787 xsdata-23.7/tests/fixtures/stripe/samples/
+-rw-r--r--   0 runner    (1001) docker     (123)     2628 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/stripe/samples/balance.json
+-rw-r--r--   0 runner    (1001) docker     (123)      137 2023-07-23 07:34:32.000000 xsdata-23.7/tests/fixtures/submodels.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.193787 xsdata-23.7/tests/formats/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.197787 xsdata-23.7/tests/formats/dataclass/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.197787 xsdata-23.7/tests/formats/dataclass/models/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/models/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    18738 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/models/test_builders.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.197787 xsdata-23.7/tests/formats/dataclass/parsers/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/parsers/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.197787 xsdata-23.7/tests/formats/dataclass/parsers/handlers/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/parsers/handlers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2894 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/parsers/handlers/test_lxml.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3318 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/parsers/handlers/test_native.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.197787 xsdata-23.7/tests/formats/dataclass/parsers/nodes/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/parsers/nodes/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20127 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/parsers/nodes/test_element.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3263 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/parsers/nodes/test_primitive.py
+-rw-r--r--   0 runner    (1001) docker     (123)      377 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/parsers/nodes/test_skip.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1676 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/parsers/nodes/test_standard.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3986 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/parsers/nodes/test_union.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2229 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/parsers/nodes/test_wildcard.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2780 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/parsers/nodes/test_wrapper.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13688 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/parsers/test_json.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1260 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/parsers/test_mixins.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7766 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/parsers/test_node.py
+-rw-r--r--   0 runner    (1001) docker     (123)      981 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/parsers/test_tree.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3877 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/parsers/test_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2297 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/parsers/test_xml.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.197787 xsdata-23.7/tests/formats/dataclass/serializers/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/serializers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3392 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/serializers/test_code.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5884 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/serializers/test_json.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7162 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/serializers/test_mixins.py
+-rw-r--r--   0 runner    (1001) docker     (123)    24101 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/serializers/test_xml.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.197787 xsdata-23.7/tests/formats/dataclass/serializers/writers/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/serializers/writers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2746 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/serializers/writers/test_lxml.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2637 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/serializers/writers/test_native.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5152 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/test_client.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1195 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/test_compat.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5673 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/test_context.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9580 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/test_elements.py
+-rw-r--r--   0 runner    (1001) docker     (123)    40645 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/test_filters.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7450 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/test_generator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2699 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/test_transport.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6643 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/dataclass/test_typing.py
+-rw-r--r--   0 runner    (1001) docker     (123)    15817 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/test_converter.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2821 2023-07-23 07:34:32.000000 xsdata-23.7/tests/formats/test_mixins.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.201787 xsdata-23.7/tests/integration/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/tests/integration/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.201787 xsdata-23.7/tests/integration/benchmarks/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/tests/integration/benchmarks/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      301 2023-07-23 07:34:32.000000 xsdata-23.7/tests/integration/benchmarks/conftest.py
+-rw-r--r--   0 runner    (1001) docker     (123)      876 2023-07-23 07:34:32.000000 xsdata-23.7/tests/integration/benchmarks/test_converters.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1331 2023-07-23 07:34:32.000000 xsdata-23.7/tests/integration/benchmarks/test_handlers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2023 2023-07-23 07:34:32.000000 xsdata-23.7/tests/integration/benchmarks/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1091 2023-07-23 07:34:32.000000 xsdata-23.7/tests/integration/test_annotations.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1166 2023-07-23 07:34:32.000000 xsdata-23.7/tests/integration/test_artists.py
+-rw-r--r--   0 runner    (1001) docker     (123)      778 2023-07-23 07:34:32.000000 xsdata-23.7/tests/integration/test_books.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1991 2023-07-23 07:34:32.000000 xsdata-23.7/tests/integration/test_calculator.py
+-rw-r--r--   0 runner    (1001) docker     (123)      655 2023-07-23 07:34:32.000000 xsdata-23.7/tests/integration/test_compound.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1880 2023-07-23 07:34:32.000000 xsdata-23.7/tests/integration/test_docstrings.py
+-rw-r--r--   0 runner    (1001) docker     (123)      578 2023-07-23 07:34:32.000000 xsdata-23.7/tests/integration/test_dtd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3781 2023-07-23 07:34:32.000000 xsdata-23.7/tests/integration/test_hello_rpc.py
+-rw-r--r--   0 runner    (1001) docker     (123)      690 2023-07-23 07:34:32.000000 xsdata-23.7/tests/integration/test_primer.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1279 2023-07-23 07:34:32.000000 xsdata-23.7/tests/integration/test_series.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1318 2023-07-23 07:34:32.000000 xsdata-23.7/tests/integration/test_stripe.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.201787 xsdata-23.7/tests/models/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.201787 xsdata-23.7/tests/models/enums/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/enums/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2956 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/enums/test_datatype.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11825 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/test_config.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21919 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/test_datatype.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6013 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/test_mixins.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1223 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/test_type_mapping.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.201787 xsdata-23.7/tests/models/typemapping/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/typemapping/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      337 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/typemapping/city.py
+-rw-r--r--   0 runner    (1001) docker     (123)      294 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/typemapping/house.py
+-rw-r--r--   0 runner    (1001) docker     (123)      448 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/typemapping/street.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.201787 xsdata-23.7/tests/models/wsdl/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/wsdl/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      700 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/wsdl/test_binding.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3104 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/wsdl/test_definitions.py
+-rw-r--r--   0 runner    (1001) docker     (123)      569 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/wsdl/test_port_type.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.205787 xsdata-23.7/tests/models/xsd/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/xsd/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      259 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/xsd/test_all.py
+-rw-r--r--   0 runner    (1001) docker     (123)      722 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/xsd/test_alternative.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1410 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/xsd/test_annotation_base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1381 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/xsd/test_any.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1411 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/xsd/test_any_attribute.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2585 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/xsd/test_attribute.py
+-rw-r--r--   0 runner    (1001) docker     (123)      432 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/xsd/test_attribute_group.py
+-rw-r--r--   0 runner    (1001) docker     (123)      440 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/xsd/test_choice.py
+-rw-r--r--   0 runner    (1001) docker     (123)      303 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/xsd/test_complex_content.py
+-rw-r--r--   0 runner    (1001) docker     (123)      533 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/xsd/test_complex_type.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3420 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/xsd/test_element.py
+-rw-r--r--   0 runner    (1001) docker     (123)      691 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/xsd/test_enumeration.py
+-rw-r--r--   0 runner    (1001) docker     (123)      292 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/xsd/test_extension.py
+-rw-r--r--   0 runner    (1001) docker     (123)      565 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/xsd/test_group.py
+-rw-r--r--   0 runner    (1001) docker     (123)      607 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/xsd/test_list.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3119 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/xsd/test_restriction.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1442 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/xsd/test_schema.py
+-rw-r--r--   0 runner    (1001) docker     (123)      462 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/xsd/test_sequence.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1864 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/xsd/test_simple_type.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1960 2023-07-23 07:34:32.000000 xsdata-23.7/tests/models/xsd/test_union.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7468 2023-07-23 07:34:32.000000 xsdata-23.7/tests/test_cli.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.205787 xsdata-23.7/tests/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/tests/utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1899 2023-07-23 07:34:32.000000 xsdata-23.7/tests/utils/test_collections.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4611 2023-07-23 07:34:32.000000 xsdata-23.7/tests/utils/test_dates.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5495 2023-07-23 07:34:32.000000 xsdata-23.7/tests/utils/test_downloader.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1244 2023-07-23 07:34:32.000000 xsdata-23.7/tests/utils/test_hooks.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5503 2023-07-23 07:34:32.000000 xsdata-23.7/tests/utils/test_namespaces.py
+-rw-r--r--   0 runner    (1001) docker     (123)      428 2023-07-23 07:34:32.000000 xsdata-23.7/tests/utils/test_objects.py
+-rw-r--r--   0 runner    (1001) docker     (123)      508 2023-07-23 07:34:32.000000 xsdata-23.7/tests/utils/test_testing.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8010 2023-07-23 07:34:32.000000 xsdata-23.7/tests/utils/test_text.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.205787 xsdata-23.7/xsdata/
+-rw-r--r--   0 runner    (1001) docker     (123)       21 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      236 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/__main__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5143 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/cli.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.209787 xsdata-23.7/xsdata/codegen/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1638 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/analyzer.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6074 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/container.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.209787 xsdata-23.7/xsdata/codegen/handlers/
+-rw-r--r--   0 runner    (1001) docker     (123)     1880 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/handlers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3479 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/handlers/add_attribute_substitutions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1490 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/handlers/calculate_attribute_paths.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5594 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/handlers/create_compound_fields.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6186 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/handlers/designate_class_packages.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1818 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/handlers/filter_classes.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1558 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/handlers/flatten_attribute_groups.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11284 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/handlers/flatten_class_extensions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2035 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/handlers/merge_attributes.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9866 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/handlers/process_attributes_types.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1612 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/handlers/process_mixed_content_class.py
+-rw-r--r--   0 runner    (1001) docker     (123)      996 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/handlers/rename_duplicate_attributes.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4651 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/handlers/rename_duplicate_classes.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1100 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/handlers/reset_attribute_sequence_numbers.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1256 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/handlers/reset_attribute_sequences.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6470 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/handlers/sanitize_attributes_default_value.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1785 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/handlers/sanitize_enumeration_class.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1817 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/handlers/unnest_inner_classes.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3832 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/handlers/update_attributes_effective_choice.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2786 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/handlers/vacuum_inner_classes.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2862 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/handlers/validate_attributes_overrides.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.209787 xsdata-23.7/xsdata/codegen/mappers/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/mappers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14459 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/mappers/definitions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1782 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/mappers/dict.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7884 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/mappers/dtd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6501 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/mappers/element.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10096 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/mappers/schema.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2890 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/mixins.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20155 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/models.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.209787 xsdata-23.7/xsdata/codegen/parsers/
+-rw-r--r--   0 runner    (1001) docker     (123)      169 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/parsers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1074 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/parsers/definitions.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2868 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/parsers/dtd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9826 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/parsers/schema.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4882 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/resolver.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11953 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/transformer.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11309 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5281 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/validator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2332 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/codegen/writer.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1352 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/exceptions.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.213787 xsdata-23.7/xsdata/formats/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1187 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/bindings.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16156 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/converter.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.213787 xsdata-23.7/xsdata/formats/dataclass/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4535 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/client.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4082 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/compat.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8947 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/context.py
+-rw-r--r--   0 runner    (1001) docker     (123)    29499 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/filters.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5236 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/generator.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.213787 xsdata-23.7/xsdata/formats/dataclass/models/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/models/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17822 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/models/builders.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13241 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/models/elements.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1364 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/models/generics.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.213787 xsdata-23.7/xsdata/formats/dataclass/parsers/
+-rw-r--r--   0 runner    (1001) docker     (123)      314 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/parsers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7257 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/parsers/bases.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1892 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/parsers/config.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.213787 xsdata-23.7/xsdata/formats/dataclass/parsers/handlers/
+-rw-r--r--   0 runner    (1001) docker     (123)      537 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/parsers/handlers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2782 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/parsers/handlers/lxml.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4217 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/parsers/handlers/native.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11828 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/parsers/json.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5621 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/parsers/mixins.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.213787 xsdata-23.7/xsdata/formats/dataclass/parsers/nodes/
+-rw-r--r--   0 runner    (1001) docker     (123)      642 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/parsers/nodes/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    14972 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/parsers/nodes/element.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1820 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/parsers/nodes/primitive.py
+-rw-r--r--   0 runner    (1001) docker     (123)      649 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/parsers/nodes/skip.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1771 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/parsers/nodes/standard.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4274 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/parsers/nodes/union.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2545 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/parsers/nodes/wildcard.py
+-rw-r--r--   0 runner    (1001) docker     (123)      736 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/parsers/nodes/wrapper.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2133 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/parsers/tree.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3044 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/parsers/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2984 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/parsers/xml.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.217787 xsdata-23.7/xsdata/formats/dataclass/serializers/
+-rw-r--r--   0 runner    (1001) docker     (123)      374 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/serializers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4560 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/serializers/code.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1996 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/serializers/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3480 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/serializers/json.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9629 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/serializers/mixins.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.217787 xsdata-23.7/xsdata/formats/dataclass/serializers/writers/
+-rw-r--r--   0 runner    (1001) docker     (123)      520 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/serializers/writers/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1673 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/serializers/writers/lxml.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2280 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/serializers/writers/native.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16192 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/serializers/xml.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.217787 xsdata-23.7/xsdata/formats/dataclass/templates/
+-rw-r--r--   0 runner    (1001) docker     (123)     2322 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/templates/class.jinja2
+-rw-r--r--   0 runner    (1001) docker     (123)       52 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/templates/docstrings.accessible.jinja2
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/templates/docstrings.blank.jinja2
+-rw-r--r--   0 runner    (1001) docker     (123)      291 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/templates/docstrings.google.jinja2
+-rw-r--r--   0 runner    (1001) docker     (123)      402 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/templates/docstrings.numpy.jinja2
+-rw-r--r--   0 runner    (1001) docker     (123)      360 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/templates/docstrings.rst.jinja2
+-rw-r--r--   0 runner    (1001) docker     (123)      781 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/templates/enum.jinja2
+-rw-r--r--   0 runner    (1001) docker     (123)      376 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/templates/imports.jinja2
+-rw-r--r--   0 runner    (1001) docker     (123)      141 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/templates/module.jinja2
+-rw-r--r--   0 runner    (1001) docker     (123)      298 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/templates/package.jinja2
+-rw-r--r--   0 runner    (1001) docker     (123)      146 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/templates/service.jinja2
+-rw-r--r--   0 runner    (1001) docker     (123)     1778 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/transports.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4319 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/dataclass/typing.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3317 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/formats/mixins.py
+-rw-r--r--   0 runner    (1001) docker     (123)       53 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/logger.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.217787 xsdata-23.7/xsdata/models/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/models/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    21294 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/models/config.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20286 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/models/datatype.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1828 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/models/dtd.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9818 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/models/enums.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7886 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/models/mixins.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5817 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/models/wsdl.py
+-rw-r--r--   0 runner    (1001) docker     (123)    36973 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/models/xsd.py
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/py.typed
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.221787 xsdata-23.7/xsdata/schemas/
+-rw-r--r--   0 runner    (1001) docker     (123)     4067 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/schemas/mathml3-common.xsd
+-rw-r--r--   0 runner    (1001) docker     (123)    28457 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/schemas/mathml3-content.xsd
+-rw-r--r--   0 runner    (1001) docker     (123)    84129 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/schemas/mathml3-presentation.xsd
+-rw-r--r--   0 runner    (1001) docker     (123)     6846 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/schemas/mathml3-strict-content.xsd
+-rw-r--r--   0 runner    (1001) docker     (123)      436 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/schemas/mathml3.xsd
+-rw-r--r--   0 runner    (1001) docker     (123)     8051 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/schemas/xlink.xsd
+-rw-r--r--   0 runner    (1001) docker     (123)     1206 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/schemas/xml.xsd
+-rw-r--r--   0 runner    (1001) docker     (123)      347 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/schemas/xsi.xsd
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.221787 xsdata-23.7/xsdata/utils/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4204 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/utils/click.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3036 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/utils/collections.py
+-rw-r--r--   0 runner    (1001) docker     (123)      489 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/utils/constants.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6709 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/utils/dates.py
+-rw-r--r--   0 runner    (1001) docker     (123)      741 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/utils/debug.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4782 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/utils/downloader.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1208 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/utils/graphs.py
+-rw-r--r--   0 runner    (1001) docker     (123)      453 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/utils/hooks.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5041 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/utils/namespaces.py
+-rw-r--r--   0 runner    (1001) docker     (123)      812 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/utils/objects.py
+-rw-r--r--   0 runner    (1001) docker     (123)      694 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/utils/package.py
+-rw-r--r--   0 runner    (1001) docker     (123)    17285 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/utils/testing.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4961 2023-07-23 07:34:32.000000 xsdata-23.7/xsdata/utils/text.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 07:34:44.205787 xsdata-23.7/xsdata.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     5197 2023-07-23 07:34:44.000000 xsdata-23.7/xsdata.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)    15635 2023-07-23 07:34:44.000000 xsdata-23.7/xsdata.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 07:34:44.000000 xsdata-23.7/xsdata.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       48 2023-07-23 07:34:44.000000 xsdata-23.7/xsdata.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      344 2023-07-23 07:34:44.000000 xsdata-23.7/xsdata.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        7 2023-07-23 07:34:44.000000 xsdata-23.7/xsdata.egg-info/top_level.txt
```

### Comparing `xsdata-23.6/CHANGES.rst` & `xsdata-23.7/CHANGES.rst`

 * *Files 1% similar despite different names*

```diff
@@ -1,7 +1,16 @@
+23.7 (2023-07-23)
+-----------------
+- Fixed decimal converter to avoid scientific notations (`#826 <https://github.com/tefra/xsdata/pull/826>`_)
+- Fixed nympy paramater docstring format  (`#827 <https://github.com/tefra/xsdata/pull/827>`_)
+- Fixed optional/required override validation (`#820 <https://github.com/tefra/xsdata/pull/820>`_)
+- Fixed WSDL mapper to respect the elements original location (`#832 <https://github.com/tefra/xsdata/pull/832>`_)
+- Added Python 3.12 support
+
+
 23.6 (2023-06-24)
 -----------------
 - Fixed conflicting enum values leading to wrong default values (`#806 <https://github.com/tefra/xsdata/pull/806>`_)
 - Added support for custom decorators and base classes (`#793 <https://github.com/tefra/xsdata/pull/793>`_)
 - Added parser config to load external dtd to resolve entities (`#797 <https://github.com/tefra/xsdata/pull/797>`_)
 - Added requests sessions on the wsdl client transport (`#798 <https://github.com/tefra/xsdata/pull/798>`_)
 - Added support subscriptable types and UnionType (`#801 <https://github.com/tefra/xsdata/pull/801>`_)
```

### Comparing `xsdata-23.6/LICENSE` & `xsdata-23.7/LICENSE`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/PKG-INFO` & `xsdata-23.7/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: xsdata
-Version: 23.6
+Version: 23.7
 Summary: Python XML Binding
 Author-email: Christodoulos Tsoulloftas <chris@komposta.net>
 License: MIT
 Project-URL: Homepage, https://github.com/tefra/xsdata
 Project-URL: Source, https://github.com/tefra/xsdata
 Project-URL: Documentation, https://xsdata.readthedocs.io/
 Project-URL: Changelog, https://xsdata.readthedocs.io/en/latest/changelog.html
@@ -30,27 +30,27 @@
 Provides-Extra: cli
 Provides-Extra: docs
 Provides-Extra: lxml
 Provides-Extra: soap
 Provides-Extra: test
 License-File: LICENSE
 
-.. image:: https://github.com/tefra/xsdata/raw/master/docs/_static/logo.svg
+.. image:: https://github.com/tefra/xsdata/raw/main/docs/_static/logo.svg
     :target: https://xsdata.readthedocs.io/
 
 Naive XML Bindings for python
 =============================
 
 .. image:: https://github.com/tefra/xsdata/workflows/tests/badge.svg
     :target: https://github.com/tefra/xsdata/actions
 
 .. image:: https://readthedocs.org/projects/xsdata/badge
     :target: https://xsdata.readthedocs.io/
 
-.. image:: https://codecov.io/gh/tefra/xsdata/branch/master/graph/badge.svg
+.. image:: https://codecov.io/gh/tefra/xsdata/branch/main/graph/badge.svg
     :target: https://codecov.io/gh/tefra/xsdata
 
 .. image:: https://img.shields.io/github/languages/top/tefra/xsdata.svg
     :target: https://xsdata.readthedocs.io/
 
 .. image:: https://www.codefactor.io/repository/github/tefra/xsdata/badge
    :target: https://www.codefactor.io/repository/github/tefra/xsdata
@@ -131,18 +131,14 @@
   - Handlers and Writers based on lxml and native xml python
   - Support wildcard elements and attributes
   - Support xinclude statements and unknown properties
   - Customize behaviour through config
 
 
 
-Changelog: 23.6 (2023-06-24)
+Changelog: 23.7 (2023-07-23)
 ----------------------------
-- Fixed conflicting enum values leading to wrong default values (`#806 <https://github.com/tefra/xsdata/pull/806>`_)
-- Added support for custom decorators and base classes (`#793 <https://github.com/tefra/xsdata/pull/793>`_)
-- Added parser config to load external dtd to resolve entities (`#797 <https://github.com/tefra/xsdata/pull/797>`_)
-- Added requests sessions on the wsdl client transport (`#798 <https://github.com/tefra/xsdata/pull/798>`_)
-- Added support subscriptable types and UnionType (`#801 <https://github.com/tefra/xsdata/pull/801>`_)
-- Added option to restrict models package for auto-locator (`#809 <https://github.com/tefra/xsdata/pull/809>`_)
-- Updated context to only cache supported classes (`#796 <https://github.com/tefra/xsdata/pull/796>`_)
-- Removed tox requirement (`#800 <https://github.com/tefra/xsdata/pull/800>`_)
-- Converted to pyproject.toml (`#802 <https://github.com/tefra/xsdata/pull/802>`_)
+- Fixed decimal converter to avoid scientific notations (`#826 <https://github.com/tefra/xsdata/pull/826>`_)
+- Fixed nympy paramater docstring format  (`#827 <https://github.com/tefra/xsdata/pull/827>`_)
+- Fixed optional/required override validation (`#820 <https://github.com/tefra/xsdata/pull/820>`_)
+- Fixed WSDL mapper to respect the elements original location (`#832 <https://github.com/tefra/xsdata/pull/832>`_)
+- Added Python 3.12 support
```

### Comparing `xsdata-23.6/README.rst` & `xsdata-23.7/README.rst`

 * *Files 7% similar despite different names*

```diff
@@ -1,20 +1,20 @@
-.. image:: https://github.com/tefra/xsdata/raw/master/docs/_static/logo.svg
+.. image:: https://github.com/tefra/xsdata/raw/main/docs/_static/logo.svg
     :target: https://xsdata.readthedocs.io/
 
 Naive XML Bindings for python
 =============================
 
 .. image:: https://github.com/tefra/xsdata/workflows/tests/badge.svg
     :target: https://github.com/tefra/xsdata/actions
 
 .. image:: https://readthedocs.org/projects/xsdata/badge
     :target: https://xsdata.readthedocs.io/
 
-.. image:: https://codecov.io/gh/tefra/xsdata/branch/master/graph/badge.svg
+.. image:: https://codecov.io/gh/tefra/xsdata/branch/main/graph/badge.svg
     :target: https://codecov.io/gh/tefra/xsdata
 
 .. image:: https://img.shields.io/github/languages/top/tefra/xsdata.svg
     :target: https://xsdata.readthedocs.io/
 
 .. image:: https://www.codefactor.io/repository/github/tefra/xsdata/badge
    :target: https://www.codefactor.io/repository/github/tefra/xsdata
@@ -95,18 +95,14 @@
   - Handlers and Writers based on lxml and native xml python
   - Support wildcard elements and attributes
   - Support xinclude statements and unknown properties
   - Customize behaviour through config
 
 
 
-Changelog: 23.6 (2023-06-24)
+Changelog: 23.7 (2023-07-23)
 ----------------------------
-- Fixed conflicting enum values leading to wrong default values (`#806 <https://github.com/tefra/xsdata/pull/806>`_)
-- Added support for custom decorators and base classes (`#793 <https://github.com/tefra/xsdata/pull/793>`_)
-- Added parser config to load external dtd to resolve entities (`#797 <https://github.com/tefra/xsdata/pull/797>`_)
-- Added requests sessions on the wsdl client transport (`#798 <https://github.com/tefra/xsdata/pull/798>`_)
-- Added support subscriptable types and UnionType (`#801 <https://github.com/tefra/xsdata/pull/801>`_)
-- Added option to restrict models package for auto-locator (`#809 <https://github.com/tefra/xsdata/pull/809>`_)
-- Updated context to only cache supported classes (`#796 <https://github.com/tefra/xsdata/pull/796>`_)
-- Removed tox requirement (`#800 <https://github.com/tefra/xsdata/pull/800>`_)
-- Converted to pyproject.toml (`#802 <https://github.com/tefra/xsdata/pull/802>`_)
+- Fixed decimal converter to avoid scientific notations (`#826 <https://github.com/tefra/xsdata/pull/826>`_)
+- Fixed nympy paramater docstring format  (`#827 <https://github.com/tefra/xsdata/pull/827>`_)
+- Fixed optional/required override validation (`#820 <https://github.com/tefra/xsdata/pull/820>`_)
+- Fixed WSDL mapper to respect the elements original location (`#832 <https://github.com/tefra/xsdata/pull/832>`_)
+- Added Python 3.12 support
```

### Comparing `xsdata-23.6/docs/Makefile` & `xsdata-23.7/docs/Makefile`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/_ext/xsdatadocs.py` & `xsdata-23.7/docs/_ext/xsdatadocs.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/_static/logo-dark.svg` & `xsdata-23.7/docs/_static/logo-dark.svg`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/_static/logo.svg` & `xsdata-23.7/docs/_static/logo.svg`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/api/codegen.rst` & `xsdata-23.7/docs/api/codegen.rst`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/api/xml-handlers.rst` & `xsdata-23.7/docs/api/xml-handlers.rst`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/api/xml-writers.rst` & `xsdata-23.7/docs/api/xml-writers.rst`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/codegen.rst` & `xsdata-23.7/docs/codegen.rst`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/conf.py` & `xsdata-23.7/docs/conf.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/data-types-table.rst` & `xsdata-23.7/docs/data-types-table.rst`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/data-types.rst` & `xsdata-23.7/docs/data-types.rst`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/examples/compound-fields.rst` & `xsdata-23.7/docs/examples/compound-fields.rst`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/examples/custom-class-factory.rst` & `xsdata-23.7/docs/examples/custom-class-factory.rst`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/examples/custom-property-names.rst` & `xsdata-23.7/docs/examples/custom-property-names.rst`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/examples/custom-type-mapping.rst` & `xsdata-23.7/docs/examples/custom-type-mapping.rst`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/examples/dataclasses-features.rst` & `xsdata-23.7/docs/examples/dataclasses-features.rst`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/examples/docstrings.rst` & `xsdata-23.7/docs/examples/docstrings.rst`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/examples/extending-models.rst` & `xsdata-23.7/docs/examples/extending-models.rst`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/examples/json-modeling.rst` & `xsdata-23.7/docs/examples/json-modeling.rst`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/examples/pycode-serializer.rst` & `xsdata-23.7/docs/examples/pycode-serializer.rst`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/examples/w3c-suite.rst` & `xsdata-23.7/docs/examples/w3c-suite.rst`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/examples/working-with-wildcards.rst` & `xsdata-23.7/docs/examples/working-with-wildcards.rst`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/examples/wrapped-list.rst` & `xsdata-23.7/docs/examples/wrapped-list.rst`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/examples/xml-modeling.rst` & `xsdata-23.7/docs/examples/xml-modeling.rst`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/examples.rst` & `xsdata-23.7/docs/examples.rst`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/faq/why-are-elements-out-of-order.rst` & `xsdata-23.7/docs/faq/why-are-elements-out-of-order.rst`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/faq/why-i-get-a-typeerror-requires-a-single-type.rst` & `xsdata-23.7/docs/faq/why-i-get-a-typeerror-requires-a-single-type.rst`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/faq/why-non-nullable-fields-are-marked-as-optional.rst` & `xsdata-23.7/docs/faq/why-non-nullable-fields-are-marked-as-optional.rst`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/index.rst` & `xsdata-23.7/docs/index.rst`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/installation.rst` & `xsdata-23.7/docs/installation.rst`

 * *Files 12% similar despite different names*

```diff
@@ -18,15 +18,15 @@
        the builtin python xml implementations.
 
 xsdata has a monthly release cycle, in order to use the latest updates you can also
 install directly from the git repo.
 
 .. code-block:: console
 
-    $ pip install git+https://github.com/tefra/xsdata@master#egg=xsdata[cli,lxml]
+    $ pip install xsdata[cli,lxml] @ git+https://github.com/tefra/xsdata
 
 
 Install using conda
 -------------------
 
 .. code-block:: console
```

### Comparing `xsdata-23.6/docs/json.rst` & `xsdata-23.7/docs/json.rst`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/make.bat` & `xsdata-23.7/docs/make.bat`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/models.rst` & `xsdata-23.7/docs/models.rst`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/scripts/generate_data_types.py` & `xsdata-23.7/docs/scripts/generate_data_types.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/wsdl.rst` & `xsdata-23.7/docs/wsdl.rst`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/docs/xml.rst` & `xsdata-23.7/docs/xml.rst`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/pyproject.toml` & `xsdata-23.7/pyproject.toml`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/handlers/test_add_attribute_substitutions.py` & `xsdata-23.7/tests/codegen/handlers/test_add_attribute_substitutions.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/handlers/test_calculate_attribute_paths.py` & `xsdata-23.7/tests/codegen/handlers/test_calculate_attribute_paths.py`

 * *Files 2% similar despite different names*

```diff
@@ -65,14 +65,21 @@
                     )
                 ),
                 AttrFactory.element(
                     restrictions=Restrictions(
                         min_occurs=1,
                         max_occurs=1,
                         path=[("s", 1, 1, 1), ("c", 5, 2, 2)],
+                    ),
+                ),
+                AttrFactory.element(
+                    restrictions=Restrictions(
+                        min_occurs=1,
+                        max_occurs=1,
+                        path=[("s", 1, 1, 1), ("c", 6, 1, 21)],
                     )
                 ),
             ]
         )
         self.processor.process(target)
 
         actual = []
@@ -95,9 +102,10 @@
             (1, None, 1, 1),
             (1, 4, 1, 2),
             (1, 3, 1, 1),
             (1, None, 0, 1),
             (1, None, 0, 1),
             (1, None, 2, 2),
             (1, None, 2, 2),
+            (1, None, 1, 21),
         ]
         self.assertEqual(expected, actual)
```

### Comparing `xsdata-23.6/tests/codegen/handlers/test_designate_class_packages.py` & `xsdata-23.7/tests/codegen/handlers/test_designate_class_packages.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/handlers/test_filter_classes.py` & `xsdata-23.7/tests/codegen/handlers/test_filter_classes.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/handlers/test_flatten_attribute_groups.py` & `xsdata-23.7/tests/codegen/handlers/test_flatten_attribute_groups.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/handlers/test_flatten_class_extensions.py` & `xsdata-23.7/tests/codegen/handlers/test_flatten_class_extensions.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/handlers/test_merge_attributes.py` & `xsdata-23.7/tests/codegen/handlers/test_merge_attributes.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/handlers/test_process_attributes_types.py` & `xsdata-23.7/tests/codegen/handlers/test_process_attributes_types.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/handlers/test_process_mixed_content_class.py` & `xsdata-23.7/tests/codegen/handlers/test_process_mixed_content_class.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/handlers/test_rename_duplicate_attributes.py` & `xsdata-23.7/tests/codegen/handlers/test_rename_duplicate_attributes.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/handlers/test_rename_duplicate_classes.py` & `xsdata-23.7/tests/codegen/handlers/test_rename_duplicate_classes.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/handlers/test_reset_attribute_sequence_numbers.py` & `xsdata-23.7/tests/codegen/handlers/test_reset_attribute_sequence_numbers.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/handlers/test_reset_attribute_sequences.py` & `xsdata-23.7/tests/codegen/handlers/test_reset_attribute_sequences.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/handlers/test_sanitize_attributes_default_value.py` & `xsdata-23.7/tests/codegen/handlers/test_sanitize_attributes_default_value.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/handlers/test_sanitize_enumeration_class.py` & `xsdata-23.7/tests/codegen/handlers/test_sanitize_enumeration_class.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/handlers/test_unnest_inner_classes.py` & `xsdata-23.7/tests/codegen/handlers/test_unnest_inner_classes.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/handlers/test_update_attributes_effective_choice.py` & `xsdata-23.7/tests/codegen/handlers/test_update_attributes_effective_choice.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/handlers/test_vacuum_inner_classes.py` & `xsdata-23.7/tests/codegen/handlers/test_vacuum_inner_classes.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/handlers/test_validate_attributes_overrides.py` & `xsdata-23.7/tests/codegen/handlers/test_validate_attributes_overrides.py`

 * *Files 14% similar despite different names*

```diff
@@ -98,20 +98,27 @@
         self.processor.validate_override(target, attr_a, attr_b)
         self.assertEqual(1, len(target.attrs))
 
         # Restrictions don't match
         attr_b.fixed = attr_a.fixed
         attr_a.restrictions.tokens = not attr_b.restrictions.tokens
         attr_a.restrictions.nillable = not attr_b.restrictions.nillable
+        attr_a.restrictions.min_occurs = 0
+        attr_b.restrictions.min_occurs = 1
+        attr_a.restrictions.max_occurs = 0
+        attr_b.restrictions.max_occurs = 1
+
         self.processor.validate_override(target, attr_a, attr_b)
         self.assertEqual(1, len(target.attrs))
 
         # Restrictions are compatible again
         attr_a.restrictions.tokens = attr_b.restrictions.tokens
         attr_a.restrictions.nillable = attr_b.restrictions.nillable
+        attr_a.restrictions.min_occurs = attr_b.restrictions.min_occurs = 1
+        attr_a.restrictions.max_occurs = attr_b.restrictions.max_occurs = 1
         self.processor.validate_override(target, attr_a, attr_b)
         self.assertEqual(0, len(target.attrs))
 
         # Source is list, parent is not
         target.attrs.append(attr_a)
         attr_a.restrictions.min_occurs = None
         attr_a.restrictions.max_occurs = 10
```

### Comparing `xsdata-23.6/tests/codegen/mappers/test_definitions.py` & `xsdata-23.7/tests/codegen/mappers/test_definitions.py`

 * *Files 0% similar despite different names*

```diff
@@ -154,16 +154,16 @@
         )
 
     @mock.patch.object(DefinitionsMapper, "map_binding_operation_messages")
     @mock.patch.object(DefinitionsMapper, "operation_namespace")
     def test_map_binding_operation(
         self, mock_operation_namespace, mock_map_binding_operation_messages
     ):
-        definitions = Definitions(location="foo.wsdl", target_namespace="xsdata")
-        operation = BindingOperation(name="Add")
+        definitions = Definitions(target_namespace="xsdata")
+        operation = BindingOperation(name="Add", location="foo.wsdl")
         operation.ns_map["foo"] = "bar"
         port_operation = PortTypeOperation()
         config = {"a": "one", "b": "two", "style": "rpc"}
         name = "Calc"
         namespace = "SomeNS"
         first = ClassFactory.create(qname="some_name_first", meta_name="Envelope")
         second = ClassFactory.create(qname="some_name_second", meta_name="Envelope")
@@ -329,22 +329,25 @@
     ):
         mock_get_or_create_inner_class.side_effect = mock_create_inner
         mock_map_binding_message_parts.side_effect = mock_create_attr
 
         name = "some_operation_bindings"
         style = "document"
         namespace = "xsdata"
-        definitions = Definitions(location="foo.wsdl", target_namespace="bar")
-        port_type_message = PortTypeMessage(message="some_operation")
+        definitions = Definitions(target_namespace="bar")
+        port_type_message = PortTypeMessage(
+            message="some_operation", location="foo.wsdl"
+        )
         binding_message = BindingMessage(
             extended=[
                 AnyElement(qname="body"),
                 AnyElement(qname="header"),
                 AnyElement(qname="header"),
-            ]
+            ],
+            location="foo.wsdl",
         )
         binding_message.ns_map["foo"] = "bar"
 
         result = DefinitionsMapper.build_envelope_class(
             definitions,
             binding_message,
             port_type_message,
@@ -411,22 +414,25 @@
         mock_get_or_create_inner_class.side_effect = mock_create_inner
         mock_map_binding_message_parts.side_effect = mock_create_attr
         mock_map_port_type_message.side_effect = mock_create_attr
 
         name = "some_operation_bindings"
         style = "rpc"
         namespace = "xsdata"
-        definitions = Definitions(location="foo.wsdl", target_namespace="bar")
-        port_type_message = PortTypeMessage(message="some_operation")
+        definitions = Definitions(target_namespace="bar")
+        port_type_message = PortTypeMessage(
+            message="some_operation", location="foo.wsdl"
+        )
         binding_message = BindingMessage(
             extended=[
                 AnyElement(qname="body", attributes={"namespace": "bodyns"}),
                 AnyElement(qname="header"),
                 AnyElement(qname="header"),
-            ]
+            ],
+            location="foo.wsdl",
         )
         binding_message.ns_map["foo"] = "bar"
 
         result = DefinitionsMapper.build_envelope_class(
             definitions,
             binding_message,
             port_type_message,
@@ -701,18 +707,16 @@
         self.assertEqual(expected, list(result))
         mock_warning.assert_called_once_with("Skip untyped message part %s", "arg2")
 
     @mock.patch.object(DefinitionsMapper, "build_parts_attributes")
     def test_build_message_class(self, mock_create_message_attributes):
         message = Message(name="bar", parts=[Part()])
         message.ns_map["foo"] = "bar"
-        definitions = Definitions(
-            messages=[message], target_namespace="xsdata", location="foo.wsdl"
-        )
-        port_type_message = PortTypeMessage(message="foo:bar")
+        definitions = Definitions(messages=[message], target_namespace="xsdata")
+        port_type_message = PortTypeMessage(message="foo:bar", location="foo.wsdl")
 
         attrs = AttrFactory.list(2)
         mock_create_message_attributes.return_value = attrs
         actual = DefinitionsMapper.build_message_class(definitions, port_type_message)
         expected = Class(
             qname=build_qname("bar", "bar"),
             status=Status.RAW,
```

### Comparing `xsdata-23.6/tests/codegen/mappers/test_dict.py` & `xsdata-23.7/tests/codegen/mappers/test_dict.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/mappers/test_dtd.py` & `xsdata-23.7/tests/codegen/mappers/test_dtd.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/mappers/test_element.py` & `xsdata-23.7/tests/codegen/mappers/test_element.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/mappers/test_schema.py` & `xsdata-23.7/tests/codegen/mappers/test_schema.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/models/test_attr.py` & `xsdata-23.7/tests/codegen/models/test_attr.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/models/test_attr_type.py` & `xsdata-23.7/tests/codegen/models/test_attr_type.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/models/test_class.py` & `xsdata-23.7/tests/codegen/models/test_class.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/models/test_restrictions.py` & `xsdata-23.7/tests/codegen/models/test_restrictions.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/parsers/test_dtd.py` & `xsdata-23.7/tests/codegen/parsers/test_dtd.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/parsers/test_schema.py` & `xsdata-23.7/tests/codegen/parsers/test_schema.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/test_analyzer.py` & `xsdata-23.7/tests/codegen/test_analyzer.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/test_container.py` & `xsdata-23.7/tests/codegen/test_container.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/test_resolver.py` & `xsdata-23.7/tests/codegen/test_resolver.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/test_transformer.py` & `xsdata-23.7/tests/codegen/test_transformer.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/test_utils.py` & `xsdata-23.7/tests/codegen/test_utils.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/test_validator.py` & `xsdata-23.7/tests/codegen/test_validator.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/codegen/test_writer.py` & `xsdata-23.7/tests/codegen/test_writer.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/conftest.py` & `xsdata-23.7/tests/conftest.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/annotations/model.py` & `xsdata-23.7/tests/fixtures/annotations/model.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/annotations/model.xsd` & `xsdata-23.7/tests/fixtures/annotations/model.xsd`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/annotations/units.xsd` & `xsdata-23.7/tests/fixtures/annotations/units.xsd`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/annotations/xsdata.xml` & `xsdata-23.7/tests/fixtures/annotations/xsdata.xml`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/artists/art001.xml` & `xsdata-23.7/tests/fixtures/artists/art001.xml`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/artists/art002.xml` & `xsdata-23.7/tests/fixtures/artists/art002.xml`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/artists/art003.xml` & `xsdata-23.7/tests/fixtures/artists/art003.xml`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/artists/metadata.py` & `xsdata-23.7/tests/fixtures/artists/metadata.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/books/books.py` & `xsdata-23.7/tests/fixtures/books/books.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/books/books.xml` & `xsdata-23.7/tests/fixtures/books/books.xml`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/books/books_auto_ns.xml` & `xsdata-23.7/tests/fixtures/books/books_auto_ns.xml`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/books/books_default_ns.xml` & `xsdata-23.7/tests/fixtures/books/books_default_ns.xml`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/books/fixtures.py` & `xsdata-23.7/tests/fixtures/books/fixtures.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/books/schema.xsd` & `xsdata-23.7/tests/fixtures/books/schema.xsd`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/calculator/__init__.py` & `xsdata-23.7/tests/fixtures/calculator/__init__.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/calculator/services.py` & `xsdata-23.7/tests/fixtures/calculator/services.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/calculator/services.wsdl` & `xsdata-23.7/tests/fixtures/calculator/services.wsdl`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/compound/models.py` & `xsdata-23.7/tests/fixtures/compound/models.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/compound/schema.xsd` & `xsdata-23.7/tests/fixtures/compound/schema.xsd`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/datatypes.py` & `xsdata-23.7/tests/fixtures/datatypes.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/docstrings/accessible/schema.py` & `xsdata-23.7/tests/fixtures/docstrings/accessible/schema.py`

 * *Files 1% similar despite different names*

```diff
@@ -13,17 +13,15 @@
     """
     class Meta:
         namespace = "urn:docs"
 
 
 @dataclass
 class DoubleQuotesSummary:
-    """
-    Dont trip on quotes: "A", "B", "C", "D" My\\Ipsum.
-    """
+    """Dont trip on quotes: "A", "B", "C", "D" My\\Ipsum"""
     class Meta:
         namespace = "urn:docs"
 
 
 class RootEnum(Enum):
     A = "A"
     B = "B"
```

### Comparing `xsdata-23.6/tests/fixtures/docstrings/blank/schema.py` & `xsdata-23.7/tests/fixtures/docstrings/blank/schema.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/docstrings/google/schema.py` & `xsdata-23.7/tests/fixtures/docstrings/google/schema.py`

 * *Files 1% similar despite different names*

```diff
@@ -13,17 +13,15 @@
     """
     class Meta:
         namespace = "urn:docs"
 
 
 @dataclass
 class DoubleQuotesSummary:
-    """
-    Dont trip on quotes: "A", "B", "C", "D" My\\Ipsum.
-    """
+    """Dont trip on quotes: "A", "B", "C", "D" My\\Ipsum"""
     class Meta:
         namespace = "urn:docs"
 
 
 class RootEnum(Enum):
     """
     Attributes
```

### Comparing `xsdata-23.6/tests/fixtures/docstrings/numpy/schema.py` & `xsdata-23.7/tests/fixtures/docstrings/numpy/schema.py`

 * *Files 3% similar despite different names*

```diff
@@ -13,40 +13,42 @@
     """
     class Meta:
         namespace = "urn:docs"
 
 
 @dataclass
 class DoubleQuotesSummary:
-    """
-    Dont trip on quotes: "A", "B", "C", "D" My\\Ipsum.
-    """
+    """Dont trip on quotes: "A", "B", "C", "D" My\\Ipsum"""
     class Meta:
         namespace = "urn:docs"
 
 
 class RootEnum(Enum):
     """
     Properties
     ----------
-    A: Lorem ipsum dolor
-    B: Lorem ipsum dolor '''sit''' amet, consectetur adipiscing elit.
-        Morbi dapibus. My\\Ipsum
+    A
+        Lorem ipsum dolor
+    B
+        Lorem ipsum dolor '''sit''' amet, consectetur adipiscing elit. Morbi
+        dapibus. My\\Ipsum
     """
     A = "A"
     B = "B"
 
 
 class RootB(Enum):
     """
     Properties
     ----------
-    YES: This is an inner enum member documentation. Lorem ipsum dolor
-        sit amet, consectetur adipiscing elit. Etiam mollis.
-    NO: Lorem ipsum dolor My\\Ipsum
+    YES
+        This is an inner enum member documentation. Lorem ipsum dolor sit
+        amet, consectetur adipiscing elit. Etiam mollis.
+    NO
+        Lorem ipsum dolor My\\Ipsum
     """
     YES = "Yes"
     NO = "No"
 
 
 class RootD(Enum):
     TRUE = "true"
@@ -60,20 +62,21 @@
     '''Lorem ipsum''' dolor sit amet, consectetur adipiscing elit. Morbi
     dapibus. Lorem ipsum dolor sit amet, consectetur adipiscing elit.
     Donec imperdiet lacus sed sagittis scelerisque. Ut sodales metus:
     "sit", "amet", "lectus" My\\Ipsum
 
     Parameters
     ----------
-    a: This is an inner type '''field''' documentation. Lorem ipsum
-        dolor sit amet, consectetur adipiscing elit. Aliquam nec.
-        My\\Ipsum
-    b: This is a second root type field documentation.
-    c:
-    d:
+    a
+        This is an inner type '''field''' documentation. Lorem ipsum dolor
+        sit amet, consectetur adipiscing elit. Aliquam nec. My\\Ipsum
+    b
+        This is a second root type field documentation.
+    c
+    d
     """
     class Meta:
         namespace = "urn:docs"
 
     a: Optional["Root.A"] = field(
         default=None,
         metadata={
@@ -110,17 +113,18 @@
     @dataclass
     class A:
         """
         This is an inner type documentation.
 
         Parameters
         ----------
-        sub_a: This is an inner type '''field''' documentation. Lorem
-            ipsum dolor sit amet, consectetur adipiscing elit. Vivamus
-            efficitur. My\\Ipsum
+        sub_a
+            This is an inner type '''field''' documentation. Lorem ipsum
+            dolor sit amet, consectetur adipiscing elit. Vivamus efficitur.
+            My\\Ipsum
         """
         sub_a: Optional[str] = field(
             default=None,
             metadata={
                 "type": "Element",
                 "namespace": "",
                 "required": True,
```

### Comparing `xsdata-23.6/tests/fixtures/docstrings/rst/schema.py` & `xsdata-23.7/tests/fixtures/docstrings/rst/schema.py`

 * *Files 0% similar despite different names*

```diff
@@ -13,17 +13,15 @@
     """
     class Meta:
         namespace = "urn:docs"
 
 
 @dataclass
 class DoubleQuotesSummary:
-    """
-    Dont trip on quotes: "A", "B", "C", "D" My\\Ipsum.
-    """
+    """Dont trip on quotes: "A", "B", "C", "D" My\\Ipsum"""
     class Meta:
         namespace = "urn:docs"
 
 
 class RootEnum(Enum):
     """
     :cvar A: Lorem ipsum dolor
```

### Comparing `xsdata-23.6/tests/fixtures/docstrings/schema.xsd` & `xsdata-23.7/tests/fixtures/docstrings/schema.xsd`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/dtd/models/complete_example.py` & `xsdata-23.7/tests/fixtures/dtd/models/complete_example.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/hello/hello.py` & `xsdata-23.7/tests/fixtures/hello/hello.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/hello/hello.wsdl` & `xsdata-23.7/tests/fixtures/hello/hello.wsdl`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/hello/hello.xsd` & `xsdata-23.7/tests/fixtures/hello/hello.xsd`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/models.py` & `xsdata-23.7/tests/fixtures/models.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/primer/order.py` & `xsdata-23.7/tests/fixtures/primer/order.py`

 * *Files 2% similar despite different names*

```diff
@@ -15,20 +15,22 @@
     )
 
     @dataclass
     class Item:
         """
         Parameters
         ----------
-        product_name:
-        quantity:
-        usprice: Price amount in USD
-        comment:
-        ship_date:
-        part_num: Stock Keeping Unit
+        product_name
+        quantity
+        usprice
+            Price amount in USD
+        comment
+        ship_date
+        part_num
+            Stock Keeping Unit
         """
         product_name: Optional[str] = field(
             default=None,
             metadata={
                 "name": "productName",
                 "type": "Element",
                 "namespace": "",
@@ -149,19 +151,21 @@
 class PurchaseOrderType:
     """Purchase order schema for Example.com.
 
     Copyright 2000 Example.com. All rights reserved.
 
     Parameters
     ----------
-    ship_to: Shipping Address
-    bill_to: Billing Address
-    comment:
-    items:
-    order_date:
+    ship_to
+        Shipping Address
+    bill_to
+        Billing Address
+    comment
+    items
+    order_date
     """
     ship_to: Optional[Usaddress] = field(
         default=None,
         metadata={
             "name": "shipTo",
             "type": "Element",
             "namespace": "",
```

### Comparing `xsdata-23.6/tests/fixtures/primer/order.xsd` & `xsdata-23.7/tests/fixtures/primer/order.xsd`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/primer/sample.json` & `xsdata-23.7/tests/fixtures/primer/sample.json`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/primer/sample.xml` & `xsdata-23.7/tests/fixtures/primer/sample.xml`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/primer/sample.xsdata.xml` & `xsdata-23.7/tests/fixtures/primer/sample.xsdata.xml`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/series/samples/show1.json` & `xsdata-23.7/tests/fixtures/series/samples/show1.json`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/series/samples/show2.json` & `xsdata-23.7/tests/fixtures/series/samples/show2.json`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/series/series.py` & `xsdata-23.7/tests/fixtures/series/series.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/stripe/.xsdata.xml` & `xsdata-23.7/tests/fixtures/stripe/.xsdata.xml`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/stripe/models/balance.py` & `xsdata-23.7/tests/fixtures/stripe/models/balance.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/fixtures/stripe/samples/balance.json` & `xsdata-23.7/tests/fixtures/stripe/samples/balance.json`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/formats/dataclass/models/test_builders.py` & `xsdata-23.7/tests/formats/dataclass/models/test_builders.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/formats/dataclass/parsers/handlers/test_lxml.py` & `xsdata-23.7/tests/formats/dataclass/parsers/handlers/test_lxml.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/formats/dataclass/parsers/handlers/test_native.py` & `xsdata-23.7/tests/formats/dataclass/parsers/handlers/test_native.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/formats/dataclass/parsers/nodes/test_element.py` & `xsdata-23.7/tests/formats/dataclass/parsers/nodes/test_element.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/formats/dataclass/parsers/nodes/test_primitive.py` & `xsdata-23.7/tests/formats/dataclass/parsers/nodes/test_primitive.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/formats/dataclass/parsers/nodes/test_standard.py` & `xsdata-23.7/tests/formats/dataclass/parsers/nodes/test_standard.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/formats/dataclass/parsers/nodes/test_union.py` & `xsdata-23.7/tests/formats/dataclass/parsers/nodes/test_union.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/formats/dataclass/parsers/nodes/test_wildcard.py` & `xsdata-23.7/tests/formats/dataclass/parsers/nodes/test_wildcard.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/formats/dataclass/parsers/nodes/test_wrapper.py` & `xsdata-23.7/tests/formats/dataclass/parsers/nodes/test_wrapper.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/formats/dataclass/parsers/test_json.py` & `xsdata-23.7/tests/formats/dataclass/parsers/test_json.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/formats/dataclass/parsers/test_mixins.py` & `xsdata-23.7/tests/formats/dataclass/parsers/test_mixins.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/formats/dataclass/parsers/test_node.py` & `xsdata-23.7/tests/formats/dataclass/parsers/test_node.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/formats/dataclass/parsers/test_tree.py` & `xsdata-23.7/tests/formats/dataclass/parsers/test_tree.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/formats/dataclass/parsers/test_utils.py` & `xsdata-23.7/tests/formats/dataclass/parsers/test_utils.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/formats/dataclass/parsers/test_xml.py` & `xsdata-23.7/tests/formats/dataclass/parsers/test_xml.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/formats/dataclass/serializers/test_code.py` & `xsdata-23.7/tests/formats/dataclass/serializers/test_code.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/formats/dataclass/serializers/test_json.py` & `xsdata-23.7/tests/formats/dataclass/serializers/test_json.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/formats/dataclass/serializers/test_mixins.py` & `xsdata-23.7/tests/formats/dataclass/serializers/test_mixins.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/formats/dataclass/serializers/test_xml.py` & `xsdata-23.7/tests/formats/dataclass/serializers/test_xml.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/formats/dataclass/serializers/writers/test_lxml.py` & `xsdata-23.7/tests/formats/dataclass/serializers/writers/test_lxml.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/formats/dataclass/serializers/writers/test_native.py` & `xsdata-23.7/tests/formats/dataclass/serializers/writers/test_native.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/formats/dataclass/test_client.py` & `xsdata-23.7/tests/formats/dataclass/test_client.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/formats/dataclass/test_compat.py` & `xsdata-23.7/tests/formats/dataclass/test_compat.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/formats/dataclass/test_context.py` & `xsdata-23.7/tests/formats/dataclass/test_context.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/formats/dataclass/test_elements.py` & `xsdata-23.7/tests/formats/dataclass/test_elements.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/formats/dataclass/test_filters.py` & `xsdata-23.7/tests/formats/dataclass/test_filters.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/formats/dataclass/test_generator.py` & `xsdata-23.7/tests/formats/dataclass/test_generator.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/formats/dataclass/test_transport.py` & `xsdata-23.7/tests/formats/dataclass/test_transport.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/formats/dataclass/test_typing.py` & `xsdata-23.7/tests/formats/dataclass/test_typing.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/formats/test_converter.py` & `xsdata-23.7/tests/formats/test_converter.py`

 * *Files 1% similar despite different names*

```diff
@@ -38,15 +38,15 @@
         self.assertEqual("1", converter.serialize(1))
         self.assertEqual("1 2 3", converter.serialize([1, "2", 3]))
         self.assertEqual(None, converter.serialize(None))
         self.assertEqual("1", converter.serialize(1))
         self.assertEqual("1.5", converter.serialize(1.5))
         self.assertEqual("true", converter.serialize(True))
         self.assertEqual("optional", converter.serialize(UseType.OPTIONAL))
-        self.assertEqual("8.77683E-8", converter.serialize(Decimal("8.77683E-8")))
+        self.assertEqual("0.0000000877683", converter.serialize(Decimal("8.77683E-8")))
         self.assertEqual("8.77683E-08", converter.serialize(float("8.77683E-8")))
 
     def test_test(self):
         self.assertTrue(converter.test("1", [int]))
         self.assertTrue(converter.test("1", [float]))
         self.assertFalse(converter.test("1", [float], strict=True))
         self.assertFalse(converter.test(None, [int]))
@@ -250,15 +250,17 @@
         self.assertEqual(Decimal(1), self.converter.deserialize("1"))
 
     def test_serialize(self):
         self.assertEqual("2.1", self.converter.serialize(Decimal("2.1")))
         self.assertEqual("INF", self.converter.serialize(Decimal("inf")))
         self.assertEqual("INF", self.converter.serialize(Decimal("+inf")))
         self.assertEqual("-INF", self.converter.serialize(Decimal("-inf")))
-        self.assertEqual("8.77683E-8", self.converter.serialize(Decimal("8.77683E-8")))
+        self.assertEqual(
+            "0.0000000877683", self.converter.serialize(Decimal("8.77683E-8"))
+        )
 
 
 class DateTimeConverterTests(TestCase):
     def setUp(self):
         self.converter = converter.type_converter(datetime)
 
     def test_converter(self):
```

### Comparing `xsdata-23.6/tests/formats/test_mixins.py` & `xsdata-23.7/tests/formats/test_mixins.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/integration/benchmarks/test_converters.py` & `xsdata-23.7/tests/integration/benchmarks/test_converters.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/integration/benchmarks/test_handlers.py` & `xsdata-23.7/tests/integration/benchmarks/test_handlers.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/integration/benchmarks/utils.py` & `xsdata-23.7/tests/integration/benchmarks/utils.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/integration/test_annotations.py` & `xsdata-23.7/tests/integration/test_annotations.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/integration/test_artists.py` & `xsdata-23.7/tests/integration/test_artists.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/integration/test_books.py` & `xsdata-23.7/tests/integration/test_books.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/integration/test_calculator.py` & `xsdata-23.7/tests/integration/test_calculator.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/integration/test_compound.py` & `xsdata-23.7/tests/integration/test_compound.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/integration/test_docstrings.py` & `xsdata-23.7/tests/integration/test_docstrings.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/integration/test_dtd.py` & `xsdata-23.7/tests/integration/test_dtd.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/integration/test_hello_rpc.py` & `xsdata-23.7/tests/integration/test_hello_rpc.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/integration/test_primer.py` & `xsdata-23.7/tests/integration/test_primer.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/integration/test_series.py` & `xsdata-23.7/tests/integration/test_series.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/integration/test_stripe.py` & `xsdata-23.7/tests/integration/test_stripe.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/models/enums/test_datatype.py` & `xsdata-23.7/tests/models/enums/test_datatype.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/models/test_config.py` & `xsdata-23.7/tests/models/test_config.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/models/test_datatype.py` & `xsdata-23.7/tests/models/test_datatype.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/models/test_mixins.py` & `xsdata-23.7/tests/models/test_mixins.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/models/test_type_mapping.py` & `xsdata-23.7/tests/models/test_type_mapping.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/models/wsdl/test_binding.py` & `xsdata-23.7/tests/models/wsdl/test_binding.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/models/wsdl/test_definitions.py` & `xsdata-23.7/tests/models/wsdl/test_definitions.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/models/wsdl/test_port_type.py` & `xsdata-23.7/tests/models/wsdl/test_port_type.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/models/xsd/test_alternative.py` & `xsdata-23.7/tests/models/xsd/test_alternative.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/models/xsd/test_annotation_base.py` & `xsdata-23.7/tests/models/xsd/test_annotation_base.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/models/xsd/test_any.py` & `xsdata-23.7/tests/models/xsd/test_any.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/models/xsd/test_any_attribute.py` & `xsdata-23.7/tests/models/xsd/test_any_attribute.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/models/xsd/test_attribute.py` & `xsdata-23.7/tests/models/xsd/test_attribute.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/models/xsd/test_complex_type.py` & `xsdata-23.7/tests/models/xsd/test_complex_type.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/models/xsd/test_element.py` & `xsdata-23.7/tests/models/xsd/test_element.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/models/xsd/test_enumeration.py` & `xsdata-23.7/tests/models/xsd/test_enumeration.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/models/xsd/test_group.py` & `xsdata-23.7/tests/models/xsd/test_group.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/models/xsd/test_list.py` & `xsdata-23.7/tests/models/xsd/test_list.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/models/xsd/test_restriction.py` & `xsdata-23.7/tests/models/xsd/test_restriction.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/models/xsd/test_schema.py` & `xsdata-23.7/tests/models/xsd/test_schema.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/models/xsd/test_simple_type.py` & `xsdata-23.7/tests/models/xsd/test_simple_type.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/models/xsd/test_union.py` & `xsdata-23.7/tests/models/xsd/test_union.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/test_cli.py` & `xsdata-23.7/tests/test_cli.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/utils/test_collections.py` & `xsdata-23.7/tests/utils/test_collections.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/utils/test_dates.py` & `xsdata-23.7/tests/utils/test_dates.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/utils/test_downloader.py` & `xsdata-23.7/tests/utils/test_downloader.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/utils/test_hooks.py` & `xsdata-23.7/tests/utils/test_hooks.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/utils/test_namespaces.py` & `xsdata-23.7/tests/utils/test_namespaces.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/tests/utils/test_text.py` & `xsdata-23.7/tests/utils/test_text.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/cli.py` & `xsdata-23.7/xsdata/cli.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/analyzer.py` & `xsdata-23.7/xsdata/codegen/analyzer.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/container.py` & `xsdata-23.7/xsdata/codegen/container.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/handlers/__init__.py` & `xsdata-23.7/xsdata/codegen/handlers/__init__.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/handlers/add_attribute_substitutions.py` & `xsdata-23.7/xsdata/codegen/handlers/add_attribute_substitutions.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/handlers/calculate_attribute_paths.py` & `xsdata-23.7/xsdata/codegen/handlers/calculate_attribute_paths.py`

 * *Files 6% similar despite different names*

```diff
@@ -32,16 +32,14 @@
         for path in attr.restrictions.path:
             name, index, mi, ma = path
 
             if name == SEQUENCE:
                 if not attr.restrictions.sequence:
                     attr.restrictions.sequence = index
             elif name == CHOICE:
-                if mi <= 1:
-                    mi = 0
                 if not attr.restrictions.choice:
                     attr.restrictions.choice = index
             elif name == GROUP:
                 attr.restrictions.group = index
             else:
                 pass
```

### Comparing `xsdata-23.6/xsdata/codegen/handlers/create_compound_fields.py` & `xsdata-23.7/xsdata/codegen/handlers/create_compound_fields.py`

 * *Files 11% similar despite different names*

```diff
@@ -13,46 +13,65 @@
 from xsdata.codegen.models import Restrictions
 from xsdata.codegen.utils import ClassUtils
 from xsdata.formats.dataclass.models.elements import XmlType
 from xsdata.models.enums import DataType
 from xsdata.models.enums import Tag
 from xsdata.utils.collections import group_by
 
+ALL = "a"
+GROUP = "g"
+SEQUENCE = "s"
+CHOICE = "c"
+
 
 class CreateCompoundFields(RelativeHandlerInterface):
     """Group attributes that belong in the same choice and replace them by
     compound fields."""
 
     __slots__ = "config"
 
     def __init__(self, container: ContainerInterface):
         super().__init__(container)
 
         self.config = container.config.output.compound_fields
 
     def process(self, target: Class):
-        if self.config.enabled:
-            groups = group_by(target.attrs, get_restriction_choice)
-            for choice, attrs in groups.items():
-                if choice and len(attrs) > 1:
+        groups = group_by(target.attrs, get_restriction_choice)
+        for choice, attrs in groups.items():
+            if choice and len(attrs) > 1:
+                if self.config.enabled:
                     self.group_fields(target, attrs)
+                else:
+                    self.calculate_choice_min_occurs(attrs)
+
+    @classmethod
+    def calculate_choice_min_occurs(cls, attrs: List[Attr]):
+        for attr in attrs:
+            for path in attr.restrictions.path:
+                name, index, mi, ma = path
+                if name == CHOICE and mi <= 1:
+                    attr.restrictions.min_occurs = 0
 
     @classmethod
     def update_counters(cls, attr: Attr, counters: Dict):
         started = False
         choice = attr.restrictions.choice
         for path in attr.restrictions.path:
-            if not started and path[0] != "c" and path[1] != choice:
+            name, index, mi, ma = path
+            if not started and name != CHOICE and index != choice:
                 continue
 
             started = True
             if path not in counters:
                 counters[path] = {"min": [], "max": []}
             counters = counters[path]
 
+            if mi <= 1:
+                attr.restrictions.min_occurs = 0
+
         counters["min"].append(attr.restrictions.min_occurs)
         counters["max"].append(attr.restrictions.max_occurs)
 
     def group_fields(self, target: Class, attrs: List[Attr]):
         """Group attributes into a new compound field."""
         pos = target.attrs.index(attrs[0])
         choice = attrs[0].restrictions.choice
```

### Comparing `xsdata-23.6/xsdata/codegen/handlers/designate_class_packages.py` & `xsdata-23.7/xsdata/codegen/handlers/designate_class_packages.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/handlers/filter_classes.py` & `xsdata-23.7/xsdata/codegen/handlers/filter_classes.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/handlers/flatten_attribute_groups.py` & `xsdata-23.7/xsdata/codegen/handlers/flatten_attribute_groups.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/handlers/flatten_class_extensions.py` & `xsdata-23.7/xsdata/codegen/handlers/flatten_class_extensions.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/handlers/merge_attributes.py` & `xsdata-23.7/xsdata/codegen/handlers/merge_attributes.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/handlers/process_attributes_types.py` & `xsdata-23.7/xsdata/codegen/handlers/process_attributes_types.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/handlers/process_mixed_content_class.py` & `xsdata-23.7/xsdata/codegen/handlers/process_mixed_content_class.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/handlers/rename_duplicate_attributes.py` & `xsdata-23.7/xsdata/codegen/handlers/rename_duplicate_attributes.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/handlers/rename_duplicate_classes.py` & `xsdata-23.7/xsdata/codegen/handlers/rename_duplicate_classes.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/handlers/reset_attribute_sequence_numbers.py` & `xsdata-23.7/xsdata/codegen/handlers/reset_attribute_sequence_numbers.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/handlers/reset_attribute_sequences.py` & `xsdata-23.7/xsdata/codegen/handlers/reset_attribute_sequences.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/handlers/sanitize_attributes_default_value.py` & `xsdata-23.7/xsdata/codegen/handlers/sanitize_attributes_default_value.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/handlers/sanitize_enumeration_class.py` & `xsdata-23.7/xsdata/codegen/handlers/sanitize_enumeration_class.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/handlers/unnest_inner_classes.py` & `xsdata-23.7/xsdata/codegen/handlers/unnest_inner_classes.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/handlers/update_attributes_effective_choice.py` & `xsdata-23.7/xsdata/codegen/handlers/update_attributes_effective_choice.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/handlers/vacuum_inner_classes.py` & `xsdata-23.7/xsdata/codegen/handlers/vacuum_inner_classes.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/handlers/validate_attributes_overrides.py` & `xsdata-23.7/xsdata/codegen/handlers/validate_attributes_overrides.py`

 * *Files 10% similar despite different names*

```diff
@@ -56,14 +56,16 @@
 
         if (
             attr.default == source_attr.default
             and bool_eq(attr.fixed, source_attr.fixed)
             and bool_eq(attr.mixed, source_attr.mixed)
             and bool_eq(attr.restrictions.tokens, source_attr.restrictions.tokens)
             and bool_eq(attr.restrictions.nillable, source_attr.restrictions.nillable)
+            and bool_eq(attr.is_prohibited, source_attr.is_prohibited)
+            and bool_eq(attr.is_optional, source_attr.is_optional)
         ):
             cls.remove_attribute(target, attr)
 
     @classmethod
     def remove_attribute(cls, target: Class, attr: Attr):
         ClassUtils.remove_attribute(target, attr)
         ClassUtils.clean_inner_classes(target)
```

### Comparing `xsdata-23.6/xsdata/codegen/mappers/definitions.py` & `xsdata-23.7/xsdata/codegen/mappers/definitions.py`

 * *Files 2% similar despite different names*

```diff
@@ -106,21 +106,21 @@
         for message_class in operation_messages:
             yield message_class
             # Only Envelope classes need to be added in service input/output
             if message_class.meta_name:
                 message_type = message_class.name.split("_")[-1]
                 attrs.append(cls.build_attr(message_type, message_class.qname))
 
-        assert definitions.location is not None
+        assert binding_operation.location is not None
 
         yield Class(
             qname=namespaces.build_qname(definitions.target_namespace, name),
             status=Status.FLATTENED,
             tag=type(binding_operation).__name__,
-            location=definitions.location,
+            location=binding_operation.location,
             ns_map=binding_operation.ns_map,
             attrs=attrs,
         )
 
     @classmethod
     def map_binding_operation_messages(
         cls,
@@ -206,21 +206,21 @@
         style: str,
         namespace: Optional[str],
         operation: Optional[str],
     ) -> Class:
         """Step 6.1: Build Envelope class for the given binding message with
         attributes from the port type message."""
 
-        assert definitions.location is not None
+        assert binding_message.location is not None
 
         target = Class(
             qname=namespaces.build_qname(definitions.target_namespace, name),
             meta_name="Envelope",
             tag=Tag.BINDING_MESSAGE,
-            location=definitions.location,
+            location=binding_message.location,
             ns_map=binding_message.ns_map,
             namespace=namespace,
         )
         message = port_type_message.message
 
         for ext in binding_message.extended_elements:
             assert ext.qname is not None
@@ -249,22 +249,22 @@
         operation."""
         prefix, name = text.split(port_type_message.message)
 
         definition_message = definitions.find_message(name)
         ns_map = definition_message.ns_map.copy()
         source_namespace = ns_map.get(prefix)
 
-        assert definitions.location is not None
+        assert port_type_message.location is not None
 
         return Class(
             qname=namespaces.build_qname(source_namespace, name),
             namespace=source_namespace,
             status=Status.RAW,
             tag=Tag.ELEMENT,
-            location=definitions.location,
+            location=port_type_message.location,
             ns_map=ns_map,
             attrs=list(cls.build_parts_attributes(definition_message.parts, ns_map)),
         )
 
     @classmethod
     def build_inner_class(
         cls, target: Class, name: str, namespace: Optional[str] = None
```

### Comparing `xsdata-23.6/xsdata/codegen/mappers/dict.py` & `xsdata-23.7/xsdata/codegen/mappers/dict.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/mappers/dtd.py` & `xsdata-23.7/xsdata/codegen/mappers/dtd.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/mappers/element.py` & `xsdata-23.7/xsdata/codegen/mappers/element.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/mappers/schema.py` & `xsdata-23.7/xsdata/codegen/mappers/schema.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/mixins.py` & `xsdata-23.7/xsdata/codegen/mixins.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/models.py` & `xsdata-23.7/xsdata/codegen/models.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/parsers/dtd.py` & `xsdata-23.7/xsdata/codegen/parsers/dtd.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/parsers/schema.py` & `xsdata-23.7/xsdata/codegen/parsers/schema.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/resolver.py` & `xsdata-23.7/xsdata/codegen/resolver.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/transformer.py` & `xsdata-23.7/xsdata/codegen/transformer.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/utils.py` & `xsdata-23.7/xsdata/codegen/utils.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/validator.py` & `xsdata-23.7/xsdata/codegen/validator.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/codegen/writer.py` & `xsdata-23.7/xsdata/codegen/writer.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/exceptions.py` & `xsdata-23.7/xsdata/exceptions.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/bindings.py` & `xsdata-23.7/xsdata/formats/bindings.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/converter.py` & `xsdata-23.7/xsdata/formats/converter.py`

 * *Files 0% similar despite different names*

```diff
@@ -320,15 +320,15 @@
         except InvalidOperation:
             raise ConverterError()
 
     def serialize(self, value: Decimal, **kwargs: Any) -> str:
         if value.is_infinite():
             return str(value).replace("Infinity", "INF")
 
-        return str(value)
+        return f"{value:f}"
 
 
 class QNameConverter(Converter):
     def deserialize(
         self,
         value: str,
         ns_map: Optional[Dict] = None,
```

### Comparing `xsdata-23.6/xsdata/formats/dataclass/client.py` & `xsdata-23.7/xsdata/formats/dataclass/client.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/compat.py` & `xsdata-23.7/xsdata/formats/dataclass/compat.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/context.py` & `xsdata-23.7/xsdata/formats/dataclass/context.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/filters.py` & `xsdata-23.7/xsdata/formats/dataclass/filters.py`

 * *Files 0% similar despite different names*

```diff
@@ -518,24 +518,26 @@
                 drop_whitespace=False,
                 replace_whitespace=False,
                 break_long_words=True,
             )
         )
         return f"(\n{value}\n{' ' * indent})"
 
-    def text_wrap(self, string: str, offset: int = 0) -> str:
+    def text_wrap(
+        self, string: str, offset: int = 0, subsequent_indent: str = "    "
+    ) -> str:
         """Wrap text in respect to the max line length and the given offset."""
         return "\n".join(
             textwrap.wrap(
                 string,
                 width=self.max_line_length - offset,
                 drop_whitespace=True,
                 replace_whitespace=True,
                 break_long_words=False,
-                subsequent_indent="    ",
+                subsequent_indent=subsequent_indent,
             )
         )
 
     @classmethod
     def clean_docstring(cls, string: Optional[str], escape: bool = True) -> str:
         """
         Prepare string for docstring generation.
```

### Comparing `xsdata-23.6/xsdata/formats/dataclass/generator.py` & `xsdata-23.7/xsdata/formats/dataclass/generator.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/models/builders.py` & `xsdata-23.7/xsdata/formats/dataclass/models/builders.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/models/elements.py` & `xsdata-23.7/xsdata/formats/dataclass/models/elements.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/models/generics.py` & `xsdata-23.7/xsdata/formats/dataclass/models/generics.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/parsers/bases.py` & `xsdata-23.7/xsdata/formats/dataclass/parsers/bases.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/parsers/config.py` & `xsdata-23.7/xsdata/formats/dataclass/parsers/config.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/parsers/handlers/__init__.py` & `xsdata-23.7/xsdata/formats/dataclass/parsers/handlers/__init__.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/parsers/handlers/lxml.py` & `xsdata-23.7/xsdata/formats/dataclass/parsers/handlers/lxml.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/parsers/handlers/native.py` & `xsdata-23.7/xsdata/formats/dataclass/parsers/handlers/native.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/parsers/json.py` & `xsdata-23.7/xsdata/formats/dataclass/parsers/json.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/parsers/mixins.py` & `xsdata-23.7/xsdata/formats/dataclass/parsers/mixins.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/parsers/nodes/__init__.py` & `xsdata-23.7/xsdata/formats/dataclass/parsers/nodes/__init__.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/parsers/nodes/element.py` & `xsdata-23.7/xsdata/formats/dataclass/parsers/nodes/element.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/parsers/nodes/primitive.py` & `xsdata-23.7/xsdata/formats/dataclass/parsers/nodes/primitive.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/parsers/nodes/skip.py` & `xsdata-23.7/xsdata/formats/dataclass/parsers/nodes/skip.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/parsers/nodes/standard.py` & `xsdata-23.7/xsdata/formats/dataclass/parsers/nodes/standard.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/parsers/nodes/union.py` & `xsdata-23.7/xsdata/formats/dataclass/parsers/nodes/union.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/parsers/nodes/wildcard.py` & `xsdata-23.7/xsdata/formats/dataclass/parsers/nodes/wildcard.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/parsers/nodes/wrapper.py` & `xsdata-23.7/xsdata/formats/dataclass/parsers/nodes/wrapper.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/parsers/tree.py` & `xsdata-23.7/xsdata/formats/dataclass/parsers/tree.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/parsers/utils.py` & `xsdata-23.7/xsdata/formats/dataclass/parsers/utils.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/parsers/xml.py` & `xsdata-23.7/xsdata/formats/dataclass/parsers/xml.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/serializers/code.py` & `xsdata-23.7/xsdata/formats/dataclass/serializers/code.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/serializers/config.py` & `xsdata-23.7/xsdata/formats/dataclass/serializers/config.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/serializers/json.py` & `xsdata-23.7/xsdata/formats/dataclass/serializers/json.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/serializers/mixins.py` & `xsdata-23.7/xsdata/formats/dataclass/serializers/mixins.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/serializers/writers/__init__.py` & `xsdata-23.7/xsdata/formats/dataclass/serializers/writers/__init__.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/serializers/writers/lxml.py` & `xsdata-23.7/xsdata/formats/dataclass/serializers/writers/lxml.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/serializers/writers/native.py` & `xsdata-23.7/xsdata/formats/dataclass/serializers/writers/native.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/serializers/xml.py` & `xsdata-23.7/xsdata/formats/dataclass/serializers/xml.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/templates/class.jinja2` & `xsdata-23.7/xsdata/formats/dataclass/templates/class.jinja2`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/templates/enum.jinja2` & `xsdata-23.7/xsdata/formats/dataclass/templates/enum.jinja2`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/transports.py` & `xsdata-23.7/xsdata/formats/dataclass/transports.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/dataclass/typing.py` & `xsdata-23.7/xsdata/formats/dataclass/typing.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/formats/mixins.py` & `xsdata-23.7/xsdata/formats/mixins.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/models/config.py` & `xsdata-23.7/xsdata/models/config.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/models/datatype.py` & `xsdata-23.7/xsdata/models/datatype.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/models/dtd.py` & `xsdata-23.7/xsdata/models/dtd.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/models/enums.py` & `xsdata-23.7/xsdata/models/enums.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/models/mixins.py` & `xsdata-23.7/xsdata/models/mixins.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/models/wsdl.py` & `xsdata-23.7/xsdata/models/wsdl.py`

 * *Files 1% similar despite different names*

```diff
@@ -28,18 +28,21 @@
 
 
 @dataclass
 class WsdlElement:
     """
     :param name:
     :param documentation:
+    :param location:
+    :param ns_map
     """
 
     name: str = attribute()
     documentation: Optional[Documentation] = element()
+    location: Optional[str] = field(default=None, metadata={"type": "Ignore"})
     ns_map: Dict[str, str] = field(
         default_factory=dict, init=False, metadata={"type": "Ignore"}
     )
 
 
 @dataclass
 class ExtensibleElement(WsdlElement):
@@ -203,15 +206,14 @@
     target_namespace: Optional[str] = attribute(name="targetNamespace")
     types: Optional[Types] = element()
     imports: List[Import] = array_element(name="import")
     messages: List[Message] = array_element(name="message")
     port_types: List[PortType] = array_element(name="portType")
     bindings: List[Binding] = array_element(name="binding")
     services: List[Service] = array_element(name="service")
-    location: Optional[str] = field(default=None)
 
     @property
     def schemas(self):
         if self.types:
             yield from self.types.schemas
 
     def find_binding(self, name: str) -> Binding:
```

### Comparing `xsdata-23.6/xsdata/models/xsd.py` & `xsdata-23.7/xsdata/models/xsd.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/schemas/mathml3-common.xsd` & `xsdata-23.7/xsdata/schemas/mathml3-common.xsd`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/schemas/mathml3-content.xsd` & `xsdata-23.7/xsdata/schemas/mathml3-content.xsd`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/schemas/mathml3-presentation.xsd` & `xsdata-23.7/xsdata/schemas/mathml3-presentation.xsd`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/schemas/mathml3-strict-content.xsd` & `xsdata-23.7/xsdata/schemas/mathml3-strict-content.xsd`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/schemas/xlink.xsd` & `xsdata-23.7/xsdata/schemas/xlink.xsd`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/schemas/xml.xsd` & `xsdata-23.7/xsdata/schemas/xml.xsd`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/utils/click.py` & `xsdata-23.7/xsdata/utils/click.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/utils/collections.py` & `xsdata-23.7/xsdata/utils/collections.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/utils/dates.py` & `xsdata-23.7/xsdata/utils/dates.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/utils/debug.py` & `xsdata-23.7/xsdata/utils/debug.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/utils/downloader.py` & `xsdata-23.7/xsdata/utils/downloader.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/utils/graphs.py` & `xsdata-23.7/xsdata/utils/graphs.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/utils/namespaces.py` & `xsdata-23.7/xsdata/utils/namespaces.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/utils/objects.py` & `xsdata-23.7/xsdata/utils/objects.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/utils/package.py` & `xsdata-23.7/xsdata/utils/package.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/utils/testing.py` & `xsdata-23.7/xsdata/utils/testing.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata/utils/text.py` & `xsdata-23.7/xsdata/utils/text.py`

 * *Files identical despite different names*

### Comparing `xsdata-23.6/xsdata.egg-info/PKG-INFO` & `xsdata-23.7/xsdata.egg-info/PKG-INFO`

 * *Files 8% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: xsdata
-Version: 23.6
+Version: 23.7
 Summary: Python XML Binding
 Author-email: Christodoulos Tsoulloftas <chris@komposta.net>
 License: MIT
 Project-URL: Homepage, https://github.com/tefra/xsdata
 Project-URL: Source, https://github.com/tefra/xsdata
 Project-URL: Documentation, https://xsdata.readthedocs.io/
 Project-URL: Changelog, https://xsdata.readthedocs.io/en/latest/changelog.html
@@ -30,27 +30,27 @@
 Provides-Extra: cli
 Provides-Extra: docs
 Provides-Extra: lxml
 Provides-Extra: soap
 Provides-Extra: test
 License-File: LICENSE
 
-.. image:: https://github.com/tefra/xsdata/raw/master/docs/_static/logo.svg
+.. image:: https://github.com/tefra/xsdata/raw/main/docs/_static/logo.svg
     :target: https://xsdata.readthedocs.io/
 
 Naive XML Bindings for python
 =============================
 
 .. image:: https://github.com/tefra/xsdata/workflows/tests/badge.svg
     :target: https://github.com/tefra/xsdata/actions
 
 .. image:: https://readthedocs.org/projects/xsdata/badge
     :target: https://xsdata.readthedocs.io/
 
-.. image:: https://codecov.io/gh/tefra/xsdata/branch/master/graph/badge.svg
+.. image:: https://codecov.io/gh/tefra/xsdata/branch/main/graph/badge.svg
     :target: https://codecov.io/gh/tefra/xsdata
 
 .. image:: https://img.shields.io/github/languages/top/tefra/xsdata.svg
     :target: https://xsdata.readthedocs.io/
 
 .. image:: https://www.codefactor.io/repository/github/tefra/xsdata/badge
    :target: https://www.codefactor.io/repository/github/tefra/xsdata
@@ -131,18 +131,14 @@
   - Handlers and Writers based on lxml and native xml python
   - Support wildcard elements and attributes
   - Support xinclude statements and unknown properties
   - Customize behaviour through config
 
 
 
-Changelog: 23.6 (2023-06-24)
+Changelog: 23.7 (2023-07-23)
 ----------------------------
-- Fixed conflicting enum values leading to wrong default values (`#806 <https://github.com/tefra/xsdata/pull/806>`_)
-- Added support for custom decorators and base classes (`#793 <https://github.com/tefra/xsdata/pull/793>`_)
-- Added parser config to load external dtd to resolve entities (`#797 <https://github.com/tefra/xsdata/pull/797>`_)
-- Added requests sessions on the wsdl client transport (`#798 <https://github.com/tefra/xsdata/pull/798>`_)
-- Added support subscriptable types and UnionType (`#801 <https://github.com/tefra/xsdata/pull/801>`_)
-- Added option to restrict models package for auto-locator (`#809 <https://github.com/tefra/xsdata/pull/809>`_)
-- Updated context to only cache supported classes (`#796 <https://github.com/tefra/xsdata/pull/796>`_)
-- Removed tox requirement (`#800 <https://github.com/tefra/xsdata/pull/800>`_)
-- Converted to pyproject.toml (`#802 <https://github.com/tefra/xsdata/pull/802>`_)
+- Fixed decimal converter to avoid scientific notations (`#826 <https://github.com/tefra/xsdata/pull/826>`_)
+- Fixed nympy paramater docstring format  (`#827 <https://github.com/tefra/xsdata/pull/827>`_)
+- Fixed optional/required override validation (`#820 <https://github.com/tefra/xsdata/pull/820>`_)
+- Fixed WSDL mapper to respect the elements original location (`#832 <https://github.com/tefra/xsdata/pull/832>`_)
+- Added Python 3.12 support
```

### Comparing `xsdata-23.6/xsdata.egg-info/SOURCES.txt` & `xsdata-23.7/xsdata.egg-info/SOURCES.txt`

 * *Files identical despite different names*

