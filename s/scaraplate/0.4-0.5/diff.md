# Comparing `tmp/scaraplate-0.4.tar.gz` & `tmp/scaraplate-0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist/scaraplate-0.4.tar", last modified: Sat Nov 12 12:36:43 2022, max compression
+gzip compressed data, was "dist/scaraplate-0.5.tar", last modified: Sun Jul 23 14:30:14 2023, max compression
```

## Comparing `scaraplate-0.4.tar` & `scaraplate-0.5.tar`

### file list

```diff
@@ -1,62 +1,62 @@
-drwxr-xr-x   0 kostya     (501) staff       (20)        0 2022-11-12 12:36:43.000000 scaraplate-0.4/
--rw-r--r--   0 kostya     (501) staff       (20)     1082 2019-07-26 19:42:41.000000 scaraplate-0.4/LICENSE
--rw-r--r--   0 kostya     (501) staff       (20)      145 2019-10-22 20:05:10.000000 scaraplate-0.4/MANIFEST.in
--rw-r--r--   0 kostya     (501) staff       (20)     2313 2022-11-12 12:36:43.000000 scaraplate-0.4/PKG-INFO
--rw-r--r--   0 kostya     (501) staff       (20)     1209 2022-11-12 11:49:17.000000 scaraplate-0.4/README.md
--rw-r--r--   0 kostya     (501) staff       (20)        3 2022-11-12 12:36:43.000000 scaraplate-0.4/VERSION
--rw-r--r--   0 kostya     (501) staff       (20)     2704 2022-11-12 12:36:43.000000 scaraplate-0.4/setup.cfg
--rwxr-xr-x   0 kostya     (501) staff       (20)     1878 2022-11-12 12:00:29.000000 scaraplate-0.4/setup.py
-drwxr-xr-x   0 kostya     (501) staff       (20)        0 2022-11-12 12:36:43.000000 scaraplate-0.4/src/
-drwxr-xr-x   0 kostya     (501) staff       (20)        0 2022-11-12 12:36:43.000000 scaraplate-0.4/src/scaraplate/
--rw-r--r--   0 kostya     (501) staff       (20)      427 2022-11-12 12:00:29.000000 scaraplate-0.4/src/scaraplate/__init__.py
--rw-r--r--   0 kostya     (501) staff       (20)     2422 2022-11-12 12:00:31.000000 scaraplate-0.4/src/scaraplate/__main__.py
-drwxr-xr-x   0 kostya     (501) staff       (20)        0 2022-11-12 12:36:43.000000 scaraplate-0.4/src/scaraplate/automation/
--rw-r--r--   0 kostya     (501) staff       (20)      246 2022-11-12 12:00:29.000000 scaraplate-0.4/src/scaraplate/automation/__init__.py
--rw-r--r--   0 kostya     (501) staff       (20)     4123 2022-11-12 12:00:29.000000 scaraplate-0.4/src/scaraplate/automation/base.py
--rw-r--r--   0 kostya     (501) staff       (20)    13823 2022-11-12 12:33:43.000000 scaraplate-0.4/src/scaraplate/automation/git.py
--rw-r--r--   0 kostya     (501) staff       (20)    10503 2022-11-12 12:00:34.000000 scaraplate-0.4/src/scaraplate/automation/gitlab.py
--rw-r--r--   0 kostya     (501) staff       (20)      717 2022-11-12 12:00:31.000000 scaraplate-0.4/src/scaraplate/compat.py
--rw-r--r--   0 kostya     (501) staff       (20)     4232 2022-11-12 12:00:29.000000 scaraplate-0.4/src/scaraplate/config.py
--rw-r--r--   0 kostya     (501) staff       (20)     3794 2022-11-12 12:00:32.000000 scaraplate-0.4/src/scaraplate/cookiecutter.py
--rw-r--r--   0 kostya     (501) staff       (20)      438 2020-05-11 03:01:14.000000 scaraplate-0.4/src/scaraplate/fields.py
--rw-r--r--   0 kostya     (501) staff       (20)     3173 2019-07-26 19:42:41.000000 scaraplate-0.4/src/scaraplate/gitremotes.py
--rw-r--r--   0 kostya     (501) staff       (20)        0 2019-10-22 20:02:07.000000 scaraplate-0.4/src/scaraplate/py.typed
--rw-r--r--   0 kostya     (501) staff       (20)    10841 2022-11-12 12:00:29.000000 scaraplate-0.4/src/scaraplate/rollup.py
--rw-r--r--   0 kostya     (501) staff       (20)    28995 2022-11-12 12:00:31.000000 scaraplate-0.4/src/scaraplate/strategies.py
--rw-r--r--   0 kostya     (501) staff       (20)     2418 2022-11-11 23:17:28.000000 scaraplate-0.4/src/scaraplate/template.py
-drwxr-xr-x   0 kostya     (501) staff       (20)        0 2022-11-12 12:36:43.000000 scaraplate-0.4/src/scaraplate.egg-info/
--rw-r--r--   0 kostya     (501) staff       (20)     2313 2022-11-12 12:36:43.000000 scaraplate-0.4/src/scaraplate.egg-info/PKG-INFO
--rw-r--r--   0 kostya     (501) staff       (20)     1570 2022-11-12 12:36:43.000000 scaraplate-0.4/src/scaraplate.egg-info/SOURCES.txt
--rw-r--r--   0 kostya     (501) staff       (20)        1 2022-11-12 12:36:43.000000 scaraplate-0.4/src/scaraplate.egg-info/dependency_links.txt
--rw-r--r--   0 kostya     (501) staff       (20)       56 2022-11-12 12:36:43.000000 scaraplate-0.4/src/scaraplate.egg-info/entry_points.txt
--rw-r--r--   0 kostya     (501) staff       (20)      310 2022-11-12 12:36:43.000000 scaraplate-0.4/src/scaraplate.egg-info/requires.txt
--rw-r--r--   0 kostya     (501) staff       (20)       11 2022-11-12 12:36:43.000000 scaraplate-0.4/src/scaraplate.egg-info/top_level.txt
-drwxr-xr-x   0 kostya     (501) staff       (20)        0 2022-11-12 12:36:43.000000 scaraplate-0.4/tests/
--rw-r--r--   0 kostya     (501) staff       (20)        0 2019-01-26 10:03:39.000000 scaraplate-0.4/tests/__init__.py
-drwxr-xr-x   0 kostya     (501) staff       (20)        0 2022-11-12 12:36:43.000000 scaraplate-0.4/tests/automation/
--rw-r--r--   0 kostya     (501) staff       (20)        0 2019-10-22 19:40:24.000000 scaraplate-0.4/tests/automation/__init__.py
--rw-r--r--   0 kostya     (501) staff       (20)     6317 2022-11-12 12:00:32.000000 scaraplate-0.4/tests/automation/conftest.py
--rw-r--r--   0 kostya     (501) staff       (20)     8341 2022-11-12 12:00:32.000000 scaraplate-0.4/tests/automation/test_git.py
--rw-r--r--   0 kostya     (501) staff       (20)     2269 2019-10-22 19:40:24.000000 scaraplate-0.4/tests/automation/test_git_wrapper.py
--rw-r--r--   0 kostya     (501) staff       (20)     7379 2022-11-12 12:00:31.000000 scaraplate-0.4/tests/automation/test_gitlab.py
--rw-r--r--   0 kostya     (501) staff       (20)     1428 2022-11-12 12:33:43.000000 scaraplate-0.4/tests/conftest.py
-drwxr-xr-x   0 kostya     (501) staff       (20)        0 2022-11-12 12:36:43.000000 scaraplate-0.4/tests/strategies/
--rw-r--r--   0 kostya     (501) staff       (20)        0 2019-10-20 14:45:44.000000 scaraplate-0.4/tests/strategies/__init__.py
--rw-r--r--   0 kostya     (501) staff       (20)     3103 2022-11-12 12:00:29.000000 scaraplate-0.4/tests/strategies/conftest.py
--rw-r--r--   0 kostya     (501) staff       (20)     3870 2019-10-20 14:45:44.000000 scaraplate-0.4/tests/strategies/test_config_parser_merge.yml
--rw-r--r--   0 kostya     (501) staff       (20)     2810 2019-07-26 19:42:41.000000 scaraplate-0.4/tests/strategies/test_config_parser_merge_pylintrc.yml
--rw-r--r--   0 kostya     (501) staff       (20)     2060 2019-10-20 14:45:44.000000 scaraplate-0.4/tests/strategies/test_detect_newline.py
--rw-r--r--   0 kostya     (501) staff       (20)      388 2019-10-20 14:45:44.000000 scaraplate-0.4/tests/strategies/test_if_missing.yml
--rw-r--r--   0 kostya     (501) staff       (20)      210 2019-07-26 19:42:41.000000 scaraplate-0.4/tests/strategies/test_no_extra_keys_schema.yml
--rw-r--r--   0 kostya     (501) staff       (20)      144 2019-10-20 14:45:44.000000 scaraplate-0.4/tests/strategies/test_overwrite.yml
--rw-r--r--   0 kostya     (501) staff       (20)     4656 2019-10-06 13:45:06.000000 scaraplate-0.4/tests/strategies/test_rendered_template_file_hash.yml
--rw-r--r--   0 kostya     (501) staff       (20)     5892 2019-10-20 14:45:44.000000 scaraplate-0.4/tests/strategies/test_setupcfg_merge.yml
--rw-r--r--   0 kostya     (501) staff       (20)     2260 2019-10-20 14:45:44.000000 scaraplate-0.4/tests/strategies/test_sorted_unique_lines.yml
--rw-r--r--   0 kostya     (501) staff       (20)     4143 2019-10-20 14:45:44.000000 scaraplate-0.4/tests/strategies/test_template_hash.yml
--rw-r--r--   0 kostya     (501) staff       (20)     1251 2019-10-13 18:49:06.000000 scaraplate-0.4/tests/test_cli.py
--rw-r--r--   0 kostya     (501) staff       (20)     7509 2019-10-20 14:45:44.000000 scaraplate-0.4/tests/test_config.py
--rw-r--r--   0 kostya     (501) staff       (20)     2259 2019-07-26 19:42:41.000000 scaraplate-0.4/tests/test_cookecutter.py
--rw-r--r--   0 kostya     (501) staff       (20)     4254 2019-07-26 19:42:41.000000 scaraplate-0.4/tests/test_gitremotes.py
--rw-r--r--   0 kostya     (501) staff       (20)      283 2019-01-26 10:03:39.000000 scaraplate-0.4/tests/test_metadata.py
--rw-r--r--   0 kostya     (501) staff       (20)    11851 2022-11-12 12:00:32.000000 scaraplate-0.4/tests/test_rollup.py
--rw-r--r--   0 kostya     (501) staff       (20)     2516 2019-10-22 19:40:24.000000 scaraplate-0.4/tests/test_template.py
+drwxr-xr-x   0 kostya     (501) staff       (20)        0 2023-07-23 14:30:14.000000 scaraplate-0.5/
+-rw-r--r--   0 kostya     (501) staff       (20)     1082 2019-07-26 19:42:41.000000 scaraplate-0.5/LICENSE
+-rw-r--r--   0 kostya     (501) staff       (20)      145 2019-10-22 20:05:10.000000 scaraplate-0.5/MANIFEST.in
+-rw-r--r--   0 kostya     (501) staff       (20)     2336 2023-07-23 14:30:14.000000 scaraplate-0.5/PKG-INFO
+-rw-r--r--   0 kostya     (501) staff       (20)     1231 2023-07-23 14:27:55.000000 scaraplate-0.5/README.md
+-rw-r--r--   0 kostya     (501) staff       (20)        3 2023-07-23 14:30:14.000000 scaraplate-0.5/VERSION
+-rw-r--r--   0 kostya     (501) staff       (20)     2716 2023-07-23 14:30:14.000000 scaraplate-0.5/setup.cfg
+-rwxr-xr-x   0 kostya     (501) staff       (20)     1878 2022-11-12 12:00:29.000000 scaraplate-0.5/setup.py
+drwxr-xr-x   0 kostya     (501) staff       (20)        0 2023-07-23 14:30:14.000000 scaraplate-0.5/src/
+drwxr-xr-x   0 kostya     (501) staff       (20)        0 2023-07-23 14:30:14.000000 scaraplate-0.5/src/scaraplate/
+-rw-r--r--   0 kostya     (501) staff       (20)      427 2022-11-12 12:00:29.000000 scaraplate-0.5/src/scaraplate/__init__.py
+-rw-r--r--   0 kostya     (501) staff       (20)     2422 2022-11-12 12:00:31.000000 scaraplate-0.5/src/scaraplate/__main__.py
+drwxr-xr-x   0 kostya     (501) staff       (20)        0 2023-07-23 14:30:14.000000 scaraplate-0.5/src/scaraplate/automation/
+-rw-r--r--   0 kostya     (501) staff       (20)      246 2022-11-12 12:00:29.000000 scaraplate-0.5/src/scaraplate/automation/__init__.py
+-rw-r--r--   0 kostya     (501) staff       (20)     4123 2022-11-12 12:00:29.000000 scaraplate-0.5/src/scaraplate/automation/base.py
+-rw-r--r--   0 kostya     (501) staff       (20)    13823 2022-11-12 12:33:43.000000 scaraplate-0.5/src/scaraplate/automation/git.py
+-rw-r--r--   0 kostya     (501) staff       (20)    10503 2022-11-12 12:00:34.000000 scaraplate-0.5/src/scaraplate/automation/gitlab.py
+-rw-r--r--   0 kostya     (501) staff       (20)      717 2022-11-12 12:00:31.000000 scaraplate-0.5/src/scaraplate/compat.py
+-rw-r--r--   0 kostya     (501) staff       (20)     4232 2022-11-12 12:00:29.000000 scaraplate-0.5/src/scaraplate/config.py
+-rw-r--r--   0 kostya     (501) staff       (20)     3794 2022-11-12 12:00:32.000000 scaraplate-0.5/src/scaraplate/cookiecutter.py
+-rw-r--r--   0 kostya     (501) staff       (20)      438 2020-05-11 03:01:14.000000 scaraplate-0.5/src/scaraplate/fields.py
+-rw-r--r--   0 kostya     (501) staff       (20)     3173 2019-07-26 19:42:41.000000 scaraplate-0.5/src/scaraplate/gitremotes.py
+-rw-r--r--   0 kostya     (501) staff       (20)        0 2019-10-22 20:02:07.000000 scaraplate-0.5/src/scaraplate/py.typed
+-rw-r--r--   0 kostya     (501) staff       (20)    10887 2023-07-23 13:43:23.000000 scaraplate-0.5/src/scaraplate/rollup.py
+-rw-r--r--   0 kostya     (501) staff       (20)    28995 2022-11-12 12:00:31.000000 scaraplate-0.5/src/scaraplate/strategies.py
+-rw-r--r--   0 kostya     (501) staff       (20)     2418 2022-11-11 23:17:28.000000 scaraplate-0.5/src/scaraplate/template.py
+drwxr-xr-x   0 kostya     (501) staff       (20)        0 2023-07-23 14:30:14.000000 scaraplate-0.5/src/scaraplate.egg-info/
+-rw-r--r--   0 kostya     (501) staff       (20)     2336 2023-07-23 14:30:14.000000 scaraplate-0.5/src/scaraplate.egg-info/PKG-INFO
+-rw-r--r--   0 kostya     (501) staff       (20)     1570 2023-07-23 14:30:14.000000 scaraplate-0.5/src/scaraplate.egg-info/SOURCES.txt
+-rw-r--r--   0 kostya     (501) staff       (20)        1 2023-07-23 14:30:14.000000 scaraplate-0.5/src/scaraplate.egg-info/dependency_links.txt
+-rw-r--r--   0 kostya     (501) staff       (20)       56 2023-07-23 14:30:14.000000 scaraplate-0.5/src/scaraplate.egg-info/entry_points.txt
+-rw-r--r--   0 kostya     (501) staff       (20)      309 2023-07-23 14:30:14.000000 scaraplate-0.5/src/scaraplate.egg-info/requires.txt
+-rw-r--r--   0 kostya     (501) staff       (20)       11 2023-07-23 14:30:14.000000 scaraplate-0.5/src/scaraplate.egg-info/top_level.txt
+drwxr-xr-x   0 kostya     (501) staff       (20)        0 2023-07-23 14:30:14.000000 scaraplate-0.5/tests/
+-rw-r--r--   0 kostya     (501) staff       (20)        0 2019-01-26 10:03:39.000000 scaraplate-0.5/tests/__init__.py
+drwxr-xr-x   0 kostya     (501) staff       (20)        0 2023-07-23 14:30:14.000000 scaraplate-0.5/tests/automation/
+-rw-r--r--   0 kostya     (501) staff       (20)        0 2019-10-22 19:40:24.000000 scaraplate-0.5/tests/automation/__init__.py
+-rw-r--r--   0 kostya     (501) staff       (20)     6578 2023-07-23 13:36:31.000000 scaraplate-0.5/tests/automation/conftest.py
+-rw-r--r--   0 kostya     (501) staff       (20)     8367 2023-07-23 13:36:31.000000 scaraplate-0.5/tests/automation/test_git.py
+-rw-r--r--   0 kostya     (501) staff       (20)     2269 2019-10-22 19:40:24.000000 scaraplate-0.5/tests/automation/test_git_wrapper.py
+-rw-r--r--   0 kostya     (501) staff       (20)     7379 2022-11-12 12:00:31.000000 scaraplate-0.5/tests/automation/test_gitlab.py
+-rw-r--r--   0 kostya     (501) staff       (20)     1728 2023-07-23 13:39:51.000000 scaraplate-0.5/tests/conftest.py
+drwxr-xr-x   0 kostya     (501) staff       (20)        0 2023-07-23 14:30:14.000000 scaraplate-0.5/tests/strategies/
+-rw-r--r--   0 kostya     (501) staff       (20)        0 2019-10-20 14:45:44.000000 scaraplate-0.5/tests/strategies/__init__.py
+-rw-r--r--   0 kostya     (501) staff       (20)     3103 2022-11-12 12:00:29.000000 scaraplate-0.5/tests/strategies/conftest.py
+-rw-r--r--   0 kostya     (501) staff       (20)     3870 2019-10-20 14:45:44.000000 scaraplate-0.5/tests/strategies/test_config_parser_merge.yml
+-rw-r--r--   0 kostya     (501) staff       (20)     2810 2019-07-26 19:42:41.000000 scaraplate-0.5/tests/strategies/test_config_parser_merge_pylintrc.yml
+-rw-r--r--   0 kostya     (501) staff       (20)     2060 2019-10-20 14:45:44.000000 scaraplate-0.5/tests/strategies/test_detect_newline.py
+-rw-r--r--   0 kostya     (501) staff       (20)      388 2019-10-20 14:45:44.000000 scaraplate-0.5/tests/strategies/test_if_missing.yml
+-rw-r--r--   0 kostya     (501) staff       (20)      210 2019-07-26 19:42:41.000000 scaraplate-0.5/tests/strategies/test_no_extra_keys_schema.yml
+-rw-r--r--   0 kostya     (501) staff       (20)      144 2019-10-20 14:45:44.000000 scaraplate-0.5/tests/strategies/test_overwrite.yml
+-rw-r--r--   0 kostya     (501) staff       (20)     4656 2019-10-06 13:45:06.000000 scaraplate-0.5/tests/strategies/test_rendered_template_file_hash.yml
+-rw-r--r--   0 kostya     (501) staff       (20)     5892 2019-10-20 14:45:44.000000 scaraplate-0.5/tests/strategies/test_setupcfg_merge.yml
+-rw-r--r--   0 kostya     (501) staff       (20)     2260 2019-10-20 14:45:44.000000 scaraplate-0.5/tests/strategies/test_sorted_unique_lines.yml
+-rw-r--r--   0 kostya     (501) staff       (20)     4143 2019-10-20 14:45:44.000000 scaraplate-0.5/tests/strategies/test_template_hash.yml
+-rw-r--r--   0 kostya     (501) staff       (20)     1251 2019-10-13 18:49:06.000000 scaraplate-0.5/tests/test_cli.py
+-rw-r--r--   0 kostya     (501) staff       (20)     7509 2019-10-20 14:45:44.000000 scaraplate-0.5/tests/test_config.py
+-rw-r--r--   0 kostya     (501) staff       (20)     2259 2019-07-26 19:42:41.000000 scaraplate-0.5/tests/test_cookecutter.py
+-rw-r--r--   0 kostya     (501) staff       (20)     4254 2019-07-26 19:42:41.000000 scaraplate-0.5/tests/test_gitremotes.py
+-rw-r--r--   0 kostya     (501) staff       (20)      283 2019-01-26 10:03:39.000000 scaraplate-0.5/tests/test_metadata.py
+-rw-r--r--   0 kostya     (501) staff       (20)    11987 2023-07-23 13:36:31.000000 scaraplate-0.5/tests/test_rollup.py
+-rw-r--r--   0 kostya     (501) staff       (20)     2516 2019-10-22 19:40:24.000000 scaraplate-0.5/tests/test_template.py
```

### Comparing `scaraplate-0.4/LICENSE` & `scaraplate-0.5/LICENSE`

 * *Files identical despite different names*

### Comparing `scaraplate-0.4/PKG-INFO` & `scaraplate-0.5/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 Metadata-Version: 2.1
 Name: scaraplate
