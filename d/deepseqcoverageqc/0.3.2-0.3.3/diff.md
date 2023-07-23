# Comparing `tmp/deepseqcoverageqc-0.3.2.tar.gz` & `tmp/deepseqcoverageqc-0.3.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "deepseqcoverageqc-0.3.2.tar", max compression
+gzip compressed data, was "deepseqcoverageqc-0.3.3.tar", max compression
```

## Comparing `deepseqcoverageqc-0.3.2.tar` & `deepseqcoverageqc-0.3.3.tar`

### file list

```diff
@@ -1,8 +1,8 @@
--rw-r--r--   0        0        0      596 2023-07-23 17:44:18.522314 deepseqcoverageqc-0.3.2/LICENSE
--rw-r--r--   0        0        0     8420 2023-07-23 17:44:18.522314 deepseqcoverageqc-0.3.2/README.md
--rw-r--r--   0        0        0       22 2023-07-23 17:44:18.522314 deepseqcoverageqc-0.3.2/deepseqcoverageqc/__init__.py
--rw-r--r--   0        0        0    10274 2023-07-23 17:44:18.522314 deepseqcoverageqc-0.3.2/deepseqcoverageqc/coverageQC.py
--rw-r--r--   0        0        0     3661 2023-07-23 17:44:18.522314 deepseqcoverageqc-0.3.2/deepseqcoverageqc/panelIndexer.py
--rw-r--r--   0        0        0     2638 2023-07-23 17:44:18.522314 deepseqcoverageqc-0.3.2/deepseqcoverageqc/panelQC.py
--rw-r--r--   0        0        0     1296 2023-07-23 17:44:18.522314 deepseqcoverageqc-0.3.2/pyproject.toml
--rw-r--r--   0        0        0     9048 1970-01-01 00:00:00.000000 deepseqcoverageqc-0.3.2/PKG-INFO
+-rw-r--r--   0        0        0      596 2023-07-23 18:45:38.265255 deepseqcoverageqc-0.3.3/LICENSE
+-rw-r--r--   0        0        0     8420 2023-07-23 18:45:38.269255 deepseqcoverageqc-0.3.3/README.md
+-rw-r--r--   0        0        0       22 2023-07-23 18:45:38.269255 deepseqcoverageqc-0.3.3/deepseqcoverageqc/__init__.py
+-rw-r--r--   0        0        0    10274 2023-07-23 18:45:38.269255 deepseqcoverageqc-0.3.3/deepseqcoverageqc/coverageQC.py
+-rw-r--r--   0        0        0     3661 2023-07-23 18:45:38.269255 deepseqcoverageqc-0.3.3/deepseqcoverageqc/panelIndexer.py
+-rw-r--r--   0        0        0     2638 2023-07-23 18:45:38.269255 deepseqcoverageqc-0.3.3/deepseqcoverageqc/panelQC.py
+-rw-r--r--   0        0        0     1296 2023-07-23 18:45:38.269255 deepseqcoverageqc-0.3.3/pyproject.toml
+-rw-r--r--   0        0        0     9048 1970-01-01 00:00:00.000000 deepseqcoverageqc-0.3.3/PKG-INFO
```

### Comparing `deepseqcoverageqc-0.3.2/LICENSE` & `deepseqcoverageqc-0.3.3/LICENSE`

 * *Files identical despite different names*

### Comparing `deepseqcoverageqc-0.3.2/README.md` & `deepseqcoverageqc-0.3.3/README.md`

 * *Files 0% similar despite different names*

```diff
@@ -47,15 +47,15 @@
 
 ---
 ## Quick Start
 
 ### Using [Docker](https://www.docker.com/)
 
 ```bash
-docker run -it pskolekar/deepseqcoverageqc:0.3.2 DeepSeqCoverageQC --help
+docker run -it pskolekar/deepseqcoverageqc:0.3.3 DeepSeqCoverageQC --help
 ```
 
 ### Using [Miniconda](https://docs.conda.io/en/latest/miniconda.html)
 
 ```bash
 conda create --name DeepSeqCoverageQC python==3.9
 conda activate DeepSeqCoverageQC
```

#### html2text {}

```diff
@@ -5,15 +5,15 @@
 
                              Explore_the_docs_Â»
 
 
                          Request_Feature | Report_Bug
                      â­ Consider starring the repo! â­
 --- ## Quick Start ### Using [Docker](https://www.docker.com/) ```bash docker
