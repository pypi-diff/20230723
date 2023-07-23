# Comparing `tmp/multicloud_diagrams-0.3.5.tar.gz` & `tmp/multicloud_diagrams-0.3.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "multicloud_diagrams-0.3.5.tar", max compression
+gzip compressed data, was "multicloud_diagrams-0.3.6.tar", max compression
```

## Comparing `multicloud_diagrams-0.3.5.tar` & `multicloud_diagrams-0.3.6.tar`

### file list

```diff
@@ -1,10 +1,10 @@
--rw-r--r--   0        0        0     1069 2023-05-14 15:36:37.276228 multicloud_diagrams-0.3.5/LICENSE
--rw-r--r--   0        0        0     8332 2023-05-18 17:11:07.243158 multicloud_diagrams-0.3.5/README.md
--rw-r--r--   0        0        0    15421 2023-07-23 08:32:18.800929 multicloud_diagrams-0.3.5/multicloud_diagrams/__init__.py
--rw-r--r--   0        0        0     3868 2023-07-23 07:39:33.823106 multicloud_diagrams-0.3.5/multicloud_diagrams/providers/aws_services.json
--rw-r--r--   0        0        0        2 2023-05-17 19:53:33.575412 multicloud_diagrams-0.3.5/multicloud_diagrams/providers/azure_services.json
--rw-r--r--   0        0        0      207 2023-05-19 12:11:15.381235 multicloud_diagrams-0.3.5/multicloud_diagrams/providers/fallback.json
--rw-r--r--   0        0        0        2 2023-05-17 19:53:33.570337 multicloud_diagrams-0.3.5/multicloud_diagrams/providers/gcp_services.json
--rw-r--r--   0        0        0      616 2023-07-23 07:39:33.816960 multicloud_diagrams-0.3.5/multicloud_diagrams/providers/on_prem_services.json
--rw-r--r--   0        0        0      525 2023-07-23 08:34:58.510960 multicloud_diagrams-0.3.5/pyproject.toml
--rw-r--r--   0        0        0     8850 1970-01-01 00:00:00.000000 multicloud_diagrams-0.3.5/PKG-INFO
+-rw-r--r--   0        0        0     1069 2023-05-14 15:36:37.276228 multicloud_diagrams-0.3.6/LICENSE
+-rw-r--r--   0        0        0     8567 2023-07-23 08:37:02.246004 multicloud_diagrams-0.3.6/README.md
+-rw-r--r--   0        0        0    16720 2023-07-23 16:29:00.842637 multicloud_diagrams-0.3.6/multicloud_diagrams/__init__.py
+-rw-r--r--   0        0        0     3868 2023-07-23 07:39:33.823106 multicloud_diagrams-0.3.6/multicloud_diagrams/providers/aws_services.json
+-rw-r--r--   0        0        0        2 2023-05-17 19:53:33.575412 multicloud_diagrams-0.3.6/multicloud_diagrams/providers/azure_services.json
+-rw-r--r--   0        0        0      207 2023-05-19 12:11:15.381235 multicloud_diagrams-0.3.6/multicloud_diagrams/providers/fallback.json
+-rw-r--r--   0        0        0        2 2023-05-17 19:53:33.570337 multicloud_diagrams-0.3.6/multicloud_diagrams/providers/gcp_services.json
+-rw-r--r--   0        0        0      616 2023-07-23 07:39:33.816960 multicloud_diagrams-0.3.6/multicloud_diagrams/providers/on_prem_services.json
+-rw-r--r--   0        0        0      525 2023-07-23 16:31:32.538368 multicloud_diagrams-0.3.6/pyproject.toml
+-rw-r--r--   0        0        0     9085 1970-01-01 00:00:00.000000 multicloud_diagrams-0.3.6/PKG-INFO
```

### Comparing `multicloud_diagrams-0.3.5/LICENSE` & `multicloud_diagrams-0.3.6/LICENSE`

 * *Files identical despite different names*

### Comparing `multicloud_diagrams-0.3.5/README.md` & `multicloud_diagrams-0.3.6/README.md`

 * *Files 3% similar despite different names*

```diff
@@ -183,11 +183,21 @@
     link_type: none }
 ```
 - Source [aws_iam_from_yaml.py](https://github.com/tsypuk/multicloud-diagrams/blob/main/samples/samples/aws_iam_from_yaml.py)
 - Output compiled [output.prod.iam-roles-from-yaml.drawio](https://raw.githubusercontent.com/tsypuk/multicloud-diagrams/main/samples/output/output.prod.iam-roles-from-yaml.drawio)
 
 - ![output.prod.iam-roles.png](https://github.com/tsypuk/multicloud-diagrams/blob/main/samples/output/png/output.prod.iam-roles-from-yaml.png?raw=True)
 
+```shell
+poetry build
+export PYPI_USERNAME=
+export PYPI_PASSWORD=
+poetry publish --build --username $PYPI_USERNAME --password $PYPI_PASSWORD
+
+cd samples/samples
+poetry install
+poetry run python aws_iam_roles_from_code_with_enum.py
+```
 
 ### FYI:
 
 OpenSource Guide, [How to contribute to opensource](https://opensource.guide/)
```

