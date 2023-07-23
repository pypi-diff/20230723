# Comparing `tmp/xso-0.0.4.tar.gz` & `tmp/xso-0.1.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "xso-0.0.4.tar", max compression
+gzip compressed data, was "xso-0.1.0.tar", max compression
```

## Comparing `xso-0.0.4.tar` & `xso-0.1.0.tar`

### file list

```diff
@@ -1,12 +1,12 @@
--rwxr-xr-x   0        0        0     1514 2023-07-23 20:40:48.959558 xso-0.0.4/LICENSE
--rw-r--r--   0        0        0     3290 2023-07-23 20:40:48.959558 xso-0.0.4/README.md
--rw-r--r--   0        0        0      783 2023-07-23 20:40:48.963558 xso-0.0.4/pyproject.toml
--rw-r--r--   0        0        0      142 2023-07-23 20:40:48.963558 xso-0.0.4/src/xso/__init__.py
--rw-r--r--   0        0        0     7700 2023-07-23 20:40:48.963558 xso-0.0.4/src/xso/backendcomps.py
--rw-r--r--   0        0        0    23117 2023-07-23 20:40:48.963558 xso-0.0.4/src/xso/component.py
--rw-r--r--   0        0        0     5297 2023-07-23 20:40:48.963558 xso-0.0.4/src/xso/core.py
--rw-r--r--   0        0        0     7215 2023-07-23 20:40:48.963558 xso-0.0.4/src/xso/model.py
--rw-r--r--   0        0        0    14522 2023-07-23 20:40:48.963558 xso-0.0.4/src/xso/solvers.py
--rw-r--r--   0        0        0     9027 2023-07-23 20:40:48.963558 xso-0.0.4/src/xso/variables.py
--rw-r--r--   0        0        0     7062 2023-07-23 20:40:48.963558 xso-0.0.4/src/xso/xsimlabwrappers.py
--rw-r--r--   0        0        0     4070 1970-01-01 00:00:00.000000 xso-0.0.4/PKG-INFO
+-rwxr-xr-x   0        0        0     1514 2023-07-23 21:06:38.373978 xso-0.1.0/LICENSE
+-rw-r--r--   0        0        0     3334 2023-07-23 21:06:38.373978 xso-0.1.0/README.md
+-rw-r--r--   0        0        0      783 2023-07-23 21:06:38.377978 xso-0.1.0/pyproject.toml
+-rw-r--r--   0        0        0      142 2023-07-23 21:06:38.377978 xso-0.1.0/src/xso/__init__.py
+-rw-r--r--   0        0        0     7700 2023-07-23 21:06:38.377978 xso-0.1.0/src/xso/backendcomps.py
+-rw-r--r--   0        0        0    23117 2023-07-23 21:06:38.377978 xso-0.1.0/src/xso/component.py
+-rw-r--r--   0        0        0     5297 2023-07-23 21:06:38.377978 xso-0.1.0/src/xso/core.py
+-rw-r--r--   0        0        0     7215 2023-07-23 21:06:38.377978 xso-0.1.0/src/xso/model.py
+-rw-r--r--   0        0        0    14522 2023-07-23 21:06:38.377978 xso-0.1.0/src/xso/solvers.py
+-rw-r--r--   0        0        0     9027 2023-07-23 21:06:38.377978 xso-0.1.0/src/xso/variables.py
+-rw-r--r--   0        0        0     7062 2023-07-23 21:06:38.377978 xso-0.1.0/src/xso/xsimlabwrappers.py
+-rw-r--r--   0        0        0     4114 1970-01-01 00:00:00.000000 xso-0.1.0/PKG-INFO
```

### Comparing `xso-0.0.4/LICENSE` & `xso-0.1.0/LICENSE`

 * *Files identical despite different names*

### Comparing `xso-0.0.4/README.md` & `xso-0.1.0/README.md`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,11 @@
 # xarray-simlab-ode
 
-[![Documentation Status](https://readthedocs.org/projects/xarray-simlab-ode/badge/?version=latest)](https://xarray-simlab-ode.readthedocs.io/en/latest/?badge=latest)
+![PyPI](https://img.shields.io/pypi/v/xso) [![Documentation Status](https://readthedocs.org/projects/xarray-simlab-ode/badge/?version=latest)](https://xarray-simlab-ode.readthedocs.io/en/latest/?badge=latest)
+
 
 The `xso` framework for building and solving models based on ordinary differential equations (ODEs), an extension of [xarray-simlab](https://github.com/xarray-contrib/xarray-simlab).
 
 Xarray-simlab provides a generic framework for building computational models in a modular fashion and an [xarray](http://xarray.pydata.org/) extension for setting and running simulations using xarray's `Dataset` structure.
 
 Xarray-simlab-ode (XSO) extends the framework with a set of variables, processes and a solver backend, suited towards ODE-based models. It is designed for flexible, interactive and reproducible modeling workflows.
```

