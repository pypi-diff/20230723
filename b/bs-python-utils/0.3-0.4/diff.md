# Comparing `tmp/bs_python_utils-0.3.tar.gz` & `tmp/bs_python_utils-0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "bs_python_utils-0.3.tar", max compression
+gzip compressed data, was "bs_python_utils-0.4.tar", max compression
```

## Comparing `bs_python_utils-0.3.tar` & `bs_python_utils-0.4.tar`

### file list

```diff
@@ -1,29 +1,30 @@
--rw-r--r--   0        0        0     1073 2023-04-21 14:06:07.415664 bs_python_utils-0.3/LICENSE
--rw-r--r--   0        0        0     1701 2023-07-21 22:13:37.495534 bs_python_utils-0.3/README.md
--rw-r--r--   0        0        0     1799 2023-07-21 20:34:46.059698 bs_python_utils-0.3/bs_python_utils/Timer.py
--rw-r--r--   0        0        0        0 2023-04-24 19:42:58.429294 bs_python_utils-0.3/bs_python_utils/__init__.py
--rw-r--r--   0        0        0    28473 2023-04-24 22:57:44.859499 bs_python_utils-0.3/bs_python_utils/bs_altair.py
--rw-r--r--   0        0        0     2976 2023-04-24 20:25:24.489951 bs_python_utils-0.3/bs_python_utils/bs_logging.py
--rw-r--r--   0        0        0     3577 2023-04-24 19:42:58.433666 bs_python_utils-0.3/bs_python_utils/bs_mathstr.py
--rw-r--r--   0        0        0     4338 2023-04-24 21:45:53.142922 bs_python_utils-0.3/bs_python_utils/bs_mem.py
--rw-r--r--   0        0        0    15009 2023-07-21 21:46:32.207754 bs_python_utils-0.3/bs_python_utils/bs_opt.py
--rw-r--r--   0        0        0       36 2023-04-24 19:42:58.438686 bs_python_utils-0.3/bs_python_utils/bs_plots.py
--rw-r--r--   0        0        0     4507 2023-04-24 20:32:13.556809 bs_python_utils-0.3/bs_python_utils/bs_seaborn.py
--rw-r--r--   0        0        0     1391 2023-04-24 22:48:26.302214 bs_python_utils-0.3/bs_python_utils/bs_sparse_gaussian.py
--rw-r--r--   0        0        0      905 2023-04-24 19:42:58.441367 bs_python_utils-0.3/bs_python_utils/bsmplutils.py
--rw-r--r--   0        0        0    33601 2023-07-21 21:46:32.440282 bs_python_utils-0.3/bs_python_utils/bsnputils.py
--rw-r--r--   0        0        0     2132 2023-04-24 20:25:24.253141 bs_python_utils-0.3/bs_python_utils/bssputils.py
--rw-r--r--   0        0        0    15438 2023-07-21 21:58:00.037774 bs_python_utils-0.3/bs_python_utils/bsstats.py
--rw-r--r--   0        0        0     9471 2023-05-08 18:43:13.753098 bs_python_utils-0.3/bs_python_utils/bsutils.py
--rw-r--r--   0        0        0    14016 2023-06-20 20:58:35.000000 bs_python_utils-0.3/bs_python_utils/chebyshev.py
--rw-r--r--   0        0        0     7801 2023-04-24 21:45:53.165270 bs_python_utils-0.3/bs_python_utils/distance_covariances.py
--rw-r--r--   0        0        0     1350 2023-04-24 22:36:28.733299 bs_python_utils-0.3/bs_python_utils/example_opt.py
--rw-r--r--   0        0        0     3833 2023-04-24 22:48:26.344134 bs_python_utils-0.3/bs_python_utils/examples_altair.py
--rw-r--r--   0        0        0     1013 2023-04-24 22:36:28.733372 bs_python_utils-0.3/bs_python_utils/examples_distance_covariances.py
--rw-r--r--   0        0        0      552 2023-04-24 22:36:28.733335 bs_python_utils-0.3/bs_python_utils/examples_mem.py
--rw-r--r--   0        0        0      771 2023-04-24 21:45:53.146924 bs_python_utils-0.3/bs_python_utils/examples_seaborn.py
--rw-r--r--   0        0        0      786 2023-04-24 22:36:28.733292 bs_python_utils-0.3/bs_python_utils/examples_sklearn.py
--rw-r--r--   0        0        0     7426 2023-04-24 20:25:24.576148 bs_python_utils-0.3/bs_python_utils/pandas_utils.py
--rw-r--r--   0        0        0     1872 2023-04-24 21:46:50.361114 bs_python_utils-0.3/bs_python_utils/sklearn_utils.py
--rw-r--r--   0        0        0     1868 2023-07-21 22:13:53.203848 bs_python_utils-0.3/pyproject.toml
--rw-r--r--   0        0        0     2670 1970-01-01 00:00:00.000000 bs_python_utils-0.3/PKG-INFO
+-rw-r--r--   0        0        0     1073 2023-04-21 14:06:07.415664 bs_python_utils-0.4/LICENSE
+-rw-r--r--   0        0        0     1791 2023-07-22 22:29:18.034303 bs_python_utils-0.4/README.md
+-rw-r--r--   0        0        0     1799 2023-07-21 20:34:46.059698 bs_python_utils-0.4/bs_python_utils/Timer.py
+-rw-r--r--   0        0        0        0 2023-04-24 19:42:58.429294 bs_python_utils-0.4/bs_python_utils/__init__.py
+-rw-r--r--   0        0        0     8986 2023-07-22 22:24:53.426171 bs_python_utils-0.4/bs_python_utils/bivariate_quantiles.py
+-rw-r--r--   0        0        0    28473 2023-04-24 22:57:44.859499 bs_python_utils-0.4/bs_python_utils/bs_altair.py
+-rw-r--r--   0        0        0     2976 2023-04-24 20:25:24.489951 bs_python_utils-0.4/bs_python_utils/bs_logging.py
+-rw-r--r--   0        0        0     3577 2023-04-24 19:42:58.433666 bs_python_utils-0.4/bs_python_utils/bs_mathstr.py
+-rw-r--r--   0        0        0     4338 2023-04-24 21:45:53.142922 bs_python_utils-0.4/bs_python_utils/bs_mem.py
+-rw-r--r--   0        0        0    15009 2023-07-21 21:46:32.207754 bs_python_utils-0.4/bs_python_utils/bs_opt.py
+-rw-r--r--   0        0        0       36 2023-04-24 19:42:58.438686 bs_python_utils-0.4/bs_python_utils/bs_plots.py
+-rw-r--r--   0        0        0     4507 2023-04-24 20:32:13.556809 bs_python_utils-0.4/bs_python_utils/bs_seaborn.py
+-rw-r--r--   0        0        0     1391 2023-04-24 22:48:26.302214 bs_python_utils-0.4/bs_python_utils/bs_sparse_gaussian.py
+-rw-r--r--   0        0        0      905 2023-04-24 19:42:58.441367 bs_python_utils-0.4/bs_python_utils/bsmplutils.py
+-rw-r--r--   0        0        0    33587 2023-07-22 22:16:47.975748 bs_python_utils-0.4/bs_python_utils/bsnputils.py
+-rw-r--r--   0        0        0     2132 2023-04-24 20:25:24.253141 bs_python_utils-0.4/bs_python_utils/bssputils.py
+-rw-r--r--   0        0        0    15438 2023-07-21 21:58:00.037774 bs_python_utils-0.4/bs_python_utils/bsstats.py
+-rw-r--r--   0        0        0     9471 2023-05-08 18:43:13.753098 bs_python_utils-0.4/bs_python_utils/bsutils.py
+-rw-r--r--   0        0        0    14016 2023-06-20 20:58:35.000000 bs_python_utils-0.4/bs_python_utils/chebyshev.py
+-rw-r--r--   0        0        0     7801 2023-04-24 21:45:53.165270 bs_python_utils-0.4/bs_python_utils/distance_covariances.py
+-rw-r--r--   0        0        0     1350 2023-04-24 22:36:28.733299 bs_python_utils-0.4/bs_python_utils/example_opt.py
+-rw-r--r--   0        0        0     3833 2023-04-24 22:48:26.344134 bs_python_utils-0.4/bs_python_utils/examples_altair.py
+-rw-r--r--   0        0        0     1013 2023-04-24 22:36:28.733372 bs_python_utils-0.4/bs_python_utils/examples_distance_covariances.py
+-rw-r--r--   0        0        0      552 2023-04-24 22:36:28.733335 bs_python_utils-0.4/bs_python_utils/examples_mem.py
+-rw-r--r--   0        0        0      771 2023-04-24 21:45:53.146924 bs_python_utils-0.4/bs_python_utils/examples_seaborn.py
+-rw-r--r--   0        0        0      786 2023-04-24 22:36:28.733292 bs_python_utils-0.4/bs_python_utils/examples_sklearn.py
+-rw-r--r--   0        0        0     7426 2023-04-24 20:25:24.576148 bs_python_utils-0.4/bs_python_utils/pandas_utils.py
+-rw-r--r--   0        0        0     1872 2023-04-24 21:46:50.361114 bs_python_utils-0.4/bs_python_utils/sklearn_utils.py
+-rw-r--r--   0        0        0     1869 2023-07-22 22:28:12.726598 bs_python_utils-0.4/pyproject.toml
+-rw-r--r--   0        0        0     2760 1970-01-01 00:00:00.000000 bs_python_utils-0.4/PKG-INFO
```

### Comparing `bs_python_utils-0.3/LICENSE` & `bs_python_utils-0.4/LICENSE`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.3/README.md` & `bs_python_utils-0.4/README.md`

 * *Files 7% similar despite different names*

