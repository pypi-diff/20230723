# Comparing `tmp/comex-0.1.4.tar.gz` & `tmp/comex-0.1.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "comex-0.1.4.tar", last modified: Tue Jul 11 12:51:11 2023, max compression
+gzip compressed data, was "comex-0.1.5.tar", last modified: Sun Jul 23 13:07:27 2023, max compression
```

## Comparing `comex-0.1.4.tar` & `comex-0.1.5.tar`

### file list

```diff
@@ -1,58 +1,58 @@
-drwxrwxrwx   0 noble      (501) staff       (20)        0 2023-07-11 12:51:11.590000 comex-0.1.4/
--rwxrwxrwx   0 noble      (501) staff       (20)    11357 2023-05-27 09:03:42.000000 comex-0.1.4/LICENSE
--rwxrwxrwx   0 noble      (501) staff       (20)    14479 2023-07-11 12:51:11.640000 comex-0.1.4/PKG-INFO
--rwxrwxrwx   0 noble      (501) staff       (20)    13862 2023-07-11 12:00:46.000000 comex-0.1.4/README.md
--rwxrwxrwx   0 noble      (501) staff       (20)     1036 2023-07-11 12:51:11.640000 comex-0.1.4/setup.cfg
--rwxrwxrwx   0 noble      (501) staff       (20)       38 2023-06-30 03:53:49.000000 comex-0.1.4/setup.py
-drwxrwxrwx   0 noble      (501) staff       (20)        0 2023-07-11 12:51:11.590000 comex-0.1.4/src/
-drwxrwxrwx   0 noble      (501) staff       (20)        0 2023-07-11 12:51:11.590000 comex-0.1.4/src/comex/
--rwxrwxrwx   0 noble      (501) staff       (20)        0 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/__init__.py
--rwxrwxrwx   0 noble      (501) staff       (20)      104 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/__main__.py
--rwxrwxrwx   0 noble      (501) staff       (20)     3654 2023-07-08 22:33:09.000000 comex-0.1.4/src/comex/cli.py
-drwxrwxrwx   0 noble      (501) staff       (20)        0 2023-07-11 12:51:11.590000 comex-0.1.4/src/comex/codeviews/
-drwxrwxrwx   0 noble      (501) staff       (20)        0 2023-07-11 12:51:11.590000 comex-0.1.4/src/comex/codeviews/AST/
--rwxrwxrwx   0 noble      (501) staff       (20)     4196 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/codeviews/AST/AST.py
--rwxrwxrwx   0 noble      (501) staff       (20)      968 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/codeviews/AST/AST_driver.py
--rwxrwxrwx   0 noble      (501) staff       (20)        0 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/codeviews/AST/__init__.py
-drwxrwxrwx   0 noble      (501) staff       (20)        0 2023-07-11 12:51:11.590000 comex-0.1.4/src/comex/codeviews/CFG/
--rwxrwxrwx   0 noble      (501) staff       (20)     1426 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/codeviews/CFG/CFG.py
--rwxrwxrwx   0 noble      (501) staff       (20)    97324 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/codeviews/CFG/CFG_csharp.py
--rwxrwxrwx   0 noble      (501) staff       (20)     1300 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/codeviews/CFG/CFG_driver.py
--rwxrwxrwx   0 noble      (501) staff       (20)    78345 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/codeviews/CFG/CFG_java.py
--rwxrwxrwx   0 noble      (501) staff       (20)        0 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/codeviews/CFG/__init__.py
-drwxrwxrwx   0 noble      (501) staff       (20)        0 2023-07-11 12:51:11.590000 comex-0.1.4/src/comex/codeviews/CST/
--rwxrwxrwx   0 noble      (501) staff       (20)     2542 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/codeviews/CST/CST_driver.py
--rwxrwxrwx   0 noble      (501) staff       (20)        0 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/codeviews/CST/__init__.py
-drwxrwxrwx   0 noble      (501) staff       (20)        0 2023-07-11 12:51:11.590000 comex-0.1.4/src/comex/codeviews/DFG/
--rwxrwxrwx   0 noble      (501) staff       (20)     1246 2023-06-30 06:38:47.000000 comex-0.1.4/src/comex/codeviews/DFG/DFG_driver.py
--rwxrwxrwx   0 noble      (501) staff       (20)        0 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/codeviews/DFG/__init__.py
-drwxrwxrwx   0 noble      (501) staff       (20)        0 2023-07-11 12:51:11.590000 comex-0.1.4/src/comex/codeviews/SDFG/
--rwxrwxrwx   0 noble      (501) staff       (20)     4581 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/codeviews/SDFG/SDFG.py
--rwxrwxrwx   0 noble      (501) staff       (20)    57510 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/codeviews/SDFG/SDFG_csharp.py
--rwxrwxrwx   0 noble      (501) staff       (20)    61649 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/codeviews/SDFG/SDFG_java.py
--rwxrwxrwx   0 noble      (501) staff       (20)        0 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/codeviews/SDFG/__init__.py
--rwxrwxrwx   0 noble      (501) staff       (20)        0 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/codeviews/__init__.py
-drwxrwxrwx   0 noble      (501) staff       (20)        0 2023-07-11 12:51:11.590000 comex-0.1.4/src/comex/codeviews/combined_graph/
--rwxrwxrwx   0 noble      (501) staff       (20)        0 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/codeviews/combined_graph/__init__.py
--rwxrwxrwx   0 noble      (501) staff       (20)     9551 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/codeviews/combined_graph/combined_driver.py
-drwxrwxrwx   0 noble      (501) staff       (20)        0 2023-07-11 12:51:11.590000 comex-0.1.4/src/comex/tree_parser/
--rwxrwxrwx   0 noble      (501) staff       (20)        0 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/tree_parser/__init__.py
--rwxrwxrwx   0 noble      (501) staff       (20)    11275 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/tree_parser/cs_parser.py
--rwxrwxrwx   0 noble      (501) staff       (20)     6210 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/tree_parser/custom_parser.py
--rwxrwxrwx   0 noble      (501) staff       (20)    10039 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/tree_parser/java_parser.py
--rwxrwxrwx   0 noble      (501) staff       (20)     1818 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/tree_parser/parser_driver.py
-drwxrwxrwx   0 noble      (501) staff       (20)        0 2023-07-11 12:51:11.590000 comex-0.1.4/src/comex/utils/
--rwxrwxrwx   0 noble      (501) staff       (20)     1763 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/utils/DFG_utils.py
--rwxrwxrwx   0 noble      (501) staff       (20)        0 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/utils/__init__.py
--rwxrwxrwx   0 noble      (501) staff       (20)    26499 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/utils/cs_nodes.py
--rwxrwxrwx   0 noble      (501) staff       (20)    25220 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/utils/java_nodes.py
--rwxrwxrwx   0 noble      (501) staff       (20)     1134 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/utils/postprocessor.py
--rwxrwxrwx   0 noble      (501) staff       (20)     2418 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/utils/preprocessor.py
--rwxrwxrwx   0 noble      (501) staff       (20)     2055 2023-06-30 03:53:49.000000 comex-0.1.4/src/comex/utils/src_parser.py
-drwxrwxrwx   0 noble      (501) staff       (20)        0 2023-07-11 12:51:11.590000 comex-0.1.4/src/comex.egg-info/
--rwxrwxrwx   0 noble      (501) staff       (20)    14479 2023-07-11 12:51:11.000000 comex-0.1.4/src/comex.egg-info/PKG-INFO
--rwxrwxrwx   0 noble      (501) staff       (20)     1404 2023-07-11 12:51:11.000000 comex-0.1.4/src/comex.egg-info/SOURCES.txt
--rwxrwxrwx   0 noble      (501) staff       (20)        1 2023-07-11 12:51:11.000000 comex-0.1.4/src/comex.egg-info/dependency_links.txt
--rwxrwxrwx   0 noble      (501) staff       (20)       40 2023-07-11 12:51:11.000000 comex-0.1.4/src/comex.egg-info/entry_points.txt
--rwxrwxrwx   0 noble      (501) staff       (20)      151 2023-07-11 12:51:11.000000 comex-0.1.4/src/comex.egg-info/requires.txt
--rwxrwxrwx   0 noble      (501) staff       (20)        6 2023-07-11 12:51:11.000000 comex-0.1.4/src/comex.egg-info/top_level.txt
+drwxrwxrwx   0 noble      (501) staff       (20)        0 2023-07-23 13:07:27.220000 comex-0.1.5/
+-rwxrwxrwx   0 noble      (501) staff       (20)    11357 2023-05-27 09:03:42.000000 comex-0.1.5/LICENSE
+-rwxrwxrwx   0 noble      (501) staff       (20)    14479 2023-07-23 13:07:27.280000 comex-0.1.5/PKG-INFO
+-rwxrwxrwx   0 noble      (501) staff       (20)    13862 2023-07-11 12:00:46.000000 comex-0.1.5/README.md
+-rwxrwxrwx   0 noble      (501) staff       (20)     1036 2023-07-23 13:07:27.280000 comex-0.1.5/setup.cfg
+-rwxrwxrwx   0 noble      (501) staff       (20)       38 2023-06-30 03:53:49.000000 comex-0.1.5/setup.py
+drwxrwxrwx   0 noble      (501) staff       (20)        0 2023-07-23 13:07:27.220000 comex-0.1.5/src/
+drwxrwxrwx   0 noble      (501) staff       (20)        0 2023-07-23 13:07:27.220000 comex-0.1.5/src/comex/
+-rwxrwxrwx   0 noble      (501) staff       (20)     3619 2023-07-21 09:30:33.000000 comex-0.1.5/src/comex/__init__.py
+-rwxrwxrwx   0 noble      (501) staff       (20)      105 2023-07-21 09:28:05.000000 comex-0.1.5/src/comex/__main__.py
+-rwxrwxrwx   0 noble      (501) staff       (20)     3704 2023-07-21 09:28:05.000000 comex-0.1.5/src/comex/cli.py
+drwxrwxrwx   0 noble      (501) staff       (20)        0 2023-07-23 13:07:27.220000 comex-0.1.5/src/comex/codeviews/
+drwxrwxrwx   0 noble      (501) staff       (20)        0 2023-07-23 13:07:27.220000 comex-0.1.5/src/comex/codeviews/AST/
+-rwxrwxrwx   0 noble      (501) staff       (20)     4196 2023-06-30 03:53:49.000000 comex-0.1.5/src/comex/codeviews/AST/AST.py
+-rwxrwxrwx   0 noble      (501) staff       (20)      968 2023-06-30 03:53:49.000000 comex-0.1.5/src/comex/codeviews/AST/AST_driver.py
+-rwxrwxrwx   0 noble      (501) staff       (20)        0 2023-06-30 03:53:49.000000 comex-0.1.5/src/comex/codeviews/AST/__init__.py
+drwxrwxrwx   0 noble      (501) staff       (20)        0 2023-07-23 13:07:27.220000 comex-0.1.5/src/comex/codeviews/CFG/
+-rwxrwxrwx   0 noble      (501) staff       (20)     1426 2023-06-30 03:53:49.000000 comex-0.1.5/src/comex/codeviews/CFG/CFG.py
+-rwxrwxrwx   0 noble      (501) staff       (20)    97324 2023-06-30 03:53:49.000000 comex-0.1.5/src/comex/codeviews/CFG/CFG_csharp.py
+-rwxrwxrwx   0 noble      (501) staff       (20)     1300 2023-06-30 03:53:49.000000 comex-0.1.5/src/comex/codeviews/CFG/CFG_driver.py
+-rwxrwxrwx   0 noble      (501) staff       (20)    78345 2023-06-30 03:53:49.000000 comex-0.1.5/src/comex/codeviews/CFG/CFG_java.py
+-rwxrwxrwx   0 noble      (501) staff       (20)        0 2023-06-30 03:53:49.000000 comex-0.1.5/src/comex/codeviews/CFG/__init__.py
+drwxrwxrwx   0 noble      (501) staff       (20)        0 2023-07-23 13:07:27.220000 comex-0.1.5/src/comex/codeviews/CST/
+-rwxrwxrwx   0 noble      (501) staff       (20)     2542 2023-06-30 03:53:49.000000 comex-0.1.5/src/comex/codeviews/CST/CST_driver.py
+-rwxrwxrwx   0 noble      (501) staff       (20)        0 2023-06-30 03:53:49.000000 comex-0.1.5/src/comex/codeviews/CST/__init__.py
+drwxrwxrwx   0 noble      (501) staff       (20)        0 2023-07-23 13:07:27.220000 comex-0.1.5/src/comex/codeviews/DFG/
+-rwxrwxrwx   0 noble      (501) staff       (20)     1246 2023-06-30 06:38:47.000000 comex-0.1.5/src/comex/codeviews/DFG/DFG_driver.py
+-rwxrwxrwx   0 noble      (501) staff       (20)        0 2023-06-30 03:53:49.000000 comex-0.1.5/src/comex/codeviews/DFG/__init__.py
+drwxrwxrwx   0 noble      (501) staff       (20)        0 2023-07-23 13:07:27.220000 comex-0.1.5/src/comex/codeviews/SDFG/
+-rwxrwxrwx   0 noble      (501) staff       (20)     4581 2023-06-30 03:53:49.000000 comex-0.1.5/src/comex/codeviews/SDFG/SDFG.py
+-rwxrwxrwx   0 noble      (501) staff       (20)    57510 2023-06-30 03:53:49.000000 comex-0.1.5/src/comex/codeviews/SDFG/SDFG_csharp.py
+-rwxrwxrwx   0 noble      (501) staff       (20)    61649 2023-06-30 03:53:49.000000 comex-0.1.5/src/comex/codeviews/SDFG/SDFG_java.py
+-rwxrwxrwx   0 noble      (501) staff       (20)        0 2023-06-30 03:53:49.000000 comex-0.1.5/src/comex/codeviews/SDFG/__init__.py
+-rwxrwxrwx   0 noble      (501) staff       (20)        0 2023-06-30 03:53:49.000000 comex-0.1.5/src/comex/codeviews/__init__.py
+drwxrwxrwx   0 noble      (501) staff       (20)        0 2023-07-23 13:07:27.220000 comex-0.1.5/src/comex/codeviews/combined_graph/
+-rwxrwxrwx   0 noble      (501) staff       (20)        0 2023-06-30 03:53:49.000000 comex-0.1.5/src/comex/codeviews/combined_graph/__init__.py
+-rwxrwxrwx   0 noble      (501) staff       (20)     9551 2023-06-30 03:53:49.000000 comex-0.1.5/src/comex/codeviews/combined_graph/combined_driver.py
+drwxrwxrwx   0 noble      (501) staff       (20)        0 2023-07-23 13:07:27.220000 comex-0.1.5/src/comex/tree_parser/
+-rwxrwxrwx   0 noble      (501) staff       (20)        0 2023-06-30 03:53:49.000000 comex-0.1.5/src/comex/tree_parser/__init__.py
+-rwxrwxrwx   0 noble      (501) staff       (20)    11275 2023-06-30 03:53:49.000000 comex-0.1.5/src/comex/tree_parser/cs_parser.py
+-rwxrwxrwx   0 noble      (501) staff       (20)     2617 2023-07-21 09:26:14.000000 comex-0.1.5/src/comex/tree_parser/custom_parser.py
+-rwxrwxrwx   0 noble      (501) staff       (20)    10039 2023-06-30 03:53:49.000000 comex-0.1.5/src/comex/tree_parser/java_parser.py
+-rwxrwxrwx   0 noble      (501) staff       (20)     1818 2023-06-30 03:53:49.000000 comex-0.1.5/src/comex/tree_parser/parser_driver.py
+drwxrwxrwx   0 noble      (501) staff       (20)        0 2023-07-23 13:07:27.220000 comex-0.1.5/src/comex/utils/
+-rwxrwxrwx   0 noble      (501) staff       (20)     1763 2023-06-30 03:53:49.000000 comex-0.1.5/src/comex/utils/DFG_utils.py
+-rwxrwxrwx   0 noble      (501) staff       (20)        0 2023-06-30 03:53:49.000000 comex-0.1.5/src/comex/utils/__init__.py
+-rwxrwxrwx   0 noble      (501) staff       (20)    26499 2023-06-30 03:53:49.000000 comex-0.1.5/src/comex/utils/cs_nodes.py
+-rwxrwxrwx   0 noble      (501) staff       (20)    25220 2023-06-30 03:53:49.000000 comex-0.1.5/src/comex/utils/java_nodes.py
+-rwxrwxrwx   0 noble      (501) staff       (20)     1134 2023-06-30 03:53:49.000000 comex-0.1.5/src/comex/utils/postprocessor.py
+-rwxrwxrwx   0 noble      (501) staff       (20)     2418 2023-06-30 03:53:49.000000 comex-0.1.5/src/comex/utils/preprocessor.py
+-rwxrwxrwx   0 noble      (501) staff       (20)     2055 2023-06-30 03:53:49.000000 comex-0.1.5/src/comex/utils/src_parser.py
+drwxrwxrwx   0 noble      (501) staff       (20)        0 2023-07-23 13:07:27.220000 comex-0.1.5/src/comex.egg-info/
+-rwxrwxrwx   0 noble      (501) staff       (20)    14479 2023-07-23 13:07:27.000000 comex-0.1.5/src/comex.egg-info/PKG-INFO
+-rwxrwxrwx   0 noble      (501) staff       (20)     1404 2023-07-23 13:07:27.000000 comex-0.1.5/src/comex.egg-info/SOURCES.txt
+-rwxrwxrwx   0 noble      (501) staff       (20)        1 2023-07-23 13:07:27.000000 comex-0.1.5/src/comex.egg-info/dependency_links.txt
+-rwxrwxrwx   0 noble      (501) staff       (20)       40 2023-07-23 13:07:27.000000 comex-0.1.5/src/comex.egg-info/entry_points.txt
+-rwxrwxrwx   0 noble      (501) staff       (20)      151 2023-07-23 13:07:27.000000 comex-0.1.5/src/comex.egg-info/requires.txt
+-rwxrwxrwx   0 noble      (501) staff       (20)        6 2023-07-23 13:07:27.000000 comex-0.1.5/src/comex.egg-info/top_level.txt
```

### Comparing `comex-0.1.4/LICENSE` & `comex-0.1.5/LICENSE`

 * *Files identical despite different names*

### Comparing `comex-0.1.4/PKG-INFO` & `comex-0.1.5/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: comex
-Version: 0.1.4
+Version: 0.1.5
 Summary: Generate combined multi-code view graphs
 Home-page: https://github.com/IBM/tree-sitter-codeviews
 License: Apache-2.0
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3 :: Only
```

### Comparing `comex-0.1.4/README.md` & `comex-0.1.5/README.md`

 * *Files identical despite different names*

### Comparing `comex-0.1.4/setup.cfg` & `comex-0.1.5/setup.cfg`

 * *Files 19% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [metadata]
 name = comex
-version = 0.1.4
+version = 0.1.5
 description = Generate combined multi-code view graphs
 long_description = file: README.md
 long_description_content_type = text/markdown
 url = https://github.com/IBM/tree-sitter-codeviews
 license = Apache-2.0
 license_file = LICENSE
 classifiers =
```

