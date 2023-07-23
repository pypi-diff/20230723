# Comparing `tmp/moosez-2.2.1.tar.gz` & `tmp/moosez-2.2.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "moosez-2.2.1.tar", last modified: Sun Jul 23 08:47:52 2023, max compression
+gzip compressed data, was "moosez-2.2.2.tar", last modified: Sun Jul 23 18:24:41 2023, max compression
```

## Comparing `moosez-2.2.1.tar` & `moosez-2.2.2.tar`

### file list

```diff
@@ -1,25 +1,25 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 08:47:52.508602 moosez-2.2.1/
--rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-07-23 08:47:40.000000 moosez-2.2.1/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     1432 2023-07-23 08:47:52.508602 moosez-2.2.1/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     9211 2023-07-23 08:47:40.000000 moosez-2.2.1/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 08:47:52.508602 moosez-2.2.1/moosez/
--rw-r--r--   0 runner    (1001) docker     (123)      253 2023-07-23 08:47:40.000000 moosez-2.2.1/moosez/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2654 2023-07-23 08:47:40.000000 moosez-2.2.1/moosez/constants.py
--rw-r--r--   0 runner    (1001) docker     (123)     5259 2023-07-23 08:47:40.000000 moosez-2.2.1/moosez/display.py
--rw-r--r--   0 runner    (1001) docker     (123)     3631 2023-07-23 08:47:40.000000 moosez-2.2.1/moosez/download.py
--rw-r--r--   0 runner    (1001) docker     (123)     4674 2023-07-23 08:47:40.000000 moosez-2.2.1/moosez/file_utilities.py
--rw-r--r--   0 runner    (1001) docker     (123)     8067 2023-07-23 08:47:40.000000 moosez-2.2.1/moosez/image_conversion.py
--rw-r--r--   0 runner    (1001) docker     (123)    22307 2023-07-23 08:47:40.000000 moosez-2.2.1/moosez/image_processing.py
--rw-r--r--   0 runner    (1001) docker     (123)     4557 2023-07-23 08:47:40.000000 moosez-2.2.1/moosez/input_validation.py
--rw-r--r--   0 runner    (1001) docker     (123)    10215 2023-07-23 08:47:40.000000 moosez-2.2.1/moosez/moosez.py
--rw-r--r--   0 runner    (1001) docker     (123)    12807 2023-07-23 08:47:40.000000 moosez-2.2.1/moosez/predict.py
--rw-r--r--   0 runner    (1001) docker     (123)     6063 2023-07-23 08:47:40.000000 moosez-2.2.1/moosez/resources.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 08:47:52.508602 moosez-2.2.1/moosez.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1432 2023-07-23 08:47:52.000000 moosez-2.2.1/moosez.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      445 2023-07-23 08:47:52.000000 moosez-2.2.1/moosez.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 08:47:52.000000 moosez-2.2.1/moosez.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       46 2023-07-23 08:47:52.000000 moosez-2.2.1/moosez.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)      268 2023-07-23 08:47:52.000000 moosez-2.2.1/moosez.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        7 2023-07-23 08:47:52.000000 moosez-2.2.1/moosez.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 08:47:52.508602 moosez-2.2.1/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     2320 2023-07-23 08:47:40.000000 moosez-2.2.1/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 18:24:41.711727 moosez-2.2.2/
+-rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-07-23 18:24:31.000000 moosez-2.2.2/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     1432 2023-07-23 18:24:41.711727 moosez-2.2.2/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     9211 2023-07-23 18:24:31.000000 moosez-2.2.2/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 18:24:41.711727 moosez-2.2.2/moosez/
+-rw-r--r--   0 runner    (1001) docker     (123)      253 2023-07-23 18:24:31.000000 moosez-2.2.2/moosez/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2654 2023-07-23 18:24:31.000000 moosez-2.2.2/moosez/constants.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3425 2023-07-23 18:24:31.000000 moosez-2.2.2/moosez/display.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3631 2023-07-23 18:24:31.000000 moosez-2.2.2/moosez/download.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4674 2023-07-23 18:24:31.000000 moosez-2.2.2/moosez/file_utilities.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8067 2023-07-23 18:24:31.000000 moosez-2.2.2/moosez/image_conversion.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22307 2023-07-23 18:24:31.000000 moosez-2.2.2/moosez/image_processing.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4557 2023-07-23 18:24:31.000000 moosez-2.2.2/moosez/input_validation.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9619 2023-07-23 18:24:31.000000 moosez-2.2.2/moosez/moosez.py
+-rw-r--r--   0 runner    (1001) docker     (123)    11781 2023-07-23 18:24:31.000000 moosez-2.2.2/moosez/predict.py
+-rw-r--r--   0 runner    (1001) docker     (123)     9500 2023-07-23 18:24:31.000000 moosez-2.2.2/moosez/resources.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 18:24:41.711727 moosez-2.2.2/moosez.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1432 2023-07-23 18:24:41.000000 moosez-2.2.2/moosez.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      445 2023-07-23 18:24:41.000000 moosez-2.2.2/moosez.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 18:24:41.000000 moosez-2.2.2/moosez.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       46 2023-07-23 18:24:41.000000 moosez-2.2.2/moosez.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      268 2023-07-23 18:24:41.000000 moosez-2.2.2/moosez.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        7 2023-07-23 18:24:41.000000 moosez-2.2.2/moosez.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 18:24:41.711727 moosez-2.2.2/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     2320 2023-07-23 18:24:31.000000 moosez-2.2.2/setup.py
```

### Comparing `moosez-2.2.1/LICENSE` & `moosez-2.2.2/LICENSE`

 * *Files identical despite different names*

### Comparing `moosez-2.2.1/PKG-INFO` & `moosez-2.2.2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: moosez
-Version: 2.2.1
+Version: 2.2.2
 Summary: An AI-inference engine for 3D clinical and preclinical whole-body segmentation tasks
 Home-page: https://github.com/QIMP-Team/mooseZ
 Author: Lalith Kumar Shiyam Sundar | Sebastian Gutschmayer
 Author-email: Lalith.shiyamsundar@meduniwien.ac.at
 License: Apache 2.0
 Keywords: moosez model-zoo nnUNet medical-imaging tumor-segmentation organ-segmentation bone-segmentation lung-segmentation muscle-segmentation fat-segmentation vessel-segmentation vertebral-segmentation rib-segmentation preclinical-segmentation clinical-segmentation
 Classifier: Development Status :: 4 - Beta
