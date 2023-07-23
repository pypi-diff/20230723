# Comparing `tmp/seagoat-0.5.4.tar.gz` & `tmp/seagoat-0.5.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "seagoat-0.5.4.tar", max compression
+gzip compressed data, was "seagoat-0.5.5.tar", max compression
```

## Comparing `seagoat-0.5.4.tar` & `seagoat-0.5.5.tar`

### file list

```diff
@@ -1,15 +1,15 @@
--rw-r--r--   0        0        0     1070 2023-07-20 12:13:37.823820 seagoat-0.5.4/LICENSE
--rw-r--r--   0        0        0      957 2023-07-20 12:13:37.823820 seagoat-0.5.4/README.md
--rw-r--r--   0        0        0     3028 2023-07-20 12:13:38.707830 seagoat-0.5.4/pyproject.toml
--rw-r--r--   0        0        0       22 2023-07-20 12:13:37.827820 seagoat-0.5.4/seagoat/__init__.py
--rw-r--r--   0        0        0     1601 2023-07-20 12:13:37.827820 seagoat-0.5.4/seagoat/cache.py
--rw-r--r--   0        0        0     2744 2023-07-20 12:13:37.827820 seagoat-0.5.4/seagoat/cli.py
--rw-r--r--   0        0        0      196 2023-07-20 12:13:37.827820 seagoat-0.5.4/seagoat/common.py
--rw-r--r--   0        0        0     4512 2023-07-20 12:13:37.827820 seagoat-0.5.4/seagoat/engine.py
--rw-r--r--   0        0        0     3492 2023-07-20 12:13:37.827820 seagoat-0.5.4/seagoat/file.py
--rw-r--r--   0        0        0     2689 2023-07-20 12:13:37.827820 seagoat-0.5.4/seagoat/repository.py
--rw-r--r--   0        0        0     2021 2023-07-20 12:13:37.827820 seagoat-0.5.4/seagoat/result.py
--rw-r--r--   0        0        0     5624 2023-07-20 12:13:37.827820 seagoat-0.5.4/seagoat/server.py
--rw-r--r--   0        0        0     1878 2023-07-20 12:13:37.827820 seagoat-0.5.4/seagoat/sources/chroma.py
--rw-r--r--   0        0        0     1210 2023-07-20 12:13:37.827820 seagoat-0.5.4/seagoat/sources/ripgrep.py
--rw-r--r--   0        0        0     1972 1970-01-01 00:00:00.000000 seagoat-0.5.4/PKG-INFO
+-rw-r--r--   0        0        0     1070 2023-07-23 11:33:18.356000 seagoat-0.5.5/LICENSE
+-rw-r--r--   0        0        0      957 2023-07-23 11:33:18.356000 seagoat-0.5.5/README.md
+-rw-r--r--   0        0        0     3028 2023-07-23 11:33:19.340005 seagoat-0.5.5/pyproject.toml
+-rw-r--r--   0        0        0       22 2023-07-23 11:33:18.360000 seagoat-0.5.5/seagoat/__init__.py
+-rw-r--r--   0        0        0     1601 2023-07-23 11:33:18.360000 seagoat-0.5.5/seagoat/cache.py
+-rw-r--r--   0        0        0     2859 2023-07-23 11:33:18.360000 seagoat-0.5.5/seagoat/cli.py
+-rw-r--r--   0        0        0      196 2023-07-23 11:33:18.360000 seagoat-0.5.5/seagoat/common.py
+-rw-r--r--   0        0        0     4512 2023-07-23 11:33:18.360000 seagoat-0.5.5/seagoat/engine.py
+-rw-r--r--   0        0        0     3492 2023-07-23 11:33:18.360000 seagoat-0.5.5/seagoat/file.py
+-rw-r--r--   0        0        0     2689 2023-07-23 11:33:18.360000 seagoat-0.5.5/seagoat/repository.py
+-rw-r--r--   0        0        0     2021 2023-07-23 11:33:18.360000 seagoat-0.5.5/seagoat/result.py
+-rw-r--r--   0        0        0     5624 2023-07-23 11:33:18.360000 seagoat-0.5.5/seagoat/server.py
+-rw-r--r--   0        0        0     1878 2023-07-23 11:33:18.360000 seagoat-0.5.5/seagoat/sources/chroma.py
+-rw-r--r--   0        0        0     1210 2023-07-23 11:33:18.360000 seagoat-0.5.5/seagoat/sources/ripgrep.py
+-rw-r--r--   0        0        0     1972 1970-01-01 00:00:00.000000 seagoat-0.5.5/PKG-INFO
```

### Comparing `seagoat-0.5.4/LICENSE` & `seagoat-0.5.5/LICENSE`

 * *Files identical despite different names*

### Comparing `seagoat-0.5.4/README.md` & `seagoat-0.5.5/README.md`

 * *Files identical despite different names*

### Comparing `seagoat-0.5.4/pyproject.toml` & `seagoat-0.5.5/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "seagoat"
-version = "0.5.4"
+version = "0.5.5"
 description = "A semantic-code search engine"
 authors = ["Daniel Kantor <git@daniel-kantor.com>"]
 readme = "README.md"
 license = "MIT"
 
 [tool.poetry.scripts]
 gt = "seagoat.cli:seagoat"
