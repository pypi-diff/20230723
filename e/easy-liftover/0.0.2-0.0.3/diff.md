# Comparing `tmp/easy_liftover-0.0.2.tar.gz` & `tmp/easy_liftover-0.0.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "easy_liftover-0.0.2.tar", max compression
+gzip compressed data, was "easy_liftover-0.0.3.tar", max compression
```

## Comparing `easy_liftover-0.0.2.tar` & `easy_liftover-0.0.3.tar`

### file list

```diff
@@ -1,15 +1,40 @@
--rw-r--r--   0        0        0    35149 2023-07-23 11:08:25.614800 easy_liftover-0.0.2/LICENSE
--rw-r--r--   0        0        0      459 2023-07-23 11:08:25.614800 easy_liftover-0.0.2/README.md
--rw-r--r--   0        0        0      729 2023-07-23 11:08:25.618800 easy_liftover-0.0.2/pyproject.toml
--rw-r--r--   0        0        0       67 2023-07-23 11:08:25.618800 easy_liftover-0.0.2/src/__init__.py
--rw-r--r--   0        0        0      189 2023-07-23 11:08:25.618800 easy_liftover-0.0.2/src/genomes.py
--rw-r--r--   0        0        0      117 2023-07-23 11:08:25.618800 easy_liftover-0.0.2/src/lifters/__init__.py
--rw-r--r--   0        0        0     1931 2023-07-23 11:08:25.618800 easy_liftover-0.0.2/src/lifters/abstract.py
--rw-r--r--   0        0        0      680 2023-07-23 11:08:25.618800 easy_liftover-0.0.2/src/lifters/bed.py
--rw-r--r--   0        0        0      661 2023-07-23 11:08:25.618800 easy_liftover-0.0.2/src/lifters/gff.py
--rw-r--r--   0        0        0     1825 2023-07-23 11:08:25.618800 easy_liftover-0.0.2/src/lifters/wig.py
--rw-r--r--   0        0        0      610 2023-07-23 11:08:25.618800 easy_liftover-0.0.2/src/targets.py
--rw-r--r--   0        0        0      770 2023-07-23 11:08:25.618800 easy_liftover-0.0.2/src/test_lifters.py
--rw-r--r--   0        0        0     1231 2023-07-23 11:08:25.618800 easy_liftover-0.0.2/src/types.json
--rw-r--r--   0        0        0     1223 2023-07-23 11:08:25.618800 easy_liftover-0.0.2/src/uplift.py
--rw-r--r--   0        0        0     1174 1970-01-01 00:00:00.000000 easy_liftover-0.0.2/PKG-INFO
+-rw-r--r--   0        0        0    35149 2023-07-23 11:15:43.843302 easy_liftover-0.0.3/LICENSE
+-rw-r--r--   0        0        0      459 2023-07-23 11:15:43.843302 easy_liftover-0.0.3/README.md
+-rw-r--r--   0        0        0      729 2023-07-23 11:15:43.843302 easy_liftover-0.0.3/pyproject.toml
+-rw-r--r--   0        0        0       67 2023-07-23 11:15:43.843302 easy_liftover-0.0.3/src/__init__.py
+-rw-r--r--   0        0        0      189 2023-07-23 11:15:43.843302 easy_liftover-0.0.3/src/genomes.py
+-rw-r--r--   0        0        0      117 2023-07-23 11:15:43.843302 easy_liftover-0.0.3/src/lifters/__init__.py
+-rw-r--r--   0        0        0     1931 2023-07-23 11:15:43.843302 easy_liftover-0.0.3/src/lifters/abstract.py
+-rw-r--r--   0        0        0      680 2023-07-23 11:15:43.843302 easy_liftover-0.0.3/src/lifters/bed.py
+-rw-r--r--   0        0        0      661 2023-07-23 11:15:43.843302 easy_liftover-0.0.3/src/lifters/gff.py
+-rw-r--r--   0        0        0       53 2023-07-23 11:15:44.495320 easy_liftover-0.0.3/src/lifters/pyliftover/.git
+-rw-r--r--   0        0        0      303 2023-07-23 11:15:44.503320 easy_liftover-0.0.3/src/lifters/pyliftover/.gitignore
+-rw-r--r--   0        0        0      139 2023-07-23 11:15:44.503320 easy_liftover-0.0.3/src/lifters/pyliftover/.travis.yml
+-rw-r--r--   0        0        0      416 2023-07-23 11:15:44.503320 easy_liftover-0.0.3/src/lifters/pyliftover/CHANGELOG.txt
+-rw-r--r--   0        0        0     1064 2023-07-23 11:15:44.503320 easy_liftover-0.0.3/src/lifters/pyliftover/LICENSE
+-rw-r--r--   0        0        0       32 2023-07-23 11:15:44.503320 easy_liftover-0.0.3/src/lifters/pyliftover/MANIFEST.in
+-rw-r--r--   0        0        0     2670 2023-07-23 11:15:44.503320 easy_liftover-0.0.3/src/lifters/pyliftover/README.rst
+-rw-r--r--   0        0        0     1661 2023-07-23 11:15:44.503320 easy_liftover-0.0.3/src/lifters/pyliftover/pyliftover/__init__.py
+-rw-r--r--   0        0        0    11116 2023-07-23 11:15:44.503320 easy_liftover-0.0.3/src/lifters/pyliftover/pyliftover/chainfile.py
+-rw-r--r--   0        0        0     6795 2023-07-23 11:15:44.503320 easy_liftover-0.0.3/src/lifters/pyliftover/pyliftover/intervaltree.py
+-rw-r--r--   0        0        0     5516 2023-07-23 11:15:44.503320 easy_liftover-0.0.3/src/lifters/pyliftover/pyliftover/liftover.py
+-rw-r--r--   0        0        0      178 2023-07-23 11:15:44.503320 easy_liftover-0.0.3/src/lifters/pyliftover/setup.cfg
+-rw-r--r--   0        0        0     1972 2023-07-23 11:15:44.503320 easy_liftover-0.0.3/src/lifters/pyliftover/setup.py
+-rw-r--r--   0        0        0      210 2023-07-23 11:15:44.503320 easy_liftover-0.0.3/src/lifters/pyliftover/tests/__init__.py
+-rw-r--r--   0        0        0     3756 2023-07-23 11:15:44.503320 easy_liftover-0.0.3/src/lifters/pyliftover/tests/chainfile_test.py
+-rw-r--r--   0        0        0      299 2023-07-23 11:15:44.503320 easy_liftover-0.0.3/src/lifters/pyliftover/tests/data/README.txt
+-rw-r--r--   0        0        0    85433 2023-07-23 11:15:44.503320 easy_liftover-0.0.3/src/lifters/pyliftover/tests/data/hg17ToHg18.over.chain.gz
+-rw-r--r--   0        0        0    68588 2023-07-23 11:15:44.507320 easy_liftover-0.0.3/src/lifters/pyliftover/tests/data/hg17ToHg18.testpoints.txt.gz
+-rw-r--r--   0        0        0  1246411 2023-07-23 11:15:44.507320 easy_liftover-0.0.3/src/lifters/pyliftover/tests/data/hg38ToHg19.over.chain.gz
+-rw-r--r--   0        0        0      818 2023-07-23 11:15:44.507320 easy_liftover-0.0.3/src/lifters/pyliftover/tests/data/hg38ToHg19.testinput.txt
+-rw-r--r--   0        0        0      523 2023-07-23 11:15:44.507320 easy_liftover-0.0.3/src/lifters/pyliftover/tests/data/hg38ToHg19.testoutput.txt
+-rw-r--r--   0        0        0      902 2023-07-23 11:15:44.507320 easy_liftover-0.0.3/src/lifters/pyliftover/tests/data/mds42.to.mg1655.liftOver
+-rw-r--r--   0        0        0     1247 2023-07-23 11:15:44.507320 easy_liftover-0.0.3/src/lifters/pyliftover/tests/intervaltree_test.py
+-rw-r--r--   0        0        0     3618 2023-07-23 11:15:44.507320 easy_liftover-0.0.3/src/lifters/pyliftover/tests/liftover_test.py
+-rw-r--r--   0        0        0     3952 2023-07-23 11:15:44.507320 easy_liftover-0.0.3/src/lifters/pyliftover/tests/open_liftover_chain_file_test.py
+-rw-r--r--   0        0        0     1825 2023-07-23 11:15:43.843302 easy_liftover-0.0.3/src/lifters/wig.py
+-rw-r--r--   0        0        0      610 2023-07-23 11:15:43.843302 easy_liftover-0.0.3/src/targets.py
+-rw-r--r--   0        0        0      770 2023-07-23 11:15:43.843302 easy_liftover-0.0.3/src/test_lifters.py
+-rw-r--r--   0        0        0     1231 2023-07-23 11:15:43.843302 easy_liftover-0.0.3/src/types.json
+-rw-r--r--   0        0        0     1223 2023-07-23 11:15:43.843302 easy_liftover-0.0.3/src/uplift.py
+-rw-r--r--   0        0        0     1174 1970-01-01 00:00:00.000000 easy_liftover-0.0.3/PKG-INFO
```

### Comparing `easy_liftover-0.0.2/LICENSE` & `easy_liftover-0.0.3/LICENSE`

 * *Files identical despite different names*

### Comparing `easy_liftover-0.0.2/pyproject.toml` & `easy_liftover-0.0.3/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["poetry-core>=1.0.0"]
 build-backend = "poetry.core.masonry.api"
 
 [tool.poetry]
 name = "easy-liftover"