```

### Comparing `moosez-2.2.1/README.md` & `moosez-2.2.2/README.md`

 * *Files identical despite different names*

### Comparing `moosez-2.2.1/moosez/constants.py` & `moosez-2.2.2/moosez/constants.py`

 * *Files identical despite different names*

### Comparing `moosez-2.2.1/moosez/download.py` & `moosez-2.2.2/moosez/download.py`

 * *Files identical despite different names*

### Comparing `moosez-2.2.1/moosez/file_utilities.py` & `moosez-2.2.2/moosez/file_utilities.py`

 * *Files identical despite different names*

### Comparing `moosez-2.2.1/moosez/image_conversion.py` & `moosez-2.2.2/moosez/image_conversion.py`

 * *Files identical despite different names*

### Comparing `moosez-2.2.1/moosez/image_processing.py` & `moosez-2.2.2/moosez/image_processing.py`

 * *Files identical despite different names*

### Comparing `moosez-2.2.1/moosez/input_validation.py` & `moosez-2.2.2/moosez/input_validation.py`

 * *Files identical despite different names*

### Comparing `moosez-2.2.1/moosez/moosez.py` & `moosez-2.2.2/moosez/moosez.py`

 * *Files 5% similar despite different names*

```diff
@@ -34,15 +34,15 @@
 from moosez import file_utilities
 from moosez import image_conversion
 from moosez import image_processing
 from moosez import input_validation
 from moosez import predict
 from moosez import resources
 from moosez.image_processing import ImageResampler
-from moosez.resources import MODELS
+from moosez.resources import MODELS, AVAILABLE_MODELS
 
 logging.basicConfig(format='%(asctime)s %(levelname)-8s [%(filename)s:%(lineno)d] %(message)s', level=logging.INFO,
                     filename=datetime.now().strftime('moosez-v.2.0.0.%H-%M-%d-%m-%Y.log'),
                     filemode='w')
 
 
 def main():
