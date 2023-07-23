# Comparing `tmp/datahelp-0.1.0.tar.gz` & `tmp/datahelp-0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "datahelp-0.1.0.tar", max compression
+gzip compressed data, was "datahelp-0.1.1.tar", max compression
```

## Comparing `datahelp-0.1.0.tar` & `datahelp-0.1.1.tar`

### file list

```diff
@@ -1,17 +1,17 @@
--rw-r--r--   0        0        0     1067 2023-07-19 21:51:44.526819 datahelp-0.1.0/LICENSE.txt
--rw-r--r--   0        0        0     3297 2023-07-23 15:41:42.769384 datahelp-0.1.0/README.md
--rw-r--r--   0        0        0        0 2023-04-26 07:38:28.009704 datahelp-0.1.0/datahelp/.editorconfig
--rw-r--r--   0        0        0       22 2023-07-23 00:05:10.248071 datahelp-0.1.0/datahelp/__init__.py
--rw-r--r--   0        0        0     4634 2023-07-23 15:41:42.769384 datahelp-0.1.0/datahelp/create_project.py
--rw-r--r--   0        0        0     7813 2023-07-23 00:03:38.918086 datahelp-0.1.0/datahelp/eda.py
--rw-r--r--   0        0        0     9791 2023-07-23 15:41:42.769384 datahelp-0.1.0/datahelp/examples/.ipynb_checkpoints/ex3-checkpoint.ipynb
--rw-r--r--   0        0        0     3858 2023-05-01 16:01:21.804048 datahelp-0.1.0/datahelp/examples/data/iris.csv
--rw-r--r--   0        0        0     1755 2023-07-22 21:56:39.608845 datahelp-0.1.0/datahelp/examples/ex1.py
--rw-r--r--   0        0        0     2112 2023-07-22 22:15:12.288732 datahelp-0.1.0/datahelp/examples/ex2.py
--rw-r--r--   0        0        0     7210 2023-07-23 15:41:42.769384 datahelp-0.1.0/datahelp/examples/ex3.ipynb
--rw-r--r--   0        0        0     5003 2023-07-22 22:04:55.078795 datahelp-0.1.0/datahelp/feature_engineering.py
--rw-r--r--   0        0        0     4231 2023-07-22 22:00:28.688823 datahelp-0.1.0/datahelp/modelling.py
--rw-r--r--   0        0        0     1042 2023-07-22 23:17:03.308364 datahelp-0.1.0/datahelp/utils.py
--rw-r--r--   0        0        0      745 2023-07-19 21:38:45.626915 datahelp-0.1.0/datahelp/visualize.py
--rw-r--r--   0        0        0     1181 2023-07-23 15:36:37.149463 datahelp-0.1.0/pyproject.toml
--rw-r--r--   0        0        0     4480 1970-01-01 00:00:00.000000 datahelp-0.1.0/PKG-INFO
+-rw-r--r--   0        0        0     1067 2023-07-19 21:51:44.526819 datahelp-0.1.1/LICENSE.txt
+-rw-r--r--   0        0        0     3277 2023-07-23 15:57:07.399162 datahelp-0.1.1/README.md
+-rw-r--r--   0        0        0        0 2023-04-26 07:38:28.009704 datahelp-0.1.1/datahelp/.editorconfig
+-rw-r--r--   0        0        0       22 2023-07-23 16:17:58.108865 datahelp-0.1.1/datahelp/__init__.py
+-rw-r--r--   0        0        0     4634 2023-07-23 15:41:42.769384 datahelp-0.1.1/datahelp/create_project.py
+-rw-r--r--   0        0        0     7813 2023-07-23 00:03:38.918086 datahelp-0.1.1/datahelp/eda.py
+-rw-r--r--   0        0        0     9791 2023-07-23 15:41:42.769384 datahelp-0.1.1/datahelp/examples/.ipynb_checkpoints/ex3-checkpoint.ipynb
+-rw-r--r--   0        0        0     3858 2023-05-01 16:01:21.804048 datahelp-0.1.1/datahelp/examples/data/iris.csv
+-rw-r--r--   0        0        0     1755 2023-07-22 21:56:39.608845 datahelp-0.1.1/datahelp/examples/ex1.py
+-rw-r--r--   0        0        0     2112 2023-07-22 22:15:12.288732 datahelp-0.1.1/datahelp/examples/ex2.py
+-rw-r--r--   0        0        0  2933835 2023-07-23 16:16:00.458892 datahelp-0.1.1/datahelp/examples/ex3.ipynb
+-rw-r--r--   0        0        0     5003 2023-07-22 22:04:55.078795 datahelp-0.1.1/datahelp/feature_engineering.py
+-rw-r--r--   0        0        0     4231 2023-07-22 22:00:28.688823 datahelp-0.1.1/datahelp/modelling.py
+-rw-r--r--   0        0        0     1042 2023-07-22 23:17:03.308364 datahelp-0.1.1/datahelp/utils.py
+-rw-r--r--   0        0        0      745 2023-07-19 21:38:45.626915 datahelp-0.1.1/datahelp/visualize.py
+-rw-r--r--   0        0        0      955 2023-07-23 16:17:44.638867 datahelp-0.1.1/pyproject.toml
+-rw-r--r--   0        0        0     4460 1970-01-01 00:00:00.000000 datahelp-0.1.1/PKG-INFO
```

### Comparing `datahelp-0.1.0/LICENSE.txt` & `datahelp-0.1.1/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.0/README.md` & `datahelp-0.1.1/README.md`

 * *Files 23% similar despite different names*

```diff
@@ -1,30 +1,30 @@
-# Data-Help
+# datahelp
 