### Comparing `multicloud_diagrams-0.3.5/multicloud_diagrams/__init__.py` & `multicloud_diagrams-0.3.6/multicloud_diagrams/__init__.py`

 * *Files 7% similar despite different names*

```diff
@@ -97,14 +97,19 @@
 
         # Position Vertex based on X,Y cords
         if f'vertex:{table_id}:list' in self.prev_coords:
             if 'x' in self.prev_coords[f'vertex:{table_id}:list']:
                 mx_geometry.set('x', self.prev_coords[f'vertex:{table_id}:list']['x'])
             if 'y' in self.prev_coords[f'vertex:{table_id}:list']:
                 mx_geometry.set('y', self.prev_coords[f'vertex:{table_id}:list']['y'])
+            if 'height' in self.prev_coords[f'vertex:{table_id}:list']:
+                mx_geometry.set('height', self.prev_coords[f'vertex:{table_id}:list']['height'])
+            if 'width' in self.prev_coords[f'vertex:{table_id}:list']:
+                mx_geometry.set('width', self.prev_coords[f'vertex:{table_id}:list']['width'])
+
 
         for index, item in enumerate(rows):
             mx_cell = et.SubElement(self.root,
                                     'mxCell',
                                     id=f'vertex:{table_id}:row:{index}',
                                     value=item,
                                     style=("text;strokeColor=none;fillColor=none;align=left;verticalAlign=middle;"
@@ -117,14 +122,18 @@
             mx_geometry.set('as', 'geometry')
             # Position Vertex based on X,Y cords
             if f'vertex:{table_id}:row:{index}' in self.prev_coords:
                 if 'x' in self.prev_coords[f'vertex:{table_id}:row:{index}']:
                     mx_geometry.set('x', self.prev_coords[f'vertex:{table_id}:row:{index}']['x'])
                 if 'y' in self.prev_coords[f'vertex:{table_id}:row:{index}']:
                     mx_geometry.set('y', self.prev_coords[f'vertex:{table_id}:row:{index}']['y'])
+                if 'height' in self.prev_coords[f'vertex:{table_id}:row:{index}']:
+                    mx_geometry.set('height', self.prev_coords[f'vertex:{table_id}:row:{index}']['height'])
+                if 'width' in self.prev_coords[f'vertex:{table_id}:row:{index}']:
+                    mx_geometry.set('width', self.prev_coords[f'vertex:{table_id}:row:{index}']['width'])
 
     def add_service(self, id: str, node_name: str, arn: str, metadata='', node_enum=Services):
         # Type checking
         if not isinstance(node_enum, Services):
             raise TypeError('node_enum must be an instance of AWS,OnPrem Enum')
         self.add_vertex(id, node_name, arn, metadata, node_enum.value)
 
@@ -166,14 +175,18 @@
 
             # Position Vertex based on X,Y cords
             if f'vertex:{node_type}:{id}' in self.prev_coords:
                 if 'x' in self.prev_coords[f'vertex:{node_type}:{id}']:
                     mx_geometry.set('x', self.prev_coords[f'vertex:{node_type}:{id}']['x'])
                 if 'y' in self.prev_coords[f'vertex:{node_type}:{id}']:
                     mx_geometry.set('y', self.prev_coords[f'vertex:{node_type}:{id}']['y'])
+                if 'height' in self.prev_coords[f'vertex:{node_type}:{id}']:
+                    mx_geometry.set('height', self.prev_coords[f'vertex:{node_type}:{id}']['height'])
+                if 'width' in self.prev_coords[f'vertex:{node_type}:{id}']:
+                    mx_geometry.set('width', self.prev_coords[f'vertex:{node_type}:{id}']['width'])
 
     def add_vertex_list(self, vertexes):
         for vertex in vertexes:
             self.add_vertex(id=vertex['id'], node_name=vertex['nodeName'], metadata=vertex['nodeDescription'],
                             node_type=vertex['nodeType'])
         return
 
@@ -315,14 +328,18 @@
                 if neighbor.get('id').startswith("vertex:"):
                     data = neighbor.find('mxGeometry')
                     cords = {}
                     if data.get('x') is not None:
                         cords['x'] = data.get('x')
                     if data.get('y') is not None:
                         cords['y'] = data.get('y')
+                    if data.get('height') is not None:
+                        cords['height'] = data.get('height')
+                    if data.get('width') is not None:
+                        cords['width'] = data.get('width')
                     self.prev_coords[neighbor.get('id')] = cords
 
     def export_to_file(self, file_path):
         with open(file_path, 'wb') as file:
             tree = et.ElementTree(self.mxfile)
             et.indent(tree, space="\t", level=0)
             tree.write(file, encoding='utf-8')
```

