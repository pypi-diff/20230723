# Comparing `tmp/volsite_postgres_common-0.1.80.tar.gz` & `tmp/volsite_postgres_common-0.1.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "volsite_postgres_common-0.1.80.tar", last modified: Sun Jul 23 01:49:28 2023, max compression
+gzip compressed data, was "volsite_postgres_common-0.1.9.tar", last modified: Thu Jan 26 09:21:45 2023, max compression
```

## Comparing `volsite_postgres_common-0.1.80.tar` & `volsite_postgres_common-0.1.9.tar`

### file list

```diff
@@ -1,73 +1,59 @@
-drwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-07-23 01:49:28.110991 volsite_postgres_common-0.1.80/
--rw-rw-r--   0 gobi      (1000) gobi      (1000)      172 2023-07-23 01:49:28.110991 volsite_postgres_common-0.1.80/PKG-INFO
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)       31 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/README.rst
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)      107 2023-07-23 01:49:28.110991 volsite_postgres_common-0.1.80/setup.cfg
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)      415 2023-07-23 01:49:25.000000 volsite_postgres_common-0.1.80/setup.py
-drwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-07-23 01:49:28.102991 volsite_postgres_common-0.1.80/src/
-drwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-07-23 01:49:28.102991 volsite_postgres_common-0.1.80/src/volsite_postgres_common/
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/__init__.py
-drwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-07-23 01:49:28.102991 volsite_postgres_common-0.1.80/src/volsite_postgres_common/api/
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/api/__init__.py
-drwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-07-23 01:49:28.102991 volsite_postgres_common-0.1.80/src/volsite_postgres_common/api/enum/
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/api/enum/__init__.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)      658 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/api/enum/enum.py
-drwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-07-23 01:49:28.106991 volsite_postgres_common-0.1.80/src/volsite_postgres_common/db/
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)     2402 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/db/BFn.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)     1796 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/db/CC.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)     1608 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/db/CFn.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)      643 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/db/FnT.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/db/__init__.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)      192 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/db/migration.py
-drwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-07-23 01:49:28.106991 volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)      513 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/AInsertFunction.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)     4263 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/SQL.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/__init__.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)     3104 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/function.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)     2997 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/general.py
-drwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-07-23 01:49:28.106991 volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/http_status/
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)      674 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/http_status/FnHttpStatusData.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)      693 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/http_status/FnHttpStatusError.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)      773 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/http_status/FnHttpStatusErrorCodeOnly.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)      785 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/http_status/InsertHttpStatusFn.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/http_status/__init__.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)     3107 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/id.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)      133 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/insert.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)     6061 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/json.py
-drwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-07-23 01:49:28.106991 volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/search/
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)     3499 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/search/AFnSearchBookList.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)     5146 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/search/AFnSearchPagination.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/search/__init__.py
-drwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-07-23 01:49:28.106991 volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/title_description/
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)     1527 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/title_description/APFnUpsertDescription.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)     1291 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/title_description/APFnUpsertTitle.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)     2384 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/title_description/APFnUpsertTitleDescriptionB64.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/title_description/__init__.py
-drwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-07-23 01:49:28.110991 volsite_postgres_common-0.1.80/src/volsite_postgres_common/table/
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/table/__init__.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)     1203 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/table/create_table_descriptions.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)     1293 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/table/create_table_titles.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)      595 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/table/description.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)      757 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/table/series.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)      951 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/table/text.py
-drwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-07-23 01:49:28.110991 volsite_postgres_common-0.1.80/src/volsite_postgres_common/test/
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)      996 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/test/UserPool.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/test/__init__.py
-drwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-07-23 01:49:28.110991 volsite_postgres_common-0.1.80/src/volsite_postgres_common/test/api/
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)      424 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/test/api/OAPI.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)     3775 2023-07-23 01:49:12.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/test/api/OpenApiValidation.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/test/api/__init__.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)     1227 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/test/api/db_fn_open_api_validation.py
-drwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-07-23 01:49:28.110991 volsite_postgres_common-0.1.80/src/volsite_postgres_common/test/db/
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)      153 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/test/db/TestDb.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)      278 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/test/db/TestSetUser.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/test/db/__init__.py
-drwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-07-23 01:49:28.110991 volsite_postgres_common-0.1.80/src/volsite_postgres_common/test/db/book_list/
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/test/db/book_list/__init__.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)     2156 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/test/db/book_list/assert_sort.py
--rwxrwxr-x   0 gobi      (1000) gobi      (1000)      448 2023-07-22 14:39:31.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common/test/db/db_response_util.py
-drwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-07-23 01:49:28.102991 volsite_postgres_common-0.1.80/src/volsite_postgres_common.egg-info/
--rw-rw-r--   0 gobi      (1000) gobi      (1000)      172 2023-07-23 01:49:28.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common.egg-info/PKG-INFO
--rw-rw-r--   0 gobi      (1000) gobi      (1000)     2735 2023-07-23 01:49:28.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common.egg-info/SOURCES.txt
--rw-rw-r--   0 gobi      (1000) gobi      (1000)        1 2023-07-23 01:49:28.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common.egg-info/dependency_links.txt
--rw-rw-r--   0 gobi      (1000) gobi      (1000)       38 2023-07-23 01:49:28.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common.egg-info/requires.txt
--rw-rw-r--   0 gobi      (1000) gobi      (1000)       24 2023-07-23 01:49:28.000000 volsite_postgres_common-0.1.80/src/volsite_postgres_common.egg-info/top_level.txt
+drwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-01-26 09:21:45.311820 volsite_postgres_common-0.1.9/
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)      234 2023-01-26 09:21:45.311820 volsite_postgres_common-0.1.9/PKG-INFO
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)       31 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/README.rst
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)      107 2023-01-26 09:21:45.311820 volsite_postgres_common-0.1.9/setup.cfg
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)      378 2023-01-26 09:21:40.000000 volsite_postgres_common-0.1.9/setup.py
+drwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-01-26 09:21:45.303820 volsite_postgres_common-0.1.9/src/
+drwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-01-26 09:21:45.303820 volsite_postgres_common-0.1.9/src/volsite_postgres_common/
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)      259 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/Base64Utf8.py
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)        0 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/__init__.py
+drwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-01-26 09:21:45.307819 volsite_postgres_common-0.1.9/src/volsite_postgres_common/api/
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)     3222 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/api/CA.py
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)        0 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/api/__init__.py
+drwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-01-26 09:21:45.307819 volsite_postgres_common-0.1.9/src/volsite_postgres_common/api/enum/
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)        0 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/api/enum/__init__.py
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)       77 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/api/enum/common_error_code.py
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)      658 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/api/enum/enum.py
+drwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-01-26 09:21:45.307819 volsite_postgres_common-0.1.9/src/volsite_postgres_common/db/
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)     2124 2023-01-26 09:19:47.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/db/BFn.py
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)      681 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/db/CC.py
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)     1037 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/db/CFn.py
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)      410 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/db/FnT.py
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)        0 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/db/__init__.py
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)      192 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/db/migration.py
+drwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-01-26 09:21:45.307819 volsite_postgres_common-0.1.9/src/volsite_postgres_common/fn/
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)      513 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/fn/AInsertFunction.py
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)        0 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/fn/__init__.py
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)     3114 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/fn/function.py
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)     1431 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/fn/general.py
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)     2450 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/fn/id.py
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)      133 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/fn/insert.py
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)     5160 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/fn/json.py
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)     1486 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/fn/sql_segments.py
+drwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-01-26 09:21:45.307819 volsite_postgres_common-0.1.9/src/volsite_postgres_common/fn/title_description/
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)     1527 2023-01-26 08:28:07.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/fn/title_description/APFnUpsertDescription.py
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)     1291 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/fn/title_description/APFnUpsertTitle.py
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)     2410 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/fn/title_description/APFnUpsertTitleDescriptionB64.py
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)        0 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/fn/title_description/__init__.py
+drwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-01-26 09:21:45.307819 volsite_postgres_common-0.1.9/src/volsite_postgres_common/table/
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)        0 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/table/__init__.py
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)     1203 2023-01-26 07:39:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/table/create_table_descriptions.py
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)     1293 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/table/create_table_titles.py
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)      595 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/table/description.py
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)      802 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/table/series.py
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)      951 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/table/text.py
+drwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-01-26 09:21:45.307819 volsite_postgres_common-0.1.9/src/volsite_postgres_common/test/
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)      515 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/test/Timer.py
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)        0 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/test/__init__.py
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)      787 2023-01-23 23:33:26.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/test/assert_util.py
+drwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-01-26 09:21:45.311820 volsite_postgres_common-0.1.9/src/volsite_postgres_common/test/db/
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)      154 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/test/db/ATestDb.py
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)      282 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/test/db/ATestSetUser.py
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)        0 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/test/db/__init__.py
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)      885 2023-01-22 07:41:08.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common/test/dokuwiki.py
+drwxrwxr-x   0 gobi      (1000) gobi      (1000)        0 2023-01-26 09:21:45.307819 volsite_postgres_common-0.1.9/src/volsite_postgres_common.egg-info/
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)      234 2023-01-26 09:21:45.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common.egg-info/PKG-INFO
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)     2092 2023-01-26 09:21:45.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common.egg-info/SOURCES.txt
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)        1 2023-01-26 09:21:45.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common.egg-info/dependency_links.txt
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)       15 2023-01-26 09:21:45.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common.egg-info/requires.txt
+-rw-rw-r--   0 gobi      (1000) gobi      (1000)       24 2023-01-26 09:21:45.000000 volsite_postgres_common-0.1.9/src/volsite_postgres_common.egg-info/top_level.txt
```

### Comparing `volsite_postgres_common-0.1.80/src/volsite_postgres_common/api/enum/enum.py` & `volsite_postgres_common-0.1.9/src/volsite_postgres_common/api/enum/enum.py`

 * *Files identical despite different names*

### Comparing `volsite_postgres_common-0.1.80/src/volsite_postgres_common/db/BFn.py` & `volsite_postgres_common-0.1.9/src/volsite_postgres_common/db/BFn.py`

 * *Files 10% similar despite different names*

```diff
@@ -12,61 +12,57 @@
     array_to_string: Final[str] = 'array_to_string'
 
     cardinality: Final[str] = 'cardinality'
     coalesce: Final[str] = 'coalesce'
     concat: Final[str] = 'concat'
     convert_from: Final[str] = 'convert_from'
     crypt: Final[str] = 'crypt'
