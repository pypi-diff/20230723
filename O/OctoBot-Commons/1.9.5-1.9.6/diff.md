# Comparing `tmp/OctoBot-Commons-1.9.5.tar.gz` & `tmp/OctoBot-Commons-1.9.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "OctoBot-Commons-1.9.5.tar", last modified: Wed May 17 11:33:45 2023, max compression
+gzip compressed data, was "OctoBot-Commons-1.9.6.tar", last modified: Sun Jul 23 13:24:07 2023, max compression
```

## Comparing `OctoBot-Commons-1.9.5.tar` & `OctoBot-Commons-1.9.6.tar`

### file list

```diff
@@ -1,184 +1,187 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.529565 OctoBot-Commons-1.9.5/
--rw-r--r--   0 runner    (1001) docker     (123)    19398 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/CHANGELOG.md
--rw-r--r--   0 runner    (1001) docker     (123)     7652 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      141 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/MANIFEST.in
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.517565 OctoBot-Commons-1.9.5/OctoBot_Commons.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1831 2023-05-17 11:33:45.000000 OctoBot-Commons-1.9.5/OctoBot_Commons.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     6307 2023-05-17 11:33:45.000000 OctoBot-Commons-1.9.5/OctoBot_Commons.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-17 11:33:45.000000 OctoBot-Commons-1.9.5/OctoBot_Commons.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-05-17 11:33:45.000000 OctoBot-Commons-1.9.5/OctoBot_Commons.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)      109 2023-05-17 11:33:45.000000 OctoBot-Commons-1.9.5/OctoBot_Commons.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       22 2023-05-17 11:33:45.000000 OctoBot-Commons-1.9.5/OctoBot_Commons.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)     1831 2023-05-17 11:33:45.529565 OctoBot-Commons-1.9.5/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1198 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.517565 OctoBot-Commons-1.9.5/octobot_commons/
--rw-r--r--   0 runner    (1001) docker     (123)      979 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1814 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/aiohttp_util.py
--rw-r--r--   0 runner    (1001) docker     (123)    10371 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/async_job.py
--rw-r--r--   0 runner    (1001) docker     (123)     4436 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/asyncio_tools.py
--rw-r--r--   0 runner    (1001) docker     (123)     4974 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/authentication.py
--rw-r--r--   0 runner    (1001) docker     (123)     2138 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/channels_name.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.521565 OctoBot-Commons-1.9.5/octobot_commons/configuration/
--rw-r--r--   0 runner    (1001) docker     (123)     3070 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/configuration/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6914 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/configuration/config_file_manager.py
--rw-r--r--   0 runner    (1001) docker     (123)     4574 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/configuration/config_operations.py
--rw-r--r--   0 runner    (1001) docker     (123)    12191 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/configuration/configuration.py
--rw-r--r--   0 runner    (1001) docker     (123)     3052 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/configuration/fields_utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     5144 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/configuration/user_input_configuration.py
--rw-r--r--   0 runner    (1001) docker     (123)    10797 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/configuration/user_inputs.py
--rw-r--r--   0 runner    (1001) docker     (123)     6830 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/constants.py
--rw-r--r--   0 runner    (1001) docker     (123)     2122 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/data_util.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.521565 OctoBot-Commons-1.9.5/octobot_commons/databases/
--rw-r--r--   0 runner    (1001) docker     (123)     3131 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.521565 OctoBot-Commons-1.9.5/octobot_commons/databases/bases/
--rw-r--r--   0 runner    (1001) docker     (123)     1067 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/bases/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6416 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/bases/base_database.py
--rw-r--r--   0 runner    (1001) docker     (123)     6226 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/bases/document_database.py
--rw-r--r--   0 runner    (1001) docker     (123)     9482 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/cache_client.py
--rw-r--r--   0 runner    (1001) docker     (123)    16509 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/cache_manager.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.521565 OctoBot-Commons-1.9.5/octobot_commons/databases/database_caches/
--rw-r--r--   0 runner    (1001) docker     (123)     1201 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/database_caches/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5588 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/database_caches/chronological_read_database_cache.py
--rw-r--r--   0 runner    (1001) docker     (123)     4885 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/database_caches/generic_database_cache.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.521565 OctoBot-Commons-1.9.5/octobot_commons/databases/databases_util/
--rw-r--r--   0 runner    (1001) docker     (123)      874 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/databases_util/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2498 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/databases_util/cache_wrapper.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.521565 OctoBot-Commons-1.9.5/octobot_commons/databases/document_database_adaptors/
--rw-r--r--   0 runner    (1001) docker     (123)     1229 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/document_database_adaptors/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     7813 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/document_database_adaptors/abstract_document_database_adaptor.py
--rw-r--r--   0 runner    (1001) docker     (123)    11991 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/document_database_adaptors/tinydb_adaptor.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.521565 OctoBot-Commons-1.9.5/octobot_commons/databases/global_storage/
--rw-r--r--   0 runner    (1001) docker     (123)      967 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/global_storage/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1481 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/global_storage/global_shared_memory_storage.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.521565 OctoBot-Commons-1.9.5/octobot_commons/databases/implementations/
--rw-r--r--   0 runner    (1001) docker     (123)     1828 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/implementations/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5255 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/implementations/_exchange_database.py
--rw-r--r--   0 runner    (1001) docker     (123)     3759 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/implementations/cache_database.py
--rw-r--r--   0 runner    (1001) docker     (123)     8433 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/implementations/cache_timestamp_database.py
--rw-r--r--   0 runner    (1001) docker     (123)     1514 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/implementations/db_reader.py
--rw-r--r--   0 runner    (1001) docker     (123)     7873 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/implementations/db_writer.py
--rw-r--r--   0 runner    (1001) docker     (123)      921 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/implementations/db_writer_reader.py
--rw-r--r--   0 runner    (1001) docker     (123)     6275 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/implementations/meta_database.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.521565 OctoBot-Commons-1.9.5/octobot_commons/databases/relational_databases/
--rw-r--r--   0 runner    (1001) docker     (123)      988 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/relational_databases/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.521565 OctoBot-Commons-1.9.5/octobot_commons/databases/relational_databases/sqlite/
--rw-r--r--   0 runner    (1001) docker     (123)      996 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/relational_databases/sqlite/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1878 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/relational_databases/sqlite/cursor_pool.py
--rw-r--r--   0 runner    (1001) docker     (123)      951 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/relational_databases/sqlite/cursor_wrapper.py
--rw-r--r--   0 runner    (1001) docker     (123)    13195 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/relational_databases/sqlite/sqlite_database.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.521565 OctoBot-Commons-1.9.5/octobot_commons/databases/run_databases/
--rw-r--r--   0 runner    (1001) docker     (123)     1790 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/run_databases/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5955 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/run_databases/abstract_run_databases_pruner.py
--rw-r--r--   0 runner    (1001) docker     (123)     2986 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/run_databases/file_system_run_databases_pruner.py
--rw-r--r--   0 runner    (1001) docker     (123)    16445 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/run_databases/run_databases_identifier.py
--rw-r--r--   0 runner    (1001) docker     (123)     5209 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/run_databases/run_databases_provider.py
--rw-r--r--   0 runner    (1001) docker     (123)     1301 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/run_databases/run_databases_pruning_factory.py
--rw-r--r--   0 runner    (1001) docker     (123)     2457 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/run_databases/storage.py
--rw-r--r--   0 runner    (1001) docker     (123)     3074 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/databases/run_databases/utils.py
--rw-r--r--   0 runner    (1001) docker     (123)     4943 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/dict_util.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.525565 OctoBot-Commons-1.9.5/octobot_commons/display/
--rw-r--r--   0 runner    (1001) docker     (123)     1222 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/display/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1225 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/display/display_factory.py
--rw-r--r--   0 runner    (1001) docker     (123)    20622 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/display/display_translator.py
--rw-r--r--   0 runner    (1001) docker     (123)     1133 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/display/plot_settings.py
--rw-r--r--   0 runner    (1001) docker     (123)    12776 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/enums.py
--rw-r--r--   0 runner    (1001) docker     (123)     2887 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/errors.py
--rw-r--r--   0 runner    (1001) docker     (123)     1777 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/evaluators_util.py
--rw-r--r--   0 runner    (1001) docker     (123)     2991 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/external_resources_manager.py
--rw-r--r--   0 runner    (1001) docker     (123)     2376 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/json_util.py
--rw-r--r--   0 runner    (1001) docker     (123)     1026 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/list_util.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.525565 OctoBot-Commons-1.9.5/octobot_commons/logging/
--rw-r--r--   0 runner    (1001) docker     (123)     1832 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/logging/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     9852 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/logging/logging_util.py
--rw-r--r--   0 runner    (1001) docker     (123)     1880 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/logical_operators.py
--rw-r--r--   0 runner    (1001) docker     (123)     2072 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/multiprocessing_util.py
--rw-r--r--   0 runner    (1001) docker     (123)     1582 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/number_util.py
--rw-r--r--   0 runner    (1001) docker     (123)     1664 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/optimization_campaign.py
--rw-r--r--   0 runner    (1001) docker     (123)     5620 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/os_clock_sync.py
--rw-r--r--   0 runner    (1001) docker     (123)     4217 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/os_util.py
--rw-r--r--   0 runner    (1001) docker     (123)    11279 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/pretty_printer.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.525565 OctoBot-Commons-1.9.5/octobot_commons/profiles/
--rw-r--r--   0 runner    (1001) docker     (123)     1212 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/profiles/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    16826 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/profiles/profile.py
--rw-r--r--   0 runner    (1001) docker     (123)    11952 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/profiles/profile_sharing.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.525565 OctoBot-Commons-1.9.5/octobot_commons/signals/
--rw-r--r--   0 runner    (1001) docker     (123)     1850 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/signals/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1176 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/signals/signal.py
--rw-r--r--   0 runner    (1001) docker     (123)     1754 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/signals/signal_builder_wrapper.py
--rw-r--r--   0 runner    (1001) docker     (123)     1683 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/signals/signal_bundle.py
--rw-r--r--   0 runner    (1001) docker     (123)     2196 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/signals/signal_bundle_builder.py
--rw-r--r--   0 runner    (1001) docker     (123)     1709 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/signals/signal_factory.py
--rw-r--r--   0 runner    (1001) docker     (123)     6334 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/signals/signal_publisher.py
--rw-r--r--   0 runner    (1001) docker     (123)     1213 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/signals/signals_emitter.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.525565 OctoBot-Commons-1.9.5/octobot_commons/singleton/
--rw-r--r--   0 runner    (1001) docker     (123)      868 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/singleton/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1636 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/singleton/singleton_class.py
--rw-r--r--   0 runner    (1001) docker     (123)      965 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/support.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.525565 OctoBot-Commons-1.9.5/octobot_commons/symbols/
--rw-r--r--   0 runner    (1001) docker     (123)     1116 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/symbols/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6948 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/symbols/symbol.py
--rw-r--r--   0 runner    (1001) docker     (123)     3502 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/symbols/symbol_util.py
--rw-r--r--   0 runner    (1001) docker     (123)     4667 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/system_resources_watcher.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.525565 OctoBot-Commons-1.9.5/octobot_commons/tentacles_management/
--rw-r--r--   0 runner    (1001) docker     (123)     1782 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/tentacles_management/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5683 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/tentacles_management/abstract_tentacle.py
--rw-r--r--   0 runner    (1001) docker     (123)     5277 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/tentacles_management/class_inspector.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.525565 OctoBot-Commons-1.9.5/octobot_commons/tests/
--rw-r--r--   0 runner    (1001) docker     (123)     1047 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/tests/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2118 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/tests/test_config.py
--rw-r--r--   0 runner    (1001) docker     (123)     1311 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/thread_util.py
--rw-r--r--   0 runner    (1001) docker     (123)     5367 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/time_frame_manager.py
--rw-r--r--   0 runner    (1001) docker     (123)     3307 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/timestamp_util.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.525565 OctoBot-Commons-1.9.5/octobot_commons/tree/
--rw-r--r--   0 runner    (1001) docker     (123)     1292 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/tree/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     9354 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/tree/base_tree.py
--rw-r--r--   0 runner    (1001) docker     (123)     4162 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/tree/event_provider.py
--rw-r--r--   0 runner    (1001) docker     (123)     6751 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/octobot_commons/tree/event_tree.py
--rw-r--r--   0 runner    (1001) docker     (123)      182 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/requirements.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-05-17 11:33:45.529565 OctoBot-Commons-1.9.5/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1985 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.517565 OctoBot-Commons-1.9.5/tests/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.525565 OctoBot-Commons-1.9.5/tests/configuration/
--rw-r--r--   0 runner    (1001) docker     (123)      716 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/configuration/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    12030 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/configuration/test_configuration.py
--rw-r--r--   0 runner    (1001) docker     (123)     1225 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/configuration/test_fields_util.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.525565 OctoBot-Commons-1.9.5/tests/databases/
--rw-r--r--   0 runner    (1001) docker     (123)       12 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/databases/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.525565 OctoBot-Commons-1.9.5/tests/databases/global_storage/
--rw-r--r--   0 runner    (1001) docker     (123)       12 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/databases/global_storage/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2989 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/databases/global_storage/test_global_shared_memory_storage.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.525565 OctoBot-Commons-1.9.5/tests/databases/relational_databases/
--rw-r--r--   0 runner    (1001) docker     (123)       12 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/databases/relational_databases/__init__.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.525565 OctoBot-Commons-1.9.5/tests/databases/relational_databases/sqlite/
--rw-r--r--   0 runner    (1001) docker     (123)       12 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/databases/relational_databases/sqlite/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    13446 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/databases/relational_databases/sqlite/test_sqlite_database.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.525565 OctoBot-Commons-1.9.5/tests/databases/run_databases/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/databases/run_databases/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1979 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/databases/run_databases/test_run_databases_provider.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.529565 OctoBot-Commons-1.9.5/tests/logging/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/logging/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2454 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/logging/test_logging_util.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.529565 OctoBot-Commons-1.9.5/tests/profiles/
--rw-r--r--   0 runner    (1001) docker     (123)     1205 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/profiles/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)    16320 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/profiles/test_profile.py
--rw-r--r--   0 runner    (1001) docker     (123)     9440 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/profiles/test_profile_sharing.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.529565 OctoBot-Commons-1.9.5/tests/signals/
--rw-r--r--   0 runner    (1001) docker     (123)     1864 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/signals/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1102 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/signals/test_signal.py
--rw-r--r--   0 runner    (1001) docker     (123)     2236 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/signals/test_signal_builder_wrapper.py
--rw-r--r--   0 runner    (1001) docker     (123)     1390 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/signals/test_signal_bundle.py
--rw-r--r--   0 runner    (1001) docker     (123)     2650 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/signals/test_signal_bundle_builder.py
--rw-r--r--   0 runner    (1001) docker     (123)     1439 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/signals/test_signal_factory.py
--rw-r--r--   0 runner    (1001) docker     (123)    10972 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/signals/test_signal_publisher.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.529565 OctoBot-Commons-1.9.5/tests/symbols/
--rw-r--r--   0 runner    (1001) docker     (123)       12 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/symbols/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     3402 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/symbols/test_symbol.py
--rw-r--r--   0 runner    (1001) docker     (123)     1496 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/symbols/test_symbol_util.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.529565 OctoBot-Commons-1.9.5/tests/tentacles_management/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/tentacles_management/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2315 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/tentacles_management/test_abstract_tentacle.py
--rw-r--r--   0 runner    (1001) docker     (123)     3316 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/tentacles_management/test_class_inspector.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:45.529565 OctoBot-Commons-1.9.5/tests/tree/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/tree/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6383 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/tree/test_base_tree.py
--rw-r--r--   0 runner    (1001) docker     (123)     5650 2023-05-17 11:33:14.000000 OctoBot-Commons-1.9.5/tests/tree/test_event_tree.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.722910 OctoBot-Commons-1.9.6/
+-rw-r--r--   0 runner    (1001) docker     (123)    19480 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/CHANGELOG.md
+-rw-r--r--   0 runner    (1001) docker     (123)     7652 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      141 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/MANIFEST.in
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.694910 OctoBot-Commons-1.9.6/OctoBot_Commons.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1831 2023-07-23 13:24:07.000000 OctoBot-Commons-1.9.6/OctoBot_Commons.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     6425 2023-07-23 13:24:07.000000 OctoBot-Commons-1.9.6/OctoBot_Commons.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 13:24:07.000000 OctoBot-Commons-1.9.6/OctoBot_Commons.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 13:24:07.000000 OctoBot-Commons-1.9.6/OctoBot_Commons.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (123)      109 2023-07-23 13:24:07.000000 OctoBot-Commons-1.9.6/OctoBot_Commons.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       22 2023-07-23 13:24:07.000000 OctoBot-Commons-1.9.6/OctoBot_Commons.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1831 2023-07-23 13:24:07.722910 OctoBot-Commons-1.9.6/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1198 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.694910 OctoBot-Commons-1.9.6/octobot_commons/
+-rw-r--r--   0 runner    (1001) docker     (123)      979 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1814 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/aiohttp_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10371 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/async_job.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4436 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/asyncio_tools.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5246 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/authentication.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2138 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/channels_name.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.694910 OctoBot-Commons-1.9.6/octobot_commons/configuration/
+-rw-r--r--   0 runner    (1001) docker     (123)     3070 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/configuration/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6914 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/configuration/config_file_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4574 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/configuration/config_operations.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12191 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/configuration/configuration.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3052 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/configuration/fields_utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5144 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/configuration/user_input_configuration.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10797 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/configuration/user_inputs.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6917 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/constants.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2122 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/data_util.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.698910 OctoBot-Commons-1.9.6/octobot_commons/databases/
+-rw-r--r--   0 runner    (1001) docker     (123)     3131 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.698910 OctoBot-Commons-1.9.6/octobot_commons/databases/bases/
+-rw-r--r--   0 runner    (1001) docker     (123)     1067 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/bases/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6416 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/bases/base_database.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6226 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/bases/document_database.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9482 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/cache_client.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16509 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/cache_manager.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.698910 OctoBot-Commons-1.9.6/octobot_commons/databases/database_caches/
+-rw-r--r--   0 runner    (1001) docker     (123)     1201 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/database_caches/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5588 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/database_caches/chronological_read_database_cache.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4885 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/database_caches/generic_database_cache.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.698910 OctoBot-Commons-1.9.6/octobot_commons/databases/databases_util/
+-rw-r--r--   0 runner    (1001) docker     (123)      874 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/databases_util/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2498 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/databases_util/cache_wrapper.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.698910 OctoBot-Commons-1.9.6/octobot_commons/databases/document_database_adaptors/
+-rw-r--r--   0 runner    (1001) docker     (123)     1229 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/document_database_adaptors/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7813 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/document_database_adaptors/abstract_document_database_adaptor.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11991 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/document_database_adaptors/tinydb_adaptor.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.698910 OctoBot-Commons-1.9.6/octobot_commons/databases/global_storage/
+-rw-r--r--   0 runner    (1001) docker     (123)      967 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/global_storage/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1481 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/global_storage/global_shared_memory_storage.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.702910 OctoBot-Commons-1.9.6/octobot_commons/databases/implementations/
+-rw-r--r--   0 runner    (1001) docker     (123)     1828 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/implementations/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5255 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/implementations/_exchange_database.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3759 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/implementations/cache_database.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8433 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/implementations/cache_timestamp_database.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1514 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/implementations/db_reader.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7873 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/implementations/db_writer.py
+-rw-r--r--   0 runner    (1001) docker     (123)      921 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/implementations/db_writer_reader.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6275 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/implementations/meta_database.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.702910 OctoBot-Commons-1.9.6/octobot_commons/databases/relational_databases/
+-rw-r--r--   0 runner    (1001) docker     (123)      988 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/relational_databases/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.702910 OctoBot-Commons-1.9.6/octobot_commons/databases/relational_databases/sqlite/
+-rw-r--r--   0 runner    (1001) docker     (123)      996 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/relational_databases/sqlite/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1878 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/relational_databases/sqlite/cursor_pool.py
+-rw-r--r--   0 runner    (1001) docker     (123)      951 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/relational_databases/sqlite/cursor_wrapper.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13195 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/relational_databases/sqlite/sqlite_database.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.706910 OctoBot-Commons-1.9.6/octobot_commons/databases/run_databases/
+-rw-r--r--   0 runner    (1001) docker     (123)     1790 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/run_databases/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5955 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/run_databases/abstract_run_databases_pruner.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2986 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/run_databases/file_system_run_databases_pruner.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16445 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/run_databases/run_databases_identifier.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5409 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/run_databases/run_databases_provider.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1301 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/run_databases/run_databases_pruning_factory.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2457 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/run_databases/storage.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3074 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/databases/run_databases/utils.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4943 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/dict_util.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.706910 OctoBot-Commons-1.9.6/octobot_commons/display/
+-rw-r--r--   0 runner    (1001) docker     (123)     1222 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/display/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1225 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/display/display_factory.py
+-rw-r--r--   0 runner    (1001) docker     (123)    20622 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/display/display_translator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1133 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/display/plot_settings.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12776 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/enums.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2887 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/errors.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1777 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/evaluators_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2991 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/external_resources_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2376 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/json_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1026 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/list_util.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.706910 OctoBot-Commons-1.9.6/octobot_commons/logging/
+-rw-r--r--   0 runner    (1001) docker     (123)     1832 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/logging/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9859 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/logging/logging_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1880 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/logical_operators.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2382 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/minimizable_dataclass.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2072 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/multiprocessing_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1582 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/number_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1664 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/optimization_campaign.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5620 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/os_clock_sync.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4217 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/os_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11280 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/pretty_printer.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.706910 OctoBot-Commons-1.9.6/octobot_commons/profiles/
+-rw-r--r--   0 runner    (1001) docker     (123)     1354 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/profiles/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16978 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/profiles/profile.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8921 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/profiles/profile_data.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11952 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/profiles/profile_sharing.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.710910 OctoBot-Commons-1.9.6/octobot_commons/signals/
+-rw-r--r--   0 runner    (1001) docker     (123)     1850 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/signals/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1176 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/signals/signal.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1754 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/signals/signal_builder_wrapper.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1683 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/signals/signal_bundle.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2196 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/signals/signal_bundle_builder.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1709 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/signals/signal_factory.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6334 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/signals/signal_publisher.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1213 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/signals/signals_emitter.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.710910 OctoBot-Commons-1.9.6/octobot_commons/singleton/
+-rw-r--r--   0 runner    (1001) docker     (123)      868 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/singleton/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1636 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/singleton/singleton_class.py
+-rw-r--r--   0 runner    (1001) docker     (123)      965 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/support.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.710910 OctoBot-Commons-1.9.6/octobot_commons/symbols/
+-rw-r--r--   0 runner    (1001) docker     (123)     1116 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/symbols/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6948 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/symbols/symbol.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3502 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/symbols/symbol_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4667 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/system_resources_watcher.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.710910 OctoBot-Commons-1.9.6/octobot_commons/tentacles_management/
+-rw-r--r--   0 runner    (1001) docker     (123)     1782 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/tentacles_management/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5683 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/tentacles_management/abstract_tentacle.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5277 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/tentacles_management/class_inspector.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.710910 OctoBot-Commons-1.9.6/octobot_commons/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     1047 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/tests/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2118 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/tests/test_config.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1311 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/thread_util.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5367 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/time_frame_manager.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3307 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/timestamp_util.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.714910 OctoBot-Commons-1.9.6/octobot_commons/tree/
+-rw-r--r--   0 runner    (1001) docker     (123)     1292 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/tree/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9354 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/tree/base_tree.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4333 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/tree/event_provider.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6751 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/octobot_commons/tree/event_tree.py
+-rw-r--r--   0 runner    (1001) docker     (123)      182 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/requirements.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 13:24:07.722910 OctoBot-Commons-1.9.6/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1985 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.690910 OctoBot-Commons-1.9.6/tests/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.714910 OctoBot-Commons-1.9.6/tests/configuration/
+-rw-r--r--   0 runner    (1001) docker     (123)      716 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/configuration/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12030 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/configuration/test_configuration.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1225 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/configuration/test_fields_util.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.714910 OctoBot-Commons-1.9.6/tests/databases/
+-rw-r--r--   0 runner    (1001) docker     (123)       12 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/databases/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.714910 OctoBot-Commons-1.9.6/tests/databases/global_storage/
+-rw-r--r--   0 runner    (1001) docker     (123)       12 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/databases/global_storage/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2989 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/databases/global_storage/test_global_shared_memory_storage.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.714910 OctoBot-Commons-1.9.6/tests/databases/relational_databases/
+-rw-r--r--   0 runner    (1001) docker     (123)       12 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/databases/relational_databases/__init__.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.714910 OctoBot-Commons-1.9.6/tests/databases/relational_databases/sqlite/
+-rw-r--r--   0 runner    (1001) docker     (123)       12 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/databases/relational_databases/sqlite/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    13446 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/databases/relational_databases/sqlite/test_sqlite_database.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.714910 OctoBot-Commons-1.9.6/tests/databases/run_databases/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/databases/run_databases/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1979 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/databases/run_databases/test_run_databases_provider.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.714910 OctoBot-Commons-1.9.6/tests/logging/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/logging/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2454 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/logging/test_logging_util.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.718910 OctoBot-Commons-1.9.6/tests/profiles/
+-rw-r--r--   0 runner    (1001) docker     (123)     1205 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/profiles/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)    16320 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/profiles/test_profile.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6765 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/profiles/test_profile_data.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9440 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/profiles/test_profile_sharing.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.718910 OctoBot-Commons-1.9.6/tests/signals/
+-rw-r--r--   0 runner    (1001) docker     (123)     1864 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/signals/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1102 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/signals/test_signal.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2236 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/signals/test_signal_builder_wrapper.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1390 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/signals/test_signal_bundle.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2650 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/signals/test_signal_bundle_builder.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1439 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/signals/test_signal_factory.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10972 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/signals/test_signal_publisher.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.718910 OctoBot-Commons-1.9.6/tests/symbols/
+-rw-r--r--   0 runner    (1001) docker     (123)       12 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/symbols/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3402 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/symbols/test_symbol.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1496 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/symbols/test_symbol_util.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.718910 OctoBot-Commons-1.9.6/tests/tentacles_management/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/tentacles_management/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2315 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/tentacles_management/test_abstract_tentacle.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3316 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/tentacles_management/test_class_inspector.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 13:24:07.722910 OctoBot-Commons-1.9.6/tests/tree/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/tree/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6383 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/tree/test_base_tree.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5650 2023-07-23 13:23:37.000000 OctoBot-Commons-1.9.6/tests/tree/test_event_tree.py
```

### Comparing `OctoBot-Commons-1.9.5/CHANGELOG.md` & `OctoBot-Commons-1.9.6/CHANGELOG.md`

 * *Files 0% similar despite different names*

```diff
@@ -1,13 +1,18 @@
 # Changelog
 All notable changes to this project will be documented in this file.
 
 The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
 and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).
 
