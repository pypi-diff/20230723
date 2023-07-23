# Comparing `tmp/paramspace-2.6.0b2.tar.gz` & `tmp/paramspace-2.6.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "paramspace-2.6.0b2.tar", last modified: Mon Oct 24 08:08:31 2022, max compression
+gzip compressed data, was "paramspace-2.6.1.tar", last modified: Sun Jul 23 15:06:25 2023, max compression
```

## Comparing `paramspace-2.6.0b2.tar` & `paramspace-2.6.1.tar`

### file list

```diff
@@ -1,21 +1,22 @@
-drwxr-xr-x   0 root         (0) root         (0)        0 2022-10-24 08:08:31.977697 paramspace-2.6.0b2/
--rw-rw-rw-   0 root         (0) root         (0)     1330 2022-10-24 08:08:21.000000 paramspace-2.6.0b2/LICENSE
--rw-r--r--   0 root         (0) root         (0)     3292 2022-10-24 08:08:31.976784 paramspace-2.6.0b2/PKG-INFO
--rw-rw-rw-   0 root         (0) root         (0)    11599 2022-10-24 08:08:21.000000 paramspace-2.6.0b2/README.md
-drwxr-xr-x   0 root         (0) root         (0)        0 2022-10-24 08:08:31.974956 paramspace-2.6.0b2/paramspace/
--rw-rw-rw-   0 root         (0) root         (0)      802 2022-10-24 08:08:21.000000 paramspace-2.6.0b2/paramspace/__init__.py
--rw-rw-rw-   0 root         (0) root         (0)    38373 2022-10-24 08:08:21.000000 paramspace-2.6.0b2/paramspace/paramdim.py
--rw-rw-rw-   0 root         (0) root         (0)    59559 2022-10-24 08:08:21.000000 paramspace-2.6.0b2/paramspace/paramspace.py
--rw-rw-rw-   0 root         (0) root         (0)    18306 2022-10-24 08:08:21.000000 paramspace-2.6.0b2/paramspace/tools.py
--rw-rw-rw-   0 root         (0) root         (0)     5551 2022-10-24 08:08:21.000000 paramspace-2.6.0b2/paramspace/yaml.py
--rw-rw-rw-   0 root         (0) root         (0)     8479 2022-10-24 08:08:21.000000 paramspace-2.6.0b2/paramspace/yaml_constructors.py
--rw-rw-rw-   0 root         (0) root         (0)     1156 2022-10-24 08:08:21.000000 paramspace-2.6.0b2/paramspace/yaml_representers.py
-drwxr-xr-x   0 root         (0) root         (0)        0 2022-10-24 08:08:31.976784 paramspace-2.6.0b2/paramspace.egg-info/
--rw-r--r--   0 root         (0) root         (0)     3292 2022-10-24 08:08:31.000000 paramspace-2.6.0b2/paramspace.egg-info/PKG-INFO
--rw-r--r--   0 root         (0) root         (0)      384 2022-10-24 08:08:31.000000 paramspace-2.6.0b2/paramspace.egg-info/SOURCES.txt
--rw-r--r--   0 root         (0) root         (0)        1 2022-10-24 08:08:31.000000 paramspace-2.6.0b2/paramspace.egg-info/dependency_links.txt
--rw-r--r--   0 root         (0) root         (0)      196 2022-10-24 08:08:31.000000 paramspace-2.6.0b2/paramspace.egg-info/requires.txt
--rw-r--r--   0 root         (0) root         (0)       11 2022-10-24 08:08:31.000000 paramspace-2.6.0b2/paramspace.egg-info/top_level.txt
--rw-rw-rw-   0 root         (0) root         (0)     1015 2022-10-24 08:08:21.000000 paramspace-2.6.0b2/pyproject.toml
--rw-r--r--   0 root         (0) root         (0)       38 2022-10-24 08:08:31.977697 paramspace-2.6.0b2/setup.cfg
--rw-rw-rw-   0 root         (0) root         (0)     5220 2022-10-24 08:08:21.000000 paramspace-2.6.0b2/setup.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:06:25.333122 paramspace-2.6.1/
+-rw-rw-rw-   0 root         (0) root         (0)     9537 2023-07-23 15:06:15.000000 paramspace-2.6.1/CHANGELOG.md
+-rw-rw-rw-   0 root         (0) root         (0)     1309 2023-07-23 15:06:15.000000 paramspace-2.6.1/LICENSE
+-rw-r--r--   0 root         (0) root         (0)     3290 2023-07-23 15:06:25.333122 paramspace-2.6.1/PKG-INFO
+-rw-rw-rw-   0 root         (0) root         (0)    11599 2023-07-23 15:06:15.000000 paramspace-2.6.1/README.md
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:06:25.331122 paramspace-2.6.1/paramspace/
+-rw-rw-rw-   0 root         (0) root         (0)      800 2023-07-23 15:06:15.000000 paramspace-2.6.1/paramspace/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)    38054 2023-07-23 15:06:15.000000 paramspace-2.6.1/paramspace/paramdim.py
+-rw-rw-rw-   0 root         (0) root         (0)    59852 2023-07-23 15:06:15.000000 paramspace-2.6.1/paramspace/paramspace.py
+-rw-rw-rw-   0 root         (0) root         (0)    17865 2023-07-23 15:06:15.000000 paramspace-2.6.1/paramspace/tools.py
+-rw-rw-rw-   0 root         (0) root         (0)      957 2023-07-23 15:06:15.000000 paramspace-2.6.1/paramspace/yaml.py
+-rw-rw-rw-   0 root         (0) root         (0)     4931 2023-07-23 15:06:15.000000 paramspace-2.6.1/paramspace/yaml_constructors.py
+-rw-rw-rw-   0 root         (0) root         (0)       63 2023-07-23 15:06:15.000000 paramspace-2.6.1/paramspace/yaml_representers.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 15:06:25.333122 paramspace-2.6.1/paramspace.egg-info/
+-rw-r--r--   0 root         (0) root         (0)     3290 2023-07-23 15:06:25.000000 paramspace-2.6.1/paramspace.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)      397 2023-07-23 15:06:25.000000 paramspace-2.6.1/paramspace.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-07-23 15:06:25.000000 paramspace-2.6.1/paramspace.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)      207 2023-07-23 15:06:25.000000 paramspace-2.6.1/paramspace.egg-info/requires.txt
+-rw-r--r--   0 root         (0) root         (0)       11 2023-07-23 15:06:25.000000 paramspace-2.6.1/paramspace.egg-info/top_level.txt
+-rw-rw-rw-   0 root         (0) root         (0)     1024 2023-07-23 15:06:15.000000 paramspace-2.6.1/pyproject.toml
+-rw-r--r--   0 root         (0) root         (0)       38 2023-07-23 15:06:25.333122 paramspace-2.6.1/setup.cfg
+-rw-rw-rw-   0 root         (0) root         (0)     5290 2023-07-23 15:06:15.000000 paramspace-2.6.1/setup.py
```

### Comparing `paramspace-2.6.0b2/LICENSE` & `paramspace-2.6.1/LICENSE`

 * *Files 9% similar despite different names*

```diff
@@ -1,11 +1,10 @@
 BSD 2-Clause License
 