-run -it pskolekar/deepseqcoverageqc:0.3.2 DeepSeqCoverageQC --help ``` ###
+run -it pskolekar/deepseqcoverageqc:0.3.3 DeepSeqCoverageQC --help ``` ###
 Using [Miniconda](https://docs.conda.io/en/latest/miniconda.html) ```bash conda
 create --name DeepSeqCoverageQC python==3.9 conda activate DeepSeqCoverageQC
 python -m pip install deepseqcoverageqc DeepSeqCoverageQC --help ``` ### Using
 Pip > **Note** > Requires [Python](https://www.python.org/) version >=3.9
 ```bash pip install deepseqcoverageqc ``` ## Usage Please refer to the
 _detailed documentation_ [here](https://pandurang-kolekar.github.io/
 DeepSeqCoverageQC/) `DeepSeqCoverageQC` is a command line interface (CLI) app
```

### Comparing `deepseqcoverageqc-0.3.2/deepseqcoverageqc/coverageQC.py` & `deepseqcoverageqc-0.3.3/deepseqcoverageqc/coverageQC.py`

 * *Files identical despite different names*

### Comparing `deepseqcoverageqc-0.3.2/deepseqcoverageqc/panelIndexer.py` & `deepseqcoverageqc-0.3.3/deepseqcoverageqc/panelIndexer.py`

 * *Files identical despite different names*

### Comparing `deepseqcoverageqc-0.3.2/deepseqcoverageqc/panelQC.py` & `deepseqcoverageqc-0.3.3/deepseqcoverageqc/panelQC.py`

 * *Files identical despite different names*

### Comparing `deepseqcoverageqc-0.3.2/pyproject.toml` & `deepseqcoverageqc-0.3.3/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "DeepSeqCoverageQC"
-version = "0.3.2"
+version = "0.3.3"
 description = "Compute coverage QC metrics for deep targeted sequencing data"
 authors = ["Pandurang Kolekar <pandurang.kolekar@gmail.com>"]
 readme = "README.md"
 
 [tool.poetry_bumpversion.file."deepseqcoverageqc/__init__.py"]
 
 [[tool.poetry_bumpversion.replacements]]
```

### Comparing `deepseqcoverageqc-0.3.2/PKG-INFO` & `deepseqcoverageqc-0.3.3/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: deepseqcoverageqc
-Version: 0.3.2
+Version: 0.3.3
 Summary: Compute coverage QC metrics for deep targeted sequencing data
 Author: Pandurang Kolekar
 Author-email: pandurang.kolekar@gmail.com
 Requires-Python: >=3.9,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
@@ -64,15 +64,15 @@
 
 ---
 ## Quick Start
 
 ### Using [Docker](https://www.docker.com/)
 
 ```bash
-docker run -it pskolekar/deepseqcoverageqc:0.3.2 DeepSeqCoverageQC --help
+docker run -it pskolekar/deepseqcoverageqc:0.3.3 DeepSeqCoverageQC --help
 ```
 
 ### Using [Miniconda](https://docs.conda.io/en/latest/miniconda.html)
 
 ```bash
 conda create --name DeepSeqCoverageQC python==3.9
 conda activate DeepSeqCoverageQC
```

#### html2text {}

```diff
@@ -1,8 +1,8 @@
-Metadata-Version: 2.1 Name: deepseqcoverageqc Version: 0.3.2 Summary: Compute
+Metadata-Version: 2.1 Name: deepseqcoverageqc Version: 0.3.3 Summary: Compute
 coverage QC metrics for deep targeted sequencing data Author: Pandurang Kolekar
 Author-email: pandurang.kolekar@gmail.com Requires-Python: >=3.9,<4.0
 Classifier: Programming Language :: Python :: 3 Classifier: Programming
 Language :: Python :: 3.9 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11 Requires-Dist: click
 (>=8.1.3,<9.0.0) Requires-Dist: pandas (>=2.0.1,<3.0.0) Requires-Dist: rich-
 click (>=1.6.1,<2.0.0) Requires-Dist: tqdm (>=4.65.0,<5.0.0) Description-
@@ -14,15 +14,15 @@
 
                              Explore_the_docs_Â»
 
 
                          Request_Feature | Report_Bug
                      â­ Consider starring the repo! â­
 --- ## Quick Start ### Using [Docker](https://www.docker.com/) ```bash docker
-run -it pskolekar/deepseqcoverageqc:0.3.2 DeepSeqCoverageQC --help ``` ###
+run -it pskolekar/deepseqcoverageqc:0.3.3 DeepSeqCoverageQC --help ``` ###
 Using [Miniconda](https://docs.conda.io/en/latest/miniconda.html) ```bash conda
 create --name DeepSeqCoverageQC python==3.9 conda activate DeepSeqCoverageQC
 python -m pip install deepseqcoverageqc DeepSeqCoverageQC --help ``` ### Using
 Pip > **Note** > Requires [Python](https://www.python.org/) version >=3.9
 ```bash pip install deepseqcoverageqc ``` ## Usage Please refer to the
 _detailed documentation_ [here](https://pandurang-kolekar.github.io/
 DeepSeqCoverageQC/) `DeepSeqCoverageQC` is a command line interface (CLI) app
```

