# Comparing `tmp/yayaml-0.1.0.tar.gz` & `tmp/yayaml-0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "yayaml-0.1.0.tar", last modified: Tue Jul 18 18:16:32 2023, max compression
+gzip compressed data, was "yayaml-0.1.1.tar", last modified: Sun Jul 23 14:14:45 2023, max compression
```

## Comparing `yayaml-0.1.0.tar` & `yayaml-0.1.1.tar`

### file list

```diff
@@ -1,29 +1,26 @@
-drwxr-xr-x   0 yunus      (501) staff       (20)        0 2023-07-18 18:16:32.966817 yayaml-0.1.0/
--rw-r--r--   0 yunus      (501) staff       (20)      514 2023-07-18 18:03:22.000000 yayaml-0.1.0/CHANGELOG.md
--rw-r--r--   0 yunus      (501) staff       (20)     1309 2023-07-18 17:38:17.000000 yayaml-0.1.0/LICENSE
--rw-r--r--   0 yunus      (501) staff       (20)      795 2023-07-18 18:16:32.966695 yayaml-0.1.0/PKG-INFO
--rw-r--r--   0 yunus      (501) staff       (20)     2063 2023-07-18 18:04:06.000000 yayaml-0.1.0/README.md
--rw-r--r--   0 yunus      (501) staff       (20)     1827 2023-07-18 12:03:41.000000 yayaml-0.1.0/pyproject.toml
--rw-r--r--   0 yunus      (501) staff       (20)       38 2023-07-18 18:16:32.966855 yayaml-0.1.0/setup.cfg
--rw-r--r--   0 yunus      (501) staff       (20)     2805 2023-07-18 18:09:24.000000 yayaml-0.1.0/setup.py
-drwxr-xr-x   0 yunus      (501) staff       (20)        0 2023-07-18 18:16:32.963998 yayaml-0.1.0/tests/
-drwxr-xr-x   0 yunus      (501) staff       (20)        0 2023-07-18 18:16:32.964420 yayaml-0.1.0/tests/_gen_figures/
--rw-r--r--   0 yunus      (501) staff       (20)      117 2023-07-18 12:03:41.000000 yayaml-0.1.0/tests/_gen_figures/__init__.py
--rw-r--r--   0 yunus      (501) staff       (20)      779 2023-07-18 12:03:41.000000 yayaml-0.1.0/tests/_gen_figures/gen_doc_examples.py
--rw-r--r--   0 yunus      (501) staff       (20)      126 2023-07-18 12:03:41.000000 yayaml-0.1.0/tests/test__import.py
--rw-r--r--   0 yunus      (501) staff       (20)     4695 2023-07-18 17:45:54.000000 yayaml-0.1.0/tests/test_io.py
--rw-r--r--   0 yunus      (501) staff       (20)    13429 2023-07-18 17:45:54.000000 yayaml-0.1.0/tests/test_yaml.py
-drwxr-xr-x   0 yunus      (501) staff       (20)        0 2023-07-18 18:16:32.965835 yayaml-0.1.0/yayaml/
--rw-r--r--   0 yunus      (501) staff       (20)      547 2023-07-18 17:58:14.000000 yayaml-0.1.0/yayaml/__init__.py
--rw-r--r--   0 yunus      (501) staff       (20)     7493 2023-07-18 17:45:54.000000 yayaml-0.1.0/yayaml/_constructors.py
--rw-r--r--   0 yunus      (501) staff       (20)     2336 2023-07-18 17:45:54.000000 yayaml-0.1.0/yayaml/_exceptions.py
--rw-r--r--   0 yunus      (501) staff       (20)     5118 2023-07-18 17:45:54.000000 yayaml-0.1.0/yayaml/_io.py
--rw-r--r--   0 yunus      (501) staff       (20)     1484 2023-07-18 17:45:54.000000 yayaml-0.1.0/yayaml/_representers.py
--rw-r--r--   0 yunus      (501) staff       (20)     1993 2023-07-18 17:45:54.000000 yayaml-0.1.0/yayaml/_tools.py
--rw-r--r--   0 yunus      (501) staff       (20)     4237 2023-07-18 17:45:54.000000 yayaml-0.1.0/yayaml/_yaml.py
-drwxr-xr-x   0 yunus      (501) staff       (20)        0 2023-07-18 18:16:32.966533 yayaml-0.1.0/yayaml.egg-info/
--rw-r--r--   0 yunus      (501) staff       (20)      795 2023-07-18 18:16:32.000000 yayaml-0.1.0/yayaml.egg-info/PKG-INFO
--rw-r--r--   0 yunus      (501) staff       (20)      467 2023-07-18 18:16:32.000000 yayaml-0.1.0/yayaml.egg-info/SOURCES.txt
--rw-r--r--   0 yunus      (501) staff       (20)        1 2023-07-18 18:16:32.000000 yayaml-0.1.0/yayaml.egg-info/dependency_links.txt
--rw-r--r--   0 yunus      (501) staff       (20)      283 2023-07-18 18:16:32.000000 yayaml-0.1.0/yayaml.egg-info/requires.txt
--rw-r--r--   0 yunus      (501) staff       (20)       13 2023-07-18 18:16:32.000000 yayaml-0.1.0/yayaml.egg-info/top_level.txt
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 14:14:45.231578 yayaml-0.1.1/
+-rw-rw-rw-   0 root         (0) root         (0)      585 2023-07-23 14:14:35.000000 yayaml-0.1.1/CHANGELOG.md
+-rw-rw-rw-   0 root         (0) root         (0)     1309 2023-07-23 14:14:35.000000 yayaml-0.1.1/LICENSE
+-rw-r--r--   0 root         (0) root         (0)      795 2023-07-23 14:14:45.231578 yayaml-0.1.1/PKG-INFO
+-rw-rw-rw-   0 root         (0) root         (0)     2063 2023-07-23 14:14:35.000000 yayaml-0.1.1/README.md
+-rw-rw-rw-   0 root         (0) root         (0)     1827 2023-07-23 14:14:35.000000 yayaml-0.1.1/pyproject.toml
+-rw-r--r--   0 root         (0) root         (0)       38 2023-07-23 14:14:45.231578 yayaml-0.1.1/setup.cfg
+-rw-rw-rw-   0 root         (0) root         (0)     2805 2023-07-23 14:14:35.000000 yayaml-0.1.1/setup.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 14:14:45.227578 yayaml-0.1.1/tests/
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 14:14:45.228578 yayaml-0.1.1/tests/_gen_figures/
+-rw-rw-rw-   0 root         (0) root         (0)      117 2023-07-23 14:14:35.000000 yayaml-0.1.1/tests/_gen_figures/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)      779 2023-07-23 14:14:35.000000 yayaml-0.1.1/tests/_gen_figures/gen_doc_examples.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 14:14:45.230578 yayaml-0.1.1/yayaml/
+-rw-rw-rw-   0 root         (0) root         (0)      706 2023-07-23 14:14:35.000000 yayaml-0.1.1/yayaml/__init__.py
+-rw-rw-rw-   0 root         (0) root         (0)     7489 2023-07-23 14:14:35.000000 yayaml-0.1.1/yayaml/constructors.py
+-rw-rw-rw-   0 root         (0) root         (0)     2336 2023-07-23 14:14:35.000000 yayaml-0.1.1/yayaml/exceptions.py
+-rw-rw-rw-   0 root         (0) root         (0)     5116 2023-07-23 14:14:35.000000 yayaml-0.1.1/yayaml/io.py
+-rw-rw-rw-   0 root         (0) root         (0)     1483 2023-07-23 14:14:35.000000 yayaml-0.1.1/yayaml/representers.py
+-rw-rw-rw-   0 root         (0) root         (0)     1993 2023-07-23 14:14:35.000000 yayaml-0.1.1/yayaml/tools.py
+-rw-rw-rw-   0 root         (0) root         (0)     4236 2023-07-23 14:14:35.000000 yayaml-0.1.1/yayaml/yaml.py
+drwxr-xr-x   0 root         (0) root         (0)        0 2023-07-23 14:14:45.230578 yayaml-0.1.1/yayaml.egg-info/
+-rw-r--r--   0 root         (0) root         (0)      795 2023-07-23 14:14:45.000000 yayaml-0.1.1/yayaml.egg-info/PKG-INFO
+-rw-r--r--   0 root         (0) root         (0)      403 2023-07-23 14:14:45.000000 yayaml-0.1.1/yayaml.egg-info/SOURCES.txt
+-rw-r--r--   0 root         (0) root         (0)        1 2023-07-23 14:14:45.000000 yayaml-0.1.1/yayaml.egg-info/dependency_links.txt
+-rw-r--r--   0 root         (0) root         (0)      283 2023-07-23 14:14:45.000000 yayaml-0.1.1/yayaml.egg-info/requires.txt
+-rw-r--r--   0 root         (0) root         (0)       13 2023-07-23 14:14:45.000000 yayaml-0.1.1/yayaml.egg-info/top_level.txt
```

### Comparing `yayaml-0.1.0/CHANGELOG.md` & `yayaml-0.1.1/CHANGELOG.md`

 * *Files 26% similar despite different names*

```diff
@@ -1,11 +1,14 @@
 # Changelog
 
 `yayaml` aims to adhere to [semantic versioning](https://semver.org/).
 
+## 0.1.1
+- !1 changes module names to no longer be prefixed with `_`.
+
 ## 0.1.0
 
 This initial version moves the YAML-related tools that were integrated into the [paramspace](https://gitlab.com/blsqr/paramspace) package (prior to its 2.6 release) into this new package named `yayaml`.
 
 yay :)
 
 Specifically, it is based on code from commit [`7b1d2e7`](https://gitlab.com/blsqr/paramspace/-/commit/7b1d2e7e44fe38dadb0e6af901d72299b1ed6dd0), but already makes a number of abstractions and improvements.
```

### Comparing `yayaml-0.1.0/LICENSE` & `yayaml-0.1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `yayaml-0.1.0/PKG-INFO` & `yayaml-0.1.1/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: yayaml
-Version: 0.1.0
+Version: 0.1.1
 Summary: yayaml makes yaml nicer. yay!
 Home-page: https://gitlab.com/blsqr/yayaml
 Author: Yunus Sevinchan
 Author-email: Yunus Sevinchan <yunussevinchan@gmail.com>
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
```

### Comparing `yayaml-0.1.0/README.md` & `yayaml-0.1.1/README.md`

 * *Files identical despite different names*

### Comparing `yayaml-0.1.0/pyproject.toml` & `yayaml-0.1.1/pyproject.toml`

 * *Files identical despite different names*

### Comparing `yayaml-0.1.0/setup.py` & `yayaml-0.1.1/setup.py`

 * *Files identical despite different names*

### Comparing `yayaml-0.1.0/tests/_gen_figures/gen_doc_examples.py` & `yayaml-0.1.1/tests/_gen_figures/gen_doc_examples.py`

 * *Files identical despite different names*

### Comparing `yayaml-0.1.0/yayaml/_constructors.py` & `yayaml-0.1.1/yayaml/constructors.py`

 * *Files 1% similar despite different names*

```diff
@@ -7,16 +7,16 @@
 from functools import partial as _partial
 from functools import reduce as _reduce
 from typing import Any, Callable
 
 import numpy as np
 import ruamel.yaml
 
-from . import _tools
-from ._yaml import (
+from . import tools
+from .yaml import (
     BaseLoader,
     ConstructorFunc,
     Node,
     add_constructor,
     is_constructor,
 )
 
@@ -204,15 +204,15 @@
     "!expr",
     aliases=("!expression", "!compute"),
     hint="Check the expression syntax",
 )
 def expression(loader: BaseLoader, node: Node):
     """Constructor that evaluates strings of simple mathematical expressions"""
     expr_str = loader.construct_scalar(node)
-    return _tools.eval_simple_math_expr(expr_str)
+    return tools.eval_simple_math_expr(expr_str)
 
 
 @is_constructor("!listgen")
 def listgen(loader: BaseLoader, node: Node):
     """Constructor for lists, where node can be a mapping or sequence"""
     if isinstance(node, ruamel.yaml.nodes.MappingNode):
         kwargs = loader.construct_mapping(node, deep=True)
@@ -222,8 +222,8 @@
 
     else:
         raise TypeError(
             f"Expected mapping or sequence node for !listgen, but "
             f"got {type(node)}!"
         )
 
-    return _tools.listgen(**kwargs)
+    return tools.listgen(**kwargs)
```

### Comparing `yayaml-0.1.0/yayaml/_exceptions.py` & `yayaml-0.1.1/yayaml/exceptions.py`

 * *Files identical despite different names*

### Comparing `yayaml-0.1.0/yayaml/_io.py` & `yayaml-0.1.1/yayaml/io.py`

 * *Files 1% similar despite different names*

```diff
@@ -3,20 +3,20 @@
 import io
 import logging
 import os
 from typing import Any, Union
 
 import ruamel.yaml
 
-from ._exceptions import (
+from .exceptions import (
     YAML_ERROR_HINTS,
     RepresenterError,
     raise_improved_exception,
 )
-from ._yaml import yaml
+from .yaml import yaml
 
 log = logging.getLogger(__name__)
 
 # -- Writing and reading from files -------------------------------------------
 
 
 def load_yml(
```

### Comparing `yayaml-0.1.0/yayaml/_representers.py` & `yayaml-0.1.1/yayaml/representers.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 """This module implements custom YAML representer functions"""
 
 from typing import Any, Callable, Union
 
-from ._yaml import (
+from .yaml import (
     BaseRepresenter,
     Node,
     RepresenterFunc,
     add_representer,
     is_representer,
 )
```

### Comparing `yayaml-0.1.0/yayaml/_tools.py` & `yayaml-0.1.1/yayaml/tools.py`

 * *Files identical despite different names*

### Comparing `yayaml-0.1.0/yayaml/_yaml.py` & `yayaml-0.1.1/yayaml/yaml.py`

 * *Files 0% similar despite different names*

```diff
@@ -7,15 +7,15 @@
 constructors.
 """
 from functools import partial as partial
 from typing import Any, Callable, Dict, List, Optional, Tuple, Union
 
 import ruamel.yaml
 
-from ._exceptions import add_yaml_error_hint
+from .exceptions import add_yaml_error_hint
 
 # -- Types --------------------------------------------------------------------
 
 Node = ruamel.yaml.nodes.Node
 
 BaseLoader = ruamel.yaml.loader.BaseLoader
```

### Comparing `yayaml-0.1.0/yayaml.egg-info/PKG-INFO` & `yayaml-0.1.1/yayaml.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: yayaml
-Version: 0.1.0
+Version: 0.1.1
 Summary: yayaml makes yaml nicer. yay!
 Home-page: https://gitlab.com/blsqr/yayaml
 Author: Yunus Sevinchan
 Author-email: Yunus Sevinchan <yunussevinchan@gmail.com>
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
```

