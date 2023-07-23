# Comparing `tmp/experiments_csv-0.5.1.tar.gz` & `tmp/experiments_csv-0.5.2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "experiments_csv-0.5.1.tar", last modified: Sun Jul 31 11:39:12 2022, max compression
+gzip compressed data, was "experiments_csv-0.5.2.tar", last modified: Sun Jul 23 13:53:50 2023, max compression
```

## Comparing `experiments_csv-0.5.1.tar` & `experiments_csv-0.5.2.tar`

### file list

```diff
@@ -1,22 +1,24 @@
-drwxrwxrwx   0        0        0        0 2022-07-31 11:39:12.919898 experiments_csv-0.5.1/
--rw-rw-rw-   0        0        0     1055 2022-05-24 07:51:17.000000 experiments_csv-0.5.1/LICENSE
--rw-rw-rw-   0        0        0      112 2022-05-24 07:51:17.000000 experiments_csv-0.5.1/MANIFEST.in
--rw-rw-rw-   0        0        0     4189 2022-07-31 11:39:12.918902 experiments_csv-0.5.1/PKG-INFO
--rw-rw-rw-   0        0        0     3566 2022-06-30 10:51:58.000000 experiments_csv-0.5.1/README.md
-drwxrwxrwx   0        0        0        0 2022-07-31 11:39:12.894965 experiments_csv-0.5.1/experiments_csv/
--rw-rw-rw-   0        0        0     8414 2022-07-04 14:17:36.000000 experiments_csv-0.5.1/experiments_csv/Experiment.py
--rw-rw-rw-   0        0        0        7 2022-07-31 11:38:11.000000 experiments_csv-0.5.1/experiments_csv/VERSION
--rw-rw-rw-   0        0        0      267 2022-07-05 07:42:29.000000 experiments_csv-0.5.1/experiments_csv/__init__.py
--rw-rw-rw-   0        0        0     1153 2022-05-24 07:51:17.000000 experiments_csv-0.5.1/experiments_csv/dict_product.py
--rw-rw-rw-   0        0        0     5085 2022-07-03 16:34:58.000000 experiments_csv-0.5.1/experiments_csv/dict_to_row.py
--rw-rw-rw-   0        0        0     7310 2022-07-08 10:54:54.000000 experiments_csv-0.5.1/experiments_csv/plot_results.py
-drwxrwxrwx   0        0        0        0 2022-07-31 11:39:12.916905 experiments_csv-0.5.1/experiments_csv.egg-info/
--rw-rw-rw-   0        0        0     4189 2022-07-31 11:39:11.000000 experiments_csv-0.5.1/experiments_csv.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      441 2022-07-31 11:39:12.000000 experiments_csv-0.5.1/experiments_csv.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2022-07-31 11:39:11.000000 experiments_csv-0.5.1/experiments_csv.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       41 2022-07-31 11:39:11.000000 experiments_csv-0.5.1/experiments_csv.egg-info/requires.txt
--rw-rw-rw-   0        0        0       16 2022-07-31 11:39:11.000000 experiments_csv-0.5.1/experiments_csv.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      302 2022-05-24 07:51:17.000000 experiments_csv-0.5.1/pyproject.toml
--rw-rw-rw-   0        0        0       20 2022-07-31 11:28:51.000000 experiments_csv-0.5.1/requirements.txt
--rw-rw-rw-   0        0        0       42 2022-07-31 11:39:12.919898 experiments_csv-0.5.1/setup.cfg
--rw-rw-rw-   0        0        0     1679 2022-07-12 07:42:16.000000 experiments_csv-0.5.1/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 13:53:50.205898 experiments_csv-0.5.2/
+drwxrwxrwx   0        0        0        0 2023-07-23 13:53:50.195998 experiments_csv-0.5.2/.pytest_cache/
+-rw-rw-rw-   0        0        0      310 2023-07-23 13:51:55.000000 experiments_csv-0.5.2/.pytest_cache/README.md
+-rw-rw-rw-   0        0        0     1055 2022-05-24 07:51:17.000000 experiments_csv-0.5.2/LICENSE
+-rw-rw-rw-   0        0        0      112 2022-05-24 07:51:17.000000 experiments_csv-0.5.2/MANIFEST.in
+-rw-rw-rw-   0        0        0     4189 2023-07-23 13:53:50.205898 experiments_csv-0.5.2/PKG-INFO
+-rw-rw-rw-   0        0        0     3566 2022-06-30 10:51:58.000000 experiments_csv-0.5.2/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 13:53:50.200761 experiments_csv-0.5.2/experiments_csv/
+-rw-rw-rw-   0        0        0     8414 2022-07-04 14:17:36.000000 experiments_csv-0.5.2/experiments_csv/Experiment.py
+-rw-rw-rw-   0        0        0        7 2023-07-23 13:46:08.000000 experiments_csv-0.5.2/experiments_csv/VERSION
+-rw-rw-rw-   0        0        0      267 2022-07-05 07:42:29.000000 experiments_csv-0.5.2/experiments_csv/__init__.py
+-rw-rw-rw-   0        0        0     1153 2022-05-24 07:51:17.000000 experiments_csv-0.5.2/experiments_csv/dict_product.py
+-rw-rw-rw-   0        0        0     5398 2023-07-23 13:51:32.000000 experiments_csv-0.5.2/experiments_csv/dict_to_row.py
+-rw-rw-rw-   0        0        0     7584 2023-07-23 13:44:03.000000 experiments_csv-0.5.2/experiments_csv/plot_results.py
+drwxrwxrwx   0        0        0        0 2023-07-23 13:53:50.204898 experiments_csv-0.5.2/experiments_csv.egg-info/
+-rw-rw-rw-   0        0        0     4189 2023-07-23 13:53:49.000000 experiments_csv-0.5.2/experiments_csv.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      465 2023-07-23 13:53:50.000000 experiments_csv-0.5.2/experiments_csv.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 13:53:49.000000 experiments_csv-0.5.2/experiments_csv.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       30 2023-07-23 13:53:49.000000 experiments_csv-0.5.2/experiments_csv.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       16 2023-07-23 13:53:49.000000 experiments_csv-0.5.2/experiments_csv.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      302 2022-05-24 07:51:17.000000 experiments_csv-0.5.2/pyproject.toml
+-rw-rw-rw-   0        0        0        8 2023-07-23 13:46:54.000000 experiments_csv-0.5.2/requirements.txt
+-rw-rw-rw-   0        0        0       42 2023-07-23 13:53:50.205898 experiments_csv-0.5.2/setup.cfg
+-rw-rw-rw-   0        0        0     1679 2022-07-12 07:42:16.000000 experiments_csv-0.5.2/setup.py
```

### Comparing `experiments_csv-0.5.1/LICENSE` & `experiments_csv-0.5.2/LICENSE`

 * *Files identical despite different names*

### Comparing `experiments_csv-0.5.1/PKG-INFO` & `experiments_csv-0.5.2/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: experiments_csv
-Version: 0.5.1
+Version: 0.5.2
 Summary: Simple framework for running simulation experiments and recording them in a CSV file
 Home-page: https://github.com/erelsgl/experiments_csv
 Author: Erel Segal-Halevi
 Author-email: erelsgl@gmail.com
 License: MIT
 Project-URL: Bug Reports, https://github.com/erelsgl/experiments_csv/issues
 Project-URL: Source Code, https://github.com/erelsgl/experiments_csv
