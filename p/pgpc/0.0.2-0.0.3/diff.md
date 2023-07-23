# Comparing `tmp/pgpc-0.0.2.tar.gz` & `tmp/pgpc-0.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pgpc-0.0.2.tar", last modified: Sat Jul 22 22:09:14 2023, max compression
+gzip compressed data, was "pgpc-0.0.3.tar", last modified: Sun Jul 23 11:06:03 2023, max compression
```

## Comparing `pgpc-0.0.2.tar` & `pgpc-0.0.3.tar`

### file list

```diff
@@ -1,18 +1,21 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:09:14.989771 pgpc-0.0.2/
--rw-r--r--   0 runner    (1001) docker     (123)    11340 2023-07-22 22:09:03.000000 pgpc-0.0.2/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)      138 2023-07-22 22:09:03.000000 pgpc-0.0.2/NOTICE
--rw-r--r--   0 runner    (1001) docker     (123)     1930 2023-07-22 22:09:14.985771 pgpc-0.0.2/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     1163 2023-07-22 22:09:03.000000 pgpc-0.0.2/README.md
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-22 22:09:14.989771 pgpc-0.0.2/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1087 2023-07-22 22:09:03.000000 pgpc-0.0.2/setup.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:09:14.985771 pgpc-0.0.2/src/
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:09:14.985771 pgpc-0.0.2/src/pgpc/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-22 22:09:03.000000 pgpc-0.0.2/src/pgpc/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2114 2023-07-22 22:09:03.000000 pgpc-0.0.2/src/pgpc/parser.py
--rw-r--r--   0 runner    (1001) docker     (123)     2685 2023-07-22 22:09:03.000000 pgpc-0.0.2/src/pgpc/scanner.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 22:09:14.985771 pgpc-0.0.2/src/pgpc.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1930 2023-07-22 22:09:14.000000 pgpc-0.0.2/src/pgpc.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      252 2023-07-22 22:09:14.000000 pgpc-0.0.2/src/pgpc.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-22 22:09:14.000000 pgpc-0.0.2/src/pgpc.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       32 2023-07-22 22:09:14.000000 pgpc-0.0.2/src/pgpc.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        5 2023-07-22 22:09:14.000000 pgpc-0.0.2/src/pgpc.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 11:06:03.763442 pgpc-0.0.3/
+-rw-r--r--   0 runner    (1001) docker     (123)    11340 2023-07-23 11:05:50.000000 pgpc-0.0.3/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)      138 2023-07-23 11:05:50.000000 pgpc-0.0.3/NOTICE
+-rw-r--r--   0 runner    (1001) docker     (123)     2177 2023-07-23 11:06:03.763442 pgpc-0.0.3/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     1410 2023-07-23 11:05:50.000000 pgpc-0.0.3/README.md
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 11:06:03.763442 pgpc-0.0.3/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1087 2023-07-23 11:05:50.000000 pgpc-0.0.3/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 11:06:03.759441 pgpc-0.0.3/src/
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 11:06:03.763442 pgpc-0.0.3/src/pgpc/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 11:05:50.000000 pgpc-0.0.3/src/pgpc/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2114 2023-07-23 11:05:50.000000 pgpc-0.0.3/src/pgpc/parser.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2685 2023-07-23 11:05:50.000000 pgpc-0.0.3/src/pgpc/scanner.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 11:06:03.763442 pgpc-0.0.3/src/pgpc.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     2177 2023-07-23 11:06:03.000000 pgpc-0.0.3/src/pgpc.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      301 2023-07-23 11:06:03.000000 pgpc-0.0.3/src/pgpc.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 11:06:03.000000 pgpc-0.0.3/src/pgpc.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       32 2023-07-23 11:06:03.000000 pgpc-0.0.3/src/pgpc.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       10 2023-07-23 11:06:03.000000 pgpc-0.0.3/src/pgpc.egg-info/top_level.txt
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 11:06:03.763442 pgpc-0.0.3/src/test/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 11:05:50.000000 pgpc-0.0.3/src/test/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)      827 2023-07-23 11:05:50.000000 pgpc-0.0.3/src/test/test_parse_text.py
```

### Comparing `pgpc-0.0.2/LICENSE` & `pgpc-0.0.3/LICENSE`

 * *Files identical despite different names*

### Comparing `pgpc-0.0.2/PKG-INFO` & `pgpc-0.0.3/PKG-INFO`

 * *Files 22% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pgpc
-Version: 0.0.2
+Version: 0.0.3
 Summary: A Python Generator based Parser Combinator library
 Home-page: https://github.com/neshkeev/pgpc
 Author: neshkeev
 Author-email: neshkeev@yandex.ru
 License: Apache 2.0
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
@@ -20,45 +20,56 @@
 License-File: LICENSE
 License-File: NOTICE
 
 # PGPC
 
 ## Overview
 
-**PGPC** is a parser combinator library. Its name is an acronym, and it stands for **P**ython **G**enerator based **P**arser **C**ombinator library.
+**PGPC** is a parser combinator library. Its name is an acronym, which stands for **P**ython **G**enerator based **P**arser **C**ombinator library.
 
 The library was heavily influenced by the [Parsec](https://github.com/haskell/parsec) monadic parser combinator library,
-so the transition from `Parsec` (and other parser combinators) to `PGPC` should be more or less easy.
+so the transition from `Parsec` (and other parser combinators) to `PGPC` should be relatively easy.
 
 The original idea of the library is emulating the `do`-notation with the `yield` Python keyword.
 
 ## Quick start
 
 The `@topology` decorator over a function allows the `yield` keyword work with parsers in a `do`-notation-like fashion:
 
+1. install the package: `pip install pgpc`
+1. save the following code into `main.py`:
 ```python
 from pgpc.scanner import TextScanner
 from pgpc.parser import Parser, topology, char, position, content
 
 
 @topology
