# Comparing `tmp/data-help-0.1.2.tar.gz` & `tmp/data-help-0.1.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "data-help-0.1.2.tar", last modified: Sat Jul 22 22:46:29 2023, max compression
+gzip compressed data, was "data-help-0.1.3.tar", last modified: Sun Jul 23 00:05:27 2023, max compression
```

## Comparing `data-help-0.1.2.tar` & `data-help-0.1.3.tar`

### file list

```diff
@@ -1,20 +1,20 @@
-drwxr-xr-x   0 shak      (1000) shak      (1000)        0 2023-07-22 22:46:29.018537 data-help-0.1.2/
--rw-r--r--   0 shak      (1000) shak      (1000)     1067 2023-07-19 21:51:44.000000 data-help-0.1.2/LICENSE.txt
--rw-r--r--   0 shak      (1000) shak      (1000)     3905 2023-07-22 22:46:29.018537 data-help-0.1.2/PKG-INFO
--rw-r--r--   0 shak      (1000) shak      (1000)     3476 2023-07-22 22:23:16.000000 data-help-0.1.2/README.md
-drwxr-xr-x   0 shak      (1000) shak      (1000)        0 2023-07-22 22:46:29.018537 data-help-0.1.2/data_help/
--rw-r--r--   0 shak      (1000) shak      (1000)       22 2023-07-22 22:46:16.000000 data-help-0.1.2/data_help/__init__.py
--rw-r--r--   0 shak      (1000) shak      (1000)     4637 2023-07-19 21:38:45.000000 data-help-0.1.2/data_help/create_project.py
--rw-r--r--   0 shak      (1000) shak      (1000)     7813 2023-07-22 22:16:10.000000 data-help-0.1.2/data_help/eda.py
--rw-r--r--   0 shak      (1000) shak      (1000)     5003 2023-07-22 22:04:55.000000 data-help-0.1.2/data_help/feature_engineering.py
--rw-r--r--   0 shak      (1000) shak      (1000)     4231 2023-07-22 22:00:28.000000 data-help-0.1.2/data_help/modelling.py
--rw-r--r--   0 shak      (1000) shak      (1000)     1043 2023-07-19 21:38:45.000000 data-help-0.1.2/data_help/utils.py
--rw-r--r--   0 shak      (1000) shak      (1000)      745 2023-07-19 21:38:45.000000 data-help-0.1.2/data_help/visualize.py
-drwxr-xr-x   0 shak      (1000) shak      (1000)        0 2023-07-22 22:46:29.018537 data-help-0.1.2/data_help.egg-info/
--rw-r--r--   0 shak      (1000) shak      (1000)     3905 2023-07-22 22:46:28.000000 data-help-0.1.2/data_help.egg-info/PKG-INFO
--rw-r--r--   0 shak      (1000) shak      (1000)      369 2023-07-22 22:46:28.000000 data-help-0.1.2/data_help.egg-info/SOURCES.txt
--rw-r--r--   0 shak      (1000) shak      (1000)        1 2023-07-22 22:46:28.000000 data-help-0.1.2/data_help.egg-info/dependency_links.txt
--rw-r--r--   0 shak      (1000) shak      (1000)       65 2023-07-22 22:46:28.000000 data-help-0.1.2/data_help.egg-info/requires.txt
--rw-r--r--   0 shak      (1000) shak      (1000)       10 2023-07-22 22:46:28.000000 data-help-0.1.2/data_help.egg-info/top_level.txt
--rw-r--r--   0 shak      (1000) shak      (1000)       79 2023-07-22 22:46:29.018537 data-help-0.1.2/setup.cfg
--rw-r--r--   0 shak      (1000) shak      (1000)     1151 2023-07-22 22:46:21.000000 data-help-0.1.2/setup.py
+drwxr-xr-x   0 shak      (1000) shak      (1000)        0 2023-07-23 00:05:27.818072 data-help-0.1.3/
+-rw-r--r--   0 shak      (1000) shak      (1000)     1067 2023-07-19 21:51:44.000000 data-help-0.1.3/LICENSE.txt
+-rw-r--r--   0 shak      (1000) shak      (1000)     3905 2023-07-23 00:05:27.818072 data-help-0.1.3/PKG-INFO
+-rw-r--r--   0 shak      (1000) shak      (1000)     3476 2023-07-22 22:23:16.000000 data-help-0.1.3/README.md
+drwxr-xr-x   0 shak      (1000) shak      (1000)        0 2023-07-23 00:05:27.818072 data-help-0.1.3/data_help/
+-rw-r--r--   0 shak      (1000) shak      (1000)       22 2023-07-23 00:05:10.000000 data-help-0.1.3/data_help/__init__.py
+-rw-r--r--   0 shak      (1000) shak      (1000)     4637 2023-07-23 00:03:56.000000 data-help-0.1.3/data_help/create_project.py
+-rw-r--r--   0 shak      (1000) shak      (1000)     7813 2023-07-23 00:03:38.000000 data-help-0.1.3/data_help/eda.py
+-rw-r--r--   0 shak      (1000) shak      (1000)     5003 2023-07-22 22:04:55.000000 data-help-0.1.3/data_help/feature_engineering.py
+-rw-r--r--   0 shak      (1000) shak      (1000)     4231 2023-07-22 22:00:28.000000 data-help-0.1.3/data_help/modelling.py
+-rw-r--r--   0 shak      (1000) shak      (1000)     1042 2023-07-22 23:17:03.000000 data-help-0.1.3/data_help/utils.py
+-rw-r--r--   0 shak      (1000) shak      (1000)      745 2023-07-19 21:38:45.000000 data-help-0.1.3/data_help/visualize.py
+drwxr-xr-x   0 shak      (1000) shak      (1000)        0 2023-07-23 00:05:27.818072 data-help-0.1.3/data_help.egg-info/
+-rw-r--r--   0 shak      (1000) shak      (1000)     3905 2023-07-23 00:05:27.000000 data-help-0.1.3/data_help.egg-info/PKG-INFO
+-rw-r--r--   0 shak      (1000) shak      (1000)      369 2023-07-23 00:05:27.000000 data-help-0.1.3/data_help.egg-info/SOURCES.txt
+-rw-r--r--   0 shak      (1000) shak      (1000)        1 2023-07-23 00:05:27.000000 data-help-0.1.3/data_help.egg-info/dependency_links.txt
+-rw-r--r--   0 shak      (1000) shak      (1000)       65 2023-07-23 00:05:27.000000 data-help-0.1.3/data_help.egg-info/requires.txt
+-rw-r--r--   0 shak      (1000) shak      (1000)       10 2023-07-23 00:05:27.000000 data-help-0.1.3/data_help.egg-info/top_level.txt
+-rw-r--r--   0 shak      (1000) shak      (1000)       79 2023-07-23 00:05:27.818072 data-help-0.1.3/setup.cfg
+-rw-r--r--   0 shak      (1000) shak      (1000)     1151 2023-07-23 00:05:16.000000 data-help-0.1.3/setup.py
```

### Comparing `data-help-0.1.2/LICENSE.txt` & `data-help-0.1.3/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `data-help-0.1.2/PKG-INFO` & `data-help-0.1.3/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: data-help
-Version: 0.1.2
+Version: 0.1.3
 Summary: A python library for easy modelling
 Home-page: https://github.com/data_help
 Author: Meshack Kitonga
 Author-email: dev.kitonga@gmail.com
 License: MIT
 Classifier: Development Status :: 2 - Pre-Alpha
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `data-help-0.1.2/README.md` & `data-help-0.1.3/README.md`

 * *Files identical despite different names*

### Comparing `data-help-0.1.2/data_help/create_project.py` & `data-help-0.1.3/data_help/create_project.py`

 * *Files identical despite different names*

### Comparing `data-help-0.1.2/data_help/eda.py` & `data-help-0.1.3/data_help/eda.py`

 * *Files 1% similar despite different names*

```diff
@@ -5,17 +5,17 @@
 
 import matplotlib.pyplot as plt
 import numpy as np
 import pandas as pd
 import seaborn as sns
 
 if platform.system() == "Darwin":
