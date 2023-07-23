# Comparing `tmp/iterlite-0.2.0.tar.gz` & `tmp/iterlite-0.2.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "iterlite-0.2.0.tar", last modified: Sun Jul 23 20:33:28 2023, max compression
+gzip compressed data, was "iterlite-0.2.1.tar", last modified: Sun Jul 23 20:45:36 2023, max compression
```

## Comparing `iterlite-0.2.0.tar` & `iterlite-0.2.1.tar`

### file list

```diff
@@ -1,13 +1,13 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 20:33:28.010592 iterlite-0.2.0/
--rw-rw-rw-   0        0        0     1968 2023-07-23 20:33:28.009593 iterlite-0.2.0/PKG-INFO
--rw-rw-rw-   0        0        0     1432 2023-06-27 16:54:51.000000 iterlite-0.2.0/README.md
-drwxrwxrwx   0        0        0        0 2023-07-23 20:33:28.002586 iterlite-0.2.0/iterlite/
--rw-rw-rw-   0        0        0       80 2023-07-23 20:31:24.000000 iterlite-0.2.0/iterlite/__init__.py
--rw-rw-rw-   0        0        0     7414 2023-07-23 20:31:06.000000 iterlite-0.2.0/iterlite/enumerable.py
-drwxrwxrwx   0        0        0        0 2023-07-23 20:33:28.008594 iterlite-0.2.0/iterlite.egg-info/
--rw-rw-rw-   0        0        0     1968 2023-07-23 20:33:27.000000 iterlite-0.2.0/iterlite.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      190 2023-07-23 20:33:27.000000 iterlite-0.2.0/iterlite.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 20:33:27.000000 iterlite-0.2.0/iterlite.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0        9 2023-07-23 20:33:27.000000 iterlite-0.2.0/iterlite.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-23 20:33:28.010592 iterlite-0.2.0/setup.cfg
--rw-rw-rw-   0        0        0      845 2023-07-05 12:40:32.000000 iterlite-0.2.0/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 20:45:36.529576 iterlite-0.2.1/
+-rw-rw-rw-   0        0        0     1968 2023-07-23 20:45:36.528564 iterlite-0.2.1/PKG-INFO
+-rw-rw-rw-   0        0        0     1432 2023-06-27 16:54:51.000000 iterlite-0.2.1/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 20:45:36.522546 iterlite-0.2.1/iterlite/
+-rw-rw-rw-   0        0        0       80 2023-07-23 20:44:33.000000 iterlite-0.2.1/iterlite/__init__.py
+-rw-rw-rw-   0        0        0     7261 2023-07-23 20:45:10.000000 iterlite-0.2.1/iterlite/enumerable.py
+drwxrwxrwx   0        0        0        0 2023-07-23 20:45:36.527435 iterlite-0.2.1/iterlite.egg-info/
+-rw-rw-rw-   0        0        0     1968 2023-07-23 20:45:36.000000 iterlite-0.2.1/iterlite.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      190 2023-07-23 20:45:36.000000 iterlite-0.2.1/iterlite.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 20:45:36.000000 iterlite-0.2.1/iterlite.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0        9 2023-07-23 20:45:36.000000 iterlite-0.2.1/iterlite.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 20:45:36.529576 iterlite-0.2.1/setup.cfg
+-rw-rw-rw-   0        0        0      845 2023-07-05 12:40:32.000000 iterlite-0.2.1/setup.py
```

### Comparing `iterlite-0.2.0/PKG-INFO` & `iterlite-0.2.1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: iterlite
-Version: 0.2.0
+Version: 0.2.1
 Summary: rust like iterators for python
 Home-page: https://github.com/peturparkur/python-rustlite
 Author: Peter Nagymathe
 Author-email: peter@nagymathe.xyz
 License: AGPLv3+
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3 :: Only
```

### Comparing `iterlite-0.2.0/README.md` & `iterlite-0.2.1/README.md`

 * *Files identical despite different names*

### Comparing `iterlite-0.2.0/iterlite/enumerable.py` & `iterlite-0.2.1/iterlite/enumerable.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,11 +1,10 @@
 from __future__ import annotations
 from concurrent.futures import ThreadPoolExecutor, ProcessPoolExecutor
 from typing import *
-import multiprocessing as mp
 from collections import deque
 import itertools
 import functools
 from typing import Callable, Iterable
 
 T = TypeVar('T')
 R = TypeVar('R')
@@ -74,19 +73,19 @@
     
     def groupby_agg(self, key: Callable[[T], R]):
         """
         Groupby on consecutive keys
 
         Note: Does not consume iterator
         """
-        return Iter(itertools.groupby(self, key))
+        return Iter(itertools.groupby(self, key)).map(lambda pair: (pair[0], Iter(pair[1])))
 
     def batch(self, n: int):
         return self.enumerate() \
-            .groupby(lambda x: x[0] // n) \
+            .groupby_agg(lambda x: x[0] // n) \
             .map(lambda x: x[1].map(lambda y: y[1]))
     
     def concat(self, other: Iterable[T]) -> Iter[T]:
         return Iter(itertools.chain(self, other))
     
     def count(self) -> int:
         return sum(1 for _ in self)
@@ -205,21 +204,14 @@
     def keys(self) -> Iter[K]:
         return Iter(iter(super().keys()))
     def values(self) -> Iter[V]:
         return Iter(iter(super().values()))
     def items(self) -> Iter[tuple[K, V]]:
         return Iter(iter(super().items()))
 
-class FuncWrapper(Callable[[T], R]):
-    def __init__(self, f: Callable[[T], R]):
-        self.f = f
-    def __call__(self, x: T) -> R:
-        return self.f(x)
-
-
 class AsyncIter(Iter[T]):
     def __init__(self, iterator: Iterable[T], func:Callable[[T], R], threadpool_factory: Optional[Callable[[], ThreadPoolExecutor]] = None) -> None:
         super().__init__(iterator)
         self.func = func
         self.factory = lambda: ThreadPoolExecutor()
     
     def __iter__(self) -> AsyncIter[R]:
```

### Comparing `iterlite-0.2.0/iterlite.egg-info/PKG-INFO` & `iterlite-0.2.1/iterlite.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: iterlite
-Version: 0.2.0
+Version: 0.2.1
 Summary: rust like iterators for python
 Home-page: https://github.com/peturparkur/python-rustlite
 Author: Peter Nagymathe
 Author-email: peter@nagymathe.xyz
 License: AGPLv3+
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3 :: Only
```

### Comparing `iterlite-0.2.0/setup.py` & `iterlite-0.2.1/setup.py`

 * *Files identical despite different names*

