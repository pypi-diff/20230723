# Comparing `tmp/xso-0.0.3.tar.gz` & `tmp/xso-0.0.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "xso-0.0.3.tar", max compression
+gzip compressed data, was "xso-0.0.4.tar", max compression
```

## Comparing `xso-0.0.3.tar` & `xso-0.0.4.tar`

### file list

```diff
@@ -1,12 +1,12 @@
--rwxr-xr-x   0        0        0     1514 2023-03-03 22:41:01.663778 xso-0.0.3/LICENSE
--rw-r--r--   0        0        0     3290 2023-07-13 13:11:23.771983 xso-0.0.3/README.md
--rw-r--r--   0        0        0      693 2023-07-16 15:33:37.590527 xso-0.0.3/pyproject.toml
--rw-r--r--   0        0        0      168 2023-07-09 14:16:37.934652 xso-0.0.3/src/xso/__init__.py
--rw-r--r--   0        0        0     7702 2023-07-12 21:12:02.882760 xso-0.0.3/src/xso/backendcomps.py
--rw-r--r--   0        0        0    23120 2023-07-09 19:41:12.784520 xso-0.0.3/src/xso/component.py
--rw-r--r--   0        0        0     5297 2023-07-12 21:20:47.997816 xso-0.0.3/src/xso/core.py
--rw-r--r--   0        0        0     7215 2023-07-12 20:43:16.541879 xso-0.0.3/src/xso/model.py
--rw-r--r--   0        0        0    14371 2023-07-12 20:41:43.354334 xso-0.0.3/src/xso/solvers.py
--rw-r--r--   0        0        0     9027 2023-07-09 14:26:51.963518 xso-0.0.3/src/xso/variables.py
--rw-r--r--   0        0        0     6757 2023-07-12 21:12:02.875376 xso-0.0.3/src/xso/xsimlabwrappers.py
--rw-r--r--   0        0        0     4215 1970-01-01 00:00:00.000000 xso-0.0.3/PKG-INFO
+-rwxr-xr-x   0        0        0     1514 2023-07-23 20:40:48.959558 xso-0.0.4/LICENSE
+-rw-r--r--   0        0        0     3290 2023-07-23 20:40:48.959558 xso-0.0.4/README.md
+-rw-r--r--   0        0        0      783 2023-07-23 20:40:48.963558 xso-0.0.4/pyproject.toml
+-rw-r--r--   0        0        0      142 2023-07-23 20:40:48.963558 xso-0.0.4/src/xso/__init__.py
+-rw-r--r--   0        0        0     7700 2023-07-23 20:40:48.963558 xso-0.0.4/src/xso/backendcomps.py
+-rw-r--r--   0        0        0    23117 2023-07-23 20:40:48.963558 xso-0.0.4/src/xso/component.py
+-rw-r--r--   0        0        0     5297 2023-07-23 20:40:48.963558 xso-0.0.4/src/xso/core.py
+-rw-r--r--   0        0        0     7215 2023-07-23 20:40:48.963558 xso-0.0.4/src/xso/model.py
+-rw-r--r--   0        0        0    14522 2023-07-23 20:40:48.963558 xso-0.0.4/src/xso/solvers.py
+-rw-r--r--   0        0        0     9027 2023-07-23 20:40:48.963558 xso-0.0.4/src/xso/variables.py
+-rw-r--r--   0        0        0     7062 2023-07-23 20:40:48.963558 xso-0.0.4/src/xso/xsimlabwrappers.py
+-rw-r--r--   0        0        0     4070 1970-01-01 00:00:00.000000 xso-0.0.4/PKG-INFO
```

### Comparing `xso-0.0.3/LICENSE` & `xso-0.0.4/LICENSE`

 * *Files identical despite different names*

### Comparing `xso-0.0.3/README.md` & `xso-0.0.4/README.md`

 * *Files identical despite different names*

### Comparing `xso-0.0.3/src/xso/backendcomps.py` & `xso-0.0.4/src/xso/backendcomps.py`

 * *Files 0% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 import xsimlab as xs
-from xso.core import XSOCore
+from .core import XSOCore
 
 
 @xs.process
 class Backend:
     """Xarray-simlab process initializing and storing model backend and solver.
 
     This is the interface between the solver and model backend of XSO
@@ -194,15 +194,15 @@
         self.core.register_flux(self.label + '_' + self.time_flux.__name__, self.time_flux)
         self.core.add_flux(self.label, 'time', 'time_flux')
 
     def time_flux(self, **kwargs):
         """Simple linear flux, that represents time within model.
         Necessary for external solvers like odeint.
         """
-        dtdt = 1
+        dtdt = 1.
         return dtdt
 
 
 def create_time_component(time_unit):
     """Helper function to create a Time component with a custom unit registered through the backend."""
 
     @xs.process
```

