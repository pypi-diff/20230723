# Comparing `tmp/moosez-2.2.0.tar.gz` & `tmp/moosez-2.2.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "moosez-2.2.0.tar", last modified: Sat Jul 22 09:05:26 2023, max compression
+gzip compressed data, was "moosez-2.2.1.tar", last modified: Sun Jul 23 08:47:52 2023, max compression
```

## Comparing `moosez-2.2.0.tar` & `moosez-2.2.1.tar`

### file list

```diff
@@ -1,25 +1,25 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:05:26.737471 moosez-2.2.0/
--rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-07-22 09:05:17.000000 moosez-2.2.0/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)     1432 2023-07-22 09:05:26.737471 moosez-2.2.0/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     9211 2023-07-22 09:05:17.000000 moosez-2.2.0/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:05:26.737471 moosez-2.2.0/moosez/
--rw-r--r--   0 runner    (1001) docker     (123)      253 2023-07-22 09:05:17.000000 moosez-2.2.0/moosez/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     2654 2023-07-22 09:05:17.000000 moosez-2.2.0/moosez/constants.py
--rw-r--r--   0 runner    (1001) docker     (123)     5259 2023-07-22 09:05:17.000000 moosez-2.2.0/moosez/display.py
--rw-r--r--   0 runner    (1001) docker     (123)     3631 2023-07-22 09:05:17.000000 moosez-2.2.0/moosez/download.py
--rw-r--r--   0 runner    (1001) docker     (123)     4674 2023-07-22 09:05:17.000000 moosez-2.2.0/moosez/file_utilities.py
--rw-r--r--   0 runner    (1001) docker     (123)     8067 2023-07-22 09:05:17.000000 moosez-2.2.0/moosez/image_conversion.py
--rw-r--r--   0 runner    (1001) docker     (123)    22307 2023-07-22 09:05:17.000000 moosez-2.2.0/moosez/image_processing.py
--rw-r--r--   0 runner    (1001) docker     (123)     4557 2023-07-22 09:05:17.000000 moosez-2.2.0/moosez/input_validation.py
--rw-r--r--   0 runner    (1001) docker     (123)     9783 2023-07-22 09:05:17.000000 moosez-2.2.0/moosez/moosez.py
--rw-r--r--   0 runner    (1001) docker     (123)    12807 2023-07-22 09:05:17.000000 moosez-2.2.0/moosez/predict.py
--rw-r--r--   0 runner    (1001) docker     (123)     6063 2023-07-22 09:05:17.000000 moosez-2.2.0/moosez/resources.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 09:05:26.737471 moosez-2.2.0/moosez.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     1432 2023-07-22 09:05:26.000000 moosez-2.2.0/moosez.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      445 2023-07-22 09:05:26.000000 moosez-2.2.0/moosez.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-22 09:05:26.000000 moosez-2.2.0/moosez.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       46 2023-07-22 09:05:26.000000 moosez-2.2.0/moosez.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)      268 2023-07-22 09:05:26.000000 moosez-2.2.0/moosez.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)        7 2023-07-22 09:05:26.000000 moosez-2.2.0/moosez.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-22 09:05:26.737471 moosez-2.2.0/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     2320 2023-07-22 09:05:17.000000 moosez-2.2.0/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 08:47:52.508602 moosez-2.2.1/
+-rw-r--r--   0 runner    (1001) docker     (123)    11357 2023-07-23 08:47:40.000000 moosez-2.2.1/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)     1432 2023-07-23 08:47:52.508602 moosez-2.2.1/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     9211 2023-07-23 08:47:40.000000 moosez-2.2.1/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 08:47:52.508602 moosez-2.2.1/moosez/
+-rw-r--r--   0 runner    (1001) docker     (123)      253 2023-07-23 08:47:40.000000 moosez-2.2.1/moosez/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     2654 2023-07-23 08:47:40.000000 moosez-2.2.1/moosez/constants.py
+-rw-r--r--   0 runner    (1001) docker     (123)     5259 2023-07-23 08:47:40.000000 moosez-2.2.1/moosez/display.py
+-rw-r--r--   0 runner    (1001) docker     (123)     3631 2023-07-23 08:47:40.000000 moosez-2.2.1/moosez/download.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4674 2023-07-23 08:47:40.000000 moosez-2.2.1/moosez/file_utilities.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8067 2023-07-23 08:47:40.000000 moosez-2.2.1/moosez/image_conversion.py
+-rw-r--r--   0 runner    (1001) docker     (123)    22307 2023-07-23 08:47:40.000000 moosez-2.2.1/moosez/image_processing.py
+-rw-r--r--   0 runner    (1001) docker     (123)     4557 2023-07-23 08:47:40.000000 moosez-2.2.1/moosez/input_validation.py
+-rw-r--r--   0 runner    (1001) docker     (123)    10215 2023-07-23 08:47:40.000000 moosez-2.2.1/moosez/moosez.py
+-rw-r--r--   0 runner    (1001) docker     (123)    12807 2023-07-23 08:47:40.000000 moosez-2.2.1/moosez/predict.py
+-rw-r--r--   0 runner    (1001) docker     (123)     6063 2023-07-23 08:47:40.000000 moosez-2.2.1/moosez/resources.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 08:47:52.508602 moosez-2.2.1/moosez.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     1432 2023-07-23 08:47:52.000000 moosez-2.2.1/moosez.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      445 2023-07-23 08:47:52.000000 moosez-2.2.1/moosez.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 08:47:52.000000 moosez-2.2.1/moosez.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       46 2023-07-23 08:47:52.000000 moosez-2.2.1/moosez.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      268 2023-07-23 08:47:52.000000 moosez-2.2.1/moosez.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        7 2023-07-23 08:47:52.000000 moosez-2.2.1/moosez.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       38 2023-07-23 08:47:52.508602 moosez-2.2.1/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     2320 2023-07-23 08:47:40.000000 moosez-2.2.1/setup.py
```

### Comparing `moosez-2.2.0/LICENSE` & `moosez-2.2.1/LICENSE`

 * *Files identical despite different names*

### Comparing `moosez-2.2.0/PKG-INFO` & `moosez-2.2.1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: moosez
-Version: 2.2.0
+Version: 2.2.1
 Summary: An AI-inference engine for 3D clinical and preclinical whole-body segmentation tasks
 Home-page: https://github.com/QIMP-Team/mooseZ
 Author: Lalith Kumar Shiyam Sundar | Sebastian Gutschmayer
 Author-email: Lalith.shiyamsundar@meduniwien.ac.at
 License: Apache 2.0
 Keywords: moosez model-zoo nnUNet medical-imaging tumor-segmentation organ-segmentation bone-segmentation lung-segmentation muscle-segmentation fat-segmentation vessel-segmentation vertebral-segmentation rib-segmentation preclinical-segmentation clinical-segmentation
 Classifier: Development Status :: 4 - Beta
