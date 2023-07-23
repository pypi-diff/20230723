# Comparing `tmp/randog-0.7.0.tar.gz` & `tmp/randog-0.8.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "randog-0.7.0.tar", last modified: Tue Jul 18 15:18:09 2023, max compression
+gzip compressed data, was "randog-0.8.0.tar", last modified: Sun Jul 23 11:18:20 2023, max compression
```

## Comparing `randog-0.7.0.tar` & `randog-0.8.0.tar`

### file list

```diff
@@ -1,64 +1,66 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 15:18:09.731652 randog-0.7.0/
--rw-r--r--   0 runner    (1001) docker     (123)     1064 2023-07-18 15:17:57.000000 randog-0.7.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     2101 2023-07-18 15:18:09.731652 randog-0.7.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1096 2023-07-18 15:17:57.000000 randog-0.7.0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 15:18:09.719652 randog-0.7.0/randog/
--rw-r--r--   0 runner    (1001) docker     (123)      161 2023-07-18 15:17:57.000000 randog-0.7.0/randog/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     5955 2023-07-18 15:17:57.000000 randog-0.7.0/randog/__main__.py
--rw-r--r--   0 runner    (1001) docker     (123)      565 2023-07-18 15:17:57.000000 randog-0.7.0/randog/_examples.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 15:18:09.723652 randog-0.7.0/randog/_main/
--rw-r--r--   0 runner    (1001) docker     (123)      114 2023-07-18 15:17:57.000000 randog-0.7.0/randog/_main/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2827 2023-07-18 15:17:57.000000 randog-0.7.0/randog/_main/_main_args.py
--rw-r--r--   0 runner    (1001) docker     (123)      253 2023-07-18 15:17:57.000000 randog-0.7.0/randog/_main/_subcmd.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 15:18:09.727652 randog-0.7.0/randog/_main/_subcmd_def/
--rw-r--r--   0 runner    (1001) docker     (123)      996 2023-07-18 15:17:57.000000 randog-0.7.0/randog/_main/_subcmd_def/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2253 2023-07-18 15:17:57.000000 randog-0.7.0/randog/_main/_subcmd_def/_base.py
--rw-r--r--   0 runner    (1001) docker     (123)     1278 2023-07-18 15:17:57.000000 randog-0.7.0/randog/_main/_subcmd_def/_bool.py
--rw-r--r--   0 runner    (1001) docker     (123)     2074 2023-07-18 15:17:57.000000 randog-0.7.0/randog/_main/_subcmd_def/_byfile.py
--rw-r--r--   0 runner    (1001) docker     (123)     2884 2023-07-18 15:17:57.000000 randog-0.7.0/randog/_main/_subcmd_def/_date.py
--rw-r--r--   0 runner    (1001) docker     (123)     2883 2023-07-18 15:17:57.000000 randog-0.7.0/randog/_main/_subcmd_def/_datetime.py
--rw-r--r--   0 runner    (1001) docker     (123)     3484 2023-07-18 15:17:57.000000 randog-0.7.0/randog/_main/_subcmd_def/_decimal.py
--rw-r--r--   0 runner    (1001) docker     (123)     3091 2023-07-18 15:17:57.000000 randog-0.7.0/randog/_main/_subcmd_def/_float.py
--rw-r--r--   0 runner    (1001) docker     (123)     1622 2023-07-18 15:17:57.000000 randog-0.7.0/randog/_main/_subcmd_def/_int.py
--rw-r--r--   0 runner    (1001) docker     (123)     2314 2023-07-18 15:17:57.000000 randog-0.7.0/randog/_main/_subcmd_def/_str.py
--rw-r--r--   0 runner    (1001) docker     (123)     2654 2023-07-18 15:17:57.000000 randog-0.7.0/randog/_main/_subcmd_def/_time.py
--rw-r--r--   0 runner    (1001) docker     (123)     4578 2023-07-18 15:17:57.000000 randog-0.7.0/randog/_main/_subcmd_def/_timedelta.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 15:18:09.727652 randog-0.7.0/randog/_utils/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-18 15:17:57.000000 randog-0.7.0/randog/_utils/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      336 2023-07-18 15:17:57.000000 randog-0.7.0/randog/_utils/nullsafe.py
--rw-r--r--   0 runner    (1001) docker     (123)      974 2023-07-18 15:17:57.000000 randog-0.7.0/randog/_utils/type.py
--rw-r--r--   0 runner    (1001) docker     (123)      240 2023-07-18 15:17:57.000000 randog-0.7.0/randog/exceptions.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 15:18:09.731652 randog-0.7.0/randog/factory/
--rw-r--r--   0 runner    (1001) docker     (123)     1392 2023-07-18 15:17:57.000000 randog-0.7.0/randog/factory/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     4568 2023-07-18 15:17:57.000000 randog-0.7.0/randog/factory/_base.py
--rw-r--r--   0 runner    (1001) docker     (123)     1635 2023-07-18 15:17:57.000000 randog-0.7.0/randog/factory/_bool.py
--rw-r--r--   0 runner    (1001) docker     (123)      798 2023-07-18 15:17:57.000000 randog-0.7.0/randog/factory/_by_callable.py
--rw-r--r--   0 runner    (1001) docker     (123)      822 2023-07-18 15:17:57.000000 randog-0.7.0/randog/factory/_by_iterator.py
--rw-r--r--   0 runner    (1001) docker     (123)     3369 2023-07-18 15:17:57.000000 randog-0.7.0/randog/factory/_choice.py
--rw-r--r--   0 runner    (1001) docker     (123)      508 2023-07-18 15:17:57.000000 randog-0.7.0/randog/factory/_const.py
--rw-r--r--   0 runner    (1001) docker     (123)     2918 2023-07-18 15:17:57.000000 randog-0.7.0/randog/factory/_date.py
--rw-r--r--   0 runner    (1001) docker     (123)     4670 2023-07-18 15:17:57.000000 randog-0.7.0/randog/factory/_datetime.py
--rw-r--r--   0 runner    (1001) docker     (123)     3125 2023-07-18 15:17:57.000000 randog-0.7.0/randog/factory/_decimal.py
--rw-r--r--   0 runner    (1001) docker     (123)     3301 2023-07-18 15:17:57.000000 randog-0.7.0/randog/factory/_dict.py
--rw-r--r--   0 runner    (1001) docker     (123)     4124 2023-07-18 15:17:57.000000 randog-0.7.0/randog/factory/_float.py
--rw-r--r--   0 runner    (1001) docker     (123)    11444 2023-07-18 15:17:57.000000 randog-0.7.0/randog/factory/_from_example.py
--rw-r--r--   0 runner    (1001) docker     (123)     2616 2023-07-18 15:17:57.000000 randog-0.7.0/randog/factory/_from_pyfile.py
--rw-r--r--   0 runner    (1001) docker     (123)     1538 2023-07-18 15:17:57.000000 randog-0.7.0/randog/factory/_increment.py
--rw-r--r--   0 runner    (1001) docker     (123)     1655 2023-07-18 15:17:57.000000 randog-0.7.0/randog/factory/_int.py
--rw-r--r--   0 runner    (1001) docker     (123)     4357 2023-07-18 15:17:57.000000 randog-0.7.0/randog/factory/_list.py
--rw-r--r--   0 runner    (1001) docker     (123)     2591 2023-07-18 15:17:57.000000 randog-0.7.0/randog/factory/_str.py
--rw-r--r--   0 runner    (1001) docker     (123)     4137 2023-07-18 15:17:57.000000 randog-0.7.0/randog/factory/_time.py
--rw-r--r--   0 runner    (1001) docker     (123)     5270 2023-07-18 15:17:57.000000 randog-0.7.0/randog/factory/_timedelta.py
--rw-r--r--   0 runner    (1001) docker     (123)     2912 2023-07-18 15:17:57.000000 randog-0.7.0/randog/factory/_union.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 15:18:09.731652 randog-0.7.0/randog/sqlalchemy/
--rw-r--r--   0 runner    (1001) docker     (123)      157 2023-07-18 15:17:57.000000 randog-0.7.0/randog/sqlalchemy/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     6873 2023-07-18 15:17:57.000000 randog-0.7.0/randog/sqlalchemy/_construct.py
--rw-r--r--   0 runner    (1001) docker     (123)     1586 2023-07-18 15:17:57.000000 randog-0.7.0/randog/sqlalchemy/_custom_func.py
--rw-r--r--   0 runner    (1001) docker     (123)     9580 2023-07-18 15:17:57.000000 randog-0.7.0/randog/timedelta_util.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-18 15:18:09.723652 randog-0.7.0/randog.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     2101 2023-07-18 15:18:09.000000 randog-0.7.0/randog.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1476 2023-07-18 15:18:09.000000 randog-0.7.0/randog.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-18 15:18:09.000000 randog-0.7.0/randog.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)        7 2023-07-18 15:18:09.000000 randog-0.7.0/randog.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-18 15:18:09.731652 randog-0.7.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1039 2023-07-18 15:17:57.000000 randog-0.7.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 11:18:20.340670 randog-0.8.0/
+-rw-r--r--   0 runner    (1001) docker     (123)     1064 2023-07-23 11:18:10.000000 randog-0.8.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     2101 2023-07-23 11:18:20.340670 randog-0.8.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1096 2023-07-23 11:18:10.000000 randog-0.8.0/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 11:18:20.336670 randog-0.8.0/randog/
+-rw-r--r--   0 runner    (1001) docker     (123)      161 2023-07-23 11:18:10.000000 randog-0.8.0/randog/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6900 2023-07-23 11:18:10.000000 randog-0.8.0/randog/__main__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      565 2023-07-23 11:18:10.000000 randog-0.8.0/randog/_examples.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 11:18:20.336670 randog-0.8.0/randog/_main/
+-rw-r--r--   0 runner    (1001) docker     (123)      114 2023-07-23 11:18:10.000000 randog-0.8.0/randog/_main/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3166 2023-07-23 11:18:10.000000 randog-0.8.0/randog/_main/_main_args.py
+-rw-r--r--   0 runner    (1001) docker     (123)      253 2023-07-23 11:18:10.000000 randog-0.8.0/randog/_main/_subcmd.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 11:18:20.340670 randog-0.8.0/randog/_main/_subcmd_def/
+-rw-r--r--   0 runner    (1001) docker     (123)      996 2023-07-23 11:18:10.000000 randog-0.8.0/randog/_main/_subcmd_def/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2253 2023-07-23 11:18:10.000000 randog-0.8.0/randog/_main/_subcmd_def/_base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1278 2023-07-23 11:18:10.000000 randog-0.8.0/randog/_main/_subcmd_def/_bool.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3378 2023-07-23 11:18:10.000000 randog-0.8.0/randog/_main/_subcmd_def/_byfile.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2884 2023-07-23 11:18:10.000000 randog-0.8.0/randog/_main/_subcmd_def/_date.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2883 2023-07-23 11:18:10.000000 randog-0.8.0/randog/_main/_subcmd_def/_datetime.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3484 2023-07-23 11:18:10.000000 randog-0.8.0/randog/_main/_subcmd_def/_decimal.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3091 2023-07-23 11:18:10.000000 randog-0.8.0/randog/_main/_subcmd_def/_float.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1622 2023-07-23 11:18:10.000000 randog-0.8.0/randog/_main/_subcmd_def/_int.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3277 2023-07-23 11:18:10.000000 randog-0.8.0/randog/_main/_subcmd_def/_str.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2654 2023-07-23 11:18:10.000000 randog-0.8.0/randog/_main/_subcmd_def/_time.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4578 2023-07-23 11:18:10.000000 randog-0.8.0/randog/_main/_subcmd_def/_timedelta.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 11:18:20.340670 randog-0.8.0/randog/_utils/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 11:18:10.000000 randog-0.8.0/randog/_utils/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      336 2023-07-23 11:18:10.000000 randog-0.8.0/randog/_utils/nullsafe.py
+-rw-r--r--   0 runner    (1001) docker     (123)      974 2023-07-23 11:18:10.000000 randog-0.8.0/randog/_utils/type.py
+-rw-r--r--   0 runner    (1001) docker     (123)      240 2023-07-23 11:18:10.000000 randog-0.8.0/randog/exceptions.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 11:18:20.340670 randog-0.8.0/randog/factory/
+-rw-r--r--   0 runner    (1001) docker     (123)     1440 2023-07-23 11:18:10.000000 randog-0.8.0/randog/factory/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7746 2023-07-23 11:18:10.000000 randog-0.8.0/randog/factory/_base.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1635 2023-07-23 11:18:10.000000 randog-0.8.0/randog/factory/_bool.py
+-rw-r--r--   0 runner    (1001) docker     (123)      798 2023-07-23 11:18:10.000000 randog-0.8.0/randog/factory/_by_callable.py
+-rw-r--r--   0 runner    (1001) docker     (123)      822 2023-07-23 11:18:10.000000 randog-0.8.0/randog/factory/_by_iterator.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3369 2023-07-23 11:18:10.000000 randog-0.8.0/randog/factory/_choice.py
+-rw-r--r--   0 runner    (1001) docker     (123)      508 2023-07-23 11:18:10.000000 randog-0.8.0/randog/factory/_const.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2918 2023-07-23 11:18:10.000000 randog-0.8.0/randog/factory/_date.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4670 2023-07-23 11:18:10.000000 randog-0.8.0/randog/factory/_datetime.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3125 2023-07-23 11:18:10.000000 randog-0.8.0/randog/factory/_decimal.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3301 2023-07-23 11:18:10.000000 randog-0.8.0/randog/factory/_dict.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4124 2023-07-23 11:18:10.000000 randog-0.8.0/randog/factory/_float.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11444 2023-07-23 11:18:10.000000 randog-0.8.0/randog/factory/_from_example.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2616 2023-07-23 11:18:10.000000 randog-0.8.0/randog/factory/_from_pyfile.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1538 2023-07-23 11:18:10.000000 randog-0.8.0/randog/factory/_increment.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1655 2023-07-23 11:18:10.000000 randog-0.8.0/randog/factory/_int.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4357 2023-07-23 11:18:10.000000 randog-0.8.0/randog/factory/_list.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 11:18:20.340670 randog-0.8.0/randog/factory/_str/
+-rw-r--r--   0 runner    (1001) docker     (123)     3721 2023-07-23 11:18:10.000000 randog-0.8.0/randog/factory/_str/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      816 2023-07-23 11:18:10.000000 randog-0.8.0/randog/factory/_str/_regex.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4137 2023-07-23 11:18:10.000000 randog-0.8.0/randog/factory/_time.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5270 2023-07-23 11:18:10.000000 randog-0.8.0/randog/factory/_timedelta.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2912 2023-07-23 11:18:10.000000 randog-0.8.0/randog/factory/_union.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 11:18:20.340670 randog-0.8.0/randog/sqlalchemy/
+-rw-r--r--   0 runner    (1001) docker     (123)      157 2023-07-23 11:18:10.000000 randog-0.8.0/randog/sqlalchemy/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6873 2023-07-23 11:18:10.000000 randog-0.8.0/randog/sqlalchemy/_construct.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1586 2023-07-23 11:18:10.000000 randog-0.8.0/randog/sqlalchemy/_custom_func.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9580 2023-07-23 11:18:10.000000 randog-0.8.0/randog/timedelta_util.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 11:18:20.336670 randog-0.8.0/randog.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2101 2023-07-23 11:18:20.000000 randog-0.8.0/randog.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1515 2023-07-23 11:18:20.000000 randog-0.8.0/randog.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 11:18:20.000000 randog-0.8.0/randog.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        7 2023-07-23 11:18:20.000000 randog-0.8.0/randog.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 11:18:20.340670 randog-0.8.0/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1039 2023-07-23 11:18:10.000000 randog-0.8.0/setup.py
```

### Comparing `randog-0.7.0/LICENSE` & `randog-0.8.0/LICENSE`

 * *Files identical despite different names*

### Comparing `randog-0.7.0/PKG-INFO` & `randog-0.8.0/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,21 +1,21 @@
 Metadata-Version: 2.1
 Name: randog
