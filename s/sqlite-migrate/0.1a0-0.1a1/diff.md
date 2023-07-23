# Comparing `tmp/sqlite-migrate-0.1a0.tar.gz` & `tmp/sqlite-migrate-0.1a1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "sqlite-migrate-0.1a0.tar", last modified: Sun Jul 23 01:31:51 2023, max compression
+gzip compressed data, was "sqlite-migrate-0.1a1.tar", last modified: Sun Jul 23 04:26:40 2023, max compression
```

## Comparing `sqlite-migrate-0.1a0.tar` & `sqlite-migrate-0.1a1.tar`

### file list

```diff
@@ -1,19 +1,19 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 01:31:51.351561 sqlite-migrate-0.1a0/
--rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-07-23 01:31:36.000000 sqlite-migrate-0.1a0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     2554 2023-07-23 01:31:51.351561 sqlite-migrate-0.1a0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2036 2023-07-23 01:31:36.000000 sqlite-migrate-0.1a0/README.md
--rw-r--r--   0 runner    (1001) docker     (123)      655 2023-07-23 01:31:36.000000 sqlite-migrate-0.1a0/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 01:31:51.351561 sqlite-migrate-0.1a0/setup.cfg
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 01:31:51.347561 sqlite-migrate-0.1a0/sqlite_migrate/
--rw-r--r--   0 runner    (1001) docker     (123)     2297 2023-07-23 01:31:36.000000 sqlite-migrate-0.1a0/sqlite_migrate/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1947 2023-07-23 01:31:36.000000 sqlite-migrate-0.1a0/sqlite_migrate/sqlite_utils_plugin.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 01:31:51.347561 sqlite-migrate-0.1a0/sqlite_migrate.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2554 2023-07-23 01:31:51.000000 sqlite-migrate-0.1a0/sqlite_migrate.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      399 2023-07-23 01:31:51.000000 sqlite-migrate-0.1a0/sqlite_migrate.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 01:31:51.000000 sqlite-migrate-0.1a0/sqlite_migrate.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       60 2023-07-23 01:31:51.000000 sqlite-migrate-0.1a0/sqlite_migrate.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)       28 2023-07-23 01:31:51.000000 sqlite-migrate-0.1a0/sqlite_migrate.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       15 2023-07-23 01:31:51.000000 sqlite-migrate-0.1a0/sqlite_migrate.egg-info/top_level.txt
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 01:31:51.347561 sqlite-migrate-0.1a0/tests/
--rw-r--r--   0 runner    (1001) docker     (123)      452 2023-07-23 01:31:36.000000 sqlite-migrate-0.1a0/tests/test_sqlite_migrate.py
--rw-r--r--   0 runner    (1001) docker     (123)     1120 2023-07-23 01:31:36.000000 sqlite-migrate-0.1a0/tests/test_sqlite_utils_migrate_command.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:26:40.600583 sqlite-migrate-0.1a1/
+-rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-07-23 04:26:23.000000 sqlite-migrate-0.1a1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     4824 2023-07-23 04:26:40.600583 sqlite-migrate-0.1a1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     4305 2023-07-23 04:26:23.000000 sqlite-migrate-0.1a1/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)      680 2023-07-23 04:26:23.000000 sqlite-migrate-0.1a1/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 04:26:40.600583 sqlite-migrate-0.1a1/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:26:40.600583 sqlite-migrate-0.1a1/sqlite_migrate/
+-rw-r--r--   0 runner    (1001) docker     (123)     3084 2023-07-23 04:26:23.000000 sqlite-migrate-0.1a1/sqlite_migrate/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3892 2023-07-23 04:26:23.000000 sqlite-migrate-0.1a1/sqlite_migrate/sqlite_utils_plugin.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:26:40.600583 sqlite-migrate-0.1a1/sqlite_migrate.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     4824 2023-07-23 04:26:40.000000 sqlite-migrate-0.1a1/sqlite_migrate.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      399 2023-07-23 04:26:40.000000 sqlite-migrate-0.1a1/sqlite_migrate.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 04:26:40.000000 sqlite-migrate-0.1a1/sqlite_migrate.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       60 2023-07-23 04:26:40.000000 sqlite-migrate-0.1a1/sqlite_migrate.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       44 2023-07-23 04:26:40.000000 sqlite-migrate-0.1a1/sqlite_migrate.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       15 2023-07-23 04:26:40.000000 sqlite-migrate-0.1a1/sqlite_migrate.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:26:40.600583 sqlite-migrate-0.1a1/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)      452 2023-07-23 04:26:23.000000 sqlite-migrate-0.1a1/tests/test_sqlite_migrate.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3478 2023-07-23 04:26:23.000000 sqlite-migrate-0.1a1/tests/test_sqlite_utils_migrate_command.py
```

### Comparing `sqlite-migrate-0.1a0/LICENSE` & `sqlite-migrate-0.1a1/LICENSE`

 * *Files identical despite different names*

### Comparing `sqlite-migrate-0.1a0/pyproject.toml` & `sqlite-migrate-0.1a1/pyproject.toml`

 * *Files 10% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [project]
 name = "sqlite-migrate"
-version = "0.1a0"
+version = "0.1a1"
 description = "A simple database migration system for SQLite, based on sqlite-utils"
 readme = "README.md"
 authors = [{name = "Simon Willison"}]
 license = {text = "Apache-2.0"}
 classifiers = [
     "Development Status :: 2 - Pre-Alpha"
 ]
@@ -15,11 +15,11 @@
 
 [project.urls]
 Homepage = "https://github.com/simonw/sqlite-migrate"
 Changelog = "https://github.com/simonw/sqlite-migrate/releases"
 Issues = "https://github.com/simonw/sqlite-migrate/issues"
 
 [project.optional-dependencies]
-test = ["pytest"]
+test = ["pytest", "mypy", "black", "ruff"]
 
 [project.entry-points.sqlite_utils]
 migrate = "sqlite_migrate.sqlite_utils_plugin"
```

