# Comparing `tmp/bs_python_utils-0.4.tar.gz` & `tmp/bs_python_utils-0.4.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "bs_python_utils-0.4.tar", max compression
+gzip compressed data, was "bs_python_utils-0.4.1.tar", max compression
```

## Comparing `bs_python_utils-0.4.tar` & `bs_python_utils-0.4.1.tar`

### file list

```diff
@@ -1,30 +1,30 @@
--rw-r--r--   0        0        0     1073 2023-04-21 14:06:07.415664 bs_python_utils-0.4/LICENSE
--rw-r--r--   0        0        0     1791 2023-07-22 22:29:18.034303 bs_python_utils-0.4/README.md
--rw-r--r--   0        0        0     1799 2023-07-21 20:34:46.059698 bs_python_utils-0.4/bs_python_utils/Timer.py
--rw-r--r--   0        0        0        0 2023-04-24 19:42:58.429294 bs_python_utils-0.4/bs_python_utils/__init__.py
--rw-r--r--   0        0        0     8986 2023-07-22 22:24:53.426171 bs_python_utils-0.4/bs_python_utils/bivariate_quantiles.py
--rw-r--r--   0        0        0    28473 2023-04-24 22:57:44.859499 bs_python_utils-0.4/bs_python_utils/bs_altair.py
--rw-r--r--   0        0        0     2976 2023-04-24 20:25:24.489951 bs_python_utils-0.4/bs_python_utils/bs_logging.py
--rw-r--r--   0        0        0     3577 2023-04-24 19:42:58.433666 bs_python_utils-0.4/bs_python_utils/bs_mathstr.py
--rw-r--r--   0        0        0     4338 2023-04-24 21:45:53.142922 bs_python_utils-0.4/bs_python_utils/bs_mem.py
--rw-r--r--   0        0        0    15009 2023-07-21 21:46:32.207754 bs_python_utils-0.4/bs_python_utils/bs_opt.py
--rw-r--r--   0        0        0       36 2023-04-24 19:42:58.438686 bs_python_utils-0.4/bs_python_utils/bs_plots.py
--rw-r--r--   0        0        0     4507 2023-04-24 20:32:13.556809 bs_python_utils-0.4/bs_python_utils/bs_seaborn.py
--rw-r--r--   0        0        0     1391 2023-04-24 22:48:26.302214 bs_python_utils-0.4/bs_python_utils/bs_sparse_gaussian.py
--rw-r--r--   0        0        0      905 2023-04-24 19:42:58.441367 bs_python_utils-0.4/bs_python_utils/bsmplutils.py
--rw-r--r--   0        0        0    33587 2023-07-22 22:16:47.975748 bs_python_utils-0.4/bs_python_utils/bsnputils.py
--rw-r--r--   0        0        0     2132 2023-04-24 20:25:24.253141 bs_python_utils-0.4/bs_python_utils/bssputils.py
--rw-r--r--   0        0        0    15438 2023-07-21 21:58:00.037774 bs_python_utils-0.4/bs_python_utils/bsstats.py
--rw-r--r--   0        0        0     9471 2023-05-08 18:43:13.753098 bs_python_utils-0.4/bs_python_utils/bsutils.py
--rw-r--r--   0        0        0    14016 2023-06-20 20:58:35.000000 bs_python_utils-0.4/bs_python_utils/chebyshev.py
--rw-r--r--   0        0        0     7801 2023-04-24 21:45:53.165270 bs_python_utils-0.4/bs_python_utils/distance_covariances.py
--rw-r--r--   0        0        0     1350 2023-04-24 22:36:28.733299 bs_python_utils-0.4/bs_python_utils/example_opt.py
--rw-r--r--   0        0        0     3833 2023-04-24 22:48:26.344134 bs_python_utils-0.4/bs_python_utils/examples_altair.py
--rw-r--r--   0        0        0     1013 2023-04-24 22:36:28.733372 bs_python_utils-0.4/bs_python_utils/examples_distance_covariances.py
--rw-r--r--   0        0        0      552 2023-04-24 22:36:28.733335 bs_python_utils-0.4/bs_python_utils/examples_mem.py
--rw-r--r--   0        0        0      771 2023-04-24 21:45:53.146924 bs_python_utils-0.4/bs_python_utils/examples_seaborn.py
--rw-r--r--   0        0        0      786 2023-04-24 22:36:28.733292 bs_python_utils-0.4/bs_python_utils/examples_sklearn.py
--rw-r--r--   0        0        0     7426 2023-04-24 20:25:24.576148 bs_python_utils-0.4/bs_python_utils/pandas_utils.py
--rw-r--r--   0        0        0     1872 2023-04-24 21:46:50.361114 bs_python_utils-0.4/bs_python_utils/sklearn_utils.py
--rw-r--r--   0        0        0     1869 2023-07-22 22:28:12.726598 bs_python_utils-0.4/pyproject.toml
--rw-r--r--   0        0        0     2760 1970-01-01 00:00:00.000000 bs_python_utils-0.4/PKG-INFO
+-rw-r--r--   0        0        0     1073 2023-04-21 14:06:07.415664 bs_python_utils-0.4.1/LICENSE
+-rw-r--r--   0        0        0     1864 2023-07-23 13:08:22.221938 bs_python_utils-0.4.1/README.md
+-rw-r--r--   0        0        0     1799 2023-07-21 20:34:46.059698 bs_python_utils-0.4.1/bs_python_utils/Timer.py
+-rw-r--r--   0        0        0        0 2023-04-24 19:42:58.429294 bs_python_utils-0.4.1/bs_python_utils/__init__.py
+-rw-r--r--   0        0        0     9089 2023-07-23 13:06:12.931194 bs_python_utils-0.4.1/bs_python_utils/bivariate_quantiles.py
+-rw-r--r--   0        0        0    28473 2023-04-24 22:57:44.859499 bs_python_utils-0.4.1/bs_python_utils/bs_altair.py
+-rw-r--r--   0        0        0     2976 2023-04-24 20:25:24.489951 bs_python_utils-0.4.1/bs_python_utils/bs_logging.py
+-rw-r--r--   0        0        0     3577 2023-04-24 19:42:58.433666 bs_python_utils-0.4.1/bs_python_utils/bs_mathstr.py
+-rw-r--r--   0        0        0     4338 2023-04-24 21:45:53.142922 bs_python_utils-0.4.1/bs_python_utils/bs_mem.py
+-rw-r--r--   0        0        0    15009 2023-07-21 21:46:32.207754 bs_python_utils-0.4.1/bs_python_utils/bs_opt.py
+-rw-r--r--   0        0        0       36 2023-04-24 19:42:58.438686 bs_python_utils-0.4.1/bs_python_utils/bs_plots.py
+-rw-r--r--   0        0        0     4507 2023-04-24 20:32:13.556809 bs_python_utils-0.4.1/bs_python_utils/bs_seaborn.py
+-rw-r--r--   0        0        0     1391 2023-04-24 22:48:26.302214 bs_python_utils-0.4.1/bs_python_utils/bs_sparse_gaussian.py
+-rw-r--r--   0        0        0      905 2023-04-24 19:42:58.441367 bs_python_utils-0.4.1/bs_python_utils/bsmplutils.py
+-rw-r--r--   0        0        0    33587 2023-07-22 22:16:47.975748 bs_python_utils-0.4.1/bs_python_utils/bsnputils.py
+-rw-r--r--   0        0        0     2132 2023-04-24 20:25:24.253141 bs_python_utils-0.4.1/bs_python_utils/bssputils.py
+-rw-r--r--   0        0        0    15438 2023-07-21 21:58:00.037774 bs_python_utils-0.4.1/bs_python_utils/bsstats.py
+-rw-r--r--   0        0        0     9471 2023-05-08 18:43:13.753098 bs_python_utils-0.4.1/bs_python_utils/bsutils.py
+-rw-r--r--   0        0        0    14016 2023-06-20 20:58:35.000000 bs_python_utils-0.4.1/bs_python_utils/chebyshev.py
+-rw-r--r--   0        0        0     7801 2023-04-24 21:45:53.165270 bs_python_utils-0.4.1/bs_python_utils/distance_covariances.py
+-rw-r--r--   0        0        0     1350 2023-04-24 22:36:28.733299 bs_python_utils-0.4.1/bs_python_utils/example_opt.py
+-rw-r--r--   0        0        0     3833 2023-04-24 22:48:26.344134 bs_python_utils-0.4.1/bs_python_utils/examples_altair.py
+-rw-r--r--   0        0        0     1013 2023-04-24 22:36:28.733372 bs_python_utils-0.4.1/bs_python_utils/examples_distance_covariances.py
+-rw-r--r--   0        0        0      552 2023-04-24 22:36:28.733335 bs_python_utils-0.4.1/bs_python_utils/examples_mem.py
+-rw-r--r--   0        0        0      771 2023-04-24 21:45:53.146924 bs_python_utils-0.4.1/bs_python_utils/examples_seaborn.py
+-rw-r--r--   0        0        0      786 2023-04-24 22:36:28.733292 bs_python_utils-0.4.1/bs_python_utils/examples_sklearn.py
+-rw-r--r--   0        0        0     7426 2023-04-24 20:25:24.576148 bs_python_utils-0.4.1/bs_python_utils/pandas_utils.py
+-rw-r--r--   0        0        0     1872 2023-04-24 21:46:50.361114 bs_python_utils-0.4.1/bs_python_utils/sklearn_utils.py
+-rw-r--r--   0        0        0     1890 2023-07-23 13:07:41.282800 bs_python_utils-0.4.1/pyproject.toml
+-rw-r--r--   0        0        0     2876 1970-01-01 00:00:00.000000 bs_python_utils-0.4.1/PKG-INFO
```

### Comparing `bs_python_utils-0.4/LICENSE` & `bs_python_utils-0.4.1/LICENSE`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.4/README.md` & `bs_python_utils-0.4.1/README.md`

 * *Files 3% similar despite different names*