-Version: 0.7.0
+Version: 0.8.0
 Summary: Generate data randomly
 Home-page: UNKNOWN
 Author: k-izumi
 Author-email: k.izumi.ysk@gmail.com
 Maintainer: k-izumi
 Maintainer-email: k.izumi.ysk@gmail.com
 License: MIT
 Project-URL: Bug Tracker, https://github.com/unaguna/random-obj-generator/issues
 Project-URL: Documentation, https://unaguna.github.io/random-obj-generator/
 Project-URL: Source Code, https://github.com/unaguna/random-obj-generator
-Description: **randog 0.7.0 — Randomly object generator**
+Description: **randog 0.8.0 — Randomly object generator**
         
         **randog** is a package which helps to generate data randomly.
         
         ## Install
         
         You can install from PyPI.
```

### Comparing `randog-0.7.0/README.md` & `randog-0.8.0/README.md`

 * *Files 0% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-**randog 0.7.0 — Randomly object generator**
+**randog 0.8.0 — Randomly object generator**
 
 **randog** is a package which helps to generate data randomly.
 
 ## Install
 
 You can install from PyPI.
```

### Comparing `randog-0.7.0/randog/__main__.py` & `randog-0.8.0/randog/__main__.py`

 * *Files 15% similar despite different names*

```diff
@@ -1,9 +1,10 @@
 import csv
 import json
+import random
 import sys
 import typing as t
 
 import randog.factory
 from .factory import FactoryDef
 from ._main import Args, Subcmd, get_subcmd_def
 
@@ -136,46 +137,73 @@
         return str
 
 
 def _output_to_csv(
     factory: randog.factory.Factory[t.Optional[t.Sequence[t.Sequence[t.Any]]]],
     line_num: int,
     fp: t.TextIO,
+    regenerate: float,
+    discard: float,
 ):
     csv_writer = csv.writer(fp, lineterminator="\n")
-    csv_writer.writerows(filter(lambda x: x is not None, factory.iter(line_num)))
+    csv_writer.writerows(
+        filter(
+            lambda x: x is not None,
+            factory.iter(
+                line_num,
+                regenerate=regenerate,
+                discard=discard,
+            ),
+        )
+    )
 
 
 def main():
     args = Args(sys.argv)
 
     with _open_output_fp_only(args) as fp_only:
         index = 0
         for factory in _build_factories(args):
             for r_index in range(args.repeat):
                 with _open_output_fp_numbered(args, index) as fp_numbered:
+                    index += 1
                     # args と index に応じて出力先 fp を決定する。
                     # args と index に応じて fp_numbered, fp_only の状態が異なるので、それを条件に使用する。
                     if not isinstance(fp_numbered, _DummyIO):
                         fp = fp_numbered
                     elif not isinstance(fp_only, _DummyIO):
                         fp = fp_only
                     else:
                         fp = sys.stdout
 
                     # 生成処理と出力処理
                     # CSV 出力の場合に生成の方法が異なるので、生成と出力をひとまとめにした。
                     if args.csv is not None:
-                        _output_to_csv(factory, args.csv, fp)
+                        _output_to_csv(
+                            factory,
+                            args.csv,
+                            fp,
+                            regenerate=args.regenerate,
+                            discard=args.discard,
+                        )
                     else:
                         if args.list is not None:
-                            generated = list(factory.iter(args.list))
+                            generated = list(
+                                factory.iter(
+                                    args.list,
+                                    regenerate=args.regenerate,
+                                    discard=args.discard,
+                                )
+                            )
                         else:
-                            generated = factory.next()
+                            while True:
+                                generated = factory.next()
+                                if random.random() >= args.regenerate:
+                                    break
+                            if random.random() < args.discard:
+                                continue
 
                         _output_generated(generated, fp, args=args)
 
-                index += 1
-
 
 if __name__ == "__main__":
     main()
```

