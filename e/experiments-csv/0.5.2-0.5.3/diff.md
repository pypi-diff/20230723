# Comparing `tmp/experiments_csv-0.5.2.tar.gz` & `tmp/experiments_csv-0.5.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "experiments_csv-0.5.2.tar", last modified: Sun Jul 23 13:53:50 2023, max compression
+gzip compressed data, was "experiments_csv-0.5.3.tar", last modified: Sun Jul 23 14:15:28 2023, max compression
```

## Comparing `experiments_csv-0.5.2.tar` & `experiments_csv-0.5.3.tar`

### file list

```diff
@@ -1,24 +1,24 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 13:53:50.205898 experiments_csv-0.5.2/
-drwxrwxrwx   0        0        0        0 2023-07-23 13:53:50.195998 experiments_csv-0.5.2/.pytest_cache/
--rw-rw-rw-   0        0        0      310 2023-07-23 13:51:55.000000 experiments_csv-0.5.2/.pytest_cache/README.md
--rw-rw-rw-   0        0        0     1055 2022-05-24 07:51:17.000000 experiments_csv-0.5.2/LICENSE
--rw-rw-rw-   0        0        0      112 2022-05-24 07:51:17.000000 experiments_csv-0.5.2/MANIFEST.in
--rw-rw-rw-   0        0        0     4189 2023-07-23 13:53:50.205898 experiments_csv-0.5.2/PKG-INFO
--rw-rw-rw-   0        0        0     3566 2022-06-30 10:51:58.000000 experiments_csv-0.5.2/README.md
-drwxrwxrwx   0        0        0        0 2023-07-23 13:53:50.200761 experiments_csv-0.5.2/experiments_csv/
--rw-rw-rw-   0        0        0     8414 2022-07-04 14:17:36.000000 experiments_csv-0.5.2/experiments_csv/Experiment.py
--rw-rw-rw-   0        0        0        7 2023-07-23 13:46:08.000000 experiments_csv-0.5.2/experiments_csv/VERSION
--rw-rw-rw-   0        0        0      267 2022-07-05 07:42:29.000000 experiments_csv-0.5.2/experiments_csv/__init__.py
--rw-rw-rw-   0        0        0     1153 2022-05-24 07:51:17.000000 experiments_csv-0.5.2/experiments_csv/dict_product.py
--rw-rw-rw-   0        0        0     5398 2023-07-23 13:51:32.000000 experiments_csv-0.5.2/experiments_csv/dict_to_row.py
--rw-rw-rw-   0        0        0     7584 2023-07-23 13:44:03.000000 experiments_csv-0.5.2/experiments_csv/plot_results.py
-drwxrwxrwx   0        0        0        0 2023-07-23 13:53:50.204898 experiments_csv-0.5.2/experiments_csv.egg-info/
--rw-rw-rw-   0        0        0     4189 2023-07-23 13:53:49.000000 experiments_csv-0.5.2/experiments_csv.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      465 2023-07-23 13:53:50.000000 experiments_csv-0.5.2/experiments_csv.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 13:53:49.000000 experiments_csv-0.5.2/experiments_csv.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       30 2023-07-23 13:53:49.000000 experiments_csv-0.5.2/experiments_csv.egg-info/requires.txt
--rw-rw-rw-   0        0        0       16 2023-07-23 13:53:49.000000 experiments_csv-0.5.2/experiments_csv.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      302 2022-05-24 07:51:17.000000 experiments_csv-0.5.2/pyproject.toml
--rw-rw-rw-   0        0        0        8 2023-07-23 13:46:54.000000 experiments_csv-0.5.2/requirements.txt
--rw-rw-rw-   0        0        0       42 2023-07-23 13:53:50.205898 experiments_csv-0.5.2/setup.cfg
--rw-rw-rw-   0        0        0     1679 2022-07-12 07:42:16.000000 experiments_csv-0.5.2/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 14:15:28.596269 experiments_csv-0.5.3/
+drwxrwxrwx   0        0        0        0 2023-07-23 14:15:28.586135 experiments_csv-0.5.3/.pytest_cache/
+-rw-rw-rw-   0        0        0      310 2023-07-23 13:51:55.000000 experiments_csv-0.5.3/.pytest_cache/README.md
+-rw-rw-rw-   0        0        0     1055 2022-05-24 07:51:17.000000 experiments_csv-0.5.3/LICENSE
+-rw-rw-rw-   0        0        0      112 2022-05-24 07:51:17.000000 experiments_csv-0.5.3/MANIFEST.in
+-rw-rw-rw-   0        0        0     4189 2023-07-23 14:15:28.593263 experiments_csv-0.5.3/PKG-INFO
+-rw-rw-rw-   0        0        0     3566 2022-06-30 10:51:58.000000 experiments_csv-0.5.3/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 14:15:28.589256 experiments_csv-0.5.3/experiments_csv/
+-rw-rw-rw-   0        0        0     8414 2022-07-04 14:17:36.000000 experiments_csv-0.5.3/experiments_csv/Experiment.py
+-rw-rw-rw-   0        0        0        7 2023-07-23 14:13:09.000000 experiments_csv-0.5.3/experiments_csv/VERSION
+-rw-rw-rw-   0        0        0      267 2022-07-05 07:42:29.000000 experiments_csv-0.5.3/experiments_csv/__init__.py
+-rw-rw-rw-   0        0        0     1153 2022-05-24 07:51:17.000000 experiments_csv-0.5.3/experiments_csv/dict_product.py
+-rw-rw-rw-   0        0        0     5398 2023-07-23 13:51:32.000000 experiments_csv-0.5.3/experiments_csv/dict_to_row.py
+-rw-rw-rw-   0        0        0     8018 2023-07-23 14:12:53.000000 experiments_csv-0.5.3/experiments_csv/plot_results.py
+drwxrwxrwx   0        0        0        0 2023-07-23 14:15:28.593263 experiments_csv-0.5.3/experiments_csv.egg-info/
+-rw-rw-rw-   0        0        0     4189 2023-07-23 14:15:28.000000 experiments_csv-0.5.3/experiments_csv.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      465 2023-07-23 14:15:28.000000 experiments_csv-0.5.3/experiments_csv.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 14:15:28.000000 experiments_csv-0.5.3/experiments_csv.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       30 2023-07-23 14:15:28.000000 experiments_csv-0.5.3/experiments_csv.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       16 2023-07-23 14:15:28.000000 experiments_csv-0.5.3/experiments_csv.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      302 2022-05-24 07:51:17.000000 experiments_csv-0.5.3/pyproject.toml
+-rw-rw-rw-   0        0        0        8 2023-07-23 13:46:54.000000 experiments_csv-0.5.3/requirements.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 14:15:28.596269 experiments_csv-0.5.3/setup.cfg
+-rw-rw-rw-   0        0        0     1679 2022-07-12 07:42:16.000000 experiments_csv-0.5.3/setup.py
```

### Comparing `experiments_csv-0.5.2/LICENSE` & `experiments_csv-0.5.3/LICENSE`

 * *Files identical despite different names*

### Comparing `experiments_csv-0.5.2/PKG-INFO` & `experiments_csv-0.5.3/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: experiments_csv
-Version: 0.5.2
+Version: 0.5.3
 Summary: Simple framework for running simulation experiments and recording them in a CSV file
 Home-page: https://github.com/erelsgl/experiments_csv
 Author: Erel Segal-Halevi
 Author-email: erelsgl@gmail.com
 License: MIT
 Project-URL: Bug Reports, https://github.com/erelsgl/experiments_csv/issues
 Project-URL: Source Code, https://github.com/erelsgl/experiments_csv