-    clock_timestamp: Final[str] = 'clock_timestamp'
     current_timestamp: Final[str] = 'current_timestamp'
 
     decode: Final[str] = 'decode'
 
     encode: Final[str] = 'encode'
     enum_range: Final[str] = 'enum_range'
 
     gen_salt: Final[str] = 'gen_salt'
 
     icount: Final[str] = 'icount'  # number of elements in array
 
     jsonb_array_length: Final[str] = 'jsonb_array_length'
+
+    lower: Final[str] = 'lower'
+
+    quote_ident: Final[str] = 'quote_ident'
+
     jsonb_agg: Final[str] = 'jsonb_agg'
     jsonb_array_elements: Final[str] = 'jsonb_array_elements'
     jsonb_array_elements_text: Final[str] = 'jsonb_array_elements_text'
     jsonb_build_array: Final[str] = 'jsonb_build_array'
     jsonb_build_object: Final[str] = 'jsonb_build_object'
     jsonb_each: Final[str] = 'jsonb_each'
     jsonb_object_agg: Final[str] = 'jsonb_object_agg'
     jsonb_object_keys: Final[str] = 'jsonb_object_keys'
-    jsonb_set: Final[str] = 'jsonb_set'
     jsonb_strip_nulls: Final[str] = 'jsonb_strip_nulls'
 
     length: Final[str] = 'length'