@@ -50,27 +50,15 @@
 
     parser = argparse.ArgumentParser()
 
     parser.add_argument("-d", "--main_directory", type=str, help="Main directory containing subject folders",
                         required=True)
 
     parser.add_argument("-m", "--model_name", type=str, help="Name of the model to use for segmentation",
-                        choices=["clin_ct_bones",
-                                 "clin_ct_ribs",
-                                 "clin_ct_vertebrae",
-                                 "clin_ct_muscles",
-                                 "clin_ct_lungs",
-                                 "clin_ct_fat",
-                                 "clin_ct_vessels",
-                                 "clin_ct_organs",
-                                 "clin_pt_fdg_tumor",
-                                 "clin_ct_all",
-                                 "clin_fdg_pt_ct_all",
-                                 "clin_ct_body",
-                                 "preclin_mr_all"], required=True)
+                        choices=AVAILABLE_MODELS, required=True)
     args = parser.parse_args()
 
     parent_folder = os.path.abspath(args.main_directory)
     model_name = args.model_name
 
     display.logo()
     display.citation()
```

### Comparing `moosez-2.2.1/moosez/predict.py` & `moosez-2.2.2/moosez/predict.py`

 * *Files 17% similar despite different names*

```diff
@@ -27,51 +27,15 @@
 from mpire import WorkerPool
 
 from moosez import constants
 from moosez import file_utilities
 from moosez import image_processing
 from moosez.image_processing import ImageResampler
 from moosez.image_processing import NiftiPreprocessor
-from moosez.resources import MODELS
-
-
-def map_model_name_to_task_number(model_name: str):
-    """
-    Maps the model name to the task number.
-    :param model_name: The name of the model.
-    :return: The task number.
-    """
-    if model_name == "clin_ct_bones":
-        return 201
-    elif model_name == "clin_ct_ribs":
-        return 202
-    elif model_name == "clin_ct_vertebrae":
-        return 203
-    elif model_name == "clin_ct_muscles":
-        return 204
-    elif model_name == "clin_ct_lungs":
-        return 333
-    elif model_name == "clin_ct_fat":
-        return 206
-    elif model_name == "clin_ct_vessels":
-        return 207
-    elif model_name == "clin_ct_organs":
-        return 123
-    elif model_name == "clin_pt_fdg_tumor":
-        return 789
-    elif model_name == "clin_ct_all":
-        return 210
-    elif model_name == "clin_fdg_pt_ct_all":
-        return 211
-    elif model_name == "preclin_mr_all":
-        return 234
-    elif model_name == "clin_ct_body":
-        return 696
-    else:
-        raise Exception(f"Error: The model name '{model_name}' is not valid.")
+from moosez.resources import MODELS, map_model_name_to_task_number
 
 
 def predict(model_name: str, input_dir: str, output_dir: str, accelerator: str):
     """
     Runs the prediction using nnunet_predict.
     :param model_name: The name of the model.
     :param input_dir: The input directory.
```

### Comparing `moosez-2.2.1/moosez.egg-info/PKG-INFO` & `moosez-2.2.2/moosez.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: moosez
-Version: 2.2.1
+Version: 2.2.2
 Summary: An AI-inference engine for 3D clinical and preclinical whole-body segmentation tasks
 Home-page: https://github.com/QIMP-Team/mooseZ
 Author: Lalith Kumar Shiyam Sundar | Sebastian Gutschmayer
 Author-email: Lalith.shiyamsundar@meduniwien.ac.at
 License: Apache 2.0
 Keywords: moosez model-zoo nnUNet medical-imaging tumor-segmentation organ-segmentation bone-segmentation lung-segmentation muscle-segmentation fat-segmentation vessel-segmentation vertebral-segmentation rib-segmentation preclinical-segmentation clinical-segmentation
 Classifier: Development Status :: 4 - Beta
```

### Comparing `moosez-2.2.1/setup.py` & `moosez-2.2.2/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name='moosez',
-    version='2.2.1',
+    version='2.2.2',
     author='Lalith Kumar Shiyam Sundar | Sebastian Gutschmayer',
     author_email='Lalith.shiyamsundar@meduniwien.ac.at',
     description='An AI-inference engine for 3D clinical and preclinical whole-body segmentation tasks',
     python_requires='>=3.9',
     long_description='mooseZ is an AI-inference engine based on nnUNet, designed for 3D clinical and preclinical'
                      ' whole-body segmentation tasks. It serves models tailored towards different modalities such'
                      ' as PET, CT, and MR. mooseZ provides fast and accurate segmentation results, making it a '
```

