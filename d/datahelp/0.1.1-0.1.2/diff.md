# Comparing `tmp/datahelp-0.1.1.tar.gz` & `tmp/datahelp-0.1.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "datahelp-0.1.1.tar", max compression
+gzip compressed data, was "datahelp-0.1.2.tar", max compression
```

## Comparing `datahelp-0.1.1.tar` & `datahelp-0.1.2.tar`

### file list

```diff
@@ -1,17 +1,17 @@
--rw-r--r--   0        0        0     1067 2023-07-19 21:51:44.526819 datahelp-0.1.1/LICENSE.txt
--rw-r--r--   0        0        0     3277 2023-07-23 15:57:07.399162 datahelp-0.1.1/README.md
--rw-r--r--   0        0        0        0 2023-04-26 07:38:28.009704 datahelp-0.1.1/datahelp/.editorconfig
--rw-r--r--   0        0        0       22 2023-07-23 16:17:58.108865 datahelp-0.1.1/datahelp/__init__.py
--rw-r--r--   0        0        0     4634 2023-07-23 15:41:42.769384 datahelp-0.1.1/datahelp/create_project.py
--rw-r--r--   0        0        0     7813 2023-07-23 00:03:38.918086 datahelp-0.1.1/datahelp/eda.py
--rw-r--r--   0        0        0     9791 2023-07-23 15:41:42.769384 datahelp-0.1.1/datahelp/examples/.ipynb_checkpoints/ex3-checkpoint.ipynb
--rw-r--r--   0        0        0     3858 2023-05-01 16:01:21.804048 datahelp-0.1.1/datahelp/examples/data/iris.csv
--rw-r--r--   0        0        0     1755 2023-07-22 21:56:39.608845 datahelp-0.1.1/datahelp/examples/ex1.py
--rw-r--r--   0        0        0     2112 2023-07-22 22:15:12.288732 datahelp-0.1.1/datahelp/examples/ex2.py
--rw-r--r--   0        0        0  2933835 2023-07-23 16:16:00.458892 datahelp-0.1.1/datahelp/examples/ex3.ipynb
--rw-r--r--   0        0        0     5003 2023-07-22 22:04:55.078795 datahelp-0.1.1/datahelp/feature_engineering.py
--rw-r--r--   0        0        0     4231 2023-07-22 22:00:28.688823 datahelp-0.1.1/datahelp/modelling.py
--rw-r--r--   0        0        0     1042 2023-07-22 23:17:03.308364 datahelp-0.1.1/datahelp/utils.py
--rw-r--r--   0        0        0      745 2023-07-19 21:38:45.626915 datahelp-0.1.1/datahelp/visualize.py
--rw-r--r--   0        0        0      955 2023-07-23 16:17:44.638867 datahelp-0.1.1/pyproject.toml
--rw-r--r--   0        0        0     4460 1970-01-01 00:00:00.000000 datahelp-0.1.1/PKG-INFO
+-rw-r--r--   0        0        0     1067 2023-07-19 21:51:44.526819 datahelp-0.1.2/LICENSE.txt
+-rw-r--r--   0        0        0     3277 2023-07-23 15:57:07.399162 datahelp-0.1.2/README.md
+-rw-r--r--   0        0        0        0 2023-04-26 07:38:28.009704 datahelp-0.1.2/datahelp/.editorconfig
+-rw-r--r--   0        0        0       22 2023-07-23 16:22:15.388803 datahelp-0.1.2/datahelp/__init__.py
+-rw-r--r--   0        0        0     4634 2023-07-23 15:41:42.769384 datahelp-0.1.2/datahelp/create_project.py
+-rw-r--r--   0        0        0     7813 2023-07-23 00:03:38.918086 datahelp-0.1.2/datahelp/eda.py
+-rw-r--r--   0        0        0     9791 2023-07-23 15:41:42.769384 datahelp-0.1.2/datahelp/examples/.ipynb_checkpoints/ex3-checkpoint.ipynb
+-rw-r--r--   0        0        0     3858 2023-05-01 16:01:21.804048 datahelp-0.1.2/datahelp/examples/data/iris.csv
+-rw-r--r--   0        0        0     1755 2023-07-22 21:56:39.608845 datahelp-0.1.2/datahelp/examples/ex1.py
+-rw-r--r--   0        0        0     2112 2023-07-22 22:15:12.288732 datahelp-0.1.2/datahelp/examples/ex2.py
+-rw-r--r--   0        0        0     8705 2023-07-23 16:22:03.338806 datahelp-0.1.2/datahelp/examples/ex3.ipynb
+-rw-r--r--   0        0        0     5003 2023-07-22 22:04:55.078795 datahelp-0.1.2/datahelp/feature_engineering.py
+-rw-r--r--   0        0        0     4231 2023-07-22 22:00:28.688823 datahelp-0.1.2/datahelp/modelling.py
+-rw-r--r--   0        0        0     1042 2023-07-22 23:17:03.308364 datahelp-0.1.2/datahelp/utils.py
+-rw-r--r--   0        0        0      745 2023-07-19 21:38:45.626915 datahelp-0.1.2/datahelp/visualize.py
+-rw-r--r--   0        0        0      938 2023-07-23 16:22:10.818804 datahelp-0.1.2/pyproject.toml
+-rw-r--r--   0        0        0     4635 1970-01-01 00:00:00.000000 datahelp-0.1.2/PKG-INFO
```

### Comparing `datahelp-0.1.1/LICENSE.txt` & `datahelp-0.1.2/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.1/README.md` & `datahelp-0.1.2/README.md`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.1/datahelp/create_project.py` & `datahelp-0.1.2/datahelp/create_project.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.1/datahelp/eda.py` & `datahelp-0.1.2/datahelp/eda.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.1/datahelp/examples/.ipynb_checkpoints/ex3-checkpoint.ipynb` & `datahelp-0.1.2/datahelp/examples/.ipynb_checkpoints/ex3-checkpoint.ipynb`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.1/datahelp/examples/data/iris.csv` & `datahelp-0.1.2/datahelp/examples/data/iris.csv`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.1/datahelp/examples/ex1.py` & `datahelp-0.1.2/datahelp/examples/ex1.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.1/datahelp/examples/ex2.py` & `datahelp-0.1.2/datahelp/examples/ex2.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.1/datahelp/feature_engineering.py` & `datahelp-0.1.2/datahelp/feature_engineering.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.1/datahelp/modelling.py` & `datahelp-0.1.2/datahelp/modelling.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.1/datahelp/utils.py` & `datahelp-0.1.2/datahelp/utils.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.1/datahelp/visualize.py` & `datahelp-0.1.2/datahelp/visualize.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.1/pyproject.toml` & `datahelp-0.1.2/pyproject.toml`

 * *Files 15% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["poetry-core>=1.1.0"]
 build-backend = "poetry.core.masonry.api"
 
 [tool.poetry]
 name = "datahelp"
