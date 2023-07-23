# Comparing `tmp/moosez-2.2.3.tar.gz` & `tmp/moosez-2.2.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "moosez-2.2.3.tar", last modified: Sun Jul 23 18:54:30 2023, max compression
+gzip compressed data, was "moosez-2.2.4.tar", last modified: Sun Jul 23 18:59:30 2023, max compression
```

## Comparing `moosez-2.2.3.tar` & `moosez-2.2.4.tar`

### file list

```diff
@@ -1,25 +1,25 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 18:54:30.217024 moosez-2.2.3/
--rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-07-23 18:54:16.000000 moosez-2.2.3/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     1432 2023-07-23 18:54:30.217024 moosez-2.2.3/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     9211 2023-07-23 18:54:16.000000 moosez-2.2.3/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 18:54:30.217024 moosez-2.2.3/moosez/
--rw-r--r--   0 runner    (1001) docker     (123)      253 2023-07-23 18:54:16.000000 moosez-2.2.3/moosez/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2654 2023-07-23 18:54:16.000000 moosez-2.2.3/moosez/constants.py
--rw-r--r--   0 runner    (1001) docker     (123)     3425 2023-07-23 18:54:16.000000 moosez-2.2.3/moosez/display.py
--rw-r--r--   0 runner    (1001) docker     (123)     3631 2023-07-23 18:54:16.000000 moosez-2.2.3/moosez/download.py
--rw-r--r--   0 runner    (1001) docker     (123)     4674 2023-07-23 18:54:16.000000 moosez-2.2.3/moosez/file_utilities.py
--rw-r--r--   0 runner    (1001) docker     (123)     8067 2023-07-23 18:54:16.000000 moosez-2.2.3/moosez/image_conversion.py
--rw-r--r--   0 runner    (1001) docker     (123)    22307 2023-07-23 18:54:16.000000 moosez-2.2.3/moosez/image_processing.py
--rw-r--r--   0 runner    (1001) docker     (123)     4557 2023-07-23 18:54:16.000000 moosez-2.2.3/moosez/input_validation.py
--rw-r--r--   0 runner    (1001) docker     (123)     9619 2023-07-23 18:54:16.000000 moosez-2.2.3/moosez/moosez.py
--rw-r--r--   0 runner    (1001) docker     (123)    11781 2023-07-23 18:54:16.000000 moosez-2.2.3/moosez/predict.py
--rw-r--r--   0 runner    (1001) docker     (123)     7399 2023-07-23 18:54:16.000000 moosez-2.2.3/moosez/resources.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 18:54:30.217024 moosez-2.2.3/moosez.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1432 2023-07-23 18:54:30.000000 moosez-2.2.3/moosez.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      445 2023-07-23 18:54:30.000000 moosez-2.2.3/moosez.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 18:54:30.000000 moosez-2.2.3/moosez.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       46 2023-07-23 18:54:30.000000 moosez-2.2.3/moosez.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)      268 2023-07-23 18:54:30.000000 moosez-2.2.3/moosez.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        7 2023-07-23 18:54:30.000000 moosez-2.2.3/moosez.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 18:54:30.217024 moosez-2.2.3/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     2320 2023-07-23 18:54:16.000000 moosez-2.2.3/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 18:59:30.419277 moosez-2.2.4/
+-rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-07-23 18:59:18.000000 moosez-2.2.4/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     1432 2023-07-23 18:59:30.419277 moosez-2.2.4/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     9211 2023-07-23 18:59:18.000000 moosez-2.2.4/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 18:59:30.419277 moosez-2.2.4/moosez/
+-rw-r--r--   0 runner    (1001) docker     (123)      253 2023-07-23 18:59:18.000000 moosez-2.2.4/moosez/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2654 2023-07-23 18:59:18.000000 moosez-2.2.4/moosez/constants.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3425 2023-07-23 18:59:18.000000 moosez-2.2.4/moosez/display.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3631 2023-07-23 18:59:18.000000 moosez-2.2.4/moosez/download.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4674 2023-07-23 18:59:18.000000 moosez-2.2.4/moosez/file_utilities.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8067 2023-07-23 18:59:18.000000 moosez-2.2.4/moosez/image_conversion.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22307 2023-07-23 18:59:18.000000 moosez-2.2.4/moosez/image_processing.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4557 2023-07-23 18:59:18.000000 moosez-2.2.4/moosez/input_validation.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9619 2023-07-23 18:59:18.000000 moosez-2.2.4/moosez/moosez.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11781 2023-07-23 18:59:18.000000 moosez-2.2.4/moosez/predict.py
+-rw-r--r--   0 runner    (1001) docker     (123)     7519 2023-07-23 18:59:18.000000 moosez-2.2.4/moosez/resources.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 18:59:30.419277 moosez-2.2.4/moosez.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1432 2023-07-23 18:59:30.000000 moosez-2.2.4/moosez.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      445 2023-07-23 18:59:30.000000 moosez-2.2.4/moosez.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 18:59:30.000000 moosez-2.2.4/moosez.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       46 2023-07-23 18:59:30.000000 moosez-2.2.4/moosez.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      268 2023-07-23 18:59:30.000000 moosez-2.2.4/moosez.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        7 2023-07-23 18:59:30.000000 moosez-2.2.4/moosez.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 18:59:30.419277 moosez-2.2.4/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     2320 2023-07-23 18:59:18.000000 moosez-2.2.4/setup.py
```

### Comparing `moosez-2.2.3/LICENSE` & `moosez-2.2.4/LICENSE`

 * *Files identical despite different names*

### Comparing `moosez-2.2.3/PKG-INFO` & `moosez-2.2.4/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: moosez
-Version: 2.2.3
+Version: 2.2.4
 Summary: An AI-inference engine for 3D clinical and preclinical whole-body segmentation tasks
 Home-page: https://github.com/QIMP-Team/mooseZ
 Author: Lalith Kumar Shiyam Sundar | Sebastian Gutschmayer
 Author-email: Lalith.shiyamsundar@meduniwien.ac.at
 License: Apache 2.0
 Keywords: moosez model-zoo nnUNet medical-imaging tumor-segmentation organ-segmentation bone-segmentation lung-segmentation muscle-segmentation fat-segmentation vessel-segmentation vertebral-segmentation rib-segmentation preclinical-segmentation clinical-segmentation
 Classifier: Development Status :: 4 - Beta