### Comparing `comex-0.1.4/src/comex/cli.py` & `comex-0.1.5/src/comex/cli.py`

 * *Files 5% similar despite different names*

```diff
@@ -5,15 +5,17 @@
 from pathlib import Path
 from typing import Optional
 
 import typer
 from loguru import logger
 
 from .codeviews.combined_graph.combined_driver import CombinedDriver
+from . import get_language_map
 
+get_language_map()
 app = typer.Typer()
 
 
 @app.callback(invoke_without_command=True)
 def main(
         lang: str = typer.Option(..., help="java, cs"),
         code: Optional[str] = typer.Option(None, help="""
```

### Comparing `comex-0.1.4/src/comex/codeviews/AST/AST.py` & `comex-0.1.5/src/comex/codeviews/AST/AST.py`

 * *Files identical despite different names*

### Comparing `comex-0.1.4/src/comex/codeviews/AST/AST_driver.py` & `comex-0.1.5/src/comex/codeviews/AST/AST_driver.py`

 * *Files identical despite different names*

### Comparing `comex-0.1.4/src/comex/codeviews/CFG/CFG.py` & `comex-0.1.5/src/comex/codeviews/CFG/CFG.py`

 * *Files identical despite different names*

### Comparing `comex-0.1.4/src/comex/codeviews/CFG/CFG_csharp.py` & `comex-0.1.5/src/comex/codeviews/CFG/CFG_csharp.py`

 * *Files identical despite different names*

