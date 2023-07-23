# Comparing `tmp/utilki-0.6.2.tar.gz` & `tmp/utilki-0.6.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "utilki-0.6.2.tar", max compression
+gzip compressed data, was "utilki-0.6.4.tar", max compression
```

## Comparing `utilki-0.6.2.tar` & `utilki-0.6.4.tar`

### file list

```diff
@@ -1,7 +1,7 @@
--rw-r--r--   0        0        0     1064 2023-07-12 02:38:23.539777 utilki-0.6.2/README.md
--rw-r--r--   0        0        0      525 2023-07-12 02:38:23.539777 utilki-0.6.2/pyproject.toml
--rw-r--r--   0        0        0       98 2023-07-12 02:38:23.539777 utilki-0.6.2/utilki/__init__.py
--rw-r--r--   0        0        0     2257 2023-07-12 02:38:23.539777 utilki-0.6.2/utilki/cli.py
--rw-r--r--   0        0        0     6761 2023-07-12 02:38:23.539777 utilki-0.6.2/utilki/log_utils.py
--rw-r--r--   0        0        0     7325 2023-07-12 02:38:23.539777 utilki-0.6.2/utilki/task_mixin.py
--rw-r--r--   0        0        0     1659 1970-01-01 00:00:00.000000 utilki-0.6.2/PKG-INFO
+-rw-r--r--   0        0        0     1064 2023-07-23 20:20:30.449570 utilki-0.6.4/README.md
+-rw-r--r--   0        0        0      544 2023-07-23 20:20:30.449570 utilki-0.6.4/pyproject.toml
+-rw-r--r--   0        0        0       98 2023-07-23 20:20:30.449570 utilki-0.6.4/utilki/__init__.py
+-rw-r--r--   0        0        0     2257 2023-07-23 20:20:30.449570 utilki-0.6.4/utilki/cli.py
+-rw-r--r--   0        0        0     7050 2023-07-23 20:20:30.449570 utilki-0.6.4/utilki/log_utils.py
+-rw-r--r--   0        0        0     7325 2023-07-23 20:20:30.449570 utilki-0.6.4/utilki/task_mixin.py
+-rw-r--r--   0        0        0     1641 1970-01-01 00:00:00.000000 utilki-0.6.4/PKG-INFO
```

### Comparing `utilki-0.6.2/README.md` & `utilki-0.6.4/README.md`

 * *Files identical despite different names*

### Comparing `utilki-0.6.2/pyproject.toml` & `utilki-0.6.4/pyproject.toml`

 * *Files 26% similar despite different names*

```diff
@@ -1,18 +1,19 @@
 [tool.poetry]
 name = "utilki"
-version = "0.6.2"
+version = "0.6.4"
 description = "A collection of useful utilities"
 readme = "README.md"
 authors = ["Khaidar Bikmaev <khaidar@bikmaev.com>"]
 
 [tool.poetry.dependencies]
-python = ">=3.7"
+python = ">=3.8"
 click = "^8.1.3"
 pydantic = "^1.10.7"
+pandas = ">=1.3.3"
 
 [tool.poetry.dev-dependencies]
 pytest = "^5.2"
 black = "^23.3.0"
 flake8 = "*"
 pytest-cov = "^4.0.0"
```

### Comparing `utilki-0.6.2/utilki/cli.py` & `utilki-0.6.4/utilki/cli.py`

 * *Files identical despite different names*

### Comparing `utilki-0.6.2/utilki/log_utils.py` & `utilki-0.6.4/utilki/log_utils.py`

 * *Files 3% similar despite different names*

```diff
@@ -1,11 +1,12 @@
 from collections.abc import Sized, Iterator
 import logging
 import sys
 from typing import Any, Callable, Optional, TypeVar, Generic, Iterable
+import pandas as pd
 
 
 def set_global(name: str, value: Any):
     globals()[name] = value
 
 
 def get_global(name: str, default=None) -> Any:
@@ -171,22 +172,24 @@
     def __init__(
         self,
         iterator: Iterable[A],
         name: str = "",
         num_steps: int = 10,
         precision: int = 1,
         print_idx: bool = False,
-    ):
+    ) -> None:
         if not isinstance(iterator, Iterable):
             raise ValueError("Passed object is not iterable")
         if not isinstance(iterator, Sized):
             raise ValueError("Passed object does not have a size")
 
         self.print_idx = print_idx
         self.iterator: Iterator[A] = iter(iterator)
+        if isinstance(iterator, pd.DataFrame):
+            self.iterator = iterator.iterrows()  # type: ignore
         self.len = len(iterator)
         self.name = name
         self.num_steps = num_steps
         if self.num_steps > self.len:
             self.num_steps = self.len
 
         if self.num_steps < 1:
@@ -253,19 +256,25 @@
     for i in progress([0.1, 0.2, 0.3], name="test4"):
         log(i)
         time.sleep(0.001)
 
     log("hello world")
 
     # logging.getLogger("ayy").setLevel(logging.INFO)
-    logger("ayy").info().fn_level(logging.CRITICAL).basic_config()
+    logger("ayy").info().fn_info().basic_config()
 
     set_global("ayy", "lmao")
     value = get_global("ayy")
     log(value)
 
     from datetime import datetime
 
     err(datetime.now())
 
     for i in progress([], name="test5"):
         time.sleep(0.001)
+
+    a = pd.DataFrame([{"a": 1, "b": 2}, {"a": 3, "b": 4}])
+
+    for idx, row in progress(a, name="test6"):  # type: ignore
+        log(row)
+        time.sleep(0.001)
```

### Comparing `utilki-0.6.2/utilki/task_mixin.py` & `utilki-0.6.4/utilki/task_mixin.py`

 * *Files identical despite different names*

### Comparing `utilki-0.6.2/PKG-INFO` & `utilki-0.6.4/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,21 +1,21 @@
 Metadata-Version: 2.1
 Name: utilki
-Version: 0.6.2
+Version: 0.6.4
 Summary: A collection of useful utilities
 Author: Khaidar Bikmaev
 Author-email: khaidar@bikmaev.com
-Requires-Python: >=3.7
+Requires-Python: >=3.8
 Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Requires-Dist: click (>=8.1.3,<9.0.0)
+Requires-Dist: pandas (>=1.3.3)
 Requires-Dist: pydantic (>=1.10.7,<2.0.0)
 Description-Content-Type: text/markdown
 
 # utilki
 
 [![codecov](https://codecov.io/gh/realbikmaev/utilki/branch/main/graph/badge.svg?token=VN0UMT7O9A)](https://codecov.io/gh/realbikmaev/utilki)
```