+## [1.9.6] - 2023-07-22
+### Added
+- ProfileData
+- Singletons: add remove methods
+
 ## [1.9.5] - 2023-05-17
 ### Added
 - DEPENDENCIES to UserInputOtherSchemaValuesTypes
 ### Fixed
 - sqlite close error
 - threadpool stop
```

### Comparing `OctoBot-Commons-1.9.5/LICENSE` & `OctoBot-Commons-1.9.6/LICENSE`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/OctoBot_Commons.egg-info/PKG-INFO` & `OctoBot-Commons-1.9.6/OctoBot_Commons.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: OctoBot-Commons
-Version: 1.9.5
+Version: 1.9.6
 Summary: OctoBot project common modules
 Home-page: https://github.com/Drakkar-Software/OctoBot-Commons
 Author: Drakkar-Software
 Author-email: contact@drakkar.software
 License: LGPL-3.0
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Operating System :: OS Independent
@@ -12,15 +12,15 @@
 Classifier: Operating System :: Microsoft :: Windows
 Classifier: Operating System :: POSIX
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Requires-Python: >=3.8
 License-File: LICENSE
 
-# OctoBot-Commons [1.9.5](https://github.com/Drakkar-Software/OctoBot-Commons/blob/master/CHANGELOG.md)
+# OctoBot-Commons [1.9.6](https://github.com/Drakkar-Software/OctoBot-Commons/blob/master/CHANGELOG.md)
 [![Codacy Badge](https://api.codacy.com/project/badge/Grade/b31f3ab3511744a5a5ca6b9bb48e77bb)](https://app.codacy.com/gh/Drakkar-Software/OctoBot-Commons?utm_source=github.com&utm_medium=referral&utm_content=Drakkar-Software/OctoBot-Commons&utm_campaign=Badge_Grade_Dashboard)
 [![PyPI](https://img.shields.io/pypi/v/OctoBot-Commons.svg)](https://pypi.python.org/pypi/OctoBot-Commons/)
 [![Coverage Status](https://coveralls.io/repos/github/Drakkar-Software/OctoBot-Commons/badge.svg?branch=master)](https://coveralls.io/github/Drakkar-Software/OctoBot-Commons?branch=master)
 [![Github-Action-CI](https://github.com/Drakkar-Software/OctoBot-Commons/workflows/Github-Action-CI/badge.svg)](https://github.com/Drakkar-Software/OctoBot-Commons/actions)
 [![Build Status](https://cloud.drone.io/api/badges/Drakkar-Software/OctoBot-Commons/status.svg)](https://cloud.drone.io/Drakkar-Software/OctoBot-Commons)
 [![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
```

