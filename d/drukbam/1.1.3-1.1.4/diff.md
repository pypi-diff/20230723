# Comparing `tmp/drukbam-1.1.3.tar.gz` & `tmp/drukbam-1.1.4.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "drukbam-1.1.3.tar", max compression
+gzip compressed data, was "drukbam-1.1.4.tar", max compression
```

## Comparing `drukbam-1.1.3.tar` & `drukbam-1.1.4.tar`

### file list

```diff
@@ -1,10 +1,10 @@
--rw-r--r--   0        0        0    15495 2023-07-22 10:22:08.767745 drukbam-1.1.3/DrukBam/MapPlot.py
--rw-r--r--   0        0        0    15779 2023-07-22 10:30:31.051968 drukbam-1.1.3/DrukBam/PlotCalc.py
--rw-r--r--   0        0        0       36 2023-07-22 10:22:08.768745 drukbam-1.1.3/DrukBam/__init__.py
--rw-r--r--   0        0        0     6326 2023-07-22 10:22:08.768745 drukbam-1.1.3/DrukBam/__main__.py
--rw-r--r--   0        0        0    10929 2023-07-22 10:22:08.769745 drukbam-1.1.3/DrukBam/bamCalc.py
--rw-r--r--   0        0        0      388 2023-07-22 10:22:08.769745 drukbam-1.1.3/DrukBam/classic.ini
--rw-r--r--   0        0        0      799 2023-07-22 10:22:08.769745 drukbam-1.1.3/DrukBam/setup.py
--rw-r--r--   0        0        0     2183 2023-07-22 10:22:08.769745 drukbam-1.1.3/DrukBam/vcfParse.py
--rw-r--r--   0        0        0      646 2023-07-22 10:34:23.806286 drukbam-1.1.3/pyproject.toml
--rw-r--r--   0        0        0      735 1970-01-01 00:00:00.000000 drukbam-1.1.3/PKG-INFO
+-rw-r--r--   0        0        0    15495 2023-07-22 10:22:08.767745 drukbam-1.1.4/DrukBam/MapPlot.py
+-rw-r--r--   0        0        0    15779 2023-07-22 10:30:31.051968 drukbam-1.1.4/DrukBam/PlotCalc.py
+-rw-r--r--   0        0        0       36 2023-07-22 10:22:08.768745 drukbam-1.1.4/DrukBam/__init__.py
+-rw-r--r--   0        0        0     6326 2023-07-22 10:22:08.768745 drukbam-1.1.4/DrukBam/__main__.py
+-rw-r--r--   0        0        0    10929 2023-07-22 10:22:08.769745 drukbam-1.1.4/DrukBam/bamCalc.py
+-rw-r--r--   0        0        0      388 2023-07-22 10:22:08.769745 drukbam-1.1.4/DrukBam/classic.ini
+-rw-r--r--   0        0        0      799 2023-07-22 10:22:08.769745 drukbam-1.1.4/DrukBam/setup.py
+-rw-r--r--   0        0        0     2183 2023-07-22 10:22:08.769745 drukbam-1.1.4/DrukBam/vcfParse.py
+-rw-r--r--   0        0        0      645 2023-07-23 09:34:34.812699 drukbam-1.1.4/pyproject.toml
+-rw-r--r--   0        0        0      727 1970-01-01 00:00:00.000000 drukbam-1.1.4/PKG-INFO
```

### Comparing `drukbam-1.1.3/DrukBam/MapPlot.py` & `drukbam-1.1.4/DrukBam/MapPlot.py`

 * *Files identical despite different names*

### Comparing `drukbam-1.1.3/DrukBam/PlotCalc.py` & `drukbam-1.1.4/DrukBam/PlotCalc.py`

 * *Files identical despite different names*

### Comparing `drukbam-1.1.3/DrukBam/__main__.py` & `drukbam-1.1.4/DrukBam/__main__.py`

 * *Files identical despite different names*

### Comparing `drukbam-1.1.3/DrukBam/bamCalc.py` & `drukbam-1.1.4/DrukBam/bamCalc.py`

 * *Files identical despite different names*

### Comparing `drukbam-1.1.3/DrukBam/setup.py` & `drukbam-1.1.4/DrukBam/setup.py`

 * *Files identical despite different names*

### Comparing `drukbam-1.1.3/DrukBam/vcfParse.py` & `drukbam-1.1.4/DrukBam/vcfParse.py`

 * *Files identical despite different names*

### Comparing `drukbam-1.1.3/pyproject.toml` & `drukbam-1.1.4/pyproject.toml`

 * *Files 18% similar despite different names*

```diff
@@ -1,22 +1,22 @@
 [tool.poetry]
 name = "DrukBam"
 homepage = "https://github.com/StephanHolgerD/DrukBam"
-version = "1.1.3"
+version = "1.1.4"
 description = "Comandline plotting of sort,indexed bam files"
 authors = ["Stephan Holger Drukewitz"]
 license = "MIT"
 packages = [
     {include = "DrukBam"}
 ]
 
 [tool.poetry.dependencies]
 python = "^3.7.1"
 cython = '^0.29'
-pysam = "^0.16.0"
+pysam = "0.21.0"
 pandas = "^1.2.4"
 matplotlib = "^3.4.2"
 tqdm = "^4.61.1"
 
 
 [build-system]
 requires = ["poetry-core>=1.0.0"]
```

### Comparing `drukbam-1.1.3/PKG-INFO` & `drukbam-1.1.4/PKG-INFO`

 * *Files 15% similar despite different names*

```diff
@@ -1,19 +1,19 @@
 Metadata-Version: 2.1
 Name: drukbam
-Version: 1.1.3
+Version: 1.1.4
 Summary: Comandline plotting of sort,indexed bam files
 Home-page: https://github.com/StephanHolgerD/DrukBam
 License: MIT
 Author: Stephan Holger Drukewitz
 Requires-Python: >=3.7.1,<4.0.0
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Programming Language :: Python :: 3
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
 Classifier: Programming Language :: Python :: 3.11
 Requires-Dist: cython (>=0.29,<0.30)
 Requires-Dist: matplotlib (>=3.4.2,<4.0.0)
 Requires-Dist: pandas (>=1.2.4,<2.0.0)
-Requires-Dist: pysam (>=0.16.0,<0.17.0)
+Requires-Dist: pysam (==0.21.0)
 Requires-Dist: tqdm (>=4.61.1,<5.0.0)
```

