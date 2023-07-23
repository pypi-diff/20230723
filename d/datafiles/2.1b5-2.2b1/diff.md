# Comparing `tmp/datafiles-2.1b5.tar.gz` & `tmp/datafiles-2.2b1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "datafiles-2.1b5.tar", max compression
+gzip compressed data, was "datafiles-2.2b1.tar", max compression
```

## Comparing `datafiles-2.1b5.tar` & `datafiles-2.2b1.tar`

### file list

```diff
@@ -1,33 +1,33 @@
--rw-r--r--   0        0        0     1088 2019-06-09 21:33:24.000000 datafiles-2.1b5/LICENSE.md
--rw-r--r--   0        0        0     3587 2022-08-20 17:08:29.834288 datafiles-2.1b5/README.md
--rw-r--r--   0        0        0      230 2022-03-05 04:25:20.295998 datafiles-2.1b5/datafiles/__init__.py
--rw-r--r--   0        0        0      929 2022-10-11 11:26:59.042300 datafiles-2.1b5/datafiles/config.py
--rw-r--r--   0        0        0     6817 2022-11-23 17:08:26.552083 datafiles-2.1b5/datafiles/converters/__init__.py
--rw-r--r--   0        0        0     1605 2022-02-02 22:35:04.726189 datafiles-2.1b5/datafiles/converters/_bases.py
--rw-r--r--   0        0        0     1369 2022-02-02 22:35:04.726539 datafiles-2.1b5/datafiles/converters/builtins.py
--rw-r--r--   0        0        0     7651 2022-07-29 16:35:41.392675 datafiles-2.1b5/datafiles/converters/containers.py
--rw-r--r--   0        0        0      605 2022-02-02 22:35:04.727351 datafiles-2.1b5/datafiles/converters/enumerations.py
--rw-r--r--   0        0        0     1038 2022-02-02 22:35:04.727646 datafiles-2.1b5/datafiles/converters/extensions.py
--rw-r--r--   0        0        0     1481 2023-03-26 19:07:40.583195 datafiles-2.1b5/datafiles/decorators.py
--rw-r--r--   0        0        0     3643 2022-11-09 21:15:25.993928 datafiles-2.1b5/datafiles/formats.py
--rw-r--r--   0        0        0     4688 2022-04-22 23:18:12.443625 datafiles-2.1b5/datafiles/hooks.py
--rw-r--r--   0        0        0     6011 2023-02-13 17:48:23.609765 datafiles-2.1b5/datafiles/manager.py
--rw-r--r--   0        0        0    10496 2023-02-13 17:48:23.611367 datafiles-2.1b5/datafiles/mapper.py
--rw-r--r--   0        0        0     2381 2023-02-13 17:48:23.612399 datafiles-2.1b5/datafiles/model.py
--rw-r--r--   0        0        0     1206 2022-11-23 17:06:22.694080 datafiles-2.1b5/datafiles/plugins.py
--rw-r--r--   0        0        0        0 2023-03-26 19:40:43.756929 datafiles-2.1b5/datafiles/py.typed
--rw-r--r--   0        0        0      133 2021-05-26 11:50:47.865164 datafiles-2.1b5/datafiles/settings.py
--rw-r--r--   0        0        0      362 2022-07-29 16:35:41.394659 datafiles-2.1b5/datafiles/tests/__init__.py
--rw-r--r--   0        0        0    16339 2022-08-20 17:08:29.835977 datafiles-2.1b5/datafiles/tests/test_converters.py
--rw-r--r--   0        0        0      923 2020-05-02 16:10:37.000000 datafiles-2.1b5/datafiles/tests/test_decorators.py
--rw-r--r--   0        0        0     1789 2022-02-02 22:35:04.730640 datafiles-2.1b5/datafiles/tests/test_formats.py
--rw-r--r--   0        0        0     2006 2022-02-02 22:35:04.730913 datafiles-2.1b5/datafiles/tests/test_generics.py
--rw-r--r--   0        0        0     1585 2022-04-22 23:06:52.609396 datafiles-2.1b5/datafiles/tests/test_hooks.py
--rw-r--r--   0        0        0     5555 2023-02-11 00:35:02.076274 datafiles-2.1b5/datafiles/tests/test_manager.py
--rw-r--r--   0        0        0     3849 2022-10-11 11:26:59.046450 datafiles-2.1b5/datafiles/tests/test_mapper.py
--rw-r--r--   0        0        0      609 2023-02-13 17:48:23.612872 datafiles-2.1b5/datafiles/tests/test_model.py
--rw-r--r--   0        0        0     2790 2022-03-07 14:07:43.245444 datafiles-2.1b5/datafiles/tests/test_utils.py
--rw-r--r--   0        0        0      743 2022-04-16 23:56:46.724770 datafiles-2.1b5/datafiles/types.py
--rw-r--r--   0        0        0     4242 2022-04-16 23:57:40.170785 datafiles-2.1b5/datafiles/utils.py
--rw-r--r--   0        0        0     2015 2023-03-26 19:40:43.757150 datafiles-2.1b5/pyproject.toml
--rw-r--r--   0        0        0     5193 1970-01-01 00:00:00.000000 datafiles-2.1b5/PKG-INFO
+-rw-r--r--   0        0        0     1088 2019-06-09 21:33:24.000000 datafiles-2.2b1/LICENSE.md
+-rw-r--r--   0        0        0     3591 2023-07-21 15:51:12.989466 datafiles-2.2b1/README.md
+-rw-r--r--   0        0        0      236 2023-07-21 15:53:49.187973 datafiles-2.2b1/datafiles/__init__.py
+-rw-r--r--   0        0        0      929 2022-10-11 11:26:59.042300 datafiles-2.2b1/datafiles/config.py
+-rw-r--r--   0        0        0     6817 2022-11-23 17:08:26.552083 datafiles-2.2b1/datafiles/converters/__init__.py
+-rw-r--r--   0        0        0     1605 2022-02-02 22:35:04.726189 datafiles-2.2b1/datafiles/converters/_bases.py
+-rw-r--r--   0        0        0     1369 2022-02-02 22:35:04.726539 datafiles-2.2b1/datafiles/converters/builtins.py
+-rw-r--r--   0        0        0     7671 2023-05-05 12:00:14.196700 datafiles-2.2b1/datafiles/converters/containers.py
+-rw-r--r--   0        0        0      605 2022-02-02 22:35:04.727351 datafiles-2.2b1/datafiles/converters/enumerations.py
+-rw-r--r--   0        0        0     1038 2022-02-02 22:35:04.727646 datafiles-2.2b1/datafiles/converters/extensions.py
+-rw-r--r--   0        0        0     2334 2023-07-23 04:01:33.922645 datafiles-2.2b1/datafiles/decorators.py
+-rw-r--r--   0        0        0     3643 2022-11-09 21:15:25.993928 datafiles-2.2b1/datafiles/formats.py
+-rw-r--r--   0        0        0     4688 2022-04-22 23:18:12.443625 datafiles-2.2b1/datafiles/hooks.py
+-rw-r--r--   0        0        0     6011 2023-02-13 17:48:23.609765 datafiles-2.2b1/datafiles/manager.py
+-rw-r--r--   0        0        0    10496 2023-07-21 16:16:07.783884 datafiles-2.2b1/datafiles/mapper.py
+-rw-r--r--   0        0        0     2402 2023-07-23 04:01:33.922788 datafiles-2.2b1/datafiles/model.py
+-rw-r--r--   0        0        0     2373 2023-05-28 18:10:33.298224 datafiles-2.2b1/datafiles/plugins.py
+-rw-r--r--   0        0        0        0 2023-03-26 23:55:27.144248 datafiles-2.2b1/datafiles/py.typed
+-rw-r--r--   0        0        0      133 2021-05-26 11:50:47.865164 datafiles-2.2b1/datafiles/settings.py
+-rw-r--r--   0        0        0      362 2022-07-29 16:35:41.394659 datafiles-2.2b1/datafiles/tests/__init__.py
+-rw-r--r--   0        0        0    16339 2022-08-20 17:08:29.835977 datafiles-2.2b1/datafiles/tests/test_converters.py
+-rw-r--r--   0        0        0     1255 2023-07-23 04:01:33.923084 datafiles-2.2b1/datafiles/tests/test_decorators.py
+-rw-r--r--   0        0        0     1789 2022-02-02 22:35:04.730640 datafiles-2.2b1/datafiles/tests/test_formats.py
+-rw-r--r--   0        0        0     2006 2022-02-02 22:35:04.730913 datafiles-2.2b1/datafiles/tests/test_generics.py
+-rw-r--r--   0        0        0     1585 2022-04-22 23:06:52.609396 datafiles-2.2b1/datafiles/tests/test_hooks.py
+-rw-r--r--   0        0        0     5555 2023-02-11 00:35:02.076274 datafiles-2.2b1/datafiles/tests/test_manager.py
+-rw-r--r--   0        0        0     3849 2022-10-11 11:26:59.046450 datafiles-2.2b1/datafiles/tests/test_mapper.py
+-rw-r--r--   0        0        0      609 2023-02-13 17:48:23.612872 datafiles-2.2b1/datafiles/tests/test_model.py
+-rw-r--r--   0        0        0     2790 2022-03-07 14:07:43.245444 datafiles-2.2b1/datafiles/tests/test_utils.py
+-rw-r--r--   0        0        0      743 2022-04-16 23:56:46.724770 datafiles-2.2b1/datafiles/types.py
+-rw-r--r--   0        0        0     4242 2022-04-16 23:57:40.170785 datafiles-2.2b1/datafiles/utils.py
+-rw-r--r--   0        0        0     2013 2023-07-23 04:01:33.924992 datafiles-2.2b1/pyproject.toml
+-rw-r--r--   0        0        0     5197 1970-01-01 00:00:00.000000 datafiles-2.2b1/PKG-INFO
```

### Comparing `datafiles-2.1b5/LICENSE.md` & `datafiles-2.2b1/LICENSE.md`

 * *Files identical despite different names*

### Comparing `datafiles-2.1b5/README.md` & `datafiles-2.2b1/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 # Datafiles: A file-based ORM for Python dataclasses
 
 Datafiles is a bidirectional serialization library for Python [dataclasses](https://docs.python.org/3/library/dataclasses.html) to synchronize objects to the filesystem using type annotations. It supports a variety of file formats with round-trip preservation of formatting and comments, where possible. Object changes are automatically saved to disk and only include the minimum data needed to restore each object.
 
-[![Travis CI](https://img.shields.io/travis/com/jacebrowning/datafiles/main.svg?label=unix)](https://travis-ci.com/jacebrowning/datafiles)
+[![Travis CI](https://img.shields.io/travis/com/jacebrowning/datafiles/main.svg?label=unix)](https://app.travis-ci.com/jacebrowning/datafiles)
 [![AppVeyor](https://img.shields.io/appveyor/ci/jacebrowning/datafiles/main.svg?label=windows)](https://ci.appveyor.com/project/jacebrowning/datafiles)
 [![Coveralls](https://img.shields.io/coveralls/jacebrowning/datafiles.svg)](https://coveralls.io/r/jacebrowning/datafiles)
 [![PyPI License](https://img.shields.io/pypi/l/datafiles.svg)](https://pypi.org/project/datafiles)
 [![PyPI Version](https://img.shields.io/pypi/v/datafiles.svg)](https://pypi.org/project/datafiles)
 [![PyPI Downloads](https://img.shields.io/pypi/dm/datafiles.svg?color=orange)](https://pypistats.org/packages/datafiles)
 [![Gitter](https://img.shields.io/gitter/room/jacebrowning/datafiles?color=D0164E)](https://gitter.im/jacebrowning/datafiles)
```

### Comparing `datafiles-2.1b5/datafiles/config.py` & `datafiles-2.2b1/datafiles/config.py`

 * *Files identical despite different names*

### Comparing `datafiles-2.1b5/datafiles/converters/__init__.py` & `datafiles-2.2b1/datafiles/converters/__init__.py`

 * *Files identical despite different names*

### Comparing `datafiles-2.1b5/datafiles/converters/_bases.py` & `datafiles-2.2b1/datafiles/converters/_bases.py`

 * *Files identical despite different names*

### Comparing `datafiles-2.1b5/datafiles/converters/builtins.py` & `datafiles-2.2b1/datafiles/converters/builtins.py`

 * *Files identical despite different names*

### Comparing `datafiles-2.1b5/datafiles/converters/containers.py` & `datafiles-2.2b1/datafiles/converters/containers.py`

 * *Files 2% similar despite different names*

```diff
@@ -19,15 +19,15 @@
     def of_type(cls, converter: type):
         name = f"{converter.__name__}{cls.__name__}"
         bases = (cls,)
         attributes = {"CONVERTER": converter}
         return type(name, bases, attributes)
 
     @classmethod
-    def to_python_value(cls, deserialized_data, *, target_object):
+    def to_python_value(cls, deserialized_data, *, target_object=None):
         if target_object is None or target_object is Missing:
             value = []
         else:
             value = target_object
             value.clear()
 
         convert = cls.CONVERTER.to_python_value
@@ -88,15 +88,15 @@
         return data
 
 
 class Set(List):
     """Base converter for sets."""
 
     @classmethod
-    def to_python_value(cls, deserialized_data, *, target_object):
+    def to_python_value(cls, deserialized_data, *, target_object=None):
         if target_object is None or target_object is Missing:
             value = set()
         else:
             value = target_object
             value.clear()
 
         convert = cls.CONVERTER.to_python_value
@@ -133,15 +133,15 @@
             name = f"{key.__name__}{value.__name__}Dict"
         except AttributeError:  # Python < 3.10
             name = "UntypedDict"
         bases = (cls,)
         return type(name, bases, {})
 
     @classmethod
-    def to_python_value(cls, deserialized_data, *, target_object):
+    def to_python_value(cls, deserialized_data, *, target_object=None):
         if isinstance(deserialized_data, dict):
             data = deserialized_data.copy()
         else:
             data = {}
 
         if target_object is None or target_object is Missing:
             value = data
@@ -172,15 +172,15 @@
     def of_mappings(cls, dataclass, converters: Dict[str, type]):
         name = f"{dataclass.__name__}Converter"
         bases = (cls,)
         attributes = {"DATACLASS": dataclass, "CONVERTERS": converters}
         return type(name, bases, attributes)
 
     @classmethod
-    def to_python_value(cls, deserialized_data, *, target_object):
+    def to_python_value(cls, deserialized_data, *, target_object=None):
         if dataclasses.is_dataclass(deserialized_data):
             data = dataclasses.asdict(deserialized_data)
         elif isinstance(deserialized_data, dict):
             data = deserialized_data.copy()
         else:
             data = {}
```

### Comparing `datafiles-2.1b5/datafiles/converters/enumerations.py` & `datafiles-2.2b1/datafiles/converters/enumerations.py`

 * *Files identical despite different names*

### Comparing `datafiles-2.1b5/datafiles/converters/extensions.py` & `datafiles-2.2b1/datafiles/converters/extensions.py`

 * *Files identical despite different names*

### Comparing `datafiles-2.1b5/datafiles/decorators.py` & `datafiles-2.2b1/datafiles/decorators.py`

 * *Files 21% similar despite different names*

```diff
@@ -1,18 +1,21 @@
 import dataclasses
 from pathlib import Path
 from typing import Callable, Dict, Optional, Union
 
+import log
+
 from .config import Meta
 from .converters import Converter
-from .model import create_model
+from .model import Model, create_model
 
 
 def datafile(
     pattern: Union[str, Callable, None] = None,
+    *,
     attrs: Optional[Dict[str, Converter]] = None,
     manual: bool = Meta.datafile_manual,
     defaults: bool = Meta.datafile_defaults,
     infer: bool = Meta.datafile_infer,
     **kwargs,
 ):
     """Synchronize a data class to the specified path."""
@@ -37,15 +40,38 @@
             defaults=defaults,
             infer=infer,
         )
 
     return decorator
 
 
+def sync(
+    instance: object,
+    pattern: str,
+    *,
+    attrs: Optional[Dict[str, Converter]] = None,
+    manual: bool = Meta.datafile_manual,
+    defaults: bool = Meta.datafile_defaults,
+    infer: bool = Meta.datafile_infer,
+):
+    """Synchronize an object to the specified path."""
+    cls = instance.__class__
+    if hasattr(instance, "datafile"):
+        pattern = cls.Meta.datafile_pattern  # type: ignore[attr-defined]
+        log.error(f"{cls} was already synchronized to {pattern!r}")
+        delattr(cls, "Meta")
+        delattr(instance, "datafile")
+    instance.__class__ = create_model(
+        cls, attrs=attrs, pattern=pattern, manual=manual, defaults=defaults, infer=infer
+    )
+    Model.__post_init__(instance)  # type: ignore[arg-type]
+
+
 def auto(filename: str, **kwargs):
+    """Map an arbitrary file to a synchronized Python object."""
     kwargs["infer"] = True
 
     path = Path.cwd() / filename
     name = path.stem.strip(".").capitalize()
 
     def auto_repr(self):
         items = (f"{k}={v!r}" for k, v in self.__dict__.items() if k != "datafile")
```

### Comparing `datafiles-2.1b5/datafiles/formats.py` & `datafiles-2.2b1/datafiles/formats.py`

 * *Files identical despite different names*

### Comparing `datafiles-2.1b5/datafiles/hooks.py` & `datafiles-2.2b1/datafiles/hooks.py`

 * *Files identical despite different names*

### Comparing `datafiles-2.1b5/datafiles/manager.py` & `datafiles-2.2b1/datafiles/manager.py`

 * *Files identical despite different names*

### Comparing `datafiles-2.1b5/datafiles/mapper.py` & `datafiles-2.2b1/datafiles/mapper.py`

 * *Files identical despite different names*

### Comparing `datafiles-2.1b5/datafiles/model.py` & `datafiles-2.2b1/datafiles/model.py`

 * *Files 6% similar despite different names*

```diff
@@ -51,29 +51,29 @@
     log.debug(f"Converting {cls} to a datafile model")
 
     if not dataclasses.is_dataclass(cls):
         raise ValueError(f"{cls} must be a dataclass")
 
     # Patch meta
 
-    m = getattr(cls, "Meta", config.Meta())
+    meta = getattr(cls, "Meta", config.Meta())
 
     if attrs is not None:
-        m.datafile_attrs = attrs
+        meta.datafile_attrs = attrs
     if pattern is not None:
-        m.datafile_pattern = pattern
+        meta.datafile_pattern = pattern
 
     if not hasattr(cls, "Meta") and manual is not None:
-        m.datafile_manual = manual
+        meta.datafile_manual = manual
     if not hasattr(cls, "Meta") and defaults is not None:
-        m.datafile_defaults = defaults
+        meta.datafile_defaults = defaults
     if not hasattr(cls, "Meta") and infer is not None:
-        m.datafile_infer = infer
+        meta.datafile_infer = infer
 
-    cls.Meta = m
+    cls.Meta = meta
 
     # Patch manager
 
     cls.objects = Manager(cls)
 
     # Patch __init__
```

### Comparing `datafiles-2.1b5/datafiles/tests/test_converters.py` & `datafiles-2.2b1/datafiles/tests/test_converters.py`

 * *Files identical despite different names*

### Comparing `datafiles-2.1b5/datafiles/tests/test_formats.py` & `datafiles-2.2b1/datafiles/tests/test_formats.py`

 * *Files identical despite different names*

### Comparing `datafiles-2.1b5/datafiles/tests/test_generics.py` & `datafiles-2.2b1/datafiles/tests/test_generics.py`

 * *Files identical despite different names*

### Comparing `datafiles-2.1b5/datafiles/tests/test_hooks.py` & `datafiles-2.2b1/datafiles/tests/test_hooks.py`

 * *Files identical despite different names*

### Comparing `datafiles-2.1b5/datafiles/tests/test_manager.py` & `datafiles-2.2b1/datafiles/tests/test_manager.py`

 * *Files identical despite different names*

### Comparing `datafiles-2.1b5/datafiles/tests/test_mapper.py` & `datafiles-2.2b1/datafiles/tests/test_mapper.py`

 * *Files identical despite different names*

### Comparing `datafiles-2.1b5/datafiles/tests/test_model.py` & `datafiles-2.2b1/datafiles/tests/test_model.py`

 * *Files identical despite different names*

### Comparing `datafiles-2.1b5/datafiles/tests/test_utils.py` & `datafiles-2.2b1/datafiles/tests/test_utils.py`

 * *Files identical despite different names*

### Comparing `datafiles-2.1b5/datafiles/types.py` & `datafiles-2.2b1/datafiles/types.py`

 * *Files identical despite different names*

### Comparing `datafiles-2.1b5/datafiles/utils.py` & `datafiles-2.2b1/datafiles/utils.py`

 * *Files identical despite different names*

### Comparing `datafiles-2.1b5/pyproject.toml` & `datafiles-2.2b1/pyproject.toml`

 * *Files 5% similar despite different names*

```diff
@@ -1,11 +1,11 @@
 [tool.poetry]
 
 name = "datafiles"
-version = "2.1b5"
+version = "2.2b1"
 description = "File-based ORM for dataclasses."
 
 license = "MIT"
 
 authors = ["Jace Browning <jacebrowning@gmail.com>"]
 
 readme = "README.md"
@@ -58,15 +58,15 @@
 [tool.poetry.dev-dependencies]
 
 # Formatters
 black = "^22.1"
 isort = "^5.10"
 
 # Linters
-mypy = "~0.991"
+mypy = "^1.3"
 pylint = "~2.15"
 pydocstyle = "*"
 
 # Testing
 pytest = "^6.2.5"
 pytest-describe = "^2.0"
 pytest-expecter = "^3.0"
@@ -78,15 +78,15 @@
 pytest-profiling = "*"
 
 # Coverage
 coveragespace = "^6.0"
 
 # Documentation
 mkdocs = "^1.4"
-pygments = "^2.10"
+pygments = "^2.15"
 
 # Notebooks
 idna = "^3.3" # papermill dependency
 ipython = "^8.10"
 jupyter = { version = "^1.0", markers = "sys_platform != 'win32'" }
 nbstripout ="~0.4"
 papermill = "^2.3"
```

### Comparing `datafiles-2.1b5/PKG-INFO` & `datafiles-2.2b1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: datafiles
-Version: 2.1b5
+Version: 2.2b1
 Summary: File-based ORM for dataclasses.
 Home-page: https://pypi.org/project/datafiles
 License: MIT
 Keywords: dataclasses,serialization,type-annotations,object-relational mapping,YAML,JSON,TOML
 Author: Jace Browning
 Author-email: jacebrowning@gmail.com
 Requires-Python: >=3.8,<4.0
@@ -36,15 +36,15 @@
 Project-URL: Repository, https://github.com/jacebrowning/datafiles
 Description-Content-Type: text/markdown
 
 # Datafiles: A file-based ORM for Python dataclasses
 
 Datafiles is a bidirectional serialization library for Python [dataclasses](https://docs.python.org/3/library/dataclasses.html) to synchronize objects to the filesystem using type annotations. It supports a variety of file formats with round-trip preservation of formatting and comments, where possible. Object changes are automatically saved to disk and only include the minimum data needed to restore each object.
 
-[![Travis CI](https://img.shields.io/travis/com/jacebrowning/datafiles/main.svg?label=unix)](https://travis-ci.com/jacebrowning/datafiles)
+[![Travis CI](https://img.shields.io/travis/com/jacebrowning/datafiles/main.svg?label=unix)](https://app.travis-ci.com/jacebrowning/datafiles)
 [![AppVeyor](https://img.shields.io/appveyor/ci/jacebrowning/datafiles/main.svg?label=windows)](https://ci.appveyor.com/project/jacebrowning/datafiles)
 [![Coveralls](https://img.shields.io/coveralls/jacebrowning/datafiles.svg)](https://coveralls.io/r/jacebrowning/datafiles)
 [![PyPI License](https://img.shields.io/pypi/l/datafiles.svg)](https://pypi.org/project/datafiles)
 [![PyPI Version](https://img.shields.io/pypi/v/datafiles.svg)](https://pypi.org/project/datafiles)
 [![PyPI Downloads](https://img.shields.io/pypi/dm/datafiles.svg?color=orange)](https://pypistats.org/packages/datafiles)
 [![Gitter](https://img.shields.io/gitter/room/jacebrowning/datafiles?color=D0164E)](https://gitter.im/jacebrowning/datafiles)
```