-version = "0.1.1"
+version = "0.1.2"
 description = "Data science library for data science / data analysis teams"
 authors = ["Meshack Kitonga <dev.kitonga@gmail.com>"]
 license = "MIT"
 homepage = "https://github.com/kimxons/datahelp"
 repository = "https://github.com/kimxons/datahelp.git"
 readme = "README.md"
 keywords = ["data", "science", "data analysis", "library", "machine learning"]
@@ -16,15 +16,14 @@
     "Development Status :: 3 - Alpha",
     "Intended Audience :: Developers",
     "License :: OSI Approved :: MIT License",
     "Programming Language :: Python :: 3",
 ]
 
 [tool.poetry.dependencies]
-python = ">=3.6"
 pandas = "^1.3.3"
 scikit-learn = "^0.24.2"
 seaborn = "^0.11.2"
 numpy = "^1.21.2"
 jupyter = "^1.0.0"
 matplotlib = "^3.4.3"
 nltk = "^3.6.4"
```

### Comparing `datahelp-0.1.1/PKG-INFO` & `datahelp-0.1.2/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,21 +1,24 @@
 Metadata-Version: 2.1
 Name: datahelp
-Version: 0.1.1
+Version: 0.1.2
 Summary: Data science library for data science / data analysis teams
 Home-page: https://github.com/kimxons/datahelp
 License: MIT
 Keywords: data,science,data analysis,library,machine learning
 Author: Meshack Kitonga
 Author-email: dev.kitonga@gmail.com
-Requires-Python: >=3.6
 Classifier: Development Status :: 3 - Alpha
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
+Classifier: Programming Language :: Python :: 2
+Classifier: Programming Language :: Python :: 2.7
 Classifier: Programming Language :: Python :: 3
+Classifier: Programming Language :: Python :: 3.4
+Classifier: Programming Language :: Python :: 3.5
 Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Requires-Dist: joblib (>=1.0.1,<2.0.0)
```

