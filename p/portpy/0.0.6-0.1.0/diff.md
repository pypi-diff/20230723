# Comparing `tmp/portpy-0.0.6.tar.gz` & `tmp/portpy-0.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dist\portpy-0.0.6.tar", last modified: Mon Jul  3 16:49:37 2023, max compression
+gzip compressed data, was "dist\portpy-0.1.0.tar", last modified: Sun Jul 23 15:00:51 2023, max compression
```

## Comparing `portpy-0.0.6.tar` & `portpy-0.1.0.tar`

### file list

```diff
@@ -1,43 +1,77 @@
-drwxrwxrwx   0        0        0        0 2023-07-03 16:49:37.000000 portpy-0.0.6/
--rw-rw-rw-   0        0        0      142 2023-06-13 16:08:24.000000 portpy-0.0.6/MANIFEST.in
--rw-rw-rw-   0        0        0     8193 2023-07-03 16:49:37.000000 portpy-0.0.6/PKG-INFO
--rw-rw-rw-   0        0        0     6587 2023-06-13 18:42:32.000000 portpy-0.0.6/README.md
-drwxrwxrwx   0        0        0        0 2023-07-03 16:49:35.000000 portpy-0.0.6/images/
--rw-rw-rw-   0        0        0   184526 2023-05-12 05:53:35.000000 portpy-0.0.6/images/PortPy_logo.jpg
-drwxrwxrwx   0        0        0        0 2023-07-03 16:49:35.000000 portpy-0.0.6/portpy/
--rw-rw-rw-   0        0        0       52 2023-07-03 16:46:25.000000 portpy-0.0.6/portpy/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-03 16:49:35.000000 portpy-0.0.6/portpy/config_files/
--rw-rw-rw-   0        0        0        0 2023-06-13 16:25:21.000000 portpy-0.0.6/portpy/config_files/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-03 16:49:35.000000 portpy-0.0.6/portpy/config_files/clinical_criteria/
-drwxrwxrwx   0        0        0        0 2023-07-03 16:49:35.000000 portpy-0.0.6/portpy/config_files/clinical_criteria/Default/
--rw-rw-rw-   0        0        0     2511 2023-01-19 21:58:41.000000 portpy-0.0.6/portpy/config_files/clinical_criteria/Default/Lung_2Gy_30Fx.json
-drwxrwxrwx   0        0        0        0 2023-07-03 16:49:35.000000 portpy-0.0.6/portpy/config_files/optimization_params/
--rw-rw-rw-   0        0        0     2419 2023-06-21 16:45:36.000000 portpy-0.0.6/portpy/config_files/optimization_params/optimization_params_Lung_2Gy_30Fx.json
-drwxrwxrwx   0        0        0        0 2023-07-03 16:49:35.000000 portpy-0.0.6/portpy/photon/
--rw-rw-rw-   0        0        0      395 2023-06-12 21:08:08.000000 portpy-0.0.6/portpy/photon/__init__.py
--rw-rw-rw-   0        0        0     8347 2023-06-13 17:33:26.000000 portpy-0.0.6/portpy/photon/beam.py
--rw-rw-rw-   0        0        0     4994 2023-06-13 15:49:21.000000 portpy-0.0.6/portpy/photon/clinical_criteria.py
--rw-rw-rw-   0        0        0      702 2023-06-13 15:15:28.000000 portpy-0.0.6/portpy/photon/ct.py
--rw-rw-rw-   0        0        0    23555 2023-06-29 15:51:21.000000 portpy-0.0.6/portpy/photon/data_explorer.py
--rw-rw-rw-   0        0        0    15901 2023-06-22 18:40:10.000000 portpy-0.0.6/portpy/photon/evaluation.py
--rw-rw-rw-   0        0        0    48833 2023-06-29 15:52:51.000000 portpy-0.0.6/portpy/photon/influence_matrix.py
--rw-rw-rw-   0        0        0    22066 2023-07-01 16:00:32.000000 portpy-0.0.6/portpy/photon/optimization.py
--rw-rw-rw-   0        0        0     5806 2023-06-13 15:50:40.000000 portpy-0.0.6/portpy/photon/plan.py
--rw-rw-rw-   0        0        0    16378 2023-06-13 17:27:58.000000 portpy-0.0.6/portpy/photon/structures.py
-drwxrwxrwx   0        0        0        0 2023-07-03 16:49:35.000000 portpy-0.0.6/portpy/photon/utils/
--rw-rw-rw-   0        0        0      342 2023-06-21 21:52:31.000000 portpy-0.0.6/portpy/photon/utils/__init__.py
--rw-rw-rw-   0        0        0     2925 2023-07-03 15:57:47.000000 portpy-0.0.6/portpy/photon/utils/convert_dose_rt_dicom_to_portpy.py
--rw-rw-rw-   0        0        0     2482 2023-07-01 16:42:21.000000 portpy-0.0.6/portpy/photon/utils/get_eclipse_fluence.py
--rw-rw-rw-   0        0        0     2846 2023-05-15 12:19:37.000000 portpy-0.0.6/portpy/photon/utils/save_nrrd.py
--rw-rw-rw-   0        0        0     4887 2023-05-15 11:43:22.000000 portpy-0.0.6/portpy/photon/utils/save_or_load_pickle.py
--rw-rw-rw-   0        0        0     1387 2023-05-09 07:09:19.000000 portpy-0.0.6/portpy/photon/utils/slicer_script.py
--rw-rw-rw-   0        0        0     4188 2023-06-12 16:42:02.000000 portpy-0.0.6/portpy/photon/utils/view_in_slicer_jupyter.py
--rw-rw-rw-   0        0        0    23970 2023-06-13 17:30:49.000000 portpy-0.0.6/portpy/photon/visualization.py
-drwxrwxrwx   0        0        0        0 2023-07-03 16:49:35.000000 portpy-0.0.6/portpy.egg-info/
--rw-rw-rw-   0        0        0     8193 2023-07-03 16:49:33.000000 portpy-0.0.6/portpy.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      993 2023-07-03 16:49:33.000000 portpy-0.0.6/portpy.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-03 16:49:33.000000 portpy-0.0.6/portpy.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0      367 2023-07-03 16:49:33.000000 portpy-0.0.6/portpy.egg-info/requires.txt
--rw-rw-rw-   0        0        0        7 2023-07-03 16:49:33.000000 portpy-0.0.6/portpy.egg-info/top_level.txt
--rw-rw-rw-   0        0        0       42 2023-07-03 16:49:37.000000 portpy-0.0.6/setup.cfg
--rw-rw-rw-   0        0        0     2529 2023-06-30 17:21:11.000000 portpy-0.0.6/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 15:00:51.000000 portpy-0.1.0/
+-rw-rw-rw-   0        0        0      142 2023-06-13 16:08:24.000000 portpy-0.1.0/MANIFEST.in
+-rw-rw-rw-   0        0        0    14876 2023-07-23 15:00:51.000000 portpy-0.1.0/PKG-INFO
+-rw-rw-rw-   0        0        0    12846 2023-07-22 01:48:07.000000 portpy-0.1.0/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 15:00:47.000000 portpy-0.1.0/images/
+-rw-rw-rw-   0        0        0   184526 2023-05-12 05:53:35.000000 portpy-0.1.0/images/PortPy_logo.jpg
+-rw-rw-rw-   0        0        0   179242 2023-07-20 15:30:39.000000 portpy-0.1.0/images/dose_comp.JPG
+-rw-rw-rw-   0        0        0   161858 2023-07-20 15:59:20.000000 portpy-0.1.0/images/planner_vs_portpy_dvh.JPG
+drwxrwxrwx   0        0        0        0 2023-07-23 15:00:47.000000 portpy-0.1.0/portpy/
+-rw-rw-rw-   0        0        0       52 2023-07-21 19:33:51.000000 portpy-0.1.0/portpy/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 15:00:47.000000 portpy-0.1.0/portpy/ai/
+-rw-rw-rw-   0        0        0        2 2023-07-21 17:36:30.000000 portpy-0.1.0/portpy/ai/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 15:00:47.000000 portpy-0.1.0/portpy/ai/data/
+-rw-rw-rw-   0        0        0     3724 2023-07-21 19:16:53.000000 portpy-0.1.0/portpy/ai/data/__init__.py
+-rw-rw-rw-   0        0        0     9475 2023-07-21 19:16:53.000000 portpy-0.1.0/portpy/ai/data/base_dataset.py
+-rw-rw-rw-   0        0        0     3675 2023-07-21 19:16:53.000000 portpy-0.1.0/portpy/ai/data/dosepred3d_dataset.py
+-rw-rw-rw-   0        0        0     2005 2023-07-21 19:16:53.000000 portpy-0.1.0/portpy/ai/data/image_folder.py
+-rw-rw-rw-   0        0        0     2353 2023-07-21 19:16:53.000000 portpy-0.1.0/portpy/ai/data/single_dataset.py
+-rw-rw-rw-   0        0        0     3583 2023-07-21 19:16:53.000000 portpy-0.1.0/portpy/ai/data/template_dataset.py
+-rw-rw-rw-   0        0        0     4811 2023-07-17 14:00:42.000000 portpy-0.1.0/portpy/ai/example.py
+drwxrwxrwx   0        0        0        0 2023-07-23 15:00:47.000000 portpy-0.1.0/portpy/ai/models/
+-rw-rw-rw-   0        0        0     3139 2023-07-21 19:16:52.000000 portpy-0.1.0/portpy/ai/models/__init__.py
+-rw-rw-rw-   0        0        0    11391 2023-07-21 19:16:52.000000 portpy-0.1.0/portpy/ai/models/base_model.py
+-rw-rw-rw-   0        0        0     7125 2023-07-21 19:16:52.000000 portpy-0.1.0/portpy/ai/models/doseprediction3d_model.py
+-rw-rw-rw-   0        0        0    22899 2023-07-21 19:16:52.000000 portpy-0.1.0/portpy/ai/models/networks3d.py
+-rw-rw-rw-   0        0        0     3490 2023-07-21 19:16:52.000000 portpy-0.1.0/portpy/ai/models/test_model.py
+drwxrwxrwx   0        0        0        0 2023-07-23 15:00:47.000000 portpy-0.1.0/portpy/ai/options/
+-rw-rw-rw-   0        0        0     1838 2023-07-21 19:16:51.000000 portpy-0.1.0/portpy/ai/options/PyesapiTutorial.py
+-rw-rw-rw-   0        0        0      137 2023-07-21 19:16:51.000000 portpy-0.1.0/portpy/ai/options/__init__.py
+-rw-rw-rw-   0        0        0     8196 2023-07-21 19:16:52.000000 portpy-0.1.0/portpy/ai/options/base_options.py
+-rw-rw-rw-   0        0        0     1181 2023-07-21 19:16:51.000000 portpy-0.1.0/portpy/ai/options/test_options.py
+-rw-rw-rw-   0        0        0     3489 2023-07-21 19:16:51.000000 portpy-0.1.0/portpy/ai/options/train_options.py
+-rw-rw-rw-   0        0        0     5048 2023-07-21 15:27:18.000000 portpy-0.1.0/portpy/ai/predict.py
+-rw-rw-rw-   0        0        0     2238 2023-07-07 04:18:05.000000 portpy-0.1.0/portpy/ai/runRandomTrain.py
+-rw-rw-rw-   0        0        0     4596 2023-07-21 19:16:53.000000 portpy-0.1.0/portpy/ai/test.py
+-rw-rw-rw-   0        0        0     9041 2023-07-21 19:16:53.000000 portpy-0.1.0/portpy/ai/train.py
+drwxrwxrwx   0        0        0        0 2023-07-23 15:00:47.000000 portpy-0.1.0/portpy/ai/util/
+-rw-rw-rw-   0        0        0       84 2023-07-21 19:16:52.000000 portpy-0.1.0/portpy/ai/util/__init__.py
+-rw-rw-rw-   0        0        0     3633 2023-07-21 19:16:52.000000 portpy-0.1.0/portpy/ai/util/html.py
+-rw-rw-rw-   0        0        0     2280 2023-07-21 19:16:52.000000 portpy-0.1.0/portpy/ai/util/image_pool.py
+-rw-rw-rw-   0        0        0     4683 2023-07-21 19:16:52.000000 portpy-0.1.0/portpy/ai/util/util.py
+-rw-rw-rw-   0        0        0    10211 2023-07-21 19:16:52.000000 portpy-0.1.0/portpy/ai/util/visualizer.py
+drwxrwxrwx   0        0        0        0 2023-07-23 15:00:47.000000 portpy-0.1.0/portpy/config_files/
+-rw-rw-rw-   0        0        0        0 2023-06-13 16:25:21.000000 portpy-0.1.0/portpy/config_files/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 15:00:47.000000 portpy-0.1.0/portpy/config_files/clinical_criteria/
+drwxrwxrwx   0        0        0        0 2023-07-23 15:00:47.000000 portpy-0.1.0/portpy/config_files/clinical_criteria/Default/
+-rw-rw-rw-   0        0        0     2511 2023-01-19 21:58:41.000000 portpy-0.1.0/portpy/config_files/clinical_criteria/Default/Lung_2Gy_30Fx.json
+drwxrwxrwx   0        0        0        0 2023-07-23 15:00:47.000000 portpy-0.1.0/portpy/config_files/optimization_params/
+-rw-rw-rw-   0        0        0     2420 2023-07-20 02:01:09.000000 portpy-0.1.0/portpy/config_files/optimization_params/optimization_params_Lung_2Gy_30Fx.json
+drwxrwxrwx   0        0        0        0 2023-07-23 15:00:47.000000 portpy-0.1.0/portpy/photon/
+-rw-rw-rw-   0        0        0      395 2023-06-12 21:08:08.000000 portpy-0.1.0/portpy/photon/__init__.py
+-rw-rw-rw-   0        0        0     8347 2023-06-13 17:33:26.000000 portpy-0.1.0/portpy/photon/beam.py
+-rw-rw-rw-   0        0        0     4994 2023-06-13 15:49:21.000000 portpy-0.1.0/portpy/photon/clinical_criteria.py
+-rw-rw-rw-   0        0        0      702 2023-06-13 15:15:28.000000 portpy-0.1.0/portpy/photon/ct.py
+-rw-rw-rw-   0        0        0    25077 2023-07-20 03:11:35.000000 portpy-0.1.0/portpy/photon/data_explorer.py
+-rw-rw-rw-   0        0        0    16364 2023-07-14 03:03:01.000000 portpy-0.1.0/portpy/photon/evaluation.py
+-rw-rw-rw-   0        0        0    48835 2023-07-09 15:14:12.000000 portpy-0.1.0/portpy/photon/influence_matrix.py
+-rw-rw-rw-   0        0        0    30648 2023-07-18 13:54:30.000000 portpy-0.1.0/portpy/photon/optimization.py
+-rw-rw-rw-   0        0        0     5806 2023-06-13 15:50:40.000000 portpy-0.1.0/portpy/photon/plan.py
+-rw-rw-rw-   0        0        0    16771 2023-07-13 20:57:27.000000 portpy-0.1.0/portpy/photon/structures.py
+drwxrwxrwx   0        0        0        0 2023-07-23 15:00:47.000000 portpy-0.1.0/portpy/photon/utils/
+-rw-rw-rw-   0        0        0      342 2023-06-21 21:52:31.000000 portpy-0.1.0/portpy/photon/utils/__init__.py
+-rw-rw-rw-   0        0        0     2926 2023-07-06 19:02:55.000000 portpy-0.1.0/portpy/photon/utils/convert_dose_rt_dicom_to_portpy.py
+-rw-rw-rw-   0        0        0     2543 2023-07-20 00:45:55.000000 portpy-0.1.0/portpy/photon/utils/get_eclipse_fluence.py
+-rw-rw-rw-   0        0        0     2846 2023-05-15 12:19:37.000000 portpy-0.1.0/portpy/photon/utils/save_nrrd.py
+-rw-rw-rw-   0        0        0     4887 2023-05-15 11:43:22.000000 portpy-0.1.0/portpy/photon/utils/save_or_load_pickle.py
+-rw-rw-rw-   0        0        0     1387 2023-05-09 07:09:19.000000 portpy-0.1.0/portpy/photon/utils/slicer_script.py
+-rw-rw-rw-   0        0        0     4188 2023-06-12 16:42:02.000000 portpy-0.1.0/portpy/photon/utils/view_in_slicer_jupyter.py
+-rw-rw-rw-   0        0        0    24232 2023-07-13 22:49:14.000000 portpy-0.1.0/portpy/photon/visualization.py
+drwxrwxrwx   0        0        0        0 2023-07-23 15:00:47.000000 portpy-0.1.0/portpy.egg-info/
+-rw-rw-rw-   0        0        0    14876 2023-07-23 15:00:40.000000 portpy-0.1.0/portpy.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0     1836 2023-07-23 15:00:41.000000 portpy-0.1.0/portpy.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 15:00:40.000000 portpy-0.1.0/portpy.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0      367 2023-07-23 15:00:40.000000 portpy-0.1.0/portpy.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        7 2023-07-23 15:00:40.000000 portpy-0.1.0/portpy.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 15:00:51.000000 portpy-0.1.0/setup.cfg
+-rw-rw-rw-   0        0        0     2529 2023-06-30 17:21:11.000000 portpy-0.1.0/setup.py
```

### Comparing `portpy-0.0.6/images/PortPy_logo.jpg` & `portpy-0.1.0/images/PortPy_logo.jpg`

 * *Files identical despite different names*

### Comparing `portpy-0.0.6/portpy/config_files/clinical_criteria/Default/Lung_2Gy_30Fx.json` & `portpy-0.1.0/portpy/config_files/clinical_criteria/Default/Lung_2Gy_30Fx.json`

 * *Files identical despite different names*

### Comparing `portpy-0.0.6/portpy/config_files/optimization_params/optimization_params_Lung_2Gy_30Fx.json` & `portpy-0.1.0/portpy/config_files/optimization_params/optimization_params_Lung_2Gy_30Fx.json`

 * *Files 0% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.9975961538461539%*

 * *Differences: {"'objective_functions'": "{12: {'weight': 100}}"}*

```diff
@@ -87,15 +87,15 @@
         {
             "structure_name": "RIND_4",
             "type": "quadratic",
             "weight": 3
         },
         {
             "type": "smoothness-quadratic",
-            "weight": 10
+            "weight": 100
         }
     ],
     "opt_structures": [
         {
             "parameters": {
                 "margin_end_mm": 5,
                 "margin_start_mm": 0,
```

### Comparing `portpy-0.0.6/portpy/photon/beam.py` & `portpy-0.1.0/portpy/photon/beam.py`

 * *Files identical despite different names*

### Comparing `portpy-0.0.6/portpy/photon/clinical_criteria.py` & `portpy-0.1.0/portpy/photon/clinical_criteria.py`

 * *Files identical despite different names*

### Comparing `portpy-0.0.6/portpy/photon/ct.py` & `portpy-0.1.0/portpy/photon/ct.py`

 * *Files identical despite different names*

### Comparing `portpy-0.0.6/portpy/photon/data_explorer.py` & `portpy-0.1.0/portpy/photon/data_explorer.py`

 * *Files 3% similar despite different names*

```diff
@@ -308,14 +308,48 @@
                              'optimization_params_' + protocol_name + '.json')
         # fname = os.path.join('..', 'config_files', 'planner_plan', patient_id, 'planner_plan.json')
         # Opening JSON file
         json_data = DataExplorer.load_json(fname)
         return json_data
 
     @staticmethod
+    def load_config_tcia_patients() -> dict:
+        """
+        Returns TCIA patients metadata
+
+        """
+        # load clinical criteria config metadata
+        fname = os.path.join(Path(__file__).parents[1], 'config_files', 'tcia_patients', 'tcia_patients_metadata.json')
+        # fname = os.path.join('..', 'config_files', 'planner_plan', patient_id, 'planner_plan.json')
+        # Opening JSON file
+        json_data = DataExplorer.load_json(fname)
+        return json_data
+
+    def get_tcia_metadata(self, patient_id: str = None):
+        """
+        Returns tcia patient metadata for the given PortPy patient id
+
+        """
+        if patient_id is None:
+            patient_id = self.patient_id
+        # load clinical criteria config metadata
+        fname = os.path.join(Path(__file__).parents[1], 'config_files', 'tcia_patients', 'tcia_patients_metadata.json')
+        # fname = os.path.join('..', 'config_files', 'planner_plan', patient_id, 'planner_plan.json')
+        # Opening JSON file
+        json_data = DataExplorer.load_json(fname)
+        # Adjust smoothness weight in the objective function to have appropriate MU
+        patient_found = False
+        for i in range(len(json_data['tcia_patients'])):
+            if json_data['tcia_patients'][i]['portpy_patient_id'] == patient_id:
+                print(json_data['tcia_patients'][i])
+                patient_found = True
+        if not patient_found:
+            print('Invalid patient id')
+
+    @staticmethod
     def load_json(file_name):
         f = open(file_name)
         json_data = json.load(f)
         f.close()
         return json_data
 
     def load_data(self, meta_data: dict, load_inf_matrix_full: bool = False) -> dict:
```

### Comparing `portpy-0.0.6/portpy/photon/evaluation.py` & `portpy-0.1.0/portpy/photon/evaluation.py`

 * *Files 4% similar despite different names*

```diff
@@ -45,14 +45,16 @@
 
         :Example:
 
         >>> Evaluation.get_dose(sol=sol, struct='PTV', volume_per=90)
 
         """
         x, y = Evaluation.get_dvh(sol, dose_1d=dose_1d, struct=struct, weight_flag=weight_flag)
+        if np.array_equal(x, np.array([0])) and np.array_equal(y, np.array([0])):
+            return 0
         f = interpolate.interp1d(100 * y, x)
 
         return f(volume_per)
 
     @staticmethod
     def display_clinical_criteria(my_plan: Plan, sol: Union[dict, List[dict]], html_file_name='temp.html',
                                   sol_names: List[str] = None, clinical_criteria: ClinicalCriteria = None,
@@ -216,14 +218,16 @@
 
         :Example:
 
         >>> Evaluation.get_volume(sol=sol, struct='PTV', dose_value_gy=60)
 
         """
         x, y = Evaluation.get_dvh(sol, dose_1d=dose_1d, struct=struct, weight_flag=weight_flag)
+        if np.array_equal(x, np.array([0])) and np.array_equal(y, np.array([0])):
+            return 0
         x1, indices = np.unique(x, return_index=True)
         y1 = y[indices]
         f = interpolate.interp1d(x1, 100 * y1)
         if dose_value_gy > max(x1):
             print('Warning: dose_1d value {} is greater than max dose_1d for {}'.format(dose_value_gy, struct))
             return 0
         else:
@@ -243,14 +247,16 @@
         :Example:
 
         >>> Evaluation.get_dvh(sol=sol, struct='PTV')
 
         """
         inf_matrix = sol['inf_matrix']
         vox = inf_matrix.get_opt_voxels_idx(struct)
+        if len(vox) == 0:
+            return np.array([0]), np.array([0])  # bug fix. if single 0 it can throw error while doing interpolation
         if dose_1d is None:
             dose_1d = sol['dose_1d']
         org_sort_dose = np.sort(dose_1d[vox])
         sort_ind = np.argsort(dose_1d[vox])
         org_sort_dose = np.append(org_sort_dose, org_sort_dose[-1] + 0.01)
         x = org_sort_dose
         if weight_flag:
@@ -279,14 +285,16 @@
         :param dose_1d: dose_1d which is not in solution dictionary
         :param struct: struct_name name
 
         :return: maximum dose_1d for the struct_name
         """
         inf_matrix = sol['inf_matrix']
         vox = inf_matrix.get_opt_voxels_idx(struct)
+        if len(vox) == 0:
+            return 0
         if dose_1d is None:
             dose_1d = sol['dose_1d']
         return np.max(dose_1d[vox])
 
     @staticmethod
     def get_mean_dose(sol: dict, struct: str, dose_1d=None) -> np.ndarray:
         """
@@ -296,14 +304,16 @@
                 :param dose_1d: dose_1d which is not in solution dictionary
                 :param struct: struct_name name
 
                 :return: mean dose_1d for the struct_name
                 """
         inf_matrix = sol['inf_matrix']
         vox = inf_matrix.get_opt_voxels_idx(struct)
+        if len(vox) == 0:
+            return np.array(0)
         if dose_1d is None:
             dose_1d = sol['dose_1d']
         return np.mean(dose_1d[vox])
 
     @staticmethod
     def get_BED(my_plan: Plan, sol: dict = None, dose_per_fraction_1d: np.ndarray = None, alpha=1, beta=1) -> np.ndarray:
         """
```

### Comparing `portpy-0.0.6/portpy/photon/influence_matrix.py` & `portpy-0.1.0/portpy/photon/influence_matrix.py`

 * *Files 0% similar despite different names*

```diff
@@ -695,25 +695,25 @@
                 remove_row = []
                 remove_col = []
                 for row in range(beam_map.shape[0]):
                     if row < beam_map.shape[0] - 1:
                         prev_elem = beam_map[row, :][beam_map[row, :] > -1]
                         next_elem = beam_map[row + 1, :][beam_map[row + 1, :] > -1]
                         matching_elements = np.intersect1d(prev_elem, next_elem)
-                        if len(matching_elements) > 1:
+                        if len(matching_elements) >= 1:
                             if len(prev_elem) <= len(next_elem):
                                 remove_row.append(row)
                             else:
                                 remove_row.append(row + 1)
                 for col in range(beam_map.shape[1]):
                     if col < beam_map.shape[1] - 1:
                         prev_elem = beam_map[:, col][beam_map[:, col] > -1]
                         next_elem = beam_map[:, col + 1][beam_map[:, col + 1] > -1]
                         matching_elements = np.intersect1d(prev_elem, next_elem)
-                        if len(matching_elements) > 1:
+                        if len(matching_elements) >= 1:
                             if len(prev_elem) <= len(next_elem):
                                 remove_col.append(col)
                             else:
                                 remove_col.append(col + 1)
                 mask_rows = np.ones(beam_map.shape[0], dtype=bool)
                 mask_columns = np.ones(beam_map.shape[1], dtype=bool)
                 if len(remove_row) > 0:
```

### Comparing `portpy-0.0.6/portpy/photon/optimization.py` & `portpy-0.1.0/portpy/photon/optimization.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 from __future__ import annotations
 import numpy as np
 import cvxpy as cp
 from typing import List, TYPE_CHECKING, Union
-
+import time
 if TYPE_CHECKING:
     from portpy.photon.plan import Plan
     from portpy.photon.influence_matrix import InfluenceMatrix
 from .clinical_criteria import ClinicalCriteria
 
 
 class Optimization(object):
@@ -30,87 +30,95 @@
         :create_cvxpy_problem(my_plan)
             Create cvxpy objective function and constraints and save them as a list
 
     """
 
     def __init__(self, my_plan: Plan, inf_matrix: InfluenceMatrix = None,
                  clinical_criteria: ClinicalCriteria = None,
-                 opt_params: dict = None):
+                 opt_params: dict = None, vars: dict = None):
         # self.x = None
         self.my_plan = my_plan
         if inf_matrix is None:
             inf_matrix = my_plan.inf_matrix
         self.inf_matrix = inf_matrix
         if clinical_criteria is None:
             clinical_criteria = my_plan.clinical_criteria
         self.clinical_criteria = clinical_criteria
         self.opt_params = opt_params
         self.prescription_gy = opt_params['prescription_gy']
         self.obj = []
         self.constraints = []
-        self.vars = {}
+        if vars is None:
+            x = cp.Variable(inf_matrix.A.shape[1], pos=True, name='x')  # creating variable for beamlet intensity
+            self.vars = {'x': x}
+        else:
+            self.vars = vars
 
     def create_cvxpy_problem(self):
         """
         It runs optimization to create optimal plan based upon clinical criteria
+        :param d: cvxpy variable or expression containing the definition of dose. If not provided, it will use d = Ax by default
 
         :return: cvxpy problem object
 
         """
 
         # unpack data
         my_plan = self.my_plan
         inf_matrix = self.inf_matrix
         opt_params = self.opt_params
         clinical_criteria = self.clinical_criteria
+        x = self.vars['x']
+        obj = self.obj
+        constraints = self.constraints
+
         # self.prescription_gy = opt_params['prescription_gy']
 
         # get opt params for optimization
         obj_funcs = opt_params['objective_functions'] if 'objective_functions' in opt_params else []
         opt_params_constraints = opt_params['constraints'] if 'constraints' in opt_params else []
 
-        # Creating rinds (aka rings, shells)
-        # Rinds are doughnut-shaped structures often created to control the radiation dose to non-specified structures
-        #   They can also control the dose fall-off after PTV.
-
         A = inf_matrix.A
         num_fractions = clinical_criteria.get_num_of_fractions()
         st = inf_matrix
 
-        # Construct optimization problem
-        obj = []
-        constraints = []
-        x = cp.Variable(A.shape[1], pos=True, name='x')
+        # if d is None:
+        #     d = cp.Variable(A.shape[0], pos=True, name='d')  # creating dummy variable for dose
+        #     constraints += [d == A @ x]
+        #     self.vars['d'] = d  # save variable
 
-        self.vars = {'x': x}
+        # Construct optimization problem
 
         # Generating objective functions
         print('Objective Start')
         for i in range(len(obj_funcs)):
             if obj_funcs[i]['type'] == 'quadratic-overdose':
                 if obj_funcs[i]['structure_name'] in my_plan.structures.get_structures():
                     struct = obj_funcs[i]['structure_name']
+                    if len(st.get_opt_voxels_idx(struct)) == 0:  # check if there are any opt voxels for the structure
+                        continue
                     dose_gy = self.get_num(obj_funcs[i]['dose_gy']) / clinical_criteria.get_num_of_fractions()
                     dO = cp.Variable(len(st.get_opt_voxels_idx(struct)), pos=True)
-                    obj += [(1 / len(st.get_opt_voxels_idx(struct))) *
-                            (obj_funcs[i]['weight'] * cp.sum_squares(dO))]
+                    obj += [(1 / len(st.get_opt_voxels_idx(struct))) * (obj_funcs[i]['weight'] * cp.sum_squares(dO))]
                     constraints += [A[st.get_opt_voxels_idx(struct), :] @ x <= dose_gy + dO]
             elif obj_funcs[i]['type'] == 'quadratic-underdose':
                 if obj_funcs[i]['structure_name'] in my_plan.structures.get_structures():
                     struct = obj_funcs[i]['structure_name']
+                    if len(st.get_opt_voxels_idx(struct)) == 0:
+                        continue
                     dose_gy = self.get_num(obj_funcs[i]['dose_gy']) / clinical_criteria.get_num_of_fractions()
                     dU = cp.Variable(len(st.get_opt_voxels_idx(struct)), pos=True)
-                    obj += [(1 / len(st.get_opt_voxels_idx(struct))) *
-                            (obj_funcs[i]['weight'] * cp.sum_squares(dU))]
+                    obj += [(1 / len(st.get_opt_voxels_idx(struct))) * (obj_funcs[i]['weight'] * cp.sum_squares(dU))]
                     constraints += [A[st.get_opt_voxels_idx(struct), :] @ x >= dose_gy - dU]
             elif obj_funcs[i]['type'] == 'quadratic':
                 if obj_funcs[i]['structure_name'] in my_plan.structures.get_structures():
                     struct = obj_funcs[i]['structure_name']
-                    obj += [(1 / len(st.get_opt_voxels_idx(struct))) * (
-                            obj_funcs[i]['weight'] * cp.sum_squares(A[st.get_opt_voxels_idx(struct), :] @ x))]
+                    if len(st.get_opt_voxels_idx(struct)) == 0:
+                        continue
+                    obj += [(1 / len(st.get_opt_voxels_idx(struct))) * (obj_funcs[i]['weight'] * cp.sum_squares(A[st.get_opt_voxels_idx(struct), :] @ x))]
             elif obj_funcs[i]['type'] == 'smoothness-quadratic':
                 [Qx, Qy, num_rows, num_cols] = self.get_smoothness_matrix(inf_matrix.beamlets_dict)
                 smoothness_X_weight = 0.6
                 smoothness_Y_weight = 0.4
                 obj += [obj_funcs[i]['weight'] * (smoothness_X_weight * (1 / num_cols) * cp.sum_squares(Qx @ x) +
                                                   smoothness_Y_weight * (1 / num_rows) * cp.sum_squares(Qy @ x))]
 
@@ -119,60 +127,64 @@
         print('Constraints Start')
 
         # add optimization constraints if present in opt params
         for param in opt_params_constraints:
             # add constraint
             if param['structure_name'] in my_plan.structures.get_structures():
                 parameters = {'structure_name': param['structure_name']}
-                # total_pres = self.get_prescription()
                 if 'max' in param['type']:
                     opt_constraints = {'limit_dose_gy': self.get_num(param['upper_limit'])}
                     clinical_criteria.add_criterion(criterion='max_dose', parameters=parameters,
                                                     constraints=opt_constraints)
                 if 'mean' in param['type']:
                     opt_constraints = {'limit_dose_gy': self.get_num(param['upper_limit'])}
                     clinical_criteria.add_criterion(criterion='mean_dose', parameters=parameters,
                                                     constraints=opt_constraints)
 
-        # get max and mean constraints
+        # get max and mean constraints based upon clinical criteria
         max_constraints = clinical_criteria.get_criteria(
             name='max_dose')  # returns all the max dose criteria as a list
         mean_constraints = clinical_criteria.get_criteria(
             name='mean_dose')  # returns all the mean dose criteria as a list
 
         # Adding max constraints
         for i in range(len(max_constraints)):
             if 'max_dose' in max_constraints[i]['name']:
                 if 'limit_dose_gy' in max_constraints[i]['constraints']:
                     limit = max_constraints[i]['constraints']['limit_dose_gy']
                     org = max_constraints[i]['parameters']['structure_name']
                     if org != 'GTV' and org != 'CTV':
-                        if org in my_plan.structures.structures_dict['name']:
+                        if org in my_plan.structures.get_structures():
+                            if len(st.get_opt_voxels_idx(org)) == 0:
+                                continue
+                            # if d is None:
+                            #     constraints += [A[st.get_opt_voxels_idx(org), :] @ x <= limit / num_fractions]
+                            # else:
                             constraints += [A[st.get_opt_voxels_idx(org), :] @ x <= limit / num_fractions]
                         else:
                             print('Structure {} not available!'.format(org))
 
         # Adding mean constraints
         for i in range(len(mean_constraints)):
             if 'mean_dose' in mean_constraints[i]['name']:
                 if 'limit_dose_gy' in mean_constraints[i]['constraints']:
                     limit = mean_constraints[i]['constraints']['limit_dose_gy']
                     org = mean_constraints[i]['parameters']['structure_name']
                     # mean constraints using voxel weights
-                    if org in my_plan.structures.structures_dict['name']:
+                    if org in my_plan.structures.get_structures():
+                        if len(st.get_opt_voxels_idx(org)) == 0:
+                            continue
                         constraints += [(1 / sum(st.get_opt_voxels_volume_cc(org))) *
-                                        (cp.sum((cp.multiply(st.get_opt_voxels_volume_cc(org), A[st.get_opt_voxels_idx(org),
-                                                                                          :] @ x)))) <= limit / num_fractions]
+                                        (cp.sum((cp.multiply(st.get_opt_voxels_volume_cc(org),
+                                                             A[st.get_opt_voxels_idx(org), :] @ x))))
+                                        <= limit / num_fractions]
 
                     else:
                         print('Structure {} not available!'.format(org))
 
