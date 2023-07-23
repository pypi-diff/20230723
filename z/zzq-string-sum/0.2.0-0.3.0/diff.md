# Comparing `tmp/zzq_string_sum-0.2.0.tar.gz` & `tmp/zzq_string_sum-0.3.0.tar.gz`

## Comparing `zzq_string_sum-0.2.0.tar` & `zzq_string_sum-0.3.0.tar`

### file list

```diff
@@ -1,94 +1,91 @@
--rw-r--r--   0        0        0     1428 1970-01-01 00:00:00.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/Cargo.toml
--rw-r--r--   0     1001      123       60 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/README.md
--rw-r--r--   0     1001      123       23 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/bo/README.md
--rw-r--r--   0     1001      123      437 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/bo/data_objects_manager.rs
--rw-r--r--   0     1001      123      326 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/bo/datasheet.rs
--rw-r--r--   0     1001      123      134 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/bo/mod.rs
--rw-r--r--   0     1001      123      336 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/bo/space.rs
--rw-r--r--   0     1001      123      536 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/bo/tests.rs
--rw-r--r--   0     1001      123       59 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/bo/types.rs
--rw-r--r--   0     1001      123     1472 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/lib.rs
--rw-r--r--   0     1001      123       80 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/ot/README.md
--rw-r--r--   0     1001      123       31 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/ot/actions/add_records.rs
--rw-r--r--   0     1001      123        1 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/ot/changeset.rs
--rw-r--r--   0     1001      123      113 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/ot/commands/add_records.rs
--rw-r--r--   0     1001      123     5992 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/ot/commands/colla_command_name.rs
--rw-r--r--   0     1001      123     8076 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/ot/commands/command_manager.rs
--rw-r--r--   0     1001      123      176 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/ot/commands/mod.rs
--rw-r--r--   0     1001      123       87 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/ot/commands/types.rs
--rw-r--r--   0     1001      123        1 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/ot/events/mod.rs
--rw-r--r--   0     1001      123      133 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/ot/mod.rs
--rw-r--r--   0     1001      123      677 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/ot/tests.rs
--rw-r--r--   0     1001      123     5866 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/shared/consts.rs
--rw-r--r--   0     1001      123      423 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/shared/container.rs
--rw-r--r--   0     1001      123      494 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/shared/errors.rs
--rw-r--r--   0     1001      123     6304 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/shared/json.rs
--rw-r--r--   0     1001      123      360 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/shared/logging.rs
--rw-r--r--   0     1001      123     2246 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/shared/macros.rs
--rw-r--r--   0     1001      123      270 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/shared/mod.rs
--rw-r--r--   0     1001      123      518 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/shared/option.rs
--rw-r--r--   0     1001      123      333 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/shared/slice.rs
--rw-r--r--   0     1001      123      443 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/shared/sql.rs
--rw-r--r--   0     1001      123       22 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/so/README.md
--rw-r--r--   0     1001      123     1702 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/so/data_bundle.rs
--rw-r--r--   0     1001      123     2002 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/so/data_functions_manager.rs
--rw-r--r--   0     1001      123        0 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/so/fields/mod.rs
--rw-r--r--   0     1001      123        0 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/so/formula/mod.rs
--rw-r--r--   0     1001      123      146 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/so/mod.rs
--rw-r--r--   0     1001      123     2389 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/so/types.rs
--rw-r--r--   0     1001      123     2319 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/types/dao.rs
--rw-r--r--   0     1001      123     5398 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/types/database.rs
--rw-r--r--   0     1001      123     4374 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/types/mod.rs
--rw-r--r--   0     1001      123     1234 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/types/node.rs
--rw-r--r--   0     1001      123      643 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/types/result.rs
--rw-r--r--   0     1001      123     3278 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/types/types2.rs
--rw-r--r--   0     1001      123     1003 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/src/types/unit.rs
--rw-r--r--   0     1001      123       39 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/tests/README.md
--rw-r--r--   0     1001      123    74107 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/tests/mock_json.rs
--rw-r--r--   0     1001      123      503 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/tests/mock_loader.rs
--rw-r--r--   0     1001      123      759 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_core/tests/test_use.rs
--rw-r--r--   0        0        0     1432 1970-01-01 00:00:00.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/Cargo.toml
--rw-r--r--   0     1001      123       27 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/README.md
--rw-r--r--   0     1001      123      384 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/api.rs
--rw-r--r--   0     1001      123   376521 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/api_mock.rs
--rw-r--r--   0     1001      123        0 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/base_dao.rs
--rw-r--r--   0     1001      123      348 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/consts.rs
--rw-r--r--   0     1001      123    79882 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/database/datasheet/dependency_analyzer.rs
--rw-r--r--   0     1001      123     9023 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/database/datasheet/foreign_datasheet_loader.rs
--rw-r--r--   0     1001      123    56810 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/database/datasheet/mod.rs
--rw-r--r--   0     1001      123     7192 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/database/datasheet/reference_manager.rs
--rw-r--r--   0     1001      123     1938 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/database/meta.rs
--rw-r--r--   0     1001      123      273 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/database/mod.rs
--rw-r--r--   0     1001      123    13616 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/database/record.rs
--rw-r--r--   0     1001      123     1404 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/database/record_comment.rs
--rw-r--r--   0     1001      123     1196 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/database/revision.rs
--rw-r--r--   0     1001      123      138 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/database_mock.rs
--rw-r--r--   0     1001      123     5089 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/datapack_dao.rs
--rw-r--r--   0     1001      123       54 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/db_manager/README.md
--rw-r--r--   0     1001      123     2299 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/db_manager/client.rs
--rw-r--r--   0     1001      123     4515 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/db_manager/mod.rs
--rw-r--r--   0     1001      123      783 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/lib.rs
--rw-r--r--   0     1001      123     3295 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/loaders.rs
--rw-r--r--   0     1001      123     2169 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/node/children.rs
--rw-r--r--   0     1001      123     1039 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/node/description.rs
--rw-r--r--   0     1001      123      117 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/node/mod.rs
--rw-r--r--   0     1001      123    15866 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/node/node.rs
--rw-r--r--   0     1001      123    43993 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/node/permission.rs
--rw-r--r--   0     1001      123     2918 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/node/share_setting.rs
--rw-r--r--   0     1001      123     6358 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/redis.rs
--rw-r--r--   0     1001      123     1101 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/resource/meta.rs
--rw-r--r--   0     1001      123       35 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/resource/mod.rs
--rw-r--r--   0     1001      123     7026 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/rest.rs
--rw-r--r--   0     1001      123       68 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/types/mod.rs
--rw-r--r--   0     1001      123     1699 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/types/unit_po.rs
--rw-r--r--   0     1001      123     8798 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/unit/mod.rs
--rw-r--r--   0     1001      123     8999 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/user.rs
--rw-r--r--   0        0        0      672 1970-01-01 00:00:00.000000 zzq_string_sum-0.2.0/Cargo.toml
--rw-r--r--   0     1001      123     2791 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/.github/workflows/CI.yml
--rw-r--r--   0     1001      123      685 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/.gitignore
--rw-r--r--   0     1001      123      132 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/README.md
--rw-r--r--   0     1001      123      438 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/pyproject.toml
--rw-r--r--   0     1001      123      202 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/python/databus_python/__init__.py
--rw-r--r--   0     1001      123     2764 2023-07-23 13:44:42.000000 zzq_string_sum-0.2.0/src/lib.rs
--rw-r--r--   0     1001      123    99205 2023-07-23 13:44:49.000000 zzq_string_sum-0.2.0/Cargo.lock
--rw-r--r--   0        0        0      465 1970-01-01 00:00:00.000000 zzq_string_sum-0.2.0/PKG-INFO
+-rw-r--r--   0        0        0     1443 1970-01-01 00:00:00.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/Cargo.toml
+-rw-r--r--   0     1001      123       63 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/README.md
+-rw-r--r--   0     1001      123       23 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/bo/README.md
+-rw-r--r--   0     1001      123      437 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/bo/data_objects_manager.rs
+-rw-r--r--   0     1001      123      326 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/bo/datasheet.rs
+-rw-r--r--   0     1001      123      134 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/bo/mod.rs
+-rw-r--r--   0     1001      123      336 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/bo/space.rs
+-rw-r--r--   0     1001      123      536 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/bo/tests.rs
+-rw-r--r--   0     1001      123       59 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/bo/types.rs
+-rw-r--r--   0     1001      123     1472 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/lib.rs
+-rw-r--r--   0     1001      123       80 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/ot/README.md
+-rw-r--r--   0     1001      123       31 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/ot/actions/add_records.rs
+-rw-r--r--   0     1001      123        1 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/ot/changeset.rs
+-rw-r--r--   0     1001      123      113 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/ot/commands/add_records.rs
+-rw-r--r--   0     1001      123     5992 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/ot/commands/colla_command_name.rs
+-rw-r--r--   0     1001      123     8076 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/ot/commands/command_manager.rs
+-rw-r--r--   0     1001      123      176 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/ot/commands/mod.rs
+-rw-r--r--   0     1001      123       87 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/ot/commands/types.rs
+-rw-r--r--   0     1001      123        1 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/ot/events/mod.rs
+-rw-r--r--   0     1001      123      133 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/ot/mod.rs
+-rw-r--r--   0     1001      123      677 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/ot/tests.rs
+-rw-r--r--   0     1001      123     5866 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/shared/consts.rs
+-rw-r--r--   0     1001      123      423 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/shared/container.rs
+-rw-r--r--   0     1001      123      494 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/shared/errors.rs
+-rw-r--r--   0     1001      123     6304 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/shared/json.rs
+-rw-r--r--   0     1001      123      360 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/shared/logging.rs
+-rw-r--r--   0     1001      123     2246 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/shared/macros.rs
+-rw-r--r--   0     1001      123      270 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/shared/mod.rs
+-rw-r--r--   0     1001      123      518 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/shared/option.rs
+-rw-r--r--   0     1001      123      333 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/shared/slice.rs
+-rw-r--r--   0     1001      123      443 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/shared/sql.rs
+-rw-r--r--   0     1001      123       22 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/so/README.md
+-rw-r--r--   0     1001      123     1702 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/so/data_bundle.rs
+-rw-r--r--   0     1001      123     2002 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/so/data_functions_manager.rs
+-rw-r--r--   0     1001      123        0 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/so/fields/mod.rs
+-rw-r--r--   0     1001      123        0 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/so/formula/mod.rs
+-rw-r--r--   0     1001      123      146 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/so/mod.rs
+-rw-r--r--   0     1001      123     2389 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/so/types.rs
+-rw-r--r--   0     1001      123     2319 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/types/dao.rs
+-rw-r--r--   0     1001      123     5398 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/types/database.rs
+-rw-r--r--   0     1001      123     4374 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/types/mod.rs
+-rw-r--r--   0     1001      123     1234 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/types/node.rs
+-rw-r--r--   0     1001      123      643 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/types/result.rs
+-rw-r--r--   0     1001      123     3278 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/types/types2.rs
+-rw-r--r--   0     1001      123     1003 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/src/types/unit.rs
+-rw-r--r--   0     1001      123       39 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/tests/README.md
+-rw-r--r--   0     1001      123    74107 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/tests/mock_json.rs
+-rw-r--r--   0     1001      123      503 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/tests/mock_loader.rs
+-rw-r--r--   0     1001      123      759 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_core/tests/test_use.rs
+-rw-r--r--   0        0        0     1447 1970-01-01 00:00:00.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/Cargo.toml
+-rw-r--r--   0     1001      123       27 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/README.md
+-rw-r--r--   0     1001      123      384 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/api.rs
+-rw-r--r--   0     1001      123   376521 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/api_mock.rs
+-rw-r--r--   0     1001      123        0 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/base_dao.rs
+-rw-r--r--   0     1001      123      348 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/consts.rs
+-rw-r--r--   0     1001      123    79882 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/database/datasheet/dependency_analyzer.rs
+-rw-r--r--   0     1001      123     9023 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/database/datasheet/foreign_datasheet_loader.rs
+-rw-r--r--   0     1001      123    56810 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/database/datasheet/mod.rs
+-rw-r--r--   0     1001      123     7192 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/database/datasheet/reference_manager.rs
+-rw-r--r--   0     1001      123     1938 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/database/meta.rs
+-rw-r--r--   0     1001      123      273 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/database/mod.rs
+-rw-r--r--   0     1001      123    13616 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/database/record.rs
+-rw-r--r--   0     1001      123     1404 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/database/record_comment.rs
+-rw-r--r--   0     1001      123     1196 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/database/revision.rs
+-rw-r--r--   0     1001      123      138 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/database_mock.rs
+-rw-r--r--   0     1001      123     5089 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/datapack_dao.rs
+-rw-r--r--   0     1001      123       54 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/db_manager/README.md
+-rw-r--r--   0     1001      123     2299 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/db_manager/client.rs
+-rw-r--r--   0     1001      123     4515 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/db_manager/mod.rs
+-rw-r--r--   0     1001      123      783 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/lib.rs
+-rw-r--r--   0     1001      123     3295 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/loaders.rs
+-rw-r--r--   0     1001      123     2169 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/node/children.rs
+-rw-r--r--   0     1001      123     1039 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/node/description.rs
+-rw-r--r--   0     1001      123      117 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/node/mod.rs
+-rw-r--r--   0     1001      123    15866 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/node/node.rs
+-rw-r--r--   0     1001      123    43993 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/node/permission.rs
+-rw-r--r--   0     1001      123     2918 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/node/share_setting.rs
+-rw-r--r--   0     1001      123     6358 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/redis.rs
+-rw-r--r--   0     1001      123     1101 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/resource/meta.rs
+-rw-r--r--   0     1001      123       35 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/resource/mod.rs
+-rw-r--r--   0     1001      123     7026 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/rest.rs
+-rw-r--r--   0     1001      123       68 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/types/mod.rs
+-rw-r--r--   0     1001      123     1699 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/types/unit_po.rs
+-rw-r--r--   0     1001      123     8798 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/unit/mod.rs
+-rw-r--r--   0     1001      123     8999 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/user.rs
+-rw-r--r--   0        0        0      687 1970-01-01 00:00:00.000000 zzq_string_sum-0.3.0/Cargo.toml
+-rw-r--r--   0     1001      123      438 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/pyproject.toml
+-rw-r--r--   0     1001      123      202 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/python/databus_python/__init__.py
+-rw-r--r--   0     1001      123     2764 2023-07-23 15:20:24.000000 zzq_string_sum-0.3.0/src/lib.rs
+-rw-r--r--   0     1001      123   102064 2023-07-23 15:20:33.000000 zzq_string_sum-0.3.0/Cargo.lock
+-rw-r--r--   0        0        0      263 1970-01-01 00:00:00.000000 zzq_string_sum-0.3.0/PKG-INFO
```

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_core/Cargo.toml` & `zzq_string_sum-0.3.0/local_dependencies/databus_core/Cargo.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 [package]
 name = "databus_core"
 version = "0.23.0"
 edition = "2021"
