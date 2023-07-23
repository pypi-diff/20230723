# Comparing `tmp/AutoQPF-0.1.0.tar.gz` & `tmp/AutoQPF-0.1.1.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "AutoQPF-0.1.0.tar", last modified: Sat Jul 22 21:28:44 2023, max compression
+gzip compressed data, was "AutoQPF-0.1.1.tar", last modified: Sun Jul 23 01:30:01 2023, max compression
```

## Comparing `AutoQPF-0.1.0.tar` & `AutoQPF-0.1.1.tar`

### file list

```diff
@@ -1,16 +1,16 @@
-drwxrwxrwx   0        0        0        0 2023-07-22 21:28:44.966891 AutoQPF-0.1.0/
-drwxrwxrwx   0        0        0        0 2023-07-22 21:28:44.962892 AutoQPF-0.1.0/AutoQPF.egg-info/
--rw-rw-rw-   0        0        0     2289 2023-07-22 21:28:44.000000 AutoQPF-0.1.0/AutoQPF.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      244 2023-07-22 21:28:44.000000 AutoQPF-0.1.0/AutoQPF.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-22 21:28:44.000000 AutoQPF-0.1.0/AutoQPF.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       12 2023-07-22 21:28:44.000000 AutoQPF-0.1.0/AutoQPF.egg-info/requires.txt
--rw-rw-rw-   0        0        0        9 2023-07-22 21:28:44.000000 AutoQPF-0.1.0/AutoQPF.egg-info/top_level.txt
--rw-rw-rw-   0        0        0     1091 2023-07-22 05:44:21.000000 AutoQPF-0.1.0/LICENSE
--rw-rw-rw-   0        0        0     2289 2023-07-22 21:28:44.964891 AutoQPF-0.1.0/PKG-INFO
--rw-rw-rw-   0        0        0     1617 2023-07-22 21:26:58.000000 AutoQPF-0.1.0/README.md
-drwxrwxrwx   0        0        0        0 2023-07-22 21:28:44.963891 AutoQPF-0.1.0/auto_qpf/
--rw-rw-rw-   0        0        0        0 2023-07-22 01:30:41.000000 AutoQPF-0.1.0/auto_qpf/__init__.py
--rw-rw-rw-   0        0        0     6125 2023-07-22 21:27:05.000000 AutoQPF-0.1.0/auto_qpf/qpf.py
--rw-rw-rw-   0        0        0      257 2023-07-22 04:57:33.000000 AutoQPF-0.1.0/auto_qpf/qpf_exceptions.py
--rw-rw-rw-   0        0        0       42 2023-07-22 21:28:44.966891 AutoQPF-0.1.0/setup.cfg
--rw-rw-rw-   0        0        0      963 2023-07-22 21:26:52.000000 AutoQPF-0.1.0/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 01:30:01.090718 AutoQPF-0.1.1/
+drwxrwxrwx   0        0        0        0 2023-07-23 01:30:01.086639 AutoQPF-0.1.1/AutoQPF.egg-info/
+-rw-rw-rw-   0        0        0     2289 2023-07-23 01:30:01.000000 AutoQPF-0.1.1/AutoQPF.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      244 2023-07-23 01:30:01.000000 AutoQPF-0.1.1/AutoQPF.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 01:30:01.000000 AutoQPF-0.1.1/AutoQPF.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       12 2023-07-23 01:30:01.000000 AutoQPF-0.1.1/AutoQPF.egg-info/requires.txt
+-rw-rw-rw-   0        0        0        9 2023-07-23 01:30:01.000000 AutoQPF-0.1.1/AutoQPF.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0     1091 2023-07-22 05:44:21.000000 AutoQPF-0.1.1/LICENSE
+-rw-rw-rw-   0        0        0     2289 2023-07-23 01:30:01.089717 AutoQPF-0.1.1/PKG-INFO
+-rw-rw-rw-   0        0        0     1617 2023-07-22 21:26:58.000000 AutoQPF-0.1.1/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 01:30:01.088710 AutoQPF-0.1.1/auto_qpf/
+-rw-rw-rw-   0        0        0      120 2023-07-23 01:27:33.000000 AutoQPF-0.1.1/auto_qpf/__init__.py
+-rw-rw-rw-   0        0        0     6125 2023-07-22 21:27:05.000000 AutoQPF-0.1.1/auto_qpf/qpf.py
+-rw-rw-rw-   0        0        0      257 2023-07-22 04:57:33.000000 AutoQPF-0.1.1/auto_qpf/qpf_exceptions.py
+-rw-rw-rw-   0        0        0       42 2023-07-23 01:30:01.090718 AutoQPF-0.1.1/setup.cfg
+-rw-rw-rw-   0        0        0      963 2023-07-23 01:27:38.000000 AutoQPF-0.1.1/setup.py
```

### Comparing `AutoQPF-0.1.0/AutoQPF.egg-info/PKG-INFO` & `AutoQPF-0.1.1/AutoQPF.egg-info/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: AutoQPF
-Version: 0.1.0
+Version: 0.1.1
 Summary: Generates QPF frame time codes to be used with x264/x265
 Home-page: https://github.com/jlw4049/AutoQPF
 Author: Jessie Wilson
 Author-email: jessielw4049@gmail.com
 License: MIT
 Keywords: AutoQPF
 Classifier: Development Status :: 5 - Production/Stable
```

### Comparing `AutoQPF-0.1.0/LICENSE` & `AutoQPF-0.1.1/LICENSE`

 * *Files identical despite different names*

### Comparing `AutoQPF-0.1.0/PKG-INFO` & `AutoQPF-0.1.1/PKG-INFO`

 * *Files 1% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: AutoQPF
-Version: 0.1.0
+Version: 0.1.1
 Summary: Generates QPF frame time codes to be used with x264/x265
 Home-page: https://github.com/jlw4049/AutoQPF
 Author: Jessie Wilson
 Author-email: jessielw4049@gmail.com
 License: MIT
 Keywords: AutoQPF
 Classifier: Development Status :: 5 - Production/Stable
```

### Comparing `AutoQPF-0.1.0/README.md` & `AutoQPF-0.1.1/README.md`

 * *Files identical despite different names*

### Comparing `AutoQPF-0.1.0/auto_qpf/qpf.py` & `AutoQPF-0.1.1/auto_qpf/qpf.py`

 * *Files identical despite different names*

### Comparing `AutoQPF-0.1.0/setup.py` & `AutoQPF-0.1.1/setup.py`

 * *Files 1% similar despite different names*

```diff
@@ -13,15 +13,15 @@
 ]
 
 with open(os.path.join(os.path.dirname(__file__), "README.md")) as fd:
     ext_long_desc = fd.read()
 
 setup(
     name="AutoQPF",
-    version="0.1.0",
+    version="0.1.1",
     description="Generates QPF frame time codes to be used with x264/x265",
     long_description=ext_long_desc,
     long_description_content_type="text/markdown",
     url="https://github.com/jlw4049/AutoQPF",
     author="Jessie Wilson",
     author_email="jessielw4049@gmail.com",
     license="MIT",
```

