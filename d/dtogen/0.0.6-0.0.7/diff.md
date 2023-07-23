# Comparing `tmp/dtogen-0.0.6.tar.gz` & `tmp/dtogen-0.0.7.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dtogen-0.0.6.tar", last modified: Sun Jul 23 05:57:47 2023, max compression
+gzip compressed data, was "dtogen-0.0.7.tar", last modified: Sun Jul 23 06:10:24 2023, max compression
```

## Comparing `dtogen-0.0.6.tar` & `dtogen-0.0.7.tar`

### file list

```diff
@@ -1,14 +1,30 @@
-drwxr-xr-x   0 mujdecisy   (501) staff       (20)        0 2023-07-23 05:57:47.944741 dtogen-0.0.6/
--rw-r--r--   0 mujdecisy   (501) staff       (20)     3099 2023-07-23 05:57:47.944578 dtogen-0.0.6/PKG-INFO
--rw-r--r--   0 mujdecisy   (501) staff       (20)     2777 2023-07-20 21:30:14.000000 dtogen-0.0.6/README.md
-drwxr-xr-x   0 mujdecisy   (501) staff       (20)        0 2023-07-23 05:57:47.944017 dtogen-0.0.6/dtogen.egg-info/
--rw-r--r--   0 mujdecisy   (501) staff       (20)     3099 2023-07-23 05:57:47.000000 dtogen-0.0.6/dtogen.egg-info/PKG-INFO
--rw-r--r--   0 mujdecisy   (501) staff       (20)      216 2023-07-23 05:57:47.000000 dtogen-0.0.6/dtogen.egg-info/SOURCES.txt
--rw-r--r--   0 mujdecisy   (501) staff       (20)        1 2023-07-23 05:57:47.000000 dtogen-0.0.6/dtogen.egg-info/dependency_links.txt
--rw-r--r--   0 mujdecisy   (501) staff       (20)       15 2023-07-23 05:57:47.000000 dtogen-0.0.6/dtogen.egg-info/requires.txt
--rw-r--r--   0 mujdecisy   (501) staff       (20)        1 2023-07-23 05:57:47.000000 dtogen-0.0.6/dtogen.egg-info/top_level.txt
--rw-r--r--   0 mujdecisy   (501) staff       (20)       38 2023-07-23 05:57:47.944795 dtogen-0.0.6/setup.cfg
--rw-r--r--   0 mujdecisy   (501) staff       (20)      737 2023-07-23 05:57:03.000000 dtogen-0.0.6/setup.py
-drwxr-xr-x   0 mujdecisy   (501) staff       (20)        0 2023-07-23 05:57:47.944361 dtogen-0.0.6/test/
--rw-r--r--   0 mujdecisy   (501) staff       (20)     1195 2023-07-22 06:17:14.000000 dtogen-0.0.6/test/test_dtogenerator.py
--rw-r--r--   0 mujdecisy   (501) staff       (20)     1285 2023-07-22 06:17:14.000000 dtogen-0.0.6/test/test_transform.py
+drwxr-xr-x   0 mujdecisy   (501) staff       (20)        0 2023-07-23 06:10:24.351123 dtogen-0.0.7/
+-rw-r--r--   0 mujdecisy   (501) staff       (20)     3099 2023-07-23 06:10:24.350935 dtogen-0.0.7/PKG-INFO
+-rw-r--r--   0 mujdecisy   (501) staff       (20)     2777 2023-07-20 21:30:14.000000 dtogen-0.0.7/README.md
+drwxr-xr-x   0 mujdecisy   (501) staff       (20)        0 2023-07-23 06:10:24.347393 dtogen-0.0.7/dtogen/
+-rw-r--r--   0 mujdecisy   (501) staff       (20)      934 2023-07-22 22:13:03.000000 dtogen-0.0.7/dtogen/__main__.py
+-rw-r--r--   0 mujdecisy   (501) staff       (20)     1620 2023-07-22 22:11:21.000000 dtogen-0.0.7/dtogen/dtogenerator.py
+drwxr-xr-x   0 mujdecisy   (501) staff       (20)        0 2023-07-23 06:10:24.349333 dtogen-0.0.7/dtogen/filewriters/
+-rw-r--r--   0 mujdecisy   (501) staff       (20)      183 2023-07-22 22:10:45.000000 dtogen-0.0.7/dtogen/filewriters/__init__.py
+-rw-r--r--   0 mujdecisy   (501) staff       (20)     2024 2023-07-22 22:12:24.000000 dtogen-0.0.7/dtogen/filewriters/filewriter.py
+-rw-r--r--   0 mujdecisy   (501) staff       (20)      567 2023-07-22 22:11:52.000000 dtogen-0.0.7/dtogen/filewriters/filewriter_java.py
+-rw-r--r--   0 mujdecisy   (501) staff       (20)      588 2023-07-22 22:12:03.000000 dtogen-0.0.7/dtogen/filewriters/filewriter_python.py
+-rw-r--r--   0 mujdecisy   (501) staff       (20)      558 2023-07-22 22:12:15.000000 dtogen-0.0.7/dtogen/filewriters/filewriter_typescript.py
+-rw-r--r--   0 mujdecisy   (501) staff       (20)      567 2023-07-20 21:12:11.000000 dtogen-0.0.7/dtogen/interfaces.py
+drwxr-xr-x   0 mujdecisy   (501) staff       (20)        0 2023-07-23 06:10:24.350338 dtogen-0.0.7/dtogen/transformers/
+-rw-r--r--   0 mujdecisy   (501) staff       (20)      191 2023-07-22 22:10:22.000000 dtogen-0.0.7/dtogen/transformers/__init__.py
+-rw-r--r--   0 mujdecisy   (501) staff       (20)     4518 2023-07-22 22:12:57.000000 dtogen-0.0.7/dtogen/transformers/transformer.py
+-rw-r--r--   0 mujdecisy   (501) staff       (20)      913 2023-07-22 22:11:38.000000 dtogen-0.0.7/dtogen/transformers/transformer_java.py
+-rw-r--r--   0 mujdecisy   (501) staff       (20)      805 2023-07-22 22:12:41.000000 dtogen-0.0.7/dtogen/transformers/transformer_python.py
+-rw-r--r--   0 mujdecisy   (501) staff       (20)      836 2023-07-22 22:12:49.000000 dtogen-0.0.7/dtogen/transformers/transformer_typescript.py
+drwxr-xr-x   0 mujdecisy   (501) staff       (20)        0 2023-07-23 06:10:24.348388 dtogen-0.0.7/dtogen.egg-info/
+-rw-r--r--   0 mujdecisy   (501) staff       (20)     3099 2023-07-23 06:10:24.000000 dtogen-0.0.7/dtogen.egg-info/PKG-INFO
+-rw-r--r--   0 mujdecisy   (501) staff       (20)      660 2023-07-23 06:10:24.000000 dtogen-0.0.7/dtogen.egg-info/SOURCES.txt
+-rw-r--r--   0 mujdecisy   (501) staff       (20)        1 2023-07-23 06:10:24.000000 dtogen-0.0.7/dtogen.egg-info/dependency_links.txt
+-rw-r--r--   0 mujdecisy   (501) staff       (20)       15 2023-07-23 06:10:24.000000 dtogen-0.0.7/dtogen.egg-info/requires.txt
+-rw-r--r--   0 mujdecisy   (501) staff       (20)        7 2023-07-23 06:10:24.000000 dtogen-0.0.7/dtogen.egg-info/top_level.txt
+-rw-r--r--   0 mujdecisy   (501) staff       (20)       38 2023-07-23 06:10:24.351174 dtogen-0.0.7/setup.cfg
+-rw-r--r--   0 mujdecisy   (501) staff       (20)      734 2023-07-23 06:10:05.000000 dtogen-0.0.7/setup.py
+drwxr-xr-x   0 mujdecisy   (501) staff       (20)        0 2023-07-23 06:10:24.350666 dtogen-0.0.7/test/
+-rw-r--r--   0 mujdecisy   (501) staff       (20)     1195 2023-07-22 06:17:14.000000 dtogen-0.0.7/test/test_dtogenerator.py
+-rw-r--r--   0 mujdecisy   (501) staff       (20)     1285 2023-07-22 06:17:14.000000 dtogen-0.0.7/test/test_transform.py
```

### Comparing `dtogen-0.0.6/PKG-INFO` & `dtogen-0.0.7/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dtogen
-Version: 0.0.6
+Version: 0.0.7
 Summary: DTO generator for Java, TypeScript, Python
 Home-page: https://github.com/mujdecisy/dtogen
 Author: mujdecisy
 Author-email: mujdecisy@gmail.com
 Keywords: python,DTO,generator
 Classifier: Programming Language :: Python :: 3
 Description-Content-Type: text/markdown