-    plt.switch_platform("TkAgg")
+    plt.switch_backend("TkAgg")
 else:
-    plt.switch_system("Agg")
+    plt.switch_backend("Agg")
 
 
 def get_num_vars(df: Union[pd.DataFrame, pd.Series]) -> None:
     """
     Returns the list of numerical features in a DataFrame or Series object.
 
     Parameters:
```

### Comparing `data-help-0.1.2/data_help/feature_engineering.py` & `data-help-0.1.3/data_help/feature_engineering.py`

 * *Files identical despite different names*

### Comparing `data-help-0.1.2/data_help/modelling.py` & `data-help-0.1.3/data_help/modelling.py`

 * *Files identical despite different names*

### Comparing `data-help-0.1.2/data_help/utils.py` & `data-help-0.1.3/data_help/utils.py`

 * *Files 0% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 def _get_home_path(filepath):
     """
     Helper function to get the project home path.
     """
     paths = ["src", "src/scripts/ingest", "src/scripts/preparation", "src/scripts/modeling", "src/notebooks"]
     for path in paths:
         if filepath.endswith(path):
-            return filepath[0 : filepath.index(path)]
+            return filepath[0: filepath.index(path)]
     return filepath
 
 
 def _get_path(dir=None):
     """
     Helper function to get a path from the project configuration file.
     """
```

### Comparing `data-help-0.1.2/data_help/visualize.py` & `data-help-0.1.3/data_help/visualize.py`

 * *Files identical despite different names*

### Comparing `data-help-0.1.2/data_help.egg-info/PKG-INFO` & `data-help-0.1.3/data_help.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: data-help
-Version: 0.1.2
+Version: 0.1.3
 Summary: A python library for easy modelling
 Home-page: https://github.com/data_help
 Author: Meshack Kitonga
 Author-email: dev.kitonga@gmail.com
 License: MIT
 Classifier: Development Status :: 2 - Pre-Alpha
 Classifier: License :: OSI Approved :: MIT License
```

### Comparing `data-help-0.1.2/setup.py` & `data-help-0.1.3/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -11,15 +11,15 @@
     except (IOError, UnicodeError) as e:
         print(f"Error reading the file: {e}")
         return None
 
 
 setup(
     name="data-help",
-    version="0.1.2",
+    version="0.1.3",
     license="MIT",
     description="A python library for easy modelling",
     long_description=read("README.md"),
     long_description_content_type="text/markdown",
     author="Meshack Kitonga",
     author_email="dev.kitonga@gmail.com",
     url="https://github.com/data_help",
```