```

### Comparing `moosez-2.2.0/README.md` & `moosez-2.2.1/README.md`

 * *Files identical despite different names*

### Comparing `moosez-2.2.0/moosez/constants.py` & `moosez-2.2.1/moosez/constants.py`

 * *Files identical despite different names*

### Comparing `moosez-2.2.0/moosez/display.py` & `moosez-2.2.1/moosez/display.py`

 * *Files identical despite different names*

### Comparing `moosez-2.2.0/moosez/download.py` & `moosez-2.2.1/moosez/download.py`

 * *Files identical despite different names*

### Comparing `moosez-2.2.0/moosez/file_utilities.py` & `moosez-2.2.1/moosez/file_utilities.py`

 * *Files identical despite different names*

### Comparing `moosez-2.2.0/moosez/image_conversion.py` & `moosez-2.2.1/moosez/image_conversion.py`

 * *Files identical despite different names*

### Comparing `moosez-2.2.0/moosez/image_processing.py` & `moosez-2.2.1/moosez/image_processing.py`

 * *Files identical despite different names*

### Comparing `moosez-2.2.0/moosez/input_validation.py` & `moosez-2.2.1/moosez/input_validation.py`

 * *Files identical despite different names*

### Comparing `moosez-2.2.0/moosez/moosez.py` & `moosez-2.2.1/moosez/moosez.py`

 * *Files 4% similar despite different names*

```diff
@@ -206,12 +206,20 @@
 
     spinner.succeed(f'{constants.ANSI_GREEN} All predictions done! | Total elapsed time for '
                     f'{len(moose_compliant_subjects)} datasets: {round(total_elapsed_time, 1)} min'
                     f' | Time per dataset: {round(time_per_dataset, 2)} min {constants.ANSI_RESET}')
 
 
 def moose(model_name: str, input_dir: str, output_dir: str, accelerator: str):
+    model_path = constants.NNUNET_RESULTS_FOLDER
+    file_utilities.create_directory(model_path)
+    download.model(model_name, model_path)
+    input_validation.make_nnunet_compatible(input_dir)
+    spinner = Halo(text=f'{constants.ANSI_VIOLET} Running prediction...{constants.ANSI_RESET}',
+                   spinner='dots')
+    spinner.start()
     predict.predict(model_name, input_dir, output_dir, accelerator)
+    spinner.succeed(f'{constants.ANSI_GREEN}Prediction done! {constants.ANSI_RESET}')
 
 
 if __name__ == '__main__':
     main()
```

### Comparing `moosez-2.2.0/moosez/predict.py` & `moosez-2.2.1/moosez/predict.py`

 * *Files identical despite different names*

### Comparing `moosez-2.2.0/moosez/resources.py` & `moosez-2.2.1/moosez/resources.py`

 * *Files identical despite different names*

### Comparing `moosez-2.2.0/moosez.egg-info/PKG-INFO` & `moosez-2.2.1/moosez.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: moosez
-Version: 2.2.0
+Version: 2.2.1
 Summary: An AI-inference engine for 3D clinical and preclinical whole-body segmentation tasks
 Home-page: https://github.com/QIMP-Team/mooseZ
 Author: Lalith Kumar Shiyam Sundar | Sebastian Gutschmayer
 Author-email: Lalith.shiyamsundar@meduniwien.ac.at
 License: Apache 2.0
 Keywords: moosez model-zoo nnUNet medical-imaging tumor-segmentation organ-segmentation bone-segmentation lung-segmentation muscle-segmentation fat-segmentation vessel-segmentation vertebral-segmentation rib-segmentation preclinical-segmentation clinical-segmentation
 Classifier: Development Status :: 4 - Beta
```

### Comparing `moosez-2.2.0/setup.py` & `moosez-2.2.1/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from setuptools import setup, find_packages
 
 setup(
     name='moosez',
-    version='2.2.0',
+    version='2.2.1',
     author='Lalith Kumar Shiyam Sundar | Sebastian Gutschmayer',
     author_email='Lalith.shiyamsundar@meduniwien.ac.at',
     description='An AI-inference engine for 3D clinical and preclinical whole-body segmentation tasks',
     python_requires='>=3.9',
     long_description='mooseZ is an AI-inference engine based on nnUNet, designed for 3D clinical and preclinical'
                      ' whole-body segmentation tasks. It serves models tailored towards different modalities such'
                      ' as PET, CT, and MR. mooseZ provides fast and accurate segmentation results, making it a '
```

