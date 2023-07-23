# Comparing `tmp/spotRiver-0.0.96.tar.gz` & `tmp/spotRiver-0.0.97.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "spotRiver-0.0.96.tar", last modified: Sun Jul 23 12:28:50 2023, max compression
+gzip compressed data, was "spotRiver-0.0.97.tar", last modified: Sun Jul 23 17:53:34 2023, max compression
```

## Comparing `spotRiver-0.0.96.tar` & `spotRiver-0.0.97.tar`

### file list

```diff
@@ -1,47 +1,47 @@
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 12:28:50.529826 spotRiver-0.0.96/
--rw-r--r--   0 bartz      (501) staff       (20)     1520 2023-01-29 11:49:35.000000 spotRiver-0.0.96/LICENSE
--rw-r--r--   0 bartz      (501) staff       (20)      164 2023-03-22 20:43:16.000000 spotRiver-0.0.96/MANIFEST.in
--rw-r--r--   0 bartz      (501) staff       (20)     3383 2023-07-23 12:28:50.529670 spotRiver-0.0.96/PKG-INFO
--rw-r--r--   0 bartz      (501) staff       (20)     2912 2023-01-29 16:41:52.000000 spotRiver-0.0.96/README.md
--rw-r--r--   0 bartz      (501) staff       (20)     1347 2023-07-23 12:21:29.000000 spotRiver-0.0.96/pyproject.toml
--rw-r--r--   0 bartz      (501) staff       (20)       38 2023-07-23 12:28:50.529876 spotRiver-0.0.96/setup.cfg
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 12:28:50.523872 spotRiver-0.0.96/src/
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 12:28:50.524355 spotRiver-0.0.96/src/spotRiver/
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 12:28:50.527679 spotRiver-0.0.96/src/spotRiver/data/
--rw-r--r--   0 bartz      (501) staff       (20)  1993321 2023-07-23 12:15:18.000000 spotRiver-0.0.96/src/spotRiver/data/UnivariateData.csv
--rw-r--r--   0 bartz      (501) staff       (20)      413 2023-01-29 11:52:00.000000 spotRiver-0.0.96/src/spotRiver/data/__init__.py
--rw-r--r--   0 bartz      (501) staff       (20)     2182 2023-01-17 12:39:58.000000 spotRiver-0.0.96/src/spotRiver/data/airline-passengers.csv
--rw-r--r--   0 bartz      (501) staff       (20)     1023 2023-03-27 20:31:30.000000 spotRiver-0.0.96/src/spotRiver/data/airline_passengers.py
--rw-r--r--   0 bartz      (501) staff       (20)    13646 2023-03-22 20:37:51.000000 spotRiver-0.0.96/src/spotRiver/data/base.py
--rw-r--r--   0 bartz      (501) staff       (20)     1113 2023-03-13 20:26:53.000000 spotRiver-0.0.96/src/spotRiver/data/bike_sharing.py
--rw-r--r--   0 bartz      (501) staff       (20)     2795 2023-07-23 12:28:36.000000 spotRiver-0.0.96/src/spotRiver/data/generic.py
--rw-r--r--   0 bartz      (501) staff       (20)     7751 2023-03-07 16:50:39.000000 spotRiver-0.0.96/src/spotRiver/data/opm.py
--rw-r--r--   0 bartz      (501) staff       (20)    17554 2023-04-08 14:44:16.000000 spotRiver-0.0.96/src/spotRiver/data/river_hyper_dict.json
--rw-r--r--   0 bartz      (501) staff       (20)      329 2023-03-31 21:04:02.000000 spotRiver-0.0.96/src/spotRiver/data/river_hyper_dict.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 12:28:50.527924 spotRiver-0.0.96/src/spotRiver/data/synth/
--rw-r--r--   0 bartz      (501) staff       (20)      328 2023-01-18 17:25:51.000000 spotRiver-0.0.96/src/spotRiver/data/synth/__init__.py
--rw-r--r--   0 bartz      (501) staff       (20)     2442 2023-02-20 15:46:37.000000 spotRiver-0.0.96/src/spotRiver/data/synth/sea.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 12:28:50.528064 spotRiver-0.0.96/src/spotRiver/drift/
--rw-r--r--   0 bartz      (501) staff       (20)      767 2023-02-20 15:46:37.000000 spotRiver-0.0.96/src/spotRiver/drift/drift_generator.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 12:28:50.528467 spotRiver-0.0.96/src/spotRiver/evaluation/
--rw-r--r--   0 bartz      (501) staff       (20)    30967 2023-07-23 10:56:04.000000 spotRiver-0.0.96/src/spotRiver/evaluation/eval_bml.py
--rw-r--r--   0 bartz      (501) staff       (20)     3958 2023-02-26 22:39:12.000000 spotRiver-0.0.96/src/spotRiver/evaluation/eval_nowcast.py
--rw-r--r--   0 bartz      (501) staff       (20)     6752 2023-04-06 12:44:54.000000 spotRiver-0.0.96/src/spotRiver/evaluation/eval_oml.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 12:28:50.528713 spotRiver-0.0.96/src/spotRiver/fun/
--rw-r--r--   0 bartz      (501) staff       (20)     5391 2023-06-10 18:01:21.000000 spotRiver-0.0.96/src/spotRiver/fun/hyperriver.py
--rw-r--r--   0 bartz      (501) staff       (20)    32460 2023-04-22 19:31:59.000000 spotRiver-0.0.96/src/spotRiver/fun/hyperriver_old.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 12:28:50.528864 spotRiver-0.0.96/src/spotRiver/plot/
--rw-r--r--   0 bartz      (501) staff       (20)     1340 2023-03-11 14:52:45.000000 spotRiver-0.0.96/src/spotRiver/plot/stats.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 12:28:50.528990 spotRiver-0.0.96/src/spotRiver/preprocess/
--rw-r--r--   0 bartz      (501) staff       (20)     2488 2023-03-07 16:50:39.000000 spotRiver-0.0.96/src/spotRiver/preprocess/impute.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 12:28:50.529234 spotRiver-0.0.96/src/spotRiver/utils/
--rw-r--r--   0 bartz      (501) staff       (20)     2284 2023-07-06 19:04:13.000000 spotRiver-0.0.96/src/spotRiver/utils/data_conversion.py
--rw-r--r--   0 bartz      (501) staff       (20)     5549 2023-04-13 20:07:21.000000 spotRiver-0.0.96/src/spotRiver/utils/features.py
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 12:28:50.525547 spotRiver-0.0.96/src/spotRiver.egg-info/
--rw-r--r--   0 bartz      (501) staff       (20)     3383 2023-07-23 12:28:50.000000 spotRiver-0.0.96/src/spotRiver.egg-info/PKG-INFO
--rw-r--r--   0 bartz      (501) staff       (20)     1025 2023-07-23 12:28:50.000000 spotRiver-0.0.96/src/spotRiver.egg-info/SOURCES.txt
--rw-r--r--   0 bartz      (501) staff       (20)        1 2023-07-23 12:28:50.000000 spotRiver-0.0.96/src/spotRiver.egg-info/dependency_links.txt
--rw-r--r--   0 bartz      (501) staff       (20)      227 2023-07-23 12:28:50.000000 spotRiver-0.0.96/src/spotRiver.egg-info/requires.txt
--rw-r--r--   0 bartz      (501) staff       (20)       10 2023-07-23 12:28:50.000000 spotRiver-0.0.96/src/spotRiver.egg-info/top_level.txt
-drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 12:28:50.529359 spotRiver-0.0.96/test/
--rw-r--r--   0 bartz      (501) staff       (20)      510 2023-02-25 09:55:05.000000 spotRiver-0.0.96/test/test_features.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 17:53:34.927972 spotRiver-0.0.97/
+-rw-r--r--   0 bartz      (501) staff       (20)     1520 2023-01-29 11:49:35.000000 spotRiver-0.0.97/LICENSE
+-rw-r--r--   0 bartz      (501) staff       (20)      164 2023-03-22 20:43:16.000000 spotRiver-0.0.97/MANIFEST.in
+-rw-r--r--   0 bartz      (501) staff       (20)     3383 2023-07-23 17:53:34.927856 spotRiver-0.0.97/PKG-INFO
+-rw-r--r--   0 bartz      (501) staff       (20)     2912 2023-01-29 16:41:52.000000 spotRiver-0.0.97/README.md
+-rw-r--r--   0 bartz      (501) staff       (20)     1347 2023-07-23 16:28:32.000000 spotRiver-0.0.97/pyproject.toml
+-rw-r--r--   0 bartz      (501) staff       (20)       38 2023-07-23 17:53:34.928006 spotRiver-0.0.97/setup.cfg
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 17:53:34.922153 spotRiver-0.0.97/src/
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 17:53:34.922646 spotRiver-0.0.97/src/spotRiver/
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 17:53:34.926015 spotRiver-0.0.97/src/spotRiver/data/
+-rw-r--r--   0 bartz      (501) staff       (20)  1993321 2023-07-23 12:15:18.000000 spotRiver-0.0.97/src/spotRiver/data/UnivariateData.csv
+-rw-r--r--   0 bartz      (501) staff       (20)      413 2023-01-29 11:52:00.000000 spotRiver-0.0.97/src/spotRiver/data/__init__.py
+-rw-r--r--   0 bartz      (501) staff       (20)     2182 2023-01-17 12:39:58.000000 spotRiver-0.0.97/src/spotRiver/data/airline-passengers.csv
+-rw-r--r--   0 bartz      (501) staff       (20)     1925 2023-07-23 17:22:39.000000 spotRiver-0.0.97/src/spotRiver/data/airline_passengers.py
+-rw-r--r--   0 bartz      (501) staff       (20)    13254 2023-07-23 17:38:31.000000 spotRiver-0.0.97/src/spotRiver/data/base.py
+-rw-r--r--   0 bartz      (501) staff       (20)     1251 2023-07-23 17:40:53.000000 spotRiver-0.0.97/src/spotRiver/data/bike_sharing.py
+-rw-r--r--   0 bartz      (501) staff       (20)     2806 2023-07-23 17:05:39.000000 spotRiver-0.0.97/src/spotRiver/data/generic.py
+-rw-r--r--   0 bartz      (501) staff       (20)     7751 2023-03-07 16:50:39.000000 spotRiver-0.0.97/src/spotRiver/data/opm.py
+-rw-r--r--   0 bartz      (501) staff       (20)    17554 2023-04-08 14:44:16.000000 spotRiver-0.0.97/src/spotRiver/data/river_hyper_dict.json
+-rw-r--r--   0 bartz      (501) staff       (20)      329 2023-03-31 21:04:02.000000 spotRiver-0.0.97/src/spotRiver/data/river_hyper_dict.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 17:53:34.926259 spotRiver-0.0.97/src/spotRiver/data/synth/
+-rw-r--r--   0 bartz      (501) staff       (20)      328 2023-01-18 17:25:51.000000 spotRiver-0.0.97/src/spotRiver/data/synth/__init__.py
+-rw-r--r--   0 bartz      (501) staff       (20)     2427 2023-07-23 17:09:13.000000 spotRiver-0.0.97/src/spotRiver/data/synth/sea.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 17:53:34.926402 spotRiver-0.0.97/src/spotRiver/drift/
+-rw-r--r--   0 bartz      (501) staff       (20)     1080 2023-07-23 16:42:10.000000 spotRiver-0.0.97/src/spotRiver/drift/drift_generator.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 17:53:34.926762 spotRiver-0.0.97/src/spotRiver/evaluation/
+-rw-r--r--   0 bartz      (501) staff       (20)    30967 2023-07-23 10:56:04.000000 spotRiver-0.0.97/src/spotRiver/evaluation/eval_bml.py
+-rw-r--r--   0 bartz      (501) staff       (20)     4018 2023-07-23 16:38:15.000000 spotRiver-0.0.97/src/spotRiver/evaluation/eval_nowcast.py
+-rw-r--r--   0 bartz      (501) staff       (20)     9240 2023-07-23 16:49:02.000000 spotRiver-0.0.97/src/spotRiver/evaluation/eval_oml.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 17:53:34.927005 spotRiver-0.0.97/src/spotRiver/fun/
+-rw-r--r--   0 bartz      (501) staff       (20)     9145 2023-07-23 17:52:18.000000 spotRiver-0.0.97/src/spotRiver/fun/hyperriver.py
+-rw-r--r--   0 bartz      (501) staff       (20)    32460 2023-04-22 19:31:59.000000 spotRiver-0.0.97/src/spotRiver/fun/hyperriver_old.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 17:53:34.927144 spotRiver-0.0.97/src/spotRiver/plot/
+-rw-r--r--   0 bartz      (501) staff       (20)     1521 2023-07-23 17:01:45.000000 spotRiver-0.0.97/src/spotRiver/plot/stats.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 17:53:34.927265 spotRiver-0.0.97/src/spotRiver/preprocess/
+-rw-r--r--   0 bartz      (501) staff       (20)     2488 2023-03-07 16:50:39.000000 spotRiver-0.0.97/src/spotRiver/preprocess/impute.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 17:53:34.927517 spotRiver-0.0.97/src/spotRiver/utils/
+-rw-r--r--   0 bartz      (501) staff       (20)     2289 2023-07-23 16:50:36.000000 spotRiver-0.0.97/src/spotRiver/utils/data_conversion.py
+-rw-r--r--   0 bartz      (501) staff       (20)     6091 2023-07-23 16:57:32.000000 spotRiver-0.0.97/src/spotRiver/utils/features.py
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 17:53:34.923823 spotRiver-0.0.97/src/spotRiver.egg-info/
+-rw-r--r--   0 bartz      (501) staff       (20)     3383 2023-07-23 17:53:34.000000 spotRiver-0.0.97/src/spotRiver.egg-info/PKG-INFO
+-rw-r--r--   0 bartz      (501) staff       (20)     1025 2023-07-23 17:53:34.000000 spotRiver-0.0.97/src/spotRiver.egg-info/SOURCES.txt
+-rw-r--r--   0 bartz      (501) staff       (20)        1 2023-07-23 17:53:34.000000 spotRiver-0.0.97/src/spotRiver.egg-info/dependency_links.txt
+-rw-r--r--   0 bartz      (501) staff       (20)      227 2023-07-23 17:53:34.000000 spotRiver-0.0.97/src/spotRiver.egg-info/requires.txt
+-rw-r--r--   0 bartz      (501) staff       (20)       10 2023-07-23 17:53:34.000000 spotRiver-0.0.97/src/spotRiver.egg-info/top_level.txt
+drwxr-xr-x   0 bartz      (501) staff       (20)        0 2023-07-23 17:53:34.927666 spotRiver-0.0.97/test/
+-rw-r--r--   0 bartz      (501) staff       (20)      510 2023-02-25 09:55:05.000000 spotRiver-0.0.97/test/test_features.py
```

### Comparing `spotRiver-0.0.96/LICENSE` & `spotRiver-0.0.97/LICENSE`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.96/PKG-INFO` & `spotRiver-0.0.97/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: spotRiver
-Version: 0.0.96
+Version: 0.0.97
 Summary: spotRiver - Sequential Parameter Optimization Interface to River
 Author-email: "T. Bartz-Beielstein" <tbb@bartzundbartz.de>
 Project-URL: Homepage, https://www.spotseven.de
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.10
```