```

### Comparing `experiments_csv-0.5.1/README.md` & `experiments_csv-0.5.2/README.md`

 * *Files identical despite different names*

### Comparing `experiments_csv-0.5.1/experiments_csv/Experiment.py` & `experiments_csv-0.5.2/experiments_csv/Experiment.py`

 * *Files identical despite different names*

### Comparing `experiments_csv-0.5.1/experiments_csv/dict_product.py` & `experiments_csv-0.5.2/experiments_csv/dict_product.py`

 * *Files identical despite different names*

### Comparing `experiments_csv-0.5.1/experiments_csv/dict_to_row.py` & `experiments_csv-0.5.2/experiments_csv/dict_to_row.py`

 * *Files 4% similar despite different names*

```diff
@@ -23,17 +23,28 @@
     >>> dict_to_rows(df, {"a":1, "b":2, "c":3})
        a  b  c    z
     0  1  2  3  123
     >>> dict_to_rows(df, {"a":1, "b":2, "c":9})
     Empty DataFrame
     Columns: [a, b, c, z]
     Index: []
+    >>> dict_to_rows(df, {"c":[3,9]})
+       a  b  c    z
+    0  1  2  3  123
+    2  1  5  9  159
+    >>> dict_to_rows(df, {"c":{3,9}})
+       a  b  c    z
+    0  1  2  3  123
+    2  1  5  9  159
     """
     for k,v in key.items():
-        df = df[df[k]==v]
+        if isinstance(v, list) or isinstance(v,set):
+            df = df[df[k].isin(v)]
+        else:
+            df = df[df[k]==v]
     return df
 
 def dict_to_row(df: pandas.DataFrame, key:dict)->dict:
     """
     Accepts a DataFrame and a dict mapping column-names to values.
     Searches a row in which the given columns contain the given values.
     Returns one such row if it exists (as a dict), or None if no such row exists.
