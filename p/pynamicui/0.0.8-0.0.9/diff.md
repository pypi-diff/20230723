# Comparing `tmp/pynamicui-0.0.8.tar.gz` & `tmp/pynamicui-0.0.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "pynamicui-0.0.8.tar", last modified: Thu Jul 20 19:11:31 2023, max compression
+gzip compressed data, was "pynamicui-0.0.9.tar", last modified: Sun Jul 23 02:16:39 2023, max compression
```

## Comparing `pynamicui-0.0.8.tar` & `pynamicui-0.0.9.tar`

### file list

```diff
@@ -1,24 +1,24 @@
-drwxrwxrwx   0        0        0        0 2023-07-20 19:11:31.914916 pynamicui-0.0.8/
--rw-rw-rw-   0        0        0    11542 2023-07-18 06:19:12.000000 pynamicui-0.0.8/LICENSE
--rw-rw-rw-   0        0        0     7598 2023-07-20 19:11:31.911915 pynamicui-0.0.8/PKG-INFO
--rw-rw-rw-   0        0        0     7115 2023-07-19 21:40:59.000000 pynamicui-0.0.8/README.md
-drwxrwxrwx   0        0        0        0 2023-07-20 19:11:31.793864 pynamicui-0.0.8/pynamicui/
--rw-rw-rw-   0        0        0      318 2023-07-20 19:10:29.000000 pynamicui-0.0.8/pynamicui/__init__.py
-drwxrwxrwx   0        0        0        0 2023-07-20 19:11:31.892397 pynamicui-0.0.8/pynamicui/createDom/
--rw-rw-rw-   0        0        0       32 2023-07-18 06:04:50.000000 pynamicui-0.0.8/pynamicui/createDom/__init__.py
--rw-rw-rw-   0        0        0     2183 2023-07-19 05:26:39.000000 pynamicui-0.0.8/pynamicui/createDom/createDom.py
-drwxrwxrwx   0        0        0        0 2023-07-20 19:11:31.900905 pynamicui-0.0.8/pynamicui/createElement/
--rw-rw-rw-   0        0        0       40 2023-07-18 06:04:41.000000 pynamicui-0.0.8/pynamicui/createElement/__init__.py
--rw-rw-rw-   0        0        0     6549 2023-07-20 18:44:32.000000 pynamicui-0.0.8/pynamicui/createElement/createElement.py
-drwxrwxrwx   0        0        0        0 2023-07-20 19:11:31.905915 pynamicui-0.0.8/pynamicui/createStylesheet/
--rw-rw-rw-   0        0        0       46 2023-07-18 06:04:27.000000 pynamicui-0.0.8/pynamicui/createStylesheet/__init__.py
--rw-rw-rw-   0        0        0      522 2023-07-18 02:33:30.000000 pynamicui-0.0.8/pynamicui/createStylesheet/createStylesheet.py
-drwxrwxrwx   0        0        0        0 2023-07-20 19:11:31.871385 pynamicui-0.0.8/pynamicui.egg-info/
--rw-rw-rw-   0        0        0     7598 2023-07-20 19:11:31.000000 pynamicui-0.0.8/pynamicui.egg-info/PKG-INFO
--rw-rw-rw-   0        0        0      455 2023-07-20 19:11:31.000000 pynamicui-0.0.8/pynamicui.egg-info/SOURCES.txt
--rw-rw-rw-   0        0        0        1 2023-07-20 19:11:31.000000 pynamicui-0.0.8/pynamicui.egg-info/dependency_links.txt
--rw-rw-rw-   0        0        0       14 2023-07-20 19:11:31.000000 pynamicui-0.0.8/pynamicui.egg-info/requires.txt
--rw-rw-rw-   0        0        0       10 2023-07-20 19:11:31.000000 pynamicui-0.0.8/pynamicui.egg-info/top_level.txt
--rw-rw-rw-   0        0        0      775 2023-07-20 19:10:22.000000 pynamicui-0.0.8/pyproject.toml
--rw-rw-rw-   0        0        0       42 2023-07-20 19:11:31.915916 pynamicui-0.0.8/setup.cfg
--rw-rw-rw-   0        0        0      808 2023-07-20 19:10:06.000000 pynamicui-0.0.8/setup.py
+drwxrwxrwx   0        0        0        0 2023-07-23 02:16:39.758376 pynamicui-0.0.9/
+-rw-rw-rw-   0        0        0    11542 2023-07-18 06:19:12.000000 pynamicui-0.0.9/LICENSE
+-rw-rw-rw-   0        0        0     7598 2023-07-23 02:16:39.756380 pynamicui-0.0.9/PKG-INFO
+-rw-rw-rw-   0        0        0     7115 2023-07-19 21:40:59.000000 pynamicui-0.0.9/README.md
+drwxrwxrwx   0        0        0        0 2023-07-23 02:16:39.677227 pynamicui-0.0.9/pynamicui/
+-rw-rw-rw-   0        0        0      752 2023-07-23 02:11:12.000000 pynamicui-0.0.9/pynamicui/__init__.py
+drwxrwxrwx   0        0        0        0 2023-07-23 02:16:39.737242 pynamicui-0.0.9/pynamicui/createDom/
+-rw-rw-rw-   0        0        0       32 2023-07-18 06:04:50.000000 pynamicui-0.0.9/pynamicui/createDom/__init__.py
+-rw-rw-rw-   0        0        0     2183 2023-07-19 05:26:39.000000 pynamicui-0.0.9/pynamicui/createDom/createDom.py
+drwxrwxrwx   0        0        0        0 2023-07-23 02:16:39.745377 pynamicui-0.0.9/pynamicui/createElement/
+-rw-rw-rw-   0        0        0       40 2023-07-18 06:04:41.000000 pynamicui-0.0.9/pynamicui/createElement/__init__.py
+-rw-rw-rw-   0        0        0    11791 2023-07-23 01:28:16.000000 pynamicui-0.0.9/pynamicui/createElement/createElement.py
+drwxrwxrwx   0        0        0        0 2023-07-23 02:16:39.752373 pynamicui-0.0.9/pynamicui/createStylesheet/
+-rw-rw-rw-   0        0        0       46 2023-07-18 06:04:27.000000 pynamicui-0.0.9/pynamicui/createStylesheet/__init__.py
+-rw-rw-rw-   0        0        0      522 2023-07-18 02:33:30.000000 pynamicui-0.0.9/pynamicui/createStylesheet/createStylesheet.py
+drwxrwxrwx   0        0        0        0 2023-07-23 02:16:39.729256 pynamicui-0.0.9/pynamicui.egg-info/
+-rw-rw-rw-   0        0        0     7598 2023-07-23 02:16:39.000000 pynamicui-0.0.9/pynamicui.egg-info/PKG-INFO
+-rw-rw-rw-   0        0        0      455 2023-07-23 02:16:39.000000 pynamicui-0.0.9/pynamicui.egg-info/SOURCES.txt
+-rw-rw-rw-   0        0        0        1 2023-07-23 02:16:39.000000 pynamicui-0.0.9/pynamicui.egg-info/dependency_links.txt
+-rw-rw-rw-   0        0        0       14 2023-07-23 02:16:39.000000 pynamicui-0.0.9/pynamicui.egg-info/requires.txt
+-rw-rw-rw-   0        0        0       10 2023-07-23 02:16:39.000000 pynamicui-0.0.9/pynamicui.egg-info/top_level.txt
+-rw-rw-rw-   0        0        0      775 2023-07-23 02:02:01.000000 pynamicui-0.0.9/pyproject.toml
+-rw-rw-rw-   0        0        0       42 2023-07-23 02:16:39.758376 pynamicui-0.0.9/setup.cfg
+-rw-rw-rw-   0        0        0      808 2023-07-23 02:02:05.000000 pynamicui-0.0.9/setup.py
```

### Comparing `pynamicui-0.0.8/LICENSE` & `pynamicui-0.0.9/LICENSE`

 * *Files identical despite different names*

### Comparing `pynamicui-0.0.8/PKG-INFO` & `pynamicui-0.0.9/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pynamicui
-Version: 0.0.8
+Version: 0.0.9
 Summary: dynamic web-like UIs using a declarative syntax
 Home-page: https://github.com/zacharie410/PynamicUI
 Author: zacharie410
 License: Apache Software License
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3 :: Only
```

### Comparing `pynamicui-0.0.8/README.md` & `pynamicui-0.0.9/README.md`

 * *Files identical despite different names*

### Comparing `pynamicui-0.0.8/pynamicui/createDom/createDom.py` & `pynamicui-0.0.9/pynamicui/createDom/createDom.py`

 * *Files identical despite different names*

### Comparing `pynamicui-0.0.8/pynamicui/createStylesheet/createStylesheet.py` & `pynamicui-0.0.9/pynamicui/createStylesheet/createStylesheet.py`

 * *Files identical despite different names*

### Comparing `pynamicui-0.0.8/pynamicui.egg-info/PKG-INFO` & `pynamicui-0.0.9/pynamicui.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: pynamicui
-Version: 0.0.8
+Version: 0.0.9
 Summary: dynamic web-like UIs using a declarative syntax
 Home-page: https://github.com/zacharie410/PynamicUI
 Author: zacharie410
 License: Apache Software License
 Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Operating System :: OS Independent
 Classifier: Programming Language :: Python :: 3 :: Only
```

### Comparing `pynamicui-0.0.8/pyproject.toml` & `pynamicui-0.0.9/pyproject.toml`

 * *Files 1% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 requires = ["setuptools", "wheel"]
 build-backend = "setuptools.build_meta"
 
 [tool.tbump]
 github_url = "https://github.com/zacharie410/PynamicUI"
 
 [tool.tbump.version]
-current = "0.0.8"
+current = "0.0.9"
 
 # Example of a semver regexp.
 # Make sure this matches current_version before
 # using tbump
 regex = '''
   (?P<major>\d+)
   \.
```

### Comparing `pynamicui-0.0.8/setup.py` & `pynamicui-0.0.9/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -1,15 +1,15 @@
 import setuptools
 
 with open('README.md', 'r', encoding='utf-8') as f:
     long_description = f.read()
 
 setuptools.setup(
     name='pynamicui',
-    version='0.0.8',
+    version='0.0.9',
     description='dynamic web-like UIs using a declarative syntax',
     long_description=long_description,
     long_description_content_type='text/markdown',
     url='https://github.com/zacharie410/PynamicUI',
     author='zacharie410',
     license='Apache Software License',
     classifiers=[
```