### Comparing `spotRiver-0.0.96/README.md` & `spotRiver-0.0.97/README.md`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.96/pyproject.toml` & `spotRiver-0.0.97/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -5,15 +5,15 @@
             "numpy",
             "scikit-learn",
             "matplotlib"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "spotRiver"
-version = "0.0.96"
+version = "0.0.97"
 authors = [
   { name="T. Bartz-Beielstein", email="tbb@bartzundbartz.de" }
 ]
 description = "spotRiver - Sequential Parameter Optimization Interface to River"
 readme = "README.md"
 requires-python = ">=3.10"
 classifiers = [
```

### Comparing `spotRiver-0.0.96/src/spotRiver/data/UnivariateData.csv` & `spotRiver-0.0.97/src/spotRiver/data/UnivariateData.csv`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.96/src/spotRiver/data/airline-passengers.csv` & `spotRiver-0.0.97/src/spotRiver/data/airline-passengers.csv`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.96/src/spotRiver/data/base.py` & `spotRiver-0.0.97/src/spotRiver/data/base.py`

 * *Files 12% similar despite different names*

```diff
@@ -79,40 +79,39 @@
 
 
 class Dataset(abc.ABC):
     """Base class for all datasets.
 
     All datasets inherit from this class, be they stored in a file or generated on the fly.
 
-    Parameters
-    ----------
-    task
-        Type of task the dataset is meant for. Should be one of:
-        - "Regression"
-        - "Binary classification"
-        - "Multi-class classification"
-        - "Multi-output binary classification"
-        - "Multi-output regression"
-    n_features
-        Number of features in the dataset.
-    n_samples
-        Number of samples in the dataset.
-    n_classes
-        Number of classes in the dataset, only applies to classification datasets.
-    n_outputs
-        Number of outputs the target is made of, only applies to multi-output datasets.
-    sparse
-        Whether the dataset is sparse or not.
+    Args:
+        task (str):
+            Type of task the dataset is meant for. Should be one of:
+            - "Regression"
+            - "Binary classification"
+            - "Multi-class classification"
+            - "Multi-output binary classification"
+            - "Multi-output regression"
+        n_features (int):
+            Number of features in the dataset.
+        n_samples (int):
+            Number of samples in the dataset.
+        n_classes (int):
+            Number of classes in the dataset, only applies to classification datasets.
+        n_outputs (int):
+            Number of outputs the target is made of, only applies to multi-output datasets.
+        sparse (bool):
+            Whether the dataset is sparse or not.
 
     """
 
     def __init__(
         self,
-        task,
-        n_features,
+        task: str,
+        n_features: int=None,
         n_samples=None,
         n_classes=None,
         n_outputs=None,
         sparse=False,
     ):
         self.task = task
         self.n_features = n_features
@@ -177,33 +176,15 @@
 
         return out
 
 
 class SyntheticDataset(Dataset):
     """A synthetic dataset.
 
-    Parameters
-    ----------
-    task
-        Type of task the dataset is meant for. Should be one of:
-        - "Regression"
-        - "Binary classification"
-        - "Multi-class classification"
-        - "Multi-output binary classification"
-        - "Multi-output regression"
-    n_features
-        Number of features in the dataset.
-    n_samples
-        Number of samples in the dataset.
-    n_classes
-        Number of classes in the dataset, only applies to classification datasets.
-    n_outputs
-        Number of outputs the target is made of, only applies to multi-output datasets.
-    sparse
-        Whether the dataset is sparse or not.
+    All synthetic datasets inherit from this class.
 
     """
 
     def __repr__(self):
         l_len_prop = max(map(len, self._repr_content.keys()))
         r_len_prop = max(map(len, self._repr_content.values()))
         params = self._get_params()
@@ -227,23 +208,21 @@
             if param.kind != param.VAR_KEYWORD
         }
 
 
 class FileConfig(Config):
     """Base class for configurations that are stored in a local file.
 
-    Parameters
-    ----------
-    filename
-        The file's name.
-    directory
-        The directory where the file is contained. Defaults to the location of the `datasets`
-        module.
-    desc
-        Extra config parameters to pass as keyword arguments.
+    Args:
+        filename (str):
+            The file's name.
+        directory (str):
+            The directory where the file is contained. Defaults to the location of the `datasets` module.
+        desc (dict):
+            Extra config parameters to pass as keyword arguments.
 
     """
 
     def __init__(self, filename, directory=None, **desc):
         super().__init__(**desc)
         self.filename = filename
         self.directory = directory