### Comparing `randog-0.7.0/randog/_examples.py` & `randog-0.8.0/randog/_examples.py`

 * *Files identical despite different names*

### Comparing `randog-0.7.0/randog/_main/_main_args.py` & `randog-0.8.0/randog/_main/_main_args.py`

 * *Files 7% similar despite different names*

```diff
@@ -80,14 +80,28 @@
     def format(self) -> t.Optional[str]:
         if hasattr(self._args, "format"):
             return self._args.format
         else:
             return None
 
     @property
+    def regenerate(self) -> float:
+        if hasattr(self._args, "regenerate"):
+            return self._args.regenerate
+        else:
+            return 0.0
+
+    @property
+    def discard(self) -> float:
+        if hasattr(self._args, "discard"):
+            return self._args.discard
+        else:
+            return 0.0
+
+    @property
     def csv(self) -> t.Optional[int]:
         if hasattr(self._args, "csv"):
             return self._args.csv
         else:
             return None
 
     def output_path_for(self, number: int) -> t.Optional[str]:
```

### Comparing `randog-0.7.0/randog/_main/_subcmd_def/__init__.py` & `randog-0.8.0/randog/_main/_subcmd_def/__init__.py`

 * *Files identical despite different names*

### Comparing `randog-0.7.0/randog/_main/_subcmd_def/_base.py` & `randog-0.8.0/randog/_main/_subcmd_def/_base.py`

 * *Files identical despite different names*

