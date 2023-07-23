# Comparing `tmp/AutoQPF-0.1.2.tar.gz` & `tmp/AutoQPF-0.1.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "AutoQPF-0.1.2.tar", last modified: Sun Jul 23 02:13:10 2023, max compression
+gzip compressed data, was "AutoQPF-0.1.3.tar", last modified: Sun Jul 23 02:29:10 2023, max compression
```

## Comparing `AutoQPF-0.1.2.tar` & `AutoQPF-0.1.3.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxrwxrwx   0        0        0        0 2023-07-23 02:13:10.569089 AutoQPF-0.1.2/
-drwxrwxrwx   0        0        0        0 2023-07-23 02:13:10.561575 AutoQPF-0.1.2/AutoQPF.egg-info/
--rw-rw-rw-   0        0        0     2289 2023-07-23 02:13:10.000000 AutoQPF-0.1.2/AutoQPF.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      244 2023-07-23 02:13:10.000000 AutoQPF-0.1.2/AutoQPF.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-23 02:13:10.000000 AutoQPF-0.1.2/AutoQPF.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       12 2023-07-23 02:13:10.000000 AutoQPF-0.1.2/AutoQPF.egg-info/requires.txt
--rw-rw-rw-   0        0        0        9 2023-07-23 02:13:10.000000 AutoQPF-0.1.2/AutoQPF.egg-info/top_level.txt
--rw-rw-rw-   0        0        0     1091 2023-07-22 05:44:21.000000 AutoQPF-0.1.2/LICENSE
--rw-rw-rw-   0        0        0     2289 2023-07-23 02:13:10.568083 AutoQPF-0.1.2/PKG-INFO
--rw-rw-rw-   0        0        0     1617 2023-07-22 21:26:58.000000 AutoQPF-0.1.2/README.md
-drwxrwxrwx   0        0        0        0 2023-07-23 02:13:10.567578 AutoQPF-0.1.2/auto_qpf/
--rw-rw-rw-   0        0        0       35 2023-07-23 02:12:13.000000 AutoQPF-0.1.2/auto_qpf/__init__.py
--rw-rw-rw-   0        0        0     6125 2023-07-22 21:27:05.000000 AutoQPF-0.1.2/auto_qpf/qpf.py
--rw-rw-rw-   0        0        0      257 2023-07-22 04:57:33.000000 AutoQPF-0.1.2/auto_qpf/qpf_exceptions.py
--rw-rw-rw-   0        0        0       42 2023-07-23 02:13:10.569089 AutoQPF-0.1.2/setup.cfg
--rw-rw-rw-   0        0        0      963 2023-07-23 02:12:57.000000 AutoQPF-0.1.2/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 02:29:10.716466 AutoQPF-0.1.3/
+drwxrwxrwx   0        0        0        0 2023-07-23 02:29:10.711464 AutoQPF-0.1.3/AutoQPF.egg-info/
+-rw-rw-rw-   0        0        0     2289 2023-07-23 02:29:10.000000 AutoQPF-0.1.3/AutoQPF.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      244 2023-07-23 02:29:10.000000 AutoQPF-0.1.3/AutoQPF.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 02:29:10.000000 AutoQPF-0.1.3/AutoQPF.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       12 2023-07-23 02:29:10.000000 AutoQPF-0.1.3/AutoQPF.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        9 2023-07-23 02:29:10.000000 AutoQPF-0.1.3/AutoQPF.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0     1091 2023-07-22 05:44:21.000000 AutoQPF-0.1.3/LICENSE
+-rw-rw-rw-   0        0        0     2289 2023-07-23 02:29:10.714466 AutoQPF-0.1.3/PKG-INFO
+-rw-rw-rw-   0        0        0     1617 2023-07-22 21:26:58.000000 AutoQPF-0.1.3/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 02:29:10.714466 AutoQPF-0.1.3/auto_qpf/
+-rw-rw-rw-   0        0        0      259 2023-07-23 02:27:06.000000 AutoQPF-0.1.3/auto_qpf/__init__.py
+-rw-rw-rw-   0        0        0     6125 2023-07-22 21:27:05.000000 AutoQPF-0.1.3/auto_qpf/qpf.py
+-rw-rw-rw-   0        0        0      257 2023-07-22 04:57:33.000000 AutoQPF-0.1.3/auto_qpf/qpf_exceptions.py
+-rw-rw-rw-   0        0        0       42 2023-07-23 02:29:10.716466 AutoQPF-0.1.3/setup.cfg
+-rw-rw-rw-   0        0        0      963 2023-07-23 02:23:21.000000 AutoQPF-0.1.3/setup.py
```

### Comparing `AutoQPF-0.1.2/AutoQPF.egg-info/PKG-INFO` & `AutoQPF-0.1.3/AutoQPF.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: AutoQPF
-Version: 0.1.2
+Version: 0.1.3
 Summary: Generates QPF frame time codes to be used with x264/x265
 Home-page: https://github.com/jlw4049/AutoQPF
 Author: Jessie Wilson
 Author-email: jessielw4049@gmail.com
 License: MIT
 Keywords: AutoQPF
 Classifier: Development Status :: 5 - Production/Stable
```

### Comparing `AutoQPF-0.1.2/LICENSE` & `AutoQPF-0.1.3/LICENSE`

 * *Files identical despite different names*

### Comparing `AutoQPF-0.1.2/PKG-INFO` & `AutoQPF-0.1.3/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: AutoQPF
-Version: 0.1.2
+Version: 0.1.3
 Summary: Generates QPF frame time codes to be used with x264/x265
 Home-page: https://github.com/jlw4049/AutoQPF
 Author: Jessie Wilson
 Author-email: jessielw4049@gmail.com
 License: MIT
 Keywords: AutoQPF
 Classifier: Development Status :: 5 - Production/Stable
```

### Comparing `AutoQPF-0.1.2/README.md` & `AutoQPF-0.1.3/README.md`

 * *Files identical despite different names*

### Comparing `AutoQPF-0.1.2/auto_qpf/qpf.py` & `AutoQPF-0.1.3/auto_qpf/qpf.py`

 * *Files identical despite different names*

### Comparing `AutoQPF-0.1.2/setup.py` & `AutoQPF-0.1.3/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -13,15 +13,15 @@
 ]
 
 with open(os.path.join(os.path.dirname(__file__), "README.md")) as fd:
     ext_long_desc = fd.read()
 
 setup(
     name="AutoQPF",
-    version="0.1.2",
+    version="0.1.3",
     description="Generates QPF frame time codes to be used with x264/x265",
     long_description=ext_long_desc,
     long_description_content_type="text/markdown",
     url="https://github.com/jlw4049/AutoQPF",
     author="Jessie Wilson",
     author_email="jessielw4049@gmail.com",
     license="MIT",
```