@@ -262,23 +241,20 @@
 
 
 class FileDataset(Dataset):
     """Base class for datasets that are stored in a local file.
 
     Small datasets that are part of the spotRiver package inherit from this class.
 
-    Parameters
-    ----------
-    filename
-        The file's name.
-    directory
-        The directory where the file is contained. Defaults to the location of the `datasets`
-        module.
-    desc
-        Extra dataset parameters to pass as keyword arguments.
+    Args:
+        filename (str): The file's name.
+        directory (str):
+            The directory where the file is contained. Defaults to the location of the `datasets` module.
+        desc (dict):
+            Extra dataset parameters to pass as keyword arguments.
 
     """
 
     def __init__(self, filename, directory=None, **desc):
         super().__init__(**desc)
         self.filename = filename
         self.directory = directory
@@ -297,30 +273,29 @@
 
 
 class RemoteDataset(FileDataset):
     """Base class for datasets that are stored in a remote file.
 
     Medium and large datasets that are not part of the river package inherit from this class.
 
-    The filename doesn't have to be provided if unpack is False. Indeed in the latter case the
-    filename will be inferred from the URL.
-
-    Parameters
-    ----------
-    url
-        The URL the dataset is located at.
-    size
-        The expected download size.
-    unpack
-        Whether to unpack the download or not.
-    filename
-        An optional name to given to the file if the file is unpacked.
-    desc
-        Extra dataset parameters to pass as keyword arguments.
-
+    Note:
+        The filename doesn't have to be provided if unpack is False. Indeed in the latter case the
+        filename will be inferred from the URL.
+
+    Args:
+        url (str):
+            The URL the dataset is located at.
+        size (int):
+            The expected download size.
+        unpack (bool):
+            Whether to unpack the download or not.
+        filename (str):
+            An optional name to given to the file if the file is unpacked.
+        desc (dict):
+            Extra dataset parameters to pass as keyword arguments.
     """
 
     def __init__(self, url, size, unpack=True, filename=None, **desc):
         if filename is None:
             filename = path.basename(url)
 
         super().__init__(filename=filename, **desc)