-Version: 0.4
+Version: 0.5
 Summary: Scaraplate is a wrapper around cookiecutter which allows to repeatedly rollup project templates onto concrete projects.
 Home-page: https://github.com/rambler-digital-solutions/scaraplate
 Author: Usermodel @ Rambler&Co
 Author-email: um@rambler-co.ru
 Maintainer: Kostya Esmukov
-Maintainer-email: kostya@esmukov.ru
+Maintainer-email: kostya@esmukov.net
 License: MIT
 Project-URL: Docs, https://scaraplate.readthedocs.io/
 Project-URL: Issue Tracker, https://github.com/rambler-digital-solutions/scaraplate/issues
 Project-URL: Source Code, https://github.com/rambler-digital-solutions/scaraplate
 Classifier: Development Status :: 4 - Beta
 Classifier: Environment :: Console
 Classifier: Intended Audience :: Developers
@@ -29,22 +29,22 @@
 
 [![GitHub Actions Build status][gha-badge]][gha-link]
 [![scaraplate on pypi][pypi-badge]][pypi-link]
 [![docs at readthedocs][docs-badge]][docs-link]
 [![Licensed under MIT][license-badge]][license-link]
 [![Code style: black][black-badge]][black-link]
 
-[gha-badge]: https://img.shields.io/github/workflow/status/rambler-digital-solutions/scaraplate/CI
+[gha-badge]: https://img.shields.io/github/actions/workflow/status/rambler-digital-solutions/scaraplate/ci.yml?branch=main
 [gha-link]: https://github.com/rambler-digital-solutions/scaraplate/actions
 [pypi-badge]: https://img.shields.io/pypi/v/scaraplate.svg
 [pypi-link]: https://pypi.org/project/scaraplate/
 [docs-badge]: https://readthedocs.org/projects/scaraplate/badge/?version=latest
 [docs-link]: https://scaraplate.readthedocs.io/
 [license-badge]: https://scaraplate.readthedocs.io/en/latest/_static/license.svg