```

### Comparing `seagoat-0.5.4/seagoat/cache.py` & `seagoat-0.5.5/seagoat/cache.py`

 * *Files identical despite different names*

### Comparing `seagoat-0.5.4/seagoat/cli.py` & `seagoat-0.5.5/seagoat/cli.py`

 * *Files 4% similar despite different names*

```diff
@@ -49,15 +49,18 @@
 def print_result_line(result, line, color_enabled):
     if color_enabled:
         highlighted_lines = get_highlighted_lines(str(result["full_path"]))
         print(
             f"{result['path']}:{click.style(str(line), bold=True)}:{highlighted_lines[line - 1]}"
         )
     else:
-        print(f"{result['path']}:{line}:{result['line_texts'][line - 1]}")
+        for line_content in result["lines"]:
+            if line_content["line"] == line:
+                print(f"{result['path']}:{line}:{line_content['line_text']}")
+                break
 
 
 @click.command()
 @click.argument("query")
 @click.argument("repo_path", required=False, default=os.getcwd())
 @click.option(
     "--no-color",
```

### Comparing `seagoat-0.5.4/seagoat/engine.py` & `seagoat-0.5.5/seagoat/engine.py`

 * *Files identical despite different names*

### Comparing `seagoat-0.5.4/seagoat/file.py` & `seagoat-0.5.5/seagoat/file.py`

 * *Files identical despite different names*

### Comparing `seagoat-0.5.4/seagoat/repository.py` & `seagoat-0.5.5/seagoat/repository.py`

 * *Files identical despite different names*

### Comparing `seagoat-0.5.4/seagoat/result.py` & `seagoat-0.5.5/seagoat/result.py`

 * *Files identical despite different names*

### Comparing `seagoat-0.5.4/seagoat/server.py` & `seagoat-0.5.5/seagoat/server.py`

 * *Files identical despite different names*

### Comparing `seagoat-0.5.4/seagoat/sources/chroma.py` & `seagoat-0.5.5/seagoat/sources/chroma.py`

 * *Files identical despite different names*

### Comparing `seagoat-0.5.4/seagoat/sources/ripgrep.py` & `seagoat-0.5.5/seagoat/sources/ripgrep.py`

 * *Files identical despite different names*

### Comparing `seagoat-0.5.4/PKG-INFO` & `seagoat-0.5.5/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: seagoat
-Version: 0.5.4
+Version: 0.5.5
 Summary: A semantic-code search engine
 License: MIT
 Author: Daniel Kantor
 Author-email: git@daniel-kantor.com
 Requires-Python: >=3.10,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
```