-    lower: Final[str] = 'lower'
 
     nextval: Final[str] = 'nextval'
 
     percentile_cont: Final[str] = 'percentile_cont'
     pg_get_serial_sequence: Final[str] = 'pg_get_serial_sequence'
 
-    quote_ident: Final[str] = 'quote_ident'
-
     regexp_matches: Final[str] = 'regexp_matches'
-    replace: Final[str] = 'replace'
 
     sha256: Final[str] = 'sha256'
     similarity: Final[str] = 'similarity'
     sort: Final[str] = 'sort'
     sort_asc: Final[str] = 'sort_asc'
     sort_desc: Final[str] = 'sort_desc'
-    statement_timestamp: Final[str] = 'statement_timestamp'
     split_part: Final[str] = 'split_part'
     substring: Final[str] = 'substring'
     sum: Final[str] = 'sum'
 
-    to_jsonb: Final[str] = 'to_jsonb'
     trim: Final[str] = 'trim'
 
     uniq: Final[str] = 'uniq'
-    uuid_generate_v4: Final[str] = 'uuid_generate_v4'
 
     word_similarity: Final[str] = 'word_similarity'
```

### Comparing `volsite_postgres_common-0.1.80/src/volsite_postgres_common/db/CFn.py` & `volsite_postgres_common-0.1.9/src/volsite_postgres_common/db/CFn.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,38 +1,26 @@
 from typing import Final
 
 
 # ====== CFn: Common Custom Function ======
 class CFn:
     array_sort: Final[str] = 'array_sort'
-    array_sort_unique: Final[str] = 'array_sort_unique'
 
     bigint_2_id: Final[str] = 'bigint_2_id'
-    bigint_array_2_id_array: Final[str] = 'bigint_array_2_id_array'
 
     count_jsonb_keys: Final[str] = 'count_jsonb_keys'
 
-    http_status_data: Final[str] = 'http_status_data'
-    http_status_error: Final[str] = 'http_status_error'
-    http_status_error_code_only: Final[str] = 'http_status_error_code_only'
-
     id_2_bigint: Final[str] = 'id_2_bigint'
     id_2_int: Final[str] = 'id_2_int'
     if_null_2_empty_bigint_array: Final[str] = 'if_null_2_empty_bigint_array'