### Comparing `comex-0.1.4/src/comex/codeviews/CFG/CFG_driver.py` & `comex-0.1.5/src/comex/codeviews/CFG/CFG_driver.py`

 * *Files identical despite different names*

### Comparing `comex-0.1.4/src/comex/codeviews/CFG/CFG_java.py` & `comex-0.1.5/src/comex/codeviews/CFG/CFG_java.py`

 * *Files identical despite different names*

### Comparing `comex-0.1.4/src/comex/codeviews/CST/CST_driver.py` & `comex-0.1.5/src/comex/codeviews/CST/CST_driver.py`

 * *Files identical despite different names*

### Comparing `comex-0.1.4/src/comex/codeviews/DFG/DFG_driver.py` & `comex-0.1.5/src/comex/codeviews/DFG/DFG_driver.py`

 * *Files identical despite different names*

### Comparing `comex-0.1.4/src/comex/codeviews/SDFG/SDFG.py` & `comex-0.1.5/src/comex/codeviews/SDFG/SDFG.py`

 * *Files identical despite different names*

### Comparing `comex-0.1.4/src/comex/codeviews/SDFG/SDFG_csharp.py` & `comex-0.1.5/src/comex/codeviews/SDFG/SDFG_csharp.py`

 * *Files identical despite different names*