-version = "0.0.2"
+version = "0.0.3"
 description = "A python package for lifting over biological files"
 packages = [
     { include = "*", from = "src" },
 ]
 license = "MIT"
 authors = ["Nico Trummer <nictru32@gmail.com>"]
 repository = "https://github.com/biomedbigdata/easyUplift"
```

### Comparing `easy_liftover-0.0.2/src/lifters/abstract.py` & `easy_liftover-0.0.3/src/lifters/abstract.py`

 * *Files identical despite different names*

### Comparing `easy_liftover-0.0.2/src/lifters/bed.py` & `easy_liftover-0.0.3/src/lifters/bed.py`

 * *Files identical despite different names*

### Comparing `easy_liftover-0.0.2/src/lifters/gff.py` & `easy_liftover-0.0.3/src/lifters/gff.py`

 * *Files identical despite different names*

### Comparing `easy_liftover-0.0.2/src/lifters/wig.py` & `easy_liftover-0.0.3/src/lifters/wig.py`

 * *Files identical despite different names*

### Comparing `easy_liftover-0.0.2/src/targets.py` & `easy_liftover-0.0.3/src/targets.py`

 * *Files identical despite different names*

### Comparing `easy_liftover-0.0.2/src/test_lifters.py` & `easy_liftover-0.0.3/src/test_lifters.py`

 * *Files identical despite different names*

### Comparing `easy_liftover-0.0.2/src/types.json` & `easy_liftover-0.0.3/src/types.json`

 * *Files identical despite different names*

### Comparing `easy_liftover-0.0.2/src/uplift.py` & `easy_liftover-0.0.3/src/uplift.py`

 * *Files identical despite different names*

### Comparing `easy_liftover-0.0.2/PKG-INFO` & `easy_liftover-0.0.3/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: easy-liftover
-Version: 0.0.2
+Version: 0.0.3
 Summary: A python package for lifting over biological files
 Home-page: https://github.com/biomedbigdata/easyUplift
 License: MIT
 Author: Nico Trummer
 Author-email: nictru32@gmail.com
 Requires-Python: >=3.8.1
 Classifier: License :: OSI Approved :: MIT License
```

