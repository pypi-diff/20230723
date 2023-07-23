# Comparing `tmp/PyEasySQL-3.0.3.tar.gz` & `tmp/PyEasySQL-3.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "PyEasySQL-3.0.3.tar", last modified: Sat Jul 22 15:24:08 2023, max compression
+gzip compressed data, was "PyEasySQL-3.1.0.tar", last modified: Sun Jul 23 11:46:01 2023, max compression
```

## Comparing `PyEasySQL-3.0.3.tar` & `PyEasySQL-3.1.0.tar`

### file list

```diff
@@ -1,24 +1,24 @@
-drwxrwxrwx   0        0        0        0 2023-07-22 15:24:08.038012 PyEasySQL-3.0.3/
-drwxrwxrwx   0        0        0        0 2023-07-22 15:24:08.018067 PyEasySQL-3.0.3/EasySQL/
--rw-rw-rw-   0        0        0     3452 2023-07-09 09:35:55.000000 PyEasySQL-3.0.3/EasySQL/ABC.py
--rw-rw-rw-   0        0        0     2887 2021-06-27 12:24:21.000000 PyEasySQL-3.0.3/EasySQL/Characters.py
--rw-rw-rw-   0        0        0    14303 2023-07-22 14:35:27.000000 PyEasySQL-3.0.3/EasySQL/Classes.py
--rw-rw-rw-   0        0        0     5764 2023-07-18 13:18:56.000000 PyEasySQL-3.0.3/EasySQL/Commands.py
--rw-rw-rw-   0        0        0      305 2023-07-11 12:44:34.000000 PyEasySQL-3.0.3/EasySQL/Decorators.py
--rw-rw-rw-   0        0        0     2097 2023-07-09 09:35:55.000000 PyEasySQL-3.0.3/EasySQL/EasyInstances.py
--rw-rw-rw-   0        0        0      757 2023-06-08 19:41:42.000000 PyEasySQL-3.0.3/EasySQL/Exceptions.py
--rw-rw-rw-   0        0        0      457 2021-04-04 16:17:30.000000 PyEasySQL-3.0.3/EasySQL/Logging.py
--rw-rw-rw-   0        0        0      134 2023-07-09 09:35:55.000000 PyEasySQL-3.0.3/EasySQL/Tags.py
--rw-rw-rw-   0        0        0     2602 2023-07-11 12:55:43.000000 PyEasySQL-3.0.3/EasySQL/Types.py
--rw-rw-rw-   0        0        0     2496 2022-04-15 06:15:51.000000 PyEasySQL-3.0.3/EasySQL/Where.py
--rw-rw-rw-   0        0        0      290 2023-07-09 11:50:43.000000 PyEasySQL-3.0.3/EasySQL/__init__.py
--rw-rw-rw-   0        0        0     6499 2023-07-22 15:24:08.037017 PyEasySQL-3.0.3/PKG-INFO
-drwxrwxrwx   0        0        0        0 2023-07-22 15:24:08.033026 PyEasySQL-3.0.3/PyEasySQL.egg-info/
--rw-rw-rw-   0        0        0     6499 2023-07-22 15:24:05.000000 PyEasySQL-3.0.3/PyEasySQL.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      416 2023-07-22 15:24:05.000000 PyEasySQL-3.0.3/PyEasySQL.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-22 15:24:05.000000 PyEasySQL-3.0.3/PyEasySQL.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       16 2023-07-22 15:24:05.000000 PyEasySQL-3.0.3/PyEasySQL.egg-info/requires.txt
--rw-rw-rw-   0        0        0        8 2023-07-22 15:24:05.000000 PyEasySQL-3.0.3/PyEasySQL.egg-info/top_level.txt
--rw-rw-rw-   0        0        0     5119 2023-07-09 10:37:27.000000 PyEasySQL-3.0.3/README.md
--rw-rw-rw-   0        0        0       42 2023-07-22 15:24:08.038012 PyEasySQL-3.0.3/setup.cfg
--rw-rw-rw-   0        0        0      859 2023-07-22 14:35:27.000000 PyEasySQL-3.0.3/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 11:46:01.298695 PyEasySQL-3.1.0/
+drwxrwxrwx   0        0        0        0 2023-07-23 11:46:01.270209 PyEasySQL-3.1.0/EasySQL/
+-rw-rw-rw-   0        0        0     3607 2023-07-23 11:44:26.000000 PyEasySQL-3.1.0/EasySQL/ABC.py
+-rw-rw-rw-   0        0        0     2887 2021-06-27 12:24:21.000000 PyEasySQL-3.1.0/EasySQL/Characters.py
+-rw-rw-rw-   0        0        0    14303 2023-07-23 11:41:39.000000 PyEasySQL-3.1.0/EasySQL/Classes.py
+-rw-rw-rw-   0        0        0     5764 2023-07-18 13:18:56.000000 PyEasySQL-3.1.0/EasySQL/Commands.py
+-rw-rw-rw-   0        0        0      305 2023-07-11 12:44:34.000000 PyEasySQL-3.1.0/EasySQL/Decorators.py
+-rw-rw-rw-   0        0        0     2097 2023-07-09 09:35:55.000000 PyEasySQL-3.1.0/EasySQL/EasyInstances.py
+-rw-rw-rw-   0        0        0      757 2023-06-08 19:41:42.000000 PyEasySQL-3.1.0/EasySQL/Exceptions.py
+-rw-rw-rw-   0        0        0      457 2021-04-04 16:17:30.000000 PyEasySQL-3.1.0/EasySQL/Logging.py
+-rw-rw-rw-   0        0        0      161 2023-07-23 11:44:26.000000 PyEasySQL-3.1.0/EasySQL/Tags.py
+-rw-rw-rw-   0        0        0     3079 2023-07-23 11:44:26.000000 PyEasySQL-3.1.0/EasySQL/Types.py
+-rw-rw-rw-   0        0        0     2496 2022-04-15 06:15:51.000000 PyEasySQL-3.1.0/EasySQL/Where.py
+-rw-rw-rw-   0        0        0      290 2023-07-09 11:50:43.000000 PyEasySQL-3.1.0/EasySQL/__init__.py
+-rw-rw-rw-   0        0        0     6499 2023-07-23 11:46:01.297657 PyEasySQL-3.1.0/PKG-INFO
+drwxrwxrwx   0        0        0        0 2023-07-23 11:46:01.293043 PyEasySQL-3.1.0/PyEasySQL.egg-info/
+-rw-rw-rw-   0        0        0     6499 2023-07-23 11:46:00.000000 PyEasySQL-3.1.0/PyEasySQL.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      416 2023-07-23 11:46:00.000000 PyEasySQL-3.1.0/PyEasySQL.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 11:46:00.000000 PyEasySQL-3.1.0/PyEasySQL.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       16 2023-07-23 11:46:00.000000 PyEasySQL-3.1.0/PyEasySQL.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        8 2023-07-23 11:46:00.000000 PyEasySQL-3.1.0/PyEasySQL.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0     5119 2023-07-09 10:37:27.000000 PyEasySQL-3.1.0/README.md
+-rw-rw-rw-   0        0        0       42 2023-07-23 11:46:01.299682 PyEasySQL-3.1.0/setup.cfg
+-rw-rw-rw-   0        0        0      859 2023-07-23 11:15:02.000000 PyEasySQL-3.1.0/setup.py
```

### Comparing `PyEasySQL-3.0.3/EasySQL/ABC.py` & `PyEasySQL-3.1.0/EasySQL/ABC.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,19 +1,19 @@
 from abc import ABC