-Copyright (c) 2017 - 2020, Yunus Sevinchan
-All rights reserved.
+Copyright (c) 2017 - 2023, Yunus Sevinchan
 
 Redistribution and use in source and binary forms, with or without
 modification, are permitted provided that the following conditions are met:
 
 1. Redistributions of source code must retain the above copyright notice, this
    list of conditions and the following disclaimer.
 2. Redistributions in binary form must reproduce the above copyright notice,
```

### Comparing `paramspace-2.6.0b2/PKG-INFO` & `paramspace-2.6.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: paramspace
-Version: 2.6.0b2
+Version: 2.6.1
 Summary: Dictionary-based, multi-dimensional parameter space iteration
 Home-page: https://gitlab.com/blsqr/paramspace
 Author: Yunus Sevinchan
 Author-email: yunussevinchan@gmail.com
 License: BSD-2-Clause
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Science/Research
```

### Comparing `paramspace-2.6.0b2/README.md` & `paramspace-2.6.1/README.md`

 * *Files identical despite different names*

### Comparing `paramspace-2.6.0b2/paramspace/__init__.py` & `paramspace-2.6.1/paramspace/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,19 +1,20 @@
 """This package provides classes to conveniently define hierarchically
 structured parameter spaces and iterate over them.
 
 To that end, any dict-like object can be populated with
 :py:class:`~paramspace.paramdim.ParamDim` objects to create a parameter
 dimension at that key. When creating a
 :py:class:`~paramspace.paramspace.ParamSpace` from this dict, it becomes
-possible to iterate over all points in the space created by the parameter dimensions, i.e. the *parameter space*.
+possible to iterate over all points in the space created by the parameter
+dimensions, i.e. the *parameter space*.
 
 Furthermore, the :py:mod:`paramspace.yaml` module provides possibilities to
 define the parameter space fully from YAML configuration files, using custom
 YAML tags.
 """
 