```diff
@@ -9,15 +9,16 @@
 My Python utilities.
 
 -   **Github repository**: <https://github.com/bsalanie/bs-python-utils/>
 -   **Documentation** <https://bsalanie.github.io/bs-python-utils/>
 
 ### Release notes
 
-
+#### 0.4 (July 22, 2023)
+Added bivariate quantiles and ranks à la optimal transportation.
 #### 0.3 (July 21, 2023)
 Added in Numpy utils a function to set upper and lower triangle to a scalar;
 and `minimize_free` in `bs_opt`.
 
 #### 0.2 (July 17, 2023)
 Fixed printing in accelerated gradient descent.
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

### Comparing `bs_python_utils-0.3/bs_python_utils/Timer.py` & `bs_python_utils-0.4/bs_python_utils/Timer.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.3/bs_python_utils/bs_altair.py` & `bs_python_utils-0.4/bs_python_utils/bs_altair.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.3/bs_python_utils/bs_logging.py` & `bs_python_utils-0.4/bs_python_utils/bs_logging.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.3/bs_python_utils/bs_mathstr.py` & `bs_python_utils-0.4/bs_python_utils/bs_mathstr.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.3/bs_python_utils/bs_mem.py` & `bs_python_utils-0.4/bs_python_utils/bs_mem.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.3/bs_python_utils/bs_opt.py` & `bs_python_utils-0.4/bs_python_utils/bs_opt.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.3/bs_python_utils/bs_seaborn.py` & `bs_python_utils-0.4/bs_python_utils/bs_seaborn.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.3/bs_python_utils/bs_sparse_gaussian.py` & `bs_python_utils-0.4/bs_python_utils/bs_sparse_gaussian.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.3/bs_python_utils/bsmplutils.py` & `bs_python_utils-0.4/bs_python_utils/bsmplutils.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.3/bs_python_utils/bsnputils.py` & `bs_python_utils-0.4/bs_python_utils/bsnputils.py`

 * *Files 0% similar despite different names*

```diff
@@ -218,16 +218,15 @@
         bs_error_abort(f"v should have 1 dimension, not {v.ndim}")
     nv = v.size
     sorted_v = np.zeros(nv + 2)
     sorted_v[1 : (nv + 1)] = np.sort(v)
     sorted_v[0] = 2.0 * sorted_v[1] - sorted_v[2]  # added to extend for q < 1/nv
     sorted_v[nv + 1] = sorted_v[nv]  # added to extend for q = 1
     if isinstance(q, float):
