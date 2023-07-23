# Comparing `tmp/dtogen-0.0.5.tar.gz` & `tmp/dtogen-0.0.6.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dtogen-0.0.5.tar", last modified: Sat Jul 22 22:19:21 2023, max compression
+gzip compressed data, was "dtogen-0.0.6.tar", last modified: Sun Jul 23 05:57:47 2023, max compression
```

## Comparing `dtogen-0.0.5.tar` & `dtogen-0.0.6.tar`

### file list

```diff
@@ -1,18 +1,14 @@
-drwxr-xr-x   0 mujdecisy   (501) staff       (20)        0 2023-07-22 22:19:21.756322 dtogen-0.0.5/
--rw-r--r--   0 mujdecisy   (501) staff       (20)     3099 2023-07-22 22:19:21.756081 dtogen-0.0.5/PKG-INFO
--rw-r--r--   0 mujdecisy   (501) staff       (20)     2777 2023-07-20 21:30:14.000000 dtogen-0.0.5/README.md
-drwxr-xr-x   0 mujdecisy   (501) staff       (20)        0 2023-07-22 22:19:21.754305 dtogen-0.0.5/dtogen/
--rw-r--r--   0 mujdecisy   (501) staff       (20)      934 2023-07-22 22:13:03.000000 dtogen-0.0.5/dtogen/__main__.py
--rw-r--r--   0 mujdecisy   (501) staff       (20)     1620 2023-07-22 22:11:21.000000 dtogen-0.0.5/dtogen/dtogenerator.py
--rw-r--r--   0 mujdecisy   (501) staff       (20)      567 2023-07-20 21:12:11.000000 dtogen-0.0.5/dtogen/interfaces.py
-drwxr-xr-x   0 mujdecisy   (501) staff       (20)        0 2023-07-22 22:19:21.755298 dtogen-0.0.5/dtogen.egg-info/
--rw-r--r--   0 mujdecisy   (501) staff       (20)     3099 2023-07-22 22:19:21.000000 dtogen-0.0.5/dtogen.egg-info/PKG-INFO
--rw-r--r--   0 mujdecisy   (501) staff       (20)      279 2023-07-22 22:19:21.000000 dtogen-0.0.5/dtogen.egg-info/SOURCES.txt
--rw-r--r--   0 mujdecisy   (501) staff       (20)        1 2023-07-22 22:19:21.000000 dtogen-0.0.5/dtogen.egg-info/dependency_links.txt
--rw-r--r--   0 mujdecisy   (501) staff       (20)       15 2023-07-22 22:19:21.000000 dtogen-0.0.5/dtogen.egg-info/requires.txt
--rw-r--r--   0 mujdecisy   (501) staff       (20)        7 2023-07-22 22:19:21.000000 dtogen-0.0.5/dtogen.egg-info/top_level.txt
--rw-r--r--   0 mujdecisy   (501) staff       (20)       38 2023-07-22 22:19:21.756376 dtogen-0.0.5/setup.cfg
--rw-r--r--   0 mujdecisy   (501) staff       (20)      691 2023-07-22 22:18:34.000000 dtogen-0.0.5/setup.py
-drwxr-xr-x   0 mujdecisy   (501) staff       (20)        0 2023-07-22 22:19:21.755759 dtogen-0.0.5/test/
--rw-r--r--   0 mujdecisy   (501) staff       (20)     1195 2023-07-22 06:17:14.000000 dtogen-0.0.5/test/test_dtogenerator.py
--rw-r--r--   0 mujdecisy   (501) staff       (20)     1285 2023-07-22 06:17:14.000000 dtogen-0.0.5/test/test_transform.py
+drwxr-xr-x   0 mujdecisy   (501) staff       (20)        0 2023-07-23 05:57:47.944741 dtogen-0.0.6/
+-rw-r--r--   0 mujdecisy   (501) staff       (20)     3099 2023-07-23 05:57:47.944578 dtogen-0.0.6/PKG-INFO
+-rw-r--r--   0 mujdecisy   (501) staff       (20)     2777 2023-07-20 21:30:14.000000 dtogen-0.0.6/README.md
+drwxr-xr-x   0 mujdecisy   (501) staff       (20)        0 2023-07-23 05:57:47.944017 dtogen-0.0.6/dtogen.egg-info/
+-rw-r--r--   0 mujdecisy   (501) staff       (20)     3099 2023-07-23 05:57:47.000000 dtogen-0.0.6/dtogen.egg-info/PKG-INFO
+-rw-r--r--   0 mujdecisy   (501) staff       (20)      216 2023-07-23 05:57:47.000000 dtogen-0.0.6/dtogen.egg-info/SOURCES.txt
+-rw-r--r--   0 mujdecisy   (501) staff       (20)        1 2023-07-23 05:57:47.000000 dtogen-0.0.6/dtogen.egg-info/dependency_links.txt
+-rw-r--r--   0 mujdecisy   (501) staff       (20)       15 2023-07-23 05:57:47.000000 dtogen-0.0.6/dtogen.egg-info/requires.txt
+-rw-r--r--   0 mujdecisy   (501) staff       (20)        1 2023-07-23 05:57:47.000000 dtogen-0.0.6/dtogen.egg-info/top_level.txt
+-rw-r--r--   0 mujdecisy   (501) staff       (20)       38 2023-07-23 05:57:47.944795 dtogen-0.0.6/setup.cfg
+-rw-r--r--   0 mujdecisy   (501) staff       (20)      737 2023-07-23 05:57:03.000000 dtogen-0.0.6/setup.py
+drwxr-xr-x   0 mujdecisy   (501) staff       (20)        0 2023-07-23 05:57:47.944361 dtogen-0.0.6/test/
+-rw-r--r--   0 mujdecisy   (501) staff       (20)     1195 2023-07-22 06:17:14.000000 dtogen-0.0.6/test/test_dtogenerator.py
+-rw-r--r--   0 mujdecisy   (501) staff       (20)     1285 2023-07-22 06:17:14.000000 dtogen-0.0.6/test/test_transform.py
```

### Comparing `dtogen-0.0.5/PKG-INFO` & `dtogen-0.0.6/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dtogen
-Version: 0.0.5
+Version: 0.0.6
 Summary: DTO generator for Java, TypeScript, Python
 Home-page: https://github.com/mujdecisy/dtogen
 Author: mujdecisy
 Author-email: mujdecisy@gmail.com
 Keywords: python,DTO,generator
 Classifier: Programming Language :: Python :: 3
 Description-Content-Type: text/markdown