### Comparing `sqlite-migrate-0.1a0/sqlite_migrate/__init__.py` & `sqlite-migrate-0.1a1/sqlite_migrate/__init__.py`

 * *Files 14% similar despite different names*

```diff
@@ -1,77 +1,104 @@
 from dataclasses import dataclass
 import datetime
-from typing import Callable, Optional
+from typing import cast, Callable, List, Optional
+from typing import TYPE_CHECKING
+
+if TYPE_CHECKING:
+    from sqlite_utils.db import Database, Table
 
 
 class Migrations:
     migrations_table = "_sqlite_migrations"
 
     @dataclass
     class _Migration:
         name: str
         fn: Callable
 
+    @dataclass
+    class _AppliedMigration:
+        name: str
+        applied_at: datetime.datetime
+
     def __init__(self, name: str):
         """
         :param name: The name of the migration set. This should be unique.
         """
         self.name = name
-        self._migrations = []
+        self._migrations: List[Migrations._Migration] = []
 
     def __call__(self, *, name: Optional[str] = None) -> Callable:
         """
         :param name: The name to use for this migration - if not provided,
           the name of the function will be used
         """
 
         def inner(func: Callable) -> Callable:
             self._migrations.append(self._Migration(name or func.__name__, func))
             return func
 
         return inner
 
-    def pending(self, db: "sqlite_utils.Database"):
+    def pending(self, db: "Database") -> List["Migrations._Migration"]:
         """
         Return a list of pending migrations.
         """
         self.ensure_migrations_table(db)
         already_applied = {r["name"] for r in db[self.migrations_table].rows}
         return [
             migration
             for migration in self._migrations
             if migration.name not in already_applied
         ]
 
-    def apply(self, db: "sqlite_utils.Database"):
+    def applied(self, db: "Database") -> List["Migrations._AppliedMigration"]:
+        """
+        Return a list of applied migrations.
+        """
+        self.ensure_migrations_table(db)
+        return [
+            self._AppliedMigration(name=row["name"], applied_at=row["applied_at"])
+            for row in db[self.migrations_table].rows_where(
+                "migration_set = ?", [self.name]
+            )
+        ]
+
+    def apply(self, db: "Database"):
         """
         Apply any pending migrations to the database.
         """
         self.ensure_migrations_table(db)
         for migration in self.pending(db):
             migration.fn(db)
-            db[self.migrations_table].insert(
+            _table(db, self.migrations_table).insert(
                 {
                     "migration_set": self.name,
                     "name": migration.name,
                     "applied_at": str(datetime.datetime.utcnow()),
                 }
             )
 
-    def ensure_migrations_table(self, db: "sqlite_utils.Database"):
+    def ensure_migrations_table(self, db: "Database"):
         """
         Create _sqlite_migrations table if it doesn't already exist
         """
-        if not db[self.migrations_table].exists():
-            db[self.migrations_table].create(
+        table = _table(db, self.migrations_table)
+        if not table.exists():
+            table.create(
                 {
                     "migration_set": str,
                     "name": str,
                     "applied_at": str,
                 },
                 pk="name",
             )
 
     def __repr__(self):
         return "<Migrations '{}': [{}]>".format(
             self.name, ", ".join(m.name for m in self._migrations)
         )
+
+
+def _table(db: "Database", name: str) -> "Table":
+    # mypy workaround
+    return cast("Table", db[name])
```

