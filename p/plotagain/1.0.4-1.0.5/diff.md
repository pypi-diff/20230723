# Comparing `tmp/plotagain-1.0.4.tar.gz` & `tmp/plotagain-1.0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "plotagain-1.0.4.tar", last modified: Thu Jul 20 18:34:55 2023, max compression
+gzip compressed data, was "plotagain-1.0.5.tar", last modified: Sun Jul 23 14:15:27 2023, max compression
```

## Comparing `plotagain-1.0.4.tar` & `plotagain-1.0.5.tar`

### file list

```diff
@@ -1,24 +1,75 @@
-drwxr-xr-x   0 jeremywilkinson   (501) staff       (20)        0 2023-07-20 18:34:55.212576 plotagain-1.0.4/
--rw-r--r--   0 jeremywilkinson   (501) staff       (20)       26 2023-07-20 12:51:44.000000 plotagain-1.0.4/.gitignore
--rw-r--r--   0 jeremywilkinson   (501) staff       (20)     3892 2023-07-20 18:34:55.212409 plotagain-1.0.4/PKG-INFO
--rw-r--r--   0 jeremywilkinson   (501) staff       (20)     3299 2023-07-20 17:59:37.000000 plotagain-1.0.4/README.md
--rw-r--r--   0 jeremywilkinson   (501) staff       (20)     2159 2023-07-20 18:09:45.000000 plotagain-1.0.4/bitbucket-pipelines.yml
--rw-r--r--   0 jeremywilkinson   (501) staff       (20)      859 2023-07-20 18:21:23.000000 plotagain-1.0.4/pyproject.toml
--rw-r--r--   0 jeremywilkinson   (501) staff       (20)       16 2023-07-20 10:56:02.000000 plotagain-1.0.4/requirements.txt
--rw-r--r--   0 jeremywilkinson   (501) staff       (20)       38 2023-07-20 18:34:55.212631 plotagain-1.0.4/setup.cfg
-drwxr-xr-x   0 jeremywilkinson   (501) staff       (20)        0 2023-07-20 18:34:55.209322 plotagain-1.0.4/src/
-drwxr-xr-x   0 jeremywilkinson   (501) staff       (20)        0 2023-07-20 18:34:55.210992 plotagain-1.0.4/src/plotagain/
--rw-r--r--   0 jeremywilkinson   (501) staff       (20)      109 2023-07-20 18:34:50.000000 plotagain-1.0.4/src/plotagain/__init__.py
--rw-r--r--   0 jeremywilkinson   (501) staff       (20)     2526 2023-07-20 18:00:09.000000 plotagain-1.0.4/src/plotagain/iddict.py
--rw-r--r--   0 jeremywilkinson   (501) staff       (20)     7252 2023-07-20 17:53:49.000000 plotagain-1.0.4/src/plotagain/pyplotcall.py
--rw-r--r--   0 jeremywilkinson   (501) staff       (20)     7882 2023-07-20 18:34:38.000000 plotagain-1.0.4/src/plotagain/saveplotcontext.py
--rw-r--r--   0 jeremywilkinson   (501) staff       (20)      124 2023-07-20 17:53:49.000000 plotagain-1.0.4/src/plotagain/script_template.txt
--rw-r--r--   0 jeremywilkinson   (501) staff       (20)     1930 2023-07-20 17:37:51.000000 plotagain-1.0.4/src/plotagain/utils.py
-drwxr-xr-x   0 jeremywilkinson   (501) staff       (20)        0 2023-07-20 18:34:55.212018 plotagain-1.0.4/src/plotagain.egg-info/
--rw-r--r--   0 jeremywilkinson   (501) staff       (20)     3892 2023-07-20 18:34:55.000000 plotagain-1.0.4/src/plotagain.egg-info/PKG-INFO
--rw-r--r--   0 jeremywilkinson   (501) staff       (20)      450 2023-07-20 18:34:55.000000 plotagain-1.0.4/src/plotagain.egg-info/SOURCES.txt
--rw-r--r--   0 jeremywilkinson   (501) staff       (20)        1 2023-07-20 18:34:55.000000 plotagain-1.0.4/src/plotagain.egg-info/dependency_links.txt
--rw-r--r--   0 jeremywilkinson   (501) staff       (20)       17 2023-07-20 18:34:55.000000 plotagain-1.0.4/src/plotagain.egg-info/requires.txt
--rw-r--r--   0 jeremywilkinson   (501) staff       (20)       10 2023-07-20 18:34:55.000000 plotagain-1.0.4/src/plotagain.egg-info/top_level.txt
-drwxr-xr-x   0 jeremywilkinson   (501) staff       (20)        0 2023-07-20 18:34:55.212167 plotagain-1.0.4/tests/
--rw-r--r--   0 jeremywilkinson   (501) staff       (20)       30 2023-07-20 18:12:48.000000 plotagain-1.0.4/tests/test_nothing.py
+drwxr-xr-x   0 jeremywilkinson   (501) staff       (20)        0 2023-07-23 14:15:27.277085 plotagain-1.0.5/
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)       49 2023-07-23 14:15:06.000000 plotagain-1.0.5/.gitignore
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)     3860 2023-07-23 14:15:27.276894 plotagain-1.0.5/PKG-INFO
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)     3267 2023-07-23 14:13:03.000000 plotagain-1.0.5/README.md
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)     2159 2023-07-20 18:09:45.000000 plotagain-1.0.5/bitbucket-pipelines.yml
+drwxr-xr-x   0 jeremywilkinson   (501) staff       (20)        0 2023-07-23 14:15:27.265892 plotagain-1.0.5/docs/
+drwxr-xr-x   0 jeremywilkinson   (501) staff       (20)        0 2023-07-23 14:15:27.266048 plotagain-1.0.5/docs/build/
+drwxr-xr-x   0 jeremywilkinson   (501) staff       (20)        0 2023-07-23 14:15:27.268211 plotagain-1.0.5/docs/build/doctrees/
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)    17067 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/doctrees/environment.pickle
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)     4971 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/doctrees/index.doctree
+drwxr-xr-x   0 jeremywilkinson   (501) staff       (20)        0 2023-07-23 14:15:27.269640 plotagain-1.0.5/docs/build/html/
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)      230 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/.buildinfo
+drwxr-xr-x   0 jeremywilkinson   (501) staff       (20)        0 2023-07-23 14:15:27.270259 plotagain-1.0.5/docs/build/html/.doctrees/
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)     7208 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/.doctrees/api.doctree
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)   146512 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/.doctrees/environment.pickle
+drwxr-xr-x   0 jeremywilkinson   (501) staff       (20)        0 2023-07-23 14:15:27.270992 plotagain-1.0.5/docs/build/html/.doctrees/generated/
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)     4927 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/.doctrees/generated/plotagain.doctree
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)    78474 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/.doctrees/generated/plotagain.saveplotcontext.SavePlotContext.doctree
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)     5033 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/.doctrees/generated/plotagain.saveplotcontext.doctree
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)     5961 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/.doctrees/generated/plotagain.utils.doctree
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)     6077 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/.doctrees/index.doctree
+drwxr-xr-x   0 jeremywilkinson   (501) staff       (20)        0 2023-07-23 14:15:27.271339 plotagain-1.0.5/docs/build/html/_sources/
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)      155 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/_sources/api.rst.txt
+drwxr-xr-x   0 jeremywilkinson   (501) staff       (20)        0 2023-07-23 14:15:27.272003 plotagain-1.0.5/docs/build/html/_sources/generated/
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)      189 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/_sources/generated/plotagain.rst.txt
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)      809 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/_sources/generated/plotagain.saveplotcontext.SavePlotContext.rst.txt
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)      227 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/_sources/generated/plotagain.saveplotcontext.rst.txt
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)      214 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/_sources/generated/plotagain.utils.rst.txt
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)      770 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/_sources/index.rst.txt
+drwxr-xr-x   0 jeremywilkinson   (501) staff       (20)        0 2023-07-23 14:15:27.273888 plotagain-1.0.5/docs/build/html/_static/
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)    11230 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/_static/alabaster.css
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)    14813 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/_static/basic.css
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)       42 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/_static/custom.css
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)     4472 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/_static/doctools.js
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)      420 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/_static/documentation_options.js
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)      286 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/_static/file.png
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)     4758 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/_static/language_data.js
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)       90 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/_static/minus.png
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)       90 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/_static/plus.png
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)     5327 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/_static/pygments.css
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)    18215 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/_static/searchtools.js
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)     4712 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/_static/sphinx_highlight.js
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)     5063 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/api.html
+drwxr-xr-x   0 jeremywilkinson   (501) staff       (20)        0 2023-07-23 14:15:27.274560 plotagain-1.0.5/docs/build/html/generated/
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)     4040 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/generated/plotagain.html
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)    22895 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/generated/plotagain.saveplotcontext.SavePlotContext.html
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)     4503 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/generated/plotagain.saveplotcontext.html
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)     4113 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/generated/plotagain.utils.html
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)     4619 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/genindex.html
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)     4812 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/index.html
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)      411 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/objects.inv
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)     3572 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/py-modindex.html
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)     2803 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/search.html
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)     5155 2023-07-23 14:13:03.000000 plotagain-1.0.5/docs/build/html/searchindex.js
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)      859 2023-07-20 18:21:23.000000 plotagain-1.0.5/pyproject.toml
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)       16 2023-07-23 14:15:06.000000 plotagain-1.0.5/requirements.txt
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)       38 2023-07-23 14:15:27.277141 plotagain-1.0.5/setup.cfg
+drwxr-xr-x   0 jeremywilkinson   (501) staff       (20)        0 2023-07-23 14:15:27.266854 plotagain-1.0.5/src/
+drwxr-xr-x   0 jeremywilkinson   (501) staff       (20)        0 2023-07-23 14:15:27.275533 plotagain-1.0.5/src/plotagain/
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)      549 2023-07-23 14:15:06.000000 plotagain-1.0.5/src/plotagain/__init__.py
+drwxr-xr-x   0 jeremywilkinson   (501) staff       (20)        0 2023-07-23 14:15:27.276490 plotagain-1.0.5/src/plotagain/data-save-dir/
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)      404 2023-07-23 08:24:22.000000 plotagain-1.0.5/src/plotagain/data-save-dir/make_plot.py
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)     2526 2023-07-20 18:00:09.000000 plotagain-1.0.5/src/plotagain/iddict.py
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)     7252 2023-07-23 14:15:06.000000 plotagain-1.0.5/src/plotagain/pyplotcall.py
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)     8911 2023-07-23 14:15:06.000000 plotagain-1.0.5/src/plotagain/saveplotcontext.py
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)      124 2023-07-20 17:53:49.000000 plotagain-1.0.5/src/plotagain/script_template.txt
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)     1930 2023-07-23 14:15:06.000000 plotagain-1.0.5/src/plotagain/utils.py
+drwxr-xr-x   0 jeremywilkinson   (501) staff       (20)        0 2023-07-23 14:15:27.276330 plotagain-1.0.5/src/plotagain.egg-info/
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)     3860 2023-07-23 14:15:27.000000 plotagain-1.0.5/src/plotagain.egg-info/PKG-INFO
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)     2199 2023-07-23 14:15:27.000000 plotagain-1.0.5/src/plotagain.egg-info/SOURCES.txt
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)        1 2023-07-23 14:15:27.000000 plotagain-1.0.5/src/plotagain.egg-info/dependency_links.txt
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)       17 2023-07-23 14:15:27.000000 plotagain-1.0.5/src/plotagain.egg-info/requires.txt
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)       10 2023-07-23 14:15:27.000000 plotagain-1.0.5/src/plotagain.egg-info/top_level.txt
+drwxr-xr-x   0 jeremywilkinson   (501) staff       (20)        0 2023-07-23 14:15:27.276642 plotagain-1.0.5/tests/
+-rw-r--r--   0 jeremywilkinson   (501) staff       (20)       30 2023-07-20 18:12:48.000000 plotagain-1.0.5/tests/test_nothing.py
```

### Comparing `plotagain-1.0.4/PKG-INFO` & `plotagain-1.0.5/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: plotagain
-Version: 1.0.4
+Version: 1.0.5
 Summary: A helper tool for matplotlib. Provides a contextmanager which automatically saves data used to make plots and automatically generates a script to re-load and re-plot this data at a later stage.
 Author-email: Jeremy John Henry Wilkinson <jero.wilkinson@gmail.com>
 License: BSD-3-Clause
 Project-URL: Homepage, https://bitbucket.org/jjhw3/plotagain/
 Keywords: save data,matplotlib,plt
 Classifier: Framework :: Matplotlib
 Classifier: Programming Language :: Python :: 3
