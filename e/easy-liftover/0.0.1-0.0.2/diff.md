# Comparing `tmp/easy_liftover-0.0.1.tar.gz` & `tmp/easy_liftover-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "easy_liftover-0.0.1.tar", max compression
+gzip compressed data, was "easy_liftover-0.0.2.tar", max compression
```

## Comparing `easy_liftover-0.0.1.tar` & `easy_liftover-0.0.2.tar`

### file list

```diff
@@ -1,15 +1,15 @@
--rw-r--r--   0        0        0    35149 2023-07-23 10:17:10.758412 easy_liftover-0.0.1/LICENSE
--rw-r--r--   0        0        0       15 2023-07-23 10:17:10.758412 easy_liftover-0.0.1/README.md
--rw-r--r--   0        0        0      716 2023-07-23 10:17:10.758412 easy_liftover-0.0.1/pyproject.toml
--rw-r--r--   0        0        0       67 2023-07-23 10:17:10.758412 easy_liftover-0.0.1/src/__init__.py
--rw-r--r--   0        0        0      189 2023-07-23 10:17:10.758412 easy_liftover-0.0.1/src/genomes.py
--rw-r--r--   0        0        0      117 2023-07-23 10:17:10.758412 easy_liftover-0.0.1/src/lifters/__init__.py
--rw-r--r--   0        0        0     1919 2023-07-23 10:17:10.758412 easy_liftover-0.0.1/src/lifters/abstract.py
--rw-r--r--   0        0        0      680 2023-07-23 10:17:10.758412 easy_liftover-0.0.1/src/lifters/bed.py
--rw-r--r--   0        0        0      661 2023-07-23 10:17:10.758412 easy_liftover-0.0.1/src/lifters/gff.py
--rw-r--r--   0        0        0     1825 2023-07-23 10:17:10.758412 easy_liftover-0.0.1/src/lifters/wig.py
--rw-r--r--   0        0        0      610 2023-07-23 10:17:10.758412 easy_liftover-0.0.1/src/targets.py
--rw-r--r--   0        0        0      770 2023-07-23 10:17:10.758412 easy_liftover-0.0.1/src/test_lifters.py
--rw-r--r--   0        0        0     1231 2023-07-23 10:17:10.758412 easy_liftover-0.0.1/src/types.json
--rw-r--r--   0        0        0     1224 2023-07-23 10:17:10.758412 easy_liftover-0.0.1/src/uplift.py
--rw-r--r--   0        0        0      769 1970-01-01 00:00:00.000000 easy_liftover-0.0.1/PKG-INFO
+-rw-r--r--   0        0        0    35149 2023-07-23 11:08:25.614800 easy_liftover-0.0.2/LICENSE
+-rw-r--r--   0        0        0      459 2023-07-23 11:08:25.614800 easy_liftover-0.0.2/README.md
+-rw-r--r--   0        0        0      729 2023-07-23 11:08:25.618800 easy_liftover-0.0.2/pyproject.toml
+-rw-r--r--   0        0        0       67 2023-07-23 11:08:25.618800 easy_liftover-0.0.2/src/__init__.py
+-rw-r--r--   0        0        0      189 2023-07-23 11:08:25.618800 easy_liftover-0.0.2/src/genomes.py
+-rw-r--r--   0        0        0      117 2023-07-23 11:08:25.618800 easy_liftover-0.0.2/src/lifters/__init__.py
+-rw-r--r--   0        0        0     1931 2023-07-23 11:08:25.618800 easy_liftover-0.0.2/src/lifters/abstract.py
+-rw-r--r--   0        0        0      680 2023-07-23 11:08:25.618800 easy_liftover-0.0.2/src/lifters/bed.py
+-rw-r--r--   0        0        0      661 2023-07-23 11:08:25.618800 easy_liftover-0.0.2/src/lifters/gff.py
+-rw-r--r--   0        0        0     1825 2023-07-23 11:08:25.618800 easy_liftover-0.0.2/src/lifters/wig.py
+-rw-r--r--   0        0        0      610 2023-07-23 11:08:25.618800 easy_liftover-0.0.2/src/targets.py
+-rw-r--r--   0        0        0      770 2023-07-23 11:08:25.618800 easy_liftover-0.0.2/src/test_lifters.py
+-rw-r--r--   0        0        0     1231 2023-07-23 11:08:25.618800 easy_liftover-0.0.2/src/types.json
+-rw-r--r--   0        0        0     1223 2023-07-23 11:08:25.618800 easy_liftover-0.0.2/src/uplift.py
+-rw-r--r--   0        0        0     1174 1970-01-01 00:00:00.000000 easy_liftover-0.0.2/PKG-INFO
```

### Comparing `easy_liftover-0.0.1/LICENSE` & `easy_liftover-0.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `easy_liftover-0.0.1/pyproject.toml` & `easy_liftover-0.0.2/pyproject.toml`

 * *Files 6% similar despite different names*

