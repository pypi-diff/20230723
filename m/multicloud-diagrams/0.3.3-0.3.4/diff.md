# Comparing `tmp/multicloud_diagrams-0.3.3.tar.gz` & `tmp/multicloud_diagrams-0.3.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "multicloud_diagrams-0.3.3.tar", max compression
+gzip compressed data, was "multicloud_diagrams-0.3.4.tar", max compression
```

## Comparing `multicloud_diagrams-0.3.3.tar` & `multicloud_diagrams-0.3.4.tar`

### file list

```diff
@@ -1,10 +1,10 @@
--rw-r--r--   0        0        0     1069 2023-05-14 15:36:37.276228 multicloud_diagrams-0.3.3/LICENSE
--rw-r--r--   0        0        0     8332 2023-05-18 17:11:07.243158 multicloud_diagrams-0.3.3/README.md
--rw-r--r--   0        0        0    14627 2023-06-15 15:55:14.082468 multicloud_diagrams-0.3.3/multicloud_diagrams/__init__.py
--rw-r--r--   0        0        0     3479 2023-05-19 12:11:13.264328 multicloud_diagrams-0.3.3/multicloud_diagrams/providers/aws_services.json
--rw-r--r--   0        0        0        2 2023-05-17 19:53:33.575412 multicloud_diagrams-0.3.3/multicloud_diagrams/providers/azure_services.json
--rw-r--r--   0        0        0      207 2023-05-19 12:11:15.381235 multicloud_diagrams-0.3.3/multicloud_diagrams/providers/fallback.json
--rw-r--r--   0        0        0        2 2023-05-17 19:53:33.570337 multicloud_diagrams-0.3.3/multicloud_diagrams/providers/gcp_services.json
--rw-r--r--   0        0        0        2 2023-05-17 19:53:33.563770 multicloud_diagrams-0.3.3/multicloud_diagrams/providers/on_prem_services.json
--rw-r--r--   0        0        0      525 2023-06-15 15:57:49.497018 multicloud_diagrams-0.3.3/pyproject.toml
--rw-r--r--   0        0        0     8850 1970-01-01 00:00:00.000000 multicloud_diagrams-0.3.3/PKG-INFO
+-rw-r--r--   0        0        0     1069 2023-05-14 15:36:37.276228 multicloud_diagrams-0.3.4/LICENSE
+-rw-r--r--   0        0        0     8332 2023-05-18 17:11:07.243158 multicloud_diagrams-0.3.4/README.md
+-rw-r--r--   0        0        0    15466 2023-07-23 08:02:49.082002 multicloud_diagrams-0.3.4/multicloud_diagrams/__init__.py
+-rw-r--r--   0        0        0     3868 2023-07-23 07:39:33.823106 multicloud_diagrams-0.3.4/multicloud_diagrams/providers/aws_services.json
+-rw-r--r--   0        0        0        2 2023-05-17 19:53:33.575412 multicloud_diagrams-0.3.4/multicloud_diagrams/providers/azure_services.json
+-rw-r--r--   0        0        0      207 2023-05-19 12:11:15.381235 multicloud_diagrams-0.3.4/multicloud_diagrams/providers/fallback.json
+-rw-r--r--   0        0        0        2 2023-05-17 19:53:33.570337 multicloud_diagrams-0.3.4/multicloud_diagrams/providers/gcp_services.json
+-rw-r--r--   0        0        0      616 2023-07-23 07:39:33.816960 multicloud_diagrams-0.3.4/multicloud_diagrams/providers/on_prem_services.json
+-rw-r--r--   0        0        0      525 2023-07-23 08:07:03.845285 multicloud_diagrams-0.3.4/pyproject.toml
+-rw-r--r--   0        0        0     8850 1970-01-01 00:00:00.000000 multicloud_diagrams-0.3.4/PKG-INFO
```

### Comparing `multicloud_diagrams-0.3.3/LICENSE` & `multicloud_diagrams-0.3.4/LICENSE`

 * *Files identical despite different names*

### Comparing `multicloud_diagrams-0.3.3/README.md` & `multicloud_diagrams-0.3.4/README.md`

 * *Files identical despite different names*

### Comparing `multicloud_diagrams-0.3.3/multicloud_diagrams/__init__.py` & `multicloud_diagrams-0.3.4/multicloud_diagrams/__init__.py`

 * *Files 4% similar despite different names*

```diff
@@ -1,15 +1,42 @@
 import json
 import xml.etree.ElementTree as et
 import logging
 import os.path
 import pkgutil
+from enum import Enum
+from typing import Union
+
 import yaml
 
 