```

### Comparing `experiments_csv-0.5.1/experiments_csv/plot_results.py` & `experiments_csv-0.5.2/experiments_csv/plot_results.py`

 * *Files 4% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 # from typing import List
 
 import logging
 logger = logging.getLogger(__name__)
 
 def plot_dataframe(ax, results: pandas.DataFrame,
     x_field:str, y_field:str, z_field:str, mean:bool=True, 
-    legend_properties={'size':8}, xlim=None, ylim=None):
+    xlim=None, ylim=None):
     """
     Plot on the given axis, results from the given pandas dataframe.
 
     :param ax      a matplotlib axis to plot on.
     :param results  a DataFrame containing the results to show.
 
     :param x_field: name of column for x axis.
@@ -34,35 +34,38 @@
         results_for_z_value = results[results[z_field]==z_value]
         # label = z_value
         if isinstance(z_value,int):
             label = f"{z_field}={z_value}"
         else:
             label = z_value
         if mean:
-            mean_results_for_z_value = results_for_z_value.groupby([x_field]).mean()
-            ax.plot(mean_results_for_z_value.index, mean_results_for_z_value[y_field], label=label)
+            try:
+                mean_results_for_z_value = results_for_z_value[[x_field,y_field]].groupby([x_field]).mean()
+                ax.plot(mean_results_for_z_value.index, mean_results_for_z_value[y_field], label=label)
+            except:
+                raise TypeError(f"Cannot take the mean when grouping by x_field={x_field}")
         else:
             ax.scatter(results_for_z_value[x_field], results_for_z_value[y_field], label=label)
-        ax.legend(prop=legend_properties)
 
     if xlim is not None:
         try:
             ax.set_xlim(*xlim)
         except AttributeError:
             ax.xlim(*xlim)
     if ylim is not None:
         try:
             ax.set_ylim(*ylim)
         except AttributeError:
             ax.ylim(*ylim)
 
 
+
 def single_plot_results(results_csv_file:str, filter:dict, 
     x_field:str, y_field:str, z_field:str, mean:bool=True, 
-    save_to_file:bool=False,
+    save_to_file:bool=False, legend_properties={'size':8}, 
     **kwargs):
     """
     Make a single plot of results from the given file.
 
     :param results_csv_file  path to the CSV file containing the results.
     :param filter: a dict used to filter the rows of the results file. See dict_to_row.
 
@@ -80,14 +83,15 @@
         title = ", ".join([f"{key}={value}" for key,value in filter.items()])
     else:
         title = "All results"
     logger.info("Plot: %s", title)
     plot_dataframe(plt, results, 
         x_field, y_field, z_field, mean, 
         **kwargs)
+    plt.legend(prop=legend_properties)
 
     plt.xlabel(x_field)
     ylabel = f"mean {y_field}" if mean else y_field
     plt.ylabel(ylabel)
     plt.title(title)
 
     if save_to_file:
@@ -100,15 +104,15 @@
 
 
 def multi_plot_results(results_csv_file:str, filter:dict,
     x_field:str, y_field:str, z_field:str, mean:bool, 
     subplot_field:str, subplot_rows:int, subplot_cols:int, 
     sharex: bool=False, sharey: bool=False,
     save_to_file:bool=False,
-    **kwargs):
+    legend_properties={'size':8}, **kwargs):
     """
     Make multiple plots (on subplots of the same figure), each time with a different value of the subplot_field column.
 
     :param results_csv_file  path to the CSV file containing the results.
     :param filter: a dict used to filter the rows of the results file. See dict_to_row.
 
     :param x_field: name of column for x axis.
@@ -151,14 +155,16 @@
         subtitle = f"{subplot_field}={subplot_value}"
         logger.info("  Subplot: %s",subtitle)
         results_for_subplot_value = results[results[subplot_field]==subplot_value]
         plot_dataframe(axs[axs_index], results_for_subplot_value, 
             x_field, y_field, z_field, mean, 
             **kwargs)
         axs[axs_index].set_title(subtitle)
+        if axs_index==0:
+            axs[axs_index].legend(prop=legend_properties)
         axs_index += 1
 
     fig.supxlabel(x_field)
     ylabel = f"mean {y_field}" if mean else y_field
     fig.supylabel(ylabel)
     fig.suptitle(suptitle)
```

### Comparing `experiments_csv-0.5.1/experiments_csv.egg-info/PKG-INFO` & `experiments_csv-0.5.2/experiments_csv.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: experiments-csv
-Version: 0.5.1
+Version: 0.5.2
 Summary: Simple framework for running simulation experiments and recording them in a CSV file
 Home-page: https://github.com/erelsgl/experiments_csv
 Author: Erel Segal-Halevi
 Author-email: erelsgl@gmail.com
 License: MIT
 Project-URL: Bug Reports, https://github.com/erelsgl/experiments_csv/issues
 Project-URL: Source Code, https://github.com/erelsgl/experiments_csv
```

### Comparing `experiments_csv-0.5.1/setup.py` & `experiments_csv-0.5.2/setup.py`

 * *Files identical despite different names*