```

### Comparing `experiments_csv-0.5.2/README.md` & `experiments_csv-0.5.3/README.md`

 * *Files identical despite different names*

### Comparing `experiments_csv-0.5.2/experiments_csv/Experiment.py` & `experiments_csv-0.5.3/experiments_csv/Experiment.py`

 * *Files identical despite different names*

### Comparing `experiments_csv-0.5.2/experiments_csv/dict_product.py` & `experiments_csv-0.5.3/experiments_csv/dict_product.py`

 * *Files identical despite different names*

### Comparing `experiments_csv-0.5.2/experiments_csv/dict_to_row.py` & `experiments_csv-0.5.3/experiments_csv/dict_to_row.py`

 * *Files identical despite different names*

### Comparing `experiments_csv-0.5.2/experiments_csv/plot_results.py` & `experiments_csv-0.5.3/experiments_csv/plot_results.py`

 * *Files 7% similar despite different names*

```diff
@@ -57,15 +57,15 @@
         except AttributeError:
             ax.ylim(*ylim)
 
 
 
 def single_plot_results(results_csv_file:str, filter:dict, 
     x_field:str, y_field:str, z_field:str, mean:bool=True, 
-    save_to_file:bool=False, legend_properties={'size':8}, 
+    save_to_file:str=None, legend_properties={'size':8}, 
     **kwargs):
     """
     Make a single plot of results from the given file.
 
     :param results_csv_file  path to the CSV file containing the results.
     :param filter: a dict used to filter the rows of the results file. See dict_to_row.
 
@@ -91,27 +91,32 @@
 
     plt.xlabel(x_field)
     ylabel = f"mean {y_field}" if mean else y_field
     plt.ylabel(ylabel)
     plt.title(title)
 
     if save_to_file:
-        output_file = results_csv_file.replace(".csv",".png")
+        if save_to_file == True:
+            output_file = results_csv_file.replace(".csv",".png")
+        elif isinstance(save_to_file,str):
+            output_file = save_to_file
+        else:
+            raise TypeError(f"Unsupported type of save_to_file: {save_to_file}")
         plt.savefig(output_file)
     else:
         plt.show()
 
 
 
 
 def multi_plot_results(results_csv_file:str, filter:dict,
     x_field:str, y_field:str, z_field:str, mean:bool, 
     subplot_field:str, subplot_rows:int, subplot_cols:int, 
     sharex: bool=False, sharey: bool=False,
-    save_to_file:bool=False,
+    save_to_file:str=None,
     legend_properties={'size':8}, **kwargs):
     """
     Make multiple plots (on subplots of the same figure), each time with a different value of the subplot_field column.
 
     :param results_csv_file  path to the CSV file containing the results.
     :param filter: a dict used to filter the rows of the results file. See dict_to_row.
 