-[license-link]: https://github.com/rambler-digital-solutions/scaraplate/blob/master/LICENSE
+[license-link]: https://github.com/rambler-digital-solutions/scaraplate/blob/main/LICENSE
 [black-badge]: https://img.shields.io/badge/code%20style-black-000000.svg
 [black-link]: https://github.com/psf/black
 
 
 Scaraplate is a wrapper around [cookiecutter][cookiecutter]
 which allows to repeatedly rollup project templates onto concrete projects.
```

### Comparing `scaraplate-0.4/README.md` & `scaraplate-0.5/README.md`

 * *Files 13% similar despite different names*

```diff
@@ -2,22 +2,22 @@
 
 [![GitHub Actions Build status][gha-badge]][gha-link]
 [![scaraplate on pypi][pypi-badge]][pypi-link]
 [![docs at readthedocs][docs-badge]][docs-link]
 [![Licensed under MIT][license-badge]][license-link]
 [![Code style: black][black-badge]][black-link]
 
-[gha-badge]: https://img.shields.io/github/workflow/status/rambler-digital-solutions/scaraplate/CI
+[gha-badge]: https://img.shields.io/github/actions/workflow/status/rambler-digital-solutions/scaraplate/ci.yml?branch=main
 [gha-link]: https://github.com/rambler-digital-solutions/scaraplate/actions
 [pypi-badge]: https://img.shields.io/pypi/v/scaraplate.svg
 [pypi-link]: https://pypi.org/project/scaraplate/
 [docs-badge]: https://readthedocs.org/projects/scaraplate/badge/?version=latest
 [docs-link]: https://scaraplate.readthedocs.io/
 [license-badge]: https://scaraplate.readthedocs.io/en/latest/_static/license.svg
