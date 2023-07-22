# Comparing `tmp/logger_extras-0.0.1rc1.tar.gz` & `tmp/logger_extras-0.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "logger_extras-0.0.1rc1.tar", last modified: Thu Jul 20 21:32:42 2023, max compression
+gzip compressed data, was "logger_extras-0.1.0.tar", last modified: Sat Jul 22 16:28:27 2023, max compression
```

## Comparing `logger_extras-0.0.1rc1.tar` & `logger_extras-0.1.0.tar`

### file list

```diff
@@ -1,22 +1,27 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-20 21:32:42.734411 logger_extras-0.0.1rc1/
--rw-r--r--   0 runner    (1001) docker     (123)      310 2023-07-20 21:32:27.000000 logger_extras-0.0.1rc1/.flake8
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-20 21:32:42.734411 logger_extras-0.0.1rc1/.github/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-20 21:32:42.734411 logger_extras-0.0.1rc1/.github/workflows/
--rw-r--r--   0 runner    (1001) docker     (123)     1888 2023-07-20 21:32:27.000000 logger_extras-0.0.1rc1/.github/workflows/test_build.yml
--rw-r--r--   0 runner    (1001) docker     (123)     1250 2023-07-20 21:32:27.000000 logger_extras-0.0.1rc1/.gitignore
--rw-r--r--   0 runner    (1001) docker     (123)     1068 2023-07-20 21:32:27.000000 logger_extras-0.0.1rc1/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      494 2023-07-20 21:32:27.000000 logger_extras-0.0.1rc1/Makefile
--rw-r--r--   0 runner    (1001) docker     (123)     3182 2023-07-20 21:32:42.734411 logger_extras-0.0.1rc1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1362 2023-07-20 21:32:27.000000 logger_extras-0.0.1rc1/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-20 21:32:42.734411 logger_extras-0.0.1rc1/logger_extras/
--rw-r--r--   0 runner    (1001) docker     (123)      104 2023-07-20 21:32:27.000000 logger_extras-0.0.1rc1/logger_extras/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)      163 2023-07-20 21:32:42.000000 logger_extras-0.0.1rc1/logger_extras/_version.py
--rw-r--r--   0 runner    (1001) docker     (123)       85 2023-07-20 21:32:27.000000 logger_extras-0.0.1rc1/logger_extras/py.typed
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-20 21:32:42.734411 logger_extras-0.0.1rc1/logger_extras.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     3182 2023-07-20 21:32:42.000000 logger_extras-0.0.1rc1/logger_extras.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      352 2023-07-20 21:32:42.000000 logger_extras-0.0.1rc1/logger_extras.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-20 21:32:42.000000 logger_extras-0.0.1rc1/logger_extras.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       91 2023-07-20 21:32:42.000000 logger_extras-0.0.1rc1/logger_extras.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       14 2023-07-20 21:32:42.000000 logger_extras-0.0.1rc1/logger_extras.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)     1534 2023-07-20 21:32:27.000000 logger_extras-0.0.1rc1/pyproject.toml
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-20 21:32:42.734411 logger_extras-0.0.1rc1/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 16:28:27.164265 logger_extras-0.1.0/
+-rw-r--r--   0 runner    (1001) docker     (123)      310 2023-07-22 16:28:12.000000 logger_extras-0.1.0/.flake8
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 16:28:27.160265 logger_extras-0.1.0/.github/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 16:28:27.160265 logger_extras-0.1.0/.github/workflows/
+-rw-r--r--   0 runner    (1001) docker     (123)     1888 2023-07-22 16:28:12.000000 logger_extras-0.1.0/.github/workflows/test_build.yml
+-rw-r--r--   0 runner    (1001) docker     (123)     1250 2023-07-22 16:28:12.000000 logger_extras-0.1.0/.gitignore
+-rw-r--r--   0 runner    (1001) docker     (123)     1068 2023-07-22 16:28:12.000000 logger_extras-0.1.0/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      494 2023-07-22 16:28:12.000000 logger_extras-0.1.0/Makefile
+-rw-r--r--   0 runner    (1001) docker     (123)     5207 2023-07-22 16:28:27.164265 logger_extras-0.1.0/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     3390 2023-07-22 16:28:12.000000 logger_extras-0.1.0/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 16:28:27.160265 logger_extras-0.1.0/logger_extras/
+-rw-r--r--   0 runner    (1001) docker     (123)      333 2023-07-22 16:28:12.000000 logger_extras-0.1.0/logger_extras/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      160 2023-07-22 16:28:27.000000 logger_extras-0.1.0/logger_extras/_version.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1741 2023-07-22 16:28:12.000000 logger_extras-0.1.0/logger_extras/filters.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2094 2023-07-22 16:28:12.000000 logger_extras-0.1.0/logger_extras/formatters.py
+-rw-r--r--   0 runner    (1001) docker     (123)       85 2023-07-22 16:28:12.000000 logger_extras-0.1.0/logger_extras/py.typed
+-rw-r--r--   0 runner    (1001) docker     (123)     1683 2023-07-22 16:28:12.000000 logger_extras-0.1.0/logger_extras/utils.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 16:28:27.164265 logger_extras-0.1.0/logger_extras.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     5207 2023-07-22 16:28:27.000000 logger_extras-0.1.0/logger_extras.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      448 2023-07-22 16:28:27.000000 logger_extras-0.1.0/logger_extras.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-22 16:28:27.000000 logger_extras-0.1.0/logger_extras.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      140 2023-07-22 16:28:27.000000 logger_extras-0.1.0/logger_extras.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       14 2023-07-22 16:28:27.000000 logger_extras-0.1.0/logger_extras.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)     1582 2023-07-22 16:28:12.000000 logger_extras-0.1.0/pyproject.toml
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-22 16:28:27.164265 logger_extras-0.1.0/setup.cfg
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 16:28:27.164265 logger_extras-0.1.0/tests/
+-rw-r--r--   0 runner    (1001) docker     (123)     5189 2023-07-22 16:28:12.000000 logger_extras-0.1.0/tests/test_tools.py
```

### Comparing `logger_extras-0.0.1rc1/.github/workflows/test_build.yml` & `logger_extras-0.1.0/.github/workflows/test_build.yml`

 * *Files identical despite different names*

### Comparing `logger_extras-0.0.1rc1/.gitignore` & `logger_extras-0.1.0/.gitignore`

 * *Files identical despite different names*

### Comparing `logger_extras-0.0.1rc1/LICENSE` & `logger_extras-0.1.0/LICENSE`

 * *Files identical despite different names*

### Comparing `logger_extras-0.0.1rc1/pyproject.toml` & `logger_extras-0.1.0/pyproject.toml`

 * *Files 6% similar despite different names*

```diff
@@ -61,10 +61,11 @@
 dev = [
     "flake8",
     "isort",
     "mypy",
     "build",
     "pytest",
     "pytest-cov",
+    "typing-extensions; python_version<'3.10'",
     "types-paho-mqtt",
 ]
 mqtt = ["paho-mqtt >=1.6,<2"]
```