```diff
@@ -9,14 +9,16 @@
 My Python utilities.
 
 -   **Github repository**: <https://github.com/bsalanie/bs-python-utils/>
 -   **Documentation** <https://bsalanie.github.io/bs-python-utils/>
 
 ### Release notes
 
+#### 0.4.1 (July 23, 2023)
+Only print if verbose in bivariate quantiles.
 #### 0.4 (July 22, 2023)
 Added bivariate quantiles and ranks à la optimal transportation.
 #### 0.3 (July 21, 2023)
 Added in Numpy utils a function to set upper and lower triangle to a scalar;
 and `minimize_free` in `bs_opt`.
 
 #### 0.2 (July 17, 2023)
```

### Comparing `bs_python_utils-0.4/bs_python_utils/Timer.py` & `bs_python_utils-0.4.1/bs_python_utils/Timer.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.4/bs_python_utils/bivariate_quantiles.py` & `bs_python_utils-0.4.1/bs_python_utils/bivariate_quantiles.py`

 * *Files 2% similar despite different names*

```diff
@@ -118,14 +118,15 @@
     y: np.ndarray, v: np.ndarray, n_nodes: int = 32, presorted: bool = False
 ) -> np.ndarray:
     """computes the vector ranks of `y`, given the converged `v`
 
     Args:
         y: the observations, an `(n,2)` matrix
         v: the converged values of the weights, an `n`-vector
+        n_nodes: the number of nodes for Chebyshev integration
         presorted: if `True`, then `y` and `v` are sorted by increasing `y[:, 1]`.
 
     Returns:
         an `(n,2)` matrix with the average ranks of `y`
     """
     n, d = y.shape
 
@@ -230,20 +231,22 @@
 
     interval01 = Interval(0.0, 1.0)
     u1_nodes, u1_weights = cheb_get_nodes_1d(interval01, n_nodes)
 
     argsog = [y_sorted, u1_nodes, u1_weights, verbose]
 
     res = minimize_free(obj_, grad_, v0, args=argsog)
-    print_optimization_results(res, "Minimizing over v")
+    if verbose:
+        print_optimization_results(res, "Minimizing over v")
 
     if not res.success:
         bs_error_abort("Problem! the optimization failed.")
     vstar = res.x
-    print(f"The final gradient is close to 0: error {npmaxabs(res.jac)}")
+    if verbose:
+        print(f"The final gradient over v is close to 0: error {npmaxabs(res.jac)}")
     vstar1_sorted = np.append(vstar, -np.sum(vstar))
 
     # revert to original order
     vstar1 = np.zeros_like(vstar1_sorted)
     vstar1[sort_order] = vstar1_sorted
 
     return vstar1
@@ -252,15 +255,15 @@
 def bivariate_quantiles(
     y: np.ndarray, u: np.ndarray, n_nodes: int = 32, verbose: bool = False
 ):
     """computes the bivariate quantiles of `y` at the quantiles `u`
 
     Args:
         y: the observations, an `(n, 2)` matrix
-        u_qtiles: the quantiles at which to compute the bivariate quantiles,
+        u: the quantiles at which to compute the bivariate quantiles,
             an `(m, 2)` matrix
         n_nodes: the number of nodes to use for the quadrature
         verbose: if `True`, print some information
 
     Returns:
         an `(m, 2)` matrix of bivariate quantiles
     """
```

