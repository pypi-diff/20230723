# Comparing `tmp/datahelp-0.1.4.tar.gz` & `tmp/datahelp-0.1.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "datahelp-0.1.4.tar", max compression
+gzip compressed data, was "datahelp-0.1.5.tar", max compression
```

## Comparing `datahelp-0.1.4.tar` & `datahelp-0.1.5.tar`

### file list

```diff
@@ -1,16 +1,16 @@
--rw-r--r--   0        0        0     1067 2023-07-19 21:51:44.526819 datahelp-0.1.4/LICENSE.txt
--rw-r--r--   0        0        0     3277 2023-07-23 15:57:07.399162 datahelp-0.1.4/README.md
--rw-r--r--   0        0        0        0 2023-04-26 07:38:28.009704 datahelp-0.1.4/datahelp/.editorconfig
--rw-r--r--   0        0        0       22 2023-07-23 18:19:57.047105 datahelp-0.1.4/datahelp/__init__.py
--rw-r--r--   0        0        0     4634 2023-07-23 15:41:42.769384 datahelp-0.1.4/datahelp/create_project.py
--rw-r--r--   0        0        0     7813 2023-07-23 00:03:38.918086 datahelp-0.1.4/datahelp/eda.py
--rw-r--r--   0        0        0     8091 2023-07-23 18:17:38.917137 datahelp-0.1.4/datahelp/examples/.ipynb_checkpoints/ex3-checkpoint.ipynb
--rw-r--r--   0        0        0     3858 2023-05-01 16:01:21.804048 datahelp-0.1.4/datahelp/examples/data/iris.csv
--rw-r--r--   0        0        0     1755 2023-07-22 21:56:39.608845 datahelp-0.1.4/datahelp/examples/ex1.py
--rw-r--r--   0        0        0     8215 2023-07-23 18:19:39.357109 datahelp-0.1.4/datahelp/examples/ex3.ipynb
--rw-r--r--   0        0        0     5003 2023-07-22 22:04:55.078795 datahelp-0.1.4/datahelp/feature_engineering.py
--rw-r--r--   0        0        0     4231 2023-07-22 22:00:28.688823 datahelp-0.1.4/datahelp/modelling.py
--rw-r--r--   0        0        0     1042 2023-07-22 23:17:03.308364 datahelp-0.1.4/datahelp/utils.py
--rw-r--r--   0        0        0      745 2023-07-19 21:38:45.626915 datahelp-0.1.4/datahelp/visualize.py
--rw-r--r--   0        0        0      940 2023-07-23 18:19:53.757106 datahelp-0.1.4/pyproject.toml
--rw-r--r--   0        0        0     4633 1970-01-01 00:00:00.000000 datahelp-0.1.4/PKG-INFO
+-rw-r--r--   0        0        0     1067 2023-07-19 21:51:44.526819 datahelp-0.1.5/LICENSE.txt
+-rw-r--r--   0        0        0     3277 2023-07-23 15:57:07.399162 datahelp-0.1.5/README.md
+-rw-r--r--   0        0        0        0 2023-04-26 07:38:28.009704 datahelp-0.1.5/datahelp/.editorconfig
+-rw-r--r--   0        0        0       22 2023-07-23 18:25:01.357035 datahelp-0.1.5/datahelp/__init__.py
+-rw-r--r--   0        0        0     4634 2023-07-23 15:41:42.769384 datahelp-0.1.5/datahelp/create_project.py
+-rw-r--r--   0        0        0     7813 2023-07-23 00:03:38.918086 datahelp-0.1.5/datahelp/eda.py
+-rw-r--r--   0        0        0     8215 2023-07-23 18:22:48.157069 datahelp-0.1.5/datahelp/examples/.ipynb_checkpoints/ex3-checkpoint.ipynb
+-rw-r--r--   0        0        0     3858 2023-05-01 16:01:21.804048 datahelp-0.1.5/datahelp/examples/data/iris.csv
+-rw-r--r--   0        0        0     1755 2023-07-22 21:56:39.608845 datahelp-0.1.5/datahelp/examples/ex1.py
+-rw-r--r--   0        0        0    10080 2023-07-23 18:24:48.367038 datahelp-0.1.5/datahelp/examples/ex3.ipynb
+-rw-r--r--   0        0        0     5003 2023-07-22 22:04:55.078795 datahelp-0.1.5/datahelp/feature_engineering.py
+-rw-r--r--   0        0        0     4231 2023-07-22 22:00:28.688823 datahelp-0.1.5/datahelp/modelling.py
+-rw-r--r--   0        0        0     1042 2023-07-22 23:17:03.308364 datahelp-0.1.5/datahelp/utils.py
+-rw-r--r--   0        0        0      745 2023-07-19 21:38:45.626915 datahelp-0.1.5/datahelp/visualize.py
+-rw-r--r--   0        0        0      932 2023-07-23 18:24:56.537036 datahelp-0.1.5/pyproject.toml
+-rw-r--r--   0        0        0     4576 1970-01-01 00:00:00.000000 datahelp-0.1.5/PKG-INFO
```

### Comparing `datahelp-0.1.4/LICENSE.txt` & `datahelp-0.1.5/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.4/README.md` & `datahelp-0.1.5/README.md`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.4/datahelp/create_project.py` & `datahelp-0.1.5/datahelp/create_project.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.4/datahelp/eda.py` & `datahelp-0.1.5/datahelp/eda.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.4/datahelp/examples/.ipynb_checkpoints/ex3-checkpoint.ipynb` & `datahelp-0.1.5/datahelp/examples/.ipynb_checkpoints/ex3-checkpoint.ipynb`

 * *Files 2% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.99609375%*

 * *Differences: {"'cells'": "{1: {'execution_count': 13, 'source': ['# !pip install scikit-learn']}, 3: "*

 * *            "{'execution_count': 18}, 4: {'execution_count': 16, 'outputs': [OrderedDict([('name', "*

 * *            "'stdout'), ('output_type', 'stream'), ('text', ['1.2.2\\n'])])], 'source': ['import "*

 * *            "sklearn\\n', 'print(sklearn.__version__)']}}"}*