@@ -409,24 +384,20 @@
 
 
 class GenericFileDataset(Dataset):
     """Base class for datasets that are stored in a local file.
 
     Small datasets that are part of the spotRiver package inherit from this class.
 
-    Parameters
-    ----------
-    filename
-        The file's name.
-    directory
-        The directory where the file is contained. Defaults to the location of the `datasets`
-        module.
-    desc
-        Extra dataset parameters to pass as keyword arguments.
-
+    Args:
+        filename (str): The file's name.
+        directory (str):
+            The directory where the file is contained. Defaults to the location of the `datasets` module.
+        desc (dict):
+            Extra dataset parameters to pass as keyword arguments.
     """
 
     def __init__(self, filename, target, converters, parse_dates, directory=None, **desc):
         super().__init__(**desc)
         self.filename = filename
         self.directory = directory
         self.target = target
```

### Comparing `spotRiver-0.0.96/src/spotRiver/data/bike_sharing.py` & `spotRiver-0.0.97/src/spotRiver/data/bike_sharing.py`

 * *Files 26% similar despite different names*

```diff
@@ -1,27 +1,26 @@
 from sklearn.datasets import fetch_openml
 
 
 def get_bike_sharing_data(train_size=0.6):
     """
     Fetches the Bike Sharing Demand dataset from OpenML and splits it into training and test sets.
 
-    Parameters
-    ----------
-    train_size : float
-        The proportion of the dataset to include in the training set. Default value: 0.6
+    Args:
+        train_size (float):
+            The proportion of the dataset to include in the training set. Default value: 0.6
+    Returns:
+        (tuple): tuple containing:
+            df (pd.DataFrame): The full dataset.
+            train (pd.DataFrame): The training set.
+            test (pd.DataFrame): The test set.
 
-    Returns
-    -------
-    df : pandas.DataFrame
-        The entire Bike Sharing Demand dataset.
-    train : pandas.DataFrame
-        The training set.
-    test : pandas.DataFrame
-        The test set.
+    Examples:
+        >>> from spotRiver.data.bike_sharing import get_bike_sharing_data
+        >>> df, train, test = get_bike_sharing_data(train_size=0.6)
     """
 
     bike_sharing = fetch_openml("Bike_Sharing_Demand", version=2, as_frame=True, parser="pandas")
     df = bike_sharing.frame
     # Normalize the count column
     df["count"] = df["count"] / df["count"].max()
     # Replace heavy_rain with rain in the weather column