### Comparing `multicloud_diagrams-0.3.5/multicloud_diagrams/providers/aws_services.json` & `multicloud_diagrams-0.3.6/multicloud_diagrams/providers/aws_services.json`

 * *Files identical despite different names*

### Comparing `multicloud_diagrams-0.3.5/multicloud_diagrams/providers/on_prem_services.json` & `multicloud_diagrams-0.3.6/multicloud_diagrams/providers/on_prem_services.json`

 * *Files identical despite different names*

### Comparing `multicloud_diagrams-0.3.5/pyproject.toml` & `multicloud_diagrams-0.3.6/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "multicloud-diagrams"
-version = "0.3.5"
+version = "0.3.6"
 description = "Library to generate DRAW.IO compatible diagrams to represent Cloud infrastructure. AWS Cloud supported."
 authors = ["Roman Tsypuk <tsypuk.conf@gmail.com>"]
 license = "MIT"
 readme = "README.md"
 packages = [{include = "multicloud_diagrams"}]
 
 [tool.poetry.dependencies]
```

### Comparing `multicloud_diagrams-0.3.5/PKG-INFO` & `multicloud_diagrams-0.3.6/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: multicloud-diagrams
-Version: 0.3.5
+Version: 0.3.6
 Summary: Library to generate DRAW.IO compatible diagrams to represent Cloud infrastructure. AWS Cloud supported.
 License: MIT
 Author: Roman Tsypuk
 Author-email: tsypuk.conf@gmail.com
 Requires-Python: >=3.10,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
@@ -197,11 +197,21 @@
     link_type: none }
 ```
 - Source [aws_iam_from_yaml.py](https://github.com/tsypuk/multicloud-diagrams/blob/main/samples/samples/aws_iam_from_yaml.py)
 - Output compiled [output.prod.iam-roles-from-yaml.drawio](https://raw.githubusercontent.com/tsypuk/multicloud-diagrams/main/samples/output/output.prod.iam-roles-from-yaml.drawio)
 
 - ![output.prod.iam-roles.png](https://github.com/tsypuk/multicloud-diagrams/blob/main/samples/output/png/output.prod.iam-roles-from-yaml.png?raw=True)
 
+```shell
+poetry build
+export PYPI_USERNAME=
+export PYPI_PASSWORD=
+poetry publish --build --username $PYPI_USERNAME --password $PYPI_PASSWORD
+
+cd samples/samples
+poetry install
+poetry run python aws_iam_roles_from_code_with_enum.py
+```
 
 ### FYI:
 
 OpenSource Guide, [How to contribute to opensource](https://opensource.guide/)
```