### Comparing `OctoBot-Commons-1.9.5/OctoBot_Commons.egg-info/SOURCES.txt` & `OctoBot-Commons-1.9.6/OctoBot_Commons.egg-info/SOURCES.txt`

 * *Files 4% similar despite different names*

```diff
@@ -22,14 +22,15 @@
 octobot_commons/enums.py
 octobot_commons/errors.py
 octobot_commons/evaluators_util.py
 octobot_commons/external_resources_manager.py
 octobot_commons/json_util.py
 octobot_commons/list_util.py
 octobot_commons/logical_operators.py
+octobot_commons/minimizable_dataclass.py
 octobot_commons/multiprocessing_util.py
 octobot_commons/number_util.py
 octobot_commons/optimization_campaign.py
 octobot_commons/os_clock_sync.py
 octobot_commons/os_util.py
 octobot_commons/pretty_printer.py
 octobot_commons/support.py
@@ -85,14 +86,15 @@
 octobot_commons/display/display_factory.py
 octobot_commons/display/display_translator.py
 octobot_commons/display/plot_settings.py
 octobot_commons/logging/__init__.py
 octobot_commons/logging/logging_util.py
 octobot_commons/profiles/__init__.py
 octobot_commons/profiles/profile.py
+octobot_commons/profiles/profile_data.py
 octobot_commons/profiles/profile_sharing.py
 octobot_commons/signals/__init__.py
 octobot_commons/signals/signal.py
 octobot_commons/signals/signal_builder_wrapper.py
 octobot_commons/signals/signal_bundle.py
 octobot_commons/signals/signal_bundle_builder.py
 octobot_commons/signals/signal_factory.py
@@ -123,14 +125,15 @@
 tests/databases/relational_databases/sqlite/test_sqlite_database.py
 tests/databases/run_databases/__init__.py
 tests/databases/run_databases/test_run_databases_provider.py
 tests/logging/__init__.py
 tests/logging/test_logging_util.py
 tests/profiles/__init__.py
 tests/profiles/test_profile.py
+tests/profiles/test_profile_data.py
 tests/profiles/test_profile_sharing.py
 tests/signals/__init__.py
 tests/signals/test_signal.py
 tests/signals/test_signal_builder_wrapper.py
 tests/signals/test_signal_bundle.py
 tests/signals/test_signal_bundle_builder.py
 tests/signals/test_signal_factory.py
```