### Comparing `bs_python_utils-0.4/bs_python_utils/bs_altair.py` & `bs_python_utils-0.4.1/bs_python_utils/bs_altair.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.4/bs_python_utils/bs_logging.py` & `bs_python_utils-0.4.1/bs_python_utils/bs_logging.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.4/bs_python_utils/bs_mathstr.py` & `bs_python_utils-0.4.1/bs_python_utils/bs_mathstr.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.4/bs_python_utils/bs_mem.py` & `bs_python_utils-0.4.1/bs_python_utils/bs_mem.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.4/bs_python_utils/bs_opt.py` & `bs_python_utils-0.4.1/bs_python_utils/bs_opt.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.4/bs_python_utils/bs_seaborn.py` & `bs_python_utils-0.4.1/bs_python_utils/bs_seaborn.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.4/bs_python_utils/bs_sparse_gaussian.py` & `bs_python_utils-0.4.1/bs_python_utils/bs_sparse_gaussian.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.4/bs_python_utils/bsmplutils.py` & `bs_python_utils-0.4.1/bs_python_utils/bsmplutils.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.4/bs_python_utils/bsnputils.py` & `bs_python_utils-0.4.1/bs_python_utils/bsnputils.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.4/bs_python_utils/bssputils.py` & `bs_python_utils-0.4.1/bs_python_utils/bssputils.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.4/bs_python_utils/bsstats.py` & `bs_python_utils-0.4.1/bs_python_utils/bsstats.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.4/bs_python_utils/bsutils.py` & `bs_python_utils-0.4.1/bs_python_utils/bsutils.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.4/bs_python_utils/chebyshev.py` & `bs_python_utils-0.4.1/bs_python_utils/chebyshev.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.4/bs_python_utils/distance_covariances.py` & `bs_python_utils-0.4.1/bs_python_utils/distance_covariances.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.4/bs_python_utils/example_opt.py` & `bs_python_utils-0.4.1/bs_python_utils/example_opt.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.4/bs_python_utils/examples_altair.py` & `bs_python_utils-0.4.1/bs_python_utils/examples_altair.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.4/bs_python_utils/examples_distance_covariances.py` & `bs_python_utils-0.4.1/bs_python_utils/examples_distance_covariances.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.4/bs_python_utils/examples_mem.py` & `bs_python_utils-0.4.1/bs_python_utils/examples_mem.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.4/bs_python_utils/examples_seaborn.py` & `bs_python_utils-0.4.1/bs_python_utils/examples_seaborn.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.4/bs_python_utils/examples_sklearn.py` & `bs_python_utils-0.4.1/bs_python_utils/examples_sklearn.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.4/bs_python_utils/pandas_utils.py` & `bs_python_utils-0.4.1/bs_python_utils/pandas_utils.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.4/bs_python_utils/sklearn_utils.py` & `bs_python_utils-0.4.1/bs_python_utils/sklearn_utils.py`

 * *Files identical despite different names*

