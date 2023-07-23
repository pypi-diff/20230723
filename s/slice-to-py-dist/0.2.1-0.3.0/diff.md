# Comparing `tmp/slice_to_py_dist-0.2.1.tar.gz` & `tmp/slice_to_py_dist-0.3.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "slice_to_py_dist-0.2.1.tar", max compression
+gzip compressed data, was "slice_to_py_dist-0.3.0.tar", max compression
```

## Comparing `slice_to_py_dist-0.2.1.tar` & `slice_to_py_dist-0.3.0.tar`

### file list

```diff
@@ -1,9 +1,9 @@
--rw-r--r--   0        0        0     6376 2023-07-12 09:02:11.606973 slice_to_py_dist-0.2.1/README.md
--rw-r--r--   0        0        0     1318 2023-07-21 16:10:25.234064 slice_to_py_dist-0.2.1/pyproject.toml
--rw-r--r--   0        0        0        0 2023-07-21 16:09:15.461548 slice_to_py_dist-0.2.1/slice_to_py_dist/__init__.py
--rw-r--r--   0        0        0     3113 2023-07-12 09:02:11.606973 slice_to_py_dist-0.2.1/slice_to_py_dist/__main__.py
--rw-r--r--   0        0        0     4547 2023-07-14 03:59:36.872429 slice_to_py_dist-0.2.1/slice_to_py_dist/build_sdist.py
--rw-r--r--   0        0        0     2735 2023-07-14 03:59:36.872429 slice_to_py_dist-0.2.1/slice_to_py_dist/custom_build_backend/backend.py
--rw-r--r--   0        0        0      247 2023-07-12 09:02:11.606973 slice_to_py_dist-0.2.1/slice_to_py_dist/types.py
--rw-r--r--   0        0        0      852 2023-07-12 09:02:11.606973 slice_to_py_dist-0.2.1/slice_to_py_dist/utils.py
--rw-r--r--   0        0        0     7021 1970-01-01 00:00:00.000000 slice_to_py_dist-0.2.1/PKG-INFO
+-rw-r--r--   0        0        0     6376 2023-07-12 09:02:11.606973 slice_to_py_dist-0.3.0/README.md
+-rw-r--r--   0        0        0     1375 2023-07-23 17:47:06.115104 slice_to_py_dist-0.3.0/pyproject.toml
+-rw-r--r--   0        0        0        0 2023-07-23 17:45:55.490474 slice_to_py_dist-0.3.0/slice_to_py_dist/__init__.py
+-rw-r--r--   0        0        0     3114 2023-07-23 17:24:38.852989 slice_to_py_dist-0.3.0/slice_to_py_dist/__main__.py
+-rw-r--r--   0        0        0     4547 2023-07-14 03:59:36.872429 slice_to_py_dist-0.3.0/slice_to_py_dist/build_sdist.py
+-rw-r--r--   0        0        0     2735 2023-07-14 03:59:36.872429 slice_to_py_dist-0.3.0/slice_to_py_dist/custom_build_backend/backend.py
+-rw-r--r--   0        0        0      247 2023-07-12 09:02:11.606973 slice_to_py_dist-0.3.0/slice_to_py_dist/types.py
+-rw-r--r--   0        0        0      852 2023-07-12 09:02:11.606973 slice_to_py_dist-0.3.0/slice_to_py_dist/utils.py
+-rw-r--r--   0        0        0     7140 1970-01-01 00:00:00.000000 slice_to_py_dist-0.3.0/PKG-INFO
```

### Comparing `slice_to_py_dist-0.2.1/README.md` & `slice_to_py_dist-0.3.0/README.md`

 * *Files identical despite different names*

### Comparing `slice_to_py_dist-0.2.1/pyproject.toml` & `slice_to_py_dist-0.3.0/pyproject.toml`

 * *Files 14% similar despite different names*

```diff
@@ -1,13 +1,14 @@
 [tool.poetry]
 name = "slice_to_py_dist"
-version = "0.2.1"  # a placeholder; will be set dynamically by poetry-dynamic-versioning
-description = "Put a set of ZeroC/ICE slice files (.ice) into python distribution package."
+version = "0.3.0"  # a placeholder; will be set dynamically by poetry-dynamic-versioning
+description = "Pack a set of ZeroC/ICE slice files (.ice) into python distribution package."
 authors = ["Evgeny Klunko <eklunko@gmail.com>"]
 readme = "README.md"
+repository = "https://gitlab.com/evgk/slice_to_py_dist"
 
 [tool.poetry.dependencies]
 python = "^3.8"
 configargparse = "^1.5.5"
 toml = "^0.10.2"
 build = "^0.10.0"
```

### Comparing `slice_to_py_dist-0.2.1/slice_to_py_dist/__main__.py` & `slice_to_py_dist-0.3.0/slice_to_py_dist/__main__.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 #!/usr/bin/env python3
 """
-Put a set of ZeroC/ICE slice files (.ice) into python distribution package.
+Pack a set of ZeroC/ICE slice files (.ice) into python distribution package.
 """
 
 from __future__ import annotations
 
 import sys
 from typing import Any, Optional, cast
```

### Comparing `slice_to_py_dist-0.2.1/slice_to_py_dist/build_sdist.py` & `slice_to_py_dist-0.3.0/slice_to_py_dist/build_sdist.py`

 * *Files identical despite different names*

### Comparing `slice_to_py_dist-0.2.1/slice_to_py_dist/custom_build_backend/backend.py` & `slice_to_py_dist-0.3.0/slice_to_py_dist/custom_build_backend/backend.py`

 * *Files identical despite different names*

### Comparing `slice_to_py_dist-0.2.1/slice_to_py_dist/utils.py` & `slice_to_py_dist-0.3.0/slice_to_py_dist/utils.py`

 * *Files identical despite different names*

### Comparing `slice_to_py_dist-0.2.1/PKG-INFO` & `slice_to_py_dist-0.3.0/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,22 +1,24 @@
 Metadata-Version: 2.1
 Name: slice-to-py-dist
-Version: 0.2.1
-Summary: Put a set of ZeroC/ICE slice files (.ice) into python distribution package.
+Version: 0.3.0
+Summary: Pack a set of ZeroC/ICE slice files (.ice) into python distribution package.
+Home-page: https://gitlab.com/evgk/slice_to_py_dist
 Author: Evgeny Klunko
 Author-email: eklunko@gmail.com
 Requires-Python: >=3.8,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Requires-Dist: build (>=0.10.0,<0.11.0)
 Requires-Dist: configargparse (>=1.5.5,<2.0.0)
 Requires-Dist: toml (>=0.10.2,<0.11.0)
+Project-URL: Repository, https://gitlab.com/evgk/slice_to_py_dist
 Description-Content-Type: text/markdown
 
 # slice_to_py_dist: упаковка Slice файлов (ZeroC/ICE) в распространяемый python-пакет
 
 ## Описание
 *Slice* является языком описания интерфейсов сетевого взаимодействия для фреймворка *ZeroC/ICE*
 (далее *ICE*). Для того, чтобы приложения могли взаимодействовать между собой посредством
```

