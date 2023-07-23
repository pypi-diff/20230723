# Comparing `tmp/ece4078-1.0.8.tar.gz` & `tmp/ece4078-1.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "ece4078-1.0.8.tar", last modified: Sun Jul 23 04:13:27 2023, max compression
+gzip compressed data, was "ece4078-1.0.9.tar", last modified: Sun Jul 23 04:28:32 2023, max compression
```

## Comparing `ece4078-1.0.8.tar` & `ece4078-1.0.9.tar`

### file list

```diff
@@ -1,27 +1,27 @@
-drwxr-xr-x   0 tinsirius  (1000) tinsirius  (1000)        0 2023-07-23 04:13:27.926854 ece4078-1.0.8/
--rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)     1066 2023-07-23 03:51:35.000000 ece4078-1.0.8/LICENSE
--rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)      178 2023-07-23 04:13:27.926854 ece4078-1.0.8/PKG-INFO
--rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)      431 2023-07-23 03:51:35.000000 ece4078-1.0.8/README.md
--rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)       38 2023-07-23 04:13:27.926854 ece4078-1.0.8/setup.cfg
--rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)      457 2023-07-23 04:12:58.000000 ece4078-1.0.8/setup.py
-drwxr-xr-x   0 tinsirius  (1000) tinsirius  (1000)        0 2023-07-23 04:13:27.922854 ece4078-1.0.8/src/
-drwxr-xr-x   0 tinsirius  (1000) tinsirius  (1000)        0 2023-07-23 04:13:27.922854 ece4078-1.0.8/src/ece4078/
--rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)     1751 2023-07-23 04:00:32.000000 ece4078-1.0.8/src/ece4078/NotebookChecker.py
--rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)    10007 2023-07-23 03:51:35.000000 ece4078-1.0.8/src/ece4078/Utility.py
-drwxr-xr-x   0 tinsirius  (1000) tinsirius  (1000)        0 2023-07-23 04:13:27.922854 ece4078-1.0.8/src/ece4078/Week02/
--rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)     8158 2023-07-23 03:51:35.000000 ece4078-1.0.8/src/ece4078/Week02/Renderer.py
--rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)       23 2023-07-23 03:51:35.000000 ece4078-1.0.8/src/ece4078/Week02/__init__.py
-drwxr-xr-x   0 tinsirius  (1000) tinsirius  (1000)        0 2023-07-23 04:13:27.926854 ece4078-1.0.8/src/ece4078/Week03/
--rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)     6082 2023-07-23 03:51:35.000000 ece4078-1.0.8/src/ece4078/Week03/Obstacle.py
--rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)      107 2023-07-23 03:51:35.000000 ece4078-1.0.8/src/ece4078/Week03/__init__.py
--rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)     6153 2023-07-23 03:51:35.000000 ece4078-1.0.8/src/ece4078/Week03/math_functions.py
--rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)     7553 2023-07-23 03:51:35.000000 ece4078-1.0.8/src/ece4078/Week03/path_animation.py
--rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)     2478 2023-07-23 03:51:35.000000 ece4078-1.0.8/src/ece4078/Week03/path_search.py
--rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)       52 2023-07-23 04:12:43.000000 ece4078-1.0.8/src/ece4078/__init__.py
--rwxr-xr-x   0 tinsirius  (1000) tinsirius  (1000)      869 2023-07-23 03:51:35.000000 ece4078-1.0.8/src/ece4078/install_nginx
--rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)      597 2023-07-23 03:51:35.000000 ece4078-1.0.8/src/ece4078/nginx-meshcat-proxy.conf
-drwxr-xr-x   0 tinsirius  (1000) tinsirius  (1000)        0 2023-07-23 04:13:27.922854 ece4078-1.0.8/src/ece4078.egg-info/
--rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)      178 2023-07-23 04:13:27.000000 ece4078-1.0.8/src/ece4078.egg-info/PKG-INFO
--rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)      539 2023-07-23 04:13:27.000000 ece4078-1.0.8/src/ece4078.egg-info/SOURCES.txt
--rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)        1 2023-07-23 04:13:27.000000 ece4078-1.0.8/src/ece4078.egg-info/dependency_links.txt
--rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)        8 2023-07-23 04:13:27.000000 ece4078-1.0.8/src/ece4078.egg-info/top_level.txt
+drwxr-xr-x   0 tinsirius  (1000) tinsirius  (1000)        0 2023-07-23 04:28:32.899456 ece4078-1.0.9/
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)     1066 2023-07-23 03:51:35.000000 ece4078-1.0.9/LICENSE
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)      178 2023-07-23 04:28:32.899456 ece4078-1.0.9/PKG-INFO
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)      431 2023-07-23 03:51:35.000000 ece4078-1.0.9/README.md
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)       38 2023-07-23 04:28:32.899456 ece4078-1.0.9/setup.cfg
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)      457 2023-07-23 04:28:13.000000 ece4078-1.0.9/setup.py
+drwxr-xr-x   0 tinsirius  (1000) tinsirius  (1000)        0 2023-07-23 04:28:32.895456 ece4078-1.0.9/src/
+drwxr-xr-x   0 tinsirius  (1000) tinsirius  (1000)        0 2023-07-23 04:28:32.899456 ece4078-1.0.9/src/ece4078/
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)     1850 2023-07-23 04:27:32.000000 ece4078-1.0.9/src/ece4078/NotebookChecker.py
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)    10007 2023-07-23 03:51:35.000000 ece4078-1.0.9/src/ece4078/Utility.py
+drwxr-xr-x   0 tinsirius  (1000) tinsirius  (1000)        0 2023-07-23 04:28:32.899456 ece4078-1.0.9/src/ece4078/Week02/
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)     8158 2023-07-23 03:51:35.000000 ece4078-1.0.9/src/ece4078/Week02/Renderer.py
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)       23 2023-07-23 03:51:35.000000 ece4078-1.0.9/src/ece4078/Week02/__init__.py
+drwxr-xr-x   0 tinsirius  (1000) tinsirius  (1000)        0 2023-07-23 04:28:32.899456 ece4078-1.0.9/src/ece4078/Week03/
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)     6082 2023-07-23 03:51:35.000000 ece4078-1.0.9/src/ece4078/Week03/Obstacle.py
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)      107 2023-07-23 03:51:35.000000 ece4078-1.0.9/src/ece4078/Week03/__init__.py
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)     6153 2023-07-23 03:51:35.000000 ece4078-1.0.9/src/ece4078/Week03/math_functions.py
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)     7553 2023-07-23 03:51:35.000000 ece4078-1.0.9/src/ece4078/Week03/path_animation.py
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)     2478 2023-07-23 03:51:35.000000 ece4078-1.0.9/src/ece4078/Week03/path_search.py
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)       52 2023-07-23 04:12:43.000000 ece4078-1.0.9/src/ece4078/__init__.py
+-rwxr-xr-x   0 tinsirius  (1000) tinsirius  (1000)      869 2023-07-23 03:51:35.000000 ece4078-1.0.9/src/ece4078/install_nginx
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)      597 2023-07-23 03:51:35.000000 ece4078-1.0.9/src/ece4078/nginx-meshcat-proxy.conf
+drwxr-xr-x   0 tinsirius  (1000) tinsirius  (1000)        0 2023-07-23 04:28:32.899456 ece4078-1.0.9/src/ece4078.egg-info/
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)      178 2023-07-23 04:28:32.000000 ece4078-1.0.9/src/ece4078.egg-info/PKG-INFO
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)      539 2023-07-23 04:28:32.000000 ece4078-1.0.9/src/ece4078.egg-info/SOURCES.txt
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)        1 2023-07-23 04:28:32.000000 ece4078-1.0.9/src/ece4078.egg-info/dependency_links.txt
+-rw-r--r--   0 tinsirius  (1000) tinsirius  (1000)        8 2023-07-23 04:28:32.000000 ece4078-1.0.9/src/ece4078.egg-info/top_level.txt
```

### Comparing `ece4078-1.0.8/LICENSE` & `ece4078-1.0.9/LICENSE`

 * *Files identical despite different names*

### Comparing `ece4078-1.0.8/src/ece4078/NotebookChecker.py` & `ece4078-1.0.9/src/ece4078/NotebookChecker.py`

 * *Files 14% similar despite different names*

```diff
@@ -7,18 +7,18 @@
 def intro(vis):
     secret_msg = ["Hello", "students", "welcome", "to", "ECE4078"]
     w_slider = widgets.IntSlider(value=0, min=0, max=len(secret_msg)-1, step=1, description='Omega',
                                                 continuous_update=False)
     
     size = 8
     def f(change):
