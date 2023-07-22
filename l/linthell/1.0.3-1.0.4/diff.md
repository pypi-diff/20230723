# Comparing `tmp/linthell-1.0.3.tar.gz` & `tmp/linthell-1.0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "linthell-1.0.3.tar", max compression
+gzip compressed data, was "linthell-1.0.4.tar", max compression
```

## Comparing `linthell-1.0.3.tar` & `linthell-1.0.4.tar`

### file list

```diff
@@ -1,18 +1,18 @@
--rw-r--r--   0        0        0      146 2023-01-15 15:54:26.327833 linthell-1.0.3/linthell/__init__.py
--rw-r--r--   0        0        0      146 2023-01-15 15:54:26.327833 linthell-1.0.3/linthell/__main__.py
--rw-r--r--   0        0        0     2252 2023-01-15 15:54:26.328832 linthell-1.0.3/linthell/cli.py
--rw-r--r--   0        0        0       21 2023-01-15 15:54:26.328832 linthell-1.0.3/linthell/commands/__init__.py
--rw-r--r--   0        0        0     1220 2023-01-15 15:54:26.329839 linthell-1.0.3/linthell/commands/baseline.py
--rw-r--r--   0        0        0     2370 2023-01-15 15:54:26.329839 linthell-1.0.3/linthell/commands/lint.py
--rw-r--r--   0        0        0       51 2023-01-15 15:54:26.330832 linthell-1.0.3/linthell/commands/pre_commit/__init__.py
--rw-r--r--   0        0        0     1995 2023-01-15 15:54:26.330832 linthell-1.0.3/linthell/commands/pre_commit/baseline.py
--rw-r--r--   0        0        0      378 2023-01-15 15:54:26.330832 linthell-1.0.3/linthell/commands/pre_commit/cli.py
--rw-r--r--   0        0        0     2881 2023-01-15 15:54:26.330832 linthell-1.0.3/linthell/commands/pre_commit/lint.py
--rw-r--r--   0        0        0       18 2023-01-15 15:54:26.331831 linthell-1.0.3/linthell/utils/__init__.py
--rw-r--r--   0        0        0     1752 2023-01-15 15:54:26.331831 linthell-1.0.3/linthell/utils/config.py
--rw-r--r--   0        0        0     1179 2023-07-13 21:17:16.393275 linthell-1.0.3/linthell/utils/id_lines.py
--rw-r--r--   0        0        0      708 2023-07-13 21:17:16.393275 linthell-1.0.3/linthell/utils/linters.py
--rw-r--r--   0        0        0     1109 2023-01-15 15:54:26.332835 linthell-1.0.3/linthell/utils/pre_commit.py
--rw-r--r--   0        0        0      961 2023-07-14 20:59:40.846598 linthell-1.0.3/pyproject.toml
--rw-r--r--   0        0        0     3772 2023-01-15 15:54:26.326833 linthell-1.0.3/README.md
--rw-r--r--   0        0        0     4447 1970-01-01 00:00:00.000000 linthell-1.0.3/PKG-INFO
+-rw-r--r--   0        0        0     3772 2023-07-22 22:53:22.127958 linthell-1.0.4/README.md
+-rw-r--r--   0        0        0      146 2023-07-22 22:53:22.127958 linthell-1.0.4/linthell/__init__.py
+-rw-r--r--   0        0        0      146 2023-07-22 22:53:22.127958 linthell-1.0.4/linthell/__main__.py
+-rw-r--r--   0        0        0     2252 2023-07-22 22:53:22.127958 linthell-1.0.4/linthell/cli.py
+-rw-r--r--   0        0        0       21 2023-07-22 22:53:22.127958 linthell-1.0.4/linthell/commands/__init__.py
+-rw-r--r--   0        0        0     1220 2023-07-22 22:53:22.127958 linthell-1.0.4/linthell/commands/baseline.py
+-rw-r--r--   0        0        0     2370 2023-07-22 22:53:22.127958 linthell-1.0.4/linthell/commands/lint.py
+-rw-r--r--   0        0        0       51 2023-07-22 22:53:22.127958 linthell-1.0.4/linthell/commands/pre_commit/__init__.py
+-rw-r--r--   0        0        0     1995 2023-07-22 22:53:22.127958 linthell-1.0.4/linthell/commands/pre_commit/baseline.py
+-rw-r--r--   0        0        0      378 2023-07-22 22:53:22.127958 linthell-1.0.4/linthell/commands/pre_commit/cli.py
+-rw-r--r--   0        0        0     2881 2023-07-22 22:53:22.127958 linthell-1.0.4/linthell/commands/pre_commit/lint.py
+-rw-r--r--   0        0        0       18 2023-07-22 22:53:22.127958 linthell-1.0.4/linthell/utils/__init__.py
+-rw-r--r--   0        0        0     1752 2023-07-22 22:53:22.127958 linthell-1.0.4/linthell/utils/config.py
+-rw-r--r--   0        0        0     1195 2023-07-22 22:53:22.127958 linthell-1.0.4/linthell/utils/id_lines.py
+-rw-r--r--   0        0        0      708 2023-07-22 22:53:22.127958 linthell-1.0.4/linthell/utils/linters.py
+-rw-r--r--   0        0        0     1109 2023-07-22 22:53:22.127958 linthell-1.0.4/linthell/utils/pre_commit.py
+-rw-r--r--   0        0        0      961 2023-07-22 22:53:22.127958 linthell-1.0.4/pyproject.toml
+-rw-r--r--   0        0        0     4447 1970-01-01 00:00:00.000000 linthell-1.0.4/PKG-INFO
```

### Comparing `linthell-1.0.3/linthell/cli.py` & `linthell-1.0.4/linthell/cli.py`

 * *Files identical despite different names*

### Comparing `linthell-1.0.3/linthell/commands/baseline.py` & `linthell-1.0.4/linthell/commands/baseline.py`

 * *Files identical despite different names*

### Comparing `linthell-1.0.3/linthell/commands/lint.py` & `linthell-1.0.4/linthell/commands/lint.py`

 * *Files identical despite different names*

### Comparing `linthell-1.0.3/linthell/commands/pre_commit/baseline.py` & `linthell-1.0.4/linthell/commands/pre_commit/baseline.py`

 * *Files identical despite different names*

### Comparing `linthell-1.0.3/linthell/commands/pre_commit/lint.py` & `linthell-1.0.4/linthell/commands/pre_commit/lint.py`

 * *Files identical despite different names*

### Comparing `linthell-1.0.3/linthell/utils/config.py` & `linthell-1.0.4/linthell/utils/config.py`

 * *Files identical despite different names*

### Comparing `linthell-1.0.3/linthell/utils/id_lines.py` & `linthell-1.0.4/linthell/utils/id_lines.py`

 * *Files 1% similar despite different names*

```diff
@@ -11,15 +11,16 @@
     code = ''
     if line:
         lines = Path(path).read_text().splitlines()
         if lines:
             try:
                 code = lines[int(line) - 1]
             except IndexError:
-                code = lines[-1]  # https://github.com/discrimy/linthell/issues/2
+                # https://github.com/discrimy/linthell/issues/2
+                code = lines[-1]
     normalized_path = Path(path).as_posix()
     return f'{normalized_path}:{code}:{message}'
 
 
 def get_id_lines(lint_output: str, regex: str) -> List[str]:
     """Search id lines from lint output via provided regex."""
     return [
```

### Comparing `linthell-1.0.3/linthell/utils/linters.py` & `linthell-1.0.4/linthell/utils/linters.py`

 * *Files identical despite different names*

### Comparing `linthell-1.0.3/linthell/utils/pre_commit.py` & `linthell-1.0.4/linthell/utils/pre_commit.py`

 * *Files identical despite different names*

### Comparing `linthell-1.0.3/pyproject.toml` & `linthell-1.0.4/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "linthell"
-version = "1.0.3"
+version = "1.0.4"
 description = "Universal flakehell replacement for almost any linter you like"
 authors = ["Alexander Bespalov <discrimy.off@gmail.com>"]
 readme = "README.md"
 homepage = "https://gitea.discrimy.ru/discrimy/linthell"
 repository = "https://gitea.discrimy.ru/discrimy/linthell"
 
 [tool.poetry.scripts]
```

### Comparing `linthell-1.0.3/README.md` & `linthell-1.0.4/README.md`

 * *Files identical despite different names*

### Comparing `linthell-1.0.3/PKG-INFO` & `linthell-1.0.4/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: linthell
-Version: 1.0.3
+Version: 1.0.4
 Summary: Universal flakehell replacement for almost any linter you like
 Home-page: https://gitea.discrimy.ru/discrimy/linthell
 Author: Alexander Bespalov
 Author-email: discrimy.off@gmail.com
 Requires-Python: >=3.7,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.7
```

