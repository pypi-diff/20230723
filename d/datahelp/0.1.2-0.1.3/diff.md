# Comparing `tmp/datahelp-0.1.2.tar.gz` & `tmp/datahelp-0.1.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "datahelp-0.1.2.tar", max compression
+gzip compressed data, was "datahelp-0.1.3.tar", max compression
```

## Comparing `datahelp-0.1.2.tar` & `datahelp-0.1.3.tar`

### file list

```diff
@@ -1,17 +1,16 @@
--rw-r--r--   0        0        0     1067 2023-07-19 21:51:44.526819 datahelp-0.1.2/LICENSE.txt
--rw-r--r--   0        0        0     3277 2023-07-23 15:57:07.399162 datahelp-0.1.2/README.md
--rw-r--r--   0        0        0        0 2023-04-26 07:38:28.009704 datahelp-0.1.2/datahelp/.editorconfig
--rw-r--r--   0        0        0       22 2023-07-23 16:22:15.388803 datahelp-0.1.2/datahelp/__init__.py
--rw-r--r--   0        0        0     4634 2023-07-23 15:41:42.769384 datahelp-0.1.2/datahelp/create_project.py
--rw-r--r--   0        0        0     7813 2023-07-23 00:03:38.918086 datahelp-0.1.2/datahelp/eda.py
--rw-r--r--   0        0        0     9791 2023-07-23 15:41:42.769384 datahelp-0.1.2/datahelp/examples/.ipynb_checkpoints/ex3-checkpoint.ipynb
--rw-r--r--   0        0        0     3858 2023-05-01 16:01:21.804048 datahelp-0.1.2/datahelp/examples/data/iris.csv
--rw-r--r--   0        0        0     1755 2023-07-22 21:56:39.608845 datahelp-0.1.2/datahelp/examples/ex1.py
--rw-r--r--   0        0        0     2112 2023-07-22 22:15:12.288732 datahelp-0.1.2/datahelp/examples/ex2.py
--rw-r--r--   0        0        0     8705 2023-07-23 16:22:03.338806 datahelp-0.1.2/datahelp/examples/ex3.ipynb
--rw-r--r--   0        0        0     5003 2023-07-22 22:04:55.078795 datahelp-0.1.2/datahelp/feature_engineering.py
--rw-r--r--   0        0        0     4231 2023-07-22 22:00:28.688823 datahelp-0.1.2/datahelp/modelling.py
--rw-r--r--   0        0        0     1042 2023-07-22 23:17:03.308364 datahelp-0.1.2/datahelp/utils.py
--rw-r--r--   0        0        0      745 2023-07-19 21:38:45.626915 datahelp-0.1.2/datahelp/visualize.py
--rw-r--r--   0        0        0      938 2023-07-23 16:22:10.818804 datahelp-0.1.2/pyproject.toml
--rw-r--r--   0        0        0     4635 1970-01-01 00:00:00.000000 datahelp-0.1.2/PKG-INFO
+-rw-r--r--   0        0        0     1067 2023-07-19 21:51:44.526819 datahelp-0.1.3/LICENSE.txt
+-rw-r--r--   0        0        0     3277 2023-07-23 15:57:07.399162 datahelp-0.1.3/README.md
+-rw-r--r--   0        0        0        0 2023-04-26 07:38:28.009704 datahelp-0.1.3/datahelp/.editorconfig
+-rw-r--r--   0        0        0       22 2023-07-23 17:30:13.327828 datahelp-0.1.3/datahelp/__init__.py
+-rw-r--r--   0        0        0     4634 2023-07-23 15:41:42.769384 datahelp-0.1.3/datahelp/create_project.py
+-rw-r--r--   0        0        0     7813 2023-07-23 00:03:38.918086 datahelp-0.1.3/datahelp/eda.py
+-rw-r--r--   0        0        0     7213 2023-07-23 16:35:21.498616 datahelp-0.1.3/datahelp/examples/.ipynb_checkpoints/ex3-checkpoint.ipynb
+-rw-r--r--   0        0        0     3858 2023-05-01 16:01:21.804048 datahelp-0.1.3/datahelp/examples/data/iris.csv
+-rw-r--r--   0        0        0     1755 2023-07-22 21:56:39.608845 datahelp-0.1.3/datahelp/examples/ex1.py
+-rw-r--r--   0        0        0     7213 2023-07-23 16:35:21.498616 datahelp-0.1.3/datahelp/examples/ex3.ipynb
+-rw-r--r--   0        0        0     5003 2023-07-22 22:04:55.078795 datahelp-0.1.3/datahelp/feature_engineering.py
+-rw-r--r--   0        0        0     4231 2023-07-22 22:00:28.688823 datahelp-0.1.3/datahelp/modelling.py
+-rw-r--r--   0        0        0     1042 2023-07-22 23:17:03.308364 datahelp-0.1.3/datahelp/utils.py
+-rw-r--r--   0        0        0      745 2023-07-19 21:38:45.626915 datahelp-0.1.3/datahelp/visualize.py
+-rw-r--r--   0        0        0      941 2023-07-23 17:30:03.877829 datahelp-0.1.3/pyproject.toml
+-rw-r--r--   0        0        0     4635 1970-01-01 00:00:00.000000 datahelp-0.1.3/PKG-INFO
```

### Comparing `datahelp-0.1.2/LICENSE.txt` & `datahelp-0.1.3/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.2/README.md` & `datahelp-0.1.3/README.md`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.2/datahelp/create_project.py` & `datahelp-0.1.3/datahelp/create_project.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.2/datahelp/eda.py` & `datahelp-0.1.3/datahelp/eda.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.2/datahelp/examples/.ipynb_checkpoints/ex3-checkpoint.ipynb` & `datahelp-0.1.3/datahelp/examples/.ipynb_checkpoints/ex3-checkpoint.ipynb`

 * *Files 24% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.9791332799145299%*

 * *Differences: {"'cells'": "{0: {'source': ['# !pip install datahelp']}, 1: {'execution_count': 2}, 2: "*

 * *            "{'execution_count': 3}, 3: {'execution_count': 4}, 4: {'execution_count': 5, "*

 * *            "'outputs': {0: {'execution_count': 5}}}, 5: {'execution_count': 6}, 6: "*

 * *            "{'execution_count': 7, 'outputs': {0: {'output_type': 'error', 'ename': "*

 * *            '\'AttributeError\', \'evalue\': "module \'datahelp\' has no attribute \'eda\'", '*

 * *            "'traceback': "*

 * *            "['\\x1b[0;31m-------- […]*

```diff
@@ -5,33 +5,33 @@
             "execution_count": null,
             "id": "dd5fb77f",
             "metadata": {
                 "tags": []
             },
             "outputs": [],
             "source": [
-                "!pip install datahelp==0.1.3"
+                "# !pip install datahelp"
             ]
         },
         {
             "cell_type": "code",
-            "execution_count": 4,
+            "execution_count": 2,
             "id": "b0aa4d5a-254e-4190-8871-e83bd0448b44",
             "metadata": {
                 "tags": []
             },
             "outputs": [],
             "source": [
                 "import datahelp as dh\n",
                 "import pkgutil"
             ]
         },
         {
             "cell_type": "code",
-            "execution_count": 5,
+            "execution_count": 3,
             "id": "0b15e2ec-4289-4f6b-890b-3f57ad16865c",
             "metadata": {
                 "tags": []
             },
             "outputs": [],
             "source": [
                 "import pandas as pd\n",
@@ -39,27 +39,27 @@
                 "from sklearn.ensemble import RandomForestClassifier\n",
                 "from sklearn.model_selection import train_test_split\n",
                 "from sklearn.metrics import accuracy_score"
             ]
         },
         {
             "cell_type": "code",
-            "execution_count": 6,
+            "execution_count": 4,
             "id": "226ff8a0",
             "metadata": {
                 "tags": []
             },
             "outputs": [],
             "source": [
                 "df = pd.read_csv(\"data/iris.csv\")"
             ]
         },
         {
             "cell_type": "code",
-            "execution_count": 7,
+            "execution_count": 5,
             "id": "86af443d",
             "metadata": {
                 "tags": []
             },
             "outputs": [
                 {
                     "data": {
@@ -139,26 +139,26 @@
                             "0           5.1          3.5           1.4          0.2  setosa\n",
                             "1           4.9          3.0           1.4          0.2  setosa\n",
                             "2           4.7          3.2           1.3          0.2  setosa\n",
                             "3           4.6          3.1           1.5          0.2  setosa\n",
                             "4           5.0          3.6           1.4          0.2  setosa"
                         ]
                     },
-                    "execution_count": 7,
+                    "execution_count": 5,
                     "metadata": {},
                     "output_type": "execute_result"
                 }
             ],
             "source": [
                 "df.head()"
             ]
         },
         {
             "cell_type": "code",
-            "execution_count": 8,
+            "execution_count": 6,
             "id": "1a47bd06-58cc-4e29-aa1e-1e59b571e51f",
             "metadata": {
                 "tags": []
             },
             "outputs": [
                 {
                     "name": "stdout",
@@ -171,201 +171,71 @@
             "source": [
                 "modules_list = [name for _, name, _ in pkgutil.iter_modules(dh.__path__)]\n",
                 "print(modules_list)"
             ]
         },
         {
             "cell_type": "code",
-            "execution_count": 9,
-            "id": "844b66ba-381a-4b74-828b-b68ca45f4861",
-            "metadata": {
-                "tags": []
-            },
-            "outputs": [],
-            "source": [
-                "from datahelp import eda"
-            ]
-        },
-        {
-            "cell_type": "code",
-            "execution_count": 10,
+            "execution_count": 7,
             "id": "9cd0961d-500e-4894-b8ab-2e6c98fd87ae",
             "metadata": {
                 "tags": []
             },
             "outputs": [
                 {
-                    "name": "stdout",
-                    "output_type": "stream",
-                    "text": [
-                        "['species']\n"
+                    "ename": "AttributeError",
+                    "evalue": "module 'datahelp' has no attribute 'eda'",
+                    "output_type": "error",
+                    "traceback": [
+                        "\u001b[0;31m---------------------------------------------------------------------------\u001b[0m",
+                        "\u001b[0;31mAttributeError\u001b[0m                            Traceback (most recent call last)",
+                        "\u001b[0;32m/tmp/ipykernel_3089/1953063358.py\u001b[0m in \u001b[0;36m<module>\u001b[0;34m\u001b[0m\n\u001b[0;32m----> 1\u001b[0;31m \u001b[0mcats\u001b[0m \u001b[0;34m=\u001b[0m \u001b[0mdh\u001b[0m\u001b[0;34m.\u001b[0m\u001b[0meda\u001b[0m\u001b[0;34m.\u001b[0m\u001b[0mget_cat_vars\u001b[0m\u001b[0;34m(\u001b[0m\u001b[0mdf\u001b[0m\u001b[0;34m)\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n\u001b[0m\u001b[1;32m      2\u001b[0m \u001b[0mprint\u001b[0m\u001b[0;34m(\u001b[0m\u001b[0mcats\u001b[0m\u001b[0;34m)\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n",
+                        "\u001b[0;31mAttributeError\u001b[0m: module 'datahelp' has no attribute 'eda'"
                     ]
                 }
             ],
             "source": [
                 "cats = dh.eda.get_cat_vars(df)\n",
                 "print(cats)"
             ]
         },
         {
             "cell_type": "code",
-            "execution_count": 11,
+            "execution_count": null,
             "id": "f51262ad-0113-404a-a303-58b76b43a41a",
             "metadata": {
                 "tags": []
             },
-            "outputs": [
-                {
-                    "name": "stdout",
-                    "output_type": "stream",
-                    "text": [
-                        "['sepal_length', 'sepal_width', 'petal_length', 'petal_width']\n"
-                    ]
-                }
-            ],
+            "outputs": [],
             "source": [
                 "num_var = dh.eda.get_num_vars(df)\n",
                 "print(num_var)"
             ]
         },
         {
             "cell_type": "code",
-            "execution_count": 12,
+            "execution_count": null,
             "id": "1467e072-c0bc-4400-9e60-fd84cead05ad",
             "metadata": {
                 "tags": []
             },
-            "outputs": [
-                {
-                    "data": {
-                        "text/html": [
-                            "<div>\n",
-                            "<style scoped>\n",
-                            "    .dataframe tbody tr th:only-of-type {\n",
-                            "        vertical-align: middle;\n",
-                            "    }\n",
-                            "\n",
-                            "    .dataframe tbody tr th {\n",
-                            "        vertical-align: top;\n",
-                            "    }\n",
-                            "\n",
-                            "    .dataframe thead th {\n",
-                            "        text-align: right;\n",
-                            "    }\n",
-                            "</style>\n",
-                            "<table border=\"1\" class=\"dataframe\">\n",
-                            "  <thead>\n",
-                            "    <tr style=\"text-align: right;\">\n",
-                            "      <th></th>\n",
-                            "      <th>Feature</th>\n",
-                            "      <th>Unique Count</th>\n",
-                            "    </tr>\n",
-                            "  </thead>\n",
-                            "  <tbody>\n",
-                            "    <tr>\n",
-                            "      <th>0</th>\n",
-                            "      <td>species</td>\n",
-                            "      <td>3</td>\n",
-                            "    </tr>\n",
-                            "  </tbody>\n",
-                            "</table>\n",
-                            "</div>"
-                        ],
-                        "text/plain": [
-                            "   Feature  Unique Count\n",
-                            "0  species             3"
-                        ]
-                    },
-                    "execution_count": 12,
-                    "metadata": {},
-                    "output_type": "execute_result"
-                }
-            ],
+            "outputs": [],
             "source": [
                 "cat_count = dh.eda.get_cat_counts(df)\n",
                 "cat_count"
             ]
         },
         {
             "cell_type": "code",
-            "execution_count": 17,
+            "execution_count": null,
             "id": "bc25acf0-19ef-4576-8559-f14db63da53a",
             "metadata": {
                 "tags": []
             },
-            "outputs": [
-                {
-                    "data": {
-                        "text/html": [
-                            "<div>\n",
-                            "<style scoped>\n",
-                            "    .dataframe tbody tr th:only-of-type {\n",
-                            "        vertical-align: middle;\n",
-                            "    }\n",
-                            "\n",
-                            "    .dataframe tbody tr th {\n",
-                            "        vertical-align: top;\n",
-                            "    }\n",
-                            "\n",
-                            "    .dataframe thead th {\n",
-                            "        text-align: right;\n",
-                            "    }\n",
-                            "</style>\n",
-                            "<table border=\"1\" class=\"dataframe\">\n",
-                            "  <thead>\n",
-                            "    <tr style=\"text-align: right;\">\n",
-                            "      <th></th>\n",
-                            "      <th>missing_count</th>\n",
-                            "      <th>missing_percent</th>\n",
-                            "    </tr>\n",
-                            "  </thead>\n",
-                            "  <tbody>\n",
-                            "    <tr>\n",
-                            "      <th>sepal_length</th>\n",
-                            "      <td>0</td>\n",
-                            "      <td>0.0</td>\n",
-                            "    </tr>\n",
-                            "    <tr>\n",
-                            "      <th>sepal_width</th>\n",
-                            "      <td>0</td>\n",
-                            "      <td>0.0</td>\n",
-                            "    </tr>\n",
-                            "    <tr>\n",
-                            "      <th>petal_length</th>\n",
-                            "      <td>0</td>\n",
-                            "      <td>0.0</td>\n",
-                            "    </tr>\n",
-                            "    <tr>\n",
-                            "      <th>petal_width</th>\n",
-                            "      <td>0</td>\n",
-                            "      <td>0.0</td>\n",
-                            "    </tr>\n",
-                            "    <tr>\n",
-                            "      <th>species</th>\n",
-                            "      <td>0</td>\n",
-                            "      <td>0.0</td>\n",
-                            "    </tr>\n",
-                            "  </tbody>\n",
-                            "</table>\n",
-                            "</div>"
-                        ],
-                        "text/plain": [
-                            "              missing_count  missing_percent\n",
-                            "sepal_length              0              0.0\n",
-                            "sepal_width               0              0.0\n",
-                            "petal_length              0              0.0\n",
-                            "petal_width               0              0.0\n",
-                            "species                   0              0.0"
-                        ]
-                    },
-                    "execution_count": 17,
-                    "metadata": {},
-                    "output_type": "execute_result"
-                }
-            ],
+            "outputs": [],
             "source": [
                 "missing = dh.eda.display_missing(df)\n",
                 "missing"
             ]
         },
         {
             "cell_type": "code",
```

### Comparing `datahelp-0.1.2/datahelp/examples/data/iris.csv` & `datahelp-0.1.3/datahelp/examples/data/iris.csv`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.2/datahelp/examples/ex1.py` & `datahelp-0.1.3/datahelp/examples/ex1.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.2/datahelp/feature_engineering.py` & `datahelp-0.1.3/datahelp/feature_engineering.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.2/datahelp/modelling.py` & `datahelp-0.1.3/datahelp/modelling.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.2/datahelp/utils.py` & `datahelp-0.1.3/datahelp/utils.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.2/datahelp/visualize.py` & `datahelp-0.1.3/datahelp/visualize.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.2/pyproject.toml` & `datahelp-0.1.3/pyproject.toml`

 * *Files 3% similar despite different names*

```diff
@@ -1,26 +1,26 @@
 [build-system]
 requires = ["poetry-core>=1.1.0"]
 build-backend = "poetry.core.masonry.api"
 
 [tool.poetry]
 name = "datahelp"
-version = "0.1.2"
+version = "0.1.3"
 description = "Data science library for data science / data analysis teams"
 authors = ["Meshack Kitonga <dev.kitonga@gmail.com>"]
 license = "MIT"
 homepage = "https://github.com/kimxons/datahelp"
 repository = "https://github.com/kimxons/datahelp.git"
 readme = "README.md"
 keywords = ["data", "science", "data analysis", "library", "machine learning"]
 classifiers = [
     "Development Status :: 3 - Alpha",
     "Intended Audience :: Developers",
     "License :: OSI Approved :: MIT License",
-    "Programming Language :: Python :: 3",
+    "Programming Language :: Python :: 3.10",
 ]
 
 [tool.poetry.dependencies]
 pandas = "^1.3.3"
 scikit-learn = "^0.24.2"
 seaborn = "^0.11.2"
 numpy = "^1.21.2"
```

### Comparing `datahelp-0.1.2/PKG-INFO` & `datahelp-0.1.3/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: datahelp
-Version: 0.1.2
+Version: 0.1.3
 Summary: Data science library for data science / data analysis teams
 Home-page: https://github.com/kimxons/datahelp
 License: MIT
 Keywords: data,science,data analysis,library,machine learning
 Author: Meshack Kitonga
 Author-email: dev.kitonga@gmail.com
 Classifier: Development Status :: 3 - Alpha
```