-__version__ = "2.6.0b2"
+__version__ = "2.6.1"
 
 from .paramdim import CoupledParamDim, ParamDim
 from .paramspace import ParamSpace
 from .yaml import yaml, yaml_safe, yaml_unsafe
```

### Comparing `paramspace-2.6.0b2/paramspace/paramdim.py` & `paramspace-2.6.1/paramspace/paramdim.py`

 * *Files 3% similar despite different names*

```diff
@@ -2,16 +2,15 @@
 can be assumed. While they provide iteration abilities on their own, they make
 sense mostly to use as objects in a dict that is converted to a ParamSpace.
 """
 
 import abc
 import copy
 import logging
-import warnings
-from typing import Hashable, Iterable, List, Sequence, Tuple, Union
+from typing import Any, Iterable, List, Optional, Sequence, Tuple, Union
 
 import numpy as np
 
 log = logging.getLogger(__name__)
 
 # -----------------------------------------------------------------------------
 # Small helper classes
@@ -47,15 +46,15 @@
     def to_yaml(cls, representer, node: "Masked"):
         """
         Args:
             representer (ruamel.yaml.representer): The representer module
             node (Masked): The node, i.e. an instance of this class
 
         Returns:
-            the scalar value that this object masks
+            the scalar value that this object masks, without tag
         """
         return representer.represent_data(node._val)
 
 
 class MaskedValueError(ValueError):
     """Raised when trying to set the state of a ParamDim to a masked value"""
 
@@ -85,52 +84,59 @@
     # .........................................................................
 
     def __init__(
         self,
         *,
         default,
         values: Iterable = None,
-        order: float = None,
+        order: Optional[Union[int, float]] = 0,
         name: str = None,
         as_type: str = None,
         assert_unique: bool = True,
         **kwargs,
     ) -> None:
         """Initialise a parameter dimension object.
 
         Args:
             default: default value of this parameter dimension
             values (Iterable, optional): Which discrete values this parameter
                 dimension can take. This argument takes precedence over any
                 constructors given in the kwargs (like range, linspace, …).
             order (float, optional): If given, this allows to specify an order
-                within a ParamSpace that includes this ParamDim object. If not,
-                will use np.inf instead.
+                within a ParamSpace that includes this ParamDim object.
+                Dimensions with lowest ``order`` will then be iterated over
+                more frequently. Default is 0.
             name (str, optional): If given, this is an *additional* name of
                 this ParamDim object, and can be used by the ParamSpace to
                 access this object.
             as_type (str, optional): If given, casts the individual created
                 values to a certain python type. The following string values
                 are possible: str, int, bool, float
             assert_unique (bool, optional): Whether to assert uniqueness of
                 the values among them.
