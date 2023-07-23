# Comparing `tmp/multicloud_diagrams-0.3.4.tar.gz` & `tmp/multicloud_diagrams-0.3.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "multicloud_diagrams-0.3.4.tar", max compression
+gzip compressed data, was "multicloud_diagrams-0.3.5.tar", max compression
```

## Comparing `multicloud_diagrams-0.3.4.tar` & `multicloud_diagrams-0.3.5.tar`

### file list

```diff
@@ -1,10 +1,10 @@
--rw-r--r--   0        0        0     1069 2023-05-14 15:36:37.276228 multicloud_diagrams-0.3.4/LICENSE
--rw-r--r--   0        0        0     8332 2023-05-18 17:11:07.243158 multicloud_diagrams-0.3.4/README.md
--rw-r--r--   0        0        0    15466 2023-07-23 08:02:49.082002 multicloud_diagrams-0.3.4/multicloud_diagrams/__init__.py
--rw-r--r--   0        0        0     3868 2023-07-23 07:39:33.823106 multicloud_diagrams-0.3.4/multicloud_diagrams/providers/aws_services.json
--rw-r--r--   0        0        0        2 2023-05-17 19:53:33.575412 multicloud_diagrams-0.3.4/multicloud_diagrams/providers/azure_services.json
--rw-r--r--   0        0        0      207 2023-05-19 12:11:15.381235 multicloud_diagrams-0.3.4/multicloud_diagrams/providers/fallback.json
--rw-r--r--   0        0        0        2 2023-05-17 19:53:33.570337 multicloud_diagrams-0.3.4/multicloud_diagrams/providers/gcp_services.json
--rw-r--r--   0        0        0      616 2023-07-23 07:39:33.816960 multicloud_diagrams-0.3.4/multicloud_diagrams/providers/on_prem_services.json
--rw-r--r--   0        0        0      525 2023-07-23 08:07:03.845285 multicloud_diagrams-0.3.4/pyproject.toml
--rw-r--r--   0        0        0     8850 1970-01-01 00:00:00.000000 multicloud_diagrams-0.3.4/PKG-INFO
+-rw-r--r--   0        0        0     1069 2023-05-14 15:36:37.276228 multicloud_diagrams-0.3.5/LICENSE
+-rw-r--r--   0        0        0     8332 2023-05-18 17:11:07.243158 multicloud_diagrams-0.3.5/README.md
+-rw-r--r--   0        0        0    15421 2023-07-23 08:32:18.800929 multicloud_diagrams-0.3.5/multicloud_diagrams/__init__.py
+-rw-r--r--   0        0        0     3868 2023-07-23 07:39:33.823106 multicloud_diagrams-0.3.5/multicloud_diagrams/providers/aws_services.json
+-rw-r--r--   0        0        0        2 2023-05-17 19:53:33.575412 multicloud_diagrams-0.3.5/multicloud_diagrams/providers/azure_services.json
+-rw-r--r--   0        0        0      207 2023-05-19 12:11:15.381235 multicloud_diagrams-0.3.5/multicloud_diagrams/providers/fallback.json
+-rw-r--r--   0        0        0        2 2023-05-17 19:53:33.570337 multicloud_diagrams-0.3.5/multicloud_diagrams/providers/gcp_services.json
+-rw-r--r--   0        0        0      616 2023-07-23 07:39:33.816960 multicloud_diagrams-0.3.5/multicloud_diagrams/providers/on_prem_services.json
+-rw-r--r--   0        0        0      525 2023-07-23 08:34:58.510960 multicloud_diagrams-0.3.5/pyproject.toml
+-rw-r--r--   0        0        0     8850 1970-01-01 00:00:00.000000 multicloud_diagrams-0.3.5/PKG-INFO
```

### Comparing `multicloud_diagrams-0.3.4/LICENSE` & `multicloud_diagrams-0.3.5/LICENSE`

 * *Files identical despite different names*

### Comparing `multicloud_diagrams-0.3.4/README.md` & `multicloud_diagrams-0.3.5/README.md`

 * *Files identical despite different names*

### Comparing `multicloud_diagrams-0.3.4/multicloud_diagrams/__init__.py` & `multicloud_diagrams-0.3.5/multicloud_diagrams/__init__.py`

 * *Files 2% similar despite different names*

```diff
@@ -118,19 +118,19 @@
             # Position Vertex based on X,Y cords
             if f'vertex:{table_id}:row:{index}' in self.prev_coords:
                 if 'x' in self.prev_coords[f'vertex:{table_id}:row:{index}']:
                     mx_geometry.set('x', self.prev_coords[f'vertex:{table_id}:row:{index}']['x'])
                 if 'y' in self.prev_coords[f'vertex:{table_id}:row:{index}']:
                     mx_geometry.set('y', self.prev_coords[f'vertex:{table_id}:row:{index}']['y'])
 
-    def add_vertex(self, id: str, node_name: str, arn: str, metadata='', node_enum=Services):
+    def add_service(self, id: str, node_name: str, arn: str, metadata='', node_enum=Services):
         # Type checking
-        if not isinstance(node_enum, self.Services):
-            raise TypeError('direction must be an instance of Direction Enum')
-        self.add_vertex(self, id=id, node_name=node_name, arn=arn, metadata=metadata, node_type=node_enum.value)
+        if not isinstance(node_enum, Services):
+            raise TypeError('node_enum must be an instance of AWS,OnPrem Enum')
+        self.add_vertex(id, node_name, arn, metadata, node_enum.value)
 
     def add_vertex(self, id: str, node_name: str, arn: str, metadata='', node_type=''):
 
         # check that there is no such vertex already
         exist = False
         for mx_cell in self.root:
             # print(mxCell.attrib['id'])
```

### Comparing `multicloud_diagrams-0.3.4/multicloud_diagrams/providers/aws_services.json` & `multicloud_diagrams-0.3.5/multicloud_diagrams/providers/aws_services.json`

 * *Files identical despite different names*

### Comparing `multicloud_diagrams-0.3.4/multicloud_diagrams/providers/on_prem_services.json` & `multicloud_diagrams-0.3.5/multicloud_diagrams/providers/on_prem_services.json`

 * *Files identical despite different names*

### Comparing `multicloud_diagrams-0.3.4/pyproject.toml` & `multicloud_diagrams-0.3.5/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "multicloud-diagrams"
-version = "0.3.4"
+version = "0.3.5"
 description = "Library to generate DRAW.IO compatible diagrams to represent Cloud infrastructure. AWS Cloud supported."
 authors = ["Roman Tsypuk <tsypuk.conf@gmail.com>"]
 license = "MIT"
 readme = "README.md"
 packages = [{include = "multicloud_diagrams"}]
 
 [tool.poetry.dependencies]
```

### Comparing `multicloud_diagrams-0.3.4/PKG-INFO` & `multicloud_diagrams-0.3.5/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: multicloud-diagrams
-Version: 0.3.4
+Version: 0.3.5
 Summary: Library to generate DRAW.IO compatible diagrams to represent Cloud infrastructure. AWS Cloud supported.
 License: MIT
 Author: Roman Tsypuk
 Author-email: tsypuk.conf@gmail.com
 Requires-Python: >=3.10,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
```

