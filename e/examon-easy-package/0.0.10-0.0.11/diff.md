# Comparing `tmp/examon_easy_package-0.0.10.tar.gz` & `tmp/examon_easy_package-0.0.11.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "examon_easy_package-0.0.10.tar", max compression
+gzip compressed data, was "examon_easy_package-0.0.11.tar", max compression
```

## Comparing `examon_easy_package-0.0.10.tar` & `examon_easy_package-0.0.11.tar`

### file list

```diff
@@ -1,4 +1,4 @@
--rw-r--r--   0        0        0       12 2023-07-16 20:17:34.381320 examon_easy_package-0.0.10/examon_package_template/__init__.py
--rw-r--r--   0        0        0      184 2023-07-23 15:37:42.553073 examon_easy_package-0.0.10/examon_package_template/questions.py
--rw-r--r--   0        0        0      334 2023-07-23 15:43:11.258072 examon_easy_package-0.0.10/pyproject.toml
--rw-r--r--   0        0        0      396 1970-01-01 00:00:00.000000 examon_easy_package-0.0.10/PKG-INFO
+-rw-r--r--   0        0        0       12 2023-07-16 20:17:34.381320 examon_easy_package-0.0.11/examon_easy_package/__init__.py
+-rw-r--r--   0        0        0      184 2023-07-23 15:37:42.553073 examon_easy_package-0.0.11/examon_easy_package/questions.py
+-rw-r--r--   0        0        0      330 2023-07-23 16:42:04.124431 examon_easy_package-0.0.11/pyproject.toml
+-rw-r--r--   0        0        0      396 1970-01-01 00:00:00.000000 examon_easy_package-0.0.11/PKG-INFO
```