-        q = np.array([q])
-        q_floor = floor(nv * q)
+        q_floor = np.array([floor(nv * q)])
         val_q = sorted_v[q_floor] + (nv * q - q_floor) * (
             sorted_v[q_floor + 1] - sorted_v[q_floor]
         )
         return cast(float, val_q)
     elif isinstance(q, np.ndarray):
         q_floor = np.floor(nv * q).astype(int)
         vals_q = sorted_v[q_floor] + (nv * q - q_floor) * (
```

### Comparing `bs_python_utils-0.3/bs_python_utils/bssputils.py` & `bs_python_utils-0.4/bs_python_utils/bssputils.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.3/bs_python_utils/bsstats.py` & `bs_python_utils-0.4/bs_python_utils/bsstats.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.3/bs_python_utils/bsutils.py` & `bs_python_utils-0.4/bs_python_utils/bsutils.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.3/bs_python_utils/chebyshev.py` & `bs_python_utils-0.4/bs_python_utils/chebyshev.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.3/bs_python_utils/distance_covariances.py` & `bs_python_utils-0.4/bs_python_utils/distance_covariances.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.3/bs_python_utils/example_opt.py` & `bs_python_utils-0.4/bs_python_utils/example_opt.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.3/bs_python_utils/examples_altair.py` & `bs_python_utils-0.4/bs_python_utils/examples_altair.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.3/bs_python_utils/examples_distance_covariances.py` & `bs_python_utils-0.4/bs_python_utils/examples_distance_covariances.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.3/bs_python_utils/examples_mem.py` & `bs_python_utils-0.4/bs_python_utils/examples_mem.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.3/bs_python_utils/examples_seaborn.py` & `bs_python_utils-0.4/bs_python_utils/examples_seaborn.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.3/bs_python_utils/examples_sklearn.py` & `bs_python_utils-0.4/bs_python_utils/examples_sklearn.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.3/bs_python_utils/pandas_utils.py` & `bs_python_utils-0.4/bs_python_utils/pandas_utils.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.3/bs_python_utils/sklearn_utils.py` & `bs_python_utils-0.4/bs_python_utils/sklearn_utils.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.3/pyproject.toml` & `bs_python_utils-0.4/pyproject.toml`

 * *Files 5% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "bs_python_utils"
-version = "0.3"
+version = "0.4"
 description = "my Python utilities"
 authors = ["Bernard Salanie <bsalanie@columbia.edu>"]
 repository = "https://github.com/bsalanie/bs-python-utils"
 documentation = "https://bsalanie.github.io/bs-python-utils/"
 readme = "README.md"
 packages = [
   {include = "bs_python_utils"}
@@ -24,15 +24,16 @@
 pytest = "^7.2.0"
 mypy = "^0.981"
 pre-commit = "^2.20.0"
 
 [tool.poetry.group.docs.dependencies]
 mkdocs = "^1.4.2"
 mkdocs-material = "^8.5.10"
-mkdocstrings = {extras = ["python"], version = "^0.22.0"}
+mkdocstrings = {extras = ["python"], version = "^0.21.0"}
+
 
 [build-system]
 requires = ["poetry-core>=1.0.0"]
 build-backend = "poetry.core.masonry.api"
 
 [tool.black]
 line-length = 88
```

### Comparing `bs_python_utils-0.3/PKG-INFO` & `bs_python_utils-0.4/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: bs-python-utils
-Version: 0.3
+Version: 0.4
 Summary: my Python utilities
 Home-page: https://github.com/bsalanie/bs-python-utils
 Author: Bernard Salanie
 Author-email: bsalanie@columbia.edu
 Requires-Python: >=3.8,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
@@ -33,15 +33,16 @@
 My Python utilities.
 
 -   **Github repository**: <https://github.com/bsalanie/bs-python-utils/>
 -   **Documentation** <https://bsalanie.github.io/bs-python-utils/>
 
 ### Release notes
 
-
+#### 0.4 (July 22, 2023)
+Added bivariate quantiles and ranks à la optimal transportation.
 #### 0.3 (July 21, 2023)
 Added in Numpy utils a function to set upper and lower triangle to a scalar;
 and `minimize_free` in `bs_opt`.
 
 #### 0.2 (July 17, 2023)
 Fixed printing in accelerated gradient descent.
```

#### encoding

```diff
@@ -1 +1 @@
-us-ascii
+utf-8
```