+class AWS(Enum):
+    lambda_function = "lambda_function"
+    sqs = "sqs"
+    sns = "sns"
+    iam_role = "iam_role"
+    iam_policy = "iam_policy"
+    iam_permission = "iam_permission"
+    dynamo = "dynamo"
+    dynamo_stream = "dynamo_stream"
+    api_gw = "api_gw"
+    s3 = "s3"
+    kms = "kms"
+    ssm = "ssm"
+    mq = "mq"
+
+
+class OnPrem(Enum):
+    http = "http"
+    mq_broker = "mq_broker"
+
+
+Services = Union[AWS, OnPrem]
+
+
 class MultiCloudDiagrams:
     def __init__(self):
         self.mxfile = et.Element('mxfile', host="multicloud-diagrams",
                                  agent="PIP package multicloud-diagrams. Generate resources in draw.io compatible format for Cloud infrastructure. Copyrights @ Roman Tsypuk 2023. MIT license.",
                                  type="MultiCloud")
         self.diagram = et.SubElement(self.mxfile, 'diagram', id="diagram_1", name="AWS components")
         self.mx_graph_model = et.SubElement(self.diagram, 'mxGraphModel', dx="1015", dy="661", grid="1", gridSize="10",
@@ -47,15 +74,15 @@
 
     # green fillColor=#d5e8d4
     # red fillColor=#f8cecc;"
     def add_list(self, table_id='', table_name='', fillColor='', rows=[], width="300"):
         if not table_id:
             table_id = table_name
 
-        style="swimlane;fontStyle=0;childLayout=stackLayout;horizontal=1;startSize=30;horizontalStack=0;resizeParent=1;resizeParentMax=0;resizeLast=0;collapsible=1;marginBottom=0;whiteSpace=wrap;html=1;"
+        style = "swimlane;fontStyle=0;childLayout=stackLayout;horizontal=1;startSize=30;horizontalStack=0;resizeParent=1;resizeParentMax=0;resizeLast=0;collapsible=1;marginBottom=0;whiteSpace=wrap;html=1;"
 
         if fillColor:
             style += f"fillColor={fillColor}"
 
         mx_cell = et.SubElement(self.root,
                                 'mxCell',
                                 id=f'vertex:{table_id}:list',
@@ -91,14 +118,20 @@
             # Position Vertex based on X,Y cords
             if f'vertex:{table_id}:row:{index}' in self.prev_coords:
                 if 'x' in self.prev_coords[f'vertex:{table_id}:row:{index}']:
                     mx_geometry.set('x', self.prev_coords[f'vertex:{table_id}:row:{index}']['x'])
                 if 'y' in self.prev_coords[f'vertex:{table_id}:row:{index}']:
                     mx_geometry.set('y', self.prev_coords[f'vertex:{table_id}:row:{index}']['y'])
 
+    def add_vertex(self, id: str, node_name: str, arn: str, metadata='', node_enum=Services):
+        # Type checking
+        if not isinstance(node_enum, self.Services):
+            raise TypeError('direction must be an instance of Direction Enum')
+        self.add_vertex(self, id=id, node_name=node_name, arn=arn, metadata=metadata, node_type=node_enum.value)
+
     def add_vertex(self, id: str, node_name: str, arn: str, metadata='', node_type=''):
 
         # check that there is no such vertex already
         exist = False
         for mx_cell in self.root:
             # print(mxCell.attrib['id'])
             if mx_cell.attrib['id'] == f'vertex:{node_type}:{id}':
```

### Comparing `multicloud_diagrams-0.3.3/multicloud_diagrams/providers/aws_services.json` & `multicloud_diagrams-0.3.4/multicloud_diagrams/providers/aws_services.json`

 * *Files 6% similar despite different names*

#### Pretty-printed

 * *Similarity: 0.9230769230769231%*

 * *Differences: {"'mq'": "OrderedDict([('style', "*

 * *         "'sketch=0;outlineConnect=0;fontColor=#232F3E;gradientColor=#FF4F8B;gradientDirection=north;fillColor=#BC1356;strokeColor=#ffffff;dashed=0;verticalLabelPosition=bottom;verticalAlign=top;align=center;html=1;fontSize=12;fontStyle=0;aspect=fixed;shape=mxgraph.aws4.resourceIcon;resIcon=mxgraph.aws4.mq;'), "*

 * *         "('width', '78'), ('height', '78'), ('nodeLevel', '2')])"}*

```diff
@@ -43,14 +43,20 @@
     },
     "lambda_function": {
         "height": "72",
         "nodeLevel": "4",
         "style": "verticalLabelPosition=bottom;html=1;verticalAlign=top;aspect=fixed;align=left;pointerEvents=1;shape=mxgraph.aws3.lambda_function;prIcon=server;fillColor=#F58534;gradientColor=none;html=1;",
         "width": "69"
     },
+    "mq": {
+        "height": "78",
+        "nodeLevel": "2",
+        "style": "sketch=0;outlineConnect=0;fontColor=#232F3E;gradientColor=#FF4F8B;gradientDirection=north;fillColor=#BC1356;strokeColor=#ffffff;dashed=0;verticalLabelPosition=bottom;verticalAlign=top;align=center;html=1;fontSize=12;fontStyle=0;aspect=fixed;shape=mxgraph.aws4.resourceIcon;resIcon=mxgraph.aws4.mq;",
+        "width": "78"
+    },
     "s3": {
         "height": "78",
         "nodeLevel": "4",
         "style": "outlineConnect=0;dashed=0;verticalLabelPosition=bottom;verticalAlign=top;align=left;html=1;shape=mxgraph.aws3.bucket_with_objects;fillColor=#E05243;gradientColor=none;",
         "width": "78"
     },
     "sns": {
```

### Comparing `multicloud_diagrams-0.3.3/pyproject.toml` & `multicloud_diagrams-0.3.4/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "multicloud-diagrams"
-version = "0.3.3"
+version = "0.3.4"
 description = "Library to generate DRAW.IO compatible diagrams to represent Cloud infrastructure. AWS Cloud supported."
 authors = ["Roman Tsypuk <tsypuk.conf@gmail.com>"]
 license = "MIT"
 readme = "README.md"
 packages = [{include = "multicloud_diagrams"}]
 
 [tool.poetry.dependencies]
```

### Comparing `multicloud_diagrams-0.3.3/PKG-INFO` & `multicloud_diagrams-0.3.4/PKG-INFO`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: multicloud-diagrams
-Version: 0.3.3
+Version: 0.3.4
 Summary: Library to generate DRAW.IO compatible diagrams to represent Cloud infrastructure. AWS Cloud supported.
 License: MIT
 Author: Roman Tsypuk
 Author-email: tsypuk.conf@gmail.com
 Requires-Python: >=3.10,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
```

