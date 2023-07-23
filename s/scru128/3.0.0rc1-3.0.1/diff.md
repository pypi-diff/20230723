# Comparing `tmp/scru128-3.0.0rc1.tar.gz` & `tmp/scru128-3.0.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "scru128-3.0.0rc1.tar", max compression
+gzip compressed data, was "scru128-3.0.1.tar", max compression
```

## Comparing `scru128-3.0.0rc1.tar` & `scru128-3.0.1.tar`

### file list

```diff
@@ -1,6 +1,6 @@
--rw-r--r--   0        0        0    11357 2021-09-26 06:39:06.272667 scru128-3.0.0rc1/LICENSE
--rw-r--r--   0        0        0     2493 2023-06-21 14:11:55.014614 scru128-3.0.0rc1/README.md
--rw-r--r--   0        0        0      681 2023-06-21 14:11:55.015256 scru128-3.0.0rc1/pyproject.toml
--rw-r--r--   0        0        0    11546 2023-06-21 14:11:55.015730 scru128-3.0.0rc1/scru128/__init__.py
--rw-r--r--   0        0        0     2134 2022-10-30 06:25:18.337374 scru128-3.0.0rc1/scru128/cli/__init__.py
--rw-r--r--   0        0        0     3211 1970-01-01 00:00:00.000000 scru128-3.0.0rc1/PKG-INFO
+-rw-r--r--   0        0        0    11357 2021-09-26 06:39:06.272667 scru128-3.0.1/LICENSE
+-rw-r--r--   0        0        0     2493 2023-06-21 14:11:55.014614 scru128-3.0.1/README.md
+-rw-r--r--   0        0        0      671 2023-07-23 13:20:28.516601 scru128-3.0.1/pyproject.toml
+-rw-r--r--   0        0        0    11549 2023-07-23 13:20:28.517176 scru128-3.0.1/scru128/__init__.py
+-rw-r--r--   0        0        0     2134 2022-10-30 06:25:18.337374 scru128-3.0.1/scru128/cli/__init__.py
+-rw-r--r--   0        0        0     3208 1970-01-01 00:00:00.000000 scru128-3.0.1/PKG-INFO
```

### Comparing `scru128-3.0.0rc1/LICENSE` & `scru128-3.0.1/LICENSE`

 * *Files identical despite different names*

### Comparing `scru128-3.0.0rc1/README.md` & `scru128-3.0.1/README.md`

 * *Files identical despite different names*

### Comparing `scru128-3.0.0rc1/pyproject.toml` & `scru128-3.0.1/pyproject.toml`

 * *Files 22% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "scru128"
-version = "3.0.0rc1"
+version = "3.0.1"
 description = "SCRU128: Sortable, Clock and Random number-based Unique identifier"
 license = "Apache-2.0"
 authors = ["LiosK <contact@mail.liosk.net>"]
 readme = "README.md"
 homepage = "https://github.com/scru128/python"
 keywords = ["identifier", "uuid", "guid", "ulid", "ksuid"]
 classifiers = ["Operating System :: OS Independent"]
@@ -13,13 +13,13 @@
 scru128 = "scru128.cli:generate"
 scru128-inspect = "scru128.cli:inspect"
 
 [tool.poetry.dependencies]
 python = "^3.8"
 
 [tool.poetry.dev-dependencies]
-black = "^23.3.0"
-mypy = "^1.4.0"
+black = "^23.7.0"
+mypy = "^1.4.1"
 
 [build-system]
-requires = ["poetry-core>=1.0.0"]
+requires = ["poetry-core"]
 build-backend = "poetry.core.masonry.api"
```

### Comparing `scru128-3.0.0rc1/scru128/__init__.py` & `scru128-3.0.1/scru128/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -149,15 +149,15 @@
     | ---------------------- | --------- | ------- | ------------------- |
     | generate               | Now       | Safe    | Resets generator    |
     | generate_or_abort      | Now       | Safe    | Returns `None`      |
     | generate_or_reset_core | Argument  | Unsafe  | Resets generator    |
     | generate_or_abort_core | Argument  | Unsafe  | Returns `None`      |
 
     All of these methods return monotonically increasing IDs unless a `timestamp`
-    provided is significantly (by default, ten seconds or more) smaller than the one
+    provided is significantly (by default, more than ten seconds) smaller than the one
     embedded in the immediately preceding ID. If such a significant clock rollback is
     detected, the `generate` (or_reset) method resets the generator and returns a new ID
     based on the given `timestamp`, while the `or_abort` variants abort and return
     `None`. The `core` functions offer low-level thread-unsafe primitives.
     """
 
     def __init__(self, *, rng: typing.Any = None) -> None:
@@ -254,15 +254,15 @@
             raise ValueError("`timestamp` must be a 48-bit positive integer")
         elif not (0 <= rollback_allowance <= MAX_TIMESTAMP):
             raise ValueError("`rollback_allowance` out of reasonable range")
 
         if timestamp > self._timestamp:
             self._timestamp = timestamp
             self._counter_lo = self._rng.getrandbits(24)
-        elif timestamp + rollback_allowance > self._timestamp:
+        elif timestamp + rollback_allowance >= self._timestamp:
             # go on with previous timestamp if new one is not much smaller
             self._counter_lo += 1
             if self._counter_lo > MAX_COUNTER_LO:
                 self._counter_lo = 0
                 self._counter_hi += 1
                 if self._counter_hi > MAX_COUNTER_HI:
                     self._counter_hi = 0
```

### Comparing `scru128-3.0.0rc1/scru128/cli/__init__.py` & `scru128-3.0.1/scru128/cli/__init__.py`

 * *Files identical despite different names*

### Comparing `scru128-3.0.0rc1/PKG-INFO` & `scru128-3.0.1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: scru128
-Version: 3.0.0rc1
+Version: 3.0.1
 Summary: SCRU128: Sortable, Clock and Random number-based Unique identifier
 Home-page: https://github.com/scru128/python
 License: Apache-2.0
 Keywords: identifier,uuid,guid,ulid,ksuid
 Author: LiosK
 Author-email: contact@mail.liosk.net
 Requires-Python: >=3.8,<4.0
```

