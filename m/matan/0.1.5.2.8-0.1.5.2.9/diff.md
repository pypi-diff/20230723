# Comparing `tmp/matan-0.1.5.2.8.tar.gz` & `tmp/matan-0.1.5.2.9.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "matan-0.1.5.2.8.tar", last modified: Wed Jun 28 22:27:25 2023, max compression
+gzip compressed data, was "matan-0.1.5.2.9.tar", last modified: Wed Jun 28 22:31:41 2023, max compression
```

## Comparing `matan-0.1.5.2.8.tar` & `matan-0.1.5.2.9.tar`

### file list

```diff
@@ -1,26 +1,26 @@
-drwxr-xr-x   0 uuu       (1000) uuu       (1000)        0 2023-06-28 22:27:25.512509 matan-0.1.5.2.8/
--rw-r--r--   0 uuu       (1000) uuu       (1000)    34670 2023-06-18 20:22:37.000000 matan-0.1.5.2.8/LICENSE
--rw-r--r--   0 uuu       (1000) uuu       (1000)     4357 2023-06-28 22:27:25.512509 matan-0.1.5.2.8/PKG-INFO
--rw-r--r--   0 uuu       (1000) uuu       (1000)     3388 2023-06-28 22:17:10.000000 matan-0.1.5.2.8/README.md
-drwxr-xr-x   0 uuu       (1000) uuu       (1000)        0 2023-06-28 22:27:25.512509 matan-0.1.5.2.8/matan/
--rw-r--r--   0 uuu       (1000) uuu       (1000)       84 2023-06-28 16:35:23.000000 matan-0.1.5.2.8/matan/__init__.py
--rw-r--r--   0 uuu       (1000) uuu       (1000)      156 2023-06-19 18:03:25.000000 matan-0.1.5.2.8/matan/_misc.py
--rw-r--r--   0 uuu       (1000) uuu       (1000)     4960 2023-06-19 18:03:25.000000 matan-0.1.5.2.8/matan/files.py
-drwxr-xr-x   0 uuu       (1000) uuu       (1000)        0 2023-06-28 22:27:25.512509 matan-0.1.5.2.8/matan/polymers/
--rw-r--r--   0 uuu       (1000) uuu       (1000)        0 2023-06-28 16:39:25.000000 matan-0.1.5.2.8/matan/polymers/__init__.py
-drwxr-xr-x   0 uuu       (1000) uuu       (1000)        0 2023-06-28 22:27:25.512509 matan-0.1.5.2.8/matan/polymers/charpy/
--rw-r--r--   0 uuu       (1000) uuu       (1000)      815 2023-06-28 16:39:25.000000 matan-0.1.5.2.8/matan/polymers/charpy/__init__.py
-drwxr-xr-x   0 uuu       (1000) uuu       (1000)        0 2023-06-28 22:27:25.512509 matan-0.1.5.2.8/matan/polymers/tensile/
-drwxr-xr-x   0 uuu       (1000) uuu       (1000)        0 2023-06-28 22:27:25.512509 matan-0.1.5.2.8/matan/polymers/tensile/ISO527/
--rw-r--r--   0 uuu       (1000) uuu       (1000)     2710 2023-06-28 16:39:25.000000 matan-0.1.5.2.8/matan/polymers/tensile/ISO527/__init__.py
--rw-r--r--   0 uuu       (1000) uuu       (1000)    13780 2023-06-28 16:39:25.000000 matan-0.1.5.2.8/matan/polymers/tensile/__init__.py
--rw-r--r--   0 uuu       (1000) uuu       (1000)       33 2023-06-28 16:39:25.000000 matan-0.1.5.2.8/matan/polymers/tensile/misc.py
--rw-r--r--   0 uuu       (1000) uuu       (1000)     7948 2023-06-28 16:39:25.000000 matan-0.1.5.2.8/matan/sample.py
-drwxr-xr-x   0 uuu       (1000) uuu       (1000)        0 2023-06-28 22:27:25.512509 matan-0.1.5.2.8/matan.egg-info/
--rw-r--r--   0 uuu       (1000) uuu       (1000)     4357 2023-06-28 22:27:25.000000 matan-0.1.5.2.8/matan.egg-info/PKG-INFO
--rw-r--r--   0 uuu       (1000) uuu       (1000)      413 2023-06-28 22:27:25.000000 matan-0.1.5.2.8/matan.egg-info/SOURCES.txt
--rw-r--r--   0 uuu       (1000) uuu       (1000)        1 2023-06-28 22:27:25.000000 matan-0.1.5.2.8/matan.egg-info/dependency_links.txt
--rw-r--r--   0 uuu       (1000) uuu       (1000)       17 2023-06-28 22:27:25.000000 matan-0.1.5.2.8/matan.egg-info/requires.txt
--rw-r--r--   0 uuu       (1000) uuu       (1000)        6 2023-06-28 22:27:25.000000 matan-0.1.5.2.8/matan.egg-info/top_level.txt
--rw-r--r--   0 uuu       (1000) uuu       (1000)      103 2023-06-28 22:27:25.512509 matan-0.1.5.2.8/setup.cfg
--rw-r--r--   0 uuu       (1000) uuu       (1000)     1775 2023-06-28 22:27:00.000000 matan-0.1.5.2.8/setup.py
+drwxr-xr-x   0 uuu       (1000) uuu       (1000)        0 2023-06-28 22:31:41.238112 matan-0.1.5.2.9/
+-rw-r--r--   0 uuu       (1000) uuu       (1000)    34670 2023-06-18 20:22:37.000000 matan-0.1.5.2.9/LICENSE
+-rw-r--r--   0 uuu       (1000) uuu       (1000)     4342 2023-06-28 22:31:41.238112 matan-0.1.5.2.9/PKG-INFO
+-rw-r--r--   0 uuu       (1000) uuu       (1000)     3373 2023-06-28 22:30:13.000000 matan-0.1.5.2.9/README.md
+drwxr-xr-x   0 uuu       (1000) uuu       (1000)        0 2023-06-28 22:31:41.238112 matan-0.1.5.2.9/matan/
+-rw-r--r--   0 uuu       (1000) uuu       (1000)       84 2023-06-28 16:35:23.000000 matan-0.1.5.2.9/matan/__init__.py
+-rw-r--r--   0 uuu       (1000) uuu       (1000)      156 2023-06-19 18:03:25.000000 matan-0.1.5.2.9/matan/_misc.py
+-rw-r--r--   0 uuu       (1000) uuu       (1000)     4960 2023-06-19 18:03:25.000000 matan-0.1.5.2.9/matan/files.py
+drwxr-xr-x   0 uuu       (1000) uuu       (1000)        0 2023-06-28 22:31:41.238112 matan-0.1.5.2.9/matan/polymers/
+-rw-r--r--   0 uuu       (1000) uuu       (1000)        0 2023-06-28 16:39:25.000000 matan-0.1.5.2.9/matan/polymers/__init__.py
+drwxr-xr-x   0 uuu       (1000) uuu       (1000)        0 2023-06-28 22:31:41.238112 matan-0.1.5.2.9/matan/polymers/charpy/
+-rw-r--r--   0 uuu       (1000) uuu       (1000)      815 2023-06-28 16:39:25.000000 matan-0.1.5.2.9/matan/polymers/charpy/__init__.py
+drwxr-xr-x   0 uuu       (1000) uuu       (1000)        0 2023-06-28 22:31:41.238112 matan-0.1.5.2.9/matan/polymers/tensile/
+drwxr-xr-x   0 uuu       (1000) uuu       (1000)        0 2023-06-28 22:31:41.238112 matan-0.1.5.2.9/matan/polymers/tensile/ISO527/
+-rw-r--r--   0 uuu       (1000) uuu       (1000)     2710 2023-06-28 16:39:25.000000 matan-0.1.5.2.9/matan/polymers/tensile/ISO527/__init__.py
+-rw-r--r--   0 uuu       (1000) uuu       (1000)    13780 2023-06-28 16:39:25.000000 matan-0.1.5.2.9/matan/polymers/tensile/__init__.py
+-rw-r--r--   0 uuu       (1000) uuu       (1000)       33 2023-06-28 16:39:25.000000 matan-0.1.5.2.9/matan/polymers/tensile/misc.py
+-rw-r--r--   0 uuu       (1000) uuu       (1000)     7948 2023-06-28 16:39:25.000000 matan-0.1.5.2.9/matan/sample.py
+drwxr-xr-x   0 uuu       (1000) uuu       (1000)        0 2023-06-28 22:31:41.238112 matan-0.1.5.2.9/matan.egg-info/
+-rw-r--r--   0 uuu       (1000) uuu       (1000)     4342 2023-06-28 22:31:41.000000 matan-0.1.5.2.9/matan.egg-info/PKG-INFO
+-rw-r--r--   0 uuu       (1000) uuu       (1000)      413 2023-06-28 22:31:41.000000 matan-0.1.5.2.9/matan.egg-info/SOURCES.txt
+-rw-r--r--   0 uuu       (1000) uuu       (1000)        1 2023-06-28 22:31:41.000000 matan-0.1.5.2.9/matan.egg-info/dependency_links.txt
+-rw-r--r--   0 uuu       (1000) uuu       (1000)       17 2023-06-28 22:31:41.000000 matan-0.1.5.2.9/matan.egg-info/requires.txt
+-rw-r--r--   0 uuu       (1000) uuu       (1000)        6 2023-06-28 22:31:41.000000 matan-0.1.5.2.9/matan.egg-info/top_level.txt
+-rw-r--r--   0 uuu       (1000) uuu       (1000)      103 2023-06-28 22:31:41.242112 matan-0.1.5.2.9/setup.cfg
+-rw-r--r--   0 uuu       (1000) uuu       (1000)     1775 2023-06-28 22:30:21.000000 matan-0.1.5.2.9/setup.py
```

### Comparing `matan-0.1.5.2.8/LICENSE` & `matan-0.1.5.2.9/LICENSE`

 * *Files identical despite different names*

### Comparing `matan-0.1.5.2.8/PKG-INFO` & `matan-0.1.5.2.9/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: matan
-Version: 0.1.5.2.8
+Version: 0.1.5.2.9
 Summary: Material analysis package to plot or extract properties like tensile modulus etc. 
 Home-page: https://codeberg.org/MatAn/matan
 Author: Igor Cudnik
 Author-email: igor.cudnik@student.put.poznan.pl
 License: GPLv3
 Project-URL: Documentation, https://matan.codeberg.page
 Keywords: material analysis,ISO 527,ISO 527-1,polymers analysis,material analysis,tensile test,charpy