@@ -46,15 +46,14 @@
 It is suggested that plots are kept simple in the scope of the code which generates them.
 Once the individual plots have been generated it is easy to move around data and edit the autogenerated scripts to merge the individual plots using subplots.
 
 ## Example Usage
 
 ```python
 import numpy as np
-import matplotlib.pyplot as plt
 from plotagain import SavePlotContext
 
 
 x_data = np.linspace(0, 2 * np.pi, 1000)
 y_data = np.sin(x_data)
 with SavePlotContext("./data-save-dir", locals(), overwrite=True) as spc:
     spc.plot(x_data, y_data, c='k', label='sin')
```

### Comparing `plotagain-1.0.4/README.md` & `plotagain-1.0.5/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -33,15 +33,14 @@
 It is suggested that plots are kept simple in the scope of the code which generates them.
 Once the individual plots have been generated it is easy to move around data and edit the autogenerated scripts to merge the individual plots using subplots.
 
 ## Example Usage
 
 ```python
 import numpy as np
-import matplotlib.pyplot as plt
 from plotagain import SavePlotContext
 
 
 x_data = np.linspace(0, 2 * np.pi, 1000)
 y_data = np.sin(x_data)
 with SavePlotContext("./data-save-dir", locals(), overwrite=True) as spc:
     spc.plot(x_data, y_data, c='k', label='sin')
```

