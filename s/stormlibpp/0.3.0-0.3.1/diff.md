# Comparing `tmp/stormlibpp-0.3.0.tar.gz` & `tmp/stormlibpp-0.3.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "stormlibpp-0.3.0.tar", last modified: Sun Jun 25 23:08:19 2023, max compression
+gzip compressed data, was "stormlibpp-0.3.1.tar", last modified: Sun Jul 23 20:02:49 2023, max compression
```

## Comparing `stormlibpp-0.3.0.tar` & `stormlibpp-0.3.1.tar`

### file list

```diff
@@ -1,25 +1,25 @@
-drwxr-xr-x   0 gormo      (501) staff       (20)        0 2023-06-25 23:08:19.813611 stormlibpp-0.3.0/
--rw-r--r--   0 gormo      (501) staff       (20)     1067 2023-06-24 17:20:21.000000 stormlibpp-0.3.0/LICENSE
--rw-r--r--   0 gormo      (501) staff       (20)     1665 2023-06-25 23:08:19.813482 stormlibpp-0.3.0/PKG-INFO
--rw-r--r--   0 gormo      (501) staff       (20)      108 2023-06-24 18:31:15.000000 stormlibpp-0.3.0/README.md
--rw-r--r--   0 gormo      (501) staff       (20)      557 2023-06-25 23:08:15.000000 stormlibpp-0.3.0/pyproject.toml
--rw-r--r--   0 gormo      (501) staff       (20)       38 2023-06-25 23:08:19.813652 stormlibpp-0.3.0/setup.cfg
-drwxr-xr-x   0 gormo      (501) staff       (20)        0 2023-06-25 23:08:19.810546 stormlibpp-0.3.0/src/
-drwxr-xr-x   0 gormo      (501) staff       (20)        0 2023-06-25 23:08:19.811705 stormlibpp-0.3.0/src/stormlibpp/
--rw-r--r--   0 gormo      (501) staff       (20)     1447 2023-06-25 23:08:15.000000 stormlibpp-0.3.0/src/stormlibpp/__init__.py
--rw-r--r--   0 gormo      (501) staff       (20)      663 2023-06-25 16:40:51.000000 stormlibpp-0.3.0/src/stormlibpp/errors.py
--rw-r--r--   0 gormo      (501) staff       (20)     5371 2023-06-25 22:22:23.000000 stormlibpp-0.3.0/src/stormlibpp/node.py
--rw-r--r--   0 gormo      (501) staff       (20)     9151 2023-06-25 18:55:59.000000 stormlibpp-0.3.0/src/stormlibpp/stormpkg.py
--rw-r--r--   0 gormo      (501) staff       (20)     1396 2023-06-25 16:42:23.000000 stormlibpp-0.3.0/src/stormlibpp/telepath.py
--rw-r--r--   0 gormo      (501) staff       (20)     1507 2023-06-25 18:55:59.000000 stormlibpp-0.3.0/src/stormlibpp/utils.py
-drwxr-xr-x   0 gormo      (501) staff       (20)        0 2023-06-25 23:08:19.812645 stormlibpp-0.3.0/src/stormlibpp.egg-info/
--rw-r--r--   0 gormo      (501) staff       (20)     1665 2023-06-25 23:08:19.000000 stormlibpp-0.3.0/src/stormlibpp.egg-info/PKG-INFO
--rw-r--r--   0 gormo      (501) staff       (20)      459 2023-06-25 23:08:19.000000 stormlibpp-0.3.0/src/stormlibpp.egg-info/SOURCES.txt
--rw-r--r--   0 gormo      (501) staff       (20)        1 2023-06-25 23:08:19.000000 stormlibpp-0.3.0/src/stormlibpp.egg-info/dependency_links.txt
--rw-r--r--   0 gormo      (501) staff       (20)       17 2023-06-25 23:08:19.000000 stormlibpp-0.3.0/src/stormlibpp.egg-info/requires.txt
--rw-r--r--   0 gormo      (501) staff       (20)       11 2023-06-25 23:08:19.000000 stormlibpp-0.3.0/src/stormlibpp.egg-info/top_level.txt
-drwxr-xr-x   0 gormo      (501) staff       (20)        0 2023-06-25 23:08:19.813294 stormlibpp-0.3.0/tests/
--rw-r--r--   0 gormo      (501) staff       (20)     1438 2023-06-25 22:24:01.000000 stormlibpp-0.3.0/tests/test_node.py
--rw-r--r--   0 gormo      (501) staff       (20)     1699 2023-06-25 18:55:59.000000 stormlibpp-0.3.0/tests/test_stormpkg.py
--rw-r--r--   0 gormo      (501) staff       (20)      720 2023-06-25 16:42:23.000000 stormlibpp-0.3.0/tests/test_telepath.py
--rw-r--r--   0 gormo      (501) staff       (20)      419 2023-06-24 18:31:15.000000 stormlibpp-0.3.0/tests/test_utils.py
+drwxr-xr-x   0 gormo      (501) staff       (20)        0 2023-07-23 20:02:49.882322 stormlibpp-0.3.1/
+-rw-r--r--   0 gormo      (501) staff       (20)     1067 2023-06-24 17:20:21.000000 stormlibpp-0.3.1/LICENSE
+-rw-r--r--   0 gormo      (501) staff       (20)     1665 2023-07-23 20:02:49.882139 stormlibpp-0.3.1/PKG-INFO
+-rw-r--r--   0 gormo      (501) staff       (20)      108 2023-06-24 18:31:15.000000 stormlibpp-0.3.1/README.md
+-rw-r--r--   0 gormo      (501) staff       (20)      557 2023-07-23 20:02:45.000000 stormlibpp-0.3.1/pyproject.toml
+-rw-r--r--   0 gormo      (501) staff       (20)       38 2023-07-23 20:02:49.882378 stormlibpp-0.3.1/setup.cfg
+drwxr-xr-x   0 gormo      (501) staff       (20)        0 2023-07-23 20:02:49.878796 stormlibpp-0.3.1/src/
+drwxr-xr-x   0 gormo      (501) staff       (20)        0 2023-07-23 20:02:49.880145 stormlibpp-0.3.1/src/stormlibpp/
+-rw-r--r--   0 gormo      (501) staff       (20)     1531 2023-07-23 20:02:45.000000 stormlibpp-0.3.1/src/stormlibpp/__init__.py
+-rw-r--r--   0 gormo      (501) staff       (20)      663 2023-06-25 16:40:51.000000 stormlibpp-0.3.1/src/stormlibpp/errors.py
+-rw-r--r--   0 gormo      (501) staff       (20)     5501 2023-07-23 19:49:57.000000 stormlibpp-0.3.1/src/stormlibpp/node.py
+-rw-r--r--   0 gormo      (501) staff       (20)     9365 2023-07-23 19:56:09.000000 stormlibpp-0.3.1/src/stormlibpp/stormpkg.py
+-rw-r--r--   0 gormo      (501) staff       (20)     1705 2023-07-23 19:40:23.000000 stormlibpp-0.3.1/src/stormlibpp/telepath.py
+-rw-r--r--   0 gormo      (501) staff       (20)     1628 2023-07-23 19:57:59.000000 stormlibpp-0.3.1/src/stormlibpp/utils.py
+drwxr-xr-x   0 gormo      (501) staff       (20)        0 2023-07-23 20:02:49.880892 stormlibpp-0.3.1/src/stormlibpp.egg-info/
+-rw-r--r--   0 gormo      (501) staff       (20)     1665 2023-07-23 20:02:49.000000 stormlibpp-0.3.1/src/stormlibpp.egg-info/PKG-INFO
+-rw-r--r--   0 gormo      (501) staff       (20)      459 2023-07-23 20:02:49.000000 stormlibpp-0.3.1/src/stormlibpp.egg-info/SOURCES.txt
+-rw-r--r--   0 gormo      (501) staff       (20)        1 2023-07-23 20:02:49.000000 stormlibpp-0.3.1/src/stormlibpp.egg-info/dependency_links.txt
+-rw-r--r--   0 gormo      (501) staff       (20)       17 2023-07-23 20:02:49.000000 stormlibpp-0.3.1/src/stormlibpp.egg-info/requires.txt
+-rw-r--r--   0 gormo      (501) staff       (20)       11 2023-07-23 20:02:49.000000 stormlibpp-0.3.1/src/stormlibpp.egg-info/top_level.txt
+drwxr-xr-x   0 gormo      (501) staff       (20)        0 2023-07-23 20:02:49.881758 stormlibpp-0.3.1/tests/
+-rw-r--r--   0 gormo      (501) staff       (20)     3747 2023-07-23 19:36:12.000000 stormlibpp-0.3.1/tests/test_node.py
+-rw-r--r--   0 gormo      (501) staff       (20)     1699 2023-06-25 18:55:59.000000 stormlibpp-0.3.1/tests/test_stormpkg.py
+-rw-r--r--   0 gormo      (501) staff       (20)      720 2023-06-25 16:42:23.000000 stormlibpp-0.3.1/tests/test_telepath.py
+-rw-r--r--   0 gormo      (501) staff       (20)      419 2023-06-24 18:31:15.000000 stormlibpp-0.3.1/tests/test_utils.py
```

### Comparing `stormlibpp-0.3.0/LICENSE` & `stormlibpp-0.3.1/LICENSE`

 * *Files identical despite different names*

### Comparing `stormlibpp-0.3.0/PKG-INFO` & `stormlibpp-0.3.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: stormlibpp
-Version: 0.3.0
+Version: 0.3.1
 Summary: The stormlibpp Python package
 Author: John Gorman
 License: MIT License
         
         Copyright (c) 2023 John Gorman
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
```

### Comparing `stormlibpp-0.3.0/pyproject.toml` & `stormlibpp-0.3.1/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,14 +1,14 @@
 [build-system]
 requires = ["setuptools"]
 build-backend = "setuptools.build_meta"
 
 [project]
 name = "stormlibpp"
