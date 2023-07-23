# Comparing `tmp/datahelp-0.1.3.tar.gz` & `tmp/datahelp-0.1.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "datahelp-0.1.3.tar", max compression
+gzip compressed data, was "datahelp-0.1.4.tar", max compression
```

## Comparing `datahelp-0.1.3.tar` & `datahelp-0.1.4.tar`

### file list

```diff
@@ -1,16 +1,16 @@
--rw-r--r--   0        0        0     1067 2023-07-19 21:51:44.526819 datahelp-0.1.3/LICENSE.txt
--rw-r--r--   0        0        0     3277 2023-07-23 15:57:07.399162 datahelp-0.1.3/README.md
--rw-r--r--   0        0        0        0 2023-04-26 07:38:28.009704 datahelp-0.1.3/datahelp/.editorconfig
--rw-r--r--   0        0        0       22 2023-07-23 17:30:13.327828 datahelp-0.1.3/datahelp/__init__.py
--rw-r--r--   0        0        0     4634 2023-07-23 15:41:42.769384 datahelp-0.1.3/datahelp/create_project.py
--rw-r--r--   0        0        0     7813 2023-07-23 00:03:38.918086 datahelp-0.1.3/datahelp/eda.py
--rw-r--r--   0        0        0     7213 2023-07-23 16:35:21.498616 datahelp-0.1.3/datahelp/examples/.ipynb_checkpoints/ex3-checkpoint.ipynb
--rw-r--r--   0        0        0     3858 2023-05-01 16:01:21.804048 datahelp-0.1.3/datahelp/examples/data/iris.csv
--rw-r--r--   0        0        0     1755 2023-07-22 21:56:39.608845 datahelp-0.1.3/datahelp/examples/ex1.py
--rw-r--r--   0        0        0     7213 2023-07-23 16:35:21.498616 datahelp-0.1.3/datahelp/examples/ex3.ipynb
--rw-r--r--   0        0        0     5003 2023-07-22 22:04:55.078795 datahelp-0.1.3/datahelp/feature_engineering.py
--rw-r--r--   0        0        0     4231 2023-07-22 22:00:28.688823 datahelp-0.1.3/datahelp/modelling.py
--rw-r--r--   0        0        0     1042 2023-07-22 23:17:03.308364 datahelp-0.1.3/datahelp/utils.py
--rw-r--r--   0        0        0      745 2023-07-19 21:38:45.626915 datahelp-0.1.3/datahelp/visualize.py
--rw-r--r--   0        0        0      941 2023-07-23 17:30:03.877829 datahelp-0.1.3/pyproject.toml
--rw-r--r--   0        0        0     4635 1970-01-01 00:00:00.000000 datahelp-0.1.3/PKG-INFO
+-rw-r--r--   0        0        0     1067 2023-07-19 21:51:44.526819 datahelp-0.1.4/LICENSE.txt
+-rw-r--r--   0        0        0     3277 2023-07-23 15:57:07.399162 datahelp-0.1.4/README.md
+-rw-r--r--   0        0        0        0 2023-04-26 07:38:28.009704 datahelp-0.1.4/datahelp/.editorconfig
+-rw-r--r--   0        0        0       22 2023-07-23 18:19:57.047105 datahelp-0.1.4/datahelp/__init__.py
+-rw-r--r--   0        0        0     4634 2023-07-23 15:41:42.769384 datahelp-0.1.4/datahelp/create_project.py
+-rw-r--r--   0        0        0     7813 2023-07-23 00:03:38.918086 datahelp-0.1.4/datahelp/eda.py
+-rw-r--r--   0        0        0     8091 2023-07-23 18:17:38.917137 datahelp-0.1.4/datahelp/examples/.ipynb_checkpoints/ex3-checkpoint.ipynb
+-rw-r--r--   0        0        0     3858 2023-05-01 16:01:21.804048 datahelp-0.1.4/datahelp/examples/data/iris.csv
+-rw-r--r--   0        0        0     1755 2023-07-22 21:56:39.608845 datahelp-0.1.4/datahelp/examples/ex1.py
+-rw-r--r--   0        0        0     8215 2023-07-23 18:19:39.357109 datahelp-0.1.4/datahelp/examples/ex3.ipynb
+-rw-r--r--   0        0        0     5003 2023-07-22 22:04:55.078795 datahelp-0.1.4/datahelp/feature_engineering.py
+-rw-r--r--   0        0        0     4231 2023-07-22 22:00:28.688823 datahelp-0.1.4/datahelp/modelling.py
+-rw-r--r--   0        0        0     1042 2023-07-22 23:17:03.308364 datahelp-0.1.4/datahelp/utils.py
+-rw-r--r--   0        0        0      745 2023-07-19 21:38:45.626915 datahelp-0.1.4/datahelp/visualize.py
+-rw-r--r--   0        0        0      940 2023-07-23 18:19:53.757106 datahelp-0.1.4/pyproject.toml
+-rw-r--r--   0        0        0     4633 1970-01-01 00:00:00.000000 datahelp-0.1.4/PKG-INFO
```

### Comparing `datahelp-0.1.3/LICENSE.txt` & `datahelp-0.1.4/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.3/README.md` & `datahelp-0.1.4/README.md`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.3/datahelp/create_project.py` & `datahelp-0.1.4/datahelp/create_project.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.3/datahelp/eda.py` & `datahelp-0.1.4/datahelp/eda.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.3/datahelp/examples/.ipynb_checkpoints/ex3-checkpoint.ipynb` & `datahelp-0.1.4/datahelp/examples/.ipynb_checkpoints/ex3-checkpoint.ipynb`

 * *Files 6% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.9680989583333333%*

 * *Differences: {"'cells'": "{3: {'execution_count': 9}, insert: [(0, OrderedDict([('cell_type', 'code'), "*

 * *            "('execution_count', 7), ('id', '0b007fe7-2ed9-40db-bf61-51ea261af252'), ('metadata', "*

 * *            "OrderedDict([('tags', [])])), ('outputs', []), ('source', ['# !pip cache purge'])])), "*

 * *            "(1, OrderedDict([('cell_type', 'code'), ('execution_count', 3), ('id', "*

 * *            "'0e658a86-9040-44e9-8588-5e26da73ecd1'), ('metadata', OrderedDict([('tags', [])])), "*

 * *            "('outputs', []), ('so […]*

```diff
@@ -1,23 +1,71 @@
 {
     "cells": [
         {
             "cell_type": "code",
-            "execution_count": null,
+            "execution_count": 7,
+            "id": "0b007fe7-2ed9-40db-bf61-51ea261af252",
+            "metadata": {
+                "tags": []
+            },
+            "outputs": [],
+            "source": [
+                "# !pip cache purge"
+            ]
+        },
+        {
+            "cell_type": "code",
+            "execution_count": 3,
+            "id": "0e658a86-9040-44e9-8588-5e26da73ecd1",
+            "metadata": {
+                "tags": []
+            },
+            "outputs": [],
+            "source": [
+                "# !pip install scikit-learn==0.24.2"
+            ]
+        },
+        {
+            "cell_type": "code",
+            "execution_count": 11,
+            "id": "376ea717-8359-45fe-b886-914a8f17bfc0",
+            "metadata": {
+                "tags": []
+            },
+            "outputs": [],
+            "source": [
+                "# !pip install --upgrade pip setuptools"
+            ]
+        },
+        {
+            "cell_type": "code",
+            "execution_count": 9,
             "id": "dd5fb77f",
             "metadata": {
                 "tags": []
             },
             "outputs": [],
             "source": [
                 "# !pip install datahelp"
             ]
         },
         {
             "cell_type": "code",
+            "execution_count": 4,
+            "id": "3bff47de-1244-4013-a0d4-5e2eba221a9d",
+            "metadata": {
+                "tags": []
+            },
+            "outputs": [],
+            "source": [
+                "# !pip install --upgrade pip"
+            ]
+        },
+        {
+            "cell_type": "code",
             "execution_count": 2,
             "id": "b0aa4d5a-254e-4190-8871-e83bd0448b44",
             "metadata": {
                 "tags": []
             },
             "outputs": [],
             "source": [
```

### Comparing `datahelp-0.1.3/datahelp/examples/data/iris.csv` & `datahelp-0.1.4/datahelp/examples/data/iris.csv`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.3/datahelp/examples/ex1.py` & `datahelp-0.1.4/datahelp/examples/ex1.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.3/datahelp/examples/ex3.ipynb` & `datahelp-0.1.4/datahelp/examples/ex3.ipynb`

 * *Files 12% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.9680989583333333%*

 * *Differences: {"'cells'": "{3: {'execution_count': 15}, insert: [(0, OrderedDict([('cell_type', 'code'), "*

 * *            "('execution_count', 7), ('id', '0b007fe7-2ed9-40db-bf61-51ea261af252'), ('metadata', "*

 * *            "OrderedDict([('tags', [])])), ('outputs', []), ('source', ['# !pip cache purge'])])), "*

 * *            "(1, OrderedDict([('cell_type', 'code'), ('execution_count', 13), ('id', "*

 * *            "'0e658a86-9040-44e9-8588-5e26da73ecd1'), ('metadata', OrderedDict([('tags', [])])), "*

 * *            "('outputs', []), (' […]*

```diff
@@ -1,23 +1,80 @@
 {
     "cells": [
         {
             "cell_type": "code",
-            "execution_count": null,
+            "execution_count": 7,
+            "id": "0b007fe7-2ed9-40db-bf61-51ea261af252",
+            "metadata": {
+                "tags": []
+            },
+            "outputs": [],
+            "source": [
+                "# !pip cache purge"
+            ]
+        },
+        {
+            "cell_type": "code",
+            "execution_count": 13,
+            "id": "0e658a86-9040-44e9-8588-5e26da73ecd1",
+            "metadata": {
+                "tags": []
+            },
+            "outputs": [],
+            "source": [
+                "# !pip install scikit-learn"
+            ]
+        },
+        {
+            "cell_type": "code",
+            "execution_count": 11,
+            "id": "376ea717-8359-45fe-b886-914a8f17bfc0",
+            "metadata": {
+                "tags": []
+            },
+            "outputs": [],
+            "source": [
+                "# !pip install --upgrade pip setuptools"
+            ]
+        },
+        {
+            "cell_type": "code",
+            "execution_count": 15,
             "id": "dd5fb77f",
             "metadata": {
                 "tags": []
             },
             "outputs": [],
             "source": [
                 "# !pip install datahelp"
             ]
         },
         {
             "cell_type": "code",
+            "execution_count": 16,
+            "id": "3bff47de-1244-4013-a0d4-5e2eba221a9d",
+            "metadata": {
+                "tags": []
+            },
+            "outputs": [
+                {
+                    "name": "stdout",
+                    "output_type": "stream",
+                    "text": [
+                        "1.2.2\n"
+                    ]
+                }
+            ],
+            "source": [
+                "import sklearn\n",
+                "print(sklearn.__version__)"
+            ]
+        },
+        {
+            "cell_type": "code",
             "execution_count": 2,
             "id": "b0aa4d5a-254e-4190-8871-e83bd0448b44",
             "metadata": {
                 "tags": []
             },
             "outputs": [],
             "source": [
```

### Comparing `datahelp-0.1.3/datahelp/feature_engineering.py` & `datahelp-0.1.4/datahelp/feature_engineering.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.3/datahelp/modelling.py` & `datahelp-0.1.4/datahelp/modelling.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.3/datahelp/utils.py` & `datahelp-0.1.4/datahelp/utils.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.3/datahelp/visualize.py` & `datahelp-0.1.4/datahelp/visualize.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.3/pyproject.toml` & `datahelp-0.1.4/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["poetry-core>=1.1.0"]
 build-backend = "poetry.core.masonry.api"
 
 [tool.poetry]
 name = "datahelp"
-version = "0.1.3"
+version = "0.1.4"
 description = "Data science library for data science / data analysis teams"
 authors = ["Meshack Kitonga <dev.kitonga@gmail.com>"]
 license = "MIT"
 homepage = "https://github.com/kimxons/datahelp"
 repository = "https://github.com/kimxons/datahelp.git"
 readme = "README.md"
 keywords = ["data", "science", "data analysis", "library", "machine learning"]
@@ -17,15 +17,15 @@
     "Intended Audience :: Developers",
     "License :: OSI Approved :: MIT License",
     "Programming Language :: Python :: 3.10",
 ]
 
 [tool.poetry.dependencies]
 pandas = "^1.3.3"
-scikit-learn = "^0.24.2"
+scikit-learn = "^1.2.2"
 seaborn = "^0.11.2"
 numpy = "^1.21.2"
 jupyter = "^1.0.0"
 matplotlib = "^3.4.3"
 nltk = "^3.6.4"
 joblib = "^1.0.1"
```

### Comparing `datahelp-0.1.3/PKG-INFO` & `datahelp-0.1.4/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: datahelp
-Version: 0.1.3
+Version: 0.1.4
 Summary: Data science library for data science / data analysis teams
 Home-page: https://github.com/kimxons/datahelp
 License: MIT
 Keywords: data,science,data analysis,library,machine learning
 Author: Meshack Kitonga
 Author-email: dev.kitonga@gmail.com
 Classifier: Development Status :: 3 - Alpha
@@ -23,15 +23,15 @@
 Classifier: Programming Language :: Python :: 3.11
 Requires-Dist: joblib (>=1.0.1,<2.0.0)
 Requires-Dist: jupyter (>=1.0.0,<2.0.0)
 Requires-Dist: matplotlib (>=3.4.3,<4.0.0)
 Requires-Dist: nltk (>=3.6.4,<4.0.0)
 Requires-Dist: numpy (>=1.21.2,<2.0.0)
 Requires-Dist: pandas (>=1.3.3,<2.0.0)
-Requires-Dist: scikit-learn (>=0.24.2,<0.25.0)
+Requires-Dist: scikit-learn (>=1.2.2,<2.0.0)
 Requires-Dist: seaborn (>=0.11.2,<0.12.0)
 Project-URL: Repository, https://github.com/kimxons/datahelp.git
 Description-Content-Type: text/markdown
 
 # datahelp
 
 datahelp is a Python library designed to assist data science and data analysis teams in their workflow. It provides various utility functions and tools to streamline common data science tasks.
```