-        vis["render"].set_object(g.SceneText(secret_msg[change],
-					width=size,
-					height=size,
-					font_size = size))
+        vis["render"].set_object(g.SceneText(secret_msg[change], width=size, height=size, font_size = size))
+    interactive_plot = widgets.interactive_output(f, {'change': w_slider})
+    return interactive_plot, w_slider
+
 
 def NotebookChecker(vis):
     w_slider = widgets.IntSlider(value=0, min=0, max=10, step=1, description='Omega',
                                                 continuous_update=False)
     def f(change):
         fig = plt.figure(figsize=(5, 5))
         ax = plt.gca()
```

### Comparing `ece4078-1.0.8/src/ece4078/Utility.py` & `ece4078-1.0.9/src/ece4078/Utility.py`

 * *Files identical despite different names*

### Comparing `ece4078-1.0.8/src/ece4078/Week02/Renderer.py` & `ece4078-1.0.9/src/ece4078/Week02/Renderer.py`

 * *Files identical despite different names*

### Comparing `ece4078-1.0.8/src/ece4078/Week03/Obstacle.py` & `ece4078-1.0.9/src/ece4078/Week03/Obstacle.py`

 * *Files identical despite different names*

### Comparing `ece4078-1.0.8/src/ece4078/Week03/math_functions.py` & `ece4078-1.0.9/src/ece4078/Week03/math_functions.py`

 * *Files identical despite different names*

### Comparing `ece4078-1.0.8/src/ece4078/Week03/path_animation.py` & `ece4078-1.0.9/src/ece4078/Week03/path_animation.py`

 * *Files identical despite different names*

### Comparing `ece4078-1.0.8/src/ece4078/Week03/path_search.py` & `ece4078-1.0.9/src/ece4078/Week03/path_search.py`

 * *Files identical despite different names*

### Comparing `ece4078-1.0.8/src/ece4078/install_nginx` & `ece4078-1.0.9/src/ece4078/install_nginx`

 * *Files identical despite different names*

### Comparing `ece4078-1.0.8/src/ece4078/nginx-meshcat-proxy.conf` & `ece4078-1.0.9/src/ece4078/nginx-meshcat-proxy.conf`

 * *Files identical despite different names*

### Comparing `ece4078-1.0.8/src/ece4078.egg-info/SOURCES.txt` & `ece4078-1.0.9/src/ece4078.egg-info/SOURCES.txt`

 * *Files identical despite different names*

