# Comparing `tmp/diagrams-yaml-0.0.6.tar.gz` & `tmp/diagrams-yaml-0.0.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "diagrams-yaml-0.0.6.tar", last modified: Sat Jul 22 14:49:55 2023, max compression
+gzip compressed data, was "diagrams-yaml-0.0.7.tar", last modified: Sat Jul 22 18:38:18 2023, max compression
```

## Comparing `diagrams-yaml-0.0.6.tar` & `diagrams-yaml-0.0.7.tar`

### file list

```diff
@@ -1,24 +1,24 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 14:49:55.812012 diagrams-yaml-0.0.6/
--rw-r--r--   0 runner    (1001) docker     (123)        6 2023-07-22 14:49:36.000000 diagrams-yaml-0.0.6/.project-version
--rw-r--r--   0 runner    (1001) docker     (123)     1075 2023-07-22 14:49:36.000000 diagrams-yaml-0.0.6/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       87 2023-07-22 14:49:36.000000 diagrams-yaml-0.0.6/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)     6787 2023-07-22 14:49:55.812012 diagrams-yaml-0.0.6/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     5970 2023-07-22 14:49:36.000000 diagrams-yaml-0.0.6/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 14:49:55.812012 diagrams-yaml-0.0.6/diagrams_yaml/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-22 14:49:36.000000 diagrams-yaml-0.0.6/diagrams_yaml/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     8417 2023-07-22 14:49:36.000000 diagrams-yaml-0.0.6/diagrams_yaml/entrypoint.py
--rw-r--r--   0 runner    (1001) docker     (123)     1309 2023-07-22 14:49:36.000000 diagrams-yaml-0.0.6/diagrams_yaml/enums.py
--rw-r--r--   0 runner    (1001) docker     (123)     1109 2023-07-22 14:49:36.000000 diagrams-yaml-0.0.6/diagrams_yaml/resources.py
--rw-r--r--   0 runner    (1001) docker     (123)     1675 2023-07-22 14:49:36.000000 diagrams-yaml-0.0.6/diagrams_yaml/schema.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 14:49:55.812012 diagrams-yaml-0.0.6/diagrams_yaml.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)     6787 2023-07-22 14:49:55.000000 diagrams-yaml-0.0.6/diagrams_yaml.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      457 2023-07-22 14:49:55.000000 diagrams-yaml-0.0.6/diagrams_yaml.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-22 14:49:55.000000 diagrams-yaml-0.0.6/diagrams_yaml.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       71 2023-07-22 14:49:55.000000 diagrams-yaml-0.0.6/diagrams_yaml.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)       47 2023-07-22 14:49:55.000000 diagrams-yaml-0.0.6/diagrams_yaml.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       14 2023-07-22 14:49:55.000000 diagrams-yaml-0.0.6/diagrams_yaml.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)      430 2023-07-22 14:49:36.000000 diagrams-yaml-0.0.6/pyproject.toml
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 14:49:55.812012 diagrams-yaml-0.0.6/requirements/
--rw-r--r--   0 runner    (1001) docker     (123)       47 2023-07-22 14:49:36.000000 diagrams-yaml-0.0.6/requirements/project.txt
--rw-r--r--   0 runner    (1001) docker     (123)      195 2023-07-22 14:49:55.812012 diagrams-yaml-0.0.6/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1483 2023-07-22 14:49:36.000000 diagrams-yaml-0.0.6/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 18:38:18.161997 diagrams-yaml-0.0.7/
+-rw-r--r--   0 runner    (1001) docker     (123)        6 2023-07-22 18:37:55.000000 diagrams-yaml-0.0.7/.project-version
+-rw-r--r--   0 runner    (1001) docker     (123)     1075 2023-07-22 18:37:55.000000 diagrams-yaml-0.0.7/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (123)       87 2023-07-22 18:37:55.000000 diagrams-yaml-0.0.7/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (123)     6789 2023-07-22 18:38:18.161997 diagrams-yaml-0.0.7/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)     5972 2023-07-22 18:37:55.000000 diagrams-yaml-0.0.7/README.md
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 18:38:18.161997 diagrams-yaml-0.0.7/diagrams_yaml/
+-rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-22 18:37:55.000000 diagrams-yaml-0.0.7/diagrams_yaml/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (123)     8417 2023-07-22 18:37:55.000000 diagrams-yaml-0.0.7/diagrams_yaml/entrypoint.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1309 2023-07-22 18:37:55.000000 diagrams-yaml-0.0.7/diagrams_yaml/enums.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1109 2023-07-22 18:37:55.000000 diagrams-yaml-0.0.7/diagrams_yaml/resources.py
+-rw-r--r--   0 runner    (1001) docker     (123)     1675 2023-07-22 18:37:55.000000 diagrams-yaml-0.0.7/diagrams_yaml/schema.py
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 18:38:18.161997 diagrams-yaml-0.0.7/diagrams_yaml.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (123)     6789 2023-07-22 18:38:18.000000 diagrams-yaml-0.0.7/diagrams_yaml.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (123)      457 2023-07-22 18:38:18.000000 diagrams-yaml-0.0.7/diagrams_yaml.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-22 18:38:18.000000 diagrams-yaml-0.0.7/diagrams_yaml.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       71 2023-07-22 18:38:18.000000 diagrams-yaml-0.0.7/diagrams_yaml.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       47 2023-07-22 18:38:18.000000 diagrams-yaml-0.0.7/diagrams_yaml.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (123)       14 2023-07-22 18:38:18.000000 diagrams-yaml-0.0.7/diagrams_yaml.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      430 2023-07-22 18:37:55.000000 diagrams-yaml-0.0.7/pyproject.toml
+drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-22 18:38:18.161997 diagrams-yaml-0.0.7/requirements/
+-rw-r--r--   0 runner    (1001) docker     (123)       47 2023-07-22 18:37:55.000000 diagrams-yaml-0.0.7/requirements/project.txt
+-rw-r--r--   0 runner    (1001) docker     (123)      195 2023-07-22 18:38:18.161997 diagrams-yaml-0.0.7/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (123)     1483 2023-07-22 18:37:55.000000 diagrams-yaml-0.0.7/setup.py
```

### Comparing `diagrams-yaml-0.0.6/LICENSE` & `diagrams-yaml-0.0.7/LICENSE`

 * *Files identical despite different names*

### Comparing `diagrams-yaml-0.0.6/PKG-INFO` & `diagrams-yaml-0.0.7/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: diagrams-yaml
-Version: 0.0.6
+Version: 0.0.7
 Summary: Diagram as Code in a declarative way using YAML for drawing cloud system architectures.
 Home-page: https://github.com/dmytrostriletskyi/diagrams-yaml
 Author: Dmytro Striletskyi
 Author-email: dmytro.striletskyi@gmail.com
 License: MIT
 Project-URL: Issue Tracker, https://github.com/dmytrostriletskyi/diagrams-yaml/issues
 Project-URL: Source Code, https://github.com/dmytrostriletskyi/diagrams-yaml