-from typing import Callable, Any
-
+from typing import Callable, Any, Iterable
 
 __all__ = ['SQLType', 'SQLTag', 'SQLCommand', 'SQLCommandExecutable', 'SQLExecutable',
            'CHARSET', 'make_collection', 'is_collection']
 
 
 class SQLType:
-    def __init__(self, name, *args, caster: Callable[[Any], Any] = None, get_caster: Callable[["SQLType"], Callable[[Any], Any]] = None, default: Any = None, parser: Callable[[Any], str] = None, modifiable: bool = False):
+    def __init__(self, name, *args, caster: Callable[[Any], Any] = None, get_caster: Callable[["SQLType"], Callable[[Any], Any]] = None, default: Any = None, parser: Callable[[Any], str] = None, modifiable: bool = False, tags: Iterable[str] = None):
         self._name = name
         self._args = args
+        self._tags = tags or ()
 
         self._modify_args = dict(caster=caster, get_caster=get_caster, default=default, parser=parser)
 
         if caster is None and get_caster is not None:
             caster = get_caster(self)
 
         if caster is None:
@@ -47,15 +47,19 @@
         return hash((self.name, self.args))
 
     def __repr__(self):
         return f'<SQLTYPE "{self.name}">'
 
     @property
     def name(self):
-        return f'{self._name}({",".join([str(arg) for arg in self._args])})' if self._args else self._name
+        name = f'{self._name}({",".join([str(arg) for arg in self._args])})' if self._args else self._name
+        for tag in self._tags:
+            name += f' {tag}'
+
+        return name
 
     def cast(self, value):
         return self._caster(value)
 
     def parse(self, value):
         return self._parser(self.cast(value))