```

### Comparing `moosez-2.2.3/README.md` & `moosez-2.2.4/README.md`

 * *Files identical despite different names*

### Comparing `moosez-2.2.3/moosez/constants.py` & `moosez-2.2.4/moosez/constants.py`

 * *Files identical despite different names*

### Comparing `moosez-2.2.3/moosez/display.py` & `moosez-2.2.4/moosez/display.py`

 * *Files identical despite different names*

### Comparing `moosez-2.2.3/moosez/download.py` & `moosez-2.2.4/moosez/download.py`

 * *Files identical despite different names*

### Comparing `moosez-2.2.3/moosez/file_utilities.py` & `moosez-2.2.4/moosez/file_utilities.py`

 * *Files identical despite different names*

### Comparing `moosez-2.2.3/moosez/image_conversion.py` & `moosez-2.2.4/moosez/image_conversion.py`

 * *Files identical despite different names*

### Comparing `moosez-2.2.3/moosez/image_processing.py` & `moosez-2.2.4/moosez/image_processing.py`

 * *Files identical despite different names*

### Comparing `moosez-2.2.3/moosez/input_validation.py` & `moosez-2.2.4/moosez/input_validation.py`

 * *Files identical despite different names*

### Comparing `moosez-2.2.3/moosez/moosez.py` & `moosez-2.2.4/moosez/moosez.py`

 * *Files identical despite different names*

### Comparing `moosez-2.2.3/moosez/predict.py` & `moosez-2.2.4/moosez/predict.py`

 * *Files identical despite different names*

### Comparing `moosez-2.2.3/moosez/resources.py` & `moosez-2.2.4/moosez/resources.py`

 * *Files 3% similar despite different names*

```diff
@@ -86,18 +86,18 @@
         "trainer": "nnUNetTrainer",
         "voxel_spacing": [1.5, 1.5, 1.5],
         "multilabel_prefix": "CT_Body_"
     },
 }
 
 
