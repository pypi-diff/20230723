# Comparing `tmp/dtogen-0.0.4.tar.gz` & `tmp/dtogen-0.0.5.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dtogen-0.0.4.tar", last modified: Fri Jul 21 21:23:03 2023, max compression
+gzip compressed data, was "dtogen-0.0.5.tar", last modified: Sat Jul 22 22:19:21 2023, max compression
```

## Comparing `dtogen-0.0.4.tar` & `dtogen-0.0.5.tar`

### file list

```diff
@@ -1,18 +1,18 @@
-drwxr-xr-x   0 mujdecisy   (501) staff       (20)        0 2023-07-21 21:23:03.648725 dtogen-0.0.4/
--rw-r--r--   0 mujdecisy   (501) staff       (20)     3099 2023-07-21 21:23:03.648554 dtogen-0.0.4/PKG-INFO
--rw-r--r--   0 mujdecisy   (501) staff       (20)     2777 2023-07-20 21:30:14.000000 dtogen-0.0.4/README.md
-drwxr-xr-x   0 mujdecisy   (501) staff       (20)        0 2023-07-21 21:23:03.646927 dtogen-0.0.4/dtogen/
--rw-r--r--   0 mujdecisy   (501) staff       (20)      940 2023-07-21 21:22:29.000000 dtogen-0.0.4/dtogen/__main__.py
--rw-r--r--   0 mujdecisy   (501) staff       (20)     1917 2023-07-21 21:21:13.000000 dtogen-0.0.4/dtogen/dtogenerator.py
--rw-r--r--   0 mujdecisy   (501) staff       (20)      567 2023-07-20 21:12:11.000000 dtogen-0.0.4/dtogen/interfaces.py
-drwxr-xr-x   0 mujdecisy   (501) staff       (20)        0 2023-07-21 21:23:03.647959 dtogen-0.0.4/dtogen.egg-info/
--rw-r--r--   0 mujdecisy   (501) staff       (20)     3099 2023-07-21 21:23:03.000000 dtogen-0.0.4/dtogen.egg-info/PKG-INFO
--rw-r--r--   0 mujdecisy   (501) staff       (20)      279 2023-07-21 21:23:03.000000 dtogen-0.0.4/dtogen.egg-info/SOURCES.txt
--rw-r--r--   0 mujdecisy   (501) staff       (20)        1 2023-07-21 21:23:03.000000 dtogen-0.0.4/dtogen.egg-info/dependency_links.txt
--rw-r--r--   0 mujdecisy   (501) staff       (20)       15 2023-07-21 21:23:03.000000 dtogen-0.0.4/dtogen.egg-info/requires.txt
--rw-r--r--   0 mujdecisy   (501) staff       (20)        7 2023-07-21 21:23:03.000000 dtogen-0.0.4/dtogen.egg-info/top_level.txt
--rw-r--r--   0 mujdecisy   (501) staff       (20)       38 2023-07-21 21:23:03.648773 dtogen-0.0.4/setup.cfg
--rw-r--r--   0 mujdecisy   (501) staff       (20)      691 2023-07-21 21:22:34.000000 dtogen-0.0.4/setup.py
-drwxr-xr-x   0 mujdecisy   (501) staff       (20)        0 2023-07-21 21:23:03.648325 dtogen-0.0.4/test/
--rw-r--r--   0 mujdecisy   (501) staff       (20)     1195 2023-07-21 21:13:23.000000 dtogen-0.0.4/test/test_dtogenerator.py
--rw-r--r--   0 mujdecisy   (501) staff       (20)     1285 2023-07-21 21:13:23.000000 dtogen-0.0.4/test/test_transform.py
+drwxr-xr-x   0 mujdecisy   (501) staff       (20)        0 2023-07-22 22:19:21.756322 dtogen-0.0.5/
+-rw-r--r--   0 mujdecisy   (501) staff       (20)     3099 2023-07-22 22:19:21.756081 dtogen-0.0.5/PKG-INFO
+-rw-r--r--   0 mujdecisy   (501) staff       (20)     2777 2023-07-20 21:30:14.000000 dtogen-0.0.5/README.md
+drwxr-xr-x   0 mujdecisy   (501) staff       (20)        0 2023-07-22 22:19:21.754305 dtogen-0.0.5/dtogen/
+-rw-r--r--   0 mujdecisy   (501) staff       (20)      934 2023-07-22 22:13:03.000000 dtogen-0.0.5/dtogen/__main__.py
+-rw-r--r--   0 mujdecisy   (501) staff       (20)     1620 2023-07-22 22:11:21.000000 dtogen-0.0.5/dtogen/dtogenerator.py
+-rw-r--r--   0 mujdecisy   (501) staff       (20)      567 2023-07-20 21:12:11.000000 dtogen-0.0.5/dtogen/interfaces.py
+drwxr-xr-x   0 mujdecisy   (501) staff       (20)        0 2023-07-22 22:19:21.755298 dtogen-0.0.5/dtogen.egg-info/
+-rw-r--r--   0 mujdecisy   (501) staff       (20)     3099 2023-07-22 22:19:21.000000 dtogen-0.0.5/dtogen.egg-info/PKG-INFO
+-rw-r--r--   0 mujdecisy   (501) staff       (20)      279 2023-07-22 22:19:21.000000 dtogen-0.0.5/dtogen.egg-info/SOURCES.txt
+-rw-r--r--   0 mujdecisy   (501) staff       (20)        1 2023-07-22 22:19:21.000000 dtogen-0.0.5/dtogen.egg-info/dependency_links.txt
+-rw-r--r--   0 mujdecisy   (501) staff       (20)       15 2023-07-22 22:19:21.000000 dtogen-0.0.5/dtogen.egg-info/requires.txt
+-rw-r--r--   0 mujdecisy   (501) staff       (20)        7 2023-07-22 22:19:21.000000 dtogen-0.0.5/dtogen.egg-info/top_level.txt
+-rw-r--r--   0 mujdecisy   (501) staff       (20)       38 2023-07-22 22:19:21.756376 dtogen-0.0.5/setup.cfg
+-rw-r--r--   0 mujdecisy   (501) staff       (20)      691 2023-07-22 22:18:34.000000 dtogen-0.0.5/setup.py
+drwxr-xr-x   0 mujdecisy   (501) staff       (20)        0 2023-07-22 22:19:21.755759 dtogen-0.0.5/test/
+-rw-r--r--   0 mujdecisy   (501) staff       (20)     1195 2023-07-22 06:17:14.000000 dtogen-0.0.5/test/test_dtogenerator.py
+-rw-r--r--   0 mujdecisy   (501) staff       (20)     1285 2023-07-22 06:17:14.000000 dtogen-0.0.5/test/test_transform.py
```

### Comparing `dtogen-0.0.4/PKG-INFO` & `dtogen-0.0.5/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dtogen
-Version: 0.0.4
+Version: 0.0.5
 Summary: DTO generator for Java, TypeScript, Python
 Home-page: https://github.com/mujdecisy/dtogen
 Author: mujdecisy
 Author-email: mujdecisy@gmail.com
 Keywords: python,DTO,generator
 Classifier: Programming Language :: Python :: 3
 Description-Content-Type: text/markdown