+resolver = "2"
 
 # See more keys and their definitions at https://doc.rust-lang.org/cargo/reference/manifest.html
 
 [dependencies]
 getrandom = { version = "0.2", features = ["js"] }
 # zip = "0.6.6"
 # tempfile = "3"
```

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_core/src/bo/tests.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_core/src/bo/tests.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_core/src/lib.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_core/src/lib.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_core/src/ot/commands/colla_command_name.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_core/src/ot/commands/colla_command_name.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_core/src/ot/commands/command_manager.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_core/src/ot/commands/command_manager.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_core/src/ot/tests.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_core/src/ot/tests.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_core/src/shared/consts.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_core/src/shared/consts.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_core/src/shared/json.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_core/src/shared/json.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_core/src/shared/macros.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_core/src/shared/macros.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_core/src/shared/option.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_core/src/shared/option.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_core/src/so/data_bundle.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_core/src/so/data_bundle.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_core/src/so/data_functions_manager.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_core/src/so/data_functions_manager.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_core/src/so/types.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_core/src/so/types.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_core/src/types/dao.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_core/src/types/dao.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_core/src/types/database.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_core/src/types/database.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_core/src/types/mod.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_core/src/types/mod.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_core/src/types/node.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_core/src/types/node.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_core/src/types/result.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_core/src/types/result.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_core/src/types/types2.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_core/src/types/types2.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_core/src/types/unit.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_core/src/types/unit.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_core/tests/mock_json.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_core/tests/mock_json.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_core/tests/test_use.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_core/tests/test_use.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/Cargo.toml` & `zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/Cargo.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 [package]
 name = "databus_dao_db"
 version = "0.23.0"
 edition = "2021"
+resolver = "2"
 
 # See more keys and their definitions at https://doc.rust-lang.org/cargo/reference/manifest.html
 
 [dependencies]
 databus_core = { path = "../databus_core" }
 getrandom = { version = "0.2", features = ["js"] }
 zip = "0.6.6"
```

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/api_mock.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/api_mock.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/database/datasheet/dependency_analyzer.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/database/datasheet/dependency_analyzer.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/database/datasheet/foreign_datasheet_loader.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/database/datasheet/foreign_datasheet_loader.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/database/datasheet/mod.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/database/datasheet/mod.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/database/datasheet/reference_manager.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/database/datasheet/reference_manager.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/database/meta.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/database/meta.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/database/record.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/database/record.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/database/record_comment.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/database/record_comment.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/database/revision.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/database/revision.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/datapack_dao.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/datapack_dao.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/db_manager/client.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/db_manager/client.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/db_manager/mod.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/db_manager/mod.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/lib.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/lib.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/loaders.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/loaders.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/node/children.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/node/children.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/node/description.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/node/description.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/node/node.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/node/node.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/node/permission.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/node/permission.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/node/share_setting.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/node/share_setting.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/redis.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/redis.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/resource/meta.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/resource/meta.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/rest.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/rest.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/types/unit_po.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/types/unit_po.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/unit/mod.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/unit/mod.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/local_dependencies/databus_dao_db/src/user.rs` & `zzq_string_sum-0.3.0/local_dependencies/databus_dao_db/src/user.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/Cargo.toml` & `zzq_string_sum-0.3.0/Cargo.toml`

 * *Files 16% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 [package]
 name = "zzq_string_sum"
-version = "0.2.0"
+version = "0.3.0"
 edition = "2021"
+resolver = "2"
 
 # See more keys and their definitions at https://doc.rust-lang.org/cargo/reference/manifest.html
 [lib]
 name = "zzq_string_sum"
 crate-type = ["cdylib"]
 
 [dependencies]
```