-version = "0.3.0"
+version = "0.3.1"
 description = "The stormlibpp Python package"
 readme = "README.md"
 requires-python = ">=3.11"
 
 # Fill in dependencies here.
 dependencies = [
     "synapse==2.139.0"
```

### Comparing `stormlibpp-0.3.0/src/stormlibpp/__init__.py` & `stormlibpp-0.3.1/src/stormlibpp/__init__.py`

 * *Files 5% similar despite different names*

```diff
@@ -25,14 +25,15 @@
   It currently contains mostly classes for describing standard Telepath API
   return values.
 
 - ``stormpkg`` defines the ``StormPkg`` class.
 
 """
 
-__version__ = "0.3.0"
+__version__ = "0.3.1"
 
+# TODO - Do we want to change this to only import submods, or do we even need that?
 from . import errors
 from . import utils
 from .node import StormNode
 from .stormpkg import StormPkg
 from .telepath import (genDefaultTelepathRetn, TelepathRetn)
```

### Comparing `stormlibpp-0.3.0/src/stormlibpp/errors.py` & `stormlibpp-0.3.1/src/stormlibpp/errors.py`

 * *Files identical despite different names*

### Comparing `stormlibpp-0.3.0/src/stormlibpp/node.py` & `stormlibpp-0.3.1/src/stormlibpp/node.py`

 * *Files 9% similar despite different names*

```diff
@@ -1,12 +1,12 @@
 """Work with storm:node objects in Python."""
 
 
 from types import SimpleNamespace
-from typing import Any, Self, TypedDict
+from typing import Any, TypedDict
 
 
 NodeForm = str
 """A valid syn:form value."""
 
 
 class NodeVals(TypedDict):
@@ -44,19 +44,22 @@
 
     Supports checking if an item is "held" via the ``in`` operator.
 
     Supports iteration of items in the SimpleNamespace. Each iteration returns
     a tuple of the item name followed by the item value.
 
     Implements only magic methods, and all of them operate on the underlying
-    SimpleNamespace. To convert this object to a ``dict`` of the items it holds,
+    SimpleNamespace.
+    
+    To convert this object to a ``dict`` of the items it holds,
     call ``vars`` on an instance.
     """
 
     def __init__(self, /, **kwargs) -> None:
+        # TODO - Is SimpleNamespace really the best option for this?
         self.__ns = SimpleNamespace(**kwargs)
     
     def __contains__(self, __name: str) -> bool:
         return __name in dir(self)
 
     @property
     def __dict__(self):
@@ -83,23 +86,22 @@
     """Properties of a StormNode."""
 
 
 class Tags(ItemContainer):
     """Tags of a StormNode."""
 
 
-
 class StormNode:
     """A storm:node Storm object that is in a Python runtime.
 
     It supports "unpacking" the node into this object, edits to the object, and
     repacking of the node to be sent back to Storm.
 
     This node can be created purely from Python code rather than a packed
-    ``storm:node`` object. Use the ``__init__`` directly instead of ``unpack``.
+    ``storm:node`` object. Use ``__init__`` directly instead of ``unpack``.
     This allows the creation of a new node in Python that can be passed back to
     Storm.
 
     The intent is to represent an object that can be read from and written back
     to a Cortex. It isn't meant to provide the same API that a ``storm:node``
     has in Storm.
     """
@@ -116,45 +118,45 @@
         tagprops: dict = {},
         **kwargs,
     ) -> None:
 
         self._form = form
         self._value = value
 
