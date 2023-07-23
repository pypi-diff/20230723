# Comparing `tmp/pelican-to-sqlite-0.5.0.tar.gz` & `tmp/pelican-to-sqlite-0.6.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pelican-to-sqlite-0.5.0.tar", last modified: Thu Feb 10 03:47:35 2022, max compression
+gzip compressed data, was "pelican-to-sqlite-0.6.0.tar", last modified: Sun Jul 23 18:26:58 2023, max compression
```

## Comparing `pelican-to-sqlite-0.5.0.tar` & `pelican-to-sqlite-0.6.0.tar`

### file list

```diff
@@ -1,14 +1,18 @@
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-02-10 03:47:35.200970 pelican-to-sqlite-0.5.0/
--rw-r--r--   0 runner    (1001) docker     (121)    11357 2022-02-10 03:47:26.000000 pelican-to-sqlite-0.5.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (121)     3583 2022-02-10 03:47:35.200970 pelican-to-sqlite-0.5.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)     2967 2022-02-10 03:47:26.000000 pelican-to-sqlite-0.5.0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-02-10 03:47:35.200970 pelican-to-sqlite-0.5.0/pelican_to_sqlite.egg-info/
--rw-r--r--   0 runner    (1001) docker     (121)     3583 2022-02-10 03:47:35.000000 pelican-to-sqlite-0.5.0/pelican_to_sqlite.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (121)      299 2022-02-10 03:47:35.000000 pelican-to-sqlite-0.5.0/pelican_to_sqlite.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2022-02-10 03:47:35.000000 pelican-to-sqlite-0.5.0/pelican_to_sqlite.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (121)       83 2022-02-10 03:47:35.000000 pelican-to-sqlite-0.5.0/pelican_to_sqlite.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (121)       52 2022-02-10 03:47:35.000000 pelican-to-sqlite-0.5.0/pelican_to_sqlite.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (121)        1 2022-02-10 03:47:35.000000 pelican-to-sqlite-0.5.0/pelican_to_sqlite.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (121)       96 2022-02-10 03:47:26.000000 pelican-to-sqlite-0.5.0/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (121)      190 2022-02-10 03:47:35.200970 pelican-to-sqlite-0.5.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (121)     1273 2022-02-10 03:47:26.000000 pelican-to-sqlite-0.5.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 18:26:58.521445 pelican-to-sqlite-0.6.0/
+-rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-07-23 18:26:44.000000 pelican-to-sqlite-0.6.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     3508 2023-07-23 18:26:58.521445 pelican-to-sqlite-0.6.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     2967 2023-07-23 18:26:44.000000 pelican-to-sqlite-0.6.0/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 18:26:58.517445 pelican-to-sqlite-0.6.0/pelican/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 18:26:58.517445 pelican-to-sqlite-0.6.0/pelican/plugins/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 18:26:58.517445 pelican-to-sqlite-0.6.0/pelican/plugins/pelican_to_sqlite/
+-rw-r--r--   0 runner    (1001) docker     (123)       40 2023-07-23 18:26:44.000000 pelican-to-sqlite-0.6.0/pelican/plugins/pelican_to_sqlite/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1665 2023-07-23 18:26:44.000000 pelican-to-sqlite-0.6.0/pelican/plugins/pelican_to_sqlite/pelican_to_sqlite.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1049 2023-07-23 18:26:44.000000 pelican-to-sqlite-0.6.0/pelican/plugins/pelican_to_sqlite/test_pelican_to_sqlite.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 18:26:58.521445 pelican-to-sqlite-0.6.0/pelican_to_sqlite.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     3508 2023-07-23 18:26:58.000000 pelican-to-sqlite-0.6.0/pelican_to_sqlite.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      407 2023-07-23 18:26:58.000000 pelican-to-sqlite-0.6.0/pelican_to_sqlite.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 18:26:58.000000 pelican-to-sqlite-0.6.0/pelican_to_sqlite.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       52 2023-07-23 18:26:58.000000 pelican-to-sqlite-0.6.0/pelican_to_sqlite.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        8 2023-07-23 18:26:58.000000 pelican-to-sqlite-0.6.0/pelican_to_sqlite.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      831 2023-07-23 18:26:44.000000 pelican-to-sqlite-0.6.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)      190 2023-07-23 18:26:58.521445 pelican-to-sqlite-0.6.0/setup.cfg
```

### Comparing `pelican-to-sqlite-0.5.0/LICENSE` & `pelican-to-sqlite-0.6.0/LICENSE`

 * *Files identical despite different names*

### Comparing `pelican-to-sqlite-0.5.0/PKG-INFO` & `pelican-to-sqlite-0.6.0/PKG-INFO`

 * *Files 9% similar despite different names*

```diff
@@ -1,19 +1,17 @@
 Metadata-Version: 2.1
 Name: pelican-to-sqlite