```

### Comparing `spotRiver-0.0.96/src/spotRiver/data/generic.py` & `spotRiver-0.0.97/src/spotRiver/data/generic.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 from river import stream
 from . import base
-from typing import Dict, List, Union
+from typing import Dict, List, Union, Generator
 
 class GenericData(base.GenericFileDataset):
     """A class for handling generic data.
 
     This class inherits from the base.GenericFileDataset class and provides an interface for handling generic data.
 
     Args:
```

### Comparing `spotRiver-0.0.96/src/spotRiver/data/opm.py` & `spotRiver-0.0.97/src/spotRiver/data/opm.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.96/src/spotRiver/data/river_hyper_dict.json` & `spotRiver-0.0.97/src/spotRiver/data/river_hyper_dict.json`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.96/src/spotRiver/data/synth/sea.py` & `spotRiver-0.0.97/src/spotRiver/data/synth/sea.py`

 * *Files 17% similar despite different names*

```diff
@@ -1,56 +1,49 @@
 import random
-
 from river import datasets
 
 
 class SEA(datasets.base.SyntheticDataset):
     """SEA synthetic dataset.
 
-    Implementation of the data stream with abrupt drift described in [^1]. Each observation is
+    Implementation of the data stream with abrupt drift described in [1]. Each observation is
     composed of 3 features. Only the first two features are relevant. The target is binary, and is
     positive if the sum of the features exceeds a certain threshold. There are 4 thresholds to
     choose from. Concept drift can be introduced by switching the threshold anytime during the
     stream.
 
-    * **Variant 0**: `True` if $att1 + att2 > 8$
-
-    * **Variant 1**: `True` if $att1 + att2 > 9$
-
-    * **Variant 2**: `True` if $att1 + att2 > 7$
+    * **Variant 0**: `True` if `att1 + att2 > 8`
 
-    * **Variant 3**: `True` if $att1 + att2 > 9.5$
+    * **Variant 1**: `True` if `att1 + att2 > 9`
 
-    Parameters
-    ----------
-    variant
-        Determines the classification function to use. Possible choices are 0, 1, 2, 3.
-    noise
-        Determines the amount of observations for which the target sign will be flipped.
-    seed
-        Random seed number used for reproducibility.
+    * **Variant 2**: `True` if `att1 + att2 > 7`
 
-    Examples
-    --------
+    * **Variant 3**: `True` if `att1 + att2 > 9.5`
 
-    >>> from river.datasets import synth
+    Args:
+        variant (int): The variant of the data stream to use. Can be 0, 1, 2, or 3.
+        noise (float): The probability of generating label noise.
+        seed (int): Random seed for reproducibility.
 
-    >>> dataset = synth.SEA(variant=0, seed=42)
+    Returns:
+        (Generator): A generator of features and labels.
 
-    >>> for x, y in dataset.take(5):
-    ...     print(x, y)
+    Examples:
+        >>> from spotRiver.data.synth import SEA
+            dataset = synth.SEA(variant=0, seed=42)
+            for x, y in dataset.take(5):
+                print(x, y)
     {0: 6.39426, 1: 0.25010, 2: 2.75029} False
     {0: 2.23210, 1: 7.36471, 2: 6.76699} True
     {0: 8.92179, 1: 0.86938, 2: 4.21921} True
     {0: 0.29797, 1: 2.18637, 2: 5.05355} False
     {0: 0.26535, 1: 1.98837, 2: 6.49884} False
 
-    References
-    ----------
-    [^1]: [A Streaming Ensemble Algorithm (SEA) for Large-Scale Classification](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.482.3991&rep=rep1&type=pdf)
+    References:
+        [1]: [A Streaming Ensemble Algorithm (SEA) for Large-Scale Classification](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.482.3991&rep=rep1&type=pdf)
 
     """
 
     def __init__(self, variant=0, noise=0.0, seed: int = None):
         super().__init__(n_features=3, task=datasets.base.BINARY_CLF)
 
         if variant not in (0, 1, 2, 3):
```

### Comparing `spotRiver-0.0.96/src/spotRiver/evaluation/eval_bml.py` & `spotRiver-0.0.97/src/spotRiver/evaluation/eval_bml.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.96/src/spotRiver/evaluation/eval_nowcast.py` & `spotRiver-0.0.97/src/spotRiver/evaluation/eval_nowcast.py`

 * *Files 10% similar despite different names*

```diff
@@ -1,26 +1,25 @@
 from river import utils
 from river import metrics
 from typing import List, Tuple
 import matplotlib.pyplot as plt
 
 
-# Define a function to evaluate a nowcast model using a rolling metric
-def eval_nowcast_model(model, dataset, time_interval="month", window_size=12) -> Tuple:
+def eval_nowcast_model(model, dataset, time_interval: str = "month", window_size: int = 12) -> Tuple[List, utils.Rolling, List, List]:
     """
     Evaluates a time series model using a rolling mean absolute error metric.
 