-[license-link]: https://github.com/rambler-digital-solutions/scaraplate/blob/master/LICENSE
+[license-link]: https://github.com/rambler-digital-solutions/scaraplate/blob/main/LICENSE
 [black-badge]: https://img.shields.io/badge/code%20style-black-000000.svg
 [black-link]: https://github.com/psf/black
 
 
 Scaraplate is a wrapper around [cookiecutter][cookiecutter]
 which allows to repeatedly rollup project templates onto concrete projects.
```

### Comparing `scaraplate-0.4/setup.cfg` & `scaraplate-0.5/setup.cfg`

 * *Files 9% similar despite different names*

```diff
@@ -38,19 +38,19 @@
 	License :: OSI Approved :: MIT License
 	Natural Language :: English
 	Operating System :: OS Independent
 	Programming Language :: Python :: 3 :: Only
 	Topic :: Software Development
 description = Scaraplate is a wrapper around cookiecutter which allows to repeatedly rollup project templates onto concrete projects.
 license = MIT
-license_file = LICENSE
+license_files = LICENSE
 long_description = file: README.md
 long_description_content_type = text/markdown
 maintainer = Kostya Esmukov
-maintainer_email = kostya@esmukov.ru
+maintainer_email = kostya@esmukov.net
 name = scaraplate
 project_urls = 
 	Docs = https://scaraplate.readthedocs.io/
 	Issue Tracker = https://github.com/rambler-digital-solutions/scaraplate/issues
 	Source Code = https://github.com/rambler-digital-solutions/scaraplate
 url = https://github.com/rambler-digital-solutions/scaraplate
 version = 
