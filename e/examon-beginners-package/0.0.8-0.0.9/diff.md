# Comparing `tmp/examon_beginners_package-0.0.8.tar.gz` & `tmp/examon_beginners_package-0.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "examon_beginners_package-0.0.8.tar", max compression
+gzip compressed data, was "examon_beginners_package-0.0.9.tar", max compression
```

## Comparing `examon_beginners_package-0.0.8.tar` & `examon_beginners_package-0.0.9.tar`

### file list

```diff
@@ -1,4 +1,4 @@
--rw-r--r--   0        0        0       24 2023-07-16 20:33:56.622876 examon_beginners_package-0.0.8/examon_beginners_package/__init__.py
--rw-r--r--   0        0        0     1573 2023-07-18 20:43:28.888259 examon_beginners_package-0.0.8/examon_beginners_package/beginners.py
--rw-r--r--   0        0        0      338 2023-07-18 20:43:58.512136 examon_beginners_package-0.0.8/pyproject.toml
--rw-r--r--   0        0        0      399 1970-01-01 00:00:00.000000 examon_beginners_package-0.0.8/PKG-INFO
+-rw-r--r--   0        0        0       24 2023-07-16 20:33:56.622876 examon_beginners_package-0.0.9/examon_beginners_package/__init__.py
+-rw-r--r--   0        0        0     1573 2023-07-18 20:43:28.888259 examon_beginners_package-0.0.9/examon_beginners_package/beginners.py
+-rw-r--r--   0        0        0      338 2023-07-21 22:00:34.115561 examon_beginners_package-0.0.9/pyproject.toml
+-rw-r--r--   0        0        0      399 1970-01-01 00:00:00.000000 examon_beginners_package-0.0.9/PKG-INFO
```

### Comparing `examon_beginners_package-0.0.8/examon_beginners_package/beginners.py` & `examon_beginners_package-0.0.9/examon_beginners_package/beginners.py`

 * *Files identical despite different names*

