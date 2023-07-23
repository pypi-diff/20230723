# Comparing `tmp/multicloud_diagrams-0.3.6.tar.gz` & `tmp/multicloud_diagrams-0.3.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "multicloud_diagrams-0.3.6.tar", max compression
+gzip compressed data, was "multicloud_diagrams-0.3.7.tar", max compression
```

## Comparing `multicloud_diagrams-0.3.6.tar` & `multicloud_diagrams-0.3.7.tar`

### file list

```diff
@@ -1,10 +1,10 @@
--rw-r--r--   0        0        0     1069 2023-05-14 15:36:37.276228 multicloud_diagrams-0.3.6/LICENSE
--rw-r--r--   0        0        0     8567 2023-07-23 08:37:02.246004 multicloud_diagrams-0.3.6/README.md
--rw-r--r--   0        0        0    16720 2023-07-23 16:29:00.842637 multicloud_diagrams-0.3.6/multicloud_diagrams/__init__.py
--rw-r--r--   0        0        0     3868 2023-07-23 07:39:33.823106 multicloud_diagrams-0.3.6/multicloud_diagrams/providers/aws_services.json
--rw-r--r--   0        0        0        2 2023-05-17 19:53:33.575412 multicloud_diagrams-0.3.6/multicloud_diagrams/providers/azure_services.json
--rw-r--r--   0        0        0      207 2023-05-19 12:11:15.381235 multicloud_diagrams-0.3.6/multicloud_diagrams/providers/fallback.json
--rw-r--r--   0        0        0        2 2023-05-17 19:53:33.570337 multicloud_diagrams-0.3.6/multicloud_diagrams/providers/gcp_services.json
--rw-r--r--   0        0        0      616 2023-07-23 07:39:33.816960 multicloud_diagrams-0.3.6/multicloud_diagrams/providers/on_prem_services.json
--rw-r--r--   0        0        0      525 2023-07-23 16:31:32.538368 multicloud_diagrams-0.3.6/pyproject.toml
--rw-r--r--   0        0        0     9085 1970-01-01 00:00:00.000000 multicloud_diagrams-0.3.6/PKG-INFO
+-rw-r--r--   0        0        0     1069 2023-05-14 15:36:37.276228 multicloud_diagrams-0.3.7/LICENSE
+-rw-r--r--   0        0        0     8567 2023-07-23 08:37:02.246004 multicloud_diagrams-0.3.7/README.md
+-rw-r--r--   0        0        0    16785 2023-07-23 19:43:42.165414 multicloud_diagrams-0.3.7/multicloud_diagrams/__init__.py
+-rw-r--r--   0        0        0     3868 2023-07-23 07:39:33.823106 multicloud_diagrams-0.3.7/multicloud_diagrams/providers/aws_services.json
+-rw-r--r--   0        0        0        2 2023-05-17 19:53:33.575412 multicloud_diagrams-0.3.7/multicloud_diagrams/providers/azure_services.json
+-rw-r--r--   0        0        0      207 2023-05-19 12:11:15.381235 multicloud_diagrams-0.3.7/multicloud_diagrams/providers/fallback.json
+-rw-r--r--   0        0        0        2 2023-05-17 19:53:33.570337 multicloud_diagrams-0.3.7/multicloud_diagrams/providers/gcp_services.json
+-rw-r--r--   0        0        0      616 2023-07-23 07:39:33.816960 multicloud_diagrams-0.3.7/multicloud_diagrams/providers/on_prem_services.json
+-rw-r--r--   0        0        0      525 2023-07-23 19:45:33.566284 multicloud_diagrams-0.3.7/pyproject.toml
+-rw-r--r--   0        0        0     9085 1970-01-01 00:00:00.000000 multicloud_diagrams-0.3.7/PKG-INFO
```

### Comparing `multicloud_diagrams-0.3.6/LICENSE` & `multicloud_diagrams-0.3.7/LICENSE`

 * *Files identical despite different names*

### Comparing `multicloud_diagrams-0.3.6/README.md` & `multicloud_diagrams-0.3.7/README.md`

 * *Files identical despite different names*

### Comparing `multicloud_diagrams-0.3.6/multicloud_diagrams/__init__.py` & `multicloud_diagrams-0.3.7/multicloud_diagrams/__init__.py`

 * *Files 0% similar despite different names*

```diff
@@ -102,20 +102,20 @@
             if 'y' in self.prev_coords[f'vertex:{table_id}:list']:
                 mx_geometry.set('y', self.prev_coords[f'vertex:{table_id}:list']['y'])
             if 'height' in self.prev_coords[f'vertex:{table_id}:list']:
                 mx_geometry.set('height', self.prev_coords[f'vertex:{table_id}:list']['height'])
             if 'width' in self.prev_coords[f'vertex:{table_id}:list']:
                 mx_geometry.set('width', self.prev_coords[f'vertex:{table_id}:list']['width'])
 
-
         for index, item in enumerate(rows):
+            name, value = item.split(":", 1)
             mx_cell = et.SubElement(self.root,
                                     'mxCell',
                                     id=f'vertex:{table_id}:row:{index}',
-                                    value=item,
+                                    value=f'<b>{name}</b>: {value}',
                                     style=("text;strokeColor=none;fillColor=none;align=left;verticalAlign=middle;"
                                            "spacingLeft=4;spacingRight=4;overflow=hidden;points=[[0,0.5],[1,0.5]];"
                                            "portConstraint=eastwest;rotatable=0;whiteSpace=wrap;html=1;"),
                                     parent=f'vertex:{table_id}:list',
                                     vertex="1")
 
             mx_geometry = et.SubElement(mx_cell, 'mxGeometry', width=width, height="30")
```

### Comparing `multicloud_diagrams-0.3.6/multicloud_diagrams/providers/aws_services.json` & `multicloud_diagrams-0.3.7/multicloud_diagrams/providers/aws_services.json`

 * *Files identical despite different names*

### Comparing `multicloud_diagrams-0.3.6/multicloud_diagrams/providers/on_prem_services.json` & `multicloud_diagrams-0.3.7/multicloud_diagrams/providers/on_prem_services.json`

 * *Files identical despite different names*

### Comparing `multicloud_diagrams-0.3.6/pyproject.toml` & `multicloud_diagrams-0.3.7/pyproject.toml`

 * *Files 2% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 [tool.poetry]
 name = "multicloud-diagrams"
-version = "0.3.6"
+version = "0.3.7"
 description = "Library to generate DRAW.IO compatible diagrams to represent Cloud infrastructure. AWS Cloud supported."
 authors = ["Roman Tsypuk <tsypuk.conf@gmail.com>"]
 license = "MIT"
 readme = "README.md"
 packages = [{include = "multicloud_diagrams"}]
 
 [tool.poetry.dependencies]
```

### Comparing `multicloud_diagrams-0.3.6/PKG-INFO` & `multicloud_diagrams-0.3.7/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: multicloud-diagrams
-Version: 0.3.6
+Version: 0.3.7
 Summary: Library to generate DRAW.IO compatible diagrams to represent Cloud infrastructure. AWS Cloud supported.
 License: MIT
 Author: Roman Tsypuk
 Author-email: tsypuk.conf@gmail.com
 Requires-Python: >=3.10,<4.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
```