-    if_null_2_empty_uuid_array: Final[str] = 'if_null_2_empty_uuid_array'
     int_2_id: Final[str] = 'int_2_id'
     is_null: Final[str] = 'is_null'
 
     jsonb_add_key_value_elements: Final[str] = 'jsonb_add_key_value_elements'
     jsonb_array_2_bigint_array: Final[str] = 'jsonb_array_2_bigint_array'
     jsonb_array_2_int_array: Final[str] = 'jsonb_array_2_int_array'
-    jsonb_2_jsonb_array: Final[str] = 'jsonb_2_jsonb_array'
     jsonb_array_2_smallint_array: Final[str] = 'jsonb_array_2_smallint_array'
     jsonb_array_2_text_array: Final[str] = 'jsonb_array_2_text_array'
-    jsonb_array_2_uuid_array: Final[str] = 'jsonb_array_2_uuid_array'
     jsonb_remove_key: Final[str] = 'jsonb_remove_key'
 
     jsonb_id_array_2_bigint_array: Final[str] = 'jsonb_id_array_2_bigint_array'
     jsonb_id_array_2_int_array: Final[str] = 'jsonb_id_array_2_int_array'
-
-    is_text_in_array: Final[str] = 'is_text_in_array'
-
```

### Comparing `volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/AInsertFunction.py` & `volsite_postgres_common-0.1.9/src/volsite_postgres_common/fn/AInsertFunction.py`

 * *Files identical despite different names*

### Comparing `volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/function.py` & `volsite_postgres_common-0.1.9/src/volsite_postgres_common/fn/function.py`

 * *Files 2% similar despite different names*

```diff
@@ -4,20 +4,20 @@
 from volsite_postgres_common.db.FnT import FnT
 
 
 class Arg:
     input: Final[str] = "_input"
     result: Final[str] = "_result"
 
-    def __init__(self, name: str, d_type: str):
+    def __init__(self, name: str, d_type: FnT):
         self.name = name
         self.type = d_type
 
     def to_str(self) -> str:
-        return f"{self.name}\t{self.type}"
+        return f"{self.name}\t{self.type.value}"
 
 
 class APlPgSqlFunction(metaclass=abc.ABCMeta):
 
     @abc.abstractmethod
     def name(self) -> str:
         raise NotImplementedError
@@ -82,15 +82,15 @@
         raise NotImplementedError
 
     @abc.abstractmethod
     def in_args(self) -> list:
         raise NotImplementedError
 
     @abc.abstractmethod
-    def return_type(self) -> str:
+    def return_type(self) -> FnT:
         raise NotImplementedError
 
     @abc.abstractmethod
     def body(self) -> str:
         raise NotImplementedError
 
     def build_function(self) -> str:
@@ -101,15 +101,15 @@
             for i in self.in_args():
                 args.append(f" {i.to_str()}")
             fn += ",\n".join(args)
             fn += "\n )\n"
         if self.return_type() is None:
             fn += " RETURNS VOID\n"
         else:
-            fn += f" RETURNS {self.return_type()} \n"
+            fn += f" RETURNS {self.return_type().value} \n"
         fn += " AS \n"
         fn += " $$ \n\n"
         fn += self.body()
         fn += "\n\n $$ \n"
         fn += " LANGUAGE SQL;"
 
         return fn
@@ -117,10 +117,9 @@
 
 class AJsonSqlFunction(ASqlFunction, metaclass=abc.ABCMeta):
     def in_args(self) -> list:
         return [
             Arg(Arg.input, FnT.JSONB)
         ]
 
-    def return_type(self) -> str:
-        return FnT.JSONB
-
+    def return_type(self) -> FnT:
+        return FnT.JSONB
```

### Comparing `volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/general.py` & `volsite_postgres_common-0.1.9/src/volsite_postgres_common/fn/general.py`

 * *Files 17% similar despite different names*

```diff
@@ -23,49 +23,14 @@
     f" AS"
     f" $$"
     f"   SELECT ARRAY(SELECT unnest($1) ORDER BY 1)"
     f" $$ "
     f" LANGUAGE SQL "
     f" IMMUTABLE;")
 