```

### Comparing `PyEasySQL-3.0.3/EasySQL/Characters.py` & `PyEasySQL-3.1.0/EasySQL/Characters.py`

 * *Files identical despite different names*

### Comparing `PyEasySQL-3.0.3/EasySQL/Classes.py` & `PyEasySQL-3.1.0/EasySQL/Classes.py`

 * *Files identical despite different names*

### Comparing `PyEasySQL-3.0.3/EasySQL/Commands.py` & `PyEasySQL-3.1.0/EasySQL/Commands.py`

 * *Files identical despite different names*

### Comparing `PyEasySQL-3.0.3/EasySQL/EasyInstances.py` & `PyEasySQL-3.1.0/EasySQL/EasyInstances.py`

 * *Files identical despite different names*

### Comparing `PyEasySQL-3.0.3/EasySQL/Exceptions.py` & `PyEasySQL-3.1.0/EasySQL/Exceptions.py`

 * *Files identical despite different names*

### Comparing `PyEasySQL-3.0.3/EasySQL/Types.py` & `PyEasySQL-3.1.0/EasySQL/Types.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,19 +1,23 @@
 from .ABC import SQLType
 
 
-def _get_int_cast_(size):
+def _get_int_cast_(size, unsigned=False):
+    minimum = (-(2 ** (size - 1))) if unsigned else 0
+    maximum = (2 ** (size - 1) - 1) if unsigned else 2 ** size
+
     def cast(value):
         if value is None:
             return None
 
         value = int(value)
-        if value.bit_length() > size:
-            raise ValueError(f'can only accept {size} bits but got {value.bit_length()} bits')
-        return int(value)
+        if not (minimum <= value <= maximum):
+            raise ValueError(f'can only accept between {minimum} and {maximum}, but got {value}')
+
+        return value
 
     return cast
 
 
 def _float_cast(value):
     if value is None:
         return None
@@ -37,14 +41,19 @@
 
 INT64 = BIGINT = SQLType('BIGINT', caster=_get_int_cast_(64), default=0)
 INT32 = INT = INTEGER = SQLType('INT', caster=_get_int_cast_(32), default=0)
 INT24 = MEDIUMINT = SQLType('MEDIUMINT', caster=_get_int_cast_(24), default=0)
 INT16 = SMALLINT = SQLType('SMALLINT', caster=_get_int_cast_(16), default=0)
 INT8 = TINYINT = SQLType('TINYINT', caster=_get_int_cast_(8), default=0)
 
+BIGINT.UNSIGNED = SQLType('BIGINT', caster=_get_int_cast_(64, True), default=0)
+INTEGER.UNSIGNED = SQLType('BIGINT', caster=_get_int_cast_(32, True), default=0)
+MEDIUMINT.UNSIGNED = SQLType('BIGINT', caster=_get_int_cast_(24, True), default=0)
+SMALLINT.UNSIGNED = SQLType('BIGINT', caster=_get_int_cast_(16, True), default=0)
+
 BIT = SQLType('BIT', 1, get_caster=lambda self: _get_int_cast_(self.args[0]), default=0, modifiable=True)
 BOOL = SQLType('BIT', 1, caster=lambda value: None if value is None else True if value else False, default=False, parser=lambda value: '1' if value else '0')
 
 FLOAT = SQLType('FLOAT', caster=_float_cast, default=0.0)
 DOUBLE = SQLType('DOUBLE', 12, 6, caster=_float_cast, default=0.0, modifiable=True)
 DEC = DECIMAL = SQLType('DECIMAL', 12, 6, caster=_float_cast, default=0.0, modifiable=True)
```

### Comparing `PyEasySQL-3.0.3/EasySQL/Where.py` & `PyEasySQL-3.1.0/EasySQL/Where.py`

 * *Files identical despite different names*

### Comparing `PyEasySQL-3.0.3/PKG-INFO` & `PyEasySQL-3.1.0/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: PyEasySQL
-Version: 3.0.3
+Version: 3.1.0
 Summary: SQL Database management without even a SQL line
 Home-page: https://github.com/ashenguard/easysql
 Author: Ashenguard
 Author-email: Ashenguard@agmdev.xyz
 License: MIT License
 Description: # EasySQL
         ![Downloads](https://pepy.tech/badge/pyeasysql)
```

### Comparing `PyEasySQL-3.0.3/PyEasySQL.egg-info/PKG-INFO` & `PyEasySQL-3.1.0/PyEasySQL.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: PyEasySQL
-Version: 3.0.3
+Version: 3.1.0
 Summary: SQL Database management without even a SQL line
 Home-page: https://github.com/ashenguard/easysql
 Author: Ashenguard
 Author-email: Ashenguard@agmdev.xyz
 License: MIT License
 Description: # EasySQL
         ![Downloads](https://pepy.tech/badge/pyeasysql)
```

### Comparing `PyEasySQL-3.0.3/README.md` & `PyEasySQL-3.1.0/README.md`

 * *Files identical despite different names*

### Comparing `PyEasySQL-3.0.3/setup.py` & `PyEasySQL-3.1.0/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import setuptools
 
 with open("README.md", "r", encoding="utf-8") as fh:
     long_description = fh.read()
 
 setuptools.setup(
     name="PyEasySQL",
-    version="3.0.3",
+    version="3.1.0",
     license='MIT License',
     author="Ashenguard",
     author_email="Ashenguard@agmdev.xyz",
     description="SQL Database management without even a SQL line",
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/ashenguard/easysql",
```