-            **kwargs: Constructors for the `values` argument, valid keys are
-                `range`, `linspace`, and `logspace`; corresponding values are
-                expected to be iterables and are passed to `range(*args)`,
-                `np.linspace(*args)`, or `np.logspace(*args)`, respectively.
+            **kwargs: Constructors for the ``values`` argument, valid keys are
+                ``range``, ``linspace``, and ``logspace``; corresponding
+                values are expected to be iterables and are passed to
+                ``range(*args)``, ``np.linspace(*args)``, or
+                ``np.logspace(*args)``, respectively.
+                See also: :py:func:`numpy.linspace`, :py:func:`numpy.logspace`.
 
         Raises:
             TypeError: For invalid arguments
         """
         # Initialize attributes that are managed by properties or methods
         self._state = 0  # corresponding to the default state
 
         # Set attributes that need no further checks
         self._name = name
-        self._order = order if order is not None else np.inf
+
+        # To allow for <2.6 `order` values, check against None.
+        if order is None:
+            order = 0
+        self._order = order
 
         # Package values into kwargs, for easier handling
         if values is not None:
             kwargs["values"] = values
 
         # Gather the initialization kwargs for use with yaml representer
         init_kwargs = dict(
@@ -229,16 +235,16 @@
 
     @property
     def order(self):
         """The order value."""
         return self._order
 
     @property
-    def default(self):
-        """The default value."""
+    def default(self) -> Union[Any, Masked]:
+        """The default value, which may be masked."""
         return self._default
 
     @property
     def values(self) -> tuple:
         """The values that are iterated over.
 
         Returns:
@@ -511,15 +517,15 @@
     # NOTE The `yaml_tag` class variable needs be set in the derived classes
 
     # Define some settings needed for saving to yaml
     # Which entries to update and with which attribute
     _YAML_UPDATE = dict()
 
     # Which entries to remove if they have a certain value
-    _YAML_REMOVE_IF = dict(name=(None,), order=(None,))
+    _YAML_REMOVE_IF = dict(name=(None,))
 
     @classmethod
     def to_yaml(cls, representer, node):
         """
         Args:
             representer (ruamel.yaml.representer): The representer module
             node (type(self)): The node, i.e. an instance of this class
@@ -545,17 +551,19 @@
             if k not in cls._YAML_REMOVE_IF or v not in cls._YAML_REMOVE_IF[k]
         }
 
         # Can now call the representer
         return representer.represent_mapping(cls.yaml_tag, d)
 
     @classmethod
-    def from_yaml(cls, constructor, node):
-        """The default constructor for ParamDim-derived objects"""
-        return cls(**constructor.construct_mapping(node, deep=True))
+    def from_yaml(cls, loader, node):
+        """The default loader for ParamDim-derived objects"""
+        from .yaml_constructors import _pdim_constructor
+
+        return _pdim_constructor(loader, node, Cls=cls)
 
 
 # -----------------------------------------------------------------------------
 
 
 class ParamDim(ParamDimBase):
     """The ParamDim class."""
@@ -566,50 +574,52 @@
         "_inside_iter",
         "_target_of",
     )
 
     # Define the additional attribute names that are to be added to __repr__
     _REPR_ATTRS = ("mask",)
 
-    # Define the yaml tag to use
-    yaml_tag = "!pdim"
+    # The YAML tag to use for representation
+    yaml_tag = "!sweep"
 
     # And the other yaml representer settings
     _YAML_UPDATE = dict(
         mask="mask",
     )
     _YAML_REMOVE_IF = dict(
         name=(None,),
-        order=(None,),
         mask=(None, False),
     )
 
     # .........................................................................
 
     def __init__(self, *, mask: Union[bool, Tuple[bool]] = False, **kwargs):
         """Initialize a regular parameter dimension.
 
         Args:
             mask (Union[bool, Tuple[bool]], optional): Which values of the
                 dimension to mask, i.e., skip in iteration. Note that masked
                 values still count to the length of the parameter dimension!
-            **kwargs: Passed to ``ParamDimBase.__init__``.
+            **kwargs: Passed to :py:meth:`ParamDimBase.__init__`.
                 Possible arguments:
 
-                - default: default value of this parameter dimension
-                - values (Iterable, optional): Which discrete values this
+                - ``default``: default value of this parameter dimension
+                - ``values`` (Iterable, optional): Which discrete values this
                     parameter dimension can take. This argument takes
                     precedence over any constructors given in the kwargs
                     (like range, linspace, …).
