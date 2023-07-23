# Comparing `tmp/temp_api-0.1.0.tar.gz` & `tmp/temp_api-0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "temp_api-0.1.0.tar", max compression
+gzip compressed data, was "temp_api-0.1.1.tar", max compression
```

## Comparing `temp_api-0.1.0.tar` & `temp_api-0.1.1.tar`

### file list

```diff
@@ -1,6 +1,6 @@
--rw-r--r--   0        0        0       11 2023-07-23 17:08:16.357430 temp_api-0.1.0/README.md
--rw-r--r--   0        0        0      379 2023-07-23 17:08:05.111100 temp_api-0.1.0/pyproject.toml
--rw-r--r--   0        0        0       22 2023-07-23 16:30:51.992714 temp_api-0.1.0/temp_api/__init__.py
--rw-r--r--   0        0        0        0 2023-07-23 16:31:04.296478 temp_api-0.1.0/temp_api/__main__.py
--rw-r--r--   0        0        0     1085 2023-07-23 17:07:28.137776 temp_api-0.1.0/temp_api/main.py
--rw-r--r--   0        0        0      338 1970-01-01 00:00:00.000000 temp_api-0.1.0/PKG-INFO
+-rw-r--r--   0        0        0       11 2023-07-23 17:08:16.357430 temp_api-0.1.1/README.md
+-rw-r--r--   0        0        0      378 2023-07-23 20:53:32.147742 temp_api-0.1.1/pyproject.toml
+-rw-r--r--   0        0        0       22 2023-07-23 16:30:51.992714 temp_api-0.1.1/temp_api/__init__.py
+-rw-r--r--   0        0        0        0 2023-07-23 16:31:04.296478 temp_api-0.1.1/temp_api/__main__.py
+-rw-r--r--   0        0        0     1085 2023-07-23 17:07:28.137776 temp_api-0.1.1/temp_api/main.py
+-rw-r--r--   0        0        0      538 1970-01-01 00:00:00.000000 temp_api-0.1.1/PKG-INFO
```

### Comparing `temp_api-0.1.0/temp_api/main.py` & `temp_api-0.1.1/temp_api/main.py`

 * *Files identical despite different names*