### Comparing `zzq_string_sum-0.2.0/src/lib.rs` & `zzq_string_sum-0.3.0/src/lib.rs`

 * *Files identical despite different names*

### Comparing `zzq_string_sum-0.2.0/Cargo.lock` & `zzq_string_sum-0.3.0/Cargo.lock`

 * *Files 1% similar despite different names*

```diff
@@ -298,14 +298,36 @@
  "pin-project-lite",
  "pin-utils",
  "slab",
  "wasm-bindgen-futures",
 ]
 
 [[package]]
+name = "async-stream"
+version = "0.3.5"
+source = "registry+https://github.com/rust-lang/crates.io-index"
+checksum = "cd56dd203fef61ac097dd65721a419ddccb106b2d2b70ba60a6b529f03961a51"
+dependencies = [
+ "async-stream-impl",
+ "futures-core",
+ "pin-project-lite",
+]
+
+[[package]]
+name = "async-stream-impl"
+version = "0.3.5"
+source = "registry+https://github.com/rust-lang/crates.io-index"
+checksum = "16e62a023e7c117e27523144c5d2459f4397fcc3cab0085af8e2224f643a0193"
+dependencies = [
+ "proc-macro2",
+ "quote",
+ "syn 2.0.27",
+]
+
+[[package]]
 name = "async-task"
 version = "4.4.0"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "ecc7ab41815b3c653ccd2978ec3255c81349336702dfdf62ee6f7069b12a3aae"
 
 [[package]]
 name = "async-tls"
@@ -945,27 +967,32 @@
 [[package]]
 name = "databus_core"
 version = "0.23.0"
 dependencies = [
  "anyhow",
  "async-trait",
  "chrono",
+ "fred",
  "futures",
  "getrandom 0.2.10",
  "http",
  "http-serde",
  "once_cell",
+ "pretty_assertions",
  "regex",
+ "rstest",
+ "rstest_reuse",
  "seahash",
  "serde",
  "serde_json",
  "serde_repr",
  "thiserror",
  "time 0.3.23",
  "tokio",
+ "tokio-test",
  "tracing",
  "tracing-subscriber",
  "url-escape",
 ]
 
 [[package]]
 name = "databus_dao_db"
@@ -981,24 +1008,26 @@
  "http",
  "http-serde",
  "mysql_async",
  "mysql_common",
  "napi",
  "napi-derive",
  "once_cell",
+ "pretty_assertions",
  "regex",
  "seahash",
  "serde",
  "serde_json",
  "serde_repr",
  "surf",
  "tempfile",
  "thiserror",
  "time 0.3.23",
  "tokio",
+ "tokio-test",
  "tracing",
  "tracing-subscriber",
  "url-escape",
  "zip",
 ]
 
 [[package]]
@@ -1012,14 +1041,20 @@
  "crossbeam-queue",
  "num_cpus",
  "serde",
  "tokio",
 ]
 
 [[package]]
+name = "diff"
+version = "0.1.13"
+source = "registry+https://github.com/rust-lang/crates.io-index"
+checksum = "56254986775e3233ffa9c4d7d3faaf6d36a2c09d30b20687e9f88bc8bafc16c8"
+
+[[package]]
 name = "digest"
 version = "0.9.0"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "d3dd60d1080a57a05ab032377049e0591415d2b31afd7028356dbf3cc6dcb066"
 dependencies = [
  "generic-array",
 ]
@@ -1325,14 +1360,20 @@
 [[package]]
 name = "futures-task"
 version = "0.3.28"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "76d3d132be6c0e6aa1534069c705a74a5997a356c0dc2f86a47765e5617c5b65"
 
 [[package]]
+name = "futures-timer"
+version = "3.0.2"
+source = "registry+https://github.com/rust-lang/crates.io-index"
+checksum = "e64b03909df88034c26dc1547e8970b91f98bdb65165d6a4e9110d94263dbb2c"
+
+[[package]]
 name = "futures-util"
 version = "0.3.28"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "26b01e40b772d54cf6c6d721c1d1abd0647a0106a12ecaa1c186273392a69533"
 dependencies = [
  "futures-channel",
  "futures-core",
@@ -2323,14 +2364,24 @@
 [[package]]
 name = "ppv-lite86"
 version = "0.2.17"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "5b40af805b3121feab8a3c29f04d8ad262fa8e0561883e7653e024ae4479e6de"
 
 [[package]]
+name = "pretty_assertions"
+version = "1.4.0"
+source = "registry+https://github.com/rust-lang/crates.io-index"
+checksum = "af7cee1a6c8a5b9208b3cb1061f10c0cb689087b3d8ce85fb9d2dd7a29b6ba66"
+dependencies = [
+ "diff",
+ "yansi",
+]
+
+[[package]]
 name = "pretty_env_logger"
 version = "0.4.0"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "926d36b9553851b8b0005f1275891b392ee4d2d833852c417ed025477350fb9d"
 dependencies = [
  "env_logger",
  "log",
@@ -2704,14 +2755,52 @@
 dependencies = [
  "proc-macro2",
  "quote",
  "syn 1.0.109",
 ]
 
 [[package]]
+name = "rstest"
+version = "0.17.0"
+source = "registry+https://github.com/rust-lang/crates.io-index"
+checksum = "de1bb486a691878cd320c2f0d319ba91eeaa2e894066d8b5f8f117c000e9d962"
+dependencies = [
+ "futures",
+ "futures-timer",
+ "rstest_macros",
+ "rustc_version 0.4.0",
+]
+
+[[package]]
+name = "rstest_macros"
+version = "0.17.0"
+source = "registry+https://github.com/rust-lang/crates.io-index"
+checksum = "290ca1a1c8ca7edb7c3283bd44dc35dd54fdec6253a3912e201ba1072018fca8"
+dependencies = [
+ "cfg-if",
+ "proc-macro2",
+ "quote",
+ "rustc_version 0.4.0",
+ "syn 1.0.109",
+ "unicode-ident",
+]
+
+[[package]]
+name = "rstest_reuse"
+version = "0.5.0"
+source = "registry+https://github.com/rust-lang/crates.io-index"
+checksum = "45f80dcc84beab3a327bbe161f77db25f336a1452428176787c8c79ac79d7073"
+dependencies = [
+ "quote",
+ "rand 0.8.5",
+ "rustc_version 0.4.0",
+ "syn 1.0.109",
+]
+
+[[package]]
 name = "rust_decimal"
 version = "1.30.0"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "d0446843641c69436765a35a5a77088e28c2e6a12da93e84aa3ab1cd4aa5a042"
 dependencies = [
  "arrayvec 0.7.4",
  "borsh",
@@ -2743,14 +2832,23 @@
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "138e3e0acb6c9fb258b19b67cb8abd63c00679d2851805ea151465464fe9030a"
 dependencies = [
  "semver 0.9.0",
 ]
 
 [[package]]
+name = "rustc_version"
+version = "0.4.0"
+source = "registry+https://github.com/rust-lang/crates.io-index"
+checksum = "bfa0f585226d2e68097d4f95d113b15b83a82e819ab25717ec0590d9584ef366"
+dependencies = [
+ "semver 1.0.18",
+]
+
+[[package]]
 name = "rustix"
 version = "0.37.23"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "4d69718bf81c6127a49dc64e44a742e8bb9213c0ff8869a22c308f84c1d4ab06"
 dependencies = [
  "bitflags 1.3.2",
  "errno",
@@ -3170,15 +3268,15 @@
 [[package]]
 name = "stdweb"
 version = "0.4.20"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "d022496b16281348b52d0e30ae99e01a73d737b2f45d38fed4edf79f9325a1d5"
 dependencies = [
  "discard",
- "rustc_version",
+ "rustc_version 0.2.3",
  "stdweb-derive",
  "stdweb-internal-macros",
  "stdweb-internal-runtime",
  "wasm-bindgen",
 ]
 
 [[package]]
@@ -3475,14 +3573,27 @@
 dependencies = [
  "futures-core",
  "pin-project-lite",
  "tokio",
 ]
 
 [[package]]
+name = "tokio-test"
+version = "0.4.2"
+source = "registry+https://github.com/rust-lang/crates.io-index"
+checksum = "53474327ae5e166530d17f2d956afcb4f8a004de581b3cae10f12006bc8163e3"
+dependencies = [
+ "async-stream",
+ "bytes",
+ "futures-core",
+ "tokio",
+ "tokio-stream",
+]
+
+[[package]]
 name = "tokio-util"
 version = "0.7.8"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "806fe8c2c87eccc8b3267cbae29ed3ab2d0bd37fca70ab622e46aaa9375ddb7d"
 dependencies = [
  "bytes",
  "futures-core",
@@ -3955,14 +4066,20 @@
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "05f360fc0b24296329c78fda852a1e9ae82de9cf7b27dae4b7f62f118f77b9ed"
 dependencies = [
  "tap",
 ]
 
 [[package]]
+name = "yansi"
+version = "0.5.1"
+source = "registry+https://github.com/rust-lang/crates.io-index"
+checksum = "09041cd90cf85f7f8b2df60c646f853b7f535ce68f85244eb6731cf89fa498ec"
+
+[[package]]
 name = "zip"
 version = "0.6.6"
 source = "registry+https://github.com/rust-lang/crates.io-index"
 checksum = "760394e246e4c28189f19d488c058bf16f564016aefac5d32bb1f3b51d5e9261"
 dependencies = [
  "aes 0.8.3",
  "byteorder",
@@ -4006,15 +4123,15 @@
  "cc",
  "libc",
  "pkg-config",
 ]
 
 [[package]]
 name = "zzq_string_sum"
-version = "0.2.0"
+version = "0.3.0"
 dependencies = [
  "async-std",
  "databus_core",
  "databus_dao_db",
  "futures",
  "pyo3",
  "pyo3-asyncio",
```