### Comparing `xso-0.0.4/pyproject.toml` & `xso-0.1.0/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "xso"
-version = "0.0.4"
+version = "0.1.0"
 description = "Framework for building and solving ODE-based models, an extension of xarray-simlab"
 authors = ["Benjamin Post"]
 license = "BSD 3-Clause"
 readme = "README.md"
 
 [tool.poetry.dependencies]
 python = ">=3.8,<4.0"
```

### Comparing `xso-0.0.4/src/xso/backendcomps.py` & `xso-0.1.0/src/xso/backendcomps.py`

 * *Files identical despite different names*

### Comparing `xso-0.0.4/src/xso/component.py` & `xso-0.1.0/src/xso/component.py`

 * *Files identical despite different names*

### Comparing `xso-0.0.4/src/xso/core.py` & `xso-0.1.0/src/xso/core.py`

 * *Files identical despite different names*

### Comparing `xso-0.0.4/src/xso/model.py` & `xso-0.1.0/src/xso/model.py`

 * *Files identical despite different names*

### Comparing `xso-0.0.4/src/xso/solvers.py` & `xso-0.1.0/src/xso/solvers.py`

 * *Files identical despite different names*

### Comparing `xso-0.0.4/src/xso/variables.py` & `xso-0.1.0/src/xso/variables.py`

 * *Files identical despite different names*

### Comparing `xso-0.0.4/src/xso/xsimlabwrappers.py` & `xso-0.1.0/src/xso/xsimlabwrappers.py`

 * *Files identical despite different names*

### Comparing `xso-0.0.4/PKG-INFO` & `xso-0.1.0/PKG-INFO`

 * *Files 3% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: xso
-Version: 0.0.4
+Version: 0.1.0
 Summary: Framework for building and solving ODE-based models, an extension of xarray-simlab
 License: BSD 3-Clause
 Author: Benjamin Post
 Requires-Python: >=3.8,<4.0
 Classifier: License :: Other/Proprietary License
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
@@ -18,15 +18,16 @@
 Requires-Dist: xarray (>=0.10.0)
 Requires-Dist: xarray-simlab (>=0.5.0,<0.6.0)
 Requires-Dist: zarr (>=2.3.0)
 Description-Content-Type: text/markdown
 
 # xarray-simlab-ode
 
-[![Documentation Status](https://readthedocs.org/projects/xarray-simlab-ode/badge/?version=latest)](https://xarray-simlab-ode.readthedocs.io/en/latest/?badge=latest)
+![PyPI](https://img.shields.io/pypi/v/xso) [![Documentation Status](https://readthedocs.org/projects/xarray-simlab-ode/badge/?version=latest)](https://xarray-simlab-ode.readthedocs.io/en/latest/?badge=latest)
+
 
 The `xso` framework for building and solving models based on ordinary differential equations (ODEs), an extension of [xarray-simlab](https://github.com/xarray-contrib/xarray-simlab).
 
 Xarray-simlab provides a generic framework for building computational models in a modular fashion and an [xarray](http://xarray.pydata.org/) extension for setting and running simulations using xarray's `Dataset` structure.
 
 Xarray-simlab-ode (XSO) extends the framework with a set of variables, processes and a solver backend, suited towards ODE-based models. It is designed for flexible, interactive and reproducible modeling workflows.
```