-    Parameters:
-        model: A predictor object (river.time_series) that implements the forecast and learn_one methods.
-        dataset: A dataset object that contains the time series data.
-        time_interval: The name of the attribute that contains the date information in the dataset.
-        window_size: The number of observations to use for calculating the rolling metric.
+    Args:
+        model (river.time_series): A predictor object (river.time_series) that implements the forecast and learn_one methods.
+        dataset (object): A dataset object that contains the time series data.
+        time_interval (str): The name of the attribute that contains the date information in the dataset.
+        window_size (int): The number of observations to use for calculating the rolling metric.
 
     Returns:
-        A tuple of four lists:
+        Tuple[List, utils.Rolling, List, List]: A tuple of four lists:
             - dates: The dates corresponding to each observation in the dataset.
             - metric: A rolling metric object that contains the mean absolute error values.
             - y_trues: The true values of the target variable in the dataset.
             - y_preds: The predicted values of the target variable by the model.
 
     Examples:
         >>> from river import compose
@@ -50,14 +49,15 @@
         # Update the error metric
         metric.update(y, y_pred)
         # Store the true value and the prediction
         dates.append(x[time_interval])
         y_trues.append(y)
         y_preds.append(y_pred)
     return dates, metric, y_trues, y_preds
+Kopieren
 
 
 def plot_nowcast_model(
     dates: List[str], metric: utils.Rolling, y_trues: List[float], y_preds: List[float], range: List[int] = None
 ) -> None:
     """
     Plots the true values and the predictions of a nowcast model along with a rolling metric.
```

### Comparing `spotRiver-0.0.96/src/spotRiver/evaluation/eval_oml.py` & `spotRiver-0.0.97/src/spotRiver/evaluation/eval_oml.py`

 * *Files 24% similar despite different names*

```diff
@@ -27,24 +27,41 @@
             where n_steps is the total number of iterations. Results from the beginning have
             a lower weight than results from the end if weight_coeff > 1. If weight_coeff == 0,
             then results are multiplied by 1 and every result has an equal weight. Defaults to 0.0.
         log_level (int): The level of logging to use. 0 = no logging, 50 = print only important
             information. Defaults to 50.
 
     Returns:
-        dict: A dictionary containing the evaluation results. The keys are the names of the
+        (dict): A dictionary containing the evaluation results. The keys are the names of the
             models, and the values are dictionaries with the following keys:
             - "step": A list of iteration numbers at which the model was evaluated.
             - "error": A list of the weighted errors for each iteration.
             - "r_time": A list of the weighted running times for each iteration.
             - "memory": A list of the weighted memory usages for each iteration.
             - "metric_name": The name of the metric used for evaluation.
 
     Reference:
         https://riverml.xyz/0.15.0/recipes/on-hoeffding-trees/
+    
+    Examples:
+        >>> from river import compose
+            from river import linear_model
+            from river import preprocessing, datasets, utils, metrics
+            import matplotlib.pyplot as plt
+            from spotRiver.utils.features import get_ordinal_date
+            from spotRiver.evaluation.eval_nowcast import eval_nowcast_model, plot_nowcast_model
+            model = compose.Pipeline(
+                ('ordinal_date', compose.FuncTransformer(get_ordinal_date)),
+                ('scale', preprocessing.StandardScaler()),
+                ('lin_reg', linear_model.LinearRegression())
+            )
+            dataset = datasets.AirlinePassengers()
+            dates, metric, y_trues, y_preds = eval_nowcast_model(model, dataset=dataset)
+            plot_nowcast_model(dates, metric, y_trues, y_preds)
+
     """
     metric_name = metric.__class__.__name__
     # Convert dataset to a list if needed
     if dataset.__class__ != list:
         dataset = [dataset]
     n_steps = len(dataset)
     result = {}
@@ -76,16 +93,43 @@
         log_x (bool, optional): If True, the x-axis is set to log scale. Defaults to False.
         log_y (bool, optional): If True, the y-axis is set to log scale. Defaults to False.
         figsize (tuple, optional): The size of the figure. Defaults to None, in which case
             the default figure size `(10, 5)` is used.
         filename (str, optional): The name of the file to save the plot to. If None, the plot
             is not saved. Defaults to None.
 
+    Returns:
+        (matplotlib.figure.Figure): The figure object.
+
     Reference:
         https://riverml.xyz/0.15.0/recipes/on-hoeffding-trees/
+
+    Examples:
+        >>> from spotRiver.evaluation.eval_oml import plot_oml_iter_progressive
+
+        >>> result = {
+        ...     "model1": {
+        ...         "step": [1, 2, 3],
+        ...         "error": [0.1, 0.2, 0.3],
+        ...         "r_time": [0.1, 0.2, 0.3],
+        ...         "memory": [0.1, 0.2, 0.3],
+        ...         "metric_name": "MAE"
+        ...     },
+        ...     "model2": {
+        ...         "step": [1, 2, 3],
+        ...         "error": [0.2, 0.3, 0.4],
+        ...         "r_time": [0.2, 0.3, 0.4],
+        ...         "memory": [0.2, 0.3, 0.4],
+        ...         "metric_name": "MAE"
+        ...     }
+        ... }
+
+        >>> plot_oml_iter_progressive(result)
+        <Figure size 1000x500 with 3 Axes>
+
     """
     if figsize is None:
         figsize = (10, 5)
     fig, ax = plt.subplots(figsize=figsize, nrows=3, dpi=300)
     for model_name, model in result.items():
         ax[0].plot(model["step"], model["error"], label=model_name)
         ax[1].plot(model["step"], model["r_time"], label=model_name)
@@ -120,18 +164,45 @@
         metric (function, optional): The metric function to use for computing the function value.
             Defaults to None, in which case the mean function is used.
         weights (numpy.array, optional): An array of weights for error, r_time, and memory.
             If None, the weights are set to [1, 0, 0], which considers only the error.
             Defaults to None.
 
     Returns:
-        numpy.array: An array of function values, one for each model in the evaluation results.
+        (numpy.array): An array of function values, one for each model in the evaluation results.
 
     Raises:
         ValueError: If the weights array is not of length 3.
+
+    Reference:
+        https://riverml.xyz/0.15.0/recipes/on-hoeffding-trees/
+
+    Examples:
+        >>> from spotRiver.evaluation.eval_oml import fun_eval_oml_iter_progressive
+
+        >>> result = {
+        ...     "model1": {
+        ...         "step": [1, 2, 3],
+        ...         "error": [0.1, 0.2, 0.3],
+        ...         "r_time": [0.1, 0.2, 0.3],
+        ...         "memory": [0.1, 0.2, 0.3],
+        ...         "metric_name": "MAE"
+        ...     },
+        ...     "model2": {
+        ...         "step": [1, 2, 3],
+        ...         "error": [0.2, 0.3, 0.4],
+        ...         "r_time": [0.2, 0.3, 0.4],
+        ...         "memory": [0.2, 0.3, 0.4],
+        ...         "metric_name": "MAE"
+        ...     }
+        ... }
+
+        >>> fun_eval_oml_iter_progressive(result)
+        array([0.1, 0.2])
+
     """
     if metric is None:
         metric = mean
     if weights is None:
         weights = array([1, 0, 0])
     if len(weights) != 3:
         raise ValueError("The weights array must be of length 3.")