-        self._tags = Props(**tags)
-        self._props = Tags(**props)
+        self._tags = Tags(**tags)
+        self._props = Props(**props)
 
         self.iden = iden
         self.nodedata = nodedata
         self.tagprops = tagprops
 
         # Not really sure if this is needed, but saving it for now.
         self._xtras = kwargs
 
     @property
     def form(self) -> str:
-        """The form of this Node."""
+        """The form of this StormNode."""
 
         return self._form
 
     @property
     def value(self) -> str:
-        """The value of this Node."""
+        """The value of this StormNode."""
 
         return self._value
 
     @property
     def tags(self):
-        """The tags of this Node."""
+        """The tags of this StormNode."""
 
         return self._tags
 
     @property
     def props(self):
-        """The properties of this Node."""
+        """The properties of this StormNode."""
 
         return self._props
 
     @property
     def nodevals(self):
         """The NodeVals dict this Node would have in a NodeTuple."""
 
@@ -163,26 +165,27 @@
             tagprops=self.tagprops,
             nodedata=self.nodedata,
             props=vars(self.props),
             tags=vars(self.tags),
         )
 
     @classmethod
-    def unpack(cls, packedtup: NodeTuple) -> Self:
+    def unpack(cls, packedtup: NodeTuple) -> 'StormNode':
         form, name = packedtup[0]
         vals = NodeVals(**packedtup[1])
         return cls(
             form,
             name,
             **vals
         )
 
     def pack(self) -> NodeTuple:
         return ((self.form, self.value), self.nodevals)
 