-        self.obj = obj
-        self.constraints = constraints
-
         print('Constraints done')
 
     def add_max(self, struct: str, dose_gy: float):
         """
         Add max constraints to the problem
 
         :param struct: struct_name name
@@ -340,15 +352,20 @@
                         "inf_matrix": my_plan.inf_marix
                         }
 
                 :return: solution dictionary
                 """
 
         problem = cp.Problem(cp.Minimize(sum(self.obj)), constraints=self.constraints)
+        print('Running Optimization..')
+        t = time.time()
         problem.solve(*args, **kwargs)
+        elapsed = time.time() - t
+        print("Optimal value: %s" % problem.value)
+        print("Elapsed time: {} seconds".format(elapsed))
         return {'optimal_intensity': self.vars['x'].value, 'inf_matrix': self.inf_matrix}
 
     def get_sol(self) -> dict:
         """
         Return optimal solution and influence matrix associated with it in the form of dictionary
 
         :Example
@@ -470,14 +487,142 @@
                     ind = beam_map[r, c]
                     DN = beam_map[r + 1, c]
                     if ind * DN >= 0:
                         sCol[ind, ind] = int(1)
                         sCol[ind, DN] = int(-1)
         return sRow, sCol, num_rows, num_cols
 
+    def create_cvxpy_problem_correction(self, d=None, delta=None):
+        """
+        It runs optimization to create optimal plan based upon clinical criteria
+        :param d: cvxpy variable or expression containing the definition of dose. If not provided, it will use d = Ax by default
+        :param delta: constant dose correction term to be used in optimization
+        :return: cvxpy problem object
+
+        """
+        if delta is None:
+            delta = np.zeros(self.inf_matrix.A.shape[0])
+        # unpack data
+        my_plan = self.my_plan
+        inf_matrix = self.inf_matrix
+        opt_params = self.opt_params
+        clinical_criteria = self.clinical_criteria
+        x = self.vars['x']
+        obj = self.obj
+        constraints = self.constraints
+
+        # self.prescription_gy = opt_params['prescription_gy']
+
+        # get opt params for optimization
+        obj_funcs = opt_params['objective_functions'] if 'objective_functions' in opt_params else []
+        opt_params_constraints = opt_params['constraints'] if 'constraints' in opt_params else []
+
+        A = inf_matrix.A
+        num_fractions = clinical_criteria.get_num_of_fractions()
+        st = inf_matrix
+
+        if d is None:
+            d = cp.Variable(A.shape[0], pos=True, name='d')  # creating dummy variable for dose
+            constraints += [d == A @ x]
+        #     self.vars['d'] = d  # save variable
+
+        # Construct optimization problem
+
+        # Generating objective functions
+        print('Objective Start')
+        for i in range(len(obj_funcs)):
+            if obj_funcs[i]['type'] == 'quadratic-overdose':
+                if obj_funcs[i]['structure_name'] in my_plan.structures.get_structures():
+                    struct = obj_funcs[i]['structure_name']
+                    if len(st.get_opt_voxels_idx(struct)) == 0:  # check if there are any opt voxels for the structure
+                        continue
+                    dose_gy = self.get_num(obj_funcs[i]['dose_gy']) / clinical_criteria.get_num_of_fractions()
+                    dO = cp.Variable(len(st.get_opt_voxels_idx(struct)), pos=True)
+                    obj += [(1 / len(st.get_opt_voxels_idx(struct))) * (obj_funcs[i]['weight'] * cp.sum_squares(dO))]
+                    constraints += [d[st.get_opt_voxels_idx(struct)] + delta[st.get_opt_voxels_idx(struct)] <= dose_gy + dO]
+            elif obj_funcs[i]['type'] == 'quadratic-underdose':
+                if obj_funcs[i]['structure_name'] in my_plan.structures.get_structures():
+                    struct = obj_funcs[i]['structure_name']
+                    if len(st.get_opt_voxels_idx(struct)) == 0:
+                        continue
+                    dose_gy = self.get_num(obj_funcs[i]['dose_gy']) / clinical_criteria.get_num_of_fractions()
+                    dU = cp.Variable(len(st.get_opt_voxels_idx(struct)), pos=True)
+                    obj += [(1 / len(st.get_opt_voxels_idx(struct))) * (obj_funcs[i]['weight'] * cp.sum_squares(dU))]
+                    constraints += [d[st.get_opt_voxels_idx(struct)] + delta[st.get_opt_voxels_idx(struct)] >= dose_gy - dU]
+            elif obj_funcs[i]['type'] == 'quadratic':
+                if obj_funcs[i]['structure_name'] in my_plan.structures.get_structures():
+                    struct = obj_funcs[i]['structure_name']
+                    if len(st.get_opt_voxels_idx(struct)) == 0:
+                        continue
+                    obj += [(1 / len(st.get_opt_voxels_idx(struct))) * (obj_funcs[i]['weight'] * cp.sum_squares(d[st.get_opt_voxels_idx(struct)] + delta[st.get_opt_voxels_idx(struct)]))]
+            elif obj_funcs[i]['type'] == 'smoothness-quadratic':
+                [Qx, Qy, num_rows, num_cols] = self.get_smoothness_matrix(inf_matrix.beamlets_dict)
+                smoothness_X_weight = 0.6
+                smoothness_Y_weight = 0.4
+                obj += [obj_funcs[i]['weight'] * (smoothness_X_weight * (1 / num_cols) * cp.sum_squares(Qx @ x) +
+                                                  smoothness_Y_weight * (1 / num_rows) * cp.sum_squares(Qy @ x))]
+
+        print('Objective done')
+
+        print('Constraints Start')
+
+        # add optimization constraints if present in opt params
+        for param in opt_params_constraints:
+            # add constraint
+            if param['structure_name'] in my_plan.structures.get_structures():
+                parameters = {'structure_name': param['structure_name']}
+                if 'max' in param['type']:
+                    opt_constraints = {'limit_dose_gy': self.get_num(param['upper_limit'])}
+                    clinical_criteria.add_criterion(criterion='max_dose', parameters=parameters,
+                                                    constraints=opt_constraints)
+                if 'mean' in param['type']:
+                    opt_constraints = {'limit_dose_gy': self.get_num(param['upper_limit'])}
+                    clinical_criteria.add_criterion(criterion='mean_dose', parameters=parameters,
+                                                    constraints=opt_constraints)
+
+        # get max and mean constraints based upon clinical criteria
+        max_constraints = clinical_criteria.get_criteria(
+            name='max_dose')  # returns all the max dose criteria as a list
+        mean_constraints = clinical_criteria.get_criteria(
+            name='mean_dose')  # returns all the mean dose criteria as a list
+
+        # Adding max constraints
+        for i in range(len(max_constraints)):
+            if 'max_dose' in max_constraints[i]['name']:
+                if 'limit_dose_gy' in max_constraints[i]['constraints']:
+                    limit = max_constraints[i]['constraints']['limit_dose_gy']
+                    org = max_constraints[i]['parameters']['structure_name']
+                    if org != 'GTV' and org != 'CTV':
+                        if org in my_plan.structures.get_structures():
+                            if len(st.get_opt_voxels_idx(org)) == 0:
+                                continue
+                            constraints += [d[st.get_opt_voxels_idx(org)] + delta[st.get_opt_voxels_idx(org)] <= limit / num_fractions]
+                        else:
+                            print('Structure {} not available!'.format(org))
+
+        # Adding mean constraints
+        for i in range(len(mean_constraints)):
+            if 'mean_dose' in mean_constraints[i]['name']:
+                if 'limit_dose_gy' in mean_constraints[i]['constraints']:
+                    limit = mean_constraints[i]['constraints']['limit_dose_gy']
+                    org = mean_constraints[i]['parameters']['structure_name']
+                    # mean constraints using voxel weights
+                    if org in my_plan.structures.get_structures():
+                        if len(st.get_opt_voxels_idx(org)) == 0:
+                            continue
+                        constraints += [(1 / sum(st.get_opt_voxels_volume_cc(org))) *
+                                        (cp.sum((cp.multiply(st.get_opt_voxels_volume_cc(org),
+                                                             d[st.get_opt_voxels_idx(org)] + delta[st.get_opt_voxels_idx(org)]))))
+                                        <= limit / num_fractions]
+
+                    else:
+                        print('Structure {} not available!'.format(org))
+
+        print('Constraints done')
+
     @staticmethod
     def matching_keys(dictionary, search_string):
         get_key = None
         for key, val in dictionary.items():
             if search_string in key:
                 get_key = key
         if get_key is not None:
```

### Comparing `portpy-0.0.6/portpy/photon/plan.py` & `portpy-0.1.0/portpy/photon/plan.py`

 * *Files identical despite different names*

### Comparing `portpy-0.0.6/portpy/photon/structures.py` & `portpy-0.1.0/portpy/photon/structures.py`

 * *Files 0% similar despite different names*

```diff
@@ -68,14 +68,24 @@
 
          :param structure_name: name of the struct_name in plan
          :return: volume of the struct_name
          """
         ind = self.structures_dict['name'].index(structure_name)
         return self.structures_dict['fraction_of_vol_in_calc_box'][ind]
 