### Comparing `plotagain-1.0.4/bitbucket-pipelines.yml` & `plotagain-1.0.5/bitbucket-pipelines.yml`

 * *Files identical despite different names*

### Comparing `plotagain-1.0.4/pyproject.toml` & `plotagain-1.0.5/pyproject.toml`

 * *Files identical despite different names*

### Comparing `plotagain-1.0.4/src/plotagain/iddict.py` & `plotagain-1.0.5/src/plotagain/iddict.py`

 * *Files identical despite different names*

### Comparing `plotagain-1.0.4/src/plotagain/pyplotcall.py` & `plotagain-1.0.5/src/plotagain/pyplotcall.py`

 * *Files identical despite different names*

### Comparing `plotagain-1.0.4/src/plotagain/saveplotcontext.py` & `plotagain-1.0.5/src/plotagain/saveplotcontext.py`

 * *Files 5% similar despite different names*

```diff
@@ -7,14 +7,15 @@
 
 from plotagain.iddict import IDDict
 from plotagain.pyplotcall import PyplotCall
 from plotagain.utils import write_pickle
 
 here = Path(__file__).parent
 pickle_load_template = "{var_name} = load_pickle('{var_name}.pkl')"
+skip_all_show_plots = False
 
 
 class SavePlotContext:
     """
     Context manager which wraps matplotlib.pyplot. Usage:
 
     with SavePlotContext("/.../save-dir/", locals(), ...) as pla:
@@ -52,26 +53,28 @@
         A list of PyplotCall objects, one for each call made to matplotlib.pyplot. E.g. 'plot', 'show', 'hist'
     """
     save_dir: Path
     outer_locals_dict: Dict[str, Any]
     outer_globals_dict: Dict[str, Any]
     overwrite: bool
     regenerate_script_name: str
+    skip_show_plots: bool
 
     used_variables: Dict[str, Any]
     calls: List[PyplotCall]
 
     def __init__(
         self,
         save_dir: Union[Path, str],
         locals_dict: Dict[str, Any],
         overwrite: bool = False,
         globals_dict: Optional[Dict[str, Any]] = None,
         script_name: str = 'make_plot.py',
         script_template: Optional[Union[Path, str]] = None,
+        skip_show_plots: bool = False,
     ):
         """
 
         Parameters
         ----------
         save_dir
             The path to a directory into which the argument pickles and autogenerated script are saved. If the directory
@@ -84,21 +87,30 @@
         overwrite
             If False, the directory self.save_dir must be empty, otherwise an exception is raised
         script_name
             The name of the autogenerated script
         script_template
             A path to the template used to autogenerate the script which recreates the plots created using this
             SavePlotContext. See script_template.txt for an example
+        skip_show_plots
+            If set to True, calls for plt.show are NOT passed on to matplotlib.pyplot but are still stored for the
+            reconstruction script. Instead of plt.show, plt.close is called instead. Allows for execution without
+            pausing for plots. As an example, code developed locally is likely to involve lots of plots to check the
+            output at various stages. Code executed remotely is likely to be unsupervised and therefore the plots ought
+            not to render. Setting skip_show_plots to True allows for the disabling of manual checks while the plots
+            that would be displayed are still saved and accessible later if required. See set_skip_all_show_plots() for
+            a global flag of this nature
         """
         self.save_dir = Path(save_dir)
         self.outer_locals_dict = locals_dict
         self.outer_globals_dict = globals_dict or {}
         self.overwrite = overwrite
         self.regenerate_script_name = script_name
         self.script_template_path = Path(script_template or (here / 'script_template.txt')).absolute()
+        self.skip_show_plots = skip_show_plots
 
         self.used_variables = {}
         self.calls = []
 
         if not self.save_dir.exists():
             self.save_dir.mkdir()
         if not self.overwrite and len(list(self.save_dir.glob('*'))) > 0:
@@ -128,23 +140,27 @@
 
         @wraps(plt_fn)
         def wrapper(*args, **kwargs):
             """
             Wrapper function which simply calls the intended matplotlib.pyplot function, stores the arguments, and
             returns the result
             """
-            ret = plt_fn(*args, **kwargs)
             self.calls.append(PyplotCall(
                 fn_name,
                 args,
                 kwargs
             ))
             calling_scope = IDDict(self.outer_locals_dict)
             calling_scope.update(self.outer_globals_dict)
             self.calls[-1].find_or_name_args(calling_scope, self.used_variables)
+
+            if fn_name == 'show' and (self.skip_show_plots or skip_all_show_plots):
+                return plt.close()
+
+            ret = plt_fn(*args, **kwargs)
             return ret
 
         return wrapper
 
     def save_used_variables(self) -> None:
         """
         Saves a pickle file for each object passed in as an argument to a matplotlib.pyplot call
```