@@ -29,15 +29,15 @@
 
 Table of content:
 
 * [Introduction](#introduction)
 * [Getting Started](#getting-started)
   * [How to Install](#how-to-install)
   * [Examples](#examples)
-* [Usage](#usage)
+  * [Usage](#usage)
 * [Disclaimer](#disclaimer)
 
 ## Introduction
 
 This project lets you draw the cloud system architecture in a declarative way with widely used `YAML` syntax which is de 
 facto a standard for infrastructure and configurations so here habitual approaches are met and industry best practices
 are aligned as well. It allows you to track an architecture's diagram changes with a version control system such as 
@@ -46,16 +46,16 @@
 Currently, the following components are provided:
 
 * Major cloud providers: AWS, Azume, GCP, IBM, Alibaba, Oracle, OpenStack, Digital Ocean and so on.
 * On premise, Kubernetes, Firebase, Elastic, SaaS.
 * Programming languages and frameworks.
 * And other generic things such as C4.
 
-Basically, with the project, you just define set of resources, compose them into groups and/or clusters and set a 
-relationship, anything else is done under the hood.
+Basically, with the project, you just define set of resources, compose them into groups and/or clusters and set 
+relationships, anything else is done under the hood.
 
 ## Getting Started
 
 ### How to install
 
 As the project uses [Graphviz](https://www.graphviz.org) to render the diagram, you need to install it:
 
@@ -78,29 +78,29 @@
 |-----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
 | ![](./assets/web-services-architecture-on-aws.png)                                                                                | ![](./assets/web-services-architecture-on-premise.png)                                                                                       | ![](./assets/exposed-pods-architecture-on-kubernetes.png)                                                                                       |
 
 | [Message Collecting on GCP](https://github.com/dmytrostriletskyi/diagrams-yaml/blob/main/examples/message-collecting-gcp.yaml)    | [Events Processing on AWS](https://github.com/dmytrostriletskyi/diagrams-yaml/blob/main/examples/events-processing-aws.yaml)                 | [Workers on AWS](https://github.com/dmytrostriletskyi/diagrams-yaml/blob/main/examples/workers-aws.yaml)                                        |
 | --------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
 | ![](./assets/message-collecting-architecture-on-gcp.png)                                                                          | ![](./assets/events-processing-on-aws.png)                                                                                                   | ![](./assets/workers-architecture-on-aws.png)                                                                                                   |
 
-## Usage
+### Usage
 
 To draw an architecture, call `diagrams-yaml` command line interface, providing a path to a `YAML` file with 
 configurations:
 
 ```bash
 $ diagrams-yaml examples/web-services-aws.yaml
 ```
 
 The drawing will be saved in the folder the command line interface was executed from:
 
 ```bash
 $ ls
 ├── ...
-└── web_services_aws.png
+└── web-services-aws.png
 ```
 
 ## Disclaimer
 
 `diagrams-yaml` is a wrapper around original [diagrams](https://github.com/mingrammer/diagrams). The original `diagrams` 
 lets you draw the cloud system architecture in `Python` code. It was born for prototyping a new system architecture 
 design without any design tools. Under the hood, `diagrams-yaml` parse a `YAML` file and map to specific set of
```

### Comparing `diagrams-yaml-0.0.6/README.md` & `diagrams-yaml-0.0.7/README.md`

 * *Files 1% similar despite different names*

```diff
@@ -10,15 +10,15 @@
 
 Table of content:
 
 * [Introduction](#introduction)
 * [Getting Started](#getting-started)
   * [How to Install](#how-to-install)
   * [Examples](#examples)
-* [Usage](#usage)
+  * [Usage](#usage)
 * [Disclaimer](#disclaimer)
 
 ## Introduction
 
 This project lets you draw the cloud system architecture in a declarative way with widely used `YAML` syntax which is de 
 facto a standard for infrastructure and configurations so here habitual approaches are met and industry best practices
 are aligned as well. It allows you to track an architecture's diagram changes with a version control system such as 
@@ -27,16 +27,16 @@
 Currently, the following components are provided:
 
 * Major cloud providers: AWS, Azume, GCP, IBM, Alibaba, Oracle, OpenStack, Digital Ocean and so on.
 * On premise, Kubernetes, Firebase, Elastic, SaaS.
 * Programming languages and frameworks.
 * And other generic things such as C4.
 
-Basically, with the project, you just define set of resources, compose them into groups and/or clusters and set a 
-relationship, anything else is done under the hood.
+Basically, with the project, you just define set of resources, compose them into groups and/or clusters and set 
+relationships, anything else is done under the hood.
 
 ## Getting Started
 
 ### How to install
 
 As the project uses [Graphviz](https://www.graphviz.org) to render the diagram, you need to install it:
 
@@ -59,29 +59,29 @@
 |-----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
 | ![](./assets/web-services-architecture-on-aws.png)                                                                                | ![](./assets/web-services-architecture-on-premise.png)                                                                                       | ![](./assets/exposed-pods-architecture-on-kubernetes.png)                                                                                       |
 
 | [Message Collecting on GCP](https://github.com/dmytrostriletskyi/diagrams-yaml/blob/main/examples/message-collecting-gcp.yaml)    | [Events Processing on AWS](https://github.com/dmytrostriletskyi/diagrams-yaml/blob/main/examples/events-processing-aws.yaml)                 | [Workers on AWS](https://github.com/dmytrostriletskyi/diagrams-yaml/blob/main/examples/workers-aws.yaml)                                        |
 | --------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
 | ![](./assets/message-collecting-architecture-on-gcp.png)                                                                          | ![](./assets/events-processing-on-aws.png)                                                                                                   | ![](./assets/workers-architecture-on-aws.png)                                                                                                   |
 
-## Usage
+### Usage
 
 To draw an architecture, call `diagrams-yaml` command line interface, providing a path to a `YAML` file with 
 configurations:
 
 ```bash
 $ diagrams-yaml examples/web-services-aws.yaml
 ```
 
 The drawing will be saved in the folder the command line interface was executed from:
 
 ```bash
 $ ls
 ├── ...
-└── web_services_aws.png
+└── web-services-aws.png
 ```
 
 ## Disclaimer
 
 `diagrams-yaml` is a wrapper around original [diagrams](https://github.com/mingrammer/diagrams). The original `diagrams` 
 lets you draw the cloud system architecture in `Python` code. It was born for prototyping a new system architecture 
 design without any design tools. Under the hood, `diagrams-yaml` parse a `YAML` file and map to specific set of
```

### Comparing `diagrams-yaml-0.0.6/diagrams_yaml/entrypoint.py` & `diagrams-yaml-0.0.7/diagrams_yaml/entrypoint.py`

 * *Files identical despite different names*

### Comparing `diagrams-yaml-0.0.6/diagrams_yaml/enums.py` & `diagrams-yaml-0.0.7/diagrams_yaml/enums.py`

 * *Files identical despite different names*

### Comparing `diagrams-yaml-0.0.6/diagrams_yaml/resources.py` & `diagrams-yaml-0.0.7/diagrams_yaml/resources.py`

 * *Files identical despite different names*

### Comparing `diagrams-yaml-0.0.6/diagrams_yaml/schema.py` & `diagrams-yaml-0.0.7/diagrams_yaml/schema.py`

 * *Files identical despite different names*

### Comparing `diagrams-yaml-0.0.6/diagrams_yaml.egg-info/PKG-INFO` & `diagrams-yaml-0.0.7/diagrams_yaml.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: diagrams-yaml
-Version: 0.0.6
+Version: 0.0.7
 Summary: Diagram as Code in a declarative way using YAML for drawing cloud system architectures.
 Home-page: https://github.com/dmytrostriletskyi/diagrams-yaml
 Author: Dmytro Striletskyi
 Author-email: dmytro.striletskyi@gmail.com
 License: MIT
 Project-URL: Issue Tracker, https://github.com/dmytrostriletskyi/diagrams-yaml/issues
 Project-URL: Source Code, https://github.com/dmytrostriletskyi/diagrams-yaml
@@ -29,15 +29,15 @@
 
 Table of content:
 
 * [Introduction](#introduction)
 * [Getting Started](#getting-started)
   * [How to Install](#how-to-install)
   * [Examples](#examples)
-* [Usage](#usage)
+  * [Usage](#usage)
 * [Disclaimer](#disclaimer)
 
 ## Introduction
 
 This project lets you draw the cloud system architecture in a declarative way with widely used `YAML` syntax which is de 
 facto a standard for infrastructure and configurations so here habitual approaches are met and industry best practices
 are aligned as well. It allows you to track an architecture's diagram changes with a version control system such as 
@@ -46,16 +46,16 @@
 Currently, the following components are provided:
 
 * Major cloud providers: AWS, Azume, GCP, IBM, Alibaba, Oracle, OpenStack, Digital Ocean and so on.
 * On premise, Kubernetes, Firebase, Elastic, SaaS.
 * Programming languages and frameworks.
 * And other generic things such as C4.
 
-Basically, with the project, you just define set of resources, compose them into groups and/or clusters and set a 
-relationship, anything else is done under the hood.
+Basically, with the project, you just define set of resources, compose them into groups and/or clusters and set 
+relationships, anything else is done under the hood.
 
 ## Getting Started
 
 ### How to install
 
 As the project uses [Graphviz](https://www.graphviz.org) to render the diagram, you need to install it:
 
@@ -78,29 +78,29 @@
 |-----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
 | ![](./assets/web-services-architecture-on-aws.png)                                                                                | ![](./assets/web-services-architecture-on-premise.png)                                                                                       | ![](./assets/exposed-pods-architecture-on-kubernetes.png)                                                                                       |
 
 | [Message Collecting on GCP](https://github.com/dmytrostriletskyi/diagrams-yaml/blob/main/examples/message-collecting-gcp.yaml)    | [Events Processing on AWS](https://github.com/dmytrostriletskyi/diagrams-yaml/blob/main/examples/events-processing-aws.yaml)                 | [Workers on AWS](https://github.com/dmytrostriletskyi/diagrams-yaml/blob/main/examples/workers-aws.yaml)                                        |
 | --------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
 | ![](./assets/message-collecting-architecture-on-gcp.png)                                                                          | ![](./assets/events-processing-on-aws.png)                                                                                                   | ![](./assets/workers-architecture-on-aws.png)                                                                                                   |
 
-## Usage
+### Usage
 
 To draw an architecture, call `diagrams-yaml` command line interface, providing a path to a `YAML` file with 
 configurations:
 
 ```bash
 $ diagrams-yaml examples/web-services-aws.yaml
 ```
 
 The drawing will be saved in the folder the command line interface was executed from:
 
 ```bash
 $ ls
 ├── ...
-└── web_services_aws.png
+└── web-services-aws.png
 ```
 
 ## Disclaimer
 
 `diagrams-yaml` is a wrapper around original [diagrams](https://github.com/mingrammer/diagrams). The original `diagrams` 
 lets you draw the cloud system architecture in `Python` code. It was born for prototyping a new system architecture 
 design without any design tools. Under the hood, `diagrams-yaml` parse a `YAML` file and map to specific set of
```

### Comparing `diagrams-yaml-0.0.6/setup.py` & `diagrams-yaml-0.0.7/setup.py`

 * *Files identical despite different names*