+    def get_structure_mask_3d(self, structure_name: str):
+        """
+        Get fraction of volume in calc box for the struct_name
+
+         :param structure_name: name of the struct_name in plan
+         :return: volume of the struct_name
+         """
+        ind = self.structures_dict['name'].index(structure_name)
+        return self.structures_dict['structure_mask_3d'][ind]
+
     def union(self, struct_1_name: str, struct_2_name: str, new_struct_name: str) -> None:
         """
         Create union of two structures struct_1_name and struct_2_name. If str1_or_str2 is not in structures dict,
         it will create new structures. If str1_or_str2 is in structure_dict, it will modify the struct_name
 
         :param struct_1_name: struct_name name for the 1st struct_name
         :param struct_2_name: struct_name name for the 2nd struct_name
```

### Comparing `portpy-0.0.6/portpy/photon/utils/convert_dose_rt_dicom_to_portpy.py` & `portpy-0.1.0/portpy/photon/utils/convert_dose_rt_dicom_to_portpy.py`

 * *Files 1% similar despite different names*

```diff
@@ -10,15 +10,15 @@
     from portpy.photon.plan import Plan
 
 
 def read_dicom_dose(dir_name: str = None, dose_file_name: str = None):
     if dir_name is not None:
         dicom_names = os.listdir(dir_name)
         for dcm in dicom_names:
-            if dcm[:2] == 'RD':
+            if dcm == 'rt_dose':
                 dose_file_name = os.path.join(dir_name, dcm)
 
     dose_img = dcmread(dose_file_name)
     # dose_img = sitk.ReadImage([dcm for dcm in dicom_paths])
     arr_dose = dose_img.pixel_array
     rt_dose = arr_dose * dose_img.DoseGridScaling
     rt_dose_itk = sitk.GetImageFromArray(rt_dose)
```

### Comparing `portpy-0.0.6/portpy/photon/utils/get_eclipse_fluence.py` & `portpy-0.1.0/portpy/photon/utils/get_eclipse_fluence.py`

 * *Files 2% similar despite different names*

```diff
@@ -15,14 +15,16 @@
     :param sol: dictionary containing optimal intensity
     :param path: directory for saving the optimal fluence
     :param beam_ids: list of string containing beam ids
 
     """
     if path is None:
         path = os.getcwd()