### Comparing `comex-0.1.4/src/comex/codeviews/SDFG/SDFG_java.py` & `comex-0.1.5/src/comex/codeviews/SDFG/SDFG_java.py`

 * *Files identical despite different names*

### Comparing `comex-0.1.4/src/comex/codeviews/combined_graph/combined_driver.py` & `comex-0.1.5/src/comex/codeviews/combined_graph/combined_driver.py`

 * *Files identical despite different names*

### Comparing `comex-0.1.4/src/comex/tree_parser/cs_parser.py` & `comex-0.1.5/src/comex/tree_parser/cs_parser.py`

 * *Files identical despite different names*

### Comparing `comex-0.1.4/src/comex/tree_parser/java_parser.py` & `comex-0.1.5/src/comex/tree_parser/java_parser.py`

 * *Files identical despite different names*

### Comparing `comex-0.1.4/src/comex/tree_parser/parser_driver.py` & `comex-0.1.5/src/comex/tree_parser/parser_driver.py`

 * *Files identical despite different names*

### Comparing `comex-0.1.4/src/comex/utils/DFG_utils.py` & `comex-0.1.5/src/comex/utils/DFG_utils.py`

 * *Files identical despite different names*

### Comparing `comex-0.1.4/src/comex/utils/cs_nodes.py` & `comex-0.1.5/src/comex/utils/cs_nodes.py`

 * *Files identical despite different names*

### Comparing `comex-0.1.4/src/comex/utils/java_nodes.py` & `comex-0.1.5/src/comex/utils/java_nodes.py`

 * *Files identical despite different names*

### Comparing `comex-0.1.4/src/comex/utils/postprocessor.py` & `comex-0.1.5/src/comex/utils/postprocessor.py`

 * *Files identical despite different names*

### Comparing `comex-0.1.4/src/comex/utils/preprocessor.py` & `comex-0.1.5/src/comex/utils/preprocessor.py`

 * *Files identical despite different names*

### Comparing `comex-0.1.4/src/comex/utils/src_parser.py` & `comex-0.1.5/src/comex/utils/src_parser.py`

 * *Files identical despite different names*

### Comparing `comex-0.1.4/src/comex.egg-info/PKG-INFO` & `comex-0.1.5/src/comex.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: comex
-Version: 0.1.4
+Version: 0.1.5
 Summary: Generate combined multi-code view graphs
 Home-page: https://github.com/IBM/tree-sitter-codeviews
 License: Apache-2.0
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3 :: Only
```

### Comparing `comex-0.1.4/src/comex.egg-info/SOURCES.txt` & `comex-0.1.5/src/comex.egg-info/SOURCES.txt`

 * *Files identical despite different names*