### Comparing `OctoBot-Commons-1.9.5/PKG-INFO` & `OctoBot-Commons-1.9.6/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: OctoBot-Commons
-Version: 1.9.5
+Version: 1.9.6
 Summary: OctoBot project common modules
 Home-page: https://github.com/Drakkar-Software/OctoBot-Commons
 Author: Drakkar-Software
 Author-email: contact@drakkar.software
 License: LGPL-3.0
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Operating System :: OS Independent
@@ -12,15 +12,15 @@
 Classifier: Operating System :: Microsoft :: Windows
 Classifier: Operating System :: POSIX
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Requires-Python: >=3.8
 License-File: LICENSE
 
-# OctoBot-Commons [1.9.5](https://github.com/Drakkar-Software/OctoBot-Commons/blob/master/CHANGELOG.md)
+# OctoBot-Commons [1.9.6](https://github.com/Drakkar-Software/OctoBot-Commons/blob/master/CHANGELOG.md)
 [![Codacy Badge](https://api.codacy.com/project/badge/Grade/b31f3ab3511744a5a5ca6b9bb48e77bb)](https://app.codacy.com/gh/Drakkar-Software/OctoBot-Commons?utm_source=github.com&utm_medium=referral&utm_content=Drakkar-Software/OctoBot-Commons&utm_campaign=Badge_Grade_Dashboard)
 [![PyPI](https://img.shields.io/pypi/v/OctoBot-Commons.svg)](https://pypi.python.org/pypi/OctoBot-Commons/)
 [![Coverage Status](https://coveralls.io/repos/github/Drakkar-Software/OctoBot-Commons/badge.svg?branch=master)](https://coveralls.io/github/Drakkar-Software/OctoBot-Commons?branch=master)
 [![Github-Action-CI](https://github.com/Drakkar-Software/OctoBot-Commons/workflows/Github-Action-CI/badge.svg)](https://github.com/Drakkar-Software/OctoBot-Commons/actions)
 [![Build Status](https://cloud.drone.io/api/badges/Drakkar-Software/OctoBot-Commons/status.svg)](https://cloud.drone.io/Drakkar-Software/OctoBot-Commons)
 [![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
```

### Comparing `OctoBot-Commons-1.9.5/README.md` & `OctoBot-Commons-1.9.6/README.md`

 * *Files 0% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-# OctoBot-Commons [1.9.5](https://github.com/Drakkar-Software/OctoBot-Commons/blob/master/CHANGELOG.md)
+# OctoBot-Commons [1.9.6](https://github.com/Drakkar-Software/OctoBot-Commons/blob/master/CHANGELOG.md)
 [![Codacy Badge](https://api.codacy.com/project/badge/Grade/b31f3ab3511744a5a5ca6b9bb48e77bb)](https://app.codacy.com/gh/Drakkar-Software/OctoBot-Commons?utm_source=github.com&utm_medium=referral&utm_content=Drakkar-Software/OctoBot-Commons&utm_campaign=Badge_Grade_Dashboard)
 [![PyPI](https://img.shields.io/pypi/v/OctoBot-Commons.svg)](https://pypi.python.org/pypi/OctoBot-Commons/)
 [![Coverage Status](https://coveralls.io/repos/github/Drakkar-Software/OctoBot-Commons/badge.svg?branch=master)](https://coveralls.io/github/Drakkar-Software/OctoBot-Commons?branch=master)
 [![Github-Action-CI](https://github.com/Drakkar-Software/OctoBot-Commons/workflows/Github-Action-CI/badge.svg)](https://github.com/Drakkar-Software/OctoBot-Commons/actions)
 [![Build Status](https://cloud.drone.io/api/badges/Drakkar-Software/OctoBot-Commons/status.svg)](https://cloud.drone.io/Drakkar-Software/OctoBot-Commons)
 [![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
```

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/__init__.py` & `OctoBot-Commons-1.9.6/octobot_commons/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -12,14 +12,14 @@
 #  MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
 #  Lesser General Public License for more details.
 #
 #  You should have received a copy of the GNU Lesser General Public
 #  License along with this library.
 
 PROJECT_NAME = "OctoBot-Commons"
-VERSION = "1.9.5"  # major.minor.revision
+VERSION = "1.9.6"  # major.minor.revision
 
 MARKET_SEPARATOR = "/"
 SETTLEMENT_ASSET_SEPARATOR = ":"
 DICT_BULLET_TOKEN_STR = "\n "
 
 OCTOBOT_KEY = b"uVEw_JJe7uiXepaU_DR4T-ThkjZlDn8Pzl8hYPIv7w0="  # TODO temp
```

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/aiohttp_util.py` & `OctoBot-Commons-1.9.6/octobot_commons/aiohttp_util.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/async_job.py` & `OctoBot-Commons-1.9.6/octobot_commons/async_job.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/asyncio_tools.py` & `OctoBot-Commons-1.9.6/octobot_commons/asyncio_tools.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/authentication.py` & `OctoBot-Commons-1.9.6/octobot_commons/authentication.py`

 * *Files 3% similar despite different names*

```diff
@@ -31,15 +31,23 @@
         self.logger: bot_logging.BotLogger = bot_logging.get_logger(
             self.__class__.__name__
         )
         self.initialized_event: asyncio.Event = None
         self.supports: None
         self.feed_callbacks = {}
         # also register this instance for the base Authenticator class in singleton
+        self.use_as_singleton_instance()
+
+    # pylint: disable=W0212
+    def use_as_singleton_instance(self):
+        """
+        Update the Authenticator Singleton to use self
+        """
         singleton.Singleton._instances[Authenticator] = self
+        singleton.Singleton._instances[self.__class__] = self
 
     @abc.abstractmethod
     async def login(self, username, password, password_token=None):
         """
         Used to trigger a login
         :param username: authentication username
         :param password: authentication password
@@ -119,15 +127,15 @@
     async def await_initialization(self, timeout):
         """
         Returns when initialized
         :return:
         """
         await asyncio.wait_for(self.initialized_event.wait(), timeout)
 
-    async def update_trades(self, trades: list, reset: bool):
+    async def update_trades(self, trades: list, exchange_name: str, reset: bool):
         """
         Updates authenticated account trades
         """
         raise NotImplementedError
 
     async def update_portfolio(
         self,
```

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/channels_name.py` & `OctoBot-Commons-1.9.6/octobot_commons/channels_name.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/configuration/__init__.py` & `OctoBot-Commons-1.9.6/octobot_commons/configuration/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/configuration/config_file_manager.py` & `OctoBot-Commons-1.9.6/octobot_commons/configuration/config_file_manager.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/configuration/config_operations.py` & `OctoBot-Commons-1.9.6/octobot_commons/configuration/config_operations.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/configuration/configuration.py` & `OctoBot-Commons-1.9.6/octobot_commons/configuration/configuration.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/configuration/fields_utils.py` & `OctoBot-Commons-1.9.6/octobot_commons/configuration/fields_utils.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/configuration/user_input_configuration.py` & `OctoBot-Commons-1.9.6/octobot_commons/configuration/user_input_configuration.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/configuration/user_inputs.py` & `OctoBot-Commons-1.9.6/octobot_commons/configuration/user_inputs.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/constants.py` & `OctoBot-Commons-1.9.6/octobot_commons/constants.py`

 * *Files 1% similar despite different names*

```diff
@@ -107,14 +107,15 @@
 CONFIG_TRADER = "trader"
 CONFIG_LOAD_TRADE_HISTORY = "load-trade-history"
 CONFIG_TRADER_RISK = "risk"
 CONFIG_TRADER_ALLOW_ARTIFICIAL_ORDERS = "allow-artificial-orders"
 CONFIG_TRADER_RISK_MIN = 0.05
 CONFIG_TRADER_RISK_MAX = 1
 CONFIG_TRADER_REFERENCE_MARKET = "reference-market"
+DEFAULT_STORAGE_TRADING_MODE = "default"
 
 # Simulator
 CONFIG_SIMULATOR = "trader-simulator"
 CONFIG_STARTING_PORTFOLIO = "starting-portfolio"
 SIMULATOR_CURRENT_PORTFOLIO = "simulator_current_portfolio"
 CONFIG_SIMULATOR_FEES = "fees"
 CONFIG_SIMULATOR_FEES_MAKER = "maker"
@@ -147,14 +148,15 @@
 DEFAULT_EVALUATOR_PRIORITY = 0
 CONFIG_TENTACLES_REQUIRED_CANDLES_COUNT = "required_candles_count"
 NESTED_TENTACLE_CONFIG = "nested_tentacle_configuration"
 CONFIG_ACTIVATION_TOPICS = "activation method"
 CONFIG_TRIGGER_TIMEFRAMES = "Trigger_timeframes"
 CONFIG_EMIT_TRADING_SIGNALS = "emit_trading_signals"
 CONFIG_TRADING_SIGNALS_STRATEGY = "trading_strategy"
+ALLOW_DEFAULT_CONFIG = "allow_default_config"
 
 # terms of service
 CONFIG_ACCEPTED_TERMS = "accepted_terms"
 
 # metrics
 CONFIG_METRICS = "metrics"
 CONFIG_METRICS_BOT_ID = "metrics-bot-id"
```

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/data_util.py` & `OctoBot-Commons-1.9.6/octobot_commons/data_util.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/__init__.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/bases/__init__.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/bases/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/bases/base_database.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/bases/base_database.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/bases/document_database.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/bases/document_database.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/cache_client.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/cache_client.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/cache_manager.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/cache_manager.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/database_caches/__init__.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/database_caches/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/database_caches/chronological_read_database_cache.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/database_caches/chronological_read_database_cache.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/database_caches/generic_database_cache.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/database_caches/generic_database_cache.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/databases_util/__init__.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/databases_util/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/databases_util/cache_wrapper.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/databases_util/cache_wrapper.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/document_database_adaptors/__init__.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/document_database_adaptors/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/document_database_adaptors/abstract_document_database_adaptor.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/document_database_adaptors/abstract_document_database_adaptor.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/document_database_adaptors/tinydb_adaptor.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/document_database_adaptors/tinydb_adaptor.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/global_storage/__init__.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/global_storage/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/global_storage/global_shared_memory_storage.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/global_storage/global_shared_memory_storage.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/implementations/__init__.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/implementations/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/implementations/_exchange_database.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/implementations/_exchange_database.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/implementations/cache_database.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/implementations/cache_database.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/implementations/cache_timestamp_database.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/implementations/cache_timestamp_database.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/implementations/db_reader.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/implementations/db_reader.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/implementations/db_writer.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/implementations/db_writer.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/implementations/db_writer_reader.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/implementations/db_writer_reader.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/implementations/meta_database.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/implementations/meta_database.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/relational_databases/__init__.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/relational_databases/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/relational_databases/sqlite/__init__.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/relational_databases/sqlite/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/relational_databases/sqlite/cursor_pool.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/relational_databases/sqlite/cursor_pool.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/relational_databases/sqlite/cursor_wrapper.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/relational_databases/sqlite/cursor_wrapper.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/relational_databases/sqlite/sqlite_database.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/relational_databases/sqlite/sqlite_database.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/run_databases/__init__.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/run_databases/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/run_databases/abstract_run_databases_pruner.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/run_databases/abstract_run_databases_pruner.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/run_databases/file_system_run_databases_pruner.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/run_databases/file_system_run_databases_pruner.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/run_databases/run_databases_identifier.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/run_databases/run_databases_identifier.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/run_databases/run_databases_provider.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/run_databases/run_databases_provider.py`

 * *Files 4% similar despite different names*

```diff
@@ -37,14 +37,21 @@
 
     def has_bot_id(self, bot_id):
         """
         :return: True if the given bot_id has been added via add_bot_id
         """
         return bot_id in self.run_databases
 
+    def remove_bot_id(self, bot_id):
+        """
+        remove the run database from the given bot_id
+        :return: the removed database
+        """
+        return self.run_databases.pop(bot_id)
+
     def is_storage_enabled(self, bot_id):
         """
         :return: True if storage is enabled for the given bot_id
         """
         return self.run_databases[bot_id].run_dbs_identifier.enable_storage
 
     def get_any_run_databases_identifier(self):
```

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/run_databases/run_databases_pruning_factory.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/run_databases/run_databases_pruning_factory.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/run_databases/storage.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/run_databases/storage.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/databases/run_databases/utils.py` & `OctoBot-Commons-1.9.6/octobot_commons/databases/run_databases/utils.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/dict_util.py` & `OctoBot-Commons-1.9.6/octobot_commons/dict_util.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/display/__init__.py` & `OctoBot-Commons-1.9.6/octobot_commons/display/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/display/display_factory.py` & `OctoBot-Commons-1.9.6/octobot_commons/display/display_factory.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/display/display_translator.py` & `OctoBot-Commons-1.9.6/octobot_commons/display/display_translator.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/display/plot_settings.py` & `OctoBot-Commons-1.9.6/octobot_commons/display/plot_settings.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/enums.py` & `OctoBot-Commons-1.9.6/octobot_commons/enums.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/errors.py` & `OctoBot-Commons-1.9.6/octobot_commons/errors.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/evaluators_util.py` & `OctoBot-Commons-1.9.6/octobot_commons/evaluators_util.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/external_resources_manager.py` & `OctoBot-Commons-1.9.6/octobot_commons/external_resources_manager.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/json_util.py` & `OctoBot-Commons-1.9.6/octobot_commons/json_util.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/list_util.py` & `OctoBot-Commons-1.9.6/octobot_commons/list_util.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/logging/__init__.py` & `OctoBot-Commons-1.9.6/octobot_commons/logging/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/logging/logging_util.py` & `OctoBot-Commons-1.9.6/octobot_commons/logging/logging_util.py`

 * *Files 0% similar despite different names*

```diff
@@ -211,15 +211,15 @@
         if publish_error_if_necessary:
             message = error_message
             if message is None:
                 message = (
                     str(exception) if str(exception) else exception.__class__.__name__
                 )
             elif include_exception_name:
-                message = f"{message} ({exception.__class__.__name__})"
+                message = f"{message} (error: {exception.__class__.__name__})"
             self.error(message, skip_post_callback=True)
         self._post_callback_if_necessary(exception, error_message, skip_post_callback)
 
     def critical(self, message, *args, **kwargs) -> None:
         """
         Called for a critical log
         :param message: the log message
```

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/logical_operators.py` & `OctoBot-Commons-1.9.6/octobot_commons/logical_operators.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/multiprocessing_util.py` & `OctoBot-Commons-1.9.6/octobot_commons/multiprocessing_util.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/number_util.py` & `OctoBot-Commons-1.9.6/octobot_commons/number_util.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/optimization_campaign.py` & `OctoBot-Commons-1.9.6/octobot_commons/optimization_campaign.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/os_clock_sync.py` & `OctoBot-Commons-1.9.6/octobot_commons/os_clock_sync.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/os_util.py` & `OctoBot-Commons-1.9.6/octobot_commons/os_util.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/pretty_printer.py` & `OctoBot-Commons-1.9.6/octobot_commons/pretty_printer.py`

 * *Files 0% similar despite different names*

```diff
@@ -146,15 +146,15 @@
     abs_number = abs(number)
     if abs_number < 0.0001:
         return 8
     if abs_number < 0.01:
         return 6
     if abs_number < 1:
         return 4
-    if abs_number < 1000:
+    if abs_number < 10000:
         return 2
     return 0
 
 
 def _get_markdown_pretty_portfolio_row(
     holdings, currency, ref_market, ref_market_value
 ):
```

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/profiles/__init__.py` & `OctoBot-Commons-1.9.6/octobot_commons/profiles/__init__.py`

 * *Files 6% similar despite different names*

```diff
@@ -26,16 +26,23 @@
     export_profile,
     install_profile,
     import_profile,
     download_profile,
     download_and_install_profile,
 )
 
+from octobot_commons.profiles import profile_data
+
+from octobot_commons.profiles.profile_data import (
+    ProfileData,
+)
+
 
 __all__ = [
     "Profile",
     "export_profile",
     "install_profile",
     "import_profile",
     "download_profile",
     "download_and_install_profile",
+    "ProfileData",
 ]
```

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/profiles/profile.py` & `OctoBot-Commons-1.9.6/octobot_commons/profiles/profile.py`

 * *Files 1% similar despite different names*

```diff
@@ -77,16 +77,22 @@
         self.config: dict = {}
 
     def read_config(self):
         """
         Reads a profile from self.path
         :return: self
         """
-        parsed_profile = json_util.read_file(self.config_file())
-        profile_config = parsed_profile.get(constants.CONFIG_PROFILE, {})
+        return self.from_dict(json_util.read_file(self.config_file()))
+
+    def from_dict(self, profile_dict: dict):
+        """
+        Reads a profile from the given dict
+        :return: self
+        """
+        profile_config = profile_dict.get(constants.CONFIG_PROFILE, {})
         self.profile_id = profile_config.get(constants.CONFIG_ID, str(uuid.uuid4()))
         self.name = profile_config.get(constants.CONFIG_NAME, "")
         self.description = profile_config.get(constants.CONFIG_DESCRIPTION, "")
         self.avatar = profile_config.get(constants.CONFIG_AVATAR, "")
         self.origin_url = profile_config.get(constants.CONFIG_ORIGIN_URL, None)
         self.read_only = profile_config.get(constants.CONFIG_READ_ONLY, False)
         self.imported = profile_config.get(constants.CONFIG_IMPORTED, False)
@@ -97,16 +103,16 @@
         )
         self.risk = enums.ProfileRisk(
             profile_config.get(constants.CONFIG_RISK, enums.ProfileRisk.MODERATE.value)
         )
         self.profile_type = enums.ProfileType(
             profile_config.get(constants.CONFIG_TYPE, enums.ProfileType.LIVE.value)
         )
-        self.config = parsed_profile[constants.PROFILE_CONFIG]
-        if self.avatar:
+        self.config = profile_dict[constants.PROFILE_CONFIG]
+        if self.avatar and self.path:
             avatar_path = os.path.join(self.path, self.avatar)
             if os.path.isfile(avatar_path):
                 self.avatar_path = avatar_path
         return self
 
     def save_config(self, global_config: dict):
         """
```

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/profiles/profile_sharing.py` & `OctoBot-Commons-1.9.6/octobot_commons/profiles/profile_sharing.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/signals/__init__.py` & `OctoBot-Commons-1.9.6/octobot_commons/signals/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/signals/signal.py` & `OctoBot-Commons-1.9.6/octobot_commons/signals/signal.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/signals/signal_builder_wrapper.py` & `OctoBot-Commons-1.9.6/octobot_commons/signals/signal_builder_wrapper.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/signals/signal_bundle.py` & `OctoBot-Commons-1.9.6/octobot_commons/signals/signal_bundle.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/signals/signal_bundle_builder.py` & `OctoBot-Commons-1.9.6/octobot_commons/signals/signal_bundle_builder.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/signals/signal_factory.py` & `OctoBot-Commons-1.9.6/octobot_commons/signals/signal_factory.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/signals/signal_publisher.py` & `OctoBot-Commons-1.9.6/octobot_commons/signals/signal_publisher.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/signals/signals_emitter.py` & `OctoBot-Commons-1.9.6/octobot_commons/signals/signals_emitter.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/singleton/__init__.py` & `OctoBot-Commons-1.9.6/octobot_commons/singleton/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/singleton/singleton_class.py` & `OctoBot-Commons-1.9.6/octobot_commons/singleton/singleton_class.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/support.py` & `OctoBot-Commons-1.9.6/octobot_commons/support.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/symbols/__init__.py` & `OctoBot-Commons-1.9.6/octobot_commons/symbols/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/symbols/symbol.py` & `OctoBot-Commons-1.9.6/octobot_commons/symbols/symbol.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/symbols/symbol_util.py` & `OctoBot-Commons-1.9.6/octobot_commons/symbols/symbol_util.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/system_resources_watcher.py` & `OctoBot-Commons-1.9.6/octobot_commons/system_resources_watcher.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/tentacles_management/__init__.py` & `OctoBot-Commons-1.9.6/octobot_commons/tentacles_management/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/tentacles_management/abstract_tentacle.py` & `OctoBot-Commons-1.9.6/octobot_commons/tentacles_management/abstract_tentacle.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/tentacles_management/class_inspector.py` & `OctoBot-Commons-1.9.6/octobot_commons/tentacles_management/class_inspector.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/tests/__init__.py` & `OctoBot-Commons-1.9.6/octobot_commons/tests/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/tests/test_config.py` & `OctoBot-Commons-1.9.6/octobot_commons/tests/test_config.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/thread_util.py` & `OctoBot-Commons-1.9.6/octobot_commons/thread_util.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/time_frame_manager.py` & `OctoBot-Commons-1.9.6/octobot_commons/time_frame_manager.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/timestamp_util.py` & `OctoBot-Commons-1.9.6/octobot_commons/timestamp_util.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/tree/__init__.py` & `OctoBot-Commons-1.9.6/octobot_commons/tree/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/tree/base_tree.py` & `OctoBot-Commons-1.9.6/octobot_commons/tree/base_tree.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/tree/event_provider.py` & `OctoBot-Commons-1.9.6/octobot_commons/tree/event_provider.py`

 * *Files 9% similar despite different names*

```diff
@@ -76,14 +76,20 @@
 
     def create_event_tree(self, bot_id):
         """
         Create a new event tree for the given bot_id
         """
         self._event_tree_by_bot_id[bot_id] = event_tree.EventTree()
 
+    def remove_event_tree(self, bot_id):
+        """
+        Removes the event tree for the given bot_id
+        """
+        self._event_tree_by_bot_id.pop(bot_id, None)
+
     async def wait_for_event(self, bot_id, path, timeout) -> bool:
         """
         Wait for the event at the given path for the given bot_id.
         Returns instantly if the path doesn't lead to an event or if timeout is 0
         :return: False if the event is not triggered after timeout
         """
         try:
```

### Comparing `OctoBot-Commons-1.9.5/octobot_commons/tree/event_tree.py` & `OctoBot-Commons-1.9.6/octobot_commons/tree/event_tree.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/setup.py` & `OctoBot-Commons-1.9.6/setup.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/tests/configuration/__init__.py` & `OctoBot-Commons-1.9.6/tests/configuration/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/tests/configuration/test_configuration.py` & `OctoBot-Commons-1.9.6/tests/configuration/test_configuration.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/tests/configuration/test_fields_util.py` & `OctoBot-Commons-1.9.6/tests/configuration/test_fields_util.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/tests/databases/global_storage/test_global_shared_memory_storage.py` & `OctoBot-Commons-1.9.6/tests/databases/global_storage/test_global_shared_memory_storage.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/tests/databases/relational_databases/sqlite/test_sqlite_database.py` & `OctoBot-Commons-1.9.6/tests/databases/relational_databases/sqlite/test_sqlite_database.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/tests/databases/run_databases/test_run_databases_provider.py` & `OctoBot-Commons-1.9.6/tests/databases/run_databases/test_run_databases_provider.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/tests/logging/test_logging_util.py` & `OctoBot-Commons-1.9.6/tests/logging/test_logging_util.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/tests/profiles/__init__.py` & `OctoBot-Commons-1.9.6/tests/profiles/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/tests/profiles/test_profile.py` & `OctoBot-Commons-1.9.6/tests/profiles/test_profile.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/tests/profiles/test_profile_sharing.py` & `OctoBot-Commons-1.9.6/tests/profiles/test_profile_sharing.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/tests/signals/__init__.py` & `OctoBot-Commons-1.9.6/tests/signals/__init__.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/tests/signals/test_signal.py` & `OctoBot-Commons-1.9.6/tests/signals/test_signal.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/tests/signals/test_signal_builder_wrapper.py` & `OctoBot-Commons-1.9.6/tests/signals/test_signal_builder_wrapper.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/tests/signals/test_signal_bundle.py` & `OctoBot-Commons-1.9.6/tests/signals/test_signal_bundle.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/tests/signals/test_signal_bundle_builder.py` & `OctoBot-Commons-1.9.6/tests/signals/test_signal_bundle_builder.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/tests/signals/test_signal_factory.py` & `OctoBot-Commons-1.9.6/tests/signals/test_signal_factory.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/tests/signals/test_signal_publisher.py` & `OctoBot-Commons-1.9.6/tests/signals/test_signal_publisher.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/tests/symbols/test_symbol.py` & `OctoBot-Commons-1.9.6/tests/symbols/test_symbol.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/tests/symbols/test_symbol_util.py` & `OctoBot-Commons-1.9.6/tests/symbols/test_symbol_util.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/tests/tentacles_management/test_abstract_tentacle.py` & `OctoBot-Commons-1.9.6/tests/tentacles_management/test_abstract_tentacle.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/tests/tentacles_management/test_class_inspector.py` & `OctoBot-Commons-1.9.6/tests/tentacles_management/test_class_inspector.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/tests/tree/test_base_tree.py` & `OctoBot-Commons-1.9.6/tests/tree/test_base_tree.py`

 * *Files identical despite different names*

### Comparing `OctoBot-Commons-1.9.5/tests/tree/test_event_tree.py` & `OctoBot-Commons-1.9.6/tests/tree/test_event_tree.py`

 * *Files identical despite different names*