### Comparing `bs_python_utils-0.4/pyproject.toml` & `bs_python_utils-0.4.1/pyproject.toml`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "bs_python_utils"
-version = "0.4"
+version = "0.4.1"
 description = "my Python utilities"
 authors = ["Bernard Salanie <bsalanie@columbia.edu>"]
 repository = "https://github.com/bsalanie/bs-python-utils"
 documentation = "https://bsalanie.github.io/bs-python-utils/"
 readme = "README.md"
 packages = [
   {include = "bs_python_utils"}
@@ -15,14 +15,15 @@
 altair = "^4.2.2"
 matplotlib = "^3.7.1"
 altair-saver = "^0.5.0"
 seaborn = "^0.12.2"
 scikit-learn = "^1.2.2"
 statsmodels = "^0.13.5"
 vega-datasets = "^0.9.0"
+griffe = "^0.32.3"
 
 [tool.poetry.group.dev.dependencies]
 pytest = "^7.2.0"
 mypy = "^0.981"
 pre-commit = "^2.20.0"
 
 [tool.poetry.group.docs.dependencies]
```

### Comparing `bs_python_utils-0.4/PKG-INFO` & `bs_python_utils-0.4.1/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,22 +1,23 @@
 Metadata-Version: 2.1
 Name: bs-python-utils
-Version: 0.4
+Version: 0.4.1
 Summary: my Python utilities
 Home-page: https://github.com/bsalanie/bs-python-utils
 Author: Bernard Salanie
 Author-email: bsalanie@columbia.edu
 Requires-Python: >=3.8,<4.0
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Requires-Dist: altair (>=4.2.2,<5.0.0)
 Requires-Dist: altair-saver (>=0.5.0,<0.6.0)
+Requires-Dist: griffe (>=0.32.3,<0.33.0)
 Requires-Dist: matplotlib (>=3.7.1,<4.0.0)
 Requires-Dist: scikit-learn (>=1.2.2,<2.0.0)
 Requires-Dist: seaborn (>=0.12.2,<0.13.0)
 Requires-Dist: statsmodels (>=0.13.5,<0.14.0)
 Requires-Dist: vega-datasets (>=0.9.0,<0.10.0)
 Project-URL: Documentation, https://bsalanie.github.io/bs-python-utils/
 Project-URL: Repository, https://github.com/bsalanie/bs-python-utils
@@ -33,14 +34,16 @@
 My Python utilities.
 
 -   **Github repository**: <https://github.com/bsalanie/bs-python-utils/>
 -   **Documentation** <https://bsalanie.github.io/bs-python-utils/>
 
 ### Release notes
 
+#### 0.4.1 (July 23, 2023)
+Only print if verbose in bivariate quantiles.
 #### 0.4 (July 22, 2023)
 Added bivariate quantiles and ranks à la optimal transportation.
 #### 0.3 (July 21, 2023)
 Added in Numpy utils a function to set upper and lower triangle to a scalar;
 and `minimize_free` in `bs_opt`.
 
 #### 0.2 (July 17, 2023)
```