@@ -24,15 +24,15 @@
 # MaTan
 
 Shortcut comes from **Mat**erial **An**analysis - ultimately is should contains modules allowing user to calculate metals and polymers properties from tensile, HDT (polymers) and DSC tests, as well as the others. There are few similar  packages in PyPI, but none of them I found good to me, so I wrote new one. 
 
 For now it includes:
 - ISO:527-1 (polymers analysis)
 
-# [Documentation]([https://matan.codeberg.page])
+# [Documentation](https://matan.codeberg.page)
 
 
 # Abstract
 
 Nowadays, Python is one of the most popular programming languages, even in non-informatics fields like mechanical engineering, due to its simplicity, and computer analysis solvers using FEM methods are part of almost all components, albeit access to material data is sometimes hard due to inadequate data in the datasheets, problems with calculations, inconsistent information, etc. To overcome this problem, the Python package was created, which allows to calculate the stress, strains, tensile modulus, and other properties from force and elongation data from a machine. For now, it includes only polymer tests according to the ISO-527-1 standard, but in the future, other standards should be included.
 
 Moreover, the package would need a graphical user interface, which could make it even simpler to use and, more importantly, allow users to upload their obtained results into OpenAccess databases and export plastic strains, tensile modulus, and other properties needed to perform FEM and other numerical analysis. That could make FEM methods even more accessible, which would lead to a decrease in the use of unnecessary materials and, due to this, less CO2 pollution.
