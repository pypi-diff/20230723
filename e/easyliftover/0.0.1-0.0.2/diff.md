# Comparing `tmp/easyliftover-0.0.1.tar.gz` & `tmp/easyliftover-0.0.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "easyliftover-0.0.1.tar", max compression
+gzip compressed data, was "easyliftover-0.0.2.tar", max compression
```

## Comparing `easyliftover-0.0.1.tar` & `easyliftover-0.0.2.tar`

### file list

```diff
@@ -1,40 +1,40 @@
--rw-r--r--   0        0        0    35149 2023-07-23 11:45:33.006519 easyliftover-0.0.1/LICENSE
--rw-r--r--   0        0        0      459 2023-07-23 11:45:33.006519 easyliftover-0.0.1/README.md
--rw-r--r--   0        0        0      728 2023-07-23 11:45:33.006519 easyliftover-0.0.1/pyproject.toml
--rw-r--r--   0        0        0       67 2023-07-23 11:45:33.006519 easyliftover-0.0.1/src/__init__.py
--rw-r--r--   0        0        0      189 2023-07-23 11:45:33.006519 easyliftover-0.0.1/src/genomes.py
--rw-r--r--   0        0        0      117 2023-07-23 11:45:33.006519 easyliftover-0.0.1/src/lifters/__init__.py
--rw-r--r--   0        0        0     1931 2023-07-23 11:45:33.006519 easyliftover-0.0.1/src/lifters/abstract.py
--rw-r--r--   0        0        0      680 2023-07-23 11:45:33.006519 easyliftover-0.0.1/src/lifters/bed.py
--rw-r--r--   0        0        0      661 2023-07-23 11:45:33.006519 easyliftover-0.0.1/src/lifters/gff.py
--rw-r--r--   0        0        0       53 2023-07-23 11:45:33.706532 easyliftover-0.0.1/src/lifters/pyliftover/.git
--rw-r--r--   0        0        0      303 2023-07-23 11:45:33.714532 easyliftover-0.0.1/src/lifters/pyliftover/.gitignore
--rw-r--r--   0        0        0      139 2023-07-23 11:45:33.714532 easyliftover-0.0.1/src/lifters/pyliftover/.travis.yml
--rw-r--r--   0        0        0      416 2023-07-23 11:45:33.714532 easyliftover-0.0.1/src/lifters/pyliftover/CHANGELOG.txt
--rw-r--r--   0        0        0     1064 2023-07-23 11:45:33.714532 easyliftover-0.0.1/src/lifters/pyliftover/LICENSE
--rw-r--r--   0        0        0       32 2023-07-23 11:45:33.714532 easyliftover-0.0.1/src/lifters/pyliftover/MANIFEST.in
--rw-r--r--   0        0        0     2670 2023-07-23 11:45:33.714532 easyliftover-0.0.1/src/lifters/pyliftover/README.rst
--rw-r--r--   0        0        0     1661 2023-07-23 11:45:33.714532 easyliftover-0.0.1/src/lifters/pyliftover/pyliftover/__init__.py
--rw-r--r--   0        0        0    11116 2023-07-23 11:45:33.714532 easyliftover-0.0.1/src/lifters/pyliftover/pyliftover/chainfile.py
--rw-r--r--   0        0        0     6795 2023-07-23 11:45:33.714532 easyliftover-0.0.1/src/lifters/pyliftover/pyliftover/intervaltree.py
--rw-r--r--   0        0        0     5516 2023-07-23 11:45:33.714532 easyliftover-0.0.1/src/lifters/pyliftover/pyliftover/liftover.py
--rw-r--r--   0        0        0      178 2023-07-23 11:45:33.714532 easyliftover-0.0.1/src/lifters/pyliftover/setup.cfg
--rw-r--r--   0        0        0     1972 2023-07-23 11:45:33.714532 easyliftover-0.0.1/src/lifters/pyliftover/setup.py
--rw-r--r--   0        0        0      210 2023-07-23 11:45:33.714532 easyliftover-0.0.1/src/lifters/pyliftover/tests/__init__.py
--rw-r--r--   0        0        0     3756 2023-07-23 11:45:33.714532 easyliftover-0.0.1/src/lifters/pyliftover/tests/chainfile_test.py
--rw-r--r--   0        0        0      299 2023-07-23 11:45:33.714532 easyliftover-0.0.1/src/lifters/pyliftover/tests/data/README.txt
--rw-r--r--   0        0        0    85433 2023-07-23 11:45:33.714532 easyliftover-0.0.1/src/lifters/pyliftover/tests/data/hg17ToHg18.over.chain.gz
--rw-r--r--   0        0        0    68588 2023-07-23 11:45:33.714532 easyliftover-0.0.1/src/lifters/pyliftover/tests/data/hg17ToHg18.testpoints.txt.gz
--rw-r--r--   0        0        0  1246411 2023-07-23 11:45:33.718532 easyliftover-0.0.1/src/lifters/pyliftover/tests/data/hg38ToHg19.over.chain.gz
--rw-r--r--   0        0        0      818 2023-07-23 11:45:33.718532 easyliftover-0.0.1/src/lifters/pyliftover/tests/data/hg38ToHg19.testinput.txt
--rw-r--r--   0        0        0      523 2023-07-23 11:45:33.718532 easyliftover-0.0.1/src/lifters/pyliftover/tests/data/hg38ToHg19.testoutput.txt
--rw-r--r--   0        0        0      902 2023-07-23 11:45:33.718532 easyliftover-0.0.1/src/lifters/pyliftover/tests/data/mds42.to.mg1655.liftOver
--rw-r--r--   0        0        0     1247 2023-07-23 11:45:33.718532 easyliftover-0.0.1/src/lifters/pyliftover/tests/intervaltree_test.py
--rw-r--r--   0        0        0     3618 2023-07-23 11:45:33.718532 easyliftover-0.0.1/src/lifters/pyliftover/tests/liftover_test.py
--rw-r--r--   0        0        0     3952 2023-07-23 11:45:33.718532 easyliftover-0.0.1/src/lifters/pyliftover/tests/open_liftover_chain_file_test.py
--rw-r--r--   0        0        0     1825 2023-07-23 11:45:33.006519 easyliftover-0.0.1/src/lifters/wig.py
--rw-r--r--   0        0        0      610 2023-07-23 11:45:33.006519 easyliftover-0.0.1/src/targets.py
--rw-r--r--   0        0        0      770 2023-07-23 11:45:33.006519 easyliftover-0.0.1/src/test_lifters.py
--rw-r--r--   0        0        0     1231 2023-07-23 11:45:33.006519 easyliftover-0.0.1/src/types.json
--rw-r--r--   0        0        0     1223 2023-07-23 11:45:33.006519 easyliftover-0.0.1/src/uplift.py
--rw-r--r--   0        0        0     1173 1970-01-01 00:00:00.000000 easyliftover-0.0.1/PKG-INFO
+-rw-r--r--   0        0        0    35149 2023-07-23 12:10:38.040300 easyliftover-0.0.2/LICENSE
+-rw-r--r--   0        0        0      459 2023-07-23 12:10:38.040300 easyliftover-0.0.2/README.md
+-rw-r--r--   0        0        0       67 2023-07-23 12:10:38.040300 easyliftover-0.0.2/easyliftover/__init__.py
+-rw-r--r--   0        0        0      189 2023-07-23 12:10:38.040300 easyliftover-0.0.2/easyliftover/genomes.py
+-rw-r--r--   0        0        0      117 2023-07-23 12:10:38.040300 easyliftover-0.0.2/easyliftover/lifters/__init__.py
+-rw-r--r--   0        0        0     1931 2023-07-23 12:10:38.040300 easyliftover-0.0.2/easyliftover/lifters/abstract.py
+-rw-r--r--   0        0        0      680 2023-07-23 12:10:38.040300 easyliftover-0.0.2/easyliftover/lifters/bed.py
+-rw-r--r--   0        0        0      661 2023-07-23 12:10:38.040300 easyliftover-0.0.2/easyliftover/lifters/gff.py
+-rw-r--r--   0        0        0       62 2023-07-23 12:10:38.804367 easyliftover-0.0.2/easyliftover/lifters/pyliftover/.git
+-rw-r--r--   0        0        0      303 2023-07-23 12:10:38.812368 easyliftover-0.0.2/easyliftover/lifters/pyliftover/.gitignore
+-rw-r--r--   0        0        0      139 2023-07-23 12:10:38.812368 easyliftover-0.0.2/easyliftover/lifters/pyliftover/.travis.yml
+-rw-r--r--   0        0        0      416 2023-07-23 12:10:38.812368 easyliftover-0.0.2/easyliftover/lifters/pyliftover/CHANGELOG.txt
+-rw-r--r--   0        0        0     1064 2023-07-23 12:10:38.812368 easyliftover-0.0.2/easyliftover/lifters/pyliftover/LICENSE
+-rw-r--r--   0        0        0       32 2023-07-23 12:10:38.812368 easyliftover-0.0.2/easyliftover/lifters/pyliftover/MANIFEST.in
+-rw-r--r--   0        0        0     2670 2023-07-23 12:10:38.812368 easyliftover-0.0.2/easyliftover/lifters/pyliftover/README.rst
+-rw-r--r--   0        0        0     1661 2023-07-23 12:10:38.812368 easyliftover-0.0.2/easyliftover/lifters/pyliftover/pyliftover/__init__.py
+-rw-r--r--   0        0        0    11116 2023-07-23 12:10:38.812368 easyliftover-0.0.2/easyliftover/lifters/pyliftover/pyliftover/chainfile.py
+-rw-r--r--   0        0        0     6795 2023-07-23 12:10:38.812368 easyliftover-0.0.2/easyliftover/lifters/pyliftover/pyliftover/intervaltree.py
+-rw-r--r--   0        0        0     5516 2023-07-23 12:10:38.812368 easyliftover-0.0.2/easyliftover/lifters/pyliftover/pyliftover/liftover.py
+-rw-r--r--   0        0        0      178 2023-07-23 12:10:38.812368 easyliftover-0.0.2/easyliftover/lifters/pyliftover/setup.cfg
+-rw-r--r--   0        0        0     1972 2023-07-23 12:10:38.812368 easyliftover-0.0.2/easyliftover/lifters/pyliftover/setup.py
+-rw-r--r--   0        0        0      210 2023-07-23 12:10:38.812368 easyliftover-0.0.2/easyliftover/lifters/pyliftover/tests/__init__.py
+-rw-r--r--   0        0        0     3756 2023-07-23 12:10:38.812368 easyliftover-0.0.2/easyliftover/lifters/pyliftover/tests/chainfile_test.py
+-rw-r--r--   0        0        0      299 2023-07-23 12:10:38.812368 easyliftover-0.0.2/easyliftover/lifters/pyliftover/tests/data/README.txt
+-rw-r--r--   0        0        0    85433 2023-07-23 12:10:38.812368 easyliftover-0.0.2/easyliftover/lifters/pyliftover/tests/data/hg17ToHg18.over.chain.gz
+-rw-r--r--   0        0        0    68588 2023-07-23 12:10:38.812368 easyliftover-0.0.2/easyliftover/lifters/pyliftover/tests/data/hg17ToHg18.testpoints.txt.gz
+-rw-r--r--   0        0        0  1246411 2023-07-23 12:10:38.816368 easyliftover-0.0.2/easyliftover/lifters/pyliftover/tests/data/hg38ToHg19.over.chain.gz
+-rw-r--r--   0        0        0      818 2023-07-23 12:10:38.816368 easyliftover-0.0.2/easyliftover/lifters/pyliftover/tests/data/hg38ToHg19.testinput.txt
+-rw-r--r--   0        0        0      523 2023-07-23 12:10:38.816368 easyliftover-0.0.2/easyliftover/lifters/pyliftover/tests/data/hg38ToHg19.testoutput.txt
+-rw-r--r--   0        0        0      902 2023-07-23 12:10:38.816368 easyliftover-0.0.2/easyliftover/lifters/pyliftover/tests/data/mds42.to.mg1655.liftOver
+-rw-r--r--   0        0        0     1247 2023-07-23 12:10:38.816368 easyliftover-0.0.2/easyliftover/lifters/pyliftover/tests/intervaltree_test.py
+-rw-r--r--   0        0        0     3618 2023-07-23 12:10:38.816368 easyliftover-0.0.2/easyliftover/lifters/pyliftover/tests/liftover_test.py
+-rw-r--r--   0        0        0     3952 2023-07-23 12:10:38.816368 easyliftover-0.0.2/easyliftover/lifters/pyliftover/tests/open_liftover_chain_file_test.py
+-rw-r--r--   0        0        0     1825 2023-07-23 12:10:38.040300 easyliftover-0.0.2/easyliftover/lifters/wig.py
+-rw-r--r--   0        0        0      610 2023-07-23 12:10:38.040300 easyliftover-0.0.2/easyliftover/targets.py
+-rw-r--r--   0        0        0      770 2023-07-23 12:10:38.040300 easyliftover-0.0.2/easyliftover/test_lifters.py
+-rw-r--r--   0        0        0     1231 2023-07-23 12:10:38.040300 easyliftover-0.0.2/easyliftover/types.json
+-rw-r--r--   0        0        0     1223 2023-07-23 12:10:38.040300 easyliftover-0.0.2/easyliftover/uplift.py
+-rw-r--r--   0        0        0      685 2023-07-23 12:10:38.040300 easyliftover-0.0.2/pyproject.toml
+-rw-r--r--   0        0        0     1173 1970-01-01 00:00:00.000000 easyliftover-0.0.2/PKG-INFO
```

### Comparing `easyliftover-0.0.1/LICENSE` & `easyliftover-0.0.2/LICENSE`

 * *Files identical despite different names*

### Comparing `easyliftover-0.0.1/pyproject.toml` & `easyliftover-0.0.2/pyproject.toml`

 * *Files 10% similar despite different names*

```diff
@@ -1,18 +1,15 @@
 [build-system]
 requires = ["poetry-core>=1.0.0"]
 build-backend = "poetry.core.masonry.api"
 
 [tool.poetry]
 name = "easyliftover"