-# This function returns a dictionary indicating the expected modality for a given model.
-# The returned dictionary includes details about the imaging technique, the type of tissue to be segmented, and
-# the model name.
-# If the model is not found, it logs an error message and returns an error message.
+# This function returns a dictionary indicating the expected modality for a given model_name, the imaging technique,
+# the type of tissue to be segmented. The model_name should be the same as the unique identifier mentioned in the
+# MODELS dictionary above and the AVAILABLE_MODELS list.
+# If the model_name is not found, it logs an error message and returns an error message.
 #
 # If you add your own model, update this function to return the expected modality dictionary for your model.
 
 def expected_modality(model_name: str) -> dict:
     """
     Display expected modality for the model.
     :param model_name: The name of the model.
@@ -116,19 +116,19 @@
         model["Model name"] = model_name
         return model
 
     logging.error(" Requested model is not available. Please check the model name.")
     return {"Error": "Requested model is not available. Please check the model name."}
 
 
-# This function maps the model name to the task number. This is the number that comes after DatasetXXXX.
-# If your model folder is Dataset123, then the task number is 123.
-# It checks for known model names and returns the associated task number, this is ABSOLUTELY NEEDED FOR NNUNETV2
-# If the provided model name doesn't match any known model, it raises an exception.
-#
+# This function maps the model name to the task number. This is the number that comes after Dataset in DatasetXXXX,
+# after nnunetv2 training. If your model folder is Dataset123, then the task number is 123.
+# It checks for known model names and returns the associated task number, this is ABSOLUTELY NEEDED for the moosez to
+# work. If the provided model name doesn't match any known model, it raises an exception.
+
 # When adding your own model, update this function to return the task number associated with your model.
 
 def map_model_name_to_task_number(model_name: str):
     """
     Maps the model name to the task number.
     :param model_name: The name of the model.
     :return: The task number.
```

### Comparing `moosez-2.2.3/moosez.egg-info/PKG-INFO` & `moosez-2.2.4/moosez.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: moosez
-Version: 2.2.3
+Version: 2.2.4
 Summary: An AI-inference engine for 3D clinical and preclinical whole-body segmentation tasks
 Home-page: https://github.com/QIMP-Team/mooseZ
 Author: Lalith Kumar Shiyam Sundar | Sebastian Gutschmayer
 Author-email: Lalith.shiyamsundar@meduniwien.ac.at
 License: Apache 2.0
 Keywords: moosez model-zoo nnUNet medical-imaging tumor-segmentation organ-segmentation bone-segmentation lung-segmentation muscle-segmentation fat-segmentation vessel-segmentation vertebral-segmentation rib-segmentation preclinical-segmentation clinical-segmentation
 Classifier: Development Status :: 4 - Beta
```

### Comparing `moosez-2.2.3/setup.py` & `moosez-2.2.4/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name='moosez',
-    version='2.2.3',
+    version='2.2.4',
     author='Lalith Kumar Shiyam Sundar | Sebastian Gutschmayer',
     author_email='Lalith.shiyamsundar@meduniwien.ac.at',
     description='An AI-inference engine for 3D clinical and preclinical whole-body segmentation tasks',
     python_requires='>=3.9',
     long_description='mooseZ is an AI-inference engine based on nnUNet, designed for 3D clinical and preclinical'
                      ' whole-body segmentation tasks. It serves models tailored towards different modalities such'
                      ' as PET, CT, and MR. mooseZ provides fast and accurate segmentation results, making it a '
```