-# @ref https://stackoverflow.com/questions/3994556/eliminate-duplicate-array-values-in-postgres
-array_sort_unique: Final = (
-    f" CREATE OR REPLACE FUNCTION "
-    f" {CFn.array_sort_unique} (ANYARRAY) "
-    f" RETURNS ANYARRAY "
-    f" AS"
-    f" $$"
-    f"   SELECT ARRAY( "
-    f"     SELECT DISTINCT $1[s.i]  "
-    f"     FROM generate_series(array_lower($1,1), array_upper($1,1)) AS s(i)  "
-    f"     ORDER BY 1  "
-    f"               );"
-    f" $$ "
-    f" LANGUAGE SQL "
-    f" IMMUTABLE;")
-
-is_text_in_array: Final = (
-    f" CREATE OR REPLACE FUNCTION "
-    f" {CFn.is_text_in_array} (    "
-    f"      search_text text, "
-    f"      text_array text[]) "
-    f" RETURNS BOOLEAN "
-    f" AS"
-    f" $$"
-    f" DECLARE"
-    f"  found boolean;"
-    f" BEGIN"
-    f"   SELECT search_text = ANY(text_array) INTO found; "
-    f"   RETURN found;"
-    f" END;"
-    f" $$ "
-    f" LANGUAGE PlPgSQL "
-    f" IMMUTABLE;")
-
-
 if_null_2_empty_bigint_array: Final = (
     f" CREATE OR REPLACE FUNCTION "
     f" {CFn.if_null_2_empty_bigint_array} ("
     f" IN _input BIGINT[], "
     f" OUT _result BIGINT[]"
     f" ) "
     f" AS"
@@ -77,33 +42,12 @@
     f"  END IF;"
     f"  _result := _input;"
     f" END;"
     f" $$ "
     f" LANGUAGE PlPgSql "
     f" ;")
 
-if_null_2_empty_uuid_array: Final = (
-    f" CREATE OR REPLACE FUNCTION "
-    f" {CFn.if_null_2_empty_uuid_array} ("
-    f" IN _input UUID[], "
-    f" OUT _result UUID[]"
-    f" ) "
-    f" AS"
-    f" $$"
-    f" BEGIN "
-    f"  IF _input IS NULL THEN"
-    f"      _result := ARRAY[]::UUID[];"
-    f"      RETURN;"
-    f"  END IF;"
-    f"  _result := _input;"
-    f" END;"
-    f" $$ "
-    f" LANGUAGE PlPgSql "
-    f" ;")
 
 def insert_util_fn__general(conn):
     insert_function(is_null, CFn.is_null, conn)
     insert_function(array_sort, CFn.array_sort, conn)
-    insert_function(array_sort_unique, CFn.array_sort_unique, conn)
     insert_function(if_null_2_empty_bigint_array, CFn.if_null_2_empty_bigint_array, conn)
-    insert_function(if_null_2_empty_uuid_array, CFn.if_null_2_empty_uuid_array, conn)
-    insert_function(is_text_in_array, CFn.is_text_in_array, conn)
```

### Comparing `volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/id.py` & `volsite_postgres_common-0.1.9/src/volsite_postgres_common/fn/id.py`

 * *Files 7% similar despite different names*

```diff
@@ -77,43 +77,15 @@
     f"   SELECT array_agg({CFn.id_2_int}(x))::INT[] || ARRAY[]::INT[] "
     f"      FROM {BFn.jsonb_array_elements_text}($1) t(x);"
     f" $$ "
     f" LANGUAGE SQL "
     f" IMMUTABLE;")
 
 
-bigint_array_2_id_array: Final = (
-    f" CREATE OR REPLACE FUNCTION "
-    f" {CFn.bigint_array_2_id_array} ("
-    f" IN _input BIGINT[], "
-    f" OUT _result TEXT[]"
-    f" ) "
-    f" AS"
-    f" $$"
-    f" DECLARE"
-    f"   _text_id   BIGINT;"
-    f" BEGIN "
-    f"  _result := ARRAY[]::TEXT[];"
-    f"  IF _input IS NULL THEN"
-    f"      RETURN;"
-    f"  END IF;"
-    f""
-    f" FOREACH _text_id IN ARRAY _input "
-    f" LOOP "
-    f"   _result := _result || bigint_2_id(_text_id); "
-    f" END LOOP;"
-    f""
-    f" END;"
-    f" $$ "
-    f" LANGUAGE PlPgSql "
-    f" ;")
-
 def insert_util_fn__id(conn):
     insert_function(bigint_2_id, CFn.bigint_2_id, conn)
     insert_function(int_2_id, CFn.int_2_id, conn)
     insert_function(id_2_bigint, CFn.id_2_bigint, conn)
     insert_function(id_2_int, CFn.id_2_int, conn)
 
-    insert_function(bigint_array_2_id_array, CFn.bigint_array_2_id_array, conn)
-
     insert_function(jsonb_id_array_2_bigint_array, CFn.jsonb_id_array_2_bigint_array, conn)
     insert_function(jsonb_id_array_2_int_array, CFn.jsonb_id_array_2_int_array, conn)
