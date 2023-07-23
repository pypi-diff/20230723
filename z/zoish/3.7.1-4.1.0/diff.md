# Comparing `tmp/zoish-3.7.1.tar.gz` & `tmp/zoish-4.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "zoish-3.7.1.tar", max compression
+gzip compressed data, was "zoish-4.1.0.tar", max compression
```

## Comparing `zoish-3.7.1.tar` & `zoish-4.1.0.tar`

### file list

```diff
@@ -1,51 +1,19 @@
--rw-r--r--   0        0        0     1351 2023-05-17 00:09:02.555950 zoish-3.7.1/LICENSE
--rw-r--r--   0        0        0    10737 2023-04-20 18:05:36.347039 zoish-3.7.1/README.md
--rw-r--r--   0        0        0     1264 2023-05-17 00:31:24.800593 zoish-3.7.1/pyproject.toml
--rw-r--r--   0        0        0       68 2023-04-20 18:05:36.358370 zoish-3.7.1/zoish/.env
--rw-r--r--   0        0        0      925 2023-05-17 00:31:24.801159 zoish-3.7.1/zoish/__init__.py
--rw-r--r--   0        0        0     1938 2023-04-20 18:05:36.358804 zoish-3.7.1/zoish/abstracs/feature_selector_abstracts.py
--rw-r--r--   0        0        0    60046 2023-04-20 18:05:36.359334 zoish-3.7.1/zoish/base_classes/best_estimator_getters.py
--rw-r--r--   0        0        0      675 2023-04-20 18:05:36.359553 zoish-3.7.1/zoish/config.yaml
--rw-r--r--   0        0        0      375 2023-04-20 18:05:36.359847 zoish-3.7.1/zoish/decorators/decorators.py
--rw-r--r--   0        0        0        0 2023-04-20 18:05:36.360014 zoish-3.7.1/zoish/examples/__init__.py
--rw-r--r--   0        0        0    54613 2023-04-20 18:05:36.361103 zoish-3.7.1/zoish/examples/recursive_addition_features/recursive_addition_grid_search_classification.ipynb
--rw-r--r--   0        0        0    42652 2023-04-20 18:05:36.361831 zoish-3.7.1/zoish/examples/recursive_addition_features/recursive_addition_optuna_search_regression.ipynb
--rw-r--r--   0        0        0    61640 2023-04-20 18:05:36.362393 zoish-3.7.1/zoish/examples/recursive_addition_features/recursive_addition_random_search_classification.ipynb
--rw-r--r--   0        0        0    97297 2023-04-20 18:05:36.362969 zoish-3.7.1/zoish/examples/recursive_addition_features/recursive_addition_tune_gridsearch_classification.ipynb
--rw-r--r--   0        0        0   114986 2023-04-20 18:05:36.363251 zoish-3.7.1/zoish/examples/recursive_addition_features/recursive_addition_tune_search_classification.ipynb
--rw-r--r--   0        0        0    20432 2023-04-20 18:05:36.363794 zoish-3.7.1/zoish/examples/recursive_elimination_features/recursive_elimination_grid_search_classification.ipynb
--rw-r--r--   0        0        0    40581 2023-04-20 18:05:36.364116 zoish-3.7.1/zoish/examples/recursive_elimination_features/recursive_elimination_optuna_search_regression.ipynb
--rw-r--r--   0        0        0    63450 2023-04-20 18:05:36.364446 zoish-3.7.1/zoish/examples/recursive_elimination_features/recursive_elimination_random_search_classification.ipynb
--rw-r--r--   0        0        0    56051 2023-04-20 18:05:36.364756 zoish-3.7.1/zoish/examples/recursive_elimination_features/recursive_elimination_tune_gridsearch_classification.ipynb
--rw-r--r--   0        0        0    71923 2023-04-20 18:05:36.365059 zoish-3.7.1/zoish/examples/recursive_elimination_features/recursive_elimination_tune_search_classification.ipynb
--rw-r--r--   0        0        0    22310 2023-04-20 18:05:36.365292 zoish-3.7.1/zoish/examples/select_by_shuffling/select_by_shuffling_grid_search_classification.ipynb
--rw-r--r--   0        0        0    53217 2023-04-20 18:05:36.365575 zoish-3.7.1/zoish/examples/select_by_shuffling/select_by_shuffling_optuna_search_regression.ipynb
--rw-r--r--   0        0        0    61941 2023-04-20 18:05:36.366026 zoish-3.7.1/zoish/examples/select_by_shuffling/select_by_shuffling_random_search_classification.ipynb
--rw-r--r--   0        0        0   102159 2023-04-20 18:05:36.366576 zoish-3.7.1/zoish/examples/select_by_shuffling/select_by_shuffling_tune_gridsearch_regression.ipynb
--rw-r--r--   0        0        0   118140 2023-04-20 18:05:36.366880 zoish-3.7.1/zoish/examples/select_by_shuffling/select_by_shuffling_tune_search_regression.ipynb
--rw-r--r--   0        0        0        0 2023-04-20 18:05:36.367139 zoish-3.7.1/zoish/examples/shap/__init__.py
--rw-r--r--   0        0        0    21194 2023-04-20 18:05:36.369666 zoish-3.7.1/zoish/examples/shap/shap_grid_search_classification.ipynb
--rw-r--r--   0        0        0    58856 2023-04-20 18:05:36.370122 zoish-3.7.1/zoish/examples/shap/shap_optuna_search_regression.ipynb
--rw-r--r--   0        0        0    61444 2023-04-20 18:05:36.373990 zoish-3.7.1/zoish/examples/shap/shap_random_search_classification_1.ipynb
--rw-r--r--   0        0        0   413648 2023-04-20 18:05:36.376447 zoish-3.7.1/zoish/examples/shap/shap_random_search_classification_2.ipynb
--rw-r--r--   0        0        0   465032 2023-04-20 18:05:36.396730 zoish-3.7.1/zoish/examples/shap/shap_random_search_classification_3.ipynb
--rw-r--r--   0        0        0    88426 2023-04-20 18:05:36.397119 zoish-3.7.1/zoish/examples/shap/shap_tune_gridsearch_classification.ipynb
--rw-r--r--   0        0        0    69117 2023-04-20 18:05:36.397585 zoish-3.7.1/zoish/examples/shap/shap_tune_search_regression.ipynb
--rw-r--r--   0        0        0        0 2023-04-20 18:05:36.397811 zoish-3.7.1/zoish/examples/single_feature/__init__.py
--rw-r--r--   0        0        0    40086 2023-04-20 18:05:36.398323 zoish-3.7.1/zoish/examples/single_feature/single_grid_search_classification.ipynb
--rw-r--r--   0        0        0    45581 2023-04-20 18:05:36.398779 zoish-3.7.1/zoish/examples/single_feature/single_optuna_search_regression.ipynb
--rw-r--r--   0        0        0    85377 2023-04-20 18:05:36.399183 zoish-3.7.1/zoish/examples/single_feature/single_random_search_classification.ipynb
--rw-r--r--   0        0        0   106211 2023-04-20 18:05:36.399543 zoish-3.7.1/zoish/examples/single_feature/single_tune_gridsearch_regression.ipynb
--rw-r--r--   0        0        0   122582 2023-04-20 18:05:36.399841 zoish-3.7.1/zoish/examples/single_feature/single_tune_search_regression.ipynb
--rw-r--r--   0        0        0        0 2023-04-20 18:05:36.399998 zoish-3.7.1/zoish/factories/factories.py
--rw-r--r--   0        0        0        0 2023-04-20 18:05:36.400140 zoish-3.7.1/zoish/feature_selectors/__init__.py
--rw-r--r--   0        0        0    85614 2023-04-20 18:05:36.400421 zoish-3.7.1/zoish/feature_selectors/recursive_feature_addition.py
--rw-r--r--   0        0        0    85793 2023-04-20 18:05:36.402572 zoish-3.7.1/zoish/feature_selectors/recursive_feature_elimination.py
--rw-r--r--   0        0        0    85872 2023-04-20 18:05:36.403025 zoish-3.7.1/zoish/feature_selectors/select_by_shuffling.py
--rw-r--r--   0        0        0   100851 2023-04-20 18:05:36.403301 zoish-3.7.1/zoish/feature_selectors/shap_selectors.py
--rw-r--r--   0        0        0    86006 2023-04-20 18:05:36.403660 zoish-3.7.1/zoish/feature_selectors/single_feature_selectors.py
--rw-r--r--   0        0        0        0 2023-05-17 00:09:02.559981 zoish-3.7.1/zoish/logs/.gitkeep
--rw-r--r--   0        0        0        0 2023-04-20 18:05:36.403960 zoish-3.7.1/zoish/mediators/mediators.py
--rw-r--r--   0        0        0       95 2023-04-20 18:05:36.404077 zoish-3.7.1/zoish/project_conf.py
--rw-r--r--   0        0        0       48 2023-05-17 00:31:24.802051 zoish-3.7.1/zoish/version.py
--rw-r--r--   0        0        0    12279 1970-01-01 00:00:00.000000 zoish-3.7.1/PKG-INFO
+-rw-r--r--   0        0        0     1351 2023-07-22 04:19:03.656318 zoish-4.1.0/LICENSE
+-rw-r--r--   0        0        0    10110 2023-07-22 04:19:03.656479 zoish-4.1.0/README.md
+-rw-r--r--   0        0        0     1407 2023-07-23 05:19:38.976682 zoish-4.1.0/pyproject.toml
+-rw-r--r--   0        0        0       68 2023-07-22 04:19:03.662679 zoish-4.1.0/zoish/.env
+-rw-r--r--   0        0        0      925 2023-07-23 05:19:38.977682 zoish-4.1.0/zoish/__init__.py
+-rw-r--r--   0        0        0     1459 2023-07-22 04:19:03.663064 zoish-4.1.0/zoish/abstracs/feature_selector_abstracts.py
+-rw-r--r--   0        0        0      676 2023-07-22 04:19:03.663195 zoish-4.1.0/zoish/config.yaml
+-rw-r--r--   0        0        0      375 2023-07-22 04:19:03.663405 zoish-4.1.0/zoish/decorators/decorators.py
+-rw-r--r--   0        0        0        0 2023-07-22 04:19:03.663516 zoish-4.1.0/zoish/examples/__init__.py
+-rw-r--r--   0        0        0        0 2023-07-22 04:19:03.663795 zoish-4.1.0/zoish/examples/shap/__init__.py
+-rw-r--r--   0        0        0   347978 2023-07-22 04:41:32.938481 zoish-4.1.0/zoish/examples/shap/shap_estimator_optimized_by_gridsearchcv.ipynb
+-rw-r--r--   0        0        0   295262 2023-07-22 04:41:32.941133 zoish-4.1.0/zoish/examples/shap/shap_estimator_optimized_by_tune.ipynb
+-rw-r--r--   0        0        0        0 2023-07-22 04:19:03.668785 zoish-4.1.0/zoish/factories/factories.py
+-rw-r--r--   0        0        0        0 2023-07-22 04:19:03.668952 zoish-4.1.0/zoish/feature_selectors/__init__.py
+-rw-r--r--   0        0        0    17467 2023-07-22 04:19:03.669144 zoish-4.1.0/zoish/feature_selectors/shap_selectors.py
+-rw-r--r--   0        0        0        0 2023-07-22 04:19:03.669299 zoish-4.1.0/zoish/logs/.gitkeep
+-rw-r--r--   0        0        0       95 2023-07-22 04:19:03.669443 zoish-4.1.0/zoish/project_conf.py
+-rw-r--r--   0        0        0       48 2023-07-23 05:19:38.977682 zoish-4.1.0/zoish/version.py
+-rw-r--r--   0        0        0    11795 1970-01-01 00:00:00.000000 zoish-4.1.0/PKG-INFO
```

### Comparing `zoish-3.7.1/LICENSE` & `zoish-4.1.0/LICENSE`

 * *Files identical despite different names*

### Comparing `zoish-3.7.1/README.md` & `zoish-4.1.0/PKG-INFO`

 * *Files 25% similar despite different names*

```diff
@@ -1,51 +1,72 @@
+Metadata-Version: 2.1
+Name: zoish
+Version: 4.1.0
+Summary: Zoish is a Python package that streamlines machine learning by leveraging SHAP values for feature selection and interpretability, making model development more efficient and user-friendly.
+Home-page: https://github.com/drhosseinjavedani/zoish
+License: BSD 2-Clause License
+Keywords: Auto ML,Feature Selection,Pipeline,Machine learning,shap
+Author: drhosseinjavedani
+Author-email: h.javedani@gmail.com
+Requires-Python: >=3.8,<3.11
+Classifier: License :: Other/Proprietary License
+Classifier: Programming Language :: Python :: 3
+Classifier: Programming Language :: Python :: 3.8
+Classifier: Programming Language :: Python :: 3.9
+Classifier: Programming Language :: Python :: 3.10
+Requires-Dist: catboost (>=1.0.6,<2.0.0)
+Requires-Dist: category-encoders (>=2.5.0,<3.0.0)
+Requires-Dist: click (>=8.1.3,<9.0.0)
+Requires-Dist: fasttreeshap (>=0.1.2,<0.2.0)
+Requires-Dist: feature-engine (>=1.4.1,<2.0.0)
+Requires-Dist: imblearn (>=0.0,<0.1)
+Requires-Dist: lightgbm (>=3.3.2,<4.0.0)
+Requires-Dist: lohrasb (>=4.1.0,<5.0.0)
+Requires-Dist: matplotlib (>=3.5.2,<4.0.0)
+Requires-Dist: numba (>=0.55.2,<0.56.0)
+Requires-Dist: numpy (<1.63.0)
+Requires-Dist: pandas (>=1.4.3,<2.0.0)
+Requires-Dist: pip-licenses (>=3.5.4,<4.0.0)
+Requires-Dist: prompt-toolkit (>=3.0.37,<4.0.0)
+Requires-Dist: pycox (>=0.2.3,<0.3.0)
+Requires-Dist: python-dotenv (>=0.21.0,<0.22.0)
+Requires-Dist: ray (>=2.6.0,<3.0.0)
+Requires-Dist: scikit-learn (>=1.1.1,<2.0.0)
+Requires-Dist: scipy (>=1.8.1,<2.0.0)
+Requires-Dist: shap (>=0.41.0,<0.42.0)
+Requires-Dist: xgboost (>=1.6.1,<2.0.0)
+Requires-Dist: xgbse (>=0.2.3,<0.3.0)
+Description-Content-Type: text/markdown
+
 
 ![GitHub Repo stars](https://img.shields.io/github/stars/TorkamaniLab/zoish?style=social) ![GitHub forks](https://img.shields.io/github/forks/TorkamaniLab/zoish?style=social) ![GitHub language count](https://img.shields.io/github/languages/count/TorkamaniLab/zoish) ![GitHub repo size](https://img.shields.io/github/repo-size/TorkamaniLab/zoish) ![GitHub](https://img.shields.io/github/license/TorkamaniLab/zoish) ![PyPI - Downloads](https://img.shields.io/pypi/dd/zoish) ![PyPI - Python Version](https://img.shields.io/pypi/pyversions/zoish) 
 
 # Zoish
 
-Zoish is a package built to ease machine learning development by providing various feature-selecting modules such as:  
-- Select By Single Feature Performance
-- Recursive Feature Elimination
-- Recursive Feature Addition
-- Select By Shuffling
-
-All of them are compatible with [scikit-learn](https://scikit-learn.org) pipeline. 
-
-
-## Introduction
-
-All of the above-mentioned modules of Zoish have class factories that have various methods and parameters. From an estimator to its tunning parameters and from optimizers to their parameters, the final goal is to automate the feature selection of the ML pipeline in a proper way. Optimizers like [Optuna](https://optuna.org/), [GridSearchCV](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.GridSearchCV.html) , [RandomizedSearchCV](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.RandomizedSearchCV.html), [TuneGridSearchCV, and TuneSearchCV](https://github.com/ray-project/tune-sklearn) has critical role in Zoish. They are used to provide the best estimator on a train set that is later used by feature selectors to check what features can improve the accuracy of this best estimator based on desired metrics. In short, Optimizers use information every bit of information in rain set to select the best feature set. 
+Zoish is a Python package that simplifies the machine learning process by using SHAP values for feature importance. It integrates with a range of machine learning models, provides feature selection to enhance performance, and improves model interpretability. With Zoish, users can also visualize feature importance through SHAP summary and bar plots, creating an efficient and user-friendly environment for machine learning development.
 
-The main process in Zoish is to split samples to train and validation set, and then optimization will estimate optimal hyper-parameters of the estimators. After that, this best estimator will be input to the feature selection objects and finally, the best subset of features with higher grades will be returned. This subset can be used as the next steps of the ML pipeline. In the next paragraphs, more details about feature selector modules have provided.
+# Introduction
 
-### ShapFeatureSelectorFactory
+Zoish is a powerful tool for streamlining your machine learning pipeline by leveraging SHAP (SHapley Additive exPlanations) values for feature selection. Designed to work seamlessly with binary and multi-class classification models as well as regression models from sklearn, Zoish is also compatible with gradient boosting frameworks such as CatBoost and LightGBM.
 
-ShapFeatureSelectorFactory uses  [SHAP](https://arxiv.org/abs/1705.07874) (SHapley Additive exPlanation)  for a better feature selection. This package uses [FastTreeSHAP](https://arxiv.org/abs/2109.09847) while calculating shap values and [SHAP](https://shap.readthedocs.io/en/latest/index.html) for plotting. Using this module users can : 
+## Features
 
-- find features using the best estimator of tree-based models with the highest shap values after hyper-parameter optimization.
-- draw some shap related plots for selected features.
-- return a  Pandas data frame with a list of features and shap values. 
+- **Model Flexibility:** Zoish exhibits outstanding flexibility as it can work with any tree-based estimator or a superior estimator emerging from a tree-based optimization process. This enables it to integrate seamlessly into binary or multi-class Sklearn classification models, all Sklearn regression models, as well as with advanced gradient boosting frameworks such as CatBoost and LightGBM.
+- 
+- **Feature Selection:** By utilizing SHAP values, Zoish efficiently determines the most influential features for your predictive models. This improves the interpretability of your model and can potentially enhance model performance by reducing overfitting.
 
-### RecursiveFeatureEliminationFeatureSelectorFactory
+- **Visualization:** Zoish includes capabilities for plotting important features using SHAP summary plots and SHAP bar plots, providing a clear and visual representation of feature importance.
 
-The job of this factory class is to ease the selection of features by following a recursive elimination process. The process uses the best estimator found by the optimizer using all the features. Then it ranks the features according to their importance derived from the best estimator. In the next step, it removes the least important feature and fits again with the best estimator. It calculates the performance of the best estimator again and calculates the performance difference between the new and old results. If the performance drop is below the threshold the feature is removed, and this process will continue until all features have been evaluated. For more information on the logic of the recursive elimination process visit this [RecursiveFeatureElimination](https://feature-engine.readthedocs.io/en/latest/api_doc/selection/RecursiveFeatureElimination.html) page. 
+## Dependencies
 
-### RecursiveFeatureAdditionFeatureSelectorFactory
-It is very similar to RecursiveFeatureEliminationFeatureSelectorFactory, however, the logic is the opposite. It selects features following a recursive addition process. Visit [RecursiveFeatureAddition](https://feature-engine.readthedocs.io/en/latest/api_doc/selection/RecursiveFeatureAddition.html) for more details. 
+The core dependency of Zoish is the `shap` package, which is used to compute the SHAP values for tree based machine learning model. SHAP values are a unified measure of feature importance and they offer an improved interpretation of machine learning models. They are based on the concept of cooperative game theory and provide a fair allocation of the contribution of each feature to the prediction of each instance.
 
-### SelectByShufflingFeatureSelectorFactory
-
-In this module, the selection of features is based on determining the drop in machine learning model performance when each feature’s values are randomly shuffled.
-
-If the variables are important, a random permutation of their values will decrease dramatically the machine learning model performance. Contrarily, the permutation of the values should have little to no effect on the model performance metric we are assessing if the feature is not predictive. To understand how it works completely go to its official page [SelectByShuffling](https://feature-engine.readthedocs.io/en/latest/api_doc/selection/SelectByShuffling.html).
-
-### SingleFeaturePerformanceFeatureSelectorFactory
+## Installation
 
-It selects features based on the performance of a machine learning model trained to utilize a single feature. In other words, it trains a machine-learning model for every single feature, then determines each model’s performance. If the performance of the model is greater than a user-specified threshold, then the feature is retained, otherwise removed. Go to this [page](https://feature-engine.readthedocs.io/en/latest/api_doc/selection/SelectBySingleFeaturePerformance.html) for more information. 
+To install Zoish, use pip:
 
 ## Installation
 
 Zoish package is available on PyPI and can be installed with pip:
 
 ```sh
 pip install zoish
@@ -60,171 +81,270 @@
 
 For log configuration in production environment use 
 
 ```sh
 export env=prod
 ```
 
-## Examples 
+# Examples 
 
-### Import required libraries
 ```
-from zoish.feature_selectors.shap_selectors import ShapFeatureSelector
-import pandas as pd
-from sklearn.model_selection import train_test_split
+
+# Built-in libraries
 import pandas as pd
+
+# Scikit-learn libraries for model selection, metrics, pipeline, impute, preprocessing, compose, and ensemble
+from sklearn.compose import ColumnTransformer
+from sklearn.ensemble import RandomForestClassifier
+from sklearn.feature_selection import SelectFromModel
+from sklearn.impute import SimpleImputer
+from sklearn.metrics import classification_report, confusion_matrix, f1_score, make_scorer
+from sklearn.model_selection import GridSearchCV, KFold, train_test_split
 from sklearn.pipeline import Pipeline
-from sklearn.metrics import r2_score
-from feature_engine.imputation import CategoricalImputer, MeanMedianImputer
-from category_encoders import OrdinalEncoder
-import xgboost
-import optuna
-from optuna.samplers import TPESampler
-from optuna.pruners import HyperbandPruner
-from sklearn.linear_model import LinearRegression
+from sklearn.preprocessing import StandardScaler
+
+# Other libraries
+from category_encoders import TargetEncoder
+from xgboost import XGBClassifier
+from zoish.feature_selectors.shap_selectors import ShapFeatureSelector, ShapPlotFeatures
+import logging
+from zoish import logger
+logger.setLevel(logging.ERROR)
+from feature_engine.imputation import (
+    CategoricalImputer,
+    MeanMedianImputer
+    )
+
+# Set logging level
+logger.setLevel(logging.ERROR)
+
 ```
 
-### Computer Hardware Data Set (a classification problem)
+#### Example: Audiology (Standardized) Data Set
+###### https://archive.ics.uci.edu/ml/datasets/Audiology+%28Standardized%29
+
+
+#### Read data
+
 ```
-urldata= "https://archive.ics.uci.edu/ml/machine-learning-databases/cpu-performance/machine.data"
+urldata = "https://archive.ics.uci.edu/ml/machine-learning-databases/lymphography/lymphography.data"
+urlname = "https://archive.ics.uci.edu/ml/machine-learning-databases/lung-cancer/lung-cancer.names"
 # column names
-col_names=[
-    "vendor name",
-    "Model Name",
-    "MYCT",
-    "MMIN",
-    "MMAX",
-    "CACH",
-    "CHMIN",
-    "CHMAX",
-    "PRP"
+col_names = [
+    "class",
+    "lymphatics",
+    "block of affere",
+    "bl. of lymph. c",
+    "bl. of lymph. s",
+    "by pass",
+    "extravasates",
+    "regeneration of",
+    "early uptake in",
+    "lym.nodes dimin",
+    "lym.nodes enlar",
+    "changes in lym.",
+    "defect in node",
+    "changes in node",
+    "special forms",
+    "dislocation of",
+    "exclusion of no",
+    "no. of nodes in",
+
 ]
-# read data
-data = pd.read_csv(urldata,header=None,names=col_names,sep=',')
+
+data = pd.read_csv(urldata,names=col_names)
+data.head()
 
 ```
-### Train test split
+
+#### Define labels and train-test split
+
+
 ```
-X = data.loc[:, data.columns != "PRP"]
-y = data.loc[:, data.columns == "PRP"]
 
-X_train, X_test, y_train, y_test =train_test_split(X, y, test_size=0.33, random_state=42)
+
+data.loc[(data["class"] == 1) | (data["class"] == 2), "class"] = 0
+data.loc[data["class"] == 3, "class"] = 1
+data.loc[data["class"] == 4, "class"] = 2
+data["class"] = data["class"].astype(int)
 ```
-### Find feature types for later use
+
+#### Train test split
+
 ```
-int_cols =  X_train.select_dtypes(include=['int']).columns.tolist()
-float_cols =  X_train.select_dtypes(include=['float']).columns.tolist()
-cat_cols =  X_train.select_dtypes(include=['object']).columns.tolist()
+X = data.loc[:, data.columns != "class"]
+y = data.loc[:, data.columns == "class"]
+
+X_train, X_test, y_train, y_test = train_test_split(
+    X, y, test_size=0.33,  random_state=42
+)
 ```
 
-###  Define Feature selector and set its arguments  
+#### Defining the feature pipeline steps:
+Here, we use an untuned XGBClassifier model with the ShapFeatureSelector.In the next section, we will repeat the same process but with a tuned XGBClassifier. The aim is to demonstrate that a better estimator can yield improved results when used with the ShapFeatureSelector.
+
 ```
-shap_feature_selector_factory = (
-    ShapFeatureSelector.shap_feature_selector_factory.set_model_params(
-        X=X_train,
-        y=y_train,
-        verbose=10,
-        random_state=0,
-        estimator=xgboost.XGBRegressor(),
-        estimator_params={
-            "max_depth": [4, 5],
-        },
-        fit_params = {
-            "callbacks": None,
-        },
-        method="optuna",
-        # if n_features=None only the threshold will be considered as a cut-off of features grades.
-        # if threshold=None only n_features will be considered to select the top n features.
-        # if both of them are set to some values, the threshold has the priority for selecting features.
-        n_features=5,
-        threshold = None,
-        list_of_obligatory_features_that_must_be_in_model=[],
-        list_of_features_to_drop_before_any_selection=[],
-    )
-    .set_shap_params(
-        model_output="raw",
-        feature_perturbation="interventional",
-        algorithm="v2",
-        shap_n_jobs=-1,
-        memory_tolerance=-1,
-        feature_names=None,
-        approximate=False,
-        shortcut=False,
-    )
-    .set_optuna_params(
-            measure_of_accuracy="r2_score(y_true, y_pred)",
-            # optuna params
-            with_stratified=False,
-            test_size=.3,
-            n_jobs=-1,
-            # optuna params
-            # optuna study init params
-            study=optuna.create_study(
-                storage=None,
-                sampler=TPESampler(),
-                pruner=HyperbandPruner(),
-                study_name="example of optuna optimizer",
-                direction="maximize",
-                load_if_exists=False,
-                directions=None,
-            ),
-            # optuna optimization params
-            study_optimize_objective=None,
-            study_optimize_objective_n_trials=20,
-            study_optimize_objective_timeout=600,
-            study_optimize_n_jobs=-1,
-            study_optimize_catch=(),
-            study_optimize_callbacks=None,
-            study_optimize_gc_after_trial=False,
-            study_optimize_show_progress_bar=False,
-            )
-)
+estimator_for_feature_selector= XGBClassifier()     
+estimator_for_feature_selector.fit(X_train, y_train)
+shap_feature_selector = ShapFeatureSelector(model=estimator_for_feature_selector, num_features=5)
+        
+# Define pre-processing for numeric columns (float and integer types)
+numeric_features = X_train.select_dtypes(include=['int64', 'float64']).columns
+numeric_transformer = Pipeline(steps=[
+    ('imputer', SimpleImputer(strategy='mean')),
+    ('scaler', StandardScaler())])
+
+# Define pre-processing for categorical features
+categorical_features = X_train.select_dtypes(include=['object']).columns
+categorical_transformer = Pipeline(steps=[
+    ('imputer', SimpleImputer(strategy='constant', fill_value='missing')),
+    ('encoder', TargetEncoder(handle_missing='return_nan'))])
+
+# Combine preprocessing into one column transformer
+preprocessor = ColumnTransformer(
+    transformers=[
+        ('num', numeric_transformer, numeric_features),
+        ('cat', categorical_transformer, categorical_features)])
+
+# Feature Selection using ShapSelector 
+feature_selection = shap_feature_selector 
+
+# Classifier model
+classifier = RandomForestClassifier(n_estimators=100)
+
+# Create a pipeline that combines the preprocessor with a feature selection and a classifier
+pipeline = Pipeline(steps=[('preprocessor', preprocessor),
+                           ('feature_selection', feature_selection),
+                           ('classifier', classifier)])
+
+# Fit the model
+pipeline.fit(X_train, y_train)
+
+# Predict on test data
+y_test_pred = pipeline.predict(X_test)
+
+# Output first 10 predictions
+print(y_test_pred[:10])
+```
+
+#### Check performance of the Pipeline
 
 ```
-### Build sklearn Pipeline  
+
+print("F1 score : ")
+print(f1_score(y_test, y_test_pred,average='micro'))
+print("Classification report : ")
+print(classification_report(y_test, y_test_pred))
+print("Confusion matrix : ")
+print(confusion_matrix(y_test, y_test_pred))
+
+
+```
+
+
+#### Use better estimator:
+In this iteration, we will utilize the optimally tuned estimator with the ShapFeatureSelector, which is expected to yield improved results."
+
 ```
+int_cols =  X_train.select_dtypes(include=['int']).columns.tolist()
+
+
+# Define the XGBClassifier
+xgb_clf = XGBClassifier()
+
+# Define the parameter grid for XGBClassifier
+param_grid = {
+    'learning_rate': [0.01, 0.1],
+    'max_depth': [ 4, 5],
+    'min_child_weight': [1, 2, 3],
+    'gamma': [0, 0.1, 0.2],
+}
+
+# Define the scoring function
+scoring = make_scorer(f1_score, average='micro')  # Use 'micro' average in case of multiclass target
+
+# Set up GridSearchCV
+grid_search = GridSearchCV(xgb_clf, param_grid, cv=5, scoring=scoring, verbose=1)
+grid_search.fit(X_train, y_train)
+# Fit the GridSearchCV object
+estimator_for_feature_selector= grid_search.best_estimator_ 
+shap_feature_selector = ShapFeatureSelector(model=estimator_for_feature_selector, num_features=5)
+ 
+
 pipeline =Pipeline([
             # int missing values imputers
-            ('intimputer', MeanMedianImputer(
-                imputation_method='median', variables=int_cols)),
-            # category missing values imputers
-            ('catimputer', CategoricalImputer(variables=cat_cols)),
-            #
-            ('catencoder', OrdinalEncoder()),
-            # feature selection
-            ("sfsf", shap_feature_selector_factory),
-            # add any regression model from sklearn e.g., LinearRegression
-            ('regression', LinearRegression())
+            ('floatimputer', MeanMedianImputer(
+                imputation_method='mean', variables=int_cols)),
+           
+            ('shap_feature_selector', shap_feature_selector),
+            ('classfier', RandomForestClassifier(n_estimators=100))
 
 
  ])
+
+
+# Fit the model
+pipeline.fit(X_train, y_train)
+
+# Predict on test data
+y_test_pred = pipeline.predict(X_test)
+
+# Output first 10 predictions
+print(y_test_pred[:10])
+            
 ```
-### Run Pipeline
+
+#### Performance has improved
+
 ```
-pipeline.fit(X_train,y_train)
-y_pred = pipeline.predict(X_test)
+
+print("F1 score : ")
+print(f1_score(y_test, y_test_pred,average='micro'))
+print("Classification report : ")
+print(classification_report(y_test, y_test_pred))
+print("Confusion matrix : ")
+print(confusion_matrix(y_test, y_test_pred))
+
+#### Shap related plots
 
 ```
-### Plots
+
+#### Plot the features importance
 ```
-ShapFeatureSelector.shap_feature_selector_factory.plot_features_all(
-    type_of_plot="summary_plot",
-    path_to_save_plot="../plots/shap_optuna_search_regression_summary_plot"
-)
+plot_factory = ShapPlotFeatures(shap_feature_selector) 
+
 ```
 
-###  Check performance of the Pipeline
+#### Summary Plot of the selected features
 ```
-print('r2 score : ')
-print(r2_score(y_test,y_pred))
+plot_factory.summary_plot()
 
 ```
-### Get access to feature selector instance
+![summary plot](https://i.imgur.com/P7Pt8cd.png)
+
+#### Summary Plot of the all features
 ```
-print(ShapFeatureSelector.shap_feature_selector_factory.get_feature_selector_instance())
+plot_factory.summary_plot_full()
+
 ```
+![summary plot full](https://i.imgur.com/tfnh1kv.png)
 
+#### Bar Plot of the selected features
+
+```
+plot_factory.bar_plot()
+```
+![bar plot](https://i.imgur.com/qsMkVT7.png)
+
+#### Bar Plot of the all features
+
+```
+plot_factory.bar_plot_full()
+```
+![bar plot full](https://i.imgur.com/fA3BPDM.png)
 
 More examples are available in the [examples](https://github.com/drhosseinjavedani/zoish/tree/main/zoish/examples). 
 
 ## License
-Licensed under the [BSD 2-Clause](https://opensource.org/licenses/BSD-2-Clause) License.
+Licensed under the [BSD 2-Clause](https://opensource.org/licenses/BSD-2-Clause) License.
+
+
```

#### encoding

```diff
@@ -1 +1 @@
-utf-8
+us-ascii
```

### Comparing `zoish-3.7.1/pyproject.toml` & `zoish-4.1.0/pyproject.toml`

 * *Files 16% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 [tool.poetry]
 name = "zoish"
-version = "3.7.1"
-description = "Zoish: Automated feature selectoion tools"
+version = "4.1.0"
+description = "Zoish is a Python package that streamlines machine learning by leveraging SHAP values for feature selection and interpretability, making model development more efficient and user-friendly."
 
 authors = ["drhosseinjavedani <h.javedani@gmail.com>"]
 homepage = "https://github.com/drhosseinjavedani/zoish"
 license = "BSD 2-Clause License"
 
 readme = "README.md"
 keywords = [
@@ -27,24 +27,24 @@
 numba = "^0.55.2"
 fasttreeshap = "^0.1.2"
 shap = "^0.41.0"
 xgboost = "^1.6.1"
 matplotlib = "^3.5.2"
 pip-licenses = "^3.5.4"
 feature-engine = "^1.4.1"
-optuna = "^2.10.1"
 catboost = "^1.0.6"
 imblearn = "^0.0"
 lightgbm = "^3.3.2"
 category-encoders = "^2.5.0"
 xgbse = "^0.2.3"
 pycox = "^0.2.3"
-lohrasb = "^3.1.0"
 python-dotenv = "^0.21.0"
 prompt-toolkit = "^3.0.37"
+lohrasb = "^4.1.0"
+ray = "^2.6.0"
 
 
 [tool.poetry.dev-dependencies]
 pytest = ">=6.2.4"
 flake8 = "^4.0.1"
 bump2version = "^1.0.1"
 nox = "^2022.1.7"
```

### Comparing `zoish-3.7.1/zoish/__init__.py` & `zoish-4.1.0/zoish/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,8 +1,8 @@
-__version__ = "3.7.1"
+__version__ = "4.1.0"
 
 import logging
 import logging.config
 import os
 
 import yaml
 from dotenv import load_dotenv
```

### Comparing `zoish-3.7.1/zoish/abstracs/feature_selector_abstracts.py` & `zoish-4.1.0/zoish/abstracs/feature_selector_abstracts.py`

 * *Files 27% similar despite different names*

```diff
@@ -1,40 +1,30 @@
-from abc import ABCMeta, abstractmethod
+from abc import ABC, ABCMeta, abstractmethod
 
 from sklearn.base import BaseEstimator, TransformerMixin
 
 
 class FeatureSelector(BaseEstimator, TransformerMixin):
     """Base class for creating feature selector."""
 
-    def __init__(self, *args, **kwargs):
+    def __init__(self):
         """
         Class initalizer
         """
-        pass
-
-    def prepare_data(self):
-        pass
+        super().__init__()
 
     @abstractmethod
-    def fit(self, *args, **kwargs):
+    def fit(self, X, y):
         """
         Fit estimator using params
         """
         pass
 
     @abstractmethod
-    def calc_best_estimator(self, *args, **kwargs):
-        """
-        Calculate best estimator using params
-        """
-        pass
-
-    @abstractmethod
-    def transform(self, *args, **kwargs):
+    def transform(self, X):
         """
         Return a transform
         """
         pass
 
 
 class BestEstimatorGetterStrategy(metaclass=ABCMeta):
@@ -50,43 +40,29 @@
     def best_estimator_getter(self, *args, **kwargs):
         """
         Get best estomator if any
         """
         pass
 
 
-class PlotFeatures(metaclass=ABCMeta):
+class PlotFeatures(ABC):
     """Base class for creating plots for feature selector."""
 
-    def __init__(self, *args, **kwargs):
-        """
-        Class initalizer
-        """
-        pass
-
     @abstractmethod
-    def get_info_of_features_and_grades(self, *args, **kwargs):
-        """
-        Get info of features grades
-        """
+    def get_info_of_features_and_grades(self):
+        """Get info of features grades"""
         pass
 
     @abstractmethod
-    def get_list_of_features(self, *args, **kwargs):
-        """
-        Get list of features grades
-        """
+    def get_list_of_features(self):
+        """Get list of features grades"""
         pass
 
     @abstractmethod
-    def plot_features(self, *args, **kwargs):
-        """
-        Get feature selector requirements
-        """
+    def plot_features(self):
+        """Get feature selector requirements"""
         pass
 
     @abstractmethod
-    def expose_plot_object(self, *args, **kwargs):
-        """
-        Expose plot object of feature selector
-        """
+    def expose_plot_object(self):
+        """Expose plot object of feature selector"""
         pass
```

### Comparing `zoish-3.7.1/zoish/config.yaml` & `zoish-4.1.0/zoish/config.yaml`

 * *Files 5% similar despite different names*

```diff
@@ -4,15 +4,15 @@
   extended:
     format: '%(asctime)-20s :: %(levelname)-8s :: [%(process)d]%(processName)s :: %(threadName)s[%(thread)d] :: %(pathname)s :: %(lineno)d :: %(message)s'
   simple:
     format: "%(asctime)s :: %(name)s :: %(message)s"
 handlers:
   console:
     class: logging.StreamHandler
-    level: DEBUG
+    level : ERROR
     formatter: simple
     stream: ext://sys.stdout
   file_handler:
     class: logging.FileHandler
     filename: zoish.log
     formatter: extended
     level: INFO
@@ -21,9 +21,9 @@
   dev:
     handlers: [console, file_handler]
   prod:
     handlers: [file_handler]
     propagate: False
  
 root:
-  level: DEBUG
+  level: ERROR
   handlers: [console]
```