@@ -78,22 +78,22 @@
 
 [options.entry_points]
 console_scripts = 
 	scaraplate = scaraplate.__main__:main
 
 [options.extras_require]
 develop = 
-	black==22.10.0
-	coverage==6.5.0
+	black==23.3.0
+	coverage==7.2.7
 	flake8==5.0.4
-	isort==5.10.1
-	mypy==0.990
-	pylint==2.15.5
-	pytest==7.2.0
-	sphinx-rtd-theme==1.1.1
+	isort==5.11.5
+	mypy==1.4.1
+	pylint==2.17.4
+	pytest==7.4.0
+	sphinx-rtd-theme==1.2.2
 	sphinx==4.3.2
 	types-PyYAML
 	types-setuptools
 gitlab = 
 	python-gitlab>=1.6.0,<4
 
 [options.packages.find]
@@ -115,12 +115,13 @@
 
 [tool:pytest]
 addopts = 
 	-ra
 	--junitxml=junit.xml
 	--showlocals
 	--verbose
+	--verbose
 
 [egg_info]
 tag_build = 
 tag_date = 0
```

### Comparing `scaraplate-0.4/setup.py` & `scaraplate-0.5/setup.py`

 * *Files identical despite different names*

### Comparing `scaraplate-0.4/src/scaraplate/__main__.py` & `scaraplate-0.5/src/scaraplate/__main__.py`

 * *Files identical despite different names*

### Comparing `scaraplate-0.4/src/scaraplate/automation/base.py` & `scaraplate-0.5/src/scaraplate/automation/base.py`

 * *Files identical despite different names*

### Comparing `scaraplate-0.4/src/scaraplate/automation/git.py` & `scaraplate-0.5/src/scaraplate/automation/git.py`

 * *Files identical despite different names*

### Comparing `scaraplate-0.4/src/scaraplate/automation/gitlab.py` & `scaraplate-0.5/src/scaraplate/automation/gitlab.py`

 * *Files identical despite different names*

### Comparing `scaraplate-0.4/src/scaraplate/compat.py` & `scaraplate-0.5/src/scaraplate/compat.py`

 * *Files identical despite different names*

### Comparing `scaraplate-0.4/src/scaraplate/config.py` & `scaraplate-0.5/src/scaraplate/config.py`

 * *Files identical despite different names*

### Comparing `scaraplate-0.4/src/scaraplate/cookiecutter.py` & `scaraplate-0.5/src/scaraplate/cookiecutter.py`

 * *Files identical despite different names*

### Comparing `scaraplate-0.4/src/scaraplate/gitremotes.py` & `scaraplate-0.5/src/scaraplate/gitremotes.py`

 * *Files identical despite different names*

### Comparing `scaraplate-0.4/src/scaraplate/rollup.py` & `scaraplate-0.5/src/scaraplate/rollup.py`

 * *Files 1% similar despite different names*

```diff
@@ -81,16 +81,16 @@
         # Give cookiecutter a fake config so it would write its stuff
         # to the tempdir, which would then be removed.
         cookiecutter_config_path = Path(tempdir_path) / "cookiecutter_home"
         cookiecutter_config_path.mkdir(parents=True)
         cookiecutter_config = cookiecutter_config_path / "cookiecutterrc.yaml"
         cookiecutter_config.write_text(
             f"""
-cookiecutters_dir: "{cookiecutter_config_path / 'cookiecutters'}"
-replay_dir: "{cookiecutter_config_path / 'replay'}"
+cookiecutters_dir: "{(cookiecutter_config_path.resolve() / 'cookiecutters').as_posix()}"
+replay_dir: "{(cookiecutter_config_path.resolve() / 'replay').as_posix()}"
 """
         )
 
         cookiecutter_context.setdefault(  # pylint: disable=no-member
             "project_dest", project_dest
         )