```

### Comparing `dtogen-0.0.4/README.md` & `dtogen-0.0.5/README.md`

 * *Files identical despite different names*

### Comparing `dtogen-0.0.4/dtogen/__main__.py` & `dtogen-0.0.5/dtogen/__main__.py`

 * *Files 12% similar despite different names*

```diff
@@ -1,9 +1,9 @@
 import argparse
-from dtogen.dtogenerator import DtoGenerator
+from .dtogenerator import DtoGenerator
 
 
 arg_parser = argparse.ArgumentParser(description="Generate DTOs from a YAML file")
 arg_parser.add_argument(
     "-i", "--input", metavar="INPUT", type=str, required=True, help="input YAML file"
 )
 arg_parser.add_argument(
```

### Comparing `dtogen-0.0.4/dtogen/dtogenerator.py` & `dtogen-0.0.5/dtogen/dtogenerator.py`

 * *Files 22% similar despite different names*

```diff
@@ -1,20 +1,24 @@
-from dtogen.transformers.transformer import Transformer
-from dtogen.transformers.transformer_java import TransformerJava
-from dtogen.transformers.transformer_python import TransformerPython
-from dtogen.transformers.transformer_typescript import TransformerTypescript
+from .interfaces import DtoGenYaml, DtoGenArgs
+from .transformers import (
+    Transformer,
+    TransformerJava,
+    TransformerPython,
+    TransformerTypescript,
+)
 
-from dtogen.filewriters.filewriter import FileWriter
-from dtogen.filewriters.filewriter_java import FileWriterJava
-from dtogen.filewriters.filewriter_python import FileWriterPython
-from dtogen.filewriters.filewriter_typescript import FileWriterTypescript
+from .filewriters import (
+    FileWriter,
+    FileWriterJava,
+    FileWriterPython,
+    FileWriterTypescript,
+)
 
 import yaml
 from mapperr import to_obj
-from dtogen.interfaces import DtoGenYaml, DtoGenArgs
 from typing import Dict
 
 
 class __LangClass:
     transformer: Transformer.__class__
     filewriter: FileWriter.__class__
```

### Comparing `dtogen-0.0.4/dtogen/interfaces.py` & `dtogen-0.0.5/dtogen/interfaces.py`

 * *Files identical despite different names*

### Comparing `dtogen-0.0.4/dtogen.egg-info/PKG-INFO` & `dtogen-0.0.5/dtogen.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: dtogen
-Version: 0.0.4
+Version: 0.0.5
 Summary: DTO generator for Java, TypeScript, Python
 Home-page: https://github.com/mujdecisy/dtogen
 Author: mujdecisy
 Author-email: mujdecisy@gmail.com
 Keywords: python,DTO,generator
 Classifier: Programming Language :: Python :: 3
 Description-Content-Type: text/markdown
```

### Comparing `dtogen-0.0.4/setup.py` & `dtogen-0.0.5/setup.py`

 * *Files 2% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 HERE = os.path.abspath(os.path.dirname(__file__))
 
 with open(os.path.join(HERE, "README.md")) as fid:
     README = fid.read()
 
 setup(
     name="dtogen",
-    version="0.0.4",
+    version="0.0.5",
     description="DTO generator for Java, TypeScript, Python",
     long_description=README,
     long_description_content_type="text/markdown",
     url="https://github.com/mujdecisy/dtogen",
     keywords=["python", "DTO", "generator"],
     author="mujdecisy",
     author_email="mujdecisy@gmail.com",
```

### Comparing `dtogen-0.0.4/test/test_dtogenerator.py` & `dtogen-0.0.5/test/test_dtogenerator.py`

 * *Files identical despite different names*

### Comparing `dtogen-0.0.4/test/test_transform.py` & `dtogen-0.0.5/test/test_transform.py`

 * *Files identical despite different names*