```

### Comparing `dtogen-0.0.5/README.md` & `dtogen-0.0.6/README.md`

 * *Files identical despite different names*

### Comparing `dtogen-0.0.5/dtogen.egg-info/PKG-INFO` & `dtogen-0.0.6/dtogen.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dtogen
-Version: 0.0.5
+Version: 0.0.6
 Summary: DTO generator for Java, TypeScript, Python
 Home-page: https://github.com/mujdecisy/dtogen
 Author: mujdecisy
 Author-email: mujdecisy@gmail.com
 Keywords: python,DTO,generator
 Classifier: Programming Language :: Python :: 3
 Description-Content-Type: text/markdown
```

### Comparing `dtogen-0.0.5/setup.py` & `dtogen-0.0.6/setup.py`

 * *Files 19% similar despite different names*

```diff
@@ -1,25 +1,25 @@
 import os.path
-from setuptools import setup
+from setuptools import setup, find_packages
 
 HERE = os.path.abspath(os.path.dirname(__file__))
 
 with open(os.path.join(HERE, "README.md")) as fid:
     README = fid.read()
 
 setup(
     name="dtogen",
-    version="0.0.5",
+    version="0.0.6",
     description="DTO generator for Java, TypeScript, Python",
     long_description=README,
     long_description_content_type="text/markdown",
     url="https://github.com/mujdecisy/dtogen",
     keywords=["python", "DTO", "generator"],
     author="mujdecisy",
     author_email="mujdecisy@gmail.com",
     classifiers=[
         "Programming Language :: Python :: 3",
     ],
-    packages=["dtogen"],
+    packages=find_packages(exclude=["test", "test.*"]),
     include_package_data=True,
     install_requires=["mapperr", "pyyaml"],
 )
```

### Comparing `dtogen-0.0.5/test/test_dtogenerator.py` & `dtogen-0.0.6/test/test_dtogenerator.py`

 * *Files identical despite different names*

### Comparing `dtogen-0.0.5/test/test_transform.py` & `dtogen-0.0.6/test/test_transform.py`

 * *Files identical despite different names*