-Data-Help is a Python library designed to assist data science and data analysis teams in their workflow. It provides various utility functions and tools to streamline common data science tasks.
+datahelp is a Python library designed to assist data science and data analysis teams in their workflow. It provides various utility functions and tools to streamline common data science tasks.
 
 ## Features
 
-Data-Help offers the following key features:
+datahelp offers the following key features:
 
-1. **Project Management:** Data-Help simplifies the creation of standard data science project structures. With a single function call, you can generate a well-organized project directory with predefined folders for datasets, processed data, raw data, outputs, models, scripts, notebooks, and more.
+1. **Project Management:** datahelp simplifies the creation of standard data science project structures. With a single function call, you can generate a well-organized project directory with predefined folders for datasets, processed data, raw data, outputs, models, scripts, notebooks, and more.
 
-2. **Model Saving and Loading:** Data-Help provides easy-to-use functions for saving and loading trained machine learning models. It supports various formats such as joblib, pickle, and keras, enabling seamless integration with different model types.
+2. **Model Saving and Loading:** datahelp provides easy-to-use functions for saving and loading trained machine learning models. It supports various formats such as joblib, pickle, and keras, enabling seamless integration with different model types.
 
 3. **Data Exploration and Visualization:** The library includes functions for data exploration, summary statistics, and visualization. You can quickly generate feature importances plots and visualize missing data to gain insights into your datasets.
 
-4. **Feature Engineering:** Data-Help includes methods for handling missing data and noise in your datasets. It offers functions for dropping missing columns based on a specified threshold and detecting outliers using Tukey's Interquartile Range (IQR) method.
+4. **Feature Engineering:** datahelp includes methods for handling missing data and noise in your datasets. It offers functions for dropping missing columns based on a specified threshold and detecting outliers using Tukey's Interquartile Range (IQR) method.
 
-5. **Model Evaluation and Cross-Validation:** Data-Help provides tools to evaluate model performance, including functions to calculate accuracy, F1-score, precision, recall, and generate classification reports. It also supports cross-validation for model evaluation.
+5. **Model Evaluation and Cross-Validation:** datahelp provides tools to evaluate model performance, including functions to calculate accuracy, F1-score, precision, recall, and generate classification reports. It also supports cross-validation for model evaluation.
 
 6. **Scaling and Normalization:** The library offers functions for min-max scaling and z-score normalization of data to bring features to a common scale.
 
 ## Getting Started
 
-To use Data-Help in your data science projects, you can install it via pip:
+To use datahelp in your data science projects, you can install it via pip:
 
 ```bash
 pip install datahelp
 ```
 
 Once installed, you can import the library and explore its functionality:
 