-                - order (float, optional): If given, this allows to specify an
-                    order within a ParamSpace that includes this ParamDim. If
-                    not given, np.inf will be used, i.e., dimension is last.
-                - name (str, optional): If given, this is an *additional* name
-                    of this ParamDim object, and can be used by the ParamSpace
-                    to access this object.
+                - ``order`` (float, optional): If given, this allows to
+                    specify an order within a ParamSpace that includes this
+                    ParamDim. If not given, 0 will be used.
+                    See :py:meth:`~paramspace.paramspace.ParamSpace.iterator`
+                    for more information on iteration order.
+                - ``name`` (str, optional): If given, this is an *additional*
+                    name of this ParamDim object, and can be used by the
+                    :py:class:`~paramspace.paramspace.ParamSpace` to access
+                    this object.
                 - ``**kwargs``: Constructors for the ``values`` argument, valid
                     keys are ``range``, ``linspace``, and ``logspace``;
                     corresponding values are expected to be iterables and are
                     passed to ``range(*args)``, ``np.linspace(*args)``, or
                     ``np.logspace(*args)``, respectively.
         """
         super().__init__(**kwargs)
@@ -705,14 +715,15 @@
         Args:
             mask (Union[bool, Tuple[bool]]): A bool or an iterable of booleans
 
         Raises:
             ValueError: If the length of the iterable does not match that of
                 this parameter dimension
         """
+
         # Helper function for setting a mask value
         def set_val(mask: bool, val):
             if mask and not isinstance(val, Masked):
                 # Should be masked but is not
                 return Masked(val)
 
             elif isinstance(val, Masked) and not mask:
@@ -849,43 +860,39 @@
     _REPR_ATTRS = (
         "target_pdim",
         "target_name",
         "_use_coupled_default",
         "_use_coupled_values",
     )
 
-    # Define the yaml tag to use
-    yaml_tag = "!coupled-pdim"
+    # The YAML tag to use for representation
+    yaml_tag = "!coupled-sweep"
 
     # And the other yaml representer settings
     _YAML_UPDATE = dict(
         target_name="_target_name_as_list",
     )
     _YAML_REMOVE_IF = dict(
         name=(None,),
         order=(None,),
         assert_unique=(True, False),
         default=(None,),
         values=(None, [None]),
-        use_coupled_default=(None,),
-        use_coupled_values=(None,),
         target_name=(None,),
         target_pdim=(None,),
     )
 
     # .........................................................................
 
     def __init__(
         self,
         *,
         default=None,
         target_pdim: ParamDim = None,
         target_name: Union[str, Sequence[str]] = None,
-        use_coupled_default: bool = None,
-        use_coupled_values: bool = None,
         **kwargs,
     ):
         """Initialize a coupled parameter dimension.
 
         If the `default` or any values-setting argument is set, those will be
         used. If that is not the case, the respective parts from the coupled
         dimension will be used.
@@ -894,36 +901,22 @@
             default (None, optional): The default value. If not given, will
                 use the one from the coupled object.
             target_pdim (ParamDim, optional): The ParamDim object to couple to
             target_name (Union[str, Sequence[str]], optional): The *name* of
                 the ParamDim object to couple to; needs to be within the same
                 ParamSpace and the ParamSpace needs to be able to resolve it
                 using this name.
-            use_coupled_default (bool, optional): DEPRECATED
-            use_coupled_values (bool, optional): DEPRECATED
             **kwargs: Passed to ParamDimBase.__init__
 
         Raises:
             TypeError: If neither target_pdim nor target_name were given or
                 or both were given
         """
         # TODO Make this __init__ more elegant!
 
-        # Deprecation warnings for old parameters
-        if use_coupled_default is not None or use_coupled_values is not None:
-            warnings.warn(
-                "The CoupledParamDim.__init__ parameters "
-                "`use_coupled_default` and `use_coupled_values` are "
-                "deprecated and will soon be removed. Whether the "
-                "counterpart from the coupled parameter dimension "
-                "is to be used is determined by whether the "
-                "`default` or any value-setting argument was given.",
-                DeprecationWarning,
-            )
-
         # Disallow mask argument
         if "mask" in kwargs:
             raise TypeError(
                 "Received invalid keyword-argument `mask` for "
                 "CoupledParamDim!"
             )
 