```diff
@@ -10,22 +10,22 @@
             "outputs": [],
             "source": [
                 "# !pip cache purge"
             ]
         },
         {
             "cell_type": "code",
-            "execution_count": 3,
+            "execution_count": 13,
             "id": "0e658a86-9040-44e9-8588-5e26da73ecd1",
             "metadata": {
                 "tags": []
             },
             "outputs": [],
             "source": [
-                "# !pip install scikit-learn==0.24.2"
+                "# !pip install scikit-learn"
             ]
         },
         {
             "cell_type": "code",
             "execution_count": 11,
             "id": "376ea717-8359-45fe-b886-914a8f17bfc0",
             "metadata": {
@@ -34,34 +34,43 @@
             "outputs": [],
             "source": [
                 "# !pip install --upgrade pip setuptools"
             ]
         },
         {
             "cell_type": "code",
-            "execution_count": 9,
+            "execution_count": 18,
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
-            "execution_count": 4,
+            "execution_count": 16,
             "id": "3bff47de-1244-4013-a0d4-5e2eba221a9d",
             "metadata": {
                 "tags": []
             },
-            "outputs": [],
+            "outputs": [
+                {
+                    "name": "stdout",
+                    "output_type": "stream",
+                    "text": [
+                        "1.2.2\n"
+                    ]
+                }
+            ],
             "source": [
-                "# !pip install --upgrade pip"
+                "import sklearn\n",
+                "print(sklearn.__version__)"
             ]
         },
         {
             "cell_type": "code",
             "execution_count": 2,
             "id": "b0aa4d5a-254e-4190-8871-e83bd0448b44",
             "metadata": {
```