+    if not os.path.exists(path):
+        os.makedirs(path)
     tol = 1e-06
     inf_matrix = sol['inf_matrix']
     optimal_fluence_2d = inf_matrix.fluence_1d_to_2d(sol=sol)
     for i in range(len(optimal_fluence_2d)):
         if beam_ids is not None:
             beam_id = beam_ids[i]
         else:
```

### Comparing `portpy-0.0.6/portpy/photon/utils/save_nrrd.py` & `portpy-0.1.0/portpy/photon/utils/save_nrrd.py`

 * *Files identical despite different names*

### Comparing `portpy-0.0.6/portpy/photon/utils/save_or_load_pickle.py` & `portpy-0.1.0/portpy/photon/utils/save_or_load_pickle.py`

 * *Files identical despite different names*

### Comparing `portpy-0.0.6/portpy/photon/utils/slicer_script.py` & `portpy-0.1.0/portpy/photon/utils/slicer_script.py`

 * *Files identical despite different names*

### Comparing `portpy-0.0.6/portpy/photon/utils/view_in_slicer_jupyter.py` & `portpy-0.1.0/portpy/photon/utils/view_in_slicer_jupyter.py`

 * *Files identical despite different names*

### Comparing `portpy-0.0.6/portpy/photon/visualization.py` & `portpy-0.1.0/portpy/photon/visualization.py`

 * *Files 1% similar despite different names*

```diff
@@ -105,14 +105,17 @@
             fig, ax = plt.subplots(figsize=figsize)
         if norm_flag:
             norm_factor = Evaluation.get_dose(sol, dose_1d=dose_1d, struct=norm_struct, volume_per=norm_volume) / pres
             dose_1d = dose_1d / norm_factor
         for i in range(np.size(all_orgs)):
             if all_orgs[i] not in struct_names:
                 continue
+            if my_plan.structures.get_fraction_of_vol_in_calc_box(all_orgs[i]) == 0:  # check if the structure is within calc box
+                print('Skipping Structure {} as it is not within calculation box.'.format(all_orgs[i]))
+                continue
             # for dose_1d in dose_list:
             #
             x, y = Evaluation.get_dvh(sol, struct=all_orgs[i], dose_1d=dose_1d)
             if dose_scale == 'Absolute(Gy)':
                 max_dose = np.maximum(max_dose, x[-1])
                 ax.set_xlabel('Dose (Gy)')
             elif dose_scale == 'Relative(%)':
```

### Comparing `portpy-0.0.6/setup.py` & `portpy-0.1.0/setup.py`

 * *Files identical despite different names*