@@ -1087,15 +1080,15 @@
 
         self._target_pdim = pdim
         log.debug("Set CoupledParamDim target.")
 
     # Properties that need to relay to the coupled ParamDim ...................
 
     @property
-    def default(self):
+    def default(self) -> Union[Any, Masked]:
         """The default value.
 
         Returns:
             the default value this parameter dimension can take.
 
         Raises:
             RuntimeError: If no ParamDim was associated yet
```

### Comparing `paramspace-2.6.0b2/paramspace/paramspace.py` & `paramspace-2.6.1/paramspace/paramspace.py`

 * *Files 1% similar despite different names*

```diff
@@ -2,16 +2,15 @@
 
 import collections
 import copy
 import logging
 import warnings
 from collections import OrderedDict
 from functools import reduce
-from itertools import chain
-from typing import Any, Dict, Generator, List, Sequence, Set, Tuple, Union
+from typing import Dict, Generator, List, Sequence, Set, Tuple, Union
 
 import numpy as np
 import numpy.ma
 
 from .paramdim import CoupledParamDim, Masked, ParamDim, ParamDimBase
 from .tools import recursive_collect, recursive_replace, recursive_update
 
@@ -75,33 +74,36 @@
         self._iter = None
 
     def _gather_paramdims(self):
         """Gathers ParamDim objects by recursively going through the dict"""
         log.debug("Gathering ParamDim objects ...")
 
         # Traverse the dict and look for ParamDim objects; collect them as
-        # (order, key, value) tuples
+        # (order, key, value) tuples, such that they can be sorted by the
+        # iteration order.
         pdims = recursive_collect(
             self._dict,
             select_func=lambda p: isinstance(p, ParamDim),
             prepend_info=("info_func", "keys"),
             info_func=lambda p: p.order,
             stop_recursion_types=(ParamDimBase,),
         )
 
         # Parse the dimension names
 
         # Sort them -- very important for consistency!
-        # This looks at the info first, which is the order entry, and then at
-        # the keys. If a ParamDim does not provide an order, it has entry
-        # np.inf there, such that those without order get sorted by the key.
+        # This looks at the info first, which is the `order` entry, and then at
+        # the keys. If a ParamDim does not provide an order, it has entry 0
+        # there, such that entries with the same `order` value get sorted by
+        # their key.
         pdims.sort()
 
         # For initializing OrderedDicts, need to reduce the list items to
-        # 2-tuples, ditching the first element (order, needed for sorting)
+        # 2-tuples, ditching the first element (order) which we needed for
+        # sorting
         pdims = [tpl[1:] for tpl in pdims]
 
         # Now, first save the objects with keys that represent their location
         # inside the dictionary.
         self._dims_by_loc = OrderedDict(pdims)
 
         # For easier access, save them in another dict, where the keys are pure
@@ -795,17 +797,15 @@
         for name, pdim in self.dims.items():
             l += [f"  - {name}"]
             l += [f"      {pdim.values}"]
 
             if pdim.mask is True:
                 l += [f"      fully masked -> using default:  {pdim.default}"]
 
-            if pdim.order < np.inf:
-                l += [f"      order: {pdim.order}"]
-
+            l += [f"      order: {pdim.order}"]
             l += [""]
 
         # CoupledParamDim information
         if self.num_coupled_dims:
             l += [""]
             l += ["Coupled Parameter Dimensions"]
             l += ["----------------------------"]
@@ -898,17 +898,19 @@
                     od[k] = to_dict(v)
             return dict(od)
 
         # Can now call the representer
         return representer.represent_mapping(cls.yaml_tag, to_dict(d))
 
     @classmethod
-    def from_yaml(cls, constructor, node):
+    def from_yaml(cls, loader, node):
         """The default constructor for a ParamSpace object"""
-        return cls(**constructor.construct_mapping(node, deep=True))
+        from .yaml_constructors import _pspace_constructor
+
+        return _pspace_constructor(loader, node, Cls=cls)
 
     # Dict access .............................................................
     # This is a restricted interface for accessing dictionary items
     # It ensures that the ParamSpace remains in a valid state: items are only
     # returned by copy or, if popping them, it is ensured that the item was not
     # a parameter dimension.
 
@@ -952,29 +954,32 @@
         *,
         with_info: Union[str, Tuple[str]] = None,
         omit_pt: bool = False,
     ) -> Generator[dict, None, None]:
         """Returns an iterator (more precisely: a generator) yielding all
         unmasked points of the parameter space.
 