### Comparing `datahelp-0.1.4/datahelp/examples/data/iris.csv` & `datahelp-0.1.5/datahelp/examples/data/iris.csv`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.4/datahelp/examples/ex1.py` & `datahelp-0.1.5/datahelp/examples/ex1.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.4/datahelp/examples/ex3.ipynb` & `datahelp-0.1.5/datahelp/examples/ex3.ipynb`

 * *Files 13% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.9920343137254902%*

 * *Differences: {"'cells'": "{4: {'execution_count': 18}, insert: [(2, OrderedDict([('cell_type', 'code'), "*

 * *            "('execution_count', None), ('id', 'ce382fdc-8f80-4ef4-bf4e-8e729fe2aac0'), "*

 * *            "('metadata', OrderedDict([('tags', [])])), ('outputs', [OrderedDict([('name', "*

 * *            "'stdout'), ('output_type', 'stream'), ('text', ['Defaulting to user installation "*

 * *            "because normal site-packages is not writeable\\n', 'Requirement already satisfied: "*

 * *            "scikit-learn in /home/shak/.l […]*

```diff
@@ -22,27 +22,57 @@
             "outputs": [],
             "source": [
                 "# !pip install scikit-learn"
             ]
         },
         {
             "cell_type": "code",
+            "execution_count": null,
+            "id": "ce382fdc-8f80-4ef4-bf4e-8e729fe2aac0",
+            "metadata": {
+                "tags": []
+            },
+            "outputs": [
+                {
+                    "name": "stdout",
+                    "output_type": "stream",
+                    "text": [
+                        "Defaulting to user installation because normal site-packages is not writeable\n",
+                        "Requirement already satisfied: scikit-learn in /home/shak/.local/lib/python3.10/site-packages (1.2.2)\n",
+                        "Collecting scikit-learn\n",
+                        "  Obtaining dependency information for scikit-learn from https://files.pythonhosted.org/packages/5c/e9/ee572691a3fb05555bcde41826faad29ae4bc1fb07982e7f53d54a176879/scikit_learn-1.3.0-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata\n",
+                        "  Downloading scikit_learn-1.3.0-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (11 kB)\n",
+                        "Requirement already satisfied: numpy>=1.17.3 in /home/shak/.local/lib/python3.10/site-packages (from scikit-learn) (1.23.5)\n",
+                        "Requirement already satisfied: scipy>=1.5.0 in /usr/lib/python3/dist-packages (from scikit-learn) (1.8.0)\n",
+                        "Requirement already satisfied: joblib>=1.1.1 in /home/shak/.local/lib/python3.10/site-packages (from scikit-learn) (1.2.0)\n",
+                        "Requirement already satisfied: threadpoolctl>=2.0.0 in /home/shak/.local/lib/python3.10/site-packages (from scikit-learn) (3.1.0)\n",
+                        "Downloading scikit_learn-1.3.0-cp310-cp310-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (10.8 MB)\n",
+                        "\u001b[2K   \u001b[91m\u2501\u2501\u2501\u2501\u2501\u2501\u2501\u2501\u2501\u2501\u2501\u2501\u2501\u2501\u2501\u2501\u2501\u001b[0m\u001b[91m\u2578\u001b[0m\u001b[90m\u2501\u2501\u2501\u2501\u2501\u2501\u2501\u2501\u2501\u2501\u2501\u2501\u2501\u2501\u2501\u2501\u2501\u2501\u2501\u2501\u2501\u2501\u001b[0m \u001b[32m4.8/10.8 MB\u001b[0m \u001b[31m87.1 kB/s\u001b[0m eta \u001b[36m0:01:09\u001b[0m"
+                    ]
+                }
+            ],
+            "source": [
+                "!pip install --upgrade scikit-learn"
+            ]
+        },
+        {
+            "cell_type": "code",
             "execution_count": 11,
             "id": "376ea717-8359-45fe-b886-914a8f17bfc0",
             "metadata": {
                 "tags": []
             },
             "outputs": [],
             "source": [
                 "# !pip install --upgrade pip setuptools"
             ]
         },
         {
             "cell_type": "code",
-            "execution_count": 15,
+            "execution_count": 18,
             "id": "dd5fb77f",
             "metadata": {
                 "tags": []
             },
             "outputs": [],
             "source": [
                 "# !pip install datahelp"
```

### Comparing `datahelp-0.1.4/datahelp/feature_engineering.py` & `datahelp-0.1.5/datahelp/feature_engineering.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.4/datahelp/modelling.py` & `datahelp-0.1.5/datahelp/modelling.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.4/datahelp/utils.py` & `datahelp-0.1.5/datahelp/utils.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.4/datahelp/visualize.py` & `datahelp-0.1.5/datahelp/visualize.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.4/PKG-INFO` & `datahelp-0.1.5/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: datahelp
-Version: 0.1.4
+Version: 0.1.5
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
-Requires-Dist: joblib (>=1.0.1,<2.0.0)
-Requires-Dist: jupyter (>=1.0.0,<2.0.0)
-Requires-Dist: matplotlib (>=3.4.3,<4.0.0)
-Requires-Dist: nltk (>=3.6.4,<4.0.0)
-Requires-Dist: numpy (>=1.21.2,<2.0.0)
-Requires-Dist: pandas (>=1.3.3,<2.0.0)
-Requires-Dist: scikit-learn (>=1.2.2,<2.0.0)
-Requires-Dist: seaborn (>=0.11.2,<0.12.0)
+Requires-Dist: joblib (==1.0.1)
+Requires-Dist: jupyter (==1.0.0)
+Requires-Dist: matplotlib (==3.4.3)
+Requires-Dist: nltk (==3.6.4)
+Requires-Dist: numpy (==1.21.2)
+Requires-Dist: pandas (==1.3.3)
+Requires-Dist: scikit-learn (==1.2.2)
+Requires-Dist: seaborn (==0.11.2)
 Project-URL: Repository, https://github.com/kimxons/datahelp.git
 Description-Content-Type: text/markdown
 
 # datahelp
 
 datahelp is a Python library designed to assist data science and data analysis teams in their workflow. It provides various utility functions and tools to streamline common data science tasks.
```