-Version: 0.5.0
-Summary: CLI tool for loading local pelican markdown files into a SQLite database
-Home-page: https://github.com/ryancheley/pelican-to-sqlite
+Version: 0.6.0
+Summary: A Pelican Plugin for outputting your Pelican posts into a SQLite Database
 Author: Ryan Cheley
-License: Apache License, Version 2.0
+License: Apache-2.0
 Project-URL: Issues, https://github.com/ryancheley/pelican-to-sqlite/issues
 Project-URL: CI, https://github.com/ryancheley/pelican-to-sqlite/actions
 Project-URL: Changelog, https://github.com/ryancheley/pelican-to-sqlite/releases
-Platform: UNKNOWN
-Requires-Python: >=3.7
+Classifier: Development Status :: 4 - Beta
 Description-Content-Type: text/markdown
 Provides-Extra: test
 License-File: LICENSE
 
 # pelican-to-sqlite
 
 [![PyPI](https://img.shields.io/pypi/v/pelican-to-sqlite.svg)](https://pypi.org/project/pelican-to-sqlite/)
@@ -79,9 +77,7 @@
 ```
 
 There are several options for outputting to Vercel. See the [documentation](https://github.com/simonw/datasette-publish-vercel/blob/main/README.md) for more details
 
 ## Using with Datasette
 
 The SQLite database produced by this tool is designed to be browsed using [Datasette](https://datasette.readthedocs.io/). See my post [Adding Search to My Pelican Blog with Datasette](https://www.ryancheley.com/2022/01/16/adding-search-to-my-pelican-blog-with-datasette/) for more details on how I implemented it.
-
-
```

### Comparing `pelican-to-sqlite-0.5.0/README.md` & `pelican-to-sqlite-0.6.0/README.md`

 * *Files identical despite different names*

### Comparing `pelican-to-sqlite-0.5.0/pelican_to_sqlite.egg-info/PKG-INFO` & `pelican-to-sqlite-0.6.0/pelican_to_sqlite.egg-info/PKG-INFO`

 * *Files 9% similar despite different names*

```diff
@@ -1,19 +1,17 @@
 Metadata-Version: 2.1
 Name: pelican-to-sqlite
-Version: 0.5.0
-Summary: CLI tool for loading local pelican markdown files into a SQLite database
-Home-page: https://github.com/ryancheley/pelican-to-sqlite
+Version: 0.6.0
+Summary: A Pelican Plugin for outputting your Pelican posts into a SQLite Database
 Author: Ryan Cheley
-License: Apache License, Version 2.0
+License: Apache-2.0
 Project-URL: Issues, https://github.com/ryancheley/pelican-to-sqlite/issues
 Project-URL: CI, https://github.com/ryancheley/pelican-to-sqlite/actions
 Project-URL: Changelog, https://github.com/ryancheley/pelican-to-sqlite/releases
-Platform: UNKNOWN
-Requires-Python: >=3.7
+Classifier: Development Status :: 4 - Beta
 Description-Content-Type: text/markdown
 Provides-Extra: test
 License-File: LICENSE
 
 # pelican-to-sqlite
 
 [![PyPI](https://img.shields.io/pypi/v/pelican-to-sqlite.svg)](https://pypi.org/project/pelican-to-sqlite/)
@@ -79,9 +77,7 @@
 ```
 
 There are several options for outputting to Vercel. See the [documentation](https://github.com/simonw/datasette-publish-vercel/blob/main/README.md) for more details
 
 ## Using with Datasette
 
 The SQLite database produced by this tool is designed to be browsed using [Datasette](https://datasette.readthedocs.io/). See my post [Adding Search to My Pelican Blog with Datasette](https://www.ryancheley.com/2022/01/16/adding-search-to-my-pelican-blog-with-datasette/) for more details on how I implemented it.
-
-
```