```

### Comparing `scaraplate-0.4/src/scaraplate/strategies.py` & `scaraplate-0.5/src/scaraplate/strategies.py`

 * *Files identical despite different names*

### Comparing `scaraplate-0.4/src/scaraplate/template.py` & `scaraplate-0.5/src/scaraplate/template.py`

 * *Files identical despite different names*

### Comparing `scaraplate-0.4/src/scaraplate.egg-info/PKG-INFO` & `scaraplate-0.5/src/scaraplate.egg-info/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,16 +1,16 @@
 Metadata-Version: 2.1
 Name: scaraplate
-Version: 0.4
+Version: 0.5
 Summary: Scaraplate is a wrapper around cookiecutter which allows to repeatedly rollup project templates onto concrete projects.
 Home-page: https://github.com/rambler-digital-solutions/scaraplate
 Author: Usermodel @ Rambler&Co
 Author-email: um@rambler-co.ru
 Maintainer: Kostya Esmukov
-Maintainer-email: kostya@esmukov.ru
+Maintainer-email: kostya@esmukov.net
 License: MIT
 Project-URL: Docs, https://scaraplate.readthedocs.io/
 Project-URL: Issue Tracker, https://github.com/rambler-digital-solutions/scaraplate/issues
 Project-URL: Source Code, https://github.com/rambler-digital-solutions/scaraplate
 Classifier: Development Status :: 4 - Beta
 Classifier: Environment :: Console
 Classifier: Intended Audience :: Developers
