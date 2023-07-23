# Comparing `tmp/diagrams-yaml-0.0.8.tar.gz` & `tmp/diagrams-yaml-0.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "diagrams-yaml-0.0.8.tar", last modified: Sun Jul 23 10:22:44 2023, max compression
+gzip compressed data, was "diagrams-yaml-0.0.9.tar", last modified: Sun Jul 23 15:02:08 2023, max compression
```

## Comparing `diagrams-yaml-0.0.8.tar` & `diagrams-yaml-0.0.9.tar`

### file list

```diff
@@ -1,24 +1,24 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:22:44.799305 diagrams-yaml-0.0.8/
--rw-r--r--   0 runner    (1001) docker     (123)        6 2023-07-23 10:22:20.000000 diagrams-yaml-0.0.8/.project-version
--rw-r--r--   0 runner    (1001) docker     (123)     1075 2023-07-23 10:22:20.000000 diagrams-yaml-0.0.8/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       87 2023-07-23 10:22:20.000000 diagrams-yaml-0.0.8/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     6789 2023-07-23 10:22:44.799305 diagrams-yaml-0.0.8/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     5972 2023-07-23 10:22:20.000000 diagrams-yaml-0.0.8/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:22:44.799305 diagrams-yaml-0.0.8/diagrams_yaml/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 10:22:20.000000 diagrams-yaml-0.0.8/diagrams_yaml/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     8417 2023-07-23 10:22:20.000000 diagrams-yaml-0.0.8/diagrams_yaml/entrypoint.py
--rw-r--r--   0 runner    (1001) docker     (123)     1309 2023-07-23 10:22:20.000000 diagrams-yaml-0.0.8/diagrams_yaml/enums.py
--rw-r--r--   0 runner    (1001) docker     (123)     1109 2023-07-23 10:22:20.000000 diagrams-yaml-0.0.8/diagrams_yaml/resources.py
--rw-r--r--   0 runner    (1001) docker     (123)     1675 2023-07-23 10:22:20.000000 diagrams-yaml-0.0.8/diagrams_yaml/schema.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:22:44.799305 diagrams-yaml-0.0.8/diagrams_yaml.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     6789 2023-07-23 10:22:44.000000 diagrams-yaml-0.0.8/diagrams_yaml.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      457 2023-07-23 10:22:44.000000 diagrams-yaml-0.0.8/diagrams_yaml.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 10:22:44.000000 diagrams-yaml-0.0.8/diagrams_yaml.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       71 2023-07-23 10:22:44.000000 diagrams-yaml-0.0.8/diagrams_yaml.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)       47 2023-07-23 10:22:44.000000 diagrams-yaml-0.0.8/diagrams_yaml.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       14 2023-07-23 10:22:44.000000 diagrams-yaml-0.0.8/diagrams_yaml.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)      430 2023-07-23 10:22:20.000000 diagrams-yaml-0.0.8/pyproject.toml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 10:22:44.799305 diagrams-yaml-0.0.8/requirements/
--rw-r--r--   0 runner    (1001) docker     (123)       47 2023-07-23 10:22:20.000000 diagrams-yaml-0.0.8/requirements/project.txt
--rw-r--r--   0 runner    (1001) docker     (123)      195 2023-07-23 10:22:44.799305 diagrams-yaml-0.0.8/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1483 2023-07-23 10:22:20.000000 diagrams-yaml-0.0.8/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:02:08.939370 diagrams-yaml-0.0.9/
+-rw-r--r--   0 runner    (1001) docker     (123)        6 2023-07-23 15:01:47.000000 diagrams-yaml-0.0.9/.project-version
+-rw-r--r--   0 runner    (1001) docker     (123)     1075 2023-07-23 15:01:47.000000 diagrams-yaml-0.0.9/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       87 2023-07-23 15:01:47.000000 diagrams-yaml-0.0.9/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     6789 2023-07-23 15:02:08.939370 diagrams-yaml-0.0.9/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     5972 2023-07-23 15:01:47.000000 diagrams-yaml-0.0.9/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:02:08.939370 diagrams-yaml-0.0.9/diagrams_yaml/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 15:01:47.000000 diagrams-yaml-0.0.9/diagrams_yaml/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8611 2023-07-23 15:01:47.000000 diagrams-yaml-0.0.9/diagrams_yaml/entrypoint.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1309 2023-07-23 15:01:47.000000 diagrams-yaml-0.0.9/diagrams_yaml/enums.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1109 2023-07-23 15:01:47.000000 diagrams-yaml-0.0.9/diagrams_yaml/resources.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1675 2023-07-23 15:01:47.000000 diagrams-yaml-0.0.9/diagrams_yaml/schema.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:02:08.939370 diagrams-yaml-0.0.9/diagrams_yaml.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     6789 2023-07-23 15:02:08.000000 diagrams-yaml-0.0.9/diagrams_yaml.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      457 2023-07-23 15:02:08.000000 diagrams-yaml-0.0.9/diagrams_yaml.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 15:02:08.000000 diagrams-yaml-0.0.9/diagrams_yaml.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       71 2023-07-23 15:02:08.000000 diagrams-yaml-0.0.9/diagrams_yaml.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       47 2023-07-23 15:02:08.000000 diagrams-yaml-0.0.9/diagrams_yaml.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       14 2023-07-23 15:02:08.000000 diagrams-yaml-0.0.9/diagrams_yaml.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      430 2023-07-23 15:01:47.000000 diagrams-yaml-0.0.9/pyproject.toml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 15:02:08.939370 diagrams-yaml-0.0.9/requirements/
+-rw-r--r--   0 runner    (1001) docker     (123)       47 2023-07-23 15:01:47.000000 diagrams-yaml-0.0.9/requirements/project.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      195 2023-07-23 15:02:08.939370 diagrams-yaml-0.0.9/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1483 2023-07-23 15:01:47.000000 diagrams-yaml-0.0.9/setup.py
```

### Comparing `diagrams-yaml-0.0.8/LICENSE` & `diagrams-yaml-0.0.9/LICENSE`

 * *Files identical despite different names*

### Comparing `diagrams-yaml-0.0.8/PKG-INFO` & `diagrams-yaml-0.0.9/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: diagrams-yaml
-Version: 0.0.8
+Version: 0.0.9
 Summary: Diagram as Code in a declarative way using YAML for drawing cloud system architectures.
 Home-page: https://github.com/dmytrostriletskyi/diagrams-yaml
 Author: Dmytro Striletskyi
 Author-email: dmytro.striletskyi@gmail.com
 License: MIT
 Project-URL: Issue Tracker, https://github.com/dmytrostriletskyi/diagrams-yaml/issues
 Project-URL: Source Code, https://github.com/dmytrostriletskyi/diagrams-yaml
