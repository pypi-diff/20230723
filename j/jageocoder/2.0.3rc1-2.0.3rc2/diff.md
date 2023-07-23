# Comparing `tmp/jageocoder-2.0.3rc1.tar.gz` & `tmp/jageocoder-2.0.3rc2.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "jageocoder-2.0.3rc1.tar", max compression
+gzip compressed data, was "jageocoder-2.0.3rc2.tar", max compression
```

## Comparing `jageocoder-2.0.3rc1.tar` & `jageocoder-2.0.3rc2.tar`

### file list

```diff
@@ -1,20 +1,21 @@
--rw-r--r--   0        0        0      113 2023-04-17 09:16:28.271600 jageocoder-2.0.3rc1/LICENSE
--rw-r--r--   0        0        0     8253 2023-04-29 04:07:32.527460 jageocoder-2.0.3rc1/README.md
--rw-r--r--   0        0        0     1362 2023-07-22 06:18:13.668357 jageocoder-2.0.3rc1/jageocoder/__init__.py
--rw-r--r--   0        0        0     6190 2023-07-22 07:23:49.444644 jageocoder-2.0.3rc1/jageocoder/__main__.py
--rw-r--r--   0        0        0     2574 2023-04-17 09:16:28.279600 jageocoder-2.0.3rc1/jageocoder/address.py
--rw-r--r--   0        0        0     1421 2023-07-12 05:27:45.348493 jageocoder-2.0.3rc1/jageocoder/aliases.json
--rw-r--r--   0        0        0    12147 2023-04-29 04:07:32.535460 jageocoder-2.0.3rc1/jageocoder/aza_master.py
--rw-r--r--   0        0        0     1171 2023-04-29 04:07:32.535460 jageocoder-2.0.3rc1/jageocoder/dataset.py
--rw-r--r--   0        0        0      691 2023-04-17 09:16:28.279600 jageocoder-2.0.3rc1/jageocoder/exceptions.py
--rw-r--r--   0        0        0    18862 2023-04-22 02:31:05.987235 jageocoder-2.0.3rc1/jageocoder/itaiji.py
--rw-r--r--   0        0        0    14220 2023-04-17 09:16:28.279600 jageocoder-2.0.3rc1/jageocoder/itaiji_dic.json
--rw-r--r--   0        0        0    11408 2023-07-22 07:19:14.984430 jageocoder-2.0.3rc1/jageocoder/module.py
--rw-r--r--   0        0        0    37985 2023-07-22 06:18:13.668357 jageocoder-2.0.3rc1/jageocoder/node.py
--rw-r--r--   0        0        0     2631 2023-04-29 04:07:32.535460 jageocoder-2.0.3rc1/jageocoder/result.py
--rw-r--r--   0        0        0    15253 2023-07-22 06:18:13.668357 jageocoder-2.0.3rc1/jageocoder/rtree.py
--rw-r--r--   0        0        0     7854 2023-04-17 09:16:28.283600 jageocoder-2.0.3rc1/jageocoder/strlib.py
--rw-r--r--   0        0        0    49426 2023-07-22 07:18:17.917448 jageocoder-2.0.3rc1/jageocoder/tree.py
--rw-r--r--   0        0        0     4995 2023-04-29 04:07:32.535460 jageocoder-2.0.3rc1/jageocoder/trie.py
--rw-r--r--   0        0        0     1228 2023-07-22 06:18:13.668357 jageocoder-2.0.3rc1/pyproject.toml
--rw-r--r--   0        0        0     9687 1970-01-01 00:00:00.000000 jageocoder-2.0.3rc1/PKG-INFO
+-rw-r--r--   0        0        0      113 2023-04-28 00:22:42.161103 jageocoder-2.0.3rc2/LICENSE
+-rw-r--r--   0        0        0     8253 2023-04-28 00:22:42.161103 jageocoder-2.0.3rc2/README.md
+-rw-r--r--   0        0        0     1362 2023-07-23 10:45:40.589103 jageocoder-2.0.3rc2/jageocoder/__init__.py
+-rw-r--r--   0        0        0     6193 2023-07-23 04:58:59.814931 jageocoder-2.0.3rc2/jageocoder/__main__.py
+-rw-r--r--   0        0        0     2574 2023-04-28 00:22:42.171103 jageocoder-2.0.3rc2/jageocoder/address.py
+-rw-r--r--   0        0        0     1421 2023-04-29 00:08:12.436781 jageocoder-2.0.3rc2/jageocoder/aliases.json
+-rw-r--r--   0        0        0    12147 2023-04-28 00:22:42.171103 jageocoder-2.0.3rc2/jageocoder/aza_master.py
+-rw-r--r--   0        0        0     1171 2023-04-28 00:22:42.171103 jageocoder-2.0.3rc2/jageocoder/dataset.py
+-rw-r--r--   0        0        0      691 2023-04-28 00:22:42.171103 jageocoder-2.0.3rc2/jageocoder/exceptions.py
+-rw-r--r--   0        0        0    18862 2023-04-28 00:22:42.171103 jageocoder-2.0.3rc2/jageocoder/itaiji.py
+-rw-r--r--   0        0        0    14220 2023-04-28 00:22:42.171103 jageocoder-2.0.3rc2/jageocoder/itaiji_dic.json
+-rw-r--r--   0        0        0    11408 2023-07-22 13:08:25.405688 jageocoder-2.0.3rc2/jageocoder/module.py
+-rw-r--r--   0        0        0    38165 2023-07-23 10:57:07.408934 jageocoder-2.0.3rc2/jageocoder/node.py
+-rw-r--r--   0        0        0     2631 2023-04-28 00:22:42.171103 jageocoder-2.0.3rc2/jageocoder/result.py
+-rw-r--r--   0        0        0    15253 2023-07-22 13:08:25.405688 jageocoder-2.0.3rc2/jageocoder/rtree.py
+-rw-r--r--   0        0        0     7854 2023-04-28 00:22:42.171103 jageocoder-2.0.3rc2/jageocoder/strlib.py
+-rw-r--r--   0        0        0    49530 2023-07-23 05:26:27.524522 jageocoder-2.0.3rc2/jageocoder/tree.py
+-rw-r--r--   0        0        0     4995 2023-04-28 00:22:42.171103 jageocoder-2.0.3rc2/jageocoder/trie.py
+-rw-r--r--   0        0        0     1228 2023-07-23 10:45:45.909102 jageocoder-2.0.3rc2/pyproject.toml
+-rw-r--r--   0        0        0     9750 1970-01-01 00:00:00.000000 jageocoder-2.0.3rc2/setup.py
+-rw-r--r--   0        0        0     9687 1970-01-01 00:00:00.000000 jageocoder-2.0.3rc2/PKG-INFO
```

### Comparing `jageocoder-2.0.3rc1/README.md` & `jageocoder-2.0.3rc2/README.md`

 * *Files identical despite different names*

### Comparing `jageocoder-2.0.3rc1/jageocoder/__init__.py` & `jageocoder-2.0.3rc2/jageocoder/__init__.py`

 * *Files 1% similar despite different names*

```diff
@@ -15,15 +15,15 @@
 running the following steps.
 
     >>> import jageocoder
     >>> jageocoder.init()
     >>> jageocoder.searchNode('<Japanese-address>')
 """
 
-__version__ = '2.0.3rc1'  # The package version
+__version__ = '2.0.3rc2'  # The package version
 __dictionary_version__ = '20230405'  # Compatible dictionary version
 __author__ = 'Takeshi Sagara <sagara@info-proto.com>'
 
 __all__ = [
     'init',
     'free',
     'is_initialized',
```

### Comparing `jageocoder-2.0.3rc1/jageocoder/__main__.py` & `jageocoder-2.0.3rc2/jageocoder/__main__.py`

 * *Files 1% similar despite different names*

```diff
@@ -156,15 +156,15 @@
 
     elif args['install-dictionary']:
         path = args['<path>']
         try:
             jageocoder.install_dictionary(
                 path=path,
                 db_dir=args['--db-dir'],
-                skip_confirmation=(args['-y'] is True),
+                skip_confirmation=(args['--yes'] is True),
             )
         except JageocoderError:
             logging.warning((
                 "辞書データファイルが '{}' にありません。".format(path)
             ))
             exit(1)
```

### Comparing `jageocoder-2.0.3rc1/jageocoder/address.py` & `jageocoder-2.0.3rc2/jageocoder/address.py`

 * *Files identical despite different names*

### Comparing `jageocoder-2.0.3rc1/jageocoder/aliases.json` & `jageocoder-2.0.3rc2/jageocoder/aliases.json`

 * *Files identical despite different names*

### Comparing `jageocoder-2.0.3rc1/jageocoder/aza_master.py` & `jageocoder-2.0.3rc2/jageocoder/aza_master.py`

 * *Files identical despite different names*

### Comparing `jageocoder-2.0.3rc1/jageocoder/dataset.py` & `jageocoder-2.0.3rc2/jageocoder/dataset.py`

 * *Files identical despite different names*

### Comparing `jageocoder-2.0.3rc1/jageocoder/exceptions.py` & `jageocoder-2.0.3rc2/jageocoder/exceptions.py`

 * *Files identical despite different names*

### Comparing `jageocoder-2.0.3rc1/jageocoder/itaiji.py` & `jageocoder-2.0.3rc2/jageocoder/itaiji.py`

 * *Files identical despite different names*

### Comparing `jageocoder-2.0.3rc1/jageocoder/itaiji_dic.json` & `jageocoder-2.0.3rc2/jageocoder/itaiji_dic.json`

 * *Files identical despite different names*

### Comparing `jageocoder-2.0.3rc1/jageocoder/module.py` & `jageocoder-2.0.3rc2/jageocoder/module.py`

 * *Files identical despite different names*

### Comparing `jageocoder-2.0.3rc1/jageocoder/node.py` & `jageocoder-2.0.3rc2/jageocoder/node.py`

 * *Files 1% similar despite different names*

```diff
@@ -1,8 +1,9 @@
 from __future__ import annotations
+from collections.abc import Iterator
 import copy
 from functools import lru_cache
 import json
 import logging
 import os
 import re
 from typing import List, Optional, TYPE_CHECKING
@@ -275,42 +276,48 @@
 
         return None
 
     @property
     def children(self) -> List[AddressNode]:
         return self.get_children()
 
-    def get_children(self) -> List[AddressNode]:
+    def iter_children(self) -> Iterator[AddressNode]:
         """
