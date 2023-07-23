# Comparing `tmp/dijkstra_conda-97830512.tar.gz` & `tmp/dijkstra_conda-98567413.tar.gz`

## filetype from file(1)

```diff
@@ -1 +1 @@
-gzip compressed data, was "dijkstra_conda-97830512.tar", last modified: Sun Jul 23 04:01:23 2023, max compression
+gzip compressed data, was "dijkstra_conda-98567413.tar", last modified: Thu Sep 22 12:50:40 2022, max compression
```

## Comparing `dijkstra_conda-97830512.tar` & `dijkstra_conda-98567413.tar`

### file list

```diff
@@ -1,19 +1,21 @@
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:01:23.695773 dijkstra_conda-97830512/
--rw-r--r--   0 runner    (1001) docker     (123)     1091 2023-07-23 04:01:01.000000 dijkstra_conda-97830512/LICENSE
--rw-r--r--   0 runner    (1001) docker     (123)       94 2023-07-23 04:01:01.000000 dijkstra_conda-97830512/MANIFEST.in
--rw-r--r--   0 runner    (1001) docker     (123)      899 2023-07-23 04:01:23.695773 dijkstra_conda-97830512/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)     2414 2023-07-23 04:01:01.000000 dijkstra_conda-97830512/README.md
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:01:23.695773 dijkstra_conda-97830512/dijkstra_conda/
--rw-r--r--   0 runner    (1001) docker     (123)        0 2023-07-23 04:01:01.000000 dijkstra_conda-97830512/dijkstra_conda/__init__.py
--rw-r--r--   0 runner    (1001) docker     (123)     1371 2023-07-23 04:01:01.000000 dijkstra_conda-97830512/dijkstra_conda/cli.py
--rw-r--r--   0 runner    (1001) docker     (123)     8207 2023-07-23 04:01:01.000000 dijkstra_conda-97830512/dijkstra_conda/ig_path.py
-drwxr-xr-x   0 runner    (1001) docker     (123)        0 2023-07-23 04:01:23.695773 dijkstra_conda-97830512/dijkstra_conda.egg-info/
--rw-r--r--   0 runner    (1001) docker     (123)      899 2023-07-23 04:01:23.000000 dijkstra_conda-97830512/dijkstra_conda.egg-info/PKG-INFO
--rw-r--r--   0 runner    (1001) docker     (123)      390 2023-07-23 04:01:23.000000 dijkstra_conda-97830512/dijkstra_conda.egg-info/SOURCES.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 04:01:23.000000 dijkstra_conda-97830512/dijkstra_conda.egg-info/dependency_links.txt
--rw-r--r--   0 runner    (1001) docker     (123)       55 2023-07-23 04:01:23.000000 dijkstra_conda-97830512/dijkstra_conda.egg-info/entry_points.txt
--rw-r--r--   0 runner    (1001) docker     (123)        1 2023-07-23 04:01:23.000000 dijkstra_conda-97830512/dijkstra_conda.egg-info/not-zip-safe
--rw-r--r--   0 runner    (1001) docker     (123)      123 2023-07-23 04:01:23.000000 dijkstra_conda-97830512/dijkstra_conda.egg-info/requires.txt
--rw-r--r--   0 runner    (1001) docker     (123)       15 2023-07-23 04:01:23.000000 dijkstra_conda-97830512/dijkstra_conda.egg-info/top_level.txt
--rw-r--r--   0 runner    (1001) docker     (123)       61 2023-07-23 04:01:23.695773 dijkstra_conda-97830512/setup.cfg
--rw-r--r--   0 runner    (1001) docker     (123)     1671 2023-07-23 04:01:01.000000 dijkstra_conda-97830512/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-22 12:50:40.908970 dijkstra_conda-98567413/
+-rw-r--r--   0 runner    (1001) docker     (121)     1091 2022-09-22 12:50:21.000000 dijkstra_conda-98567413/LICENSE
+-rw-r--r--   0 runner    (1001) docker     (121)       94 2022-09-22 12:50:21.000000 dijkstra_conda-98567413/MANIFEST.in
+-rw-r--r--   0 runner    (1001) docker     (121)      848 2022-09-22 12:50:40.908970 dijkstra_conda-98567413/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (121)     3336 2022-09-22 12:50:21.000000 dijkstra_conda-98567413/README.md
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-22 12:50:40.908970 dijkstra_conda-98567413/dijkstra_conda/
+-rw-r--r--   0 runner    (1001) docker     (121)        0 2022-09-22 12:50:21.000000 dijkstra_conda-98567413/dijkstra_conda/__init__.py
+-rw-r--r--   0 runner    (1001) docker     (121)     2035 2022-09-22 12:50:21.000000 dijkstra_conda-98567413/dijkstra_conda/cli.py
+-rw-r--r--   0 runner    (1001) docker     (121)    27197 2022-09-22 12:50:21.000000 dijkstra_conda-98567413/dijkstra_conda/dfs_path_test.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-22 12:50:40.908970 dijkstra_conda-98567413/dijkstra_conda.egg-info/
+-rw-r--r--   0 runner    (1001) docker     (121)      848 2022-09-22 12:50:40.000000 dijkstra_conda-98567413/dijkstra_conda.egg-info/PKG-INFO
+-rw-r--r--   0 runner    (1001) docker     (121)      424 2022-09-22 12:50:40.000000 dijkstra_conda-98567413/dijkstra_conda.egg-info/SOURCES.txt
+-rw-r--r--   0 runner    (1001) docker     (121)        1 2022-09-22 12:50:40.000000 dijkstra_conda-98567413/dijkstra_conda.egg-info/dependency_links.txt
+-rw-r--r--   0 runner    (1001) docker     (121)       55 2022-09-22 12:50:40.000000 dijkstra_conda-98567413/dijkstra_conda.egg-info/entry_points.txt
+-rw-r--r--   0 runner    (1001) docker     (121)        1 2022-09-22 12:50:40.000000 dijkstra_conda-98567413/dijkstra_conda.egg-info/not-zip-safe
+-rw-r--r--   0 runner    (1001) docker     (121)      141 2022-09-22 12:50:40.000000 dijkstra_conda-98567413/dijkstra_conda.egg-info/requires.txt
+-rw-r--r--   0 runner    (1001) docker     (121)       15 2022-09-22 12:50:40.000000 dijkstra_conda-98567413/dijkstra_conda.egg-info/top_level.txt
+-rw-r--r--   0 runner    (1001) docker     (121)       61 2022-09-22 12:50:40.908970 dijkstra_conda-98567413/setup.cfg
+-rw-r--r--   0 runner    (1001) docker     (121)     1612 2022-09-22 12:50:21.000000 dijkstra_conda-98567413/setup.py
+drwxr-xr-x   0 runner    (1001) docker     (121)        0 2022-09-22 12:50:40.908970 dijkstra_conda-98567413/test/
+-rw-r--r--   0 runner    (1001) docker     (121)      276 2022-09-22 12:50:21.000000 dijkstra_conda-98567413/test/test_dijkstra-conda.py
```