@@ -46,20 +46,20 @@
 
 missing = dh.eda.display_missing(df)
 missing
 ```
 
 ## Documentation
 
-For detailed usage instructions and API reference, please refer to the official documentation at [https://data-help-docs.example.com](https://data-help-docs.example.com)
+For detailed usage instructions and API reference, please refer to the official documentation at [https://datahelp-docs.example.com](https://datahelp-docs.example.com)
 
 ## Contribution
 
-Data-Help is an open-source project, and we welcome contributions from the data science community. If you find a bug, have a feature request, or want to contribute improvements, please open an issue or submit a pull request on our GitHub repository at [https://github.com/data-help/data-help](https://github.com/data-help/data-help).
+datahelp is an open-source project, and we welcome contributions from the data science community. If you find a bug, have a feature request, or want to contribute improvements, please open an issue or submit a pull request on our GitHub repository at [https://github.com/datahelp/datahelp](https://github.com/datahelp/datahelp).
 
 ## License
 
-Data-Help is licensed under the MIT License. See the [LICENSE](https://github.com/data-help/data-help/blob/main/LICENSE) file for more details.
+datahelp is licensed under the MIT License. See the [LICENSE](https://github.com/datahelp/datahelp/blob/main/LICENSE) file for more details.
 
 ## Contact
 
-If you have any questions or feedback, feel free to reach out to our support team at dev.kitonga@gmail.com or join our community forum at [https://community.data-help.com](https://community.data-help.com). We are here to assist you in making your data science journey smooth and successful!
+If you have any questions or feedback, feel free to reach out to our support team at dev.kitonga@gmail.com or join our community forum at [https://community.datahelp.com](https://community.datahelp.com). We are here to assist you in making your data science journey smooth and successful!
```

### Comparing `datahelp-0.1.0/datahelp/create_project.py` & `datahelp-0.1.1/datahelp/create_project.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.0/datahelp/eda.py` & `datahelp-0.1.1/datahelp/eda.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.0/datahelp/examples/.ipynb_checkpoints/ex3-checkpoint.ipynb` & `datahelp-0.1.1/datahelp/examples/.ipynb_checkpoints/ex3-checkpoint.ipynb`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.0/datahelp/examples/data/iris.csv` & `datahelp-0.1.1/datahelp/examples/data/iris.csv`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.0/datahelp/examples/ex1.py` & `datahelp-0.1.1/datahelp/examples/ex1.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.0/datahelp/examples/ex2.py` & `datahelp-0.1.1/datahelp/examples/ex2.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.0/datahelp/feature_engineering.py` & `datahelp-0.1.1/datahelp/feature_engineering.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.0/datahelp/modelling.py` & `datahelp-0.1.1/datahelp/modelling.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.0/datahelp/utils.py` & `datahelp-0.1.1/datahelp/utils.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.0/datahelp/visualize.py` & `datahelp-0.1.1/datahelp/visualize.py`

 * *Files identical despite different names*

### Comparing `datahelp-0.1.0/pyproject.toml` & `datahelp-0.1.1/pyproject.toml`

 * *Files 13% similar despite different names*

```diff
@@ -1,31 +1,26 @@
 [build-system]
 requires = ["poetry-core>=1.1.0"]
 build-backend = "poetry.core.masonry.api"
 
 [tool.poetry]
 name = "datahelp"
-version = "0.1.0"
+version = "0.1.1"
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
     "Programming Language :: Python :: 3",
-    "Programming Language :: Python :: 3.6",
-    "Programming Language :: Python :: 3.7",
-    "Programming Language :: Python :: 3.8",
-    "Programming Language :: Python :: 3.9",
-    "Programming Language :: Python :: 3.10",
 ]
 
 [tool.poetry.dependencies]
 python = ">=3.6"
 pandas = "^1.3.3"
 scikit-learn = "^0.24.2"
 seaborn = "^0.11.2"
```

### Comparing `datahelp-0.1.0/PKG-INFO` & `datahelp-0.1.1/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: datahelp
-Version: 0.1.0
+Version: 0.1.1
 Summary: Data science library for data science / data analysis teams
 Home-page: https://github.com/kimxons/datahelp
 License: MIT
 Keywords: data,science,data analysis,library,machine learning
 Author: Meshack Kitonga
 Author-email: dev.kitonga@gmail.com
 Requires-Python: >=3.6
@@ -25,37 +25,37 @@
 Requires-Dist: numpy (>=1.21.2,<2.0.0)
 Requires-Dist: pandas (>=1.3.3,<2.0.0)
 Requires-Dist: scikit-learn (>=0.24.2,<0.25.0)
 Requires-Dist: seaborn (>=0.11.2,<0.12.0)
 Project-URL: Repository, https://github.com/kimxons/datahelp.git
 Description-Content-Type: text/markdown
 
-# Data-Help
+# datahelp
 