+    # TODO - Support tag properties
     def addTag(self, tag, timestamps: tuple = (None, None)) -> None:
         if tag in self._tags and timestamps != (None, None) and self._tags[tag] != timestamps:
             self._tags[tag] = timestamps
         elif tag not in self._tags:
             self._tags[tag] = timestamps
 
     def addTags(self, tags, timestamps: tuple = (None, None)) -> None:
```

### Comparing `stormlibpp-0.3.0/src/stormlibpp/stormpkg.py` & `stormlibpp-0.3.1/src/stormlibpp/stormpkg.py`

 * *Files 2% similar despite different names*

```diff
@@ -128,14 +128,15 @@
                 raise errors.StormPkgResolveError(
                     "Unable to automatically resolve the package proto's directory. "
                     "Try passing proto_dir."
                 ) from err
 
             self.proto_dir = utils.absjoin(
                 os.path.dirname(resolved_path),
+                # TODO - Make this configurable
                 "pkgproto",
             )
 
         self.proto = os.path.join(
             self.proto_dir,
             f"{self.proto_name}.yaml",
         )
@@ -209,14 +210,17 @@
         """The full definitions of the modules this package defines."""
 
         return self.pkgdef.get("modules", [])
 
     def storm(self) -> dict[str, str]:
         """The Storm code this package defines.
 
+        Iterates over the dicts from ``cmds()`` + ``mods()`` to map all names
+        to the Storm code each dict defines in the ``storm`` key.
+
         Returns
         -------
         dict[str, str]
             Keys are the module/command name and values are the Storm code.
         """
 
         storm = {}
@@ -234,23 +238,23 @@
     @property
     def modnames(self) -> list[str]:
         """The names of the modules this package defines, if any."""
 
         return [mod.get("name") for mod in self.mods() if "name" in mod]
 
     @property
-    def pkg_guid(self) -> str:
+    def pkg_guid(self) -> str | None:
         """The package's guid, None if not set."""
 
         return self.pkgdef.get("guid")
 
     @property
-    def pkg_name(self) -> str:
+    def pkg_name(self) -> str | None:
         """The package's name, None if not set."""
 
         return self.pkgdef.get("name")
 
     @property
-    def pkg_ver(self) -> str:
+    def pkg_ver(self) -> str | None:
         """The package's version, None if not set."""
 
         return self.pkgdef.get("version")
```

### Comparing `stormlibpp-0.3.0/src/stormlibpp/utils.py` & `stormlibpp-0.3.1/src/stormlibpp/utils.py`

 * *Files 2% similar despite different names*

```diff
@@ -34,14 +34,16 @@
     StormSyntaxError
         If a Storm syntax error was found in the given Storm code.
     """
 
     try:
         s_parser.parseQuery(storm)
     except s_exc.BadSyntax as err:
+        # TODO - Make sure this gives the caller verbose error info
+        # and add it to the StormSyntaxError if not.
         raise errors.StormSyntaxError() from err
 
 
 def normver(ver: str | tuple) -> tuple[str, tuple]:
     """Take either a version str "x.x.x" or tuple (x, x, x) and return both.
 
     Raises
```

### Comparing `stormlibpp-0.3.0/src/stormlibpp.egg-info/PKG-INFO` & `stormlibpp-0.3.1/src/stormlibpp.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: stormlibpp
-Version: 0.3.0
+Version: 0.3.1
 Summary: The stormlibpp Python package
 Author: John Gorman
 License: MIT License
         
         Copyright (c) 2023 John Gorman
         
         Permission is hereby granted, free of charge, to any person obtaining a copy
```

### Comparing `stormlibpp-0.3.0/tests/test_stormpkg.py` & `stormlibpp-0.3.1/tests/test_stormpkg.py`

 * *Files identical despite different names*

### Comparing `stormlibpp-0.3.0/tests/test_telepath.py` & `stormlibpp-0.3.1/tests/test_telepath.py`

 * *Files identical despite different names*