@@ -29,22 +29,22 @@
 
 [![GitHub Actions Build status][gha-badge]][gha-link]
 [![scaraplate on pypi][pypi-badge]][pypi-link]
 [![docs at readthedocs][docs-badge]][docs-link]
 [![Licensed under MIT][license-badge]][license-link]
 [![Code style: black][black-badge]][black-link]
 
-[gha-badge]: https://img.shields.io/github/workflow/status/rambler-digital-solutions/scaraplate/CI
+[gha-badge]: https://img.shields.io/github/actions/workflow/status/rambler-digital-solutions/scaraplate/ci.yml?branch=main
 [gha-link]: https://github.com/rambler-digital-solutions/scaraplate/actions
 [pypi-badge]: https://img.shields.io/pypi/v/scaraplate.svg
 [pypi-link]: https://pypi.org/project/scaraplate/
 [docs-badge]: https://readthedocs.org/projects/scaraplate/badge/?version=latest
 [docs-link]: https://scaraplate.readthedocs.io/
 [license-badge]: https://scaraplate.readthedocs.io/en/latest/_static/license.svg
-[license-link]: https://github.com/rambler-digital-solutions/scaraplate/blob/master/LICENSE
+[license-link]: https://github.com/rambler-digital-solutions/scaraplate/blob/main/LICENSE
 [black-badge]: https://img.shields.io/badge/code%20style-black-000000.svg
 [black-link]: https://github.com/psf/black
 
 
 Scaraplate is a wrapper around [cookiecutter][cookiecutter]
 which allows to repeatedly rollup project templates onto concrete projects.
```

### Comparing `scaraplate-0.4/src/scaraplate.egg-info/SOURCES.txt` & `scaraplate-0.5/src/scaraplate.egg-info/SOURCES.txt`

 * *Files identical despite different names*

### Comparing `scaraplate-0.4/tests/automation/conftest.py` & `scaraplate-0.5/tests/automation/conftest.py`

 * *Files 4% similar despite different names*

```diff
@@ -4,14 +4,20 @@
 from concurrent.futures import Future
 from pathlib import Path
 from typing import Any, Callable, List, Optional
 
 import pytest
 
 
+def pytest_configure(config):
+    config.addinivalue_line(
+        "markers", "template_with_sense_vars: write cookiecutter context to a file"
+    )
+
+
 def convert_git_repo_to_bare(call_git, *, cwd: Path) -> None:
     """Git bare repo is a git repo without a working copy. `git clone`
     can clone these repos my simply pointing at their location in the local
     filesystem.
     """
     # https://stackoverflow.com/a/3251126
     call_git("git config --bool core.bare true", cwd=cwd)
@@ -119,15 +125,19 @@
                     self.send_error(500, "request_handler is None")
                 else:
                     try:
                         # https://stackoverflow.com/a/20879937
                         body = self.rfile.read(
                             int(self.headers.get("content-length", 0))
                         )
-                        (code, headers, body,) = thread.request_handler(
+                        (
+                            code,
+                            headers,
+                            body,
+                        ) = thread.request_handler(
                             method, self.path, headers=self.headers, body=body
                         )
                         self.send_response(code)
                         for name, value in headers.items():
                             self.send_header(name, value)
                         self.end_headers()
                         self.wfile.write(body)
```

### Comparing `scaraplate-0.4/tests/automation/test_git.py` & `scaraplate-0.5/tests/automation/test_git.py`

 * *Files 0% similar despite different names*

```diff
@@ -209,14 +209,15 @@
 
     cookiecutter_context_text = call_git(
         f"git show {target_branch}:sense_vars", cwd=project_bare_git_repo
     )
 
     assert json.loads(cookiecutter_context_text) == {
         "_output_dir": ANY,
+        "_repo_dir": ANY,
         "_template": monorepo_inner_path if monorepo_inner_path else "remote_template",
         "project_dest": "remote_project",
         "key1": "value1",
         "key2": "value2",
     }
```

### Comparing `scaraplate-0.4/tests/automation/test_git_wrapper.py` & `scaraplate-0.5/tests/automation/test_git_wrapper.py`

 * *Files identical despite different names*

### Comparing `scaraplate-0.4/tests/automation/test_gitlab.py` & `scaraplate-0.5/tests/automation/test_gitlab.py`

 * *Files identical despite different names*

### Comparing `scaraplate-0.4/tests/conftest.py` & `scaraplate-0.5/tests/conftest.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 import os
 import subprocess
 import tempfile
 from pathlib import Path
+from unittest.mock import patch
 
 import pytest
 
 
 @pytest.fixture
 def tempdir_path():
     with tempfile.TemporaryDirectory() as tempdir_path:
@@ -23,23 +24,36 @@
                 "git remote add origin https://gitlab.localhost/nonexisting/repo.git",
                 cwd=path,
             )
 
     return _init_git_and_commit
 
 