### Comparing `randog-0.7.0/randog/_main/_subcmd_def/_bool.py` & `randog-0.8.0/randog/_main/_subcmd_def/_bool.py`

 * *Files identical despite different names*

### Comparing `randog-0.7.0/randog/_main/_subcmd_def/_byfile.py` & `randog-0.8.0/randog/_main/_subcmd_def/_datetime.py`

 * *Files 20% similar despite different names*

```diff
@@ -1,53 +1,76 @@
 import argparse
 import typing as t
 
+import randog.factory
+from ..._utils.type import datetime
 from .. import Args, Subcmd
 from ._base import SubcmdDef, add_common_arguments
-from ..._utils.type import positive_int
 
 
-class SubcmdDefByfile(SubcmdDef):
+class SubcmdDefDatetime(SubcmdDef):
     def cmd(self) -> Subcmd:
-        return Subcmd.Byfile
+        return Subcmd.Datetime
 
     def add_parser(self, subparsers) -> argparse.ArgumentParser:
-        byfile_parser = subparsers.add_parser(
-            Subcmd.Byfile.value,
-            usage="python -m randog byfile FACTORY_PATH [FACTORY_PATH ...] [--csv ROW_NUM] [common-options]",
-            description="It generates values according to factory definition files.",
+        datetime_parser = subparsers.add_parser(
+            Subcmd.Datetime.value,
+            usage="python -m randog datetime [MINIMUM MAXIMUM] [--iso | --fmt FORMAT] [common-options]",
+            description="It generates values of type datetime.datetime.",
             add_help=False,
         )
-        byfile_args_group = byfile_parser.add_argument_group("arguments")
-        byfile_args_group.add_argument(
-            "factories",
-            nargs="+",
-            metavar="FACTORY_PATH",
-            help="path of factory definition files",
+        datetime_args_group = datetime_parser.add_argument_group("arguments")
+        datetime_args_group.add_argument(
+            "minimum",
+            type=datetime,
+            nargs="?",
+            metavar="MINIMUM",
+            help="the minimum value with the ISO-8601 format. "
+            "If not specified, the behavior is left to the specification of randog.factory.randdatetime.",
         )
-        byfile_args_group.add_argument(
-            "--csv",
-            metavar="ROW_NUM",
-            type=positive_int,
-            help="if specified, it outputs generated ROW_NUM objects as CSV. "
-            "When using this option, it is recommended to use a factory that generates dictionaries and "
-            "to define CSV_COLUMNS in the definition file to specify the fields of the CSV.",
+        datetime_args_group.add_argument(
+            "maximum",
+            type=datetime,
+            nargs="?",
+            metavar="MAXIMUM",
+            help="the maximum value with the ISO-8601 format. "
+            "If not specified, the behavior is left to the specification of randog.factory.randdatetime.",
         )
-        add_common_arguments(byfile_parser)
+        group_date_fmt = datetime_args_group.add_mutually_exclusive_group()
+        group_date_fmt.add_argument(
+            "--iso",
+            action="store_true",
+            help="if specified, it outputs generated object with ISO-8601 format",
+        )
+        group_date_fmt.add_argument(
+            "--fmt",
+            dest="format",
+            metavar="FORMAT",
+            help="if specified, it outputs generated object with the specified format, "
+            "such as '%%Y/%%m/%%d %%H:%%M:%%S.%%f'",
+        )
+        add_common_arguments(datetime_parser)
 
-        return byfile_parser
+        return datetime_parser
 
     def validate_parser(self, args: Args, subparser: argparse.ArgumentParser):
-        if args.output_fmt == "repr" and args.csv is not None:
-            subparser.error("argument --csv: not allowed with argument --repr")
-        elif args.output_fmt == "json" and args.csv is not None:
-            subparser.error("argument --csv: not allowed with argument --json")
-        elif args.list is not None and args.csv is not None:
-            subparser.error("argument --csv: not allowed with argument --list/-L")
+        if args.sub_cmd != Subcmd.Datetime:
+            return
+
+        iargs, kwargs = self.build_args(args)
+        minimum, maximum = iargs
+
+        if minimum is not None and maximum is not None and minimum > maximum:
+            subparser.error("arguments must satisfy MINIMUM <= MAXIMUM")
+
+        if args.output_fmt == "repr" and args.iso:
+            subparser.error("argument --iso: not allowed with argument --repr")
+        elif args.output_fmt == "repr" and args.format:
+            subparser.error("argument --fmt: not allowed with argument --repr")
 
     def build_args(
         self, args: Args
     ) -> t.Tuple[t.Sequence[t.Any], t.Mapping[str, t.Any]]:
-        pass
+        return (args.get("minimum"), args.get("maximum")), {}
 
     def get_factory_constructor(self) -> t.Callable:
-        pass
+        return randog.factory.randdatetime
```