-        To control which information is returned at each point, the `with_info`
-        and `omit_pt` arguments can be used. By default, the generator will
-        return a single dictionary.
+        Iteration order depends on the ``order`` parameter, where smaller
+        values of a parameter dimension will lead to more frequent iterations.
+
+        To control which information is returned at each point, the
+        ``with_info`` and `omit_pt` arguments can be used. By default, the
+        generator will return a single dictionary for each iteration point.
 
         Note that an iteration is also possible for zero-volume parameter
         spaces, i.e. where no parameter dimensions were defined.
 
         Args:
             with_info (Union[str, Tuple[str]], optional): Can pass strings
-                here that are to be returned as the second value. Possible
-                values are: 'state_no', 'state_vector', 'state_no_str', and
-                'current_coords'.
-                To get multiple, add them to a tuple.
+                here that are to be returned as the second value.
+                Possible values are: ``state_no``, ``state_vector``,
+                ``state_no_str``, and ``current_coords``.
+                To get multiple of them, add them to a tuple.
             omit_pt (bool, optional): If true, the current value is omitted and
-                only the information is returned.
+                *only* the information tuple is returned.
 
         Returns:
             Generator[dict, None, None]: yields point after point of the
                 ParamSpace and the corresponding information
         """
 
         # Parse the with_info argument, making sure it is a tuple
@@ -1333,15 +1338,15 @@
     def set_masks(self, *mask_specs) -> None:
         """Sets multiple mask specifications after another. Note that the order
         is maintained and that sequential specifications can apply to the same
         parameter dimensions.
 
         Args:
             *mask_specs: Can be tuples/lists or dicts which will be unpacked
-                (in the given order) and passed to .set_mask
+                (in the given order) and passed to :py:meth:`.set_mask`
         """
         log.debug("Setting %d masks ...", len(mask_specs))
 
         for ms in mask_specs:
             if isinstance(ms, dict):
                 self.set_mask(**ms)
             else:
```

### Comparing `paramspace-2.6.0b2/paramspace/tools.py` & `paramspace-2.6.1/paramspace/tools.py`

 * *Files 5% similar despite different names*

```diff
@@ -29,58 +29,14 @@
 
     pass
 
 
 # Initialize a global Skip object, simplifying calls and detection.
 SKIP = Skip()
 
-# .............................................................................
-
-
-def create_indices(
-    *,
-    from_range: list = None,
-    unique: bool = False,
-    sort: bool = True,
-    append: list = None,
-    remove: list = None,
-) -> List[int]:
-    """Generates a list of integer elements.
-
-    Args:
-        from_range (list, optional): range arguments to use as the basis of the
-            list
-        unique (bool, optional): Whether to ascertain uniqueness of elements
-        sort (bool, optional): Whether to sort the list before returning
-        append (list, optional): Additional elements to append to the list
-        remove (list, optional): Elements to remove all occurrences of
-
-    Returns:
-        List[int]: The generated list
-    """
-    l = []
-    if from_range:
-        l += list(range(*from_range))
-
-    if append:
-        l += append
-
-    if remove:
-        for element_to_remove in list(set(remove)):
-            while element_to_remove in l:
-                l.remove(element_to_remove)
-
-    if unique:
-        l = list(set(l))
-
-    if sort:
-        l.sort()
-
-    return l
-
 
 # -----------------------------------------------------------------------------
 
 
 def recursive_contains(
     obj: Union[Mapping, Sequence], *, keys: Sequence
 ) -> bool:
@@ -474,14 +430,38 @@
 
         # else: was not selected and cannot be further recursed, thus: stays
         # the same
 
     return obj
 
 
+def recursively_sort_dict(d: dict) -> collections.OrderedDict:
+    """Recursively sorts a dictionary by its keys, transforming it to an
+    OrderedDict in the process.
+
+    From: http://stackoverflow.com/a/22721724/1827608
+
+    Args:
+        d (dict): The dictionary to be sorted
+
+    Returns:
+        OrderedDict: the recursively sorted dict
+    """
+    # Start with empty ordered dict for this recursion level
+    res = collections.OrderedDict()
+
+    # Fill it with the values from the dictionary
+    for k, v in sorted(d.items()):
+        if isinstance(v, dict):
+            res[k] = recursively_sort_dict(v)
+        else:
+            res[k] = v
+    return res
+
+
 # Helpers ---------------------------------------------------------------------
 
 
 def is_iterable(obj) -> bool:
     """Whether the given object is iterable or not.
 
     This is tested simply by invoking ``iter(obj)`` and returning ``False`` if