```

### Comparing `diagrams-yaml-0.0.8/README.md` & `diagrams-yaml-0.0.9/README.md`

 * *Files identical despite different names*

### Comparing `diagrams-yaml-0.0.8/diagrams_yaml/entrypoint.py` & `diagrams-yaml-0.0.9/diagrams_yaml/entrypoint.py`

 * *Files 2% similar despite different names*

```diff
@@ -140,17 +140,18 @@
 
     with open(yaml_file_path) as yaml_file:
         yaml_as_dict = yaml.safe_load(yaml_file)
 
     diagram_as_dict = yaml_as_dict.get('diagram')
     diagram = YamlDiagram(**diagram_as_dict)
 
-    graph_style = Diagram._default_graph_attrs | diagram.style.graph
-    node_style = Diagram._default_node_attrs | diagram.style.node
-    edge_style = Diagram._default_edge_attrs | diagram.style.edge
+    # TODO: figure out how to pass empty `YamlDiagramStyle` to `diagram.style` in Pydantic to remove the if condition.
+    graph_style = Diagram._default_graph_attrs | diagram.style.graph if diagram.style else {}
+    node_style = Diagram._default_node_attrs | diagram.style.node if diagram.style else {}
+    edge_style = Diagram._default_edge_attrs | diagram.style.edge if diagram.style else {}
 
     with Diagram(
         name=diagram.name,
         filename=diagram.file_name,
         direction=diagram.direction.mapped,
         outformat=diagram.format,
         autolabel=diagram.label_resources,
```

### Comparing `diagrams-yaml-0.0.8/diagrams_yaml/enums.py` & `diagrams-yaml-0.0.9/diagrams_yaml/enums.py`

 * *Files identical despite different names*

### Comparing `diagrams-yaml-0.0.8/diagrams_yaml/resources.py` & `diagrams-yaml-0.0.9/diagrams_yaml/resources.py`

 * *Files identical despite different names*

### Comparing `diagrams-yaml-0.0.8/diagrams_yaml/schema.py` & `diagrams-yaml-0.0.9/diagrams_yaml/schema.py`

 * *Files identical despite different names*

### Comparing `diagrams-yaml-0.0.8/diagrams_yaml.egg-info/PKG-INFO` & `diagrams-yaml-0.0.9/diagrams_yaml.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: diagrams-yaml
-Version: 0.0.8
+Version: 0.0.9
 Summary: Diagram as Code in a declarative way using YAML for drawing cloud system architectures.
 Home-page: https://github.com/dmytrostriletskyi/diagrams-yaml
 Author: Dmytro Striletskyi
 Author-email: dmytro.striletskyi@gmail.com
 License: MIT
 Project-URL: Issue Tracker, https://github.com/dmytrostriletskyi/diagrams-yaml/issues
 Project-URL: Source Code, https://github.com/dmytrostriletskyi/diagrams-yaml
```

### Comparing `diagrams-yaml-0.0.8/setup.py` & `diagrams-yaml-0.0.9/setup.py`

 * *Files identical despite different names*

