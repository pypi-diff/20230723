# Comparing `tmp/BERTSimilar-0.2.2.tar.gz` & `tmp/BERTSimilar-0.2.3.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "BERTSimilar-0.2.2.tar", last modified: Sun Jul 23 02:43:54 2023, max compression
+gzip compressed data, was "BERTSimilar-0.2.3.tar", last modified: Sun Jul 23 02:45:51 2023, max compression
```

## Comparing `BERTSimilar-0.2.2.tar` & `BERTSimilar-0.2.3.tar`

### file list

```diff
@@ -1,15 +1,15 @@
-drwxr-xr-x   0 rdp        (501) staff       (20)        0 2023-07-23 02:43:54.374549 BERTSimilar-0.2.2/
-drwxr-xr-x   0 rdp        (501) staff       (20)        0 2023-07-23 02:43:54.373048 BERTSimilar-0.2.2/BERTSimilar/
--rw-r--r--   0 rdp        (501) staff       (20)    23529 2023-07-23 01:37:57.000000 BERTSimilar-0.2.2/BERTSimilar/BERTSimilar.py
--rw-r--r--   0 rdp        (501) staff       (20)       37 2023-07-13 00:23:07.000000 BERTSimilar-0.2.2/BERTSimilar/__init__.py
-drwxr-xr-x   0 rdp        (501) staff       (20)        0 2023-07-23 02:43:54.373918 BERTSimilar-0.2.2/BERTSimilar.egg-info/
--rw-r--r--   0 rdp        (501) staff       (20)    11778 2023-07-23 02:43:54.000000 BERTSimilar-0.2.2/BERTSimilar.egg-info/PKG-INFO
--rw-r--r--   0 rdp        (501) staff       (20)      255 2023-07-23 02:43:54.000000 BERTSimilar-0.2.2/BERTSimilar.egg-info/SOURCES.txt
--rw-r--r--   0 rdp        (501) staff       (20)        1 2023-07-23 02:43:54.000000 BERTSimilar-0.2.2/BERTSimilar.egg-info/dependency_links.txt
--rw-r--r--   0 rdp        (501) staff       (20)      127 2023-07-23 02:43:54.000000 BERTSimilar-0.2.2/BERTSimilar.egg-info/requires.txt
--rw-r--r--   0 rdp        (501) staff       (20)       12 2023-07-23 02:43:54.000000 BERTSimilar-0.2.2/BERTSimilar.egg-info/top_level.txt
--rw-r--r--   0 rdp        (501) staff       (20)     1069 2023-01-01 19:42:33.000000 BERTSimilar-0.2.2/LICENSE.txt
--rw-r--r--   0 rdp        (501) staff       (20)    11778 2023-07-23 02:43:54.374187 BERTSimilar-0.2.2/PKG-INFO
--rw-r--r--   0 rdp        (501) staff       (20)    11254 2023-07-23 02:43:44.000000 BERTSimilar-0.2.2/README.md
--rw-r--r--   0 rdp        (501) staff       (20)       38 2023-07-23 02:43:54.374625 BERTSimilar-0.2.2/setup.cfg
--rw-r--r--   0 rdp        (501) staff       (20)      849 2023-07-23 02:41:26.000000 BERTSimilar-0.2.2/setup.py
+drwxr-xr-x   0 rdp        (501) staff       (20)        0 2023-07-23 02:45:51.521770 BERTSimilar-0.2.3/
+drwxr-xr-x   0 rdp        (501) staff       (20)        0 2023-07-23 02:45:51.520388 BERTSimilar-0.2.3/BERTSimilar/
+-rw-r--r--   0 rdp        (501) staff       (20)    23529 2023-07-23 01:37:57.000000 BERTSimilar-0.2.3/BERTSimilar/BERTSimilar.py
+-rw-r--r--   0 rdp        (501) staff       (20)       37 2023-07-13 00:23:07.000000 BERTSimilar-0.2.3/BERTSimilar/__init__.py
+drwxr-xr-x   0 rdp        (501) staff       (20)        0 2023-07-23 02:45:51.521315 BERTSimilar-0.2.3/BERTSimilar.egg-info/
+-rw-r--r--   0 rdp        (501) staff       (20)    11805 2023-07-23 02:45:51.000000 BERTSimilar-0.2.3/BERTSimilar.egg-info/PKG-INFO
+-rw-r--r--   0 rdp        (501) staff       (20)      255 2023-07-23 02:45:51.000000 BERTSimilar-0.2.3/BERTSimilar.egg-info/SOURCES.txt
+-rw-r--r--   0 rdp        (501) staff       (20)        1 2023-07-23 02:45:51.000000 BERTSimilar-0.2.3/BERTSimilar.egg-info/dependency_links.txt
+-rw-r--r--   0 rdp        (501) staff       (20)      127 2023-07-23 02:45:51.000000 BERTSimilar-0.2.3/BERTSimilar.egg-info/requires.txt
+-rw-r--r--   0 rdp        (501) staff       (20)       12 2023-07-23 02:45:51.000000 BERTSimilar-0.2.3/BERTSimilar.egg-info/top_level.txt
+-rw-r--r--   0 rdp        (501) staff       (20)     1069 2023-01-01 19:42:33.000000 BERTSimilar-0.2.3/LICENSE.txt
+-rw-r--r--   0 rdp        (501) staff       (20)    11805 2023-07-23 02:45:51.521562 BERTSimilar-0.2.3/PKG-INFO
+-rw-r--r--   0 rdp        (501) staff       (20)    11254 2023-07-23 02:43:44.000000 BERTSimilar-0.2.3/README.md
+-rw-r--r--   0 rdp        (501) staff       (20)       38 2023-07-23 02:45:51.521830 BERTSimilar-0.2.3/setup.cfg
+-rw-r--r--   0 rdp        (501) staff       (20)      876 2023-07-23 02:45:45.000000 BERTSimilar-0.2.3/setup.py
```

### Comparing `BERTSimilar-0.2.2/BERTSimilar/BERTSimilar.py` & `BERTSimilar-0.2.3/BERTSimilar/BERTSimilar.py`

 * *Files identical despite different names*

### Comparing `BERTSimilar-0.2.2/BERTSimilar.egg-info/PKG-INFO` & `BERTSimilar-0.2.3/BERTSimilar.egg-info/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,19 +1,19 @@
 Metadata-Version: 2.1
 Name: BERTSimilar