```

### Comparing `dtogen-0.0.6/README.md` & `dtogen-0.0.7/README.md`

 * *Files identical despite different names*

### Comparing `dtogen-0.0.6/dtogen.egg-info/PKG-INFO` & `dtogen-0.0.7/dtogen.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dtogen
-Version: 0.0.6
+Version: 0.0.7
 Summary: DTO generator for Java, TypeScript, Python
 Home-page: https://github.com/mujdecisy/dtogen
 Author: mujdecisy
 Author-email: mujdecisy@gmail.com
 Keywords: python,DTO,generator
 Classifier: Programming Language :: Python :: 3
 Description-Content-Type: text/markdown
```

### Comparing `dtogen-0.0.6/setup.py` & `dtogen-0.0.7/setup.py`

 * *Files 18% similar despite different names*

```diff
@@ -1,25 +1,25 @@
 import os.path
-from setuptools import setup, find_packages
+from setuptools import setup
 
 HERE = os.path.abspath(os.path.dirname(__file__))
 
 with open(os.path.join(HERE, "README.md")) as fid:
     README = fid.read()
 
 setup(
     name="dtogen",
-    version="0.0.6",
+    version="0.0.7",
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
-    packages=find_packages(exclude=["test", "test.*"]),
+    packages=['dtogen','dtogen.transformers','dtogen.filewriters'],
     include_package_data=True,
     install_requires=["mapperr", "pyyaml"],
 )
```

### Comparing `dtogen-0.0.6/test/test_dtogenerator.py` & `dtogen-0.0.7/test/test_dtogenerator.py`

 * *Files identical despite different names*

### Comparing `dtogen-0.0.6/test/test_transform.py` & `dtogen-0.0.7/test/test_transform.py`

 * *Files identical despite different names*

