# Comparing `tmp/datahelp-0.1.5.tar.gz` & `tmp/datahelp-0.1.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "datahelp-0.1.5.tar", max compression
+gzip compressed data, was "datahelp-0.1.6.tar", max compression
```

## Comparing `datahelp-0.1.5.tar` & `datahelp-0.1.6.tar`

### file list

```diff
@@ -1,16 +1,16 @@
--rw-r--r--   0        0        0     1067 2023-07-19 21:51:44.526819 datahelp-0.1.5/LICENSE.txt
--rw-r--r--   0        0        0     3277 2023-07-23 15:57:07.399162 datahelp-0.1.5/README.md
--rw-r--r--   0        0        0        0 2023-04-26 07:38:28.009704 datahelp-0.1.5/datahelp/.editorconfig
--rw-r--r--   0        0        0       22 2023-07-23 18:25:01.357035 datahelp-0.1.5/datahelp/__init__.py
--rw-r--r--   0        0        0     4634 2023-07-23 15:41:42.769384 datahelp-0.1.5/datahelp/create_project.py
--rw-r--r--   0        0        0     7813 2023-07-23 00:03:38.918086 datahelp-0.1.5/datahelp/eda.py
--rw-r--r--   0        0        0     8215 2023-07-23 18:22:48.157069 datahelp-0.1.5/datahelp/examples/.ipynb_checkpoints/ex3-checkpoint.ipynb
--rw-r--r--   0        0        0     3858 2023-05-01 16:01:21.804048 datahelp-0.1.5/datahelp/examples/data/iris.csv
--rw-r--r--   0        0        0     1755 2023-07-22 21:56:39.608845 datahelp-0.1.5/datahelp/examples/ex1.py
--rw-r--r--   0        0        0    10080 2023-07-23 18:24:48.367038 datahelp-0.1.5/datahelp/examples/ex3.ipynb
--rw-r--r--   0        0        0     5003 2023-07-22 22:04:55.078795 datahelp-0.1.5/datahelp/feature_engineering.py
--rw-r--r--   0        0        0     4231 2023-07-22 22:00:28.688823 datahelp-0.1.5/datahelp/modelling.py
--rw-r--r--   0        0        0     1042 2023-07-22 23:17:03.308364 datahelp-0.1.5/datahelp/utils.py
--rw-r--r--   0        0        0      745 2023-07-19 21:38:45.626915 datahelp-0.1.5/datahelp/visualize.py
--rw-r--r--   0        0        0      932 2023-07-23 18:24:56.537036 datahelp-0.1.5/pyproject.toml
--rw-r--r--   0        0        0     4576 1970-01-01 00:00:00.000000 datahelp-0.1.5/PKG-INFO
+-rw-r--r--   0        0        0     1067 2023-07-19 21:51:44.526819 datahelp-0.1.6/LICENSE.txt
+-rw-r--r--   0        0        0     3277 2023-07-23 15:57:07.399162 datahelp-0.1.6/README.md
+-rw-r--r--   0        0        0        0 2023-04-26 07:38:28.009704 datahelp-0.1.6/datahelp/.editorconfig
+-rw-r--r--   0        0        0       22 2023-07-23 19:01:46.446493 datahelp-0.1.6/datahelp/__init__.py
+-rw-r--r--   0        0        0     4634 2023-07-23 15:41:42.769384 datahelp-0.1.6/datahelp/create_project.py
+-rw-r--r--   0        0        0     7813 2023-07-23 00:03:38.918086 datahelp-0.1.6/datahelp/eda.py
+-rw-r--r--   0        0        0     8215 2023-07-23 18:22:48.157069 datahelp-0.1.6/datahelp/examples/.ipynb_checkpoints/ex3-checkpoint.ipynb
+-rw-r--r--   0        0        0     3858 2023-05-01 16:01:21.804048 datahelp-0.1.6/datahelp/examples/data/iris.csv
+-rw-r--r--   0        0        0     1755 2023-07-22 21:56:39.608845 datahelp-0.1.6/datahelp/examples/ex1.py
+-rw-r--r--   0        0        0    17425 2023-07-23 18:52:53.576632 datahelp-0.1.6/datahelp/examples/ex3.ipynb
+-rw-r--r--   0        0        0     5003 2023-07-22 22:04:55.078795 datahelp-0.1.6/datahelp/feature_engineering.py
+-rw-r--r--   0        0        0     4231 2023-07-22 22:00:28.688823 datahelp-0.1.6/datahelp/modelling.py
+-rw-r--r--   0        0        0     1042 2023-07-22 23:17:03.308364 datahelp-0.1.6/datahelp/utils.py
+-rw-r--r--   0        0        0      745 2023-07-19 21:38:45.626915 datahelp-0.1.6/datahelp/visualize.py
+-rw-r--r--   0        0        0      941 2023-07-23 19:01:41.196494 datahelp-0.1.6/pyproject.toml
+-rw-r--r--   0        0        0     4626 1970-01-01 00:00:00.000000 datahelp-0.1.6/PKG-INFO
```

### Comparing `datahelp-0.1.5/LICENSE.txt` & `datahelp-0.1.6/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.5/README.md` & `datahelp-0.1.6/README.md`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.5/datahelp/create_project.py` & `datahelp-0.1.6/datahelp/create_project.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.5/datahelp/eda.py` & `datahelp-0.1.6/datahelp/eda.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.5/datahelp/examples/.ipynb_checkpoints/ex3-checkpoint.ipynb` & `datahelp-0.1.6/datahelp/examples/.ipynb_checkpoints/ex3-checkpoint.ipynb`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.5/datahelp/examples/data/iris.csv` & `datahelp-0.1.6/datahelp/examples/data/iris.csv`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.5/datahelp/examples/ex1.py` & `datahelp-0.1.6/datahelp/examples/ex1.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.5/datahelp/feature_engineering.py` & `datahelp-0.1.6/datahelp/feature_engineering.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.5/datahelp/modelling.py` & `datahelp-0.1.6/datahelp/modelling.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.5/datahelp/utils.py` & `datahelp-0.1.6/datahelp/utils.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.5/datahelp/visualize.py` & `datahelp-0.1.6/datahelp/visualize.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.5/PKG-INFO` & `datahelp-0.1.6/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: datahelp
-Version: 0.1.5
+Version: 0.1.6
 Summary: Data science library for data science / data analysis teams
 Home-page: https://github.com/kimxons/datahelp
 License: MIT
 Keywords: data,science,data analysis,library,machine learning
 Author: Meshack Kitonga
 Author-email: dev.kitonga@gmail.com
 Classifier: Development Status :: 3 - Alpha
@@ -17,22 +17,22 @@
 Classifier: Programming Language :: Python :: 3.5
 Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
-Requires-Dist: joblib (==1.0.1)
-Requires-Dist: jupyter (==1.0.0)
-Requires-Dist: matplotlib (==3.4.3)
-Requires-Dist: nltk (==3.6.4)
-Requires-Dist: numpy (==1.21.2)
-Requires-Dist: pandas (==1.3.3)
-Requires-Dist: scikit-learn (==1.2.2)
-Requires-Dist: seaborn (==0.11.2)
+Requires-Dist: joblib (>=1.0.1)
+Requires-Dist: jupyter (>=1.0.0,<2.0.0)
+Requires-Dist: matplotlib (>=3.4.3,<4.0.0)
+Requires-Dist: nltk (>=3.6.4,<4.0.0)
+Requires-Dist: numpy (>=1.21.2,<2.0.0)
+Requires-Dist: pandas (>=1.3.3,<2.0.0)
+Requires-Dist: scikit-learn (>=1.2.2,<2.0.0)
+Requires-Dist: seaborn (>=0.11.2,<0.12.0)
 Project-URL: Repository, https://github.com/kimxons/datahelp.git
 Description-Content-Type: text/markdown
 
 # datahelp
 
 datahelp is a Python library designed to assist data science and data analysis teams in their workflow. It provides various utility functions and tools to streamline common data science tasks.
```