### Comparing `xso-0.0.3/src/xso/component.py` & `xso-0.0.4/src/xso/component.py`

 * *Files 0% similar despite different names*

```diff
@@ -5,15 +5,15 @@
 
 from collections import OrderedDict, defaultdict, Counter
 from functools import wraps
 import inspect
 import numpy as np
 
 from .variables import XSOVarType
-from xso.backendcomps import FirstInit, SecondInit, ThirdInit, FourthInit, FifthInit
+from .backendcomps import FirstInit, SecondInit, ThirdInit, FourthInit, FifthInit
 
 
 def _create_variables_dict(process_cls):
     """Get all phydra variables declared in a component.
     Exclude attr.Attribute objects that are not XSO specific.
     """
     return OrderedDict(
```

### Comparing `xso-0.0.3/src/xso/core.py` & `xso-0.0.4/src/xso/core.py`

 * *Files identical despite different names*

### Comparing `xso-0.0.3/src/xso/model.py` & `xso-0.0.4/src/xso/model.py`

 * *Files identical despite different names*

### Comparing `xso-0.0.3/src/xso/solvers.py` & `xso-0.0.4/src/xso/solvers.py`

 * *Files 1% similar despite different names*

```diff
@@ -69,19 +69,22 @@
         if it requires specific math functions.
 
         Accessible within XSO components using self.m as defined in backendcomps.py class Backend.
          """
 
         # Constants:
         pi = np.pi  # pi constant
+        e = np.e  # e constant
 
         def exp(x):
             """Exponential function"""
             return np.exp(x)
 
+        # add np.errstate to ignore superfluous warnings, caused by solve_ivp solver
+        @np.errstate(all='ignore')
         def sqrt(x):
             """Square root function"""
             return np.sqrt(x)
 
         def log(x):
             """Logarithmic function """
             return np.log(x)
```

### Comparing `xso-0.0.3/src/xso/variables.py` & `xso-0.0.4/src/xso/variables.py`

 * *Files identical despite different names*

### Comparing `xso-0.0.3/src/xso/xsimlabwrappers.py` & `xso-0.0.4/src/xso/xsimlabwrappers.py`

 * *Files 5% similar despite different names*

```diff
@@ -6,30 +6,38 @@
 from xso.backendcomps import Backend, RunSolver, Time, create_time_component
 
 
 def create(components, time_unit='d'):
     """Creates xsimlab Model instance, from dict of XSO components,
     automatically adding the necessary model backend, solver and time components.
 
+    It is a simple wrapper of the xsimlab Model constructor, and returns a fully functional
+    Xarray-simlab model object with the XSO core, Solver and Time components added.
+
     Parameters
     ----------
     components : dict
         Dictionary with component names as keys and classes (decorated with
         :func:`component`) as values.
     time_unit : str, optional
         Unit of time to be used in the model. Default is 'd' for days. This has to be
         supplied at model creation, since the time unit is written to the immutable
         metadata of the model object.
+
+    Returns
+    -------
+    model : :class:`xsimlab.Model`
+        Xarray-simlab model object with the XSO core, Solver and Time components added.
     """
 
     components.update({'Core': Backend, 'Solver': RunSolver, 'Time': create_time_component(time_unit)})
     return xs.Model(components)
 
 
-def setup(solver, model, input_vars, output_vars=None, time=None, solver_kwargs=None):
+def setup(solver, model, input_vars, output_vars=None, time=None):
     """Create a specific setup for model runs.
 
     This function wraps xsimlab's create_setup and adds a dummy clock parameter
     necessary for model execution. This convenient function creates a new
     :class:`xarray.Dataset` object with everything needed to run a model
     (i.e., input values, time steps, output variables to save at given times)
     as data variables, coordinates and attributes.
```

### Comparing `xso-0.0.3/PKG-INFO` & `xso-0.0.4/PKG-INFO`

 * *Files 11% similar despite different names*

```diff
@@ -1,19 +1,16 @@
 Metadata-Version: 2.1
 Name: xso
-Version: 0.0.3
+Version: 0.0.4
 Summary: Framework for building and solving ODE-based models, an extension of xarray-simlab
 License: BSD 3-Clause
 Author: Benjamin Post
-Requires-Python: >=3.5
+Requires-Python: >=3.8,<4.0
 Classifier: License :: Other/Proprietary License
 Classifier: Programming Language :: Python :: 3
-Classifier: Programming Language :: Python :: 3.5
-Classifier: Programming Language :: Python :: 3.6
-Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Requires-Dist: dask[distributed] (>=2022.10.0)
 Requires-Dist: numpy
 Requires-Dist: scipy (>=1.9.1)
```