-Version: 0.2.2
+Version: 0.2.3
 Summary: Get Similar Words and Embeddings using BERT Models
 Home-page: https://github.com/rdpahalavan/BERTSimilarWords
 Author: Pahalavan R D
 Author-email: rdpahalavan24@gmail.com
-License: MIT
+License: Apache License 2.0
 Keywords: BERT NLP
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
-Classifier: License :: OSI Approved :: MIT License
+Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.7.0
 Description-Content-Type: text/markdown
 License-File: LICENSE.txt
 
 # BERTSimilar
```

### Comparing `BERTSimilar-0.2.2/LICENSE.txt` & `BERTSimilar-0.2.3/LICENSE.txt`

 * *Files identical despite different names*

### Comparing `BERTSimilar-0.2.2/PKG-INFO` & `BERTSimilar-0.2.3/PKG-INFO`

 * *Files 0% similar despite different names*

```diff
@@ -1,19 +1,19 @@
 Metadata-Version: 2.1
 Name: BERTSimilar
-Version: 0.2.2
+Version: 0.2.3
 Summary: Get Similar Words and Embeddings using BERT Models
 Home-page: https://github.com/rdpahalavan/BERTSimilarWords
 Author: Pahalavan R D
 Author-email: rdpahalavan24@gmail.com
-License: MIT
+License: Apache License 2.0
 Keywords: BERT NLP
 Platform: UNKNOWN
 Classifier: Programming Language :: Python :: 3
-Classifier: License :: OSI Approved :: MIT License
+Classifier: License :: OSI Approved :: Apache Software License
 Classifier: Operating System :: OS Independent
 Requires-Python: >=3.7.0
 Description-Content-Type: text/markdown
 License-File: LICENSE.txt
 
 # BERTSimilar
```

### Comparing `BERTSimilar-0.2.2/README.md` & `BERTSimilar-0.2.3/README.md`

 * *Files identical despite different names*

### Comparing `BERTSimilar-0.2.2/setup.py` & `BERTSimilar-0.2.3/setup.py`

 * *Files 7% similar despite different names*

```diff
@@ -4,25 +4,25 @@
     requirements = f.read().splitlines()
 
 with open("README.md", "r", encoding="utf-8") as f:
     long_description = f.read()
 
 setuptools.setup(
     name='BERTSimilar',
-    version='0.2.2',
+    version='0.2.3',
     description="Get Similar Words and Embeddings using BERT Models",
     keywords="BERT NLP",
     long_description=long_description,
     long_description_content_type="text/markdown",
-    license='MIT',
+    license='Apache License 2.0',
     author="Pahalavan R D",
     author_email='rdpahalavan24@gmail.com',
     packages=['BERTSimilar'],
     python_requires='>=3.7.0',
     url='https://github.com/rdpahalavan/BERTSimilarWords',
     classifiers=[
         "Programming Language :: Python :: 3",
-        "License :: OSI Approved :: MIT License",
+        "License :: OSI Approved :: Apache Software License",
         "Operating System :: OS Independent",
     ],
     install_requires=requirements
 )
```