```

### Comparing `volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/json.py` & `volsite_postgres_common-0.1.9/src/volsite_postgres_common/fn/json.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,16 +1,15 @@
 from psycopg2._json import Json
 from typing import Final
 import json
-from volworld_common.api.CA import CA
+from volsite_postgres_common.api.CA import CA
 from volsite_postgres_common.db.BFn import BFn
 from volsite_postgres_common.db.CFn import CFn
-from volworld_common.test.Timer import Timer
-from volsite_postgres_common.test.db.TestDb import TestDb
-from volworld_common.util.json import print_json_by_attributes
+from volsite_postgres_common.test.Timer import Timer
+from volsite_postgres_common.test.db.ATestDb import ATestDb
 
 
 def json_fn(fn: str, input_j: dict, conn, attList,
             do_commit: bool = False,
             print_input_output: bool = True,
             print_long_att: bool = True):  # -> dict:
     cursor = conn.cursor()
@@ -32,39 +31,36 @@
     if print_input_output:
         print('=== Output ===')
         print('<code>')
         print_json_by_attributes(output, attList, print_long_att)
         print('</code>')
     return output
 
-# def convert_json_by_attributes(j, attList) -> str:
-#     abb_att = {}
-#
-#     for a in attList:
-#         for name in a.__dict__:
-#             abb = a.__dict__[name]
-#             abb_att[f"\"{abb}\":"] = f"\"{abb}__{name}\":"
-#
-#     res = json.dumps(j, indent=4, sort_keys=True)
-#     for att in abb_att.keys():
-#         res = res.replace(att, abb_att[att])
-#
-#     return res
-
-# def print_json_by_attributes(j, attList, print_long_att: bool = False):
-#     if not print_long_att:
-#         print(json.dumps(j, indent=4, sort_keys=True))
-#         return
-#
-#     print(convert_json_by_attributes(j, attList))
+
+def print_json_by_attributes(j, attList, print_long_att: bool = False):
+    if not print_long_att:
+        print(json.dumps(j, indent=4, sort_keys=True))
+        return
+
+    abb_att = {}
+
+    for a in attList:
+        for name in a.__dict__:
+            abb = a.__dict__[name]
+            abb_att[f"\"{abb}\":"] = f"\"{abb}__{name}\":"
+
+    res = json.dumps(j, indent=4, sort_keys=True)
+    for att in abb_att.keys():
+        res = res.replace(att, abb_att[att])
+    print(res)
 
 
 def json_fn_db(
         fn: str, input_j: dict,
-        test_db: TestDb, attList,
+        test_db: ATestDb, attList,
         do_commit: bool = False,
         print_long_att: bool = True):  # -> dict:
     with Timer(fn):
         return json_fn(fn, input_j, test_db.p_conn, attList,
                        do_commit=do_commit,
                        print_input_output=test_db.print_input_output,
                        print_long_att=print_long_att)
@@ -106,34 +102,14 @@
     f" RETURNS TEXT[] "
     f" AS $$ "
     f"   SELECT array_agg(x)::TEXT[] || ARRAY[]::TEXT[] FROM {BFn.jsonb_array_elements_text}($1) t(x);"
     f" $$ "
     f" LANGUAGE SQL "
     f" IMMUTABLE;")
 