+@pytest.fixture(scope="session", autouse=True)
+def mock_git_env():
+    os.environ.pop("SSH_AUTH_SOCK", None)
+    with patch.dict(
+        os.environ,
+        {
+            "GIT_CONFIG_NOSYSTEM": "1",
+            "GIT_CONFIG_GLOBAL": "",
+            "GIT_CONFIG_SYSTEM": "",
+        },
+    ):
+        yield
+
+
 @pytest.fixture
 def call_git():
     def _call_git(shell_cmd: str, cwd: Path) -> str:
         env = {
             "GIT_AUTHOR_EMAIL": "pytest@scaraplate",
             "GIT_AUTHOR_NAME": "tests_scaraplate",
             "GIT_COMMITTER_EMAIL": "pytest@scaraplate",
             "GIT_COMMITTER_NAME": "tests_scaraplate",
-            "GIT_CONFIG_NOSYSTEM": "1",
             "PATH": os.getenv("PATH", os.defpath),
         }
         out = subprocess.run(
             shell_cmd,
             shell=True,
             check=True,
             cwd=cwd,
```

### Comparing `scaraplate-0.4/tests/strategies/conftest.py` & `scaraplate-0.5/tests/strategies/conftest.py`

 * *Files identical despite different names*

### Comparing `scaraplate-0.4/tests/strategies/test_config_parser_merge.yml` & `scaraplate-0.5/tests/strategies/test_config_parser_merge.yml`

 * *Files identical despite different names*

### Comparing `scaraplate-0.4/tests/strategies/test_config_parser_merge_pylintrc.yml` & `scaraplate-0.5/tests/strategies/test_config_parser_merge_pylintrc.yml`

 * *Files identical despite different names*

### Comparing `scaraplate-0.4/tests/strategies/test_detect_newline.py` & `scaraplate-0.5/tests/strategies/test_detect_newline.py`

 * *Files identical despite different names*

### Comparing `scaraplate-0.4/tests/strategies/test_rendered_template_file_hash.yml` & `scaraplate-0.5/tests/strategies/test_rendered_template_file_hash.yml`

 * *Files identical despite different names*

### Comparing `scaraplate-0.4/tests/strategies/test_setupcfg_merge.yml` & `scaraplate-0.5/tests/strategies/test_setupcfg_merge.yml`

 * *Files identical despite different names*

### Comparing `scaraplate-0.4/tests/strategies/test_sorted_unique_lines.yml` & `scaraplate-0.5/tests/strategies/test_sorted_unique_lines.yml`

 * *Files identical despite different names*

### Comparing `scaraplate-0.4/tests/strategies/test_template_hash.yml` & `scaraplate-0.5/tests/strategies/test_template_hash.yml`

 * *Files identical despite different names*

### Comparing `scaraplate-0.4/tests/test_cli.py` & `scaraplate-0.5/tests/test_cli.py`

 * *Files identical despite different names*

### Comparing `scaraplate-0.4/tests/test_config.py` & `scaraplate-0.5/tests/test_config.py`

 * *Files identical despite different names*

### Comparing `scaraplate-0.4/tests/test_cookecutter.py` & `scaraplate-0.5/tests/test_cookecutter.py`

 * *Files identical despite different names*

### Comparing `scaraplate-0.4/tests/test_gitremotes.py` & `scaraplate-0.5/tests/test_gitremotes.py`

 * *Files identical despite different names*

### Comparing `scaraplate-0.4/tests/test_rollup.py` & `scaraplate-0.5/tests/test_rollup.py`

 * *Files 1% similar despite different names*

```diff
@@ -72,14 +72,15 @@
 
         assert "test mock!" == (target_project_path / "README.md").read_text()
         assert 0o755 == (0o777 & (target_project_path / "setup.py").stat().st_mode)
 
         with open((target_project_path / "sense_vars"), "rt") as f:
             assert json.load(f) == {
                 "_output_dir": ANY,
+                "_repo_dir": ANY,
                 "_template": "template",
                 "project_dest": "test",
             }
 
 
 def test_add_remove_template_var(tempdir_path, init_git_and_commit):
     template_path = tempdir_path / "template"
@@ -111,14 +112,15 @@
     rollup(
         template_dir=str(template_path),
         target_project_dir=str(target_project_path),
         no_input=True,
     )
     assert (target_project_path / ".scaraplate.conf").read_text() == (
         """[cookiecutter_context]
+_repo_dir = template
 _template = template
 project_dest = test
 removed_var = 42
 """
     )
 
     # Remove `removed_var` and add `added_var`
@@ -128,14 +130,15 @@
     rollup(
         template_dir=str(template_path),
         target_project_dir=str(target_project_path),
         no_input=True,
     )
     assert (target_project_path / ".scaraplate.conf").read_text() == (
         """[cookiecutter_context]
+_repo_dir = template
 _template = template
 added_var = 24
 project_dest = test
 """
     )
 
 
@@ -203,14 +206,15 @@
         target_project_dir=str(target_project_path),
         no_input=True,
         extra_context={"key1": "initial1", "key2": "initial2"},
     )
     with open((target_project_path / "sense_vars"), "rt") as f:
         assert json.load(f) == {
             "_output_dir": ANY,
+            "_repo_dir": ANY,
             "_template": "template",
             "project_dest": "test",
             "key1": "initial1",
             "key2": "initial2",
         }
 
     # A second rollup with a different context
@@ -219,14 +223,15 @@
         target_project_dir=str(target_project_path),
         no_input=True,
         extra_context={"key1": "second1", "key2": "second2"},
     )
     with open((target_project_path / "sense_vars"), "rt") as f:
         assert json.load(f) == {
             "_output_dir": ANY,
+            "_repo_dir": ANY,
             "_template": "template",
             "project_dest": "test",
             "key1": "second1",
             "key2": "second2",
         }
```

### Comparing `scaraplate-0.4/tests/test_template.py` & `scaraplate-0.5/tests/test_template.py`

 * *Files identical despite different names*