```diff
@@ -1,30 +1,29 @@
 [build-system]
 requires = ["poetry-core>=1.0.0"]
 build-backend = "poetry.core.masonry.api"
 
 [tool.poetry]
 name = "easy-liftover"
-version = "0.0.1"
+version = "0.0.2"
 description = "A python package for lifting over biological files"
 packages = [
     { include = "*", from = "src" },
 ]
 license = "MIT"
 authors = ["Nico Trummer <nictru32@gmail.com>"]
 repository = "https://github.com/biomedbigdata/easyUplift"
 homepage = "https://github.com/biomedbigdata/easyUplift"
 readme = "README.md"
 
 [tool.poetry.dependencies]
 python = ">=3.8.1"
 requests = "^2.26.0"
 beautifulsoup4 = "^4.9.3"
-pyliftover = "^0.4"
 
 [tool.poetry.dev-dependencies]
 pytest = "^6.2.4"
 pytest-cov = "^2.12.1"
 flake8 = "^6.0.0"
 
 [tool.pytest.ini_options]
-addopts = "--cov"
+addopts = "--cov --ignore=src/lifters/pyliftover"
```

### Comparing `easy_liftover-0.0.1/src/lifters/abstract.py` & `easy_liftover-0.0.2/src/lifters/abstract.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 from abc import ABC, abstractmethod
-from pyliftover import LiftOver
+from .pyliftover.pyliftover import LiftOver
 from typing import Tuple
 
 
 class AbstractLifter(ABC):
     """Abstract class for lifters."""
 
     def __init__(self, from_ga: str, to_ga: str):
```

### Comparing `easy_liftover-0.0.1/src/lifters/bed.py` & `easy_liftover-0.0.2/src/lifters/bed.py`

 * *Files identical despite different names*

### Comparing `easy_liftover-0.0.1/src/lifters/gff.py` & `easy_liftover-0.0.2/src/lifters/gff.py`

 * *Files identical despite different names*

### Comparing `easy_liftover-0.0.1/src/lifters/wig.py` & `easy_liftover-0.0.2/src/lifters/wig.py`

 * *Files identical despite different names*

### Comparing `easy_liftover-0.0.1/src/targets.py` & `easy_liftover-0.0.2/src/targets.py`

 * *Files identical despite different names*

### Comparing `easy_liftover-0.0.1/src/test_lifters.py` & `easy_liftover-0.0.2/src/test_lifters.py`

 * *Files identical despite different names*

### Comparing `easy_liftover-0.0.1/src/types.json` & `easy_liftover-0.0.2/src/types.json`

 * *Files identical despite different names*

### Comparing `easy_liftover-0.0.1/src/uplift.py` & `easy_liftover-0.0.2/src/uplift.py`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,9 @@
 from .lifters import BedLifter, GffLifter, WigLifter, AbstractLifter
 
-
 def uplift(
     fromGenome: str, toGenome: str, path: str, file_type: "str | None" = None
 ) -> str:
     """
     Uplifts a file from one genome build to another.
 
     Parameters:
```