-version = "0.0.1"
+version = "0.0.2"
 description = "A python package for lifting over biological files"
-packages = [
-    { include = "*", from = "src" },
-]
 license = "MIT"
 authors = ["Nico Trummer <nictru32@gmail.com>"]
 repository = "https://github.com/biomedbigdata/easyUplift"
 homepage = "https://github.com/biomedbigdata/easyUplift"
 readme = "README.md"
 
 [tool.poetry.dependencies]
@@ -22,8 +19,8 @@
 
 [tool.poetry.dev-dependencies]
 pytest = "^6.2.4"
 pytest-cov = "^2.12.1"
 flake8 = "^6.0.0"
 
 [tool.pytest.ini_options]
-addopts = "--cov --ignore=src/lifters/pyliftover"
+addopts = "--cov --ignore=easyliftover/lifters/pyliftover"
```

### Comparing `easyliftover-0.0.1/src/lifters/abstract.py` & `easyliftover-0.0.2/easyliftover/lifters/abstract.py`

 * *Files identical despite different names*

### Comparing `easyliftover-0.0.1/src/lifters/bed.py` & `easyliftover-0.0.2/easyliftover/lifters/bed.py`

 * *Files identical despite different names*

### Comparing `easyliftover-0.0.1/src/lifters/gff.py` & `easyliftover-0.0.2/easyliftover/lifters/gff.py`

 * *Files identical despite different names*

### Comparing `easyliftover-0.0.1/src/lifters/pyliftover/LICENSE` & `easyliftover-0.0.2/easyliftover/lifters/pyliftover/LICENSE`

 * *Files identical despite different names*

### Comparing `easyliftover-0.0.1/src/lifters/pyliftover/README.rst` & `easyliftover-0.0.2/easyliftover/lifters/pyliftover/README.rst`

 * *Files identical despite different names*

### Comparing `easyliftover-0.0.1/src/lifters/pyliftover/pyliftover/__init__.py` & `easyliftover-0.0.2/easyliftover/lifters/pyliftover/pyliftover/__init__.py`

 * *Files identical despite different names*

### Comparing `easyliftover-0.0.1/src/lifters/pyliftover/pyliftover/chainfile.py` & `easyliftover-0.0.2/easyliftover/lifters/pyliftover/pyliftover/chainfile.py`

 * *Files identical despite different names*

### Comparing `easyliftover-0.0.1/src/lifters/pyliftover/pyliftover/intervaltree.py` & `easyliftover-0.0.2/easyliftover/lifters/pyliftover/pyliftover/intervaltree.py`

 * *Files identical despite different names*

### Comparing `easyliftover-0.0.1/src/lifters/pyliftover/pyliftover/liftover.py` & `easyliftover-0.0.2/easyliftover/lifters/pyliftover/pyliftover/liftover.py`

 * *Files identical despite different names*

### Comparing `easyliftover-0.0.1/src/lifters/pyliftover/setup.py` & `easyliftover-0.0.2/easyliftover/lifters/pyliftover/setup.py`

 * *Files identical despite different names*

### Comparing `easyliftover-0.0.1/src/lifters/pyliftover/tests/chainfile_test.py` & `easyliftover-0.0.2/easyliftover/lifters/pyliftover/tests/chainfile_test.py`

 * *Files identical despite different names*

### Comparing `easyliftover-0.0.1/src/lifters/pyliftover/tests/data/hg17ToHg18.over.chain.gz` & `easyliftover-0.0.2/easyliftover/lifters/pyliftover/tests/data/hg17ToHg18.over.chain.gz`

 * *Files identical despite different names*

### Comparing `easyliftover-0.0.1/src/lifters/pyliftover/tests/data/hg17ToHg18.testpoints.txt.gz` & `easyliftover-0.0.2/easyliftover/lifters/pyliftover/tests/data/hg17ToHg18.testpoints.txt.gz`

 * *Files identical despite different names*

### Comparing `easyliftover-0.0.1/src/lifters/pyliftover/tests/data/hg38ToHg19.over.chain.gz` & `easyliftover-0.0.2/easyliftover/lifters/pyliftover/tests/data/hg38ToHg19.over.chain.gz`

 * *Files identical despite different names*

### Comparing `easyliftover-0.0.1/src/lifters/pyliftover/tests/data/hg38ToHg19.testinput.txt` & `easyliftover-0.0.2/easyliftover/lifters/pyliftover/tests/data/hg38ToHg19.testinput.txt`

 * *Files identical despite different names*

### Comparing `easyliftover-0.0.1/src/lifters/pyliftover/tests/data/hg38ToHg19.testoutput.txt` & `easyliftover-0.0.2/easyliftover/lifters/pyliftover/tests/data/hg38ToHg19.testoutput.txt`

 * *Files identical despite different names*

### Comparing `easyliftover-0.0.1/src/lifters/pyliftover/tests/data/mds42.to.mg1655.liftOver` & `easyliftover-0.0.2/easyliftover/lifters/pyliftover/tests/data/mds42.to.mg1655.liftOver`

 * *Files identical despite different names*

### Comparing `easyliftover-0.0.1/src/lifters/pyliftover/tests/intervaltree_test.py` & `easyliftover-0.0.2/easyliftover/lifters/pyliftover/tests/intervaltree_test.py`

 * *Files identical despite different names*

### Comparing `easyliftover-0.0.1/src/lifters/pyliftover/tests/liftover_test.py` & `easyliftover-0.0.2/easyliftover/lifters/pyliftover/tests/liftover_test.py`

 * *Files identical despite different names*

### Comparing `easyliftover-0.0.1/src/lifters/pyliftover/tests/open_liftover_chain_file_test.py` & `easyliftover-0.0.2/easyliftover/lifters/pyliftover/tests/open_liftover_chain_file_test.py`

 * *Files identical despite different names*

### Comparing `easyliftover-0.0.1/src/lifters/wig.py` & `easyliftover-0.0.2/easyliftover/lifters/wig.py`

 * *Files identical despite different names*

### Comparing `easyliftover-0.0.1/src/targets.py` & `easyliftover-0.0.2/easyliftover/targets.py`

 * *Files identical despite different names*

### Comparing `easyliftover-0.0.1/src/test_lifters.py` & `easyliftover-0.0.2/easyliftover/test_lifters.py`

 * *Files identical despite different names*

### Comparing `easyliftover-0.0.1/src/types.json` & `easyliftover-0.0.2/easyliftover/types.json`

 * *Files identical despite different names*

### Comparing `easyliftover-0.0.1/src/uplift.py` & `easyliftover-0.0.2/easyliftover/uplift.py`

 * *Files identical despite different names*

### Comparing `easyliftover-0.0.1/PKG-INFO` & `easyliftover-0.0.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: easyliftover
-Version: 0.0.1
+Version: 0.0.2
 Summary: A python package for lifting over biological files
 Home-page: https://github.com/biomedbigdata/easyUplift
 License: MIT
 Author: Nico Trummer
 Author-email: nictru32@gmail.com
 Requires-Python: >=3.8.1
 Classifier: License :: OSI Approved :: MIT License
```

