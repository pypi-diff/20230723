# Comparing `tmp/mdgpt-0.1.0.tar.gz` & `tmp/mdgpt-0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "mdgpt-0.1.0.tar", max compression
+gzip compressed data, was "mdgpt-0.1.1.tar", max compression
```

## Comparing `mdgpt-0.1.0.tar` & `mdgpt-0.1.1.tar`

### file list

```diff
@@ -1,9 +1,9 @@
--rw-r--r--   0        0        0     1064 2023-07-18 20:46:07.614765 mdgpt-0.1.0/LICENSE
--rw-r--r--   0        0        0      274 2023-07-22 23:02:13.763187 mdgpt-0.1.0/mdgpt/__init__.py
--rw-r--r--   0        0        0     2852 2023-07-23 10:43:22.221126 mdgpt-0.1.0/mdgpt/build.py
--rw-r--r--   0        0        0      502 2023-07-22 23:00:37.776738 mdgpt-0.1.0/mdgpt/misc.py
--rw-r--r--   0        0        0     8884 2023-07-23 10:55:28.885589 mdgpt-0.1.0/mdgpt/translate.py
--rw-r--r--   0        0        0     2479 2023-07-22 23:01:02.240963 mdgpt-0.1.0/mdgpt/utils.py
--rw-r--r--   0        0        0      735 2023-07-22 23:03:36.636114 mdgpt-0.1.0/pyproject.toml
--rw-r--r--   0        0        0     1002 2023-07-23 11:01:20.930821 mdgpt-0.1.0/setup.py
--rw-r--r--   0        0        0      634 2023-07-23 11:01:20.931083 mdgpt-0.1.0/PKG-INFO
+-rw-r--r--   0        0        0     1064 2023-07-18 20:46:07.614765 mdgpt-0.1.1/LICENSE
+-rw-r--r--   0        0        0      274 2023-07-22 23:02:13.763187 mdgpt-0.1.1/mdgpt/__init__.py
+-rw-r--r--   0        0        0     2852 2023-07-23 10:43:22.221126 mdgpt-0.1.1/mdgpt/build.py
+-rw-r--r--   0        0        0      502 2023-07-22 23:00:37.776738 mdgpt-0.1.1/mdgpt/misc.py
+-rw-r--r--   0        0        0     8884 2023-07-23 10:55:28.885589 mdgpt-0.1.1/mdgpt/translate.py
+-rw-r--r--   0        0        0     2479 2023-07-22 23:01:02.240963 mdgpt-0.1.1/mdgpt/utils.py
+-rw-r--r--   0        0        0      735 2023-07-23 20:41:52.004138 mdgpt-0.1.1/pyproject.toml
+-rw-r--r--   0        0        0     1002 2023-07-23 20:41:56.179154 mdgpt-0.1.1/setup.py
+-rw-r--r--   0        0        0      634 2023-07-23 20:41:56.179427 mdgpt-0.1.1/PKG-INFO
```

### Comparing `mdgpt-0.1.0/LICENSE` & `mdgpt-0.1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `mdgpt-0.1.0/mdgpt/build.py` & `mdgpt-0.1.1/mdgpt/build.py`

 * *Files identical despite different names*

### Comparing `mdgpt-0.1.0/mdgpt/translate.py` & `mdgpt-0.1.1/mdgpt/translate.py`

 * *Files identical despite different names*

### Comparing `mdgpt-0.1.0/mdgpt/utils.py` & `mdgpt-0.1.1/mdgpt/utils.py`

 * *Files identical despite different names*

### Comparing `mdgpt-0.1.0/pyproject.toml` & `mdgpt-0.1.1/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -8,15 +8,15 @@
   | dist
   | venv
 )/
 '''
 
 [tool.poetry]
 name = "mdgpt"
-version = "0.1.0"
+version = "0.1.1"
 description = "Translate and generate static site from Markdown files using ChatGTP"
 authors = ["Jeppe Bårris <jeppe@barris.dk>"]
 license = "MIT"
 
 [tool.poetry.dependencies]
 python = "^3.10"
 python-frontmatter = "^1.0.0"
```

### Comparing `mdgpt-0.1.0/setup.py` & `mdgpt-0.1.1/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -18,15 +18,15 @@
 entry_points = \
 {'console_scripts': ['mdbuild = mdgpt:build',
                      'mdengines = mdgpt:engines',
                      'mdtranslate = mdgpt:translate']}
 
 setup_kwargs = {
     'name': 'mdgpt',
-    'version': '0.1.0',
+    'version': '0.1.1',
     'description': 'Translate and generate static site from Markdown files using ChatGTP',
     'long_description': None,
     'author': 'Jeppe Bårris',
     'author_email': 'jeppe@barris.dk',
     'maintainer': None,
     'maintainer_email': None,
     'url': None,
```

### Comparing `mdgpt-0.1.0/PKG-INFO` & `mdgpt-0.1.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: mdgpt
-Version: 0.1.0
+Version: 0.1.1
 Summary: Translate and generate static site from Markdown files using ChatGTP
 License: MIT
 Author: Jeppe Bårris
 Author-email: jeppe@barris.dk
 Requires-Python: >=3.10,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
```