-def hello(value: str):
+def parse_hello_world():
     start = yield position()
 
-    for c in value:
+    for c in "Hello":
         yield char(c)
 
+    yield char(",")
+    yield char(" ")
+
+    for c in "World":
+        yield char(c)
+
+    yield char("!")
+
     end = yield position()
     source = yield content()
 
-    return f"Parsed {source[start.offset:end.offset]} which started at {start} and ended at {end}"
+    return f"Parsed '{source[start.offset:end.offset]}' which started at {start} and ended at {end}"
 
 
 if __name__ == '__main__':
-    text = "HELLO"
-    
-    par: Parser[str] = hello(text)
-    
-    result = par(TextScanner(text))
-    
+    text = "Hello, World!"
+
+    hw_parser: Parser[str] = parse_hello_world()
+
+    result = hw_parser(TextScanner(text))
+
     print(result)
 ```
+3. run `main.py`: `python main.py`
```

### Comparing `pgpc-0.0.2/README.md` & `pgpc-0.0.3/README.md`

 * *Files 16% similar despite different names*

```diff
@@ -1,42 +1,53 @@
 # PGPC
 
 ## Overview
 
-**PGPC** is a parser combinator library. Its name is an acronym, and it stands for **P**ython **G**enerator based **P**arser **C**ombinator library.
+**PGPC** is a parser combinator library. Its name is an acronym, which stands for **P**ython **G**enerator based **P**arser **C**ombinator library.
 
 The library was heavily influenced by the [Parsec](https://github.com/haskell/parsec) monadic parser combinator library,
-so the transition from `Parsec` (and other parser combinators) to `PGPC` should be more or less easy.
+so the transition from `Parsec` (and other parser combinators) to `PGPC` should be relatively easy.
 
 The original idea of the library is emulating the `do`-notation with the `yield` Python keyword.
 
 ## Quick start
 
 The `@topology` decorator over a function allows the `yield` keyword work with parsers in a `do`-notation-like fashion:
 
+1. install the package: `pip install pgpc`
+1. save the following code into `main.py`:
 ```python
 from pgpc.scanner import TextScanner
 from pgpc.parser import Parser, topology, char, position, content
 
 
 @topology
-def hello(value: str):
+def parse_hello_world():
     start = yield position()
 
-    for c in value:
+    for c in "Hello":
         yield char(c)
 
+    yield char(",")
+    yield char(" ")
+
+    for c in "World":
+        yield char(c)
+
+    yield char("!")
+
     end = yield position()
     source = yield content()
 