### Comparing `plotagain-1.0.4/src/plotagain/utils.py` & `plotagain-1.0.5/src/plotagain/utils.py`

 * *Files identical despite different names*

### Comparing `plotagain-1.0.4/src/plotagain.egg-info/PKG-INFO` & `plotagain-1.0.5/src/plotagain.egg-info/PKG-INFO`

 * *Files 7% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: plotagain
-Version: 1.0.4
+Version: 1.0.5
 Summary: A helper tool for matplotlib. Provides a contextmanager which automatically saves data used to make plots and automatically generates a script to re-load and re-plot this data at a later stage.
 Author-email: Jeremy John Henry Wilkinson <jero.wilkinson@gmail.com>
 License: BSD-3-Clause
 Project-URL: Homepage, https://bitbucket.org/jjhw3/plotagain/
 Keywords: save data,matplotlib,plt
 Classifier: Framework :: Matplotlib
 Classifier: Programming Language :: Python :: 3
@@ -46,15 +46,14 @@
 It is suggested that plots are kept simple in the scope of the code which generates them.
 Once the individual plots have been generated it is easy to move around data and edit the autogenerated scripts to merge the individual plots using subplots.
 
 ## Example Usage
 
 ```python
 import numpy as np
-import matplotlib.pyplot as plt
 from plotagain import SavePlotContext
 
 
 x_data = np.linspace(0, 2 * np.pi, 1000)
 y_data = np.sin(x_data)
 with SavePlotContext("./data-save-dir", locals(), overwrite=True) as spc:
     spc.plot(x_data, y_data, c='k', label='sin')
```

