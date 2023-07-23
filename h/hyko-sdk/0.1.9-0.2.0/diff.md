# Comparing `tmp/hyko_sdk-0.1.9.tar.gz` & `tmp/hyko_sdk-0.2.0.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "hyko_sdk-0.1.9.tar", last modified: Mon Jun 26 13:17:25 2023, max compression
+gzip compressed data, was "hyko_sdk-0.2.0.tar", last modified: Sun Jul 23 12:53:47 2023, max compression
```

## Comparing `hyko_sdk-0.1.9.tar` & `hyko_sdk-0.2.0.tar`

### file list

```diff
@@ -1,16 +1,17 @@
-drwxr-xr-x   0 dahmadjid  (1000) dahmadjid  (1000)        0 2023-06-26 13:17:25.780210 hyko_sdk-0.1.9/
--rw-r--r--   0 dahmadjid  (1000) dahmadjid  (1000)      192 2023-06-26 13:17:25.780210 hyko_sdk-0.1.9/PKG-INFO
--rw-r--r--   0 dahmadjid  (1000) dahmadjid  (1000)      411 2023-05-19 16:11:29.000000 hyko_sdk-0.1.9/README.md
-drwxr-xr-x   0 dahmadjid  (1000) dahmadjid  (1000)        0 2023-06-26 13:17:25.780210 hyko_sdk-0.1.9/hyko_sdk/
--rw-r--r--   0 dahmadjid  (1000) dahmadjid  (1000)       60 2023-06-26 13:00:23.000000 hyko_sdk-0.1.9/hyko_sdk/__init__.py
--rw-r--r--   0 dahmadjid  (1000) dahmadjid  (1000)      682 2023-06-26 13:00:23.000000 hyko_sdk-0.1.9/hyko_sdk/error.py
--rw-r--r--   0 dahmadjid  (1000) dahmadjid  (1000)     4767 2023-06-26 13:16:13.000000 hyko_sdk-0.1.9/hyko_sdk/io.py
--rw-r--r--   0 dahmadjid  (1000) dahmadjid  (1000)     2791 2023-06-26 13:00:23.000000 hyko_sdk-0.1.9/hyko_sdk/metadata.py
-drwxr-xr-x   0 dahmadjid  (1000) dahmadjid  (1000)        0 2023-06-26 13:17:25.780210 hyko_sdk-0.1.9/hyko_sdk.egg-info/
--rw-r--r--   0 dahmadjid  (1000) dahmadjid  (1000)      192 2023-06-26 13:17:25.000000 hyko_sdk-0.1.9/hyko_sdk.egg-info/PKG-INFO
--rw-r--r--   0 dahmadjid  (1000) dahmadjid  (1000)      268 2023-06-26 13:17:25.000000 hyko_sdk-0.1.9/hyko_sdk.egg-info/SOURCES.txt
--rw-r--r--   0 dahmadjid  (1000) dahmadjid  (1000)        1 2023-06-26 13:17:25.000000 hyko_sdk-0.1.9/hyko_sdk.egg-info/dependency_links.txt
--rw-r--r--   0 dahmadjid  (1000) dahmadjid  (1000)       37 2023-06-26 13:17:25.000000 hyko_sdk-0.1.9/hyko_sdk.egg-info/requires.txt
--rw-r--r--   0 dahmadjid  (1000) dahmadjid  (1000)        9 2023-06-26 13:17:25.000000 hyko_sdk-0.1.9/hyko_sdk.egg-info/top_level.txt
--rw-r--r--   0 dahmadjid  (1000) dahmadjid  (1000)       80 2023-06-21 08:15:38.000000 hyko_sdk-0.1.9/pyproject.toml
--rw-r--r--   0 dahmadjid  (1000) dahmadjid  (1000)      357 2023-06-26 13:17:25.780210 hyko_sdk-0.1.9/setup.cfg
+drwxrwxr-x   0 dahmadjid  (1005) docker     (999)        0 2023-07-23 12:53:47.839647 hyko_sdk-0.2.0/
+-rw-rw-r--   0 dahmadjid  (1005) docker     (999)      192 2023-07-23 12:53:47.843647 hyko_sdk-0.2.0/PKG-INFO
+-rw-rw-r--   0 dahmadjid  (1005) docker     (999)      411 2023-07-23 09:57:30.000000 hyko_sdk-0.2.0/README.md
+drwxrwxr-x   0 dahmadjid  (1005) docker     (999)        0 2023-07-23 12:53:47.839647 hyko_sdk-0.2.0/hyko_sdk/
+-rw-rw-r--   0 dahmadjid  (1005) docker     (999)       60 2023-07-23 09:57:30.000000 hyko_sdk-0.2.0/hyko_sdk/__init__.py
+-rw-rw-r--   0 dahmadjid  (1005) docker     (999)      682 2023-07-23 09:57:30.000000 hyko_sdk-0.2.0/hyko_sdk/error.py
+-rw-rw-r--   0 dahmadjid  (1005) docker     (999)    18128 2023-07-23 12:48:09.000000 hyko_sdk-0.2.0/hyko_sdk/io.py
+-rw-rw-r--   0 dahmadjid  (1005) docker     (999)     3021 2023-07-23 09:57:30.000000 hyko_sdk-0.2.0/hyko_sdk/metadata.py
+-rw-rw-r--   0 dahmadjid  (1005) docker     (999)     2263 2023-07-23 09:57:30.000000 hyko_sdk-0.2.0/hyko_sdk/utils.py
+drwxrwxr-x   0 dahmadjid  (1005) docker     (999)        0 2023-07-23 12:53:47.839647 hyko_sdk-0.2.0/hyko_sdk.egg-info/
+-rw-rw-r--   0 dahmadjid  (1005) docker     (999)      192 2023-07-23 12:53:47.000000 hyko_sdk-0.2.0/hyko_sdk.egg-info/PKG-INFO
+-rw-rw-r--   0 dahmadjid  (1005) docker     (999)      286 2023-07-23 12:53:47.000000 hyko_sdk-0.2.0/hyko_sdk.egg-info/SOURCES.txt
+-rw-rw-r--   0 dahmadjid  (1005) docker     (999)        1 2023-07-23 12:53:47.000000 hyko_sdk-0.2.0/hyko_sdk.egg-info/dependency_links.txt
+-rw-rw-r--   0 dahmadjid  (1005) docker     (999)       62 2023-07-23 12:53:47.000000 hyko_sdk-0.2.0/hyko_sdk.egg-info/requires.txt
+-rw-rw-r--   0 dahmadjid  (1005) docker     (999)        9 2023-07-23 12:53:47.000000 hyko_sdk-0.2.0/hyko_sdk.egg-info/top_level.txt
+-rw-rw-r--   0 dahmadjid  (1005) docker     (999)       80 2023-07-23 09:57:30.000000 hyko_sdk-0.2.0/pyproject.toml
+-rw-rw-r--   0 dahmadjid  (1005) docker     (999)      387 2023-07-23 12:53:47.843647 hyko_sdk-0.2.0/setup.cfg
```

### Comparing `hyko_sdk-0.1.9/hyko_sdk/error.py` & `hyko_sdk-0.2.0/hyko_sdk/error.py`

 * *Files identical despite different names*

### Comparing `hyko_sdk-0.1.9/hyko_sdk/metadata.py` & `hyko_sdk-0.2.0/hyko_sdk/metadata.py`

 * *Files 4% similar despite different names*

```diff
@@ -28,14 +28,16 @@
             string_format = field_props.get("format")
 
             if string_format is not None:
                 if string_format == "image":
                     port_type = IOPortType.IMAGE
                 elif string_format == "audio":
                     port_type = IOPortType.AUDIO
+                elif string_format == "video":
+                    port_type = IOPortType.VIDEO
                 else:
                     port_type = IOPortType.STRING
             else:
                 port_type = IOPortType.STRING
         
         elif field_type == "array":
             try:
@@ -49,14 +51,16 @@
                     try:
                         string_format = field_props["items"]["format"]
                         
                         if string_format == "image":
                             port_type = IOPortType.ARRAY_IMAGE
                         elif string_format == "audio":
                             port_type = IOPortType.ARRAY_AUDIO
+                        elif string_format == "video":
+                            port_type = IOPortType.VIDEO
                         else:
                             continue
 
                     except:
                         port_type = IOPortType.ARRAY_STRING
                 else:
                     continue
@@ -86,7 +90,8 @@
     name: str
     description: str
     version: str
     category: str
     inputs: List[IOPort]
     outputs: List[IOPort]
     params: List[IOPort]
+    requires_gpu: bool
```