-        Get all children of the node.
+        Iterate children of the node.
 
         Returns
         -------
-        List[AddressNode]
+        Iterator[AddressNode]
         """
-        children = []
         pos: int = self.id + 1
         while pos < self.sibling_id:
             node = self.table.get_record(pos=pos)
             if node.parent_id == self.id:
-                children.append(node)
+                yield node
                 pos = node.sibling_id
             else:
                 parent = self.table.get_record(pos=node.parent_id)
                 pos = parent.sibling_id
 
-        return children
+    def get_children(self) -> List[AddressNode]:
+        """
+        Get all children of the node.
+
+        Returns
+        -------
+        List[AddressNode]
+        """
+        return list(self.iter_children())
 
     def add_dummy_coordinates(self) -> AddressNode:
         """
         Add dummy coordinate values to the node.
         """
-        children = self.children
         new_node = copy.copy(self)
-        for child in children:
+        for child in self.iter_children():
             if child.y <= 90.0:
                 new_node.x, new_node.y = child.x, child.y
                 logger.debug((
                     "Node {}({}) has no coordinates. "
                     "Use the coordinates of the child {}({}) instead."
                 ).format(
                     self.name, self.id, child.name, child.id))
```

### Comparing `jageocoder-2.0.3rc1/jageocoder/result.py` & `jageocoder-2.0.3rc2/jageocoder/result.py`

 * *Files identical despite different names*

### Comparing `jageocoder-2.0.3rc1/jageocoder/rtree.py` & `jageocoder-2.0.3rc2/jageocoder/rtree.py`

 * *Files identical despite different names*

### Comparing `jageocoder-2.0.3rc1/jageocoder/strlib.py` & `jageocoder-2.0.3rc2/jageocoder/strlib.py`

 * *Files identical despite different names*

### Comparing `jageocoder-2.0.3rc1/jageocoder/tree.py` & `jageocoder-2.0.3rc2/jageocoder/tree.py`

 * *Files 0% similar despite different names*

```diff
@@ -1352,16 +1352,18 @@
                 matched = matched_substring[v[1]]
             else:
                 matched = self._get_matched_substring(query, v)
                 matched_substring[v[1]] = matched
 
             results.append(Result(v[0], matched))
 
-        # Sort the results in acending order by node.priority.
-        results.sort(key=lambda r: r.node.priority)
+        # Sort the result list in descending order of the length of the match
+        # and ascending order of the node priority.
+        results.sort(
+            key=lambda r: len(r.matched) * -100 + r.node.priority)
 
         return results
 
     def _get_matched_substring(
             self, query: str,
             retrieved: list) -> str:
         """
```

### Comparing `jageocoder-2.0.3rc1/jageocoder/trie.py` & `jageocoder-2.0.3rc2/jageocoder/trie.py`

 * *Files identical despite different names*

### Comparing `jageocoder-2.0.3rc1/pyproject.toml` & `jageocoder-2.0.3rc2/pyproject.toml`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "jageocoder"
-version = "2.0.3rc1"
+version = "2.0.3rc2"
 description = "A Japanese-address geocoder for Python."
 authors = ["Takeshi Sagara <sagara@info-proto.com>"]
 repository = "https://github.com/t-sagara/jageocoder/"
 license = "The MIT License"
 readme = "README.md"
 documentation = "https://jageocoder.readthedocs.io/"
 packages = [
```

### Comparing `jageocoder-2.0.3rc1/PKG-INFO` & `jageocoder-2.0.3rc2/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: jageocoder
-Version: 2.0.3rc1
+Version: 2.0.3rc2
 Summary: A Japanese-address geocoder for Python.
 Home-page: https://github.com/t-sagara/jageocoder/
 License: The MIT License
 Author: Takeshi Sagara
 Author-email: sagara@info-proto.com
 Requires-Python: >=3.7,<4.0
 Classifier: License :: OSI Approved :: MIT License
```