-Data-Help is a Python library designed to assist data science and data analysis teams in their workflow. It provides various utility functions and tools to streamline common data science tasks.
+datahelp is a Python library designed to assist data science and data analysis teams in their workflow. It provides various utility functions and tools to streamline common data science tasks.
 
 ## Features
 
-Data-Help offers the following key features:
+datahelp offers the following key features:
 
-1. **Project Management:** Data-Help simplifies the creation of standard data science project structures. With a single function call, you can generate a well-organized project directory with predefined folders for datasets, processed data, raw data, outputs, models, scripts, notebooks, and more.
+1. **Project Management:** datahelp simplifies the creation of standard data science project structures. With a single function call, you can generate a well-organized project directory with predefined folders for datasets, processed data, raw data, outputs, models, scripts, notebooks, and more.
 
-2. **Model Saving and Loading:** Data-Help provides easy-to-use functions for saving and loading trained machine learning models. It supports various formats such as joblib, pickle, and keras, enabling seamless integration with different model types.
+2. **Model Saving and Loading:** datahelp provides easy-to-use functions for saving and loading trained machine learning models. It supports various formats such as joblib, pickle, and keras, enabling seamless integration with different model types.
 
 3. **Data Exploration and Visualization:** The library includes functions for data exploration, summary statistics, and visualization. You can quickly generate feature importances plots and visualize missing data to gain insights into your datasets.
 
-4. **Feature Engineering:** Data-Help includes methods for handling missing data and noise in your datasets. It offers functions for dropping missing columns based on a specified threshold and detecting outliers using Tukey's Interquartile Range (IQR) method.
+4. **Feature Engineering:** datahelp includes methods for handling missing data and noise in your datasets. It offers functions for dropping missing columns based on a specified threshold and detecting outliers using Tukey's Interquartile Range (IQR) method.
 
-5. **Model Evaluation and Cross-Validation:** Data-Help provides tools to evaluate model performance, including functions to calculate accuracy, F1-score, precision, recall, and generate classification reports. It also supports cross-validation for model evaluation.
+5. **Model Evaluation and Cross-Validation:** datahelp provides tools to evaluate model performance, including functions to calculate accuracy, F1-score, precision, recall, and generate classification reports. It also supports cross-validation for model evaluation.
 
 6. **Scaling and Normalization:** The library offers functions for min-max scaling and z-score normalization of data to bring features to a common scale.
 
 ## Getting Started
 
-To use Data-Help in your data science projects, you can install it via pip:
+To use datahelp in your data science projects, you can install it via pip:
 
 ```bash
 pip install datahelp
 ```
 
 Once installed, you can import the library and explore its functionality:
 
@@ -77,21 +77,21 @@
 
 missing = dh.eda.display_missing(df)
 missing
 ```
 
 ## Documentation
 
-For detailed usage instructions and API reference, please refer to the official documentation at [https://data-help-docs.example.com](https://data-help-docs.example.com)
+For detailed usage instructions and API reference, please refer to the official documentation at [https://datahelp-docs.example.com](https://datahelp-docs.example.com)
 
 ## Contribution
 
-Data-Help is an open-source project, and we welcome contributions from the data science community. If you find a bug, have a feature request, or want to contribute improvements, please open an issue or submit a pull request on our GitHub repository at [https://github.com/data-help/data-help](https://github.com/data-help/data-help).
+datahelp is an open-source project, and we welcome contributions from the data science community. If you find a bug, have a feature request, or want to contribute improvements, please open an issue or submit a pull request on our GitHub repository at [https://github.com/datahelp/datahelp](https://github.com/datahelp/datahelp).
 
 ## License
 
-Data-Help is licensed under the MIT License. See the [LICENSE](https://github.com/data-help/data-help/blob/main/LICENSE) file for more details.
+datahelp is licensed under the MIT License. See the [LICENSE](https://github.com/datahelp/datahelp/blob/main/LICENSE) file for more details.
 
 ## Contact
 
-If you have any questions or feedback, feel free to reach out to our support team at dev.kitonga@gmail.com or join our community forum at [https://community.data-help.com](https://community.data-help.com). We are here to assist you in making your data science journey smooth and successful!
+If you have any questions or feedback, feel free to reach out to our support team at dev.kitonga@gmail.com or join our community forum at [https://community.datahelp.com](https://community.datahelp.com). We are here to assist you in making your data science journey smooth and successful!
```