-    return f"Parsed {source[start.offset:end.offset]} which started at {start} and ended at {end}"
+    return f"Parsed '{source[start.offset:end.offset]}' which started at {start} and ended at {end}"
 
 
 if __name__ == '__main__':
-    text = "HELLO"
-    
-    par: Parser[str] = hello(text)
-    
-    result = par(TextScanner(text))
-    
+    text = "Hello, World!"
+
+    hw_parser: Parser[str] = parse_hello_world()
+
+    result = hw_parser(TextScanner(text))
+
     print(result)
 ```
+3. run `main.py`: `python main.py`
```

### Comparing `pgpc-0.0.2/setup.py` & `pgpc-0.0.3/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 from setuptools import find_packages, setup
 
 with open("./README.md", "r") as f:
     long_description = f.read()
 
 setup(
     name="pgpc",
-    version="0.0.2",
+    version="0.0.3",
     description="A Python Generator based Parser Combinator library",
     package_dir={"": "src"},
     packages=find_packages(where="src"),
     long_description=long_description,
     long_description_content_type="text/markdown",
     url="https://github.com/neshkeev/pgpc",
     author="neshkeev",
```

### Comparing `pgpc-0.0.2/src/pgpc/parser.py` & `pgpc-0.0.3/src/pgpc/parser.py`

 * *Files identical despite different names*

### Comparing `pgpc-0.0.2/src/pgpc/scanner.py` & `pgpc-0.0.3/src/pgpc/scanner.py`

 * *Files identical despite different names*

### Comparing `pgpc-0.0.2/src/pgpc.egg-info/PKG-INFO` & `pgpc-0.0.3/src/pgpc.egg-info/PKG-INFO`

 * *Files 22% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pgpc
-Version: 0.0.2
+Version: 0.0.3
 Summary: A Python Generator based Parser Combinator library
 Home-page: https://github.com/neshkeev/pgpc
 Author: neshkeev
 Author-email: neshkeev@yandex.ru
 License: Apache 2.0
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
@@ -20,45 +20,56 @@
 License-File: LICENSE
 License-File: NOTICE
 
 # PGPC
 
 ## Overview
 
-**PGPC** is a parser combinator library. Its name is an acronym, and it stands for **P**ython **G**enerator based **P**arser **C**ombinator library.
+**PGPC** is a parser combinator library. Its name is an acronym, which stands for **P**ython **G**enerator based **P**arser **C**ombinator library.
 
 The library was heavily influenced by the [Parsec](https://github.com/haskell/parsec) monadic parser combinator library,
-so the transition from `Parsec` (and other parser combinators) to `PGPC` should be more or less easy.
+so the transition from `Parsec` (and other parser combinators) to `PGPC` should be relatively easy.
 
 The original idea of the library is emulating the `do`-notation with the `yield` Python keyword.
 
 ## Quick start
 
 The `@topology` decorator over a function allows the `yield` keyword work with parsers in a `do`-notation-like fashion:
 
+1. install the package: `pip install pgpc`
+1. save the following code into `main.py`:
 ```python
 from pgpc.scanner import TextScanner
 from pgpc.parser import Parser, topology, char, position, content
 
 
 @topology
-def hello(value: str):
+def parse_hello_world():
     start = yield position()
 
-    for c in value:
+    for c in "Hello":
         yield char(c)
 
+    yield char(",")
+    yield char(" ")
+
+    for c in "World":
+        yield char(c)
+
+    yield char("!")
+
     end = yield position()
     source = yield content()
 
-    return f"Parsed {source[start.offset:end.offset]} which started at {start} and ended at {end}"
+    return f"Parsed '{source[start.offset:end.offset]}' which started at {start} and ended at {end}"
 
 
 if __name__ == '__main__':
-    text = "HELLO"
-    
-    par: Parser[str] = hello(text)
-    
-    result = par(TextScanner(text))
-    
+    text = "Hello, World!"
+
+    hw_parser: Parser[str] = parse_hello_world()
+
+    result = hw_parser(TextScanner(text))
+
     print(result)
 ```
+3. run `main.py`: `python main.py`
```