@@ -165,16 +170,21 @@
 
     fig.supxlabel(x_field)
     ylabel = f"mean {y_field}" if mean else y_field
     fig.supylabel(ylabel)
     fig.suptitle(suptitle)
 
     if save_to_file:
-        output_file = results_csv_file.replace(".csv",".png")
-        fig.savefig(output_file)
+        if save_to_file == True:
+            output_file = results_csv_file.replace(".csv",".png")
+        elif isinstance(save_to_file,str):
+            output_file = save_to_file
+        else:
+            raise TypeError(f"Unsupported type of save_to_file: {save_to_file}")
+        plt.savefig(output_file)
     else:
         plt.show()
 
 
 plot_dataframe.logger = single_plot_results.logger = multi_plot_results.logger = logger
 logger.setLevel(logging.INFO)
 logger.addHandler(logging.StreamHandler())
```

### Comparing `experiments_csv-0.5.2/experiments_csv.egg-info/PKG-INFO` & `experiments_csv-0.5.3/experiments_csv.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: experiments-csv
-Version: 0.5.2
+Version: 0.5.3
 Summary: Simple framework for running simulation experiments and recording them in a CSV file
 Home-page: https://github.com/erelsgl/experiments_csv
 Author: Erel Segal-Halevi
 Author-email: erelsgl@gmail.com
 License: MIT
 Project-URL: Bug Reports, https://github.com/erelsgl/experiments_csv/issues
 Project-URL: Source Code, https://github.com/erelsgl/experiments_csv
```

### Comparing `experiments_csv-0.5.2/setup.py` & `experiments_csv-0.5.3/setup.py`

 * *Files identical despite different names*