@@ -50,15 +50,15 @@
 
 path_to_your_CSV = r"path/to/your/CSV"
 
 
 '''
 Be aware that somethimes some software machines uses diffrent encoding! Check the documentation of pandas.read_csv for more
 '''
-test_data_frame = pd.read_csv(path_to_your_CSV)
+df = pd.read_csv(path_to_your_CSV)
 
 elongation_array=df["elongation"]
 force_array=df["force"]
 
 # This uses N ewtons and mm by default to ensure [N/mm^2] as it is equal to MPa
 # by default force units are Newtons and lenght units are mm
 example=mt.sample(name="your sample name",
```

### Comparing `matan-0.1.5.2.8/README.md` & `matan-0.1.5.2.9/README.md`

 * *Files 2% similar despite different names*

```diff
@@ -2,15 +2,15 @@
 # MaTan
 
 Shortcut comes from **Mat**erial **An**analysis - ultimately is should contains modules allowing user to calculate metals and polymers properties from tensile, HDT (polymers) and DSC tests, as well as the others. There are few similar  packages in PyPI, but none of them I found good to me, so I wrote new one. 
 
 For now it includes:
 - ISO:527-1 (polymers analysis)
 
-# [Documentation]([https://matan.codeberg.page])
+# [Documentation](https://matan.codeberg.page)
 
 
 # Abstract
 
 Nowadays, Python is one of the most popular programming languages, even in non-informatics fields like mechanical engineering, due to its simplicity, and computer analysis solvers using FEM methods are part of almost all components, albeit access to material data is sometimes hard due to inadequate data in the datasheets, problems with calculations, inconsistent information, etc. To overcome this problem, the Python package was created, which allows to calculate the stress, strains, tensile modulus, and other properties from force and elongation data from a machine. For now, it includes only polymer tests according to the ISO-527-1 standard, but in the future, other standards should be included.
 
 Moreover, the package would need a graphical user interface, which could make it even simpler to use and, more importantly, allow users to upload their obtained results into OpenAccess databases and export plastic strains, tensile modulus, and other properties needed to perform FEM and other numerical analysis. That could make FEM methods even more accessible, which would lead to a decrease in the use of unnecessary materials and, due to this, less CO2 pollution.
@@ -28,15 +28,15 @@
 
 path_to_your_CSV = r"path/to/your/CSV"
 
 
 '''
 Be aware that somethimes some software machines uses diffrent encoding! Check the documentation of pandas.read_csv for more
 '''
-test_data_frame = pd.read_csv(path_to_your_CSV)
+df = pd.read_csv(path_to_your_CSV)
 
 elongation_array=df["elongation"]
 force_array=df["force"]
 
 # This uses N ewtons and mm by default to ensure [N/mm^2] as it is equal to MPa
 # by default force units are Newtons and lenght units are mm
 example=mt.sample(name="your sample name",
```

### Comparing `matan-0.1.5.2.8/matan/files.py` & `matan-0.1.5.2.9/matan/files.py`

 * *Files identical despite different names*

### Comparing `matan-0.1.5.2.8/matan/polymers/charpy/__init__.py` & `matan-0.1.5.2.9/matan/polymers/charpy/__init__.py`

 * *Files identical despite different names*

### Comparing `matan-0.1.5.2.8/matan/polymers/tensile/ISO527/__init__.py` & `matan-0.1.5.2.9/matan/polymers/tensile/ISO527/__init__.py`

 * *Files identical despite different names*

### Comparing `matan-0.1.5.2.8/matan/polymers/tensile/__init__.py` & `matan-0.1.5.2.9/matan/polymers/tensile/__init__.py`

 * *Files identical despite different names*

### Comparing `matan-0.1.5.2.8/matan/sample.py` & `matan-0.1.5.2.9/matan/sample.py`

 * *Files identical despite different names*

### Comparing `matan-0.1.5.2.8/matan.egg-info/PKG-INFO` & `matan-0.1.5.2.9/matan.egg-info/PKG-INFO`

 * *Files 4% similar despite different names*

```diff
@@ -1,10 +1,10 @@
 Metadata-Version: 2.1
 Name: matan
-Version: 0.1.5.2.8
+Version: 0.1.5.2.9
 Summary: Material analysis package to plot or extract properties like tensile modulus etc. 
 Home-page: https://codeberg.org/MatAn/matan
 Author: Igor Cudnik
 Author-email: igor.cudnik@student.put.poznan.pl
 License: GPLv3
 Project-URL: Documentation, https://matan.codeberg.page
 Keywords: material analysis,ISO 527,ISO 527-1,polymers analysis,material analysis,tensile test,charpy
@@ -24,15 +24,15 @@
 # MaTan
 
 Shortcut comes from **Mat**erial **An**analysis - ultimately is should contains modules allowing user to calculate metals and polymers properties from tensile, HDT (polymers) and DSC tests, as well as the others. There are few similar  packages in PyPI, but none of them I found good to me, so I wrote new one. 
 
 For now it includes:
 - ISO:527-1 (polymers analysis)
 
-# [Documentation]([https://matan.codeberg.page])
+# [Documentation](https://matan.codeberg.page)
 
 
 # Abstract
 
 Nowadays, Python is one of the most popular programming languages, even in non-informatics fields like mechanical engineering, due to its simplicity, and computer analysis solvers using FEM methods are part of almost all components, albeit access to material data is sometimes hard due to inadequate data in the datasheets, problems with calculations, inconsistent information, etc. To overcome this problem, the Python package was created, which allows to calculate the stress, strains, tensile modulus, and other properties from force and elongation data from a machine. For now, it includes only polymer tests according to the ISO-527-1 standard, but in the future, other standards should be included.
 
 Moreover, the package would need a graphical user interface, which could make it even simpler to use and, more importantly, allow users to upload their obtained results into OpenAccess databases and export plastic strains, tensile modulus, and other properties needed to perform FEM and other numerical analysis. That could make FEM methods even more accessible, which would lead to a decrease in the use of unnecessary materials and, due to this, less CO2 pollution.
@@ -50,15 +50,15 @@
 
 path_to_your_CSV = r"path/to/your/CSV"
 
 
 '''
 Be aware that somethimes some software machines uses diffrent encoding! Check the documentation of pandas.read_csv for more
 '''
-test_data_frame = pd.read_csv(path_to_your_CSV)
+df = pd.read_csv(path_to_your_CSV)
 
 elongation_array=df["elongation"]
 force_array=df["force"]
 
 # This uses N ewtons and mm by default to ensure [N/mm^2] as it is equal to MPa
 # by default force units are Newtons and lenght units are mm
 example=mt.sample(name="your sample name",
```

### Comparing `matan-0.1.5.2.8/setup.py` & `matan-0.1.5.2.9/setup.py`

 * *Files 0% similar despite different names*

```diff
@@ -4,15 +4,15 @@
 
 def readme():
     with open('README.md') as f:
         return f.read()
 
 setup(
     name='matan',
-    version='0.1.5.2.8',
+    version='0.1.5.2.9',
     license='GPLv3',
     author="Igor Cudnik",
     author_email='igor.cudnik@student.put.poznan.pl',
     description='Material analysis package to plot or extract properties like tensile modulus etc. ',
     long_description=readme(),
     long_description_content_type='text/markdown',
     packages=find_packages(),
```