### Comparing `dijkstra_conda-97830512/LICENSE` & `dijkstra_conda-98567413/LICENSE`

 * *Files identical despite different names*

### Comparing `dijkstra_conda-97830512/PKG-INFO` & `dijkstra_conda-98567413/dijkstra_conda.egg-info/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,23 +1,22 @@
 Metadata-Version: 2.1
-Name: dijkstra_conda
-Version: 97830512
+Name: dijkstra-conda
+Version: 98567413
 Summary: A test project
 Home-page: https://github.com/iHeadWater/dijkstra-conda
 Author: dijkstra_conda-test
 License: MIT
 Keywords: dijkstra_conda
 Classifier: Development Status :: 2 - Pre-Alpha
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Natural Language :: English
 Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
-Classifier: Programming Language :: Python :: 3.11
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Programming Language :: Python :: Implementation :: PyPy
 License-File: LICENSE
 
 https://readthedocs.org/projects/calctest/
```

### Comparing `dijkstra_conda-97830512/dijkstra_conda.egg-info/PKG-INFO` & `dijkstra_conda-98567413/PKG-INFO`

 * *Files 6% similar despite different names*

```diff
@@ -1,23 +1,22 @@
 Metadata-Version: 2.1
-Name: dijkstra-conda
-Version: 97830512
+Name: dijkstra_conda
+Version: 98567413
 Summary: A test project
 Home-page: https://github.com/iHeadWater/dijkstra-conda
 Author: dijkstra_conda-test
 License: MIT
 Keywords: dijkstra_conda
 Classifier: Development Status :: 2 - Pre-Alpha
 Classifier: Intended Audience :: Developers
 Classifier: License :: OSI Approved :: MIT License
 Classifier: Natural Language :: English
 Classifier: Programming Language :: Python :: 3.6
 Classifier: Programming Language :: Python :: 3.7
 Classifier: Programming Language :: Python :: 3.8
 Classifier: Programming Language :: Python :: 3.9
 Classifier: Programming Language :: Python :: 3.10
-Classifier: Programming Language :: Python :: 3.11
 Classifier: Programming Language :: Python :: Implementation :: CPython
 Classifier: Programming Language :: Python :: Implementation :: PyPy
 License-File: LICENSE
 
 https://readthedocs.org/projects/calctest/
```

### Comparing `dijkstra_conda-97830512/setup.py` & `dijkstra_conda-98567413/setup.py`

 * *Files 17% similar despite different names*

```diff
@@ -24,27 +24,25 @@
     author='dijkstra_conda-test',
     url='https://github.com/iHeadWater/dijkstra-conda',
     packages=[
         'dijkstra_conda',
     ],
     package_dir={'dijkstra_conda': 'dijkstra_conda'},
     include_package_data=True,
-    install_requires=['geopandas>=0.12.2', 'pytest>=7.1.3', 'setuptools>=63.4.1', 'click>=8.1.3', 'pandas>=1.4.3',
-                      'shapely>=2.0.1', 'pyogrio>=0.4.2', 'igraph>=0.10.4'],
+    install_requires=['pytest>=7.1.3','setuptools>=63.4.1','click>=8.1.3','geopandas>=0.11.1','bidict>=0.21.2','multidict>=6.0.2','networkx>=2.8.6','pandas>=1.4.3','shapely>=1.8.4'],
     license='MIT',
     zip_safe=False,
     keywords='dijkstra_conda',
     classifiers=[
         'Development Status :: 2 - Pre-Alpha',
         'Intended Audience :: Developers',
         'License :: OSI Approved :: MIT License',
         'Natural Language :: English',
         "Programming Language :: Python :: 3.6",
         "Programming Language :: Python :: 3.7",
         "Programming Language :: Python :: 3.8",
         "Programming Language :: Python :: 3.9",
         "Programming Language :: Python :: 3.10",
-        "Programming Language :: Python :: 3.11",
         "Programming Language :: Python :: Implementation :: CPython",
         'Programming Language :: Python :: Implementation :: PyPy',
     ],
 )
```

