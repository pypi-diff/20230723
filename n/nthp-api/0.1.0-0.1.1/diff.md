# Comparing `tmp/nthp_api-0.1.0.tar.gz` & `tmp/nthp_api-0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "nthp_api-0.1.0.tar", max compression
+gzip compressed data, was "nthp_api-0.1.1.tar", max compression
```

## Comparing `nthp_api-0.1.0.tar` & `nthp_api-0.1.1.tar`

### file list

```diff
@@ -1,34 +1,34 @@
--rw-r--r--   0        0        0        0 2023-07-22 21:18:36.830335 nthp_api-0.1.0/nthp_api/__init__.py
--rw-r--r--   0        0        0     2009 2023-07-22 23:25:03.364745 nthp_api-0.1.0/nthp_api/cli/__init__.py
--rw-r--r--   0        0        0      386 2023-07-22 23:19:37.865743 nthp_api-0.1.0/nthp_api/cli/logs.py
--rw-r--r--   0        0        0        0 2023-07-22 21:18:36.830335 nthp_api-0.1.0/nthp_api/nthp_build/__init__.py
--rw-r--r--   0        0        0     7378 2023-07-22 21:18:36.830335 nthp_api-0.1.0/nthp_api/nthp_build/assets.py
--rw-r--r--   0        0        0      523 2023-07-22 23:19:29.737534 nthp_api-0.1.0/nthp_api/nthp_build/config.py
--rw-r--r--   0        0        0     1103 2023-07-22 21:18:36.830335 nthp_api-0.1.0/nthp_api/nthp_build/content.py
--rw-r--r--   0        0        0     3996 2023-07-22 21:18:36.830335 nthp_api-0.1.0/nthp_api/nthp_build/database.py
--rw-r--r--   0        0        0     1427 2023-07-22 23:27:42.751459 nthp_api-0.1.0/nthp_api/nthp_build/documents.py
--rw-r--r--   0        0        0    12110 2023-07-22 21:18:36.830335 nthp_api-0.1.0/nthp_api/nthp_build/dumper.py
--rw-r--r--   0        0        0      461 2023-07-22 21:18:36.830335 nthp_api-0.1.0/nthp_api/nthp_build/history.py
--rw-r--r--   0        0        0     7687 2023-07-22 23:11:37.068447 nthp_api-0.1.0/nthp_api/nthp_build/loader.py
--rw-r--r--   0        0        0     4694 2023-07-22 21:18:36.830335 nthp_api-0.1.0/nthp_api/nthp_build/models.py
--rw-r--r--   0        0        0     1124 2023-07-22 21:18:36.830335 nthp_api-0.1.0/nthp_api/nthp_build/parallel.py
--rw-r--r--   0        0        0     7912 2023-07-22 21:18:36.830335 nthp_api-0.1.0/nthp_api/nthp_build/people.py
--rw-r--r--   0        0        0     3826 2023-07-22 21:18:36.834335 nthp_api-0.1.0/nthp_api/nthp_build/playwrights.py
--rw-r--r--   0        0        0     6388 2023-07-22 21:18:36.834335 nthp_api-0.1.0/nthp_api/nthp_build/roles.py
--rw-r--r--   0        0        0     9700 2023-07-22 21:18:36.834335 nthp_api-0.1.0/nthp_api/nthp_build/schema.py
--rw-r--r--   0        0        0      416 2023-07-22 21:18:36.834335 nthp_api-0.1.0/nthp_api/nthp_build/search.py
--rw-r--r--   0        0        0     6446 2023-07-22 21:18:36.834335 nthp_api-0.1.0/nthp_api/nthp_build/shows.py
--rw-r--r--   0        0        0     1098 2023-07-22 21:18:36.834335 nthp_api-0.1.0/nthp_api/nthp_build/smugmug.py
--rw-r--r--   0        0        0     9559 2023-07-22 21:18:36.834335 nthp_api-0.1.0/nthp_api/nthp_build/spec.py
--rw-r--r--   0        0        0     1940 2023-07-22 21:18:36.834335 nthp_api-0.1.0/nthp_api/nthp_build/trivia.py
--rw-r--r--   0        0        0     2117 2023-07-22 21:18:36.834335 nthp_api-0.1.0/nthp_api/nthp_build/venues.py
--rw-r--r--   0        0        0     1168 2023-07-22 21:18:36.834335 nthp_api-0.1.0/nthp_api/nthp_build/years.py
--rw-r--r--   0        0        0      305 2023-07-22 21:18:36.834335 nthp_api-0.1.0/nthp_api/smugmugger/__init__.py
--rw-r--r--   0        0        0      649 2023-07-22 21:18:36.834335 nthp_api-0.1.0/nthp_api/smugmugger/album.py
--rw-r--r--   0        0        0     2583 2023-07-22 21:18:36.834335 nthp_api-0.1.0/nthp_api/smugmugger/client.py
--rw-r--r--   0        0        0      358 2023-07-22 21:18:36.834335 nthp_api-0.1.0/nthp_api/smugmugger/config.py
--rw-r--r--   0        0        0      661 2023-07-22 21:18:36.834335 nthp_api-0.1.0/nthp_api/smugmugger/database.py
--rw-r--r--   0        0        0     1134 2023-07-22 21:18:36.834335 nthp_api-0.1.0/nthp_api/smugmugger/schema.py
--rw-r--r--   0        0        0     2019 2023-07-22 21:18:36.834335 nthp_api-0.1.0/nthp_api/smugmugger/smugmug.py
--rw-r--r--   0        0        0     1857 2023-07-22 21:18:36.834335 nthp_api-0.1.0/pyproject.toml
--rw-r--r--   0        0        0      827 1970-01-01 00:00:00.000000 nthp_api-0.1.0/PKG-INFO
+-rw-r--r--   0        0        0        0 2023-07-22 21:18:36.830335 nthp_api-0.1.1/nthp_api/__init__.py
+-rw-r--r--   0        0        0     2009 2023-07-22 23:25:03.364745 nthp_api-0.1.1/nthp_api/cli/__init__.py
+-rw-r--r--   0        0        0      386 2023-07-22 23:19:37.865743 nthp_api-0.1.1/nthp_api/cli/logs.py
+-rw-r--r--   0        0        0        0 2023-07-22 21:18:36.830335 nthp_api-0.1.1/nthp_api/nthp_build/__init__.py
+-rw-r--r--   0        0        0     7378 2023-07-22 21:18:36.830335 nthp_api-0.1.1/nthp_api/nthp_build/assets.py
+-rw-r--r--   0        0        0      523 2023-07-22 23:19:29.737534 nthp_api-0.1.1/nthp_api/nthp_build/config.py
+-rw-r--r--   0        0        0     1103 2023-07-22 21:18:36.830335 nthp_api-0.1.1/nthp_api/nthp_build/content.py
+-rw-r--r--   0        0        0     3996 2023-07-22 21:18:36.830335 nthp_api-0.1.1/nthp_api/nthp_build/database.py
+-rw-r--r--   0        0        0     1427 2023-07-22 23:27:42.751459 nthp_api-0.1.1/nthp_api/nthp_build/documents.py
+-rw-r--r--   0        0        0    12110 2023-07-22 21:18:36.830335 nthp_api-0.1.1/nthp_api/nthp_build/dumper.py
+-rw-r--r--   0        0        0      461 2023-07-22 21:18:36.830335 nthp_api-0.1.1/nthp_api/nthp_build/history.py
+-rw-r--r--   0        0        0     7687 2023-07-22 23:11:37.068447 nthp_api-0.1.1/nthp_api/nthp_build/loader.py
+-rw-r--r--   0        0        0     4694 2023-07-22 21:18:36.830335 nthp_api-0.1.1/nthp_api/nthp_build/models.py
+-rw-r--r--   0        0        0     1124 2023-07-22 21:18:36.830335 nthp_api-0.1.1/nthp_api/nthp_build/parallel.py
+-rw-r--r--   0        0        0     7912 2023-07-22 21:18:36.830335 nthp_api-0.1.1/nthp_api/nthp_build/people.py
+-rw-r--r--   0        0        0     3826 2023-07-22 21:18:36.834335 nthp_api-0.1.1/nthp_api/nthp_build/playwrights.py
+-rw-r--r--   0        0        0     6388 2023-07-22 21:18:36.834335 nthp_api-0.1.1/nthp_api/nthp_build/roles.py
+-rw-r--r--   0        0        0     9700 2023-07-22 21:18:36.834335 nthp_api-0.1.1/nthp_api/nthp_build/schema.py
+-rw-r--r--   0        0        0      416 2023-07-22 21:18:36.834335 nthp_api-0.1.1/nthp_api/nthp_build/search.py
+-rw-r--r--   0        0        0     6446 2023-07-22 21:18:36.834335 nthp_api-0.1.1/nthp_api/nthp_build/shows.py
+-rw-r--r--   0        0        0     1098 2023-07-22 21:18:36.834335 nthp_api-0.1.1/nthp_api/nthp_build/smugmug.py
+-rw-r--r--   0        0        0     9559 2023-07-22 21:18:36.834335 nthp_api-0.1.1/nthp_api/nthp_build/spec.py
+-rw-r--r--   0        0        0     1940 2023-07-22 21:18:36.834335 nthp_api-0.1.1/nthp_api/nthp_build/trivia.py
+-rw-r--r--   0        0        0     2117 2023-07-22 21:18:36.834335 nthp_api-0.1.1/nthp_api/nthp_build/venues.py
+-rw-r--r--   0        0        0     1168 2023-07-22 21:18:36.834335 nthp_api-0.1.1/nthp_api/nthp_build/years.py
+-rw-r--r--   0        0        0      305 2023-07-22 21:18:36.834335 nthp_api-0.1.1/nthp_api/smugmugger/__init__.py
+-rw-r--r--   0        0        0      649 2023-07-22 21:18:36.834335 nthp_api-0.1.1/nthp_api/smugmugger/album.py
+-rw-r--r--   0        0        0     2583 2023-07-22 21:18:36.834335 nthp_api-0.1.1/nthp_api/smugmugger/client.py
+-rw-r--r--   0        0        0      358 2023-07-22 21:18:36.834335 nthp_api-0.1.1/nthp_api/smugmugger/config.py
+-rw-r--r--   0        0        0      661 2023-07-22 21:18:36.834335 nthp_api-0.1.1/nthp_api/smugmugger/database.py
+-rw-r--r--   0        0        0     1134 2023-07-22 21:18:36.834335 nthp_api-0.1.1/nthp_api/smugmugger/schema.py
+-rw-r--r--   0        0        0     2019 2023-07-22 21:18:36.834335 nthp_api-0.1.1/nthp_api/smugmugger/smugmug.py
+-rw-r--r--   0        0        0     1887 2023-07-22 23:36:46.538872 nthp_api-0.1.1/pyproject.toml
+-rw-r--r--   0        0        0      827 1970-01-01 00:00:00.000000 nthp_api-0.1.1/PKG-INFO
```

### Comparing `nthp_api-0.1.0/nthp_api/cli/__init__.py` & `nthp_api-0.1.1/nthp_api/cli/__init__.py`

 * *Files identical despite different names*

### Comparing `nthp_api-0.1.0/nthp_api/nthp_build/assets.py` & `nthp_api-0.1.1/nthp_api/nthp_build/assets.py`

 * *Files identical despite different names*

### Comparing `nthp_api-0.1.0/nthp_api/nthp_build/config.py` & `nthp_api-0.1.1/nthp_api/nthp_build/config.py`

 * *Files identical despite different names*

### Comparing `nthp_api-0.1.0/nthp_api/nthp_build/content.py` & `nthp_api-0.1.1/nthp_api/nthp_build/content.py`

 * *Files identical despite different names*

### Comparing `nthp_api-0.1.0/nthp_api/nthp_build/database.py` & `nthp_api-0.1.1/nthp_api/nthp_build/database.py`

 * *Files identical despite different names*

### Comparing `nthp_api-0.1.0/nthp_api/nthp_build/documents.py` & `nthp_api-0.1.1/nthp_api/nthp_build/documents.py`

 * *Files identical despite different names*

### Comparing `nthp_api-0.1.0/nthp_api/nthp_build/dumper.py` & `nthp_api-0.1.1/nthp_api/nthp_build/dumper.py`

 * *Files identical despite different names*

### Comparing `nthp_api-0.1.0/nthp_api/nthp_build/loader.py` & `nthp_api-0.1.1/nthp_api/nthp_build/loader.py`

 * *Files identical despite different names*

### Comparing `nthp_api-0.1.0/nthp_api/nthp_build/models.py` & `nthp_api-0.1.1/nthp_api/nthp_build/models.py`

 * *Files identical despite different names*

### Comparing `nthp_api-0.1.0/nthp_api/nthp_build/parallel.py` & `nthp_api-0.1.1/nthp_api/nthp_build/parallel.py`

 * *Files identical despite different names*

### Comparing `nthp_api-0.1.0/nthp_api/nthp_build/people.py` & `nthp_api-0.1.1/nthp_api/nthp_build/people.py`

 * *Files identical despite different names*

### Comparing `nthp_api-0.1.0/nthp_api/nthp_build/playwrights.py` & `nthp_api-0.1.1/nthp_api/nthp_build/playwrights.py`

 * *Files identical despite different names*

### Comparing `nthp_api-0.1.0/nthp_api/nthp_build/roles.py` & `nthp_api-0.1.1/nthp_api/nthp_build/roles.py`

 * *Files identical despite different names*

### Comparing `nthp_api-0.1.0/nthp_api/nthp_build/schema.py` & `nthp_api-0.1.1/nthp_api/nthp_build/schema.py`

 * *Files identical despite different names*

### Comparing `nthp_api-0.1.0/nthp_api/nthp_build/shows.py` & `nthp_api-0.1.1/nthp_api/nthp_build/shows.py`

 * *Files identical despite different names*

### Comparing `nthp_api-0.1.0/nthp_api/nthp_build/smugmug.py` & `nthp_api-0.1.1/nthp_api/nthp_build/smugmug.py`

 * *Files identical despite different names*

### Comparing `nthp_api-0.1.0/nthp_api/nthp_build/spec.py` & `nthp_api-0.1.1/nthp_api/nthp_build/spec.py`

 * *Files identical despite different names*

### Comparing `nthp_api-0.1.0/nthp_api/nthp_build/trivia.py` & `nthp_api-0.1.1/nthp_api/nthp_build/trivia.py`

 * *Files identical despite different names*

### Comparing `nthp_api-0.1.0/nthp_api/nthp_build/venues.py` & `nthp_api-0.1.1/nthp_api/nthp_build/venues.py`

 * *Files identical despite different names*

### Comparing `nthp_api-0.1.0/nthp_api/nthp_build/years.py` & `nthp_api-0.1.1/nthp_api/nthp_build/years.py`

 * *Files identical despite different names*

### Comparing `nthp_api-0.1.0/nthp_api/smugmugger/album.py` & `nthp_api-0.1.1/nthp_api/smugmugger/album.py`

 * *Files identical despite different names*

### Comparing `nthp_api-0.1.0/nthp_api/smugmugger/client.py` & `nthp_api-0.1.1/nthp_api/smugmugger/client.py`

 * *Files identical despite different names*

### Comparing `nthp_api-0.1.0/nthp_api/smugmugger/database.py` & `nthp_api-0.1.1/nthp_api/smugmugger/database.py`

 * *Files identical despite different names*

### Comparing `nthp_api-0.1.0/nthp_api/smugmugger/schema.py` & `nthp_api-0.1.1/nthp_api/smugmugger/schema.py`

 * *Files identical despite different names*

### Comparing `nthp_api-0.1.0/nthp_api/smugmugger/smugmug.py` & `nthp_api-0.1.1/nthp_api/smugmugger/smugmug.py`

 * *Files identical despite different names*

### Comparing `nthp_api-0.1.0/pyproject.toml` & `nthp_api-0.1.1/pyproject.toml`

 * *Files 16% similar despite different names*

```diff
@@ -1,16 +1,17 @@
 [tool.poetry]
 name = "nthp_api"
-version = "0.1.0"
+version = "0.1.1"
 description = ""
 authors = ["Will Pimblett <will@wjdp.uk>"]
 license = "MIT"
 
 [tool.poetry.scripts]
 nthp = "nthp_api.cli:cli"
+nthp_api = "nthp_api.cli:cli"
 
 [tool.poetry.dependencies]
 python = "^3.10"
 pydantic = "^1.10.7"
 python-frontmatter = "^1.0.0"
 peewee = "^3.16.2"
 python-slugify = "^8.0.1"
```

### Comparing `nthp_api-0.1.0/PKG-INFO` & `nthp_api-0.1.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: nthp-api
-Version: 0.1.0
+Version: 0.1.1
 Summary: 
 License: MIT
 Author: Will Pimblett
 Author-email: will@wjdp.uk
 Requires-Python: >=3.10,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
```

