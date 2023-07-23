# Comparing `tmp/firefox_bookmarks-0.1.0.tar.gz` & `tmp/firefox_bookmarks-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "firefox_bookmarks-0.1.0.tar", max compression
+gzip compressed data, was "firefox_bookmarks-0.2.0.tar", max compression
```

## Comparing `firefox_bookmarks-0.1.0.tar` & `firefox_bookmarks-0.2.0.tar`

### file list

```diff
@@ -1,8 +1,9 @@
--rw-r--r--   0        0        0      137 2023-07-23 11:39:08.278273 firefox_bookmarks-0.1.0/firefox_bookmarks/__init__.py
--rw-r--r--   0        0        0      892 2023-07-23 11:39:08.280116 firefox_bookmarks-0.1.0/firefox_bookmarks/connect.py
--rw-r--r--   0        0        0      276 2023-07-22 14:07:55.049329 firefox_bookmarks-0.1.0/firefox_bookmarks/constants.py
--rw-r--r--   0        0        0     2280 2023-07-22 14:10:44.937368 firefox_bookmarks-0.1.0/firefox_bookmarks/locate.py
--rw-r--r--   0        0        0    35184 2023-07-21 16:18:12.325494 firefox_bookmarks-0.1.0/LICENSE
--rw-r--r--   0        0        0     1235 2023-07-23 08:37:01.651455 firefox_bookmarks-0.1.0/pyproject.toml
--rw-r--r--   0        0        0      616 2023-07-23 08:35:10.919927 firefox_bookmarks-0.1.0/README.md
--rw-r--r--   0        0        0     1910 1970-01-01 00:00:00.000000 firefox_bookmarks-0.1.0/PKG-INFO
+-rw-r--r--   0        0        0      420 2023-07-23 11:43:23.291314 firefox_bookmarks-0.2.0/firefox_bookmarks/__init__.py
+-rw-r--r--   0        0        0     1175 2023-07-23 11:43:23.293750 firefox_bookmarks-0.2.0/firefox_bookmarks/connect.py
+-rw-r--r--   0        0        0      276 2023-07-22 14:07:55.049329 firefox_bookmarks-0.2.0/firefox_bookmarks/constants.py
+-rw-r--r--   0        0        0     2280 2023-07-22 14:10:44.937368 firefox_bookmarks-0.2.0/firefox_bookmarks/locate.py
+-rw-r--r--   0        0        0     3771 2023-07-23 11:43:23.295826 firefox_bookmarks-0.2.0/firefox_bookmarks/models.py
+-rw-r--r--   0        0        0    35184 2023-07-21 16:18:12.325494 firefox_bookmarks-0.2.0/LICENSE
+-rw-r--r--   0        0        0     1235 2023-07-23 11:43:48.655434 firefox_bookmarks-0.2.0/pyproject.toml
+-rw-r--r--   0        0        0      616 2023-07-23 08:35:10.919927 firefox_bookmarks-0.2.0/README.md
+-rw-r--r--   0        0        0     1910 1970-01-01 00:00:00.000000 firefox_bookmarks-0.2.0/PKG-INFO
```

### Comparing `firefox_bookmarks-0.1.0/firefox_bookmarks/connect.py` & `firefox_bookmarks-0.2.0/firefox_bookmarks/connect.py`

 * *Files 11% similar despite different names*

```diff
@@ -2,28 +2,35 @@
 
 from .constants import ProfileCriterion
 from .locate import locate_db
 
 
 def connect_to_places_db(
     *,
+    database: SqliteDatabase | None = None,
     look_under_path: str | None = None,
     criterion: ProfileCriterion = ProfileCriterion.LATEST,
 ) -> SqliteDatabase:
     """Connects to a Places database according to the chosen criterion
 
     Args:
+        database: A dummy pre-existing `SqliteDatabase` object to be \
+        initialized with the actual path. If not supplied, a new one is \
+        created.
         look_under_path: Path from where to start searching. \
         If not supplied, looks under default profiles directory.
         criterion: Which profile to choose, in case there are multiple. \
         Defaults to `ProfileCriterion.LATEST`.
 
     Returns:
         A connection to the Places database under the chosen profile
     """
 
     db_path = locate_db(look_under_path=look_under_path, criterion=criterion)
 
-    database = SqliteDatabase(db_path)
+    if database is None:
+        database = SqliteDatabase(db_path)
+    else:
+        database.init(db_path)
     database.connect(reuse_if_open=True)
 
     return database
```

### Comparing `firefox_bookmarks-0.1.0/firefox_bookmarks/locate.py` & `firefox_bookmarks-0.2.0/firefox_bookmarks/locate.py`

 * *Files identical despite different names*

### Comparing `firefox_bookmarks-0.1.0/LICENSE` & `firefox_bookmarks-0.2.0/LICENSE`

 * *Files identical despite different names*

### Comparing `firefox_bookmarks-0.1.0/pyproject.toml` & `firefox_bookmarks-0.2.0/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "firefox-bookmarks"
-version = "0.1.0"
+version = "0.2.0"
 description = "Manage your Firefox bookmarks with ease"
 authors = ["Aditya Rajput <adiraj20072002@gmail.com>"]
 license = "AGPL-3.0-or-later"
 readme = "README.md"
 packages = [{include = "firefox_bookmarks"}]
 repository = "https://github.com/BURG3R5/firefox-bookmarks"
 documentation = "https://github.com/BURG3R5/firefox-bookmarks"
```

### Comparing `firefox_bookmarks-0.1.0/README.md` & `firefox_bookmarks-0.2.0/README.md`

 * *Files identical despite different names*

### Comparing `firefox_bookmarks-0.1.0/PKG-INFO` & `firefox_bookmarks-0.2.0/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: firefox-bookmarks
-Version: 0.1.0
+Version: 0.2.0
 Summary: Manage your Firefox bookmarks with ease
 Home-page: https://github.com/BURG3R5/firefox-bookmarks
 License: AGPL-3.0-or-later
 Keywords: firefox,bookmarks,browser,util
 Author: Aditya Rajput
 Author-email: adiraj20072002@gmail.com
 Requires-Python: >=3.10,<4.0
```