-fn_jsonb_array_2_uuid_array: Final = (
-    f" CREATE OR REPLACE FUNCTION "
-    f" {CFn.jsonb_array_2_uuid_array} (JSONB) "
-    f" RETURNS UUID[] "
-    f" AS $$ "
-    f"   SELECT array_agg(x)::UUID[] || ARRAY[]::UUID[] FROM {BFn.jsonb_array_elements_text}($1) t(x);"
-    f" $$ "
-    f" LANGUAGE SQL "
-    f" IMMUTABLE;")
-
-fn_jsonb_2_jsonb_array: Final = (
-    f" CREATE OR REPLACE FUNCTION "
-    f" {CFn.jsonb_2_jsonb_array} (JSONB) "
-    f" RETURNS JSONB[] "
-    f" AS $$ "
-    f"   SELECT array_agg(x)::JSONB[] || ARRAY[]::JSONB[] FROM {BFn.jsonb_array_elements}($1) t(x);"
-    f" $$ "
-    f" LANGUAGE SQL "
-    f" IMMUTABLE;")
-
 fn_jsonb_remove_key: Final = (
     f" CREATE OR REPLACE FUNCTION "
     f" {CFn.jsonb_remove_key} (JSONB, TEXT) "
     f" RETURNS JSONB "
     f" AS $$ "
     f"   SELECT $1 - $2;"
     f" $$ "
@@ -178,14 +154,12 @@
 
 def insert_util_fn__json(conn):
     cursor = conn.cursor()
     cursor.execute(fn_jsonb_array_2_bigint_array)
     cursor.execute(fn_jsonb_array_2_int_array)
     cursor.execute(fn_jsonb_array_2_smallint_array)
     cursor.execute(fn_jsonb_array_2_text_array)
-    cursor.execute(fn_jsonb_array_2_uuid_array)
-    cursor.execute(fn_jsonb_2_jsonb_array)
     cursor.execute(fn_jsonb_remove_key)
     cursor.execute(fn_count_jsonb_keys)
     # cursor.execute(fn_jsonb_add_key_value)
     cursor.execute(fn_jsonb_add_key_val_elements)
     conn.commit()
```

### Comparing `volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/title_description/APFnUpsertDescription.py` & `volsite_postgres_common-0.1.9/src/volsite_postgres_common/fn/title_description/APFnUpsertDescription.py`

 * *Files identical despite different names*

### Comparing `volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/title_description/APFnUpsertTitle.py` & `volsite_postgres_common-0.1.9/src/volsite_postgres_common/fn/title_description/APFnUpsertTitle.py`

 * *Files identical despite different names*

### Comparing `volsite_postgres_common-0.1.80/src/volsite_postgres_common/fn/title_description/APFnUpsertTitleDescriptionB64.py` & `volsite_postgres_common-0.1.9/src/volsite_postgres_common/fn/title_description/APFnUpsertTitleDescriptionB64.py`

 * *Files 6% similar despite different names*

```diff
@@ -3,15 +3,15 @@
 from typing import Final
 
 from volsite_postgres_common.db.FnT import FnT
 from volsite_postgres_common.db.BFn import BFn
 from volsite_postgres_common.db.CFn import CFn
 from volsite_postgres_common.fn.function import AJsonPlPgSqlFunction, Arg
 
-from volworld_common.api.CA import CA
+from volsite_postgres_common.api.CA import CA
 
 
 class APFnUpsertTitleDescriptionB64(AJsonPlPgSqlFunction, ABC):
 
     _title_id: Final[str] = '_title_id'
     _description_id: Final[str] = '_description_id'
 
@@ -44,19 +44,19 @@
             Arg(self._des_plain, FnT.TEXT),
             Arg(self._des_format, FnT.TEXT)
         ]
 
     def body(self) -> str:
         return (
             f" {self._title} := {BFn.convert_from}( "
-            f"      {BFn.decode}( ({Arg.input}->>'{self.input_a_title()}')::{FnT.TEXT}, 'base64'), 'UTF-8');"
+            f"      {BFn.decode}( ({Arg.input}->>'{self.input_a_title()}')::{FnT.TEXT.value}, 'base64'), 'UTF-8');"
             f" {self._des_plain} := {BFn.convert_from}( "
-            f"      {BFn.decode}( ({Arg.input}->>'{CA.DescriptionPlain}')::{FnT.TEXT}, 'base64'), 'UTF-8');"
+            f"      {BFn.decode}( ({Arg.input}->>'{CA.DescriptionPlain}')::{FnT.TEXT.value}, 'base64'), 'UTF-8');"
             f" {self._des_format} := {BFn.convert_from}( "
-            f"      {BFn.decode}( ({Arg.input}->>'{CA.DescriptionFormatted}')::{FnT.TEXT}, 'base64'), 'UTF-8');"
+            f"      {BFn.decode}( ({Arg.input}->>'{CA.DescriptionFormatted}')::{FnT.TEXT.value}, 'base64'), 'UTF-8');"
             f""
             f" {self._title_id} := {self.pfn_title___upsert()}({self._title}); "
             f" {self._description_id} := {self.pfn_description___upsert()}({self._des_format}, {self._des_plain}); "
             f" {Arg.result} := {BFn.jsonb_build_object}("
             f"       '{self.output_a_title_id()}', {CFn.bigint_2_id}({self._title_id}),"
             f"       '{CA.DescriptionId}', {CFn.bigint_2_id}({self._description_id}) "
             f"   );"
```

### Comparing `volsite_postgres_common-0.1.80/src/volsite_postgres_common/table/create_table_descriptions.py` & `volsite_postgres_common-0.1.9/src/volsite_postgres_common/table/create_table_descriptions.py`

 * *Files identical despite different names*

### Comparing `volsite_postgres_common-0.1.80/src/volsite_postgres_common/table/create_table_titles.py` & `volsite_postgres_common-0.1.9/src/volsite_postgres_common/table/create_table_titles.py`

 * *Files identical despite different names*

### Comparing `volsite_postgres_common-0.1.80/src/volsite_postgres_common/table/description.py` & `volsite_postgres_common-0.1.9/src/volsite_postgres_common/table/description.py`

 * *Files identical despite different names*

### Comparing `volsite_postgres_common-0.1.80/src/volsite_postgres_common/table/text.py` & `volsite_postgres_common-0.1.9/src/volsite_postgres_common/table/text.py`

 * *Files identical despite different names*

### Comparing `volsite_postgres_common-0.1.80/src/volsite_postgres_common.egg-info/SOURCES.txt` & `volsite_postgres_common-0.1.9/src/volsite_postgres_common.egg-info/SOURCES.txt`

 * *Files 23% similar despite different names*

```diff
@@ -1,56 +1,46 @@
 README.rst
 setup.cfg
 setup.py
+src/volsite_postgres_common/Base64Utf8.py
 src/volsite_postgres_common/__init__.py
 src/volsite_postgres_common.egg-info/PKG-INFO
 src/volsite_postgres_common.egg-info/SOURCES.txt
 src/volsite_postgres_common.egg-info/dependency_links.txt
 src/volsite_postgres_common.egg-info/requires.txt
 src/volsite_postgres_common.egg-info/top_level.txt
+src/volsite_postgres_common/api/CA.py
 src/volsite_postgres_common/api/__init__.py
 src/volsite_postgres_common/api/enum/__init__.py
+src/volsite_postgres_common/api/enum/common_error_code.py
 src/volsite_postgres_common/api/enum/enum.py
 src/volsite_postgres_common/db/BFn.py
 src/volsite_postgres_common/db/CC.py
 src/volsite_postgres_common/db/CFn.py
 src/volsite_postgres_common/db/FnT.py
 src/volsite_postgres_common/db/__init__.py
 src/volsite_postgres_common/db/migration.py
 src/volsite_postgres_common/fn/AInsertFunction.py
-src/volsite_postgres_common/fn/SQL.py
 src/volsite_postgres_common/fn/__init__.py
 src/volsite_postgres_common/fn/function.py
 src/volsite_postgres_common/fn/general.py
 src/volsite_postgres_common/fn/id.py
 src/volsite_postgres_common/fn/insert.py
 src/volsite_postgres_common/fn/json.py
-src/volsite_postgres_common/fn/http_status/FnHttpStatusData.py
-src/volsite_postgres_common/fn/http_status/FnHttpStatusError.py
-src/volsite_postgres_common/fn/http_status/FnHttpStatusErrorCodeOnly.py
-src/volsite_postgres_common/fn/http_status/InsertHttpStatusFn.py
-src/volsite_postgres_common/fn/http_status/__init__.py
-src/volsite_postgres_common/fn/search/AFnSearchBookList.py
-src/volsite_postgres_common/fn/search/AFnSearchPagination.py
-src/volsite_postgres_common/fn/search/__init__.py
+src/volsite_postgres_common/fn/sql_segments.py
 src/volsite_postgres_common/fn/title_description/APFnUpsertDescription.py
 src/volsite_postgres_common/fn/title_description/APFnUpsertTitle.py
 src/volsite_postgres_common/fn/title_description/APFnUpsertTitleDescriptionB64.py
 src/volsite_postgres_common/fn/title_description/__init__.py
 src/volsite_postgres_common/table/__init__.py
 src/volsite_postgres_common/table/create_table_descriptions.py
 src/volsite_postgres_common/table/create_table_titles.py
 src/volsite_postgres_common/table/description.py
 src/volsite_postgres_common/table/series.py
 src/volsite_postgres_common/table/text.py
-src/volsite_postgres_common/test/UserPool.py
+src/volsite_postgres_common/test/Timer.py
 src/volsite_postgres_common/test/__init__.py
-src/volsite_postgres_common/test/api/OAPI.py
-src/volsite_postgres_common/test/api/OpenApiValidation.py
-src/volsite_postgres_common/test/api/__init__.py
-src/volsite_postgres_common/test/api/db_fn_open_api_validation.py
-src/volsite_postgres_common/test/db/TestDb.py
-src/volsite_postgres_common/test/db/TestSetUser.py
-src/volsite_postgres_common/test/db/__init__.py
-src/volsite_postgres_common/test/db/db_response_util.py
-src/volsite_postgres_common/test/db/book_list/__init__.py
-src/volsite_postgres_common/test/db/book_list/assert_sort.py
+src/volsite_postgres_common/test/assert_util.py
+src/volsite_postgres_common/test/dokuwiki.py
+src/volsite_postgres_common/test/db/ATestDb.py
+src/volsite_postgres_common/test/db/ATestSetUser.py
+src/volsite_postgres_common/test/db/__init__.py
```