```

### Comparing `spotRiver-0.0.96/src/spotRiver/fun/hyperriver_old.py` & `spotRiver-0.0.97/src/spotRiver/fun/hyperriver_old.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.96/src/spotRiver/plot/stats.py` & `spotRiver-0.0.97/src/spotRiver/plot/stats.py`

 * *Files 10% similar despite different names*

```diff
@@ -6,22 +6,26 @@
     """Function plots a graphical correlation matrix for each pair of columns in the dataframe.
         The function takes a DataFrame df as input and generates a graphical correlation matrix
         for each pair of columns in the dataframe.
         The upper triangle of the correlation matrix is masked out and set to NaN values.
         The resulting matrix is then styled and returned as a heatmap with colors
         ranging from blue (for negative correlations) to red (for positive correlations).
 
-    Input:
-        df: pandas DataFrame
-        numeric_only: bool, default True.
+    Args:
+        df (pd.DataFrame): Data to plot.
+        numeric_only (bool, default True):
             Include only float, int or boolean data.
+    Returns:
+        (pd.DataFrame): A styled correlation matrix heatmap.
 
-    Example:
-    >>> X = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6], 'C': [7, 8, 9]})
-        corrplot(X)
+    Examples:
+        >>> from spotRiver.plot.stats import corrplot
+            import pandas as pd
+            X = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6], 'C': [7, 8, 9]})
+            corrplot(X)
 
     """
 
     # Compute the correlation matrix
     corr = df.corr(numeric_only=numeric_only)
 
     # Generate a mask for the upper triangle
```

### Comparing `spotRiver-0.0.96/src/spotRiver/preprocess/impute.py` & `spotRiver-0.0.97/src/spotRiver/preprocess/impute.py`

 * *Files identical despite different names*

### Comparing `spotRiver-0.0.96/src/spotRiver/utils/data_conversion.py` & `spotRiver-0.0.97/src/spotRiver/utils/data_conversion.py`

 * *Files 15% similar despite different names*

```diff
@@ -7,17 +7,17 @@
     """Converts a river dataset into a pandas DataFrame.
 
     Args:
         dataset (datasets.base.Dataset): The river dataset to be converted.
         target_column (str): The name of the target column in the resulting DataFrame.
 
     Returns:
-        pd.DataFrame: A pandas DataFrame representation of the given dataset.
+        (pd.DataFrame): A pandas DataFrame representation of the given dataset.
 
-    Example:
+    Examples:
         >>> dataset = datasets.TrumpApproval()
             target_column = "Approval"
             df = convert_to_df(dataset, target_column)
             df.rename(columns={
                 'date': 'ordinal_date',
                 'Gallup': 'gallup',
                 'Ipsos': 'ipsos',
@@ -47,15 +47,15 @@
 
 def compare_two_tree_models(model1, model2, headers=["Parameter", "Default", "Spot"]):
     """Compares two tree models and returns a table of the differences.
     Args:
         model1 (Pipeline): A river model pipeline.
         model2 (Pipeline): A river model pipeline.
     Returns:
-        str: A table of the differences between the two models.
+        (str): A table of the differences between the two models.
     """
     keys = model1[1].summary.keys()
     values1 = model1[1].summary.values()
     values2 = model2[1].summary.values()
     tbl = []
     for key, value1, value2 in zip(keys, values1, values2):
         tbl.append([key, value1, value2])
```

### Comparing `spotRiver-0.0.96/src/spotRiver/utils/features.py` & `spotRiver-0.0.97/src/spotRiver/utils/features.py`

 * *Files 8% similar despite different names*

```diff
@@ -7,21 +7,24 @@
 def get_month_distances(x: Dict[str, datetime]) -> Dict[str, float]:
     """
     This function takes in a dictionary with a single key-value pair where the key is a string and the value is a datetime object.
     It returns a new dictionary where the keys are the names of the months and the values are the result of applying a Gaussian
     function to the difference between the month of the input datetime object and each month.
 
     Args:
-        x (Dict[str, datetime]): A dictionary with a single key-value pair where the key is a string and the value is a
-        datetime object.
+        x (Dict[str, datetime]):
+            A dictionary with a single key-value pair where the key is a string and the value is a datetime object.
 
     Returns:
-        Dict[str, float]: A dictionary where the keys are the names of the months and the values are the result of
-        applying a Gaussian function to the difference between the month of the input datetime object and each month.
-    Example:
+        (Dict[str, float]):
+            A dictionary where the keys are the names of the months and the values are the result of
+            applying a Gaussian function to the difference between the month of the input datetime object and each month.
+    Examples:
+        >>> from spotRiver.utils.features import get_month_distances
+        >>> from datetime import datetime
         >>> get_month_distances({"date": datetime(2020, 1, 1)})
         {'January': 0.6065306597126334, 'February': 0.36787944117144233,
         'March': 0.1353352832366127, 'April': 0.01831563888873418, 'May': 0.00033546262790251185,
         'June': 3.354626279025118e-06, 'July': 2.0611536224385582e-08,
         'August': 8.315287191035679e-11,
         'September': 2.0611536224385582e-13, 'October': 3.354626279025118e-16,
         'November': 3.354626279025118e-19, 'December': 2.0611536224385582e-22}
@@ -33,21 +36,24 @@
 def get_weekday_distances(x):
     """This function takes in a dictionary with a single key-value pair where the key is a string and the value is
         a datetime object.
         It returns a new dictionary where the keys are the names of the days of the week and the values are the
         result of applying a Gaussian function to the difference between the weekday of the input datetime object
         and each day of the week.
     Args:
-        x (Dict[str, datetime]): A dictionary with a single key-value pair where the key is a string and the
-        value is a datetime object.
+        x (Dict[str, datetime]):
+            A dictionary with a single key-value pair where the key is a string and the value is a datetime object.
     Returns:
-        Dict[str, float]: A dictionary where the keys are the names of the days of the week and the values
-        are the result of applying a Gaussian function to the difference between the weekday of the input
-        datetime object and each day of the week.
-    Example:
+        (Dict[str, float]):
+            A dictionary where the keys are the names of the days of the week and the values
+            are the result of applying a Gaussian function to the difference between the weekday of the input
+            datetime object and each day of the week.
+    Examples:
+        >>> from spotRiver.utils.features import get_weekday_distances
+        >>> from datetime import datetime
         >>> get_weekday_distances({"date": datetime(2020, 1, 1)})
         {'Monday': 0.6065306597126334, 'Tuesday': 0.36787944117144233, 'Wednesday': 0.1353352832366127,
         'Thursday': 0.01831563888873418, 'Friday': 0.00033546262790251185, 'Saturday': 3.354626279025118e-06,
         'Sunday': 2.0611536224385582e-08}
     """
     # Monday is the first day, i.e., 0:
     k = list(x.keys())[0]
@@ -57,20 +63,24 @@
 def get_hour_distances(x):
     """This function takes in a dictionary with a single key-value pair where the key is a string and the value
         is a datetime object.
         It returns a new dictionary where the keys are the names of the hours of the day and the values are
         the result of applying a Gaussian function to the difference between the hour of the input datetime
         object and each hour of the day.
     Args:
-        x (Dict[str, datetime]): A dictionary with a single key-value pair where the key is a string and the
-        value is a datetime object.
+        x (Dict[str, datetime]):
+            A dictionary with a single key-value pair where the key is a string and the value is a datetime object.
     Returns:
-        Dict[str, float]: A dictionary where the keys are the names of the hours of the day and the values are
-        the result of applying a Gaussian function to the difference between the hour of the input datetime object and each hour of the day.
-    Example:
+        (Dict[str, float]):
+            A dictionary where the keys are the names of the hours of the day and the values are
+            the result of applying a Gaussian function to the difference between the hour of the
+            input datetime object and each hour of the day.
+    Examples:
+        >>> from spotRiver.utils.features import get_hour_distances
+        >>> from datetime import datetime
         >>> get_hour_distances({"date": datetime(2020, 1, 1)})
         {'0': 0.6065306597126334, '1': 0.36787944117144233, '2': 0.1353352832366127, '3': 0.01831563888873418,
         '4': 0.00033546262790251185, '5': 3.354626279025118e-06, '6': 2.0611536224385582e-08, '7': 8.315287191035679e-11,
         '8': 2.0611536224385582e-13, '9': 3.354626279025118e-16, '10': 3.354626279025118e-19,
         '11': 2.0611536224385582e-22, '12': 8.315287191035679e-26, '13': 2.0611536224385582e-29,
         '14': 3.354626279025118e-33, '15': 3.354626279025118e-37, '16': 2.0611536224385582e-41,
         '17': 8.315287191035679e-46, '18': 2.0611536224385582e-50, '19': 3.354626279025118e-55,
@@ -82,14 +92,17 @@
 
 def get_ordinal_date(x):
     """This function takes in a dictionary with a single key-value pair where the key is a string and the value is a datetime object.
         It returns a new dictionary where the keys are the string "ordinal_date" and the value is the ordinal date of the input datetime object.
     Args:
         x (Dict[str, datetime]): A dictionary with a single key-value pair where the key is a string and the value is a datetime object.
     Returns:
-        Dict[str, float]: A dictionary where the keys are the string "ordinal_date" and the value is the ordinal date of the input datetime object.
-    Example:
+        (Dict[str, float]):
+            A dictionary where the keys are the string "ordinal_date" and the value is the ordinal date of the input datetime object.
+    Examples:
+        >>> from datetime import datetime
+        >>> from spotRiver.utils.features import get_ordinal_date
         >>> get_ordinal_date({"date": datetime(2020, 1, 1)})
         {'ordinal_date': 737424}
     """
     k = list(x.keys())[0]
     return {"ordinal_date": x[k].toordinal()}
```

### Comparing `spotRiver-0.0.96/src/spotRiver.egg-info/PKG-INFO` & `spotRiver-0.0.97/src/spotRiver.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: spotRiver
-Version: 0.0.96
+Version: 0.0.97
 Summary: spotRiver - Sequential Parameter Optimization Interface to River
 Author-email: "T. Bartz-Beielstein" <tbb@bartzundbartz.de>
 Project-URL: Homepage, https://www.spotseven.de
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.10
```

### Comparing `spotRiver-0.0.96/src/spotRiver.egg-info/SOURCES.txt` & `spotRiver-0.0.97/src/spotRiver.egg-info/SOURCES.txt`

 * *Files identical despite different names*

