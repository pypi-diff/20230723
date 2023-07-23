# Comparing `tmp/atro_args-0.1.0.tar.gz` & `tmp/atro_args-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "atro_args-0.1.0.tar", max compression
+gzip compressed data, was "atro_args-0.2.0.tar", max compression
```

## Comparing `atro_args-0.1.0.tar` & `atro_args-0.2.0.tar`

### file list

```diff
@@ -1,4 +1,7 @@
--rw-r--r--   0        0        0        0 2023-06-17 12:33:58.233092 atro_args-0.1.0/README.md
--rw-r--r--   0        0        0      276 2023-07-16 21:47:16.150095 atro_args-0.1.0/atro_args/__init__.py
--rw-r--r--   0        0        0      329 2023-07-17 21:43:35.030720 atro_args-0.1.0/pyproject.toml
--rw-r--r--   0        0        0      341 1970-01-01 00:00:00.000000 atro_args-0.1.0/PKG-INFO
+-rw-r--r--   0        0        0        0 2023-06-17 12:33:58.233092 atro_args-0.2.0/README.md
+-rw-r--r--   0        0        0       89 2023-07-23 14:15:04.213219 atro_args-0.2.0/atro_args/__init__.py
+-rw-r--r--   0        0        0      267 2023-07-23 14:11:53.169286 atro_args-0.2.0/atro_args/arg.py
+-rw-r--r--   0        0        0      147 2023-07-23 14:11:53.169286 atro_args-0.2.0/atro_args/arg_type.py
+-rw-r--r--   0        0        0     5670 2023-07-23 14:39:31.620100 atro_args-0.2.0/atro_args/input_args.py
+-rw-r--r--   0        0        0      407 2023-07-23 14:11:53.895968 atro_args-0.2.0/pyproject.toml
+-rw-r--r--   0        0        0      349 1970-01-01 00:00:00.000000 atro_args-0.2.0/PKG-INFO
```

