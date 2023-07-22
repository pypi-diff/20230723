# Comparing `tmp/fruitcraft-0.0.1.tar.gz` & `tmp/fruitcraft-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "fruitcraft-0.0.1.tar", max compression
+gzip compressed data, was "fruitcraft-0.0.2.tar", max compression
```

## Comparing `fruitcraft-0.0.1.tar` & `fruitcraft-0.0.2.tar`

### file list

```diff
@@ -1,6 +1,9 @@
--rw-r--r--   0        0        0     1068 2023-07-19 13:26:22.980145 fruitcraft-0.0.1/LICENSE
--rw-r--r--   0        0        0      128 2023-07-19 13:26:22.980145 fruitcraft-0.0.1/README.md
--rw-r--r--   0        0        0       99 2023-07-19 13:26:22.980145 fruitcraft-0.0.1/fruitcraft/__init__.py
--rw-r--r--   0        0        0       74 2023-07-19 13:26:22.980145 fruitcraft-0.0.1/fruitcraft/client.py
--rw-r--r--   0        0        0      809 2023-07-19 13:26:22.980145 fruitcraft-0.0.1/pyproject.toml
--rw-r--r--   0        0        0     1026 1970-01-01 00:00:00.000000 fruitcraft-0.0.1/PKG-INFO
+-rw-r--r--   0        0        0     1068 2023-07-21 22:41:52.689190 fruitcraft-0.0.2/LICENSE
+-rw-r--r--   0        0        0      128 2023-07-21 22:41:52.689190 fruitcraft-0.0.2/README.md
+-rw-r--r--   0        0        0       99 2023-07-21 22:41:52.689190 fruitcraft-0.0.2/fruitcraft/__init__.py
+-rw-r--r--   0        0        0    12326 2023-07-21 22:41:52.689190 fruitcraft-0.0.2/fruitcraft/client.py
+-rw-r--r--   0        0        0    21900 2023-07-21 22:41:52.689190 fruitcraft-0.0.2/fruitcraft/f_types/__init__.py
+-rw-r--r--   0        0        0      727 2023-07-21 22:41:52.689190 fruitcraft-0.0.2/fruitcraft/f_types/errors.py
+-rw-r--r--   0        0        0     3985 2023-07-21 22:41:52.689190 fruitcraft-0.0.2/fruitcraft/f_types/utils.py
+-rw-r--r--   0        0        0      809 2023-07-21 22:41:52.689190 fruitcraft-0.0.2/pyproject.toml
+-rw-r--r--   0        0        0     1026 1970-01-01 00:00:00.000000 fruitcraft-0.0.2/PKG-INFO
```

### Comparing `fruitcraft-0.0.1/LICENSE` & `fruitcraft-0.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `fruitcraft-0.0.1/pyproject.toml` & `fruitcraft-0.0.2/pyproject.toml`

 * *Files 12% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "fruitcraft"
-version = "0.0.1"
+version = "0.0.2"
 description = "Full Python Wrapper for fruitcraft game API. By Mr.AW ."
 authors = ["Mr. AW <mrawfruitly@gmail.com>"]
 packages = [
     { include = "fruitcraft" }
 ]
 classifiers = [
     "Programming Language :: Python :: 3",
```

### Comparing `fruitcraft-0.0.1/PKG-INFO` & `fruitcraft-0.0.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: fruitcraft
-Version: 0.0.1
+Version: 0.0.2
 Summary: Full Python Wrapper for fruitcraft game API. By Mr.AW .
 Home-page: https://github.com/MrAwFruitly/FruitcraftClient-py
 Keywords: fruit,fruitcraft,fruit-craft,game-library
 Author: Mr. AW
 Author-email: mrawfruitly@gmail.com
 Requires-Python: >=3.7,<4.0
 Classifier: License :: OSI Approved :: MIT License
```