```

### Comparing `paramspace-2.6.0b2/paramspace.egg-info/PKG-INFO` & `paramspace-2.6.1/paramspace.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: paramspace
-Version: 2.6.0b2
+Version: 2.6.1
 Summary: Dictionary-based, multi-dimensional parameter space iteration
 Home-page: https://gitlab.com/blsqr/paramspace
 Author: Yunus Sevinchan
 Author-email: yunussevinchan@gmail.com
 License: BSD-2-Clause
 Classifier: Development Status :: 5 - Production/Stable
 Classifier: Intended Audience :: Science/Research
```

### Comparing `paramspace-2.6.0b2/pyproject.toml` & `paramspace-2.6.1/pyproject.toml`

 * *Files 10% similar despite different names*

```diff
@@ -15,15 +15,15 @@
 use_parentheses = true
 line_length = 79
 
 
 # Black configuration .........................................................
 [tool.black]
 line-length = 79
-target-version = ["py36", "py37", "py38", "py39", "py310"]
+target-version = ["py36", "py37", "py38", "py39", "py310", "py311"]
 
 # NOTE: you have to use single-quoted strings in TOML for regular expressions.
 # It's the equivalent of r-strings in Python.  Multiline strings are treated as
 # verbose regular expressions by Black.  Use [ ] to denote a significant space
 # character.
 exclude = '''
 /(
```

### Comparing `paramspace-2.6.0b2/setup.py` & `paramspace-2.6.1/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,16 @@
 #!/usr/bin/env python3
 from setuptools import setup
 
 # Dependencies for paramspace itself
 install_deps = [
-    "numpy",
+    "numpy < 2.0",
     "xarray",
     "ruamel.yaml",
+    "yayaml",
 ]
 
 # Dependencies for executing tests
 test_deps = [
     "tox",
     "pytest",
     "pytest-cov",
@@ -90,14 +91,15 @@
 or the `Utopia Project <https://utopia-project.org/>`_.
 
 """
 
 
 # .............................................................................
 
+
 # A function to extract version number from __init__.py
 def find_version(*file_paths) -> str:
     """Tries to extract a version from the given path sequence"""
     import codecs
     import os
     import re
 
@@ -126,31 +128,33 @@
     author_email="yunussevinchan@gmail.com",
     url="https://gitlab.com/blsqr/paramspace",
     license="BSD-2-Clause",
     classifiers=[
         "Development Status :: 5 - Production/Stable",
         "Intended Audience :: Science/Research",
         "License :: OSI Approved :: BSD License",
+        #
         "Programming Language :: Python :: 3",
         "Programming Language :: Python :: 3 :: Only",
         "Programming Language :: Python :: 3.6",
         "Programming Language :: Python :: 3.7",
         "Programming Language :: Python :: 3.8",
         "Programming Language :: Python :: 3.9",
         "Programming Language :: Python :: 3.10",
         "Programming Language :: Python :: 3.11",
+        #
         "Topic :: Utilities",
         "Typing :: Typed",
     ],
     packages=["paramspace"],
     include_package_data=True,
     python_requires=">=3.6",
     install_requires=install_deps,
     tests_require=test_deps,
     test_suite="tox",
     extras_require=dict(
         test=test_deps,
         dev=dev_deps,
         doc=doc_deps,
     ),
-    data_files=[("", ["LICENSE"])],
+    data_files=[("", ["LICENSE", "README.md", "CHANGELOG.md"])],
 )
```