### Comparing `randog-0.7.0/randog/_main/_subcmd_def/_date.py` & `randog-0.8.0/randog/_main/_subcmd_def/_date.py`

 * *Files identical despite different names*

### Comparing `randog-0.7.0/randog/_main/_subcmd_def/_datetime.py` & `randog-0.8.0/randog/_main/_subcmd_def/_float.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,76 +1,92 @@
 import argparse
 import typing as t
 
 import randog.factory
-from ..._utils.type import datetime
+from ..._utils.type import probability
 from .. import Args, Subcmd
 from ._base import SubcmdDef, add_common_arguments
 
 
-class SubcmdDefDatetime(SubcmdDef):
+class SubcmdDefFloat(SubcmdDef):
     def cmd(self) -> Subcmd:
-        return Subcmd.Datetime
+        return Subcmd.Float
 
     def add_parser(self, subparsers) -> argparse.ArgumentParser:
-        datetime_parser = subparsers.add_parser(
-            Subcmd.Datetime.value,
-            usage="python -m randog datetime [MINIMUM MAXIMUM] [--iso | --fmt FORMAT] [common-options]",
-            description="It generates values of type datetime.datetime.",
+        float_parser = subparsers.add_parser(
+            Subcmd.Float.value,
+            usage="python -m randog float [MINIMUM MAXIMUM] [--p-inf PROB_P_INF] [--n-inf PROB_N_INF] [--nan PROB_NAN] "
+            "[common-options]",
+            description="It generates values of type float.",
             add_help=False,
         )
-        datetime_args_group = datetime_parser.add_argument_group("arguments")
-        datetime_args_group.add_argument(
+        float_args_group = float_parser.add_argument_group("arguments")
+        float_args_group.add_argument(
             "minimum",
-            type=datetime,
+            type=float,
             nargs="?",
             metavar="MINIMUM",
-            help="the minimum value with the ISO-8601 format. "
-            "If not specified, the behavior is left to the specification of randog.factory.randdatetime.",
+            help="the minimum value. "
+            "If not specified, the behavior is left to the specification of randog.factory.randfloat.",
         )
-        datetime_args_group.add_argument(
+        float_args_group.add_argument(
             "maximum",
-            type=datetime,
+            type=float,
             nargs="?",
             metavar="MAXIMUM",
-            help="the maximum value with the ISO-8601 format. "
-            "If not specified, the behavior is left to the specification of randog.factory.randdatetime.",
+            help="the maximum value. "
+            "If not specified, the behavior is left to the specification of randog.factory.randfloat.",
         )
-        group_date_fmt = datetime_args_group.add_mutually_exclusive_group()
-        group_date_fmt.add_argument(
-            "--iso",
-            action="store_true",
-            help="if specified, it outputs generated object with ISO-8601 format",
-        )
-        group_date_fmt.add_argument(
-            "--fmt",
-            dest="format",
-            metavar="FORMAT",
-            help="if specified, it outputs generated object with the specified format, "
-            "such as '%%Y/%%m/%%d %%H:%%M:%%S.%%f'",
+        float_args_group.add_argument(
+            "--p-inf",
+            type=probability,
+            default=0.0,
+            metavar="PROB_P_INF",
+            help="the probability of positive infinity; default=0.0",
         )
-        add_common_arguments(datetime_parser)
+        float_args_group.add_argument(
+            "--n-inf",
+            type=probability,
+            default=0.0,
+            metavar="PROB_N_INF",
+            help="the probability of negative infinity; default=0.0",
+        )
+        float_args_group.add_argument(
+            "--nan",
+            type=probability,
+            default=0.0,
+            metavar="PROB_NAN",
+            help="the probability of NaN; default=0.0",
+        )
+        add_common_arguments(float_parser)
 
-        return datetime_parser
+        return float_parser
 
     def validate_parser(self, args: Args, subparser: argparse.ArgumentParser):
-        if args.sub_cmd != Subcmd.Datetime:
+        if args.sub_cmd != Subcmd.Float:
             return
 
         iargs, kwargs = self.build_args(args)
         minimum, maximum = iargs
+        nan = kwargs["nan"]
+        p_inf = kwargs["p_inf"]
+        n_inf = kwargs["n_inf"]
 
         if minimum is not None and maximum is not None and minimum > maximum:
             subparser.error("arguments must satisfy MINIMUM <= MAXIMUM")
 
-        if args.output_fmt == "repr" and args.iso:
-            subparser.error("argument --iso: not allowed with argument --repr")
-        elif args.output_fmt == "repr" and args.format:
-            subparser.error("argument --fmt: not allowed with argument --repr")
+        if nan + p_inf + n_inf > 1.0:
+            subparser.error(
+                "arguments must satisfy that PROB_P_INF + PROB_N_INF + PROB_NAN <= 1.0"
+            )
 
     def build_args(
         self, args: Args
     ) -> t.Tuple[t.Sequence[t.Any], t.Mapping[str, t.Any]]:
-        return (args.get("minimum"), args.get("maximum")), {}
+        return (args.get("minimum"), args.get("maximum")), {
+            "p_inf": args.get("p_inf"),
+            "n_inf": args.get("n_inf"),
+            "nan": args.get("nan"),
+        }
 
     def get_factory_constructor(self) -> t.Callable:
-        return randog.factory.randdatetime
+        return randog.factory.randfloat
```

### Comparing `randog-0.7.0/randog/_main/_subcmd_def/_decimal.py` & `randog-0.8.0/randog/_main/_subcmd_def/_decimal.py`

 * *Files identical despite different names*

### Comparing `randog-0.7.0/randog/_main/_subcmd_def/_int.py` & `randog-0.8.0/randog/_main/_subcmd_def/_int.py`

 * *Files identical despite different names*

### Comparing `randog-0.7.0/randog/_main/_subcmd_def/_str.py` & `randog-0.8.0/randog/_main/_subcmd_def/_str.py`

 * *Files 24% similar despite different names*

```diff
@@ -10,15 +10,15 @@
 class SubcmdDefString(SubcmdDef):
     def cmd(self) -> Subcmd:
         return Subcmd.String
 
     def add_parser(self, subparsers) -> argparse.ArgumentParser:
         str_parser = subparsers.add_parser(
             Subcmd.String.value,
-            usage="python -m randog str [--length LENGTH] [--charset CHARSET] [common-options]",
+            usage="python -m randog str [--length LENGTH] [--charset CHARSET] [--regex REGEX] [common-options]",
             description="It generates values of type str.",
             add_help=False,
         )
         str_args_group = str_parser.add_argument_group("arguments")
         str_args_group.add_argument(
             "--length",
             type=non_negative_int_range,
@@ -30,25 +30,48 @@
         str_args_group.add_argument(
             "--charset",
             type=str,
             default=None,
             metavar="CHARSET",
             help="the characters which contained by generated strings",
         )
+        str_args_group.add_argument(
+            "--regex",
+            type=str,
+            default=None,
+            metavar="REGEX",
+            help="the regular expression for generated string. It cannot be used with `--length` or `--charset`.",
+        )
         add_common_arguments(str_parser)
 
         return str_parser
 
     def validate_parser(self, args: Args, subparser: argparse.ArgumentParser):
-        pass
+        iargs, kwargs = self.build_args(args)
+        regex = kwargs["regex"]
+        length = kwargs.get("length")
+        charset = kwargs["charset"]
+
+        if regex is not None:
+            try:
+                import rstr
+            except ImportError:
+                subparser.error(
+                    "argument --regex: package 'rstr' is required to use --regex"
+                )
+
+        if regex is not None and length is not None:
+            subparser.error("argument --regex: not allowed with argument --length")
+        if regex is not None and charset is not None:
+            subparser.error("argument --regex: not allowed with argument --charset")
 
     def build_args(
         self, args: Args
     ) -> t.Tuple[t.Sequence[t.Any], t.Mapping[str, t.Any]]:
-        kwargs = {"charset": args.get("charset")}
+        kwargs = {"charset": args.get("charset"), "regex": args.get("regex")}
         length = args.get("length")
         if length is not None:
             if length[0] == length[1]:
                 kwargs["length"] = length[0]
             else:
                 kwargs["length"] = randog.factory.randint(*length)
```

### Comparing `randog-0.7.0/randog/_main/_subcmd_def/_time.py` & `randog-0.8.0/randog/_main/_subcmd_def/_time.py`

 * *Files identical despite different names*

### Comparing `randog-0.7.0/randog/_main/_subcmd_def/_timedelta.py` & `randog-0.8.0/randog/_main/_subcmd_def/_timedelta.py`

 * *Files identical despite different names*

### Comparing `randog-0.7.0/randog/_utils/type.py` & `randog-0.8.0/randog/_utils/type.py`

 * *Files identical despite different names*

### Comparing `randog-0.7.0/randog/factory/__init__.py` & `randog-0.8.0/randog/factory/__init__.py`

 * *Files 8% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-from ._base import Factory
+from ._base import Factory, REGENERATE_PROB_MAX
 from ._choice import ChoiceRandomFactory, randchoice, randenum
 from ._const import const
 from ._bool import BoolRandomFactory, randbool
 from ._int import IntRandomFactory, randint
 from ._float import FloatRandomFactory, randfloat
 from ._decimal import DecimalRandomFactory, randdecimal
 from ._str import StrRandomFactory, randstr
@@ -40,8 +40,9 @@
     "randdict",
     "by_callable",
     "by_iterator",
     "increment",
     "union",
     "DictItem",
     "FactoryDef",
+    "REGENERATE_PROB_MAX",
 ]
```

### Comparing `randog-0.7.0/randog/factory/_bool.py` & `randog-0.8.0/randog/factory/_bool.py`

 * *Files identical despite different names*

### Comparing `randog-0.7.0/randog/factory/_by_callable.py` & `randog-0.8.0/randog/factory/_by_callable.py`

 * *Files identical despite different names*

### Comparing `randog-0.7.0/randog/factory/_by_iterator.py` & `randog-0.8.0/randog/factory/_by_iterator.py`

 * *Files identical despite different names*

### Comparing `randog-0.7.0/randog/factory/_choice.py` & `randog-0.8.0/randog/factory/_choice.py`

 * *Files identical despite different names*

### Comparing `randog-0.7.0/randog/factory/_date.py` & `randog-0.8.0/randog/factory/_date.py`

 * *Files identical despite different names*

### Comparing `randog-0.7.0/randog/factory/_datetime.py` & `randog-0.8.0/randog/factory/_datetime.py`

 * *Files identical despite different names*

### Comparing `randog-0.7.0/randog/factory/_decimal.py` & `randog-0.8.0/randog/factory/_decimal.py`

 * *Files identical despite different names*

### Comparing `randog-0.7.0/randog/factory/_dict.py` & `randog-0.8.0/randog/factory/_dict.py`

 * *Files identical despite different names*

### Comparing `randog-0.7.0/randog/factory/_float.py` & `randog-0.8.0/randog/factory/_float.py`

 * *Files identical despite different names*

### Comparing `randog-0.7.0/randog/factory/_from_example.py` & `randog-0.8.0/randog/factory/_from_example.py`

 * *Files identical despite different names*

### Comparing `randog-0.7.0/randog/factory/_from_pyfile.py` & `randog-0.8.0/randog/factory/_from_pyfile.py`

 * *Files identical despite different names*

### Comparing `randog-0.7.0/randog/factory/_increment.py` & `randog-0.8.0/randog/factory/_increment.py`

 * *Files identical despite different names*

### Comparing `randog-0.7.0/randog/factory/_int.py` & `randog-0.8.0/randog/factory/_int.py`

 * *Files identical despite different names*

### Comparing `randog-0.7.0/randog/factory/_list.py` & `randog-0.8.0/randog/factory/_list.py`

 * *Files identical despite different names*

### Comparing `randog-0.7.0/randog/factory/_str.py` & `randog-0.8.0/randog/factory/_str/__init__.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,52 +1,91 @@
 import string
 import typing as t
 from random import Random
 
-from ._base import Factory
-from .._utils.nullsafe import dfor
-from ..exceptions import FactoryConstructionError
+from .._base import Factory
+from ..._utils.nullsafe import dfor
+from ...exceptions import FactoryConstructionError
 
 
+@t.overload
 def randstr(
     *,
-    length: t.Union[int, Factory[int]] = 8,
+    length: t.Union[int, Factory[int], None] = None,
     charset: t.Optional[str] = None,
+    regex: None = None,
+    rnd: t.Optional[Random] = None,
+) -> Factory[str]:
+    pass
+
+
+@t.overload
+def randstr(
+    *,
+    length: None = None,
+    charset: None = None,
+    regex: t.Union[str, t.Pattern],
+    rnd: t.Optional[Random] = None,
+) -> Factory[str]:
+    pass
+
+
+def randstr(
+    *,
+    length: t.Union[int, Factory[int], None] = None,
+    charset: t.Optional[str] = None,
+    regex: t.Optional[str] = None,
     rnd: t.Optional[Random] = None,
 ) -> Factory[str]:
     """Return a factory generating random str values.
 
     Parameters
     ----------
     length : int|Factory[int], default=8
         length of generated string
     charset : str, optional
         characters to be used
+    regex : str, optional
+        regular expression for generated string. It cannot be used with `length` or `charset`.
     rnd : Random, optional
         random number generator to be used
 
     Raises
     ------
     FactoryConstructionError
         When the specified generating conditions are inconsistent.
     """
-    return StrRandomFactory(length=length, charset=charset, rnd=rnd)
+    if regex is not None and (length is not None or charset is not None):
+        raise FactoryConstructionError(
+            "cannot specify argument 'regex' for randstr() with 'length' or 'charset'"
+        )
+
+    if regex is not None:
+        try:
+            from ._regex import StrRegexRandomFactory
+        except ImportError:
+            raise FactoryConstructionError(
+                "package 'rstr' must be installed to specify 'regex' to randstr()"
+            )
+        return StrRegexRandomFactory(regex=regex, rnd=rnd)
+    else:
+        return StrRandomFactory(length=length, charset=charset, rnd=rnd)
 
 
 class StrRandomFactory(Factory[str]):
     """factory generating random int values"""
 
     _random: Random
     _length: t.Union[int, Factory[int]]
     _charset: str
 
     def __init__(
         self,
         *,
-        length: t.Union[int, Factory[int]] = 8,
+        length: t.Union[int, Factory[int], None] = None,
         charset: t.Optional[str] = None,
         rnd: t.Optional[Random] = None,
     ):
         """Return a factory generating random str values.
 
         Parameters
         ----------
@@ -59,15 +98,15 @@
 
         Raises
         ------
         FactoryConstructionError
             When the specified generating conditions are inconsistent.
         """
         self._random = dfor(rnd, Random())
-        self._length = length
+        self._length = dfor(length, 8)
         self._charset = dfor(charset, string.ascii_letters + string.digits)
 
         if isinstance(self._length, Factory) and len(self._charset) == 0:
             raise FactoryConstructionError(
                 "the charset for randstr() must not be empty if length is at random"
             )
         if (
```

### Comparing `randog-0.7.0/randog/factory/_time.py` & `randog-0.8.0/randog/factory/_time.py`

 * *Files identical despite different names*

### Comparing `randog-0.7.0/randog/factory/_timedelta.py` & `randog-0.8.0/randog/factory/_timedelta.py`

 * *Files identical despite different names*

### Comparing `randog-0.7.0/randog/factory/_union.py` & `randog-0.8.0/randog/factory/_union.py`

 * *Files identical despite different names*

### Comparing `randog-0.7.0/randog/sqlalchemy/_construct.py` & `randog-0.8.0/randog/sqlalchemy/_construct.py`

 * *Files identical despite different names*

### Comparing `randog-0.7.0/randog/sqlalchemy/_custom_func.py` & `randog-0.8.0/randog/sqlalchemy/_custom_func.py`

 * *Files identical despite different names*

### Comparing `randog-0.7.0/randog/timedelta_util.py` & `randog-0.8.0/randog/timedelta_util.py`

 * *Files identical despite different names*

### Comparing `randog-0.7.0/randog.egg-info/PKG-INFO` & `randog-0.8.0/randog.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,21 +1,21 @@
 Metadata-Version: 2.1
 Name: randog
-Version: 0.7.0
+Version: 0.8.0
 Summary: Generate data randomly
 Home-page: UNKNOWN
 Author: k-izumi
 Author-email: k.izumi.ysk@gmail.com
 Maintainer: k-izumi
 Maintainer-email: k.izumi.ysk@gmail.com
 License: MIT
 Project-URL: Bug Tracker, https://github.com/unaguna/random-obj-generator/issues
 Project-URL: Documentation, https://unaguna.github.io/random-obj-generator/
 Project-URL: Source Code, https://github.com/unaguna/random-obj-generator
-Description: **randog 0.7.0 — Randomly object generator**
+Description: **randog 0.8.0 — Randomly object generator**
         
         **randog** is a package which helps to generate data randomly.
         
         ## Install
         
         You can install from PyPI.
```

### Comparing `randog-0.7.0/randog.egg-info/SOURCES.txt` & `randog-0.8.0/randog.egg-info/SOURCES.txt`

 * *Files 4% similar despite different names*

```diff
@@ -41,14 +41,15 @@
 randog/factory/_dict.py
 randog/factory/_float.py
 randog/factory/_from_example.py
 randog/factory/_from_pyfile.py
 randog/factory/_increment.py
 randog/factory/_int.py
 randog/factory/_list.py
-randog/factory/_str.py
 randog/factory/_time.py
 randog/factory/_timedelta.py
 randog/factory/_union.py
+randog/factory/_str/__init__.py
+randog/factory/_str/_regex.py
 randog/sqlalchemy/__init__.py
 randog/sqlalchemy/_construct.py
 randog/sqlalchemy/_custom_func.py
```

### Comparing `randog-0.7.0/setup.py` & `randog-0.8.0/setup.py`

 * *Files identical despite different names*

